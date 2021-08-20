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
ms.openlocfilehash: f873a487eb573eca562b3f7cd350ed0977a035ecd77b326c5d179777f559d817
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/05/2021
ms.locfileid: "6753822"
---
# <a name="you-cant-add-a-line-to-a-purchase-requisition-after-you-request-a-change"></a>変更を要求した後で購買要求に明細行を追加することができない

KB 番号: 4611211

## <a name="symptoms"></a>現象

システムでは、変更を要求した後で購買要求に明細行を追加することを許可しません。

## <a name="resolution"></a>解像度

ワークフローを取り消す必要があります。 購買要求のステータスが *ドラフト* に設定された後は、引き続きその購買要求を編集したり、明細行を追加することができます。
