---
title: コンフィギュレーション可能な製品の属性ベースの価格決定の設定
description: このトピックでは、属性ベースの価格決定の方法を説明します。
author: ShylaThompson
ms.date: 08/20/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: DefaultDashboard, EcoResProductVariantMaintainWorkspace, PCProductConfigurationModelListPage, PCPriceModelList, PCPriceModel, PCConstraintEditor
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 0c30c520e7265c2676937f5191844f6789c364e6
ms.sourcegitcommit: fa99a36c3d30d0c0577fd3f63ed6bf2f71599e40
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/20/2021
ms.locfileid: "5921244"
---
# <a name="set-up-attribute-based-pricing-for-configurable-products"></a><span data-ttu-id="25450-103">コンフィギュレーション可能な製品の属性ベースの価格決定の設定</span><span class="sxs-lookup"><span data-stu-id="25450-103">Set up attribute-based pricing for configurable products</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="25450-104">このトピックでは、属性ベースの価格決定の方法を説明します。</span><span class="sxs-lookup"><span data-stu-id="25450-104">This topic explains how to set up attribute-based pricing.</span></span> <span data-ttu-id="25450-105">前提条件として、1 つ以上のコンポーネントと属性を持つ製品コンフィギュレーション モデルが必要です。</span><span class="sxs-lookup"><span data-stu-id="25450-105">As a prerequisite, you must have a product configuration model that has one or more components and attributes.</span></span> <span data-ttu-id="25450-106">この例では、デモ データの会社 USMF のハイエンド スピーカーの製品モデルが使用されています。</span><span class="sxs-lookup"><span data-stu-id="25450-106">This example uses the High End Speaker product model in the USMF demo data company.</span></span> <span data-ttu-id="25450-107">通常、製品マネージャーがこの手順を使用します。</span><span class="sxs-lookup"><span data-stu-id="25450-107">Typically, a product manager uses this procedure.</span></span>


## <a name="create-a-new-price-model"></a><span data-ttu-id="25450-108">新しい価格モデルの作成</span><span class="sxs-lookup"><span data-stu-id="25450-108">Create a new price model</span></span>

1. <span data-ttu-id="25450-109">**製品情報管理\>製品\>製品コンフィギュレーション モデル** の順にクリックします。</span><span class="sxs-lookup"><span data-stu-id="25450-109">Go to **Product information management \> Products \> Product configuration models**.</span></span>
1. <span data-ttu-id="25450-110">リストで、名前のリンクを選択せずに、**ハイ エンド スピーカー** 行を選択します。</span><span class="sxs-lookup"><span data-stu-id="25450-110">In the list, select the **High End Speaker** line, but don't select the link for the name.</span></span>
1. <span data-ttu-id="25450-111">アクション ウィンドウで、**モデル** を選択します。</span><span class="sxs-lookup"><span data-stu-id="25450-111">On the Action Pane, select **Model**.</span></span>
1. <span data-ttu-id="25450-112">**価格モデル** を選択します。</span><span class="sxs-lookup"><span data-stu-id="25450-112">Select **Price models**.</span></span>
1. <span data-ttu-id="25450-113">**新規** を選択します。</span><span class="sxs-lookup"><span data-stu-id="25450-113">Select **New**.</span></span>
1. <span data-ttu-id="25450-114">**価格モデル名** フィールドに、値を入力します。</span><span class="sxs-lookup"><span data-stu-id="25450-114">In the **Price model name** field, type a value.</span></span> <span data-ttu-id="25450-115">容易にモデルを識別できる名前を使用します。</span><span class="sxs-lookup"><span data-stu-id="25450-115">Use a name that makes the model easy to identify.</span></span>  
1. <span data-ttu-id="25450-116">**説明** フィールドで、値を入力します。</span><span class="sxs-lookup"><span data-stu-id="25450-116">In the **Description** field, type a value.</span></span>
1. <span data-ttu-id="25450-117">**保存** を選択します。</span><span class="sxs-lookup"><span data-stu-id="25450-117">Select **Save**.</span></span>

## <a name="add-price-elements"></a><span data-ttu-id="25450-118">価格要素の追加</span><span class="sxs-lookup"><span data-stu-id="25450-118">Add price elements</span></span>

1. <span data-ttu-id="25450-119">**編集** を選択します。</span><span class="sxs-lookup"><span data-stu-id="25450-119">Select **Edit**.</span></span> <span data-ttu-id="25450-120">製品モデルの各コンポーネントごとに、価格の式のルールの基準価格要素および任意の数字を設定できます。</span><span class="sxs-lookup"><span data-stu-id="25450-120">Each component in a product model can have a base price element and any number of price expression rules.</span></span> <span data-ttu-id="25450-121">異なる通貨でも価格を追加できます。</span><span class="sxs-lookup"><span data-stu-id="25450-121">You can also add prices in different currencies.</span></span>  
2. <span data-ttu-id="25450-122">**基準価格の式** フィールドに、値を入力します。</span><span class="sxs-lookup"><span data-stu-id="25450-122">In the **Base price expression** field, type a value.</span></span> <span data-ttu-id="25450-123">たとえば、「100」と入力します。</span><span class="sxs-lookup"><span data-stu-id="25450-123">For example, type 100.</span></span> <span data-ttu-id="25450-124">基準価格の式は、数値あるいは 1 つ以上の属性を含む算術計算で構成できます。</span><span class="sxs-lookup"><span data-stu-id="25450-124">A base price expression can be a numerical value, or it can consist of an arithmetic calculation that involves one or more attributes.</span></span>  
3. <span data-ttu-id="25450-125">**追加** を選択します。</span><span class="sxs-lookup"><span data-stu-id="25450-125">Select **Add**.</span></span>
4. <span data-ttu-id="25450-126">**名前** フィールドに、`Rosewood` と入力します。</span><span class="sxs-lookup"><span data-stu-id="25450-126">In the **Name** field, type `Rosewood`.</span></span> <span data-ttu-id="25450-127">価格の式の名前は、価格要素が表す内容を識別する場合に役立ちます。</span><span class="sxs-lookup"><span data-stu-id="25450-127">The price expression name helps identify what the price element represents.</span></span> <span data-ttu-id="25450-128">この例では、シタンのスピーカー キャビネットの仕上げオプションに対する価格要素を作成します。</span><span class="sxs-lookup"><span data-stu-id="25450-128">In this example, we are creating a price element for the Rosewood speaker cabinet finish option.</span></span>  
5. <span data-ttu-id="25450-129">**条件の編集** を選択します。</span><span class="sxs-lookup"><span data-stu-id="25450-129">Select **Edit condition**.</span></span> <span data-ttu-id="25450-130">価格の条件によって、属性の特定の組み合わせがある場合にのみ、価格の式の要素を確実に販売価格に含められます。</span><span class="sxs-lookup"><span data-stu-id="25450-130">A price condition helps guarantee that a price expression element is included in the sales price only if a specific combination of attributes is present.</span></span>  
6. <span data-ttu-id="25450-131">**ConstraintBody** フィールドに、`CabinetFinish=="Rosewood"` と入力します。</span><span class="sxs-lookup"><span data-stu-id="25450-131">In the **ConstraintBody** field, enter `CabinetFinish=="Rosewood"`.</span></span>
7. <span data-ttu-id="25450-132">**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="25450-132">Select **OK**.</span></span>
8. <span data-ttu-id="25450-133">**式** フィールドに、値を入力します。</span><span class="sxs-lookup"><span data-stu-id="25450-133">In the **Expression** field, type a value.</span></span> <span data-ttu-id="25450-134">たとえば、`50` と入力します。</span><span class="sxs-lookup"><span data-stu-id="25450-134">For example, type `50`.</span></span> 
9. <span data-ttu-id="25450-135">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="25450-135">Close the page.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]