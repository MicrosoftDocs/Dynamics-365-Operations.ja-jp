---
title: 給与作業者の住所
description: このトピックでは、Dynamics 365 Human Resources における給与作業者の住所エンティティに対するクエリの詳細および例を示します。
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
ms.openlocfilehash: 964f04261ea95ee6fa2880b0905a669855f6c58a
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/11/2021
ms.locfileid: "6020708"
---
# <a name="payroll-worker-address"></a><span data-ttu-id="df4c2-103">給与作業者の住所</span><span class="sxs-lookup"><span data-stu-id="df4c2-103">Payroll worker address</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="df4c2-104">このトピックでは、Dynamics 365 Human Resources における給与作業者の住所エンティティに対するクエリの詳細および例を示します。</span><span class="sxs-lookup"><span data-stu-id="df4c2-104">This topic provides details and an example query for the Payroll worker address entity in Dynamics 365 Human Resources.</span></span>

## <a name="properties"></a><span data-ttu-id="df4c2-105">プロパティ</span><span class="sxs-lookup"><span data-stu-id="df4c2-105">Properties</span></span>

| <span data-ttu-id="df4c2-106">プロパティ</span><span class="sxs-lookup"><span data-stu-id="df4c2-106">Property</span></span><br><span data-ttu-id="df4c2-107">**現物名**</span><span class="sxs-lookup"><span data-stu-id="df4c2-107">**Physical name**</span></span><br><span data-ttu-id="df4c2-108">**_種類_**</span><span class="sxs-lookup"><span data-stu-id="df4c2-108">**_Type_**</span></span> | <span data-ttu-id="df4c2-109">使用</span><span class="sxs-lookup"><span data-stu-id="df4c2-109">Use</span></span> | <span data-ttu-id="df4c2-110">説明</span><span class="sxs-lookup"><span data-stu-id="df4c2-110">Description</span></span> |
| --- | --- | --- |
| <span data-ttu-id="df4c2-111">**市町村**</span><span class="sxs-lookup"><span data-stu-id="df4c2-111">**City**</span></span><br><span data-ttu-id="df4c2-112">mshr_city</span><span class="sxs-lookup"><span data-stu-id="df4c2-112">mshr_city</span></span><br><span data-ttu-id="df4c2-113">*文字列*</span><span class="sxs-lookup"><span data-stu-id="df4c2-113">*String*</span></span> | <span data-ttu-id="df4c2-114">読み取り専用</span><span class="sxs-lookup"><span data-stu-id="df4c2-114">Read-only</span></span><br><span data-ttu-id="df4c2-115">必須</span><span class="sxs-lookup"><span data-stu-id="df4c2-115">Required</span></span> | <span data-ttu-id="df4c2-116">住所に定義されている市町村。</span><span class="sxs-lookup"><span data-stu-id="df4c2-116">The city defined for the address.</span></span>   |
| <span data-ttu-id="df4c2-117">**個人番号**</span><span class="sxs-lookup"><span data-stu-id="df4c2-117">**Personnel number**</span></span><br><span data-ttu-id="df4c2-118">mshr_personnelnumber</span><span class="sxs-lookup"><span data-stu-id="df4c2-118">mshr_personnelnumber</span></span><br><span data-ttu-id="df4c2-119">*文字列*</span><span class="sxs-lookup"><span data-stu-id="df4c2-119">*String*</span></span> | <span data-ttu-id="df4c2-120">読み取り専用</span><span class="sxs-lookup"><span data-stu-id="df4c2-120">Read-only</span></span><br><span data-ttu-id="df4c2-121">必須</span><span class="sxs-lookup"><span data-stu-id="df4c2-121">Required</span></span> | <span data-ttu-id="df4c2-122">従業員の一意の職員番号。</span><span class="sxs-lookup"><span data-stu-id="df4c2-122">The employee's unique personnel number.</span></span>  |
| <span data-ttu-id="df4c2-123">**国地域**</span><span class="sxs-lookup"><span data-stu-id="df4c2-123">**Country region**</span></span><br><span data-ttu-id="df4c2-124">mshr_countryregionid</span><span class="sxs-lookup"><span data-stu-id="df4c2-124">mshr_countryregionid</span></span><br><span data-ttu-id="df4c2-125">*文字列*</span><span class="sxs-lookup"><span data-stu-id="df4c2-125">*String*</span></span> | <span data-ttu-id="df4c2-126">読み取り専用</span><span class="sxs-lookup"><span data-stu-id="df4c2-126">Read-only</span></span><br><span data-ttu-id="df4c2-127">必須</span><span class="sxs-lookup"><span data-stu-id="df4c2-127">Required</span></span> | <span data-ttu-id="df4c2-128">住所に定義されている国の地域</span><span class="sxs-lookup"><span data-stu-id="df4c2-128">The country region defined for the address</span></span>  |
| <span data-ttu-id="df4c2-129">**発効日**</span><span class="sxs-lookup"><span data-stu-id="df4c2-129">**Valid from**</span></span><br><span data-ttu-id="df4c2-130">mshr_postaladdressvalidfrom</span><span class="sxs-lookup"><span data-stu-id="df4c2-130">mshr_postaladdressvalidfrom</span></span><br><span data-ttu-id="df4c2-131">*日時オフセット*</span><span class="sxs-lookup"><span data-stu-id="df4c2-131">*Date Time Offset*</span></span> | <span data-ttu-id="df4c2-132">読み取り専用</span><span class="sxs-lookup"><span data-stu-id="df4c2-132">Read-only</span></span> <br><span data-ttu-id="df4c2-133">必須</span><span class="sxs-lookup"><span data-stu-id="df4c2-133">Required</span></span> | <span data-ttu-id="df4c2-134">住所が有効な日付。</span><span class="sxs-lookup"><span data-stu-id="df4c2-134">The date the address is valid from.</span></span> |
| <span data-ttu-id="df4c2-135">**住所で作業**</span><span class="sxs-lookup"><span data-stu-id="df4c2-135">**Worked in address**</span></span><br><span data-ttu-id="df4c2-136">mshr_isworkedinaddressbr>*Int32*</span><span class="sxs-lookup"><span data-stu-id="df4c2-136">mshr_isworkedinaddressbr>*Int32*</span></span> | <span data-ttu-id="df4c2-137">読み取り専用</span><span class="sxs-lookup"><span data-stu-id="df4c2-137">Read-only</span></span><br><span data-ttu-id="df4c2-138">必須</span><span class="sxs-lookup"><span data-stu-id="df4c2-138">Required</span></span> | <span data-ttu-id="df4c2-139">住所が従業員の勤務地であるかどうかを表します。</span><span class="sxs-lookup"><span data-stu-id="df4c2-139">Denotes if the address is where the employee works.</span></span> |
| <span data-ttu-id="df4c2-140">**郡**</span><span class="sxs-lookup"><span data-stu-id="df4c2-140">**County**</span></span><br><span data-ttu-id="df4c2-141">mshr_county</span><span class="sxs-lookup"><span data-stu-id="df4c2-141">mshr_county</span></span><br><span data-ttu-id="df4c2-142">*文字列*</span><span class="sxs-lookup"><span data-stu-id="df4c2-142">*String*</span></span> | <span data-ttu-id="df4c2-143">読み取り専用</span><span class="sxs-lookup"><span data-stu-id="df4c2-143">Read-only</span></span><br><span data-ttu-id="df4c2-144">必須</span><span class="sxs-lookup"><span data-stu-id="df4c2-144">Required</span></span> | <span data-ttu-id="df4c2-145">住所に定義されている国。</span><span class="sxs-lookup"><span data-stu-id="df4c2-145">The county defined for the address.</span></span>  |
| <span data-ttu-id="df4c2-146">**給与作業者の住所 ID**</span><span class="sxs-lookup"><span data-stu-id="df4c2-146">**Payroll worker address ID**</span></span><br><span data-ttu-id="df4c2-147">mshr_payrollworkeraddressentityid</span><span class="sxs-lookup"><span data-stu-id="df4c2-147">mshr_payrollworkeraddressentityid</span></span><br><span data-ttu-id="df4c2-148">*GUID*</span><span class="sxs-lookup"><span data-stu-id="df4c2-148">*GUID*</span></span> | <span data-ttu-id="df4c2-149">必須</span><span class="sxs-lookup"><span data-stu-id="df4c2-149">Required</span></span><br><span data-ttu-id="df4c2-150">システム生成</span><span class="sxs-lookup"><span data-stu-id="df4c2-150">System generated</span></span> | <span data-ttu-id="df4c2-151">住所を一意に識別するためのシステム生成の GUID 値。</span><span class="sxs-lookup"><span data-stu-id="df4c2-151">A system-generated GUID value to uniquely identify the address.</span></span>  |
| <span data-ttu-id="df4c2-152">**基本フィールド**</span><span class="sxs-lookup"><span data-stu-id="df4c2-152">**Primary field**</span></span><br><span data-ttu-id="df4c2-153">mshr_primaryfield</span><span class="sxs-lookup"><span data-stu-id="df4c2-153">mshr_primaryfield</span></span><br><span data-ttu-id="df4c2-154">*文字列*</span><span class="sxs-lookup"><span data-stu-id="df4c2-154">*String*</span></span> | <span data-ttu-id="df4c2-155">読み取り専用</span><span class="sxs-lookup"><span data-stu-id="df4c2-155">Read-only</span></span><br><span data-ttu-id="df4c2-156">必須</span><span class="sxs-lookup"><span data-stu-id="df4c2-156">Required</span></span> |  |
| <span data-ttu-id="df4c2-157">**住所**</span><span class="sxs-lookup"><span data-stu-id="df4c2-157">**Street**</span></span><br><span data-ttu-id="df4c2-158">mshr_street</span><span class="sxs-lookup"><span data-stu-id="df4c2-158">mshr_street</span></span><br><span data-ttu-id="df4c2-159">*文字列*</span><span class="sxs-lookup"><span data-stu-id="df4c2-159">*String*</span></span> | <span data-ttu-id="df4c2-160">読み取り専用</span><span class="sxs-lookup"><span data-stu-id="df4c2-160">Read-only</span></span><br><span data-ttu-id="df4c2-161">必須</span><span class="sxs-lookup"><span data-stu-id="df4c2-161">Required</span></span> | <span data-ttu-id="df4c2-162">住所に定義されている番地。</span><span class="sxs-lookup"><span data-stu-id="df4c2-162">The street defined for the address.</span></span> |
| <span data-ttu-id="df4c2-163">**失効日**</span><span class="sxs-lookup"><span data-stu-id="df4c2-163">**Valid to**</span></span><br><span data-ttu-id="df4c2-164">mshr_postaladdressvalidto</span><span class="sxs-lookup"><span data-stu-id="df4c2-164">mshr_postaladdressvalidto</span></span><br><span data-ttu-id="df4c2-165">*日時オフセット*</span><span class="sxs-lookup"><span data-stu-id="df4c2-165">*Date Time Offset*</span></span> | <span data-ttu-id="df4c2-166">読み取り専用</span><span class="sxs-lookup"><span data-stu-id="df4c2-166">Read-only</span></span> <br><span data-ttu-id="df4c2-167">必須</span><span class="sxs-lookup"><span data-stu-id="df4c2-167">Required</span></span> | <span data-ttu-id="df4c2-168">住所が有効な日付。</span><span class="sxs-lookup"><span data-stu-id="df4c2-168">The date the address is valid to.</span></span>  |
| <span data-ttu-id="df4c2-169">**場所 ID**</span><span class="sxs-lookup"><span data-stu-id="df4c2-169">**Location ID**</span></span><br><span data-ttu-id="df4c2-170">mshr_locationidbr>*文字列*</span><span class="sxs-lookup"><span data-stu-id="df4c2-170">mshr_locationidbr>*String*</span></span> | <span data-ttu-id="df4c2-171">読み取り専用</span><span class="sxs-lookup"><span data-stu-id="df4c2-171">Read-only</span></span> <br><span data-ttu-id="df4c2-172">必須</span><span class="sxs-lookup"><span data-stu-id="df4c2-172">Required</span></span> | <span data-ttu-id="df4c2-173">住所の ID。</span><span class="sxs-lookup"><span data-stu-id="df4c2-173">The ID for the address.</span></span>  |
| <span data-ttu-id="df4c2-174">**郵便番号**</span><span class="sxs-lookup"><span data-stu-id="df4c2-174">**Postal code**</span></span><br><span data-ttu-id="df4c2-175">mshr_zipcode</span><span class="sxs-lookup"><span data-stu-id="df4c2-175">mshr_zipcode</span></span><br><span data-ttu-id="df4c2-176">*文字列*</span><span class="sxs-lookup"><span data-stu-id="df4c2-176">*String*</span></span> | <span data-ttu-id="df4c2-177">読み取り専用</span><span class="sxs-lookup"><span data-stu-id="df4c2-177">Read-only</span></span> <br><span data-ttu-id="df4c2-178">必須</span><span class="sxs-lookup"><span data-stu-id="df4c2-178">Required</span></span> |<span data-ttu-id="df4c2-179">従業員に対して定義される ID 番号。</span><span class="sxs-lookup"><span data-stu-id="df4c2-179">The identification number defined for the employee.</span></span>  |
| <span data-ttu-id="df4c2-180">**住所に住んでいた**</span><span class="sxs-lookup"><span data-stu-id="df4c2-180">**Lived in address**</span></span><br><span data-ttu-id="df4c2-181">mshr_islivedinaddressbr>*文字列*</span><span class="sxs-lookup"><span data-stu-id="df4c2-181">mshr_islivedinaddressbr>*String*</span></span> | <span data-ttu-id="df4c2-182">読み取り専用</span><span class="sxs-lookup"><span data-stu-id="df4c2-182">Read-only</span></span><br><span data-ttu-id="df4c2-183">必須</span><span class="sxs-lookup"><span data-stu-id="df4c2-183">Required</span></span> | <span data-ttu-id="df4c2-184">住所が従業員の居住地であるかどうかを表します。</span><span class="sxs-lookup"><span data-stu-id="df4c2-184">Denotes if the address is where the employee lives.</span></span> |
| <span data-ttu-id="df4c2-185">**行政単位 (区画)**</span><span class="sxs-lookup"><span data-stu-id="df4c2-185">**State**</span></span><br><span data-ttu-id="df4c2-186">mshr_state</span><span class="sxs-lookup"><span data-stu-id="df4c2-186">mshr_state</span></span><br><span data-ttu-id="df4c2-187">*文字列*</span><span class="sxs-lookup"><span data-stu-id="df4c2-187">*String*</span></span> | <span data-ttu-id="df4c2-188">読み取り専用</span><span class="sxs-lookup"><span data-stu-id="df4c2-188">Read-only</span></span><br><span data-ttu-id="df4c2-189">必須</span><span class="sxs-lookup"><span data-stu-id="df4c2-189">Required</span></span> | <span data-ttu-id="df4c2-190">住所に定義されている状態。</span><span class="sxs-lookup"><span data-stu-id="df4c2-190">The state defined for the address.</span></span>  |

## <a name="example-query"></a><span data-ttu-id="df4c2-191">クエリの例</span><span class="sxs-lookup"><span data-stu-id="df4c2-191">Example query</span></span>

<span data-ttu-id="df4c2-192">**申請**</span><span class="sxs-lookup"><span data-stu-id="df4c2-192">**Request**</span></span>

```http
GET [Organizaton URI]/api/data/v9.1/mshr_payrollworkeraddressentities?$filter=mshr_personnelnumber eq @personnelnumber and mshr_postaladdressvalidfrom le @asofdate and mshr_postaladdressvalidto ge @asofdate&@personnelnumber='000041'&@asofdate=2021-04-01
```

<span data-ttu-id="df4c2-193">**応答**</span><span class="sxs-lookup"><span data-stu-id="df4c2-193">**Response**</span></span>

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
