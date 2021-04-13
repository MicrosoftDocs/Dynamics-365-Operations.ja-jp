---
title: X++ 演算子
description: このトピックでは、X++ でサポートされている演算子について説明します。
author: RobinARH
ms.date: 12/02/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Developer
ms.reviewer: rhaertle
ms.custom: 150373
ms.search.region: Global
ms.author: rhaertle
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: a384adb80649e7149db4d545fcfc2d40135c2b0d
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/31/2021
ms.locfileid: "5749926"
---
# <a name="x-operators"></a><span data-ttu-id="1d6ee-103">X++ 演算子</span><span class="sxs-lookup"><span data-stu-id="1d6ee-103">X++ operators</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="1d6ee-104">このトピックでは、X++ でサポートされている演算子について説明します。</span><span class="sxs-lookup"><span data-stu-id="1d6ee-104">This topic describes the operators supported in X++.</span></span>

## <a name="assignment-operators"></a><span data-ttu-id="1d6ee-105">代入演算子</span><span class="sxs-lookup"><span data-stu-id="1d6ee-105">Assignment operators</span></span>

<span data-ttu-id="1d6ee-106">割り当ては、変数やフィールドの値を変更します。</span><span class="sxs-lookup"><span data-stu-id="1d6ee-106">An assignment changes the value of a variable or field.</span></span> <span data-ttu-id="1d6ee-107">次のテーブルは、X++ の代入演算子を示しています。</span><span class="sxs-lookup"><span data-stu-id="1d6ee-107">The following table shows the X++ assignment operators.</span></span> <span data-ttu-id="1d6ee-108">接頭辞と接尾辞の演算子には違いはありません。</span><span class="sxs-lookup"><span data-stu-id="1d6ee-108">There is no difference between prefix and postfix operators.</span></span>

| <span data-ttu-id="1d6ee-109">オペレーター</span><span class="sxs-lookup"><span data-stu-id="1d6ee-109">Operator</span></span>   | <span data-ttu-id="1d6ee-110">説明</span><span class="sxs-lookup"><span data-stu-id="1d6ee-110">Description</span></span>                                                                                      |
|------------|--------------------------------------------------------------------------------------------------|
| `=`        | <span data-ttu-id="1d6ee-111">等号の右側の式を左側の変数に割り当てます。</span><span class="sxs-lookup"><span data-stu-id="1d6ee-111">Assign the expression on the right of the equal sign to the variable on the left.</span></span>                |
| `+=`       | <span data-ttu-id="1d6ee-112">現在の変数の値に右側の式を足したものを左側の変数に割り当てます。</span><span class="sxs-lookup"><span data-stu-id="1d6ee-112">Assign the current variable value plus the expression on the right to the variable on the left.</span></span>  |
| `++`       | <span data-ttu-id="1d6ee-113">変数を 1 ずつ増加します。</span><span class="sxs-lookup"><span data-stu-id="1d6ee-113">Increment the variable by 1.</span></span>                                                                     |
| `-=`       | <span data-ttu-id="1d6ee-114">現在の変数の値から右側の式を差し引いたものを左側の変数に割り当てます。</span><span class="sxs-lookup"><span data-stu-id="1d6ee-114">Assign the current variable value minus the expression on the right to the variable on the left.</span></span> |
| `--`       | <span data-ttu-id="1d6ee-115">変数を 1 ずつ減分します。</span><span class="sxs-lookup"><span data-stu-id="1d6ee-115">Decrement the variable by 1.</span></span>                                                                     |

### <a name="code-examples-for-assignment-operators"></a><span data-ttu-id="1d6ee-116">代入演算子のコード例</span><span class="sxs-lookup"><span data-stu-id="1d6ee-116">Code examples for assignment operators</span></span>

```xpp
// An example of assignment operators and their output. 
static void Example1()
{
    int i = 1;
    // Using the = operator. i is assigned the value of i, plus 1. i = 2.
    i = i + 1;
    info(strFmt("Example 1: The result is "), i); // The result is 2.
}

static void Example2()
{
    int i = 1;
    // Using the += operator. i is assigned the value of i, plus 1. 
    // i = 2 (i = i + 1).
    i += 1;
    info(strFmt("Example 2: The result is "), i); // The result is 2. 
}

static void Example3()
{
    int i = 1;
    // Using the ++ operator. i is incremented by 1, and then 
    // by 1 again in the second statement. The final value of i is 3.
    i++;
    ++i;
    info(strFmt("Example 3: The result is "), i); // The result is 3. 
}

static void Example4()
{
    int i = 1;
    // Using the -= operator. i is assigned the value of i minus 1. 
    // i = 0 (i = i - 1).
    i -= 1;
    info(strFmt("Example 4: The result is "), i); // The result is 0. 
}

static void Example5()
{
    int i = 1;
    // Using the -- operator. i is decremented by 1, and then by 
    // 1 again in the second statement. The final value of i is -1.
    i--;
    --i;
    info(strFmt("Example 5: The result is "), i); // The result is -1. 
}
```

## <a name="arithmetic-operators"></a><span data-ttu-id="1d6ee-117">算術演算子</span><span class="sxs-lookup"><span data-stu-id="1d6ee-117">Arithmetic operators</span></span>
<span data-ttu-id="1d6ee-118">算術演算子を使用して、数値計算を実行します。</span><span class="sxs-lookup"><span data-stu-id="1d6ee-118">You use arithmetic operators to perform numeric calculations.</span></span> <span data-ttu-id="1d6ee-119">演算子のほとんどはバイナリであり、2 つのオペランドを取ります。</span><span class="sxs-lookup"><span data-stu-id="1d6ee-119">Most of the operators are binary and take two operands.</span></span> <span data-ttu-id="1d6ee-120">ただし、**not** (`~`) 演算子は単項であり、オペランドを 1 つだけ受け取ります。</span><span class="sxs-lookup"><span data-stu-id="1d6ee-120">However, the **not** (`~`) operator is unary and takes only one operand.</span></span> <span data-ttu-id="1d6ee-121">バイナリ演算子の構文: *expression1* *ArithmeticOperator* *expression2* 単項演算子の構文: *ArithmeticOperator* *expression1*</span><span class="sxs-lookup"><span data-stu-id="1d6ee-121">Syntax for binary operators: *expression1* *ArithmeticOperator* *expression2* Syntax for unary operators: *ArithmeticOperator* *expression1*</span></span>

| <span data-ttu-id="1d6ee-122">オペレーター</span><span class="sxs-lookup"><span data-stu-id="1d6ee-122">Operator</span></span>   | <span data-ttu-id="1d6ee-123">説明</span><span class="sxs-lookup"><span data-stu-id="1d6ee-123">Description</span></span>      |
|------------|------------------|
| `<<`       | <span data-ttu-id="1d6ee-124">**left shift** 演算子は、*expression1* で *expression2* の左シフト (2 により乗算) を実行します。</span><span class="sxs-lookup"><span data-stu-id="1d6ee-124">The **left shift** operator performs *expression2* left shift (multiplication by 2) on *expression1*.</span></span>              |
| `>>`       | <span data-ttu-id="1d6ee-125">**right shift** 演算子は、*expression1* で *expression2* の右シフト (2 で除算) を実行します。</span><span class="sxs-lookup"><span data-stu-id="1d6ee-125">The **right shift** operator performs *expression2* right shift (division by 2) on *expression1*.</span></span>                  |
| `\*`       | <span data-ttu-id="1d6ee-126">**multiply** 演算子は、*expression1* を *expression2* で乗算します。</span><span class="sxs-lookup"><span data-stu-id="1d6ee-126">The **multiply** operator multiplies *expression1* by *expression2*.</span></span>                                               |
| `/`        | <span data-ttu-id="1d6ee-127">**divide** 演算子は、*expression1* を *expression2* で除算します。</span><span class="sxs-lookup"><span data-stu-id="1d6ee-127">The **divide** operator divides *expression1* by *expression2*.</span></span>                                                    |
| `DIV`      | <span data-ttu-id="1d6ee-128">**integer division** 演算子は、*expression1* の整数除算を *expression2* で実行します。</span><span class="sxs-lookup"><span data-stu-id="1d6ee-128">The **integer division** operator performs an integer division of *expression1* by *expression2*.</span></span>                  |
| `MOD`      | <span data-ttu-id="1d6ee-129">**integer remainder** 演算子は、*expression2* による *expression1* の整数除算の余りを返します。</span><span class="sxs-lookup"><span data-stu-id="1d6ee-129">The **integer remainder** operator returns the remainder of an integer division of *expression1* by *expression2*.</span></span> |
| `~`        | <span data-ttu-id="1d6ee-130">**not** 演算子、つまり単項演算子は、操作ではなくバイナリを実行します。</span><span class="sxs-lookup"><span data-stu-id="1d6ee-130">The **not** operator, or unary operator, performs a binary not operation.</span></span>                                          |
| `&`        | <span data-ttu-id="1d6ee-131">**binary AND** 演算子は、*expression1* および *expression2* でバイナリおよび演算を実行します。</span><span class="sxs-lookup"><span data-stu-id="1d6ee-131">The **binary AND** operator performs a binary and operation on *expression1* and *expression2*.</span></span>                    |
| `^`        | <span data-ttu-id="1d6ee-132">**binary XOR** 演算子は、*expression1* および *expression2* でバイナリ XOR 演算を実行します。</span><span class="sxs-lookup"><span data-stu-id="1d6ee-132">The **binary XOR** operator performs a binary XOR-operation on *expression1* and *expression2*.</span></span>                    |
| `|`        | <span data-ttu-id="1d6ee-133">**binary OR** 演算子は、*expression1* および *expression2* でバイナリまたは演算を実行します。</span><span class="sxs-lookup"><span data-stu-id="1d6ee-133">The **binary OR** operator performs a binary or operation on *expression1* and *expression2*.</span></span>                      |
| `+`        | <span data-ttu-id="1d6ee-134">**plus** 演算子は *expression1* を *expression2* に追加します。</span><span class="sxs-lookup"><span data-stu-id="1d6ee-134">The **plus** operator adds *expression1* to *expression2*.</span></span>                                                         |
| `-`        | <span data-ttu-id="1d6ee-135">**minus** 演算子は、*expression1* から *expression2* を減算します。</span><span class="sxs-lookup"><span data-stu-id="1d6ee-135">The **minus** operator subtracts *expression2* from *expression1*.</span></span>                                                 |
| `?`        | <span data-ttu-id="1d6ee-136">**ternary** 演算子は、3 つの式を取ります: *expression1* ?</span><span class="sxs-lookup"><span data-stu-id="1d6ee-136">The **ternary** operator takes three expressions: *expression1* ?</span></span> <span data-ttu-id="1d6ee-137">*式2* : *式3*。</span><span class="sxs-lookup"><span data-stu-id="1d6ee-137">*expression2* : *expression3*.</span></span> <span data-ttu-id="1d6ee-138">*expression1* が true の場合、*expression2* が返されます。</span><span class="sxs-lookup"><span data-stu-id="1d6ee-138">If *expression1* is true, *expression2* is returned.</span></span> <span data-ttu-id="1d6ee-139">それ以外の場合、*expression3* が返されます。</span><span class="sxs-lookup"><span data-stu-id="1d6ee-139">Otherwise, *expression3* is returned.</span></span> |

### <a name="code-examples-for-arithmetic-operators"></a><span data-ttu-id="1d6ee-140">算術演算子のコード例</span><span class="sxs-lookup"><span data-stu-id="1d6ee-140">Code examples for arithmetic operators</span></span>

```xpp
int a = 1 << 4;      // Perform four left shifts on 1 (1*2*2*2*2). a=16.
int b = 16 >> 4;     // Perform four right shifts on 16 (16/2/2/2/2). b=1.
int c = 4 * 5;       // Multiply 4 by 5. c=20.
int d = 20 / 5;      // Divide 20 by 5. d=4.
int e = 100 div 21;  // Return the integer division of 100 by 21. e=4 (4*21 = 84, remainder 16).
int f = 100 mod 21;  // Return the remainder of the integer division of 100 by 21. f=16.
int g = ~1;          // Binary negate 1 (all bits are reversed). g=-2.
int h = 1 & 3;       // Binary AND. Return the bits that are in common in the two integers. h=1.
int i = 1 | 3;       // Binary OR. Return the bits that are set in either 1 or 3. i=3.
int j = 1 ^ 3;       // Binary XOR. Return the bits that are set in 1 and NOT set in 3, and vice versa. j=2.
int k = 1 + 3;       // Add 1 and 3. k=4.
int l = 3 - 1;       // Subtract 1 from 3. l=2.
int m = (400 > 4) ? 1 : 5;  // If 400>4, 1 is returned. Otherwise, 5 is returned. Because 400>4, 1 is returned. m=1.
```

## <a name="expression-operators"></a><span data-ttu-id="1d6ee-141">式の演算子</span><span class="sxs-lookup"><span data-stu-id="1d6ee-141">Expression operators</span></span>
<span data-ttu-id="1d6ee-142">`as` および `is` 式演算子は、ダウンキャストの割り当てを制御します。</span><span class="sxs-lookup"><span data-stu-id="1d6ee-142">The `as` and `is` expression operators control downcast assignments.</span></span> <span data-ttu-id="1d6ee-143">ダウン キャストの割り当てには、クラスまたはテーブルの継承が含まれています。</span><span class="sxs-lookup"><span data-stu-id="1d6ee-143">Downcast assignments involve class or table inheritance.</span></span> <span data-ttu-id="1d6ee-144">暗黙的にダウンキャストされた代入ステートメントは、予測および診断が困難なエラーを引き起こす可能性があります。</span><span class="sxs-lookup"><span data-stu-id="1d6ee-144">Assignment statements that implicitly downcast can cause errors that are difficult to predict and diagnose.</span></span> <span data-ttu-id="1d6ee-145">`as` キーワードを使用するとダウンキャストを明示的にすることができます。</span><span class="sxs-lookup"><span data-stu-id="1d6ee-145">You can use the `as` keyword to make your downcasts explicit.</span></span> <span data-ttu-id="1d6ee-146">`is` キーワードを使用して、実行時にダウンキャストが有効かどうかをテストできます。</span><span class="sxs-lookup"><span data-stu-id="1d6ee-146">You can use the `is` keyword to test whether a downcast is valid at run time.</span></span>

### <a name="the-as-keyword"></a><span data-ttu-id="1d6ee-147">as キーワード</span><span class="sxs-lookup"><span data-stu-id="1d6ee-147">The as keyword</span></span>

<span data-ttu-id="1d6ee-148">基本クラス変数から派生クラス変数にダウンキャストする割り当てキーワードには、`as` を使用します。</span><span class="sxs-lookup"><span data-stu-id="1d6ee-148">Use the `as` keyword for assignments that downcast from a base class variable to a derived class variable.</span></span> <span data-ttu-id="1d6ee-149">`as` キーワードは、他のプログラマやコンパイラに対して、ダウンキャストが実行時に有効であると考えられることを通知します。</span><span class="sxs-lookup"><span data-stu-id="1d6ee-149">The `as` keyword tells other programmers and the compiler that you believe that the downcast will be valid during run time.</span></span>

-   <span data-ttu-id="1d6ee-150">コンパイラは、`as` キーワードを持たないダウンキャスト割り当てステートメントのエラーを報告します。</span><span class="sxs-lookup"><span data-stu-id="1d6ee-150">The compiler reports an error for downcast assignment statements that lack the `as` keyword.</span></span>
-   <span data-ttu-id="1d6ee-151">実行時に `as` キーワードを指定すると、ダウンキャストが有効でない場合に、ダウンキャスト割り当てステートメントに `null` が割り当てられます。</span><span class="sxs-lookup"><span data-stu-id="1d6ee-151">At run time, the `as` keyword causes the downcast assignment statement to assign `null` if the downcast isn't valid.</span></span>
-   <span data-ttu-id="1d6ee-152">この `is` キーワードは、多くの場合、`as` キーワードが機能するかどうかのテストを問題なく行うために使用されます。</span><span class="sxs-lookup"><span data-stu-id="1d6ee-152">This `is` keyword is often used to safely test whether the `as` keyword will work.</span></span>

#### <a name="code-example-for-the-as-keyword"></a><span data-ttu-id="1d6ee-153">キーワードとしてのコード例</span><span class="sxs-lookup"><span data-stu-id="1d6ee-153">Code example for the as keyword</span></span>

<span data-ttu-id="1d6ee-154">次のコード例では、**DerivedClass** クラスが **BaseClass** クラスを拡張します。</span><span class="sxs-lookup"><span data-stu-id="1d6ee-154">In the following code example, the **DerivedClass** class extends the **BaseClass** class.</span></span> <span data-ttu-id="1d6ee-155">このコード例には、**basec** と **derivedc** 変数の間に 2 つの有効な割り当てが含まれています。</span><span class="sxs-lookup"><span data-stu-id="1d6ee-155">The code example contains two valid assignments between its **basec** and **derivedc** variables.</span></span> <span data-ttu-id="1d6ee-156">**basec** へのアップキャスト割り当てには `as` キーワードは必要ありませんが、**derivedc** へのダウンキャストの割り当てには `as` キーワードが必要です。</span><span class="sxs-lookup"><span data-stu-id="1d6ee-156">The upcast assignment to **basec** doesn't require the `as` keyword, but the downcast assignment to **derivedc** does require the `as` keyword.</span></span> <span data-ttu-id="1d6ee-157">次のコードはエラーなしでコンパイルして実行します。</span><span class="sxs-lookup"><span data-stu-id="1d6ee-157">The following code will compile and run without errors.</span></span>

```xpp
static void AsKeywordExample()
{
    // DerivedClass extends BaseClass.
    BaseClass basec;
    DerivedClass derivedc;
    // BottomClass extends DerivedClass.
    BottomClass bottomc;
    derivedc = new DerivedClass();
    // AS is not required for an upcast assignment like this.
    basec = derivedc;
    // AS is required for a downcast assignment like this.
    derivedc = basec as DerivedClass;
    bottomc = new BottomClass();
    // AS causes this invalid downcast to assign null.
    bottomc = basec as DerivedClass;
}
```

### <a name="the-is-keyword"></a><span data-ttu-id="1d6ee-158">is キーワード</span><span class="sxs-lookup"><span data-stu-id="1d6ee-158">The is keyword</span></span>

<span data-ttu-id="1d6ee-159">`is` キーワードは、オブジェクトが指定されたクラスのサブタイプであるかどうかを確認します。</span><span class="sxs-lookup"><span data-stu-id="1d6ee-159">The `is` keyword verifies whether an object is a subtype of a specified class.</span></span> <span data-ttu-id="1d6ee-160">`is` 式は、オブジェクトがクラスのサブタイプである場合、またはオブジェクトがクラスと同じ型である場合に **true** を返します。</span><span class="sxs-lookup"><span data-stu-id="1d6ee-160">The `is` expression returns **true** if the object is a subtype of the class, or if the object is the same type as the class.</span></span> <span data-ttu-id="1d6ee-161">`is` キーワード式が 2 つの型を比較するが、どちらの型も他方のサブタイプではなく、同じ型でない場合、コンパイラはエラーを報告します。</span><span class="sxs-lookup"><span data-stu-id="1d6ee-161">The compiler reports an error if an `is` keyword expression compares two types, but neither type is a subtype of the other, and they aren't of the same type.</span></span> <span data-ttu-id="1d6ee-162">コンパイラは、2 つの型の間の任意の明示的な代入ステートメントについて同様のエラーを報告します。どちらの型も一方の型のサブタイプではなく、同じ型ではありません。</span><span class="sxs-lookup"><span data-stu-id="1d6ee-162">The compiler reports a similar error for any plain assignment statement between two types, where neither type is a subtype of the other, and they aren't of the same type.</span></span> <span data-ttu-id="1d6ee-163">実行時に、基になるオブジェクトを参照する変数の型は `is` キーワードとは無関係です。</span><span class="sxs-lookup"><span data-stu-id="1d6ee-163">At run time, the type of variable that references the underlying object is irrelevant to the `is` keyword.</span></span> <span data-ttu-id="1d6ee-164">`is` キーワードを指定すると、システムは、オブジェクトを参照する変数の宣言された型ではなく、変数が参照するオブジェクトを検証します。</span><span class="sxs-lookup"><span data-stu-id="1d6ee-164">The `is` keyword causes the system to verify the object that the variable references, not the declared type of the variable that references the object.</span></span>

#### <a name="code-examples-for-the-is-keyword"></a><span data-ttu-id="1d6ee-165">のコード例はキーワードです</span><span class="sxs-lookup"><span data-stu-id="1d6ee-165">Code examples for the is keyword</span></span>

<span data-ttu-id="1d6ee-166">次のコード例は、`is`式が **true** または **false** を返すかどうかを制御する条件を示しています。</span><span class="sxs-lookup"><span data-stu-id="1d6ee-166">The following code examples illustrate the conditions that control whether an `is` expression returns **true** or **false**.</span></span> <span data-ttu-id="1d6ee-167">このコード例は、**Form** クラスと **Query** クラスの両方が **TreeNode** クラスを拡張しているという事実に依存しています。</span><span class="sxs-lookup"><span data-stu-id="1d6ee-167">The code examples depend on the fact that the **Form** class and the **Query** class both extend the **TreeNode** class.</span></span>

```xpp
// The compiler issues an error for the following code. 
// The compiler ascertains that the Form class and the Query class are not 
// part of the same inheritance hierarchy. Both the Form class and the Query class
// extend the TreeNode class, but neither Form nor Query is a subtype of the other.
Form myForm = new Form();
info(strFmt("%1", (myForm is Query)));

// The Infolog displays 0 during run time, where 0 means false. No supertype 
// object can be considered to also be of its subtype class.
TreeNode myTreeNode = new TreeNode();
info(strFmt("%1", (myTreeNode is Form)));

// The Infolog displays 0 during run time, where 0 means false. A null 
// reference causes the is expression to return false.
Form myForm;
info(strFmt("%1", (myForm is Form)));

// The Infolog displays 1 during run time, where 1 means true. 
// An object is an instance of its own class type.
Form myForm = new Form();
info(strFmt("%1", (myForm is Form)));

// The Infolog displays 1 during run time, where 1 means true. 
// Every subtype is also of its supertype.
Form myForm = new Form();
info(strFmt("%1", (myForm is TreeNode)));

// The Infolog displays 1 during run time, where 1 means true. 
// The type of the underlying object matters in the is expression,
// not the type of the variable that references the object.
Form myForm = new Form();
TreeNode myTreeNode;
myTreeNode = myForm; // Upcast.
info(strFmt("%1", (myTreeNode is Form)));
```

#### <a name="code-example-for-the-is-and-as-keywords"></a><span data-ttu-id="1d6ee-168">と キーワードとしてのコード例</span><span class="sxs-lookup"><span data-stu-id="1d6ee-168">Code example for the is and as keywords</span></span>

<span data-ttu-id="1d6ee-169">次のコード例には、`is` キーワードの一般的な使用方法が含まれています。</span><span class="sxs-lookup"><span data-stu-id="1d6ee-169">The following code example contains a typical use of the `is` keyword.</span></span> <span data-ttu-id="1d6ee-170">`as` キーワードは `is` キーワードが `as` キーワードが成功することを確認した後に使用されます。</span><span class="sxs-lookup"><span data-stu-id="1d6ee-170">The `as` keyword is used after the `is` keyword verifies that the `as` keyword will succeed.</span></span> <span data-ttu-id="1d6ee-171">この例では、`is` キーワードと `as` キーワードは大文字で表示され、見やすくなっています。</span><span class="sxs-lookup"><span data-stu-id="1d6ee-171">In this example, the `is` and `as` keywords are uppercase to make them more visible.</span></span>

```xpp
static void IsKeywordExample() 
{
    DerivedClass derivedc;
    BaseClass basec;
    basec = new DerivedClass();  // An upcast.
    if (basec IS DerivedClass)
    {
        info("Test 1: (basec IS DerivedClass) is true. Good.");
        derivedc = basec AS DerivedClass;
    }
    basec = new BaseClass();
    if (!(basec IS DerivedClass))
    {
        info("Test 2: !(basec IS DerivedClass) is true. Good.");
    }
}

//Output to the Infolog
Test 1: (basec IS DerivedClass) is true. Good.
Test 2: (!(basec IS DerivedClass)) is true. Good.
```

### <a name="object-class-as-a-special-case"></a><span data-ttu-id="1d6ee-172">特殊なケースとしてのオブジェクト クラス</span><span class="sxs-lookup"><span data-stu-id="1d6ee-172">Object class as a special case</span></span>

<span data-ttu-id="1d6ee-173">**Object** クラスは、継承機能に特別なケースとして表示できます。</span><span class="sxs-lookup"><span data-stu-id="1d6ee-173">The **Object** class can appear as a special case in inheritance functionality.</span></span> <span data-ttu-id="1d6ee-174">コンパイラは、**オブジェクト** 型であると宣言された変数との間の割り当ての型チェックをバイパスします。</span><span class="sxs-lookup"><span data-stu-id="1d6ee-174">The compiler bypasses type checking for assignments to and from variables that are declared to be of type **Object**.</span></span> <span data-ttu-id="1d6ee-175">**オブジェクト** クラスから継承されるクラス、別のクラスから継承されるクラス、どのクラスからも継承されないクラスがあります。</span><span class="sxs-lookup"><span data-stu-id="1d6ee-175">Some classes inherit from the **Object** class, some classes inherit from another class, and some classes don't inherit from any class.</span></span> <span data-ttu-id="1d6ee-176">**ダイアログ** クラスはどのクラスからも継承しませんが、次のコード例の割り当ておよび呼び出しステートメントからの処理はおこなわれます。</span><span class="sxs-lookup"><span data-stu-id="1d6ee-176">Although the **Dialog** class doesn't inherit from any class, the assignment and call statements in the following code example work.</span></span> <span data-ttu-id="1d6ee-177">ただし、割り当てが `bank4 = dlog3;` の場合、**銀行** クラスと **ダイアログ** クラスは互いに継承関係を持たないため、コンパイル時に失敗します。</span><span class="sxs-lookup"><span data-stu-id="1d6ee-177">However, if the assignment is `bank4 = dlog3;`, it will fail at compile time, because the **Bank** and **Dialog** classes have no inheritance relationship to each other.</span></span> <span data-ttu-id="1d6ee-178">コンパイラは、**オブジェクト** クラスであると宣言された変数への割り当てに対して、1 つの小さな検証しか実行しません。</span><span class="sxs-lookup"><span data-stu-id="1d6ee-178">The compiler performs only one small validation on assignments to a variable that is declared to be of the **Object** class.</span></span> <span data-ttu-id="1d6ee-179">コンパイラは、**オブジェクト** 変数に割り当てられている項目がクラスのインスタンスであることを確認します。</span><span class="sxs-lookup"><span data-stu-id="1d6ee-179">The compiler verifies that the item that is being assigned to the **Object** variable is an instance of a class.</span></span> <span data-ttu-id="1d6ee-180">コンパイラでは、テーブル バッファーのインスタンスを **オブジェクト** 変数に割り当てることはできません。</span><span class="sxs-lookup"><span data-stu-id="1d6ee-180">The compiler doesn't allow an instance of a table buffer to be assigned to the **Object** variable.</span></span> <span data-ttu-id="1d6ee-181">また、コンパイラは、`int` または `str`のようなプリミティブ データ型を **オブジェクトt** 変数に割り当てることはできません。</span><span class="sxs-lookup"><span data-stu-id="1d6ee-181">Additionally, the compiler doesn't allow primitive data types, such as `int` or `str`, to be assigned to the **Object** variable.</span></span>

```xpp
static void ObjectExample()
{
    Bank bank4;
    Object obj2;
    Dialog dlog3 = new Dialog("Test 4.");
    obj2 = dlog3;  // The assignment does work.
    obj2.run(false);  // The call causes the dialog to appear.
    info("Test 4a is finished.");
}
```

### <a name="tables"></a><span data-ttu-id="1d6ee-182">テーブル</span><span class="sxs-lookup"><span data-stu-id="1d6ee-182">Tables</span></span>

<span data-ttu-id="1d6ee-183">すべての表は、異なる表から明示的に継承しない限り、共通システム表から直接継承します。</span><span class="sxs-lookup"><span data-stu-id="1d6ee-183">All tables inherit directly from the Common system table, unless they explicitly inherit from a different table.</span></span> <span data-ttu-id="1d6ee-184">共通テーブルをインスタンス化することはできません。</span><span class="sxs-lookup"><span data-stu-id="1d6ee-184">The Common table can't be instantiated.</span></span> <span data-ttu-id="1d6ee-185">基になる物理データベースに存在しません。</span><span class="sxs-lookup"><span data-stu-id="1d6ee-185">It doesn't exist in the underlying physical database.</span></span> <span data-ttu-id="1d6ee-186">共通テーブルは **xRecord** クラスから継承されますが、`is` キーワードまたは `as` キーワードに適切でない特別な方法で継承されます。</span><span class="sxs-lookup"><span data-stu-id="1d6ee-186">The Common table inherits from the **xRecord** class, but in a special way that isn't appropriate for the `is` keyword or the `as` keyword.</span></span> <span data-ttu-id="1d6ee-187">テーブル間の無効なダウンキャストの実行に`as` キーワードが使用されるとき、ターゲット変数は使用不可能な null エンティティを参照します。</span><span class="sxs-lookup"><span data-stu-id="1d6ee-187">When the `as` keyword is used to perform an invalid downcast among tables, the target variable references an unusable non-null entity.</span></span> <span data-ttu-id="1d6ee-188">ターゲット変数の参照を解除しようとすると、プログラムを停止させるエラーが発生します。</span><span class="sxs-lookup"><span data-stu-id="1d6ee-188">Any attempt to de-reference the target variable will cause an error that stops the program.</span></span>

### <a name="the-is-and-as-keywords-and-extended-data-types"></a><span data-ttu-id="1d6ee-189">is キーワードと as キーワードと拡張データ型</span><span class="sxs-lookup"><span data-stu-id="1d6ee-189">The is and as keywords and extended data types</span></span>

<span data-ttu-id="1d6ee-190">各拡張データ タイプには、**拡張** プロパティがあります。</span><span class="sxs-lookup"><span data-stu-id="1d6ee-190">Each extended data type has an **Extends** property.</span></span> <span data-ttu-id="1d6ee-191">このプロパティが制御する継承のスタイルは、`is` で、`as` のキーワードが設計されている継承のスタイルと異なります。</span><span class="sxs-lookup"><span data-stu-id="1d6ee-191">The style of inheritance that this property controls differs from the style of inheritance that the `is` and `as` keywords are designed for.</span></span>

## <a name="relational-operators"></a><span data-ttu-id="1d6ee-192">リレーショナル演算子</span><span class="sxs-lookup"><span data-stu-id="1d6ee-192">Relational operators</span></span>
<span data-ttu-id="1d6ee-193">次のテーブルは、X++ で使用できるリレーショナル演算子の一覧です。</span><span class="sxs-lookup"><span data-stu-id="1d6ee-193">The following table lists the relational operators that can be used in X++.</span></span> <span data-ttu-id="1d6ee-194">演算子のほとんどはバイナリであり、2 つのオペランドを取ります。</span><span class="sxs-lookup"><span data-stu-id="1d6ee-194">Most of the operators are binary and take two operands.</span></span> <span data-ttu-id="1d6ee-195">ただし、**not** (`!`) 演算子は単項であり、オペランドを 1 つだけ受け取ります。</span><span class="sxs-lookup"><span data-stu-id="1d6ee-195">However, the **not** (`!`) operator is unary and takes only one operand.</span></span> <span data-ttu-id="1d6ee-196">バイナリ演算子の構文: *expression1* *relationalOperator* *expression2* 単項演算子の構文: *relationalOperator* *expression1*</span><span class="sxs-lookup"><span data-stu-id="1d6ee-196">Syntax for binary operators: *expression1* *relationalOperator* *expression2* Syntax for unary operators: *relationalOperator* *expression1*</span></span>

| <span data-ttu-id="1d6ee-197">オペレーター</span><span class="sxs-lookup"><span data-stu-id="1d6ee-197">Operator</span></span> | <span data-ttu-id="1d6ee-198">説明</span><span class="sxs-lookup"><span data-stu-id="1d6ee-198">Description</span></span>     |
|----------|--------------------------------|
| `like`   | <span data-ttu-id="1d6ee-199">**like** 関係演算子は、*expression1* が *expression2* と似ている場合に **true** を返します。</span><span class="sxs-lookup"><span data-stu-id="1d6ee-199">The **like** relational operator returns **true** if *expression1* is like *expression2*.</span></span>  |
| `==`     | <span data-ttu-id="1d6ee-200">**equal** 関係演算子は、両方の式が等しい場合に **true** を返します。</span><span class="sxs-lookup"><span data-stu-id="1d6ee-200">The **equal** relational operator returns **true** if both expressions are equal.</span></span>  |
| `>=`     | <span data-ttu-id="1d6ee-201">**greater than or equal to** 関係演算子は、*expression1* が *expression2* 以上の場合に **true** を返します。</span><span class="sxs-lookup"><span data-stu-id="1d6ee-201">The **greater than or equal to** relational operator returns **true** if *expression1* is greater than or equal to *expression2*.</span></span>   |
| `<=`     | <span data-ttu-id="1d6ee-202">**less than or equal to** 関係演算子は、*expression1* が *expression2* 以下の場合に **true** を返します。</span><span class="sxs-lookup"><span data-stu-id="1d6ee-202">The **less than or equal to** relational operator returns **true** if *expression1* is less than or equal to *expression2*.</span></span>|
| `>`      | <span data-ttu-id="1d6ee-203">**greater than** 関係演算子は、*expression1* が *expression2* より大きい場合に **true** を返します。</span><span class="sxs-lookup"><span data-stu-id="1d6ee-203">The **greater than** relational operator returns **true** if *expression1* is greater than *expression2*.</span></span> |
| `<`      | <span data-ttu-id="1d6ee-204">**less than** 関係演算子は、*expression1* が *expression2* より小さい場合に **true** を返します。</span><span class="sxs-lookup"><span data-stu-id="1d6ee-204">The **less than** relational operator returns **true** if *expression1* is less than *expression2*.</span></span>  |
| `!=`     | <span data-ttu-id="1d6ee-205">**not equal** 関係演算子は、*expression1* が *expression2* と異なる (つまり等しくない) 場合に **true** を返します。</span><span class="sxs-lookup"><span data-stu-id="1d6ee-205">The **not equal** relational operator returns **true** if *expression1* differs from (that is, if it isn't equal to) *expression2*.</span></span>                          |
| `&&`     | <span data-ttu-id="1d6ee-206">**and** 関係演算子は、*expression1* と *expression2* の両方が true の場合に、**true** を返します。</span><span class="sxs-lookup"><span data-stu-id="1d6ee-206">The **and** relational operator returns **true** if both *expression1* and *expression2* are true.</span></span>  |
| `||`     | <span data-ttu-id="1d6ee-207">**or** 関係演算子は、*expression1* または *expression2* が true の場合、または両方が true の場合に **true** を返します。</span><span class="sxs-lookup"><span data-stu-id="1d6ee-207">The **or** relational operator returns **true** if *expression1* or *expression2* is true, or if both are true.</span></span> |
| `!`      | <span data-ttu-id="1d6ee-208">**not** または **unary** 関係演算子、式を無効にします。</span><span class="sxs-lookup"><span data-stu-id="1d6ee-208">The **not** or **unary** relational operator negates the expression.</span></span> <span data-ttu-id="1d6ee-209">式が false の場合は **true**、式が true の場合は **false** を返します。</span><span class="sxs-lookup"><span data-stu-id="1d6ee-209">It returns **true** if the expression is false and **false** if the expression is true.</span></span> |

### <a name="the-like-operator"></a><span data-ttu-id="1d6ee-210">like 演算子</span><span class="sxs-lookup"><span data-stu-id="1d6ee-210">The like operator</span></span>

<span data-ttu-id="1d6ee-211">`like`演算子は、`*` を 0 文字以上のワイルドカード文字として、さらに、 `?` を 1 つの文字に対する 1 つのワイルドカード文字として使用できます。</span><span class="sxs-lookup"><span data-stu-id="1d6ee-211">The `like` operator can use `*` as a wildcard character for zero or more characters, and `?` as a wildcard character for one character.</span></span> <span data-ttu-id="1d6ee-212">オペランドは 1,000 文字を超えることはできません。</span><span class="sxs-lookup"><span data-stu-id="1d6ee-212">The maximum length of the operand is 1,000 characters.</span></span> <span data-ttu-id="1d6ee-213">`like` 演算子は、基になる SQL により評価されるため、インストールごとに結果が異なる可能性があります。</span><span class="sxs-lookup"><span data-stu-id="1d6ee-213">The `like` operator is evaluated by the underlying SQL, so the result might differ on different installations.</span></span> <span data-ttu-id="1d6ee-214">比較している式にファイルのパスが含まれている場合は、次の例で示すように、各要素の間で次の 4 つのバックスラッシュを含める必要があります。</span><span class="sxs-lookup"><span data-stu-id="1d6ee-214">If the expressions that you're comparing contain a file path, you must include four backslashes between each element, as shown in the following example.</span></span>

```xpp
select * from xRefpaths
where xRefPaths.Path like "\\\\Classes\\\\AddressSelectForm"
```

### <a name="the-equal--operator"></a><span data-ttu-id="1d6ee-215">等号 (==) 演算子</span><span class="sxs-lookup"><span data-stu-id="1d6ee-215">The equal (==) operator</span></span>

<span data-ttu-id="1d6ee-216">**等号** (`==`) 演算子を使用してオブジェクトを比較するとき、オブジェクト自体ではなく、オブジェクト参照が比較されます。 </span><span class="sxs-lookup"><span data-stu-id="1d6ee-216">When you use the **equal** (`==`) operator to compare objects, the object references are compared, not the objects themselves.</span></span> <span data-ttu-id="1d6ee-217">この動作は、2 つのオブジェクト (そのうちの 1 つはサーバー上にあり、もう 1 つはクライアント上にあるオブジェクト) を比較すると問題が発生する可能性があります。</span><span class="sxs-lookup"><span data-stu-id="1d6ee-217">This behavior might cause issues if you compare two objects, one of which is located on the server, and the other of which is located on the client.</span></span> <span data-ttu-id="1d6ee-218">そのような場合、**equal** メソッドを **オブジェクト** クラスで使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="1d6ee-218">In these cases, you should use the **equal** method in the **Object** class.</span></span> <span data-ttu-id="1d6ee-219">このメソッドをオーバーライドして、2つのオブジェクトが等しいことが何を意味するかを指定することができます。</span><span class="sxs-lookup"><span data-stu-id="1d6ee-219">You can override this method to specify what it means for two objects to be equal.</span></span> <span data-ttu-id="1d6ee-220">**等号** メソッドを上書きしない場合、比較は **等号** (`==`) 演算子によって行われる比較と同じになります。</span><span class="sxs-lookup"><span data-stu-id="1d6ee-220">If you don't override the **equal** method, the comparison is identical to the comparison that is done by the **equal** (`==`) operator.</span></span>

### <a name="code-examples-for-relational-operators"></a><span data-ttu-id="1d6ee-221">リレーショナル演算子のコード例</span><span class="sxs-lookup"><span data-stu-id="1d6ee-221">Code examples for relational operators</span></span>

```xpp
"Jones" like "Jo?es"  // Returns true, because the ? is equal to any single character.
"Fabrikam, Inc." like "Fa*"  // Returns true, because the * is equal to zero or more characters.
(( 42 * 2) == 84)  // Returns true, because 42*2 is equal to 84.
today() >= 1\1\1980  // Returns true, because today is later than January 1, 1980.
((11 div 10) >= 1)  // Returns true, because 11 div 10 is 1 (therefore, >= 1 is true).
(11<= 12)  // Returns true, because 11 is less than 12.
((11 div 10) > 1)  // Returns false, because 11 div 10 is 1.
(11 div 10) < 1)  // Returns false, because 11 div 10 is 1.
(11 != 12)  // Returns true, because 11 is not equal to 12.
(1 == 1) && (3 > 1)  // Returns true, because both expressions are true.
```

## <a name="operator-precedence"></a><span data-ttu-id="1d6ee-222">演算子の優先順位</span><span class="sxs-lookup"><span data-stu-id="1d6ee-222">Operator precedence</span></span>
<span data-ttu-id="1d6ee-223">複合式が評価される順序は重要です。</span><span class="sxs-lookup"><span data-stu-id="1d6ee-223">The order that a compound expression is evaluated in can be important.</span></span> <span data-ttu-id="1d6ee-224">たとえば `(x + y / 100)` は、追加または区分を最初に実行するかどうかによって、結果が異なります。</span><span class="sxs-lookup"><span data-stu-id="1d6ee-224">For example, `(x + y / 100)` gives a different result, depending on whether the addition or the division is done first.</span></span> <span data-ttu-id="1d6ee-225">かっこ (`()`) を使用すると、式の評価方法を明示的にコンパイラに指示することができます。</span><span class="sxs-lookup"><span data-stu-id="1d6ee-225">You can use parentheses (`()`) to explicitly tell the compiler how it should evaluate an expression.</span></span> <span data-ttu-id="1d6ee-226">たとえば、 `(x + y) / 100`を指定できます。</span><span class="sxs-lookup"><span data-stu-id="1d6ee-226">For example, you can specify `(x + y) / 100`.</span></span> <span data-ttu-id="1d6ee-227">オペレーションを実行する順序をコンパイラーに明示的に伝えていない場合、順序はオペレーターに割り当てられた優先順位に基づきます。</span><span class="sxs-lookup"><span data-stu-id="1d6ee-227">If you don't explicitly tell the compiler the order that you want operations to be done in, the order is based on the precedence that is assigned to the operators.</span></span> <span data-ttu-id="1d6ee-228">たとえば、除算演算子には、加算演算子より高い優先順位があります。</span><span class="sxs-lookup"><span data-stu-id="1d6ee-228">For example, the division operator has higher precedence than the addition operator.</span></span> <span data-ttu-id="1d6ee-229">したがって、`x + y / 100`の式では、コンパイラはまず `y / 100` を評価します。</span><span class="sxs-lookup"><span data-stu-id="1d6ee-229">Therefore, for the expression `x + y / 100`, the compiler evaluates `y / 100` first.</span></span> <span data-ttu-id="1d6ee-230">つまり、 `x + y / 100` は `x + (y / 100)` と等しくなります。</span><span class="sxs-lookup"><span data-stu-id="1d6ee-230">In other words, `x + y / 100` is equivalent to `x + (y / 100)`.</span></span> <span data-ttu-id="1d6ee-231">コードを読みやすく管理しやすくするために、明示的に記述します。</span><span class="sxs-lookup"><span data-stu-id="1d6ee-231">To make your code easy to read and maintain, be explicit.</span></span> <span data-ttu-id="1d6ee-232">最初に評価する演算子を示すには、かっこを使用します。</span><span class="sxs-lookup"><span data-stu-id="1d6ee-232">Use parentheses to indicate which operators should be evaluated first.</span></span> <span data-ttu-id="1d6ee-233">次のテーブルは、優先順位の順に演算子を示します。</span><span class="sxs-lookup"><span data-stu-id="1d6ee-233">The following table lists the operators in order of precedence.</span></span> <span data-ttu-id="1d6ee-234">テーブルの演算子は高いほど、優先順位が高くなります。</span><span class="sxs-lookup"><span data-stu-id="1d6ee-234">The higher an operator appears in the table, the higher its precedence.</span></span> <span data-ttu-id="1d6ee-235">高い優先順位がある演算子は、低い優先順位がある演算子より前に評価されます。</span><span class="sxs-lookup"><span data-stu-id="1d6ee-235">Operators that have higher precedence are evaluated before operators that have lower precedence.</span></span> <span data-ttu-id="1d6ee-236">X++ の演算子の優先順位は、C\# および Java などの他の言語の演算子の優先順位と同じではないことに注意してください。</span><span class="sxs-lookup"><span data-stu-id="1d6ee-236">Note that the operator precedence of X++ isn't the same as the operator precedence of other languages, such as C\# and Java.</span></span>


| <span data-ttu-id="1d6ee-237">演算子グループ (優先順位順)</span><span class="sxs-lookup"><span data-stu-id="1d6ee-237">Operator groups, in order of precedence</span></span>                          |                 <span data-ttu-id="1d6ee-238">演算子</span><span class="sxs-lookup"><span data-stu-id="1d6ee-238">Operators</span></span>    |
|------------------------------------------------------------------|------------------------------|
| <span data-ttu-id="1d6ee-239">単項</span><span class="sxs-lookup"><span data-stu-id="1d6ee-239">Unary</span></span>                                                            | `- ~ !`                      |
| <span data-ttu-id="1d6ee-240">乗算、シフト、ビット演算 **AND**、ビット演算排他的 **OR**</span><span class="sxs-lookup"><span data-stu-id="1d6ee-240">Multiplicative, shift, bitwise **AND**, bitwise exclusive **OR**</span></span> | `* / % DIV << >> & ^ `       |
| <span data-ttu-id="1d6ee-241">加法、ビット演算包括的 **OR**</span><span class="sxs-lookup"><span data-stu-id="1d6ee-241">Additive, bitwise inclusive **OR**</span></span>                               | `+ –`                        |
| <span data-ttu-id="1d6ee-242">リレーショナル、同等</span><span class="sxs-lookup"><span data-stu-id="1d6ee-242">Relational, equality</span></span>                                             | `< <= == != > >= like as is` |
| <span data-ttu-id="1d6ee-243">論理 (**AND**、**OR**)</span><span class="sxs-lookup"><span data-stu-id="1d6ee-243">Logical (**AND**, **OR**)</span></span>                                        | <span data-ttu-id="1d6ee-244">`&&` `||`</span><span class="sxs-lookup"><span data-stu-id="1d6ee-244">`&&` `||`</span></span>                    |
| <span data-ttu-id="1d6ee-245">条件付</span><span class="sxs-lookup"><span data-stu-id="1d6ee-245">Conditional</span></span>                                                      | `? :`                        |

<span data-ttu-id="1d6ee-246">同じ行の演算子には、同等な優先順位があります。</span><span class="sxs-lookup"><span data-stu-id="1d6ee-246">Operators on the same line have equal precedence.</span></span> <span data-ttu-id="1d6ee-247">式にこれらの演算子のうち 1 つ以上が含まれる場合、代入演算子が使用されない限り、式は左から右に評価されます。</span><span class="sxs-lookup"><span data-stu-id="1d6ee-247">If an expression includes more than one of these operators, it's evaluated from left to right, unless assignment operators are used.</span></span> <span data-ttu-id="1d6ee-248">(代入演算子は、右から左に評価されます)。たとえば、`&&` (論理 `AND`) および `||` (論理 `OR`) には、同じ優先順位で、左から右に評価されます。</span><span class="sxs-lookup"><span data-stu-id="1d6ee-248">(Assignment operators are evaluated from right to left.) For example, `&&` (logical `AND`) and `||` (logical `OR`) have the same precedence, and are evaluated from left to right.</span></span> <span data-ttu-id="1d6ee-249">したがって、</span><span class="sxs-lookup"><span data-stu-id="1d6ee-249">Therefore:</span></span> 
+ <span data-ttu-id="1d6ee-250">`0 && 0 || 1` == `1`</span><span class="sxs-lookup"><span data-stu-id="1d6ee-250">`0 && 0 || 1` is equal to `1`</span></span>
+ <span data-ttu-id="1d6ee-251">`1 || 0 && 0` == `0` です。</span><span class="sxs-lookup"><span data-stu-id="1d6ee-251">`1 || 0 && 0` is equal to `0`.</span></span>


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]