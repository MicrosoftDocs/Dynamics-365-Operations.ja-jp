---
title: 検索結果モジュール
description: このトピックでは、検索結果モジュールを取り上げ、Microsoft Dynamics 365 Commerce のサイト ページにそれを追加する方法について説明します。
author: anupamar-ms
ms.date: 05/28/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: 645022000d8746db3793a8a8611ab8f17c7bcc6e
ms.sourcegitcommit: 53b797ff1b524f581046b48cdde42f50b37495bc
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/28/2021
ms.locfileid: "6117136"
---
# <a name="search-results-module"></a><span data-ttu-id="0f43f-103">検索結果モジュール</span><span class="sxs-lookup"><span data-stu-id="0f43f-103">Search results module</span></span>

[!include [banner](includes/banner.md)]
[!include [banner](includes/preview-banner.md)]

<span data-ttu-id="0f43f-104">このトピックでは、検索結果モジュールを取り上げ、Microsoft Dynamics 365 Commerce のサイト ページにそれを追加する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="0f43f-104">This topic covers search results modules and describes how to add them to site pages in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="0f43f-105">検索結果モジュールは、製品の検索結果と、製品に該当する絞り込み条件の一覧を返します。</span><span class="sxs-lookup"><span data-stu-id="0f43f-105">The search results module returns product search results and a list of applicable refiners for the products.</span></span> <span data-ttu-id="0f43f-106">Dynamics 365 Commerce サイト上の検索結果モジュールは、次のシナリオのページの表示に使用できます。</span><span class="sxs-lookup"><span data-stu-id="0f43f-106">Search results modules on Dynamics 365 Commerce sites can be used to render pages for the following scenarios:</span></span>

- <span data-ttu-id="0f43f-107">ユーザーの検索によって開始される検索結果</span><span class="sxs-lookup"><span data-stu-id="0f43f-107">Search results that are initiated by a user search</span></span>
- <span data-ttu-id="0f43f-108">"類似した外観のショップ "など、特定の商品をセットで表示した検索結果です</span><span class="sxs-lookup"><span data-stu-id="0f43f-108">Search results that show a specific set of products, such as "Shop similar looks"</span></span>
- <span data-ttu-id="0f43f-109">指定されたカテゴリに属する製品のリスト</span><span class="sxs-lookup"><span data-stu-id="0f43f-109">Lists of products that belong to a category</span></span>

<span data-ttu-id="0f43f-110">カテゴリや検索結果ページについては、[既定のカテゴリ ランディング ページと検索結果ページの概要](category-search-page-overview.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="0f43f-110">For more information about category and search results pages, see [Default category landing page and search results page overview](category-search-page-overview.md).</span></span>

<span data-ttu-id="0f43f-111">以下の図は、Fabrikam のウェブ サイトのカテゴリの検索結果ページの例です。</span><span class="sxs-lookup"><span data-stu-id="0f43f-111">The following illustration shows an example of a search results page for a category on the Fabrikam site.</span></span>

![Fabrikam のウェブサイトにおける検索結果ページの例](./media/SimpleCategoryLandingDressCategory.png)

## <a name="search-results-module-properties"></a><span data-ttu-id="0f43f-113">検索結果モジュールのプロパティ</span><span class="sxs-lookup"><span data-stu-id="0f43f-113">Search results module properties</span></span>

<span data-ttu-id="0f43f-114">次の表に、検索結果モジュールのプロパティとその値と説明を示します。</span><span class="sxs-lookup"><span data-stu-id="0f43f-114">The following table lists the properties of search result modules, together with their values and descriptions.</span></span>

| <span data-ttu-id="0f43f-115">プロパティ</span><span class="sxs-lookup"><span data-stu-id="0f43f-115">Property</span></span> | <span data-ttu-id="0f43f-116">値</span><span class="sxs-lookup"><span data-stu-id="0f43f-116">Values</span></span> | <span data-ttu-id="0f43f-117">説明</span><span class="sxs-lookup"><span data-stu-id="0f43f-117">Description</span></span> |
|----------|--------|-------------|
| <span data-ttu-id="0f43f-118">ページあたりの品目数</span><span class="sxs-lookup"><span data-stu-id="0f43f-118">Items per page</span></span> | <span data-ttu-id="0f43f-119">整数</span><span class="sxs-lookup"><span data-stu-id="0f43f-119">Integer</span></span> | <span data-ttu-id="0f43f-120">各ページに表示する項目の数です。</span><span class="sxs-lookup"><span data-stu-id="0f43f-120">The number of items that should be shown on each page.</span></span> |
| <span data-ttu-id="0f43f-121">PDP を再度許可する</span><span class="sxs-lookup"><span data-stu-id="0f43f-121">Allow back on PDP</span></span> | <span data-ttu-id="0f43f-122">**True** または **False**</span><span class="sxs-lookup"><span data-stu-id="0f43f-122">**True** or **False**</span></span> | <span data-ttu-id="0f43f-123">このプロパティが **True** に設定されている場合、ユーザーが検索結果ページで製品を選択すると、開いた製品の詳細ページ (PDP) の大画面ナビゲーションに "結果に戻る" リンクが表示されます。</span><span class="sxs-lookup"><span data-stu-id="0f43f-123">If this property is set to **True**, when a user selects a product on the search results page, the breadcrumb navigation on the product details page (PDP) that is opened will show a "Back to results" link.</span></span> |
| <span data-ttu-id="0f43f-124">絞り込み条件の展開</span><span class="sxs-lookup"><span data-stu-id="0f43f-124">Expand Refiners</span></span> | <span data-ttu-id="0f43f-125">**すべて**、**1**、**2**、**3**、**4**</span><span class="sxs-lookup"><span data-stu-id="0f43f-125">**All**, **1**, **2**, **3**, or **4**</span></span> | <span data-ttu-id="0f43f-126">ページが読み込まれたときに展開する上位絞り込み条件の数です。</span><span class="sxs-lookup"><span data-stu-id="0f43f-126">The number of top refiners that should be expanded when a page is loaded.</span></span> <span data-ttu-id="0f43f-127">たとえば、このプロパティが **3** に設定されている場合、ページの最初の3つの絞り込み条件が展開されます。</span><span class="sxs-lookup"><span data-stu-id="0f43f-127">For example, if this property is set to **3**, the first three refiners on the page will be expanded.</span></span> |
| <span data-ttu-id="0f43f-128">カテゴリ階層を非表示にする</span><span class="sxs-lookup"><span data-stu-id="0f43f-128">Hide category hierarchy display</span></span> | <span data-ttu-id="0f43f-129">**True** または **False**</span><span class="sxs-lookup"><span data-stu-id="0f43f-129">**True** or **False**</span></span> | <span data-ttu-id="0f43f-130">このプロパティが **True** に設定されている場合、ページのカテゴリ階層は表示されません。</span><span class="sxs-lookup"><span data-stu-id="0f43f-130">If this property is set to **True**, the category hierarchy display on the page will be hidden.</span></span> <span data-ttu-id="0f43f-131">[パンくずモジュール](add-breadcrumb.md)を使用してカテゴリ階層を表示する場合、このプロパティは **True** に設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="0f43f-131">This property should be set to **True** if you're using the [breadcrumb module](add-breadcrumb.md) to show the category hierarchy.</span></span>|
| <span data-ttu-id="0f43f-132">検索結果に製品属性を含める</span><span class="sxs-lookup"><span data-stu-id="0f43f-132">Include product attributes in search results</span></span> | <span data-ttu-id="0f43f-133">**True** または **False**</span><span class="sxs-lookup"><span data-stu-id="0f43f-133">**True** or **False**</span></span> | <span data-ttu-id="0f43f-134">このプロパティが **True** に設定されている場合、検索結果の商品に対して属性が返されます。</span><span class="sxs-lookup"><span data-stu-id="0f43f-134">If this property is set to **True**, attributes will be returned for the products in the search results.</span></span> <span data-ttu-id="0f43f-135">これらの属性を Commerce サイトに表示することもできますが、その場合は拡張機能が必要です。</span><span class="sxs-lookup"><span data-stu-id="0f43f-135">Although these attributes can be shown on a Commerce site, an extension is required.</span></span>|
| <span data-ttu-id="0f43f-136">所属価格の表示</span><span class="sxs-lookup"><span data-stu-id="0f43f-136">Show affiliation prices</span></span> | <span data-ttu-id="0f43f-137">**True** または **False**</span><span class="sxs-lookup"><span data-stu-id="0f43f-137">**True** or **False**</span></span> | <span data-ttu-id="0f43f-138">このプロパティが **True** に設定されている場合、ユーザーがサインイン ページを参照すると、検索結果に製品の所属価格が表示されます。</span><span class="sxs-lookup"><span data-stu-id="0f43f-138">If this property is set to **True**, affiliation prices for products will be shown in the search results when a signed-in user browses the page.</span></span> |
| <span data-ttu-id="0f43f-139">絞り込み条件パネルの更新</span><span class="sxs-lookup"><span data-stu-id="0f43f-139">Update refiner panel</span></span> | <span data-ttu-id="0f43f-140">**True** または **False**</span><span class="sxs-lookup"><span data-stu-id="0f43f-140">**True** or **False**</span></span> | <span data-ttu-id="0f43f-141">このプロパティが **True** に設定されている場合、絞り込み条件を選択すると、絞り込み条件パネルが更新されます。</span><span class="sxs-lookup"><span data-stu-id="0f43f-141">If this property is set to **True**, the refiner panel will be updated when refiners are selected.</span></span> <span data-ttu-id="0f43f-142">このモードでは、複数選択が可能な絞り込み条件は、絞り込み条件パネルを更新するときに単一選択の絞り込み条件のように動作します。</span><span class="sxs-lookup"><span data-stu-id="0f43f-142">In this mode, some multiple-selection refiners will behave like single-selection refiners when the refiner panel is updated.</span></span> |

> [!IMPORTANT]
> <span data-ttu-id="0f43f-143">Commerce バージョン 10.0.16 リリース以降では、**所属価格の表示** の構成を使用して、ページに所属価格を表示できます。</span><span class="sxs-lookup"><span data-stu-id="0f43f-143">In the Commerce version 10.0.16 release and later, the **Show affiliation prices** configuration can be used to show affiliation prices on the page.</span></span>
>
> <span data-ttu-id="0f43f-144">Commerce バージョン 10.0.20 リリース以降では、**絞り込み条件パネルの更新** の構成を使用して、絞り込み条件の選択時に絞り込みパネルを更新できます。</span><span class="sxs-lookup"><span data-stu-id="0f43f-144">In the Commerce version 10.0.20 release and later, the **Update refiner panel** configuration can be used to update the refiner panel during refiner selection.</span></span>

## <a name="supported-modules"></a><span data-ttu-id="0f43f-145">サポートされているモジュール</span><span class="sxs-lookup"><span data-stu-id="0f43f-145">Supported modules</span></span>

<span data-ttu-id="0f43f-146">検索結果モジュールは、[クイックビューモジュール](quick-view-module.md)に対応しているため、ユーザーは製品収集ページから商品情報を表示し、カートに商品を追加できます。</span><span class="sxs-lookup"><span data-stu-id="0f43f-146">The search results module supports the [quick view module](quick-view-module.md), which lets users view product information and add items to the cart from the search results page.</span></span>

## <a name="add-a-search-results-module-to-a-category-page"></a><span data-ttu-id="0f43f-147">カテゴリ ページに検索結果モジュールを追加する</span><span class="sxs-lookup"><span data-stu-id="0f43f-147">Add a search results module to a category page</span></span>

<span data-ttu-id="0f43f-148">検索結果モジュールをカテゴリ ページに追加するには、以下の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="0f43f-148">To add a search results module to a category page, follow these steps.</span></span>

1. <span data-ttu-id="0f43f-149">**テンプレート** に移動し、**新規** を選択して新たなテンプレートを作成します。</span><span class="sxs-lookup"><span data-stu-id="0f43f-149">Go to **Templates**, and select **New** to create a new template.</span></span>
1. <span data-ttu-id="0f43f-150">**新規テンプレート** ダイアログボックスで、**検索結果** を入力し、**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="0f43f-150">In the **New template** dialog box, enter the name **Search results**, and then select **OK**.</span></span>
1. <span data-ttu-id="0f43f-151">**本文** スロットの省略ボタン (...) を選択し、**モジュールの追加** を選択します。</span><span class="sxs-lookup"><span data-stu-id="0f43f-151">In the **Body** slot, select the ellipsis (...), and then select **Add Module**.</span></span>
1. <span data-ttu-id="0f43f-152">**モジュールの追加** ダイアログ ボックスで、**規定のページ** モジュールを選択して、**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="0f43f-152">In the **Add Module** dialog box, select the **Default Page** module, and then select **OK**.</span></span>
1. <span data-ttu-id="0f43f-153">**既定のページ** モジュールの **メイン** スロットで、省略記号ボタン (...) を選択し、**モジュールの追加**.を選択します。</span><span class="sxs-lookup"><span data-stu-id="0f43f-153">In the **Main** slot of the **Default Page** module, select the ellipsis (...), and then select **Add Module**.</span></span>
1. <span data-ttu-id="0f43f-154">**モジュールの追加** ダイアログ ボックスで、**コンテナー** モジュールを選択して、**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="0f43f-154">In the **Add Module** dialog box, select the **Container** module, and then select **OK**.</span></span>
1. <span data-ttu-id="0f43f-155">**コンテナー** スロットの省略ボタン (...) を選択し、**モジュールの追加** を選択します。</span><span class="sxs-lookup"><span data-stu-id="0f43f-155">In the **Container** slot, select the ellipsis (...), and then select **Add Module**.</span></span>
1. <span data-ttu-id="0f43f-156">**モジュールの追加** ダイアログ ボックスで、**階層リンク** モジュールを選択して、**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="0f43f-156">In the **Add Module** dialog box, select the **Breadcrumb** module, and then select **OK**.</span></span>
1. <span data-ttu-id="0f43f-157">**パンくず** プロパティで、 **Min Occurs** に 値 : **1** を入力します。</span><span class="sxs-lookup"><span data-stu-id="0f43f-157">In the **Breadcrumb** properties pane, enter the value **1** for **Min Occurs**.</span></span>
1. <span data-ttu-id="0f43f-158">**コンテナー** スロットの省略ボタン (...) を選択し、**モジュールの追加** を選択します。</span><span class="sxs-lookup"><span data-stu-id="0f43f-158">In the **Container** slot, select the ellipsis (...), and then select **Add Module**.</span></span>
1. <span data-ttu-id="0f43f-159">**モジュールの追加** ダイアログ ボックスで、**検索結果** モジュールを選択して、**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="0f43f-159">In the **Add Module** dialog box, select the **Search results** module, and then select **OK**.</span></span>
1. <span data-ttu-id="0f43f-160">**検索結果のプロパティ** ウィンドウで、**Min Occurs** の値に **1** を入力し、検索結果モジュールに必要なその他の プロパティを設定します。</span><span class="sxs-lookup"><span data-stu-id="0f43f-160">In the **Search results** properties pane, enter the value **1** for **Min Occurs**, and then set any other required properties for the search results module.</span></span> <span data-ttu-id="0f43f-161">テンプレートでこれらのプロパティを設定することで、特定のカテゴリページへのカスタマイズに、自動的にこれらの設定が含まれるようになります。</span><span class="sxs-lookup"><span data-stu-id="0f43f-161">By setting these properties in the template, you ensure that any customizations to a specific category page will automatically include these settings.</span></span>
1. <span data-ttu-id="0f43f-162">**編集の完了** を選択し、 **発行** を選択してテンプレートを公開します。</span><span class="sxs-lookup"><span data-stu-id="0f43f-162">Select **Finish editing**, and then select **Publish** to publish the template.</span></span>
1. <span data-ttu-id="0f43f-163">**ページ** に移動し、**新規** を選択して新たなページを作成します。</span><span class="sxs-lookup"><span data-stu-id="0f43f-163">Go to **Pages**, and select **New** to create a new page.</span></span>
1. <span data-ttu-id="0f43f-164">**テンプレートの選択** ダイアログ ボックスで、作成した **検索結果** テンプレートを選択し、**ページ名** の **カテゴリ ページ** を入力して、**OK** を選択します 。</span><span class="sxs-lookup"><span data-stu-id="0f43f-164">In the **Choose a template** dialog box, select the **Search results** template that you created, enter **Category page** for **Page name**, and then select **OK**.</span></span> <span data-ttu-id="0f43f-165">テンプレートにはすべての値が設定されているため、ページを公開する準備ができています。</span><span class="sxs-lookup"><span data-stu-id="0f43f-165">Because all the values are set in the template, the page is ready to be published.</span></span>
1. <span data-ttu-id="0f43f-166">**編集の完了** を選択してページをチェックインし、 **発行** を選択して公開します。</span><span class="sxs-lookup"><span data-stu-id="0f43f-166">Select **Finish editing** to check in the page, and then select **Publish** to publish it.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="0f43f-167">追加リソース</span><span class="sxs-lookup"><span data-stu-id="0f43f-167">Additional resources</span></span>

[<span data-ttu-id="0f43f-168">既定のカテゴリ ランディング ページと検索結果ページの概要</span><span class="sxs-lookup"><span data-stu-id="0f43f-168">Default category landing page and search results page overview</span></span>](category-search-page-overview.md)

[<span data-ttu-id="0f43f-169">モジュール ライブラリの概要</span><span class="sxs-lookup"><span data-stu-id="0f43f-169">Module library overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="0f43f-170">クイック ビュー モジュール</span><span class="sxs-lookup"><span data-stu-id="0f43f-170">Quick view module</span></span>](quick-view-module.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
