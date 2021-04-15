---
title: 完了の状態
description: このトピックでは、Dynamics 365 Human Resources における完了の状態のオプションについて説明します。
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
ms.openlocfilehash: f1b0c61ac9d9dc611d2a4700a1a004e3d15b4445
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/31/2021
ms.locfileid: "5798372"
---
# <a name="completion-status"></a><span data-ttu-id="cd1b5-103">完了の状態</span><span class="sxs-lookup"><span data-stu-id="cd1b5-103">Completion status</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="cd1b5-104">このトピックでは、Dynamics 365 Human Resources における完了の状態のオプションについて説明します。</span><span class="sxs-lookup"><span data-stu-id="cd1b5-104">This topic describes the Completion status option set for Dynamics 365 Human Resources.</span></span>

<span data-ttu-id="cd1b5-105">物理名 : mshr_hcmcompletionstatus</span><span class="sxs-lookup"><span data-stu-id="cd1b5-105">Physical name: mshr_hcmcompletionstatus</span></span>

<span data-ttu-id="cd1b5-106">このリストは、候補者の審査に対して、状態値のオプション セットを提供します。</span><span class="sxs-lookup"><span data-stu-id="cd1b5-106">This enumeration provides the option set of status values for candidate screenings.</span></span> 

| <span data-ttu-id="cd1b5-107">先頭値</span><span class="sxs-lookup"><span data-stu-id="cd1b5-107">Value</span></span> | <span data-ttu-id="cd1b5-108">ラベル</span><span class="sxs-lookup"><span data-stu-id="cd1b5-108">Label</span></span> | <span data-ttu-id="cd1b5-109">説明</span><span class="sxs-lookup"><span data-stu-id="cd1b5-109">Description</span></span> |
| --- | --- | --- |
| <span data-ttu-id="cd1b5-110">200000000</span><span class="sxs-lookup"><span data-stu-id="cd1b5-110">200000000</span></span> | <span data-ttu-id="cd1b5-111">未完了</span><span class="sxs-lookup"><span data-stu-id="cd1b5-111">Not Complete</span></span> | <span data-ttu-id="cd1b5-112">候補者の審査がまだ完了していません。</span><span class="sxs-lookup"><span data-stu-id="cd1b5-112">The candidate has not yet completed the screening.</span></span> |
| <span data-ttu-id="cd1b5-113">200000001</span><span class="sxs-lookup"><span data-stu-id="cd1b5-113">200000001</span></span> | <span data-ttu-id="cd1b5-114">成功</span><span class="sxs-lookup"><span data-stu-id="cd1b5-114">Pass</span></span> | <span data-ttu-id="cd1b5-115">候補者が審査に合格しました。</span><span class="sxs-lookup"><span data-stu-id="cd1b5-115">The candidate has passed the screening.</span></span> |
| <span data-ttu-id="cd1b5-116">200000002</span><span class="sxs-lookup"><span data-stu-id="cd1b5-116">200000002</span></span> | <span data-ttu-id="cd1b5-117">不合格</span><span class="sxs-lookup"><span data-stu-id="cd1b5-117">Fail</span></span> | <span data-ttu-id="cd1b5-118">候補者が審査に不合格となりました。</span><span class="sxs-lookup"><span data-stu-id="cd1b5-118">The candidate has failed the screening.</span></span> |

## <a name="see-also"></a><span data-ttu-id="cd1b5-119">参照</span><span class="sxs-lookup"><span data-stu-id="cd1b5-119">See also</span></span>

[<span data-ttu-id="cd1b5-120">申請者追跡システム統合APIの概要</span><span class="sxs-lookup"><span data-stu-id="cd1b5-120">Applicant Tracking System integration API introduction</span></span>](hr-admin-integration-ats-api-introduction.md)<br>
[<span data-ttu-id="cd1b5-121">採用する採用候補者に対するクエリの例</span><span class="sxs-lookup"><span data-stu-id="cd1b5-121">Example query for Candidate to hire</span></span>](hr-admin-integration-ats-api-candidate-to-hire-example-query.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]