---
title: 予測値を検証する
description: このトピックでは、Regression Suite Automation を使用して予測値を検証する方法を示します。
author: robadawy
manager: AnnBe
ms.date: 08/01/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Developer
ms.reviewer: rhaertle
ms.search.scope: Operations
ms.custom: 21631
ms.search.region: Global
ms.author: robadawy
ms.search.validFrom: 2019-08-01
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 5f6f586dc4f5dc908c5658c0191fb98f356db7f1
ms.sourcegitcommit: 57bc7e17682e2edb5e1766496b7a22f4621819dd
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/18/2019
ms.locfileid: "2812035"
---
# <a name="validate-expected-values"></a><span data-ttu-id="59cdb-103">予測値を検証する</span><span class="sxs-lookup"><span data-stu-id="59cdb-103">Validate expected values</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="59cdb-104">テスト ケースの重要なコンポーネントに、予期値の検証があります。</span><span class="sxs-lookup"><span data-stu-id="59cdb-104">An important component of a test case is validation of expected values.</span></span> <span data-ttu-id="59cdb-105">タスク レコーダーを使用するテスト ケースの作成時に検証パラメーターを定義できます。</span><span class="sxs-lookup"><span data-stu-id="59cdb-105">You can define validation parameters during the authoring of your test cases using Task Recorder.</span></span> <span data-ttu-id="59cdb-106">記録中にコントロールを右クリックし、**タスク レコーダー > 検証** メニューの **現在の値** を選択します。</span><span class="sxs-lookup"><span data-stu-id="59cdb-106">While recording, right-click on a control and select **CurrentValue** under the **Task Recorder > Validate** menu.</span></span> <span data-ttu-id="59cdb-107">このアクションは、Regression Suite Automation Tool と共に使用できる検証手順になります。</span><span class="sxs-lookup"><span data-stu-id="59cdb-107">This action becomes a validation step that you can use with the Regression suite automation tool.</span></span> <span data-ttu-id="59cdb-108">このコントロール値は、自動的に生成された Excel パラメーター ファイルの検証変数になります。</span><span class="sxs-lookup"><span data-stu-id="59cdb-108">The control value will become a validation variable in the automatically generated Excel parameters file.</span></span> <span data-ttu-id="59cdb-109">メニュー項目を次の図に示します。</span><span class="sxs-lookup"><span data-stu-id="59cdb-109">The menu item is shown in the following image.</span></span>

![メニュー項目の検証](media/validate-test-case.png)
 
<span data-ttu-id="59cdb-111">タスク の作成方法についての詳細は、[タスク レコーダー リソース](../../user-interface/task-recorder.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="59cdb-111">For more information about how to create task recordings, see [Task recorder resources](../../user-interface/task-recorder.md).</span></span>

## <a name="validate-expected-values-using-operators"></a><span data-ttu-id="59cdb-112">演算子を使用して予測値を検証する</span><span class="sxs-lookup"><span data-stu-id="59cdb-112">Validate expected values using operators</span></span>

<span data-ttu-id="59cdb-113">この機能を使用するには、Regression Suite Automation Tool のインストール フォルダーの **Microsoft.Dynamics.RegressionSuite.WindowsApp.exe.config** という名前の構成ファイルを編集する必要があります。</span><span class="sxs-lookup"><span data-stu-id="59cdb-113">To utilize this feature, you need to edit the config file named **Microsoft.Dynamics.RegressionSuite.WindowsApp.exe.config** in the Regression suite automation tool installation folder.</span></span> <span data-ttu-id="59cdb-114">ファイルを編集し、**AddOperatorFieldsToExcelValidation** の値を **true** に変更します。</span><span class="sxs-lookup"><span data-stu-id="59cdb-114">Edit the file and modify the value of the **AddOperatorFieldsToExcelValidation** to **true**.</span></span>

```Xml
<add key=" AddOperatorFieldsToExcelValidation" value="true" />
```

<span data-ttu-id="59cdb-115">Regression Suite Automation Tool の以前のバージョンでは、コントロール値が予測値に等しいかどうかのみが検証可能でした。</span><span class="sxs-lookup"><span data-stu-id="59cdb-115">In previous versions of the Regression suite automation tool, you could only validate if a control value is equal to an expected value.</span></span> <span data-ttu-id="59cdb-116">この新しい機能を使用すると、変数が指定された値と等しくない、指定された値より小さい、または指定された値より大きいことを検証できます。</span><span class="sxs-lookup"><span data-stu-id="59cdb-116">This new feature allows you to validate that a variable is not equal, less than, or greater than a specified value.</span></span>

<span data-ttu-id="59cdb-117">このツールの古いバージョンを使用してきた場合、この機能を活用するためには、新しい Excel パラメーター ファイルを再生成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="59cdb-117">If you have been using an older version of the tool, you will need to regenerate new Excel parameter files to take advantage of this functionality.</span></span> <span data-ttu-id="59cdb-118">Excel ファイルに、次の図に示すような新しい **オペレーター** フィールドが表示されます。</span><span class="sxs-lookup"><span data-stu-id="59cdb-118">In the Excel file, a new **Operator** field will appear, as shown in the following image.</span></span>

![以前のバージョンの Excel での検証](media/validate-test-case-example.png)

