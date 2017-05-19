---
title: "販売注文に対する同一バッチの引当"
description: "この記事では、在庫の単一のバッチに対して在庫引当を許可する製品の設定方法を説明します。"
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: EcoResProductDetailsExtended, EcoResStorageDimensionGroup, EcoResTrackingDimensionGroup, InventBatch, InventModelGroup, PdsAskSameLotForm, PdsCustSellableDays
audience: Application User
ms.reviewer: YuyuScheller
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 28911
ms.assetid: 5823d75e-f839-46dd-beb3-e09b79fc8aa4
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: yuyus
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: fd3392eba3a394bd4b92112093c1f1f9b894426d
ms.openlocfilehash: 2f82d8bf65dcb421420eabbfe9f4c4ef0332b1cc
ms.contentlocale: ja-jp
ms.lasthandoff: 04/25/2017


---

# <a name="reserve-the-same-batch-for-a-sales-order"></a>販売注文に対する同一バッチの引当

[!include[banner](../includes/banner.md)]


この記事では、在庫の単一のバッチに対して在庫引当を許可する製品の設定方法を説明します。

同じバッチの引当により、販売注文明細行の在庫を単一の在庫バッチに対して引当できます。 たとえば、壁紙を注文する顧客が、壁紙のロール間で不整合が生じないように、同じバッチまたはロットで注文全体に対応することを要求する場合があります。 同じバッチの引当を使用する製品を設定するには、次の設定で、製品に割り当てる品目モデル グループ、追跡用分析コード グループ、および保管分析コード グループを有効にする必要があります。

-   **品目モデル グループ** – 品目モデル グループは、在庫ポリシーの**引当**フィールド グループで、**同じバッチの選択**と**要求の連結**が選択されている必要があります。
-   **追跡用の分析コード グループ** – 追跡用分析コード グループでは、バッチ番号に対して**分析コード別補充計画**フィールドが選択されている必要があります。
-   **保管分析コード グループ** – 保管分析コード グループには**サイト**および**倉庫**に対して選択された**分析コード別補充計画**フィールドが必要です。

同じバッチの選択に対して設定された販売注文明細行の製品の在庫引当を行う場合、Microsoft Dynamics 365 for Operations は、単一の在庫バッチから注文数量を引当しようとします。 すべての特定のバッチ属性要件を考慮します。 数量が単一のバッチで対応できない場合は**同じバッチの引当の競合**ページが表示されます。 このページでは、引当を続行する際の問題と、実行できるアクションについて説明します。 次の条件は、バッチの引当を防ぐ場合があります。

-   バッチの廃棄コードに、販売の [**引当のブロック**] が [**ブロック**] とフラグ設定されている。
-   有効期限と該当する顧客の販売可能日数に基づくと、バッチが期限切れになっている。 品目モデル グループが先入れ先出し (FEFO) 日付管理対象で、品質保持期限日がピック基準として選択されている場合、品目には引き続き引当が考慮されます。
-   有効期限、出庫期限、および顧客の販売可能日数に基づくと、バッチの在庫有効期間が十分に残っていない。





