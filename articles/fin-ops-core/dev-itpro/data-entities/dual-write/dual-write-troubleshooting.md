---
title: 一般的なトラブルシューティング
description: このトピックでは、Finance and Operations アプリと Common Data Service 間のデュアル書き込み統合に関する一般的なトラブルシューティングの情報を提供します。
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
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-03-16
ms.openlocfilehash: f7ee0b5aa4e72614205e129acd986376b33efc70
ms.sourcegitcommit: 68f1485de7d64a6c9eba1088af63bd07992d972d
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/27/2020
ms.locfileid: "3172694"
---
# <a name="general-troubleshooting"></a><span data-ttu-id="460c7-103">一般的なトラブルシューティング</span><span class="sxs-lookup"><span data-stu-id="460c7-103">General troubleshooting</span></span>

[!include [banner](../../includes/banner.md)]



<span data-ttu-id="460c7-104">このトピックでは、Finance and Operations アプリと Common Data Service 間のデュアル書き込み統合に関する一般的なトラブルシューティングの情報を提供します。</span><span class="sxs-lookup"><span data-stu-id="460c7-104">This topic provides general troubleshooting information for dual-write integration between Finance and Operations apps and Common Data Service.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="460c7-105">このトピックで説明されている問題の中には、システム管理者ロールまたは Microsoft Azure Active Directory（Azure AD）テナント管理者の資格情報のいずれかが必要な場合があります。</span><span class="sxs-lookup"><span data-stu-id="460c7-105">Some of the issues that this topic addresses might require either the system admin role or Microsoft Azure Active Directory (Azure AD) tenant admin credentials.</span></span> <span data-ttu-id="460c7-106">各問題のセクションでは、特定のロールまたは資格情報が必要な場合について説明しています。</span><span class="sxs-lookup"><span data-stu-id="460c7-106">The section for each issue explains whether a specific role or credentials are required.</span></span>

## <a name="when-you-try-to-install-the-dual-write-package-by-using-the-package-deployer-tool-no-available-solutions-are-shown"></a><span data-ttu-id="460c7-107">Package Deployer ツールを使用してデュアル書書き込み込みパッケージをインストールしようとすると、使用可能なソリューションが表示されない</span><span class="sxs-lookup"><span data-stu-id="460c7-107">When you try to install the dual-write package by using the package deployer tool, no available solutions are shown</span></span>

<span data-ttu-id="460c7-108">Package Deployer ツールの一部のバージョンは、デュアル書き込みソリューション パッケージと互換性がありません。</span><span class="sxs-lookup"><span data-stu-id="460c7-108">Some versions of the package deployer tool are incompatible with the dual-write solution package.</span></span> <span data-ttu-id="460c7-109">パッケージを正常にインストールするには、Package Deployer ツールの [バージョン 9.1.0.20](https://www.nuget.org/packages/Microsoft.CrmSdk.XrmTooling.PackageDeployment.Wpf/9.1.0.20) またはそれ以降を使用してください。</span><span class="sxs-lookup"><span data-stu-id="460c7-109">To successfully install the package, be sure to use [version 9.1.0.20](https://www.nuget.org/packages/Microsoft.CrmSdk.XrmTooling.PackageDeployment.Wpf/9.1.0.20) or later of the package deployer tool.</span></span>

<span data-ttu-id="460c7-110">Package Deployer ツールをインストールした後、次の手順に従ってソリューション パッケージをインストールしてください。</span><span class="sxs-lookup"><span data-stu-id="460c7-110">After you install the package deployer tool, install the solution package by following these steps.</span></span>

1. <span data-ttu-id="460c7-111">Yammer.com から最新のソリューション パッケージ ファイルをダウンロードします。</span><span class="sxs-lookup"><span data-stu-id="460c7-111">Download the latest solution package file from Yammer.com.</span></span> <span data-ttu-id="460c7-112">パッケージのZIP ファイルをダウンロードした後、ファイルを右クリックして **プロパティ**を選択します。</span><span class="sxs-lookup"><span data-stu-id="460c7-112">After the package zip file is downloaded, right-click it, and select **Properties**.</span></span> <span data-ttu-id="460c7-113">**ブロックの解除** チェック ボックスを選択し、**適用** を選択します。</span><span class="sxs-lookup"><span data-stu-id="460c7-113">Select the **Unblock** check box, and then select **Apply**.</span></span> <span data-ttu-id="460c7-114">**ブロックの解除** チェックボックスが表示されない場合は、zip ファイルのブロック解除が既にされているため、この手順を省略できます。</span><span class="sxs-lookup"><span data-stu-id="460c7-114">If you don't see the **Unblock** check box, the zip file is already unblocked, and you can skip this step.</span></span>

    ![プロパティ ダイアログ ボックス](media/unblock_option.png)

2. <span data-ttu-id="460c7-116">パッケージの zip ファイルを展開し、**Dynamics365FinanceAndOperationsCommon** フォルダのすべてのファイルをコピーします。</span><span class="sxs-lookup"><span data-stu-id="460c7-116">Extract the package zip file, and copy all the files in the **Dynamics365FinanceAndOperationsCommon.PackageDeployer.2.0.438** folder.</span></span>

    ![Dynamics365FinanceAndOperationsCommon.PackageDeployer.2.0.438 フォルダの内容](media/extract_package.png)

3. <span data-ttu-id="460c7-118">コピーされたすべてのファイルを Package Deployer ツールの**Tools** フォルダーに貼り付けます。</span><span class="sxs-lookup"><span data-stu-id="460c7-118">Paste all the copied files into the **Tools** folder of the package deployer tool.</span></span> 
4. <span data-ttu-id="460c7-119">**PackageDeployer.exe** を実行して Common Data Service の環境を選択し、ソリューションをインストールします。</span><span class="sxs-lookup"><span data-stu-id="460c7-119">Run **PackageDeployer.exe** to select the Common Data Service environment and install the solutions.</span></span>

    ![ツール フォルダのコンテンツ](media/paste_copied_files.png)

## <a name="enable-and-view-the-plug-in-trace-log-in-common-data-service-to-view-error-details"></a><span data-ttu-id="460c7-121">Common Data Service のプラグイン トレース ログを有効にして確認し、エラーの詳細を表示します。</span><span class="sxs-lookup"><span data-stu-id="460c7-121">Enable and view the plug-in trace log in Common Data Service to view error details</span></span>

<span data-ttu-id="460c7-122">**トレース ログを有効にするために必要な役割とエラーの表示:** システム管理者</span><span class="sxs-lookup"><span data-stu-id="460c7-122">**Required role to turn on the trace log and view errors:** System admin</span></span>

<span data-ttu-id="460c7-123">トレース ログを有効にするには、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="460c7-123">To turn on the trace log, follow these steps.</span></span>

1. <span data-ttu-id="460c7-124">Finance and Operations アプリにログインし、**設定** ページを開いて、**システム** 配下の**管理** を選択します。</span><span class="sxs-lookup"><span data-stu-id="460c7-124">Sign in to the Finance and Operations app, open the **Settings** page, and then, under **System**, select **Administration**.</span></span>
2. <span data-ttu-id="460c7-125">**管理者** ページで、**システム管理**を選択します。</span><span class="sxs-lookup"><span data-stu-id="460c7-125">On the **Administration** page, select **System Settings**.</span></span>
3. <span data-ttu-id="460c7-126">**カスタマイズ** タブの **プラグインおよびユーザー定義ワークフロー活動の追跡** フィールドで、**すべて** を選択してプラグインのトレース ログを有効にします。</span><span class="sxs-lookup"><span data-stu-id="460c7-126">On the **Customization** tab, in the **Plug-in and custom workflow activity tracing** field, select **All** to enable the plug-in trace log.</span></span> <span data-ttu-id="460c7-127">例外が発生したときにのみトレースログを記録する場合は **例外** を選択します。</span><span class="sxs-lookup"><span data-stu-id="460c7-127">If you want to log trace logs only when exceptions occur, you can select **Exception** instead.</span></span>


<span data-ttu-id="460c7-128">トレースログを確認にするには、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="460c7-128">To view the trace log, follow these steps.</span></span>

1. <span data-ttu-id="460c7-129">Finance and Operations アプリにログインし、**設定** ページを開いて、**カスタマイズ** 配下の**プラグイン トレース ログ** を選択します。</span><span class="sxs-lookup"><span data-stu-id="460c7-129">Sign in to the Finance and Operations app, open the **Settings** page, and then, under **Customization**, select **Plug-in Trace Log**.</span></span>
2. <span data-ttu-id="460c7-130">**タイプ名** フィールドが **Microsoft.Dynamics.Integrator.CrmPlugins.Plugin**に設定されているトレース ログを検索します。</span><span class="sxs-lookup"><span data-stu-id="460c7-130">Find the trace logs where the **Type Name** field is set to **Microsoft.Dynamics.Integrator.CrmPlugins.Plugin**.</span></span>
3. <span data-ttu-id="460c7-131">完全なログを表示するには、項目をダブルクリックし、**実行**ファストタブで **メッセージ ブロック** のテキストを確認します。</span><span class="sxs-lookup"><span data-stu-id="460c7-131">Double-click an item to view the full log, and then, on the **Execution** FastTab, review the **Message Block** text.</span></span>

## <a name="enable-debug-mode-to-troubleshoot-live-synchronization-issues-in-finance-and-operations-apps"></a><span data-ttu-id="460c7-132">デバッグ モードを有効にして、アプリ Finance and Operations でのライブ同期に関する問題のトラブルシューティングを行います。</span><span class="sxs-lookup"><span data-stu-id="460c7-132">Enable debug mode to troubleshoot live synchronization issues in Finance and Operations apps</span></span>

<span data-ttu-id="460c7-133">**エラーを表示するために必要な役割：** システム管理者</span><span class="sxs-lookup"><span data-stu-id="460c7-133">**Required role to view the errors:** System admin</span></span>

<span data-ttu-id="460c7-134">Common Data Serviceで発生するデュアル書き込みエラーは、Finance and Operationsアプリでも発生する場合があります。</span><span class="sxs-lookup"><span data-stu-id="460c7-134">Dual-write errors that originate in Common Data Service can appear in the Finance and Operations app.</span></span> <span data-ttu-id="460c7-135">エラーメッセージの完全なテキストが表示されない場合がありますが、これはメッセージが長すぎるか個人の識別情報 (PII) が含まれていることが原因です。</span><span class="sxs-lookup"><span data-stu-id="460c7-135">In some cases, the full text of the error message isn't available because the message is too long or contains personally identifying information (PII).</span></span> <span data-ttu-id="460c7-136">エラーの詳細ログを有効にするには、次の手順を実行してください。</span><span class="sxs-lookup"><span data-stu-id="460c7-136">You can turn on verbose logging for errors by following these steps.</span></span>

1. <span data-ttu-id="460c7-137">Finance and Operations アプリにおけるすべてのプロジェクトの構成は、**DualWriteProjectConfiguration** エンティティ内に **IsDebugMode** プロパティが存在します。</span><span class="sxs-lookup"><span data-stu-id="460c7-137">All project configurations in Finance and Operations apps have an **IsDebugMode** property in the **DualWriteProjectConfiguration** entity.</span></span> <span data-ttu-id="460c7-138">Excel アドインを使用して **DualWriteProjectConfiguration** エンティティを開きます。</span><span class="sxs-lookup"><span data-stu-id="460c7-138">Open the **DualWriteProjectConfiguration** entity by using the Excel add-in.</span></span>

    > [!TIP]
    > <span data-ttu-id="460c7-139">エンティティを簡単に開くには、Excelアドインで **デザイン** モードを有効にしてから、ワークシートに**DualWriteProjectConfigurationEntity** を追加してください。</span><span class="sxs-lookup"><span data-stu-id="460c7-139">An easy way to open the entity is to turn on **Design** mode in the Excel add-in and then add **DualWriteProjectConfigurationEntity** to the worksheet.</span></span> <span data-ttu-id="460c7-140">詳細については、[Excel でエンティティ データを開き、Excel アドインを使用して更新する](../../office-integration/use-excel-add-in.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="460c7-140">For more information, see [Open entity data in Excel and update it by using the Excel add-in](../../office-integration/use-excel-add-in.md).</span></span>

2. <span data-ttu-id="460c7-141">プロジェクトの **IsDebugMode**プロパティを **はい** に設定します。</span><span class="sxs-lookup"><span data-stu-id="460c7-141">Set the **IsDebugMode** property to **Yes** for the project.</span></span>
3. <span data-ttu-id="460c7-142">エラーが発生するシナリオを実行します。</span><span class="sxs-lookup"><span data-stu-id="460c7-142">Run the scenario that is generating errors.</span></span>
4. <span data-ttu-id="460c7-143">詳細なログは、DualWriteErrorLog テーブルで確認できます。</span><span class="sxs-lookup"><span data-stu-id="460c7-143">The verbose logs are available in the DualWriteErrorLog table.</span></span> <span data-ttu-id="460c7-144">テーブル ブラウザーでデータを参照するには、次のURLを使用してください（必要に応じて**XXX**を置き換えてください）：</span><span class="sxs-lookup"><span data-stu-id="460c7-144">To look up data in the table browser, use the following URL (replace **XXX** as appropriate):</span></span>

    `https://XXXaos.cloudax.dynamics.com/?mi=SysTableBrowser&tableName=>DualWriteErrorLog`

## <a name="check-synchronization-errors-on-the-virtual-machine-for-the-finance-and-operations-app"></a><span data-ttu-id="460c7-145">Finance and Operations アプリの仮想マシンの同期エラーを確認する</span><span class="sxs-lookup"><span data-stu-id="460c7-145">Check synchronization errors on the virtual machine for the Finance and Operations app</span></span>

<span data-ttu-id="460c7-146">**エラーを表示するために必要な役割：** システム管理者</span><span class="sxs-lookup"><span data-stu-id="460c7-146">**Required role to view the errors:** System admin</span></span>

1. <span data-ttu-id="460c7-147">Microsoft Dynamics Lifecycle Services (LCS) にログインします。</span><span class="sxs-lookup"><span data-stu-id="460c7-147">Sign in to Microsoft Dynamics Lifecycle Services (LCS).</span></span>
2. <span data-ttu-id="460c7-148">デュアル書き込みテストを実行する、LCS プロジェクトを開きます。</span><span class="sxs-lookup"><span data-stu-id="460c7-148">Open the LCS project that you chose to do the dual-write testing for.</span></span>
3. <span data-ttu-id="460c7-149">**クラウド ホスト環境**のタイトルを選択します。</span><span class="sxs-lookup"><span data-stu-id="460c7-149">Select the **Cloud-hosted environments** tile.</span></span>
4. <span data-ttu-id="460c7-150">リモート デスクトップを使用して、Finance and Operations アプリの仮想マシン (VM) にログインします。</span><span class="sxs-lookup"><span data-stu-id="460c7-150">Use Remote Desktop to sign in to the virtual machine (VM) for the Finance and Operations app.</span></span> <span data-ttu-id="460c7-151">LCS に表示されるローカル アカウントを使用します。</span><span class="sxs-lookup"><span data-stu-id="460c7-151">Use the local account that is shown in LCS.</span></span>
5. <span data-ttu-id="460c7-152">イベント ビューアーを開きます。</span><span class="sxs-lookup"><span data-stu-id="460c7-152">Open Event viewer.</span></span>
6. <span data-ttu-id="460c7-153">**アプリケーションとサービス ログ \> Microsoft \> Dynamics \> AX-DualWriteSync \> オペレーション**を選択します。</span><span class="sxs-lookup"><span data-stu-id="460c7-153">Select **Applications and Services Logs \> Microsoft \> Dynamics \> AX-DualWriteSync \> Operational**.</span></span>
7. <span data-ttu-id="460c7-154">最近発生したエラーの一覧を確認します。</span><span class="sxs-lookup"><span data-stu-id="460c7-154">Review the list of recent errors.</span></span>

## <a name="unlink-and-link-another-common-data-service-environment-from-a-finance-and-operations-app"></a><span data-ttu-id="460c7-155">Finance and Operations アプリの Common Data Service 環境のリンクを解除し、他の環境をリンクする</span><span class="sxs-lookup"><span data-stu-id="460c7-155">Unlink and link another Common Data Service environment from a Finance and Operations app</span></span>

<span data-ttu-id="460c7-156">**環境のリンクの解除に必要な資格情報：** Azure ADテナント管理者</span><span class="sxs-lookup"><span data-stu-id="460c7-156">**Required credentials to unlink the environment:** Azure AD tenant admin</span></span>

1. <span data-ttu-id="460c7-157">Finance and Operations アプリにサインインします。</span><span class="sxs-lookup"><span data-stu-id="460c7-157">Sign in to the Finance and Operations app.</span></span>
2. <span data-ttu-id="460c7-158">**ワークスペース \> データ管理**に移動して、**デュアル書き込み**のタイルを選択します。</span><span class="sxs-lookup"><span data-stu-id="460c7-158">Go to **Workspaces \> Data management**, and select the **Dual Write** tile.</span></span>
3. <span data-ttu-id="460c7-159">実行中のすべてのマッピングを選択し、**停止**を選択します。</span><span class="sxs-lookup"><span data-stu-id="460c7-159">Select all running mappings, and then select **Stop**.</span></span>
4. <span data-ttu-id="460c7-160">**リンク解除の環境**を選択します。</span><span class="sxs-lookup"><span data-stu-id="460c7-160">Select **Unlink environment**.</span></span>
5. <span data-ttu-id="460c7-161">**はい**を選択して操作を確認します。</span><span class="sxs-lookup"><span data-stu-id="460c7-161">Select **Yes** to confirm the operation.</span></span>

<span data-ttu-id="460c7-162">環境に新たなリンクを設定することができるようになります。</span><span class="sxs-lookup"><span data-stu-id="460c7-162">You can now link a new environment.</span></span>
