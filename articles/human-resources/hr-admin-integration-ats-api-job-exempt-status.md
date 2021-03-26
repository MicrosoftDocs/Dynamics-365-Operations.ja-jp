---
title: ジョブ除外する状態
description: このトピックでは、Dynamics 365 Human Resources におけるジョブ除外状態のオプション セットについて説明します。
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
ms.openlocfilehash: 0cd6ffc01793c8ff12e36175c7c9feaf8a4b3cdf
ms.sourcegitcommit: 33b5c8bc4f9461e290513aa22de1ec1fba3b0742
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/05/2021
ms.locfileid: "5125572"
---
# <a name="job-exempt-status"></a><span data-ttu-id="03c83-103">ジョブ除外する状態</span><span class="sxs-lookup"><span data-stu-id="03c83-103">Job exempt status</span></span>

<span data-ttu-id="03c83-104">このトピックでは、Dynamics 365 Human Resources におけるジョブ除外状態のオプション セットについて説明します。</span><span class="sxs-lookup"><span data-stu-id="03c83-104">This topic describes the Job exempt status option set for Dynamics 365 Human Resources.</span></span>

<span data-ttu-id="03c83-105">物理名 : cdm_jobexemptstatus</span><span class="sxs-lookup"><span data-stu-id="03c83-105">Physical name: cdm_jobexemptstatus</span></span>

<span data-ttu-id="03c83-106">このリストでは、FLSA ジョブ除外状態の値のオプションセットを指定します。</span><span class="sxs-lookup"><span data-stu-id="03c83-106">This enumeration specifies the option set for FLSA job exempt status values.</span></span> <span data-ttu-id="03c83-107">これは、既存の cdm_jobexemptstatus オプション セットで提供されます。</span><span class="sxs-lookup"><span data-stu-id="03c83-107">This is provided in the existing cdm_jobexemptstatus option set.</span></span>

| <span data-ttu-id="03c83-108">先頭値</span><span class="sxs-lookup"><span data-stu-id="03c83-108">Value</span></span> | <span data-ttu-id="03c83-109">ラベル</span><span class="sxs-lookup"><span data-stu-id="03c83-109">Label</span></span> | <span data-ttu-id="03c83-110">説明</span><span class="sxs-lookup"><span data-stu-id="03c83-110">Description</span></span> |
| --- | --- | --- |
| <span data-ttu-id="03c83-111">200000000</span><span class="sxs-lookup"><span data-stu-id="03c83-111">200000000</span></span> | <span data-ttu-id="03c83-112">控除</span><span class="sxs-lookup"><span data-stu-id="03c83-112">Exempt</span></span> | <span data-ttu-id="03c83-113">ジョブは、FLSA ガイドラインに基づく除外の状態です。</span><span class="sxs-lookup"><span data-stu-id="03c83-113">The job has an exempt status based on FLSA guidelines.</span></span> |
| <span data-ttu-id="03c83-114">200000001</span><span class="sxs-lookup"><span data-stu-id="03c83-114">200000001</span></span> | <span data-ttu-id="03c83-115">NonExempt</span><span class="sxs-lookup"><span data-stu-id="03c83-115">NonExempt</span></span> | <span data-ttu-id="03c83-116">ジョブは、FLSA ガイドラインに基づく非除外の状態です。</span><span class="sxs-lookup"><span data-stu-id="03c83-116">The job has a non-exempt status based on FLSA guidelines.</span></span> |
| <span data-ttu-id="03c83-117">200000002</span><span class="sxs-lookup"><span data-stu-id="03c83-117">200000002</span></span> | <span data-ttu-id="03c83-118">適用しない</span><span class="sxs-lookup"><span data-stu-id="03c83-118">Does Not Apply</span></span> | <span data-ttu-id="03c83-119">FLSA の状態のガイドラインはジョブには適用されません。</span><span class="sxs-lookup"><span data-stu-id="03c83-119">FLSA status guidelines do not apply to the job.</span></span> |

## <a name="see-also"></a><span data-ttu-id="03c83-120">参照</span><span class="sxs-lookup"><span data-stu-id="03c83-120">See also</span></span>

[<span data-ttu-id="03c83-121">申請者追跡システム統合APIの概要</span><span class="sxs-lookup"><span data-stu-id="03c83-121">Applicant Tracking System integration API introduction</span></span>](hr-admin-integration-ats-api-introduction.md)<br>
[<span data-ttu-id="03c83-122">採用要求のクエリの例</span><span class="sxs-lookup"><span data-stu-id="03c83-122">Example query for Recruiting request</span></span>](hr-admin-integration-ats-api-recruiting-request-example-query.md)