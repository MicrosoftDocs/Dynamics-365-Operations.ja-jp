---
title: 製品構成モデルの計算で誤った整数に丸められる
description: 製品構成モデルが計算されると、誤った整数に丸められる場合があります。 追加された小数点属性と計算に関する問題を修正します。
author: SmithaNataraj
ms.date: 06/24/2021
ms.topic: troubleshooting
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: smnatara
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: b17145d7d17cb784fe11b3fbf65ddf5aa5530f27
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/07/2021
ms.locfileid: "7476895"
---
# <a name="integers-incorrectly-rounded-when-product-configuration-models-are-calculated"></a>製品構成モデルが計算されると、誤った整数に丸められる

## <a name="symptoms"></a>現象

この問題は、次の一連のアクションを実行した場合に発生する可能性があります。

1. 本番稼働構成モデルで次の属性を設定する。

    - 入力 (整数)
    - パーセント(10 進数)
    - 結果 (整数)

2. 以下の式を持つ計算を作成します。

    *結果* = *入力* × *パーセント* ÷ 100

この場合、整数の結果は常に正しく丸められるわけではありません。 たとえば、入力が 1,000 で、パーセントが 2.40 である場合、1,000 の 2.40% は 24 (小数点付きでは 24.00) なので、整数の結果は 24 になります。 代わりに、23 という結果が表示されます。 しかし、パーセントが 2.39 の場合、計算は 23 ではなく 24 に丸められます。 パーセントが 2.50 の場合、計算は予想どおり 25 に丸められます。

## <a name="cause"></a>原因

この問題は、Microsoft Solver Foundation の内部で端数を使用して数値を表す方法が原因で発生します。 前の例では、パーセントが 2.40 である計算の結果は、27021597764222975 ÷ 1125899906842624 = 23.99999999999999911182158029987476766109466552734375 として表されます。 .NET がこの値を整数としてキャストする場合、23 を返します。

## <a name="resolution"></a>解決策

他のシナリオがこれに依存しているため、この動作は変更されません。 前の例では、追加の小数点属性と計算を導入することにより、この問題を修正できます。

たとえば、本番稼働構成モデルで次の属性を設定できます。

- 入力 (整数)
- パーセント (10 進数)
- ResultDecimal (10 進数)
- ResultInteger (整数)

この場合、次の計算を追加できます。

- *ResultDecimal* = *入力* × *パーセント* ÷ 100
- *ResultInteger* = *ResultDecimal*
