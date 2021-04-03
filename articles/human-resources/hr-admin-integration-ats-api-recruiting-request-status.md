---
title: 採用で要求する状態
description: このトピックでは、Dynamics 365 Human Resources の採用で要求する状態のオプションセットについて説明します。
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
ms.openlocfilehash: 0032e6bfdbfd2792dafda8bf24a1b0cbc551740d
ms.sourcegitcommit: 6affb3316be757c99e1fe9c7c7b312b93c483408
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/17/2021
ms.locfileid: "5464649"
---
# <a name="recruiting-request-status"></a><span data-ttu-id="21573-103">採用で要求する状態</span><span class="sxs-lookup"><span data-stu-id="21573-103">Recruiting request status</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="21573-104">このトピックでは、Dynamics 365 Human Resources の採用で要求する状態のオプションセットについて説明します。</span><span class="sxs-lookup"><span data-stu-id="21573-104">This topic describes the Recruiting request status option set for Dynamics 365 Human Resources.</span></span>

<span data-ttu-id="21573-105">物理名 : mshr_hcmrecruitingrequeststatus</span><span class="sxs-lookup"><span data-stu-id="21573-105">Physical name: mshr_hcmrecruitingrequeststatus</span></span>

<span data-ttu-id="21573-106">このリストは、RecruitingRequest に対して、状態値のオプション セットを提供します。</span><span class="sxs-lookup"><span data-stu-id="21573-106">This enumeration provides the option set for the status values of a RecruitingRequest.</span></span>

| <span data-ttu-id="21573-107">先頭値</span><span class="sxs-lookup"><span data-stu-id="21573-107">Value</span></span> | <span data-ttu-id="21573-108">ラベル</span><span class="sxs-lookup"><span data-stu-id="21573-108">Label</span></span> | <span data-ttu-id="21573-109">説明</span><span class="sxs-lookup"><span data-stu-id="21573-109">Description</span></span> |
| --- | --- | --- |
| <span data-ttu-id="21573-110">200000000</span><span class="sxs-lookup"><span data-stu-id="21573-110">200000000</span></span> | <span data-ttu-id="21573-111">ドラフト</span><span class="sxs-lookup"><span data-stu-id="21573-111">Draft</span></span> | <span data-ttu-id="21573-112">要求が下書きの状態となっているため、アクティブな採用を行うことができません。</span><span class="sxs-lookup"><span data-stu-id="21573-112">The request is in draft and isn't ready for active recruiting.</span></span> |
| <span data-ttu-id="21573-113">200000001</span><span class="sxs-lookup"><span data-stu-id="21573-113">200000001</span></span> | <span data-ttu-id="21573-114">確認中</span><span class="sxs-lookup"><span data-stu-id="21573-114">In Review</span></span> | <span data-ttu-id="21573-115">要求がすでに送信されており、ワークフローによる承認を受け付中です。</span><span class="sxs-lookup"><span data-stu-id="21573-115">The request has been submitted and is being routed for approval by workflow.</span></span> <span data-ttu-id="21573-116">ワークフローが有効になっている場合にのみ使用できます。</span><span class="sxs-lookup"><span data-stu-id="21573-116">Only available when workflow is enabled.</span></span> |
| <span data-ttu-id="21573-117">200000002</span><span class="sxs-lookup"><span data-stu-id="21573-117">200000002</span></span> | <span data-ttu-id="21573-118">保留中</span><span class="sxs-lookup"><span data-stu-id="21573-118">Pending</span></span> | <span data-ttu-id="21573-119">要求が保留中のワークフロー アクションです。</span><span class="sxs-lookup"><span data-stu-id="21573-119">The request is pending workflow action.</span></span> <span data-ttu-id="21573-120">ワークフローが有効になっている場合にのみ使用できます。</span><span class="sxs-lookup"><span data-stu-id="21573-120">Only available when workflow is enabled.</span></span> |
| <span data-ttu-id="21573-121">200000003</span><span class="sxs-lookup"><span data-stu-id="21573-121">200000003</span></span> | <span data-ttu-id="21573-122">取消済</span><span class="sxs-lookup"><span data-stu-id="21573-122">Canceled</span></span> | <span data-ttu-id="21573-123">要求がキャンセルされました。</span><span class="sxs-lookup"><span data-stu-id="21573-123">The request has been canceled.</span></span> <span data-ttu-id="21573-124">ワークフローが有効になっている場合にのみ使用できます。</span><span class="sxs-lookup"><span data-stu-id="21573-124">Only available when workflow is enabled.</span></span> |
| <span data-ttu-id="21573-125">200000004</span><span class="sxs-lookup"><span data-stu-id="21573-125">200000004</span></span> | <span data-ttu-id="21573-126">拒否済</span><span class="sxs-lookup"><span data-stu-id="21573-126">Denied</span></span> | <span data-ttu-id="21573-127">要求が否認されました。</span><span class="sxs-lookup"><span data-stu-id="21573-127">The request has been denied.</span></span> <span data-ttu-id="21573-128">ワークフローが有効になっている場合にのみ使用できます。</span><span class="sxs-lookup"><span data-stu-id="21573-128">Only available when workflow is enabled.</span></span> |
| <span data-ttu-id="21573-129">200000005</span><span class="sxs-lookup"><span data-stu-id="21573-129">200000005</span></span> | <span data-ttu-id="21573-130">使用可能</span><span class="sxs-lookup"><span data-stu-id="21573-130">Active</span></span> | <span data-ttu-id="21573-131">ワークフローが完了して承認されると、その要求に対して有効な採用を行う準備が整います。</span><span class="sxs-lookup"><span data-stu-id="21573-131">Any workflow is completed and approved, and the request is ready for active recruiting.</span></span> |
| <span data-ttu-id="21573-132">200000006</span><span class="sxs-lookup"><span data-stu-id="21573-132">200000006</span></span> | <span data-ttu-id="21573-133">終了済</span><span class="sxs-lookup"><span data-stu-id="21573-133">Closed</span></span> | <span data-ttu-id="21573-134">採用要求が完了しました。</span><span class="sxs-lookup"><span data-stu-id="21573-134">The recruiting request is closed.</span></span> |

## <a name="see-also"></a><span data-ttu-id="21573-135">参照</span><span class="sxs-lookup"><span data-stu-id="21573-135">See also</span></span>

[<span data-ttu-id="21573-136">申請者追跡システム統合APIの概要</span><span class="sxs-lookup"><span data-stu-id="21573-136">Applicant Tracking System integration API introduction</span></span>](hr-admin-integration-ats-api-introduction.md)<br>
[<span data-ttu-id="21573-137">採用要求のクエリの例</span><span class="sxs-lookup"><span data-stu-id="21573-137">Example query for Recruiting request</span></span>](hr-admin-integration-ats-api-recruiting-request-example-query.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]