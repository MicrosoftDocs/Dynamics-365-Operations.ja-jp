---
title: 事前定義された製品バリアントの作成
description: この手順では、製品分析コードの組み合わせを使用する製品マスターの製品バリアントの作成を説明します。
author: ShylaThompson
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EcoResProductListPage, EcoResProductCreate, EcoResProductDetails, EcoResProductMasterDimension, EcoResProductVariants, EcoResProductVariantSuggestions, EcoResProductVariantsPendingReleaseFormPart
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 6009f6de76155ea7c2982b28fe4505232447c9c8
ms.sourcegitcommit: 97d4a9bd442fe20f90605d8154c3a947c7645b37
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/28/2020
ms.locfileid: "3895308"
---
# <a name="create-predefined-product-variants"></a><span data-ttu-id="60582-103">事前定義された製品バリアントの作成</span><span class="sxs-lookup"><span data-stu-id="60582-103">Create predefined product variants</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="60582-104">この手順では、製品分析コードの組み合わせを使用する製品マスターの製品バリアントの作成を説明します。</span><span class="sxs-lookup"><span data-stu-id="60582-104">This procedure walks through creating product variants for a product master using the combinations of product dimensions.</span></span> <span data-ttu-id="60582-105">この手順の作成に使用されるデモ データ会社は USMF です。</span><span class="sxs-lookup"><span data-stu-id="60582-105">The demo company used to create this procedure is USMF.</span></span>


## <a name="create-a-product-master"></a><span data-ttu-id="60582-106">製品マスターの作成</span><span class="sxs-lookup"><span data-stu-id="60582-106">Create a product master</span></span>
1. <span data-ttu-id="60582-107">[製品情報管理] > [製品] > [製品マスター] の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="60582-107">Go to Product information management > Products > Product masters.</span></span>
2. <span data-ttu-id="60582-108">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="60582-108">Click New.</span></span>
3. <span data-ttu-id="60582-109">[製品番号] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="60582-109">In the Product number field, type a value.</span></span>
    * <span data-ttu-id="60582-110">[製品番号] フィールドに番号順序が設定されていない場合は、製品番号の手動入力のみ必須です。</span><span class="sxs-lookup"><span data-stu-id="60582-110">Entering a product number manually is only required if no number sequence has been set for the product number field.</span></span> <span data-ttu-id="60582-111">つまり、番号順序がフィールドに設定されている場合、手順を省略します。</span><span class="sxs-lookup"><span data-stu-id="60582-111">In other words, skip the step if number sequence has been set for the field.</span></span>  
4. <span data-ttu-id="60582-112">[製品名] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="60582-112">In the Product name field, type a value.</span></span>
5. <span data-ttu-id="60582-113">[製品分析コード グループ] フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="60582-113">In the Product dimension group field, enter or select a value.</span></span>
    * <span data-ttu-id="60582-114">製品分析コード グループ SizeCol (サイズおよび色) を選択します。</span><span class="sxs-lookup"><span data-stu-id="60582-114">Select the product dimension group SizeCol (Size and Color).</span></span>  
6. <span data-ttu-id="60582-115">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="60582-115">Click OK.</span></span>

## <a name="add-product-dimensions"></a><span data-ttu-id="60582-116">製品分析コードの追加</span><span class="sxs-lookup"><span data-stu-id="60582-116">Add product dimensions</span></span>
1. <span data-ttu-id="60582-117">[製品分析コード] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="60582-117">Click Product dimensions.</span></span>
    * <span data-ttu-id="60582-118">この例では、手動で製品分析コードを入力する方法を示します。</span><span class="sxs-lookup"><span data-stu-id="60582-118">This example shows how to manually enter product dimensions.</span></span> <span data-ttu-id="60582-119">使用する製品分析コードの値を含むサイズ、色、またはスタイル グループを選択することもできます。</span><span class="sxs-lookup"><span data-stu-id="60582-119">You can also choose to select a size, color or style group that includes the product dimension values you want to use.</span></span>  
2. <span data-ttu-id="60582-120">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="60582-120">Click New.</span></span>
3. <span data-ttu-id="60582-121">一覧で、選択された行をマークします。</span><span class="sxs-lookup"><span data-stu-id="60582-121">In the list, mark the selected row.</span></span>
4. <span data-ttu-id="60582-122">[サイズ] フィールドで値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="60582-122">In the Size field, enter or select a value.</span></span>
5. <span data-ttu-id="60582-123">[名前] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="60582-123">In the Name field, type a value.</span></span>
6. <span data-ttu-id="60582-124">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="60582-124">Click New.</span></span>
7. <span data-ttu-id="60582-125">一覧で、選択された行をマークします。</span><span class="sxs-lookup"><span data-stu-id="60582-125">In the list, mark the selected row.</span></span>
8. <span data-ttu-id="60582-126">[サイズ] フィールドで値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="60582-126">In the Size field, enter or select a value.</span></span>
9. <span data-ttu-id="60582-127">[名前] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="60582-127">In the Name field, type a value.</span></span>
10. <span data-ttu-id="60582-128">[色] タブをクリックします。</span><span class="sxs-lookup"><span data-stu-id="60582-128">Click the Colors tab.</span></span>
11. <span data-ttu-id="60582-129">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="60582-129">Click New.</span></span>
12. <span data-ttu-id="60582-130">一覧で、選択された行をマークします。</span><span class="sxs-lookup"><span data-stu-id="60582-130">In the list, mark the selected row.</span></span>
13. <span data-ttu-id="60582-131">[色] フィールドで値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="60582-131">In the Color field, enter or select a value.</span></span>
14. <span data-ttu-id="60582-132">[名前] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="60582-132">In the Name field, type a value.</span></span>
15. <span data-ttu-id="60582-133">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="60582-133">Click New.</span></span>
16. <span data-ttu-id="60582-134">一覧で、選択された行をマークします。</span><span class="sxs-lookup"><span data-stu-id="60582-134">In the list, mark the selected row.</span></span>
17. <span data-ttu-id="60582-135">[色] フィールドで値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="60582-135">In the Color field, enter or select a value.</span></span>
18. <span data-ttu-id="60582-136">[名前] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="60582-136">In the Name field, type a value.</span></span>
19. <span data-ttu-id="60582-137">[保存] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="60582-137">Click Save.</span></span>
20. <span data-ttu-id="60582-138">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="60582-138">Close the page.</span></span>

## <a name="generate-product-variants"></a><span data-ttu-id="60582-139">製品バリアントの生成</span><span class="sxs-lookup"><span data-stu-id="60582-139">Generate product variants</span></span>
1. <span data-ttu-id="60582-140">[製品バリアント] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="60582-140">Click Product variants.</span></span>
2. <span data-ttu-id="60582-141">[バリアント修正候補] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="60582-141">Click Variant suggestions.</span></span>
3. <span data-ttu-id="60582-142">[すべて選択] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="60582-142">Click Select all.</span></span>
    * <span data-ttu-id="60582-143">この例では、すべての可能なバリアントが選択されます。</span><span class="sxs-lookup"><span data-stu-id="60582-143">In this example, all possible variants are selected.</span></span> <span data-ttu-id="60582-144">可能な製品分析コードの組み合わせのサブセットのみをバリアントの作成に使用する場合、個々のエントリを選択できます。</span><span class="sxs-lookup"><span data-stu-id="60582-144">If only a subset of the possible product dimension combinations will be used to create variants, you can select the individual entries.</span></span>  
4. <span data-ttu-id="60582-145">[作成] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="60582-145">Click Create.</span></span>
    * <span data-ttu-id="60582-146">製品分析コードの値の組み合わせに基づいてすべてのバリアントの説明を生成できます。</span><span class="sxs-lookup"><span data-stu-id="60582-146">You can generate descriptions for all your variants based on the combination of product dimension values.</span></span> <span data-ttu-id="60582-147">説明はオプションです。</span><span class="sxs-lookup"><span data-stu-id="60582-147">The descriptions are optional.</span></span>  
5. <span data-ttu-id="60582-148">[保存] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="60582-148">Click Save.</span></span>

