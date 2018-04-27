---
title: "経費レポートでの配分"
description: "経費精算書に経費を入力すると、組織内の複数のプロジェクト、法人、勘定に経費を配分できます。"
author: saraschi2
manager: AnnBe
ms.date: 09/19/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom:
- month/year of release that feature was introduced in
- in format yyyy-mm-dd
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: 0f3f50061fc5b9b4cfc00000492840061fc3b386
ms.contentlocale: ja-jp
ms.lasthandoff: 04/13/2018

---

# <a name="distributions-on-an-expense-report"></a><span data-ttu-id="b83d0-103">経費レポートでの配分</span><span class="sxs-lookup"><span data-stu-id="b83d0-103">Distributions on an expense report</span></span>

[!INCLUDE [banner](../includes/banner.md)]

<span data-ttu-id="b83d0-104"> 経費精算書に経費を入力すると、組織内の複数のプロジェクト、財務分析コード、勘定に経費を配分できます。</span><span class="sxs-lookup"><span data-stu-id="b83d0-104">When you enter expenses on an expense report, you can distribute the expense across multiple projects, financial dimensions, or accounts in your organization.</span></span>

<span data-ttu-id="b83d0-105">たとえば、Fabrikam の販売担当者ナンシーは、コペンハーゲンからブランクフルトに旅行しました。</span><span class="sxs-lookup"><span data-stu-id="b83d0-105">For example, Nancy, a Fabrikam sales representative, traveled from Copenhagen to Frankfurt.</span></span> <span data-ttu-id="b83d0-106">ブランクフルトでは、2 つの組織と会い、各組織の別個のプロジェクトについて話し合いました。</span><span class="sxs-lookup"><span data-stu-id="b83d0-106">In Frankfurt, she met with two organizations to discuss separate projects for each organization.</span></span> <span data-ttu-id="b83d0-107">ナンシーは、プロジェクト A に関して組織 A と 7 営業日作業し、プロジェクト B に関して組織 B と 3 営業日作業しました。</span><span class="sxs-lookup"><span data-stu-id="b83d0-107">Nancy spent seven business days working with organization A on project A, and three business days working with organization B on project B.</span></span>

<span data-ttu-id="b83d0-108">ナンシーはフランクフルトで 2 つの異なるプロジェクトの仕事をしたため、彼女は経費レポートを入力するとき、各プロジェクトに応じて経費を配分します。</span><span class="sxs-lookup"><span data-stu-id="b83d0-108">Because Nancy worked on two separate projects when she was in Frankfurt, when she enters her expense report, she distributes her expenses as appropriate for each project.</span></span> <span data-ttu-id="b83d0-109">ナンシーが自分の経費をどのように配分するかを次の表に示します。</span><span class="sxs-lookup"><span data-stu-id="b83d0-109">The following table shows how Nancy distributed her expenses.</span></span>


| <span data-ttu-id="b83d0-110"><strong>経費タイプ</strong></span><span class="sxs-lookup"><span data-stu-id="b83d0-110"><strong>Expense type</strong></span></span> | <span data-ttu-id="b83d0-111"><strong>経費合計金額</strong></span><span class="sxs-lookup"><span data-stu-id="b83d0-111"><strong>Total expense amount</strong></span></span> | <span data-ttu-id="b83d0-112"><strong>プロジェクト A に配分する量</strong></span><span class="sxs-lookup"><span data-stu-id="b83d0-112"><strong>Amount distributed to project A</strong></span></span> | <span data-ttu-id="b83d0-113"><strong>プロジェクト B に配分する量</strong></span><span class="sxs-lookup"><span data-stu-id="b83d0-113"><strong>Amount distributed to project B</strong></span></span> |
|-------------------------------|---------------------------------------|--------------------------------------------------|--------------------------------------------------|
|          <span data-ttu-id="b83d0-114">トレーニング手数料</span><span class="sxs-lookup"><span data-stu-id="b83d0-114">Train fare</span></span>           |                <span data-ttu-id="b83d0-115">DKK 578</span><span class="sxs-lookup"><span data-stu-id="b83d0-115">DKK 578</span></span>                |                     <span data-ttu-id="b83d0-116">DKK 405</span><span class="sxs-lookup"><span data-stu-id="b83d0-116">DKK 405</span></span>                      |                     <span data-ttu-id="b83d0-117">DKK 173</span><span class="sxs-lookup"><span data-stu-id="b83d0-117">DKK 173</span></span>                      |
|             <span data-ttu-id="b83d0-118">ホテル</span><span class="sxs-lookup"><span data-stu-id="b83d0-118">Hotel</span></span>             |                <span data-ttu-id="b83d0-119">EUR 725</span><span class="sxs-lookup"><span data-stu-id="b83d0-119">EUR 725</span></span>                |                     <span data-ttu-id="b83d0-120">EUR 557</span><span class="sxs-lookup"><span data-stu-id="b83d0-120">EUR 557</span></span>                      |                     <span data-ttu-id="b83d0-121">EUR 168</span><span class="sxs-lookup"><span data-stu-id="b83d0-121">EUR 168</span></span>                      |
|             <span data-ttu-id="b83d0-122">食費</span><span class="sxs-lookup"><span data-stu-id="b83d0-122">Meals</span></span>             |                <span data-ttu-id="b83d0-123">EUR 346</span><span class="sxs-lookup"><span data-stu-id="b83d0-123">EUR 346</span></span>                |                     <span data-ttu-id="b83d0-124">EUR 284</span><span class="sxs-lookup"><span data-stu-id="b83d0-124">EUR 284</span></span>                      |                      <span data-ttu-id="b83d0-125">EUR 62</span><span class="sxs-lookup"><span data-stu-id="b83d0-125">EUR 62</span></span>                      |


