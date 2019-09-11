---
title: 事前定義された製品バリアントの製品番号の分類の作成
description: このトピックでは、事前定義済製品バリアントの製品番号の分類を設定する方法、および適切な製品分析コード グループに割り当てる方法を説明します。
author: ShylaThompson
manager: AnnBe
ms.date: 08/20/2019
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
ms.openlocfilehash: 5cf0efeac2851e6ead6fc5e15a016370dfa620bc
ms.sourcegitcommit: e10491a2ff04f65d9f306ef6e068ee123213b23b
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/21/2019
ms.locfileid: "1914910"
---
# <a name="create-a-product-number-nomenclature-for-predefined-product-variants"></a><span data-ttu-id="3bc92-103">事前定義された製品バリアントの製品番号の分類の作成</span><span class="sxs-lookup"><span data-stu-id="3bc92-103">Create a product number nomenclature for predefined product variants</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="3bc92-104">このトピックでは、事前定義済製品バリアントの製品番号の分類を設定する方法、および適切な製品分析コード グループに割り当てる方法を説明します。</span><span class="sxs-lookup"><span data-stu-id="3bc92-104">This topic explains how to set up a product number nomenclature for predefined product variants, and how you assign it to the appropriate product dimension group.</span></span> <span data-ttu-id="3bc92-105">この手順の作成に使用するデモ データの会社は USMF です。</span><span class="sxs-lookup"><span data-stu-id="3bc92-105">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="3bc92-106">新しい製品番号に関する分類は、色やサイズの製品分析コード グループに割り当てられます。</span><span class="sxs-lookup"><span data-stu-id="3bc92-106">The new product number nomenclature is assigned to the Color and Size product dimension group.</span></span> <span data-ttu-id="3bc92-107">このタスクは、通常、製品デザイナーが行います。</span><span class="sxs-lookup"><span data-stu-id="3bc92-107">This task would typically be done by a product designer.</span></span>


## <a name="create-a-product-number-nomenclature"></a><span data-ttu-id="3bc92-108">[製品番号の分類] を作成します。</span><span class="sxs-lookup"><span data-stu-id="3bc92-108">Create a product number nomenclature</span></span>
1. <span data-ttu-id="3bc92-109">**製品バリアント モデルの定義**を選択します。</span><span class="sxs-lookup"><span data-stu-id="3bc92-109">Select **Product variant model definition**.</span></span>
2. <span data-ttu-id="3bc92-110">**製品の分類**を選択します。</span><span class="sxs-lookup"><span data-stu-id="3bc92-110">Select **Product nomenclature**.</span></span>
3. <span data-ttu-id="3bc92-111">**新規** を選択します。</span><span class="sxs-lookup"><span data-stu-id="3bc92-111">Select **New**.</span></span>
4. <span data-ttu-id="3bc92-112">**名前**フィールドに、目標の製品分析コード グループ、たとえば、`ColorSize` を特定する用語の名前を入力します。</span><span class="sxs-lookup"><span data-stu-id="3bc92-112">In the **Name** field, enter a nomenclature name that helps to identify the target product dimension group, for example, `ColorSize`.</span></span>
5. <span data-ttu-id="3bc92-113">**説明**フィールドで、値を入力します。</span><span class="sxs-lookup"><span data-stu-id="3bc92-113">In the **Description** field, type a value.</span></span>
6. <span data-ttu-id="3bc92-114">**追加**を選択します。</span><span class="sxs-lookup"><span data-stu-id="3bc92-114">Select **Add**.</span></span>
7. <span data-ttu-id="3bc92-115">**製品マスター**番号を選択します。</span><span class="sxs-lookup"><span data-stu-id="3bc92-115">Select **Product master** number.</span></span>
8. <span data-ttu-id="3bc92-116">**追加**を選択します。</span><span class="sxs-lookup"><span data-stu-id="3bc92-116">Select **Add**.</span></span>
9. <span data-ttu-id="3bc92-117">**テキスト定数**を選択します。</span><span class="sxs-lookup"><span data-stu-id="3bc92-117">Select **Text constant**.</span></span>
10. <span data-ttu-id="3bc92-118">**テキスト** フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="3bc92-118">In the **Text** field, type a value.</span></span>
11. <span data-ttu-id="3bc92-119">**追加**を選択します。</span><span class="sxs-lookup"><span data-stu-id="3bc92-119">Select **Add**.</span></span>
12. <span data-ttu-id="3bc92-120">**色**を選択します。</span><span class="sxs-lookup"><span data-stu-id="3bc92-120">Select **Color**.</span></span>
13. <span data-ttu-id="3bc92-121">**追加**を選択します。</span><span class="sxs-lookup"><span data-stu-id="3bc92-121">Select **Add**.</span></span>
14. <span data-ttu-id="3bc92-122">**テキスト定数**を選択します。</span><span class="sxs-lookup"><span data-stu-id="3bc92-122">Select **Text constant**.</span></span>
15. <span data-ttu-id="3bc92-123">**テキスト** フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="3bc92-123">In the **Text** field, type a value.</span></span>
16. <span data-ttu-id="3bc92-124">**追加**を選択します。</span><span class="sxs-lookup"><span data-stu-id="3bc92-124">Select **Add**.</span></span>
17. <span data-ttu-id="3bc92-125">**サイズ**を選択します。</span><span class="sxs-lookup"><span data-stu-id="3bc92-125">Select **Size**.</span></span>
18. <span data-ttu-id="3bc92-126">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="3bc92-126">Close the page.</span></span>

## <a name="assign-the-nomenclature-to-a-product-master"></a><span data-ttu-id="3bc92-127">製品マスターに用語を割り当て</span><span class="sxs-lookup"><span data-stu-id="3bc92-127">Assign the nomenclature to a product master</span></span>
1. <span data-ttu-id="3bc92-128">**製品分析コード グループ**を選択します。</span><span class="sxs-lookup"><span data-stu-id="3bc92-128">Select **Product dimension groups**.</span></span>
2. <span data-ttu-id="3bc92-129">**SizeCol 製品分析コード** グループを選択します。</span><span class="sxs-lookup"><span data-stu-id="3bc92-129">Select the **SizeCol product dimension** group.</span></span>
3. <span data-ttu-id="3bc92-130">**編集**を選択します。</span><span class="sxs-lookup"><span data-stu-id="3bc92-130">Select **Edit**.</span></span>
4. <span data-ttu-id="3bc92-131">**分類の使用**フィールドで、**はい**を選択します。</span><span class="sxs-lookup"><span data-stu-id="3bc92-131">Select **Yes** in the **Use nomenclature** field.</span></span>
5. <span data-ttu-id="3bc92-132">**製品バリアント番号の分類**フィールドに、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="3bc92-132">In the **Product variant number nomenclature** field, enter or select a value.</span></span>
6. <span data-ttu-id="3bc92-133">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="3bc92-133">Close the page.</span></span>

