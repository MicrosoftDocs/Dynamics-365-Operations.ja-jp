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
# <a name="use-pos-controls-in-extensions"></a><span data-ttu-id="9ac39-103">拡張機能での POS コントロールの使用</span><span class="sxs-lookup"><span data-stu-id="9ac39-103">Use POS controls in extensions</span></span>

[!include [banner](../../../includes/banner.md)]

<span data-ttu-id="9ac39-104">このトピックでは、拡張機能で POS コントロールを使用する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="9ac39-104">This topic explains how to use POS controls in extensions.</span></span> <span data-ttu-id="9ac39-105">Retail SDK バージョン 10.0.18 以降に適用されます。</span><span class="sxs-lookup"><span data-stu-id="9ac39-105">It applies to the Retail SDK version 10.0.18 and later.</span></span>

<span data-ttu-id="9ac39-106">**PosApi** ライブラリは、一般的な POS コントロールへのアクセスを提供することで、拡張機能 UI と他の POS の間で一貫した外観と権限を提供します。</span><span class="sxs-lookup"><span data-stu-id="9ac39-106">The **PosApi** library provides a consistent look and feel between the extension UI and the rest of POS by providing access to common POS controls.</span></span> <span data-ttu-id="9ac39-107">これらのコントロールは、**PosApi/消費/コントロール** モジュールのインターフェイスとして使用できます。</span><span class="sxs-lookup"><span data-stu-id="9ac39-107">These controls are available as interfaces in the **PosApi/Consume/Controls** module.</span></span> <span data-ttu-id="9ac39-108">これらのコントロールのインスタンスは、拡張機能コンテキストで提供された **ControlFactory** を使用して作成できます。</span><span class="sxs-lookup"><span data-stu-id="9ac39-108">Instances of these controls can be created using the **ControlFactory** provided in the extension context.</span></span> <span data-ttu-id="9ac39-109">UI 拡張機能クラスには、ビュー、ダイアログおよびカスタム コントロールが含まれます。</span><span class="sxs-lookup"><span data-stu-id="9ac39-109">The UI extension classes include views, dialogs, and custom controls.</span></span>

<span data-ttu-id="9ac39-110">次のコード例では、**ControlFactory** を使用してカスタム ビュー コントローラの **onReady** 関数で **DataList** コントロールを作成する方法を示します。</span><span class="sxs-lookup"><span data-stu-id="9ac39-110">The following code example shows how to use the **ControlFactory** to create a **DataList** control in the **onReady** function of a custom view controller.</span></span>

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

<span data-ttu-id="9ac39-111">POS コントロールおよびコントロール ファクトリのより多くの使用例は、GitHub リポジトリの [PosSample フォルダ](https://github.com/microsoft/Dynamics365Commerce.InStore/tree/release/9.28/src/PosSample) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="9ac39-111">More examples of how to use POS controls and the control factory can be found in the [PosSample folder](https://github.com/microsoft/Dynamics365Commerce.InStore/tree/release/9.28/src/PosSample) of the GitHub repo.</span></span>

## <a name="pos-controls"></a><span data-ttu-id="9ac39-112">POS コントロール</span><span class="sxs-lookup"><span data-stu-id="9ac39-112">POS controls</span></span>

<span data-ttu-id="9ac39-113">サポートされているコントロールは次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="9ac39-113">The following controls are supported.</span></span>

| <span data-ttu-id="9ac39-114">状態</span><span class="sxs-lookup"><span data-stu-id="9ac39-114">Control</span></span> | <span data-ttu-id="9ac39-115">インターフェイス</span><span class="sxs-lookup"><span data-stu-id="9ac39-115">Interfaces</span></span> | <span data-ttu-id="9ac39-116">説明</span><span class="sxs-lookup"><span data-stu-id="9ac39-116">Description</span></span> |
|---------|-----------|-------------|
| <span data-ttu-id="9ac39-117">データ リスト</span><span class="sxs-lookup"><span data-stu-id="9ac39-117">Data list</span></span> | <span data-ttu-id="9ac39-118">IDataList、IPaginatedDataList</span><span class="sxs-lookup"><span data-stu-id="9ac39-118">IDataList, IPaginatedDataList</span></span> | <span data-ttu-id="9ac39-119">データ リストは、POS 全体で情報行を表示するために使用される応答可能なリスト コントロールです。</span><span class="sxs-lookup"><span data-stu-id="9ac39-119">The data list is a responsive list control used throughout POS to display rows of information.</span></span> |
| <span data-ttu-id="9ac39-120">日付の選択</span><span class="sxs-lookup"><span data-stu-id="9ac39-120">Date picker</span></span>  | <span data-ttu-id="9ac39-121">IDatePicker</span><span class="sxs-lookup"><span data-stu-id="9ac39-121">IDatePicker</span></span> | <span data-ttu-id="9ac39-122">POSで使用される日付の選択 コントロール。</span><span class="sxs-lookup"><span data-stu-id="9ac39-122">The date picker control used in POS.</span></span> |
| <span data-ttu-id="9ac39-123">メニュー</span><span class="sxs-lookup"><span data-stu-id="9ac39-123">Menu</span></span>         | <span data-ttu-id="9ac39-124">IMenu</span><span class="sxs-lookup"><span data-stu-id="9ac39-124">IMenu</span></span> | <span data-ttu-id="9ac39-125">POS でコンテキスト情報を表示するために使用されるメニュー コントロールです。</span><span class="sxs-lookup"><span data-stu-id="9ac39-125">The menu control used in POS to display contextual information.</span></span> |
| <span data-ttu-id="9ac39-126">Pad 番号</span><span class="sxs-lookup"><span data-stu-id="9ac39-126">Number Pad</span></span>   | <span data-ttu-id="9ac39-127">IAlphanumericNumPad、ICurrencyNumPad、INumericNumPad、ITransactionNumPad</span><span class="sxs-lookup"><span data-stu-id="9ac39-127">IAlphanumericNumPad, ICurrencyNumPad, INumericNumPad, ITransactionNumPad</span></span> | <span data-ttu-id="9ac39-128">番号パッドは、さまざまな動作および入力形式により POS 全体で使用されます。</span><span class="sxs-lookup"><span data-stu-id="9ac39-128">Number pads are used throughout POS with various behaviors and input formatting.</span></span><ul><li><span data-ttu-id="9ac39-129">英数字のテンキー: 英数字による入力を使用できます。</span><span class="sxs-lookup"><span data-stu-id="9ac39-129">Alphanumeric numpad: Accepts alphanumeric input.</span></span></li><li><span data-ttu-id="9ac39-130">通貨のテンキー: 金銭的価値を受け入れます。</span><span class="sxs-lookup"><span data-stu-id="9ac39-130">Currency numpad: Accepts monetary values.</span></span></li><li><span data-ttu-id="9ac39-131">数値テンキー: 数値のみを使用します。</span><span class="sxs-lookup"><span data-stu-id="9ac39-131">Numeric numpad: Accepts only numeric values.</span></span></li><li><span data-ttu-id="9ac39-132">トランザクションのテンキー: 品目の ID または数量を受け入れます。</span><span class="sxs-lookup"><span data-stu-id="9ac39-132">Transaction numpad: Accepts an item identifier or quantity.</span></span> <span data-ttu-id="9ac39-133">通常はトランザクション シナリオで使用されます。</span><span class="sxs-lookup"><span data-stu-id="9ac39-133">Typically used in a transaction scenario.</span></span></li></ul> |
| <span data-ttu-id="9ac39-134">時刻のピッカー</span><span class="sxs-lookup"><span data-stu-id="9ac39-134">Time Picker</span></span> | <span data-ttu-id="9ac39-135">ITimePicker</span><span class="sxs-lookup"><span data-stu-id="9ac39-135">ITimePicker</span></span> | <span data-ttu-id="9ac39-136">POS で使用される時刻の選択コントロール。</span><span class="sxs-lookup"><span data-stu-id="9ac39-136">The time picker control used in POS.</span></span> |
| <span data-ttu-id="9ac39-137">切り替え</span><span class="sxs-lookup"><span data-stu-id="9ac39-137">Toggle</span></span> | <span data-ttu-id="9ac39-138">IToggle</span><span class="sxs-lookup"><span data-stu-id="9ac39-138">IToggle</span></span> | <span data-ttu-id="9ac39-139">POS で使用される切り替えコントロールです。</span><span class="sxs-lookup"><span data-stu-id="9ac39-139">The toggle switch control used in POS.</span></span> |

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
