---
title: 小売明細書に影響を及ぼす 小売パラメーターのコンフィギュレーション
description: このトピックでは、小売明細書の作成や転記が小売パラメーターのコンフィギュレーションにどのように影響を及ぼすかを示します。
author: josaw1
manager: AnnBe
ms.date: 08/01/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: RetailParameters
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: b9a0386a4d61395903e82d988244dd131c1febaf
ms.sourcegitcommit: a368682f9cf3897347d155f1a2d4b33e555cc2c4
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/08/2019
ms.locfileid: "1867274"
---
# <a name="configure-retail-parameters-that-affect-retail-statements"></a>小売明細書に影響を及ぼす 小売パラメーターのコンフィギュレーション

[!include[task guide banner](../includes/task-guide-banner.md)]

このトピックでは、小売明細書の作成や転記が小売パラメーターのコンフィギュレーションにどのように影響を及ぼすかを示します。 この手順では、USMF というデモ会社を使用します。

1. ナビゲーション ウィンドウで、**モジュール > 小売りとコマース > 本社の設定 > パラメーター > 小売パラメーター**に移動します。
2. **転記**タブを選択します。
    - 期間割引金額を転記する場合は、**はい**を選択します。  
    - 既定の勘定を使用するには、**標準**を選択します。あるいは、各期間割引に使用する勘定を定義するには、**定期処理**を選択します。  
      - 在庫明細行が集計可能である場合には、**集計**を選択します。  
      - 請求書や支払が明細書の転記プロセス中に自動的に決済される場合は、**はい**を選択します。  
      - 金庫保管トランザクションが集計される場合は、**はい**を選択します。  
      - 銀行入金トランザクションが集計される場合は、**はい**を選択します。  
      - 明細書の転記の集計を有効にする場合は、**はい**を選択します。  
      - 明細書の転記時に注文を同時に作成および処理する場合は、**はい**を選択します。  
      - 各バッチ ジョブのタスクで処理される最大注文を入力します。  
3. **保存** を選択します。

