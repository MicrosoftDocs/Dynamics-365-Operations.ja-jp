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
ms.openlocfilehash: afe4f4323d1f90f5debebe36aa6ecda1df71f013
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/31/2021
ms.locfileid: "5745143"
---
# <a name="testing-and-validations"></a>テストと検証

[!include [banner](../includes/banner.md)]

このチュートリアルでは、テスト ケースを作成して実行する方法を説明します。

<a name="prerequisites"></a>前提条件
-------------

開発者トポロジを開発者およびビルト VM を使用して配置する必要があります。

## <a name="key-concepts"></a>重要な概念
-   SysTest フレームワークを使用して単位またはコンポーネントのテスト コードを作成します。
-   テストの分離
-   テスト コードと FormAdaptors を管理するテスト モジュールの作成。
-   テスト コードを生成するために Visual Studio に記録しているタスク レコーダーをインポートします。
-   ビルド マシンとテスト モジュールを統合します。

[![テスト モジュールの統合](./media/54.png)](./media/54.png)  

## <a name="use-systest-framework-to-author-unitcomponent-test-code"></a>SysTest フレームワークを使用して単位またはコンポーネントのテスト コードを作成
新しいテスト ケースを作成して、アプリケーションで機能をテストすることができます。

1.  Visual Studio を管理者としてオープンします。
1.  **ファイル** メニューで、**開く** &gt; **プロジェクト/ソリューション** をクリックし、デスクトップ フォルダーから **FleetManagement** **ソリューション** を選択します。 ソリューション ファイルがコンピュータにない場合は、作成手順が「[チュートリアル: AOT のフリート管理モデルからフリート管理ソリューションを作成する](https://community.dynamics.com/ax/b/newdynamicsax/archive/2016/05/19/tutorial-create-a-fleet-management-solution-file-out-of-the-fleet-management-models-in-the-aot)」に記載されています。
1.  **ソリューション エクスプローラー** で、**フリート管理** ソリューションを右クリックして **追加** をポイントしてから **新規プロジェクト** をクリックします。
1.  作成するプロジェクトタイプとして **Finance and Operations** を選択します。
1.  この新しいプロジェクトに *FleetManagementUnitTestSample* と名前を付け、デスクトップの FleetManagement フォルダー (C:\Users\Public\Desktop\FleetManagement) を場所として指定してから、**OK** をクリックします。 
1.  **ソリューション エクスプローラー** で、新規プロジェクトを右クリックしてから **プロパティ** をクリックします。
1.  **Model** プロパティを **FleetManagementUnitTests** に設定し、**OK** をクリックします。 

    [![モデル プロパティ](./media/56.png)](./media/56.png)

1.  FleetManagementUnitTestSample プロジェクトを右クリックして **追加** をポイントしてから **新しい項目** をクリックします。
1.  **新しい項目の追加** ウィンドウで、追加する要素のタイプとして **クラス** を選択します。 新しいクラスに FMUnitTestSample と名前を付けてから、**追加** をクリックします。 

    [![新しい品目を追加](./media/57.png)](./media/57.png)

1. 新しいクラスのコードの最初の行で、クラスが SysTestCase クラスを拡張していることを示します。
1. クラスのメソッドを定義する次のコードを追加します。 これらのメソッドは、2 つの追加テストを定義します。

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
            this.assertFalse(fmCar.validateField(Fieldnum("FMCarClass&quot;, &quot;NumberOfDoors")));

            fmCar.NumberOfDoors = 4;
            this.assertTrue(fmCar.validateField(Fieldnum("FMCarClass", "NumberOfDoors")));
        }
    }
    ```

1. 新しいクラスを保存します。 保存が完了した後、**テスト エクスプローラー** に追加 2 つのテスト ケースが表示されます。 **ソリューション エクスプローラー** で FleetManagementUnitTestSample プロジェクトを右クリックし、**ビルド** をクリックします。
1.  **表示** メニューで、**テスト エクスプローラー** を開きます。 
1. 特定のテスト ケースを実行するには、**選択したテストの実行** をクリックします。
1. 完了した後、テスト エクスプローラーにテストの結果が表示されます。 

    [![完了したテスト](./media/59-300x290.png)](./media/59.png)

## <a name="test-isolation"></a>テストの分離
テストが高い価値を持つためには、信頼できるものでなければなりません。 テストは、他のテストなどの他の要因に関係なく、常に成功または失敗します。 信頼性の低いテストの典型的な原因の 1 つとして、ダウンストリーム テストに影響を与えるデータベースに残されたデータなどのリーク状態があります。 このタイプの問題を回避するには、```SysTestTransaction``` 属性を使用できます。

|  TestTransactionMode | 説明  |
|---|---|
| AutoRollback | **既定**。 これにより、最適な分離が提供されます。<br><br> すべてのトランザクションは、SQL セーブ ポイントを使用してロールバックされ、すべてのデータベース ステートメントは、ユーザー接続を含む、メインの接続にルーティングされます。 データは保存されません。 |
| LegacyRollback | すべての挿入ステートメントは、クリーンアップ時に追跡および削除されます。<br><br> すべての挿入ステートメントは、行ごとにダウングレードされます。 典型的なユース ケースの 1 つは、ユーザー接続または同時実行シナリオをテストする場合です。 この分離レベルは、セットアップ データのクリーンアップをするため、推奨は各テスト メソッドを ttsBegin と ttsAbort でラップすることです。 |
| LegacyRollbackWithUpdateTracking | すべての更新、削除、挿入ステートメントは、クリーンアップ中に追跡され、元に戻されます。<br><br> すべての挿入、更新、削除ステートメントが行ごとに追跡され、ダウングレードされます。 これは、最も遅い分離レベルです。 |
| None | **デバッグにのみ使用します**。 これは分離を提供しません。<br><br> この設定は、テストで作成されたデータを通常のユーザー インターフェイスを使用してナビゲートできるため、一時的にテストをデバッグする場合に役立ちます。 |

例:

```xpp    
    [SysTestTransaction(TestTransactionMode::LegacyRollback)]
    class MyTestSample extends SysTestCase
```    

## <a name="test-module-creation-to-manage-test-code-and-formadaptors"></a>テスト コードと FormAdaptors を管理するテスト モジュールの作成
テスト コードをまとめて管理しやすくするためにテスト固有のモジュールを作成しています。

1. **Visual Studio** を開き、**Finance and Operations** > **モデル管理** > **モデルの作成** に移動します。

2. モデル名を入力し、レイヤーを選択し、次に追加詳細を入力します。 テスト モジュールの名前に **テスト** という語を含めることをお勧めします。 既定のビルド定義は、**テスト** という単語を含むすべてのテスト モジュールを検出するように設定されています。 
   
3. このモデルは Application Platform/Foundation からのフォームを保持するため、以下に示すモデルへの参照を追加します。

    [![モデル参照](./media/62-1024x786.png)](./media/62.png)

基本テスト モジュールを配置した後、タスク レコーダーの記録をインポートしてテスト コードを生成することができます。 タスク レコーダーの記録の XML をインポートするとき、FormAdaptors を使用してテスト コードが生成されます。 フォーム アダプターは、フォーム機能をテストするために使用される、強く定型化された API を提供するフォーム上のラッパー クラスです。 組み込みのフォームの各パッケージの事前に生成した FormAdapters を含めました。 テスト モジュールで、テスト コードを実行するヘルパー メソッドがある、パッケージおよび Test Essentials に対応するフォーム アダプタへの参照を追加します。

## <a name="import-a-task-recorder-recording-into-visual-studio-to-generate-test-code"></a>テスト コードを生成するために Visual Studio に記録しているタスク レコーダーをインポートします。
タスク レコーダーの記録からテスト コードを生成して、ヘッドレス (非 UI) テストを実行することができます。

1. タスク レコーダーを使用してシナリオを記録します。

2. Visual Studio にタスク記録をインポートするには、**Finance and Operations** > **アドイン** > **タスク記録をインポート** をクリックします。 

3. **タスクの記録をインポート** ダイアログで、タスクの記録をインポートするテスト モジュール (ISVTestModule) を選択し、記録している xml ファイルを参照します。 

    [![テスト モジュール](./media/64-249x300.png)](./media/64.png)

4. タスクの記録インポート プロセスは、Visual Studio IDE で表示できる SysTestAdapter および FormAdaptor に基づいてテスト コードを生成します。 このステップの一部として生成されるテスト ソース コードをお客様が変更することを予定していません。
  
5. テスト コードが生成された後、テスト検出および実行のための Visual Studio オプションを設定します。
   - 64 ビット コンピューターを使用する場合は、単体テストを実行し、64 ビット プロセスとしてコード カバレッジ情報を取得できます。
   - これを構成するには、**テスト**&gt;**テストの設定**&gt;**既定のプロセッサ アーキテクチャ** を選択し、**X64** を選択します。
   - テストの実行エンジンが開き、テスト プロジェクト内のアセンブリをロックする状態が発生した可能性があります。 この場合、たとえば、アセンブリに対する変更を保存することはできません。 これを修正するには、**テスト**&gt;**テスト設定** を選択し、**テスト実行エンジンを実行し続ける** を選択します。 
    - Visual Studio IDE で生成されたテスト コードがあるので、テストを検出してローカルで実行します。

6. メニュー オプションから、**テスト** &gt; **Windows** を選択し、**テスト エクスプ ローラー** をクリックします。 テスト エクスプローラー ウィンドウが開いた後、テスト コードからテストを検出し、次のように使用可能なすべてのテストを一覧表示します。

    [![テスト エクスプローラー](./media/67-1024x658.png)](./media/67.png)

7. テストを選択し、**実行** &gt; **選択されている実行** をクリックします。 これにより、ローカルに展開された環境に対してテストが実行されます。 

    [![選択の実行](./media/68-1024x652.png)](./media/68.png)

## <a name="integration-of-the-test-module-with-build-process"></a>ビルド プロセスのあるテスト モジュールの統合
テスト モジュールがソース管理の一部である場合、ビルド プロセス テンプレートは、名前に **テスト** という単語を含むすべてのテスト モジュールを検出します。 次の図は、Visual Studio Online の一部としてのビルドとテストの実行を示しています。 

[![ビルドおよびテストの実行](./media/69.png)](./media/69.png)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]