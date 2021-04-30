---
title: 固定報酬の報酬計画
description: このトピックでは、Dynamics 365 Human Resources における固定報酬の報酬計画エンティティに対するクエリの詳細および例を示します。
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
ms.openlocfilehash: 78a274cc491041d3d917a50bfb433f667cd8c255
ms.sourcegitcommit: d18d9cdb175c9d42eafbed66352c24b2aa94258b
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/13/2021
ms.locfileid: "5882025"
---
# <a name="payroll-fixed-compensation-plan"></a><span data-ttu-id="e4242-103">固定報酬の報酬計画</span><span class="sxs-lookup"><span data-stu-id="e4242-103">Payroll fixed compensation plan</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="e4242-104">このトピックでは、Dynamics 365 Human Resources における固定報酬の報酬計画エンティティに対するクエリの詳細および例を示します。</span><span class="sxs-lookup"><span data-stu-id="e4242-104">This topic provides details and an example query for the Payroll fixed compensation plan entity in Dynamics 365 Human Resources.</span></span>

## <a name="properties"></a><span data-ttu-id="e4242-105">プロパティ</span><span class="sxs-lookup"><span data-stu-id="e4242-105">Properties</span></span>

| <span data-ttu-id="e4242-106">プロパティ</span><span class="sxs-lookup"><span data-stu-id="e4242-106">Property</span></span><br><span data-ttu-id="e4242-107">**現物名**</span><span class="sxs-lookup"><span data-stu-id="e4242-107">**Physical name**</span></span><br><span data-ttu-id="e4242-108">**_種類_**</span><span class="sxs-lookup"><span data-stu-id="e4242-108">**_Type_**</span></span> | <span data-ttu-id="e4242-109">使用</span><span class="sxs-lookup"><span data-stu-id="e4242-109">Use</span></span> | <span data-ttu-id="e4242-110">説明</span><span class="sxs-lookup"><span data-stu-id="e4242-110">Description</span></span> |
| --- | --- | --- |
| <span data-ttu-id="e4242-111">**従業員 ID**</span><span class="sxs-lookup"><span data-stu-id="e4242-111">**Employee ID**</span></span><br><span data-ttu-id="e4242-112">mshr_fk_employee_id_value</span><span class="sxs-lookup"><span data-stu-id="e4242-112">mshr_fk_employee_id_value</span></span><br><span data-ttu-id="e4242-113">*GUID*</span><span class="sxs-lookup"><span data-stu-id="e4242-113">*GUID*</span></span> | <span data-ttu-id="e4242-114">読み取り専用</span><span class="sxs-lookup"><span data-stu-id="e4242-114">Read-only</span></span><br><span data-ttu-id="e4242-115">必須</span><span class="sxs-lookup"><span data-stu-id="e4242-115">Required</span></span><br><span data-ttu-id="e4242-116">外部キー: mshr_payrollemployeeentity エンティティの mshr_Employee_id</span><span class="sxs-lookup"><span data-stu-id="e4242-116">Foreign key:mshr_Employee_id of mshr_payrollemployeeentity entity</span></span>  | <span data-ttu-id="e4242-117">従業員 ID</span><span class="sxs-lookup"><span data-stu-id="e4242-117">Employee ID</span></span> |
| <span data-ttu-id="e4242-118">**支払レート**</span><span class="sxs-lookup"><span data-stu-id="e4242-118">**Pay rate**</span></span><br><span data-ttu-id="e4242-119">mshr_payrate</span><span class="sxs-lookup"><span data-stu-id="e4242-119">mshr_payrate</span></span><br><span data-ttu-id="e4242-120">*実数*</span><span class="sxs-lookup"><span data-stu-id="e4242-120">*Decimal*</span></span> | <span data-ttu-id="e4242-121">読み取り専用</span><span class="sxs-lookup"><span data-stu-id="e4242-121">Read-only</span></span><br><span data-ttu-id="e4242-122">必須</span><span class="sxs-lookup"><span data-stu-id="e4242-122">Required</span></span> | <span data-ttu-id="e4242-123">固定報酬計画で定義された支払レート。</span><span class="sxs-lookup"><span data-stu-id="e4242-123">Pay rate defined in fixed compensation plan.</span></span> |
| <span data-ttu-id="e4242-124">**計画 ID**</span><span class="sxs-lookup"><span data-stu-id="e4242-124">**Plan ID**</span></span><br><span data-ttu-id="e4242-125">mshr_planid</span><span class="sxs-lookup"><span data-stu-id="e4242-125">mshr_planid</span></span><br><span data-ttu-id="e4242-126">*文字列*</span><span class="sxs-lookup"><span data-stu-id="e4242-126">*String*</span></span> | <span data-ttu-id="e4242-127">読み取り専用</span><span class="sxs-lookup"><span data-stu-id="e4242-127">Read-only</span></span><br><span data-ttu-id="e4242-128">必須</span><span class="sxs-lookup"><span data-stu-id="e4242-128">Required</span></span> |<span data-ttu-id="e4242-129">報酬計画を指定します。</span><span class="sxs-lookup"><span data-stu-id="e4242-129">Specifies the compensation plan.</span></span>  |
| <span data-ttu-id="e4242-130">**発効日**</span><span class="sxs-lookup"><span data-stu-id="e4242-130">**Valid from**</span></span><br><span data-ttu-id="e4242-131">mshr_validfrom</span><span class="sxs-lookup"><span data-stu-id="e4242-131">mshr_validfrom</span></span><br><span data-ttu-id="e4242-132">*日時オフセット*</span><span class="sxs-lookup"><span data-stu-id="e4242-132">*Date Time Offset*</span></span> |  <span data-ttu-id="e4242-133">読み取り専用</span><span class="sxs-lookup"><span data-stu-id="e4242-133">Read-only</span></span><br><span data-ttu-id="e4242-134">必須</span><span class="sxs-lookup"><span data-stu-id="e4242-134">Required</span></span> |<span data-ttu-id="e4242-135">従業員の固定報酬が有効になる日付。</span><span class="sxs-lookup"><span data-stu-id="e4242-135">Date the employee fixed compensation is valid from.</span></span>  |
| <span data-ttu-id="e4242-136">**固定報酬の報酬計画エンティティ**</span><span class="sxs-lookup"><span data-stu-id="e4242-136">**Payroll Fixed Compensation Plan entity**</span></span><br><span data-ttu-id="e4242-137">mshr_payrollfixedcompensationplanentityid</span><span class="sxs-lookup"><span data-stu-id="e4242-137">mshr_payrollfixedcompensationplanentityid</span></span><br><span data-ttu-id="e4242-138">*GUID*</span><span class="sxs-lookup"><span data-stu-id="e4242-138">*GUID*</span></span> | <span data-ttu-id="e4242-139">必須</span><span class="sxs-lookup"><span data-stu-id="e4242-139">Required</span></span><br><span data-ttu-id="e4242-140">システム生成</span><span class="sxs-lookup"><span data-stu-id="e4242-140">Sytem generated</span></span> | <span data-ttu-id="e4242-141">システムで生成する、報酬計画を一意に識別する GUID 値です。</span><span class="sxs-lookup"><span data-stu-id="e4242-141">A system-generated GUID value to uniquely identify the compensation plan.</span></span> |
| <span data-ttu-id="e4242-142">**支払頻度**</span><span class="sxs-lookup"><span data-stu-id="e4242-142">**Pay frequency**</span></span><br><span data-ttu-id="e4242-143">mshr_payfrequency</span><span class="sxs-lookup"><span data-stu-id="e4242-143">mshr_payfrequency</span></span><br><span data-ttu-id="e4242-144">*文字列*</span><span class="sxs-lookup"><span data-stu-id="e4242-144">*String*</span></span> | <span data-ttu-id="e4242-145">読み取り専用</span><span class="sxs-lookup"><span data-stu-id="e4242-145">Read-only</span></span><br><span data-ttu-id="e4242-146">必須</span><span class="sxs-lookup"><span data-stu-id="e4242-146">Required</span></span> |<span data-ttu-id="e4242-147">従業員に支払われる頻度。</span><span class="sxs-lookup"><span data-stu-id="e4242-147">The frequency the employee will be paid.</span></span>  |
| <span data-ttu-id="e4242-148">**失効日**</span><span class="sxs-lookup"><span data-stu-id="e4242-148">**Valid to**</span></span><br><span data-ttu-id="e4242-149">mshr_validto</span><span class="sxs-lookup"><span data-stu-id="e4242-149">mshr_validto</span></span><br><span data-ttu-id="e4242-150">*日時オフセット*</span><span class="sxs-lookup"><span data-stu-id="e4242-150">*Date Time Offset*</span></span> | <span data-ttu-id="e4242-151">読み取り専用</span><span class="sxs-lookup"><span data-stu-id="e4242-151">Read-only</span></span> <br><span data-ttu-id="e4242-152">必須</span><span class="sxs-lookup"><span data-stu-id="e4242-152">Required</span></span> | <span data-ttu-id="e4242-153">従業員の固定報酬が有効な日付。</span><span class="sxs-lookup"><span data-stu-id="e4242-153">Date the employee fixed compensation is valid to.</span></span> |
| <span data-ttu-id="e4242-154">**職位 ID**</span><span class="sxs-lookup"><span data-stu-id="e4242-154">**Position ID**</span></span><br><span data-ttu-id="e4242-155">mshr_positionid</span><span class="sxs-lookup"><span data-stu-id="e4242-155">mshr_positionid</span></span><br><span data-ttu-id="e4242-156">*文字列*</span><span class="sxs-lookup"><span data-stu-id="e4242-156">*String*</span></span> | <span data-ttu-id="e4242-157">読み取り専用</span><span class="sxs-lookup"><span data-stu-id="e4242-157">Read-only</span></span> <br><span data-ttu-id="e4242-158">必須</span><span class="sxs-lookup"><span data-stu-id="e4242-158">Required</span></span> | <span data-ttu-id="e4242-159">従業員および固定報酬計画の登録に関連付けられた転記 ID。</span><span class="sxs-lookup"><span data-stu-id="e4242-159">Postion ID associated with the employee and fixed compensation plan enrollment.</span></span> |
| <span data-ttu-id="e4242-160">**通貨**</span><span class="sxs-lookup"><span data-stu-id="e4242-160">**Currency**</span></span><br><span data-ttu-id="e4242-161">mshr_currency</span><span class="sxs-lookup"><span data-stu-id="e4242-161">mshr_currency</span></span><br><span data-ttu-id="e4242-162">*文字列*</span><span class="sxs-lookup"><span data-stu-id="e4242-162">*String*</span></span> | <span data-ttu-id="e4242-163">読み取り専用</span><span class="sxs-lookup"><span data-stu-id="e4242-163">Read-only</span></span> <br><span data-ttu-id="e4242-164">必須</span><span class="sxs-lookup"><span data-stu-id="e4242-164">Required</span></span> |<span data-ttu-id="e4242-165">固定報酬計画に定義されている通貨</span><span class="sxs-lookup"><span data-stu-id="e4242-165">The currency defined for the fixed compensation plan</span></span>   |
| <span data-ttu-id="e4242-166">**個人番号**</span><span class="sxs-lookup"><span data-stu-id="e4242-166">**Personnel number**</span></span><br><span data-ttu-id="e4242-167">mshr_personnelnumber</span><span class="sxs-lookup"><span data-stu-id="e4242-167">mshr_personnelnumber</span></span><br><span data-ttu-id="e4242-168">*文字列*</span><span class="sxs-lookup"><span data-stu-id="e4242-168">*String*</span></span> | <span data-ttu-id="e4242-169">読み取り専用</span><span class="sxs-lookup"><span data-stu-id="e4242-169">Read-only</span></span><br><span data-ttu-id="e4242-170">必須</span><span class="sxs-lookup"><span data-stu-id="e4242-170">Required</span></span> |<span data-ttu-id="e4242-171">従業員の一意の職員番号。</span><span class="sxs-lookup"><span data-stu-id="e4242-171">The employee's unique personnel number.</span></span>  |

<span data-ttu-id="e4242-172">**クエリ**</span><span class="sxs-lookup"><span data-stu-id="e4242-172">**Query**</span></span>

<span data-ttu-id="e4242-173">**申請**</span><span class="sxs-lookup"><span data-stu-id="e4242-173">**Request**</span></span>

```http
GET [Organizaton URI]/api/data/v9.1/mshr_payrollfixedcompensationplanentities?$filter=mshr_personnelnumber eq @personnelnumber and mshr_validfrom le @asofdate and mshr_validto ge @asofdate&@personnelnumber='000041'&@asofdate=2021-04-01
```

<span data-ttu-id="e4242-174">**応答**</span><span class="sxs-lookup"><span data-stu-id="e4242-174">**Response**</span></span>

```json
{
            "mshr_planid": "GradeC",
            "mshr_personnelnumber": "000041",
            "mshr_payrate": 75200,
            "mshr_positionid": "000276",
            "mshr_validfrom": "2011-04-05T00:00:00Z",
            "mshr_validto": "2154-12-31T00:00:00Z",
            "mshr_payfrequency": "Annual",
            "mshr_currency": "USD",
            "_mshr_fk_employee_id_value": "00000d3c-0000-0000-d5ff-004105000000",
            "_mshr_fk_plan_id_value": "0000070c-0000-0000-b328-fef003000000",
            "_mshr_fk_job_id_value": "00010094-0000-0000-df00-014105000000",
            "mshr_payrollfixedcompensationplanentityid": "0000029f-0000-0000-d5ff-004105000000",
            "_mshr_fk_payroll_id_value": null
}
```
