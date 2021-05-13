---
title: Visual Studio のプロジェクトのテスト
description: このトピックでは、Visual Studio でテストするためのオプションについて説明します。
author: RobinARH
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Developer
ms.reviewer: rhaertle
ms.custom: 24161
ms.assetid: d94f46f0-cde2-47c3-8994-c79e609eabce
ms.search.region: Global
ms.author: shailesn
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: f5c9efcb61781b6e0943032965a0dc6ea3136331
ms.sourcegitcommit: e4992c57eea4c15ac052e9d65dddae625e3528f9
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/07/2021
ms.locfileid: "5866136"
---
# <a name="test-projects-in-visual-studio"></a>Visual Studio のプロジェクトのテスト

[!include [banner](../includes/banner.md)]

このトピックでは、Visual Studio でテストするためのオプションについて説明します。

カスタム単体テスト アダプターは、Visual Studio で利用可能です。 このアダプタを使用すると、テスト作成者は Visual Studio の標準の **Test Explorer** ウィンドウを使用して、X++ テストのスケジュールを立て、テスト結果を分析できます。 開発者は **SysTestAdaptor** を使用してテストを作成できます。 タスク レコーダーの記録からテスト コードを生成することもできます。 これらのテスト ケースは、検証のためにシステムを構築するために追加することができます。 

[![Visual Studio のテスト用オプションの図](./media/1_support.png)](./media/1_support.png)

## <a name="author-unitcomponent-test-code-by-using-the-systest-framework"></a>SysTest フレームワークを使用して単位またはコンポーネント テスト コードを作成
Visual Studio でプロジェクトを作成するときは、X++ 単体テストを追加できます。 **SysTestCase** を含むクラスを拡張し、その後 **SysTestMethodAttribute** 属性を追加するか、またはメソッド名に "test" を含むケースを接頭語として付けます。

```xpp
class FMUnitTestSample extends SysTestCase
{
    [SysTestMethod]
    public void testTotalsEngineConfig()
    {
    }
}
```

クラスを保存すると、C\# テストが表示されるのと同じように、テスト エクスプローラーに各テストが表示されます。 

[![テスト エクスプローラーに表示されるテストの例](./media/2_support.png)](./media/2_support.png) 

テスト エクスプローラーで、テストを実行したり、右クリックからの選択したテストの実行やデバッグによってテスト ケースをデバッグしたりできます。 

> [!NOTE]
> テストを実行する前に、テストが含まれるようプロジェクトを構築する必要があります。 

[![選択したテストを実行またはデバッグするための右クリックの例](./media/3_support.png)](./media/3_support.png) 

また、プロジェクト内のオブジェクトのための既存のテストを見つけることができます。 検索では、相互参照データを使用します。 プロジェクトでオブジェクトを右クリックし、**関連するテストの検出** を選択します。 このコマンドは、相互参照データを照会し、そのオブジェクトを参照するテストを返します。 テスト ケースのリストがテスト エクスプローラーに表示されます。 

[![テスト エクスプローラーに表示されるテスト ケースの例](./media/4_support.png)](./media/4_support.png) 

この機能を使用することにより、関連するすべてのテストを実行できます。 テスト エクスプローラーには、現在のプロジェクトのすべてのテストと参照されているオブジェクトのすべてのテストが含まれます。

## <a name="generate-test-code-by-importing-task-recorder-recordings-into-visual-studio"></a>Visual Studio に記録しているタスク レコーダーをインポートして、テスト コードを生成します。
タスク レコーダーの記録のために XML をインポートして、さまざまな業務プロセスのシナリオを検証するために使用できるテスト コードを生成することができます。 

[![インポート タスク記録 ダイアログ ボックスの例](./media/5_support.png)](./media/5_support.png) 

生成されたコードは SysTest フレームワークおよび FormAdaptors に基づいています。 FormAdaptors は、ページ上のラッパー クラスです。 これらは、ページ機能をテストするために使用できる強く型付けされたアプリケーション プログラミング インターフェイス (API) を提供します。 組み込みのページの各パッケージに、事前に生成した FormAdapters が含まれます。 テスト モジュールで、テスト コードを実行するヘルパー メソッドを含む、パッケージおよび「Test Essentials」に対応する FormAdaptor への参照を追加します。

## <a name="advanced-options"></a>詳細オプション

分類および実行のためのテストをフィルター処理する詳細オプションについては、[クラスおよびメソッドの属性を使用した SysTest フィルター処理](systest-filtering.md)を参照してください。


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]