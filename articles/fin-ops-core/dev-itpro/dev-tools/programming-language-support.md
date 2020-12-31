---
title: X++ と X++ コンパイラの変更
description: このトピックでは、Finance and Operations アプリケーションのコンパイラーになされた変更についてレビューします。
author: pvillads
manager: AnnBe
ms.date: 12/18/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Developer
ms.reviewer: rhaertle
ms.custom: 26781
ms.search.region: Global
ms.author: pvillads
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 31e40d59a98b12ddeac0a20a589585f6aca17eeb
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/13/2020
ms.locfileid: "4408987"
---
# <a name="changes-in-x-and-the-x-compiler"></a><span data-ttu-id="9b3f3-103">X++ と X++ コンパイラの変更</span><span class="sxs-lookup"><span data-stu-id="9b3f3-103">Changes in X++ and the X++ compiler</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="9b3f3-104">このトピックでは、Finance and Operations アプリケーションのコンパイラーになされた変更についてレビューします。</span><span class="sxs-lookup"><span data-stu-id="9b3f3-104">This topic reviews the changes made to the compiler for Finance and Operations applications.</span></span> <span data-ttu-id="9b3f3-105">X++ コンパイラは書き換えられています。</span><span class="sxs-lookup"><span data-stu-id="9b3f3-105">The X++ compiler has been rewritten.</span></span> <span data-ttu-id="9b3f3-106">製品への構造的な変更によって必須とされる場合を除き、X++ に導入された下位互換性のない変更はありません。</span><span class="sxs-lookup"><span data-stu-id="9b3f3-106">No backward-incompatible changes have been introduced to X++ except where required by structural changes to the product.</span></span> <span data-ttu-id="9b3f3-107">いくつかの言語拡張機能が追加されました。</span><span class="sxs-lookup"><span data-stu-id="9b3f3-107">A few language enhancements have been added.</span></span> <span data-ttu-id="9b3f3-108">また、新しい X++ ベスト プラクティス ツールが実装されているため、ユーザー定義のカスタム ルールを追加できます。</span><span class="sxs-lookup"><span data-stu-id="9b3f3-108">A new X++ best practice tool has also been implemented, which allows the addition of user-defined custom rules.</span></span>

## <a name="no-more-p-code-everything-is-in-net-framework-cil"></a><span data-ttu-id="9b3f3-109">P コードはもう不要です。すべては .NET Framework CIL にあります</span><span class="sxs-lookup"><span data-stu-id="9b3f3-109">No more p-code, everything is in .NET Framework CIL</span></span>
<span data-ttu-id="9b3f3-110">Microsoft Dynamics AX 2012 によって X++ ソース コードは p コードにコンパイルされ、実行時にインタープリタによって解釈されました。</span><span class="sxs-lookup"><span data-stu-id="9b3f3-110">Through Microsoft Dynamics AX 2012, X++ source code was compiled into p-code, which was understood by the interpreter at run time.</span></span> <span data-ttu-id="9b3f3-111">必要に応じて、Microsoft .NET CIL (共通中間言語) に p コードをコンパイルすることができます。</span><span class="sxs-lookup"><span data-stu-id="9b3f3-111">Optionally, you could then compile the p-code into Microsoft .NET CIL (Common Intermediate Language).</span></span> <span data-ttu-id="9b3f3-112">CIL は C\# および Visual Basic の .NETコンパイラ が生成するものです。</span><span class="sxs-lookup"><span data-stu-id="9b3f3-112">CIL is what the .NET compilers for C\# and Visual Basic generate.</span></span> <span data-ttu-id="9b3f3-113">ただし、X++ CIL コードは、主にサービスとバッチ ジョブで実行されるコードに対して、限られた場合でのみ使用できました。</span><span class="sxs-lookup"><span data-stu-id="9b3f3-113">However, X++ CIL code was usable only in limited cases, mainly for code executed in services and batch jobs.</span></span> <span data-ttu-id="9b3f3-114">新しい X++ コンパイラは CIL のみを生成します。</span><span class="sxs-lookup"><span data-stu-id="9b3f3-114">The new X++ compiler generates CIL only.</span></span> <span data-ttu-id="9b3f3-115">他の p コードはありません。</span><span class="sxs-lookup"><span data-stu-id="9b3f3-115">There is no more p-code.</span></span> <span data-ttu-id="9b3f3-116">p コードを扱う以下のツールは廃止され、Dynamics AX から削除され、.NET ツールに置き換えられました。</span><span class="sxs-lookup"><span data-stu-id="9b3f3-116">The following tools that worked with p-code are now obsolete and have been removed from Dynamics AX and replaced by .NET tools:</span></span>

-   <span data-ttu-id="9b3f3-117">P コードを生成する X++ コンパイラ。</span><span class="sxs-lookup"><span data-stu-id="9b3f3-117">The X++ compiler that generated p-code.</span></span>
-   <span data-ttu-id="9b3f3-118">p-code を入力して .NET CIL を生成する特別なコンパイラ。</span><span class="sxs-lookup"><span data-stu-id="9b3f3-118">The special compiler that input p-code and generated .NET CIL.</span></span>
-   <span data-ttu-id="9b3f3-119">その確定的なガベージ コレクターを含む p コードの実行時インタプリター。</span><span class="sxs-lookup"><span data-stu-id="9b3f3-119">The run time interpreter of p-code including its deterministic garbage collector.</span></span>
-   <span data-ttu-id="9b3f3-120">Dynamics AX デバッガーー。</span><span class="sxs-lookup"><span data-stu-id="9b3f3-120">The Dynamics AX Debugger.</span></span>
-   <span data-ttu-id="9b3f3-121">パフォーマンス上のボトルネックを特定するのに役立つ Dynamics AX コード プロファイラー。</span><span class="sxs-lookup"><span data-stu-id="9b3f3-121">The Dynamics AX Code Profiler, which helped find performance bottlenecks.</span></span>
-   <span data-ttu-id="9b3f3-122">Dynamics AX と相互運用される外部アプリケーションの AX .NET Business Connector。</span><span class="sxs-lookup"><span data-stu-id="9b3f3-122">The AX .NET Business Connector for external applications that interoperated with Dynamics AX.</span></span>

<span data-ttu-id="9b3f3-123">.NET CIL として排他的に動作する X++ コードには、次のような重要な利点があります。</span><span class="sxs-lookup"><span data-stu-id="9b3f3-123">There are important benefits to X++ code running exclusively as .NET CIL, including:</span></span>

-   <span data-ttu-id="9b3f3-124">ほとんどのシナリオでは、CIL はより高速に動作します。</span><span class="sxs-lookup"><span data-stu-id="9b3f3-124">CIL runs much faster in most scenarios.</span></span> <span data-ttu-id="9b3f3-125">多くのメソッドの呼び出しがあり、大量のアルゴリズム コンテンツ (データベース アクセスではない) がある場合、大幅なパフォーマンスの向上が期待できます。</span><span class="sxs-lookup"><span data-stu-id="9b3f3-125">In cases where there are many method calls, and a lot of algorithmic content (as opposed to database access), you can expect significant performance improvements.</span></span>
    -   <span data-ttu-id="9b3f3-126">アプリケーション ロジックを他のマネージド言語で記述することがより簡単です。</span><span class="sxs-lookup"><span data-stu-id="9b3f3-126">It's easier to write application logic in other managed languages.</span></span>
    -   <span data-ttu-id="9b3f3-127">アセンブリを直接消費することができるため、AX .NET Business Connector や管理プロキシは必要なくなりました。</span><span class="sxs-lookup"><span data-stu-id="9b3f3-127">There's no longer any need for the AX .NET Business Connector or managed proxies, because the assemblies can be consumed directly.</span></span>
    -   <span data-ttu-id="9b3f3-128">ビジネス ロジックを外部で使用する適切な方法は、サービスを使用することです。</span><span class="sxs-lookup"><span data-stu-id="9b3f3-128">The preferred way of consuming business logic externally is by using services.</span></span>
-   <span data-ttu-id="9b3f3-129">CIL は、他の .NET アセンブリ DLL ファイルで使用可能なクラスを効率的に参照できます。実行時間リフレクション ベースのオーバーヘッドは P コード インタープリターに負担をかけません。</span><span class="sxs-lookup"><span data-stu-id="9b3f3-129">CIL can efficiently reference classes that are available in other .NET assembly DLL files, without the run time reflection-based overhead that burdened the p-code interpreter.</span></span>
-   <span data-ttu-id="9b3f3-130">CIL は多数の .NET ツールから操作できます。</span><span class="sxs-lookup"><span data-stu-id="9b3f3-130">CIL can be operated on by the many .NET tools.</span></span>

## <a name="unit-of-compilation"></a><span data-ttu-id="9b3f3-131">コンパイルの単位</span><span class="sxs-lookup"><span data-stu-id="9b3f3-131">Unit of compilation</span></span>
<span data-ttu-id="9b3f3-132">Microsoft Dynamics AX の以前のバージョンは、個々のメソッドのレベルで X++ をコンパイルできます。</span><span class="sxs-lookup"><span data-stu-id="9b3f3-132">Previous versions of Microsoft Dynamics AX could compile X++ at the level of an individual method.</span></span> <span data-ttu-id="9b3f3-133">したがって、クラスのコンパイルにおいてクラスの 1 つのメソッドでエラーが見つかった場合、正しくコンパイルされたメソッドはまだ実行可能でした。</span><span class="sxs-lookup"><span data-stu-id="9b3f3-133">Thus if a compilation of a class found an error in one method of the class, the methods that did compile correctly were still runnable.</span></span> <span data-ttu-id="9b3f3-134">標準のコンパイルで、単位は C\# などの他の .NET 言語と同じです。</span><span class="sxs-lookup"><span data-stu-id="9b3f3-134">In the standard compilation unit now is the same as for other .NET languages such as C\#.</span></span> <span data-ttu-id="9b3f3-135">モデル要素 (クラス、フォーム、クエリなど) で任意のメソッドがコンパイルに失敗すると、すべてのコンパイルが失敗します。</span><span class="sxs-lookup"><span data-stu-id="9b3f3-135">If any method in a model element (class, form, query etc.) fails to compile, the whole compilation fails.</span></span>

## <a name="enhancements-to-x"></a><span data-ttu-id="9b3f3-136">X++ の拡張機能</span><span class="sxs-lookup"><span data-stu-id="9b3f3-136">Enhancements to X++</span></span>
<span data-ttu-id="9b3f3-137">X++ は .NET の世界でファーストクラスの住民になりました。</span><span class="sxs-lookup"><span data-stu-id="9b3f3-137">X++ is now a first-class citizen in the .NET world.</span></span> <span data-ttu-id="9b3f3-138">そのため、C\# や他の .NET 言語で利用可能な X++ のいくつかの構造に追加しています。</span><span class="sxs-lookup"><span data-stu-id="9b3f3-138">Therefore we are adding to X++ several constructs that are available in C\# and other mainstream .NET languages.</span></span> <span data-ttu-id="9b3f3-139">変更は一般的に非侵入型です。</span><span class="sxs-lookup"><span data-stu-id="9b3f3-139">The changes are generally non-intrusive.</span></span> <span data-ttu-id="9b3f3-140">実際、非常にわずかな変更が既存の X++ コードの構文とセマンティクスに対して行われました。</span><span class="sxs-lookup"><span data-stu-id="9b3f3-140">In fact, very few changes have been made to the syntax and semantics of existing X++ code.</span></span> <span data-ttu-id="9b3f3-141">これらの追加内容のほとんどが、次の一覧にあります。</span><span class="sxs-lookup"><span data-stu-id="9b3f3-141">Most of these additions are in the following list:</span></span>

-   <span data-ttu-id="9b3f3-142">`finally` キーワードを `try` および `catch` キーワードの後に使用できるようになりました。</span><span class="sxs-lookup"><span data-stu-id="9b3f3-142">The `finally` keyword is now available to follow the `try` and `catch` keywords.</span></span> <span data-ttu-id="9b3f3-143">セマンティクスは C\# のセマンティクスと同じです。</span><span class="sxs-lookup"><span data-stu-id="9b3f3-143">The semantics are identical to the semantics in C\#.</span></span> <span data-ttu-id="9b3f3-144">finally 句に指定されたステートメントは、try ブロックが例外をスローしたかどうかにかかわらず実行されます。</span><span class="sxs-lookup"><span data-stu-id="9b3f3-144">The statements provided in the finally clause are executed irrespective of whether the try block threw any exceptions.</span></span>
-   <span data-ttu-id="9b3f3-145">`using` キーワードは、.NET 名前空間を参照するための省略形として追加されました。</span><span class="sxs-lookup"><span data-stu-id="9b3f3-145">The `using` keyword has been added as shorthand for referencing .NET namespaces.</span></span> <span data-ttu-id="9b3f3-146">次のコード例は、using キーワードを使用して名前空間を参照する2つの方法を示しています。</span><span class="sxs-lookup"><span data-stu-id="9b3f3-146">The following code example illustrates two ways of utilizing the using keyword to reference namespaces:</span></span>

    ```xpp
    using SysColl = System.Collections;  // SysColl is an alias for the whole namespace.
    using           System.CodeDom;      // Contains the class named CodeComment.

    public class MyClass2
    {
        static SysColl.ArrayList arrayList = new SysColl.ArrayList(); // Initialized on declaration.
        CodeComment codeComment          = new CodeComment("I am a comment.");

        // More X++ code here.
    }
    ```

-   <span data-ttu-id="9b3f3-147">クラスのフィールドをフィールドの declaration ステートメントで初期化することができるようになりました。</span><span class="sxs-lookup"><span data-stu-id="9b3f3-147">You can now initialize a class's field in the field's declaration statement.</span></span> <span data-ttu-id="9b3f3-148">これは、前のコード例で 2 回示されています。</span><span class="sxs-lookup"><span data-stu-id="9b3f3-148">This is illustrated twice in the previous code example.</span></span>
-   <span data-ttu-id="9b3f3-149">メソッドの開始時だけでなく、小さなスコープ内で変数を宣言することができます。</span><span class="sxs-lookup"><span data-stu-id="9b3f3-149">You can declare variables in smaller scopes, not just at the start of methods.</span></span>
-   <span data-ttu-id="9b3f3-150">`var` キーワードは、宣言された変数の型を推定するコンパイラを許可するショートカットとして使用できます。</span><span class="sxs-lookup"><span data-stu-id="9b3f3-150">The `var` keyword is available as a shortcut that allows the compiler to infer the type of the declared variable.</span></span>
-   <span data-ttu-id="9b3f3-151">クラスのフィールドを静的にすることができます。</span><span class="sxs-lookup"><span data-stu-id="9b3f3-151">A class's fields can now be static.</span></span> <span data-ttu-id="9b3f3-152">以前のバージョンでは、インスタンス フィールドのみ許可されていました。</span><span class="sxs-lookup"><span data-stu-id="9b3f3-152">In previous versions, only instance fields were allowed.</span></span>
-   <span data-ttu-id="9b3f3-153">クラスは、1 つの静的コンストラクターを持つことができます。</span><span class="sxs-lookup"><span data-stu-id="9b3f3-153">A class can now have one static constructor.</span></span> <span data-ttu-id="9b3f3-154">以前のバージョンでは、インスタンス コンストラクターのみ使用できました。</span><span class="sxs-lookup"><span data-stu-id="9b3f3-154">In previous versions, only instance constructors were available.</span></span> <span data-ttu-id="9b3f3-155">次の X++のコード例は、新しいキーワード typenew による 、静的コンストラクターの構文を示しています。</span><span class="sxs-lookup"><span data-stu-id="9b3f3-155">The following X++ code example shows the syntax for a static constructor, through the new keyword typenew.</span></span>

    ```xpp
    public class MyClass4
    {
        static utcdatetime utcInitialized3;  // Static variable member.
        static void typenew()                // Static constructor member. 'typenew' is a new keyword.
        {
            utcInitialized3 = DateTimeUtil::utcNow(); // Static variable referenced without class name.
        }
    }
    ```

-   <span data-ttu-id="9b3f3-156">属性の修飾で、接尾語に `Attribute` がある場合、クラスまたはメソッドのような属性名の接尾語を省略できます。</span><span class="sxs-lookup"><span data-stu-id="9b3f3-156">An attribute decoration, such as on a class or a method, can now omit the suffix of the attribute name if the suffix is `Attribute`.</span></span> <span data-ttu-id="9b3f3-157">したがって、X++ は C\# を結合し、`[MyFavoriteAttribute]` を要求する代わりに `[MyFavorite]` を許可します。</span><span class="sxs-lookup"><span data-stu-id="9b3f3-157">So the X++ joins the C\# in allowing `[MyFavorite]` instead of requiring `[MyFavoriteAttribute]`.</span></span>
-   <span data-ttu-id="9b3f3-158">デリゲートはクラスにだけでなく、テーブル、フォーム、またはクエリで定義できるようになりました。</span><span class="sxs-lookup"><span data-stu-id="9b3f3-158">A delegate can now be defined in a table, form, or query, and not just in a class.</span></span>
-   <span data-ttu-id="9b3f3-159">属性はデリゲートとメソッドのハンドラーに現在適用され、ハンドラーをこれらの目標にマップします。</span><span class="sxs-lookup"><span data-stu-id="9b3f3-159">Attributes are now applied to the handlers of delegates and methods, to map the handlers to those targets.</span></span>
-   <span data-ttu-id="9b3f3-160">これで、クラスは X++ ソース コードに入れ子にできます。</span><span class="sxs-lookup"><span data-stu-id="9b3f3-160">Classes can now be nested in X++ source code.</span></span> <span data-ttu-id="9b3f3-161">入れ子になったクラスはフォーム内 (FormRun を拡張するクラスなど) でのみ使用でき、コントロール、データ ソースまたはデータ フィールドを表します。</span><span class="sxs-lookup"><span data-stu-id="9b3f3-161">Nested classes are available only inside forms (such as a class that extends FormRun) to represent controls, data sources, or data fields.</span></span>

## <a name="backward-incompatible-changes-to-x"></a><span data-ttu-id="9b3f3-162">X++ への後方互換性のない変更</span><span class="sxs-lookup"><span data-stu-id="9b3f3-162">Backward-incompatible changes to X++</span></span>
<span data-ttu-id="9b3f3-163">従来のカスタム X++ ソース コードに対応する変更が必要な X++ には、変更点がいくつかあります。</span><span class="sxs-lookup"><span data-stu-id="9b3f3-163">There are a few changes to X++ that require corresponding changes in legacy custom X++ source code.</span></span> <span data-ttu-id="9b3f3-164">これらの変更内容のほとんどが、次の一覧にあります。</span><span class="sxs-lookup"><span data-stu-id="9b3f3-164">Most of these changes are in the following list:</span></span>

-   <span data-ttu-id="9b3f3-165">次のキーワードは、X++ 言語の一部ではなくなっており、使用するとコンパイル エラーが発生します。</span><span class="sxs-lookup"><span data-stu-id="9b3f3-165">The following keywords are no longer part of the X++ language, and their use causes compilation errors:</span></span>
    -   `changeSite`
    -   `pause`
    -   `window`
-   <span data-ttu-id="9b3f3-166">旧式 X++ では、クライアントまたはサーバーのいずれかを実行するメソッドを指定できました。</span><span class="sxs-lookup"><span data-stu-id="9b3f3-166">In legacy X++, it was possible to designate a method to run either on the client or the server.</span></span> <span data-ttu-id="9b3f3-167">これは不可能です。</span><span class="sxs-lookup"><span data-stu-id="9b3f3-167">This is no longer possible.</span></span> <span data-ttu-id="9b3f3-168">すべてのコンパイルされた X++ コードは、サーバー上の .NET CIL で実行されます。</span><span class="sxs-lookup"><span data-stu-id="9b3f3-168">All compiled X++ code is executed as .NET CIL on the server.</span></span> <span data-ttu-id="9b3f3-169">クライアント サイトまたはブラウザーで評価される X++ コードは存在しないため、*client* と *server* の 2 つのキーワードは無視されます。</span><span class="sxs-lookup"><span data-stu-id="9b3f3-169">There is no longer any X++ code that is evaluated at the client site or in the browser, therefore, the two keywords, *client* and *server*, are now ignored.</span></span> <span data-ttu-id="9b3f3-170">コンパイル エラーは発生しませんが、新しい X++ コードのいずれでも使用しないでください。</span><span class="sxs-lookup"><span data-stu-id="9b3f3-170">Their use doesn't cause a compile error, but they should not be used in any new X++ code.</span></span>
-   <span data-ttu-id="9b3f3-171">Microsoft Dynamics AX 2012 には、P コード対 CIL にコンパイルしたときに X++ が異なる動作をするいくつかの領域がありました。</span><span class="sxs-lookup"><span data-stu-id="9b3f3-171">In Microsoft Dynamics AX 2012, there were a few areas where X++ behaved differently when compiled to p-code versus CIL.</span></span> <span data-ttu-id="9b3f3-172">Finance and Operations アプリケーションのこれらすべての領域では、Microsoft Dynamics AX 2012 の CIL で実行されたように動作します。</span><span class="sxs-lookup"><span data-stu-id="9b3f3-172">In Finance and Operations applications, all these areas behave as they did in CIL in Microsoft Dynamics AX 2012.</span></span> <span data-ttu-id="9b3f3-173">X++ p-code と CIL としての X++ との間の重要な動作の違いは次のとおりです:</span><span class="sxs-lookup"><span data-stu-id="9b3f3-173">The significant behavioral differences between X++ p-code versus X++ as CIL were as follows:</span></span>
    -   <span data-ttu-id="9b3f3-174">CIL では、`real `データ型が `System.Decimal` として表されます。</span><span class="sxs-lookup"><span data-stu-id="9b3f3-174">In CIL, the `real `data type is represented as `System.Decimal`.</span></span> <span data-ttu-id="9b3f3-175">これは、各 `real` の範囲と精度が p コードの場合と異なることを意味します。</span><span class="sxs-lookup"><span data-stu-id="9b3f3-175">This means the range and precision for each `real` is different than it was under p-code.</span></span> <span data-ttu-id="9b3f3-176">この変更は、.NET CIL が実行された時点で Microsoft Dynamics AX 2012 ですでに有効でした。</span><span class="sxs-lookup"><span data-stu-id="9b3f3-176">This change was already in effect in Microsoft Dynamics AX 2012 when .NET CIL was run.</span></span>
    -   <span data-ttu-id="9b3f3-177">1 つの全体配列を別の配列に割り当てることが P コード モードの値で実行されましたが、CIL モードでの参照が実行されます。</span><span class="sxs-lookup"><span data-stu-id="9b3f3-177">An assignment of one entire array to another was performed in value in p-code mode, but it's performed by reference in CIL mode.</span></span>
    -   <span data-ttu-id="9b3f3-178">`Global::runClassMethodIL` などの CIL ヘルパー メソッドは、関連性が無くなったため削除されました。</span><span class="sxs-lookup"><span data-stu-id="9b3f3-178">CIL helper methods such as `Global::runClassMethodIL` have been removed, since they're no longer relevant.</span></span>
-   <span data-ttu-id="9b3f3-179">**AOT** &gt; **Jobs** &gt; **MyJob** の意味にジョブの概念はありません。</span><span class="sxs-lookup"><span data-stu-id="9b3f3-179">There is no concept of a job, in the sense of **AOT** &gt; **Jobs** &gt; **MyJob**.</span></span> <span data-ttu-id="9b3f3-180">X++ メソッドをすばやく簡単に実行するには、`static Main` メソッドをクラスに追加し、そのクラスを Microsoft Visual Studio のプロジェクトのスタートアップ オブジェクト フォームとして設定します。</span><span class="sxs-lookup"><span data-stu-id="9b3f3-180">To quickly and easily run an X++ method, you can still add in a `static Main` method to a class, and then set the class as the startup object form for the project in Microsoft Visual Studio.</span></span> <span data-ttu-id="9b3f3-181">プロジェクトが実行されるときは、`Main`メソッドが実行されます。</span><span class="sxs-lookup"><span data-stu-id="9b3f3-181">When the project is run, the `Main` method will be run.</span></span>


## <a name="additional-resources"></a><span data-ttu-id="9b3f3-182">追加リソース</span><span class="sxs-lookup"><span data-stu-id="9b3f3-182">Additional resources</span></span>

[<span data-ttu-id="9b3f3-183">C# の統合言語クエリ (LINQ) プロバイダー</span><span class="sxs-lookup"><span data-stu-id="9b3f3-183">Language Integrated Query (LINQ) provider for C#</span></span>](linq-provider-c.md)

[<span data-ttu-id="9b3f3-184">開発およびカスタマイズのホーム ページ</span><span class="sxs-lookup"><span data-stu-id="9b3f3-184">Develop and customize home page</span></span>](developer-home-page.md)



