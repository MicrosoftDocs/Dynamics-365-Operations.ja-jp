---
title: ヘルプ システムに接続する
description: このトピックでは、Finance and Operations アプリのヘルプ システムのコンポーネントについて説明し、それらを関連付ける方法の概要や、独自のヘルプを作成する方法について説明します。
author: margoc
manager: AnnBe
ms.date: 10/02/2019
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
ms.openlocfilehash: 4427388d75c1aef40a978ce35c831d5b714f2562
ms.sourcegitcommit: 40163705a134c9874fd33be80c7ae59ccce22c21
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/03/2020
ms.locfileid: "3006175"
---
# <a name="connect-the-help-system"></a><span data-ttu-id="fa22f-103">ヘルプ システムに接続する</span><span class="sxs-lookup"><span data-stu-id="fa22f-103">Connect the Help system</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="fa22f-104">このトピックでは、Finance and Operations アプリ向けのヘルプ システムのコンポーネント (Dynamics 365 Finance、Supply Chain Management、Commerce、および Human Resourcesなど) について説明します。</span><span class="sxs-lookup"><span data-stu-id="fa22f-104">This topic describes the components of the Help system for Finance and Operations apps, such as Dynamics 365 Finance, Supply Chain Management, Commerce, and Human Resources.</span></span> <span data-ttu-id="fa22f-105">これらのコンポーネントを関連付ける方法の概要や、独自のヘルプを作成する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="fa22f-105">It provides an overview of how to connect these components and a summary of how to create custom help.</span></span>

## <a name="help-architecture"></a><span data-ttu-id="fa22f-106">ヘルプ アーキテクチャ</span><span class="sxs-lookup"><span data-stu-id="fa22f-106">Help architecture</span></span>

<span data-ttu-id="fa22f-107">次の図は、ヘルプ システムの一部を示します。</span><span class="sxs-lookup"><span data-stu-id="fa22f-107">The following illustration shows the parts of the Help system.</span></span> <span data-ttu-id="fa22f-108">製品内ヘルプ システムは https://docs.microsoft.com、Lifecycle Services (LCS) のビジネス プロセス モデラーに格納されているタスク ガイドから記事を参照します。</span><span class="sxs-lookup"><span data-stu-id="fa22f-108">The in-product Help system pulls articles from https://docs.microsoft.com, as well as task guides stored in Business Process Modeler in Lifecycle Services (LCS).</span></span>

> [!NOTE]
> <span data-ttu-id="fa22f-109">図にアスタリスク (\*) 付きで表示される機能は計画されているもので、まだ使用できません。</span><span class="sxs-lookup"><span data-stu-id="fa22f-109">The features listed in the diagram with an asterisk (\*) are planned, but are not available yet.</span></span>

<span data-ttu-id="fa22f-110">[![ヘルプ アーキテクチャ](./media/help-architecture.png)](./media/help-architecture.png)</span><span class="sxs-lookup"><span data-stu-id="fa22f-110">[![Help architecture](./media/help-architecture.png)](./media/help-architecture.png)</span></span>

## <a name="connecting-the-help-system"></a><span data-ttu-id="fa22f-111">ヘルプ システムの接続</span><span class="sxs-lookup"><span data-stu-id="fa22f-111">Connecting the Help system</span></span>

> [!NOTE]
> <span data-ttu-id="fa22f-112">**タスク ガイド** タブは、現在 Dynamics 365 Human Resources および Commerce では使用できません。</span><span class="sxs-lookup"><span data-stu-id="fa22f-112">The **Task guides** tab is currently not available in Dynamics 365 Human Resources or Commerce.</span></span> <span data-ttu-id="fa22f-113">将来のリリースではこの機能を有効にするよう、作業が進行中です。</span><span class="sxs-lookup"><span data-stu-id="fa22f-113">We are currently working to enable this functionality in a future release.</span></span> <span data-ttu-id="fa22f-114">Human Resources でのはじめにエクスペリエンスのタスク ガイドは、基本的機能をカバーするために引き続き使用可能です。</span><span class="sxs-lookup"><span data-stu-id="fa22f-114">The Task guides in the Getting Started experience in Human Resources remain available to cover basic functionality.</span></span> <span data-ttu-id="fa22f-115">Human Resources および Commerce の両方に関する docs.microsoft.com サイト上で手順を追ったヘルプを利用できます。</span><span class="sxs-lookup"><span data-stu-id="fa22f-115">Procedural help is also available on the docs.microsoft.com site for both Human Resources and Commerce.</span></span>

<span data-ttu-id="fa22f-116">**システム パラメーター** ページを使用して、システム管理者は実装に向けてヘルプ システムのピースを繋ぎ合せます。</span><span class="sxs-lookup"><span data-stu-id="fa22f-116">Using the **System Parameters** page, system administrators connect the pieces of the Help system for an implementation.</span></span>

<span data-ttu-id="fa22f-117">[![システム パラメーター フォームとヘルプ設定](./media/system-parameters_ops-1024x437.png)](./media/system-parameters_ops.png)</span><span class="sxs-lookup"><span data-stu-id="fa22f-117">[![System Parameters form with Help settings](./media/system-parameters_ops-1024x437.png)](./media/system-parameters_ops.png)</span></span>

<span data-ttu-id="fa22f-118">**システム パラメーター** ページで、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="fa22f-118">On the **System parameters** page, follow these steps:</span></span>

> [!IMPORTANT]
> <span data-ttu-id="fa22f-119">初めて **ヘルプ** タブを開く際には、Lifecycle Services に接続する必要があります。</span><span class="sxs-lookup"><span data-stu-id="fa22f-119">The first time that you open the **Help** tab, you must connect to Lifecycle Services.</span></span> <span data-ttu-id="fa22f-120">フォームの中程のリンクをクリックし、接続されるまで待機し、ダイアログ ボックスを閉じ、**OK** をクリックして**システム パラメーター**ページを取得します。</span><span class="sxs-lookup"><span data-stu-id="fa22f-120">Be sure to click the link in the middle of the form, wait for the connection, close the dialog box, and then click **OK** to get to the **System Parameters** page.</span></span>
>
> <span data-ttu-id="fa22f-121">[![LCS に接続](./media/connect-to-lcs-crop-1024x365.png "LCS に接続")](./media/connect-to-lcs-crop.png)</span><span class="sxs-lookup"><span data-stu-id="fa22f-121">[![Connect to LCS](./media/connect-to-lcs-crop-1024x365.png "Connect to LCS")](./media/connect-to-lcs-crop.png)</span></span>

1. <span data-ttu-id="fa22f-122">接続する Lifecycle Services プロジェクトを選択します。</span><span class="sxs-lookup"><span data-stu-id="fa22f-122">Select the Lifecycle Services project to connect to.</span></span>
2. <span data-ttu-id="fa22f-123">タスク記録を取得する BPM ライブラリ (選択したプロジェクト内) を選択します。</span><span class="sxs-lookup"><span data-stu-id="fa22f-123">Select the BPM libraries (within the selected project) to retrieve task recordings from.</span></span>
3. <span data-ttu-id="fa22f-124">BPM ライブラリの表示順序を選択します。</span><span class="sxs-lookup"><span data-stu-id="fa22f-124">Set the display order of the BPM libraries.</span></span> <span data-ttu-id="fa22f-125">これにより、ライブラリからのタスク記録が **ヘルプ** ウィンドウに表示される順序が決まります。</span><span class="sxs-lookup"><span data-stu-id="fa22f-125">This determines the order in which task recordings from the libraries will appear in the **Help** pane.</span></span>

<span data-ttu-id="fa22f-126">これらのステップを完了したのちに**ヘルプ** ウィンドウを開いて**タスク ガイド** タブをクリックできます。Finance and Operations アプリの現在のページに対応するタスク ガイドが表示されるようになります。</span><span class="sxs-lookup"><span data-stu-id="fa22f-126">After you complete these steps, you can open the **Help** pane and click the **Task guides** tab. You'll now see the task guides that apply to the page that you're currently on in Finance and Operations apps.</span></span> <span data-ttu-id="fa22f-127">タスク ガイドがない場合は、検索するキーワードを入力できます。</span><span class="sxs-lookup"><span data-stu-id="fa22f-127">If no task guides are found, you can enter keywords to refine your search.</span></span>

### <a name="showing-translated-task-guides"></a><span data-ttu-id="fa22f-128">翻訳されたタスク ガイドの表示</span><span class="sxs-lookup"><span data-stu-id="fa22f-128">Showing translated task guides</span></span>

<span data-ttu-id="fa22f-129">翻訳されたタスク ガイドは、2016 年 5 月の APQC 統合ライブラリおよび「はじめに」ライブラリで初めて同梱されました。</span><span class="sxs-lookup"><span data-stu-id="fa22f-129">Translated task guides were first shipped in the May 2016 APQC Unified Library, and the Getting Started library.</span></span> <span data-ttu-id="fa22f-130">Finance and Operations アプリでローカライズされたタスク ガイドのヘルプを参照するには、5 月のライブラリに接続できることを確認してください。</span><span class="sxs-lookup"><span data-stu-id="fa22f-130">In Finance and Operations apps, to see localized task guide help, make sure that you are connected to the May library.</span></span> <span data-ttu-id="fa22f-131">タスク ガイドの表示言語は、**オプション** &gt; **基本設定** の [言語の設定] でユーザーごとに制御されます。</span><span class="sxs-lookup"><span data-stu-id="fa22f-131">The language that a task guide appears in is controlled for each user by the Language settings under **Options** &gt; **Preferences**.</span></span>

> [!NOTE]
> <span data-ttu-id="fa22f-132">多くの作業ガイドが翻訳されていますが、現在クライアントには翻訳済みのタスクガイドの名前は表示されません。</span><span class="sxs-lookup"><span data-stu-id="fa22f-132">Even though many task guides have been translated, right now the client is not showing the translated task guide names.</span></span> <span data-ttu-id="fa22f-133">また、現時点では 2016 年 2 月にリリースされたタスク ガイドのみが 5 月のライブラリで翻訳版として利用可能です。</span><span class="sxs-lookup"><span data-stu-id="fa22f-133">Also, only the task guides that were released in February 2016 are available in translation in the May library.</span></span> <span data-ttu-id="fa22f-134">翻訳の追加のあるライブラリ更新をリリース予定です。</span><span class="sxs-lookup"><span data-stu-id="fa22f-134">We will release an updated library with additional translations.</span></span>
>
> - <span data-ttu-id="fa22f-135">タスク ガイドが翻訳されている場合、そのタスク ガイドを開くと、タスク ガイドのすべてのテキストは選択した言語で表示されます。</span><span class="sxs-lookup"><span data-stu-id="fa22f-135">If a task guide has been translated, when you open that task guide all the text of the task guide will appear in your selected language.</span></span>
> - <span data-ttu-id="fa22f-136">タスク ガイドが翻訳されていない場合、それを開くと、一部のテキスト (コントロールのテキスト) のみが選択した言語で表示されます。</span><span class="sxs-lookup"><span data-stu-id="fa22f-136">If a task guide has not yet been translated, when you open it, only some of the text (the text of the controls) will appear in your selected language.</span></span>

## <a name="creating-custom-help"></a><span data-ttu-id="fa22f-137">カスタム ヘルプの作成</span><span class="sxs-lookup"><span data-stu-id="fa22f-137">Creating custom help</span></span>

<span data-ttu-id="fa22f-138">タスク ガイドを使用して、カスタム ヘルプを作成したり、ヘルプ ウィンドウを Web サイトに接続できます。</span><span class="sxs-lookup"><span data-stu-id="fa22f-138">You can use task guides to create custom help, or connect a website to the Help pane.</span></span>

### <a name="create-custom-help-with-task-guides"></a><span data-ttu-id="fa22f-139">タスク ガイドを使用したカスタム ヘルプの作成</span><span class="sxs-lookup"><span data-stu-id="fa22f-139">Create custom help with task guides</span></span>

<span data-ttu-id="fa22f-140">実装を反映するタスク記録を作成して LCS 業務プロセス ライブラリに保存することで、Finance、Supply Chain Management、および Commerce のカスタム ヘルプを作成できます。</span><span class="sxs-lookup"><span data-stu-id="fa22f-140">You can create custom help for Finance, Supply Chain Management, and Commerce by creating task recordings that reflect your implementation, and saving them to an LCS Business Process Library.</span></span> <span data-ttu-id="fa22f-141">Human Resources のカスタム タスク ガイドを作成することはできません。</span><span class="sxs-lookup"><span data-stu-id="fa22f-141">You cannot create custom task guides for Human Resources.</span></span>

<span data-ttu-id="fa22f-142">パートナーの場合、ライブラリを会社のライブラリに昇格してソリューションに含める場合、顧客が使用できます。</span><span class="sxs-lookup"><span data-stu-id="fa22f-142">For partners, if you promote a library to be a corporate library, and include it in a solution, it will be available to your customers.</span></span> <span data-ttu-id="fa22f-143">APQC 統合グローバル ライブラリのコピーを作成して開き、タスクの記録を開いて変更し、変更がある記録を保存します。</span><span class="sxs-lookup"><span data-stu-id="fa22f-143">You can also make a copy of the APQC Unified global library, and then open your copy, open task recordings from it, modify them, and save the recordings with your changes.</span></span> <span data-ttu-id="fa22f-144">詳細については、[タスク レコーダーのリソース](../../dev-itpro/user-interface/task-recorder.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="fa22f-144">For more information, see [Task recorder resources](../../dev-itpro/user-interface/task-recorder.md).</span></span>

### <a name="connect-a-custom-site"></a><span data-ttu-id="fa22f-145">カスタム サイトを接続する</span><span class="sxs-lookup"><span data-stu-id="fa22f-145">Connect a custom site</span></span>

<span data-ttu-id="fa22f-146">Microsoft は、カスタム ヘルプのサイトを作成およびヘルプ ウィンドウに接続する方法について説明するホワイト ペーパーおよびサンプル コードを提供しています。</span><span class="sxs-lookup"><span data-stu-id="fa22f-146">Microsoft has provided a white paper and sample code that describe how to create and connect a custom help site to the Help pane.</span></span> <span data-ttu-id="fa22f-147">詳細については、以下を参照してください。</span><span class="sxs-lookup"><span data-stu-id="fa22f-147">For more information, see:</span></span>

- [<span data-ttu-id="fa22f-148">Finance and Operations アプリ (ホワイト ペーパー) のカスタム ヘルプの作成</span><span class="sxs-lookup"><span data-stu-id="fa22f-148">Create Custom Help for Finance and Operations apps (white paper)</span></span>](https://go.microsoft.com/fwlink/?linkid=2041185)
- [<span data-ttu-id="fa22f-149">カスタム ヘルプ GitHub リポジトリ</span><span class="sxs-lookup"><span data-stu-id="fa22f-149">Custom help GitHub repository</span></span>](https://github.com/microsoft/dynamics356f-o-custom-help)

## <a name="additional-resources"></a><span data-ttu-id="fa22f-150">追加リソース</span><span class="sxs-lookup"><span data-stu-id="fa22f-150">Additional resources</span></span>

[<span data-ttu-id="fa22f-151">ヘルプ システム</span><span class="sxs-lookup"><span data-stu-id="fa22f-151">Help system</span></span>](help-overview.md)

[<span data-ttu-id="fa22f-152">タスク レコーダー リソース</span><span class="sxs-lookup"><span data-stu-id="fa22f-152">Task recorder resources</span></span>](../../dev-itpro/user-interface/task-recorder.md)

[<span data-ttu-id="fa22f-153">タスク レコーダーを使用したドキュメントやトレーニングの作成</span><span class="sxs-lookup"><span data-stu-id="fa22f-153">Create documentation or training with Task Recorder</span></span>](../../dev-itpro/user-interface/task-recorder-training-docs.md)
