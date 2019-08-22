---
title: 標準ユーザー承認テスト (UAT) データベースのコピーのエクスポート
description: このトピックでは、Microsoft Dynamics 365 for Finance and Operations のデータベース エクスポート シナリオについて説明します。
author: LaneSwenka
manager: AnnBe
ms.date: 07/08/2019
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
ms.openlocfilehash: 2ffdd62adb98dacb4dc9af66ed23908fa9932ed1
ms.sourcegitcommit: 9de43b1c2ba0291550545baecaeef52673bcdb9e
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 07/15/2019
ms.locfileid: "1754733"
---
# <a name="export-a-copy-of-the-standard-user-acceptance-testing-uat-database"></a>標準ユーザー承認テスト (UAT) データベースのコピーのエクスポート

[!include [banner](../includes/banner.md)]

データベース移動操作は、データ アプリケーション ライフ サイクル管理 (DataALM) の一部として使用できる一連のセルフ サービスのアクションです。 このチュートリアルでは、サンドボックス標準ユーザー受け入れテスト (UAT) からすべてのデータおよびトランザクションをエクスポートする方法を示します。

このチュートリアルでは、次の方法について説明します。

> [!div class="checklist"]
> * UAT 環境を更新します。
> * Microsoft Dynamics Lifecycle Services (LCS) の資産ライブラリへのエクスポートを実行します。
> * データベース バックアップをダウンロードします。
> * データベースをインポートし、開発者環境で使用できるようにそれを準備します。

このシナリオの例として、Microsoft Dynamics 365 for Finance and Operations を既に稼働している顧客が、開発環境に生産トランザクションの最新のコピーを読み込もうとしています。 これにより、顧客は特定のトランザクションをデバッグしたり、または実際的なデータセットを使用して新しい機能とレポートを開発できます。

## <a name="known-limitations"></a>既知の制限

Microsoft Azure SQL データベース プラットフォームによる最新の制限があるため、200 GB よりも大きい場合はデータベースのエクスポートをお勧めしません。 大規模なデータベースをエクスポートする必要がある場合、SQL データベースが大規模なエクスポートをサポートするまで[レガシー ドキュメント](https://github.com/MicrosoftDocs/dynamics-365-unified-operations-public/blob/b86878500e79f0fe0488c9aedf3fd38b30749fd4/articles/dev-itpro/database/copy-database-from-azure-sql-to-sql-server.md)を使用することをお勧めします。 この推奨事項は、更新操作ではなくエクスポート操作に適用されることに注意してください。 更新操作は、サイズが最大 4 TB のデータベースをサポートできます。

## <a name="prerequisites"></a>必要条件

更新操作を行うには、実稼働環境を配置している必要があります。または標準的な UAT 環境を 2 つ以上持つ必要があります。 このチュートリアルを完了するには、開発者環境が配置されている必要があります。

## <a name="refresh-the-uat-environment"></a>UAT 環境を更新

この更新操作は、生産データベースの最新のコピーで UAT 環境を上書きします。 この手順を完了するには、[トレーニング目的での更新](dbmovement-scenario-general-refresh.md)の手順に従います。

## <a name="back-up-to-the-asset-library"></a>資産ライブラリへのバックアップ

[!include [dbmovement-export](../includes/dbmovement-export.md)]

## <a name="import-the-database"></a>データベースのインポート

データベース バックアップ (.bacpac) ファイルをダウンロードした後、レベル 1 環境の手動インポート操作を開始することができます。 データベースをインポートするときは、これらのガイドラインに従うことお勧めします。

- 必要な場合は、後で戻すことができるように、既存の AxDB データベースのコピーを保持します。
- **AxDB\_fromProd** などの新しい名前の下に新しいデータベースをインポートします。

最高のパフォーマンスを保証するには、\*.bacpac ファイルをインポート元のローカル コンピューターにコピーします。 **コマンド プロンプト** ウィンドウを開き、次のコマンドを実行します。

```
cd C:\Program Files (x86)\Microsoft SQL Server\140\DAC\bin

SqlPackage.exe /a:import /sf:D:\Exportedbacpac\my.bacpac /tsn:localhost /tdn:<target database name> /p:CommandTimeout=1200
```

パラメータの説明を以下に示します。

- **tsn (ターゲット サーバー名)** – インポートする Microsoft SQL Server インスタンスの名前。
- **tdn(ターゲット データベース名)** – インポートするデータベースの名前。 データベースが既に存在していては**いけません**。
- **sf(ソース ファイル)** – インポートするファイルのパスと名前。

> [!NOTE]
> インポート中に、ユーザー名およびパスワードは必要ありません。 既定では、SQL Server は、現在サインインしているユーザーに対して Microsoft Windows 認証を使用します。

## <a name="update-the-database"></a>データベースの更新

インポートされたデータベースに対して、次の SQL スクリプトを実行します。 このスクリプトは、ソース データベースから削除したユーザーを追加し、この SQL Server インスタンスの SQL のログインに正しくリンクします。 スクリプトはまた、変更の追跡を元に戻します。 必ず、データベースの名前を使用できるように、最後の **ALTER DATABASE** ステートメントを編集してください。

```
CREATE USER axdeployuser FROM LOGIN axdeployuser
EXEC sp_addrolemember 'db_owner', 'axdeployuser'

CREATE USER axdbadmin FROM LOGIN axdbadmin
EXEC sp_addrolemember 'db_owner', 'axdbadmin'

CREATE USER axmrruntimeuser FROM LOGIN axmrruntimeuser
EXEC sp_addrolemember 'db_datareader', 'axmrruntimeuser'
EXEC sp_addrolemember 'db_datawriter', 'axmrruntimeuser'

CREATE USER axretaildatasyncuser FROM LOGIN axretaildatasyncuser
EXEC sp_addrolemember 'DataSyncUsersRole', 'axretaildatasyncuser'

CREATE USER axretailruntimeuser FROM LOGIN axretailruntimeuser
EXEC sp_addrolemember 'UsersRole', 'axretailruntimeuser'
EXEC sp_addrolemember 'ReportUsersRole', 'axretailruntimeuser'

CREATE USER axdeployextuser FROM LOGIN axdeployextuser
EXEC sp_addrolemember 'DeployExtensibilityRole', 'axdeployextuser'

CREATE USER [NT AUTHORITY\NETWORK SERVICE] FROM LOGIN [NT AUTHORITY\NETWORK SERVICE]
EXEC sp_addrolemember 'db_owner', 'NT AUTHORITY\NETWORK SERVICE'

UPDATE T1
SET T1.storageproviderid = 0
    , T1.accessinformation = ''
    , T1.modifiedby = 'Admin'
    , T1.modifieddatetime = getdate()
FROM docuvalue T1
WHERE T1.storageproviderid = 1 --Azure storage

DROP PROCEDURE IF EXISTS SP_ConfigureTablesForChangeTracking
DROP PROCEDURE IF EXISTS SP_ConfigureTablesForChangeTracking_V2
GO
-- Begin Refresh Retail FullText Catalogs
DECLARE @RFTXNAME NVARCHAR(MAX);
DECLARE @RFTXSQL NVARCHAR(MAX);
DECLARE retail_ftx CURSOR FOR
SELECT OBJECT_SCHEMA_NAME(object_id) + '.' + OBJECT_NAME(object_id) fullname FROM SYS.FULLTEXT_INDEXES
    WHERE FULLTEXT_CATALOG_ID = (SELECT TOP 1 FULLTEXT_CATALOG_ID FROM SYS.FULLTEXT_CATALOGS WHERE NAME = 'COMMERCEFULLTEXTCATALOG');
OPEN retail_ftx;
FETCH NEXT FROM retail_ftx INTO @RFTXNAME;

BEGIN TRY
    WHILE @@FETCH_STATUS = 0 
    BEGIN 
        PRINT 'Refreshing Full Text Index ' + @RFTXNAME;
        EXEC SP_FULLTEXT_TABLE @RFTXNAME, 'activate';
        SET @RFTXSQL = 'ALTER FULLTEXT INDEX ON ' + @RFTXNAME + ' START FULL POPULATION';
        EXEC SP_EXECUTESQL @RFTXSQL;
        FETCH NEXT FROM retail_ftx INTO @RFTXNAME;
    END
END TRY
BEGIN CATCH
    PRINT error_message()
END CATCH

CLOSE retail_ftx; 
DEALLOCATE retail_ftx; 
-- End Refresh Retail FullText Catalogs
```

### <a name="turn-on-change-tracking"></a>変更追跡を有効にする

ソース データベースで変更追跡が有効になっている場合は、ターゲット環境の新たなプロビジョニング データベースで有効にしてください。 変更追跡を有効にするには、**ALTER DATABASE** コマンドを使用します。

```
ALTER DATABASE [your database name] SET CHANGE_TRACKING = ON (CHANGE_RETENTION = 6 DAYS, AUTO_CLEANUP = ON);
```

新しいデータベースで店舗の業務手順の現在のバージョン (変更追跡に関連する) が使用されていることを保証するには、データ管理のデータ エンティティの変更追跡をオンまたはオフにする必要があります。 任意のエンティティを選択します。 ストアド プロシージャの更新を起動するには、この手順が必要です。

## <a name="start-to-use-the-new-database"></a>新しいデータベースの使用を開始します。

環境を切り替えて新しいデータベースを使用するには、最初に次のサービスを停止します。

- World Wide Web 公開サービス
- Microsoft Dynamics 365 Unified Operations: バッチ管理サービス
- Management Reporter 2012 処理サービス

これらのサービスが停止した後、AxDB データベース **AxDB\_orig** の名前を変更し、新しくインポートしたデータベース **AxDB** の名前を変更し、そして 3 つのサービスを再起動します。

元のデータベースに戻すには、このプロセスを逆にします。 つまり、サービスを停止し、データベースの名前を変更してから、サービスを再起動します。

### <a name="reprovision-the-target-environment"></a>対象の環境を再プロビジョニング

[!include [environment-reprovision](../includes/environment-reprovision.md)]

### <a name="reset-the-financial-reporting-database"></a>財務報告データベースのリセット

財務報告を使用する場合は、[データベースを復元した後の財務報告のデータ マートのリセット](../analytics/reset-financial-reporting-datamart-after-restore.md)の手順に従って、財務報告データベースをリセットする必要があります。 (財務報告は以前は Management Reporter という名前でした)

## <a name="reenter-data-from-encrypted-and-environment-specific-fields-in-the-target-database"></a>ターゲット データベースの暗号化された環境固有のフィールドからデータを再入力

Finance and Operations クライアントでは、暗号化された環境固有のフィールドに記録した値を入力します。 次のフィールドが影響されます。 フィールド名は *Table.Field* 形式で指定されます。

| フィールド名                                               | 値を設定する場所 |
|----------------------------------------------------------|------------------------|
| CreditCardAccountSetup.SecureMerchantProperties          | **売掛金勘定** &gt; **支払設定** &gt; **支払サービス** を選択します。 |
| ExchangeRateProviderConfigurationDetails.Value           | **総勘定元帳** &gt; **通貨** &gt; **為替レート プロバイダーを構成する** を選択します。 |
| FiscalEstablishment\_BR.ConsumerEFDocCsc                 | **組織管理** &gt; **会計機関** &gt; **会計機関** の順に移動します。 |
| FiscalEstablishmentStaging.CSC                           | このフィールドは、データ インポート/エクスポート フレームワーク (DIXF) によって使用されます。 |
| HcmPersonIdentificationNumber.PersonIdentificationNumber | **人事管理** &gt; **作業者** &gt; **作業者** の順に選択します。 **ワーカー**タブの、**個人情報**グループで、**ID 番号**を選択します。 |
| HcmWorkerActionHire.PersonIdentificationNumber           | このフィールドは、Microsoft Dynamics AX 7.0 以降 (2016 年 2 月) は廃止されました。 これは以前、**すべての作業者アクション** フォーム (**人事管理** &gt; **作業者** &gt; **アクション** &gt; **すべての作業者アクション**) でした。 |
| SysEmailSMTPPassword.Password                            | **システム管理** &gt; **電子メール** &gt; **電子メール パラメーター** の順に選択します。 |
| SysOAuthUserTokens.EncryptedAccessToken                  | このフィールドは、アプリケーション オブジェクト サーバー (AOS) により内部で使用されています。 これは無視できます。 |
| SysOAuthUserTokens.EncryptedRefreshToken                 | このフィールドは、AOS で内部的に使用されます。 これは無視できます。 |

## <a name="community-tools"></a>コミュニティ ツール

開発者環境にバックアップ ファイルをインポートするための他のツールをお探しですか。 他の情報源を次に示します。

* [D365fo.Tools](https://github.com/d365collaborative/d365fo.tools/blob/development/docs/Import-D365Bacpac.md) には、コミュニティによって作成された多くの貴重なツールがあります。
* [GitHub でコミュニティによって提供されたオープン ソース プロジェクト](https://github.com/search?q=dynamics+365+finance+operations&s=stars)。

## <a name="known-issues"></a>既知の問題

### <a name="the-export-database-is-in-a-preparation-failed-state"></a>エクスポート データベースが「準備に失敗しました」状態

LCS からのオートメーションがタイムアウトした場合、エクスポート データベースの状態が **準備に失敗しました** に変わります。 アセット ライブラリにエクスポートするエクスポート操作は、引き続き SQL データベースで実行されています。 この問題を解決するには、**再開** を使用してプロセスと SQL データベースを再接続できます。 その後、プロセスが正常に完了します。

### <a name="the-export-database-takes-a-very-long-time"></a>エクスポート データベースに時間が非常にかかる

最近、Azure SQL チームは、サイズが 200 GB を超えるデータベースの場合、LCS が使用するインポート/エクスポート アプリケーション プログラミング インターフェイス (API) の実行時間が変化すると発表しました。 この問題が発生した場合、[UAT データベースに直接 DevTest 環境を接続](dbmovement-scenario-debugdiag.md)するか、[レガシー ドキュメント](https://github.com/MicrosoftDocs/dynamics-365-unified-operations-public/blob/68eef5b1ef783a62f3139adab236a574457af47e/articles/dev-itpro/database/copy-database-from-azure-sql-to-sql-server.md)に従うことができます。 ご利用の環境では、ポイントインタイム リストア機能が使用可能となっているため、バックアップ目的でのデータベースのエクスポートを推奨しません。

Lifecycle Services チームは、インポート/エクスポート API のパフォーマンスを改善するために Azure SQL チームと直接協力しており、LCS の将来のリリースで修正する予定です。

### <a name="i-cant-download-management-studio-installation-files"></a>Management Studio インストール ファイルをダウンロードできません

Microsoft SQL Server Management Studio インストーラーをダウンロードしようとすると、次のエラー メッセージが表示される場合があります。

> 現在のセキュリティ設定では、このファイルをダウンロードすることはできません。

この問題を回避するには、次の手順を実行してファイルのダウンロードを有効にします。

1. Web ブラウザーで**インターネット オプション**を開きます。
2. **セキュリティ**タブで、**インターネット**ゾーンを選択し、**レベルのカスタマイズ**を選択します。
3. **ダウンロード** までスクロールし、**ファイルのダウンロード** で **有効にする** オプションを選択します。

### <a name="database-synchronization-fails"></a>データベース同期の失敗

データベースを Microsoft Visual Studio から新しくインポートされたデータベースと同期させると、その同期は失敗することがあり、次のエラー メッセージが表示される場合があります。

> コード 1 で終了した SQL connection syncengine.exe のオープンに失敗しました。

この場合、次のメッセージも Windows アプリケーション ログのイベント ID 140 で記録されます。

> オブジェクト サーバー データベース シンクロナイザー: データベースに格納されている内部システム テーブル バージョン番号が、カーネル (141/138) でサポートされているバージョンよりも大きくなっています。 新しい Microsoft Dynamics カーネルを使用するか、-REPAIR コマンドライン パラメーターを使用して Microsoft Dynamics を起動し、同期を強制します。

この問題は、現在の環境のプラットフォーム ビルド番号がソース環境のプラットフォーム ビルド番号よりも低い場合に発生する可能性があります。 問題を解決するには、状況に応じて、次のいずれかのステップを実行します。

- LCS で環境ページの **更新** タイルを使用し、ソース環境のプラットフォームに一致するように現在の環境のプラットフォームをアップグレードします。
- データベースで必要なバージョンを調整する次のクエリを実行します。

    ```
    UPDATE SQLSYSTEMVARIABLES

    SET VALUE = 138

    WHERE PARM = 'SYSTABVERSION'
    ```

    > [!NOTE]
    > このクエリの値 **138** は、この特定の環境でバージョン 138 が予想されるイベント ログ メッセージから取得されます。

### <a name="performance"></a>パフォーマンス

次のガイドラインは、最適なパフォーマンスを達成するのに役立ちます。

- 常に .bacpac ファイルを SQL Server インスタンスを実行するコンピューターにローカルでインポートします。 リモート マシンで Management Studio からインポートしないでください。
- Azure でホストされている Finance and Operations 1 ボックス環境では、インポートするときに D ドライブに .bacpac ファイルを配置します。 (ワンボックス環境はレベル 1 環境とも呼ばれます。) Azure 仮想マシン (VM) 上でのテンポラリー ドライブに関する詳細については、[Windows Azure 仮想マシンのテンポラリー ドライブを理解する](https://blogs.msdn.microsoft.com/mast/2013/12/06/understanding-the-temporary-drive-on-windows-azure-virtual-machines/) ブログ投稿を参照してください。
- SQL Server Windows サービス [インスタンス ファイルの初期化](https://msdn.microsoft.com/library/ms175935.aspx) を実行するアカウントに権限を付与します。 この方法で、インポート処理の速度および \*.bak ファイルからの復元の速度を向上させることができます。 開発者環境では、axlocaladmin アカウントとして実行する SQL Server を設定することにより、SQL Server サービスを実行するアカウントがこれらの権限を持っていることを簡単に確認することができます。
