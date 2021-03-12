---
title: 作成から開始までのバッチ オーダーのライフサイクル
description: この手順では、バッチ オーダーのライフ サイクルの最初の部分を説明します。
author: ShylaThompson
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProdTableListPage, ProdTableCreate, ProdBOM, PmfProdCoBy, ProdParmCostEstimation, ProdCalcTrans, ProdParmRelease, ProdSchedule, ProdRouteJob, ProdParmStartUp, ProdJournalTransBOM, ProdJournalTransRoute
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: e5fd04587c95ba8a48750f96302a11aeaf82308d
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/15/2021
ms.locfileid: "4981409"
---
# <a name="batch-order-lifecycle-from-create-to-start"></a><span data-ttu-id="78b7f-103">作成から開始までのバッチ オーダーのライフサイクル</span><span class="sxs-lookup"><span data-stu-id="78b7f-103">Batch order lifecycle from create to start</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="78b7f-104">この手順では、バッチ オーダーのライフ サイクルの最初の部分を説明します。</span><span class="sxs-lookup"><span data-stu-id="78b7f-104">This procedure takes you through the first part of the life cycle of a batch order.</span></span>

<span data-ttu-id="78b7f-105">作成、原価見積、超過生産ジョブ スケジュールからバッチ オーダーの実際の開始までです。</span><span class="sxs-lookup"><span data-stu-id="78b7f-105">From creation, cost estimation, and over production job scheduling to the actual start of a batch order.</span></span>



<span data-ttu-id="78b7f-106">この手順の作成に使用するデモ データの会社は USMF です。</span><span class="sxs-lookup"><span data-stu-id="78b7f-106">The demo data company used to create this procedure is USMF.</span></span> 



<span data-ttu-id="78b7f-107">別のデータセットの手順を実行する前提条件は、有効なフォーミュラおよび工順バージョンを含むリリース済製品です。</span><span class="sxs-lookup"><span data-stu-id="78b7f-107">The prerequisites for running the procedure with another dataset are a released product with an active formula and route version.</span></span>


## <a name="create-a-batch-order"></a><span data-ttu-id="78b7f-108">バッチ オーダーの作成</span><span class="sxs-lookup"><span data-stu-id="78b7f-108">Create a batch order</span></span>
1. <span data-ttu-id="78b7f-109">[すべての製造オーダー] に移動します。</span><span class="sxs-lookup"><span data-stu-id="78b7f-109">Go to All production orders.</span></span>
2. <span data-ttu-id="78b7f-110">[新しいバッチ オーダー] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="78b7f-110">Click New batch order.</span></span>
3. <span data-ttu-id="78b7f-111">[品目番号] フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="78b7f-111">In the Item number field, enter or select a value.</span></span>
4. <span data-ttu-id="78b7f-112">[作成] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="78b7f-112">Click Create.</span></span>
5. <span data-ttu-id="78b7f-113">[クイック フィルター] を使用して、値が「b」である [生産] フィールドをフィルター処理します。</span><span class="sxs-lookup"><span data-stu-id="78b7f-113">Use the Quick Filter to filter on the Production field with a value of 'b'.</span></span>

## <a name="view-production-formula-and-expected-co-products"></a><span data-ttu-id="78b7f-114">生産フォーミュラおよび予想される連産品の表示</span><span class="sxs-lookup"><span data-stu-id="78b7f-114">View production formula and expected co-products</span></span>
1. <span data-ttu-id="78b7f-115">アクション ウィンドウで、[製造オーダー] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="78b7f-115">On the Action Pane, click Production order.</span></span>
2. <span data-ttu-id="78b7f-116">[式] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="78b7f-116">Click Formula.</span></span>
3. <span data-ttu-id="78b7f-117">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="78b7f-117">Close the page.</span></span>
4. <span data-ttu-id="78b7f-118">[連産品 (複数)] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="78b7f-118">Click Co-products.</span></span>
5. <span data-ttu-id="78b7f-119">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="78b7f-119">Close the page.</span></span>

## <a name="estimate-the-batch-order"></a><span data-ttu-id="78b7f-120">バッチ オーダーの見積</span><span class="sxs-lookup"><span data-stu-id="78b7f-120">Estimate the batch order</span></span>
1. <span data-ttu-id="78b7f-121">[見積] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="78b7f-121">Click Estimate.</span></span>
2. <span data-ttu-id="78b7f-122">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="78b7f-122">Click OK.</span></span>
3. <span data-ttu-id="78b7f-123">[アクション] ペインで [原価の管理] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="78b7f-123">On the Action Pane, click Manage costs.</span></span>
4. <span data-ttu-id="78b7f-124">[計算の詳細の表示] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="78b7f-124">Click View calculation details.</span></span>
5. <span data-ttu-id="78b7f-125">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="78b7f-125">Close the page.</span></span>

## <a name="release-the-batch-order"></a><span data-ttu-id="78b7f-126">バッチ オーダーのリリース</span><span class="sxs-lookup"><span data-stu-id="78b7f-126">Release the batch order</span></span>
1. <span data-ttu-id="78b7f-127">アクション ウィンドウで、[製造オーダー] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="78b7f-127">On the Action Pane, click Production order.</span></span>
2. <span data-ttu-id="78b7f-128">[リリース] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="78b7f-128">Click Release.</span></span>
3. <span data-ttu-id="78b7f-129">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="78b7f-129">Click OK.</span></span>

## <a name="schedule-production-jobs"></a><span data-ttu-id="78b7f-130">生産ジョブのスケジュール</span><span class="sxs-lookup"><span data-stu-id="78b7f-130">Schedule production jobs</span></span>
1. <span data-ttu-id="78b7f-131">[アクション ペイン] で、[スケジュール] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="78b7f-131">On the Action Pane, click Schedule.</span></span>
2. <span data-ttu-id="78b7f-132">[ジョブのスケジュール設定] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="78b7f-132">Click Schedule jobs.</span></span>
3. <span data-ttu-id="78b7f-133">[有限能力] フィールドで [いいえ] を選択します。</span><span class="sxs-lookup"><span data-stu-id="78b7f-133">Select No in the Finite capacity field.</span></span>
4. <span data-ttu-id="78b7f-134">[有限原材料] フィールドで [いいえ] を選択します。</span><span class="sxs-lookup"><span data-stu-id="78b7f-134">Select No in the Finite material field.</span></span>
5. <span data-ttu-id="78b7f-135">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="78b7f-135">Click OK.</span></span>
6. <span data-ttu-id="78b7f-136">アクション ウィンドウで、[製造オーダー] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="78b7f-136">On the Action Pane, click Production order.</span></span>
7. <span data-ttu-id="78b7f-137">[すべてのジョブ] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="78b7f-137">Click All jobs.</span></span>
8. <span data-ttu-id="78b7f-138">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="78b7f-138">Close the page.</span></span>

## <a name="start-the-batch-order"></a><span data-ttu-id="78b7f-139">バッチ オーダーの開始</span><span class="sxs-lookup"><span data-stu-id="78b7f-139">Start the batch order</span></span>
1. <span data-ttu-id="78b7f-140">[開始] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="78b7f-140">Click Start.</span></span>
2. <span data-ttu-id="78b7f-141">[一般] タブをクリックします。</span><span class="sxs-lookup"><span data-stu-id="78b7f-141">Click the General tab.</span></span>
3. <span data-ttu-id="78b7f-142">[ピッキング リスト転記] フィールドで、[いいえ] を選択します。</span><span class="sxs-lookup"><span data-stu-id="78b7f-142">Select No in the Post picking list now field.</span></span>
4. <span data-ttu-id="78b7f-143">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="78b7f-143">Click OK.</span></span>
5. <span data-ttu-id="78b7f-144">アクション ウィンドウで、[表示] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="78b7f-144">On the Action Pane, click View.</span></span>
6. <span data-ttu-id="78b7f-145">[ピッキング リスト] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="78b7f-145">Click Picking list.</span></span>
7. <span data-ttu-id="78b7f-146">一覧で、選択された行のリンクをクリックします。</span><span class="sxs-lookup"><span data-stu-id="78b7f-146">In the list, click the link in the selected row.</span></span>
8. <span data-ttu-id="78b7f-147">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="78b7f-147">Close the page.</span></span>
9. <span data-ttu-id="78b7f-148">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="78b7f-148">Close the page.</span></span>
10. <span data-ttu-id="78b7f-149">[工順カード] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="78b7f-149">Click Route card.</span></span>
11. <span data-ttu-id="78b7f-150">一覧で、選択された行のリンクをクリックします。</span><span class="sxs-lookup"><span data-stu-id="78b7f-150">In the list, click the link in the selected row.</span></span>
12. <span data-ttu-id="78b7f-151">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="78b7f-151">Close the page.</span></span>
13. <span data-ttu-id="78b7f-152">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="78b7f-152">Close the page.</span></span>

