---
title: オンラインの販売と支払の転記
description: この手順では、オンライン ストアのトランザクションの販売注文と支払を作成する反復バッチ ジョブを構成および実行する方法を説明します。
author: psimolin
manager: AnnBe
ms.date: 08/06/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: RetailChannelOperationsWorkspace, RetailOperatingUnitPicker, SysRecurrence
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Retail
ms.author: jashanno
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: e3bac0cab764436a618fa570901c84ab720dbc86
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/13/2020
ms.locfileid: "4413795"
---
# <a name="posting-of-online-sales-and-payments"></a>オンラインの販売と支払の転記

[!include [banner](../includes/banner.md)]

この手順では、オンライン ストアのトランザクションの販売注文と支払を作成する反復バッチ ジョブを構成および実行する方法を説明します。

オンライン販売と支払の転記は、2 段階のプロセスで行われます。

- HQ でオンライン コマース トランザクション データを引き出します。
- HQ でオーダーを同期させて、販売注文を作成します。

オンライン トランザクション データの取得は、手動で P ジョブを実行することによって、または反復バッチ ジョブを作成することによって行うこともできます。

### <a name="manually-running-the-p-job"></a>手動による P ジョブの実行

1. すべてのワークスペース > Retail とコマース IT に移動します。
2. 配送スケジュールをクリックします。
3. P-0001 を選択します。
4. 必要に応じて、チャネル データベース グループを調整します。
5. 今すぐ実行をクリックします。
6. [はい] をクリックします。

### <a name="scheduling-a-recurring-p-job"></a>定期的な P ジョブのスケジューリング

1. すべてのワークスペース > Retail とコマース IT に移動します。
2. 配送スケジュールをクリックします。
3. P-0001 を選択します。
4. バッチ ジョブの作成をクリックします。
5. バックグラウンドで実行をクリックします。
5. バッチ処理を有効にします。
6. 再実行をクリックします。
7. [終了日なし] のオプションを選択します。
8. カウント フィールドで、実行の間隔を分単位で入力します。 通常、これは 5-10 になります。
9. [OK] をクリックします。
10. [OK] をクリックします。

注文を同期するには、「同期注文」ジョブを手動で実行するか、定期的なバッチジョブを作成します。

### <a name="manually-running-order-synchronization"></a>注文の同期を手動で実行 

「注文の同期」ジョブを一度手動で実行するには、次の手順に従います。

1. すべてのワークスペース > 店舗の財務に移動します。
2. [注文の同期] をクリックします。
3. 組織階層のフィールドで、'地域ごとの店舗' を選択します。
    * 店舗グループのバッチ ジョブを作成する場合は、特定のオンライン ストアまたはノードを選択します。  
    * 選択した項目を追加するには、矢印をクリックします。  
4. [バックグラウンドで実行] タブをクリックします。
5. バッチ処理を無効にする
6. [再実行] をクリックします。
7. 後に終了オプションを選択
8. 後に終了フィールドに、1 と入力します。
9. [OK] をクリックします。
10. [OK] をクリックします。

### <a name="scheduling-recurring-order-synchronization"></a>繰返し注文の同期をスケジューリングする

この手順では、オンライン ストアのトランザクションの販売注文と支払を作成する反復バッチ ジョブを構成および実行する方法を説明します。 この手順では、デモ データの会社 USRT を使用します。

1. すべてのワークスペース > 店舗の財務に移動します。
2. [注文の同期] をクリックします。
3. 組織階層のフィールドで、'地域ごとの店舗' を選択します。
    * 店舗グループのバッチ ジョブを作成する場合は、特定のオンライン ストアまたはノードを選択します。  
    * 選択した項目を追加するには、矢印をクリックします。  
4. [バックグラウンドで実行] タブをクリックします。
5. バッチ処理を有効にする
6. [再実行] をクリックします。
7. [終了日なし] のオプションを選択します。
8. カウント フィールドで、実行の間隔を分単位で入力します。 通常、これは 2-20 になります
9. [OK] をクリックします。
10. [OK] をクリックします。

## <a name="data-entities-involved-in-the-process"></a>プロセスに含まれるデータ エンティティ

- RetailTransactionTable
- RetailTransactionAddressTrans
- RetailTransactionInfocodeTrans
- RetailTransactionTaxTrans
- RetailTransactionSalesTrans
- RetailTransactionTaxMeasure
- RetailTransactionDiscountTrans
- RetailTransactionTaxTransGTE
- RetailTransactionMarkupTrans
- RetailTransactionPaymentTrans
- RetailTransactionAttributeTrans
