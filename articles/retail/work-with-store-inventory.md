---
title: "店舗在庫の管理"
description: "この記事では、在庫の管理に使用できるドキュメントのタイプについて説明します。"
author: rubencdelgado
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations, Retail
ms.custom: 21391
ms.assetid: bfef3717-d0e0-491d-8466-d8a9c995177d
ms.search.region: global
ms.search.industry: Retail
ms.author: rubendel
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 1fd37bcd7155c61492f5f4990685203ea97bca36
ms.contentlocale: ja-jp
ms.lasthandoff: 09/29/2017

---

# <a name="manage-store-inventory"></a>店舗在庫の管理

[!include[banner](includes/banner.md)]


この記事では、在庫の管理に使用できるドキュメントのタイプについて説明します。

組織の在庫を管理するには、次のドキュメント タイプを使用できます。

## <a name="purchase-orders"></a>発注書
発注書は本社で作成されます。 小売倉庫が発注書ヘッダーに含まれている場合、Modern POS (MPOS) または Microsoft Dynamics 365 for Retail のクラウド POS を使用して、店舗でこの発注書を受け入れることができます。 店舗で受け入れる数量が入力された後、追加変更に対してその数量をローカルに保存できます。 または、数量を確定して本社に送信することもできます。 本社では、店舗で受け入れた数量が Dynamics 365 for Retail の発注書の [**今回受入**] フィールドに表示されます。

## <a name="transfer-orders"></a>移動オーダー
移動オーダーでは、特定の店舗が品目の出荷元の場所であることを指定できます。 この場合、移動オーダーは MPOS またはクラウド POS のピッキング要求として店舗に表示されます。 必要な数量をピッキングした後、その数量が確定され、本社に送信されます。 本社では、店舗でピッキングされた数量が Dynamics 365 for Retail の移動オーダーの [**今すぐ出荷**] フィールドに表示されます。 移動オーダーでは、特定の店舗が品目の出荷先の場所であることを指定できます。 この場合、移動オーダーは MPOS またはクラウド POS の入荷要求として店舗に表示されます。 店舗で受け入れる数量が入力された後、追加変更に対してその数量をローカルに保存できます。 または、数量を確定して本社に送信することもできます。 本社では、店舗で受け入れた数量が Dynamics 365 for Retail の移動オーダーの [**今回受入**] フィールドに表示されます。

## <a name="stock-counts"></a>在庫数
在庫棚卸は、計画済または計画外のいずれかです。 計画済の在庫棚卸は、棚卸を行う必要がある品目を指定する本社で開始されます。 本社で店舗に送信可能な棚卸ドキュメントが作成され、実際の手持在庫数量が店舗で MPOS またはクラウド POS に入力されます。 手動在庫棚卸は店舗で開始され、MPOS またはクラウド POS で実際の手持在庫数量が更新されます。 計画済在庫棚卸とは異なり、計画外在庫棚卸に品目の定義済リストはありません。 いずれかのタイプの在庫棚卸が完了すると、その在庫棚卸が確定され、本社に送信されます。 本社でその在庫棚卸が検証され、転記されます。

## <a name="inventory-lookup"></a>在庫検索
複数の店舗および倉庫の現在の手持在庫製品の数量は、在庫検索ページで表示できます。 手持在庫の現在の数量に加えて、将来の納期回答可能在庫 (ATP) 数量は、各店舗ごとに表示できます。 これを行うには、表示したい ATP の店舗を選択して、次に [**店舗の使用可能性を表示**] をクリックします。





