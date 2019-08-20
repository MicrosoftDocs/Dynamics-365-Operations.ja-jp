---
redirect_url: /dynamics365/unified-operations/dev-itpro/database/dbmovement-operations
title: Finance and Operations データベースを Azure SQL データベースから SQL Server 環境にコピーする
description: このトピックでは、Microsoft Dynamics 365 for Finance and Operations のデータベースを Azure ベースの環境から SQL Server ベースの環境に移動する方法について説明します。
author: laneswenka
manager: AnnBe
ms.date: 01/07/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Developer, IT Pro
ms.reviewer: sericks
ms.search.scope: Operations
ms.custom: 203764
ms.assetid: 45efdabf-1714-4ba4-9a9d-217143a6c6e0
ms.search.region: Global
ms.author: laswenka
ms.search.validFrom: 2016-05-31
ms.dyn365.ops.version: AX 7.0.1
ms.openlocfilehash: fee59f6f4bccfcb2ede41b7d7bcd0b84f7425720
ms.sourcegitcommit: 45f8cea6ac75bd2f4187380546a201c056072c59
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 07/12/2019
ms.locfileid: "1741532"
---
# <a name="copy-finance-and-operations-databases-from-azure-sql-database-to-sql-server-environments"></a>Finance and Operations データベースを Azure SQL データベースから SQL Server 環境にコピーする

[!include [banner](../includes/banner.md)]

このトピックでは、Microsoft Dynamics 365 for Finance and Operations のデータベースを、Microsoft Azure に基づいた環境からエクスポートし、Microsoft SQL Server に基づいた環境にインポートする方法について説明します。

## <a name="overview"></a>概要

データベースを移動するには、セルフ サービス アクションを使用して Azure SQL データベースからデータベースをエクスポートし、Microsoft SQL Server にインポートします。 エクスポートされたデータのファイル名拡張子は .bacpac なので、このプロセスは多くの場合 *bacpac プロセス*と呼ばれます。

データベース移動の高レベルのプロセスには、次のフェーズが含まれます。

1. LCS 資産ライブラリにソース環境をエクスポートします。
2. SQL Server にデータベースをインポートします。
3. データベースの更新のため SQL スクリプトを実行します。

## <a name="prerequisites"></a>必要条件

データベースを移動するには、次の前提条件を満たす必要があります。

- ソース環境 (つまりソース データベースに接続されている環境) は、ターゲット環境が実行されているプラットフォームのバージョンよりも前または同じバージョンの Finance and Operations プラットフォームを実行する必要があります。
- サンドボックス環境データベースのみをエクスポートできます。 実稼働環境をコピーする必要がある場合は、最初に、その環境をサンド ボックス環境に更新する必要があります。 

    > [!NOTE]
    > このトピックでは、*サンドボックス* という用語を使用して SQL Azure データベースに接続されている標準またはプレミア承認テスト (レベル 2 以上)、またはより高度な環境を示します。

- 出力先の SQL Server 環境では、SQL Server 2016 Release to Manufacturing (RTM) (13.00.1601.5) 以降を実行する必要があります。 SQL Server 2016 の Community Technology Preview (CTP) バージョンでは、インポート処理中にエラーが発生する可能性があります。

## <a name="before-you-begin"></a>準備

暗号化された環境固有の値を新しい環境にインポートすることはできません。 インポート処理を完了した後は、ターゲット環境内のソース環境から一部のデータを再入力する必要があります。

### <a name="document-the-values-of-encrypted-fields"></a>暗号化されたフィールドの値を文書化

データ暗号化に使用される証明書に関連する技術的な制限のため、データベースの暗号化されたフィールドに格納されている値はそのデータベースが新しい環境にインポートされた後は読み取れません。 したがって、インポート後、暗号化されたフィールドに格納されている値を手動で削除して再入力する必要があります。 インポート後に暗号化されたフィールドに入力される新しい値は読み取り可能になります。 次のフィールドが影響されます。 フィールド名は Table.Field 形式で指定されます。

| フィールド名                                               | 値を設定する場所 |
|----------------------------------------------------------|------------------------|
| CreditCardAccountSetup.SecureMerchantProperties          | **売掛金勘定** &gt; **支払設定** &gt; **支払サービス** を選択します。 |
| ExchangeRateProviderConfigurationDetails.Value           | **総勘定元帳** &gt; **通貨** &gt; **為替レート プロバイダーを構成する** を選択します。 |
| FiscalEstablishment\_BR.ConsumerEFDocCsc                 | **組織管理** &gt; **会計機関** &gt; **会計機関** の順に移動します。 |
| FiscalEstablishmentStaging.CSC                           | このフィールドは、データ インポート/エクスポート フレームワーク (DIXF) によって使用されます。 |
| HcmPersonIdentificationNumber.PersonIdentificationNumber | **人事管理** &gt; **作業者** &gt; **作業者** の順に選択します。 **ワーカー**タブの、**個人情報**グループで、**ID 番号**を選択します。 |
| HcmWorkerActionHire.PersonIdentificationNumber           | このフィールドは、Microsoft Dynamics AX 7.0 以降 (2016 年 2 月) は廃止されました。 これは以前、**すべての作業者アクション** フォーム (**人事管理** &gt; **作業者** &gt; **アクション** &gt; **すべての作業者アクション**) でした。 |
| SysEmailSMTPPassword.Password                            | **システム管理** &gt; **電子メール** &gt; **電子メール パラメーター** の順に選択します。 |
| SysOAuthUserTokens.EncryptedAccessToken                  | このフィールドは、AOS で内部的に使用されます。 これは無視できます。 |
| SysOAuthUserTokens.EncryptedRefreshToken                 | このフィールドは、AOS で内部的に使用されます。 これは無視できます。 |

### <a name="if-youre-running-retail-components-document-encrypted-and-environment-specific-values"></a>小売コンポーネントを実行している場合は、暗号化された、環境固有の値を文書化します。

次のページの値は、環境固有またはデータベースで暗号化されています。 したがって、インポートされた値はすべて正しくありません。

- 支払サービス (**売掛金勘定** &gt; **支払設定** &gt; **支払サービス**) に移動します。
- ハードウェア プロファイル (**小売りとコマース** &gt; **チャネル設定** &gt; **POS 設定** &gt; **POS プロファイル** &gt; **ハードウェア プロファイル**)

## <a name="self-service-database-export"></a>データベースのセルフ サービスエクスポート

[!include [dbmovement-export](../includes/dbmovement-export.md)]

## <a name="import-the-database"></a>データベースのインポート

.bacpac ファイルをダウンロードした後、レベル 1 環境の手動インポート操作を開始することができます。 データベースをインポートするときは、これらのガイドラインに従うことお勧めします。

- 必要な場合は、後で戻すことができるように、既存の AxDB データベースのコピーを保持します。
- **AxDB\_fromProd** などの新しい名前の下に新しいデータベースをインポートします。

最高のパフォーマンスを確保するには、\*.bacpac ファイルをインポート元のローカル コンピューターにコピーします。 **コマンド プロンプト** ウィンドウを開き、次のコマンドを実行します。

```
cd C:\Program Files (x86)\Microsoft SQL Server\140\DAC\bin

SqlPackage.exe /a:import /sf:D:\Exportedbacpac\my.bacpac /tsn:localhost /tdn:<target database name> /p:CommandTimeout=2400
```

パラメータの説明を以下に示します。

- **tsn(ターゲット サーバー名)** – インポートする SQL Server の名前。
- **tdn(ターゲット データベース名)** – インポートするデータベースの名前。 データベースが既に存在していては**いけません**。
- **sf(ソース ファイル)** – インポートするファイルのパスと名前。

> [!NOTE]
> インポート中に、ユーザー名およびパスワードは必要ありません。 既定では、SQL Server は、現在サインインしているユーザーに対して Microsoft Windows 認証を使用します。

## <a name="update-the-database"></a>データベースの更新

インポートされたデータベースに対して、次の SQL スクリプトを実行します。 このスクリプトは、ソース データベースから削除したユーザーを追加し、この SQL インスタンスの SQL のログインに正しくリンクします。 スクリプトはまた、変更の追跡を元に戻します。 必ず、データベースの名前を使用できるように、最後の **ALTER DATABASE** ステートメントを編集してください。

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

ALTER DATABASE [<your AX database name>] SET CHANGE_TRACKING = ON (CHANGE_RETENTION = 6 DAYS, AUTO_CLEANUP = ON)
GO
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

### <a name="enable-change-tracking"></a>変更追跡の有効化
ソース データベースで変更追跡が有効になっている場合は、ALTER DATABASE コマンドを使用して、ターゲット環境の新たなプロビジョニング データベースで変更追跡を再度有効にしてください。

```
ALTER DATABASE [your database name] SET CHANGE_TRACKING = ON (CHANGE_RETENTION = 6 DAYS, AUTO_CLEANUP = ON);
```

新しいデータベースで店舗の業務手順の現在のバージョン (変更追跡に関連する) が使用されていることを確認するには、データ管理のデータ エンティティの変更追跡を有効または無効にする必要があります。 これは、店舗の業務手順の更新をトリガーするために必要なので、どのエンティティでも実行できます。

## <a name="start-to-use-the-new-database"></a>新しいデータベースの使用を開始します。

環境を切り替えて新しいデータベースを使用するには、最初に次のサービスを停止します。

- World Wide Web 公開サービス
- Microsoft Dynamics 365 Unified Operations: バッチ管理サービス
- Management Reporter 2012 処理サービス

サービスが停止した後、AxDB データベース **AxDB\_orig** の名前を変更し、新しくインポートしたデータベース **AxDB** の名前を変更し、そして 3 つのサービスを再起動します。

データベースの名前を変更するには、次の ALTER DATABASE コマンドを使用します。
```
ALTER DATABASE [your database name] MODIFY NAME = [new database name];
```

元のデータベースに戻すには、このプロセスを逆にします。 つまり、サービスを停止し、データベースの名前を変更してから、サービスを再起動します。

### <a name="re-provision-the-target-environment"></a>対象の環境を再プロビジョニング

[!include [environment-reprovision](../includes/environment-reprovision.md)]

### <a name="reset-the-financial-reporting-database"></a>財務報告データベースのリセット

Management Reporter という以前の名前を持った財務報告を使用する場合は、[データベースを復元した後の財務報告のデータ マートのリセット](../analytics/reset-financial-reporting-datamart-after-restore.md)の手順に従って、財務報告データベースをリセットする必要があります

## <a name="re-enter-data-from-encrypted-and-environment-specific-fields-in-the-target-database"></a>ターゲット データベースの暗号化された環境固有のフィールドからデータを再入力

Finance and Operations クライアントでは、暗号化された環境固有のフィールドに記録した値を入力します。 次のフィールドが影響されます。 フィールド名は Table.Field 形式で指定されます。

| フィールド名                                               | 値を設定する場所 |
|----------------------------------------------------------|------------------------|
| CreditCardAccountSetup.SecureMerchantProperties          | **売掛金勘定** &gt; **支払設定** &gt; **支払サービス** を選択します。 |
| ExchangeRateProviderConfigurationDetails.Value           | **総勘定元帳** &gt; **通貨** &gt; **為替レート プロバイダーを構成する** を選択します。 |
| FiscalEstablishment\_BR.ConsumerEFDocCsc                 | **組織管理** &gt; **会計機関** &gt; **会計機関** の順に移動します。 |
| FiscalEstablishmentStaging.CSC                           | このフィールドは DIXF で使用されます。 |
| HcmPersonIdentificationNumber.PersonIdentificationNumber | **人事管理** &gt; **作業者** &gt; **作業者** の順に選択します。 **ワーカー**タブの、**個人情報**グループで、**ID 番号**を選択します。 |
| HcmWorkerActionHire.PersonIdentificationNumber           | このフィールドは、AX 7.0 以降 (2016 年 2 月) は廃止されました。 これは以前、**すべての作業者アクション** フォーム (**人事管理** &gt; **作業者** &gt; **アクション** &gt; **すべての作業者アクション**) でした。 |
| SysEmailSMTPPassword.Password                            | **システム管理** &gt; **電子メール** &gt; **電子メール パラメーター** の順に選択します。 |
| SysOAuthUserTokens.EncryptedAccessToken                  | このフィールドは、AOS で内部的に使用されます。 これは無視できます。 |
| SysOAuthUserTokens.EncryptedRefreshToken                 | このフィールドは、AOS で内部的に使用されます。 これは無視できます。 |

## <a name="known-issues"></a>既知の問題

### <a name="i-cant-download-management-studio-installation-files"></a>Management Studio インストール ファイルをダウンロードできません

Management Studio インストーラーをダウンロードしようとすると、次のエラー メッセージが表示される場合があります。

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

この問題は、現在の環境のプラットフォーム ビルド番号がソース環境のプラットフォーム ビルド番号よりも低い場合に発生する可能性があります。 状況に応じて、LCS **環境**ページの**更新**タイルを使用して、現在の環境のプラットフォームをソース環境のプラットフォームと一致するようにアップグレードするか、次のクエリを実行してデータベースの必要なバージョンを調整します。

```
UPDATE SQLSYSTEMVARIABLES

SET VALUE = 138

WHERE PARM = 'SYSTABVERSION'
```

> [!NOTE]
> 前のクエリの値 **138** は、この特定の環境でバージョン 138 が予想されるイベント ログ メッセージから取得されます。

### <a name="performance"></a>パフォーマンス

次のガイドラインは、最適なパフォーマンスを達成するのに役立ちます。

- 常に Azure SQL データベースと同じ Azure データ センター内にある仮想マシン (VM) からデータベースをエクスポートします。 サンドボックス データベースのコピーをエクスポートする場合は、サンド ボックス AOS コンピューターからエクスポートします。
- 常に .bacpac ファイルを SQL Server インスタンスを実行するコンピューターにローカルでインポートします。 リモート マシンで Management Studio からインポートしないでください。
- Azure でホストされている Finance and Operations 1 ボックス環境では、インポートするときに D ドライブに .bacpac ファイルを配置します。 (ワンボックス環境はレベル 1 環境とも呼ばれます。) Azure Vm 上でのテンポラリー ドライブに関する詳細については、[Windows Azure 仮想マシンのテンポラリー ドライブを理解する](https://blogs.msdn.microsoft.com/mast/2013/12/06/understanding-the-temporary-drive-on-windows-azure-virtual-machines/) ブログ投稿を参照してください。
- SQL Server Windows サービス [インスタンス ファイルの初期化](https://msdn.microsoft.com/library/ms175935.aspx) を実行するアカウントに権限を付与します。 この方法で、インポート処理の速度および \*.bak ファイルからの復元の速度を向上させることができます。 開発者環境では、axlocaladmin アカウントとして実行する SQL Server を設定することにより、SQL Server サービスを実行するアカウントがこれらの権限を持っていることを簡単に確認することができます。
- 大きなデータベースのメモリ制限が存在する場合があるので、Azure SQLデータベースから、**Management Studio でデータ層アプリケーションのエクスポート**を選択しないでください。
