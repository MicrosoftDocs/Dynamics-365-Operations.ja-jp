---
title: モジュールで動作
description: このトピックでは、Microsoft Dynamics 365 Commerce でモジュールを使用する時期と方法について説明します。
author: v-chgri
manager: annbe
ms.date: 01/31/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.search.region: Global
ms.search.industry: ''
ms.author: phinneyridge
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 769d6754fa944830b989d657e0dad9cc42212932
ms.sourcegitcommit: 829329220475ed8cff5a5db92a59dd90c22b04fa
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/05/2020
ms.locfileid: "3025882"
---
# <a name="work-with-modules"></a><span data-ttu-id="eba1e-103">モジュールで動作</span><span class="sxs-lookup"><span data-stu-id="eba1e-103">Work with modules</span></span>

<span data-ttu-id="eba1e-104">このトピックでは、Microsoft Dynamics 365 Commerce でモジュールを使用する時期と方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="eba1e-104">This topic describes how and when to use modules in Microsoft Dynamics 365 Commerce.</span></span>


[!include [banner](includes/banner.md)]

## <a name="overview"></a><span data-ttu-id="eba1e-105">概要</span><span class="sxs-lookup"><span data-stu-id="eba1e-105">Overview</span></span>

<span data-ttu-id="eba1e-106">モジュールは、ページ構造を構成する論理構成要素であり、さまざまな目的と範囲があります。</span><span class="sxs-lookup"><span data-stu-id="eba1e-106">Modules are logical building blocks that make up your page structure, and they have various purposes and scopes.</span></span> <span data-ttu-id="eba1e-107">一部のモジュールは上位レベルのコンテナーであり、その唯一の目的は、他のモジュール (子モジュール) を保持して整理することです。</span><span class="sxs-lookup"><span data-stu-id="eba1e-107">Some modules are high-level containers, and their only purpose is to hold and organize other modules (child modules).</span></span> <span data-ttu-id="eba1e-108">単純なイメージ配置モジュールなど、その他のモジュールには、特定の目的があります。</span><span class="sxs-lookup"><span data-stu-id="eba1e-108">Other modules, such as a simple image placement module, have a very specific purpose.</span></span> <span data-ttu-id="eba1e-109">カルーセル モジュールなど、その他のモジュールは、これら 2 つのカテゴリの間に含まれます。</span><span class="sxs-lookup"><span data-stu-id="eba1e-109">Other modules, such as a carousel module, fall somewhere between those two categories.</span></span>

<span data-ttu-id="eba1e-110">既定では、Dynamics 365 Commerce のサイトには、もっとも基本的な E コマースのシナリオを実現できるスターター キット モジュール ライブラリが含まれています。</span><span class="sxs-lookup"><span data-stu-id="eba1e-110">By default, your Dynamics 365 Commerce site includes a starter kit module library that lets you achieve most basic e-Commerce scenarios.</span></span> <span data-ttu-id="eba1e-111">これらのモジュールを使用するだけで、エンド ツー エンドの E コマースサイトを構築できます。</span><span class="sxs-lookup"><span data-stu-id="eba1e-111">You should be able to construct an end-to-end e-Commerce site just by using these modules.</span></span> <span data-ttu-id="eba1e-112">ただし、特定のニーズに合わせて、これらのモジュールをカスタマイズしたり、新しいカスタム モジュールを作成したりすることが必要な場合もあります。</span><span class="sxs-lookup"><span data-stu-id="eba1e-112">However, you might also want to customize these modules or build new, custom modules for specific needs.</span></span> <span data-ttu-id="eba1e-113">カスタム モジュールを作成する場合は、モジュール デザイン ソフトウェア開発キット (SDK) を使用して、カスタム モジュール ライブラリを作成できます。</span><span class="sxs-lookup"><span data-stu-id="eba1e-113">If you want to build custom modules, a module design software development kit (SDK) is available to help you create a custom module library.</span></span>

## <a name="container-modules-and-slots"></a><span data-ttu-id="eba1e-114">コンテナー モジュールとスロット</span><span class="sxs-lookup"><span data-stu-id="eba1e-114">Container modules and slots</span></span>

<span data-ttu-id="eba1e-115">既に説明したように、一部のモジュールは、子モジュールを保持するように設計されています。</span><span class="sxs-lookup"><span data-stu-id="eba1e-115">As was mentioned earlier, some modules are designed to hold child modules.</span></span> <span data-ttu-id="eba1e-116">これらのモジュールは*コンテナー*と呼ばれ、入れ子になったモジュールの階層を許可します。</span><span class="sxs-lookup"><span data-stu-id="eba1e-116">These modules are known as *containers*, and they allow for hierarchies of nested modules.</span></span> <span data-ttu-id="eba1e-117">コンテナー モジュールは*スロット*を含みます。</span><span class="sxs-lookup"><span data-stu-id="eba1e-117">Container modules include *slots*.</span></span> <span data-ttu-id="eba1e-118">スロットは、コンテナー内の子モジュールのレイアウトと目的を処理するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="eba1e-118">Slots are used to handle the layout and purpose of child modules in the container.</span></span> <span data-ttu-id="eba1e-119">たとえば、いくつかの重要なスロットを定義する基本的なページ コンテナー モジュール (すべてのページでトップレベルのモジュール) があります。</span><span class="sxs-lookup"><span data-stu-id="eba1e-119">An example is a basic page container module (a top-level module for any page) that defines several important slots:</span></span>

- <span data-ttu-id="eba1e-120">ヘッダー スロット</span><span class="sxs-lookup"><span data-stu-id="eba1e-120">A header slot</span></span>
- <span data-ttu-id="eba1e-121">本文スロット</span><span class="sxs-lookup"><span data-stu-id="eba1e-121">A body slot</span></span>
- <span data-ttu-id="eba1e-122">フッター スロット</span><span class="sxs-lookup"><span data-stu-id="eba1e-122">A footer slot</span></span>

<span data-ttu-id="eba1e-123">モジュールの開発者はこれらのスロットを定義し、子モジュールとそれに直接入れることができる子モジュールの数を決定します。</span><span class="sxs-lookup"><span data-stu-id="eba1e-123">The module's developer defines these slots, and determines which child modules and how many child modules can be put directly inside it.</span></span> <span data-ttu-id="eba1e-124">たとえば、ヘッダー スロットは**ヘッダー モジュール**タイプのモジュールを 1 つだけサポートするのに対して、本文スロットはすべてのタイプのモジュールを無制限にサポートすることができます (他のページのコンテナー モジュールを除く)。</span><span class="sxs-lookup"><span data-stu-id="eba1e-124">For example, the header slot might support only one module of the **Header Module** type, whereas the body slot might support an unlimited number of modules of any type (except other page container modules).</span></span>

<span data-ttu-id="eba1e-125">作成ツールでは、ページの作成者は、どのモジュールを各スロットに配置できるか/できないかをあらかじめ把握している必要はありません。</span><span class="sxs-lookup"><span data-stu-id="eba1e-125">In the authoring tools, page authors don't have to know in advance which modules can and can't be put in each slot.</span></span> <span data-ttu-id="eba1e-126">ページの作成者がスロットを選択し、そのスロットに追加するモジュールを選択しようとすると、そのスロットでサポートされているモジュールのタイプがフィルター処理されて表示されます。</span><span class="sxs-lookup"><span data-stu-id="eba1e-126">When page authors select a slot and then try to select a module to add to it, they see a filtered view of module types that are supported for that slot.</span></span>

## <a name="content-modules"></a><span data-ttu-id="eba1e-127">コンテンツ モジュール</span><span class="sxs-lookup"><span data-stu-id="eba1e-127">Content modules</span></span>

<span data-ttu-id="eba1e-128">コンテンツ モジュールには、テキスト (ヘッドライン、段落、リンクなど) または資産参照 (画像、ビデオ、PDF など) といったコンテンツやメディア要素が含まれます。</span><span class="sxs-lookup"><span data-stu-id="eba1e-128">Content modules contain content and media elements, such as text (for example, headlines, paragraphs, and links) or asset references (for example, images, video, and PDFs).</span></span> <span data-ttu-id="eba1e-129">一般的なコンテンツ モジュール タイプの例として、**ヒーロー**、**フィーチャー**、**バナー**があります。</span><span class="sxs-lookup"><span data-stu-id="eba1e-129">Examples of typical content module types are **Hero**, **Feature**, and **Banner**.</span></span> <span data-ttu-id="eba1e-130">これら 3 つのタイプのモジュールには、テキストまたはメディアを含めることができます。また、ページ上に表示されないようにするために、子モジュールを使用する必要はありません。</span><span class="sxs-lookup"><span data-stu-id="eba1e-130">Modules of these three types can contain text or media, and they don't require any child modules to make something visible on a page.</span></span>

<span data-ttu-id="eba1e-131">一般的な日々のページとコンテンツ作成活動の大部分は、コンテンツ モジュールに関連しています。主には、これらのモジュールが親コンテナー モジュールに表示される実際のコンテンツを定義するためです。</span><span class="sxs-lookup"><span data-stu-id="eba1e-131">The majority of typical, day-to-day page and content authoring activities involve content modules, primarily because these modules define the actual content that is rendered in their parent container modules.</span></span> <span data-ttu-id="eba1e-132">多くのコンテンツ モジュールが使用可能で、これらのモジュールは通常、入れ子になったモジュールのページ階層に追加する最後のピースになります。</span><span class="sxs-lookup"><span data-stu-id="eba1e-132">Many content modules are available, and these modules are typically the last pieces that you will add to a page's hierarchy of nested modules.</span></span>

<span data-ttu-id="eba1e-133">次の図は、モジュールが親コンテナー モジュール スロットの中でどのように入れ子になるかを示しています。</span><span class="sxs-lookup"><span data-stu-id="eba1e-133">The following illustration shows how modules are nested inside parent container module slots.</span></span>

![入れ子のモジュール](../commerce/media/basic-module-nesting.png)

## <a name="add-or-remove-modules"></a><span data-ttu-id="eba1e-135">モジュールの追加または削除</span><span class="sxs-lookup"><span data-stu-id="eba1e-135">Add or remove modules</span></span>

<span data-ttu-id="eba1e-136">次の手順では、モジュールを追加および削除する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="eba1e-136">The following procedures describe how to add and remove modules.</span></span>

### <a name="add-a-module"></a><span data-ttu-id="eba1e-137">モジュールの追加</span><span class="sxs-lookup"><span data-stu-id="eba1e-137">Add a module</span></span>

<span data-ttu-id="eba1e-138">ページ上のスロットまたはコンテナーにモジュールを追加するには、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="eba1e-138">To add a module to a slot or container on a page, follow these steps.</span></span>

1. <span data-ttu-id="eba1e-139">左側のアウトライン ウィンドウで、子モジュールを追加できるコンテナーまたはスロットを選択します。</span><span class="sxs-lookup"><span data-stu-id="eba1e-139">In the outline pane on the left, select a container or slot that a child module can be added to.</span></span>

    > [!NOTE]
    > <span data-ttu-id="eba1e-140">モジュール デザイナーは、特定のモジュール スロットに追加できるモジュール タイプのリストを定義します。</span><span class="sxs-lookup"><span data-stu-id="eba1e-140">The module designer defines the list of modules types that can be added to a specific module slot.</span></span> <span data-ttu-id="eba1e-141">テンプレートの作成者は、使用可能なモジュール オプションを調整して一貫性のある検索エンジン最適化 (SEO) を実現し、特定のテンプレートから作成されたすべてのページの作成効率を高めることができます。</span><span class="sxs-lookup"><span data-stu-id="eba1e-141">Template authors can then refine the allowed module options to help guarantee consistent search engine optimization (SEO) and authoring efficiency for all the pages pages that are built from a specific template.</span></span>

1. <span data-ttu-id="eba1e-142">モジュールの省略記号ボタン (**...**) を選択し、**モジュールの追加**を選択します。</span><span class="sxs-lookup"><span data-stu-id="eba1e-142">Select the ellipsis button (**...**) for the module, and then select **Add Module**.</span></span> <span data-ttu-id="eba1e-143">**モジュールの追加**ダイアログ ボックスが表示されます。</span><span class="sxs-lookup"><span data-stu-id="eba1e-143">The **Add Module** dialog box appears.</span></span> <span data-ttu-id="eba1e-144">このダイアログ ボックスは自動的にフィルター処理され、選択したコンテナーまたはスロットでサポートされているモジュールのみが表示されます。</span><span class="sxs-lookup"><span data-stu-id="eba1e-144">This dialog box is automatically filtered so that it shows only modules that are supported in the selected container or slot.</span></span> <span data-ttu-id="eba1e-145">モジュールの一覧は、ページのテンプレートまたはコンテナー モジュールの定義によって決まります。</span><span class="sxs-lookup"><span data-stu-id="eba1e-145">The list of modules is determined by the page's template or the container module definition.</span></span>

    > [!NOTE]
    > <span data-ttu-id="eba1e-146">コンテナーまたはスロットが新しい子モジュールをサポートしていない場合、**モジュールの追加**オプションは使用できません。</span><span class="sxs-lookup"><span data-stu-id="eba1e-146">If a container or slot doesn't support new child modules, the **Add Module** option is unavailable.</span></span>

1. <span data-ttu-id="eba1e-147">ダイアログ ボックスで、ページに追加するモジュールを検索して選択します。</span><span class="sxs-lookup"><span data-stu-id="eba1e-147">In the dialog box, search for and select a module to add to your page.</span></span>

    > [!TIP]
    > <span data-ttu-id="eba1e-148">**フィーチャー**と**ヒーロー**は、初心者が使用するのに適したモジュール タイプです。</span><span class="sxs-lookup"><span data-stu-id="eba1e-148">**Feature** and **Hero** are good module types for beginners to work with.</span></span>

1. <span data-ttu-id="eba1e-149">**OK** をクリックすると、選択したモジュールがページ内で選択したコンテナーまたはスロットに追加されます。</span><span class="sxs-lookup"><span data-stu-id="eba1e-149">Select **OK** to add the selected module to the selected container or slot on your page.</span></span>

### <a name="remove-a-module"></a><span data-ttu-id="eba1e-150">モジュールの削除</span><span class="sxs-lookup"><span data-stu-id="eba1e-150">Remove a module</span></span>

<span data-ttu-id="eba1e-151">ページ上のスロットまたはコンテナーからモジュールを削除するには、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="eba1e-151">To remove a module from a slot or container on a page, follow these steps.</span></span>

1. <span data-ttu-id="eba1e-152">左のアウトライン ウィンドウで、削除するモジュールの名前の横にある省略記号ボタンを選択し、ごみ箱ボタンを選択します。</span><span class="sxs-lookup"><span data-stu-id="eba1e-152">In the outline pane on the left, select the ellipsis button next to the name of the module to remove, and then select the trash can button.</span></span>
1. <span data-ttu-id="eba1e-153">モジュールを削除するかどうかを確認するメッセージが表示されたら、**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="eba1e-153">When you're prompted to confirm that you want to remove the module, select **OK**.</span></span>

## <a name="configure-modules"></a><span data-ttu-id="eba1e-154">モジュールのコンフィギュレーション</span><span class="sxs-lookup"><span data-stu-id="eba1e-154">Configure modules</span></span>

<span data-ttu-id="eba1e-155">次の手順では、コンテンツおよびコンテナー モジュールをコンフィギュレーションする方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="eba1e-155">The following procedures describe how to configure content and container modules.</span></span>

### <a name="configure-a-content-module"></a><span data-ttu-id="eba1e-156">コンテンツ モジュールのコンフィギュレーション</span><span class="sxs-lookup"><span data-stu-id="eba1e-156">Configure a content module</span></span>

<span data-ttu-id="eba1e-157">ページでコンテンツ モジュールをコンフィギュレーションするには、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="eba1e-157">To configure a content module on a page, follow these steps.</span></span>

1. <span data-ttu-id="eba1e-158">左側のアウトライン ウィンドウで、ツリーを展開し、任意のコンテンツ モジュール (**フィーチャー**、**ヒーロー**、**バナー**など) を選択します。</span><span class="sxs-lookup"><span data-stu-id="eba1e-158">In the outline pane on the left, expand the tree and select any content module (for example, **Feature**, **Hero**, or **Banner**).</span></span>
1. <span data-ttu-id="eba1e-159">右のプロパティ ウィンドウで、モジュールのコンテンツおよび設定コントロールを検索します。</span><span class="sxs-lookup"><span data-stu-id="eba1e-159">In the properties pane on the right, find the module's content and settings controls.</span></span>
1. <span data-ttu-id="eba1e-160">目的のモジュール コントロールのプロパティを入力します。</span><span class="sxs-lookup"><span data-stu-id="eba1e-160">Enter properties for any desired module controls.</span></span>
1. <span data-ttu-id="eba1e-161">コマンド バーで、**保存**を選択します。</span><span class="sxs-lookup"><span data-stu-id="eba1e-161">Select **Save** in the command bar.</span></span> <span data-ttu-id="eba1e-162">これにより、プレビュー キャンバスも更新されます。</span><span class="sxs-lookup"><span data-stu-id="eba1e-162">This will also refresh the preview canvas.</span></span>

### <a name="configure-a-container-module"></a><span data-ttu-id="eba1e-163">コンテナー モジュールのコンフィギュレーション</span><span class="sxs-lookup"><span data-stu-id="eba1e-163">Configure a container module</span></span>

<span data-ttu-id="eba1e-164">ページでコンテナー モジュールをコンフィギュレーションするには、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="eba1e-164">To configure a container module on a page, follow these steps.</span></span>

1. <span data-ttu-id="eba1e-165">ページ上のコンテナー モジュールを選択します (カルーセルや流動的なコンテナー モジュールなど)。</span><span class="sxs-lookup"><span data-stu-id="eba1e-165">Select a container module on your page (for example, a carousel or fluid container module).</span></span>
1. <span data-ttu-id="eba1e-166">右側のプロパティ ウィンドウで、ヘッダーを選択して入れ子になったコントロールを展開し、必要なコントロール値を設定します。</span><span class="sxs-lookup"><span data-stu-id="eba1e-166">In the properties pane on the right, expand the nested controls by selecting the headers, and set any required control values.</span></span>
1. <span data-ttu-id="eba1e-167">左側のアウトライン ウィンドウで、コンテナーまたはコンテナー内のスロットいずれかの名前の横にある省略記号ボタンを選択し、**モジュールの追加**を選択します。</span><span class="sxs-lookup"><span data-stu-id="eba1e-167">In the outline pane on the left, select the ellipsis button next to the name of either the container or any slots inside the container, and then select **Add Module**.</span></span> <span data-ttu-id="eba1e-168">次に、選択したコンテナーに子モジュールを追加します。</span><span class="sxs-lookup"><span data-stu-id="eba1e-168">Then, add child modules to the selected container.</span></span> <span data-ttu-id="eba1e-169">詳細については、このトピックで前述した [モジュールの使用](#add-a-module) セクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="eba1e-169">For more information, see the [Work with modules](#add-a-module) section earlier in this topic.</span></span>
1. <span data-ttu-id="eba1e-170">複数の子モジュールが親コンテナーで兄弟として存在する場合は、親コンテナーでの表示順序を変更できます。</span><span class="sxs-lookup"><span data-stu-id="eba1e-170">If multiple child modules exist as siblings in a parent container, you can change their display order in the parent container.</span></span> <span data-ttu-id="eba1e-171">モジュールの省略記号ボタンを選択し、上矢印ボタンと下矢印ボタンを使用します。</span><span class="sxs-lookup"><span data-stu-id="eba1e-171">Select the ellipsis button for a module, and then use the up arrow and down arrow buttons.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="eba1e-172">追加リソース</span><span class="sxs-lookup"><span data-stu-id="eba1e-172">Additional resources</span></span>

[<span data-ttu-id="eba1e-173">テンプレートとレイアウトの概要</span><span class="sxs-lookup"><span data-stu-id="eba1e-173">Templates and layouts overview</span></span>](templates-layouts-overview.md)

[<span data-ttu-id="eba1e-174">テンプレートの使用</span><span class="sxs-lookup"><span data-stu-id="eba1e-174">Work with templates</span></span>](work-with-templates.md)

[<span data-ttu-id="eba1e-175">プリセット レイアウトの使用</span><span class="sxs-lookup"><span data-stu-id="eba1e-175">Work with preset layouts</span></span>](work-with-layouts.md)

[<span data-ttu-id="eba1e-176">フラグメントで動作</span><span class="sxs-lookup"><span data-stu-id="eba1e-176">Work with fragments</span></span>](work-with-fragments.md)

[<span data-ttu-id="eba1e-177">コンテナー モジュールをページに追加する</span><span class="sxs-lookup"><span data-stu-id="eba1e-177">Add a container module to a page</span></span>](add-container-module.md)

[<span data-ttu-id="eba1e-178">公開グループの作業</span><span class="sxs-lookup"><span data-stu-id="eba1e-178">Work with publish groups</span></span>](publish-groups.md)

