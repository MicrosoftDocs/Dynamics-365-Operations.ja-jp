--- 
title: "発注書の作成時に購買リリース注文を作成"
description: "この手順では、発注書を作成するときに購買契約書を使用する方法を示します。"
author: mkirknel
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bis
ms.search.scope: Operations
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: 194d811da09c746167bd9489ce39ae6a6f810ec0
ms.contentlocale: ja-jp
ms.lasthandoff: 08/29/2017

---
# <a name="create-a-purchase-release-order-when-creating-the-purchase-order"></a><span data-ttu-id="cef7b-103">発注書の作成時に購買リリース注文を作成</span><span class="sxs-lookup"><span data-stu-id="cef7b-103">Create a purchase release order when creating the purchase order</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="cef7b-104">この手順では、発注書を作成するときに購買契約書を使用する方法を示します。</span><span class="sxs-lookup"><span data-stu-id="cef7b-104">This procedure shows how to use a purchase agreement when you create a purchase order.</span></span> <span data-ttu-id="cef7b-105">発注書ヘッダーには一般的な条件をコピーする必要があるので、発注書を作成するときに購買契約書を適用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="cef7b-105">The purchase agreement has to be applied when you create the purchase order because there are general terms that should be copied to the purchase order header.</span></span> <span data-ttu-id="cef7b-106">通常、これらのタスクを実施するのは、購買担当者です。</span><span class="sxs-lookup"><span data-stu-id="cef7b-106">Typically this task would be carried out by a purchasing agent.</span></span> <span data-ttu-id="cef7b-107">このガイドの前提条件として、仕入先および品目の製品数量が確約された有効購買契約書が必要です。</span><span class="sxs-lookup"><span data-stu-id="cef7b-107">As a prerequisite for this guide, you must have an effective purchase agreement with a product quantity commitment for a vendor and items.</span></span> <span data-ttu-id="cef7b-108">同じ手順は、他のタイプの確約のある購買契約書が存在する場合に使用できます。</span><span class="sxs-lookup"><span data-stu-id="cef7b-108">The same procedure can be used if you have a purchase agreement with other types of commitments.</span></span> <span data-ttu-id="cef7b-109">デモ データの会社 USMF でこのガイドを実行できます。</span><span class="sxs-lookup"><span data-stu-id="cef7b-109">You can run this guide in demo data company USMF.</span></span> <span data-ttu-id="cef7b-110">USMF を使用する場合、最初に「購買契約の作成」ガイドを実行して、このガイドに必要な前提条件を設定することができます。</span><span class="sxs-lookup"><span data-stu-id="cef7b-110">If you’re using USMF, you can run the “Create a purchase agreement” guide first to set up the necessary preconditions for this guide.</span></span>


## <a name="create-a-purchase-order"></a><span data-ttu-id="cef7b-111">発注書の作成</span><span class="sxs-lookup"><span data-stu-id="cef7b-111">Create a purchase order</span></span>
1. <span data-ttu-id="cef7b-112">発注書準備ワークスペースを開きます。</span><span class="sxs-lookup"><span data-stu-id="cef7b-112">Open the purchase order preparation workspace.</span></span>
2. <span data-ttu-id="cef7b-113">[新しい発注書] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="cef7b-113">Click New purchase order.</span></span>
3. <span data-ttu-id="cef7b-114">[仕入先] フィールドで、ドロップ ダウン ボタンをクリックし、ルックアップを開きます。</span><span class="sxs-lookup"><span data-stu-id="cef7b-114">In the Vendor account field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="cef7b-115">一覧で、目的のレコードを見つけ、選択します。</span><span class="sxs-lookup"><span data-stu-id="cef7b-115">In the list, find and select the desired record.</span></span>
5. <span data-ttu-id="cef7b-116">一覧で、選択された行のリンクをクリックします。</span><span class="sxs-lookup"><span data-stu-id="cef7b-116">In the list, click the link in the selected row.</span></span>
6. <span data-ttu-id="cef7b-117">[一般] セクションの展開を切り替えます。</span><span class="sxs-lookup"><span data-stu-id="cef7b-117">Toggle the expansion of the General section.</span></span>
7. <span data-ttu-id="cef7b-118">[購買契約] フィールドで、ドロップ ダウン ボタンをクリックし、ルックアップを開きます。</span><span class="sxs-lookup"><span data-stu-id="cef7b-118">In the Purchase agreement field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="cef7b-119">利用可能な仕入先とのすべての契約がここに表示されます。</span><span class="sxs-lookup"><span data-stu-id="cef7b-119">All available agreements for the vendor are listed here.</span></span> <span data-ttu-id="cef7b-120">使用する有効な契約を検索します。</span><span class="sxs-lookup"><span data-stu-id="cef7b-120">Find the effective agreement that you want to use.</span></span>  
8. <span data-ttu-id="cef7b-121">一覧で、選択された行のリンクをクリックします。</span><span class="sxs-lookup"><span data-stu-id="cef7b-121">In the list, click the link in the selected row.</span></span>
9. <span data-ttu-id="cef7b-122">[はい] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="cef7b-122">Click Yes.</span></span>
10. <span data-ttu-id="cef7b-123">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="cef7b-123">Click OK.</span></span>

## <a name="add-a-line"></a><span data-ttu-id="cef7b-124">明細行の追加</span><span class="sxs-lookup"><span data-stu-id="cef7b-124">Add a line</span></span>
1. <span data-ttu-id="cef7b-125">[品目番号] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="cef7b-125">In the Item number field, type a value.</span></span>
    * <span data-ttu-id="cef7b-126">確約に特定の在庫または場所分析コードがある場合、契約を使用する購買注文明細行に同じ値を入力する必要があります。</span><span class="sxs-lookup"><span data-stu-id="cef7b-126">If there are specific inventory or location dimensions on the commitment you must enter the same values on the purchase order line to make use of the agreement.</span></span>  
2. <span data-ttu-id="cef7b-127">[サイト] フィールドで、ドロップ ダウン ボタンをクリックし、ルックアップを開きます。</span><span class="sxs-lookup"><span data-stu-id="cef7b-127">In the Site field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="cef7b-128">サイトは、注文または仕入先の既定値から、既に設定されいる場合があります。</span><span class="sxs-lookup"><span data-stu-id="cef7b-128">The site may already be populated with the default value from the order, or from the vendor.</span></span> <span data-ttu-id="cef7b-129">その場合、この手順を省略します。</span><span class="sxs-lookup"><span data-stu-id="cef7b-129">If this is the case, skip this step.</span></span>  
3. <span data-ttu-id="cef7b-130">一覧で、目的のレコードを見つけ、選択します。</span><span class="sxs-lookup"><span data-stu-id="cef7b-130">In the list, find and select the desired record.</span></span>
4. <span data-ttu-id="cef7b-131">一覧で、選択された行のリンクをクリックします。</span><span class="sxs-lookup"><span data-stu-id="cef7b-131">In the list, click the link in the selected row.</span></span>
5. <span data-ttu-id="cef7b-132">[数量] フィールドに数値を入力します。</span><span class="sxs-lookup"><span data-stu-id="cef7b-132">In the Quantity field, enter a number.</span></span>
    * <span data-ttu-id="cef7b-133">価格が確約からコピーされたことを確認します。</span><span class="sxs-lookup"><span data-stu-id="cef7b-133">Validate that the price is copied from the commitment.</span></span>  

## <a name="look-up-the-commitment"></a><span data-ttu-id="cef7b-134">確約の検索</span><span class="sxs-lookup"><span data-stu-id="cef7b-134">Look up the commitment</span></span>
1. <span data-ttu-id="cef7b-135">[明細行の更新] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="cef7b-135">Click Update line.</span></span>
2. <span data-ttu-id="cef7b-136">[添付済] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="cef7b-136">Click Attached.</span></span>
    * <span data-ttu-id="cef7b-137">ここで購買契約書の詳細を取得できます。</span><span class="sxs-lookup"><span data-stu-id="cef7b-137">Here you can get details for the purchase agreement.</span></span> <span data-ttu-id="cef7b-138">たとえば、価格の確認や、価格や割引が変更されたものであるかの確認ができます。これはつまり、発注書の価格や割引を確約と異なる値に変更した場合に、システムはリンクを削除して購買注文明細行が確約を満たさないものとします。</span><span class="sxs-lookup"><span data-stu-id="cef7b-138">For example, you can see the price and whether the price and discount are fixed, which means that if you change price or discount on the purchase order to a different value than on the commitment, the system will remove the link so the purchase order line does not fulfill the commitment.</span></span> <span data-ttu-id="cef7b-139">また、[最大値の適用] オプションが選択されていることを確認できます。これは、確約の数量が、確約を履行するすべての購買の合計を超えることができないことを意味します。</span><span class="sxs-lookup"><span data-stu-id="cef7b-139">You can also see if the Max is enforced option is selected, which means that the quantity on the commitment cannot be exceeded by summing all of the purchases that fulfill the commitment.</span></span>  
3. <span data-ttu-id="cef7b-140">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="cef7b-140">Close the page.</span></span>

## <a name="look-up-the-purchase-agreement"></a><span data-ttu-id="cef7b-141">購買契約書の検索</span><span class="sxs-lookup"><span data-stu-id="cef7b-141">Look up the purchase agreement</span></span>
1. <span data-ttu-id="cef7b-142">アクション ウィンドウで、[一般] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="cef7b-142">On the Action Pane, click General.</span></span>
2. <span data-ttu-id="cef7b-143">[購買契約書] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="cef7b-143">Click Purchase agreement.</span></span>
3. <span data-ttu-id="cef7b-144">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="cef7b-144">Close the page.</span></span>
4. <span data-ttu-id="cef7b-145">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="cef7b-145">Close the page.</span></span>


