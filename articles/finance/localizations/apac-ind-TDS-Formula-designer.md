---
title: TDS 計算の式デザイナー
description: このトピックでは、トランザクションに関連付けられた TDS グループのそれぞれの TDS 税コードに対して定義されている式に基づいて、源泉徴収税 (TDS) がどのように計算されるかの例を示しています。
author: kailiang
ms.date: 02/12/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 15721
ms.assetid: b4b406fa-b772-44ec-8dd8-8eb818a921ef
ms.search.region: Global
ms.author: kailiang
ms.search.validFrom: 2021-02-12
ms.dyn365.ops.version: AX 10.0.17
ms.openlocfilehash: d0f644da640b56761a52baec9ff01c898e895d19
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/11/2021
ms.locfileid: "6023379"
---
# <a name="formula-designer-for-tds-calculations"></a><span data-ttu-id="27e17-103">TDS 計算の式デザイナー</span><span class="sxs-lookup"><span data-stu-id="27e17-103">Formula designer for TDS calculations</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="27e17-104">このトピックでは、TDS の税コードごとに定義された計算式に基づいて、源泉徴収税 (TDS) がどのように計算されるかの例を示しています。</span><span class="sxs-lookup"><span data-stu-id="27e17-104">This topic provides an example of how Tax Deducted at Source (TDS) is calculated based on the formula defined for each TDS tax code.</span></span> <span data-ttu-id="27e17-105">TDS 税コードは、トランザクションに関連付けられた TDS グループで定義されます。</span><span class="sxs-lookup"><span data-stu-id="27e17-105">TDS tax codes are defined in the TDS group that's attached to the transaction.</span></span> <span data-ttu-id="27e17-106">TDS 式を設計する前に、TDSに必要な基本的な設定を以下の手順で行います。</span><span class="sxs-lookup"><span data-stu-id="27e17-106">Before designing TDS formulas, complete the basic setup required for TDS as listed in the following steps.</span></span> 

- <span data-ttu-id="27e17-107">**源泉徴収税グループ** ページを使って、TDSコンポーネントグループを設定します。</span><span class="sxs-lookup"><span data-stu-id="27e17-107">Set up TDS component groups using the **Withholding tax component groups** page.</span></span> 
- <span data-ttu-id="27e17-108">**源泉徴収税コンポーネント** ページを使用して、TDS コンポーネントを設定し、TDS コンポーネントグループを TDS コンポーネントに関連付けます。</span><span class="sxs-lookup"><span data-stu-id="27e17-108">Set up TDS components and attach TDS component group to the TDS components using the **Withholding tax components** page.</span></span> 
- <span data-ttu-id="27e17-109">**源泉徴収税コード** ページを使用して、TDS の税コードの設定と、TDS コンポーネントを税コードに関連付けます。</span><span class="sxs-lookup"><span data-stu-id="27e17-109">Set up TDS tax codes and attach TDS components to the tax codes using the **Withholding tax codes** page.</span></span> 
- <span data-ttu-id="27e17-110">**源泉徴収税グループ** ページを使って、TDS税グループを設定します。</span><span class="sxs-lookup"><span data-stu-id="27e17-110">Set up TDS tax groups using the **Withholding tax groups** page.</span></span> <span data-ttu-id="27e17-111">続いて、TDS の税コードを税グループに関連付け、**式デザイナー** ページを使って式を定義します。</span><span class="sxs-lookup"><span data-stu-id="27e17-111">Then attach the TDS tax codes to the tax group, and define the formula, using the **Formula designer** page.</span></span> 

<span data-ttu-id="27e17-112">**式の例**</span><span class="sxs-lookup"><span data-stu-id="27e17-112">**Example formula**</span></span>

<span data-ttu-id="27e17-113">この例では、TDS グループ 「Rent」 は、仕入先 A に対して作成される購買請求書に関連付けることができます。請求金額は $100,000 です。</span><span class="sxs-lookup"><span data-stu-id="27e17-113">In this example, the TDS group, Rent, is attached to a purchase invoice that's created for vendor A. The invoice amount is $100,000.</span></span> <span data-ttu-id="27e17-114">請求書の TDS 計算を表示するには、次の表を参照してください。</span><span class="sxs-lookup"><span data-stu-id="27e17-114">Refer to the following table to view the TDS calculation for the invoice.</span></span>

| <span data-ttu-id="27e17-115">TDS グループ</span><span class="sxs-lookup"><span data-stu-id="27e17-115">TDS  group</span></span>                                                   | <span data-ttu-id="27e17-116">TDS グループに関連付けられた TDS 税コード</span><span class="sxs-lookup"><span data-stu-id="27e17-116">TDS tax codes attached to the TDS group</span></span> | <span data-ttu-id="27e17-117">先頭値</span><span class="sxs-lookup"><span data-stu-id="27e17-117">Value</span></span>              | <span data-ttu-id="27e17-118">課税対象 (式デザイナー)</span><span class="sxs-lookup"><span data-stu-id="27e17-118">Taxable basis  (Formula designer)</span></span> | <span data-ttu-id="27e17-119">計算式 (式デザイナー)</span><span class="sxs-lookup"><span data-stu-id="27e17-119">Calculation expression  (Formula designer)</span></span> | <span data-ttu-id="27e17-120">基準額</span><span class="sxs-lookup"><span data-stu-id="27e17-120">Base amount</span></span> | <span data-ttu-id="27e17-121">計算済 TDS の金額</span><span class="sxs-lookup"><span data-stu-id="27e17-121">Calculated TDS amount</span></span> |
| ------------------------------------------------------------ | --------------------------------------- | ------------------ | --------------------------------- | :----------------------------------------: | ----------- | --------------------- |
| <span data-ttu-id="27e17-122">賃料</span><span class="sxs-lookup"><span data-stu-id="27e17-122">Rent</span></span>                                                         | <span data-ttu-id="27e17-123">TDS (TDS コンポーネント-TDS)</span><span class="sxs-lookup"><span data-stu-id="27e17-123">TDS  (TDS component-TDS)</span></span>                | <span data-ttu-id="27e17-124">10%</span><span class="sxs-lookup"><span data-stu-id="27e17-124">10%</span></span>                | <span data-ttu-id="27e17-125">総額</span><span class="sxs-lookup"><span data-stu-id="27e17-125">Gross amount</span></span>                      |                                            | <span data-ttu-id="27e17-126">100,000</span><span class="sxs-lookup"><span data-stu-id="27e17-126">100,000</span></span>      | <span data-ttu-id="27e17-127">10,000</span><span class="sxs-lookup"><span data-stu-id="27e17-127">10,000</span></span>                 |
| <span data-ttu-id="27e17-128">割増金 (TDS コンポーネント - 割増金)</span><span class="sxs-lookup"><span data-stu-id="27e17-128">Surcharge  (TDS component-Surcharge)</span></span>                         | <span data-ttu-id="27e17-129">10%</span><span class="sxs-lookup"><span data-stu-id="27e17-129">10%</span></span>                                     | <span data-ttu-id="27e17-130">総額を除く</span><span class="sxs-lookup"><span data-stu-id="27e17-130">Excl. gross amount</span></span> | <span data-ttu-id="27e17-131">+TDS</span><span class="sxs-lookup"><span data-stu-id="27e17-131">+TDS</span></span>                              |                   <span data-ttu-id="27e17-132">10000</span><span class="sxs-lookup"><span data-stu-id="27e17-132">10000</span></span>                    | <span data-ttu-id="27e17-133">1.000</span><span class="sxs-lookup"><span data-stu-id="27e17-133">1,000</span></span>        |                       |
| <span data-ttu-id="27e17-134">PE-Cess (TDS コンポーネント - PE-Cess)</span><span class="sxs-lookup"><span data-stu-id="27e17-134">PE-Cess  (TDS component- PE-Cess)</span></span>                            | <span data-ttu-id="27e17-135">2%</span><span class="sxs-lookup"><span data-stu-id="27e17-135">2%</span></span>                                      | <span data-ttu-id="27e17-136">総額を除く</span><span class="sxs-lookup"><span data-stu-id="27e17-136">Excl. gross amount</span></span> | <span data-ttu-id="27e17-137">+TDS+割増金</span><span class="sxs-lookup"><span data-stu-id="27e17-137">+TDS+Surcharge</span></span>                    |                   <span data-ttu-id="27e17-138">11000</span><span class="sxs-lookup"><span data-stu-id="27e17-138">11000</span></span>                    | <span data-ttu-id="27e17-139">220</span><span class="sxs-lookup"><span data-stu-id="27e17-139">220</span></span>         |                       |
| <span data-ttu-id="27e17-140">SHE Cess (TDS コンポーネント - SHE Cess)</span><span class="sxs-lookup"><span data-stu-id="27e17-140">SHE Cess  (TDS component- SHE Cess)</span></span>                          | <span data-ttu-id="27e17-141">1%</span><span class="sxs-lookup"><span data-stu-id="27e17-141">1%</span></span>                                      | <span data-ttu-id="27e17-142">総額を除く</span><span class="sxs-lookup"><span data-stu-id="27e17-142">Excl. gross amount</span></span> | <span data-ttu-id="27e17-143">+TDS+割増金</span><span class="sxs-lookup"><span data-stu-id="27e17-143">+TDS+Surcharge</span></span>                    |                   <span data-ttu-id="27e17-144">11000</span><span class="sxs-lookup"><span data-stu-id="27e17-144">11000</span></span>                    | <span data-ttu-id="27e17-145">110</span><span class="sxs-lookup"><span data-stu-id="27e17-145">110</span></span>         |                       |
| <span data-ttu-id="27e17-146">**請求書に対して計算された TDS の合計**</span><span class="sxs-lookup"><span data-stu-id="27e17-146">**Total** **TDS**  **calculated** **for** **the** **invoice**</span></span> | <span data-ttu-id="27e17-147">**11,330**</span><span class="sxs-lookup"><span data-stu-id="27e17-147">**11,330**</span></span>                               |                    |                                   |                                            |             |                       |

<span data-ttu-id="27e17-148">伝票ノ入力は次のように作成されます。</span><span class="sxs-lookup"><span data-stu-id="27e17-148">The voucher entries are created as follows.</span></span>

| <span data-ttu-id="27e17-149">口座</span><span class="sxs-lookup"><span data-stu-id="27e17-149">Account</span></span>           | <span data-ttu-id="27e17-150">借方</span><span class="sxs-lookup"><span data-stu-id="27e17-150">Debit</span></span>  | <span data-ttu-id="27e17-151">与信</span><span class="sxs-lookup"><span data-stu-id="27e17-151">Credit</span></span> |
| ----------------- | ------ | ------ |
| <span data-ttu-id="27e17-152">賃料</span><span class="sxs-lookup"><span data-stu-id="27e17-152">Rent</span></span>              | <span data-ttu-id="27e17-153">100,000</span><span class="sxs-lookup"><span data-stu-id="27e17-153">100,000</span></span> |        |
| <span data-ttu-id="27e17-154">仕入先 A</span><span class="sxs-lookup"><span data-stu-id="27e17-154">Vendor A</span></span>          |        | <span data-ttu-id="27e17-155">100,000</span><span class="sxs-lookup"><span data-stu-id="27e17-155">100,000</span></span> |
| <span data-ttu-id="27e17-156">仕入先 A</span><span class="sxs-lookup"><span data-stu-id="27e17-156">Vendor A</span></span>          | <span data-ttu-id="27e17-157">11,330</span><span class="sxs-lookup"><span data-stu-id="27e17-157">11,330</span></span>  |        |
| <span data-ttu-id="27e17-158">TDS 買掛金</span><span class="sxs-lookup"><span data-stu-id="27e17-158">TDS payable</span></span>       |        | <span data-ttu-id="27e17-159">10,000</span><span class="sxs-lookup"><span data-stu-id="27e17-159">10,000</span></span>  |
| <span data-ttu-id="27e17-160">割増金買掛金</span><span class="sxs-lookup"><span data-stu-id="27e17-160">Surcharge payable</span></span> |        | <span data-ttu-id="27e17-161">1.000</span><span class="sxs-lookup"><span data-stu-id="27e17-161">1,000</span></span>   |
| <span data-ttu-id="27e17-162">PE-Cess 買掛金</span><span class="sxs-lookup"><span data-stu-id="27e17-162">PE-Cess payable</span></span>   |        | <span data-ttu-id="27e17-163">220</span><span class="sxs-lookup"><span data-stu-id="27e17-163">220</span></span>    |
| <span data-ttu-id="27e17-164">SHE Cess 買掛金</span><span class="sxs-lookup"><span data-stu-id="27e17-164">SHE Cess payable</span></span>  |        | <span data-ttu-id="27e17-165">110</span><span class="sxs-lookup"><span data-stu-id="27e17-165">110</span></span>    |
