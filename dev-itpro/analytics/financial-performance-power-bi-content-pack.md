---
title: "財務パフォーマンス Power BI コンテンツ"
description: "このトピックでは、Microsoft Dynamics 365 for Operations の Microsoft Power BI 用財務パフォーマンス コンテンツパックについて説明します。 コンテンツ パックに含まれているダッシュボードおよびレポートについて説明され、コンテンツ パックを作成するために使用したデータモデルとエンティティについて説明されます。"
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User, IT Pro
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 106233
ms.assetid: 517e6a88-e7a1-4398-9971-b22fa83306ba
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 388b6398488e6f316c1ec07a00182e81c1dc8d08
ms.openlocfilehash: 227285720e7f28beeb135eea081940578531d458
ms.lasthandoff: 03/31/2017


---

# <a name="financial-performance-power-bi-content"></a>財務パフォーマンス Power BI コンテンツ

[!include[banner](../includes/banner.md)]


このトピックでは、Microsoft Dynamics 365 for Operations の Microsoft Power BI 用財務パフォーマンス コンテンツパックについて説明します。 コンテンツ パックに含まれているダッシュボードおよびレポートについて説明され、コンテンツ パックを作成するために使用したデータモデルとエンティティについて説明されます。

<a name="accessing-the-content-pack"></a>コンテンツ パックへのアクセス
--------------------------

2 バージョンの財務パフォーマンス コンテンツ パックが使用できます。 1 つのバージョンは、Microsoft Dynamics Lifecycle Services (LCS) から使用でき、もう一方は PowerBI.com から使用できます。

-   **LCS から使用可能なバージョン:** LCS から使用できる財務パフォーマンス コンテンツ パックは、Microsoft Dynamics 365 for Operations バージョン 1611 をサポートしています。 LCS の共有資産ライブラリにコンテンツ パックがあります。 コンテンツ パックのダウンロード方法および Microsoft Dynamics 365 for Operations データに接続する方法の詳細については、「[Power BI content in LCS from Microsoft and your partners](power-bi-content-microsoft-partners.md)」を参照してください。
-   **PowerBI.com から使用可能なバージョン:** PowerBI.com から使用できる財務パフォーマンス コンテンツ パックは、Microsoft Dynamics AX バージョン 7.0 および 7.0.1 をサポートしています。 Dynamics 365 for Operations データの接続および読み込む方法の詳細については、「[Access Power BI content from PowerBI.com](power-bi-home-page.md)」を参照してください。

## <a name="main-account-setup"></a>主勘定の設定
組織は負債と収益の勘定をレポートに正の金額として表示させるため、Dynamics 365 for Operations の主勘定の設定が重要です。 これらの主勘定を正の金額として表示するには、主勘定タイプを [**負債**] または [**収益**] に設定する必要があります。 これらの勘定タイプを使用すると、Microsoft Power BI での報告は符号が逆になり、正として金額が表示されます。

## <a name="dashboard-and-reports-that-are-included-in-the-content-pack"></a>コンテンツ パックに含まれるダッシュボードおよびレポート
内容パックを Dynamics 365 for Operations データに接続した後に、ダッシュボードとレポートに財務データが表示されます。 Power BI を以前に使用したことがない場合は、詳細については「[Guided Learning page for Power BI](https://powerbi.microsoft.com/en-us/guided-learning/?WT.mc_id=PBIService_GetData)」を参照してください。 ダッシュボードには、基になるレポートに基づいて集計されたデータ タイルが含まれます。 各タイルには、組織のすべての会社間での今年度における集計情報が含まれます。 次にタイルの例を示します。

-   現金
-   今年度の総収益
-   今年度の経費合計
-   今年度の純利益
-   当座比率
-   勘定カテゴリごとの今年度合計経費
-   現在の比率
-   [負債総資産比率]
-   実績対予測された収益
-   今年度の請求収益
-   今年度の営業経費の比率
-   今年度利益率
-   実績対予算の経費 – すべての会社

各タイルがサポート レポートによってサポートされます。 これらのレポートには、詳細情報を提供するテーブルとグラフが含まれます。 次の表にレポートを示します。

| レポート                       | レポートに含まれる情報                                                                                                                                                                                                                                                                                                          |
|-----------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 現金分析               | 法人による現金、四半期ごとの現金、合計現金および勘定ごとの現金 **注記:** **四半期ごとの現金**レポートでは、第 1 四半期の合計に期首残高は含まれません。 これは四半期ごとに転記される新しいトランザクションの合計を表示します。                                                                                |
| 現在の比率分析      | 法人による現在の比率、四半期ごとの現在の比率、現在の流動資産および負債の残高                                                                                                                                                                                                                              |
| 当座比率の分析        | 法人による当座比率、四半期ごとの当座比率、現金残高、売掛金勘定および現在の負債                                                                                                                                                                                                                      |
| 売却済商品の原価分析 | 法人による売却済商品の原価 (COGS)、四半期ごとの今年度および昨年度の COGS、法人による COGS から売上、COGS 合計、および売上に対する COGS の割合                                                                                                                                                                                   |
| 運営資金の分析    | 法人による運営資金、四半期ごとの運営資金、現在の流動資産、現在の負債、および総運営資金                                                                                                                                                                                                                   |
| 資産および負債の分析     | 総資産利益率および法人による負債総資産比率、負債総資産比率および四半期累計期間 (現時点までの) における総資産利益率、資産、および負債                                                                                                                                                                                     |
| 利益率の分析      | 法人による実績および予算の利益率、四半期ごとの利益、利益率の割合、および利益率                                                                                                                                                                                                                       |
| 純利益の分析         | 法人による実績および予算純利益、今年度および昨年度の純利益、および純利益に対する経費の割合                                                                                                                                                                                                                       |
| 収益の分析           | 法人による実績と予算における金利税引き前利益 (EBIT)、今年度と昨年度の EBIT、収益に対する経費の割合、および実績および予算における収益に対する経費の割合                                                                                                                                                          |
| 収益の分析            | 総収益、法人による実績と予算の総収益、今年度および昨年度の総収益、法人による収益予算差異、この期間と最後の期間における総収益                                                                                                                                                 |
| 経費の分析            | 経費の合計金額、法人による合計経費予算に対する実績金額、四半期ごとの合計経費予算、勘定カテゴリごとの合計経費、および営業経費の比率                                                                                                                                                                 |
| 請求収益の分析     | 売掛金勘定の合計、法人による売掛金勘定の合計、四半期ごとの売掛金勘定の合計、売掛金勘定の勘定残高 **注記:** このレポートでは、売掛金勘定の勘定科目の期首残高は含まれません。 売掛金勘定に転記される新しいトランザクションの合計を表示します。 |

これらすべてのレポートのグラフとタイルはフィルター処理し、ダッシュボードに固定することができます。 Power BI のフィルター処理と固定方法の詳細については、[ダッシュボードの作成およびコンフィギュレーション](https://powerbi.microsoft.com/en-us/guided-learning/powerbi-learning-4-2-create-configure-dashboards) を参照してください。

## <a name="understanding-the-data-model-and-entities"></a>データ モデルおよびエンティティの理解
財務パフォーマンスのコンテンツ パック内にダッシュボードとレポートを設定するデータは Dynamics 365 for Operations のデータです。 次のエンティティはコンテンツ パックの基準として使用されていました: **データ エンティティの集計**

-   **GeneralLedgerActivities** – このエンティティは、勘定カテゴリの総勘定元帳の残高を集計します。
-   **BudgetActivities** – このエンティティは、勘定カテゴリの予算残高を集計します。

**データ エンティティ**

-   FiscalCalendars
-   MainAccounts
-   LegalEntities
-   元帳
-   ChartofAccounts

これらのエンティティは、データ モデルの計算メジャーを作成するために使用されました。 計算メジャーは、主要業績評価指標 (KPI) およびコンテンツ パックで使用するためのレポートを計算するために使用されます。 既定では、コンテンツ パックにより、過去 3 年間および将来 1 年間のデータが取得されます。 追加の計算をレポートおよびダッシュボードに含めるには、[Microsoft Excel ワークブック](https://mbs.microsoft.com/customersource/global/AX/downloads/reports/msdaxfinpercontentpowerbi) を変更できます。 このワークブックはコンテンツ パックを作成するために使用された既定のデータ モデルです。 自分の変更が終了した後に、追加した情報を含む組織のコンテンツ パックとダッシュボードを作成できます。

## <a name="additional-resources"></a>追加リソース
エンティティと建物 Power BI の内容に関連する役立つリンクを次に示します:

-   [データ エンティティ](..\data-entities\data-entities.md)
-   [組織のコンテンツ パックの作成](https://powerbi.microsoft.com/en-us/documentation/powerbi-service-organizational-content-packs-introduction/)
-   [Power BI を使用したデータのモデル化](https://powerbi.microsoft.com/en-us/guided-learning/powerbi-learning-2-1-intro-modeling-data)
-   [Power BI タイルをワークスペースへ追加する](configure-power-bi-integration.md)





