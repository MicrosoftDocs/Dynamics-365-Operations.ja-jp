---
title: "製品コンフィギュレーション モデルの計算についてよく寄せられる質問"
description: "この記事では、製品コンフィギュレーション モデルの計算および計算と制約の使用方法について説明します。"
author: cvocph
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: PCConstraintEditor, PCProductConfigurationModelDetails, PCRuntimeConfigurator
audience: Application User
ms.reviewer: YuyuScheller
ms.search.scope: Core, Operations
ms.custom: 19191
ms.assetid: 8993f9a1-d1c0-49f5-afd3-5e1077ded0fe
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: yuyus
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 73de1658ed4f104008ff0654c999bdc2f3bfc8a8
ms.contentlocale: ja-jp
ms.lasthandoff: 11/03/2017

---

# <a name="calculations-for-product-configuration-models-faq"></a><span data-ttu-id="2075c-103">製品コンフィギュレーション モデルの計算についてよく寄せられる質問</span><span class="sxs-lookup"><span data-stu-id="2075c-103">Calculations for product configuration models FAQ</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="2075c-104">この記事では、製品コンフィギュレーション モデルの計算および計算と制約の使用方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="2075c-104">This article describes calculations for product configuration models and explains how to use calculations together with constraints.</span></span>

<span data-ttu-id="2075c-105">計算は、算術または論理工程に使用できます。</span><span class="sxs-lookup"><span data-stu-id="2075c-105">Calculations can be used for arithmetic or logical operations.</span></span> <span data-ttu-id="2075c-106">これらは、製品コンフィギュレーション モデルの式の制約を補足します。</span><span class="sxs-lookup"><span data-stu-id="2075c-106">They complement expression constraints in product configuration models.</span></span> <span data-ttu-id="2075c-107">計算を [**制約ベースの製品コンフィギュレーション モデルの詳細**] ページで定義し、式エディターで計算式を作成できます。</span><span class="sxs-lookup"><span data-stu-id="2075c-107">You can define calculations on the **Constraint-based product configuration model details** page and then build expressions for the calculations in the expression editor.</span></span> <span data-ttu-id="2075c-108">計算の詳細については、「計算の作成」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="2075c-108">For more information, see Create calculations.</span></span>

## <a name="what-is-a-calculation"></a><span data-ttu-id="2075c-109">計算とは</span><span class="sxs-lookup"><span data-stu-id="2075c-109">What is a calculation?</span></span>
<span data-ttu-id="2075c-110">計算とは、製品コンフィギュレーション モデルで使用できる要素のことです。</span><span class="sxs-lookup"><span data-stu-id="2075c-110">A calculation is an element that you can use in a product configuration model.</span></span> <span data-ttu-id="2075c-111">計算は、製品をコンフィギュレーションする際に、小数を使用した値の計算を可能にして、制約を補完します。</span><span class="sxs-lookup"><span data-stu-id="2075c-111">Calculations complement constraints by letting you use decimal numbers to calculate values when you configure a product.</span></span> <span data-ttu-id="2075c-112">さらに、計算には、制約よりも多くの演算子を使用できます。</span><span class="sxs-lookup"><span data-stu-id="2075c-112">Additionally, calculations have a larger set of available operators than constraints have.</span></span>  

<span data-ttu-id="2075c-113">制約と同様に、計算は、製品コンフィギュレーション モデルの特定のコンポーネントに関連付けられ、別のコンポーネントが再利用することも共有することもできません。</span><span class="sxs-lookup"><span data-stu-id="2075c-113">Like a constraint, a calculation is associated with a specific component in a product configuration model, and can’t be reused by or shared with another component.</span></span> <span data-ttu-id="2075c-114">計算と制約の重要な違いの 1 つは、計算は必須 (単一方向) で、制約は宣言です (双方向)。</span><span class="sxs-lookup"><span data-stu-id="2075c-114">One important difference between calculations and constraints is that calculations are imperative (unidirectional), whereas constraints are declarative (bi-directional).</span></span> <span data-ttu-id="2075c-115">制約に関する詳細については、「[式の制約およびテーブル制約](expression-constraints-table-constraints-product-configuration-models.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="2075c-115">For more information about constraints, see [Expression constraints and table constraints](expression-constraints-table-constraints-product-configuration-models.md).</span></span>  

<span data-ttu-id="2075c-116">計算は、ターゲット属性と計算式で構成されます。</span><span class="sxs-lookup"><span data-stu-id="2075c-116">A calculation consists of a target attribute and a calculation expression.</span></span>

## <a name="what-is-a-target-attribute"></a><span data-ttu-id="2075c-117">ターゲット属性とは</span><span class="sxs-lookup"><span data-stu-id="2075c-117">What is a target attribute?</span></span>
<span data-ttu-id="2075c-118">ターゲット属性とは、計算式の結果を受け取る属性のことです。</span><span class="sxs-lookup"><span data-stu-id="2075c-118">A target attribute is an attribute that receives the result of the calculation expression.</span></span>  

<span data-ttu-id="2075c-119">次の式で、ターゲット属性はテーブルクロスの測定です:</span><span class="sxs-lookup"><span data-stu-id="2075c-119">In the following expression, the target attribute is a tablecloth measurement:</span></span>  

<span data-ttu-id="2075c-120">**式:** If\[decimalAttribute1 &lt;= decimalAttribute2, True, False\]</span><span class="sxs-lookup"><span data-stu-id="2075c-120">**Expression:** If\[decimalAttribute1 &lt;= decimalAttribute2, True, False\]</span></span>  

<span data-ttu-id="2075c-121">**DecimalAttribute1** はテーブルの長さで、**decimalAttribute2** はテーブルクロスの長さです。</span><span class="sxs-lookup"><span data-stu-id="2075c-121">**DecimalAttribute1** is the table length, and **decimalAttribute2** is the tablecloth length.</span></span> <span data-ttu-id="2075c-122">この式は、**decimalAttribute2** が **decimalAttribute1** より大きいか等しい場合は **True** 値をターゲット属性に返します。</span><span class="sxs-lookup"><span data-stu-id="2075c-122">The expression returns the value **True** to the target attribute if **decimalAttribute2** is greater than or equal to **decimalAttribute1**.</span></span> <span data-ttu-id="2075c-123">それ以外の場合は、**False** が返されます。</span><span class="sxs-lookup"><span data-stu-id="2075c-123">Otherwise, the expression returns **False**.</span></span> <span data-ttu-id="2075c-124">したがって、テーブルクロスの測定は、テーブルクロスの長さがテーブルの長さに等しいかまたは超える場合に受け入れることができます。</span><span class="sxs-lookup"><span data-stu-id="2075c-124">Therefore, the tablecloth measurement is acceptable if the tablecloth length is the same as or exceeds the length of the table.</span></span>

## <a name="what-attribute-types-can-be-set-to-target-attributes"></a><span data-ttu-id="2075c-125">ターゲット属性に設定できるのはどの属性タイプか</span><span class="sxs-lookup"><span data-stu-id="2075c-125">What attribute types can be set to target attributes?</span></span>
<span data-ttu-id="2075c-126">固定リストのないテキストを除いて、製品コンフィギュレーターでサポートされているすべての属性タイプはターゲット属性に設定できます。</span><span class="sxs-lookup"><span data-stu-id="2075c-126">All attribute types that the product configurator supports can be set to target attributes, except text without a fixed list.</span></span>

## <a name="can-the-value-of-a-target-attribute-restrict-the-values-of-the-input-attributes-in-a-calculation"></a><span data-ttu-id="2075c-127">ターゲット属性の値は計算の入力属性の値を制限できますか</span><span class="sxs-lookup"><span data-stu-id="2075c-127">Can the value of a target attribute restrict the values of the input attributes in a calculation?</span></span>
<span data-ttu-id="2075c-128">計算は一方向なので、ターゲット属性の値は入力属性の値を制限できません。</span><span class="sxs-lookup"><span data-stu-id="2075c-128">No, the value of a target attribute can’t restrict the values of the input attributes, because calculations are unidirectional.</span></span> <span data-ttu-id="2075c-129">したがって、入力属性値の変更に基づいてターゲット属性の値が設定されますが、ターゲットの値を変更しても入力属性の値には影響しません。</span><span class="sxs-lookup"><span data-stu-id="2075c-129">Therefore, the value of the target attribute is set based on changes in the value of the input attributes, but a change in the value of the target doesn’t affect the value of the input attributes.</span></span> <span data-ttu-id="2075c-130">この動作は制約の動作とは異なります。</span><span class="sxs-lookup"><span data-stu-id="2075c-130">This behavior differs from the behavior for constraints.</span></span> <span data-ttu-id="2075c-131">制約は両方の方向で行います。</span><span class="sxs-lookup"><span data-stu-id="2075c-131">Constraints occur in both directions.</span></span>

### <a name="example"></a><span data-ttu-id="2075c-132">例</span><span class="sxs-lookup"><span data-stu-id="2075c-132">Example</span></span>

<span data-ttu-id="2075c-133">次の式では、計算のターゲットは電源コードの長さで、入力値は色です。</span><span class="sxs-lookup"><span data-stu-id="2075c-133">In the following expression, the target for the calculation is the length of a power cord, and the input value is a color:</span></span>  

<span data-ttu-id="2075c-134">**式:** \[If Color == "Green", 1.5, 1.0\]</span><span class="sxs-lookup"><span data-stu-id="2075c-134">**Expression:** \[If Color == "Green", 1.5, 1.0\]</span></span>  

<span data-ttu-id="2075c-135">品目のコンフィギュレーション時、[**Green**] を色の属性の値として指定する場合、電源コードの長さは、**1.5** に設定されます。</span><span class="sxs-lookup"><span data-stu-id="2075c-135">When you configure the item, the length of the power cord is set to **1.5** if you specify **Green** as the value of color attribute.</span></span> <span data-ttu-id="2075c-136">他の色を指定した場合、長さは **1.0** に設定されます。</span><span class="sxs-lookup"><span data-stu-id="2075c-136">If you specify any other color, the length is set to **1.0**.</span></span> <span data-ttu-id="2075c-137">ただし、計算は一方向なので、**1.5** の長さを指定するとき、計算では色の属性値は [**緑**] に設定されません。</span><span class="sxs-lookup"><span data-stu-id="2075c-137">However, because calculations are unidirectional, the calculation doesn't set the value of the color attribute to **Green** if you specify a length of **1.5**.</span></span>

## <a name="what-happens-if-a-calculation-has-a-target-attribute-of-the-integer-type-but-a-calculation-generates-a-decimal-number"></a><span data-ttu-id="2075c-138">計算のターゲット属性が整数タイプで、計算で小数を生成するとき、何が起きますか</span><span class="sxs-lookup"><span data-stu-id="2075c-138">What happens if a calculation has a target attribute of the integer type but a calculation generates a decimal number?</span></span>
<span data-ttu-id="2075c-139">ターゲットの属性が整数タイプで、計算が小数を生成した場合、計算結果の整数部分だけが返されます。</span><span class="sxs-lookup"><span data-stu-id="2075c-139">If a target attribute is of the integer type, but a calculation generates a decimal number, only the integer part of the calculated result is returned.</span></span> <span data-ttu-id="2075c-140">小数部分は削除され、結果を丸められません。</span><span class="sxs-lookup"><span data-stu-id="2075c-140">The decimal part is removed, and the result isn't rounded.</span></span> <span data-ttu-id="2075c-141">たとえば、12.70 の結果は 12 として表示されます。</span><span class="sxs-lookup"><span data-stu-id="2075c-141">For example, a result of 12.70 is shown as 12.</span></span>

## <a name="when-do-calculations-occur"></a><span data-ttu-id="2075c-142">計算はいつ発生しますか</span><span class="sxs-lookup"><span data-stu-id="2075c-142">When do calculations occur?</span></span>
<span data-ttu-id="2075c-143">計算は、すべて入力属性の値が用意されたときに発生します。</span><span class="sxs-lookup"><span data-stu-id="2075c-143">Calculations occur when a value has been provided for all input attributes.</span></span>

## <a name="can-i-overwrite-the-value-that-is-calculated-for-the-target-attribute"></a><span data-ttu-id="2075c-144">ターゲット属性に対して計算された値を上書きできますか</span><span class="sxs-lookup"><span data-stu-id="2075c-144">Can I overwrite the value that is calculated for the target attribute?</span></span>
<span data-ttu-id="2075c-145">ターゲット属性が非表示または読み取り専用に設定されていなければ、ターゲット属性に対して計算された値を上書きできます。</span><span class="sxs-lookup"><span data-stu-id="2075c-145">You can overwrite the value that is calculated for the target attribute, unless the target attribute is set as hidden or read-only.</span></span>

## <a name="how-do-i-set-a-target-attribute-as-hidden-or-readonly"></a><span data-ttu-id="2075c-146">ターゲット属性を非表示または読み取り専用に設定する方法</span><span class="sxs-lookup"><span data-stu-id="2075c-146">How do I set a target attribute as hidden or readonly?</span></span>
<span data-ttu-id="2075c-147">属性を非表示または読み取り専用に設定するには、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="2075c-147">To set an attribute as hidden or read-only, follow these steps.</span></span>

1.  <span data-ttu-id="2075c-148">[**製品情報管理**] &gt; [**共通**] &gt; [**製品コンフィギュレーション モデル**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="2075c-148">Click **Product information management** &gt; **Common** &gt; **Product configuration models**.</span></span>
2.  <span data-ttu-id="2075c-149">製品コンフィギュレーション モデルを選択し、[アクション ペイン] で、[**編集**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="2075c-149">Select a product configuration model, and then, on the Action Pane, click **Edit**.</span></span>
3.  <span data-ttu-id="2075c-150">[**制約ベースの製品コンフィギュレーション モデルの詳細**] ページで、ターゲット属性として使用する属性を選択します。</span><span class="sxs-lookup"><span data-stu-id="2075c-150">On the **Constraint-based product configuration model details** page, select the attribute to use as a target attribute.</span></span>
4.  <span data-ttu-id="2075c-151">[**属性**] クイック タブで、[**非表示**] または [**読み取り専用**] を選択します。</span><span class="sxs-lookup"><span data-stu-id="2075c-151">On the **Attributes** FastTab, select **Hidden** or **Read-only**.</span></span>

## <a name="can-a-calculation-overwrite-the-values-that-i-set"></a><span data-ttu-id="2075c-152">計算はユーザーが設定した値を上書きできますか</span><span class="sxs-lookup"><span data-stu-id="2075c-152">Can a calculation overwrite the values that I set?</span></span>
<span data-ttu-id="2075c-153">一連番号</span><span class="sxs-lookup"><span data-stu-id="2075c-153">No.</span></span> <span data-ttu-id="2075c-154">製品をコンフィギュレーションした際に設定した値が使用される値です。</span><span class="sxs-lookup"><span data-stu-id="2075c-154">The values that you set when you configure a product are the values that are used.</span></span> <span data-ttu-id="2075c-155">計算の入力値を変更したときに行われる計算は、特定の属性に対して与えた値を上書きすることはできません。</span><span class="sxs-lookup"><span data-stu-id="2075c-155">The calculation that occurs when the input values in a calculation are changed can’t overwrite the values that you provide for a specific attribute.</span></span>

## <a name="what-happens-if-i-remove-an-input-value-in-a-calculation"></a><span data-ttu-id="2075c-156">計算の入力値を削除すると、何が発生しますか</span><span class="sxs-lookup"><span data-stu-id="2075c-156">What happens if I remove an input value in a calculation?</span></span>
<span data-ttu-id="2075c-157">計算の入力値を削除すると、ターゲット属性の値も削除されます。</span><span class="sxs-lookup"><span data-stu-id="2075c-157">If you remove an input value in a calculation, the value of the target attribute is also removed.</span></span>

## <a name="why-do-i-receive-an-error-message-that-says-that-my-model-is-in-contradiction"></a><span data-ttu-id="2075c-158">自分のモデルが矛盾しているというエラー メッセージが表示される理由は</span><span class="sxs-lookup"><span data-stu-id="2075c-158">Why do I receive an error message that says that my model is in contradiction?</span></span>
<span data-ttu-id="2075c-159">このメッセージは、計算にエラーがあるか、または矛盾が 1 つ以上の制約に存在する場合に表示されます。</span><span class="sxs-lookup"><span data-stu-id="2075c-159">This message is shown when a calculation includes an error, or when a contradiction exists in one or more constraints.</span></span> <span data-ttu-id="2075c-160">制約での矛盾の詳細については、「[式の制約およびテーブル制約](expression-constraints-table-constraints-product-configuration-models.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="2075c-160">For more information about contradictions in constraints, see [Expression constraints and table constraints](expression-constraints-table-constraints-product-configuration-models.md).</span></span> <span data-ttu-id="2075c-161">次に、計算でエラーが発生する状況を示します。</span><span class="sxs-lookup"><span data-stu-id="2075c-161">Here are some situations where errors can occur in calculations:</span></span>

-   <span data-ttu-id="2075c-162">値を 0 (ゼロ) で割る。</span><span class="sxs-lookup"><span data-stu-id="2075c-162">A value is divided by 0 (zero).</span></span>
-   <span data-ttu-id="2075c-163">次の 2 つの要素間に不一致が存在する。</span><span class="sxs-lookup"><span data-stu-id="2075c-163">A conflict exists between the following two elements:</span></span>
    -   <span data-ttu-id="2075c-164">属性に対して使用できて、制約によって限定されている値。</span><span class="sxs-lookup"><span data-stu-id="2075c-164">The values that are available for an attribute and are limited by a constraint</span></span>
    -   <span data-ttu-id="2075c-165">計算によって生成される値</span><span class="sxs-lookup"><span data-stu-id="2075c-165">A value that is generated by a calculation</span></span>
-   <span data-ttu-id="2075c-166">計算によって返される値が属性の範囲外にある。</span><span class="sxs-lookup"><span data-stu-id="2075c-166">The values that are returned by the calculation are outside the domain of the attribute.</span></span> <span data-ttu-id="2075c-167">例は 0 に計算される \[1..10\] からの整数です。</span><span class="sxs-lookup"><span data-stu-id="2075c-167">An example is an integer from \[1..10\] that is calculated to 0.</span></span>

## <a name="why-do-i-receive-an-error-message-even-though-i-successfully-validated-my-product-model"></a><span data-ttu-id="2075c-168">自分のプロダクト モデルの検証に成功しても、エラー メッセージが出力される理由は</span><span class="sxs-lookup"><span data-stu-id="2075c-168">Why do I receive an error message even though I successfully validated my product model?</span></span>
<span data-ttu-id="2075c-169">計算は検証に含まれていません。</span><span class="sxs-lookup"><span data-stu-id="2075c-169">Calculations aren't included in the validation.</span></span> <span data-ttu-id="2075c-170">計算エラーを探すには、製品コンフィギュレーション モデルをテストする必要があります。</span><span class="sxs-lookup"><span data-stu-id="2075c-170">You must test the product configuration model to find errors in calculations.</span></span> <span data-ttu-id="2075c-171">製品コンフィギュレーション モデルをテストするには、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="2075c-171">To test a product configuration model, follow these steps.</span></span>

1.  <span data-ttu-id="2075c-172">[**製品情報管理**] &gt; [**共通**] &gt; [**製品コンフィギュレーション モデル**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="2075c-172">Click **Product information management** &gt; **Common** &gt; **Product configuration models**.</span></span>
2.  <span data-ttu-id="2075c-173">製品コンフィギュレーション モデルを選択し、[アクション ペイン] で、[**実行**] グループ内の [**テスト**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="2075c-173">Select a product configuration model, and then, on the Action Pane, in the **Run** group, click **Test**.</span></span>





