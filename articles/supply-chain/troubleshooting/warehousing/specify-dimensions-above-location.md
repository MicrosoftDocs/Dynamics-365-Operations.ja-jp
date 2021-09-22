---
title: バッチ上の階層の部分数量に対する積荷をリリースできない
description: バッチ上の引当階層を持つ品目を使用する場合、在庫が割り当てられるには、積荷明細行はその場所より上の分析コードを指定する必要があります。
author: perlynne
ms.date: 06/24/2021
ms.topic: troubleshooting
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: eb7e71cc271903cb689c33777b72862246f2dd42
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/07/2021
ms.locfileid: "7476851"
---
# <a name="cant-release-a-load-for-partial-quantity-with-batch-above-reservation-hierarchy"></a>バッチ上の引当階層の部分数量に対する積荷をリリースできない

## <a name="symptoms"></a>現象

*バッチ-上* 予約階層を持つ品目を使用する時、部分数量に対する積荷をリリースしようとする場合、**積荷計画ワークベンチ** ページの **倉庫にリリース** コマンドが機能しません。 次のエラー メッセージが表示されます。

> ウェーブに割り当てるには、積荷明細行は、その場所より上の分析コードを指定する必要があります。 これらの分析コードを割り当てるには、積荷明細行を引当して再作成します。

ただし、*下バッチ* 予約階層を持つ品目を使用する時、部分数量に対する積荷を **計画ワークベンチの積荷** からをリリースできます。

## <a name="cause"></a>原因

予約階層で **場所** 分析コードの上に分析コードを配置する場合は、倉庫へのリリース前に指定する必要があります。 在庫の割り当ては、在庫場所の上の分析コードにすき間がない場合にのみ正常に割り当てできます。

## <a name="resolution"></a>解決策

積荷明細行を引当して再作成することで、**場所** 上のすべての分析コードが割り当てられていることを確認します。
