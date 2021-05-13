---
title: 製品コンフィギュレーション モデルの作成
description: この手順は、製品コンフィギュレーション モデルの作成方法ならびに属性およびサブコンポーネントなどの基本情報の入力方法を示します。
author: ShylaThompson
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: DefaultDashboard, EcoResProductVariantMaintainWorkspace, PCProductConfigurationModelListPage, PCCreateProductConfigurationModel, PCProductConfigurationModelDetails, PCBOMLineDetails
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 2cb9e33d7bab6ca9cd378ec40baa796d1a933ece
ms.sourcegitcommit: fa99a36c3d30d0c0577fd3f63ed6bf2f71599e40
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/20/2021
ms.locfileid: "5921368"
---
# <a name="create-a-product-configuration-model"></a><span data-ttu-id="d897d-103">製品コンフィギュレーション モデルの作成</span><span class="sxs-lookup"><span data-stu-id="d897d-103">Create a product configuration model</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="d897d-104">この手順は、製品コンフィギュレーション モデルの作成方法ならびに属性およびサブコンポーネントなどの基本情報の入力方法を示します。</span><span class="sxs-lookup"><span data-stu-id="d897d-104">This procedure shows how to create a product configuration model and enter basic information such as attributes and subcomponents.</span></span> <span data-ttu-id="d897d-105">この手順の作成に使用するデモ データの会社は USMF です。</span><span class="sxs-lookup"><span data-stu-id="d897d-105">The demo data company used to create this procedure is USMF.</span></span>


## <a name="create-a-product-model"></a><span data-ttu-id="d897d-106">製品モデルの作成</span><span class="sxs-lookup"><span data-stu-id="d897d-106">Create a product model</span></span>

1. <span data-ttu-id="d897d-107">**製品情報管理\>製品\>製品コンフィギュレーション モデル** の順にクリックします。</span><span class="sxs-lookup"><span data-stu-id="d897d-107">Go to **Product information management \> Products \> Product configuration models**.</span></span>
1. <span data-ttu-id="d897d-108">**新規** を選択します。</span><span class="sxs-lookup"><span data-stu-id="d897d-108">Select **New**.</span></span>
1. <span data-ttu-id="d897d-109">**名前** フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="d897d-109">In the **Name** field, type a value.</span></span>
1. <span data-ttu-id="d897d-110">**説明** フィールドで、値を入力します。</span><span class="sxs-lookup"><span data-stu-id="d897d-110">In the **Description** field, type a value.</span></span>
1. <span data-ttu-id="d897d-111">**ソルバー戦略** フィールドで、オプションを選択します。</span><span class="sxs-lookup"><span data-stu-id="d897d-111">In the **Solver strategy** field, select an option.</span></span>
    * <span data-ttu-id="d897d-112">ソルバー戦略によって、制約ベースの製品コンフィギュレーション モデルの制約がどのように処理されるかが決まります。</span><span class="sxs-lookup"><span data-stu-id="d897d-112">The solver strategy determines how the constraints in a constraint-based product configuration model are processed.</span></span> <span data-ttu-id="d897d-113">この選択は、製品コンフィギュレーション モデルのパフォーマンスに影響することがあります。</span><span class="sxs-lookup"><span data-stu-id="d897d-113">This selection can have an impact on the performance of the product configuration model.</span></span>  
1. <span data-ttu-id="d897d-114">**名前** フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="d897d-114">In the **Name** field, type a value.</span></span>
    * <span data-ttu-id="d897d-115">ルート コンポーネントは、製品コンフィギュレーション モデルを表しますが、他の製品モデルでも使用できます。</span><span class="sxs-lookup"><span data-stu-id="d897d-115">The root component represents the product configuration model, but it can also be used in other product models.</span></span>  
1. <span data-ttu-id="d897d-116">**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="d897d-116">Select **OK**.</span></span>
1. <span data-ttu-id="d897d-117">**コンフィギュレーションの再利用** フィールドで、オプションを選択します。</span><span class="sxs-lookup"><span data-stu-id="d897d-117">In the **Reuse configurations** field, select an option.</span></span>
    * <span data-ttu-id="d897d-118">[コンフィギュレーションの再利用] パラメータが [はい] に設定されている場合、システムは、各コンフィギュレーション セッションの後で同一のコンフィギュレーションがあるかどうかを確認し、完全に一致するコンフィギュレーションがあれば再利用します。</span><span class="sxs-lookup"><span data-stu-id="d897d-118">If the reuse configurations parameter is set to Yes, the system will check for identical configurations after each configuration session and reuse if an exact match is found.</span></span>  

## <a name="add-attributes"></a><span data-ttu-id="d897d-119">属性の追加</span><span class="sxs-lookup"><span data-stu-id="d897d-119">Add attributes</span></span>

1. <span data-ttu-id="d897d-120">**属性** セクションを展開します。</span><span class="sxs-lookup"><span data-stu-id="d897d-120">Expand the **Attributes** section.</span></span>
2. <span data-ttu-id="d897d-121">**追加** を選択します。</span><span class="sxs-lookup"><span data-stu-id="d897d-121">Select **Add**.</span></span>
3. <span data-ttu-id="d897d-122">一覧で、選択された行をマークします。</span><span class="sxs-lookup"><span data-stu-id="d897d-122">In the list, mark the selected row.</span></span>
4. <span data-ttu-id="d897d-123">**名前** フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="d897d-123">In the **Name** field, type a value.</span></span>
5. <span data-ttu-id="d897d-124">**ソルバー名** フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="d897d-124">In the **Solver name** field, type a value.</span></span>
    * <span data-ttu-id="d897d-125">ソルバー名は、製品コンフィギュレーターの制約ソルバーで使用されます。</span><span class="sxs-lookup"><span data-stu-id="d897d-125">The solver name is used by the constraint solver of the product configurator.</span></span> <span data-ttu-id="d897d-126">スペースまたは _ (アンダースコア) 以外の特殊文字は含めないようにしてください。</span><span class="sxs-lookup"><span data-stu-id="d897d-126">It must not include spaces or special characters except _ (underscore).</span></span>  
6. <span data-ttu-id="d897d-127">**説明** フィールドで、値を入力します。</span><span class="sxs-lookup"><span data-stu-id="d897d-127">In the **Description** field, type a value.</span></span>
    * <span data-ttu-id="d897d-128">説明テキストはコンフィギュレーション ユーザーに表示されるため、適切な属性値を選択するためのヘルプとして使用できます。</span><span class="sxs-lookup"><span data-stu-id="d897d-128">The description text is displayed to the configuration user and can therefore serve as help in selecting the right attribute value.</span></span>  
7. <span data-ttu-id="d897d-129">**属性タイプ** フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="d897d-129">In the **Attribute type** field, enter or select a value.</span></span>
    * <span data-ttu-id="d897d-130">属性タイプによって、属性で使用できる値が決まります。</span><span class="sxs-lookup"><span data-stu-id="d897d-130">The attribute type determines which values are available for the attribute.</span></span>  
8. <span data-ttu-id="d897d-131">**再利用に含める** チェック ボックスをオンにします。</span><span class="sxs-lookup"><span data-stu-id="d897d-131">Select the **Include in reuse** check box.</span></span>
    * <span data-ttu-id="d897d-132">このオプションは、[コンフィギュレーションの再利用] オプションが選択されている場合にのみ使用できます。</span><span class="sxs-lookup"><span data-stu-id="d897d-132">This option is only available when the Reuse configurations option is selected.</span></span> <span data-ttu-id="d897d-133">[コンフィギュレーションの再利用] チェック ボックスに属性を含めると、システムが完全一致を検索する際にこの属性を考慮することになります。</span><span class="sxs-lookup"><span data-stu-id="d897d-133">Including the attribute in the reuse check box means that this attribute will be considered when the system is looking for an exact match.</span></span>  

## <a name="add-subcomponents"></a><span data-ttu-id="d897d-134">サブコンポーネントを追加</span><span class="sxs-lookup"><span data-stu-id="d897d-134">Add subcomponents</span></span>

1. <span data-ttu-id="d897d-135">**サブコンポーネント** セクションを展開します。</span><span class="sxs-lookup"><span data-stu-id="d897d-135">Expand the **Subcomponents** section.</span></span>
2. <span data-ttu-id="d897d-136">**追加** を選択します。</span><span class="sxs-lookup"><span data-stu-id="d897d-136">Select **Add**.</span></span>
3. <span data-ttu-id="d897d-137">一覧で、選択された行をマークします。</span><span class="sxs-lookup"><span data-stu-id="d897d-137">In the list, mark the selected row.</span></span>
4. <span data-ttu-id="d897d-138">**名前** フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="d897d-138">In the **Name** field, type a value.</span></span>
5. <span data-ttu-id="d897d-139">**ソルバー名** フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="d897d-139">In the **Solver name** field, type a value.</span></span>
6. <span data-ttu-id="d897d-140">**説明** フィールドで、値を入力します。</span><span class="sxs-lookup"><span data-stu-id="d897d-140">In the **Description** field, type a value.</span></span>
7. <span data-ttu-id="d897d-141">**コンポーネント** フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="d897d-141">In the **Component** field, enter or select a value.</span></span>
    * <span data-ttu-id="d897d-142">各サブコンポーネントは、コンポーネント定義を参照する必要があります。</span><span class="sxs-lookup"><span data-stu-id="d897d-142">Each subcomponent must reference a component definition.</span></span> <span data-ttu-id="d897d-143">このデザインは再利用可能コンポーネントをサポートしており、1 回定義したコンポーネントを多くの製品モデルで使用できるようになります。</span><span class="sxs-lookup"><span data-stu-id="d897d-143">This design supports reusable components and ensures that once a component has been defined it can be used in many product models.</span></span>  
8. <span data-ttu-id="d897d-144">**保存** を選択します。</span><span class="sxs-lookup"><span data-stu-id="d897d-144">Select **Save**.</span></span>
9. <span data-ttu-id="d897d-145">**BOM 明細行の詳細** を選択します。</span><span class="sxs-lookup"><span data-stu-id="d897d-145">Select **BOM line details**.</span></span>
    * <span data-ttu-id="d897d-146">"BOM 明細行の詳細" フォームでは、サブコンポーネントで必要なプロパティをユーザーが選択できます。</span><span class="sxs-lookup"><span data-stu-id="d897d-146">The BOM line details form enables the user to select the required properties for the subcomponent.</span></span> <span data-ttu-id="d897d-147">各プロパティには、固定値を指定するか、属性にマップできます。</span><span class="sxs-lookup"><span data-stu-id="d897d-147">Each property can be given a fixed value or mapped to an attribute.</span></span> <span data-ttu-id="d897d-148">属性へのマッピングを行うと、コンフィギュレーションの選択に応じて、異なる値が BOM 明細行プロパティに割り当てられることになります。</span><span class="sxs-lookup"><span data-stu-id="d897d-148">Mapping to an attribute will result in the BOM line property getting different values depending on the configuration selection.</span></span>  
10. <span data-ttu-id="d897d-149">**品目番号グループ** フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="d897d-149">In the **Item number** field, enter or select a value.</span></span>
    * <span data-ttu-id="d897d-150">各サブコンポーネントは、制約ベースのコンフィギュレーション テクノロジを使用したコンフィギュレーション可能な製品マスターを表します。</span><span class="sxs-lookup"><span data-stu-id="d897d-150">Each subcomponent represents a configurable product master with constraint-based configuration technology.</span></span> <span data-ttu-id="d897d-151">参照は、品目番号を使用して行われます。</span><span class="sxs-lookup"><span data-stu-id="d897d-151">The reference is made through the item number.</span></span>  
11. <span data-ttu-id="d897d-152">**設定** チェック ボックスを選択します。</span><span class="sxs-lookup"><span data-stu-id="d897d-152">Select the **Set** check box.</span></span>
12. <span data-ttu-id="d897d-153">**計算** フィールドで、**はい** を選択します。</span><span class="sxs-lookup"><span data-stu-id="d897d-153">Select **Yes** in the **Calculation** field.</span></span>
    * <span data-ttu-id="d897d-154">計算オプションを設定して、製品の原価計算を実行するときに製品が含まれるようにします。</span><span class="sxs-lookup"><span data-stu-id="d897d-154">Setting the calculation option ensures that the product will be included when running a cost calculation for the product.</span></span>  
13. <span data-ttu-id="d897d-155">**設定** タブを選択します。</span><span class="sxs-lookup"><span data-stu-id="d897d-155">Select the **Setup** tab.</span></span>
14. <span data-ttu-id="d897d-156">**設定** チェック ボックスを選択します。</span><span class="sxs-lookup"><span data-stu-id="d897d-156">Select the **Set** check box.</span></span>
15. <span data-ttu-id="d897d-157">**数量** フィールドに、数値を入力します。</span><span class="sxs-lookup"><span data-stu-id="d897d-157">In the **Quantity** field, enter a number.</span></span>
    * <span data-ttu-id="d897d-158">数量フィールドは、構成済製品にこの製品が消費される量を決定します。</span><span class="sxs-lookup"><span data-stu-id="d897d-158">The quantity field determines how much of this product will be consumed in the configured product.</span></span>  
16. <span data-ttu-id="d897d-159">**設定** チェック ボックスを選択します。</span><span class="sxs-lookup"><span data-stu-id="d897d-159">Select the **Set** check box.</span></span>
17. <span data-ttu-id="d897d-160">**生産数** フィールドに数値を入力します。</span><span class="sxs-lookup"><span data-stu-id="d897d-160">In the **Per series** field, enter a number.</span></span>
18. <span data-ttu-id="d897d-161">**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="d897d-161">Select **OK**.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]