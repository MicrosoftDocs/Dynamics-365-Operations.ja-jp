---
title: テストと検証
description: このチュートリアルでは、テスト ケースを作成して実行する方法を説明します。
author: jorisdg
ms.date: 04/14/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Developer
ms.reviewer: rhaertle
ms.custom: 24231
ms.assetid: 41dcbbda-e377-45a8-b180-5daa0e63c4a9
ms.search.region: Global
ms.author: jorisde
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 08fbeff94462a7f72c0a930c68b934382e0b6f9e
ms.sourcegitcommit: 51cad1ce3ed44ebf7eb9bdf553ee2df4c1f03135
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/10/2021
ms.locfileid: "6015815"
---
# <a name="testing-and-validations"></a><span data-ttu-id="4f627-103">テストと検証</span><span class="sxs-lookup"><span data-stu-id="4f627-103">Testing and validations</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="4f627-104">このチュートリアルでは、テスト ケースを作成して実行する方法を説明します。</span><span class="sxs-lookup"><span data-stu-id="4f627-104">This tutorial shows you how to create and run test cases.</span></span>

<a name="prerequisites"></a><span data-ttu-id="4f627-105">前提条件</span><span class="sxs-lookup"><span data-stu-id="4f627-105">Prerequisites</span></span>
-------------

<span data-ttu-id="4f627-106">開発者トポロジを開発者およびビルト VM を使用して配置する必要があります。</span><span class="sxs-lookup"><span data-stu-id="4f627-106">You will need to deploy Developer Topology with Developer and Build VM.</span></span>

## <a name="key-concepts"></a><span data-ttu-id="4f627-107">重要な概念</span><span class="sxs-lookup"><span data-stu-id="4f627-107">Key concepts</span></span>
-   <span data-ttu-id="4f627-108">SysTest フレームワークを使用して単位またはコンポーネントのテスト コードを作成します。</span><span class="sxs-lookup"><span data-stu-id="4f627-108">Use SysTest Framework to author unit/component test code.</span></span>
-   <span data-ttu-id="4f627-109">テストの分離</span><span class="sxs-lookup"><span data-stu-id="4f627-109">Test isolation</span></span>
-   <span data-ttu-id="4f627-110">テスト コードと FormAdaptors を管理するテスト モジュールの作成。</span><span class="sxs-lookup"><span data-stu-id="4f627-110">Test module creation to manage test code and FormAdaptors.</span></span>
-   <span data-ttu-id="4f627-111">テスト コードを生成するために Visual Studio に記録しているタスク レコーダーをインポートします。</span><span class="sxs-lookup"><span data-stu-id="4f627-111">Import Task Recorder recordings into Visual Studio to generate test code.</span></span>
-   <span data-ttu-id="4f627-112">ビルド マシンとテスト モジュールを統合します。</span><span class="sxs-lookup"><span data-stu-id="4f627-112">Integrate a Test module with a build machine.</span></span>

<span data-ttu-id="4f627-113">[![テスト モジュールの統合](./media/54.png)](./media/54.png)</span><span class="sxs-lookup"><span data-stu-id="4f627-113">[![Integrate a test module](./media/54.png)](./media/54.png)</span></span>  

## <a name="use-systest-framework-to-author-unitcomponent-test-code"></a><span data-ttu-id="4f627-114">SysTest フレームワークを使用して単位またはコンポーネントのテスト コードを作成</span><span class="sxs-lookup"><span data-stu-id="4f627-114">Use SysTest Framework to author unit/component test code</span></span>
<span data-ttu-id="4f627-115">新しいテスト ケースを作成して、アプリケーションで機能をテストすることができます。</span><span class="sxs-lookup"><span data-stu-id="4f627-115">You can create new test cases to test the functionality in an application.</span></span>

1.  <span data-ttu-id="4f627-116">Visual Studio を管理者としてオープンします。</span><span class="sxs-lookup"><span data-stu-id="4f627-116">Open Visual Studio as an administrator.</span></span>
1.  <span data-ttu-id="4f627-117">**ファイル** メニューで、**開く** &gt; **プロジェクト/ソリューション** をクリックし、デスクトップ フォルダーから **FleetManagement** **ソリューション** を選択します。</span><span class="sxs-lookup"><span data-stu-id="4f627-117">On the **File** menu, click **Open** &gt; **Project/Solution**, and then select **FleetManagement** **solution** from the desktop folder.</span></span> <span data-ttu-id="4f627-118">ソリューション ファイルがコンピュータにない場合は、作成手順が「[チュートリアル: AOT のフリート管理モデルからフリート管理ソリューションを作成する](https://community.dynamics.com/ax/b/newdynamicsax/archive/2016/05/19/tutorial-create-a-fleet-management-solution-file-out-of-the-fleet-management-models-in-the-aot)」に記載されています。</span><span class="sxs-lookup"><span data-stu-id="4f627-118">If the solution file is not on your computer, the steps to create it are listed in [Tutorial: Create a Fleet Management solution file out of the Fleet Management models in the AOT](https://community.dynamics.com/ax/b/newdynamicsax/archive/2016/05/19/tutorial-create-a-fleet-management-solution-file-out-of-the-fleet-management-models-in-the-aot).</span></span>
1.  <span data-ttu-id="4f627-119">**ソリューション エクスプローラー** で、**フリート管理** ソリューションを右クリックして **追加** をポイントしてから **新規プロジェクト** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="4f627-119">In **Solution Explorer**, right-click the **Fleet Management** solution, point to **Add**, and then click **New Project**.</span></span>
1.  <span data-ttu-id="4f627-120">作成するプロジェクトタイプとして **Finance and Operations** を選択します。</span><span class="sxs-lookup"><span data-stu-id="4f627-120">Choose **Finance and Operations** as the project type to create.</span></span>
1.  <span data-ttu-id="4f627-121">この新しいプロジェクトに *FleetManagementUnitTestSample* と名前を付け、デスクトップの FleetManagement フォルダー (C:\Users\Public\Desktop\FleetManagement) を場所として指定してから、**OK** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="4f627-121">Name this new project *FleetManagementUnitTestSample*, specify the FleetManagement folder on the desktop (C:\Users\Public\Desktop\FleetManagement) as the location, and then click **OK**.</span></span> 
1.  <span data-ttu-id="4f627-122">**ソリューション エクスプローラー** で、新規プロジェクトを右クリックしてから **プロパティ** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="4f627-122">In **Solution Explorer**, right-click the new project, and then click **Properties**.</span></span>
1.  <span data-ttu-id="4f627-123">**Model** プロパティを **FleetManagementUnitTests** に設定し、**OK** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="4f627-123">Set the **Model** property to **FleetManagementUnitTests**, and then click **OK**.</span></span> 

    <span data-ttu-id="4f627-124">[![モデル プロパティ](./media/56.png)](./media/56.png)</span><span class="sxs-lookup"><span data-stu-id="4f627-124">[![Model property](./media/56.png)](./media/56.png)</span></span>

1.  <span data-ttu-id="4f627-125">FleetManagementUnitTestSample プロジェクトを右クリックして **追加** をポイントしてから **新しい項目** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="4f627-125">Right-click the FleetManagementUnitTestSample project, point to **Add**, and then click **New Item**.</span></span>
1.  <span data-ttu-id="4f627-126">**新しい項目の追加** ウィンドウで、追加する要素のタイプとして **クラス** を選択します。</span><span class="sxs-lookup"><span data-stu-id="4f627-126">In the **Add New Item** window, select **Class** as the type of element to add.</span></span> <span data-ttu-id="4f627-127">新しいクラスに FMUnitTestSample と名前を付けてから、**追加** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="4f627-127">Name the new class FMUnitTestSample, and then click **Add**.</span></span> 

    <span data-ttu-id="4f627-128">[![新しい品目を追加](./media/57.png)](./media/57.png)</span><span class="sxs-lookup"><span data-stu-id="4f627-128">[![Add new item](./media/57.png)](./media/57.png)</span></span>

1. <span data-ttu-id="4f627-129">新しいクラスのコードの最初の行で、クラスが SysTestCase クラスを拡張していることを示します。</span><span class="sxs-lookup"><span data-stu-id="4f627-129">In the first line of the code for the new class, indicate that the class extends the SysTestCase class.</span></span>
1. <span data-ttu-id="4f627-130">クラスのメソッドを定義する次のコードを追加します。</span><span class="sxs-lookup"><span data-stu-id="4f627-130">Add the following code to define the methods for the class.</span></span> <span data-ttu-id="4f627-131">これらのメソッドは、2 つの追加テストを定義します。</span><span class="sxs-lookup"><span data-stu-id="4f627-131">These methods define two additional tests.</span></span>

    ```xpp
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
    ```

1. <span data-ttu-id="4f627-132">新しいクラスを保存します。</span><span class="sxs-lookup"><span data-stu-id="4f627-132">Save the new class.</span></span> <span data-ttu-id="4f627-133">保存が完了した後、**テスト エクスプローラー** に追加 2 つのテスト ケースが表示されます。</span><span class="sxs-lookup"><span data-stu-id="4f627-133">After the save is complete, you will see the additional two test cases in **Test Explorer**.</span></span> <span data-ttu-id="4f627-134">**ソリューション エクスプローラー** で FleetManagementUnitTestSample プロジェクトを右クリックし、**ビルド** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="4f627-134">Right-click on the FleetManagementUnitTestSample project in **Solution Explorer**, and then click **Build.**</span></span>
1.  <span data-ttu-id="4f627-135">**表示** メニューで、**テスト エクスプローラー** を開きます。</span><span class="sxs-lookup"><span data-stu-id="4f627-135">On the **View** menu, open **Test Explorer**.</span></span> 
1. <span data-ttu-id="4f627-136">特定のテスト ケースを実行するには、**選択したテストの実行** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="4f627-136">Click **Run selected test** to execute specific test case.</span></span>
1. <span data-ttu-id="4f627-137">完了した後、テスト エクスプローラーにテストの結果が表示されます。</span><span class="sxs-lookup"><span data-stu-id="4f627-137">Test Explorer will show the results of test after it is complete.</span></span> 

    <span data-ttu-id="4f627-138">[![完了したテスト](./media/59-300x290.png)](./media/59.png)</span><span class="sxs-lookup"><span data-stu-id="4f627-138">[![Completed test](./media/59-300x290.png)](./media/59.png)</span></span>

## <a name="test-isolation"></a><span data-ttu-id="4f627-139">テストの分離</span><span class="sxs-lookup"><span data-stu-id="4f627-139">Test isolation</span></span>
<span data-ttu-id="4f627-140">テストが高い価値を持つためには、信頼できるものでなければなりません。</span><span class="sxs-lookup"><span data-stu-id="4f627-140">For a test to be of high value it must be reliable.</span></span> <span data-ttu-id="4f627-141">テストは、他のテストなどの他の要因に関係なく、常に成功または失敗します。</span><span class="sxs-lookup"><span data-stu-id="4f627-141">A test will pass or fail consistently, independent of other factors such as other tests.</span></span> <span data-ttu-id="4f627-142">信頼性の低いテストの典型的な原因の 1 つとして、ダウンストリーム テストに影響を与えるデータベースに残されたデータなどのリーク状態があります。</span><span class="sxs-lookup"><span data-stu-id="4f627-142">One typical cause of unreliable tests is leaking state, such as data left behind in the data base that influences downstream tests.</span></span> <span data-ttu-id="4f627-143">このタイプの問題を回避するには、```SysTestTransaction``` 属性を使用できます。</span><span class="sxs-lookup"><span data-stu-id="4f627-143">To prevent this type of issue, you can use the ```SysTestTransaction``` attribute.</span></span>

|  <span data-ttu-id="4f627-144">TestTransactionMode</span><span class="sxs-lookup"><span data-stu-id="4f627-144">TestTransactionMode</span></span> | <span data-ttu-id="4f627-145">説明</span><span class="sxs-lookup"><span data-stu-id="4f627-145">Description</span></span>  |
|---|---|
| <span data-ttu-id="4f627-146">AutoRollback</span><span class="sxs-lookup"><span data-stu-id="4f627-146">AutoRollback</span></span> | <span data-ttu-id="4f627-147">**既定**。</span><span class="sxs-lookup"><span data-stu-id="4f627-147">**Default**.</span></span> <span data-ttu-id="4f627-148">これにより、最適な分離が提供されます。</span><span class="sxs-lookup"><span data-stu-id="4f627-148">This provides the best isolation.</span></span><br><br> <span data-ttu-id="4f627-149">すべてのトランザクションは、SQL セーブ ポイントを使用してロールバックされ、すべてのデータベース ステートメントは、ユーザー接続を含む、メインの接続にルーティングされます。</span><span class="sxs-lookup"><span data-stu-id="4f627-149">All transactions are rolled back using SQL save points, and all database statements are routed to the main connection, including user connections.</span></span> <span data-ttu-id="4f627-150">データは保存されません。</span><span class="sxs-lookup"><span data-stu-id="4f627-150">No data will be persisted.</span></span> |
| <span data-ttu-id="4f627-151">LegacyRollback</span><span class="sxs-lookup"><span data-stu-id="4f627-151">LegacyRollback</span></span> | <span data-ttu-id="4f627-152">すべての挿入ステートメントは、クリーンアップ時に追跡および削除されます。</span><span class="sxs-lookup"><span data-stu-id="4f627-152">All insert statements are tracked and deleted during clean-up.</span></span><br><br> <span data-ttu-id="4f627-153">すべての挿入ステートメントは、行ごとにダウングレードされます。</span><span class="sxs-lookup"><span data-stu-id="4f627-153">All insert statements are downgraded to row-by-row.</span></span> <span data-ttu-id="4f627-154">典型的なユース ケースの 1 つは、ユーザー接続または同時実行シナリオをテストする場合です。</span><span class="sxs-lookup"><span data-stu-id="4f627-154">One typical use case is when testing user connections or concurrency scenarios.</span></span> <span data-ttu-id="4f627-155">この分離レベルは、セットアップ データのクリーンアップをするため、推奨は各テスト メソッドを ttsBegin と ttsAbort でラップすることです。</span><span class="sxs-lookup"><span data-stu-id="4f627-155">This isolation level will clean up setup data, and the recommendation is to wrap each test method in a ttsBegin and ttsAbort.</span></span> |
| <span data-ttu-id="4f627-156">LegacyRollbackWithUpdateTracking</span><span class="sxs-lookup"><span data-stu-id="4f627-156">LegacyRollbackWithUpdateTracking</span></span> | <span data-ttu-id="4f627-157">すべての更新、削除、挿入ステートメントは、クリーンアップ中に追跡され、元に戻されます。</span><span class="sxs-lookup"><span data-stu-id="4f627-157">All update, delete, and insert statements are tracked and reverted during cleanup.</span></span><br><br> <span data-ttu-id="4f627-158">すべての挿入、更新、削除ステートメントが行ごとに追跡され、ダウングレードされます。</span><span class="sxs-lookup"><span data-stu-id="4f627-158">All insert, update, and delete statements are tracked and downgraded to row-by-row.</span></span> <span data-ttu-id="4f627-159">これは、最も遅い分離レベルです。</span><span class="sxs-lookup"><span data-stu-id="4f627-159">This is the slowest isolation level.</span></span> |
| <span data-ttu-id="4f627-160">None</span><span class="sxs-lookup"><span data-stu-id="4f627-160">None</span></span> | <span data-ttu-id="4f627-161">**デバッグにのみ使用します**。</span><span class="sxs-lookup"><span data-stu-id="4f627-161">**Only use for debugging**.</span></span> <span data-ttu-id="4f627-162">これは分離を提供しません。</span><span class="sxs-lookup"><span data-stu-id="4f627-162">This provides no isolation.</span></span><br><br> <span data-ttu-id="4f627-163">この設定は、テストで作成されたデータを通常のユーザー インターフェイスを使用してナビゲートできるため、一時的にテストをデバッグする場合に役立ちます。</span><span class="sxs-lookup"><span data-stu-id="4f627-163">This setting can be useful to temporarily to debug a test, as it allows you to use the regular user interface to navigate the data that the test created.</span></span> |

<span data-ttu-id="4f627-164">例:</span><span class="sxs-lookup"><span data-stu-id="4f627-164">Example:</span></span>

```xpp    
    [SysTestTransaction(TestTransactionMode::LegacyRollback)]
    class MyTestSample extends SysTestCase
```    

## <a name="test-module-creation-to-manage-test-code-and-formadaptors"></a><span data-ttu-id="4f627-165">テスト コードと FormAdaptors を管理するテスト モジュールの作成</span><span class="sxs-lookup"><span data-stu-id="4f627-165">Test module creation to manage test code and FormAdaptors</span></span>
<span data-ttu-id="4f627-166">テスト コードをまとめて管理しやすくするためにテスト固有のモジュールを作成しています。</span><span class="sxs-lookup"><span data-stu-id="4f627-166">Creating a test specific module helps to keep test code together and manageable.</span></span>

1. <span data-ttu-id="4f627-167">**Visual Studio** を開き、**Dynamics 365** > **モデル管理** > **モデルの作成** に移動します。</span><span class="sxs-lookup"><span data-stu-id="4f627-167">Open **Visual Studio** and go to **Dynamics 365** > **Model Management** > **Create model**.</span></span>

2. <span data-ttu-id="4f627-168">モデル名を入力し、レイヤーを選択し、次に追加詳細を入力します。</span><span class="sxs-lookup"><span data-stu-id="4f627-168">Enter the model name, select the layer, and then enter any additional details.</span></span> <span data-ttu-id="4f627-169">テスト モジュールの名前に **テスト** という語を含めることをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="4f627-169">Note that it's a good idea to include the word **Test** in the name of the test module.</span></span> <span data-ttu-id="4f627-170">既定のビルド定義は、**テスト** という単語を含むすべてのテスト モジュールを検出するように設定されています。</span><span class="sxs-lookup"><span data-stu-id="4f627-170">The default build definition is configured to discover all test modules that contain the word **Test**.</span></span> 
   
3. <span data-ttu-id="4f627-171">このモデルは Application Platform/Foundation からのフォームを保持するため、以下に示すモデルへの参照を追加します。</span><span class="sxs-lookup"><span data-stu-id="4f627-171">Because this model holds forms from the Application Platform/Foundation, add references to models shown below.</span></span>

    <span data-ttu-id="4f627-172">[![モデル参照](./media/62-1024x786.png)](./media/62.png)</span><span class="sxs-lookup"><span data-stu-id="4f627-172">[![Model references](./media/62-1024x786.png)](./media/62.png)</span></span>

<span data-ttu-id="4f627-173">基本テスト モジュールを配置した後、タスク レコーダーの記録をインポートしてテスト コードを生成することができます。</span><span class="sxs-lookup"><span data-stu-id="4f627-173">After the base test module is in place, you can import a Task Recorder recording to generate test code.</span></span> <span data-ttu-id="4f627-174">タスク レコーダーの記録の XML をインポートするとき、FormAdaptors を使用してテスト コードが生成されます。</span><span class="sxs-lookup"><span data-stu-id="4f627-174">When you import a Task Recorder recording XML, test code is generated using FormAdaptors.</span></span> <span data-ttu-id="4f627-175">フォーム アダプターは、フォーム機能をテストするために使用される、強く定型化された API を提供するフォーム上のラッパー クラスです。</span><span class="sxs-lookup"><span data-stu-id="4f627-175">Form adaptors are wrapper classes over forms which provide strongly typed API that can be used to test form functionality.</span></span> <span data-ttu-id="4f627-176">組み込みのフォームの各パッケージの事前に生成した FormAdapters を含めました。</span><span class="sxs-lookup"><span data-stu-id="4f627-176">We have included pre-generated FormAdapters for each package for built-in forms.</span></span> <span data-ttu-id="4f627-177">テスト モジュールで、テスト コードを実行するヘルパー メソッドがある、パッケージおよび Test Essentials に対応するフォーム アダプタへの参照を追加します。</span><span class="sxs-lookup"><span data-stu-id="4f627-177">In the test module, add a reference to the corresponding Form Adaptor for packages and Test Essentials, which has helper methods to execute test code.</span></span>

## <a name="import-a-task-recorder-recording-into-visual-studio-to-generate-test-code"></a><span data-ttu-id="4f627-178">テスト コードを生成するために Visual Studio に記録しているタスク レコーダーをインポートします。</span><span class="sxs-lookup"><span data-stu-id="4f627-178">Import a Task Recorder recording into Visual Studio to generate test code</span></span>
<span data-ttu-id="4f627-179">タスク レコーダーの記録からテスト コードを生成して、ヘッドレス (非 UI) テストを実行することができます。</span><span class="sxs-lookup"><span data-stu-id="4f627-179">You can generate test code from Task Recorder recording to execute headless (non-UI) test.</span></span>

1. <span data-ttu-id="4f627-180">タスク レコーダーを使用してシナリオを記録します。</span><span class="sxs-lookup"><span data-stu-id="4f627-180">Record a scenario in by using Task Recorder.</span></span>

2. <span data-ttu-id="4f627-181"> Visual Studio にタスク記録をインポートするには、**Dynamics 365** > **アドイン** > **タスク記録のインポート** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="4f627-181">To import a Task Recording, in Visual Studio, click **Dynamics 365** > **Addins** > **Import Task Recording**.</span></span> 

3. <span data-ttu-id="4f627-182">**タスクの記録をインポート** ダイアログで、タスクの記録をインポートするテスト モジュール (ISVTestModule) を選択し、記録している xml ファイルを参照します。</span><span class="sxs-lookup"><span data-stu-id="4f627-182">In the **Import Task Recording** dialog, select the Test Module (ISVTestModule) under which you want to import task recording, and browse to recording xml file.</span></span> 

    <span data-ttu-id="4f627-183">[![テスト モジュール](./media/64-249x300.png)](./media/64.png)</span><span class="sxs-lookup"><span data-stu-id="4f627-183">[![Test module](./media/64-249x300.png)](./media/64.png)</span></span>

4. <span data-ttu-id="4f627-184">タスクの記録インポート プロセスは、Visual Studio IDE で表示できる SysTestAdapter および FormAdaptor に基づいてテスト コードを生成します。</span><span class="sxs-lookup"><span data-stu-id="4f627-184">The task recording import process generates test code that is based on the SysTestAdapter and FormAdaptor which can be viewed in Visual Studio IDE.</span></span> <span data-ttu-id="4f627-185">このステップの一部として生成されるテスト ソース コードをお客様が変更することを予定していません。</span><span class="sxs-lookup"><span data-stu-id="4f627-185">We do not expect you to change any test source code that is generated as part of this step.</span></span>
  
5. <span data-ttu-id="4f627-186">テスト コードが生成された後、テスト検出および実行のための Visual Studio オプションを設定します。</span><span class="sxs-lookup"><span data-stu-id="4f627-186">After the test code is generated, set up Visual Studio options for test discovery and execution:</span></span>
   - <span data-ttu-id="4f627-187">64 ビット コンピューターを使用する場合は、単体テストを実行し、64 ビット プロセスとしてコード カバレッジ情報を取得できます。</span><span class="sxs-lookup"><span data-stu-id="4f627-187">If you have a 64-bit machine, you can run unit tests and capture code coverage information as a 64-bit process.</span></span>
   - <span data-ttu-id="4f627-188">これを構成するには、**テスト**&gt;**テストの設定**&gt;**既定のプロセッサ アーキテクチャ** を選択し、**X64** を選択します。</span><span class="sxs-lookup"><span data-stu-id="4f627-188">To configure this, select **Test** &gt; **Test Settings** &gt; **Default Processor Architecture**, and then select **X64**.</span></span>
   - <span data-ttu-id="4f627-189">テストの実行エンジンが開き、テスト プロジェクト内のアセンブリをロックする状態が発生した可能性があります。</span><span class="sxs-lookup"><span data-stu-id="4f627-189">You might run into a situation in which the test execution engine opens and locks an assembly in your test project.</span></span> <span data-ttu-id="4f627-190">この場合、たとえば、アセンブリに対する変更を保存することはできません。</span><span class="sxs-lookup"><span data-stu-id="4f627-190">When this happens, you can’t for example, save changes to the assembly.</span></span> <span data-ttu-id="4f627-191">これを修正するには、**テスト**&gt;**テスト設定** を選択し、**テスト実行エンジンを実行し続ける** を選択します。</span><span class="sxs-lookup"><span data-stu-id="4f627-191">To fix this, select **Test** &gt; **Test Settings**, and then select **Keep Test Execution Engine Running**.</span></span> 
    - <span data-ttu-id="4f627-192">Visual Studio IDE で生成されたテスト コードがあるので、テストを検出してローカルで実行します。</span><span class="sxs-lookup"><span data-stu-id="4f627-192">Now that you have test code generated in Visual Studio IDE, it's time to discover the test and try executing them locally.</span></span>

6. <span data-ttu-id="4f627-193">メニュー オプションから、**テスト** &gt; **Windows** を選択し、**テスト エクスプ ローラー** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="4f627-193">From menu options, select **Test** &gt; **Windows**, and then click **Test Explorer**.</span></span> <span data-ttu-id="4f627-194">テスト エクスプローラー ウィンドウが開いた後、テスト コードからテストを検出し、次のように使用可能なすべてのテストを一覧表示します。</span><span class="sxs-lookup"><span data-stu-id="4f627-194">After the Test Explorer window is open, it will try to discover test from test code and list all the available tests as shown below.</span></span>

    <span data-ttu-id="4f627-195">[![テスト エクスプローラー](./media/67-1024x658.png)](./media/67.png)</span><span class="sxs-lookup"><span data-stu-id="4f627-195">[![Test explorer](./media/67-1024x658.png)](./media/67.png)</span></span>

7. <span data-ttu-id="4f627-196">テストを選択し、**実行** &gt; **選択されている実行** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="4f627-196">Select the test and then click **Run** &gt; **Execute selected**.</span></span> <span data-ttu-id="4f627-197">これにより、ローカルに展開された環境に対してテストが実行されます。</span><span class="sxs-lookup"><span data-stu-id="4f627-197">This will execute test against the locally deployed environment.</span></span> 

    <span data-ttu-id="4f627-198">[![選択の実行](./media/68-1024x652.png)](./media/68.png)</span><span class="sxs-lookup"><span data-stu-id="4f627-198">[![Execute selected](./media/68-1024x652.png)](./media/68.png)</span></span>

## <a name="integration-of-the-test-module-with-build-process"></a><span data-ttu-id="4f627-199">ビルド プロセスのあるテスト モジュールの統合</span><span class="sxs-lookup"><span data-stu-id="4f627-199">Integration of the test module with build process</span></span>
<span data-ttu-id="4f627-200">テスト モジュールがソース管理の一部である場合、ビルド プロセス テンプレートは、名前に **テスト** という単語を含むすべてのテスト モジュールを検出します。</span><span class="sxs-lookup"><span data-stu-id="4f627-200">After the test module is a part of source control, the build process template will discover all test modules, which contain the word **Test** in the name.</span></span> <span data-ttu-id="4f627-201">次の図は、Visual Studio Online の一部としてのビルドとテストの実行を示しています。</span><span class="sxs-lookup"><span data-stu-id="4f627-201">The following illustration shows build and test execution as part of Visual Studio Online.</span></span> 

<span data-ttu-id="4f627-202">[![ビルドおよびテストの実行](./media/69.png)](./media/69.png)</span><span class="sxs-lookup"><span data-stu-id="4f627-202">[![Build and test execution](./media/69.png)](./media/69.png)</span></span>


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]