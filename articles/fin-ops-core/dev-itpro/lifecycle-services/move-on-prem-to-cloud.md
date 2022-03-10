---
title: LCS 実装プロジェクトをオンプレミスからクラウドに移動する
description: このトピックでは、Microsoft Dynamics 365 Finance + Operations (オンプレミス) 環境をクラウドに移行する方法について説明します。
author: MartinWalkerDynSA
ms.date: 02/02/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: IT Pro
ms.reviewer: sericks
ms.search.region: Global
ms.author: marwalke
ms.search.validFrom: 2020-09-30
ms.dyn365.ops.version: 10.0.13
ms.openlocfilehash: a771527e04f9ea13edb2496cf69040c2778a922234ea6f43eeb70920957f5120
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/05/2021
ms.locfileid: "6745162"
---
# <a name="move-lcs-implementation-projects-from-on-premises-to-the-cloud"></a>LCS 実装プロジェクトをオンプレミスからクラウドに移動する

[!include [banner](../includes/banner.md)]

このトピックでは、独自のインフラストラクチャでホストされている Microsoft Dynamics 365 Finance + Operations (オンプレミス) 環境を Azure クラウドに移動する方法について説明します。

## <a name="cloud-subscription-licenses"></a>クラウド サブスクリプション ライセンス

クラウド サブスクリプション ライセンスをまだお持ちでない場合は、クラウド サービス プロバイダーまたはボリューム ライセン スリセラーと協力して、 Azure Active Directory (Azure AD) テナントで必要なサブスクリプションを取得してアクティブ化します。 ユーザーおよびアドオン環境のすべてのサブスクリプションを有効にする必要があります。

## <a name="configure-lcs-cloud-implementation-project"></a>LCS クラウドの実装プロジェクトを構成する

以前に Azure AD テナントで Finance and Operations クラウド名のユーザー サブスクリプション ライセンスがアクティブ化されていない場合、新しい Microsoft Dynamics Lifecycle Services (LCS) クラウド実装プロジェクトが自動的にプロビジョニングされます。 それ以外の場合は、サポート要求を開いて LCS クラウドの実装プロジェクトを作成する必要があります。 詳細については、[1 つの Azure AD テナントでの複数の LCS プロジェクトと運用環境](../../fin-ops/get-started/implement-multiple-projects-aad-tenant.md) を参照してください。

LCS クラウドの実装プロジェクトが作成されたら、完全に構成する必要があります。 この構成の一部として、ユーザー、Azure DevOps DevOps アソシエーション、サブスクリプションの見積りを追加し、アセット ライブラリおよびビジネス プロセス モデラー (BPM) などに入力する必要があります。

> [!NOTE]
> プロジェクトのオンボードしている間、ソースシステムとして **AX 2012 アップグレード** を選択する必要があります。これにより、エラスティック プールの代わりにシングルトンの Azure SQL データベースがサンドボックスに使用されます。 最終的には、オンプレミスの **Finance and Operations** など、より適切なオプションが利用可能となります。

## <a name="complete-development-and-testing-of-updated-integrations"></a>更新された統合の開発とテストの完了

おそらく、Finance + Operations (オンプレミス) 環境とのインターフェイスに使用した統合デザイン パターンにいくつかの変更を加える必要があります。 これらの変更はかなりのものになる可能性があり、それらの詳細な説明はこのトピックの範囲を超えています。 ただし、すべてのインターフェイスを評価して、それらに適切な変更を行う必要があります。

元のインターフェースと同じコードベースで共存できるように、更新されたインターフェースを開発することを検討する必要があります。 このアプローチにより、オンプレミスからクラウドへの移行期間中のコード ライフサイクル管理が簡素化されます。 このアプローチが不可能な場合は、クラウドの運用開始を通じて新しい開発ブランチを管理する必要があります。 移行期間中のこの新しいブランチの管理を簡素化するために、他のコード変更を可能な限り凍結することをお勧めします。 さらに、詳細なカットオーバー計画では、古いインターフェイスを無効にし、新しいインターフェイスを有効化する手順を慎重に文書化する必要があります。

## <a name="do-a-trial-migration-and-resolve-issues"></a>試用版の移行を実行し、問題を解決する

1. 階層 2 環境を展開します。
2. オンプレミスの運用環境 (または、必要に応じて、前のセクションで説明したクラウド統合開発ブランチからの現在のビルド) に適用されるのと同じコード パッケージを適用します。 このコード パッケージは、独立系ソフトウェア ベンダー (ISV) のソリューションとライセンスを含む単一の完全な展開可能なパッケージである必要があります。
3. SQL Server Management Studio (SSMS) では、サンドボックス データベースに対して次の Transact-SQL (T-SQL) コマンドを実行し、現在の管理者アカウントと Azure AD テナント ID 情報、およびデータ管理フレームワーク (DMF) 共有作業ディレクトリをそのデータベースに保持します。 結果を保存します。

    ```sql
    SELECT SID,NETWORKALIAS,NETWORKDOMAIN,IDENTITYPROVIDER from USERINFO WHERE ID = 'Admin'
    SELECT VALUE from SYSSERVICECONFIGURATIONSETTING where name = 'TENANTID'
    SELECT TENANTID from POWERBICONFIG
    SELECT TENANTID from PROVISIONINGMESSAGETABLE
    SELECT TENANTID from B2BINVITATIONCONFIG
    SELECT TENANTID from RETAILSHAREDPARAMETER
    SELECT SHAREDFOLDERPATH from DMFPARAMETERS
    ```

4. データベースをオンプレミスからオンラインにコピーします。 使用するエクスポートとインポートのプロセスは、[ゴールデン構成プロモーション](../database/dbmovement-scenario-goldenconfig.md) データベースの移動チュートリアルで説明されているプロセスと同じです。 ただし、この場合、ソース データベースは既存のオンプレミスの実稼動 SQL データベースであり、開発環境にインポートするために説明されている sqlpackage.exe アプローチを使用する必要があります。 代わりに、LCS セルフ サービス データベース インポート オプションを使用する場合は、クリーンアップされるデータ要素に関する警告に記載されているように、一部のデータがインポートされません。 次のコードに示されているプレースホルダーの代わりに、LCS 環境の詳細で使用可能なターゲット データベース情報を使用する必要があります。

    ```powershell
    SqlPackage.exe /a:import /sf:D:\BacpacToImport\my.bacpac /tsn:<Azure SQL database server> /tdn:<target database name> /tu:<axdbadmin user from LCS> /tp:<axdbadmin password from LCS> /p:CommandTimeout=1200
    ```

5. 管理者アカウント、Azure AD テナント ID、および、DMF 共有ディレクトリの値を復元します。 また、**SF** スキーマとそのテーブルが存在する場合は削除します。

    ```sql
    UPDATE USERINFO SET SID='<preserved SID>', NETWORKALIAS='<preserved NETWORKALIAS>', NETWORKDOMAIN='<preserved NETWORKDOMAIN>', IDENTITYPROVIDER='<preserved IDENTITYPROVIDER>' WHERE ID = 'Admin'
    UPDATE SYSSERVICECONFIGURATIONSETTING set VALUE='<preserved VALUE>' where name = 'TENANTID'
    UPDATE POWERBICONFIG SET TENANTID='<preserved TENANTID>'
    UPDATE PROVISIONINGMESSAGETABLE SET TENANTID='<preserved TENANTID>'
    UPDATE B2BINVITATIONCONFIG SET TENANTID='<preserved TENANTID>'
    UPDATE RETAILSHAREDPARAMETER SET TENANTID='<preserved TENANTID>'
    UPDATE DMFPARAMETERS SET SHAREDFOLDERPATH='<preserved SHAREDFOLDERPATH>'
    DROP TABLE IF EXISTS SYNCLOG
    DROP TABLE IF EXISTS SYNCLOCK
    DROP SCHEMA IF EXISTS SF
    ```

6. 他のすべてのユーザーを再インポートし、適切なセキュリティ ロールを割り当てます。
7. クラウド環境での直接印刷は、ドキュメント回覧エージェント (DRA) を介して行われます。 [ネットワーク印刷を有効にしてドキュメント回覧エージェントをインストール](../analytics/install-document-routing-agent.md) の説明に従ってサンドボックス DRA を設定し、回帰テストに印刷シナリオを含めることができます。
8. ドキュメント処理の添付ファイルをクラウドにコピーします。 ドキュメント処理の添付ファイルはデータベースに保存されません。 保存する必要がある場合は、個別に移動する必要があります。 手順については、このトピックで後述する[サンドボックスへの添付ファイルを処理するドキュメントの移行](#migrate-document-handling-attachments-to-your-sandbox) セクションを参照してください。
9. 完全な回帰テスト サイクルを実行します。 このサイクルには、統合のテストを含める必要があります。
10. テスト中に検出された問題を解決します。 各問題ごとに、サンドボックスで行った修正調整を文書化して追跡し、オンプレミスソースで繰り返します。 オンプレミス環境で変更を加えてはならない場合は、その環境の正しい機能と互換性がないため、移行プロセスの繰り返しごとに手動で適用するのではなく、DMF データパッケージを作成することをお勧めします。
11. すべてのテストが成功し、コードまたは構成に変更が加えられなくなるまで、手順 2 ～ 10 を繰り返します。

## <a name="repeat-the-migration-to-production"></a>実稼働への移行の繰り返し

1. 新しい運用環境を展開します。 通常の前提条件が適用されることに注意してください。 たとえば、有効なサブスクリプションの見積もりツールが必要であり、運用フェーズの前に LCS の方法のフェーズを完了し、FastTrack 準備レビューを完了する必要があります。 詳細については、「[Go-Live の準備](../../fin-ops/imp-lifecycle/prepare-go-live.md)」を参照してください。
2. ソフトウェア展開可能パッケージの最終バージョンを実稼働に適用します。
3. オンプレミスの運用環境に対するデータの変更を中止します。
4. [試用版の移行と問題の解決](#do-a-trial-migration-and-resolve-issues) セクションで手順 3 ～ 6 を繰り返して、最終的な/最新のオンプレミス本番データベースをクラウド サンドボックスにコピーします。
5. [試用版の移行と問題の解決](#do-a-trial-migration-and-resolve-issues) セクションで手順 8 を繰り返して、添付ファイルを処理する最終/最新のドキュメントをクラウドサンドボックスにコピーします。
6. サンドボックスから実稼働へのデータベースの更新を要求します。 (このプロセスは、ゴールデン構成データベースを実稼働にプロモートするために使用されるプロセスと同じです。)
7. サポートリクエストを開いて、Dynamics サービス エンジニアリング にドキュメント処理の添付ファイルをサンド ボックス ストレージ アカウントから実稼働ストレージ アカウントにコピーさせ、本番データベースの DocuValue テーブルと DocuDeletedValue テーブルの参照を更新します。 要求が完了したら、添付ファイルがドキュメント処理レコードのサンプルに使用できるかどうかを確認します。
8. 実稼働用の DRA を設定します。 試用版の移行の一部として以前にインストールされた DRA のいずれかを再利用する場合は、サンドボックス URL ではなく、実稼働 URL に接続するように構成を更新するようにしてください。
9. カットオーバー計画で詳しく説明されているように、クラウドとオンプレミスの運用環境を調整します。
10. 運用開始のサインオフを取得します。
11. クラウド プロダクション インターフェイス、バッチジョブなどをアクティブ化します。
12. クラウド運用環境での取引を開始します。

## <a name="migrate-document-handling-attachments-to-your-sandbox"></a>ドキュメント処理の添付ファイルをサンドボックスに移行

Finance + Operations (オンプレミス) 環境のドキュメント処理添付ファイルは、ファイル共有に格納されます。 ただし、クラウド バージョンはこのファイル共有をサポートしていません。 次の手順を使用して、添付ファイルをサンドボックス環境の Azure ストレージ アカウントにコピーし、データベース内の対応するメタデータを更新できます。 その後の実稼働への昇格のために、Dynamics サービス エンジニアリングは添付ファイルをサンドボックスから実稼働にコピーするように要求できます。

1. <!--HERE-->添付ファイルを処理するドキュメントのコピーを、オンプレミスの実稼働ファイル共有から、Application Object Server (AOS) のサンドボックス インスタンスの 1 つにある一時フォルダーにアップロードします。 たとえば、添付ファイルの ZIP ファイルをアップロードし、ターゲットで展開することができます。 リモート デスクトップ アクセスがない場合 (たとえば、セルフ サービス環境など) は、代わりに別の仮想マシン (VM) を使用できます。 妥当な変換パフォーマンスを得るには、この VM をターゲット サンドボックスと同じ Azure データセンターに配置する必要があります。 AOS インスタンスを使用していない場合は、サンドボックスの SQL データベース インスタンスへのアクセスの許可リストに VM を追加する必要があります。
2. サポート リクエストを開いて、サンドボックス Azure ストレージ アカウントの名前と、ドキュメント コンテナの時間制限のある共有アクセス署名トークンを取得します。 次の手順で実行する Windows PowerShell スクリプトの対応するプレースホルダーを更新します。 また、LCS の環境の詳細を使用して、一時フォルダーと Finance and Operations トランザクション データベースのプレースホルダーを更新し ます。
3. サンドボックス AOS インスタンスまたはその他の VM で次の Windows PowerShell スクリプトを実行して、ドキュメント処理ファイルをストレージアカウントにアップロードし、各ファイルに必要なメタデータを作成します。

    ```powershell
    #Upload F&O on-prem document handling attachments to Azure storage account
    #
    $filesPath = "<TEMP_ATTACHMENTS_FOLDER_PATH>"
    $dBHostName = "<DATABASE_SERVER>.database.windows.net"
    $dBName = "<DATABASE_NAME>"
    $dBUsername = "<DATABASE_USER>"
    $dBPassword  = "<DATABASE_PASSWORD>"
    $storageAccountName = "<STORAGE_ACCOUNT_NAME>"
    $sasToken = "<SAS_TOKEN>"

    [Reflection.Assembly]::LoadWithPartialName("System.Security.Cryptography") #Load crypto
    $cryptoObj = [System.Security.Cryptography.SHA256]::Create()
    $StorageContext = New-AzStorageContext -StorageAccountName $storageAccountName -SasToken $sasToken
    foreach ($file in Get-ChildItem $filesPath) 
    {
        try
        {
            $blob = (Set-AzStorageBlobContent -Context $StorageContext -Container documents -File $file.FullName -Blob "$($file.Name)" -Force).ICloudBlob
        }
        catch
        {
            Write-Host "Could not upload $($file.Fullname) to blob"
            Write-Host $_
        }
        if($blob)
        {
            #Write-Host "Processing $($file.Fullname)..."
            #FileHash:
            $fileBytes = [System.IO.File]::ReadAllBytes($file.FullName)
            $hashBytes = $cryptoObj.ComputeHash($fileBytes)
            $encodedHash = [System.Convert]::ToBase64String($hashBytes)
            #FullFileName:
            $origFileName = (Invoke-Sqlcmd -Query "SELECT ORIGINALFILENAME FROM DOCUVALUE WHERE FILEID = '$($file.Name)'" -ServerInstance $dBHostName -Database $dBName -Username $dBUsername -Password $dBPassword).ORIGINALFILENAME
            if ($origFileName.Length -eq 0)
            {
                $origFileName = (Invoke-Sqlcmd -Query "SELECT ORIGINALFILENAME FROM DOCUDELETEDVALUE WHERE FILEID = '$($file.Name)'" -ServerInstance $dBHostName -Database $dBName -Username $dBUsername -Password $dBPassword).ORIGINALFILENAME
            }
            if ($origFileName.Length -eq 0)
            {
                Write-Host "Missing DOCUVALUE $($file.Name)"
            }
            else
            {
                $nameBytes  = [System.Text.Encoding]::UTF8.GetBytes($origFileName)
                $encodedName =  [System.Convert]::ToBase64String($nameBytes)
                #Write-Host "Base64 encoded original filename $encodedName."
                $blob.Metadata["FileHash"] = $encodedHash
                $blob.Metadata["FileSize"] = $file.Length
                $blob.Metadata["FullFileName"] = $encodedName
                $blob.SetMetadata()
                Write-Host "Uploaded $($file.Fullname)"
            }
        }
    }
    ```

4. SSMS で、次の T-SQL コマンドを実行して、DocuValue レコードと DocuDeletedValue レコードを更新し、ターゲットの保存場所を参照するようにします。

    ```sql
    update DOCUVALUE
    set ACCESSINFORMATION = replace(ACCESSINFORMATION, 'file://<SOURCE_PREFIX>/documents/', 'https://<STORAGE_ACCOUNT>.blob.core.windows.net/documents/'), STORAGEPROVIDERID = 1
    where STORAGEPROVIDERID = 4 --4 for LBD filesystem, 1 for Azure blob
    and ACCESSINFORMATION like 'file://<SOURCE_PREFIX>/documents/%'

    update DOCUDELETEDVALUE
    set ACCESSINFORMATION = replace(ACCESSINFORMATION, 'file://<SOURCE_PREFIX>/documents/', 'https://<STORAGE_ACCOUNT>.blob.core.windows.net/documents/'), STORAGEPROVIDERID = 1
    where STORAGEPROVIDERID = 4 --4 for LBD filesystem, 1 for Azure blob
    and ACCESSINFORMATION like 'file://<SOURCE_PREFIX>/documents/%'
    ```

5. ドキュメント処理の添付ファイルのサンプルをテストして、サンドボックス環境でアクセスできるようになったことを確認します。


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
