---
title: 倉庫の在庫集計
description: この記事では、倉庫内のある場所にある特定の品目を棚卸しするために、在庫棚卸仕訳帳を作成して転記するプロセスを示します。
author: yufeihuang
ms.date: 07/09/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: InventJournalCount, InventJournalCreate, HcmWorkerLookUp, InventItemIdLookupSimple, InventLocationIdLookup, WMSLocationIdLookup, InventTrans
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: yufeihuang
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 7c8712b88867dc4be48bbdb4b905993e3ccbc73f
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/03/2022
ms.locfileid: "8870640"
---
# <a name="count-inventory-in-a-warehouse"></a>倉庫の在庫集計

[!include [banner](../../includes/banner.md)]

この記事では、倉庫内のある場所にある特定の品目を棚卸しするために、在庫棚卸仕訳帳を作成して転記するプロセスを示します。 この手順は、倉庫管理モジュールで使用できる倉庫機能ではなく、在庫管理モジュールで使用できる "基本倉庫" 機能に該当します。 デモ データ会社 USMF または独自のデータを使用してこの手順の説明を見ることができます。 独自のデータを使用する場合は、製品および場所を設定してあること、および棚卸仕訳帳用の在庫仕訳帳名を作成したことを確認してください。 通常、在庫棚卸は倉庫の従業員が実行します。


## <a name="create-an-inventory-counting-journal"></a>在庫棚卸仕訳帳の作成
1. **ナビゲーション ウィンドウ > モジュール > 在庫管理 > 仕訳入力 > 品目棚卸 > 棚卸** の順に移動します。
2. **新規** を選択します。
3. **名前** フィールドで、ドロップダウン リストから使用する在庫棚卸仕訳帳名を選択します。 他の一部のフィールドは、選択した在庫棚卸仕訳帳名の設定に基づいて設定されます。  
4. **作業者** フィールドで、ドロップダウン ボタンを選択し、ルックアップを開きます。
5. 一覧で、使用する作業者を **選択** します。
6. **OK** を選択します。

## <a name="create-journal-lines"></a>仕訳帳明細行を作成します
1. **新規** を選択します。
2. **品目番号** フィールドで、ドロップダウン リストから目的のレコードを選択します。 デモ データの会社 USMF を使用している場合は、**A0001** を選択します。  
3. **サイト** フィールドで、ドロップダウン リストから目的のレコードを選択します。 デモ データの会社 USMF を使用している場合は、サイト **2** を選択します。
4. **倉庫** フィールドで、ドロップダウン リストから目的のレコードを選択します。 デモ データの会社 USMF を使用している場合は、倉庫 **24** を選択します。  
5. **場所** フィールドで、ドロップダウン リストから目的のレコードを選択します。 デモ データの会社 USMF を使用している場合は、場所 **BULK-001** を選択します。  
6. [カウント済] フィールドに数値を入力します。 **手持在庫** フィールドに表示されている数値と異なるカウント済数を入力すると、**数量** フィールドが更新されて差異が表示されます。  
7. **保存** を選択します。

## <a name="post-the-inventory-counting-journal"></a>在庫棚卸仕訳帳の転記
1. **投稿** を選択します。 在庫棚卸仕訳帳を転記する際に、カウントした量が **手持在庫** フィールドで報告されている量と異なる場合は、在庫入庫または在庫払出が転記され、在庫レベルおよび値が変更され、元帳トランザクションが生成されます。
2. **OK** を選択します。

## <a name="view-inventory-transactions"></a>在庫トランザクションの表示
1. **在庫** を選択します。
2. **トランザクション** を選択します。 ここで、在庫棚卸仕訳帳を転記するときに作成されるすべての関連トランザクションを確認できます。   



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]