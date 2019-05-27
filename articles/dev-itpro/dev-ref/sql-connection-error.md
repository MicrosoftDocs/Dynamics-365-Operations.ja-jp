---
title: X++ の SQL 接続エラー例外
description: このトピックでは、X++ での SQL 接続エラー例外のタイプについて説明します。
author: yiqju
manager: AnnBe
ms.date: 09/27/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Developer
ms.reviewer: kfend
ms.search.scope: Operations
ms.custom: 150373
ms.assetid: f06da12e-911c-442c-97fd-280cbc970061
ms.search.region: Global
ms.author: robinr
ms.search.validFrom: 2018-10-01
ms.dyn365.ops.version: Plaform update 21
ms.openlocfilehash: de01f405ef1c570fc74aa9509909140361935133
ms.sourcegitcommit: 2b890cd7a801055ab0ca24398efc8e4e777d4d8c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/07/2019
ms.locfileid: "1537004"
---
# <a name="sql-connection-error-x-exception"></a><span data-ttu-id="913f7-103">X++ の SQL 接続エラー例外</span><span class="sxs-lookup"><span data-stu-id="913f7-103">SQL connection error X++ exception</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="913f7-104">このトピックでは、X++ での SQL 接続エラー例外のタイプについて説明します。</span><span class="sxs-lookup"><span data-stu-id="913f7-104">This topic describes the SQL connection error exception types in X++.</span></span>

## <a name="transientsqlconnectionerror-x-exception"></a><span data-ttu-id="913f7-105">TransientSqlConnectionError X++ 例外</span><span class="sxs-lookup"><span data-stu-id="913f7-105">TransientSqlConnectionError X++ exception</span></span>
<span data-ttu-id="913f7-106">X++ SQL クエリの実行中、サーバー側で一時的な SQL 接続エラーが発生すると、TransientSqlConnectionError X++ 例外が発生します。</span><span class="sxs-lookup"><span data-stu-id="913f7-106">During an X++ SQL query execution, when a transient SQL connection error occurs on the server side, a TransientSqlConnectionError X++ exception will occur.</span></span> <span data-ttu-id="913f7-107">アプリケーションの要件に応じて、アプリケーションは例外をキャッチして処理する必要があります。</span><span class="sxs-lookup"><span data-stu-id="913f7-107">Depending on the application requirements, the application should catch and handle the exception.</span></span>

<span data-ttu-id="913f7-108">この例外は通常、大規模なトランザクションの際に、またはデータベースに大きな処理負荷がかかっている場合に発生します。</span><span class="sxs-lookup"><span data-stu-id="913f7-108">This exception usually occurs during a large transaction or when the database is under a lot of processing pressure.</span></span>

<span data-ttu-id="913f7-109">TransientSqlConnectionError 例外は、トランザクション内ではキャッチできません。</span><span class="sxs-lookup"><span data-stu-id="913f7-109">The TransientSqlConnectionError exception is not catchable within the transaction.</span></span> <span data-ttu-id="913f7-110">この例外が検出された X++ トランザクションは、例外が発生する前にキャンセルされます (**ttsAbort** を呼び出す)。</span><span class="sxs-lookup"><span data-stu-id="913f7-110">The X++ transaction that encounters this exception is canceled (calling **ttsAbort**) before the exception occurs.</span></span> <span data-ttu-id="913f7-111">つまり、汎用 X++ エラー例外ではなく一時的な SQL 接続エラーを特定するためにキャッチ ブロックを使用した後、最上位のトランザクションを再試行するか、新しいセッションでアプリケーション コード ロジックを再試行する必要があります。</span><span class="sxs-lookup"><span data-stu-id="913f7-111">This means that you need to use the catch block to identify the transient SQL connection error instead of a generic X++ error exception, and then retry the outermost transaction or retry application code logic in a new session.</span></span> <span data-ttu-id="913f7-112">この例外は、一時的なサーバーの障害時にアプリケーションの設計を許可します。</span><span class="sxs-lookup"><span data-stu-id="913f7-112">This exception allows the application to be designed for transient server failures.</span></span>

<span data-ttu-id="913f7-113">アプリケーション トランザクションの処理に時間がかかる場合、複数の増分遅延を使用して TransientSqlConnectionError 例外をキャッチできます。</span><span class="sxs-lookup"><span data-stu-id="913f7-113">If an application transaction takes a long time to process, you can use multiple incremental delays to catch the TransientSqlConnectionError exception.</span></span> <span data-ttu-id="913f7-114">新しいセッションでアプリケーション コードを再実行すると、例外をキャッチした後に成功する可能性が最も高くなります。</span><span class="sxs-lookup"><span data-stu-id="913f7-114">Retrying your application code in a new session is most likely to succeed after you have caught the exception.</span></span>


### <a name="example"></a><span data-ttu-id="913f7-115">例</span><span class="sxs-lookup"><span data-stu-id="913f7-115">Example</span></span>
```
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
