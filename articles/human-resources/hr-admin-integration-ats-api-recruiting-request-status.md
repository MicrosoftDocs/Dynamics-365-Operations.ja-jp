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
ms.openlocfilehash: 55ed9c391a1b5f86c3c443b9fceeee5c2301444d
ms.sourcegitcommit: 33b5c8bc4f9461e290513aa22de1ec1fba3b0742
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/05/2021
ms.locfileid: "5125957"
---
# <a name="recruiting-request-status"></a><span data-ttu-id="da5c0-103">採用で要求する状態</span><span class="sxs-lookup"><span data-stu-id="da5c0-103">Recruiting request status</span></span>

<span data-ttu-id="da5c0-104">このトピックでは、Dynamics 365 Human Resources の採用で要求する状態のオプションセットについて説明します。</span><span class="sxs-lookup"><span data-stu-id="da5c0-104">This topic describes the Recruiting request status option set for Dynamics 365 Human Resources.</span></span>

<span data-ttu-id="da5c0-105">物理名 : mshr_hcmrecruitingrequeststatus</span><span class="sxs-lookup"><span data-stu-id="da5c0-105">Physical name: mshr_hcmrecruitingrequeststatus</span></span>

<span data-ttu-id="da5c0-106">このリストは、RecruitingRequest に対して、状態値のオプション セットを提供します。</span><span class="sxs-lookup"><span data-stu-id="da5c0-106">This enumeration provides the option set for the status values of a RecruitingRequest.</span></span>

| <span data-ttu-id="da5c0-107">先頭値</span><span class="sxs-lookup"><span data-stu-id="da5c0-107">Value</span></span> | <span data-ttu-id="da5c0-108">ラベル</span><span class="sxs-lookup"><span data-stu-id="da5c0-108">Label</span></span> | <span data-ttu-id="da5c0-109">説明</span><span class="sxs-lookup"><span data-stu-id="da5c0-109">Description</span></span> |
| --- | --- | --- |
| <span data-ttu-id="da5c0-110">200000000</span><span class="sxs-lookup"><span data-stu-id="da5c0-110">200000000</span></span> | <span data-ttu-id="da5c0-111">ドラフト</span><span class="sxs-lookup"><span data-stu-id="da5c0-111">Draft</span></span> | <span data-ttu-id="da5c0-112">要求が下書きの状態となっているため、アクティブな採用を行うことができません。</span><span class="sxs-lookup"><span data-stu-id="da5c0-112">The request is in draft and isn't ready for active recruiting.</span></span> |
| <span data-ttu-id="da5c0-113">200000001</span><span class="sxs-lookup"><span data-stu-id="da5c0-113">200000001</span></span> | <span data-ttu-id="da5c0-114">確認中</span><span class="sxs-lookup"><span data-stu-id="da5c0-114">In Review</span></span> | <span data-ttu-id="da5c0-115">要求がすでに送信されており、ワークフローによる承認を受け付中です。</span><span class="sxs-lookup"><span data-stu-id="da5c0-115">The request has been submitted and is being routed for approval by workflow.</span></span> <span data-ttu-id="da5c0-116">ワークフローが有効になっている場合にのみ使用できます。</span><span class="sxs-lookup"><span data-stu-id="da5c0-116">Only available when workflow is enabled.</span></span> |
| <span data-ttu-id="da5c0-117">200000002</span><span class="sxs-lookup"><span data-stu-id="da5c0-117">200000002</span></span> | <span data-ttu-id="da5c0-118">保留中</span><span class="sxs-lookup"><span data-stu-id="da5c0-118">Pending</span></span> | <span data-ttu-id="da5c0-119">要求が保留中のワークフロー アクションです。</span><span class="sxs-lookup"><span data-stu-id="da5c0-119">The request is pending workflow action.</span></span> <span data-ttu-id="da5c0-120">ワークフローが有効になっている場合にのみ使用できます。</span><span class="sxs-lookup"><span data-stu-id="da5c0-120">Only available when workflow is enabled.</span></span> |
| <span data-ttu-id="da5c0-121">200000003</span><span class="sxs-lookup"><span data-stu-id="da5c0-121">200000003</span></span> | <span data-ttu-id="da5c0-122">取消済</span><span class="sxs-lookup"><span data-stu-id="da5c0-122">Canceled</span></span> | <span data-ttu-id="da5c0-123">要求がキャンセルされました。</span><span class="sxs-lookup"><span data-stu-id="da5c0-123">The request has been canceled.</span></span> <span data-ttu-id="da5c0-124">ワークフローが有効になっている場合にのみ使用できます。</span><span class="sxs-lookup"><span data-stu-id="da5c0-124">Only available when workflow is enabled.</span></span> |
| <span data-ttu-id="da5c0-125">200000004</span><span class="sxs-lookup"><span data-stu-id="da5c0-125">200000004</span></span> | <span data-ttu-id="da5c0-126">拒否済</span><span class="sxs-lookup"><span data-stu-id="da5c0-126">Denied</span></span> | <span data-ttu-id="da5c0-127">要求が否認されました。</span><span class="sxs-lookup"><span data-stu-id="da5c0-127">The request has been denied.</span></span> <span data-ttu-id="da5c0-128">ワークフローが有効になっている場合にのみ使用できます。</span><span class="sxs-lookup"><span data-stu-id="da5c0-128">Only available when workflow is enabled.</span></span> |
| <span data-ttu-id="da5c0-129">200000005</span><span class="sxs-lookup"><span data-stu-id="da5c0-129">200000005</span></span> | <span data-ttu-id="da5c0-130">使用可能</span><span class="sxs-lookup"><span data-stu-id="da5c0-130">Active</span></span> | <span data-ttu-id="da5c0-131">ワークフローが完了して承認されると、その要求に対して有効な採用を行う準備が整います。</span><span class="sxs-lookup"><span data-stu-id="da5c0-131">Any workflow is completed and approved, and the request is ready for active recruiting.</span></span> |
| <span data-ttu-id="da5c0-132">200000006</span><span class="sxs-lookup"><span data-stu-id="da5c0-132">200000006</span></span> | <span data-ttu-id="da5c0-133">終了済</span><span class="sxs-lookup"><span data-stu-id="da5c0-133">Closed</span></span> | <span data-ttu-id="da5c0-134">採用要求が完了しました。</span><span class="sxs-lookup"><span data-stu-id="da5c0-134">The recruiting request is closed.</span></span> |

## <a name="see-also"></a><span data-ttu-id="da5c0-135">参照</span><span class="sxs-lookup"><span data-stu-id="da5c0-135">See also</span></span>

[<span data-ttu-id="da5c0-136">申請者追跡システム統合APIの概要</span><span class="sxs-lookup"><span data-stu-id="da5c0-136">Applicant Tracking System integration API introduction</span></span>](hr-admin-integration-ats-api-introduction.md)<br>
[<span data-ttu-id="da5c0-137">採用要求のクエリの例</span><span class="sxs-lookup"><span data-stu-id="da5c0-137">Example query for Recruiting request</span></span>](hr-admin-integration-ats-api-recruiting-request-example-query.md)
