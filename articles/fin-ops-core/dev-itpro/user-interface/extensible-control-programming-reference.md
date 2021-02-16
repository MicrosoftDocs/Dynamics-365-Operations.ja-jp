---
title: 拡張可能なコントロールのプログラミング リファレンス
description: このトピックでは、拡張可能なコントロール プログラミングの参考資料を提供します。
author: TLeforMicrosoft
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Developer, IT Pro
ms.reviewer: rhaertle
ms.custom: 50211
ms.assetid: 0a774c73-9e5d-4faa-8716-61476c1a9b6e
ms.search.region: Global
ms.author: tlefor
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: a3abaf0e94ebf1413dfe323d058a6750b834672d
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 12/05/2020
ms.locfileid: "4686610"
---
# <a name="extensible-control-programming-reference"></a>拡張可能なコントロールのプログラミング リファレンス

[!include [banner](../includes/banner.md)]

このトピックでは、拡張可能なコントロール プログラミングの参考資料を提供します。

このドキュメントでは、拡張可能なコントロールを作成するための API、HTML、および JavaScript のサポートについて説明します。

## <a name="examples"></a>例
このドキュメントには、文書化されている各 API の使用方法を示す小さなコード スニペットが含まれています。 これらの API の多くを活用する完成したコントロールのより完全な例は Github で確認できます。 [Github での拡張可能コントロールの例](https://github.com/Microsoft/Dynamics-AX-Extensible-Control-Samples)

## <a name="control-block-diagram"></a>コントロール ブロック図
この高度な図は、拡張可能なコントロールの主要コンポーネントと、それらが相互にやり取りする方法を示しています。 拡張可能なコントロール ソリューションには、コントロールを実装する 2 つの X++ クラスが含まれます。 ランタイム クラスは、ランタイム データ、プレゼンテーション、コントロールの動作を実装します。 ビルド クラスは、コントロールがフォーム デザイナー、プロパティ ウィンドウ、およびアプリケーション エクスプローラーでどのように表示されるかを定義します。 [![Extensibility アーキテクチャ](./media/extensibilityarchitecture.png)](./media/extensibilityarchitecture.png)

<a name="x"></a>X++
---

コントロールの X++ API は、フォーム開発者向けの API です。 コントロールの X++ API を設計する際には、フォーム開発者に提供する API とビヘイビアーを考慮してください。

## <a name="runtime-the-x-runtime-class"></a>ランタイム: X++ ランタイム クラス
ランタイム クラスは、開発者向け API をコントロール用に定義します。 これには、コントロールのランタイム ロジックも含まれます。 実行時クラスの仕事は、コントロールのプロパティを使用してコントロールの状態を維持することです。

## <a name="runtime-class-declaration"></a>ランタイム: クラス宣言
<strong>FormTemplateControl</strong> または <strong>FormTemplateControl</strong><em> から派生した型を拡張する X++ クラスを宣言します。***FormTemplateControl</em>* には、テンプレート ID やリソース バンドルなど、すべてのコントロールに必要な基本的なプロパティが含まれています。 次の例では、基本コントロール クラス、<strong>FormTemplateControl</strong> を拡張しています。

```xpp
class MyControl extends FormTemplateControl
```

## <a name="runtime-formcontrolattribute"></a>ランタイム: FormControlAttribute
**FormControlAttribute** 属性を X++ クラス宣言に適用する必要があります。

```xpp
[FormControlAttribute(<Template ID>, <Resource Bundle Path>, <Build class name>))]
```

以下の引数を供給する必要があります。

-   **テンプレート ID**: テンプレートの ID を指定する文字列。 テンプレート ID は JavaScript クラス名であり、コントロールの HTML 要素 ID です。 慣例として、TemplateID はコントロールのランタイム クラスのクラス名と一致します。
-   **リソース バンドル パス**: リソース バンドルへのパスを指定する文字列。 リソース バンドル パスは、主要な HTM ファイルが置かれている Web パスです。 実行時に、クライアント フレームワークはリソース バンドル パスで指定された HTM ファイルを読み込みます。 実行時に、クライアント フレームワークは指定されたテンプレート ID と一致する ID を持つ HTML 要素のリソース バンドルを検索します。 実行時に、クライアント フレームワークはテンプレート ID で指定された JavaScript クラスをインスタンス化します。 このパスは Web ディレクトリのルートからの相対パスです。
-   **ビルド クラス名**: ビルド クラスの名前を指定する文字列。 ビルド クラス名は、デザイン時の動作を決定する X++ クラスです。 デザイン時に、Visual Studio のフレームワークはこの属性を反映し、デザイナー クラスとして指定された X++ クラスを読み込みます。 実行時に、X++ フレームワークは指定した X++ クラスを applyBuild() の super のビルド クラスとしてインスタンス化します。

次の例は、"MyControl" という名前のコントロールの標準的なクラスと属性の宣言を示しています。

```xpp
[FormControlAttribute('MyControl', '/resources/html/MyControl', classStr(MyControlBuild))]
class MyControl extends FormTemplateControl
```

## <a name="runtime-formcommandattribute"></a>ランタイム: FormCommandAttribute
**FormCommandAttribute** は、コントロール クラスのメソッドに適用されるため、メソッドをコントロールの JavaScript クラスから呼び出すことができます。 この属性を適用したメソッドは **コマンド** と呼ばれます。 **FormCommandAttribute** は、コントロールの JavaScript クラスから直接アクセスする必要がある X++ メソッドのみで使用します。 のみ使用します。 コマンドとしての役割を果たす X++ メソッドは、文字列の引数のみ受け入れることができます。 このメソッドは、文字列引数を他の型にシリアル化または逆シリアル化するために必要な操作を実行する必要があります。 **FormCommandAttribute** は、X++ 内からメソッドが使用される場合、X++ メソッドの動作に影響を与えません。 **FormCommandAttribute** は、JavaScript からアクセス可能な外のエンドポイントとして X++ メソッドを公開します。 したがって、すべてのコマンドは脅威モデル化およびエクスプロイトのためにテストされる必要があります。また、そのすべての引数について検証を実行する必要があります。 基礎となる X++ メソッドは、X++ からアクセスできないようにプライベート宣言する必要があります。 X++ コードがこのメソッドの動作にアクセスする必要がある場合は、個別の X++ メソッドは **FormCommandAttribute** なしで public として宣言する必要があります。 このパブリック メソッドには、X++と JavaScript の両方で必要な共有コードが含まれている必要があります。 **FormCommandAttribute** を使用した private X++ メソッドは、このパブリック メソッドを呼び出して、共有コードにアクセスできます。 この方法では、コア共有 X++ ロジックを実行する前に、JavaScript (引数の型の逆シリアル化、引数の検証、セキュリティの検証など) からの呼び出しに特定なロジックをコマンドで実行できます。 次の引数を **FormCommandAttribute** コンストラクターに指定します。

-   **名前**: コマンドの名前を指定する必要な文字列。 プロパティの名前を付けるためのいくつかのベスト プラクティス。
    -   最初の文字を大文字にし、PascalCase を使用します。
    -   名前に動詞を使用します。
    -   コマンドが FormProperty の読み取り/書き込みに使用される場合、プロパティ名を含めます (例: Set\_&lt;PropertyName&gt;)
    -   継承済 JavaScript プロパティの名前を使用しないでください。
-   **即時実行**: このコマンドへの呼び出しを延期するか、即時実行を必要とするかを指定するオプションのブール値。 既定では、コマンドは **即時実行** を **true、** に設定しているため、呼び出しは延期されません。 ユーザーが次のアクションを完了できるようになる前に X++ ロジックを実行する必要があるため、ほとんどのコマンドは即時実行が必要になります。 ただし、次のアクションを実行するユーザー機能に副作用のないコマンドは、パフォーマンス上のメリットを得るために安全に据え置かれる可能性があります。 延期されるコマンドについては、ネットワークおしゃべりを減らすため、即時実行を **false** に設定します。

次の例では、"SetText" という名前のコマンドを宣言しています。

```xpp
[FormCommandAttribute("SetText")]
private void setText(str value)
{
    // Add implementation code here.
}
```

## <a name="runtime-formpropertyattribute"></a>ランタイム: FormPropertyAttribute
**FormPropertyAttribute** は、コントロール クラスのメソッドに適用されるため、X++ メソッドをコントロールの JavaScript クラスから **FormProperty** ゲッター/セッターとして呼び出すことができます。 この属性を適用したメソッドは **プロパティ** と呼ばれます。 コントロールの JavaScript クラスから直接アクセスする必要がある X++ メソッドの **FormPropertyAttribute** のみ使用します。 **FormPropertyAttribute** は、X++ 内からメソッドが使用される場合、X++ メソッドの動作に影響を与えません。 すべてのプロパティは、ブラウザーにエンドポイントを公開します。 したがって、すべてのプロパティは脅威モデル化およびエクスプロイトのためにテストされる必要があります。 基礎となる X++ メソッドは、他の X++ コードからアクセスできないようにプライベート宣言する必要があります。 別の X++ コードがプロパティにアクセスする必要がある場合、別のパブリック X++ メソッドを **FormPropertyAttibute** なしで宣言し、このメソッドに共有プロパティ ロジックを移動します。 次に、このメソッドを **FormPropertyAttribute を持つプライベート X++ メソッドから呼び出します。この方法により、コア共有 X++ ロジックを実行する前に、JavaScript からの呼び出しに固有のロジック (引数の型の逆シリアル化、引数の検証、セキュリティの検証など) をプロパティで実行できます。** 基本となる X++ メソッドは、必要なタイプのプロパティを受け入れて返す必要があります。 目的の型が EDT である場合は、プロパティは、EDT の基本データ型を受け入れ、返す必要があります。 サポートされているプロパティの種類は次のとおりです。

-   [X++ プリミティブ型](https://msdn.microsoft.com/library/aa602290.aspx)
-   [X++ データ契約](https://msdn.microsoft.com/library/system.runtime.serialization.datacontractattribute(v=vs.110).aspx) (そのメンバーもサポートされているタイプ)
-   [X++ リスト](https://msdn.microsoft.com/library/list.aspx) (その項目もサポートされているタイプ)

次の引数を **FormPropertyAttribute** コンストラクターに指定します。

-   **FormPropertyKind:** プロパティの種類を示す必須の **FormProperyKind** の値。 データ ソース フィールドにバインドされないプロパティには **FormPropertyKind::Value** を使用し、データ ソース フィールドにバインドされるプロパティには **FormPropertyKind::BindableValue** を使用します。
-   **名前:** プロパティの名前を指定する必要な文字列。 プロパティの名前を付けるためのいくつかのベスト プラクティス。
    -   最初の文字を大文字にし、PascalCase を使用します。
    -   継承済 JavaScript プロパティの名前を使用しない
-   **読み取り専用**: このプロパティをコントロールの JavaScript クラスから書き込み可能にするかどうかを指定するオプションのブール値。 既定のプロパティでは **読み取り専用** が **false、** に設定されているため、書き込み可能です。 この引数は、X++ からこのプロパティに書き込む機能には影響しません。 X++ メソッドを読み取り専用にするには、メソッド宣言からすべてのメソッド引数を削除します。 プロパティの大部分は、コントロールの JavaScript クラスから書き込みできません。 ほとんどのプロパティ値は検証を必要とするため、プロパティのセッターとしてコマンドを使用してバッキング プロパティが設定される前に検証ロジックを実行できるようにする必要があります。
-   **即時実行**: このプロパティへの書き込みを延期するか、即時実行がひつようであるかを指定するオプションのブール値。 既定のプロパティでは **即時実行** が **false、** に設定されているため、書き込みは延期されます。 大多数のプロパティはコントロールの JavaScript クラスに書き込み可能なフォームであってはならないため、**即時実行** フラグの既定値は **false** で、パフォーマンス上の利益を提供します。 コントロールの JavaScript クラスから書き込み可能なプロパティの場合でも、動作を有効にする前に、即時実行のパフォーマンスの副作用を慎重に検討する必要があります。

次の例は、一般的なプロパティ宣言を示しています。 ほとんどのプロパティは、以下のように取得/設定に同じ定型コードを共有します。 textProperty 変数は、このプロパティの FormProperty の後ろにあるフィールドです。

```xpp
[FormPropertyAttribute(FormPropertyKind::Value, "Text", true)
private str parmText(str _value = textProperty.parmValue())
{
    if(!prmIsDefault(_value))
    {
        textProperty.setValueOrBinding(_value);
    }
    return textProperty.parmValue();
}
```

## <a name="runtime-formproperty"></a>ランタイム: FormProperty
##### <a name="behavior"></a>動作

**FormProperty** は X++ と JavaScript の間のプロパティの値の同期のために管理フレームワークによって使用される X++ [派生型](https://msdn.microsoft.com/library/esd9wew8(v=vs.100).aspx) です。 **FormProperty** オブジェクトはプロパティによって内部で使用されるバックアップ フィールドと見なされます。 各 **FormProperty** は、コントロールの X++ ランタイム クラスの 4 つの場所で通常使用されます。

1.  **FormProperty** は通常クラス宣言のすぐ下で宣言されます。
2.  **FormProperty** は、クラスの **new** メソッドでインスタンス化されます
3.  **FormProperty** は、クラスの **applyBuild** メソッドで初期化されます
4.  **FormProperty** は、プロパティの X++ メソッドで読み書きされます

次の例は、典型的なコントロールの X++ ランタイム クラスで使用されている **FormProperty** を示しています。

```xpp
[FormControlAttribute("MyControl", "/resources/html/MyControl", classStr(BuildMyControl))]
class MyControl extends FormTemplateControl
{             
    FormProperty textProperty;          

    public void new(FormBuildControl _build, FormRun _formRun)
    {
        super(_build, _formRun);
        
        this.setTemplateId("MyControl");
        this.setResourceBundleName("/resources/html/MyControl");
        textProperty = this.addProperty(
        methodStr(MyControl, parmText), Types::String);
    }

    public void applyBuild()
    {
        BuildMyControl build;
        
        super();

        build = this.build();
        if(build)
        {
            this.parmText(build.Text());
        }
    }

    [FormPropertyAttribute(FormPropertyKind::Value, "Text", true)
    private str parmText(str _value = textProperty.parmValue())
    {
        if(!prmIsDefault(_value))
        {
            textProperty.setValueOrBinding(_value);
        }
        return textProperty.parmValue();
    }
}
```

## <a name="runtime-new-method"></a>ランタイム: 新しいメソッド
コントロールの X++ ランタイム クラスの **new** メソッドは、フォームのコントロールのインスタンス化の一部として呼び出されます。 **新規** メソッドがフォーム ライフ サイクルで呼び出される際の詳細については、「コントロール ライフサイクルの図」を参照してください。 ここのメソッドは、コントロールの FormProperties をインスタンス化し、コントロールのテンプレート ID とリソース バンドル パスを設定するために使用されます。 FormProperty の例で **new** メソッドの一般的な使用方法を参照してください。

## <a name="runtime-applybuild-method"></a>ランタイム: applyBuild メソッド
コントロールの X++ ランタイム クラスの **applyBuild** メソッドは、フォームのコントロールのインスタンス化の一部として呼び出されます。 **applyBuild** メソッドがフォーム ライフ サイクルで呼び出される際の詳細については、「コントロール ライフサイクルの図」を参照してください。 このメソッドは、コントロールの FormProperties を既定値、またはコントロールをフォームに配置したフォーム開発者が指定した値に初期化するために使用されます。 FormProperty の例で **applyBuild** メソッドの一般的な使用方法を参照してください。

## <a name="runtime-formbindingutilinitbinding-method"></a>ランタイム: FormBindingUtil::initbinding メソッド
**FormBindingUtil** は、コントロール フレームワークで提供される API です。 データ ソースで FormProperties をデータ フィールドおよびデータ メソッドにバインドするために使用されます。 次の例では、DataSource1 という名前のデータ ソース上の "Value" という名前のデータ フィールドを、ランタイムクラスの textProperty FormProperty にバインドします。

```xpp
[FormControlAttribute("MyControl", "/resources/html/MyControl", classStr(BuildMyControl))]
class MyControl extends FormTemplateControl
{
    FormProperty textProperty;

    public void new(FormBuildControl _build, FormRun _formRun)
    {
        super(_build, _formRun);
        this.setTemplateId("MyControl");
        this.setResourceBundleName("/resources/html/MyControl");
        textProperty = this.addProperty(
        methodStr(MyControl, parmText), Types::String);
    }

    public void applyBuild()
    {
        BuildMyControl build;
            
        super();
           
        build = this.build();
        if(build)
        {
            this.parmText(FormBindingUtil::initBinding(
            "DataSource1", "Value", this.formRun()));
        }
    }

    [FormPropertyAttribute(FormPropertyKind::Value, "Text", true)
    private str parmText(str _value = textProperty.parmValue())
    {
        if(!prmIsDefault(_value))
        {
            textProperty.setValueOrBinding(_value);
        }
        return textProperty.parmValue();
    }
}
```

## <a name="design-time-the-x-build-class"></a>デザイン時間: X++ ビルド クラス
ビルド クラスは、コントロールのデザイン時の動作を定義します。 このクラスは、プロパティ シートに表示されるプロパティと、フォーム デザイナーでモデル化されたときのコントロールの動作を決定します。 デザイン時クラスの仕事は、後でアクセスするために実行時クラスの設計時間情報を取り込むことです。

## <a name="design-time-class-declaration--formdesigncontrolattribute"></a>デザイン時間: クラス宣言 & FormDesignControlAttribute
FormDesignControlAttribute は、フォームのデザイン ノードを右クリックしたときに、コントロールが Visual Studio フォーム デザイナーに表示されるために必要です。 FromDesignControlAttribute が欠落している場合は、コントロールは、必須の X++ コードを介してのみフォームに追加することができます (例えば、フォームの addControlEx メソッドを介して)。

```xpp
[FormDesignControlAttribute("MyControl")]
class MyControlBuild extends FormBuildControl
{

}
```

## <a name="design-time-formdesignpropertyattribute"></a>デザイン時間: FormDesignPropertyAttribute
デザイン時間クラスのメソッドにこの属性を配置すると、最初の引数により (および 2 番目の引数により指定されたセクションで) 指定された新しいプロパティが、プロパティの取得/設定メソッドとして動作する対応する X++ メソッドと共にこのコントロールのプロパティ シートに表示されます。

```xpp
[FormDesignControlAttribute("MyControl")]
class MyControlBuild extends FormBuildControl
{
    str text; 

    [FormDesignPropertyAttribute("Text", "Data")]
    public str Text(str _value = text)
    {
        if(!prmIsDefault(_value))
        {
            text = _value;
        }
        return text;
    }
}
```

## <a name="design-time-formdesignproperty-attribute"></a>デザイン時間: FormDesignProperty** **属性
プロパティ シート内の特殊な動作のために、標準の FormDesignPropertyAttribute と一緒に適用できるいくつかの FormDesignProperty 属性があります。 特殊なビヘイビアーには、プロパティを値のリストから選択できるコンボ ボックスとして有効にすることが含まれます。 使用されたさまざまな種類のリストが以下に列挙されています。 ユーザーがコンボ ボックスから項目を選択するたびに、その項目の文字列名が、その属性を使用して X++ メソッドのゲッター/セッターに渡されます。

-   \[FormDesignPropertyDataSourceAttribute\] - フォームのデータ ソースのリストを表示します。
-   \[FormDesignPropertyDataFieldAttribute (&lt;データ ソース名&gt;)\] - 指定されたデータ ソースのデータ フィールドのリストを表示します。
-   \[FormDesignPropertyDataMethodAttribute(&lt;データ ソース名&gt;)\] - 指定されたデータ ソースのデータ メソッドのリストを表示します。
-   \[FormDesignPropertyFieldGroupAttribute(&lt;データ ソース名&gt;)\] - 指定されたデータ ソースのフィールド グループのリストを表示します。
-   \[FormDesignPropertyExtendsClassAttribute (&lt;クラス名&gt;)\] - 指定されたクラスを拡張するクラスのリストを表示します。
-   \[FormDesignPropertyImplementsAttribute (&lt;インターフェイス名&gt;)\] - 指定されたインターフェイスを実装するクラスのリストを表示します。
-   \[FormDesignPropertyReferenceAttribute(&lt;FormDesignPropertyReferenceType::&lt;type&gt;\]) - これは、特定のタイプで指定された AOT コンポーネントのリストを表示します。 サポートされている種類は次のとおりです。
    -   テーブル
    -   表示
    -   マップ
    -   EDT
    -   BaseEnum
    -   クエリ
    -   クラス
    -   フォーム
    -   MenuItemDisplay
    -   MenuItemOuput
    -   MenuItemAction
    -   タイル
    -   KPI

次の例は、フォーム開発者がデザイン タイム クラスのデータ ソースとデータ フィールドを指定できるようにするために使用される標準プロパティを示しています。

```xpp
[FormDesignControlAttribute("MyControl")]
class MyControlBuild extends FormBuildControl
{
    str dataSource; 
    str dataField;
    str dataMethod;

    [FormDesignPropertyAttribute("Data source", "Data"),
     FormDesignPropertyDataSourceAttribute]
    public str DataSource(str _value = dataSource)
    {
        if(!prmIsDefault(_value))
        {
            dataSource = _value;
        }
        return dataSource;
    }

    [FormDesignPropertyAttribute("Data Field", "Data"),
     FormDesignPropertyDataFieldAttribute(methodStr(MyControlBuild, DataSource))]
    public str DataField(str _value = dataField)
    {
        if(!prmIsDefault(dataField))
        {
            dataField = _value;
        }
        return dataField;
    }

    [FormDesignPropertyAttribute("Data Method", "Data"),
     FormDesignPropertyDataMethodAttribute(methodStr(MyControlBuild, DataSource))]
    public str DataMethod(str _value = dataMethod)
    {
        if(!prmIsDefault(dataMethod))
        {
            dataMethod = _value;
        }
        return dataMethod;
    }
}
```

上記のようなデザイン時クラスを持つコントロールは、以下に示すように、指定されたデータ ソースと applyBuild メソッド内のデータ フィールドにバインドできます。

```xpp
public void applyBuild()
{
    BuildMyControl build;

    super();

    build = this.build();
    if(build)
    {
        this.parmText(FormBindingUtil::initBinding(
        build.DataSource(), build.DataField(), this.formRun(), build.DataMethod()));
    }
}
```

データ フィールドとデータ メソッドの両方を FormBindingUtil::initBinding に渡すと、データ フィールド バインディングはデータ メソッド バインディングを上書きします。

## <a name="html"></a>HTML
## <a name="html-framework-attributes"></a>HTML: フレームワーク属性

次のセクションでは、コントロール開発のコントロール フレームワークで使用される HTML 属性について説明します。

### <a name="data-dyn-bind"></a>data-dyn-bind

**data-dyn-bind**、データ バインディング属性は - 宣言 HTML-based API を使用して、要素の属性、プロパティおよび CSS、または DOM イベントの処理などの変更のような、多くの一般的な DOM 操作を標準化しています。 データ バインディング属性は、複雑な JavaScript を必要とせずにこれらの動作を可能にします。 複雑な JavaScript を記述するのではなく、データ バインド属性を使用することで、コントロールの設計、デバッグ、および維持をより簡単にすることによって、コントロールの開発者の貴重な時間を節約することができます。 ただし、シナリオが必要とする場合、複合 JavaScript が引き続き使用可能です。 データ バインディング属性は、HTML 要素の動作をコントロール開発者が提供する値に結合します。 指定された値は、単純な JavaScript [変数](https://www.w3schools.com/js/js_variables.asp)、JavaScript [比較](https://www.w3schools.com/js/js_comparisons.asp)、[算術](https://www.w3schools.com/js/js_arithmetic.asp)式、JavaScript [関数](https://www.w3schools.com/js/js_functions.asp)、JSON [オブジェクト](https://www.w3schools.com/js/js_json_objects.asp)のいずれかになります。 提供される値は、このドキュメントで説明されている API を使用して作成された、観察可能な変数でもあります。 指定された値が HTML 要素にバインドされる方法は、データ バインディング属性で使用されるバインディング ハンドラーによって決まります。 このドキュメントでは、サポートされているすべてのバインディング ハンドラーの一覧を提供します。 バインディング ハンドラーで使用する場合、データ バインディング属性には次の構文が必要です。 **data-dyn-bind** の構文は次のとおりです。

```xpp
data-dyn-bind="[first binding handler]: [value to bind to]"
```

データ バインディング属性はバインディング ハンドラーと値のペアのコンマ区切りリストを受け入れます。したがって、一度に複数のバインディング ハンドラーをバインディング属性に指定できます。 次の例では、div 要素の **visible** プロパティを true にバインドし、div 要素の **textContent** プロパティを "Hi" にバインドします。

```xpp
data-dyn-bind="text: 'Hi', visible: true"
```

データ バインディング属性は、コントロール フレームワークによって認識されるカスタム HTML 属性です。 データ バインディング属性は、任意の HTML 要素に適用できます。 一部の HTML 要素には、バンディング ハンドラーが変更する動作がない可能性があります。 たとえば、**&lt;svg&gt;** 要素でのテキスト バインディング ハンドラーの使用は、**&lt;svg&gt;** 要素に textContent プロパティがないため、テキストを表示しません。 コントロール フレームワークは、実行時にコントロールのテンプレートで指定されたデータ バインディングを読み取り、実行します。 ブラウザーでのコントロールのライフサイクルは、次のように要約できます。

1.  コントロールの HTM ファイルは、ブラウザーによって読み込まれます。
2.  HTM ファイルで参照されているスクリプトまたはリソース ファイルも、ブラウザーによって読み込まれます。 手順 1 と 2 は、コントロールの複数のインスタンスがある場合でも、ユーザーのセッション中に 1 回だけ実行されます。
3.  コントロールの JavaScript クラスのコンストラクターは、呼び出しであり、コントロール インスタンスの X++ プロパティを使用して渡されます。
4.  コントロールのテンプレートは、HTM ファイルからブラウザーのメモリにコピーされます。
5.  コントロールのテンプレートでの HTML 要素は階層順に (深さ優先) データ バインディング用に処理され、各要素のデータ バインディングは左から右の順に実行されます。
6.  元のデータ バインディング属性や、バインディング ハンドラーやフレームワークによって追加されたその他のマークアップを含む最終的な HTML は、ブラウザーの DOM に追加され、ユーザーに表示されるようにレンダリングされます。
7.  後で、観測可能なオブジェクトの値が変更されると、オブザーバブルに対してサブスクライブされたバインディング ハンドラーが再実行され、稼働している DOM がリアルタイムで更新されます。

## <a name="html-binding-handlers"></a>HTML: バインディング ハンドラー
### <a name="attr"></a>attr

**attr** バンディング ハンドラーは、指定された HTML 属性と値を要素に適用します。 HTML 属性の一覧については、[W3 学校 – HTML 属性](https://www.w3schools.com/html/html_attributes.asp) を参照してください。 引数は、オブジェクト配列として渡されます。 各引数は、デュアル値です。 最初の値は属性の名前で、2 番目の値は属性の値です。

-   **名前**: 作成する属性の任意の名前を指定する文字列。
-   **値または式:** 属性に設定する値を指定する文字列。 式が指定されている場合は、式を評価することによって返される値が使用されます。

次の例では、title 属性と name 属性を作成し、その値を設定します。

```xpp
<!-- the markup in the HTML template -->
<div data-dyn-bind="attr: {title: 'Hello', name: 'Greeting'}"></div>

<!-- the markup in the browser after the binding handler is applied -->
<div title="Hello" data-dyn-bind="attr: {title: 'Hello', name: 'Greeting'}" name="Greeting"></div>
```

次の例では、式と関数を使用します。 ただし、下の例のようにインライン HTML として JavaScript 関数を使用することはお勧めできません。

```xpp
<!-- the markup in the HTML template -->
<div data-dyn-bind="attr: {title: false? 'Hello':'World', name: function(){return 'Greetings';}()}"></div>

<!-- the markup in the browser after the binding handler is applied -->
<div title="World" data-dyn-bind="attr: {title: false? 'Hello':'World', name: function(){return 'Greetings';}()}" name="Greetings"></div>
```

#### <a name="click"></a>click

##### <a name="behavior"></a>動作

要素のクリック イベントに指定された関数をサブスクライブします。 クリック イベントのサブスクライブの詳細については、[jQuery – click()](https://api.jquery.com/click/) を参照してください。

##### <a name="arguments"></a>引数

###### <a name="eventhandler-function"></a>EventHandler (関数)

イベントが発生したときに呼び出す関数。

##### <a name="example-1"></a>例 1

次の例は、要素がクリックされたときの警告メッセージ「Hello」を示しています。

```xpp
// In your control’s code-behind JS file
<script>
... // boilerplate code
self.ElementClicked = function (event) {
    /* handle the click event */
    alert('Hello');
};
...
</script>

<!-- In your control’s template HTM file -->
<div data-dyn-bind="click: $control.ElementClicked"></div>
```

次の例では、子要素のクリック イベントが親要素までバブル アップできなくなります。 次の例では、子要素をクリックするとメッセージ「こんにちは」を含む警告が 1 つだけ表示されます。

```xpp
// In your control’s code-behind JS file
<script>
... // boilerplate code
self.ParentElementClicked = function (event) {
    /* handle the click event */
    alert('Hi');
};

self.ElementClicked = function (event) {
    /* prevents the event form bubbling up to parent elements*/
    event.stopPropagation();

    /* handle the click event */
    alert('Hello');
};

...
</script>

<!-- In your control’s template HTM file -->
<div data-dyn-bind="click: $control.ParentElementClicked">
<div data-dyn-bind="click: $control.ElementClicked"></div>
</div>
```

次の例では、ブラウザの既定の動作が実行できなくなります。 アンカー タグについては、既定のハイパーリンク動作が防止されるため、要素のクリック時にブラウザーがリンクに移動しません。

```xpp
// In your control’s code-behind JS file
<script>
... // boilerplate code
self.LinkClicked = function (event) {
        /* handle the click event */
        alert($dyn.format('Navigation to ' + {0} + ' was prevented', $(event.target).attr("href")));

        /* prevents the default event behavior */
        event.preventDefault();
};
</script>

<!-- In your control’s template HTM file -->
<a href="https://www.microsoft.com" data-dyn-bind="click: $control.LinkClicked">Click here</a>
```

#### <a name="css"></a>css

##### <a name="behavior"></a>動作

指定された条件に基づいて、指定された CSS クラス名を追加または削除します。 バインディング ハンドラーに指定された式は 1 回だけ実行されることに注意してください。

##### <a name="arguments"></a>引数

引数は、オブジェクト配列として渡されます。 各引数は、デュアル値です。 最初の値はクラス名で、2 番目の値は条件です。

###### <a name="class-name-string"></a>クラス名 (文字列)

要素に追加する CSS クラス名。

###### <a name="condition-expression"></a>条件 (式)

CSS クラス名を追加する条件。 条件が true の場合は、CSS のクラス名は追加されます。 条件が false の場合は、CSS のクラス名は削除されます。 指定した条件が監視可能な値 ($ dyn.value 経由) に依存する場合、監視可能な値が変わるたびに条件が再評価され、関連する CSS クラス名が新しい条件に基づいて追加/削除されます。 次の例では、CSS クラス名 「red」、「green」、および「yellow」を追加します。

```xpp
// In your control’s code-behind JS file
<script>
... // boilerplate code
self.red = function () { return true; };
self.yellow = $dyn.observable(true);
...
</script>

<!-- the markup in the HTML template -->
<div data-dyn-bind="css: {green: true, red: $control.red, yellow: $dyn.value($control.yellow)}"></div>

<!-- the markup in the browser after the binding handler is applied -->
<div class="green red yellow" data-dyn-bind="css: {green: true, red: $data.red, yellow: $dyn.value($control.yellow) }"></div>
```

#### <a name="event"></a>イベント

##### <a name="behavior"></a>動作

指定した DOM イベントに指定されたイベントをサブスクライブします。 サポートされている DOM イベントの一覧については、[jQuery - イベント](https://api.jquery.com/Types/#Event) を参照してください。

##### <a name="arguments"></a>引数

イベント バインディング ハンドラーへの引数の詳細については、[jQuery - .bind()](https://api.jquery.com/bind/) を参照してください。 次の例では、mouseover イベントにサブスクライブし、要素がポイントされたときにアラートを表示します。

```xpp
// In your control’s code-behind JS file
<script>
... // boilerplate code
self.elementHovered = function (event) { alert($dyn.format('{0}',$(event.target).text()))};
...
</script>

<!-- the markup in the HTML template -->
<div data-dyn-bind="event: {mouseover: $data.elementHovered}">Greetings!</div>
```

#### <a name="foreach"></a>foreach

##### <a name="behavior"></a>動作

渡されたデータに基づいて各子のバインド コンテキストを更新して、子要素の内容を繰り返します。 _ *foreach** バインディングを持つ要素内の子要素_ を ***1 つだけ** 指定します。 この 1 つの要素は、複製され、繰り返される要素です。 バインディングが適用される場合に、その他の追加要素またはコンテンツは削除されます。 要素に表示される順序でバインディング ハンドラーが実行されます。 **foreach** バンディングによりバインディング コンテキストが変わるため、必ず **foreach** バインディングは要素の他のすべてのバインディングより後に配置することをお勧めします。 これにより、先行するバインドは、**foreach** バインドによって作成されたバインド コンテキストの影響を受けないことが保証されます。 パフォーマンスの問題を避けるために、**foreach** 内の observable に意図しない依存関係を生成しないように注意してください。 **foreach** バインドが配列内の監視可能にすでにサブスクライブされている際は、**foreach** の子要素の中から **$dyn.value** を使って配列内の監視可能にアクセスしないでください。 代わりに、**$dyn.peek** を使用してサブスクリプションを作成せずにオブザーバブルの値に一度アクセスします。

##### <a name="arguments"></a>引数

###### <a name="data-array-list-or-json-object"></a>データ (配列リストまたは JSON オブジェクト)

子要素をバインドする項目のリスト。 配列リストを指定する場合は、配列内の品目はバインド コンテキストです。 JSON オブジェクト配列が指定されている場合、拘束力のあるコンテキストは、オブジェクトのプロパティのいずれかになります。

##### <a name="scope-variables"></a>スコープ変数

**foreach** のスコープの範囲内では、次のスコープ変数が有用であり、反復可能な子要素である $data、インデックス、コントロール、ユーザー独自のスコープ変数で使用できます。 次の例では、**foreach** を使用して配列の各色の期間要素を表示します。

```xpp
// In your control’s code-behind JS file
<script>
... // boilerplate code
self.colors = ['Red','Blue','Green'];
...
</script>

<!-- the markup in the HTML template -->
<div data-dyn-bind="foreach: $control.Colors">
<span data-dyn-bind="text: $data"></span>
</div>

<!-- the markup in the browser after the binding handler is applied -->
<div data-dyn-bind="foreach: $control.colors">
<span data-dyn-bind="text: $data">Red</span>
<span data-dyn-bind="text: $data">Blue</span>
<span data-dyn-bind="text: $data">Green</span>
</div>
```

次の例では、入れ子になった **foreach** バインディングを示しています。 この例では、インデックス フレームワーク スコープ変数とカスタム スコープ変数を使用して、親要素からバインド コンテキストにアクセスする方法を示します。

```xpp
    // In your control’s code-behind JS file
<script>
... // boilerplate code
self.colors = [
    {
        Name: 'Red',
        Variants: ['Maroon','Burgundy','Sunrise']
    },
    {
        Name: 'Green',
        Variants: ['Sage','Forest','Lime']
    },
    {
        Name: 'Blue',
        Variants: ['Navy','Sky','Ice']
    }
];
...
</script>
<!-- the markup in the HTML template -->
<div data-dyn-bind="foreach: $control.colors">
<div data-dyn-bind="vars: {$BaseIndex: $index, $BaseColor: $data.Name}">
<div data-dyn-bind="foreach: $data.Variants">
<div data-dyn-bind="text: $BaseIndex+'.'+$index+' '+$data+' '+$BaseColor"></div>
</div>
</div>
</div>
<!-- the markup in the browser after the binding handler is applied -->
<div data-dyn-bind="foreach...">
<div data-dyn-bind="vars...">
<div data-dyn-bind="foreach...">
<div data-dyn-bind="vars...foreach...">
<div data-dyn-bind="text...">1.1 (0.2552) X++ Language</div>
<div data-dyn-bind="text...">1.2 (0.7) Applications</div>
</div>
</div>
<div data-dyn-bind="vars...">
<div data-dyn-bind="text...">2. (600) Technology</div>
<div data-dyn-bind="vars... foreach...">
<div data-dyn-bind="text...">2.1 (600.343) Microsoft Corporation</div>
<div data-dyn-bind="text...">2.2 (600.117) Enterprise Resource Planning</div>
</div>
</div>
</div>
```

#### <a name="if"></a>if

##### <a name="behavior"></a>動作

このバインドで要素の子要素を条件付きでレンダリングおよびバインドします。 このバインディング ハンドラーは、子要素に対してのみ有効です。 バインディングのある要素を表示/非表示せず、このバインディングもバインディングのある要素のテキスト内容を表示/非表示しません。 子要素のバインディングは条件が true と評価される場合にのみ実行されます。 子要素のバインディングが一度評価されると、条件が false に変更されてもデータ バインドされたままになります。 これは、子要素へのバインディングによって引き起こされる計算は、子要素が非表示になった後でも引き続き動作することを意味します。 コントロールのパフォーマンスを評価する際にこれを考慮してください。

##### <a name="arguments"></a>引数

###### <a name="condition-expression"></a>条件 (式)

子要素を表示するかどうかを決定します。 次の例では、**show** および **text** 要素を条件付きでバインドしています。

```xpp
    // In your control’s code-behind JS file
<script>
... // boilerplate code
self.show = $dyn.observable(false);
self.text = "Hello";
...
</script>
<!-- the markup in the HTML template -->
<div data-dyn-bind="if: $control.show">
<div data-dyn-bind="text: $control.text"></div>
</div>
<!-- the markup in the browser after the binding handler is applied -->
<div data-dyn-bind="if: $control.show">
</div>
// Later on, the value of the “show” observable changes to true
<script>
...
self.show(true);
...
</script>
<!-- the markup in the browser after the binding handler is re-applied due to the observable value changing -->
<div data-dyn-bind="if: $control.show">
<div data-dyn-bind="text: $control.text">Hello</div>
</div>
```

#### <a name="sizing"></a>sizing

##### <a name="behavior"></a>動作

コントロールの高さと幅を指定します。 サイズ変更バインド ハンドラーは、常にテンプレートのルート要素 (id 属性を持つ要素) に適用し、$dyn.layout.sizing ヘルパー関数を使用してコントロールの X++ インスタンスから height 値と width 値を指定する必要があります。 例 1 を参照してください。

##### <a name="arguments"></a>引数

引数には、高さと幅のプロパティを含むオブジェクトが渡されます。

###### <a name="height-int"></a>高さ (int)

バインディング ハンドラーが適用される要素の高さをピクセル単位で指定します。

###### <a name="width-int"></a>幅 (整数)

バインディング ハンドラーが適用される要素の幅をピクセル単位で指定します。 次の例では、**MyControl** のサイズを指定しています。

```xpp
<!-- the markup in the HTML template -->
<!-- this boilerplate binding ensures that the control’s container is sized based on the height and width properties -->
<div id="MyControl" data-dyn-bind="sizing: $dyn.layout.sizing($control)"></div>
<!-- the markup in browser after the binding handler is applied will vary based on the height and width properties defined in $control -->
```

次の例では、**bigbox** 変数の値に応じてコントロールを大きくまたは小さくします。

```xpp
// Later on, the value of the “show” observable changes to true
<script>
...
self.bigBox = true;
...
</script>
<!-- the markup in the HTML template -->
<div data-dyn-bind="sizing: {height: $control.bigBox?50:10, width: $control.bigBox?50:10}"></div>
<!-- the markup in the browser after the binding handler is applied -->
<div style="width: 50px; height: 50px;" data-dyn-bind="sizing: {height: $control.bigBox?50:10, width: $control.bigBox?50:10}"></div>
```

#### <a name="text"></a>テキスト

##### <a name="behavior"></a>動作

要素の textContent プロパティにバインドします。 テキスト バインド ハンドラーは、UI テキストで使用するためのものです。 要素に文字列ではない値 (数値、日付、またはブール値など) をバインドすることはありません。 dyn.format 関数を使用して、すべての値を文字列に変換してからバインディング ハンドラーに渡します。 テキスト バインド ハンドラーは、既存のコンテンツが HTML であるかシンプル テキストであるかにかかわらず、要素内のすべてのコンテンツをバインドで置き換えます。

##### <a name="arguments"></a>引数

###### <a name="text-string"></a>テキスト (文字列)

バインドするテキスト。 次の例では、div 要素の textContext プロパティをコントロールの text プロパティにバインドします。

```xpp
// In your control’s code-behind JS file
<script>
... // boilerplate code
self.text = "Hello";
...
</script>
<!-- the markup in the HTML template -->
<div data-dyn-bind="text: $dyn.format('{0}',$control.text)"></div>
<!-- the markup in browser after the binding handler is applied -->
<div data-dyn-bind="text: $dyn.format('{0}',$control.text)">Hello</div>
```

#### <a name="vars"></a>vars

##### <a name="behavior"></a>動作

指定された名前と値を持つ HTML スコープ変数を作成します。 作成されたスコープ変数は、テンプレート内のバインドからのみアクセスできます。 さらに、スコープ変数は子要素によって継承されます。 要素に表示される順序でバインディング ハンドラーが実行されます。 vars バンディングによりバインディング コンテキストに変数が追加されるため、必ず vars バインディングは要素の他のすべてのバインディングより前に配置することをお勧めします。 これにより、後続のバインドが vars バインドによって追加されたスコープ変数に確実にアクセスできるようになります。 以下の名前でスコープ変数を作成しないでください。$control、$data、$index、および $value は、フレームワーク スコープ変数に対して既に引当されています。

##### <a name="arguments"></a>引数

###### <a name="scope-variables-object-array"></a>スコープ変数 (オブジェクト配列)

スコープ変数名をキーとし、その値がスコープ変数の初期値であるオブジェクト配列。 次の例では、"Hello" および "World" という名前のスコープ変数を作成し、その値を表示します。

```xpp
<!-- the markup in the HTML template -->
<div data-dyn-bind="vars: {$myVar: 'Hello', $myObs: $dyn.observable('World')}">
<span data-dyn-bind="text: $dyn.format('{0} {1}!', $myVar, $myObs)">
</span>
</div>
<!-- the markup in browser after the binding handler is applied -->
<div data-dyn-bind="vars: {$myVar: 'Hello', $myObs: $dyn.observable('World')}">
<span data-dyn-bind="text: $dyn.format('{0} {1}!', $myVar, $myObs)">
Hello World!
</span>
</div>
```

##### <a name="example-2"></a>例 2

例については、foreach バインド ハンドラーの例を参照してください。

#### <a name="visible"></a>表示

##### <a name="behavior"></a>動作

要素の表示を設定します。 常にテンプレートのルート要素に表示されているバインディング ハンドラーを供給し、X++ コントロールの *表示* プロパティからバインドします。 これにより、コントロールがフォーム開発者によって設定されている場合、またはフレームワークによって設定されている場合に、コントロールが *Visible* プロパティを確実に使用するようになります。 *表示* X++ プロパティを false に設定してコントロールを初期化すると、フォームにコントロールが表示されず、コントロールのテンプレートがブラウザに読み込まれません。 コントロールの *Visible* X++ プロパティを後で true 設定する場合、コントロールのテンプレートが読み込まれ、その時点で、ブラウザーがインスタンス化されます。 コントロールの *Visible* X++ プロパティは、フォーム上の親コントロールから継承できます。 要素の可視性は表示されているバインディング ハンドラーが適用されるかどうかにかかわりなく、親要素、コントロールおよびコンテナーに制御されます。 カスケード表示の性質は標準的な HTML 動作であり、コントロール フレームワークに固有のものではありません。

##### <a name="arguments"></a>引数

###### <a name="visible-boolean"></a>Visible (ブール値)

要素が表示されるかどうかを決定します。 次の例では、コントロールの最も外側の div 要素の可視性を設定します。

```xpp
// In your control’s code-behind JS file
<script>
... // boilerplate code
self.Visible(false); // set the X++ observable property to false
...
</script>
<!-- the markup on the root element of the HTML template -->
<div id="MyControl" data-dyn-bind="visible: $control.Visible">Hello World!</div>
<!-- the markup in browser after the binding handler is applied -->
<div id="MyControl" style="display: none;" data-dyn-bind="visible: $control.Visible">Hello World!</div>
```

## <a name="html-scope-variables"></a>HTML: スコープ変数
値をバインディング ハンドラーにバインドする場合に、スコープ変数を使用できます。 スコープ変数には、コントロールの HTML テンプレート内からのみアクセスでき、データ バインディング属性でのみ使用できます。 スコープ変数は、他の HTML 属性からもコントロールの JavaScript クラスからもアクセスできませんが、スコープ変数は、バインディング ハンドラーに渡されたインライン JavaScript 式、関数、JSON オブジェクトで使用できます。

#### <a name="control"></a>$control

*$control* スコープ変数は、コントロールの JavaScript インスタンスのプロパティと関数にアクセスできる HTML テンプレートでバインドを提供します。 次の例では、div 要素の表示をコントロールの表示プロパティにバインドします。

```xpp
<div id="MyControl" data-dyn-bind="visible: $control.Visible"></div>
```

#### <a name="data"></a>$data

*$data* スコープ変数は、現在のバンディング コンテキストへのアクセスを持つ要素を提供します。 $data 内で定義される変数 (バインド コンテキスト) またはスコープ変数のみ HTML バインディング内で使用されます。 現在のバインディング コンテキストに存在せず、現在のスコープ変数として存在しない変数は、HTML バインディングからアクセスすることはできません。 ほとんどの場合、バインド コンテキストはコントロールの JavaScript インスタンスとなるので、*$data* および *$control* と同じになります。 ただし、場合によってはバインド コンテキストを変更できます。 たとえば、**foreach** バインディング内の要素に対して、*$data* は現在の配列品目へのアクセスによる要素を提供します。 複数の入れ子になった **foreach** バインドが関連する場合、入れ子になったバインドの要素は親の **foreach** バインドの配列品目へのアクセスを必要とする場合があります。 親の **foreach** バインドの項目にアクセスするには、入れ子になった **foreach** バインドの要素にアクセス可能なスコープ変数を作成できます。 例については、foreach バインド ハンドラーの例を参照してください。

#### <a name="index"></a>$index

$index スコープ変数は、**foreach** バインディングに含まれる場合、配列項目の 0 から始まるインデックスを提供します。 例については、foreach バインド ハンドラーの例を参照してください。

## <a name="javascript-inherited-properties"></a>JavaScript: 継承されたプロパティ
#### <a name="visible"></a>表示

**Visible** プロパティは、ベース JavaScript クラスから継承されます (**$dyn.ui.Controls.apply** 経由)。 ランタイムクラスが基本 **FormControl** X++ クラスから継承する X++ には、**Visible** プロパティもあります。 このプロパティを表示されたバインディング ハンドラーにそのままバインドし、コントロールの HTML テンプレートのルート要素に配置します。 このフレームワークは残りの部分を処理します。 次の例は、表示プロパティの使用方法を示しています。

```xpp
<!-- the markup in the HTML template -->
<div id="MyControl" data-dyn-bind="visible: $control.Visible"></div>
```

## <a name="observable-framework"></a>監視可能なフレームワーク
#### <a name="dynobserve"></a>$dyn.observe

##### <a name="usage"></a>用途

オブザーバブルの変更に関数をサブスクライブします。 廃棄を使用することをお勧めします。

```xpp
$dyn.observe(observable, observer, [context], [disposableObserver])
```

##### <a name="arguments"></a>引数

###### <a name="observable-observable"></a>オブザーバブル (オブザーバブル)

オブザーバブルのインスタンスです。 または、関数 ($dyn.computed になります)。

###### <a name="observer-function"></a>オブザーバー (関数)

登録時およびのちにオブザーバブルが更新される際にも、関数が呼び出されます。 関数は 1 つの引数、オブザーバブルの値で呼び出されます。 オブザーバーが false の場合、自動的に購読を解除します。

###### <a name="context-options-optional"></a>コンテキスト (選択可、オプション)

オブザーバーに渡すコンテキスト。 コンテキストは、オブザーバー内の **_this_* _ 変数になります。

###### <a name="disposableobserver-options-optional"></a>DisposableObserver (選択可、オプション)

付属の DisposableObserver の購読を取り消します

##### <a name="returns"></a>返品

###### <a name="subscription-object"></a>サブスクリプション (オブジェクト)

サブスクライブ解除に使用されたオブザーバブル、ID、Dispose 関数 (パブリック)。次の例は、myObs オブザーバブルをサブスクライブし、myObs オブザーバブルの値が変化すると必ず指定された関数を実行します。

```xpp
$dyn.observe(myObs, function (value) { console.log(value);});
```

次の例は、$dyn.value を使用してオブザーバブルの値にアクセスするだけで、関数がオブザーバブルの値に自動的にサブスクライブする方法を示しています。 最初の関数は、他の 2 つの監視可能な値 (FirstName と LastName) の値に依存する監視可能な値のように扱われます。 観測可能なオブジェクト (FirstName または LastName) のいずれかが値を変更するたびに、最初の関数の値も変更されます。 この場合、2 つ目の関数 (コールバック関数) は、観察可能な値の連結をコンソールに記録します。

```xpp
self.FirstName = $dyn.observable("Joanne");
self.LastName = $dyn.observable("Gordon");
$dyn.observe(
    function () {
        // Joann + " " + Gordon
        return $dyn.value(self.FirstName) + " " + $dyn.value(self.LastName);
    },
    function (value) {
        // "Joanne Gordon"
        console.log(value);
    }
);
```

次の例は、前の例と同様に実行されます。 ただし、この例では、連結を処理するために、myComp という名前の計算されたオブザーバブルを使用します。

```xpp
self.FirstName = $dyn.observable("Joanne");
self.LastName = $dyn.observable("Gordon");
self.myComp = $dyn.computed(function () {
    // Joanne + " " + Gordon
    return $dyn.value(self.FirstName) + " " + $dyn.value(self.LastName);
});
$dyn.observe(
    self.myComp,
    function (value) {
        // "Joanne Gordon"
        console.log(value)
    );
},
{FirstNameLabel: label1, LastNameLabel: label2}
);
```

#### <a name="dynobservable"></a>$dyn.observable

##### <a name="usage"></a>用途

監視可能な変数を作成します。

```xpp
$dyn.observable([initial value])
```

##### <a name="arguments"></a>引数

###### <a name="initial-value-optional"></a>初期値 (オプション)

観測値を初期化する値。

##### <a name="returns"></a>返品

###### <a name="observable-function"></a>オブザーバブル (関数)

新しく作成された observable。次の例では、「Hello」という名前の変数を作成し、それを監視します。

```xpp
var greeting = $dyn.observable("Hello");
```

#### <a name="dynvalue"></a>$dyn.value

##### <a name="usage"></a>用途

監視可能な変数の値にアクセス。 オブサーバー関数 (バインディング ハンドラーへ渡されるバインディング式だけでなく、**$dyn.observe** または **$dyn.computed** に渡されるオブザーバーなど) の内部から _ *$dyn.value** が呼び出されると、観測可能なオブジェクトへの依存関係が作成されます。 これにより、オブザーバブルの値が変更されるたびにバインディング ハンドラーまたはコールバックが再実行されます。 この依存関係は **$dyn.value** を使用すると自動的に作成されるため、このような依存関係を意図的に作成する場合は **$dyn.value** のみを使用することが重要です。 依存関係を作成せずに observable の値にアクセスするには、$dyn.peek を使用する必要があります。

```xpp
$dyn.value(observable)
```

##### <a name="arguments"></a>引数

###### <a name="observable"></a>オブザーバブル

値にアクセスできる監視可能なプロパティ。

##### <a name="returns"></a>返品

###### <a name="value"></a>先頭値

監視可能なプロパティの現在の値。次の例では、observable という名前の変数を返し、コンソールに出力します。

```xpp
console.log($dyn.value(observable));
```

#### <a name="dynpeek"></a>$dyn.peek

##### <a name="usage"></a>用途

依存関係の作成なしで、監視可能な変数の値にアクセス。 依存関係の詳細については、$dyn.value 機能を参照してください。

```xpp
$dyn.peek(observable)
```

##### <a name="arguments"></a>引数

###### <a name="observable"></a>オブザーバブル

値にアクセスできる observable。

##### <a name="returns"></a>返品

###### <a name="value"></a>先頭値

監視可能な値の現在の値。次の例では、observable という名前の変数を返し、コンソールに出力します。

```xpp
console.log($dyn.peek(observable));
```

#### <a name="dyncomputed"></a>$dyn.computed

##### <a name="usage"></a>用途

機能を監視範囲と共にラッピングします。 観測可能なオブジェクトを、**$dyn.value** 機能を使用して機能からアクセスする場合、その観測可能なオブジェクトの値が変更されるたびにこの機能を再度実行するようになります。 **$dyn.peek** を使用してアクセスされるオブザーバブルは、値が変わったときに関数を再実行しません。

```xpp
$dyn.computed(observer, [context], [disposableObserver])
```

##### <a name="arguments"></a>引数

###### <a name="observer-function"></a>オブザーバー (関数)

関数は登録時に呼び出され、および後に監視可能な値の変更のためにも呼び出されます。 オブザーバーは、関数の範囲内から $dyn.value を使用してアクセスされる任意の観測可能オブジェクトを自動的に監視します。

###### <a name="context-options-optional"></a>コンテキスト (選択可、オプション)

オブザーバーに渡すコンテキスト。 コンテキストは、オブザーバーの内部で *this* 変数になります。

###### <a name="disposableobserver-options-optional"></a>DisposableObserver (選択可、オプション)

付属の DisposableObserver の購読を取り消します

##### <a name="returns"></a>返品

###### <a name="anything-optional"></a>何でも (オプション)

オブザーバーが値を返すと、その値は、最初に **$dyn.computed** への呼び出しによって返されます。**$dyn.computed** は、オブザーバーが呼び出されるたびに (登録時に) 呼び出されます。

## <a name="framework-functions"></a>フレームワーク機能
#### <a name="dyncallfunction"></a>$dyn.callFunction

##### <a name="usage"></a>用途

指定された関数で適用メソッドを呼び出します。 インタラクション中は使用できません。

##### <a name="arguments"></a>引数

###### <a name="function-function-or-observable"></a>関数 (関数またはオブザーバブル)

呼び出す関数。 監視可能なオブジェクトが指定されている場合、監視可能なオブジェクトの現在の値が取得され、関数として使用されます。

###### <a name="this-object-optional"></a>この (オブジェクト、オプション)

関数のスコープ内で、*this* に割り当てるオブジェクト。

###### <a name="arguments-array-optional"></a>引数 (配列、省略可)

指定された関数に渡す引数。

###### <a name="callback-function-optional"></a>コールバック (関数、オプション)

指定された関数が返されたときに呼び出すコールバック関数。 コールバックには、呼び出された関数が返す値が渡されます。 次の例では、**printName** 関数で **apply** 関数を呼び出します。

```xpp
self.Name = "Joanne M Gordon";
var printName = function () {
    console.log(this.Name);
};
$dyn.callFunction(printName, self);
```

次の例では、**getWholeName** 関数を呼び出します。

```xpp
var getWholeName = function (first, middle, last) {
    var wholeName = first + " " + middle + " " + last;
    return wholeName;
};
var printName = function (wholeName) {
    console.log("Your name is: " + wholeName);
};
var firstName = "Joanne";
var middleName = "M";
var lastName = "Gordon";
$dyn.callFunction(getWholeName, null, [firstName , middleName, lastName], printName);
```

#### <a name="dynformat"></a>$dyn.format

##### <a name="usage"></a>用途

指定された形式に基づいて指定された値を使用する文字列を作成します。

##### <a name="arguments"></a>引数

###### <a name="format-string"></a>形式 (文字列)

文字列を作成する形式。 プレースホルダーにはブラケット表記を使用します。

###### <a name="values-optional"></a>値 (省略可)

このフォーマットで使用するコンマ区切りの値

##### <a name="returns"></a>返品

###### <a name="formattedstring-string"></a>FormattedString (文字列)

書式設定が適用された後の文字列次の例では、最初の文字列、中間の最初の文字列、最後の文字列を含む文字列を作成します。

##### <a name="example-1"></a>例 1

```xpp
var first = "Joanne";
var middle = "M";
var last = "Gordon";
var $dyn.format("Your name is : {0} {1} {2}", first, middle, last);
```

#### <a name="dynlabel"></a>$dyn.label

##### <a name="usage"></a>用途

グローバリゼーション API 経由で保存されている任意のラベルへのアクセスを提供します。

##### <a name="arguments"></a>引数

###### <a name="identifier-string"></a>ID (文字列)

グローバリゼーション API に指定されているラベル ID。

##### <a name="returns"></a>返品

###### <a name="value-string"></a>値 (文字列)

識別子が見つかった場合の、現在のカルチャ内のラベル文字列。 それ以外の場合、提供された識別子を文字列として返します。 次の例では、"greeting" という名前のラベルを返して出力します。

```xpp
Globalize.addCultureInfo("en", {
    messages: {
        "greeting": "Hello!"
    },
});
console.log($dyn.label("greeting"));
```

## <a name="css"></a>CSS

コントロールのテンプレート ID を持つクラス名を付加して、すべての CSS クラス名に名前空間を追加します。 これにより、コントロールとそのスタイルがクライアントの他のコントロールと競合するのを防ぐことができます。

## <a name="flexbox"></a>Flexbox
高度なレイアウト シナリオでは、Flexbox の使用をお勧めします。 Flexbox は、拡張可能な管理フレームワークと互換性があります。 [CSS 変動ボックス (Mozilla 開発者ネットワーク) を使用する](https://developer.mozilla.org/docs/Web/CSS/CSS_Flexible_Box_Layout/Using_CSS_flexible_boxes) 次のトピックの説明と例については [パブリック Flexbox ドキュメント](https://developer.mozilla.org/docs/Web/CSS/CSS_Flexible_Box_Layout/Using_CSS_flexible_boxes) を参照してください。

-   反応の敏感なレイアウト
-   列および行の構築
-   水平垂直方向に要素を配置する
-   入れ子要素の階層化
-   伸縮し縮小する要素の自動サイズ変更
-   要素のロック/凍結
-   スクロール可能な要素の作成

## <a name="control-lifecycle-diagrams"></a>制御ライフサイクル図

### <a name="control-instantiation"></a>インスタンス化の制御
[![Extensibility プロセス](./media/extensibilityprocess-951x1024.png)](./media/extensibilityprocess.png)
