---
title: フッター モジュール
description: このトピックでは、フッター モジュール、および Dynamics 365 Commerce での作成方法について説明します。
author: anupamar-ms
ms.date: 09/15/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: d6e7b0ad4fe0723575a0ec55a9b02d110568db58
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/31/2021
ms.locfileid: "5797236"
---
# <a name="footer-module"></a><span data-ttu-id="02854-103">フッター モジュール</span><span class="sxs-lookup"><span data-stu-id="02854-103">Footer module</span></span>  

[!include [banner](includes/banner.md)]

<span data-ttu-id="02854-104">このトピックでは、フッター モジュール、および Microsoft Dynamics 365 Commerce での作成方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="02854-104">This topic covers footer modules and describes how to create them in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="02854-105">フッター モジュールは、ページ フッターに表示されるモジュールをホストするために使用される特別なコンテナーです。</span><span class="sxs-lookup"><span data-stu-id="02854-105">The footer module is a special container that is used to host the modules that appear in the page footer.</span></span> <span data-ttu-id="02854-106">たとえば、**お問い合わせ** や **店舗ポリシー** ページなど、サイト内のさまざまなページへのリンクを含めることができます。</span><span class="sxs-lookup"><span data-stu-id="02854-106">For example, it can include links to various pages across the site, such as **Contact Us** and **Store Policies** pages.</span></span>

<span data-ttu-id="02854-107">以下の図は、サイトのページにおけるフッター モジュールの例を示しています。</span><span class="sxs-lookup"><span data-stu-id="02854-107">The following image shows an example of a footer module on a site page.</span></span>

![フッター モジュールの例](./media/ecommerce-footer.PNG)

## <a name="footer-module-properties"></a><span data-ttu-id="02854-109">フッター モジュール プロパティ</span><span class="sxs-lookup"><span data-stu-id="02854-109">Footer module properties</span></span> 

<span data-ttu-id="02854-110">ほとんどのコンテナーと同様に、フッター モジュールでは見出しと幅のプロパティに対応しています。</span><span class="sxs-lookup"><span data-stu-id="02854-110">Like most containers, a footer module supports properties for the heading and the width.</span></span> <span data-ttu-id="02854-111">また、複数のフッター カテゴリ モジュールの追加もサポートされています。</span><span class="sxs-lookup"><span data-stu-id="02854-111">It also supports the addition of multiple footer category modules.</span></span> <span data-ttu-id="02854-112">追加された各フッター カテゴリ モジュールは、フッター モジュールの列としてレンダリングされます。</span><span class="sxs-lookup"><span data-stu-id="02854-112">Each footer category module that is added is rendered as a column in the footer module.</span></span>

## <a name="modules-available-in-a-footer-module"></a><span data-ttu-id="02854-113">フッター モジュールで使用できるモジュール</span><span class="sxs-lookup"><span data-stu-id="02854-113">Modules available in a footer module</span></span>

<span data-ttu-id="02854-114">**フッター項目** – フッター項目モジュールには、見出し、画像、およびリンクを含めることができます。</span><span class="sxs-lookup"><span data-stu-id="02854-114">**Footer items** – A footer items module can contain a heading, an image, and a link.</span></span> <span data-ttu-id="02854-115">見出しは、単独で、または画像およびリンクと組み合わせて使用できます。</span><span class="sxs-lookup"><span data-stu-id="02854-115">The heading can be used either alone or in combination with an image and a link.</span></span> <span data-ttu-id="02854-116">フッター内のすべてのリンクは、テキストのみ (「お問い合わせ」や「プライバシー」リンクなど)、またはテキストと画像 (ソーシャル メディア リンクなど) の両方を持つようにコンフィギュレーションできます。</span><span class="sxs-lookup"><span data-stu-id="02854-116">Every link in the footer can be configured so that it has just text (for example, "Contact Us" and "Privacy" links), or so that it has both text and an image (for example, social media links).</span></span>

<span data-ttu-id="02854-117">**トップに戻る** – トップに戻るモジュールは、ページの上部にすばやく移動するためのリンクを提供します。</span><span class="sxs-lookup"><span data-stu-id="02854-117">**Back to top** – A back to top module provides a link for quick navigation to the top of the page.</span></span> <span data-ttu-id="02854-118">行先が必要です。</span><span class="sxs-lookup"><span data-stu-id="02854-118">A destination is required.</span></span> <span data-ttu-id="02854-119">既定値は \# です。この値はユーザーをページの先頭に移動します。</span><span class="sxs-lookup"><span data-stu-id="02854-119">The default destination value is \#, which takes the user to the top of the page.</span></span>

## <a name="create-a-footer-module"></a><span data-ttu-id="02854-120">フッター モジュールの作成</span><span class="sxs-lookup"><span data-stu-id="02854-120">Create a footer module</span></span>

1. <span data-ttu-id="02854-121">**フラグメント** に移動し、続いて **新規** を選択して新規フラグメントを作成します。</span><span class="sxs-lookup"><span data-stu-id="02854-121">Go to **Fragments**, and select **New** to create a new fragment.</span></span>
1. <span data-ttu-id="02854-122">**新規フラグメント** ダイアログ ボックスで、**コンテナー** モジュールを選択し、フラグメントの名前を入力して、**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="02854-122">In the **New fragment** dialog box, select the **Container** module, enter a name for the fragment, and then select **OK**.</span></span>
1. <span data-ttu-id="02854-123">**既定のコンテナー** スロットの省略ボタン (**...**) を選択し、**モジュールの追加** を選択します。</span><span class="sxs-lookup"><span data-stu-id="02854-123">In the **Default container** slot, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="02854-124">**モジュールの追加** ダイアログ ボックスで、**フッター カテゴリ モジュール** を選択し、続いて **OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="02854-124">In the **Add Module** dialog box, select the **Footer category** module, and then select **OK**.</span></span>
1. <span data-ttu-id="02854-125">**フッター カテゴリ** スロットで、省略ボタン (**...**) を選択し、**モジュールの追加** を選択します。</span><span class="sxs-lookup"><span data-stu-id="02854-125">In the **Footer category** slot, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="02854-126">**モジュールの追加** ダイアログ ボックスで、**フッター項目** モジュールを選択してから、 **OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="02854-126">In the **Add Module** dialog box, select the **Footer item** module, and then select **OK**.</span></span>
1. <span data-ttu-id="02854-127">右側のプロパティ ウィンドウで **フッター項目** スロットを選択し、必要に応じて見出し、リンクとリンク テキスト、画像を構成します。</span><span class="sxs-lookup"><span data-stu-id="02854-127">Select the **Footer item** slot, and then, in the properties pane on the right, configure the heading, link and link text, and image as needed.</span></span>
1. <span data-ttu-id="02854-128">フッター項目を追加する場合は、手順 5 から 7 を繰り返します。</span><span class="sxs-lookup"><span data-stu-id="02854-128">To add more footer items, repeat steps 5 through 7 for each.</span></span>
1. <span data-ttu-id="02854-129">フッターに「トップに戻る」リンクを追加するには、**フッター カテゴリ** スロットの省略記号ボタン (**...**) を選択し、続いて **モジュールの追加** を選択します。</span><span class="sxs-lookup"><span data-stu-id="02854-129">To add a "back to top" link to your footer, select the ellipsis (**...**) in the **Footer category** slot, and then select **Add Module**.</span></span>
1. <span data-ttu-id="02854-130">**モジュールの追加** ダイアログ ボックスで、**トップに戻る** モジュールを選択し、続いて **OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="02854-130">In the **Add Module** dialog box, select the **Back to top** module, and then select **OK**.</span></span>
1. <span data-ttu-id="02854-131">右側のプロパティ ウィンドウで **トップに戻る** スロットを選択し、必要に応じてテキストやその他のモジュール プロパティを構成します。</span><span class="sxs-lookup"><span data-stu-id="02854-131">Select the **Back to top** slot, and then, in the properties pane on the right, configure the text and other module properties as needed.</span></span>
1. <span data-ttu-id="02854-132">**編集の完了** を選択してフラグメントにチェックインし、 **発行** を選択して公開します。</span><span class="sxs-lookup"><span data-stu-id="02854-132">Select **Finish editing** to check in the fragment, and then select **Publish** to publish it.</span></span>

<span data-ttu-id="02854-133">すべてのページにヘッダーが表示されることを保証するには、サイトに対して作成されたすべてのページ テンプレートで次の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="02854-133">To help guarantee that a header appears on every page, follow these steps on every page template that is created for the site.</span></span>

1. <span data-ttu-id="02854-134">**既定ページ** モジュールの **フッター** スロットに、作成したフッター フラグメントを追加します。</span><span class="sxs-lookup"><span data-stu-id="02854-134">In the **Footer** slot of the **Default page** module, add the footer fragment that you created.</span></span>
1. <span data-ttu-id="02854-135">**編集の完了**  を選択してテンプレートをチェックインし、 **発行** を選択して公開します。</span><span class="sxs-lookup"><span data-stu-id="02854-135">Select **Finish editing** to check in the template, and then select **Publish** to publish it.</span></span>

<span data-ttu-id="02854-136">ページ テンプレートにフラグメントを追加することにより、フッターがすべてのページにレンダリングされるようになります。</span><span class="sxs-lookup"><span data-stu-id="02854-136">By adding the fragment to page templates, you help guarantee that the footer is rendered on every page.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="02854-137">追加リソース</span><span class="sxs-lookup"><span data-stu-id="02854-137">Additional resources</span></span>

[<span data-ttu-id="02854-138">モジュール ライブラリの概要</span><span class="sxs-lookup"><span data-stu-id="02854-138">Module library overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="02854-139">コンテナー モジュール</span><span class="sxs-lookup"><span data-stu-id="02854-139">Container module</span></span>](add-container-module.md)

[<span data-ttu-id="02854-140">購入ボックス モジュール</span><span class="sxs-lookup"><span data-stu-id="02854-140">Buy box module</span></span>](add-buy-box.md)

[<span data-ttu-id="02854-141">カート モジュール</span><span class="sxs-lookup"><span data-stu-id="02854-141">Cart module</span></span>](add-cart-module.md)

[<span data-ttu-id="02854-142">チェックアウト モジュール</span><span class="sxs-lookup"><span data-stu-id="02854-142">Checkout module</span></span>](add-checkout-module.md)

[<span data-ttu-id="02854-143">注文確認モジュール</span><span class="sxs-lookup"><span data-stu-id="02854-143">Order confirmation module</span></span>](order-confirmation-module.md)

[<span data-ttu-id="02854-144">ヘッダー モジュール</span><span class="sxs-lookup"><span data-stu-id="02854-144">Header module</span></span>](author-header-module.md)

[<span data-ttu-id="02854-145">フッター モジュール</span><span class="sxs-lookup"><span data-stu-id="02854-145">Footer module</span></span>](author-footer-module.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]