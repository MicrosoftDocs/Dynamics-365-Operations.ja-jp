---
title: 償却超過額/償却不足額の定期決済
description: このタスクでは、損金の減価償却費を計算および記録する方法を説明します。
author: kfend
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Japan
ms.author: kfend
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.search.form: LedgerJournalTable, LedgerJournalTransAsset, SysQueryForm, AssetDepPreTaxDedProcess_JP, AssetDepPreTaxDedProcessDetail_JP
ms.openlocfilehash: 79182e3db6ad6f82deab8f7109fbec8a943d1083
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/12/2022
ms.locfileid: "9275203"
---
# <a name="periodic-settlement-of-over-and-under-depreciation"></a>償却超過額/償却不足額の定期決済

[!include [banner](../../includes/banner.md)]

このタスクでは、損金の減価償却費を計算および記録する方法を説明します。



この手順では、JPMF デモ会社のデータを使用します。




## <a name="fixed-asset-depreciation"></a>固定資産の減価償却
1. 次の順に移動します: [固定資産] > > [固定資産仕訳帳]。
2. [新規] をクリックします。
3. [名前] フィールドに値を入力します。
    * 例: FAD  
4. [明細行] をクリックします。
5. [提案] をクリックします。
6. [償却提案] をクリックします。
7. [終了日] フィールドで、日付を入力します。
    * 例: 3/31/ 2016  
8. [フィルター] をクリックします。
9. [基準] フィールドに値を入力します。
    * たとえば、固定資産番号 = BUILM-000005 に設定します。  
10. [OK] をクリックします。
11. [OK] をクリックします。
    * 原価償却仕訳帳が作成されたことを確認します。  
12. [転記] をクリックします。

## <a name="over-and-under-depr-settlements"></a>償却超過/償却不足決済
1. [固定資産] > [定期処理のタスク] > [償却超過/償却不足額の決済] の順に移動します。
2. [新規] をクリックします。
3. [終了日] フィールドで、日付を入力します。
    * 例: 03/31/2016  
4. [仕訳帳名] フィールドに値を入力します。
    * 例: FAD_TAX  
5. [対象に含めるレコード] セクションを展開します。
6. [フィルター] をクリックします。
7. [基準] フィールドに値を入力します。
    * たとえば、固定資産番号 = BUILM-000005 に設定します。  
8. [OK] をクリックします。
9. [OK] をクリックします。
10. ページを更新します。
    * 結果はすぐに表示されないことがあります。 更新をクリックして、結果が作成されたか表示します。  
11. 一覧で、目的のレコードを見つけ、選択します。
    * [ステータス] = [ドラフト] である新しい結果をクリックします。  
12. [決済結果の表示] をクリックします。
    * 正しい結果が作成されていることを確認します。  
13. [転記] をクリックします。



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
