---
title: データベースのエクスポート
description: このトピックでは、Microsoft Dynamics 365 for Finance and Operations のデータベースをエクスポートする方法について説明します。
author: LaneSwenka
manager: AnnBe
ms.date: 08/15/2019
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
ms.openlocfilehash: 7f168cb57c3ac2cc459a5a6c7c7f66521b5597e3
ms.sourcegitcommit: 6ff2c25d859c435106192e07c9ef0a9067c1e8d0
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/16/2019
ms.locfileid: "1886616"
---
# <a name="export-a-database"></a>データベースのエクスポート

[!include [banner](../includes/banner.md)]

サンドボックス ユーザー受け入れテスト (UAT) 環境からアセット ライブラリへの Dynamics 365 for Finance and Operations のデータベースのエクスポートの実行に Microsoft Dynamics Lifecycle Services (LCS) を使用できます。

## <a name="self-service-export-database"></a>セルフ サービスエクスポート データベース

[!include [dbmovement-export](../includes/dbmovement-export.md)]

### <a name="export-operation-failure"></a>エクスポート操作失敗

エクスポート操作が正常に行われない場合は、*ロールバック*できます。 操作が最初に失敗した後に**ロールバック** オプションをクリックすると、ソース サンドボックス環境がエクスポートの開始前の状態に戻されます。

失敗の根本原因を特定するには、ロールバック操作を開始する前に、使用可能なボタンを使用して Runbook ログをダウンロードします。

### <a name="data-elements-that-arent-exported"></a>エクスポートされないデータ要素

環境からデータベース バックアップをエクスポートするときは、バックアップ ファイルにエクスポートされないデータベース要素があります。 次にいくつか例を挙げます。

* LogisticsElectronicAddress テーブル内の電子メール アドレス。
* BatchJobHistory、BatchHistory、および BatchConstraintHistory テーブルのバッチ ジョブ履歴。
* SysEmailSMTPPassword テーブルの SMTP パスワード。
* SysEmailParameters テーブルの SMTP 中継サーバー。
* PrintMgmtSettings と PrintMgmtDocInstance テーブルの印刷管理設定。
* SysServerConfig、SysServerSessions、SysCorpNetPrinters、SysClientSessions、BatchServerConfig、および BatchServerGroup テーブル内の環境固有のレコード。
* DocuValue テーブル内のドキュメント添付ファイル。 これには元の環境で無効化されたオフィスのテンプレートが含まれます。
* PersonnellIntegrationConfiguration テーブルの接続文字列
* 管理者以外のすべてのユーザーは **無効** のステータスに設定されます。
* すべてのバッチ ジョブは、 **保留** 状態に設定されます。

### <a name="known-issues"></a>既知の問題

#### <a name="export-ran-for-some-time-and-then-reached-a-preparation-failed-state"></a>エクスポートはしばらく実行され、「準備に失敗しました」の状態になります。

エクスポート プロセスは、大規模なデータベースが関係する Azure SQL データベースではタイムアウトすることがあります。 場合によっては、LCS から **再開** アクションを使用してエクスポート プロセスを復元することができます、 Lifecycle Services チームは既知のエラー コードを認識するよう努めており、データベースのエクスポート操作のログにこれらを追加することで、ユーザーが問題を解決できるようにします。 LCS の将来のリリースでは、これらの既知のエラー コードが追加されます。 問題が発生した場合は、以下の「手動エクスポート」セクションに従って手動でのエクスポートを行うことができます。

#### <a name="export-doesnt-show-any-progress-in-lcs"></a>エクスポートで LCS に進捗状況が表示されない

エクスポートのプロセスは、他のデータベース移動の操作および、ランブックを使用しない一般的なパッケージ展開とは異なります。 したがって、LCS の進行状況インジケーターには、それ以外のシナリオのような出力が表示されません。 LCSチームは、このようなエラー コードをエクスポート データベース操作のログに追加してユーザーが問題を解決できるようにするべく、既知のエラー コードの識別作業を行っています。 LCS の将来のリリースでは、これらの既知のエラー コードが追加されます。 問題が発生した場合は、以下の「手動エクスポート」セクションに従って手動でのエクスポートを行うことができます。

## <a name="manual-export"></a>手動エクスポート

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

### <a name="create-a-copy-of-the-source-database"></a>ソース データベースのコピーを作成します。

ソースの Azure SQL データベースをエクスポートする前に、変更の追跡を無効にし、データベース ユーザーを削除する必要があるため、データベースのコピーを作成する必要があります。 これによって元のデータベースから情報を削除するかわりに、コピーを使用して作業することができます。 以下の SQL ステートメントは、axdb\_mySourceDatabaseToCopy データベースのコピーを **MyNewCopy**という名前で作成します。 以下のスクリプトを編集して、ご利用のデータベースの名称を使用してください。

```
CREATE DATABASE MyNewCopy AS COPY OF axdb_mySourceDatabaseToCopy
```

このSQL ステートメントは非同期です。 つまり、1分ほどで処理が完了したようにみえても、バックグラウンドでは処理が継続しています。 詳細については、 [データベースの作成 (Azure SQL データベース)](https://msdn.microsoft.com/en-us/library/dn268335.aspx)。 コピーの進行状況を監視するには、同じインタンスのMASTERデータベースに対して以下のクエリを実行してください。

```
SELECT * FROM sys.dm_database_copies
```

> [!WARNING] 
> どの Finance and Operations 環境でも、長期間にわたってデータベースのコピーを保持することはできません。 Microsoft は、事前に通知することなく、7 日を超える古いデータベースのコピーを削除する権限を保有します。

### <a name="prepare-the-database"></a>データベースの準備

以下のスクリプトを実行してデータベースのコピーにて変更の追跡を無効にし、システムビューから SQL Database のユーザーを削除します。 このスクリプトはまた、システムフラグの修正、旧環境に対する参照の削除、バッチ処理の保留、電子メール設定の削除を行います。 データベースを正常にエクスポート/インポートするには、これらすべての変更が必要となります。 これらの変更は、ターゲットとする環境で AOSのコンピューターが開始された際に、自動的に何も開始しないようにすることにも役立ちます。

> [!NOTE]
> 以下の **ALTER DATABASE** コマンドを編集して、データベース コピーの名前を使用する必要があります。

```
--Prepare a database in Azure SQL ddatabase for export to SQL Server.

--Remove certificates in database from Electronic Signature usage
DECLARE @SQLElectronicSig nvarchar(512)
DECLARE certCursor CURSOR for
select 'DROP CERTIFICATE ' + QUOTENAME(c.name) + ';'
from sys.certificates c;
OPEN certCursor;
FETCH certCursor into @SQLElectronicSig;
WHILE @@Fetch_Status = 0
BEGIN
print @SQLElectronicSig;
exec(@SQLElectronicSig);
FETCH certCursor into @SQLElectronicSig;
END;
CLOSE certCursor;
DEALLOCATE certCursor;


-- Re-assign full rext catalogs to [dbo]
BEGIN
    DECLARE @catalogName nvarchar(256);
    DECLARE @sqlStmtTable nvarchar(512)

    DECLARE reassignFullTextCatalogCursor CURSOR
       FOR SELECT DISTINCT name
       FROM sys.fulltext_catalogs 
       
       -- Open cursor and disable on all tables returned
       OPEN reassignFullTextCatalogCursor
       FETCH NEXT FROM reassignFullTextCatalogCursor INTO @catalogName

       WHILE @@FETCH_STATUS = 0
       BEGIN
              SET @sqlStmtTable = 'ALTER AUTHORIZATION ON Fulltext Catalog::[' + @catalogName + '] TO [dbo]'
              EXEC sp_executesql @sqlStmtTable
              FETCH NEXT FROM reassignFullTextCatalogCursor INTO @catalogName
       END
       CLOSE reassignFullTextCatalogCursor
       DEALLOCATE reassignFullTextCatalogCursor
END

--Disable change tracking on tables where it is enabled.
declare
@SQL varchar(1000)
set quoted_identifier off
declare changeTrackingCursor CURSOR for
select 'ALTER TABLE [' + t.name + '] DISABLE CHANGE_TRACKING'
from sys.change_tracking_tables c, sys.tables t
where t.object_id = c.object_id
OPEN changeTrackingCursor
FETCH changeTrackingCursor into @SQL
WHILE @@Fetch_Status = 0
BEGIN
exec(@SQL)
FETCH changeTrackingCursor into @SQL
END
CLOSE changeTrackingCursor
DEALLOCATE changeTrackingCursor

--Disable change tracking on the database itself.
ALTER DATABASE
-- SET THE NAME OF YOUR DATABASE BELOW
MyNewCopy
set CHANGE_TRACKING = OFF

--Change ownership of alternate schemas to DBO
ALTER AUTHORIZATION ON schema::shadow TO [dbo]
ALTER AUTHORIZATION ON schema::[BACKUP] TO [dbo]

--Remove the database level users from the database
--these will be recreated after importing in SQL Server.
declare
@userSQL varchar(1000)
set quoted_identifier off
declare userCursor CURSOR for
select 'DROP USER [' + name + ']'
from sys.sysusers
where issqlrole = 0 and hasdbaccess = 1 and name <> 'dbo'
OPEN userCursor
FETCH userCursor into @userSQL
WHILE @@Fetch_Status = 0
BEGIN
exec(@userSQL)
FETCH userCursor into @userSQL
END
CLOSE userCursor
DEALLOCATE userCursor
--Delete the SYSSQLRESOURCESTATSVIEW view as it has an Azure-specific definition in it.
--We will run db synch later to recreate the correct view for SQL Server.
if(1=(select 1 from sys.views where name = 'SYSSQLRESOURCESTATSVIEW'))
DROP VIEW SYSSQLRESOURCESTATSVIEW
--Next, set system parameters ready for being a SQL Server Database.
update sysglobalconfiguration
set value = 'SQLSERVER'
where name = 'BACKENDDB'
update sysglobalconfiguration
set value = 0
where name = 'TEMPTABLEINAXDB'
--Clean up the batch server configuration, server sessions, and printers from the previous environment.
TRUNCATE TABLE SYSSERVERCONFIG
TRUNCATE TABLE SYSSERVERSESSIONS
TRUNCATE TABLE SYSCORPNETPRINTERS
TRUNCATE TABLE SYSCLIENTSESSIONS
TRUNCATE TABLE BATCHSERVERCONFIG
TRUNCATE TABLE BATCHSERVERGROUP
--Remove records which could lead to accidentally sending an email externally.
UPDATE SysEmailParameters
SET SMTPRELAYSERVERNAME = '', MAILERNONINTERACTIVE = 'SMTP' 
--Remove encrypted SMTP Password record(s)
TRUNCATE TABLE SYSEMAILSMTPPASSWORD
GO
UPDATE LogisticsElectronicAddress
SET LOCATOR = ''
WHERE Locator LIKE '%@%'
GO
TRUNCATE TABLE PrintMgmtSettings
TRUNCATE TABLE PrintMgmtDocInstance
--Set any waiting, executing, ready, or canceling batches to withhold.
UPDATE BatchJob
SET STATUS = 0
WHERE STATUS IN (1,2,5,7)
GO
-- Clear encrypted hardware profile merchand properties
update dbo.RETAILHARDWAREPROFILE set SECUREMERCHANTPROPERTIES = null where SECUREMERCHANTPROPERTIES is not null
```

### <a name="export-the-database"></a>データベースのエクスポート

**コマンド プロンプト** ウィンドウを開き、次のコマンドを実行します。

```
cd C:\Program Files (x86)\Microsoft SQL Server\140\DAC\bin

SqlPackage.exe /a:export /ssn:<server>.database.windows.net /sdn:<database to export> /tf:D:\Exportedbacpac\my.bacpac /p:CommandTimeout=2400 /p:VerifyFullTextDocumentTypesSupported=false /sp:<SQL password> /su:<sql user>
```

パラメータの説明を以下に示します。

- **ssn (source server name)** – エクスポートを行う元の Azure SQL データベース サーバーの名称
- **sdn(ソース データベース名)** – エクスポートするデータベースの名前。
- **tf(ターゲット ファイル)** – エクスポートするファイルのパスと名前。
- **sp (source password)** – エクスポートを行う元の SQL Server のSQL パスワード。
- **su (source user)** – エクスポートを行う元の SQL ユーザー名。 ユーザーには **sqladmin** を使用することを推奨します。 ユーザーは、展開時にすべての Finance and Operations SQL インスタンスで作成されます。 このユーザーのパスワードは、Dynamics Lifecycle Services のプロジェクトから取得できます。

エクスポートの完了後、以下のコマンドを実行してデータベースのコピーを削除します。

```
DROP DATABASE [MyNewCopy]
```
