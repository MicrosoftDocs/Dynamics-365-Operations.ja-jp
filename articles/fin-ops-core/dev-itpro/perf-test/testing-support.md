---
title: Visual Studio のプロジェクトのテスト
description: このトピックでは、Visual Studio でテストするためのオプションについて説明します。
author: RobinARH
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Developer
ms.reviewer: rhaertle
ms.search.scope: Operations
ms.custom: 24161
ms.assetid: d94f46f0-cde2-47c3-8994-c79e609eabce
ms.search.region: Global
ms.author: shailesn
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 497a98e1082b75eaa9a3448dea8d963414144722
ms.sourcegitcommit: 8ff2413b6cb504d2b36fce2bb50441b2e690330e
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/24/2020
ms.locfileid: "3082009"
---
# <a name="test-projects-in-visual-studio"></a><span data-ttu-id="e838b-103">Visual Studio のプロジェクトのテスト</span><span class="sxs-lookup"><span data-stu-id="e838b-103">Test projects in Visual Studio</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="e838b-104">このトピックでは、Visual Studio でテストするためのオプションについて説明します。</span><span class="sxs-lookup"><span data-stu-id="e838b-104">This topic describes the options for testing in Visual Studio.</span></span>

<span data-ttu-id="e838b-105">カスタム単体テスト アダプターは、Visual Studio で利用可能です。</span><span class="sxs-lookup"><span data-stu-id="e838b-105">A custom unit test adapter is available in Visual Studio.</span></span> <span data-ttu-id="e838b-106">このアダプタを使用すると、テスト作成者は Visual Studio の標準の **Test Explorer** ウィンドウを使用して、X++ テストのスケジュールを立て、テスト結果を分析できます。</span><span class="sxs-lookup"><span data-stu-id="e838b-106">This adapter lets test authors use the standard **Test Explorer** window in Visual Studio to schedule X++ tests and analyze test results.</span></span> <span data-ttu-id="e838b-107">開発者は **SysTestAdaptor** を使用してテストを作成できます。</span><span class="sxs-lookup"><span data-stu-id="e838b-107">Developers can author tests by using **SysTestAdaptor**.</span></span> <span data-ttu-id="e838b-108">タスク レコーダーの記録からテスト コードを生成することもできます。</span><span class="sxs-lookup"><span data-stu-id="e838b-108">They can also generate test code from Task Recorder recordings.</span></span> <span data-ttu-id="e838b-109">これらのテスト ケースは、検証のためにシステムを構築するために追加することができます。</span><span class="sxs-lookup"><span data-stu-id="e838b-109">These test cases can then be added to build systems for validations.</span></span> 

<span data-ttu-id="e838b-110">[![Visual Studio のテスト用オプションの図](./media/1_support.png)](./media/1_support.png)</span><span class="sxs-lookup"><span data-stu-id="e838b-110">[![Illustration of options for testing in Visual Studio](./media/1_support.png)](./media/1_support.png)</span></span>

## <a name="author-unitcomponent-test-code-by-using-the-systest-framework"></a><span data-ttu-id="e838b-111">SysTest フレームワークを使用して単位またはコンポーネント テスト コードを作成</span><span class="sxs-lookup"><span data-stu-id="e838b-111">Author unit/component test code by using the SysTest Framework</span></span>
<span data-ttu-id="e838b-112">Visual Studio でプロジェクトを作成するときは、X++ 単体テストを追加できます。</span><span class="sxs-lookup"><span data-stu-id="e838b-112">When you create a project in Visual Studio, you can add an X++ unit test.</span></span> <span data-ttu-id="e838b-113">**SysTestCase** を含むクラスを拡張し、その後 **SysTestMethodAttribute** 属性を追加するか、またはメソッド名に "test" を含むケースを接頭語として付けます。</span><span class="sxs-lookup"><span data-stu-id="e838b-113">You extend the class with **SysTestCase**, and then either add the **SysTestMethodAttribute** attribute or prefix the case with "test" in the method name.</span></span>

```xpp
class FMUnitTestSample extends SysTestCase
{
    [SysTestMethod]
    public void testTotalsEngineConfig()
    {
    }
}
```

<span data-ttu-id="e838b-114">クラスを保存すると、C\# テストが表示されるのと同じように、テスト エクスプローラーに各テストが表示されます。</span><span class="sxs-lookup"><span data-stu-id="e838b-114">After you save the class, each test appears in Test Explorer, just as a C\# test would appear.</span></span> 

<span data-ttu-id="e838b-115">[![テスト エクスプローラーに表示されるテストの例](./media/2_support.png)](./media/2_support.png)</span><span class="sxs-lookup"><span data-stu-id="e838b-115">[![Example of test appearing in Test Explorer](./media/2_support.png)](./media/2_support.png)</span></span> 

<span data-ttu-id="e838b-116">テスト エクスプローラーで、テストを実行したり、右クリックからの選択したテストの実行やデバッグによってテスト ケースをデバッグしたりできます。</span><span class="sxs-lookup"><span data-stu-id="e838b-116">In Test Explorer, you can run the tests, or you can debug the test case by right-clicking and running or debugging the selected tests.</span></span> 

> [!NOTE]
> <span data-ttu-id="e838b-117">テストを実行する前に、テストが含まれるようプロジェクトを構築する必要があります。</span><span class="sxs-lookup"><span data-stu-id="e838b-117">Before you can run tests, you must build the project so that it includes tests.</span></span> 

<span data-ttu-id="e838b-118">[![選択したテストを実行またはデバッグするための右クリックの例](./media/3_support.png)](./media/3_support.png)</span><span class="sxs-lookup"><span data-stu-id="e838b-118">[![Example of right-clicking to run or debug selected tests](./media/3_support.png)](./media/3_support.png)</span></span> 

<span data-ttu-id="e838b-119">また、プロジェクト内のオブジェクトのための既存のテストを見つけることができます。</span><span class="sxs-lookup"><span data-stu-id="e838b-119">You can also discover existing tests for an object in your project.</span></span> <span data-ttu-id="e838b-120">検索では、相互参照データを使用します。</span><span class="sxs-lookup"><span data-stu-id="e838b-120">Discovery uses cross-reference data.</span></span> <span data-ttu-id="e838b-121">プロジェクトでオブジェクトを右クリックし、**関連するテストの検出** を選択します。</span><span class="sxs-lookup"><span data-stu-id="e838b-121">Right-click an object in the project, and then select **Discover Related Tests**.</span></span> <span data-ttu-id="e838b-122">このコマンドは、相互参照データを照会し、そのオブジェクトを参照するテストを返します。</span><span class="sxs-lookup"><span data-stu-id="e838b-122">This command queries the cross-reference data and returns any tests that reference the object.</span></span> <span data-ttu-id="e838b-123">テスト ケースのリストがテスト エクスプローラーに表示されます。</span><span class="sxs-lookup"><span data-stu-id="e838b-123">The list of test cases is displayed in Test Explorer.</span></span> 

<span data-ttu-id="e838b-124">[![テスト エクスプローラーに表示されるテスト ケースの例](./media/4_support.png)](./media/4_support.png)</span><span class="sxs-lookup"><span data-stu-id="e838b-124">[![Example of test cases displayed in Test Explorer](./media/4_support.png)](./media/4_support.png)</span></span> 

<span data-ttu-id="e838b-125">この機能を使用することにより、関連するすべてのテストを実行できます。</span><span class="sxs-lookup"><span data-stu-id="e838b-125">By using this functionality, you can run all the relevant tests.</span></span> <span data-ttu-id="e838b-126">テスト エクスプローラーには、現在のプロジェクトのすべてのテストと参照されているオブジェクトのすべてのテストが含まれます。</span><span class="sxs-lookup"><span data-stu-id="e838b-126">Test Explorer contains all tests for the current project and all tests for the referenced objects.</span></span>

## <a name="generate-test-code-by-importing-task-recorder-recordings-into-visual-studio"></a><span data-ttu-id="e838b-127">Visual Studio に記録しているタスク レコーダーをインポートして、テスト コードを生成します。</span><span class="sxs-lookup"><span data-stu-id="e838b-127">Generate test code by importing Task Recorder recordings into Visual Studio</span></span>
<span data-ttu-id="e838b-128">タスク レコーダーの記録のために XML をインポートして、さまざまな業務プロセスのシナリオを検証するために使用できるテスト コードを生成することができます。</span><span class="sxs-lookup"><span data-stu-id="e838b-128">You can import the XML for Task Recorder recordings to generate test code that can be used to validate various business process scenarios.</span></span> 

<span data-ttu-id="e838b-129">[![インポート タスク記録 ダイアログ ボックスの例](./media/5_support.png)](./media/5_support.png)</span><span class="sxs-lookup"><span data-stu-id="e838b-129">[![Example of Import Task Recording dialog box](./media/5_support.png)](./media/5_support.png)</span></span> 

<span data-ttu-id="e838b-130">生成されたコードは SysTest フレームワークおよび FormAdaptors に基づいています。</span><span class="sxs-lookup"><span data-stu-id="e838b-130">Generated code is based on the SysTest Framework and FormAdaptors.</span></span> <span data-ttu-id="e838b-131">FormAdaptors は、ページ上のラッパー クラスです。</span><span class="sxs-lookup"><span data-stu-id="e838b-131">FormAdaptors are wrapper classes over pages.</span></span> <span data-ttu-id="e838b-132">これらは、ページ機能をテストするために使用できる強く型付けされたアプリケーション プログラミング インターフェイス (API) を提供します。</span><span class="sxs-lookup"><span data-stu-id="e838b-132">They provide strongly typed application programming interfaces (APIs) that can be used to test page functionality.</span></span> <span data-ttu-id="e838b-133">組み込みのページの各パッケージに、事前に生成した FormAdapters が含まれます。</span><span class="sxs-lookup"><span data-stu-id="e838b-133">Pre-generated FormAdaptors are included for each package for built-in pages.</span></span> <span data-ttu-id="e838b-134">テスト モジュールで、テスト コードを実行するヘルパー メソッドを含む、パッケージおよび「Test Essentials」に対応する FormAdaptor への参照を追加します。</span><span class="sxs-lookup"><span data-stu-id="e838b-134">In a test module, add a reference to a corresponding FormAdaptor for packages and "Test Essentials," which contain helper methods to run test code.</span></span>

## <a name="advanced-options"></a><span data-ttu-id="e838b-135">詳細オプション</span><span class="sxs-lookup"><span data-stu-id="e838b-135">Advanced Options</span></span>

<span data-ttu-id="e838b-136">分類および実行のためのテストをフィルター処理する詳細オプションは、[systest-filtering.md] を参照してください。</span><span class="sxs-lookup"><span data-stu-id="e838b-136">For advanced options to categorize and filter tests for execution, see [systest-filtering.md]</span></span>
