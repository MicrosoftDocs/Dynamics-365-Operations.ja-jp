---
title: 給与従業員
description: このトピックでは、Dynamics 365 Human Resources における給与従業員エンティティに対するクエリの詳細および例を示します。
author: jcart
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
ms.openlocfilehash: 0cd37a7323c0dd0dc6e60ff0495f827e9a8582c1
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/11/2021
ms.locfileid: "6019373"
---
# <a name="payroll-employee"></a><span data-ttu-id="e3666-103">給与従業員</span><span class="sxs-lookup"><span data-stu-id="e3666-103">Payroll employee</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="e3666-104">このトピックでは、Dynamics 365 Human Resources における給与従業員エンティティに対するクエリの詳細および例を示します。</span><span class="sxs-lookup"><span data-stu-id="e3666-104">This topic provides details and an example query for the Payroll employee entity in Dynamics 365 Human Resources.</span></span>

## <a name="properties"></a><span data-ttu-id="e3666-105">プロパティ</span><span class="sxs-lookup"><span data-stu-id="e3666-105">Properties</span></span>

| <span data-ttu-id="e3666-106">プロパティ</span><span class="sxs-lookup"><span data-stu-id="e3666-106">Property</span></span><br><span data-ttu-id="e3666-107">**現物名**</span><span class="sxs-lookup"><span data-stu-id="e3666-107">**Physical name**</span></span><br><span data-ttu-id="e3666-108">**_種類_**</span><span class="sxs-lookup"><span data-stu-id="e3666-108">**_Type_**</span></span> | <span data-ttu-id="e3666-109">使用</span><span class="sxs-lookup"><span data-stu-id="e3666-109">Use</span></span> | <span data-ttu-id="e3666-110">説明</span><span class="sxs-lookup"><span data-stu-id="e3666-110">Description</span></span> |
| --- | --- | --- |
| <span data-ttu-id="e3666-111">**個人番号**</span><span class="sxs-lookup"><span data-stu-id="e3666-111">**Personnel number**</span></span><br><span data-ttu-id="e3666-112">mshr_personnelnumber</span><span class="sxs-lookup"><span data-stu-id="e3666-112">mshr_personnelnumber</span></span><br><span data-ttu-id="e3666-113">*文字列*</span><span class="sxs-lookup"><span data-stu-id="e3666-113">*String*</span></span> | <span data-ttu-id="e3666-114">読み取り専用</span><span class="sxs-lookup"><span data-stu-id="e3666-114">Read-only</span></span><br><span data-ttu-id="e3666-115">必須</span><span class="sxs-lookup"><span data-stu-id="e3666-115">Required</span></span> | <span data-ttu-id="e3666-116">従業員の一意の職員番号。</span><span class="sxs-lookup"><span data-stu-id="e3666-116">The employee's unique personnel number.</span></span> |
| <span data-ttu-id="e3666-117">**基本フィールド**</span><span class="sxs-lookup"><span data-stu-id="e3666-117">**Primary field**</span></span><br><span data-ttu-id="e3666-118">mshr_primaryfield</span><span class="sxs-lookup"><span data-stu-id="e3666-118">mshr_primaryfield</span></span><br><span data-ttu-id="e3666-119">*文字列*</span><span class="sxs-lookup"><span data-stu-id="e3666-119">*String*</span></span> | <span data-ttu-id="e3666-120">必須</span><span class="sxs-lookup"><span data-stu-id="e3666-120">Required</span></span><br><span data-ttu-id="e3666-121">システム生成</span><span class="sxs-lookup"><span data-stu-id="e3666-121">System generated</span></span> |  |
| <span data-ttu-id="e3666-122">**姓**</span><span class="sxs-lookup"><span data-stu-id="e3666-122">**Last name**</span></span><br><span data-ttu-id="e3666-123">mshr_lastname</span><span class="sxs-lookup"><span data-stu-id="e3666-123">mshr_lastname</span></span><br><span data-ttu-id="e3666-124">*文字列*</span><span class="sxs-lookup"><span data-stu-id="e3666-124">*String*</span></span> | <span data-ttu-id="e3666-125">読み取り専用</span><span class="sxs-lookup"><span data-stu-id="e3666-125">Read only</span></span><br><span data-ttu-id="e3666-126">必須</span><span class="sxs-lookup"><span data-stu-id="e3666-126">Required</span></span> | <span data-ttu-id="e3666-127">従業員の姓。</span><span class="sxs-lookup"><span data-stu-id="e3666-127">Employee last name.</span></span> |
| <span data-ttu-id="e3666-128">**法人 ID**</span><span class="sxs-lookup"><span data-stu-id="e3666-128">**Legal entity ID**</span></span><br><span data-ttu-id="e3666-129">mshr_legalentityID</span><span class="sxs-lookup"><span data-stu-id="e3666-129">mshr_legalentityID</span></span><br><span data-ttu-id="e3666-130">*文字列*</span><span class="sxs-lookup"><span data-stu-id="e3666-130">*String*</span></span> | <span data-ttu-id="e3666-131">読み取り専用</span><span class="sxs-lookup"><span data-stu-id="e3666-131">Read-only</span></span><br><span data-ttu-id="e3666-132">必須</span><span class="sxs-lookup"><span data-stu-id="e3666-132">Required</span></span> | <span data-ttu-id="e3666-133">法人 (会社) を指定します。</span><span class="sxs-lookup"><span data-stu-id="e3666-133">Specifies the legal entity (company).</span></span> |
| <span data-ttu-id="e3666-134">**発効日**</span><span class="sxs-lookup"><span data-stu-id="e3666-134">**Valid from**</span></span><br><span data-ttu-id="e3666-135">mshr_namevalidfrom</span><span class="sxs-lookup"><span data-stu-id="e3666-135">mshr_namevalidfrom</span></span><br><span data-ttu-id="e3666-136">*日時オフセット*</span><span class="sxs-lookup"><span data-stu-id="e3666-136">*Date Time Offset*</span></span> | <span data-ttu-id="e3666-137">読み取り専用</span><span class="sxs-lookup"><span data-stu-id="e3666-137">Read-only</span></span> <br><span data-ttu-id="e3666-138">必須</span><span class="sxs-lookup"><span data-stu-id="e3666-138">Required</span></span> | <span data-ttu-id="e3666-139">従業員情報の有効日。</span><span class="sxs-lookup"><span data-stu-id="e3666-139">Date the employee information is valid from.</span></span>  |
| <span data-ttu-id="e3666-140">**種類**</span><span class="sxs-lookup"><span data-stu-id="e3666-140">**Gender**</span></span><br><span data-ttu-id="e3666-141">mshr_gender</span><span class="sxs-lookup"><span data-stu-id="e3666-141">mshr_gender</span></span><br><span data-ttu-id="e3666-142">*Int32*</span><span class="sxs-lookup"><span data-stu-id="e3666-142">*Int32*</span></span> | <span data-ttu-id="e3666-143">読み取り専用</span><span class="sxs-lookup"><span data-stu-id="e3666-143">Read-only</span></span><br><span data-ttu-id="e3666-144">必須</span><span class="sxs-lookup"><span data-stu-id="e3666-144">Required</span></span> | <span data-ttu-id="e3666-145">従業員の性別。</span><span class="sxs-lookup"><span data-stu-id="e3666-145">The employee's gender.</span></span> |
| <span data-ttu-id="e3666-146">**給与従業員エンティティ ID**</span><span class="sxs-lookup"><span data-stu-id="e3666-146">**Payroll employee entity ID**</span></span><br><span data-ttu-id="e3666-147">mshr_payrollemployeeentityid</span><span class="sxs-lookup"><span data-stu-id="e3666-147">mshr_payrollemployeeentityid</span></span><br><span data-ttu-id="e3666-148">*GUID*</span><span class="sxs-lookup"><span data-stu-id="e3666-148">*GUID*</span></span> | <span data-ttu-id="e3666-149">必須</span><span class="sxs-lookup"><span data-stu-id="e3666-149">Required</span></span><br><span data-ttu-id="e3666-150">システム生成</span><span class="sxs-lookup"><span data-stu-id="e3666-150">System generated</span></span> | <span data-ttu-id="e3666-151">従業員を一意に識別するためのシステム生成の GUID 値。</span><span class="sxs-lookup"><span data-stu-id="e3666-151">A system-generated GUID value to uniquely identify the employee.</span></span> |
| <span data-ttu-id="e3666-152">**雇用開始日**</span><span class="sxs-lookup"><span data-stu-id="e3666-152">**Employment start date**</span></span><br><span data-ttu-id="e3666-153">mshr_employmentstartdate</span><span class="sxs-lookup"><span data-stu-id="e3666-153">mshr_employmentstartdate</span></span><br><span data-ttu-id="e3666-154">*日時オフセット*</span><span class="sxs-lookup"><span data-stu-id="e3666-154">*Date time offset*</span></span> | <span data-ttu-id="e3666-155">読み取り専用</span><span class="sxs-lookup"><span data-stu-id="e3666-155">Read-only</span></span><br><span data-ttu-id="e3666-156">必須</span><span class="sxs-lookup"><span data-stu-id="e3666-156">Required</span></span> | <span data-ttu-id="e3666-157">従業員の雇用開始日。</span><span class="sxs-lookup"><span data-stu-id="e3666-157">The start date of the employee's employment.</span></span> |
| <span data-ttu-id="e3666-158">**識別タイプ ID**</span><span class="sxs-lookup"><span data-stu-id="e3666-158">**Identification type ID**</span></span><br><span data-ttu-id="e3666-159">mshr_identificationtypeid</span><span class="sxs-lookup"><span data-stu-id="e3666-159">mshr_identificationtypeid</span></span><br><span data-ttu-id="e3666-160">*文字列*</span><span class="sxs-lookup"><span data-stu-id="e3666-160">*String*</span></span> |<span data-ttu-id="e3666-161">読み取り専用</span><span class="sxs-lookup"><span data-stu-id="e3666-161">Read-only</span></span><br><span data-ttu-id="e3666-162">必須</span><span class="sxs-lookup"><span data-stu-id="e3666-162">Required</span></span> | <span data-ttu-id="e3666-163">従業員に対して定義される ID タイプ。</span><span class="sxs-lookup"><span data-stu-id="e3666-163">The identification type defined for the employee.</span></span> |
| <span data-ttu-id="e3666-164">**雇用終了日**</span><span class="sxs-lookup"><span data-stu-id="e3666-164">**Employment end date**</span></span><br><span data-ttu-id="e3666-165">mshr_employmentenddate</span><span class="sxs-lookup"><span data-stu-id="e3666-165">mshr_employmentenddate</span></span><br><span data-ttu-id="e3666-166">*日時オフセット*</span><span class="sxs-lookup"><span data-stu-id="e3666-166">*Date time offset*</span></span> | <span data-ttu-id="e3666-167">読み取り専用</span><span class="sxs-lookup"><span data-stu-id="e3666-167">Read-only</span></span><br><span data-ttu-id="e3666-168">必須</span><span class="sxs-lookup"><span data-stu-id="e3666-168">Required</span></span> |<span data-ttu-id="e3666-169">従業員の雇用の終了。</span><span class="sxs-lookup"><span data-stu-id="e3666-169">The end of the employee's employment.</span></span>  |
| <span data-ttu-id="e3666-170">**データ領域 ID**</span><span class="sxs-lookup"><span data-stu-id="e3666-170">**Data area ID**</span></span><br><span data-ttu-id="e3666-171">mshr_dataareaid_id</span><span class="sxs-lookup"><span data-stu-id="e3666-171">mshr_dataareaid_id</span></span><br><span data-ttu-id="e3666-172">*GUID*</span><span class="sxs-lookup"><span data-stu-id="e3666-172">*GUID*</span></span> | <span data-ttu-id="e3666-173">必須</span><span class="sxs-lookup"><span data-stu-id="e3666-173">Required</span></span> <br><span data-ttu-id="e3666-174">システム生成</span><span class="sxs-lookup"><span data-stu-id="e3666-174">System generated</span></span> | <span data-ttu-id="e3666-175">システムが生成する、法人 (会社) を識別する GUID 値です。</span><span class="sxs-lookup"><span data-stu-id="e3666-175">System-generated GUID value identifying the legal entity (company).</span></span> |
| <span data-ttu-id="e3666-176">**失効日**</span><span class="sxs-lookup"><span data-stu-id="e3666-176">**Valid to**</span></span><br><span data-ttu-id="e3666-177">mshr_namevalidto</span><span class="sxs-lookup"><span data-stu-id="e3666-177">mshr_namevalidto</span></span><br><span data-ttu-id="e3666-178">*日時オフセット*</span><span class="sxs-lookup"><span data-stu-id="e3666-178">*Date Time Offset*</span></span> |  <span data-ttu-id="e3666-179">読み取り専用</span><span class="sxs-lookup"><span data-stu-id="e3666-179">Read-only</span></span><br><span data-ttu-id="e3666-180">必須</span><span class="sxs-lookup"><span data-stu-id="e3666-180">Required</span></span> | <span data-ttu-id="e3666-181">従業員情報が有効な日付。</span><span class="sxs-lookup"><span data-stu-id="e3666-181">Date the employee information is valid to.</span></span> |
| <span data-ttu-id="e3666-182">**生年月日**</span><span class="sxs-lookup"><span data-stu-id="e3666-182">**Birth date**</span></span><br><span data-ttu-id="e3666-183">mshr_birthdate</span><span class="sxs-lookup"><span data-stu-id="e3666-183">mshr_birthdate</span></span><br><span data-ttu-id="e3666-184">*日時オフセット*</span><span class="sxs-lookup"><span data-stu-id="e3666-184">*Date Time Offset*</span></span> | <span data-ttu-id="e3666-185">読み取り専用</span><span class="sxs-lookup"><span data-stu-id="e3666-185">Read-only</span></span> <br><span data-ttu-id="e3666-186">必須</span><span class="sxs-lookup"><span data-stu-id="e3666-186">Required</span></span> | <span data-ttu-id="e3666-187">従業員の生年月日</span><span class="sxs-lookup"><span data-stu-id="e3666-187">The employee's birth date</span></span> |
| <span data-ttu-id="e3666-188">**ID 番号**</span><span class="sxs-lookup"><span data-stu-id="e3666-188">**Identification number to**</span></span><br><span data-ttu-id="e3666-189">mshr_identificationnumber</span><span class="sxs-lookup"><span data-stu-id="e3666-189">mshr_identificationnumber</span></span><br><span data-ttu-id="e3666-190">*文字列*</span><span class="sxs-lookup"><span data-stu-id="e3666-190">*String*</span></span> | <span data-ttu-id="e3666-191">読み取り専用</span><span class="sxs-lookup"><span data-stu-id="e3666-191">Read-only</span></span> <br><span data-ttu-id="e3666-192">必須</span><span class="sxs-lookup"><span data-stu-id="e3666-192">Required</span></span> |<span data-ttu-id="e3666-193">従業員に対して定義される ID 番号。</span><span class="sxs-lookup"><span data-stu-id="e3666-193">The identification number defined for the employee.</span></span>  |
| <span data-ttu-id="e3666-194">**名**</span><span class="sxs-lookup"><span data-stu-id="e3666-194">**First name**</span></span><br><span data-ttu-id="e3666-195">mshr_firstname</span><span class="sxs-lookup"><span data-stu-id="e3666-195">mshr_firstname</span></span><br><span data-ttu-id="e3666-196">*文字列*</span><span class="sxs-lookup"><span data-stu-id="e3666-196">*String*</span></span> | <span data-ttu-id="e3666-197">読み取り専用</span><span class="sxs-lookup"><span data-stu-id="e3666-197">Read-only</span></span><br><span data-ttu-id="e3666-198">必須</span><span class="sxs-lookup"><span data-stu-id="e3666-198">Required</span></span> | <span data-ttu-id="e3666-199">従業員の名。</span><span class="sxs-lookup"><span data-stu-id="e3666-199">Employee first name.</span></span> |
| <span data-ttu-id="e3666-200">**ミドル ネーム**</span><span class="sxs-lookup"><span data-stu-id="e3666-200">**Middle name**</span></span><br><span data-ttu-id="e3666-201">mshr_middlename</span><span class="sxs-lookup"><span data-stu-id="e3666-201">mshr_middlename</span></span><br><span data-ttu-id="e3666-202">*文字列*</span><span class="sxs-lookup"><span data-stu-id="e3666-202">*String*</span></span> | <span data-ttu-id="e3666-203">読み取り専用</span><span class="sxs-lookup"><span data-stu-id="e3666-203">Read-only</span></span><br><span data-ttu-id="e3666-204">必須</span><span class="sxs-lookup"><span data-stu-id="e3666-204">Required</span></span> |<span data-ttu-id="e3666-205">従業員のミドル ネーム。</span><span class="sxs-lookup"><span data-stu-id="e3666-205">Employee middle name.</span></span>  |

## <a name="example-query-for-payroll-employee"></a><span data-ttu-id="e3666-206">給与従業員のクエリの例</span><span class="sxs-lookup"><span data-stu-id="e3666-206">Example query for Payroll employee</span></span>

<span data-ttu-id="e3666-207">**申請**</span><span class="sxs-lookup"><span data-stu-id="e3666-207">**Request**</span></span>

```http
GET [Organizaton URI]/api/data/v9.1/mshr_payrollemployeeentities?$filter=mshr_personnelnumber eq @personnelnumber and mshr_identificationtypeid eq @idtype and mshr_namevalidfrom le @asofdate and mshr_namevalidto ge @asofdate&@personnelnumber='000041'&@idtype='SSN'&@asofdate=2021-04-01
```

<span data-ttu-id="e3666-208">**応答**</span><span class="sxs-lookup"><span data-stu-id="e3666-208">**Response**</span></span>

```json
{
         "mshr_legalentityid": "USMF",
            "mshr_personnelnumber": "000041",
            "mshr_employmentstartdate": "2011-04-05T07:00:00Z",
            "mshr_employmentenddate": "2154-12-31T23:59:59Z",
            "mshr_firstname": "Cassie",
            "mshr_middlename": "Lassie",
            "mshr_lastname": "Hicks",
            "mshr_namevalidfrom": "2021-03-12T20:34:25Z",
            "mshr_namevalidto": "2154-12-31T23:59:59Z",
            "mshr_birthdate": "1987-09-12T00:00:00Z",
            "mshr_gender": 200000002,
            "mshr_identificationtypeid": "SSN",
            "mshr_identificationnumber": "888-99-9342",
            "mshr_dataareaid": "USMF",
            "mshr_primaryfield": "000041 | USMF | 4/5/2011 07:00:00 am",
            "_mshr_fk_worker_id_value": "000000ad-0000-0000-d5ff-004105000000",
            "_mshr_fk_employment_id_value": "00000d0d-0000-0000-0600-014105000000",
            "_mshr_fk_fixedcompplan_id_value": "0000029f-0000-0000-d5ff-004105000000",
            "mshr_payrollemployeeentityid": "00000d3c-0000-0000-d5ff-004105000000",
            "_mshr_dataareaid_id_value": null
}
```
