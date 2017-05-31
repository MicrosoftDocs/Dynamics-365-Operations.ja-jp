---
title: "店舗在庫の管理"
description: "この記事では、在庫の管理に使用できるドキュメントのタイプについて説明します。"
author: josaw1
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core, Retail
ms.custom: 21391
ms.assetid: bfef3717-d0e0-491d-8466-d8a9c995177d
ms.search.region: global
ms.search.industry: Retail
ms.author: rubendel
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: 5e5043d5951015fc14d29989ef4cab20a8b24f3b
ms.contentlocale: ja-jp
ms.lasthandoff: 05/25/2017


---

# <a name="manage-store-inventory"></a>店舗在庫の管理

[!include[banner](includes/banner.md)]


この記事では、在庫の管理に使用できるドキュメントのタイプについて説明します。

組織の在庫を管理するには、次のドキュメント タイプを使用できます。

## <a name="purchase-orders"></a>発注書
発注書は本社で作成されます。 小売倉庫が発注書ヘッダーに含まれている場合、Modern POS (MPOS) または Microsoft Dynamics 365 for Operations - Retail のクラウド POS を使用して、店舗でこの発注書を受け入れることができます。 店舗で受け入れる数量が入力された後、追加変更に対してその数量をローカルに保存できます。 または、数量を確定して本社に送信することもできます。 本社では、店舗で受け入れた数量が Dynamics 365 for Operations の発注書の **今回受入** フィールドに表示されます。

## <a name="transfer-orders"></a>移動オーダー
移動オーダーでは、特定の店舗が品目の出荷元の場所であることを指定できます。 この場合、移動オーダーは MPOS またはクラウド POS のピッキング要求として店舗に表示されます。 必要な数量をピッキングした後、その数量が確定され、本社に送信されます。 本社では、店舗でピッキングされた数量が Dynamics 365 for Operations の移動オーダーの **今すぐ出荷** フィールドに表示されます。 移動オーダーでは、特定の店舗が品目の出荷先の場所であることを指定できます。 この場合、移動オーダーは MPOS またはクラウド POS の入荷要求として店舗に表示されます。 店舗で受け入れる数量が入力された後、追加変更に対してその数量をローカルに保存できます。 または、数量を確定して本社に送信することもできます。 本社では、店舗で受け入れた数量が Dynamics 365 for Operations の移動オーダーの **今回受入** フィールドに表示されます。

## <a name="stock-counts"></a>在庫数
在庫棚卸は、計画済または計画外のいずれかです。 計画済の在庫棚卸は、棚卸を行う必要がある品目を指定する本社で開始されます。 本社で店舗に送信可能な棚卸ドキュメントが作成され、実際の手持在庫数量が店舗で MPOS またはクラウド POS に入力されます。 手動在庫棚卸は店舗で開始され、MPOS またはクラウド POS で実際の手持在庫数量が更新されます。 計画済在庫棚卸とは異なり、計画外在庫棚卸に品目の定義済リストはありません。 いずれかのタイプの在庫棚卸が完了すると、その在庫棚卸が確定され、本社に送信されます。 本社でその在庫棚卸が検証され、転記されます。






