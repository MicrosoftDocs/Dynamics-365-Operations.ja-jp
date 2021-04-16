---
title: 採用で要求する状態
description: このトピックでは、Dynamics 365 Human Resources の採用で要求する状態のオプションセットについて説明します。
author: jaredha
ms.date: 02/05/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: jaredha
ms.search.validFrom: 2021-02-05
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 888fbc511bffbecd837c929049006266191da5ba
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/31/2021
ms.locfileid: "5806045"
---
# <a name="recruiting-request-status"></a><span data-ttu-id="8e024-103">採用で要求する状態</span><span class="sxs-lookup"><span data-stu-id="8e024-103">Recruiting request status</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="8e024-104">このトピックでは、Dynamics 365 Human Resources の採用で要求する状態のオプションセットについて説明します。</span><span class="sxs-lookup"><span data-stu-id="8e024-104">This topic describes the Recruiting request status option set for Dynamics 365 Human Resources.</span></span>

<span data-ttu-id="8e024-105">物理名 : mshr_hcmrecruitingrequeststatus</span><span class="sxs-lookup"><span data-stu-id="8e024-105">Physical name: mshr_hcmrecruitingrequeststatus</span></span>

<span data-ttu-id="8e024-106">このリストは、RecruitingRequest に対して、状態値のオプション セットを提供します。</span><span class="sxs-lookup"><span data-stu-id="8e024-106">This enumeration provides the option set for the status values of a RecruitingRequest.</span></span>

| <span data-ttu-id="8e024-107">先頭値</span><span class="sxs-lookup"><span data-stu-id="8e024-107">Value</span></span> | <span data-ttu-id="8e024-108">ラベル</span><span class="sxs-lookup"><span data-stu-id="8e024-108">Label</span></span> | <span data-ttu-id="8e024-109">説明</span><span class="sxs-lookup"><span data-stu-id="8e024-109">Description</span></span> |
| --- | --- | --- |
| <span data-ttu-id="8e024-110">200000000</span><span class="sxs-lookup"><span data-stu-id="8e024-110">200000000</span></span> | <span data-ttu-id="8e024-111">ドラフト</span><span class="sxs-lookup"><span data-stu-id="8e024-111">Draft</span></span> | <span data-ttu-id="8e024-112">要求が下書きの状態となっているため、アクティブな採用を行うことができません。</span><span class="sxs-lookup"><span data-stu-id="8e024-112">The request is in draft and isn't ready for active recruiting.</span></span> |
| <span data-ttu-id="8e024-113">200000001</span><span class="sxs-lookup"><span data-stu-id="8e024-113">200000001</span></span> | <span data-ttu-id="8e024-114">確認中</span><span class="sxs-lookup"><span data-stu-id="8e024-114">In Review</span></span> | <span data-ttu-id="8e024-115">要求がすでに送信されており、ワークフローによる承認を受け付中です。</span><span class="sxs-lookup"><span data-stu-id="8e024-115">The request has been submitted and is being routed for approval by workflow.</span></span> <span data-ttu-id="8e024-116">ワークフローが有効になっている場合にのみ使用できます。</span><span class="sxs-lookup"><span data-stu-id="8e024-116">Only available when workflow is enabled.</span></span> |
| <span data-ttu-id="8e024-117">200000002</span><span class="sxs-lookup"><span data-stu-id="8e024-117">200000002</span></span> | <span data-ttu-id="8e024-118">保留中</span><span class="sxs-lookup"><span data-stu-id="8e024-118">Pending</span></span> | <span data-ttu-id="8e024-119">要求が保留中のワークフロー アクションです。</span><span class="sxs-lookup"><span data-stu-id="8e024-119">The request is pending workflow action.</span></span> <span data-ttu-id="8e024-120">ワークフローが有効になっている場合にのみ使用できます。</span><span class="sxs-lookup"><span data-stu-id="8e024-120">Only available when workflow is enabled.</span></span> |
| <span data-ttu-id="8e024-121">200000003</span><span class="sxs-lookup"><span data-stu-id="8e024-121">200000003</span></span> | <span data-ttu-id="8e024-122">取消済</span><span class="sxs-lookup"><span data-stu-id="8e024-122">Canceled</span></span> | <span data-ttu-id="8e024-123">要求がキャンセルされました。</span><span class="sxs-lookup"><span data-stu-id="8e024-123">The request has been canceled.</span></span> <span data-ttu-id="8e024-124">ワークフローが有効になっている場合にのみ使用できます。</span><span class="sxs-lookup"><span data-stu-id="8e024-124">Only available when workflow is enabled.</span></span> |
| <span data-ttu-id="8e024-125">200000004</span><span class="sxs-lookup"><span data-stu-id="8e024-125">200000004</span></span> | <span data-ttu-id="8e024-126">拒否済</span><span class="sxs-lookup"><span data-stu-id="8e024-126">Denied</span></span> | <span data-ttu-id="8e024-127">要求が否認されました。</span><span class="sxs-lookup"><span data-stu-id="8e024-127">The request has been denied.</span></span> <span data-ttu-id="8e024-128">ワークフローが有効になっている場合にのみ使用できます。</span><span class="sxs-lookup"><span data-stu-id="8e024-128">Only available when workflow is enabled.</span></span> |
| <span data-ttu-id="8e024-129">200000005</span><span class="sxs-lookup"><span data-stu-id="8e024-129">200000005</span></span> | <span data-ttu-id="8e024-130">使用可能</span><span class="sxs-lookup"><span data-stu-id="8e024-130">Active</span></span> | <span data-ttu-id="8e024-131">ワークフローが完了して承認されると、その要求に対して有効な採用を行う準備が整います。</span><span class="sxs-lookup"><span data-stu-id="8e024-131">Any workflow is completed and approved, and the request is ready for active recruiting.</span></span> |
| <span data-ttu-id="8e024-132">200000006</span><span class="sxs-lookup"><span data-stu-id="8e024-132">200000006</span></span> | <span data-ttu-id="8e024-133">終了済</span><span class="sxs-lookup"><span data-stu-id="8e024-133">Closed</span></span> | <span data-ttu-id="8e024-134">採用要求が完了しました。</span><span class="sxs-lookup"><span data-stu-id="8e024-134">The recruiting request is closed.</span></span> |

## <a name="see-also"></a><span data-ttu-id="8e024-135">参照</span><span class="sxs-lookup"><span data-stu-id="8e024-135">See also</span></span>

[<span data-ttu-id="8e024-136">申請者追跡システム統合APIの概要</span><span class="sxs-lookup"><span data-stu-id="8e024-136">Applicant Tracking System integration API introduction</span></span>](hr-admin-integration-ats-api-introduction.md)<br>
[<span data-ttu-id="8e024-137">採用要求のクエリの例</span><span class="sxs-lookup"><span data-stu-id="8e024-137">Example query for Recruiting request</span></span>](hr-admin-integration-ats-api-recruiting-request-example-query.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]