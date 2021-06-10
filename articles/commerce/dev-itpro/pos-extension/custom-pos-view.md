---
title: POS でのカスタム ビューの作成
description: このトピックでは、POS でのカスタム ビューの作成方法について説明します。
author: mugunthanm
ms.date: 04/13/2021
ms.topic: article
audience: Developer
ms.reviewer: rhaertle
ms.search.region: Global
ms.author: mumani
ms.search.validFrom: 04-13-2020
ms.dyn365.ops.version: AX 10.0.18
ms.openlocfilehash: b8b6c770a7f1d8e1eff3789a67e2ce07bcca24bc
ms.sourcegitcommit: 4c880b152e81350f023b944c2ab13e60498e2c7b
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/25/2021
ms.locfileid: "6093898"
---
# <a name="create-a-custom-view-in-pos"></a>POS でのカスタム ビューの作成

[!include [banner](../../../includes/banner.md)]

このトピックでは、POS でのカスタム ビューの作成方法について説明します。 Retail SDK バージョン 10.0.18 以降に適用されます。

POS でカスタム ビューを作成すると、POS に新しい機能を追加できます。 新しいビューの作成は、POS でさらに多くのシナリオをサポートするシナリオに最適です。 カスタム ダイアログは、既存の POS ワークフローを拡張するのに適しています。

POS の新しいビューはすべて **PosApi/Create/Views** モジュールの **CustomViewControllerBase** クラスから拡張されます。これらのビューは、次の抽象メソッドを実装する必要があります。

+ **onReady** - POS フレームワークは、ページが DOM に追加されると、ビューの **onReady** メソッドを呼び出します。 このメソッドは、提供された HTML 要素内のビューのレンダリングを担当します。
+ **dispose** - POS フレームワークは、ビューが DOM および POS ナビゲーション履歴から削除されたときに、ビューの **dispose** メソッドを呼び出します。 このメソッドは、ビューによって作成されたすべてのリソースをリリースします。

上記の必要なメソッドに加えて、カスタム ビュー コントローラーは以下のページ ライフサイクル メソッドも実装できます。

+ **onShown** - このメソッドは、ビューが表示されるたびに呼び出されます。
+ **onHidden** - このメソッドは、ビューが非表示になるたびに呼び出されます。

## <a name="configure-the-custom-view-controller"></a>カスタム ビュー コントローラーのコンフィギュレーション

**CustomViewControllerBase** クラスは、拡張ビューがページのタイトルや AppBar などの一般的なビューを制御できるようにするオプションのコンフィギュレーション オブジェクトを受け入れます。 ビューが表示されている場合、コンフィギュレーション オブジェクトで指定されたページ タイトルが POS ヘッダーに表示されます。

**ICustomViewControllerConfiguration** オブジェクトに指定された値は、**CustomViewControllerBase** クラスの状態フィールドに転送されます。 一部のデータは、ビューのライフサイクル全体を通じて更新できます。

カスタム ビュー コントローラーを構成する方法を次のコード例に示します。 この例は、GitHub リポジトリの [ExampleView.ts ファイル](https://github.com/microsoft/Dynamics365Commerce.InStore/blob/release/9.28/src/PosSample/Pos.Extension/Views/ExampleView.ts)からダウンロードできます。

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

## <a name="using-the-appbar"></a>AppBar の使用

**config** オブジェクトには、カスタム ビューが表示されているときに POS AppBar にコマンドを追加するために使用される **commandBar** が含まれています。 コマンド バー コンフィギュレーションには、ビューが表示される際に表示されるコマンド定義のコレクションが含まれています。 これらのコマンド定義は、最初のコマンドがページの右側から順番に表示されます。

各コマンド定義は、**PosApi/Create/Views** モジュールからエクスポートされる **ICommandDefinition** インターフェイスを実装する必要があります。 以下は、コマンド定義のプロパティとメソッドの一覧です。

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

プロパティ|説明
---|---
実行 | コマンドが呼び出されると実行されます。
 アイコン | コマンドに使用するアイコンを定義します。
名前 | コマンドの名前を定義します。 使用されるビュー内で一意である必要があります。
ラベル | コマンドの AppBar にラベルを付け、ローカライズする必要があります。
canExecute | コマンドを最初に作成するときに有効にするかどうかを指定します。
isVisible | コマンドを最初に作成するときに表示するかどうかを指定します。

## <a name="changing-a-commands-visibility-and-enabling-and-disabling-commands"></a>コマンドの可視性の変更、およびコマンドの有効化と無効化

コマンドがコンストラクターで作成された後、コマンドの **isProcessing** および **canExecute** フィールドをビュー内で更新でき、変更により、UI でのコマンドの有効化と可視性のステータスが制御されます。

次のコード例は、データ リストの **SelectionChanged** イベントを使用して、**編集** および **削除** コマンドを有効にする方法を示しています。

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
