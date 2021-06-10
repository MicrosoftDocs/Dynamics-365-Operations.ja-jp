---
title: 生産現場の実行インターフェースのスタイル
description: このトピックでは、既定の生産フロア実行スタイルが適用されるように、フォーム コントロールを構成する方法について説明します。
author: johanhoffmann
ms.date: 02/22/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Developer
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2021-02-22
ms.dyn365.ops.version: Release 10.0.15
ms.openlocfilehash: 3ff7187bdd035a639ed8bb1eb61d643136db76c4
ms.sourcegitcommit: 588f8343aaa654309d2ff735fd437dba6acd9d46
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/28/2021
ms.locfileid: "6115037"
---
# <a name="style-the-production-floor-execution-interface"></a>生産現場の実行インターフェースのスタイル

[!include [banner](../includes/banner.md)]

このトピックでは、既定の生産フロア実行スタイルが適用されるように、フォーム コントロールを構成する方法について説明します。

## <a name="forms-and-dialogs"></a>フォームおよびダイアログ

スタイルは、次の要件が満たされている場合にのみ、フォームまたはダイアログに適用されます。

- フォームが既存のレポートの進行状況フォームと類似している場合は、フォームまたはダイアログの名前を **JmgProductionFloorExecutionCustomInputDialog** で始める必要があります。
- フォームまたはダイアログには、詳細フォームのパーツを含めることができます。 スタイルを適用するには、詳細フォームのパーツの名前を **JmgProductionFloorExecutionCustomDetailsDialog** で始める必要があります。
- フォームまたはダイアログに簡単なビューを表示する必要がある場合は、簡易ビューの名前を **JmgProductionFloorExecutionCustomDialog** で始める必要があります。 簡易ビューを持つフォームの例としては、開始フォームおよび間接活動フォームがあります。
- ダイアログのすべてのコントロールをこのトピックで説明されているように構成する必要があります。

> [!IMPORTANT]
> このリストの最初の 2 つのポイントで述べた機能には、Supply Chain Management バージョン 10.0.19 以降が必要です。

スタイルは、次の要件が満たされている場合にのみ、ダイアログの **OK** ボタンに適用されます。

- ボタンはフォーム グループに含まれています。
- グループ名が **OkButtonGroup** で始まる。

スタイルは、次の要件が満たされている場合にのみ、ダイアログ ボックスの **キャンセル** ボタンに適用されます。

- ボタンはフォーム グループに含まれています。
- グループ名が **CancelButtonGroup** で始まる。

## <a name="grid"></a>グリッド

スタイルは自動的に適用されます。 固有のコンフィギュレーションは必要はありません。

## <a name="card-view"></a>カード ビュー

スタイルは、次の要件が満たされている場合にのみ、カード ビュー コントロールに適用されます。

- 各カード ビューはフォーム グループに含まれています。
- グループ名が **CardGroup** で始まる (**CardGroupJobsView** など)。

次の図は、その中にコントロールがないカード ビューを示しています。

![要素のないカード ビュー](media/pfe-styles-empty-card.png)

次の図は、その中にコントロールを含んでいるカード ビューを示しています。

![Hz を示す要素を含むカード](media/pfe-styles-elements.png)

![メンテナンス要求の要素を含むカード](media/pfe-styles-elements-maintenance.png)

## <a name="business-card"></a>ビジネス カード

スタイルは、次の要件が満たされている場合にのみ、ビジネス カード コントロールに適用されます。

- 各ビジネス カードはフォーム グループに含まれています。
- グループ名が **BusinessCardGroup** で始まる (**BusinessCardGroupJobsList** など)。

ビジネス カードで以下のプロパティを設定します。

- **スタイル**: **リスト**
- **拡張スタイル**: **cardList**
- **複数選択**: **いいえ**
- **列ラベルの表示**: **いいえ**

![ビジネス カード](media/pfe-styles-business-card.png)

## <a name="radio-button"></a>オプション ボタン

スタイルは、次の要件が満たされている場合にのみ、ラジオ ボタンに適用されます。

- 各ラジオ ボタンはフォーム グループに含まれています。
- グループ名が、テキストを表示させる場所に応じて、**RadioTextBelow** または **RadioTextRight** で始まる。

ラジオ ボタンに以下のプロパティを設定します。

- **トグル ボタン**: **チェック**
- **トグル値**: ラジオ ボタンを選択する必要がある場合は **オン**、それ以外の場合は **オフ**

次の図は、テキストがラジオ ボタンの下に表示される例を示しています。

![下にテキストが表示されているラジオ ボタン](media/pfe-styles-radio-text-below.png)

次の図は、テキストがラジオ ボタンの右に表示される例を示しています。

![右にテキストが表示されているラジオ ボタン](media/pfe-styles-radio-text-right.png)

### <a name="radio-buttons-in-internet-explorer"></a>Internet Explorer のラジオ ボタン

ラジオ ボタン スタイルは Internet Explorer ではサポートされません。 次の図は、ラジオ ボタンが Internet Explorer でどのように表示されるかを示しています。

![Internet Explorer のラジオ ボタン](media/pfe-styles-browser.png)

## <a name="buttons"></a>ボタン

スタイルは、次の要件が満たされている場合にのみ、ボタンに適用されます。

- 各ボタン グループはフォーム グループに含まれています。 グループ内のすべてのボタンは同じスタイルになります。
- グループ名に関する要件はありません。

ボタンに以下のプロパティを設定します。

- **ボタン表示**: **TextWithImageLeft**。
- **通常のイメージ**: このプロパティを空白にすることはできません。 たとえば、**CoffeeScript** を使用します。
- **テキスト**: このプロパティを空白にすることはできません。 たとえば、**分割の開始** を使用します。
- **幅**: **自動**。
- **高さ**: **自動**。

### <a name="primary-button"></a>プライマリ ボタン

スタイルは、次の要件が満たされている場合にのみ、基本ボタンに適用されます。

- ボタンはフォーム グループに含まれています。
- グループ名が **DefaultButtonGroup** または **PrimaryButtonGroup** で始まる (**DefaultButtonGroup10** など)。

![プライマリ ボタン](media/pfe-styles-first.png)

### <a name="secondary-button"></a>セカンダリ ボタン

スタイルは、次の要件が満たされている場合にのみ、二次ボタンに適用されます。

- ボタンはフォーム グループに含まれています。
- グループが **右側のパネル** と名前が付けられている、またはグループ名が **SecondaryButtonGroup** で始まる。

![セカンダリ ボタン](media/pfe-styles-second.png)

### <a name="third-group-button"></a>3 番目のグループ ボタン

スタイルは、次の要件が満たされている場合にのみ、3 番目のグループのボタンに適用されます。

- ボタンはフォーム グループに含まれています。
- グループが **左側のパネル** と名前が付けられている、またはグループ名が **ThirdButtonGroup** で始まる。

![3 番目のグループのボタン](media/pfe-styles-third.png)

### <a name="fourth-group-button"></a>4 番目のグループのボタン

スタイルは、次の要件が満たされている場合にのみ、4 番目のグループのボタンに適用されます。

- ボタンはフォーム グループに含まれています。
- グループ名が **FourthButtonGroup** で始まる。

ボタンに以下のプロパティを設定します。

- **ボタン表示**: **TextOnly**。
- **通常のイメージ**: このプロパティは空白にする必要があります。
- **テキスト**: このプロパティを空白にすることはできません。 たとえば、**表示** または **編集** を使用します。
- **幅**: **自動**。
- **高さ**: **自動**。

![4 番目のグループ ボタン](media/pfe-styles-fourth.png)

### <a name="flat-button"></a>フラット ボタン

スタイルは、次の要件が満たされている場合にのみ、フラット ボタンに適用されます。

- ボタンはフォーム グループに含まれています。
- グループ名が **FlatButtonGroup** で始まる。

ボタンに以下のプロパティを設定します。

- **ボタン表示**: **ImageOnly**。
- **通常のイメージ**: このプロパティを空白にすることはできません。 たとえば、**CoffeeScript** を使用します。
- **テキスト**: このプロパティは空白にする必要があります。
- **幅**: **自動**。
- **高さ**: **自動**。

![フラット ボタン](media/pfe-styles-flat-button.png)

## <a name="combo-box"></a>コンボ ボックス

コンボ ボックスは、入力コントロール、入力コントロールをクリアするボタン、および検索を実行するボタンの 3 つのコントロールの組み合わせです。

スタイルは、次の要件が満たされている場合にのみ、コンボ ボックスに適用されます。

- コンボ ボックスはフォーム グループに含まれています。
- グループ名は **Combobox** で始まります。
- グループ内で、最初のコントロールは **AxFormStringControl** です。 このコントロールは現在の値を表示し、ユーザーは必要な値を入力します。
- 2 つ目のコントロールは **CommonButton** コントロールで、名前は **ClearButton** で始まります。 このボタンには、ボタンを表示または非表示にする **enable** プロパティを使用するコードが含まれている必要があります。 たとえば、ユーザーが入力コントロールに情報を入力している間に **クリア** ボタンを表示または非表示にするには、次のコードを使用することができます。

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

    **クリア** ボタンの **clicked** メソッドには次のコードを使用します。

    ```xpp
    public void clicked()
    {
        element.setSerialId('');
        InventSerialId.setFocus(); // set focus back to the input box
    }
    ```

    フォームを **init** メソッドを使用して初期化するときに、入力コントロール **AxFormStringControl** の値を設定します。 値が空白でない場合は、**クリア** ボタンを有効にします。 値が空白の場合は、**クリア** ボタンを無効にします。

- 3 つ目のコントロールは **CommonButton** コントロールで、名前は **SearchButton** で始まります。

次の図は、2 つのコンボ ボックス コントロールを示します。 左側のコンボ ボックスには空のテキスト ボックスがあり、**クリア** ボタンは無効になっています。 右側のコンボ ボックスにはテキスト ボックスにテキストがあり、**クリア** ボタンが有効になっています。

![クリア ボタン付き、またはなしのコンボ ボックス](media/pfe-styles-combo.png)

## <a name="quick-filter"></a>クイック フィルター

クイック フィルター コントロールによって、ページに検索フィールドが追加されます。 次の要件が満たされている場合、クイック フィルターにスタイルを適用できます。

- クイック フィルターはフォーム グループに含まれています。
- グループ名は **SearchInput** で始まります。
- グループ内で、最初のコントロールは **QuickFilter** コントロールです。 (これはユーザーが検索文字列を入力する場所です。)
- 2 つ目のコントロールは **FormStaticTextControl** で、名前は **NumberOfResults** で始まります。 (これはオプションで、検出された品目の数が含まれている場合は表示されます。)
- 3 つ目のコントロールは **CommonButton** コントロールで、名前は **ClearButton** で始まります。

次の図は、2 つのクイック フィルター コントロールを示します。 左側のクイック フィルターは空になっており、結果の数は表示されません。 右側のクイック フィルターには検索文字列が含まれるので、結果の数が表示されます。

![検索文字列を使用した場合および使用しない場合のクイック フィルター コントロールの例](media/pfe-styles-quick-filter.png "検索文字列を使用した場合および使用しない場合のクイック フィルター コントロールの例")


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
