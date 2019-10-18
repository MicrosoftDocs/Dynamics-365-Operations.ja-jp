---
title: 経費レポートでの配分
description: 経費精算書に経費を入力すると、組織内の複数のプロジェクト、法人、勘定に経費を配分できます。
author: ShylaThompson
manager: AnnBe
ms.date: 09/19/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: b450c952bd53d6e573b08cfcfd86ad666f743040
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/27/2019
ms.locfileid: "2187639"
---
# <a name="distributions-on-an-expense-report"></a><span data-ttu-id="f4ee8-103">経費レポートでの配分</span><span class="sxs-lookup"><span data-stu-id="f4ee8-103">Distributions on an expense report</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="f4ee8-104"> 経費精算書に経費を入力すると、組織内の複数のプロジェクト、財務分析コード、勘定に経費を配分できます。</span><span class="sxs-lookup"><span data-stu-id="f4ee8-104">When you enter expenses on an expense report, you can distribute the expense across multiple projects, financial dimensions, or accounts in your organization.</span></span>

<span data-ttu-id="f4ee8-105">たとえば、Fabrikam の販売担当者ナンシーは、コペンハーゲンからブランクフルトに旅行しました。</span><span class="sxs-lookup"><span data-stu-id="f4ee8-105">For example, Nancy, a Fabrikam sales representative, traveled from Copenhagen to Frankfurt.</span></span> <span data-ttu-id="f4ee8-106">ブランクフルトでは、2 つの組織と会い、各組織の別個のプロジェクトについて話し合いました。</span><span class="sxs-lookup"><span data-stu-id="f4ee8-106">In Frankfurt, she met with two organizations to discuss separate projects for each organization.</span></span> <span data-ttu-id="f4ee8-107">ナンシーは、プロジェクト A に関して組織 A と 7 営業日作業し、プロジェクト B に関して組織 B と 3 営業日作業しました。</span><span class="sxs-lookup"><span data-stu-id="f4ee8-107">Nancy spent seven business days working with organization A on project A, and three business days working with organization B on project B.</span></span>

<span data-ttu-id="f4ee8-108">ナンシーはフランクフルトで 2 つの異なるプロジェクトの仕事をしたため、彼女は経費レポートを入力するとき、各プロジェクトに応じて経費を配分します。</span><span class="sxs-lookup"><span data-stu-id="f4ee8-108">Because Nancy worked on two separate projects when she was in Frankfurt, when she enters her expense report, she distributes her expenses as appropriate for each project.</span></span> <span data-ttu-id="f4ee8-109">ナンシーが自分の経費をどのように配分するかを次の表に示します。</span><span class="sxs-lookup"><span data-stu-id="f4ee8-109">The following table shows how Nancy distributed her expenses.</span></span>


| <span data-ttu-id="f4ee8-110">経費タイプ</span><span class="sxs-lookup"><span data-stu-id="f4ee8-110">Expense type</span></span> | <span data-ttu-id="f4ee8-111">経費合計金額</span><span class="sxs-lookup"><span data-stu-id="f4ee8-111">Total expense amount</span></span>|<span data-ttu-id="f4ee8-112">プロジェクト A に配分する量</span><span class="sxs-lookup"><span data-stu-id="f4ee8-112">Amount distributed to project A</span></span>| <span data-ttu-id="f4ee8-113">プロジェクト B に配分する量</span><span class="sxs-lookup"><span data-stu-id="f4ee8-113">Amount distributed to project B</span></span> |
|--------------|---------------------|-------------------------------|---------------------------------|
|<span data-ttu-id="f4ee8-114">トレーニング手数料</span><span class="sxs-lookup"><span data-stu-id="f4ee8-114">Train fare</span></span>   |<span data-ttu-id="f4ee8-115">DKK 578</span><span class="sxs-lookup"><span data-stu-id="f4ee8-115">DKK 578</span></span>              |<span data-ttu-id="f4ee8-116">DKK 405</span><span class="sxs-lookup"><span data-stu-id="f4ee8-116">DKK 405</span></span>                        |<span data-ttu-id="f4ee8-117">DKK 173</span><span class="sxs-lookup"><span data-stu-id="f4ee8-117">DKK 173</span></span>                          |
|<span data-ttu-id="f4ee8-118">ホテル</span><span class="sxs-lookup"><span data-stu-id="f4ee8-118">Hotel</span></span>         |<span data-ttu-id="f4ee8-119">EUR 725</span><span class="sxs-lookup"><span data-stu-id="f4ee8-119">EUR 725</span></span>              |<span data-ttu-id="f4ee8-120">EUR 557</span><span class="sxs-lookup"><span data-stu-id="f4ee8-120">EUR 557</span></span>                        |<span data-ttu-id="f4ee8-121">EUR 168</span><span class="sxs-lookup"><span data-stu-id="f4ee8-121">EUR 168</span></span>                          |
|<span data-ttu-id="f4ee8-122">食費</span><span class="sxs-lookup"><span data-stu-id="f4ee8-122">Meals</span></span>         |<span data-ttu-id="f4ee8-123">EUR 346</span><span class="sxs-lookup"><span data-stu-id="f4ee8-123">EUR 346</span></span>              |<span data-ttu-id="f4ee8-124">EUR 284</span><span class="sxs-lookup"><span data-stu-id="f4ee8-124">EUR 284</span></span>                        |<span data-ttu-id="f4ee8-125">EUR 62</span><span class="sxs-lookup"><span data-stu-id="f4ee8-125">EUR 62</span></span>                           |

