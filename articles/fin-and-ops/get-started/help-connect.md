---
title: "ヘルプ システムに接続する"
description: "このトピックでは、Microsoft Dynamics 365 for Finance and Operations のヘルプ システムのコンポーネンツについて説明し、それらを関連付ける方法の概要や、独自のヘルプを作成する方法について説明します。"
author: margoc
manager: AnnBe
ms.date: 09/11/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
ms.search.form: SystemParameters
audience: Application User, Developer, IT Pro
ms.reviewer: margoc
ms.search.scope: Core, Operations
ms.custom: 16141
ms.assetid: 0b9c8630-9474-4473-80fd-7db5d54b2275
ms.search.region: Global
ms.author: margoc
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: c0942b66859da3659be49b19986bfd146ac43130
ms.contentlocale: ja-jp
ms.lasthandoff: 11/03/2017

---

# <a name="connect-the-help-system"></a><span data-ttu-id="6c6d6-103">ヘルプ システムに接続する</span><span class="sxs-lookup"><span data-stu-id="6c6d6-103">Connect the Help system</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="6c6d6-104">このトピックでは、Microsoft Dynamics 365 for Finance and Operations のヘルプ システムのコンポーネントについて説明します。</span><span class="sxs-lookup"><span data-stu-id="6c6d6-104">This topic describes the components of the Help system for Microsoft Dynamics 365 for Finance and Operations.</span></span> <span data-ttu-id="6c6d6-105">これらのコンポーネントを関連付ける方法の概要や、独自のヘルプを作成する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="6c6d6-105">It provides an overview of how to connect these components and a summary of how to create custom help.</span></span> 

## <a name="help-architecture"></a><span data-ttu-id="6c6d6-106">ヘルプ アーキテクチャ</span><span class="sxs-lookup"><span data-stu-id="6c6d6-106">Help architecture</span></span>
<span data-ttu-id="6c6d6-107">次の図では、Finance and Operations のヘルプ システムの一部を示します。</span><span class="sxs-lookup"><span data-stu-id="6c6d6-107">The following illustration shows the parts of the Finance and Operations Help system.</span></span> <span data-ttu-id="6c6d6-108">製品内ヘルプ システムは https://docs.microsoft.com の Finance and Operations サイト、Lifecycle Services (LCS) のビジネス プロセス モデラーに格納されているタスク ガイドから記事を参照します。</span><span class="sxs-lookup"><span data-stu-id="6c6d6-108">The in-product Help system pulls articles from the Finance and Operations site on https://docs.microsoft.com, as well as task guides stored in Business Process Modeler in Lifecycle Services (LCS).</span></span> 
> [!NOTE]
> <span data-ttu-id="6c6d6-109">図にアスタリスク (\*) 付きで表示される機能は計画されているもので、まだ使用できません。</span><span class="sxs-lookup"><span data-stu-id="6c6d6-109">The features listed in the diagram with an asterisk (\*) are planned, but are not available yet.</span></span> <span data-ttu-id="6c6d6-110">[![ヘルプ アーキテクチャ](./media/help-architecture.png)](./media/help-architecture.png)</span><span class="sxs-lookup"><span data-stu-id="6c6d6-110">[![Help architecture](./media/help-architecture.png)](./media/help-architecture.png)</span></span>


## <a name="connecting-the-help-system"></a><span data-ttu-id="6c6d6-111">ヘルプ システムの接続</span><span class="sxs-lookup"><span data-stu-id="6c6d6-111">Connecting the Help system</span></span>
> [!NOTE]
> <span data-ttu-id="6c6d6-112">[**タスク ガイド**] タブは、Microsoft Dynamics 365 for Talent および Microsoft Dynamics 365 for Retail で現在使用できません。</span><span class="sxs-lookup"><span data-stu-id="6c6d6-112">The **Task guides** tab is currently not available in Microsoft Dynamics 365 for Talent and Microsoft Dynamics 365 for Retail.</span></span> <span data-ttu-id="6c6d6-113">将来のリリースではこの機能を有効にするよう、作業が進行中です。</span><span class="sxs-lookup"><span data-stu-id="6c6d6-113">We are currently working to enable this functionality in a future release.</span></span> <span data-ttu-id="6c6d6-114">[Talent] での [はじめに] の経験タスク ガイドは、基本的機能をカバーするために引き続き使用可能です。</span><span class="sxs-lookup"><span data-stu-id="6c6d6-114">The Task guides in the Getting Started experience in Talent remain available to cover basic functionality.</span></span> <span data-ttu-id="6c6d6-115">[Retail] および [Talent] の両方に関する docs.microsoft.com サイト上 ([docs.microsoft.com/dynamics365/unified-operations](../../index.md)) でも利用可能な、手順を追ったヘルプ。</span><span class="sxs-lookup"><span data-stu-id="6c6d6-115">Procedural help is also available on the docs.microsoft.com site ([docs.microsoft.com/dynamics365/unified-operations](../../index.md)) for both Retail and Talent.</span></span>
 

<span data-ttu-id="6c6d6-116">**システム パラメーター** ページを使用して、システム管理者は実装に向けてヘルプ システムのピースを繋ぎ合せます。</span><span class="sxs-lookup"><span data-stu-id="6c6d6-116">Using the **System Parameters** page, system administrators connect the pieces of the Help system for an implementation.</span></span> <span data-ttu-id="6c6d6-117">[![システム パラメーター フォームとヘルプ設定](./media/system-parameters_ops-1024x437.png)](./media/system-parameters_ops.png) **システム パラメーター** ページで次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="6c6d6-117">[![System Parameters form with Help settings](./media/system-parameters_ops-1024x437.png)](./media/system-parameters_ops.png) On the **System parameters** page, follow these steps:</span></span>

> [!IMPORTANT]
> <span data-ttu-id="6c6d6-118">初めて **ヘルプ** タブを開く際には、Lifecycle Services に接続する必要があります。</span><span class="sxs-lookup"><span data-stu-id="6c6d6-118">The first time that you open the **Help** tab, you must connect to Lifecycle Services.</span></span> <span data-ttu-id="6c6d6-119">フォームの中程のリンクをクリックし、接続されるまで待機し、ダイアログ ボックスを閉じ、[**OK**] をクリックして**システム パラメーター** ページを取得します。[![LCS に接続](./media/connect-to-lcs-crop-1024x365.png "Connect to LCS")](./media/connect-to-lcs-crop.png)</span><span class="sxs-lookup"><span data-stu-id="6c6d6-119">Be sure to click the link in the middle of the form, wait for the connection, close the dialog box, and then click **OK** to get to the **System Parameters** page.[![Connect to LCS](./media/connect-to-lcs-crop-1024x365.png "Connect to LCS")](./media/connect-to-lcs-crop.png)</span></span>

1.  <span data-ttu-id="6c6d6-120">接続する Lifecycle Services プロジェクトを選択します。</span><span class="sxs-lookup"><span data-stu-id="6c6d6-120">Select the Lifecycle Services project to connect to.</span></span>
2.  <span data-ttu-id="6c6d6-121">タスク記録を取得する BPM ライブラリ (選択したプロジェクト内) を選択します。</span><span class="sxs-lookup"><span data-stu-id="6c6d6-121">Select the BPM libraries (within the selected project) to retrieve task recordings from.</span></span>
    - <span data-ttu-id="6c6d6-122">Finance and Operations、Microsoft のコンテンツ用に、Finance and Operations 用の最新の APQC 統合ライブラリを選択します。</span><span class="sxs-lookup"><span data-stu-id="6c6d6-122">For Finance and Operations, for Microsoft content, select the most recent APQC Unified Library for Finance and Operations.</span></span> 
    - <span data-ttu-id="6c6d6-123">[Retail] 用に、近い将来にライブラリをリリースする予定です。</span><span class="sxs-lookup"><span data-stu-id="6c6d6-123">For Retail, we will be releasing a library in the near future.</span></span> 
    - <span data-ttu-id="6c6d6-124">[Talent] のライブラリを選択する必要はありません。適切なライブラリへの接続が確立されます。</span><span class="sxs-lookup"><span data-stu-id="6c6d6-124">You do not need to select a library for Talent—the connection to the correct library is established for you.</span></span> 

3.  <span data-ttu-id="6c6d6-125">BPM ライブラリの表示順序を選択します。</span><span class="sxs-lookup"><span data-stu-id="6c6d6-125">Set the display order of the BPM libraries.</span></span> <span data-ttu-id="6c6d6-126">これにより、ライブラリからのタスク記録が [**ヘルプ**] ウィンドウに表示される順序が決まります。</span><span class="sxs-lookup"><span data-stu-id="6c6d6-126">This determines the order in which task recordings from the libraries will appear in the **Help** pane.</span></span>

<span data-ttu-id="6c6d6-127">これらのステップを完了したのちに [**ヘルプ**] ウィンドウを開いて [**タスク ガイド**] タブをクリックできます。Finance and Operations の現在のページに対応するタスク ガイドが表示されるようになります。</span><span class="sxs-lookup"><span data-stu-id="6c6d6-127">After you complete these steps, you can open the **Help** pane and click the **Task guides** tab. You'll now see the task guides that apply to the page that you’re currently on in Finance and Operations.</span></span> <span data-ttu-id="6c6d6-128">タスク ガイドがない場合は、検索するキーワードを入力できます。</span><span class="sxs-lookup"><span data-stu-id="6c6d6-128">If no task guides are found, you can enter keywords to refine your search.</span></span>

### <a name="showing-translated-task-guides"></a><span data-ttu-id="6c6d6-129">翻訳されたタスク ガイドの表示</span><span class="sxs-lookup"><span data-stu-id="6c6d6-129">Showing translated task guides</span></span>

<span data-ttu-id="6c6d6-130">翻訳されたタスク ガイドは、2016 年 5 月の APQC 統合ライブラリおよび「はじめに」ライブラリで初めて同梱されました。</span><span class="sxs-lookup"><span data-stu-id="6c6d6-130">Translated task guides were first shipped in the May 2016 APQC Unified Library, and the Getting Started library.</span></span> <span data-ttu-id="6c6d6-131">Finance and Operations でローカライズされたタスク ガイドのヘルプを参照するには、5 月のライブラリに接続できることを確認してください。</span><span class="sxs-lookup"><span data-stu-id="6c6d6-131">In Finance and Operations, to see localized task guide help, make sure that you are connected to the May library.</span></span> <span data-ttu-id="6c6d6-132">タスク ガイドの表示言語は、[**オプション**] &gt; [**基本設定**] の [言語の設定] でユーザーごとに制御されます。</span><span class="sxs-lookup"><span data-stu-id="6c6d6-132">The language that a task guide appears in is controlled for each user by the Language settings under **Options** &gt; **Preferences**.</span></span> 

> [!NOTE]
> <span data-ttu-id="6c6d6-133">多くのタスク ガイドが翻訳されていますが、現在 Finance and Operations クライアントには翻訳済みのタスク ガイド名は表示されません。</span><span class="sxs-lookup"><span data-stu-id="6c6d6-133">Even though many task guides have been translated, right now the Finance and Operations client is not showing the translated task guide names.</span></span> <span data-ttu-id="6c6d6-134">また、現時点では 2016 年 2 月にリリースされたタスク ガイドのみが 5 月のライブラリで翻訳版として利用可能です。</span><span class="sxs-lookup"><span data-stu-id="6c6d6-134">Also, only the task guides that were released in February 2016 are available in translation in the May library.</span></span> <span data-ttu-id="6c6d6-135">翻訳の追加のあるライブラリ更新をリリース予定です。</span><span class="sxs-lookup"><span data-stu-id="6c6d6-135">We will release an updated library with additional translations.</span></span>
> -   <span data-ttu-id="6c6d6-136">タスク ガイドが翻訳されている場合、そのタスク ガイドを開くと、タスク ガイドのすべてのテキストは選択した言語で表示されます。</span><span class="sxs-lookup"><span data-stu-id="6c6d6-136">If a task guide has been translated, when you open that task guide all the text of the task guide will appear in your selected language.</span></span>
> -   <span data-ttu-id="6c6d6-137">タスク ガイドが翻訳されていない場合、それを開くと、一部のテキスト (コントロールのテキスト) のみが選択した言語で表示されます。</span><span class="sxs-lookup"><span data-stu-id="6c6d6-137">If a task guide has not yet been translated, when you open it, only some of the text (the text of the controls) will appear in your selected language.</span></span>

## <a name="creating-custom-help"></a><span data-ttu-id="6c6d6-138">カスタム ヘルプの作成</span><span class="sxs-lookup"><span data-stu-id="6c6d6-138">Creating custom help</span></span>
<span data-ttu-id="6c6d6-139">実装を反映するタスク記録を作成して LCS 業務プロセス ライブラリに保存することで、Finance and Operations、および [Retail] へ向けてカスタム ヘルプを作成できます。</span><span class="sxs-lookup"><span data-stu-id="6c6d6-139">You can create custom help for Finance and Operations, and for Retail by creating task recordings that reflect your implementation, and saving them to an LCS Business Process Library.</span></span> <span data-ttu-id="6c6d6-140">[Talent] のカスタム タスク ガイドを作成することはできません。</span><span class="sxs-lookup"><span data-stu-id="6c6d6-140">You cannot create custom task guides for Talent.</span></span> 

<span data-ttu-id="6c6d6-141">パートナーの場合、ライブラリを会社のライブラリに昇格してソリューションに含める場合、顧客が使用できます。</span><span class="sxs-lookup"><span data-stu-id="6c6d6-141">For partners, if you promote a library to be a corporate library, and include it in a solution, it will be available to your customers.</span></span> <span data-ttu-id="6c6d6-142">APQC 統合グローバル ライブラリのコピーを作成して開き、タスクの記録を開いて変更し、変更がある記録を保存します。</span><span class="sxs-lookup"><span data-stu-id="6c6d6-142">You can also make a copy of the APQC Unified global library, and then open your copy, open task recordings from it, modify them, and save the recordings with your changes.</span></span> <span data-ttu-id="6c6d6-143">詳細については、「[ドキュメントやトレーニングとして使用するタスク記録の作成方法](../../dev-itpro/user-interface/task-recorder.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="6c6d6-143">For more information, see [How to create a task recording to use as documentation or training](../../dev-itpro/user-interface/task-recorder.md).</span></span>

<a name="see-also"></a><span data-ttu-id="6c6d6-144">参照</span><span class="sxs-lookup"><span data-stu-id="6c6d6-144">See also</span></span>
--------

[<span data-ttu-id="6c6d6-145">ヘルプ概要</span><span class="sxs-lookup"><span data-stu-id="6c6d6-145">Help overview</span></span>](help-overview.md)

[<span data-ttu-id="6c6d6-146">タスク レコーダーの概要</span><span class="sxs-lookup"><span data-stu-id="6c6d6-146">Task recorder overview</span></span>](../../dev-itpro/user-interface/task-recorder.md)

[<span data-ttu-id="6c6d6-147">ドキュメントやトレーニングとして使用するタスク記録の作成方法</span><span class="sxs-lookup"><span data-stu-id="6c6d6-147">How to create a task recording to use as documentation or training</span></span>](../../dev-itpro/user-interface/task-recorder-training-docs.md)





