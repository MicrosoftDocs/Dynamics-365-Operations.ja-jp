---
title: 測定単位設定の適用
description: このトピックでは測定単位設定を取り上げ、Microsoft Dynamics 365 Commerce で適用する方法について説明します。
author: anupamar-ms
ms.date: 04/23/2021
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
ms.openlocfilehash: 7d338ba207c9a101f5e224ca66555b16a457bcbc
ms.sourcegitcommit: dc4898aa32f381620c517bf89c7856e693563ace
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/17/2021
ms.locfileid: "6271404"
---
# <a name="apply-unit-of-measure-settings"></a><span data-ttu-id="1e0f7-103">測定単位設定の適用</span><span class="sxs-lookup"><span data-stu-id="1e0f7-103">Apply unit of measure settings</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="1e0f7-104">このトピックでは測定単位設定を取り上げ、Microsoft Dynamics 365 Commerce で適用する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="1e0f7-104">This topic covers unit of measure settings and describes how to apply them in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="1e0f7-105">製品は、「各」、「ペア」、「ダース」など、異なる単位で販売できます。</span><span class="sxs-lookup"><span data-stu-id="1e0f7-105">A product can be sold in different units, such as "each," "pair," and "dozen."</span></span> <span data-ttu-id="1e0f7-106">Commerce 本社では、測定単位の販売は製品を定義して、eコマース サイトに表示できます。</span><span class="sxs-lookup"><span data-stu-id="1e0f7-106">In Commerce headquarters, the sell-by unit of measure can be defined for a product and shown on an e-commerce site.</span></span> <span data-ttu-id="1e0f7-107">たとえば、小売業者が個別と数十単位の両方で製品を販売する場合、使用可能な測定単位を他の製品情報と共に表示できます。</span><span class="sxs-lookup"><span data-stu-id="1e0f7-107">For example, if a retailer sells a product both individually and in dozens, the available units of measure can be shown together with other product information.</span></span>

<span data-ttu-id="1e0f7-108">次の図の例では、**ea** (それぞれ) の測定単位の販売は、Commerce 本部の製品用に構成されています。</span><span class="sxs-lookup"><span data-stu-id="1e0f7-108">In the example in the following illustration, a sell-by unit of measure of **ea** (each) has been configured for a product in Commerce headquarters.</span></span>

![Commerce 本部の測定単位で構成されている製品の例](./media/Productunit-headquarters.PNG)

> [!NOTE]
> <span data-ttu-id="1e0f7-110">測定単位の適用および表示のサポートは、Commerce のバージョン 10.0.19 リリース以降で利用できます。</span><span class="sxs-lookup"><span data-stu-id="1e0f7-110">Support for applying and showing the unit of measure is available as of the Commerce version 10.0.19 release.</span></span>

## <a name="unit-of-measure-settings"></a><span data-ttu-id="1e0f7-111">測定単位設定</span><span class="sxs-lookup"><span data-stu-id="1e0f7-111">Unit of measure settings</span></span>

<span data-ttu-id="1e0f7-112">測定単位の表示設定は、Commerce サイト ビルダーの、**サイト設定 \> 拡張機能 \> 製品の測定単位の表示** で定義されます。</span><span class="sxs-lookup"><span data-stu-id="1e0f7-112">Unit of measure display settings are defined in Commerce site builder, at **Site settings \> Extensions \> Display unit of measure for products**.</span></span> <span data-ttu-id="1e0f7-113">サポートされている設定は 3 つあります。</span><span class="sxs-lookup"><span data-stu-id="1e0f7-113">There are three supported settings:</span></span>

- <span data-ttu-id="1e0f7-114">**表示しない** – この設定が選択されている場合、eコマース サイトに製品の測定単位は表示されません。</span><span class="sxs-lookup"><span data-stu-id="1e0f7-114">**Do not display** – When this setting is selected, the e-commerce site won't show the unit of measure for the product.</span></span> <span data-ttu-id="1e0f7-115">この動作は既定の動作です。</span><span class="sxs-lookup"><span data-stu-id="1e0f7-115">This behavior is the default behavior.</span></span>
- <span data-ttu-id="1e0f7-116">**製品の購入経験での表示**: この設定が選択されている場合、測定単位は製品の詳細、カート、チェックアウト、注文履歴、および注文の詳細ページに表示されます。</span><span class="sxs-lookup"><span data-stu-id="1e0f7-116">**Display in the product buying experience** – When this setting is selected, the unit of measure is shown on product details, cart, checkout, order history, and order details pages.</span></span>
- <span data-ttu-id="1e0f7-117">**製品閲覧および購入エクスペリエンスでの表示**: この設定が選択されている場合、測定単位は製品の購入エクスペリエンスページおよび製品ブラウジングエクスペリエンス中にも表示されます。</span><span class="sxs-lookup"><span data-stu-id="1e0f7-117">**Display in the product browsing and buying experience** – When this setting is selected, the unit of measure is shown on the product buying experience pages and also during the product browsing experience.</span></span> <span data-ttu-id="1e0f7-118">この動作の一部として、測定単位は、検索結果および製品収集モジュールに表示されます。</span><span class="sxs-lookup"><span data-stu-id="1e0f7-118">As part of this behavior, units of measure are shown in search results and product collection modules.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="1e0f7-119">測定単位の表示設定は、Commerce のバージョン 10.0.19 リリース以降で使用できます。</span><span class="sxs-lookup"><span data-stu-id="1e0f7-119">Unit of measure display settings are available as of the Commerce version 10.0.19 release.</span></span> <span data-ttu-id="1e0f7-120">古いバージョンの Commerce を更新する場合は、appsettings.json ファイルを手動で更新する必要があります。</span><span class="sxs-lookup"><span data-stu-id="1e0f7-120">If you're updating from an older version of Commerce, you must manually update the appsettings.json file.</span></span> <span data-ttu-id="1e0f7-121">手順については、[SDK およびモジュール ライブラリの更新](e-commerce-extensibility/sdk-updates.md#update-the-appsettingsjson-file) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="1e0f7-121">For instructions, see [SDK and module library updates](e-commerce-extensibility/sdk-updates.md#update-the-appsettingsjson-file).</span></span>

## <a name="modules-that-use-unit-of-measure-settings"></a><span data-ttu-id="1e0f7-122">測定単位の設定を使用するモジュール</span><span class="sxs-lookup"><span data-stu-id="1e0f7-122">Modules that use unit of measure settings</span></span>

<span data-ttu-id="1e0f7-123">測定単位の設定を使用するモジュールには、購入ボックス、欲しい物リスト、買い物カゴ、買い物カゴ アイコン、検索結果コンテナー、製品コレクション、チェックアウト、注文詳細モジュールが含まれます。</span><span class="sxs-lookup"><span data-stu-id="1e0f7-123">Modules that use the unit of measure settings include the buy box, wishlist, cart, cart icon, search results container, product collection, checkout, and order details modules.</span></span>

<span data-ttu-id="1e0f7-124">次の図の例では、製品の詳細ページ (PDP) は、製品の測定単位 (**ea**) を示しています。</span><span class="sxs-lookup"><span data-stu-id="1e0f7-124">In the example in the following illustration, a product details page (PDP) shows the unit of measure (**ea**) for a product.</span></span>

![測定単位を示す PDP の例](./media/Productunit-PDP.png)

<span data-ttu-id="1e0f7-126">次の図の例では、製品収集モジュールは、製品の測定単位 (**ea**) を示しています。</span><span class="sxs-lookup"><span data-stu-id="1e0f7-126">In the example in the following illustration, a product collection module shows the unit of measure (**ea**) for a product.</span></span>

![測定単位を示す製品収集モジュールの例](./media/Productunit-productcollection.png)

## <a name="additional-resources"></a><span data-ttu-id="1e0f7-128">追加リソース</span><span class="sxs-lookup"><span data-stu-id="1e0f7-128">Additional resources</span></span>

[<span data-ttu-id="1e0f7-129">モジュール ライブラリの概要</span><span class="sxs-lookup"><span data-stu-id="1e0f7-129">Module library overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="1e0f7-130">カート モジュール</span><span class="sxs-lookup"><span data-stu-id="1e0f7-130">Cart module</span></span>](add-cart-module.md)

[<span data-ttu-id="1e0f7-131">購入ボックス モジュール</span><span class="sxs-lookup"><span data-stu-id="1e0f7-131">Buy box module</span></span>](add-buy-box.md)

[<span data-ttu-id="1e0f7-132">アカウント管理ページとモジュール</span><span class="sxs-lookup"><span data-stu-id="1e0f7-132">Account management pages and modules</span></span>](account-management.md)

[<span data-ttu-id="1e0f7-133">SDK およびモジュール ライブラリの更新</span><span class="sxs-lookup"><span data-stu-id="1e0f7-133">SDK and module library updates</span></span>](e-commerce-extensibility/sdk-updates.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
