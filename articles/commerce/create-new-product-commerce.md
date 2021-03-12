---
title: Commerce の新しい製品を作成
description: このトピックでは、Microsoft Dynamics 365 Commerce に新しい製品を作成する方法について説明します。
author: samjarawan
manager: annbe
ms.date: 01/27/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: samjar
ms.search.validFrom: 2020-01-20
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: 3b578c1bdfe1c6b4bf66cc85cc09ed906fb812a8
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/15/2021
ms.locfileid: "4965318"
---
# <a name="create-a-new-product-in-commerce"></a><span data-ttu-id="f7a09-103">Commerce の新しい製品を作成</span><span class="sxs-lookup"><span data-stu-id="f7a09-103">Create a new product in Commerce</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="f7a09-104">このトピックでは、Microsoft Dynamics 365 Commerce に新しい製品を作成する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="f7a09-104">This topic describes how to create a new product in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="f7a09-105">概要</span><span class="sxs-lookup"><span data-stu-id="f7a09-105">Overview</span></span>

<span data-ttu-id="f7a09-106">製品は、主に、製品番号、名前、および説明によって定義されます。</span><span class="sxs-lookup"><span data-stu-id="f7a09-106">A product is primarily defined by a product number, name, and description.</span></span> <span data-ttu-id="f7a09-107">しかし、製品またはサービスを説明するためには、他のデータも必要です:</span><span class="sxs-lookup"><span data-stu-id="f7a09-107">However, other data is also required in order to describe a product or service:</span></span>

## <a name="create-a-new-product"></a><span data-ttu-id="f7a09-108">新しい製品の作成</span><span class="sxs-lookup"><span data-stu-id="f7a09-108">Create a new product</span></span>

1. <span data-ttu-id="f7a09-109">ナビゲーション ウィンドウで、**モジュール \> 小売りとコマース \> 製品とカテゴリ \> カテゴリ別製品** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="f7a09-109">In the navigation pane, go to **Modules \> Retail and commerce \> Products and categories \> Products by category**.</span></span>
1. <span data-ttu-id="f7a09-110">アクション ウィンドウで、**新規** を選択します。</span><span class="sxs-lookup"><span data-stu-id="f7a09-110">On the action pane, select **New**.</span></span>
1. <span data-ttu-id="f7a09-111">**製品タイプ** ドロップダウン リストで、**品目** または **サービス** のいずれかを選択します。</span><span class="sxs-lookup"><span data-stu-id="f7a09-111">In the **Product type** drop-down list, select either **Item** or **Service**.</span></span>
1. <span data-ttu-id="f7a09-112">**製品サブタイプ** ドロップ ダウン リストで、**製品** (製品にバリアントが含まれていない場合) または **製品マスター** (製品にバリアントがある場合) を選択します。</span><span class="sxs-lookup"><span data-stu-id="f7a09-112">In the **Product subtype** drop-down list, select either **Product** (if the product will have no variants) or **Product master** (if the product will have variants).</span></span>
1. <span data-ttu-id="f7a09-113">**製品番号** ボックスで、製品番号を事前に登録していない場合は、製品番号を入力します。</span><span class="sxs-lookup"><span data-stu-id="f7a09-113">In the **Product number** box, enter a product number if one is not already prepopulated.</span></span>
1. <span data-ttu-id="f7a09-114">**製品名** ボックスに、製品名を入力します。</span><span class="sxs-lookup"><span data-stu-id="f7a09-114">In the **Product name** box, enter a product name.</span></span>
1. <span data-ttu-id="f7a09-115">**検索名** ボックスに、検索名を入力します。</span><span class="sxs-lookup"><span data-stu-id="f7a09-115">In the **Search name** box, enter a search name.</span></span>
1. <span data-ttu-id="f7a09-116">**小売りカテゴリ** ドロップ ダウン リストで、適切なカテゴリを選択します。</span><span class="sxs-lookup"><span data-stu-id="f7a09-116">In the **Retail category** drop-down list, select an appropriate category.</span></span>
1. <span data-ttu-id="f7a09-117">製品がキットの場合は、**製品キット** の **はい** を選択します。</span><span class="sxs-lookup"><span data-stu-id="f7a09-117">If the product is a kit, select **Yes** for **Product kit**.</span></span>
1. <span data-ttu-id="f7a09-118">製品サブタイプが製品マスターの場合は、サポートされているバリアントを含めるために **製品分析コードグループ** を設定します。</span><span class="sxs-lookup"><span data-stu-id="f7a09-118">If the product subtype is product master, set the **Product dimension group** to include the supported variants.</span></span> <span data-ttu-id="f7a09-119">オプションには、**色**、**サイズ**、**スタイル**、および **構成** が含まれます。</span><span class="sxs-lookup"><span data-stu-id="f7a09-119">Options include **Color**, **Size**, **Style**, and **Configuration**.</span></span> <span data-ttu-id="f7a09-120">必要に応じて、追加の製品分析コードグループを作成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="f7a09-120">You may need to create additional product dimension groups if needed.</span></span>
1. <span data-ttu-id="f7a09-121">**コンフィギュレーション テクノロジ** ドロップ ダウン リストで、適切なオプションを選択します。</span><span class="sxs-lookup"><span data-stu-id="f7a09-121">In the **Configuration technology** drop-down list, select an appropriate option.</span></span>
1. <span data-ttu-id="f7a09-122">**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="f7a09-122">Select **OK**.</span></span>

<span data-ttu-id="f7a09-123">次の図は、製品が追加された例を示しています。</span><span class="sxs-lookup"><span data-stu-id="f7a09-123">The following image shows an example product being added.</span></span>

![製品の作成](media/create-new-product.png)

<span data-ttu-id="f7a09-125">製品を追加すると、**製品説明**、**バリアント グループ**、**分析コードグループ**、**製品属性**、**関連製品** などの追加データを設定できます。</span><span class="sxs-lookup"><span data-stu-id="f7a09-125">Once a product is added, additional data can be set for it, such as **Product description**, **Variant groups**, **Dimension groups**, **Product attributes**, and **Related products**.</span></span>

<span data-ttu-id="f7a09-126">次の図は、製品の詳細を示しています。</span><span class="sxs-lookup"><span data-stu-id="f7a09-126">The following image shows a product's additional details.</span></span>

![製品の詳細](media/create-new-product-2.png)

### <a name="create-product-variants"></a><span data-ttu-id="f7a09-128">製品バリアントの作成</span><span class="sxs-lookup"><span data-stu-id="f7a09-128">Create product variants</span></span>

<span data-ttu-id="f7a09-129">製品サブタイプが **製品マスター** の場合は、特定のバリアントを作成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="f7a09-129">If the product subtype is **Product master**, specific variants will need to be created.</span></span> 

<span data-ttu-id="f7a09-130">製品バリアントを作成するには、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="f7a09-130">To create product variants, follow these steps.</span></span>

1. <span data-ttu-id="f7a09-131">アクション ウィンドウで、**製品バリアント** を選択します。</span><span class="sxs-lookup"><span data-stu-id="f7a09-131">On the action pane, select **Product variants**.</span></span>
1. <span data-ttu-id="f7a09-132">アクション ウィンドウでバリアント グループが選択されている場合は \**バリアントの提案* を選択します。</span><span class="sxs-lookup"><span data-stu-id="f7a09-132">If variant groups have been selected on the action pane, select \**Variant suggestions*.</span></span>
1. <span data-ttu-id="f7a09-133">製品に対してサポートするバリアントを選択します。</span><span class="sxs-lookup"><span data-stu-id="f7a09-133">Select the variants you would like to support for the product.</span></span>
1. <span data-ttu-id="f7a09-134">**作成** を選択します。</span><span class="sxs-lookup"><span data-stu-id="f7a09-134">Select **Create**.</span></span>

## <a name="release-a-product"></a><span data-ttu-id="f7a09-135">製品のリリース</span><span class="sxs-lookup"><span data-stu-id="f7a09-135">Release a product</span></span>

<span data-ttu-id="f7a09-136">製品を販売するには、まず、それを法人にリリースする必要があります。</span><span class="sxs-lookup"><span data-stu-id="f7a09-136">To sell a product it must first be released to a legal entity.</span></span>

1. <span data-ttu-id="f7a09-137">製品ページで、**リリース製品** を選択します。</span><span class="sxs-lookup"><span data-stu-id="f7a09-137">From the product page, select **Release products**.</span></span>

    ![製品をリリース](media/create-new-product-3.png)

1. <span data-ttu-id="f7a09-139">リリースする製品を選択し、**次へ** を選択します。</span><span class="sxs-lookup"><span data-stu-id="f7a09-139">Select the product to release, and then select **Next**.</span></span>

    ![リリースする製品を選択](media/create-new-product-4.png)

1. <span data-ttu-id="f7a09-141">リリースする製品バリアントのセットを選択し、**次へ** を選択します。</span><span class="sxs-lookup"><span data-stu-id="f7a09-141">Select the set of product variants to release, and then select **Next**.</span></span>

    ![リリースするバリアントを選択](media/create-new-product-5.png)

1. <span data-ttu-id="f7a09-143">法人を選択し、**次へ** を選択します。</span><span class="sxs-lookup"><span data-stu-id="f7a09-143">Select the legal entity, and then select **Next**.</span></span>

    ![法人の選択](media/create-new-product-6.png)

1. <span data-ttu-id="f7a09-145">**完了** を選択します。</span><span class="sxs-lookup"><span data-stu-id="f7a09-145">Select **Finish**.</span></span>

    ![製品リリース完了](media/create-new-product-7.png)

## <a name="configure-a-released-product"></a><span data-ttu-id="f7a09-147">リリースされた製品をコンフィギュレーションする</span><span class="sxs-lookup"><span data-stu-id="f7a09-147">Configure a released product</span></span>

<span data-ttu-id="f7a09-148">製品がリリースされた後、製品に価格を追加することを含む、追加のコンフィギュレーションが必要になります。</span><span class="sxs-lookup"><span data-stu-id="f7a09-148">Once a product is released, it will then require further configuration that includes adding a price to the product.</span></span>

1. <span data-ttu-id="f7a09-149">ナビゲーション ウィンドウで、**モジュール \> 小売りとコマース \> 製品とカテゴリ \> カテゴリ別リリース済製品** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="f7a09-149">In the navigation pane, go to **Modules \> Retail and commerce \> Products and categories \> Released products by category**.</span></span>
1. <span data-ttu-id="f7a09-150">リリースされた製品の製品カテゴリ ノードを選択し、製品リストから製品を選択します。</span><span class="sxs-lookup"><span data-stu-id="f7a09-150">Select the product category node for the product that was released, and then select the product from the product list.</span></span>
1. <span data-ttu-id="f7a09-151">アクション ウィンドウで、**編集** を選択します。</span><span class="sxs-lookup"><span data-stu-id="f7a09-151">On the action pane, select **Edit**.</span></span>
1. <span data-ttu-id="f7a09-152">**購買** セクションで、**単位**、**価格**、および **数量** を含む、必要なプロパティをコンフィギュレーションします。</span><span class="sxs-lookup"><span data-stu-id="f7a09-152">In the **Purchase** section, configure any required properties including **Unit**, **Price**,  and **Quantity**.</span></span>
1. <span data-ttu-id="f7a09-153">アクションウィンドウで、**検証** を選択して、欠落しているフィールドについてエラーが報告されないことを確認します。</span><span class="sxs-lookup"><span data-stu-id="f7a09-153">On the action pane, select **Validate** to ensure that no errors are reported for missing fields.</span></span>
1. <span data-ttu-id="f7a09-154">アクション ウィンドウで、**保存** を選択します。</span><span class="sxs-lookup"><span data-stu-id="f7a09-154">On the action pane, select **Save**.</span></span>

<span data-ttu-id="f7a09-155">次の図は、リリースされた製品のコンフィギュレーションの例を示しています。</span><span class="sxs-lookup"><span data-stu-id="f7a09-155">The following image shows an example configuration for a released product.</span></span>

![リリースされた製品をコンフィギュレーションする](media/create-new-product-8.png)

## <a name="additional-resources"></a><span data-ttu-id="f7a09-157">追加リソース</span><span class="sxs-lookup"><span data-stu-id="f7a09-157">Additional resources</span></span>

[<span data-ttu-id="f7a09-158">法人の作成</span><span class="sxs-lookup"><span data-stu-id="f7a09-158">Create legal entities</span></span>](channels-legal-entities.md)

[<span data-ttu-id="f7a09-159">バリアント グループの作成</span><span class="sxs-lookup"><span data-stu-id="f7a09-159">Create a variant group</span></span>](create-variant-group.md) 
