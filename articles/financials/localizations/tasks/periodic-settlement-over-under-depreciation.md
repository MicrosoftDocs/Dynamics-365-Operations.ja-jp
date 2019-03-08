---
title: 償却超過額/償却不足額の定期決済
description: このタスクでは、損金の減価償却費を計算および記録する方法を説明します。
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerJournalTable, LedgerJournalTransAsset, SysQueryForm, AssetDepPreTaxDedProcess_JP, AssetDepPreTaxDedProcessDetail_JP
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Japan
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 5bd14f3e21d61cb3ca9552ff9cf9bbcb5c4a91e4
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/29/2019
ms.locfileid: "371138"
---
# <a name="periodic-settlement-of-over-and-under-depreciation"></a>償却超過額/償却不足額の定期決済

[!include [task guide banner](../../includes/task-guide-banner.md)]

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

