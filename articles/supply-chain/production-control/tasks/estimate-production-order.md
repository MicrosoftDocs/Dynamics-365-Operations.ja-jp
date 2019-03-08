---
title: 製造オーダーの見積
description: USMF デモ データ会社または用意したデータ セットを使用して、この手順を実行できます。
author: johanhoffmann
manager: AnnBe
ms.date: 11/11/2016
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 8274e390a177f51649f5cad70ef7ad5bd50a8830
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/29/2019
ms.locfileid: "351864"
---
# <a name="estimate-a-production-order"></a><span data-ttu-id="ce78d-103">製造オーダーの見積</span><span class="sxs-lookup"><span data-stu-id="ce78d-103">Estimate a production order</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="ce78d-104">USMF デモ データ会社または用意したデータ セットを使用して、この手順を実行できます。</span><span class="sxs-lookup"><span data-stu-id="ce78d-104">You can run this procedure by using the USMF demo data company or your own data set.</span></span> <span data-ttu-id="ce78d-105">どちらの場合も、ステータスが [作成済] である未処理の製造オーダーが必要です。</span><span class="sxs-lookup"><span data-stu-id="ce78d-105">In both cases, you need to have an open production order that has the Created status.</span></span> <span data-ttu-id="ce78d-106">これは、製造オーダーのライフ サイクルを説明する 7 個の手順の 2 番目です。</span><span class="sxs-lookup"><span data-stu-id="ce78d-106">This is the second procedure out of seven which explains the production order lifecycle.</span></span>


## <a name="estimate-a-production-order"></a><span data-ttu-id="ce78d-107">製造オーダーの見積</span><span class="sxs-lookup"><span data-stu-id="ce78d-107">Estimate a production order</span></span>
1. <span data-ttu-id="ce78d-108">[生産管理] > [製造オーダー] > [すべての製造オーダー] の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="ce78d-108">Go to Production control > Production orders > All production orders.</span></span>
2. <span data-ttu-id="ce78d-109">グリッドでステータスが [作成済] の注文を選択します。</span><span class="sxs-lookup"><span data-stu-id="ce78d-109">Select an order that has the Created status in the grid.</span></span>
3. <span data-ttu-id="ce78d-110">アクション ウィンドウで、[製造オーダー] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="ce78d-110">On the Action Pane, click Production order.</span></span>
4. <span data-ttu-id="ce78d-111">[見積] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="ce78d-111">Click Estimate.</span></span>
    * <span data-ttu-id="ce78d-112">このステップでは、1 つの製造オーダーの見積原価が計算されます。</span><span class="sxs-lookup"><span data-stu-id="ce78d-112">In this step, the estimated costs of a single production order is calculated.</span></span>   
5. <span data-ttu-id="ce78d-113">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="ce78d-113">Click OK.</span></span>

## <a name="view-the-calculation-details"></a><span data-ttu-id="ce78d-114">計算の詳細の表示</span><span class="sxs-lookup"><span data-stu-id="ce78d-114">View the calculation details</span></span>
1. <span data-ttu-id="ce78d-115">[アクション] ペインで [原価の管理] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="ce78d-115">On the Action Pane, click Manage costs.</span></span>
2. <span data-ttu-id="ce78d-116">[計算の詳細の表示] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="ce78d-116">Click View calculation details.</span></span>
    * <span data-ttu-id="ce78d-117">このページは、原価内訳を表示します。</span><span class="sxs-lookup"><span data-stu-id="ce78d-117">This page displays the cost breakdown.</span></span> <span data-ttu-id="ce78d-118">たとえば、先頭行の完成品の単位あたりの原価価格合計を表示できます。</span><span class="sxs-lookup"><span data-stu-id="ce78d-118">For example, you can view the total cost price per unit for the finished product in the first row.</span></span> <span data-ttu-id="ce78d-119">後続の行には、部品表、生産工順、および間接原価などの原価が含まれます。</span><span class="sxs-lookup"><span data-stu-id="ce78d-119">The subsequent rows contain costs according to the bill of materials, production route, and indirect costs.</span></span>  
