---
title: 採用で要求する職位の状態
description: このトピックでは、Dynamics 365 Human Resources の採用で要求する職位の状態のオプションセットについて説明します。
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
ms.openlocfilehash: e287ec4b9b78194b76ef3c993c6ce32f808e26f9
ms.sourcegitcommit: 879ee8a10e6158885795dce4b3db5077540eec41
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/18/2021
ms.locfileid: "6051884"
---
# <a name="recruiting-request-position-status"></a><span data-ttu-id="d0ad1-103">採用で要求する職位の状態</span><span class="sxs-lookup"><span data-stu-id="d0ad1-103">Recruiting request position status</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="d0ad1-104">このトピックでは、Dynamics 365 Human Resources の採用で要求する職位の状態のオプションセットについて説明します。</span><span class="sxs-lookup"><span data-stu-id="d0ad1-104">This topic describes the Recruiting request position status option set for Dynamics 365 Human Resources.</span></span>

<span data-ttu-id="d0ad1-105">物理名 : mshr_hcmrecruitingrequestpositionstatus</span><span class="sxs-lookup"><span data-stu-id="d0ad1-105">Physical name: mshr_hcmrecruitingrequestpositionstatus</span></span>

<span data-ttu-id="d0ad1-106">このリストでは、 RecruitingRequestPosition エンティティ内の採用で要求する職位の状態に対するオプション セットを提供します。</span><span class="sxs-lookup"><span data-stu-id="d0ad1-106">This enumeration provides the option set for the status values of each position a recruiting request in the RecruitingRequestPosition entity.</span></span>

| <span data-ttu-id="d0ad1-107">先頭値</span><span class="sxs-lookup"><span data-stu-id="d0ad1-107">Value</span></span> | <span data-ttu-id="d0ad1-108">ラベル</span><span class="sxs-lookup"><span data-stu-id="d0ad1-108">Label</span></span> | <span data-ttu-id="d0ad1-109">説明</span><span class="sxs-lookup"><span data-stu-id="d0ad1-109">Description</span></span> |
| --- | --- | --- |
| <span data-ttu-id="d0ad1-110">200000000</span><span class="sxs-lookup"><span data-stu-id="d0ad1-110">200000000</span></span> | <span data-ttu-id="d0ad1-111">空いている</span><span class="sxs-lookup"><span data-stu-id="d0ad1-111">Open</span></span> | <span data-ttu-id="d0ad1-112">募集中となっている職位です。</span><span class="sxs-lookup"><span data-stu-id="d0ad1-112">The position in the recruiting request is open for recruiting.</span></span> <span data-ttu-id="d0ad1-113">これは、現在アクティブな職位の割り当てがないことを示すものではありません。</span><span class="sxs-lookup"><span data-stu-id="d0ad1-113">This does not indicate that there is no currently active position assignment for the position.</span></span> <span data-ttu-id="d0ad1-114">採用時に職位に従業員が存在する場合があります。</span><span class="sxs-lookup"><span data-stu-id="d0ad1-114">There may be an employee in the position at the time of recruiting.</span></span> <span data-ttu-id="d0ad1-115">これは、職位が採用要求のコンテキストにおいて採用に利用できる状態のみを示します。</span><span class="sxs-lookup"><span data-stu-id="d0ad1-115">It indicates only that the position is available for recruiting in the context of the recruiting request.</span></span> |
| <span data-ttu-id="d0ad1-116">200000001</span><span class="sxs-lookup"><span data-stu-id="d0ad1-116">200000001</span></span> | <span data-ttu-id="d0ad1-117">採用済み</span><span class="sxs-lookup"><span data-stu-id="d0ad1-117">Filled</span></span> | <span data-ttu-id="d0ad1-118">職位への割り当てに従業員が選択されています。</span><span class="sxs-lookup"><span data-stu-id="d0ad1-118">A worker has been selected for assignment to the position.</span></span> |
| <span data-ttu-id="d0ad1-119">200000002</span><span class="sxs-lookup"><span data-stu-id="d0ad1-119">200000002</span></span> | <span data-ttu-id="d0ad1-120">取消済</span><span class="sxs-lookup"><span data-stu-id="d0ad1-120">Canceled</span></span> | <span data-ttu-id="d0ad1-121">この職位に対する採用の要求はキャンセルされました。</span><span class="sxs-lookup"><span data-stu-id="d0ad1-121">The request to recruit for this position has been canceled.</span></span> |

## <a name="see-also"></a><span data-ttu-id="d0ad1-122">参照</span><span class="sxs-lookup"><span data-stu-id="d0ad1-122">See also</span></span>

[<span data-ttu-id="d0ad1-123">申請者追跡システム統合APIの概要</span><span class="sxs-lookup"><span data-stu-id="d0ad1-123">Applicant Tracking System integration API introduction</span></span>](hr-admin-integration-ats-api-introduction.md)<br>
[<span data-ttu-id="d0ad1-124">採用要求のクエリの例</span><span class="sxs-lookup"><span data-stu-id="d0ad1-124">Example query for Recruiting request</span></span>](hr-admin-integration-ats-api-recruiting-request-example-query.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]