--- 
title: "倉庫の在庫棚卸"
description: "この手順では、倉庫内のある場所にある特定の品目を棚卸しするために、在庫棚卸仕訳帳を作成して転記するプロセスを説明します。"
author: MarkusFogelberg
manager: AnnBe
ms.date: 8/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: InventJournalCount, InventJournalCreate, HcmWorkerLookUp, InventItemIdLookupSimple, InventLocationIdLookup, WMSLocationIdLookup, InventTrans
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: mafoge
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: fa72cb0d651f5e60797fa41f6e2b2cf1891730b5
ms.contentlocale: ja-jp
ms.lasthandoff: 09/29/2017

---
# <a name="count-inventory-in-a-warehouse"></a>倉庫の在庫棚卸

[!include [task guide banner](../../includes/task-guide-banner.md)]

この手順では、倉庫内のある場所にある特定の品目を棚卸しするために、在庫棚卸仕訳帳を作成して転記するプロセスを説明します。 この手順は、倉庫管理モジュールで使用できる倉庫機能ではなく、在庫管理モジュールで使用できる "基本倉庫" 機能に該当します。 デモ データ会社 USMF または独自のデータを使用してこの手順の説明を見ることができます。 独自のデータを使用する場合は、製品および場所を設定してあること、および棚卸仕訳帳用の在庫仕訳帳名を作成したことを確認してください。 通常、在庫棚卸は倉庫の従業員が実行します。


## <a name="create-an-inventory-counting-journal"></a>在庫棚卸仕訳帳の作成
1. [在庫管理] > [仕訳入力] > [品目棚卸] > [棚卸] の順に選択します。
2. [新規] をクリックします。
3. [名前] フィールドで、ドロップ ダウン ボタンをクリックし、ルックアップを開きます。
4. 一覧で、使用する在庫棚卸仕訳帳の名前をクリックします。
    * 他の一部のフィールドは、選択した在庫棚卸仕訳帳名の設定に基づいて設定されます。  
5. [作業者] フィールドで、ドロップ ダウン ボタンをクリックし、ルックアップを開きます。
6. 一覧で、使用する作業者を選択します。
7. [選択] をクリックします。
8. [OK] をクリックします。

## <a name="create-journal-lines"></a>仕訳帳明細行の作成
1. [新規] をクリックします。
2. [品目番号] フィールドで、ドロップ ダウン ボタンをクリックし、ルックアップを開きます。
3. 一覧で、目的のレコードを見つけ、選択します。
    * デモ データの会社 USMF を使用する場合は、'A0001' を選択します。  
4. [サイト] フィールドで、ドロップ ダウン ボタンをクリックし、ルックアップを開きます。
5. 一覧で、目的のレコードを見つけ、選択します。
    * デモ データの会社 USMF を使用する場合は、サイト '2' を選択します。  
6. [倉庫] フィールドで、ドロップ ダウン ボタンをクリックし、ルックアップを開きます。
7. 一覧で、目的のレコードを見つけ、選択します。
    * デモ データの会社 USMF を使用する場合は、倉庫 '24' を選択します。  
8. [場所] フィールドで、ドロップ ダウン ボタンをクリックし、ルックアップを開きます。
9. 一覧で、目的のレコードを見つけ、選択します。
    * デモ データの会社 USMF を使用する場合は、場所 'BULK-001' を選択します。  
10. [カウント済] フィールドに数値を入力します。
    * [手持在庫] フィールドに表示されている数値と異なるカウント済数を入力すると [数量] フィールドが更新されて差異が表示されます。  
11. [保存] をクリックします。

## <a name="post-the-inventory-counting-journal"></a>在庫棚卸仕訳帳の転記
1. [転記] をクリックします。
    * 在庫棚卸仕訳帳を転記する際に、カウントした量が [手持在庫] フィールドで報告されている量と異なる場合は、在庫入庫または在庫払出が転記され、在庫レベルおよび値が変更され、元帳トランザクションが生成されます。  
2. [OK] をクリックします。

## <a name="view-inventory-transactions"></a>在庫トランザクションの表示
1. [在庫] をクリックします。
2. [トランザクション] をクリックします。
    * ここで、在庫棚卸仕訳帳を転記するときに作成されるすべての関連トランザクションを確認できます。   


