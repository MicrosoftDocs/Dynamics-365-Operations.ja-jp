---
title: 固定資産の取得と政府助成金の申請
description: 固定資産の取得および政府補助金の申請についての説明を見るには、このタスクを使用します。
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerJournalTable, LedgerJournalTransAsset, SysQueryForm
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Japan
ms.author: roschlom
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: cf0653fbbb571327ffb0bcba5d54222e6cfb57b9
ms.sourcegitcommit: 708ca25687a4e48271cdcd6d2d22d99fb94cf140
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/10/2020
ms.locfileid: "3981464"
---
# <a name="acquire-a-fixed-asset-and-claim-for-the-government-grant-subsidy"></a><span data-ttu-id="0abd0-103">固定資産の取得と政府助成金の申請</span><span class="sxs-lookup"><span data-stu-id="0abd0-103">Acquire a fixed asset and claim for the government grant subsidy</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="0abd0-104">固定資産の取得および政府補助金の申請についての説明を見るには、このタスクを使用します。</span><span class="sxs-lookup"><span data-stu-id="0abd0-104">Use this task to walk through acquiring a fixed asset and then claiming it for a government grant.</span></span>



<span data-ttu-id="0abd0-105">このタスクを完了するためには、[固定資産コンフィギュレーション キー] を選択する必要があります。</span><span class="sxs-lookup"><span data-stu-id="0abd0-105">In order to complete this task, the Fixed Asset configuration key must be selected.</span></span>



<span data-ttu-id="0abd0-106">このタスクでは、JPMF のデモ データを使用します。</span><span class="sxs-lookup"><span data-stu-id="0abd0-106">This task uses the JPMF demo data.</span></span>


## <a name="acquire-the-fixed-asset"></a><span data-ttu-id="0abd0-107">固定資産の取得</span><span class="sxs-lookup"><span data-stu-id="0abd0-107">Acquire the fixed asset</span></span>
1. <span data-ttu-id="0abd0-108">[固定資産] > [仕訳入力] > [固定資産仕訳帳] の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="0abd0-108">Go to Fixed assets > Journal entries > Fixed assets journal.</span></span>
2. <span data-ttu-id="0abd0-109">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="0abd0-109">Click New.</span></span>
3. <span data-ttu-id="0abd0-110">[名前] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="0abd0-110">In the Name field, type a value.</span></span>
4. <span data-ttu-id="0abd0-111">[明細行] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="0abd0-111">Click Lines.</span></span>
5. <span data-ttu-id="0abd0-112">[日付] フィールドに日付を入力します。</span><span class="sxs-lookup"><span data-stu-id="0abd0-112">In the Date field, enter a date.</span></span>
6. <span data-ttu-id="0abd0-113">[勘定] フィールドで、任意の値を指定します。</span><span class="sxs-lookup"><span data-stu-id="0abd0-113">In the Account field, specify the desired values.</span></span>
    * <span data-ttu-id="0abd0-114">取得する固定資産を選択します。</span><span class="sxs-lookup"><span data-stu-id="0abd0-114">Select the fixed asset to acquire.</span></span>  
7. <span data-ttu-id="0abd0-115">[帳簿] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="0abd0-115">In the Book field, type a value.</span></span>
8. <span data-ttu-id="0abd0-116">[借方] フィールドに数値を入力します。</span><span class="sxs-lookup"><span data-stu-id="0abd0-116">In the Debit field, enter a number.</span></span>
9. <span data-ttu-id="0abd0-117">[保存] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="0abd0-117">Click Save.</span></span>
10. <span data-ttu-id="0abd0-118">[転記] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="0abd0-118">Click Post.</span></span>

## <a name="claim-the-fixed-asset-for-a-government-grant"></a><span data-ttu-id="0abd0-119">固定資産の政府助成金の申請</span><span class="sxs-lookup"><span data-stu-id="0abd0-119">Claim the fixed asset for a government grant</span></span>
1. <span data-ttu-id="0abd0-120">[固定資産] > [仕訳入力] > [固定資産仕訳帳] の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="0abd0-120">Go to Fixed assets > Journal entries > Fixed assets journal.</span></span>
2. <span data-ttu-id="0abd0-121">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="0abd0-121">Click New.</span></span>
3. <span data-ttu-id="0abd0-122">[名前] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="0abd0-122">In the Name field, type a value.</span></span>
4. <span data-ttu-id="0abd0-123">[保存] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="0abd0-123">Click Save.</span></span>
5. <span data-ttu-id="0abd0-124">[明細行] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="0abd0-124">Click Lines.</span></span>
6. <span data-ttu-id="0abd0-125">[提案] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="0abd0-125">Click Proposals.</span></span>
7. <span data-ttu-id="0abd0-126">[圧縮記帳の提案] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="0abd0-126">Click Reduction entry proposal.</span></span>
8. <span data-ttu-id="0abd0-127">[フィルター] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="0abd0-127">Click Filter.</span></span>
    * <span data-ttu-id="0abd0-128">フィルタ処理により、固定資産のより速く検索できます。</span><span class="sxs-lookup"><span data-stu-id="0abd0-128">You can filter to help find the fixed asset faster.</span></span>  
9. <span data-ttu-id="0abd0-129">[基準] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="0abd0-129">In the Criteria field, type a value.</span></span>
10. <span data-ttu-id="0abd0-130">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="0abd0-130">Click OK.</span></span>
11. <span data-ttu-id="0abd0-131">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="0abd0-131">Click OK.</span></span>
12. <span data-ttu-id="0abd0-132">[日付] フィールドに日付を入力します。</span><span class="sxs-lookup"><span data-stu-id="0abd0-132">In the Date field, enter a date.</span></span>
    * <span data-ttu-id="0abd0-133">助成金を仕訳入力する会計日を入力します。</span><span class="sxs-lookup"><span data-stu-id="0abd0-133">Enter the accounting date on which to journalize the subsidy.</span></span>  
13. <span data-ttu-id="0abd0-134">[貸方] フィールドに数値を入力します。</span><span class="sxs-lookup"><span data-stu-id="0abd0-134">In the Credit field, enter a number.</span></span>
    * <span data-ttu-id="0abd0-135">政府助成金を入力します。</span><span class="sxs-lookup"><span data-stu-id="0abd0-135">Enter the amount of the government grant.</span></span>  
14. <span data-ttu-id="0abd0-136">[転記] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="0abd0-136">Click Post.</span></span>

