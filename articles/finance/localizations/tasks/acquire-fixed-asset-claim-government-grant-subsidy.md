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
ms.search.region: Japan
ms.author: roschlom
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 0b0a8a3dca77e6d082fa76658b211085822f4dc2
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/15/2021
ms.locfileid: "5253890"
---
# <a name="acquire-a-fixed-asset-and-claim-for-the-government-grant-subsidy"></a><span data-ttu-id="896d9-103">固定資産の取得と政府助成金の申請</span><span class="sxs-lookup"><span data-stu-id="896d9-103">Acquire a fixed asset and claim for the government grant subsidy</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="896d9-104">固定資産の取得および政府補助金の申請についての説明を見るには、このタスクを使用します。</span><span class="sxs-lookup"><span data-stu-id="896d9-104">Use this task to walk through acquiring a fixed asset and then claiming it for a government grant.</span></span>



<span data-ttu-id="896d9-105">このタスクを完了するためには、[固定資産コンフィギュレーション キー] を選択する必要があります。</span><span class="sxs-lookup"><span data-stu-id="896d9-105">In order to complete this task, the Fixed Asset configuration key must be selected.</span></span>



<span data-ttu-id="896d9-106">このタスクでは、JPMF のデモ データを使用します。</span><span class="sxs-lookup"><span data-stu-id="896d9-106">This task uses the JPMF demo data.</span></span>


## <a name="acquire-the-fixed-asset"></a><span data-ttu-id="896d9-107">固定資産の取得</span><span class="sxs-lookup"><span data-stu-id="896d9-107">Acquire the fixed asset</span></span>
1. <span data-ttu-id="896d9-108">[固定資産] > [仕訳入力] > [固定資産仕訳帳] の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="896d9-108">Go to Fixed assets > Journal entries > Fixed assets journal.</span></span>
2. <span data-ttu-id="896d9-109">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="896d9-109">Click New.</span></span>
3. <span data-ttu-id="896d9-110">[名前] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="896d9-110">In the Name field, type a value.</span></span>
4. <span data-ttu-id="896d9-111">[明細行] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="896d9-111">Click Lines.</span></span>
5. <span data-ttu-id="896d9-112">[日付] フィールドに日付を入力します。</span><span class="sxs-lookup"><span data-stu-id="896d9-112">In the Date field, enter a date.</span></span>
6. <span data-ttu-id="896d9-113">[勘定] フィールドで、任意の値を指定します。</span><span class="sxs-lookup"><span data-stu-id="896d9-113">In the Account field, specify the desired values.</span></span>
    * <span data-ttu-id="896d9-114">取得する固定資産を選択します。</span><span class="sxs-lookup"><span data-stu-id="896d9-114">Select the fixed asset to acquire.</span></span>  
7. <span data-ttu-id="896d9-115">[帳簿] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="896d9-115">In the Book field, type a value.</span></span>
8. <span data-ttu-id="896d9-116">[借方] フィールドに数値を入力します。</span><span class="sxs-lookup"><span data-stu-id="896d9-116">In the Debit field, enter a number.</span></span>
9. <span data-ttu-id="896d9-117">[保存] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="896d9-117">Click Save.</span></span>
10. <span data-ttu-id="896d9-118">[転記] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="896d9-118">Click Post.</span></span>

## <a name="claim-the-fixed-asset-for-a-government-grant"></a><span data-ttu-id="896d9-119">固定資産の政府助成金の申請</span><span class="sxs-lookup"><span data-stu-id="896d9-119">Claim the fixed asset for a government grant</span></span>
1. <span data-ttu-id="896d9-120">[固定資産] > [仕訳入力] > [固定資産仕訳帳] の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="896d9-120">Go to Fixed assets > Journal entries > Fixed assets journal.</span></span>
2. <span data-ttu-id="896d9-121">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="896d9-121">Click New.</span></span>
3. <span data-ttu-id="896d9-122">[名前] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="896d9-122">In the Name field, type a value.</span></span>
4. <span data-ttu-id="896d9-123">[保存] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="896d9-123">Click Save.</span></span>
5. <span data-ttu-id="896d9-124">[明細行] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="896d9-124">Click Lines.</span></span>
6. <span data-ttu-id="896d9-125">[提案] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="896d9-125">Click Proposals.</span></span>
7. <span data-ttu-id="896d9-126">[圧縮記帳の提案] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="896d9-126">Click Reduction entry proposal.</span></span>
8. <span data-ttu-id="896d9-127">[フィルター] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="896d9-127">Click Filter.</span></span>
    * <span data-ttu-id="896d9-128">フィルタ処理により、固定資産のより速く検索できます。</span><span class="sxs-lookup"><span data-stu-id="896d9-128">You can filter to help find the fixed asset faster.</span></span>  
9. <span data-ttu-id="896d9-129">[基準] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="896d9-129">In the Criteria field, type a value.</span></span>
10. <span data-ttu-id="896d9-130">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="896d9-130">Click OK.</span></span>
11. <span data-ttu-id="896d9-131">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="896d9-131">Click OK.</span></span>
12. <span data-ttu-id="896d9-132">[日付] フィールドに日付を入力します。</span><span class="sxs-lookup"><span data-stu-id="896d9-132">In the Date field, enter a date.</span></span>
    * <span data-ttu-id="896d9-133">助成金を仕訳入力する会計日を入力します。</span><span class="sxs-lookup"><span data-stu-id="896d9-133">Enter the accounting date on which to journalize the subsidy.</span></span>  
13. <span data-ttu-id="896d9-134">[貸方] フィールドに数値を入力します。</span><span class="sxs-lookup"><span data-stu-id="896d9-134">In the Credit field, enter a number.</span></span>
    * <span data-ttu-id="896d9-135">政府助成金を入力します。</span><span class="sxs-lookup"><span data-stu-id="896d9-135">Enter the amount of the government grant.</span></span>  
14. <span data-ttu-id="896d9-136">[転記] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="896d9-136">Click Post.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]