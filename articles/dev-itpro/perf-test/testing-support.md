---
title: "Visual Studio のプロジェクトのテスト"
description: "このトピックでは、Visual Studio でテストするためのオプションについて説明します。"
author: RobinARH
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Developer
ms.reviewer: robinr
ms.search.scope: Operations
ms.custom: 24161
ms.assetid: d94f46f0-cde2-47c3-8994-c79e609eabce
ms.search.region: Global
ms.author: shailesn
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: a90ba87b5fb195b846e44fb37eecbf4a4e2523e3
ms.contentlocale: ja-jp
ms.lasthandoff: 05/08/2018

---

# <a name="test-projects-in-visual-studio"></a><span data-ttu-id="77f71-103">Visual Studio のプロジェクトのテスト</span><span class="sxs-lookup"><span data-stu-id="77f71-103">Test projects in Visual Studio</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="77f71-104">このトピックでは、Visual Studio でテストするためのオプションについて説明します。</span><span class="sxs-lookup"><span data-stu-id="77f71-104">This topic describes the options for testing in Visual Studio.</span></span>

<span data-ttu-id="77f71-105">カスタム単体テスト アダプターは、Visual Studio で利用可能です。</span><span class="sxs-lookup"><span data-stu-id="77f71-105">A custom unit test adapter is available in Visual Studio.</span></span> <span data-ttu-id="77f71-106">このアダプタを使用すると、テスト作成者は Visual Studio の標準の **Test Explorer** ウィンドウを使用して、X++ テストのスケジュールを立て、テスト結果を分析できます。</span><span class="sxs-lookup"><span data-stu-id="77f71-106">This adapter lets test authors use the standard **Test Explorer** window in Visual Studio to schedule X++ tests and analyze test results.</span></span> <span data-ttu-id="77f71-107">開発者は **SysTestAdaptor** を使用してテストを作成できます。</span><span class="sxs-lookup"><span data-stu-id="77f71-107">Developers can author tests by using **SysTestAdaptor**.</span></span> <span data-ttu-id="77f71-108">タスク レコーダーの記録からテスト コードを生成することもできます。</span><span class="sxs-lookup"><span data-stu-id="77f71-108">They can also generate test code from Task Recorder recordings.</span></span> <span data-ttu-id="77f71-109">これらのテスト ケースは、検証のためにシステムを構築するために追加することができます。</span><span class="sxs-lookup"><span data-stu-id="77f71-109">These test cases can then be added to build systems for validations.</span></span> 

<span data-ttu-id="77f71-110">[![1\_サポート](./media/1_support.png)](./media/1_support.png)</span><span class="sxs-lookup"><span data-stu-id="77f71-110">[![1\_Support](./media/1_support.png)](./media/1_support.png)</span></span>

## <a name="author-unitcomponent-test-code-by-using-the-systest-framework"></a><span data-ttu-id="77f71-111">SysTest フレームワークを使用して単位またはコンポーネント テスト コードを作成</span><span class="sxs-lookup"><span data-stu-id="77f71-111">Author unit/component test code by using the SysTest Framework</span></span>
<span data-ttu-id="77f71-112">Visual Studioでプロジェクトを作成するときは、X++ 単体テストを追加できます。</span><span class="sxs-lookup"><span data-stu-id="77f71-112">When you create a project in Visual Studio, you can add an X++ unit test.</span></span> <span data-ttu-id="77f71-113">**SysTestCase** を含むクラスを拡張し、その後 **SysTestMethodAttribute** 属性を追加するか、またはメソッド名に "test" を含むケースを接頭語として付けます。</span><span class="sxs-lookup"><span data-stu-id="77f71-113">You extend the class with **SysTestCase**, and then either add the **SysTestMethodAttribute** attribute or prefix the case with "test" in the method name.</span></span>

    class FMUnitTestSample extends SysTestCase
    {
        [SysTestMethodAttribute]
        public void testTotalsEngineConfig()
        {
        }
    }

<span data-ttu-id="77f71-114">クラスを保存すると、C\# テストが表示されるのと同じように、テスト エクスプローラーに各テストが表示されます。</span><span class="sxs-lookup"><span data-stu-id="77f71-114">After you save the class, each test appears in Test Explorer, just as a C\# test would appear.</span></span> 

<span data-ttu-id="77f71-115">[![2\_サポート](./media/2_support.png)](./media/2_support.png)</span><span class="sxs-lookup"><span data-stu-id="77f71-115">[![2\_Support](./media/2_support.png)](./media/2_support.png)</span></span> 

<span data-ttu-id="77f71-116">テスト エクスプローラーで、テストを実行したり、右クリックからの選択したテストの実行やデバッグによってテスト ケースをデバッグしたりできます。</span><span class="sxs-lookup"><span data-stu-id="77f71-116">In Test Explorer, you can run the tests, or you can debug the test case by right-clicking and running or debugging the selected tests.</span></span> <span data-ttu-id="77f71-117">**注記:** テストを実行する前に、テストが含まれるように、プロジェクトを構築する必要があります。</span><span class="sxs-lookup"><span data-stu-id="77f71-117">**Note:** Before you can run tests, you must build the project so that it includes tests.</span></span> 

<span data-ttu-id="77f71-118">[![3\_サポート](./media/3_support.png)](./media/3_support.png)</span><span class="sxs-lookup"><span data-stu-id="77f71-118">[![3\_Support](./media/3_support.png)](./media/3_support.png)</span></span> 

<span data-ttu-id="77f71-119">また、プロジェクト内のオブジェクトのための既存のテストを見つけることができます。</span><span class="sxs-lookup"><span data-stu-id="77f71-119">You can also discover existing tests for an object in your project.</span></span> <span data-ttu-id="77f71-120">検索では、相互参照データを使用します。</span><span class="sxs-lookup"><span data-stu-id="77f71-120">Discovery uses cross-reference data.</span></span> <span data-ttu-id="77f71-121">プロジェクトでオブジェクトを右クリックし、**関連するテストの検出** を選択します。</span><span class="sxs-lookup"><span data-stu-id="77f71-121">Right-click an object in the project, and then select **Discover Related Tests**.</span></span> <span data-ttu-id="77f71-122">このコマンドは、相互参照データを照会し、そのオブジェクトを参照するテストを返します。</span><span class="sxs-lookup"><span data-stu-id="77f71-122">This command queries the cross-reference data and returns any tests that reference the object.</span></span> <span data-ttu-id="77f71-123">テスト ケースのリストがテスト エクスプローラーに表示されます。</span><span class="sxs-lookup"><span data-stu-id="77f71-123">The list of test cases is displayed in Test Explorer.</span></span> 

<span data-ttu-id="77f71-124">[![4\_サポート](./media/4_support.png)](./media/4_support.png)</span><span class="sxs-lookup"><span data-stu-id="77f71-124">[![4\_Support](./media/4_support.png)](./media/4_support.png)</span></span> 

<span data-ttu-id="77f71-125">この機能を使用することにより、関連するすべてのテストを実行できます。</span><span class="sxs-lookup"><span data-stu-id="77f71-125">By using this functionality, you can run all the relevant tests.</span></span> <span data-ttu-id="77f71-126">テスト エクスプローラーには、現在のプロジェクトのすべてのテストと参照されているオブジェクトのすべてのテストが含まれます。</span><span class="sxs-lookup"><span data-stu-id="77f71-126">Test Explorer contains all tests for the current project and all tests for the referenced objects.</span></span>

## <a name="generate-test-code-by-importing-task-recorder-recordings-into-visual-studio"></a><span data-ttu-id="77f71-127">Visual Studio に記録しているタスク レコーダーをインポートして、テスト コードを生成します。</span><span class="sxs-lookup"><span data-stu-id="77f71-127">Generate test code by importing Task Recorder recordings into Visual Studio</span></span>
<span data-ttu-id="77f71-128">タスク レコーダーの記録のために XML をインポートして、さまざまな業務プロセスのシナリオを検証するために使用できるテスト コードを生成することができます。</span><span class="sxs-lookup"><span data-stu-id="77f71-128">You can import the XML for Task Recorder recordings to generate test code that can be used to validate various business process scenarios.</span></span> 

<span data-ttu-id="77f71-129">[![5\_サポート](./media/5_support.png)](./media/5_support.png)</span><span class="sxs-lookup"><span data-stu-id="77f71-129">[![5\_Support](./media/5_support.png)](./media/5_support.png)</span></span> 

<span data-ttu-id="77f71-130">生成されたコードは SysTest フレームワークおよび FormAdaptors に基づいています。</span><span class="sxs-lookup"><span data-stu-id="77f71-130">Generated code is based on the SysTest Framework and FormAdaptors.</span></span> <span data-ttu-id="77f71-131">FormAdaptors は、ページ上のラッパー クラスです。</span><span class="sxs-lookup"><span data-stu-id="77f71-131">FormAdaptors are wrapper classes over pages.</span></span> <span data-ttu-id="77f71-132">これらは、ページ機能をテストするために使用できる強く型付けされたアプリケーション プログラミング インターフェイス (API) を提供します。</span><span class="sxs-lookup"><span data-stu-id="77f71-132">They provide strongly typed application programming interfaces (APIs) that can be used to test page functionality.</span></span> <span data-ttu-id="77f71-133">組み込みのページの各パッケージに、事前に生成した FormAdapters が含まれます。</span><span class="sxs-lookup"><span data-stu-id="77f71-133">Pre-generated FormAdaptors are included for each package for built-in pages.</span></span> <span data-ttu-id="77f71-134">テスト モジュールで、テスト コードを実行するヘルパー メソッドを含む、パッケージおよび「Test Essentials」に対応する FormAdaptor への参照を追加します。</span><span class="sxs-lookup"><span data-stu-id="77f71-134">In a test module, add a reference to a corresponding FormAdaptor for packages and "Test Essentials," which contain helper methods to run test code.</span></span>




