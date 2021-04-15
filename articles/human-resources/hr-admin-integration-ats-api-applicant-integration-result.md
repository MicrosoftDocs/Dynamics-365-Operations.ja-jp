---
title: 申請者の統合結果
description: このトピックでは、Dynamics 365 Human Resources の申請者統合結果オプションについて説明します。
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
ms.openlocfilehash: e8e41fe485cc70a668d4610ce6eabba5cd16ac86
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/31/2021
ms.locfileid: "5795120"
---
# <a name="applicant-integration-result"></a><span data-ttu-id="c7bba-103">申請者の統合結果</span><span class="sxs-lookup"><span data-stu-id="c7bba-103">Applicant integration result</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="c7bba-104">このトピックでは、Dynamics 365 Human Resources の申請者統合結果オプションについて説明します。</span><span class="sxs-lookup"><span data-stu-id="c7bba-104">This topic describes the Applicant integration result option set for Dynamics 365 Human Resources.</span></span>

<span data-ttu-id="c7bba-105">物理名 : mshr_hcmapplicantintegrationresult</span><span class="sxs-lookup"><span data-stu-id="c7bba-105">Physical name: mshr_hcmapplicantintegrationresult</span></span>

<span data-ttu-id="c7bba-106">このリストは、候補者レコードの状態を表わします。</span><span class="sxs-lookup"><span data-stu-id="c7bba-106">This enumeration provides status for a candidate record.</span></span>

| <span data-ttu-id="c7bba-107">先頭値</span><span class="sxs-lookup"><span data-stu-id="c7bba-107">Value</span></span> | <span data-ttu-id="c7bba-108">ラベル</span><span class="sxs-lookup"><span data-stu-id="c7bba-108">Label</span></span> | <span data-ttu-id="c7bba-109">説明</span><span class="sxs-lookup"><span data-stu-id="c7bba-109">Description</span></span> |
| --- | --- | --- |
| <span data-ttu-id="c7bba-110">200000000</span><span class="sxs-lookup"><span data-stu-id="c7bba-110">200000000</span></span> | <span data-ttu-id="c7bba-111">処理されません</span><span class="sxs-lookup"><span data-stu-id="c7bba-111">Not processed</span></span> | <span data-ttu-id="c7bba-112">候補者がまだ検討中です。</span><span class="sxs-lookup"><span data-stu-id="c7bba-112">Candidate is still under consideration.</span></span> |
| <span data-ttu-id="c7bba-113">200000001</span><span class="sxs-lookup"><span data-stu-id="c7bba-113">200000001</span></span> | <span data-ttu-id="c7bba-114">雇用</span><span class="sxs-lookup"><span data-stu-id="c7bba-114">Hired</span></span> | <span data-ttu-id="c7bba-115">候補者が採用されました。</span><span class="sxs-lookup"><span data-stu-id="c7bba-115">The candidate has been hired.</span></span> |
| <span data-ttu-id="c7bba-116">200000002</span><span class="sxs-lookup"><span data-stu-id="c7bba-116">200000002</span></span> | <span data-ttu-id="c7bba-117">未採用</span><span class="sxs-lookup"><span data-stu-id="c7bba-117">Not hired</span></span> | <span data-ttu-id="c7bba-118">候補者を採用しない決定が下されました。</span><span class="sxs-lookup"><span data-stu-id="c7bba-118">Decision was made to not hire the candidate.</span></span> |
| <span data-ttu-id="c7bba-119">200000003</span><span class="sxs-lookup"><span data-stu-id="c7bba-119">200000003</span></span> | <span data-ttu-id="c7bba-120">解除済み</span><span class="sxs-lookup"><span data-stu-id="c7bba-120">Dismissed</span></span> | <span data-ttu-id="c7bba-121">候補者は検討から外されました。</span><span class="sxs-lookup"><span data-stu-id="c7bba-121">The candidate was dismissed from consideration.</span></span> |

## <a name="see-also"></a><span data-ttu-id="c7bba-122">参照</span><span class="sxs-lookup"><span data-stu-id="c7bba-122">See also</span></span>

[<span data-ttu-id="c7bba-123">申請者追跡システム統合APIの概要</span><span class="sxs-lookup"><span data-stu-id="c7bba-123">Applicant Tracking System integration API introduction</span></span>](hr-admin-integration-ats-api-introduction.md)<br>
[<span data-ttu-id="c7bba-124">採用する採用候補者に対するクエリの例</span><span class="sxs-lookup"><span data-stu-id="c7bba-124">Example query for Candidate to hire</span></span>](hr-admin-integration-ats-api-candidate-to-hire-example-query.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]