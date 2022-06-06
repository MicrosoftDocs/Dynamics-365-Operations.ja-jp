---
title: API スループットの最大化
description: このトピックでは、サービス保護アプリケーション プログラミング インターフェイス (API) の制限に対するスロットル応答の管理と、API スループットの最大限化に役立つ戦略について説明します。
author: jaredha
ms.date: 05/04/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Developer
ms.reviewer: sericks
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: jaredha
ms.search.validFrom: 2022-04-16
ms.dyn365.ops.version: Platform update 52
ms.openlocfilehash: e23720cf67a60982df1c61257fcb0ff58033335d
ms.sourcegitcommit: 04e6c1c9400e1b582180cf3e0e4767434e736c26
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/05/2022
ms.locfileid: "8712790"
---
# <a name="maximize-api-throughput"></a>API スループットの最大化

[!include [banner](../includes/banner.md)]

このトピックでは、サービス保護アプリケーション プログラミング インターフェイス (API) の制限に対するスロットル応答の管理と、API スループットの最大限化に役立つ戦略について説明します。

最短期間でほとんどのデータを移動するためにスループットに優先順位を付ける必要があるアプリケーションがある場合、適用できるいくつかの戦略があります。

## <a name="let-the-server-tell-you-when-to-retry-the-request"></a>要求を再試行するタイミングをサーバーに指示させる

一度に送信する要求の数を計算しようとしないでください。 環境ごとに異なる場合があります。 限界に達するまで、リクエストを送信するレートを徐々に上げていきます。 次に、サービス保護 API 制限の **再試行** 間隔の値に依存して、送信するタイミングを指示します。 この値は、スループットの合計を可能な限り最も高いレベルで維持するのに役立ちます。 

詳細については、[再試行操作](service-protection-retry-operations.md) を参照してください。

## <a name="use-multiple-threads"></a>複数のスレッドの使用

個々の操作が比較的速い場合、アプリケーションは同時実行スレッドの数の上限を使用して、パフォーマンスを大幅に向上させることができます。 処理するデータの性質によっては、最適なスループットを実現するためにスレッドの数を調整する必要がある場合があります。

## <a name="distribute-workloads-across-multiple-service-principals"></a>複数のサービス プリンシパル間でのワークロードの配分

ユーザーベースのサービス保護 API の制限は、ユーザーごとに実装されます。 統合が単一のサービス プリンシパルを使用して大規模なバルク データ操作を実行している場合や、単一のサービス プリンシパルを使用してすべてのユーザー要求をサーバーに送信する対話型のクライアント アプリケーションの場合は、サービス保護 API の制限にかなり迅速に到達できます。 複数のサービス プリンシパル間でワークロードを小さなバッチで分配することで、この問題を防ぐのに役立ちます。

## <a name="avoid-large-batches"></a>大きなバッチを避ける

*バッチ処理* とは、単一の要求に対して複数の操作を送信するプロセスを指します。 ほとんどのシナリオは単一の要求が送信され、高い並列度がある場合に最速となります。 バッチ サイズによってパフォーマンスが向上すると考える場合は、小さなバッチ サイズから開始し、操作を再試行する必要があるというサービス保護 API 制限エラーの受信を開始するまで同時実行数を増やすのが最良の戦略です。 財務と運用アプリでは、バッチ サイズが 5,000 操作に限定されます。

財務と運用アプリのサービス エンドポイントを持つバッチ要求の詳細については、[バッチ要求](../data-entities/odata.md#batch-requests) を参照してください。

## <a name="remove-the-affinity-cookie"></a>アフィニティ cookie の削除

Azure のサービスに接続すると、応答を含む cookie が返されます。 容量管理によって他のサーバーに強制的に移動させられない限り、後続のすべての要求は同じサーバーにルーティングされます。 cookie を削除すると、送信するすべての要求が、適格なサーバーのいずれかにルーティングされます。 したがって、サーバーごとに制限が適用されるため、スループットは向上します。 この戦略により、使用可能なサーバーがあればより多くのサーバーを使用できます。

> [!NOTE]
> この戦略は、スループットを最適化しようとしているアプリケーションでのみ使用する必要があります。 再作成が必要なキャッシュされたデータを再利用できるので、対話型のクライアント アプリケーションはアフィニティ cookie からメリットを受けられます。 データを再作成する必要がある場合、パフォーマンスに影響します。

次のコードでは、Web サービスを使用して **HttpClient** を初期化するときに cookie を無効にする方法を示します。 カスタムの **HttpMessageHandler** を使用して認証を管理する必要があります。

```C#
HttpMessageHandler messageHandler = new OAuthMessageHandler(
    config,
    new HttpClientHandler() { UseCookies = false }
    );
HttpClient httpClient = new HttpClient(messageHandler)
```

## <a name="optimize-your-connection"></a>接続の最適化

接続を最適化すると、スループットが向上する可能性があります。 .NET サンプル コードをサポートすると、次の設定が使用されます。

```C#
//Change max connections from .NET to a remote service default: 2
System.Net.ServicePointManager.DefaultConnectionLimit = 65000;
//Bump up the min threads reserved for this app to ramp connections faster - minWorkerThreads defaults to 4, minIOCP defaults to 4 
System.Threading.ThreadPool.SetMinThreads(100, 100);
//Turn off the Expect 100 to continue message - 'true' will cause the caller to wait until it round-trip confirms a connection to the server 
System.Net.ServicePointManager.Expect100Continue = false;
//Can decrease overall transmission overhead but can cause delay in data packet arrival
System.Net.ServicePointManager.UseNagleAlgorithm = false;
```

詳細については、[接続の管理](/dotnet/framework/network-programming/managing-connections) を参照してください。

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
