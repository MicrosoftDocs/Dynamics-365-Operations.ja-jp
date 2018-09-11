--- 
title: "委託販売補充注文の作成"
description: "この手順では、委託製品の補充注文の作成方法が説明され、仕入先から該当する委託製品在庫までの予定配送を追跡確認できます。"
author: mkirknel
manager: AnnBe
ms.date: 8/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: ConsignmentReplenishmentOrder, ConsignmentReplenishmentOrderCreate, InventTrans, ConsignmentDraftReplenishmentOrderJournal, InventOnhandMovement, InventOnhandItem, InventItemIdLookupSimple
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: mkirknel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f827b4787506cfdec8b9a91c4a68f3293190158a
ms.openlocfilehash: f7f8005ec9e723c94d53e6ab81f04ee388c83faa
ms.contentlocale: ja-jp
ms.lasthandoff: 09/29/2017

---
# <a name="create-a-consignment-replenishment-order"></a>委託販売補充注文の作成

[!include [task guide banner](../../includes/task-guide-banner.md)]

この手順では、委託製品の補充注文の作成方法が説明され、仕入先から該当する委託製品在庫までの予定配送を追跡確認できます。 このほか、委託製品が仕入先所有の手持在庫として登録されるように製品の受領を記録する方法についても記述されています。 この作業は通常、調達担当者が行います。 デモ データの会社 USMF でこのガイドを使用できます。 この手順は、Dynamics 365 for Operations、バージョン 1611 に追加された機能です。




## <a name="create-a-consignment-replenishment-order"></a>委託販売補充注文の作成
1. [調達] > [委託販売] > [委託販売補充注文] の順に移動します。
2. [新規] をクリックします。
3. [仕入先アカウント] フィールドで「US-104」を選択します。
    * 在庫所有者ページで、所有者として登録されている仕入先を選択する必要があります。  
4. [OK] をクリックします。
5. [明細行の追加] をクリックします。
6. [品目番号] フィールドで「M9211CI」を入力します。
    * 委託販売積送品の在庫に設定されている品目を選択する必要があります。  
7. [数量] フィールドに数値を入力します。
8. [配送希望日] フィールドに日付を入力します。
    * 要求、確認された日付は、製品の予定着荷のMRPエンジンにより使用されています。  
9. [確認済配送日] フィールドに日付を入力します。
10. [明細行の詳細] セクションを展開します。
11. [在庫分析コード] タブをクリックします。
12. 在庫規模所有者フィールドで所有者を表示するには、ページを更新します。
    * 仕入先US-104は所有者としてリストアップされています。  

## <a name="check-the-inventory-transaction-status"></a>在庫トランザクション状態をチェックします。
1. [在庫] をクリックします。
2. [トランザクション] をクリックします。
3. 一覧で、選択された行をマークします。
    * [受領] フィールドが [注文済] に設定されていることを確認します。  
4. ページを閉じます。

## <a name="receive-items"></a>品目の受信 (複数)
1. [製品受領書] をクリックします。
2. [外部製品受領] フィールドで、値を入力します。
3. [数量] フィールドにおいて、ここに表示される数値より小さい数値を入力します。 
4. [OK] をクリックします。

## <a name="check-the-on-hand-inventory"></a>手持在庫を確認します。
1. [在庫] をクリックします。
2. [手持] をクリックします。
3. [概要] をクリックします。
    * 仕入先が所有する委託製品在庫として受領された品目は手持在庫として使用できます。 委託製品補充注文の残余数量は [合計] フィールドの [注文済] に表示されます。  
4. ページを閉じます。
5. [閉じる] をクリックします。


