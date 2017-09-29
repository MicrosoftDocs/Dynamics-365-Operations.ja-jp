--- 
title: "発注書の製品パッケージの作成"
description: "この手順では、製品パッケージを作成し、発注書を使用する方法を説明します。"
author: josaw1
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: a3be1e7aca7f0382aea55fa8a371c33c8b53df95
ms.contentlocale: ja-jp
ms.lasthandoff: 08/29/2017

---
# <a name="create-product-packages-for-purchase-orders"></a><span data-ttu-id="eb7c8-103">発注書の製品パッケージの作成</span><span class="sxs-lookup"><span data-stu-id="eb7c8-103">Create product packages for purchase orders</span></span>

[!include[task guide banner](../includes/task-guide-banner.md)]

<span data-ttu-id="eb7c8-104">この手順では、製品パッケージを作成し、発注書を使用する方法を説明します。</span><span class="sxs-lookup"><span data-stu-id="eb7c8-104">This procedure walks through creating a product package and using it on a purchase order.</span></span> <span data-ttu-id="eb7c8-105">発注書は、事前に定義された一連の製品の発注の作成に使用されます。</span><span class="sxs-lookup"><span data-stu-id="eb7c8-105">The purchase order will be used to create an order for a pre-defined set of products.</span></span> <span data-ttu-id="eb7c8-106">この手順では、デモ データの会社 USRT を使用します。</span><span class="sxs-lookup"><span data-stu-id="eb7c8-106">This procedure uses the USRT demo data company.</span></span>


## <a name="create-a-product-package"></a><span data-ttu-id="eb7c8-107">製品パッケージの作成</span><span class="sxs-lookup"><span data-stu-id="eb7c8-107">Create a product package</span></span>
1. <span data-ttu-id="eb7c8-108">[小売りとコマース] > [在庫管理] > [補充] > [製品パッケージ] に移動します。</span><span class="sxs-lookup"><span data-stu-id="eb7c8-108">Go to Retail and commerce > Inventory management > Replenishment > Product packages.</span></span>
2. <span data-ttu-id="eb7c8-109">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="eb7c8-109">Click New.</span></span>
3. <span data-ttu-id="eb7c8-110">[パッケージ番号] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="eb7c8-110">In the Package number field, type a value.</span></span>
4. <span data-ttu-id="eb7c8-111">[説明] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="eb7c8-111">In the Description field, type a value.</span></span>
5. <span data-ttu-id="eb7c8-112">[仕入先] フィールドで、ドロップ ダウン ボタンをクリックし、ルックアップを開きます。</span><span class="sxs-lookup"><span data-stu-id="eb7c8-112">In the Vendor account field, click the drop-down button to open the lookup.</span></span>
6. <span data-ttu-id="eb7c8-113">一覧で、選択された行のリンクをクリックします。</span><span class="sxs-lookup"><span data-stu-id="eb7c8-113">In the list, click the link in the selected row.</span></span>
7. <span data-ttu-id="eb7c8-114">[追加] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="eb7c8-114">Click Add.</span></span>
8. <span data-ttu-id="eb7c8-115">[品目番号] フィールドで「0160」と入力します。</span><span class="sxs-lookup"><span data-stu-id="eb7c8-115">In the Item number field, type '0160'.</span></span>
9. <span data-ttu-id="eb7c8-116">[サイズ] フィールドで、ドロップ ダウン ボタンをクリックし、ルックアップを開きます。</span><span class="sxs-lookup"><span data-stu-id="eb7c8-116">In the Size field, click the drop-down button to open the lookup.</span></span>
10. <span data-ttu-id="eb7c8-117">一覧で、選択された行のリンクをクリックします。</span><span class="sxs-lookup"><span data-stu-id="eb7c8-117">In the list, click the link in the selected row.</span></span>
11. <span data-ttu-id="eb7c8-118">[数量] フィールドに数値を入力します。</span><span class="sxs-lookup"><span data-stu-id="eb7c8-118">In the Quantity field, enter a number.</span></span>
12. <span data-ttu-id="eb7c8-119">[追加] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="eb7c8-119">Click Add.</span></span>
13. <span data-ttu-id="eb7c8-120">[品目番号] フィールドで「0160」と入力します。</span><span class="sxs-lookup"><span data-stu-id="eb7c8-120">In the Item number field, type '0160'.</span></span>
14. <span data-ttu-id="eb7c8-121">[バリアント番号] フィールドで、ドロップ ダウン ボタンをクリックし、ルックアップを開きます。</span><span class="sxs-lookup"><span data-stu-id="eb7c8-121">In the Variant number field, click the drop-down button to open the lookup.</span></span>
15. <span data-ttu-id="eb7c8-122">一覧で、選択された行のリンクをクリックします。</span><span class="sxs-lookup"><span data-stu-id="eb7c8-122">In the list, click the link in the selected row.</span></span>
16. <span data-ttu-id="eb7c8-123">[数量] フィールドに数値を入力します。</span><span class="sxs-lookup"><span data-stu-id="eb7c8-123">In the Quantity field, enter a number.</span></span>
17. <span data-ttu-id="eb7c8-124">[追加] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="eb7c8-124">Click Add.</span></span>
18. <span data-ttu-id="eb7c8-125">[品目番号] フィールドで「0175」と入力します。</span><span class="sxs-lookup"><span data-stu-id="eb7c8-125">In the Item number field, type '0175'.</span></span>
19. <span data-ttu-id="eb7c8-126">[数量] フィールドに数値を入力します。</span><span class="sxs-lookup"><span data-stu-id="eb7c8-126">In the Quantity field, enter a number.</span></span>
20. <span data-ttu-id="eb7c8-127">[保存] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="eb7c8-127">Click Save.</span></span>
21. <span data-ttu-id="eb7c8-128">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="eb7c8-128">Close the page.</span></span>

## <a name="add-package-to-puchase-order"></a><span data-ttu-id="eb7c8-129">発注書にパッケージを追加</span><span class="sxs-lookup"><span data-stu-id="eb7c8-129">Add package to puchase order</span></span>
1. <span data-ttu-id="eb7c8-130">[買掛金勘定] > [発注書] > [すべての発注書] に移動します。</span><span class="sxs-lookup"><span data-stu-id="eb7c8-130">Go to Accounts payable > Purchase orders > All purchase orders.</span></span>
2. <span data-ttu-id="eb7c8-131">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="eb7c8-131">Click New.</span></span>
3. <span data-ttu-id="eb7c8-132">[仕入先] フィールドで、ドロップ ダウン ボタンをクリックし、ルックアップを開きます。</span><span class="sxs-lookup"><span data-stu-id="eb7c8-132">In the Vendor account field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="eb7c8-133">リストで、仕入先が選択されている場合、製品パッケージが以前に作成された同じ仕入先を選択します。</span><span class="sxs-lookup"><span data-stu-id="eb7c8-133">In the list, select the same vendor that the product package was previously created for, if a vendor was selected.</span></span>
5. <span data-ttu-id="eb7c8-134">[一般] セクションの展開を切り替えます。</span><span class="sxs-lookup"><span data-stu-id="eb7c8-134">Toggle the expansion of the General section.</span></span>
6. <span data-ttu-id="eb7c8-135">[サイト] フィールドで、ドロップ ダウン ボタンをクリックし、ルックアップを開きます。</span><span class="sxs-lookup"><span data-stu-id="eb7c8-135">In the Site field, click the drop-down button to open the lookup.</span></span>
7. <span data-ttu-id="eb7c8-136">一覧で、選択された行のリンクをクリックします。</span><span class="sxs-lookup"><span data-stu-id="eb7c8-136">In the list, click the link in the selected row.</span></span>
8. <span data-ttu-id="eb7c8-137">[倉庫] フィールドで、ドロップ ダウン ボタンをクリックし、ルックアップを開きます。</span><span class="sxs-lookup"><span data-stu-id="eb7c8-137">In the Warehouse field, click the drop-down button to open the lookup.</span></span>
9. <span data-ttu-id="eb7c8-138">一覧で、選択された行のリンクをクリックします。</span><span class="sxs-lookup"><span data-stu-id="eb7c8-138">In the list, click the link in the selected row.</span></span>
10. <span data-ttu-id="eb7c8-139">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="eb7c8-139">Click OK.</span></span>
11. <span data-ttu-id="eb7c8-140">[明細行の詳細] セクションの展開を切り替えます。</span><span class="sxs-lookup"><span data-stu-id="eb7c8-140">Toggle the expansion of the Line details section.</span></span>
12. <span data-ttu-id="eb7c8-141">[製品パッケージ] タブをクリックします。</span><span class="sxs-lookup"><span data-stu-id="eb7c8-141">Click the Product packages tab.</span></span>
13. <span data-ttu-id="eb7c8-142">[購買注文明細行] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="eb7c8-142">Click Purchase order line.</span></span>
14. <span data-ttu-id="eb7c8-143">梱包から明細の作成をクリックします。</span><span class="sxs-lookup"><span data-stu-id="eb7c8-143">Click Create lines from package.</span></span>
15. <span data-ttu-id="eb7c8-144">リストで、前のステップで作成された製品パッケージを参照して選択します。</span><span class="sxs-lookup"><span data-stu-id="eb7c8-144">In the list, find and select the product package created in previous step.</span></span>
16. <span data-ttu-id="eb7c8-145">[数量] フィールドに数値を入力します。</span><span class="sxs-lookup"><span data-stu-id="eb7c8-145">In the Quantity field, enter a number.</span></span>
17. <span data-ttu-id="eb7c8-146">[作成] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="eb7c8-146">Click Create.</span></span>
18. <span data-ttu-id="eb7c8-147">[保存] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="eb7c8-147">Click Save.</span></span>


