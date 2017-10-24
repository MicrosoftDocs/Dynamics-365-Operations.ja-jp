---
title: "損益計算書財務諸表"
description: "この記事では、損益計算書の既定のレポートについて説明します。 また、このレポートに関連付けられる構成要素を説明します。"
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
ms.custom: 12294
ms.assetid: 30820be0-d943-4f8b-8c25-6414ec393b3d
ms.search.region: Global
ms.author: jcart
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 0017d13b7f7594462dfff4ef896f4139607d4bc5
ms.contentlocale: ja-jp
ms.lasthandoff: 09/29/2017

---

# <a name="income-statement-financial-report"></a>損益計算書財務諸表

[!include[banner](../includes/banner.md)]


この記事では、損益計算書の既定のレポートについて説明します。 また、このレポートに関連付けられる構成要素を説明します。 

<a name="default-income-statement-report"></a>既定の損益計算書表
-------------------------------

| 既定のレポート             | 目的                                                                                              |
|----------------------------|-----------------------------------------------------------------------------------------------------------|
| 損益計算書 – 既定 | 現在の期間また年間累計の組織の収益性のビューを提供します。 |

## <a name="building-blocks"></a>構成要素
損益計算書財務諸表は、次の構成要素を使用します。

| 既定のレポート             | 行の定義                     | 列の定義          |
|----------------------------|------------------------------------|----------------------------|
| 損益計算書 - 既定 | 集計損益計算書 - 既定 | 定期処理および現時点の年間累計 - 既定 |

### <a name="row-definition"></a>行の定義

行定義、集計損益計算書 - 既定には、従来の損益計算書の各部分のセクションが含まれます。 主勘定カテゴリの分析コードは、この行定義の構築に使用されます。 したがって、ユーザーは変更しないでレポートを生成できます。

### <a name="column-definition"></a>列の定義

列の定義には、さまざまな詳細なレベルと財務データを提供する列のさまざまなタイプが含まれます。

-   **定期処理と現時点の年間累計 – 既定の列のタイプ:**
    -   **DESC** – 行定義の説明
    -   **FD** – 現在の期間の財務データ
    -   **FD** – 年間累計の財務データ

 

<a name="see-also"></a>参照
--------

[財務報告](financial-reporting-getting-started.md)

[財務諸表の表示](view-financial-reports.md)

[Dynamics Financial Reporting ブログ](http://blogs.msdn.com/b/dynamics_financial_reporting/)




