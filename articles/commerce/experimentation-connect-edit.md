---
title: 実験に接続しバリエーションを編集する
description: このトピックでは、サードパーティ サービスの実験を Dynamics 365 Commerce に接続する方法と実験のバリエーションを編集する方法について説明します。
author: sushma-rao
manager: AnnBe
ms.date: 10/01/2020
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
ms.openlocfilehash: ea1da0a7dc90b7197f3ee532bccc55d2ddbe4ddd
ms.sourcegitcommit: b6ab46f6e5ce60e2c3d70a348827eaf60c84cae2
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/01/2020
ms.locfileid: "3930238"
---
# <a name="connect-an-experiment-and-edit-variations"></a><span data-ttu-id="dd827-103">実験に接続しバリエーションを編集する</span><span class="sxs-lookup"><span data-stu-id="dd827-103">Connect an experiment and edit variations</span></span>

<span data-ttu-id="dd827-104">このトピックでは、コマースの実験に接続して、仮説に合わせるためにバリエーションを変更する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="dd827-104">This topic describes how to connect your experiment in Commerce and make changes to your variations so they align with your hypothesis.</span></span> <span data-ttu-id="dd827-105">次の図は、Dynamics 365 Commerce の電子商取引 web サイトでの実験の設定と実行に関連するすべての手順を示しています。</span><span class="sxs-lookup"><span data-stu-id="dd827-105">The following diagram shows all of the steps involved in setting up and running an experiment on an e-Commerce website in Dynamics 365 Commerce.</span></span> <span data-ttu-id="dd827-106">追加の手順については、個別のトピックで説明します。</span><span class="sxs-lookup"><span data-stu-id="dd827-106">Additional steps are covered in separate topics.</span></span>

<span data-ttu-id="dd827-107">[![実験ユーザー体験 - 接続と編集](./media/experimentation_connect_edit.svg) ](./media/experimentation_connect_edit.svg#lightbox)</span><span class="sxs-lookup"><span data-stu-id="dd827-107">[ ![Experimentation user journey - Connect & Edit](./media/experimentation_connect_edit.svg) ](./media/experimentation_connect_edit.svg#lightbox)</span></span>

<span data-ttu-id="dd827-108">サードパーティ サービスで[実験を設定](experimentation-setup.md) した後、Dynamics 365 Commerce で実験を接続し、実験バリエーションを編集します。</span><span class="sxs-lookup"><span data-stu-id="dd827-108">After you've [set up your experiment](experimentation-setup.md) in a third-party service, you'll connect the experiment in Dynamics 365 Commerce and edit the experiment variations.</span></span>

## <a name="planning-considerations"></a><span data-ttu-id="dd827-109">計画の考慮事項</span><span class="sxs-lookup"><span data-stu-id="dd827-109">Planning considerations</span></span>

<span data-ttu-id="dd827-110">コマースの実験を接続する前に、コンテンツのコマース管理方法に影響を与えるいくつかの決定を行う必要があります。</span><span class="sxs-lookup"><span data-stu-id="dd827-110">Before you connect your experiment in Commerce, you'll need to make some decisions that impact the way Commerce manages your content.</span></span>

### <a name="determine-the-scope-of-your-experiment"></a><span data-ttu-id="dd827-111">実験のスコープの決定</span><span class="sxs-lookup"><span data-stu-id="dd827-111">Determine the scope of your experiment</span></span>
<span data-ttu-id="dd827-112">実験を接続すると、実験のスコープを定義するように求めるメッセージが表示されます。</span><span class="sxs-lookup"><span data-stu-id="dd827-112">When you connect an experiment, you are prompted to define the scope of the experiment.</span></span> <span data-ttu-id="dd827-113">実験は、**部分**スコープまたは**全体**スコープとして定義されます。</span><span class="sxs-lookup"><span data-stu-id="dd827-113">Experiments are defined as **partial** scope or **entire** scope.</span></span>
- <span data-ttu-id="dd827-114">ページの特定の部分で実験を実行する場合は、**部分**を選択します。</span><span class="sxs-lookup"><span data-stu-id="dd827-114">Choose **partial** if you want to conduct an experiment on a specific portion of a page.</span></span> <span data-ttu-id="dd827-115">このオプションを選択した場合、実験に含まれるモジュールを識別する必要があります。</span><span class="sxs-lookup"><span data-stu-id="dd827-115">If you select this option, you must identify which modules are included in the experiment.</span></span> <span data-ttu-id="dd827-116">実験に関連していない既定のページまたはフラグメントの一部に加えられた変更は、バリエーション間で自動的に同期されます。</span><span class="sxs-lookup"><span data-stu-id="dd827-116">Changes that are made to parts of the default page or fragment that aren't related to the experiment are automatically synchronized across variations.</span></span>
- <span data-ttu-id="dd827-117">ページ全体またはフラグメント全体で実験を実行する場合は、**全体**を選択します。</span><span class="sxs-lookup"><span data-stu-id="dd827-117">Choose **entire** if you want to conduct an experiment on an entire page or fragment.</span></span> <span data-ttu-id="dd827-118">既定ページまたはフラグメントの個別のコピーが作成されます。</span><span class="sxs-lookup"><span data-stu-id="dd827-118">Separate copies of the default page or fragment are created.</span></span> <span data-ttu-id="dd827-119">編集領域全体を変更できるので、実験に含まれるモジュールを選択する必要はありません。</span><span class="sxs-lookup"><span data-stu-id="dd827-119">You won't have to select which modules are included in the experiment because the whole editing surface is available to change.</span></span> <span data-ttu-id="dd827-120">必要に応じて、モジュールの追加、削除、および順序の変更を行うことができます。</span><span class="sxs-lookup"><span data-stu-id="dd827-120">You can add, delete, and re-order modules as needed.</span></span> <span data-ttu-id="dd827-121">ただし、実験が関連付けられている既定のページまたはフラグメントに変更を加えた場合は、それらの変更をすべてのバリエーションに対して手動で同期する必要があります。</span><span class="sxs-lookup"><span data-stu-id="dd827-121">However, if any changes are made to the default page or fragment that the experiment is associated with, those changes have to be manually synchronized across all variations.</span></span>

<!-- not to editors, we're adding an image here to illustrate the difference. it will help.) -->

> [!NOTE]
> <span data-ttu-id="dd827-122">レイアウトを使用するページに実験を関連付ける場合は、実験の範囲を**全体**として限定できます。</span><span class="sxs-lookup"><span data-stu-id="dd827-122">If you associate your experiment with a page that uses a layout, you can only scope the experiment as **entire**.</span></span>

### <a name="decide-if-you-want-to-schedule-when-your-experiment-is-published"></a><span data-ttu-id="dd827-123">実験の発行時にスケジュール設定を行うかどうかの決定</span><span class="sxs-lookup"><span data-stu-id="dd827-123">Decide if you want to schedule when your experiment is published</span></span>
<span data-ttu-id="dd827-124">実験をライブ サイトに発行する際のスケジュールを設定する場合は、実験に接続する*前*に、実験に関連付けるコンテンツを発行グループで使用できることを確認してください。</span><span class="sxs-lookup"><span data-stu-id="dd827-124">If you want to schedule when your experiment is published to your live site, make sure the content you want to associate with the experiment is available in a publish group *before* you connect the experiment.</span></span> 

<span data-ttu-id="dd827-125">公開グループの更なる詳細については、[公開グループの使用](publish-groups.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="dd827-125">For more information about publish groups, refer to [Work with publish groups](publish-groups.md).</span></span>


## <a name="connect-your-experiment"></a><span data-ttu-id="dd827-126">実験の接続</span><span class="sxs-lookup"><span data-stu-id="dd827-126">Connect your experiment</span></span>
<span data-ttu-id="dd827-127">実験を接続するには、**実験の接続**ウィザードを起動します。</span><span class="sxs-lookup"><span data-stu-id="dd827-127">To connect your experiment, you'll launch the **Connect experiment** wizard.</span></span> <span data-ttu-id="dd827-128">ウィザードでは、実験に接続するために必要な手順を実行できます。</span><span class="sxs-lookup"><span data-stu-id="dd827-128">The wizard walks you through the steps required to connect your experiment.</span></span> <span data-ttu-id="dd827-129">ウィザードを完了すると、実験が関連付けられ、バリエーションを作成および編集する準備ができます。</span><span class="sxs-lookup"><span data-stu-id="dd827-129">When you complete the wizard, your experiment is connected and variations are created and ready to be edited.</span></span>

1. <span data-ttu-id="dd827-130">ウィザードを起動するには、サイト ビルダーの**実験**タブを選び、**接続**を選択します。</span><span class="sxs-lookup"><span data-stu-id="dd827-130">To launch the wizard, select the **Experiments** tab in site builder and then select **Connect**.</span></span> <span data-ttu-id="dd827-131">別の方法として、ページまたはフラグメント エディターからウィザードにアクセスすることもできます。</span><span class="sxs-lookup"><span data-stu-id="dd827-131">Alternatively, the wizard can be accessed from a page or fragment editor.</span></span> <span data-ttu-id="dd827-132">編集モードで、コマンドバーの**実験の接続**を選択します。</span><span class="sxs-lookup"><span data-stu-id="dd827-132">In edit mode, select **Connect experiment** in the command bar.</span></span>

> [!NOTE]
> <span data-ttu-id="dd827-133">ページは、一度に 1 つの実験にのみ関連付けることができます。</span><span class="sxs-lookup"><span data-stu-id="dd827-133">A page can only be connected to one experiment at a time.</span></span> <span data-ttu-id="dd827-134">ページを異なる実験に関連付けるには、最初にページが現在接続されている実験を削除します。</span><span class="sxs-lookup"><span data-stu-id="dd827-134">To connect a page to a different experiment, first delete the experiment that the page is currently connected to.</span></span>

1. <span data-ttu-id="dd827-135">実験を実行するページまたはフラグメントを選択します。</span><span class="sxs-lookup"><span data-stu-id="dd827-135">Choose the page or fragment you want to run your experiment on.</span></span>
1. <span data-ttu-id="dd827-136">上記の[実験のスコープを決定](#determine-the-scope-of-your-experiment) セクションで行った選択に基づき、実験スコープを**部分**または**全体**に設定します。</span><span class="sxs-lookup"><span data-stu-id="dd827-136">Set the experimentation scope to **partial** or **entire**, based on the choice you made in the [Determine the scope of your experiment](#determine-the-scope-of-your-experiment) section above.</span></span>
    > [!NOTE]
    > <span data-ttu-id="dd827-137">全ページまたはフラグメントで実験する場合、**ページまたはフラグメントの実験**機能フラグを有効にする必要があります。</span><span class="sxs-lookup"><span data-stu-id="dd827-137">The **Experiment on pages or fragments** feature flag must be enabled if you want to experiment on a full page or fragment.</span></span> <span data-ttu-id="dd827-138">詳細については、[Dynamics 365 Commerce の実験](experimentation-overview.md) トピックを参照してください。</span><span class="sxs-lookup"><span data-stu-id="dd827-138">Refer to the [Experimentation in Dynamics 365 Commerce](experimentation-overview.md) topic for more information.</span></span>
    
1. <span data-ttu-id="dd827-139">ウィザードの最終手順で、**バリエーションの生成およびウィザードの終了**を選択します。</span><span class="sxs-lookup"><span data-stu-id="dd827-139">In the final step of the wizard, select **Generate variations and exit wizard**.</span></span> <span data-ttu-id="dd827-140">実験に対してバリエーションが作成されます。</span><span class="sxs-lookup"><span data-stu-id="dd827-140">Variations are created for the experiment.</span></span> 

## <a name="edit-your-variations"></a><span data-ttu-id="dd827-141">バリエーションの編集</span><span class="sxs-lookup"><span data-stu-id="dd827-141">Edit your variations</span></span>
<span data-ttu-id="dd827-142">ウィザードを終了すると、バリエーションが作成されます。</span><span class="sxs-lookup"><span data-stu-id="dd827-142">When you exit the wizard, variations are created for you.</span></span> 

<span data-ttu-id="dd827-143">次に、実験仮説で検証の必要がある選択を反映するようにバリエーションを編集します。</span><span class="sxs-lookup"><span data-stu-id="dd827-143">Next, you'll edit the variations so they reflect the choices that you need to verify in the experiment hypothesis.</span></span> <span data-ttu-id="dd827-144">上記[実験スコープを決定](#determine-the-scope-of-your-experiment) セクションで、実験に対して選択したスコープに対応する次の手順のいずれかを選択します。</span><span class="sxs-lookup"><span data-stu-id="dd827-144">Choose one of following procedures that corresponds to the scope you chose for your experiment in the [Determine the scope of your experiment](#determine-the-scope-of-your-experiment) section above.</span></span>

### <a name="edit-variations-for-experiments-with-partial-scope"></a><span data-ttu-id="dd827-145">部分的スコープの実験バリエーションの編集</span><span class="sxs-lookup"><span data-stu-id="dd827-145">Edit variations for experiments with partial scope</span></span>
<span data-ttu-id="dd827-146">**実験を接続**ウィザードの**部分**として実験のスコープを決定する場合は、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="dd827-146">Follow these steps if you defined the scope of your experiment as **partial** in the **Connect experiment** wizard.</span></span>

1. <span data-ttu-id="dd827-147">編集ビューでは、コマンド バーの下にあるバリエーション ドロップダウン メニューを使用して、元の仮説に基づき各バリエーションを編集します。</span><span class="sxs-lookup"><span data-stu-id="dd827-147">In editor view, use the variations drop-down menu below the command bar to edit each variation based on your original hypothesis.</span></span> <span data-ttu-id="dd827-148">バリエーションのいずれかを変更しないで、コントロールまたは基本バリエーションを設定することもできます。</span><span class="sxs-lookup"><span data-stu-id="dd827-148">You may also want to establish a control or base variation by leaving one of the variations unchanged.</span></span>
1. <span data-ttu-id="dd827-149">実験したモジュールを選び、省略記号 (...) から**実験に追加**の順に選択します。</span><span class="sxs-lookup"><span data-stu-id="dd827-149">Select the module to be experimented on, select the ellipsis (...), and then select **Add to experiment**.</span></span>

### <a name="edit-variations-for-experiments-with-entire-scope"></a><span data-ttu-id="dd827-150">全体スコープの実験バリエーションの編集</span><span class="sxs-lookup"><span data-stu-id="dd827-150">Edit variations for experiments with entire scope</span></span>
<span data-ttu-id="dd827-151">編集ビューで、**実験の接続**の**全体**となる実験のスコープを決定したら、コマンドバーの下にあるバリエーション ドロップダウン メニューを使用して、元の仮説に基づき各バリエーションを編集します。</span><span class="sxs-lookup"><span data-stu-id="dd827-151">If you defined the scope of your experiment as **entire** in the **Connect experiment** wizard, while in editor view, use the variations drop-down menu below the command bar to edit each variation based on your original hypothesis.</span></span> 

> [!NOTE]
> <span data-ttu-id="dd827-152">どちらの場合でも、バリエーションのいずれかを変更しないで、コントロールまたは基本バリエーションを設定することもできます。</span><span class="sxs-lookup"><span data-stu-id="dd827-152">In either case, you may also want to establish a control or base variation by leaving one of the variations unchanged.</span></span>

## <a name="previous-step"></a><span data-ttu-id="dd827-153">前のステップ</span><span class="sxs-lookup"><span data-stu-id="dd827-153">Previous step</span></span>
[<span data-ttu-id="dd827-154">実験の設定</span><span class="sxs-lookup"><span data-stu-id="dd827-154">Set up an experiment</span></span>](experimentation-setup.md) 


## <a name="next-step"></a><span data-ttu-id="dd827-155">次のステップ</span><span class="sxs-lookup"><span data-stu-id="dd827-155">Next step</span></span>
[<span data-ttu-id="dd827-156">実験のプレビューと公開</span><span class="sxs-lookup"><span data-stu-id="dd827-156">Preview and publish an experiment</span></span>](experimentation-preview-publish.md)
