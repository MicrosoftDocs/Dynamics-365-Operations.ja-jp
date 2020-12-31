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
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Japan
ms.author: roschlom
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: cc29b4fb7e17014b4332c43a3f956ee8ea91b539
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/13/2020
ms.locfileid: "4408178"
---
# <a name="set-up-master-data-for-inclusion-of-deductible-expenses-for-multiple-posting-layers"></a><span data-ttu-id="37647-103">複数の転記階層の損金算入額のマスター データの設定</span><span class="sxs-lookup"><span data-stu-id="37647-103">Set up master data for inclusion of deductible expenses for multiple posting layers</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="37647-104">この手順では、固定資産ルールと、複数の転記階層の損金算入額に必要なマスター データの作成について説明します。</span><span class="sxs-lookup"><span data-stu-id="37647-104">This procedure walks you through creating fixed asset rules with required master data for inclusion of deductible expenses for multiple posting layers.</span></span> <span data-ttu-id="37647-105">この手順を完了する前に、 [固定資産コンフィギュレーション キー] を選択する必要があります。</span><span class="sxs-lookup"><span data-stu-id="37647-105">Before you can complete this procedure, the Fixed Assets configuration key must be selected.</span></span> <span data-ttu-id="37647-106">この手順は、デモ データ会社 JPMF を使用して作成されました。</span><span class="sxs-lookup"><span data-stu-id="37647-106">This procedure was created using the demo data company JPMF.</span></span>


## <a name="depreciation-settlement-rules"></a><span data-ttu-id="37647-107">減価償却決済ルール</span><span class="sxs-lookup"><span data-stu-id="37647-107">Depreciation settlement rules</span></span>
1. <span data-ttu-id="37647-108">[固定資産] > [設定] > [減価償却決済ルール] の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="37647-108">Go to Fixed assets > Setup > Depreciation settlement rules.</span></span>
    * <span data-ttu-id="37647-109">オプション: 決済ルール テーブルが空の場合、既定のルールをインポートするかどうかの確認を求められます。</span><span class="sxs-lookup"><span data-stu-id="37647-109">Optional: If the settlement rule table is empty, you will be asked if you want to import the default set of rules.</span></span> <span data-ttu-id="37647-110">[OK] をクリックして、既定のルールをインポートします。</span><span class="sxs-lookup"><span data-stu-id="37647-110">Click OK to import the default set of rules.</span></span>  
2. <span data-ttu-id="37647-111">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="37647-111">Click New.</span></span>
3. <span data-ttu-id="37647-112">[償却超過額] フィールドで、オプションを選択します。</span><span class="sxs-lookup"><span data-stu-id="37647-112">In the Over depreciation field, select an option.</span></span>
    * <span data-ttu-id="37647-113">[償却超過額] = [普通償却] を選択します。</span><span class="sxs-lookup"><span data-stu-id="37647-113">Select Over depreciation = Ordinary depreciation.</span></span>  
4. <span data-ttu-id="37647-114">[償却不足額] フィールドで、オプションを選択します。</span><span class="sxs-lookup"><span data-stu-id="37647-114">In the Under depreciation field, select an option.</span></span>
    * <span data-ttu-id="37647-115">[償却不足額] = [割増償却 (準備金)] を選択します。</span><span class="sxs-lookup"><span data-stu-id="37647-115">Select Under depreciation = Additional depreciation (reserve).</span></span>  
5. <span data-ttu-id="37647-116">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="37647-116">Click OK.</span></span>
6. <span data-ttu-id="37647-117">[ルール タイプでフィルター] フィールドで、オプションを選択します。</span><span class="sxs-lookup"><span data-stu-id="37647-117">In the Filter by rule type field, select an option.</span></span>
    * <span data-ttu-id="37647-118">[ルール タイプでフィルター] = [償却超過額/償却不足額の繰越] を選択します。</span><span class="sxs-lookup"><span data-stu-id="37647-118">Select Filter by rule type = Carry forward of over depreciation or under depreciation amount.</span></span>  
7. <span data-ttu-id="37647-119">[ルールの編集] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="37647-119">Click Edit rule.</span></span>
8. <span data-ttu-id="37647-120">[繰越期間 (年)] フィールドに番号を入力します。</span><span class="sxs-lookup"><span data-stu-id="37647-120">In the Periods to carry forward(years) field, enter a number.</span></span>
    * <span data-ttu-id="37647-121">この例では、 5 を入力します。</span><span class="sxs-lookup"><span data-stu-id="37647-121">For this example, enter 5.</span></span>  
9. <span data-ttu-id="37647-122">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="37647-122">Click OK.</span></span>

## <a name="book"></a><span data-ttu-id="37647-123">予約</span><span class="sxs-lookup"><span data-stu-id="37647-123">Book</span></span>
1. <span data-ttu-id="37647-124">[固定資産] > [設定] > [帳簿] の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="37647-124">Go to Fixed assets > Setup > Books.</span></span>
2. <span data-ttu-id="37647-125">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="37647-125">Click New.</span></span>
3. <span data-ttu-id="37647-126">[帳簿] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="37647-126">In the Book field, type a value.</span></span>
    * <span data-ttu-id="37647-127">この例では、Book = RBです。</span><span class="sxs-lookup"><span data-stu-id="37647-127">For this example, Book = RB.</span></span>  
4. <span data-ttu-id="37647-128">[説明] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="37647-128">In the Description field, type a value.</span></span>
5. <span data-ttu-id="37647-129">[一般] セクションを展開します。</span><span class="sxs-lookup"><span data-stu-id="37647-129">Expand the General section.</span></span>
    * <span data-ttu-id="37647-130">コアの固定資産の機能に従ってパラメーターをコンフィギュレーションします。</span><span class="sxs-lookup"><span data-stu-id="37647-130">Configure the parameters according to the core fixed asset features.</span></span>  
6. <span data-ttu-id="37647-131">取得済み帳簿のセクションを展開します。</span><span class="sxs-lookup"><span data-stu-id="37647-131">Expand the Derived books section.</span></span>
7. <span data-ttu-id="37647-132">これを参照する税関連帳簿を選択します。</span><span class="sxs-lookup"><span data-stu-id="37647-132">Select the book on the tax layer that will be referencing this one.</span></span>
    * <span data-ttu-id="37647-133">取得タイプで取得済みの帳簿を追加する場合、税関連帳簿を自動的に取得することによって作業が簡素化されます。</span><span class="sxs-lookup"><span data-stu-id="37647-133">If you add a derived book for the Acquisition type, it will simplify the operation by automatically acquiring the tax layer book.</span></span>  <span data-ttu-id="37647-134">例: NSL_TAX</span><span class="sxs-lookup"><span data-stu-id="37647-134">Example: NSL_TAX</span></span>  
8. <span data-ttu-id="37647-135">[保存] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="37647-135">Click Save.</span></span>
9. <span data-ttu-id="37647-136">クイック フィルターを使用して、レコードを見つけます。</span><span class="sxs-lookup"><span data-stu-id="37647-136">Use the Quick Filter to find records.</span></span> <span data-ttu-id="37647-137">たとえば、「NSL_TAX」の値を含む [帳簿] フィールドでフィルターします。</span><span class="sxs-lookup"><span data-stu-id="37647-137">For example, filter on the Book field with a value of 'NSL_TAX'.</span></span>
    * <span data-ttu-id="37647-138">現在の関連帳簿で精算が実行される税関連帳簿を検索します。</span><span class="sxs-lookup"><span data-stu-id="37647-138">Search for the Tax layer book that you want to run settlement with the Current layer book.</span></span>  
10. <span data-ttu-id="37647-139">[一般] セクションを展開します。</span><span class="sxs-lookup"><span data-stu-id="37647-139">Expand the General section.</span></span>
11. <span data-ttu-id="37647-140">[参照先帳簿] フィールドで、値を入力します。</span><span class="sxs-lookup"><span data-stu-id="37647-140">In the Referenced book field, type a value.</span></span>
    * <span data-ttu-id="37647-141">作成した帳簿を入力します。</span><span class="sxs-lookup"><span data-stu-id="37647-141">Type the book that you have just created.</span></span>  
12. <span data-ttu-id="37647-142">[保存] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="37647-142">Click Save.</span></span>
13. <span data-ttu-id="37647-143">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="37647-143">Close the page.</span></span>

