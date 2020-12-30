---
title: テンプレートの使用
description: このトピックでは、Microsoft Dynamics 365 Commerce でのテンプレートの使用方法について説明します。
author: phinneyridge
manager: annbe
ms.date: 04/14/2020
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
ms.author: niholman
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: a3fc4259a76f6edcfaa0b8f6e08292477c6c0835
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/13/2020
ms.locfileid: "4413766"
---
# <a name="work-with-templates"></a><span data-ttu-id="2e553-103">テンプレートの使用</span><span class="sxs-lookup"><span data-stu-id="2e553-103">Work with templates</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="2e553-104">このトピックでは、Microsoft Dynamics 365 Commerce でのテンプレートの使用方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="2e553-104">This topic describes how to work with templates in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="2e553-105">概要</span><span class="sxs-lookup"><span data-stu-id="2e553-105">Overview</span></span>

<span data-ttu-id="2e553-106">[テンプレートとレイアウトの概要](templates-layouts-overview.md)で説明したように、テンプレートは、下流の作成者が使用できる一連のオプションを定義します。</span><span class="sxs-lookup"><span data-stu-id="2e553-106">As was discussed in [Templates and layouts overview](templates-layouts-overview.md), templates define the set of options that is available to downstream authors.</span></span> <span data-ttu-id="2e553-107">テンプレートは企業の Web 作成チームにとってさまざまな理由から役に立ちます。適切なテンプレートを使用することで、次の目標を達成できます。</span><span class="sxs-lookup"><span data-stu-id="2e553-107">Templates are useful to an enterprise's web authoring team for several reasons, and well-structured templates can help with all the following goals:</span></span>

- <span data-ttu-id="2e553-108">日々のコンテンツ編集者の役割において、作成エクスペリエンスを簡略化します。</span><span class="sxs-lookup"><span data-stu-id="2e553-108">Simplify the authoring experience for day-to-day content editor roles.</span></span>

    - <span data-ttu-id="2e553-109">モジュール オプションをフィルター処理して、特定のページ セクションに関連モジュールのみを表示します。</span><span class="sxs-lookup"><span data-stu-id="2e553-109">Filter module options so that only relevant modules are shown for a specific page section.</span></span> <span data-ttu-id="2e553-110">(たとえば、テンプレートのマーケティング セクションをコンフィギュレーションして、そのコンテキストでは使用しない不適切なモジュールをフィルター処理し、表示されている場合はコンテンツの作成タスクを複雑化します。)</span><span class="sxs-lookup"><span data-stu-id="2e553-110">(For example, a marketing section of a template can be configured to filter out irrelevant modules that should never be used in that context, and that will just complicate content authoring tasks if they are shown.)</span></span>
    - <span data-ttu-id="2e553-111">既定のモジュール設定をコンフィギュレーションして、作成の効率を高めます。</span><span class="sxs-lookup"><span data-stu-id="2e553-111">Configure default module setting to help improve authoring efficiency.</span></span>
    - <span data-ttu-id="2e553-112">既定のページ フラグメントを定義して、作成の効率を高めます。</span><span class="sxs-lookup"><span data-stu-id="2e553-112">Define default page fragments to help improve authoring efficiency.</span></span> <span data-ttu-id="2e553-113">(たとえば、テンプレートのヘッダーおよびフッター フラグメントは、下流のページすべてで自動的に表示されます。)</span><span class="sxs-lookup"><span data-stu-id="2e553-113">(For example, header and footer fragments in a template will automatically appear on every downstream page.)</span></span>

- <span data-ttu-id="2e553-114">承認済の一連のモジュール配置およびコンフィギュレーション オプションを定義することで、企業のサイトをブランド イメージに沿ったものに保ちます。</span><span class="sxs-lookup"><span data-stu-id="2e553-114">Keep enterprise sites on-brand by defining an approved set of module arrangement and configuration options.</span></span>

    > [!TIP] 
    > <span data-ttu-id="2e553-115">成功している E コマース サイトには、顧客になじみがあり、反復可能で、ブランドイメージに沿ったユーザー エクスペリエンス (UX) デザイン パターンがあります。</span><span class="sxs-lookup"><span data-stu-id="2e553-115">Successful e-Commerce sites provide customers with familiar, repeatable, and on-brand user experience (UX) design patterns.</span></span> <span data-ttu-id="2e553-116">テンプレートを使用すると、サイト全体の一貫性を制御するのに役立ちます。</span><span class="sxs-lookup"><span data-stu-id="2e553-116">By using templates, you help control consistency across your site.</span></span>

- <span data-ttu-id="2e553-117">反復可能でプログラムによって定義された、ページ定義およびメタデータを確認して、検索エンジン最適化 (SEO) スコアを向上させます。</span><span class="sxs-lookup"><span data-stu-id="2e553-117">Improve search engine optimization (SEO) scores by ensuring repeatable and programmatically defined page definitions and metadata.</span></span>

> [!NOTE]
> <span data-ttu-id="2e553-118">テンプレートはサイト全体の整合性を制御するように設計されていますが、理論的には、一貫性を強要しないようにコンフィギュレーションすることができます。</span><span class="sxs-lookup"><span data-stu-id="2e553-118">Although templates are designed to control consistency across a site, they can theoretically be configured so that they don't enforce any consistency.</span></span> <span data-ttu-id="2e553-119">ブランドとサイトの管理者は、サイトのページの可変性レベルを定義できます。</span><span class="sxs-lookup"><span data-stu-id="2e553-119">Brand and site administrators can define any level of variability for the pages on their site.</span></span> <span data-ttu-id="2e553-120">たとえば、テンプレートを完全に開いたままにすると、コンテンツ作成者が選択したページ デザインを作成できるようになります。</span><span class="sxs-lookup"><span data-stu-id="2e553-120">For example, a template can be left entirely open, so that content authors can create any page design that they choose.</span></span> <span data-ttu-id="2e553-121">この場合、上記のどの利点も適用されません。</span><span class="sxs-lookup"><span data-stu-id="2e553-121">In this case, none of the benefits in the preceding list are applicable.</span></span>

## <a name="modify-a-template"></a><span data-ttu-id="2e553-122">テンプレートの変更</span><span class="sxs-lookup"><span data-stu-id="2e553-122">Modify a template</span></span>

<span data-ttu-id="2e553-123">テンプレートは、テンプレート エディターを使用して変更できます。</span><span class="sxs-lookup"><span data-stu-id="2e553-123">Templates are modified by using the template editor.</span></span>

<span data-ttu-id="2e553-124">テンプレート エディターを開くには、次の手順のいずれかに従います。</span><span class="sxs-lookup"><span data-stu-id="2e553-124">To open the template editor, follow one of these steps:</span></span>

- <span data-ttu-id="2e553-125">サイトのナビゲーション ウィンドウで、**テンプレート** を選択し、変更するテンプレートを選択します。</span><span class="sxs-lookup"><span data-stu-id="2e553-125">In the navigation pane of your site, select **Templates**, and then select the template to modify.</span></span>
- <span data-ttu-id="2e553-126">既存のページのページ エディターで、左側のアウトライン ツリーのトップ ノードを選択します。</span><span class="sxs-lookup"><span data-stu-id="2e553-126">In the page editor for an existing page, select the top node in the outline tree on the left.</span></span> <span data-ttu-id="2e553-127">次に、右のプロパティ ウィンドウで、**テンプレートの編集** を選択します。</span><span class="sxs-lookup"><span data-stu-id="2e553-127">Then, in the property pane on the right, select **Edit Template**.</span></span>

<span data-ttu-id="2e553-128">左側のアウトライン ツリー ビューには、子レイアウトとページで使用できるモジュール オプションと構造が表示されます。</span><span class="sxs-lookup"><span data-stu-id="2e553-128">The outline tree view on the left shows the module options and structures that are available to child layouts and pages.</span></span> <span data-ttu-id="2e553-129">アウトライン ツリーでモジュールを選択すると、選択したモジュールのテンプレート プロパティが右側のプロパティ ウィンドウに表示されます。</span><span class="sxs-lookup"><span data-stu-id="2e553-129">When you select a module in the outline tree, you can view the template properties for the selected module in the property pane on the right.</span></span> <span data-ttu-id="2e553-130">これらのプロパティの一部は、テンプレート編集に固有です。</span><span class="sxs-lookup"><span data-stu-id="2e553-130">Some of these properties are unique to template editing.</span></span> <span data-ttu-id="2e553-131">次のテーブルにこれらのプロパティを示します。</span><span class="sxs-lookup"><span data-stu-id="2e553-131">The following table describes these properties.</span></span>

| <span data-ttu-id="2e553-132">プロパティ名</span><span class="sxs-lookup"><span data-stu-id="2e553-132">Property name</span></span> | <span data-ttu-id="2e553-133">説明</span><span class="sxs-lookup"><span data-stu-id="2e553-133">Description</span></span> |
|---|---|
| <span data-ttu-id="2e553-134">最小発生数</span><span class="sxs-lookup"><span data-stu-id="2e553-134">Min Occurs</span></span> | <span data-ttu-id="2e553-135">このプロパティは、選択されたモジュールの最小発生数を定義します。</span><span class="sxs-lookup"><span data-stu-id="2e553-135">This property defines the minimum number of occurrences for the selected module.</span></span> <span data-ttu-id="2e553-136">たとえば、値が **1** に設定されている場合、モジュールは下流の作成者に対して必要ですが、値が **0** (ゼロ) に設定されている場合、モジュールはオプションです。</span><span class="sxs-lookup"><span data-stu-id="2e553-136">For example, if the value is set to **1**, the module is required for downstream authors, whereas if the value is set to **0** (zero), the module is optional.</span></span> |
| <span data-ttu-id="2e553-137">最大発生数</span><span class="sxs-lookup"><span data-stu-id="2e553-137">Max Occurs</span></span> | <span data-ttu-id="2e553-138">このプロパティは、選択されたモジュールの最大発生数を定義します。</span><span class="sxs-lookup"><span data-stu-id="2e553-138">This property defines the maximum number of occurrences for the selected module.</span></span> <span data-ttu-id="2e553-139">たとえば、この値が **1** に設定されている場合、モジュールを追加できるのは 1 回だけです。</span><span class="sxs-lookup"><span data-stu-id="2e553-139">For example, if the value is set to **1**, the module can be added only one time.</span></span> |
| <span data-ttu-id="2e553-140">最小モジュール (コンテナー)</span><span class="sxs-lookup"><span data-stu-id="2e553-140">Min Modules (Containers)</span></span> | <span data-ttu-id="2e553-141">他のモジュールを含むモジュール (つまり、*コンテナーモジュール*) では、このプロパティは子として追加する必要があるモジュール総数の最小数を定義します。</span><span class="sxs-lookup"><span data-stu-id="2e553-141">For modules that contain other modules (that is, for *containers modules*), this property defines the minimum number of total modules that should be added as children.</span></span> <span data-ttu-id="2e553-142">たとえば、カルーセル モジュールでは、値が 1 より大きい数値に設定されている場合があります。</span><span class="sxs-lookup"><span data-stu-id="2e553-142">For example, for a carousel module, the value might be set to a number that is more than 1.</span></span> |
| <span data-ttu-id="2e553-143">最大モジュール (コンテナー)</span><span class="sxs-lookup"><span data-stu-id="2e553-143">Max Modules (Containers)</span></span> | <span data-ttu-id="2e553-144">コンテナー モジュールの場合、このプロパティは子として追加する必要があるモジュール総数の最大値を定義します。</span><span class="sxs-lookup"><span data-stu-id="2e553-144">For container modules, this property defines the maximum number of total modules that should be added as children.</span></span> <span data-ttu-id="2e553-145">たとえば、カルーセル モジュールでは、値が 10 より小さい数値に設定されている場合があります。</span><span class="sxs-lookup"><span data-stu-id="2e553-145">For example, for a carousel module, the value might be set to a number that is less than 10.</span></span> |
| <span data-ttu-id="2e553-146">ロック済</span><span class="sxs-lookup"><span data-stu-id="2e553-146">Locked</span></span> | <span data-ttu-id="2e553-147">**ロック済** のブール コントロールは、すべてのコア モジュール プロパティの横に表示されます。</span><span class="sxs-lookup"><span data-stu-id="2e553-147">A **Locked** Boolean control appears next to all core module properties.</span></span> <span data-ttu-id="2e553-148">これにより、テンプレート作成者はテンプレートのモジュール設定をロックできます。</span><span class="sxs-lookup"><span data-stu-id="2e553-148">It lets the template author lock a module setting in the template.</span></span> <span data-ttu-id="2e553-149">ロック済のモジュールの設定は、子レイアウトまたはページで上書きすることはできません。</span><span class="sxs-lookup"><span data-stu-id="2e553-149">A module setting that is locked can't be overridden by any child layouts or pages.</span></span> <span data-ttu-id="2e553-150">このテンプレートを使用するすべてのレイアウトとページで、一括編集可能なプロパティ値になります。</span><span class="sxs-lookup"><span data-stu-id="2e553-150">It becomes a centrally editable property value for all layouts and pages that use the template.</span></span> |

## <a name="create-a-new-template"></a><span data-ttu-id="2e553-151">新しいテンプレートを作成</span><span class="sxs-lookup"><span data-stu-id="2e553-151">Create a new template</span></span>

<span data-ttu-id="2e553-152">新しいテンプレートを作成するには、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="2e553-152">To create a new template, follow these steps.</span></span>

1. <span data-ttu-id="2e553-153">サイトのナビゲーション ウィンドウで、**テンプレート** を選択し、テンプレート インスペクター ビューを開きます。</span><span class="sxs-lookup"><span data-stu-id="2e553-153">In the navigation pane of your site, select **Templates** to open the template inspector view.</span></span>
1. <span data-ttu-id="2e553-154">**新しいテンプレート** を選択します。</span><span class="sxs-lookup"><span data-stu-id="2e553-154">Select **New Template**.</span></span>
1. <span data-ttu-id="2e553-155">テンプレート作成ダイアログ ボックスで、テンプレートの名前と説明を入力します。</span><span class="sxs-lookup"><span data-stu-id="2e553-155">In the template creation dialog box, enter a name and description for the template.</span></span> <span data-ttu-id="2e553-156">入力する値は、新しいページを作成するときに作成者に表示されます。</span><span class="sxs-lookup"><span data-stu-id="2e553-156">The values that you enter will be shown to authors when they create new pages.</span></span> <span data-ttu-id="2e553-157">したがって、ページ作成者にとって有用なメタデータを入力します。</span><span class="sxs-lookup"><span data-stu-id="2e553-157">Therefore, enter metadata that will be useful to page authors.</span></span> <span data-ttu-id="2e553-158">たとえば、説明として、**このテンプレートを使用して一般的なマーケティング ページを作成します** と入力します。</span><span class="sxs-lookup"><span data-stu-id="2e553-158">For example, enter **Use this template to create general marketing pages** as the description.</span></span> <span data-ttu-id="2e553-159">このメタデータは、後で編集できます。</span><span class="sxs-lookup"><span data-stu-id="2e553-159">This metadata can be edited later.</span></span>
1. <span data-ttu-id="2e553-160">**OK** をクリックして新しいテンプレートを作成し、テンプレート エディターを開きます。</span><span class="sxs-lookup"><span data-stu-id="2e553-160">Select **OK** to create the new template and open the template editor.</span></span> <span data-ttu-id="2e553-161">テンプレート エディターでは、左側にアウトライン ツリー、右側にプロパティ ウィンドウが表示されます。</span><span class="sxs-lookup"><span data-stu-id="2e553-161">The template editor shows an outline tree on the left and a property pane on the right.</span></span>
1. <span data-ttu-id="2e553-162">アウトライン ツリーでノードを展開し、**HTML ヘッド** スロットを選択します。</span><span class="sxs-lookup"><span data-stu-id="2e553-162">In the outline tree, expand the nodes, and select the **HTML Head** slot.</span></span>
1. <span data-ttu-id="2e553-163">このスロットにまだモジュールが存在しない場合は、省略記号ボタン (**...**) をクリックし、**モジュールの追加** を選択します。</span><span class="sxs-lookup"><span data-stu-id="2e553-163">If there aren't yet any modules in this slot, select the ellipsis button (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="2e553-164">**モジュールの追加** ダイアログ ボックスで **既定のページの概要** を選択し、**OK** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="2e553-164">In the **Add Module** dialog box, select **Default page summary**, and then select **OK**.</span></span>
1. <span data-ttu-id="2e553-165">アウトライン ツリーで新しいモジュールを選択し、プロパティ ウィンドウで、テンプレートのすべての子ページに対して自動的にコンフィギュレーションされる既定の設定を入力します。</span><span class="sxs-lookup"><span data-stu-id="2e553-165">In the outline tree, select the new module, and then, in the property pane, enter any default settings that should be automatically configured for all child pages of the template.</span></span> <span data-ttu-id="2e553-166">既定の設定を使用しない場合は、値を空白のままにします。</span><span class="sxs-lookup"><span data-stu-id="2e553-166">If you don't want any default settings, leave the values blank.</span></span>
1. <span data-ttu-id="2e553-167">アウトライン ツリーで **本文** スロットを選択し、省略記号ボタンを選択してから、**モジュールの追加** を選択します。</span><span class="sxs-lookup"><span data-stu-id="2e553-167">In the outline tree, select the **Body** slot, select the ellipsis button, and then select **Add Module**.</span></span>
1. <span data-ttu-id="2e553-168">ページ コンテナー モジュールを選択し (オプションは 1 つしか存在しない場合があります)、**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="2e553-168">Select a page container module (there might be only one option), and then select **OK**.</span></span>

<span data-ttu-id="2e553-169">新しいページ コンテナー モジュールの下に、新しい一連のスロット (**ヘッダー**、**メイン** など) が表示されます。</span><span class="sxs-lookup"><span data-stu-id="2e553-169">Under the new page container module, you will see a new set of slots (**Header**, **Main**, and so on).</span></span> <span data-ttu-id="2e553-170">ここで、このテンプレートからページを作成するときに作成者が利用できるモジュール オプションを、追加およびコンフィギュレーションできます。</span><span class="sxs-lookup"><span data-stu-id="2e553-170">Here, you can add and configure the module options that will be available to authors when they create pages from this template.</span></span> <span data-ttu-id="2e553-171">既定では、スロットにモジュールを追加しない場合、そのスロットで使用可能なすべてのモジュール タイプがサポートされます。</span><span class="sxs-lookup"><span data-stu-id="2e553-171">By default, if you don't add any modules to a slot, all available modules types are supported for that slot.</span></span>

<span data-ttu-id="2e553-172">これで、このテンプレートは技術的に有効になり、保存され、チェック インし、新しいページを作成するために使用することができます。</span><span class="sxs-lookup"><span data-stu-id="2e553-172">The template is now technically valid, and it can be saved, checked in, and used to create new pages.</span></span> <span data-ttu-id="2e553-173">ただし、次の 3 つのセクションでは、最初にコンフィギュレーションする必要があるその他の既定の設定について説明します。</span><span class="sxs-lookup"><span data-stu-id="2e553-173">However, the next three sections describe some other default settings that you might want to configure first.</span></span>

## <a name="add-a-header-and-a-footer"></a><span data-ttu-id="2e553-174">ヘッダーおよびフッターの追加</span><span class="sxs-lookup"><span data-stu-id="2e553-174">Add a header and a footer</span></span>

<span data-ttu-id="2e553-175">サイトに既にヘッダー フラグメントが存在する場合、次の手順に従ってヘッダーとフッターをテンプレートに追加します。</span><span class="sxs-lookup"><span data-stu-id="2e553-175">If your site already has a header fragment, follow these steps to add a header and a footer to a template.</span></span>

1. <span data-ttu-id="2e553-176">アウトライン ツリーで、**本文** スロットとその子ページ モジュールを展開します。</span><span class="sxs-lookup"><span data-stu-id="2e553-176">In the outline tree, expand the **Body** slot and its child page module.</span></span>
1. <span data-ttu-id="2e553-177">**ヘッダー** スロットを選択します。</span><span class="sxs-lookup"><span data-stu-id="2e553-177">Select the **Header** slot.</span></span>
1. <span data-ttu-id="2e553-178">**ヘッダー** スロットの省略記号ボタンを選択し、**フラグメントの追加** を選択します。</span><span class="sxs-lookup"><span data-stu-id="2e553-178">Select the ellipsis button for the **Header** slot, and then select **Add Fragment**.</span></span>
1. <span data-ttu-id="2e553-179">サイトのヘッダー フラグメントを検索して選択し、**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="2e553-179">Search for and select your site's header fragment, and then select **OK**.</span></span>

<span data-ttu-id="2e553-180">このテンプレートを使用するすべてのページでは、このヘッダー フラグメントが自動的に継承されます。</span><span class="sxs-lookup"><span data-stu-id="2e553-180">All pages that use the template will now automatically inherit this header fragment.</span></span>

<span data-ttu-id="2e553-181">サイトにヘッダー フラグメントがまだ存在しない場合は、[フラグメントの作成](work-with-fragments.md#create-a-fragment)を参照してフラグメントの作成方法を理解してから、前の手順を実行してください。</span><span class="sxs-lookup"><span data-stu-id="2e553-181">If your site doesn't yet have a header fragment, see [Create a fragment](work-with-fragments.md#create-a-fragment) for information about how to create it, and then complete the previous procedure.</span></span>

## <a name="change-the-template-theme"></a><span data-ttu-id="2e553-182">テンプレート テーマの変更</span><span class="sxs-lookup"><span data-stu-id="2e553-182">Change the template theme</span></span>

<span data-ttu-id="2e553-183">テンプレートを使用するすべてのページに適用する既定のテーマを設定するには、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="2e553-183">To set the default theme for all pages that use a template, follow these steps.</span></span>

1. <span data-ttu-id="2e553-184">左側のアウトライン ツリーで、**本文** スロットを展開します。</span><span class="sxs-lookup"><span data-stu-id="2e553-184">In the outline tree on the left, expand the **Body** slot.</span></span>
1. <span data-ttu-id="2e553-185">**本文** スロットで、ページのコンテナー モジュールを選択します (たとえば、**既定のページ**)。</span><span class="sxs-lookup"><span data-stu-id="2e553-185">In the **Body** slot, select the page container module (for example, **Default Page**).</span></span>
1. <span data-ttu-id="2e553-186">右側のプロパティ ウィンドウの **テーマ** フィールドで、テーマを選択します。</span><span class="sxs-lookup"><span data-stu-id="2e553-186">In the property pane on the right, in the **Theme** field, select a theme.</span></span>

<span data-ttu-id="2e553-187">既定では、選択したテーマがすべての新しいページで使用されます。</span><span class="sxs-lookup"><span data-stu-id="2e553-187">By default, all new pages will now use the selected theme.</span></span> <span data-ttu-id="2e553-188">ページがレイアウト レベルまたはページ レベルでこの設定を上書きしないようにするには、**ロック済** ブール コントロールを **True** に設定します。</span><span class="sxs-lookup"><span data-stu-id="2e553-188">To prevent pages from overriding this setting at the layout or page level, set the **Locked** Boolean control to **True**.</span></span>

## <a name="add-a-script-to-a-template"></a><span data-ttu-id="2e553-189">テンプレートへのスクリプトの追加</span><span class="sxs-lookup"><span data-stu-id="2e553-189">Add a script to a template</span></span>

<span data-ttu-id="2e553-190">JavaScript を含む HTML **&lt;スクリプト&gt;** 要素をテンプレートに追加できます。</span><span class="sxs-lookup"><span data-stu-id="2e553-190">You can add HTML **&lt;script&gt;** elements that contain JavaScript to your template.</span></span> <span data-ttu-id="2e553-191">これにより、ページの HTML ヘッド、本文の開始、および本文の終了セクションに対して、既定のスクリプト動作を指定できます。</span><span class="sxs-lookup"><span data-stu-id="2e553-191">In this way, you can provide default script behaviors to the HTML head, body begin, and body end sections of your pages.</span></span>

<span data-ttu-id="2e553-192">作業テンプレートにスクリプトを追加するには、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="2e553-192">To add a script to a template, follow these steps.</span></span>

1. <span data-ttu-id="2e553-193">左側にあるアウトライン ツリーで、**&lt;スクリプト&gt;** 要素を追加するスロットを選択します (たとえば、HTML ヘッド、本文の開始、本文の終了など)。</span><span class="sxs-lookup"><span data-stu-id="2e553-193">In the outline tree on the left, select the slot where you want to add the **&lt;script&gt;** element (for example, the HTML head, body begin, or body end).</span></span>
1. <span data-ttu-id="2e553-194">スロットの省略記号ボタンを選択し、**モジュールの追加** を選択します。</span><span class="sxs-lookup"><span data-stu-id="2e553-194">Select the ellipsis button for the slot, and then select **Add Module**.</span></span>
1. <span data-ttu-id="2e553-195">**モジュールの追加** ダイアログ ボックスで、スクリプト モジュールを選択します (たとえば **外部スクリプト** や **インライン スクリプト** など)。</span><span class="sxs-lookup"><span data-stu-id="2e553-195">In the **Add Module** dialog box, select a script module (for example, **External Script** or **Inline Script**).</span></span>
1. <span data-ttu-id="2e553-196">右側のプロパティ ウィンドウの、適切なスクリプト プロパティ コントロール (たとえば **インライン スクリプト** や **スクリプト タグ** など) で、スクリプトを入力します。</span><span class="sxs-lookup"><span data-stu-id="2e553-196">In the property pane on the right, in the appropriate script property control (for example, **Inline Script** or **Script tags**), enter your script.</span></span>
1. <span data-ttu-id="2e553-197">プロパティ ウィンドウで、コンフィギュレーションするその他のオプション設定を入力します。</span><span class="sxs-lookup"><span data-stu-id="2e553-197">In the property pane, enter any other optional settings that you want to configure.</span></span>

> [!TIP]
> <span data-ttu-id="2e553-198">他のテンプレートのスクリプト モジュールを再利用する場合は、それらをフラグメントに変換することができます。</span><span class="sxs-lookup"><span data-stu-id="2e553-198">If you want to reuse any of your script modules for other templates, you can convert them to fragments.</span></span> <span data-ttu-id="2e553-199">この方法により、作成プロセスを効率化し、更新プロセスを一元化することができます。</span><span class="sxs-lookup"><span data-stu-id="2e553-199">In this way, you help make the authoring process more efficient, and you centralize the update process.</span></span> <span data-ttu-id="2e553-200">スクリプト モジュールをフラグメントに変換する方法については、[既存のモジュール コンフィギュレーションをフラグメントとして保存する](work-with-fragments.md#save-an-existing-module-configuration-as-a-fragment)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="2e553-200">For information about how to convert a script module to a fragment, see [Save an existing module configuration as a fragment](work-with-fragments.md#save-an-existing-module-configuration-as-a-fragment).</span></span>

## <a name="save-check-in-preview-and-publish-a-template"></a><span data-ttu-id="2e553-201">テンプレートの保存、チェック イン、プレビュー、および公開</span><span class="sxs-lookup"><span data-stu-id="2e553-201">Save, check in, preview, and publish a template</span></span>

<span data-ttu-id="2e553-202">テンプレートを保存してチェック インするには、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="2e553-202">To save and check in a template, follow these steps.</span></span>

1. <span data-ttu-id="2e553-203">テンプレート エディターの上部にある **保存** を選択します。</span><span class="sxs-lookup"><span data-stu-id="2e553-203">Select **Save** at the top of the template editor.</span></span> <span data-ttu-id="2e553-204">保存された変更は、チェック インされるまで下流ページに影響しません。</span><span class="sxs-lookup"><span data-stu-id="2e553-204">Saved changes don't affect downstream pages until they are checked in.</span></span>
1. <span data-ttu-id="2e553-205">**編集完了** を選択します。</span><span class="sxs-lookup"><span data-stu-id="2e553-205">Select **Finish editing**.</span></span> <span data-ttu-id="2e553-206">下流のワークフローで変更が検出可能になりました。</span><span class="sxs-lookup"><span data-stu-id="2e553-206">Your changes are now discoverable for downstream workflows.</span></span>

<span data-ttu-id="2e553-207">変更をプレビューするには、テンプレートを使用している既存のページを開くか、テンプレートから新しいページを作成します。</span><span class="sxs-lookup"><span data-stu-id="2e553-207">To preview your changes, either open an existing page that uses the template or create a new page from the template.</span></span>

<span data-ttu-id="2e553-208">テンプレートの変更をプレビューしたら、次のいずれかの手順に従って、実際のサイトにテンプレートを公開します。</span><span class="sxs-lookup"><span data-stu-id="2e553-208">After you've previewed the changes to your template, follow one of these steps to publish the template to your live site:</span></span>

* <span data-ttu-id="2e553-209">**テンプレート** に移動し、テンプレートを選択してから、**公開** を選択します。</span><span class="sxs-lookup"><span data-stu-id="2e553-209">Go to **Templates**, select the template, and then select **Publish**.</span></span>
* <span data-ttu-id="2e553-210">レイアウト名を選択してレイアウト エディターを開き、**発行** を選択します。</span><span class="sxs-lookup"><span data-stu-id="2e553-210">Select the layout name to open the layout editor, and then select **Publish**.</span></span>
* <span data-ttu-id="2e553-211">未公開のテンプレートを参照するページを公開します。</span><span class="sxs-lookup"><span data-stu-id="2e553-211">Publish a page that references the unpublished template.</span></span> <span data-ttu-id="2e553-212">テンプレートが自動的に公開されます。</span><span class="sxs-lookup"><span data-stu-id="2e553-212">The template is automatically published.</span></span>

> [!WARNING]
> <span data-ttu-id="2e553-213">テンプレートまたはその他のコンテンツ管理システム (CMS) 項目を公開すると、インターネット上で検出可能になります。</span><span class="sxs-lookup"><span data-stu-id="2e553-213">When a template, or any other content management system (CMS) item, is published, it's discoverable on the internet.</span></span> <span data-ttu-id="2e553-214">ドキュメントまたは資産を公開する準備が整うまで、公開しないでください。</span><span class="sxs-lookup"><span data-stu-id="2e553-214">Don't publish documents or assets until you're ready to make them public.</span></span> <span data-ttu-id="2e553-215">保存およびチェック インされているが、まだ公開されていないドキュメント バージョンは、認証済みのシステム ユーザーだけが検出可能です。</span><span class="sxs-lookup"><span data-stu-id="2e553-215">Document versions that have been saved and checked in, but that haven't been published, are discoverable only to authenticated system users.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="2e553-216">追加リソース</span><span class="sxs-lookup"><span data-stu-id="2e553-216">Additional resources</span></span>

[<span data-ttu-id="2e553-217">テンプレートとレイアウトの概要</span><span class="sxs-lookup"><span data-stu-id="2e553-217">Templates and layouts overview</span></span>](templates-layouts-overview.md)

[<span data-ttu-id="2e553-218">プリセット レイアウトの使用</span><span class="sxs-lookup"><span data-stu-id="2e553-218">Work with preset layouts</span></span>](work-with-layouts.md)
