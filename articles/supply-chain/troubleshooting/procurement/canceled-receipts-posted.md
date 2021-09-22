---
title: トランザクションは保留中の勘定に転記される可能性があります
description: 製品受領書がキャンセルされると、主勘定が中断された場合でも、保留中の勘定科目にトランザクションを転記することができます
author: kamaybac
ms.date: 05/31/2021
ms.topic: troubleshooting
ms.search.form: PurchTable, PurchTablePart
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: yanansong
ms.search.validFrom: 2021-05-31
ms.dyn365.ops.version: 10.0.13
ms.openlocfilehash: 20df0ee4107ad62bec0dd9a683660fe2375a3dd1
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/07/2021
ms.locfileid: "7476924"
---
# <a name="transactions-can-be-posted-to-a-suspended-ledger-account"></a>トランザクションは保留中の勘定に転記される可能性があります

## <a name="symptoms"></a>現象

製品受領書がキャンセルされると、主勘定が中断された場合でも、保留中の勘定科目にトランザクションを転記することができます。

## <a name="reproduce-the-issue"></a>問題を再現する

この問題を再現する一つの方法は次のプロシージャです。

1. **買掛金勘定パラメーター** ページの **一般** タブで、**元帳の製品受領書の転記** オプションが *はい* に設定されていることを確認します。
1. 発注書を作成し、製品に対して *1000* の数量を持つ注文明細行を追加します。
1. 発注書を確認します。
1. 製品受領書を転記し、伝票を確認します。
1. 関連する主勘定 *200140* と *140200* を中断します。
1. 転記された製品受領書をキャンセルします。
1. トランザクションが保留中の勘定に転記される可能性があることに注意してください。

## <a name="resolution"></a>解決策

製品受領書がキャンセルされると、トランザクションが保留中の勘定に転記される場合があります。なぜなら、この動作では、正しい転記が許可されるからです。
