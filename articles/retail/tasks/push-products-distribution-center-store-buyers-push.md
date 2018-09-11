--- 
title: "集中的購買を使用した物流センターから店舗への製品の配送"
description: "この手順は、一つの場所から、一つまたは複数の店舗に製品を配分する集中的購買を作成および処理する手順を説明します。"
author: rubencdelgado
manager: AnnBe
ms.date: 8/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: RetailBuyersPush, InventLocationIdLookup, InventItemIdLookupSimple, RetailReplenishmentTreeLookup
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Retail
ms.author: rubendel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 32d71167fdad65cb1dec37671999a497759ca484
ms.openlocfilehash: 3337241f8b0e3b30a3382a402257844e7438477a
ms.contentlocale: ja-jp
ms.lasthandoff: 09/11/2018

---
# <a name="push-products-from-distribution-center-to-store-using-buyers-push"></a><span data-ttu-id="359e2-103">集中的購買を使用した物流センターから店舗への製品の配送</span><span class="sxs-lookup"><span data-stu-id="359e2-103">Push products from distribution center to store using buyer's push</span></span>

[!include[task guide banner](../includes/task-guide-banner.md)]

<span data-ttu-id="359e2-104">この手順は、一つの場所から、一つまたは複数の店舗に製品を配分する集中的購買を作成および処理する手順を説明します。</span><span class="sxs-lookup"><span data-stu-id="359e2-104">This procedure walks through the steps to create and process a Buyer´s push to distribute products from one location to one or many stores.</span></span> <span data-ttu-id="359e2-105">ユーザーは、複数のコンフィギュレーションを定義したり、製品の配分方法を提案するシステムを使用できます。あるいは製品をどこに、どの程度各店舗に配分するか手動で入力することもできます。</span><span class="sxs-lookup"><span data-stu-id="359e2-105">The user can define multiple configurations and have the system suggest how to distribute the products, or manually enter where the products are distributed to and how much gets distributed to each store.</span></span> <span data-ttu-id="359e2-106">この手順には、補充ルール、組織階層と店舗の重量などの集中的購買に使用できるデータの設定は含まれません。</span><span class="sxs-lookup"><span data-stu-id="359e2-106">This procedure doesn't include setup of data that can be used in the Buyer´s push, such as replenishment rules, organizational hierarchies, and store weights.</span></span> <span data-ttu-id="359e2-107">この手順では、USMF というデモ会社を使用します。</span><span class="sxs-lookup"><span data-stu-id="359e2-107">This procedure uses the USRT demo company.</span></span>

1. <span data-ttu-id="359e2-108">[集中的購買] に移動します。</span><span class="sxs-lookup"><span data-stu-id="359e2-108">Go to Buyer's push.</span></span>
2. <span data-ttu-id="359e2-109">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="359e2-109">Click New.</span></span>
3. <span data-ttu-id="359e2-110">[説明] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="359e2-110">In the Description field, type a value.</span></span>
4. <span data-ttu-id="359e2-111">[サイト] フィールドで値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="359e2-111">In the Site field, enter or select a value.</span></span>
5. <span data-ttu-id="359e2-112">[倉庫] フィールドで、手持在庫数量の製品のある倉庫を入力、または選択します。</span><span class="sxs-lookup"><span data-stu-id="359e2-112">In the Warehouse field, enter or select a warehouse that has products with on-hand quantities.</span></span>
6. <span data-ttu-id="359e2-113">[追加] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="359e2-113">Click Add.</span></span>
7. <span data-ttu-id="359e2-114">一覧で、選択された行をマークします。</span><span class="sxs-lookup"><span data-stu-id="359e2-114">In the list, mark the selected row.</span></span>
8. <span data-ttu-id="359e2-115">[品目番号] フィールドで、製品を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="359e2-115">In the Item number field, enter or select a product.</span></span>
9. <span data-ttu-id="359e2-116">[追加] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="359e2-116">Click Add.</span></span>
10. <span data-ttu-id="359e2-117">一覧で、選択された行をマークします。</span><span class="sxs-lookup"><span data-stu-id="359e2-117">In the list, mark the selected row.</span></span>
11. <span data-ttu-id="359e2-118">[品目番号] フィールドで、バリアント製品を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="359e2-118">In the Item number field, enter or select a variant product.</span></span>
    * <span data-ttu-id="359e2-119">バリアント製品を入力すると、明細行がバリアントごとに作成されます。</span><span class="sxs-lookup"><span data-stu-id="359e2-119">When entering a variant product, lines will be created for each variant.</span></span>  
12. <span data-ttu-id="359e2-120">一覧で行をマーキングします。</span><span class="sxs-lookup"><span data-stu-id="359e2-120">In the list, mark a row.</span></span>
13. <span data-ttu-id="359e2-121">[プッシュ数量] フィールドに、配布する選択された製品の数量を入力します。</span><span class="sxs-lookup"><span data-stu-id="359e2-121">In the Pushed quantity field, type how many of the selected product you want to distribute.</span></span>
14. <span data-ttu-id="359e2-122">[プッシュする追加数量] フィールドで、配送先の有効数量がある製品の数量を入力します。</span><span class="sxs-lookup"><span data-stu-id="359e2-122">In the Additional quantity to push field, enter the quantity of the products that have available quantity to distribute.</span></span>
15. <span data-ttu-id="359e2-123">[配送] フィールドで、[場所の重量] を入力します。</span><span class="sxs-lookup"><span data-stu-id="359e2-123">In the Distribution field, enter 'Location weight'.</span></span>
    * <span data-ttu-id="359e2-124">配送のために、他のルールを使用する他のタイプを選択できます。</span><span class="sxs-lookup"><span data-stu-id="359e2-124">You can select the other types to use other rules for the distribution.</span></span>  
16. <span data-ttu-id="359e2-125">[補充階層] フィールドで値を選択します。</span><span class="sxs-lookup"><span data-stu-id="359e2-125">In the Replenishment hierarchy field, select a value.</span></span>
17. <span data-ttu-id="359e2-126">[品揃えの考慮] フィールドで、[はい] を選択します。</span><span class="sxs-lookup"><span data-stu-id="359e2-126">Select Yes in the Respect assortments field.</span></span>
18. <span data-ttu-id="359e2-127">[数量の計算] クリックし、[倉庫] セクションの行に追加される数量を確認します。</span><span class="sxs-lookup"><span data-stu-id="359e2-127">Click Calculate quantities and review the quantities that are added to the rows in the Warehouse section.</span></span>
19. <span data-ttu-id="359e2-128">[注文の作成] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="359e2-128">Click Create order.</span></span>
20. <span data-ttu-id="359e2-129">[はい] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="359e2-129">Click Yes.</span></span>


