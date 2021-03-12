---
title: コンフィギュレーション可能な製品の属性ベースの価格決定の設定
description: このトピックでは、属性ベースの価格決定の方法を説明します。
author: ShylaThompson
manager: tfehr
ms.date: 08/20/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DefaultDashboard, EcoResProductVariantMaintainWorkspace, PCProductConfigurationModelListPage, PCPriceModelList, PCPriceModel, PCConstraintEditor
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: b2f9a78902ff1a0333c46c8ad9142338678b6e7d
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/15/2021
ms.locfileid: "4986782"
---
# <a name="set-up-attribute-based-pricing-for-configurable-products"></a><span data-ttu-id="ac608-103">コンフィギュレーション可能な製品の属性ベースの価格決定の設定</span><span class="sxs-lookup"><span data-stu-id="ac608-103">Set up attribute-based pricing for configurable products</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="ac608-104">このトピックでは、属性ベースの価格決定の方法を説明します。</span><span class="sxs-lookup"><span data-stu-id="ac608-104">This topic explains how to set up attribute-based pricing.</span></span> <span data-ttu-id="ac608-105">前提条件として、1 つ以上のコンポーネントと属性を持つ製品コンフィギュレーション モデルが必要です。</span><span class="sxs-lookup"><span data-stu-id="ac608-105">As a prerequisite, you must have a product configuration model that has one or more components and attributes.</span></span> <span data-ttu-id="ac608-106">この例では、デモ データの会社 USMF のハイエンド スピーカーの製品モデルが使用されています。</span><span class="sxs-lookup"><span data-stu-id="ac608-106">This example uses the High End Speaker product model in the USMF demo data company.</span></span> <span data-ttu-id="ac608-107">通常、製品マネージャーがこの手順を使用します。</span><span class="sxs-lookup"><span data-stu-id="ac608-107">Typically, a product manager uses this procedure.</span></span>


## <a name="create-a-new-price-model"></a><span data-ttu-id="ac608-108">新しい価格モデルの作成</span><span class="sxs-lookup"><span data-stu-id="ac608-108">Create a new price model</span></span>
1. <span data-ttu-id="ac608-109">ホームページで **製品バリアント モデルの定義** を選択します。</span><span class="sxs-lookup"><span data-stu-id="ac608-109">Select **Product variant model definition** on the home page.</span></span>
2. <span data-ttu-id="ac608-110">**リンク** セクションで、**製品コンフィギュレーション モデル** を選択します。</span><span class="sxs-lookup"><span data-stu-id="ac608-110">Select **Product configuration models** in the **links** section.</span></span>
3. <span data-ttu-id="ac608-111">リストで、名前のリンクを選択せずに、**ハイ エンド スピーカー** 行を選択します。</span><span class="sxs-lookup"><span data-stu-id="ac608-111">In the list, select the **High End Speaker** line, but don't select the link for the name.</span></span>
4. <span data-ttu-id="ac608-112">アクション ウィンドウで、**モデル** を選択します。</span><span class="sxs-lookup"><span data-stu-id="ac608-112">On the Action Pane, select **Model**.</span></span>
5. <span data-ttu-id="ac608-113">**価格モデル** を選択します。</span><span class="sxs-lookup"><span data-stu-id="ac608-113">Select **Price models**.</span></span>
6. <span data-ttu-id="ac608-114">**新規** を選択します。</span><span class="sxs-lookup"><span data-stu-id="ac608-114">Select **New**.</span></span>
7. <span data-ttu-id="ac608-115">**価格モデル名** フィールドに、値を入力します。</span><span class="sxs-lookup"><span data-stu-id="ac608-115">In the **Price model name** field, type a value.</span></span> <span data-ttu-id="ac608-116">容易にモデルを識別できる名前を使用します。</span><span class="sxs-lookup"><span data-stu-id="ac608-116">Use a name that makes the model easy to identify.</span></span>  
8. <span data-ttu-id="ac608-117">**説明** フィールドで、値を入力します。</span><span class="sxs-lookup"><span data-stu-id="ac608-117">In the **Description** field, type a value.</span></span>
9. <span data-ttu-id="ac608-118">**保存** を選択します。</span><span class="sxs-lookup"><span data-stu-id="ac608-118">Select **Save**.</span></span>

## <a name="add-price-elements"></a><span data-ttu-id="ac608-119">価格要素の追加</span><span class="sxs-lookup"><span data-stu-id="ac608-119">Add price elements</span></span>
1. <span data-ttu-id="ac608-120">**編集** を選択します。</span><span class="sxs-lookup"><span data-stu-id="ac608-120">Select **Edit**.</span></span> <span data-ttu-id="ac608-121">製品モデルの各コンポーネントごとに、価格の式のルールの基準価格要素および任意の数字を設定できます。</span><span class="sxs-lookup"><span data-stu-id="ac608-121">Each component in a product model can have a base price element and any number of price expression rules.</span></span> <span data-ttu-id="ac608-122">異なる通貨でも価格を追加できます。</span><span class="sxs-lookup"><span data-stu-id="ac608-122">You can also add prices in different currencies.</span></span>  
2. <span data-ttu-id="ac608-123">**基準価格の式** フィールドに、値を入力します。</span><span class="sxs-lookup"><span data-stu-id="ac608-123">In the **Base price expression** field, type a value.</span></span> <span data-ttu-id="ac608-124">たとえば、「100」と入力します。</span><span class="sxs-lookup"><span data-stu-id="ac608-124">For example, type 100.</span></span> <span data-ttu-id="ac608-125">基準価格の式は、数値あるいは 1 つ以上の属性を含む算術計算で構成できます。</span><span class="sxs-lookup"><span data-stu-id="ac608-125">A base price expression can be a numerical value, or it can consist of an arithmetic calculation that involves one or more attributes.</span></span>  
3. <span data-ttu-id="ac608-126">**追加** を選択します。</span><span class="sxs-lookup"><span data-stu-id="ac608-126">Select **Add**.</span></span>
4. <span data-ttu-id="ac608-127">**名前** フィールドに、`Rosewood` と入力します。</span><span class="sxs-lookup"><span data-stu-id="ac608-127">In the **Name** field, type `Rosewood`.</span></span> <span data-ttu-id="ac608-128">価格の式の名前は、価格要素が表す内容を識別する場合に役立ちます。</span><span class="sxs-lookup"><span data-stu-id="ac608-128">The price expression name helps identify what the price element represents.</span></span> <span data-ttu-id="ac608-129">この例では、シタンのスピーカー キャビネットの仕上げオプションに対する価格要素を作成します。</span><span class="sxs-lookup"><span data-stu-id="ac608-129">In this example, we are creating a price element for the Rosewood speaker cabinet finish option.</span></span>  
5. <span data-ttu-id="ac608-130">**条件の編集** を選択します。</span><span class="sxs-lookup"><span data-stu-id="ac608-130">Select **Edit condition**.</span></span> <span data-ttu-id="ac608-131">価格の条件によって、属性の特定の組み合わせがある場合にのみ、価格の式の要素を確実に販売価格に含められます。</span><span class="sxs-lookup"><span data-stu-id="ac608-131">A price condition helps guarantee that a price expression element is included in the sales price only if a specific combination of attributes is present.</span></span>  
6. <span data-ttu-id="ac608-132">**ConstraintBody** フィールドに、`CabinetFinish=="Rosewood"` と入力します。</span><span class="sxs-lookup"><span data-stu-id="ac608-132">In the **ConstraintBody** field, enter `CabinetFinish=="Rosewood"`.</span></span>
7. <span data-ttu-id="ac608-133">**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="ac608-133">Select **OK**.</span></span>
8. <span data-ttu-id="ac608-134">**式** フィールドに、値を入力します。</span><span class="sxs-lookup"><span data-stu-id="ac608-134">In the **Expression** field, type a value.</span></span> <span data-ttu-id="ac608-135">たとえば、`50` と入力します。</span><span class="sxs-lookup"><span data-stu-id="ac608-135">For example, type `50`.</span></span> 
9. <span data-ttu-id="ac608-136">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="ac608-136">Close the page.</span></span>

