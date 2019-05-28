---
title: ステージ理由コードの使用
description: 理由コードを使用して、サービス レベル契約 (SLA) がキャンセルされた理由、またはサービス注文が SLA で定義されている期限を過ぎた理由を示します。
author: ShylaThompson
manager: AnnBe
ms.date: 05/07/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SMAServiceOrderTable, SMAParameters
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: ShylaThompson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 33fa7e5f08f09fe109d0507d686315d01e043928
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/15/2019
ms.locfileid: "1557759"
---
# <a name="use-stage-reason-codes"></a>ステージ理由コードの使用 

[!include [banner](../includes/banner.md)]


理由コードを使用して、サービス レベル契約 (SLA) がキャンセルされた理由、またはサービス注文が SLA で定義されている期限を過ぎた理由を示します。

また、SLA がキャンセルされた場合、または期日がサービス注文に対して SLA に指定された時間を超えたときに理由コードが必要であることを指定できます。

理由コードが必要であることを指定した場合、次の状況で理由コードを入力する必要があります。

  - サービス注文の SLA に対する時刻記録を停止するステージにサービス注文が移行される場合。

  - サービス注文が承認される場合

  - 時刻記録が手動で停止される場合。

## <a name="set-up-reason-codes"></a>理由コードの設定

1.  **サービス管理** \> **設定** \> **サービス注文** \> **ステージ理由コード**の順にクリックします。

2.  **ステージ理由コード**フォームで、**新規**をクリックして新しい理由コードを作成します。

3.  **ステージ理由コード**フィールドに、固有のステージの理由コードを入力します。

4.  **説明**フィールドに、ステージの理由コードの説明を入力します。

5.  フォームを閉じて、変更を保存します。

## <a name="require-reason-codes-when-a-service-level-agreement-is-canceled"></a>サービス レベル契約がキャンセルされた場合の理由コードの要求

1.  **サービス管理** \> **設定** \> **サービス管理パラメーター**の順にクリックします。

2.  **サービス管理パラメーター**フォームで、**一般**リンクをクリックし、次に**キャンセルの理由コード**チェック ボックスをオンにします。

## <a name="require-reason-codes-when-the-a-service-order-exceeds-the-time-limit-that-is-set-by-the-service-level-agreement"></a>サービス注文がサービス レベル契約で設定されている期限を過ぎた場合の理由コードの要求

1.  **サービス管理** \> **設定** \> **サービス管理パラメーター**の順にクリックします。

2.  **サービス管理パラメーター**フォームで、**一般**リンクをクリックし、次に**時間超過の理由コード**チェック ボックスをオンにします。

## <a name="see-also"></a>参照

[サービス注文の時刻記録の開始および停止](start-and-stop-time-recording-on-a-service-order.md)

  


