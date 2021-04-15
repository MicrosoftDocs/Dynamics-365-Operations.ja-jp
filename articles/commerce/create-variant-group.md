---
title: バリアント グループの作成
description: このトピックでは、Microsoft Dynamics 365 Commerce で製品のサイズ、スタイル、または色バリアント グループを作成する方法について説明します。
author: samjarawan
ms.date: 01/27/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: RetailSizeGroupTable, ConfigGroupIdLookup, RetailStyleGroupTable
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: samjar
ms.search.validFrom: 2020-01-20
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: 0462958d8225de145a8d886b096f96cd3f2cb5c5
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/31/2021
ms.locfileid: "5799544"
---
# <a name="create-a-variant-group"></a><span data-ttu-id="c9ae4-103">バリアント グループの作成</span><span class="sxs-lookup"><span data-stu-id="c9ae4-103">Create a variant group</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="c9ae4-104">このトピックでは、Microsoft Dynamics 365 Commerce で製品のサイズ、スタイル、または色バリアント グループを作成する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="c9ae4-104">This topic describes how to create a size, style, or color variant group for a product in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="c9ae4-105">概要</span><span class="sxs-lookup"><span data-stu-id="c9ae4-105">Overview</span></span>

<span data-ttu-id="c9ae4-106">Dynamics 365 Commerce は、製品に対して複数のバリアントをサポートしています。</span><span class="sxs-lookup"><span data-stu-id="c9ae4-106">Dynamics 365 Commerce supports multiple variants for products.</span></span> <span data-ttu-id="c9ae4-107">異なる製品カテゴリに対してさまざまなバリアント グループを設定するのが最適です。</span><span class="sxs-lookup"><span data-stu-id="c9ae4-107">It is ideal to set up variant groups for different product categories.</span></span> <span data-ttu-id="c9ae4-108">たとえば、XS、S、M、L、および XL サイズの T シャツに対してサイズ グループを作成したり、使用可能なすべての製品の色を含むようにカラー グループを作成したりすることができます。</span><span class="sxs-lookup"><span data-stu-id="c9ae4-108">For example, a size group can be created for t-shirts with sizes extra small, small, medium, large, and extra large, or a color group could be created to include all available colors of a product.</span></span> <span data-ttu-id="c9ae4-109">製品を追加する前に、バリアント グループを追加する必要があります。</span><span class="sxs-lookup"><span data-stu-id="c9ae4-109">Variant groups should be added before products are added.</span></span>

<span data-ttu-id="c9ae4-110">このトピックでは、サイズ グループを作成し、コンフィギュレーションします。</span><span class="sxs-lookup"><span data-stu-id="c9ae4-110">In this topic, a size group will be created and configured.</span></span> <span data-ttu-id="c9ae4-111">同じような手順を使用して、スタイル グループおよびカラー グループの追加およびコンフィギュレーションをすることができます。</span><span class="sxs-lookup"><span data-stu-id="c9ae4-111">Similar procedures can be used for adding and configuring style groups and color groups.</span></span>

## <a name="create-a-size-group"></a><span data-ttu-id="c9ae4-112">サイズ グループの作成</span><span class="sxs-lookup"><span data-stu-id="c9ae4-112">Create a size group</span></span>

<span data-ttu-id="c9ae4-113">サイズ グループを作成するには、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="c9ae4-113">To create a size group, follow these steps.</span></span>
 
1. <span data-ttu-id="c9ae4-114">ナビゲーション ウィンドウで、**モジュール \> Retail と Commerce \> 製品とカテゴリ \> バリアント グループ \> サイズ グループ** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="c9ae4-114">In the navigation pane, go to **Modules \> Retail and commerce \> Products and categories \> Variant groups \> Size groups**.</span></span>
1. <span data-ttu-id="c9ae4-115">アクション ウィンドウで、**新規** を選択します。</span><span class="sxs-lookup"><span data-stu-id="c9ae4-115">On the action pane, select **New**.</span></span>
1. <span data-ttu-id="c9ae4-116">**サイズ グループ** ボックスで、サイズ グループの名前を入力します。</span><span class="sxs-lookup"><span data-stu-id="c9ae4-116">In the **Size group** box, enter a name for the size group.</span></span>
1. <span data-ttu-id="c9ae4-117">**説明** ボックスに、適切な説明を入力します。</span><span class="sxs-lookup"><span data-stu-id="c9ae4-117">In the **Description** box, enter an appropriate description.</span></span>
1. <span data-ttu-id="c9ae4-118">アクション ウィンドウで、**保存** を選択します。</span><span class="sxs-lookup"><span data-stu-id="c9ae4-118">On the action pane, select **Save**.</span></span>

## <a name="add-attributes-to-the-size-group"></a><span data-ttu-id="c9ae4-119">サイズ グループへの属性の追加</span><span class="sxs-lookup"><span data-stu-id="c9ae4-119">Add attributes to the size group</span></span>

<span data-ttu-id="c9ae4-120">サイズ グループに属性を追加するには、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="c9ae4-120">To add attributes to a size group, follow these steps.</span></span>

1. <span data-ttu-id="c9ae4-121">ナビゲーション ウィンドウで、**モジュール \> Retail と Commerce \> 製品とカテゴリ \> バリアント グループ \> サイズ グループ** の順に移動</span><span class="sxs-lookup"><span data-stu-id="c9ae4-121">In the navigation pane, go to **Modules \> Retail and commerce \> Products and categories \> Variant groups \> Size groups**</span></span>
1. <span data-ttu-id="c9ae4-122">ナビゲーション ウィンドウで、サイズ グループを選択します。</span><span class="sxs-lookup"><span data-stu-id="c9ae4-122">In the navigation pane, select a size group.</span></span>
1. <span data-ttu-id="c9ae4-123">**サイズ グループ明細行** の下で、**追加** を選択します。</span><span class="sxs-lookup"><span data-stu-id="c9ae4-123">Under **Size group lines**, select **Add**.</span></span>
1. <span data-ttu-id="c9ae4-124">**サイズ** ボックスで、サイズを表す文字列を入力します (たとえば、「XL」)。</span><span class="sxs-lookup"><span data-stu-id="c9ae4-124">In the **Size** box, enter a string representing the size (for example, "XL").</span></span>
1. <span data-ttu-id="c9ae4-125">**サイズ名** ボックスで、サイズの名前を入力します (たとえば、「特大」)。</span><span class="sxs-lookup"><span data-stu-id="c9ae4-125">In the **Size name** box, enter a name for the size (for example, "Extra Large").</span></span>
1. <span data-ttu-id="c9ae4-126">**補充重量** ボックスに、補充重量を表す番号を入力します。</span><span class="sxs-lookup"><span data-stu-id="c9ae4-126">In the **Replenishment weight** box, enter a number representing the replenishment weight.</span></span>
1. <span data-ttu-id="c9ae4-127">**バーコードの番号** ボックスに、バーコードを表す番号を入力します。</span><span class="sxs-lookup"><span data-stu-id="c9ae4-127">In the **Number in bar code** box, enter a number representing the bar code.</span></span>
1. <span data-ttu-id="c9ae4-128">**表示順序** ボックスに、表示順序を表す番号を入力します。</span><span class="sxs-lookup"><span data-stu-id="c9ae4-128">In the **Display order** box, enter a number representing the display order.</span></span>
1. <span data-ttu-id="c9ae4-129">サイズの追加が完了したら、アクション ウィンドウの **保存** を選択します。</span><span class="sxs-lookup"><span data-stu-id="c9ae4-129">When finished adding sizes, select **Save** on the action pane.</span></span>

<span data-ttu-id="c9ae4-130">次の図は、「カジュアル シャツのサイズ」のサイズ グループの例を示しています。</span><span class="sxs-lookup"><span data-stu-id="c9ae4-130">The following image shows an example of a size group for "casual shirt sizes".</span></span>

![サイズ グループの作成](media/create-variant-group.png)

## <a name="additional-resources"></a><span data-ttu-id="c9ae4-132">追加リソース</span><span class="sxs-lookup"><span data-stu-id="c9ae4-132">Additional resources</span></span>

[<span data-ttu-id="c9ae4-133">製品情報の概要</span><span class="sxs-lookup"><span data-stu-id="c9ae4-133">Product information overview</span></span>](../supply-chain/pim/product-information.md?toc=/dynamics365/commerce/toc.json)

[<span data-ttu-id="c9ae4-134">小売製品の設定</span><span class="sxs-lookup"><span data-stu-id="c9ae4-134">Set up retail products</span></span>](set-up-retail-products.md)

[<span data-ttu-id="c9ae4-135">製品分析コード</span><span class="sxs-lookup"><span data-stu-id="c9ae4-135">Product dimensions</span></span>](../supply-chain/pim/product-dimensions.md?toc=/dynamics365/commerce/toc.json)


[!INCLUDE[footer-include](../includes/footer-banner.md)]