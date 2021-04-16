---
title: サイト ナビゲーションのカスタマイズ
description: このトピックでは、カスタマイズされたオンライン ナビゲーション階層を作成して、Microsoft Dynamics 365 Commerce サイトで参照するため製品を整理する方法について説明します。
author: bicyclingfool
ms.date: 09/15/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: StuHarg
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 5bc50243ac3845adc60bfc173fc532fb28f3cdf6
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/31/2021
ms.locfileid: "5799352"
---
# <a name="customize-site-navigation"></a><span data-ttu-id="16234-103">サイト ナビゲーションのカスタマイズ</span><span class="sxs-lookup"><span data-stu-id="16234-103">Customize site navigation</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="16234-104">このトピックでは、カスタマイズされたオンライン ナビゲーション階層を作成して、Microsoft Dynamics 365 Commerce サイトで参照するため製品を整理する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="16234-104">This topic describes how to create a customized online navigation hierarchy to organize your products for browsing on your Microsoft Dynamics 365 Commerce site.</span></span>

<span data-ttu-id="16234-105">オンライン店舗では、製品カテゴリを移動することで、顧客は製品を検索して参照することができます。</span><span class="sxs-lookup"><span data-stu-id="16234-105">Online storefronts typically let customers discover and browse products by navigating through product categories.</span></span> <span data-ttu-id="16234-106">この機能は通常、ページ上部にあるタブまたは左側にあるナビゲーション バーによって提供されます。</span><span class="sxs-lookup"><span data-stu-id="16234-106">This capability is usually provided by tabs at the top of the page or by a navigation bar on the left.</span></span> <span data-ttu-id="16234-107">Dynamics 365 Commerce では、カテゴリ ナビゲーションの階層構造と、さまざまなカテゴリに含まれる製品を作成および管理できます。</span><span class="sxs-lookup"><span data-stu-id="16234-107">In Dynamics 365 Commerce, you can create and manage the hierarchal structure of your category navigation and the products that are included in the various categories.</span></span>

## <a name="create-a-channel-navigation-hierarchy"></a><span data-ttu-id="16234-108">チャネル ナビゲーション階層の作成</span><span class="sxs-lookup"><span data-stu-id="16234-108">Create a channel navigation hierarchy</span></span>

<span data-ttu-id="16234-109">チャネルのナビゲーション階層を作成するには、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="16234-109">To create a channel navigation hierarchy, follow these steps.</span></span>

1. <span data-ttu-id="16234-110">**Retail と Commerce \> 製品とカテゴリ \> カテゴリと製品の管理** に移動します。</span><span class="sxs-lookup"><span data-stu-id="16234-110">Go to **Retail and Commerce \> Products and categories \> Category and product management**.</span></span>
1. <span data-ttu-id="16234-111">**カテゴリ階層** を選択し、**新規** を選択します。</span><span class="sxs-lookup"><span data-stu-id="16234-111">Select **Category hierarchies**, and then select **New**.</span></span>
1. <span data-ttu-id="16234-112">階層に名前を付けます。</span><span class="sxs-lookup"><span data-stu-id="16234-112">Name the hierarchy.</span></span>

    > [!NOTE]
    > <span data-ttu-id="16234-113">作成する最上位カテゴリは、ルート カテゴリ ノードです。</span><span class="sxs-lookup"><span data-stu-id="16234-113">The topmost category that you create is the root category node.</span></span> <span data-ttu-id="16234-114">サイトには表示されません。</span><span class="sxs-lookup"><span data-stu-id="16234-114">It won't be shown on your site.</span></span> <span data-ttu-id="16234-115">サイトに単一のトップ レベル ノードが表示されているカテゴリ階層を作成するには、カテゴリを作成し、ルート カテゴリの子として名前を付けます。</span><span class="sxs-lookup"><span data-stu-id="16234-115">To create a category hierarchy where a single top-level node is shown on your site, create and name the category as a child of the root category.</span></span>

1. <span data-ttu-id="16234-116">**新しいカテゴリ ノード** を選択し、カテゴリに名前を付けます。</span><span class="sxs-lookup"><span data-stu-id="16234-116">Select **New category node**, and name the category.</span></span>
1. <span data-ttu-id="16234-117">必要に応じて、兄弟カテゴリと子カテゴリの作成を続行します。</span><span class="sxs-lookup"><span data-stu-id="16234-117">Continue to create sibling and child categories as you require.</span></span>

<span data-ttu-id="16234-118">トップレベルのカテゴリの下に作成した各カテゴリに製品を割り当てることができるようになりました。</span><span class="sxs-lookup"><span data-stu-id="16234-118">You can now assign products to each category that you created under the top-level category.</span></span>

## <a name="customize-the-order-of-categories"></a><span data-ttu-id="16234-119">カテゴリの順序のカスタマイズ</span><span class="sxs-lookup"><span data-stu-id="16234-119">Customize the order of categories</span></span>

<span data-ttu-id="16234-120">既定では、定義したカテゴリはサイトでアルファベット順に表示されます。</span><span class="sxs-lookup"><span data-stu-id="16234-120">By default, the categories that you define will appear in alphabetical order on your site.</span></span> <span data-ttu-id="16234-121">ただし、カテゴリの表示順序をカスタマイズすることもできます。</span><span class="sxs-lookup"><span data-stu-id="16234-121">However, you can also customize the display order of categories.</span></span>

## <a name="assign-a-category-hierarchy-type"></a><span data-ttu-id="16234-122">カテゴリ階層タイプの割り当て</span><span class="sxs-lookup"><span data-stu-id="16234-122">Assign a category hierarchy type</span></span>

1. <span data-ttu-id="16234-123">**Retail と Commerce \> 製品とカテゴリ \> カテゴリと製品の管理** に移動します。</span><span class="sxs-lookup"><span data-stu-id="16234-123">Go to **Retail and Commerce \> Products and categories \> Category and product management**.</span></span>
1. <span data-ttu-id="16234-124">**カテゴリ階層** を選択します。</span><span class="sxs-lookup"><span data-stu-id="16234-124">Select **Category hierarchies**.</span></span>
1. <span data-ttu-id="16234-125">アクション ペイン、**カテゴリ階層** タブの、**設定** グループで、**階層タイプの関連付け** を選択します。</span><span class="sxs-lookup"><span data-stu-id="16234-125">On the Action Pane, on the **Category hierarchy** tab, in the **Set up** group, select **Associate hierarchy type**.</span></span>
1. <span data-ttu-id="16234-126">**新規** を選択します。</span><span class="sxs-lookup"><span data-stu-id="16234-126">Select **New**.</span></span>
1. <span data-ttu-id="16234-127">**カテゴリ階層タイプ** フィールドで、**チャネル ナビゲーション階層** を選択します。</span><span class="sxs-lookup"><span data-stu-id="16234-127">In the **Category hierarchy type** field, select **Channel navigation hierarchy**.</span></span>
1. <span data-ttu-id="16234-128">**カテゴリ階層** フィールドで、以前に作成したチャンネル ナビゲーション階層を選択します。</span><span class="sxs-lookup"><span data-stu-id="16234-128">In the **Category hierarchy** field, select the channel navigation hierarchy that you created earlier.</span></span>

## <a name="publish-new-or-updated-navigation-hierarchies"></a><span data-ttu-id="16234-129">新規または更新されたナビゲーション階層の公開</span><span class="sxs-lookup"><span data-stu-id="16234-129">Publish new or updated navigation hierarchies</span></span>

<span data-ttu-id="16234-130">オンライン店舗でナビゲーション階層を使用できるようにするには、次の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="16234-130">To make your navigation hierarchy available to your online storefront, follow these steps.</span></span>

1. <span data-ttu-id="16234-131">**Retail と Commerce \> チャネル設定 \> チャネル カテゴリと製品属性** に移動します。</span><span class="sxs-lookup"><span data-stu-id="16234-131">Go to **Retail and Commerce \> Channel setup \> Channel categories and product attributes**.</span></span>
1. <span data-ttu-id="16234-132">左側のツリーで、オンライン ストアを選択します。</span><span class="sxs-lookup"><span data-stu-id="16234-132">In the tree on the left, select your online store.</span></span>
1. <span data-ttu-id="16234-133">**チャネル更新の公開** を選択します。</span><span class="sxs-lookup"><span data-stu-id="16234-133">Select **Publish channel updates**.</span></span>
1. <span data-ttu-id="16234-134">**Retail とコマース \> Retail とコマース IT \> 配送スケジュール** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="16234-134">Go to **Retail and Commerce \> Retail and Commerce IT \> Distribution schedule**.</span></span>
1. <span data-ttu-id="16234-135">一覧から **ジョブ 1040** を見つけ、選択します。</span><span class="sxs-lookup"><span data-stu-id="16234-135">In the list, find and select **Job 1040**.</span></span>
1. <span data-ttu-id="16234-136">**今すぐ実行** を選択します。</span><span class="sxs-lookup"><span data-stu-id="16234-136">Select **Run now**.</span></span>
1. <span data-ttu-id="16234-137">ジョブ 1070 および 1150 についても、手順 5 と 6 を繰り返します。</span><span class="sxs-lookup"><span data-stu-id="16234-137">Repeat steps 5 and 6 for jobs 1070 and 1150.</span></span>

## <a name="show-categories-on-your-site"></a><span data-ttu-id="16234-138">サイトにカテゴリを表示する</span><span class="sxs-lookup"><span data-stu-id="16234-138">Show categories on your site</span></span>

<span data-ttu-id="16234-139">オンライン店舗でカテゴリ階層を表示するには、テンプレートまたはフラグメント内の適切な場所にナビゲーション メニュー モジュールを追加する必要があります。</span><span class="sxs-lookup"><span data-stu-id="16234-139">To show your category hierarchy on your online storefront, you must add the navigation menu module in the appropriate location in a template or fragment.</span></span> <span data-ttu-id="16234-140">サイトがバインドされているチャンネルにナビゲーション階層を公開している場合は、ナビゲーション メニュー モジュールにナビゲーション階層が表示されます。</span><span class="sxs-lookup"><span data-stu-id="16234-140">The navigation menu module will then show your navigation hierarchy, provided that you've published your navigation hierarchy to the channel that your site is bound to.</span></span>

> [!NOTE]
> <span data-ttu-id="16234-141">モジュール ライブラリに含まれているナビゲーション メニュー モジュールを使用することで、ユーザーはサブカテゴリを持たないカテゴリにのみ移動できます。</span><span class="sxs-lookup"><span data-stu-id="16234-141">The navigation menu module that is included in the module library lets users navigate only to categories that don't have subcategories.</span></span> <span data-ttu-id="16234-142">顧客がサブカテゴリを持つカテゴリに移動できるようにする場合は、ナビゲーション メニュー モジュールをカスタマイズする必要があります。</span><span class="sxs-lookup"><span data-stu-id="16234-142">If your customers should be able to navigate to categories that have subcategories, you must customize the navigation menu module.</span></span>

## <a name="add-custom-navigation-options"></a><span data-ttu-id="16234-143">カスタム ナビゲーション オプションを追加する</span><span class="sxs-lookup"><span data-stu-id="16234-143">Add custom navigation options</span></span>

<span data-ttu-id="16234-144">ナビゲーション メニューでは、製品カテゴリ階層に含まれていないナビゲーション オプションを追加できます。</span><span class="sxs-lookup"><span data-stu-id="16234-144">On your navigation menu, you can add navigation options that aren't part of your product category hierarchy.</span></span> <span data-ttu-id="16234-145">たとえば、製品カテゴリの一覧の最後に、サイトに対して作成した連絡先ページを指す **お問い合わせ** 項目を追加することができます。</span><span class="sxs-lookup"><span data-stu-id="16234-145">For example, at the end of the list of product categories, you can add a **Contact Us** item that points to a contact page that you've built for your site.</span></span>

<span data-ttu-id="16234-146">ナビゲーション メニューにカスタム ナビゲーション オプションを追加するには、次の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="16234-146">To add custom navigation options to your navigation menu, follow these steps.</span></span>

1. <span data-ttu-id="16234-147">カスタマイズするテンプレートまたはフラグメントで、ナビゲーション メニュー モジュールを選択します。</span><span class="sxs-lookup"><span data-stu-id="16234-147">In the template or fragment that you want to customize, select the navigation menu module.</span></span>
1. <span data-ttu-id="16234-148">プロパティ ウィンドウの **データ** タブで、**品目の追加** を選択し、新しいコンテンツ管理システム (CMS) を選択します。</span><span class="sxs-lookup"><span data-stu-id="16234-148">In the property pane, on the **Data** tab, select **Add item** to create a new content management system (CMS) navigation item.</span></span>
1. <span data-ttu-id="16234-149">リンク テキストと URL を入力します。</span><span class="sxs-lookup"><span data-stu-id="16234-149">Enter link text and a URL.</span></span>
1. <span data-ttu-id="16234-150">手順 2 と 3 を繰り返して、さらにカスタム ナビゲーション オプションを追加します。</span><span class="sxs-lookup"><span data-stu-id="16234-150">Repeat steps 2 and 3 to add more custom navigation options.</span></span>
1. <span data-ttu-id="16234-151">完了後、**保存** を選択してテンプレートまたはフラグメントを保存し、**編集の完了** を選択してチェック インします。</span><span class="sxs-lookup"><span data-stu-id="16234-151">When you've finished, select **Save** to save the template or fragment, and then select **Finish editing** to check it in.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="16234-152">追加リソース</span><span class="sxs-lookup"><span data-stu-id="16234-152">Additional resources</span></span>

[<span data-ttu-id="16234-153">テンプレートとレイアウトの概要</span><span class="sxs-lookup"><span data-stu-id="16234-153">Templates and layouts overview</span></span>](templates-layouts-overview.md)

[<span data-ttu-id="16234-154">テンプレートの使用</span><span class="sxs-lookup"><span data-stu-id="16234-154">Work with templates</span></span>](work-with-templates.md)

[<span data-ttu-id="16234-155">プリセット レイアウトの使用</span><span class="sxs-lookup"><span data-stu-id="16234-155">Work with preset layouts</span></span>](work-with-layouts.md)

[<span data-ttu-id="16234-156">フラグメントで動作</span><span class="sxs-lookup"><span data-stu-id="16234-156">Work with fragments</span></span>](work-with-fragments.md)

[<span data-ttu-id="16234-157">モジュールで動作</span><span class="sxs-lookup"><span data-stu-id="16234-157">Work with modules</span></span>](work-with-modules.md)

[<span data-ttu-id="16234-158">ページ URL の作成</span><span class="sxs-lookup"><span data-stu-id="16234-158">Create a page URL</span></span>](create-page-url.md)

[<span data-ttu-id="16234-159">公開グループで動作</span><span class="sxs-lookup"><span data-stu-id="16234-159">Work with publish groups</span></span>](publish-groups.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
