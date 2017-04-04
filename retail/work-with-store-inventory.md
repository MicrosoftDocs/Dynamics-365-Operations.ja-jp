---
title: "店舗在庫の管理"
description: "この記事では、在庫を管理するのに使用できるドキュメントのタイプを示します。"
author: josaw1
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 21391
ms.assetid: bfef3717-d0e0-491d-8466-d8a9c995177d
ms.search.region: global
ms.search.industry: Retail
ms.author: rubendel
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 0c6a7bdc4ba82dd57ab3e395e6dfb0ae4de31fc4
ms.openlocfilehash: fbe9945799f1e65ed6ad624a3df270fa4eb72b88
ms.lasthandoff: 03/31/2017


---

# <a name="manage-store-inventory"></a>店舗在庫の管理

この記事では、在庫を管理するのに使用できるドキュメントのタイプを示します。

組織の在庫を管理するには、次のドキュメント タイプを使用できます。

## <a name="purchase-orders"></a>発注書
発注書は本社で作成されます。 Retailの倉庫が発注書ヘッダーに含める場合、注文は店舗で、[小売に現代POS (MPOS) またはMicrosoft Dynamics 365のクラウドPOSを使用して受信できます。 店舗で受け入れる数量が入力された後、追加変更に対してその数量をローカルに保存できます。 または、数量を確定して本社に送信することもできます。 本社で、店舗で入庫数量は365 for Operationsで発注書に、**に受け取ります。**フィールドに正表示されます。
移動オーダー
---------------

移動オーダーでは、特定の店舗が品目の出荷元の場所であることを指定できます。 この場合、移動オーダー、またはMPOSクラウドPOS.のピッキングの要求として店舗に表示されます。 必要な数量をピッキングした後、その数量が確定され、本社に送信されます。 本社で、店舗で選択された数量は365 for Operationsで移動オーダーに、**、出荷**フィールドに正表示されます。 移動オーダーでは、特定の店舗が品目の出荷先の場所であることを指定できます。 この場合、移動オーダー、またはMPOSクラウドPOS.の受取人の要求として店舗に表示されます。 店舗で受け入れる数量が入力された後、追加変更に対してその数量をローカルに保存できます。 または、数量を確定して本社に送信することもできます。 本社で、店舗で入庫数量は365 for Operationsで移動オーダーに、**に受け取ります。**フィールドに正表示されます。

## <a name="stock-counts"></a>在庫数
在庫棚卸は、計画済または計画外のいずれかです。 計画済の在庫棚卸は、棚卸を行う必要がある品目を指定する本社で開始されます。 本社は、実際の手持在庫数量がMPOSで入力、またはPOS.を曇らせる店舗で入庫する棚卸ドキュメントが作成されます。 計画外在庫棚卸は店舗で開始され、実際の手持在庫数量はMPOSに更新されるか、またはPOS.を曇らせます。 計画済在庫棚卸とは異なり、計画外在庫棚卸に品目の定義済リストはありません。 いずれかのタイプの在庫棚卸が完了すると、その在庫棚卸が確定され、本社に送信されます。 本社でその在庫棚卸が検証され、転記されます。




