--- 
title: "製品コンフィギュレーション モデルの作成"
description: "この手順は、製品コンフィギュレーション モデルの作成方法ならびに属性およびサブコンポーネントなどの基本情報の入力方法を示します。"
author: BibiSp
manager: AnnBe
ms.date: 03/02/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bis
ms.search.scope: Operations
ms.search.region: Global
ms.author: bis
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 866a4f29723e10eb0a1e1be86d6d4f6da8a69b1c
ms.contentlocale: ja-jp
ms.lasthandoff: 09/29/2017

---
# <a name="create-a-product-configuration-model"></a><span data-ttu-id="60b60-103">製品コンフィギュレーション モデルの作成</span><span class="sxs-lookup"><span data-stu-id="60b60-103">Create a product configuration model</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="60b60-104">この手順は、製品コンフィギュレーション モデルの作成方法ならびに属性およびサブコンポーネントなどの基本情報の入力方法を示します。</span><span class="sxs-lookup"><span data-stu-id="60b60-104">This procedure shows how to create a product configuration model and enter basic information such as attributes and subcomponents.</span></span> <span data-ttu-id="60b60-105">この手順の作成に使用するデモ データの会社は USMF です。</span><span class="sxs-lookup"><span data-stu-id="60b60-105">The demo data company used to create this procedure is USMF.</span></span>


## <a name="create-a-product-model"></a><span data-ttu-id="60b60-106">製品モデルの作成</span><span class="sxs-lookup"><span data-stu-id="60b60-106">Create a product model</span></span>
1. <span data-ttu-id="60b60-107">[製品バリアント モデルの定義] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="60b60-107">Click Product variant model definition.</span></span>
2. <span data-ttu-id="60b60-108">[製品コンフィギュレーション モデル] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="60b60-108">Click Product configuration models.</span></span>
3. <span data-ttu-id="60b60-109">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="60b60-109">Click New.</span></span>
4. <span data-ttu-id="60b60-110">[名前] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="60b60-110">In the Name field, type a value.</span></span>
5. <span data-ttu-id="60b60-111">[説明] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="60b60-111">In the Description field, type a value.</span></span>
6. <span data-ttu-id="60b60-112">[ソルバー戦略] フィールドで、オプションを選択します。</span><span class="sxs-lookup"><span data-stu-id="60b60-112">In the Solver strategy field, select an option.</span></span>
    * <span data-ttu-id="60b60-113">ソルバー戦略によって、制約ベースの製品コンフィギュレーション モデルの制約がどのように処理されるかが決まります。</span><span class="sxs-lookup"><span data-stu-id="60b60-113">The solver strategy determines how the constraints in a constraint-based product configuration model are processed.</span></span> <span data-ttu-id="60b60-114">この選択は、製品コンフィギュレーション モデルのパフォーマンスに影響することがあります。</span><span class="sxs-lookup"><span data-stu-id="60b60-114">This selection can have an impact on the performance of the product configuration model.</span></span>  
7. <span data-ttu-id="60b60-115">[名前] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="60b60-115">In the Name field, type a value.</span></span>
    * <span data-ttu-id="60b60-116">ルート コンポーネントは、製品コンフィギュレーション モデルを表しますが、他の製品モデルでも使用できます。</span><span class="sxs-lookup"><span data-stu-id="60b60-116">The root component represents the product configuration model, but it can also be used in other product models.</span></span>  
8. <span data-ttu-id="60b60-117">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="60b60-117">Click OK.</span></span>
9. <span data-ttu-id="60b60-118">[コンフィギュレーションの再利用] フィールドで、オプションを選択します。</span><span class="sxs-lookup"><span data-stu-id="60b60-118">In the Reuse configurations field, select an option.</span></span>
    * <span data-ttu-id="60b60-119">[コンフィギュレーションの再利用] パラメータが [はい] に設定されている場合、システムは、各コンフィギュレーション セッションの後で同一のコンフィギュレーションがあるかどうかを確認し、完全に一致するコンフィギュレーションがあれば再利用します。</span><span class="sxs-lookup"><span data-stu-id="60b60-119">If the reuse configurations parameter is set to Yes, the system will check for identical configurations after each configuration session and reuse if an exact match is found.</span></span>  

## <a name="add-attributes"></a><span data-ttu-id="60b60-120">属性の追加</span><span class="sxs-lookup"><span data-stu-id="60b60-120">Add attributes</span></span>
1. <span data-ttu-id="60b60-121">[属性] セクションを展開します。</span><span class="sxs-lookup"><span data-stu-id="60b60-121">Expand the Attributes section.</span></span>
2. <span data-ttu-id="60b60-122">[追加] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="60b60-122">Click Add.</span></span>
3. <span data-ttu-id="60b60-123">一覧で、選択された行をマークします。</span><span class="sxs-lookup"><span data-stu-id="60b60-123">In the list, mark the selected row.</span></span>
4. <span data-ttu-id="60b60-124">[名前] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="60b60-124">In the Name field, type a value.</span></span>
5. <span data-ttu-id="60b60-125">[ソルバー名] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="60b60-125">In the Solver name field, type a value.</span></span>
    * <span data-ttu-id="60b60-126">ソルバー名は、製品コンフィギュレーターの制約ソルバーで使用されます。</span><span class="sxs-lookup"><span data-stu-id="60b60-126">The Solver name is used by the constraint solver of the product configurator.</span></span> <span data-ttu-id="60b60-127">スペースまたは _ (アンダースコア) 以外の特殊文字は含めないようにしてください。</span><span class="sxs-lookup"><span data-stu-id="60b60-127">It must not include spaces or special characters except _ (underscore).</span></span>  
6. <span data-ttu-id="60b60-128">[説明] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="60b60-128">In the Description field, type a value.</span></span>
    * <span data-ttu-id="60b60-129">説明テキストはコンフィギュレーション ユーザーに表示されるため、適切な属性値を選択するためのヘルプとして使用できます。</span><span class="sxs-lookup"><span data-stu-id="60b60-129">The description text is displayed to the configuration user and can therefore serve as help in selecting the right attribute value.</span></span>  
7. <span data-ttu-id="60b60-130">[属性タイプ] フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="60b60-130">In the Attribute type field, enter or select a value.</span></span>
    * <span data-ttu-id="60b60-131">属性タイプによって、属性で使用できる値が決まります。</span><span class="sxs-lookup"><span data-stu-id="60b60-131">The attribute type determines which values are available for the attribute.</span></span>  
8. <span data-ttu-id="60b60-132">[再利用に含める] チェック ボックスを選択します。</span><span class="sxs-lookup"><span data-stu-id="60b60-132">Select the Include in reuse check box.</span></span>
    * <span data-ttu-id="60b60-133">このオプションは、[コンフィギュレーションの再利用] オプションが選択されている場合にのみ使用できます。</span><span class="sxs-lookup"><span data-stu-id="60b60-133">This option is only available when the Reuse configurations option is selected.</span></span> <span data-ttu-id="60b60-134">[コンフィギュレーションの再利用] チェック ボックスに属性を含めると、システムが完全一致を検索する際にこの属性を考慮することになります。</span><span class="sxs-lookup"><span data-stu-id="60b60-134">Including the attribute in the reuse check box means that this attribute will be considered when the system is looking for an exact match.</span></span>  

## <a name="add-subcomponents"></a><span data-ttu-id="60b60-135">サブコンポーネントを追加</span><span class="sxs-lookup"><span data-stu-id="60b60-135">Add subcomponents</span></span>
1. <span data-ttu-id="60b60-136">[サブコンポーネント] セクションを展開します。</span><span class="sxs-lookup"><span data-stu-id="60b60-136">Expand the Subcomponents section.</span></span>
2. <span data-ttu-id="60b60-137">[追加] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="60b60-137">Click Add.</span></span>
3. <span data-ttu-id="60b60-138">一覧で、選択された行をマークします。</span><span class="sxs-lookup"><span data-stu-id="60b60-138">In the list, mark the selected row.</span></span>
4. <span data-ttu-id="60b60-139">[名前] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="60b60-139">In the Name field, type a value.</span></span>
5. <span data-ttu-id="60b60-140">[ソルバー名] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="60b60-140">In the Solver name field, type a value.</span></span>
6. <span data-ttu-id="60b60-141">[説明] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="60b60-141">In the Description field, type a value.</span></span>
7. <span data-ttu-id="60b60-142">[コンポーネント] フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="60b60-142">In the Component field, enter or select a value.</span></span>
    * <span data-ttu-id="60b60-143">各サブコンポーネントは、コンポーネント定義を参照する必要があります。</span><span class="sxs-lookup"><span data-stu-id="60b60-143">Each subcomponent must reference a component definition.</span></span> <span data-ttu-id="60b60-144">このデザインは再利用可能コンポーネントをサポートしており、1 回定義したコンポーネントを多くの製品モデルで使用できるようになります。</span><span class="sxs-lookup"><span data-stu-id="60b60-144">This design supports reusable components and ensures that once a component has been defined it can be used in many product models.</span></span>  
8. <span data-ttu-id="60b60-145">[保存] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="60b60-145">Click Save.</span></span>
9. <span data-ttu-id="60b60-146">[BOM 明細行の詳細] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="60b60-146">Click BOM line details.</span></span>
    * <span data-ttu-id="60b60-147">"BOM 明細行の詳細" フォームでは、サブコンポーネントで必要なプロパティをユーザーが選択できます。</span><span class="sxs-lookup"><span data-stu-id="60b60-147">The BOM line details form enables the user to select the required properties for the subcomponent.</span></span> <span data-ttu-id="60b60-148">各プロパティには、固定値を指定するか、属性にマップできます。</span><span class="sxs-lookup"><span data-stu-id="60b60-148">Each property can be given a fixed value or mapped to an attribute.</span></span> <span data-ttu-id="60b60-149">属性へのマッピングを行うと、コンフィギュレーションの選択に応じて、異なる値が BOM 明細行プロパティに割り当てられることになります。</span><span class="sxs-lookup"><span data-stu-id="60b60-149">Mapping to an attribute will result in the BOM line property getting different values depending on the configuration selection.</span></span>  
10. <span data-ttu-id="60b60-150">[品目番号] フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="60b60-150">In the Item number field, enter or select a value.</span></span>
    * <span data-ttu-id="60b60-151">各サブコンポーネントは、制約ベースのコンフィギュレーション テクノロジを使用したコンフィギュレーション可能な製品マスターを表します。</span><span class="sxs-lookup"><span data-stu-id="60b60-151">Each subcomponent represents a configurable product master with constraint-based configuration technology.</span></span> <span data-ttu-id="60b60-152">参照は、品目番号を使用して行われます。</span><span class="sxs-lookup"><span data-stu-id="60b60-152">The reference is made through the item number.</span></span>  
11. <span data-ttu-id="60b60-153">[設定] チェック ボックスを選択します。</span><span class="sxs-lookup"><span data-stu-id="60b60-153">Select the Set check box.</span></span>
12. <span data-ttu-id="60b60-154">[計算] フィールドで、[はい] を選択します。</span><span class="sxs-lookup"><span data-stu-id="60b60-154">Select Yes in the Calculation field.</span></span>
    * <span data-ttu-id="60b60-155">計算オプションを設定して、製品の原価計算を実行するときに製品が含まれるようにします。</span><span class="sxs-lookup"><span data-stu-id="60b60-155">Setting the calculation option ensures that the product will be included when running a cost calculation for the product.</span></span>  
13. <span data-ttu-id="60b60-156">[設定] タブをクリックします。</span><span class="sxs-lookup"><span data-stu-id="60b60-156">Click the Setup tab.</span></span>
14. <span data-ttu-id="60b60-157">[設定] チェック ボックスを選択します。</span><span class="sxs-lookup"><span data-stu-id="60b60-157">Select the Set check box.</span></span>
15. <span data-ttu-id="60b60-158">[数量] フィールドに数値を入力します。</span><span class="sxs-lookup"><span data-stu-id="60b60-158">In the Quantity field, enter a number.</span></span>
    * <span data-ttu-id="60b60-159">数量フィールドは、構成済製品にこの製品が消費される量を決定します。</span><span class="sxs-lookup"><span data-stu-id="60b60-159">The quantity field determines how much of this product will be consumed in the configured product.</span></span>  
16. <span data-ttu-id="60b60-160">[設定] チェック ボックスを選択します。</span><span class="sxs-lookup"><span data-stu-id="60b60-160">Select the Set check box.</span></span>
17. <span data-ttu-id="60b60-161">[生産数] フィールドに数値を入力します。</span><span class="sxs-lookup"><span data-stu-id="60b60-161">In the Per series field, enter a number.</span></span>
18. <span data-ttu-id="60b60-162">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="60b60-162">Click OK.</span></span>


