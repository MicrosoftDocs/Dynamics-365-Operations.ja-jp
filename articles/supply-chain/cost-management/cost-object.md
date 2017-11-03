---
title: "原価オブジェクト"
description: "この記事は、原価オブジェクトに関する情報を提供し、原価と数量を累計する方法を説明します。 原価オブジェクトは、原価と数量を累計するエンティティです。 原価オブジェクトのエンティティは、製品またはスタイル、および色のバリアントなどの製品バリアントのいずれかです。"
author: AndersGirke
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: InventCostOnhandItem
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 19451
ms.assetid: ec776b98-813a-490d-848f-468452d98fac
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: yuyus
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 69eeb90387ca5765c163c7d482295ea104cc078c
ms.openlocfilehash: 2549ace837fcdfb9f927e6b486b6a94566bcbbd2
ms.contentlocale: ja-jp
ms.lasthandoff: 09/29/2017

---

# <a name="cost-objects"></a>原価オブジェクト

[!include[banner](../includes/banner.md)]


この記事は、原価オブジェクトに関する情報を提供し、原価と数量を累計する方法を説明します。 原価オブジェクトは、原価と数量を累計するエンティティです。 原価オブジェクトのエンティティは、製品またはスタイル、および色のバリアントなどの製品バリアントのいずれかです。  

## <a name="cost-objects"></a>原価オブジェクト

[**原価オブジェクト**] ページは、製品に登録されるすべての原価オブジェクトを表示します。 原価オブジェクトは、次のソースのデータによって定義されます。

-   品目
-   製品分析コード グループ
-   保管分析コード グループ
-   追跡用分析コード グループ

**注記:** 原価オブジェクトは、**直接材料** タイプの原価要素のみ表します。 原価オブジェクトと在庫オブジェクトは、資産在庫のために選択した在庫分析コードによる原価オブジェクトの定義方法が異なります。 たとえば、品目には次のコンフィギュレーションがあります。

-   **サイト:** 現物在庫 = 有、資産在庫 = 有
-   **倉庫:** 現物在庫 = 有、資産在庫 = 無
-   **バッチ番号:** 現物在庫 = 有、資産在庫 = 無

次の表に、原価オブジェクトと在庫オブジェクトの概要を示します。

| オブジェクト タイプ      | 品目番号 | サービス拠点 | 倉庫 | バッチ番号 |
|------------------|-------------|------|-----------|-----------|
| 原価オブジェクト      |  x           |  x    |           |           |
| 在庫オブジェクト |  x           |  x    |   x        |  x         |

## <a name="accumulation-of-costs-and-quantities"></a>原価と数量の累計
-   [**値**] フィールドの値は、次の値の合計です。
    -   現物原価金額
    -   財務費用金額
    -   調整
-   [**数量**] フィールドの値は、次の値の合計です。
    -   受取済
    -   払出済
    -   転記された数量
-   [**平均単位原価**] フィールドは計算済フィールドです。 この値は、[**値**] の値を [**数量**] の値で割ることにより計算されます。

**注記:** [**現物価格を含める**] パラメーターは、前の計算には影響しません。

<a name="see-also"></a>参照
--------

[製品分析コード グループ](https://technet.microsoft.com/en-us/library/aa499382.aspx)

[保管分析コード グループ](https://technet.microsoft.com/en-us/library/hh209317.aspx)

[追跡用分析コード グループ](https://technet.microsoft.com/en-us/library/hh209465.aspx)

[新機能および変更された機能](../../fin-and-ops/get-started/whats-new-changed.md)

[コスト エントリ](cost-entries.md)




