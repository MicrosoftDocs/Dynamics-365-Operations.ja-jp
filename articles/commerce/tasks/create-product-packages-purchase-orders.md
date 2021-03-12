---
title: 発注書の製品パッケージの作成
description: この手順では、製品パッケージを作成し、発注書を使用する方法を説明します。
author: josaw1
manager: AnnBe
ms.date: 11/14/2017
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.region: Global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 296b3fb03b20dee5b6024c182df7feb3ce280913
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/15/2021
ms.locfileid: "4964673"
---
# <a name="create-product-packages-for-purchase-orders"></a><span data-ttu-id="fbd0c-103">発注書の製品パッケージの作成</span><span class="sxs-lookup"><span data-stu-id="fbd0c-103">Create product packages for purchase orders</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="fbd0c-104">この手順では、製品パッケージを作成し、発注書を使用する方法を説明します。</span><span class="sxs-lookup"><span data-stu-id="fbd0c-104">This procedure walks through creating a product package and using it on a purchase order.</span></span> <span data-ttu-id="fbd0c-105">発注書は、事前に定義された一連の製品の発注の作成に使用されます。</span><span class="sxs-lookup"><span data-stu-id="fbd0c-105">The purchase order will be used to create an order for a pre-defined set of products.</span></span> <span data-ttu-id="fbd0c-106">この手順では、デモ データの会社 USRT を使用します。</span><span class="sxs-lookup"><span data-stu-id="fbd0c-106">This procedure uses the USRT demo data company.</span></span>


## <a name="create-a-product-package"></a><span data-ttu-id="fbd0c-107">製品パッケージの作成</span><span class="sxs-lookup"><span data-stu-id="fbd0c-107">Create a product package</span></span>
1. <span data-ttu-id="fbd0c-108">Retail と Commerce > 在庫管理 > 補充 > 製品パッケージに移動します。</span><span class="sxs-lookup"><span data-stu-id="fbd0c-108">Go to Retail and Commerce > Inventory management > Replenishment > Product packages.</span></span>
2. <span data-ttu-id="fbd0c-109">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="fbd0c-109">Click New.</span></span>
3. <span data-ttu-id="fbd0c-110">[パッケージ番号] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="fbd0c-110">In the Package number field, type a value.</span></span>
4. <span data-ttu-id="fbd0c-111">[説明] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="fbd0c-111">In the Description field, type a value.</span></span>
5. <span data-ttu-id="fbd0c-112">[仕入先] フィールドで、ドロップ ダウン ボタンをクリックし、ルックアップを開きます。</span><span class="sxs-lookup"><span data-stu-id="fbd0c-112">In the Vendor account field, click the drop-down button to open the lookup.</span></span>
6. <span data-ttu-id="fbd0c-113">一覧で、選択された行のリンクをクリックします。</span><span class="sxs-lookup"><span data-stu-id="fbd0c-113">In the list, click the link in the selected row.</span></span>
7. <span data-ttu-id="fbd0c-114">[追加] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="fbd0c-114">Click Add.</span></span>
8. <span data-ttu-id="fbd0c-115">[品目番号] フィールドで「0160」と入力します。</span><span class="sxs-lookup"><span data-stu-id="fbd0c-115">In the Item number field, type '0160'.</span></span>
9. <span data-ttu-id="fbd0c-116">[サイズ] フィールドで、ドロップ ダウン ボタンをクリックし、ルックアップを開きます。</span><span class="sxs-lookup"><span data-stu-id="fbd0c-116">In the Size field, click the drop-down button to open the lookup.</span></span>
10. <span data-ttu-id="fbd0c-117">一覧で、選択された行のリンクをクリックします。</span><span class="sxs-lookup"><span data-stu-id="fbd0c-117">In the list, click the link in the selected row.</span></span>
11. <span data-ttu-id="fbd0c-118">[数量] フィールドに数値を入力します。</span><span class="sxs-lookup"><span data-stu-id="fbd0c-118">In the Quantity field, enter a number.</span></span>
12. <span data-ttu-id="fbd0c-119">[追加] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="fbd0c-119">Click Add.</span></span>
13. <span data-ttu-id="fbd0c-120">[品目番号] フィールドで「0160」と入力します。</span><span class="sxs-lookup"><span data-stu-id="fbd0c-120">In the Item number field, type '0160'.</span></span>
14. <span data-ttu-id="fbd0c-121">[バリアント番号] フィールドで、ドロップ ダウン ボタンをクリックし、ルックアップを開きます。</span><span class="sxs-lookup"><span data-stu-id="fbd0c-121">In the Variant number field, click the drop-down button to open the lookup.</span></span>
15. <span data-ttu-id="fbd0c-122">一覧で、選択された行のリンクをクリックします。</span><span class="sxs-lookup"><span data-stu-id="fbd0c-122">In the list, click the link in the selected row.</span></span>
16. <span data-ttu-id="fbd0c-123">[数量] フィールドに数値を入力します。</span><span class="sxs-lookup"><span data-stu-id="fbd0c-123">In the Quantity field, enter a number.</span></span>
17. <span data-ttu-id="fbd0c-124">[追加] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="fbd0c-124">Click Add.</span></span>
18. <span data-ttu-id="fbd0c-125">[品目番号] フィールドで「0175」と入力します。</span><span class="sxs-lookup"><span data-stu-id="fbd0c-125">In the Item number field, type '0175'.</span></span>
19. <span data-ttu-id="fbd0c-126">[数量] フィールドに数値を入力します。</span><span class="sxs-lookup"><span data-stu-id="fbd0c-126">In the Quantity field, enter a number.</span></span>
20. <span data-ttu-id="fbd0c-127">[保存] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="fbd0c-127">Click Save.</span></span>
21. <span data-ttu-id="fbd0c-128">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="fbd0c-128">Close the page.</span></span>

## <a name="add-package-to-purchase-order"></a><span data-ttu-id="fbd0c-129">発注書にパッケージを追加</span><span class="sxs-lookup"><span data-stu-id="fbd0c-129">Add package to purchase order</span></span>
1. <span data-ttu-id="fbd0c-130">[買掛金勘定] > [発注書] > [すべての発注書] に移動します。</span><span class="sxs-lookup"><span data-stu-id="fbd0c-130">Go to Accounts payable > Purchase orders > All purchase orders.</span></span>
2. <span data-ttu-id="fbd0c-131">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="fbd0c-131">Click New.</span></span>
3. <span data-ttu-id="fbd0c-132">[仕入先] フィールドで、ドロップ ダウン ボタンをクリックし、ルックアップを開きます。</span><span class="sxs-lookup"><span data-stu-id="fbd0c-132">In the Vendor account field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="fbd0c-133">リストで、仕入先が選択されている場合、製品パッケージが以前に作成された同じ仕入先を選択します。</span><span class="sxs-lookup"><span data-stu-id="fbd0c-133">In the list, select the same vendor that the product package was previously created for, if a vendor was selected.</span></span>
5. <span data-ttu-id="fbd0c-134">[一般] セクションの展開を切り替えます。</span><span class="sxs-lookup"><span data-stu-id="fbd0c-134">Toggle the expansion of the General section.</span></span>
6. <span data-ttu-id="fbd0c-135">[サイト] フィールドで、ドロップ ダウン ボタンをクリックし、ルックアップを開きます。</span><span class="sxs-lookup"><span data-stu-id="fbd0c-135">In the Site field, click the drop-down button to open the lookup.</span></span>
7. <span data-ttu-id="fbd0c-136">一覧で、選択された行のリンクをクリックします。</span><span class="sxs-lookup"><span data-stu-id="fbd0c-136">In the list, click the link in the selected row.</span></span>
8. <span data-ttu-id="fbd0c-137">[倉庫] フィールドで、ドロップ ダウン ボタンをクリックし、ルックアップを開きます。</span><span class="sxs-lookup"><span data-stu-id="fbd0c-137">In the Warehouse field, click the drop-down button to open the lookup.</span></span>
9. <span data-ttu-id="fbd0c-138">一覧で、選択された行のリンクをクリックします。</span><span class="sxs-lookup"><span data-stu-id="fbd0c-138">In the list, click the link in the selected row.</span></span>
10. <span data-ttu-id="fbd0c-139">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="fbd0c-139">Click OK.</span></span>
11. <span data-ttu-id="fbd0c-140">[明細行の詳細] セクションの展開を切り替えます。</span><span class="sxs-lookup"><span data-stu-id="fbd0c-140">Toggle the expansion of the Line details section.</span></span>
12. <span data-ttu-id="fbd0c-141">[製品パッケージ] タブをクリックします。</span><span class="sxs-lookup"><span data-stu-id="fbd0c-141">Click the Product packages tab.</span></span>
13. <span data-ttu-id="fbd0c-142">[購買注文明細行] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="fbd0c-142">Click Purchase order line.</span></span>
14. <span data-ttu-id="fbd0c-143">梱包から明細の作成をクリックします。</span><span class="sxs-lookup"><span data-stu-id="fbd0c-143">Click Create lines from package.</span></span>
15. <span data-ttu-id="fbd0c-144">リストで、前のステップで作成された製品パッケージを参照して選択します。</span><span class="sxs-lookup"><span data-stu-id="fbd0c-144">In the list, find and select the product package created in previous step.</span></span>
16. <span data-ttu-id="fbd0c-145">[数量] フィールドに数値を入力します。</span><span class="sxs-lookup"><span data-stu-id="fbd0c-145">In the Quantity field, enter a number.</span></span>
17. <span data-ttu-id="fbd0c-146">[作成] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="fbd0c-146">Click Create.</span></span>
18. <span data-ttu-id="fbd0c-147">[保存] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="fbd0c-147">Click Save.</span></span>

