---
title: X++ 変数
description: このトピックでは、X++の変数について説明します。
author: RobinARH
ms.date: 07/08/2019
ms.topic: article
audience: Developer
ms.reviewer: rhaertle
ms.custom: 150183
ms.search.region: Global
ms.author: rhaertle
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 2475f94f398a4a50fa02deb454b8d025244055f7
ms.sourcegitcommit: e4992c57eea4c15ac052e9d65dddae625e3528f9
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/07/2021
ms.locfileid: "5865957"
---
# <a name="x-variables"></a><span data-ttu-id="7ca54-103">X++ 変数</span><span class="sxs-lookup"><span data-stu-id="7ca54-103">X++ variables</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="7ca54-104">このトピックでは、X++の変数について説明します。</span><span class="sxs-lookup"><span data-stu-id="7ca54-104">This topic describes variables in X++.</span></span>

- <span data-ttu-id="7ca54-105">*変数* は、特定のデータ型の情報が格納されているメモリ位置を示す識別子です。</span><span class="sxs-lookup"><span data-stu-id="7ca54-105">A *variable* is an identifier that points to a memory location where information of a specific data type is stored.</span></span> <span data-ttu-id="7ca54-106">サイズ、精度、既定値、暗黙的および明示的[変換](xpp-conversion-run-time-functions.md)関数、範囲は、変数のデータ型によって異なります。</span><span class="sxs-lookup"><span data-stu-id="7ca54-106">The size, precision, default value, implicit and explicit [conversion](xpp-conversion-run-time-functions.md) functions, and range depend on the variable's data type.</span></span> 
- <span data-ttu-id="7ca54-107">変数の *スコープ* は、項目にアクセスできるコード内の領域を定義します。</span><span class="sxs-lookup"><span data-stu-id="7ca54-107">The *scope* of a variable defines the area in the code where an item can be accessed.</span></span> 
- <span data-ttu-id="7ca54-108">*インスタンス変数* はクラス宣言で宣言され、クラス内の任意のメソッドからまたは拡張クラスのメソッドからアクセスできます。</span><span class="sxs-lookup"><span data-stu-id="7ca54-108">*Instance variables* are declared in class declarations, and can be accessed from any methods in the class or from methods that extend the class.</span></span> 
- <span data-ttu-id="7ca54-109">*ローカル変数* は定義されたブロック内でのみアクセスできます。</span><span class="sxs-lookup"><span data-stu-id="7ca54-109">*Local variables* can be accessed only in the block where they were defined.</span></span> 
- <span data-ttu-id="7ca54-110">変数が宣言されると、メモリが割り当てられ、その変数が既定値に初期化されます。</span><span class="sxs-lookup"><span data-stu-id="7ca54-110">When a variable is declared, memory is allocated, and the variable is initialized to the default value.</span></span> 
- <span data-ttu-id="7ca54-111">静的フィールドおよびインスタンス フィールドの両方に、値を declaration ステートメントの一部として割り当てることができます。</span><span class="sxs-lookup"><span data-stu-id="7ca54-111">You can assign values to both static fields and instance fields as part of the declaration statement.</span></span> 
- <span data-ttu-id="7ca54-112">変数は、メソッドのコード ブロック内の任意の場所で宣言できます。</span><span class="sxs-lookup"><span data-stu-id="7ca54-112">Variables can be declared anywhere in a code block in a method.</span></span> <span data-ttu-id="7ca54-113">これらは、メソッドの先頭で宣言される必要はありません。</span><span class="sxs-lookup"><span data-stu-id="7ca54-113">They don't have to be declared at the beginning of a method.</span></span> 
- <span data-ttu-id="7ca54-114">*定数* は、変数が宣言されたときに値を変更できない変数です。</span><span class="sxs-lookup"><span data-stu-id="7ca54-114">*Constants* are variables where the value can't be changed when the variable is declared.</span></span> <span data-ttu-id="7ca54-115">**const** キーワードまたは **readonly** キーワードを使用します。</span><span class="sxs-lookup"><span data-stu-id="7ca54-115">They use the **const** or **readonly** keyword.</span></span> 
- <span data-ttu-id="7ca54-116">定数は 1 つの方法で *読み取り専用のフィールド* とは異なります。</span><span class="sxs-lookup"><span data-stu-id="7ca54-116">Constants differ from *read-only fields* in only one way.</span></span> <span data-ttu-id="7ca54-117">読み取り専用フィールドには値を 1 回だけ割り当てることができ、その値は変わりません。</span><span class="sxs-lookup"><span data-stu-id="7ca54-117">Read-only fields can be assigned a value only one time, and that value never changes.</span></span> <span data-ttu-id="7ca54-118">フィールドには、フィールドが宣言されている場所、またはコンストラクターのいずれかでインラインで値を割り当てることができます。</span><span class="sxs-lookup"><span data-stu-id="7ca54-118">The field can be assigned its value either inline, at the place where the field is declared, or in the constructor.</span></span> 

<span data-ttu-id="7ca54-119">X++ で作成されていないマネージ型の変数を宣言するときは、2 つのオプションがあります。</span><span class="sxs-lookup"><span data-stu-id="7ca54-119">When you declare variables of managed types that aren't authored in X++, you have two options.</span></span> <span data-ttu-id="7ca54-120">完全な名前空間を含めることにより宣言内のタイプ名を完全に修飾、または **using** ステートメントをファイルに追加してから名前空間をタイプ名から省略することができます。</span><span class="sxs-lookup"><span data-stu-id="7ca54-120">You can fully qualify the type names in the declaration by including the full namespace, or you can add a **using** statement to your file and then omit the namespace from the type name.</span></span>

## <a name="variable-examples"></a><span data-ttu-id="7ca54-121">変数の例</span><span class="sxs-lookup"><span data-stu-id="7ca54-121">Variable examples</span></span>

```xpp
// An example of two valid variable names.
str variableName;
CustInfo custNumber;

// An example of simultaneously declaring and initializing a variable.
real pi = 3.14159265359; // Assigns value of pi to 12 significant digits.

// An example of initializing an object by using the new method on the class.
Access accessObject = new Access(); // Simple call to the new method in the Access class.

// An example of multiple declarations using integers.
int i,j; // Declares 2 integers, i and j.

// An example of multiple declarations using an array.
int a[100,5], b=1; // Declares array with 100 integers with 5 in memory and b as an integer with value 1.

// An example of how variable scopes work.
class ScopeExample
{
    // The variable a is declared within the class.
    int a;

    // Because the method below is declared within the class,
    // it can access all the variables defined within the class.
    void aNewMethod()
    {
        // The variable b is declared within the method.
        // It can only be accessed by this method.
        int b;
    }
}

// An example of an assignment of field members inline.
public class FieldAssignmentExample
{
    int field1 = 1;
    str field2 = "Banana";
    void new()
    {
        // ...
    }
}

class ConstantExample
{
    // An example of a constant being declared at the class level.
    public const str MyContent = 'SomeValue';
    public int ResultSoFar()
    {
        return 1;
    }
}

// The constants can then be referenced by using the double-colon syntax.
str value = ConstantExample::MyContent;
// If you're in the scope of the class where the const is defined, 
// you can omit the type name prefix (ConstantExample in this example).

// An example of the using clause where the alias can denote
// namespaces and classes.
using System;
using IONS=System.IO; // Namespace alias.
using Alist=System.Collections.ArrayList; // Class alias.
public class NamespaceExample
{
    public static void Main(Args a)
    {
        Int32 I; // Alternative to System.Int32.
        Alist al; // Using a class alias.
        al = new Alist();
        str s;
        al.Add(1);
        IONS.Path::ChangeExtension(@"c:\tmp\test.xml", ".txt");
    }
}
```

## <a name="var"></a><span data-ttu-id="7ca54-122">var</span><span class="sxs-lookup"><span data-stu-id="7ca54-122">var</span></span>

<span data-ttu-id="7ca54-123">コンパイラが初期化式から種類を判断することができる場合は、変数の種類を明示的に提供せずに変数を宣言することができます。</span><span class="sxs-lookup"><span data-stu-id="7ca54-123">You can declare a variable without explicitly providing the type of the variable, if the compiler can determine the type from the initialization expression.</span></span> <span data-ttu-id="7ca54-124">変数は、まだ厳密に型指定されている明確な型です。</span><span class="sxs-lookup"><span data-stu-id="7ca54-124">The variable is still strongly-typed into one, unambiguous type.</span></span> 

<span data-ttu-id="7ca54-125">**var** は初期化式が提供されている宣言でのみ使用することができます。</span><span class="sxs-lookup"><span data-stu-id="7ca54-125">You can use **var** only on declarations where initialization expressions are provided.</span></span> <span data-ttu-id="7ca54-126">(コンパイラは、初期化式から種類を推定します。) 場合によっては、この方法によって、コードが読みやすくなります。</span><span class="sxs-lookup"><span data-stu-id="7ca54-126">(The compiler will infer the type from the initialization expression.) In some cases, this approach can make code easier to read.</span></span> 

<span data-ttu-id="7ca54-127">こうした状況でローカル変数を宣言するには、**var** を使用してください。</span><span class="sxs-lookup"><span data-stu-id="7ca54-127">You should use **var** to declare local variables in these situations:</span></span>

- <span data-ttu-id="7ca54-128">変数の型が右側の割り当てから明らかなとき</span><span class="sxs-lookup"><span data-stu-id="7ca54-128">When the type of the variable is obvious from the right side of the assignment</span></span>
- <span data-ttu-id="7ca54-129">正確な型が重要でないとき</span><span class="sxs-lookup"><span data-stu-id="7ca54-129">When the exact type isn't important</span></span>
- <span data-ttu-id="7ca54-130">ループ カウンター **用** の申告について</span><span class="sxs-lookup"><span data-stu-id="7ca54-130">For the declarations of **for** loop counters</span></span>
- <span data-ttu-id="7ca54-131">**using** ステートメント内での破棄可能なオブジェクト対象</span><span class="sxs-lookup"><span data-stu-id="7ca54-131">For disposable objects inside **using** statements</span></span>

<span data-ttu-id="7ca54-132">種類が初期化式からクリアされていない際は、**var** を使用しないでください。</span><span class="sxs-lookup"><span data-stu-id="7ca54-132">Don't use **var** when the type isn't clear from the initialization expression.</span></span>

## <a name="var-examples"></a><span data-ttu-id="7ca54-133">var の例</span><span class="sxs-lookup"><span data-stu-id="7ca54-133">var examples</span></span>

```xpp
// When the type of a variable is clear from
// the context, use var in the declaration.
var var1 = "This is clearly a string.";
var var2 = 27; // This is an integer (not a real).
var i = System.Convert::ToInt32(3.4);

// Don't use var when the type of the variable is not clear
// from the context. Use an explicit type instead.
int var4 = myObject.ResultSoFar();
```

## <a name="declare-anywhere"></a><span data-ttu-id="7ca54-134">任意の場所で宣言</span><span class="sxs-lookup"><span data-stu-id="7ca54-134">Declare anywhere</span></span>

<span data-ttu-id="7ca54-135">ステートメントを提供できる場所に宣言を提供できるようになりました。</span><span class="sxs-lookup"><span data-stu-id="7ca54-135">Declarations can now be provided wherever statements can be provided.</span></span> <span data-ttu-id="7ca54-136">宣言は、構文的にはステートメントで、*宣言ステートメント* です。</span><span class="sxs-lookup"><span data-stu-id="7ca54-136">A declaration is syntactically a statement, a *declaration statement*.</span></span> 

<span data-ttu-id="7ca54-137">変数は使用される直前に宣言することができます。すべての変数を 1 つの場所で宣言する必要はありません。</span><span class="sxs-lookup"><span data-stu-id="7ca54-137">You can provide declarations immediately before the variable is used, and you don’t have to declare all the variables in one place.</span></span> <span data-ttu-id="7ca54-138">したがって、変数のスコープを正確に制御できます。</span><span class="sxs-lookup"><span data-stu-id="7ca54-138">Therefore, you have precise control over the scope of your variables.</span></span> 

<span data-ttu-id="7ca54-139">変数を参照することができない場所で、変数に小さなスコープを付与することができます。</span><span class="sxs-lookup"><span data-stu-id="7ca54-139">You can give variables smaller scopes, outside which the variables can’t be referenced.</span></span> <span data-ttu-id="7ca54-140">変数の有効期間は宣言されているスコープです。</span><span class="sxs-lookup"><span data-stu-id="7ca54-140">The lifetime of the variable is the scope that it’s declared in.</span></span> <span data-ttu-id="7ca54-141">スコープは、**for** ステートメントおよび **using** ステートメント内においてブロック レベルで開始することができます (複合ステートメント内)。</span><span class="sxs-lookup"><span data-stu-id="7ca54-141">Scopes can be started at the block level (inside compound statements), in **for** statements, and in **using** statements.</span></span> 

<span data-ttu-id="7ca54-142">スコープを小さくすることにはいくつかの利点があります。</span><span class="sxs-lookup"><span data-stu-id="7ca54-142">There are several advantages to making scopes small:</span></span>

- <span data-ttu-id="7ca54-143">読みやすさが向上しました。</span><span class="sxs-lookup"><span data-stu-id="7ca54-143">Readability is enhanced.</span></span>
- <span data-ttu-id="7ca54-144">コードの長期保守中に変数が不適切な方法で再利用されるリスクを軽減します。</span><span class="sxs-lookup"><span data-stu-id="7ca54-144">You reduce the risk that a variable will be reused in an inappropriate manner during long-term maintenance of the code.</span></span>
- <span data-ttu-id="7ca54-145">コードをリファクターすることがより簡単です。</span><span class="sxs-lookup"><span data-stu-id="7ca54-145">It's easier to refactor code.</span></span> <span data-ttu-id="7ca54-146">再使用すべきでないコンテキストで変数が再使用される心配をせずに、コードをコピーすることができます。</span><span class="sxs-lookup"><span data-stu-id="7ca54-146">You can copy in code without having to worry that variables might be reused in contexts where they shouldn’t be reused.</span></span>

<span data-ttu-id="7ca54-147">次の例では、使用される **for** ステートメント内のループ カウンターを宣言します。</span><span class="sxs-lookup"><span data-stu-id="7ca54-147">In the following example, we declare the loop counter inside the **for** statement that it's used in.</span></span>

```xpp
void MyMethod()
{
    for (int i = 0; i < 10; i++)
    {
        info(strfmt("i is %1", i));
    }
}
```

<span data-ttu-id="7ca54-148">変数のスコープは **for** ステートメントそのものであり、条件式とループ更新部分を含みます。</span><span class="sxs-lookup"><span data-stu-id="7ca54-148">The scope of the variable is the **for** statement itself, and includes the condition expression and the loop update parts.</span></span> <span data-ttu-id="7ca54-149">この範囲外で値を使用することはできません。</span><span class="sxs-lookup"><span data-stu-id="7ca54-149">The value can’t be used outside this scope.</span></span> 

<span data-ttu-id="7ca54-150">次の例では、コンパイラが **info** ステートメントに達すると、「'i' が宣言されていません」というエラー メッセージを発行します。</span><span class="sxs-lookup"><span data-stu-id="7ca54-150">In the following example, when the compiler reaches the **info** statement, it will issue the following error message: "'i' isn't declared."</span></span>

```xpp
void MyMethod()
{
    for (int i = 0; i < 10; i++)
    {
        if (i == 7)
        {
            break;
        }
    }
    // The next statement causes a compiler error.
    info(strfmt("Found: %1", i));
}
```

<span data-ttu-id="7ca54-151">また、以下の例に示されるように、変数を **using** ステートメントにスコープすることができます。</span><span class="sxs-lookup"><span data-stu-id="7ca54-151">You can also scope variables to a **using** statement, as shown in the following example.</span></span>

```xpp
static void AnotherMethod()
{
    str textFromFile;
    using (System.IO.StreamReader sr = new System.IO.StreamReader("c:\\test.txt"))
    {
        textFromFile = sr.ReadToEnd();
    }
}
```

<span data-ttu-id="7ca54-152">**IDisposable** を実装するオブジェクトを使用するときは、**using** ステートメントで、そのオブジェクトを宣言し、インスタンスを作成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="7ca54-152">When you use an object that implements **IDisposable**, you should declare and instantiate that object in a **using** statement.</span></span> <span data-ttu-id="7ca54-153">**using** ステートメントは、オブジェクトのメソッドを呼び出すときに例外が発生した場合でも、正しい方法でオブジェクトの **Dispose** メソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="7ca54-153">The **using** statement calls the **Dispose** method on the object correctly, even if an exception occurs while you're calling methods on the object.</span></span> <span data-ttu-id="7ca54-154">オブジェクトを **try** ブロック内に配置してから **finally** ブロック内で **Dispose** を明示的に呼び出すことにより、同じ結果を達成することができます。</span><span class="sxs-lookup"><span data-stu-id="7ca54-154">You can achieve the same result by putting the object inside a **try** block and then explicitly calling **Dispose** in a **finally** block.</span></span> <span data-ttu-id="7ca54-155">実際、コンパイラはこの方法だけで **using** ステートメントを変換します。</span><span class="sxs-lookup"><span data-stu-id="7ca54-155">In fact, the compiler translates the **using** statement in just this manner.</span></span> 

<span data-ttu-id="7ca54-156">次の例は、説明してきた機能のいくつかを示しています。</span><span class="sxs-lookup"><span data-stu-id="7ca54-156">The following example shows some of the features that we have been describing.</span></span>

```xpp
// loop variable declared within the loop: It will
// not be misused outside the loop
for(int i = 1; i < 10; i++)
{
    // Because this value is not used from outside the loop,
    // its declaration belongs in this smaller scope.
    str s = int2str(i);
    info(s);
}
```

<span data-ttu-id="7ca54-157">混乱を避けるために、コンパイラは囲みスコープ内または同じスコープであっても、別の変数を隠す変数を導入しようとすると、エラー メッセージを発行します。</span><span class="sxs-lookup"><span data-stu-id="7ca54-157">To prevent confusion, the compiler issues an error message if you try to introduce a variable that will hide another variable in an enclosing scope, or even in the same scope.</span></span> <span data-ttu-id="7ca54-158">たとえば、次のコードは、以下の診断メッセージを発行するコンパイラの原因になります: 「i と呼ばれるローカルの変数はこのスコープでは宣言されません。それは既に親または現在のスコープで別のものを表示している i が別の意味になってしまうためです。」</span><span class="sxs-lookup"><span data-stu-id="7ca54-158">For example, the following code will cause the compiler to issue the following diagnostic message: "A local variable named 'i' can't be declared in this scope because it would give a different meaning to 'i', which is already used in a parent or current scope to denote something else."</span></span>

```xpp
{
    int i;
    {
        int i;
    }
}
```

## <a name="constants-read-only-variables-and-macros"></a><span data-ttu-id="7ca54-159">定数、読み取り専用変数、およびマクロ</span><span class="sxs-lookup"><span data-stu-id="7ca54-159">Constants, read-only variables, and macros</span></span>

<span data-ttu-id="7ca54-160">マクロの概念は完全にサポートされています。</span><span class="sxs-lookup"><span data-stu-id="7ca54-160">The concept of macros is fully supported.</span></span> <span data-ttu-id="7ca54-161">ただし、定数にはマクロに比べて次のような利点があります。</span><span class="sxs-lookup"><span data-stu-id="7ca54-161">Constants have the following advantages over macros:</span></span>

- <span data-ttu-id="7ca54-162">ドキュメント コメントは定数に対して追加することができますが、マクロの値に対して追加することはできません。</span><span class="sxs-lookup"><span data-stu-id="7ca54-162">You can add a documentation comment to a constant but not to the value of a macro.</span></span> <span data-ttu-id="7ca54-163">最終的に、言語サービスはこのコメントを受け取り、ユーザーに有用な情報を提供します。</span><span class="sxs-lookup"><span data-stu-id="7ca54-163">Eventually, the language service will pick up this comment and provide useful information to the user.</span></span>
- <span data-ttu-id="7ca54-164">定数は、IntelliSense で知られています。</span><span class="sxs-lookup"><span data-stu-id="7ca54-164">A constant is known by IntelliSense.</span></span>
- <span data-ttu-id="7ca54-165">定数は、相互参照です。</span><span class="sxs-lookup"><span data-stu-id="7ca54-165">A constant is cross-referenced.</span></span> <span data-ttu-id="7ca54-166">したがって、マクロではなく、特定の定数のすべての参照を見つけることができます。</span><span class="sxs-lookup"><span data-stu-id="7ca54-166">Therefore, you can find all references for a specific constant but not for a macro.</span></span>
- <span data-ttu-id="7ca54-167">定数は、アクセス修飾子が適用されます。</span><span class="sxs-lookup"><span data-stu-id="7ca54-167">A constant is subject to access modifiers.</span></span> <span data-ttu-id="7ca54-168">**private**、**protected**、および **public** モディファイアを使用することができます。</span><span class="sxs-lookup"><span data-stu-id="7ca54-168">You can use the **private**, **protected**, and **public** modifiers.</span></span> <span data-ttu-id="7ca54-169">マクロのアクセシビリティが厳密に定義されていません。</span><span class="sxs-lookup"><span data-stu-id="7ca54-169">The accessibility of macros isn't rigorously defined.</span></span>
- <span data-ttu-id="7ca54-170">定数変数にはスコープがありますが、マクロにはスコープがありません。</span><span class="sxs-lookup"><span data-stu-id="7ca54-170">Constant variables have scope, whereas macros don't have scope.</span></span>
- <span data-ttu-id="7ca54-171">デバッガーには定数の値または読み取り専用変数を表示することができます。</span><span class="sxs-lookup"><span data-stu-id="7ca54-171">You can see the value of a constant or a read-only variable in the debugger.</span></span>

<span data-ttu-id="7ca54-172">クラス スコープ (つまりクラスの宣言) で定義されているマクロは、すべての派生クラスのすべてのメソッドで効率的に使用できます。</span><span class="sxs-lookup"><span data-stu-id="7ca54-172">Macros that are defined in class scopes (that is, in class declarations) are effectively available in all methods of all derived classes.</span></span> <span data-ttu-id="7ca54-173">この機能は元はレガシ コンパイラ マクロの実装におけるバグしたが、ただし、多くのアプリケーション プログラマが多くの場合それを活用できるようになりました。</span><span class="sxs-lookup"><span data-stu-id="7ca54-173">This feature was originally a bug in the implementation of the legacy compiler macro, however, many application programmers often take advantage of it now.</span></span> <span data-ttu-id="7ca54-174">X++ コンパイラには、この機能が残されていますが、この機能を使用する新しいコードは記述しないでください。</span><span class="sxs-lookup"><span data-stu-id="7ca54-174">The X++ compiler still honors this feature, but no new code that uses it should be written.</span></span> <span data-ttu-id="7ca54-175">この機能は、コンパイラのパフォーマンスにも大きな影響を与えます。</span><span class="sxs-lookup"><span data-stu-id="7ca54-175">This feature also has a significant effect on the performance of the compiler.</span></span> 

<span data-ttu-id="7ca54-176">次の例に示すように、定数はクラス レベルで宣言できます。</span><span class="sxs-lookup"><span data-stu-id="7ca54-176">Constants can be declared at the class level, as shown in the following example.</span></span>

```xpp
private const str MyConstant = 'SomeValue';
```

<span data-ttu-id="7ca54-177">次に、定数を二重コロン (::) 構文を使用して参照することができます。</span><span class="sxs-lookup"><span data-stu-id="7ca54-177">The constants can then be referenced by using the double colon (::) syntax.</span></span>

```xpp
str value = MyClass::MyConstant;
```

<span data-ttu-id="7ca54-178">定数 (**const**) が定義されているクラスのスコープにいる場合は、型名の接頭語 (上記の例では **MyClass**) を省略できます。</span><span class="sxs-lookup"><span data-stu-id="7ca54-178">If you're in the scope of the class where the constant (**const**) is defined, you can omit the type name prefix (**MyClass** in the preceding example).</span></span> <span data-ttu-id="7ca54-179">したがって、マクロ ライブラリの概念を簡単に実装することができます。</span><span class="sxs-lookup"><span data-stu-id="7ca54-179">Therefore, you can easily implement the concept of a macro library.</span></span> <span data-ttu-id="7ca54-180">マクロ シンボルのリストは、パブリック **const** の定義を持つクラスになります。</span><span class="sxs-lookup"><span data-stu-id="7ca54-180">The list of macro symbols becomes a class that has public **const** definitions.</span></span> 

<span data-ttu-id="7ca54-181">また、定数を変数のみとして定義することができます。</span><span class="sxs-lookup"><span data-stu-id="7ca54-181">You can also define constants as variables only.</span></span> <span data-ttu-id="7ca54-182">コンパイラはインバリアントを維持して、値を変更できないようにします。</span><span class="sxs-lookup"><span data-stu-id="7ca54-182">The compiler will maintain the invariant so that the value can't be modified.</span></span>

```xpp
{
    const int Blue = 0x0000FF;
    const int Green = 0x00FF00;
    const int Red = 0xFF0000;
}
```

## <a name="null-values-for-data-types"></a><span data-ttu-id="7ca54-183">データ型の null 値</span><span class="sxs-lookup"><span data-stu-id="7ca54-183">Null values for data types</span></span>
<span data-ttu-id="7ca54-184">その他の数多くのデータベース管理システム (DBMS) で使用できる **null** 値の概念がサポートされていません。</span><span class="sxs-lookup"><span data-stu-id="7ca54-184">The concept of **null** values that is available in many other database management systems (DBMSs) is not supported.</span></span> <span data-ttu-id="7ca54-185">X++ の変数は、常にタイプと値を持ちます。ただし、各データ タイプでは、1 つの値が **null** と見なされます (たとえば、**validateField** テーブル メソッドの実行時)。</span><span class="sxs-lookup"><span data-stu-id="7ca54-185">A variable in X++ always has a type and a value, however, for each data type, one value is considered **null** (for example, when the **validateField** table method is run).</span></span>

| <span data-ttu-id="7ca54-186">種類</span><span class="sxs-lookup"><span data-stu-id="7ca54-186">Type</span></span> | <span data-ttu-id="7ca54-187">null として扱われる値</span><span class="sxs-lookup"><span data-stu-id="7ca54-187">Value that is treated as null</span></span> |
|------|-------------------------------|
| <span data-ttu-id="7ca54-188">日</span><span class="sxs-lookup"><span data-stu-id="7ca54-188">Date</span></span>        | <span data-ttu-id="7ca54-189">1900-01-01</span><span class="sxs-lookup"><span data-stu-id="7ca54-189">1900-01-01</span></span>                                              |
| <span data-ttu-id="7ca54-190">列挙</span><span class="sxs-lookup"><span data-stu-id="7ca54-190">Enum</span></span>        | <span data-ttu-id="7ca54-191">その値が **0** に設定されている要素</span><span class="sxs-lookup"><span data-stu-id="7ca54-191">An element that has its value set to **0**</span></span>              |
| <span data-ttu-id="7ca54-192">整数</span><span class="sxs-lookup"><span data-stu-id="7ca54-192">Integer</span></span>     | <span data-ttu-id="7ca54-193">0</span><span class="sxs-lookup"><span data-stu-id="7ca54-193">0</span></span>                                                       |
| <span data-ttu-id="7ca54-194">実数</span><span class="sxs-lookup"><span data-stu-id="7ca54-194">Real</span></span>        | <span data-ttu-id="7ca54-195">0.0</span><span class="sxs-lookup"><span data-stu-id="7ca54-195">0.0</span></span>                                                     |
| <span data-ttu-id="7ca54-196">文字列</span><span class="sxs-lookup"><span data-stu-id="7ca54-196">String</span></span>      | <span data-ttu-id="7ca54-197">空の文字列</span><span class="sxs-lookup"><span data-stu-id="7ca54-197">An empty string</span></span>                                         |
| <span data-ttu-id="7ca54-198">時刻</span><span class="sxs-lookup"><span data-stu-id="7ca54-198">Time</span></span>        | <span data-ttu-id="7ca54-199">00:00:00</span><span class="sxs-lookup"><span data-stu-id="7ca54-199">00:00:00</span></span>                                                |
| <span data-ttu-id="7ca54-200">Utcdatetime</span><span class="sxs-lookup"><span data-stu-id="7ca54-200">Utcdatetime</span></span> | <span data-ttu-id="7ca54-201">時間部分の値に関係なく、日付部が **1900-01-01** に設定されている値。</span><span class="sxs-lookup"><span data-stu-id="7ca54-201">Any value that has its date portion set to **1900-01-01**, regardless of the value of the time portion.</span></span> <span data-ttu-id="7ca54-202">たとえば、値 **1900-01-01T22:33:44** は **null** として扱われます。</span><span class="sxs-lookup"><span data-stu-id="7ca54-202">For example, the value **1900-01-01T22:33:44** is treated as **null**.</span></span> <span data-ttu-id="7ca54-203">日付部分が **1900-01-01** に設定されている **utcDateTime** 値は X++ **print** ステートメントでは空白で表示されることに注意してください。</span><span class="sxs-lookup"><span data-stu-id="7ca54-203">Note that any **utcDateTime** value that has its date portion set to **1900-01-01** is shown as blank by the X++ **print** statement.</span></span> <span data-ttu-id="7ca54-204">**1900-01-01T00:00:00** 値のみ空白として **Global::info** メソッドにより表示されます。</span><span class="sxs-lookup"><span data-stu-id="7ca54-204">Only the value **1900-01-01T00:00:00** is shown as blank by the **Global::info** method.</span></span> <span data-ttu-id="7ca54-205">値は、**DateTimeUtil::MinValue** メソッドの値です。</span><span class="sxs-lookup"><span data-stu-id="7ca54-205">That value is the value from the **DateTimeUtil::MinValue** method.</span></span> |

<span data-ttu-id="7ca54-206">したがって、**validateField** メソッドによりユーザーが必須項目に入力したかどうかがチェックされる際、たとえば、**0** は **integer** タイプ フィールドで許容されず、最初のエントリは **enum** タイプ フィールドで許容されません。</span><span class="sxs-lookup"><span data-stu-id="7ca54-206">When the **validateField** method checks whether a user has entered a value in a mandatory field, **0** isn't accepted in an **integer** type field, the first entry isn't accepted in an **enum** type field, and so on.</span></span> <span data-ttu-id="7ca54-207">また、SQL X++ ステートメントで、前のテーブルにリストされている値は、ブール値比較で **false** になります。</span><span class="sxs-lookup"><span data-stu-id="7ca54-207">Additionally, in SQL X++ statements, the values that are listed in the previous table yield **false** in a Boolean comparison.</span></span> <span data-ttu-id="7ca54-208">ただし、非 SQL X++ ステートメントでは、同等演算子およびリレーショナル演算子は他の値に対して動作するのと同じように、これらの値に対して動作します。</span><span class="sxs-lookup"><span data-stu-id="7ca54-208">However, in non-SQL X++ statements, the equal and relational operators work with these values, just as they work with other values.</span></span> <span data-ttu-id="7ca54-209">従来の DBMS の意味では、**コンテナー** 型と **テーブル** 型のクラスおよび変数は **null** とすることができます。</span><span class="sxs-lookup"><span data-stu-id="7ca54-209">Variables of the **container** type, and classes and variables of the **table** type can be **null** in the traditional DBMS sense.</span></span> <span data-ttu-id="7ca54-210">**テーブル** タイプは、すべてのフィールドに **null** 値がある場合は **null** です。</span><span class="sxs-lookup"><span data-stu-id="7ca54-210">A **table** type is **null** if all its fields have their **null** value.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]