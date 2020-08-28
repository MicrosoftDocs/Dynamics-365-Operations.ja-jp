---
title: フッター モジュール
description: このトピックでは、フッター モジュール、および Dynamics 365 Commerce での作成方法について説明します。
author: anupamar
manager: annbe
ms.date: 05/28/2020
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
ms.author: anupamar-ms
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: e81617979a945274500c9f4ceaa8078d8dfd79e8
ms.sourcegitcommit: 81f162f2d50557d7afe292c8d326618ba0bc3259
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/11/2020
ms.locfileid: "3686721"
---
# <a name="footer-module"></a><span data-ttu-id="276f4-103">フッター モジュール</span><span class="sxs-lookup"><span data-stu-id="276f4-103">Footer module</span></span>  

[!include [banner](includes/banner.md)]

<span data-ttu-id="276f4-104">このトピックでは、フッター モジュール、および Microsoft Dynamics 365 Commerce での作成方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="276f4-104">This topic covers footer modules and describes how to create them in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="276f4-105">概要</span><span class="sxs-lookup"><span data-stu-id="276f4-105">Overview</span></span>

<span data-ttu-id="276f4-106">フッター モジュールは、ページ フッターに表示されるモジュールをホストするために使用される特別なコンテナーです。</span><span class="sxs-lookup"><span data-stu-id="276f4-106">The footer module is a special container that is used to host the modules that appear in the page footer.</span></span> <span data-ttu-id="276f4-107">たとえば、**お問い合わせ**や**店舗ポリシー** ページなど、サイト内のさまざまなページへのリンクを含めることができます。</span><span class="sxs-lookup"><span data-stu-id="276f4-107">For example, it can include links to various pages across the site, such as **Contact Us** and **Store Policies** pages.</span></span>

<span data-ttu-id="276f4-108">以下の図は、サイトのページにおけるフッター モジュールの例を示しています。</span><span class="sxs-lookup"><span data-stu-id="276f4-108">The following image shows an example of a footer module on a site page.</span></span>

![フッター モジュールの例](./media/ecommerce-footer.PNG)

## <a name="footer-module-properties"></a><span data-ttu-id="276f4-110">フッター モジュール プロパティ</span><span class="sxs-lookup"><span data-stu-id="276f4-110">Footer module properties</span></span> 

<span data-ttu-id="276f4-111">ほとんどのコンテナーと同様に、フッター モジュールでは見出しと幅のプロパティに対応しています。</span><span class="sxs-lookup"><span data-stu-id="276f4-111">Like most containers, a footer module supports properties for the heading and the width.</span></span> <span data-ttu-id="276f4-112">また、複数のフッター カテゴリ モジュールの追加もサポートされています。</span><span class="sxs-lookup"><span data-stu-id="276f4-112">It also supports the addition of multiple footer category modules.</span></span> <span data-ttu-id="276f4-113">追加された各フッター カテゴリ モジュールは、フッター モジュールの列としてレンダリングされます。</span><span class="sxs-lookup"><span data-stu-id="276f4-113">Each footer category module that is added is rendered as a column in the footer module.</span></span>

## <a name="modules-available-in-a-footer-module"></a><span data-ttu-id="276f4-114">フッター モジュールで使用できるモジュール</span><span class="sxs-lookup"><span data-stu-id="276f4-114">Modules available in a footer module</span></span>

<span data-ttu-id="276f4-115">**フッター項目** – フッター項目モジュールには、見出し、画像、およびリンクを含めることができます。</span><span class="sxs-lookup"><span data-stu-id="276f4-115">**Footer items** – A footer items module can contain a heading, an image, and a link.</span></span> <span data-ttu-id="276f4-116">見出しは、単独で、または画像およびリンクと組み合わせて使用できます。</span><span class="sxs-lookup"><span data-stu-id="276f4-116">The heading can be used either alone or in combination with an image and a link.</span></span> <span data-ttu-id="276f4-117">フッター内のすべてのリンクは、テキストのみ (「お問い合わせ」や「プライバシー」リンクなど)、またはテキストと画像 (ソーシャル メディア リンクなど) の両方を持つようにコンフィギュレーションできます。</span><span class="sxs-lookup"><span data-stu-id="276f4-117">Every link in the footer can be configured so that it has just text (for example, "Contact Us" and "Privacy" links), or so that it has both text and an image (for example, social media links).</span></span>

<span data-ttu-id="276f4-118">**トップに戻る** – トップに戻るモジュールは、ページの上部にすばやく移動するためのリンクを提供します。</span><span class="sxs-lookup"><span data-stu-id="276f4-118">**Back to top** – A back to top module provides a link for quick navigation to the top of the page.</span></span> <span data-ttu-id="276f4-119">行先が必要です。</span><span class="sxs-lookup"><span data-stu-id="276f4-119">A destination is required.</span></span> <span data-ttu-id="276f4-120">既定値は \# です。この値はユーザーをページの先頭に移動します。</span><span class="sxs-lookup"><span data-stu-id="276f4-120">The default destination value is \#, which takes the user to the top of the page.</span></span>

## <a name="create-a-footer-module"></a><span data-ttu-id="276f4-121">フッター モジュールの作成</span><span class="sxs-lookup"><span data-stu-id="276f4-121">Create a footer module</span></span>

1. <span data-ttu-id="276f4-122">**フラグメント** に移動し、続いて **新規** を選択して新規フラグメントを作成します。</span><span class="sxs-lookup"><span data-stu-id="276f4-122">Go to **Fragments**, and select **New** to create a new fragment.</span></span>
1. <span data-ttu-id="276f4-123">**新規ページ フラグメント** ダイアログ ボックスで、**コンテナー** モジュールを選択し、ページ フラグメントの名前を入力して、**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="276f4-123">In the **New page fragment** dialog box, select the **Container** module, enter a name for the page fragment, and then select **OK**.</span></span>
1. <span data-ttu-id="276f4-124">**既定のコンテナー** スロットの省略ボタン (**...**) を選択し、**モジュールの追加** を選択します。</span><span class="sxs-lookup"><span data-stu-id="276f4-124">In the **Default container** slot, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="276f4-125">**モジュールの追加** ダイアログ ボックスで、**フッター カテゴリ モジュール** を選択し、続いて**OK**を選択します。</span><span class="sxs-lookup"><span data-stu-id="276f4-125">In the **Add Module** dialog box, select the **Footer category** module, and then select **OK**.</span></span>
1. <span data-ttu-id="276f4-126">**フッター カテゴリ**スロットで、省略ボタン (**...**) を選択し、**モジュールの追加** を選択します。</span><span class="sxs-lookup"><span data-stu-id="276f4-126">In the **Footer category** slot, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="276f4-127">**モジュールの追加** ダイアログ ボックスで、**フッター項目** モジュールを選択してから、 **OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="276f4-127">In the **Add Module** dialog box, select the **Footer item** module, and then select **OK**.</span></span>
1. <span data-ttu-id="276f4-128">右側のプロパティ ウィンドウで**フッター項目**スロットを選択し、必要に応じて見出し、リンクとリンク テキスト、画像を構成します。</span><span class="sxs-lookup"><span data-stu-id="276f4-128">Select the **Footer item** slot, and then, in the properties pane on the right, configure the heading, link and link text, and image as needed.</span></span>
1. <span data-ttu-id="276f4-129">フッター項目を追加する場合は、手順 5 から 7 を繰り返します。</span><span class="sxs-lookup"><span data-stu-id="276f4-129">To add more footer items, repeat steps 5 through 7 for each.</span></span>
1. <span data-ttu-id="276f4-130">フッターに「トップに戻る」リンクを追加するには、**フッター カテゴリ**スロットの省略記号ボタン (**...**) を選択し、続いて**モジュールの追加**を選択します。</span><span class="sxs-lookup"><span data-stu-id="276f4-130">To add a "back to top" link to your footer, select the ellipsis (**...**) in the **Footer category** slot, and then select **Add Module**.</span></span>
1. <span data-ttu-id="276f4-131">**モジュールの追加** ダイアログ ボックスで、**トップに戻る** モジュールを選択し、続いて **OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="276f4-131">In the **Add Module** dialog box, select the **Back to top** module, and then select **OK**.</span></span>
1. <span data-ttu-id="276f4-132">右側のプロパティ ウィンドウで**トップに戻る**スロットを選択し、必要に応じてテキストやその他のモジュール プロパティを構成します。</span><span class="sxs-lookup"><span data-stu-id="276f4-132">Select the **Back to top** slot, and then, in the properties pane on the right, configure the text and other module properties as needed.</span></span>
1. <span data-ttu-id="276f4-133">**編集の完了** を選択してフラグメントにチェックインし、 **発行** を選択して公開します。</span><span class="sxs-lookup"><span data-stu-id="276f4-133">Select **Finish editing** to check in the fragment, and then select **Publish** to publish it.</span></span>

<span data-ttu-id="276f4-134">すべてのページにヘッダーが表示されることを保証するには、サイトに対して作成されたすべてのページ テンプレートで次の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="276f4-134">To help guarantee that a header appears on every page, follow these steps on every page template that is created for the site.</span></span>

1. <span data-ttu-id="276f4-135">**既定ページ** モジュールの **フッター** スロットに、作成したフッター フラグメントを追加します。</span><span class="sxs-lookup"><span data-stu-id="276f4-135">In the **Footer** slot of the **Default page** module, add the footer fragment that you created.</span></span>
1. <span data-ttu-id="276f4-136">**編集の完了**  を選択してテンプレートをチェックインし、 **発行** を選択して公開します。</span><span class="sxs-lookup"><span data-stu-id="276f4-136">Select **Finish editing** to check in the template, and then select **Publish** to publish it.</span></span>

<span data-ttu-id="276f4-137">ページ テンプレートにページ フラグメントを追加することにより、フッターがすべてのページにレンダリングされることを保証できます。</span><span class="sxs-lookup"><span data-stu-id="276f4-137">By adding the page fragment to page templates, you help guarantee that the footer is rendered on every page.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="276f4-138">追加リソース</span><span class="sxs-lookup"><span data-stu-id="276f4-138">Additional resources</span></span>

[<span data-ttu-id="276f4-139">スタート キットの概要</span><span class="sxs-lookup"><span data-stu-id="276f4-139">Starter kit overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="276f4-140">コンテナー モジュール</span><span class="sxs-lookup"><span data-stu-id="276f4-140">Container module</span></span>](add-container-module.md)

[<span data-ttu-id="276f4-141">購入ボックス モジュール</span><span class="sxs-lookup"><span data-stu-id="276f4-141">Buy box module</span></span>](add-buy-box.md)

[<span data-ttu-id="276f4-142">カート モジュール</span><span class="sxs-lookup"><span data-stu-id="276f4-142">Cart module</span></span>](add-cart-module.md)

[<span data-ttu-id="276f4-143">チェックアウト モジュール</span><span class="sxs-lookup"><span data-stu-id="276f4-143">Checkout module</span></span>](add-checkout-module.md)

[<span data-ttu-id="276f4-144">注文確認モジュール</span><span class="sxs-lookup"><span data-stu-id="276f4-144">Order confirmation module</span></span>](order-confirmation-module.md)

[<span data-ttu-id="276f4-145">ヘッダー モジュール</span><span class="sxs-lookup"><span data-stu-id="276f4-145">Header module</span></span>](author-header-module.md)

[<span data-ttu-id="276f4-146">フッター モジュール</span><span class="sxs-lookup"><span data-stu-id="276f4-146">Footer module</span></span>](author-footer-module.md)
