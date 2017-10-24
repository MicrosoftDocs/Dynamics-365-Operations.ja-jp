--- 
title: "受入倉庫から店舗までのクロスドッキング製品"
description: "この手順は、発注書の入荷場所から、一つまたは複数の店舗に製品を配分するクロスドッキングを作成および処理する手順を説明します。"
author: BibiSp
manager: AnnBe
ms.date: 02/17/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bis
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: bis
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: daa42bb83d6b988e8fd18db6ad8386c67fd3e6e5
ms.contentlocale: ja-jp
ms.lasthandoff: 09/29/2017

---
# <a name="cross-dock-products-from-receiving-warehouse-to-stores"></a><span data-ttu-id="67f17-103">受入倉庫から店舗までのクロスドッキング製品</span><span class="sxs-lookup"><span data-stu-id="67f17-103">Cross-dock products from receiving warehouse to stores</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="67f17-104">この手順は、発注書の入荷場所から、一つまたは複数の店舗に製品を配分するクロスドッキングを作成および処理する手順を説明します。</span><span class="sxs-lookup"><span data-stu-id="67f17-104">This procedure walks through the steps to create and process a Cross-dock to distribute products from the receiving location of a purchase order to one or many stores.</span></span> <span data-ttu-id="67f17-105">ユーザーは、複数のコンフィギュレーションを定義したり、製品の配分方法を提案するシステムを使用できます。あるいは製品をどこに、どの程度各店舗に配分するか手動で入力することもできます。</span><span class="sxs-lookup"><span data-stu-id="67f17-105">The user can define multiple configurations and have the system suggest how to distribute the products, or manually enter where the products are distributed to and how much gets distributed to each store.</span></span> <span data-ttu-id="67f17-106">手順には、補充ルール、組織階層と店舗の重量などのクロスドッキングに使用できるデータの設定は含まれません。</span><span class="sxs-lookup"><span data-stu-id="67f17-106">The procedure doesn't include setup of data that can be used in the Cross-dock, such as replenishment rules, organizational hierarchies, and store weights.</span></span> <span data-ttu-id="67f17-107">この手順では、USRT というデモ会社を使用します。</span><span class="sxs-lookup"><span data-stu-id="67f17-107">The procedure uses the USRT demo company.</span></span>

1. <span data-ttu-id="67f17-108">[すべての発注書] に移動します。</span><span class="sxs-lookup"><span data-stu-id="67f17-108">Go to All purchase orders.</span></span>
2. <span data-ttu-id="67f17-109">一覧から購買注文ポリシーを選択し、リンクをクリックして注文を開きます。</span><span class="sxs-lookup"><span data-stu-id="67f17-109">Select a purchase order in the list and click the link to open the order.</span></span>
3. <span data-ttu-id="67f17-110">アクション ウィンドウで、[小売] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="67f17-110">On the Action Pane, click Retail.</span></span>
4. <span data-ttu-id="67f17-111">[クロスドッキング] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="67f17-111">Click Cross docking.</span></span>
5. <span data-ttu-id="67f17-112">[編集] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="67f17-112">Click Edit.</span></span>
    * <span data-ttu-id="67f17-113">[明細] セクションの品目をフィルタ処理するためにカテゴリを使用できます。</span><span class="sxs-lookup"><span data-stu-id="67f17-113">The category can be used to filter the items in the Lines section.</span></span>  
6. <span data-ttu-id="67f17-114">一覧で、目的のレコードを見つけ、選択します。</span><span class="sxs-lookup"><span data-stu-id="67f17-114">In the list, find and select the desired record.</span></span>
7. <span data-ttu-id="67f17-115">[クロスドッキング数量] フィールドで、配分する必要がある選択した製品の購買数量の数量を指定するための値を入力します。</span><span class="sxs-lookup"><span data-stu-id="67f17-115">In the Cross docking quantity field, type a value to specify how much of the quantity being purchased of the selected product should be distributed.</span></span>
8. <span data-ttu-id="67f17-116">[追加のクロスドッキング数量] フィールドに購入できる製品に対して配分する数量を指定するための値を入力します。</span><span class="sxs-lookup"><span data-stu-id="67f17-116">In the Additional cross docking quantity field, enter a value to specify the quantities to distribute for the available products being purchased</span></span>
9. <span data-ttu-id="67f17-117">[配送] フィールドで、[場所の重量] を入力します。</span><span class="sxs-lookup"><span data-stu-id="67f17-117">In the Distribution field, enter 'Location weight'.</span></span>
    * <span data-ttu-id="67f17-118">配送のために、さまざまなルールを使用する他のタイプを選択できます。</span><span class="sxs-lookup"><span data-stu-id="67f17-118">You can select the other types to use different rules for the distribution.</span></span>  
10. <span data-ttu-id="67f17-119">[補充階層] フィールドで値を選択します。</span><span class="sxs-lookup"><span data-stu-id="67f17-119">In the Replenishment hierarchy field, select a value.</span></span>
11. <span data-ttu-id="67f17-120">[品揃えの考慮] フィールドで、[はい] を選択します。</span><span class="sxs-lookup"><span data-stu-id="67f17-120">Select Yes in the Respect assortments field.</span></span>
12. <span data-ttu-id="67f17-121">[数量の計算] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="67f17-121">Click Calculate quantities.</span></span>
13. <span data-ttu-id="67f17-122">[注文の作成] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="67f17-122">Click Create order.</span></span>
14. <span data-ttu-id="67f17-123">[はい] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="67f17-123">Click Yes.</span></span>
15. <span data-ttu-id="67f17-124">一覧で、製品を受け入れる倉庫を見つけ、選択します。</span><span class="sxs-lookup"><span data-stu-id="67f17-124">In the list, find and select a warehouse that received products</span></span>
16. <span data-ttu-id="67f17-125">選択した倉庫に対して作成された注文を表示するには、[注文] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="67f17-125">Click Order to view the orders that got created for the selected warehouse</span></span>


