---
title: 事前定義された製品バリアントの製品番号の分類の作成
description: このトピックでは、事前定義済製品バリアントの製品番号の分類を設定する方法、および適切な製品分析コード グループに割り当てる方法を説明します。
author: ShylaThompson
ms.date: 08/20/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: DefaultDashboard, EcoResProductVariantMaintainWorkspace, EcoResNomenclature, EcoResProductDimensionGroup
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 4bb73854f52525c0722683086d1b4f1dd7173306
ms.sourcegitcommit: fa99a36c3d30d0c0577fd3f63ed6bf2f71599e40
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/20/2021
ms.locfileid: "5920660"
---
# <a name="create-a-product-number-nomenclature-for-predefined-product-variants"></a><span data-ttu-id="8c874-103">事前定義された製品バリアントの製品番号の分類の作成</span><span class="sxs-lookup"><span data-stu-id="8c874-103">Create a product number nomenclature for predefined product variants</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="8c874-104">このトピックでは、事前定義済製品バリアントの製品番号の分類を設定する方法、および適切な製品分析コード グループに割り当てる方法を説明します。</span><span class="sxs-lookup"><span data-stu-id="8c874-104">This topic explains how to set up a product number nomenclature for predefined product variants, and how you assign it to the appropriate product dimension group.</span></span> <span data-ttu-id="8c874-105">この手順の作成に使用するデモ データの会社は USMF です。</span><span class="sxs-lookup"><span data-stu-id="8c874-105">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="8c874-106">新しい製品番号に関する分類は、色やサイズの製品分析コード グループに割り当てられます。</span><span class="sxs-lookup"><span data-stu-id="8c874-106">The new product number nomenclature is assigned to the Color and Size product dimension group.</span></span> <span data-ttu-id="8c874-107">このタスクは、通常、製品デザイナーが行います。</span><span class="sxs-lookup"><span data-stu-id="8c874-107">This task would typically be done by a product designer.</span></span>


## <a name="create-a-product-number-nomenclature"></a><span data-ttu-id="8c874-108">[製品番号の分類] を作成します。</span><span class="sxs-lookup"><span data-stu-id="8c874-108">Create a product number nomenclature</span></span>

1. <span data-ttu-id="8c874-109">**製品情報管理\>設定\>製品の分類** の順にクリックします。</span><span class="sxs-lookup"><span data-stu-id="8c874-109">Go to **Product information management \> Setup \> Product nomenclature**.</span></span>
1. <span data-ttu-id="8c874-110">**新規** を選択します。</span><span class="sxs-lookup"><span data-stu-id="8c874-110">Select **New**.</span></span>
1. <span data-ttu-id="8c874-111">**名前** フィールドに、目標の製品分析コード グループ、たとえば、`ColorSize` を特定する用語の名前を入力します。</span><span class="sxs-lookup"><span data-stu-id="8c874-111">In the **Name** field, enter a nomenclature name that helps to identify the target product dimension group, for example, `ColorSize`.</span></span>
1. <span data-ttu-id="8c874-112">**説明** フィールドで、値を入力します。</span><span class="sxs-lookup"><span data-stu-id="8c874-112">In the **Description** field, type a value.</span></span>
1. <span data-ttu-id="8c874-113">**追加** を選択します。</span><span class="sxs-lookup"><span data-stu-id="8c874-113">Select **Add**.</span></span>
1. <span data-ttu-id="8c874-114">**製品マスター** 番号を選択します。</span><span class="sxs-lookup"><span data-stu-id="8c874-114">Select **Product master** number.</span></span>
1. <span data-ttu-id="8c874-115">**追加** を選択します。</span><span class="sxs-lookup"><span data-stu-id="8c874-115">Select **Add**.</span></span>
1. <span data-ttu-id="8c874-116">**テキスト定数** を選択します。</span><span class="sxs-lookup"><span data-stu-id="8c874-116">Select **Text constant**.</span></span>
1. <span data-ttu-id="8c874-117">**テキスト** フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="8c874-117">In the **Text** field, type a value.</span></span>
1. <span data-ttu-id="8c874-118">**追加** を選択します。</span><span class="sxs-lookup"><span data-stu-id="8c874-118">Select **Add**.</span></span>
1. <span data-ttu-id="8c874-119">**色** を選択します。</span><span class="sxs-lookup"><span data-stu-id="8c874-119">Select **Color**.</span></span>
1. <span data-ttu-id="8c874-120">**追加** を選択します。</span><span class="sxs-lookup"><span data-stu-id="8c874-120">Select **Add**.</span></span>
1. <span data-ttu-id="8c874-121">**テキスト定数** を選択します。</span><span class="sxs-lookup"><span data-stu-id="8c874-121">Select **Text constant**.</span></span>
1. <span data-ttu-id="8c874-122">**テキスト** フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="8c874-122">In the **Text** field, type a value.</span></span>
1. <span data-ttu-id="8c874-123">**追加** を選択します。</span><span class="sxs-lookup"><span data-stu-id="8c874-123">Select **Add**.</span></span>
1. <span data-ttu-id="8c874-124">**サイズ** を選択します。</span><span class="sxs-lookup"><span data-stu-id="8c874-124">Select **Size**.</span></span>
1. <span data-ttu-id="8c874-125">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="8c874-125">Close the page.</span></span>

## <a name="assign-the-nomenclature-to-a-product-master"></a><span data-ttu-id="8c874-126">製品マスターに用語を割り当て</span><span class="sxs-lookup"><span data-stu-id="8c874-126">Assign the nomenclature to a product master</span></span>

1. <span data-ttu-id="8c874-127">**製品分析コード グループ** を選択します。</span><span class="sxs-lookup"><span data-stu-id="8c874-127">Select **Product dimension groups**.</span></span>
2. <span data-ttu-id="8c874-128">**SizeCol 製品分析コード** グループを選択します。</span><span class="sxs-lookup"><span data-stu-id="8c874-128">Select the **SizeCol product dimension** group.</span></span>
3. <span data-ttu-id="8c874-129">**編集** を選択します。</span><span class="sxs-lookup"><span data-stu-id="8c874-129">Select **Edit**.</span></span>
4. <span data-ttu-id="8c874-130">**分類の使用** フィールドで、**はい** を選択します。</span><span class="sxs-lookup"><span data-stu-id="8c874-130">Select **Yes** in the **Use nomenclature** field.</span></span>
5. <span data-ttu-id="8c874-131">**製品バリアント番号の分類** フィールドに、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="8c874-131">In the **Product variant number nomenclature** field, enter or select a value.</span></span>
6. <span data-ttu-id="8c874-132">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="8c874-132">Close the page.</span></span>


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]