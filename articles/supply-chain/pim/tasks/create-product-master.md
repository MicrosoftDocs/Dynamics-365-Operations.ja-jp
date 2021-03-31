---
title: 製品マスターの作成
description: 事前に定義されたバリアントのために製品マスターを作成します。
author: ShylaThompson
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EcoResProductListPage, EcoResProductCreate, EcoResProductDetails, EcoResProductInventoryDimensionGroups
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: d580d323409d84bab66dc03d39e084f5ee0cfc64
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/15/2021
ms.locfileid: "5218492"
---
# <a name="create-a-product-master"></a><span data-ttu-id="ae1c4-103">製品マスターの作成</span><span class="sxs-lookup"><span data-stu-id="ae1c4-103">Create a product master</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="ae1c4-104">事前に定義されたバリアントのために製品マスターを作成します。</span><span class="sxs-lookup"><span data-stu-id="ae1c4-104">Create a product master for the predefined variants.</span></span> <span data-ttu-id="ae1c4-105">この手順の作成に使用するデモ データの会社は USMF です。</span><span class="sxs-lookup"><span data-stu-id="ae1c4-105">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="ae1c4-106">この手順は、製品デザイナーを対象としています。</span><span class="sxs-lookup"><span data-stu-id="ae1c4-106">This procedure is intended for the product designer.</span></span>


## <a name="create-a-new-product-master"></a><span data-ttu-id="ae1c4-107">新しい製品マスターの作成</span><span class="sxs-lookup"><span data-stu-id="ae1c4-107">Create a new product master</span></span>
1. <span data-ttu-id="ae1c4-108">**ナビゲーション ウィンドウ > モジュール > 製品情報管理 > 製品 > 製品マスター** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="ae1c4-108">Go to **Navigation pane > Modules > Product information management > Products > Product masters**.</span></span>
2. <span data-ttu-id="ae1c4-109">**新規** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="ae1c4-109">Click **New**.</span></span>
3. <span data-ttu-id="ae1c4-110">**製品番号** フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="ae1c4-110">In the **Product number** field, type a value.</span></span> <span data-ttu-id="ae1c4-111">番号は一意である必要があります。</span><span class="sxs-lookup"><span data-stu-id="ae1c4-111">The number must be unique.</span></span> <span data-ttu-id="ae1c4-112">**製品番号** フィールドに、番号順序を設定できます。</span><span class="sxs-lookup"><span data-stu-id="ae1c4-112">A number sequence can be set for the **Product number** field.</span></span> <span data-ttu-id="ae1c4-113">この場合、ユーザーは値を入力する必要はありません。</span><span class="sxs-lookup"><span data-stu-id="ae1c4-113">In this case, the user doesn't have to enter a value.</span></span>
4. <span data-ttu-id="ae1c4-114">**製品名** フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="ae1c4-114">In the **Product name** field, type a value.</span></span> <span data-ttu-id="ae1c4-115">製品の内容を示す名前を入力します。</span><span class="sxs-lookup"><span data-stu-id="ae1c4-115">Enter a descriptive product name.</span></span> <span data-ttu-id="ae1c4-116">既定値は検索名になりますが、これはユーザーが変更できます。</span><span class="sxs-lookup"><span data-stu-id="ae1c4-116">The value defaults to the search name, but this can be changed by the user.</span></span>
5. <span data-ttu-id="ae1c4-117">**製品分析コード グループ** フィールドで、ドロップ ダウン ボタンをクリックし、ルックアップを開きます。</span><span class="sxs-lookup"><span data-stu-id="ae1c4-117">In the **Product dimension group** field, click the drop-down button to open the lookup.</span></span> <span data-ttu-id="ae1c4-118">製品分析コード グループにより、製品バリアントを作成するために使用する 4 つの製品分析コードが決まります。</span><span class="sxs-lookup"><span data-stu-id="ae1c4-118">The product dimension group determines which of the 4 product dimensions that can be used to create product variants.</span></span> <span data-ttu-id="ae1c4-119">この例では、色とサイズのグループを使用します。</span><span class="sxs-lookup"><span data-stu-id="ae1c4-119">This example uses a group with color and size.</span></span>
6. <span data-ttu-id="ae1c4-120">一覧で、目的のレコードを見つけ、選択します。</span><span class="sxs-lookup"><span data-stu-id="ae1c4-120">In the list, find and select the desired record.</span></span>
7. <span data-ttu-id="ae1c4-121">一覧で、選択された行のリンクをクリックします。</span><span class="sxs-lookup"><span data-stu-id="ae1c4-121">In the list, click the link in the selected row.</span></span> <span data-ttu-id="ae1c4-122">既定の **コンフィギュレーション テクノロジ** は、「事前に定義されたバリアント」です。</span><span class="sxs-lookup"><span data-stu-id="ae1c4-122">The default **Configuration technology** is 'Predefined variant'.</span></span> <span data-ttu-id="ae1c4-123">これは、この例に使用されます。</span><span class="sxs-lookup"><span data-stu-id="ae1c4-123">This will be used for this example.</span></span>
8. <span data-ttu-id="ae1c4-124">**OK** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="ae1c4-124">Click **OK**.</span></span>

## <a name="select-product-dimension-groups"></a><span data-ttu-id="ae1c4-125">製品分析コード グループの選択</span><span class="sxs-lookup"><span data-stu-id="ae1c4-125">Select product dimension groups</span></span>
1. <span data-ttu-id="ae1c4-126">**色グループ** フィールドで、ドロップ ダウン ボタンをクリックし、ルックアップを開きます。</span><span class="sxs-lookup"><span data-stu-id="ae1c4-126">In the **Color group** field, click the drop-down button to open the lookup.</span></span>
2. <span data-ttu-id="ae1c4-127">一覧で、目的のレコードを見つけ、選択します。</span><span class="sxs-lookup"><span data-stu-id="ae1c4-127">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="ae1c4-128">一覧で、選択された行のリンクをクリックします。</span><span class="sxs-lookup"><span data-stu-id="ae1c4-128">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="ae1c4-129">**サイズ グループ** フィールドで、ドロップ ダウン ボタンをクリックし、ルックアップを開きます。</span><span class="sxs-lookup"><span data-stu-id="ae1c4-129">In the **Size group** field, click the drop-down button to open the lookup.</span></span>
5. <span data-ttu-id="ae1c4-130">一覧で、目的のレコードを見つけ、選択します。</span><span class="sxs-lookup"><span data-stu-id="ae1c4-130">In the list, find and select the desired record.</span></span>
6. <span data-ttu-id="ae1c4-131">一覧で、選択された行のリンクをクリックします。</span><span class="sxs-lookup"><span data-stu-id="ae1c4-131">In the list, click the link in the selected row.</span></span>

## <a name="add-dimension-groups"></a><span data-ttu-id="ae1c4-132">分析コード グループの追加</span><span class="sxs-lookup"><span data-stu-id="ae1c4-132">Add dimension groups</span></span>
1. <span data-ttu-id="ae1c4-133">**アクション ペイン** で、**製品** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="ae1c4-133">On the **Action Pane**, click **Product**.</span></span>
2. <span data-ttu-id="ae1c4-134">**分析コード グループ** をクリックすると、ドロップ ダイアログが開きます。</span><span class="sxs-lookup"><span data-stu-id="ae1c4-134">Click **Dimension groups** to open the drop dialog.</span></span>
3. <span data-ttu-id="ae1c4-135">**保管分析コード グループ** フィールドで、ドロップ ダウン ボタンをクリックし、ルックアップを開きます。</span><span class="sxs-lookup"><span data-stu-id="ae1c4-135">In the **Storage dimension group** field, click the drop-down button to open the lookup.</span></span> <span data-ttu-id="ae1c4-136">保管分析コードは、品目の保管方法と在庫からの取得方法を管理できます。</span><span class="sxs-lookup"><span data-stu-id="ae1c4-136">The storage dimensions help you control how items are stored and taken from inventory.</span></span> <span data-ttu-id="ae1c4-137">たとえば、保管分析コードにはサイトと倉庫を含めることができます。</span><span class="sxs-lookup"><span data-stu-id="ae1c4-137">For example, a storage dimension can include Site and Warehouse.</span></span>
4. <span data-ttu-id="ae1c4-138">一覧で、目的のレコードを見つけ、選択します。</span><span class="sxs-lookup"><span data-stu-id="ae1c4-138">In the list, find and select the desired record.</span></span>
5. <span data-ttu-id="ae1c4-139">一覧で、選択された行のリンクをクリックします。</span><span class="sxs-lookup"><span data-stu-id="ae1c4-139">In the list, click the link in the selected row.</span></span>
6. <span data-ttu-id="ae1c4-140">**追跡用分析コード グループ** フィールドで、ドロップ ダウン ボタンをクリックし、ルックアップを開きます。</span><span class="sxs-lookup"><span data-stu-id="ae1c4-140">In the **Tracking dimension group** field, click the drop-down button to open the lookup.</span></span> <span data-ttu-id="ae1c4-141">追跡用分析コード グループにより、製品に追加できる追跡用分析コードが決まります。</span><span class="sxs-lookup"><span data-stu-id="ae1c4-141">The tracking dimension group determines which tracking dimensions you can add to a product.</span></span> <span data-ttu-id="ae1c4-142">たとえば、バッチ番号とシリアル番号は、在庫品目を追跡するために使用します。</span><span class="sxs-lookup"><span data-stu-id="ae1c4-142">For example, the batch number and serial number are used to track inventory items.</span></span>
7. <span data-ttu-id="ae1c4-143">一覧で、目的のレコードを見つけ、選択します。</span><span class="sxs-lookup"><span data-stu-id="ae1c4-143">In the list, find and select the desired record.</span></span>
8. <span data-ttu-id="ae1c4-144">一覧で、選択された行のリンクをクリックします。</span><span class="sxs-lookup"><span data-stu-id="ae1c4-144">In the list, click the link in the selected row.</span></span>
9. <span data-ttu-id="ae1c4-145">**OK** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="ae1c4-145">Click **OK**.</span></span>
10. <span data-ttu-id="ae1c4-146">**保存** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="ae1c4-146">Click **Save**.</span></span>
11. <span data-ttu-id="ae1c4-147">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="ae1c4-147">Close the page.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]