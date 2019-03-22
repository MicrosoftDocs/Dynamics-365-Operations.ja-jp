---
title: ゴールデン コンフィギュレーション プロモーション
description: このトピックでは、Microsoft Dynamics 365 for Finance and Operations のゴールデン コンフィギュレーション プロモーションについて説明します。
author: LaneSwenka
manager: AnnBe
ms.date: 01/29/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: IT Pro, Developer
ms.reviewer: sericks
ms.search.scope: Operations
ms.search.region: Global
ms.author: laneswenka
ms.search.validFrom: 2019-01-31
ms.dyn365.ops.version: 8.1.3
ms.openlocfilehash: 4e211952765364f97ee9abb983bcff9f6721484c
ms.sourcegitcommit: 0c1deb100d0bf6dacd14b328968bbc7a9d92583a
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/28/2019
ms.locfileid: "771270"
---
# <a name="golden-configuration-promotion"></a>ゴールデン コンフィギュレーション プロモーション

[!include [banner](../includes/banner.md)]

データベース移動操作は、データ アプリケーション ライフ サイクル管理 (DataALM) の一部として使用できる一連のセルフ サービスのアクションです。 「ゴールデン コンフィギュレーション」は、開発者環境が構成ストアとして使用されている Microsoft Dynamics エコシステムにおける顧客とパートナーの間での一般的な方法を示します。 この方法では、実装プロジェクトは、後で会議室パイロット、モック Go-Live、Go-Live の基準とできる際集荷されたグローバルおよび会社固有の設定をデータベースに保存できます。 このチュートリアルでは、ゴールデン構成データベースを準備し、ターゲット ユーザー受け入れテスト (UAT) 環境に取り込む方法を示します。

このチュートリアルでは、次の方法について説明します。

> [!div class="checklist"]
> * Microsoft Azure SQL データベースのゴールデン構成データベースを準備する。
> * ターゲット UAT 環境のインポートを実行する。
> * 実稼働環境に UAT 環境をコピーする。

このシナリオの例として、Microsoft Dynamics 365 for Finance and Operations で Go-Live していない顧客が、代わりに会議室パイロット、モック Go-Live、Go-Live を準備します。 このシナリオでは、開発者環境からのベースライン ゴールド ・ データベースを UAT 環境に昇格し、最終的を生産環境をサポートすることをします。

## <a name="prerequisites"></a>必要条件

このチュートリアルを完了するには、ゴールデン コンフィギュレーション データベースとして管理されるデータベースに配置されている開発者環境が必要です。 少なくとも 1 つの標準 UAT 環境が展開されていることと、必要に応じて、実稼働環境が 1 つ以上必要です。

開発環境は、ターゲット UAT 環境と同じ Finance and Operations の*アプリケーションのバージョン*を実行している必要があります。 加えて、開発者環境の*プラットフォーム バージョン*は、ターゲット UAT 環境のプラットフォーム バージョン以前でなければなりません。

## <a name="before-you-begin"></a>準備

### <a name="supported-sql-server-collation"></a>サポートされる SQL Server の照合順序

クラウドの Finance and Operations データベースでサポートされている唯一の照合順序は、**SQL\_Latin1\_General\_CP1\_CI\_AS** です。 開発環境の Microsoft SQL Server とデータベース照合順序がこの値に設定されていることを確認してください。 また、サンドボックスに発行されたすべてのコンフィギュレーション環境にこの照合順序があることを確認します。

### <a name="document-the-values-of-encrypted-fields"></a>暗号化されたフィールドの値を文書化

暗号化された環境固有の値を新しい環境にインポートすることはできません。 インポート処理を完了した後は、ターゲット環境内のソース環境から一部のデータを再入力する必要があります。

データ暗号化に使用される証明書に関連する技術的な制限のため、データベースの暗号化されたフィールドに格納されている値はそのデータベースが新しい環境にインポートされた後は読み取れません。 したがって、インポート後、暗号化されたフィールドに格納されている値を手動で削除して再入力する必要があります。 インポート後に暗号化されたフィールドに入力される新しい値は読み取り可能になります。 次のフィールドが影響されます。 フィールド名は *Table.Field* 形式で指定されます。

| フィールド名                                               | 値を設定する場所 |
|----------------------------------------------------------|------------------------|
| CreditCardAccountSetup.SecureMerchantProperties          | **売掛金勘定** &gt; **支払設定** &gt; **支払サービス** を選択します。 |
| ExchangeRateProviderConfigurationDetails.Value           | **総勘定元帳** &gt; **通貨** &gt; **為替レート プロバイダーを構成する** を選択します。 |
| FiscalEstablishment\_BR.ConsumerEFDocCsc                 | **組織管理** &gt; **会計機関** &gt; **会計機関** の順に移動します。 |
| FiscalEstablishmentStaging.CSC                           | このフィールドは、データ インポート/エクスポート フレームワーク (DIXF) によって使用されます。 |
| HcmPersonIdentificationNumber.PersonIdentificationNumber | **人事管理** &gt; **作業者** &gt; **作業者** の順に選択します。 **ワーカー**タブの、**個人情報**グループで、**ID 番号**を選択します。 |
| HcmWorkerActionHire.PersonIdentificationNumber           | このフィールドは、Microsoft Dynamics AX 7.0 以降 (2016 年 2 月) は廃止されました。 これは以前、**すべての作業者アクション** ページ (**人事管理** &gt; **作業者** &gt; **アクション** &gt; **すべての作業者アクション**) に表示されていました。 |
| SysEmailSMPTPassword.Password                            | **システム管理** &gt; **電子メール** &gt; **電子メール パラメーター** の順に選択します。 |
| SysOAuthUserTokens.EncryptedAccessToken                  | このフィールドは、アプリケーション オブジェクト サーバー (AOS) により内部で使用されています。 これは無視できます。 |
| SysOAuthUserTokens.EncryptedRefreshToken                 | このフィールドは、AOS で内部的に使用されます。 これは無視できます。 |

### <a name="if-youre-running-retail-components-document-encrypted-and-environment-specific-values"></a>小売コンポーネントを実行している場合は、暗号化された、環境固有の値を文書化します。

次のページの値は、環境固有またはデータベースで暗号化されています。 したがって、インポートされた値はすべて正しくありません。

- 支払サービス (**売掛金勘定** &gt; **支払設定** &gt; **支払サービス**) に移動します。
- ハードウェア プロファイル (**小売りとコマース** &gt; **チャネル設定** &gt; **POS 設定** &gt; **POS プロファイル** &gt; **ハードウェア プロファイル**)

## <a name="create-a-copy-of-the-source-database"></a>ソース データベースのコピーを作成します。

ソース SQL Server データベースをエクスポートする前に、データベース ユーザーを削除する必要があるため、そのデータベースのコピーを作成してください。 元のデータベースを修正する代わりに、コピーで作業することができます。 次のスクリプトは、既定の AxDB データベースをバックアップし、それを新しいインスタンス名に変更して同じインスタンスに復元します。 このスクリプトを使用するには、最初に D:\\backups のパスが存在することを確認します。

```
BACKUP DATABASE [AxDB] TO DISK = N'D:\Backups\axdb_golden.bak' WITH NOFORMAT, NOINIT,
NAME = N'AxDB_golden-Full Database Backup', SKIP, NOREWIND, NOUNLOAD, COMPRESSION, STATS = 10
GO
RESTORE DATABASE [AxDB_CopyForExport] FROM DISK = N'D:\Backups\axdb_golden.bak' WITH FILE = 1,
MOVE N'AXDBBuild_Data' TO N'F:\MSSQL_DATA\AxDB_CopyForExport.mdf',
MOVE N'AXDBBuild_Log' TO N'G:\MSSQL_LOGS\AxDB_CopyForExport_Log.ldf',
NOUNLOAD, STATS = 5
```

## <a name="prepare-the-database"></a>データベースの準備

次のスクリプトを、前のセクションで作成した AxDB\_CopyForExport データベースに対して実行します。 このスクリプトは、次の変更を行います。

- **SysGlobalConfiguration** フラグを設定し、データベースが Azure ベースであることを Finance and Operations に知らせます。
- XU\_DisableEnableNonClusteredIndexes 手順で tempDB への参照を削除します。 Azure SQL データベースでは、tempDB の参照が許可されていません。 データベース同期プロセスは後で照会を再作成します。
- Microsoft Windows のユーザーは Azure SQL データベースで許可されていないため、ユーザーをドロップします。 他のユーザーは、対象のサーバーの適切なサインインに正しくリンクされるように、後で再作成する必要があります。
- 暗号化されたハードウェア プロファイルの商社プロパティの消去。

データベースのエクスポートとインポートに成功するには、これらすべての変更が必要です。

```
update sysglobalconfiguration
set value = 'SQLAZURE'
where name = 'BACKENDDB'

update sysglobalconfiguration
set value = 1
where name = 'TEMPTABLEINAXDB'

drop procedure XU_DisableEnableNonClusteredIndexes
drop procedure if exists SP_ConfigureTablesForChangeTracking
drop procedure if exists SP_ConfigureTablesForChangeTracking_V2
drop schema [NT AUTHORITY\NETWORK SERVICE]
drop user [NT AUTHORITY\NETWORK SERVICE]
drop user axdbadmin
drop user axdeployuser
drop user axmrruntimeuser
drop user axretaildatasyncuser
drop user axretailruntimeuser
drop user axdeployextuser
-- Clear encrypted hardware profile merchant properties
update dbo.RETAILHARDWAREPROFILE set SECUREMERCHANTPROPERTIES = null where SECUREMERCHANTPROPERTIES is not null
```

## <a name="export-the-database-from-sql-server"></a>SQL Server からデータベースをエクスポート

**コマンド プロンプト** ウィンドウを開き、次のコマンドを実行します。

> [!IMPORTANT]
> 140 フォルダに現在のバージョンが反映されます。 サンドボックス環境で使用可能なバージョンを使用する必要があります。 したがって、開発環境に [Microsoft SQL Server Management Studio の最新バージョン](https://msdn.microsoft.com/library/mt238290.aspx)をインストールする必要が生じる場合があります。

```
cd C:\Program Files (x86)\Microsoft SQL Server\140\DAC\bin\
SqlPackage.exe /a:export /ssn:localhost /sdn:<database to export> /tf:D:\Exportedbacpac\my.bacpac /p:CommandTimeout=1200 /p:VerifyFullTextDocumentTypesSupported=false
```

パラメータの説明を以下に示します。

- **ssn(ソース サーバー名)** – エクスポートする SQL Server の名前。 このトピックでは、名前は常に **localhost** である必要があります。
- **sdn(ソース データベース名)** – エクスポートするデータベースの名前。
- **tf(ターゲット ファイル)** – エクスポートするファイルのパスと名前。 フォルダーはすでに存在しているはずですが、エクスポート プロセスによってファイルが作成されます。

## <a name="import-the-database"></a>データベースのインポート

前の手順で作成された .bacpac ファイルを、LCS プロジェクトの資産ライブラリ内の **データベースのバックアップ** セクションにアップロードします。 次に、インポートを開始します。 対象となる UAT 環境のデータベースは、ゴールデン構成データベースによって上書きされます。

[!include [dbmovement-import](../includes/dbmovement-import.md)]

## <a name="perform-master-data-migration"></a>マスター データを移行します。

UAT 環境にゴールデン コンフィギュレーションが適用され、マスター データの移行を開始することができます。 [データ エンティティを使用して](../data-entities/develop-entity-for-data-migration.md)、このデータの移行を行うことができます。 UAT 環境を生産環境にコピーする前にデータ移行アクティビティを完了することをお勧めします。トラブルシューティングのために UAT 環境のデータベースにアクセスするためです。

## <a name="copy-the-sandbox-database-to-production"></a>サンドボックス データベースを生産環境にコピーします。

モック Go-Live または実際の Go-Live を行う準備ができたら、生産環境に UAT 環境をコピーすることができます。 このプロセスは、*切替*と呼ばれます。 実際の Go-Live には複数回切り替えることをお勧めします。 この方法では、Microsoft にコピー操作の実行を依頼する**生産へのサンドボックス** サービス要求を送信するステップを含む、プロセスの各ステップで詳細な時間見積を取得できます。

> [!NOTE]
> 要求には実稼働環境へのコピーが含まれるので、**データベースを最新の情報に更新要求** タイプの要求を使用することはできません。

1. LCS のプロジェクト ホーム ページで、**サービス要求** を選択します。
2. **サービス要求** ページで、**追加** を選択し、**サンドボックスから実稼働環境** を選択します。
3. **サンドボックスから実稼働環境** ダイアログ ボックスで、次の手順に従います。

    1. **環境名**フィールドで、実稼動環境を選択します。
    2. **ダウンタイム開始日を優先** および **ダウンタイム終了日を優先** フィールドを設定します。 サイクル終了日は、サイクル開始日の少なくとも 1 時間後でなければなりません。 要求を実行するためのリソースが確保されるようにするには、推奨ダウンタイム ウィンドウの少なくとも 24 時間前にリクエストを送信してください。
    3. 下部にあるチェック ボックスをオンにして、条項に同意します。

## <a name="reconfigure-environment-specific-settings"></a>環境の固有の設定を変更

更新が完了した後、LCS で**サインオフ** ボタンを使用し、操作を閉じます。 その後、環境固有の設定のコンフィギュレーションを開始できます。

まず、環境にログインします。LCS の**環境の詳細**ページにある管理者アカウントを使用します。 再設定の標準的な領域をいくつか次に示します。 設定およびインストールされている独立系ソフトウェア ベンダー (ISV) ソリューションによっては、追加の再設定が必要です。

* **システム管理**\>**設定**\>**バッチ グループ:** 必要なバッチ サーバー グループにさまざまな AOS インスタンスを追加します。
* **システム管理**\>**設定**\>**エンティティ店舗:** Microsoft Power BI レポートに必要なさまざまなエンティティを更新します。
* **システム管理**\>**設定**\>**システム パラメーター:** タスク ガイドの LCS ヘルプ コンフィギュレーションに環境を再接続します。
* **システム管理**\>**設定**\>**電子メール**\>**パラメータを電子メールで送信:** UAT 環境内で電子メールを使用する場合は、簡易メール転送プロトコル (SMTP) の設定を入力します。
* **システム管理**\>**照会**\>**バッチ ジョブ:** UAT 環境で実行するジョブを選択し、ステータスを **待機中** に更新します。

> [!NOTE]
> ベスト プラクティスとして、定期的なアイテムで実行されるすべてのミッション クリティカル バッチ ジョブが作成され、管理者アカウントで実行される必要があります。 管理者は、`erp@customer.com` など一般的なユーザーである必要があります。 特定の従業員の Azure Active Directory(Azure AD) アカウントにリンクしないでください。従業員が退職すると、そのアカウントは使用できなくなる可能性があるためです。

## <a name="open-the-environment-to-users"></a>ユーザーに環境を開く

必要に応じて、システムを構成する場合は、選択したユーザーが環境にアクセスできるようにできます。 デフォルトでは、管理者と Microsoft サービス アカウントを除くすべてのユーザーが無効になります。

**システム管理**\>**ユーザー**\>**ユーザー** に移動し、UAT 環境へのアクセスが必要なユーザーを有効にします。 多くのユーザーを有効にする必要がある場合、[Microsoft Excel アドイン](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/office-integration/use-excel-add-in#open-entity-data-in-excel-when-you-start-from-finance-and-operations)を使用してこのタスクをすばやく完了できます。

## <a name="community-tools"></a>コミュニティ ツール

開発者環境からバックアップ ファイルを準備するための他のツールをお探しですか。 他の情報源を次に示します。

* [D365fo.Tools](https://github.com/d365collaborative/d365fo.tools/blob/development/docs/Import-D365Bacpac.md) には、コミュニティによって作成された多くの貴重なツールがあります。
* [GitHub でコミュニティによって提供されたオープン ソース プロジェクト](https://github.com/search?q=dynamics+365+finance+operations&s=stars)。
