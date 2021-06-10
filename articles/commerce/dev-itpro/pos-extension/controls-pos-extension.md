---
title: 拡張機能での POS コントロールの使用
description: このトピックでは、拡張機能で POS コントロールを使用する方法について説明します。
author: mugunthanm
ms.date: 04/13/2021
ms.topic: article
audience: Developer
ms.reviewer: rhaertle
ms.search.region: Global
ms.author: mumani
ms.search.validFrom: 04-13-2020
ms.dyn365.ops.version: AX 10.0.18
ms.openlocfilehash: 6a156754ac661923de963a3d5fd9f88483392de1
ms.sourcegitcommit: d84329f903d359ae042e8c0a4594982a7e06756f
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/06/2021
ms.locfileid: "5984296"
---
# <a name="use-pos-controls-in-extensions"></a>拡張機能での POS コントロールの使用

[!include [banner](../../../includes/banner.md)]

このトピックでは、拡張機能で POS コントロールを使用する方法について説明します。 Retail SDK バージョン 10.0.18 以降に適用されます。

**PosApi** ライブラリは、一般的な POS コントロールへのアクセスを提供することで、拡張機能 UI と他の POS の間で一貫した外観と権限を提供します。 これらのコントロールは、**PosApi/消費/コントロール** モジュールのインターフェイスとして使用できます。 これらのコントロールのインスタンスは、拡張機能コンテキストで提供された **ControlFactory** を使用して作成できます。 UI 拡張機能クラスには、ビュー、ダイアログおよびカスタム コントロールが含まれます。

次のコード例では、**ControlFactory** を使用してカスタム ビュー コントローラの **onReady** 関数で **DataList** コントロールを作成する方法を示します。

```Javascript
public onReady(element: HTMLElement): void {
    // DataList
    let dataListOptions: IDataListOptions<Entities.ExampleEntity> = {
        interactionMode: DataListInteractionMode.SingleSelect,
        data: this.viewModel.loadedData,
        columns: [
            {
                title: this.context.resources.getString("string_1001"), // Int data
                ratio: 40, collapseOrder: 1, minWidth: 100,
                computeValue: (data: Entities.ExampleEntity): string => data.IntData.toString()
            },
            {
                title: this.context.resources.getString("string_1002"), // String data
                ratio: 60, collapseOrder: 2, minWidth: 100,
                computeValue: (data: Entities.ExampleEntity): string => data.StringData
            }
        ]
    };

    let dataListRootElem: HTMLDivElement = element.querySelector("#exampleListView") as HTMLDivElement;
    this.dataList = this.context.controlFactory.create(this.context.logger.getNewCorrelationId(), "DataList", dataListOptions, dataListRootElem);

    this.dataList.addEventListener("SelectionChanged", (eventData: { items: Entities.ExampleEntity[] }) => {
        this.viewModel.seletionChanged(eventData.items);

        // Update the command states to reflect the current selection state.
        this.state.commandBar.commands.forEach(
            command => command.canExecute = (
                ["Create", "PingTest"].some(name => name == command.name) ||
                this.viewModel.isItemSelected()
            )
        );
    });

    this.state.isProcessing = true;
    this.viewModel.load().then((): void => {
        // Initialize the data list with what the view model loaded
        this.dataList.data = this.viewModel.loadedData;
        this.state.isProcessing = false;
    });
}
```

POS コントロールおよびコントロール ファクトリのより多くの使用例は、GitHub リポジトリの [PosSample フォルダ](https://github.com/microsoft/Dynamics365Commerce.InStore/tree/release/9.28/src/PosSample) を参照してください。

## <a name="pos-controls"></a>POS コントロール

サポートされているコントロールは次のとおりです。

| 状態 | インターフェイス | 説明 |
|---------|-----------|-------------|
| データ リスト | IDataList、IPaginatedDataList | データ リストは、POS 全体で情報行を表示するために使用される応答可能なリスト コントロールです。 |
| 日付の選択  | IDatePicker | POSで使用される日付の選択 コントロール。 |
| メニュー         | IMenu | POS でコンテキスト情報を表示するために使用されるメニュー コントロールです。 |
| Pad 番号   | IAlphanumericNumPad、ICurrencyNumPad、INumericNumPad、ITransactionNumPad | 番号パッドは、さまざまな動作および入力形式により POS 全体で使用されます。<ul><li>英数字のテンキー: 英数字による入力を使用できます。</li><li>通貨のテンキー: 金銭的価値を受け入れます。</li><li>数値テンキー: 数値のみを使用します。</li><li>トランザクションのテンキー: 品目の ID または数量を受け入れます。 通常はトランザクション シナリオで使用されます。</li></ul> |
| 時刻のピッカー | ITimePicker | POS で使用される時刻の選択コントロール。 |
| 切り替え | IToggle | POS で使用される切り替えコントロールです。 |

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
