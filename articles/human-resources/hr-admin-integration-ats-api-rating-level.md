---
title: 評価レベル
description: このトピックでは、Dynamics 365 Human Resources の評価レベルのエンティティについて説明します。
author: jaredha
manager: tfehr
ms.date: 02/05/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-human-resources
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: jaredha
ms.search.validFrom: 2021-02-05
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 1ad37c7a5b961bb03d37775168dac91e606d2b08
ms.sourcegitcommit: 33b5c8bc4f9461e290513aa22de1ec1fba3b0742
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/05/2021
ms.locfileid: "5125260"
---
# <a name="rating-level"></a><span data-ttu-id="e8350-103">評価レベル</span><span class="sxs-lookup"><span data-stu-id="e8350-103">Rating level</span></span>

<span data-ttu-id="e8350-104">このトピックでは、Dynamics 365 Human Resources の評価レベルのエンティティについて説明します。</span><span class="sxs-lookup"><span data-stu-id="e8350-104">This topic describes the Rating level entity for Dynamics 365 Human Resources.</span></span>

<span data-ttu-id="e8350-105">物理名 : mshr_hcmratinglevelentity</span><span class="sxs-lookup"><span data-stu-id="e8350-105">Physical name: mshr_hcmratinglevelentity</span></span>

## <a name="description"></a><span data-ttu-id="e8350-106">説明</span><span class="sxs-lookup"><span data-stu-id="e8350-106">Description</span></span>

<span data-ttu-id="e8350-107">このエンティティは、スキルの評価レベルを提供します。</span><span class="sxs-lookup"><span data-stu-id="e8350-107">This entity provides the available rating levels for skills.</span></span> <span data-ttu-id="e8350-108">評価レベルは、すべての法人に適用されます。</span><span class="sxs-lookup"><span data-stu-id="e8350-108">Rating levels apply across all legal entities.</span></span>

## <a name="json-representation"></a><span data-ttu-id="e8350-109">JSON 表記</span><span class="sxs-lookup"><span data-stu-id="e8350-109">JSON representation</span></span>

```json
{
    "mshr_description": "String",
    "mshr_factor": Int,
    "mshr_note": "String",
    "mshr_ratinglevelid": "String",
    "mshr_ratingmodelid": "String",
    "mshr_primaryfield": "String",
    "_mshr_fk_ratingmodelentity_id_value": "Guid",
    "mshr_hcmratinglevelentityid": "Guid"
}
```

## <a name="properties"></a><span data-ttu-id="e8350-110">プロパティ</span><span class="sxs-lookup"><span data-stu-id="e8350-110">Properties</span></span>

| <span data-ttu-id="e8350-111">プロパティ</span><span class="sxs-lookup"><span data-stu-id="e8350-111">Property</span></span><br><span data-ttu-id="e8350-112">**現物名**</span><span class="sxs-lookup"><span data-stu-id="e8350-112">**Physical name**</span></span><br><span data-ttu-id="e8350-113">**_種類_**</span><span class="sxs-lookup"><span data-stu-id="e8350-113">**_Type_**</span></span> | <span data-ttu-id="e8350-114">使用</span><span class="sxs-lookup"><span data-stu-id="e8350-114">Use</span></span> | <span data-ttu-id="e8350-115">説明</span><span class="sxs-lookup"><span data-stu-id="e8350-115">Description</span></span> |
| --- | --- | --- |
| <span data-ttu-id="e8350-116">**評価レベル エンティティ ID**</span><span class="sxs-lookup"><span data-stu-id="e8350-116">**Rating Level Entity ID**</span></span><br><span data-ttu-id="e8350-117">mshr_hcmratinglevelentityid</span><span class="sxs-lookup"><span data-stu-id="e8350-117">mshr_hcmratinglevelentityid</span></span><br><span data-ttu-id="e8350-118">*GUID*</span><span class="sxs-lookup"><span data-stu-id="e8350-118">*GUID*</span></span> | <span data-ttu-id="e8350-119">読み取り専用</span><span class="sxs-lookup"><span data-stu-id="e8350-119">Read-only</span></span><br><span data-ttu-id="e8350-120">必須</span><span class="sxs-lookup"><span data-stu-id="e8350-120">Required</span></span><br><span data-ttu-id="e8350-121">システム生成</span><span class="sxs-lookup"><span data-stu-id="e8350-121">System-generated</span></span> | <span data-ttu-id="e8350-122">システムが生成した、レベルの一意識別子です。</span><span class="sxs-lookup"><span data-stu-id="e8350-122">The system-generated unique identifier for the level.</span></span> |
| <span data-ttu-id="e8350-123">**評価レベル ID**</span><span class="sxs-lookup"><span data-stu-id="e8350-123">**Rating Level ID**</span></span><br><span data-ttu-id="e8350-124">mshr_ratinglevelid</span><span class="sxs-lookup"><span data-stu-id="e8350-124">mshr_ratinglevelid</span></span><br><span data-ttu-id="e8350-125">*文字列*</span><span class="sxs-lookup"><span data-stu-id="e8350-125">*String*</span></span> | <span data-ttu-id="e8350-126">読み取り/書き込み</span><span class="sxs-lookup"><span data-stu-id="e8350-126">Read/write</span></span><br><span data-ttu-id="e8350-127">必須</span><span class="sxs-lookup"><span data-stu-id="e8350-127">Required</span></span> | <span data-ttu-id="e8350-128">ユーザーが読取り可能なレベルの一意識別子です。</span><span class="sxs-lookup"><span data-stu-id="e8350-128">User-readable unique identifier for the level.</span></span> |
| <span data-ttu-id="e8350-129">**評価モデル ID**</span><span class="sxs-lookup"><span data-stu-id="e8350-129">**Rating Model ID**</span></span><br><span data-ttu-id="e8350-130">mshr_ratingmodelid</span><span class="sxs-lookup"><span data-stu-id="e8350-130">mshr_ratingmodelid</span></span><br><span data-ttu-id="e8350-131">*文字列*</span><span class="sxs-lookup"><span data-stu-id="e8350-131">*String*</span></span> | <span data-ttu-id="e8350-132">読み取り/書き込み</span><span class="sxs-lookup"><span data-stu-id="e8350-132">Read/write</span></span><br><span data-ttu-id="e8350-133">必須</span><span class="sxs-lookup"><span data-stu-id="e8350-133">Required</span></span> | <span data-ttu-id="e8350-134">評価レベルが属する評価モデルです。</span><span class="sxs-lookup"><span data-stu-id="e8350-134">The rating model to which the rating level belongs.</span></span> |
| <span data-ttu-id="e8350-135">**評価モデル エンティティ ID**</span><span class="sxs-lookup"><span data-stu-id="e8350-135">**Rating Model Entity ID**</span></span><br><span data-ttu-id="e8350-136">_mshr_fk_ratingmodelentity_id_value</span><span class="sxs-lookup"><span data-stu-id="e8350-136">_mshr_fk_ratingmodelentity_id_value</span></span><br><span data-ttu-id="e8350-137">*GUID*</span><span class="sxs-lookup"><span data-stu-id="e8350-137">*GUID*</span></span> | <span data-ttu-id="e8350-138">読み取り専用</span><span class="sxs-lookup"><span data-stu-id="e8350-138">Read-only</span></span><br><span data-ttu-id="e8350-139">必須</span><span class="sxs-lookup"><span data-stu-id="e8350-139">Required</span></span><br><span data-ttu-id="e8350-140">外部キー : mshr_hcmratingmodelentity の mshr_hcmratingmodelentityid</span><span class="sxs-lookup"><span data-stu-id="e8350-140">Foreign key: mshr_hcmratingmodelentityid of mshr_hcmratingmodelentity</span></span> | <span data-ttu-id="e8350-141">システムが生成する、評価レベルが属する評価モデルの識別子です。</span><span class="sxs-lookup"><span data-stu-id="e8350-141">The system-generated identifier for the rating model to which the rating level belongs.</span></span> |
| <span data-ttu-id="e8350-142">**説明**</span><span class="sxs-lookup"><span data-stu-id="e8350-142">**Description**</span></span><br><span data-ttu-id="e8350-143">mshr_description</span><span class="sxs-lookup"><span data-stu-id="e8350-143">mshr_description</span></span><br><span data-ttu-id="e8350-144">*文字列*</span><span class="sxs-lookup"><span data-stu-id="e8350-144">*String*</span></span> | <span data-ttu-id="e8350-145">読み取り/書き込み</span><span class="sxs-lookup"><span data-stu-id="e8350-145">Read/write</span></span><br><span data-ttu-id="e8350-146">必須</span><span class="sxs-lookup"><span data-stu-id="e8350-146">Required</span></span> | <span data-ttu-id="e8350-147">評価レベルの説明です。</span><span class="sxs-lookup"><span data-stu-id="e8350-147">The description of the rating level.</span></span> |
| <span data-ttu-id="e8350-148">**係数**</span><span class="sxs-lookup"><span data-stu-id="e8350-148">**Factor**</span></span><br><span data-ttu-id="e8350-149">mshr_factor</span><span class="sxs-lookup"><span data-stu-id="e8350-149">mshr_factor</span></span><br><span data-ttu-id="e8350-150">*整数*</span><span class="sxs-lookup"><span data-stu-id="e8350-150">*Integer*</span></span> | <span data-ttu-id="e8350-151">読み取り/書き込み</span><span class="sxs-lookup"><span data-stu-id="e8350-151">Read/write</span></span><br><span data-ttu-id="e8350-152">必須</span><span class="sxs-lookup"><span data-stu-id="e8350-152">Required</span></span> | <span data-ttu-id="e8350-153">評価レベルの係数です。</span><span class="sxs-lookup"><span data-stu-id="e8350-153">The factor for the rating level.</span></span> <span data-ttu-id="e8350-154">評価レベルの異なる数の項目を比較する際には、スコアを正規化するためにこの係数が使用されます。</span><span class="sxs-lookup"><span data-stu-id="e8350-154">When you compare items with a different number of rating levels, the factor is used to normalize the scores.</span></span> <span data-ttu-id="e8350-155">値は 0 (ゼロ) から 9 までの間の整数値である必要があります。</span><span class="sxs-lookup"><span data-stu-id="e8350-155">The value must be an integer between 0 and 9.</span></span> |
| <span data-ttu-id="e8350-156">**メモ**</span><span class="sxs-lookup"><span data-stu-id="e8350-156">**Note**</span></span><br><span data-ttu-id="e8350-157">mshr_note</span><span class="sxs-lookup"><span data-stu-id="e8350-157">mshr_note</span></span><br><span data-ttu-id="e8350-158">*文字列*</span><span class="sxs-lookup"><span data-stu-id="e8350-158">*String*</span></span> | <span data-ttu-id="e8350-159">読み取り/書き込み</span><span class="sxs-lookup"><span data-stu-id="e8350-159">Read/write</span></span><br><span data-ttu-id="e8350-160">オプション</span><span class="sxs-lookup"><span data-stu-id="e8350-160">Optional</span></span> | <span data-ttu-id="e8350-161">評価レベルに関連付けられているメモです。</span><span class="sxs-lookup"><span data-stu-id="e8350-161">Any notes associated with the rating level.</span></span> |
| <span data-ttu-id="e8350-162">**基本フィールド**</span><span class="sxs-lookup"><span data-stu-id="e8350-162">**Primary Field**</span></span><br><span data-ttu-id="e8350-163">mshr_primaryfield</span><span class="sxs-lookup"><span data-stu-id="e8350-163">mshr_primaryfield</span></span><br><span data-ttu-id="e8350-164">*文字列*</span><span class="sxs-lookup"><span data-stu-id="e8350-164">*String*</span></span> | <span data-ttu-id="e8350-165">読み取り専用</span><span class="sxs-lookup"><span data-stu-id="e8350-165">Read-only</span></span><br><span data-ttu-id="e8350-166">必須</span><span class="sxs-lookup"><span data-stu-id="e8350-166">Required</span></span> | <span data-ttu-id="e8350-167">エンティティ レコードの識別子として使用されるフィールドです。</span><span class="sxs-lookup"><span data-stu-id="e8350-167">Field to be used as an identifier of the entity record.</span></span> <span data-ttu-id="e8350-168">評価レベル ID と評価モデル ID の組み合わせです。</span><span class="sxs-lookup"><span data-stu-id="e8350-168">Combination of rating level ID and rating model ID.</span></span> |

## <a name="see-also"></a><span data-ttu-id="e8350-169">参照</span><span class="sxs-lookup"><span data-stu-id="e8350-169">See also</span></span>

[<span data-ttu-id="e8350-170">申請者追跡システム統合APIの概要</span><span class="sxs-lookup"><span data-stu-id="e8350-170">Applicant Tracking System integration API introduction</span></span>](hr-admin-integration-ats-api-introduction.md)<br>
[<span data-ttu-id="e8350-171">採用する採用候補者に対するクエリの例</span><span class="sxs-lookup"><span data-stu-id="e8350-171">Example query for Candidate to hire</span></span>](hr-admin-integration-ats-api-candidate-to-hire-example-query.md)
