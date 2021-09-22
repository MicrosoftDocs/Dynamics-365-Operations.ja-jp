---
title: 注文から転記された後に梱包明細をキャンセルできません
description: WMS に対してピッキングおよび出荷プロセスが有効になっている場合は、販売注文から転記された後に梱包明細をキャンセルすることはできません。 このページには大きな影響を受け取ります。
author: perlynne
ms.date: 06/24/2021
ms.topic: troubleshooting
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: d20e66e2721560b8409eb63c3546a79adc188c7c
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/07/2021
ms.locfileid: "7476929"
---
# <a name="cant-cancel-a-packing-slip-after-its-posted-from-a-sales-order"></a>販売注文から転記された後に梱包明細をキャンセルできません

## <a name="symptoms"></a>現象

高度な倉庫管理 (WMS) に対してピッキングおよび出荷プロセスが有効になっている場合は、販売注文から転記された後に梱包明細をキャンセルすることはできません。

## <a name="resolution"></a>解決策

WMS が有効になっている品目に対して転記された梱包明細を修正するには、注文からではなく、積荷から転記を行う必要があります。 Microsoft は、この問題を評価し、それが機能上の制限であることを確認しました。  

一般に、倉庫管理プロセスを通じてピッキングおよび出荷された販売注文は、梱包明細として、積荷または出荷と販売注文ドキュメント自体から更新することができます。 ただし、梱包明細の販売注文を販売注文ドキュメントから更新した場合は、梱包明細の取消を、積荷または販売注文から行うことはできません。 したがって、積荷から梱包明細の転記を使用することをお勧めします。 この場合、積荷から実行する必要がある取消が有効になります。
