---
title: 製品コンフィギュレーターのトラブルシューティング
description: このトピックでは、製品コンフィギュレーターを操作する際に発生する可能性がある問題の修正方法について説明します。
author: SmithaNataraj
ms.date: 11/04/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: smnatara
ms.search.validFrom: 2020-11-04
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: 77d0c21fbb5a8479ca5e7bdb759c1373b6b255a4
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/01/2021
ms.locfileid: "5841554"
---
# <a name="troubleshoot-the-product-configurator"></a>製品コンフィギュレーターのトラブルシューティング

このトピックでは、製品コンフィギュレーターを操作する際に発生する可能性がある問題の修正方法について説明します。

## <a name="item-text-is-overwritten-when-i-configure-a-product-on-a-sales-order-line"></a>販売注文明細行で製品を構成すると、品目テキストが上書きされます。

### <a name="issue-description"></a>問題の説明

この問題は、構成可能品目の販売注文明細行を作成し、品目テキストを変更した場合に発生します。 品目を構成してから **OK** をクリックすると、テキストは標準テキストで上書きされます。

### <a name="issue-resolution"></a>問題の解決

この動作は予期されています。 テキスト フィールドには、バリアント名が含まれており、行を構成した後にのみ入力されます。 したがって、行を構成した後でなくても、テキストを変更する必要があります。

## <a name="integer-attributes-are-incorrectly-rounded-when-product-configuration-models-are-calculated"></a>製品構成モデルが計算されると、整数属性が誤って丸められます。

### <a name="issue-description"></a>問題の説明

この問題は、次の一連のアクションを実行した場合に発生する可能性があります。

1. 生産構成モデルで次の属性を設定します。

    - 入力 (整数)
    - パーセント(10 進数)
    - 結果 (整数)

2. 以下の式を持つ計算を作成します。

    *結果* = *入力* × *パーセント* ÷ 100

この場合、整数の結果は常に正しく丸められるわけではありません。 たとえば、入力が 1000 で、パーセントが 2.40 であるとします。 したがって、1000 の 2.40 パーセントが 24 (10 進数では 24.00) であるため、整数の結果は 24 であると想定されます。 代わりに、23 という結果が表示されます。 しかし、パーセントが 2.39 の場合、計算は 23 ではなく 24 に丸められます。 パーセントが 2.50 の場合、計算は予想どおり 25 に丸められます。

### <a name="issue-resolution"></a>問題の解決

この問題は、Microsoft Solver Foundation の内部で端数を使用して数値を表す方法が原因で発生します。 前の例では、パーセントが 2.40 である計算の結果は、27021597764222975 ÷ 1125899906842624 = 23.99999999999999911182158029987476766109466552734375 として表されます。 .NET がこの値を整数としてキャストする場合、23 を返します。

他のシナリオがこれに依存しているため、この動作は変更されません。 前の例では、追加の小数点属性と計算を導入することにより、この問題を修正できます。

たとえば、生産構成モデルで次の属性を設定できます。

- 入力 (整数)
- パーセント (10 進数)
- ResultDecimal (10 進数)
- ResultInteger (整数)

この場合、次の計算を追加できます。

- *ResultDecimal* = *入力* × *パーセント* ÷ 100
- *ResultInteger* = *ResultDecimal*


[!INCLUDE[footer-include](../../includes/footer-banner.md)]