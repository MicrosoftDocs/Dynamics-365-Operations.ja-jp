---
title: クラスの拡張機能 - メソッドのラッピングとコマンド チェーン
description: このトピックでは、メソッド ラッピングを使用してパブリック メソッドと保護メソッドのビジネス ロジックを拡張する方法について説明します。
author: ChrisGarty
manager: AnnBe
ms.date: 12/18/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Developer
ms.reviewer: sericks
ms.search.scope: Operations
ms.search.region: Global
ms.author: cgarty
ms.search.validFrom: 2017-08-21
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 934fce4db88780f341932b74785da7d88e9d32df
ms.sourcegitcommit: 2b890cd7a801055ab0ca24398efc8e4e777d4d8c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/07/2019
ms.locfileid: "1506302"
---
# <a name="class-extension-via-method-wrapping-and-chain-of-command-coc"></a>メソッドのラッピングとコマンド チェーン経由のクラスの拡張機能 (CoC)

[!include [banner](../includes/banner.md)]

クラス拡張やクラス強化の機能が、Microsoft Dynamics 365 for Finance and Operations で強化されました。 強化対象である基本クラスで定義されたメソッド関連のロジックをラップできるようになりました。 イベント ハンドラーを使用せずに、パブリック メソッドとプロテクト メソッドのロジックを拡張することができます。 メソッドをラップするとき、基本クラスのパブリック メソッドと保護されたメソッド、および変数にもアクセスできます。 この方法で、トランザクションを開始し、クラスに関連付けられた状態変数を容易に管理することができます。

たとえば、モデルには次のコードが含まれています。

```
class BusinessLogic1
{
    str doSomething(int arg) 
    {
        // ...
    }
}
```

同じメソッド名を再利用することにより、拡張クラス内の **doSomething** メソッドの機能を強化することができるようになりました。 拡張クラスは強化されたクラスが定義されているモデルを参照するパッケージに属している必要があります。

```
[ExtensionOf(classStr(BusinessLogic1))]
final class BusinessLogic1_Extension
{
    str doSomething(int arg) 
    {
        // Part 1
        var s = next doSomething(arg + 4);
        // Part 2
        return s;
    }
}
```


この例では、**doSomething** のラッパーと **next** キーワードを必要に応じて使用することにより、メソッドのコマンド チェーン (CoC) を作成します。 CoC は、要求が一連の受信者によって処理される設計パターンです。 パターンは、送信者と受信者の疎結合をサポートします。

現在は次のコードを実行します。

```
BusinessLogic1 object = new BusinessLogic1();
info(object.doSomething(33));
```

このコードが実行されると、システムは、**doSomething** メソッドをラップするメソッドを検索します。 システムは、**BusinessLogic1_Extension** クラスの **doSomething** メソッドなど、これらのメソッドの 1 つをランダムに実行します。 次の **doSomething** メソッドへの呼び出しが発生すると、システムは CoC 内の別のメソッドをランダムに選択します。 ラップされたメソッドがこれ以上ない場合は、システムは元の実装を呼び出します。

## <a name="supported-versions"></a>サポートされているバージョン
> [!IMPORTANT]
> このトピックで説明する機能 (CoC および保護されたメソッドと変数へのアクセス) は、Platform update 9 で利用できます。 ただし、強化されているクラスは、プラットフォーム更新プログラム 9 またはそれ以降でコンパイルされる必要があります。 2017 年 8 月現在、Finance and Operations のアプリケーションの現在のリリースはすべて Platform Update 8 またはそれ以前でコンパイルされています。 したがって、基本パッケージ (Application Suite など) で定義されているメソッドをラップするには、プラットフォーム更新 9 以降でその基本パッケージを再コンパイルする必要があります。
例: アプリケーション スイート モデルに存在するクラスを増補する独自の拡張モデルを作成し、CoC を使用している場合や保護されたメソッド/変数にアクセスする場合は、アプリケーション スイートと拡張モデルの両方を構築する必要があります。 ランタイム環境でこの機能を配置するには、両方のモデルを含む配置可能なパッケージを作成する必要があります。
これは、Dynamics 365 for Finance and Operations アプリケーションの次のリリースまでの一時的な状況です。

## <a name="capabilities"></a>処理能力
次のセクションでは、ラッピング メソッドと CoC メソッドの機能について詳しく説明します。

### <a name="wrapping-public-and-protected-methods"></a>パブリック メソッドと保護対象メソッドのラッピング
クラス、テーブル、データ エンティティ、またはフォームの保護またはパブリック メソッドは、拡張子クラスを使用してラップできます。 ラッパー メソッドは、基本メソッドと同じシグネチャを持つ必要があります。

- フォーム クラスを拡張するときは、ルート レベルのメソッドのみをラップできます。 入れ子になったクラスで定義されているメソッドをラップすることはできません。
- 現在のところ、通常のクラスで定義されているメソッドのみラップできます。 拡張クラスで定義されているメソッドは、拡張クラスを強化してラップできません。 この機能は、将来の更新で計画されています。

### <a name="what-about-default-parameters"></a>既定のパラメーターはどうなのですか ?
既定のパラメーターを持つメソッドは、拡張クラスでラップできます。 ただし、ラッパー メソッドのメソッド シグネチャは、パラメータの既定値を含む必要がありません。

たとえば、次の簡単なクラスには、既定のパラメーターを持つメソッドがあります。

``` 
class Person 
{
    public void salute(str message = "Hi") {...}
}
```

この場合、ラッパー メソッドは次の例のようにする必要があります。

```
[ExtensionOf(classStr(Person))]
final class APerson_Extension
{
    public void salute(str message)
    {
        // ...
    }
}
```

**APerson_Extension** 拡張子クラスで、**salute** メソッドが**メッセージ** パラメーターの既定値に含まれていないことを確認します。 

### <a name="wrapping-instance-and-static-methods"></a>インスタンス メソッドと静的メソッドをラッピング
インスタンスと静的メソッドは、拡張クラスでラップできます。 静的メソッドがラップされるターゲットである場合、**静的**キーワードを使用して拡張内のメソッドを指定する必要があります。

たとえば、次の **A** クラスがあります。

```
class A 
{
    public static void aStaticMethod(int parameter1)
    {
        // ...
    }
}
```
 
この場合、ラッパー メソッドは次の例のようにする必要があります。

```
[ExtensionOf(classStr(A)]
final class An_Extension
{
    public static void aStaticMethod(int parameter1)
    {
        // ...
        next aStaticMethod(parameter1);
    }
}
```

> [!IMPORTANT]
> 静的メソッドをラップする機能はフォームには適用されません。 X++ では、フォーム クラスは新しいクラスではなく、インスタンスを作成したり通常クラスとして参照したりできません。 フォーム内の静的メソッドにはセマンティクスがありません。

### <a name="wrapper-methods-must-always-call-next"></a>ラッパー メソッドは常に次を呼び出す必要があります 

拡張クラス内のラッパー メソッドは常に **次** を呼び出す必要があるため、チェーン内の次のメソッド、および最後には常に元の実装が呼び出されます。 この制限により、チェーン内のすべてのメソッドが結果に寄与することが保証されます。

この制限の現在の実装では、**次**の呼び出しはメソッド本体の第 1 レベルのステートメントである必要があります。

いくつかの重要なルールを次に示します。

- **if** 文の中で、条件付きで **next** への呼び出しを行うことはできません。 
- **while**、**do-while**、または **for** ループ ステートメント内で **next** への呼び出しを行うことはできません 
- **次**ステートメントの前に、**戻る**ステートメントを置くことはできません。 
- 論理式は最適化されているため、**次へ**の呼び出しは論理式では実行できません。 実行時に、完全な式の実行は保証されません。

> [!NOTE]
> メソッドが置き換え可能な場合は、拡張担当者はコマンド チェーンを使用してメソッドをラップするときに無条件に **next** を呼び出す必要はありません。 拡張担当者はチェーンを中断できますが、条件がある場合のみ中断することが期待されます。 コンパイラは、属性 **Replaceable** を持つメソッドの **next** の呼び出しを強制しません。  

### <a name="wrapping-a-base-method-in-an-extension-of-a-derived-class"></a>派生クラスの拡張で基本メソッドをラッピング
次の例は、派生クラスの拡張機能で基準メソッドをラップする方法を示しています。 この例では、次のクラス階層が使用されます。

```
class A
{
    public void salute(str message)
    {   
        info(message);
    }
}

class B extends A {}
class C extends A {}
```

したがって、1 つの基本クラス **A** があり、2 つのクラス **B** および **C** が **A** から派生します。ここに示すように、派生クラスの 1 つ (この場合は **B**) の拡張クラスを追加または作成します。

```
[ExtensionOf(classStr(B))]
final class B_Extension
{
    public void salute(str message)
    {
        next salute(message);
        info("B extension");
    }
}
```

**B_Extension** クラスは **B** の拡張子ではあり、**B** は **salute** メソッドのメソッドの定義がありませんが、**salute** メソッドを基本クラス **A** で定義しラップすることができます。したがって、**B** クラスのインスタンスのみが **salute** メソッドのラッピングを含みます。 **A** クラスおよび **C** クラスのインスタンスは、**B** クラスの拡張機能に定義されているラッパー メソッドを呼び出すことはありません。 

これらの 3 つのクラスを使用するメソッドを実装すると、この動作はより明確になります。

```
class ProgramTest 
{
    public static void main(Args args)
    {
        var a = new A();
        var b = new B();
        var c = new C();

        a.salute("Hi");
        b.salute("Hi");
        c.salute("Hi");
    }
}
```

**a.salute(「Hi」)** および **c.salute(「Hi」)** の呼び出しでは、情報ログに「Hi」のメッセージのみが表示されます。 ただし、**b.salute(「Hi」)** が呼び出されると、情報ログは「Hi」に続いて 「B 拡張子」を表示します。 

このメカニズムを使用することによって、特定の派生クラスに対してのみ元の方法をラップすることができます。

### <a name="accessing-protected-members-from-extension-classes"></a>拡張クラスから保護されたメンバーへのアクセス
プラットフォーム更新プログラム 9 では、拡張クラスから保護されたメンバーにアクセスできます。 これらの保護されたメンバーには、フィールドとメソッドが含まれます。 このサポートは、メソッドのラップに固有ではありませんが、クラス拡張内のすべてのメソッドを適用することに注意してください。 したがって、クラス拡張は以前よりも強力です。

### <a name="the-hookable-attribute"></a>Hookable 属性
メソッドが **[Hookable(false)]** として明示的にマークされている場合、メソッドを拡張子クラスで囲むことはできません。 次の例では、**anyMethod** は **AnyClass1** を補強するクラスでラップできません。

```
class AnyClass1 
{
    [HookableAttribute(false)]
    public void anyMethod() {...}
}
```

### <a name="final-methods-and-the-wrappable-attribute"></a>最終的な方法および Wrappable 属性
**final** とマークされているパブリック メソッドと保護されたメソッドは、拡張クラスでラップできません。 **Wrappable** 属性を使用して属性パラメーターを **true** (**[Wrappable(true)]**) に設定することにより、この制限をオーバーライドすることができます。 同様に、(最終ではない) パブリックまたは保護されたメソッドの既定の機能を無効にするには、折り返し不可としてこれらのメソッドをマークすることができます (**[Wrappable(false)]**)。

次の例では、**doSomething** メソッドは、パブリック メソッドである場合でもラップできないものとして明示的にマークされます。 **doSomethingElse** メソッドは、最後のメソッドであっても、折り返し可能と明示的にマークされます。

```
class AnyClass2 
{
    [Wrappable(false)]
    public void doSomething(str message) {...}

    [Wrappable(true)]
    final public void doSomethingElse(str message) {...}
}
```


### <a name="extensions-of-form-nested-concepts-such-as-data-sources-data-fields-and-controls"></a>データ ソース、データ フィールド、および制御といったフォームで入れ子になった概念の拡張

データ ソース、データ フィールド、コントロールなど、フォームで入れ子になった概念の CoC メソッドを実装するため、入れ子になった各概念には拡張クラスが必要です。 

#### <a name="form-data-sources"></a>フォーム データ ソース

この例では、**FormToExtend** はフォーム、**DataSource1** はフォームで有効な既存のデータ ソース、**init** と **validateWrite** はデータ ソースで折り返し可能なメソッドです。

```C#
[ExtensionOf(formdatasourcestr(FormToExtend, DataSource1))]
final class FormDataSource1_Extension
{
    public void init()
    {
        next init();
        //...
        //use element.FormToExtendVariable to access form's variables and datasources
        //element.FormToExtendMethod() to call form methods
    }
 
    public boolean validateWrite()
    {
        boolean ret;
        //...
        ret = next validateWrite();
        //...
        return ret;
    }
}
```

#### <a name="form-data-fields"></a>フォーム データ フィールド

この例では、データ フィールドが拡張されます。 **FormToExtend** はフォーム、**DataSource1** はフォームのデータ ソース、**Field1** はデータ ソースのフィールド、**validate** はこの入れ子になった概念で折り返し可能な多くのメソッドのいずれかです。

```C#
[ExtensionOf(formdatafieldstr(FormToExtend, DataSource1, Field1))]
final class FormDataField1_Extension 
{ 
    public boolean validate()
    {
        boolean ret
        //...
        ret = next validate();
        //...
        return ret;
    }
}
```

#### <a name="controls"></a>コントロール

この例では、**FormToExtend** はフォーム、**Button1** はフォーム内のボタン コントロール、**clicked** はボタン コントロールで折り返し可能なメソッドです。

```C#
[ExtensionOf(formControlStr(FormToExtend, Button1))]
final class FormButton1_Extension
{
    public void clicked()
    {
        next clicked();
        //...
    }
}
```

#### <a name="requirements-and-considerations-when-you-write-coc-methods-on-extensions-for-form-nested-concepts"></a>フォームで入れ子になった概念で CoC メソッドを書き込むときの要件と考慮事項

- その他の CoC メソッドと同様、これらのメソッドは常に **next** を呼び出してチェーン内の次のメソッドを呼び出す必要があります。これにより、チェーンは実行時の動作でカーネルまたはネイティブ実装まで進むことができます。 next の呼び出しは、ランタイムにおける基本の動作が常に正常に実行されることを保証する、フォーム自体からの **super()** の呼び出しに相当します。
- 現時点では、Microsoft Visual Studio の X++ エディターは、折り返し可能なメソッドの検出をサポートしていません。 したがって、折り返し対象となるメソッドとその正確なシグネチャを識別するための入れ子になった各概念については、システムのドキュメントを参照する必要があります。
- 入れ子になったコントロール タイプの元の基本動作で定義されていないメソッドをラップする CoC を追加することは**できません**。 たとえば、拡張において **methodInButton1** CoC を追加することはできません。 ただし、制御の拡張からは、メソッドがパブリックまたは保護として定義されている場合にこのメソッドへの呼び出しを行うことができます。 以下に、**methodInButton1** メソッドと同じように **Button1** コントロールが **FormToExtend** フォームで定義される例を示します。

    ```C#
    [Form]
    public class FormToExtend extends FormRun
    {
        [Control("Button")]
        class Button1
        {
            public void methodInButton1(str param1)
            {
                info("Hi from methodInButton1");
                //...
    ```

- 拡張からのそのフォームで入れ子になった概念における CoC メソッドをサポートするために元のフォームが定義されたモジュールを再コンパイルする必要は**ありません**。 たとえば、前の例の **FormToExtend** フォームが **ApplicationSuite** モジュールにある場合、異なるモジュールからそのフォームで入れ子になった概念の CoC で拡張するために **ApplicationSuite** を再コンパイルする必要はありません。

### <a name="extensions-of-tables-and-data-entities"></a>テーブルとデータ エンティティの拡張機能

拡張機能クラスは、概念ごとに必要です。 

#### <a name="tables"></a>テーブル

この例では、**TableToExtend** はテーブルであり、**delete**、**canSubmitToWorkflow**、**caption** はテーブルでラップできるメソッドです。

```C#
[ExtensionOf(tablestr(TableToExtend))]
final class TableToExtend_Extension
{
    public void delete()
    {
        next delete();
        //...
    }
 
     public boolean canSubmitToWorkflow(str _workflowType)
    {
        boolean ret;
        //...
        ret = next canSubmitToWorkflow(_workflowType);
        //...
        return ret;
    }
        
    public str caption()
    {
        str ret;
        //...
        ret = next caption();
        //...
        return ret;
    }
}
```

#### <a name="data-entities"></a>データ エンティティ
この例では、**DataEntityToExtend** はデータ エンティティで、**validateDelete** および **validateWrite** はデータ エンティティでラップできるメソッドです。

```C#
[ExtensionOf(TableStr(LedgerJournalEntity))]
final class LedgerJournalEntity_Extension
{
        public boolean validateDelete()
    {
        boolean ret;
        //...
        ret = next validateDelete();
        //...
        return ret;
    }

    public boolean validateWrite()
    {
        boolean ret;
        //...
        ret = next validateWrite();
        //...
        return ret;
    }
}
```

## <a name="restrictions-on-wrapper-methods"></a>ラッパー メソッドに関する制限事項
次のセクションでは、CoC およびメソッド ラッピングの使用上の制限について説明します。

### <a name="x-classes-that-are-compiled-by-using-platform-update-8-or-earlier"></a>プラットフォーム更新プログラム 8 またはそれ以前を使用してコンパイルされた X++ クラス 
メソッドのラッピング機能には、プラットフォーム update 9 以降の一部である X++ コンパイラによって出力される特定の機能が必要です。 以前のバージョンを使用してコンパイルされたメソッドには、この機能をサポートするインフラストラクチャはありません。

### <a name="methods-on-types-nested-within-forms-can-be-wrapped-in-platform-update-16-and-later"></a>プラットフォーム更新 16 以降ではフォーム内で入れ子になったタイプのメソッドをラップできます。
クラス拡張を使用してフォーム (データ ソースとコントロール) 内で入れ子になった型のメソッドをラップする機能がプラットフォーム更新 16 で追加されました。 つまり、コマンド チェーンを使用して、データ ソース メソッドおよびフォーム制御メソッドのオーバーライドを提供できます。

ただし、これらの入れ子にされた型 (フォーム コントロールとフォーム データ ソース) の純粋な X++ メソッドのラップ (拡張) は、他の型 (フォーム、テーブル、データ エンティティ) と同様にまだサポートされていません。 現時点では、開発者は、フォーム内の型の純粋な X++ メソッドでコマンド チェーンを使用する場合、コンパイルしますが、実行時に拡張メソッドじゃ呼び出されません。 この機能は、将来の更新で計画されています。

### <a name="unimplemented-system-methods-on-tables-and-data-entities-can-be-wrapped-in-platform-update-22-and-later"></a>テーブルとデータ エンティティの実装されていないシステム メソッドは、プラットフォーム更新 22 以降でラップできます。
クラス拡張を使用して入れ子になったクラスでメソッドをラップする機能がプラットフォーム更新 16 で追加されました。 X++ の入れ子になったクラスの概念は、データソース メソッドやフォームコ ントロール メソッドを上書きするためのフォームに適用されます。

### <a name="next-calls-can-be-put-inside-trycatchfinally-in-platform-update-21-and-later"></a>プラットフォーム更新 21 以降では、次の呼び出しを try/catch/finally 内に配置できます 
CoC 拡張メソッドでは、次の呼び出しを条件付きで呼び出してはなりません。 ただし、プラットフォーム更新 21 以降では、例外およびリソースのクリーンアップの標準的な処理を許可するため、次の呼び出しを try/catch/finally 内に配置できます。

```C#
    public void someMethod()
    {
        try
        {
            //...
            next updateBalances();
            //...
        }
        catch(Exception::Error)
        {
            //...
        }
    }
```

### <a name="extensions-of-extensions-are-not-yet-supported"></a>拡張機能の拡張機能はまだサポートされていません
現在のところ、通常のクラスで定義されているメソッドのみラップできます。 拡張クラスで定義されているメソッドは、拡張クラスを強化してラップできません。 この機能は、将来のリリースで計画されています。

### <a name="tooling"></a>ツール
このトピックに記載されている機能については、Microsoft Visual Studio X++ エディターは、相互参照および Microsoft IntelliSense の完全なサポートまだ提供していません。 Dynamics 365 for Finance and Operations プラットフォーム更新プログラム 10 で完全なサポートが利用できるようにする予定です。
