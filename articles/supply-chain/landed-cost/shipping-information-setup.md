---
title: 出荷情報設定
description: このトピックでは、陸揚原価モジュールの出荷情報を設定する方法について説明します。
author: sherry-zheng
manager: tfehr
ms.date: 12/04/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ITMGoodsDescriptionTable, ITMVesselTable, ITMExporterTable, ITMCommodityCodeTable, ITMCustomsDescription
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: chuzheng
ms.search.validFrom: 2020-12-04
ms.dyn365.ops.version: Release 10.0.17
ms.openlocfilehash: 90794a154eb2a63f33277383cda80323dafd77b0
ms.sourcegitcommit: 2b4809e60974e72df9476ffd62706b1bfc8da4a7
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/04/2021
ms.locfileid: "5500937"
---
# <a name="shipping-information-setup"></a><span data-ttu-id="1a3f0-103">出荷情報設定</span><span class="sxs-lookup"><span data-stu-id="1a3f0-103">Shipping information setup</span></span>

[!include [banner](../../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

<span data-ttu-id="1a3f0-104">このトピックでは、**陸揚原価** モジュールの出荷情報を設定する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="1a3f0-104">This topic describes how to set up shipping information for the **Landed cost** module.</span></span>

## <a name="description-of-goods"></a><a name="description-of-goods"></a><span data-ttu-id="1a3f0-105">商品の説明</span><span class="sxs-lookup"><span data-stu-id="1a3f0-105">Description of goods</span></span>

<span data-ttu-id="1a3f0-106">商品の説明は、航海、出荷コンテナー、または商品の変更方法、および商品のフォリオに役立ちます。</span><span class="sxs-lookup"><span data-stu-id="1a3f0-106">Descriptions of goods help identify a voyage, shipping container, or folio of goods, and the goods in it.</span></span> <span data-ttu-id="1a3f0-107">出荷コンテナー ヘッダーまたはフォリオ ヘッダーで商品の説明を選択できます。</span><span class="sxs-lookup"><span data-stu-id="1a3f0-107">You can select a description of goods on the shipping container header or the folio header.</span></span>

<span data-ttu-id="1a3f0-108">商品の説明を使用するには、**陸揚原価 \> 出荷情報設定 \> 商品の説明** に移動します。</span><span class="sxs-lookup"><span data-stu-id="1a3f0-108">To work with descriptions of goods, go to **Landed cost \> Shipping information setup \> Description of goods**.</span></span> <span data-ttu-id="1a3f0-109">そこで、商品の説明のレコードを表示し、開き、作成、および削除することができます。</span><span class="sxs-lookup"><span data-stu-id="1a3f0-109">There, you can view, open, create, and delete records for descriptions of goods.</span></span> <span data-ttu-id="1a3f0-110">次の表は、各レコードに使用できるフィールドを説明します。</span><span class="sxs-lookup"><span data-stu-id="1a3f0-110">The following table describes the fields that are available for each record.</span></span>

| <span data-ttu-id="1a3f0-111">フィールド</span><span class="sxs-lookup"><span data-stu-id="1a3f0-111">Field</span></span> | <span data-ttu-id="1a3f0-112">説明</span><span class="sxs-lookup"><span data-stu-id="1a3f0-112">Description</span></span> |
|---|---|
| <span data-ttu-id="1a3f0-113">商品の説明</span><span class="sxs-lookup"><span data-stu-id="1a3f0-113">Description of goods</span></span> | <span data-ttu-id="1a3f0-114">この説明を使用する商品タイプの固有 ID 名/番号を入力します。</span><span class="sxs-lookup"><span data-stu-id="1a3f0-114">Enter a unique identification name/number for the type of goods that will use this description.</span></span> |
| <span data-ttu-id="1a3f0-115">説明</span><span class="sxs-lookup"><span data-stu-id="1a3f0-115">Description</span></span> | <span data-ttu-id="1a3f0-116">このカテゴリに含まれる商品のタイプの説明を入力します。</span><span class="sxs-lookup"><span data-stu-id="1a3f0-116">Enter a description of the type of goods in this category.</span></span> |

## <a name="vessels"></a><a name="vessels"></a><span data-ttu-id="1a3f0-117">船舶</span><span class="sxs-lookup"><span data-stu-id="1a3f0-117">Vessels</span></span>

<span data-ttu-id="1a3f0-118">船は、出荷会社または代理店が使用する出荷または船舶の固有の名前です。</span><span class="sxs-lookup"><span data-stu-id="1a3f0-118">A vessel is the unique name of a ship or vessel that a shipping company or agency uses.</span></span> <span data-ttu-id="1a3f0-119">航海を作成する場合、常に船舶を選択または入力する必要があります。</span><span class="sxs-lookup"><span data-stu-id="1a3f0-119">When you create a voyage, you must always either select or enter a vessel for it.</span></span> <span data-ttu-id="1a3f0-120">同じ船舶を頻繁に使用する場合は、それぞれの船舶レコードを作成することで、新しい航海をすばやく簡単に作成できます。これにより、ユーザーは、名前や番号を手動で入力するのではなく、リストから船舶を選択できます。</span><span class="sxs-lookup"><span data-stu-id="1a3f0-120">If you often use the same vessels, then you can make it faster and easier to create a new voyage by creating a vessel record for each of them, thereby allowing users to select the vessel from a list rather then enter the name or number manually each time.</span></span>

<span data-ttu-id="1a3f0-121">船舶を使用するには、**陸揚原価 \> 出荷情報設定 \> 船舶** に移動します。</span><span class="sxs-lookup"><span data-stu-id="1a3f0-121">To work with vessels, go to **Landed cost \> Shipping information setup \> Vessels**.</span></span> <span data-ttu-id="1a3f0-122">そこで、船舶のレコードを表示し、開き、作成、および削除することができます。</span><span class="sxs-lookup"><span data-stu-id="1a3f0-122">There, you can view, open, create, and delete records for vessels.</span></span> <span data-ttu-id="1a3f0-123">次の表は、各レコードに使用できるフィールドを説明します。</span><span class="sxs-lookup"><span data-stu-id="1a3f0-123">The following table describes the fields that are available for each record.</span></span>

| <span data-ttu-id="1a3f0-124">フィールド</span><span class="sxs-lookup"><span data-stu-id="1a3f0-124">Field</span></span> | <span data-ttu-id="1a3f0-125">説明</span><span class="sxs-lookup"><span data-stu-id="1a3f0-125">Description</span></span> |
|---|---|
| <span data-ttu-id="1a3f0-126">船舶</span><span class="sxs-lookup"><span data-stu-id="1a3f0-126">Vessel</span></span> | <span data-ttu-id="1a3f0-127">航海で商品を輸送するために使用される船の固有の ID 名/番号を入力します。</span><span class="sxs-lookup"><span data-stu-id="1a3f0-127">Enter a unique identification name/number for the ship that will be used to transport goods on a voyage.</span></span> |
| <span data-ttu-id="1a3f0-128">説明</span><span class="sxs-lookup"><span data-stu-id="1a3f0-128">Description</span></span> | <span data-ttu-id="1a3f0-129">船舶の説明を入力します。</span><span class="sxs-lookup"><span data-stu-id="1a3f0-129">Enter a description of the vessel.</span></span> <span data-ttu-id="1a3f0-130">通常、この説明は、船の名前と出荷会社/エージェントを識別します。</span><span class="sxs-lookup"><span data-stu-id="1a3f0-130">Typically, this description identifies the name of the ship and the shipping company/agent.</span></span> |
| <span data-ttu-id="1a3f0-131">荷渡方法</span><span class="sxs-lookup"><span data-stu-id="1a3f0-131">Mode of delivery</span></span> | <span data-ttu-id="1a3f0-132">船舶が使用する配送モード (_航空_, _船便_, or _電車_ など) を選択します。</span><span class="sxs-lookup"><span data-stu-id="1a3f0-132">Select the mode of delivery that the vessel uses (such as _Air_, _Ocean_, or _Train_).</span></span> |

## <a name="exporters"></a><span data-ttu-id="1a3f0-133">輸出者</span><span class="sxs-lookup"><span data-stu-id="1a3f0-133">Exporters</span></span>

<span data-ttu-id="1a3f0-134">各輸出者レコードは、航海の仕入先として定義できる仕入先または輸出者を識別します。</span><span class="sxs-lookup"><span data-stu-id="1a3f0-134">Each exporter record identifies a vendor or exporter that can be defined as the vendor for a voyage.</span></span> <span data-ttu-id="1a3f0-135">輸出者は航海に関連付けられ、報告に使用できます。</span><span class="sxs-lookup"><span data-stu-id="1a3f0-135">The exporter can be associated with a voyage and used for reporting.</span></span>

<span data-ttu-id="1a3f0-136">輸出者を使用するには、**陸揚原価 \> 出荷情報設定 \> 輸出者** に移動します。</span><span class="sxs-lookup"><span data-stu-id="1a3f0-136">To work with exporters, go to **Landed cost \> Shipping information setup \> Exporters**.</span></span> <span data-ttu-id="1a3f0-137">そこで、輸出者のレコードを表示し、開き、作成、および削除することができます。</span><span class="sxs-lookup"><span data-stu-id="1a3f0-137">There, you can view, open, create, and delete records for exporters.</span></span> <span data-ttu-id="1a3f0-138">次の表は、各レコードに使用できるフィールドを説明します。</span><span class="sxs-lookup"><span data-stu-id="1a3f0-138">The following table describes the fields that are available for each record.</span></span>

| <span data-ttu-id="1a3f0-139">フィールド</span><span class="sxs-lookup"><span data-stu-id="1a3f0-139">Field</span></span> | <span data-ttu-id="1a3f0-140">説明</span><span class="sxs-lookup"><span data-stu-id="1a3f0-140">Description</span></span> |
|---|---|
| <span data-ttu-id="1a3f0-141">輸出者</span><span class="sxs-lookup"><span data-stu-id="1a3f0-141">Exporter</span></span> | <span data-ttu-id="1a3f0-142">航海で輸送される商品の輸出者の固有の ID 名/番号を入力します。</span><span class="sxs-lookup"><span data-stu-id="1a3f0-142">Enter a unique identification name/number for the exporter of goods that are transported on a voyage.</span></span> |
| <span data-ttu-id="1a3f0-143">説明</span><span class="sxs-lookup"><span data-stu-id="1a3f0-143">Description</span></span> | <span data-ttu-id="1a3f0-144">輸出者の説明を入力します。</span><span class="sxs-lookup"><span data-stu-id="1a3f0-144">Enter a description of the exporter.</span></span> <span data-ttu-id="1a3f0-145">通常、この説明は、出荷会社/エージェントのフル ネームを識別します。</span><span class="sxs-lookup"><span data-stu-id="1a3f0-145">Typically, this description identifies the full name of the shipping company/agent.</span></span> |

## <a name="commodity-codes"></a><span data-ttu-id="1a3f0-146">商品コード</span><span class="sxs-lookup"><span data-stu-id="1a3f0-146">Commodity codes</span></span>

<span data-ttu-id="1a3f0-147">商品コードは、関税 ID と航海中の商品の関税率の計算に役立ちます。</span><span class="sxs-lookup"><span data-stu-id="1a3f0-147">You use commodity codes to help with customs identification and the calculation of duty rates for goods on a voyage.</span></span> <span data-ttu-id="1a3f0-148">商品コードは、**リリース済製品** ページで選択できます。</span><span class="sxs-lookup"><span data-stu-id="1a3f0-148">You can select commodity codes on the **Released products** page.</span></span>

<span data-ttu-id="1a3f0-149">商品コードを使用するには、**陸揚原価 \> 出荷情報設定 \> 商品コード** に移動します。</span><span class="sxs-lookup"><span data-stu-id="1a3f0-149">To work with commodity codes, go to **Landed cost \> Shipping information setup \> Commodity codes**.</span></span> <span data-ttu-id="1a3f0-150">そこで、商品コードのレコードを表示し、開き、作成、および削除することができます。</span><span class="sxs-lookup"><span data-stu-id="1a3f0-150">There, you can view, open, create, and delete records for commodity codes.</span></span> <span data-ttu-id="1a3f0-151">次の表は、各レコードに使用できるフィールドを説明します。</span><span class="sxs-lookup"><span data-stu-id="1a3f0-151">The following table describes the fields that are available for each record.</span></span>

| <span data-ttu-id="1a3f0-152">フィールド</span><span class="sxs-lookup"><span data-stu-id="1a3f0-152">Field</span></span> | <span data-ttu-id="1a3f0-153">説明</span><span class="sxs-lookup"><span data-stu-id="1a3f0-153">Description</span></span> |
|---|---|
| <span data-ttu-id="1a3f0-154">商品コード</span><span class="sxs-lookup"><span data-stu-id="1a3f0-154">Commodity code</span></span> | <span data-ttu-id="1a3f0-155">このタイプの商品の固有のコードを入力します。</span><span class="sxs-lookup"><span data-stu-id="1a3f0-155">Enter a unique code for this type of commodity.</span></span> |
| <span data-ttu-id="1a3f0-156">説明</span><span class="sxs-lookup"><span data-stu-id="1a3f0-156">Description</span></span> | <span data-ttu-id="1a3f0-157">商品タイプの説明を入力します。</span><span class="sxs-lookup"><span data-stu-id="1a3f0-157">Enter a description of the commodity type.</span></span> |

## <a name="customs-description"></a><span data-ttu-id="1a3f0-158">関税説明</span><span class="sxs-lookup"><span data-stu-id="1a3f0-158">Customs description</span></span>

<span data-ttu-id="1a3f0-159">関税の説明は、関税の目的のために商品を識別するのに役立ちます。</span><span class="sxs-lookup"><span data-stu-id="1a3f0-159">Customs descriptions help identify goods for customs purposes.</span></span> <span data-ttu-id="1a3f0-160">関税の説明は、**リリースされた製品** ページまたは発注書明細行で選択できます。</span><span class="sxs-lookup"><span data-stu-id="1a3f0-160">You can select a customs description on the **Released products** page or on purchase order lines.</span></span>

<span data-ttu-id="1a3f0-161">関税の説明を使用するには、**陸揚原価 \> 出荷情報設定 \> 関税の説明** に移動します。</span><span class="sxs-lookup"><span data-stu-id="1a3f0-161">To work with customs descriptions, go to **Landed cost \> Shipping information setup \> Customs description**.</span></span> <span data-ttu-id="1a3f0-162">そこで、関税の説明のレコードを表示し、開き、作成、および削除することができます。</span><span class="sxs-lookup"><span data-stu-id="1a3f0-162">There, you can view, open, create, and delete records for custom descriptions.</span></span> <span data-ttu-id="1a3f0-163">次の表は、各レコードに使用できるフィールドを説明します。</span><span class="sxs-lookup"><span data-stu-id="1a3f0-163">The following table describes the fields that are available for each record.</span></span>

| <span data-ttu-id="1a3f0-164">フィールド</span><span class="sxs-lookup"><span data-stu-id="1a3f0-164">Field</span></span> | <span data-ttu-id="1a3f0-165">説明</span><span class="sxs-lookup"><span data-stu-id="1a3f0-165">Description</span></span> |
|---|---|
| <span data-ttu-id="1a3f0-166">関税説明</span><span class="sxs-lookup"><span data-stu-id="1a3f0-166">Customs description</span></span> | <span data-ttu-id="1a3f0-167">関税分類のタイプの固有のコードを入力します。</span><span class="sxs-lookup"><span data-stu-id="1a3f0-167">Enter a unique code for this type of customs classification.</span></span> <span data-ttu-id="1a3f0-168">多くの場合、このコードは、商品の説明と定性値のために関税当局が提供する公式の説明になります。</span><span class="sxs-lookup"><span data-stu-id="1a3f0-168">Often, this code will be the official description that is provided by a customs authority for the description and qualitative value of the goods.</span></span> |
| <span data-ttu-id="1a3f0-169">説明</span><span class="sxs-lookup"><span data-stu-id="1a3f0-169">Description</span></span> | <span data-ttu-id="1a3f0-170">関税分類の説明を入力します。</span><span class="sxs-lookup"><span data-stu-id="1a3f0-170">Enter a description of the customs classification.</span></span> |
