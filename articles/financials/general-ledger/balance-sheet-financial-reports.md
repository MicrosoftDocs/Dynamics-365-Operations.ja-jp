---
title: "貸借対照表の会計報告書"
description: "この記事では、貸借対照表の既定のレポートについて説明します。 また、これらのレポートに関連付けられる構成要素を説明します。"
author: jcart1106
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 12274
ms.assetid: 52f78229-f531-4d16-b337-e2628994acb6
ms.search.region: Global
ms.author: jcart
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 6323a2bf40a853edff4b3cef31eea7e95542a92e
ms.contentlocale: ja-jp
ms.lasthandoff: 09/29/2017

---

# <a name="balance-sheet-financial-reports"></a>貸借対照表の会計報告書

[!include[banner](../includes/banner.md)]


この記事では、貸借対照表の既定のレポートについて説明します。 また、これらのレポートに関連付けられる構成要素を説明します。 

<a name="default-balance-sheet-reports"></a>既定の貸借対照表のレポート
-----------------------------

2 つの既定の貸借対照表レポートがあります。 1 つのレポートでは、セクションが積み重ねられています。 他のレポートでは、セクションは並べて表示されています。

| 既定のレポート                       | 目的                                                                                                                           |
|--------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------|
| 貸借対照表 – 既定              | 年度の組織の財務状態のビューを提供します。                                                                 |
| 並行表示の貸借対照表 – 既定 | 年度の組織の財務状態のビューを提供します。 資産および負債、また株主の株主資本は並べて表示されます。 |

## <a name="building-blocks"></a>構成要素
貸借対照表の財務レポートは、次の構成要素を使用します。

| 既定のレポート                       | 行の定義                       | 列の定義             |
|--------------------------------------|--------------------------------------|-------------------------------|
| 貸借対照表 - 既定              | 貸借対照表 - 既定              | 現時点年間累計および差異 - 既定    |
| 並行表示の貸借対照表 – 既定 | 並行表示の貸借対照表 – 既定 | 年度累計の列 - 既定 |

### <a name="row-definition"></a>行の定義

両方の貸借対照表レポートの行定義には、従来の貸借対照表の各部分のセクションが含まれます。 並べて表示されたレポートには段区切りが含まれます。それで負債、および所有者の株主資本が資産の横に表示されます。 主勘定カテゴリの分析コードが、両方の行定義の構築に使用されます。 したがって、ユーザーは変更しないでをレポートを生成できます。

### <a name="column-definition"></a>列の定義

列の定義には、さまざまな詳細なレベルと財務データを提供する列のさまざまなタイプが含まれます。

-   **現時点年間累計および差異 – 既定の列のタイプ:**
    -   **DESC** – 行定義の説明
    -   **FD** – 今年度の年度累計の財務データ
    -   **FD** – 昨年度の年度累計の財務データ
    -   **CALC** – 今年度から昨年度を差し引いた差異

<!-- -->

-   **年度累計の列 - 既定:**
    -   **DESC** – 行定義の説明
    -   **FD** – 今年度の年度累計の財務データ

 

<a name="see-also"></a>参照
--------

[財務レポート](financial-reporting-getting-started.md)

[財務レポートの表示](view-financial-reports.md)

[Dynamics Financial Reporting ブログ](http://blogs.msdn.com/b/dynamics_financial_reporting/)




