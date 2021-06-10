---
title: 個人の審査
description: このトピックでは、Dynamics 365 Human Resources の人物の選考エンティティについて説明します。
author: jaredha
ms.date: 02/05/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: jaredha
ms.search.validFrom: 2021-02-05
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 9d29b26094e307c3f68d57f297ab3614f3a5ccae
ms.sourcegitcommit: 879ee8a10e6158885795dce4b3db5077540eec41
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/18/2021
ms.locfileid: "6059283"
---
# <a name="person-screening"></a><span data-ttu-id="ca3f3-103">個人の審査</span><span class="sxs-lookup"><span data-stu-id="ca3f3-103">Person screening</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="ca3f3-104">このトピックでは、Dynamics 365 Human Resources の人物の選考エンティティについて説明します。</span><span class="sxs-lookup"><span data-stu-id="ca3f3-104">This topic describes the Person screening entity for Dynamics 365 Human Resources.</span></span>

<span data-ttu-id="ca3f3-105">物理名 : mshr_hcmpersonscreeningentity</span><span class="sxs-lookup"><span data-stu-id="ca3f3-105">Physical name: mshr_hcmpersonscreeningentity</span></span>

## <a name="description"></a><span data-ttu-id="ca3f3-106">説明</span><span class="sxs-lookup"><span data-stu-id="ca3f3-106">Description</span></span>

<span data-ttu-id="ca3f3-107">このエンティティは、候補者が合格した、または採用に合格する必要がある選考を表します。</span><span class="sxs-lookup"><span data-stu-id="ca3f3-107">This entity describes screenings a candidate has passed or must pass for employment.</span></span>

## <a name="json-representation"></a><span data-ttu-id="ca3f3-108">JSON 表記</span><span class="sxs-lookup"><span data-stu-id="ca3f3-108">JSON representation</span></span>

```json
{
    "mshr_note": "String",
    "mshr_requiredby": "Date",
    "mshr_status": Int,
    "mshr_partynumber": "String",
    "mshr_screeningtypeid": "String",
    "mshr_primaryfield": "String",
    "_mshr_fk_person_id_value": "Guid",
    "mshr_hcmpersonscreeningentityid": "Guid",
    "mshr_completeddate": "Date"
}
```

## <a name="properties"></a><span data-ttu-id="ca3f3-109">プロパティ</span><span class="sxs-lookup"><span data-stu-id="ca3f3-109">Properties</span></span>

| <span data-ttu-id="ca3f3-110">プロパティ</span><span class="sxs-lookup"><span data-stu-id="ca3f3-110">Property</span></span><br><span data-ttu-id="ca3f3-111">**現物名**</span><span class="sxs-lookup"><span data-stu-id="ca3f3-111">**Physical name**</span></span><br><span data-ttu-id="ca3f3-112">**_種類_**</span><span class="sxs-lookup"><span data-stu-id="ca3f3-112">**_Type_**</span></span> | <span data-ttu-id="ca3f3-113">使用</span><span class="sxs-lookup"><span data-stu-id="ca3f3-113">Use</span></span> | <span data-ttu-id="ca3f3-114">説明</span><span class="sxs-lookup"><span data-stu-id="ca3f3-114">Description</span></span> |
| --- | --- | --- |
| <span data-ttu-id="ca3f3-115">**人物の選考エンティティ ID**</span><span class="sxs-lookup"><span data-stu-id="ca3f3-115">**Person Screening Entity ID**</span></span><br><span data-ttu-id="ca3f3-116">mshr_hcmpersonscreeningentityid</span><span class="sxs-lookup"><span data-stu-id="ca3f3-116">mshr_hcmpersonscreeningentityid</span></span><br><span data-ttu-id="ca3f3-117">*GUID*</span><span class="sxs-lookup"><span data-stu-id="ca3f3-117">*GUID*</span></span> | <span data-ttu-id="ca3f3-118">読み取り専用</span><span class="sxs-lookup"><span data-stu-id="ca3f3-118">Read-only</span></span><br><span data-ttu-id="ca3f3-119">必須</span><span class="sxs-lookup"><span data-stu-id="ca3f3-119">Required</span></span><br><span data-ttu-id="ca3f3-120">システム生成</span><span class="sxs-lookup"><span data-stu-id="ca3f3-120">System-generated</span></span> | <span data-ttu-id="ca3f3-121">人物の選考レコードの一意の基本識別子です。</span><span class="sxs-lookup"><span data-stu-id="ca3f3-121">Unique primary identifier for the person screening record.</span></span> |
| <span data-ttu-id="ca3f3-122">**関係者番号**</span><span class="sxs-lookup"><span data-stu-id="ca3f3-122">**Party Number**</span></span><br><span data-ttu-id="ca3f3-123">mshr_partynumber</span><span class="sxs-lookup"><span data-stu-id="ca3f3-123">mshr_partynumber</span></span><br><span data-ttu-id="ca3f3-124">*文字列*</span><span class="sxs-lookup"><span data-stu-id="ca3f3-124">*String*</span></span> | <span data-ttu-id="ca3f3-125">読み取り/書き込み</span><span class="sxs-lookup"><span data-stu-id="ca3f3-125">Read/write</span></span><br><span data-ttu-id="ca3f3-126">必須</span><span class="sxs-lookup"><span data-stu-id="ca3f3-126">Required</span></span> | <span data-ttu-id="ca3f3-127">候補者に関連付けられている関係者 (人物) 番号です。</span><span class="sxs-lookup"><span data-stu-id="ca3f3-127">The party (person) number associated with the candidate.</span></span> |
| <span data-ttu-id="ca3f3-128">**個人 ID の値**</span><span class="sxs-lookup"><span data-stu-id="ca3f3-128">**Person ID Value**</span></span><br><span data-ttu-id="ca3f3-129">_mshr_fk_person_id_value</span><span class="sxs-lookup"><span data-stu-id="ca3f3-129">_mshr_fk_person_id_value</span></span><br><span data-ttu-id="ca3f3-130">*GUID*</span><span class="sxs-lookup"><span data-stu-id="ca3f3-130">*GUID*</span></span> | <span data-ttu-id="ca3f3-131">読み取り専用</span><span class="sxs-lookup"><span data-stu-id="ca3f3-131">Read-only</span></span><br><span data-ttu-id="ca3f3-132">必須</span><span class="sxs-lookup"><span data-stu-id="ca3f3-132">Required</span></span><br><span data-ttu-id="ca3f3-133">外部キー : mshr_dirpersonentity の mshr_dirpersonentityid</span><span class="sxs-lookup"><span data-stu-id="ca3f3-133">Foreign key: mshr_dirpersonentityid of mshr_dirpersonentity</span></span> | <span data-ttu-id="ca3f3-134">システムが生成する、当事者 (個人) エンティティ レコードの識別子です。</span><span class="sxs-lookup"><span data-stu-id="ca3f3-134">The system-generated identifier of the party (person) entity record.</span></span> |
| <span data-ttu-id="ca3f3-135">**選考タイプ ID**</span><span class="sxs-lookup"><span data-stu-id="ca3f3-135">**Screening Type ID**</span></span><br><span data-ttu-id="ca3f3-136">mshr_screeningtypeid</span><span class="sxs-lookup"><span data-stu-id="ca3f3-136">mshr_screeningtypeid</span></span><br><span data-ttu-id="ca3f3-137">*文字列*</span><span class="sxs-lookup"><span data-stu-id="ca3f3-137">*String*</span></span> | <span data-ttu-id="ca3f3-138">読み取り/書き込み</span><span class="sxs-lookup"><span data-stu-id="ca3f3-138">Read/write</span></span><br><span data-ttu-id="ca3f3-139">必須</span><span class="sxs-lookup"><span data-stu-id="ca3f3-139">Required</span></span><br><span data-ttu-id="ca3f3-140">外部キー : 選考タイプ</span><span class="sxs-lookup"><span data-stu-id="ca3f3-140">Foreign key: ScreeningType</span></span> | <span data-ttu-id="ca3f3-141">Human Resources で定義されている選考タイプの ID です。</span><span class="sxs-lookup"><span data-stu-id="ca3f3-141">The identifier of the screening type defined in Human Resources.</span></span> |
| <span data-ttu-id="ca3f3-142">**選考タイプ ID 値**</span><span class="sxs-lookup"><span data-stu-id="ca3f3-142">**Screening Type ID Value**</span></span><br><span data-ttu-id="ca3f3-143">_mshr_fk_screeningtype_id_value</span><span class="sxs-lookup"><span data-stu-id="ca3f3-143">_mshr_fk_screeningtype_id_value</span></span><br><span data-ttu-id="ca3f3-144">*GUID*</span><span class="sxs-lookup"><span data-stu-id="ca3f3-144">*GUID*</span></span> | <span data-ttu-id="ca3f3-145">読み取り専用</span><span class="sxs-lookup"><span data-stu-id="ca3f3-145">Read-only</span></span><br><span data-ttu-id="ca3f3-146">必須</span><span class="sxs-lookup"><span data-stu-id="ca3f3-146">Required</span></span><br><span data-ttu-id="ca3f3-147">外部キー : mshr_hcmscreeningtypeentity の mshr_hcmscreeningtypeentityid</span><span class="sxs-lookup"><span data-stu-id="ca3f3-147">Foreign key: mshr_hcmscreeningtypeentityid of mshr_hcmscreeningtypeentity</span></span> | <span data-ttu-id="ca3f3-148">関連するエンティティの選考タイプ レコーに向けてシステムが生成して識別子です。</span><span class="sxs-lookup"><span data-stu-id="ca3f3-148">System-generated identifier for the screening type record in the associated entity.</span></span> |
| <span data-ttu-id="ca3f3-149">**期日**</span><span class="sxs-lookup"><span data-stu-id="ca3f3-149">**Required By**</span></span><br><span data-ttu-id="ca3f3-150">mshr_requiredby</span><span class="sxs-lookup"><span data-stu-id="ca3f3-150">mshr_requiredby</span></span><br><span data-ttu-id="ca3f3-151">*Datetime*</span><span class="sxs-lookup"><span data-stu-id="ca3f3-151">*Datetime*</span></span> | <span data-ttu-id="ca3f3-152">読み取り/書き込み</span><span class="sxs-lookup"><span data-stu-id="ca3f3-152">Read/write</span></span><br><span data-ttu-id="ca3f3-153">オプション</span><span class="sxs-lookup"><span data-stu-id="ca3f3-153">Optional</span></span> | <span data-ttu-id="ca3f3-154">選考を完了する必要がある期日です。</span><span class="sxs-lookup"><span data-stu-id="ca3f3-154">The date by which the screening is required to be completed.</span></span> |
| <span data-ttu-id="ca3f3-155">**状態**</span><span class="sxs-lookup"><span data-stu-id="ca3f3-155">**Status**</span></span><br><span data-ttu-id="ca3f3-156">mshr_status</span><span class="sxs-lookup"><span data-stu-id="ca3f3-156">mshr_status</span></span><br><span data-ttu-id="ca3f3-157">*mshr_hcmcompletionstatus オプション セット*</span><span class="sxs-lookup"><span data-stu-id="ca3f3-157">*mshr_hcmcompletionstatus option set*</span></span><br><span data-ttu-id="ca3f3-158">読み取り/書き込み</span><span class="sxs-lookup"><span data-stu-id="ca3f3-158">Read/write</span></span><br><span data-ttu-id="ca3f3-159">必須</span><span class="sxs-lookup"><span data-stu-id="ca3f3-159">Required</span></span> | <span data-ttu-id="ca3f3-160">候補者の選考の状態を指定します。</span><span class="sxs-lookup"><span data-stu-id="ca3f3-160">Provides the candidate’s status for the screening.</span></span> |
| <span data-ttu-id="ca3f3-161">**完了日**</span><span class="sxs-lookup"><span data-stu-id="ca3f3-161">**Completed Date**</span></span><br><span data-ttu-id="ca3f3-162">mshr_completeddate</span><span class="sxs-lookup"><span data-stu-id="ca3f3-162">mshr_completeddate</span></span><br><span data-ttu-id="ca3f3-163">*Datetime*</span><span class="sxs-lookup"><span data-stu-id="ca3f3-163">*Datetime*</span></span> | <span data-ttu-id="ca3f3-164">読み取り/書き込み</span><span class="sxs-lookup"><span data-stu-id="ca3f3-164">Read/write</span></span><br><span data-ttu-id="ca3f3-165">オプション</span><span class="sxs-lookup"><span data-stu-id="ca3f3-165">Optional</span></span> | <span data-ttu-id="ca3f3-166">選考が完了した日付です。</span><span class="sxs-lookup"><span data-stu-id="ca3f3-166">The date the screening was completed.</span></span> |
| <span data-ttu-id="ca3f3-167">**摘要**</span><span class="sxs-lookup"><span data-stu-id="ca3f3-167">**Notes**</span></span><br><span data-ttu-id="ca3f3-168">mshr_note</span><span class="sxs-lookup"><span data-stu-id="ca3f3-168">mshr_note</span></span><br><span data-ttu-id="ca3f3-169">*文字列*</span><span class="sxs-lookup"><span data-stu-id="ca3f3-169">*String*</span></span> | <span data-ttu-id="ca3f3-170">読み取り/書き込み</span><span class="sxs-lookup"><span data-stu-id="ca3f3-170">Read/write</span></span><br><span data-ttu-id="ca3f3-171">オプション</span><span class="sxs-lookup"><span data-stu-id="ca3f3-171">Optional</span></span> | <span data-ttu-id="ca3f3-172">採用担当者や採用マネージャーが使用するメモです。</span><span class="sxs-lookup"><span data-stu-id="ca3f3-172">Notes for use by hiring managers and recruiters.</span></span> |

## <a name="see-also"></a><span data-ttu-id="ca3f3-173">参照</span><span class="sxs-lookup"><span data-stu-id="ca3f3-173">See also</span></span>

[<span data-ttu-id="ca3f3-174">申請者追跡システム統合APIの概要</span><span class="sxs-lookup"><span data-stu-id="ca3f3-174">Applicant Tracking System integration API introduction</span></span>](hr-admin-integration-ats-api-introduction.md)<br>
[<span data-ttu-id="ca3f3-175">採用する採用候補者に対するクエリの例</span><span class="sxs-lookup"><span data-stu-id="ca3f3-175">Example query for Candidate to hire</span></span>](hr-admin-integration-ats-api-candidate-to-hire-example-query.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]