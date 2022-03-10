---
title: ルックアップのコンテキスト データ入力
description: このトピックでは、コンテキスト データ入力の仕組みについて説明し、ルックアップにこの動作が必要な開発者向けの実装の詳細とヒントを提供します。
author: jasongre
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Developer
ms.reviewer: tfehr
ms.custom: 13631
ms.assetid: 5c41c565-5f83-47f9-a75e-ca5bb4b062e7
ms.search.region: Global
ms.author: jasongre
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 7853e04af21dde1ad7d6b2595a64973252b0e65b
ms.sourcegitcommit: 9acfb9ddba9582751f53501b82a7e9e60702a613
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/10/2021
ms.locfileid: "7783136"
---
# <a name="contextual-data-entry-for-lookups"></a>ルックアップのコンテキスト データ入力

[!include [banner](../includes/banner.md)]

データ入力のシナリオでは、そのエンティティが番号順序などの統合キーによって正式に識別される場合、ユーザーは詳細な内容を示す属性や自然言語属性でエンティティを識別しようとすることが一般的です。 コンテキスト データ入力機能を使用すると、統合キーまたはより記述的な属性のいずれかを検索フィールドに直接入力できます。 このページでは、コンテキスト データ入力の仕組みについて説明し、ルックアップにこの動作が必要な開発者向けの実装の詳細とヒントを提供します。

## <a name="introduction"></a>はじめに

データ入力のシナリオでは、そのエンティティが番号順序などの統合キーによって正式に識別される場合、ユーザーは詳細な内容を示す属性や自然言語属性でエンティティを識別しようとすることが一般的です。 ユーザーは、通常、Sales Order の作成時に **顧客口座** の **アカウント ID** の代わりに **アカウント名** を入力しようとします。 これは、顧客とのほとんどのやり取りは、何らかの統合識別子の代わりに実際の名前を使用して行われるためです。 ただし、**顧客 ID** コントロールの基礎となる外部キーが、合成キー (数字のシーケンス) であるフィールドに関連するため、**アカウント名** を入力しようとすると失敗します。AX 2012 (およびそれ以前) は、入力された値を常に直接検証しようとします。 したがって、正しい **アカウント ID** を特定するために、**顧客アカウント** コントロールのルックアップを開き、**アカウント名** 列をフィルタリングするなど、**アカウント ID** がユーザーに知られていない場合、ユーザーは何らかのタイプの検索ステップを実行することを余儀なくされます (次の画像を参照)。 

[![正しいアカウント ID を識別するためのアカウント名でのフィルタリングの例。](./media/howtocontextuallookups-3.png)](./media/howtocontextuallookups-3.png) 

このユーザー エクスペリエンスは最適ではないため、データ入力の効率性と生産性によって対処されています。 このプラットフォームは、コンテキスト データ入力の初期サポートを追加します。コンテキスト データ入力では、システムは、ユーザーが入力したデータがキー フィールドであるか、あるいはその他のより記述的またはよく分かっているフィールドであるかという状況を理解し、それを適切に処理することを自動的に試みます。 **このドキュメントの残りの部分では、これらのタイプのフィールドをそれぞれ ID (統合) フィールドと NAME (内容を示す) フィールドと総称して参照します。**

## <a name="contextual-lookup-forms"></a>コンテキストのルックアップ フォーム
キーボード データの入力と同じように、システム生成のすべてのルックアップ フォームでもコンテキストを持つようになり、ユーザーが入力したデータのコンテキストでフィルター処理および並べ替えが発生します。 販売注文シナリオの作成を例として使用すると、ID が入力された場合、ユーザーには次のようにルックアップが表示されます。 

[![ID のコンテキストで開かれた顧客アカウントの検索フォーム。](./media/howtocontextuallookups-1.png)](./media/howtocontextuallookups-1.png) 

NAME が入力された場合は、次のルックアップが表示されます。 ユーザーのデータが名前のコンテキストにあるときに、グリッドで最初に名前の列が移動する方法と、ルックアップの並べ替えおよびフィルターの方法を確認します。 

![顧客 ID のルックアップ フォームを名前のコンテキストで開きます。](./media/howtocontextuallookups-2.png)

## <a name="contextual-data-entry-implementation-details"></a>コンテキスト データ入力の実装の詳細
### <a name="behavior"></a>動作

上記の販売注文の作成シナリオのコンテキストでは、コンテキストでのデータ入力機能により、ユーザーは手間のかかる検索プロセスを実行せずに ID または名前を自由に入力できます。 詳細には、次のような挙動が発生します。

1.  完全な ID の参照を入力すると、値が直接適用されます。
2.  ユーザーが完全且つ固有の名前の参照を入力すると、値は ID に自動的に変換され、処理されます。
3.  ユーザーが完全でない ID または NAME 参照を入力した場合 (次のように *Micro* の代わりに *Microsoft*)、BEGINS WITH 述部を介して ID または NAME のいずれかと一意に一致する場合、その値は完全 ID に変換されて処理されます。
4.  ユーザーが完全でない ID または一意ではない NAME を入力し、複数の一致がある場合、*一義化* ルックアップがユーザーに提示され、実際にどの値が意図されたかを選択します。

コンテキスト データ入力の詳細な使用シナリオについては、付録 A を参照してください。

### <a name="prerequisites"></a>前提条件

機能の正確性と適切なパフォーマンスを管理するために、前のセクションで説明した動作の適用に以下の制約が追加されました。

1. **タイトル フィールド 2** が名前フィールドです**。
2. NAME フィールドは、インデックスでカバーされているか _ **または** _ *Cache Lookup* プロパティが *EntireTable* に設定されているテーブルに属している必要があります。 すべてのコンテキスト ルックアップ動作がパフォーマンス上の理由でこの要件に満たされていない場合は無効になります。 **注: インデックスの保守コストのために、NON TRANSACTIONAL テーブルに対してのみインデックスを追加する必要があります。** また **このインデックスを一意ではないとマークする可能性が高い** (重複を許可 = はい) に注意してください。
3. コントロールでカスタム検索フォーム (EDT 上の SysTableLookup; FormHelp など) が使用されている場合、前述の曖昧さ回避の動作は既定でオンになりません。 これは、これらのカスタム ルックアップ フォーム (および周囲の修正メソッドやルックアップ メソッドのオーバーライドさえも) は、コンテキストのルックアップのコンテキストでは望ましくないダイアログを提示するなどの高度な処理を行うことができるためです。

カスタム ルックアップ フォームの処理には追加の情報が必要で、独自のセクションで対象となります。

### <a name="programming-model-additions"></a>プログラミング モデルの追加

*一覧 1* および *一覧 2* に表される動作およびルールは、*FormControlAmbiguousReferenceResolver* と呼ばれる新しい X++ クラスに主に含まれています。 *FormControlAmbiguousReferenceResolver* より高度なシナリオでは、アプリケーション コードの取得が必要になります。 その使用についてはドキュメントの後半で説明します。 *FormControlAmbiguousReferenceResolver* クラスに加えて、*resolveAmbiguousReference* と呼ばれる新しいコントロールのオーバーライドが追加されました。 R *esolveAmbiguousReference* は、システムで発生している値にユーザーが入力した内容を変換するために、システムでフック ポイントとして機能します。 基本的なフローは次のとおりです。

1.  ユーザーがコントロールに値を入力し、フォーカスを削除します。
2.  インタラクションはクライアントからサーバーへ送信され、新しい値が入力されたことを示します。 適切なコマンドがサーバーで実行されます。
3.  コマンドがユーザーによって入力された値をプロセスしようとする前に、*resolveAmbiguousReference* を呼び出して、システムが値を予想されるドメインに変換できるようにします。
4.  resolveAmbiguousReference のスーパー実装は、上記のルールを実行する *FormControlAmbiguousReferenceResolver* インスタンスを作成します。

*resolveAmbiguousReference* から返される値は、コマンドの実行の残りの部分に使用します。 Validate() および modified() は、返された値に対して機能します。

## <a name="standard-lookup-uptake"></a>標準参照の取得
### <a name="add-an-index-that-covers-titlefield2"></a>TitleField2 の対象となるインデックスの追加

*TitleField2* 名前のデフォルト定義を定義します。 ID と名前のコンテキストのデータ入力を有効にするために、*TitleField2* をインデックスするか、*EntireTable* に対して *CacheLookup* を設定したテーブルに含める必要があります。 *TitleField2* を含むテーブルで *TitleField2* をカバーするインデックスを定義しない場合、**重要な事は、テーブルに大量の CUD (作成/更新/削除\*) がないため**、*TitleField2* をカバーする **一意ではない** インデックス (重複を許可する = はい) を追加します。 これにより、前提条件のセクションで説明したカスタム ルックアップの制限を除いて、システムはコンテキスト データ入力動作の実行を開始します。 \*大量のトランザクション テーブルにインデックスを追加すると、インデックス保守コストのために顕著なパフォーマンス ペナルティが発生する場合があります。

### <a name="enable-disambiguation-behavior-for-custom-lookup-scenarios"></a>カスタム ルックアップ シナリオの曖昧性解消動作の有効化

カスタム ルックアップの実装では、ダイアログの提示など、高度な動作や非典型的な動作を提供できます。 したがって、カスタム ルックアップ シナリオが検出されると、システムは既定の曖昧さ回避動作を無効にします。 既定の曖昧性解消動作を有効にするには、**ルックアップをホストするコントロール** で *resolveAmbiguousReference* メソッド (下記参照) をオーバーライドします。 *resolveAmbiguousReferenceForControl* の呼び出しに対する 2 つ目のパラメーターは、カスタム ルックアップ シナリオについて曖昧性解消を実行しないという既定の動作をオーバーライドするものであることに注意してください。

```xpp
public str resolveAmbiguousReference()
{
    FormControlAmbiguousReferenceResolver::resolveAmbiguousReferenceForControl (this, true);
}
```

### <a name="make-custom-lookup-forms-contextual"></a>カスタム ルックアップ フォームをコンテキストにする

先に述べたように、システム生成のルックアップ フォームはすべて、ホスト コントロールに入力されたデータのコンテキストを自動的に考慮します。 これには、*SysTableLookup* によって生成されるほとんどのルックアップ フォームが含まれます。 モデル化されたカスタム ルックアップ フォームは、その性質によってシステムで完全に処理することはできず、コンテキストのルックアップ フォームの動作およびビジュアルと一致するように変更する必要があります。

1.  ホスト コントロールに含まれるデータが ID のコンテキスト内にある場合:
    1.  グリッドにまず ID 列を作成します。
    2.  ID により並べ替えてフィルター処理します。

2.  ホスト コントロールに含まれるデータが NAME のコンテキスト内にある場合:
    1.  グリッドにまず名前列を作成します。
    2.  NAME により並べ替えてフィルター処理します。

次のシナリオでは、カスタム ルックアップと、これらの場合のコンテキストでのデータ入力を有効にする方法の推奨事項を示しています。

#### <a name="scenario-1-custom-lookup-defined-via-the-formhelp-property-on-an-edt"></a>シナリオ 1: EDT で FormHelp プロパティ経由で定義されたユーザー設定のルックアップ

FormHelp で定義されたカスタム ルックアップ (モデル化されていても) は、通常のカーネル ベースのルックアップ生成ルーティンをそのまま使います。 したがって、カーネルには引き続きルックアップ フォームを変更するためのフックがあります。 具体的には、ルックアップ システムに、正しいフィルターおよび並べ替えを適用するための十分な情報があります。ただし、ルックアップのグリッドで移動すべきコントロールは既知ではありません。  (バインディングに基づいて推測することは可能ですが、その推測はより高度なルックアップ フォーム デザインでは不正確である可能性があります)。カスタム ルックアップ フォームが `SysTableLookup::filterLookupPreRun` メソッドおよび `SysTableLookup::filterLookupPostRun` メソッドを利用している場合、`filterLookupPostRun` で (新しい) オプション パラメーターを取得して、名前コントロールを次のように自動的に移動させます。

```xpp
public class MyCustomLookupForm extends FormRun
{
    public void run()
    {
        FormStringControl lookupHostControl = SysTableLookup::getCallerStringControl(this.args());
        boolean isFiltered = SysTableLookup::filterLookupPreRun(lookupHostControl, ID_Control, FormDataSourceToFilter);

        super();

        SysTableLookup::filterLookupPostRun(isFiltered, lookupHostControl.text(), ID_Control, FormDataSourceToFilter, 
            new FormControlAmbiguousReferenceResolver(callingControl), NAME_Control);
    }
}
```

ルックアップ フォームが *SysTableLookup::filterLookup\** メソッドを使用しておらず、それらのメソッドを取得しない場合、以下のように、単にコントロール移動を追加することができます。

```xpp
public class MyCustomLookupForm extends FormRun
{
    public void init()
    {
        super();
        this.applyControlOrdering();
    }

    private void applyControlOrdering()
    {
        FormControl callerControl = SysTableLookup::getCallerControl(this.args());
        if (FormControlAmbiguousReferenceResolver::isControlValueMappedToAlternativeField(callerControl))
        {
            Grid.moveControl(ID_Control.id(), NAME_control.id());
        }
        else
        {
            Grid.moveControl(NAME_Control.id(), ID_Control.id());
        }
    }
}
```

#### <a name="scenario-2-override-of-lookup-method-manually-launching-a-form"></a>シナリオ 2: フォームを手動で起動するルックアップ メソッドの上書き

シナリオ 1 とは異なり、クラス ファクトリなどの完全な手動メカニズムによって起動されるルックアップ フォームにはカーネル フックはありません。 したがって、コンテキスト データ入力動作を遵守するのはルックアップ フォームの責任です。 これを行う最も簡単な方法は、並べ替えを維持する必要があることを示す 1 つの追加パラメーターを含めることを除いて、(シナリオ 1 と同様の) SysTableLookup::filterLookup\* メソッドを活用することです。 例として以下に表示します。

```xpp
public class MyCustomLookupForm extends FormRun
{
    public void run()
    {
        FormStringControl lookupHostControl = SysTableLookup::getCallerStringControl(this.args());
        boolean isFiltered = SysTableLookup::filterLookupPreRun(lookupHostControl, ID_Control, FormDataSourceToFilter);

        super();

        SysTableLookup::filterLookupPostRun(isFiltered, lookupHostControl.text(), ID_Control, FormDataSourceToFilter, 
            new FormControlAmbiguousReferenceResolver(callingControl), NAME_Control, true);
    }
}
```

## <a name="advanced-lookup-uptake"></a>高度なルックアップの取得
### <a name="scenario-1-overriding-id-and-name-bindings"></a>シナリオ 1: ID と NAME バインドの上書き

既定で選択されている以外のフィールドのセットを使用する場合は、*FormControlAmbiguousReferenceResolver* のインスタンスを手動で構築し、カスタム バインドを表すオプションのパラメーターを指定する必要があります。 この特別なインスタンスは、*resolveAmbiguousReference* のオーバーライドおよびカスタム ルックアップ フォーム (*FormControlAmbiguousReferenceResolver* のインスタンスも受け入れる *SysTableLookup* など) で使用する必要があります。 カスタム バインディングは、現在カーネルによって生成されるルックアップで指定できません。 現在カスタムの ID と名前のバインディングを受け入れているメソッド:

1.  FormControlAmbiguousReferenceResolver
    -   コンストラクター
    -   resolveAmbiguousReferenceForControl
    -   surrogateFKHelperForAlternativeFieldMapping
    -   isControlValueMappedToAlternativeField

カスタム バインドを提供する方法のエンド ツー エンドの例を次に示します。

```xpp
[Control Hosting Lookup]
public str resolveAmbiguousReference()
{
    return FormControlAmbiguousReferenceResolver::resolveAmbiguousReferenceForControl(
        this, true, AbsoluteFieldBinding::construct(IDField, Table), 
        AbsoluteFieldBinding::construct(SomeOtherNAMEField, Table));
}

[Custom Lookup Form]
public class MyCustomLookupForm extends FormRun
{
    public void run()
    {
        FormStringControl lookupHostControl = SysTableLookup::getCallerStringControl(this.args());
        boolean isFiltered = SysTableLookup::filterLookupPreRun(lookupHostControl, ID_Control, FormDataSourceToFilter);

        super();

        SysTableLookup::filterLookupPostRun(isFiltered, lookupHostControl.text(), ID_Control, FormDataSourceToFilter, 
            new FormControlAmbiguousReferenceResolver(callingControl, AbsoluteFieldBinding::construct(IDField, Table),
            AbsoluteFieldBinding::construct(SomeOtherNAMEField, Table)), NAME_Control, true);
    }
}
```

### <a name="scenario-2-custom-resolution-logic"></a>シナリオ 2: カスタム解像度ロジック

resolveAmbiguousReference をオーバーライドし、FormControlAmbiguousReferenceResolver 以外のものを活用することによってカスタム解決ロジックを使用できます。 このロジックは、キーボードおよびルックアップ ベースのエントリが常に同期されるように、ホストされているルックアップ フォームと共通にする必要があることに注意してください。

```xpp
public str resolveAmbiguousReference()
{
    // In this sample, allow “looser” data entry by simply picking the first record that matches, if any.
    CLI_Job _job;
    str mappedValue = this.text();
    if (strLen(mappedValue) > 0)
    {
        select firstonly _job order by _job.Title where _job.Title like mappedValue + “*”;
    }

    if (_job.RecId)
    {
        mappedValue = _job.Title;
    }

    return mappedValue;
}
```

## <a name="appendix--detailed-usage-scenarios-for-contextual-data-entry"></a>付録コンテキスト データ入力の詳細な使用シナリオ
シナリオでは、PK フィールド「ID」およびインデックス フィールド「名」を持つ「TableA」と呼ばれるテーブルがあり、FK で ID (ユーザーは最終的には ID をピックする必要がある) に関連するものを入力しようとしていると仮定します。 類似または始まる値に依存するアルゴリズムは、文字列フィールドを想定していることに注意してください。 たとえば、整数型では、高品質の解決の動作を提供することはできません。 

**シナリオ 1: ユーザーが 有効な ID 「1234」を入力する** resolveReference の super() 実装は、適切な述部で TableA.ID を最初に照会します。 クエリは単一のレコードを検索し、ユーザーの入力値を返して、検証および変更によって追加の処理に進みます。 検証が成功すると、UI に「1234」と表示されます。 

**シナリオ 2: ユーザーが 無効な ID 「4321」を入力します** resolveReference の super() 実装が TableA.ID に対する最初のクエリを実行します。 クエリはレコードを検索しないため、2 番目のクエリは Name フィールドに対して実行されます (SELECT TOP 2 FROM TableA WHERE TableA.Name LIKE "4321％")。 それでもレコードが見つからないため、検証を通じて「4321」が渡されますが、失敗します。 ユーザーはブラウザーで「4321」と表示され、検証エラーが発生します。 

**シナリオ 3: ユーザーが「ACME」の有効な名前を入力する** resolveReference の super() 実装が TableA.ID に対する最初のクエリを実行します。 クエリはレコードを検索しないため、2 番目のクエリは Name フィールドに対して実行されます (SELECT TOP 2 FROM TableA WHERE TableA.Name LIKE "ACME％")。 このクエリは単一のレコード (一意の参照) を検索するので、ルックアップは対応する TableA.ID を自動的に返します。 その値のコンテキストでの実行を検証および変更継続します。 検証が成功すると、最終的にはブラウザーに ACME の ID 値が表示されます (たとえば、ブラウザーで ACME は 1234 に切り替わります)。 

**シナリオ 4: ユーザーが「ACNE」の無効な名前を入力する** resolveReference の super() 実装が TableA.ID に対する最初のクエリを実行します。 クエリはレコードを検索しないため、2 番目のクエリは Name フィールドに対して実行されます (SELECT TOP 2 FROM TableA WHERE TableA.Name LIKE "ACNE％")。 このクエリではレコードが見つからないため、ルックアップによって ACNE が検証に渡されますが検出できません。 ユーザーはブラウザーで「ACNE」と表示され、検証エラーが発生します。 

**シナリオ 5: ユーザーが「ACME」のあいまいな名前を入力する** この場合は、データベース内に 2 つのレコードがあると仮定 : 1 つは「ACME W」という名前で、もう 1 つは「ACME E」とします。 TableA.ID に対する resolveReference の最初のクエリの super() 実装。 クエリはレコードを検索しないため、2 番目のクエリは Name フィールドに対して実行されます (SELECT TOP 2 FROM TableA WHERE TableA.Name LIKE "ACME％")。 このクエリは 2 つのレコードを検出します。それ以上の仮定はできません。 曖昧性解消ルックアップは、"ACME W" と "ACME E" を示すユーザーに選択肢として表示されます。 ユーザーは「ACME E」を選択します。 resolveReference を選択してから、選択したレコードを取得して "ACME E" の ID にリダイレクトします。 "ACME E" の ID コンテキストでの実行を検証および変更継続します。 ブラウザーは最終的に "ACME E" の ID を表示します (たとえば、1234)。 

**シナリオ 6: ユーザーが「ACME」のあいまいな名前を入力し、非不明瞭ルックアップで選択しないこと** この場合は、データベース内に 2 つのレコードがあると仮定 : 1 つは「ACME W」という名前で、もう 1 つは「ACME E」とします。 TableA.ID に対する resolveReference の最初のクエリの super() 実装。 クエリはレコードを検索しないため、2 番目のクエリは Name フィールドに対して実行されます (SELECT TOP 2 FROM TableA WHERE TableA.Name LIKE "ACME％")。 このクエリは 2 つのレコードを検出します。それ以上の仮定はできません。 曖昧性解消ルックアップは、"ACME W" と "ACME E" を示すユーザーに選択肢として表示されます。 ユーザーはルックアップから選択しません。 したがって、「ACME」が検証され、変更されます。 検証が失敗し、ユーザーに検証エラー メッセージが表示されます。 ブラウザーには "ACME" という値が表示されます。 

**シナリオ 7: ユーザーはが有効な ID「12」を入力し、ルックアップ フォームを提示します** ルックアップを提示する前に、システムは TableA.ID (「12%」のような TableA の ID からトップ 1 を選ぶ) に対して照会します。 クエリはレコードを検出するため、ユーザーが ID のコンテキストで操作しているものと想定されます。 これは、ID でのルックアップ、フィルターや並べ替えを提供します。 

**シナリオ 8: ユーザーが無効な ID 「4321」を入力し、ルックアップ フォームを提示します** ルックアップを提示する前に、システムは TableA.ID (「4321%」 のような TableA の ID からトップ 1 を選ぶ) に対して照会します。 クエリで一致するレコードが見つからないため、ユーザーが名前を入力していることを前提としています。 ルックアップは、フィルタリングされ、名前 (この場合はレコードは表示されません) で並べ替えられて表示されます。 

**シナリオ 9: ユーザーが「AC」の「有効な」名前を入力し、ルックアップ フォームを提示します** ルックアップを提示する前に、システムは TableA.ID(「AC%」のような TableA.ID からトップ 1 を選ぶ) に対して照会します。 クエリで一致するレコードが見つからないため、ユーザーが名前を入力していることを前提としています。 ルックアップは、フィルタリングされたもの (「AC で始まる」に一致するレコード) とアルファベット順の名前で並べ替えられて表示されます。 

**シナリオ 10: ユーザーが無効な「EM」という名前を入力し、ルックアップ フォームを提示します** ルックアップを提示する前に、システムは TableA.ID (「EM%」のような TableA の ID からトップ 1 を選ぶ)に対して照会します。 クエリで一致するレコードが見つからないため、ユーザーが名前を入力していることを前提としています。 ルックアップは、フィルタリングされ、名前で並べ替えられて表示されます。 レコードが見つからないため、空白のルックアップがユーザーを表示されます。





[!INCLUDE[footer-include](../../../includes/footer-banner.md)]