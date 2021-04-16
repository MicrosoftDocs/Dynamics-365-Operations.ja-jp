---
title: 製品の構成モデルの計算
description: このトピックでは、製品の構成モデルの属性の計算を作成する方法について説明します
author: t-benebo
ms.date: 03/18/2021
ms.topic: article
ms.search.form: PCProductConfigurationModelListPage, PCProductConfigurationModelDetails
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2021-03-18
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: eaf6264f060d33575740ad38e7a65158baba296b
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/01/2021
ms.locfileid: "5829621"
---
# <a name="product-configuration-model-calculations"></a><span data-ttu-id="30a20-103">製品の構成モデルの計算</span><span class="sxs-lookup"><span data-stu-id="30a20-103">Product configuration model calculations</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="30a20-104">このトピックでは、製品の構成モデルの属性の計算を作成する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="30a20-104">This topic describes how to create calculations for attributes in a product configuration model.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="30a20-105">必要条件</span><span class="sxs-lookup"><span data-stu-id="30a20-105">Prerequisites</span></span>

<span data-ttu-id="30a20-106">製品の構成モデルで計算を使用して、製品の構成値を計算することもできます。</span><span class="sxs-lookup"><span data-stu-id="30a20-106">Calculations are used in a product configuration model to calculate the configuration values for a product.</span></span> <span data-ttu-id="30a20-107">計算の設定を開始する前に、関連する製品の構成モデルが存在している必要があります。</span><span class="sxs-lookup"><span data-stu-id="30a20-107">Before you can start to set up calculations, the related product configuration model must exist.</span></span> <span data-ttu-id="30a20-108">構成モデルの設定プロセスの概要と関連するタスクについては、[製品構成モデルの設定](set-up-maintain-product-configuration-model.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="30a20-108">For an overview of the setup process for configuration models and the related tasks, see [Set up a product configuration model](set-up-maintain-product-configuration-model.md).</span></span>

## <a name="create-a-calculation"></a><span data-ttu-id="30a20-109">計算の作成</span><span class="sxs-lookup"><span data-stu-id="30a20-109">Create a calculation</span></span>

<span data-ttu-id="30a20-110">計算は、式とターゲットとなる属性で構成されます。</span><span class="sxs-lookup"><span data-stu-id="30a20-110">A calculation consists of an expression and a target attribute.</span></span> <span data-ttu-id="30a20-111">詳細については、[製品構成モデルの計算方法の FAQ](calculate-product-configuration-models.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="30a20-111">For more information, see [Calculations for product configuration models FAQ](calculate-product-configuration-models.md).</span></span>

<span data-ttu-id="30a20-112">既存の製品モデルの計算を作成するには、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="30a20-112">To create a calculation for an existing product model, follow these steps.</span></span>

1. <span data-ttu-id="30a20-113">**製品情報管理 \> 共通 \> 製品構成モデル** に移動します。</span><span class="sxs-lookup"><span data-stu-id="30a20-113">Go to **Product information management \> Common \> Product configuration models**.</span></span>
1. <span data-ttu-id="30a20-114">製品の構成モデルを選択し、**編集** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="30a20-114">Open a product configuration model, and then select **Edit**.</span></span>
1. <span data-ttu-id="30a20-115">**計算** クイック タブで、**追加** を選択して計算を追加し、次のフィールドを設定します :</span><span class="sxs-lookup"><span data-stu-id="30a20-115">On the **Calculations** FastTab, select **Add** to add a calculation, and then set the following fields:</span></span>

    - <span data-ttu-id="30a20-116">**名前** – 計算の名前を入力します。</span><span class="sxs-lookup"><span data-stu-id="30a20-116">**Name** – Enter a name for the calculation.</span></span>
    - <span data-ttu-id="30a20-117">**説明** – 計算の説明を入力します。</span><span class="sxs-lookup"><span data-stu-id="30a20-117">**Description** – Enter a description of the calculation.</span></span>
    - <span data-ttu-id="30a20-118">**目標属性** - 計算の対象となる属性を選択します。</span><span class="sxs-lookup"><span data-stu-id="30a20-118">**Target attribute** – Select the attribute that you're making the calculation for.</span></span>

1. <span data-ttu-id="30a20-119">**式の編集** を選択します。</span><span class="sxs-lookup"><span data-stu-id="30a20-119">Select **Edit expression**.</span></span>
1. <span data-ttu-id="30a20-120">**計算の入力** ダイアログ ボックスで、必要な属性、演算子、値を式に追加します。</span><span class="sxs-lookup"><span data-stu-id="30a20-120">In the **Enter a calculation** dialog box, add the required attributes, operators, and values to the expression.</span></span> <span data-ttu-id="30a20-121">これら要素の使用方法の詳細については、[製品構成モデルにおける式の制約およびテーブル制約](expression-constraints-table-constraints-product-configuration-models.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="30a20-121">For more information about how to work with these elements, see [Expression constraints and table constraints in product configuration models](expression-constraints-table-constraints-product-configuration-models.md).</span></span>
1. <span data-ttu-id="30a20-122">式の準備の完了後、**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="30a20-122">When your expression is ready, select **OK**.</span></span>

## <a name="calculation-examples"></a><span data-ttu-id="30a20-123">計算の例</span><span class="sxs-lookup"><span data-stu-id="30a20-123">Calculation examples</span></span>

<span data-ttu-id="30a20-124">このセクションでは、計算の機能を示すいくつかの例を示します。</span><span class="sxs-lookup"><span data-stu-id="30a20-124">This section provides a few examples that show how calculations work.</span></span>

### <a name="example-1"></a><span data-ttu-id="30a20-125">例 1</span><span class="sxs-lookup"><span data-stu-id="30a20-125">Example 1</span></span>

<span data-ttu-id="30a20-126">次の例では、ターゲットの属性はブール型で、次の条件式を使用しています :</span><span class="sxs-lookup"><span data-stu-id="30a20-126">The target attribute is Boolean, and the calculation uses the following conditional expression:</span></span>

`If[(decimalAttribute1 / decimalAttribute2) < 1, True, False]`

<span data-ttu-id="30a20-127">この式は、`decimalAttribute2` が `decimalAttribute1` より大きいか等しい場合は *True* 値をターゲット属性に返します。</span><span class="sxs-lookup"><span data-stu-id="30a20-127">This expression returns a value of *True* to the target attribute if `decimalAttribute2` is greater than or equal to `decimalAttribute1`.</span></span> <span data-ttu-id="30a20-128">それ以外の場合は、*False* のブール値が返されます。</span><span class="sxs-lookup"><span data-stu-id="30a20-128">Otherwise, it returns a value of *False*.</span></span>

### <a name="example-2"></a><span data-ttu-id="30a20-129">例 2</span><span class="sxs-lookup"><span data-stu-id="30a20-129">Example 2</span></span>

<span data-ttu-id="30a20-130">この例では、テキスト属性 `textFixedList` をターゲット属性として使用します。</span><span class="sxs-lookup"><span data-stu-id="30a20-130">This example uses the text attribute `textFixedList` as the target attribute.</span></span> <span data-ttu-id="30a20-131">この属性には、次の固定リストが含まれます。</span><span class="sxs-lookup"><span data-stu-id="30a20-131">This attribute contains the following fixed list.</span></span>

| <span data-ttu-id="30a20-132">先頭値</span><span class="sxs-lookup"><span data-stu-id="30a20-132">Value</span></span> | <span data-ttu-id="30a20-133">ソルバー値</span><span class="sxs-lookup"><span data-stu-id="30a20-133">Solver value</span></span> |
|---|---|
| <span data-ttu-id="30a20-134">A</span><span class="sxs-lookup"><span data-stu-id="30a20-134">A</span></span> | <span data-ttu-id="30a20-135">1a</span><span class="sxs-lookup"><span data-stu-id="30a20-135">1a</span></span> |
| <span data-ttu-id="30a20-136">B</span><span class="sxs-lookup"><span data-stu-id="30a20-136">B</span></span> | <span data-ttu-id="30a20-137">2b</span><span class="sxs-lookup"><span data-stu-id="30a20-137">2b</span></span> |
| <span data-ttu-id="30a20-138">貸方</span><span class="sxs-lookup"><span data-stu-id="30a20-138">C</span></span> | <span data-ttu-id="30a20-139">2c</span><span class="sxs-lookup"><span data-stu-id="30a20-139">2c</span></span> |

<span data-ttu-id="30a20-140">次のスクリーンショットは、この属性の設定がご利用のシステムでどのように表示されるかを示しています。</span><span class="sxs-lookup"><span data-stu-id="30a20-140">The following screenshot shows how the settings for this attribute might look in your system.</span></span>

<span data-ttu-id="30a20-141">![例 2 で使用する属性タイプの設定](media/model-calculations-example2.png "例 2 で使用する属性タイプの設定")</span><span class="sxs-lookup"><span data-stu-id="30a20-141">![Attribute type settings for example 2](media/model-calculations-example2.png "Attribute type settings for example 2")</span></span>

<span data-ttu-id="30a20-142">この属性は、次の条件付きステートメントで使用されます :</span><span class="sxs-lookup"><span data-stu-id="30a20-142">The attribute is used in the following conditional statement:</span></span>

`If[integerAttribute < 150, 0, 2]`

<span data-ttu-id="30a20-143">`integerAttribute` が 150未満の場合、このステートメントは固定リスト *A* の最初のレコードのテキスト値 を返します。それ以外の場合は、固定リスト *C* の 3 番目のレコードのテキスト値を返 します。</span><span class="sxs-lookup"><span data-stu-id="30a20-143">If `integerAttribute` is less than 150, this statement returns the text value of the first record in the fixed list, *A*. Otherwise, it returns the text value of the third record in the fixed list, *C*.</span></span>

> [!NOTE]
> <span data-ttu-id="30a20-144">固定リストはゼロ ベースのリスト (enum) と同等であり、その値は適切な整数値によってアクセスされます。</span><span class="sxs-lookup"><span data-stu-id="30a20-144">The fixed list is equivalent to a zero-based enumeration (enum), and its values are accessed by the appropriate integer value.</span></span> <span data-ttu-id="30a20-145">したがって、最初の固定リスト値 (*A*) は *0* に、2番目の値 (*B*) は *1* に、3番目の値 (*C*) は *2* に一致します。</span><span class="sxs-lookup"><span data-stu-id="30a20-145">Therefore, the first fixed list value (*A*) is matched to *0*, the second value (*B*) is matched to *1*, and the third value (*C*) is matched to *2*.</span></span>

### <a name="example-3"></a><span data-ttu-id="30a20-146">例 3</span><span class="sxs-lookup"><span data-stu-id="30a20-146">Example 3</span></span>

<span data-ttu-id="30a20-147">この例では、前述の例の `textFixedList` ターゲット属性を使用しています。</span><span class="sxs-lookup"><span data-stu-id="30a20-147">This example uses the `textFixedList` target attribute from the previous example.</span></span> <span data-ttu-id="30a20-148">また、もうひとつのテキスト属性である `textAttribute` を使用しており、その中には以下の固定リストが含まれています。</span><span class="sxs-lookup"><span data-stu-id="30a20-148">It also uses another text attribute, `textAttribute`, that contains the following fixed list.</span></span>

| <span data-ttu-id="30a20-149">先頭値</span><span class="sxs-lookup"><span data-stu-id="30a20-149">Value</span></span> | <span data-ttu-id="30a20-150">ソルバー値</span><span class="sxs-lookup"><span data-stu-id="30a20-150">Solver value</span></span> |
|---|---|
| <span data-ttu-id="30a20-151">AA</span><span class="sxs-lookup"><span data-stu-id="30a20-151">AA</span></span> | <span data-ttu-id="30a20-152">1aa</span><span class="sxs-lookup"><span data-stu-id="30a20-152">1aa</span></span> |
| <span data-ttu-id="30a20-153">BB</span><span class="sxs-lookup"><span data-stu-id="30a20-153">BB</span></span> | <span data-ttu-id="30a20-154">2bb</span><span class="sxs-lookup"><span data-stu-id="30a20-154">2bb</span></span> |

<span data-ttu-id="30a20-155">次のスクリーンショットは、この属性の設定がご利用のシステムでどのように表示されるかを示しています。</span><span class="sxs-lookup"><span data-stu-id="30a20-155">The following screenshot shows how the settings for this attribute might look in your system.</span></span>

<span data-ttu-id="30a20-156">![例 3 で使用する属性タイプの設定](media/model-calculations-example3.png "例 3 で使用する属性タイプの設定")</span><span class="sxs-lookup"><span data-stu-id="30a20-156">![Attribute type settings for example 3](media/model-calculations-example3.png "Attribute type settings for example 3")</span></span>

<span data-ttu-id="30a20-157">`textFixedList` 属性の値は、以下の条件付きステートメントを用いて算出されます :</span><span class="sxs-lookup"><span data-stu-id="30a20-157">The value for the `textFixedList` attribute is calculated by using the following conditional statement:</span></span>

`If[textAttribute == "1aa", 0, 2]`

<span data-ttu-id="30a20-158">`textAttribute` の値が *1aa* に相当するソルバー値を持つ場合、この式は、 `textFixedList` 固定リストの最初のレコードである *A* のテキスト値を返します。それ以外の場合は、`textFixedList` 固定リストの3番目のレコード、*C* のテキスト値を返します。</span><span class="sxs-lookup"><span data-stu-id="30a20-158">If the `textAttribute` value has a solver value that equals *1aa*, this expression returns the text value of the first record in the `textFixedList` fixed list, *A*. Otherwise, it returns the text value of the third record in the `textFixedList` fixed list, *C*.</span></span>

> [!NOTE]
> - <span data-ttu-id="30a20-159">条件付きステートメントは、属性のオプションの値を使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="30a20-159">The conditional statement must use the solver value of the attribute.</span></span>
> - <span data-ttu-id="30a20-160">計算に使用できるのは、固定リストのテキスト属性のみです。</span><span class="sxs-lookup"><span data-stu-id="30a20-160">Only fixed-list text attributes can be used in calculations.</span></span>

## <a name="see-also"></a><span data-ttu-id="30a20-161">参照</span><span class="sxs-lookup"><span data-stu-id="30a20-161">See also</span></span>

- [<span data-ttu-id="30a20-162">製品コンフィギュレーション モデルの計算についてよく寄せられる質問</span><span class="sxs-lookup"><span data-stu-id="30a20-162">Calculations for product configuration models FAQ</span></span>](calculate-product-configuration-models.md)
- [<span data-ttu-id="30a20-163">製品コンフィギュレーション モデルへ式の制約の追加</span><span class="sxs-lookup"><span data-stu-id="30a20-163">Add an expression constraint to a product configuration model</span></span>](tasks/add-expression-constraint-product-configuration-model.md)
- [<span data-ttu-id="30a20-164">製品コンフィギュレーション モデルの概要</span><span class="sxs-lookup"><span data-stu-id="30a20-164">Product configuration models overview</span></span>](product-configuration-models.md)
