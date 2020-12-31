---
title: 資産除去債務見積の調整
description: 日本では、資産除去責務 (ARO) の最初の見積を調整できます。
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AssetTable, AssetRetirementObligation_JP, AssetRetirementObligationLine_JP, LedgerJournalTable, LedgerJournalTransAsset, SysQueryForm
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Japan
ms.author: roschlom
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: d2799435590fdf8b12130df9785183444e4f79fb
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/13/2020
ms.locfileid: "4408154"
---
# <a name="adjustment-of-the-asset-retirement-obligation-estimate"></a><span data-ttu-id="e5fb7-103">資産除去債務見積の調整</span><span class="sxs-lookup"><span data-stu-id="e5fb7-103">Adjustment of the asset retirement obligation estimate</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="e5fb7-104">日本では、資産除去責務 (ARO) の最初の見積を調整できます。</span><span class="sxs-lookup"><span data-stu-id="e5fb7-104">For Japan, the initial estimate of the asset retirement obligations (ARO) can be adjusted.</span></span> 



<span data-ttu-id="e5fb7-105">この手順を使用して、ARO 金額を調整する方法を説明します。</span><span class="sxs-lookup"><span data-stu-id="e5fb7-105">Use this procedure to learn how to adjust the ARO amount.</span></span>



<span data-ttu-id="e5fb7-106">この手順を完了するためには、[固定資産コンフィギュレーション キー] を選択する必要があります。</span><span class="sxs-lookup"><span data-stu-id="e5fb7-106">To complete this procedure, the Fixed Assets configuration key must be selected.</span></span>



<span data-ttu-id="e5fb7-107">このタスクは デモ データ会社 JPMF を使用して作成されました。</span><span class="sxs-lookup"><span data-stu-id="e5fb7-107">This task was created using the demo data company JPMF.</span></span>


## <a name="adjust-the-aro-estimate"></a><span data-ttu-id="e5fb7-108">ARO 見積の調整</span><span class="sxs-lookup"><span data-stu-id="e5fb7-108">Adjust the ARO estimate</span></span>
1. <span data-ttu-id="e5fb7-109">[固定資産] > [資産除去責務] > [固定資産] に移動します。</span><span class="sxs-lookup"><span data-stu-id="e5fb7-109">Go to Fixed assets > Asset retirement obligations > Fixed assets.</span></span>
2. <span data-ttu-id="e5fb7-110">一覧で、目的のレコードを見つけ、選択します。</span><span class="sxs-lookup"><span data-stu-id="e5fb7-110">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="e5fb7-111">[アクション] ウィンドウで、[固定資産] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="e5fb7-111">On the Action Pane, click Fixed asset.</span></span>
4. <span data-ttu-id="e5fb7-112">[資産除去責務] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="e5fb7-112">Click Asset retirement obligation.</span></span>
5. <span data-ttu-id="e5fb7-113">[切り上げ] をクリックしてドロップ ダイアログを開きます。</span><span class="sxs-lookup"><span data-stu-id="e5fb7-113">Click Upward to open the drop dialog.</span></span>
    * <span data-ttu-id="e5fb7-114">[切り捨て] をクリックしてマイナス調整することもできます。</span><span class="sxs-lookup"><span data-stu-id="e5fb7-114">You can also click Downward for minus adjustment.</span></span>  
6. <span data-ttu-id="e5fb7-115">[トランザクション日付] フィールドで、調整金額を転記する日付を入力します。</span><span class="sxs-lookup"><span data-stu-id="e5fb7-115">In the Transaction date field, enter the date on which to post the adjustment amount.</span></span>
7. <span data-ttu-id="e5fb7-116">[切り上げ] フィールドに調整金額を入力します。</span><span class="sxs-lookup"><span data-stu-id="e5fb7-116">In the Upward field, enter the amount of adjustment.</span></span>
8. <span data-ttu-id="e5fb7-117">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="e5fb7-117">Click OK.</span></span>

## <a name="post-the-adjustment"></a><span data-ttu-id="e5fb7-118">調整の転記</span><span class="sxs-lookup"><span data-stu-id="e5fb7-118">Post the adjustment</span></span>
1. <span data-ttu-id="e5fb7-119">[固定資産] > [資産除去責務] > [固定資産仕訳帳] の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="e5fb7-119">Go to Fixed assets > Asset retirement obligations > Fixed assets journal.</span></span>
2. <span data-ttu-id="e5fb7-120">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="e5fb7-120">Click New.</span></span>
3. <span data-ttu-id="e5fb7-121">[名前] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="e5fb7-121">In the Name field, type a value.</span></span>
4. <span data-ttu-id="e5fb7-122">[保存] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="e5fb7-122">Click Save.</span></span>
5. <span data-ttu-id="e5fb7-123">[明細行] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="e5fb7-123">Click Lines.</span></span>
6. <span data-ttu-id="e5fb7-124">[提案] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="e5fb7-124">Click Proposals.</span></span>
7. <span data-ttu-id="e5fb7-125">[除去費用の資産計上] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="e5fb7-125">Click Capitalized asset retirement obligation.</span></span>
8. <span data-ttu-id="e5fb7-126">[終了日] フィールドで、日付を入力します。</span><span class="sxs-lookup"><span data-stu-id="e5fb7-126">In the To date field, enter a date.</span></span>
9. <span data-ttu-id="e5fb7-127">[フィルター] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="e5fb7-127">Click Filter.</span></span>
10. <span data-ttu-id="e5fb7-128">[基準] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="e5fb7-128">In the Criteria field, type a value.</span></span>
11. <span data-ttu-id="e5fb7-129">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="e5fb7-129">Click OK.</span></span>
12. <span data-ttu-id="e5fb7-130">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="e5fb7-130">Click OK.</span></span>
    * <span data-ttu-id="e5fb7-131">調整が提案されていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="e5fb7-131">Confirm the adjustment is proposed.</span></span> <span data-ttu-id="e5fb7-132">提案された金額は現在の値に割引されます。</span><span class="sxs-lookup"><span data-stu-id="e5fb7-132">The amount proposed is discounted to the present value.</span></span>  
13. <span data-ttu-id="e5fb7-133">[転記] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="e5fb7-133">Click Post.</span></span>

