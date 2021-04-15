---
title: テンプレートの使用
description: このトピックでは、Microsoft Dynamics 365 Commerce でのテンプレートの使用方法について説明します。
author: phinneyridge
ms.date: 04/14/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.region: Global
ms.search.industry: ''
ms.author: niholman
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 96a8cbfd208095833514f374c060bb2d43781913
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/31/2021
ms.locfileid: "5793852"
---
# <a name="work-with-templates"></a><span data-ttu-id="e7f15-103">テンプレートの使用</span><span class="sxs-lookup"><span data-stu-id="e7f15-103">Work with templates</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="e7f15-104">このトピックでは、Microsoft Dynamics 365 Commerce でのテンプレートの使用方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="e7f15-104">This topic describes how to work with templates in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="e7f15-105">[テンプレートとレイアウトの概要](templates-layouts-overview.md)で説明したように、テンプレートは、下流の作成者が使用できる一連のオプションを定義します。</span><span class="sxs-lookup"><span data-stu-id="e7f15-105">As was discussed in [Templates and layouts overview](templates-layouts-overview.md), templates define the set of options that is available to downstream authors.</span></span> <span data-ttu-id="e7f15-106">テンプレートは企業の Web 作成チームにとってさまざまな理由から役に立ちます。適切なテンプレートを使用することで、次の目標を達成できます。</span><span class="sxs-lookup"><span data-stu-id="e7f15-106">Templates are useful to an enterprise's web authoring team for several reasons, and well-structured templates can help with all the following goals:</span></span>

- <span data-ttu-id="e7f15-107">日々のコンテンツ編集者の役割において、作成エクスペリエンスを簡略化します。</span><span class="sxs-lookup"><span data-stu-id="e7f15-107">Simplify the authoring experience for day-to-day content editor roles.</span></span>

    - <span data-ttu-id="e7f15-108">モジュール オプションをフィルター処理して、特定のページ セクションに関連モジュールのみを表示します。</span><span class="sxs-lookup"><span data-stu-id="e7f15-108">Filter module options so that only relevant modules are shown for a specific page section.</span></span> <span data-ttu-id="e7f15-109">(たとえば、テンプレートのマーケティング セクションをコンフィギュレーションして、そのコンテキストでは使用しない不適切なモジュールをフィルター処理し、表示されている場合はコンテンツの作成タスクを複雑化します。)</span><span class="sxs-lookup"><span data-stu-id="e7f15-109">(For example, a marketing section of a template can be configured to filter out irrelevant modules that should never be used in that context, and that will just complicate content authoring tasks if they are shown.)</span></span>
    - <span data-ttu-id="e7f15-110">既定のモジュール設定をコンフィギュレーションして、作成の効率を高めます。</span><span class="sxs-lookup"><span data-stu-id="e7f15-110">Configure default module setting to help improve authoring efficiency.</span></span>
    - <span data-ttu-id="e7f15-111">既定のページ フラグメントを定義して、作成の効率を高めます。</span><span class="sxs-lookup"><span data-stu-id="e7f15-111">Define default page fragments to help improve authoring efficiency.</span></span> <span data-ttu-id="e7f15-112">(たとえば、テンプレートのヘッダーおよびフッター フラグメントは、下流のページすべてで自動的に表示されます。)</span><span class="sxs-lookup"><span data-stu-id="e7f15-112">(For example, header and footer fragments in a template will automatically appear on every downstream page.)</span></span>

- <span data-ttu-id="e7f15-113">承認済の一連のモジュール配置およびコンフィギュレーション オプションを定義することで、企業のサイトをブランド イメージに沿ったものに保ちます。</span><span class="sxs-lookup"><span data-stu-id="e7f15-113">Keep enterprise sites on-brand by defining an approved set of module arrangement and configuration options.</span></span>

    > [!TIP] 
    > <span data-ttu-id="e7f15-114">成功している E コマース サイトには、顧客になじみがあり、反復可能で、ブランドイメージに沿ったユーザー エクスペリエンス (UX) デザイン パターンがあります。</span><span class="sxs-lookup"><span data-stu-id="e7f15-114">Successful e-Commerce sites provide customers with familiar, repeatable, and on-brand user experience (UX) design patterns.</span></span> <span data-ttu-id="e7f15-115">テンプレートを使用すると、サイト全体の一貫性を制御するのに役立ちます。</span><span class="sxs-lookup"><span data-stu-id="e7f15-115">By using templates, you help control consistency across your site.</span></span>

- <span data-ttu-id="e7f15-116">反復可能でプログラムによって定義された、ページ定義およびメタデータを確認して、検索エンジン最適化 (SEO) スコアを向上させます。</span><span class="sxs-lookup"><span data-stu-id="e7f15-116">Improve search engine optimization (SEO) scores by ensuring repeatable and programmatically defined page definitions and metadata.</span></span>

> [!NOTE]
> <span data-ttu-id="e7f15-117">テンプレートはサイト全体の整合性を制御するように設計されていますが、理論的には、一貫性を強要しないようにコンフィギュレーションすることができます。</span><span class="sxs-lookup"><span data-stu-id="e7f15-117">Although templates are designed to control consistency across a site, they can theoretically be configured so that they don't enforce any consistency.</span></span> <span data-ttu-id="e7f15-118">ブランドとサイトの管理者は、サイトのページの可変性レベルを定義できます。</span><span class="sxs-lookup"><span data-stu-id="e7f15-118">Brand and site administrators can define any level of variability for the pages on their site.</span></span> <span data-ttu-id="e7f15-119">たとえば、テンプレートを完全に開いたままにすると、コンテンツ作成者が選択したページ デザインを作成できるようになります。</span><span class="sxs-lookup"><span data-stu-id="e7f15-119">For example, a template can be left entirely open, so that content authors can create any page design that they choose.</span></span> <span data-ttu-id="e7f15-120">この場合、上記のどの利点も適用されません。</span><span class="sxs-lookup"><span data-stu-id="e7f15-120">In this case, none of the benefits in the preceding list are applicable.</span></span>

## <a name="modify-a-template"></a><span data-ttu-id="e7f15-121">テンプレートの変更</span><span class="sxs-lookup"><span data-stu-id="e7f15-121">Modify a template</span></span>

<span data-ttu-id="e7f15-122">テンプレートは、テンプレート エディターを使用して変更できます。</span><span class="sxs-lookup"><span data-stu-id="e7f15-122">Templates are modified by using the template editor.</span></span>

<span data-ttu-id="e7f15-123">テンプレート エディターを開くには、次の手順のいずれかに従います。</span><span class="sxs-lookup"><span data-stu-id="e7f15-123">To open the template editor, follow one of these steps:</span></span>

- <span data-ttu-id="e7f15-124">サイトのナビゲーション ウィンドウで、**テンプレート** を選択し、変更するテンプレートを選択します。</span><span class="sxs-lookup"><span data-stu-id="e7f15-124">In the navigation pane of your site, select **Templates**, and then select the template to modify.</span></span>
- <span data-ttu-id="e7f15-125">既存のページのページ エディターで、左側のアウトライン ツリーのトップ ノードを選択します。</span><span class="sxs-lookup"><span data-stu-id="e7f15-125">In the page editor for an existing page, select the top node in the outline tree on the left.</span></span> <span data-ttu-id="e7f15-126">次に、右のプロパティ ウィンドウで、**テンプレートの編集** を選択します。</span><span class="sxs-lookup"><span data-stu-id="e7f15-126">Then, in the property pane on the right, select **Edit Template**.</span></span>

<span data-ttu-id="e7f15-127">左側のアウトライン ツリー ビューには、子レイアウトとページで使用できるモジュール オプションと構造が表示されます。</span><span class="sxs-lookup"><span data-stu-id="e7f15-127">The outline tree view on the left shows the module options and structures that are available to child layouts and pages.</span></span> <span data-ttu-id="e7f15-128">アウトライン ツリーでモジュールを選択すると、選択したモジュールのテンプレート プロパティが右側のプロパティ ウィンドウに表示されます。</span><span class="sxs-lookup"><span data-stu-id="e7f15-128">When you select a module in the outline tree, you can view the template properties for the selected module in the property pane on the right.</span></span> <span data-ttu-id="e7f15-129">これらのプロパティの一部は、テンプレート編集に固有です。</span><span class="sxs-lookup"><span data-stu-id="e7f15-129">Some of these properties are unique to template editing.</span></span> <span data-ttu-id="e7f15-130">次のテーブルにこれらのプロパティを示します。</span><span class="sxs-lookup"><span data-stu-id="e7f15-130">The following table describes these properties.</span></span>

| <span data-ttu-id="e7f15-131">プロパティ名</span><span class="sxs-lookup"><span data-stu-id="e7f15-131">Property name</span></span> | <span data-ttu-id="e7f15-132">説明</span><span class="sxs-lookup"><span data-stu-id="e7f15-132">Description</span></span> |
|---|---|
| <span data-ttu-id="e7f15-133">最小発生数</span><span class="sxs-lookup"><span data-stu-id="e7f15-133">Min Occurs</span></span> | <span data-ttu-id="e7f15-134">このプロパティは、選択されたモジュールの最小発生数を定義します。</span><span class="sxs-lookup"><span data-stu-id="e7f15-134">This property defines the minimum number of occurrences for the selected module.</span></span> <span data-ttu-id="e7f15-135">たとえば、値が **1** に設定されている場合、モジュールは下流の作成者に対して必要ですが、値が **0** (ゼロ) に設定されている場合、モジュールはオプションです。</span><span class="sxs-lookup"><span data-stu-id="e7f15-135">For example, if the value is set to **1**, the module is required for downstream authors, whereas if the value is set to **0** (zero), the module is optional.</span></span> |
| <span data-ttu-id="e7f15-136">最大発生数</span><span class="sxs-lookup"><span data-stu-id="e7f15-136">Max Occurs</span></span> | <span data-ttu-id="e7f15-137">このプロパティは、選択されたモジュールの最大発生数を定義します。</span><span class="sxs-lookup"><span data-stu-id="e7f15-137">This property defines the maximum number of occurrences for the selected module.</span></span> <span data-ttu-id="e7f15-138">たとえば、この値が **1** に設定されている場合、モジュールを追加できるのは 1 回だけです。</span><span class="sxs-lookup"><span data-stu-id="e7f15-138">For example, if the value is set to **1**, the module can be added only one time.</span></span> |
| <span data-ttu-id="e7f15-139">最小モジュール (コンテナー)</span><span class="sxs-lookup"><span data-stu-id="e7f15-139">Min Modules (Containers)</span></span> | <span data-ttu-id="e7f15-140">他のモジュールを含むモジュール (つまり、*コンテナーモジュール*) では、このプロパティは子として追加する必要があるモジュール総数の最小数を定義します。</span><span class="sxs-lookup"><span data-stu-id="e7f15-140">For modules that contain other modules (that is, for *containers modules*), this property defines the minimum number of total modules that should be added as children.</span></span> <span data-ttu-id="e7f15-141">たとえば、カルーセル モジュールでは、値が 1 より大きい数値に設定されている場合があります。</span><span class="sxs-lookup"><span data-stu-id="e7f15-141">For example, for a carousel module, the value might be set to a number that is more than 1.</span></span> |
| <span data-ttu-id="e7f15-142">最大モジュール (コンテナー)</span><span class="sxs-lookup"><span data-stu-id="e7f15-142">Max Modules (Containers)</span></span> | <span data-ttu-id="e7f15-143">コンテナー モジュールの場合、このプロパティは子として追加する必要があるモジュール総数の最大値を定義します。</span><span class="sxs-lookup"><span data-stu-id="e7f15-143">For container modules, this property defines the maximum number of total modules that should be added as children.</span></span> <span data-ttu-id="e7f15-144">たとえば、カルーセル モジュールでは、値が 10 より小さい数値に設定されている場合があります。</span><span class="sxs-lookup"><span data-stu-id="e7f15-144">For example, for a carousel module, the value might be set to a number that is less than 10.</span></span> |
| <span data-ttu-id="e7f15-145">ロック済</span><span class="sxs-lookup"><span data-stu-id="e7f15-145">Locked</span></span> | <span data-ttu-id="e7f15-146">**ロック済** のブール コントロールは、すべてのコア モジュール プロパティの横に表示されます。</span><span class="sxs-lookup"><span data-stu-id="e7f15-146">A **Locked** Boolean control appears next to all core module properties.</span></span> <span data-ttu-id="e7f15-147">これにより、テンプレート作成者はテンプレートのモジュール設定をロックできます。</span><span class="sxs-lookup"><span data-stu-id="e7f15-147">It lets the template author lock a module setting in the template.</span></span> <span data-ttu-id="e7f15-148">ロック済のモジュールの設定は、子レイアウトまたはページで上書きすることはできません。</span><span class="sxs-lookup"><span data-stu-id="e7f15-148">A module setting that is locked can't be overridden by any child layouts or pages.</span></span> <span data-ttu-id="e7f15-149">このテンプレートを使用するすべてのレイアウトとページで、一括編集可能なプロパティ値になります。</span><span class="sxs-lookup"><span data-stu-id="e7f15-149">It becomes a centrally editable property value for all layouts and pages that use the template.</span></span> |

## <a name="create-a-new-template"></a><span data-ttu-id="e7f15-150">新しいテンプレートを作成</span><span class="sxs-lookup"><span data-stu-id="e7f15-150">Create a new template</span></span>

<span data-ttu-id="e7f15-151">新しいテンプレートを作成するには、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="e7f15-151">To create a new template, follow these steps.</span></span>

1. <span data-ttu-id="e7f15-152">サイトのナビゲーション ウィンドウで、**テンプレート** を選択し、テンプレート インスペクター ビューを開きます。</span><span class="sxs-lookup"><span data-stu-id="e7f15-152">In the navigation pane of your site, select **Templates** to open the template inspector view.</span></span>
1. <span data-ttu-id="e7f15-153">**新しいテンプレート** を選択します。</span><span class="sxs-lookup"><span data-stu-id="e7f15-153">Select **New Template**.</span></span>
1. <span data-ttu-id="e7f15-154">テンプレート作成ダイアログ ボックスで、テンプレートの名前と説明を入力します。</span><span class="sxs-lookup"><span data-stu-id="e7f15-154">In the template creation dialog box, enter a name and description for the template.</span></span> <span data-ttu-id="e7f15-155">入力する値は、新しいページを作成するときに作成者に表示されます。</span><span class="sxs-lookup"><span data-stu-id="e7f15-155">The values that you enter will be shown to authors when they create new pages.</span></span> <span data-ttu-id="e7f15-156">したがって、ページ作成者にとって有用なメタデータを入力します。</span><span class="sxs-lookup"><span data-stu-id="e7f15-156">Therefore, enter metadata that will be useful to page authors.</span></span> <span data-ttu-id="e7f15-157">たとえば、説明として、**このテンプレートを使用して一般的なマーケティング ページを作成します** と入力します。</span><span class="sxs-lookup"><span data-stu-id="e7f15-157">For example, enter **Use this template to create general marketing pages** as the description.</span></span> <span data-ttu-id="e7f15-158">このメタデータは、後で編集できます。</span><span class="sxs-lookup"><span data-stu-id="e7f15-158">This metadata can be edited later.</span></span>
1. <span data-ttu-id="e7f15-159">**OK** をクリックして新しいテンプレートを作成し、テンプレート エディターを開きます。</span><span class="sxs-lookup"><span data-stu-id="e7f15-159">Select **OK** to create the new template and open the template editor.</span></span> <span data-ttu-id="e7f15-160">テンプレート エディターでは、左側にアウトライン ツリー、右側にプロパティ ウィンドウが表示されます。</span><span class="sxs-lookup"><span data-stu-id="e7f15-160">The template editor shows an outline tree on the left and a property pane on the right.</span></span>
1. <span data-ttu-id="e7f15-161">アウトライン ツリーでノードを展開し、**HTML ヘッド** スロットを選択します。</span><span class="sxs-lookup"><span data-stu-id="e7f15-161">In the outline tree, expand the nodes, and select the **HTML Head** slot.</span></span>
1. <span data-ttu-id="e7f15-162">このスロットにまだモジュールが存在しない場合は、省略記号ボタン (**...**) をクリックし、**モジュールの追加** を選択します。</span><span class="sxs-lookup"><span data-stu-id="e7f15-162">If there aren't yet any modules in this slot, select the ellipsis button (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="e7f15-163">**モジュールの追加** ダイアログ ボックスで **既定のページの概要** を選択し、**OK** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="e7f15-163">In the **Add Module** dialog box, select **Default page summary**, and then select **OK**.</span></span>
1. <span data-ttu-id="e7f15-164">アウトライン ツリーで新しいモジュールを選択し、プロパティ ウィンドウで、テンプレートのすべての子ページに対して自動的にコンフィギュレーションされる既定の設定を入力します。</span><span class="sxs-lookup"><span data-stu-id="e7f15-164">In the outline tree, select the new module, and then, in the property pane, enter any default settings that should be automatically configured for all child pages of the template.</span></span> <span data-ttu-id="e7f15-165">既定の設定を使用しない場合は、値を空白のままにします。</span><span class="sxs-lookup"><span data-stu-id="e7f15-165">If you don't want any default settings, leave the values blank.</span></span>
1. <span data-ttu-id="e7f15-166">アウトライン ツリーで **本文** スロットを選択し、省略記号ボタンを選択してから、**モジュールの追加** を選択します。</span><span class="sxs-lookup"><span data-stu-id="e7f15-166">In the outline tree, select the **Body** slot, select the ellipsis button, and then select **Add Module**.</span></span>
1. <span data-ttu-id="e7f15-167">ページ コンテナー モジュールを選択し (オプションは 1 つしか存在しない場合があります)、**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="e7f15-167">Select a page container module (there might be only one option), and then select **OK**.</span></span>

<span data-ttu-id="e7f15-168">新しいページ コンテナー モジュールの下に、新しい一連のスロット (**ヘッダー**、**メイン** など) が表示されます。</span><span class="sxs-lookup"><span data-stu-id="e7f15-168">Under the new page container module, you will see a new set of slots (**Header**, **Main**, and so on).</span></span> <span data-ttu-id="e7f15-169">ここで、このテンプレートからページを作成するときに作成者が利用できるモジュール オプションを、追加およびコンフィギュレーションできます。</span><span class="sxs-lookup"><span data-stu-id="e7f15-169">Here, you can add and configure the module options that will be available to authors when they create pages from this template.</span></span> <span data-ttu-id="e7f15-170">既定では、スロットにモジュールを追加しない場合、そのスロットで使用可能なすべてのモジュール タイプがサポートされます。</span><span class="sxs-lookup"><span data-stu-id="e7f15-170">By default, if you don't add any modules to a slot, all available modules types are supported for that slot.</span></span>

<span data-ttu-id="e7f15-171">これで、このテンプレートは技術的に有効になり、保存され、チェック インし、新しいページを作成するために使用することができます。</span><span class="sxs-lookup"><span data-stu-id="e7f15-171">The template is now technically valid, and it can be saved, checked in, and used to create new pages.</span></span> <span data-ttu-id="e7f15-172">ただし、次の 3 つのセクションでは、最初にコンフィギュレーションする必要があるその他の既定の設定について説明します。</span><span class="sxs-lookup"><span data-stu-id="e7f15-172">However, the next three sections describe some other default settings that you might want to configure first.</span></span>

## <a name="add-a-header-and-a-footer"></a><span data-ttu-id="e7f15-173">ヘッダーおよびフッターの追加</span><span class="sxs-lookup"><span data-stu-id="e7f15-173">Add a header and a footer</span></span>

<span data-ttu-id="e7f15-174">サイトに既にヘッダー フラグメントが存在する場合、次の手順に従ってヘッダーとフッターをテンプレートに追加します。</span><span class="sxs-lookup"><span data-stu-id="e7f15-174">If your site already has a header fragment, follow these steps to add a header and a footer to a template.</span></span>

1. <span data-ttu-id="e7f15-175">アウトライン ツリーで、**本文** スロットとその子ページ モジュールを展開します。</span><span class="sxs-lookup"><span data-stu-id="e7f15-175">In the outline tree, expand the **Body** slot and its child page module.</span></span>
1. <span data-ttu-id="e7f15-176">**ヘッダー** スロットを選択します。</span><span class="sxs-lookup"><span data-stu-id="e7f15-176">Select the **Header** slot.</span></span>
1. <span data-ttu-id="e7f15-177">**ヘッダー** スロットの省略記号ボタンを選択し、**フラグメントの追加** を選択します。</span><span class="sxs-lookup"><span data-stu-id="e7f15-177">Select the ellipsis button for the **Header** slot, and then select **Add Fragment**.</span></span>
1. <span data-ttu-id="e7f15-178">サイトのヘッダー フラグメントを検索して選択し、**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="e7f15-178">Search for and select your site's header fragment, and then select **OK**.</span></span>

<span data-ttu-id="e7f15-179">このテンプレートを使用するすべてのページでは、このヘッダー フラグメントが自動的に継承されます。</span><span class="sxs-lookup"><span data-stu-id="e7f15-179">All pages that use the template will now automatically inherit this header fragment.</span></span>

<span data-ttu-id="e7f15-180">サイトにヘッダー フラグメントがまだ存在しない場合は、[フラグメントの作成](work-with-fragments.md#create-a-fragment)を参照してフラグメントの作成方法を理解してから、前の手順を実行してください。</span><span class="sxs-lookup"><span data-stu-id="e7f15-180">If your site doesn't yet have a header fragment, see [Create a fragment](work-with-fragments.md#create-a-fragment) for information about how to create it, and then complete the previous procedure.</span></span>

## <a name="change-the-template-theme"></a><span data-ttu-id="e7f15-181">テンプレート テーマの変更</span><span class="sxs-lookup"><span data-stu-id="e7f15-181">Change the template theme</span></span>

<span data-ttu-id="e7f15-182">テンプレートを使用するすべてのページに適用する既定のテーマを設定するには、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="e7f15-182">To set the default theme for all pages that use a template, follow these steps.</span></span>

1. <span data-ttu-id="e7f15-183">左側のアウトライン ツリーで、**本文** スロットを展開します。</span><span class="sxs-lookup"><span data-stu-id="e7f15-183">In the outline tree on the left, expand the **Body** slot.</span></span>
1. <span data-ttu-id="e7f15-184">**本文** スロットで、ページのコンテナー モジュールを選択します (たとえば、**既定のページ**)。</span><span class="sxs-lookup"><span data-stu-id="e7f15-184">In the **Body** slot, select the page container module (for example, **Default Page**).</span></span>
1. <span data-ttu-id="e7f15-185">右側のプロパティ ウィンドウの **テーマ** フィールドで、テーマを選択します。</span><span class="sxs-lookup"><span data-stu-id="e7f15-185">In the property pane on the right, in the **Theme** field, select a theme.</span></span>

<span data-ttu-id="e7f15-186">既定では、選択したテーマがすべての新しいページで使用されます。</span><span class="sxs-lookup"><span data-stu-id="e7f15-186">By default, all new pages will now use the selected theme.</span></span> <span data-ttu-id="e7f15-187">ページがレイアウト レベルまたはページ レベルでこの設定を上書きしないようにするには、**ロック済** ブール コントロールを **True** に設定します。</span><span class="sxs-lookup"><span data-stu-id="e7f15-187">To prevent pages from overriding this setting at the layout or page level, set the **Locked** Boolean control to **True**.</span></span>

## <a name="add-a-script-to-a-template"></a><span data-ttu-id="e7f15-188">テンプレートへのスクリプトの追加</span><span class="sxs-lookup"><span data-stu-id="e7f15-188">Add a script to a template</span></span>

<span data-ttu-id="e7f15-189">JavaScript を含む HTML **&lt;スクリプト&gt;** 要素をテンプレートに追加できます。</span><span class="sxs-lookup"><span data-stu-id="e7f15-189">You can add HTML **&lt;script&gt;** elements that contain JavaScript to your template.</span></span> <span data-ttu-id="e7f15-190">これにより、ページの HTML ヘッド、本文の開始、および本文の終了セクションに対して、既定のスクリプト動作を指定できます。</span><span class="sxs-lookup"><span data-stu-id="e7f15-190">In this way, you can provide default script behaviors to the HTML head, body begin, and body end sections of your pages.</span></span>

<span data-ttu-id="e7f15-191">作業テンプレートにスクリプトを追加するには、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="e7f15-191">To add a script to a template, follow these steps.</span></span>

1. <span data-ttu-id="e7f15-192">左側にあるアウトライン ツリーで、**&lt;スクリプト&gt;** 要素を追加するスロットを選択します (たとえば、HTML ヘッド、本文の開始、本文の終了など)。</span><span class="sxs-lookup"><span data-stu-id="e7f15-192">In the outline tree on the left, select the slot where you want to add the **&lt;script&gt;** element (for example, the HTML head, body begin, or body end).</span></span>
1. <span data-ttu-id="e7f15-193">スロットの省略記号ボタンを選択し、**モジュールの追加** を選択します。</span><span class="sxs-lookup"><span data-stu-id="e7f15-193">Select the ellipsis button for the slot, and then select **Add Module**.</span></span>
1. <span data-ttu-id="e7f15-194">**モジュールの追加** ダイアログ ボックスで、スクリプト モジュールを選択します (たとえば **外部スクリプト** や **インライン スクリプト** など)。</span><span class="sxs-lookup"><span data-stu-id="e7f15-194">In the **Add Module** dialog box, select a script module (for example, **External Script** or **Inline Script**).</span></span>
1. <span data-ttu-id="e7f15-195">右側のプロパティ ウィンドウの、適切なスクリプト プロパティ コントロール (たとえば **インライン スクリプト** や **スクリプト タグ** など) で、スクリプトを入力します。</span><span class="sxs-lookup"><span data-stu-id="e7f15-195">In the property pane on the right, in the appropriate script property control (for example, **Inline Script** or **Script tags**), enter your script.</span></span>
1. <span data-ttu-id="e7f15-196">プロパティ ウィンドウで、コンフィギュレーションするその他のオプション設定を入力します。</span><span class="sxs-lookup"><span data-stu-id="e7f15-196">In the property pane, enter any other optional settings that you want to configure.</span></span>

> [!TIP]
> <span data-ttu-id="e7f15-197">他のテンプレートのスクリプト モジュールを再利用する場合は、それらをフラグメントに変換することができます。</span><span class="sxs-lookup"><span data-stu-id="e7f15-197">If you want to reuse any of your script modules for other templates, you can convert them to fragments.</span></span> <span data-ttu-id="e7f15-198">この方法により、作成プロセスを効率化し、更新プロセスを一元化することができます。</span><span class="sxs-lookup"><span data-stu-id="e7f15-198">In this way, you help make the authoring process more efficient, and you centralize the update process.</span></span> <span data-ttu-id="e7f15-199">スクリプト モジュールをフラグメントに変換する方法については、[既存のモジュール コンフィギュレーションをフラグメントとして保存する](work-with-fragments.md#save-an-existing-module-configuration-as-a-fragment)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="e7f15-199">For information about how to convert a script module to a fragment, see [Save an existing module configuration as a fragment](work-with-fragments.md#save-an-existing-module-configuration-as-a-fragment).</span></span>

## <a name="save-check-in-preview-and-publish-a-template"></a><span data-ttu-id="e7f15-200">テンプレートの保存、チェック イン、プレビュー、および公開</span><span class="sxs-lookup"><span data-stu-id="e7f15-200">Save, check in, preview, and publish a template</span></span>

<span data-ttu-id="e7f15-201">テンプレートを保存してチェック インするには、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="e7f15-201">To save and check in a template, follow these steps.</span></span>

1. <span data-ttu-id="e7f15-202">テンプレート エディターの上部にある **保存** を選択します。</span><span class="sxs-lookup"><span data-stu-id="e7f15-202">Select **Save** at the top of the template editor.</span></span> <span data-ttu-id="e7f15-203">保存された変更は、チェック インされるまで下流ページに影響しません。</span><span class="sxs-lookup"><span data-stu-id="e7f15-203">Saved changes don't affect downstream pages until they are checked in.</span></span>
1. <span data-ttu-id="e7f15-204">**編集完了** を選択します。</span><span class="sxs-lookup"><span data-stu-id="e7f15-204">Select **Finish editing**.</span></span> <span data-ttu-id="e7f15-205">下流のワークフローで変更が検出可能になりました。</span><span class="sxs-lookup"><span data-stu-id="e7f15-205">Your changes are now discoverable for downstream workflows.</span></span>

<span data-ttu-id="e7f15-206">変更をプレビューするには、テンプレートを使用している既存のページを開くか、テンプレートから新しいページを作成します。</span><span class="sxs-lookup"><span data-stu-id="e7f15-206">To preview your changes, either open an existing page that uses the template or create a new page from the template.</span></span>

<span data-ttu-id="e7f15-207">テンプレートの変更をプレビューしたら、次のいずれかの手順に従って、実際のサイトにテンプレートを公開します。</span><span class="sxs-lookup"><span data-stu-id="e7f15-207">After you've previewed the changes to your template, follow one of these steps to publish the template to your live site:</span></span>

* <span data-ttu-id="e7f15-208">**テンプレート** に移動し、テンプレートを選択してから、**公開** を選択します。</span><span class="sxs-lookup"><span data-stu-id="e7f15-208">Go to **Templates**, select the template, and then select **Publish**.</span></span>
* <span data-ttu-id="e7f15-209">レイアウト名を選択してレイアウト エディターを開き、**発行** を選択します。</span><span class="sxs-lookup"><span data-stu-id="e7f15-209">Select the layout name to open the layout editor, and then select **Publish**.</span></span>
* <span data-ttu-id="e7f15-210">未公開のテンプレートを参照するページを公開します。</span><span class="sxs-lookup"><span data-stu-id="e7f15-210">Publish a page that references the unpublished template.</span></span> <span data-ttu-id="e7f15-211">テンプレートが自動的に公開されます。</span><span class="sxs-lookup"><span data-stu-id="e7f15-211">The template is automatically published.</span></span>

> [!WARNING]
> <span data-ttu-id="e7f15-212">テンプレートまたはその他のコンテンツ管理システム (CMS) 項目を公開すると、インターネット上で検出可能になります。</span><span class="sxs-lookup"><span data-stu-id="e7f15-212">When a template, or any other content management system (CMS) item, is published, it's discoverable on the internet.</span></span> <span data-ttu-id="e7f15-213">ドキュメントまたは資産を公開する準備が整うまで、公開しないでください。</span><span class="sxs-lookup"><span data-stu-id="e7f15-213">Don't publish documents or assets until you're ready to make them public.</span></span> <span data-ttu-id="e7f15-214">保存およびチェック インされているが、まだ公開されていないドキュメント バージョンは、認証済みのシステム ユーザーだけが検出可能です。</span><span class="sxs-lookup"><span data-stu-id="e7f15-214">Document versions that have been saved and checked in, but that haven't been published, are discoverable only to authenticated system users.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="e7f15-215">追加リソース</span><span class="sxs-lookup"><span data-stu-id="e7f15-215">Additional resources</span></span>

[<span data-ttu-id="e7f15-216">テンプレートとレイアウトの概要</span><span class="sxs-lookup"><span data-stu-id="e7f15-216">Templates and layouts overview</span></span>](templates-layouts-overview.md)

[<span data-ttu-id="e7f15-217">プリセット レイアウトの使用</span><span class="sxs-lookup"><span data-stu-id="e7f15-217">Work with preset layouts</span></span>](work-with-layouts.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
