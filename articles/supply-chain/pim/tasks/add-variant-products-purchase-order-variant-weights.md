--- 
title: "バリアント重量を使用した発注書へのバリアント製品の追加"
description: "この手順では、自動事前設定の購買注文明細行に製品のバリアントごとに異なる重量を使用するための手順を説明します。"
author: ShylaThompson
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
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: d9747ba144d56c9410846769e5465372c89ea111
ms.openlocfilehash: 446260a09bd5177877637ac8a288ad584dfa2b2b
ms.contentlocale: ja-jp
ms.lasthandoff: 08/07/2018

---
# <a name="add-variant-products-to-purchase-orders-using-variant-weights"></a><span data-ttu-id="2d899-103">バリアント重量を使用した発注書へのバリアント製品の追加</span><span class="sxs-lookup"><span data-stu-id="2d899-103">Add variant products to purchase orders using variant weights</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="2d899-104">この手順では、自動事前設定の購買注文明細行に製品のバリアントごとに異なる重量を使用するための手順を説明します。</span><span class="sxs-lookup"><span data-stu-id="2d899-104">This procedure walks through the steps for using variant weights to auto populate purchase order lines for each variant of a product.</span></span> <span data-ttu-id="2d899-105">自分が購買する製品の数量を選択すると、製品バリアントの重量コンフィギュレーションに基づく推奨数量のすべての製品のバリアントに、購買注文明細行が作成されます。</span><span class="sxs-lookup"><span data-stu-id="2d899-105">When you select the quantity of the product you want to purchase, purchase order lines are created for all the variants of the product with suggested quantities based on the weights configured on the product variants.</span></span> <span data-ttu-id="2d899-106">この手順には、製品分析コードおよび製品バリアントの重量の値をコンフィギュレーションするステップは含まれません。</span><span class="sxs-lookup"><span data-stu-id="2d899-106">This procedure doesn’t include steps to configure weight values on product dimensions and product variants.</span></span> <span data-ttu-id="2d899-107">この手順では、デモ データの会社 USRT を使用します。</span><span class="sxs-lookup"><span data-stu-id="2d899-107">This procedure uses the USRT company in demo data.</span></span>

1. <span data-ttu-id="2d899-108">[買掛金勘定] > [発注書] > [すべての発注書] に移動します。</span><span class="sxs-lookup"><span data-stu-id="2d899-108">Go to Accounts payable > Purchase orders > All purchase orders.</span></span>
2. <span data-ttu-id="2d899-109">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="2d899-109">Click New.</span></span>
3. <span data-ttu-id="2d899-110">[仕入先] フィールドで、ドロップ ダウン ボタンをクリックし、ルックアップを開きます。</span><span class="sxs-lookup"><span data-stu-id="2d899-110">In the Vendor account field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="2d899-111">一覧で、選択された行のリンクをクリックします。</span><span class="sxs-lookup"><span data-stu-id="2d899-111">In the list, click the link in the selected row.</span></span>
5. <span data-ttu-id="2d899-112">[一般] セクションの展開を切り替えます。</span><span class="sxs-lookup"><span data-stu-id="2d899-112">Toggle the expansion of the General section.</span></span>
6. <span data-ttu-id="2d899-113">[サイト] フィールドで、ドロップ ダウン ボタンをクリックし、ルックアップを開きます。</span><span class="sxs-lookup"><span data-stu-id="2d899-113">In the Site field, click the drop-down button to open the lookup.</span></span>
7. <span data-ttu-id="2d899-114">一覧で、選択された行のリンクをクリックします。</span><span class="sxs-lookup"><span data-stu-id="2d899-114">In the list, click the link in the selected row.</span></span>
8. <span data-ttu-id="2d899-115">[倉庫] フィールドで、ドロップ ダウン ボタンをクリックし、ルックアップを開きます。</span><span class="sxs-lookup"><span data-stu-id="2d899-115">In the Warehouse field, click the drop-down button to open the lookup.</span></span>
9. <span data-ttu-id="2d899-116">一覧で、目的のレコードを見つけ、選択します。</span><span class="sxs-lookup"><span data-stu-id="2d899-116">In the list, find and select the desired record.</span></span>
10. <span data-ttu-id="2d899-117">一覧で、選択された行のリンクをクリックします。</span><span class="sxs-lookup"><span data-stu-id="2d899-117">In the list, click the link in the selected row.</span></span>
11. <span data-ttu-id="2d899-118">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="2d899-118">Click OK.</span></span>
12. <span data-ttu-id="2d899-119">[明細行の詳細] セクションの展開を切り替えます。</span><span class="sxs-lookup"><span data-stu-id="2d899-119">Toggle the expansion of the Line details section.</span></span>
13. <span data-ttu-id="2d899-120">[バリアント] タブをクリックします。</span><span class="sxs-lookup"><span data-stu-id="2d899-120">Click the Variants tab.</span></span>
14. <span data-ttu-id="2d899-121">[行の追加] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="2d899-121">Click Add line.</span></span>
15. <span data-ttu-id="2d899-122">一覧で、選択された行をマークします。</span><span class="sxs-lookup"><span data-stu-id="2d899-122">In the list, mark the selected row.</span></span>
16. <span data-ttu-id="2d899-123">[品目番号] フィールドで「0140」と入力します。</span><span class="sxs-lookup"><span data-stu-id="2d899-123">In the Item number field, type '0140'.</span></span>
17. <span data-ttu-id="2d899-124">数量を '1000' に設定します。</span><span class="sxs-lookup"><span data-stu-id="2d899-124">Set Quantity to '1000'.</span></span>
18. <span data-ttu-id="2d899-125">[保存] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="2d899-125">Click Save.</span></span>


