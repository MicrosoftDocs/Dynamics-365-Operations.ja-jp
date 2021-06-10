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
# <a name="create-a-custom-view-in-pos"></a><span data-ttu-id="3a2fd-103">POS でのカスタム ビューの作成</span><span class="sxs-lookup"><span data-stu-id="3a2fd-103">Create a custom view in POS</span></span>

[!include [banner](../../../includes/banner.md)]

<span data-ttu-id="3a2fd-104">このトピックでは、POS でのカスタム ビューの作成方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="3a2fd-104">This topic explains how to create a custom view in POS.</span></span> <span data-ttu-id="3a2fd-105">Retail SDK バージョン 10.0.18 以降に適用されます。</span><span class="sxs-lookup"><span data-stu-id="3a2fd-105">It applies to the Retail SDK version 10.0.18 and later.</span></span>

<span data-ttu-id="3a2fd-106">POS でカスタム ビューを作成すると、POS に新しい機能を追加できます。</span><span class="sxs-lookup"><span data-stu-id="3a2fd-106">Creating a custom view in POS is a great way to add new functionality to POS.</span></span> <span data-ttu-id="3a2fd-107">新しいビューの作成は、POS でさらに多くのシナリオをサポートするシナリオに最適です。</span><span class="sxs-lookup"><span data-stu-id="3a2fd-107">Creating a new view is best in scenarios where you want to support more scenarios in POS.</span></span> <span data-ttu-id="3a2fd-108">カスタム ダイアログは、既存の POS ワークフローを拡張するのに適しています。</span><span class="sxs-lookup"><span data-stu-id="3a2fd-108">A custom dialog is better suited to extending existing POS workflows.</span></span>

<span data-ttu-id="3a2fd-109">POS の新しいビューはすべて **PosApi/Create/Views** モジュールの **CustomViewControllerBase** クラスから拡張されます。これらのビューは、次の抽象メソッドを実装する必要があります。</span><span class="sxs-lookup"><span data-stu-id="3a2fd-109">All new views in POS extend from the **CustomViewControllerBase** class in the **PosApi/Create/Views** module, and they must implement the following abstract methods.</span></span>

+ <span data-ttu-id="3a2fd-110">**onReady** - POS フレームワークは、ページが DOM に追加されると、ビューの **onReady** メソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="3a2fd-110">**onReady** - The POS framework calls the view’s **onReady** method when the page has been added to the DOM.</span></span> <span data-ttu-id="3a2fd-111">このメソッドは、提供された HTML 要素内のビューのレンダリングを担当します。</span><span class="sxs-lookup"><span data-stu-id="3a2fd-111">This method is responsible for rendering the view inside of the provided HTML element.</span></span>
+ <span data-ttu-id="3a2fd-112">**dispose** - POS フレームワークは、ビューが DOM および POS ナビゲーション履歴から削除されたときに、ビューの **dispose** メソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="3a2fd-112">**dispose** - The POS framework calls the view’s **dispose** method when the view is removed from the DOM and the POS navigation history.</span></span> <span data-ttu-id="3a2fd-113">このメソッドは、ビューによって作成されたすべてのリソースをリリースします。</span><span class="sxs-lookup"><span data-stu-id="3a2fd-113">This method should release any resources created by the view.</span></span>

<span data-ttu-id="3a2fd-114">上記の必要なメソッドに加えて、カスタム ビュー コントローラーは以下のページ ライフサイクル メソッドも実装できます。</span><span class="sxs-lookup"><span data-stu-id="3a2fd-114">In addition to the required methods above, a custom view controller can also implement the page lifecycle methods below.</span></span>

+ <span data-ttu-id="3a2fd-115">**onShown** - このメソッドは、ビューが表示されるたびに呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="3a2fd-115">**onShown** - This method is called every time the view is displayed.</span></span>
+ <span data-ttu-id="3a2fd-116">**onHidden** - このメソッドは、ビューが非表示になるたびに呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="3a2fd-116">**onHidden** - This method is called every time the view is hidden.</span></span>

## <a name="configure-the-custom-view-controller"></a><span data-ttu-id="3a2fd-117">カスタム ビュー コントローラーのコンフィギュレーション</span><span class="sxs-lookup"><span data-stu-id="3a2fd-117">Configure the custom view controller</span></span>

<span data-ttu-id="3a2fd-118">**CustomViewControllerBase** クラスは、拡張ビューがページのタイトルや AppBar などの一般的なビューを制御できるようにするオプションのコンフィギュレーション オブジェクトを受け入れます。</span><span class="sxs-lookup"><span data-stu-id="3a2fd-118">The **CustomViewControllerBase** class accepts an optional configuration object that enables extension views to control common view functionality like the title of the page and the AppBar.</span></span> <span data-ttu-id="3a2fd-119">ビューが表示されている場合、コンフィギュレーション オブジェクトで指定されたページ タイトルが POS ヘッダーに表示されます。</span><span class="sxs-lookup"><span data-stu-id="3a2fd-119">The page title specified in the config object is displayed on the POS header when the view is visible.</span></span>

<span data-ttu-id="3a2fd-120">**ICustomViewControllerConfiguration** オブジェクトに指定された値は、**CustomViewControllerBase** クラスの状態フィールドに転送されます。</span><span class="sxs-lookup"><span data-stu-id="3a2fd-120">The values specified in the **ICustomViewControllerConfiguration** object are transferred to the state field in the **CustomViewControllerBase** class.</span></span> <span data-ttu-id="3a2fd-121">一部のデータは、ビューのライフサイクル全体を通じて更新できます。</span><span class="sxs-lookup"><span data-stu-id="3a2fd-121">Some of them can be updated throughout the view's lifecycle.</span></span>

<span data-ttu-id="3a2fd-122">カスタム ビュー コントローラーを構成する方法を次のコード例に示します。</span><span class="sxs-lookup"><span data-stu-id="3a2fd-122">Configuring the custom view controller is shown in the following code example.</span></span> <span data-ttu-id="3a2fd-123">この例は、GitHub リポジトリの [ExampleView.ts ファイル](https://github.com/microsoft/Dynamics365Commerce.InStore/blob/release/9.28/src/PosSample/Pos.Extension/Views/ExampleView.ts)からダウンロードできます。</span><span class="sxs-lookup"><span data-stu-id="3a2fd-123">You can download the example from the [ExampleView.ts file](https://github.com/microsoft/Dynamics365Commerce.InStore/blob/release/9.28/src/PosSample/Pos.Extension/Views/ExampleView.ts) in the GitHub repo.</span></span>

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

## <a name="using-the-appbar"></a><span data-ttu-id="3a2fd-124">AppBar の使用</span><span class="sxs-lookup"><span data-stu-id="3a2fd-124">Using the AppBar</span></span>

<span data-ttu-id="3a2fd-125">**config** オブジェクトには、カスタム ビューが表示されているときに POS AppBar にコマンドを追加するために使用される **commandBar** が含まれています。</span><span class="sxs-lookup"><span data-stu-id="3a2fd-125">The **config** object contains a **commandBar** that is used to add commands the POS AppBar when the custom view is visible.</span></span> <span data-ttu-id="3a2fd-126">コマンド バー コンフィギュレーションには、ビューが表示される際に表示されるコマンド定義のコレクションが含まれています。</span><span class="sxs-lookup"><span data-stu-id="3a2fd-126">The command bar configuration contains a collection of command definitions that are displayed when the view is visible.</span></span> <span data-ttu-id="3a2fd-127">これらのコマンド定義は、最初のコマンドがページの右側から順番に表示されます。</span><span class="sxs-lookup"><span data-stu-id="3a2fd-127">These command definitions are displayed in order with the first command being the furthest right on the page.</span></span>

<span data-ttu-id="3a2fd-128">各コマンド定義は、**PosApi/Create/Views** モジュールからエクスポートされる **ICommandDefinition** インターフェイスを実装する必要があります。</span><span class="sxs-lookup"><span data-stu-id="3a2fd-128">Each command definition must implement the **ICommandDefinition** interface that is exported from the **PosApi/Create/Views** module.</span></span> <span data-ttu-id="3a2fd-129">以下は、コマンド定義のプロパティとメソッドの一覧です。</span><span class="sxs-lookup"><span data-stu-id="3a2fd-129">Below is a list of the properties and methods on the command definition.</span></span>

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

<span data-ttu-id="3a2fd-130">プロパティ</span><span class="sxs-lookup"><span data-stu-id="3a2fd-130">Property</span></span>|<span data-ttu-id="3a2fd-131">説明</span><span class="sxs-lookup"><span data-stu-id="3a2fd-131">Description</span></span>
---|---
<span data-ttu-id="3a2fd-132">実行</span><span class="sxs-lookup"><span data-stu-id="3a2fd-132">execute</span></span> | <span data-ttu-id="3a2fd-133">コマンドが呼び出されると実行されます。</span><span class="sxs-lookup"><span data-stu-id="3a2fd-133">Runs when the command is invoked.</span></span>
<span data-ttu-id="3a2fd-134"> アイコン</span><span class="sxs-lookup"><span data-stu-id="3a2fd-134">icon</span></span> | <span data-ttu-id="3a2fd-135">コマンドに使用するアイコンを定義します。</span><span class="sxs-lookup"><span data-stu-id="3a2fd-135">Defines the icon to be used for the command.</span></span>
<span data-ttu-id="3a2fd-136">名前</span><span class="sxs-lookup"><span data-stu-id="3a2fd-136">name</span></span> | <span data-ttu-id="3a2fd-137">コマンドの名前を定義します。</span><span class="sxs-lookup"><span data-stu-id="3a2fd-137">Defines the command’s name.</span></span> <span data-ttu-id="3a2fd-138">使用されるビュー内で一意である必要があります。</span><span class="sxs-lookup"><span data-stu-id="3a2fd-138">Must be unique within the view where it is used.</span></span>
<span data-ttu-id="3a2fd-139">ラベル</span><span class="sxs-lookup"><span data-stu-id="3a2fd-139">label</span></span> | <span data-ttu-id="3a2fd-140">コマンドの AppBar にラベルを付け、ローカライズする必要があります。</span><span class="sxs-lookup"><span data-stu-id="3a2fd-140">Label on the AppBar for the command and should be localized.</span></span>
<span data-ttu-id="3a2fd-141">canExecute</span><span class="sxs-lookup"><span data-stu-id="3a2fd-141">canExecute</span></span> | <span data-ttu-id="3a2fd-142">コマンドを最初に作成するときに有効にするかどうかを指定します。</span><span class="sxs-lookup"><span data-stu-id="3a2fd-142">Specifies if the command should be enabled when it is first created.</span></span>
<span data-ttu-id="3a2fd-143">isVisible</span><span class="sxs-lookup"><span data-stu-id="3a2fd-143">isVisible</span></span> | <span data-ttu-id="3a2fd-144">コマンドを最初に作成するときに表示するかどうかを指定します。</span><span class="sxs-lookup"><span data-stu-id="3a2fd-144">Specifies if the command should be visible when it is first created.</span></span>

## <a name="changing-a-commands-visibility-and-enabling-and-disabling-commands"></a><span data-ttu-id="3a2fd-145">コマンドの可視性の変更、およびコマンドの有効化と無効化</span><span class="sxs-lookup"><span data-stu-id="3a2fd-145">Changing a command’s visibility and enabling and disabling commands</span></span>

<span data-ttu-id="3a2fd-146">コマンドがコンストラクターで作成された後、コマンドの **isProcessing** および **canExecute** フィールドをビュー内で更新でき、変更により、UI でのコマンドの有効化と可視性のステータスが制御されます。</span><span class="sxs-lookup"><span data-stu-id="3a2fd-146">After the commands are created in the constructor, the **isProcessing** and **canExecute** fields on the commands can be updated within the view and the changes will control the enabled and visibility status of the commands on the UI.</span></span>

<span data-ttu-id="3a2fd-147">次のコード例は、データ リストの **SelectionChanged** イベントを使用して、**編集** および **削除** コマンドを有効にする方法を示しています。</span><span class="sxs-lookup"><span data-stu-id="3a2fd-147">The following code example shows how to use the data list's **SelectionChanged** event to enable the **Edit** and **Delete** commands.</span></span>

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
