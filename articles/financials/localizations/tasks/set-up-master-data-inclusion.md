---
title: 複数の転記階層の損金算入額のマスター データの設定
description: この手順では、固定資産ルールと、複数の転記階層の損金算入額に必要なマスター データの作成について説明します。
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AssetAdvancedRule_JP, AssetAdvancedRuleCreateEdit_JP,  AssetBookTable
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Japan
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 88d797b85961a6b6f7ad0add97c857b6c9032907
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/15/2019
ms.locfileid: "1549037"
---
# <a name="set-up-master-data-for-inclusion-of-deductible-expenses-for-multiple-posting-layers"></a><span data-ttu-id="ea122-103">複数の転記階層の損金算入額のマスター データの設定</span><span class="sxs-lookup"><span data-stu-id="ea122-103">Set up master data for inclusion of deductible expenses for multiple posting layers</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="ea122-104">この手順では、固定資産ルールと、複数の転記階層の損金算入額に必要なマスター データの作成について説明します。</span><span class="sxs-lookup"><span data-stu-id="ea122-104">This procedure walks you through creating fixed asset rules with required master data for inclusion of deductible expenses for multiple posting layers.</span></span> <span data-ttu-id="ea122-105">この手順を完了する前に、 [固定資産コンフィギュレーション キー] を選択する必要があります。</span><span class="sxs-lookup"><span data-stu-id="ea122-105">Before you can complete this procedure, the Fixed Assets configuration key must be selected.</span></span> <span data-ttu-id="ea122-106">この手順は、デモ データ会社 JPMF を使用して作成されました。</span><span class="sxs-lookup"><span data-stu-id="ea122-106">This procedure was created using the demo data company JPMF.</span></span>


## <a name="depreciation-settlement-rules"></a><span data-ttu-id="ea122-107">減価償却決済ルール</span><span class="sxs-lookup"><span data-stu-id="ea122-107">Depreciation settlement rules</span></span>
1. <span data-ttu-id="ea122-108">[固定資産] > [設定] > [減価償却決済ルール] の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="ea122-108">Go to Fixed assets > Setup > Depreciation settlement rules.</span></span>
    * <span data-ttu-id="ea122-109">オプション: 決済ルール テーブルが空の場合、既定のルールをインポートするかどうかの確認を求められます。</span><span class="sxs-lookup"><span data-stu-id="ea122-109">Optional: If the settlement rule table is empty, you will be asked if you want to import the default set of rules.</span></span> <span data-ttu-id="ea122-110">[OK] をクリックして、既定のルールをインポートします。</span><span class="sxs-lookup"><span data-stu-id="ea122-110">Click OK to import the default set of rules.</span></span>  
2. <span data-ttu-id="ea122-111">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="ea122-111">Click New.</span></span>
3. <span data-ttu-id="ea122-112">[償却超過額] フィールドで、オプションを選択します。</span><span class="sxs-lookup"><span data-stu-id="ea122-112">In the Over depreciation field, select an option.</span></span>
    * <span data-ttu-id="ea122-113">[償却超過額] = [普通償却] を選択します。</span><span class="sxs-lookup"><span data-stu-id="ea122-113">Select Over depreciation = Ordinary depreciation.</span></span>  
4. <span data-ttu-id="ea122-114">[償却不足額] フィールドで、オプションを選択します。</span><span class="sxs-lookup"><span data-stu-id="ea122-114">In the Under depreciation field, select an option.</span></span>
    * <span data-ttu-id="ea122-115">[償却不足額] = [割増償却 (準備金)] を選択します。</span><span class="sxs-lookup"><span data-stu-id="ea122-115">Select Under depreciation = Additional depreciation (reserve).</span></span>  
5. <span data-ttu-id="ea122-116">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="ea122-116">Click OK.</span></span>
6. <span data-ttu-id="ea122-117">[ルール タイプでフィルター] フィールドで、オプションを選択します。</span><span class="sxs-lookup"><span data-stu-id="ea122-117">In the Filter by rule type field, select an option.</span></span>
    * <span data-ttu-id="ea122-118">[ルール タイプでフィルター] = [償却超過額/償却不足額の繰越] を選択します。</span><span class="sxs-lookup"><span data-stu-id="ea122-118">Select Filter by rule type = Carry forward of over depreciation or under depreciation amount.</span></span>  
7. <span data-ttu-id="ea122-119">[ルールの編集] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="ea122-119">Click Edit rule.</span></span>
8. <span data-ttu-id="ea122-120">[繰越期間 (年)] フィールドに番号を入力します。</span><span class="sxs-lookup"><span data-stu-id="ea122-120">In the Periods to carry forward(years) field, enter a number.</span></span>
    * <span data-ttu-id="ea122-121">この例では、 5 を入力します。</span><span class="sxs-lookup"><span data-stu-id="ea122-121">For this example, enter 5.</span></span>  
9. <span data-ttu-id="ea122-122">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="ea122-122">Click OK.</span></span>

## <a name="book"></a><span data-ttu-id="ea122-123">予約</span><span class="sxs-lookup"><span data-stu-id="ea122-123">Book</span></span>
1. <span data-ttu-id="ea122-124">[固定資産] > [設定] > [帳簿] の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="ea122-124">Go to Fixed assets > Setup > Books.</span></span>
2. <span data-ttu-id="ea122-125">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="ea122-125">Click New.</span></span>
3. <span data-ttu-id="ea122-126">[帳簿] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="ea122-126">In the Book field, type a value.</span></span>
    * <span data-ttu-id="ea122-127">この例では、Book = RBです。</span><span class="sxs-lookup"><span data-stu-id="ea122-127">For this example, Book = RB.</span></span>  
4. <span data-ttu-id="ea122-128">[説明] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="ea122-128">In the Description field, type a value.</span></span>
5. <span data-ttu-id="ea122-129">[一般] セクションを展開します。</span><span class="sxs-lookup"><span data-stu-id="ea122-129">Expand the General section.</span></span>
    * <span data-ttu-id="ea122-130">コアの固定資産の機能に従ってパラメーターをコンフィギュレーションします。</span><span class="sxs-lookup"><span data-stu-id="ea122-130">Configure the parameters according to the core fixed asset features.</span></span>  
6. <span data-ttu-id="ea122-131">取得済み帳簿のセクションを展開します。</span><span class="sxs-lookup"><span data-stu-id="ea122-131">Expand the Derived books section.</span></span>
7. <span data-ttu-id="ea122-132">これを参照する税関連帳簿を選択します。</span><span class="sxs-lookup"><span data-stu-id="ea122-132">Select the book on the tax layer that will be referencing this one.</span></span>
    * <span data-ttu-id="ea122-133">取得タイプで取得済みの帳簿を追加する場合、税関連帳簿を自動的に取得することによって作業が簡素化されます。</span><span class="sxs-lookup"><span data-stu-id="ea122-133">If you add a derived book for the Acquisition type, it will simplify the operation by automatically acquiring the tax layer book.</span></span>  <span data-ttu-id="ea122-134">例: NSL_TAX</span><span class="sxs-lookup"><span data-stu-id="ea122-134">Example: NSL_TAX</span></span>  
8. <span data-ttu-id="ea122-135">[保存] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="ea122-135">Click Save.</span></span>
9. <span data-ttu-id="ea122-136">クイック フィルターを使用して、レコードを見つけます。</span><span class="sxs-lookup"><span data-stu-id="ea122-136">Use the Quick Filter to find records.</span></span> <span data-ttu-id="ea122-137">たとえば、「NSL_TAX」の値を含む [帳簿] フィールドでフィルターします。</span><span class="sxs-lookup"><span data-stu-id="ea122-137">For example, filter on the Book field with a value of 'NSL_TAX'.</span></span>
    * <span data-ttu-id="ea122-138">現在の関連帳簿で精算が実行される税関連帳簿を検索します。</span><span class="sxs-lookup"><span data-stu-id="ea122-138">Search for the Tax layer book that you want to run settlement with the Current layer book.</span></span>  
10. <span data-ttu-id="ea122-139">[一般] セクションを展開します。</span><span class="sxs-lookup"><span data-stu-id="ea122-139">Expand the General section.</span></span>
11. <span data-ttu-id="ea122-140">[参照先帳簿] フィールドで、値を入力します。</span><span class="sxs-lookup"><span data-stu-id="ea122-140">In the Referenced book field, type a value.</span></span>
    * <span data-ttu-id="ea122-141">作成した帳簿を入力します。</span><span class="sxs-lookup"><span data-stu-id="ea122-141">Type the book that you have just created.</span></span>  
12. <span data-ttu-id="ea122-142">[保存] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="ea122-142">Click Save.</span></span>
13. <span data-ttu-id="ea122-143">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="ea122-143">Close the page.</span></span>

