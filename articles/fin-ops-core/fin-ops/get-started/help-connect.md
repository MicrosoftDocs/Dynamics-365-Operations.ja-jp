---
title: Finance and Operations アプリのヘルプ エクスペリエンスを構成する
description: このトピックでは、一部の Microsoft Dynamics 365 アプリのヘルプシステムのコンポーネントに関する情報を提供します。 また、これらのアプリケーションの接続方法と、ユーザー定義のヘルプを作成するプロセスの概要についても説明します。
author: margoc
manager: AnnBe
ms.date: 05/11/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: SystemParameters
audience: Application User, Developer, IT Pro
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.custom: 16141
ms.assetid: 0b9c8630-9474-4473-80fd-7db5d54b2275
ms.search.region: Global
ms.author: margoc
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 827d4cd14f497b79c85fb084a6295af13c5eb0c7
ms.sourcegitcommit: 89022f39502b19c24c0997ae3a01a64b93280f42
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/12/2020
ms.locfileid: "3367387"
---
# <a name="configure-the-help-experience-for-finance-and-operations-apps"></a><span data-ttu-id="25a8f-104">Finance and Operations アプリのヘルプ エクスペリエンスを構成する</span><span class="sxs-lookup"><span data-stu-id="25a8f-104">Configure the Help experience for Finance and Operations apps</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="25a8f-105">このトピックでは、Microsoft Dynamics 365 Finance、Dynamics 365 Supply Chain Management、Dynamics 365 Commerce、Dynamics 365 Human Resources などの Finance and Operations アプリに関するヘルプシステムのコンポーネントの概要を説明します。</span><span class="sxs-lookup"><span data-stu-id="25a8f-105">In this topic, you will find an overview of the components of the Help system for Finance and Operations apps, such as Microsoft Dynamics 365 Finance, Dynamics 365 Supply Chain Management, Dynamics 365 Commerce, and Dynamics 365 Human Resources.</span></span> <span data-ttu-id="25a8f-106">また、これらのコンポーネントの接続方法と、ユーザー定義のヘルプを作成するプロセスの概要についても説明します。</span><span class="sxs-lookup"><span data-stu-id="25a8f-106">The topic also explains how to connect these components and provides a summary of the process for creating custom Help.</span></span>

## <a name="help-architecture"></a><span data-ttu-id="25a8f-107">ヘルプ アーキテクチャ</span><span class="sxs-lookup"><span data-stu-id="25a8f-107">Help architecture</span></span>

<span data-ttu-id="25a8f-108">Finance and Operations アプリには、[https://docs.microsoft.com/dynamics365](/dynamics365/) サイトにて公開されている概要やその他のトピックが含まれています。</span><span class="sxs-lookup"><span data-stu-id="25a8f-108">Finance and Operations apps include conceptual overviews and other topics that are published to the [https://docs.microsoft.com/dynamics365](/dynamics365/) site.</span></span> <span data-ttu-id="25a8f-109">このコンテンツには、製品内の **ヘルプ** ウィンドウからアクセスできます。</span><span class="sxs-lookup"><span data-stu-id="25a8f-109">This content can then be accessed from the in-product **Help** pane.</span></span> <span data-ttu-id="25a8f-110">次の図は、ヘルプ システムの一部を示します。</span><span class="sxs-lookup"><span data-stu-id="25a8f-110">The following illustration shows the parts of the Help system.</span></span>

<span data-ttu-id="25a8f-111">[![ヘルプ アーキテクチャ](./media/help-architecture.png)](./media/help-architecture.png)</span><span class="sxs-lookup"><span data-stu-id="25a8f-111">[![Help architecture](./media/help-architecture.png)](./media/help-architecture.png)</span></span>

<span data-ttu-id="25a8f-112">製品内のヘルプ システムでは、docs.microsoft.com やその他の接続 web サイトから記事を取得しています。</span><span class="sxs-lookup"><span data-stu-id="25a8f-112">The in-product Help system pulls articles from docs.microsoft.com and other connected websites.</span></span> <span data-ttu-id="25a8f-113">また、Microsoft Dynamics Lifecycle Services (LCS) 内の業務プロセス (BPM) にて保管されているタスクガイドも取得しています。</span><span class="sxs-lookup"><span data-stu-id="25a8f-113">It also pulls in task guides that are stored in Business process modeler (BPM) in Microsoft Dynamics Lifecycle Services (LCS).</span></span>

## <a name="adding-task-guides"></a><span data-ttu-id="25a8f-114">タスク ガイドの追加</span><span class="sxs-lookup"><span data-stu-id="25a8f-114">Adding task guides</span></span>

> [!NOTE]
> <span data-ttu-id="25a8f-115">現時点では、**タスク ガイド** タブは人事管理やコマースでは使用できません。</span><span class="sxs-lookup"><span data-stu-id="25a8f-115">The **Task guides** tab isn't currently available in Human Resources or Commerce.</span></span> <!--We are currently working to enable this functionality in a future release.--> <span data-ttu-id="25a8f-116">しかし、人事管理内の [はじめに] のタスク ガイドは、基本機能の一環として利用可能となっています。</span><span class="sxs-lookup"><span data-stu-id="25a8f-116">However, the task guides in the Getting Started experience in Human Resources remain available to cover basic functionality.</span></span> <span data-ttu-id="25a8f-117">[https://docs.microsoft.com/dynamics365](/dynamics365/) 上の手順ガイドは、コマースおよび人事管理の両方で利用可能です。</span><span class="sxs-lookup"><span data-stu-id="25a8f-117">For both Human Resources and Commerce, procedural Help is available on the [https://docs.microsoft.com/dynamics365](/dynamics365/) site.</span></span>

<span data-ttu-id="25a8f-118">**システム パラメーター** ページでは、システム管理者は、実装に関連するタスク ガイド ライブラリへのアクセスを構成できます。</span><span class="sxs-lookup"><span data-stu-id="25a8f-118">On the **System parameters** page, system admins can configure access to the relevant task guide libraries for an implementation.</span></span>

> [!NOTE]
> - <span data-ttu-id="25a8f-119">ヘルプを構成するには、アプリを導入しているテナントと同じアカウントを使用してサイン インする必要があります。</span><span class="sxs-lookup"><span data-stu-id="25a8f-119">To configure Help, you must sign in by using an account in the same tenant as the tenant where the app is deployed.</span></span>
> - <span data-ttu-id="25a8f-120">ローカル仮想ハード ドライブ (VHD) で実行されているアプリのインスタンスからは、LCS ライブラリに接続することはできません。</span><span class="sxs-lookup"><span data-stu-id="25a8f-120">An LCS library can't be connected from an instance of the app that is running on a local virtual hard drive (VHD).</span></span>

<span data-ttu-id="25a8f-121">[![システム パラメーター フォームとヘルプ設定](./media/system-parameters_ops-1024x437.png)](./media/system-parameters_ops.png)</span><span class="sxs-lookup"><span data-stu-id="25a8f-121">[![System Parameters form with Help settings](./media/system-parameters_ops-1024x437.png)](./media/system-parameters_ops.png)</span></span>

<span data-ttu-id="25a8f-122">ソリューションの作業ガイドを構成するには、**システム パラメーター**のページで次の手順を実行 します。</span><span class="sxs-lookup"><span data-stu-id="25a8f-122">To configure task guides for a solution, follow these steps on the **System parameters** page.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="25a8f-123">初めて **ヘルプ** タブを開く際には、Lifecycle Services に接続する必要があります。</span><span class="sxs-lookup"><span data-stu-id="25a8f-123">The first time that you open the **Help** tab, you must connect to Lifecycle Services.</span></span> <span data-ttu-id="25a8f-124">フォームの中程のリンクを選択し、接続されるまで待機します。ダイアログ ボックスを閉じ、**OK** を選択して**システム パラメーター**ページを取得します。</span><span class="sxs-lookup"><span data-stu-id="25a8f-124">Be sure to select the link in the middle of the form, wait for the connection, close the dialog box, and then select **OK** to get to the **System Parameters** page.</span></span>
>
> <span data-ttu-id="25a8f-125">[![LCS に接続](./media/connect-to-lcs-crop-1024x365.png "LCS に接続")](./media/connect-to-lcs-crop.png)</span><span class="sxs-lookup"><span data-stu-id="25a8f-125">[![Connect to LCS](./media/connect-to-lcs-crop-1024x365.png "Connect to LCS")](./media/connect-to-lcs-crop.png)</span></span>

1. <span data-ttu-id="25a8f-126">接続する Lifecycle Services プロジェクトを選択します。</span><span class="sxs-lookup"><span data-stu-id="25a8f-126">Select the Lifecycle Services project to connect to.</span></span>
2. <span data-ttu-id="25a8f-127">タスク記録を取得する BPM ライブラリ (選択したプロジェクト内) を選択します。</span><span class="sxs-lookup"><span data-stu-id="25a8f-127">Select the BPM libraries (within the selected project) to retrieve task recordings from.</span></span>
3. <span data-ttu-id="25a8f-128">BPM ライブラリの表示順序を選択します。</span><span class="sxs-lookup"><span data-stu-id="25a8f-128">Set the display order of the BPM libraries.</span></span> <span data-ttu-id="25a8f-129">表示順序では、ライブラリからのタスク録画が**ヘルプ**ウィンドウに表示される順序を定義します。</span><span class="sxs-lookup"><span data-stu-id="25a8f-129">The display order defines the order in which task recordings from the libraries will appear in the **Help** pane.</span></span>

<span data-ttu-id="25a8f-130">これらのステップを完了すると、**ヘルプ** ウィンドウを開いて**タスク ガイド** タブを選択すすることができます。Finance and Operations アプリの現在のページに対応するタスク ガイドが表示されるようになります。</span><span class="sxs-lookup"><span data-stu-id="25a8f-130">After you complete these steps, you can open the **Help** pane and select the **Task guides** tab. You'll now see the task guides that apply to the page that you're currently on in Finance and Operations apps.</span></span> <span data-ttu-id="25a8f-131">タスク ガイドがない場合は、検索するキーワードを入力できます。</span><span class="sxs-lookup"><span data-stu-id="25a8f-131">If no task guides are found, you can enter keywords to refine your search.</span></span>

### <a name="showing-translated-task-guides"></a><span data-ttu-id="25a8f-132">翻訳されたタスク ガイドの表示</span><span class="sxs-lookup"><span data-stu-id="25a8f-132">Showing translated task guides</span></span>

<span data-ttu-id="25a8f-133">翻訳されたタスク ガイドは、2016 年 5 月の APQC 統合ライブラリと [はじめに] ライブラリで初めて公開されました。</span><span class="sxs-lookup"><span data-stu-id="25a8f-133">Translated task guides were first released in the May 2016 APQC Unified Library and in the Getting Started library.</span></span> <span data-ttu-id="25a8f-134">ローカライズされたタスク ガイドのヘルプを参照するには、ご利用の Dynamics 365 ソリューションが 2016年5月のライブラリに接続できている必要があります。</span><span class="sxs-lookup"><span data-stu-id="25a8f-134">To view localized task guide Help, make sure that your Dynamics 365 solution is connected to the May 2016 library.</span></span> <span data-ttu-id="25a8f-135">タスク ガイドの表示言語は、**オプション** &gt; **基本設定** の言語の設定で変更することができます。</span><span class="sxs-lookup"><span data-stu-id="25a8f-135">Users can change the language that a task guide appears in by changing the language settings under **Options** &gt; **Preferences**.</span></span>

> [!NOTE]
> <span data-ttu-id="25a8f-136">現在多くのタスク ガイドが翻訳されていますが、クライアントには翻訳済みのタスク ガイドの名前は表示されません。</span><span class="sxs-lookup"><span data-stu-id="25a8f-136">Although many task guides have been translated, the client doesn't currently show the translated task guide names.</span></span> <span data-ttu-id="25a8f-137">また、2016 年 5 月のライブラリでは、2016 年 2 月に公開されたタスク ガイドの翻訳版のみが利用可能です。</span><span class="sxs-lookup"><span data-stu-id="25a8f-137">Additionally, in the May 2016 library, translations are available only for the task guides that were released in February 2016.</span></span> <span data-ttu-id="25a8f-138">Microsoft は、追加された翻訳を含む更新されたライブラリをリリース予定です。</span><span class="sxs-lookup"><span data-stu-id="25a8f-138">Microsoft will release an updated library that includes additional translations.</span></span>
>
> - <span data-ttu-id="25a8f-139">タスク ガイドが翻訳されている場合、そのタスク ガイドを開くと、タスク ガイドのすべてのテキストは選択した言語で表示されます。</span><span class="sxs-lookup"><span data-stu-id="25a8f-139">If a task guide has been translated, when you open that task guide all the text of the task guide will appear in your selected language.</span></span>
> - <span data-ttu-id="25a8f-140">タスク ガイドが翻訳されていない場合、それを開くと、一部のテキスト (コントロールのテキスト) のみが選択した言語で表示されます。</span><span class="sxs-lookup"><span data-stu-id="25a8f-140">If a task guide has not yet been translated, when you open it, only some of the text (the text of the controls) will appear in your selected language.</span></span>

## <a name="adding-custom-help"></a><span data-ttu-id="25a8f-141">ユーザー定義のヘルプを追加する</span><span class="sxs-lookup"><span data-stu-id="25a8f-141">Adding custom Help</span></span>

<span data-ttu-id="25a8f-142">タスク ガイドを使用して、ユーザー定義のヘルプの作成や、**ヘルプ** ウィンドウにユーザー定義の web サイトを接続することができます。</span><span class="sxs-lookup"><span data-stu-id="25a8f-142">You can use task guides to create custom Help, or you can connect a custom Help website to the **Help** pane.</span></span>

### <a name="create-custom-help-by-using-task-guides"></a><span data-ttu-id="25a8f-143">タスク ガイドを使用したユーザー定義のヘルプを作成する</span><span class="sxs-lookup"><span data-stu-id="25a8f-143">Create custom Help by using task guides</span></span>

<span data-ttu-id="25a8f-144">実装を反映したタスクの記録を作成し、LCS のビジネス プロセス ライブラリに保存することで、対応するアプリのユーザー定義のヘルプを作成することができます。</span><span class="sxs-lookup"><span data-stu-id="25a8f-144">You can create custom Help for the supported apps by creating task recordings that reflect your implementation and then saving them to a Business process library in LCS.</span></span> <span data-ttu-id="25a8f-145">人事管理ではユーザー定義のタスク ガイドを作成することはできません。</span><span class="sxs-lookup"><span data-stu-id="25a8f-145">You can't create custom task guides for Human Resources.</span></span>

<span data-ttu-id="25a8f-146">パートナーの場合は、ライブラリを会社のライブラリに昇格してソリューションに含めることで顧客が使用することができます。</span><span class="sxs-lookup"><span data-stu-id="25a8f-146">If you're a partner, and you promote a library to a corporate library and include it in a solution, it will be available to your customers.</span></span> <span data-ttu-id="25a8f-147">APQC 統合グローバル ライブラリのコピーを作成して開き、タスクの記録を開いて編集し、変更を保存します。</span><span class="sxs-lookup"><span data-stu-id="25a8f-147">You can also make a copy of the APQC Unified Library, and then open the task recordings in the copy, edit them, and save your changes.</span></span> <span data-ttu-id="25a8f-148">詳細については、[タスク レコーダーのリソース](../../dev-itpro/user-interface/task-recorder.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="25a8f-148">For more information, see [Task recorder resources](../../dev-itpro/user-interface/task-recorder.md).</span></span>

### <a name="connect-a-custom-help-site"></a><span data-ttu-id="25a8f-149">ユーザー定義のヘルプ サイトに接続する</span><span class="sxs-lookup"><span data-stu-id="25a8f-149">Connect a custom Help site</span></span>

<span data-ttu-id="25a8f-150">Finance and Operations アプリが既成のフォームで使用されることはほとんどありません。</span><span class="sxs-lookup"><span data-stu-id="25a8f-150">Finance and Operations apps are rarely used in their out-of-box form.</span></span> <span data-ttu-id="25a8f-151">その代わりに、ソリューションは組織のニーズに合わせてカスタマイズされ、拡張されます。</span><span class="sxs-lookup"><span data-stu-id="25a8f-151">Instead, the solution is customized and extended to fit the organization's needs.</span></span> <span data-ttu-id="25a8f-152">また、ヘルプ エクスペリエンスをカスタマイズ、拡張することが可能です。</span><span class="sxs-lookup"><span data-stu-id="25a8f-152">You can also customize and extend the Help experience.</span></span> <span data-ttu-id="25a8f-153">たとえば、製品内の **ヘルプ** ウィンドウにユーザー定義のヘルプを追加できます。</span><span class="sxs-lookup"><span data-stu-id="25a8f-153">For example, you can add custom Help to the in-product **Help** pane.</span></span>

<span data-ttu-id="25a8f-154">Microsoft では、ユーザー定義のヘルプを展開して**ヘルプ**ウィンドウに接続するツールキットを提供しています。</span><span class="sxs-lookup"><span data-stu-id="25a8f-154">Microsoft has provided a toolkit to help you deploy and connect custom Help to the **Help** pane.</span></span> <span data-ttu-id="25a8f-155">**ヘルプ**ウィンドウに接続されているユーザー定義のヘルプ ソリューションを設定する方法の詳細については 、[カスタムヘルプの概要](../../dev-itpro/help/custom-help-overview.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="25a8f-155">For information about how you can set up a custom Help solution that is connected to the **Help** pane, see [Custom Help overview](../../dev-itpro/help/custom-help-overview.md).</span></span>

<span data-ttu-id="25a8f-156">ヘルプをカスタマイズするのツールやプロセスを Microsoft と連携したい場合は、[https://aka.ms/customhelpfeedback](https://aka.ms/customhelpfeedback) のフォームに記入してください。</span><span class="sxs-lookup"><span data-stu-id="25a8f-156">If you want to collaborate with Microsoft on tools and processes for customizing Help, fill in the form at [https://aka.ms/customhelpfeedback](https://aka.ms/customhelpfeedback).</span></span>

## <a name="see-also"></a><span data-ttu-id="25a8f-157">参照</span><span class="sxs-lookup"><span data-stu-id="25a8f-157">See also</span></span>

[<span data-ttu-id="25a8f-158">ヘルプ システム</span><span class="sxs-lookup"><span data-stu-id="25a8f-158">Help system</span></span>](help-overview.md)  
[<span data-ttu-id="25a8f-159">カスタム ヘルプの概要</span><span class="sxs-lookup"><span data-stu-id="25a8f-159">Custom Help overview</span></span>](../../dev-itpro/help/custom-help-overview.md)  
[<span data-ttu-id="25a8f-160">タスク レコーダー リソース</span><span class="sxs-lookup"><span data-stu-id="25a8f-160">Task recorder resources</span></span>](../../dev-itpro/user-interface/task-recorder.md)  
[<span data-ttu-id="25a8f-161">タスク レコーダーを使用したドキュメントやトレーニングの作成</span><span class="sxs-lookup"><span data-stu-id="25a8f-161">Create documentation or training with Task Recorder</span></span>](../../dev-itpro/user-interface/task-recorder-training-docs.md)  
[<span data-ttu-id="25a8f-162">カスタム ヘルプ GitHub リポジトリ</span><span class="sxs-lookup"><span data-stu-id="25a8f-162">Custom Help GitHub repository</span></span>](https://github.com/microsoft/dynamics356f-o-custom-help)  
