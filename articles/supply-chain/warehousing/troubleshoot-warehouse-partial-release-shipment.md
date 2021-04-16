---
title: 部分的なリリースと部分的な出荷に関するトラブルシューティング
description: このトピックでは、Microsoft Dynamics 365 Supply Chain Management での部分的なリリースと部分的な出荷の処理中に発生する可能性がある問題を修正する方法について説明します。
author: perlynne
ms.date: 10/19/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2020-10-19
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: 5534099f81a97a1dcf4908784fd71dd03cf94eaf
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/01/2021
ms.locfileid: "5828157"
---
# <a name="troubleshoot-partial-releases-and-partial-shipments"></a>部分的なリリースと部分的な出荷に関するトラブルシューティング

[!include [banner](../includes/banner.md)]

このトピックでは、Microsoft Dynamics 365 Supply Chain Management での部分的なリリースと部分的な出荷の処理中に発生する可能性がある問題を修正する方法について説明します。

## <a name="the-release-status-of-a-sales-order-remains-partially-released-even-after-the-sales-order-is-invoiced"></a>販売注文のリリース ステータスは、販売注文の請求が行われた後も部分的にリリースされたままになります。

### <a name="issue-description"></a>問題の説明

販売注文は出荷注文ですが、その中の 1 つ以上の品目の荷渡方法が異なります。 注文が請求された後も、まだリリース ステータスが *部分的にリリース済み* になっています。

たとえば、販売注文には配送用と集荷用の 2 つの項目があります。 出荷と集荷の両方が完了しています。 したがって、両方の明細行が請求されています。 ただし、リリース ステータスはまだ *部分的にリリース済み* と表示されますが、これは誤解を招くことになります。

### <a name="issue-resolution"></a>問題の解決

リリース ステータスは、品目が倉庫管理に対して有効になっている注文明細行に対してのみ適用されます。 したがって、このシナリオではリリース ステータスが *部分的にリリース済み* の ままになります。 Microsoft は、この問題を評価し、それが機能上の制限であることを確認しました。 リリース ステータスを更新するには、梱包明細および請求プロセスの一部として拡張機能を追加することができます。


[!INCLUDE[footer-include](../../includes/footer-banner.md)]