---
title: パフォーマンス タイマー
description: このトピックでは、パフォーマンス タイマーの概要を示します。このタイマーは、システムのパフォーマンスが低下する原因を特定するのに役立つツールです。
author: RobinARH
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Developer
ms.reviewer: robinr
ms.search.scope: Operations
ms.custom: 27191
ms.assetid: 64b8f266-a9e1-48ee-93c7-e082f21ddfa7
ms.search.region: Global
ms.author: chwolf
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 21ab1934715ca938a43d14ab16202f8ddc439518
ms.sourcegitcommit: 2b890cd7a801055ab0ca24398efc8e4e777d4d8c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/07/2019
ms.locfileid: "1537316"
---
# <a name="performance-timer"></a>パフォーマンス タイマー

[!include [banner](../includes/banner.md)]

このトピックでは、パフォーマンス タイマーの概要を示します。このタイマーは、システムのパフォーマンスが低下する原因を特定するのに役立つツールです。 

パフォーマンス タイマーを開くには、追加パラメータ debug=develop: https://<em>yoursite</em>.cloud.test.dynamics.com/en/?cmp=USMF&debug=develop を使用して Web ページを開きます。**注:** デバッグ モードで実行すると、パフォーマンスが低下することがわかります。 F12 キーを押して、ブラウザーで使用可能なデバッグ ツールを使用し、パフォーマンスの大半の問題の概要を素早く取得することができます。 タイマーはここで表示されます。 

[![タイマー](./media/timer.png)](./media/timer.png) 

発注書一覧ページなどの一覧ページを開くには、[パフォーマンス タイマー] をクリックします。 次のスクリーン ショットは、クライアント時間とサーバー時間の区切り、および合計時間を示しています。 また、一連のパフォーマンス カウンターと高価なサーバー呼び出しを確認できます。 

[![2\_タイマー](./media/2_timer.png)](./media/2_timer.png) 

サーバー パフォーマンス カウンターの詳細については、リンクのいずれかをクリックします。

-   **フォーム** - フォームには、現在開いているフォームの数と、それらが開いたり閉じられたりした割合 (秒ごと) と、作成されたフォームまたは閉じられたフォームの合計数などの一連のカウンターが表示されます。
-   **GC** - これは、サーバー上のガベージ コレクション プロセスに関する情報です。
-   **Web クライアント セッション** - これは、現在持っている Web クライアント セッションの数と使用中の Web クライアント セッションの数を示します。
-   **サービス セッション プロバイダー** - これは、作成したセッションの合計数です。

詳細については、リンクをクリックしてください。 次の画面で、個別の呼び出しによってトリガーされた SQL クエリの数、および価値が高い SQL クエリを表示できます。 

[![3\_タイマー](./media/3_timer.png)](./media/3_timer.png) 

この情報は、トレースする内容とトラブルシューティングの開始場所の理解に役立ちます。 

<!--In addition to this topic, you can watch this video for more information: [PERF The Performance Timer and Other Tools](https://mix.office.com/watch/ij5cqidra5q3)-->



