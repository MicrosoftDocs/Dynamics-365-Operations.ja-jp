---
title: フラグメントで動作
description: このトピックでは、Microsoft Dynamics 365 Commerce でフラグメントを使用する理由、時期、および方法について説明します。
author: v-chgri
manager: annbe
ms.date: 12/12/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.search.region: Global
ms.search.industry: retail
ms.author: phinneyridge
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 32482538b2913e6585257bcf7a1cbe780d3cdd30
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 12/20/2019
ms.locfileid: "2914703"
---
# <a name="work-with-fragments"></a><span data-ttu-id="9bf16-103">フラグメントで動作</span><span class="sxs-lookup"><span data-stu-id="9bf16-103">Work with fragments</span></span> 

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

<span data-ttu-id="9bf16-104">このトピックでは、Microsoft Dynamics 365 Commerce でフラグメントを使用する理由、時期、および方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="9bf16-104">This topic describes why, when, and how to use fragments in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="9bf16-105">概要</span><span class="sxs-lookup"><span data-stu-id="9bf16-105">Overview</span></span>

<span data-ttu-id="9bf16-106">フラグメントを使用すると、サイト全体で再利用する必要があるモジュール コンフィギュレーションに対して、一元的な作成エクスペリエンスを実行できます。</span><span class="sxs-lookup"><span data-stu-id="9bf16-106">Fragments allow for a centralized authoring experience for module configurations that must be reused throughout your site.</span></span> <span data-ttu-id="9bf16-107">たとえば、ヘッダー、フッター、およびバナーは多くのページに渡って共有されるため、フラグメントとしてコンフィギュレーションされることがよくあります。</span><span class="sxs-lookup"><span data-stu-id="9bf16-107">For example, headers, footers, and banners are often configured as fragments, because they are shared across many pages.</span></span> <span data-ttu-id="9bf16-108">サイトの別のページに挿入することができる小さな Web ページとして、フラグメントを考えることができます。</span><span class="sxs-lookup"><span data-stu-id="9bf16-108">You can think of fragments as miniature webpages that can be inserted into other pages on your site.</span></span> <span data-ttu-id="9bf16-109">フラグメントには独自のライフサイクルがあります。</span><span class="sxs-lookup"><span data-stu-id="9bf16-109">Fragments have their own lifecycle.</span></span> <span data-ttu-id="9bf16-110">つまり、作成ツールでは、独立したエンティティとして作成、参照、更新、削除されるということです。</span><span class="sxs-lookup"><span data-stu-id="9bf16-110">In other words, they are created, referenced, updated, and deleted as independent entities in the authoring tools.</span></span>

<span data-ttu-id="9bf16-111">フラグメントをコンフィギュレーションした後は、サイト構造でモジュールを使用できる場所ではどこでも使用できます。</span><span class="sxs-lookup"><span data-stu-id="9bf16-111">After fragments are configured, they can be used wherever modules can be used in your site structure.</span></span> <span data-ttu-id="9bf16-112">フラグメントは、ページ、レイアウト、テンプレート、およびその他のフラグメントで参照できます。</span><span class="sxs-lookup"><span data-stu-id="9bf16-112">Fragments can be referenced on pages, in layouts, in templates, and in other fragments.</span></span>

> [!NOTE]
> <span data-ttu-id="9bf16-113">フラグメントは、他のフラグメント内の 7 つの階層にまで入れ子にすることができます。</span><span class="sxs-lookup"><span data-stu-id="9bf16-113">Fragments can be nested up to seven levels deep inside other fragments.</span></span>

<span data-ttu-id="9bf16-114">たとえば、季節のイベントをサイト内の多数のページで推進したい場合に、フラグメントを使用できます。</span><span class="sxs-lookup"><span data-stu-id="9bf16-114">For example, if you want to promote a seasonal event cross many pages on our site, you can use a fragment.</span></span> <span data-ttu-id="9bf16-115">新しいフラグメントを作成するプロセスの最初のステップとして、開始するモジュールのタイプを選択します。</span><span class="sxs-lookup"><span data-stu-id="9bf16-115">The first step in the process of creating a new fragment is to select the type of module that you want to start from.</span></span> <span data-ttu-id="9bf16-116">この例では、ヒーロー モジュールからフラグメントを作成できます。</span><span class="sxs-lookup"><span data-stu-id="9bf16-116">For this example, you can build the fragment from a hero module.</span></span>

> [!NOTE]
> <span data-ttu-id="9bf16-117">フラグメントは、どのモジュール タイプからでも作成できます。</span><span class="sxs-lookup"><span data-stu-id="9bf16-117">Fragments can be built from any module type.</span></span>

<span data-ttu-id="9bf16-118">その後、特定の販促コンテンツで、ヒーロー フラグメントをコンフィギュレーションすることができます。</span><span class="sxs-lookup"><span data-stu-id="9bf16-118">You can then configure the hero fragment with your specific promotional content.</span></span> <span data-ttu-id="9bf16-119">必要に応じてローカライズすることもできます。</span><span class="sxs-lookup"><span data-stu-id="9bf16-119">You can also localize it as you require.</span></span> <span data-ttu-id="9bf16-120">新しいスタンドアロンのヒーローのフラグメントを、サイト全体で事前にコンフィギュレーションされたモジュールとして使用できます。</span><span class="sxs-lookup"><span data-stu-id="9bf16-120">The new stand-alone hero fragment can then be consumed as a preconfigured module throughout your site.</span></span> <span data-ttu-id="9bf16-121">これは、テンプレート、特定のページ、またはヒーロー モジュールを含むことができるその他のフラグメントに、簡単に追加できます。</span><span class="sxs-lookup"><span data-stu-id="9bf16-121">You can easily add it to templates, to specific pages, or to other fragments that can contain hero modules.</span></span>

<span data-ttu-id="9bf16-122">フラグメントが追加された場所はすべて、作成したセントラル ヒーロー フラグメントへの参照です。</span><span class="sxs-lookup"><span data-stu-id="9bf16-122">All the places where the fragment is added are references to the central hero fragment that you created.</span></span> <span data-ttu-id="9bf16-123">フラグメントに変更を発行した場合、その変更は、サイト全体でそのフラグメントが参照されているすべての場所にすぐに反映されます。</span><span class="sxs-lookup"><span data-stu-id="9bf16-123">If you publish changes to the fragment, those changes are immediately reflected in all the places where the fragment is referenced across the site.</span></span> <span data-ttu-id="9bf16-124">したがって、フラグメントは、サイトのモジュール コンフィギュレーションを再利用して一元管理するための、強力かつ効率的な方法です。</span><span class="sxs-lookup"><span data-stu-id="9bf16-124">Therefore, fragments provide a powerful and efficient way to reuse and centrally manage module configurations on a site.</span></span> <span data-ttu-id="9bf16-125">これらを効果的に使用することにより、機敏性を大幅に向上させ、サイトのコンテンツ管理に関連するコストを削減することができます。</span><span class="sxs-lookup"><span data-stu-id="9bf16-125">By effectively using them, you can significantly increase agility and help reduce the cost that is associated with managing site content.</span></span>

<span data-ttu-id="9bf16-126">次の図は、フラグメントを使用して、E コマース サイト全体で共有しているモジュールのコンフィギュレーションを一元的に作成する方法を示しています。</span><span class="sxs-lookup"><span data-stu-id="9bf16-126">The following illustration shows how fragments can be used to centralize authoring of shared module configurations across an e-Commerce site.</span></span>

![フラグメントを使用して、E コマース サイト全体で共有しているモジュールのコンフィギュレーションを一元的に作成する方法を示した図](./media/fragment-figure1.png)

## <a name="create-a-fragment"></a><span data-ttu-id="9bf16-128">フラグメントの作成</span><span class="sxs-lookup"><span data-stu-id="9bf16-128">Create a fragment</span></span>

<span data-ttu-id="9bf16-129">新しいフラグメントを作成するか、既存のモジュール コンフィギュレーションをフラグメントとして保存することができます。</span><span class="sxs-lookup"><span data-stu-id="9bf16-129">You can either create a new fragment or save an existing module configuration as a fragment.</span></span>

### <a name="create-a-new-fragment"></a><span data-ttu-id="9bf16-130">新しいフラグメントの作成</span><span class="sxs-lookup"><span data-stu-id="9bf16-130">Create a new fragment</span></span>

<span data-ttu-id="9bf16-131">新しいフラグメントを作成するには、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="9bf16-131">To create a new fragment, follow these steps.</span></span>

1. <span data-ttu-id="9bf16-132">左のナビゲーション ウィンドウで、**フラグメント**を選択します。</span><span class="sxs-lookup"><span data-stu-id="9bf16-132">In the navigation pane on the left, select **Fragments**.</span></span>
1. <span data-ttu-id="9bf16-133">**新しいページ フラグメント**を選択します。</span><span class="sxs-lookup"><span data-stu-id="9bf16-133">Select **New Page Fragment**.</span></span> <span data-ttu-id="9bf16-134">使用可能なすべてのモジュール タイプを示すダイアログ ボックスが表示されます。</span><span class="sxs-lookup"><span data-stu-id="9bf16-134">A dialog box appears that shows all the available module types.</span></span> <span data-ttu-id="9bf16-135">先に説明したように、どのモジュール タイプからでもフラグメントを作成できます。</span><span class="sxs-lookup"><span data-stu-id="9bf16-135">As was mentioned earlier, fragments can be created from any module type.</span></span>
1. <span data-ttu-id="9bf16-136">フラグメントのモジュール タイプを選択し、**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="9bf16-136">Select a module type for your fragment, and then select **OK**.</span></span>

    > [!TIP]
    > <span data-ttu-id="9bf16-137">汎用コンテナー モジュール タイプを選択することで、後でフラグメントを更新およびコンフィギュレーションする必要がある場合に、最大の柔軟性を得ることができます。</span><span class="sxs-lookup"><span data-stu-id="9bf16-137">By selecting a generic container module type, you get the most flexibility when you must update and configure your fragment later.</span></span>

### <a name="save-an-existing-module-configuration-as-a-fragment"></a><span data-ttu-id="9bf16-138">フラグメントとして既存のモジュール コンフィギュレーションを保存</span><span class="sxs-lookup"><span data-stu-id="9bf16-138">Save an existing module configuration as a fragment</span></span>

<span data-ttu-id="9bf16-139">以前にコンフィギュレーションしたモジュールを再利用可能なフラグメントに変換するには、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="9bf16-139">To convert a previously configured module to a reusable fragment, follow these steps.</span></span>

1. <span data-ttu-id="9bf16-140">フラグメントに変換するモジュールを含むページまたはテンプレートを開きます。</span><span class="sxs-lookup"><span data-stu-id="9bf16-140">Open a page or template that contains the module that you want to convert to a fragment.</span></span>
1. <span data-ttu-id="9bf16-141">左のアウトライン ウィンドウで、モジュールの名前の横にある省略記号ボタン (**...**) を選択し、**フラグメントとして保存**を選択します。</span><span class="sxs-lookup"><span data-stu-id="9bf16-141">In the outline pane on the left, select the ellipsis button (**...**) next to the name of the module, and then select **Save as Fragment**.</span></span> <span data-ttu-id="9bf16-142">ダイアログ ボックスが表示されます。</span><span class="sxs-lookup"><span data-stu-id="9bf16-142">A dialog box appears.</span></span>
1. <span data-ttu-id="9bf16-143">フラグメントの名前とメタデータを入力します。</span><span class="sxs-lookup"><span data-stu-id="9bf16-143">Enter a name and metadata for the fragment.</span></span>
1. <span data-ttu-id="9bf16-144">**OK** を選択すると、他のページに追加できるフラグメントとしてモジュール コンフィギュレーションが保存されます。</span><span class="sxs-lookup"><span data-stu-id="9bf16-144">Select **OK** to save the module configuration as a fragment that can be added to other pages.</span></span>

## <a name="add-remove-or-edit-fragments-on-a-page"></a><span data-ttu-id="9bf16-145">ページでのフラグメントの追加、削除、または編集</span><span class="sxs-lookup"><span data-stu-id="9bf16-145">Add, remove, or edit fragments on a page</span></span>

<span data-ttu-id="9bf16-146">次の手順では、フラグメントを追加、削除、および編集する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="9bf16-146">The following procedures describe how to add, remove, and edit fragments.</span></span>

### <a name="add-a-fragment"></a><span data-ttu-id="9bf16-147">フラグメントの追加</span><span class="sxs-lookup"><span data-stu-id="9bf16-147">Add a fragment</span></span>

<span data-ttu-id="9bf16-148">ページにフラグメントを追加するには、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="9bf16-148">To add a fragment to a page, follow these steps.</span></span>

1. <span data-ttu-id="9bf16-149">左側のアウトライン ウィンドウで、子モジュールを追加できるコンテナーまたはスロットを選択します。</span><span class="sxs-lookup"><span data-stu-id="9bf16-149">In the outline pane on the left, select a container or slot that child modules can be added to.</span></span>
1. <span data-ttu-id="9bf16-150">コンテナーまたはスロットの名前の横にある省略記号ボタンを選択し、**フラグメントの追加**を選択します。</span><span class="sxs-lookup"><span data-stu-id="9bf16-150">Select the ellipsis button next to the name of the container or slot, and then select **Add Fragment**.</span></span> <span data-ttu-id="9bf16-151">ダイアログ ボックスが表示されます。</span><span class="sxs-lookup"><span data-stu-id="9bf16-151">A dialog box appears.</span></span>

    > [!NOTE]
    > <span data-ttu-id="9bf16-152">コンテナーまたはスロットが新しい子モジュールをサポートしていない場合、**フラグメントの追加**オプションは使用できません。</span><span class="sxs-lookup"><span data-stu-id="9bf16-152">If the container or slot doesn't support new child modules, the **Add Fragment** option is unavailable.</span></span>

1. <span data-ttu-id="9bf16-153">ダイアログ ボックスで、追加するフラグメントを検索して選択します。</span><span class="sxs-lookup"><span data-stu-id="9bf16-153">In the dialog box, search for and select a fragment to add.</span></span> <span data-ttu-id="9bf16-154">利用可能なフラグメントが一覧にない場合は、まず最初に、選択したコンテナーまたはスロットがサポートするモジュール タイプからフラグメントを作成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="9bf16-154">If no available fragments are listed, you might first have to create a fragment from a module type that the selected container or slot supports.</span></span>
1. <span data-ttu-id="9bf16-155">**OK** をクリックすると、選択したフラグメントがページ内で選択したコンテナーまたはスロットに追加されます。</span><span class="sxs-lookup"><span data-stu-id="9bf16-155">Select **OK** to add the selected fragment to the selected container or slot on your page.</span></span>

> [!NOTE]
> <span data-ttu-id="9bf16-156">コンテナーまたはスロットで許可されるモジュールは、ページのテンプレートまたはモジュール自体の定義によって定義されます。</span><span class="sxs-lookup"><span data-stu-id="9bf16-156">The modules that are allowed in a container or slot are defined by the page's template or the modules' own definitions.</span></span>

### <a name="remove-a-fragment"></a><span data-ttu-id="9bf16-157">フラグメントの削除</span><span class="sxs-lookup"><span data-stu-id="9bf16-157">Remove a fragment</span></span>

<span data-ttu-id="9bf16-158">ページ上のスロットまたはコンテナーからフラグメントを削除するには、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="9bf16-158">To remove a fragment from a slot or container on a page, follow these steps.</span></span>

1. <span data-ttu-id="9bf16-159">左のアウトライン ウィンドウで、削除するフラグメントの名前の横にある省略記号ボタンを選択し、ごみ箱ボタンを選択します。</span><span class="sxs-lookup"><span data-stu-id="9bf16-159">In the outline pane on the left, select the ellipsis button next to the name of the fragment to remove, and then select the trash can button.</span></span>
1. <span data-ttu-id="9bf16-160">フラグメントを削除するかどうかを確認するメッセージが表示されたら、**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="9bf16-160">When you're prompted to confirm that you want to remove the fragment, select **OK**.</span></span>

> [!NOTE]
> <span data-ttu-id="9bf16-161">ページからフラグメントを削除する場合は、そのページからそのフラグメントへの参照を削除するだけです。</span><span class="sxs-lookup"><span data-stu-id="9bf16-161">When you remove a fragment from a page, you just remove the reference to it from that page.</span></span> <span data-ttu-id="9bf16-162">サイトからフラグメントを削除することは**ありません**。</span><span class="sxs-lookup"><span data-stu-id="9bf16-162">You do **not** delete the fragment from your site.</span></span> <span data-ttu-id="9bf16-163">サイトからフラグメントを削除するには、フラグメント インスペクター ユーザーインターフェイス (UI) を使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="9bf16-163">To delete fragments from your site, you must use the fragment inspector user interface (UI).</span></span> <span data-ttu-id="9bf16-164">すべてのページ、テンプレート、またはその他のフラグメントで、フラグメントが参照されていない場合にのみ、フラグメントをサイトから削除することができます。</span><span class="sxs-lookup"><span data-stu-id="9bf16-164">You can delete fragments from a site only if they aren't currently referenced by any pages, templates, or other fragments.</span></span>

### <a name="edit-a-fragment"></a><span data-ttu-id="9bf16-165">フラグメントの編集</span><span class="sxs-lookup"><span data-stu-id="9bf16-165">Edit a fragment</span></span>

<span data-ttu-id="9bf16-166">フラグメントを編集するには、フラグメント エディター UI を使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="9bf16-166">To edit fragments, you must use the fragment editor UI.</span></span> <span data-ttu-id="9bf16-167">この制限は仕様です。</span><span class="sxs-lookup"><span data-stu-id="9bf16-167">This restriction is by design.</span></span> <span data-ttu-id="9bf16-168">作成者が、特定のページでモジュールを編集するプロセスを、多くのページで共有される可能性のあるフラグメントを編集するプロセスと混同しないようにすることができます。</span><span class="sxs-lookup"><span data-stu-id="9bf16-168">It helps guarantee that authors don't confuse the process of editing the modules for a specific page with the process of editing fragments that might be shared across many pages.</span></span>

<span data-ttu-id="9bf16-169">フラグメントを編集するには、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="9bf16-169">To edit a fragment, follow these steps.</span></span>

1. <span data-ttu-id="9bf16-170">左のナビゲーション ウィンドウで、**フラグメント**を選択します。</span><span class="sxs-lookup"><span data-stu-id="9bf16-170">In the navigation pane on the left, select **Fragments**.</span></span>
1. <span data-ttu-id="9bf16-171">**フラグメント**下で、編集するフラグメントを選択します。</span><span class="sxs-lookup"><span data-stu-id="9bf16-171">Under **Fragments**, select the fragment to edit.</span></span>
1. <span data-ttu-id="9bf16-172">必要に応じて、フラグメントのモジュール プロパティと構造を編集します。</span><span class="sxs-lookup"><span data-stu-id="9bf16-172">Edit the fragment's module properties and structure as you require.</span></span> <span data-ttu-id="9bf16-173">このプロセスは、ページ エディター ビューで編集するモジュールの編集プロセスに似ています。</span><span class="sxs-lookup"><span data-stu-id="9bf16-173">The process resembles the process for editing modules are edited in the page editor view.</span></span>

<span data-ttu-id="9bf16-174">ページ、テンプレート、または親フラグメントでフラグメントを選択し、右側のプロパティ ウィンドウで**フラグメントの編集**を選択することによって、フラグメントを編集することもできます。</span><span class="sxs-lookup"><span data-stu-id="9bf16-174">You can also edit a fragment by selecting it on a page, in a template, or in a parent fragment, and then selecting **Edit Fragment** in the properties pane on the right.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="9bf16-175">追加リソース</span><span class="sxs-lookup"><span data-stu-id="9bf16-175">Additional resources</span></span>

[<span data-ttu-id="9bf16-176">テンプレートとレイアウトの概要</span><span class="sxs-lookup"><span data-stu-id="9bf16-176">Templates and layouts overview</span></span>](templates-layouts-overview.md)

[<span data-ttu-id="9bf16-177">テンプレートの使用</span><span class="sxs-lookup"><span data-stu-id="9bf16-177">Work with templates</span></span>](work-with-templates.md)

[<span data-ttu-id="9bf16-178">プリセット レイアウトの使用</span><span class="sxs-lookup"><span data-stu-id="9bf16-178">Work with preset layouts</span></span>](work-with-layouts.md)

[<span data-ttu-id="9bf16-179">公開グループで動作</span><span class="sxs-lookup"><span data-stu-id="9bf16-179">Work with publish groups</span></span>](publish-groups.md)
