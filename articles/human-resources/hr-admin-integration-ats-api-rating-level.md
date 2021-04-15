---
title: 評価レベル
description: このトピックでは、Dynamics 365 Human Resources の評価レベルのエンティティについて説明します。
author: jaredha
ms.date: 02/05/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: jaredha
ms.search.validFrom: 2021-02-05
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: eac80599de07a045aa233f1cdfd16fe0db8733a2
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/31/2021
ms.locfileid: "5800336"
---
# <a name="rating-level"></a><span data-ttu-id="3b05f-103">評価レベル</span><span class="sxs-lookup"><span data-stu-id="3b05f-103">Rating level</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="3b05f-104">このトピックでは、Dynamics 365 Human Resources の評価レベルのエンティティについて説明します。</span><span class="sxs-lookup"><span data-stu-id="3b05f-104">This topic describes the Rating level entity for Dynamics 365 Human Resources.</span></span>

<span data-ttu-id="3b05f-105">物理名 : mshr_hcmratinglevelentity</span><span class="sxs-lookup"><span data-stu-id="3b05f-105">Physical name: mshr_hcmratinglevelentity</span></span>

## <a name="description"></a><span data-ttu-id="3b05f-106">説明</span><span class="sxs-lookup"><span data-stu-id="3b05f-106">Description</span></span>

<span data-ttu-id="3b05f-107">このエンティティは、スキルの評価レベルを提供します。</span><span class="sxs-lookup"><span data-stu-id="3b05f-107">This entity provides the available rating levels for skills.</span></span> <span data-ttu-id="3b05f-108">評価レベルは、すべての法人に適用されます。</span><span class="sxs-lookup"><span data-stu-id="3b05f-108">Rating levels apply across all legal entities.</span></span>

## <a name="json-representation"></a><span data-ttu-id="3b05f-109">JSON 表記</span><span class="sxs-lookup"><span data-stu-id="3b05f-109">JSON representation</span></span>

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

## <a name="properties"></a><span data-ttu-id="3b05f-110">プロパティ</span><span class="sxs-lookup"><span data-stu-id="3b05f-110">Properties</span></span>

| <span data-ttu-id="3b05f-111">プロパティ</span><span class="sxs-lookup"><span data-stu-id="3b05f-111">Property</span></span><br><span data-ttu-id="3b05f-112">**現物名**</span><span class="sxs-lookup"><span data-stu-id="3b05f-112">**Physical name**</span></span><br><span data-ttu-id="3b05f-113">**_種類_**</span><span class="sxs-lookup"><span data-stu-id="3b05f-113">**_Type_**</span></span> | <span data-ttu-id="3b05f-114">使用</span><span class="sxs-lookup"><span data-stu-id="3b05f-114">Use</span></span> | <span data-ttu-id="3b05f-115">説明</span><span class="sxs-lookup"><span data-stu-id="3b05f-115">Description</span></span> |
| --- | --- | --- |
| <span data-ttu-id="3b05f-116">**評価レベル エンティティ ID**</span><span class="sxs-lookup"><span data-stu-id="3b05f-116">**Rating Level Entity ID**</span></span><br><span data-ttu-id="3b05f-117">mshr_hcmratinglevelentityid</span><span class="sxs-lookup"><span data-stu-id="3b05f-117">mshr_hcmratinglevelentityid</span></span><br><span data-ttu-id="3b05f-118">*GUID*</span><span class="sxs-lookup"><span data-stu-id="3b05f-118">*GUID*</span></span> | <span data-ttu-id="3b05f-119">読み取り専用</span><span class="sxs-lookup"><span data-stu-id="3b05f-119">Read-only</span></span><br><span data-ttu-id="3b05f-120">必須</span><span class="sxs-lookup"><span data-stu-id="3b05f-120">Required</span></span><br><span data-ttu-id="3b05f-121">システム生成</span><span class="sxs-lookup"><span data-stu-id="3b05f-121">System-generated</span></span> | <span data-ttu-id="3b05f-122">システムが生成した、レベルの一意識別子です。</span><span class="sxs-lookup"><span data-stu-id="3b05f-122">The system-generated unique identifier for the level.</span></span> |
| <span data-ttu-id="3b05f-123">**評価レベル ID**</span><span class="sxs-lookup"><span data-stu-id="3b05f-123">**Rating Level ID**</span></span><br><span data-ttu-id="3b05f-124">mshr_ratinglevelid</span><span class="sxs-lookup"><span data-stu-id="3b05f-124">mshr_ratinglevelid</span></span><br><span data-ttu-id="3b05f-125">*文字列*</span><span class="sxs-lookup"><span data-stu-id="3b05f-125">*String*</span></span> | <span data-ttu-id="3b05f-126">読み取り/書き込み</span><span class="sxs-lookup"><span data-stu-id="3b05f-126">Read/write</span></span><br><span data-ttu-id="3b05f-127">必須</span><span class="sxs-lookup"><span data-stu-id="3b05f-127">Required</span></span> | <span data-ttu-id="3b05f-128">ユーザーが読取り可能なレベルの一意識別子です。</span><span class="sxs-lookup"><span data-stu-id="3b05f-128">User-readable unique identifier for the level.</span></span> |
| <span data-ttu-id="3b05f-129">**評価モデル ID**</span><span class="sxs-lookup"><span data-stu-id="3b05f-129">**Rating Model ID**</span></span><br><span data-ttu-id="3b05f-130">mshr_ratingmodelid</span><span class="sxs-lookup"><span data-stu-id="3b05f-130">mshr_ratingmodelid</span></span><br><span data-ttu-id="3b05f-131">*文字列*</span><span class="sxs-lookup"><span data-stu-id="3b05f-131">*String*</span></span> | <span data-ttu-id="3b05f-132">読み取り/書き込み</span><span class="sxs-lookup"><span data-stu-id="3b05f-132">Read/write</span></span><br><span data-ttu-id="3b05f-133">必須</span><span class="sxs-lookup"><span data-stu-id="3b05f-133">Required</span></span> | <span data-ttu-id="3b05f-134">評価レベルが属する評価モデルです。</span><span class="sxs-lookup"><span data-stu-id="3b05f-134">The rating model to which the rating level belongs.</span></span> |
| <span data-ttu-id="3b05f-135">**評価モデル エンティティ ID**</span><span class="sxs-lookup"><span data-stu-id="3b05f-135">**Rating Model Entity ID**</span></span><br><span data-ttu-id="3b05f-136">_mshr_fk_ratingmodelentity_id_value</span><span class="sxs-lookup"><span data-stu-id="3b05f-136">_mshr_fk_ratingmodelentity_id_value</span></span><br><span data-ttu-id="3b05f-137">*GUID*</span><span class="sxs-lookup"><span data-stu-id="3b05f-137">*GUID*</span></span> | <span data-ttu-id="3b05f-138">読み取り専用</span><span class="sxs-lookup"><span data-stu-id="3b05f-138">Read-only</span></span><br><span data-ttu-id="3b05f-139">必須</span><span class="sxs-lookup"><span data-stu-id="3b05f-139">Required</span></span><br><span data-ttu-id="3b05f-140">外部キー : mshr_hcmratingmodelentity の mshr_hcmratingmodelentityid</span><span class="sxs-lookup"><span data-stu-id="3b05f-140">Foreign key: mshr_hcmratingmodelentityid of mshr_hcmratingmodelentity</span></span> | <span data-ttu-id="3b05f-141">システムが生成する、評価レベルが属する評価モデルの識別子です。</span><span class="sxs-lookup"><span data-stu-id="3b05f-141">The system-generated identifier for the rating model to which the rating level belongs.</span></span> |
| <span data-ttu-id="3b05f-142">**説明**</span><span class="sxs-lookup"><span data-stu-id="3b05f-142">**Description**</span></span><br><span data-ttu-id="3b05f-143">mshr_description</span><span class="sxs-lookup"><span data-stu-id="3b05f-143">mshr_description</span></span><br><span data-ttu-id="3b05f-144">*文字列*</span><span class="sxs-lookup"><span data-stu-id="3b05f-144">*String*</span></span> | <span data-ttu-id="3b05f-145">読み取り/書き込み</span><span class="sxs-lookup"><span data-stu-id="3b05f-145">Read/write</span></span><br><span data-ttu-id="3b05f-146">必須</span><span class="sxs-lookup"><span data-stu-id="3b05f-146">Required</span></span> | <span data-ttu-id="3b05f-147">評価レベルの説明です。</span><span class="sxs-lookup"><span data-stu-id="3b05f-147">The description of the rating level.</span></span> |
| <span data-ttu-id="3b05f-148">**係数**</span><span class="sxs-lookup"><span data-stu-id="3b05f-148">**Factor**</span></span><br><span data-ttu-id="3b05f-149">mshr_factor</span><span class="sxs-lookup"><span data-stu-id="3b05f-149">mshr_factor</span></span><br><span data-ttu-id="3b05f-150">*整数*</span><span class="sxs-lookup"><span data-stu-id="3b05f-150">*Integer*</span></span> | <span data-ttu-id="3b05f-151">読み取り/書き込み</span><span class="sxs-lookup"><span data-stu-id="3b05f-151">Read/write</span></span><br><span data-ttu-id="3b05f-152">必須</span><span class="sxs-lookup"><span data-stu-id="3b05f-152">Required</span></span> | <span data-ttu-id="3b05f-153">評価レベルの係数です。</span><span class="sxs-lookup"><span data-stu-id="3b05f-153">The factor for the rating level.</span></span> <span data-ttu-id="3b05f-154">評価レベルの異なる数の項目を比較する際には、スコアを正規化するためにこの係数が使用されます。</span><span class="sxs-lookup"><span data-stu-id="3b05f-154">When you compare items with a different number of rating levels, the factor is used to normalize the scores.</span></span> <span data-ttu-id="3b05f-155">値は 0 (ゼロ) から 9 までの間の整数値である必要があります。</span><span class="sxs-lookup"><span data-stu-id="3b05f-155">The value must be an integer between 0 and 9.</span></span> |
| <span data-ttu-id="3b05f-156">**メモ**</span><span class="sxs-lookup"><span data-stu-id="3b05f-156">**Note**</span></span><br><span data-ttu-id="3b05f-157">mshr_note</span><span class="sxs-lookup"><span data-stu-id="3b05f-157">mshr_note</span></span><br><span data-ttu-id="3b05f-158">*文字列*</span><span class="sxs-lookup"><span data-stu-id="3b05f-158">*String*</span></span> | <span data-ttu-id="3b05f-159">読み取り/書き込み</span><span class="sxs-lookup"><span data-stu-id="3b05f-159">Read/write</span></span><br><span data-ttu-id="3b05f-160">オプション</span><span class="sxs-lookup"><span data-stu-id="3b05f-160">Optional</span></span> | <span data-ttu-id="3b05f-161">評価レベルに関連付けられているメモです。</span><span class="sxs-lookup"><span data-stu-id="3b05f-161">Any notes associated with the rating level.</span></span> |
| <span data-ttu-id="3b05f-162">**基本フィールド**</span><span class="sxs-lookup"><span data-stu-id="3b05f-162">**Primary Field**</span></span><br><span data-ttu-id="3b05f-163">mshr_primaryfield</span><span class="sxs-lookup"><span data-stu-id="3b05f-163">mshr_primaryfield</span></span><br><span data-ttu-id="3b05f-164">*文字列*</span><span class="sxs-lookup"><span data-stu-id="3b05f-164">*String*</span></span> | <span data-ttu-id="3b05f-165">読み取り専用</span><span class="sxs-lookup"><span data-stu-id="3b05f-165">Read-only</span></span><br><span data-ttu-id="3b05f-166">必須</span><span class="sxs-lookup"><span data-stu-id="3b05f-166">Required</span></span> | <span data-ttu-id="3b05f-167">エンティティ レコードの識別子として使用されるフィールドです。</span><span class="sxs-lookup"><span data-stu-id="3b05f-167">Field to be used as an identifier of the entity record.</span></span> <span data-ttu-id="3b05f-168">評価レベル ID と評価モデル ID の組み合わせです。</span><span class="sxs-lookup"><span data-stu-id="3b05f-168">Combination of rating level ID and rating model ID.</span></span> |

## <a name="see-also"></a><span data-ttu-id="3b05f-169">参照</span><span class="sxs-lookup"><span data-stu-id="3b05f-169">See also</span></span>

[<span data-ttu-id="3b05f-170">申請者追跡システム統合APIの概要</span><span class="sxs-lookup"><span data-stu-id="3b05f-170">Applicant Tracking System integration API introduction</span></span>](hr-admin-integration-ats-api-introduction.md)<br>
[<span data-ttu-id="3b05f-171">採用する採用候補者に対するクエリの例</span><span class="sxs-lookup"><span data-stu-id="3b05f-171">Example query for Candidate to hire</span></span>](hr-admin-integration-ats-api-candidate-to-hire-example-query.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]