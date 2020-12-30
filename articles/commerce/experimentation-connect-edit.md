---
title: 実験に接続しバリエーションを編集する
description: このトピックでは、サードパーティ サービスの実験を Dynamics 365 Commerce に接続する方法と実験のバリエーションを編集する方法について説明します。
author: sushma-rao
manager: AnnBe
ms.date: 10/21/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail
ms.author: sushmar
ms.search.validFrom: 2020-09-30
ms.dyn365.ops.version: AX 10.0.13
ms.openlocfilehash: 030640ba8907ae52c198ac96ad2c243b533d8c53
ms.sourcegitcommit: cd83f2bc0e52e13071ad306e07e4c255fc65cb03
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/22/2020
ms.locfileid: "4413893"
---
# <a name="connect-an-experiment-and-edit-variations"></a><span data-ttu-id="213bf-103">実験に接続しバリエーションを編集する</span><span class="sxs-lookup"><span data-stu-id="213bf-103">Connect an experiment and edit variations</span></span>

<span data-ttu-id="213bf-104">このトピックでは、Commerce の実験に接続して、仮説にに沿うようにバリエーションを変化させる方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="213bf-104">This topic describes how to connect your experiment in Commerce and make changes to your variations so that they align with your hypothesis.</span></span> 

<span data-ttu-id="213bf-105">次の図は、Dynamics 365 Commerce の電子商取引 web サイトでの実験の設定と実行に関連するすべての手順を示しています。</span><span class="sxs-lookup"><span data-stu-id="213bf-105">The following diagram shows all of the steps involved in setting up and running an experiment on an e-Commerce website in Dynamics 365 Commerce.</span></span> <span data-ttu-id="213bf-106">追加の手順については、個別のトピックで説明します。</span><span class="sxs-lookup"><span data-stu-id="213bf-106">Additional steps are covered in separate topics.</span></span>

<span data-ttu-id="213bf-107">[![実験ユーザー体験 - 接続と編集](./media/experimentation_connect_edit.svg) ](./media/experimentation_connect_edit.svg#lightbox)</span><span class="sxs-lookup"><span data-stu-id="213bf-107">[ ![Experimentation user journey - Connect & Edit](./media/experimentation_connect_edit.svg) ](./media/experimentation_connect_edit.svg#lightbox)</span></span>

<span data-ttu-id="213bf-108">サードパーティ サービスで[実験を設定](experimentation-setup.md) した後、Dynamics 365 Commerce で実験を接続し、実験バリエーションを編集します。</span><span class="sxs-lookup"><span data-stu-id="213bf-108">After you've [set up your experiment](experimentation-setup.md) in a third-party service, you'll connect the experiment in Dynamics 365 Commerce and edit the experiment variations.</span></span>

## <a name="planning-considerations"></a><span data-ttu-id="213bf-109">計画の考慮事項</span><span class="sxs-lookup"><span data-stu-id="213bf-109">Planning considerations</span></span>

<span data-ttu-id="213bf-110">コマースの実験を接続する前に、コンテンツのコマース管理方法に影響を与えるいくつかの決定を行う必要があります。</span><span class="sxs-lookup"><span data-stu-id="213bf-110">Before you connect your experiment in Commerce, you'll need to make some decisions that impact the way Commerce manages your content.</span></span>

### <a name="determine-the-scope-of-your-experiment"></a><span data-ttu-id="213bf-111">実験のスコープの決定</span><span class="sxs-lookup"><span data-stu-id="213bf-111">Determine the scope of your experiment</span></span>
<span data-ttu-id="213bf-112">実験を接続すると、実験のスコープを定義するように求めるメッセージが表示されます。</span><span class="sxs-lookup"><span data-stu-id="213bf-112">When you connect an experiment, you are prompted to define the scope of the experiment.</span></span> <span data-ttu-id="213bf-113">実験は、**部分** スコープまたは **全体** スコープとして定義されます。</span><span class="sxs-lookup"><span data-stu-id="213bf-113">Experiments are defined as **partial** scope or **entire** scope.</span></span>
- <span data-ttu-id="213bf-114">ページの特定の部分で実験を実行する場合は、**部分** を選択します。</span><span class="sxs-lookup"><span data-stu-id="213bf-114">Choose **partial** if you want to conduct an experiment on a specific portion of a page.</span></span> <span data-ttu-id="213bf-115">このオプションを選択した場合、実験に含まれるモジュールを識別する必要があります。</span><span class="sxs-lookup"><span data-stu-id="213bf-115">If you select this option, you must identify which modules are included in the experiment.</span></span> <span data-ttu-id="213bf-116">実験に関連していない既定のページまたはフラグメントの一部に加えられた変更は、バリエーション間で自動的に同期されます。</span><span class="sxs-lookup"><span data-stu-id="213bf-116">Changes that are made to parts of the default page or fragment that aren't related to the experiment are automatically synchronized across variations.</span></span>
- <span data-ttu-id="213bf-117">ページ全体またはフラグメント全体で実験を実行する場合は、**全体** を選択します。</span><span class="sxs-lookup"><span data-stu-id="213bf-117">Choose **entire** if you want to conduct an experiment on an entire page or fragment.</span></span> <span data-ttu-id="213bf-118">既定ページまたはフラグメントの個別のコピーが作成されます。</span><span class="sxs-lookup"><span data-stu-id="213bf-118">Separate copies of the default page or fragment are created.</span></span> <span data-ttu-id="213bf-119">編集領域全体を変更できるので、実験に含まれるモジュールを選択する必要はありません。</span><span class="sxs-lookup"><span data-stu-id="213bf-119">You won't have to select which modules are included in the experiment because the whole editing surface is available to change.</span></span> <span data-ttu-id="213bf-120">必要に応じて、モジュールの追加、削除、並び順の変更を行うことができます。</span><span class="sxs-lookup"><span data-stu-id="213bf-120">You can add, delete, or re-order modules as needed.</span></span> <span data-ttu-id="213bf-121">ただし、実験が関連付けられている既定のページまたはフラグメントに変更を加えた場合は、それらの変更をすべてのバリエーションに対して手動で同期する必要があります。</span><span class="sxs-lookup"><span data-stu-id="213bf-121">However, if any changes are made to the default page or fragment that the experiment is associated with, those changes have to be manually synchronized across all variations.</span></span>

<!-- not to editors, we're adding an image here to illustrate the difference. it will help.) -->

> [!NOTE]
> <span data-ttu-id="213bf-122">レイアウトを使用するページに実験を関連付ける場合は、実験の範囲を **全体** として限定できます。</span><span class="sxs-lookup"><span data-stu-id="213bf-122">If you associate your experiment with a page that uses a layout, you can only scope the experiment as **entire**.</span></span>

### <a name="decide-if-you-want-to-schedule-when-your-experiment-is-published"></a><span data-ttu-id="213bf-123">実験の発行時にスケジュール設定を行うかどうかの決定</span><span class="sxs-lookup"><span data-stu-id="213bf-123">Decide if you want to schedule when your experiment is published</span></span>
<span data-ttu-id="213bf-124">実験をライブ サイトに発行する際のスケジュールを設定する場合は、実験に接続する *前* に、実験に関連付けるコンテンツを発行グループで使用できることを確認してください。</span><span class="sxs-lookup"><span data-stu-id="213bf-124">If you want to schedule when your experiment is published to your live site, make sure the content you want to associate with the experiment is available in a publish group *before* you connect the experiment.</span></span> 

<span data-ttu-id="213bf-125">公開グループの更なる詳細については、[公開グループの使用](publish-groups.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="213bf-125">For more information about publish groups, refer to [Work with publish groups](publish-groups.md).</span></span>


## <a name="connect-your-experiment"></a><span data-ttu-id="213bf-126">実験の接続</span><span class="sxs-lookup"><span data-stu-id="213bf-126">Connect your experiment</span></span>
<span data-ttu-id="213bf-127">実験を接続するには、**実験の接続** ウィザードを起動します。</span><span class="sxs-lookup"><span data-stu-id="213bf-127">To connect your experiment, you'll launch the **Connect experiment** wizard.</span></span> <span data-ttu-id="213bf-128">ウィザードでは、実験に接続するために必要な手順を実行できます。</span><span class="sxs-lookup"><span data-stu-id="213bf-128">The wizard walks you through the steps required to connect your experiment.</span></span> <span data-ttu-id="213bf-129">ウィザードを完了すると、実験が関連付けられ、バリエーションを作成および編集する準備ができます。</span><span class="sxs-lookup"><span data-stu-id="213bf-129">When you complete the wizard, your experiment is connected and variations are created and ready to be edited.</span></span>

<span data-ttu-id="213bf-130">Commerce サイト ビルダーでの実験の接続を開始するには、以下の手順に従ってください。</span><span class="sxs-lookup"><span data-stu-id="213bf-130">To get started connecting your experiment in Commerce site builder, follow these steps.</span></span>

1. <span data-ttu-id="213bf-131">**実験の接続** ウィザードを起動するには、左側のナビゲーションウィンドウで **実験** を選択し、**接続** を選択します。</span><span class="sxs-lookup"><span data-stu-id="213bf-131">To launch the **Connect experiment** wizard, select **Experiments** in the left navigation pane, and then select **Connect**.</span></span> <span data-ttu-id="213bf-132">別の方法として、ページやフラグメント エディターからウィザードにアクセスするには、このウィザードを編集し、コマンドバーの **実験に接続する** を選択します。</span><span class="sxs-lookup"><span data-stu-id="213bf-132">Alternatively, you can access the wizard from a page or fragment editor by editing it and selecting **Connect experiment** on the command bar.</span></span>

    > [!NOTE]
    > <span data-ttu-id="213bf-133">ページは、一度に 1 つの実験にのみ関連付けることができます。</span><span class="sxs-lookup"><span data-stu-id="213bf-133">A page can only be connected to one experiment at a time.</span></span> <span data-ttu-id="213bf-134">ページを異なる実験に関連付けるには、最初にページが現在接続されている実験を削除します。</span><span class="sxs-lookup"><span data-stu-id="213bf-134">To connect a page to a different experiment, first delete the experiment that the page is currently connected to.</span></span>

1. <span data-ttu-id="213bf-135">実験を実行するページまたはフラグメントを選択します。</span><span class="sxs-lookup"><span data-stu-id="213bf-135">Choose the page or fragment you want to run your experiment on.</span></span>
1. <span data-ttu-id="213bf-136">上記の [実験のスコープを決定](#determine-the-scope-of-your-experiment) セクションで行った選択に基づき、実験スコープを **部分** または **全体** に設定します。</span><span class="sxs-lookup"><span data-stu-id="213bf-136">Set the experimentation scope to **partial** or **entire**, based on the choice you made in the [Determine the scope of your experiment](#determine-the-scope-of-your-experiment) section above.</span></span>
    > [!NOTE]
    > <span data-ttu-id="213bf-137">全ページまたはフラグメントで実験する場合、**ページまたはフラグメントの実験** 機能フラグを有効にする必要があります。</span><span class="sxs-lookup"><span data-stu-id="213bf-137">The **Experiment on pages or fragments** feature flag must be enabled if you want to experiment on a full page or fragment.</span></span> <span data-ttu-id="213bf-138">詳細については、[Dynamics 365 Commerce の実験](experimentation-overview.md) トピックを参照してください。</span><span class="sxs-lookup"><span data-stu-id="213bf-138">Refer to the [Experimentation in Dynamics 365 Commerce](experimentation-overview.md) topic for more information.</span></span>
    
1. <span data-ttu-id="213bf-139">ウィザードの最終手順で、**バリエーションの生成およびウィザードの終了** を選択します。</span><span class="sxs-lookup"><span data-stu-id="213bf-139">In the final step of the wizard, select **Generate variations and exit wizard**.</span></span> <span data-ttu-id="213bf-140">実験に対してバリエーションが作成されます。</span><span class="sxs-lookup"><span data-stu-id="213bf-140">Variations are created for the experiment.</span></span> 

## <a name="edit-your-variations"></a><span data-ttu-id="213bf-141">バリエーションの編集</span><span class="sxs-lookup"><span data-stu-id="213bf-141">Edit your variations</span></span>
<span data-ttu-id="213bf-142">ウィザードを終了すると、バリエーションが作成されます。</span><span class="sxs-lookup"><span data-stu-id="213bf-142">When you exit the wizard, variations are created for you.</span></span> 

<span data-ttu-id="213bf-143">次に、実験仮説で検証の必要がある選択を反映するようにバリエーションを編集します。</span><span class="sxs-lookup"><span data-stu-id="213bf-143">Next, you'll edit the variations so they reflect the choices that you need to verify in the experiment hypothesis.</span></span> <span data-ttu-id="213bf-144">上記[実験スコープを決定](#determine-the-scope-of-your-experiment) セクションで、実験に対して選択したスコープに対応する次の手順のいずれかを選択します。</span><span class="sxs-lookup"><span data-stu-id="213bf-144">Choose one of following procedures that corresponds to the scope you chose for your experiment in the [Determine the scope of your experiment](#determine-the-scope-of-your-experiment) section above.</span></span>

### <a name="edit-variations-for-experiments-with-partial-scope"></a><span data-ttu-id="213bf-145">部分的スコープの実験バリエーションの編集</span><span class="sxs-lookup"><span data-stu-id="213bf-145">Edit variations for experiments with partial scope</span></span>
<span data-ttu-id="213bf-146">**実験を接続** ウィザードの **部分** として実験のスコープを決定する場合は、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="213bf-146">Follow these steps if you defined the scope of your experiment as **partial** in the **Connect experiment** wizard.</span></span>

1. <span data-ttu-id="213bf-147">編集ビューでは、コマンド バーの下にあるバリエーション ドロップダウン メニューを使用して、元の仮説に基づき各バリエーションを編集します。</span><span class="sxs-lookup"><span data-stu-id="213bf-147">In editor view, use the variations drop-down menu below the command bar to edit each variation based on your original hypothesis.</span></span> <span data-ttu-id="213bf-148">バリエーションのいずれかを変更しないで、コントロールまたは基本バリエーションを設定することもできます。</span><span class="sxs-lookup"><span data-stu-id="213bf-148">You may also want to establish a control or base variation by leaving one of the variations unchanged.</span></span>
1. <span data-ttu-id="213bf-149">実験したモジュールを選び、省略記号 (...) から **実験に追加** の順に選択します。</span><span class="sxs-lookup"><span data-stu-id="213bf-149">Select the module to be experimented on, select the ellipsis (...), and then select **Add to experiment**.</span></span>

### <a name="edit-variations-for-experiments-with-entire-scope"></a><span data-ttu-id="213bf-150">全体スコープの実験バリエーションの編集</span><span class="sxs-lookup"><span data-stu-id="213bf-150">Edit variations for experiments with entire scope</span></span>
<span data-ttu-id="213bf-151">編集ビューで、**実験の接続** の **全体** となる実験のスコープを決定したら、コマンドバーの下にあるバリエーション ドロップダウン メニューを使用して、元の仮説に基づき各バリエーションを編集します。</span><span class="sxs-lookup"><span data-stu-id="213bf-151">If you defined the scope of your experiment as **entire** in the **Connect experiment** wizard, while in editor view, use the variations drop-down menu below the command bar to edit each variation based on your original hypothesis.</span></span> 

> [!NOTE]
> <span data-ttu-id="213bf-152">どちらの場合でも、バリエーションのいずれかを変更しないで、コントロールまたは基本バリエーションを設定することもできます。</span><span class="sxs-lookup"><span data-stu-id="213bf-152">In either case, you may also want to establish a control or base variation by leaving one of the variations unchanged.</span></span>

## <a name="previous-step"></a><span data-ttu-id="213bf-153">前のステップ</span><span class="sxs-lookup"><span data-stu-id="213bf-153">Previous step</span></span>
[<span data-ttu-id="213bf-154">実験の設定</span><span class="sxs-lookup"><span data-stu-id="213bf-154">Set up an experiment</span></span>](experimentation-setup.md) 


## <a name="next-step"></a><span data-ttu-id="213bf-155">次のステップ</span><span class="sxs-lookup"><span data-stu-id="213bf-155">Next step</span></span>
[<span data-ttu-id="213bf-156">実験のプレビューと公開</span><span class="sxs-lookup"><span data-stu-id="213bf-156">Preview and publish an experiment</span></span>](experimentation-preview-publish.md)
