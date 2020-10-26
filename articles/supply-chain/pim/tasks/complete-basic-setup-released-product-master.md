---
title: リリース済み製品マスターの基本設定の完了
description: このトピックは、製品マスターを BOM バージョンで使用する前に必要な最小限の設定の完了方法を示します。
author: ShylaThompson
manager: tfehr
ms.date: 07/08/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EcoResProductDetailsExtended, InventTableInventoryDimensionGroups, InventItemOrderSetup
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 8ac4ceeb3e21ab089eb16565bb6e38c7eb44be80
ms.sourcegitcommit: 708ca25687a4e48271cdcd6d2d22d99fb94cf140
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/10/2020
ms.locfileid: "3986410"
---
# <a name="complete-basic-setup-of-a-released-product-master"></a><span data-ttu-id="b6230-103">リリース済み製品マスターの基本設定の完了</span><span class="sxs-lookup"><span data-stu-id="b6230-103">Complete basic setup of a released product master</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="b6230-104">このトピックは、製品マスターを BOM バージョンで使用する前に必要な最小限の設定の完了方法を示します。</span><span class="sxs-lookup"><span data-stu-id="b6230-104">This topic shows how to complete the minimum setup that is required before the product master can be used in BOM versions.</span></span>

<span data-ttu-id="b6230-105">これは、分析コードベースのコンフィギュレーションでの組み合わせの作成方法を説明する 8 つの手順の 3 番目です。</span><span class="sxs-lookup"><span data-stu-id="b6230-105">This is the third procedure out of eight which explains how to build combinations for dimension-based configuration.</span></span> <span data-ttu-id="b6230-106">この手順の作成に使用するデモ データの会社は USMF です。</span><span class="sxs-lookup"><span data-stu-id="b6230-106">The demo data company used to create this procedure is USMF.</span></span>

1. <span data-ttu-id="b6230-107">**ナビゲーション ウィンドウ > モジュール > 製品情報管理 > 製品 > リリース済製品**の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="b6230-107">Go to **Navigation pane > Modules > Product information management > Products > Released products**.</span></span>
2. <span data-ttu-id="b6230-108">一覧で、目的のレコードを見つけ、選択します。</span><span class="sxs-lookup"><span data-stu-id="b6230-108">In the list, find and select the desired record.</span></span> <span data-ttu-id="b6230-109">2 番目の手順でリリースする製品マスターを選択します。</span><span class="sxs-lookup"><span data-stu-id="b6230-109">Select the product master that you have released in the second procedure.</span></span> <span data-ttu-id="b6230-110">この製品マスターは、分析コード ベースのコンフィギュレーション テクノロジで作成されます。</span><span class="sxs-lookup"><span data-stu-id="b6230-110">This product master is created with the dimension-based configuration technology.</span></span>  
3. <span data-ttu-id="b6230-111">アクション ウィンドウで、**製品**を選択します。</span><span class="sxs-lookup"><span data-stu-id="b6230-111">On the Action Pane, select **Product**.</span></span>
4. <span data-ttu-id="b6230-112">**分析コード グループ**を選択して、ドロップ ダイアログを開きます。</span><span class="sxs-lookup"><span data-stu-id="b6230-112">Select **Dimension groups** to open the drop dialog.</span></span>
5. <span data-ttu-id="b6230-113">**保管分析コード グループ** フィールドで、ドロップダウン ボタンを選択し、ルックアップを開きます。</span><span class="sxs-lookup"><span data-stu-id="b6230-113">In the **Storage dimension group** field, select the drop-down button to open the lookup.</span></span>
6. <span data-ttu-id="b6230-114">一覧で、目的のレコードを見つけ、選択します。</span><span class="sxs-lookup"><span data-stu-id="b6230-114">In the list, find and select the desired record.</span></span> <span data-ttu-id="b6230-115">保管分析コード グループにより、製品トランザクションに使用される保管分析コードが決まります。</span><span class="sxs-lookup"><span data-stu-id="b6230-115">The storage dimension group determines which storage dimensions are used for product transaction.</span></span> <span data-ttu-id="b6230-116">この手順では**サイト**を選択します。</span><span class="sxs-lookup"><span data-stu-id="b6230-116">Select **Site** for this procedure.</span></span>  
7. <span data-ttu-id="b6230-117">**追跡用分析コード グループ** フィールドで、ドロップダウン ボタンを選択し、ルックアップを開きます。</span><span class="sxs-lookup"><span data-stu-id="b6230-117">In the **Tracking dimension group** field, select the drop-down button to open the lookup.</span></span>
8. <span data-ttu-id="b6230-118">一覧で、目的のレコードを見つけ、選択します。</span><span class="sxs-lookup"><span data-stu-id="b6230-118">In the list, find and select the desired record.</span></span> <span data-ttu-id="b6230-119">追跡用分析コード グループにより、製品トランザクションに使用される追跡用分析コードが決まります。</span><span class="sxs-lookup"><span data-stu-id="b6230-119">The tracking dimension group determines which tracking dimensions are used for product transaction.</span></span> <span data-ttu-id="b6230-120">この手順では**なし**を選択します。</span><span class="sxs-lookup"><span data-stu-id="b6230-120">Select **None** for this procedure.</span></span>  
9. <span data-ttu-id="b6230-121">**OK**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="b6230-121">Click **OK**.</span></span>
10. <span data-ttu-id="b6230-122">**編集** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="b6230-122">Click **Edit**.</span></span>
11. <span data-ttu-id="b6230-123">**品目モデル グループ** フィールドで、ドロップダウン ボタンを選択し、ルックアップを開きます。</span><span class="sxs-lookup"><span data-stu-id="b6230-123">In the **Item model group** field, select the drop-down button to open the lookup.</span></span>
12. <span data-ttu-id="b6230-124">一覧で、目的のレコードを見つけ、選択します。</span><span class="sxs-lookup"><span data-stu-id="b6230-124">In the list, find and select the desired record.</span></span> <span data-ttu-id="b6230-125">品目モデル グループには、品目の入庫および出庫時における品目の管理方法および処理方法を決定する設定が含まれています。</span><span class="sxs-lookup"><span data-stu-id="b6230-125">Item model groups contain settings that determine how items are controlled and handled on item receipts and issues.</span></span> <span data-ttu-id="b6230-126">在庫モデル グループは、品目消費の計算方法も決定します。</span><span class="sxs-lookup"><span data-stu-id="b6230-126">They also determine how item consumption is calculated.</span></span> <span data-ttu-id="b6230-127">この手順では **FIFO** を選択します。</span><span class="sxs-lookup"><span data-stu-id="b6230-127">Select **FIFO** for this procedure.</span></span>  
13. <span data-ttu-id="b6230-128">**原価の管理**セクションを展開します。</span><span class="sxs-lookup"><span data-stu-id="b6230-128">Expand the **Manage costs** section.</span></span>
14. <span data-ttu-id="b6230-129">**品目グループ** フィールドで、ドロップダウン ボタンを選択し、ルックアップを開きます。</span><span class="sxs-lookup"><span data-stu-id="b6230-129">In the **Item group** field, select the drop-down button to open the lookup.</span></span>
15. <span data-ttu-id="b6230-130">一覧で、目的のレコードを見つけ、選択します。</span><span class="sxs-lookup"><span data-stu-id="b6230-130">In the list, find and select the desired record.</span></span> <span data-ttu-id="b6230-131">品目グループは、在庫品目の分類による在庫管理に使用されます。</span><span class="sxs-lookup"><span data-stu-id="b6230-131">Item groups are used to manage inventory by dividing inventory items into groups.</span></span> <span data-ttu-id="b6230-132">この手順では **CarAudio** を選択します。</span><span class="sxs-lookup"><span data-stu-id="b6230-132">Select **CarAudio** for this procedure.</span></span>  
16. <span data-ttu-id="b6230-133">アクション ウィンドウで、**計画**を選択します。</span><span class="sxs-lookup"><span data-stu-id="b6230-133">On the Action Pane, select **Plan**.</span></span>
17. <span data-ttu-id="b6230-134">**既定の注文設定**を選択します。</span><span class="sxs-lookup"><span data-stu-id="b6230-134">Select **Default order settings**.</span></span>
18. <span data-ttu-id="b6230-135">**既定の注文タイプ フィールド**で、オプションを選択します。</span><span class="sxs-lookup"><span data-stu-id="b6230-135">In the **Default order type field**, select an option.</span></span> <span data-ttu-id="b6230-136">**生産**を選択して、この製品マスターの既定の供給オプションが製品の生産であることを指定します。</span><span class="sxs-lookup"><span data-stu-id="b6230-136">Select **Production** to specify that the default supply option for this product master is to produce it.</span></span>  
19. <span data-ttu-id="b6230-137">**保存** を選択します。</span><span class="sxs-lookup"><span data-stu-id="b6230-137">Select **Save**.</span></span>
20. <span data-ttu-id="b6230-138">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="b6230-138">Close the page.</span></span>
21. <span data-ttu-id="b6230-139">**リリース製品の詳細**フォームを閉じます。</span><span class="sxs-lookup"><span data-stu-id="b6230-139">Close the **Released product details** form.</span></span>

