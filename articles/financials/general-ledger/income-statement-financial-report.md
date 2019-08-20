---
title: 損益計算書財務諸表
description: この記事では、損益計算書の既定のレポートについて説明します。 また、このレポートに関連付けられる構成要素を説明します。
author: jcart1106
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: FinancialReports
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 12294
ms.assetid: 30820be0-d943-4f8b-8c25-6414ec393b3d
ms.search.region: Global
ms.author: jcart
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: b7c5d27d43b287aef87f5ead7f469d5465dd2dcb
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/01/2019
ms.locfileid: "1839090"
---
# <a name="income-statement-financial-report"></a>損益計算書財務諸表

[!include [banner](../includes/banner.md)]

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



<a name="additional-resources"></a>その他のリソース
--------

[財務報告](financial-reporting-getting-started.md)

[財務諸表の表示](view-financial-reports.md)

[Dynamics Financial Reporting ブログ](https://blogs.msdn.com/b/dynamics_financial_reporting/)



