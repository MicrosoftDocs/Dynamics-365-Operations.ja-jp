---
title: X++ の SQL 接続エラー例外
description: この記事では、X++ での SQL 接続エラー例外のタイプについて説明します。
author: josaw1
ms.date: 09/27/2018
audience: Developer
ms.reviewer: josaw
ms.search.region: Global
ms.author: josaw
ms.search.validFrom: 2018-10-01
ms.dyn365.ops.version: Plaform update 21
ms.openlocfilehash: bff78bf8289089d09ad99717b8dcb97fb5cc695a
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/12/2022
ms.locfileid: "9271419"
---
# <a name="sql-connection-error-x-exception"></a>X++ の SQL 接続エラー例外

[!include [banner](../includes/banner.md)]

この記事では、X++ での SQL 接続エラー例外のタイプについて説明します。

## <a name="transientsqlconnectionerror-x-exception"></a>TransientSqlConnectionError X++ 例外
X++ SQL クエリの実行中、サーバー側で一時的な SQL 接続エラーが発生すると、TransientSqlConnectionError X++ 例外が発生します。 アプリケーションの要件に応じて、アプリケーションは例外をキャッチして処理する必要があります。

この例外は通常、大規模なトランザクションの際に、またはデータベースに大きな処理負荷がかかっている場合に発生します。

TransientSqlConnectionError 例外は、トランザクション内ではキャッチできません。 この例外が検出された X++ トランザクションは、例外が発生する前にキャンセルされます (**ttsAbort** を呼び出す)。 つまり、汎用 X++ エラー例外ではなく一時的な SQL 接続エラーを特定するためにキャッチ ブロックを使用した後、最上位のトランザクションを再試行するか、新しいセッションでアプリケーション コード ロジックを再試行する必要があります。 この例外は、一時的なサーバーの障害時にアプリケーションの設計を許可します。

アプリケーション トランザクションの処理に時間がかかる場合、複数の増分遅延を使用して TransientSqlConnectionError 例外をキャッチできます。 新しいセッションでアプリケーション コードを再実行すると、例外をキャッチした後に成功する可能性が最も高くなります。


### <a name="example"></a>例

```xpp
public static void LargeTransactionWrapper()
{
    try
    {
        LargeTransaction();
    }
    catch (Exception::TransientSqlConnectionError)
    {
        info("Caught transient SQL connection error, ttslevel=" + int2Str(appl.ttsLevel()));
        // At this point, transaction is canceled
        // Code that indicates retry is possible
    }
    finally
    {
        // Do clean up
    }
}
```


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
