---
title: "実行時間の長いレポートがタイムアウトしないようにする"
description: "この記事では、長時間実行されるレポートがタイムアウトするのを防ぐのに役立つヒントを紹介します。"
author: TJVass
manager: AnnBe
ms.date: 09/14/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Developer
ms.reviewer: robinr
ms.search.scope: Operations
ms.custom: 20521
ms.assetid: 74ffc94a-188f-4198-a4b0-f949ec4886cb
ms.search.region: Global
ms.author: tjvass
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 879eb9f2a63a8514791f74965005ed3e22bc0de7
ms.openlocfilehash: 4a4cbe23771105cf42bf172d2d615281cc106a9d
ms.contentlocale: ja-jp
ms.lasthandoff: 04/20/2018

---

# <a name="help-prevent-long-running-reports-from-timing-out"></a>実行時間の長いレポートがタイムアウトしないようにする

[!include [banner](../includes/banner.md)]

この記事では、長時間実行されるレポートがタイムアウトするのを防ぐのに役立つヒントを紹介します。 

ページ設定されたレポートおよびドキュメントは、Microsoft SQL Server Reporting Services を使用して生成されます。 Reporting Services は、Windows Communication Foundation (WCF) を使って AOS と通信するカスタム拡張機能を使うことにより、Application Object Server (AOS) からレポート データを取得します。 データセットのサイズと生成されるレポートの複雑さは、レポートの表示に必要な時間に影響する可能性があります。 また、さまざまなタイムアウトおよびその他のしきい値に達すると、レポートの生成が失敗する可能性があります。 展開におけるサービスのタイムアウトは固定されており、対話型の接続を 10 分に制限します。 このサービスのタイムアウト制限を超えるデータ セット生成プロセスは完了しません。 この記事では、実行時間の長いレポートをサポートするための拡張機能について説明します。 これらの拡張機能は、プロセスが 10 分のサービス タイム アウト制限を超えていても長時間実行されるレポートを生成できるようにします。

## <a name="preprocess-the-data-source"></a>データ ソースの前処理
レポートでレポートのデータ プロバイダー (RDP) を使用してデータを取得している場合、レポートは、事前処理 RDP クラスをデータ ソースとして使用するために変更される必要があります。 この方法では、処理ロジックが Reporting Services に対して呼び出しが行われる前に呼び出されます。 RDP クラスの詳細については、[レポート データにアクセスするレポートのデータ プロバイダー クラスを使用する](http://technet.microsoft.com/library/66667d57-37b1-48a8-90a1-ab8231698463(AX.60).aspx) および [レポートのプログラム ガイド](http://technet.microsoft.com/library/1a6cb21f-e665-45ef-8bf7-4df31e6ca0b7(AX.60).aspx) を参照してください。 

[![レポート タイムアウト](./media/report-timeouts.png)](./media/report-timeouts.png) 

## <a name="how-do-i-migrate-a-regular-rdp-to-a-pre-process-data-access-solution-by-using-tempdb"></a>TempDB を使用して、通常の RDP を事前処理されたデータ アクセス ソリューションに移行するにはどうすればよいですか。

1.  RDP 基本クラスを **SRSReportDataProviderBase** から **SRSReportDataProviderPreProcessTempDB** に変更します。
2.  テーブル タイプを **InMemory** から **TempDB** に更新します。
3.  レポートの RDP クラスをリビルドします。
4.  レポート デザイナーで RDP クラスにリンクされているデータ ソースを復元します。
5.  レポートを再配置します。
6.  **コントローラー** クラスを導入してレポートを実行します。
7.  レポートの代わりに **Controller** クラスを指すように出力メニュー項目を更新します。

次のビデオはそのプロセスを示しています。 

> [!ビデオ https://www.youtube.com/embed/6tdQtHV2WAc

## <a name="use-batch-processing"></a>バッチ処理の使用
大量のデータを含む明細書またはレポートを印刷するときのパフォーマンスを向上させるには、バッチ処理を使用します。 バッチ処理を使用すると、特定のタスクをバッチ ジョブとして実行した後、そのバッチ ジョブを、別のコンピューター (バッチ サーバー) で実行されるようにスケジュールすることができます。 これらのタスクの処理をバッチ サーバーに移すことによって、クライアント コンピューターのレポートのパフォーマンスが向上します。 また、各バッチ サイズを制限するために範囲制限を適用できます。 

パフォーマンスをさらに向上させるには、1 つの大きなバッチを送信しないでください。 代わりに、同時に別のサーバーで処理するための複数の小さいバッチを送信します。 多くのタスクをバッチ ジョブの一部として実行できます。 詳細については、[バッチ処理の概要](../sysadmin/batch-processing-overview.md) を参照してください。




