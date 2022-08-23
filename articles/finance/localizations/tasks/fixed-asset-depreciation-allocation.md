---
title: 固定資産減価償却配賦の設定
description: 日本では、特定の固定資産の減価償却費は複数の部門間で共有できます。
author: kfend
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: China (PRC), Japan
ms.author: kfend
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.search.form:
- AssetAllocationRuleSetup_CN
- AssetPosting
ms.openlocfilehash: e001cafd351e23c1d7a068a34fef637d76bdc4b2
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/12/2022
ms.locfileid: "9285740"
---
# <a name="setup-fixed-asset-depreciation-allocation"></a>固定資産減価償却配賦の設定

[!include [banner](../../includes/banner.md)]

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
7. BusinessUnit フィールドに値を入力します。
    * 最初の配賦のターゲットに関する情報を入力します。  
8. [割合] フィールドに数値を入力します。
    * すべての配賦のターゲットの合計は 100 にする必要があります。  
9. [相殺勘定] フィールドで、任意の値を指定します。
10. [追加] をクリックします。
11. BusinessUnit フィールドに値を入力します。
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



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
