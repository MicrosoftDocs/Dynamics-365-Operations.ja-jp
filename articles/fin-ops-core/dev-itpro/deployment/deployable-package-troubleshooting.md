---
title: パッケージ アプリケーションの問題のトラブルシューティング
description: トピックでは、1 層または 2 層〜 5 層の環境でパッケージを適用する際に発生する可能性がある問題のトラブルシューティングに役立つ情報を提供します。
author: laneswenka
manager: AnnBe
ms.date: 08/08/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Developer, IT Pro
ms.reviewer: sericks
ms.search.scope: Operations
ms.custom: 107013
ms.assetid: 341a229f-d9c3-4678-b353-d08d5b2c1caf
ms.search.region: Global
ms.author: laswenka
ms.search.validFrom: 2016-05-31
ms.dyn365.ops.version: Platform update 1
ms.openlocfilehash: b57fe3a70916f9fc6051caf3c7fb9e6fce66136d
ms.sourcegitcommit: 567132f4e4f7a1d76dccf762068209a42c788b52
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/03/2020
ms.locfileid: "3096740"
---
# <a name="troubleshoot-package-application-issues"></a><span data-ttu-id="491b1-103">パッケージ アプリケーションの問題のトラブルシューティング</span><span class="sxs-lookup"><span data-stu-id="491b1-103">Troubleshoot package application issues</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="491b1-104">このトピックでは、1 層または 2 層〜 5 層の環境でパッケージを適用する際に発生する可能性がある問題のトラブルシューティングに役立つ詳細情報を提供します。</span><span class="sxs-lookup"><span data-stu-id="491b1-104">This topic provides detailed information that will help you troubleshoot issues that might occur when you apply packages on your Tier 1 or Tier 2 through Tier 5 environments.</span></span> <span data-ttu-id="491b1-105">配置可能パッケージの適用方法についての詳細情報は、 [クラウド環境に更新を適する](apply-deployable-package-system.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="491b1-105">For information about how to apply a package, see [Apply updates to cloud environments](apply-deployable-package-system.md).</span></span>

## <a name="general-troubleshooting-and-diagnostics"></a><span data-ttu-id="491b1-106">一般的なトラブルシューティングと診断</span><span class="sxs-lookup"><span data-stu-id="491b1-106">General troubleshooting and diagnostics</span></span>
<span data-ttu-id="491b1-107">パッケージが正常に適用されていない場合は、2 つのオプションがあります。</span><span class="sxs-lookup"><span data-stu-id="491b1-107">If a package isn't successfully applied, you have two options:</span></span>

- <span data-ttu-id="491b1-108">失敗した操作を再試行します。</span><span class="sxs-lookup"><span data-stu-id="491b1-108">Retry the operation that failed.</span></span>
- <span data-ttu-id="491b1-109">ログを使用します。</span><span class="sxs-lookup"><span data-stu-id="491b1-109">Use the logs.</span></span>

### <a name="retry-the-failed-operation"></a><span data-ttu-id="491b1-110">失敗した操作の再試行</span><span class="sxs-lookup"><span data-stu-id="491b1-110">Retry the failed operation</span></span>
<span data-ttu-id="491b1-111">パッケージ アプリケーションが失敗した場合、操作を再実行する必要があり、**経歴**を選択します。</span><span class="sxs-lookup"><span data-stu-id="491b1-111">If package application fails, and you want to retry the operation, select **Resume**.</span></span>

### <a name="use-the-logs"></a><span data-ttu-id="491b1-112">ログの使用</span><span class="sxs-lookup"><span data-stu-id="491b1-112">Use the logs</span></span>
<span data-ttu-id="491b1-113">パッケージ アプリケーションが失敗すると、ログを使用する場合は、これらの手順に従います。</span><span class="sxs-lookup"><span data-stu-id="491b1-113">If package application fails, and you want to use the logs, follow these steps.</span></span>

1. <span data-ttu-id="491b1-114">ログ ファイルをダウンロードして解凍します。</span><span class="sxs-lookup"><span data-stu-id="491b1-114">Download and then unzip the log files.</span></span>
2. <span data-ttu-id="491b1-115">**AOS** や **BI** など、ステップが失敗したロールを選択します。</span><span class="sxs-lookup"><span data-stu-id="491b1-115">Select the role that a step failed for, such as **AOS** or **BI**.</span></span>
3. <span data-ttu-id="491b1-116">ステップが失敗した場合は仮想マシン (VM) を選択します。</span><span class="sxs-lookup"><span data-stu-id="491b1-116">Select the virtual machine (VM) where the step failed.</span></span> <span data-ttu-id="491b1-117">この情報は **環境の更新** セクションの **コンピューター名** 列で見つけることができます。</span><span class="sxs-lookup"><span data-stu-id="491b1-117">You can find this information in the **Machine name** column in the **Environment updates** section.</span></span>
4. <span data-ttu-id="491b1-118">VM ログで、問題が発生したステップに対応するフォルダーを選択します。</span><span class="sxs-lookup"><span data-stu-id="491b1-118">In the VM logs, select the folder that corresponds to the step where the issue occurred.</span></span> <span data-ttu-id="491b1-119">フォルダー名は、各フォルダーが対応するステップを識別します。</span><span class="sxs-lookup"><span data-stu-id="491b1-119">The folder name identifies the step that each folder corresponds to.</span></span> 

    <span data-ttu-id="491b1-120">たとえば、この手順の過程で問題が発生した場合は、 **ExecuteRunbook** フォルダーを選択します。</span><span class="sxs-lookup"><span data-stu-id="491b1-120">For example, if the issue occurred during the execution of a step, select the **ExecuteRunbook** folder.</span></span> <span data-ttu-id="491b1-121">ステップ番号は、強調表示されたグローバル一意識別子 (GUID) の後の番号です。</span><span class="sxs-lookup"><span data-stu-id="491b1-121">The step number is highlighted and is the number after the globally unique identifier (GUID).</span></span>

## <a name="package-application-issues"></a><span data-ttu-id="491b1-122">パッケージ アプリケーションの問題</span><span class="sxs-lookup"><span data-stu-id="491b1-122">Package application issues</span></span>

### <a name="issue-the-package-that-was-applied-isnt-valid"></a><span data-ttu-id="491b1-123">問題: 適用されたパッケージが有効ではありません</span><span class="sxs-lookup"><span data-stu-id="491b1-123">Issue: The package that was applied isn't valid</span></span>

<span data-ttu-id="491b1-124">**説明**</span><span class="sxs-lookup"><span data-stu-id="491b1-124">**Description**</span></span>

<span data-ttu-id="491b1-125">適用されたパッケージは有効ではないため、サービスの状態は**失敗**になり**環境の更新**セクションには更新が表示されません。</span><span class="sxs-lookup"><span data-stu-id="491b1-125">Because the package that was applied wasn't valid, the servicing status is **Failed**, and no updates are listed in the **Environment updates** section.</span></span> <span data-ttu-id="491b1-126">パッケージが有効かどうかを確認するには、次の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="491b1-126">To verify whether the package is valid, follow these steps.</span></span>

1. <span data-ttu-id="491b1-127">ログをダウンロードして解凍します。</span><span class="sxs-lookup"><span data-stu-id="491b1-127">Download and unzip the logs.</span></span>
2. <span data-ttu-id="491b1-128">Application Object Server (AOS) マシンのログに移動します。</span><span class="sxs-lookup"><span data-stu-id="491b1-128">Navigate to the logs for the Application Object Server (AOS) machine.</span></span>
3. <span data-ttu-id="491b1-129">**DownloadFilesAndSlipstreamTools xxx** および **GenerateRunbook xxx** フォルダーが存在することを確認します。</span><span class="sxs-lookup"><span data-stu-id="491b1-129">Verify that the **DownloadFilesAndSlipstreamTools-xxx** and **GenerateRunbook-xxx** folders exist.</span></span>
4. <span data-ttu-id="491b1-130">**GenerateRunbook-xxx フォルダ**を開いて、出力タイプのファイルを開きます。</span><span class="sxs-lookup"><span data-stu-id="491b1-130">Open the **GenerateRunbook-xxx folder**, and then open the file for the output type.</span></span>

    <span data-ttu-id="491b1-131">ファイルが見つからない、または runbook のステップを生成できなかったことを示すエラー メッセージまたは例外が見つかった場合は、無効なパッケージをアップロードしようとされます。</span><span class="sxs-lookup"><span data-stu-id="491b1-131">If you find an error message or an exception that states that a file is missing or failed to generate any steps for the runbook, there was an attempt to upload a package that wasn't valid.</span></span>

<span data-ttu-id="491b1-132">**操作**</span><span class="sxs-lookup"><span data-stu-id="491b1-132">**Action**</span></span>

<span data-ttu-id="491b1-133">**中止** を選択して現在のパッケージを中止し、新しいパッケージをアップロードしてからサービスのフローを再開します。</span><span class="sxs-lookup"><span data-stu-id="491b1-133">Select **Abort** to abort the current package, upload a new package, and then restart the servicing flow.</span></span>

### <a name="issue-package-deployment-fails-even-though-no-steps-failed"></a><span data-ttu-id="491b1-134">問題: 失敗したステップはありませんが、パッケージの展開に失敗します</span><span class="sxs-lookup"><span data-stu-id="491b1-134">Issue: Package deployment fails even though no steps failed</span></span>

<span data-ttu-id="491b1-135">**説明**</span><span class="sxs-lookup"><span data-stu-id="491b1-135">**Description**</span></span>

<span data-ttu-id="491b1-136">タイムアウトは、パッケージをマシンにダウンロードするときに発生します。</span><span class="sxs-lookup"><span data-stu-id="491b1-136">A time-out occurs when you download the package to the machine.</span></span> <span data-ttu-id="491b1-137">事前のサービス中に、Runbook で手順が完了する前にいくつかの手順を完了する必要があります。</span><span class="sxs-lookup"><span data-stu-id="491b1-137">During pre-servicing, a few steps must be completed before steps are completed in the runbook.</span></span> <span data-ttu-id="491b1-138">事前サービスの一環として、パッケージはすべてのマシンにダウンロードする必要があります。</span><span class="sxs-lookup"><span data-stu-id="491b1-138">As part of the pre-servicing, the package must be downloaded to all the machines.</span></span> <span data-ttu-id="491b1-139">ダウンロードする時間は、環境が存在するデータ センターによって若干異なる場合があります。</span><span class="sxs-lookup"><span data-stu-id="491b1-139">The time to download might vary slightly, depending on the datacenter where the environment resides.</span></span> <span data-ttu-id="491b1-140">30 分以内にダウンロードが実行されない場合は、サービス ステータスがエラーと見なされ停止されます。</span><span class="sxs-lookup"><span data-stu-id="491b1-140">Any download doesn't occur within 30 minutes is considered a failure in the servicing status and will be stopped.</span></span>

<span data-ttu-id="491b1-141">**操作**</span><span class="sxs-lookup"><span data-stu-id="491b1-141">**Action**</span></span>

1. <span data-ttu-id="491b1-142">**再開** を選択し、問題を解決することができるかどうかを確認します。</span><span class="sxs-lookup"><span data-stu-id="491b1-142">Select **Resume** to see whether you can resolve the issue.</span></span> <span data-ttu-id="491b1-143">この手順で動作しない場合は、手順 2 に進みます。</span><span class="sxs-lookup"><span data-stu-id="491b1-143">If this step doesn't work, move on to step 2.</span></span>
2. <span data-ttu-id="491b1-144">ログを**環境**ページからダウンロードします。</span><span class="sxs-lookup"><span data-stu-id="491b1-144">Download the logs from the **Environment** page.</span></span>
3. <span data-ttu-id="491b1-145">すべてのコンピューターへのパッケージのダウンロードに DownloadFilesAndSlipstreamTools フォルダーを含むログが含まれていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="491b1-145">Verify that the package download on all the machines has logs that include the DownloadFilesAndSlipstreamTools folder.</span></span>
4. <span data-ttu-id="491b1-146">ログ ファイルを確認します。</span><span class="sxs-lookup"><span data-stu-id="491b1-146">Review the log files.</span></span> <span data-ttu-id="491b1-147">パッケージのダウンロードが完了しなかったために、ログ ファイルの末尾に、「ファイルのダウンロードとスリップストリームが正常に完了しました」というテキストが表示されない場合、問題が発生しています。</span><span class="sxs-lookup"><span data-stu-id="491b1-147">If you don't see the following text at the end of the log file, the issue occurred because the package download wasn't completed: "Completed file download and slipstream successfully"</span></span>

### <a name="issue-package-deployment-fails-even-though-no-steps-failed"></a><span data-ttu-id="491b1-148">問題: 失敗したステップはありませんが、パッケージの展開に失敗します</span><span class="sxs-lookup"><span data-stu-id="491b1-148">Issue: Package deployment fails even though no steps failed</span></span>

<span data-ttu-id="491b1-149">**説明**</span><span class="sxs-lookup"><span data-stu-id="491b1-149">**Description**</span></span>

<span data-ttu-id="491b1-150">パッケージをダウンロードするのに十分なディスク容量がありません。</span><span class="sxs-lookup"><span data-stu-id="491b1-150">There isn't enough disk space to download the package.</span></span> <span data-ttu-id="491b1-151">すべてのマシンを検査します。</span><span class="sxs-lookup"><span data-stu-id="491b1-151">Inspect all the machines.</span></span> <span data-ttu-id="491b1-152">この問題は、すべてのマシンのサービスのドライブがいっぱいの場合に発生します。</span><span class="sxs-lookup"><span data-stu-id="491b1-152">This issue occurs if the servicing drive of any machines is full.</span></span>

<span data-ttu-id="491b1-153">この状況で**再開**を選択する場合、問題が解決されないことに注意してください。</span><span class="sxs-lookup"><span data-stu-id="491b1-153">Note that if you select **Resume** in this situation, you won't resolve the issue.</span></span>

<span data-ttu-id="491b1-154">スペースの問題により展開が失敗したことを確認するには、次の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="491b1-154">To verify that the deployment failed because space issues, follow these steps.</span></span>

1. <span data-ttu-id="491b1-155">**DownloadFilesAndSlipstreamTools-xxx** フォルダーに移動します。</span><span class="sxs-lookup"><span data-stu-id="491b1-155">Navigate to the **DownloadFilesAndSlipstreamTools-xxx** folder.</span></span>
2. <span data-ttu-id="491b1-156">出力ファイルを開いて、スペースの問題によりステップが失敗したかどうかを確認するエラー メッセージを表示します。</span><span class="sxs-lookup"><span data-stu-id="491b1-156">Open the output file, and view the error message to see whether the step failed because space issues.</span></span>

<span data-ttu-id="491b1-157">**操作**</span><span class="sxs-lookup"><span data-stu-id="491b1-157">**Action**</span></span>

<span data-ttu-id="491b1-158">トポロジの自動クリーンアップの一環として、30 日以上経過した %ServiceVolume%\\DeployablePackages の配置可能なパッケージは削除されます。</span><span class="sxs-lookup"><span data-stu-id="491b1-158">As part of the automated cleanup on topologies, any deployable packages in %ServiceVolume%\\DeployablePackages that are more than 30 days old are deleted.</span></span> <span data-ttu-id="491b1-159">同じタイムラインは、サービス関連のログを削除するためにも使用されます。</span><span class="sxs-lookup"><span data-stu-id="491b1-159">The same timeline is also used to delete servicing-related logs.</span></span> <span data-ttu-id="491b1-160">通常、これらのログは C:\\Dynamics にあります。</span><span class="sxs-lookup"><span data-stu-id="491b1-160">These logs are usually located in C:\\Dynamics.</span></span>

<span data-ttu-id="491b1-161">ただし、dev/one-box マシンには、さらに柔軟性があります。</span><span class="sxs-lookup"><span data-stu-id="491b1-161">However, on dev/one-box machines, there is more flexibility.</span></span> <span data-ttu-id="491b1-162">ServiceVolume およびログ ドライブの保持日数および最小ディスク容量はカスタマイズできます。</span><span class="sxs-lookup"><span data-stu-id="491b1-162">The number of retention days and the minimum disk space of the ServiceVolume and Logs drives can be customized.</span></span>

- <span data-ttu-id="491b1-163">**HKLM:\\ソフトウェア\\Microsoft\\Dynamics\\展開** レジストリ キーで、以下のキーを作成して、クリーンアップを実行するときにカスタマイズできます。</span><span class="sxs-lookup"><span data-stu-id="491b1-163">Under the **HKLM:\\SOFTWARE\\Microsoft\\Dynamics\\Deployment** registry key, you can create the following keys to customize when cleanup should occur.</span></span> <span data-ttu-id="491b1-164">自動クリーンアップ タスクでは、これらの値が考慮されます。</span><span class="sxs-lookup"><span data-stu-id="491b1-164">The automated cleanup task will consider these values.</span></span>

    - <span data-ttu-id="491b1-165">**CutoffDaysForCleanup** - 古いパッケージとログが保持される日数。</span><span class="sxs-lookup"><span data-stu-id="491b1-165">**CutoffDaysForCleanup** – The number of days that old packages and logs should be retained.</span></span> <span data-ttu-id="491b1-166">既定値は **30** です。</span><span class="sxs-lookup"><span data-stu-id="491b1-166">The default value is **30**.</span></span>
    - <span data-ttu-id="491b1-167">**CutoffDiskSpaceLimitForPackages** - パッケージ フォルダーがあるサービス ボリューム ドライブ上 (ギガバイト単位 [GB]) の最小空きディスク容量。</span><span class="sxs-lookup"><span data-stu-id="491b1-167">**CutoffDiskSpaceLimitForPackages** – The minimum free disk space (in gigabytes [GB]) on the service volume drive where the package folder is located.</span></span> <span data-ttu-id="491b1-168">たとえば、ディスク領域が 200 GB の場合、クリーンアップ タスクは日数に基づいてパッケージを削除します。</span><span class="sxs-lookup"><span data-stu-id="491b1-168">For example, if the disk space is 200 GB, the cleanup task will remove the packages, based on the number of days.</span></span>
    - <span data-ttu-id="491b1-169">**CutoffDiskSpaceLimitForLogs** - ログのフォルダーがあるシステム ドライブの最小空きディスク容量 (GB 単位)。</span><span class="sxs-lookup"><span data-stu-id="491b1-169">**CutoffDiskSpaceLimitForLogs** – The minimum free disk space (in GB) of the system drive where the log folder is located.</span></span> <span data-ttu-id="491b1-170">たとえば、ディスク領域が 100 GB の場合、クリーンアップ タスクは日数に基づいてサービス関連のログを削除します。</span><span class="sxs-lookup"><span data-stu-id="491b1-170">For example, if the disk space is 100 GB, the cleanup task will remove the servicing-related logs, based on the number of days.</span></span>

### <a name="issue-a-step-failed-with-errors"></a><span data-ttu-id="491b1-171">問題: ステップがエラーで失敗しました</span><span class="sxs-lookup"><span data-stu-id="491b1-171">Issue: A step failed with errors</span></span>

<span data-ttu-id="491b1-172">**説明**</span><span class="sxs-lookup"><span data-stu-id="491b1-172">**Description**</span></span>

<span data-ttu-id="491b1-173">ステップは、次のいずれかの理由により、エラーで失敗する可能性があります。</span><span class="sxs-lookup"><span data-stu-id="491b1-173">A step might fail with errors for one of the following reasons:</span></span>

- <span data-ttu-id="491b1-174">パッケージにカスタマイズの問題があるか、依存関係がありません。</span><span class="sxs-lookup"><span data-stu-id="491b1-174">The package has customization issues or is missing dependencies.</span></span>
- <span data-ttu-id="491b1-175">サービス スクリプトに問題があります。</span><span class="sxs-lookup"><span data-stu-id="491b1-175">There is an issue with the servicing scripts.</span></span>
- <span data-ttu-id="491b1-176">ステップが実行されたときに、ランダムなエラーが発生しました。</span><span class="sxs-lookup"><span data-stu-id="491b1-176">A random failure occurred when the step was executed.</span></span>

<span data-ttu-id="491b1-177">問題の内容を確認するには、次の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="491b1-177">To verify what the issue is, follow these steps.</span></span>

1. <span data-ttu-id="491b1-178">ステップ・ログをダウンロードしてナビゲートします。</span><span class="sxs-lookup"><span data-stu-id="491b1-178">Download and navigate to the step logs.</span></span>
2. <span data-ttu-id="491b1-179">ステップの出力ファイルを開いて、エラーがないか確認してください。</span><span class="sxs-lookup"><span data-stu-id="491b1-179">Open the output file for the step, and see whether there are any errors.</span></span>
3. <span data-ttu-id="491b1-180">追加のログ ファイルがある場合は、エラーのログ ファイルを検査します。</span><span class="sxs-lookup"><span data-stu-id="491b1-180">If any additional log files are available, inspect them for errors.</span></span>

<span data-ttu-id="491b1-181">**操作**</span><span class="sxs-lookup"><span data-stu-id="491b1-181">**Action**</span></span> 

1. <span data-ttu-id="491b1-182">ログをダウンロードします。</span><span class="sxs-lookup"><span data-stu-id="491b1-182">Download the logs.</span></span>
2. <span data-ttu-id="491b1-183">**ステップの再実行** を選択し、失敗したステップを再試行します。</span><span class="sxs-lookup"><span data-stu-id="491b1-183">Select **Rerun step** to retry the failed step.</span></span>

<span data-ttu-id="491b1-184">ステップが再度失敗し、同じエラーが発生した場合は、ログに戻り、詳細情報を確認します。</span><span class="sxs-lookup"><span data-stu-id="491b1-184">If the step fails again, and the same error occurs, go back to the logs to look for more information.</span></span> 

- <span data-ttu-id="491b1-185">カスタマイズに問題があること場合は、このパッケージを中止し、新しいパッケージを使用して再試行します。</span><span class="sxs-lookup"><span data-stu-id="491b1-185">If you notice that there is an issue with the customizations, abort this package, and retry by using the new package.</span></span>
- <span data-ttu-id="491b1-186">問題の修正プログラムが問題検索にあるかどうかを参照してください。</span><span class="sxs-lookup"><span data-stu-id="491b1-186">See whether a fix for the issue is available in Issue search.</span></span>
- <span data-ttu-id="491b1-187">次の手順の失敗が表示された場合は、データベース同期の問題が発生している可能性、またはレポート展開に失敗した可能性のいずれかです "サービス モデルの GlobalUpdate スクリプト: AOSService"</span><span class="sxs-lookup"><span data-stu-id="491b1-187">If you see the following step failure, either database synchronization or report deployment might have failed: "GlobalUpdate script for service model: AOSService"</span></span>
- <span data-ttu-id="491b1-188">DBSync.err ファイルを検索し、エラー内容を確認します。</span><span class="sxs-lookup"><span data-stu-id="491b1-188">Look for the DBSync.err file, and see what the errors are.</span></span> <span data-ttu-id="491b1-189">DBSync.log ファイルを検査します。</span><span class="sxs-lookup"><span data-stu-id="491b1-189">Inspect the DBSync.log file.</span></span> <span data-ttu-id="491b1-190">DB 同期ステップ中の特定の失敗については、**一般的な DB 同期の失敗**セクションを検索します。</span><span class="sxs-lookup"><span data-stu-id="491b1-190">For specific failures during the DB Sync step, look in the **Common DB Sync Failures** section.</span></span>

### <a name="issue-the-deployment-status-is-servicing-but-the-servicing-status-is-failed"></a><span data-ttu-id="491b1-191">問題: 配置ステータスがサービスとなっていますが、サービス ステータスが失敗しました</span><span class="sxs-lookup"><span data-stu-id="491b1-191">Issue: The deployment status is Servicing but the servicing status is Failed</span></span>

<span data-ttu-id="491b1-192">**説明**</span><span class="sxs-lookup"><span data-stu-id="491b1-192">**Description**</span></span>

<span data-ttu-id="491b1-193">組み込みのメカニズムにより、システムは放棄する前に何度も再試行します。</span><span class="sxs-lookup"><span data-stu-id="491b1-193">A built-in mechanism enables the system to retry multiple times before it gives up.</span></span> <span data-ttu-id="491b1-194">次の準備手順は、複数回再試行することもできます。</span><span class="sxs-lookup"><span data-stu-id="491b1-194">The following preparation steps can also be retried several times:</span></span> 

- <span data-ttu-id="491b1-195">マシンにパッケージをダウンロードします。</span><span class="sxs-lookup"><span data-stu-id="491b1-195">Download the package to the machines.</span></span>
- <span data-ttu-id="491b1-196">サービス パッケージをスリップ ストリームします。</span><span class="sxs-lookup"><span data-stu-id="491b1-196">Slipstream the servicing package.</span></span>
- <span data-ttu-id="491b1-197">Runbook の生成</span><span class="sxs-lookup"><span data-stu-id="491b1-197">Generate the runbook.</span></span>

<span data-ttu-id="491b1-198">**操作**</span><span class="sxs-lookup"><span data-stu-id="491b1-198">**Action**</span></span>

<span data-ttu-id="491b1-199">ログをダウンロードしてエラーを表示し、すべての再試行が終わる前にアクションを取ります。</span><span class="sxs-lookup"><span data-stu-id="491b1-199">You can download the logs to view the error and take action before all retries are exhausted.</span></span> <span data-ttu-id="491b1-200">再試行の仕組みが準備段階を超えない場合、**失敗**のステータスが表示された場合は、チケットを開いて Microsoft チームが問題をさらに調査できるようにします。</span><span class="sxs-lookup"><span data-stu-id="491b1-200">If the retry mechanism fails to go beyond the preparation stage, and you see a status of **Failed**, open a ticket so that the Microsoft team can investigate the issue further.</span></span> 

### <a name="issue-the-dashboard-doesnt-open-after-package-deployment-is-completed"></a><span data-ttu-id="491b1-201">問題: パッケージの展開が完了した後にダッシュボードが開きません</span><span class="sxs-lookup"><span data-stu-id="491b1-201">Issue: The dashboard doesn't open after package deployment is completed</span></span>

<span data-ttu-id="491b1-202">**説明**</span><span class="sxs-lookup"><span data-stu-id="491b1-202">**Description**</span></span>

<span data-ttu-id="491b1-203">パッケージの展開が完了した後にダッシュ ボードが開かない場合は、AOS コンピューターの開始時にランタイム エラーが発生している可能性があります。</span><span class="sxs-lookup"><span data-stu-id="491b1-203">If the dashboard doesn't open after package deployment is completed, a run-time error might be occurring when the AOS machine is started.</span></span>

<span data-ttu-id="491b1-204">**操作**</span><span class="sxs-lookup"><span data-stu-id="491b1-204">**Action**</span></span>

1. <span data-ttu-id="491b1-205">イベント ビューアーを起動します。</span><span class="sxs-lookup"><span data-stu-id="491b1-205">Start Event Viewer.</span></span>
2. <span data-ttu-id="491b1-206">**アプリケーションとサービス ログ** > **Microsoft** > **Dynamics** > **Ax-SystemRuntime** > **エラーで操作フィルター**と移動し、エラーがあるかどうかを確認して、必要に応じてエラーを調査します。</span><span class="sxs-lookup"><span data-stu-id="491b1-206">Navigate to **Applications and Services Logs** > **Microsoft** > **Dynamics** > **Ax-SystemRuntime** > **Operational Filter by errors**, see whether there are any errors, and investigate the errors as required.</span></span>

## <a name="typical-database-synchronization-issues"></a><span data-ttu-id="491b1-207">一般的なデータベース同期の問題</span><span class="sxs-lookup"><span data-stu-id="491b1-207">Typical database synchronization issues</span></span>
<span data-ttu-id="491b1-208">次の手順の失敗が表示された場合は、データベース同期の問題が発生している可能性があります: "サービス モデルの GlobalUpdate スクリプト: AOSService"</span><span class="sxs-lookup"><span data-stu-id="491b1-208">If you see the following step failure, a database synchronization issue might be occurring: "GlobalUpdate script for service model: AOSService"</span></span>

<span data-ttu-id="491b1-209">DBSync.err ファイルを検索し、エラーを検出し、および DBSync.log ファイルを検査するには、これらの手順に従います。</span><span class="sxs-lookup"><span data-stu-id="491b1-209">Follow these steps to look for the DBSync.err file, find the errors, and inspect the DBSync.log file.</span></span>

1. <span data-ttu-id="491b1-210">ステップ・ログをダウンロードしてナビゲートします。</span><span class="sxs-lookup"><span data-stu-id="491b1-210">Download and navigate to the step logs.</span></span>
2. <span data-ttu-id="491b1-211">ステップの出力ファイルを開いて、エラーがないか確認してください。</span><span class="sxs-lookup"><span data-stu-id="491b1-211">Open the output file for the step, and see whether there are any errors.</span></span>
3. <span data-ttu-id="491b1-212">追加のログ ファイルがある場合は、エラーのログを検査します。</span><span class="sxs-lookup"><span data-stu-id="491b1-212">If additional log files are available, inspect the logs for any errors.</span></span>
4. <span data-ttu-id="491b1-213">次のテーブルは、最も頻繁に表示されるエラーと、実行する必要のあるアクションを示しています。</span><span class="sxs-lookup"><span data-stu-id="491b1-213">The following table shows the failures that are seen most often and the action that you should take.</span></span> <span data-ttu-id="491b1-214">**問題** 列には、dbsync.err ファイルに表示されるエラー メッセージが表示されます。</span><span class="sxs-lookup"><span data-stu-id="491b1-214">The **Issue** column shows the error message that you will see in the dbsync.err file.</span></span> <span data-ttu-id="491b1-215">パーセント記号 (%) は、テーブル、フィールド、インデックスなどのメタデータの名前に置き換えできます。</span><span class="sxs-lookup"><span data-stu-id="491b1-215">The percentage sign (%) can be replaced with the metadata name of the table, field, index, and so on.</span></span>

    | <span data-ttu-id="491b1-216">問題</span><span class="sxs-lookup"><span data-stu-id="491b1-216">Issue</span></span> | <span data-ttu-id="491b1-217">アクション</span><span class="sxs-lookup"><span data-stu-id="491b1-217">Action</span></span> |
    |-------|--------|
    | <span data-ttu-id="491b1-218">% テーブルでテーブル同期に失敗しました % 一意のインデックスを作成します %</span><span class="sxs-lookup"><span data-stu-id="491b1-218">%Table Sync Failed for Table%Create Unique Index%</span></span> | <span data-ttu-id="491b1-219">この問題は通常、ユニークなインデックスが作成されたが、データが一意でない場合に発生します。</span><span class="sxs-lookup"><span data-stu-id="491b1-219">This issue typically occurs when a unique index is created, but the data isn't unique.</span></span> <span data-ttu-id="491b1-220">手順をもう一度実行する前に、データを修正します。</span><span class="sxs-lookup"><span data-stu-id="491b1-220">Fix the data before you run the step again.</span></span> |
    | <span data-ttu-id="491b1-221">% アプリケーション構成の同期に失敗しました。% カスタム アクションの同期がエラーにより失敗しました。%</span><span class="sxs-lookup"><span data-stu-id="491b1-221">%Application configuration sync failed.%Custom action sync failed with error:%</span></span> | <span data-ttu-id="491b1-222">エラー メッセージと呼び出しスタック内の情報を表示して、問題の原因となるアプリケーション コードを決定します。</span><span class="sxs-lookup"><span data-stu-id="491b1-222">View the information in the error message and the call stack to determine the application code that is causing the issue.</span></span> |
    | <span data-ttu-id="491b1-223">% 基になるクエリ&#39;&#39;のテーブルには見つかりません %</span><span class="sxs-lookup"><span data-stu-id="491b1-223">%cannot be found from underlying query&#39;&#39;s table%</span></span> | <span data-ttu-id="491b1-224">この問題は修正されました。</span><span class="sxs-lookup"><span data-stu-id="491b1-224">This issue was fixed.</span></span> <span data-ttu-id="491b1-225">詳細については、KB 4018815 を参照してください。</span><span class="sxs-lookup"><span data-stu-id="491b1-225">For more information, refer to KB 4018815.</span></span> |
    | <span data-ttu-id="491b1-226">% テーブルでテーブル同期が失敗しました % 変換フィールド %</span><span class="sxs-lookup"><span data-stu-id="491b1-226">%Table Sync Failed for Table%Converting Field%</span></span> | <span data-ttu-id="491b1-227">エラー メッセージに従って、問題を修正し、ステップを再度実行します。</span><span class="sxs-lookup"><span data-stu-id="491b1-227">Follow the error message, fix the issue, and run the step again.</span></span> |
    | <span data-ttu-id="491b1-228">% 1 つ以上のオブジェクトがこの列にアクセスしているため失敗しました %</span><span class="sxs-lookup"><span data-stu-id="491b1-228">%failed because one or more objects access this column%</span></span> | <span data-ttu-id="491b1-229">インデックスがメタデータにあるかどうかを確認します。</span><span class="sxs-lookup"><span data-stu-id="491b1-229">See whether the index is in the metadata.</span></span> <span data-ttu-id="491b1-230">インデックスがメタデータ内にある場合は、この問題は SyncEngine 製品問題です。</span><span class="sxs-lookup"><span data-stu-id="491b1-230">If the index is in the metadata, this issue is a SyncEngine product issue.</span></span> <span data-ttu-id="491b1-231">インデックスがメタデータにない場合、ステップを再度実行する前に、SQL データベースからインデックスを削除します。</span><span class="sxs-lookup"><span data-stu-id="491b1-231">If the index isn't in the metadata, remove the index from the SQL database before you run the step again.</span></span> |
    | <span data-ttu-id="491b1-232">% 基になるデータ ソース&#39;&#39;テーブルから見つかりません %</span><span class="sxs-lookup"><span data-stu-id="491b1-232">%cannot be found from underlying data source&#39;&#39;s table%</span></span> | <span data-ttu-id="491b1-233">この問題は修正されました。</span><span class="sxs-lookup"><span data-stu-id="491b1-233">This issue was fixed.</span></span> <span data-ttu-id="491b1-234">詳細については、KB 4018815 を参照してください。</span><span class="sxs-lookup"><span data-stu-id="491b1-234">For more information, refer to KB 4018815.</span></span> |
    | <span data-ttu-id="491b1-235">「% テーブルの % テーブルへの同期が失敗しました」、そして、「% という名前のオブジェクトは既に存在しています %」のような errorMessage が表示されます</span><span class="sxs-lookup"><span data-stu-id="491b1-235">&#39;%Table Sync Failed for Table%&#39; and errorMessage like &#39;%There is already an object named%&#39;</span></span> | <span data-ttu-id="491b1-236">内部 SqlDictionary テーブルおよび SQL スキーマが同期されていません。この状態に到達する方法を理解するのに十分な情報がログにありません。</span><span class="sxs-lookup"><span data-stu-id="491b1-236">The Internal SqlDictionary table and SQL schema are out of sync. There isn't enough information in the logs to understand how this state was reached.</span></span> |
    | <span data-ttu-id="491b1-237">% テーブルでテーブル同期が失敗しました % 各テーブルの列名は一意である必要があります %</span><span class="sxs-lookup"><span data-stu-id="491b1-237">%Table Sync Failed for Table%Column names in each table must be unique%</span></span> | <span data-ttu-id="491b1-238">テーブルの SqlDictionary エントリが破損しており、フィールドがありません。</span><span class="sxs-lookup"><span data-stu-id="491b1-238">SqlDictionary entries for the table are corrupted, and the field is missing.</span></span> <span data-ttu-id="491b1-239">この状態にどのように達したかを理解するには、ログに十分な情報がありません。</span><span class="sxs-lookup"><span data-stu-id="491b1-239">There isn't enough information in the logs to understand how this state was reached.</span></span> |
    | <span data-ttu-id="491b1-240">% 列の名前「LOAD\_」は、ターゲット テーブルまたはビューに存在しません。</span><span class="sxs-lookup"><span data-stu-id="491b1-240">%Column name &#39;LOAD\_&#39; does not exist in the target table or view.</span></span> <span data-ttu-id="491b1-241">インデックスの作成%</span><span class="sxs-lookup"><span data-stu-id="491b1-241">CREATE INDEX%</span></span> | <span data-ttu-id="491b1-242">この問題は、SyncEngine の問題のようです。</span><span class="sxs-lookup"><span data-stu-id="491b1-242">This issue appears to be a SyncEngine issue.</span></span> <span data-ttu-id="491b1-243">Microsoft サポートにチケットを作成します。</span><span class="sxs-lookup"><span data-stu-id="491b1-243">Create a ticket on Microsoft Support.</span></span> |
    | <span data-ttu-id="491b1-244">「VENDREQUESTPROFILEQUESTIONNAIRE.I\_1301PROFILEQUESTIONNAIRE」インデックスは存在しないか、アクセス許可がないため削除することはできません。</span><span class="sxs-lookup"><span data-stu-id="491b1-244">Cannot drop the index &#39;VENDREQUESTPROFILEQUESTIONNAIRE.I\_1301PROFILEQUESTIONNAIRE&#39;, because it does not exist or you do not have permission</span></span> | <span data-ttu-id="491b1-245">この問題は、SyncEngine の問題のようです。</span><span class="sxs-lookup"><span data-stu-id="491b1-245">This issue appears to be a SyncEngine issue.</span></span> <span data-ttu-id="491b1-246">Microsoft サポートにチケットを作成します。</span><span class="sxs-lookup"><span data-stu-id="491b1-246">Create a ticket on Microsoft Support.</span></span> |
    | <span data-ttu-id="491b1-247">% インデックス「I\_65750INDEX1」の長さ 2046 バイトのインデックス エントリは、非クラスター化インデックスの最大長 1700 バイトを超えています %</span><span class="sxs-lookup"><span data-stu-id="491b1-247">%The index entry of length 2046 bytes for the index &#39;I\_65750INDEX1&#39; exceeds the maximum length of 1700 bytes for nonclustered indexes%</span></span> | <span data-ttu-id="491b1-248">手順をもう一度実行する前に、インデックスを変更します。</span><span class="sxs-lookup"><span data-stu-id="491b1-248">Modify the index before you run the step again.</span></span> |
    | <span data-ttu-id="491b1-249">% 付近に正しくない構文があります %</span><span class="sxs-lookup"><span data-stu-id="491b1-249">%Incorrect syntax near%</span></span> | <span data-ttu-id="491b1-250">この問題は、SyncEngine の問題です。</span><span class="sxs-lookup"><span data-stu-id="491b1-250">This issue is a SyncEngine issue.</span></span> <span data-ttu-id="491b1-251">Microsoft サポートにチケットを作成します。</span><span class="sxs-lookup"><span data-stu-id="491b1-251">Create a ticket on Microsoft Support.</span></span> |
    | <span data-ttu-id="491b1-252">「TEMPDB.DBO.T\_TRVREQUISITIONLINE\_C4C3569DD5A14CDABAE71A341743FB61」におけるデータベースまたはサーバーの名前の参照は、このバージョンの SQL Server ではサポートされていません</span><span class="sxs-lookup"><span data-stu-id="491b1-252">Reference to database and/or server name in &#39;TEMPDB.DBO.T\_TRVREQUISITIONLINE\_C4C3569DD5A14CDABAE71A341743FB61&#39; is not supported in this version of SQL Server</span></span> | <span data-ttu-id="491b1-253">この問題は、SyncEngine の問題です。</span><span class="sxs-lookup"><span data-stu-id="491b1-253">This issue is a SyncEngine issue.</span></span> <span data-ttu-id="491b1-254">Microsoft サポートにチケットを作成します。</span><span class="sxs-lookup"><span data-stu-id="491b1-254">Create a ticket on Microsoft Support.</span></span> |
    | <span data-ttu-id="491b1-255">% エラー: タイムアウトが発生しました。</span><span class="sxs-lookup"><span data-stu-id="491b1-255">%Error: Timeout expired.</span></span>  <span data-ttu-id="491b1-256">pool.% から接続を取得するまでに経過したタイムアウト時間。</span><span class="sxs-lookup"><span data-stu-id="491b1-256">The timeout period elapsed prior to obtaining a connection from the pool.%</span></span> | <span data-ttu-id="491b1-257">ステップを再試行します。</span><span class="sxs-lookup"><span data-stu-id="491b1-257">Retry the step.</span></span> |
    | <span data-ttu-id="491b1-258">データベースの実行に失敗しました: 無効な列名「DEFAULTDIMENSION」。</span><span class="sxs-lookup"><span data-stu-id="491b1-258">Database execution failed: Invalid column name &#39;DEFAULTDIMENSION&#39;.</span></span> <span data-ttu-id="491b1-259">VIEW の作成</span><span class="sxs-lookup"><span data-stu-id="491b1-259">CREATE VIEW</span></span> | <span data-ttu-id="491b1-260">この問題は、SyncEngine の問題のようです。</span><span class="sxs-lookup"><span data-stu-id="491b1-260">This issue appears to be a SyncEngine issue.</span></span> <span data-ttu-id="491b1-261">Microsoft サポートにチケットを作成します。</span><span class="sxs-lookup"><span data-stu-id="491b1-261">Create a ticket on Microsoft Support.</span></span> |
    | <span data-ttu-id="491b1-262">データベースの実行に失敗しました: 無効なオブジェクトの名前「PMBI\_DEPROJECTTIMESHEET」。</span><span class="sxs-lookup"><span data-stu-id="491b1-262">Database execution failed: Invalid object name &#39;PMBI\_DEPROJECTTIMESHEET&#39;.</span></span> <span data-ttu-id="491b1-263">VIEW の作成</span><span class="sxs-lookup"><span data-stu-id="491b1-263">CREATE VIEW</span></span> | <span data-ttu-id="491b1-264">この問題は、SyncEngine の問題のようです。</span><span class="sxs-lookup"><span data-stu-id="491b1-264">This issue appears to be a SyncEngine issue.</span></span> <span data-ttu-id="491b1-265">Microsoft サポートにチケットを作成します。</span><span class="sxs-lookup"><span data-stu-id="491b1-265">Create a ticket on Microsoft Support.</span></span> |
    | <span data-ttu-id="491b1-266">% プロバイダー: 名前付きパイプ プロバイダー、エラー: 40: - SQL Server への接続を開けませんでした %</span><span class="sxs-lookup"><span data-stu-id="491b1-266">%provider: Named Pipes Provider, error: 40 - Could not open a connection to SQL Server%</span></span>  | <span data-ttu-id="491b1-267">Platform Update 3 でこの問題を修正されている必要があります。</span><span class="sxs-lookup"><span data-stu-id="491b1-267">This issue should have been fixed in Platform Update 3.</span></span> <span data-ttu-id="491b1-268">ステップを再試行します。</span><span class="sxs-lookup"><span data-stu-id="491b1-268">Retry the step.</span></span> |
