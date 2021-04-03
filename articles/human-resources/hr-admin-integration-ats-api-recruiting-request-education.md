---
title: 採用で要求する教育
description: このトピックでは、Dynamics 365 Human Resources の人物の要求する教育エンティティについて説明します。
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
ms.openlocfilehash: efc5c4813f8abd869e8137052c4aeb356a930d0b
ms.sourcegitcommit: 6affb3316be757c99e1fe9c7c7b312b93c483408
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/17/2021
ms.locfileid: "5465969"
---
# <a name="recruiting-request-education"></a><span data-ttu-id="9ed2d-103">採用で要求する教育</span><span class="sxs-lookup"><span data-stu-id="9ed2d-103">Recruiting request education</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="9ed2d-104">このトピックでは、Dynamics 365 Human Resources の人物の要求する教育エンティティについて説明します。</span><span class="sxs-lookup"><span data-stu-id="9ed2d-104">This topic describes the Recruiting request education entity for Dynamics 365 Human Resources.</span></span>

<span data-ttu-id="9ed2d-105">物理名 : mshr_hcmrecruitingrequesteducationentity</span><span class="sxs-lookup"><span data-stu-id="9ed2d-105">Physical name: mshr_hcmrecruitingrequesteducationentity</span></span>

### <a name="description"></a><span data-ttu-id="9ed2d-106">説明</span><span class="sxs-lookup"><span data-stu-id="9ed2d-106">Description</span></span>

<span data-ttu-id="9ed2d-107">RecruitingRequest の教育要件について説明します。</span><span class="sxs-lookup"><span data-stu-id="9ed2d-107">Describes educational requirements for a RecruitingRequest.</span></span>

### <a name="json-representation"></a><span data-ttu-id="9ed2d-108">JSON 表記</span><span class="sxs-lookup"><span data-stu-id="9ed2d-108">JSON representation</span></span>

```json
{
    "mshr_recruitingrequestid": "String",
    "mshr_educationdisciplineid": "String",
    "mshr_educationdisciplinedescription": "String",
    "mshr_educationlevelid": "String",
    "mshr_educationleveldescription": "String",
    "mshr_dataareaid": "String",
    "_mshr_dataareaid_id_value": "Guid",
    "mshr_primaryfield": "String",
    "_mshr_fk_recruitingrequest_id_value": "Guid",
    "_mshr_fk_educationdiscipline_id_value": "Guid",
    "_mshr_fk_educationlevel_id_value": "Guid",
    "mshr_hcmrecruitingrequesteducationentityid": "Guid"
}
```

### <a name="properties"></a><span data-ttu-id="9ed2d-109">プロパティ</span><span class="sxs-lookup"><span data-stu-id="9ed2d-109">Properties</span></span>

| <span data-ttu-id="9ed2d-110">プロパティ</span><span class="sxs-lookup"><span data-stu-id="9ed2d-110">Property</span></span><br><span data-ttu-id="9ed2d-111">**現物名**</span><span class="sxs-lookup"><span data-stu-id="9ed2d-111">**Physical name**</span></span><br><span data-ttu-id="9ed2d-112">**_種類_**</span><span class="sxs-lookup"><span data-stu-id="9ed2d-112">**_Type_**</span></span> | <span data-ttu-id="9ed2d-113">使用</span><span class="sxs-lookup"><span data-stu-id="9ed2d-113">Use</span></span> | <span data-ttu-id="9ed2d-114">説明</span><span class="sxs-lookup"><span data-stu-id="9ed2d-114">Description</span></span> |
| --- | --- | --- |
| <span data-ttu-id="9ed2d-115">**採用で要求する教育エンティティ ID**</span><span class="sxs-lookup"><span data-stu-id="9ed2d-115">**Recruiting Request Education Entity ID**</span></span><br><span data-ttu-id="9ed2d-116">mshr_hcmrecruitingrequesteducationentityid</span><span class="sxs-lookup"><span data-stu-id="9ed2d-116">mshr_hcmrecruitingrequesteducationentityid</span></span><br><span data-ttu-id="9ed2d-117">*GUID*</span><span class="sxs-lookup"><span data-stu-id="9ed2d-117">*GUID*</span></span> | <span data-ttu-id="9ed2d-118">読み取り専用</span><span class="sxs-lookup"><span data-stu-id="9ed2d-118">Read-only</span></span><br><span data-ttu-id="9ed2d-119">必須</span><span class="sxs-lookup"><span data-stu-id="9ed2d-119">Required</span></span> | <span data-ttu-id="9ed2d-120">システムが生成した、採用で要求する教育レコードの一意識別子です。</span><span class="sxs-lookup"><span data-stu-id="9ed2d-120">System-generated unique identifier for the Recruiting Request Education record.</span></span> |
| <span data-ttu-id="9ed2d-121">**採用要求 ID**</span><span class="sxs-lookup"><span data-stu-id="9ed2d-121">**Recruiting Request ID**</span></span><br><span data-ttu-id="9ed2d-122">mshr_recruitingrequestid</span><span class="sxs-lookup"><span data-stu-id="9ed2d-122">mshr_recruitingrequestid</span></span><br><span data-ttu-id="9ed2d-123">*文字列*</span><span class="sxs-lookup"><span data-stu-id="9ed2d-123">*String*</span></span> | <span data-ttu-id="9ed2d-124">1回書き込み</span><span class="sxs-lookup"><span data-stu-id="9ed2d-124">Write-once</span></span><br><span data-ttu-id="9ed2d-125">必須</span><span class="sxs-lookup"><span data-stu-id="9ed2d-125">Required</span></span> | <span data-ttu-id="9ed2d-126">読み取り可能な、関連する採用要求の一意識別子です。</span><span class="sxs-lookup"><span data-stu-id="9ed2d-126">The user-readable unique identifier of the related recruiting request.</span></span> |
| <span data-ttu-id="9ed2d-127">**採用要求 ID 値**</span><span class="sxs-lookup"><span data-stu-id="9ed2d-127">**Recruiting Request ID Value**</span></span><br><span data-ttu-id="9ed2d-128">_mshr_fk_recruitingrequest_id_value</span><span class="sxs-lookup"><span data-stu-id="9ed2d-128">_mshr_fk_recruitingrequest_id_value</span></span><br><span data-ttu-id="9ed2d-129">*GUID*</span><span class="sxs-lookup"><span data-stu-id="9ed2d-129">*GUID*</span></span> | <span data-ttu-id="9ed2d-130">読み取り専用</span><span class="sxs-lookup"><span data-stu-id="9ed2d-130">Read-only</span></span><br><span data-ttu-id="9ed2d-131">必須</span><span class="sxs-lookup"><span data-stu-id="9ed2d-131">Required</span></span><br><span data-ttu-id="9ed2d-132">外部キー : mshr_hcmrecruitingrequestentity の mshr_hcmrecruitingrequestentityid</span><span class="sxs-lookup"><span data-stu-id="9ed2d-132">Foreign key: mshr_hcmrecruitingrequestentityid of mshr_hcmrecruitingrequestentity</span></span> | <span data-ttu-id="9ed2d-133">システムが生成する、関連する採用要求の一意識別子です。</span><span class="sxs-lookup"><span data-stu-id="9ed2d-133">System-generated unique identifier of the related recruiting request.</span></span> |
| <span data-ttu-id="9ed2d-134">**教育レベル ID**</span><span class="sxs-lookup"><span data-stu-id="9ed2d-134">**Education Level ID**</span></span><br><span data-ttu-id="9ed2d-135">mshr_educationlevelid</span><span class="sxs-lookup"><span data-stu-id="9ed2d-135">mshr_educationlevelid</span></span><br><span data-ttu-id="9ed2d-136">*文字列*</span><span class="sxs-lookup"><span data-stu-id="9ed2d-136">*String*</span></span> | <span data-ttu-id="9ed2d-137">1回書き込み</span><span class="sxs-lookup"><span data-stu-id="9ed2d-137">Write-once</span></span><br><span data-ttu-id="9ed2d-138">必須</span><span class="sxs-lookup"><span data-stu-id="9ed2d-138">Required</span></span> | <span data-ttu-id="9ed2d-139">要求される教育のレベルです。</span><span class="sxs-lookup"><span data-stu-id="9ed2d-139">The level of education required.</span></span> |
| <span data-ttu-id="9ed2d-140">**教育レベル ID 値**</span><span class="sxs-lookup"><span data-stu-id="9ed2d-140">**Educational Level ID Value**</span></span><br><span data-ttu-id="9ed2d-141">_mshr_fk_educationlevel_id_value</span><span class="sxs-lookup"><span data-stu-id="9ed2d-141">_mshr_fk_educationlevel_id_value</span></span><br><span data-ttu-id="9ed2d-142">*GUID*</span><span class="sxs-lookup"><span data-stu-id="9ed2d-142">*GUID*</span></span> | <span data-ttu-id="9ed2d-143">読み取り専用</span><span class="sxs-lookup"><span data-stu-id="9ed2d-143">Read-only</span></span><br><span data-ttu-id="9ed2d-144">必須</span><span class="sxs-lookup"><span data-stu-id="9ed2d-144">Required</span></span><br><span data-ttu-id="9ed2d-145">外部キー : mshr_hcmeducationlevelentity の mshr_hcmeducationlevelentityid</span><span class="sxs-lookup"><span data-stu-id="9ed2d-145">Foreign key: mshr_hcmeducationlevelentityid of mshr_hcmeducationlevelentity</span></span> | <span data-ttu-id="9ed2d-146">システムが生成した、要求される教育のレベルの一意識別子です。</span><span class="sxs-lookup"><span data-stu-id="9ed2d-146">System-generated unique identifier of the level of education required.</span></span> |
| <span data-ttu-id="9ed2d-147">**教育レベルの説明**</span><span class="sxs-lookup"><span data-stu-id="9ed2d-147">**Education Level Description**</span></span><br><span data-ttu-id="9ed2d-148">mshr_educationleveldescription</span><span class="sxs-lookup"><span data-stu-id="9ed2d-148">mshr_educationleveldescription</span></span><br><span data-ttu-id="9ed2d-149">*文字列*</span><span class="sxs-lookup"><span data-stu-id="9ed2d-149">*String*</span></span> | <span data-ttu-id="9ed2d-150">読み取り専用</span><span class="sxs-lookup"><span data-stu-id="9ed2d-150">Read-only</span></span><br><span data-ttu-id="9ed2d-151">必須</span><span class="sxs-lookup"><span data-stu-id="9ed2d-151">Required</span></span> | <span data-ttu-id="9ed2d-152">スキルに要求されるレベルの説明です。</span><span class="sxs-lookup"><span data-stu-id="9ed2d-152">The description of the level required for the skill.</span></span> |
| <span data-ttu-id="9ed2d-153">**教育の分野 ID**</span><span class="sxs-lookup"><span data-stu-id="9ed2d-153">**Education Discipline ID**</span></span><br><span data-ttu-id="9ed2d-154">mshr_educationdisciplinedescription</span><span class="sxs-lookup"><span data-stu-id="9ed2d-154">mshr_educationdisciplinedescription</span></span><br><span data-ttu-id="9ed2d-155">*文字列*</span><span class="sxs-lookup"><span data-stu-id="9ed2d-155">*String*</span></span> | <span data-ttu-id="9ed2d-156">1回書き込み</span><span class="sxs-lookup"><span data-stu-id="9ed2d-156">Write-once</span></span><br><span data-ttu-id="9ed2d-157">必須</span><span class="sxs-lookup"><span data-stu-id="9ed2d-157">Required</span></span> | <span data-ttu-id="9ed2d-158">教育の分野です。</span><span class="sxs-lookup"><span data-stu-id="9ed2d-158">The area of educational discipline.</span></span> |
| <span data-ttu-id="9ed2d-159">**教育の分野 ID の値**</span><span class="sxs-lookup"><span data-stu-id="9ed2d-159">**Education Discipline ID Value**</span></span><br><span data-ttu-id="9ed2d-160">_mshr_fk_educationdiscipline_id_value</span><span class="sxs-lookup"><span data-stu-id="9ed2d-160">_mshr_fk_educationdiscipline_id_value</span></span><br><span data-ttu-id="9ed2d-161">*GUID*</span><span class="sxs-lookup"><span data-stu-id="9ed2d-161">*GUID*</span></span> | <span data-ttu-id="9ed2d-162">読み取り専用</span><span class="sxs-lookup"><span data-stu-id="9ed2d-162">Read-only</span></span><br><span data-ttu-id="9ed2d-163">必須</span><span class="sxs-lookup"><span data-stu-id="9ed2d-163">Required</span></span><br><span data-ttu-id="9ed2d-164">外部キー : mshr_hcmeducationdisciplineentity の mshr_hcmeducationdisciplineentityid</span><span class="sxs-lookup"><span data-stu-id="9ed2d-164">Foreign key: mshr_hcmeducationdisciplineentityid of mshr_hcmeducationdisciplineentity</span></span> | <span data-ttu-id="9ed2d-165">システムが生成した、教育分野の一意識別子です。</span><span class="sxs-lookup"><span data-stu-id="9ed2d-165">System-generated unique identifier of the area of educational discipline.</span></span> |
| <span data-ttu-id="9ed2d-166">**教育分野の説明**</span><span class="sxs-lookup"><span data-stu-id="9ed2d-166">**Education Discipline Description**</span></span><br><span data-ttu-id="9ed2d-167">mshr_educationdisciplinedescription</span><span class="sxs-lookup"><span data-stu-id="9ed2d-167">mshr_educationdisciplinedescription</span></span><br><span data-ttu-id="9ed2d-168">文字列</span><span class="sxs-lookup"><span data-stu-id="9ed2d-168">String</span></span> | <span data-ttu-id="9ed2d-169">読み取り専用</span><span class="sxs-lookup"><span data-stu-id="9ed2d-169">Read-only</span></span><br><span data-ttu-id="9ed2d-170">必須</span><span class="sxs-lookup"><span data-stu-id="9ed2d-170">Required</span></span> | <span data-ttu-id="9ed2d-171">教育分野の説明です。</span><span class="sxs-lookup"><span data-stu-id="9ed2d-171">The description of the area of educational discipline.</span></span> |
| <span data-ttu-id="9ed2d-172">**データ領域 ID**</span><span class="sxs-lookup"><span data-stu-id="9ed2d-172">**Data Area ID**</span></span><br><span data-ttu-id="9ed2d-173">mshr_dataareaid</span><span class="sxs-lookup"><span data-stu-id="9ed2d-173">mshr_dataareaid</span></span><br><span data-ttu-id="9ed2d-174">*文字列*</span><span class="sxs-lookup"><span data-stu-id="9ed2d-174">*String*</span></span> | <span data-ttu-id="9ed2d-175">読み取り/書き込み</span><span class="sxs-lookup"><span data-stu-id="9ed2d-175">Read/write</span></span><br><span data-ttu-id="9ed2d-176">オプション</span><span class="sxs-lookup"><span data-stu-id="9ed2d-176">Optional</span></span> | <span data-ttu-id="9ed2d-177">法人 (会社) を指定します。</span><span class="sxs-lookup"><span data-stu-id="9ed2d-177">Specifies the legal entity (company).</span></span>|
| <span data-ttu-id="9ed2d-178">**データ領域 ID 値**</span><span class="sxs-lookup"><span data-stu-id="9ed2d-178">**Data Area ID Value**</span></span><br><span data-ttu-id="9ed2d-179">_mshr_dataareaid_id_value</span><span class="sxs-lookup"><span data-stu-id="9ed2d-179">_mshr_dataareaid_id_value</span></span><br><span data-ttu-id="9ed2d-180">*GUID*</span><span class="sxs-lookup"><span data-stu-id="9ed2d-180">*GUID*</span></span> | <span data-ttu-id="9ed2d-181">読み取り専用</span><span class="sxs-lookup"><span data-stu-id="9ed2d-181">Read-only</span></span><br><span data-ttu-id="9ed2d-182">オプション</span><span class="sxs-lookup"><span data-stu-id="9ed2d-182">Optional</span></span><br><span data-ttu-id="9ed2d-183">外部キー : cdm_companyid of cdm_company エンティティ</span><span class="sxs-lookup"><span data-stu-id="9ed2d-183">Foreign key: cdm_companyid of cdm_company entity</span></span> | <span data-ttu-id="9ed2d-184">システムが生成する、法人 (会社) を識別する GUID 値です。</span><span class="sxs-lookup"><span data-stu-id="9ed2d-184">System-generated GUID value identifying the legal entity (company).</span></span> |
| <span data-ttu-id="9ed2d-185">**基本フィールド**</span><span class="sxs-lookup"><span data-stu-id="9ed2d-185">**Primary Field**</span></span><br><span data-ttu-id="9ed2d-186">mshr_primaryfield</span><span class="sxs-lookup"><span data-stu-id="9ed2d-186">mshr_primaryfield</span></span><br><span data-ttu-id="9ed2d-187">*文字列*</span><span class="sxs-lookup"><span data-stu-id="9ed2d-187">*String*</span></span> | <span data-ttu-id="9ed2d-188">読み取り専用</span><span class="sxs-lookup"><span data-stu-id="9ed2d-188">Read-only</span></span><br><span data-ttu-id="9ed2d-189">必須</span><span class="sxs-lookup"><span data-stu-id="9ed2d-189">Required</span></span> | <span data-ttu-id="9ed2d-190">レコードを一意に識別する別の方法としての採用要求値、教育レベルID、教育分野 ID の連結です。</span><span class="sxs-lookup"><span data-stu-id="9ed2d-190">Concatenation of Recruiting Request value, Education Level ID, and Education Discipline ID as another method to uniquely identify the record.</span></span> |

## <a name="see-also"></a><span data-ttu-id="9ed2d-191">参照</span><span class="sxs-lookup"><span data-stu-id="9ed2d-191">See also</span></span>

[<span data-ttu-id="9ed2d-192">申請者追跡システム統合APIの概要</span><span class="sxs-lookup"><span data-stu-id="9ed2d-192">Applicant Tracking System integration API introduction</span></span>](hr-admin-integration-ats-api-introduction.md)<br>
[<span data-ttu-id="9ed2d-193">採用要求のクエリの例</span><span class="sxs-lookup"><span data-stu-id="9ed2d-193">Example query for Recruiting request</span></span>](hr-admin-integration-ats-api-recruiting-request-example-query.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]