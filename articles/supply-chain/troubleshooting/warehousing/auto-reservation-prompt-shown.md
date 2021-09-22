---
title: 自動予約プロンプトが利用可能な在庫と一緒に表示される
description: 倉庫プロセスが有効になっていない倉庫で品目を使用した場合、その倉庫に対する自動予約プロンプトは表示されます。 上記のすべての分析コードを指定します。
author: perlynne
ms.date: 06/24/2021
ms.topic: troubleshooting
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: a15502ce8c5bc61d37cedd746985176408a2f362
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/07/2021
ms.locfileid: "7476913"
---
# <a name="auto-reservation-prompt-for-batch-number-is-shown-even-with-available-inventory"></a>バッチ番号の自動予約プロンプトが利用可能な在庫と一緒に表示される

## <a name="symptoms"></a>現象

倉庫プロセスが有効になっていない倉庫で *バッチ-上* の予約階層を持つ品目を使用し、自動予約が有効になっている場合は、ピッキングに使用できるバッチが 1 つだけの場合でも、バッチ番号の自動予約プロンプトが表示されます。

ただし、倉庫プロセスが有効になっている倉庫で同じ品目を使用した場合は、その倉庫に対する自動予約プロンプトは表示されません。

## <a name="resolution"></a>解決策

予約階層が *バッチ-上* または *シリアル-上* と定義されている場合、要求オーダーでは、常に参照される分析コード (**バッチ番号** または **シリアル番号**) を指定する必要があります。 単一のバッチ番号またはシリアル番号が利用可能な場合、倉庫プロセスで情報を完了できる場合があります。 ただし、倉庫の移動が倉庫プロセスに対して有効になっていないので、ユーザーは常に **場所** よりも上のすべての分析コードを指定する必要があります 。
