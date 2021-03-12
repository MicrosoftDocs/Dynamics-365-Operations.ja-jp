---
title: フラグメントで動作
description: このトピックでは、Microsoft Dynamics 365 Commerce でフラグメントを使用する理由、時期、および方法について説明します。
author: phinneyridge
manager: annbe
ms.date: 10/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.region: Global
ms.search.industry: retail
ms.author: stuharg
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 8436fd3621e94fb761c076454423fe9842306c78
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/15/2021
ms.locfileid: "4982241"
---
# <a name="work-with-fragments"></a><span data-ttu-id="de76e-103">フラグメントで動作</span><span class="sxs-lookup"><span data-stu-id="de76e-103">Work with fragments</span></span> 

[!include [banner](includes/banner.md)]

<span data-ttu-id="de76e-104">このトピックでは、Microsoft Dynamics 365 Commerce でフラグメントを使用する理由、時期、および方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="de76e-104">This topic describes why, when, and how to use fragments in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="de76e-105">概要</span><span class="sxs-lookup"><span data-stu-id="de76e-105">Overview</span></span>

<span data-ttu-id="de76e-106">フラグメントを使用すると、サイト全体で再利用する必要があるモジュール コンフィギュレーションに対して、一元的な作成エクスペリエンスを実行できます。</span><span class="sxs-lookup"><span data-stu-id="de76e-106">Fragments allow for a centralized authoring experience for module configurations that must be reused throughout your site.</span></span> <span data-ttu-id="de76e-107">たとえば、ヘッダー、フッター、およびバナーは多くのページに渡って共有されるため、フラグメントとしてコンフィギュレーションされることがよくあります。</span><span class="sxs-lookup"><span data-stu-id="de76e-107">For example, headers, footers, and banners are often configured as fragments, because they are shared across many pages.</span></span> <span data-ttu-id="de76e-108">サイトの別のページに挿入することができる小さな Web ページとして、フラグメントを考えることができます。</span><span class="sxs-lookup"><span data-stu-id="de76e-108">You can think of fragments as miniature webpages that can be inserted into other pages on your site.</span></span> <span data-ttu-id="de76e-109">フラグメントには独自のライフサイクルがあります。</span><span class="sxs-lookup"><span data-stu-id="de76e-109">Fragments have their own lifecycle.</span></span> <span data-ttu-id="de76e-110">つまり、作成ツールでは、独立したエンティティとして作成、参照、更新、削除されるということです。</span><span class="sxs-lookup"><span data-stu-id="de76e-110">In other words, they are created, referenced, updated, and deleted as independent entities in the authoring tools.</span></span>

<span data-ttu-id="de76e-111">フラグメントをコンフィギュレーションした後は、サイト構造でモジュールを使用できる場所ではどこでも使用できます。</span><span class="sxs-lookup"><span data-stu-id="de76e-111">After fragments are configured, they can be used wherever modules can be used in your site structure.</span></span> <span data-ttu-id="de76e-112">フラグメントは、ページ、レイアウト、テンプレート、およびその他のフラグメントで参照できます。</span><span class="sxs-lookup"><span data-stu-id="de76e-112">Fragments can be referenced on pages, in layouts, in templates, and in other fragments.</span></span>

> [!NOTE]
> <span data-ttu-id="de76e-113">フラグメントは、他のフラグメント内の 7 つの階層にまで入れ子にすることができます。</span><span class="sxs-lookup"><span data-stu-id="de76e-113">Fragments can be nested up to seven levels deep inside other fragments.</span></span>

<span data-ttu-id="de76e-114">たとえば、季節のイベントをサイト内の多数のページで推進したい場合に、フラグメントを使用できます。</span><span class="sxs-lookup"><span data-stu-id="de76e-114">For example, if you want to promote a seasonal event cross many pages on our site, you can use a fragment.</span></span> <span data-ttu-id="de76e-115">新しいフラグメントを作成するプロセスの最初のステップとして、開始するモジュールのタイプを選択します。</span><span class="sxs-lookup"><span data-stu-id="de76e-115">The first step in the process of creating a new fragment is to select the type of module that you want to start from.</span></span> <span data-ttu-id="de76e-116">この例では、ヒーロー モジュールからフラグメントを作成できます。</span><span class="sxs-lookup"><span data-stu-id="de76e-116">For this example, you can build the fragment from a hero module.</span></span>

> [!NOTE]
> <span data-ttu-id="de76e-117">フラグメントは、どのモジュール タイプからでも作成できます。</span><span class="sxs-lookup"><span data-stu-id="de76e-117">Fragments can be built from any module type.</span></span>

<span data-ttu-id="de76e-118">その後、特定の販促コンテンツで、ヒーロー フラグメントをコンフィギュレーションすることができます。</span><span class="sxs-lookup"><span data-stu-id="de76e-118">You can then configure the hero fragment with your specific promotional content.</span></span> <span data-ttu-id="de76e-119">必要に応じてローカライズすることもできます。</span><span class="sxs-lookup"><span data-stu-id="de76e-119">You can also localize it as you require.</span></span> <span data-ttu-id="de76e-120">新しいスタンドアロンのヒーローのフラグメントを、サイト全体で事前にコンフィギュレーションされたモジュールとして使用できます。</span><span class="sxs-lookup"><span data-stu-id="de76e-120">The new stand-alone hero fragment can then be consumed as a preconfigured module throughout your site.</span></span> <span data-ttu-id="de76e-121">これは、テンプレート、特定のページ、またはヒーロー モジュールを含むことができるその他のフラグメントに、簡単に追加できます。</span><span class="sxs-lookup"><span data-stu-id="de76e-121">You can easily add it to templates, to specific pages, or to other fragments that can contain hero modules.</span></span>

<span data-ttu-id="de76e-122">フラグメントが追加された場所はすべて、作成したセントラル ヒーロー フラグメントへの参照です。</span><span class="sxs-lookup"><span data-stu-id="de76e-122">All the places where the fragment is added are references to the central hero fragment that you created.</span></span> <span data-ttu-id="de76e-123">フラグメントに変更を発行した場合、その変更は、サイト全体でそのフラグメントが参照されているすべての場所にすぐに反映されます。</span><span class="sxs-lookup"><span data-stu-id="de76e-123">If you publish changes to the fragment, those changes are immediately reflected in all the places where the fragment is referenced across the site.</span></span> <span data-ttu-id="de76e-124">したがって、フラグメントは、サイトのモジュール コンフィギュレーションを再利用して一元管理するための、強力かつ効率的な方法です。</span><span class="sxs-lookup"><span data-stu-id="de76e-124">Therefore, fragments provide a powerful and efficient way to reuse and centrally manage module configurations on a site.</span></span> <span data-ttu-id="de76e-125">これらを効果的に使用することにより、機敏性を大幅に向上させ、サイトのコンテンツ管理に関連するコストを削減することができます。</span><span class="sxs-lookup"><span data-stu-id="de76e-125">By effectively using them, you can significantly increase agility and help reduce the cost that is associated with managing site content.</span></span>

<span data-ttu-id="de76e-126">次の図は、フラグメントを使用して、E コマース サイト全体で共有しているモジュールのコンフィギュレーションを一元的に作成する方法を示しています。</span><span class="sxs-lookup"><span data-stu-id="de76e-126">The following illustration shows how fragments can be used to centralize authoring of shared module configurations across an e-Commerce site.</span></span>

![フラグメントを使用して、E コマース サイト全体で共有しているモジュールのコンフィギュレーションを一元的に作成する方法を示した図](./media/fragment-figure1.png)

## <a name="create-a-fragment"></a><span data-ttu-id="de76e-128">フラグメントの作成</span><span class="sxs-lookup"><span data-stu-id="de76e-128">Create a fragment</span></span>

<span data-ttu-id="de76e-129">新しいフラグメントを作成するか、既存のモジュール コンフィギュレーションをフラグメントとして保存することができます。</span><span class="sxs-lookup"><span data-stu-id="de76e-129">You can either create a new fragment or save an existing module configuration as a fragment.</span></span>

### <a name="save-an-existing-module-configuration-as-a-fragment"></a><span data-ttu-id="de76e-130">フラグメントとして既存のモジュール コンフィギュレーションを保存</span><span class="sxs-lookup"><span data-stu-id="de76e-130">Save an existing module configuration as a fragment</span></span>

<span data-ttu-id="de76e-131">以前にコンフィギュレーションしたモジュールを、Commerce サイトビルダーで再利用可能なフラグメントに変換するには、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="de76e-131">To convert a previously configured module to a reusable fragment in Commerce site builder, follow these steps.</span></span>

1. <span data-ttu-id="de76e-132">フラグメントに変換するモジュールを含むページまたはテンプレートを開きます。</span><span class="sxs-lookup"><span data-stu-id="de76e-132">Open a page or template that contains the module that you want to convert to a fragment.</span></span>
1. <span data-ttu-id="de76e-133">左のアウトライン ウィンドウで、またはビジュアル ページ ビルダーで直接、以前に構成したモジュールを選択します。</span><span class="sxs-lookup"><span data-stu-id="de76e-133">In the outline pane on the left or directly in visual page builder, select the previously configured module.</span></span>
1. <span data-ttu-id="de76e-134">アウトライン ウィンドウ、またはビジュアル ページ ビルダーで選択したモジュールのツールバーで、モジュールの名前の横にある省略記号 (**...**) を選択します。</span><span class="sxs-lookup"><span data-stu-id="de76e-134">Select the ellipsis (**...**) next to the name of the module in either the outline pane or the selected module's toolbar in visual page builder.</span></span> 
1. <span data-ttu-id="de76e-135">**フラグメントとして共有** を選択します。</span><span class="sxs-lookup"><span data-stu-id="de76e-135">Select **Share as fragment**.</span></span> 
1. <span data-ttu-id="de76e-136">**フラグメントとして保存** ダイアログ ボックスで、フラグメントの名前を入力します。</span><span class="sxs-lookup"><span data-stu-id="de76e-136">In the **Save as fragment** dialog box, enter a name for the fragment.</span></span>
1. <span data-ttu-id="de76e-137">**OK** を選択すると、他のページに追加できるフラグメントとしてモジュール コンフィギュレーションが保存されます。</span><span class="sxs-lookup"><span data-stu-id="de76e-137">Select **OK** to save the module configuration as a fragment that can be added to other pages.</span></span>
<!-- The following image shows how to save a module configuration as a fragment.-->
<!--![A screen capture of how to save a module configuration as a fragment](./media/save-as-fragment.png)-->

### <a name="create-a-new-fragment"></a><span data-ttu-id="de76e-138">新しいフラグメントの作成</span><span class="sxs-lookup"><span data-stu-id="de76e-138">Create a new fragment</span></span>

<span data-ttu-id="de76e-139">Commerce サイト ビルダーで新規フラグメントを作成するには、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="de76e-139">To create a new fragment in Commerce site builder, follow these steps.</span></span>

1. <span data-ttu-id="de76e-140">左のナビゲーション ウィンドウで、**フラグメント** を選択します。</span><span class="sxs-lookup"><span data-stu-id="de76e-140">In the navigation pane on the left, select **Fragments**.</span></span>
1. <span data-ttu-id="de76e-141">**新規** を選択します。</span><span class="sxs-lookup"><span data-stu-id="de76e-141">Select **New**.</span></span> <span data-ttu-id="de76e-142">使用可能なすべてのモジュール タイプを示す **新規フラグメント** ダイアログ ボックスが表示されます。</span><span class="sxs-lookup"><span data-stu-id="de76e-142">A **New fragment** dialog box appears that shows all the available module types.</span></span> <span data-ttu-id="de76e-143">先に説明したように、どのモジュール タイプからでもフラグメントを作成できます。</span><span class="sxs-lookup"><span data-stu-id="de76e-143">As was mentioned earlier, fragments can be created from any module type.</span></span>
1. <span data-ttu-id="de76e-144">フラグメントのモジュール タイプを選択します。</span><span class="sxs-lookup"><span data-stu-id="de76e-144">Select a module type for your fragment.</span></span>

<!-- The following image shows where to create a new fragment.-->
<!-- ![A screen capture of where to create a new fragment](./media/fragment-nav-menu.png)-->
> [!TIP]
> <span data-ttu-id="de76e-145">汎用コンテナー モジュール タイプを選択することで、後でフラグメントを更新およびコンフィギュレーションする必要がある場合に、最大の柔軟性を得ることができます。</span><span class="sxs-lookup"><span data-stu-id="de76e-145">By selecting a generic container module type, you get the most flexibility when you need to update and configure your fragment later.</span></span>

## <a name="add-remove-or-edit-fragments-on-a-page"></a><span data-ttu-id="de76e-146">ページでのフラグメントの追加、削除、または編集</span><span class="sxs-lookup"><span data-stu-id="de76e-146">Add, remove, or edit fragments on a page</span></span>

<span data-ttu-id="de76e-147">次の手順では、フラグメントを追加、削除、および編集する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="de76e-147">The following procedures describe how to add, remove, and edit fragments.</span></span>

### <a name="add-a-fragment"></a><span data-ttu-id="de76e-148">フラグメントの追加</span><span class="sxs-lookup"><span data-stu-id="de76e-148">Add a fragment</span></span>

<span data-ttu-id="de76e-149">Commerce サイト ビルダーでフラグメントをページに追加するには、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="de76e-149">To add a fragment to a page in Commerce site builder, follow these steps.</span></span>

1. <span data-ttu-id="de76e-150">左側のアウトライン ウィンドウで、またはビジュアル ページ ビルダーで直接、子モジュールを追加できるコンテナーまたはスロットを選択します。</span><span class="sxs-lookup"><span data-stu-id="de76e-150">In the outline pane on the left or directly in visual page builder, select a container or slot to which child modules can be added.</span></span>
1. <span data-ttu-id="de76e-151">コンテナまたはスロットの名前の横にある省略符号 (**...**) を選択します。</span><span class="sxs-lookup"><span data-stu-id="de76e-151">Select the ellipsis (**...**) next to the name of the container or slot.</span></span>  <span data-ttu-id="de76e-152">または、ビジュアル ページ ビルダーを使用している場合は、プラス記号 (**+**) を選択します。</span><span class="sxs-lookup"><span data-stu-id="de76e-152">Alternately, if using visual page builder, select the plus symbol (**+**).</span></span>  
1. <span data-ttu-id="de76e-153">**フラグメントの追加** を選択します。</span><span class="sxs-lookup"><span data-stu-id="de76e-153">Select **Add fragment**.</span></span>
    <!-- ![A screen capture of how to add an existing fragment to a slot or container](./media/add-fragment.png)-->
 
    > [!NOTE]
    > <span data-ttu-id="de76e-154">コンテナーまたはスロットが新しい子モジュールをサポートしていない場合、**フラグメントの追加** オプションは使用できません。</span><span class="sxs-lookup"><span data-stu-id="de76e-154">If the container or slot doesn't support new child modules, the **Add fragment** option is unavailable.</span></span>
    
1. <span data-ttu-id="de76e-155">**フラグメントの選択** ダイアログ ボックスで、追加するフラグメントを検索して選択します。</span><span class="sxs-lookup"><span data-stu-id="de76e-155">In the **Select fragment** dialog box, search for and select a fragment to add.</span></span> <span data-ttu-id="de76e-156">利用可能なフラグメントが一覧にない場合は、まず最初に、選択したコンテナーまたはスロットがサポートするモジュール タイプからフラグメントを作成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="de76e-156">If no available fragments are listed, you might first have to create a fragment from a module type that the selected container or slot supports.</span></span>
1. <span data-ttu-id="de76e-157">目的のフラグメントを選択して、ページのコンテナーまたはスロットに追加します。</span><span class="sxs-lookup"><span data-stu-id="de76e-157">Select your desired fragment to add it to the container or slot on your page.</span></span>
<!--    ![A screen capture of the fragment picker modal window](./media/fragment-picker.png)-->

> [!NOTE]
> <span data-ttu-id="de76e-158">コンテナーまたはスロットで許可されるモジュールは、ページのテンプレートまたはモジュール自体の定義によって定義されます。</span><span class="sxs-lookup"><span data-stu-id="de76e-158">The modules that are allowed in a container or slot are defined by the page's template or the modules' own definitions.</span></span>

### <a name="remove-a-fragment"></a><span data-ttu-id="de76e-159">フラグメントの削除</span><span class="sxs-lookup"><span data-stu-id="de76e-159">Remove a fragment</span></span>

<span data-ttu-id="de76e-160">Commerce サイト ビルダーのページのスロットまたはコンテナーからフラグメントを削除するには、次の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="de76e-160">To remove a fragment from a slot or container on a page in Commerce site builder, follow these steps.</span></span>

1. <span data-ttu-id="de76e-161">左のアウトライン ウィンドウで、削除するフラグメントの名前の横にある省略記号 (**...**)を選択し、ごみ箱記号を選択します。</span><span class="sxs-lookup"><span data-stu-id="de76e-161">In the outline pane on the left, select the ellipsis (**...**) next to the name of the fragment to be removed, and then select the trash can symbol.</span></span>  <span data-ttu-id="de76e-162">または、ビジュアル ページ ビルダーでフラグメントを選択し、フラグメントのツールバーにあるごみ箱の記号を選択することもできます。</span><span class="sxs-lookup"><span data-stu-id="de76e-162">Alternately, you can select the fragment in visual page builder and select the trash can symbol in the fragment's toolbar.</span></span>
1. <span data-ttu-id="de76e-163">フラグメントを削除するかどうかを確認するメッセージが表示されたら、**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="de76e-163">When you're prompted to confirm that you want to remove the fragment, select **OK**.</span></span>

> [!NOTE]
> <span data-ttu-id="de76e-164">ページからフラグメントを削除する場合は、そのページからそのフラグメントへの参照を削除するだけです。</span><span class="sxs-lookup"><span data-stu-id="de76e-164">When you remove a fragment from a page, you just remove the reference to it from that page.</span></span> <span data-ttu-id="de76e-165">サイトからフラグメントを削除することは **ありません**。</span><span class="sxs-lookup"><span data-stu-id="de76e-165">You do **not** delete the fragment from your site.</span></span> <span data-ttu-id="de76e-166">サイトからフラグメントを削除するには、フラグメント インスペクター ユーザーインターフェイス (UI) を使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="de76e-166">To delete fragments from your site, you must use the fragment inspector user interface (UI).</span></span> <span data-ttu-id="de76e-167">すべてのページ、テンプレート、またはその他のフラグメントで、フラグメントが参照されていない場合にのみ、フラグメントをサイトから削除することができます。</span><span class="sxs-lookup"><span data-stu-id="de76e-167">You can delete fragments from a site only if they aren't currently referenced by any pages, templates, or other fragments.</span></span>

### <a name="edit-a-fragment"></a><span data-ttu-id="de76e-168">フラグメントの編集</span><span class="sxs-lookup"><span data-stu-id="de76e-168">Edit a fragment</span></span>

<span data-ttu-id="de76e-169">フラグメントを編集するには、フラグメント エディター UI を使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="de76e-169">To edit fragments, you must use the fragment editor UI.</span></span> <span data-ttu-id="de76e-170">この制限は仕様です。</span><span class="sxs-lookup"><span data-stu-id="de76e-170">This restriction is by design.</span></span> <span data-ttu-id="de76e-171">作成者が、特定のページでモジュールを編集するプロセスを、多くのページで共有される可能性のあるフラグメントを編集するプロセスと混同しないようにすることができます。</span><span class="sxs-lookup"><span data-stu-id="de76e-171">It helps guarantee that authors don't confuse the process of editing the modules for a specific page with the process of editing fragments that might be shared across many pages.</span></span>

<span data-ttu-id="de76e-172">Commerce サイト ビルダーでフラグメントを編集するには、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="de76e-172">To edit a fragment in Commerce site builder, follow these steps.</span></span>

1. <span data-ttu-id="de76e-173">左のナビゲーション ウィンドウで、**フラグメント** を選択します。</span><span class="sxs-lookup"><span data-stu-id="de76e-173">In the navigation pane on the left, select **Fragments**.</span></span>
1. <span data-ttu-id="de76e-174">**フラグメント** 下で、編集するフラグメントを選択します。</span><span class="sxs-lookup"><span data-stu-id="de76e-174">Under **Fragments**, select the fragment to edit.</span></span>
1. <span data-ttu-id="de76e-175">必要に応じて、フラグメントのモジュール プロパティと構造を編集します。</span><span class="sxs-lookup"><span data-stu-id="de76e-175">Edit the fragment's module properties and structure as you require.</span></span> <span data-ttu-id="de76e-176">このプロセスは、ページ エディター ビューで編集するモジュールの編集プロセスに似ています。</span><span class="sxs-lookup"><span data-stu-id="de76e-176">The process resembles the process for editing modules are edited in the page editor view.</span></span>

<span data-ttu-id="de76e-177">ページ、テンプレート、または親フラグメントでフラグメントを選択し、右側のプロパティ ウィンドウで **フラグメントの編集** を選択することによって、フラグメントを編集することもできます。</span><span class="sxs-lookup"><span data-stu-id="de76e-177">You can also edit a fragment by selecting it on a page, in a template, or in a parent fragment, and then selecting **Edit Fragment** in the properties pane on the right.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="de76e-178">追加リソース</span><span class="sxs-lookup"><span data-stu-id="de76e-178">Additional resources</span></span>

[<span data-ttu-id="de76e-179">テンプレートとレイアウトの概要</span><span class="sxs-lookup"><span data-stu-id="de76e-179">Templates and layouts overview</span></span>](templates-layouts-overview.md)

[<span data-ttu-id="de76e-180">テンプレートの使用</span><span class="sxs-lookup"><span data-stu-id="de76e-180">Work with templates</span></span>](work-with-templates.md)

[<span data-ttu-id="de76e-181">プリセット レイアウトの使用</span><span class="sxs-lookup"><span data-stu-id="de76e-181">Work with preset layouts</span></span>](work-with-layouts.md)

[<span data-ttu-id="de76e-182">公開グループで動作</span><span class="sxs-lookup"><span data-stu-id="de76e-182">Work with publish groups</span></span>](publish-groups.md)
