--- 
title: "既定の製品のライフサイクルの状態を作成"
description: "この手順では、既定の製品ライフサイクルの状態の作成方法、およびリリースされた製品に既定状態を関連付ける方法を示します。"
author: cvocph
manager: AnnBe
ms.date: 12/05/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.author: conradv
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: d9747ba144d56c9410846769e5465372c89ea111
ms.openlocfilehash: 6e7e637157ee06a3d07a1a9c5da71295eb75b424
ms.contentlocale: ja-jp
ms.lasthandoff: 08/07/2018

---
# <a name="create-a-default-product-lifecycle-state"></a><span data-ttu-id="8806d-103">既定の製品のライフサイクルの状態を作成</span><span class="sxs-lookup"><span data-stu-id="8806d-103">Create a default product lifecycle state</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="8806d-104">この手順では、既定の製品ライフサイクルの状態の作成方法、およびリリースされた製品に既定状態を関連付ける方法を示します。</span><span class="sxs-lookup"><span data-stu-id="8806d-104">This procedure shows how to create a default product lifecycle state as well as how to associate the default state with released products.</span></span>


## <a name="create-a-default-lifecycle-state"></a><span data-ttu-id="8806d-105">既定のライフサイクルの状態を作成</span><span class="sxs-lookup"><span data-stu-id="8806d-105">Create a default lifecycle state</span></span>
1. <span data-ttu-id="8806d-106">[製品情報管理] > [設定] > [製品ライフサイクルの状態] の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="8806d-106">Go to Product information management > Setup > Product lifecycle state.</span></span>
2. <span data-ttu-id="8806d-107">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="8806d-107">Click New.</span></span>
3. <span data-ttu-id="8806d-108">[状態] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="8806d-108">In the State field, type a value.</span></span>
4. <span data-ttu-id="8806d-109">法人フィールドへのリリース時には既定で [はい] を選択します。</span><span class="sxs-lookup"><span data-stu-id="8806d-109">Select Yes in the Default when released to legal entity field.</span></span>
5. <span data-ttu-id="8806d-110">[説明] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="8806d-110">In the Description field, type a value.</span></span>
6. <span data-ttu-id="8806d-111">[計画に対して有効] フィールドで [いいえ] を選択します。</span><span class="sxs-lookup"><span data-stu-id="8806d-111">Select No in the Is active for planning field.</span></span>

> [!NOTE]
> <span data-ttu-id="8806d-112">新たにリリースされた製品をマスター プランに含めない場合は、[いいえ] を選択します。</span><span class="sxs-lookup"><span data-stu-id="8806d-112">If a new released product should not be included in Master planning, select No.</span></span> <span data-ttu-id="8806d-113">マスター プランに含める必要がある場合は、コントロールを既定値の [はい] のままにします。</span><span class="sxs-lookup"><span data-stu-id="8806d-113">If it should be included in Master planning, leave the control at its default value Yes.</span></span>  

## <a name="create-a-new-released-product"></a><span data-ttu-id="8806d-114">新しくリリースされた製品の作成</span><span class="sxs-lookup"><span data-stu-id="8806d-114">Create a new released product</span></span>
1. <span data-ttu-id="8806d-115">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="8806d-115">Close the page.</span></span>
2. <span data-ttu-id="8806d-116">[製品情報管理] > [製品] > [リリースされた製品] の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="8806d-116">Go to Product information management > Products > Released products.</span></span>
3. <span data-ttu-id="8806d-117">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="8806d-117">Click New.</span></span>
4. <span data-ttu-id="8806d-118">[製品番号] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="8806d-118">In the Product number field, type a value.</span></span>
5. <span data-ttu-id="8806d-119">[製品名] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="8806d-119">In the Product name field, type a value.</span></span>
6. <span data-ttu-id="8806d-120">[検索名] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="8806d-120">In the Search name field, type a value.</span></span>
7. <span data-ttu-id="8806d-121">[品目モデル グループ] フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="8806d-121">In the Item model group field, enter or select a value.</span></span>
8. <span data-ttu-id="8806d-122">[品目グループ] フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="8806d-122">In the Item group field, enter or select a value.</span></span>
9. <span data-ttu-id="8806d-123">[保管分析コード グループ] フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="8806d-123">In the Storage dimension group field, enter or select a value.</span></span>
10. <span data-ttu-id="8806d-124">[追跡用分析コード グループ] フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="8806d-124">In the Tracking dimension group field, enter or select a value.</span></span>
11. <span data-ttu-id="8806d-125">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="8806d-125">Click OK.</span></span>

> [!NOTE]
> <span data-ttu-id="8806d-126">既定の製品のライフサイクルの状態は、グローバル定義です。</span><span class="sxs-lookup"><span data-stu-id="8806d-126">The default product lifecycle state is a global definition.</span></span>  

## <a name="change-the-product-to-an-active-state"></a><span data-ttu-id="8806d-127">製品を有効な状態に変更する</span><span class="sxs-lookup"><span data-stu-id="8806d-127">Change the product to an active state</span></span>
1. <span data-ttu-id="8806d-128">[製品ライフサイクルの状態] フィールドで値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="8806d-128">In the Product lifecycle state field, enter or select a value.</span></span>

> [!NOTE]
> <span data-ttu-id="8806d-129">アクティブな状態を設定したと仮定して、アクティブな状態を選択し、マスター プランおよび BOM レベルの計算で製品を使用できるようになります。</span><span class="sxs-lookup"><span data-stu-id="8806d-129">Assume that you have set up an active state, you can now select the active state to allow the product to be used in Master planning and BOM-level calculation.</span></span> <span data-ttu-id="8806d-130">当然、一貫した計画に必要なすべての製品の詳細が指定されている場合にのみ意味があります。</span><span class="sxs-lookup"><span data-stu-id="8806d-130">Obviously, this only makes sense if all the product details that are required for consistent planning are specified.</span></span>  


