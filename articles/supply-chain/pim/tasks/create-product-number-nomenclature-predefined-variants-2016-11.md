---
title: 事前定義された製品バリアントの製品番号の分類の作成
description: この手順では、事前定義済製品バリアントの製品番号の分類を設定する方法、および適切な製品分析コード グループに割り当てる方法を示します。
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DefaultDashboard, EcoResProductVariantMaintainWorkspace, EcoResNomenclature, EcoResProductDimensionGroup
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 6a2e61fd99cb80a1a9cc3d8e985fb0f14e3c2fc2
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/01/2019
ms.locfileid: "1844684"
---
# <a name="create-a-product-number-nomenclature-for-predefined-product-variants"></a><span data-ttu-id="9de71-103">事前定義された製品バリアントの製品番号の分類の作成</span><span class="sxs-lookup"><span data-stu-id="9de71-103">Create a product number nomenclature for predefined product variants</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="9de71-104">この手順では、事前定義済製品バリアントの製品番号の分類を設定する方法、および適切な製品分析コード グループに割り当てる方法を示します。</span><span class="sxs-lookup"><span data-stu-id="9de71-104">This guide shows you how to set up a product number nomenclature for predefined product variants, and how you assign it to the appropriate product dimension group.</span></span> <span data-ttu-id="9de71-105">この手順の作成に使用するデモ データの会社は USMF です。</span><span class="sxs-lookup"><span data-stu-id="9de71-105">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="9de71-106">新しい製品番号に関する分類は、色やサイズの製品分析コード グループに割り当てられます。</span><span class="sxs-lookup"><span data-stu-id="9de71-106">The new product number nomenclature is assigned to the Color and Size product dimension group.</span></span> <span data-ttu-id="9de71-107">このタスクは、通常、製品デザイナーが行います。</span><span class="sxs-lookup"><span data-stu-id="9de71-107">This task would typically be done by a product designer.</span></span>


## <a name="create-a-product-number-nomenclature"></a><span data-ttu-id="9de71-108">[製品番号の分類] を作成します。</span><span class="sxs-lookup"><span data-stu-id="9de71-108">Create a product number nomenclature</span></span>
1. <span data-ttu-id="9de71-109">[製品バリアント モデルの定義] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="9de71-109">Click Product variant model definition.</span></span>
2. <span data-ttu-id="9de71-110">[製品の分類] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="9de71-110">Click Product nomenclature.</span></span>
3. <span data-ttu-id="9de71-111">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="9de71-111">Click New.</span></span>
4. <span data-ttu-id="9de71-112">[名前] フィールドに、目標の製品分析コード グループ、たとえば、ColorSize を特定する用語の名前を入力します。</span><span class="sxs-lookup"><span data-stu-id="9de71-112">In the Name field, enter a nomenclature name that helps to identify the target product dimension group, for example, ColorSize..</span></span>
5. <span data-ttu-id="9de71-113">[説明] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="9de71-113">In the Description field, type a value.</span></span>
6. <span data-ttu-id="9de71-114">[追加] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="9de71-114">Click Add.</span></span>
7. <span data-ttu-id="9de71-115">[製品マスター番号] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="9de71-115">Click Product master number.</span></span>
8. <span data-ttu-id="9de71-116">[追加] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="9de71-116">Click Add.</span></span>
9. <span data-ttu-id="9de71-117">[テキスト定数] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="9de71-117">Click Text constant.</span></span>
10. <span data-ttu-id="9de71-118">[テキスト] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="9de71-118">In the Text field, type a value.</span></span>
11. <span data-ttu-id="9de71-119">[追加] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="9de71-119">Click Add.</span></span>
12. <span data-ttu-id="9de71-120">[色] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="9de71-120">Click Color.</span></span>
13. <span data-ttu-id="9de71-121">[追加] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="9de71-121">Click Add.</span></span>
14. <span data-ttu-id="9de71-122">[テキスト定数] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="9de71-122">Click Text constant.</span></span>
15. <span data-ttu-id="9de71-123">[テキスト] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="9de71-123">In the Text field, type a value.</span></span>
16. <span data-ttu-id="9de71-124">[追加] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="9de71-124">Click Add.</span></span>
17. <span data-ttu-id="9de71-125">[サイズ] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="9de71-125">Click Size.</span></span>
18. <span data-ttu-id="9de71-126">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="9de71-126">Close the page.</span></span>

## <a name="assign-the-nomenclature-to-a-product-master"></a><span data-ttu-id="9de71-127">製品マスターに用語を割り当て</span><span class="sxs-lookup"><span data-stu-id="9de71-127">Assign the nomenclature to a product master</span></span>
1. <span data-ttu-id="9de71-128">[製品分析コード グループ] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="9de71-128">Click Product dimension groups.</span></span>
2. <span data-ttu-id="9de71-129">[SizeCol 製品分析コード グループ] を選択します。</span><span class="sxs-lookup"><span data-stu-id="9de71-129">Select the SizeCol product dimension group.</span></span>
3. <span data-ttu-id="9de71-130">[編集] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="9de71-130">Click Edit.</span></span>
4. <span data-ttu-id="9de71-131">[分類の使用] フィールドで、[はい] を選択します。</span><span class="sxs-lookup"><span data-stu-id="9de71-131">Select Yes in the Use nomenclature field.</span></span>
5. <span data-ttu-id="9de71-132">[製品バリアント番号の分類] フィールドに、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="9de71-132">In the Product variant number nomenclature field, enter or select a value.</span></span>
6. <span data-ttu-id="9de71-133">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="9de71-133">Close the page.</span></span>

