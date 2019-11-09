---
title: テストと検証
description: このチュートリアルでは、テスト ケースを作成して実行する方法を説明します。
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
ms.custom: 24231
ms.assetid: 41dcbbda-e377-45a8-b180-5daa0e63c4a9
ms.search.region: Global
ms.author: shailesn
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: ecc8e86136c2aa11b10b7ac114526bf2fc62b817
ms.sourcegitcommit: 574309903f15eeab7911091114885b5c7279d22a
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/24/2019
ms.locfileid: "2658880"
---
# <a name="testing-and-validations"></a><span data-ttu-id="8cc9b-103">テストと検証</span><span class="sxs-lookup"><span data-stu-id="8cc9b-103">Testing and validations</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="8cc9b-104">このチュートリアルでは、テスト ケースを作成して実行する方法を説明します。</span><span class="sxs-lookup"><span data-stu-id="8cc9b-104">This tutorial shows you how to create and run test cases.</span></span>

<a name="prerequisites"></a><span data-ttu-id="8cc9b-105">前提条件</span><span class="sxs-lookup"><span data-stu-id="8cc9b-105">Prerequisites</span></span>
-------------

<span data-ttu-id="8cc9b-106">開発者トポロジを開発者およびビルト VM を使用して配置する必要があります。</span><span class="sxs-lookup"><span data-stu-id="8cc9b-106">You will need to deploy Developer Topology with Developer and Build VM.</span></span>

## <a name="key-concepts"></a><span data-ttu-id="8cc9b-107">重要な概念</span><span class="sxs-lookup"><span data-stu-id="8cc9b-107">Key concepts</span></span>
-   <span data-ttu-id="8cc9b-108">SysTest フレームワークを使用して単位またはコンポーネントのテスト コードを作成します。</span><span class="sxs-lookup"><span data-stu-id="8cc9b-108">Use SysTest Framework to author unit/component test code.</span></span>
-   <span data-ttu-id="8cc9b-109">テスト コードと FormAdaptors を管理するテスト モジュールの作成。</span><span class="sxs-lookup"><span data-stu-id="8cc9b-109">Test module creation to manage test code and FormAdaptors.</span></span>
-   <span data-ttu-id="8cc9b-110">テスト コードを生成するために Visual Studio に記録しているタスク レコーダーをインポートします。</span><span class="sxs-lookup"><span data-stu-id="8cc9b-110">Import Task Recorder recordings into Visual Studio to generate test code.</span></span>
-   <span data-ttu-id="8cc9b-111">ビルド マシンとテスト モジュールを統合します。</span><span class="sxs-lookup"><span data-stu-id="8cc9b-111">Integrate a Test module with a build machine.</span></span>

<span data-ttu-id="8cc9b-112">[![テスト モジュールの統合](./media/54.png)](./media/54.png)</span><span class="sxs-lookup"><span data-stu-id="8cc9b-112">[![Integrate a test module](./media/54.png)](./media/54.png)</span></span>  

## <a name="use-systest-framework-to-author-unitcomponent-test-code"></a><span data-ttu-id="8cc9b-113">SysTest フレームワークを使用して単位またはコンポーネントのテスト コードを作成</span><span class="sxs-lookup"><span data-stu-id="8cc9b-113">Use SysTest Framework to author unit/component test code</span></span>
<span data-ttu-id="8cc9b-114">新しいテスト ケースを作成して、アプリケーションで機能をテストすることができます。</span><span class="sxs-lookup"><span data-stu-id="8cc9b-114">You can create new test cases to test the functionality in an application.</span></span>

1.  <span data-ttu-id="8cc9b-115">Visual Studio を管理者としてオープンします。</span><span class="sxs-lookup"><span data-stu-id="8cc9b-115">Open Visual Studio as an administrator.</span></span>
1.  <span data-ttu-id="8cc9b-116">**ファイル**メニューで、**開く** &gt; **プロジェクト/ソリューション**をクリックし、デスクトップ フォルダーから **FleetManagement** **ソリューション**を選択します。</span><span class="sxs-lookup"><span data-stu-id="8cc9b-116">On the **File** menu, click **Open** &gt; **Project/Solution**, and then select **FleetManagement** **solution** from the desktop folder.</span></span> <span data-ttu-id="8cc9b-117">ソリューション ファイルがコンピュータにない場合は、作成手順が「[チュートリアル: AOT のフリート管理モデルからフリート管理ソリューションを作成する](https://community.dynamics.com/ax/b/newdynamicsax/archive/2016/05/19/tutorial-create-a-fleet-management-solution-file-out-of-the-fleet-management-models-in-the-aot)」に記載されています。</span><span class="sxs-lookup"><span data-stu-id="8cc9b-117">If the solution file is not on your computer, the steps to create it are listed in [Tutorial: Create a Fleet Management solution file out of the Fleet Management models in the AOT](https://community.dynamics.com/ax/b/newdynamicsax/archive/2016/05/19/tutorial-create-a-fleet-management-solution-file-out-of-the-fleet-management-models-in-the-aot).</span></span>
1.  <span data-ttu-id="8cc9b-118">**ソリューション エクスプローラー**で、**フリート管理**ソリューションを右クリックして**追加**をポイントしてから**新規プロジェクト**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="8cc9b-118">In **Solution Explorer**, right-click the **Fleet Management** solution, point to **Add**, and then click **New Project**.</span></span>
1.  <span data-ttu-id="8cc9b-119">作成するプロジェクト タイプとして **Finance and Operations** を選択します。</span><span class="sxs-lookup"><span data-stu-id="8cc9b-119">Choose **Finance and Operations** as the project type to create.</span></span>
1.  <span data-ttu-id="8cc9b-120">この新しいプロジェクトに *FleetManagementUnitTestSample* と名前を付け、デスクトップの FleetManagement フォルダー (C:\Users\Public\Desktop\FleetManagement) を場所として指定してから、**OK** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="8cc9b-120">Name this new project *FleetManagementUnitTestSample*, specify the FleetManagement folder on the desktop (C:\Users\Public\Desktop\FleetManagement) as the location, and then click **OK**.</span></span> 
1.  <span data-ttu-id="8cc9b-121">**ソリューション エクスプローラー**で、新規プロジェクトを右クリックしてから**プロパティ**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="8cc9b-121">In **Solution Explorer**, right-click the new project, and then click **Properties**.</span></span>
1.  <span data-ttu-id="8cc9b-122">**Model** プロパティを **FleetManagementUnitTests** に設定し、**OK** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="8cc9b-122">Set the **Model** property to **FleetManagementUnitTests**, and then click **OK**.</span></span> 

    <span data-ttu-id="8cc9b-123">[![モデル プロパティ](./media/56.png)](./media/56.png)</span><span class="sxs-lookup"><span data-stu-id="8cc9b-123">[![Model property](./media/56.png)](./media/56.png)</span></span>

1.  <span data-ttu-id="8cc9b-124">FleetManagementUnitTestSample プロジェクトを右クリックして**追加**をポイントしてから**新しい項目**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="8cc9b-124">Right-click the FleetManagementUnitTestSample project, point to **Add**, and then click **New Item**.</span></span>
1.  <span data-ttu-id="8cc9b-125">**新しい項目の追加**ウィンドウで、追加する要素のタイプとして**クラス**を選択します。</span><span class="sxs-lookup"><span data-stu-id="8cc9b-125">In the **Add New Item** window, select **Class** as the type of element to add.</span></span> <span data-ttu-id="8cc9b-126">新しいクラスに FMUnitTestSample と名前を付けてから、**追加**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="8cc9b-126">Name the new class FMUnitTestSample, and then click **Add**.</span></span> 

    <span data-ttu-id="8cc9b-127">[![新しい品目を追加](./media/57.png)](./media/57.png)</span><span class="sxs-lookup"><span data-stu-id="8cc9b-127">[![Add new item](./media/57.png)](./media/57.png)</span></span>

1. <span data-ttu-id="8cc9b-128">新しいクラスのコードの最初の行で、クラスが SysTestCase クラスを拡張していることを示します。</span><span class="sxs-lookup"><span data-stu-id="8cc9b-128">In the first line of the code for the new class, indicate that the class extends the SysTestCase class.</span></span>
1. <span data-ttu-id="8cc9b-129">クラスのメソッドを定義する次のコードを追加します。</span><span class="sxs-lookup"><span data-stu-id="8cc9b-129">Add the following code to define the methods for the class.</span></span> <span data-ttu-id="8cc9b-130">これらのメソッドは、2 つの追加テストを定義します。</span><span class="sxs-lookup"><span data-stu-id="8cc9b-130">These methods define two additional tests.</span></span>

        class FMUnitTestSample extends SysTestCase
        {
            public void setup()
            {
                // Reset the test data to be sure things are clean
                FMDataHelper::main(null);
            }

            [SysTestMethodAttribute]
            public void testFMTotalsEngine()
            {
                FMRental rental;
                FMTotalsEngine fmTotals;
                FMRentalTotal fmRentalTotal;
                FMRentalCharge rentalCharge;
                FMRentalTotal expectedtotal;
                str rentalID = '000022';

                // Find a known rental
                rental = FMRental::find(rentalID);

                // Get the rental charges associated with the rental
                // Data is seeded randomly, so this will change for each run
                select sum(ExtendedAmount) from rentalCharge
                        where rentalCharge.RentalId == rental.RentalId;

                fmTotals = FMTotalsEngine::construct();
                fmTotals.calculateRentalVehicleRate(rental);

                // Get the totals from the engine
                fmRentalTotal = fmTotals.totals(rental);

                // Set the expected amount
                expectedTotal = rental.VehicleRateTotal + rentalCharge.ExtendedAmount;

                this.assertEquals(expectedTotal,fmRentalTotal);
            }

            [SysTestMethodAttribute]
            public void testFMCarValidateField()
            {
                FMCarClass fmCar;

                fmCar.NumberOfDoors = -1;
                this.assertFalse(fmCar.validateField(Fieldnum("FMCarClass", "NumberOfDoors")));

                fmCar.NumberOfDoors = 4;
                this.assertTrue(fmCar.validateField(Fieldnum("FMCarClass", "NumberOfDoors")));
            }
        }

1. <span data-ttu-id="8cc9b-131">新しいクラスを保存します。</span><span class="sxs-lookup"><span data-stu-id="8cc9b-131">Save the new class.</span></span> <span data-ttu-id="8cc9b-132">保存が完了した後、**テスト エクスプローラー**に追加 2 つのテスト ケースが表示されます。</span><span class="sxs-lookup"><span data-stu-id="8cc9b-132">After the save is complete, you will see the additional two test cases in **Test Explorer**.</span></span> <span data-ttu-id="8cc9b-133">**ソリューション エクスプローラー**で FleetManagementUnitTestSample プロジェクトを右クリックし、**ビルド** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="8cc9b-133">Right-click on the FleetManagementUnitTestSample project in **Solution Explorer**, and then click **Build.**</span></span>
1.  <span data-ttu-id="8cc9b-134">**表示**メニューで、**テスト エクスプローラー**を開きます。</span><span class="sxs-lookup"><span data-stu-id="8cc9b-134">On the **View** menu, open **Test Explorer**.</span></span> 
1. <span data-ttu-id="8cc9b-135">特定のテスト ケースを実行するには、**選択したテストの実行**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="8cc9b-135">Click **Run selected test** to execute specific test case.</span></span>
1. <span data-ttu-id="8cc9b-136">完了した後、テスト エクスプローラーにテストの結果が表示されます。</span><span class="sxs-lookup"><span data-stu-id="8cc9b-136">Test Explorer will show the results of test after it is complete.</span></span> 

    <span data-ttu-id="8cc9b-137">[![完了したテスト](./media/59-300x290.png)](./media/59.png)</span><span class="sxs-lookup"><span data-stu-id="8cc9b-137">[![Completed test](./media/59-300x290.png)](./media/59.png)</span></span>

## <a name="test-module-creation-to-manage-test-code-and-formadaptors"></a><span data-ttu-id="8cc9b-138">テスト コードと FormAdaptors を管理するテスト モジュールの作成</span><span class="sxs-lookup"><span data-stu-id="8cc9b-138">Test module creation to manage test code and FormAdaptors</span></span>
<span data-ttu-id="8cc9b-139">テスト コードをまとめて管理しやすくするためにテスト固有のモジュールを作成しています。</span><span class="sxs-lookup"><span data-stu-id="8cc9b-139">Creating a test specific module helps to keep test code together and manageable.</span></span>

1. <span data-ttu-id="8cc9b-140">**Visual Studio** を開き、**Finance and Operations** > **モデル管理** > **モデルの作成** に移動します。</span><span class="sxs-lookup"><span data-stu-id="8cc9b-140">Open **Visual Studio** and go to **Finance and Operations** > **Model Management** > **Create model**.</span></span>

2. <span data-ttu-id="8cc9b-141">モデル名を入力し、レイヤーを選択し、次に追加詳細を入力します。</span><span class="sxs-lookup"><span data-stu-id="8cc9b-141">Enter the model name, select the layer, and then enter any additional details.</span></span> <span data-ttu-id="8cc9b-142">テスト モジュールの名前に**テスト**という語を含めることをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="8cc9b-142">Note that it's a good idea to include the word **Test** in the name of the test module.</span></span> <span data-ttu-id="8cc9b-143">既定のビルド定義は、**テスト** という単語を含むすべてのテスト モジュールを検出するように設定されています。</span><span class="sxs-lookup"><span data-stu-id="8cc9b-143">The default build definition is configured to discover all test modules that contain the word **Test**.</span></span> 
   
3. <span data-ttu-id="8cc9b-144">このモデルは Application Platform/Foundation からのフォームを保持するため、以下に示すモデルへの参照を追加します。</span><span class="sxs-lookup"><span data-stu-id="8cc9b-144">Because this model holds forms from the Application Platform/Foundation, add references to models shown below.</span></span>

    <span data-ttu-id="8cc9b-145">[![モデル参照](./media/62-1024x786.png)](./media/62.png)</span><span class="sxs-lookup"><span data-stu-id="8cc9b-145">[![Model references](./media/62-1024x786.png)](./media/62.png)</span></span>

<span data-ttu-id="8cc9b-146">基本テスト モジュールを配置した後、タスク レコーダーの記録をインポートしてテスト コードを生成することができます。</span><span class="sxs-lookup"><span data-stu-id="8cc9b-146">After the base test module is in place, you can import a Task Recorder recording to generate test code.</span></span> <span data-ttu-id="8cc9b-147">タスク レコーダーの記録の XML をインポートするとき、FormAdaptors を使用してテスト コードが生成されます。</span><span class="sxs-lookup"><span data-stu-id="8cc9b-147">When you import a Task Recorder recording XML, test code is generated using FormAdaptors.</span></span> <span data-ttu-id="8cc9b-148">フォーム アダプターは、フォーム機能をテストするために使用される、強く定型化された API を提供するフォーム上のラッパー クラスです。</span><span class="sxs-lookup"><span data-stu-id="8cc9b-148">Form adaptors are wrapper classes over forms which provide strongly typed API that can be used to test form functionality.</span></span> <span data-ttu-id="8cc9b-149">組み込みのフォームの各パッケージの事前に生成した FormAdapters を含めました。</span><span class="sxs-lookup"><span data-stu-id="8cc9b-149">We have included pre-generated FormAdapters for each package for built-in forms.</span></span> <span data-ttu-id="8cc9b-150">テスト モジュールで、テスト コードを実行するヘルパー メソッドがある、パッケージおよび Test Essentials に対応するフォーム アダプタへの参照を追加します。</span><span class="sxs-lookup"><span data-stu-id="8cc9b-150">In the test module, add a reference to the corresponding Form Adaptor for packages and Test Essentials, which has helper methods to execute test code.</span></span>

## <a name="import-a-task-recorder-recording-into-visual-studio-to-generate-test-code"></a><span data-ttu-id="8cc9b-151">テスト コードを生成するために Visual Studio に記録しているタスク レコーダーをインポートします。</span><span class="sxs-lookup"><span data-stu-id="8cc9b-151">Import a Task Recorder recording into Visual Studio to generate test code</span></span>
<span data-ttu-id="8cc9b-152">タスク レコーダーの記録からテスト コードを生成して、ヘッドレス (非 UI) テストを実行することができます。</span><span class="sxs-lookup"><span data-stu-id="8cc9b-152">You can generate test code from Task Recorder recording to execute headless (non-UI) test.</span></span>

1. <span data-ttu-id="8cc9b-153">タスク レコーダーを使用してシナリオを記録します。</span><span class="sxs-lookup"><span data-stu-id="8cc9b-153">Record a scenario in by using Task Recorder.</span></span>

2. <span data-ttu-id="8cc9b-154">Visual Studio でタスク記録をインポートするには、**Finance and Operations** > **アドイン** > **タスク記録をインポート** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="8cc9b-154">To import a Task Recording, in Visual Studio, click **Finance and Operations** > **Addins** > **Import Task Recording**.</span></span> 

3. <span data-ttu-id="8cc9b-155">**タスクの記録をインポート** ダイアログで、タスクの記録をインポートするテスト モジュール (ISVTestModule) を選択し、記録している xml ファイルを参照します。</span><span class="sxs-lookup"><span data-stu-id="8cc9b-155">In the **Import Task Recording** dialog, select the Test Module (ISVTestModule) under which you want to import task recording, and browse to recording xml file.</span></span> 

    <span data-ttu-id="8cc9b-156">[![テスト モジュール](./media/64-249x300.png)](./media/64.png)</span><span class="sxs-lookup"><span data-stu-id="8cc9b-156">[![Test module](./media/64-249x300.png)](./media/64.png)</span></span>

4. <span data-ttu-id="8cc9b-157">タスクの記録インポート プロセスは、Visual Studio IDE で表示できる SysTestAdapter および FormAdaptor に基づいてテスト コードを生成します。</span><span class="sxs-lookup"><span data-stu-id="8cc9b-157">The task recording import process generates test code that is based on the SysTestAdapter and FormAdaptor which can be viewed in Visual Studio IDE.</span></span> <span data-ttu-id="8cc9b-158">このステップの一部として生成されるテスト ソース コードをお客様が変更することを予定していません。</span><span class="sxs-lookup"><span data-stu-id="8cc9b-158">We do not expect you to change any test source code that is generated as part of this step.</span></span>
  
5. <span data-ttu-id="8cc9b-159">テスト コードが生成された後、テスト検出および実行のための Visual Studio オプションを設定します。</span><span class="sxs-lookup"><span data-stu-id="8cc9b-159">After the test code is generated, set up Visual Studio options for test discovery and execution:</span></span>
   - <span data-ttu-id="8cc9b-160">64 ビット コンピューターを使用する場合は、単体テストを実行し、64 ビット プロセスとしてコード カバレッジ情報を取得できます。</span><span class="sxs-lookup"><span data-stu-id="8cc9b-160">If you have a 64-bit machine, you can run unit tests and capture code coverage information as a 64-bit process.</span></span>
   - <span data-ttu-id="8cc9b-161">これを構成するには、**テスト**&gt;**テストの設定**&gt;**既定のプロセッサ アーキテクチャ** を選択し、**X64** を選択します。</span><span class="sxs-lookup"><span data-stu-id="8cc9b-161">To configure this, select **Test** &gt; **Test Settings** &gt; **Default Processor Architecture**, and then select **X64**.</span></span>
   - <span data-ttu-id="8cc9b-162">テストの実行エンジンが開き、テスト プロジェクト内のアセンブリをロックする状態が発生した可能性があります。</span><span class="sxs-lookup"><span data-stu-id="8cc9b-162">You might run into a situation in which the test execution engine opens and locks an assembly in your test project.</span></span> <span data-ttu-id="8cc9b-163">この場合、たとえば、アセンブリに対する変更を保存することはできません。</span><span class="sxs-lookup"><span data-stu-id="8cc9b-163">When this happens, you can’t for example, save changes to the assembly.</span></span> <span data-ttu-id="8cc9b-164">これを修正するには、**テスト**&gt;**テスト設定** を選択し、**テスト実行エンジンを実行し続ける** を選択します。</span><span class="sxs-lookup"><span data-stu-id="8cc9b-164">To fix this, select **Test** &gt; **Test Settings**, and then select **Keep Test Execution Engine Running**.</span></span> 
    - <span data-ttu-id="8cc9b-165">Visual Studio IDE で生成されたテスト コードがあるので、テストを検出してローカルで実行します。</span><span class="sxs-lookup"><span data-stu-id="8cc9b-165">Now that you have test code generated in Visual Studio IDE, it's time to discover the test and try executing them locally.</span></span>

6. <span data-ttu-id="8cc9b-166">メニュー オプションから、**テスト** &gt; **Windows** を選択し、**テスト エクスプ ローラー**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="8cc9b-166">From menu options, select **Test** &gt; **Windows**, and then click **Test Explorer**.</span></span> <span data-ttu-id="8cc9b-167">テスト エクスプローラー ウィンドウが開いた後、テスト コードからテストを検出し、次のように使用可能なすべてのテストを一覧表示します。</span><span class="sxs-lookup"><span data-stu-id="8cc9b-167">After the Test Explorer window is open, it will try to discover test from test code and list all the available tests as shown below.</span></span>

    <span data-ttu-id="8cc9b-168">[![テスト エクスプローラー](./media/67-1024x658.png)](./media/67.png)</span><span class="sxs-lookup"><span data-stu-id="8cc9b-168">[![Test explorer](./media/67-1024x658.png)](./media/67.png)</span></span>

7. <span data-ttu-id="8cc9b-169">テストを選択し、**実行** &gt; **選択されている実行** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="8cc9b-169">Select the test and then click **Run** &gt; **Execute selected**.</span></span> <span data-ttu-id="8cc9b-170">これにより、ローカルに展開された環境に対してテストが実行されます。</span><span class="sxs-lookup"><span data-stu-id="8cc9b-170">This will execute test against the locally deployed environment.</span></span> 

    <span data-ttu-id="8cc9b-171">[![選択の実行](./media/68-1024x652.png)](./media/68.png)</span><span class="sxs-lookup"><span data-stu-id="8cc9b-171">[![Execute selected](./media/68-1024x652.png)](./media/68.png)</span></span>

## <a name="integration-of-the-test-module-with-build-process"></a><span data-ttu-id="8cc9b-172">ビルド プロセスのあるテスト モジュールの統合</span><span class="sxs-lookup"><span data-stu-id="8cc9b-172">Integration of the test module with build process</span></span>
<span data-ttu-id="8cc9b-173">テスト モジュールがソース管理の一部である場合、ビルド プロセス テンプレートは、名前に**テスト**という単語を含むすべてのテスト モジュールを検出します。</span><span class="sxs-lookup"><span data-stu-id="8cc9b-173">After the test module is a part of source control, the build process template will discover all test modules, which contain the word **Test** in the name.</span></span> <span data-ttu-id="8cc9b-174">次の図は、Visual Studio Online の一部としてのビルドとテストの実行を示しています。</span><span class="sxs-lookup"><span data-stu-id="8cc9b-174">The following illustration shows build and test execution as part of Visual Studio Online.</span></span> 

<span data-ttu-id="8cc9b-175">[![ビルドおよびテストの実行](./media/69.png)](./media/69.png)</span><span class="sxs-lookup"><span data-stu-id="8cc9b-175">[![Build and test execution](./media/69.png)](./media/69.png)</span></span>


