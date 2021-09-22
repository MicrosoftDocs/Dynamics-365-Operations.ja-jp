---
title: 分割ピッキングの実行時、単位 %1 に対して数量は無効
description: 複数のバッチ間で分割ピッキングを実行すると、数量が単位 %1 に対して無効であるというエラーが表示される場合があります。 このページは問題を解決するのに役立ちます。
author: perlynne
ms.date: 06/24/2021
ms.topic: troubleshooting
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 4627db7400d6ccd81f25f100de4696058ce35c42
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/07/2021
ms.locfileid: "7476833"
---
# <a name="quantity-is-not-valid-when-performing-a-split-pick-across-multiple-batches"></a>複数のバッチ間で分割ピッキングを実行する場合、数量は無効

## <a name="symptoms"></a>現象

複数のバッチ間で *分割ピッキング* を実行しようとすると、このエラー メッセージが表示されます。

> 数量は単位 %1 に対して無効です。

## <a name="resolution"></a>解決策

倉庫の作業者は、Warehouse Management モバイル アプリで *ショート ピッキング* プロセスを使用する必要があります。 同じ場所から複数のバッチを選択する場合は、アプリの **完全** オプションを使用することもできます。
