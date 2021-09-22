---
title: 販売注文は出荷倉庫操作でリリースできまなかった
description: 販売注文をリリースできませんでした、というエラー メッセージが表示される場合は、いくつかの理由があります。 このページでは、その理由と問題を軽減する方法について説明します。
author: perlynne
ms.date: 06/24/2021
ms.topic: troubleshooting
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: fca5ee1bc97545ea4de56d940fdedd320a6cfe84
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/07/2021
ms.locfileid: "7476891"
---
# <a name="sales-order-could-not-be-released-with-outbound-warehouse-operations"></a>販売注文は出荷倉庫操作でリリースできなかった

## <a name="symptoms"></a>現象

出荷倉庫の操作を行う場合、次のエラー メッセージが表示される場合があります。

> 販売注文をリリースできませんでした。

## <a name="cause"></a>原因

この問題は、いくつかの理由で発生する可能性があります。 たとえば、与信管理保留中の注文で、注文に関連付けられているすべての販売明細行に有効な住所が入力されるまで出荷を作成することはできません。 また、注文を倉庫にリリースする前に対応する必要がある注文保留もあります。 この保留は注文固有の場合もありますが、顧客 ID に含まれている場合もあります。

## <a name="resolution"></a>解決策

販売注文と注文明細行の住所を追加または更新し、注文を倉庫にリリースします。 注文は、有効な配送先住所がある場合にのみ倉庫にリリースできます (**組織管理** モジュールでの住所形式の設定に従って)。

注文の保留を調査し、問題に対処します。 次に、注文または顧客から保留を削除し、注文を倉庫に解放します。
