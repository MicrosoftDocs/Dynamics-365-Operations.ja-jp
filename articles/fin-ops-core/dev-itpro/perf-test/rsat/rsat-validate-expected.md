---
title: 予測値を検証する
description: このトピックでは、Regression Suite Automation を使用して予測値を検証する方法を示します。
author: FrankDahl
ms.date: 01/15/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Developer
ms.reviewer: rhaertle
ms.custom: 21631
ms.search.region: Global
ms.author: fdahl
ms.search.validFrom: 2019-08-01
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: b04eac616bcfb780ca9ff0b2943bc635da41fc77
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/31/2021
ms.locfileid: "5745153"
---
# <a name="validate-expected-values"></a><span data-ttu-id="2661a-103">予測値を検証する</span><span class="sxs-lookup"><span data-stu-id="2661a-103">Validate expected values</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="2661a-104">テスト ケースの重要なコンポーネントに、予期値の検証があります。</span><span class="sxs-lookup"><span data-stu-id="2661a-104">An important component of a test case is validation of expected values.</span></span> <span data-ttu-id="2661a-105">タスク レコーダーを使用するテスト ケースの作成時に検証パラメーターを定義できます。</span><span class="sxs-lookup"><span data-stu-id="2661a-105">You can define validation parameters during the authoring of your test cases using Task Recorder.</span></span> <span data-ttu-id="2661a-106">記録中にコントロールを右クリックし、**タスク レコーダー > 検証** メニューの **現在の値** を選択します。</span><span class="sxs-lookup"><span data-stu-id="2661a-106">While recording, right-click on a control and select **CurrentValue** under the **Task Recorder > Validate** menu.</span></span> <span data-ttu-id="2661a-107">このアクションは、Regression Suite Automation Tool と共に使用できる検証手順になります。</span><span class="sxs-lookup"><span data-stu-id="2661a-107">This action becomes a validation step that you can use with the Regression suite automation tool.</span></span> <span data-ttu-id="2661a-108">このコントロール値は、自動的に生成された Excel パラメーター ファイルの検証変数になります。</span><span class="sxs-lookup"><span data-stu-id="2661a-108">The control value will become a validation variable in the automatically generated Excel parameters file.</span></span> <span data-ttu-id="2661a-109">メニュー項目を次の図に示します。</span><span class="sxs-lookup"><span data-stu-id="2661a-109">The menu item is shown in the following image.</span></span>

![メニュー項目の検証](media/validate-test-case.png)

<span data-ttu-id="2661a-111">タスク の作成方法についての詳細は、[タスク レコーダー リソース](../../user-interface/task-recorder.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="2661a-111">For more information about how to create task recordings, see [Task recorder resources](../../user-interface/task-recorder.md).</span></span>

<span data-ttu-id="2661a-112">RSAT がテスト ケースの Excel パラメーター ファイルを生成すると、次の図に示すように検証ステップが追加されます。</span><span class="sxs-lookup"><span data-stu-id="2661a-112">When RSAT generates the Excel parameter file for a test case, validation steps are added as shown in the image below.</span></span> <span data-ttu-id="2661a-113">テスト ケースの実行中に使用する予測値を入力できます。</span><span class="sxs-lookup"><span data-stu-id="2661a-113">You can enter the expected value to use during execution of the test case.</span></span>

![変数の検証](media/rsat-validate-variables.png)

## <a name="validate-expected-values-using-operators"></a><span data-ttu-id="2661a-115">演算子を使用して予測値を検証する</span><span class="sxs-lookup"><span data-stu-id="2661a-115">Validate expected values using operators</span></span>

<span data-ttu-id="2661a-116">検証ステップで演算子を使用して、指定された値より変数が等しい、より小さい、または大きいことを検証することもできます。</span><span class="sxs-lookup"><span data-stu-id="2661a-116">You can also use operators in validation steps to validate that a variable is not equal, less than, or greater than a specified value.</span></span> <span data-ttu-id="2661a-117">この機能を使用するには、**設定** タブを開いて、**オプション** タブを選択します。**検証に演算子を使用する** という設定をオンにします。</span><span class="sxs-lookup"><span data-stu-id="2661a-117">To use this feature, open the **Settings** tab and select the **Optional** tab. Turn on the setting named **Use operators for validation**.</span></span> <span data-ttu-id="2661a-118">このオプションは、RSAT バージョン 1.210 で使用できます。</span><span class="sxs-lookup"><span data-stu-id="2661a-118">This option is available as of RSAT version 1.210.</span></span> <span data-ttu-id="2661a-119">以前のバージョンのツールを使用していた場合は、この機能を利用するために新しい Excel パラメーター ファイルを再生成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="2661a-119">If you have been using an older version of the tool, you must regenerate new Excel parameter files to take advantage of this functionality.</span></span> <span data-ttu-id="2661a-120">Excel ファイルに、次の図に示すような新しい **オペレーター** フィールドが表示されます。</span><span class="sxs-lookup"><span data-stu-id="2661a-120">In the Excel file, a new **Operator** field will appear, as shown in the following image.</span></span>

![以前のバージョンの Excel での検証](media/validate-test-case-example.png)

## <a name="validate-the-state-of-a-control"></a><span data-ttu-id="2661a-122">コントロールの状態の検証</span><span class="sxs-lookup"><span data-stu-id="2661a-122">Validate the state of a control</span></span>

<span data-ttu-id="2661a-123">テスト ケースを記録する場合、タスク レコーダーは、次の追加の検証アクションをサポートします。</span><span class="sxs-lookup"><span data-stu-id="2661a-123">When recording test cases, Task Recorder supports additional validation action:</span></span>

+ <span data-ttu-id="2661a-124">コントロールが有効か無効かを検証します。</span><span class="sxs-lookup"><span data-stu-id="2661a-124">Validate whether a control is enabled or disabled.</span></span>
+ <span data-ttu-id="2661a-125">コントロールが編集可能か読み取り専用かを検証します。</span><span class="sxs-lookup"><span data-stu-id="2661a-125">Validate whether a control is editable or read-only.</span></span>

<span data-ttu-id="2661a-126">この検証を活用するには、10.0.13 (またはそれ以降) および RSAT 2.0 (またはそれ以降) で実行されている Finance and Operationsアプリを使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="2661a-126">To take advantage of this validation, you need to be use a Finance and Operations app running on 10.0.13 (or newer) and RSAT 2.0 (or newer).</span></span> <span data-ttu-id="2661a-127">詳細については、[検証](../../user-interface/task-recorder.md#validate)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="2661a-127">For more information, see [Validate](../../user-interface/task-recorder.md#validate).</span></span>


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]