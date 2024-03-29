---
title: 貸借対照表の会計報告書
description: この記事では、貸借対照表の既定のレポートについて説明します。 また、これらのレポートに関連付けられる構成要素を説明します。
author: jinniew
ms.date: 10/10/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: FinanicalReports
audience: Application User
ms.reviewer: twheeloc
ms.custom: 12274
ms.assetid: 52f78229-f531-4d16-b337-e2628994acb6
ms.search.region: Global
ms.author: jiwo
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 4aad297f401143388d682da175a6b14727a8f2f0
ms.sourcegitcommit: c5f2cba3c2b0758e536eeaaa40506659a53085e1
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/12/2022
ms.locfileid: "9643826"
---
# <a name="balance-sheet-financial-reports"></a>貸借対照表の会計報告書

[!include [banner](../includes/banner.md)]

この記事では、貸借対照表の既定のレポートについて説明します。 また、これらのレポートに関連付けられる構成要素を説明します。 

## <a name="default-balance-sheet-reports"></a>既定の貸借対照表のレポート

2 つの既定の貸借対照表レポートがあります。 1 つのレポートでは、セクションが積み重ねられています。 他のレポートでは、セクションは並べて表示されています。

| 既定のレポート                       | 目的                                                                                                                           |
|--------------------------------------|--------------------------------------------------------------------------------------|
| 貸借対照表 – 既定              | 年度の組織の財務状態のビューを提供します。                    |
| 貸借対照表と損益計算書の並行表示 – 既定 | 年度の組織の財務状態を並べて表示します。 |

## <a name="building-blocks"></a>レポート パーツ
貸借対照表の財務レポートは、次の構成要素を使用します。

| 既定のレポート                       | 行の定義                       | 列の定義             |
|--------------------------------------|--------------------------------------|-------------------------------|
| 貸借対照表 - 既定              | 貸借対照表 - 既定              | 現時点年間累計および差異 - 既定    |
| 貸借対照表と損益計算書の並行表示 – 既定 | 貸借対照表と損益計算書の並行表示 – 既定 | 年度累計の列 - 既定 |

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



## <a name="additional-resources"></a>追加リソース

[財務諸表の概要](financial-reporting-getting-started.md)

[財務諸表の表示](view-financial-reports.md)

[Dynamics Financial Reporting ブログ](https://blogs.msdn.com/b/dynamics_financial_reporting/)





[!INCLUDE[footer-include](../../includes/footer-banner.md)]
