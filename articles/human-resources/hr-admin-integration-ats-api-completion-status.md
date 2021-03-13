---
title: 完了の状態
description: このトピックでは、Dynamics 365 Human Resources における完了の状態のオプションについて説明します。
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
ms.openlocfilehash: e9024e00b5d25117fd255084609c4f8db9284f32
ms.sourcegitcommit: 33b5c8bc4f9461e290513aa22de1ec1fba3b0742
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/05/2021
ms.locfileid: "5125692"
---
# <a name="completion-status"></a><span data-ttu-id="089ba-103">完了の状態</span><span class="sxs-lookup"><span data-stu-id="089ba-103">Completion status</span></span>

<span data-ttu-id="089ba-104">このトピックでは、Dynamics 365 Human Resources における完了の状態のオプションについて説明します。</span><span class="sxs-lookup"><span data-stu-id="089ba-104">This topic describes the Completion status option set for Dynamics 365 Human Resources.</span></span>

<span data-ttu-id="089ba-105">物理名 : mshr_hcmcompletionstatus</span><span class="sxs-lookup"><span data-stu-id="089ba-105">Physical name: mshr_hcmcompletionstatus</span></span>

<span data-ttu-id="089ba-106">このリストは、候補者の審査に対して、状態値のオプション セットを提供します。</span><span class="sxs-lookup"><span data-stu-id="089ba-106">This enumeration provides the option set of status values for candidate screenings.</span></span> 

| <span data-ttu-id="089ba-107">先頭値</span><span class="sxs-lookup"><span data-stu-id="089ba-107">Value</span></span> | <span data-ttu-id="089ba-108">ラベル</span><span class="sxs-lookup"><span data-stu-id="089ba-108">Label</span></span> | <span data-ttu-id="089ba-109">説明</span><span class="sxs-lookup"><span data-stu-id="089ba-109">Description</span></span> |
| --- | --- | --- |
| <span data-ttu-id="089ba-110">200000000</span><span class="sxs-lookup"><span data-stu-id="089ba-110">200000000</span></span> | <span data-ttu-id="089ba-111">未完了</span><span class="sxs-lookup"><span data-stu-id="089ba-111">Not Complete</span></span> | <span data-ttu-id="089ba-112">候補者の審査がまだ完了していません。</span><span class="sxs-lookup"><span data-stu-id="089ba-112">The candidate has not yet completed the screening.</span></span> |
| <span data-ttu-id="089ba-113">200000001</span><span class="sxs-lookup"><span data-stu-id="089ba-113">200000001</span></span> | <span data-ttu-id="089ba-114">成功</span><span class="sxs-lookup"><span data-stu-id="089ba-114">Pass</span></span> | <span data-ttu-id="089ba-115">候補者が審査に合格しました。</span><span class="sxs-lookup"><span data-stu-id="089ba-115">The candidate has passed the screening.</span></span> |
| <span data-ttu-id="089ba-116">200000002</span><span class="sxs-lookup"><span data-stu-id="089ba-116">200000002</span></span> | <span data-ttu-id="089ba-117">不合格</span><span class="sxs-lookup"><span data-stu-id="089ba-117">Fail</span></span> | <span data-ttu-id="089ba-118">候補者が審査に不合格となりました。</span><span class="sxs-lookup"><span data-stu-id="089ba-118">The candidate has failed the screening.</span></span> |

## <a name="see-also"></a><span data-ttu-id="089ba-119">参照</span><span class="sxs-lookup"><span data-stu-id="089ba-119">See also</span></span>

[<span data-ttu-id="089ba-120">申請者追跡システム統合APIの概要</span><span class="sxs-lookup"><span data-stu-id="089ba-120">Applicant Tracking System integration API introduction</span></span>](hr-admin-integration-ats-api-introduction.md)<br>
[<span data-ttu-id="089ba-121">採用する採用候補者に対するクエリの例</span><span class="sxs-lookup"><span data-stu-id="089ba-121">Example query for Candidate to hire</span></span>](hr-admin-integration-ats-api-candidate-to-hire-example-query.md)
