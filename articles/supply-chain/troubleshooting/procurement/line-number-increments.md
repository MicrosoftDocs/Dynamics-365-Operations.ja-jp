---
title: インポートされた発注書に正しくない行番号が表示される
description: データ管理を通して発注書をインポートした場合、発注書明細行番号がシステム パラメーターで定義されている増分に従わない
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
ms.openlocfilehash: e1cf5cf1d04824213f495ac3ebf556796c96611a
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/07/2021
ms.locfileid: "7476831"
---
# <a name="imported-purchase-orders-show-incorrect-line-numbers"></a>インポートされた発注書に正しくない行番号が表示される

## <a name="symptoms"></a>現象

既定では、*発注書明細行 V2*  データ エンティティを通じてインポートされた発注書明細行の自動生成された行番号は、システム パラメータで指定されたシステム行番号の増分を使用しません。 ユーザー インターフェイス (UI) を通じて発注書を手動で作成し、明細行を追加すると、行番号が正しく増加します。 ただし、データ管理フレームワーク (DMF) を使用すると、正しく増分しません。

この問題が発生するのは、DMF で明細行をインポートしたときに、インポートされたエンティティで行番号が割り当てられていない場合に、DMF メソッドを使用してそれを割り当てるためです。 このメソッドでは、常に行番号が 1 ずつ増加します。

## <a name="workaround"></a>回避策

発注書明細行をインポートするときに、目的の行番号が [データエンティティの行番号] フィールドに既に設定されていることを確認します。 この場合、DMF は行番号を上書きしません。
