--- 
title: "固定資産減価償却配賦の設定 (中国)"
description: "日本では、特定の固定資産の減価償却費は複数の部門間で共有できます。"
author: ShylaThompson
manager: AnnBe
ms.date: 11/11/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Operations
ms.search.region: China (PRC), Japan
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f01d88149074b37517d00f03d8f55e1199a5198f
ms.openlocfilehash: 34d7ad4e3b101d3c265faee430094c15586a964f
ms.contentlocale: ja-jp
ms.lasthandoff: 07/27/2017

---
# <a name="set-up-fixed-asset-depreciation-allocation-china"></a>固定資産減価償却配賦の設定 (中国)

[!include[task guide banner](../../includes/task-guide-banner.md)]

日本では、特定の固定資産の減価償却費は複数の部門間で共有できます。 



このタスクは、固定資産の減価償却の配賦について説明します。 



このタスクは デモ データ会社 JPMF を使用して作成されました。


## <a name="create-a-fixed-asset-allocation-rule"></a>固定資産配賦ルールの作成
1. [固定資産] > [設定] > [減価償却配賦ルール] の順に移動します。
2. [新規] をクリックします。
3. [ルール ID] フィールドに値を入力します。
4. [説明] フィールドに値を入力します。
5. [分析コード名] フィールドで、値を入力します。
6. [追加] をクリックします。
7. [BusinessUnit] フィールドに値を入力します。
    * 最初の配賦のターゲットに関する情報を入力します。  
8. [割合] フィールドに数値を入力します。
    * すべての配賦のターゲットの合計は 100 にする必要があります。  
9. [相殺勘定] フィールドで、任意の値を指定します。
10. [追加] をクリックします。
11. [BusinessUnit] フィールドに値を入力します。
12. [割合] フィールドに数値を入力します。
    * すべての配賦のターゲットの合計は 100 にする必要があります。  
13. [相殺勘定] フィールドで、任意の値を指定します。
14. [保存] をクリックします。

## <a name="assign-a-fixed-asset-allocation-rule-to-a-posting-profile"></a>固定資産配賦ルールの転記プロファイルへの割り当て
1. [固定資産] > [設定] > [固定資産転記プロファイル] の順に移動します。
2. [編集] をクリックします。
3. [トランザクション タイプ] フィールドで [減価償却] を選択します。
4. 一覧で、目的のレコードを見つけ、選択します。
    * 配賦ルールをリンクするレコードを選択します。  
5. [減価償却配賦ルール] セクションを展開します。
6. [減価償却の資産の配賦ルール] フィールドに値を入力します。
7. [保存] をクリックします。


