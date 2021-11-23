---
title: POS でのカスタム ビューの作成
description: このトピックでは、販売時点管理 (POS) でカスタマイズ ビューの作成方法について説明します。
author: mugunthanm
ms.date: 04/13/2021
ms.topic: article
audience: Developer
ms.reviewer: tfehr
ms.search.region: Global
ms.author: mumani
ms.search.validFrom: 04-13-2020
ms.dyn365.ops.version: AX 10.0.18
ms.openlocfilehash: 403a9b0779e9ffc7acdb2c9ba7ef75a9b0d02730
ms.sourcegitcommit: 9acfb9ddba9582751f53501b82a7e9e60702a613
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/10/2021
ms.locfileid: "7781572"
---
# <a name="create-a-custom-view-in-pos"></a>POS でのカスタム ビューの作成

[!include [banner](../../../includes/banner.md)]

このトピックでは、販売時点管理 (POS) でカスタマイズ ビューの作成方法について説明します。 Retail ソフトウェア開発キット (SDK) バージョン 10.0.18 以降に適用されます。

POS のカスタム ビューでは、POS に新しい機能を追加できます。 このアプローチは、POS でさらに多くのシナリオをサポートするシナリオに最適に機能します。 既存の POS ワークフローを拡張する場合は、カスタム ダイアログ ボックスの方が優れた方法です。

POS の新しいビューはすべて **PosApi/Create/Views** モジュールの **CustomViewControllerBase** クラスから拡張され、これらのビューは、次の抽象メソッドを実装する必要があります:

+ **onReady** - POS フレームワークは、ページが Document Object Model (DOM) に追加されると、ビューの **onReady** メソッドを呼び出します。 このメソッドは、提供された HTML 要素内のビューのレンダリングを担当します。
+ **dispose** – POS フレームワークは、ビューが DOM および POS ナビゲーション履歴から削除されたときに、ビューの **dispose** メソッドを呼び出します。 このメソッドは、ビューを作成したすべてのリソースをリリースします。

先行の必要な抽象メソッドに加えて、カスタム ビュー コントローラーは以下のページ ライフサイクル メソッドも実装できます。

+ **onShown** – このメソッドは、ビューが表示されるたびに呼び出されます。
+ **onHidden** – このメソッドは、ビューが非表示になるたびに呼び出されます。

## <a name="configuring-the-custom-view-controller"></a>カスタム ビュー コントローラーのコンフィギュレーション

**CustomViewControllerBase** クラスは、拡張ビューがページのタイトルやアプリ バーなどの一般的なビューを制御できるようにするオプションのコンフィギュレーション オブジェクトを受け入れます。 ビューが表示されている場合、コンフィギュレーション オブジェクトで指定されたページ タイトルが POS ヘッダーに表示されます。

**ICustomViewControllerConfiguration** オブジェクトに指定された値は、**CustomViewControllerBase** クラスの **状態** フィールドに転送されます。 一部の値は、ビューのライフサイクル全体を通じて更新できます。

以下の例では、カスタム ビュー コントローラーの構成が表示されます。 この例は、GitHub リポジトリ (repo) の [ExampleView.ts ファイル](https://github.com/microsoft/Dynamics365Commerce.InStore/blob/release/9.28/src/PosSample/Pos.Extension/Views/ExampleView.ts) からダウンロードできます。

```TypeScript
export default class ExampleView extends Views.CustomViewControllerBase {
    constructor(context: Views.ICustomViewControllerContext) {
        let config: Views.ICustomViewControllerConfiguration = {
            title: context.resources.getString("string_0001"),
            commandBar: {
                commands: [
                    {
                        name: "Create",
                        label: context.resources.getString("string_2001"),
                        icon: Views.Icons.Add,
                        isVisible: true,
                        canExecute: true,
                        execute: (args: Views.CustomViewControllerExecuteCommandArgs): void => {
                            this.createExampleEntity().then((entityCreated) => {
                                if (entityCreated) {
                                    // Re-load the list, since the underlying data was amended
                                    this.dataList.data = this.viewModel.loadedData;
                                }
                            });
                        }
                    },
                    {
                        name: "Edit",
                        label: context.resources.getString("string_2002"),
                        icon: Views.Icons.Edit,
                        isVisible: true,
                        canExecute: false,
                        execute: (args: Views.CustomViewControllerExecuteCommandArgs): void => {
                            this.state.isProcessing = true;
                            this.editExampleEntity().then((editsMade) => {
                                if (editsMade) {
                                    // Re-load the list since the underlying data changed
                                    this.dataList.data = this.viewModel.loadedData;
                                }
                                this.state.isProcessing = false;
                            });
                        }
                    },
                    {
                        name: "Delete",
                        label: context.resources.getString("string_1006"),
                        icon: Views.Icons.Delete,
                        isVisible: true,
                        canExecute: false,
                        execute: (args: Views.CustomViewControllerExecuteCommandArgs): void => {
                            this.state.isProcessing = true;
                            this.deleteExampleEntity().then(() => {
                                // Re-load the list, since the data has changed
                                this.dataList.data = this.viewModel.loadedData;
                                this.state.isProcessing = false;
                            });
                        }
                    },
                    {
                        name: "PingTest",
                        label: context.resources.getString("string_3001"),
                        icon: Views.Icons.LightningBolt,
                        isVisible: true,
                        canExecute: true,
                        execute: (args: Views.CustomViewControllerExecuteCommandArgs): void => {
                            this.state.isProcessing = true;
                            setTimeout(() => {
                                this.state.isProcessing = false;
                            }, 100);
                        }
                    }
                ]
            }
        };
        super(context, config);
    }
}
```

## <a name="using-the-app-bar"></a>アプリ バーの使用

**config** オブジェクトには、カスタム ビューが表示されているときに POS アプリ バー にコマンドを追加するために使用される **commandBar** 構成が含まれています。 **commandBar** コンフィギュレーションには、ビューが表示される際に表示されるコマンド定義のコレクションが含まれています。 これらのコマンド定義は、順番に表示されます: 最初のコマンドが右側のページに最も遠いです。

各コマンド定義は、**PosApi/Create/Views** モジュールからエクスポートされる **ICommandDefinition** インターフェイスを実装する必要があります。 こちらはコマンド定義のプロパティとメソッドの一覧です。

```TypeScript
export interface ICommandDefinition extends Commerce.Extensibility.ICommandDefinition {
    readonly execute: (args: CustomViewControllerExecuteCommandArgs) => void;
    readonly icon: Commerce.Framework.UI.IconName;
    readonly name: string;
    readonly label: string;
    readonly canExecute: boolean;
    readonly isVisible: boolean;
}
```

| プロパティ | 説明 |
|---|---|
| 実行 | コマンドが呼び出されるとこのフィールドが実行されます。 |
|  アイコン | このフィールドでは、コマンドに使用されるアイコンを定義します。 |
| 名前 | このフィールドではコマンドの名前を定義します。 この名前は使用されるビュー内で一意である必要があります。 |
| ラベル | このフィールドでは、アプリ バーでコマンドに使用されるラベルを定義します。 このラベルはローカライズする必要があります。 |
| canExecute | このフィールドはコマンドを最初に作成するときに有効にするかどうかを指定します。 |
| isVisible | このフィールドはコマンドを最初に作成するときに表示されるかどうかを指定します。 |

## <a name="changing-a-commands-visibility-and-enabling-and-disabling-commands"></a>コマンドの可視性の変更、およびコマンドの有効化と無効化

コマンドがコンストラクターで作成された後、**isProcessing** および **canExecute** フィールドはビュー内で更新できます。 これらの更新によって、コマンドが有効かユーザー インターフェイス (UI) に有効で表示されるか制御されます。

次の例は、データ リストの **SelectionChanged** イベントを使用して、**編集** および **削除** コマンドを有効にする方法を示しています。

```TypeScript
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
        this.state.commandBar.commands.forEach((command) => {
            if (command.name === "Edit" || command.name === "Delete") {
                command.canExecute = eventData.items.length;
            }
        });
    });
}
```

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
