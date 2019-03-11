---
title: X++ およびデバッガーの機能
description: このチュートリアルでは、開発者が X++ 言語の高度なコンストラクトを使用し、生産的なデバッガ機能を利用できるようにすることを目的としています。 これは、これらの機能を使用してプラクティスするための新しい機能のチュートリアルです。
author: pvillads
manager: AnnBe
ms.date: 11/03/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Developer
ms.reviewer: robinr
ms.search.scope: Operations
ms.custom: 26801
ms.assetid: 27c65e79-df74-4249-b684-97e1d40da753
ms.search.region: Global
ms.author: pvillads
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 8706e9ea940c535271f01aabcee90f5f3a340c4d
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/29/2019
ms.locfileid: "369715"
---
# <a name="x-and-debugger-features"></a><span data-ttu-id="6850f-104">X++ およびデバッガーの機能</span><span class="sxs-lookup"><span data-stu-id="6850f-104">X++ and debugger features</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="6850f-105">このチュートリアルでは、開発者が X++ 言語の高度なコンストラクトを使用し、生産的なデバッガ機能を利用できるようにすることを目的としています。</span><span class="sxs-lookup"><span data-stu-id="6850f-105">This tutorial is for developers to use advanced constructs of the X++ language and take advantage of productive debugger features.</span></span> <span data-ttu-id="6850f-106">これは、これらの機能を使用してプラクティスするための新しい機能のチュートリアルです。</span><span class="sxs-lookup"><span data-stu-id="6850f-106">This is a walkthrough of the new features with exercises included to practice using these features.</span></span> 

<span data-ttu-id="6850f-107">以前のバージョンでは、X++ コードは疑似コードつまり P コードにコンパイルされ、サーバーまたはクライアント アプリケーションで解釈されていました。</span><span class="sxs-lookup"><span data-stu-id="6850f-107">In previous versions, the X++ code was compiled into pseudo-code, or p-code, that was interpreted on the server or on the client application.</span></span> <span data-ttu-id="6850f-108">このコードは、その後、CIL にコンパイルされました。</span><span class="sxs-lookup"><span data-stu-id="6850f-108">This code was then subject to further compilation into CIL.</span></span> <span data-ttu-id="6850f-109">今日の話はずっと単純です - CIL だけがサポートされ、このコードは新しいコンパイラから生成されます。</span><span class="sxs-lookup"><span data-stu-id="6850f-109">Today the story is much simpler--only CIL is supported, and this code is generated from a new compiler.</span></span> <span data-ttu-id="6850f-110">このチュートリアルでは、X++ 言語に追加された新しい機能の一部について説明します。</span><span class="sxs-lookup"><span data-stu-id="6850f-110">In this tutorial, we’ll be discussing some of the new features that have been added to the X++ language.</span></span> <span data-ttu-id="6850f-111">シナリオを実行するとき、デバッガーの新機能の一部が表示されます。</span><span class="sxs-lookup"><span data-stu-id="6850f-111">As we run through the scenarios, you’ll also see some of the new features in the debugger.</span></span>

## <a name="declare-anywhere"></a><span data-ttu-id="6850f-112">任意の場所で宣言</span><span class="sxs-lookup"><span data-stu-id="6850f-112">Declare anywhere</span></span>
<span data-ttu-id="6850f-113">以前は、すべてのローカル変数を、使用しているメソッドの先頭に配置する必要がありました。</span><span class="sxs-lookup"><span data-stu-id="6850f-113">Previously, all local variables had to be placed at the start of the method in which they’re used.</span></span> <span data-ttu-id="6850f-114">現在は、変数のスコープを詳細に制御できます。</span><span class="sxs-lookup"><span data-stu-id="6850f-114">Now, you have fine-grained control over the scope of your variables.</span></span> <span data-ttu-id="6850f-115">この新しい機能では、変数のための小さなスコープを用意することができ、この外では変数を参照することはできません。</span><span class="sxs-lookup"><span data-stu-id="6850f-115">With this new feature, it’s possible to provide smaller scopes for variables, outside of which the variables can’t be referenced.</span></span> <span data-ttu-id="6850f-116">変数の有効期間は宣言されているスコープです。</span><span class="sxs-lookup"><span data-stu-id="6850f-116">The lifetime of the variable is the scope in which it’s declared.</span></span> <span data-ttu-id="6850f-117">以下に示すように、スコープは、for ステートメントおよび using ステートメント内においてブロック レベルで開始することができます (複合ステートメント内)。</span><span class="sxs-lookup"><span data-stu-id="6850f-117">Scopes can be started at the block level (inside compound statements), in for statements, and in using statements as we will see below.</span></span> <span data-ttu-id="6850f-118">スコープを小さくすることにはいくつかの利点があります。</span><span class="sxs-lookup"><span data-stu-id="6850f-118">There are several advantages to making scopes small.</span></span>

-   <span data-ttu-id="6850f-119">読みやすさが向上しました。</span><span class="sxs-lookup"><span data-stu-id="6850f-119">Readability is enhanced.</span></span>
-   <span data-ttu-id="6850f-120">コードの長期保守中に変数が不適切に再利用されるリスクを軽減することができます。</span><span class="sxs-lookup"><span data-stu-id="6850f-120">You can reduce the risk of reusing a variable inappropriately during long-term maintenance of the code.</span></span>
-   <span data-ttu-id="6850f-121">リファクタリングがかなり簡単になります。</span><span class="sxs-lookup"><span data-stu-id="6850f-121">Refactoring becomes much easier.</span></span> <span data-ttu-id="6850f-122">使用すべきでないコンテキストで変数が再使用される心配をせずに、コードをコピーすることができます。</span><span class="sxs-lookup"><span data-stu-id="6850f-122">You can copy code in without having to worry about variables being reused in contexts they shouldn’t.</span></span>

### <a name="example"></a><span data-ttu-id="6850f-123">例</span><span class="sxs-lookup"><span data-stu-id="6850f-123">Example</span></span>

<span data-ttu-id="6850f-124">この例では、使用される「for」ステートメント内のループ カウンターを宣言します。</span><span class="sxs-lookup"><span data-stu-id="6850f-124">In this example, we declare the loop counter inside the 'for' statement in which it's used.</span></span>

      void MyMethod()
      {
        for (int i = 0; i < 10; i++)
        {
          info(strfmt("i is %1", i));
        }
      }

<span data-ttu-id="6850f-125">変数のスコープは for ステートメントそのものであり、条件式とループ更新部分を含みます。</span><span class="sxs-lookup"><span data-stu-id="6850f-125">The scope of the variable is the for statement itself, including the condition expression and the loop update parts.</span></span> <span data-ttu-id="6850f-126">この範囲外で値を使用することはできません。</span><span class="sxs-lookup"><span data-stu-id="6850f-126">The value can’t be used outside this scope.</span></span> <span data-ttu-id="6850f-127">それを試行すると、次が表示されます。</span><span class="sxs-lookup"><span data-stu-id="6850f-127">If you attempt to do that, you will get the following.</span></span>

      void MyMethod()
      {
        for (int i = 0; i < 10; i++)
        {
          if (i == 7)
          {
            break;
          }
        }
        info(strfmt("Found: %1", i));
      }

<span data-ttu-id="6850f-128">コンパイラは情報の呼び出しで次のエラー メッセージを発行します: 'i' が宣言されていません。</span><span class="sxs-lookup"><span data-stu-id="6850f-128">The compiler will issue an error message in the info call: 'i' is not declared.</span></span>

### <a name="example"></a><span data-ttu-id="6850f-129">例</span><span class="sxs-lookup"><span data-stu-id="6850f-129">Example</span></span>

<span data-ttu-id="6850f-130">スコープを確立できる場所がもう 1 つあります。using ステートメントは、X++ 言語のもう 1 つの新しいコンポーネントです。</span><span class="sxs-lookup"><span data-stu-id="6850f-130">There's another place where scopes can be established: the using statement, which is another newcomer to the X++ language.</span></span>

      static void AnotherMethod()
      {
        str textFromFile;

        using (System.IO.StreamReader sr = new System.IO.StreamReader("c:\\test.txt"))
        {
          textFromFile = sr.ReadToEnd();
        }
      }

<span data-ttu-id="6850f-131">原則として、IDisposable オブジェクトを使用する場合は、明細書の使用において宣言しインスタンスを作成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="6850f-131">As a rule, when you use an IDisposable object, you should declare and instantiate it in a using statement.</span></span> <span data-ttu-id="6850f-132">using ステートメントは、オブジェクトのメソッドを呼び出すときに例外が発生した場合でも、正しい方法でオブジェクトの Dispose メソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="6850f-132">The using statement calls the Dispose method on the object in the correct way, even if an exception occurs while you are calling methods on the object.</span></span> <span data-ttu-id="6850f-133">オブジェクトを try ブロック内に配置してから finally ブロック内で明示的に Dispose を呼び出すことにより、同じ結果を達成することができます。実際、これはコンパイラが using ステートメントを翻訳する方法です。</span><span class="sxs-lookup"><span data-stu-id="6850f-133">You can achieve the same result by putting the object inside a try block, and then explicitly calling Dispose in a finally block; in fact, this is how the using statement is translated by the compiler.</span></span> <span data-ttu-id="6850f-134">宣言は、提供できる、どこのステートメントにも提供できるようになりました。宣言は構文的なステートメントおよび申告ステートメントです。</span><span class="sxs-lookup"><span data-stu-id="6850f-134">Declarations can now be provided anywhere statements can be provided-- a declaration is syntactically a statement, a declaration statement.</span></span> <span data-ttu-id="6850f-135">したがって、使用する直前に宣言を提供できます。</span><span class="sxs-lookup"><span data-stu-id="6850f-135">You can, therefore, provide declarations immediately prior to the usage.</span></span> <span data-ttu-id="6850f-136">変数をすべて 1 ヶ所で宣言する必要はありません。</span><span class="sxs-lookup"><span data-stu-id="6850f-136">You don’t have to declare the variables all in one place.</span></span>

### <a name="example"></a><span data-ttu-id="6850f-137">例</span><span class="sxs-lookup"><span data-stu-id="6850f-137">Example</span></span>

<span data-ttu-id="6850f-138">次のサンプルは、上記の機能のいくつかを示しています。</span><span class="sxs-lookup"><span data-stu-id="6850f-138">The following sample shows some of the features described above.</span></span>

      // loop variable declared within the loop: It will
      // not be misused outside the loop
      for(int i = 1; i < 10; i++)
      {
      // Because this value is not used from outside the loop,
      // its declaration belongs in this smaller scope.
        str s = int2str(i);
        info(s);
      }

<span data-ttu-id="6850f-139">混乱を避けるために、X++ コンパイラは、囲みスコープ内または同じスコープであっても、別の変数を隠す変数を導入しようとすると、エラーを発行します。</span><span class="sxs-lookup"><span data-stu-id="6850f-139">To avoid confusion, the X++ compiler will issue an error if you attempt to introduce a variable that would hide another variable in an enclosing scope or even in the same scope.</span></span> <span data-ttu-id="6850f-140">たとえば、次のコードは、以下の診断メッセージを発行するコンパイラの原因になります。「i 」と呼ばれるローカルの変数はこのスコープでは宣言されません。それは既に親または現在のスコープで別のものを表示している「 i 」が別の意味になってしまうためです。</span><span class="sxs-lookup"><span data-stu-id="6850f-140">For instance, the following code will cause the compiler to issue the following diagnostic message: A local variable named 'i' cannot be declared in this scope because it would give a different meaning to 'i', which is already used in a parent or current scope to denote something else.</span></span>

      {
        int i;
        {
          int i;
        }
      }

<span data-ttu-id="6850f-141">これは C\# のルールとよく似ていますが、シャドウが診断されていない C ++ のルールとは異なります。</span><span class="sxs-lookup"><span data-stu-id="6850f-141">This aligns well with the rules that are known from C\#, but is different from the rule in C++ where shadowing is not diagnosed.</span></span>

### <a name="exercise"></a><span data-ttu-id="6850f-142">練習</span><span class="sxs-lookup"><span data-stu-id="6850f-142">Exercise</span></span>

<span data-ttu-id="6850f-143">FMVehicleInventoryServiceClass のコードを変更して、より小さなスコープを使用します。</span><span class="sxs-lookup"><span data-stu-id="6850f-143">Adapt the code in FMVehicleInventoryServiceClass to use smaller scopes.</span></span>

## <a name="static-constructors-and-static-fields"></a><span data-ttu-id="6850f-144">静的コンストラクターおよび静的フィールド</span><span class="sxs-lookup"><span data-stu-id="6850f-144">Static constructors and static fields</span></span>
<span data-ttu-id="6850f-145">静的コンストラクターおよび静的フィールドは、X++ 言語の新しい機能です。</span><span class="sxs-lookup"><span data-stu-id="6850f-145">Static constructors and static fields are new features in the X++ language.</span></span> <span data-ttu-id="6850f-146">静的コンストラクターは、静的またはインスタンス呼び出しがクラスに対して行われる前に実行されることが保証されます。</span><span class="sxs-lookup"><span data-stu-id="6850f-146">Static constructors are guaranteed to run before any static or instance calls are made to the class.</span></span> <span data-ttu-id="6850f-147">C\# では、静的の概念が実行中のアプリケーション ドメイン全体に関係します。</span><span class="sxs-lookup"><span data-stu-id="6850f-147">In C\#, the concept of static relates to the whole executing application domain.</span></span> <span data-ttu-id="6850f-148">静的コンストラクターの実行は、ユーザーのセッションに対して相対的です。</span><span class="sxs-lookup"><span data-stu-id="6850f-148">The execution of the static constructor is relative to the user’s session.</span></span> <span data-ttu-id="6850f-149">静的コンストラクターには、次のプロファイルがあります。</span><span class="sxs-lookup"><span data-stu-id="6850f-149">The static constructor has the following profile.</span></span>

    static void TypeNew() 

<span data-ttu-id="6850f-150">静的コンストラクターを明示的に呼び出すことはありません。コンパイラは、クラスの他のメソッドに先立って、静的コンストラクターを 1 回だけ確実に呼び出すコードを生成します。</span><span class="sxs-lookup"><span data-stu-id="6850f-150">You’ll never call the static constructor explicitly; the compiler will generate code to ensure that the constructor is called exactly once prior to any other method on the class.</span></span> <span data-ttu-id="6850f-151">静的コンストラクターは、任意の静的データを初期化したり、一度だけ実行する必要のある特定のアクションを実行するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="6850f-151">A static constructor is used to initialize any static data, or to perform a particular action that needs to be performed only once.</span></span> <span data-ttu-id="6850f-152">静的コンストラクターに指定できるパラメーターはなく、静的としてマークする必要があります。</span><span class="sxs-lookup"><span data-stu-id="6850f-152">No parameters can be provided for the static constructor, and it must be marked as static.</span></span> <span data-ttu-id="6850f-153">静的フィールドは静的キーワードを使用して宣言されているフィールドです。</span><span class="sxs-lookup"><span data-stu-id="6850f-153">Static fields are fields that are declared using the static keyword.</span></span> <span data-ttu-id="6850f-154">概念的には、クラスのインスタンスではなくクラスに適用されます。</span><span class="sxs-lookup"><span data-stu-id="6850f-154">Conceptually they apply to the class, not instances of the class.</span></span>

### <a name="example"></a><span data-ttu-id="6850f-155">例</span><span class="sxs-lookup"><span data-stu-id="6850f-155">Example</span></span>

<span data-ttu-id="6850f-156">下の例ではインスタンスと呼ばれる単一を、静的コンストラクターを使用して作成する方法を説明します。</span><span class="sxs-lookup"><span data-stu-id="6850f-156">We'll show how a singleton, called instance in the example below, can be created by using the static constructor.</span></span>

    public class Singleton
    {
      private static Singleton instance;

      private void new()
      {
      }

      static void TypeNew()
      {
        instance = new Singleton();
      }

      public static Singleton Instance()
      {
        return Singleton::instance;
      }
    }

<span data-ttu-id="6850f-157">単一は、クラスのインスタンスが 1 つしか呼び出されないことを保証します。これは、以下で消費されます。</span><span class="sxs-lookup"><span data-stu-id="6850f-157">The singleton will guarantee that only one instance of the class will ever be called, which is consumed by the following.</span></span>

    {
        …
        Singleton i = Singleton::Instance();
      }

## <a name="assignment-of-field-members-inline"></a><span data-ttu-id="6850f-158">フィールド メンバー インラインの割り当て</span><span class="sxs-lookup"><span data-stu-id="6850f-158">Assignment of field members inline</span></span>
<span data-ttu-id="6850f-159">フィールド自体の宣言などと共に、フィールド インラインに値を代入できるようになりました。</span><span class="sxs-lookup"><span data-stu-id="6850f-159">It's now possible to assign a value to a field inline, i.e. along with the declaration of the field itself.</span></span> <span data-ttu-id="6850f-160">これは、静的フィールドとインスタンス フィールドの両方に適用されます。</span><span class="sxs-lookup"><span data-stu-id="6850f-160">This applies to both static and instance fields.</span></span> <span data-ttu-id="6850f-161">次のコードでは、field1 と field2 の値はこの方法で定義されます。</span><span class="sxs-lookup"><span data-stu-id="6850f-161">In the following code, the values of field1 and field2 are defined in this fashion.</span></span>

    public class MyClass2
    {
      int field1 = 1;
      str field2 = "Banana";

      void new()
      {
        // …
      }
    }

<span data-ttu-id="6850f-162">上記のコードは、以下と同じ意味を持ちます。</span><span class="sxs-lookup"><span data-stu-id="6850f-162">The code above has the same semantic meaning as:</span></span>  

    public class MyClass2
    {
      int field1;
      str field2;

      void new()
      {
        this.field1 = 1;
        this.field2 = "Banana";
        // …
      }
    }

<span data-ttu-id="6850f-163">インライン割り当ては、静的メンバーとインスタンス メンバーの両方で機能します。</span><span class="sxs-lookup"><span data-stu-id="6850f-163">The inline assignments work for both static and instance members.</span></span>

## <a name="constsreadonly"></a><span data-ttu-id="6850f-164">Consts/読み取り専用</span><span class="sxs-lookup"><span data-stu-id="6850f-164">Consts/Readonly</span></span>
<span data-ttu-id="6850f-165">マクロの概念は、引き続き X++ で完全にサポートされています。</span><span class="sxs-lookup"><span data-stu-id="6850f-165">The concept of macros continues to be fully supported in X++.</span></span> <span data-ttu-id="6850f-166">ただし、\#定義の代わりに定数を使用することには、多くのメリットがあります。</span><span class="sxs-lookup"><span data-stu-id="6850f-166">However, using constants instead of \#defines has a number of benefits.</span></span>

-   <span data-ttu-id="6850f-167">ドキュメント コメントは定数に対して追加することができますが、マクロの値に対して追加することはできません。</span><span class="sxs-lookup"><span data-stu-id="6850f-167">You can add a documentation comment to the const, not to the value of the macro.</span></span> <span data-ttu-id="6850f-168">最終的に、言語サービスによってこれが選択され、ユーザーに適切な情報が提供されます。</span><span class="sxs-lookup"><span data-stu-id="6850f-168">Ultimately, the language service will pick this up and provide good information to the user.</span></span>
-   <span data-ttu-id="6850f-169">定数は、IntelliSense で知られています。</span><span class="sxs-lookup"><span data-stu-id="6850f-169">The const is known by IntelliSense.</span></span>
-   <span data-ttu-id="6850f-170">定数は相互参照されるので、特定の定数のすべての参照を見つけることができます。</span><span class="sxs-lookup"><span data-stu-id="6850f-170">The const is cross referenced, so you can find all references of a particular constant.</span></span> <span data-ttu-id="6850f-171">これは、マクロのケースではありません。</span><span class="sxs-lookup"><span data-stu-id="6850f-171">This is not the case for a macro.</span></span>
-   <span data-ttu-id="6850f-172">定数は、プライベート、プロテクト、またはパブリックのいずれかのアクセス修飾子となります。</span><span class="sxs-lookup"><span data-stu-id="6850f-172">The const is subject to access modifiers, either private, protected, or public.</span></span> <span data-ttu-id="6850f-173">マクロのアクセシビリティが十分に理解されていないか、厳密に定義されていません。</span><span class="sxs-lookup"><span data-stu-id="6850f-173">The accessibility of macros is not well understood or even rigorously defined.</span></span>
-   <span data-ttu-id="6850f-174">Consts にはスコープがありますが、マクロにはスコープはありません。</span><span class="sxs-lookup"><span data-stu-id="6850f-174">Consts have scope, while macros do not.</span></span>
-   <span data-ttu-id="6850f-175">デバッガーには定数の値および読み取り専用変数を表示することができます。</span><span class="sxs-lookup"><span data-stu-id="6850f-175">You can see the value of consts and readonly variables in the debugger.</span></span>

<span data-ttu-id="6850f-176">クラス スコープ (クラスの宣言) で定義されているマクロは、すべての派生クラスのすべてのメソッドで効率的に使用できます。</span><span class="sxs-lookup"><span data-stu-id="6850f-176">Macros that are defined in class scopes (in class declarations) are effectively available in all methods of all derived classes.</span></span> <span data-ttu-id="6850f-177">これはもともとレガシーなコンパイラ マクロ実装のバグでしたが、この抜け穴はアプリケーション プログラマがよく利用しています。</span><span class="sxs-lookup"><span data-stu-id="6850f-177">This was originally a bug in the legacy compiler macro implementation, but this loophole is now massively exploited by application programmers.</span></span> <span data-ttu-id="6850f-178">新しい X++ コンパイラには、この機能が残されていますが、この機能を使用する新しいコードは記述しないでください。</span><span class="sxs-lookup"><span data-stu-id="6850f-178">The new X++ compiler still honors this, but no new code that uses this should be written.</span></span> <span data-ttu-id="6850f-179">この特定の機能は、コンパイラのパフォーマンスにも大きく影響を与えます。</span><span class="sxs-lookup"><span data-stu-id="6850f-179">This particular feature also considerably impacts compiler performance.</span></span> <span data-ttu-id="6850f-180">定数は、下記のようにクラス レベルで宣言できます。</span><span class="sxs-lookup"><span data-stu-id="6850f-180">Constants can be declared at the class level as suggested below.</span></span>

    private const str MyConstant = 'SomeValue';

<span data-ttu-id="6850f-181">次に、定数を二重コロン構文を使用して参照することができます。</span><span class="sxs-lookup"><span data-stu-id="6850f-181">The constants can then be referenced by using the double-colon syntax.</span></span>

      str value = MyClass::MyConstant;

<span data-ttu-id="6850f-182">定数が定義されているクラスのスコープにいる場合は、型名の接頭語 (上記の例では MyClass) を省略できます。</span><span class="sxs-lookup"><span data-stu-id="6850f-182">If you're in the scope of the class where the const is defined, you can omit the type name prefix (MyClass in the example above).</span></span> <span data-ttu-id="6850f-183">このようにマクロ ライブラリの概念を簡単に実装することができます。</span><span class="sxs-lookup"><span data-stu-id="6850f-183">You can easily implement the concept of a macro library this way.</span></span> <span data-ttu-id="6850f-184">マクロ シンボルのリストは、パブリック const の定義を持つクラスになります。</span><span class="sxs-lookup"><span data-stu-id="6850f-184">The list of macro symbols becomes a class with public const definitions.</span></span>

### <a name="exercise"></a><span data-ttu-id="6850f-185">練習</span><span class="sxs-lookup"><span data-stu-id="6850f-185">Exercise</span></span>

<span data-ttu-id="6850f-186">フリート アプリケーションには、以下のマクロ定義を含む FMDataHelper クラスが含まれています。</span><span class="sxs-lookup"><span data-stu-id="6850f-186">The fleet application contains the FMDataHelper class that contains the following macro definitions.</span></span>

    public class FMDataHelper
    {
      #define.FMSvcTechUserId('FMSvcTec')
      #define.FMClerkUserId('FMClerk')
      #define.FMManagerUserId('FMMgr')
      #define.FMSvcTechUserGrpId('FMSvcTech')
      #define.FMClerkUserGrpId('FMClerk')
      #define.FMManagerUserGrpId('FMManager')
    …
    }

<span data-ttu-id="6850f-187">これらを定数定義に変更し、それに従ってマクロが使用される場所を更新します。</span><span class="sxs-lookup"><span data-stu-id="6850f-187">Change these to const definitions and update the places where the macros are used accordingly.</span></span>

<span data-ttu-id="6850f-188">また、定数を変数のみとして定義することもできます。</span><span class="sxs-lookup"><span data-stu-id="6850f-188">You can also define consts solely as variables.</span></span> <span data-ttu-id="6850f-189">コンパイラはインバリアントを維持して、値を変更できないようにします。</span><span class="sxs-lookup"><span data-stu-id="6850f-189">The compiler will maintain the invariant that the value can't be modified.</span></span>

    {
      const int Blue = 0x0000FF;
      const int Green = 0x00FF00;
      const int Red = 0xFF0000;
    }

<span data-ttu-id="6850f-190">読み取り専用フィールドには値を 1 回だけ割り当てることがき、その値は変わりません。フィールドには、インラインで (フィールドが宣言した場所)、またはコンストラクターで値を割り当てることができます。</span><span class="sxs-lookup"><span data-stu-id="6850f-190">Read-only fields can only be assigned a value once, and that value never changes; the field can be assigned its value either inline, at the place where the field is declared, or in the constructor.</span></span> <span data-ttu-id="6850f-191">現時点では、定数と読み取り専用の唯一の違いです。</span><span class="sxs-lookup"><span data-stu-id="6850f-191">Currently, that's the only difference between const and read-only.</span></span>

<a name="var"></a><span data-ttu-id="6850f-192">Var</span><span class="sxs-lookup"><span data-stu-id="6850f-192">Var</span></span>
---

<span data-ttu-id="6850f-193">コンパイラが初期化式から種類を判断することができる場合は、変数の種類を明示的に提供せずに変数を宣言することができるようになりました。</span><span class="sxs-lookup"><span data-stu-id="6850f-193">You can now declare a variable without explicitly providing the type of the variable, if the compiler can determine the type from the initialization expression.</span></span> <span data-ttu-id="6850f-194">変数が、まだ厳密に型指定されている明確な型であることに注意してください。</span><span class="sxs-lookup"><span data-stu-id="6850f-194">Note that the variable is still strongly-typed into one, unambiguous type.</span></span> <span data-ttu-id="6850f-195">(コンパイラが型を推定する) 初期化式が用意されている宣言でのみ var を使用することができます。</span><span class="sxs-lookup"><span data-stu-id="6850f-195">It's only possible to use var on declarations where initialization expressions are provided (from which the compiler will infer the type).</span></span> <span data-ttu-id="6850f-196">コードを読みやすくできる状況がありますが、この機能を誤用すべきではありません。</span><span class="sxs-lookup"><span data-stu-id="6850f-196">There are situations where this can make code easier to read, but this feature shouldn't be misused.</span></span> <span data-ttu-id="6850f-197">次のルールを考慮してください。</span><span class="sxs-lookup"><span data-stu-id="6850f-197">You should consider the following rules:</span></span>

-   <span data-ttu-id="6850f-198">代入の右側から見て変数の型が明らかである場合、または正確な型が重要でない場合は、var を使用してローカル変数を宣言します。</span><span class="sxs-lookup"><span data-stu-id="6850f-198">Use var to declare local variables when the type of the variable is obvious from the right side of the assignment, or when the precise type is not important.</span></span>


~~~
    // When the type of a variable is clear from the context, use var 
    // in the declaration. 
    var var1 = "This is clearly a string.";
    var var2 = 27; // This is an integer (not a real).
    var i = System.Convert::ToInt32(3.4);
~~~

-   <span data-ttu-id="6850f-199">種類が初期化式から明らかでない場合は、var を使用しないでください。</span><span class="sxs-lookup"><span data-stu-id="6850f-199">Don't use var when the type isn't apparent from the initialization expression.</span></span>

        // When the type of a variable is not clear from the context, use an 
        // explicit type. 
            int var4 = myObject.ResultSoFar();

-   <span data-ttu-id="6850f-200">for ループ カウンターの宣言には、var を使用します。</span><span class="sxs-lookup"><span data-stu-id="6850f-200">Use var for the declarations of for loop counters.</span></span>
-   <span data-ttu-id="6850f-201">using 文内で破棄可能なオブジェクトには、var を使用します。</span><span class="sxs-lookup"><span data-stu-id="6850f-201">Use var for disposable objects inside using statements.</span></span>

## <a name="private-and-protected-member-variables"></a><span data-ttu-id="6850f-202">プライベートおよび保護されたメンバー変数</span><span class="sxs-lookup"><span data-stu-id="6850f-202">Private and protected member variables</span></span>
<span data-ttu-id="6850f-203">以前は、クラスで定義されたすべてのメンバー変数が可変保護されていました。</span><span class="sxs-lookup"><span data-stu-id="6850f-203">Previously, all member variables defined in a class were invariably protected.</span></span> <span data-ttu-id="6850f-204">private、protected、および public キーワードを加えることにより、メンバー変数の表示を明示的にできるようになりました。</span><span class="sxs-lookup"><span data-stu-id="6850f-204">It's now possible to make the visibility of member variables explicit by adding the private, protected, and public keywords.</span></span> <span data-ttu-id="6850f-205">これらの修飾子の解釈は明白であり、メソッドのセマンティクスに沿っています。</span><span class="sxs-lookup"><span data-stu-id="6850f-205">The interpretation of these modifiers is obvious and aligns with the semantics for methods:</span></span>

-   <span data-ttu-id="6850f-206">プライベート メンバーは、定義されているクラス内でのみ使用できます。</span><span class="sxs-lookup"><span data-stu-id="6850f-206">A private member can only be used within the class where it's defined.</span></span>
-   <span data-ttu-id="6850f-207">保護されているメンバーは、それが定義されているクラスとそのすべてのサブクラスで使用できます。</span><span class="sxs-lookup"><span data-stu-id="6850f-207">a protected member can be used in the class where it's defined, and all subclasses thereof.</span></span>
-   <span data-ttu-id="6850f-208">パブリック メンバーは、どこででも使用することができ、定義されているクラス階層の範囲外に表示されます。</span><span class="sxs-lookup"><span data-stu-id="6850f-208">A public member can be used anywhere: it's visible outside the confines of the class hierarchy in which it's defined.</span></span>

<span data-ttu-id="6850f-209">明示的なモディファイアーで実装されていないメンバー変数の既定値は、引き続き保護されています。</span><span class="sxs-lookup"><span data-stu-id="6850f-209">The default for member variables that aren't adorned with an explicit modifier is still protected.</span></span> <span data-ttu-id="6850f-210">可視性を明示的に指定する習慣をつける必要があります。</span><span class="sxs-lookup"><span data-stu-id="6850f-210">You should make it a habit of explicitly specifying the visibility.</span></span> <span data-ttu-id="6850f-211">説明のように、メンバー 変数が public として定義されている場合、定義されているクラス外で消費される可能性があります。</span><span class="sxs-lookup"><span data-stu-id="6850f-211">As described, when a member variable is defined as public, it may be consumed outside of the class in which it's defined.</span></span> <span data-ttu-id="6850f-212">この場合、変数をホストしているオブジェクトを指定する修飾子は、(メソッド呼び出しの場合と同様に) ドット表記を使用して指定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="6850f-212">In this case, a qualifier designating the object hosting the variable has to be specified, using the dot notation (as is the case for method calls).</span></span> <span data-ttu-id="6850f-213">上記のコードを再利用:</span><span class="sxs-lookup"><span data-stu-id="6850f-213">Reusing the code from above:</span></span>

    public class MyClass2
    {
      int field1;
      str field2;

      void new()
      {
        this.field1 = 1;   // Explicit object designated
        field2 = "Banana";  // 'this' assumed, as usual
      }
    }

<span data-ttu-id="6850f-214">この場合、field1 には明示的な 'this' を使用してアクセスします。</span><span class="sxs-lookup"><span data-stu-id="6850f-214">In this case, field1 is accessed using the explicit 'this.'</span></span> <span data-ttu-id="6850f-215">修飾子。</span><span class="sxs-lookup"><span data-stu-id="6850f-215">qualifier.</span></span> <span data-ttu-id="6850f-216">**注記**: 消費者にクラスの内部作業を公開することになり、クラスの実装と消費者の間に強い依存関係が生じるため、メンバー変数をパブリックにすることはお勧めできません。</span><span class="sxs-lookup"><span data-stu-id="6850f-216">**Note**: Making a member variable public may not be a good idea since it exposes the internal workings of the class to its consumers, creating a strong dependency between the class implementation and its consumers.</span></span> <span data-ttu-id="6850f-217">常に、実装ではなくコントラクトにのみ依存させる必要があります。</span><span class="sxs-lookup"><span data-stu-id="6850f-217">You should always strive to only depend on a contract, not an implementation.</span></span>

## <a name="finally-in-trycatch-statements"></a><span data-ttu-id="6850f-218">最後に try/catch 明細書において</span><span class="sxs-lookup"><span data-stu-id="6850f-218">Finally in try/catch statements</span></span>
<span data-ttu-id="6850f-219">try/catch 文にオプションの finally 句を追加できるようになりました。</span><span class="sxs-lookup"><span data-stu-id="6850f-219">Try/catch statements can now include an optional finally clause.</span></span> <span data-ttu-id="6850f-220">セマンティクスは C\# やその他のマネージド言語と同じです。</span><span class="sxs-lookup"><span data-stu-id="6850f-220">The semantics are the same as they are in C\# and other managed languages.</span></span> <span data-ttu-id="6850f-221">finally 句のステートメントは、通常または例外を介してコントロールが try ブロックを離れるときに実行されます。</span><span class="sxs-lookup"><span data-stu-id="6850f-221">The statements in the finally clause are executed when control leaves the try block, either normally or through an exception.</span></span>

      try
      {
        // ...
      }
      catch
      {
        // Executes when any exception is thrown in the dynamic
        // scope in the try block.
      }
      finally
      {
        // Executed irrespective of how the try block exits.
      }

## <a name="event-handlers-and-prepost-methods"></a><span data-ttu-id="6850f-222">イベント ハンドラーおよび予備または転記メソッド</span><span class="sxs-lookup"><span data-stu-id="6850f-222">Event handlers and Pre/Post methods</span></span>
<span data-ttu-id="6850f-223">旧式 X++ では、特定のメソッドがメソッドの実行前後に実行されるようにメタデータで指定できました。</span><span class="sxs-lookup"><span data-stu-id="6850f-223">In legacy X++, it was possible to prescribe in metadata that certain methods were to be executed prior to and after the execution of a method.</span></span> <span data-ttu-id="6850f-224">サブスクリプションが何を呼び出すかに関する情報は、パブリッシャーに記録されていますが、これは環境には役立ちません。</span><span class="sxs-lookup"><span data-stu-id="6850f-224">The information about what subscribes call was recorded on the publisher, which isn't useful in the environment.</span></span> <span data-ttu-id="6850f-225">サブスクライバーに SubscribesTo 属性を指定することにより、コードを通じて前後のハンドラーを指定できるようになりました。</span><span class="sxs-lookup"><span data-stu-id="6850f-225">It's now possible to provide Pre and Post handlers through code, by providing the SubscribesTo attribute on the subscribers.</span></span>

### <a name="example"></a><span data-ttu-id="6850f-226">例</span><span class="sxs-lookup"><span data-stu-id="6850f-226">Example</span></span>

    [PreHandlerFor(classStr(MyClass2), methodstr(MyClass2, publisher))]
      public static void PreHandler(XppPrePostArgs arguments)
      {
        int arg = arguments.getArg("i");
      }

      [PostHandlerFor(classStr(MyClass2), methodstr(MyClass2, publisher))]
      public static void PostHandler(XppPrePostArgs arguments)
      {
        int arg = arguments.getArg("i");
        int retvalFromMethod = arguments.getReturnValue();
      }

      public int Publisher(int i)
      {
        return 1;
      }

<span data-ttu-id="6850f-227">この例は、Publisher という公開メソッドを示しています。</span><span class="sxs-lookup"><span data-stu-id="6850f-227">This example shows a publishing method called Publisher.</span></span> <span data-ttu-id="6850f-228">2 人のサブスクライバーが PreHandlerFor と PostHandlerFor に登録されています。</span><span class="sxs-lookup"><span data-stu-id="6850f-228">Two subscribers are enlisted with the PreHandlerFor and PostHandlerFor.</span></span> <span data-ttu-id="6850f-229">このコードは、変数と戻り値にアクセスする方法を示しています。</span><span class="sxs-lookup"><span data-stu-id="6850f-229">The code shows how to access the variables, and the return values.</span></span> <span data-ttu-id="6850f-230">**注記**: アプリケーション コードに重要なアプリケーション イベントを公開するための多数の委任がないため、この機能は下位互換性のために提供されています。</span><span class="sxs-lookup"><span data-stu-id="6850f-230">**Note**: This feature is provided for backward compatibility and, because the application code doesn't have many delegates, to publish important application events.</span></span> <span data-ttu-id="6850f-231">前後のハンドラーは、パラメーターの追加または変更のため、パラメータータイプの変更ため、メソッドが呼び出されなくなったり、別の状況で呼び出されたりしたために容易に中断する可能があります。</span><span class="sxs-lookup"><span data-stu-id="6850f-231">Pre and Post handlers can easily break as the result of added or removed parameters, changed parameter types, or because methods are no longer called, or called under different circumstances.</span></span> <span data-ttu-id="6850f-232">属性はバインディング イベント ハンドラーをデリゲートするためにも使用されます。</span><span class="sxs-lookup"><span data-stu-id="6850f-232">Attributes are also used for binding event handlers to delegates:</span></span>

      [SubscribesTo(
        classstr(FMRentalCheckoutProcessor),  
        delegatestr(FMRentalCheckoutProcessor, RentalTransactionAboutTobeFinalizedEvent))]
      public static void RentalFinalizedEventHandler(
        FMRental rentalrecord, Struct rentalConfirmation)
      {
      }

      delegate void RentalTransactionAboutTobeFinalizedEvent(
        FMRental fmrentalrecord, struct RentalConfirmation)
      {
      }

<span data-ttu-id="6850f-233">この場合、SubscribesTo 属性は、FmRentalCheckoutProcessor.RentalTransactionAboutToBeFinalizedEvent デリゲートが呼び出されたときにメソッド RentalFinalizedEventHandler を呼び出す必要があることを指定します。</span><span class="sxs-lookup"><span data-stu-id="6850f-233">In this case, the SubscribesTo attribute specifies that the method RentalFinalizedEventHandler should be called when the FmRentalCheckoutProcessor.RentalTransactionAboutToBeFinalizedEvent delegate is called.</span></span> <span data-ttu-id="6850f-234">パブリッシャーとサブスクライバーの間のバインディングは属性を通じて行われるため、サブスクライバーが呼び出される順序を指定する方法はありません。</span><span class="sxs-lookup"><span data-stu-id="6850f-234">Since the binding between the publisher and subscribers is done through attributes, there's no way of specifying the sequence in which subscribers are called.</span></span>

## <a name="extension-methods"></a><span data-ttu-id="6850f-235">拡張メソッド</span><span class="sxs-lookup"><span data-stu-id="6850f-235">Extension methods</span></span>
<span data-ttu-id="6850f-236">拡張メソッド機能を使用すると、メソッドを別の拡張クラスに記述することによって、拡張メソッドを対象クラスに追加できます。</span><span class="sxs-lookup"><span data-stu-id="6850f-236">The extension method feature lets you add extension methods to a target class by writing the methods in a separate extension class.</span></span> <span data-ttu-id="6850f-237">次のルールが適用されます。</span><span class="sxs-lookup"><span data-stu-id="6850f-237">The following rules apply:</span></span>

-   <span data-ttu-id="6850f-238">拡張クラスは静的でなければなりません。</span><span class="sxs-lookup"><span data-stu-id="6850f-238">The extension class must be static.</span></span>
-   <span data-ttu-id="6850f-239">拡張クラスの名前は、10 文字の接尾語 \_Extension で終了する必要があります。</span><span class="sxs-lookup"><span data-stu-id="6850f-239">The name of the extension class must end with the ten-character suffix \_Extension.</span></span> <span data-ttu-id="6850f-240">ただし、接尾辞に先行する名前の部分には制限はありません。</span><span class="sxs-lookup"><span data-stu-id="6850f-240">However, there's no restriction on the part of the name that precedes the suffix.</span></span>
-   <span data-ttu-id="6850f-241">拡張子クラス内のすべての拡張子メソッドは、パブリック静的として宣言する必要があります。</span><span class="sxs-lookup"><span data-stu-id="6850f-241">Every extension method in the extension class must be declared as public static.</span></span>
-   <span data-ttu-id="6850f-242">すべての拡張メソッドの最初のパラメーターは、拡張メソッドが拡張する型です。</span><span class="sxs-lookup"><span data-stu-id="6850f-242">The first parameter in every extension method is the type that the extension method extends.</span></span> <span data-ttu-id="6850f-243">ただし、拡張メソッドが呼び出されると、呼び出し元は最初のパラメーターに対して何も渡す必要がありません。</span><span class="sxs-lookup"><span data-stu-id="6850f-243">However, when the extension method is called, the caller must not pass in anything for the first parameter.</span></span> <span data-ttu-id="6850f-244">代わりに、システムが最初のパラメーターに必要なオブジェクトを自動的に渡します。</span><span class="sxs-lookup"><span data-stu-id="6850f-244">Instead, the system automatically passes in the required object for the first parameter.</span></span>

<span data-ttu-id="6850f-245">拡張クラスにプライベートまたは保護された静的メソッドを含めることは完全に有効です。</span><span class="sxs-lookup"><span data-stu-id="6850f-245">It's perfectly valid to have private or protected static methods in an extension class.</span></span> <span data-ttu-id="6850f-246">これらは通常、実装の詳細に使用され、拡張として公開されません。</span><span class="sxs-lookup"><span data-stu-id="6850f-246">These are typically used for implementation details and are not exposed as extensions.</span></span> <span data-ttu-id="6850f-247">次の例は、いくつかの拡張メソッドを保持している拡張機能クラスを示しています。</span><span class="sxs-lookup"><span data-stu-id="6850f-247">The example below illustrates an extension class holding a few extension methods:</span></span>

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

### <a name="why-use-extension-methods"></a><span data-ttu-id="6850f-248">なぜ拡張メソッドを使用しますか。</span><span class="sxs-lookup"><span data-stu-id="6850f-248">Why use extension methods?</span></span>

<span data-ttu-id="6850f-249">拡張メソッドの手法は、拡張するクラスのソース コードには影響しません。</span><span class="sxs-lookup"><span data-stu-id="6850f-249">The extension method technique doesn't affect the source code of the class it extends.</span></span> <span data-ttu-id="6850f-250">したがって、クラスへの追加はオーバーレイなしで行うことができます。</span><span class="sxs-lookup"><span data-stu-id="6850f-250">Therefore, the addition to the class can be done without over-layering.</span></span> <span data-ttu-id="6850f-251">ターゲット クラスへのアップグレードは、既存の拡張メソッドの影響を受けることはありません。</span><span class="sxs-lookup"><span data-stu-id="6850f-251">Upgrades to the target class are never affected by any existing extension methods.</span></span> <span data-ttu-id="6850f-252">ただし、ターゲット クラスへのアップグレードで拡張メソッドとして同じ名前のメソッドが追加される場合、拡張メソッドはターゲット クラスのオブジェクトを通して到達できなくなります。</span><span class="sxs-lookup"><span data-stu-id="6850f-252">However, if an upgrade to the target class adds a method that has the same name as your extension method, your extension method becomes unreachable through objects of the target class.</span></span> <span data-ttu-id="6850f-253">拡張メソッドは使いやすいです。</span><span class="sxs-lookup"><span data-stu-id="6850f-253">Extension methods are easy to use.</span></span> <span data-ttu-id="6850f-254">拡張メソッドの手法では、通常のインスタンス メソッドを呼び出すときによく使うドット区切り構文と同じものを使用します。</span><span class="sxs-lookup"><span data-stu-id="6850f-254">The extension method technique uses the same dot-delimited syntax that you routinely use the call regular instance methods.</span></span> <span data-ttu-id="6850f-255">拡張メソッドは、ターゲット クラスのすべてのパブリック コンポーネントにアクセスできますが、保護されたまたはプライベートのオブジェクトにはアクセスできません。</span><span class="sxs-lookup"><span data-stu-id="6850f-255">Extension methods can access all public artifacts of the target class, but they can't access things that are protected or private.</span></span> <span data-ttu-id="6850f-256">この方法では、拡張メソッドは糖衣構文の種類とみなすことができます。</span><span class="sxs-lookup"><span data-stu-id="6850f-256">In this way, extension methods can be seen as a kind of syntactic sugar.</span></span>

### <a name="where-can-extension-methods-be-applied"></a><span data-ttu-id="6850f-257">拡張メソッドはどこに適用できるか</span><span class="sxs-lookup"><span data-stu-id="6850f-257">Where can extension methods be applied?</span></span>

<span data-ttu-id="6850f-258">拡張メソッドのターゲットは、次のアプリケーション オブジェクト タイプのいずれかである必要があります。</span><span class="sxs-lookup"><span data-stu-id="6850f-258">The target of an extension method must be one of the following application object types:</span></span>

-   <span data-ttu-id="6850f-259">クラス</span><span class="sxs-lookup"><span data-stu-id="6850f-259">Class</span></span>
-   <span data-ttu-id="6850f-260">テーブル</span><span class="sxs-lookup"><span data-stu-id="6850f-260">Table</span></span>
-   <span data-ttu-id="6850f-261">表示</span><span class="sxs-lookup"><span data-stu-id="6850f-261">View</span></span>
-   <span data-ttu-id="6850f-262">マップ</span><span class="sxs-lookup"><span data-stu-id="6850f-262">Map</span></span>

<span data-ttu-id="6850f-263">目標タイプに関係なく、拡張機能*クラス*はタイプに拡張メソッドを追加するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="6850f-263">Regardless of the target type, an extension *class* is used to add extension methods to the type.</span></span> <span data-ttu-id="6850f-264">たとえば、拡張テーブルは、メソッドをテーブルに追加するために使用されて*いません*し、拡張テーブルというものは存在しません。</span><span class="sxs-lookup"><span data-stu-id="6850f-264">For example, an extension table is *not* used to add methods to a table, and there's no such thing as an extension table.</span></span>

## <a name="using-clauses"></a><span data-ttu-id="6850f-265">句の使用</span><span class="sxs-lookup"><span data-stu-id="6850f-265">Using clauses</span></span>
<span data-ttu-id="6850f-266">以前は、X++ で作成されなかったマネージド コンポーネントに対するすべての参照が、各タイプの名前空間を含むを完全修飾名を使用して行われていました。</span><span class="sxs-lookup"><span data-stu-id="6850f-266">Previously, all references to managed artifacts that weren't authored in X++ was done using fully qualified names, including the namespace for each type.</span></span> <span data-ttu-id="6850f-267">これはまだ可能ですが、このようなコンポーネントの使用の煩わしさを軽減をするために、句を使用できます。</span><span class="sxs-lookup"><span data-stu-id="6850f-267">This is still possible, but you can now provide using clauses to make the use of such artifacts less onerous.</span></span> <span data-ttu-id="6850f-268">using ステートメントとは対照的に、各 using 句はその句が適用されるクラスに先行します。</span><span class="sxs-lookup"><span data-stu-id="6850f-268">As opposed to a using statement, each using clause precedes the class in which the clause is applied.</span></span> <span data-ttu-id="6850f-269">完全修飾名の短縮名を導入するエイリアスを提供することもできます。</span><span class="sxs-lookup"><span data-stu-id="6850f-269">It's also possible to provide aliases that introduce a short name for a fully qualified name.</span></span> <span data-ttu-id="6850f-270">エイリアスは、以下に示すように名前空間とクラスを示すことができます。</span><span class="sxs-lookup"><span data-stu-id="6850f-270">Aliases can denote namespaces and classes as shown below.</span></span>

### <a name="example"></a><span data-ttu-id="6850f-271">例</span><span class="sxs-lookup"><span data-stu-id="6850f-271">Example</span></span>

<span data-ttu-id="6850f-272">次のコードを考慮してください。</span><span class="sxs-lookup"><span data-stu-id="6850f-272">Consider the following code:</span></span>

     using System;
    using IONS=System.IO; // Namespace alias
    using Alist=System.Collections.ArrayList; // Class alias

    public class MyClass2
    {
      public static void Main(Args a)
      {
        Int32 I; // Alternative to System.Int32
        Alist al; // Using a class alias

        al = new Alist();
        str s;

        al.Add(1);

        s = IONS.Path::ChangeExtension(@"c:\tmp\test.xml", ".txt");
      }
    }

## <a name="differences-between-legacy-x-and-new-x"></a><span data-ttu-id="6850f-273">レガシー X++ と新しい X++ の違い</span><span class="sxs-lookup"><span data-stu-id="6850f-273">Differences between legacy X++ and new X++</span></span>
<span data-ttu-id="6850f-274">このセクションでは、旧式 X++ と新しい X++ の違いを説明します。</span><span class="sxs-lookup"><span data-stu-id="6850f-274">In this section, we'll see some of the differences between legacy X++ and the new X++.</span></span>

### <a name="reals-are-decimals"></a><span data-ttu-id="6850f-275">Reals は Decimals です</span><span class="sxs-lookup"><span data-stu-id="6850f-275">Reals are Decimals</span></span>

<span data-ttu-id="6850f-276">実際の値を表すために使用されるタイプは、解釈された X++ から変更されています。</span><span class="sxs-lookup"><span data-stu-id="6850f-276">The type used to represent real values has changed from interpreted X++.</span></span> <span data-ttu-id="6850f-277">新しいタイプは、古いタイプの値をすべて表すことができるので、コードを書き直す必要はありません。</span><span class="sxs-lookup"><span data-stu-id="6850f-277">This won't require you to rewrite any code, because the new type can express all of the values that the old one could.</span></span> <span data-ttu-id="6850f-278">完全な開示のためにこの材料を提供します。</span><span class="sxs-lookup"><span data-stu-id="6850f-278">We provide this material in the interest of full disclosure only.</span></span> <span data-ttu-id="6850f-279">実数タイプのすべてのインスタンスが .NET 小数タイプ (System.Decimal) のインスタンスとして実装されます。</span><span class="sxs-lookup"><span data-stu-id="6850f-279">All instances of the real type are now implemented as instances of the .NET decimal type (System.Decimal).</span></span> <span data-ttu-id="6850f-280">以前のバージョンでの real 型と同様に、バイナリ コード化された小数点以下の型での decimal 型は浮動小数点の型とは違い、丸め誤差に対する対応力があります。</span><span class="sxs-lookup"><span data-stu-id="6850f-280">Just as the real type in previous versions, the decimal type in a binary coded decimal type that, unlike floating point type, is resilient to rounding errors.</span></span> <span data-ttu-id="6850f-281">10 進型の範囲と解像度は、元の型とは異なります。</span><span class="sxs-lookup"><span data-stu-id="6850f-281">The range and resolution of the decimal type are different from the original types.</span></span> <span data-ttu-id="6850f-282">元の X++ 実数型は 16 桁をサポートし、小数点の配置位置を指し示す指数をサポートしていました。</span><span class="sxs-lookup"><span data-stu-id="6850f-282">The original X++ real type supported 16 digits and an exponent that defined where the decimal point is placed.</span></span> <span data-ttu-id="6850f-283">新しい X++ 実数型は、正の 79,228,162,514,264,337,593,543,950,335 (2⁹⁶-1) から 負の 79,228,162,514,264,337,593,543,950,335 (-(2⁹⁶-1)) までの 10 進数を表すことができます。</span><span class="sxs-lookup"><span data-stu-id="6850f-283">The new X++ real type can represent decimal numbers ranging from positive 79,228,162,514,264,337,593,543,950,335 (2⁹⁶-1) to negative 79,228,162,514,264,337,593,543,950,335 (-(2⁹⁶-1)).</span></span> <span data-ttu-id="6850f-284">新しい実数型は、丸めの必要性を排除しません。</span><span class="sxs-lookup"><span data-stu-id="6850f-284">The new real type doesn't eliminate the need for rounding.</span></span> <span data-ttu-id="6850f-285">たとえば、次のコードは、1 ではなく 0.9999999999999999999999999999 という結果を生成します。</span><span class="sxs-lookup"><span data-stu-id="6850f-285">For example, the following code produces a result of 0.9999999999999999999999999999 instead of 1.</span></span> <span data-ttu-id="6850f-286">これは、以下の変数の値を表示するためにデバッガーを使用するとすぐに見られます。</span><span class="sxs-lookup"><span data-stu-id="6850f-286">This is readily seen when using the debugger to show the value of the variables below.</span></span>

    public class MyClass2
    {
      public static void Main(Args a)
      {
        real dividend = 1.0;
        real divisor = 3.0;
        str stringvalue;
        System.Decimal valueAsDecimal;

        real value = dividend/divisor * divisor;

        valueAsDecimal = value;
        info(valueAsDecimal.ToString("G28"));

      }
    }

<span data-ttu-id="6850f-287">1/3 の値を正確に表せる小数点以下の桁数はありません。</span><span class="sxs-lookup"><span data-stu-id="6850f-287">No number of decimals will suffice to represent the value of 1/3 accurately.</span></span> <span data-ttu-id="6850f-288">ここで得られる不一致は、有限数の小数しか提供されないことによるものです。</span><span class="sxs-lookup"><span data-stu-id="6850f-288">The discrepancy obtained here is due to the fact that only a finite number of decimals are provided.</span></span> <span data-ttu-id="6850f-289">必要な小数点以下の桁数まで丸めるには、Round 関数を使用します。</span><span class="sxs-lookup"><span data-stu-id="6850f-289">You should use the Round function to round to the number of decimals required.</span></span>

      value = round(value, 2);

## <a name="internal-representation"></a><span data-ttu-id="6850f-290">内部表示</span><span class="sxs-lookup"><span data-stu-id="6850f-290">Internal representation</span></span>
<span data-ttu-id="6850f-291">10 進数は、符号と数値の桁ごとの値が 0～9 の範囲にある数値と、流動少数点の整数部と小数部分を区切るための位置を示すスケーリング係数で構成される浮動小数点値です。</span><span class="sxs-lookup"><span data-stu-id="6850f-291">A decimal number is a floating-point value that consists of a sign, a numeric value where each digit in the value ranges from 0 to 9, and a scaling factor that indicates the position of a floating decimal point that separates the integral and fractional parts of the numeric value.</span></span> <span data-ttu-id="6850f-292">実数値のバイナリ表現は、96ビットの整数を除算し、それが小数部分であることを指定するために使用する 1 ビットの符号、96ビットの整数、スケーリング係数で構成されます。</span><span class="sxs-lookup"><span data-stu-id="6850f-292">The binary representation of a real value consists of a 1-bit sign, a 96-bit integer number, and a scaling factor used to divide the 96-bit integer and specify what portion of it is a decimal fraction.</span></span> <span data-ttu-id="6850f-293">拡大縮小係数は、0 から 28 の範囲の指数に暗黙的に 10 を引いたものです。</span><span class="sxs-lookup"><span data-stu-id="6850f-293">The scaling factor is implicitly the number 10, raised to an exponent ranging from 0 to 28.</span></span> <span data-ttu-id="6850f-294">したがって、10 進数のバイナリ表現は ((-2⁹⁶ ～ 2⁹⁶)/10(0\\ ～\\ 28)) を表します。ここで -(2⁹⁶-1) は表現できる最小値と等しく、2⁹⁶-1 は最大値に等しくなります。</span><span class="sxs-lookup"><span data-stu-id="6850f-294">Therefore, the binary representation of a decimal value represents ((-2⁹⁶ to 2⁹⁶)/10(0\\ to\\ 28)), where -(2⁹⁶-1) is equal to the minimum value and 2⁹⁶-1 is equal to the maximum value that can be expressed.</span></span>

## <a name="string-truncation"></a><span data-ttu-id="6850f-295">文字列の切り捨て</span><span class="sxs-lookup"><span data-stu-id="6850f-295">String truncation</span></span>
<span data-ttu-id="6850f-296">文字列の切り捨ては、新しい機能ではありません。</span><span class="sxs-lookup"><span data-stu-id="6850f-296">String truncation is not a new feature.</span></span> <span data-ttu-id="6850f-297">ただし、コードが以前のバージョンの IL で実行されると、ここで説明されている自動文字列の切り捨ては行われません。</span><span class="sxs-lookup"><span data-stu-id="6850f-297">However, when code is executed in IL in previous versions, the automatic string truncation described here doesn’t take place.</span></span> <span data-ttu-id="6850f-298">文字列値は、最大文字数を格納するために X++ で宣言できます。</span><span class="sxs-lookup"><span data-stu-id="6850f-298">String values can be declared in X++ to contain a maximum number of characters.</span></span> <span data-ttu-id="6850f-299">これは通常、以下に示すように、この情報を拡張データ型でエンコードすることによって実現されます。クレジット カード番号は 20 文字を超えることはできません。</span><span class="sxs-lookup"><span data-stu-id="6850f-299">Typically, this is achieved by encoding this information in an extended data type, as shown below: Credit card numbers cannot exceed 20 characters.</span></span> <span data-ttu-id="6850f-300">[![StringTruncationSolutionExplorer\_DebugFeatures](./media/stringtruncationsolutionexplorer_debugfeatures.png)](./media/stringtruncationsolutionexplorer_debugfeatures.png) 長さ制約を X++ 構文で直接指定することもできます。</span><span class="sxs-lookup"><span data-stu-id="6850f-300">[![StringTruncationSolutionExplorer\_DebugFeatures](./media/stringtruncationsolutionexplorer_debugfeatures.png)](./media/stringtruncationsolutionexplorer_debugfeatures.png) It's also possible to specify length constraints directly in the X++ syntax:</span></span>

    str 20 creditCardNumber;

<span data-ttu-id="6850f-301">これらの値に対するすべての割り当ては最大長に暗黙的に切り捨てられます。</span><span class="sxs-lookup"><span data-stu-id="6850f-301">All assignments to these values are implicitly truncated to this maximum length.</span></span>

### <a name="exercise"></a><span data-ttu-id="6850f-302">練習</span><span class="sxs-lookup"><span data-stu-id="6850f-302">Exercise</span></span>

<span data-ttu-id="6850f-303">静的メイン メソッドに含めることにより、デバッガーで次のコードを実行します。</span><span class="sxs-lookup"><span data-stu-id="6850f-303">Run the following code in the debugger by including it in a static main method:</span></span>

    creditCardNumber = "12345678901234567890Excess string";

## <a name="casting"></a><span data-ttu-id="6850f-304">キャスティング</span><span class="sxs-lookup"><span data-stu-id="6850f-304">Casting</span></span>
<span data-ttu-id="6850f-305">X++ の以前のバージョンは、型キャストの処理で、非常に少ない制限でした。</span><span class="sxs-lookup"><span data-stu-id="6850f-305">The previous version of X++ was very permissive in its treatment of type casting.</span></span> <span data-ttu-id="6850f-306">アップキャストとダウンキャストの両方が、プログラマの介在なしに許可されています。</span><span class="sxs-lookup"><span data-stu-id="6850f-306">Both up-casting and down-casting were allowed without intervention from the programmer.</span></span> <span data-ttu-id="6850f-307">レガシ X++ で許可されるキャストの一部は、.NET ランタイム環境の範囲に実装することはできません。</span><span class="sxs-lookup"><span data-stu-id="6850f-307">Some of the casting permitted in legacy X++ can’t be implemented in the confines of the .NET runtime environment.</span></span> <span data-ttu-id="6850f-308">X++ を含む、オブジェクト指向のプログラミング言語では、キャストは宣言された型が両方同じ継承チェーンにある変数間の代入を表します。</span><span class="sxs-lookup"><span data-stu-id="6850f-308">In object oriented programming languages, including X++, casting refers to assignments between variables whose declared types are both in the same inheritance chain.</span></span> <span data-ttu-id="6850f-309">キャストはダウン キャストまたはアップ キャストのいずれかです。</span><span class="sxs-lookup"><span data-stu-id="6850f-309">A cast is either a down-cast or an up-cast.</span></span> <span data-ttu-id="6850f-310">この説明の準備として、いくつかのわかりやすいクラス階層、[![Casting\_DebugFeatures](./media/casting_debugfeatures.png)](./media/casting_debugfeatures.png) を紹介します。ご覧のとおり、MotorVehicle クラスは Animal クラスとは関係ありません。</span><span class="sxs-lookup"><span data-stu-id="6850f-310">To set the stage for this discussion, we introduce a few self-explanatory class hierarchies: [![Casting\_DebugFeatures](./media/casting_debugfeatures.png)](./media/casting_debugfeatures.png) As you can see, the MotorVehicle class isn't related to the Animal class.</span></span> <span data-ttu-id="6850f-311">**up-cast** は派生型の式を基本型に割り当てる場合に発生します。</span><span class="sxs-lookup"><span data-stu-id="6850f-311">An **up-cast** happens when assigning an expression of a derived type to a base type:</span></span>

      Animal a = new Horse();

<span data-ttu-id="6850f-312">**down-cast**は、基本型の式を派生変数に代入する場合に発生します。</span><span class="sxs-lookup"><span data-stu-id="6850f-312">A **down-cast** happens when assigning an expression of a base type to a derived variable.</span></span>

    Horse h = new Animal();

<span data-ttu-id="6850f-313">アップキャストとダウンキャストの両方が X++ でサポートされています。</span><span class="sxs-lookup"><span data-stu-id="6850f-313">Both up-casts and down-casts are supported in X++.</span></span> <span data-ttu-id="6850f-314">ただし、ダウン キャストは危険であり、できる限り回避する必要があります。</span><span class="sxs-lookup"><span data-stu-id="6850f-314">However, down-casts are dangerous and should be avoided whenever possible.</span></span> <span data-ttu-id="6850f-315">割り当てが意味をなさないため、上記の例は実行時に InvalidCastException で失敗します。</span><span class="sxs-lookup"><span data-stu-id="6850f-315">The example above will fail with an InvalidCastException at runtime, since the assignment doesn't make sense.</span></span> <span data-ttu-id="6850f-316">X++ はオブジェクトおよび formrun などの、いくつかのタイプで遅延バインドをサポートします。</span><span class="sxs-lookup"><span data-stu-id="6850f-316">X++ supports late binding on a few types, like object and formrun.</span></span> <span data-ttu-id="6850f-317">これは、つまり、そのメソッドがその型に対して明示的に宣言されていない場合、コンパイラは、コンパイル時に、それらの型に対して呼び出されているメソッドを見てもエラーを診断しないということを意味します。</span><span class="sxs-lookup"><span data-stu-id="6850f-317">This means that the compiler won't diagnose any errors at compile-time when it sees a method being called on those types, if that method isn't declared explicitly on the type.</span></span> <span data-ttu-id="6850f-318">開発者は彼らが何をしているかを把握しているとみなされます。</span><span class="sxs-lookup"><span data-stu-id="6850f-318">It's assumed that the developer knows what they're doing.</span></span> <span data-ttu-id="6850f-319">たとえば、フォーム内で検索される次のコードを参照してください。</span><span class="sxs-lookup"><span data-stu-id="6850f-319">For instance, the following code may be found in a form.</span></span>

    Object o = element.args().caller();
      o.MyMethod(3.14, “Banana”);

<span data-ttu-id="6850f-320">コンパイラは、このメソッドがオブジェクト クラスで宣言されていないため、MyMethod メソッドのパラメーター、戻り値などをチェックすることはできません。</span><span class="sxs-lookup"><span data-stu-id="6850f-320">The compiler can't check the parameters, return values, etc. for the MyMethod method, since this method isn't declared on the object class.</span></span> <span data-ttu-id="6850f-321">実行時には、リフレクションを使用して呼び出しが行われます。これは通常の呼び出しよりも桁違いに低速化されます。</span><span class="sxs-lookup"><span data-stu-id="6850f-321">At runtime, the call will be made using reflection, which is orders of magnitude slower than normal calls.</span></span> <span data-ttu-id="6850f-322">遅延バインディング型で実際に定義されているメソッドの呼び出しは必然的にチェックされることに注意してください。</span><span class="sxs-lookup"><span data-stu-id="6850f-322">Note that calls to methods that are actually defined on the late binding types will be naturally checked.</span></span> <span data-ttu-id="6850f-323">たとえば、ToString() へ呼び出します。</span><span class="sxs-lookup"><span data-stu-id="6850f-323">For example, the call to ToString():</span></span>

    o.ToString(45);

<span data-ttu-id="6850f-324">コンパイル エラーの原因になります。</span><span class="sxs-lookup"><span data-stu-id="6850f-324">will cause a compilation error:</span></span>

    'Object.toString' expects 0 argument(s), but 1 specified.

<span data-ttu-id="6850f-325">ToStringメソッド がオブジェクト クラスで定義されているため。</span><span class="sxs-lookup"><span data-stu-id="6850f-325">because the ToString method is defined on the object class.</span></span> <span data-ttu-id="6850f-326">以前のバージョンの X++ の実装とは違いが 1 つあります。これは、たとえパラメーターのプロファイルが完全に正しくない場合でも、メソッドの名前が正しい限り、関連のないオブジェクトに対してメソッドを呼び出すことができるという事実に関連しています。</span><span class="sxs-lookup"><span data-stu-id="6850f-326">There's one difference from the implementation of previous version of X++, related to the fact that methods could be called on unrelated objects, as long as the name of the method was correct, even if the parameter profiles weren't entirely correct.</span></span> <span data-ttu-id="6850f-327">これは、CIL ではサポートされていません。</span><span class="sxs-lookup"><span data-stu-id="6850f-327">This isn't supported in CIL.</span></span>

### <a name="example"></a><span data-ttu-id="6850f-328">例</span><span class="sxs-lookup"><span data-stu-id="6850f-328">Example</span></span>

    public class MyClass2
    {
      public static void Main(Args a)
      {
        Object obj = new Car();
        Horse horse = obj; // exception now thrown
        horse.run();    // Used to call car.run()!
      }
    }

<span data-ttu-id="6850f-329">コード内で IS 演算子と AS 演算子を自由に使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="6850f-329">You should use the IS and AS operators liberally in your code.</span></span> <span data-ttu-id="6850f-330">指定した式が特定の型 (派生型を含む) の場合は、IS 演算子を使用することができます。AS 演算子は、特定のタイプへのキャストを実行し、キャストが使用できない場合は null を返します。</span><span class="sxs-lookup"><span data-stu-id="6850f-330">The IS operator can be used if the expression provided is of a particular type (including derived types); the AS operator will perform casting into the given type and return null if a cast isn't possible.</span></span>

## <a name="compiler-diagnoses-attempts-to-store-objects-in-containers"></a><span data-ttu-id="6850f-331">コンパイラは、オブジェクトをコンテナに格納しようとすると診断します</span><span class="sxs-lookup"><span data-stu-id="6850f-331">Compiler diagnoses attempts to store objects in containers</span></span>
<span data-ttu-id="6850f-332">以前の X++ コンパイラでは、実行時に失敗した場合でもコンテナーにオブジェクト参照を格納することができました。</span><span class="sxs-lookup"><span data-stu-id="6850f-332">In previous incarnations of the X++ compiler, it was possible to store object references into containers, even though this would fail at runtime.</span></span> <span data-ttu-id="6850f-333">これは不可能です。</span><span class="sxs-lookup"><span data-stu-id="6850f-333">This is no longer possible.</span></span> <span data-ttu-id="6850f-334">コンパイラは、コンテナーへのオブジェクト参照の保存の試みを確認したとき</span><span class="sxs-lookup"><span data-stu-id="6850f-334">When the compiler sees an attempt to store an object reference into a container:</span></span>

    container c = [new Query()];

<span data-ttu-id="6850f-335">エラー メッセージを発行します。</span><span class="sxs-lookup"><span data-stu-id="6850f-335">It will issue the error message:</span></span>

    Instances of type 'Query' cannot be added to a container.

<span data-ttu-id="6850f-336">コンテナーに追加される要素のタイプが任意のタイプである場合、コンパイラーは値は参照タイプであるかどうかを決定することをできません。</span><span class="sxs-lookup"><span data-stu-id="6850f-336">If the type of the element that is added to the container is any type that the compiler can't make the determination of whether the value is a reference type.</span></span> <span data-ttu-id="6850f-337">コンパイラは、ユーザーが何をしているのかを把握していることを前提としてこれを許可します。</span><span class="sxs-lookup"><span data-stu-id="6850f-337">The compiler will allow this under the assumption that the user knows what they're doing.</span></span> <span data-ttu-id="6850f-338">コンパイラは次のコードを誤っていると診断しません。</span><span class="sxs-lookup"><span data-stu-id="6850f-338">The compiler won't diagnose the following code as erroneous:</span></span>

    anytype a = new Query();
            container c = [a];

<span data-ttu-id="6850f-339">しかし、実行時にエラーがスローされます。</span><span class="sxs-lookup"><span data-stu-id="6850f-339">but an error will be thrown at runtime.</span></span>

## <a name="cross-company-clause-can-contain-arbitrary-expressions"></a><span data-ttu-id="6850f-340">会社間の句には任意の式を含めることができます</span><span class="sxs-lookup"><span data-stu-id="6850f-340">Cross company clause can contain arbitrary expressions</span></span>
<span data-ttu-id="6850f-341">会社間の句は、検索ステートメントを考慮する必要のある会社を示すために select ステートメントで使用できます。</span><span class="sxs-lookup"><span data-stu-id="6850f-341">The cross company clause can be used on select statements to indicate the companies that the search statement should take into account.</span></span> <span data-ttu-id="6850f-342">構文は、コンテナー型の変数である単一の識別子ではなく、コンテナー型の任意の式を許可するように拡張されていません。</span><span class="sxs-lookup"><span data-stu-id="6850f-342">The syntax hasn't been enhanced to allow arbitrary expressions (of type container) instead of a single identifier, which is a variable of type container.</span></span>

      private void SampleMethod()
      {
        MyTable t;
        container mycompanies = ['dat', 'dmo'];
        select crosscompany: mycompanies t;
      }

<span data-ttu-id="6850f-343">現在は、この目的で変数を使用することなく、式を指定することができます。</span><span class="sxs-lookup"><span data-stu-id="6850f-343">Now, it's possible to provide the expression without having to use a variable for this purpose.</span></span>

      private void SampleMethod()
      {
        MyTable t;
        container mycompanies = ['dat', 'dmo'];
        select crosscompany: (['dat'] + ['dmo']) t;
      }

## <a name="mkdate-predefined-function-no-longer-accepts-shorthand-values"></a><span data-ttu-id="6850f-344">定義済みの mkDate 関数はショートハンド値を受け入れません</span><span class="sxs-lookup"><span data-stu-id="6850f-344">mkDate predefined function no longer accepts shorthand values</span></span>
<span data-ttu-id="6850f-345">旧式システムでは、mkDate 関数の年の引数に「短縮形」の値を使用できました。</span><span class="sxs-lookup"><span data-stu-id="6850f-345">In legacy systems, it was possible to use "shorthand" values for the year argument of the mkDate function.</span></span> <span data-ttu-id="6850f-346">結果は、次のコード サンプルで確認できます。</span><span class="sxs-lookup"><span data-stu-id="6850f-346">The effect can be seen in the following code sample.</span></span>

    static void Job16(Args _args)
    {
      int y;
      date d;

      for (y = 0; y < 150; y++)
      {
        d = mkDate(1,1,y);  
        info(strFmt("%1 - %2", y, year(d)));
      }
    }

<span data-ttu-id="6850f-347">レガシ システムでこのコードを実行すると、次の値が生成されます: 0 – 2000 1 – 2001 2 – 2002 …</span><span class="sxs-lookup"><span data-stu-id="6850f-347">Running this code in the legacy system will produce the following values: 0 – 2000 1 – 2001 2 – 2002 …</span></span> <span data-ttu-id="6850f-348">27 - 2027 28 - 2028 29 - 2029 **30 - 2030** **31 - 1931** 32 - 1932 33 - 1933 …</span><span class="sxs-lookup"><span data-stu-id="6850f-348">27 – 2027 28 – 2028 29 – 2029 **30 – 2030** **31 – 1931** 32 – 1932 33 – 1933 …</span></span> <span data-ttu-id="6850f-349">97 - 1997 98: 1998 **99 - 1999** **100 - 1900** これらの値はもうサポートされません。</span><span class="sxs-lookup"><span data-stu-id="6850f-349">97 – 1997 98 – 1998 **99 – 1999** **100 – 1900** We no longer support these values.</span></span> <span data-ttu-id="6850f-350">このような値を使用しようとすると、mkDate 関数は null の日付 (1900年1月1日) を返します。</span><span class="sxs-lookup"><span data-stu-id="6850f-350">Attempts to use such values will cause the mkDate function to return the null date (1/1/1900).</span></span>

## <a name="obsolete-statement-types"></a><span data-ttu-id="6850f-351">古いステートメント タイプ</span><span class="sxs-lookup"><span data-stu-id="6850f-351">Obsolete statement types</span></span>
<span data-ttu-id="6850f-352">次のステートメントがサポートされなくなりました。</span><span class="sxs-lookup"><span data-stu-id="6850f-352">The following statements are no longer supported.</span></span>

### <a name="pause-and-window-statements"></a><span data-ttu-id="6850f-353">一時停止およびウィンドウ ステートメント</span><span class="sxs-lookup"><span data-stu-id="6850f-353">Pause and Window statements</span></span>

<span data-ttu-id="6850f-354">X++ pause ステートメントは、影響下にあったポップアップ **印刷ウィンドウ**が削除されたため、現在はサポートされていません。</span><span class="sxs-lookup"><span data-stu-id="6850f-354">The X++ pause statement is no longer supported because the pop-up **Print Window** that it affected has been removed.</span></span> <span data-ttu-id="6850f-355">pause および window ステートメントは主に、実行環境と同じである、MorphX 開発環境内でデバッグのために使用されていました。</span><span class="sxs-lookup"><span data-stu-id="6850f-355">The pause and window statements were mainly used for debugging within the MorphX development environment, which was the same as the execution environment.</span></span> <span data-ttu-id="6850f-356">2 つが分離されたため、MorphX 環境を Visual Studio に置き換えると、これらのステートメントに関連性がなくなります。</span><span class="sxs-lookup"><span data-stu-id="6850f-356">Since the two are now separated, with Visual Studio taking the place of the MorphX environment, these statements are no longer relevant.</span></span>

### <a name="print-statement"></a><span data-ttu-id="6850f-357">明細書の印刷</span><span class="sxs-lookup"><span data-stu-id="6850f-357">Print statement</span></span>

<span data-ttu-id="6850f-358">X++ print ステートメントは、デバッグのためだけに存在していた、もう 1 つのステートメントです。</span><span class="sxs-lookup"><span data-stu-id="6850f-358">The X++ print statement is another statement that existed only for debugging purposes.</span></span> <span data-ttu-id="6850f-359">これはまだ存在しており、その基本的な考えは変わりません。</span><span class="sxs-lookup"><span data-stu-id="6850f-359">It still exists, and its basic idea is unchanged.</span></span> <span data-ttu-id="6850f-360">ただし、印刷は System.Diagnostics.WriteLine を通じて出力されるようになりました。</span><span class="sxs-lookup"><span data-stu-id="6850f-360">But print now outputs through System.Diagnostics.WriteLine.</span></span> <span data-ttu-id="6850f-361">製品の構成では、送付された書面による情報の詳細を決定します。</span><span class="sxs-lookup"><span data-stu-id="6850f-361">The product configuration determines the detail of the written information is sent.</span></span> <span data-ttu-id="6850f-362">[![DebuggingAdmin\_DebugFeatures](./media/debuggingadmin_debugfeatures.png)](./media/debuggingadmin_debugfeatures.png) 情報ログを使用することにより、出力がデバッガーおよび実行中のフォームに表示されるため、より魅力的になります。</span><span class="sxs-lookup"><span data-stu-id="6850f-362">[![DebuggingAdmin\_DebugFeatures](./media/debuggingadmin_debugfeatures.png)](./media/debuggingadmin_debugfeatures.png) You may find that using the Infolog is more compelling, since its output appears in the debugger and the running form.</span></span>

## <a name="the-ignore-list"></a><span data-ttu-id="6850f-363">Ignore リスト</span><span class="sxs-lookup"><span data-stu-id="6850f-363">The Ignore list</span></span>
<span data-ttu-id="6850f-364">従来の環境はすべて解釈されたため、一部のパーツをコンパイルせず、残りの部分を使用することも可能でした。</span><span class="sxs-lookup"><span data-stu-id="6850f-364">Since the legacy environment was all interpreted, it was possible to have some parts not compile, and use the rest.</span></span> <span data-ttu-id="6850f-365">正常にコンパイルしたメソッドのみを呼び出す場合、問題はありません。ただし、正常にコンパイルされなかったメソッドを呼び出そうとすると、問題が発生します。</span><span class="sxs-lookup"><span data-stu-id="6850f-365">As long as you only called methods that compiled correctly, you were fine; however, you would run into trouble if you tried to call methods that weren't successfully compiled.</span></span> <span data-ttu-id="6850f-366">この作業方法は CIL では機能しません。</span><span class="sxs-lookup"><span data-stu-id="6850f-366">This way of working doesn't work in CIL.</span></span> <span data-ttu-id="6850f-367">アセンブリは正常に行われたコンパイルから生成され、ランタイム システムは未完了の組み立てを読み込むことができません。</span><span class="sxs-lookup"><span data-stu-id="6850f-367">Assemblies are generated from successful compilations and the runtime system can't load incomplete assemblies.</span></span> <span data-ttu-id="6850f-368">しかし、従来のアプリケーションを新しい環境に移植する際には、段階的なやり方で実行することが有益であり、すべてを移植する前にアプリケーションの一部をテストする必要もあり、そのための正当なシナリオがあります。</span><span class="sxs-lookup"><span data-stu-id="6850f-368">However, there are legitimate scenarios when porting legacy applications into the new environment where it's beneficial to get things running in a staged fashion and where parts of the application need to be tested before everything is ported.</span></span> <span data-ttu-id="6850f-369">これはこの非常に限定されたシナリオでは役立ちますが、システムが展開された後は、実行時に発生する問題を隠してしまう可能性があるため、アプリケーションの生産準備ができた後は使用すべきではありません。</span><span class="sxs-lookup"><span data-stu-id="6850f-369">While this is useful for this very limited scenario, it shouldn't be used once the application is ready for production, since you would be hiding problems that will occur at runtime, after the system has been deployed.</span></span> <span data-ttu-id="6850f-370">プロジェクトのコンテキスト メニューから「ベスト プラクティスの抑制を編集」を選択することで、XML でメソッドを指定できます。</span><span class="sxs-lookup"><span data-stu-id="6850f-370">This is how it currently works: You can specify a method in an XML by selecting, "Edit Best Practice Suppressions," from the context menu on the project.</span></span> <span data-ttu-id="6850f-371">これにより、除外項目を管理する XML ドキュメントが開きます。</span><span class="sxs-lookup"><span data-stu-id="6850f-371">This will open an XML document where the exclusions are maintained.</span></span>

## <a name="new-debugger-features"></a><span data-ttu-id="6850f-372">新しいデバッガーの機能</span><span class="sxs-lookup"><span data-stu-id="6850f-372">New Debugger features</span></span>
<span data-ttu-id="6850f-373">このセクションでは、Visual Studio のデバッグ環境に追加した新機能について説明します。</span><span class="sxs-lookup"><span data-stu-id="6850f-373">This section provides information about the new features that we've added to the debugging experience in Visual Studio.</span></span>

### <a name="adding-tostring-methods-to-your-classes"></a><span data-ttu-id="6850f-374">クラスへの ToString メソッドの追加</span><span class="sxs-lookup"><span data-stu-id="6850f-374">Adding ToString methods to your classes</span></span>

<span data-ttu-id="6850f-375">多くの場合、ToString() メソッドをクラスに追加することが利点となります。</span><span class="sxs-lookup"><span data-stu-id="6850f-375">It's often a benefit to add ToString() methods to your classes.</span></span> <span data-ttu-id="6850f-376">これを行うのに費やした労力は何度も戻ってきます。それは簡単です。</span><span class="sxs-lookup"><span data-stu-id="6850f-376">The effort spent doing this comes back many times and it's easy to do.</span></span> <span data-ttu-id="6850f-377">このアドバイスは、レガシ X++ にも当てはまります。</span><span class="sxs-lookup"><span data-stu-id="6850f-377">This advice also holds true for legacy X++.</span></span> <span data-ttu-id="6850f-378">**注記**: ToString メソッドが予期しない時に呼び出されることがあるため、ここでオブジェクトの状態を変更することはお勧めできません。</span><span class="sxs-lookup"><span data-stu-id="6850f-378">**Note**: Since ToString methods can be called at unpredictable times, it isn't a good idea to change the state of the object here.</span></span>

### <a name="identifying-unselected-fields"></a><span data-ttu-id="6850f-379">選択されていないフィールドの識別</span><span class="sxs-lookup"><span data-stu-id="6850f-379">Identifying unselected fields</span></span>

<span data-ttu-id="6850f-380">フィールドが select ステートメントのフィールドの一覧に表示されない場合に、テーブルのフィールドを使用することがバグの一般的な発生源となります。</span><span class="sxs-lookup"><span data-stu-id="6850f-380">It's a common source of bugs to use fields from a table when these fields don't appear in the field list in a select statement.</span></span> <span data-ttu-id="6850f-381">このようなフィールドには、そのタイプに従って既定値が設定されます。</span><span class="sxs-lookup"><span data-stu-id="6850f-381">Such fields will have a default value according to their type.</span></span> <span data-ttu-id="6850f-382">値が選択されているかどうかはデバッガーで確認できるようになりました。</span><span class="sxs-lookup"><span data-stu-id="6850f-382">It's now possible in the debugger to see if a value has been selected or not.</span></span>

#### <a name="exercise"></a><span data-ttu-id="6850f-383">練習</span><span class="sxs-lookup"><span data-stu-id="6850f-383">Exercise</span></span>

<span data-ttu-id="6850f-384">次のコードを考慮してください。</span><span class="sxs-lookup"><span data-stu-id="6850f-384">Consider the following code:</span></span>

    class MyClass
    {
      public static void Main(Args a)
      {
        FMRental rental;

        select EndMileage, RentalId from rental;

        rental.Comments = "Something";
      }
    }

<span data-ttu-id="6850f-385">代入ステートメントにブレークポイントを設定します。</span><span class="sxs-lookup"><span data-stu-id="6850f-385">Set a breakpoint on the assignment statement.</span></span> <span data-ttu-id="6850f-386">クラスをプロジェクトのスタートアップ オブジェクトにして、F5 キーを押して開始します。</span><span class="sxs-lookup"><span data-stu-id="6850f-386">Make your class the startup object in your project, and start by pressing F5.</span></span> <span data-ttu-id="6850f-387">ブレークポイントが検出されたときは、ローカル ウィンドウでレンタル変数を展開して表示します。</span><span class="sxs-lookup"><span data-stu-id="6850f-387">When the breakpoint is encountered, view the rental variable by expanding it in the locals window.</span></span> <span data-ttu-id="6850f-388">次の図に似たものが表示されます。</span><span class="sxs-lookup"><span data-stu-id="6850f-388">You'll see something similar to the following graphic.</span></span> <span data-ttu-id="6850f-389">[![DebuggingAdmin2\_DebugFeatures](./media/debuggingadmin2_debugfeatures.png)](./media/debuggingadmin2_debugfeatures.png) 選択されていないフィールドが null として表示されるとき、選択された値で表示される選択されたフィールド (EndMileage および RentalId) を確認できます。</span><span class="sxs-lookup"><span data-stu-id="6850f-389">[![DebuggingAdmin2\_DebugFeatures](./media/debuggingadmin2_debugfeatures.png)](./media/debuggingadmin2_debugfeatures.png) You can see that the fields that have been selected (EndMileage and RentalId) appear with their selected values, while the unselected fields appear as null.</span></span> <span data-ttu-id="6850f-390">これは、その値がデータベースからフェッチされなかったことを示します。</span><span class="sxs-lookup"><span data-stu-id="6850f-390">This signifies their value wasn't fetched from the database.</span></span> <span data-ttu-id="6850f-391">当然、これはデバッグ コンポーネントです。</span><span class="sxs-lookup"><span data-stu-id="6850f-391">Obviously, this is a debugging artifact.</span></span> <span data-ttu-id="6850f-392">選択されていないフィールドの値は、フィールドのタイプの規定値になります。</span><span class="sxs-lookup"><span data-stu-id="6850f-392">The values of the unselected fields will be the default value for the type of the field.</span></span> <span data-ttu-id="6850f-393">これをステップオーバーし、デバッガーが実際の値のレンダリングをどのように変更するかを確認します。</span><span class="sxs-lookup"><span data-stu-id="6850f-393">Step over this and notice how the debugger changes the rendering to the actual value.</span></span> <span data-ttu-id="6850f-394">**注記**: テーブルがキャッシュに設定されている場合、システムは常にコードに含まれるフィールド リストに関係なく、テーブル全体からすべてのフィールドをフェッチします。</span><span class="sxs-lookup"><span data-stu-id="6850f-394">**Note**: If the table is set to Cache, the system will always fetch all fields from the entire table, irrespective of the field list provided in the code.</span></span>

### <a name="the-auto-and-infolog-windows"></a><span data-ttu-id="6850f-395">自動および情報ログ ウィンドウ</span><span class="sxs-lookup"><span data-stu-id="6850f-395">The Auto and Infolog Windows</span></span>

<span data-ttu-id="6850f-396">デバッガーを使用すると、アプリケーションの状態の特定の部分にアクセスできます。</span><span class="sxs-lookup"><span data-stu-id="6850f-396">The debugger will allow you to easily access certain parts of the state of the application.</span></span> <span data-ttu-id="6850f-397">この情報は、現在の会社、パーティション、トランザクション レベル、および現在のユーザー ID が一覧表示される [自動] ウィンドウで使用できます。</span><span class="sxs-lookup"><span data-stu-id="6850f-397">This information is available in the autos window, where the current company, the partition, the transaction level, and the current user ID are listed.</span></span> <span data-ttu-id="6850f-398">[![自動 \_DebugFeatures](./media/autos_debugfeatures.png)](./media/autos_debugfeatures.png) また、情報ログに書き込まれるデータを示すウィンドウもあります。</span><span class="sxs-lookup"><span data-stu-id="6850f-398">[![Autos\_DebugFeatures](./media/autos_debugfeatures.png)](./media/autos_debugfeatures.png) There is also a window showing the data that is written to the Infolog.</span></span> <span data-ttu-id="6850f-399">[![Infolog\_DebugFeatures](./media/infolog_debugfeatures.png)](./media/infolog_debugfeatures.png)</span><span class="sxs-lookup"><span data-stu-id="6850f-399">[![Infolog\_DebugFeatures](./media/infolog_debugfeatures.png)](./media/infolog_debugfeatures.png)</span></span>

### <a name="new-breakpoint-features"></a><span data-ttu-id="6850f-400">新しいブレークポイント機能</span><span class="sxs-lookup"><span data-stu-id="6850f-400">New breakpoint features</span></span>

<span data-ttu-id="6850f-401">Visual Studio デバッガーでは、条件付きブレークポイントと、ヒット カウントによってトリガーされたブレークポイントをサポートします。</span><span class="sxs-lookup"><span data-stu-id="6850f-401">The Visual Studio debugger supports conditional breakpoints and breakpoints that are triggered by hit count.</span></span> <span data-ttu-id="6850f-402">また、ブレークポイントをヒットするとき、ユーザーのためにシステムが特定のアクションを実行させることができます。</span><span class="sxs-lookup"><span data-stu-id="6850f-402">You can also have the system perform specific actions for you as you hit the breakpoint.</span></span> <span data-ttu-id="6850f-403">これらの機能のいずれも従来のデバッガーでは使用できませんでした。</span><span class="sxs-lookup"><span data-stu-id="6850f-403">None of these features were available in the legacy debugger.</span></span> <span data-ttu-id="6850f-404">これらについて以下に詳しく説明します。</span><span class="sxs-lookup"><span data-stu-id="6850f-404">These are explained below:</span></span>

-   <span data-ttu-id="6850f-405">ヒット カウントを使用することで、デバッガーが実行を中断する前にブレークポイントがヒットする回数を決定できます。</span><span class="sxs-lookup"><span data-stu-id="6850f-405">Hit count enables you to determine how many times the breakpoint is hit before the debugger breaks execution.</span></span> <span data-ttu-id="6850f-406">既定では、デバッガーはブレークポイントがヒットするたびに実行を中断します。</span><span class="sxs-lookup"><span data-stu-id="6850f-406">By default, the debugger breaks execution every time that the breakpoint is hit.</span></span> <span data-ttu-id="6850f-407">ブレークポイントが 2 回ヒットするたび、または 10 回ヒットするたび、または 512 回ヒットするたび、またはユーザーが選択した回数ヒットするたびにデバッガーが中断するよう、ヒット カウントを設定することができます。</span><span class="sxs-lookup"><span data-stu-id="6850f-407">You can set a hit count to tell the debugger to break every 2 times the breakpoint is hit, or every 10 times, or every 512 times, or any other number you choose.</span></span> <span data-ttu-id="6850f-408">一部のバグは、最初にユーザー プログラムがループを実行し、関数を呼び出し、または変数へアクセスする際に現れないため、ヒット数は役に立ちます。</span><span class="sxs-lookup"><span data-stu-id="6850f-408">Hit counts can be useful because some bugs don't appear the first time your program executes a loop, calls a function, or accesses a variable.</span></span> <span data-ttu-id="6850f-409">場合によっては、100 回または 1000 回繰り返すまでバグが表示されない可能性があります、</span><span class="sxs-lookup"><span data-stu-id="6850f-409">Sometimes, the bug might not appear until the 100th or the 1000th iteration.</span></span> <span data-ttu-id="6850f-410">このような問題をデバッグするには、ヒット数が 100 または 1000 のブレークポイントを設定します。</span><span class="sxs-lookup"><span data-stu-id="6850f-410">To debug such a problem, you can set a breakpoint with a hit count of 100 or 1000.</span></span>
-   <span data-ttu-id="6850f-411">条件は、ブレークポイントがヒットするかスキップするかを決定する式です。</span><span class="sxs-lookup"><span data-stu-id="6850f-411">Condition is an expression that determines whether the breakpoint is hit or skipped.</span></span> <span data-ttu-id="6850f-412">デバッガーは、ブレークポイントに到達すると、条件を評価します。</span><span class="sxs-lookup"><span data-stu-id="6850f-412">When the debugger reaches the breakpoint, it'll evaluate the condition.</span></span> <span data-ttu-id="6850f-413">条件が満たされた場合にのみ、ブレークポイントにヒットします。</span><span class="sxs-lookup"><span data-stu-id="6850f-413">The breakpoint will be hit only if the condition is satisfied.</span></span> <span data-ttu-id="6850f-414">場所ブレークポイントを持つ条件を使用して、特定の条件が true の時にのみ指定された場所で停止することができます。</span><span class="sxs-lookup"><span data-stu-id="6850f-414">You can use a condition with a location breakpoint to stop at a specified location only when a certain condition is true.</span></span> <span data-ttu-id="6850f-415">たとえば、勘定残高がマイナスにならないように、銀行決済プログラムをデバッグしているとします。</span><span class="sxs-lookup"><span data-stu-id="6850f-415">For example, suppose you're debugging a banking program where the account balance is never allowed to go below zero.</span></span> <span data-ttu-id="6850f-416">コード内の特定の場所でブレークポイントを設定し、残高 &lt; 0 などの条件をそれぞれに添付する場合があります。</span><span class="sxs-lookup"><span data-stu-id="6850f-416">You might set breakpoints at certain locations in the code and attach a condition such as balance &lt; 0 to each one.</span></span> <span data-ttu-id="6850f-417">プログラムを実行するとき、残高が 0 より小さい場合にのみこれらの場所で実行が中断されます。</span><span class="sxs-lookup"><span data-stu-id="6850f-417">When you run the program, execution will break at those locations only when the balance is less than zero.</span></span> <span data-ttu-id="6850f-418">最初のブレークポイントの位置で変数およびプログラムの状態を調べ、2 つ目のブレークポイントの位置まで実行を続行、などを実行することができます。</span><span class="sxs-lookup"><span data-stu-id="6850f-418">You can examine variables and program state at the first breakpoint location, and then continue execution to the second breakpoint location, and so on.</span></span>
-   <span data-ttu-id="6850f-419">アクションは、ブレークポイントがヒットした場合に発生する必要のあるものを指定します。</span><span class="sxs-lookup"><span data-stu-id="6850f-419">Action specifies something that should occur when the breakpoint is hit.</span></span> <span data-ttu-id="6850f-420">既定では、デバッガーは実行を中断しますが、代わりにメッセージを印刷するか Visual Studio マクロを実行するかを選択できます。</span><span class="sxs-lookup"><span data-stu-id="6850f-420">By default, the debugger breaks execution, but you can choose to print a message or run a Visual Studio macro instead.</span></span> <span data-ttu-id="6850f-421">中断するのではなく、メッセージを印刷する場合は、ブレークポイントは Trace ステートメントと非常に類似します。</span><span class="sxs-lookup"><span data-stu-id="6850f-421">If you decide to print a message instead of breaking, the breakpoint has an effect very similar to a Trace statement.</span></span> <span data-ttu-id="6850f-422">このブレークポイントを使用するメソッドはトレース ポイントと呼ばれます。</span><span class="sxs-lookup"><span data-stu-id="6850f-422">This method of using breakpoints is called trace points.</span></span>

#### <a name="exercise"></a><span data-ttu-id="6850f-423">練習</span><span class="sxs-lookup"><span data-stu-id="6850f-423">Exercise</span></span>

<span data-ttu-id="6850f-424">次のコードを考慮してください。</span><span class="sxs-lookup"><span data-stu-id="6850f-424">Consider the following code:</span></span>

    class PVsClass
    {
      public static void Main(Args a)
      {
        int i;
        for (i = 0; i < 10; i++)
        {
          print i;
        }
      }
    }

<span data-ttu-id="6850f-425">そのステートメントが選択されているときに F9 キーを押すことで、印刷明細書にブレークポイントを設定します。</span><span class="sxs-lookup"><span data-stu-id="6850f-425">Put a breakpoint on the print statements by pressing F9 while that statement is selected.</span></span> <span data-ttu-id="6850f-426">これにより、通常の無条件ブレークポイントが作成されます。</span><span class="sxs-lookup"><span data-stu-id="6850f-426">This will create a normal, unconditional breakpoint.</span></span> <span data-ttu-id="6850f-427">ここで、マウスを使用して、ブレークポイントのコンテキスト メニューを開き、**条件**を選択します。</span><span class="sxs-lookup"><span data-stu-id="6850f-427">Now, use the mouse to open the context menu for the breakpoint and select **Condition**.</span></span> <span data-ttu-id="6850f-428">"i" 変数が 5 を超えたときにブレークポイントが発生することを示す条件を配置します。</span><span class="sxs-lookup"><span data-stu-id="6850f-428">Put in a condition that indicates that the breakpoint should happen when the value of the 'i' variable exceeds 5.</span></span> <span data-ttu-id="6850f-429">スタートアップ プロジェクトとしてクラスを設定し、プロジェクト内のスタートアップ項目としてコードを含むクラスを設定します。</span><span class="sxs-lookup"><span data-stu-id="6850f-429">Set the class as a startup project, and the class containing the code as the startup item in the project.</span></span> <span data-ttu-id="6850f-430">コードを実行します。</span><span class="sxs-lookup"><span data-stu-id="6850f-430">Run the code.</span></span> <span data-ttu-id="6850f-431">デバッガーを使用して「i」の値を自由に変更してください。</span><span class="sxs-lookup"><span data-stu-id="6850f-431">Feel free to modify the value of 'i' using the debugger.</span></span> <span data-ttu-id="6850f-432">ここで、このブレークポイントを削除し、ヒット カウント機能を使用して同じことを実現します。</span><span class="sxs-lookup"><span data-stu-id="6850f-432">Now, remove this breakpoint, and use the Hit count feature to accomplish the same thing.</span></span> <span data-ttu-id="6850f-433">**注記**: ブレークポイントにはいくつかの条件があります。</span><span class="sxs-lookup"><span data-stu-id="6850f-433">**Note**: A breakpoint can have several conditions.</span></span> <span data-ttu-id="6850f-434">多くの場合、ブレークポイントにカーソルを置くと役立つツールヒントが表示されれば便利です。</span><span class="sxs-lookup"><span data-stu-id="6850f-434">It's often helpful to hover the cursor over the breakpoint, causing an informative tooltip to appear.</span></span> <span data-ttu-id="6850f-435">トレース ポイントは、しばしばトレースの実行に役立ちます。</span><span class="sxs-lookup"><span data-stu-id="6850f-435">Trace points are often useful tot race execution.</span></span> <span data-ttu-id="6850f-436">対象の行に追跡ポイントを挿入し、変数の値を記録します。</span><span class="sxs-lookup"><span data-stu-id="6850f-436">Insert a trace point on the line in question and log the value of the variable.</span></span> <span data-ttu-id="6850f-437">トレース出力がデバッガーの出力ウィンドウに表示されます。</span><span class="sxs-lookup"><span data-stu-id="6850f-437">The trace output will appear in the output window in the debugger.</span></span>

### <a name="the-immediate-window"></a><span data-ttu-id="6850f-438">直接ウィンドウ</span><span class="sxs-lookup"><span data-stu-id="6850f-438">The immediate window</span></span>

<span data-ttu-id="6850f-439">直接ウィンドウは VS デバッガーの便利な機能で、ユーザーはいつでも評価するために式と明細書を入力できます。</span><span class="sxs-lookup"><span data-stu-id="6850f-439">The immediate window is a useful feature in the VS debugger that allows the user to enter expression and statements to evaluate at any given time.</span></span> <span data-ttu-id="6850f-440">この機能は現在、X++スタックには実装されていません。多くの言語、特に \# の場合と同様です。</span><span class="sxs-lookup"><span data-stu-id="6850f-440">This feature isn't currently implemented in the X++ stack, as is the case for many other languages, notably F\#.</span></span> <span data-ttu-id="6850f-441">ただし、それは精通したユーザーが直接ウィンドウから益を得られないという意味ではありません。</span><span class="sxs-lookup"><span data-stu-id="6850f-441">However, that doesn't mean that the savvy user can't benefit from the immediate window.</span></span> <span data-ttu-id="6850f-442">スニペットは X++ ではなく C\# で表す必要があることを示すだけです。</span><span class="sxs-lookup"><span data-stu-id="6850f-442">It just means that snippets must be expressed in C\#, not in X++.</span></span> <span data-ttu-id="6850f-443">これがどのように大きな効果を発揮するかについての詳細を記述した、別のドキュメントがあります。</span><span class="sxs-lookup"><span data-stu-id="6850f-443">There's a separate document that describes the details of how this can be done to great effect.</span></span>



