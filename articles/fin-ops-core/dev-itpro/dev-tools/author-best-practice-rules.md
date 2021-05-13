---
title: ベスト プラクティス ルールを記述する
description: このトピックでは、メタデータと X++ コードの両方について、C# でベスト プラクティス ルールを作成する方法について説明します。
author: pvillads
ms.date: 11/03/2017
ms.topic: article
audience: Developer
ms.reviewer: rhaertle
ms.custom: 48071
ms.assetid: 4fe671c4-c556-4942-8570-307cf68ae0a7
ms.search.region: Global
ms.author: pvillads
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: fd19ae4fc02d4cedd731d4a7e60d10c476129a7d
ms.sourcegitcommit: e4992c57eea4c15ac052e9d65dddae625e3528f9
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/07/2021
ms.locfileid: "5865952"
---
# <a name="write-best-practice-rules"></a><span data-ttu-id="6f562-103">ベスト プラクティス ルールを記述する</span><span class="sxs-lookup"><span data-stu-id="6f562-103">Write best practice rules</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="6f562-104">このトピックでは、メタデータと X++ コードの両方について、C# でベスト プラクティス ルールを作成する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="6f562-104">This topic describes how you can author best practice rules in C#, for both metadata and X++ code.</span></span> <span data-ttu-id="6f562-105">ベスト プラクティス チェックは、コンパイラによって実行されます。</span><span class="sxs-lookup"><span data-stu-id="6f562-105">Best practice checks are run by the compiler.</span></span> <span data-ttu-id="6f562-106">それらは出荷コードで許容されない不都合なプラクティスをキャッチするために日単位ビルドで実行することができます。</span><span class="sxs-lookup"><span data-stu-id="6f562-106">You can run them in daily builds to catch objectionable practices that are unacceptable in shipping code.</span></span> <span data-ttu-id="6f562-107">この機能を使用して、アプリケーションに関する情報を収集するための簡単なツールを作成することもできます。</span><span class="sxs-lookup"><span data-stu-id="6f562-107">The features can also be used to author simple one-of tools to gather information about the application.</span></span>

<span data-ttu-id="6f562-108">また、ベスト プラクティス ルールを使用して、アプリケーションに関する情報を収集する単純なツールを作成することもできます。</span><span class="sxs-lookup"><span data-stu-id="6f562-108">You can also use best practice rules to author simple tools that gather information about your application.</span></span> <span data-ttu-id="6f562-109">フレームワークは、XLNT (X++ LaNguage ツールキットの省略形) と呼ばれるマネージド フレームワークの上に構築されています。</span><span class="sxs-lookup"><span data-stu-id="6f562-109">The framework is built on top of a managed framework called XLNT (shorthand for X++ LaNguage Toolkit).</span></span> <span data-ttu-id="6f562-110">フレームワークを使用して、X++ コードから情報を抽出し、および変更するカスタム ツールを構築できます。</span><span class="sxs-lookup"><span data-stu-id="6f562-110">You can use the framework to build custom tools that extract information from, and modify, X++ code.</span></span> <span data-ttu-id="6f562-111">2 種類のベスト プラクティス ルールがあります: メタデータを処理するルールとソース コードを処理するルール。</span><span class="sxs-lookup"><span data-stu-id="6f562-111">There are two types of best practice rules: rules that deal with metadata and rules that deal with source code.</span></span>

## <a name="code-best-practice-framework"></a><span data-ttu-id="6f562-112">コードのベスト プラクティス フレームワーク</span><span class="sxs-lookup"><span data-stu-id="6f562-112">Code Best Practice framework</span></span>

<span data-ttu-id="6f562-113">コード ベスト プラクティス フレームワーク (CBPF) を使用すると、X++ ソース コードを分析するための独自のツールを作成できます。</span><span class="sxs-lookup"><span data-stu-id="6f562-113">The Code Best Practice Framework (CBPF) enables you to write your own tools for analyzing X++ source code.</span></span> <span data-ttu-id="6f562-114">これらのルールは、X++ ソース コードに問題があると判断するものを診断します。</span><span class="sxs-lookup"><span data-stu-id="6f562-114">These rules diagnose things that you consider to be problems with X++ source code.</span></span> <span data-ttu-id="6f562-115">このセクションでは、ベスト プラクティス機能の基礎について説明します。</span><span class="sxs-lookup"><span data-stu-id="6f562-115">This section describes the foundation of the Best Practice functionality.</span></span> <span data-ttu-id="6f562-116">この情報は、独自のルールの作成について詳しく説明する後のセクションの理解に役立ちます。</span><span class="sxs-lookup"><span data-stu-id="6f562-116">This information is helpful for understanding the later sections that describe creating your own rules in greater detail.</span></span> <span data-ttu-id="6f562-117">また、このドキュメントで示されているものよりも複雑なコード ルールを求める開発者にとっても便利です。</span><span class="sxs-lookup"><span data-stu-id="6f562-117">It is also helpful to developers who want to code rules that are more complex than those demonstrated in this document.</span></span> <span data-ttu-id="6f562-118">CBPF APIにより、インフラストラクチャの問題を処理しなくても表現するルールに焦点を絞ることができます。</span><span class="sxs-lookup"><span data-stu-id="6f562-118">The CBPF API lets you focus on the rule you are expressing, without having to deal with infrastructure issues.</span></span> <span data-ttu-id="6f562-119">トークンを読み取り、それらを組み合わせて分かり易いものを作成する必要はありません。</span><span class="sxs-lookup"><span data-stu-id="6f562-119">You don't need to read tokens and piece them together to create something intelligible from them.</span></span> <span data-ttu-id="6f562-120">代わりに、CBPF は次のパーツを提供します。</span><span class="sxs-lookup"><span data-stu-id="6f562-120">Instead, the CBPF provides the following parts:</span></span>

- <span data-ttu-id="6f562-121">X++ ソース コードから抽象構文ツリー (AST) を構築するパーサー。</span><span class="sxs-lookup"><span data-stu-id="6f562-121">A parser that builds an Abstract Syntax Tree (AST) from X++ source code.</span></span>
- <span data-ttu-id="6f562-122">X++ コードでパスの順序を実行するパイプライン。</span><span class="sxs-lookup"><span data-stu-id="6f562-122">A pipeline that runs a sequence of passes over the X++ code.</span></span>
- <span data-ttu-id="6f562-123">作成済みのパスの数。</span><span class="sxs-lookup"><span data-stu-id="6f562-123">A number of prebuilt passes.</span></span> <span data-ttu-id="6f562-124">最初のパスは、ソース コードの解析です。</span><span class="sxs-lookup"><span data-stu-id="6f562-124">The first pass is the parsing of the source code.</span></span>
- <span data-ttu-id="6f562-125">メタデータを読み取るインフラストラクチャ。</span><span class="sxs-lookup"><span data-stu-id="6f562-125">Infrastructure to read metadata.</span></span>

<span data-ttu-id="6f562-126">ルールは AST に基づいているために、ルールの作成を始める前にその概念を理解する必要があります。</span><span class="sxs-lookup"><span data-stu-id="6f562-126">Because rules are based on ASTs, it is important to understand that concept before starting to write rules.</span></span>

### <a name="the-parser-and-asts"></a><span data-ttu-id="6f562-127">パーサーと AST</span><span class="sxs-lookup"><span data-stu-id="6f562-127">The parser and ASTs</span></span>

<span data-ttu-id="6f562-128">パーサーは、X++ コードを読み込み、それに重大な構文エラーが含まれていない場合は、それから AST を生成します。</span><span class="sxs-lookup"><span data-stu-id="6f562-128">The parser reads  X++ code and produces an AST from it if it does not contain egregious syntax errors.</span></span> <span data-ttu-id="6f562-129">パーサーは、組み込みのエラー回復スキームを持つため、大部分の構文エラーから適切に回復できます。</span><span class="sxs-lookup"><span data-stu-id="6f562-129">The parser has a built-in error recovery scheme, so it can recover from most syntax errors reasonably well.</span></span> <span data-ttu-id="6f562-130">構文エラーが発生するときは、パーサーはセミコロンに到達するまで記号を読み取り、セミコロンが正しい記号となる状態に到達するまでその状態をアンスタックして AST の構築を試みます。</span><span class="sxs-lookup"><span data-stu-id="6f562-130">When a syntax error happens, the parser will read symbols until it encounters a semicolon, and then try to building the AST by unstacking its state until it reaches a state where a semicolon is a correct symbol.</span></span> <span data-ttu-id="6f562-131">さらに、パーサーは構文エラーが発生したときに、適切な記号のセットを提案できます。</span><span class="sxs-lookup"><span data-stu-id="6f562-131">In addition, the parser is able to suggest the correct set of symbols when a syntax error occurs.</span></span> <span data-ttu-id="6f562-132">パーサーは、API のコンシューマーと直接対話するようにはなっていませんが、ユーザーの介入なしに機能するブラック ボックスと見なす必要があります。</span><span class="sxs-lookup"><span data-stu-id="6f562-132">The parser is not intended to be directly interacted with by consumers of the API, but should be considered a black box that works without user intervention.</span></span> <span data-ttu-id="6f562-133">パーサーはソース コードの言語構成を認識すると、AST を構築します。</span><span class="sxs-lookup"><span data-stu-id="6f562-133">As the parser recognizes the language constructs in the source code, it builds an AST.</span></span> <span data-ttu-id="6f562-134">AST は、それらが表す X++ コンポーネントの抽象化であるノードで構成されます。</span><span class="sxs-lookup"><span data-stu-id="6f562-134">The AST consists of nodes that are abstractions of the X++ artifact they represent.</span></span> <span data-ttu-id="6f562-135">この概念を、いくつかの AST ノードを表示することによって、下図に示します。</span><span class="sxs-lookup"><span data-stu-id="6f562-135">We will illustrate the concept by showing a few AST nodes below:</span></span>

```xpp
public abstract class Statement : Ast
{
    /// <summary>
    /// Gets or sets the comments in the statement
    /// </summary>
    public string Comments { get; set; }

    public abstract string ToString(int indent);
}
```

<span data-ttu-id="6f562-136">**ステートメント** クラスは、抽象です。"ステートメント" のインスタンスを作成しても意味がありません。</span><span class="sxs-lookup"><span data-stu-id="6f562-136">The **Statement** class is abstract, because it doesn't make sense to instantiate a ”statement”.</span></span> <span data-ttu-id="6f562-137">**if** および **while** ステートメントなどのコンクリート派生クラスのみのインスタンスを作成することができます。</span><span class="sxs-lookup"><span data-stu-id="6f562-137">Only concrete derived classes, like **if** and **while** statements, can be instantiated.</span></span> <span data-ttu-id="6f562-138">コメント プロパティはこの基準クラスに配置されるため、すべての派生クラスに適用されます。</span><span class="sxs-lookup"><span data-stu-id="6f562-138">Since the Comments property is placed on this base class, it applies to all derived classes.</span></span> <span data-ttu-id="6f562-139">つまり、すべてのステートメントはステートメントの前にコメントを持つことができます。</span><span class="sxs-lookup"><span data-stu-id="6f562-139">In other words, all statements can have comments preceding the statement.</span></span> <span data-ttu-id="6f562-140">コメントは、特定のプロパティを使用してアクセスできます。</span><span class="sxs-lookup"><span data-stu-id="6f562-140">The comments are accessible through the given property.</span></span> <span data-ttu-id="6f562-141">X++ にはさまざまな多数の種類のステートメントがあり、それぞれは上記の抽象 **ステートメント** クラスから 1 つ以上の手順で派生したクラスによって記述されます。</span><span class="sxs-lookup"><span data-stu-id="6f562-141">There are many different kinds of statement in X++ and each one is described by a class derived in one or more steps from the abstract **Statement** class shown above.</span></span> <span data-ttu-id="6f562-142">次の例は、**while** ステートメントの定義を示しています。</span><span class="sxs-lookup"><span data-stu-id="6f562-142">The following example shows the definition of a **while** statement.</span></span>

```xpp
public class WhileStatement : Statement
{
    /// <summary>
    /// Gets or sets the while condition.
    /// </summary>
    public Expression Condition { get; set; }

    /// <summary>
    /// Gets or sets the constituent while statement.
    /// </summary>
    public Statement Statement { get; set; }
}
```

<span data-ttu-id="6f562-143">**while** ステートメントは条件 (式) と、条件が true と評価される限り実行される構成ステートメントで構成されています。</span><span class="sxs-lookup"><span data-stu-id="6f562-143">The **while** statement consists of the condition (an expression) and the constituent statement, that is executed as long as the condition evaluates to true.</span></span> <span data-ttu-id="6f562-144">パーサーは、表現された成果物が開始および終了するソース コードの位置 (つまり、その範囲) を保持します。</span><span class="sxs-lookup"><span data-stu-id="6f562-144">The parser will maintain the source code positions where the represented artifact starts and ends (that is, its extent).</span></span> <span data-ttu-id="6f562-145">AST がスキャンされるので、個々のノードに情報を追加すると便利です。</span><span class="sxs-lookup"><span data-stu-id="6f562-145">As the ASTs are traversed, it may be useful to add information to the individual nodes.</span></span> <span data-ttu-id="6f562-146">たとえば、すべての式にはタイプがあります。</span><span class="sxs-lookup"><span data-stu-id="6f562-146">For example, every expression has a type.</span></span> <span data-ttu-id="6f562-147">タイプの互換性の問題を診断するためにツリーがスキャンされるので、個々のノードにその情報を配置できるようになると便利です。</span><span class="sxs-lookup"><span data-stu-id="6f562-147">As the tree is traversed to diagnose type compatibility problems it becomes useful to be able to place that information on the individual node.</span></span> <span data-ttu-id="6f562-148">各要件の AST ノードを変更する必要はなく、各ノードに名前/値の組み合わせを提供するために使用するプロパティ コレクションがあります。</span><span class="sxs-lookup"><span data-stu-id="6f562-148">Rather than having to modify the AST nodes for each requirement, there is a property collection that can be used to provide name/value pairs to each node.</span></span> <span data-ttu-id="6f562-149">各 AST ノードには、ノードの高精度の文字列表現を戻す **ToString** 方法があります。これはシナリオのデバッグに役立ちます。</span><span class="sxs-lookup"><span data-stu-id="6f562-149">Each AST node has a **ToString** method that will return a high fidelity string representation of the node, which is useful in debugging scenarios.</span></span>

### <a name="the-astsweeper-class"></a><span data-ttu-id="6f562-150">AstSweeper クラス</span><span class="sxs-lookup"><span data-stu-id="6f562-150">The AstSweeper class</span></span>

<span data-ttu-id="6f562-151">AstSweeper は、指定された AST インスタンスに ビジター パターンを適用します。</span><span class="sxs-lookup"><span data-stu-id="6f562-151">The AstSweeper applies a visitor pattern to the AST instance that it is given.</span></span> <span data-ttu-id="6f562-152">ビジター パターンを使用すると、プログラマーは、ユーザーがノード上で実行する操作 (つまり、コードに関する論理推論) から基礎となるデータ構造 (つまり、AST) を分離することが可能になります。</span><span class="sxs-lookup"><span data-stu-id="6f562-152">The visitor pattern allows the programmer to separate the underlying data structure (that is, the AST) from the operations that the user wants to perform on the nodes (that is, the logic reasoning about the code).</span></span> <span data-ttu-id="6f562-153">**AstSweeper** クラスには、AST ノード タイプごとに仮想メソッドがあり、AST の構造の指示に従って呼び出します。</span><span class="sxs-lookup"><span data-stu-id="6f562-153">The **AstSweeper** class has a virtual method for each of the AST node types, and it will call them as directed by the structure of the AST.</span></span> <span data-ttu-id="6f562-154">次の例では、スウィーパーの動作を示しています。</span><span class="sxs-lookup"><span data-stu-id="6f562-154">The following examples show how the sweeper works.</span></span> <span data-ttu-id="6f562-155">わかりやすくするためにいくつかの詳細が除外されました。</span><span class="sxs-lookup"><span data-stu-id="6f562-155">Some details have been omitted for clarity.</span></span>

```xpp
/// <summary>The AST sweeper visits each node in the AST</summary>
/// <typeparm name="TReturn">The type returned by each of the sweeper methods</typeparm>
/// <typeparm name="TPayload">
/// The type of the payload passed to each of the sweeper methods
/// </typeparm>
public class AstSweeper<TReturn, TPayload> where TReturn : class
{
    protected virtual TReturn VisitStatement(TPayload o, Statement statement)
    {
        var compoundStatement = statement as CompoundStatement;
        if (compoundStatement != null)
        {
            return this.VisitCompoundStatement(o, compoundStatement);
        }

        var whileStatement = statement as WhileStatement;
        if (whileStatement != null)
        {
            return this.VisitWhileStatement(o, whileStatement);
        }
    }

    protected virtual TReturn VisitWhileStatement(TPayload o, WhileStatement statement)
    {
        this.VisitExpression(statement.Condition);
        this.VisitStatement(statement.Statement);

        return null;
    }
}
```

<span data-ttu-id="6f562-156">特定の AST ノードを扱う仮想メソッドの名前は、Visit が先頭に追加された AST クラスの名前です。</span><span class="sxs-lookup"><span data-stu-id="6f562-156">The name of the virtual method handling a particular AST node is the name of the AST class prepended with Visit.</span></span> <span data-ttu-id="6f562-157">そのパラメーターは、参照するノードと、呼び出されたときすべての参照者に渡すことのできるペイロードです。</span><span class="sxs-lookup"><span data-stu-id="6f562-157">The parameters are the node to visit and a payload that may be passed to all the visitors as they are called.</span></span> <span data-ttu-id="6f562-158">この方法で、スウィーパーは深さ優先トラバーサルで渡される AST のノードのそれぞれに対して 1 回仮想メソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="6f562-158">In this way, the sweeper will call the virtual method once for each and every one of the nodes in the AST that is passed to it in a depth-first traversal.</span></span> <span data-ttu-id="6f562-159">ペイロード パラメーターを使用して、必要に応じて、各ノードに情報 (たとえば、シンボル テーブル) を渡すことができます。</span><span class="sxs-lookup"><span data-stu-id="6f562-159">The payload parameter can be used to pass information (for example, a symbol table) to each node as required.</span></span> <span data-ttu-id="6f562-160">開発者は、AstSweeper クラスから派生したクラスを構築し、特定の関心のあるメソッドを上書きします。</span><span class="sxs-lookup"><span data-stu-id="6f562-160">Developers will build classes derived from the AstSweeper class, overriding the methods of particular interest to them.</span></span>

#### <a name="example"></a><span data-ttu-id="6f562-161">例</span><span class="sxs-lookup"><span data-stu-id="6f562-161">Example</span></span>

<span data-ttu-id="6f562-162">X++ コーディング ガイドラインに準拠するため、アンダースコア文字で始まるパラメーター名の割合を決定する必要があるとします。</span><span class="sxs-lookup"><span data-stu-id="6f562-162">Suppose you need to determine the percentage of parameter names starting with an underscore character, thus conforming to the X++ coding guidelines.</span></span> <span data-ttu-id="6f562-163">次に、パラメーター数とアンダー スコアで始まるパラメーター数を計算したロジックを使用して、**AstSweeper** から派生するクラスを記述します。</span><span class="sxs-lookup"><span data-stu-id="6f562-163">You would then write a class deriving from the **AstSweeper** class with logic that calculated the number of parameters and the number of parameters starting with underscore.</span></span> <span data-ttu-id="6f562-164">次の例は、このコードを示しています。</span><span class="sxs-lookup"><span data-stu-id="6f562-164">The following example shows this code.</span></span>

```xpp
public class ParameterCounter : AstSweeper<object, object>
{
    /// <summary>
    /// The parameter count maintained as the methods are encountered.
    /// </summary>
    public int ParameterCount { get; set; }

    /// <summary>
    /// The number of parameters that start with an underscore character.
    /// </summary>
    public int UnderscoredParameters { get; set; }

    /// <summary>
    /// Visits the method parameters.
    /// </summary>
    /// <param name="o">The payload. Not used in this scenario.</param>
    /// <param name="parameters">The list of parameters to visit.</param>
    /// <returns>The method parameters.</returns>
    protected override object VisitMethodParameters(object o,
        IEnumerable<ParameterDeclaration> parameters)
    {
        this.ParameterCount += parameters.Count();
        this.UnderscoredParameters += parameters
            .Where(p => p.Name.StartsWith("_")).Count();

        return null;
    }
}
```

<span data-ttu-id="6f562-165">この場合、集計はクラス スコープで定義されている **ParametersCount** および **UnderscoredParameters** プロパティで維持されます。</span><span class="sxs-lookup"><span data-stu-id="6f562-165">In this case, the tally is maintained in the **ParametersCount** and **UnderscoredParameters** properties that are defined in the class scope.</span></span> <span data-ttu-id="6f562-166">もう 1 つの均等に有効なアプローチでは、すべての **Visit** メソッドに渡されるペイロードにこの情報を渡すことができます。</span><span class="sxs-lookup"><span data-stu-id="6f562-166">Another equally valid approach would be to pass this information into the payload that is passed to all the **Visit** methods.</span></span> <span data-ttu-id="6f562-167">ほとんどの場合、ユーザーは **Visit** メソッドがアクセスしたノード以下のすべてのノードに対して呼び出されることを確認するために、オーバーライドされたメソッドから **super()** を無条件に呼び出す必要があります。</span><span class="sxs-lookup"><span data-stu-id="6f562-167">In most cases, the user should unconditionally call **super()** from the overridden method to make sure that the **Visit** methods are called for all nodes below the one being visited.</span></span> <span data-ttu-id="6f562-168">上記の場合、相違が生じないため、AST ツリー トラバーサルを簡略化することでパフォーマンスを向上します。</span><span class="sxs-lookup"><span data-stu-id="6f562-168">In the case above, it does not make a difference so we opt to improve performance by pruning the AST tree traversal.</span></span>

### <a name="writing-code-for-best-practice-rules"></a><span data-ttu-id="6f562-169">ベスト プラクティス ルールのコードを記述</span><span class="sxs-lookup"><span data-stu-id="6f562-169">Writing code for Best Practice rules</span></span>

<span data-ttu-id="6f562-170">ビジネス ルールを作成するには :</span><span class="sxs-lookup"><span data-stu-id="6f562-170">To author a business rule:</span></span>

1. <span data-ttu-id="6f562-171">AST のプロパティに関して診断したい状況を定義します。</span><span class="sxs-lookup"><span data-stu-id="6f562-171">Define the situation you want to diagnose in terms of properties of the AST.</span></span> <span data-ttu-id="6f562-172">解析を実行できる **Visit\*** メソッドを記述できます。</span><span class="sxs-lookup"><span data-stu-id="6f562-172">You will write **Visit\*** methods that can do the analysis.</span></span>
2. <span data-ttu-id="6f562-173">エラー状態が検出されたとき、診断メッセージを生成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="6f562-173">When the error condition has been found, a diagnostic message must be generated.</span></span> <span data-ttu-id="6f562-174">この目的のために使用される API があります。基本的には、各診断メッセージの定型コードを書く必要があります。</span><span class="sxs-lookup"><span data-stu-id="6f562-174">There is an API that is used for this purpose; basically you need to write some boilerplate code for each diagnostic message.</span></span>
3. <span data-ttu-id="6f562-175">ユーザーが作業にルールを含めるかどうか、またそう指定された場合に実行するかどうかを決められるように、新しいベスト プラクティス ルールを残りのフレームワークにフックする必要があります。</span><span class="sxs-lookup"><span data-stu-id="6f562-175">You need to hook your new best practice rule into the rest of the framework, so the user can decide whether or not to include your rule and to run it if so directed.</span></span>

### <a name="create-a-best-practice-rules-project-in-visual-studio"></a><span data-ttu-id="6f562-176">Visual Studio でのベスト プラクティス ルール プロジェクトの作成</span><span class="sxs-lookup"><span data-stu-id="6f562-176">Create a best practice rules project in Visual Studio</span></span>

<span data-ttu-id="6f562-177">このチュートリアルでは、次のシナリオを考えてみましょう。</span><span class="sxs-lookup"><span data-stu-id="6f562-177">In this walkthrough, we imagine the following scenario:</span></span>

- <span data-ttu-id="6f562-178">一部のメソッドには、コードを記述した個人の名前を指定する作成者属性が用意されています。</span><span class="sxs-lookup"><span data-stu-id="6f562-178">Some methods are adorned with an Author attribute that provides the name of the individual who wrote the code.</span></span> <span data-ttu-id="6f562-179">この属性は、そのメソッドを含むスタック トレースが表示されたときに指摘する人を見つけるときに便利です。</span><span class="sxs-lookup"><span data-stu-id="6f562-179">The attribute is useful when finding who to point the finger at when stack traces containing that method appear.</span></span>
- <span data-ttu-id="6f562-180">開発者の重要な納期があるので、一覧表示された開発者の名前は静的である必要があります。</span><span class="sxs-lookup"><span data-stu-id="6f562-180">Since we have a significant turnaround of developers, the names of the developers listed cannot be static.</span></span> <span data-ttu-id="6f562-181">作成者属性で使用されている名前を検索し、現在の開発者の名前のリストと照合します。</span><span class="sxs-lookup"><span data-stu-id="6f562-181">We want to find the names that are used in the Author attributes, and match them against a list of names of current developers.</span></span>

<span data-ttu-id="6f562-182">作成者属性クラスは、次のように定義されます。</span><span class="sxs-lookup"><span data-stu-id="6f562-182">The author attribute class is defined as:</span></span>

```xpp
class AuthorAttribute extends SysAttribute
{
    private str theAuthor;

    public void new(str _author) 
    {
        this.theAuthor = _author;
    }
}
```

<span data-ttu-id="6f562-183">実稼働コードでは、パラメーターの値などに関する主な前提を検証するために、ドキュメント コメントとアサーションを挿入します。このチュートリアルではコードをわかりやすく書くため、これらの手順を省略します。</span><span class="sxs-lookup"><span data-stu-id="6f562-183">In production code, we would put in documentation comments and assertions to validate key assumptions about parameter values etc. For the sake of clarity, we omit these steps in this walkthrough, where the code is written for clarity.</span></span> <span data-ttu-id="6f562-184">アーカイブするものに対してステージを設定したので、Visual Studio を開始してベスト プラクティス ルール プロジェクトを作成することができます。</span><span class="sxs-lookup"><span data-stu-id="6f562-184">Now that we have set the stage for what we want to achieve, we can start up Visual Studio and create a best practice rules project.</span></span> <span data-ttu-id="6f562-185">ルールの目的を適切に伝えるわかりやすい名前を入力してください。Visual Studio は、いくつかのソース コード スニペットおよびプロジェクト参照が設定されたプロジェクトを作成します。</span><span class="sxs-lookup"><span data-stu-id="6f562-185">Provide a meaningful name that properly conveys what the rules are intended to do: Visual Studio creates a project with some source code snippets and project references set up.</span></span> <span data-ttu-id="6f562-186">このソース コードを自分のコードの出発点として使用することにより、時間を大幅に節約することができます。</span><span class="sxs-lookup"><span data-stu-id="6f562-186">You can save considerable time by using this source code as a starting point for your own code.</span></span> <span data-ttu-id="6f562-187">既定の例には、メソッド名に "Microsoft" という語を禁止するルール (著作権上の理由から)、および名前に特定の文字を禁止するというメタデータ ベースのルールが含まれています。</span><span class="sxs-lookup"><span data-stu-id="6f562-187">The pre-canned example contains rules that prohibit the word “Microsoft” in any method names (presumably for copyright reasons) and a metadata-based rule prohibiting certain characters in names.</span></span> <span data-ttu-id="6f562-188">ここではメタデータ チェックを行いませんので、プロジェクトから InvalidCharactersDiagnosticItem.cs ファイルと DemoMetadataCheck.cs ファイルを削除できます。</span><span class="sxs-lookup"><span data-stu-id="6f562-188">Since we are not concerned with the metadata checks for now, you can delete the InvalidCharactersDiagnosticItem.cs and DemoMetadataCheck.cs files from the project.</span></span> <span data-ttu-id="6f562-189">また、Microsoft の名前チェックに興味がないので、DemoAST クラスの VisitMethod メソッドのコンテンツを削除してください。</span><span class="sxs-lookup"><span data-stu-id="6f562-189">Also, since we are not interested in the Microsoft name check, go ahead and delete the content of the VisitMethod method in the DemoAST class.</span></span> <span data-ttu-id="6f562-190">最初に行う必要があるのは、特定のメソッドの作成者属性が 1 つ以上あるかどうかを調べることです。</span><span class="sxs-lookup"><span data-stu-id="6f562-190">The first thing we need to do is to find out if there are one or more Author attributes for a particular method.</span></span> <span data-ttu-id="6f562-191">このメソッド タイプ (これは、VisitMethod メソッドにパラメーターとして渡されます) に AttributeList タイプの属性プロパティが含まれていることがわかります。</span><span class="sxs-lookup"><span data-stu-id="6f562-191">You will notice that the Method type (that is passed as a parameter to the VisitMethod method) has an Attributes property of type AttributeList.</span></span> <span data-ttu-id="6f562-192">これを使用して、Author 属性がこのメソッドで定義されるかどうかを確認しましょう。</span><span class="sxs-lookup"><span data-stu-id="6f562-192">Let's use it to see if any Author attributes are defined on this method:</span></span>

```xpp
protected override object VisitMethod(BestPracticeCheckerPayload payload, Method method)
{
    var names = new List<string>();
    foreach (var attribute in method.Attributes.Attributes)
    {
        if (string.Compare(attribute.Name, "Author",
            ignoreCase: true, culture: CultureInfo.InvariantCulture) == 0)
        {
            var authorNameLiteral = attribute.Parameters.First().Literal as StringAttributeLiteral;
            // The name contains quotes (either single or double). Get rid of those
            var authorName = authorNameLiteral.Value.Trim('\'', '"');
            names.Add(authorName);
        }
    }

    // More to come...
    return null;
}
```

<span data-ttu-id="6f562-193">この時点であらゆる属性をループし作成者名、つまり作成者属性に最初のパラメータとして提供される名前のリストを収集しています。</span><span class="sxs-lookup"><span data-stu-id="6f562-193">At this point we have looped through any attributes, and collected a list of author names, that is names that are provided as the first parameters to the Author attributes.</span></span> <span data-ttu-id="6f562-194">現在は、リストを許可された作成者のリストと比較する必要があり、静的リストで維持しています。</span><span class="sxs-lookup"><span data-stu-id="6f562-194">Now we need to compare the list against a list of acceptable authors, that we maintain in a static list.</span></span> <span data-ttu-id="6f562-195">リストに記載されていない作成者が指定されるときはいつでも、適切な診断メッセージを発行する必要があります。</span><span class="sxs-lookup"><span data-stu-id="6f562-195">Whenever an author is provided that is not mentioned in the list we need to issue an appropriate diagnostic message.</span></span> <span data-ttu-id="6f562-196">現時点では、次のようなものがあります。</span><span class="sxs-lookup"><span data-stu-id="6f562-196">At this time, we have something like:</span></span>

```xpp
public class AuthorListRule : BestPracticeAstChecker<BestPracticeCheckerPayload>
{
    private static HashSet<string> authorlist = new HashSet<string>()
    {
        "Alan Kay", "John von Neuman", "C.A.R. Hoare"
    };

    public AuthorListRule() : base()
    {
    }

    protected override object VisitMethod(BestPracticeCheckerPayload payload, Method method)
    {
        var names = new List<string>();
        foreach (var attribute in method.Attributes.Attributes)
        {
            if (string.Compare(attribute.Name, "Author",
                ignoreCase: true, culture: CultureInfo.InvariantCulture) == 0)
            {
                var authorNameLiteral = attribute.Parameters.First().Literal as StringAttributeLiteral;
                // The name contains quotes (either single or double). Get rid of those
                var authorName = authorNameLiteral.Value.Trim('\'', '"');
                names.Add(authorName);
            }
        }

        foreach (var name in names)
        {
            if (!authorlist.Contains(name))
            {
                // TODO: Add a diagnostic message
            }
        }
        return null;
    }
}
```

<span data-ttu-id="6f562-197">つまり、ルールの違反についてユーザーに通知するために診断メッセージを作成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="6f562-197">In other words, we need to create a diagnostic message to let the user know about the transgression of the rule.</span></span> <span data-ttu-id="6f562-198">前述のように、ビジターの基本実装を呼び出すことが重要です。メソッドに含まれるすべてのノードのビジター メソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="6f562-198">As noted before, it is important to call the base implementation of your visitor, which will then call visitor methods for all the nodes that are contained in the method.</span></span> <span data-ttu-id="6f562-199">ただし、この場合は、作成者属性がリストにあるかを判断した後の詳しい操作は行うことを望みません。</span><span class="sxs-lookup"><span data-stu-id="6f562-199">However, in this case, we do not want to do any further processing once we have determined if the author attribute is on the list.</span></span>

### <a name="add-a-class-for-the-diagnostic-message"></a><span data-ttu-id="6f562-200">診断メッセージのクラスの追加</span><span class="sxs-lookup"><span data-stu-id="6f562-200">Add a class for the diagnostic message</span></span>

<span data-ttu-id="6f562-201">プロジェクトにはすでにエラー メッセージの定型コードが含まれているため、ルールに違反した場合に返される診断メッセージを作成するための出発点として使用します。</span><span class="sxs-lookup"><span data-stu-id="6f562-201">The project already includes boilerplate code for an error message, so we will use that as our starting point to create the diagnostic message that will be returned if the rule is violated.</span></span> <span data-ttu-id="6f562-202">各メッセージは、独自のクラスとして実装されます。</span><span class="sxs-lookup"><span data-stu-id="6f562-202">Each message is implemented as a class of its own.</span></span> <span data-ttu-id="6f562-203">各エラー メッセージは、コード化された文脈情報を任意の量で有することができます。</span><span class="sxs-lookup"><span data-stu-id="6f562-203">Each error message may have any amount of contextual information encoded into it.</span></span> <span data-ttu-id="6f562-204">この場合、コンテキスト情報は一覧にない作成者の名前です。</span><span class="sxs-lookup"><span data-stu-id="6f562-204">In this case, the contextual information is the name of the author that is not found in the list.</span></span> <span data-ttu-id="6f562-205">「プロジェクトでそのファイルを開き、文字列を追加します」というメッセージをメッセージ リソース ファイルに追加することから開始します。</span><span class="sxs-lookup"><span data-stu-id="6f562-205">We will start by adding the message to the messages resource file: Open that file in the project and add a string to it.</span></span> <span data-ttu-id="6f562-206">AuthorNotCurrent という名前 (エラー モニカーとも呼ばれます) を使用します。</span><span class="sxs-lookup"><span data-stu-id="6f562-206">We will use the name (also known as the error moniker) AuthorNotCurrent.</span></span> <span data-ttu-id="6f562-207">‘{0}’ 文字列はコンテキスト情報のプレースホルダで、この場合、リストに含まれていない作成者の名前です。</span><span class="sxs-lookup"><span data-stu-id="6f562-207">The ‘{0}’ string is a placeholder for the contextual information, in this case the name of the author who is not in the list.</span></span> <span data-ttu-id="6f562-208">エラー メッセージに表示される実際のテキストに加えて、ルールの説明を含む文字列もあります。</span><span class="sxs-lookup"><span data-stu-id="6f562-208">In addition to the actual text that will appear in the error message, there is also a string containing a description of the rule.</span></span> <span data-ttu-id="6f562-209">この情報は、Visual Studio 内でベスト プラクティス ダイアログに表示され、ユーザーがシステムで有効にできるルールを決定できるように設計されています。</span><span class="sxs-lookup"><span data-stu-id="6f562-209">This information is shown in the best practice dialog within Visual Studio and is designed to help the user decide which rules to enable on the system.</span></span> <span data-ttu-id="6f562-210">診断メッセージのクラスを作成し、**AuthorNotCurrentDiagnosticItem.cs** という名前を付けます。</span><span class="sxs-lookup"><span data-stu-id="6f562-210">Create a class for the diagnostic message, and call it **AuthorNotCurrentDiagnosticItem.cs**.</span></span> <span data-ttu-id="6f562-211">Add the following code inspired from the **NotAllowedWordDiagnosticItem** クラスから基づいた次のコードを追加します。</span><span class="sxs-lookup"><span data-stu-id="6f562-211">Add the following code inspired from the **NotAllowedWordDiagnosticItem** class.</span></span>

```xpp
namespace CompareAuthorsToList
{
    using System;
    using System.Collections.Generic;
    using System.Runtime.Serialization;
    using System.Xml.Linq;
    using Microsoft.Dynamics.AX.Metadata.XppCompiler;

    [DataContract]
    public class AuthorNotCurrentDiagnosticItem : CustomDiagnosticItem
    {
        private const string AuthorNotCurrentKey = "Author";
        public const string DiagnosticMoniker = "AuthorNotCurrent";

        public AuthorNotCurrentDiagnosticItem(string path, string elementType, TextPosition textPosition, string author)
            : base(path, elementType, textPosition, DiagnosticType.BestPractices, Severity.Warning, DiagnosticMoniker, Messages.AuthorNotCurrent, author)
        {
            this.AuthorNotCurrent = author;
        }

        public AuthorNotCurrentDiagnosticItem(Stack<Ast> context, TextPosition textPosition, string author)
            : base(context, textPosition, DiagnosticType.BestPractices, Severity.Warning, DiagnosticMoniker, Messages.AuthorNotCurrent, author)
        {
            this.AuthorNotCurrent = author;
        }

        // Serialization support
        public AuthorNotCurrentDiagnosticItem(XElement element)
            : base(element)
        {
        }

        [DataMember]
        public string AuthorNotCurrent { get; private set; }

        /// <summary>
        /// Hydrate the diagnostic item from the given XML element.
        /// </summary>
        /// <param name="itemSpecificNode">The XML element containing the diagnostic.</param>
        protected override void ReadItemSpecificFields(System.Xml.Linq.XElement itemSpecificNode)
        {
            this.AuthorNotCurrent = base.ReadCustomField(itemSpecificNode, AuthorNotCurrentKey);
        }

        /// <summary>
        /// Write the state into the given XML element.
        /// </summary>
        /// <param name="itemSpecificNode">The element into which the state is persisted.</param>
        protected override void WriteItemSpecificFields(System.Xml.Linq.XElement itemSpecificNode)
        {
            this.WriteCustomField(itemSpecificNode, AuthorNotCurrentKey, this.AuthorNotCurrent);
        }
    }
}
```

<span data-ttu-id="6f562-212">診断メッセージは消費の準備ができています。</span><span class="sxs-lookup"><span data-stu-id="6f562-212">The diagnostic message is ready for consumption.</span></span> <span data-ttu-id="6f562-213">実行する必要がある簿記は 1 つだけです。このルールは、潜在的にどの診断を行うかを宣言的に公表する必要があります。</span><span class="sxs-lookup"><span data-stu-id="6f562-213">There is just one piece of bookkeeping that needs to be done; the rule needs to publish declaratively which diagnostics it potentially issues.</span></span> <span data-ttu-id="6f562-214">ルールに戻り、新しい診断メッセージを反映するように BestPracticeRule 属性を変更します。</span><span class="sxs-lookup"><span data-stu-id="6f562-214">Go back to your rule and modify the BestPracticeRule attribute to reflect the new diagnostic message:</span></span>

```xpp
[BestPracticeRule(
    AuthorNotCurrentDiagnosticItem.DiagnosticMoniker,
    typeof(Messages),
    AuthorNotCurrentDiagnosticItem.DiagnosticMoniker + "Description",
    BestPracticeCheckerTargets.Class)]
public class AuthorListRule : BestPracticeAstChecker<BestPracticeCheckerPayload>
{ // ... }
```

<span data-ttu-id="6f562-215">ご覧のように、**BestPracticeRule** 属性に 4 つのパラメータが指定されています。</span><span class="sxs-lookup"><span data-stu-id="6f562-215">As you can see, there are four parameters specified for the **BestPracticeRule** attribute:</span></span>

1. <span data-ttu-id="6f562-216">ルール モニカー</span><span class="sxs-lookup"><span data-stu-id="6f562-216">The rule moniker.</span></span>
2. <span data-ttu-id="6f562-217">ルール記述を保持するリソース ファイルのタイプ。</span><span class="sxs-lookup"><span data-stu-id="6f562-217">The type of the resource file holding the rule description.</span></span> <span data-ttu-id="6f562-218">この例では、既定のリソース ファイルの名前を使用しています。</span><span class="sxs-lookup"><span data-stu-id="6f562-218">In this example, we are using the default resource file named.</span></span> <span data-ttu-id="6f562-219">メッセージと呼ばれるクラスを作成したメッセージ。</span><span class="sxs-lookup"><span data-stu-id="6f562-219">Messages, which created a class called Messages.</span></span> <span data-ttu-id="6f562-220">このクラスのタイプを 2 番目の引数とすることを求めます。</span><span class="sxs-lookup"><span data-stu-id="6f562-220">We want the type of this class as the second argument.</span></span>
3. <span data-ttu-id="6f562-221">ルールの説明を含む文字列リソースの名前。</span><span class="sxs-lookup"><span data-stu-id="6f562-221">The name of the string resource that contains the description of the rule.</span></span> <span data-ttu-id="6f562-222">この名前は、上記のリソース ファイルに追加した **AuthorNotCurrentDescription** という文字列で、ルールを記述するために人間に読みやすい文字列が含まれています。</span><span class="sxs-lookup"><span data-stu-id="6f562-222">This name is the string called **AuthorNotCurrentDescription** that we added to the resource file above; it contains a human legible string to describe the rule.</span></span> <span data-ttu-id="6f562-223">この文字列を使用して、Visual Studio 内のベスト プラクティスのダイアログでユーザーにルールを記述します。</span><span class="sxs-lookup"><span data-stu-id="6f562-223">This string is used to describe the rule to the user in a best practice dialog within Visual Studio.</span></span> <span data-ttu-id="6f562-224">Visual Studio で、**Dynamics 365 &gt; ベスト プラクティス コンフィギュレーション** を選択してダイアログを表示します。</span><span class="sxs-lookup"><span data-stu-id="6f562-224">In Visual Studio, select **Dynamics 365 &gt; Best Practices Configuration** to view the dialog.</span></span>
4. <span data-ttu-id="6f562-225">チェックするアーティファクトの説明。</span><span class="sxs-lookup"><span data-stu-id="6f562-225">A description of the artifacts to check.</span></span> <span data-ttu-id="6f562-226">この場合、値は、ルールをクラスにのみ適用する必要があることを指定します。</span><span class="sxs-lookup"><span data-stu-id="6f562-226">In this case, the value specifies that the rule should only be applied to classes.</span></span> <span data-ttu-id="6f562-227">Modify the description as needed by using one of the other literals in the **BestPracticeCheckerTargets** リスト内の他のリテラルのいずれかを使用して、必要に応じて説明を変更します。</span><span class="sxs-lookup"><span data-stu-id="6f562-227">Modify the description as needed by using one of the other literals in the **BestPracticeCheckerTargets** enumeration.</span></span>

<span data-ttu-id="6f562-228">診断メッセージを記述するクラスのインスタンスを作成し、診断のセットに追加します。</span><span class="sxs-lookup"><span data-stu-id="6f562-228">Instantiate the class that describes the diagnostic message and add it to the set of diagnostics:</span></span>

```xpp
foreach (var name in names)
{
    if (!authorlist.Contains(name))
    {
        // Create the custom error message, including
        // the contextual name information...
        var warning = new AuthorNotCurrentDiagnosticItem(
            this.Context, method.Position, name);

        // and add it to the set of reported messages.
        this.ExtensionContext.AddErrorMessage(warning);
    }
}
```

<span data-ttu-id="6f562-229">この時点で、完全なベスト プラクティス ルールが整っており、組織内の値が提供可能です。</span><span class="sxs-lookup"><span data-stu-id="6f562-229">At this point, you have a complete best practice rule, ready to provide value in your organization.</span></span> <span data-ttu-id="6f562-230">それを構築しエラーを修正します。</span><span class="sxs-lookup"><span data-stu-id="6f562-230">Build it and fix any errors.</span></span>

## <a name="metadata-based-best-practice-rules"></a><span data-ttu-id="6f562-231">メタデータ ベースのベスト プラクティス ルール</span><span class="sxs-lookup"><span data-stu-id="6f562-231">Metadata based Best Practice rules</span></span>

<span data-ttu-id="6f562-232">これまではコードを扱うルールの記述方法について説明してきました。</span><span class="sxs-lookup"><span data-stu-id="6f562-232">Until now we have been describing how to write rules that deal with code.</span></span> <span data-ttu-id="6f562-233">このセクションでは、コードではなく、メタデータに適用されるルールを作成する方法を説明します。</span><span class="sxs-lookup"><span data-stu-id="6f562-233">In this section we show how to author rules that apply to metadata, not code.</span></span> <span data-ttu-id="6f562-234">メタデータ ルールを取り扱うクラスは、**BestPracticeMetadataChecker** から派生します。</span><span class="sxs-lookup"><span data-stu-id="6f562-234">Classes that deal with metadata rules are derived from **BestPracticeMetadataChecker**.</span></span> <span data-ttu-id="6f562-235">派生インスタンスは、チェックする必要があるコンポーネントを記述するメタデータのインスタンスを受け取ります。</span><span class="sxs-lookup"><span data-stu-id="6f562-235">The derived instance receives an instance of the metadata describing the artifact that must be checked.</span></span> <span data-ttu-id="6f562-236">次に、**Microsoft.Dynamics.AX.Metadata.Metamodel** で API を使用し、メタデータ グラフに対して LINQ クエリを使用します。</span><span class="sxs-lookup"><span data-stu-id="6f562-236">You then use the APIs in the **Microsoft.Dynamics.AX.Metadata.Metamodel** to fetch further metadata as needed, and use LINQ queries over the metadata graphs.</span></span> <span data-ttu-id="6f562-237">ベスト プラクティス チェック用のテンプレートには、前のセクションで説明したコード ベースのものと同様に、メタデータ チェックを実行するクラスが含まれています。</span><span class="sxs-lookup"><span data-stu-id="6f562-237">The template for best practice checks contains a class performing metadata checks as well as a code based one we discussed in the previous section.</span></span> <span data-ttu-id="6f562-238">診断メッセージの発行に関する仕組みは、上記で説明したものと同じです。</span><span class="sxs-lookup"><span data-stu-id="6f562-238">The mechanics involved in issuing diagnostic messages is the same as we covered above.</span></span>

## <a name="install-run-and-test-your-rule"></a><span data-ttu-id="6f562-239">ルールのインストール、実行、テスト</span><span class="sxs-lookup"><span data-stu-id="6f562-239">Install, run, and test your rule</span></span>

<span data-ttu-id="6f562-240">コードが正しくコンパイルされたら、DLLが作成されます。</span><span class="sxs-lookup"><span data-stu-id="6f562-240">When your code compiles cleanly, a DLL will be created.</span></span> <span data-ttu-id="6f562-241">ツールが新しいルールを選択できるようにするためには、実行する前にこの DLL をインストールする必要があります。</span><span class="sxs-lookup"><span data-stu-id="6f562-241">In order for the tooling to be able to pick up the new rule, this DLL must be installed before running it.</span></span> <span data-ttu-id="6f562-242">DLL のインストールには、次の 2 つの方法があります。</span><span class="sxs-lookup"><span data-stu-id="6f562-242">Installing the DLL can be done in two ways:</span></span>

- <span data-ttu-id="6f562-243">ベスト プラクティス コンフィギュレーション ダイアログのボタンを使用します。</span><span class="sxs-lookup"><span data-stu-id="6f562-243">By using the button on the Best Practice configuration dialog.</span></span> <span data-ttu-id="6f562-244">**拡張機能をインストール** ボタンをクリックします。</span><span class="sxs-lookup"><span data-stu-id="6f562-244">Click the **Install extension** button.</span></span> <span data-ttu-id="6f562-245">自分のルール (つまり、ルール作成時に生成される DLL) を含むアセンブリ ファイルを指すように求められます。</span><span class="sxs-lookup"><span data-stu-id="6f562-245">You will be asked to point to the assembly file that contains your rule (that is, the DLL generated when you build the rule).</span></span> <span data-ttu-id="6f562-246">[OK] を押すと、システムが必要な DLL をコピーします (以下を参照)。</span><span class="sxs-lookup"><span data-stu-id="6f562-246">Press OK, and the system will copy the DLL where it needs to be (see below).</span></span>
- <span data-ttu-id="6f562-247">DLL を C:\\Packages\\bin\\BPExtensions フォルダーに手動でインストールします。</span><span class="sxs-lookup"><span data-stu-id="6f562-247">By manually installing the DLL into the C:\\Packages\\bin\\BPExtensions folder.</span></span>

<span data-ttu-id="6f562-248">ルールをデバッグする場合は、.pdb ファイルをアセンブリと同じディレクトリにコピーすると便利です。</span><span class="sxs-lookup"><span data-stu-id="6f562-248">If you want to debug your rule, you will find it useful to copy the .pdb file to the same directory as the assembly.</span></span> <span data-ttu-id="6f562-249">DLL がターゲット ディレクトリに展開したら、Visual Studio を再起動する必要があります。</span><span class="sxs-lookup"><span data-stu-id="6f562-249">After the DLL has been deployed to the target directory, Visual Studio needs to be restarted.</span></span> <span data-ttu-id="6f562-250">その後は、ルールは使用可能です。</span><span class="sxs-lookup"><span data-stu-id="6f562-250">After that, the rule is available for use.</span></span> <span data-ttu-id="6f562-251">残りの欠陥を解決するルールをデバッグすることが必要な場合があります。</span><span class="sxs-lookup"><span data-stu-id="6f562-251">You may have to debug your rule to iron out any remaining kinks.</span></span> <span data-ttu-id="6f562-252">実際には、開始するとき、ルールに従って進み AST を検査することは重要です。</span><span class="sxs-lookup"><span data-stu-id="6f562-252">In fact, stepping through your rule and inspecting the ASTs is valuable when you are getting started.</span></span> <span data-ttu-id="6f562-253">ルールをデバッグするには、ベスト プラクティス ルールが **xppAgent** プロセスによって実行されることを確認する必要があります。したがって、VS 自体のコンテキスト内では実行されません。</span><span class="sxs-lookup"><span data-stu-id="6f562-253">To debug a rule, you need to know that the best practice rule is run by the **xppAgent** process; it is therefore not run within the context of VS itself.</span></span> <span data-ttu-id="6f562-254">**Finance and Operations** ページの Visual Studio オプション ダイアログで **ベスト プラクティス チェックの実行** を選択したことを確認します。</span><span class="sxs-lookup"><span data-stu-id="6f562-254">Make sure you have selected **Run best practice checks** in the Visual Studio Options dialog, in the **Finance and Operations** page.</span></span> <span data-ttu-id="6f562-255">それ以外の場合、チェックは実行されません。</span><span class="sxs-lookup"><span data-stu-id="6f562-255">Otherwise, your check will not run.</span></span>   <span data-ttu-id="6f562-256">**VisitMethod** メソッドでブレークポイントを設定し、上記のようにフリート管理モデルでオンに切り替えられた新しいルールを含むモデルのビルドを行います。</span><span class="sxs-lookup"><span data-stu-id="6f562-256">Set a breakpoint in the **VisitMethod** method, and then do a build of a model that has the new rule switched on as shown above for the Fleet management model.</span></span> <span data-ttu-id="6f562-257">VS インスタンスを **xppcAgent** プロセスに添付します。</span><span class="sxs-lookup"><span data-stu-id="6f562-257">Attach your VS instance to the **xppcAgent** process.</span></span> <span data-ttu-id="6f562-258">ビルドを実行すると、ブレークポイントにヒットして、コードへのドリルダウンを開始することができます。</span><span class="sxs-lookup"><span data-stu-id="6f562-258">When you do a build your breakpoint will be hit, and you can start drilling into your code.</span></span> <span data-ttu-id="6f562-259">すべてのプロパティ、宣言およびステートメントの一覧を表示し、それらに関するすべての詳細を見つけることができます。</span><span class="sxs-lookup"><span data-stu-id="6f562-259">You can see all the properties, the list of declarations and statements, and find out all the details about them.</span></span>

### <a name="running-rules-in-xppbpexe"></a><span data-ttu-id="6f562-260">XppBp.exe でルールを実行</span><span class="sxs-lookup"><span data-stu-id="6f562-260">Running rules in XppBp.exe</span></span>

<span data-ttu-id="6f562-261">上記のとおりベスト プラクティス ルールは、Visual Studio のプロジェクトのビルドのパーツとして多くの場合実行されますが、それを実行する専用のコマンド ライン ツールもあります。</span><span class="sxs-lookup"><span data-stu-id="6f562-261">As described above the best practice rules are often run as part of the build of a project from Visual Studio, but there is also a dedicated command-line tool to run them.</span></span> <span data-ttu-id="6f562-262">このツールは **xppbp.exe** ツールで、主に夜間のビルド シナリオ用です。</span><span class="sxs-lookup"><span data-stu-id="6f562-262">This tools is the **xppbp.exe** tool, and it is intended mainly for nightly build scenarios.</span></span> <span data-ttu-id="6f562-263">コマンド ラインから起動することにより、有効なコマンド ラインのスイッチと引数の概要が得られます。</span><span class="sxs-lookup"><span data-stu-id="6f562-263">Invoking it from the command line yields a useful overview of the command-line switches and arguments.</span></span> <span data-ttu-id="6f562-264">次にいくつか役に立つ例を挙げます。</span><span class="sxs-lookup"><span data-stu-id="6f562-264">Here are some useful examples:</span></span>

- <span data-ttu-id="6f562-265">モジュール内のすべてのフォームで BP を実行します: `xppbp -module:FleetManagement form:*`</span><span class="sxs-lookup"><span data-stu-id="6f562-265">Run BP on all forms in a module: `xppbp -module:FleetManagement form:*`</span></span>
- <span data-ttu-id="6f562-266">特定の要素で BP を実行します: `xppbp -module:FleetManagement class:MyClass form:MyForm`</span><span class="sxs-lookup"><span data-stu-id="6f562-266">Run BP on specific elements: `xppbp -module:FleetManagement class:MyClass form:MyForm`</span></span>
- <span data-ttu-id="6f562-267">モデル内のすべての項目で BP を実行します (モジュール内のこの 1 つのモデルに対してのみ): `xppbp -module:FleetManagement -model:FleetManagement –all`</span><span class="sxs-lookup"><span data-stu-id="6f562-267">Run BP on all items in the model (and only for this one model in the module): `xppbp -module:FleetManagement -model:FleetManagement –all`</span></span>
- <span data-ttu-id="6f562-268">モジュール内のすべてのモデルのすべての品目で BP を実行します: `xppbp -module:FleetManagement –all`</span><span class="sxs-lookup"><span data-stu-id="6f562-268">Run BP on all items in all models in the module: `xppbp -module:FleetManagement –all`</span></span>
- <span data-ttu-id="6f562-269">ログ ファイルに対する出力を記述します: `xppbp -module:FleetManagement -all -xmllog=Log.xml -log=Log.txt`</span><span class="sxs-lookup"><span data-stu-id="6f562-269">Write the output to log files: `xppbp -module:FleetManagement -all -xmllog=Log.xml -log=Log.txt`</span></span>


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]