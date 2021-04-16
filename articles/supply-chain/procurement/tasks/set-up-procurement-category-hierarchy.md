---
title: 調達カテゴリ階層の設定
description: この手順では、調達カテゴリ階層に新しいノードを作成する方法、および調達プロセスに使用する調達カテゴリをコンフィギュレーションする方法を示します。
author: kamaybac
ms.date: 06/21/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: dabourq
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 206dd5dc8f332268fe7665d84b005b5a7bfd1f9a
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/01/2021
ms.locfileid: "5837708"
---
# <a name="set-up-a-procurement-category-hierarchy"></a><span data-ttu-id="6815d-103">調達カテゴリ階層の設定</span><span class="sxs-lookup"><span data-stu-id="6815d-103">Set up a procurement category hierarchy</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="6815d-104">この手順では、調達カテゴリ階層に新しいノードを作成する方法、および調達プロセスに使用する調達カテゴリをコンフィギュレーションする方法を示します。</span><span class="sxs-lookup"><span data-stu-id="6815d-104">This procedure shows you how to create new nodes in a procurement category hierarchy and how to configure a procurement category to be used in a procurement process.</span></span> <span data-ttu-id="6815d-105">通常、これらのタスクを実施するのは、購買マネージャーです。</span><span class="sxs-lookup"><span data-stu-id="6815d-105">These tasks would typically be carried out by a Purchasing manager.</span></span> <span data-ttu-id="6815d-106">この手順を開始する前に、調達タイプのカテゴリ階層が必要です。</span><span class="sxs-lookup"><span data-stu-id="6815d-106">Before you can start this procedure, there must be a category hierarchy of type Procurement.</span></span> <span data-ttu-id="6815d-107">デモ データの会社を使用すると、USMF 会社でこの手順を実行できます。</span><span class="sxs-lookup"><span data-stu-id="6815d-107">If you're using a demo data company, you can run this procedure in the USMF company.</span></span>


## <a name="add-a-new-procurement-category"></a><span data-ttu-id="6815d-108">新しい調達カテゴリを追加します。</span><span class="sxs-lookup"><span data-stu-id="6815d-108">Add a new procurement category</span></span>
1. <span data-ttu-id="6815d-109">**ナビゲーション ウィンドウ > モジュール > 調達 > 委託販売 > 調達カテゴリ** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="6815d-109">Go to **Navigation pane > Modules > Procurement and sourcing > Consignment > Procurement categories**.</span></span>
2. <span data-ttu-id="6815d-110">アクション ウィンドウで、**カテゴリ階層の編集** を選択します。</span><span class="sxs-lookup"><span data-stu-id="6815d-110">On the Action Pane, select **Edit category hierarchy**.</span></span> <span data-ttu-id="6815d-111">現在の調達カテゴリ階層が、ページの左側に表示されます。</span><span class="sxs-lookup"><span data-stu-id="6815d-111">The current procurement category hierarchy is displayed in the left side of the page.</span></span> <span data-ttu-id="6815d-112">階層を修正しようとしています。</span><span class="sxs-lookup"><span data-stu-id="6815d-112">You  are about to modify the hierarchy.</span></span>  
3. <span data-ttu-id="6815d-113">アクション ウィンドウで、**新規カテゴリ ノード** を選択します。</span><span class="sxs-lookup"><span data-stu-id="6815d-113">On the Action Pane, select **New category node**.</span></span> <span data-ttu-id="6815d-114">システムは、既定によりトップ ノードを選択します。</span><span class="sxs-lookup"><span data-stu-id="6815d-114">The system selects the top node by default.</span></span> <span data-ttu-id="6815d-115">タスク ガイドの手順を実行している場合、[ロック解除] ボタンをクリックして、別の親ノードを選択し、新しいノードを挿入することができます。</span><span class="sxs-lookup"><span data-stu-id="6815d-115">If you are running this procedure as a task guide, you can click the Unlock button and select another parent node to insert your new node into.</span></span> <span data-ttu-id="6815d-116">その場合、タスクのガイドを再度ロックし、[新しいカテゴリ ノード] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="6815d-116">Once that is done, lock the task guide again and then click New category node.</span></span>  
4. <span data-ttu-id="6815d-117">**名前** フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="6815d-117">In the **Name** field, type a value.</span></span>
5. <span data-ttu-id="6815d-118">**説明** フィールドで、値を入力します。</span><span class="sxs-lookup"><span data-stu-id="6815d-118">In the **Description** field, type a value.</span></span>
6. <span data-ttu-id="6815d-119">**フレンドリ名** フィールドで、値を入力します。</span><span class="sxs-lookup"><span data-stu-id="6815d-119">In the **Friendly name** field, type a value.</span></span> <span data-ttu-id="6815d-120">フレンドリ名はオプションです。</span><span class="sxs-lookup"><span data-stu-id="6815d-120">The friendly name is optional.</span></span> <span data-ttu-id="6815d-121">これは、カテゴリの名前と一緒に、カテゴリのルックアップに表示されます。</span><span class="sxs-lookup"><span data-stu-id="6815d-121">It will be displayed in category lookups together with the category name.</span></span>  
7. <span data-ttu-id="6815d-122">**保存** を選択します。</span><span class="sxs-lookup"><span data-stu-id="6815d-122">Select **Save**.</span></span>

## <a name="add-products-to-your-new-procurement-category"></a><span data-ttu-id="6815d-123">新しい調達カテゴリへの製品の追加</span><span class="sxs-lookup"><span data-stu-id="6815d-123">Add products to your new procurement category</span></span>
1. <span data-ttu-id="6815d-124">**調達 > 委託販売 > 調達カテゴリ** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="6815d-124">Go to **Procurement and sourcing > Consignment > Procurement categories**.</span></span> <span data-ttu-id="6815d-125">追加したノードを選択します。</span><span class="sxs-lookup"><span data-stu-id="6815d-125">Select the node you just added.</span></span> <span data-ttu-id="6815d-126">タスク ガイドとしてこの手順を実行している場合は、ノードを選択するために、タスク ガイドのロック解除が必要な場合があります。</span><span class="sxs-lookup"><span data-stu-id="6815d-126">If you're running this procedure as a task guide you might need to unlock the task guide to select the node.</span></span>  
2. <span data-ttu-id="6815d-127">**製品** セクションの展開を切り替えます。</span><span class="sxs-lookup"><span data-stu-id="6815d-127">Toggle the expansion of the **Products** section.</span></span>
3. <span data-ttu-id="6815d-128">調達カテゴリに製品を関連付けるには、**追加** を選択します。</span><span class="sxs-lookup"><span data-stu-id="6815d-128">Select **Add** to associate products with the procurement category.</span></span>
4. <span data-ttu-id="6815d-129">調達カテゴリに追加する製品を選択します。</span><span class="sxs-lookup"><span data-stu-id="6815d-129">Select the products you want to add to the procurement category.</span></span>
5. <span data-ttu-id="6815d-130">矢印を選択して **選択済** テーブルに製品を追加します。</span><span class="sxs-lookup"><span data-stu-id="6815d-130">Select the arrow to add the products to the **Selected** table.</span></span>
6. <span data-ttu-id="6815d-131">**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="6815d-131">Select **OK**.</span></span>


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]