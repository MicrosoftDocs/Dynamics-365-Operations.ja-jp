---
title: 採用で要求する職位の状態
description: このトピックでは、Dynamics 365 Human Resources の採用で要求する職位の状態のオプションセットについて説明します。
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
ms.openlocfilehash: 01e8aa5157d0ad1c01f996886e7845e49ab97603
ms.sourcegitcommit: 6affb3316be757c99e1fe9c7c7b312b93c483408
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/17/2021
ms.locfileid: "5464721"
---
# <a name="recruiting-request-position-status"></a><span data-ttu-id="0fcd6-103">採用で要求する職位の状態</span><span class="sxs-lookup"><span data-stu-id="0fcd6-103">Recruiting request position status</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="0fcd6-104">このトピックでは、Dynamics 365 Human Resources の採用で要求する職位の状態のオプションセットについて説明します。</span><span class="sxs-lookup"><span data-stu-id="0fcd6-104">This topic describes the Recruiting request position status option set for Dynamics 365 Human Resources.</span></span>

<span data-ttu-id="0fcd6-105">物理名 : mshr_hcmrecruitingrequestpositionstatus</span><span class="sxs-lookup"><span data-stu-id="0fcd6-105">Physical name: mshr_hcmrecruitingrequestpositionstatus</span></span>

<span data-ttu-id="0fcd6-106">このリストでは、 RecruitingRequestPosition エンティティ内の採用で要求する職位の状態に対するオプション セットを提供します。</span><span class="sxs-lookup"><span data-stu-id="0fcd6-106">This enumeration provides the option set for the status values of each position a recruiting request in the RecruitingRequestPosition entity.</span></span>

| <span data-ttu-id="0fcd6-107">先頭値</span><span class="sxs-lookup"><span data-stu-id="0fcd6-107">Value</span></span> | <span data-ttu-id="0fcd6-108">ラベル</span><span class="sxs-lookup"><span data-stu-id="0fcd6-108">Label</span></span> | <span data-ttu-id="0fcd6-109">説明</span><span class="sxs-lookup"><span data-stu-id="0fcd6-109">Description</span></span> |
| --- | --- | --- |
| <span data-ttu-id="0fcd6-110">200000000</span><span class="sxs-lookup"><span data-stu-id="0fcd6-110">200000000</span></span> | <span data-ttu-id="0fcd6-111">空いている</span><span class="sxs-lookup"><span data-stu-id="0fcd6-111">Open</span></span> | <span data-ttu-id="0fcd6-112">募集中となっている職位です。</span><span class="sxs-lookup"><span data-stu-id="0fcd6-112">The position in the recruiting request is open for recruiting.</span></span> <span data-ttu-id="0fcd6-113">これは、現在アクティブな職位の割り当てがないことを示すものではありません。</span><span class="sxs-lookup"><span data-stu-id="0fcd6-113">This does not indicate that there is no currently active position assignment for the position.</span></span> <span data-ttu-id="0fcd6-114">採用時に職位に従業員が存在する場合があります。</span><span class="sxs-lookup"><span data-stu-id="0fcd6-114">There may be an employee in the position at the time of recruiting.</span></span> <span data-ttu-id="0fcd6-115">これは、職位が採用要求のコンテキストにおいて採用に利用できる状態のみを示します。</span><span class="sxs-lookup"><span data-stu-id="0fcd6-115">It indicates only that the position is available for recruiting in the context of the recruiting request.</span></span> |
| <span data-ttu-id="0fcd6-116">200000001</span><span class="sxs-lookup"><span data-stu-id="0fcd6-116">200000001</span></span> | <span data-ttu-id="0fcd6-117">採用済み</span><span class="sxs-lookup"><span data-stu-id="0fcd6-117">Filled</span></span> | <span data-ttu-id="0fcd6-118">職位への割り当てに従業員が選択されています。</span><span class="sxs-lookup"><span data-stu-id="0fcd6-118">A worker has been selected for assignment to the position.</span></span> |
| <span data-ttu-id="0fcd6-119">200000002</span><span class="sxs-lookup"><span data-stu-id="0fcd6-119">200000002</span></span> | <span data-ttu-id="0fcd6-120">取消済</span><span class="sxs-lookup"><span data-stu-id="0fcd6-120">Canceled</span></span> | <span data-ttu-id="0fcd6-121">この職位に対する採用の要求はキャンセルされました。</span><span class="sxs-lookup"><span data-stu-id="0fcd6-121">The request to recruit for this position has been canceled.</span></span> |

## <a name="see-also"></a><span data-ttu-id="0fcd6-122">参照</span><span class="sxs-lookup"><span data-stu-id="0fcd6-122">See also</span></span>

[<span data-ttu-id="0fcd6-123">申請者追跡システム統合APIの概要</span><span class="sxs-lookup"><span data-stu-id="0fcd6-123">Applicant Tracking System integration API introduction</span></span>](hr-admin-integration-ats-api-introduction.md)<br>
[<span data-ttu-id="0fcd6-124">採用要求のクエリの例</span><span class="sxs-lookup"><span data-stu-id="0fcd6-124">Example query for Recruiting request</span></span>](hr-admin-integration-ats-api-recruiting-request-example-query.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]