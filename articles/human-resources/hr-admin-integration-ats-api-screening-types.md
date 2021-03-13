---
title: 審査タイプ
description: このトピックでは、Dynamics 365 Human Resources の選考タイプ エンティティについて説明します。
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
ms.openlocfilehash: 227c15acb44e020ea9858961e45c11ad07e18a74
ms.sourcegitcommit: 33b5c8bc4f9461e290513aa22de1ec1fba3b0742
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/05/2021
ms.locfileid: "5126173"
---
# <a name="screening-types"></a><span data-ttu-id="ea690-103">審査タイプ</span><span class="sxs-lookup"><span data-stu-id="ea690-103">Screening types</span></span>

<span data-ttu-id="ea690-104">このトピックでは、Dynamics 365 Human Resources の選考タイプ エンティティについて説明します。</span><span class="sxs-lookup"><span data-stu-id="ea690-104">This topic describes the Screening types entity for Dynamics 365 Human Resources.</span></span>

<span data-ttu-id="ea690-105">物理名 : mshr_hcmscreeningtypeentity</span><span class="sxs-lookup"><span data-stu-id="ea690-105">Physical name: mshr_hcmscreeningtypeentity</span></span>

## <a name="description"></a><span data-ttu-id="ea690-106">説明</span><span class="sxs-lookup"><span data-stu-id="ea690-106">Description</span></span>

<span data-ttu-id="ea690-107">このエンティティには、雇用前および継続的な従業員の選考プロセスに会社が設定した選考の種類が記載されています。</span><span class="sxs-lookup"><span data-stu-id="ea690-107">This entity describes the screening types set up by the company for pre-employment and ongoing employee screening processes.</span></span>

## <a name="json-representation"></a><span data-ttu-id="ea690-108">JSON 表記</span><span class="sxs-lookup"><span data-stu-id="ea690-108">JSON representation</span></span>

```json
{
    "mshr_description": "String",
    "mshr_frequencyunit": Int,
    "mshr_generatefrom": Int,
    "mshr_frequencyinterval": Int,
    "mshr_screeningtypeid": "String",
    "mshr_hcmscreeningtypeentityid": "Guid"
}
```

## <a name="properties"></a><span data-ttu-id="ea690-109">プロパティ</span><span class="sxs-lookup"><span data-stu-id="ea690-109">Properties</span></span>

| <span data-ttu-id="ea690-110">プロパティ</span><span class="sxs-lookup"><span data-stu-id="ea690-110">Property</span></span><br><span data-ttu-id="ea690-111">**現物名**</span><span class="sxs-lookup"><span data-stu-id="ea690-111">**Physical name**</span></span><br><span data-ttu-id="ea690-112">**_種類_**</span><span class="sxs-lookup"><span data-stu-id="ea690-112">**_Type_**</span></span> | <span data-ttu-id="ea690-113">使用</span><span class="sxs-lookup"><span data-stu-id="ea690-113">Use</span></span> | <span data-ttu-id="ea690-114">説明</span><span class="sxs-lookup"><span data-stu-id="ea690-114">Description</span></span> |
| --- | --- | --- |
| <span data-ttu-id="ea690-115">**選考タイプ エンティティ ID**</span><span class="sxs-lookup"><span data-stu-id="ea690-115">**Screening Type Entity ID**</span></span><br><span data-ttu-id="ea690-116">mshr_hcmscreeningtypeentityid</span><span class="sxs-lookup"><span data-stu-id="ea690-116">mshr_hcmscreeningtypeentityid</span></span><br><span data-ttu-id="ea690-117">*GUID*</span><span class="sxs-lookup"><span data-stu-id="ea690-117">*GUID*</span></span> | <span data-ttu-id="ea690-118">読み取り専用</span><span class="sxs-lookup"><span data-stu-id="ea690-118">Read-only</span></span><br><span data-ttu-id="ea690-119">必須</span><span class="sxs-lookup"><span data-stu-id="ea690-119">Required</span></span><br><span data-ttu-id="ea690-120">システム生成</span><span class="sxs-lookup"><span data-stu-id="ea690-120">System-generated</span></span> | <span data-ttu-id="ea690-121">人物の選考タイプ レコードの一意の基本識別子です。</span><span class="sxs-lookup"><span data-stu-id="ea690-121">Unique primary identifier for the screening type record.</span></span> |
| <span data-ttu-id="ea690-122">**選考タイプ ID**</span><span class="sxs-lookup"><span data-stu-id="ea690-122">**Screening Type ID**</span></span><br><span data-ttu-id="ea690-123">mshr_screeningtypeid</span><span class="sxs-lookup"><span data-stu-id="ea690-123">mshr_screeningtypeid</span></span><br><span data-ttu-id="ea690-124">*文字列*</span><span class="sxs-lookup"><span data-stu-id="ea690-124">*String*</span></span> | <span data-ttu-id="ea690-125">読み取り/書き込み</span><span class="sxs-lookup"><span data-stu-id="ea690-125">Read/write</span></span><br><span data-ttu-id="ea690-126">必須</span><span class="sxs-lookup"><span data-stu-id="ea690-126">Required</span></span> | <span data-ttu-id="ea690-127">ユーザー定義の選考タイプ レコードの一意識別子です。</span><span class="sxs-lookup"><span data-stu-id="ea690-127">User-defined unique identifier for the screening type.</span></span> |
| <span data-ttu-id="ea690-128">**説明**</span><span class="sxs-lookup"><span data-stu-id="ea690-128">**Description**</span></span><br><span data-ttu-id="ea690-129">mshr_description</span><span class="sxs-lookup"><span data-stu-id="ea690-129">mshr_description</span></span><br><span data-ttu-id="ea690-130">*文字列*</span><span class="sxs-lookup"><span data-stu-id="ea690-130">*String*</span></span> | <span data-ttu-id="ea690-131">読み取り/書き込み</span><span class="sxs-lookup"><span data-stu-id="ea690-131">Read/write</span></span><br><span data-ttu-id="ea690-132">必須</span><span class="sxs-lookup"><span data-stu-id="ea690-132">Required</span></span> | <span data-ttu-id="ea690-133">選考タイプの説明です。</span><span class="sxs-lookup"><span data-stu-id="ea690-133">The description of the screening type.</span></span> |
| <span data-ttu-id="ea690-134">**頻度の単位**</span><span class="sxs-lookup"><span data-stu-id="ea690-134">**Frequency Unit**</span></span><br><span data-ttu-id="ea690-135">mshr_frequencyunit</span><span class="sxs-lookup"><span data-stu-id="ea690-135">mshr_frequencyunit</span></span><br><span data-ttu-id="ea690-136">*mshr_hcmfrequencyunit オプション セット*</span><span class="sxs-lookup"><span data-stu-id="ea690-136">*mshr_hcmfrequencyunit option set*</span></span> | <span data-ttu-id="ea690-137">読み取り/書き込み</span><span class="sxs-lookup"><span data-stu-id="ea690-137">Read/write</span></span><br><span data-ttu-id="ea690-138">必須</span><span class="sxs-lookup"><span data-stu-id="ea690-138">Required</span></span> | <span data-ttu-id="ea690-139">割り当てられた人物に対して審査を完了しなければならない頻度を表します。</span><span class="sxs-lookup"><span data-stu-id="ea690-139">Describes the frequency with which the screening must be completed for the assigned person.</span></span> |
| <span data-ttu-id="ea690-140">**生成元**</span><span class="sxs-lookup"><span data-stu-id="ea690-140">**Generate From**</span></span><br><span data-ttu-id="ea690-141">mshr_generatefrom</span><span class="sxs-lookup"><span data-stu-id="ea690-141">mshr_generatefrom</span></span><br><span data-ttu-id="ea690-142">*mshr_hcmfrequencygeneratefrom オプション セット*</span><span class="sxs-lookup"><span data-stu-id="ea690-142">*mshr_hcmfrequencygeneratefrom option set*</span></span> | <span data-ttu-id="ea690-143">読み取り/書き込み</span><span class="sxs-lookup"><span data-stu-id="ea690-143">Read-write</span></span><br><span data-ttu-id="ea690-144">必須</span><span class="sxs-lookup"><span data-stu-id="ea690-144">Required</span></span> | <span data-ttu-id="ea690-145">頻度の値が [一時のみ] 以外の値である場合は、GenerateFrom 値により、次の選考イベントを計算する開始日が決定されます。</span><span class="sxs-lookup"><span data-stu-id="ea690-145">If the Frequency value is any value other than “One-time only”, the GenerateFrom value determines the date from which to calculate the next screening event.</span></span> |
| <span data-ttu-id="ea690-146">**頻度の間隔**</span><span class="sxs-lookup"><span data-stu-id="ea690-146">**Frequency Interval**</span></span><br><span data-ttu-id="ea690-147">mshr_frequencyinterval</span><span class="sxs-lookup"><span data-stu-id="ea690-147">mshr_frequencyinterval</span></span><br><span data-ttu-id="ea690-148">*整数*</span><span class="sxs-lookup"><span data-stu-id="ea690-148">*Integer*</span></span> | <span data-ttu-id="ea690-149">読み取り/書き込み</span><span class="sxs-lookup"><span data-stu-id="ea690-149">Read-write</span></span><br><span data-ttu-id="ea690-150">必須</span><span class="sxs-lookup"><span data-stu-id="ea690-150">Required</span></span> | <span data-ttu-id="ea690-151">頻度の値が [一時のみ] 以外の値である場合は、各選考イベントの間隔を定義する必要があります。</span><span class="sxs-lookup"><span data-stu-id="ea690-151">If the Frequency value is any value other than “One-time only”, you must define an interval for the units of time between each screening event.</span></span> |

## <a name="see-also"></a><span data-ttu-id="ea690-152">参照</span><span class="sxs-lookup"><span data-stu-id="ea690-152">See also</span></span>

[<span data-ttu-id="ea690-153">申請者追跡システム統合APIの概要</span><span class="sxs-lookup"><span data-stu-id="ea690-153">Applicant Tracking System integration API introduction</span></span>](hr-admin-integration-ats-api-introduction.md)<br>
[<span data-ttu-id="ea690-154">採用する採用候補者に対するクエリの例</span><span class="sxs-lookup"><span data-stu-id="ea690-154">Example query for Candidate to hire</span></span>](hr-admin-integration-ats-api-candidate-to-hire-example-query.md)
