---
title: フッター モジュール
description: このトピックでは、フッター モジュール、および Dynamics 365 Commerce での作成方法について説明します。
author: anupamar
manager: annbe
ms.date: 10/31/2019
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
ms.openlocfilehash: f8e0290b5af9d0c1fc9ad0279b0d7f81c9feb2fc
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/01/2020
ms.locfileid: "3001160"
---
# <a name="footer-module"></a><span data-ttu-id="097a3-103">フッター モジュール</span><span class="sxs-lookup"><span data-stu-id="097a3-103">Footer module</span></span>  


[!include [banner](includes/banner.md)]

<span data-ttu-id="097a3-104">このトピックでは、フッター モジュール、および Microsoft Dynamics 365 Commerce での作成方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="097a3-104">This topic covers footer modules and describes how to create them in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="097a3-105">概要</span><span class="sxs-lookup"><span data-stu-id="097a3-105">Overview</span></span>

<span data-ttu-id="097a3-106">フッター モジュールは、ページ フッターに表示されるモジュールをホストするために使用される特別なコンテナーです。</span><span class="sxs-lookup"><span data-stu-id="097a3-106">The footer module is a special container that is used to host the modules that appear in the page footer.</span></span> <span data-ttu-id="097a3-107">たとえば、**お問い合わせ**や**店舗ポリシー** ページなど、サイト内のさまざまなページへのリンクを含めることができます。</span><span class="sxs-lookup"><span data-stu-id="097a3-107">For example, it can include links to various pages across the site, such as **Contact Us** and **Store Policies** pages.</span></span>

## <a name="footer-module-properties"></a><span data-ttu-id="097a3-108">フッター モジュール プロパティ</span><span class="sxs-lookup"><span data-stu-id="097a3-108">Footer module properties</span></span> 

<span data-ttu-id="097a3-109">ほとんどのコンテナーと同様に、フッター モジュールでは見出しと幅のプロパティがサポートされています。</span><span class="sxs-lookup"><span data-stu-id="097a3-109">Like most containers, a footer module support properties for the heading and the width.</span></span> <span data-ttu-id="097a3-110">また、複数のフッター カテゴリ モジュールの追加もサポートされています。</span><span class="sxs-lookup"><span data-stu-id="097a3-110">It also supports the addition of multiple footer category modules.</span></span> <span data-ttu-id="097a3-111">追加された各フッター カテゴリ モジュールは、フッター モジュールの列としてレンダリングされます。</span><span class="sxs-lookup"><span data-stu-id="097a3-111">Each footer category module that is added is rendered as a column in the footer module.</span></span>

## <a name="modules-available-in-a-footer-module"></a><span data-ttu-id="097a3-112">フッター モジュールで使用できるモジュール</span><span class="sxs-lookup"><span data-stu-id="097a3-112">Modules available in a footer module</span></span>

<span data-ttu-id="097a3-113">**フッター項目** – フッター項目モジュールには、見出し、画像、およびリンクを含めることができます。</span><span class="sxs-lookup"><span data-stu-id="097a3-113">**Footer items** – A footer items module can contain a heading, an image, and a link.</span></span> <span data-ttu-id="097a3-114">見出しは、単独で、または画像およびリンクと組み合わせて使用できます。</span><span class="sxs-lookup"><span data-stu-id="097a3-114">The heading can be used either alone or in combination with an image and a link.</span></span> <span data-ttu-id="097a3-115">フッター内のすべてのリンクは、テキストのみ (「お問い合わせ」や「プライバシー」リンクなど)、またはテキストと画像 (ソーシャル メディア リンクなど) の両方を持つようにコンフィギュレーションできます。</span><span class="sxs-lookup"><span data-stu-id="097a3-115">Every link in the footer can be configured so that it has just text (for example, "Contact Us" and "Privacy" links), or so that it has both text and an image (for example, social media links).</span></span>

<span data-ttu-id="097a3-116">**トップに戻る** – トップに戻るモジュールは、ページの上部にすばやく移動するためのリンクを提供します。</span><span class="sxs-lookup"><span data-stu-id="097a3-116">**Back to top** – A back to top module provides a link for quick navigation to the top of the page.</span></span> <span data-ttu-id="097a3-117">行先が必要です。</span><span class="sxs-lookup"><span data-stu-id="097a3-117">A destination is required.</span></span> <span data-ttu-id="097a3-118">既定値は # で、ユーザーをページの先頭に移動します。</span><span class="sxs-lookup"><span data-stu-id="097a3-118">The default destination value is #, which takes the user to the top of the page.</span></span>

## <a name="author-a-footer-module"></a><span data-ttu-id="097a3-119">フッター モジュールの作成</span><span class="sxs-lookup"><span data-stu-id="097a3-119">Author a footer module</span></span>

1. <span data-ttu-id="097a3-120">ナビゲーション ウィンドウで、**フラグメント**を選択し、**新しいページ フラグメント**を選択します。</span><span class="sxs-lookup"><span data-stu-id="097a3-120">In the navigation pane, select **Fragments**, and then select **New Page Fragment**.</span></span>
1. <span data-ttu-id="097a3-121">**新しいページ フラグメント** ダイアログ ボックスで、フッター モジュールを選択し、ページ フラグメントの名前を入力して、**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="097a3-121">In the **New Page Fragment** dialog box, select the footer module, enter a name for the page fragment, and then select **OK**.</span></span>
1. <span data-ttu-id="097a3-122">左側のアウトライン ツリーで、フッター モジュールの省略記号ボタン (**...**) を選択してから、**モジュールの追加**を選択します。</span><span class="sxs-lookup"><span data-stu-id="097a3-122">In the outline tree on the left, select the ellipsis button (**...**) for the footer module, and then select **Add Module**.</span></span>
1. <span data-ttu-id="097a3-123">**モジュールの追加**ダイアログ ボックスで、フッター カテゴリ モジュールを選択してから、**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="097a3-123">In the **Add Module** dialog box, select the footer category module, and then select **OK**.</span></span>
1. <span data-ttu-id="097a3-124">アウトライン ツリーで、フッター カテゴリ モジュールの省略記号ボタン (...) を選択してから、**モジュールの追加**を選択します。</span><span class="sxs-lookup"><span data-stu-id="097a3-124">In the outline tree, select the ellipsis button for the footer category module, and then select **Add Module**.</span></span>
1. <span data-ttu-id="097a3-125">**モジュールの追加**ダイアログ ボックスで、フッター項目モジュールを選択してから、**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="097a3-125">In the **Add Module** dialog box, select the footer item module, and then select **OK**.</span></span>
1. <span data-ttu-id="097a3-126">アウトライン ツリーで、フッター項目モジュールを選択します。</span><span class="sxs-lookup"><span data-stu-id="097a3-126">In the outline tree, select the footer item module.</span></span> <span data-ttu-id="097a3-127">その後、右側のプロパティ ウィンドウで、必要に応じて見出し、リンクとリンク テキスト、および画像をコンフィギュレーションします。</span><span class="sxs-lookup"><span data-stu-id="097a3-127">Then, in the properties pane on the right, configure the heading, link and link text, and image as you require.</span></span>
1. <span data-ttu-id="097a3-128">フッター項目をさらに追加する場合は、ステップ 5 から 7 を繰り返します。</span><span class="sxs-lookup"><span data-stu-id="097a3-128">To add more footer items, repeat steps 5 through 7.</span></span>
1. <span data-ttu-id="097a3-129">フッターに「トップに戻る」リンクを追加するには、フッター カテゴリ モジュールの省略記号ボタン (...) を選択してから、**モジュールの追加**を選択します。</span><span class="sxs-lookup"><span data-stu-id="097a3-129">To add a "back to top" link to your footer, select the ellipsis button for the footer category module, and then select **Add Module**.</span></span>
1. <span data-ttu-id="097a3-130">**モジュールの追加**ダイアログ ボックスで、トップに戻るモジュールを選択してから、**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="097a3-130">In the **Add Module** dialog box, select the back to top module, and then select **OK**.</span></span>
1. <span data-ttu-id="097a3-131">アウトライン ツリーで、トップに戻るモジュールを選択します。</span><span class="sxs-lookup"><span data-stu-id="097a3-131">In the outline tree, select the back to top module.</span></span> <span data-ttu-id="097a3-132">その後、右側のプロパティ ウィンドウで、トップに戻るモジュールを必要に応じてコンフィギュレーションします。</span><span class="sxs-lookup"><span data-stu-id="097a3-132">Then, in the properties pane on the right, configure the back to top module as you require.</span></span>
1. <span data-ttu-id="097a3-133">ページ フラグメントを保存し、チェック イン後に公開します。</span><span class="sxs-lookup"><span data-stu-id="097a3-133">Save the page fragment, check it in, and publish it.</span></span>

<span data-ttu-id="097a3-134">サイトに対して作成されたすべてのページ テンプレートで、次の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="097a3-134">On every page template that has been created for the site, follow these steps.</span></span>

1. <span data-ttu-id="097a3-135">既定ページの**メイン** スロットのフッターモジュールに、作成したフッター フラグメントを追加します。</span><span class="sxs-lookup"><span data-stu-id="097a3-135">In the **Main** slot of the default page, in the footer module, add the footer fragment that you created.</span></span>
1. <span data-ttu-id="097a3-136">テンプレートを保存し、チェック イン後に発行します。</span><span class="sxs-lookup"><span data-stu-id="097a3-136">Save the template, check it in, and publish it.</span></span>

<span data-ttu-id="097a3-137">ページ テンプレートにページ フラグメントを追加することにより、フッターがすべてのページにレンダリングされることを保証できます。</span><span class="sxs-lookup"><span data-stu-id="097a3-137">By adding the page fragment to page templates, you help guarantee that the footer is rendered on every page.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="097a3-138">追加リソース</span><span class="sxs-lookup"><span data-stu-id="097a3-138">Additional resources</span></span>

[<span data-ttu-id="097a3-139">スタート キットの概要</span><span class="sxs-lookup"><span data-stu-id="097a3-139">Starter kit overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="097a3-140">コンテナー モジュール</span><span class="sxs-lookup"><span data-stu-id="097a3-140">Container module</span></span>](add-container-module.md)

[<span data-ttu-id="097a3-141">購入ボックス モジュール</span><span class="sxs-lookup"><span data-stu-id="097a3-141">Buy box module</span></span>](add-buy-box.md)

[<span data-ttu-id="097a3-142">カート モジュール</span><span class="sxs-lookup"><span data-stu-id="097a3-142">Cart module</span></span>](add-cart-module.md)

[<span data-ttu-id="097a3-143">チェックアウト モジュール</span><span class="sxs-lookup"><span data-stu-id="097a3-143">Checkout module</span></span>](add-checkout-module.md)

[<span data-ttu-id="097a3-144">注文確認モジュール</span><span class="sxs-lookup"><span data-stu-id="097a3-144">Order confirmation module</span></span>](order-confirmation-module.md)

[<span data-ttu-id="097a3-145">ヘッダー モジュール</span><span class="sxs-lookup"><span data-stu-id="097a3-145">Header module</span></span>](author-header-module.md)

[<span data-ttu-id="097a3-146">フッター モジュール</span><span class="sxs-lookup"><span data-stu-id="097a3-146">Footer module</span></span>](author-footer-module.md)
