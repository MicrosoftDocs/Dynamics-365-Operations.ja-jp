---
title: 人物の職務経験
description: このトピックでは、Dynamics 365 Human Resources の人物の職務経験エンティティについて説明します。
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
ms.openlocfilehash: 5672e32b157b46b6863f06fea123fd3d6a3d96d2
ms.sourcegitcommit: 6affb3316be757c99e1fe9c7c7b312b93c483408
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/17/2021
ms.locfileid: "5466427"
---
# <a name="person-professional-experience"></a><span data-ttu-id="ee802-103">人物の職務経験</span><span class="sxs-lookup"><span data-stu-id="ee802-103">Person professional experience</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="ee802-104">このトピックでは、Dynamics 365 Human Resources の人物の職務経験エンティティについて説明します。</span><span class="sxs-lookup"><span data-stu-id="ee802-104">This topic describes the Person professional experience entity for Dynamics 365 Human Resources.</span></span>

<span data-ttu-id="ee802-105">物理名 : mshr_hcmpersonprofessionalexperienceentity</span><span class="sxs-lookup"><span data-stu-id="ee802-105">Physical name: mshr_hcmpersonprofessionalexperienceentity</span></span>

## <a name="description"></a><span data-ttu-id="ee802-106">説明</span><span class="sxs-lookup"><span data-stu-id="ee802-106">Description</span></span>

<span data-ttu-id="ee802-107">このエンティティは、候補者の職務経験または業務経歴を記述します。</span><span class="sxs-lookup"><span data-stu-id="ee802-107">This entity describes professional experience or work history of a candidate.</span></span>

## <a name="json-representation"></a><span data-ttu-id="ee802-108">JSON 表記</span><span class="sxs-lookup"><span data-stu-id="ee802-108">JSON representation</span></span>

```json
{
    "mshr_partynumber": "String",
    "mshr_employerposition": "String",
    "mshr_startdate": "Date",
    "mshr_allowcontactemployer": Int,
    "mshr_employerlocation": "String",
    "mshr_employername": "String",
    "mshr_enddate": "Date",
    "mshr_note": "String",
    "mshr_phone": "String",
    "mshr_url": "String",
    "mshr_primaryfield": "String",
    "_mshr_fk_person_id_value": "Guid",
    "mshr_hcmpersonprofessionalexperienceentityid": "Guid"
}
```

## <a name="properties"></a><span data-ttu-id="ee802-109">プロパティ</span><span class="sxs-lookup"><span data-stu-id="ee802-109">Properties</span></span>

| <span data-ttu-id="ee802-110">プロパティ</span><span class="sxs-lookup"><span data-stu-id="ee802-110">Property</span></span><br><span data-ttu-id="ee802-111">**現物名**</span><span class="sxs-lookup"><span data-stu-id="ee802-111">**Physical name**</span></span><br><span data-ttu-id="ee802-112">**_種類_**</span><span class="sxs-lookup"><span data-stu-id="ee802-112">**_Type_**</span></span> | <span data-ttu-id="ee802-113">使用</span><span class="sxs-lookup"><span data-stu-id="ee802-113">Use</span></span> | <span data-ttu-id="ee802-114">説明</span><span class="sxs-lookup"><span data-stu-id="ee802-114">Description</span></span> |
| --- | --- | --- |
| <span data-ttu-id="ee802-115">**人物の職務経験エンティティ ID**</span><span class="sxs-lookup"><span data-stu-id="ee802-115">**Person Professional Experience Entity ID**</span></span><br><span data-ttu-id="ee802-116">mshr_hcmpersonprofessionalexperienceentityid</span><span class="sxs-lookup"><span data-stu-id="ee802-116">mshr_hcmpersonprofessionalexperienceentityid</span></span><br><span data-ttu-id="ee802-117">*GUID*</span><span class="sxs-lookup"><span data-stu-id="ee802-117">*GUID*</span></span> | <span data-ttu-id="ee802-118">読み取り専用</span><span class="sxs-lookup"><span data-stu-id="ee802-118">Read-only</span></span><br><span data-ttu-id="ee802-119">必須</span><span class="sxs-lookup"><span data-stu-id="ee802-119">Required</span></span> | <span data-ttu-id="ee802-120">システムが生成した、エンティティ レコードの一意識別子です。</span><span class="sxs-lookup"><span data-stu-id="ee802-120">System-generated unique identifier for the entity record.</span></span> |
| <span data-ttu-id="ee802-121">**当事者番号**</span><span class="sxs-lookup"><span data-stu-id="ee802-121">**Party Number**</span></span><br><span data-ttu-id="ee802-122">mshr_partynumber</span><span class="sxs-lookup"><span data-stu-id="ee802-122">mshr_partynumber</span></span><br><span data-ttu-id="ee802-123">*文字列*</span><span class="sxs-lookup"><span data-stu-id="ee802-123">*String*</span></span> | <span data-ttu-id="ee802-124">読み取り/書き込み</span><span class="sxs-lookup"><span data-stu-id="ee802-124">Read/write</span></span><br><span data-ttu-id="ee802-125">必須</span><span class="sxs-lookup"><span data-stu-id="ee802-125">Required</span></span> | <span data-ttu-id="ee802-126">候補者の個人レコードの一意識別子です。</span><span class="sxs-lookup"><span data-stu-id="ee802-126">Unique identifier of the person record for the candidate.</span></span> |
| <span data-ttu-id="ee802-127">**個人 ID の値**</span><span class="sxs-lookup"><span data-stu-id="ee802-127">**Person ID Value**</span></span><br><span data-ttu-id="ee802-128">_mshr_fk_person_id_value</span><span class="sxs-lookup"><span data-stu-id="ee802-128">_mshr_fk_person_id_value</span></span><br><span data-ttu-id="ee802-129">*GUID*</span><span class="sxs-lookup"><span data-stu-id="ee802-129">*GUID*</span></span> | <span data-ttu-id="ee802-130">読み取り専用</span><span class="sxs-lookup"><span data-stu-id="ee802-130">Read-only</span></span><br><span data-ttu-id="ee802-131">必須</span><span class="sxs-lookup"><span data-stu-id="ee802-131">Required</span></span><br><span data-ttu-id="ee802-132">外部キー : mshr_dirpersonentity の mshr_dirpersonentityid</span><span class="sxs-lookup"><span data-stu-id="ee802-132">Foreign key: mshr_dirpersonentityid of mshr_dirpersonentity</span></span> | <span data-ttu-id="ee802-133">システムが生成した、人物のエンティティ レコードの一意識別子です。</span><span class="sxs-lookup"><span data-stu-id="ee802-133">System-generated unique identifier of the person entity record.</span></span> |
| <span data-ttu-id="ee802-134">**雇用主の職位**</span><span class="sxs-lookup"><span data-stu-id="ee802-134">**Employer Position**</span></span><br><span data-ttu-id="ee802-135">mshr_employerposition</span><span class="sxs-lookup"><span data-stu-id="ee802-135">mshr_employerposition</span></span><br><span data-ttu-id="ee802-136">*文字列*</span><span class="sxs-lookup"><span data-stu-id="ee802-136">*String*</span></span> | <span data-ttu-id="ee802-137">読み取り/書き込み</span><span class="sxs-lookup"><span data-stu-id="ee802-137">Read/write</span></span><br><span data-ttu-id="ee802-138">必須</span><span class="sxs-lookup"><span data-stu-id="ee802-138">Required</span></span> | <span data-ttu-id="ee802-139">候補者が在職中に経験した職位です。</span><span class="sxs-lookup"><span data-stu-id="ee802-139">The position title held by the candidate while under employment.</span></span> |
| <span data-ttu-id="ee802-140">**従業員名称**</span><span class="sxs-lookup"><span data-stu-id="ee802-140">**Employer Name**</span></span><br><span data-ttu-id="ee802-141">mshr_employername</span><span class="sxs-lookup"><span data-stu-id="ee802-141">mshr_employername</span></span><br><span data-ttu-id="ee802-142">*文字列*</span><span class="sxs-lookup"><span data-stu-id="ee802-142">*String*</span></span> | <span data-ttu-id="ee802-143">読み取り/書き込み</span><span class="sxs-lookup"><span data-stu-id="ee802-143">Read/write</span></span><br><span data-ttu-id="ee802-144">必須</span><span class="sxs-lookup"><span data-stu-id="ee802-144">Required</span></span> | <span data-ttu-id="ee802-145">従業員の名前です。</span><span class="sxs-lookup"><span data-stu-id="ee802-145">The name of the employer.</span></span> |
| <span data-ttu-id="ee802-146">**雇用主の場所**</span><span class="sxs-lookup"><span data-stu-id="ee802-146">**Employer Location**</span></span><br><span data-ttu-id="ee802-147">mshr_employerlocation</span><span class="sxs-lookup"><span data-stu-id="ee802-147">mshr_employerlocation</span></span><br><span data-ttu-id="ee802-148">*文字列*</span><span class="sxs-lookup"><span data-stu-id="ee802-148">*String*</span></span> | <span data-ttu-id="ee802-149">読み取り/書き込み</span><span class="sxs-lookup"><span data-stu-id="ee802-149">Read/write</span></span><br><span data-ttu-id="ee802-150">オプション</span><span class="sxs-lookup"><span data-stu-id="ee802-150">Optional</span></span> | <span data-ttu-id="ee802-151">雇用主の場所です。</span><span class="sxs-lookup"><span data-stu-id="ee802-151">The employer’s location.</span></span> <span data-ttu-id="ee802-152">最大の長さ : 60 。</span><span class="sxs-lookup"><span data-stu-id="ee802-152">Max length: 60.</span></span> <span data-ttu-id="ee802-153">特定の形式や定義は不要です。</span><span class="sxs-lookup"><span data-stu-id="ee802-153">No specific format defined or required.</span></span> |
| <span data-ttu-id="ee802-154">**電話**</span><span class="sxs-lookup"><span data-stu-id="ee802-154">**Phone**</span></span><br><span data-ttu-id="ee802-155">mshr_phone</span><span class="sxs-lookup"><span data-stu-id="ee802-155">mshr_phone</span></span><br><span data-ttu-id="ee802-156">*文字列*</span><span class="sxs-lookup"><span data-stu-id="ee802-156">*String*</span></span> | <span data-ttu-id="ee802-157">読み取り/書き込み</span><span class="sxs-lookup"><span data-stu-id="ee802-157">Read/write</span></span><br><span data-ttu-id="ee802-158">オプション</span><span class="sxs-lookup"><span data-stu-id="ee802-158">Optional</span></span> | <span data-ttu-id="ee802-159">雇用主の電話番号です。</span><span class="sxs-lookup"><span data-stu-id="ee802-159">The employer’s phone number.</span></span> |
| <span data-ttu-id="ee802-160">**URL**</span><span class="sxs-lookup"><span data-stu-id="ee802-160">**URL**</span></span><br><span data-ttu-id="ee802-161">mshr_url</span><span class="sxs-lookup"><span data-stu-id="ee802-161">mshr_url</span></span><br><span data-ttu-id="ee802-162">*文字列*</span><span class="sxs-lookup"><span data-stu-id="ee802-162">*String*</span></span> | <span data-ttu-id="ee802-163">読み取り/書き込み</span><span class="sxs-lookup"><span data-stu-id="ee802-163">Read/write</span></span><br><span data-ttu-id="ee802-164">オプション</span><span class="sxs-lookup"><span data-stu-id="ee802-164">Optional</span></span> | <span data-ttu-id="ee802-165">雇用主の Web サイトの URL です。</span><span class="sxs-lookup"><span data-stu-id="ee802-165">The URL of the employer’s website.</span></span> |
| <span data-ttu-id="ee802-166">**開始日**</span><span class="sxs-lookup"><span data-stu-id="ee802-166">**Start Date**</span></span><br><span data-ttu-id="ee802-167">mshr_startdate</span><span class="sxs-lookup"><span data-stu-id="ee802-167">mshr_startdate</span></span><br><span data-ttu-id="ee802-168">*Datetime*</span><span class="sxs-lookup"><span data-stu-id="ee802-168">*Datetime*</span></span> | <span data-ttu-id="ee802-169">読み取り/書き込み</span><span class="sxs-lookup"><span data-stu-id="ee802-169">Read/write</span></span><br><span data-ttu-id="ee802-170">必須</span><span class="sxs-lookup"><span data-stu-id="ee802-170">Required</span></span> | <span data-ttu-id="ee802-171">候補者の雇用開始日です。</span><span class="sxs-lookup"><span data-stu-id="ee802-171">The start date of the candidate’s employment.</span></span> |
| <span data-ttu-id="ee802-172">**終了日**</span><span class="sxs-lookup"><span data-stu-id="ee802-172">**End Date**</span></span><br><span data-ttu-id="ee802-173">mshr_enddate</span><span class="sxs-lookup"><span data-stu-id="ee802-173">mshr_enddate</span></span><br><span data-ttu-id="ee802-174">*Datetime*</span><span class="sxs-lookup"><span data-stu-id="ee802-174">*Datetime*</span></span> | <span data-ttu-id="ee802-175">読み取り/書き込み</span><span class="sxs-lookup"><span data-stu-id="ee802-175">Read/write</span></span><br><span data-ttu-id="ee802-176">オプション</span><span class="sxs-lookup"><span data-stu-id="ee802-176">Optional</span></span> | <span data-ttu-id="ee802-177">候補者の雇用終了日です。候補者の雇用が継続している場合は、null 値となります。</span><span class="sxs-lookup"><span data-stu-id="ee802-177">The end date of the candidate’s employment, or null if the candidate is still employed here.</span></span> |
| <span data-ttu-id="ee802-178">**雇用主への連絡を許可する**</span><span class="sxs-lookup"><span data-stu-id="ee802-178">**Allow Contact Employer**</span></span><br><span data-ttu-id="ee802-179">mshr_allowcontactemployer</span><span class="sxs-lookup"><span data-stu-id="ee802-179">mshr_allowcontactemployer</span></span><br><span data-ttu-id="ee802-180">*mshr_hrmblankyesno オプション セット*</span><span class="sxs-lookup"><span data-stu-id="ee802-180">*mshr_hrmblankyesno option set*</span></span> | <span data-ttu-id="ee802-181">読み取り/書き込み</span><span class="sxs-lookup"><span data-stu-id="ee802-181">Read/write</span></span><br><span data-ttu-id="ee802-182">オプション</span><span class="sxs-lookup"><span data-stu-id="ee802-182">Optional</span></span> | <span data-ttu-id="ee802-183">候補者が前の雇用主への連絡を許可するかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="ee802-183">Signifies whether the candidate allows contacting the previous employer.</span></span> |
| <span data-ttu-id="ee802-184">**摘要**</span><span class="sxs-lookup"><span data-stu-id="ee802-184">**Notes**</span></span><br><span data-ttu-id="ee802-185">mshr_note</span><span class="sxs-lookup"><span data-stu-id="ee802-185">mshr_note</span></span><br><span data-ttu-id="ee802-186">*文字列*</span><span class="sxs-lookup"><span data-stu-id="ee802-186">*String*</span></span> | <span data-ttu-id="ee802-187">読み取り/書き込み</span><span class="sxs-lookup"><span data-stu-id="ee802-187">Read/write</span></span><br><span data-ttu-id="ee802-188">オプション</span><span class="sxs-lookup"><span data-stu-id="ee802-188">Optional</span></span> | <span data-ttu-id="ee802-189">採用担当者や採用マネージャーが使用するメモです。</span><span class="sxs-lookup"><span data-stu-id="ee802-189">Notes for use by the recruiter or hiring manager.</span></span> |
| <span data-ttu-id="ee802-190">**基本フィールド**</span><span class="sxs-lookup"><span data-stu-id="ee802-190">**Primary Field**</span></span><br><span data-ttu-id="ee802-191">mshr_primaryfield</span><span class="sxs-lookup"><span data-stu-id="ee802-191">mshr_primaryfield</span></span><br><span data-ttu-id="ee802-192">*文字列*</span><span class="sxs-lookup"><span data-stu-id="ee802-192">*String*</span></span> | <span data-ttu-id="ee802-193">読み取り専用</span><span class="sxs-lookup"><span data-stu-id="ee802-193">Read-only</span></span><br><span data-ttu-id="ee802-194">必須</span><span class="sxs-lookup"><span data-stu-id="ee802-194">Required</span></span> | <span data-ttu-id="ee802-195">エンティティ レコードの基本識別子として使用されるフィールドです。</span><span class="sxs-lookup"><span data-stu-id="ee802-195">Field used as a primary identifier of the entity record.</span></span> <span data-ttu-id="ee802-196">関係者番号、開始日、雇用主の職位、雇用主名の組み合わせです。</span><span class="sxs-lookup"><span data-stu-id="ee802-196">Combination of party number, start date, employer position, and employer name.</span></span> |

## <a name="see-also"></a><span data-ttu-id="ee802-197">参照</span><span class="sxs-lookup"><span data-stu-id="ee802-197">See also</span></span>

[<span data-ttu-id="ee802-198">申請者追跡システム統合APIの概要</span><span class="sxs-lookup"><span data-stu-id="ee802-198">Applicant Tracking System integration API introduction</span></span>](hr-admin-integration-ats-api-introduction.md)<br>
[<span data-ttu-id="ee802-199">採用する採用候補者に対するクエリの例</span><span class="sxs-lookup"><span data-stu-id="ee802-199">Example query for Candidate to hire</span></span>](hr-admin-integration-ats-api-candidate-to-hire-example-query.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]