--- 
title: "固定資産の分割"
description: "このタスク ガイドでは、1 つの資産帳簿を新しい資産帳簿に分割します。"
author: saraschi2
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: AssetTable, AssetBook, AssetSplit, AssetBookLookup, LedgerJournalTable, LedgerJournalTransAsset
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: b4c1b39bcae1fa3830f3a217d1ad89e84cd72134
ms.contentlocale: ja-jp
ms.lasthandoff: 09/29/2017

---
# <a name="split-a-fixed-asset"></a>固定資産の分割

[!include [task guide banner](../../includes/task-guide-banner.md)]

このタスク ガイドでは、1 つの資産帳簿を新しい資産帳簿に分割します。  これは、経理担当ロールと USMF デモ データを使用します。


## <a name="create-a-new-fixed-asset"></a>新しい固定資産の作成
1. [固定資産] > [固定資産] > [固定資産] に移動します。
2. [新規] をクリックします。
3. [固定資産グループ] フィールドで、値を入力または選択します。
4. 分割処理で使用する固定資産番号を確認します。
5. [名前] フィールドに値を入力します。
6. フォームを閉じます。

## <a name="split-a-fixed-asset"></a>固定資産の分割
1. 一覧で、分割する固定資産を選択します。
2. 一覧で、選択された行のリンクをクリックします。
3. [帳簿] をクリックします。
    * 新しい資産に分割する帳簿を選択します。  
4. [機能] をクリックします。
5. [固定資産価値の分割] をクリックします。
6. [分割先固定資産] フィールドで、値を入力または選択します。
7. [次の帳簿まで] フィールドで、ドロップ ダウン ボタンをクリックし、ルックアップを開きます。
8. [トランザクション日付] フィールドに、日付を入力します。
9. [割合] フィールドに数を入力します。
10. [仕訳帳名] フィールドで値を入力または選択します。
11. [OK] をクリックします。

## <a name="post-the-journal-transaction"></a>仕訳帳トランザクションの転記
1. [固定資産] > [仕訳入力] > [固定資産仕訳帳] の順に移動します。
2. リストで、分割処理で作成された仕訳帳を選択します。
3. [明細行] をクリックします。
    * 作成した仕訳帳明細行を確認します。  取得原価調整トランザクションは、指定した割合で分割処理中に元の資産の価値を減らすために作成されます。  取得トランザクションは、新しい資産に対して同じ金額で作成されます。  
4. [転記] をクリックします。


