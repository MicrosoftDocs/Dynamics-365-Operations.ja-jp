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
ms.openlocfilehash: 428030a443eab41adb7aa2c48e5b9e7112f05ffe
ms.sourcegitcommit: 27a98a7a0f1d2623f5236a88066f483def30889c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/01/2019
ms.locfileid: "1833248"
---
# <a name="test-projects-in-visual-studio"></a>Visual Studio のプロジェクトのテスト

[!include [banner](../includes/banner.md)]

このトピックでは、Visual Studio でテストするためのオプションについて説明します。

カスタム単体テスト アダプターは、Visual Studio で利用可能です。 このアダプタを使用すると、テスト作成者は Visual Studio の標準の **Test Explorer** ウィンドウを使用して、X++ テストのスケジュールを立て、テスト結果を分析できます。 開発者は **SysTestAdaptor** を使用してテストを作成できます。 タスク レコーダーの記録からテスト コードを生成することもできます。 これらのテスト ケースは、検証のためにシステムを構築するために追加することができます。 

[![1\_サポート](./media/1_support.png)](./media/1_support.png)

## <a name="author-unitcomponent-test-code-by-using-the-systest-framework"></a>SysTest フレームワークを使用して単位またはコンポーネント テスト コードを作成
Visual Studio でプロジェクトを作成するときは、X++ 単体テストを追加できます。 **SysTestCase** を含むクラスを拡張し、その後 **SysTestMethodAttribute** 属性を追加するか、またはメソッド名に "test" を含むケースを接頭語として付けます。

    class FMUnitTestSample extends SysTestCase
    {
        [SysTestMethod]
        public void testTotalsEngineConfig()
        {
        }
    }

クラスを保存すると、C\# テストが表示されるのと同じように、テスト エクスプローラーに各テストが表示されます。 

[![2\_サポート](./media/2_support.png)](./media/2_support.png) 

テスト エクスプローラーで、テストを実行したり、右クリックからの選択したテストの実行やデバッグによってテスト ケースをデバッグしたりできます。 **注記:** テストを実行する前に、テストが含まれるように、プロジェクトを構築する必要があります。 

[![3\_サポート](./media/3_support.png)](./media/3_support.png) 

また、プロジェクト内のオブジェクトのための既存のテストを見つけることができます。 検索では、相互参照データを使用します。 プロジェクトでオブジェクトを右クリックし、**関連するテストの検出** を選択します。 このコマンドは、相互参照データを照会し、そのオブジェクトを参照するテストを返します。 テスト ケースのリストがテスト エクスプローラーに表示されます。 

[![4\_サポート](./media/4_support.png)](./media/4_support.png) 

この機能を使用することにより、関連するすべてのテストを実行できます。 テスト エクスプローラーには、現在のプロジェクトのすべてのテストと参照されているオブジェクトのすべてのテストが含まれます。

## <a name="generate-test-code-by-importing-task-recorder-recordings-into-visual-studio"></a>Visual Studio に記録しているタスク レコーダーをインポートして、テスト コードを生成します。
タスク レコーダーの記録のために XML をインポートして、さまざまな業務プロセスのシナリオを検証するために使用できるテスト コードを生成することができます。 

[![5\_サポート](./media/5_support.png)](./media/5_support.png) 

生成されたコードは SysTest フレームワークおよび FormAdaptors に基づいています。 FormAdaptors は、ページ上のラッパー クラスです。 これらは、ページ機能をテストするために使用できる強く型付けされたアプリケーション プログラミング インターフェイス (API) を提供します。 組み込みのページの各パッケージに、事前に生成した FormAdapters が含まれます。 テスト モジュールで、テスト コードを実行するヘルパー メソッドを含む、パッケージおよび「Test Essentials」に対応する FormAdaptor への参照を追加します。

## <a name="advanced-options"></a>詳細オプション

分類および実行のためのテストをフィルター処理する詳細オプションは、[systest-filtering.md] を参照してください。
