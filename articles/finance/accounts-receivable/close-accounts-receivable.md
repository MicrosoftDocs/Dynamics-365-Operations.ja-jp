---
title: 売掛金勘定の決算
description: 次の記事に売掛金勘定の決算業務プロセスをサポートしているページの一覧を示します。
author: ShivamPandey-msft
ms.date: 10/26/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: twheeloc
ms.custom: 59372
ms.assetid: c18d83e5-4adb-422a-91be-82a665d8288b
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 801f086cb0a7c7269abad720c848d2b1ab09cd76
ms.sourcegitcommit: 9c4638c4bb5b5f8adc7508542a0a2c3e1de5190c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/15/2022
ms.locfileid: "9778001"
---
# <a name="close-accounts-receivable"></a>売掛金勘定の決算

[!include [banner](../includes/banner.md)]

次の表に売掛金勘定の決算業務プロセスをサポートしているページの一覧を示します。

> [!NOTE] 
> 次の表で一部のページを開くには、情報の入力またはパラメーター設定の指定が必要です。

**業務プロセス コンポーネント タスク**                   

一般会計の期間の閉鎖

| ページ名                            | 用途                                                                                      |
|--------------------------------------|--------------------------------------------------------------------------------------------|
|**バッチ ジョブ**                          | バッチ ジョブを表示または作成します。 バッチ ジョブを完了できなかった可能性があるため、すべての転記が完了したことを確認します。     |
|**販売注文の確認**                   | 販売注文を更新します。                                                                       |
|**外貨再評価**    | 外貨で転記された未処理の顧客トランザクションの値を更新するトランザクションを生成します。                          |
| **仕訳帳**                              | 請求書、支払、および約束手形を転記します。                                             |
| **仕訳伝票**                      |<ul><li>**支払仕訳帳** : 支払を生成、処理、および転記します。</li><li>**為替手形振出仕訳帳** : 為替手形を転記します。</li><li>**為替手形受取拒否仕訳帳** : 受取拒否手形を転記します。</li><li>**為替手形仕訳の振出** : 再振出済為替手形を転記します。</li><li>**送金仕訳帳** : 送金を転記します。</li><li>**為替手形仕訳帳の決済** : 決済済為替手形を転記します</li></ul>                   |
| **梱包明細転記**                 | 販売注文の梱包明細を更新します。                                                     |
| **自由書式の請求書の転記**               | 自由書式の請求書を転記します。                                                                   |
| **請求の転記**                      | 販売注文の請求書を転記します。                                                            |
| **ピッキング リストの転記**                 |販売注文のピッキング リストを更新します。                                                      |

**業務プロセス コンポーネント タスク**   

EU 販売リストの作成および送信

| ページ名                            | 用途                                                                                      |
|--------------------------------------|--------------------------------------------------------------------------------------------|
|**EU 販売リスト**                        | 付加価値税 (VAT) 申告のための売上税所轄官庁への欧州連合 (EU) 販売のレポート。               |








[!INCLUDE[footer-include](../../includes/footer-banner.md)]
