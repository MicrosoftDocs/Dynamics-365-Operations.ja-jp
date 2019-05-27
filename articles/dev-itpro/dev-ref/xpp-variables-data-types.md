---
title: X++ の変数とデータ型
description: このトピックでは、X++ の変数とデータ型について説明します。
author: RobinARH
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Developer
ms.reviewer: robinr
ms.search.scope: Operations
ms.custom: 150183
ms.assetid: 0ff4e759-851d-4b53-aa67-6f03eee53f02
ms.search.region: Global
ms.author: robinr
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: c33fd7ce86552ee6c05688fb8caefbb1f363257b
ms.sourcegitcommit: 2b890cd7a801055ab0ca24398efc8e4e777d4d8c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/07/2019
ms.locfileid: "1536984"
---
# <a name="x-variables-and-data-types"></a><span data-ttu-id="266e4-103">X++ の変数とデータ型</span><span class="sxs-lookup"><span data-stu-id="266e4-103">X++ variables and data types</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="266e4-104">このトピックでは、X++ の変数とデータ型について説明します。</span><span class="sxs-lookup"><span data-stu-id="266e4-104">This topic describes variables and data types in X++.</span></span>

<a name="variables"></a><span data-ttu-id="266e4-105">変数</span><span class="sxs-lookup"><span data-stu-id="266e4-105">Variables</span></span>
---------

<span data-ttu-id="266e4-106">*変数*は、特定のデータ型の情報が格納されているメモリ位置を示す識別子です。</span><span class="sxs-lookup"><span data-stu-id="266e4-106">A *variable* is an identifier that points to a memory location where information of a specific data type is stored.</span></span> <span data-ttu-id="266e4-107">サイズ、精度、既定値、暗黙的および明示的[変換](xpp-conversion-run-time-functions.md)関数、範囲は、変数のデータ型によって異なります。</span><span class="sxs-lookup"><span data-stu-id="266e4-107">The size, precision, default value, implicit and explicit [conversion](xpp-conversion-run-time-functions.md) functions, and range depend on the variable's data type.</span></span> <span data-ttu-id="266e4-108">変数の*スコープ*は、項目にアクセスできるコード内の領域を定義します。</span><span class="sxs-lookup"><span data-stu-id="266e4-108">The *scope* of a variable defines the area in the code where an item can be accessed.</span></span> <span data-ttu-id="266e4-109">*インスタンス変数*はクラス宣言で宣言され、クラス内の任意のメソッドからまたは拡張クラスのメソッドからアクセスできます。</span><span class="sxs-lookup"><span data-stu-id="266e4-109">*Instance variables* are declared in class declarations, and can be accessed from any methods in the class or from methods that extend the class.</span></span> <span data-ttu-id="266e4-110">*ローカル変数*は定義されたブロック内でのみアクセスできます。</span><span class="sxs-lookup"><span data-stu-id="266e4-110">*Local variables* can be accessed only in the block where they were defined.</span></span> <span data-ttu-id="266e4-111">変数が宣言されると、メモリが割り当てられ、その変数が既定値に初期化されます。</span><span class="sxs-lookup"><span data-stu-id="266e4-111">When a variable is declared, memory is allocated, and the variable is initialized to the default value.</span></span> <span data-ttu-id="266e4-112">静的フィールドおよびインスタンス フィールドの両方に、値を declaration ステートメントの一部として割り当てることができます。</span><span class="sxs-lookup"><span data-stu-id="266e4-112">You can assign values to both static fields and instance fields as part of the declaration statement.</span></span> <span data-ttu-id="266e4-113">変数は、メソッドのコード ブロック内の任意の場所で宣言できます。</span><span class="sxs-lookup"><span data-stu-id="266e4-113">Variables can be declared anywhere in a code block in a method.</span></span> <span data-ttu-id="266e4-114">これらは、メソッドの先頭で宣言される必要はありません。</span><span class="sxs-lookup"><span data-stu-id="266e4-114">They don't have to be declared at the beginning of a method.</span></span> <span data-ttu-id="266e4-115">*定数*は、変数が宣言されたときに値を変更できない変数です。</span><span class="sxs-lookup"><span data-stu-id="266e4-115">*Constants* are variables where the value can't be changed when the variable is declared.</span></span> <span data-ttu-id="266e4-116">**const** キーワードまたは **readonly** キーワードを使用します。</span><span class="sxs-lookup"><span data-stu-id="266e4-116">They use the **const** or **readonly** keyword.</span></span> <span data-ttu-id="266e4-117">定数は 1 つの方法で*読み取り専用のフィールド*とは異なります。</span><span class="sxs-lookup"><span data-stu-id="266e4-117">Constants differ from *read-only fields* in only one way.</span></span> <span data-ttu-id="266e4-118">読み取り専用フィールドには値を 1 回だけ割り当てることができ、その値は変わりません。</span><span class="sxs-lookup"><span data-stu-id="266e4-118">Read-only fields can be assigned a value only one time, and that value never changes.</span></span> <span data-ttu-id="266e4-119">フィールドには、フィールドが宣言されている場所、またはコンストラクターのいずれかでインラインで値を割り当てることができます。</span><span class="sxs-lookup"><span data-stu-id="266e4-119">The field can be assigned its value either inline, at the place where the field is declared, or in the constructor.</span></span> <span data-ttu-id="266e4-120">X++ で作成されていないマネージ型の変数を宣言するときは、2 つのオプションがあります。</span><span class="sxs-lookup"><span data-stu-id="266e4-120">When you declare variables of managed types that aren't authored in X++, you have two options.</span></span> <span data-ttu-id="266e4-121">完全な名前空間を含めることにより宣言内のタイプ名を完全に修飾、または **using** ステートメントをファイルに追加してから名前空間をタイプ名から省略することができます。</span><span class="sxs-lookup"><span data-stu-id="266e4-121">You can fully qualify the type names in the declaration by including the full namespace, or you can add a **using** statement to your file and then omit the namespace from the type name.</span></span>

### <a name="variable-examples"></a><span data-ttu-id="266e4-122">変数の例</span><span class="sxs-lookup"><span data-stu-id="266e4-122">Variable examples</span></span>

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
            s.IONS.Path::ChangeExtension(@"c:\tmp\test.xml", ".txt");
        }
    }

### <a name="var"></a><span data-ttu-id="266e4-123">var</span><span class="sxs-lookup"><span data-stu-id="266e4-123">var</span></span>

<span data-ttu-id="266e4-124">コンパイラが初期化式から種類を判断することができる場合は、変数の種類を明示的に提供せずに変数を宣言することができます。</span><span class="sxs-lookup"><span data-stu-id="266e4-124">You can declare a variable without explicitly providing the type of the variable, if the compiler can determine the type from the initialization expression.</span></span> <span data-ttu-id="266e4-125">変数は、まだ厳密に型指定されている明確な型です。</span><span class="sxs-lookup"><span data-stu-id="266e4-125">The variable is still strongly-typed into one, unambiguous type.</span></span> <span data-ttu-id="266e4-126">**var** は初期化式が提供されている宣言でのみ使用することができます。</span><span class="sxs-lookup"><span data-stu-id="266e4-126">You can use **var** only on declarations where initialization expressions are provided.</span></span> <span data-ttu-id="266e4-127">(コンパイラは、初期化式から種類を推定します。) 場合によっては、この方法によって、コードが読みやすくなります。</span><span class="sxs-lookup"><span data-stu-id="266e4-127">(The compiler will infer the type from the initialization expression.) In some cases, this approach can make code easier to read.</span></span> <span data-ttu-id="266e4-128">こうした状況でローカル変数を宣言するには、**var** を使用してください。</span><span class="sxs-lookup"><span data-stu-id="266e4-128">You should use **var** to declare local variables in these situations:</span></span>

-   <span data-ttu-id="266e4-129">変数の型が右側の割り当てから明らかなとき</span><span class="sxs-lookup"><span data-stu-id="266e4-129">When the type of the variable is obvious from the right side of the assignment</span></span>
-   <span data-ttu-id="266e4-130">正確な型が重要でないとき</span><span class="sxs-lookup"><span data-stu-id="266e4-130">When the exact type isn't important</span></span>
-   <span data-ttu-id="266e4-131">ループ カウンター**用**の申告について</span><span class="sxs-lookup"><span data-stu-id="266e4-131">For the declarations of **for** loop counters</span></span>
-   <span data-ttu-id="266e4-132">**using** ステートメント内での破棄可能なオブジェクト対象</span><span class="sxs-lookup"><span data-stu-id="266e4-132">For disposable objects inside **using** statements</span></span>

<span data-ttu-id="266e4-133">種類が初期化式からクリアされていない際は、**var** を使用しないでください。</span><span class="sxs-lookup"><span data-stu-id="266e4-133">Don't use **var** when the type isn't clear from the initialization expression.</span></span>

### <a name="var-examples"></a><span data-ttu-id="266e4-134">var の例</span><span class="sxs-lookup"><span data-stu-id="266e4-134">var examples</span></span>

    // When the type of a variable is clear from
    // the context, use var in the declaration.
    var var1 = "This is clearly a string.";
    var var2 = 27; // This is an integer (not a real).
    var i = System.Convert::ToInt32(3.4);

    // Don't use var when the type of the variable is not clear
    // from the context. Use an explicit type instead.
    int var4 = myObject.ResultSoFar();

### <a name="declare-anywhere"></a><span data-ttu-id="266e4-135">任意の場所で宣言</span><span class="sxs-lookup"><span data-stu-id="266e4-135">Declare anywhere</span></span>

<span data-ttu-id="266e4-136">ステートメントを提供できる場所に宣言を提供できるようになりました。</span><span class="sxs-lookup"><span data-stu-id="266e4-136">Declarations can now be provided wherever statements can be provided.</span></span> <span data-ttu-id="266e4-137">宣言は、構文的にはステートメントで、*宣言ステートメント*です。</span><span class="sxs-lookup"><span data-stu-id="266e4-137">A declaration is syntactically a statement, a *declaration statement*.</span></span> <span data-ttu-id="266e4-138">変数は使用される直前に宣言することができます。すべての変数を 1 つの場所で宣言する必要はありません。</span><span class="sxs-lookup"><span data-stu-id="266e4-138">You can provide declarations immediately before the variable is used, and you don’t have to declare all the variables in one place.</span></span> <span data-ttu-id="266e4-139">したがって、変数のスコープを正確に制御できます。</span><span class="sxs-lookup"><span data-stu-id="266e4-139">Therefore, you have precise control over the scope of your variables.</span></span> <span data-ttu-id="266e4-140">変数を参照することができない場所で、変数に小さなスコープを付与することができます。</span><span class="sxs-lookup"><span data-stu-id="266e4-140">You can give variables smaller scopes, outside which the variables can’t be referenced.</span></span> <span data-ttu-id="266e4-141">変数の有効期間は宣言されているスコープです。</span><span class="sxs-lookup"><span data-stu-id="266e4-141">The lifetime of the variable is the scope that it’s declared in.</span></span> <span data-ttu-id="266e4-142">スコープは、**for** ステートメントおよび **using** ステートメント内においてブロック レベルで開始することができます (複合ステートメント内)。</span><span class="sxs-lookup"><span data-stu-id="266e4-142">Scopes can be started at the block level (inside compound statements), in **for** statements, and in **using** statements.</span></span> <span data-ttu-id="266e4-143">スコープを小さくすることにはいくつかの利点があります。</span><span class="sxs-lookup"><span data-stu-id="266e4-143">There are several advantages to making scopes small:</span></span>

-   <span data-ttu-id="266e4-144">読みやすさが向上しました。</span><span class="sxs-lookup"><span data-stu-id="266e4-144">Readability is enhanced.</span></span>
-   <span data-ttu-id="266e4-145">コードの長期保守中に変数が不適切な方法で再利用されるリスクを軽減します。</span><span class="sxs-lookup"><span data-stu-id="266e4-145">You reduce the risk that a variable will be reused in an inappropriate manner during long-term maintenance of the code.</span></span>
-   <span data-ttu-id="266e4-146">コードをリファクターすることがより簡単です。</span><span class="sxs-lookup"><span data-stu-id="266e4-146">It's easier to refactor code.</span></span> <span data-ttu-id="266e4-147">再使用すべきでないコンテキストで変数が再使用される心配をせずに、コードをコピーすることができます。</span><span class="sxs-lookup"><span data-stu-id="266e4-147">You can copy in code without having to worry that variables might be reused in contexts where they shouldn’t be reused.</span></span>

<span data-ttu-id="266e4-148">次の例では、使用される **for** ステートメント内のループ カウンターを宣言します。</span><span class="sxs-lookup"><span data-stu-id="266e4-148">In the following example, we declare the loop counter inside the **for** statement that it's used in.</span></span>

    void MyMethod()
    {
        for (int i = 0; i < 10; i++)
        {
            info(strfmt("i is %1", i));
        }
    }

<span data-ttu-id="266e4-149">変数のスコープは **for** ステートメントそのものであり、条件式とループ更新部分を含みます。</span><span class="sxs-lookup"><span data-stu-id="266e4-149">The scope of the variable is the **for** statement itself, and includes the condition expression and the loop update parts.</span></span> <span data-ttu-id="266e4-150">この範囲外で値を使用することはできません。</span><span class="sxs-lookup"><span data-stu-id="266e4-150">The value can’t be used outside this scope.</span></span> <span data-ttu-id="266e4-151">次の例では、コンパイラが **info** ステートメントに達すると、「'i' が宣言されていません」というエラー メッセージを発行します。</span><span class="sxs-lookup"><span data-stu-id="266e4-151">In the following example, when the compiler reaches the **info** statement, it will issue the following error message: "'i' isn't declared."</span></span>

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

<span data-ttu-id="266e4-152">また、以下の例に示されるように、変数を **using** ステートメントにスコープすることができます。</span><span class="sxs-lookup"><span data-stu-id="266e4-152">You can also scope variables to a **using** statement, as shown in the following example.</span></span>

    static void AnotherMethod()
    {
        str textFromFile;
        using (System.IO.StreamReader sr = new System.IO.StreamReader("c:\\test.txt"))
        {
            textFromFile = sr.ReadToEnd();
        }
    }

<span data-ttu-id="266e4-153">**IDisposable** を実装するオブジェクトを使用するときは、**using** ステートメントで、そのオブジェクトを宣言し、インスタンスを作成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="266e4-153">When you use an object that implements **IDisposable**, you should declare and instantiate that object in a **using** statement.</span></span> <span data-ttu-id="266e4-154">**using** ステートメントは、オブジェクトのメソッドを呼び出すときに例外が発生した場合でも、正しい方法でオブジェクトの **Dispose** メソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="266e4-154">The **using** statement calls the **Dispose** method on the object correctly, even if an exception occurs while you're calling methods on the object.</span></span> <span data-ttu-id="266e4-155">オブジェクトを **try** ブロック内に配置してから **finally** ブロック内で **Dispose** を明示的に呼び出すことにより、同じ結果を達成することができます。</span><span class="sxs-lookup"><span data-stu-id="266e4-155">You can achieve the same result by putting the object inside a **try** block and then explicitly calling **Dispose** in a **finally** block.</span></span> <span data-ttu-id="266e4-156">実際、コンパイラはこの方法だけで **using** ステートメントを変換します。</span><span class="sxs-lookup"><span data-stu-id="266e4-156">In fact, the compiler translates the **using** statement in just this manner.</span></span> <span data-ttu-id="266e4-157">次の例は、説明してきた機能のいくつかを示しています。</span><span class="sxs-lookup"><span data-stu-id="266e4-157">The following example shows some of the features that we have been describing.</span></span>

    // loop variable declared within the loop: It will
    // not be misused outside the loop
    for(int i = 1; i < 10; i++)
    {
        // Because this value is not used from outside the loop,
        // its declaration belongs in this smaller scope.
        str s = int2str(i);
        info(s);
    }

<span data-ttu-id="266e4-158">混乱を避けるために、コンパイラは囲みスコープ内または同じスコープであっても、別の変数を隠す変数を導入しようとすると、エラー メッセージを発行します。</span><span class="sxs-lookup"><span data-stu-id="266e4-158">To prevent confusion, the compiler issues an error message if you try to introduce a variable that will hide another variable in an enclosing scope, or even in the same scope.</span></span> <span data-ttu-id="266e4-159">たとえば、次のコードは、以下の診断メッセージを発行するコンパイラの原因になります: 「i と呼ばれるローカルの変数はこのスコープでは宣言されません。それは既に親または現在のスコープで別のものを表示している i が別の意味になってしまうためです。」</span><span class="sxs-lookup"><span data-stu-id="266e4-159">For example, the following code will cause the compiler to issue the following diagnostic message: "A local variable named 'i' can't be declared in this scope because it would give a different meaning to 'i', which is already used in a parent or current scope to denote something else."</span></span>

    {
        int i;
        {
            int i;
        }
    }

### <a name="constants-read-only-variables-and-macros"></a><span data-ttu-id="266e4-160">定数、読み取り専用変数、およびマクロ</span><span class="sxs-lookup"><span data-stu-id="266e4-160">Constants, read-only variables, and macros</span></span>

<span data-ttu-id="266e4-161">マクロの概念は完全にサポートされています。</span><span class="sxs-lookup"><span data-stu-id="266e4-161">The concept of macros is fully supported.</span></span> <span data-ttu-id="266e4-162">ただし、定数にはマクロに比べて次のような利点があります。</span><span class="sxs-lookup"><span data-stu-id="266e4-162">However, constants have the following advantages over macros:</span></span>

-   <span data-ttu-id="266e4-163">ドキュメント コメントは定数に対して追加することができますが、マクロの値に対して追加することはできません。</span><span class="sxs-lookup"><span data-stu-id="266e4-163">You can add a documentation comment to a constant but not to the value of a macro.</span></span> <span data-ttu-id="266e4-164">最終的に、言語サービスはこのコメントを受け取り、ユーザーに有用な情報を提供します。</span><span class="sxs-lookup"><span data-stu-id="266e4-164">Eventually, the language service will pick up this comment and provide useful information to the user.</span></span>
-   <span data-ttu-id="266e4-165">定数は、IntelliSense で知られています。</span><span class="sxs-lookup"><span data-stu-id="266e4-165">A constant is known by IntelliSense.</span></span>
-   <span data-ttu-id="266e4-166">定数は、相互参照です。</span><span class="sxs-lookup"><span data-stu-id="266e4-166">A constant is cross-referenced.</span></span> <span data-ttu-id="266e4-167">したがって、マクロではなく、特定の定数のすべての参照を見つけることができます。</span><span class="sxs-lookup"><span data-stu-id="266e4-167">Therefore, you can find all references for a specific constant but not for a macro.</span></span>
-   <span data-ttu-id="266e4-168">定数は、アクセス修飾子が適用されます。</span><span class="sxs-lookup"><span data-stu-id="266e4-168">A constant is subject to access modifiers.</span></span> <span data-ttu-id="266e4-169">**private**、**protected**、および **public** モディファイアを使用することができます。</span><span class="sxs-lookup"><span data-stu-id="266e4-169">You can use the **private**, **protected**, and **public** modifiers.</span></span> <span data-ttu-id="266e4-170">マクロのアクセシビリティが厳密に定義されていません。</span><span class="sxs-lookup"><span data-stu-id="266e4-170">The accessibility of macros isn't rigorously defined.</span></span>
-   <span data-ttu-id="266e4-171">定数変数にはスコープがありますが、マクロにはスコープがありません。</span><span class="sxs-lookup"><span data-stu-id="266e4-171">Constant variables have scope, whereas macros don't have scope.</span></span>
-   <span data-ttu-id="266e4-172">デバッガーには定数の値または読み取り専用変数を表示することができます。</span><span class="sxs-lookup"><span data-stu-id="266e4-172">You can see the value of a constant or a read-only variable in the debugger.</span></span>

<span data-ttu-id="266e4-173">クラス スコープ (つまりクラスの宣言) で定義されているマクロは、すべての派生クラスのすべてのメソッドで効率的に使用できます。</span><span class="sxs-lookup"><span data-stu-id="266e4-173">Macros that are defined in class scopes (that is, in class declarations) are effectively available in all methods of all derived classes.</span></span> <span data-ttu-id="266e4-174">この機能は元はレガシ コンパイラ マクロの実装におけるバグでした。</span><span class="sxs-lookup"><span data-stu-id="266e4-174">This feature was originally a bug in the implementation of the legacy compiler macro.</span></span> <span data-ttu-id="266e4-175">ただし、多くのアプリケーション プログラマが多くの場合それを活用できるようになりました。</span><span class="sxs-lookup"><span data-stu-id="266e4-175">However, many application programmers often take advantage of it now.</span></span> <span data-ttu-id="266e4-176">X++ コンパイラには、この機能が残されていますが、この機能を使用する新しいコードは記述しないでください。</span><span class="sxs-lookup"><span data-stu-id="266e4-176">The X++ compiler still honors this feature, but no new code that uses it should be written.</span></span> <span data-ttu-id="266e4-177">この機能は、コンパイラのパフォーマンスにも大きな影響を与えます。</span><span class="sxs-lookup"><span data-stu-id="266e4-177">This feature also has a significant effect on the performance of the compiler.</span></span> <span data-ttu-id="266e4-178">次の例に示すように、定数はクラス レベルで宣言できます。</span><span class="sxs-lookup"><span data-stu-id="266e4-178">Constants can be declared at the class level, as shown in the following example.</span></span>

    private const str MyConstant = 'SomeValue';

<span data-ttu-id="266e4-179">次に、定数を二重コロン (::) 構文を使用して参照することができます。</span><span class="sxs-lookup"><span data-stu-id="266e4-179">The constants can then be referenced by using the double colon (::) syntax.</span></span>

    str value = MyClass::MyConstant;

<span data-ttu-id="266e4-180">定数 (**const**) が定義されているクラスのスコープにいる場合は、型名の接頭語 (上記の例では **MyClass**) を省略できます。</span><span class="sxs-lookup"><span data-stu-id="266e4-180">If you're in the scope of the class where the constant (**const**) is defined, you can omit the type name prefix (**MyClass** in the preceding example).</span></span> <span data-ttu-id="266e4-181">したがって、マクロ ライブラリの概念を簡単に実装することができます。</span><span class="sxs-lookup"><span data-stu-id="266e4-181">Therefore, you can easily implement the concept of a macro library.</span></span> <span data-ttu-id="266e4-182">マクロ シンボルのリストは、パブリック **const** の定義を持つクラスになります。</span><span class="sxs-lookup"><span data-stu-id="266e4-182">The list of macro symbols becomes a class that has public **const** definitions.</span></span> <span data-ttu-id="266e4-183">また、定数を変数のみとして定義することができます。</span><span class="sxs-lookup"><span data-stu-id="266e4-183">You can also define constants as variables only.</span></span> <span data-ttu-id="266e4-184">コンパイラはインバリアントを維持して、値を変更できないようにします。</span><span class="sxs-lookup"><span data-stu-id="266e4-184">The compiler will maintain the invariant so that the value can't be modified.</span></span>

    {
        const int Blue = 0x0000FF;
        const int Green = 0x00FF00;
        const int Red = 0xFF0000;
    }

## <a name="primitive-data-types"></a><span data-ttu-id="266e4-185">プリミティブ データ型</span><span class="sxs-lookup"><span data-stu-id="266e4-185">Primitive data types</span></span>
<span data-ttu-id="266e4-186">X++ のプリミティブ データ型は、**anytype**、**boolean**、**date**、**enum**、**guid**、**int**、**int64**、**real**、**str**、**timeOfDay**、および **utcdatetime** です。</span><span class="sxs-lookup"><span data-stu-id="266e4-186">The primitive data types in X++ are **anytype**, **boolean**, **date**, **enum**, **guid**, **int**, **int64**, **real**, **str**, **timeOfDay**, and **utcdatetime**.</span></span>

### <a name="anytype"></a><span data-ttu-id="266e4-187">anytype</span><span class="sxs-lookup"><span data-stu-id="266e4-187">anytype</span></span>

<span data-ttu-id="266e4-188">**anytype** データ型は任意のデータ型のプレースホルダーです。</span><span class="sxs-lookup"><span data-stu-id="266e4-188">The **anytype** data type is a placeholder for any data type.</span></span> <span data-ttu-id="266e4-189">このタイプの変数は、引数および戻り値としてのみ使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="266e4-189">You should use variables of this type only as arguments and return values.</span></span> <span data-ttu-id="266e4-190">**anytype** を変数として使用するには、最初に変数に値を割り当てる必要があります。</span><span class="sxs-lookup"><span data-stu-id="266e4-190">To use **anytype** as a variable, you must first assign a value to it.</span></span> <span data-ttu-id="266e4-191">それ以外の場合、実行時エラーが発生します。</span><span class="sxs-lookup"><span data-stu-id="266e4-191">Otherwise, a run-time error occurs.</span></span> <span data-ttu-id="266e4-192">**anytype** 値に割り当てた後、別のデータ型に変換することはできません。</span><span class="sxs-lookup"><span data-stu-id="266e4-192">After you've assigned a value to **anytype**, you can't convert it to another data type.</span></span> <span data-ttu-id="266e4-193">式に **anytype** の変数を使用できますが、通常は引数および戻り値の型として使用されます。</span><span class="sxs-lookup"><span data-stu-id="266e4-193">Although you can use **anytype** variables in expressions, they're usually used as arguments and return types.</span></span> <span data-ttu-id="266e4-194">サイズ、精度、有効範囲、既定値、**anytype** の範囲は、割り当てた変換タイプによって異なります。</span><span class="sxs-lookup"><span data-stu-id="266e4-194">The size, precision, scope, default value, and range of **anytype** depend on the conversion type that you assign to it.</span></span> <span data-ttu-id="266e4-195">変換対象のデータ タイプを使用するように、**anytype** を使用することができます。</span><span class="sxs-lookup"><span data-stu-id="266e4-195">You can use **anytype** just as you use the data type that you convert it to.</span></span> <span data-ttu-id="266e4-196">たとえば、整数を割り当てる場合、変数にリレーショナル演算子と算術演算子を適用できます。</span><span class="sxs-lookup"><span data-stu-id="266e4-196">For example, if you assign an integer, you can then apply relational and arithmetic operators to the variable.</span></span> <span data-ttu-id="266e4-197">**anytype** 変数は値をタイプに割り当てるとき、日付、列挙 (enum)、整数、実数、文字列、拡張データ型 (EDT) (レコード)、クラス、またはコンテナーを自動的に変換します。</span><span class="sxs-lookup"><span data-stu-id="266e4-197">An **anytype** variable is automatically converted to a date, enumeration (enum), integer, real, string, extended data type (EDT) (record), class, or container when a value is assigned to the type.</span></span> <span data-ttu-id="266e4-198">また、次の明示的な [変換関数](xpp-conversion-run-time-functions.md) を使用できます: **any2date**、**any2enum**、**any2int**、**any2real**、**any2str**。</span><span class="sxs-lookup"><span data-stu-id="266e4-198">Additionally, the following explicit [conversion functions](xpp-conversion-run-time-functions.md) can be used: **any2date**, **any2enum**, **any2int**, **any2real**, and **any2str**.</span></span> <span data-ttu-id="266e4-199">**anytype** に変換した後は、変数を別のデータ型に変更することはできません。</span><span class="sxs-lookup"><span data-stu-id="266e4-199">You can't change the variable to another data type after you've converted it to **anytype**.</span></span>

#### <a name="anytype-examples"></a><span data-ttu-id="266e4-200">anytype 例</span><span class="sxs-lookup"><span data-stu-id="266e4-200">anytype examples</span></span>

    // An example of using anytype variables.
    public static str range(anytype _from, anytype _to)
    {
        return queryValue(_from) + '..' + queryValue(_to);
    }

    // Another example of using anytype variables.
    void put(int position, anytype data)
    {
        record = conPoke (record, position, data);
    }

    public void AnytypeMethod()
    {
        // An example of automatic conversion for anytype.
        anytype a;
        a = "text"; // Automatically assigns a string literal.
    }

### <a name="boolean"></a><span data-ttu-id="266e4-201">ブール値</span><span class="sxs-lookup"><span data-stu-id="266e4-201">boolean</span></span>

<span data-ttu-id="266e4-202">**ブール** データ型には、**true** または **false** のいずれかとして評価される値が含まれます。</span><span class="sxs-lookup"><span data-stu-id="266e4-202">The **boolean** data type contains a value that is evaluated as either **true** or **false**.</span></span> <span data-ttu-id="266e4-203">**ブール** 式が予期される場所では、引当済のリテラル キーワード **true** および **false** を使用することができます。</span><span class="sxs-lookup"><span data-stu-id="266e4-203">You can use the reserved literal keywords **true** and **false** wherever a **boolean** expression is expected.</span></span> <span data-ttu-id="266e4-204">**boolean** のサイズは 1 byte です。</span><span class="sxs-lookup"><span data-stu-id="266e4-204">The size of a **boolean** is 1 byte.</span></span> <span data-ttu-id="266e4-205">既定値は、**false** で、内部表示は、短い番号です。</span><span class="sxs-lookup"><span data-stu-id="266e4-205">The default value is **false**, and the internal representation is a short number.</span></span> <span data-ttu-id="266e4-206">**ブール**は、自動的に **int**、**date**、または **real** に変更されます。</span><span class="sxs-lookup"><span data-stu-id="266e4-206">A **boolean** is automatically converted to an **int**, **date**, or **real**.</span></span> <span data-ttu-id="266e4-207">明示的な変換関数はありません。</span><span class="sxs-lookup"><span data-stu-id="266e4-207">It has no explicit conversion functions.</span></span> <span data-ttu-id="266e4-208">**ブール** の内部テーブル現は整数です。</span><span class="sxs-lookup"><span data-stu-id="266e4-208">The internal representation of a **boolean** is an integer.</span></span> <span data-ttu-id="266e4-209">**ブール値** タイプとして宣言された変数には任意の整数値を割り当てることができます。</span><span class="sxs-lookup"><span data-stu-id="266e4-209">You can assign any integer value to a variable that is declared as the **boolean** type.</span></span> <span data-ttu-id="266e4-210">整数値 **0** (ゼロ) は **false** と評価され、他のすべての整数値は **true** と評価されます。</span><span class="sxs-lookup"><span data-stu-id="266e4-210">The integer value **0** (zero) is evaluated as **false**, and all other integer values are evaluated as **true**.</span></span> <span data-ttu-id="266e4-211">**ブール**の内部表示は整数なので、**ブール**値は自動的に整数と実数に変換されます。</span><span class="sxs-lookup"><span data-stu-id="266e4-211">Because the internal representation of a **boolean** is an integer, **boolean** values are automatically converted to integers and reals.</span></span>

#### <a name="boolean-examples"></a><span data-ttu-id="266e4-212">ブール値の例</span><span class="sxs-lookup"><span data-stu-id="266e4-212">boolean examples</span></span>

    public void BooleanMethod()
    {
        // Simple declaration of a boolean variable, b.
        boolean b;

        // Multiple declarations of booleans.
        boolean b1, b2;

        // Boolean variable is initialized to true.
        boolean b3 = true;

        // Declares a dynamic array of booleans.
        boolean b4[];

        // This example shows the most common usage of a boolean: a boolean in
        // a conditional statement and as a result of a logical expression.
        void main()
        {
            // Declares a boolean called exprValue.
            boolean exprValue;

            // Assigns ExprValue the value of (7*6 == 42), which equates to true.
            exprValue = (7*6 == 42);

            // If the conditional statement is true, print "OK".
            if (exprValue)
            {
                print "OK";  //"OK" is printed because the expression is true.
            }
        }
    }

### <a name="date"></a><span data-ttu-id="266e4-213">日付</span><span class="sxs-lookup"><span data-stu-id="266e4-213">date</span></span>

<span data-ttu-id="266e4-214">**date** データ型は、年、月、日を格納します。</span><span class="sxs-lookup"><span data-stu-id="266e4-214">The **date** data type contains the day, month, and year.</span></span> <span data-ttu-id="266e4-215">日付は、次の構文を使用してリテラルとして記述できます。**日付リテラル = 日 \\ 月 \\ 年**。</span><span class="sxs-lookup"><span data-stu-id="266e4-215">Dates can be written as literals by using the following syntax: **Date literal = day \\ month \\ year**.</span></span> <span data-ttu-id="266e4-216">その年の 4 桁の数字を使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="266e4-216">You must use four digits for the year.</span></span> <span data-ttu-id="266e4-217">**日付**データ型は、1900 年 1 月 1 日～ 2154 年 12 月 31 日の日付を保持できます。</span><span class="sxs-lookup"><span data-stu-id="266e4-217">The **date** data type can hold dates between January 1, 1900, and December 31, 2154.</span></span> <span data-ttu-id="266e4-218">**date** のサイズは 32 ビットです。</span><span class="sxs-lookup"><span data-stu-id="266e4-218">The size of a **date** is 32 bits.</span></span> <span data-ttu-id="266e4-219">既定値は、**null** で、内部表示は、日付です。</span><span class="sxs-lookup"><span data-stu-id="266e4-219">The default value is **null**, and the internal representation is a date.</span></span> <span data-ttu-id="266e4-220">**日付**に暗黙的な変換はありません。</span><span class="sxs-lookup"><span data-stu-id="266e4-220">A **date** has no implicit conversions.</span></span> <span data-ttu-id="266e4-221">ただし、次の明示的な [変換関数](xpp-conversion-run-time-functions.md) が使用できます: **str2date**、**date2str**、**date2num**、および **int2date**。</span><span class="sxs-lookup"><span data-stu-id="266e4-221">However, the following explicit [conversion functions](xpp-conversion-run-time-functions.md) can used: **str2date**, **date2str**, **date2num**, and **int2date**.</span></span> <span data-ttu-id="266e4-222">日付から整数を加算または減算することはできますが、お互いに 2 つの日付を加算または減算することはできません。</span><span class="sxs-lookup"><span data-stu-id="266e4-222">You can add and subtract integers from dates, but you can't add or subtract two dates from each other.</span></span> <span data-ttu-id="266e4-223">試行すると、コンパイラ エラーが発生します。</span><span class="sxs-lookup"><span data-stu-id="266e4-223">If you try, a compiler error occurs.</span></span>

#### <a name="date-examples"></a><span data-ttu-id="266e4-224">date の例</span><span class="sxs-lookup"><span data-stu-id="266e4-224">date examples</span></span>

    public void DateMethod()
    {
        // Simple declaration of a date variable, d.
       date d;

        // Multiple declaration of two date variables.
        date d1, d2;

        // A date variable, d3, is initialized to the 21st of November 1998.
        date d3 = 21\11\1998;

        // Declaration of a dynamic array of dates.
        date d4[];

        // Using arithmetic operators with integer variables and dates.
        void myMethod()
        {
            int anInteger;
            date aDate;
            // Sets the date variable aDate to January 1, 1998.
            aDate = 1\1\1998;
            // Sets the integer variable anInteger to 30.
            anInteger = 30;
            // Uses an integer value in the computation of dates.
            // This sets aDate to aDate + 30; that is the 31st of January 1998.
            aDate = aDate + anInteger;

            // Create 2 variables, set bDate, and then subtract from that date.
            date bDate;
            int dateDifference;
            bDate = 2\10\1998; 
            dateDifference = bDate - aDate;    // dateDifference will equal 9.
        }
    }

### <a name="enum"></a><span data-ttu-id="266e4-225">列挙型</span><span class="sxs-lookup"><span data-stu-id="266e4-225">enum</span></span>

<span data-ttu-id="266e4-226">**列挙**はリテラルのリストです。</span><span class="sxs-lookup"><span data-stu-id="266e4-226">An **enum** is a list of literals.</span></span> <span data-ttu-id="266e4-227">**列挙**を使用する前に、アプリケーション エクスプローラーで宣言する必要があります。</span><span class="sxs-lookup"><span data-stu-id="266e4-227">Before you can use an **enum**, you must declare it in Application Explorer.</span></span> <span data-ttu-id="266e4-228">リテラルの値は、内部的に整数で表されます。</span><span class="sxs-lookup"><span data-stu-id="266e4-228">The literal values are represented internally as integers.</span></span> <span data-ttu-id="266e4-229">最初のリテラルは数字 0、次のリテラルは 1、次のリテラルは 2 というように続きます。</span><span class="sxs-lookup"><span data-stu-id="266e4-229">The first literal has the number 0, the next literal has the number 1, the next literal has the number 2, and so on.</span></span> <span data-ttu-id="266e4-230">式の中では **列挙型** の値を整数として使用することができます。</span><span class="sxs-lookup"><span data-stu-id="266e4-230">You can use **enum** values as integers in expressions.</span></span> <span data-ttu-id="266e4-231">最初のエントリの既定値は、**0** で、内部表示は、短い番号です。</span><span class="sxs-lookup"><span data-stu-id="266e4-231">The default value for the first entry is **0**, and the internal representation is a short number.</span></span> <span data-ttu-id="266e4-232">**列挙**値は自動的に**ブール**、**int**、または **real** に変換されます。</span><span class="sxs-lookup"><span data-stu-id="266e4-232">An **enum** value is automatically converted to a **boolean**, **int**, or **real**.</span></span> <span data-ttu-id="266e4-233">また、次の明示的な [変換関数](xpp-conversion-run-time-functions.md) を使用できます: **enum2str** および **str2enum**。</span><span class="sxs-lookup"><span data-stu-id="266e4-233">Additionally, the following explicit [conversion functions](xpp-conversion-run-time-functions.md) can be used: **enum2str** and **str2enum**.</span></span> <span data-ttu-id="266e4-234">百種類の列挙型が標準アプリケーションに組み込まれています。</span><span class="sxs-lookup"><span data-stu-id="266e4-234">Hundreds of enumerable types are built into the standard application.</span></span> <span data-ttu-id="266e4-235">たとえば、**NoYes** 列挙には関連付けられている 2 つのリテラルがあります: **No** は **0** の値を、および**Yes**は **1** の値です。</span><span class="sxs-lookup"><span data-stu-id="266e4-235">For example, the **NoYes** enum has two associated literals: **No** has the value **0**, and **Yes** has the value **1**.</span></span> <span data-ttu-id="266e4-236">必要なだけ列挙型を作成して、最大で 251 (0 ~ 250) のリテラルを単一列挙型で宣言することができます。</span><span class="sxs-lookup"><span data-stu-id="266e4-236">You can create as many enum types as you want, and you can declare up to 251 (0 to 250) literals in a single enum type.</span></span> <span data-ttu-id="266e4-237">**列挙型**の値を参照するには、列挙型の名前、2 つのコロン、およびリテラルの名前を入力します。</span><span class="sxs-lookup"><span data-stu-id="266e4-237">To reference an **enum** value, enter the name of the enum, two colons, and then the name of the literal.</span></span> <span data-ttu-id="266e4-238">たとえば、**NoYes** 列挙でリテラルの **No** を使用するには、**NoYes::No** を入力します。</span><span class="sxs-lookup"><span data-stu-id="266e4-238">For example, to use the literal **No** in the **NoYes** enum, enter **NoYes::No**.</span></span>

#### <a name="create-an-enum"></a><span data-ttu-id="266e4-239">列挙型を作成する</span><span class="sxs-lookup"><span data-stu-id="266e4-239">Create an enum</span></span>

1.  <span data-ttu-id="266e4-240">ソリューション エクスプローラーで、プロジェクトを右クリックして**追加**をポイントしてから**新しい項目**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="266e4-240">In Solution Explorer, right-click the project, point to **Add**, and then click **New Item**.</span></span>
2.  <span data-ttu-id="266e4-241">**アーティファクト** で、**データ型** を選択します。</span><span class="sxs-lookup"><span data-stu-id="266e4-241">Under **Artifacts**, select **Data Types**.</span></span>
3.  <span data-ttu-id="266e4-242">**基本列挙**をクリックし、を新しい項目の種類を選択します。</span><span class="sxs-lookup"><span data-stu-id="266e4-242">Click **Base Enum** to select the new item type.</span></span>
4.  <span data-ttu-id="266e4-243">**名前**フィールドに、列挙型の名前を入力してから **OK** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="266e4-243">In the **Name** field, enter a name for the enum, and then click **Add**.</span></span> <span data-ttu-id="266e4-244">新しい列挙型がプロジェクトに追加され、新しい要素の列挙型デザイナーが開きます。</span><span class="sxs-lookup"><span data-stu-id="266e4-244">A new enum is added to the project, and the enum designer for the new element is opened.</span></span>
5.  <span data-ttu-id="266e4-245">列挙型デザイナーで、列挙名を右クリックしてから**新しい要素**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="266e4-245">In the enum designer, right-click the enum name, and then click **New Element**.</span></span>
6.  <span data-ttu-id="266e4-246">**プロパティ** ウィンドウで、列挙要素の名前を入力します。</span><span class="sxs-lookup"><span data-stu-id="266e4-246">In the **Properties** window, enter the name of the enum element.</span></span>

#### <a name="enum-examples"></a><span data-ttu-id="266e4-247">列挙型の例</span><span class="sxs-lookup"><span data-stu-id="266e4-247">enum examples</span></span>

    public void EnumMethod()
    {
        // Declare the enum (a NoYes enum) in the Application Explorer.
        NoYes done;

        // An array of Criteria enums.
        Criteria crit[100];
    }

### <a name="guid"></a><span data-ttu-id="266e4-248">guid</span><span class="sxs-lookup"><span data-stu-id="266e4-248">guid</span></span>

<span data-ttu-id="266e4-249">**guid** データ型は、*グローバルに一意の識別子* (GUID) 値を保持します。</span><span class="sxs-lookup"><span data-stu-id="266e4-249">The **guid** data type holds a *globally unique identifier* (GUID) value.</span></span> <span data-ttu-id="266e4-250">GUID は、固有の識別子が必要な場合に、すべてのコンピューターとネットワークで使用できる整数です。</span><span class="sxs-lookup"><span data-stu-id="266e4-250">A GUID is an integer that can be used across all computers and networks, wherever a unique identifier is required.</span></span> <span data-ttu-id="266e4-251">数字が重複することはあまりありません。</span><span class="sxs-lookup"><span data-stu-id="266e4-251">It's unlikely that the number will be duplicated.</span></span> <span data-ttu-id="266e4-252">有効な GUID は、次のすべての仕様を満たします。</span><span class="sxs-lookup"><span data-stu-id="266e4-252">A valid GUID meets all the following specifications:</span></span>

-   <span data-ttu-id="266e4-253">32 桁の 16 進数が必要です。</span><span class="sxs-lookup"><span data-stu-id="266e4-253">It must have 32 hexadecimal digits.</span></span>
-   <span data-ttu-id="266e4-254">次の場所では埋め込まれるダッシュ文字が 4 つ必要です: 8-4-4-4-12。</span><span class="sxs-lookup"><span data-stu-id="266e4-254">It must have four dash characters that are embedded at the following locations: 8-4-4-4-12.</span></span>
-   <span data-ttu-id="266e4-255">文字列の先頭と末尾の中かっこ ({}) はオプションです。</span><span class="sxs-lookup"><span data-stu-id="266e4-255">Braces ({}) at the beginning and end of a string are optional.</span></span> <span data-ttu-id="266e4-256">たとえば、「12345678-BBBb-cCCCC-0000-123456789012」および「{12345678-BBBb-cCCCC-0000-123456789012}」両方共有効な GUID 文字列です。</span><span class="sxs-lookup"><span data-stu-id="266e4-256">For example, both "12345678-BBBb-cCCCC-0000-123456789012" and "{12345678-BBBb-cCCCC-0000-123456789012}" are valid GUID strings.</span></span>
-   <span data-ttu-id="266e4-257">かっこを追加するかどうかに応じて、合計 36 文字または 38 文字にする必要があります。</span><span class="sxs-lookup"><span data-stu-id="266e4-257">It must have a total of either 36 or 38 characters, depending on whether braces are added.</span></span>
-   <span data-ttu-id="266e4-258">a 〜 f (または A 〜 F) の 16 進数は、大文字、小文字、または混在することができます。</span><span class="sxs-lookup"><span data-stu-id="266e4-258">The hexadecimal digits a–f (or A–F) can be uppercase, lowercase, or mixed.</span></span>

<span data-ttu-id="266e4-259">**guid** のサイズは 16 byte または 128 ビットです。</span><span class="sxs-lookup"><span data-stu-id="266e4-259">The size of a **guid** is 16 bytes or 128 bits.</span></span> <span data-ttu-id="266e4-260">次の明示的な [変換関数](xpp-conversion-run-time-functions.md)、**any2guid**、**guid2str**、**newGuid**、**str2guid**、**Global::guidFromString**、および **Global::stringFromGuid** も使用できます。</span><span class="sxs-lookup"><span data-stu-id="266e4-260">The following explicit [conversion functions](xpp-conversion-run-time-functions.md) can be used: **any2guid**, **guid2str**, **newGuid**, **str2guid**, **Global::guidFromString**, and **Global::stringFromGuid**.</span></span>

#### <a name="guid-examples"></a><span data-ttu-id="266e4-261">guid の例</span><span class="sxs-lookup"><span data-stu-id="266e4-261">guid examples</span></span>

<span data-ttu-id="266e4-262">次の例は、**guid** 関数の使い方を示しています。</span><span class="sxs-lookup"><span data-stu-id="266e4-262">The following set of examples shows how to use the **guid** functions.</span></span> <span data-ttu-id="266e4-263">これらの例のコード出力は次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="266e4-263">The code output of these examples follows.</span></span>

    // An example of how to use the GUID functions.
    static void GuidRoundTripJob(Args _args)
    {
        guid guid2;
        str string3;

        // Convert a guid to a string, and back to a guid.
        guid2 = newGuid();
        info(strFmt("Info_a1:  guid2 == %1", guid2));
        string3 = guid2str(guid2);
        info(strFmt("Info_a2:  string3 == %1", string3));
        guid2 = str2guid(string3);
        info(strFmt("Info_a3:  guid2 == %1", guid2));

        // Test string representations of a guid. Mixing upper and lower case letters does not affect the guid.
        guid2 = str2guid("BB345678-abcd-ABCD-0000-bbbbffff9012");
        string3 = guid2str(guid2);
        info(strFmt("Info_b1:  8-4-4-4-12 format for dashes works (%1)", string3));
        info(strFmt("Info_b2:  Mixed upper and lower case works."));

        // Test invalid dash locations, see output is all zeros. Dash locations must be exact.
        guid2 = str2guid("CC2345678abcd-ABCD-0000-cccc9012");
        string3 = guid2str(guid2);
        info(strFmt("Info_c1:  These embedded dash locations are required.  %1", string3));

        // Braces {} are optional.
        guid2 = str2guid("{DD345678-abcd-ABCD-0000-ddddaaaa9012}");
        string3 = guid2str(guid2);
        info(strFmt("Info_d1:  Braces {} are optional (%1)", string3));
    }

#### <a name="guid-code-output"></a><span data-ttu-id="266e4-264">guid コード出力</span><span class="sxs-lookup"><span data-stu-id="266e4-264">guid code output</span></span>

<span data-ttu-id="266e4-265">次の出力は、情報ログに表示されます。</span><span class="sxs-lookup"><span data-stu-id="266e4-265">The following output appears in the Infolog.</span></span> <span data-ttu-id="266e4-266">文字列にはオプションの中かっこが含まれることに注意してください。</span><span class="sxs-lookup"><span data-stu-id="266e4-266">Note that the string includes the optional braces.</span></span>

    Message (02:26:46 pm)
    Info_a1:  guid2 == {93945629-734B-475E-99CE-6AA7AFA43259}
    Info_a2:  string3 == {93945629-734B-475E-99CE-6AA7AFA43259}
    Info_a3:  guid2 == {93945629-734B-475E-99CE-6AA7AFA43259}
    Info_b1:  8-4-4-4-12 format for dashes works ({BB345678-ABCD-ABCD-0000-BBBBFFFF9012})
    Info_b2:  Mixed upper and lower case works.
    Info_c1:  These embedded dash locations are required.  {00000000-0000-0000-0000-000000000000}
    Info_d1:  Braces {} are optional ({DD345678-ABCD-ABCD-0000-DDDDAAAA9012})

### <a name="int-and-int64"></a><span data-ttu-id="266e4-267">int および int64</span><span class="sxs-lookup"><span data-stu-id="266e4-267">int and int64</span></span>

<span data-ttu-id="266e4-268">*整数*は小数点以下の桁数のない数字です。</span><span class="sxs-lookup"><span data-stu-id="266e4-268">*Integers* are numbers that have no decimal places.</span></span> <span data-ttu-id="266e4-269">**int** および **int64** の、2 つの整数タイプがあります。</span><span class="sxs-lookup"><span data-stu-id="266e4-269">There are two integer types: **int** and **int64**.</span></span> <span data-ttu-id="266e4-270">整数は、繰り返しのステートメントの制御変数または配列のインデックスとして使用されます。</span><span class="sxs-lookup"><span data-stu-id="266e4-270">Integers are used as control variables in repetitive statements or as indexes in arrays.</span></span> <span data-ttu-id="266e4-271">また、整数式が必要で、リレーショナル演算子と算術演算子の両方を適用することができる任意の場所で *整数リテラル* を使用することができます。</span><span class="sxs-lookup"><span data-stu-id="266e4-271">You can also use *integer literals* anywhere that an integer expression is expected, and both relational and arithmetic operators can be applied.</span></span> <span data-ttu-id="266e4-272">整数リテラルは **32768** のように、コードに直接入力された整数。</span><span class="sxs-lookup"><span data-stu-id="266e4-272">An integer literal is the integer as it's entered directly in the code, such as **32768**.</span></span> <span data-ttu-id="266e4-273">**Int** は 32 ビット幅で、**int64** は 64 ビット幅です。</span><span class="sxs-lookup"><span data-stu-id="266e4-273">An **int** is 32 bits wide, and an **int64** is 64 bits wide.</span></span> <span data-ttu-id="266e4-274">既定値は、**0** で、内部表示は、長い番号です。</span><span class="sxs-lookup"><span data-stu-id="266e4-274">The default value is **0**, and the internal representation is a long number.</span></span> <span data-ttu-id="266e4-275">整数は自動的に **boolean**、**enum** または **real** に変換されます。</span><span class="sxs-lookup"><span data-stu-id="266e4-275">An integer is automatically converted to a **boolean**, **enum**, or **real**.</span></span> <span data-ttu-id="266e4-276">また、次の明示的な [変換関数](xpp-conversion-run-time-functions.md) を使用できます: **str2int**、**int2str**、**str2int64**、**int642str**。</span><span class="sxs-lookup"><span data-stu-id="266e4-276">Additionally, the following explicit [conversion functions](xpp-conversion-run-time-functions.md) can be used: **str2int**, **int2str**, **str2int64**, and **int642str**.</span></span> <span data-ttu-id="266e4-277">**int** の範囲は \[-2,147,483,647 : 2,147,483,647\]、**int64** の範囲は \[-9,223,372,036,854,775,808 : 9,223,372,036,854,775,808\] です。</span><span class="sxs-lookup"><span data-stu-id="266e4-277">The range of an **int** is \[-2,147,483,647 : 2,147,483,647\], and the range of an **int64** is \[-9,223,372,036,854,775,808 : 9,223,372,036,854,775,808\].</span></span> <span data-ttu-id="266e4-278">全整数はこれらの範囲のいずれかでリテラルとして使用することができます。</span><span class="sxs-lookup"><span data-stu-id="266e4-278">All integers in either of these ranges can be used as literals.</span></span>

#### <a name="int-and-int64-examples"></a><span data-ttu-id="266e4-279">int および int64 の例</span><span class="sxs-lookup"><span data-stu-id="266e4-279">int and int64 examples</span></span>

<span data-ttu-id="266e4-280">次の例は、整数を宣言して式で使用する方法を示しています。</span><span class="sxs-lookup"><span data-stu-id="266e4-280">The following example shows how to declare integers and use them in expressions.</span></span> <span data-ttu-id="266e4-281">**int64** に最大整数プラス 1 を代入しようとすると、数値は 32 ビット数として解釈されるため、間違った結果になります。</span><span class="sxs-lookup"><span data-stu-id="266e4-281">If you try to assign the largest integer plus 1 to an **int64**, you get the wrong result, because the number is interpreted as a 32-bit number.</span></span> <span data-ttu-id="266e4-282">したがって、番号は折り返され、代わりに -2,147,483,647 として格納されます。</span><span class="sxs-lookup"><span data-stu-id="266e4-282">Therefore, the number is wrapped around and stored as -2,147,483,647 instead.</span></span> <span data-ttu-id="266e4-283">この問題を防ぐためには、番号の最後に "u" を追加します。</span><span class="sxs-lookup"><span data-stu-id="266e4-283">To prevent this behavior, add "u" to the end of the number.</span></span> <span data-ttu-id="266e4-284">たとえば、**int64 I = 0x8000 0000u** (0x8000 0000 は 2,147,483,648 です) を入力します。</span><span class="sxs-lookup"><span data-stu-id="266e4-284">For example, enter **int64 i = 0x8000 0000u** (0x8000 0000 is 2,147,483,648).</span></span>

    public void IntegerMethod()
    {
        // Declaration of an integer variable, i.
        int i;

        // Declaration of two int64 variables.
        int64 i1, i2;

        // An integer variable is initialized to the value 100.
        int i3 = 100;

        // Declaration of a dynamic array of integers.
        int i4[];
        void element()
        {
            // Two integer variables are declared and initialized.
            int k = 1, j = 2;

            // j is assigned the result of j + ((i + i) DIV 2).
            j +=(i + i) div 2;

            // This results in: j=3.

            if (j > 2 )
            {
                print "J is greater than 2";
            }
            else
            {
                print "J is NOT greater than 2";
            }
        }
    }

### <a name="real"></a><span data-ttu-id="266e4-285">real</span><span class="sxs-lookup"><span data-stu-id="266e4-285">real</span></span>

<span data-ttu-id="266e4-286">**実数**変数は、整数に加えて小数値を保持できます。</span><span class="sxs-lookup"><span data-stu-id="266e4-286">A **real** variable can hold decimal values in addition to integers.</span></span> <span data-ttu-id="266e4-287">*10 進リテラル* は **実数** が予期される場所ではどこでも使用することができます。</span><span class="sxs-lookup"><span data-stu-id="266e4-287">You can use *decimal literals* anywhere that a **real** is expected.</span></span> <span data-ttu-id="266e4-288">10 進数リテラルは、**2.123876** のように、コードで直接入力された 10 進数です。</span><span class="sxs-lookup"><span data-stu-id="266e4-288">A decimal literal is the decimal as it's entered directly in the code, such as **2.123876**.</span></span> <span data-ttu-id="266e4-289">実数リテラルは、**1.0e3** などの指数の表記を使用して記述することもできます。</span><span class="sxs-lookup"><span data-stu-id="266e4-289">Real literals can also be written by using exponential notation, such as **1.0e3**.</span></span> <span data-ttu-id="266e4-290">Reals は、すべての式で使用することができ、リレーショナル演算子と算術演算子の両方と共に使用できます。</span><span class="sxs-lookup"><span data-stu-id="266e4-290">Reals can be used in all expressions, and they can be used with both relational and arithmetic operators.</span></span> <span data-ttu-id="266e4-291">**実数**は、16桁の有効な数値の精度があります。</span><span class="sxs-lookup"><span data-stu-id="266e4-291">A **real** has a precision of 16 significant digits.</span></span> <span data-ttu-id="266e4-292">**real** の既定値は **0.0** で、内部表示はバイナリコード化されたデジタル (BCD) 番号です。</span><span class="sxs-lookup"><span data-stu-id="266e4-292">The default value for a **real** is **0.0**, and the internal representation is a binary-coded digital (BCD) number.</span></span> <span data-ttu-id="266e4-293">BCD エンコードにより、0.1 の倍数の値の正確な表現が可能になります。</span><span class="sxs-lookup"><span data-stu-id="266e4-293">The BCD encoding enables exact representations of values that are multiples of 0.1.</span></span> <span data-ttu-id="266e4-294">**実数** 変数の範囲は、-(10)¹²⁷ から (10)¹²⁷ です。</span><span class="sxs-lookup"><span data-stu-id="266e4-294">The range of a **real** variable is -(10)¹²⁷ through (10)¹²⁷.</span></span> <span data-ttu-id="266e4-295">この範囲内のすべての実数は X++ でリテラルとして使用できます。</span><span class="sxs-lookup"><span data-stu-id="266e4-295">All reals in this range can be used as literals in X++.</span></span> <span data-ttu-id="266e4-296">**実数**変数は、自動的に**ブール**、**enum**、または **int** に変換されます。結果が整数の場合、または演算子が整数演算子の場合には、**実数**は整数に変換されます。</span><span class="sxs-lookup"><span data-stu-id="266e4-296">A **real** variable is automatically converted to a **boolean**, **enum**, or **int**. If the result is an integer, or if the operator is an integer operator, the **real** is converted to an integer.</span></span> <span data-ttu-id="266e4-297">結果が**ブール値**である場合、**実数**が**ブール値**に変換されたりします。</span><span class="sxs-lookup"><span data-stu-id="266e4-297">If the result is a **boolean**, the **real** is converted to a **boolean**, and so on.</span></span> <span data-ttu-id="266e4-298">また、次の明示的な [変換関数](xpp-conversion-run-time-functions.md) を使用できます: **str2num**、**num2str**。</span><span class="sxs-lookup"><span data-stu-id="266e4-298">Additionally, the following explicit [conversion functions](xpp-conversion-run-time-functions.md) can be used: **str2num** and **num2str**.</span></span> <span data-ttu-id="266e4-299">X++ **実数** と Microsoft .NET Framework **System.Decimal** 間の直接割り当てによって、値が正しく変換されます。</span><span class="sxs-lookup"><span data-stu-id="266e4-299">Direct assignments between X++ **real** and Microsoft .NET Framework **System.Decimal** convert the value correctly.</span></span> <span data-ttu-id="266e4-300">換算関数を呼び出す必要はありません。</span><span class="sxs-lookup"><span data-stu-id="266e4-300">A call to a conversion function isn't required.</span></span> <span data-ttu-id="266e4-301">*10 進数*は、符号、0 から 9 の範囲内の数値、および数値の整数と小数点以下を区切る浮動小数点の位置を表すスケーリング係数で構成される浮動小数点値です。</span><span class="sxs-lookup"><span data-stu-id="266e4-301">A *decimal number* is a floating-point value that consists of a sign, a numeric value where each digit is in the range 0 through 9, and a scaling factor that indicates the position of a floating decimal point that separates the integral and fractional parts of the numeric value.</span></span> <span data-ttu-id="266e4-302">**実数**値のバイナリ表現は、1 ビットの符号、96ビットの整数、スケーリング係数で構成されます。</span><span class="sxs-lookup"><span data-stu-id="266e4-302">The binary representation of a **real** value consists of a 1-bit sign, a 96-bit integer number, and a scaling factor.</span></span> <span data-ttu-id="266e4-303">拡大縮小係数は、96 ビット整数を分割し、小数部の部分を指定するのに使用されます。</span><span class="sxs-lookup"><span data-stu-id="266e4-303">The scaling factor is used to divide the 96-bit integer and specify what part of it is a decimal fraction.</span></span> <span data-ttu-id="266e4-304">拡大縮小係数は、0 から 28 の範囲の指数に暗黙的に 10 を引いたものです。</span><span class="sxs-lookup"><span data-stu-id="266e4-304">The scaling factor is implicitly the number 10 raised to an exponent in the range 0 through 28.</span></span> <span data-ttu-id="266e4-305">したがって、10 進数のバイナリ表現は (\[-2⁹⁶ ～ 2⁹⁶\] ÷ 10(0\\ ～\\ 28)) を表します。ここで -(2⁹⁶-1) は表現できる最小値と等しく、2⁹⁶-1 は最大値になります。</span><span class="sxs-lookup"><span data-stu-id="266e4-305">Therefore, the binary representation of a decimal value represents (\[-2⁹⁶ through 2⁹⁶\] ÷ 10(0\\ through\\ 28)), where -(2⁹⁶-1) is the minimum value that can be expressed and 2⁹⁶-1 is the maximum value.</span></span> <span data-ttu-id="266e4-306">**注記:** Microsoft Dynamics 365 for Finance and Operations で**実数**値を表すために使用されるタイプは、変換された Microsoft Dynamics AX 2012 の X++ から変更されています。</span><span class="sxs-lookup"><span data-stu-id="266e4-306">**Note:** The type that is used to represent **real** values in Microsoft Dynamics 365 for Finance and Operations has changed from the interpreted X++ of Microsoft Dynamics AX 2012.</span></span> <span data-ttu-id="266e4-307">ただし、新しいタイプは、古いタイプが表すことができるすべての値を表すことができるので、コードを書き直す必要はありません。</span><span class="sxs-lookup"><span data-stu-id="266e4-307">However, you don't have to rewrite any code, because the new type can express all the values that the old type could express.</span></span> <span data-ttu-id="266e4-308">完全な開示のためにこの材料を提供します。</span><span class="sxs-lookup"><span data-stu-id="266e4-308">We provide this material in the interest of full disclosure only.</span></span> <span data-ttu-id="266e4-309">**実数**タイプのすべてのインスタンスが .NET 小数タイプ (**System.Decimal**) のインスタンスとして実装されます。</span><span class="sxs-lookup"><span data-stu-id="266e4-309">All instances of the **real** type are now implemented as instances of the .NET decimal type (**System.Decimal**).</span></span> <span data-ttu-id="266e4-310">以前のバージョンでの **real** 型と同様に、バイナリ コード化された小数点以下の型での decimal 型は丸め誤差に対する対応力があります。</span><span class="sxs-lookup"><span data-stu-id="266e4-310">Just as the **real** type in previous versions, the decimal type in a binary-coded decimal type is resilient to rounding errors.</span></span> <span data-ttu-id="266e4-311">以前のバージョンと異なる 10 進型の範囲と解像度。</span><span class="sxs-lookup"><span data-stu-id="266e4-311">The range and resolution of the decimal type differ from previous versions.</span></span> <span data-ttu-id="266e4-312">元の X++ **実数** 型は 16 桁と小数点の位置を定義した指数をサポートしていました。</span><span class="sxs-lookup"><span data-stu-id="266e4-312">The original X++ **real** type supported 16 digits and an exponent that defined the position of the decimal point.</span></span> <span data-ttu-id="266e4-313">ただし、Microsoft Dynamics 365 for Finance and Operations 以降の X++ **実数**タイプは 79,228,162,514,264,337,593,543,950,335 (2⁹⁶-1) から -79,228,162,514,264,337,593,543,950,335 (-\[2⁹⁶-1\]) の範囲の 10 進数を表します。</span><span class="sxs-lookup"><span data-stu-id="266e4-313">However, the X++ **real** type for Microsoft Dynamics 365 for Finance and Operations and later can represent decimal numbers in the range 79,228,162,514,264,337,593,543,950,335 (2⁹⁶-1) through -79,228,162,514,264,337,593,543,950,335 (-\[2⁹⁶-1\]).</span></span> <span data-ttu-id="266e4-314">新しい**実数**タイプにはさらに丸めが必要です。</span><span class="sxs-lookup"><span data-stu-id="266e4-314">Rounding is still required for the new **real** type.</span></span> <span data-ttu-id="266e4-315">たとえば、次のコードは、1 ではなく 0.9999999999999999999999999999 という結果を生成します。</span><span class="sxs-lookup"><span data-stu-id="266e4-315">For example, the following code produces a result of 0.9999999999999999999999999999 instead of 1.</span></span> <span data-ttu-id="266e4-316">1/3 の値を正確に表せる小数点以下の桁数はありません。</span><span class="sxs-lookup"><span data-stu-id="266e4-316">No number of decimals will suffice to represent the value of 1/3 accurately.</span></span> <span data-ttu-id="266e4-317">ここで得られる不一致は、有限数の小数しか提供されないことによるものです。</span><span class="sxs-lookup"><span data-stu-id="266e4-317">The discrepancy obtained here is due to the fact that only a finite number of decimals are provided.</span></span> <span data-ttu-id="266e4-318">必要な小数点以下の桁数まで丸めるには、**round** 関数を使用します。</span><span class="sxs-lookup"><span data-stu-id="266e4-318">You should use the **round** function to round to the number of decimals required.</span></span>

    // An example of using the debugger to show the value of the variables.
    public static void UseTheDebugger(Args a)
    {
        real dividend = 1.0;
        real divisor = 3.0;
        str stringvalue;
        System.Decimal valueAsDecimal;
        real value = dividend/divisor * divisor; 
        valueAsDecimal = value;
        info(valueAsDecimal.ToString("G28"));
        // An example of using the Round function to round to the number of decimals required.
        value  = round(value, 2);
    }

#### <a name="real-examples"></a><span data-ttu-id="266e4-319">real の例</span><span class="sxs-lookup"><span data-stu-id="266e4-319">real examples</span></span>

    public void RealMethod()
    {
        // Simple declaration of a real variable, r.
        real r;

        // Multiple declaration of two real variables.
        real r1, r2;

        // A real variable is initialized to the approximate value of pi.
        real r3 = 3.1415;

        // Declaration of a dynamic array of reals.
        real r4[];

        // An example of a real literal written using exponential notation.
        real r;
        r = 1.000e3;
        r = 1.2345e+3;
        r = 1.2345e+03;
        r = 1234.5e4;
        r = 1.0e1; // Means 1.0E1 
    }

    // An example of automatic conversions.
    void main()
    {
        // Declares a variable of type integer with the name exprValue.
        int exprValue;

        // Declares a real variable with the name area.
        real area = 3.141528;
        exprValue = Area/3;

        // The expression Area/3 is a real expression because
        // division is a real operator, and the result is 1.047176. This result is
        // automatically converted (actually truncated) to an integer with the value 1,
        // because exprValue is an integer.
    }

    // An example of a real being converted to .NET System.Decimal.
    void AnotherMain(Args _args)
    {
        real real9;
        System.Decimal sysdec1;

        // Direct assignments supported between these types.
        sysdec1 = 2.3456;
        real9 = sysdec1;
        info(strFmt("strFmt says real9 == %1", real9));
    }

    /***
    Message (05:48:43 pm)
    strFmt says real9 == 2.35
    ***/

    // An example of using reals in expressions.
    void myMethod()
    {
        // Two real variables are declared and initialized.
        real i = 2.5, j = 2.5;

        // j is assigned the result of j * i, so j=6.25.
        j = j * i;
        if (j > (i * 2)) // If j > 5 
        {
            print "Great"; // "Great" is printed.
        }
        else
        {
           print "Oops"; // else "Oops" is printed.
        }
    }

### <a name="str"></a><span data-ttu-id="266e4-320">str</span><span class="sxs-lookup"><span data-stu-id="266e4-320">str</span></span>

<span data-ttu-id="266e4-321">**str** 変数 (*文字列*) は、テキスト、ヘルプ行、住所、電話番号などとして使用される文字の並びです。</span><span class="sxs-lookup"><span data-stu-id="266e4-321">A **str** variable (a *string*) is a sequence of characters that are used as texts, help lines, addresses, telephone numbers, and so on.</span></span> <span data-ttu-id="266e4-322">文字列を宣言するには、**str** キーワードを使用します。</span><span class="sxs-lookup"><span data-stu-id="266e4-322">To declare a string, use the **str** keyword.</span></span> <span data-ttu-id="266e4-323">*文字列リテラル*引用符 ("") で囲まれた文字です。</span><span class="sxs-lookup"><span data-stu-id="266e4-323">*String literals* are characters that are enclosed in quotation marks ("").</span></span> <span data-ttu-id="266e4-324">文字列式が必要な場合はいつでも、文字列リテラルを使用することができます。</span><span class="sxs-lookup"><span data-stu-id="266e4-324">String literals can be used wherever string expressions are expected.</span></span> <span data-ttu-id="266e4-325">文字列リテラルの例には、「StringLit」および「Hello World」が含まれます。</span><span class="sxs-lookup"><span data-stu-id="266e4-325">Examples of string literals include "StringLit" and "Hello World".</span></span> <span data-ttu-id="266e4-326">文字列を複数の行にまたがるようにするには、その前にアットマーク (@) を付けます。</span><span class="sxs-lookup"><span data-stu-id="266e4-326">If you want the string to span more than one line, precede it with an at sign (@).</span></span> <span data-ttu-id="266e4-327">比較などの論理式では文字列を使用することができます。</span><span class="sxs-lookup"><span data-stu-id="266e4-327">You can use strings in logical expressions, such as comparisons.</span></span> <span data-ttu-id="266e4-328">また、+ 演算子を使用することで文字列を連結することができます。</span><span class="sxs-lookup"><span data-stu-id="266e4-328">You can also concatenate strings by using the + operator.</span></span> <span data-ttu-id="266e4-329">文字列の既定値は **空**で、内部表示は文字のリストです。</span><span class="sxs-lookup"><span data-stu-id="266e4-329">The default value for a string is **empty**, and the internal representation is a list of characters.</span></span> <span data-ttu-id="266e4-330">文字列の自動変換はありません。</span><span class="sxs-lookup"><span data-stu-id="266e4-330">There are no automatic conversions for strings.</span></span> <span data-ttu-id="266e4-331">ただし、次の明示的な [変換関数](xpp-conversion-run-time-functions.md) が使用できます: **str2int**、**str2int64**、**int2str**、**str2num**、**num2str**、**str2date**、および **date2str**。</span><span class="sxs-lookup"><span data-stu-id="266e4-331">However, the following explicit [conversion functions](xpp-conversion-run-time-functions.md) can be used: **str2int**, **str2int64**, **int2str**, **str2num**, **num2str**, **str2date**, and **date2str**.</span></span> <span data-ttu-id="266e4-332">文字列は、無制限の文字数を保持できます。</span><span class="sxs-lookup"><span data-stu-id="266e4-332">A string can hold an unlimited number of characters.</span></span> <span data-ttu-id="266e4-333">ただし、変数の宣言で文字列の最大の長さを指定できます。</span><span class="sxs-lookup"><span data-stu-id="266e4-333">However, you can specify the maximum length of a string in the variable declaration.</span></span> <span data-ttu-id="266e4-334">文字列はその最大長に切り捨てられます。</span><span class="sxs-lookup"><span data-stu-id="266e4-334">The string is then truncated to that maximum length.</span></span> <span data-ttu-id="266e4-335">例として次のセクションに表示します。</span><span class="sxs-lookup"><span data-stu-id="266e4-335">An example is shown in the next section.</span></span>

#### <a name="str-examples"></a><span data-ttu-id="266e4-336">str の例</span><span class="sxs-lookup"><span data-stu-id="266e4-336">str examples</span></span>

    void StringMethod()
    {
        // Declare a dynamic string of unlimited length.
        str unlimitedString;

        // Declare a string with a maximum of 64 characters
        // in order to force a truncation, initialized to "A".
        str 64 maxLengthString = "A";

        // Declare an array of 100 strings.
       str 30 hundredStrings[100];

        // Using strings in expressions.
        void myMethod()
        {
            // Two strings are declared and initialized.
            str a="Hello", b="World";

            // The concatenation of a, " " and b is printed in a window.
            print a+" "+b;
        }
    }

### <a name="timeofday"></a><span data-ttu-id="266e4-337">timeOfDay</span><span class="sxs-lookup"><span data-stu-id="266e4-337">timeOfDay</span></span>

<span data-ttu-id="266e4-338">**timeOfDay** (時間) データ型は、午前 0 時から経過した秒数を表す整数値です。</span><span class="sxs-lookup"><span data-stu-id="266e4-338">The **timeOfDay** (time) data type is an integer value that represents the number of seconds that have passed since midnight.</span></span> <span data-ttu-id="266e4-339">整数と同様に、**timeOfDay** 変数はリテラルとして使用することができます。</span><span class="sxs-lookup"><span data-stu-id="266e4-339">Like integers, **timeOfDay** variables can be used as literals.</span></span> <span data-ttu-id="266e4-340">リレーショナルおよび算術演算子は、**timeOfDay** 変数に適用できます。</span><span class="sxs-lookup"><span data-stu-id="266e4-340">Relational and arithmetic operators can be applied to **timeOfDay** variables.</span></span> <span data-ttu-id="266e4-341">**timeOfDay** 変数も式で使用できます。</span><span class="sxs-lookup"><span data-stu-id="266e4-341">A **timeOfDay** variable can also be used in expressions.</span></span> <span data-ttu-id="266e4-342">**timeOfDay** データ型の範囲は \[0;86,400\] のクローズ区間にあります。</span><span class="sxs-lookup"><span data-stu-id="266e4-342">The range of a **timeOfDay** data type is in the closed interval \[0; 86,400\].</span></span> <span data-ttu-id="266e4-343">86,400 (23: 59:59) を超える値は解釈できません。</span><span class="sxs-lookup"><span data-stu-id="266e4-343">Values above 86,400 (23:59:59) can't be interpreted.</span></span> <span data-ttu-id="266e4-344">**timeOfDay** 変数は、自動的に**ブール**、**enum**、または**実数**に変換されます。</span><span class="sxs-lookup"><span data-stu-id="266e4-344">A **timeOfDay** variable is automatically converted to a **boolean**, **enum**, or **real**.</span></span> <span data-ttu-id="266e4-345">また、次の明示的な [変換関数](xpp-conversion-run-time-functions.md) を使用できます: **str2time**、**time2str**。</span><span class="sxs-lookup"><span data-stu-id="266e4-345">Additionally, the following explicit [conversion functions](xpp-conversion-run-time-functions.md) can be used: **str2time** and **time2str**.</span></span>

#### <a name="timeofday-examples"></a><span data-ttu-id="266e4-346">timeOfDay の例</span><span class="sxs-lookup"><span data-stu-id="266e4-346">timeOfDay examples</span></span>

    public void TimeofdayMethod()
    {
        // Declaration of a timeOfDay variable, time1.
        timeOfDay time1;

        // Declaration and initialization of a timeOfDay variable to 00:21:35.
        timeOfDay time2 = 1295;
    }

### <a name="utcdatetime"></a><span data-ttu-id="266e4-347">utcdatetime</span><span class="sxs-lookup"><span data-stu-id="266e4-347">utcdatetime</span></span>

<span data-ttu-id="266e4-348">**utcdatetime** データ型は、**date** 型と **timeOfDay** 型を結合します。</span><span class="sxs-lookup"><span data-stu-id="266e4-348">The **utcdatetime** data type combines the **date** type and the **timeOfDay** type.</span></span> <span data-ttu-id="266e4-349">**utcdatetime** 変数には、タイム ゾーンに関する情報も含まれています。</span><span class="sxs-lookup"><span data-stu-id="266e4-349">A **utcdatetime** variable also holds information about the time zone.</span></span> <span data-ttu-id="266e4-350">ただし、この情報はコードではアクセスできません。</span><span class="sxs-lookup"><span data-stu-id="266e4-350">However, this information can't be accessed in code.</span></span> <span data-ttu-id="266e4-351">**utcdatetime** リテラルの形式は、**yyyy-mm-ddThh:mm:ss** です。</span><span class="sxs-lookup"><span data-stu-id="266e4-351">The format for a **utcdatetime** literal is **yyyy-mm-ddThh:mm:ss**.</span></span> <span data-ttu-id="266e4-352">大文字「T」が必要です。</span><span class="sxs-lookup"><span data-stu-id="266e4-352">The uppercase "T" is required.</span></span> <span data-ttu-id="266e4-353">この形式は引用符を使用せずに記述できます。</span><span class="sxs-lookup"><span data-stu-id="266e4-353">This format can be written without quotation marks.</span></span> <span data-ttu-id="266e4-354">最小値は、**1900-01-01T00:00:00** で、最大値は **1900-01-01T00:00:00** です。</span><span class="sxs-lookup"><span data-stu-id="266e4-354">The minimum value is **1900-01-01T00:00:00**, and the maximum value is **1900-01-01T00:00:00**.</span></span> <span data-ttu-id="266e4-355">この最大値は、**date** と **timeOfDay** の上位範囲に一致します。</span><span class="sxs-lookup"><span data-stu-id="266e4-355">This maximum value matches the upper range of **date** and **timeOfDay**.</span></span> <span data-ttu-id="266e4-356">**utcdatetime** の最小単位は 1 秒です。</span><span class="sxs-lookup"><span data-stu-id="266e4-356">The smallest unit of time in **utcdatetime** is one second.</span></span> <span data-ttu-id="266e4-357">宣言されているもののまた初期化されていない **utcdatetime** 変数の規定値は、 **1900-01-01T00:00:00** です。</span><span class="sxs-lookup"><span data-stu-id="266e4-357">A **utcdatetime** variable that has been declared but hasn't been initialized has the default value **1900-01-01T00:00:00**.</span></span> <span data-ttu-id="266e4-358">この値は、**DateTimeUtil::minValue()** によって返される値です。</span><span class="sxs-lookup"><span data-stu-id="266e4-358">This value is the value that is returned by **DateTimeUtil::minValue()**.</span></span> <span data-ttu-id="266e4-359">一部の機能は、この最小値の入力パラメーターを **null** として扱います。</span><span class="sxs-lookup"><span data-stu-id="266e4-359">Some functions treat an input parameter of this minimum value as **null**.</span></span> <span data-ttu-id="266e4-360">たとえば、**DateTimeUtil::toStr** メソッドは、空の文字列を返します。</span><span class="sxs-lookup"><span data-stu-id="266e4-360">For example, the **DateTimeUtil::toStr** method returns an empty string.</span></span> <span data-ttu-id="266e4-361">ただし、**DateTimeUtil::addSeconds** メソッドは使用可能な **utcdatetime** 値を返します。</span><span class="sxs-lookup"><span data-stu-id="266e4-361">However, the **DateTimeUtil::addSeconds** method returns a usable **utcdatetime** value.</span></span> <span data-ttu-id="266e4-362">**utcdatetime** データ型の暗黙的な変換はありません。</span><span class="sxs-lookup"><span data-stu-id="266e4-362">There are no implicit conversions for the **utcdatetime** data type.</span></span> <span data-ttu-id="266e4-363">**DateTimeUtil** クラスは、**utcdatetime** 値を操作するために使用できるさまざまなメソッドを提供します。</span><span class="sxs-lookup"><span data-stu-id="266e4-363">The **DateTimeUtil** class provides many methods that you can use to manipulate **utcdatetime** values.</span></span> <span data-ttu-id="266e4-364">次の明示的な [変換関数](xpp-conversion-run-time-functions.md)、**str2datetime** および **datetime2str** も使用できます。</span><span class="sxs-lookup"><span data-stu-id="266e4-364">The following explicit [conversion functions](xpp-conversion-run-time-functions.md) can also be used: **str2datetime** and **datetime2str**.</span></span> <span data-ttu-id="266e4-365">また、**グローバル** クラスは、**utcDateTime2SystemDateTime** と **CLRSystemDateTime2UtcDateTime** 変換メソッドを提供して、共通言語ランタイム (CLR) 相互運用をサポートします。</span><span class="sxs-lookup"><span data-stu-id="266e4-365">Additionally, the **Global** class provides the **utcDateTime2SystemDateTime** and **CLRSystemDateTime2UtcDateTime** conversion methods to support common language runtime (CLR) interop.</span></span> <span data-ttu-id="266e4-366">比較演算子は、**utcdatetime** データ型で使用できる唯一の演算子です。</span><span class="sxs-lookup"><span data-stu-id="266e4-366">Comparison operators are the only type of operators that can be used with the **utcdatetime** data type.</span></span> <span data-ttu-id="266e4-367">次の演算子を使用して、2つの **utcdatetime** 値を比較することができます: !=、&lt;、&lt;=、==、&gt;、および &gt;=。</span><span class="sxs-lookup"><span data-stu-id="266e4-367">The following operators can be used to compare two **utcdatetime** values: !=, &lt;, &lt;=, ==, &gt;, and &gt;=.</span></span> <span data-ttu-id="266e4-368">テーブルに **utcdatetime** フィールドを追加するときは、そのフィールドを EDT にもとづいて決めることをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="266e4-368">When you add a **utcdatetime** field to a table, we recommend that you base the field on an EDT.</span></span>

#### <a name="utcdatetime-examples"></a><span data-ttu-id="266e4-369">utcdatetime の例</span><span class="sxs-lookup"><span data-stu-id="266e4-369">utcdatetime examples</span></span>

    public void UtcdatetimeMethod()
    {
        // Declaring a utcdatetime literal.
        utcdatetime myUtc2 = 1988-07-20T13:34:45;

        // Another example of declaring a utcdatetime literal.
        int iDay = DateTimeUtil::day(1988-07-20T13:34:45);

        // utcdatetime using a quoted string parameter into the DateTimeUtil::parse method.
        utcdatetime myUtc4 = DateTimeUtil::parse("1988-07-20T13:34:45");
    }

## <a name="composite-data-types"></a><span data-ttu-id="266e4-370">複合データ型</span><span class="sxs-lookup"><span data-stu-id="266e4-370">Composite data types</span></span>
<span data-ttu-id="266e4-371">X++ の複合データ型は、配列、コンテナー、データ型としてのクラス、データ型としてのデリゲート、データ型としてのテーブルです。</span><span class="sxs-lookup"><span data-stu-id="266e4-371">The composite data types in X++ are arrays, containers, classes as data types, delegates as data types, and tables as data types.</span></span>

### <a name="array"></a><span data-ttu-id="266e4-372">配列</span><span class="sxs-lookup"><span data-stu-id="266e4-372">Array</span></span>

<span data-ttu-id="266e4-373">*配列*は同じデータ型を持つ項目のリストを含む変数です。</span><span class="sxs-lookup"><span data-stu-id="266e4-373">An *array* is a variable that contains a list of items that have the same data type.</span></span> <span data-ttu-id="266e4-374">配列の要素は、整数インデックスを使用してアクセスされます。</span><span class="sxs-lookup"><span data-stu-id="266e4-374">The elements of an array are accessed by using integer indexes.</span></span> <span data-ttu-id="266e4-375">配列内の各要素を初期化するには、別のステートメントを使用します。</span><span class="sxs-lookup"><span data-stu-id="266e4-375">You use a separate statement to initialize each element in an array.</span></span> <span data-ttu-id="266e4-376">コンテナー データ型または配列オブジェクトを使用してコレクションを作成するとき、1 つのステートメントを使用して複数の要素を初期化できます。</span><span class="sxs-lookup"><span data-stu-id="266e4-376">When you use a container data type or an array object to create a collection, you can initialize multiple elements by using a single statement.</span></span> <span data-ttu-id="266e4-377">既定では、配列内のすべての項目は配列のデータ型の既定値を持ちます。</span><span class="sxs-lookup"><span data-stu-id="266e4-377">By default, all the items in an array have the default value of the data type in the array.</span></span> <span data-ttu-id="266e4-378">*動的配列*、*固定長配列*、*ディスク配列の一部*の 3 種類の配列があります。</span><span class="sxs-lookup"><span data-stu-id="266e4-378">There are three kinds of arrays: *dynamic arrays*, *fixed-length arrays*, and *partly on disk arrays*.</span></span>

-   <span data-ttu-id="266e4-379">**動的配列** - これらの配列は、空の配列オプションを使用して宣言されます。</span><span class="sxs-lookup"><span data-stu-id="266e4-379">**Dynamic arrays** – These arrays are declared by using an empty array option.</span></span> <span data-ttu-id="266e4-380">つまり、かっこ (\[\]) だけがあります。</span><span class="sxs-lookup"><span data-stu-id="266e4-380">In other word, they have only brackets (\[\]).</span></span>
-   <span data-ttu-id="266e4-381">**固定長の配列** – これらの配列は、宣言で指定されている品目の数を保持できます。</span><span class="sxs-lookup"><span data-stu-id="266e4-381">**Fixed-length arrays** – These arrays can hold the number of items that is specified in the declaration.</span></span> <span data-ttu-id="266e4-382">固定長の配列は動的配列と宣言されますが、かっこ内に長さのオプションが含まれます。</span><span class="sxs-lookup"><span data-stu-id="266e4-382">Fixed-length arrays are declared like dynamic arrays, but a length option is included in the brackets.</span></span>
-   <span data-ttu-id="266e4-383">**ディスク配列の一部** – これらの配列は、動的配列または固定長の配列として宣言され、メモリに保持する品目の数を宣言するオプションが追加されています。</span><span class="sxs-lookup"><span data-stu-id="266e4-383">**Partly on disk arrays** – These arrays are declared as either dynamic arrays or fixed-length arrays that have an extra option that declares how many items should be held in memory.</span></span> <span data-ttu-id="266e4-384">他の項目はディスクに保存され、参照されると自動的に読み込まれます。</span><span class="sxs-lookup"><span data-stu-id="266e4-384">The other items are stored on disk and are automatically loaded when they are referenced.</span></span>

<span data-ttu-id="266e4-385">X++ は1次元配列のみをサポートしています。</span><span class="sxs-lookup"><span data-stu-id="266e4-385">X++ supports only one-dimensional arrays.</span></span> <span data-ttu-id="266e4-386">ただし、複数の配列インデックスの動作を再現することができます。</span><span class="sxs-lookup"><span data-stu-id="266e4-386">However, you can mimic the behavior of multiple array indexes.</span></span> <span data-ttu-id="266e4-387">(詳細については、「複数の配列インデックス」セクションを参照してください)。</span><span class="sxs-lookup"><span data-stu-id="266e4-387">(For more information, see the "Multiple array indexes" section).</span></span> <span data-ttu-id="266e4-388">オブジェクトとテーブル内の変数は配列として宣言することができます。</span><span class="sxs-lookup"><span data-stu-id="266e4-388">Variables in objects and tables can be declared as arrays.</span></span> <span data-ttu-id="266e4-389">たとえば、この機能は、標準アプリケーションの住所明細行で使用されます。</span><span class="sxs-lookup"><span data-stu-id="266e4-389">For example, this functionality is used in address lines in the standard application.</span></span> <span data-ttu-id="266e4-390">配列コレクション クラスを配列内のオブジェクトに格納できます。</span><span class="sxs-lookup"><span data-stu-id="266e4-390">An array collection class lets you store objects in an array.</span></span> <span data-ttu-id="266e4-391">配列インデックスは 1 から開始されます。</span><span class="sxs-lookup"><span data-stu-id="266e4-391">Array indexes begin at 1.</span></span> <span data-ttu-id="266e4-392">配列の最初の項目は \[1\] で参照され、2番目の項目は、 \[2\] などで参照されます。</span><span class="sxs-lookup"><span data-stu-id="266e4-392">The first item in the array is referenced as \[1\], the second item is referenced as \[2\], and so on.</span></span> <span data-ttu-id="266e4-393">次の構文は、配列要素にアクセスするために使用されます: **ArrayItemReference = ArrayVariable \[ Index \]**。</span><span class="sxs-lookup"><span data-stu-id="266e4-393">The following syntax is used to access an array element: **ArrayItemReference = ArrayVariable \[ Index \]**.</span></span> <span data-ttu-id="266e4-394">この構文では、**ArrayVariable** は配列の識別子であり、**Index** は配列要素の数です。</span><span class="sxs-lookup"><span data-stu-id="266e4-394">In this syntax, **ArrayVariable** is the identifier of the array, and **Index** is the number of the array element.</span></span> <span data-ttu-id="266e4-395">**インデックス**には整数式を指定できます。</span><span class="sxs-lookup"><span data-stu-id="266e4-395">**Index** can be an integer expression.</span></span> <span data-ttu-id="266e4-396">項目ゼロ \[0\] は配列をクリアするために使用します。</span><span class="sxs-lookup"><span data-stu-id="266e4-396">Item zero \[0\] is used to clear the array.</span></span> <span data-ttu-id="266e4-397">値が配列のインデックス 0 に割り当てられている場合は、配列内のすべての要素が既定値にリセットされます。</span><span class="sxs-lookup"><span data-stu-id="266e4-397">If a value is assigned to index 0 in an array, all elements in the array are reset to their default value.</span></span>

#### <a name="array-examples"></a><span data-ttu-id="266e4-398">配列の例</span><span class="sxs-lookup"><span data-stu-id="266e4-398">Array examples</span></span>

    public void ArrayMethod()
    {
        int myArray[10]; // Fixed-length array with 10 integers.
        myArray[4] = 1; // Accessing the 4th element in the array.
        myArray[0] = 0; // Resets all elements in intArray. 

        // Dynamic array of integers.
        int intArray[];

        // Dynamic array of variables of type Datatype.
        //Datatype arrayVariable[];

        // Fixed-length arrays.
        boolean boolArray[100]; // Fixed-length array of booleans with 100 items.

        // Two examples of Partly On Disk Arrays.
        // Dynamic integer array with only 100 elements in memory.
        int arrayVariable [ ,100];
        // Fixed-length string array with 1000 elements, and only 200 in memory.
        str arrayVariable2 [1000,200];

            // A dynamic array of integers.
            int i[];
            // A fixed-length real array with 100 elements.
            real r[100];
            // A dynamic array of dates with only 10 elements in memory.
            date d[,10];
            // A fixed length array of NoYes variables with 100 elements and 10 in memory.
            NoYes ny[100,10];
    }

#### <a name="multiple-array-indexes"></a><span data-ttu-id="266e4-399">複数の配列インデックス</span><span class="sxs-lookup"><span data-stu-id="266e4-399">Multiple array indexes</span></span>

<span data-ttu-id="266e4-400">C++ および C\# などの一部の言語を使用すると、1 つ以上のインデックスを持つ配列を宣言できます。</span><span class="sxs-lookup"><span data-stu-id="266e4-400">Some languages, such as C++ and C\#, let you declare arrays that have more than one index.</span></span> <span data-ttu-id="266e4-401">つまり、「配列の配列」を定義することができます。</span><span class="sxs-lookup"><span data-stu-id="266e4-401">In other words, you can define "arrays of arrays."</span></span> <span data-ttu-id="266e4-402">X++ では、1 次元配列のみサポートされているため、複数の配列インデックスを直接作成できません。</span><span class="sxs-lookup"><span data-stu-id="266e4-402">In X++, you can't directly create multiple array indexes, because only one-dimensional arrays are supported.</span></span> <span data-ttu-id="266e4-403">ただし、このセクションに記載されているメソッドを使用して、複数のインデックスを実装することができます。</span><span class="sxs-lookup"><span data-stu-id="266e4-403">However, you can implement multiple indexes by using the method that is described in this section.</span></span> <span data-ttu-id="266e4-404">たとえば、国別分析コードにより獲得される量を保持するため、2 つの分析コードを持つ配列を宣言します。</span><span class="sxs-lookup"><span data-stu-id="266e4-404">For example, you want to declare an array that has two dimensions, to hold an amount that is earned by country by dimension.</span></span> <span data-ttu-id="266e4-405">10 の国と 3 つの分析コードがあります。</span><span class="sxs-lookup"><span data-stu-id="266e4-405">There are 10 countries and three dimensions.</span></span> <span data-ttu-id="266e4-406">C++ および C\# では、次の配列を宣言します。</span><span class="sxs-lookup"><span data-stu-id="266e4-406">In C++ and C\#, you declare the following array.</span></span>

    // This is C# or C++ code, not X++ code.
    real earning[10, 3];

<span data-ttu-id="266e4-407">ただし、X++ はこの申告をサポートしていません。</span><span class="sxs-lookup"><span data-stu-id="266e4-407">However, X++ doesn't support this declaration.</span></span> <span data-ttu-id="266e4-408">代わりに、要素の数が各分析コード内の要素の製品である 1 次元配列を定義することができます。</span><span class="sxs-lookup"><span data-stu-id="266e4-408">Instead, you can define a one-dimensional array where the number of elements is the product of the elements in each dimension.</span></span> <span data-ttu-id="266e4-409">次に例を示します。</span><span class="sxs-lookup"><span data-stu-id="266e4-409">Here is an example.</span></span>

    public void MultipleArrayMethod()
    {
        // Step 1: define a one-dimensional array with the number
        // of elements that is the product of the elements in each dimension.
        real earnings[10*3];

        // Step 2: to refer to a specific element, such as earnings[i,j], write the following:
        // declare i and j (maybe) and assign the value to something
        int i = 1;
        int j = 2;
        real element = earnings[(i-1)*3 + j];
    }

    // This can be written into a macro like this:
    #localmacro.earningIndex
    (%1-1)*3+%2
    #endmacro

    public void CallTheMacro()
    {
        // Next, call the specific element within the macro like this:
        int i = 1;
        int j = 2;
        real element = earnings[#earningIndex(i,j)];

        // The previous scheme can be extended to any number of dimensions.
        // The element a[i1, i2, ..., ik] can be accessed by computing the
        // offset into an array containing (d1*d2*...*dk) elements.
        //(i1 - 1)*d2*d3*..*dk +
        //(i2 - 1)*d3*d4*...*dk + .... +
        //(ik-1 -1)*dk +
        //(ik-1)
    }

### <a name="container"></a><span data-ttu-id="266e4-410">コンテナー</span><span class="sxs-lookup"><span data-stu-id="266e4-410">Container</span></span>

<span data-ttu-id="266e4-411">*コンテナー*オブジェクトは、プリミティブ データ型または複合データ型が含まれる項目の動的リストです。</span><span class="sxs-lookup"><span data-stu-id="266e4-411">A *container* object is a dynamic list of items that contain primitive data types or composite data types.</span></span> <span data-ttu-id="266e4-412">コンテナーは、クライアント層とサーバー層の間でさまざまな種類の値を渡す必要がある場合に便利です。</span><span class="sxs-lookup"><span data-stu-id="266e4-412">A container is useful when you must pass various types of values between the client and server tiers.</span></span> <span data-ttu-id="266e4-413">ただし、ループ内でのリストに繰り返し追加する予定がある場合、コンテナーは適切な選択肢ではありません。</span><span class="sxs-lookup"><span data-stu-id="266e4-413">However, if you plan to repeatedly add to a list in a loop, a container isn't a good choice.</span></span> <span data-ttu-id="266e4-414">コンテナーは、コンテナーのサイズまたは内容を過度に変更することがないプロセスに最も適しています。</span><span class="sxs-lookup"><span data-stu-id="266e4-414">Containers are most suitable for processes that don't involve excessive modification to the size or contents of the container.</span></span> <span data-ttu-id="266e4-415">コンテナーに過剰にデータが追加されると、コンテナーのデータを繰り返しコピーする必要があり、また新しい領域を繰り返し割り当てる必要があるため、システム全体のパフォーマンスが低下する可能性があります。</span><span class="sxs-lookup"><span data-stu-id="266e4-415">When a container undergoes excessive additions of data, overall system performance can decrease, because container data must be repeatedly copied, and new space must be repeatedly allocated.</span></span> <span data-ttu-id="266e4-416">コンテナーはクラスではありません。</span><span class="sxs-lookup"><span data-stu-id="266e4-416">A container isn't a class.</span></span> <span data-ttu-id="266e4-417">コンテナーには、プリミティブ値またはその他のコンテナーの注文済のシーケンスが含まれています。</span><span class="sxs-lookup"><span data-stu-id="266e4-417">A container contains an ordered sequence of primitive values or other containers.</span></span> <span data-ttu-id="266e4-418">**anytype** の柔軟性のために、コンテナーは異なるタイプの値を一緒に保存する良い方法を提供します。</span><span class="sxs-lookup"><span data-stu-id="266e4-418">Because of the flexibility of **anytype**, a container offers a good way to store values of different types together.</span></span> <span data-ttu-id="266e4-419">コンテナーは、データベースに保管できます。</span><span class="sxs-lookup"><span data-stu-id="266e4-419">A container can be stored in the database.</span></span> <span data-ttu-id="266e4-420">コンテナーとは、アプリケーション エクスプローラーを使用して、テーブルに列を追加する場合に選択可能な列タイプの 1 つです。</span><span class="sxs-lookup"><span data-stu-id="266e4-420">A container is one of the column types that you can select when you use Application Explorer to add a column to a table.</span></span> <span data-ttu-id="266e4-421">配列に少し似た、または **List** や **Stack** クラスのようなコレクションのコンテナーです。</span><span class="sxs-lookup"><span data-stu-id="266e4-421">A container slightly resembles an array, or collections such as the **List** or **Stack** classes.</span></span> <span data-ttu-id="266e4-422">ただし、コンテナーを作成した後にコンテナーのサイズまたはコンテンツを変更できません。</span><span class="sxs-lookup"><span data-stu-id="266e4-422">However, you can never change the size or content of a container after the container is created.</span></span> <span data-ttu-id="266e4-423">コンテナを変更するために表示される X++ ステートメントは、内部で新しいコンテナを構築して必要に応じ値をコピーします。</span><span class="sxs-lookup"><span data-stu-id="266e4-423">X++ statements that appear to modify a container are internally building a new container and copying values as required.</span></span> <span data-ttu-id="266e4-424">コンテナーを別のコンテナー変数に割り当てても、コンテナーの新しいコピーは作成されます。</span><span class="sxs-lookup"><span data-stu-id="266e4-424">Even an assignment of a container to another container variable creates a new copy of the container.</span></span> <span data-ttu-id="266e4-425">これらすべての工程はパフォーマンスに影響を与えることがあります。</span><span class="sxs-lookup"><span data-stu-id="266e4-425">All these operations can affect performance.</span></span> <span data-ttu-id="266e4-426">コンテナーへのアクセスを提供する関数 (**conPeek** など) では、コンテナーは 0 ベースではなく、1 ベースです。</span><span class="sxs-lookup"><span data-stu-id="266e4-426">In the functions that provide access to a container (such as **conPeek**), the container is 1-based, not 0-based.</span></span> <span data-ttu-id="266e4-427">インデックスは配列に対して 1 ベースです。</span><span class="sxs-lookup"><span data-stu-id="266e4-427">Indexing is 1-based for arrays.</span></span> <span data-ttu-id="266e4-428">コンテナーの既定値は **空** です。</span><span class="sxs-lookup"><span data-stu-id="266e4-428">The default value of a container is **empty**.</span></span> <span data-ttu-id="266e4-429">コンテナーには値が含まれていません。</span><span class="sxs-lookup"><span data-stu-id="266e4-429">The container doesn't contain any values.</span></span> <span data-ttu-id="266e4-430">コンテナーを使用するいくつかのステートメントは、コンテナーを変更するように見えることがあります。</span><span class="sxs-lookup"><span data-stu-id="266e4-430">Some statements that use containers might appear to modify a container.</span></span> <span data-ttu-id="266e4-431">ただし、システム内部では、コンテナーは決して変更されません。</span><span class="sxs-lookup"><span data-stu-id="266e4-431">However, inside the system, containers are never modified.</span></span> <span data-ttu-id="266e4-432">代わりに、元のコンテナーからのデータは、新しいコンテナーを構築するためにコマンドからのデータと結合されます。</span><span class="sxs-lookup"><span data-stu-id="266e4-432">Instead, the data from the original container is combined with data from the command to build a new container.</span></span> <span data-ttu-id="266e4-433">**conDel**、**conIns**、または **conPoke** のいずれかの関数を使用して、新しいコンテナを作成することができます。</span><span class="sxs-lookup"><span data-stu-id="266e4-433">You can create a new container by using one of the following functions: **conDel**, **conIns**, or **conPoke**.</span></span> <span data-ttu-id="266e4-434">また、**グローバル** クラスには、コンテナーを処理するための静的メソッドがあります。</span><span class="sxs-lookup"><span data-stu-id="266e4-434">Additionally, the **Global** class has static methods for handling containers.</span></span> <span data-ttu-id="266e4-435">これらのメソッドには、**con2ArraySource**、**con2Buf**、**con2List**、**con2Str**、**containerFromXmlNode**、**conView**、**str2Con** が含まれます。</span><span class="sxs-lookup"><span data-stu-id="266e4-435">These methods include **con2ArraySource**, **con2Buf**, **con2List**, **con2Str**, **containerFromXmlNode**, **conView**, and **str2Con**.</span></span> <span data-ttu-id="266e4-436">**conIns** や **conPeek** のような、コンテナーを扱うためのいくつかの固有の関数があります。</span><span class="sxs-lookup"><span data-stu-id="266e4-436">There are several intrinsic functions for handling a container, such as **conIns** and **conPeek**.</span></span> <span data-ttu-id="266e4-437">X++ **conPeek** 関数は **anytype** タイプを返します。</span><span class="sxs-lookup"><span data-stu-id="266e4-437">The X++ **conPeek** function returns an **anytype** type.</span></span> <span data-ttu-id="266e4-438">したがって、各値の型がわからない場合は、コンテナーから値を読み取る方が簡単です。</span><span class="sxs-lookup"><span data-stu-id="266e4-438">Therefore, it's easier to read the values from a container when you don't know the type of each value.</span></span> <span data-ttu-id="266e4-439">**anytype** は値を変換することができればすべての X++ 値タイプに割り当てることができます。</span><span class="sxs-lookup"><span data-stu-id="266e4-439">An **anytype** can be assigned to any X++ value type, provided that the value can be converted.</span></span> <span data-ttu-id="266e4-440">明示的なデータ型の変換を回避すると、コードは読みやすくなります。</span><span class="sxs-lookup"><span data-stu-id="266e4-440">Your code is easier to read when it avoids explicit data type conversions.</span></span> <span data-ttu-id="266e4-441">したがって、値をコンテナーに配置するために使用されたのと同じデータ型にコンテナーから値を割り当てます。</span><span class="sxs-lookup"><span data-stu-id="266e4-441">Therefore, assign values from a container to the same data type that was used to put the value into the container.</span></span> <span data-ttu-id="266e4-442">コンテナーを **エニタイプ** に割り当てることはできません。適切な変換を決定できない可能性があるためです。</span><span class="sxs-lookup"><span data-stu-id="266e4-442">You must not assign a container to an **anytype**, because the system might not be able to determine the correct conversions.</span></span> <span data-ttu-id="266e4-443">そのような場合、予期しない動作やエラーが発生する可能性があります。</span><span class="sxs-lookup"><span data-stu-id="266e4-443">In these cases, unexpected behavior or errors might occur.</span></span>

#### <a name="comparing-container-to-other-options"></a><span data-ttu-id="266e4-444">コンテナーと他のオプションの比較</span><span class="sxs-lookup"><span data-stu-id="266e4-444">Comparing container to other options</span></span>

<span data-ttu-id="266e4-445">**コンテナー**型は、**List** や **Stack** などの配列およびコレクション クラスなど、他の構成要素と似ています。</span><span class="sxs-lookup"><span data-stu-id="266e4-445">The **container** type resembles other constructs, such as arrays and collection classes such as **List** and **Stack**.</span></span> <span data-ttu-id="266e4-446">コンテナーと **リスト** の違いは、**リスト** クラスのインスタンスが不変であるという点です。</span><span class="sxs-lookup"><span data-stu-id="266e4-446">The difference between a container and **List** is that an instance of the **List** class is mutable.</span></span> <span data-ttu-id="266e4-447">**リスト**オブジェクトは、最初にそのデータが消費するよりも多くの領域を割り当てます。</span><span class="sxs-lookup"><span data-stu-id="266e4-447">A **List** object first allocates more space than its data consumes.</span></span> <span data-ttu-id="266e4-448">その後、データが追加されると、スペースが埋められます。</span><span class="sxs-lookup"><span data-stu-id="266e4-448">Then, as data is added, the space is filled.</span></span> <span data-ttu-id="266e4-449">この動作は、要素が追加されるたびに多くの領域を割り当てる場合よりも効率的です。</span><span class="sxs-lookup"><span data-stu-id="266e4-449">This behavior is more efficient than allocating more space every time that an element is added.</span></span> <span data-ttu-id="266e4-450">**リスト**の更新はコンテナーの同様の操作よりも高速に実行します。</span><span class="sxs-lookup"><span data-stu-id="266e4-450">An update of a **List** performs faster than similar operations on a container.</span></span> <span data-ttu-id="266e4-451">**リスト** オブジェクトを作成するときは、**リスト** オブジェクトが格納できるデータの 1 つのタイプを決定します。</span><span class="sxs-lookup"><span data-stu-id="266e4-451">When you construct a **List** object, you determine the one type of data that the **List** object can store.</span></span> <span data-ttu-id="266e4-452">この制限は、コンテナの場合よりも**リスト**の柔軟性が低くなります。</span><span class="sxs-lookup"><span data-stu-id="266e4-452">This restriction is less flexible for a **List** than it is for a container.</span></span> <span data-ttu-id="266e4-453">ただし、**リスト**のオブジェクトを格納できますが、コンテナーでは値の型しか格納できません。</span><span class="sxs-lookup"><span data-stu-id="266e4-453">However, you can store objects in a **List**, whereas a container can store only value types.</span></span> <span data-ttu-id="266e4-454">コンテナーと配列の違いは、配列は宣言された型の項目だけを保持できるという点です。</span><span class="sxs-lookup"><span data-stu-id="266e4-454">The difference between a container and an array is that an array can hold only items of its declared type.</span></span> <span data-ttu-id="266e4-455">配列にメモリ容量を割り当て、後からその容量に値を入力することができます。</span><span class="sxs-lookup"><span data-stu-id="266e4-455">You can allocate memory space for an array and fill that space with values later.</span></span> <span data-ttu-id="266e4-456">たとえば、ループに値を入力することができます。</span><span class="sxs-lookup"><span data-stu-id="266e4-456">For example, you can fill in values in a loop.</span></span> <span data-ttu-id="266e4-457">この動作は効率的であり、適正に動作します。</span><span class="sxs-lookup"><span data-stu-id="266e4-457">This behavior is efficient and performs well.</span></span> <span data-ttu-id="266e4-458">新しいデータを追加して新しいコンテナーを作成するときは、**+=** 演算子かまたは **conIns** 機能のいずれかを使用します。</span><span class="sxs-lookup"><span data-stu-id="266e4-458">When you want to build a new container by appending new data, you can use either the **+=** operator or the **conIns** function.</span></span> <span data-ttu-id="266e4-459">**+=** 演算子は高速の代替です。</span><span class="sxs-lookup"><span data-stu-id="266e4-459">The **+=** operator is the faster alternative.</span></span> <span data-ttu-id="266e4-460">**conIns** 関数は、元のデータの最後のインデックスの前に新しいデータを追加する場合にのみ使用します。</span><span class="sxs-lookup"><span data-stu-id="266e4-460">Use the **conIns** function only when you want to add new data before the last index of the original data.</span></span> <span data-ttu-id="266e4-461">Dynamics AX 2012 では、コンテナーのオブジェクト参照を格納するために X++ コンパイラを使用できましたが、結果は実行時に失敗していました。</span><span class="sxs-lookup"><span data-stu-id="266e4-461">In Dynamics AX 2012, although you could use the X++ compiler to store object references in containers, the result would fail at run time.</span></span> <span data-ttu-id="266e4-462">ただし、Microsoft Dynamics 365 for Finance and Operations で、コンパイラがコンテナー内のオブジェクト参照を格納しようとする試みを確認すると、エラー メッセージを出します。</span><span class="sxs-lookup"><span data-stu-id="266e4-462">However, in Microsoft Dynamics 365 for Finance and Operations, when the compiler sees an attempt to store an object reference in a container, it issues an error message.</span></span> <span data-ttu-id="266e4-463">コンテナーに追加される要素のタイプが **anytype** である場合、コンパイラーは値は参照タイプであるかどうかを決定することをできません。</span><span class="sxs-lookup"><span data-stu-id="266e4-463">If the type of the element that is added to the container is **anytype**, the compiler can’t determine whether the value is a reference type.</span></span> <span data-ttu-id="266e4-464">この場合、コンパイラはその試行を認めます。</span><span class="sxs-lookup"><span data-stu-id="266e4-464">In this case, the compiler allows the attempt.</span></span> <span data-ttu-id="266e4-465">ユーザーは何をしているかを把握しているとみなされます。</span><span class="sxs-lookup"><span data-stu-id="266e4-465">It's assumed that the user knows what he or she is doing.</span></span> <span data-ttu-id="266e4-466">コンパイラはコードを誤っていると診断しませんが、エラーは実行時間にスローされます。</span><span class="sxs-lookup"><span data-stu-id="266e4-466">Although the compiler doesn't diagnose the code as erroneous, an error will be thrown at run time.</span></span>

#### <a name="container-examples"></a><span data-ttu-id="266e4-467">コンテナーの例</span><span class="sxs-lookup"><span data-stu-id="266e4-467">Container examples</span></span>

    public void ContainerExample() 
    {
        // First, declare the variables you are using.  
        container myContainer;
        container myContainer4;
        container myContainer5; 
        // Three ways to declare a container.
        myContainer = [1];
        myContainer += [2];
        myContainer4 = myContainer5;

        // Declare a container.
        container cr3;

        // Assign a literal container to a container variable.
        cr3 = [22, "blue"];

        // Declare and assign a container.
        container cr2 = [1, "blue", true];

        // Mimic container modification (implicitly creates a copy).
        cr3 += [16, strMyColorString];
        cr3 = conIns(cr3, 1, 3.14);
        cr3 = conPoke(cr3, 2, "violet");

        // Assignment of a container (implicitly creates a copy).
        cr2 = cr3;

        // Read a value from the container.
        str  myStr = conPeek(cr2, 1);

        // One statement that does multiple assignments from a container.
        str myStr;
        int myInt;
        container cr4 = ["Hello", 22, 20\07\1988];
        [myStr, myInt] = cr4; // "Hello", 22

        // Example of applying the = operator to a container. The example
        // initializes myContainer2 and myContainer33.
        myContainer2 = [2, "apple"];

        // Next, you make a copy of myContainer33 and assign the copy to myContainer2.
        myContainer33 = [33, "grape"];
        myContainer2 = myContainer33;  // The container that myContainer2 had been holding is no longer available and cannot be recovered.
        // An example of building a new container by
        // assigning a new value to myContainer33 through the += operator.
        myContainer33 += [34, "banana"];
    }

    // List class example. In this example, variable2 and variable3 refer to the same List object.
    static void JobC(Args _args)
    {
        container variable2, variable33;
        variable2 += [98];
        variable33 = variable2;
        variable2 += [97];
    }

    // Container example. The variable2 and variable3 hold different containers.
    static void JobL(Args _args)
    {
        List variable2,variable33;
        variable2 = new List(Types::Integer);
        variable2.addEnd(98);
        variable33 = variable2;
        variable2.addEnd(97);
    }

    // The automatic type conversion by anytype also applies to the special syntax for making multiple
    // assignments from a container in one statement. This is shown in the following code example,
    // which assigns a str to an int, and an int to a str.
    static void JobContainerMultiAssignmentUsesAnytype(Args _args)
    {
        container con2;
        int int4;
        str str7;
        con2 = ["11", 222];
        [int4, str7] = con2;
        info(strfmt("int4==11==(%1), str7==222==(%2)", int4, str7));
    }

    /***  Output:
    Message (10:36:22 am)
    int4==11==(11), str7==222==(222)
    ***/

    static void UseQuery()
    {
        // An example of how the compiler diagnoses attempts to store object in containers
        container c = [new Query()];   // This statement will cause the error message shown below.
        /*** Instance of type 'Query' cannot be added to a container. ***/

        // An example of a code that won't cause an error message, but will
        // cause an error message to be thrown at runtime.
        anytype a = new Query();
        container d = [a];
    }

### <a name="classes-as-data-types"></a><span data-ttu-id="266e4-468">データ型としてのクラス</span><span class="sxs-lookup"><span data-stu-id="266e4-468">Classes as data types</span></span>

<span data-ttu-id="266e4-469">*クラス*は、クラスのインスタンスの変数とメソッドの両方を説明するタイプ定義です。</span><span class="sxs-lookup"><span data-stu-id="266e4-469">A *class* is a type definition that describes both variables and methods for instances of the class.</span></span> <span data-ttu-id="266e4-470">(クラスのインスタンスは*オブジェクト*ともよばれます。) クラスはオブジェクトの定義に過ぎず、すべてのオブジェクトは宣言されると **null** です。</span><span class="sxs-lookup"><span data-stu-id="266e4-470">(The instances of a class are also known as *objects*.) A class is only a definition for objects, and all objects are **null** when they are declared.</span></span> <span data-ttu-id="266e4-471">アプリケーション エクスプローラーでは、**クラス** ノードの各アプリケーション クラスはデータ型です。</span><span class="sxs-lookup"><span data-stu-id="266e4-471">In Application Explorer, every application class under the **Classes** node is a data type.</span></span> <span data-ttu-id="266e4-472">これらの種類の変数をコード内で宣言することができます。</span><span class="sxs-lookup"><span data-stu-id="266e4-472">You can declare variables of these types in your code.</span></span> <span data-ttu-id="266e4-473">クラスのインスタンスを構築してインスタンスを変数に割り当てることができます。</span><span class="sxs-lookup"><span data-stu-id="266e4-473">You can construct instances of a class and assign the instances to variables.</span></span> <span data-ttu-id="266e4-474">クラスはソース コードに入れ子にできます。</span><span class="sxs-lookup"><span data-stu-id="266e4-474">Classes can be nested in source code.</span></span> <span data-ttu-id="266e4-475">入れ子になったクラスはフォーム内 (**FormRun** を拡張するクラスなど) でのみ使用でき、コントロール、データ ソースまたはデータ フィールドを表すために使用します。</span><span class="sxs-lookup"><span data-stu-id="266e4-475">Nested classes are available only inside forms (such as a class that extends **FormRun**), and are used to represent controls, data sources, or data fields.</span></span> <span data-ttu-id="266e4-476">属性の修飾で接尾語に**属性**がある場合、属性の修飾などのクラスまたはメソッドで、属性名の接尾語を省略できます。</span><span class="sxs-lookup"><span data-stu-id="266e4-476">An attribute decoration, such as the attribute decoration on a class or a method, can omit the suffix of the attribute name if the suffix is **Attribute**.</span></span> <span data-ttu-id="266e4-477">したがって、X++ は **\[MyFavoriteAttribute\]** を必要とするのではなく、**\[MyFavorite\]** を許可します。</span><span class="sxs-lookup"><span data-stu-id="266e4-477">Therefore, X++ allows **\[MyFavorite\]** instead of requiring **\[MyFavoriteAttribute\]**.</span></span> <span data-ttu-id="266e4-478">また、属性はデリゲートとメソッドのハンドラーに現在適用され、ハンドラーをこれらのターゲットにマップします。</span><span class="sxs-lookup"><span data-stu-id="266e4-478">Additionally, attributes are now applied to the handlers of delegates and methods, to map the handlers to those targets.</span></span> <span data-ttu-id="266e4-479">AX 2012 およびそれ以前のバージョンでは、クライアントまたはサーバーのいずれかで実行するメソッドを指定することができました。</span><span class="sxs-lookup"><span data-stu-id="266e4-479">In AX 2012 and earlier versions, you could designate a method to run on either the client or the server.</span></span> <span data-ttu-id="266e4-480">ただし、Microsoft Dynamics 365 for Finance and Operations およびそれ以降のバージョンでは、コンパイルされたすべての X++ コードがサーバーの .NET 共通中間言語 (CIL) として実行されます。</span><span class="sxs-lookup"><span data-stu-id="266e4-480">However, in Microsoft Dynamics 365 for Finance and Operations and later versions, all compiled X++ code is run as .NET Common Intermediate Language (CIL) on the server.</span></span> <span data-ttu-id="266e4-481">クライアント サイトまたはブラウザーで評価されるコードはなくなりました。</span><span class="sxs-lookup"><span data-stu-id="266e4-481">There is no longer any code that is evaluated at the client site or in the browser.</span></span> <span data-ttu-id="266e4-482">したがって、**client** キーワードと **server** キーワードは無視されるようになりました。</span><span class="sxs-lookup"><span data-stu-id="266e4-482">Therefore, the **client** and **server** keywords are now ignored.</span></span> <span data-ttu-id="266e4-483">これらのキーワードが使用される場合コンパイル エラーは発生しませんが、新しいコードを使用することはできません。</span><span class="sxs-lookup"><span data-stu-id="266e4-483">Although these keywords don't cause a compile error if they are used, they should not be used in any new code.</span></span>

#### <a name="private-and-protected-member-variables"></a><span data-ttu-id="266e4-484">プライベートおよび保護されたメンバー変数</span><span class="sxs-lookup"><span data-stu-id="266e4-484">Private and protected member variables</span></span>

<span data-ttu-id="266e4-485">以前は、クラスで定義されていたすべてのメンバー変数が保護されていました。</span><span class="sxs-lookup"><span data-stu-id="266e4-485">Previously, all member variables that were defined in a class were protected.</span></span> <span data-ttu-id="266e4-486">**private**、**protected**、および **public** キーワードを加えることにより、メンバー変数の表示を明示的にすることができるようになりました。</span><span class="sxs-lookup"><span data-stu-id="266e4-486">You can now make the visibility of member variables explicit by adding the **private**, **protected**, and **public** keywords.</span></span> <span data-ttu-id="266e4-487">これらの修飾子の解釈は明白であり、メソッドのセマンティクスに沿っています。</span><span class="sxs-lookup"><span data-stu-id="266e4-487">The interpretation of these modifiers is obvious and is aligned with the semantics for methods:</span></span>

-   <span data-ttu-id="266e4-488">**プライベート** – メンバー変数は、定義されているクラス内でのみ使用できます。</span><span class="sxs-lookup"><span data-stu-id="266e4-488">**private** – The member variable can be used only within the class where it’s defined.</span></span>
-   <span data-ttu-id="266e4-489">**保護されている** – メンバー変数は、それが定義されているクラスおよびクラスのすべてのサブクラスで使用できます。</span><span class="sxs-lookup"><span data-stu-id="266e4-489">**protected** – The member variable can be used in the class where it’s defined and all subclasses of that class.</span></span>
-   <span data-ttu-id="266e4-490">**パブリック** – メンバー変数を任意の場所に使用することができます。</span><span class="sxs-lookup"><span data-stu-id="266e4-490">**public** – The member variable can be used anywhere.</span></span> <span data-ttu-id="266e4-491">これは、定義されているクラス階層の範囲外に表示されます。</span><span class="sxs-lookup"><span data-stu-id="266e4-491">It’s visible outside the confines of the class hierarchy where it’s defined.</span></span>

<span data-ttu-id="266e4-492">既定では、明示的なモディファイアーで実装されていないメンバー変数は引き続き保護されています。</span><span class="sxs-lookup"><span data-stu-id="266e4-492">By default, member variables that aren’t adorned with an explicit modifier are still protected.</span></span> <span data-ttu-id="266e4-493">ただし、ベスト プラクティスとしては、可視性を明示的に指定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="266e4-493">However, as a best practice, you should explicitly specify the visibility.</span></span> <span data-ttu-id="266e4-494">先に説明したように、メンバー変数が**パブリック**として定義されている場合、メンバー変数は定義されているクラス外でアクセスできます。</span><span class="sxs-lookup"><span data-stu-id="266e4-494">As we described earlier, when a member variable is defined as **public**, it can be accessed outside the class where it’s defined.</span></span> <span data-ttu-id="266e4-495">この場合、変数をホストしているオブジェクトを指定する修飾子を指定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="266e4-495">In this case, you must specify a qualifier that designates the object that is hosting the variable.</span></span> <span data-ttu-id="266e4-496">修飾子を指定するには、メソッド呼び出しの場合と同様にドット表記法を使用します。</span><span class="sxs-lookup"><span data-stu-id="266e4-496">To specify the qualifier, use the dot notation, as you do for method calls.</span></span> <span data-ttu-id="266e4-497">次の例では、**field1** に明示的な **this** 修飾子を使用することでアクセスします。</span><span class="sxs-lookup"><span data-stu-id="266e4-497">In the following example, **field1** is accessed by using the explicit **this** qualifier.</span></span> <span data-ttu-id="266e4-498">この場合、そのアプローチは消費者にクラスの内部作業を公開することになり、クラスの実装と消費者の間に強い依存関係が生じるため、メンバー変数をパブリックにすることをお勧めできない場合があります。</span><span class="sxs-lookup"><span data-stu-id="266e4-498">In this case, it might not be a good idea to make a member variable public, because that approach exposes the internal workings of the class to its consumers, and therefore creates a strong dependency between the class implementation and its consumers.</span></span> <span data-ttu-id="266e4-499">常に、実装ではなくコントラクトにのみ依存させる必要があります。</span><span class="sxs-lookup"><span data-stu-id="266e4-499">You should always try to depend only on a contract, not an implementation.</span></span>

    public class AnotherClass3
    {
        int field1;
        str field2;
        void new()
        {
            this.field1 = 1;   // Explicit object designated.
            field2 = "Banana";  // 'this' assumed, as usual.
        }
    }

#### <a name="static-constructors-and-static-fields"></a><span data-ttu-id="266e4-500">静的コンストラクターおよび静的フィールド</span><span class="sxs-lookup"><span data-stu-id="266e4-500">Static constructors and static fields</span></span>

<span data-ttu-id="266e4-501">*静的フィールド*は**静的**キーワードを使用して宣言されているフィールドです。</span><span class="sxs-lookup"><span data-stu-id="266e4-501">*Static fields* are fields that are declared by using the **static** keyword.</span></span> <span data-ttu-id="266e4-502">概念的には、クラスのインスタンスではなく静的フィールドに適用されます。</span><span class="sxs-lookup"><span data-stu-id="266e4-502">Conceptually, static fields apply to the class, not to instances of the class.</span></span> <span data-ttu-id="266e4-503">静的コンストラクターは、静的呼び出しまたはインスタンス呼び出しがクラスに対して行われる前に実行されることが保証されます。</span><span class="sxs-lookup"><span data-stu-id="266e4-503">Static constructors are guaranteed to run before any static calls or instance calls are made to the class.</span></span> <span data-ttu-id="266e4-504">静的コンストラクターの実行は、ユーザーのセッションに対して相対的です。</span><span class="sxs-lookup"><span data-stu-id="266e4-504">The execution of the static constructor is relative to the user’s session.</span></span> <span data-ttu-id="266e4-505">静的コンストラクターは明示的に呼び出さないでください。</span><span class="sxs-lookup"><span data-stu-id="266e4-505">You never call the static constructor explicitly.</span></span> <span data-ttu-id="266e4-506">代わりに、コンパイラはコンストラクターがクラスの他のメソッドの前に正確に 1 回呼び出されるようにするコードを生成します。</span><span class="sxs-lookup"><span data-stu-id="266e4-506">Instead, the compiler will generate code to make sure that the constructor is called exactly one time, before any other method on the class is called.</span></span> <span data-ttu-id="266e4-507">静的コンストラクターは、任意の静的データを初期化したり、一度だけ実行する必要のあるアクションを実行するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="266e4-507">A static constructor is used to initialize any static data or perform an action that must be performed only one time.</span></span> <span data-ttu-id="266e4-508">静的コンストラクターのパラメーターを指定することはできず、**静的** キーワードでマークされる必要があります。</span><span class="sxs-lookup"><span data-stu-id="266e4-508">You can't provide parameters for the static constructor, and it must be marked with the **static** keyword.</span></span>

    // An example of how a singleton (call instance in the example below)
    // can be created using the static constructor.
    public class Singleton
    {
        private static Singleton instance;
        private void new()
        {
        }
        static void TypeNew()    // This is the static constructor.
        {
            instance = new Singleton();
        }

        public static Singleton Instance()
        {
            return Singleton::instance;
        }
    }

    // The singleton ensures that only one instance of the class
    // will be called, which is consumed by the following. 
    {
        // Your code here.
        Singleton i = Singleton::Instance();
    }

#### <a name="class-elements-in-application-explorer"></a><span data-ttu-id="266e4-509">アプリケーション エクスプローラーのクラス要素</span><span class="sxs-lookup"><span data-stu-id="266e4-509">Class elements in Application Explorer</span></span>

<span data-ttu-id="266e4-510">アプリケーション エクスプ ローラーのほとんどのクラス・ノードの下には、**classDeclaration** ノードと **new** ノードという 2 つの特殊ノードがあります。</span><span class="sxs-lookup"><span data-stu-id="266e4-510">Under most class nodes in Application Explorer, there are two special nodes: a **classDeclaration** node and a **new** node.</span></span> <span data-ttu-id="266e4-511">**classDeclaration** は、常に X++ **クラス**キーワードになります。</span><span class="sxs-lookup"><span data-stu-id="266e4-511">A **classDeclaration** always contains the X++ **class** keyword.</span></span> <span data-ttu-id="266e4-512">追加のキーワードは、**拡張**のように、クラスを変更するために含めることができます。</span><span class="sxs-lookup"><span data-stu-id="266e4-512">Additional keywords, such as **extends**, can be included to modify the class.</span></span> <span data-ttu-id="266e4-513">このノードには、メンバー変数の宣言も含めることができます。</span><span class="sxs-lookup"><span data-stu-id="266e4-513">This node can also contain declarations of member variables.</span></span> <span data-ttu-id="266e4-514">メンバー変数は、**classDeclaration** の値に初期化することはできません。また静的にすることはできません。</span><span class="sxs-lookup"><span data-stu-id="266e4-514">The member variables can't be initialized to a value in **classDeclaration**, and they can't be static.</span></span> <span data-ttu-id="266e4-515">次の例では、変数 **m\_priority** および **m\_rectangle** はクラスのメンバーです。</span><span class="sxs-lookup"><span data-stu-id="266e4-515">In the following example, the variables **m\_priority** and **m\_rectangle** are members of the class.</span></span>

    // An example of a classDeclaration.
    public class YourDerivedClass extends YourBaseClass
    {
        int m_priority;
        Rectangle m_rectangle;
        void new(int _length, int _width)
        {
            this.m_rectangle = new Rectangle(_length, _width);
        }
    }

<span data-ttu-id="266e4-516">**新しい**演算子には、**新しい**演算子を使用して、クラスのインスタンスを作成するときに実行されるロジックが含まれます。</span><span class="sxs-lookup"><span data-stu-id="266e4-516">A **new** operator contains logic that is run when the **new** operator is used to create an instance of the class.</span></span> <span data-ttu-id="266e4-517">**新規** メソッドのロジックは、オブジェクトを作成し、そのオブジェクトを **classDeclaration** で宣言された変数に割り当てることができます。</span><span class="sxs-lookup"><span data-stu-id="266e4-517">The logic in the **new** method might construct an object and assign that object to a variable that is declared in the **classDeclaration**.</span></span> <span data-ttu-id="266e4-518">各クラスは、**新しい**方法を 1 つだけ持つことが可能です。</span><span class="sxs-lookup"><span data-stu-id="266e4-518">Each class can have only one **new** method.</span></span> <span data-ttu-id="266e4-519">ただし、**新しい**メソッドでは、多くの場合基本クラスの**新しい**メソッドを呼び出す必要があります。</span><span class="sxs-lookup"><span data-stu-id="266e4-519">However, in the **new** method, you often should call the **new** method of the base class.</span></span> <span data-ttu-id="266e4-520">基本クラスの<**新規**メソッドを呼び出すには、**super()** を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="266e4-520">To call the **new** method of the base class, call **super()**.</span></span> <span data-ttu-id="266e4-521">次の例は、前の **classDeclaration** の例の **YourDerivedClass** クラスの **new** メソッドを示しています。</span><span class="sxs-lookup"><span data-stu-id="266e4-521">The following example shows the **new** method for the **YourDerivedClass** class in the previous **classDeclaration** example.</span></span> <span data-ttu-id="266e4-522">この**新しい**メソッドで、コードは**長方形**クラスのインスタンスを構築します。</span><span class="sxs-lookup"><span data-stu-id="266e4-522">In this **new** method, the code constructs an instance of the **Rectangle** class.</span></span> <span data-ttu-id="266e4-523">インスタンスは、**m\_rectangle** 変数に割り当てられます。</span><span class="sxs-lookup"><span data-stu-id="266e4-523">The instance is assigned to the **m\_rectangle** variable.</span></span> <span data-ttu-id="266e4-524">例で使用される **this** キーワードはオプションです。</span><span class="sxs-lookup"><span data-stu-id="266e4-524">The **this** keyword that is used in the example is optional.</span></span> <span data-ttu-id="266e4-525">ただし、それを含める場合、IntelliSense が役立つ可能性があります。</span><span class="sxs-lookup"><span data-stu-id="266e4-525">However, if you include it, IntelliSense might be more helpful.</span></span>

    // An example of the new method from the previous classDeclaration example.
    void new(int _length, int _width)
    {
        this.m_rectangle = new Rectangle(_length, _width);
    }

#### <a name="garbage-collection"></a><span data-ttu-id="266e4-526">ガベージ コレクション</span><span class="sxs-lookup"><span data-stu-id="266e4-526">Garbage collection</span></span>

<span data-ttu-id="266e4-527">最終的に実行中では、ほとんどのオブジェクトがそれらを指す変数はなくなります。</span><span class="sxs-lookup"><span data-stu-id="266e4-527">Eventually during run time, most objects no longer have any variable that points to them.</span></span> <span data-ttu-id="266e4-528">システムはこれらのオブジェクトをスキャンし、それらをメモリから消去します。</span><span class="sxs-lookup"><span data-stu-id="266e4-528">The system scans for these objects and erases them from memory.</span></span> <span data-ttu-id="266e4-529">その後、メモリ空間は他の用途に利用できるようになります。</span><span class="sxs-lookup"><span data-stu-id="266e4-529">The memory space then becomes available for other uses.</span></span> <span data-ttu-id="266e4-530">**Object** クラスには、**finalize** というメソッドがあります。</span><span class="sxs-lookup"><span data-stu-id="266e4-530">The **Object** class has a method that is named **finalize**.</span></span> <span data-ttu-id="266e4-531">ただし、**確定**メソッドはデストラクタではありません。</span><span class="sxs-lookup"><span data-stu-id="266e4-531">However, the **finalize** method isn't a destructor.</span></span> <span data-ttu-id="266e4-532">ランタイムは、オブジェクトがガベージとして収集された場合でも、**finalize** メソッドを呼び出すことはありません。</span><span class="sxs-lookup"><span data-stu-id="266e4-532">The runtime never calls the **finalize** method, even when an object is collected as garbage.</span></span>

#### <a name="system-classes"></a><span data-ttu-id="266e4-533">システム クラス</span><span class="sxs-lookup"><span data-stu-id="266e4-533">System classes</span></span>

<span data-ttu-id="266e4-534">アプリケーション エクスプローラーの**システムのドキュメント** &gt; **クラス**には、カーネル クラスまたはシステム クラスの一覧があります。</span><span class="sxs-lookup"><span data-stu-id="266e4-534">In Application Explorer, under **System Documentation** &gt; **Classes**, there is a list of the kernel classes or system classes.</span></span> <span data-ttu-id="266e4-535">システム クラスは、X++ で記述されておらず、ソース コードを表示することはできません。</span><span class="sxs-lookup"><span data-stu-id="266e4-535">System classes aren't written in X++, and you can't see their source code.</span></span> <span data-ttu-id="266e4-536">システム クラスを追加することはできません。</span><span class="sxs-lookup"><span data-stu-id="266e4-536">You can't add system classes.</span></span> <span data-ttu-id="266e4-537">システム クラには通常、**new** メソッドがありますが、**classDeclaration** ノードはありません。</span><span class="sxs-lookup"><span data-stu-id="266e4-537">System classes usually have a **new** method, but they don't have a **classDeclaration** node.</span></span> <span data-ttu-id="266e4-538">すべてのアプリケーション クラスは**オブジェクト**システム クラスを暗黙的に拡張します。</span><span class="sxs-lookup"><span data-stu-id="266e4-538">Every application class implicitly extends the **Object** system class.</span></span> <span data-ttu-id="266e4-539">一部のシステム クラスは、類似した名前を持つアプリケーション クラスで拡張されます。</span><span class="sxs-lookup"><span data-stu-id="266e4-539">Some system classes are extended by an application class that has a similar name.</span></span> <span data-ttu-id="266e4-540">たとえば、**xClassFactory** が **ClassFactory** ごとに延期されます。</span><span class="sxs-lookup"><span data-stu-id="266e4-540">For instance, **xClassFactory** is extended by **ClassFactory**.</span></span> <span data-ttu-id="266e4-541">そのような場合、システム クラスは使用しないでください。</span><span class="sxs-lookup"><span data-stu-id="266e4-541">In these cases, you should not use the system class.</span></span> <span data-ttu-id="266e4-542">詳細については、[X++ クラスおよびメソッド](xpp-classes-methods.md) で「システム クラスの代替アプリケーション クラス」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="266e4-542">For more information, see "Substitute application classes for system classes" in [X++ classes and methods](xpp-classes-methods.md).</span></span>

#### <a name="extension-methods"></a><span data-ttu-id="266e4-543">拡張メソッド</span><span class="sxs-lookup"><span data-stu-id="266e4-543">Extension methods</span></span>

<span data-ttu-id="266e4-544">拡張メソッド機能を使用すると、メソッドを別の拡張クラスに記述することによって、拡張メソッドを対象クラスに追加できます。</span><span class="sxs-lookup"><span data-stu-id="266e4-544">The extension method feature lets you add extension methods to a target class by writing the methods in a separate extension class.</span></span> <span data-ttu-id="266e4-545">次のルールが適用されます。</span><span class="sxs-lookup"><span data-stu-id="266e4-545">The following rules apply:</span></span>

-   <span data-ttu-id="266e4-546">拡張クラスは静的でなければなりません。</span><span class="sxs-lookup"><span data-stu-id="266e4-546">The extension class must be static.</span></span>
-   <span data-ttu-id="266e4-547">拡張クラスの名前は、10 文字の接尾語 **\_Extension** で終了する必要があります。</span><span class="sxs-lookup"><span data-stu-id="266e4-547">The name of the extension class must end with the ten-character suffix **\_Extension**.</span></span> <span data-ttu-id="266e4-548">ただし、接尾辞に先行する名前の部分には制限はありません。</span><span class="sxs-lookup"><span data-stu-id="266e4-548">However, there’s no restriction on the part of the name that precedes the suffix.</span></span>
-   <span data-ttu-id="266e4-549">拡張子クラス内のすべての拡張子メソッドは、**パブリック静的**として宣言する必要があります。</span><span class="sxs-lookup"><span data-stu-id="266e4-549">Every extension method in the extension class must be declared as **public static**.</span></span>
-   <span data-ttu-id="266e4-550">すべての拡張メソッドの最初のパラメーターは、拡張メソッドが拡張する型です。</span><span class="sxs-lookup"><span data-stu-id="266e4-550">The first parameter in every extension method is the type that the extension method extends.</span></span> <span data-ttu-id="266e4-551">ただし、拡張メソッドが呼び出されると、呼び出し元は最初のパラメーターに対して何も渡す必要がありません。</span><span class="sxs-lookup"><span data-stu-id="266e4-551">However, when the extension method is called, the caller must not pass in anything for the first parameter.</span></span> <span data-ttu-id="266e4-552">代わりに、システムが最初のパラメーターに必要なオブジェクトを自動的に渡します。</span><span class="sxs-lookup"><span data-stu-id="266e4-552">Instead, the system automatically passes in the required object for the first parameter.</span></span>
-   <span data-ttu-id="266e4-553">拡張メソッドのターゲットは、クラス、テーブル、ビュー、またはマップ アプリケーション オブジェクト タイプである必要があります。</span><span class="sxs-lookup"><span data-stu-id="266e4-553">The target of an extension method must be a class, table, view, or map application object type.</span></span>

<span data-ttu-id="266e4-554">拡張クラスはプライベートまたは保護された静的メソッドを含めることができます。</span><span class="sxs-lookup"><span data-stu-id="266e4-554">An extension class can contain private or protected static methods.</span></span> <span data-ttu-id="266e4-555">これらのメソッドは通常、実装の詳細に使用され、拡張として公開されません。</span><span class="sxs-lookup"><span data-stu-id="266e4-555">These methods are typically used for implementation details and aren't exposed as extensions.</span></span> <span data-ttu-id="266e4-556">拡張メソッドの手法は、拡張するクラスのソース コードには影響しません。</span><span class="sxs-lookup"><span data-stu-id="266e4-556">The extension method technique doesn’t affect the source code of the class that it extends.</span></span> <span data-ttu-id="266e4-557">したがって、クラスへの追加はオーバーレイを必要なく行うことができます。</span><span class="sxs-lookup"><span data-stu-id="266e4-557">Therefore, the addition to the class doesn't require over-layering.</span></span> <span data-ttu-id="266e4-558">ターゲット クラスへのアップグレードは、既存の拡張メソッドの影響を受けることはありません。</span><span class="sxs-lookup"><span data-stu-id="266e4-558">Upgrades to the target class are never affected by any existing extension methods.</span></span> <span data-ttu-id="266e4-559">ただし、ターゲット クラスへのアップグレードで拡張メソッドとして同じ名前のメソッドが追加される場合、拡張メソッドはターゲット クラスのオブジェクトを通して到達できなくなります。</span><span class="sxs-lookup"><span data-stu-id="266e4-559">However, if an upgrade to the target class adds a method that has the same name as your extension method, your extension method can no longer be reached through objects of the target class.</span></span> <span data-ttu-id="266e4-560">拡張メソッドの手法では、通常のインスタンス メソッドを呼び出すときによく使うドット区切り構文と同じものを使用します。</span><span class="sxs-lookup"><span data-stu-id="266e4-560">The extension method technique uses the same dot-delimited syntax that you often use to call regular instance methods.</span></span> <span data-ttu-id="266e4-561">拡張メソッドは、ターゲット クラスのすべてのパブリック コンポーネントにアクセスできますが、保護されたまたはプライベートのオブジェクトには何もアクセスできません。</span><span class="sxs-lookup"><span data-stu-id="266e4-561">Extension methods can access all public artifacts of the target class, but they can’t access anything that is protected or private.</span></span> <span data-ttu-id="266e4-562">したがって、拡張メソッドは構文砂糖の一種と考えることができます。</span><span class="sxs-lookup"><span data-stu-id="266e4-562">Therefore, extension methods can be considered a type of syntactic sugar.</span></span> <span data-ttu-id="266e4-563">目標タイプに関係なく、拡張機能クラスはタイプに拡張メソッドを追加するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="266e4-563">Regardless of the target type, an extension class is used to add extension methods to the type.</span></span> <span data-ttu-id="266e4-564">たとえば、拡張テーブルは、メソッドをテーブルに追加するために使用されていませんし、拡張テーブルというものは存在しません。</span><span class="sxs-lookup"><span data-stu-id="266e4-564">For example, an extension table isn't used to add methods to a table, and there’s no such thing as an extension table.</span></span>

    // An example of an extension class holding a few extension methods.
    public static class AtlInventLocation_Extension
    {
        public static InventLocation refillEnabled(
           InventLocation _warehouse,
           boolean _isRefillEnabled = true)
        {
           _warehouse.ReqRefill = _isRefillEnabled;
           return _warehouse;
        }

        public static InventLocation save(InventLocation _warehouse)
        {
           _warehouse.write();
           return _warehouse;
        }
    }

### <a name="delegates-as-data-types"></a><span data-ttu-id="266e4-565">データ型としてのデリゲート</span><span class="sxs-lookup"><span data-stu-id="266e4-565">Delegates as data types</span></span>

<span data-ttu-id="266e4-566">*デリゲート*は、それをサブスクライブするメソッドを収集します。</span><span class="sxs-lookup"><span data-stu-id="266e4-566">A *delegate* collects methods that subscribe to it.</span></span> <span data-ttu-id="266e4-567">デリゲートは、すべてのサブスクライバ メソッドが共有する必要があるパラメーター署名を指定します。</span><span class="sxs-lookup"><span data-stu-id="266e4-567">The delegate specifies the parameter signature that all its subscriber methods must share.</span></span> <span data-ttu-id="266e4-568">デリゲートが呼び出されると、デリゲートはその各サブスクライバを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="266e4-568">When the delegate is called, the delegate calls each of its subscribers.</span></span> <span data-ttu-id="266e4-569">デリゲートは値を返しませんし、**既定値を持つことはできません**。</span><span class="sxs-lookup"><span data-stu-id="266e4-569">A delegate never returns a value and **can't have a default value**.</span></span> <span data-ttu-id="266e4-570">最初に、すべてのデリゲートにはサブスクライブされたメソッドがありません。</span><span class="sxs-lookup"><span data-stu-id="266e4-570">At first, every delegate has no subscribed methods.</span></span> <span data-ttu-id="266e4-571">デリゲートが宣言できるパラメーターの数に制限はなく、これらのパラメーターの種類に制限はありません。</span><span class="sxs-lookup"><span data-stu-id="266e4-571">There is no limit on the number of parameters that a delegate can declare, and there is no limitation on the type of those parameters.</span></span> <span data-ttu-id="266e4-572">デリゲートの唯一の目的は、サブスクライバが従わなければならない契約を定義することであるため、デリゲート本文は常に空です。</span><span class="sxs-lookup"><span data-stu-id="266e4-572">The delegate body is always empty, because the delegate's only purpose is to define the contract that subscribers must conform to.</span></span> <span data-ttu-id="266e4-573">デリゲートは、クラスで定義をしなくてもかまいません。</span><span class="sxs-lookup"><span data-stu-id="266e4-573">A delegate doesn't have to be defined in a class.</span></span> <span data-ttu-id="266e4-574">デリゲートは、テーブル、フォーム、またはクエリで定義することもできます。</span><span class="sxs-lookup"><span data-stu-id="266e4-574">Delegates can also be defined in a table, form, or query.</span></span>

#### <a name="delegate-examples"></a><span data-ttu-id="266e4-575">デリゲートの例</span><span class="sxs-lookup"><span data-stu-id="266e4-575">Delegate examples</span></span>

    abstract class VarDatClass
    {
        // delegatemethod examples
        // An example of declaring a delegate.
        delegate void notifyChange(utcdatetime _dateTime, str _changeDescription)
        {
        }

        // An example of subscribing an event handler to a delegate.
        public static void notifyStatic(utcDateTime _dateTime, str _changeDescription)
        {
            info("A notification has occurred calling static handler:" +
                DateTimeUtil::toStr(_dateTime) +
                " Message:" +
                _changeDescription);
        }
    }

### <a name="tables-as-data-types"></a><span data-ttu-id="266e4-576">データ型としてのテーブル</span><span class="sxs-lookup"><span data-stu-id="266e4-576">Tables as data types</span></span>

<span data-ttu-id="266e4-577">すべてのテーブルはクラス定義として扱うことができます。</span><span class="sxs-lookup"><span data-stu-id="266e4-577">All tables can be treated as class definitions.</span></span> <span data-ttu-id="266e4-578">テーブル変数は、テーブル (class) の定義のインスタンス (オブジェクト) と見なすことができます。</span><span class="sxs-lookup"><span data-stu-id="266e4-578">A table variable can be considered an instance (object) of the table (class) definition.</span></span> <span data-ttu-id="266e4-579">テーブル変数の各フィールドでは、既定値は**空**です。</span><span class="sxs-lookup"><span data-stu-id="266e4-579">For every field in a table variable, the default value is **empty**.</span></span> <span data-ttu-id="266e4-580">フィールドに注意を向けてテーブル上でメソッドを作成することができます。</span><span class="sxs-lookup"><span data-stu-id="266e4-580">You can address fields and create methods on tables.</span></span> <span data-ttu-id="266e4-581">これらのメソッドは、テーブルのインスタンス上で呼び出すことができます。</span><span class="sxs-lookup"><span data-stu-id="266e4-581">The methods can be invoked on instances of the table.</span></span> <span data-ttu-id="266e4-582">テーブル内のレコードを操作 (つまり、読み取り、更新、挿入、削除) するには、レコードを保持しておくための少なくとも 1 つのテーブル変数を宣言する必要があります。</span><span class="sxs-lookup"><span data-stu-id="266e4-582">To manipulate (that is, read, update, insert, and delete) records in tables, you must declare at least one table variable that can hold the record in focus.</span></span> <span data-ttu-id="266e4-583">ベスト プラクティスは、変数の名前としてテーブルの名前を使用する必要がありますが、最初の小文字を使用します。</span><span class="sxs-lookup"><span data-stu-id="266e4-583">As a best practice, you should use the name of the table as the name of the variable but use an initial lowercase letter.</span></span> <span data-ttu-id="266e4-584">テーブルとオブジェクト間のいくつかの重要な違いを次に示します。</span><span class="sxs-lookup"><span data-stu-id="266e4-584">Here are a few important differences between tables and objects:</span></span>

-   <span data-ttu-id="266e4-585">テーブル変数の容量を割り当てることはできません。</span><span class="sxs-lookup"><span data-stu-id="266e4-585">You can't allocate space for table variables.</span></span> <span data-ttu-id="266e4-586">配賦は暗黙的に行われます。</span><span class="sxs-lookup"><span data-stu-id="266e4-586">Allocation is done implicitly.</span></span>
-   <span data-ttu-id="266e4-587">テーブル変数のフィールドは、パブリックです。</span><span class="sxs-lookup"><span data-stu-id="266e4-587">Fields in table variables are public.</span></span> <span data-ttu-id="266e4-588">任意の場所でそれを参照することができます。</span><span class="sxs-lookup"><span data-stu-id="266e4-588">You can reference them anywhere.</span></span>
-   <span data-ttu-id="266e4-589">テーブル変数のフィールドは、式を使用して参照できます。</span><span class="sxs-lookup"><span data-stu-id="266e4-589">Fields in table variables can be referenced by using expressions.</span></span>

<span data-ttu-id="266e4-590">自動変換はありませんが、**共通**として宣言されているテーブル変数は、どのテーブルからでもデータを保持できます。</span><span class="sxs-lookup"><span data-stu-id="266e4-590">There is no automatic conversion, but table variables that are declared as **Common** can hold data from any table.</span></span>

#### <a name="scope-of-table-variables"></a><span data-ttu-id="266e4-591">テーブル変数の範囲</span><span class="sxs-lookup"><span data-stu-id="266e4-591">Scope of table variables</span></span>

<span data-ttu-id="266e4-592">ほとんどの点で、テーブル変数をオブジェクトとみなすことができます。</span><span class="sxs-lookup"><span data-stu-id="266e4-592">In most respects, table variables can be considered objects.</span></span> <span data-ttu-id="266e4-593">ただし、オブジェクトとは異なり、それらは明示的に割り当てられません。</span><span class="sxs-lookup"><span data-stu-id="266e4-593">However, unlike objects, they aren't explicitly allocated.</span></span> <span data-ttu-id="266e4-594">変数の宣言のみ必要です。</span><span class="sxs-lookup"><span data-stu-id="266e4-594">Only a variable declaration is required.</span></span> <span data-ttu-id="266e4-595">すべてのテーブルには共通のテーブルと互換性があるように、すべてのオブジェクトにも**オブジェクト**クラスの互換性があります。</span><span class="sxs-lookup"><span data-stu-id="266e4-595">All tables are compatible with the Common table, just as all objects are compatible with the **Object** class.</span></span> <span data-ttu-id="266e4-596">テーブル変数は、一般的なバッファーとして宣言され、任意のテーブルからデータを保持するために使用できます。</span><span class="sxs-lookup"><span data-stu-id="266e4-596">Table variables are declared as common buffers and can be used to hold data from any table.</span></span> <span data-ttu-id="266e4-597">テーブル変数を持たないテーブルにはアクセスできません。</span><span class="sxs-lookup"><span data-stu-id="266e4-597">You can't access tables that don't have table variables.</span></span> <span data-ttu-id="266e4-598">テーブルの変数およびオブジェクトの宣言の原則は、領域の割り当てに関する点を除いて同じです。</span><span class="sxs-lookup"><span data-stu-id="266e4-598">The principles for declaring table variables and objects are the same, except with regard to the allocation of space.</span></span>

#### <a name="table-examples"></a><span data-ttu-id="266e4-599">テーブルの例</span><span class="sxs-lookup"><span data-stu-id="266e4-599">Table examples</span></span>

<span data-ttu-id="266e4-600">構文は、レコード内のフィールドを参照するさまざまな可能性を高めます。</span><span class="sxs-lookup"><span data-stu-id="266e4-600">The syntax enables various possibilities for referencing fields in records.</span></span> <span data-ttu-id="266e4-601">たとえば、**TableName.(FieldId)** 構文を使用できます。</span><span class="sxs-lookup"><span data-stu-id="266e4-601">For example, you can use the **TableName.(FieldId)** syntax.</span></span> <span data-ttu-id="266e4-602">次の例では、顧客テーブルの現在のレコードにあるフィールドの内容を出力します。</span><span class="sxs-lookup"><span data-stu-id="266e4-602">The following example prints the contents of the fields in the current record in the Customer table.</span></span>

    // Declares and allocates space for one CustTable record.
    public void myMethod()
    {
        CustomerTable custTable;
    }

    // An example of referencing table variables.
    public void printAccountNo()
    {
        CustomerTable custTable;
        print custTable.AccountNo;  // Prints the field reference.
    }

<span data-ttu-id="266e4-603">次の例では、**fieldCnt** および **fieldCnt2Id** メソッドを使用しています。</span><span class="sxs-lookup"><span data-stu-id="266e4-603">The following example uses the **fieldCnt** and **fieldCnt2Id** methods.</span></span> <span data-ttu-id="266e4-604">**fieldCnt** メソッドは、テーブル内のフィールドの数をカウントしますが、**fieldCnt2Id** はフィールド番号の ID を返します。</span><span class="sxs-lookup"><span data-stu-id="266e4-604">The **fieldCnt** method counts the number of fields in a table, whereas **fieldCnt2Id** returns the ID for a field number.</span></span> <span data-ttu-id="266e4-605">たとえば、**fieldCnt2Id** メソッドを使用して、テーブルでそのフィールド番号 6 が ID 54 を持っていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="266e4-605">For example, you can use the **fieldCnt2Id** method to learn that field number 6 in a table has the ID 54.</span></span> <span data-ttu-id="266e4-606">この変換は、表内のフィールドの ID が連続しているという保証がないため、この変換が必要です。</span><span class="sxs-lookup"><span data-stu-id="266e4-606">This conversion is required, because there is no guarantee that the IDs of the fields in a table are consecutive.</span></span>

    // An example of the various possibilities for referencing fields in records.
    public void printCust()
    {
        int i, n, k;
        CustomerTable custTable;
        DictTable dictTable;
        dictTable = new DictTable(custTable.TableId);
        n = dictTable.fieldCnt();
        print "Number of fields in table: ", n;
        for(i=1; i<=n; i++)
        {
            k = dictTable.fieldCnt2Id(i);
            print "The ", dictTable.fieldName(k),
            " field with Id=",k, " contains '",
            custTable.(k), "'";
        }
    }

## <a name="collection-classes"></a><span data-ttu-id="266e4-607">コレクション クラス</span><span class="sxs-lookup"><span data-stu-id="266e4-607">Collection classes</span></span>
<span data-ttu-id="266e4-608">X++ 言語の構文には、配列とコンテナーという 2 種類の複合が用意されています。</span><span class="sxs-lookup"><span data-stu-id="266e4-608">The X++ language syntax provides two composite types: arrays and containers.</span></span> <span data-ttu-id="266e4-609">これらの複合型は、プリミティブ型の値を集約するのに便利です。</span><span class="sxs-lookup"><span data-stu-id="266e4-609">These composite types are useful for aggregating values of primitive types.</span></span> <span data-ttu-id="266e4-610">ただし、配列またはコンテナーのクラス オブジェクトを格納することはできません。</span><span class="sxs-lookup"><span data-stu-id="266e4-610">However, you can't store class objects in arrays or containers.</span></span> <span data-ttu-id="266e4-611">*コレクション クラス*はオブジェクトの格納に使用されます。</span><span class="sxs-lookup"><span data-stu-id="266e4-611">*Collection classes* are used to store objects.</span></span> <span data-ttu-id="266e4-612">これらは、配列、リスト、セット、マップ、任意のデータ型を保持できる構造、オブジェクトさえも作成できます。</span><span class="sxs-lookup"><span data-stu-id="266e4-612">They let you create arrays, lists, sets, maps, and structs that can hold any data type, even objects.</span></span> <span data-ttu-id="266e4-613">最大パフォーマンスについては、C++ (システム クラス) で、クラスが実装されます。</span><span class="sxs-lookup"><span data-stu-id="266e4-613">For maximum performance, the classes are implemented in C++ (they are system classes).</span></span> <span data-ttu-id="266e4-614">*ファンデーション クラス*と呼ばれていたコレクション クラス。</span><span class="sxs-lookup"><span data-stu-id="266e4-614">Collection classes were previously known as *foundation classes*.</span></span> <span data-ttu-id="266e4-615">コレクション クラスは、**配列**、**リスト**、**マップ**、**設定**、および**構造体**です。</span><span class="sxs-lookup"><span data-stu-id="266e4-615">The collection classes are **Array**, **List**, **Map**, **Set**, and **Struct**.</span></span>

-   <span data-ttu-id="266e4-616">**配列** - このクラスは、X++ 言語の**配列**タイプに似ていますが、単一タイプ、オブジェクトおよびレコードの値を保持できます。</span><span class="sxs-lookup"><span data-stu-id="266e4-616">**Array** – This class resembles the **array** type in the X++ language, but it can hold values of any single type, even objects and records.</span></span> <span data-ttu-id="266e4-617">オブジェクトは、特定の順序でアクセスされます。</span><span class="sxs-lookup"><span data-stu-id="266e4-617">Objects are accessed in a specific order.</span></span>
-   <span data-ttu-id="266e4-618">**リスト** – このクラスには、順にアクセスされる要素が含まれます。</span><span class="sxs-lookup"><span data-stu-id="266e4-618">**List** – This class contains elements that are accessed sequentially.</span></span> <span data-ttu-id="266e4-619">配列とは異なり、**List** クラスは **addStart** メソッドを提供します。</span><span class="sxs-lookup"><span data-stu-id="266e4-619">Unlike an array, the **List** class provides an **addStart** method.</span></span> <span data-ttu-id="266e4-620">**Set** クラスと同様に、**List** クラスは **getEnumerator** メソッドと **getIterator** メソッドを提供します。</span><span class="sxs-lookup"><span data-stu-id="266e4-620">Like the **Set** class, the **List** class provides the **getEnumerator** and **getIterator** methods.</span></span> <span data-ttu-id="266e4-621">反復子を使用して、**リスト** オブジェクトから項目を挿入および削除することができます。</span><span class="sxs-lookup"><span data-stu-id="266e4-621">You can use an iterator to insert and delete items from a **List** object.</span></span>
-   <span data-ttu-id="266e4-622">**マップ** – このクラスはキー値を別の値に関連付けます。</span><span class="sxs-lookup"><span data-stu-id="266e4-622">**Map** – This class associates a key value with another value.</span></span>
-   <span data-ttu-id="266e4-623">**設定** – このクラスは、1 つのタイプの値を保持します。</span><span class="sxs-lookup"><span data-stu-id="266e4-623">**Set** – This class holds values of any single type.</span></span> <span data-ttu-id="266e4-624">値は、追加された順序で格納されません。</span><span class="sxs-lookup"><span data-stu-id="266e4-624">Values aren't stored in the sequence in which they are added.</span></span> <span data-ttu-id="266e4-625">代わりに、**Set** オブジェクトは **in** メソッドのパフォーマンスを最適化するように値を格納します。</span><span class="sxs-lookup"><span data-stu-id="266e4-625">Instead, the **Set** object stores the value in a manner that optimizes performance for the **in** method.</span></span> <span data-ttu-id="266e4-626">**セット**オブジェクトは、**セット**オブジェクトが既に格納している値を追加しようとする試みをすべて無視します。</span><span class="sxs-lookup"><span data-stu-id="266e4-626">A **Set** object ignores any attempt to add a value that the **Set** object is already storing.</span></span> <span data-ttu-id="266e4-627">**Set** クラスは、**Array** クラスとは異なり、**in** メソッドと **remove** メソッドを提供します。</span><span class="sxs-lookup"><span data-stu-id="266e4-627">Unlike the **Array** class, the **Set** class provides the **in** and **remove** methods.</span></span>
-   <span data-ttu-id="266e4-628">**構造体** – このクラスは、1 つ以上のタイプの値を含めることができます。</span><span class="sxs-lookup"><span data-stu-id="266e4-628">**Struct** – This class can contain values of more than one type.</span></span> <span data-ttu-id="266e4-629">これは、特定のエンティティに関する情報をグループ化するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="266e4-629">It's used to group information about a specific entity.</span></span>

<span data-ttu-id="266e4-630">**構造体**を除くすべてのコレクション クラスのコンストラクターは、**型**システム列挙型の要素である型パラメーターをとります。</span><span class="sxs-lookup"><span data-stu-id="266e4-630">The constructor for every collection class except **Struct** takes a type parameter that is an element of the **Types** system enum.</span></span> <span data-ttu-id="266e4-631">コレクション インスタンスは、その型のアイテムのみを格納できます。</span><span class="sxs-lookup"><span data-stu-id="266e4-631">The collection instance can store items of that type only.</span></span> <span data-ttu-id="266e4-632">**Types::AnyType** 列挙要素は、**Set** オブジェクトなどのコレクション オブジェクトを作成するために使用できない特殊なケースです。</span><span class="sxs-lookup"><span data-stu-id="266e4-632">The **Types::AnyType** enum element is a special case that can't be used to construct a collection object, such as a **Set** object.</span></span> <span data-ttu-id="266e4-633">**null** 値は、**Set** オブジェクトに要素として格納できません。</span><span class="sxs-lookup"><span data-stu-id="266e4-633">The **null** value can't be stored as an element in a **Set** object.</span></span> <span data-ttu-id="266e4-634">また、**マップ** オブジェクトで **null** はキーになることはできません。</span><span class="sxs-lookup"><span data-stu-id="266e4-634">Additionally, **null** can't be a key in a **Map** object.</span></span> <span data-ttu-id="266e4-635">反復子または列挙子を使用して、コレクション オブジェクトを介して反復することができます。</span><span class="sxs-lookup"><span data-stu-id="266e4-635">You can iterate through a collection object by using an iterator or enumerator.</span></span> <span data-ttu-id="266e4-636">反復子を取得する方法を示す一般的な例を次に示します。</span><span class="sxs-lookup"><span data-stu-id="266e4-636">Here are typical examples that show how you can obtain an iterator.</span></span>

    new MapIterator(myMap)
    myMap.getEnumerator()

<span data-ttu-id="266e4-637">**設定**オブジェクトで、任意の要素が追加または反復子が作成された後に削除される場合、反復子インスタンスは読み取りまたはコレクションによるステップで使用されることはなくなります。</span><span class="sxs-lookup"><span data-stu-id="266e4-637">For **Set** objects, if any elements are added or removed after an iterator is created, the iterator instance can no longer be used to read from or step through the collection.</span></span> <span data-ttu-id="266e4-638">**マップ**オブジェクトで、**設定**オブジェクトと同じように、任意の要素が削除されると、反復子が有効ではなくなります。</span><span class="sxs-lookup"><span data-stu-id="266e4-638">For **Map** objects, as for **Set** objects, if any elements are removed, the iterator is no longer valid.</span></span> <span data-ttu-id="266e4-639">ただし、キーが新しいか、またはキーが既に存在していてその値のみが**マップ**要素で更新されているかどうかに関係なく、**Map.insert** メソッドへの呼び出し後も、**MapIterator** オブジェクトは有効です。</span><span class="sxs-lookup"><span data-stu-id="266e4-639">However, a **MapIterator** object remains valid even after a call to the **Map.insert** method, regardless of whether the key is new, or whether the key already exists and only the value is being updated in the **Map** element.</span></span> <span data-ttu-id="266e4-640">**Map.insert** を呼び出し、反復子オブジェクトが有効であることに依存するコードは、.NET Framework CIL として実行されると失敗する可能性があります。</span><span class="sxs-lookup"><span data-stu-id="266e4-640">Code that calls **Map.insert** and depends on the iterator object remaining valid might fail if it's run as .NET Framework CIL.</span></span> <span data-ttu-id="266e4-641">コレクション クラスを使用するとより複雑なクラスを作成することができます。</span><span class="sxs-lookup"><span data-stu-id="266e4-641">You can use the collection classes to form more complex classes.</span></span> <span data-ttu-id="266e4-642">たとえば、リストの先頭に要素が常に追加されるリストを使用して、スタックを簡単に実装できます。</span><span class="sxs-lookup"><span data-stu-id="266e4-642">For example, you can easily implement a stack by using a list where elements are always added to the beginning of the list.</span></span> <span data-ttu-id="266e4-643">最新の要素がスタックの先頭を占めます。</span><span class="sxs-lookup"><span data-stu-id="266e4-643">The newest element then occupies the top of the stack.</span></span> <span data-ttu-id="266e4-644">コレクション クラスを拡張することもできます。</span><span class="sxs-lookup"><span data-stu-id="266e4-644">You can also extend the collection classes.</span></span> <span data-ttu-id="266e4-645">たとえば、**リスト**クラスを拡張して、操作がタイプ セーフである顧客レコードの一覧を作成します。</span><span class="sxs-lookup"><span data-stu-id="266e4-645">For example, you can extend the **List** class to create a list of customer records where the operations are type-safe.</span></span> <span data-ttu-id="266e4-646">この場合、派生したコレクション クラスは顧客レコードのみを受け入れます。</span><span class="sxs-lookup"><span data-stu-id="266e4-646">In this case, the derived collection class will accept only customer records.</span></span>

## <a name="extended-data-types"></a><span data-ttu-id="266e4-647">拡張データ型</span><span class="sxs-lookup"><span data-stu-id="266e4-647">Extended data types</span></span>
<span data-ttu-id="266e4-648">*拡張データ型*は**ブール**、**int**、**int64**、**実数**、**str**、および**日付**プリミティブ データ型、および**コンテナー**複合型に基づくユーザー定義型です。</span><span class="sxs-lookup"><span data-stu-id="266e4-648">*Extended data types* are user-defined types that are based on the **boolean**, **int**, **int64**, **real**, **str**, and **date** primitive data types, and on the **container** composite type.</span></span> <span data-ttu-id="266e4-649">EDT はプリミティブ データ型または補助名および追加のプロパティを持つコンテナーです。</span><span class="sxs-lookup"><span data-stu-id="266e4-649">An EDT is a primitive data type or container that has a supplementary name and additional properties.</span></span> <span data-ttu-id="266e4-650">たとえば、文字列を基準にして、**名前**という新しい EDT を作成することができます。</span><span class="sxs-lookup"><span data-stu-id="266e4-650">For example, you can create a new EDT that is named **Name** and base it on a string.</span></span> <span data-ttu-id="266e4-651">新しい EDT は、開発環境の変数とフィールド宣言で使用することができます。</span><span class="sxs-lookup"><span data-stu-id="266e4-651">You can then use the new EDT in variable and field declarations in the development environment.</span></span> <span data-ttu-id="266e4-652">また、EDT を他の EDT の基準にすることができます。</span><span class="sxs-lookup"><span data-stu-id="266e4-652">You can also base EDTs on other EDTs.</span></span> <span data-ttu-id="266e4-653">EDTs は、標準的なデータ型ですが、特定の名前および追加のプロパティがあります。</span><span class="sxs-lookup"><span data-stu-id="266e4-653">EDTs are standard data types, but they have a specific name and additional properties.</span></span> <span data-ttu-id="266e4-654">EDTs は、それらが基づいている標準データ型と同じ値とタイプ[換算](xpp-conversion-run-time-functions.md)を適用します。</span><span class="sxs-lookup"><span data-stu-id="266e4-654">EDTs undergo the same value and type [conversions](xpp-conversion-run-time-functions.md) as the standard data types that they are based on.</span></span> <span data-ttu-id="266e4-655">EDT の利点を次に示します。</span><span class="sxs-lookup"><span data-stu-id="266e4-655">Here are the benefits of EDTs:</span></span>

-   <span data-ttu-id="266e4-656">変数は意味のあるデータ型を持つため、コードは読みやすくなります。</span><span class="sxs-lookup"><span data-stu-id="266e4-656">Code is easier to read, because variables have a meaningful data type.</span></span> <span data-ttu-id="266e4-657">たとえば、データ型は **str** の代わりに**名前**です。</span><span class="sxs-lookup"><span data-stu-id="266e4-657">For example, the data type is **Name** instead of **str**.</span></span>
-   <span data-ttu-id="266e4-658">EDT に設定するプロパティは、そのタイプのすべてのインスタンスで使用されます。</span><span class="sxs-lookup"><span data-stu-id="266e4-658">The properties that you set for an EDT are used by all instances of that type.</span></span> <span data-ttu-id="266e4-659">したがって、EDT は作業を減らし、一貫性を促進するのに役立ちます。</span><span class="sxs-lookup"><span data-stu-id="266e4-659">Therefore, EDTs help reduce work and promote consistency.</span></span> <span data-ttu-id="266e4-660">たとえば、勘定番号 (**AccountNum** データ型) には、システム全体で同じプロパティがあります。</span><span class="sxs-lookup"><span data-stu-id="266e4-660">For example, account numbers (**AccountNum** data type) have the same properties throughout the system.</span></span>
-   <span data-ttu-id="266e4-661">EDT の階層を作成することができます。</span><span class="sxs-lookup"><span data-stu-id="266e4-661">You can create hierarchies of EDTs.</span></span> <span data-ttu-id="266e4-662">EDT は、親から適切なプロパティを継承でき、その他のプロパティを変更することができます。</span><span class="sxs-lookup"><span data-stu-id="266e4-662">The EDTs can inherit the appropriate properties from the parent, and you can change other properties.</span></span> <span data-ttu-id="266e4-663">たとえば、**ItemCode** データ型が、**MarkupItemCode** および **PriceDiscItemCode** データ型の基準として使用されます。</span><span class="sxs-lookup"><span data-stu-id="266e4-663">For example, the **ItemCode** data type is used as the basis for the **MarkupItemCode** and **PriceDiscItemCode** data types.</span></span>

### <a name="create-an-edt"></a><span data-ttu-id="266e4-664">EDT の作成</span><span class="sxs-lookup"><span data-stu-id="266e4-664">Create an EDT</span></span>

<span data-ttu-id="266e4-665">この機能は、言語コンストラクトとして実装されていません。</span><span class="sxs-lookup"><span data-stu-id="266e4-665">This feature isn't implemented as a language construct.</span></span> <span data-ttu-id="266e4-666">EDT を作成するには、次の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="266e4-666">To create an EDT, follow these steps.</span></span>

1.  <span data-ttu-id="266e4-667">ソリューション エクスプローラーで、プロジェクトを右クリックして**追加**をポイントしてから**新しい項目**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="266e4-667">In Solution Explorer, right-click on the project, point to **Add**, and then click **New item**.</span></span>
2.  <span data-ttu-id="266e4-668">**新しい項目の追加**ダイアログ ボックスで、**インストール済み**を選択してから左ウィンドウの**アーティファクト**を選択します。</span><span class="sxs-lookup"><span data-stu-id="266e4-668">In the **Add New Item** dialog box, select **Installed** and then **Artifacts** in the left pane.</span></span>
3.  <span data-ttu-id="266e4-669">中央ウィンドウで、作成する EDT タイプを選択します。</span><span class="sxs-lookup"><span data-stu-id="266e4-669">In the middle pane, select the EDT type to create.</span></span>
4.  <span data-ttu-id="266e4-670">名前を入力し、次に**追加**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="266e4-670">Enter a name, and then click **Add**.</span></span>

### <a name="edt-example"></a><span data-ttu-id="266e4-671">EDT 例</span><span class="sxs-lookup"><span data-stu-id="266e4-671">EDT example</span></span>

    public void EdtMethod()
    {
        // Example of declaring EDT variables where
        // a UserGroupID (integer) variable is declared and initialized to 1.
        UserGroupID groupID = 1;

        // An Amount (real) variable is declared.
        Amount currency;
    }

## <a name="null-values-for-data-types"></a><span data-ttu-id="266e4-672">データ型の null 値</span><span class="sxs-lookup"><span data-stu-id="266e4-672">Null values for data types</span></span>
<span data-ttu-id="266e4-673">Microsoft Dynamics 365 for Finance and Operations は、その他の数多くのデータベース管理システム (DBMS) で使用できる **null** 値の概念をサポートしていません。</span><span class="sxs-lookup"><span data-stu-id="266e4-673">Microsoft Dynamics 365 for Finance and Operations doesn't support the concept of **null** values that is available in many other database management systems (DBMSs).</span></span> <span data-ttu-id="266e4-674">X++ の変数は、常にタイプと値を持ちます。</span><span class="sxs-lookup"><span data-stu-id="266e4-674">A variable in X++ always has a type and a value.</span></span> <span data-ttu-id="266e4-675">ただし、各データ タイプでは、1 つの値が **null** と見なされます (たとえば、**validateField** テーブル メソッドの実行時)。</span><span class="sxs-lookup"><span data-stu-id="266e4-675">However, for each data type, one value is considered **null** (for example, when the **validateField** table method is run).</span></span>

| <span data-ttu-id="266e4-676">種類</span><span class="sxs-lookup"><span data-stu-id="266e4-676">Type</span></span>        | <span data-ttu-id="266e4-677">null として扱われる値</span><span class="sxs-lookup"><span data-stu-id="266e4-677">Value that is treated as null</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
|-------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="266e4-678">日</span><span class="sxs-lookup"><span data-stu-id="266e4-678">Date</span></span>        | <span data-ttu-id="266e4-679">1900-01-01</span><span class="sxs-lookup"><span data-stu-id="266e4-679">1900-01-01</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| <span data-ttu-id="266e4-680">列挙</span><span class="sxs-lookup"><span data-stu-id="266e4-680">Enum</span></span>        | <span data-ttu-id="266e4-681">その値が **0** に設定されている要素</span><span class="sxs-lookup"><span data-stu-id="266e4-681">An element that has its value set to **0**</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| <span data-ttu-id="266e4-682">整数</span><span class="sxs-lookup"><span data-stu-id="266e4-682">Integer</span></span>     | <span data-ttu-id="266e4-683">0</span><span class="sxs-lookup"><span data-stu-id="266e4-683">0</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
| <span data-ttu-id="266e4-684">実数</span><span class="sxs-lookup"><span data-stu-id="266e4-684">Real</span></span>        | <span data-ttu-id="266e4-685">0.0</span><span class="sxs-lookup"><span data-stu-id="266e4-685">0.0</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| <span data-ttu-id="266e4-686">文字列</span><span class="sxs-lookup"><span data-stu-id="266e4-686">String</span></span>      | <span data-ttu-id="266e4-687">空の文字列</span><span class="sxs-lookup"><span data-stu-id="266e4-687">An empty string</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| <span data-ttu-id="266e4-688">時刻</span><span class="sxs-lookup"><span data-stu-id="266e4-688">Time</span></span>        | <span data-ttu-id="266e4-689">00:00:00</span><span class="sxs-lookup"><span data-stu-id="266e4-689">00:00:00</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| <span data-ttu-id="266e4-690">Utcdatetime</span><span class="sxs-lookup"><span data-stu-id="266e4-690">Utcdatetime</span></span> | <span data-ttu-id="266e4-691">時間部分の値に関係なく、日付部分が **1900-01-01** に設定されている値たとえば、値 **1900-01-01T22:33:44** は **null** として扱われます。</span><span class="sxs-lookup"><span data-stu-id="266e4-691">Any value that has its date portion set to **1900-01-01**, regardless of the value of the time portion For example, the value **1900-01-01T22:33:44** is treated as **null**.</span></span> <span data-ttu-id="266e4-692">日付部分が **1900-01-01** に設定されている **utcDateTime** 値は X++ **print** ステートメントでは空白で表示されることに注意してください。</span><span class="sxs-lookup"><span data-stu-id="266e4-692">Note that any **utcDateTime** value that has its date portion set to **1900-01-01** is shown as blank by the X++ **print** statement.</span></span> <span data-ttu-id="266e4-693">**1900-01-01T00:00:00** 値のみ空白として **Global::info** メソッドにより表示されます。</span><span class="sxs-lookup"><span data-stu-id="266e4-693">Only the value **1900-01-01T00:00:00** is shown as blank by the **Global::info** method.</span></span> <span data-ttu-id="266e4-694">値は、**DateTimeUtil::MinValue** メソッドの値です。</span><span class="sxs-lookup"><span data-stu-id="266e4-694">That value is the value from the **DateTimeUtil::MinValue** method.</span></span> |

<span data-ttu-id="266e4-695">したがって、**validateField** メソッドによりユーザーが必須項目に入力したかどうかがチェックされる際、たとえば、**0** は **integer** タイプ フィールドで許容されず、最初のエントリは **enum** タイプ フィールドで許容されません。</span><span class="sxs-lookup"><span data-stu-id="266e4-695">Therefore, when the **validateField** method checks whether a user has entered a value in a mandatory field, **0** isn't accepted in an **integer** type field, the first entry isn't accepted in an **enum** type field, and so on.</span></span> <span data-ttu-id="266e4-696">また、SQL X++ ステートメントで、前のテーブルにリストされている値は、ブール値比較で **false** になります。</span><span class="sxs-lookup"><span data-stu-id="266e4-696">Additionally, in SQL X++ statements, the values that are listed in the previous table yield **false** in a Boolean comparison.</span></span> <span data-ttu-id="266e4-697">ただし、非 SQL X++ ステートメントでは、同等演算子およびリレーショナル演算子は他の値に対して動作するのと同じように、これらの値に対して動作します。</span><span class="sxs-lookup"><span data-stu-id="266e4-697">However, In non-SQL X++ statements, the equal and relational operators work with these values, just as they work with other values.</span></span> <span data-ttu-id="266e4-698">従来の DBMS の意味では、**コンテナー**型と**テーブル**型のクラスおよび変数は **null** とすることができます。</span><span class="sxs-lookup"><span data-stu-id="266e4-698">Variables of the **container** type, and classes and variables of the **table** type can be **null** in the traditional DBMS sense.</span></span> <span data-ttu-id="266e4-699">**テーブル**タイプは、すべてのフィールドに **null** 値がある場合は **null** です。</span><span class="sxs-lookup"><span data-stu-id="266e4-699">A **table** type is **null** if all its fields have their **null** value.</span></span>



