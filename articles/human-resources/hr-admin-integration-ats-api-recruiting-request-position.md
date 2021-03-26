---
title: 採用要求職位
description: このトピックでは、Dynamics 365 Human Resources の採用要求職位のエンティティについて説明します。
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
ms.openlocfilehash: 01d73d390f72343c7498ccbb99838d38be45a19e
ms.sourcegitcommit: 33b5c8bc4f9461e290513aa22de1ec1fba3b0742
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/05/2021
ms.locfileid: "5126029"
---
# <a name="recruiting-request-position"></a><span data-ttu-id="e8d68-103">採用要求職位</span><span class="sxs-lookup"><span data-stu-id="e8d68-103">Recruiting request position</span></span>

<span data-ttu-id="e8d68-104">このトピックでは、Dynamics 365 Human Resources の採用要求職位のエンティティについて説明します。</span><span class="sxs-lookup"><span data-stu-id="e8d68-104">This topic describes the Recruiting request position entity for Dynamics 365 Human Resources.</span></span>

<span data-ttu-id="e8d68-105">物理名 : mshr_hcmrecruitingrequestpositionentity</span><span class="sxs-lookup"><span data-stu-id="e8d68-105">Physical name: mshr_hcmrecruitingrequestpositionentity</span></span>

### <a name="description"></a><span data-ttu-id="e8d68-106">説明</span><span class="sxs-lookup"><span data-stu-id="e8d68-106">Description</span></span>

<span data-ttu-id="e8d68-107">採用要求に対応する職位についての説明です。</span><span class="sxs-lookup"><span data-stu-id="e8d68-107">Describes the position or positions to fill for a recruiting request.</span></span> <span data-ttu-id="e8d68-108">採用要求への職位の追加はオプションです。</span><span class="sxs-lookup"><span data-stu-id="e8d68-108">Adding a position to the recruiting request is optional.</span></span> <span data-ttu-id="e8d68-109">職位のプロパティは、職位マスター レコード上のものとは異なり、採用要求上では異なってはいけないため、職位のプロパティは読み取り専用です。</span><span class="sxs-lookup"><span data-stu-id="e8d68-109">The properties of the position are read-only, as the position properties shouldn't be different on the recruiting request than they are on the position master record.</span></span> <span data-ttu-id="e8d68-110">プロパティを変更する必要がある場合は、採用要求に職位を追加する前に、職位マスターレコード上で行う必要があります。</span><span class="sxs-lookup"><span data-stu-id="e8d68-110">If the properties need to change, it should be done on the position master record before adding the position to the recruiting request.</span></span>

### <a name="json-representation"></a><span data-ttu-id="e8d68-111">JSON 表記</span><span class="sxs-lookup"><span data-stu-id="e8d68-111">JSON representation</span></span>
```json
{
    "mshr_recruitingrequestid": "String",
    "mshr_positionid": "String",
    "mshr_description": "String",
    "mshr_positiontypeid": "String",
    "mshr_status": Int,
    "mshr_departmentnumber": "String",
    "mshr_reportstopositionid": "String",
    "mshr_reportstopersonnelnumber": "String",
    "mshr_financialdimension": "String",
    "mshr_dataareaid": "String",
    "_mshr_dataareaid_id_value": "Guid",
    "mshr_primaryfield": "String",
    "_mshr_fk_recruitingrequest_id_value": "Guid",
    "_mshr_fk_position_id_value": "Guid",
    "_mshr_fk_positiontype_id_value": "Guid",
    "_mshr_fk_department_id_value": "Guid",
    "_mshr_fk_reportstoposition_id_value": "Guid",
    "_mshr_fk_reportstoworker_id_value": "Guid",
    "mshr_hcmrecruitingrequestpositionentityid": "Guid"
}
```

### <a name="properties"></a><span data-ttu-id="e8d68-112">プロパティ</span><span class="sxs-lookup"><span data-stu-id="e8d68-112">Properties</span></span>

| <span data-ttu-id="e8d68-113">プロパティ</span><span class="sxs-lookup"><span data-stu-id="e8d68-113">Property</span></span><br><span data-ttu-id="e8d68-114">**現物名**</span><span class="sxs-lookup"><span data-stu-id="e8d68-114">**Physical name**</span></span><br><span data-ttu-id="e8d68-115">**_種類_**</span><span class="sxs-lookup"><span data-stu-id="e8d68-115">**_Type_**</span></span> | <span data-ttu-id="e8d68-116">使用</span><span class="sxs-lookup"><span data-stu-id="e8d68-116">Use</span></span> | <span data-ttu-id="e8d68-117">説明</span><span class="sxs-lookup"><span data-stu-id="e8d68-117">Description</span></span> |
| --- | --- | --- |
| <span data-ttu-id="e8d68-118">**採用で要求する職位のエンティティ ID**</span><span class="sxs-lookup"><span data-stu-id="e8d68-118">**Recruiting Request Position Entity ID**</span></span><br><span data-ttu-id="e8d68-119">mshr_hcmrecruitingrequestpositionentityid</span><span class="sxs-lookup"><span data-stu-id="e8d68-119">mshr_hcmrecruitingrequestpositionentityid</span></span><br><span data-ttu-id="e8d68-120">*GUID*</span><span class="sxs-lookup"><span data-stu-id="e8d68-120">*GUID*</span></span> | <span data-ttu-id="e8d68-121">読み取り専用</span><span class="sxs-lookup"><span data-stu-id="e8d68-121">Read-only</span></span><br><span data-ttu-id="e8d68-122">必須</span><span class="sxs-lookup"><span data-stu-id="e8d68-122">Required</span></span> |    <span data-ttu-id="e8d68-123">システムが生成する、採用で要求する職位レコードの識別子です。</span><span class="sxs-lookup"><span data-stu-id="e8d68-123">System-generated identifier of the recruiting request position record.</span></span> |
| <span data-ttu-id="e8d68-124">**採用要求 ID**</span><span class="sxs-lookup"><span data-stu-id="e8d68-124">**Recruiting Request ID**</span></span><br><span data-ttu-id="e8d68-125">mshr_recruitingrequestid</span><span class="sxs-lookup"><span data-stu-id="e8d68-125">mshr_recruitingrequestid</span></span><br><span data-ttu-id="e8d68-126">*文字列*</span><span class="sxs-lookup"><span data-stu-id="e8d68-126">*String*</span></span> | <span data-ttu-id="e8d68-127">1回書き込み</span><span class="sxs-lookup"><span data-stu-id="e8d68-127">Write-once</span></span><br><span data-ttu-id="e8d68-128">必須</span><span class="sxs-lookup"><span data-stu-id="e8d68-128">Required</span></span> | <span data-ttu-id="e8d68-129">読み取り可能な、採用要求の一意識別子です。</span><span class="sxs-lookup"><span data-stu-id="e8d68-129">The user-readable unique identifier of the recruiting request.</span></span> |
| <span data-ttu-id="e8d68-130">**採用要求 ID 値**</span><span class="sxs-lookup"><span data-stu-id="e8d68-130">**Recruiting Request ID Value**</span></span><br><span data-ttu-id="e8d68-131">_mshr_fk_recruitingrequest_id_value</span><span class="sxs-lookup"><span data-stu-id="e8d68-131">_mshr_fk_recruitingrequest_id_value</span></span><br><span data-ttu-id="e8d68-132">*GUID*</span><span class="sxs-lookup"><span data-stu-id="e8d68-132">*GUID*</span></span> | <span data-ttu-id="e8d68-133">読み取り専用</span><span class="sxs-lookup"><span data-stu-id="e8d68-133">Read-only</span></span><br><span data-ttu-id="e8d68-134">必須</span><span class="sxs-lookup"><span data-stu-id="e8d68-134">Required</span></span><br><span data-ttu-id="e8d68-135">外部キー : mshr_hcmrecruitingrequestentity エンティの mshr_hcmrecruitingrequestentityid</span><span class="sxs-lookup"><span data-stu-id="e8d68-135">Foreign key: mshr_hcmrecruitingrequestentityid of mshr_hcmrecruitingrequestentity entity</span></span> | <span data-ttu-id="e8d68-136">システムが生成する、職位が割り当てられている採用要求の識別子です。</span><span class="sxs-lookup"><span data-stu-id="e8d68-136">System-generated identifier of the recruiting request to which the position is assigned.</span></span> |
| <span data-ttu-id="e8d68-137">**職位 ID**</span><span class="sxs-lookup"><span data-stu-id="e8d68-137">**Position ID**</span></span><br><span data-ttu-id="e8d68-138">mshr_positionid</span><span class="sxs-lookup"><span data-stu-id="e8d68-138">mshr_positionid</span></span><br><span data-ttu-id="e8d68-139">*文字列*</span><span class="sxs-lookup"><span data-stu-id="e8d68-139">*String*</span></span> | <span data-ttu-id="e8d68-140">1回書き込み</span><span class="sxs-lookup"><span data-stu-id="e8d68-140">Write-once</span></span><br><span data-ttu-id="e8d68-141">必須</span><span class="sxs-lookup"><span data-stu-id="e8d68-141">Required</span></span> | <span data-ttu-id="e8d68-142">読み取り可能な、職位の一意識別子です。</span><span class="sxs-lookup"><span data-stu-id="e8d68-142">The user-readable unique identifier of the position.</span></span> |
| <span data-ttu-id="e8d68-143">**ポジション ID の値**</span><span class="sxs-lookup"><span data-stu-id="e8d68-143">**Position ID Value**</span></span><br><span data-ttu-id="e8d68-144">_mshr_fk_position_id_value</span><span class="sxs-lookup"><span data-stu-id="e8d68-144">_mshr_fk_position_id_value</span></span><br><span data-ttu-id="e8d68-145">*GUID*</span><span class="sxs-lookup"><span data-stu-id="e8d68-145">*GUID*</span></span> | <span data-ttu-id="e8d68-146">読み取り専用</span><span class="sxs-lookup"><span data-stu-id="e8d68-146">Read-only</span></span><br><span data-ttu-id="e8d68-147">必須</span><span class="sxs-lookup"><span data-stu-id="e8d68-147">Required</span></span><br><span data-ttu-id="e8d68-148">外部キー : mshr_hcmpositionv2entity エンティティの mshr_hcmpositionv2entityid</span><span class="sxs-lookup"><span data-stu-id="e8d68-148">Foreign key: mshr_hcmpositionv2entityid of mshr_hcmpositionv2entity entity</span></span> | <span data-ttu-id="e8d68-149">システムが生成する職位の識別子です。</span><span class="sxs-lookup"><span data-stu-id="e8d68-149">System-generated identifier of the position.</span></span> |
| <span data-ttu-id="e8d68-150">**説明**</span><span class="sxs-lookup"><span data-stu-id="e8d68-150">**Description**</span></span><br><span data-ttu-id="e8d68-151">mshr_description</span><span class="sxs-lookup"><span data-stu-id="e8d68-151">mshr_description</span></span><br><span data-ttu-id="e8d68-152">*文字列*</span><span class="sxs-lookup"><span data-stu-id="e8d68-152">*String*</span></span> | <span data-ttu-id="e8d68-153">読み取り専用</span><span class="sxs-lookup"><span data-stu-id="e8d68-153">Read-only</span></span><br><span data-ttu-id="e8d68-154">必須</span><span class="sxs-lookup"><span data-stu-id="e8d68-154">Required</span></span> | <span data-ttu-id="e8d68-155">職位の説明です。</span><span class="sxs-lookup"><span data-stu-id="e8d68-155">The position description.</span></span> |
| <span data-ttu-id="e8d68-156">**職位タイプ ID**</span><span class="sxs-lookup"><span data-stu-id="e8d68-156">**Position Type ID**</span></span><br><span data-ttu-id="e8d68-157">mshr_positiontypeid</span><span class="sxs-lookup"><span data-stu-id="e8d68-157">mshr_positiontypeid</span></span><br><span data-ttu-id="e8d68-158">*文字列*</span><span class="sxs-lookup"><span data-stu-id="e8d68-158">*String*</span></span> | <span data-ttu-id="e8d68-159">読み取り専用</span><span class="sxs-lookup"><span data-stu-id="e8d68-159">Read-only</span></span><br><span data-ttu-id="e8d68-160">オプション</span><span class="sxs-lookup"><span data-stu-id="e8d68-160">Optional</span></span> | <span data-ttu-id="e8d68-161">読み取り可能な、この職位タイプの一意識別子です。</span><span class="sxs-lookup"><span data-stu-id="e8d68-161">The user-readable unique identifier of the position type for this position.</span></span> |
| <span data-ttu-id="e8d68-162">**職位タイプ ID 値**</span><span class="sxs-lookup"><span data-stu-id="e8d68-162">**Position Type ID Value**</span></span><br><span data-ttu-id="e8d68-163">_mshr_fk_positiontype_id_value</span><span class="sxs-lookup"><span data-stu-id="e8d68-163">_mshr_fk_positiontype_id_value</span></span><br><span data-ttu-id="e8d68-164">*GUID*</span><span class="sxs-lookup"><span data-stu-id="e8d68-164">*GUID*</span></span> | <span data-ttu-id="e8d68-165">読み取り専用</span><span class="sxs-lookup"><span data-stu-id="e8d68-165">Read-only</span></span><br><span data-ttu-id="e8d68-166">オプション</span><span class="sxs-lookup"><span data-stu-id="e8d68-166">Optional</span></span><br><span data-ttu-id="e8d68-167">外部キー : mshr_hcmpositiontypeentity エンティティの mshr_hcmpositiontypeentityid</span><span class="sxs-lookup"><span data-stu-id="e8d68-167">Foreign key: mshr_hcmpositiontypeentityid of mshr_hcmpositiontypeentity entity</span></span> | <span data-ttu-id="e8d68-168">システムが生成する、この職位タイプの一意識別子です。</span><span class="sxs-lookup"><span data-stu-id="e8d68-168">A system-generated unique identifier of the position type for this position.</span></span> |
| <span data-ttu-id="e8d68-169">**状態**</span><span class="sxs-lookup"><span data-stu-id="e8d68-169">**Status**</span></span><br><span data-ttu-id="e8d68-170">mshr_status</span><span class="sxs-lookup"><span data-stu-id="e8d68-170">mshr_status</span></span><br><span data-ttu-id="e8d68-171">*RecruitingRequestPositionStatus* オプション セット</span><span class="sxs-lookup"><span data-stu-id="e8d68-171">*RecruitingRequestPositionStatus* option set</span></span> | <span data-ttu-id="e8d68-172">読み取り/書き込み</span><span class="sxs-lookup"><span data-stu-id="e8d68-172">Read/write</span></span><br><span data-ttu-id="e8d68-173">必須</span><span class="sxs-lookup"><span data-stu-id="e8d68-173">Required</span></span> | <span data-ttu-id="e8d68-174">採用要求の職位の状態を示します。</span><span class="sxs-lookup"><span data-stu-id="e8d68-174">Status of the position for the recruiting request.</span></span> |
| <span data-ttu-id="e8d68-175">**部門番号**</span><span class="sxs-lookup"><span data-stu-id="e8d68-175">**Department Number**</span></span><br><span data-ttu-id="e8d68-176">mshr_departmentnumber</span><span class="sxs-lookup"><span data-stu-id="e8d68-176">mshr_departmentnumber</span></span><br><span data-ttu-id="e8d68-177">*文字列*</span><span class="sxs-lookup"><span data-stu-id="e8d68-177">*String*</span></span> | <span data-ttu-id="e8d68-178">読み取り専用</span><span class="sxs-lookup"><span data-stu-id="e8d68-178">Read-only</span></span><br><span data-ttu-id="e8d68-179">オプション</span><span class="sxs-lookup"><span data-stu-id="e8d68-179">Optional</span></span><br> | <span data-ttu-id="e8d68-180">職位の部門番号です。</span><span class="sxs-lookup"><span data-stu-id="e8d68-180">The department number of the position.</span></span> |
| <span data-ttu-id="e8d68-181">**部門 ID 値**</span><span class="sxs-lookup"><span data-stu-id="e8d68-181">**Department ID Value**</span></span><br><span data-ttu-id="e8d68-182">_mshr_fk_department_id_value</span><span class="sxs-lookup"><span data-stu-id="e8d68-182">_mshr_fk_department_id_value</span></span><br><span data-ttu-id="e8d68-183">*GUID*</span><span class="sxs-lookup"><span data-stu-id="e8d68-183">*GUID*</span></span> | <span data-ttu-id="e8d68-184">読み取り専用</span><span class="sxs-lookup"><span data-stu-id="e8d68-184">Read-only</span></span><br><span data-ttu-id="e8d68-185">オプション</span><span class="sxs-lookup"><span data-stu-id="e8d68-185">Optional</span></span><br><span data-ttu-id="e8d68-186">外部キー : mshr_omdepartmententity entity の mshr_omdepartmententityid</span><span class="sxs-lookup"><span data-stu-id="e8d68-186">Foreign key: mshr_omdepartmententityid of mshr_omdepartmententity entity</span></span> | <span data-ttu-id="e8d68-187">システムが生成する、職位が属する部門の一意識別子です。</span><span class="sxs-lookup"><span data-stu-id="e8d68-187">System-generated unique identifier of the department of the position.</span></span> |
| <span data-ttu-id="e8d68-188">**報告先の職位 ID**</span><span class="sxs-lookup"><span data-stu-id="e8d68-188">**Reports To Position ID**</span></span><br><span data-ttu-id="e8d68-189">mshr_reportstopositionid</span><span class="sxs-lookup"><span data-stu-id="e8d68-189">mshr_reportstopositionid</span></span><br><span data-ttu-id="e8d68-190">*文字列*</span><span class="sxs-lookup"><span data-stu-id="e8d68-190">*String*</span></span> | <span data-ttu-id="e8d68-191">読み取り専用</span><span class="sxs-lookup"><span data-stu-id="e8d68-191">Read-only</span></span><br><span data-ttu-id="e8d68-192">必須</span><span class="sxs-lookup"><span data-stu-id="e8d68-192">Required</span></span> | <span data-ttu-id="e8d68-193">ユーザーが読み取り可能な、組織階層の中で、採用された職位が所属する職位の ID です。</span><span class="sxs-lookup"><span data-stu-id="e8d68-193">The user-readable ID of the position to which the recruited position reports in the organizational hierarchy.</span></span> |
| <span data-ttu-id="e8d68-194">**所属する職位 ID の値**</span><span class="sxs-lookup"><span data-stu-id="e8d68-194">**Reports To Position ID Value**</span></span><br><span data-ttu-id="e8d68-195">_mshr_fk_reportstoposition_id_value</span><span class="sxs-lookup"><span data-stu-id="e8d68-195">_mshr_fk_reportstoposition_id_value</span></span><br><span data-ttu-id="e8d68-196">*GUID*</span><span class="sxs-lookup"><span data-stu-id="e8d68-196">*GUID*</span></span> | <span data-ttu-id="e8d68-197">読み取り専用</span><span class="sxs-lookup"><span data-stu-id="e8d68-197">Read-only</span></span><br><span data-ttu-id="e8d68-198">必須</span><span class="sxs-lookup"><span data-stu-id="e8d68-198">Required</span></span><br><span data-ttu-id="e8d68-199">外部キー : mshr_hcmpositionv2entity エンティティの mshr_hcmpositionv2entityid</span><span class="sxs-lookup"><span data-stu-id="e8d68-199">Foreign key: mshr_hcmpositionv2entityid of mshr_hcmpositionv2entity entity</span></span> | <span data-ttu-id="e8d68-200">システムが生成する、採用されたポジションが属する職位の ID です。</span><span class="sxs-lookup"><span data-stu-id="e8d68-200">The system-generated ID of the position to which the recruited position reports.</span></span> |
| <span data-ttu-id="e8d68-201">**個人番号に属する**</span><span class="sxs-lookup"><span data-stu-id="e8d68-201">**Reports To Personnel Number**</span></span><br><span data-ttu-id="e8d68-202">mshr_reportstopersonnelnumber</span><span class="sxs-lookup"><span data-stu-id="e8d68-202">mshr_reportstopersonnelnumber</span></span><br><span data-ttu-id="e8d68-203">*文字列*</span><span class="sxs-lookup"><span data-stu-id="e8d68-203">*String*</span></span> | <span data-ttu-id="e8d68-204">読み取り専用</span><span class="sxs-lookup"><span data-stu-id="e8d68-204">Read-only</span></span><br><span data-ttu-id="e8d68-205">必須</span><span class="sxs-lookup"><span data-stu-id="e8d68-205">Required</span></span> | <span data-ttu-id="e8d68-206">採用された候補者が属する従業員の従業員 ID です。</span><span class="sxs-lookup"><span data-stu-id="e8d68-206">The worker ID of the worker to which the hired candidate will report.</span></span> |
| <span data-ttu-id="e8d68-207">**所属する従業員 ID の値**</span><span class="sxs-lookup"><span data-stu-id="e8d68-207">**Reports To Worker ID Value**</span></span><br><span data-ttu-id="e8d68-208">_mshr_fk_reportstoworker_id_value</span><span class="sxs-lookup"><span data-stu-id="e8d68-208">_mshr_fk_reportstoworker_id_value</span></span><br><span data-ttu-id="e8d68-209">*GUID*</span><span class="sxs-lookup"><span data-stu-id="e8d68-209">*GUID*</span></span> | <span data-ttu-id="e8d68-210">読み取り専用</span><span class="sxs-lookup"><span data-stu-id="e8d68-210">Read-only</span></span><br><span data-ttu-id="e8d68-211">必須</span><span class="sxs-lookup"><span data-stu-id="e8d68-211">Required</span></span><br><span data-ttu-id="e8d68-212">外部キー : mshr_hcmworkerbaseentity entity の mshr_hcmworkerbaseentityid</span><span class="sxs-lookup"><span data-stu-id="e8d68-212">Foreign key: mshr_hcmworkerbaseentityid of mshr_hcmworkerbaseentity entity</span></span> | <span data-ttu-id="e8d68-213">システムが生成する、採用された候補者が属する従業員の ID です。</span><span class="sxs-lookup"><span data-stu-id="e8d68-213">System-generated ID of the worker to which the hired candidate will report.</span></span> |
| <span data-ttu-id="e8d68-214">**財務分析コード**</span><span class="sxs-lookup"><span data-stu-id="e8d68-214">**Financial Dimension**</span></span><br><span data-ttu-id="e8d68-215">mshr_financialdimension</span><span class="sxs-lookup"><span data-stu-id="e8d68-215">mshr_financialdimension</span></span><br><span data-ttu-id="e8d68-216">*文字列*</span><span class="sxs-lookup"><span data-stu-id="e8d68-216">*String*</span></span> | <span data-ttu-id="e8d68-217">読み取り専用</span><span class="sxs-lookup"><span data-stu-id="e8d68-217">Read-only</span></span><br><span data-ttu-id="e8d68-218">オプション</span><span class="sxs-lookup"><span data-stu-id="e8d68-218">Optional</span></span> | <span data-ttu-id="e8d68-219">職位に割り当てられている財務分析コード (原価センターなど)。</span><span class="sxs-lookup"><span data-stu-id="e8d68-219">The financial dimension (for example, cost center) assigned to the position.</span></span> <span data-ttu-id="e8d68-220">財務分析コードは、法人ごとの各職位に割り当てられます。</span><span class="sxs-lookup"><span data-stu-id="e8d68-220">The financial dimension is assigned for each position per legal entity.</span></span> <span data-ttu-id="e8d68-221">分析コードで定義された原価センターには、mshr_dimattributeomcostcenterentity エンティティからアクセス可能です。</span><span class="sxs-lookup"><span data-stu-id="e8d68-221">Cost centers that are defined in dimensions are accessible through the mshr_dimattributeomcostcenterentity entity.</span></span> |
| <span data-ttu-id="e8d68-222">**データ領域 ID**</span><span class="sxs-lookup"><span data-stu-id="e8d68-222">**Data Area ID**</span></span><br><span data-ttu-id="e8d68-223">mshr_dataareaid</span><span class="sxs-lookup"><span data-stu-id="e8d68-223">mshr_dataareaid</span></span><br><span data-ttu-id="e8d68-224">*文字列*</span><span class="sxs-lookup"><span data-stu-id="e8d68-224">*String*</span></span> | <span data-ttu-id="e8d68-225">読み取り/書き込み</span><span class="sxs-lookup"><span data-stu-id="e8d68-225">Read/write</span></span><br><span data-ttu-id="e8d68-226">オプション</span><span class="sxs-lookup"><span data-stu-id="e8d68-226">Optional</span></span> | <span data-ttu-id="e8d68-227">採用要求職位の法人 (会社) を指定します。</span><span class="sxs-lookup"><span data-stu-id="e8d68-227">Specifies the legal entity (company) for the recruiting request position.</span></span> |
| <span data-ttu-id="e8d68-228">**データ領域 ID 値**</span><span class="sxs-lookup"><span data-stu-id="e8d68-228">**Data Area ID Value**</span></span><br><span data-ttu-id="e8d68-229">_mshr_dataareaid_id_value</span><span class="sxs-lookup"><span data-stu-id="e8d68-229">_mshr_dataareaid_id_value</span></span><br><span data-ttu-id="e8d68-230">*GUID*</span><span class="sxs-lookup"><span data-stu-id="e8d68-230">*GUID*</span></span> | <span data-ttu-id="e8d68-231">読み取り専用</span><span class="sxs-lookup"><span data-stu-id="e8d68-231">Read-only</span></span><br><span data-ttu-id="e8d68-232">オプション</span><span class="sxs-lookup"><span data-stu-id="e8d68-232">Optional</span></span><br><span data-ttu-id="e8d68-233">外部キー : cdm_companyid of cdm_company エンティティ</span><span class="sxs-lookup"><span data-stu-id="e8d68-233">Foreign key: cdm_companyid of cdm_company entity</span></span> | <span data-ttu-id="e8d68-234">システムが生成する、要求された職位の採用を行う法人 (会社) を識別する GUID 値です。</span><span class="sxs-lookup"><span data-stu-id="e8d68-234">System-generated GUID value identifying the legal entity (company) for the recruiting request position.</span></span> |
| <span data-ttu-id="e8d68-235">**基本フィールド**</span><span class="sxs-lookup"><span data-stu-id="e8d68-235">**Primary Field**</span></span><br><span data-ttu-id="e8d68-236">mshr_primaryfield</span><span class="sxs-lookup"><span data-stu-id="e8d68-236">mshr_primaryfield</span></span><br><span data-ttu-id="e8d68-237">*文字列*</span><span class="sxs-lookup"><span data-stu-id="e8d68-237">*String*</span></span> | <span data-ttu-id="e8d68-238">読み取り専用</span><span class="sxs-lookup"><span data-stu-id="e8d68-238">Read-only</span></span><br><span data-ttu-id="e8d68-239">必須</span><span class="sxs-lookup"><span data-stu-id="e8d68-239">Required</span></span> | <span data-ttu-id="e8d68-240">レコードを一意に識別する別の方法としての採用要求値、職位 ID の連結です。</span><span class="sxs-lookup"><span data-stu-id="e8d68-240">Concatenation of Recruiting Request value and Position ID as another method to uniquely identify the record.</span></span> |

## <a name="see-also"></a><span data-ttu-id="e8d68-241">参照</span><span class="sxs-lookup"><span data-stu-id="e8d68-241">See also</span></span>

[<span data-ttu-id="e8d68-242">申請者追跡システム統合APIの概要</span><span class="sxs-lookup"><span data-stu-id="e8d68-242">Applicant Tracking System integration API introduction</span></span>](hr-admin-integration-ats-api-introduction.md)<br>
[<span data-ttu-id="e8d68-243">採用要求のクエリの例</span><span class="sxs-lookup"><span data-stu-id="e8d68-243">Example query for Recruiting request</span></span>](hr-admin-integration-ats-api-recruiting-request-example-query.md)
