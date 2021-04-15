---
title: モジュールで動作
description: このトピックでは、Microsoft Dynamics 365 Commerce でモジュールを使用する時期と方法について説明します。
author: phinneyridge
ms.date: 09/15/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.region: Global
ms.search.industry: ''
ms.author: stuharg
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 6d872719d3b1aa27ccfdcf36d7739c883e7b4996
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/31/2021
ms.locfileid: "5801364"
---
# <a name="work-with-modules"></a><span data-ttu-id="839d8-103">モジュールで動作</span><span class="sxs-lookup"><span data-stu-id="839d8-103">Work with modules</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="839d8-104">このトピックでは、Microsoft Dynamics 365 Commerce でモジュールを使用する時期と方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="839d8-104">This topic describes how and when to use modules in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="839d8-105">モジュールは、ページ構造を構成する論理構成要素であり、さまざまな目的と範囲があります。</span><span class="sxs-lookup"><span data-stu-id="839d8-105">Modules are logical building blocks that make up your page structure, and they have various purposes and scopes.</span></span> <span data-ttu-id="839d8-106">一部のモジュールは上位レベルのコンテナーであり、その唯一の目的は、他のモジュール (子モジュール) を保持して整理することです。</span><span class="sxs-lookup"><span data-stu-id="839d8-106">Some modules are high-level containers, and their only purpose is to hold and organize other modules (child modules).</span></span> <span data-ttu-id="839d8-107">単純なイメージ配置モジュールなど、その他のモジュールには、特定の目的があります。</span><span class="sxs-lookup"><span data-stu-id="839d8-107">Other modules, such as a simple image placement module, have a very specific purpose.</span></span> <span data-ttu-id="839d8-108">カルーセル モジュールなど、その他のモジュールは、これら 2 つのカテゴリの間に含まれます。</span><span class="sxs-lookup"><span data-stu-id="839d8-108">Other modules, such as a carousel module, fall somewhere between those two categories.</span></span>

<span data-ttu-id="839d8-109">既定では、Dynamics 365 Commerce のサイトには、もっとも基本的な eコマースのシナリオを実現できるモジュール ライブラリが含まれています。</span><span class="sxs-lookup"><span data-stu-id="839d8-109">By default, your Dynamics 365 Commerce site includes a module library that lets you achieve most basic e-Commerce scenarios.</span></span> <span data-ttu-id="839d8-110">これらのモジュールを使用するだけで、エンド ツー エンドの E コマースサイトを構築できます。</span><span class="sxs-lookup"><span data-stu-id="839d8-110">You should be able to construct an end-to-end e-Commerce site just by using these modules.</span></span> <span data-ttu-id="839d8-111">ただし、特定のニーズに合わせて、これらのモジュールをカスタマイズしたり、新しいカスタム モジュールを作成したりすることが必要な場合もあります。</span><span class="sxs-lookup"><span data-stu-id="839d8-111">However, you might also want to customize these modules or build new, custom modules for specific needs.</span></span> <span data-ttu-id="839d8-112">カスタム モジュールを作成する場合は、モジュール デザイン ソフトウェア開発キット (SDK) を使用して、カスタム モジュール ライブラリを作成できます。</span><span class="sxs-lookup"><span data-stu-id="839d8-112">If you want to build custom modules, a module design software development kit (SDK) is available to help you create a custom module library.</span></span>

## <a name="container-modules-and-slots"></a><span data-ttu-id="839d8-113">コンテナー モジュールとスロット</span><span class="sxs-lookup"><span data-stu-id="839d8-113">Container modules and slots</span></span>

<span data-ttu-id="839d8-114">既に説明したように、一部のモジュールは、子モジュールを保持するように設計されています。</span><span class="sxs-lookup"><span data-stu-id="839d8-114">As was mentioned earlier, some modules are designed to hold child modules.</span></span> <span data-ttu-id="839d8-115">これらのモジュールは *コンテナー* と呼ばれ、入れ子になったモジュールの階層を許可します。</span><span class="sxs-lookup"><span data-stu-id="839d8-115">These modules are known as *containers*, and they allow for hierarchies of nested modules.</span></span> <span data-ttu-id="839d8-116">コンテナー モジュールは *スロット* を含みます。</span><span class="sxs-lookup"><span data-stu-id="839d8-116">Container modules include *slots*.</span></span> <span data-ttu-id="839d8-117">スロットは、コンテナー内の子モジュールのレイアウトと目的を処理するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="839d8-117">Slots are used to handle the layout and purpose of child modules in the container.</span></span> <span data-ttu-id="839d8-118">たとえば、いくつかの重要なスロットを定義する基本的なページ コンテナー モジュール (すべてのページでトップレベルのモジュール) があります。</span><span class="sxs-lookup"><span data-stu-id="839d8-118">An example is a basic page container module (a top-level module for any page) that defines several important slots:</span></span>

- <span data-ttu-id="839d8-119">ヘッダー スロット</span><span class="sxs-lookup"><span data-stu-id="839d8-119">A header slot</span></span>
- <span data-ttu-id="839d8-120">サブヘッダー スロット</span><span class="sxs-lookup"><span data-stu-id="839d8-120">A sub-header slot</span></span>
- <span data-ttu-id="839d8-121">メイン スロット</span><span class="sxs-lookup"><span data-stu-id="839d8-121">A main slot</span></span>
- <span data-ttu-id="839d8-122">フッター スロット</span><span class="sxs-lookup"><span data-stu-id="839d8-122">A footer slot</span></span>
- <span data-ttu-id="839d8-123">サブフッター スロット</span><span class="sxs-lookup"><span data-stu-id="839d8-123">A sub-footer slot</span></span>

<span data-ttu-id="839d8-124">モジュールの開発者はこれらのスロットを定義し、子モジュールとそれに直接入れることができる子モジュールの数を決定します。</span><span class="sxs-lookup"><span data-stu-id="839d8-124">The module's developer defines these slots, and determines which child modules and how many child modules can be put directly inside it.</span></span> <span data-ttu-id="839d8-125">たとえば、ヘッダー スロットは **ヘッダー モジュール** タイプのモジュールを 1 つだけサポートするのに対して、本文スロットはすべてのタイプのモジュールを無制限にサポートすることができます (他のページのコンテナー モジュールを除く)。</span><span class="sxs-lookup"><span data-stu-id="839d8-125">For example, the header slot might support only one module of the **Header Module** type, whereas the body slot might support an unlimited number of modules of any type (except other page container modules).</span></span>

<span data-ttu-id="839d8-126">作成ツールでは、ページの作成者は、どのモジュールを各スロットに配置できるか/できないかをあらかじめ把握している必要はありません。</span><span class="sxs-lookup"><span data-stu-id="839d8-126">In the authoring tools, page authors don't have to know in advance which modules can and can't be put in each slot.</span></span> <span data-ttu-id="839d8-127">ページの作成者がスロットを選択し、そのスロットに追加するモジュールを選択しようとすると、そのスロットでサポートされているモジュールのタイプがフィルター処理されて表示されます。</span><span class="sxs-lookup"><span data-stu-id="839d8-127">When page authors select a slot and then try to select a module to add to it, they see a filtered view of module types that are supported for that slot.</span></span>

## <a name="content-modules"></a><span data-ttu-id="839d8-128">コンテンツ モジュール</span><span class="sxs-lookup"><span data-stu-id="839d8-128">Content modules</span></span>

<span data-ttu-id="839d8-129">コンテンツ モジュールには、テキスト (ヘッドライン、段落、リンクなど) または資産参照 (画像、ビデオ、PDF など) といったコンテンツやメディア要素が含まれます。</span><span class="sxs-lookup"><span data-stu-id="839d8-129">Content modules contain content and media elements, such as text (for example, headlines, paragraphs, and links) or asset references (for example, images, video, and PDFs).</span></span> <span data-ttu-id="839d8-130">一般的なコンテンツ モジュール タイプには、コンテンツ ブロック、テキスト ブロック、およびプロモーションのバナー モジュールがあります。</span><span class="sxs-lookup"><span data-stu-id="839d8-130">Typical content module types include content block, text block, and promo banner modules.</span></span> <span data-ttu-id="839d8-131">これら 3 つのタイプのモジュールには、テキストまたはメディアを含めることができます。また、ページ上に表示されないようにするために、子モジュールを使用する必要はありません。</span><span class="sxs-lookup"><span data-stu-id="839d8-131">Modules of these three types can contain text or media, and they don't require any child modules to make something visible on a page.</span></span>

<span data-ttu-id="839d8-132">一般的な日々のページとコンテンツ作成活動の大部分は、コンテンツ モジュールに関連しています。主には、これらのモジュールが親コンテナー モジュールに表示される実際のコンテンツを定義するためです。</span><span class="sxs-lookup"><span data-stu-id="839d8-132">The majority of typical, day-to-day page and content authoring activities involve content modules, primarily because these modules define the actual content that is rendered in their parent container modules.</span></span> <span data-ttu-id="839d8-133">多くのコンテンツ モジュールが使用可能で、これらのモジュールは通常、入れ子になったモジュールのページ階層に追加する最後のピースになります。</span><span class="sxs-lookup"><span data-stu-id="839d8-133">Many content modules are available, and these modules are typically the last pieces that you will add to a page's hierarchy of nested modules.</span></span>

<span data-ttu-id="839d8-134">次の図は、モジュールが親コンテナー モジュール スロットの中でどのように入れ子になるかを示しています。</span><span class="sxs-lookup"><span data-stu-id="839d8-134">The following illustration shows how modules are nested inside parent container module slots.</span></span>

![入れ子のモジュール](../commerce/media/basic-module-nesting.png)

## <a name="add-or-remove-modules"></a><span data-ttu-id="839d8-136">モジュールの追加または削除</span><span class="sxs-lookup"><span data-stu-id="839d8-136">Add or remove modules</span></span>

<span data-ttu-id="839d8-137">次の手順では、モジュールを追加および削除する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="839d8-137">The following procedures describe how to add and remove modules.</span></span>

### <a name="add-a-module"></a><span data-ttu-id="839d8-138">モジュールの追加</span><span class="sxs-lookup"><span data-stu-id="839d8-138">Add a module</span></span>

<span data-ttu-id="839d8-139">ページ上のスロットまたはコンテナーにモジュールを追加するには、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="839d8-139">To add a module to a slot or container on a page, follow these steps.</span></span>

1. <span data-ttu-id="839d8-140">左側のアウトライン ウィンドウで、またはメイン キャンバスで直接、子モジュールを追加できるコンテナーまたはスロットを選択します。</span><span class="sxs-lookup"><span data-stu-id="839d8-140">In the outline pane on the left or directly in the main canvas, select a container or slot to which a child module can be added.</span></span>

    > [!NOTE]
    > <span data-ttu-id="839d8-141">モジュール デザイナーは、特定のモジュール スロットに追加できるモジュール タイプのリストを定義します。</span><span class="sxs-lookup"><span data-stu-id="839d8-141">The module designer defines the list of modules types that can be added to a specific module slot.</span></span> <span data-ttu-id="839d8-142">テンプレートの作成者は、使用可能なモジュール オプションを調整して一貫性のある検索エンジン最適化 (SEO) を実現し、特定のテンプレートから作成されたすべてのページの作成効率を高めることができます。</span><span class="sxs-lookup"><span data-stu-id="839d8-142">Template authors can then refine the allowed module options to help guarantee consistent search engine optimization (SEO) and authoring efficiency for all the pages that are built from a specific template.</span></span> <span data-ttu-id="839d8-143">モジュールをスロットに追加するとき、**モジュールの追加** ダイアログ ボックスは自動的にフィルター処理され、選択したコンテナーまたはスロットでサポートされているモジュールのみが表示されます。</span><span class="sxs-lookup"><span data-stu-id="839d8-143">When adding a module to a slot, the **Add Module** dialog box is automatically filtered so that it shows only modules that are supported in the selected container or slot.</span></span> <span data-ttu-id="839d8-144">許可されるモジュールのこの一覧は、ページのテンプレートまたはコンテナー モジュールの定義によって決まります。</span><span class="sxs-lookup"><span data-stu-id="839d8-144">This list of allowed modules is determined by the page's template or the container's module definition.</span></span>

1. <span data-ttu-id="839d8-145">アウトライン ペインを使用している場合は、モジュール名の横にある省略記号 (**...**) を選択し、**モジュールの追加** を選択します。</span><span class="sxs-lookup"><span data-stu-id="839d8-145">If using the outline pane, select the ellipsis (**...**) next to the module name, and then select **Add Module**.</span></span> <span data-ttu-id="839d8-146">コントロールをキャンバス内で直接使用している場合は、現在選択されているモジュールと隣接している空のスロットでプラス記号 (**+**) を選択し、**モジュールの追加** を選択します。</span><span class="sxs-lookup"><span data-stu-id="839d8-146">If using the controls directly within the canvas, select the plus symbol (**+**) in an empty slot or adjacent to the currently selected module, and then select **Add Module**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="839d8-147">コンテナーまたはスロットが新しい子モジュールをサポートしていない場合、**モジュールの追加** オプションは使用できません。</span><span class="sxs-lookup"><span data-stu-id="839d8-147">If a container or slot doesn't support new child modules, the **Add Module** option is unavailable.</span></span>

1. <span data-ttu-id="839d8-148">**モジュールの追加** ダイアログ ボックスで、ページに追加するモジュールを選択します。</span><span class="sxs-lookup"><span data-stu-id="839d8-148">In the **Add Module** dialog box, select a module to add to your page.</span></span>

    > [!TIP]
    > <span data-ttu-id="839d8-149">**コンテンツ ブロック** は、初心者向けの優れたモジュール タイプです。</span><span class="sxs-lookup"><span data-stu-id="839d8-149">**Content block** is a good module type for beginners to work with.</span></span>

1. <span data-ttu-id="839d8-150">**OK** をクリックすると、選択したモジュールがページ内で選択したコンテナーまたはスロットに追加されます。</span><span class="sxs-lookup"><span data-stu-id="839d8-150">Select **OK** to add the selected module to the selected container or slot on your page.</span></span>

### <a name="remove-a-module"></a><span data-ttu-id="839d8-151">モジュールの削除</span><span class="sxs-lookup"><span data-stu-id="839d8-151">Remove a module</span></span>

<span data-ttu-id="839d8-152">ページ上のスロットまたはコンテナーからモジュールを削除するには、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="839d8-152">To remove a module from a slot or container on a page, follow these steps.</span></span>

1. <span data-ttu-id="839d8-153">左のアウトライン ウィンドウで、削除するモジュールの名前の横にある省略記号 (**...**)を選択し、ごみ箱記号を選択します。</span><span class="sxs-lookup"><span data-stu-id="839d8-153">In the outline pane on the left, select the ellipsis (**...**) next to the name of the module to be removed, and then select the trash can symbol.</span></span> <span data-ttu-id="839d8-154">また、メインキャン バスでは、選択したモジュールのツールバー上のごみ箱記号を選択することもできます。</span><span class="sxs-lookup"><span data-stu-id="839d8-154">Alternately, in the main canvas you can select the trash can symbol on a selected module's toolbar.</span></span>
1. <span data-ttu-id="839d8-155">モジュールを削除するかどうかを確認するメッセージが表示されたら、**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="839d8-155">When prompted to confirm that you want to remove the module, select **OK**.</span></span>

## <a name="move-a-module-to-a-new-position"></a><span data-ttu-id="839d8-156">モジュールを新しい位置に移動する</span><span class="sxs-lookup"><span data-stu-id="839d8-156">Move a module to a new position</span></span>

<span data-ttu-id="839d8-157">ページ内の新しい位置にモジュールを移動するには、次のいずれかの方法を使用します。</span><span class="sxs-lookup"><span data-stu-id="839d8-157">To move a module to a new position within your page, use any of the following methods.</span></span>

### <a name="move-a-module-using-the-outline-pane"></a><span data-ttu-id="839d8-158">アウトライン ウィンドウを使用したモジュールの移動</span><span class="sxs-lookup"><span data-stu-id="839d8-158">Move a module using the outline pane</span></span>

<span data-ttu-id="839d8-159">アウトライン ペインを使用してモジュールを移動するには、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="839d8-159">To move a module using the outline pane, follow these steps.</span></span>

1. <span data-ttu-id="839d8-160">アウトライン ウィンドウで移動するモジュールを選択したままにし、アウトラインの新しい位置にモジュールをドラッグします。</span><span class="sxs-lookup"><span data-stu-id="839d8-160">Select and hold the module you want to move in the outline pane, then drag the module to a new position in the outline.</span></span> <span data-ttu-id="839d8-161">アウトラインとキャンバスの青い線は、モジュールを配置できる場所を示します。</span><span class="sxs-lookup"><span data-stu-id="839d8-161">The blue line in the outline and on the canvas indicates where the module can be placed.</span></span>
1. <span data-ttu-id="839d8-162">モジュールを放して、新しい位置にドロップします。</span><span class="sxs-lookup"><span data-stu-id="839d8-162">Release the module to drop it into the new position.</span></span>

### <a name="move-a-module-directly-within-the-canvas"></a><span data-ttu-id="839d8-163">キャンバス内でのモジュールの直接移動</span><span class="sxs-lookup"><span data-stu-id="839d8-163">Move a module directly within the canvas</span></span>

<span data-ttu-id="839d8-164">キャンバスを使用してモジュールを直接移動するには、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="839d8-164">To move a module directly within the canvas, follow these steps.</span></span>

1. <span data-ttu-id="839d8-165">キャンバスで移動するモジュールを選択します。</span><span class="sxs-lookup"><span data-stu-id="839d8-165">Select the module you want to move in the canvas.</span></span> 
1. <span data-ttu-id="839d8-166">モジュールのツールバーで上向きまたは下向きの矢印記号を選択し、ページの新しい位置まで矢印をドラッグします。</span><span class="sxs-lookup"><span data-stu-id="839d8-166">Select either an upward or downward pointing arrow symbol in the module's toolbar, and then drag the arrow to a new position on the page.</span></span> <span data-ttu-id="839d8-167">キャンバスの青い線とアウトラインは、モジュールを配置できる場所を示します。</span><span class="sxs-lookup"><span data-stu-id="839d8-167">The blue line in the canvas and outline indicates where the module can be placed.</span></span> <span data-ttu-id="839d8-168">モジュールを上または下に移動できない場合、その矢印記号は淡色表示になります。</span><span class="sxs-lookup"><span data-stu-id="839d8-168">If a module cannot be moved up or down, that arrow symbol will be grayed out.</span></span> 
1. <span data-ttu-id="839d8-169">モジュールを放して、新しい位置にドロップします。</span><span class="sxs-lookup"><span data-stu-id="839d8-169">Release the module to drop it into the new position.</span></span>

### <a name="move-a-module-using-the-ellipsis-menu"></a><span data-ttu-id="839d8-170">省略記号メニューを使用したモジュールの移動</span><span class="sxs-lookup"><span data-stu-id="839d8-170">Move a module using the ellipsis menu</span></span>

<span data-ttu-id="839d8-171">省略記号メニューを使用してモジュールを移動するには、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="839d8-171">To move a module using the ellipsis menu, follow these steps.</span></span>

1. <span data-ttu-id="839d8-172">アウトラインまたはキャンバスのいずれかでモジュールを選択します。</span><span class="sxs-lookup"><span data-stu-id="839d8-172">Select a module in either the outline or the canvas.</span></span>
1. <span data-ttu-id="839d8-173">アウトライン ペイン、またはキャンバスのモジュールのツールバーで、モジュールの名前の横にある省略記号 (**...**) を選択します。</span><span class="sxs-lookup"><span data-stu-id="839d8-173">Select the ellipsis (**...**) next to the module's name in the outline pane, or in the module's toolbar in the canvas.</span></span>
1. <span data-ttu-id="839d8-174">コンテナーまたはスロット内でモジュールを上または下に移動できる場合は、**上に移動** または **下に移動** オプションが表示されます。</span><span class="sxs-lookup"><span data-stu-id="839d8-174">If the module can be moved up or down within the container or slot, you will see options for **Move up** or **Move down**.</span></span> <span data-ttu-id="839d8-175">兄弟を基準としてモジュールを上下に移動するには、目的の移動オプションを選択します。</span><span class="sxs-lookup"><span data-stu-id="839d8-175">Select the desired move option to move the module up or down relative to its siblings.</span></span>

## <a name="configure-modules"></a><span data-ttu-id="839d8-176">モジュールのコンフィギュレーション</span><span class="sxs-lookup"><span data-stu-id="839d8-176">Configure modules</span></span>

<span data-ttu-id="839d8-177">次の手順では、コンテンツおよびコンテナー モジュールをコンフィギュレーションする方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="839d8-177">The following procedures describe how to configure content and container modules.</span></span>

### <a name="configure-a-content-module"></a><span data-ttu-id="839d8-178">コンテンツ モジュールのコンフィギュレーション</span><span class="sxs-lookup"><span data-stu-id="839d8-178">Configure a content module</span></span>

<span data-ttu-id="839d8-179">ページでコンテンツ モジュールをコンフィギュレーションするには、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="839d8-179">To configure a content module on a page, follow these steps.</span></span>

1. <span data-ttu-id="839d8-180">左側のアウトライン ウィンドウで、ツリーを展開し、任意のコンテンツ モジュール (**コンテンツ ブロック** など) を選択します。</span><span class="sxs-lookup"><span data-stu-id="839d8-180">In the outline pane on the left, expand the tree and select any content module (for example, **Content block**).</span></span> <span data-ttu-id="839d8-181">または、メイン キャンバスでモジュールを選択できます。</span><span class="sxs-lookup"><span data-stu-id="839d8-181">Alternately, you can select the module in the main canvas.</span></span>
1. <span data-ttu-id="839d8-182">右側のモジュールのプロパティ ウィンドウで、必要なモジュール コントロールのプロパティを入力します。</span><span class="sxs-lookup"><span data-stu-id="839d8-182">In the module properties pane on the right, enter properties for any desired module controls.</span></span>
1. <span data-ttu-id="839d8-183">コマンド バーで、**保存** を選択します。</span><span class="sxs-lookup"><span data-stu-id="839d8-183">On the command bar, select **Save**.</span></span> <span data-ttu-id="839d8-184">これにより、プレビュー キャンバスも更新されます。</span><span class="sxs-lookup"><span data-stu-id="839d8-184">This will also refresh the preview canvas.</span></span>

### <a name="edit-module-text-properties"></a><span data-ttu-id="839d8-185">モジュール テキスト プロパティの編集</span><span class="sxs-lookup"><span data-stu-id="839d8-185">Edit module text properties</span></span>

<span data-ttu-id="839d8-186">読み取り専用ではないモジュール テキスト プロパティは、キャンバスで直接編集できます。</span><span class="sxs-lookup"><span data-stu-id="839d8-186">Module text properties that are not read-only can be edited directly in the canvas.</span></span>

<span data-ttu-id="839d8-187">モジュール テキストのプロパティを編集するには、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="839d8-187">To edit module text properties, follow these steps.</span></span>

1. <span data-ttu-id="839d8-188">キャンバスでテキスト コントロールを選択し、テキストを編集する場所にカーソルを置きます。</span><span class="sxs-lookup"><span data-stu-id="839d8-188">Select the text control in the canvas, then place your cursor where you wish to edit text.</span></span>
1. <span data-ttu-id="839d8-189">テキストの内容を入力します。</span><span class="sxs-lookup"><span data-stu-id="839d8-189">Enter your text content.</span></span>
1. <span data-ttu-id="839d8-190">他のコンテンツの編集を続けるには、テキスト コンテンツの外側の任意の場所を選択します。</span><span class="sxs-lookup"><span data-stu-id="839d8-190">Select anywhere outside the text content to continue editing other content.</span></span>

### <a name="inline-image-selection"></a><span data-ttu-id="839d8-191">インライン画像の選択</span><span class="sxs-lookup"><span data-stu-id="839d8-191">Inline image selection</span></span>

<span data-ttu-id="839d8-192">読み取り専用ではないモジュール画像は、キャンバスから直接編集できます。</span><span class="sxs-lookup"><span data-stu-id="839d8-192">Module images that are not read-only can be changed directly from the canvas.</span></span>

<span data-ttu-id="839d8-193">コンテンツ モジュールの新しい画像を選択するには、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="839d8-193">To choose a new image for a content module, follow these steps.</span></span>

1. <span data-ttu-id="839d8-194">キャンバスで、画像をダブルクリックします。</span><span class="sxs-lookup"><span data-stu-id="839d8-194">In the canvas, double-click the image.</span></span> <span data-ttu-id="839d8-195">メディア選択ウィンドウが開きます。</span><span class="sxs-lookup"><span data-stu-id="839d8-195">This will bring up the media picker window.</span></span>
1. <span data-ttu-id="839d8-196">使用する新しい画像を検索して選択し、**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="839d8-196">Find and select a new image you want to use, and then select **OK**.</span></span> <span data-ttu-id="839d8-197">キャンバスに新しい画像が表示されます。</span><span class="sxs-lookup"><span data-stu-id="839d8-197">The new image is now rendered in the canvas.</span></span>

### <a name="configure-a-container-module"></a><span data-ttu-id="839d8-198">コンテナー モジュールのコンフィギュレーション</span><span class="sxs-lookup"><span data-stu-id="839d8-198">Configure a container module</span></span>

<span data-ttu-id="839d8-199">ページでコンテナー モジュールをコンフィギュレーションするには、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="839d8-199">To configure a container module on a page, follow these steps.</span></span>

1. <span data-ttu-id="839d8-200">ページ上のコンテナー モジュールを選択します (カルーセルや流動的なコンテナー モジュールなど)。</span><span class="sxs-lookup"><span data-stu-id="839d8-200">Select a container module on your page (for example, a carousel or fluid container module).</span></span>
1. <span data-ttu-id="839d8-201">右側のプロパティ ウィンドウで、ヘッダーを選択して入れ子になったコントロールを展開し、必要なコントロール値を設定します。</span><span class="sxs-lookup"><span data-stu-id="839d8-201">In the properties pane on the right, expand the nested controls by selecting the headers, and set any required control values.</span></span>
1. <span data-ttu-id="839d8-202">左側のアウトライン ウィンドウで、コンテナーまたはコンテナー内のスロットいずれかの名前の横にある省略記号ボタンを選択し、**モジュールの追加** を選択します。</span><span class="sxs-lookup"><span data-stu-id="839d8-202">In the outline pane on the left, select the ellipsis button next to the name of either the container or any slots inside the container, and then select **Add Module**.</span></span> <span data-ttu-id="839d8-203">次に、選択したコンテナーに子モジュールを追加します。</span><span class="sxs-lookup"><span data-stu-id="839d8-203">Then, add child modules to the selected container.</span></span> <span data-ttu-id="839d8-204">詳細については、このトピックで前述した [モジュールの使用](#add-a-module) セクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="839d8-204">For more information, see the [Work with modules](#add-a-module) section earlier in this topic.</span></span>
1. <span data-ttu-id="839d8-205">複数の子モジュールが親コンテナーで兄弟として存在する場合は、親コンテナーでの表示順序を変更できます。</span><span class="sxs-lookup"><span data-stu-id="839d8-205">If multiple child modules exist as siblings in a parent container, you can change their display order in the parent container.</span></span> <span data-ttu-id="839d8-206">モジュールの省略記号ボタンを選択し、上矢印ボタンと下矢印ボタンを使用します。</span><span class="sxs-lookup"><span data-stu-id="839d8-206">Select the ellipsis button for a module, and then use the up arrow and down arrow buttons.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="839d8-207">追加リソース</span><span class="sxs-lookup"><span data-stu-id="839d8-207">Additional resources</span></span>

[<span data-ttu-id="839d8-208">テンプレートとレイアウトの概要</span><span class="sxs-lookup"><span data-stu-id="839d8-208">Templates and layouts overview</span></span>](templates-layouts-overview.md)

[<span data-ttu-id="839d8-209">テンプレートの使用</span><span class="sxs-lookup"><span data-stu-id="839d8-209">Work with templates</span></span>](work-with-templates.md)

[<span data-ttu-id="839d8-210">プリセット レイアウトの使用</span><span class="sxs-lookup"><span data-stu-id="839d8-210">Work with preset layouts</span></span>](work-with-layouts.md)

[<span data-ttu-id="839d8-211">フラグメントで動作</span><span class="sxs-lookup"><span data-stu-id="839d8-211">Work with fragments</span></span>](work-with-fragments.md)

[<span data-ttu-id="839d8-212">コンテナー モジュールをページに追加する</span><span class="sxs-lookup"><span data-stu-id="839d8-212">Add a container module to a page</span></span>](add-container-module.md)

[<span data-ttu-id="839d8-213">公開グループの作業</span><span class="sxs-lookup"><span data-stu-id="839d8-213">Work with publish groups</span></span>](publish-groups.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]
