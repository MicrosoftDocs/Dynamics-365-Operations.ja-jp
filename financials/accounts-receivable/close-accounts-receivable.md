---
title: "売掛金勘定の決算"
description: 
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 59372
ms.assetid: c18d83e5-4adb-422a-91be-82a665d8288b
ms.search.region: Global
ms.author: mfalkner
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 4bb647cfd3f012efbffa93a81462c538a24ac850
ms.openlocfilehash: 013c638b93bf2fe97b594de57a363c11e9a98dad
ms.lasthandoff: 03/31/2017


---

# <a name="close-accounts-receivable"></a>売掛金勘定の決算

[!include[banner](../includes/banner.md)]




次の表に売掛金勘定の決算業務プロセスをサポートしているページの一覧を示します。

> [!NOTE] 
> 次の表で一部のページを開くには、情報の入力またはパラメーター設定の指定が必要です。

**業務プロセス コンポーネント タスク**                   

一般会計の期間の閉鎖

| ページ名                            | 用途                                                                                      |
|--------------------------------------|--------------------------------------------------------------------------------------------|
|バッチ ジョブ                             | バッチ ジョブを表示または作成します。 バッチ ジョブを完了できなかったため、すべての転記が完了したことを確認します。                                                                                                               |
|販売注文の確認                   | 販売注文を更新します。                                                                       |
|外貨再評価          | 外貨で転記された未処理の顧客トランザクションの値を更新するトランザクションを生成します。                                                                                                                         |
| 仕訳帳                              | 請求書、支払、および約束手形を転記します。                                             |
| 仕訳伝票                      | -   **支払仕訳帳** – 支払を生成、処理、および転記します。
                                         -   **Draw bill of exchange journal** – Post bills of exchange.
                                         -   **Protest bill of exchange journal** – Post protested bills of exchange.
                                         -   **Redraw bill of exchange journal** – Post redrawn bills of exchange.
                                         -   **Remittance journal** – Post remittances.
                                         -   **Settle bill of exchange journal** – Post settled bills of exchange                   |
| 梱包明細転記                 | 販売注文の梱包明細を更新します。                                                     | | 自由書式の請求書の転記               | 自由書式の請求書を転記します。                                                                   | | 請求書の転記                      | 販売注文の請求書を転記します。                                                            | | ピッキング リストの転記                 |販売注文のピッキング リストを更新します。                                                      |

**業務プロセス コンポーネント タスク**   

EU 販売リストの作成および送信

| ページ名                            | 用途                                                                                      |
|--------------------------------------|--------------------------------------------------------------------------------------------|
|EU 販売リスト                         | 付加価値税 (VAT) 申告のための売上税所轄官庁への欧州連合 (EU) 販売のレポート。                                                                                                                           |







