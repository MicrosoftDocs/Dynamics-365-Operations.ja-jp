---
title: 特別償却の提案
description: 日本では、特定の条件下で特別償却が許可されます。
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerJournalTable, LedgerJournalTransAsset, SysQueryForm
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Japan
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: d8929755858ce3a531a367ea18869cdc3761382b
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/29/2019
ms.locfileid: "371145"
---
# <a name="propose-special-depreciation"></a><span data-ttu-id="8a18f-103">特別償却の提案</span><span class="sxs-lookup"><span data-stu-id="8a18f-103">Propose special depreciation</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="8a18f-104">日本では、特定の条件下で特別償却が許可されます。</span><span class="sxs-lookup"><span data-stu-id="8a18f-104">In Japan, a special depreciation is permitted under certain conditions.</span></span> <span data-ttu-id="8a18f-105">引当メソッドの場合、このタスクには 2 つのステップがあります。準備金の転記と準備金配賦の転記です。</span><span class="sxs-lookup"><span data-stu-id="8a18f-105">For Reserve method, this is a two step task: post reserve, and then post reserve allocation.</span></span> <span data-ttu-id="8a18f-106">ディレクト オフ メソッドの場合、必要なステップは 1 つです。これは準備金の転記と同じ手順です。</span><span class="sxs-lookup"><span data-stu-id="8a18f-106">For Direct-off method, only one step is needed, which is the same procedure as post reserve.</span></span> 



<span data-ttu-id="8a18f-107">この手順では、引当メソッドによる特別償却の提案方法を説明します。</span><span class="sxs-lookup"><span data-stu-id="8a18f-107">Use this procedure to learn how to propose special depreciation under Reserve method.</span></span>

<span data-ttu-id="8a18f-108">この手順を実行する前に固定資産が取得済であることを確認します。</span><span class="sxs-lookup"><span data-stu-id="8a18f-108">Make sure that the fixed asset has been acquired before following this procedure.</span></span> <span data-ttu-id="8a18f-109">また、[固定資産コンフィギュレーション キー] が選択されていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="8a18f-109">Also, be sure that the Fixed Assets configuration key is selected.</span></span>



<span data-ttu-id="8a18f-110">この手順では、JPMF デモ会社のデータを使用します。</span><span class="sxs-lookup"><span data-stu-id="8a18f-110">This procedure uses the JPMF demo company data.</span></span>


## <a name="post-reserve"></a><span data-ttu-id="8a18f-111">準備金の転記</span><span class="sxs-lookup"><span data-stu-id="8a18f-111">Post Reserve</span></span>
1. <span data-ttu-id="8a18f-112">[固定資産] > [仕訳入力] > [固定資産仕訳帳] の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="8a18f-112">Go to Fixed assets > Journal entries > Fixed assets journal.</span></span>
2. <span data-ttu-id="8a18f-113">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="8a18f-113">Click New.</span></span>
3. <span data-ttu-id="8a18f-114">[名前] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="8a18f-114">In the Name field, type a value.</span></span>
4. <span data-ttu-id="8a18f-115">[保存] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="8a18f-115">Click Save.</span></span>
5. <span data-ttu-id="8a18f-116">[明細行] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="8a18f-116">Click Lines.</span></span>
6. <span data-ttu-id="8a18f-117">[提案] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="8a18f-117">Click Proposals.</span></span>
7. <span data-ttu-id="8a18f-118">[特別償却提案] クリックします。</span><span class="sxs-lookup"><span data-stu-id="8a18f-118">Click Extraordinary depreciation proposal.</span></span>
8. <span data-ttu-id="8a18f-119">[終了日] フィールドで、日付を入力します。</span><span class="sxs-lookup"><span data-stu-id="8a18f-119">In the To date field, enter a date.</span></span>
9. <span data-ttu-id="8a18f-120">[フィルター] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="8a18f-120">Click Filter.</span></span>
10. <span data-ttu-id="8a18f-121">[基準] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="8a18f-121">In the Criteria field, type a value.</span></span>
11. <span data-ttu-id="8a18f-122">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="8a18f-122">Click OK.</span></span>
12. <span data-ttu-id="8a18f-123">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="8a18f-123">Click OK.</span></span>
13. <span data-ttu-id="8a18f-124">[転記] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="8a18f-124">Click Post.</span></span>

## <a name="post-reserve-allocation"></a><span data-ttu-id="8a18f-125">準備金配賦の転記</span><span class="sxs-lookup"><span data-stu-id="8a18f-125">Post Reserve allocation</span></span>
1. <span data-ttu-id="8a18f-126">[固定資産] > [仕訳入力] > [固定資産仕訳帳] の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="8a18f-126">Go to Fixed assets > Journal entries > Fixed assets journal.</span></span>
2. <span data-ttu-id="8a18f-127">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="8a18f-127">Click New.</span></span>
3. <span data-ttu-id="8a18f-128">[名前] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="8a18f-128">In the Name field, type a value.</span></span>
4. <span data-ttu-id="8a18f-129">[保存] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="8a18f-129">Click Save.</span></span>
5. <span data-ttu-id="8a18f-130">[明細行] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="8a18f-130">Click Lines.</span></span>
6. <span data-ttu-id="8a18f-131">[提案] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="8a18f-131">Click Proposals.</span></span>
7. <span data-ttu-id="8a18f-132">[特別償却提案] クリックします。</span><span class="sxs-lookup"><span data-stu-id="8a18f-132">Click Extraordinary depreciation proposal.</span></span>
8. <span data-ttu-id="8a18f-133">[終了日] フィールドで、日付を入力します。</span><span class="sxs-lookup"><span data-stu-id="8a18f-133">In the To date field, enter a date.</span></span>
    * <span data-ttu-id="8a18f-134">[準備金配賦開始日] は、[取崩開始] によって異なります。</span><span class="sxs-lookup"><span data-stu-id="8a18f-134">Depending on the Allocation start convention, the Reserve allocation start date is different.</span></span>  
9. <span data-ttu-id="8a18f-135">[フィルター] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="8a18f-135">Click Filter.</span></span>
10. <span data-ttu-id="8a18f-136">[基準] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="8a18f-136">In the Criteria field, type a value.</span></span>
11. <span data-ttu-id="8a18f-137">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="8a18f-137">Click OK.</span></span>
12. <span data-ttu-id="8a18f-138">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="8a18f-138">Click OK.</span></span>
13. <span data-ttu-id="8a18f-139">[転記] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="8a18f-139">Click Post.</span></span>

