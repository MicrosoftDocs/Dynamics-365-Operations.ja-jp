--- 
title: "製品マスターの作成"
description: "事前に定義されたバリアントのために製品マスターを作成します。"
author: BibiSp
manager: AnnBe
ms.date: 11/11/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bis
ms.search.scope: Operations
ms.search.region: Global
ms.author: bis
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: 4e8d438da1524850c115f5c38865fac2f19f3ff5
ms.contentlocale: ja-jp
ms.lasthandoff: 08/29/2017

---
# <a name="create-a-product-master"></a><span data-ttu-id="16e9f-103">製品マスターの作成</span><span class="sxs-lookup"><span data-stu-id="16e9f-103">Create a product master</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="16e9f-104">事前に定義されたバリアントのために製品マスターを作成します。</span><span class="sxs-lookup"><span data-stu-id="16e9f-104">Create a product master for the predefined variants.</span></span> <span data-ttu-id="16e9f-105">この手順の作成に使用するデモ データの会社は USMF です。</span><span class="sxs-lookup"><span data-stu-id="16e9f-105">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="16e9f-106">この手順は、製品デザイナーを対象としています。</span><span class="sxs-lookup"><span data-stu-id="16e9f-106">This procedure is intended for the product designer.</span></span>


## <a name="create-a-new-product-master"></a><span data-ttu-id="16e9f-107">新しい製品マスターの作成</span><span class="sxs-lookup"><span data-stu-id="16e9f-107">Create a new product master</span></span>
1. <span data-ttu-id="16e9f-108">[製品情報管理] > [製品] > [製品マスター] の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="16e9f-108">Go to Product information management > Products > Product masters.</span></span>
2. <span data-ttu-id="16e9f-109">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="16e9f-109">Click New.</span></span>
3. <span data-ttu-id="16e9f-110">[製品番号] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="16e9f-110">In the Product number field, type a value.</span></span>
    * <span data-ttu-id="16e9f-111">番号は一意である必要があります。</span><span class="sxs-lookup"><span data-stu-id="16e9f-111">The number must be unique.</span></span> <span data-ttu-id="16e9f-112">[製品番号] フィールドに、番号順序を設定できます。</span><span class="sxs-lookup"><span data-stu-id="16e9f-112">A number sequence can be set for the Product number field.</span></span> <span data-ttu-id="16e9f-113">この場合、ユーザーは値を入力する必要はありません。</span><span class="sxs-lookup"><span data-stu-id="16e9f-113">In this case, the user doesn't have to enter a value.</span></span>  
4. <span data-ttu-id="16e9f-114">[製品名] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="16e9f-114">In the Product name field, type a value.</span></span>
    * <span data-ttu-id="16e9f-115">製品の内容を示す名前を入力します。</span><span class="sxs-lookup"><span data-stu-id="16e9f-115">Enter a descriptive product name.</span></span> <span data-ttu-id="16e9f-116">既定値は検索名になりますが、これはユーザーが変更できます。</span><span class="sxs-lookup"><span data-stu-id="16e9f-116">The value defaults to the search name, but this can be changed by the user.</span></span>  
5. <span data-ttu-id="16e9f-117">[製品分析コード グループ] フィールドで、ドロップ ダウン ボタンをクリックし、ルックアップを開きます。</span><span class="sxs-lookup"><span data-stu-id="16e9f-117">In the Product dimension group field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="16e9f-118">製品分析コード グループにより、製品バリアントを作成するために使用する 4 つの製品分析コードが決まります。</span><span class="sxs-lookup"><span data-stu-id="16e9f-118">The product dimension group determines which of the 4 product dimensions that can be used to create product variants.</span></span> <span data-ttu-id="16e9f-119">この例では、色とサイズのグループを使用します。</span><span class="sxs-lookup"><span data-stu-id="16e9f-119">This example uses a group with color and size.</span></span>  
6. <span data-ttu-id="16e9f-120">一覧で、目的のレコードを見つけ、選択します。</span><span class="sxs-lookup"><span data-stu-id="16e9f-120">In the list, find and select the desired record.</span></span>
7. <span data-ttu-id="16e9f-121">一覧で、選択された行のリンクをクリックします。</span><span class="sxs-lookup"><span data-stu-id="16e9f-121">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="16e9f-122">既定のコンフィギュレーション テクノロジは、事前に定義されたバリアントです。</span><span class="sxs-lookup"><span data-stu-id="16e9f-122">The default configuration technology is Predefined variant.</span></span> <span data-ttu-id="16e9f-123">これは、この例に使用されます。</span><span class="sxs-lookup"><span data-stu-id="16e9f-123">This will be used for this example.</span></span>  
8. <span data-ttu-id="16e9f-124">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="16e9f-124">Click OK.</span></span>

## <a name="select-product-dimension-groups"></a><span data-ttu-id="16e9f-125">製品分析コード グループの選択</span><span class="sxs-lookup"><span data-stu-id="16e9f-125">Select product dimension groups</span></span>
1. <span data-ttu-id="16e9f-126">[色グループ] フィールドで、ドロップ ダウン ボタンをクリックし、ルックアップを開きます。</span><span class="sxs-lookup"><span data-stu-id="16e9f-126">In the Color group field, click the drop-down button to open the lookup.</span></span>
2. <span data-ttu-id="16e9f-127">一覧で、目的のレコードを見つけ、選択します。</span><span class="sxs-lookup"><span data-stu-id="16e9f-127">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="16e9f-128">一覧で、選択された行のリンクをクリックします。</span><span class="sxs-lookup"><span data-stu-id="16e9f-128">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="16e9f-129">[サイズ グループ] フィールドで、ドロップ ダウン ボタンをクリックし、ルックアップを開きます。</span><span class="sxs-lookup"><span data-stu-id="16e9f-129">In the Size group field, click the drop-down button to open the lookup.</span></span>
5. <span data-ttu-id="16e9f-130">一覧で、目的のレコードを見つけ、選択します。</span><span class="sxs-lookup"><span data-stu-id="16e9f-130">In the list, find and select the desired record.</span></span>
6. <span data-ttu-id="16e9f-131">一覧で、選択された行のリンクをクリックします。</span><span class="sxs-lookup"><span data-stu-id="16e9f-131">In the list, click the link in the selected row.</span></span>

## <a name="add-dimension-groups"></a><span data-ttu-id="16e9f-132">分析コード グループの追加</span><span class="sxs-lookup"><span data-stu-id="16e9f-132">Add dimension groups</span></span>
1. <span data-ttu-id="16e9f-133">アクション ウィンドウで、[製品] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="16e9f-133">On the Action Pane, click Product.</span></span>
2. <span data-ttu-id="16e9f-134">[分析コード グループ] をクリックすると、ドロップ ダイアログが開きます。</span><span class="sxs-lookup"><span data-stu-id="16e9f-134">Click Dimension groups to open the drop dialog.</span></span>
3. <span data-ttu-id="16e9f-135">[保管分析コード グループ] フィールドで、ドロップ ダウン ボタンをクリックし、ルックアップを開きます。</span><span class="sxs-lookup"><span data-stu-id="16e9f-135">In the Storage dimension group field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="16e9f-136">保管分析コードは、品目の保管方法と在庫からの取得方法を管理できます。</span><span class="sxs-lookup"><span data-stu-id="16e9f-136">The storage dimensions help you control how items are stored and taken from inventory.</span></span> <span data-ttu-id="16e9f-137">たとえば、保管分析コードにはサイトと倉庫を含めることができます。</span><span class="sxs-lookup"><span data-stu-id="16e9f-137">For example, a storage dimension can include Site and Warehouse.</span></span>  
4. <span data-ttu-id="16e9f-138">一覧で、目的のレコードを見つけ、選択します。</span><span class="sxs-lookup"><span data-stu-id="16e9f-138">In the list, find and select the desired record.</span></span>
5. <span data-ttu-id="16e9f-139">一覧で、選択された行のリンクをクリックします。</span><span class="sxs-lookup"><span data-stu-id="16e9f-139">In the list, click the link in the selected row.</span></span>
6. <span data-ttu-id="16e9f-140">[追跡用分析コード グループ] フィールドで、ドロップ ダウン ボタンをクリックし、ルックアップを開きます。</span><span class="sxs-lookup"><span data-stu-id="16e9f-140">In the Tracking dimension group field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="16e9f-141">追跡用分析コード グループにより、製品に追加できる追跡用分析コードが決まります。</span><span class="sxs-lookup"><span data-stu-id="16e9f-141">The tracking dimension group determines which tracking dimensions you can add to a product.</span></span> <span data-ttu-id="16e9f-142">たとえば、バッチ番号とシリアル番号は、在庫品目を追跡するために使用します。</span><span class="sxs-lookup"><span data-stu-id="16e9f-142">For example, the batch number and serial number are used to track inventory items.</span></span>  
7. <span data-ttu-id="16e9f-143">一覧で、目的のレコードを見つけ、選択します。</span><span class="sxs-lookup"><span data-stu-id="16e9f-143">In the list, find and select the desired record.</span></span>
8. <span data-ttu-id="16e9f-144">一覧で、選択された行のリンクをクリックします。</span><span class="sxs-lookup"><span data-stu-id="16e9f-144">In the list, click the link in the selected row.</span></span>
9. <span data-ttu-id="16e9f-145">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="16e9f-145">Click OK.</span></span>
10. <span data-ttu-id="16e9f-146">[保存] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="16e9f-146">Click Save.</span></span>
11. <span data-ttu-id="16e9f-147">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="16e9f-147">Close the page.</span></span>


