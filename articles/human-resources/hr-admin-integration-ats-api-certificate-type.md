---
title: 証明書タイプ
description: このトピックでは、Dynamics 365 Human Resources の証明書タイプ エンティティについて説明します。
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
ms.openlocfilehash: b8e979f242eb689b730b7f8a8684b3e697adbee6
ms.sourcegitcommit: 879ee8a10e6158885795dce4b3db5077540eec41
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/18/2021
ms.locfileid: "6054695"
---
# <a name="certificate-type"></a><span data-ttu-id="04030-103">証明書タイプ</span><span class="sxs-lookup"><span data-stu-id="04030-103">Certificate type</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="04030-104">このトピックでは、Dynamics 365 Human Resources の証明書タイプ エンティティについて説明します。</span><span class="sxs-lookup"><span data-stu-id="04030-104">This topic describes the Certificate type entity for Dynamics 365 Human Resources.</span></span>

<span data-ttu-id="04030-105">物理名 : mshr_hcmcertificatetypeentity</span><span class="sxs-lookup"><span data-stu-id="04030-105">Physical name: mshr_hcmcertificatetypeentity</span></span>

## <a name="description"></a><span data-ttu-id="04030-106">説明</span><span class="sxs-lookup"><span data-stu-id="04030-106">Description</span></span>

<span data-ttu-id="04030-107">このエンティティは、Human Resources で設定された職業証明書タイプの一覧を定義します。</span><span class="sxs-lookup"><span data-stu-id="04030-107">This entity defines the list of professional certificate types set up in Human Resources.</span></span> <span data-ttu-id="04030-108">エンティティは、法人 (会社) に固有のエンティティではありません。</span><span class="sxs-lookup"><span data-stu-id="04030-108">The entity isn't specific to a legal entity (company).</span></span>

## <a name="json-representation"></a><span data-ttu-id="04030-109">JSON 表記</span><span class="sxs-lookup"><span data-stu-id="04030-109">JSON representation</span></span>

```json
{
    "mshr_certificatetype": "String",
    "mshr_description": "String",
    "mshr_requirerenewal": Int,
    "mshr_hcmcertificatetypeentityid": "Guid"
}
```

## <a name="properties"></a><span data-ttu-id="04030-110">プロパティ</span><span class="sxs-lookup"><span data-stu-id="04030-110">Properties</span></span>

| <span data-ttu-id="04030-111">プロパティ</span><span class="sxs-lookup"><span data-stu-id="04030-111">Property</span></span><br><span data-ttu-id="04030-112">**現物名**</span><span class="sxs-lookup"><span data-stu-id="04030-112">**Physical name**</span></span><br><span data-ttu-id="04030-113">**_種類_**</span><span class="sxs-lookup"><span data-stu-id="04030-113">**_Type_**</span></span> | <span data-ttu-id="04030-114">使用</span><span class="sxs-lookup"><span data-stu-id="04030-114">Use</span></span> | <span data-ttu-id="04030-115">説明</span><span class="sxs-lookup"><span data-stu-id="04030-115">Description</span></span> |
| --- | --- | --- |
| <span data-ttu-id="04030-116">**証明書タイプ エンティティ ID**</span><span class="sxs-lookup"><span data-stu-id="04030-116">**Certificate Type Entity ID**</span></span><br><span data-ttu-id="04030-117">mshr_hcmcertificatetypeentityid</span><span class="sxs-lookup"><span data-stu-id="04030-117">mshr_hcmcertificatetypeentityid</span></span><br><span data-ttu-id="04030-118">*GUID*</span><span class="sxs-lookup"><span data-stu-id="04030-118">*GUID*</span></span> | <span data-ttu-id="04030-119">読み取り専用</span><span class="sxs-lookup"><span data-stu-id="04030-119">Read-only</span></span><br><span data-ttu-id="04030-120">必須</span><span class="sxs-lookup"><span data-stu-id="04030-120">Required</span></span> 
<span data-ttu-id="04030-121">システム生成</span><span class="sxs-lookup"><span data-stu-id="04030-121">System-generated</span></span> | <span data-ttu-id="04030-122">証明書タイプに固有のプライマリ識別子です。</span><span class="sxs-lookup"><span data-stu-id="04030-122">Unique primary identifier for the certificate type.</span></span> |
| <span data-ttu-id="04030-123">**証明書タイプ**</span><span class="sxs-lookup"><span data-stu-id="04030-123">**Certificate Type**</span></span><br><span data-ttu-id="04030-124">mshr_certificatetype</span><span class="sxs-lookup"><span data-stu-id="04030-124">mshr_certificatetype</span></span><br><span data-ttu-id="04030-125">*文字列*</span><span class="sxs-lookup"><span data-stu-id="04030-125">*String*</span></span> | <span data-ttu-id="04030-126">読み取り/書き込み</span><span class="sxs-lookup"><span data-stu-id="04030-126">Read/write</span></span><br><span data-ttu-id="04030-127">必須</span><span class="sxs-lookup"><span data-stu-id="04030-127">Required</span></span> | <span data-ttu-id="04030-128">証明書タイプに固有のユーザーが読取り可能な識別子です。</span><span class="sxs-lookup"><span data-stu-id="04030-128">Unique user-readable identifier for the certificate type.</span></span> |
| <span data-ttu-id="04030-129">**説明**</span><span class="sxs-lookup"><span data-stu-id="04030-129">**Description**</span></span><br><span data-ttu-id="04030-130">mshr_description</span><span class="sxs-lookup"><span data-stu-id="04030-130">mshr_description</span></span><br><span data-ttu-id="04030-131">*文字列*</span><span class="sxs-lookup"><span data-stu-id="04030-131">*String*</span></span> | <span data-ttu-id="04030-132">読み取り/書き込み</span><span class="sxs-lookup"><span data-stu-id="04030-132">Read/write</span></span><br><span data-ttu-id="04030-133">必須</span><span class="sxs-lookup"><span data-stu-id="04030-133">Required</span></span> | <span data-ttu-id="04030-134">証明書タイプの説明。</span><span class="sxs-lookup"><span data-stu-id="04030-134">Description of the certificate type.</span></span> |
| <span data-ttu-id="04030-135">**更新の要求**</span><span class="sxs-lookup"><span data-stu-id="04030-135">**Require Renewal**</span></span><br><span data-ttu-id="04030-136">mshr_requirerenewal</span><span class="sxs-lookup"><span data-stu-id="04030-136">mshr_requirerenewal</span></span><br><span data-ttu-id="04030-137">*mshr_noyes オプション セット*</span><span class="sxs-lookup"><span data-stu-id="04030-137">*mshr_noyes option set*</span></span> | <span data-ttu-id="04030-138">読み取り/書き込み</span><span class="sxs-lookup"><span data-stu-id="04030-138">Read/write</span></span><br><span data-ttu-id="04030-139">オプション</span><span class="sxs-lookup"><span data-stu-id="04030-139">Optional</span></span> | <span data-ttu-id="04030-140">証明書に更新が必要かどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="04030-140">Indicates whether renewal is required for the certificate.</span></span> |

## <a name="see-also"></a><span data-ttu-id="04030-141">参照</span><span class="sxs-lookup"><span data-stu-id="04030-141">See also</span></span>

[<span data-ttu-id="04030-142">申請者追跡システム統合APIの概要</span><span class="sxs-lookup"><span data-stu-id="04030-142">Applicant Tracking System integration API introduction</span></span>](hr-admin-integration-ats-api-introduction.md)<br>
[<span data-ttu-id="04030-143">採用する採用候補者に対するクエリの例</span><span class="sxs-lookup"><span data-stu-id="04030-143">Example query for Candidate to hire</span></span>](hr-admin-integration-ats-api-candidate-to-hire-example-query.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]