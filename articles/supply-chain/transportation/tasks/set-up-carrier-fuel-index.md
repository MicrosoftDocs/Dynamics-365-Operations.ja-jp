---
title: 配送業者の燃料インデックスの設定
description: このガイドでは、燃料インデックス領域、燃料インデックス、および輸送業者の燃料インデックスを作成する方法を説明します。
author: ShylaThompson
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 73336c6803f28239ff8ca78dcff5ea8db0835e32
ms.sourcegitcommit: fcb27d6a46cd544feef34f6ec7607bdd46b0c12b
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/18/2020
ms.locfileid: "3146260"
---
# <a name="set-up-a-carrier-fuel-index"></a><span data-ttu-id="2149f-103">配送業者の燃料インデックスの設定</span><span class="sxs-lookup"><span data-stu-id="2149f-103">Set up a carrier fuel index</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="2149f-104">このガイドでは、燃料インデックス領域、燃料インデックス、および輸送業者の燃料インデックスを作成する方法を説明します。</span><span class="sxs-lookup"><span data-stu-id="2149f-104">This guide shows how to create a fuel index region, a fuel index and a carrier fuel index.</span></span> <span data-ttu-id="2149f-105">燃料インデックス領域は燃料インデックスを適用する地域を指定し、燃料インデックスは特定の期間の燃料価格を指定します。</span><span class="sxs-lookup"><span data-stu-id="2149f-105">The fuel index region specifies which region the fuel index should apply to, and the fuel index specifies a fuel price for a particular period of time.</span></span> <span data-ttu-id="2149f-106">時間経過に伴う燃料価格の変化を反映させる場合は、輸送業者に複数の燃料インデックスを関連付けることができます。</span><span class="sxs-lookup"><span data-stu-id="2149f-106">To reflect the change in fuel prices over time, you can associate multiple fuel indexes with a carrier.</span></span>  <span data-ttu-id="2149f-107">通常これらのタスクは配送コーディネーターが行います。</span><span class="sxs-lookup"><span data-stu-id="2149f-107">These tasks are normally done by a transportation coordinator.</span></span> <span data-ttu-id="2149f-108">デモ データの会社 USMF でこの手順を使用するか、または独自のデータを使用できます。</span><span class="sxs-lookup"><span data-stu-id="2149f-108">You can use this procedure in demo data company USMF or using your own data.</span></span>


## <a name="create-a-fuel-index-region"></a><span data-ttu-id="2149f-109">配送業者の燃料インデックス地域の作成</span><span class="sxs-lookup"><span data-stu-id="2149f-109">Create a fuel index region</span></span>
1. <span data-ttu-id="2149f-110">[配送管理] > [設定] > [燃料インデックス] > [燃料インデックス地域] に移動します。</span><span class="sxs-lookup"><span data-stu-id="2149f-110">Go to Transportation management > Setup > Fuel indexes > Fuel index regions.</span></span>
    * <span data-ttu-id="2149f-111">最初に異なる地域を作成し、稼働場所、および異なる燃料割増金を計算する必要があります。</span><span class="sxs-lookup"><span data-stu-id="2149f-111">First you have to create the different regions, where you operate and calculate different fuel surcharges.</span></span>  
2. <span data-ttu-id="2149f-112">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="2149f-112">Click New.</span></span>
3. <span data-ttu-id="2149f-113">[地域] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="2149f-113">In the Region field, type a value.</span></span>
4. <span data-ttu-id="2149f-114">[名前] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="2149f-114">In the Name field, type a value.</span></span>
5. <span data-ttu-id="2149f-115">[保存] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="2149f-115">Click Save.</span></span>

## <a name="create-a-fuel-index"></a><span data-ttu-id="2149f-116">燃料インデックスの作成</span><span class="sxs-lookup"><span data-stu-id="2149f-116">Create a fuel index</span></span>
1. <span data-ttu-id="2149f-117">[輸送管理] > [設定] > [燃料インデックス] > [燃料インデックス] に移動します。</span><span class="sxs-lookup"><span data-stu-id="2149f-117">Go to Transportation management > Setup > Fuel indexes > Fuel indexes.</span></span>
    * <span data-ttu-id="2149f-118">設定した地域については、現在の燃料価格を入力する必要があります。</span><span class="sxs-lookup"><span data-stu-id="2149f-118">For the regions you have set up you need to enter the current prices for the fuel.</span></span>  
2. <span data-ttu-id="2149f-119">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="2149f-119">Click New.</span></span>
3. <span data-ttu-id="2149f-120">[地域] フィールドで、ドロップ ダウン ボタンをクリックし、ルックアップを開きます。</span><span class="sxs-lookup"><span data-stu-id="2149f-120">In the Region field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="2149f-121">一覧で、選択された行のリンクをクリックします。</span><span class="sxs-lookup"><span data-stu-id="2149f-121">In the list, click the link in the selected row.</span></span>
5. <span data-ttu-id="2149f-122">[ガロンあたりの価格] フィールドに数値を入力します。</span><span class="sxs-lookup"><span data-stu-id="2149f-122">In the Price per gallon field, enter a number.</span></span>
6. <span data-ttu-id="2149f-123">[有効開始日時] フィールドで、日時を入力します。</span><span class="sxs-lookup"><span data-stu-id="2149f-123">In the Effective start date and time field, enter a date and time.</span></span>
7. <span data-ttu-id="2149f-124">[保存] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="2149f-124">Click Save.</span></span>

## <a name="create-a-carrier-fuel-index"></a><span data-ttu-id="2149f-125">配送業者の燃料インデックスの作成</span><span class="sxs-lookup"><span data-stu-id="2149f-125">Create a Carrier fuel index</span></span>
1. <span data-ttu-id="2149f-126">[輸送管理] > [設定] > [燃料インデックス] > [輸送業者の燃料インデックス] に移動します。</span><span class="sxs-lookup"><span data-stu-id="2149f-126">Go to Transportation management > Setup > Fuel indexes > Carrier fuel indexes.</span></span>
2. <span data-ttu-id="2149f-127">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="2149f-127">Click New.</span></span>
3. <span data-ttu-id="2149f-128">[配送業者の燃料インデックス] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="2149f-128">In the Carrier fuel index field, type a value.</span></span>
4. <span data-ttu-id="2149f-129">[説明] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="2149f-129">In the Description field, type a value.</span></span>
5. <span data-ttu-id="2149f-130">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="2149f-130">Click New.</span></span>
6. <span data-ttu-id="2149f-131">[有効開始日時] フィールドで、日時を入力します。</span><span class="sxs-lookup"><span data-stu-id="2149f-131">In the Effective start date and time field, enter a date and time.</span></span>
7. <span data-ttu-id="2149f-132">[PPG ソース フィールド] フィールドに数値を入力します。</span><span class="sxs-lookup"><span data-stu-id="2149f-132">In the PPG From field, enter a number.</span></span>
    * <span data-ttu-id="2149f-133">この例では、PPG ソース フィールドを「1.95」に設定できます。</span><span class="sxs-lookup"><span data-stu-id="2149f-133">In this example, you can set PPG From field to 1.95.</span></span>  
8. <span data-ttu-id="2149f-134">[PPG ターゲット フィールド] フィールドに数値を入力します。</span><span class="sxs-lookup"><span data-stu-id="2149f-134">In the PPG To field, enter a number.</span></span>
    * <span data-ttu-id="2149f-135">この例では、PPG ターゲット フィールドを「2」に設定できます。</span><span class="sxs-lookup"><span data-stu-id="2149f-135">In this example you can set the PPG To field to 2.</span></span>  
9. <span data-ttu-id="2149f-136">[割合] フィールドに数値を入力します。</span><span class="sxs-lookup"><span data-stu-id="2149f-136">In the Percentage field, enter a number.</span></span>
    * <span data-ttu-id="2149f-137">この例では、割合を「3」に設定できます。</span><span class="sxs-lookup"><span data-stu-id="2149f-137">In this example you can set the percentage to 3.</span></span>  
10. <span data-ttu-id="2149f-138">[通貨] フィールドで、ドロップ ダウン ボタンをクリックし、ルックアップを開きます。</span><span class="sxs-lookup"><span data-stu-id="2149f-138">In the Currency field, click the drop-down button to open the lookup.</span></span>
11. <span data-ttu-id="2149f-139">一覧で、目的のレコードを見つけ、選択します。</span><span class="sxs-lookup"><span data-stu-id="2149f-139">In the list, find and select the desired record.</span></span>
12. <span data-ttu-id="2149f-140">一覧で、選択された行のリンクをクリックします。</span><span class="sxs-lookup"><span data-stu-id="2149f-140">In the list, click the link in the selected row.</span></span>
13. <span data-ttu-id="2149f-141">[保存] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="2149f-141">Click Save.</span></span>

