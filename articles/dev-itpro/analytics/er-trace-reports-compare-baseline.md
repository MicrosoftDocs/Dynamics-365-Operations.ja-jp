---
title: 生成されたレポート結果を追跡し、ベースライン値と比較する
description: このトピックでは、ベースライン レポート値で生成された ER レポートの結果を比較する方法に関する情報を提供します。
author: NickSelin
manager: AnnBe
ms.date: 05/25/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 220314
ms.assetid: 2685df16-5ec8-4fd7-9495-c0f653e82567
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2018-04-01
ms.dyn365.ops.version: Release 8.0
ms.openlocfilehash: 7f7877ccaa0c45ab5f0032d6808280e3c47a43ca
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/29/2019
ms.locfileid: "317939"
---
# <a name="trace-generated-report-results-and-compare-them-with-baseline-values"></a>生成されたレポート結果を追跡し、ベースライン値と比較する

[!include[banner](../includes/banner.md)]

送信する電子ドキュメントを生成する ER 形式の結果を追跡できます。 トレースの生成が有効である場合 (ER ユーザー パラメーター**デバッグ モードで実行**)、ER レポートが実行されるたびに ER 形式実行ログで新しいトレース レコードが生成されます。 生成される各トレースには、次の情報が格納されます。

- 検証ルールによって生成されたすべての警告
- 検証ルールによって生成されたすべてのエラー
- トレース レコードの添付ファイルとして格納されるすべての生成されたファイル

任意の ER 形式の個々のベースライン アプリケーション ファイルを格納できます。 ファイルは、実行されるレポートの予期される結果の説明時にベースライン ファイルと見なされます。 トレースの生成がオンである間に実行された ER 形式に対してベースライン ファイルが使用可能な場合、トレースは、前述した詳細内容に加えて、ベースライン ファイルに生成された電子ドキュメントの比較の結果を格納します。 ワンクリックで、生成された電子ドキュメントおよびそのベースライン ファイルを単一の zip ファイルで取得することもできます。 Windiff などの外部ツールを使用して詳細な比較を行うことができます。

生成される電子ドキュメントが予想されるコンテンツを含むかどうかを分析するトレースを評価できます。 コード ベースが変更されたとき (たとえば、アプリケーションの新しいインスタンスに移行したとき、修正プログラム パッケージをインストールしたとき、またはコード変更を配置したとき)、ユーザー受け入れテスト (UAT) 環境でこの評価を行うことができます 。 この方法で、評価は使用される ER レポートの実行に影響しないことを確認できます。 多くの ER レポートについては、無人モードで評価を実行できます。

この機能の詳細については、**7.5.4.3 IT サービス/ソリューションのテスト (10679)** 業務プロセスの一部である、**ER レポートの生成および結果の比較 (第 1 部)** および **ER レポートの生成および結果の比較 (第 2 部)** タスク ガイドを再生し、[Microsoft ダウンロード センター](https://go.microsoft.com/fwlink/?linkid=874684) からダウンロードできます。 これらのタスク ガイドでは、生成される電子ドキュメントを評価するためにベースライン ファイルを使用して、ER フレームワークを構成するプロセスについて説明します。
