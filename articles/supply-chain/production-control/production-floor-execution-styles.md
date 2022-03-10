---
title: 生産現場の実行インターフェースのスタイル
description: このトピックでは、既定の生産フロア実行スタイルが適用されるように、フォーム コントロールを構成する方法について説明します。
author: johanhoffmann
ms.date: 11/08/2021
ms.topic: article
ms.search.form: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2021-02-22
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: ef39dc6414f0afdadd4a4b5a41e1fb1fe60e4974
ms.sourcegitcommit: bc9e75c38e192664cde226ed3a94df5a0b304369
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/10/2021
ms.locfileid: "7790893"
---
# <a name="style-the-production-floor-execution-interface"></a>生産現場の実行インターフェースのスタイル

[!include [banner](../includes/banner.md)]

このトピックでは、既定の生産フロア実行スタイルが適用されるように、フォーム コントロールを構成する方法について説明します。

## <a name="forms-and-dialogs"></a>フォームおよびダイアログ

スタイルは、次の要件が満たされている場合にのみ、フォームまたはダイアログに適用されます。

- フォームが既存のレポートの進行状況フォームと類似している場合は、フォームまたはダイアログの名前を `JmgProductionFloorExecutionCustomInputDialog` で始める必要があります。
- フォームまたはダイアログには、詳細フォームのパーツを含めることができます。 スタイルをそれに適用するには、詳細フォームパーツの名前は `JmgProductionFloorExecutionCustomDetailsDialog` で始まる必要があります。
- フォームまたはダイアログに簡単なビューを表示する必要がある場合は、簡易ビューの名前を `JmgProductionFloorExecutionCustomDialog` で始める必要があります。 簡易ビューを持つフォームの例としては、開始フォームおよび間接活動フォームがあります。
- ダイアログのすべてのコントロールをこのトピックで説明されているように構成する必要があります。

> [!IMPORTANT]
> このリストの最初の 2 つのポイントで述べた機能には、Supply Chain Management バージョン 10.0.19 以降が必要です。

スタイルは、次の要件が満たされている場合にのみ、ダイアログの **OK** ボタンに適用されます。

- ボタンはフォーム グループに含まれています。
- グループ名は `OkButtonGroup` で始まります。

スタイルは、次の要件が満たされている場合にのみ、ダイアログ ボックスの **キャンセル** ボタンに適用されます。

- ボタンはフォーム グループに含まれています。
- グループ名が `CancelButtonGroup` で始まる。

### <a name="header"></a>ヘッダー

次の図は、一般的なフォームまたはダイアログ ヘッダーを示しています。

![一般的なフォームまたはダイアログ ヘッダー。](media/pfe-styles-header.png "一般的なフォームまたはダイアログ ヘッダー")

Visual Studio では、次の図に示す構造を使用してヘッダーが作成されます。

![ヘッダーを作成するための標準的なコード構造。](media/pfe-styles-header-code-structure.png "ヘッダーを作成するための標準的なコード構造")

ヘッダーにテキストを追加するには、次の例のようなコードを使用します。

```xpp
private void setCaption()
{
    HeaderFieldWithSeparatorText1.text("Report Progress");
    HeaderFieldWithSeparatorText2.text(ProdId);

    …

    HeaderFieldText.text(OprNum);
}
```

ヘッダー コードを記述する際には、次のルールを適用します。

- メイン グループの名前は `TableRowHeaderGroup` である必要があります。
- テキストの各ブロック (形式で区切る) は、`HeaderFieldWithSeparatorText` で始まる必要があります。
- 最後のテキスト名は、`HeaderFieldText` で始まる必要があります。
- `CaptionImage` は省略できます。

### <a name="progress-indicator"></a>進捗状況インジケーター

ヘッダーの右側に表示される進捗状況インジケーターを含めることができます。 次の図は、進捗状況インジケーターを示します。

![一般的な進捗状況インジケーター。](media/pfe-styles-header-progress.png "一般的な進捗状況インジケーター")

進捗状況インジケーターを表示するには、テキスト フィールド名が `ShowProgress` である必要があります。

## <a name="grid"></a>グリッド

スタイルは自動的に適用されます。 固有のコンフィギュレーションは必要はありません。

新しいグリッドはまだサポートされていないので、グリッドは `TabularView` スタイルである必要があり、カスタム フォーム上の `run()` メソッドは上書きされている必要があります。 次のコードを追加します。

```xpp
public void run()
{
    super();
    // To opt out a page from the new grid
    this.forceLegacyGrid();
}
```

メイン ビューのデータを更新するには、アクションの `click` メソッドの `this.parmParentForm().updateLayout();` のような何かを使用すると良いです。 (例としては、`JmgProductionFloorExecutionReportFeedbackAction` クラスを参照してください。) `parmDataSource` が新しいフォーム (`formCaller.parmDataSource(this.dataSource(1));`) の `init` の メソッドで設定されていることを確認します。 例については、`JmgProductionFloorExecutionMainGrid` フォームを参照してください。

## <a name="card-view"></a>カード ビュー

スタイルは、次の要件が満たされている場合にのみ、カード ビュー コントロールに適用されます。

- 各カード ビューはフォーム グループに含まれています。
- グループ名が `CardGroup` から始まる (たとえば、`CardGroupJobsView`)。

次の図は、その中にコントロールがないカード ビューを示しています。

![要素のないカード ビュー。](media/pfe-styles-empty-card.png)

次の図は、その中にコントロールを含んでいるカード ビューを示しています。

![Hz を示す要素を含むカード。](media/pfe-styles-elements.png)

![メンテナンス要求の要素を含むカード。](media/pfe-styles-elements-maintenance.png)

## <a name="business-card"></a>ビジネス カード

スタイルは、次の要件が満たされている場合にのみ、ビジネス カード コントロールに適用されます。

- 各ビジネス カードはフォーム グループに含まれています。
- グループ名は `BusinessCardGroup` から始まる (たとえば、`BusinessCardGroupJobsList`)。

ビジネス カードで以下のプロパティを設定します。

- **スタイル:** *リスト*
- **拡張型スタイル:** *cardList*
- **複数選択:** *いいえ*
- **列ラベルの表示:** *いいえ*

![ビジネス カード。](media/pfe-styles-business-card.png)

## <a name="radio-button"></a>オプション ボタン

スタイルは、次の要件が満たされている場合にのみ、ラジオ ボタンに適用されます。

- 各ラジオ ボタンはフォーム グループに含まれています。
- グループ名が、テキストを表示させる場所に応じて、`RadioTextBelow` または `RadioTextRight` で始まる。

ラジオ ボタンに以下のプロパティを設定します。

- **トグル ボタン:** *検査*
- **トグル値:** ラジオ ボタンを選択する必要がある場合は *オン*、それ以外の場合は *オフ*

次の図は、テキストがラジオ ボタンの下に表示される例を示しています。

![下にテキストが表示されているラジオ ボタン。](media/pfe-styles-radio-text-below.png)

次の図は、テキストがラジオ ボタンの右に表示される例を示しています。

![右にテキストが表示されているラジオ ボタン。](media/pfe-styles-radio-text-right.png)

### <a name="radio-buttons-in-internet-explorer"></a>Internet Explorer のラジオ ボタン

ラジオ ボタン スタイルは Internet Explorer ではサポートされません。 次の図は、ラジオ ボタンが Internet Explorer でどのように表示されるかを示しています。

![Internet Explorer のラジオ ボタン。](media/pfe-styles-browser.png)

## <a name="buttons"></a>ボタン

スタイルは、次の要件が満たされている場合にのみ、ボタンに適用されます。

- 各ボタン グループはフォーム グループに含まれています。 グループ内のすべてのボタンは同じスタイルになります。
- グループ名に関する要件はありません。

ボタンに以下のプロパティを設定します。

- **ボタン表示:** *TextWithImageLeft*
- **通常のイメージ:** このプロパティを空白にすることはできません。 たとえば、*CoffeeScript* を使用します。
- **テキスト:** このプロパティを空白にすることはできません。 たとえば、*分割の開始* を使用します。
- **幅:** *自動* または *SizeToContent*
- **幅:** *自動* または *SizeToContent*

### <a name="primary-button"></a>プライマリ ボタン

スタイルは、次の要件が満たされている場合にのみ、基本ボタンに適用されます。

- ボタンはフォーム グループに含まれています。
- グループ名が `DefaultButtonGroup` または `PrimaryButtonGroup` で始まる (たとえば、`DefaultButtonGroup10`)。

![プライマリ ボタン。](media/pfe-styles-first.png)

### <a name="secondary-button"></a>セカンダリ ボタン

スタイルは、次の要件が満たされている場合にのみ、二次ボタンに適用されます。

- ボタンはフォーム グループに含まれています。
- グループが **右側のパネル** と名前が付けられている、またはグループ名が `SecondaryButtonGroup` で始まる。

![セカンダリ ボタン。](media/pfe-styles-second.png)

### <a name="third-group-button"></a>3 番目のグループ ボタン

スタイルは、次の要件が満たされている場合にのみ、3 番目のグループのボタンに適用されます。

- ボタンはフォーム グループに含まれています。
- グループが **左側のパネル** と名前が付けられている、またはグループ名が `ThirdButtonGroup` で始まる。

![3 番目のグループのボタン。](media/pfe-styles-third.png)

### <a name="fourth-group-button"></a>4 番目のグループのボタン

スタイルは、次の要件が満たされている場合にのみ、4 番目のグループのボタンに適用されます。

- ボタンはフォーム グループに含まれています。
- グループ名が `FourthButtonGroup` で始まる。

ボタンに以下のプロパティを設定します。

- **ボタン表示:** *TextOnly*
- **通常のイメージ:** このプロパティは空白にする必要があります。
- **テキスト:** このプロパティを空白にすることはできません。 たとえば、*表示* または *編集* を使用します。
- **幅:** *自動*
- **高さ:** *自動*

![4 番目のグループ ボタン。](media/pfe-styles-fourth.png)

### <a name="flat-button"></a>フラット ボタン

スタイルは、次の要件が満たされている場合にのみ、フラット ボタンに適用されます。

- ボタンはフォーム グループに含まれています。
- グループ名が `FlatButtonGroup` で始まる。

ボタンに以下のプロパティを設定します。

- **ボタン表示:** *ImageOnly*
- **通常のイメージ:** このプロパティを空白にすることはできません。 たとえば、*CoffeeScript* を使用します。
- **テキスト:** このプロパティは空白にする必要があります。
- **幅:** *自動* または *SizeToContent*
- **幅:** *自動* または *SizeToContent*

![フラット ボタン。](media/pfe-styles-flat-button.png)

### <a name="continue-button"></a>続行ボタン

スタイルは、次の要件が満たされている場合にのみ、続行ボタンに適用されます。

- ボタンはフォーム グループに含まれています。
- グループ名が `ContinueButtonGroup` で始まる。

ボタンに以下のプロパティを設定します。

- **ボタン表示:** *ImageOnly*
- **通常のイメージ:** *転送*
- **テキスト:** このプロパティは空白にする必要があります。
- **幅:** *自動* または *SizeToContent*
- **幅:** *自動* または *SizeToContent*

![続行ボタン。](media/pfe-styles-continue-button.png)

## <a name="combo-box"></a>コンボ ボックス

コンボ ボックスは、入力コントロール、入力コントロールをクリアするボタン、および検索を実行するボタンの 3 つのコントロールの組み合わせです。

スタイルは、次の要件が満たされている場合にのみ、コンボ ボックスに適用されます。

- コンボ ボックスはフォーム グループに含まれています。
- グループ名が `Combobox` で始まる。
- グループ内で、最初のコントロールは `AxFormStringControl` です。 このコントロールは現在の値を表示し、ユーザーは必要な値を入力します。
- 2 つ目のコントロールは `CommonButton` コントロールで、名前は `ClearButton` で始まります。 このボタンには、ボタンを表示または非表示にする `enable` プロパティを使用するコードが含まれている必要があります。 たとえば、ユーザーが入力コントロールに情報を入力している間に **クリア** ボタンを表示または非表示にするには、次のコードを使用することができます。

    ```xpp
    public void textChange()
    {
        super();
        ClearButtonSerial.enabled(this.text()? true : false);
    }
    ```

    入力コントロールでデータを設定する方法が 1 つ必要です。 そのメソッドの **クリア** ボタンを有効にします。 次に例を示します。

    ```xpp
    public void setSerialId(str _serialId)
    {
        JmgTmpJobBundleProdFeedback.InventSerial = _serialId;
        ClearButtonSerial.enabled(_serialId? true : false);

        if (_serialId)
        {
            this.addSerialNumber();
        }
    }
    ```

    **クリア** ボタンの `clicked` メソッドには次のコードを使用します。

    ```xpp
    public void clicked()
    {
        element.setSerialId('');
        InventSerialId.setFocus(); // set focus back to the input box
    }
    ```

    フォームを `init` メソッドを使用して初期化するときに、入力コントロール `AxFormStringControl` の値を設定します。 値が空白でない場合は、**クリア** ボタンを有効にします。 値が空白の場合は、**クリア** ボタンを無効にします。

- 3 つ目のコントロールは `CommonButton` コントロールで、名前は `SearchButton` で始まります。

次の図は、2 つのコンボ ボックス コントロールを示します。 左側のコンボ ボックスには空のテキスト ボックスがあり、**クリア** ボタンは無効になっています。 右側のコンボ ボックスにはテキスト ボックスにテキストがあり、**クリア** ボタンが有効になっています。

![クリア ボタン付き、またはなしのコンボ ボックス。](media/pfe-styles-combo.png)

## <a name="quick-filter"></a>クイック フィルター

クイック フィルター コントロールによって、ページに検索フィールドが追加されます。 次の要件が満たされている場合、クイック フィルターにスタイルを適用できます。

- クイック フィルターはフォーム グループに含まれています。
- グループ名が `SearchInputGroup` で始まる。
- グループ内で、最初のコントロールは `QuickFilter` コントロールです。 (このコントロールはユーザーが検索文字列を入力する場所です。)
- 2 つ目のコントロールは `NumberOfResults` という名前の `FormStaticTextControl` です。 (このコントロールはオプションです。 これが含まれている場合は、検出された項目の数が表示されます。)
- 3 つ目のコントロールは `CommonButton` コントロールで、名前は `ClearButton` で始まります。

次の図は、2 つのクイック フィルター コントロールを示します。 左側のクイック フィルターは空になっており、結果の数は表示されません。 右側のクイック フィルターには検索文字列が含まれるので、結果の数が表示されます。

![検索文字列を使用した場合、および使用しない場合のクイック フィルター コントロールの例。](media/pfe-styles-quick-filter.png "検索文字列を使用した場合および使用しない場合のクイック フィルター コントロールの例")

## <a name="center-align-elements-on-a-tab"></a>タブの中央位置揃え要素

タブの中央に要素の位置を合わせるには、グループ名は `TabContentGroup` で始まる必要があり、グループには次のプロパティが 必要です。

- **幅モード:** `SizeToAvailable`
- **高さモード:** `SizeToAvailable`

## <a name="align-a-grid-detail-part-and-quick-filter"></a>グリッド、詳細パーツ、クイック フィルターの位置を合わせる

標準のデザインに似たカスタマイズされたグリッド、詳細部品、クイック フィルターを並び替える場合は、それらをすべてまとめる際に次の点を念頭に置きます。

- グリッドに簡単なフィルタがある場合は、グリッドとクイック フィルタの両方が、名前が `GridGroup` ".
- スタイルを詳細部分に適用するには、グループ名は `DetailInformationGroup` で始まる必要があります。

次の図は、簡単なフィルターと右側の詳細部分を含む一般的なグリッドを示しています。

![クイック フィルターと詳細部分を含む通常グリッド。](media/pfe-styles-align-grid.png "クイック フィルターと詳細部分を含む通常グリッド")

Visual Studio では、次の図に示す構造を使用してグリッド、詳細部分、クイック フィルターを作成できます。

![グリッド、詳細部分、クイック フィルターに対応した通常コード構造。](media/pfe-styles-header-code-structure2.png "グリッド、詳細部分、クイック フィルターに対応した通常コード構造")

## <a name="additional-resources"></a>追加リソース

- [生産現場の実行インターフェースのカスタマイズ](production-floor-execution-customize.md)
- [生産現場の実行インターフェースをデザインする](production-floor-execution-tabs.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
