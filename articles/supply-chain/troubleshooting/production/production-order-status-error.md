---
title: ステータスを完了報告済から終了に変更するとエラーになる
description: 製造オーダーのステータスを完了報告済から終了に変更すると、エラーが表示される場合があります。 このページでは、問題を軽減する方法について説明します。
author: SmithaNataraj
ms.date: 06/24/2021
ms.topic: troubleshooting
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: smnatara
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 744637f5cccffe44b85f77c1a9df2034012fac40
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/07/2021
ms.locfileid: "7476882"
---
# <a name="error-when-changing-status-of-production-order-from-reported-as-finished-to-end"></a>製造オーダーのステータスを完了報告済から終了に変更すると、エラーが表示される

## <a name="symptoms"></a>現象

製造オーダーのステータスが完了報告済から終了に変更された場合、以下のいずれかのエラー メッセージが表示されます:

> 更新が競合しています。 更新後の標準原価が資産在庫金額と一致しません。

> 関数 InventCostMovement.checkVariance で重大なエラーが発生しました。

## <a name="cause"></a>原因

この問題は、基になるデータが別のプロセスによって変更されたために発生します。 このプロセスでは、最大 5 回までデータを更新しようとします。 5 回試行しても競合が発生する場合は、上記のいずれかのエラー メッセージが表示されます。

## <a name="resolution"></a>解決策

この動作は仕様です。 この問題を回避するには、バッチ ジョブを再開します。 実行が完了する必要があります。

バッチ ジョブが再開後に一貫して失敗する場合は、元帳の既定の通貨の丸め精度が、InventSum テーブルの値に適用される丸めに準拠していることを確認してください。 丸めの精度が準拠していない値に変更された場合は、通常、それを対応する値に変更する必要があります。 **ModifiedDateTime** を探します。 この場合、値は、通常、丸めの精度が最近変更されたことを示しています。
