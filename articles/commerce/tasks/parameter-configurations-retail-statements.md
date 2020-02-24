---
title: 小売明細書に影響を及ぼすパラメーターのコンフィギュレーション
description: このトピックでは、明細書の作成や転記の方法に影響する Commerce パラメーターのコンフィギュレーションを示します。
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
ms.openlocfilehash: d8cae6d2fa7c469f50fa92141a6cb5a0af1df4b0
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/01/2020
ms.locfileid: "3023156"
---
# <a name="configure-parameters-that-affect-retail-statements"></a>小売明細書に影響を及ぼすパラメーターのコンフィギュレーション

[!include[task guide banner](../includes/task-guide-banner.md)]

このトピックでは、明細書の作成や転記の方法に影響する Commerce パラメーターのコンフィギュレーションを示します。 この手順では、USMF というデモ会社を使用します。

1. ナビゲーション ウィンドウで、**モジュール > Retail および Commerce > Headquarters 設定 > パラメーター > Commerce パラメーター**の順に移動します。
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

