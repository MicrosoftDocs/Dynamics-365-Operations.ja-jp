---
title: サイト ナビゲーションのカスタマイズ
description: このトピックでは、カスタマイズされたオンライン ナビゲーション階層を作成して、Microsoft Dynamics 365 Commerce サイトで参照するため製品を整理する方法について説明します。
author: bicyclingfool
manager: annbe
ms.date: 09/15/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: StuHarg
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: c2b6a7a3b35873e80be391c627d0397fd6398a99
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/13/2020
ms.locfileid: "4413738"
---
# <a name="customize-site-navigation"></a><span data-ttu-id="8fe51-103">サイト ナビゲーションのカスタマイズ</span><span class="sxs-lookup"><span data-stu-id="8fe51-103">Customize site navigation</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="8fe51-104">このトピックでは、カスタマイズされたオンライン ナビゲーション階層を作成して、Microsoft Dynamics 365 Commerce サイトで参照するため製品を整理する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="8fe51-104">This topic describes how to create a customized online navigation hierarchy to organize your products for browsing on your Microsoft Dynamics 365 Commerce site.</span></span>

## <a name="overview"></a><span data-ttu-id="8fe51-105">概要</span><span class="sxs-lookup"><span data-stu-id="8fe51-105">Overview</span></span>

<span data-ttu-id="8fe51-106">オンライン店舗では、製品カテゴリを移動することで、顧客は製品を検索して参照することができます。</span><span class="sxs-lookup"><span data-stu-id="8fe51-106">Online storefronts typically let customers discover and browse products by navigating through product categories.</span></span> <span data-ttu-id="8fe51-107">この機能は通常、ページ上部にあるタブまたは左側にあるナビゲーション バーによって提供されます。</span><span class="sxs-lookup"><span data-stu-id="8fe51-107">This capability is usually provided by tabs at the top of the page or by a navigation bar on the left.</span></span> <span data-ttu-id="8fe51-108">Dynamics 365 Commerce では、カテゴリ ナビゲーションの階層構造と、さまざまなカテゴリに含まれる製品を作成および管理できます。</span><span class="sxs-lookup"><span data-stu-id="8fe51-108">In Dynamics 365 Commerce, you can create and manage the hierarchal structure of your category navigation and the products that are included in the various categories.</span></span>

## <a name="create-a-channel-navigation-hierarchy"></a><span data-ttu-id="8fe51-109">チャネル ナビゲーション階層の作成</span><span class="sxs-lookup"><span data-stu-id="8fe51-109">Create a channel navigation hierarchy</span></span>

<span data-ttu-id="8fe51-110">チャネルのナビゲーション階層を作成するには、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="8fe51-110">To create a channel navigation hierarchy, follow these steps.</span></span>

1. <span data-ttu-id="8fe51-111">**Retail と Commerce \> 製品とカテゴリ \> カテゴリと製品の管理** に移動します。</span><span class="sxs-lookup"><span data-stu-id="8fe51-111">Go to **Retail and Commerce \> Products and categories \> Category and product management**.</span></span>
1. <span data-ttu-id="8fe51-112">**カテゴリ階層** を選択し、**新規** を選択します。</span><span class="sxs-lookup"><span data-stu-id="8fe51-112">Select **Category hierarchies**, and then select **New**.</span></span>
1. <span data-ttu-id="8fe51-113">階層に名前を付けます。</span><span class="sxs-lookup"><span data-stu-id="8fe51-113">Name the hierarchy.</span></span>

    > [!NOTE]
    > <span data-ttu-id="8fe51-114">作成する最上位カテゴリは、ルート カテゴリ ノードです。</span><span class="sxs-lookup"><span data-stu-id="8fe51-114">The topmost category that you create is the root category node.</span></span> <span data-ttu-id="8fe51-115">サイトには表示されません。</span><span class="sxs-lookup"><span data-stu-id="8fe51-115">It won't be shown on your site.</span></span> <span data-ttu-id="8fe51-116">サイトに単一のトップ レベル ノードが表示されているカテゴリ階層を作成するには、カテゴリを作成し、ルート カテゴリの子として名前を付けます。</span><span class="sxs-lookup"><span data-stu-id="8fe51-116">To create a category hierarchy where a single top-level node is shown on your site, create and name the category as a child of the root category.</span></span>

1. <span data-ttu-id="8fe51-117">**新しいカテゴリ ノード** を選択し、カテゴリに名前を付けます。</span><span class="sxs-lookup"><span data-stu-id="8fe51-117">Select **New category node**, and name the category.</span></span>
1. <span data-ttu-id="8fe51-118">必要に応じて、兄弟カテゴリと子カテゴリの作成を続行します。</span><span class="sxs-lookup"><span data-stu-id="8fe51-118">Continue to create sibling and child categories as you require.</span></span>

<span data-ttu-id="8fe51-119">トップレベルのカテゴリの下に作成した各カテゴリに製品を割り当てることができるようになりました。</span><span class="sxs-lookup"><span data-stu-id="8fe51-119">You can now assign products to each category that you created under the top-level category.</span></span>

## <a name="customize-the-order-of-categories"></a><span data-ttu-id="8fe51-120">カテゴリの順序のカスタマイズ</span><span class="sxs-lookup"><span data-stu-id="8fe51-120">Customize the order of categories</span></span>

<span data-ttu-id="8fe51-121">既定では、定義したカテゴリはサイトでアルファベット順に表示されます。</span><span class="sxs-lookup"><span data-stu-id="8fe51-121">By default, the categories that you define will appear in alphabetical order on your site.</span></span> <span data-ttu-id="8fe51-122">ただし、カテゴリの表示順序をカスタマイズすることもできます。</span><span class="sxs-lookup"><span data-stu-id="8fe51-122">However, you can also customize the display order of categories.</span></span>

## <a name="assign-a-category-hierarchy-type"></a><span data-ttu-id="8fe51-123">カテゴリ階層タイプの割り当て</span><span class="sxs-lookup"><span data-stu-id="8fe51-123">Assign a category hierarchy type</span></span>

1. <span data-ttu-id="8fe51-124">**Retail と Commerce \> 製品とカテゴリ \> カテゴリと製品の管理** に移動します。</span><span class="sxs-lookup"><span data-stu-id="8fe51-124">Go to **Retail and Commerce \> Products and categories \> Category and product management**.</span></span>
1. <span data-ttu-id="8fe51-125">**カテゴリ階層** を選択します。</span><span class="sxs-lookup"><span data-stu-id="8fe51-125">Select **Category hierarchies**.</span></span>
1. <span data-ttu-id="8fe51-126">アクション ペイン、**カテゴリ階層** タブの、**設定** グループで、**階層タイプの関連付け** を選択します。</span><span class="sxs-lookup"><span data-stu-id="8fe51-126">On the Action Pane, on the **Category hierarchy** tab, in the **Set up** group, select **Associate hierarchy type**.</span></span>
1. <span data-ttu-id="8fe51-127">**新規** を選択します。</span><span class="sxs-lookup"><span data-stu-id="8fe51-127">Select **New**.</span></span>
1. <span data-ttu-id="8fe51-128">**カテゴリ階層タイプ** フィールドで、**チャネル ナビゲーション階層** を選択します。</span><span class="sxs-lookup"><span data-stu-id="8fe51-128">In the **Category hierarchy type** field, select **Channel navigation hierarchy**.</span></span>
1. <span data-ttu-id="8fe51-129">**カテゴリ階層** フィールドで、以前に作成したチャンネル ナビゲーション階層を選択します。</span><span class="sxs-lookup"><span data-stu-id="8fe51-129">In the **Category hierarchy** field, select the channel navigation hierarchy that you created earlier.</span></span>

## <a name="publish-new-or-updated-navigation-hierarchies"></a><span data-ttu-id="8fe51-130">新規または更新されたナビゲーション階層の公開</span><span class="sxs-lookup"><span data-stu-id="8fe51-130">Publish new or updated navigation hierarchies</span></span>

<span data-ttu-id="8fe51-131">オンライン店舗でナビゲーション階層を使用できるようにするには、次の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="8fe51-131">To make your navigation hierarchy available to your online storefront, follow these steps.</span></span>

1. <span data-ttu-id="8fe51-132">**Retail と Commerce \> チャネル設定 \> チャネル カテゴリと製品属性** に移動します。</span><span class="sxs-lookup"><span data-stu-id="8fe51-132">Go to **Retail and Commerce \> Channel setup \> Channel categories and product attributes**.</span></span>
1. <span data-ttu-id="8fe51-133">左側のツリーで、オンライン ストアを選択します。</span><span class="sxs-lookup"><span data-stu-id="8fe51-133">In the tree on the left, select your online store.</span></span>
1. <span data-ttu-id="8fe51-134">**チャネル更新の公開** を選択します。</span><span class="sxs-lookup"><span data-stu-id="8fe51-134">Select **Publish channel updates**.</span></span>
1. <span data-ttu-id="8fe51-135">**Retail とコマース \> Retail とコマース IT \> 配送スケジュール** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="8fe51-135">Go to **Retail and Commerce \> Retail and Commerce IT \> Distribution schedule**.</span></span>
1. <span data-ttu-id="8fe51-136">一覧から **ジョブ 1040** を見つけ、選択します。</span><span class="sxs-lookup"><span data-stu-id="8fe51-136">In the list, find and select **Job 1040**.</span></span>
1. <span data-ttu-id="8fe51-137">**今すぐ実行** を選択します。</span><span class="sxs-lookup"><span data-stu-id="8fe51-137">Select **Run now**.</span></span>
1. <span data-ttu-id="8fe51-138">ジョブ 1070 および 1150 についても、手順 5 と 6 を繰り返します。</span><span class="sxs-lookup"><span data-stu-id="8fe51-138">Repeat steps 5 and 6 for jobs 1070 and 1150.</span></span>

## <a name="show-categories-on-your-site"></a><span data-ttu-id="8fe51-139">サイトにカテゴリを表示する</span><span class="sxs-lookup"><span data-stu-id="8fe51-139">Show categories on your site</span></span>

<span data-ttu-id="8fe51-140">オンライン店舗でカテゴリ階層を表示するには、テンプレートまたはフラグメント内の適切な場所にナビゲーション メニュー モジュールを追加する必要があります。</span><span class="sxs-lookup"><span data-stu-id="8fe51-140">To show your category hierarchy on your online storefront, you must add the navigation menu module in the appropriate location in a template or fragment.</span></span> <span data-ttu-id="8fe51-141">サイトがバインドされているチャンネルにナビゲーション階層を公開している場合は、ナビゲーション メニュー モジュールにナビゲーション階層が表示されます。</span><span class="sxs-lookup"><span data-stu-id="8fe51-141">The navigation menu module will then show your navigation hierarchy, provided that you've published your navigation hierarchy to the channel that your site is bound to.</span></span>

> [!NOTE]
> <span data-ttu-id="8fe51-142">モジュール ライブラリに含まれているナビゲーション メニュー モジュールを使用することで、ユーザーはサブカテゴリを持たないカテゴリにのみ移動できます。</span><span class="sxs-lookup"><span data-stu-id="8fe51-142">The navigation menu module that is included in the module library lets users navigate only to categories that don't have subcategories.</span></span> <span data-ttu-id="8fe51-143">顧客がサブカテゴリを持つカテゴリに移動できるようにする場合は、ナビゲーション メニュー モジュールをカスタマイズする必要があります。</span><span class="sxs-lookup"><span data-stu-id="8fe51-143">If your customers should be able to navigate to categories that have subcategories, you must customize the navigation menu module.</span></span>

## <a name="add-custom-navigation-options"></a><span data-ttu-id="8fe51-144">カスタム ナビゲーション オプションを追加する</span><span class="sxs-lookup"><span data-stu-id="8fe51-144">Add custom navigation options</span></span>

<span data-ttu-id="8fe51-145">ナビゲーション メニューでは、製品カテゴリ階層に含まれていないナビゲーション オプションを追加できます。</span><span class="sxs-lookup"><span data-stu-id="8fe51-145">On your navigation menu, you can add navigation options that aren't part of your product category hierarchy.</span></span> <span data-ttu-id="8fe51-146">たとえば、製品カテゴリの一覧の最後に、サイトに対して作成した連絡先ページを指す **お問い合わせ** 項目を追加することができます。</span><span class="sxs-lookup"><span data-stu-id="8fe51-146">For example, at the end of the list of product categories, you can add a **Contact Us** item that points to a contact page that you've built for your site.</span></span>

<span data-ttu-id="8fe51-147">ナビゲーション メニューにカスタム ナビゲーション オプションを追加するには、次の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="8fe51-147">To add custom navigation options to your navigation menu, follow these steps.</span></span>

1. <span data-ttu-id="8fe51-148">カスタマイズするテンプレートまたはフラグメントで、ナビゲーション メニュー モジュールを選択します。</span><span class="sxs-lookup"><span data-stu-id="8fe51-148">In the template or fragment that you want to customize, select the navigation menu module.</span></span>
1. <span data-ttu-id="8fe51-149">プロパティ ウィンドウの **データ** タブで、**品目の追加** を選択し、新しいコンテンツ管理システム (CMS) を選択します。</span><span class="sxs-lookup"><span data-stu-id="8fe51-149">In the property pane, on the **Data** tab, select **Add item** to create a new content management system (CMS) navigation item.</span></span>
1. <span data-ttu-id="8fe51-150">リンク テキストと URL を入力します。</span><span class="sxs-lookup"><span data-stu-id="8fe51-150">Enter link text and a URL.</span></span>
1. <span data-ttu-id="8fe51-151">手順 2 と 3 を繰り返して、さらにカスタム ナビゲーション オプションを追加します。</span><span class="sxs-lookup"><span data-stu-id="8fe51-151">Repeat steps 2 and 3 to add more custom navigation options.</span></span>
1. <span data-ttu-id="8fe51-152">完了後、**保存** を選択してテンプレートまたはフラグメントを保存し、**編集の完了** を選択してチェック インします。</span><span class="sxs-lookup"><span data-stu-id="8fe51-152">When you've finished, select **Save** to save the template or fragment, and then select **Finish editing** to check it in.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="8fe51-153">追加リソース</span><span class="sxs-lookup"><span data-stu-id="8fe51-153">Additional resources</span></span>

[<span data-ttu-id="8fe51-154">テンプレートとレイアウトの概要</span><span class="sxs-lookup"><span data-stu-id="8fe51-154">Templates and layouts overview</span></span>](templates-layouts-overview.md)

[<span data-ttu-id="8fe51-155">テンプレートの使用</span><span class="sxs-lookup"><span data-stu-id="8fe51-155">Work with templates</span></span>](work-with-templates.md)

[<span data-ttu-id="8fe51-156">プリセット レイアウトの使用</span><span class="sxs-lookup"><span data-stu-id="8fe51-156">Work with preset layouts</span></span>](work-with-layouts.md)

[<span data-ttu-id="8fe51-157">フラグメントで動作</span><span class="sxs-lookup"><span data-stu-id="8fe51-157">Work with fragments</span></span>](work-with-fragments.md)

[<span data-ttu-id="8fe51-158">モジュールで動作</span><span class="sxs-lookup"><span data-stu-id="8fe51-158">Work with modules</span></span>](work-with-modules.md)

[<span data-ttu-id="8fe51-159">ページ URL の作成</span><span class="sxs-lookup"><span data-stu-id="8fe51-159">Create a page URL</span></span>](create-page-url.md)

[<span data-ttu-id="8fe51-160">公開グループで動作</span><span class="sxs-lookup"><span data-stu-id="8fe51-160">Work with publish groups</span></span>](publish-groups.md)
