---
title: "新しい倉庫レイアウトの作成"
description: "この手順は、倉庫での場所に関する情報を設定する方法を示します。"
author: perlynne
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: YuyuScheller
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 0e7f66cccd76e5326fce75d1a13aff294c16fb9b
ms.openlocfilehash: 253440d81edd6f71b52ae349398e3c6a895bf05c
ms.contentlocale: ja-jp
ms.lasthandoff: 09/12/2017

---
# <a name="create-a-new-warehouse-layout"></a><span data-ttu-id="21c05-103">新しい倉庫レイアウトの作成</span><span class="sxs-lookup"><span data-stu-id="21c05-103">Create a new warehouse layout</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="21c05-104">この手順は、倉庫での場所に関する情報を設定する方法を示します。</span><span class="sxs-lookup"><span data-stu-id="21c05-104">This procedure shows you how to set up information about the locations in a warehouse.</span></span> <span data-ttu-id="21c05-105">これは、[在庫管理] モジュールで「基本倉庫」を使用して作成された倉庫のみが対象で、[倉庫管理] モジュールで作成された倉庫には適用されません。</span><span class="sxs-lookup"><span data-stu-id="21c05-105">This applies only to warehouses created using "basic warehousing" in the Inventory management module, not to warehouses created in the Warehouse management module.</span></span> <span data-ttu-id="21c05-106">デモ データの会社 USMF のこの手順を使うか、または独自のデータを使うことができます。</span><span class="sxs-lookup"><span data-stu-id="21c05-106">You can use this procedure in demo data company USMF, or on your own data.</span></span>


## <a name="set-the-default-location-capacity"></a><span data-ttu-id="21c05-107">既定の場所の能力を設定します</span><span class="sxs-lookup"><span data-stu-id="21c05-107">Set the default location capacity</span></span>
1. <span data-ttu-id="21c05-108">[在庫管理] > [設定] > [在庫および倉庫管理パラメーター] を表示します。</span><span class="sxs-lookup"><span data-stu-id="21c05-108">Go to Inventory management > Setup > Inventory and warehouse management parameters.</span></span>
2. <span data-ttu-id="21c05-109">[場所] タブをクリックします。</span><span class="sxs-lookup"><span data-stu-id="21c05-109">Click the Locations tab.</span></span>
3. <span data-ttu-id="21c05-110">[標準の幅] フィールドに数値を入力します。</span><span class="sxs-lookup"><span data-stu-id="21c05-110">In the Standard width field, enter a number.</span></span>
4. <span data-ttu-id="21c05-111">[標準の奥行き] フィールドに数値を入力します。</span><span class="sxs-lookup"><span data-stu-id="21c05-111">In the Standard depth field, enter a number.</span></span>
5. <span data-ttu-id="21c05-112">[標準の高さ] フィールドに数値を入力します。</span><span class="sxs-lookup"><span data-stu-id="21c05-112">In the Standard height field, enter a number.</span></span>
6. <span data-ttu-id="21c05-113">[保存] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="21c05-113">Click Save.</span></span>
7. <span data-ttu-id="21c05-114">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="21c05-114">Close the page.</span></span>

## <a name="define-the-location-name-format"></a><span data-ttu-id="21c05-115">場所の名前の形式を定義します。</span><span class="sxs-lookup"><span data-stu-id="21c05-115">Define the location name format</span></span>
1. <span data-ttu-id="21c05-116">[在庫管理] > [設定] > [在庫詳細] > [倉庫] の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="21c05-116">Go to Inventory management > Setup > Inventory breakdown > Warehouses.</span></span>
2. <span data-ttu-id="21c05-117">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="21c05-117">Click New.</span></span>
3. <span data-ttu-id="21c05-118">[倉庫] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="21c05-118">In the Warehouse field, type a value.</span></span>
4. <span data-ttu-id="21c05-119">[名前] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="21c05-119">In the Name field, type a value.</span></span>
5. <span data-ttu-id="21c05-120">[サイト] フィールドで、ドロップ ダウン ボタンをクリックし、ルックアップを開きます。</span><span class="sxs-lookup"><span data-stu-id="21c05-120">In the Site field, click the drop-down button to open the lookup.</span></span>
6. <span data-ttu-id="21c05-121">一覧で、目的のレコードを見つけ、選択します。</span><span class="sxs-lookup"><span data-stu-id="21c05-121">In the list, find and select the desired record.</span></span>
7. <span data-ttu-id="21c05-122">場所の名前セクションの展開を切り替えます。</span><span class="sxs-lookup"><span data-stu-id="21c05-122">Toggle the expansion of the Location names section.</span></span>
    * <span data-ttu-id="21c05-123">このセクションのオプションは、場所の名前の既定の形式を定義します。</span><span class="sxs-lookup"><span data-stu-id="21c05-123">The options in this section define the default format for location names.</span></span> <span data-ttu-id="21c05-124">上記の例では、通路番号、ラック番号、棚番号が含まれます。</span><span class="sxs-lookup"><span data-stu-id="21c05-124">In our example, we'll include the aisle number, rack number and shelf number.</span></span>  
8. <span data-ttu-id="21c05-125">[通路を含める] オプションをオンに設定します。</span><span class="sxs-lookup"><span data-stu-id="21c05-125">Set the Include aisle option to Yes.</span></span>
9. <span data-ttu-id="21c05-126">[ラックを含める] オプションをオンに設定します。</span><span class="sxs-lookup"><span data-stu-id="21c05-126">Set the Include rack option to Yes.</span></span>
10. <span data-ttu-id="21c05-127">ラックの [形式] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="21c05-127">In the Format field, for the rack, type a value.</span></span>
    * <span data-ttu-id="21c05-128">例: -##</span><span class="sxs-lookup"><span data-stu-id="21c05-128">For example: -##</span></span>  
11. <span data-ttu-id="21c05-129">[棚を含める] オプションをオンに設定します。</span><span class="sxs-lookup"><span data-stu-id="21c05-129">Set the Include shelf option to Yes.</span></span>
12. <span data-ttu-id="21c05-130">棚の [形式] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="21c05-130">In the Format field, for the shelf, type a value.</span></span>
    * <span data-ttu-id="21c05-131">例: -##</span><span class="sxs-lookup"><span data-stu-id="21c05-131">For example: -##</span></span>  

## <a name="define-warehouse-locations"></a><span data-ttu-id="21c05-132">倉庫の場所の定義</span><span class="sxs-lookup"><span data-stu-id="21c05-132">Define warehouse locations</span></span>
1. <span data-ttu-id="21c05-133">アクション ペインで [倉庫] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="21c05-133">On the Action Pane, click Warehouse.</span></span>
2. <span data-ttu-id="21c05-134">[場所ウィザード] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="21c05-134">Click Location Wizard.</span></span>
3. <span data-ttu-id="21c05-135">[次へ] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="21c05-135">Click Next.</span></span>
4. <span data-ttu-id="21c05-136">[出荷ドック] オプションを選択解除します。</span><span class="sxs-lookup"><span data-stu-id="21c05-136">De-select the Outbound docks option</span></span>
5. <span data-ttu-id="21c05-137">[バルク場所] オプションを選択解除します。</span><span class="sxs-lookup"><span data-stu-id="21c05-137">De-select the Bulk locations option</span></span>
6. <span data-ttu-id="21c05-138">[次へ] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="21c05-138">Click Next.</span></span>
7. <span data-ttu-id="21c05-139">[次へ] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="21c05-139">Click Next.</span></span>
8. <span data-ttu-id="21c05-140">[次へ] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="21c05-140">Click Next.</span></span>
9. <span data-ttu-id="21c05-141">[次へ] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="21c05-141">Click Next.</span></span>
10. <span data-ttu-id="21c05-142">[次へ] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="21c05-142">Click Next.</span></span>
11. <span data-ttu-id="21c05-143">[次へ] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="21c05-143">Click Next.</span></span>
12. <span data-ttu-id="21c05-144">[次へ] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="21c05-144">Click Next.</span></span>
    * <span data-ttu-id="21c05-145">このページに表示される物理的な寸法は、この手順の開始時に指定したものであることに注意してください。</span><span class="sxs-lookup"><span data-stu-id="21c05-145">Note that the physical dimensions shown on this page are the ones that you set at the start of this procedure.</span></span>  
13. <span data-ttu-id="21c05-146">[次へ] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="21c05-146">Click Next.</span></span>
14. <span data-ttu-id="21c05-147">[完了] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="21c05-147">Click Finish.</span></span>
15. <span data-ttu-id="21c05-148">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="21c05-148">Close the page.</span></span>
16. <span data-ttu-id="21c05-149">ページを更新します。</span><span class="sxs-lookup"><span data-stu-id="21c05-149">Refresh the page.</span></span>
