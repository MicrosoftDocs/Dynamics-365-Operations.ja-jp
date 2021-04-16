---
title: 新しい倉庫レイアウトの作成
description: このトピックでは、倉庫での場所に関する情報を設定する方法を説明します。
author: perlynne
ms.date: 07/29/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: InventParameters, DefaultDashboard, InventLocation, WMSLocationWizard
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 3a329df85c339c90e4bdc620c8a63837ebc19a7c
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/01/2021
ms.locfileid: "5833980"
---
# <a name="create-a-new-warehouse-layout"></a><span data-ttu-id="76833-103">新しい倉庫レイアウトの作成</span><span class="sxs-lookup"><span data-stu-id="76833-103">Create a new warehouse layout</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="76833-104">このトピックでは、倉庫での場所に関する情報を設定する方法を説明します。</span><span class="sxs-lookup"><span data-stu-id="76833-104">This topic describes how to set up information about the locations in a warehouse.</span></span> <span data-ttu-id="76833-105">これは、[在庫管理] モジュールで「基本倉庫」を使用して作成された倉庫のみが対象で、[倉庫管理] モジュールで作成された倉庫には適用されません。</span><span class="sxs-lookup"><span data-stu-id="76833-105">This applies only to warehouses created using "basic warehousing" in the Inventory management module, not to warehouses created in the Warehouse management module.</span></span> <span data-ttu-id="76833-106">デモ データの会社 USMF のこの手順を使うか、または独自のデータを使うことができます。</span><span class="sxs-lookup"><span data-stu-id="76833-106">You can use this procedure in demo data company USMF, or on your own data.</span></span>


## <a name="set-the-default-location-capacity"></a><span data-ttu-id="76833-107">既定の場所の能力を設定します</span><span class="sxs-lookup"><span data-stu-id="76833-107">Set the default location capacity</span></span>
1. <span data-ttu-id="76833-108">ナビゲーション ウィンドウで、**モジュール > 在庫管理 > 設定 > 在庫および倉庫管理パラメーター** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="76833-108">In the navigation pane, go to **Modules > Inventory management > Setup > Inventory and warehouse management parameters**.</span></span>
2. <span data-ttu-id="76833-109">**場所** タブを選択します。</span><span class="sxs-lookup"><span data-stu-id="76833-109">Select the **Locations** tab.</span></span>
3. <span data-ttu-id="76833-110">**標準の幅** フィールドに数値を入力します。</span><span class="sxs-lookup"><span data-stu-id="76833-110">In the **Standard width** field, enter a number.</span></span>
4. <span data-ttu-id="76833-111">**標準の奥行き** フィールドに数値を入力します。</span><span class="sxs-lookup"><span data-stu-id="76833-111">In the **Standard depth** field, enter a number.</span></span>
5. <span data-ttu-id="76833-112">**標準の高さ** フィールドに数値を入力します。</span><span class="sxs-lookup"><span data-stu-id="76833-112">In the **Standard height** field, enter a number.</span></span>
6. <span data-ttu-id="76833-113">**保存** を選択します。</span><span class="sxs-lookup"><span data-stu-id="76833-113">Select **Save**.</span></span>
7. <span data-ttu-id="76833-114">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="76833-114">Close the page.</span></span>

## <a name="define-the-location-name-format"></a><span data-ttu-id="76833-115">場所の名前の形式を定義します。</span><span class="sxs-lookup"><span data-stu-id="76833-115">Define the location name format</span></span>
1. <span data-ttu-id="76833-116">ナビゲーション ウィンドウで、**モジュール > 在庫管理 > 設定 > 在庫詳細 > 倉庫** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="76833-116">In the navigation pane, go to **Modules > Inventory management > Setup > Inventory breakdown > Warehouses**.</span></span>
2. <span data-ttu-id="76833-117">**新規** を選択します。</span><span class="sxs-lookup"><span data-stu-id="76833-117">Select **New**.</span></span>
3. <span data-ttu-id="76833-118">**倉庫** フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="76833-118">In the **Warehouse** field, type a value.</span></span>
4. <span data-ttu-id="76833-119">**名前** フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="76833-119">In the **Name** field, type a value.</span></span>
5. <span data-ttu-id="76833-120">**サイト** フィールドで、ルックアップの目的のレコードを選択します。</span><span class="sxs-lookup"><span data-stu-id="76833-120">In the **Site** field, select the desired record in the lookup.</span></span>
6. <span data-ttu-id="76833-121">**場所の名前** セクションの展開を切り替えます。</span><span class="sxs-lookup"><span data-stu-id="76833-121">Toggle the expansion of the **Location names** section.</span></span> <span data-ttu-id="76833-122">このセクションのオプションは、場所の名前の既定の形式を定義します。</span><span class="sxs-lookup"><span data-stu-id="76833-122">The options in this section define the default format for location names.</span></span> <span data-ttu-id="76833-123">上記の例では、通路番号、ラック番号、棚番号が含まれます。</span><span class="sxs-lookup"><span data-stu-id="76833-123">In our example, we'll include the aisle number, rack number and shelf number.</span></span>  
7. <span data-ttu-id="76833-124">**通路を含める** オプションを **はい** に設定します。</span><span class="sxs-lookup"><span data-stu-id="76833-124">Set the **Include aisle** option to **Yes**.</span></span>
8. <span data-ttu-id="76833-125">**ラックを含める** オプションを **はい** に設定します。</span><span class="sxs-lookup"><span data-stu-id="76833-125">Set the **Include rack** option to **Yes**.</span></span> 
9. <span data-ttu-id="76833-126">ラックの **形式** フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="76833-126">In the **Format** field, for the rack, type a value.</span></span>
10. <span data-ttu-id="76833-127">**棚を含める** オプションを **はい** に設定します。</span><span class="sxs-lookup"><span data-stu-id="76833-127">Set the **Include shelf** option to **Yes**.</span></span>
11. <span data-ttu-id="76833-128">棚の **形式** フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="76833-128">In the **Format** field, for the shelf, type a value.</span></span>

## <a name="define-warehouse-locations"></a><span data-ttu-id="76833-129">倉庫の場所の定義</span><span class="sxs-lookup"><span data-stu-id="76833-129">Define warehouse locations</span></span>
1. <span data-ttu-id="76833-130">アクション ウィンドウで、**倉庫** を選択します。</span><span class="sxs-lookup"><span data-stu-id="76833-130">On the Action Pane, select **Warehouse**.</span></span>
2. <span data-ttu-id="76833-131">**場所ウィザード** を選択します。</span><span class="sxs-lookup"><span data-stu-id="76833-131">Select **Location Wizard**.</span></span>
3. <span data-ttu-id="76833-132">**次へ** を選択します。</span><span class="sxs-lookup"><span data-stu-id="76833-132">Select **Next**.</span></span>
4. <span data-ttu-id="76833-133">**出荷ドック** オプションを選択解除します。</span><span class="sxs-lookup"><span data-stu-id="76833-133">De-select the **Outbound docks** option</span></span>
5. <span data-ttu-id="76833-134">**バルク場所** オプションを選択解除します。</span><span class="sxs-lookup"><span data-stu-id="76833-134">De-select the **Bulk locations** option</span></span>
6. <span data-ttu-id="76833-135">**完了** を選択するオプションが表示されるまで、**次へ** を選択します。</span><span class="sxs-lookup"><span data-stu-id="76833-135">Select **Next** until you come to the option to select **Finish**.</span></span>
7. <span data-ttu-id="76833-136">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="76833-136">Close the page.</span></span>
8. <span data-ttu-id="76833-137">ページを更新します。</span><span class="sxs-lookup"><span data-stu-id="76833-137">Refresh the page.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]