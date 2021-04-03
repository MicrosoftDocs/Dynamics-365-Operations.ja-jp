---
title: 人物の証明書
description: このトピックでは、Dynamics 365 Human Resources の人物の証明書エンティティについて説明します。
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
ms.openlocfilehash: 4587337d8fd52828309826f3301b6f053b267819
ms.sourcegitcommit: 6affb3316be757c99e1fe9c7c7b312b93c483408
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/17/2021
ms.locfileid: "5466523"
---
# <a name="person-certificate"></a><span data-ttu-id="7f311-103">人物の証明書</span><span class="sxs-lookup"><span data-stu-id="7f311-103">Person certificate</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="7f311-104">このトピックでは、Dynamics 365 Human Resources の人物の証明書エンティティについて説明します。</span><span class="sxs-lookup"><span data-stu-id="7f311-104">This topic describes the Person certificate entity for Dynamics 365 Human Resources.</span></span>

<span data-ttu-id="7f311-105">物理名 : mshr_hcmpersoncertificateentity</span><span class="sxs-lookup"><span data-stu-id="7f311-105">Physical name: mshr_hcmpersoncertificateentity</span></span>

## <a name="description"></a><span data-ttu-id="7f311-106">説明</span><span class="sxs-lookup"><span data-stu-id="7f311-106">Description</span></span>

<span data-ttu-id="7f311-107">このエンティティは、候補者の職業証明書を表します。</span><span class="sxs-lookup"><span data-stu-id="7f311-107">This entity describes the professional certificates of a candidate.</span></span>

## <a name="json-representation"></a><span data-ttu-id="7f311-108">JSON 表記</span><span class="sxs-lookup"><span data-stu-id="7f311-108">JSON representation</span></span>

```json
{
    "mshr_certificatetypeid": "String",
    "mshr_startdate": "Date",
    "mshr_enddate": "Date",
    "mshr_notes": "String",
    "mshr_partynumber": "String",
    "mshr_primaryfield": "String",
    "_mshr_fk_certificatetype_id_value": "Guid",
    "_mshr_fk_person_id_value": "Guid",
    "mshr_hcmpersoncertificateentityid": "Guid"
}
```

## <a name="properties"></a><span data-ttu-id="7f311-109">プロパティ</span><span class="sxs-lookup"><span data-stu-id="7f311-109">Properties</span></span>

| <span data-ttu-id="7f311-110">プロパティ</span><span class="sxs-lookup"><span data-stu-id="7f311-110">Property</span></span><br><span data-ttu-id="7f311-111">**現物名**</span><span class="sxs-lookup"><span data-stu-id="7f311-111">**Physical name**</span></span><br><span data-ttu-id="7f311-112">**_種類_**</span><span class="sxs-lookup"><span data-stu-id="7f311-112">**_Type_**</span></span> | <span data-ttu-id="7f311-113">使用</span><span class="sxs-lookup"><span data-stu-id="7f311-113">Use</span></span> | <span data-ttu-id="7f311-114">説明</span><span class="sxs-lookup"><span data-stu-id="7f311-114">Description</span></span> |
| --- | --- | --- |
| <span data-ttu-id="7f311-115">**人物の証明書エンティティ ID**</span><span class="sxs-lookup"><span data-stu-id="7f311-115">**Person Certificate Entity ID**</span></span><br><span data-ttu-id="7f311-116">mshr_hcmpersoncertificateentityid</span><span class="sxs-lookup"><span data-stu-id="7f311-116">mshr_hcmpersoncertificateentityid</span></span><br><span data-ttu-id="7f311-117">*GUID*</span><span class="sxs-lookup"><span data-stu-id="7f311-117">*GUID*</span></span> | <span data-ttu-id="7f311-118">読み取り専用</span><span class="sxs-lookup"><span data-stu-id="7f311-118">Read-only</span></span><br><span data-ttu-id="7f311-119">必須</span><span class="sxs-lookup"><span data-stu-id="7f311-119">Required</span></span> | <span data-ttu-id="7f311-120">システムが生成した、人物の証明書エンティティ レコードの一意識別子です。</span><span class="sxs-lookup"><span data-stu-id="7f311-120">System-generated unique identifier for the person certificate entity record.</span></span> |
| <span data-ttu-id="7f311-121">**当事者番号**</span><span class="sxs-lookup"><span data-stu-id="7f311-121">**Party Number**</span></span><br><span data-ttu-id="7f311-122">mshr_partynumber</span><span class="sxs-lookup"><span data-stu-id="7f311-122">mshr_partynumber</span></span><br><span data-ttu-id="7f311-123">*文字列*</span><span class="sxs-lookup"><span data-stu-id="7f311-123">*String*</span></span> | <span data-ttu-id="7f311-124">読み取り/書き込み</span><span class="sxs-lookup"><span data-stu-id="7f311-124">Read/write</span></span><br><span data-ttu-id="7f311-125">必須</span><span class="sxs-lookup"><span data-stu-id="7f311-125">Required</span></span> | <span data-ttu-id="7f311-126">候補者の関係者 (人物) ID です。</span><span class="sxs-lookup"><span data-stu-id="7f311-126">The party (person) ID of the candidate.</span></span> |
| <span data-ttu-id="7f311-127">**個人 ID の値**</span><span class="sxs-lookup"><span data-stu-id="7f311-127">**Person ID Value**</span></span><br><span data-ttu-id="7f311-128">_mshr_fk_person_id_value</span><span class="sxs-lookup"><span data-stu-id="7f311-128">_mshr_fk_person_id_value</span></span><br><span data-ttu-id="7f311-129">*GUID*</span><span class="sxs-lookup"><span data-stu-id="7f311-129">*GUID*</span></span> | <span data-ttu-id="7f311-130">読み取り専用</span><span class="sxs-lookup"><span data-stu-id="7f311-130">Read-only</span></span><br><span data-ttu-id="7f311-131">必須</span><span class="sxs-lookup"><span data-stu-id="7f311-131">Required</span></span><br><span data-ttu-id="7f311-132">外部キー : mshr_dirpersonentity の mshr_dirpersonentityid</span><span class="sxs-lookup"><span data-stu-id="7f311-132">Foreign key: mshr_dirpersonentityid of mshr_dirpersonentity</span></span> | <span data-ttu-id="7f311-133">システムが生成する、当事者 (個人) エンティティ レコードの識別子です。</span><span class="sxs-lookup"><span data-stu-id="7f311-133">The system-generated identifier of the party (person) entity record.</span></span> |
| <span data-ttu-id="7f311-134">**証明書タイプ ID**</span><span class="sxs-lookup"><span data-stu-id="7f311-134">**Certificate Type ID**</span></span><br><span data-ttu-id="7f311-135">mshr_certificatetypeid</span><span class="sxs-lookup"><span data-stu-id="7f311-135">mshr_certificatetypeid</span></span><br><span data-ttu-id="7f311-136">*文字列*</span><span class="sxs-lookup"><span data-stu-id="7f311-136">*String*</span></span> | <span data-ttu-id="7f311-137">読み取り/書き込み</span><span class="sxs-lookup"><span data-stu-id="7f311-137">Read/write</span></span><br><span data-ttu-id="7f311-138">必須</span><span class="sxs-lookup"><span data-stu-id="7f311-138">Required</span></span> |  <span data-ttu-id="7f311-139">Human Resources で定義されている証明書タイプの ID です。</span><span class="sxs-lookup"><span data-stu-id="7f311-139">The identifier of the certificate type defined in Human Resources.</span></span> |
| <span data-ttu-id="7f311-140">**証明書タイプ ID 値**</span><span class="sxs-lookup"><span data-stu-id="7f311-140">**Certificate Type ID Value**</span></span><br><span data-ttu-id="7f311-141">_mshr_fk_certificatetype_id_value</span><span class="sxs-lookup"><span data-stu-id="7f311-141">_mshr_fk_certificatetype_id_value</span></span><br><span data-ttu-id="7f311-142">*GUID*</span><span class="sxs-lookup"><span data-stu-id="7f311-142">*GUID*</span></span> | <span data-ttu-id="7f311-143">読み取り専用</span><span class="sxs-lookup"><span data-stu-id="7f311-143">Read-only</span></span><br><span data-ttu-id="7f311-144">必須</span><span class="sxs-lookup"><span data-stu-id="7f311-144">Required</span></span><br><span data-ttu-id="7f311-145">外部キー : mshr_hcmcertificatetypeentity の mshr_hcmcertificatetypeentityid</span><span class="sxs-lookup"><span data-stu-id="7f311-145">Foreign key: mshr_hcmcertificatetypeentityid of mshr_hcmcertificatetypeentity</span></span> | <span data-ttu-id="7f311-146">システムが生成する関連エンティティの証明書タイプの一意識別子です。</span><span class="sxs-lookup"><span data-stu-id="7f311-146">System-generated unique identifier of the certificate type in the associated entity.</span></span> |
| <span data-ttu-id="7f311-147">**開始日**</span><span class="sxs-lookup"><span data-stu-id="7f311-147">**Start Date**</span></span><br><span data-ttu-id="7f311-148">mshr_startdate</span><span class="sxs-lookup"><span data-stu-id="7f311-148">mshr_startdate</span></span><br><span data-ttu-id="7f311-149">*Datetime*</span><span class="sxs-lookup"><span data-stu-id="7f311-149">*Datetime*</span></span> | <span data-ttu-id="7f311-150">読み取り/書き込み</span><span class="sxs-lookup"><span data-stu-id="7f311-150">Read/write</span></span><br><span data-ttu-id="7f311-151">必須</span><span class="sxs-lookup"><span data-stu-id="7f311-151">Required</span></span> | <span data-ttu-id="7f311-152">証明書が発行された日付です。</span><span class="sxs-lookup"><span data-stu-id="7f311-152">The date at which the certificate was issued.</span></span> |
| <span data-ttu-id="7f311-153">**終了日**</span><span class="sxs-lookup"><span data-stu-id="7f311-153">**End Date**</span></span><br><span data-ttu-id="7f311-154">mshr_enddate</span><span class="sxs-lookup"><span data-stu-id="7f311-154">mshr_enddate</span></span><br><span data-ttu-id="7f311-155">*Datetime*</span><span class="sxs-lookup"><span data-stu-id="7f311-155">*Datetime*</span></span> | <span data-ttu-id="7f311-156">読み取り/書き込み</span><span class="sxs-lookup"><span data-stu-id="7f311-156">Read/write</span></span><br><span data-ttu-id="7f311-157">オプション</span><span class="sxs-lookup"><span data-stu-id="7f311-157">Optional</span></span> | <span data-ttu-id="7f311-158">証明書が失効する日付です。</span><span class="sxs-lookup"><span data-stu-id="7f311-158">The date at which the certificate will expire.</span></span> |
| <span data-ttu-id="7f311-159">**摘要**</span><span class="sxs-lookup"><span data-stu-id="7f311-159">**Notes**</span></span><br><span data-ttu-id="7f311-160">mshr_notes</span><span class="sxs-lookup"><span data-stu-id="7f311-160">mshr_notes</span></span><br><span data-ttu-id="7f311-161">*文字列*</span><span class="sxs-lookup"><span data-stu-id="7f311-161">*String*</span></span> | <span data-ttu-id="7f311-162">読み取り/書き込み</span><span class="sxs-lookup"><span data-stu-id="7f311-162">Read/write</span></span><br><span data-ttu-id="7f311-163">オプション</span><span class="sxs-lookup"><span data-stu-id="7f311-163">Optional</span></span> | <span data-ttu-id="7f311-164">採用担当者や採用マネージャーが使用するメモです。</span><span class="sxs-lookup"><span data-stu-id="7f311-164">Notes for use by hiring managers and recruiters.</span></span> |
| <span data-ttu-id="7f311-165">**基本フィールド**</span><span class="sxs-lookup"><span data-stu-id="7f311-165">**Primary Field**</span></span><br><span data-ttu-id="7f311-166">mshr_primaryfield</span><span class="sxs-lookup"><span data-stu-id="7f311-166">mshr_primaryfield</span></span><br><span data-ttu-id="7f311-167">*文字列*</span><span class="sxs-lookup"><span data-stu-id="7f311-167">*String*</span></span> | <span data-ttu-id="7f311-168">読み取り専用</span><span class="sxs-lookup"><span data-stu-id="7f311-168">Read-only</span></span><br><span data-ttu-id="7f311-169">必須</span><span class="sxs-lookup"><span data-stu-id="7f311-169">Required</span></span> |  <span data-ttu-id="7f311-170">エンティティ レコードの識別子として使用されるフィールドです。</span><span class="sxs-lookup"><span data-stu-id="7f311-170">Field to be used as an identifier of the entity record.</span></span> <span data-ttu-id="7f311-171">関係者番号、証明書タイプ ID、開始日の組み合わせです。</span><span class="sxs-lookup"><span data-stu-id="7f311-171">Combination of party number, certificate type ID, and start date.</span></span> |

## <a name="see-also"></a><span data-ttu-id="7f311-172">参照</span><span class="sxs-lookup"><span data-stu-id="7f311-172">See also</span></span>

[<span data-ttu-id="7f311-173">申請者追跡システム統合APIの概要</span><span class="sxs-lookup"><span data-stu-id="7f311-173">Applicant Tracking System integration API introduction</span></span>](hr-admin-integration-ats-api-introduction.md)<br>
[<span data-ttu-id="7f311-174">採用する採用候補者に対するクエリの例</span><span class="sxs-lookup"><span data-stu-id="7f311-174">Example query for Candidate to hire</span></span>](hr-admin-integration-ats-api-candidate-to-hire-example-query.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]