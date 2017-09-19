--- 
title: "固定資産への追加物の入力"
description: "この手順では、既存の固定資産への追加物を追加する方法を示します。"
author: saraschi2
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: 4c22fb105d0deedda1b7dbfdd919d1745ad0ca2f
ms.contentlocale: ja-jp
ms.lasthandoff: 08/29/2017

---
# <a name="enter-an-addition-to-a-fixed-asset"></a><span data-ttu-id="61890-103">固定資産への追加物の入力</span><span class="sxs-lookup"><span data-stu-id="61890-103">Enter an addition to a fixed asset</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="61890-104">この手順では、既存の固定資産への追加物を追加する方法を示します。</span><span class="sxs-lookup"><span data-stu-id="61890-104">This procedure shows how to add an addition to an existing fixed asset.</span></span> <span data-ttu-id="61890-105">固定資産の付属品の目的は、品目の追加、メンテナンス、改善を追跡することであり、情報提供のみを目的としています。</span><span class="sxs-lookup"><span data-stu-id="61890-105">The purpose of Fixed asset additions is to track item additions, maintenance, or improvements for an asset, and is informational only.</span></span> <span data-ttu-id="61890-106">固定資産価値または耐用年数の変更はすべて、個別に行う必要があります。</span><span class="sxs-lookup"><span data-stu-id="61890-106">Any changes to the fixed asset value or service life must be made separately.</span></span>   



<span data-ttu-id="61890-107">この手順では USMF の法人に対して経理担当ロールとデモ データを使用します。</span><span class="sxs-lookup"><span data-stu-id="61890-107">The procedure uses the Accountant role and demo data for the USMF legal entity.</span></span>

1. <span data-ttu-id="61890-108">[固定資産] > [固定資産] > [固定資産] に移動します。</span><span class="sxs-lookup"><span data-stu-id="61890-108">Go to Fixed assets > Fixed assets > Fixed assets.</span></span>
2. <span data-ttu-id="61890-109">一覧で、付属品に関連する固定資産を見つけ、選択します。</span><span class="sxs-lookup"><span data-stu-id="61890-109">In the list, find and select the fixed asset for the addition.</span></span>
3. <span data-ttu-id="61890-110">一覧で、選択された行のリンクをクリックします。</span><span class="sxs-lookup"><span data-stu-id="61890-110">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="61890-111">[アクション] ウィンドウで、[固定資産] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="61890-111">On the Action Pane, click Fixed asset.</span></span>
5. <span data-ttu-id="61890-112">[固定資産の追加物] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="61890-112">Click Fixed asset additions.</span></span>
6. <span data-ttu-id="61890-113">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="61890-113">Click New.</span></span>
7. <span data-ttu-id="61890-114">[名前] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="61890-114">In the Name field, type a value.</span></span>
8. <span data-ttu-id="61890-115">追加の購買またはサービスの日付を設定します。</span><span class="sxs-lookup"><span data-stu-id="61890-115">Set the date of the addition purchase or service.</span></span>
9. <span data-ttu-id="61890-116">資産に関する品目、保守、またはその他の改良の原価を入力します。</span><span class="sxs-lookup"><span data-stu-id="61890-116">Enter the cost of the item, maintenance, or other improvement for the asset.</span></span>
10. <span data-ttu-id="61890-117">[数量] フィールドに数値を入力します。</span><span class="sxs-lookup"><span data-stu-id="61890-117">In the Quantity field, enter a number.</span></span>
    * <span data-ttu-id="61890-118">原価合計は、固定資産の値に影響せず、追跡および情報目的でのみ使用されます。</span><span class="sxs-lookup"><span data-stu-id="61890-118">The total cost will have no impact on the value of the fixed asset and is for tracking and informational purposes only.</span></span> <span data-ttu-id="61890-119">原価が資本化される場合、評価増調整トランザクションは個別に転記する必要があります。</span><span class="sxs-lookup"><span data-stu-id="61890-119">If the cost will be capitalized, then a write-up adjustment transaction must be posted separately.</span></span>  
11. <span data-ttu-id="61890-120">[一般] タブをクリックします。</span><span class="sxs-lookup"><span data-stu-id="61890-120">Click the General tab.</span></span>
    * <span data-ttu-id="61890-121">追加物によって固定資産の耐用年数が増加する場合は、耐用年数の増加を設定します。</span><span class="sxs-lookup"><span data-stu-id="61890-121">Set Increases service life if the addition increases the service life of the asset.</span></span>  
    * <span data-ttu-id="61890-122">これは情報提供のみを目的としたフィールドです。</span><span class="sxs-lookup"><span data-stu-id="61890-122">This field is informational only.</span></span> <span data-ttu-id="61890-123">耐用年数を増加させるには、資産の価値モデルまたは減価償却簿の耐用年数を変更します。</span><span class="sxs-lookup"><span data-stu-id="61890-123">To increase the service life, modify the Service life on the Value models and/or Depreciation books for the asset.</span></span>  

