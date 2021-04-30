---
title: 職位の給与詳細
description: このトピックでは、Dynamics 365 Human Resources における職位エンティティの給与詳細に対するクエリの詳細および例を示します。
author: jcart
manager: tfehr
ms.date: 04/07/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: jcart
ms.search.validFrom: 2021-04-07
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: f6c4bb0e2f4521e8c870f6c4fb645e2ce506138c
ms.sourcegitcommit: d18d9cdb175c9d42eafbed66352c24b2aa94258b
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/13/2021
ms.locfileid: "5882020"
---
# <a name="payroll-position"></a><span data-ttu-id="9fae3-103">給与職位</span><span class="sxs-lookup"><span data-stu-id="9fae3-103">Payroll position</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="9fae3-104">このトピックでは、Dynamics 365 Human Resources における職位エンティティの給与詳細に対するクエリの詳細および例を示します。</span><span class="sxs-lookup"><span data-stu-id="9fae3-104">This topic provides details and an example query for the Payroll details for the Positions entity in Dynamics 365 Human Resources.</span></span>

## <a name="properties"></a><span data-ttu-id="9fae3-105">プロパティ</span><span class="sxs-lookup"><span data-stu-id="9fae3-105">Properties</span></span>

| <span data-ttu-id="9fae3-106">プロパティ</span><span class="sxs-lookup"><span data-stu-id="9fae3-106">Property</span></span><br><span data-ttu-id="9fae3-107">**現物名**</span><span class="sxs-lookup"><span data-stu-id="9fae3-107">**Physical name**</span></span><br><span data-ttu-id="9fae3-108">**_種類_**</span><span class="sxs-lookup"><span data-stu-id="9fae3-108">**_Type_**</span></span> | <span data-ttu-id="9fae3-109">使用</span><span class="sxs-lookup"><span data-stu-id="9fae3-109">Use</span></span> | <span data-ttu-id="9fae3-110">説明</span><span class="sxs-lookup"><span data-stu-id="9fae3-110">Description</span></span> |
| --- | --- | --- |
| <span data-ttu-id="9fae3-111">**年間基本勤務時間**</span><span class="sxs-lookup"><span data-stu-id="9fae3-111">**Annual regular hours**</span></span><br><span data-ttu-id="9fae3-112">annualregularhours</span><span class="sxs-lookup"><span data-stu-id="9fae3-112">annualregularhours</span></span><br><span data-ttu-id="9fae3-113">*実数*</span><span class="sxs-lookup"><span data-stu-id="9fae3-113">*Decimal*</span></span> | <span data-ttu-id="9fae3-114">読み取り専用</span><span class="sxs-lookup"><span data-stu-id="9fae3-114">Read-only</span></span><br><span data-ttu-id="9fae3-115">必須</span><span class="sxs-lookup"><span data-stu-id="9fae3-115">Required</span></span> | <span data-ttu-id="9fae3-116">職位に定義されている年間基本勤務時間。</span><span class="sxs-lookup"><span data-stu-id="9fae3-116">Annual regular hours defined on the position.</span></span>  |
| <span data-ttu-id="9fae3-117">**給与職位詳細エンティティ ID**</span><span class="sxs-lookup"><span data-stu-id="9fae3-117">**Payroll position details entity ID**</span></span><br><span data-ttu-id="9fae3-118">payrollpositiondetailsentityid</span><span class="sxs-lookup"><span data-stu-id="9fae3-118">payrollpositiondetailsentityid</span></span><br><span data-ttu-id="9fae3-119">*Guid*</span><span class="sxs-lookup"><span data-stu-id="9fae3-119">*Guid*</span></span> | <span data-ttu-id="9fae3-120">必須</span><span class="sxs-lookup"><span data-stu-id="9fae3-120">Required</span></span><br><span data-ttu-id="9fae3-121">システム生成。</span><span class="sxs-lookup"><span data-stu-id="9fae3-121">System generated.</span></span> | <span data-ttu-id="9fae3-122">職位を一意に識別するためのシステム生成の GUID 値。</span><span class="sxs-lookup"><span data-stu-id="9fae3-122">A system-generated GUID value to uniquely identify the position.</span></span>  |
| <span data-ttu-id="9fae3-123">**基本フィールド**</span><span class="sxs-lookup"><span data-stu-id="9fae3-123">**Primary field**</span></span><br><span data-ttu-id="9fae3-124">mshr_primaryfield</span><span class="sxs-lookup"><span data-stu-id="9fae3-124">mshr_primaryfield</span></span><br><span data-ttu-id="9fae3-125">*文字列*</span><span class="sxs-lookup"><span data-stu-id="9fae3-125">*String*</span></span> | <span data-ttu-id="9fae3-126">必須</span><span class="sxs-lookup"><span data-stu-id="9fae3-126">Required</span></span><br><span data-ttu-id="9fae3-127">システム生成</span><span class="sxs-lookup"><span data-stu-id="9fae3-127">System generated</span></span> |  |
| <span data-ttu-id="9fae3-128">**職位職務 ID の値**</span><span class="sxs-lookup"><span data-stu-id="9fae3-128">**Position job ID value**</span></span><br><span data-ttu-id="9fae3-129">_mshr_fk_positionjob_id_value</span><span class="sxs-lookup"><span data-stu-id="9fae3-129">_mshr_fk_positionjob_id_value</span></span><br><span data-ttu-id="9fae3-130">*GUID*</span><span class="sxs-lookup"><span data-stu-id="9fae3-130">*GUID*</span></span> | <span data-ttu-id="9fae3-131">読み取り専用</span><span class="sxs-lookup"><span data-stu-id="9fae3-131">Read-only</span></span><br><span data-ttu-id="9fae3-132">必須</span><span class="sxs-lookup"><span data-stu-id="9fae3-132">Required</span></span><br><span data-ttu-id="9fae3-133">外部キー: mshr_payrollpositionjobentity の mshr_PayrollPositionJobEntity</span><span class="sxs-lookup"><span data-stu-id="9fae3-133">Foreign key:mshr_PayrollPositionJobEntity of the mshr_payrollpositionjobentity</span></span> |<span data-ttu-id="9fae3-134">この職位に関連付けられているジョブの ID です。</span><span class="sxs-lookup"><span data-stu-id="9fae3-134">The ID of the job associated with the position.</span></span>|
| <span data-ttu-id="9fae3-135">**固定報酬の報酬計画 ID 値**</span><span class="sxs-lookup"><span data-stu-id="9fae3-135">**Fixed compensation plan ID value**</span></span><br><span data-ttu-id="9fae3-136">_mshr_fk_fixedcompplan_id_value</span><span class="sxs-lookup"><span data-stu-id="9fae3-136">_mshr_fk_fixedcompplan_id_value</span></span><br><span data-ttu-id="9fae3-137">*GUID*</span><span class="sxs-lookup"><span data-stu-id="9fae3-137">*GUID*</span></span> | <span data-ttu-id="9fae3-138">読み取り専用</span><span class="sxs-lookup"><span data-stu-id="9fae3-138">Read-only</span></span><br><span data-ttu-id="9fae3-139">必須</span><span class="sxs-lookup"><span data-stu-id="9fae3-139">Required</span></span><br><span data-ttu-id="9fae3-140">外部キー: mshr_payrollfixedcompensationplanentity の mshr_FixedCompPlan_id</span><span class="sxs-lookup"><span data-stu-id="9fae3-140">Foreign key: mshr_FixedCompPlan_id of mshr_payrollfixedcompensationplanentity</span></span>  | <span data-ttu-id="9fae3-141">この職位に関連付けられている固定報酬計画の ID です。</span><span class="sxs-lookup"><span data-stu-id="9fae3-141">The ID of the fixed compensation plan associated with the position.</span></span> |
| <span data-ttu-id="9fae3-142">**支払サイクル ID**</span><span class="sxs-lookup"><span data-stu-id="9fae3-142">**Pay cycle ID**</span></span><br><span data-ttu-id="9fae3-143">mshr_primaryfield</span><span class="sxs-lookup"><span data-stu-id="9fae3-143">mshr_primaryfield</span></span><br><span data-ttu-id="9fae3-144">*文字列*</span><span class="sxs-lookup"><span data-stu-id="9fae3-144">*String*</span></span> | <span data-ttu-id="9fae3-145">読み取り専用</span><span class="sxs-lookup"><span data-stu-id="9fae3-145">Read-only</span></span><br><span data-ttu-id="9fae3-146">必須</span><span class="sxs-lookup"><span data-stu-id="9fae3-146">Required</span></span> | <span data-ttu-id="9fae3-147">職位に定義された支払サイクル。</span><span class="sxs-lookup"><span data-stu-id="9fae3-147">The pay cycle defined on the position.</span></span> |
| <span data-ttu-id="9fae3-148">**法人による支払**</span><span class="sxs-lookup"><span data-stu-id="9fae3-148">**Paid by legal entity**</span></span><br><span data-ttu-id="9fae3-149">paidbylegalentity</span><span class="sxs-lookup"><span data-stu-id="9fae3-149">paidbylegalentity</span></span><br><span data-ttu-id="9fae3-150">*文字列*</span><span class="sxs-lookup"><span data-stu-id="9fae3-150">*String*</span></span> | <span data-ttu-id="9fae3-151">読み取り専用</span><span class="sxs-lookup"><span data-stu-id="9fae3-151">Read-only</span></span><br><span data-ttu-id="9fae3-152">必須</span><span class="sxs-lookup"><span data-stu-id="9fae3-152">Required</span></span> | <span data-ttu-id="9fae3-153">支払の発行を担当する職位で定義されている法人。</span><span class="sxs-lookup"><span data-stu-id="9fae3-153">The legal entity defined on the positoin responsible for issuing payment.</span></span> |
| <span data-ttu-id="9fae3-154">**職位 ID**</span><span class="sxs-lookup"><span data-stu-id="9fae3-154">**Position ID**</span></span><br><span data-ttu-id="9fae3-155">mshr_positionid</span><span class="sxs-lookup"><span data-stu-id="9fae3-155">mshr_positionid</span></span><br><span data-ttu-id="9fae3-156">*文字列*</span><span class="sxs-lookup"><span data-stu-id="9fae3-156">*String*</span></span> | <span data-ttu-id="9fae3-157">読み取り専用</span><span class="sxs-lookup"><span data-stu-id="9fae3-157">Read-only</span></span><br><span data-ttu-id="9fae3-158">必須</span><span class="sxs-lookup"><span data-stu-id="9fae3-158">Required</span></span> | <span data-ttu-id="9fae3-159">職位の ID。</span><span class="sxs-lookup"><span data-stu-id="9fae3-159">The ID of the position.</span></span> |
| <span data-ttu-id="9fae3-160">**失効日**</span><span class="sxs-lookup"><span data-stu-id="9fae3-160">**Valid to**</span></span><br><span data-ttu-id="9fae3-161">validto</span><span class="sxs-lookup"><span data-stu-id="9fae3-161">validto</span></span><br><span data-ttu-id="9fae3-162">*日時オフセット*</span><span class="sxs-lookup"><span data-stu-id="9fae3-162">*Date Time Offset*</span></span> | <span data-ttu-id="9fae3-163">読み取り専用</span><span class="sxs-lookup"><span data-stu-id="9fae3-163">Read-only</span></span><br><span data-ttu-id="9fae3-164">必須</span><span class="sxs-lookup"><span data-stu-id="9fae3-164">Required</span></span> |<span data-ttu-id="9fae3-165">職位の詳細が有効になる日付。</span><span class="sxs-lookup"><span data-stu-id="9fae3-165">The date the position details are valid from.</span></span>  |
| <span data-ttu-id="9fae3-166">**発効日**</span><span class="sxs-lookup"><span data-stu-id="9fae3-166">**Valid from**</span></span><br><span data-ttu-id="9fae3-167">validfrom</span><span class="sxs-lookup"><span data-stu-id="9fae3-167">validfrom</span></span><br><span data-ttu-id="9fae3-168">*日時オフセット*</span><span class="sxs-lookup"><span data-stu-id="9fae3-168">*Date Time Offset*</span></span> | <span data-ttu-id="9fae3-169">読み取り専用</span><span class="sxs-lookup"><span data-stu-id="9fae3-169">Read-only</span></span><br><span data-ttu-id="9fae3-170">必須</span><span class="sxs-lookup"><span data-stu-id="9fae3-170">Required</span></span> |<span data-ttu-id="9fae3-171">職位の詳細が有効な日付。</span><span class="sxs-lookup"><span data-stu-id="9fae3-171">The date the position details are valid to.</span></span>  |

<span data-ttu-id="9fae3-172">**クエリ**</span><span class="sxs-lookup"><span data-stu-id="9fae3-172">**Query**</span></span>

<span data-ttu-id="9fae3-173">**申請**</span><span class="sxs-lookup"><span data-stu-id="9fae3-173">**Request**</span></span>

```http
GET [Organizaton URI]/api/data/v9.1/mshr_payrollpositionentities?$filter=mshr_positionid eq @positionid and mshr_validfrom le @asofdate and mshr_validto ge @asofdate&@positionid='000276'&@asofdate=2021-04-01
```

<span data-ttu-id="9fae3-174">**応答**</span><span class="sxs-lookup"><span data-stu-id="9fae3-174">**Response**</span></span>

```json
{
            "mshr_positionid": "000276",
            "mshr_paycycleid": "w",
            "mshr_annualregularhours": 3000,
            "mshr_paidbylegalentity": "USMF",
            "mshr_validfrom": "2021-03-14T00:00:00Z",
            "mshr_validto": "2154-12-31T00:00:00Z",
            "mshr_primaryfield": "000276 | 3/14/2021",
            "_mshr_fk_job_id_value": "00010094-0000-0000-df00-014105000000",
            "_mshr_fk_fixedcompplan_id_value": "0000029f-0000-0000-d5ff-004105000000",
            "mshr_payrollpositionentityid": "00010097-0000-0000-df00-014105000000"
}
```
