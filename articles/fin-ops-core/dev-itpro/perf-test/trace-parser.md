---
title: Trace Parser を使用した問題点の診断およびパフォーマンスの分析
description: このトピックでは、トレース パーサーを使用してトレースを操作し、展開におけるパフォーマンスを分析する方法について説明します。
author: RobinARH
manager: AnnBe
ms.date: 10/19/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Developer
ms.reviewer: rhaertle
ms.custom: 13441
ms.assetid: eb0fbbaf-07d4-4a02-85e8-0d4f7920a0b9
ms.search.region: Global
ms.author: chwolf
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 6a991363847ab1996d07c0ab3c0f7aaf419a9bbf
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 12/05/2020
ms.locfileid: "4680428"
---
# <a name="diagnose-issues-and-analyze-performance-by-using-trace-parser"></a>Trace Parser を使用した問題点の診断およびパフォーマンスの分析

[!include [banner](../includes/banner.md)]

このトピックでは、トレース パーサーを使用してトレースを操作し、展開におけるパフォーマンスを分析する方法について説明します。 Trace Parser を使用すると、さまざまな種類のエラーを見つけて診断することができます。 また、ツールを使用して X++ メソッドの実行、および実行コール ツリーを視覚化することができます。

> [!NOTE]
> Trace parser には Microsoft Dynamics AX 2012 と類似する機能が多数あります。 詳細については、 [Dynamics Ax Performance チーム ブログ](https://blogs.msdn.com/axperf) を参照してください。

## <a name="finding-the-trace-parser"></a>Trace Parser の検索
トレース パーサーには、開発者展開または VHD があらかじめインストールされている必要があります。 インストール場所は **C:\\Program Files (x86)\\Microsoft Dynamics Trace Parser** です。 インストールされていない場合は、インストーラーを **C:\\PerfSDK\\PerfTools\\traceparser.msi** から実行することができます。

## <a name="capturing-events"></a>イベントのキャプチャ
トレース パーサーで分析するデータを取得するには、2 つの方法があります。 次のものが含まれます。

-   ローカルのインストールからイベントをキャプチャします。
    -   **トレースの選択** ウィンドウが開いていない場合、**ファイル** メニューに移動し、**トレースを開く** をクリックします。 **追跡の選択** ウィンドウで、**イベントのキャプチャ** をクリックします。 プロバイダーを選択して、**開始** をクリックします。 Trace Parser ツールは、すべてのプロバイダーのリッスンとイベントのキャプチャを開始します。 **停止およびインポート** をクリックするとキャプチャは停止します。
-   Logman などのツールを使用してキャプチャされた、既存の ETL(Windows イベント) ファイルを開きます。 

    [![開いている Windows イベントのファイルの例](./media/1_desktop.png)](./media/1_desktop.png)

## <a name="viewing-traces"></a>トレースの表示
**タイムライン ビュー** タイムライン タブは、Trace Parser にトレースをインポートした後に表示される最初のタブです。 このタブは、次の図に表示されます。 

[![[タイムライン] タブの情報の例](./media/2_desktop.png)](./media/2_desktop.png) 

**タイムライン** タブには、次の主要なコンポーネントがあります。

-   **グループ化を選択** ドロップダウンでは、さまざまなカテゴリ (顧客 ID、ユーザー名、セッション名など) に基づいてグループ化できます。[グループ化] には、イベントの最大および最小タイムスタンプ、イベントの合計数、グループ内の最下位イベント レベルが表示されます。
-   スレッドまたはスレッドではないビューのすべてのイベントのリスト。
-   選択したイベントに表示されるプロパティ グリッド。
-   選択したすべてのイベントのタイムライン チャートです。
-   イベントのフィルター処理。
-   セッション分析メモ。

**呼び出しツリーの表示** **呼び出しツリー** タブを選択すると、すべての X++ メソッドの呼び出しツリーが表示されます。 タブは、次に示します。 

[呼び出しツリー タブ](./media/3_desktop.png)に表示される情報の例 (./media/3_desktop.png) 

デスクトップ同様に、**X++** タブを表示し、すべての X++ メソッドの一覧を表示することができます。 包括的/排他的な期間、RPC、データベース呼び出しなどのフィールドでソートされます。 これらは Trace Parser の対応するタブに類似しており、同じ動作をすることに注意してください。

<a name="additional-resources"></a>追加リソース
--------

[開発およびカスタマイズのホーム ページ](../dev-tools/developer-home-page.md)



