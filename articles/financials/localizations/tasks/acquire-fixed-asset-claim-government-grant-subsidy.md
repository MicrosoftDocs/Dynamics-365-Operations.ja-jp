--- 
title: "固定資産の取得と政府助成金の申請"
description: "固定資産の取得および政府補助金の申請についての説明を見るには、このタスクを使用します。"
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: LedgerJournalTable, LedgerJournalTransAsset, SysQueryForm
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Japan
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 0312b8cfadd45f8e59225e9daba78b9e216cff51
ms.openlocfilehash: aa1212248f1c35246992b54de2cd323b4c02531e
ms.contentlocale: ja-jp
ms.lasthandoff: 10/16/2018

---
# <a name="acquire-a-fixed-asset-and-claim-for-the-government-grant-subsidy"></a><span data-ttu-id="12514-103">固定資産の取得と政府助成金の申請</span><span class="sxs-lookup"><span data-stu-id="12514-103">Acquire a fixed asset and claim for the government grant subsidy</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="12514-104">固定資産の取得および政府補助金の申請についての説明を見るには、このタスクを使用します。</span><span class="sxs-lookup"><span data-stu-id="12514-104">Use this task to walk through acquiring a fixed asset and then claiming it for a government grant.</span></span>



<span data-ttu-id="12514-105">このタスクを完了するためには、[固定資産コンフィギュレーション キー] を選択する必要があります。</span><span class="sxs-lookup"><span data-stu-id="12514-105">In order to complete this task, the Fixed Asset configuration key must be selected.</span></span>



<span data-ttu-id="12514-106">このタスクでは、JPMF のデモ データを使用します。</span><span class="sxs-lookup"><span data-stu-id="12514-106">This task uses the JPMF demo data.</span></span>


## <a name="acquire-the-fixed-asset"></a><span data-ttu-id="12514-107">固定資産の取得</span><span class="sxs-lookup"><span data-stu-id="12514-107">Acquire the fixed asset</span></span>
1. <span data-ttu-id="12514-108">[固定資産] > [仕訳入力] > [固定資産仕訳帳] の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="12514-108">Go to Fixed assets > Journal entries > Fixed assets journal.</span></span>
2. <span data-ttu-id="12514-109">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="12514-109">Click New.</span></span>
3. <span data-ttu-id="12514-110">[名前] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="12514-110">In the Name field, type a value.</span></span>
4. <span data-ttu-id="12514-111">[明細行] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="12514-111">Click Lines.</span></span>
5. <span data-ttu-id="12514-112">[日付] フィールドに日付を入力します。</span><span class="sxs-lookup"><span data-stu-id="12514-112">In the Date field, enter a date.</span></span>
6. <span data-ttu-id="12514-113">[勘定] フィールドで、任意の値を指定します。</span><span class="sxs-lookup"><span data-stu-id="12514-113">In the Account field, specify the desired values.</span></span>
    * <span data-ttu-id="12514-114">取得する固定資産を選択します。</span><span class="sxs-lookup"><span data-stu-id="12514-114">Select the fixed asset to acquire.</span></span>  
7. <span data-ttu-id="12514-115">[帳簿] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="12514-115">In the Book field, type a value.</span></span>
8. <span data-ttu-id="12514-116">[借方] フィールドに数値を入力します。</span><span class="sxs-lookup"><span data-stu-id="12514-116">In the Debit field, enter a number.</span></span>
9. <span data-ttu-id="12514-117">[保存] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="12514-117">Click Save.</span></span>
10. <span data-ttu-id="12514-118">[転記] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="12514-118">Click Post.</span></span>

## <a name="claim-the-fixed-asset-for-a-government-grant"></a><span data-ttu-id="12514-119">固定資産の政府助成金の申請</span><span class="sxs-lookup"><span data-stu-id="12514-119">Claim the fixed asset for a government grant</span></span>
1. <span data-ttu-id="12514-120">[固定資産] > [仕訳入力] > [固定資産仕訳帳] の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="12514-120">Go to Fixed assets > Journal entries > Fixed assets journal.</span></span>
2. <span data-ttu-id="12514-121">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="12514-121">Click New.</span></span>
3. <span data-ttu-id="12514-122">[名前] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="12514-122">In the Name field, type a value.</span></span>
4. <span data-ttu-id="12514-123">[保存] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="12514-123">Click Save.</span></span>
5. <span data-ttu-id="12514-124">[明細行] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="12514-124">Click Lines.</span></span>
6. <span data-ttu-id="12514-125">[提案] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="12514-125">Click Proposals.</span></span>
7. <span data-ttu-id="12514-126">[圧縮記帳の提案] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="12514-126">Click Reduction entry proposal.</span></span>
8. <span data-ttu-id="12514-127">[フィルター] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="12514-127">Click Filter.</span></span>
    * <span data-ttu-id="12514-128">フィルタ処理により、固定資産のより速く検索できます。</span><span class="sxs-lookup"><span data-stu-id="12514-128">You can filter to help find the fixed asset faster.</span></span>  
9. <span data-ttu-id="12514-129">[基準] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="12514-129">In the Criteria field, type a value.</span></span>
10. <span data-ttu-id="12514-130">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="12514-130">Click OK.</span></span>
11. <span data-ttu-id="12514-131">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="12514-131">Click OK.</span></span>
12. <span data-ttu-id="12514-132">[日付] フィールドに日付を入力します。</span><span class="sxs-lookup"><span data-stu-id="12514-132">In the Date field, enter a date.</span></span>
    * <span data-ttu-id="12514-133">助成金を仕訳入力する会計日を入力します。</span><span class="sxs-lookup"><span data-stu-id="12514-133">Enter the accounting date on which to journalize the subsidy.</span></span>  
13. <span data-ttu-id="12514-134">[貸方] フィールドに数値を入力します。</span><span class="sxs-lookup"><span data-stu-id="12514-134">In the Credit field, enter a number.</span></span>
    * <span data-ttu-id="12514-135">政府助成金を入力します。</span><span class="sxs-lookup"><span data-stu-id="12514-135">Enter the amount of the government grant.</span></span>  
14. <span data-ttu-id="12514-136">[転記] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="12514-136">Click Post.</span></span>


