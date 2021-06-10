---
title: 完了の状態
description: このトピックでは、Dynamics 365 Human Resources における完了の状態のオプションについて説明します。
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
ms.openlocfilehash: 54ad5cc8f5f18d57b6713304cceb985acfdc93d1
ms.sourcegitcommit: 879ee8a10e6158885795dce4b3db5077540eec41
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/18/2021
ms.locfileid: "6055367"
---
# <a name="completion-status"></a><span data-ttu-id="b2b51-103">完了の状態</span><span class="sxs-lookup"><span data-stu-id="b2b51-103">Completion status</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="b2b51-104">このトピックでは、Dynamics 365 Human Resources における完了の状態のオプションについて説明します。</span><span class="sxs-lookup"><span data-stu-id="b2b51-104">This topic describes the Completion status option set for Dynamics 365 Human Resources.</span></span>

<span data-ttu-id="b2b51-105">物理名 : mshr_hcmcompletionstatus</span><span class="sxs-lookup"><span data-stu-id="b2b51-105">Physical name: mshr_hcmcompletionstatus</span></span>

<span data-ttu-id="b2b51-106">このリストは、候補者の審査に対して、状態値のオプション セットを提供します。</span><span class="sxs-lookup"><span data-stu-id="b2b51-106">This enumeration provides the option set of status values for candidate screenings.</span></span> 

| <span data-ttu-id="b2b51-107">先頭値</span><span class="sxs-lookup"><span data-stu-id="b2b51-107">Value</span></span> | <span data-ttu-id="b2b51-108">ラベル</span><span class="sxs-lookup"><span data-stu-id="b2b51-108">Label</span></span> | <span data-ttu-id="b2b51-109">説明</span><span class="sxs-lookup"><span data-stu-id="b2b51-109">Description</span></span> |
| --- | --- | --- |
| <span data-ttu-id="b2b51-110">200000000</span><span class="sxs-lookup"><span data-stu-id="b2b51-110">200000000</span></span> | <span data-ttu-id="b2b51-111">未完了</span><span class="sxs-lookup"><span data-stu-id="b2b51-111">Not Complete</span></span> | <span data-ttu-id="b2b51-112">候補者の審査がまだ完了していません。</span><span class="sxs-lookup"><span data-stu-id="b2b51-112">The candidate has not yet completed the screening.</span></span> |
| <span data-ttu-id="b2b51-113">200000001</span><span class="sxs-lookup"><span data-stu-id="b2b51-113">200000001</span></span> | <span data-ttu-id="b2b51-114">成功</span><span class="sxs-lookup"><span data-stu-id="b2b51-114">Pass</span></span> | <span data-ttu-id="b2b51-115">候補者が審査に合格しました。</span><span class="sxs-lookup"><span data-stu-id="b2b51-115">The candidate has passed the screening.</span></span> |
| <span data-ttu-id="b2b51-116">200000002</span><span class="sxs-lookup"><span data-stu-id="b2b51-116">200000002</span></span> | <span data-ttu-id="b2b51-117">不合格</span><span class="sxs-lookup"><span data-stu-id="b2b51-117">Fail</span></span> | <span data-ttu-id="b2b51-118">候補者が審査に不合格となりました。</span><span class="sxs-lookup"><span data-stu-id="b2b51-118">The candidate has failed the screening.</span></span> |

## <a name="see-also"></a><span data-ttu-id="b2b51-119">参照</span><span class="sxs-lookup"><span data-stu-id="b2b51-119">See also</span></span>

[<span data-ttu-id="b2b51-120">申請者追跡システム統合APIの概要</span><span class="sxs-lookup"><span data-stu-id="b2b51-120">Applicant Tracking System integration API introduction</span></span>](hr-admin-integration-ats-api-introduction.md)<br>
[<span data-ttu-id="b2b51-121">採用する採用候補者に対するクエリの例</span><span class="sxs-lookup"><span data-stu-id="b2b51-121">Example query for Candidate to hire</span></span>](hr-admin-integration-ats-api-candidate-to-hire-example-query.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]