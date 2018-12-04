---
title: "サービス レベル アグリーメント"
description: "サービス レベル アグリーメントにおいて、顧客はサービス会社が案件を記録し、案件が解決される時に基づく最低限の応答時間に合意します。"
author: ShylaThompson
manager: AnnBe
ms.date: 05/01/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: SMAServicelevelagreement
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 
ms.assetid: 
ms.search.region: Global
ms.author: ShylaThompson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: 63389ed348e9b1bebe00d9aaa9f78b97ac39317b
ms.contentlocale: ja-jp
ms.lasthandoff: 05/08/2018

---

# <a name="service-level-agreements"></a>サービス レベル アグリーメント        

[!include [banner](../includes/banner.md)]


サービス レベル契約 (SLA) はサービス会社とサービス顧客の間の契約です。 SLA において、顧客はサービス会社が案件を記録し、案件が解決される時に基づく最低限の応答時間に合意します。

SLA により、顧客に提供されるサービスの水準が決定されます。また、いつサービス ジョブを実行する必要があるかがサービス会社に示されます。

任意の数の SLA を作成して、さまざまなレベルのサービスをサービス顧客に提供できます。

## <a name="create-a-service-level-agreement"></a>サービス レベル契約の作成

1.  **サービス管理** \> **設定** \> **サービス契約** \> **サービス レベル契約**の順にクリックします。

2.  **サービス レベル契約**フィールドで、サービス レベル契約の名前をタイプします。

3.  サービス レベル契約に関連付けられているサービス コールの完了に許容する時間を入力します。 それから、サービス レベル契約を特定のカレンダーに基づかせる場合には、カレンダーを選択します。

## <a name="apply-a-service-level-agreement"></a>サービス レベル契約の適用

SLA はサービス合意に直接適用されます。

手動で作成して SLA 付きのサービス合意に関連付けたサービス注文は、その SLA を基準で測定されます。

自動的に作成したサービス注文は SLA に関連付けられません。

## <a name="apply-the-service-level-agreement-to-the-service-agreement"></a>サービス合意へのサービス レベル契約の適用

1.  **サービス管理** \> **共通** \> **サービス契約** \> **サービス契約**の順にクリックします。 SLA を適用するサービス契約を選択してから、**アクション ウィンドウ**で**編集**をクリックします。

2.  **サービス レベル契約**フィールドで、割り当てる SLA を選択します。

## <a name="apply-the-service-level-agreement-to-the-service-agreement-group"></a>サービス合意グループへのサービス レベル契約の適用

1.  **サービス管理** \> **設定** \> **サービス契約** \> **サービス契約グループ**の順にクリックします。

2.  **サービス レベル契約**フィールドで、割り当てる SLA を選択します。

## <a name="track-time-on-a-service-order-against-an-sla"></a>サービス注文での SLA に対する時間の追跡

SLA が割り当てられているサービス契約に新しいサービス注文を作成すると、サービスの提供の時間期間が開始され、システムでは提供時間の追跡を開始します。 さらに次のオプションを設定できます。

  - サービス注文で、サービス注文に対して使われた合計時間を登録するための時刻記録を開始および停止できます。

  - サービス レベル契約で設定された時間期間への準拠を監視できます。

  - サービス レベル契約の時間期間を超過した場合に設定する必要がある理由コードを定義できます。

## <a name="see-also"></a>参照

[サービス レベル契約に準拠しているかどうかの表示](view-compliance-with-service-level-agreements.md)

  



