--- 
title: "在庫追跡情報の修正"
description: "この手順は、在庫追跡情報を修正するための在庫振替仕訳帳の作成および転記プロセスについて説明します。"
author: MarkusFogelberg
manager: AnnBe
ms.date: 03/02/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bis
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: mafoge
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 9b947a02be981155053e33a4ef20e19bf2a194a5
ms.openlocfilehash: caf8c67d315666edfffe86e459bc7a4478697f07
ms.contentlocale: ja-jp
ms.lasthandoff: 07/27/2017

---
# <a name="correct-inventory-tracking-information"></a>在庫追跡情報の修正

[!include[task guide banner](../../includes/task-guide-banner.md)]

この手順は、在庫追跡情報を修正するための在庫振替仕訳帳の作成および転記プロセスについて説明します。 この例では、間違って登録したバッチを別のバッチに変更することにより、バッチ管理されている品目の情報が更新されます。 デモ データ会社 USPI または独自のデータを使用してこの手順の説明を見ることができます。 独自のデータを使用する場合、バッチ対応の品目が必要であり、場所により制御されていない必要があります。 在庫振替用に在庫仕訳帳名を設定してある必要もあります。 通常、これらのタスクを実施するのは、倉庫の従業員です。


## <a name="create-an-inventory-transfer-journal"></a>在庫振替仕訳帳の作成
1. [移動] に移動します。
2. [新規] をクリックします。
3. [名前] フィールドで値を入力または選択します。
4. [OK] をクリックします。

## <a name="create-journal-lines"></a>仕訳帳明細行の作成
1. [新規] をクリックします。
2. [品目番号] フィールドで、値を入力または選択します。
    * USPI を使用する場合は、 品目 M5003 を選択します。  
3. [数量] フィールドに数値を入力します。
4. [在庫分析コード] タブをクリックします。
5. [バッチ番号] フィールドで値を入力または選択します。
6. [サイト] フィールドで値を入力または選択します。
7. [倉庫] フィールドで、値を入力または選択します。
8. [バッチ番号] フィールドで値を入力または選択します。

## <a name="post-the-journal"></a>仕訳帳の転記
1. [転記] をクリックします。
2. [OK] をクリックします。

## <a name="check-tracing-information"></a>追跡情報の確認
1. [在庫] をクリックします。
2. [追跡] をクリックします。
3. [OK] をクリックします。
    * この追跡情報を使用して、在庫を修正したバッチを追跡できます。  また、[品目追跡] ページを使用して、この情報を表示できます。  
4. ページを閉じます。

## <a name="check-inventory-transactions"></a>在庫トランザクションの確認
1. [在庫] をクリックします。
2. [トランザクション] をクリックします。
    * ここで、仕訳帳の転記時に作成されたトランザクションを確認できます。   


