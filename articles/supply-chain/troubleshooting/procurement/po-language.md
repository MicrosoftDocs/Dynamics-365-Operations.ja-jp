---
title: 購買注文に法人の言語設定が反映されない
description: 発注書上の製品名が、発注書が作成された法人に対して設定されている言語ではなく、システム言語で表示されます
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
ms.openlocfilehash: 4deec493b5480dc570ac82876243bc31a2ae87aa
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/07/2021
ms.locfileid: "7476865"
---
# <a name="purchase-orders-dont-reflect-the-language-settings-of-the-legal-entity"></a>購買注文に法人の言語設定が反映されない


## <a name="symptoms"></a>現象

発注書上の製品名は、発注書が作成された法人に対して設定されている言語ではなく、システム言語で表示されます。

## <a name="reproduce-the-issue"></a>問題を再現する

この問題を再現する一つの方法は次のプロシージャです。

1. システム言語を *EN-US* (米国英語) に設定します。
1. 製品名の翻訳に、*EN-US* と *DE* (ドイツ語) 言語が維持される製品があることを確認してください。
1. 法人の言語を *"DE"* に変更します。
1. 言語として *DE* が設定されている法人では、製品を含む発注書を作成します。
1. 製品名が米国英語 (システム言語) で表示されたままになっていることに注意してください。

## <a name="resolution"></a>解決策

この動作は仕様です。 発注書では、製品は常にシステム言語で表示されます。 発注書の言語は、確認仕訳帳が作成されたときに使用されます。
