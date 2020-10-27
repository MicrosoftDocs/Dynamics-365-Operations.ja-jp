---
title: 販売注文に対する同一バッチの引当
description: この記事では、在庫の単一のバッチに対して在庫引当を許可する製品の設定方法を説明します。
author: omulvad
manager: tfehr
ms.date: 03/17/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EcoResProductDetailsExtended, EcoResStorageDimensionGroup, EcoResTrackingDimensionGroup, InventBatch, InventModelGroup, PdsAskSameLotForm, PdsCustSellableDays
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 28911
ms.assetid: 5823d75e-f839-46dd-beb3-e09b79fc8aa4
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 29fd7afdd032e5d3afbe90a1883783b0f2dd83e2
ms.sourcegitcommit: 708ca25687a4e48271cdcd6d2d22d99fb94cf140
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/10/2020
ms.locfileid: "3982164"
---
# <a name="reserve-the-same-batch-for-a-sales-order"></a>販売注文に対する同一バッチの引当

[!include [banner](../includes/banner.md)]

この記事では、在庫の単一のバッチに対して在庫引当を許可する製品の設定方法を説明します。

同じバッチの引当により、販売注文明細行の在庫を単一の在庫バッチに対して引当できます。 たとえば、壁紙を注文する顧客が、壁紙のロール間で不整合が生じないように、同じバッチまたはロットで注文全体に対応することを要求する場合があります。 同じバッチの引当を使用する製品を設定するには、次の設定で、製品に割り当てる品目モデル グループ、追跡用分析コード グループ、および保管分析コード グループを有効にする必要があります。

- **品目モデル グループ** – 品目モデル グループは、在庫ポリシーの**引当**フィールド グループで、**同じバッチの選択**と**要求の連結**が選択されている必要があります。
- **追跡用の分析コード グループ** – 追跡用分析コード グループでは、バッチ番号に対して**分析コード別補充計画**フィールドが選択されている必要があります。
- **保管分析コード グループ** – 保管分析コード グループには**サイト**および**倉庫**に対して選択された**分析コード別補充計画**フィールドが必要です。

同じバッチの選択に対して設定された販売注文明細行の製品の在庫引当を行う場合、システムは、単一の在庫バッチから注文数量を引当しようとします。 すべての特定のバッチ属性要件を考慮します。 数量が単一のバッチで対応できない場合は**同じバッチの引当の競合**ページが表示されます。 このページでは、引当を続行する際の問題と、実行できるアクションについて説明します。 次の条件は、バッチの引当を防ぐ場合があります。

- バッチの廃棄コードに、販売の **引当のブロック** が **ブロック** とフラグ設定されている。
- 有効期限と該当する顧客の販売可能日数に基づくと、バッチが期限切れになっている。 品目モデル グループが先入れ先出し (FEFO) 日付管理対象で、品質保持期限日がピック基準として選択されている場合、品目には引き続き引当が考慮されます。
- 有効期限、出庫期限、および顧客の販売可能日数に基づくと、バッチの在庫有効期間が十分に残っていない。

**倉庫管理プロセスを使用** が有効になっている保管分析コード グループに関連付けられている品目については、場所分析コードの上に定義されているバッチ番号在庫分析コードのある引当階層を使用して、特定のバッチ番号を引当することができます。 販売および移動指示明細書の **バッチ引当** ページで、利用可能なバッチ番号に基づいて複数の明細行を選択および引当することもできます。 場所の下にバッチ番号分析コードがある引当階層を使用している場合の処理の詳細については、[フレキシブルな倉庫レベル分析コードの引当ポリシー](../warehousing/flexible-warehouse-level-dimension-reservation.md) を参照してください。
