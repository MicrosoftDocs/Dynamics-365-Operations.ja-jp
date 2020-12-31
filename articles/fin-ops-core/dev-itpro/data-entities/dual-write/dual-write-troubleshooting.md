---
title: 一般的なトラブルシューティング
description: このトピックでは、Finance and Operations アプリと Dataverse 間のデュアル書き込み統合に関する一般的なトラブルシューティングの情報を提供します。
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 03/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-03-16
ms.openlocfilehash: 6356ec6850667f32f9e9e4133686c40f0b6d76d7
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 12/05/2020
ms.locfileid: "4688262"
---
# <a name="general-troubleshooting"></a><span data-ttu-id="44ca6-103">一般的なトラブルシューティング</span><span class="sxs-lookup"><span data-stu-id="44ca6-103">General troubleshooting</span></span>

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]



<span data-ttu-id="44ca6-104">このトピックでは、Finance and Operations アプリと Dataverse 間のデュアル書き込み統合に関する一般的なトラブルシューティングの情報を提供します。</span><span class="sxs-lookup"><span data-stu-id="44ca6-104">This topic provides general troubleshooting information for dual-write integration between Finance and Operations apps and Dataverse.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="44ca6-105">このトピックで説明されている問題の中には、システム管理者ロールまたは Microsoft Azure Active Directory（Azure AD）テナント管理者の資格情報のいずれかが必要な場合があります。</span><span class="sxs-lookup"><span data-stu-id="44ca6-105">Some of the issues that this topic addresses might require either the system admin role or Microsoft Azure Active Directory (Azure AD) tenant admin credentials.</span></span> <span data-ttu-id="44ca6-106">各問題のセクションでは、特定のロールまたは資格情報が必要な場合について説明しています。</span><span class="sxs-lookup"><span data-stu-id="44ca6-106">The section for each issue explains whether a specific role or credentials are required.</span></span>

## <a name="when-you-try-to-install-the-dual-write-package-by-using-the-package-deployer-tool-no-available-solutions-are-shown"></a><span data-ttu-id="44ca6-107">Package Deployer ツールを使用してデュアル書書き込み込みパッケージをインストールしようとすると、使用可能なソリューションが表示されない</span><span class="sxs-lookup"><span data-stu-id="44ca6-107">When you try to install the dual-write package by using the package deployer tool, no available solutions are shown</span></span>

<span data-ttu-id="44ca6-108">Package Deployer ツールの一部のバージョンは、デュアル書き込みソリューション パッケージと互換性がありません。</span><span class="sxs-lookup"><span data-stu-id="44ca6-108">Some versions of the package deployer tool are incompatible with the dual-write solution package.</span></span> <span data-ttu-id="44ca6-109">パッケージを正常にインストールするには、Package Deployer ツールの [バージョン 9.1.0.20](https://www.nuget.org/packages/Microsoft.CrmSdk.XrmTooling.PackageDeployment.Wpf/9.1.0.20) またはそれ以降を使用してください。</span><span class="sxs-lookup"><span data-stu-id="44ca6-109">To successfully install the package, be sure to use [version 9.1.0.20](https://www.nuget.org/packages/Microsoft.CrmSdk.XrmTooling.PackageDeployment.Wpf/9.1.0.20) or later of the package deployer tool.</span></span>

<span data-ttu-id="44ca6-110">Package Deployer ツールをインストールした後、次の手順に従ってソリューション パッケージをインストールしてください。</span><span class="sxs-lookup"><span data-stu-id="44ca6-110">After you install the package deployer tool, install the solution package by following these steps.</span></span>

1. <span data-ttu-id="44ca6-111">Yammer.com から最新のソリューション パッケージ ファイルをダウンロードします。</span><span class="sxs-lookup"><span data-stu-id="44ca6-111">Download the latest solution package file from Yammer.com.</span></span> <span data-ttu-id="44ca6-112">パッケージのZIP ファイルをダウンロードした後、ファイルを右クリックして **プロパティ** を選択します。</span><span class="sxs-lookup"><span data-stu-id="44ca6-112">After the package zip file is downloaded, right-click it, and select **Properties**.</span></span> <span data-ttu-id="44ca6-113">**ブロックの解除** チェック ボックスを選択し、**適用** を選択します。</span><span class="sxs-lookup"><span data-stu-id="44ca6-113">Select the **Unblock** check box, and then select **Apply**.</span></span> <span data-ttu-id="44ca6-114">**ブロックの解除** チェックボックスが表示されない場合は、zip ファイルのブロック解除が既にされているため、この手順を省略できます。</span><span class="sxs-lookup"><span data-stu-id="44ca6-114">If you don't see the **Unblock** check box, the zip file is already unblocked, and you can skip this step.</span></span>

    ![プロパティ ダイアログ ボックス](media/unblock_option.png)

2. <span data-ttu-id="44ca6-116">パッケージの zip ファイルを展開し、**Dynamics365FinanceAndOperationsCommon** フォルダのすべてのファイルをコピーします。</span><span class="sxs-lookup"><span data-stu-id="44ca6-116">Extract the package zip file, and copy all the files in the **Dynamics365FinanceAndOperationsCommon.PackageDeployer.2.0.438** folder.</span></span>

    ![Dynamics365FinanceAndOperationsCommon.PackageDeployer.2.0.438 フォルダの内容](media/extract_package.png)

3. <span data-ttu-id="44ca6-118">コピーされたすべてのファイルを Package Deployer ツールの **Tools** フォルダーに貼り付けます。</span><span class="sxs-lookup"><span data-stu-id="44ca6-118">Paste all the copied files into the **Tools** folder of the package deployer tool.</span></span> 
4. <span data-ttu-id="44ca6-119">**PackageDeployer.exe** を実行して Dataverse の環境を選択し、ソリューションをインストールします。</span><span class="sxs-lookup"><span data-stu-id="44ca6-119">Run **PackageDeployer.exe** to select the Dataverse environment and install the solutions.</span></span>

    ![ツール フォルダのコンテンツ](media/paste_copied_files.png)

## <a name="enable-and-view-the-plug-in-trace-log-in-dataverse-to-view-error-details"></a><a id="enable-view-trace"></a><span data-ttu-id="44ca6-121">Dataverse のプラグイン トレース ログを有効にして確認し、エラーの詳細を表示します</span><span class="sxs-lookup"><span data-stu-id="44ca6-121">Enable and view the plug-in trace log in Dataverse to view error details</span></span>

<span data-ttu-id="44ca6-122">**トレース ログを有効にするために必要な役割とエラーの表示:** システム管理者</span><span class="sxs-lookup"><span data-stu-id="44ca6-122">**Required role to turn on the trace log and view errors:** System admin</span></span>

<span data-ttu-id="44ca6-123">トレース ログを有効にするには、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="44ca6-123">To turn on the trace log, follow these steps.</span></span>

1. <span data-ttu-id="44ca6-124">Dynamics 365 のモデル駆動型アプリにサインインし、**システム** 配下の **設定** ページを開き、 **管理** を選択します。</span><span class="sxs-lookup"><span data-stu-id="44ca6-124">Sign in to the model-driven app in Dynamics 365, open the **Settings** page, and then, under **System**, select **Administration**.</span></span>
2. <span data-ttu-id="44ca6-125">**管理者** ページで、**システム管理** を選択します。</span><span class="sxs-lookup"><span data-stu-id="44ca6-125">On the **Administration** page, select **System Settings**.</span></span>
3. <span data-ttu-id="44ca6-126">**カスタマイズ** タブの **プラグインおよびユーザー定義ワークフロー活動の追跡** フィールドで、**すべて** を選択してプラグインのトレース ログを有効にします。</span><span class="sxs-lookup"><span data-stu-id="44ca6-126">On the **Customization** tab, in the **Plug-in and custom workflow activity tracing** field, select **All** to enable the plug-in trace log.</span></span> <span data-ttu-id="44ca6-127">例外が発生したときにのみトレースログを記録する場合は **例外** を選択します。</span><span class="sxs-lookup"><span data-stu-id="44ca6-127">If you want to log trace logs only when exceptions occur, you can select **Exception** instead.</span></span>


<span data-ttu-id="44ca6-128">トレースログを確認にするには、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="44ca6-128">To view the trace log, follow these steps.</span></span>

1. <span data-ttu-id="44ca6-129">Dynamics 365 のモデル駆動型アプリにサインインし、**カスタマイズ** 配下の **設定** ページを開き、 **プラグイン トレース ログ** を選択します。</span><span class="sxs-lookup"><span data-stu-id="44ca6-129">Sign in to the model-driven app in Dynamics 365, open the **Settings** page, and then, under **Customization**, select **Plug-in Trace Log**.</span></span>
2. <span data-ttu-id="44ca6-130">**タイプ名** フィールドが **Microsoft.Dynamics.Integrator.DualWriteRuntime.Plugins.PreCommmitPlugin** に設定されているトレース ログを検索します。</span><span class="sxs-lookup"><span data-stu-id="44ca6-130">Find the trace logs where the **Type Name** field is set to **Microsoft.Dynamics.Integrator.DualWriteRuntime.Plugins.PreCommmitPlugin**.</span></span>
3. <span data-ttu-id="44ca6-131">完全なログを表示するには、項目をダブルクリックし、**実行** ファストタブで **メッセージ ブロック** のテキストを確認します。</span><span class="sxs-lookup"><span data-stu-id="44ca6-131">Double-click an item to view the full log, and then, on the **Execution** FastTab, review the **Message Block** text.</span></span>

## <a name="enable-debug-mode-to-troubleshoot-live-synchronization-issues-in-finance-and-operations-apps"></a><span data-ttu-id="44ca6-132">デバッグ モードを有効にして、アプリ Finance and Operations でのライブ同期に関する問題のトラブルシューティングを行います。</span><span class="sxs-lookup"><span data-stu-id="44ca6-132">Enable debug mode to troubleshoot live synchronization issues in Finance and Operations apps</span></span>

<span data-ttu-id="44ca6-133">**エラーを表示するために必要な役割：** Dataverse で発生したシステム管理のデュアル書き込みエラーは、Finance and Operations アプリに表示される場合があります。</span><span class="sxs-lookup"><span data-stu-id="44ca6-133">**Required role to view the errors:** System admin Dual-write errors that originate in Dataverse can appear in the Finance and Operations app.</span></span> <span data-ttu-id="44ca6-134">エラーメッセージの完全なテキストが表示されない場合がありますが、これはメッセージが長すぎるか個人の識別情報 (PII) が含まれていることが原因です。</span><span class="sxs-lookup"><span data-stu-id="44ca6-134">In some cases, the full text of the error message isn't available because the message is too long or contains personally identifying information (PII).</span></span> <span data-ttu-id="44ca6-135">エラーの詳細ログを有効にするには、次の手順を実行してください。</span><span class="sxs-lookup"><span data-stu-id="44ca6-135">You can turn on verbose logging for errors by following these steps.</span></span>

1. <span data-ttu-id="44ca6-136">Finance and Operations アプリにおけるすべてのプロジェクトの構成は、**DualWriteProjectConfiguration** エンティティ内に **IsDebugMode** プロパティが存在します。</span><span class="sxs-lookup"><span data-stu-id="44ca6-136">All project configurations in Finance and Operations apps have an **IsDebugMode** property in the **DualWriteProjectConfiguration** entity.</span></span> <span data-ttu-id="44ca6-137">Excel アドインを使用して **DualWriteProjectConfiguration** エンティティを開きます。</span><span class="sxs-lookup"><span data-stu-id="44ca6-137">Open the **DualWriteProjectConfiguration** entity by using the Excel add-in.</span></span>

    > [!TIP]
    > <span data-ttu-id="44ca6-138">エンティティを簡単に開くには、Excelアドインで **デザイン** モードを有効にしてから、ワークシートに **DualWriteProjectConfigurationEntity** を追加してください。</span><span class="sxs-lookup"><span data-stu-id="44ca6-138">An easy way to open the entity is to turn on **Design** mode in the Excel add-in and then add **DualWriteProjectConfigurationEntity** to the worksheet.</span></span> <span data-ttu-id="44ca6-139">詳細については、[Excel でエンティティ データを開き、Excel アドインを使用して更新する](../../office-integration/use-excel-add-in.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="44ca6-139">For more information, see [Open entity data in Excel and update it by using the Excel add-in](../../office-integration/use-excel-add-in.md).</span></span>

2. <span data-ttu-id="44ca6-140">プロジェクトの **IsDebugMode** プロパティを **はい** に設定します。</span><span class="sxs-lookup"><span data-stu-id="44ca6-140">Set the **IsDebugMode** property to **Yes** for the project.</span></span>
3. <span data-ttu-id="44ca6-141">エラーが発生するシナリオを実行します。</span><span class="sxs-lookup"><span data-stu-id="44ca6-141">Run the scenario that is generating errors.</span></span>
4. <span data-ttu-id="44ca6-142">詳細なログは、DualWriteErrorLog テーブルで確認できます。</span><span class="sxs-lookup"><span data-stu-id="44ca6-142">The verbose logs are available in the DualWriteErrorLog table.</span></span> <span data-ttu-id="44ca6-143">テーブル ブラウザーでデータを参照するには、次のURLを使用してください（必要に応じて **XXX** を置き換えてください）：</span><span class="sxs-lookup"><span data-stu-id="44ca6-143">To look up data in the table browser, use the following URL (replace **XXX** as appropriate):</span></span>

    `https://XXXaos.cloudax.dynamics.com/?mi=SysTableBrowser&tableName=DualWriteErrorLog`

## <a name="check-synchronization-errors-on-the-virtual-machine-for-the-finance-and-operations-app"></a><span data-ttu-id="44ca6-144">Finance and Operations アプリの仮想マシンの同期エラーを確認する</span><span class="sxs-lookup"><span data-stu-id="44ca6-144">Check synchronization errors on the virtual machine for the Finance and Operations app</span></span>

<span data-ttu-id="44ca6-145">**エラーを表示するために必要な役割：** システム管理者</span><span class="sxs-lookup"><span data-stu-id="44ca6-145">**Required role to view the errors:** System administrator</span></span>

1. <span data-ttu-id="44ca6-146">Microsoft Dynamics Lifecycle Services (LCS) にログインします。</span><span class="sxs-lookup"><span data-stu-id="44ca6-146">Sign in to Microsoft Dynamics Lifecycle Services (LCS).</span></span>
2. <span data-ttu-id="44ca6-147">デュアル書き込みテストを実行する、LCS プロジェクトを開きます。</span><span class="sxs-lookup"><span data-stu-id="44ca6-147">Open the LCS project that you chose to do the dual-write testing for.</span></span>
3. <span data-ttu-id="44ca6-148">**クラウド ホスト環境** のタイトルを選択します。</span><span class="sxs-lookup"><span data-stu-id="44ca6-148">Select the **Cloud-hosted environments** tile.</span></span>
4. <span data-ttu-id="44ca6-149">リモート デスクトップを使用して、Finance and Operations アプリの仮想マシン (VM) にログインします。</span><span class="sxs-lookup"><span data-stu-id="44ca6-149">Use Remote Desktop to sign in to the virtual machine (VM) for the Finance and Operations app.</span></span> <span data-ttu-id="44ca6-150">LCS に表示されるローカル アカウントを使用します。</span><span class="sxs-lookup"><span data-stu-id="44ca6-150">Use the local account that is shown in LCS.</span></span>
5. <span data-ttu-id="44ca6-151">イベント ビューアーを開きます。</span><span class="sxs-lookup"><span data-stu-id="44ca6-151">Open Event viewer.</span></span>
6. <span data-ttu-id="44ca6-152">**アプリケーションとサービス ログ \> Microsoft \> Dynamics \> AX-DualWriteSync \> オペレーション** を選択します。</span><span class="sxs-lookup"><span data-stu-id="44ca6-152">Select **Applications and Services Logs \> Microsoft \> Dynamics \> AX-DualWriteSync \> Operational**.</span></span>
7. <span data-ttu-id="44ca6-153">最近発生したエラーの一覧を確認します。</span><span class="sxs-lookup"><span data-stu-id="44ca6-153">Review the list of recent errors.</span></span>

## <a name="unlink-and-link-another-dataverse-environment-from-a-finance-and-operations-app"></a><span data-ttu-id="44ca6-154">Finance and Operations アプリの Dataverse 環境のリンクを解除し、他の環境をリンクする</span><span class="sxs-lookup"><span data-stu-id="44ca6-154">Unlink and link another Dataverse environment from a Finance and Operations app</span></span>

<span data-ttu-id="44ca6-155">**環境のリンクの解除に必要な役割：** Finance and Operations アプリ、または Dataverse のいずれかのシステム管理者。</span><span class="sxs-lookup"><span data-stu-id="44ca6-155">**Required role to unlink the environment:** System administrator for either Finance and Operations app or Dataverse.</span></span>

1. <span data-ttu-id="44ca6-156">Finance and Operations アプリにサインインします。</span><span class="sxs-lookup"><span data-stu-id="44ca6-156">Sign in to the Finance and Operations app.</span></span>
2. <span data-ttu-id="44ca6-157">**ワークスペース \> データ管理** に移動して、**デュアル書き込み** のタイルを選択します。</span><span class="sxs-lookup"><span data-stu-id="44ca6-157">Go to **Workspaces \> Data management**, and select the **Dual Write** tile.</span></span>
3. <span data-ttu-id="44ca6-158">実行中のすべてのマッピングを選択し、**停止** を選択します。</span><span class="sxs-lookup"><span data-stu-id="44ca6-158">Select all running mappings, and then select **Stop**.</span></span>
4. <span data-ttu-id="44ca6-159">**リンク解除の環境** を選択します。</span><span class="sxs-lookup"><span data-stu-id="44ca6-159">Select **Unlink environment**.</span></span>
5. <span data-ttu-id="44ca6-160">**はい** を選択して操作を確認します。</span><span class="sxs-lookup"><span data-stu-id="44ca6-160">Select **Yes** to confirm the operation.</span></span>

<span data-ttu-id="44ca6-161">環境に新たなリンクを設定することができるようになります。</span><span class="sxs-lookup"><span data-stu-id="44ca6-161">You can now link a new environment.</span></span>

## <a name="unable-to-view-the-sales-order-line-information-form"></a><span data-ttu-id="44ca6-162">販売注文明細行の情報フォームを表示できない</span><span class="sxs-lookup"><span data-stu-id="44ca6-162">Unable to view the sales order line Information form</span></span> 

<span data-ttu-id="44ca6-163">Dynamics 365 Sales で販売注文を作成する際に、**+ 製品の追加** をクリックすると、Dynamics 365 Project Operations の注文明細行フォームにリダイレクトされる場合があります。</span><span class="sxs-lookup"><span data-stu-id="44ca6-163">When you create a sales order in Dynamics 365 Sales, clicking on **+ Add products** might redirect you to the Dynamics 365 Project Operations order line form.</span></span> <span data-ttu-id="44ca6-164">このフォームでは、販売注文明細行の **情報** フォームを表示することはできません。</span><span class="sxs-lookup"><span data-stu-id="44ca6-164">There is no way from that form to view the sales order line **Information** form.</span></span> <span data-ttu-id="44ca6-165">**新規注文明細行** 配下のドロップダウン リストには、**情報** のオプションが表示されません。</span><span class="sxs-lookup"><span data-stu-id="44ca6-165">The option for **Information** does not appear in the dropdown below **New Order Line**.</span></span> <span data-ttu-id="44ca6-166">これが発生するのは、プロジェクト オペレーションがご利用の環境にインストールされているためです。</span><span class="sxs-lookup"><span data-stu-id="44ca6-166">This happens because Project Operations has been installed in your environment.</span></span>

<span data-ttu-id="44ca6-167">**情報** フォームのオプションを再度有効にするには、次の手順を実行してください：</span><span class="sxs-lookup"><span data-stu-id="44ca6-167">To re-enable the **Information** form option, follow these steps:</span></span>
1. <span data-ttu-id="44ca6-168">**注文明細行** エンティティに移動します。</span><span class="sxs-lookup"><span data-stu-id="44ca6-168">Navigate to the **Order Line** entity.</span></span>
2. <span data-ttu-id="44ca6-169">フォーム ノード配下の **情報** フォームを確認します。</span><span class="sxs-lookup"><span data-stu-id="44ca6-169">Find the **Information** form under the forms node.</span></span> 
3. <span data-ttu-id="44ca6-170">**情報** フォームを選択し、**セキュリティロールの有効化** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="44ca6-170">Select the **Information** form and click **Enable security roles**.</span></span> 
4. <span data-ttu-id="44ca6-171">**すべてのユーザーに表示** されるようにセキュリティ設定を変更します。</span><span class="sxs-lookup"><span data-stu-id="44ca6-171">Change the security setting to **Display to everyone**.</span></span>
