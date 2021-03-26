---
title: 採用候補者
description: このトピックでは、Dynamics 365 Human Resources の採用候補者エンティティについて説明します。
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
ms.openlocfilehash: eb16f9f46e3f5c58854ec06c3b89ec72dd7bae00
ms.sourcegitcommit: 33b5c8bc4f9461e290513aa22de1ec1fba3b0742
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/05/2021
ms.locfileid: "5125740"
---
# <a name="candidate-to-hire"></a><span data-ttu-id="7ff88-103">採用候補者</span><span class="sxs-lookup"><span data-stu-id="7ff88-103">Candidate to hire</span></span>

<span data-ttu-id="7ff88-104">このトピックでは、Dynamics 365 Human Resources の採用候補者エンティティについて説明します。</span><span class="sxs-lookup"><span data-stu-id="7ff88-104">This topic describes the Candidate to hire entity for Dynamics 365 Human Resources.</span></span>

<span data-ttu-id="7ff88-105">物理名 : mshr_hcmcandidatetohireentity</span><span class="sxs-lookup"><span data-stu-id="7ff88-105">Physical name: mshr_hcmcandidatetohireentity</span></span>

## <a name="description"></a><span data-ttu-id="7ff88-106">説明</span><span class="sxs-lookup"><span data-stu-id="7ff88-106">Description</span></span>

<span data-ttu-id="7ff88-107">このエンティティは、 Dynamics 365 Human Resources で従業員の作成に使用される候補者の詳細を提供します。</span><span class="sxs-lookup"><span data-stu-id="7ff88-107">This entity provides candidate details used to create a worker in Dynamics 365 Human Resources.</span></span> <span data-ttu-id="7ff88-108">すべての候補者レコードを読み取り、内部および外部の候補者の記録の作成に使用され、新しい候補者の個人情報を作成できます。</span><span class="sxs-lookup"><span data-stu-id="7ff88-108">It's used to read all candidate records and create internal and external candidate records, allowing you to create personal details for the new candidate.</span></span>

<span data-ttu-id="7ff88-109">システム内で新規人物レコードとなる外部の候補者レコードを作成する際には、新規候補者レコードを投稿する当事者 (人物) 番号を定義する必要があります。</span><span class="sxs-lookup"><span data-stu-id="7ff88-109">When you create an external candidate record who will be a new person record in the system, you must not define a party (person) number you post a new candidate record.</span></span> <span data-ttu-id="7ff88-110">新しい人物のエンティティ レコードは、新しい候補者レコードを使用して作成されます。</span><span class="sxs-lookup"><span data-stu-id="7ff88-110">The new person entity record is created with the new candidate record.</span></span>

<span data-ttu-id="7ff88-111">社内の候補者レコード (すでに社内で従業員レコードを持っている職位の候補者) を作成する場合は、新しい人物のレコードを作成する際に使用する個人情報 (名前、性別、生年月日など) を定義するのではなく、候補者レコードの mshr_partynumber プロパティに、すでに存在する人物レコードの当事者 (個人) 番号を定義してください。</span><span class="sxs-lookup"><span data-stu-id="7ff88-111">When you create an internal candidate record (a candidate for the position who already has an employee record with the company), define the party (person) number of the record that already exists for person for the mshr_partynumber property on the candidate record rather than defining personal information (such as name, gender, or birthdate) that would be used to create a new person record.</span></span>

## <a name="json-representation"></a><span data-ttu-id="7ff88-112">JSON 表記</span><span class="sxs-lookup"><span data-stu-id="7ff88-112">JSON representation</span></span>

```json
        {
            "mshr_candidateid": "String",
            "mshr_partynumber": "String",
            "mshr_partytype": "String",
            "mshr_recruitingrequestid": "String",
            "mshr_positionid": "String",
            "mshr_firstname": "String",
            "mshr_middlename": "String",
            "mshr_lastnameprefix": "String",
            "mshr_lastname": "String",
            "mshr_gender": Int,
            "mshr_birthdate": "Date",
            "mshr_citizenshipcountrycode": "String",
            "mshr_veteranstatusid": "String",
            "mshr_isdisabledveteran": Int,
            "mshr_availabilitydate": "Date",
            "mshr_iswillingtorelocate": Int,
            "mshr_comments": "String",
            "mshr_applicantintegrationresult": Int,
            "mshr_donothirereasoncodeid": "String",
            "mshr_dataareaid": "String",
            "_mshr_dataareaid_id_value": "Guid",
            "_mshr_fk_person_id_value": "Guid",
            "_mshr_fk_recruitingrequest_id_value": "Guid",
            "_mshr_fk_position_id_value": "Guid",
            "mshr_hcmcandidatetohireentityid": "Guid",
            "_mshr_fk_veteranstatus_id_value": "Guid",
            "_mshr_fk_reasoncode_id_value": "Guid",
            "mshr_militaryserviceenddate": "Guid",
            "mshr_militaryservicestartdate": "Guid"
        }
```

## <a name="properties"></a><span data-ttu-id="7ff88-113">プロパティ</span><span class="sxs-lookup"><span data-stu-id="7ff88-113">Properties</span></span>

| <span data-ttu-id="7ff88-114">プロパティ</span><span class="sxs-lookup"><span data-stu-id="7ff88-114">Property</span></span><br><span data-ttu-id="7ff88-115">**現物名**</span><span class="sxs-lookup"><span data-stu-id="7ff88-115">**Physical name**</span></span><br><span data-ttu-id="7ff88-116">**_種類_**</span><span class="sxs-lookup"><span data-stu-id="7ff88-116">**_Type_**</span></span> | <span data-ttu-id="7ff88-117">使用</span><span class="sxs-lookup"><span data-stu-id="7ff88-117">Use</span></span> | <span data-ttu-id="7ff88-118">説明</span><span class="sxs-lookup"><span data-stu-id="7ff88-118">Description</span></span> |
| --- | --- | --- |
| <span data-ttu-id="7ff88-119">**採用候補者のエンティティ ID**</span><span class="sxs-lookup"><span data-stu-id="7ff88-119">**Candidate to Hire Entity ID**</span></span><br><span data-ttu-id="7ff88-120">mshr_hcmcandidatetohireentityid</span><span class="sxs-lookup"><span data-stu-id="7ff88-120">mshr_hcmcandidatetohireentityid</span></span><br><span data-ttu-id="7ff88-121">GUID</span><span class="sxs-lookup"><span data-stu-id="7ff88-121">GUID</span></span> | <span data-ttu-id="7ff88-122">読み取り専用</span><span class="sxs-lookup"><span data-stu-id="7ff88-122">Read-only</span></span><br><span data-ttu-id="7ff88-123">必須</span><span class="sxs-lookup"><span data-stu-id="7ff88-123">Required</span></span><br><span data-ttu-id="7ff88-124">システム生成</span><span class="sxs-lookup"><span data-stu-id="7ff88-124">System-generated</span></span> | <span data-ttu-id="7ff88-125">システムが生成した、エンティティ レコードの一意識別子です。</span><span class="sxs-lookup"><span data-stu-id="7ff88-125">A system-generated unique identifier for the entity record.</span></span> |
| <span data-ttu-id="7ff88-126">**候補者 ID**</span><span class="sxs-lookup"><span data-stu-id="7ff88-126">**Candidate ID**</span></span><br><span data-ttu-id="7ff88-127">mshr_candidateid</span><span class="sxs-lookup"><span data-stu-id="7ff88-127">mshr_candidateid</span></span><br><span data-ttu-id="7ff88-128">文字列</span><span class="sxs-lookup"><span data-stu-id="7ff88-128">String</span></span> | <span data-ttu-id="7ff88-129">読み取り専用</span><span class="sxs-lookup"><span data-stu-id="7ff88-129">Read-only</span></span><br><span data-ttu-id="7ff88-130">必須</span><span class="sxs-lookup"><span data-stu-id="7ff88-130">Required</span></span><br><span data-ttu-id="7ff88-131">システム生成</span><span class="sxs-lookup"><span data-stu-id="7ff88-131">System-generated</span></span> | <span data-ttu-id="7ff88-132">エンティティの一意の識別子。</span><span class="sxs-lookup"><span data-stu-id="7ff88-132">A unique identifier for the entity.</span></span> |
| <span data-ttu-id="7ff88-133">**当事者番号**</span><span class="sxs-lookup"><span data-stu-id="7ff88-133">**Party Number**</span></span><br><span data-ttu-id="7ff88-134">mshr_partynumber</span><span class="sxs-lookup"><span data-stu-id="7ff88-134">mshr_partynumber</span></span><br><span data-ttu-id="7ff88-135">文字列</span><span class="sxs-lookup"><span data-stu-id="7ff88-135">String</span></span> | <span data-ttu-id="7ff88-136">読み取り専用</span><span class="sxs-lookup"><span data-stu-id="7ff88-136">Read-only</span></span><br><span data-ttu-id="7ff88-137">必須</span><span class="sxs-lookup"><span data-stu-id="7ff88-137">Required</span></span> | <span data-ttu-id="7ff88-138">候補者の人物レコードの当事者 (個人) 番号。</span><span class="sxs-lookup"><span data-stu-id="7ff88-138">The party (person) number of the candidate’s person record.</span></span> |
| <span data-ttu-id="7ff88-139">**個人 ID の値**</span><span class="sxs-lookup"><span data-stu-id="7ff88-139">**Person ID Value**</span></span><br><span data-ttu-id="7ff88-140">_mshr_fk_person_id_value</span><span class="sxs-lookup"><span data-stu-id="7ff88-140">_mshr_fk_person_id_value</span></span><br><span data-ttu-id="7ff88-141">GUID</span><span class="sxs-lookup"><span data-stu-id="7ff88-141">GUID</span></span> | <span data-ttu-id="7ff88-142">読み取り専用</span><span class="sxs-lookup"><span data-stu-id="7ff88-142">Read-only</span></span><br><span data-ttu-id="7ff88-143">必須</span><span class="sxs-lookup"><span data-stu-id="7ff88-143">Required</span></span><br><span data-ttu-id="7ff88-144">外部キー : mshr_direpersonentity の mshr_dirpersonentityid</span><span class="sxs-lookup"><span data-stu-id="7ff88-144">Foreign key: mshr_dirpersonentityid of mshr_direpersonentity</span></span> | <span data-ttu-id="7ff88-145">システムが生成する、候補者の当事者 (個人) レコードの一意識別子。</span><span class="sxs-lookup"><span data-stu-id="7ff88-145">The system-generated unique identifier for the party (person) record of the candidate.</span></span> |
| <span data-ttu-id="7ff88-146">**当事者 タイプ**</span><span class="sxs-lookup"><span data-stu-id="7ff88-146">**Party Type**</span></span><br><span data-ttu-id="7ff88-147">mshr_partytype</span><span class="sxs-lookup"><span data-stu-id="7ff88-147">mshr_partytype</span></span><br><span data-ttu-id="7ff88-148">mshr_dirpartytype オプション セット</span><span class="sxs-lookup"><span data-stu-id="7ff88-148">mshr_dirpartytype option set</span></span> | <span data-ttu-id="7ff88-149">読み取り専用</span><span class="sxs-lookup"><span data-stu-id="7ff88-149">Read-only</span></span><br><span data-ttu-id="7ff88-150">必須</span><span class="sxs-lookup"><span data-stu-id="7ff88-150">Required</span></span> | <span data-ttu-id="7ff88-151">mshr_dirpartytype オプションセットに定義されている、当事者タイプのレコード。</span><span class="sxs-lookup"><span data-stu-id="7ff88-151">The party type of the record, as defined in the mshr_dirpartytype option set.</span></span> <span data-ttu-id="7ff88-152">このエンティティのタイプは常に "人" です。</span><span class="sxs-lookup"><span data-stu-id="7ff88-152">For this entity, the type will always be “Person”.</span></span> |
| <span data-ttu-id="7ff88-153">**採用要求 ID**</span><span class="sxs-lookup"><span data-stu-id="7ff88-153">**Recruiting Request ID**</span></span><br><span data-ttu-id="7ff88-154">mshr_recruitingrequestid</span><span class="sxs-lookup"><span data-stu-id="7ff88-154">mshr_recruitingrequestid</span></span><br><span data-ttu-id="7ff88-155">文字列</span><span class="sxs-lookup"><span data-stu-id="7ff88-155">String</span></span> | <span data-ttu-id="7ff88-156">1回書き込み</span><span class="sxs-lookup"><span data-stu-id="7ff88-156">Write once</span></span><br><span data-ttu-id="7ff88-157">オプション</span><span class="sxs-lookup"><span data-stu-id="7ff88-157">Optional</span></span> | <span data-ttu-id="7ff88-158">この候補者が履行する採用要求を参照します。</span><span class="sxs-lookup"><span data-stu-id="7ff88-158">References the Recruiting Request this candidate fulfills.</span></span> |
| <span data-ttu-id="7ff88-159">**採用要求 ID 値**</span><span class="sxs-lookup"><span data-stu-id="7ff88-159">**Recruiting Request ID Value**</span></span><br><span data-ttu-id="7ff88-160">_mshr_fk_recruitingrequest_id_value</span><span class="sxs-lookup"><span data-stu-id="7ff88-160">_mshr_fk_recruitingrequest_id_value</span></span><br><span data-ttu-id="7ff88-161">GUID</span><span class="sxs-lookup"><span data-stu-id="7ff88-161">GUID</span></span> | <span data-ttu-id="7ff88-162">読み取り/書き込み</span><span class="sxs-lookup"><span data-stu-id="7ff88-162">Read/write</span></span><br><span data-ttu-id="7ff88-163">オプション</span><span class="sxs-lookup"><span data-stu-id="7ff88-163">Optional</span></span><br><span data-ttu-id="7ff88-164">外部キー : mshr_hcmrecruitingrequestentity の mshr_hcmrecruitingrequestentityid</span><span class="sxs-lookup"><span data-stu-id="7ff88-164">Foreign key: mshr_hcmrecruitingrequestentityid of mshr_hcmrecruitingrequestentity</span></span> | <span data-ttu-id="7ff88-165">システムが生成する、候補者が履行する採用要求の一意識別子。</span><span class="sxs-lookup"><span data-stu-id="7ff88-165">The system-generated unique identifier of the recruiting request the candidate fulfills.</span></span> |
| <span data-ttu-id="7ff88-166">**職位 ID**</span><span class="sxs-lookup"><span data-stu-id="7ff88-166">**Position ID**</span></span><br><span data-ttu-id="7ff88-167">mshr_positionid</span><span class="sxs-lookup"><span data-stu-id="7ff88-167">mshr_positionid</span></span><br><span data-ttu-id="7ff88-168">文字列</span><span class="sxs-lookup"><span data-stu-id="7ff88-168">String</span></span> | <span data-ttu-id="7ff88-169">読み取り/書き込み</span><span class="sxs-lookup"><span data-stu-id="7ff88-169">Read/write</span></span><br><span data-ttu-id="7ff88-170">オプション</span><span class="sxs-lookup"><span data-stu-id="7ff88-170">Optional</span></span> | <span data-ttu-id="7ff88-171">候補者が検討しているポジションの ID。</span><span class="sxs-lookup"><span data-stu-id="7ff88-171">The ID of the position for which the candidate is being considered.</span></span> |
| <span data-ttu-id="7ff88-172">**ポジション ID の値**</span><span class="sxs-lookup"><span data-stu-id="7ff88-172">**Position ID Value**</span></span><br><span data-ttu-id="7ff88-173">_mshr_fk_position_if_value</span><span class="sxs-lookup"><span data-stu-id="7ff88-173">_mshr_fk_position_if_value</span></span><br><span data-ttu-id="7ff88-174">GUID</span><span class="sxs-lookup"><span data-stu-id="7ff88-174">GUID</span></span> | <span data-ttu-id="7ff88-175">読み取り専用</span><span class="sxs-lookup"><span data-stu-id="7ff88-175">Read-only</span></span><br><span data-ttu-id="7ff88-176">オプション</span><span class="sxs-lookup"><span data-stu-id="7ff88-176">Optional</span></span><br><span data-ttu-id="7ff88-177">外部キー : mshr_hcmpositionv2entity の mshr_hcmpositionv2entityid</span><span class="sxs-lookup"><span data-stu-id="7ff88-177">Foreign key: mshr_hcmpositionv2entityid of mshr_hcmpositionv2entity</span></span> | <span data-ttu-id="7ff88-178">システムが生成する、 候補者が検討しているポジションの識別子。</span><span class="sxs-lookup"><span data-stu-id="7ff88-178">System-generated identifier of the position for with the candidate is being considered.</span></span> |
| <span data-ttu-id="7ff88-179">**名**</span><span class="sxs-lookup"><span data-stu-id="7ff88-179">**First Name**</span></span><br><span data-ttu-id="7ff88-180">mshr_firstname</span><span class="sxs-lookup"><span data-stu-id="7ff88-180">mshr_firstname</span></span><br><span data-ttu-id="7ff88-181">文字列</span><span class="sxs-lookup"><span data-stu-id="7ff88-181">String</span></span> | <span data-ttu-id="7ff88-182">読み取り/書き込み</span><span class="sxs-lookup"><span data-stu-id="7ff88-182">Read/write</span></span><br><span data-ttu-id="7ff88-183">必須</span><span class="sxs-lookup"><span data-stu-id="7ff88-183">Required</span></span> | <span data-ttu-id="7ff88-184">候補者の名前。</span><span class="sxs-lookup"><span data-stu-id="7ff88-184">Candidate first name.</span></span> |
| <span data-ttu-id="7ff88-185">**ミドル ネーム**</span><span class="sxs-lookup"><span data-stu-id="7ff88-185">**Middle Name**</span></span><br><span data-ttu-id="7ff88-186">mshr_middlename</span><span class="sxs-lookup"><span data-stu-id="7ff88-186">mshr_middlename</span></span><br><span data-ttu-id="7ff88-187">文字列</span><span class="sxs-lookup"><span data-stu-id="7ff88-187">String</span></span> | <span data-ttu-id="7ff88-188">読み取り/書き込み</span><span class="sxs-lookup"><span data-stu-id="7ff88-188">Read/write</span></span><br><span data-ttu-id="7ff88-189">オプション</span><span class="sxs-lookup"><span data-stu-id="7ff88-189">Optional</span></span> | <span data-ttu-id="7ff88-190">候補者のミドルネーム。</span><span class="sxs-lookup"><span data-stu-id="7ff88-190">Candidate middle name.</span></span> |
| <span data-ttu-id="7ff88-191">**姓の接頭辞**</span><span class="sxs-lookup"><span data-stu-id="7ff88-191">**Last Name Prefix**</span></span><br><span data-ttu-id="7ff88-192">mshr_lastnameprefix</span><span class="sxs-lookup"><span data-stu-id="7ff88-192">mshr_lastnameprefix</span></span><br><span data-ttu-id="7ff88-193">文字列</span><span class="sxs-lookup"><span data-stu-id="7ff88-193">String</span></span> | <span data-ttu-id="7ff88-194">読み取り/書き込み</span><span class="sxs-lookup"><span data-stu-id="7ff88-194">Read/write</span></span><br><span data-ttu-id="7ff88-195">オプション</span><span class="sxs-lookup"><span data-stu-id="7ff88-195">Optional</span></span> | <span data-ttu-id="7ff88-196">候補者の姓の接頭辞です。</span><span class="sxs-lookup"><span data-stu-id="7ff88-196">Candidate last name prefix.</span></span> |
| <span data-ttu-id="7ff88-197">**姓**</span><span class="sxs-lookup"><span data-stu-id="7ff88-197">**Last Name**</span></span><br><span data-ttu-id="7ff88-198">mshr_lastname</span><span class="sxs-lookup"><span data-stu-id="7ff88-198">mshr_lastname</span></span><br><span data-ttu-id="7ff88-199">文字列</span><span class="sxs-lookup"><span data-stu-id="7ff88-199">String</span></span> | <span data-ttu-id="7ff88-200">読み取り/書き込み</span><span class="sxs-lookup"><span data-stu-id="7ff88-200">Read/write</span></span><br><span data-ttu-id="7ff88-201">オプション</span><span class="sxs-lookup"><span data-stu-id="7ff88-201">Optional</span></span> | <span data-ttu-id="7ff88-202">候補者の名前。</span><span class="sxs-lookup"><span data-stu-id="7ff88-202">Candidate last name.</span></span> |
| <span data-ttu-id="7ff88-203">**種類**</span><span class="sxs-lookup"><span data-stu-id="7ff88-203">**Gender**</span></span><br><span data-ttu-id="7ff88-204">mshr_gender</span><span class="sxs-lookup"><span data-stu-id="7ff88-204">mshr_gender</span></span><br><span data-ttu-id="7ff88-205">mshr_hcmpersongender オプション セット</span><span class="sxs-lookup"><span data-stu-id="7ff88-205">mshr_hcmpersongender option set</span></span> | <span data-ttu-id="7ff88-206">読み取り/書き込み</span><span class="sxs-lookup"><span data-stu-id="7ff88-206">Read/write</span></span><br><span data-ttu-id="7ff88-207">オプション</span><span class="sxs-lookup"><span data-stu-id="7ff88-207">Optional</span></span> | <span data-ttu-id="7ff88-208">候補者の性別。</span><span class="sxs-lookup"><span data-stu-id="7ff88-208">The candidate’s gender.</span></span> |
| <span data-ttu-id="7ff88-209">**生年月日**</span><span class="sxs-lookup"><span data-stu-id="7ff88-209">**Birth Date**</span></span><br><span data-ttu-id="7ff88-210">mshr_birthdate</span><span class="sxs-lookup"><span data-stu-id="7ff88-210">mshr_birthdate</span></span><br><span data-ttu-id="7ff88-211">日時</span><span class="sxs-lookup"><span data-stu-id="7ff88-211">Datetime</span></span> | <span data-ttu-id="7ff88-212">読み取り/書き込み</span><span class="sxs-lookup"><span data-stu-id="7ff88-212">Read/write</span></span><br><span data-ttu-id="7ff88-213">オプション</span><span class="sxs-lookup"><span data-stu-id="7ff88-213">Optional</span></span> | <span data-ttu-id="7ff88-214">候補者の生年月日。</span><span class="sxs-lookup"><span data-stu-id="7ff88-214">The candidate’s birth date.</span></span> |
| <span data-ttu-id="7ff88-215">**市民権のある国番号**</span><span class="sxs-lookup"><span data-stu-id="7ff88-215">**Citizenship Country Code**</span></span><br><span data-ttu-id="7ff88-216">mshr_citizenshipcountrycode</span><span class="sxs-lookup"><span data-stu-id="7ff88-216">mshr_citizenshipcountrycode</span></span><br><span data-ttu-id="7ff88-217">文字列</span><span class="sxs-lookup"><span data-stu-id="7ff88-217">String</span></span> | <span data-ttu-id="7ff88-218">読み取り/書き込み</span><span class="sxs-lookup"><span data-stu-id="7ff88-218">Read/write</span></span><br><span data-ttu-id="7ff88-219">オプション</span><span class="sxs-lookup"><span data-stu-id="7ff88-219">Optional</span></span> | <span data-ttu-id="7ff88-220">候補者が市民権を有する国を指定します。</span><span class="sxs-lookup"><span data-stu-id="7ff88-220">Specifies the country where the candidate has citizenship.</span></span> <span data-ttu-id="7ff88-221">有効な国番号は、mshr_logisticaddresscountryregionentity にあります。</span><span class="sxs-lookup"><span data-stu-id="7ff88-221">Valid country codes are in mshr_logisticaddresscountryregionentity.</span></span> |
| <span data-ttu-id="7ff88-222">**ベテランの状態 ID**</span><span class="sxs-lookup"><span data-stu-id="7ff88-222">**Veteran Status ID**</span></span><br><span data-ttu-id="7ff88-223">mshr_veteranstatusid</span><span class="sxs-lookup"><span data-stu-id="7ff88-223">mshr_veteranstatusid</span></span><br><span data-ttu-id="7ff88-224">文字列</span><span class="sxs-lookup"><span data-stu-id="7ff88-224">String</span></span> | <span data-ttu-id="7ff88-225">読み取り/書き込み</span><span class="sxs-lookup"><span data-stu-id="7ff88-225">Read/write</span></span><br><span data-ttu-id="7ff88-226">オプション</span><span class="sxs-lookup"><span data-stu-id="7ff88-226">Optional</span></span> | <span data-ttu-id="7ff88-227">候補者の退役者状態を示します。</span><span class="sxs-lookup"><span data-stu-id="7ff88-227">Indicates the veteran status of the candidate.</span></span> |
| <span data-ttu-id="7ff88-228">**退役者の状態 ID 値**</span><span class="sxs-lookup"><span data-stu-id="7ff88-228">**Veteran Status ID Value**</span></span><br><span data-ttu-id="7ff88-229">_mshr_fk_veteranstatus_id_value</span><span class="sxs-lookup"><span data-stu-id="7ff88-229">_mshr_fk_veteranstatus_id_value</span></span><br><span data-ttu-id="7ff88-230">GUID</span><span class="sxs-lookup"><span data-stu-id="7ff88-230">GUID</span></span> | <span data-ttu-id="7ff88-231">読み取り専用</span><span class="sxs-lookup"><span data-stu-id="7ff88-231">Read-only</span></span><br><span data-ttu-id="7ff88-232">オプション</span><span class="sxs-lookup"><span data-stu-id="7ff88-232">Optional</span></span><br><span data-ttu-id="7ff88-233">外部キー : mshr_hcmveteranstatusentity の mshr_hcmveteranstatusentityid</span><span class="sxs-lookup"><span data-stu-id="7ff88-233">Foreign key: mshr_hcmveteranstatusentityid of mshr_hcmveteranstatusentity</span></span> | <span data-ttu-id="7ff88-234">システムが生成した、退役者の状態エンティティ レコードの一意識別子。</span><span class="sxs-lookup"><span data-stu-id="7ff88-234">System-generated unique identifier for the veteran status entity record.</span></span> |
| <span data-ttu-id="7ff88-235">**兵役の開始日**</span><span class="sxs-lookup"><span data-stu-id="7ff88-235">**Military Service Start Date**</span></span><br><span data-ttu-id="7ff88-236">mshr_militaryservicestartdate</span><span class="sxs-lookup"><span data-stu-id="7ff88-236">mshr_militaryservicestartdate</span></span><br><span data-ttu-id="7ff88-237">日時</span><span class="sxs-lookup"><span data-stu-id="7ff88-237">Datetime</span></span> | <span data-ttu-id="7ff88-238">読み取り/書き込み</span><span class="sxs-lookup"><span data-stu-id="7ff88-238">Read/write</span></span><br><span data-ttu-id="7ff88-239">オプション</span><span class="sxs-lookup"><span data-stu-id="7ff88-239">Optional</span></span> | <span data-ttu-id="7ff88-240">候補者の兵役開始日。</span><span class="sxs-lookup"><span data-stu-id="7ff88-240">The start date of the candidate’s military service.</span></span> |
| <span data-ttu-id="7ff88-241">**兵役の終了日**</span><span class="sxs-lookup"><span data-stu-id="7ff88-241">**Military Service End Date**</span></span><br><span data-ttu-id="7ff88-242">mshr_militaryserviceenddate</span><span class="sxs-lookup"><span data-stu-id="7ff88-242">mshr_militaryserviceenddate</span></span><br><span data-ttu-id="7ff88-243">日時</span><span class="sxs-lookup"><span data-stu-id="7ff88-243">Datetime</span></span> | <span data-ttu-id="7ff88-244">読み取り/書き込み</span><span class="sxs-lookup"><span data-stu-id="7ff88-244">Read/write</span></span><br><span data-ttu-id="7ff88-245">オプション</span><span class="sxs-lookup"><span data-stu-id="7ff88-245">Optional</span></span> | <span data-ttu-id="7ff88-246">候補者の兵役終了日。</span><span class="sxs-lookup"><span data-stu-id="7ff88-246">The end date of the candidate’s military service.</span></span> |
| <span data-ttu-id="7ff88-247">**退役傷病軍人かどうか**</span><span class="sxs-lookup"><span data-stu-id="7ff88-247">**Is Disabled Veteran**</span></span><br><span data-ttu-id="7ff88-248">mshr_isdisabledveteran</span><span class="sxs-lookup"><span data-stu-id="7ff88-248">mshr_isdisabledveteran</span></span><br><span data-ttu-id="7ff88-249">mshr_noyes オプション セット</span><span class="sxs-lookup"><span data-stu-id="7ff88-249">mshr_noyes option set</span></span> | <span data-ttu-id="7ff88-250">読み取り/書き込み</span><span class="sxs-lookup"><span data-stu-id="7ff88-250">Read/write</span></span><br><span data-ttu-id="7ff88-251">オプション</span><span class="sxs-lookup"><span data-stu-id="7ff88-251">Optional</span></span> | <span data-ttu-id="7ff88-252">候補者が退役者の資格を持っているかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="7ff88-252">Indicates if the candidate has disabled veteran status.</span></span> |
| <span data-ttu-id="7ff88-253">**使用可能日**</span><span class="sxs-lookup"><span data-stu-id="7ff88-253">**Availability Date**</span></span><br><span data-ttu-id="7ff88-254">mshr_availabilitydate</span><span class="sxs-lookup"><span data-stu-id="7ff88-254">mshr_availabilitydate</span></span><br><span data-ttu-id="7ff88-255">日時</span><span class="sxs-lookup"><span data-stu-id="7ff88-255">Datetime</span></span> | <span data-ttu-id="7ff88-256">読み取り/書き込み</span><span class="sxs-lookup"><span data-stu-id="7ff88-256">Read/write</span></span><br><span data-ttu-id="7ff88-257">オプション</span><span class="sxs-lookup"><span data-stu-id="7ff88-257">Optional</span></span> | <span data-ttu-id="7ff88-258">候補者が勤務可能な最も早い日付。</span><span class="sxs-lookup"><span data-stu-id="7ff88-258">The earliest date the candidate would be available to work.</span></span> |
| <span data-ttu-id="7ff88-259">**配置転換の意思あり**</span><span class="sxs-lookup"><span data-stu-id="7ff88-259">**Is Willing To Relocate**</span></span><br><span data-ttu-id="7ff88-260">mshr_iswillingtorelocate</span><span class="sxs-lookup"><span data-stu-id="7ff88-260">mshr_iswillingtorelocate</span></span><br><span data-ttu-id="7ff88-261">mshr_noyes オプション セット</span><span class="sxs-lookup"><span data-stu-id="7ff88-261">mshr_noyes option set</span></span> | <span data-ttu-id="7ff88-262">読み取り/書き込み</span><span class="sxs-lookup"><span data-stu-id="7ff88-262">Read/write</span></span><br><span data-ttu-id="7ff88-263">オプション</span><span class="sxs-lookup"><span data-stu-id="7ff88-263">Optional</span></span> | <span data-ttu-id="7ff88-264">候補者がそのポジションのために転勤する意思があるかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="7ff88-264">Indicates whether the candidate is willing to relocate for the position.</span></span> |
| <span data-ttu-id="7ff88-265">**備考**</span><span class="sxs-lookup"><span data-stu-id="7ff88-265">**Comments**</span></span><br><span data-ttu-id="7ff88-266">mshr_comments</span><span class="sxs-lookup"><span data-stu-id="7ff88-266">mshr_comments</span></span><br><span data-ttu-id="7ff88-267">文字列</span><span class="sxs-lookup"><span data-stu-id="7ff88-267">String</span></span> | <span data-ttu-id="7ff88-268">読み取り/書き込み</span><span class="sxs-lookup"><span data-stu-id="7ff88-268">Read/write</span></span><br><span data-ttu-id="7ff88-269">オプション</span><span class="sxs-lookup"><span data-stu-id="7ff88-269">Optional</span></span> | <span data-ttu-id="7ff88-270">採用担当者、または採用マネージャが使用するコメント。</span><span class="sxs-lookup"><span data-stu-id="7ff88-270">Comments to be used by the recruiter or hiring manager.</span></span> |
| <span data-ttu-id="7ff88-271">**アプリケーションの統合結果**</span><span class="sxs-lookup"><span data-stu-id="7ff88-271">**Application Integration Result**</span></span><br><span data-ttu-id="7ff88-272">mshr_applcantintegrationresult</span><span class="sxs-lookup"><span data-stu-id="7ff88-272">mshr_applcantintegrationresult</span></span><br><span data-ttu-id="7ff88-273">mshr_applicantintegrationresult オプションセット</span><span class="sxs-lookup"><span data-stu-id="7ff88-273">mshr_applicantintegrationresult option set</span></span> | <span data-ttu-id="7ff88-274">読み取り/書き込み</span><span class="sxs-lookup"><span data-stu-id="7ff88-274">Read/write</span></span><br><span data-ttu-id="7ff88-275">必須</span><span class="sxs-lookup"><span data-stu-id="7ff88-275">Required</span></span> | <span data-ttu-id="7ff88-276">統合に関連する採用プロセスにおける候補者の状態。</span><span class="sxs-lookup"><span data-stu-id="7ff88-276">The status of the candidate in the hiring process related to the integration.</span></span> |
| <span data-ttu-id="7ff88-277">**不採用理由コード ID**</span><span class="sxs-lookup"><span data-stu-id="7ff88-277">**Do Not Hire Reason Code ID**</span></span><br><span data-ttu-id="7ff88-278">mshr_donothirereasoncodeid</span><span class="sxs-lookup"><span data-stu-id="7ff88-278">mshr_donothirereasoncodeid</span></span><br><span data-ttu-id="7ff88-279">文字列</span><span class="sxs-lookup"><span data-stu-id="7ff88-279">String</span></span> | <span data-ttu-id="7ff88-280">読み取り/書き込み</span><span class="sxs-lookup"><span data-stu-id="7ff88-280">Read/write</span></span><br><span data-ttu-id="7ff88-281">オプション</span><span class="sxs-lookup"><span data-stu-id="7ff88-281">Optional</span></span> | <span data-ttu-id="7ff88-282">状態 (アプリケーション統合結果) が [採用されていない] に設定されている場合に、任意で指定される理由コードです。</span><span class="sxs-lookup"><span data-stu-id="7ff88-282">A reason code optionally provided when the status (application integration result) is set to “Not hired”.</span></span> |
| <span data-ttu-id="7ff88-283">**理由コード ID の値**</span><span class="sxs-lookup"><span data-stu-id="7ff88-283">**Reason Code ID Value**</span></span><br><span data-ttu-id="7ff88-284">_mshr_fk_reasoncode_id_value</span><span class="sxs-lookup"><span data-stu-id="7ff88-284">_mshr_fk_reasoncode_id_value</span></span><br><span data-ttu-id="7ff88-285">GUID</span><span class="sxs-lookup"><span data-stu-id="7ff88-285">GUID</span></span> | <span data-ttu-id="7ff88-286">読み取り専用</span><span class="sxs-lookup"><span data-stu-id="7ff88-286">Read-only</span></span><br><span data-ttu-id="7ff88-287">オプション</span><span class="sxs-lookup"><span data-stu-id="7ff88-287">Optional</span></span><br><span data-ttu-id="7ff88-288">外部キー : mshr_hcmreasoncodeentity entity の mshr_hcmreasoncodeentityid</span><span class="sxs-lookup"><span data-stu-id="7ff88-288">Foreign key: mshr_hcmreasoncodeentityid of mshr_hcmreasoncodeentity entity</span></span> | <span data-ttu-id="7ff88-289">**採用しない** 理由コードに対してシステムが生成する一意識別子。</span><span class="sxs-lookup"><span data-stu-id="7ff88-289">System-generated unique identifier for the **Do Not Hire** reason code.</span></span> |
| <span data-ttu-id="7ff88-290">**データ領域 ID**</span><span class="sxs-lookup"><span data-stu-id="7ff88-290">**Data Area ID**</span></span><br><span data-ttu-id="7ff88-291">mshr_dataareaid</span><span class="sxs-lookup"><span data-stu-id="7ff88-291">mshr_dataareaid</span></span><br><span data-ttu-id="7ff88-292">文字列</span><span class="sxs-lookup"><span data-stu-id="7ff88-292">String</span></span> | <span data-ttu-id="7ff88-293">読み取り/書き込み</span><span class="sxs-lookup"><span data-stu-id="7ff88-293">Read/write</span></span><br><span data-ttu-id="7ff88-294">オプション</span><span class="sxs-lookup"><span data-stu-id="7ff88-294">Optional</span></span> |  <span data-ttu-id="7ff88-295">法人 (会社) を指定します。</span><span class="sxs-lookup"><span data-stu-id="7ff88-295">Specifies the legal entity (company).</span></span> |
| <span data-ttu-id="7ff88-296">**データ領域 ID 値**</span><span class="sxs-lookup"><span data-stu-id="7ff88-296">**Data Area ID Value**</span></span><br><span data-ttu-id="7ff88-297">_mshr_dataareaid_id_value</span><span class="sxs-lookup"><span data-stu-id="7ff88-297">_mshr_dataareaid_id_value</span></span><br><span data-ttu-id="7ff88-298">GUID</span><span class="sxs-lookup"><span data-stu-id="7ff88-298">GUID</span></span> | <span data-ttu-id="7ff88-299">読み取り専用</span><span class="sxs-lookup"><span data-stu-id="7ff88-299">Read-only</span></span><br><span data-ttu-id="7ff88-300">オプション</span><span class="sxs-lookup"><span data-stu-id="7ff88-300">Optional</span></span><br><span data-ttu-id="7ff88-301">外部キー : cdm_companyid of cdm_company エンティティ</span><span class="sxs-lookup"><span data-stu-id="7ff88-301">Foreign key: cdm_companyid of cdm_company entity</span></span> | <span data-ttu-id="7ff88-302">システムが生成する、法人 (会社) を識別する GUID 値です。</span><span class="sxs-lookup"><span data-stu-id="7ff88-302">System-generated GUID value identifying the legal entity (company).</span></span> |

## <a name="see-also"></a><span data-ttu-id="7ff88-303">参照</span><span class="sxs-lookup"><span data-stu-id="7ff88-303">See also</span></span>

[<span data-ttu-id="7ff88-304">申請者追跡システム統合APIの概要</span><span class="sxs-lookup"><span data-stu-id="7ff88-304">Applicant Tracking System integration API introduction</span></span>](hr-admin-integration-ats-api-introduction.md)<br>
[<span data-ttu-id="7ff88-305">採用する採用候補者に対するクエリの例</span><span class="sxs-lookup"><span data-stu-id="7ff88-305">Example query for Candidate to hire</span></span>](hr-admin-integration-ats-api-candidate-to-hire-example-query.md)