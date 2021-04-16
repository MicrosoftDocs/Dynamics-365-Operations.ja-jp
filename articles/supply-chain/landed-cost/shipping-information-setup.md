---
title: 出荷情報設定
description: このトピックでは、陸揚原価モジュールの出荷情報を設定する方法について説明します。
author: sherry-zheng
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
ms.openlocfilehash: 74ac7e0eac545369eef1a48f0085c820a4728e75
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/01/2021
ms.locfileid: "5833692"
---
# <a name="shipping-information-setup"></a><span data-ttu-id="3cc64-103">出荷情報設定</span><span class="sxs-lookup"><span data-stu-id="3cc64-103">Shipping information setup</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="3cc64-104">このトピックでは、**陸揚原価** モジュールの出荷情報を設定する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="3cc64-104">This topic describes how to set up shipping information for the **Landed cost** module.</span></span>

## <a name="description-of-goods"></a><a name="description-of-goods"></a><span data-ttu-id="3cc64-105">商品の説明</span><span class="sxs-lookup"><span data-stu-id="3cc64-105">Description of goods</span></span>

<span data-ttu-id="3cc64-106">商品の説明は、航海、出荷コンテナー、または商品の変更方法、および商品のフォリオに役立ちます。</span><span class="sxs-lookup"><span data-stu-id="3cc64-106">Descriptions of goods help identify a voyage, shipping container, or folio of goods, and the goods in it.</span></span> <span data-ttu-id="3cc64-107">出荷コンテナー ヘッダーまたはフォリオ ヘッダーで商品の説明を選択できます。</span><span class="sxs-lookup"><span data-stu-id="3cc64-107">You can select a description of goods on the shipping container header or the folio header.</span></span>

<span data-ttu-id="3cc64-108">商品の説明を使用するには、**陸揚原価 \> 出荷情報設定 \> 商品の説明** に移動します。</span><span class="sxs-lookup"><span data-stu-id="3cc64-108">To work with descriptions of goods, go to **Landed cost \> Shipping information setup \> Description of goods**.</span></span> <span data-ttu-id="3cc64-109">そこで、商品の説明のレコードを表示し、開き、作成、および削除することができます。</span><span class="sxs-lookup"><span data-stu-id="3cc64-109">There, you can view, open, create, and delete records for descriptions of goods.</span></span> <span data-ttu-id="3cc64-110">次の表は、各レコードに使用できるフィールドを説明します。</span><span class="sxs-lookup"><span data-stu-id="3cc64-110">The following table describes the fields that are available for each record.</span></span>

| <span data-ttu-id="3cc64-111">フィールド</span><span class="sxs-lookup"><span data-stu-id="3cc64-111">Field</span></span> | <span data-ttu-id="3cc64-112">説明</span><span class="sxs-lookup"><span data-stu-id="3cc64-112">Description</span></span> |
|---|---|
| <span data-ttu-id="3cc64-113">商品の説明</span><span class="sxs-lookup"><span data-stu-id="3cc64-113">Description of goods</span></span> | <span data-ttu-id="3cc64-114">この説明を使用する商品タイプの固有 ID 名/番号を入力します。</span><span class="sxs-lookup"><span data-stu-id="3cc64-114">Enter a unique identification name/number for the type of goods that will use this description.</span></span> |
| <span data-ttu-id="3cc64-115">説明</span><span class="sxs-lookup"><span data-stu-id="3cc64-115">Description</span></span> | <span data-ttu-id="3cc64-116">このカテゴリに含まれる商品のタイプの説明を入力します。</span><span class="sxs-lookup"><span data-stu-id="3cc64-116">Enter a description of the type of goods in this category.</span></span> |

## <a name="vessels"></a><a name="vessels"></a><span data-ttu-id="3cc64-117">船舶</span><span class="sxs-lookup"><span data-stu-id="3cc64-117">Vessels</span></span>

<span data-ttu-id="3cc64-118">船は、出荷会社または代理店が使用する出荷または船舶の固有の名前です。</span><span class="sxs-lookup"><span data-stu-id="3cc64-118">A vessel is the unique name of a ship or vessel that a shipping company or agency uses.</span></span> <span data-ttu-id="3cc64-119">航海を作成する場合、常に船舶を選択または入力する必要があります。</span><span class="sxs-lookup"><span data-stu-id="3cc64-119">When you create a voyage, you must always either select or enter a vessel for it.</span></span> <span data-ttu-id="3cc64-120">同じ船舶を頻繁に使用する場合は、それぞれの船舶レコードを作成することで、新しい航海をすばやく簡単に作成できます。これにより、ユーザーは、名前や番号を手動で入力するのではなく、リストから船舶を選択できます。</span><span class="sxs-lookup"><span data-stu-id="3cc64-120">If you often use the same vessels, then you can make it faster and easier to create a new voyage by creating a vessel record for each of them, thereby allowing users to select the vessel from a list rather then enter the name or number manually each time.</span></span>

<span data-ttu-id="3cc64-121">船舶を使用するには、**陸揚原価 \> 出荷情報設定 \> 船舶** に移動します。</span><span class="sxs-lookup"><span data-stu-id="3cc64-121">To work with vessels, go to **Landed cost \> Shipping information setup \> Vessels**.</span></span> <span data-ttu-id="3cc64-122">そこで、船舶のレコードを表示し、開き、作成、および削除することができます。</span><span class="sxs-lookup"><span data-stu-id="3cc64-122">There, you can view, open, create, and delete records for vessels.</span></span> <span data-ttu-id="3cc64-123">次の表は、各レコードに使用できるフィールドを説明します。</span><span class="sxs-lookup"><span data-stu-id="3cc64-123">The following table describes the fields that are available for each record.</span></span>

| <span data-ttu-id="3cc64-124">フィールド</span><span class="sxs-lookup"><span data-stu-id="3cc64-124">Field</span></span> | <span data-ttu-id="3cc64-125">説明</span><span class="sxs-lookup"><span data-stu-id="3cc64-125">Description</span></span> |
|---|---|
| <span data-ttu-id="3cc64-126">船舶</span><span class="sxs-lookup"><span data-stu-id="3cc64-126">Vessel</span></span> | <span data-ttu-id="3cc64-127">航海で商品を輸送するために使用される船の固有の ID 名/番号を入力します。</span><span class="sxs-lookup"><span data-stu-id="3cc64-127">Enter a unique identification name/number for the ship that will be used to transport goods on a voyage.</span></span> |
| <span data-ttu-id="3cc64-128">説明</span><span class="sxs-lookup"><span data-stu-id="3cc64-128">Description</span></span> | <span data-ttu-id="3cc64-129">船舶の説明を入力します。</span><span class="sxs-lookup"><span data-stu-id="3cc64-129">Enter a description of the vessel.</span></span> <span data-ttu-id="3cc64-130">通常、この説明は、船の名前と出荷会社/エージェントを識別します。</span><span class="sxs-lookup"><span data-stu-id="3cc64-130">Typically, this description identifies the name of the ship and the shipping company/agent.</span></span> |
| <span data-ttu-id="3cc64-131">荷渡方法</span><span class="sxs-lookup"><span data-stu-id="3cc64-131">Mode of delivery</span></span> | <span data-ttu-id="3cc64-132">船舶が使用する配送モード (_航空_, _船便_, or _電車_ など) を選択します。</span><span class="sxs-lookup"><span data-stu-id="3cc64-132">Select the mode of delivery that the vessel uses (such as _Air_, _Ocean_, or _Train_).</span></span> |

## <a name="exporters"></a><span data-ttu-id="3cc64-133">輸出者</span><span class="sxs-lookup"><span data-stu-id="3cc64-133">Exporters</span></span>

<span data-ttu-id="3cc64-134">各輸出者レコードは、航海の仕入先として定義できる仕入先または輸出者を識別します。</span><span class="sxs-lookup"><span data-stu-id="3cc64-134">Each exporter record identifies a vendor or exporter that can be defined as the vendor for a voyage.</span></span> <span data-ttu-id="3cc64-135">輸出者は航海に関連付けられ、報告に使用できます。</span><span class="sxs-lookup"><span data-stu-id="3cc64-135">The exporter can be associated with a voyage and used for reporting.</span></span>

<span data-ttu-id="3cc64-136">輸出者を使用するには、**陸揚原価 \> 出荷情報設定 \> 輸出者** に移動します。</span><span class="sxs-lookup"><span data-stu-id="3cc64-136">To work with exporters, go to **Landed cost \> Shipping information setup \> Exporters**.</span></span> <span data-ttu-id="3cc64-137">そこで、輸出者のレコードを表示し、開き、作成、および削除することができます。</span><span class="sxs-lookup"><span data-stu-id="3cc64-137">There, you can view, open, create, and delete records for exporters.</span></span> <span data-ttu-id="3cc64-138">次の表は、各レコードに使用できるフィールドを説明します。</span><span class="sxs-lookup"><span data-stu-id="3cc64-138">The following table describes the fields that are available for each record.</span></span>

| <span data-ttu-id="3cc64-139">フィールド</span><span class="sxs-lookup"><span data-stu-id="3cc64-139">Field</span></span> | <span data-ttu-id="3cc64-140">説明</span><span class="sxs-lookup"><span data-stu-id="3cc64-140">Description</span></span> |
|---|---|
| <span data-ttu-id="3cc64-141">輸出者</span><span class="sxs-lookup"><span data-stu-id="3cc64-141">Exporter</span></span> | <span data-ttu-id="3cc64-142">航海で輸送される商品の輸出者の固有の ID 名/番号を入力します。</span><span class="sxs-lookup"><span data-stu-id="3cc64-142">Enter a unique identification name/number for the exporter of goods that are transported on a voyage.</span></span> |
| <span data-ttu-id="3cc64-143">説明</span><span class="sxs-lookup"><span data-stu-id="3cc64-143">Description</span></span> | <span data-ttu-id="3cc64-144">輸出者の説明を入力します。</span><span class="sxs-lookup"><span data-stu-id="3cc64-144">Enter a description of the exporter.</span></span> <span data-ttu-id="3cc64-145">通常、この説明は、出荷会社/エージェントのフル ネームを識別します。</span><span class="sxs-lookup"><span data-stu-id="3cc64-145">Typically, this description identifies the full name of the shipping company/agent.</span></span> |

## <a name="commodity-codes"></a><span data-ttu-id="3cc64-146">商品コード</span><span class="sxs-lookup"><span data-stu-id="3cc64-146">Commodity codes</span></span>

<span data-ttu-id="3cc64-147">商品コードは、関税 ID と航海中の商品の関税率の計算に役立ちます。</span><span class="sxs-lookup"><span data-stu-id="3cc64-147">You use commodity codes to help with customs identification and the calculation of duty rates for goods on a voyage.</span></span> <span data-ttu-id="3cc64-148">商品コードは、**リリース済製品** ページで選択できます。</span><span class="sxs-lookup"><span data-stu-id="3cc64-148">You can select commodity codes on the **Released products** page.</span></span>

<span data-ttu-id="3cc64-149">商品コードを使用するには、**陸揚原価 \> 出荷情報設定 \> 商品コード** に移動します。</span><span class="sxs-lookup"><span data-stu-id="3cc64-149">To work with commodity codes, go to **Landed cost \> Shipping information setup \> Commodity codes**.</span></span> <span data-ttu-id="3cc64-150">そこで、商品コードのレコードを表示し、開き、作成、および削除することができます。</span><span class="sxs-lookup"><span data-stu-id="3cc64-150">There, you can view, open, create, and delete records for commodity codes.</span></span> <span data-ttu-id="3cc64-151">次の表は、各レコードに使用できるフィールドを説明します。</span><span class="sxs-lookup"><span data-stu-id="3cc64-151">The following table describes the fields that are available for each record.</span></span>

| <span data-ttu-id="3cc64-152">フィールド</span><span class="sxs-lookup"><span data-stu-id="3cc64-152">Field</span></span> | <span data-ttu-id="3cc64-153">説明</span><span class="sxs-lookup"><span data-stu-id="3cc64-153">Description</span></span> |
|---|---|
| <span data-ttu-id="3cc64-154">商品コード</span><span class="sxs-lookup"><span data-stu-id="3cc64-154">Commodity code</span></span> | <span data-ttu-id="3cc64-155">このタイプの商品の固有のコードを入力します。</span><span class="sxs-lookup"><span data-stu-id="3cc64-155">Enter a unique code for this type of commodity.</span></span> |
| <span data-ttu-id="3cc64-156">説明</span><span class="sxs-lookup"><span data-stu-id="3cc64-156">Description</span></span> | <span data-ttu-id="3cc64-157">商品タイプの説明を入力します。</span><span class="sxs-lookup"><span data-stu-id="3cc64-157">Enter a description of the commodity type.</span></span> |

## <a name="customs-description"></a><span data-ttu-id="3cc64-158">関税説明</span><span class="sxs-lookup"><span data-stu-id="3cc64-158">Customs description</span></span>

<span data-ttu-id="3cc64-159">関税の説明は、関税の目的のために商品を識別するのに役立ちます。</span><span class="sxs-lookup"><span data-stu-id="3cc64-159">Customs descriptions help identify goods for customs purposes.</span></span> <span data-ttu-id="3cc64-160">関税の説明は、**リリースされた製品** ページまたは発注書明細行で選択できます。</span><span class="sxs-lookup"><span data-stu-id="3cc64-160">You can select a customs description on the **Released products** page or on purchase order lines.</span></span>

<span data-ttu-id="3cc64-161">関税の説明を使用するには、**陸揚原価 \> 出荷情報設定 \> 関税の説明** に移動します。</span><span class="sxs-lookup"><span data-stu-id="3cc64-161">To work with customs descriptions, go to **Landed cost \> Shipping information setup \> Customs description**.</span></span> <span data-ttu-id="3cc64-162">そこで、関税の説明のレコードを表示し、開き、作成、および削除することができます。</span><span class="sxs-lookup"><span data-stu-id="3cc64-162">There, you can view, open, create, and delete records for custom descriptions.</span></span> <span data-ttu-id="3cc64-163">次の表は、各レコードに使用できるフィールドを説明します。</span><span class="sxs-lookup"><span data-stu-id="3cc64-163">The following table describes the fields that are available for each record.</span></span>

| <span data-ttu-id="3cc64-164">フィールド</span><span class="sxs-lookup"><span data-stu-id="3cc64-164">Field</span></span> | <span data-ttu-id="3cc64-165">説明</span><span class="sxs-lookup"><span data-stu-id="3cc64-165">Description</span></span> |
|---|---|
| <span data-ttu-id="3cc64-166">関税説明</span><span class="sxs-lookup"><span data-stu-id="3cc64-166">Customs description</span></span> | <span data-ttu-id="3cc64-167">関税分類のタイプの固有のコードを入力します。</span><span class="sxs-lookup"><span data-stu-id="3cc64-167">Enter a unique code for this type of customs classification.</span></span> <span data-ttu-id="3cc64-168">多くの場合、このコードは、商品の説明と定性値のために関税当局が提供する公式の説明になります。</span><span class="sxs-lookup"><span data-stu-id="3cc64-168">Often, this code will be the official description that is provided by a customs authority for the description and qualitative value of the goods.</span></span> |
| <span data-ttu-id="3cc64-169">説明</span><span class="sxs-lookup"><span data-stu-id="3cc64-169">Description</span></span> | <span data-ttu-id="3cc64-170">関税分類の説明を入力します。</span><span class="sxs-lookup"><span data-stu-id="3cc64-170">Enter a description of the customs classification.</span></span> |
