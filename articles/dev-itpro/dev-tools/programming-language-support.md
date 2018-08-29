---
title: "X++ と X++ コンパイラの変更"
description: "このトピックでは、Microsoft Dynamics 365 for Finance and Operations のコンパイラに対する変更点について説明します。"
author: pvillads
manager: AnnBe
ms.date: 11/03/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Developer
ms.reviewer: robinr
ms.search.scope: Operations
ms.custom: 26781
ms.assetid: 056d4064-e365-487c-a606-e2fadfe28242
ms.search.region: Global
ms.author: pvillads
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: e782d33f3748524491dace28008cd9148ae70529
ms.openlocfilehash: e4135506ce79ea51b10350220f38f46aa4c6776c
ms.contentlocale: ja-jp
ms.lasthandoff: 08/09/2018

---

# <a name="changes-in-x-and-the-x-compiler"></a><span data-ttu-id="32591-103">X++ と X++ コンパイラの変更</span><span class="sxs-lookup"><span data-stu-id="32591-103">Changes in X++ and the X++ compiler</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="32591-104">このトピックでは、Microsoft Dynamics 365 for Finance and Operations のコンパイラに対する変更点について説明します。</span><span class="sxs-lookup"><span data-stu-id="32591-104">This topic reviews the changes made to the compiler for Microsoft Dynamics 365 for Finance and Operations.</span></span> <span data-ttu-id="32591-105">X++ コンパイラは書き換えられています。</span><span class="sxs-lookup"><span data-stu-id="32591-105">The X++ compiler has been rewritten.</span></span> <span data-ttu-id="32591-106">製品への構造的な変更によって必須とされる場合を除き、X++ に導入された下位互換性のない変更はありません。</span><span class="sxs-lookup"><span data-stu-id="32591-106">No backward-incompatible changes have been introduced to X++ except where required by structural changes to the product.</span></span> <span data-ttu-id="32591-107">いくつかの言語拡張機能が追加されました。</span><span class="sxs-lookup"><span data-stu-id="32591-107">A few language enhancements have been added.</span></span> <span data-ttu-id="32591-108">また、新しい X++ ベスト プラクティス ツールが実装されているため、ユーザー定義のカスタム ルールを追加できます。</span><span class="sxs-lookup"><span data-stu-id="32591-108">A new X++ best practice tool has also been implemented, which allows the addition of user-defined custom rules.</span></span>

## <a name="no-more-p-code-everything-is-in-net-framework-cil"></a><span data-ttu-id="32591-109">P コードはもう不要です。すべては .NET Framework CIL にあります</span><span class="sxs-lookup"><span data-stu-id="32591-109">No more p-code, everything is in .NET Framework CIL</span></span>
<span data-ttu-id="32591-110">Microsoft Dynamics AX 2012 によって X++ ソース コードは p コードにコンパイルされ、実行時にインタープリタによって解釈されました。</span><span class="sxs-lookup"><span data-stu-id="32591-110">Through Microsoft Dynamics AX 2012, X++ source code was compiled into p-code, which was understood by the interpreter at run time.</span></span> <span data-ttu-id="32591-111">必要に応じて、Microsoft .NET CIL (共通中間言語) に p コードをコンパイルすることができます。</span><span class="sxs-lookup"><span data-stu-id="32591-111">Optionally, you could then compile the p-code into Microsoft .NET CIL (Common Intermediate Language).</span></span> <span data-ttu-id="32591-112">CIL は C\# および Visual Basic の .NETコンパイラ が生成するものです。</span><span class="sxs-lookup"><span data-stu-id="32591-112">CIL is what the .NET compilers for C\# and Visual Basic generate.</span></span> <span data-ttu-id="32591-113">ただし、X++ CIL コードは、主にサービスとバッチ ジョブで実行されるコードに対して、限られた場合でのみ使用できました。</span><span class="sxs-lookup"><span data-stu-id="32591-113">However, X++ CIL code was usable only in limited cases, mainly for code executed in services and batch jobs.</span></span> <span data-ttu-id="32591-114">新しい X++ コンパイラは CIL のみを生成します。</span><span class="sxs-lookup"><span data-stu-id="32591-114">The new X++ compiler generates CIL only.</span></span> <span data-ttu-id="32591-115">他の p コードはありません。</span><span class="sxs-lookup"><span data-stu-id="32591-115">There is no more p-code.</span></span> <span data-ttu-id="32591-116">p コードを扱う以下のツールは廃止され、Dynamics AX から削除され、.NET ツールに置き換えられました。</span><span class="sxs-lookup"><span data-stu-id="32591-116">The following tools that worked with p-code are now obsolete and have been removed from Dynamics AX and replaced by .NET tools:</span></span>

-   <span data-ttu-id="32591-117">P コードを生成する X++ コンパイラ。</span><span class="sxs-lookup"><span data-stu-id="32591-117">The X++ compiler that generated p-code.</span></span>
-   <span data-ttu-id="32591-118">p-code を入力して .NET CIL を生成する特別なコンパイラ。</span><span class="sxs-lookup"><span data-stu-id="32591-118">The special compiler that input p-code and generated .NET CIL.</span></span>
-   <span data-ttu-id="32591-119">その確定的なガベージ コレクターを含む p コードの実行時インタプリター。</span><span class="sxs-lookup"><span data-stu-id="32591-119">The run time interpreter of p-code including its deterministic garbage collector.</span></span>
-   <span data-ttu-id="32591-120">Dynamics AX デバッガーー。</span><span class="sxs-lookup"><span data-stu-id="32591-120">The Dynamics AX Debugger.</span></span>
-   <span data-ttu-id="32591-121">パフォーマンス上のボトルネックを特定するのに役立つ Dynamics AX コード プロファイラー。</span><span class="sxs-lookup"><span data-stu-id="32591-121">The Dynamics AX Code Profiler, which helped find performance bottlenecks.</span></span>
-   <span data-ttu-id="32591-122">Dynamics AX と相互運用される外部アプリケーションの AX .NET Business Connector。</span><span class="sxs-lookup"><span data-stu-id="32591-122">The AX .NET Business Connector for external applications that interoperated with Dynamics AX.</span></span>

<span data-ttu-id="32591-123">.NET CIL として排他的に動作する X++ コードには、次のような重要な利点があります。</span><span class="sxs-lookup"><span data-stu-id="32591-123">There are important benefits to X++ code running exclusively as .NET CIL, including:</span></span>

-   <span data-ttu-id="32591-124">ほとんどのシナリオでは、CIL はより高速に動作します。</span><span class="sxs-lookup"><span data-stu-id="32591-124">CIL runs much faster in most scenarios.</span></span> <span data-ttu-id="32591-125">多くのメソッドの呼び出しがあり、大量のアルゴリズム コンテンツ (データベース アクセスではない) がある場合、大幅なパフォーマンスの向上が期待できます。</span><span class="sxs-lookup"><span data-stu-id="32591-125">In cases where there are many method calls, and a lot of algorithmic content (as opposed to database access), you can expect significant performance improvements.</span></span>
    -   <span data-ttu-id="32591-126">アプリケーション ロジックを他のマネージド言語で記述することがより簡単です。</span><span class="sxs-lookup"><span data-stu-id="32591-126">It's easier to write application logic in other managed languages.</span></span>
    -   <span data-ttu-id="32591-127">アセンブリを直接消費することができるため、AX .NET Business Connector や管理プロキシは必要なくなりました。</span><span class="sxs-lookup"><span data-stu-id="32591-127">There's no longer any need for the AX .NET Business Connector or managed proxies, because the assemblies can be consumed directly.</span></span>
    -   <span data-ttu-id="32591-128">ビジネス ロジックを外部で使用する適切な方法は、サービスを使用することです。</span><span class="sxs-lookup"><span data-stu-id="32591-128">The preferred way of consuming business logic externally is by using services.</span></span>
-   <span data-ttu-id="32591-129">CIL は、他の .NET アセンブリ DLL ファイルで使用可能なクラスを効率的に参照できます。実行時間リフレクション ベースのオーバーヘッドは P コード インタープリターに負担をかけません。</span><span class="sxs-lookup"><span data-stu-id="32591-129">CIL can efficiently reference classes that are available in other .NET assembly DLL files, without the run time reflection-based overhead that burdened the p-code interpreter.</span></span>
-   <span data-ttu-id="32591-130">CIL は多数の .NET ツールから操作できます。</span><span class="sxs-lookup"><span data-stu-id="32591-130">CIL can be operated on by the many .NET tools.</span></span>

## <a name="unit-of-compilation"></a><span data-ttu-id="32591-131">コンパイルの単位</span><span class="sxs-lookup"><span data-stu-id="32591-131">Unit of compilation</span></span>
<span data-ttu-id="32591-132">Microsoft Dynamics AX の以前のバージョンは、個々のメソッドのレベルで X++ をコンパイルできます。</span><span class="sxs-lookup"><span data-stu-id="32591-132">Previous versions of Microsoft Dynamics AX could compile X++ at the level of an individual method.</span></span> <span data-ttu-id="32591-133">したがって、クラスのコンパイルにおいてクラスの 1 つのメソッドでエラーが見つかった場合、正しくコンパイルされたメソッドはまだ実行可能でした。</span><span class="sxs-lookup"><span data-stu-id="32591-133">Thus if a compilation of a class found an error in one method of the class, the methods that did compile correctly were still runnable.</span></span> <span data-ttu-id="32591-134">標準のコンパイルで、単位は C\# などの他の .NET 言語と同じです。</span><span class="sxs-lookup"><span data-stu-id="32591-134">In the standard compilation unit now is the same as for other .NET languages such as C\#.</span></span> <span data-ttu-id="32591-135">モデル要素 (クラス、フォーム、クエリなど) で任意のメソッドがコンパイルに失敗すると、すべてのコンパイルが失敗します。</span><span class="sxs-lookup"><span data-stu-id="32591-135">If any method in a model element (class, form, query etc.) fails to compile, the whole compilation fails.</span></span>

## <a name="enhancements-to-x"></a><span data-ttu-id="32591-136">X++ の拡張機能</span><span class="sxs-lookup"><span data-stu-id="32591-136">Enhancements to X++</span></span>
<span data-ttu-id="32591-137">X++ は .NET の世界でファーストクラスの住民になりました。</span><span class="sxs-lookup"><span data-stu-id="32591-137">X++ is now a first-class citizen in the .NET world.</span></span> <span data-ttu-id="32591-138">そのため、C\# や他の .NET 言語で利用可能な X++ のいくつかの構造に追加しています。</span><span class="sxs-lookup"><span data-stu-id="32591-138">Therefore we are adding to X++ several constructs that are available in C\# and other mainstream .NET languages.</span></span> <span data-ttu-id="32591-139">変更は一般的に非侵入型です。</span><span class="sxs-lookup"><span data-stu-id="32591-139">The changes are generally non-intrusive.</span></span> <span data-ttu-id="32591-140">実際、非常にわずかな変更が既存の X++ コードの構文とセマンティクスに対して行われました。</span><span class="sxs-lookup"><span data-stu-id="32591-140">In fact, very few changes have been made to the syntax and semantics of existing X++ code.</span></span> <span data-ttu-id="32591-141">これらの追加内容のほとんどが、次の一覧にあります。</span><span class="sxs-lookup"><span data-stu-id="32591-141">Most of these additions are in the following list:</span></span>

-   <span data-ttu-id="32591-142">`finally` キーワードを `try` および `catch` キーワードの後に使用できるようになりました。</span><span class="sxs-lookup"><span data-stu-id="32591-142">The `finally` keyword is now available to follow the `try` and `catch` keywords.</span></span> <span data-ttu-id="32591-143">セマンティクスは C\# のセマンティクスと同じです。</span><span class="sxs-lookup"><span data-stu-id="32591-143">The semantics are identical to the semantics in C\#.</span></span> <span data-ttu-id="32591-144">finally 句に指定されたステートメントは、try ブロックが例外をスローしたかどうかにかかわらず実行されます。</span><span class="sxs-lookup"><span data-stu-id="32591-144">The statements provided in the finally clause are executed irrespective of whether the try block threw any exceptions.</span></span>
-   <span data-ttu-id="32591-145">`using` キーワードは、.NET 名前空間を参照するための省略形として追加されました。</span><span class="sxs-lookup"><span data-stu-id="32591-145">The `using` keyword has been added as shorthand for referencing .NET namespaces.</span></span> <span data-ttu-id="32591-146">次のコード例は、using キーワードを使用して名前空間を参照する2つの方法を示しています。</span><span class="sxs-lookup"><span data-stu-id="32591-146">The following code example illustrates two ways of utilizing the using keyword to reference namespaces:</span></span>

        using SysColl = System.Collections;  // SysColl is an alias for the whole namespace.
        using           System.CodeDom;      // Contains the class named CodeComment.

        public class MyClass2
        {
            static SysColl.ArrayList arrayList = new SysColl.ArrayList(); // Initialized on declaration.
            CodeComment codeComment          = new CodeComment("I am a comment.");

            // More X++ code here.
        }

-   <span data-ttu-id="32591-147">クラスのフィールドをフィールドの declaration ステートメントで初期化することができるようになりました。</span><span class="sxs-lookup"><span data-stu-id="32591-147">You can now initialize a class's field in the field's declaration statement.</span></span> <span data-ttu-id="32591-148">これは、前のコード例で 2 回示されています。</span><span class="sxs-lookup"><span data-stu-id="32591-148">This is illustrated twice in the previous code example.</span></span>
-   <span data-ttu-id="32591-149">メソッドの開始時だけでなく、小さなスコープ内で変数を宣言することができます。</span><span class="sxs-lookup"><span data-stu-id="32591-149">You can declare variables in smaller scopes, not just at the start of methods.</span></span>
-   <span data-ttu-id="32591-150">`var` キーワードは、宣言された変数の型を推定するコンパイラを許可するショートカットとして使用できます。</span><span class="sxs-lookup"><span data-stu-id="32591-150">The `var` keyword is available as a shortcut that allows the compiler to infer the type of the declared variable.</span></span>
-   <span data-ttu-id="32591-151">クラスのフィールドを静的にすることができます。</span><span class="sxs-lookup"><span data-stu-id="32591-151">A class's fields can now be static.</span></span> <span data-ttu-id="32591-152">以前のバージョンでは、インスタンス フィールドのみ許可されていました。</span><span class="sxs-lookup"><span data-stu-id="32591-152">In previous versions, only instance fields were allowed.</span></span>
-   <span data-ttu-id="32591-153">クラスは、1 つの静的コンストラクターを持つことができます。</span><span class="sxs-lookup"><span data-stu-id="32591-153">A class can now have one static constructor.</span></span> <span data-ttu-id="32591-154">以前のバージョンでは、インスタンス コンストラクターのみ使用できました。</span><span class="sxs-lookup"><span data-stu-id="32591-154">In previous versions, only instance constructors were available.</span></span> <span data-ttu-id="32591-155">次の X++のコード例は、新しいキーワード typenew による 、静的コンストラクターの構文を示しています。</span><span class="sxs-lookup"><span data-stu-id="32591-155">The following X++ code example shows the syntax for a static constructor, through the new keyword typenew.</span></span>

        .    public class MyClass4
            {
                static utcdatetime utcInitialized3;  // Static variable member.
                static void typenew()                // Static constructor member. 'typenew' is a new keyword.
                {
                utcInitialized3 = DateTimeUtil::utcNow(); // Static variable referenced without class name.
                }
            }

-   <span data-ttu-id="32591-156">属性の修飾で、接尾語に `Attribute` がある場合、クラスまたはメソッドのような属性名の接尾語を省略できます。</span><span class="sxs-lookup"><span data-stu-id="32591-156">An attribute decoration, such as on a class or a method, can now omit the suffix of the attribute name if the suffix is `Attribute`.</span></span> <span data-ttu-id="32591-157">したがって、X++ は C\# を結合し、`[MyFavoriteAttribute]` を要求する代わりに `[MyFavorite]` を許可します。</span><span class="sxs-lookup"><span data-stu-id="32591-157">So the X++ joins the C\# in allowing `[MyFavorite]` instead of requiring `[MyFavoriteAttribute]`.</span></span>
-   <span data-ttu-id="32591-158">デリゲートはクラスにだけでなく、テーブル、フォーム、またはクエリで定義できるようになりました。</span><span class="sxs-lookup"><span data-stu-id="32591-158">A delegate can now be defined in a table, form, or query, and not just in a class.</span></span>
-   <span data-ttu-id="32591-159">属性はデリゲートとメソッドのハンドラーに現在適用され、ハンドラーをこれらの目標にマップします。</span><span class="sxs-lookup"><span data-stu-id="32591-159">Attributes are now applied to the handlers of delegates and methods, to map the handlers to those targets.</span></span>
-   <span data-ttu-id="32591-160">これで、クラスは X++ ソース コードに入れ子にできます。</span><span class="sxs-lookup"><span data-stu-id="32591-160">Classes can now be nested in X++ source code.</span></span> <span data-ttu-id="32591-161">入れ子になったクラスはフォーム内 (FormRun を拡張するクラスなど) でのみ使用でき、コントロール、データ ソースまたはデータ フィールドを表します。</span><span class="sxs-lookup"><span data-stu-id="32591-161">Nested classes are available only inside forms (such as a class that extends FormRun) to represent controls, data sources, or data fields.</span></span>

## <a name="backward-incompatible-changes-to-x"></a><span data-ttu-id="32591-162">X++ への後方互換性のない変更</span><span class="sxs-lookup"><span data-stu-id="32591-162">Backward-incompatible changes to X++</span></span>
<span data-ttu-id="32591-163">従来のカスタム X++ ソース コードに対応する変更が必要な X++ には、変更点がいくつかあります。</span><span class="sxs-lookup"><span data-stu-id="32591-163">There are a few changes to X++ that require corresponding changes in legacy custom X++ source code.</span></span> <span data-ttu-id="32591-164">これらの変更内容のほとんどが、次の一覧にあります。</span><span class="sxs-lookup"><span data-stu-id="32591-164">Most of these changes are in the following list:</span></span>

-   <span data-ttu-id="32591-165">次のキーワードは、X++ 言語の一部ではなくなっており、使用するとコンパイル エラーが発生します。</span><span class="sxs-lookup"><span data-stu-id="32591-165">The following keywords are no longer part of the X++ language, and their use causes compilation errors:</span></span>
    -   `changeSite`
    -   `pause`
    -   `window`
-   <span data-ttu-id="32591-166">旧式 X++ では、クライアントまたはサーバーのいずれかを実行するメソッドを指定できました。</span><span class="sxs-lookup"><span data-stu-id="32591-166">In legacy X++, it was possible to designate a method to run either on the client or the server.</span></span> <span data-ttu-id="32591-167">これは不可能です。</span><span class="sxs-lookup"><span data-stu-id="32591-167">This is no longer possible.</span></span> <span data-ttu-id="32591-168">すべてのコンパイルされた X++ コードは、サーバー上の .NET CIL で実行されます。</span><span class="sxs-lookup"><span data-stu-id="32591-168">All compiled X++ code is executed as .NET CIL on the server.</span></span> <span data-ttu-id="32591-169">クライアント サイトまたはブラウザーで評価される X++ コードは存在しないため、*client* と *server* の 2 つのキーワードは無視されます。</span><span class="sxs-lookup"><span data-stu-id="32591-169">There is no longer any X++ code that is evaluated at the client site or in the browser, therefore, the two keywords, *client* and *server*, are now ignored.</span></span> <span data-ttu-id="32591-170">コンパイル エラーは発生しませんが、新しい X++ コードのいずれでも使用しないでください。</span><span class="sxs-lookup"><span data-stu-id="32591-170">Their use doesn't cause a compile error, but they should not be used in any new X++ code.</span></span>
-   <span data-ttu-id="32591-171">Microsoft Dynamics AX 2012 には、P コード対 CIL にコンパイルしたときに X++ が異なる動作をするいくつかの領域がありました。</span><span class="sxs-lookup"><span data-stu-id="32591-171">In Microsoft Dynamics AX 2012, there were a few areas where X++ behaved differently when compiled to p-code versus CIL.</span></span> <span data-ttu-id="32591-172">Dynamics 365 for Finance and Operations では、これらすべての領域が Microsoft Dynamics AX 2012 の CIL のときと同様に動作します。</span><span class="sxs-lookup"><span data-stu-id="32591-172">In Dynamics 365 for Finance and Operations, all these areas behave as they did in CIL in Microsoft Dynamics AX 2012.</span></span> <span data-ttu-id="32591-173">X++ p-code と CIL としての X+ との間の有意な行動上の相違は次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="32591-173">The significant behavioral differences between X++ p-code versus X+ as CIL were as follows:</span></span>
    -   <span data-ttu-id="32591-174">CIL では、`real `データ型が `System.Decimal` として表されます。</span><span class="sxs-lookup"><span data-stu-id="32591-174">In CIL, the `real `data type is represented as `System.Decimal`.</span></span> <span data-ttu-id="32591-175">これは、各 `real` の範囲と精度が p コードの場合と異なることを意味します。</span><span class="sxs-lookup"><span data-stu-id="32591-175">This means the range and precision for each `real` is different than it was under p-code.</span></span> <span data-ttu-id="32591-176">この変更は、.NET CIL が実行された時点で Microsoft Dynamics AX 2012 ですでに有効でした。</span><span class="sxs-lookup"><span data-stu-id="32591-176">This change was already in effect in Microsoft Dynamics AX 2012 when .NET CIL was run.</span></span>
    -   <span data-ttu-id="32591-177">1 つの全体配列を別の配列に割り当てることが P コード モードの値で実行されましたが、CIL モードでの参照が実行されます。</span><span class="sxs-lookup"><span data-stu-id="32591-177">An assignment of one entire array to another was performed in value in p-code mode, but it's performed by reference in CIL mode.</span></span>
    -   <span data-ttu-id="32591-178">`Global::runClassMethodIL` などの CIL ヘルパー メソッドは、関連性が無くなったため削除されました。</span><span class="sxs-lookup"><span data-stu-id="32591-178">CIL helper methods such as `Global::runClassMethodIL` have been removed, since they're no longer relevant.</span></span>
-   <span data-ttu-id="32591-179">**AOT** &gt; **Jobs** &gt; **MyJob** の意味にジョブの概念はありません。</span><span class="sxs-lookup"><span data-stu-id="32591-179">There is no concept of a job, in the sense of **AOT** &gt; **Jobs** &gt; **MyJob**.</span></span> <span data-ttu-id="32591-180">X++ メソッドをすばやく簡単に実行するには、`static Main` メソッドをクラスに追加し、そのクラスを Microsoft Visual Studio のプロジェクトのスタートアップ オブジェクト フォームとして設定します。</span><span class="sxs-lookup"><span data-stu-id="32591-180">To quickly and easily run an X++ method, you can still add in a `static Main` method to a class, and then set the class as the startup object form for the project in Microsoft Visual Studio.</span></span> <span data-ttu-id="32591-181">プロジェクトが実行されるときは、`Main`メソッドが実行されます。</span><span class="sxs-lookup"><span data-stu-id="32591-181">When the project is run, the `Main` method will be run.</span></span>


<a name="additional-resources"></a><span data-ttu-id="32591-182">その他のリソース</span><span class="sxs-lookup"><span data-stu-id="32591-182">Additional resources</span></span>
--------

[<span data-ttu-id="32591-183">C# で使用する Dynamics AX LINQ プロバイダー</span><span class="sxs-lookup"><span data-stu-id="32591-183">Dynamics AX LINQ Provider for use in C#</span></span>](linq-provider-c.md)

[<span data-ttu-id="32591-184">技術概念ガイド</span><span class="sxs-lookup"><span data-stu-id="32591-184">Technical Concepts Guide</span></span>](developer-home-page.md)




