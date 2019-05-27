---
title: ベスト プラクティス ルールを記述する
description: このトピックでは、メタデータと X++ コードの両方について、C# でベスト プラクティス ルールを作成する方法について説明します。
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
ms.custom: 48071
ms.assetid: 4fe671c4-c556-4942-8570-307cf68ae0a7
ms.search.region: Global
ms.author: pvillads
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 500012dd945c7ab32bcba63d1267f0ac9a23bb77
ms.sourcegitcommit: 2b890cd7a801055ab0ca24398efc8e4e777d4d8c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/07/2019
ms.locfileid: "1536977"
---
# <a name="write-best-practice-rules"></a>ベスト プラクティス ルールを記述する

[!include [banner](../includes/banner.md)]

このトピックでは、メタデータと X++ コードの両方について、C# でベスト プラクティス ルールを作成する方法について説明します。 推奨チェックは出荷コードで許容されない不都合なプラクティスをキャッチするためにコンパイラおよび日単位ビルドで実行されます。 この機能を使用して、アプリケーションに関する情報を収集するための簡単なツールを作成することもできます。

このトピックでは、ベスト プラクティス フレームワークを使用して、新しいベスト プラクティス ルールを作成する方法を説明します。 推奨チェックは出荷コードで許容できないとみなされるコーディング プラクティスをキャッチするために開発時および日単位ビルドで実行されます。 ただし、ベスト プラクティス ルールはこの使用に制限されません。アプリケーションに関する情報を収集するための簡単なツールを作成するのにも使用できます。 このフレームワークは、XLNT (X++ LaNguage ツールキットの省略形) と呼ばれるマネージド フレームワークの上に構築され、X++ コードから情報を抽出して変更するカスタム ツールを構築するのに使用できます。 ベスト プラクティス ルールには、メタデータを処理するルールとソース コードを処理するルールの 2 種類があります。

## <a name="code-best-practice-framework"></a>コードのベスト プラクティス フレームワーク
コード ベスト プラクティス フレームワーク (CBPF) を使用すると、X++ ソース コードを分析するための独自のツールを作成できます。 これらのルールは、X++ ソース コードに問題があると判断するものを診断します。 このセクションでは、ベスト プラクティス機能の基礎について説明します。 この情報は、独自のルールの作成について詳しく説明する後のセクションの理解に役立ちます。 また、このドキュメントで示されているものよりも複雑なコード ルールを求める開発者にとっても便利です。 CBPF API は、インフラストラクチャの問題に対しなくても、、表現するルールに焦点を当てることができるように設計されています。トークンを読み取り、それらを組み合わせてインテリジェンスなものを作成する必要はありません。 代わりに、CBPF は次のパーツを提供します。

-   X++ ソース コードから抽象構文ツリー (AST) を構築するパーサー。
-   X++ コードでパスの順序を実行するパイプライン。
-   作成済みのパスの数。 最初のパスは、ソース コードの解析です。
-   メタデータを読み取るインフラストラクチャ。

ルールは AST に基づいているために、ルールの作成を始める前にその概念を理解する必要があります。

### <a name="the-parser-and-asts"></a>パーサーと AST

パーサーは、X++ コードを読み込み、それに重大な構文エラーが含まれていない場合は、それから AST を生成します。 パーサーは、組み込みのエラー回復スキームを持つため、大部分の構文エラーから適切に回復できます。 構文エラーが発生するときは、パーサーはセミコロンに到達するまで記号を読み取り、セミコロンが正しい記号となる状態に到達するまでその状態をアンスタックして AST の構築を試みます。 さらに、パーサーは構文エラーが発生したときに、適切な記号のセットを提案できます。 パーサーは、API のコンシューマーと直接対話するようにはなっていませんが、ユーザーの介入なしに機能するブラック ボックスと見なす必要があります。 パーサーはソース コードの言語構成を認識すると、AST を構築します。 AST は、それらが表す X++ コンポーネントの抽象化であるノードで構成されます。 この概念を、いくつかの AST ノードを表示することによって、下図に示します。

    public abstract class Statement : Ast
    {
        /// <summary>
        /// Gets or sets the comments in the statement
        /// </summary>
        public string Comments { get; set; }

        public abstract string ToString(int indent);
    }

Statement クラスは抽象的です。"ステートメント" のインスタンスを作成しても意味がありません。コンクリート派生クラス (if ステートメントや while ステートメントなど同様) のインスタンスのみ作成できます。 コメント プロパティはこの基本クラスに置かれるため、すべての派生クラスに適用されます。つまり、すべてのステートメントはステートメントの前にコメントを持つことができ、特定のプロパティを使用してアクセスできます。 X++ にはさまざまな多数の種類のステートメントがあり、それぞれが上記の抽象ステートメント クラスの 1 つ以上のステップで派生したクラスによって記述されています。 次の例は、**while** ステートメントの定義を示しています。

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

**while** ステートメントは条件 (式) と、条件が true と評価される限り実行される構成ステートメントで構成されています。 パーサーは、表現された成果物が開始および終了するソース コードの位置 (つまり、その範囲) を保持します。 AST がスキャンされるので、個々のノードに情報を追加すると便利です。 たとえば、すべての式にはタイプがあります。 タイプの互換性の問題を診断するためにツリーがスキャンされるので、個々のノードにその情報を配置できるようになると便利です。 各要件の AST ノードを変更する必要はなく、各ノードに名前/値の組み合わせを提供するために使用するプロパティ コレクションがあります。 各 AST ノードには、ノードの高精度の文字列表現を戻す **ToString** 方法があります。これはシナリオのデバッグに役立ちます。

### <a name="the-astsweeper-class"></a>AstSweeper クラス

AstSweeper は、指定された AST インスタンスに ビジター パターンを適用します。 ビジター パターンを使用すると、プログラマーは、ユーザーがノード上で実行する操作 (コードに関する論理推論) から基礎となるデータ構造 (AST) を分離することが可能になります。 **AstSweeper** クラスには、AST ノード タイプごとに仮想メソッドがあり、AST の構造の指示に従って呼び出します。 次の例では、スウィーパーの動作を示しています。 わかりやすくするためにいくつかの詳細が除外されました。

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

特定の AST ノードを扱う仮想メソッドの名前は、Visit が先頭に追加された AST クラスの名前です。 そのパラメーターは、参照するノードと、呼び出されたときすべての参照者に渡すことのできるペイロードです。 この方法で、スウィーパーは深さ優先トラバーサルで渡される AST のノードのそれぞれに対して 1 回仮想メソッドを呼び出します。 ペイロード パラメーターを使用して、必要に応じて、各ノードに情報 (シンボル テーブルなど) を渡すことができます。 開発者は、AstSweeper クラスから派生したクラスを構築し、特定の関心のあるメソッドを上書きします。

#### <a name="example"></a>例

X++ コーディング ガイドラインに準拠するため、アンダースコア文字で始まるパラメーター名の割合を決定する必要があるとします。 次に、パラメーター数とアンダー スコアで始まるパラメーター数を計算したロジックを使用して、**AstSweeper** から派生するクラスを記述します。 次の例は、このコードを示しています。

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

この場合、集計はクラス スコープで定義されている **ParametersCount** および **UnderscoredParameters** プロパティで維持されます。 もう 1 つの均等に有効なアプローチでは、すべての **Visit** メソッドに渡されるペイロードにこの情報を渡すことができます。 ほとんどの場合、ユーザーは Visit メソッドがアクセスしたノード以下のすべてのノードに対して呼び出されることを確認するために、オーバーライドされたメソッドから super() を無条件に呼び出す必要があります。 上記の場合、相違が生じないため、AST ツリー トラバーサルを簡略化することでパフォーマンスを向上します。

### <a name="writing-code-for-best-practice-rules"></a>ベスト プラクティス ルールのコードを記述

概念が導入されたので、ビジネス ルールを作成する準備が整いました。 基本的には次のことが必要です。

1. AST のプロパティに関して診断したい状況を定義します。 解析を実行できる <strong>Visit\</strong>* メソッドを記述できます。
2. エラー状態が検出されたとき、診断メッセージを生成する必要があります。 この目的のために使用される API があります。基本的には、各診断メッセージの定型コードを書く必要があります。
3. ユーザーが自分の作業にルールを含めるかどうか、またそう指定された場合に実行するかどうかを決められるように、新しいベスト プラクティス ルールを残りのフレームワークにフックする必要があります。

### <a name="create-a-best-practice-rules-project-in-visual-studio"></a>Visual Studio でのベスト プラクティス ルール プロジェクトの作成

このチュートリアルでは、次のシナリオを考えてみましょう。

1.  一部のメソッドには、コードを記述した個人の名前を指定する Author 属性が用意されています。 これは、そのメソッドを含むスタック トレースが表示されたときに指摘する人を見つけるときに便利です。
2.  開発者の重要な納期があるので、一覧表示された開発者の名前は静的である必要があります。 Author 属性で使用されている名前を確認し、現在の開発者の名前のリストと照合します。

作成者属性クラスは、単に次のように定義されます。

    class AuthorAttribute extends SysAttribute
    {
        private str theAuthor;

        public void new(str _author) 
        {
            this.theAuthor = _author;
        }
    }

実稼働コードでは、パラメーターの値などに関する主な前提を検証するために、ドキュメント コメントとアサートを挿入します。このチュートリアルではコードをわかりやすく書くため、これらの手順を省略します。 アーカイブするものに対してステージを設定したので、Visual Studio を開始してベスト プラクティス ルール プロジェクトを作成することができます。 ルールの目的を適切に伝えるわかりやすい名前を入力してください。Visual Studio は、いくつかのソース コード スニペットおよびプロジェクト参照が設定されたプロジェクトを作成します。 このソース コードを自分のコードの出発点として使用することにより、時間を大幅に節約することができます。 既定の例には、メソッド名に "Microsoft" という語を禁止するルール (著作権上の理由から)、また名前に特定の文字を禁止するというメタデータ ベースのルールが含まれています。 ここではメタデータ チェックを行いませんので、プロジェクトから InvalidCharactersDiagnosticItem.cs ファイルと DemoMetadataCheck.cs ファイルを削除できます。 また、Microsoft の名前チェックに興味がないので、DemoAST クラスの VisitMethod メソッドのコンテンツを削除してください。 最初に行う必要があるのは、特定のメソッドの作成者属性が 1 つ以上あるかどうかを調べることです。 このメソッド タイプ (これは、VisitMethod メソッドにパラメーターとして渡されます) に AttributeList タイプの属性プロパティが含まれていることがわかります。 これを使用して、Author 属性がこのメソッドで定義されるかどうかを確認しましょう。

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

この時点であらゆる属性をループし作成者名のリストを収集しています (Author 属性の最初のパラメータとして提供される名前など)。 現在は、リストを許可された作成者のリストと比較する必要があり、静的リストで維持しています。 リストに記載されていない作成者が指定されるときはいつでも、適切な診断メッセージを発行する必要があります。 現時点では、次のようなものがあります。

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

つまり、ルールの違反についてユーザーに通知するために診断メッセージを作成する必要があります。 前述のように、ビジターの基本実装を呼び出すことが重要です。メソッドに含まれるすべてのノードのビジター メソッドを呼び出します。 ただし、この場合は、作成者属性がリストにあるかを判断した後の詳しい操作は行うことを望みません。

### <a name="add-a-class-for-the-diagnostic-message"></a>診断メッセージのクラスの追加

プロジェクトにはすでにエラー メッセージの定型コードが含まれているため、ルールに違反した場合に返される診断メッセージを作成するための出発点として使用します。 各メッセージは、独自のクラスとして実装されます。 各エラー メッセージは、コード化された文脈情報を任意の量で有することができます。 この場合、コンテキスト情報は一覧にない作成者の名前です。 「プロジェクトでそのファイルを開き、文字列を追加します」というメッセージをメッセージ リソース ファイルに追加することから開始します。 AuthorNotCurrent という名前 (エラー モニカーとも呼ばれます) を使用します。 ‘{0}’ 文字列はコンテキスト情報のプレースホルダで、この場合、リストに含まれていない作成者の名前です。 エラー メッセージに表示される実際のテキストに加えて、ルールの説明を含む文字列もあります。この情報は、Visual Studio 内のベスト プラクティス ダイアログに表示され、ユーザーがシステムで有効にできるルールを決定できるように設計されています。 診断メッセージのクラスを作成し、AuthorNotCurrentDiagnosticItem.cs という名前を付けます。 NotAllowedWordDiagnosticItem クラスから、次の基となるコードを追加します。

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

診断メッセージは消費の準備ができています。 実行する必要がある簿記は 1 つだけです。このルールは、潜在的にどの診断を行うかを宣言的に公表する必要があります。 ルールに戻り、新しい診断メッセージを反映するように BestPracticeRule 属性を変更します。

    [BestPracticeRule(
        AuthorNotCurrentDiagnosticItem.DiagnosticMoniker,
        typeof(Messages),
        AuthorNotCurrentDiagnosticItem.DiagnosticMoniker + "Description",
        BestPracticeCheckerTargets.Class)]
    public class AuthorListRule : BestPracticeAstChecker<BestPracticeCheckerPayload>
    { ... }

ご覧のように、**BestPracticeRule** 属性に 4 つのパラメータが指定されています。

1.  ルール モニカー
2.  ルール記述を保持するリソース ファイルのタイプ。 この例では、メッセージと呼ばれるクラスを作成した、メッセージという名前の既定のリソース ファイルを使用しています。 このクラスのタイプを 2 番目の引数とすることを求めます。
3.  ルールの説明を含む文字列リソースの名前。 これは、上記のリソース ファイルに追加した **AuthorNotCurrentDescription** という文字列です。 ルールを記述するために人間に読みやすい文字列が含まれています。 この文字列を使用して、Visual Studio 内のベスト プラクティスのダイアログでユーザーにルールを記述します。 Visual Studio で、**Dynamics 365 &gt; ベスト プラクティス コンフィギュレーション** を選択してダイアログを表示します。
4.  チェックするアーティファクトの説明。 ここでは、値は、ルールをクラスにのみ適用する必要があることを指定します。 BestPracticeCheckerTargets 列挙に含まれる他のリテラルのいずれかを使用して、ユーザーのニーズに自由に変更してください。

保留中の TODO 項目に今もなお入力する必要があります。これは、現在は、診断メッセージを記述するクラスのインスタンス化と診断セットにそのメッセージを追加することに縮小されています。

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

この時点で完全なベスト プラクティス ルールが整っており、組織内の値を提供可能です。 先に進んで構築し、入り込んだ可能性のあるエラーを修正します。

## <a name="metadata-based-best-practice-rules"></a>メタデータ ベースのベスト プラクティス ルール
これまではコードを扱うルールの記述方法について説明してきました。 このセクションでは、コードではなく、メタデータに適用されるルールを作成する方法を説明します。 メタデータ ルールを扱うクラスは、**BestPracticeMetadataChecker** から派生しています。 派生インスタンスは、チェックする必要があるコンポーネントを記述するメタデータのインスタンスを受け取ります。 次に、Microsoft.Dynamics.AX.Metadata.Metamodel で API を使用して、必要に応じて追加のメタデータをフェッチし、メタデータ グラフに対して LINQ クエリを使用します。 ベスト プラクティス チェック用のテンプレートには、前のセクションで説明したコード ベースのものと同様に、メタデータ チェックを実行するクラスが含まれています。 診断メッセージの発行に関する仕組みは、上記で説明したものと同じです。

## <a name="install-run-and-test-your-rule"></a>ルールのインストール、実行、テスト
コードが正しくコンパイルされたら、DLLが作成されます。 ツールが新しいルールを選択できるようにするためには、実行する前にこの DLL をインストールする必要があります。 DLL のインストールには、次の 2 つの方法があります。

-   ベスト プラクティス コンフィギュレーション ダイアログのボタンを使用します。 **拡張機能をインストールする...** ボタンをクリックします。 自分のルール (つまり、ルール作成時に生成される DLL) を含むアセンブリ ファイルを指さすように求められます。 [OK] を押すと、システムが必要な DLL をコピーします (以下を参照)。
-   DLL を C:\\Packages\\bin\\BPExtensions フォルダーに手動でインストールします。

ルールをデバッグする場合は、.pdb ファイルをアセンブリと同じディレクトリにコピーすると便利です。DLL をターゲット ディレクトリに展開したら、Visual Studio を再起動する必要があります。 その後は、ルールは使用可能です。 残りの欠陥を解決するルールをデバッグすることが必要な場合があります。 実際、ロープを学習している場合、ルールに従って進み、AST を検査することは重要です。 ルールをデバッグするには、ベスト プラクティス ルールが実際に xppAgent プロセスによって実行されることを確認する必要があります。したがって、VS 自体のコンテキスト内では実行されません。 **Finance and Operations** ページの Visual Studio オプション ダイアログ ボックスで **推奨チェックの実行** を選択したことを確認します。 それ以外の場合、チェックは実行されません。   **VisitMethod** メソッドでブレークポイントを設定し、上記のようにフリート管理モデルでオンに切り替えられた新しいルールを含むモデルのビルドを行います。 VS インスタンスを xppcAgent プロセスにアタッチします。 ビルドを実行すると、ブレークポイントにヒットして、コードへのドリルダウンを開始することができます。 すべてのプロパティ、宣言およびステートメントの一覧を表示し、それらに関するすべての詳細を見つけることができます。

### <a name="running-rules-in-xppbpexe"></a>XppBp.exe でルールを実行

上記のとおりベスト プラクティス ルールは、Visual Studio のプロジェクトのビルドのパーツとして多くの場合実行されますが、それを実行する専用のコマンド ライン ツールもあります。 これは xppbp.exe ツールで、主に夜間のビルド シナリオ用です。 コマンド ラインから起動することにより、有効なコマンド ラインのスイッチと引数の概要が得られます。 次にいくつか役に立つ例を挙げます。

-   モジュール内のすべてのフォームで BP を実行します: `xppbp -module:FleetManagement form:*`
-   特定の要素で BP を実行します: `xppbp -module:FleetManagement class:MyClass form:MyForm`
-   モデル内のすべての項目で BP を実行します (モジュール内のこの 1 つのモデルに対してのみ): `xppbp -module:FleetManagement -model:FleetManagement –all`
-   モジュール内のすべてのモデルのすべての品目で BP を実行します: `xppbp -module:FleetManagement –all`
-   ログ ファイルに対する出力を記述します: `xppbp -module:FleetManagement -all -xmllog=Log.xml -log=Log.txt`





