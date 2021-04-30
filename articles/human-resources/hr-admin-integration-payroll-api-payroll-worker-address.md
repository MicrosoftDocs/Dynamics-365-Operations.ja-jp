---
title: 給与作業者の住所
description: このトピックでは、Dynamics 365 Human Resources における給与作業者の住所エンティティに対するクエリの詳細および例を示します。
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
ms.openlocfilehash: 6d93c38b21e953446142fc32cc2a0911616ac61d
ms.sourcegitcommit: d18d9cdb175c9d42eafbed66352c24b2aa94258b
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/13/2021
ms.locfileid: "5882022"
---
# <a name="payroll-worker-address"></a><span data-ttu-id="1e91b-103">給与作業者の住所</span><span class="sxs-lookup"><span data-stu-id="1e91b-103">Payroll worker address</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="1e91b-104">このトピックでは、Dynamics 365 Human Resources における給与作業者の住所エンティティに対するクエリの詳細および例を示します。</span><span class="sxs-lookup"><span data-stu-id="1e91b-104">This topic provides details and an example query for the Payroll worker address entity in Dynamics 365 Human Resources.</span></span>

## <a name="properties"></a><span data-ttu-id="1e91b-105">プロパティ</span><span class="sxs-lookup"><span data-stu-id="1e91b-105">Properties</span></span>

| <span data-ttu-id="1e91b-106">プロパティ</span><span class="sxs-lookup"><span data-stu-id="1e91b-106">Property</span></span><br><span data-ttu-id="1e91b-107">**現物名**</span><span class="sxs-lookup"><span data-stu-id="1e91b-107">**Physical name**</span></span><br><span data-ttu-id="1e91b-108">**_種類_**</span><span class="sxs-lookup"><span data-stu-id="1e91b-108">**_Type_**</span></span> | <span data-ttu-id="1e91b-109">使用</span><span class="sxs-lookup"><span data-stu-id="1e91b-109">Use</span></span> | <span data-ttu-id="1e91b-110">説明</span><span class="sxs-lookup"><span data-stu-id="1e91b-110">Description</span></span> |
| --- | --- | --- |
| <span data-ttu-id="1e91b-111">**市町村**</span><span class="sxs-lookup"><span data-stu-id="1e91b-111">**City**</span></span><br><span data-ttu-id="1e91b-112">mshr_city</span><span class="sxs-lookup"><span data-stu-id="1e91b-112">mshr_city</span></span><br><span data-ttu-id="1e91b-113">*文字列*</span><span class="sxs-lookup"><span data-stu-id="1e91b-113">*String*</span></span> | <span data-ttu-id="1e91b-114">読み取り専用</span><span class="sxs-lookup"><span data-stu-id="1e91b-114">Read-only</span></span><br><span data-ttu-id="1e91b-115">必須</span><span class="sxs-lookup"><span data-stu-id="1e91b-115">Required</span></span> | <span data-ttu-id="1e91b-116">住所に定義されている市町村。</span><span class="sxs-lookup"><span data-stu-id="1e91b-116">The city defined for the address.</span></span>   |
| <span data-ttu-id="1e91b-117">**個人番号**</span><span class="sxs-lookup"><span data-stu-id="1e91b-117">**Personnel number**</span></span><br><span data-ttu-id="1e91b-118">mshr_personnelnumber</span><span class="sxs-lookup"><span data-stu-id="1e91b-118">mshr_personnelnumber</span></span><br><span data-ttu-id="1e91b-119">*文字列*</span><span class="sxs-lookup"><span data-stu-id="1e91b-119">*String*</span></span> | <span data-ttu-id="1e91b-120">読み取り専用</span><span class="sxs-lookup"><span data-stu-id="1e91b-120">Read-only</span></span><br><span data-ttu-id="1e91b-121">必須</span><span class="sxs-lookup"><span data-stu-id="1e91b-121">Required</span></span> | <span data-ttu-id="1e91b-122">従業員の一意の職員番号。</span><span class="sxs-lookup"><span data-stu-id="1e91b-122">The employee's unique personnel number.</span></span>  |
| <span data-ttu-id="1e91b-123">**国地域**</span><span class="sxs-lookup"><span data-stu-id="1e91b-123">**Country region**</span></span><br><span data-ttu-id="1e91b-124">mshr_countryregionid</span><span class="sxs-lookup"><span data-stu-id="1e91b-124">mshr_countryregionid</span></span><br><span data-ttu-id="1e91b-125">*文字列*</span><span class="sxs-lookup"><span data-stu-id="1e91b-125">*String*</span></span> | <span data-ttu-id="1e91b-126">読み取り専用</span><span class="sxs-lookup"><span data-stu-id="1e91b-126">Read-only</span></span><br><span data-ttu-id="1e91b-127">必須</span><span class="sxs-lookup"><span data-stu-id="1e91b-127">Required</span></span> | <span data-ttu-id="1e91b-128">住所に定義されている国の地域</span><span class="sxs-lookup"><span data-stu-id="1e91b-128">The country region defined for the address</span></span>  |
| <span data-ttu-id="1e91b-129">**発効日**</span><span class="sxs-lookup"><span data-stu-id="1e91b-129">**Valid from**</span></span><br><span data-ttu-id="1e91b-130">mshr_postaladdressvalidfrom</span><span class="sxs-lookup"><span data-stu-id="1e91b-130">mshr_postaladdressvalidfrom</span></span><br><span data-ttu-id="1e91b-131">*日時オフセット*</span><span class="sxs-lookup"><span data-stu-id="1e91b-131">*Date Time Offset*</span></span> | <span data-ttu-id="1e91b-132">読み取り専用</span><span class="sxs-lookup"><span data-stu-id="1e91b-132">Read-only</span></span> <br><span data-ttu-id="1e91b-133">必須</span><span class="sxs-lookup"><span data-stu-id="1e91b-133">Required</span></span> | <span data-ttu-id="1e91b-134">住所が有効な日付。</span><span class="sxs-lookup"><span data-stu-id="1e91b-134">The date the address is valid from.</span></span> |
| <span data-ttu-id="1e91b-135">**住所で作業**</span><span class="sxs-lookup"><span data-stu-id="1e91b-135">**Worked in address**</span></span><br><span data-ttu-id="1e91b-136">mshr_isworkedinaddressbr>*Int32*</span><span class="sxs-lookup"><span data-stu-id="1e91b-136">mshr_isworkedinaddressbr>*Int32*</span></span> | <span data-ttu-id="1e91b-137">読み取り専用</span><span class="sxs-lookup"><span data-stu-id="1e91b-137">Read-only</span></span><br><span data-ttu-id="1e91b-138">必須</span><span class="sxs-lookup"><span data-stu-id="1e91b-138">Required</span></span> | <span data-ttu-id="1e91b-139">住所が従業員の勤務地であるかどうかを表します。</span><span class="sxs-lookup"><span data-stu-id="1e91b-139">Denotes if the address is where the employee works.</span></span> |
| <span data-ttu-id="1e91b-140">**郡**</span><span class="sxs-lookup"><span data-stu-id="1e91b-140">**County**</span></span><br><span data-ttu-id="1e91b-141">mshr_county</span><span class="sxs-lookup"><span data-stu-id="1e91b-141">mshr_county</span></span><br><span data-ttu-id="1e91b-142">*文字列*</span><span class="sxs-lookup"><span data-stu-id="1e91b-142">*String*</span></span> | <span data-ttu-id="1e91b-143">読み取り専用</span><span class="sxs-lookup"><span data-stu-id="1e91b-143">Read-only</span></span><br><span data-ttu-id="1e91b-144">必須</span><span class="sxs-lookup"><span data-stu-id="1e91b-144">Required</span></span> | <span data-ttu-id="1e91b-145">住所に定義されている国。</span><span class="sxs-lookup"><span data-stu-id="1e91b-145">The county defined for the address.</span></span>  |
| <span data-ttu-id="1e91b-146">**給与作業者の住所 ID**</span><span class="sxs-lookup"><span data-stu-id="1e91b-146">**Payroll worker address ID**</span></span><br><span data-ttu-id="1e91b-147">mshr_payrollworkeraddressentityid</span><span class="sxs-lookup"><span data-stu-id="1e91b-147">mshr_payrollworkeraddressentityid</span></span><br><span data-ttu-id="1e91b-148">*GUID*</span><span class="sxs-lookup"><span data-stu-id="1e91b-148">*GUID*</span></span> | <span data-ttu-id="1e91b-149">必須</span><span class="sxs-lookup"><span data-stu-id="1e91b-149">Required</span></span><br><span data-ttu-id="1e91b-150">システム生成</span><span class="sxs-lookup"><span data-stu-id="1e91b-150">System generated</span></span> | <span data-ttu-id="1e91b-151">住所を一意に識別するためのシステム生成の GUID 値。</span><span class="sxs-lookup"><span data-stu-id="1e91b-151">A system-generated GUID value to uniquely identify the address.</span></span>  |
| <span data-ttu-id="1e91b-152">**基本フィールド**</span><span class="sxs-lookup"><span data-stu-id="1e91b-152">**Primary field**</span></span><br><span data-ttu-id="1e91b-153">mshr_primaryfield</span><span class="sxs-lookup"><span data-stu-id="1e91b-153">mshr_primaryfield</span></span><br><span data-ttu-id="1e91b-154">*文字列*</span><span class="sxs-lookup"><span data-stu-id="1e91b-154">*String*</span></span> | <span data-ttu-id="1e91b-155">読み取り専用</span><span class="sxs-lookup"><span data-stu-id="1e91b-155">Read-only</span></span><br><span data-ttu-id="1e91b-156">必須</span><span class="sxs-lookup"><span data-stu-id="1e91b-156">Required</span></span> |  |
| <span data-ttu-id="1e91b-157">**住所**</span><span class="sxs-lookup"><span data-stu-id="1e91b-157">**Street**</span></span><br><span data-ttu-id="1e91b-158">mshr_street</span><span class="sxs-lookup"><span data-stu-id="1e91b-158">mshr_street</span></span><br><span data-ttu-id="1e91b-159">*文字列*</span><span class="sxs-lookup"><span data-stu-id="1e91b-159">*String*</span></span> | <span data-ttu-id="1e91b-160">読み取り専用</span><span class="sxs-lookup"><span data-stu-id="1e91b-160">Read-only</span></span><br><span data-ttu-id="1e91b-161">必須</span><span class="sxs-lookup"><span data-stu-id="1e91b-161">Required</span></span> | <span data-ttu-id="1e91b-162">住所に定義されている番地。</span><span class="sxs-lookup"><span data-stu-id="1e91b-162">The street defined for the address.</span></span> |
| <span data-ttu-id="1e91b-163">**失効日**</span><span class="sxs-lookup"><span data-stu-id="1e91b-163">**Valid to**</span></span><br><span data-ttu-id="1e91b-164">mshr_postaladdressvalidto</span><span class="sxs-lookup"><span data-stu-id="1e91b-164">mshr_postaladdressvalidto</span></span><br><span data-ttu-id="1e91b-165">*日時オフセット*</span><span class="sxs-lookup"><span data-stu-id="1e91b-165">*Date Time Offset*</span></span> | <span data-ttu-id="1e91b-166">読み取り専用</span><span class="sxs-lookup"><span data-stu-id="1e91b-166">Read-only</span></span> <br><span data-ttu-id="1e91b-167">必須</span><span class="sxs-lookup"><span data-stu-id="1e91b-167">Required</span></span> | <span data-ttu-id="1e91b-168">住所が有効な日付。</span><span class="sxs-lookup"><span data-stu-id="1e91b-168">The date the address is valid to.</span></span>  |
| <span data-ttu-id="1e91b-169">**場所 ID**</span><span class="sxs-lookup"><span data-stu-id="1e91b-169">**Location ID**</span></span><br><span data-ttu-id="1e91b-170">mshr_locationidbr>*文字列*</span><span class="sxs-lookup"><span data-stu-id="1e91b-170">mshr_locationidbr>*String*</span></span> | <span data-ttu-id="1e91b-171">読み取り専用</span><span class="sxs-lookup"><span data-stu-id="1e91b-171">Read-only</span></span> <br><span data-ttu-id="1e91b-172">必須</span><span class="sxs-lookup"><span data-stu-id="1e91b-172">Required</span></span> | <span data-ttu-id="1e91b-173">住所の ID。</span><span class="sxs-lookup"><span data-stu-id="1e91b-173">The ID for the address.</span></span>  |
| <span data-ttu-id="1e91b-174">**郵便番号**</span><span class="sxs-lookup"><span data-stu-id="1e91b-174">**Postal code**</span></span><br><span data-ttu-id="1e91b-175">mshr_zipcode</span><span class="sxs-lookup"><span data-stu-id="1e91b-175">mshr_zipcode</span></span><br><span data-ttu-id="1e91b-176">*文字列*</span><span class="sxs-lookup"><span data-stu-id="1e91b-176">*String*</span></span> | <span data-ttu-id="1e91b-177">読み取り専用</span><span class="sxs-lookup"><span data-stu-id="1e91b-177">Read-only</span></span> <br><span data-ttu-id="1e91b-178">必須</span><span class="sxs-lookup"><span data-stu-id="1e91b-178">Required</span></span> |<span data-ttu-id="1e91b-179">従業員に対して定義される ID 番号。</span><span class="sxs-lookup"><span data-stu-id="1e91b-179">The identification number defined for the employee.</span></span>  |
| <span data-ttu-id="1e91b-180">**住所に住んでいた**</span><span class="sxs-lookup"><span data-stu-id="1e91b-180">**Lived in address**</span></span><br><span data-ttu-id="1e91b-181">mshr_islivedinaddressbr>*文字列*</span><span class="sxs-lookup"><span data-stu-id="1e91b-181">mshr_islivedinaddressbr>*String*</span></span> | <span data-ttu-id="1e91b-182">読み取り専用</span><span class="sxs-lookup"><span data-stu-id="1e91b-182">Read-only</span></span><br><span data-ttu-id="1e91b-183">必須</span><span class="sxs-lookup"><span data-stu-id="1e91b-183">Required</span></span> | <span data-ttu-id="1e91b-184">住所が従業員の居住地であるかどうかを表します。</span><span class="sxs-lookup"><span data-stu-id="1e91b-184">Denotes if the address is where the employee lives.</span></span> |
| <span data-ttu-id="1e91b-185">**行政単位 (区画)**</span><span class="sxs-lookup"><span data-stu-id="1e91b-185">**State**</span></span><br><span data-ttu-id="1e91b-186">mshr_state</span><span class="sxs-lookup"><span data-stu-id="1e91b-186">mshr_state</span></span><br><span data-ttu-id="1e91b-187">*文字列*</span><span class="sxs-lookup"><span data-stu-id="1e91b-187">*String*</span></span> | <span data-ttu-id="1e91b-188">読み取り専用</span><span class="sxs-lookup"><span data-stu-id="1e91b-188">Read-only</span></span><br><span data-ttu-id="1e91b-189">必須</span><span class="sxs-lookup"><span data-stu-id="1e91b-189">Required</span></span> | <span data-ttu-id="1e91b-190">住所に定義されている状態。</span><span class="sxs-lookup"><span data-stu-id="1e91b-190">The state defined for the address.</span></span>  |

## <a name="example-query"></a><span data-ttu-id="1e91b-191">クエリの例</span><span class="sxs-lookup"><span data-stu-id="1e91b-191">Example query</span></span>

<span data-ttu-id="1e91b-192">**申請**</span><span class="sxs-lookup"><span data-stu-id="1e91b-192">**Request**</span></span>

```http
GET [Organizaton URI]/api/data/v9.1/mshr_payrollworkeraddressentities?$filter=mshr_personnelnumber eq @personnelnumber and mshr_postaladdressvalidfrom le @asofdate and mshr_postaladdressvalidto ge @asofdate&@personnelnumber='000041'&@asofdate=2021-04-01
```

<span data-ttu-id="1e91b-193">**応答**</span><span class="sxs-lookup"><span data-stu-id="1e91b-193">**Response**</span></span>

```json
{
            "mshr_personnelnumber": "000041",
            "mshr_locationid": "000000538",
            "mshr_islivedinaddress": 200000001,
            "mshr_isworkedinaddress": 200000000,
            "mshr_countryregionid": "USA",
            "mshr_zipcode": "99025",
            "mshr_street": "6543 Cypress Ave",
            "mshr_city": "Tacoma",
            "mshr_state": "WA",
            "mshr_county": "KING",
            "mshr_postaladdressvalidfrom": "2012-09-20T20:14:27Z",
            "mshr_postaladdressvalidto": "2154-12-31T23:59:59Z",
            "mshr_primaryfield": "000041 | 000000538 | 9/20/2012 08:14:27 pm",
            "_mshr_fk_worker_id_value": "00000d3c-0000-0000-d5ff-004105000000",
            "mshr_payrollworkeraddressentityid": "000006f0-0000-0000-f90f-014105000000"

}
```
