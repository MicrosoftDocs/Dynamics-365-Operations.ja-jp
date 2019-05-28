---
title: X++ と X++ コンパイラの変更
description: このトピックでは、Microsoft Dynamics 365 for Finance and Operations のコンパイラーになされた変更についてレビューします。
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
ms.custom: 26781
ms.assetid: 056d4064-e365-487c-a606-e2fadfe28242
ms.search.region: Global
ms.author: pvillads
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: d4f06921ccaec53cf9d2ab3d769b8ab3d6406b1a
ms.sourcegitcommit: 2b890cd7a801055ab0ca24398efc8e4e777d4d8c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/07/2019
ms.locfileid: "1506140"
---
# <a name="changes-in-x-and-the-x-compiler"></a>X++ と X++ コンパイラの変更

[!include [banner](../includes/banner.md)]

このトピックでは、Microsoft Dynamics 365 for Finance and Operations のコンパイラーになされた変更についてレビューします。 X++ コンパイラは書き換えられています。 製品への構造的な変更によって必須とされる場合を除き、X++ に導入された下位互換性のない変更はありません。 いくつかの言語拡張機能が追加されました。 また、新しい X++ ベスト プラクティス ツールが実装されているため、ユーザー定義のカスタム ルールを追加できます。

## <a name="no-more-p-code-everything-is-in-net-framework-cil"></a>P コードはもう不要です。すべては .NET Framework CIL にあります
Microsoft Dynamics AX 2012 によって X++ ソース コードは p コードにコンパイルされ、実行時にインタープリタによって解釈されました。 必要に応じて、Microsoft .NET CIL (共通中間言語) に p コードをコンパイルすることができます。 CIL は C\# および Visual Basic の .NETコンパイラ が生成するものです。 ただし、X++ CIL コードは、主にサービスとバッチ ジョブで実行されるコードに対して、限られた場合でのみ使用できました。 新しい X++ コンパイラは CIL のみを生成します。 他の p コードはありません。 p コードを扱う以下のツールは廃止され、Dynamics AX から削除され、.NET ツールに置き換えられました。

-   P コードを生成する X++ コンパイラ。
-   p-code を入力して .NET CIL を生成する特別なコンパイラ。
-   その確定的なガベージ コレクターを含む p コードの実行時インタプリター。
-   Dynamics AX デバッガーー。
-   パフォーマンス上のボトルネックを特定するのに役立つ Dynamics AX コード プロファイラー。
-   Dynamics AX と相互運用される外部アプリケーションの AX .NET Business Connector。

.NET CIL として排他的に動作する X++ コードには、次のような重要な利点があります。

-   ほとんどのシナリオでは、CIL はより高速に動作します。 多くのメソッドの呼び出しがあり、大量のアルゴリズム コンテンツ (データベース アクセスではない) がある場合、大幅なパフォーマンスの向上が期待できます。
    -   アプリケーション ロジックを他のマネージド言語で記述することがより簡単です。
    -   アセンブリを直接消費することができるため、AX .NET Business Connector や管理プロキシは必要なくなりました。
    -   ビジネス ロジックを外部で使用する適切な方法は、サービスを使用することです。
-   CIL は、他の .NET アセンブリ DLL ファイルで使用可能なクラスを効率的に参照できます。実行時間リフレクション ベースのオーバーヘッドは P コード インタープリターに負担をかけません。
-   CIL は多数の .NET ツールから操作できます。

## <a name="unit-of-compilation"></a>コンパイルの単位
Microsoft Dynamics AX の以前のバージョンは、個々のメソッドのレベルで X++ をコンパイルできます。 したがって、クラスのコンパイルにおいてクラスの 1 つのメソッドでエラーが見つかった場合、正しくコンパイルされたメソッドはまだ実行可能でした。 標準のコンパイルで、単位は C\# などの他の .NET 言語と同じです。 モデル要素 (クラス、フォーム、クエリなど) で任意のメソッドがコンパイルに失敗すると、すべてのコンパイルが失敗します。

## <a name="enhancements-to-x"></a>X++ の拡張機能
X++ は .NET の世界でファーストクラスの住民になりました。 そのため、C\# や他の .NET 言語で利用可能な X++ のいくつかの構造に追加しています。 変更は一般的に非侵入型です。 実際、非常にわずかな変更が既存の X++ コードの構文とセマンティクスに対して行われました。 これらの追加内容のほとんどが、次の一覧にあります。

-   `finally` キーワードを `try` および `catch` キーワードの後に使用できるようになりました。 セマンティクスは C\# のセマンティクスと同じです。 finally 句に指定されたステートメントは、try ブロックが例外をスローしたかどうかにかかわらず実行されます。
-   `using` キーワードは、.NET 名前空間を参照するための省略形として追加されました。 次のコード例は、using キーワードを使用して名前空間を参照する2つの方法を示しています。

        using SysColl = System.Collections;  // SysColl is an alias for the whole namespace.
        using           System.CodeDom;      // Contains the class named CodeComment.

        public class MyClass2
        {
            static SysColl.ArrayList arrayList = new SysColl.ArrayList(); // Initialized on declaration.
            CodeComment codeComment          = new CodeComment("I am a comment.");

            // More X++ code here.
        }

-   クラスのフィールドをフィールドの declaration ステートメントで初期化することができるようになりました。 これは、前のコード例で 2 回示されています。
-   メソッドの開始時だけでなく、小さなスコープ内で変数を宣言することができます。
-   `var` キーワードは、宣言された変数の型を推定するコンパイラを許可するショートカットとして使用できます。
-   クラスのフィールドを静的にすることができます。 以前のバージョンでは、インスタンス フィールドのみ許可されていました。
-   クラスは、1 つの静的コンストラクターを持つことができます。 以前のバージョンでは、インスタンス コンストラクターのみ使用できました。 次の X++のコード例は、新しいキーワード typenew による 、静的コンストラクターの構文を示しています。

        .    public class MyClass4
            {
                static utcdatetime utcInitialized3;  // Static variable member.
                static void typenew()                // Static constructor member. 'typenew' is a new keyword.
                {
                utcInitialized3 = DateTimeUtil::utcNow(); // Static variable referenced without class name.
                }
            }

-   属性の修飾で、接尾語に `Attribute` がある場合、クラスまたはメソッドのような属性名の接尾語を省略できます。 したがって、X++ は C\# を結合し、`[MyFavoriteAttribute]` を要求する代わりに `[MyFavorite]` を許可します。
-   デリゲートはクラスにだけでなく、テーブル、フォーム、またはクエリで定義できるようになりました。
-   属性はデリゲートとメソッドのハンドラーに現在適用され、ハンドラーをこれらの目標にマップします。
-   これで、クラスは X++ ソース コードに入れ子にできます。 入れ子になったクラスはフォーム内 (FormRun を拡張するクラスなど) でのみ使用でき、コントロール、データ ソースまたはデータ フィールドを表します。

## <a name="backward-incompatible-changes-to-x"></a>X++ への後方互換性のない変更
従来のカスタム X++ ソース コードに対応する変更が必要な X++ には、変更点がいくつかあります。 これらの変更内容のほとんどが、次の一覧にあります。

-   次のキーワードは、X++ 言語の一部ではなくなっており、使用するとコンパイル エラーが発生します。
    -   `changeSite`
    -   `pause`
    -   `window`
-   旧式 X++ では、クライアントまたはサーバーのいずれかを実行するメソッドを指定できました。 これは不可能です。 すべてのコンパイルされた X++ コードは、サーバー上の .NET CIL で実行されます。 クライアント サイトまたはブラウザーで評価される X++ コードは存在しないため、*client* と *server* の 2 つのキーワードは無視されます。 コンパイル エラーは発生しませんが、新しい X++ コードのいずれでも使用しないでください。
-   Microsoft Dynamics AX 2012 には、P コード対 CIL にコンパイルしたときに X++ が異なる動作をするいくつかの領域がありました。 Dynamics 365 for Finance and Operations のこれらすべての領域では、Microsoft DynamicsAX 2012 の CIL で実行されたように動作します。 X++ p-code と CIL としての X+ との間の有意な行動上の相違は次のとおりです。
    -   CIL では、`real `データ型が `System.Decimal` として表されます。 これは、各 `real` の範囲と精度が p コードの場合と異なることを意味します。 この変更は、.NET CIL が実行された時点で Microsoft Dynamics AX 2012 ですでに有効でした。
    -   1 つの全体配列を別の配列に割り当てることが P コード モードの値で実行されましたが、CIL モードでの参照が実行されます。
    -   `Global::runClassMethodIL` などの CIL ヘルパー メソッドは、関連性が無くなったため削除されました。
-   **AOT** &gt; **Jobs** &gt; **MyJob** の意味にジョブの概念はありません。 X++ メソッドをすばやく簡単に実行するには、`static Main` メソッドをクラスに追加し、そのクラスを Microsoft Visual Studio のプロジェクトのスタートアップ オブジェクト フォームとして設定します。 プロジェクトが実行されるときは、`Main`メソッドが実行されます。


<a name="additional-resources"></a>追加リソース
--------

[C# で使用する Dynamics AX LINQ プロバイダー](linq-provider-c.md)

[技術概念ガイド](developer-home-page.md)



