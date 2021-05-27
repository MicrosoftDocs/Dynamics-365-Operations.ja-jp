---
title: 変更を要求した後で購買要求に明細行を追加することができない
description: システムでは、変更を要求した後で購買要求に明細行を追加することを許可しません。
author: niwang
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: PurchReqTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: jeyao
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 5dbb55a6a352a7acf16729c1cfe1afdac2e2eef8
ms.sourcegitcommit: c011a2ef66b38e71ddaf003f7d243677bb2707c5
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/12/2021
ms.locfileid: "6026682"
---
# <a name="you-cant-add-a-line-to-a-purchase-requisition-after-you-request-a-change"></a>変更を要求した後で購買要求に明細行を追加することができない

KB 番号: 4611211

## <a name="symptoms"></a>現象

システムでは、変更を要求した後で購買要求に明細行を追加することを許可しません。

## <a name="resolution"></a>解像度

ワークフローを取り消す必要があります。 購買要求のステータスが *ドラフト* に設定された後は、引き続きその購買要求を編集したり、明細行を追加することができます。
