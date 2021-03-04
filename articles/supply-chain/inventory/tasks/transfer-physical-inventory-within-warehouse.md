---
title: 倉庫内の現物在庫の移動
description: この手順では、倉庫内の場所間で行われる品目の移動を登録する在庫振替仕訳帳を作成して転記するプロセスを説明します。
author: MarkusFogelberg
manager: tfehr
ms.date: 08/08/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventJournalTransfer, InventJournalCreate, InventItemIdLookupSimple, InventLocationIdLookup, WMSLocationIdLookup, InventTrans
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: mafoge
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 540ba2266ea74c36babce57670f84159c89018f1
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/13/2020
ms.locfileid: "4432216"
---
# <a name="transfer-physical-inventory-within-the-warehouse"></a>倉庫内の現物在庫の移動

[!include [banner](../../includes/banner.md)]

この手順では、倉庫内の場所間で行われる品目の移動を登録する在庫振替仕訳帳を作成して転記するプロセスを説明します。 これを開始する前に、在庫振替用の在庫仕訳帳名を設定してある必要があります。 この手順を確認するには、示されているサンプル値を使用してデモ データの会社 USMF を使用するか、製品と場所を設定済みの場合に独自のデータを使用することができます。 通常、これらのタスクを実施するのは、倉庫の従業員です。


## <a name="create-an-inventory-transfer-journal"></a>在庫振替仕訳帳の作成
1. **ナビゲーション ウィンドウ** で、**在庫管理 > 仕訳入力 > 品目 > 転送** に移動します。
2. **新規** をクリックします。
3. **名前** フィールドで値を入力または選択します。
4. **OK** をクリックします。 仕訳帳明細行ごとに、分析コードの [開始] および [終了] を指定するオプションがあります。 これらは、この仕訳帳タイプでは必須です。 各種ルールを使用して複数の場所に品目を移動できます。 この例では、同じ倉庫内のライセンス プレートにより制御される場所からライセンス プレートにより制御されない場所に項目を移動します。   

## <a name="create-journal-lines"></a>仕訳帳明細行を作成します
1. **仕訳帳明細行クイック タブ** で、**新規** をクリックします。
2. **品目番号グループ** フィールドで、値を入力または選択します。 USMF を使用すると、'A0001' を選択できます。  
3. **移動元サイト** フィールドで値を入力または選択します。 USMF を使用すると、'2' を選択できます。  
4. **移動先サイト** フィールドで値を入力または選択します。 USMF を使用すると、'2' を選択できます。  
5. **移動元倉庫** フィールドで値を入力または選択します。 USMF を使用すると、'24' を選択できます。  
6. **移動先倉庫** フィールドで値を入力または選択します。 USMF を使用すると、'24' を選択できます。  
7. **移動元場所** フィールドで値を入力または選択します。 USMF を使用すると、'FL-001' を選択できます。  
8. **移動先場所** フィールドで値を入力または選択します。 USMF を使用すると、'BULK-001' を選択できます。  
9. **数量** フィールドに、数値を入力します。
10. **明細行の詳細** クイック タブで、**在庫分析コード** タブをクリックします。
11. **開始在庫分析コード**、**ライセンス プレート** フィールドで、値を入力または選択します。 USMF を使用すると、'24' を選択できます。  
12. **保存** をクリックします。

## <a name="post-the-inventory-transfer-journal"></a>在庫振替仕訳帳の転記
1. **アクション ウィンドウ** で、**転記** をクリックします。
2. **OK** をクリックします。

## <a name="view-inventory-transactions"></a>在庫トランザクションの表示
1. **在庫** をクリックします。
2. **トランザクション** をクリックします。 ここで、仕訳帳の転記時に作成されたトランザクションを確認できます。  



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]