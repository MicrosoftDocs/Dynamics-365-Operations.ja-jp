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
ms.openlocfilehash: aebae3e0e77b1dfe0d1d75972de0052f2c2e2f5f
ms.sourcegitcommit: 2b890cd7a801055ab0ca24398efc8e4e777d4d8c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/07/2019
ms.locfileid: "1537336"
---
# <a name="x-and-debugger-features"></a>X++ およびデバッガーの機能

[!include [banner](../includes/banner.md)]

このチュートリアルでは、開発者が X++ 言語の高度なコンストラクトを使用し、生産的なデバッガ機能を利用できるようにすることを目的としています。 これは、これらの機能を使用してプラクティスするための新しい機能のチュートリアルです。 

以前のバージョンでは、X++ コードは疑似コードつまり P コードにコンパイルされ、サーバーまたはクライアント アプリケーションで解釈されていました。 このコードは、その後、CIL にコンパイルされました。 今日の話はずっと単純です - CIL だけがサポートされ、このコードは新しいコンパイラから生成されます。 このチュートリアルでは、X++ 言語に追加された新しい機能の一部について説明します。 シナリオを実行するとき、デバッガーの新機能の一部が表示されます。

## <a name="declare-anywhere"></a>任意の場所で宣言
以前は、すべてのローカル変数を、使用しているメソッドの先頭に配置する必要がありました。 現在は、変数のスコープを詳細に制御できます。 この新しい機能では、変数のための小さなスコープを用意することができ、この外では変数を参照することはできません。 変数の有効期間は宣言されているスコープです。 以下に示すように、スコープは、for ステートメントおよび using ステートメント内においてブロック レベルで開始することができます (複合ステートメント内)。 スコープを小さくすることにはいくつかの利点があります。

-   読みやすさが向上しました。
-   コードの長期保守中に変数が不適切に再利用されるリスクを軽減することができます。
-   リファクタリングがかなり簡単になります。 使用すべきでないコンテキストで変数が再使用される心配をせずに、コードをコピーすることができます。

### <a name="example"></a>例

この例では、使用される「for」ステートメント内のループ カウンターを宣言します。

      void MyMethod()
      {
        for (int i = 0; i < 10; i++)
        {
          info(strfmt("i is %1", i));
        }
      }

変数のスコープは for ステートメントそのものであり、条件式とループ更新部分を含みます。 この範囲外で値を使用することはできません。 それを試行すると、次が表示されます。

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

コンパイラは情報の呼び出しで次のエラー メッセージを発行します: 'i' が宣言されていません。

### <a name="example"></a>例

スコープを確立できる場所がもう 1 つあります。using ステートメントは、X++ 言語のもう 1 つの新しいコンポーネントです。

      static void AnotherMethod()
      {
        str textFromFile;

        using (System.IO.StreamReader sr = new System.IO.StreamReader("c:\\test.txt"))
        {
          textFromFile = sr.ReadToEnd();
        }
      }

原則として、IDisposable オブジェクトを使用する場合は、明細書の使用において宣言しインスタンスを作成する必要があります。 using ステートメントは、オブジェクトのメソッドを呼び出すときに例外が発生した場合でも、正しい方法でオブジェクトの Dispose メソッドを呼び出します。 オブジェクトを try ブロック内に配置してから finally ブロック内で明示的に Dispose を呼び出すことにより、同じ結果を達成することができます。実際、これはコンパイラが using ステートメントを翻訳する方法です。 宣言は、提供できる、どこのステートメントにも提供できるようになりました。宣言は構文的なステートメントおよび申告ステートメントです。 したがって、使用する直前に宣言を提供できます。 変数をすべて 1 ヶ所で宣言する必要はありません。

### <a name="example"></a>例

次のサンプルは、上記の機能のいくつかを示しています。

      // loop variable declared within the loop: It will
      // not be misused outside the loop
      for(int i = 1; i < 10; i++)
      {
      // Because this value is not used from outside the loop,
      // its declaration belongs in this smaller scope.
        str s = int2str(i);
        info(s);
      }

混乱を避けるために、X++ コンパイラは、囲みスコープ内または同じスコープであっても、別の変数を隠す変数を導入しようとすると、エラーを発行します。 たとえば、次のコードは、以下の診断メッセージを発行するコンパイラの原因になります。「i 」と呼ばれるローカルの変数はこのスコープでは宣言されません。それは既に親または現在のスコープで別のものを表示している「 i 」が別の意味になってしまうためです。

      {
        int i;
        {
          int i;
        }
      }

これは C\# のルールとよく似ていますが、シャドウが診断されていない C ++ のルールとは異なります。

### <a name="exercise"></a>練習

FMVehicleInventoryServiceClass のコードを変更して、より小さなスコープを使用します。

## <a name="static-constructors-and-static-fields"></a>静的コンストラクターおよび静的フィールド
静的コンストラクターおよび静的フィールドは、X++ 言語の新しい機能です。 静的コンストラクターは、静的またはインスタンス呼び出しがクラスに対して行われる前に実行されることが保証されます。 C\# では、静的の概念が実行中のアプリケーション ドメイン全体に関係します。 静的コンストラクターの実行は、ユーザーのセッションに対して相対的です。 静的コンストラクターには、次のプロファイルがあります。

    static void TypeNew() 

静的コンストラクターを明示的に呼び出すことはありません。コンパイラは、クラスの他のメソッドに先立って、静的コンストラクターを 1 回だけ確実に呼び出すコードを生成します。 静的コンストラクターは、任意の静的データを初期化したり、一度だけ実行する必要のある特定のアクションを実行するために使用されます。 静的コンストラクターに指定できるパラメーターはなく、静的としてマークする必要があります。 静的フィールドは静的キーワードを使用して宣言されているフィールドです。 概念的には、クラスのインスタンスではなくクラスに適用されます。

### <a name="example"></a>例

下の例ではインスタンスと呼ばれる単一を、静的コンストラクターを使用して作成する方法を説明します。

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

      public static Singleton instance()
      {
        return Singleton::instance;
      }
    }

単一は、クラスのインスタンスが 1 つしか呼び出されないことを保証します。これは、以下で消費されます。

    {
        …
        Singleton i = Singleton::instance();
      }

## <a name="assignment-of-field-members-inline"></a>フィールド メンバー インラインの割り当て
フィールド自体の宣言などと共に、フィールド インラインに値を代入できるようになりました。 これは、静的フィールドとインスタンス フィールドの両方に適用されます。 次のコードでは、field1 と field2 の値はこの方法で定義されます。

    public class MyClass2
    {
      int field1 = 1;
      str field2 = "Banana";

      void new()
      {
        // …
      }
    }

上記のコードは、以下と同じ意味を持ちます。  

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

インライン割り当ては、静的メンバーとインスタンス メンバーの両方で機能します。

## <a name="constsreadonly"></a>Consts/読み取り専用
マクロの概念は、引き続き X++ で完全にサポートされています。 ただし、\#定義の代わりに定数を使用することには、多くのメリットがあります。

-   ドキュメント コメントは定数に対して追加することができますが、マクロの値に対して追加することはできません。 最終的に、言語サービスによってこれが選択され、ユーザーに適切な情報が提供されます。
-   定数は、IntelliSense で知られています。
-   定数は相互参照されるので、特定の定数のすべての参照を見つけることができます。 これは、マクロのケースではありません。
-   定数は、プライベート、プロテクト、またはパブリックのいずれかのアクセス修飾子となります。 マクロのアクセシビリティが十分に理解されていないか、厳密に定義されていません。
-   Consts にはスコープがありますが、マクロにはスコープはありません。
-   デバッガーには定数の値および読み取り専用変数を表示することができます。

クラス スコープ (クラスの宣言) で定義されているマクロは、すべての派生クラスのすべてのメソッドで効率的に使用できます。 これはもともとレガシーなコンパイラ マクロ実装のバグでしたが、この抜け穴はアプリケーション プログラマがよく利用しています。 新しい X++ コンパイラには、この機能が残されていますが、この機能を使用する新しいコードは記述しないでください。 この特定の機能は、コンパイラのパフォーマンスにも大きく影響を与えます。 定数は、下記のようにクラス レベルで宣言できます。

    private const str MyConstant = 'SomeValue';

次に、定数を二重コロン構文を使用して参照することができます。

      str value = MyClass::MyConstant;

定数が定義されているクラスのスコープにいる場合は、型名の接頭語 (上記の例では MyClass) を省略できます。 このようにマクロ ライブラリの概念を簡単に実装することができます。 マクロ シンボルのリストは、パブリック const の定義を持つクラスになります。

### <a name="exercise"></a>練習

フリート アプリケーションには、以下のマクロ定義を含む FMDataHelper クラスが含まれています。

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

これらを定数定義に変更し、それに従ってマクロが使用される場所を更新します。

また、定数を変数のみとして定義することもできます。 コンパイラはインバリアントを維持して、値を変更できないようにします。

    {
      const int Blue = 0x0000FF;
      const int Green = 0x00FF00;
      const int Red = 0xFF0000;
    }

読み取り専用フィールドには値を 1 回だけ割り当てることがき、その値は変わりません。フィールドには、インラインで (フィールドが宣言した場所)、またはコンストラクターで値を割り当てることができます。 現時点では、定数と読み取り専用の唯一の違いです。

<a name="var"></a>Var
---

コンパイラが初期化式から種類を判断することができる場合は、変数の種類を明示的に提供せずに変数を宣言することができるようになりました。 変数が、まだ厳密に型指定されている明確な型であることに注意してください。 (コンパイラが型を推定する) 初期化式が用意されている宣言でのみ var を使用することができます。 コードを読みやすくできる状況がありますが、この機能を誤用すべきではありません。 次のルールを考慮してください。

-   代入の右側から見て変数の型が明らかである場合、または正確な型が重要でない場合は、var を使用してローカル変数を宣言します。


~~~
    // When the type of a variable is clear from the context, use var 
    // in the declaration. 
    var var1 = "This is clearly a string.";
    var var2 = 27; // This is an integer (not a real).
    var i = System.Convert::ToInt32(3.4);
~~~

-   種類が初期化式から明らかでない場合は、var を使用しないでください。

        // When the type of a variable is not clear from the context, use an 
        // explicit type. 
            int var4 = myObject.ResultSoFar();

-   for ループ カウンターの宣言には、var を使用します。
-   using 文内で破棄可能なオブジェクトには、var を使用します。

## <a name="private-and-protected-member-variables"></a>プライベートおよび保護されたメンバー変数
以前は、クラスで定義されたすべてのメンバー変数が可変保護されていました。 private、protected、および public キーワードを加えることにより、メンバー変数の表示を明示的にできるようになりました。 これらの修飾子の解釈は明白であり、メソッドのセマンティクスに沿っています。

-   プライベート メンバーは、定義されているクラス内でのみ使用できます。
-   保護されているメンバーは、それが定義されているクラスとそのすべてのサブクラスで使用できます。
-   パブリック メンバーは、どこででも使用することができ、定義されているクラス階層の範囲外に表示されます。

明示的なモディファイアーで実装されていないメンバー変数の既定値は、引き続き保護されています。 可視性を明示的に指定する習慣をつける必要があります。 説明のように、メンバー 変数が public として定義されている場合、定義されているクラス外で消費される可能性があります。 この場合、変数をホストしているオブジェクトを指定する修飾子は、(メソッド呼び出しの場合と同様に) ドット表記を使用して指定する必要があります。 上記のコードを再利用:

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

この場合、field1 には明示的な 'this' を使用してアクセスします。 修飾子。 **注記**: 消費者にクラスの内部作業を公開することになり、クラスの実装と消費者の間に強い依存関係が生じるため、メンバー変数をパブリックにすることはお勧めできません。 常に、実装ではなくコントラクトにのみ依存させる必要があります。

## <a name="finally-in-trycatch-statements"></a>最後に try/catch 明細書において
try/catch 文にオプションの finally 句を追加できるようになりました。 セマンティクスは C\# やその他のマネージド言語と同じです。 finally 句のステートメントは、通常または例外を介してコントロールが try ブロックを離れるときに実行されます。

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

## <a name="event-handlers-and-prepost-methods"></a>イベント ハンドラーおよび予備または転記メソッド
旧式 X++ では、特定のメソッドがメソッドの実行前後に実行されるようにメタデータで指定できました。 サブスクリプションが何を呼び出すかに関する情報は、パブリッシャーに記録されていますが、これは環境には役立ちません。 サブスクライバーに SubscribesTo 属性を指定することにより、コードを通じて前後のハンドラーを指定できるようになりました。

### <a name="example"></a>例

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

この例は、Publisher という公開メソッドを示しています。 2 人のサブスクライバーが PreHandlerFor と PostHandlerFor に登録されています。 このコードは、変数と戻り値にアクセスする方法を示しています。 **注記**: アプリケーション コードに重要なアプリケーション イベントを公開するための多数の委任がないため、この機能は下位互換性のために提供されています。 前後のハンドラーは、パラメーターの追加または変更のため、パラメータータイプの変更ため、メソッドが呼び出されなくなったり、別の状況で呼び出されたりしたために容易に中断する可能があります。 属性はバインディング イベント ハンドラーをデリゲートするためにも使用されます。

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

この場合、SubscribesTo 属性は、FmRentalCheckoutProcessor.RentalTransactionAboutToBeFinalizedEvent デリゲートが呼び出されたときにメソッド RentalFinalizedEventHandler を呼び出す必要があることを指定します。 パブリッシャーとサブスクライバーの間のバインディングは属性を通じて行われるため、サブスクライバーが呼び出される順序を指定する方法はありません。

## <a name="extension-methods"></a>拡張メソッド
拡張メソッド機能を使用すると、メソッドを別の拡張クラスに記述することによって、拡張メソッドを対象クラスに追加できます。 次のルールが適用されます。

-   拡張クラスは静的でなければなりません。
-   拡張クラスの名前は、10 文字の接尾語 \_Extension で終了する必要があります。 ただし、接尾辞に先行する名前の部分には制限はありません。
-   拡張子クラス内のすべての拡張子メソッドは、パブリック静的として宣言する必要があります。
-   すべての拡張メソッドの最初のパラメーターは、拡張メソッドが拡張する型です。 ただし、拡張メソッドが呼び出されると、呼び出し元は最初のパラメーターに対して何も渡す必要がありません。 代わりに、システムが最初のパラメーターに必要なオブジェクトを自動的に渡します。

拡張クラスにプライベートまたは保護された静的メソッドを含めることは完全に有効です。 これらは通常、実装の詳細に使用され、拡張として公開されません。 次の例は、いくつかの拡張メソッドを保持している拡張機能クラスを示しています。

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

### <a name="why-use-extension-methods"></a>なぜ拡張メソッドを使用しますか。

拡張メソッドの手法は、拡張するクラスのソース コードには影響しません。 したがって、クラスへの追加はオーバーレイなしで行うことができます。 ターゲット クラスへのアップグレードは、既存の拡張メソッドの影響を受けることはありません。 ただし、ターゲット クラスへのアップグレードで拡張メソッドとして同じ名前のメソッドが追加される場合、拡張メソッドはターゲット クラスのオブジェクトを通して到達できなくなります。 拡張メソッドは使いやすいです。 拡張メソッドの手法では、通常のインスタンス メソッドを呼び出すときによく使うドット区切り構文と同じものを使用します。 拡張メソッドは、ターゲット クラスのすべてのパブリック コンポーネントにアクセスできますが、保護されたまたはプライベートのオブジェクトにはアクセスできません。 この方法では、拡張メソッドは糖衣構文の種類とみなすことができます。

### <a name="where-can-extension-methods-be-applied"></a>拡張メソッドはどこに適用できるか

拡張メソッドのターゲットは、次のアプリケーション オブジェクト タイプのいずれかである必要があります。

-   クラス
-   テーブル
-   表示
-   マップ

目標タイプに関係なく、拡張機能*クラス*はタイプに拡張メソッドを追加するために使用されます。 たとえば、拡張テーブルは、メソッドをテーブルに追加するために使用されて*いません*し、拡張テーブルというものは存在しません。

## <a name="using-clauses"></a>句の使用
以前は、X++ で作成されなかったマネージド コンポーネントに対するすべての参照が、各タイプの名前空間を含むを完全修飾名を使用して行われていました。 これはまだ可能ですが、このようなコンポーネントの使用の煩わしさを軽減をするために、句を使用できます。 using ステートメントとは対照的に、各 using 句はその句が適用されるクラスに先行します。 完全修飾名の短縮名を導入するエイリアスを提供することもできます。 エイリアスは、以下に示すように名前空間とクラスを示すことができます。

### <a name="example"></a>例

次のコードを考慮してください。

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

## <a name="differences-between-legacy-x-and-new-x"></a>レガシー X++ と新しい X++ の違い
このセクションでは、旧式 X++ と新しい X++ の違いを説明します。

### <a name="reals-are-decimals"></a>Reals は Decimals です

実際の値を表すために使用されるタイプは、解釈された X++ から変更されています。 新しいタイプは、古いタイプの値をすべて表すことができるので、コードを書き直す必要はありません。 完全な開示のためにこの材料を提供します。 実数タイプのすべてのインスタンスが .NET 小数タイプ (System.Decimal) のインスタンスとして実装されます。 以前のバージョンでの real 型と同様に、バイナリ コード化された小数点以下の型での decimal 型は浮動小数点の型とは違い、丸め誤差に対する対応力があります。 10 進型の範囲と解像度は、元の型とは異なります。 元の X++ 実数型は 16 桁をサポートし、小数点の配置位置を指し示す指数をサポートしていました。 新しい X++ 実数型は、正の 79,228,162,514,264,337,593,543,950,335 (2⁹⁶-1) から 負の 79,228,162,514,264,337,593,543,950,335 (-(2⁹⁶-1)) までの 10 進数を表すことができます。 新しい実数型は、丸めの必要性を排除しません。 たとえば、次のコードは、1 ではなく 0.9999999999999999999999999999 という結果を生成します。 これは、以下の変数の値を表示するためにデバッガーを使用するとすぐに見られます。

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

1/3 の値を正確に表せる小数点以下の桁数はありません。 ここで得られる不一致は、有限数の小数しか提供されないことによるものです。 必要な小数点以下の桁数まで丸めるには、Round 関数を使用します。

      value = round(value, 2);

## <a name="internal-representation"></a>内部表示
10 進数は、符号と数値の桁ごとの値が 0～9 の範囲にある数値と、流動少数点の整数部と小数部分を区切るための位置を示すスケーリング係数で構成される浮動小数点値です。 実数値のバイナリ表現は、96ビットの整数を除算し、それが小数部分であることを指定するために使用する 1 ビットの符号、96ビットの整数、スケーリング係数で構成されます。 拡大縮小係数は、0 から 28 の範囲の指数に暗黙的に 10 を引いたものです。 したがって、10 進数のバイナリ表現は ((-2⁹⁶ ～ 2⁹⁶)/10(0\\ ～\\ 28)) を表します。ここで -(2⁹⁶-1) は表現できる最小値と等しく、2⁹⁶-1 は最大値に等しくなります。

## <a name="string-truncation"></a>文字列の切り捨て
文字列の切り捨ては、新しい機能ではありません。 ただし、コードが以前のバージョンの IL で実行されると、ここで説明されている自動文字列の切り捨ては行われません。 文字列値は、最大文字数を格納するために X++ で宣言できます。 これは通常、以下に示すように、この情報を拡張データ型でエンコードすることによって実現されます。クレジット カード番号は 20 文字を超えることはできません。 [![StringTruncationSolutionExplorer\_DebugFeatures](./media/stringtruncationsolutionexplorer_debugfeatures.png)](./media/stringtruncationsolutionexplorer_debugfeatures.png) 長さ制約を X++ 構文で直接指定することもできます。

    str 20 creditCardNumber;

これらの値に対するすべての割り当ては最大長に暗黙的に切り捨てられます。

### <a name="exercise"></a>練習

静的メイン メソッドに含めることにより、デバッガーで次のコードを実行します。

    creditCardNumber = "12345678901234567890Excess string";

## <a name="casting"></a>キャスティング
X++ の以前のバージョンは、型キャストの処理で、非常に少ない制限でした。 アップキャストとダウンキャストの両方が、プログラマの介在なしに許可されています。 レガシ X++ で許可されるキャストの一部は、.NET ランタイム環境の範囲に実装することはできません。 X++ を含む、オブジェクト指向のプログラミング言語では、キャストは宣言された型が両方同じ継承チェーンにある変数間の代入を表します。 キャストはダウン キャストまたはアップ キャストのいずれかです。 この説明の準備として、いくつかのわかりやすいクラス階層、[![Casting\_DebugFeatures](./media/casting_debugfeatures.png)](./media/casting_debugfeatures.png) を紹介します。ご覧のとおり、MotorVehicle クラスは Animal クラスとは関係ありません。 **up-cast** は派生型の式を基本型に割り当てる場合に発生します。

      Animal a = new Horse();

**down-cast**は、基本型の式を派生変数に代入する場合に発生します。

    Horse h = new Animal();

アップキャストとダウンキャストの両方が X++ でサポートされています。 ただし、ダウン キャストは危険であり、できる限り回避する必要があります。 割り当てが意味をなさないため、上記の例は実行時に InvalidCastException で失敗します。 X++ はオブジェクトおよび formrun などの、いくつかのタイプで遅延バインドをサポートします。 これは、つまり、そのメソッドがその型に対して明示的に宣言されていない場合、コンパイラは、コンパイル時に、それらの型に対して呼び出されているメソッドを見てもエラーを診断しないということを意味します。 開発者は彼らが何をしているかを把握しているとみなされます。 たとえば、フォーム内で検索される次のコードを参照してください。

    Object o = element.args().caller();
      o.MyMethod(3.14, “Banana”);

コンパイラは、このメソッドがオブジェクト クラスで宣言されていないため、MyMethod メソッドのパラメーター、戻り値などをチェックすることはできません。 実行時には、リフレクションを使用して呼び出しが行われます。これは通常の呼び出しよりも桁違いに低速化されます。 遅延バインディング型で実際に定義されているメソッドの呼び出しは必然的にチェックされることに注意してください。 たとえば、ToString() へ呼び出します。

    o.ToString(45);

コンパイル エラーの原因になります。

    'Object.toString' expects 0 argument(s), but 1 specified.

ToStringメソッド がオブジェクト クラスで定義されているため。 以前のバージョンの X++ の実装とは違いが 1 つあります。これは、たとえパラメーターのプロファイルが完全に正しくない場合でも、メソッドの名前が正しい限り、関連のないオブジェクトに対してメソッドを呼び出すことができるという事実に関連しています。 これは、CIL ではサポートされていません。

### <a name="example"></a>例

    public class MyClass2
    {
      public static void Main(Args a)
      {
        Object obj = new Car();
        Horse horse = obj; // exception now thrown
        horse.run();    // Used to call car.run()!
      }
    }

コード内で IS 演算子と AS 演算子を自由に使用する必要があります。 指定した式が特定の型 (派生型を含む) の場合は、IS 演算子を使用することができます。AS 演算子は、特定のタイプへのキャストを実行し、キャストが使用できない場合は null を返します。

## <a name="compiler-diagnoses-attempts-to-store-objects-in-containers"></a>コンパイラは、オブジェクトをコンテナに格納しようとすると診断します
以前の X++ コンパイラでは、実行時に失敗した場合でもコンテナーにオブジェクト参照を格納することができました。 これは不可能です。 コンパイラは、コンテナーへのオブジェクト参照の保存の試みを確認したとき

    container c = [new Query()];

エラー メッセージを発行します。

    Instances of type 'Query' cannot be added to a container.

コンテナーに追加される要素のタイプが任意のタイプである場合、コンパイラーは値は参照タイプであるかどうかを決定することをできません。 コンパイラは、ユーザーが何をしているのかを把握していることを前提としてこれを許可します。 コンパイラは次のコードを誤っていると診断しません。

    anytype a = new Query();
            container c = [a];

しかし、実行時にエラーがスローされます。

## <a name="cross-company-clause-can-contain-arbitrary-expressions"></a>会社間の句には任意の式を含めることができます
会社間の句は、検索ステートメントを考慮する必要のある会社を示すために select ステートメントで使用できます。 構文は、コンテナー型の変数である単一の識別子ではなく、コンテナー型の任意の式を許可するように拡張されています。

      private void SampleMethod()
      {
        MyTable t;
        container mycompanies = ['dat', 'dmo'];
        select crosscompany: mycompanies t;
      }

現在は、この目的で変数を使用することなく、式を指定することができます。

      private void SampleMethod()
      {
        MyTable t;
        container mycompanies = ['dat', 'dmo'];
        select crosscompany: (['dat'] + ['dmo']) t;
      }

## <a name="mkdate-predefined-function-no-longer-accepts-shorthand-values"></a>定義済みの mkDate 関数はショートハンド値を受け入れません
旧式システムでは、mkDate 関数の年の引数に「短縮形」の値を使用できました。 結果は、次のコード サンプルで確認できます。

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

レガシ システムでこのコードを実行すると、次の値が生成されます: 0 – 2000 1 – 2001 2 – 2002 … 27 - 2027 28 - 2028 29 - 2029 **30 - 2030** **31 - 1931** 32 - 1932 33 - 1933 … 97 - 1997 98: 1998 **99 - 1999** **100 - 1900** これらの値はもうサポートされません。 このような値を使用しようとすると、mkDate 関数は null の日付 (1900年1月1日) を返します。

## <a name="obsolete-statement-types"></a>古いステートメント タイプ
次のステートメントがサポートされなくなりました。

### <a name="pause-and-window-statements"></a>一時停止およびウィンドウ ステートメント

X++ pause ステートメントは、影響下にあったポップアップ **印刷ウィンドウ**が削除されたため、現在はサポートされていません。 pause および window ステートメントは主に、実行環境と同じである、MorphX 開発環境内でデバッグのために使用されていました。 2 つが分離されたため、MorphX 環境を Visual Studio に置き換えると、これらのステートメントに関連性がなくなります。

### <a name="print-statement"></a>明細書の印刷

X++ print ステートメントは、デバッグのためだけに存在していた、もう 1 つのステートメントです。 これはまだ存在しており、その基本的な考えは変わりません。 ただし、印刷は System.Diagnostics.WriteLine を通じて出力されるようになりました。 製品の構成では、送付された書面による情報の詳細を決定します。 [![DebuggingAdmin\_DebugFeatures](./media/debuggingadmin_debugfeatures.png)](./media/debuggingadmin_debugfeatures.png) 情報ログを使用することにより、出力がデバッガーおよび実行中のフォームに表示されるため、より魅力的になります。

## <a name="the-ignore-list"></a>Ignore リスト
従来の環境はすべて解釈されたため、一部のパーツをコンパイルせず、残りの部分を使用することも可能でした。 正常にコンパイルしたメソッドのみを呼び出す場合、問題はありません。ただし、正常にコンパイルされなかったメソッドを呼び出そうとすると、問題が発生します。 この作業方法は CIL では機能しません。 アセンブリは正常に行われたコンパイルから生成され、ランタイム システムは未完了の組み立てを読み込むことができません。 しかし、従来のアプリケーションを新しい環境に移植する際には、段階的なやり方で実行することが有益であり、すべてを移植する前にアプリケーションの一部をテストする必要もあり、そのための正当なシナリオがあります。 これはこの非常に限定されたシナリオでは役立ちますが、システムが展開された後は、実行時に発生する問題を隠してしまう可能性があるため、アプリケーションの生産準備ができた後は使用すべきではありません。 プロジェクトのコンテキスト メニューから「ベスト プラクティスの抑制を編集」を選択することで、XML でメソッドを指定できます。 これにより、除外項目を管理する XML ドキュメントが開きます。

## <a name="new-debugger-features"></a>新しいデバッガーの機能
このセクションでは、Visual Studio のデバッグ環境に追加した新機能について説明します。

### <a name="adding-tostring-methods-to-your-classes"></a>クラスへの ToString メソッドの追加

多くの場合、ToString() メソッドをクラスに追加することが利点となります。 これを行うのに費やした労力は何度も戻ってきます。それは簡単です。 このアドバイスは、レガシ X++ にも当てはまります。 **注記**: ToString メソッドが予期しない時に呼び出されることがあるため、ここでオブジェクトの状態を変更することはお勧めできません。

### <a name="identifying-unselected-fields"></a>選択されていないフィールドの識別

フィールドが select ステートメントのフィールドの一覧に表示されない場合に、テーブルのフィールドを使用することがバグの一般的な発生源となります。 このようなフィールドには、そのタイプに従って既定値が設定されます。 値が選択されているかどうかはデバッガーで確認できるようになりました。

#### <a name="exercise"></a>練習

次のコードを考慮してください。

    class MyClass
    {
      public static void Main(Args a)
      {
        FMRental rental;

        select EndMileage, RentalId from rental;

        rental.Comments = "Something";
      }
    }

代入ステートメントにブレークポイントを設定します。 クラスをプロジェクトのスタートアップ オブジェクトにして、F5 キーを押して開始します。 ブレークポイントが検出されたときは、ローカル ウィンドウでレンタル変数を展開して表示します。 次の図に似たものが表示されます。 [![DebuggingAdmin2\_DebugFeatures](./media/debuggingadmin2_debugfeatures.png)](./media/debuggingadmin2_debugfeatures.png) 選択されていないフィールドが null として表示されるとき、選択された値で表示される選択されたフィールド (EndMileage および RentalId) を確認できます。 これは、その値がデータベースからフェッチされなかったことを示します。 当然、これはデバッグ コンポーネントです。 選択されていないフィールドの値は、フィールドのタイプの規定値になります。 これをステップオーバーし、デバッガーが実際の値のレンダリングをどのように変更するかを確認します。 **注記**: テーブルがキャッシュに設定されている場合、システムは常にコードに含まれるフィールド リストに関係なく、テーブル全体からすべてのフィールドをフェッチします。

### <a name="the-auto-and-infolog-windows"></a>自動および情報ログ ウィンドウ

デバッガーを使用すると、アプリケーションの状態の特定の部分にアクセスできます。 この情報は、現在の会社、パーティション、トランザクション レベル、および現在のユーザー ID が一覧表示される [自動] ウィンドウで使用できます。 [![自動 \_DebugFeatures](./media/autos_debugfeatures.png)](./media/autos_debugfeatures.png) また、情報ログに書き込まれるデータを示すウィンドウもあります。 [![Infolog\_DebugFeatures](./media/infolog_debugfeatures.png)](./media/infolog_debugfeatures.png)

### <a name="new-breakpoint-features"></a>新しいブレークポイント機能

Visual Studio デバッガーでは、条件付きブレークポイントと、ヒット カウントによってトリガーされたブレークポイントをサポートします。 また、ブレークポイントをヒットするとき、ユーザーのためにシステムが特定のアクションを実行させることができます。 これらの機能のいずれも従来のデバッガーでは使用できませんでした。 これらについて以下に詳しく説明します。

-   ヒット カウントを使用することで、デバッガーが実行を中断する前にブレークポイントがヒットする回数を決定できます。 既定では、デバッガーはブレークポイントがヒットするたびに実行を中断します。 ブレークポイントが 2 回ヒットするたび、または 10 回ヒットするたび、または 512 回ヒットするたび、またはユーザーが選択した回数ヒットするたびにデバッガーが中断するよう、ヒット カウントを設定することができます。 一部のバグは、最初にユーザー プログラムがループを実行し、関数を呼び出し、または変数へアクセスする際に現れないため、ヒット数は役に立ちます。 場合によっては、100 回または 1000 回繰り返すまでバグが表示されない可能性があります、 このような問題をデバッグするには、ヒット数が 100 または 1000 のブレークポイントを設定します。
-   条件は、ブレークポイントがヒットするかスキップするかを決定する式です。 デバッガーは、ブレークポイントに到達すると、条件を評価します。 条件が満たされた場合にのみ、ブレークポイントにヒットします。 場所ブレークポイントを持つ条件を使用して、特定の条件が true の時にのみ指定された場所で停止することができます。 たとえば、勘定残高がマイナスにならないように、銀行決済プログラムをデバッグしているとします。 コード内の特定の場所でブレークポイントを設定し、残高 &lt; 0 などの条件をそれぞれに添付する場合があります。 プログラムを実行するとき、残高が 0 より小さい場合にのみこれらの場所で実行が中断されます。 最初のブレークポイントの位置で変数およびプログラムの状態を調べ、2 つ目のブレークポイントの位置まで実行を続行、などを実行することができます。
-   アクションは、ブレークポイントがヒットした場合に発生する必要のあるものを指定します。 既定では、デバッガーは実行を中断しますが、代わりにメッセージを印刷するか Visual Studio マクロを実行するかを選択できます。 中断するのではなく、メッセージを印刷する場合は、ブレークポイントは Trace ステートメントと非常に類似します。 このブレークポイントを使用するメソッドはトレース ポイントと呼ばれます。

#### <a name="exercise"></a>練習

次のコードを考慮してください。

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

そのステートメントが選択されているときに F9 キーを押すことで、印刷明細書にブレークポイントを設定します。 これにより、通常の無条件ブレークポイントが作成されます。 ここで、マウスを使用して、ブレークポイントのコンテキスト メニューを開き、**条件**を選択します。 "i" 変数が 5 を超えたときにブレークポイントが発生することを示す条件を配置します。 スタートアップ プロジェクトとしてクラスを設定し、プロジェクト内のスタートアップ項目としてコードを含むクラスを設定します。 コードを実行します。 デバッガーを使用して「i」の値を自由に変更してください。 ここで、このブレークポイントを削除し、ヒット カウント機能を使用して同じことを実現します。 **注記**: ブレークポイントにはいくつかの条件があります。 多くの場合、ブレークポイントにカーソルを置くと役立つツールヒントが表示されれば便利です。 トレース ポイントは、しばしばトレースの実行に役立ちます。 対象の行に追跡ポイントを挿入し、変数の値を記録します。 トレース出力がデバッガーの出力ウィンドウに表示されます。

### <a name="the-immediate-window"></a>直接ウィンドウ

直接ウィンドウは VS デバッガーの便利な機能で、ユーザーはいつでも評価するために式と明細書を入力できます。 この機能は現在、X++スタックには実装されていません。多くの言語、特に \# の場合と同様です。 ただし、それは精通したユーザーが直接ウィンドウから益を得られないという意味ではありません。 スニペットは X++ ではなく C\# で表す必要があることを示すだけです。 これがどのように大きな効果を発揮するかについての詳細を記述した、別のドキュメントがあります。



