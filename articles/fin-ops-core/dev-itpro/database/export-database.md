---
title: データベースのエクスポート
description: このトピックでは、Finance and Operations アプリケーションのデータベースをエクスポートする方法について説明します。
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
ms.openlocfilehash: 4fb690a1228ad42581dc243ce87494914f7d002e
ms.sourcegitcommit: 2460d0da812c45fce67a061386db52e0ae46b0f3
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/30/2019
ms.locfileid: "2249317"
---
# <a name="export-a-database"></a><span data-ttu-id="c94ad-103">データベースのエクスポート</span><span class="sxs-lookup"><span data-stu-id="c94ad-103">Export a database</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="c94ad-104">サンドボックス ユーザー受け入れテスト (UAT) 環境からアセット ライブラリへのデータベースのエクスポートに Microsoft Dynamics Lifecycle Services (LCS) を使用できます。</span><span class="sxs-lookup"><span data-stu-id="c94ad-104">You can use Microsoft Dynamics Lifecycle Services (LCS) to export a database from a sandbox user acceptance testing (UAT) environment to the Asset library.</span></span>

## <a name="self-service-export-database"></a><span data-ttu-id="c94ad-105">セルフ サービスエクスポート データベース</span><span class="sxs-lookup"><span data-stu-id="c94ad-105">Self-service export database</span></span>

[!include [dbmovement-export](../includes/dbmovement-export.md)]

### <a name="export-operation-failure"></a><span data-ttu-id="c94ad-106">エクスポート操作失敗</span><span class="sxs-lookup"><span data-stu-id="c94ad-106">Export operation failure</span></span>

<span data-ttu-id="c94ad-107">エクスポート操作が正常に行われない場合は、*ロールバック*できます。</span><span class="sxs-lookup"><span data-stu-id="c94ad-107">If the export operation isn't successful, you can do a *rollback*.</span></span> <span data-ttu-id="c94ad-108">操作が最初に失敗した後に**ロールバック** オプションをクリックすると、ソース サンドボックス環境がエクスポートの開始前の状態に戻されます。</span><span class="sxs-lookup"><span data-stu-id="c94ad-108">If you select the **Rollback** option after the initial failure of the operation, your source sandbox environment is restored to the state that it was in before the export began.</span></span>

<span data-ttu-id="c94ad-109">失敗の根本原因を特定するには、ロールバック操作を開始する前に、使用可能なボタンを使用して Runbook ログをダウンロードします。</span><span class="sxs-lookup"><span data-stu-id="c94ad-109">To determine the root cause of the failure, download the runbook logs by using the available buttons before you start the rollback operation.</span></span>

### <a name="data-elements-that-arent-exported"></a><span data-ttu-id="c94ad-110">エクスポートされないデータ要素</span><span class="sxs-lookup"><span data-stu-id="c94ad-110">Data elements that aren't exported</span></span>

<span data-ttu-id="c94ad-111">環境からデータベース バックアップをエクスポートするときは、バックアップ ファイルにエクスポートされないデータベース要素があります。</span><span class="sxs-lookup"><span data-stu-id="c94ad-111">When you export a database backup from an environment, some elements of the database aren't exported in the backup file.</span></span> <span data-ttu-id="c94ad-112">次にいくつか例を挙げます。</span><span class="sxs-lookup"><span data-stu-id="c94ad-112">Here are some examples:</span></span>

* <span data-ttu-id="c94ad-113">LogisticsElectronicAddress テーブル内の電子メール アドレス。</span><span class="sxs-lookup"><span data-stu-id="c94ad-113">Email addresses in the LogisticsElectronicAddress table.</span></span>
* <span data-ttu-id="c94ad-114">BatchJobHistory、BatchHistory、および BatchConstraintHistory テーブルのバッチ ジョブ履歴。</span><span class="sxs-lookup"><span data-stu-id="c94ad-114">Batch job history in the BatchJobHistory, BatchHistory, and BatchConstraintHistory tables.</span></span>
* <span data-ttu-id="c94ad-115">SysEmailSMTPPassword テーブルの SMTP パスワード。</span><span class="sxs-lookup"><span data-stu-id="c94ad-115">SMTP password in the SysEmailSMTPPassword table.</span></span>
* <span data-ttu-id="c94ad-116">SysEmailParameters テーブルの SMTP 中継サーバー。</span><span class="sxs-lookup"><span data-stu-id="c94ad-116">SMTP Relay server in the SysEmailParameters table.</span></span>
* <span data-ttu-id="c94ad-117">PrintMgmtSettings と PrintMgmtDocInstance テーブルの印刷管理設定。</span><span class="sxs-lookup"><span data-stu-id="c94ad-117">Print Management settings in the PrintMgmtSettings and PrintMgmtDocInstance tables.</span></span>
* <span data-ttu-id="c94ad-118">SysServerConfig、SysServerSessions、SysCorpNetPrinters、SysClientSessions、BatchServerConfig、および BatchServerGroup テーブル内の環境固有のレコード。</span><span class="sxs-lookup"><span data-stu-id="c94ad-118">Environment-specific records in the SysServerConfig, SysServerSessions, SysCorpNetPrinters, SysClientSessions, BatchServerConfig, and BatchServerGroup tables.</span></span>
* <span data-ttu-id="c94ad-119">DocuValue テーブル内のドキュメント添付ファイル。</span><span class="sxs-lookup"><span data-stu-id="c94ad-119">Document attachments in the DocuValue table.</span></span> <span data-ttu-id="c94ad-120">これには元の環境で無効化されたオフィスのテンプレートが含まれます。</span><span class="sxs-lookup"><span data-stu-id="c94ad-120">This includes any Office Templates that were overriden in the source environment.</span></span>
* <span data-ttu-id="c94ad-121">PersonnellIntegrationConfiguration テーブルの接続文字列</span><span class="sxs-lookup"><span data-stu-id="c94ad-121">Connection string in the PersonnellIntegrationConfiguration table</span></span>
* <span data-ttu-id="c94ad-122">管理者以外のすべてのユーザーは **無効** のステータスに設定されます。</span><span class="sxs-lookup"><span data-stu-id="c94ad-122">All users except the admin will be set to **Disabled** status.</span></span>
* <span data-ttu-id="c94ad-123">すべてのバッチ ジョブは、 **保留** 状態に設定されます。</span><span class="sxs-lookup"><span data-stu-id="c94ad-123">All batch jobs are set to **Withhold** status.</span></span>

### <a name="known-issues"></a><span data-ttu-id="c94ad-124">既知の問題</span><span class="sxs-lookup"><span data-stu-id="c94ad-124">Known issues</span></span>

#### <a name="export-ran-for-some-time-and-then-reached-a-preparation-failed-state"></a><span data-ttu-id="c94ad-125">エクスポートはしばらく実行され、「準備に失敗しました」の状態になります。</span><span class="sxs-lookup"><span data-stu-id="c94ad-125">Export ran for some time and then reached a "Preparation failed" state</span></span>

<span data-ttu-id="c94ad-126">エクスポート プロセスは、大規模なデータベースが関係する Azure SQL データベースではタイムアウトすることがあります。</span><span class="sxs-lookup"><span data-stu-id="c94ad-126">The export process can time out on Azure SQL Database when large databases are involved.</span></span> <span data-ttu-id="c94ad-127">場合によっては、LCS から **再開** アクションを使用してエクスポート プロセスを復元することができます、</span><span class="sxs-lookup"><span data-stu-id="c94ad-127">In some cases, the export process can be recovered by using the **Resume** action from LCS.</span></span> <span data-ttu-id="c94ad-128">Lifecycle Services チームは既知のエラー コードを認識するよう努めており、データベースのエクスポート操作のログにこれらを追加することで、ユーザーが問題を解決できるようにします。</span><span class="sxs-lookup"><span data-stu-id="c94ad-128">The Lifecycle Services team is working to identify known error codes, so these can be added to the logs for the export database operation to help guide users toward a resolution.</span></span> <span data-ttu-id="c94ad-129">LCS の将来のリリースでは、これらの既知のエラー コードが追加されます。</span><span class="sxs-lookup"><span data-stu-id="c94ad-129">These known error codes will be added in a future release of LCS.</span></span> <span data-ttu-id="c94ad-130">問題が発生した場合は、以下の「手動エクスポート」セクションに従って手動でのエクスポートを行うことができます。</span><span class="sxs-lookup"><span data-stu-id="c94ad-130">If you encounter an issue, you can manually export by following the “Manual export” section below.</span></span>

#### <a name="export-doesnt-show-any-progress-in-lcs"></a><span data-ttu-id="c94ad-131">エクスポートで LCS に進捗状況が表示されない</span><span class="sxs-lookup"><span data-stu-id="c94ad-131">Export doesn't show any progress in LCS</span></span>

<span data-ttu-id="c94ad-132">エクスポートのプロセスは、他のデータベース移動の操作および、ランブックを使用しない一般的なパッケージ展開とは異なります。</span><span class="sxs-lookup"><span data-stu-id="c94ad-132">The export process differs from other database movement operations and the general package deployment doesn't use a runbook.</span></span> <span data-ttu-id="c94ad-133">したがって、LCS の進行状況インジケーターには、それ以外のシナリオのような出力が表示されません。</span><span class="sxs-lookup"><span data-stu-id="c94ad-133">Therefore, the progress indicator in LCS doesn't show any output, as it would typically show in other scenarios.</span></span> <span data-ttu-id="c94ad-134">LCSチームは、このようなエラー コードをエクスポート データベース操作のログに追加してユーザーが問題を解決できるようにするべく、既知のエラー コードの識別作業を行っています。</span><span class="sxs-lookup"><span data-stu-id="c94ad-134">The LCS team is working to identify known error codes, so these can be added to the logs for the export database operation to help guide users toward a resolution.</span></span> <span data-ttu-id="c94ad-135">LCS の将来のリリースでは、これらの既知のエラー コードが追加されます。</span><span class="sxs-lookup"><span data-stu-id="c94ad-135">These known error codes will be added in a future release of LCS.</span></span> <span data-ttu-id="c94ad-136">問題が発生した場合は、以下の「手動エクスポート」セクションに従って手動でのエクスポートを行うことができます。</span><span class="sxs-lookup"><span data-stu-id="c94ad-136">If you encounter an issue, you can export manually by following the “Manual export” section below.</span></span>

## <a name="manual-export"></a><span data-ttu-id="c94ad-137">手動エクスポート</span><span class="sxs-lookup"><span data-stu-id="c94ad-137">Manual export</span></span>

<span data-ttu-id="c94ad-138">暗号化された環境固有の値を新しい環境にインポートすることはできません。</span><span class="sxs-lookup"><span data-stu-id="c94ad-138">Encrypted and environment-specific values can't be imported into a new environment.</span></span> <span data-ttu-id="c94ad-139">インポート処理を完了した後は、ターゲット環境内のソース環境から一部のデータを再入力する必要があります。</span><span class="sxs-lookup"><span data-stu-id="c94ad-139">After you've completed the import, you must re-enter some data from your source environment in your target environment.</span></span>

### <a name="document-the-values-of-encrypted-fields"></a><span data-ttu-id="c94ad-140">暗号化されたフィールドの値を文書化</span><span class="sxs-lookup"><span data-stu-id="c94ad-140">Document the values of encrypted fields</span></span>

<span data-ttu-id="c94ad-141">データ暗号化に使用される証明書に関連する技術的な制限のため、データベースの暗号化されたフィールドに格納されている値はそのデータベースが新しい環境にインポートされた後は読み取れません。</span><span class="sxs-lookup"><span data-stu-id="c94ad-141">Because of a technical limitation that is related to the certificate that is used for data encryption, values that are stored in encrypted fields in a database will be unreadable after that database is imported into a new environment.</span></span> <span data-ttu-id="c94ad-142">したがって、インポート後、暗号化されたフィールドに格納されている値を手動で削除して再入力する必要があります。</span><span class="sxs-lookup"><span data-stu-id="c94ad-142">Therefore, after an import, you must manually delete and re-enter values that are stored in encrypted fields.</span></span> <span data-ttu-id="c94ad-143">インポート後に暗号化されたフィールドに入力される新しい値は読み取り可能になります。</span><span class="sxs-lookup"><span data-stu-id="c94ad-143">New values that are entered in encrypted fields after an import will be readable.</span></span> <span data-ttu-id="c94ad-144">次のフィールドが影響されます。</span><span class="sxs-lookup"><span data-stu-id="c94ad-144">The following fields are affected.</span></span> <span data-ttu-id="c94ad-145">フィールド名は Table.Field 形式で指定されます。</span><span class="sxs-lookup"><span data-stu-id="c94ad-145">The field names are given in Table.Field format.</span></span>

| <span data-ttu-id="c94ad-146">フィールド名</span><span class="sxs-lookup"><span data-stu-id="c94ad-146">Field name</span></span>                                               | <span data-ttu-id="c94ad-147">値を設定する場所</span><span class="sxs-lookup"><span data-stu-id="c94ad-147">Where to set the value</span></span> |
|----------------------------------------------------------|------------------------|
| <span data-ttu-id="c94ad-148">CreditCardAccountSetup.SecureMerchantProperties</span><span class="sxs-lookup"><span data-stu-id="c94ad-148">CreditCardAccountSetup.SecureMerchantProperties</span></span>          | <span data-ttu-id="c94ad-149">**売掛金勘定** &gt; **支払設定** &gt; **支払サービス** を選択します。</span><span class="sxs-lookup"><span data-stu-id="c94ad-149">Select **Accounts receivable** &gt; **Payments setup** &gt; **Payment services**.</span></span> |
| <span data-ttu-id="c94ad-150">ExchangeRateProviderConfigurationDetails.Value</span><span class="sxs-lookup"><span data-stu-id="c94ad-150">ExchangeRateProviderConfigurationDetails.Value</span></span>           | <span data-ttu-id="c94ad-151">**総勘定元帳** &gt; **通貨** &gt; **為替レート プロバイダーを構成する** を選択します。</span><span class="sxs-lookup"><span data-stu-id="c94ad-151">Select **General ledger** &gt; **Currencies** &gt; **Configure exchange rate providers**.</span></span> |
| <span data-ttu-id="c94ad-152">FiscalEstablishment\_BR.ConsumerEFDocCsc</span><span class="sxs-lookup"><span data-stu-id="c94ad-152">FiscalEstablishment\_BR.ConsumerEFDocCsc</span></span>                 | <span data-ttu-id="c94ad-153">**組織管理** &gt; **会計機関** &gt; **会計機関** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="c94ad-153">Select **Organization administration** &gt; **Fiscal establishments** &gt; **Fiscal establishments**.</span></span> |
| <span data-ttu-id="c94ad-154">FiscalEstablishmentStaging.CSC</span><span class="sxs-lookup"><span data-stu-id="c94ad-154">FiscalEstablishmentStaging.CSC</span></span>                           | <span data-ttu-id="c94ad-155">このフィールドは、データ インポート/エクスポート フレームワーク (DIXF) によって使用されます。</span><span class="sxs-lookup"><span data-stu-id="c94ad-155">This field is used by the Data Import/Export Framework (DIXF).</span></span> |
| <span data-ttu-id="c94ad-156">HcmPersonIdentificationNumber.PersonIdentificationNumber</span><span class="sxs-lookup"><span data-stu-id="c94ad-156">HcmPersonIdentificationNumber.PersonIdentificationNumber</span></span> | <span data-ttu-id="c94ad-157">**人事管理** &gt; **作業者** &gt; **作業者** の順に選択します。</span><span class="sxs-lookup"><span data-stu-id="c94ad-157">Select **Human resources** &gt; **Workers** &gt; **Workers**.</span></span> <span data-ttu-id="c94ad-158">**ワーカー**タブの、**個人情報**グループで、**ID 番号**を選択します。</span><span class="sxs-lookup"><span data-stu-id="c94ad-158">On the **Worker** tab, in the **Personal information** group, select **Identification numbers**.</span></span> |
| <span data-ttu-id="c94ad-159">HcmWorkerActionHire.PersonIdentificationNumber</span><span class="sxs-lookup"><span data-stu-id="c94ad-159">HcmWorkerActionHire.PersonIdentificationNumber</span></span>           | <span data-ttu-id="c94ad-160">このフィールドは、Microsoft Dynamics AX 7.0 以降 (2016 年 2 月) は廃止されました。</span><span class="sxs-lookup"><span data-stu-id="c94ad-160">This field has been obsolete since Microsoft Dynamics AX 7.0 (February 2016).</span></span> <span data-ttu-id="c94ad-161">これは以前、**すべての作業者アクション** フォーム (**人事管理** &gt; **作業者** &gt; **アクション** &gt; **すべての作業者アクション**) でした。</span><span class="sxs-lookup"><span data-stu-id="c94ad-161">It was previously in the **All worker actions** form (**Human resources** &gt; **Workers** &gt; **Actions** &gt; **All worker actions**).</span></span> |
| <span data-ttu-id="c94ad-162">SysEmailSMTPPassword.Password</span><span class="sxs-lookup"><span data-stu-id="c94ad-162">SysEmailSMTPPassword.Password</span></span>                            | <span data-ttu-id="c94ad-163">**システム管理** &gt; **電子メール** &gt; **電子メール パラメーター** の順に選択します。</span><span class="sxs-lookup"><span data-stu-id="c94ad-163">Select **System administration** &gt; **Email** &gt; **Email parameters**.</span></span> |
| <span data-ttu-id="c94ad-164">SysOAuthUserTokens.EncryptedAccessToken</span><span class="sxs-lookup"><span data-stu-id="c94ad-164">SysOAuthUserTokens.EncryptedAccessToken</span></span>                  | <span data-ttu-id="c94ad-165">このフィールドは、AOS で内部的に使用されます。</span><span class="sxs-lookup"><span data-stu-id="c94ad-165">This field is used internally by AOS.</span></span> <span data-ttu-id="c94ad-166">これは無視できます。</span><span class="sxs-lookup"><span data-stu-id="c94ad-166">It can be ignored.</span></span> |
| <span data-ttu-id="c94ad-167">SysOAuthUserTokens.EncryptedRefreshToken</span><span class="sxs-lookup"><span data-stu-id="c94ad-167">SysOAuthUserTokens.EncryptedRefreshToken</span></span>                 | <span data-ttu-id="c94ad-168">このフィールドは、AOS で内部的に使用されます。</span><span class="sxs-lookup"><span data-stu-id="c94ad-168">This field is used internally by AOS.</span></span> <span data-ttu-id="c94ad-169">これは無視できます。</span><span class="sxs-lookup"><span data-stu-id="c94ad-169">It can be ignored.</span></span> |

### <a name="if-youre-running-retail-components-document-encrypted-and-environment-specific-values"></a><span data-ttu-id="c94ad-170">小売コンポーネントを実行している場合は、暗号化された、環境固有の値を文書化します。</span><span class="sxs-lookup"><span data-stu-id="c94ad-170">If you're running Retail components, document encrypted and environment-specific values</span></span>

<span data-ttu-id="c94ad-171">次のページの値は、環境固有またはデータベースで暗号化されています。</span><span class="sxs-lookup"><span data-stu-id="c94ad-171">The values on the following pages are either environment-specific or encrypted in the database.</span></span> <span data-ttu-id="c94ad-172">したがって、インポートされた値はすべて正しくありません。</span><span class="sxs-lookup"><span data-stu-id="c94ad-172">Therefore, all the imported values will be incorrect.</span></span>

- <span data-ttu-id="c94ad-173">支払サービス (**売掛金勘定** &gt; **支払設定** &gt; **支払サービス**) に移動します。</span><span class="sxs-lookup"><span data-stu-id="c94ad-173">Payments services (**Accounts receivable** &gt; **Payments setup** &gt; **Payments services**)</span></span>
- <span data-ttu-id="c94ad-174">ハードウェア プロファイル (**小売りとコマース** &gt; **チャネル設定** &gt; **POS 設定** &gt; **POS プロファイル** &gt; **ハードウェア プロファイル**)</span><span class="sxs-lookup"><span data-stu-id="c94ad-174">Hardware profiles (**Retail and commerce** &gt; **Channel setup** &gt; **POS setup** &gt; **POS profiles** &gt; **Hardware profiles**)</span></span>

### <a name="create-a-copy-of-the-source-database"></a><span data-ttu-id="c94ad-175">ソース データベースのコピーを作成します。</span><span class="sxs-lookup"><span data-stu-id="c94ad-175">Create a copy of the source database</span></span>

<span data-ttu-id="c94ad-176">ソースの Azure SQL データベースをエクスポートする前に、変更の追跡を無効にし、データベース ユーザーを削除する必要があるため、データベースのコピーを作成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="c94ad-176">Because you must turn off change tracking and delete database users before you can export the source Azure SQL database, you should create a copy of that database.</span></span> <span data-ttu-id="c94ad-177">これによって元のデータベースから情報を削除するかわりに、コピーを使用して作業することができます。</span><span class="sxs-lookup"><span data-stu-id="c94ad-177">You can then work with the copy instead of deleting information from the original database.</span></span> <span data-ttu-id="c94ad-178">以下の SQL ステートメントは、axdb\_mySourceDatabaseToCopy データベースのコピーを **MyNewCopy**という名前で作成します。</span><span class="sxs-lookup"><span data-stu-id="c94ad-178">The following SQL statement creates a copy of the axdb\_mySourceDatabaseToCopy database and names it **MyNewCopy**.</span></span> <span data-ttu-id="c94ad-179">以下のスクリプトを編集して、ご利用のデータベースの名称を使用してください。</span><span class="sxs-lookup"><span data-stu-id="c94ad-179">Edit this script so that it uses the names of your databases.</span></span>

```
CREATE DATABASE MyNewCopy AS COPY OF axdb_mySourceDatabaseToCopy
```

<span data-ttu-id="c94ad-180">このSQL ステートメントは非同期です。</span><span class="sxs-lookup"><span data-stu-id="c94ad-180">This SQL statement runs asynchronously.</span></span> <span data-ttu-id="c94ad-181">つまり、1分ほどで処理が完了したようにみえても、バックグラウンドでは処理が継続しています。</span><span class="sxs-lookup"><span data-stu-id="c94ad-181">In other words, although it appears to be completed after one minute, it actually continues to run in the background.</span></span> <span data-ttu-id="c94ad-182">詳細については、 [データベースの作成 (Azure SQL データベース)](https://msdn.microsoft.com/en-us/library/dn268335.aspx)。</span><span class="sxs-lookup"><span data-stu-id="c94ad-182">For more information, see [CREATE DATABASE (Azure SQL Database)](https://msdn.microsoft.com/en-us/library/dn268335.aspx).</span></span> <span data-ttu-id="c94ad-183">コピーの進行状況を監視するには、同じインタンスのMASTERデータベースに対して以下のクエリを実行してください。</span><span class="sxs-lookup"><span data-stu-id="c94ad-183">To monitor the progress of the copy operation, run the following query against the MASTER database in the same instance.</span></span>

```
SELECT * FROM sys.dm_database_copies
```

> [!WARNING] 
> <span data-ttu-id="c94ad-184">どの Dynamics 365 Finance and Operation アプリ環境でも、長期間にわたってデータベースのコピーを保持することはできません。</span><span class="sxs-lookup"><span data-stu-id="c94ad-184">Retaining copies of the database for an extended period is not allowed in any Dynamics 365 Finance and Operation apps environments.</span></span> <span data-ttu-id="c94ad-185">Microsoft は、事前に通知することなく、7 日を超える古いデータベースのコピーを削除する権限を保有します。</span><span class="sxs-lookup"><span data-stu-id="c94ad-185">Microsoft reserves the right to delete any copies of the database older than 7 days without any prior notice.</span></span>

### <a name="prepare-the-database"></a><span data-ttu-id="c94ad-186">データベースの準備</span><span class="sxs-lookup"><span data-stu-id="c94ad-186">Prepare the database</span></span>

<span data-ttu-id="c94ad-187">以下のスクリプトを実行してデータベースのコピーにて変更の追跡を無効にし、システムビューから SQL Database のユーザーを削除します。</span><span class="sxs-lookup"><span data-stu-id="c94ad-187">Run the following script against the copy of the database to turn off change tracking, and to remove SQL Database users and a system view.</span></span> <span data-ttu-id="c94ad-188">このスクリプトはまた、システムフラグの修正、旧環境に対する参照の削除、バッチ処理の保留、電子メール設定の削除を行います。</span><span class="sxs-lookup"><span data-stu-id="c94ad-188">The script also corrects system flags, removes references to the previous environment, withholds batches, and removes email configuration.</span></span> <span data-ttu-id="c94ad-189">データベースを正常にエクスポート/インポートするには、これらすべての変更が必要となります。</span><span class="sxs-lookup"><span data-stu-id="c94ad-189">All these changes are required for a successful export and import of the database.</span></span> <span data-ttu-id="c94ad-190">これらの変更は、ターゲットとする環境で AOSのコンピューターが開始された際に、自動的に何も開始しないようにすることにも役立ちます。</span><span class="sxs-lookup"><span data-stu-id="c94ad-190">These changes also help to ensure that when the AOS computer is started in the target environment, nothing automatically starts to run.</span></span>

> [!NOTE]
> <span data-ttu-id="c94ad-191">以下の **ALTER DATABASE** コマンドを編集して、データベース コピーの名前を使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="c94ad-191">You must edit the following **ALTER DATABASE** command so that it uses the name of your database copy.</span></span>

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

### <a name="export-the-database"></a><span data-ttu-id="c94ad-192">データベースのエクスポート</span><span class="sxs-lookup"><span data-stu-id="c94ad-192">Export the database</span></span>

<span data-ttu-id="c94ad-193">**コマンド プロンプト** ウィンドウを開き、次のコマンドを実行します。</span><span class="sxs-lookup"><span data-stu-id="c94ad-193">Open a **Command Prompt** window and run the following commands.</span></span>

```
cd C:\Program Files (x86)\Microsoft SQL Server\140\DAC\bin

SqlPackage.exe /a:export /ssn:<server>.database.windows.net /sdn:<database to export> /tf:D:\Exportedbacpac\my.bacpac /p:CommandTimeout=2400 /p:VerifyFullTextDocumentTypesSupported=false /sp:<SQL password> /su:<sql user>
```

<span data-ttu-id="c94ad-194">パラメータの説明を以下に示します。</span><span class="sxs-lookup"><span data-stu-id="c94ad-194">Here is an explanation of the parameters:</span></span>

- <span data-ttu-id="c94ad-195">**ssn (source server name)** – エクスポートを行う元の Azure SQL データベース サーバーの名称</span><span class="sxs-lookup"><span data-stu-id="c94ad-195">**ssn (source server name)** – The name of the Azure SQL Database server to export from.</span></span>
- <span data-ttu-id="c94ad-196">**sdn(ソース データベース名)** – エクスポートするデータベースの名前。</span><span class="sxs-lookup"><span data-stu-id="c94ad-196">**sdn (source database name)** – The name of the database to export.</span></span>
- <span data-ttu-id="c94ad-197">**tf(ターゲット ファイル)** – エクスポートするファイルのパスと名前。</span><span class="sxs-lookup"><span data-stu-id="c94ad-197">**tf (target file)** – The path and name of the file to export to.</span></span>
- <span data-ttu-id="c94ad-198">**sp (source password)** – エクスポートを行う元の SQL Server のSQL パスワード。</span><span class="sxs-lookup"><span data-stu-id="c94ad-198">**sp (source password)** – The SQL password for the source SQL Server.</span></span>
- <span data-ttu-id="c94ad-199">**su (source user)** – エクスポートを行う元の SQL ユーザー名。</span><span class="sxs-lookup"><span data-stu-id="c94ad-199">**su (source user)** – The SQL user name for the source SQL Server.</span></span> <span data-ttu-id="c94ad-200">ユーザーには **sqladmin** を使用することを推奨します。</span><span class="sxs-lookup"><span data-stu-id="c94ad-200">We recommend that you use the **sqladmin** user.</span></span> <span data-ttu-id="c94ad-201">このユーザーは、展開中に Dynamics Finance and Operations アプリのすべての SQL インスタンスで作成されます。</span><span class="sxs-lookup"><span data-stu-id="c94ad-201">This user is created on every Dynamics Finance and Operations apps SQL instance during deployment.</span></span> <span data-ttu-id="c94ad-202">このユーザーのパスワードは、Dynamics Lifecycle Services のプロジェクトから取得できます。</span><span class="sxs-lookup"><span data-stu-id="c94ad-202">You can retrieve the password for this user from your project in Dynamics Lifecycle Services.</span></span>

<span data-ttu-id="c94ad-203">エクスポートの完了後、以下のコマンドを実行してデータベースのコピーを削除します。</span><span class="sxs-lookup"><span data-stu-id="c94ad-203">After the export is completed, run the following command to delete the database copy.</span></span>

```
DROP DATABASE [MyNewCopy]
```
