---
title: 再試行操作
description: このトピックでは、アプリケーション プログラミング インターフェイス (API) 要求がサービス保護 API の制限に達したため調整された場合に実装できる再試行操作について説明します。
author: jaredha
ms.date: 05/04/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Developer
ms.reviewer: v-chgriffin
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: jaredha
ms.search.validFrom: 2022-04-16
ms.dyn365.ops.version: Platform update 52
ms.openlocfilehash: 103b1cf06565f5cfcbaf7cfcff65cadf304d2813
ms.sourcegitcommit: 04e6c1c9400e1b582180cf3e0e4767434e736c26
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/05/2022
ms.locfileid: "8712791"
---
# <a name="retry-operations"></a>再試行操作

[!include [banner](../includes/banner.md)]

このトピックでは、アプリケーション プログラミング インターフェイス (API) 要求がサービス保護 API の制限に達したため調整された場合に実装できる再試行操作について説明します。

サービス保護 API の制限エラーが発生した場合、ユーザーからの新しい要求を処理できるまでの時間を示す値が提供されます。 Web API から 429 エラーが返された場合、応答ヘッダーには、ユーザーが要求を再送信するまでに待機する間隔 (秒) を示す[再試行](https://developer.mozilla.org/docs/Web/HTTP/Headers/Retry-After) 間隔が含まれます。

**再試行** 間隔の後に再送信される要求は、他の受信要求と共に処理され、サーバーに対する新しい要求のように優先順位が付きます。 再試行要求の優先順位は新しい要求よりも高く設定されません。

## <a name="retry-for-interactive-applications"></a>対話型アプリケーションの再試行

クライアントが対話型アプリケーションである場合は、要求を再試行している間はサーバーがビジー状態であるというメッセージを表示する必要があります。 ユーザーが操作をキャンセルできるオプションを指定できます。 以前に送信された要求が完了するまで、ユーザーがさらに要求を送信し続けることは許可されません。

## <a name="retry-for-non-interactive-applications"></a>非対話型アプリケーションの再試行

クライアントが対話型アプリケーションではない場合は、一般的な方法として、要求が再送信されるまでの指定した間隔が過ぎるまで待機します。 通常、この動作は、[Task.Delay](/dotnet/api/system.threading.tasks.task.delay) または同等の方法で現在のタスクの実行を一時停止することで実装されます。

## <a name="retry-after-intervals"></a>再試行間隔

**再試行** 間隔の期間は、前の 5 分間の間に送信された操作の内容によって異なります。 要求が厳しくなればなるほど、サーバーの復旧に時間がかかります。

クライアント アプリケーションが最初の 429 応答を受信した後、厳しい要求を送信し続けると **再試行** 間隔は拡張され、共有リソースに対する影響を最小限に抑えるのに役立ちます。 この拡張子を指定すると個々の **再試行** 間隔が長くなるので、待機中にアプリケーションで長い非アクティブ期間が表示されます。

最初は少ないリクエスト数から始めて、サービス保護 API の制限に達するまで徐々にその数を増やすなどして、できる限り一貫したレートを目指すことをお勧めします。 次に、5 分間の間で処理できる要求数をサーバーから確認できます。 この 5 分間の間に最大の要求数を制限し、徐々に増やしていくことで、**再試行** 間隔を低くすることができます。 これにより、スループットの合計を最適化し、サーバー リソースのスパイクを最小限に抑えるのに役立ちます。

## <a name="implement-retry-operations"></a>再試行操作の実装

次の例では、**再試行** 間隔に指定された秒後に要求を再試行する方法を示します。 

```C#
if (!response.IsSuccessStatusCode) 
{ 
    if ((int)response.StatusCode == 429) 
    { 
        int seconds = 30; 
        //Try to use the Retry-After header value if it is returned. 
        if (response.Headers.Contains("Retry-After")) 
        { 
            seconds = int.Parse(response.Headers.GetValues("Retry-After").FirstOrDefault()); 
        } 
        Thread.Sleep(TimeSpan.FromSeconds(seconds)); 

        // Retry sending the request.
    } 
} 
```

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
