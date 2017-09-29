--- 
title: "製品のバーコードの作成"
description: "この手順では、品目番号「M0001」を例として使用してバーコードを手動で作成する方法を示します。"
author: YuyuScheller
manager: AnnBe
ms.date: 09/26/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.author: yuyus
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: f53de983389dd8cbfb2c29af84539f1a73dc0a85
ms.contentlocale: ja-jp
ms.lasthandoff: 08/29/2017

---
# <a name="create-a-bar-code-for-a-product"></a><span data-ttu-id="8015f-103">製品のバーコードの作成</span><span class="sxs-lookup"><span data-stu-id="8015f-103">Create a bar code for a product</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="8015f-104">この手順では、品目番号「M0001」を例として使用してバーコードを手動で作成する方法を示します。</span><span class="sxs-lookup"><span data-stu-id="8015f-104">This procedure shows how to manually create a bar code using the item number M0001 as an example.</span></span> <span data-ttu-id="8015f-105">この手順の作成に使用するデモ データの会社は USMF です。</span><span class="sxs-lookup"><span data-stu-id="8015f-105">The demo data company used to create this procedure is USMF.</span></span>

1. <span data-ttu-id="8015f-106">[リリース済製品の保守] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="8015f-106">Click Released product maintenance.</span></span>
2. <span data-ttu-id="8015f-107">[リリース済製品] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="8015f-107">Click Released products.</span></span>
3. <span data-ttu-id="8015f-108">一覧で、目的のレコードを見つけ、選択します。</span><span class="sxs-lookup"><span data-stu-id="8015f-108">In the list, find and select the desired record.</span></span>
4. <span data-ttu-id="8015f-109">[アクション] ウィンドウで [在庫の管理] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="8015f-109">On the Action Pane, click Manage inventory.</span></span>
5. <span data-ttu-id="8015f-110">[バーコード] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="8015f-110">Click Bar codes.</span></span>
6. <span data-ttu-id="8015f-111">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="8015f-111">Click New.</span></span>
7. <span data-ttu-id="8015f-112">一覧で、選択された行をマークします。</span><span class="sxs-lookup"><span data-stu-id="8015f-112">In the list, mark the selected row.</span></span>
8. <span data-ttu-id="8015f-113">[バーコード設定] フィールドで値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="8015f-113">In the Barcode setup field, enter or select a value.</span></span>
9. <span data-ttu-id="8015f-114">[バーコード] フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="8015f-114">In the Bar code field, enter or select a value.</span></span>
10. <span data-ttu-id="8015f-115">[バーコード] フィールドに、値を入力します。</span><span class="sxs-lookup"><span data-stu-id="8015f-115">In the Bar code field, type a value.</span></span>
    * <span data-ttu-id="8015f-116">[タブ] キーを押します。</span><span class="sxs-lookup"><span data-stu-id="8015f-116">Press the Tab key.</span></span>  
11. <span data-ttu-id="8015f-117">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="8015f-117">Close the page.</span></span>
12. <span data-ttu-id="8015f-118">[数量] フィールドに数値を入力します。</span><span class="sxs-lookup"><span data-stu-id="8015f-118">In the Quantity field, enter a number.</span></span>
13. <span data-ttu-id="8015f-119">[保存] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="8015f-119">Click Save.</span></span>
    * <span data-ttu-id="8015f-120">[保存] をクリックすると、バーコード チェックが実行され、この場合、予測されるチェック ディジットは 8 ですが、3 が検出されたことを示すエラーが表示されます。</span><span class="sxs-lookup"><span data-stu-id="8015f-120">When you click Save, the barcode check is run, and in this case it will display an error stating that the expected check digit is 8, but that 3 was found.</span></span> <span data-ttu-id="8015f-121">8 が最後になるように手動でバーコード番号を更新します。</span><span class="sxs-lookup"><span data-stu-id="8015f-121">Manually update the barcode number so that 8 is at the end.</span></span>  
14. <span data-ttu-id="8015f-122">[バーコード] フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="8015f-122">In the Bar code field, enter or select a value.</span></span>
15. <span data-ttu-id="8015f-123">[バーコード] フィールドに、値を入力します。</span><span class="sxs-lookup"><span data-stu-id="8015f-123">In the Bar code field, type a value.</span></span>
    * <span data-ttu-id="8015f-124">[タブ] キーを押します。</span><span class="sxs-lookup"><span data-stu-id="8015f-124">Press the Tab key.</span></span>  
16. <span data-ttu-id="8015f-125">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="8015f-125">Close the page.</span></span>
17. <span data-ttu-id="8015f-126">[保存] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="8015f-126">Click Save.</span></span>
18. <span data-ttu-id="8015f-127">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="8015f-127">Close the page.</span></span>


