---
title: "財務パフォーマンス Power BI コンテンツ"
description: "このトピックでは、財務パフォーマンス Power BI コンテンツについて説明します。"
author: kweekley
manager: AnnBe
ms.date: 02/02/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.custom: 106233
ms.assetid: 517e6a88-e7a1-4398-9971-b22fa83306ba
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7b5c4428c8610a7b2d4cf1a28287ba2bb1f9c2ea
ms.openlocfilehash: b7cb5f2096f0be5211024fc6ecbfaa61d6c48c9a
ms.contentlocale: ja-jp
ms.lasthandoff: 02/06/2018

---

# <a name="financial-performance-power-bi-content"></a>財務パフォーマンス Power BI コンテンツ

[!include[banner](../includes/banner.md)]

> [!Note]
> このコンテンツ パックは [Power BI コンテンツ パックを PowerBI.com に公開する](https://docs.microsoft.com/en-us/dynamics365/unified-operations/dev-itpro/migration-upgrade/deprecated-features#power-bi-content-packs-published-to-powerbicom)で記載されたものとして非推奨になっています。

このトピックでは、**財務パフォーマンス** Microsoft Power BI コンテンツについて説明します。 含まれているダッシュボードおよびレポートについて説明し、コンテンツを作成するために使用したデータモデルとエンティティに関する情報を提供します。

## <a name="main-account-setup"></a>主勘定の設定
組織は負債と収益の勘定をレポートに正の金額として表示させるため、主勘定の設定が重要です。 これらの主勘定を正の金額として表示するには、主勘定タイプを [**負債**] または [**収益**] に設定する必要があります。 これらの勘定タイプを使用すると、Power BI での報告は符号が逆になり、正として金額が表示されます。

## <a name="dashboard-and-reports-that-are-included-in-the-power-bi-content"></a>Power BI コンテンツに含まれるダッシュボードおよびレポート
ダッシュボードには、基になるレポートに基づいて集計されたデータ タイルが含まれます。 各タイルには、組織のすべての会社間での今年度における集計情報が含まれます。 次にタイルの例を示します。

- 現金
- 今年度の総収益
- 今年度の経費合計
- 今年度の純利益
- 当座比率
- 勘定カテゴリごとの今年度合計経費
- 現在の比率
- [負債総資産比率]
- 実績対予測された収益
- 今年度の請求収益
- 今年度の営業経費の比率
- 今年度利益率
- 実績対予算の経費 – すべての会社

各タイルがサポート レポートによってサポートされます。 これらのレポートには、詳細情報を提供するテーブルとグラフが含まれます。 次の表にレポートを示します。

| レポート                       | レポートに含まれる情報 |
|-----------------------------|--------------------------------------|
| 現金分析               | 法人による現金、四半期ごとの現金、合計現金および勘定ごとの現金<blockquote>[!NOTE]<br>四半期ごとの現金は、第 1 四半期の合計の期首残高に含まれていません。 これは四半期ごとに転記される新しいトランザクションの合計を表示します。</blockquote> |
| 現在の比率分析      | 法人による現在の比率、四半期ごとの現在の比率、現在の流動資産および負債の残高 |
| 当座比率の分析        | 法人による当座比率、四半期ごとの当座比率、現金残高、売掛金勘定および現在の負債 |
| 売却済商品の原価分析 | 法人による売却済商品の原価 (COGS)、四半期ごとの今年度および昨年度の COGS、法人による COGS から売上、COGS 合計、および売上に対する COGS の割合 |
| 運営資金の分析    | 法人による運営資金、四半期ごとの運営資金、現在の流動資産、現在の負債、および総運営資金 |
| 資産および負債の分析     | 総資産利益率および法人による負債総資産比率、負債総資産比率および四半期累計期間 (現時点までの) における総資産利益率、資産、および負債 |
| 利益率の分析      | 法人による実績および予算の利益率、四半期ごとの利益、利益率の割合、および利益率 |
| 純利益の分析         | 法人による実績および予算純利益、今年度および昨年度の純利益、および純利益に対する経費の割合 |
| 収益の分析           | 法人による実績と予算における金利税引き前利益 (EBIT)、今年度と昨年度の EBIT、収益に対する経費の割合、および実績および予算における収益に対する経費の割合 |
| 収益の分析            | 総収益、法人による実績と予算の総収益、今年度および昨年度の総収益、法人による収益予算差異、この期間と最後の期間における総収益 |
| 経費の分析            | 経費の合計金額、法人による合計経費予算に対する実績金額、四半期ごとの合計経費予算、勘定カテゴリごとの合計経費、および営業経費の比率 |
| 請求収益の分析     | 売掛金勘定の合計、法人による売掛金勘定の合計、四半期ごとの売掛金勘定の合計、売掛金勘定の勘定残高<blockquote>[!NOTE]<br>第 1 四半期の売掛金勘定の勘定科目は、情報に含まれていません。 売掛金勘定に転記される新しいトランザクションの合計を表示します。</blockquote> |

これらすべてのレポートのグラフとタイルはフィルター処理し、ダッシュボードに固定することができます。 Power BI のフィルター処理と固定方法の詳細については、[ダッシュボードの作成およびコンフィギュレーション](https://powerbi.microsoft.com/en-us/guided-learning/powerbi-learning-4-2-create-configure-dashboards) を参照してください。

## <a name="understanding-the-data-model-and-entities"></a>データ モデルおよびエンティティの理解
次のエンティティは**財務パフォーマンス** Power BI コンテンツの基準として使用されていました。

**データ エンティティの集計**

- **GeneralLedgerActivities** – このエンティティは、勘定カテゴリの総勘定元帳の残高を集計します。
- **BudgetActivities** – このエンティティは、勘定カテゴリの予算残高を集計します。

**データ エンティティ**

- FiscalCalendars
- MainAccounts
- LegalEntities
- 元帳
- ChartofAccounts

これらのエンティティは、データ モデルの計算メジャーを作成するために使用されました。 計算メジャーは、主要業績評価指標 (KPI) およびコンテンツで使用されるレポートを計算するために使用されます。 既定では、コンテンツにより、過去 3 年間および将来 1 年間のデータが取得されます。 追加の計算をレポートおよびダッシュボードに含めるには、[Microsoft Excel ワークブック](https://mbs.microsoft.com/customersource/global/AX/downloads/reports/msdaxfinpercontentpowerbi) を変更できます。 このワークブックはコンテンツを作成するために使用された既定のデータ モデルです。 

