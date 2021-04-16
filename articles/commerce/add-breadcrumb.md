---
title: 階層リンク モジュール
description: このトピックでは、 breadcrumb モジュールと Microsoft Dynamics 365 Commerce のサイト ページにそれを追加する方法について説明します。
author: anupamar-ms
ms.date: 10/20/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: ''
ms.openlocfilehash: e7b7cff280d8c6bcb09f2f59d96ec415b9cc1167
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/31/2021
ms.locfileid: "5796201"
---
# <a name="breadcrumb-module"></a><span data-ttu-id="36fe4-103">階層リンク モジュール</span><span class="sxs-lookup"><span data-stu-id="36fe4-103">Breadcrumb module</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="36fe4-104">このトピックでは、 breadcrumb モジュールと Microsoft Dynamics 365 Commerce のサイト ページにそれを追加する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="36fe4-104">This topic covers breadcrumb modules and describes how to add them to site pages in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="36fe4-105">階層リンク モジュールは、サイト ページにおけるセカンダリ ナビゲーションを提供する目的で使用されます。</span><span class="sxs-lookup"><span data-stu-id="36fe4-105">Breadcrumb modules are used to provide secondary navigation on site pages.</span></span> <span data-ttu-id="36fe4-106">通常は、ページ上部のヘッダー下部に表示されます。</span><span class="sxs-lookup"><span data-stu-id="36fe4-106">They are typically shown at the top of a page, below the header.</span></span> <span data-ttu-id="36fe4-107">階層リンク モジュールは任意のページに追加することができますが、製品カテゴリの階層を示す、またはサイト内を簡単に移動する方法として、製品の詳細ページ (PDPs) 上で使用される場合が多く見られます。</span><span class="sxs-lookup"><span data-stu-id="36fe4-107">Although breadcrumb modules can be added to any page, they are most often used on product details pages (PDPs), to show the product category hierarchy and provide a quick way to move around a site.</span></span> <span data-ttu-id="36fe4-108">また、ユーザーが検索ページまたは一覧ページから PDP を開く際に、階層リンク モジュールを使用して [結果に戻る] リンクを表示することもできます。</span><span class="sxs-lookup"><span data-stu-id="36fe4-108">A breadcrumb module can also be used to show a "Back to results" link when users open a PDP from a search or list page.</span></span> <span data-ttu-id="36fe4-109">これにより、ユーザーは簡単に [フィルタ処理済リスト] のページに戻って買い物を続けることができます。</span><span class="sxs-lookup"><span data-stu-id="36fe4-109">In this way, users can quickly return to their filtered list page to continue shopping.</span></span>

<span data-ttu-id="36fe4-110">PDPs やカテゴリ ページなど、製品カテゴリのコンテキストを持つページでは、階層リンク モジュールがカテゴリの階層を示します。</span><span class="sxs-lookup"><span data-stu-id="36fe4-110">On pages that have product category context, such as PDPs and category pages, breadcrumb modules show the category hierarchy.</span></span> <span data-ttu-id="36fe4-111">カテゴリのコンテキストを持たないページでは、階層リンク モジュールに既定で、 **&lt;サイトのルート&gt; / &lt;現在のページ&gt;** が表示されます。</span><span class="sxs-lookup"><span data-stu-id="36fe4-111">On pages that don't have category context, breadcrumb modules show **&lt;Site root&gt; / &lt;Current page&gt;** by default.</span></span> <span data-ttu-id="36fe4-112">また別の種類のサイト ページに、階層リンク モジュールを手動で構成して、サイトの特定のページへのリンクを表示することもできます。</span><span class="sxs-lookup"><span data-stu-id="36fe4-112">Breadcrumb modules can also be manually configured on other types of site pages to show links to specific pages on the site.</span></span>

> [!NOTE]
> <span data-ttu-id="36fe4-113">階層リンク モジュールは、Dynamics 365 Commerce のリリース バージョン 10.0.12 で入手できます。</span><span class="sxs-lookup"><span data-stu-id="36fe4-113">The breadcrumb module is available in the Dynamics 365 Commerce 10.0.12 release.</span></span>

<span data-ttu-id="36fe4-114">次の図では、PDP のカテゴリ階層を表示する階層リンク モジュールの例を示しています。</span><span class="sxs-lookup"><span data-stu-id="36fe4-114">The following image shows an example of a breadcrumb module that shows the category hierarchy on a PDP.</span></span>

![階層リンク モジュールの例](./media/ecommerce-breadcrumb.PNG)

## <a name="breadcrumb-module-settings"></a><span data-ttu-id="36fe4-116">階層リンク モジュールの設定</span><span class="sxs-lookup"><span data-stu-id="36fe4-116">Breadcrumb module settings</span></span>

<span data-ttu-id="36fe4-117">階層リンク モジュールは、サイト ビルダーの **サイト設定 \> 拡張** で定義されている、**PDP 上の階層リンク モジュール タイプ** の設定に依存します。</span><span class="sxs-lookup"><span data-stu-id="36fe4-117">The breadcrumb module relies on the **Breadcrumb display type on PDP** setting, which is defined at **Site Settings \> Extensions** in site builder.</span></span> <span data-ttu-id="36fe4-118">この設定には、3つの値があります :</span><span class="sxs-lookup"><span data-stu-id="36fe4-118">This setting has three possible values:</span></span>

- <span data-ttu-id="36fe4-119">**カテゴリ階層を表示する** - この値が選択されている場合、階層リンク モジュールには、PDP に表示される製品のカテゴリ階層全体が表示されます。</span><span class="sxs-lookup"><span data-stu-id="36fe4-119">**Show category hierarchy** – When this value is selected, the breadcrumb module will show the full category hierarchy of the product that is viewed on the PDP.</span></span>
- <span data-ttu-id="36fe4-120">**結果に戻る** - この値が選択されている場合、[結果に戻る] リンクを有効化しているモジュールから PDP を開いた場合、階層リンク モジュールによって PDP 上に [結果に戻る] リンクが表示されます。</span><span class="sxs-lookup"><span data-stu-id="36fe4-120">**Show back to results** – When this value is selected, the breadcrumb module will show a "Back to results" link on a PDP if the user opened the PDP from a module that allows for a "Back to results" link.</span></span> <span data-ttu-id="36fe4-121">この機能は、カテゴリ、検索、リスト、推奨事項リスト ページからユーザーが移動する際に使用できます。</span><span class="sxs-lookup"><span data-stu-id="36fe4-121">This functionality is available when users navigate from category, search, list, and recommendation lists pages.</span></span> <span data-ttu-id="36fe4-122">この機能に対応するために、製品コレクションおよび検索結果モジュールには、**PDP で結果に戻ることを許可する** という名前のプロパティがあり ます。</span><span class="sxs-lookup"><span data-stu-id="36fe4-122">To support this functionality, product collection and search results modules have a property that is named **Allow back to results on PDP**.</span></span> <span data-ttu-id="36fe4-123">このプロパティは、、どのモジュールが PDP の [結果に戻る] のリンク機能をサポートするかを柔軟に定義できます。</span><span class="sxs-lookup"><span data-stu-id="36fe4-123">This property gives you the flexibility to define which modules should support the "Back to results" link functionality on the PDP.</span></span> <span data-ttu-id="36fe4-124">たとえば、階層リンク モジュールの **PDP における階層リンクの表示タイプ** の設定に **結果に戻るを表示する** が設定されており、検索結果モジュールの検索ページに **PDP で結果に戻ることを許可する** が設定されている場合は、ユーザーが検索ページから PDP に移動する際に「結果に戻る」のリンクが表示されます。</span><span class="sxs-lookup"><span data-stu-id="36fe4-124">For example, when **Show back to results** is selected for the **Breadcrumb display type on PDP** setting of the breadcrumb module, and **Allow back to results on PDP** is selected for the search page search results module, a "Back to results" link will be shown when users navigate from the search page to a PDP.</span></span>
- <span data-ttu-id="36fe4-125">**カテゴリの階層を表示し、結果に戻る** - この値は、前述の 2 つの組み合わせです。</span><span class="sxs-lookup"><span data-stu-id="36fe4-125">**Show category hierarchy and back to results** – This value is a combination of the previous two.</span></span> <span data-ttu-id="36fe4-126">この値を選択すると、階層リンク モジュールに、PDP 上のカテゴリ階層全体と 「結果に戻る」 リンク (構成されている場合) の両方が表示されます。</span><span class="sxs-lookup"><span data-stu-id="36fe4-126">When this value is selected, the breadcrumb module will show both the full category hierarchy and a "Back to results" link (if it's configured) on a PDP.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="36fe4-127">これらの設定は、Dynamics 365 Commerce のリリース バージョン 10.0.12 で使用可能です。</span><span class="sxs-lookup"><span data-stu-id="36fe4-127">These settings are available in the Dynamics 365 Commerce 10.0.12 release.</span></span> <span data-ttu-id="36fe4-128">古いバージョンの Dynamics 365 Commerce を更新する場合は、appsettings.json ファイルを手動で更新する必要があります。</span><span class="sxs-lookup"><span data-stu-id="36fe4-128">If you are updating from an older version of Dynamics 365 Commerce, you must manually update the appsettings.json file.</span></span> <span data-ttu-id="36fe4-129">appsettings.json ファイルを更新する手順については、[SDK およびモジュール ライブラリの更新](e-commerce-extensibility/sdk-updates.md#update-the-appsettingsjson-file)を参照してください 。</span><span class="sxs-lookup"><span data-stu-id="36fe4-129">For instructions on updating the appsettings.json file, see [SDK and module library updates](e-commerce-extensibility/sdk-updates.md#update-the-appsettingsjson-file).</span></span>

## <a name="breadcrumb-module-properties"></a><span data-ttu-id="36fe4-130">階層リンク モジュールのプロパティ</span><span class="sxs-lookup"><span data-stu-id="36fe4-130">Breadcrumb module properties</span></span>

| <span data-ttu-id="36fe4-131">プロパティ名</span><span class="sxs-lookup"><span data-stu-id="36fe4-131">Property name</span></span> | <span data-ttu-id="36fe4-132">値</span><span class="sxs-lookup"><span data-stu-id="36fe4-132">Values</span></span> | <span data-ttu-id="36fe4-133">説明</span><span class="sxs-lookup"><span data-stu-id="36fe4-133">Description</span></span> |
|---------------|--------|-------------|
| <span data-ttu-id="36fe4-134">ルート</span><span class="sxs-lookup"><span data-stu-id="36fe4-134">Root</span></span> | <span data-ttu-id="36fe4-135">テキストまたはリンク</span><span class="sxs-lookup"><span data-stu-id="36fe4-135">Text or link</span></span>| <span data-ttu-id="36fe4-136">このオプションのプロパティでは、階層リンク サイト ルートに対するリンク テキストとリンクのターゲットを指定します。</span><span class="sxs-lookup"><span data-stu-id="36fe4-136">This optional property specifies link text and a link target for the breadcrumb site root.</span></span> <span data-ttu-id="36fe4-137">このプロパティが構成されていない場合、ルートは定義されません。</span><span class="sxs-lookup"><span data-stu-id="36fe4-137">If this property isn't configured, no root will be defined.</span></span> |
| <span data-ttu-id="36fe4-138">階層リンク</span><span class="sxs-lookup"><span data-stu-id="36fe4-138">Breadcrumb link</span></span> | <span data-ttu-id="36fe4-139">リンク</span><span class="sxs-lookup"><span data-stu-id="36fe4-139">Link</span></span> | <span data-ttu-id="36fe4-140">このオプションのプロパティは、手動で構成された階層リンクで使用するリンクが必要な場合に指定します。</span><span class="sxs-lookup"><span data-stu-id="36fe4-140">This optional property specifies links for a manually configured breadcrumb, if these links are required.</span></span> <span data-ttu-id="36fe4-141">リンクは、一覧に表示されている順序で表示されます。</span><span class="sxs-lookup"><span data-stu-id="36fe4-141">Links appear in the order that they are listed in.</span></span> |

## <a name="add-a-breadcrumb-module-to-a-new-page"></a><span data-ttu-id="36fe4-142">階層リンク モジュールを新しいページに追加する</span><span class="sxs-lookup"><span data-stu-id="36fe4-142">Add a breadcrumb module to a new page</span></span>

<span data-ttu-id="36fe4-143">PDP に階層リンク モジュールを追加して必要なプロパティを設定するには、次の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="36fe4-143">To add a breadcrumb module to a PDP and set the required properties, follow these steps.</span></span>

1. <span data-ttu-id="36fe4-144">**サイト設定 \> 拡張機能** に移動し、その後 **PDP 上のブレッドクラム表示タイプ** 設定に対して、**カテゴリ階層を表示** を選択します。</span><span class="sxs-lookup"><span data-stu-id="36fe4-144">Go to **Site Settings \> Extensions**, and then, for the **Breadcrumb display type on PDP** setting, select **Show category hierarchy**.</span></span>
1. <span data-ttu-id="36fe4-145">**テンプレート** に移動 し、PDP テンプレートを選択します。</span><span class="sxs-lookup"><span data-stu-id="36fe4-145">Go to **Templates**, and select the PDP template.</span></span>
1. <span data-ttu-id="36fe4-146">購入用ボックス モジュールを含む **コンテナ** スロットにて、省略記号  (**...**) を選択し、**モジュールの追加** を選択します。</span><span class="sxs-lookup"><span data-stu-id="36fe4-146">In the **Container** slot that contains the buy box module, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="36fe4-147">**モジュールの追加** ダイアログ ボックスで、**階層リンク** モジュールを選択して、**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="36fe4-147">In the **Add Module** dialog box, select the **Breadcrumb** module, and then select **OK**.</span></span>
1. <span data-ttu-id="36fe4-148">**保存** を選択し、 **編集の完了** を選択してテンプレートをチェックインし、**発行** を選択して公開します。</span><span class="sxs-lookup"><span data-stu-id="36fe4-148">Select **Save**, select **Finish editing** to check in the template, and then select **Publish** to publish it.</span></span>
1. <span data-ttu-id="36fe4-149">**ページ** に移動 し、PDP テンプレートを使用している PDP を開きます。</span><span class="sxs-lookup"><span data-stu-id="36fe4-149">Go to **Pages**, and open a PDP that uses the PDP template.</span></span> <span data-ttu-id="36fe4-150">PDP がまだ存在しない場合は、作成します。</span><span class="sxs-lookup"><span data-stu-id="36fe4-150">If a PDP doesn't yet exist, create one.</span></span>
1. <span data-ttu-id="36fe4-151">購入用ボックス モジュールを含む **コンテナ** スロットにて、省略記号  (**...**) を選択し、**モジュールの追加** を選択します。</span><span class="sxs-lookup"><span data-stu-id="36fe4-151">In the **Container** slot that contains the buy box module, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="36fe4-152">**モジュールの追加** ダイアログ ボックスで、**階層リンク** モジュールを選択して、**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="36fe4-152">In the **Add Module** dialog box, select the **Breadcrumb** module, and then select **OK**.</span></span>
1. <span data-ttu-id="36fe4-153">**ルート** 配下にある、**階層リンク** スロットのプロパティ ウィンドウで、 **リンク テキスト** を選択します。</span><span class="sxs-lookup"><span data-stu-id="36fe4-153">In the properties pane of the **Breadcrumb** slot, under **Root**, select **Link text**.</span></span>
1. <span data-ttu-id="36fe4-154">**リンク ターゲット** 配下の、**リンク テキスト** ダイアログ ボックスで **ホーム** と入力し、**リンクの追加** を選択し ます。</span><span class="sxs-lookup"><span data-stu-id="36fe4-154">In the **Link text** dialog box, enter **Home**, and then, under **Link target**, select **Add a link**.</span></span>
1. <span data-ttu-id="36fe4-155">**リンクの追加** ダイアログ ボックスで、階層リンクで使用するリンクを選択し、**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="36fe4-155">In the **Add a link** dialog box, select a link for the breadcrumb root, and then select **OK**.</span></span>
1. <span data-ttu-id="36fe4-156">**保存** を選択し、 続いて **プレビュー** を選択してページをプレビューします。</span><span class="sxs-lookup"><span data-stu-id="36fe4-156">Select **Save**, and then select **Preview** to preview the page.</span></span>
1. <span data-ttu-id="36fe4-157">**編集の完了**  を選択してテンプレートをチェックインし、 **発行** を選択して公開します。</span><span class="sxs-lookup"><span data-stu-id="36fe4-157">Select **Finish editing** to check in the template, and then select **Publish** to publish it.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="36fe4-158">追加リソース</span><span class="sxs-lookup"><span data-stu-id="36fe4-158">Additional resources</span></span>

[<span data-ttu-id="36fe4-159">モジュール ライブラリの概要</span><span class="sxs-lookup"><span data-stu-id="36fe4-159">Module library overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="36fe4-160">ナビゲーション メニュー モジュール</span><span class="sxs-lookup"><span data-stu-id="36fe4-160">Navigation menu module</span></span>](nav-menu-module.md)

[<span data-ttu-id="36fe4-161">サイト セレクター モジュール</span><span class="sxs-lookup"><span data-stu-id="36fe4-161">Site selector module</span></span>](site-selector.md)

[<span data-ttu-id="36fe4-162">既定のカテゴリ ランディング ページと検索結果ページの概要</span><span class="sxs-lookup"><span data-stu-id="36fe4-162">Overview of default category landing page and search results page</span></span>](category-search-page-overview.md)

[<span data-ttu-id="36fe4-163">製品収集モジュール</span><span class="sxs-lookup"><span data-stu-id="36fe4-163">Product collection modules</span></span>](product-collection-module-overview.md)

[<span data-ttu-id="36fe4-164">購入ボックス モジュール</span><span class="sxs-lookup"><span data-stu-id="36fe4-164">Buy box module</span></span>](add-buy-box.md)

[<span data-ttu-id="36fe4-165">SDK およびモジュール ライブラリの更新</span><span class="sxs-lookup"><span data-stu-id="36fe4-165">SDK and module library updates</span></span>](e-commerce-extensibility/sdk-updates.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]