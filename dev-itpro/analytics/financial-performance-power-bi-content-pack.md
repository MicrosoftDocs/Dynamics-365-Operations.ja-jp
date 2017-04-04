---
title: Financial Performance Power BI content
description: "このトピックでは、Microsoft Power BI工程の財務実績の内容PackのMicrosoft Dynamics 365について説明します。 [コンテンツ パックに含まれるついて、コンテンツ パックを作成するのに使用されたエンティティとデータ モデルについて説明しますレポートおよびダッシュボードを。"
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

# <a name="financial-performance-power-bi-content"></a>Financial Performance Power BI content

このトピックでは、Microsoft Power BI工程の財務実績の内容PackのMicrosoft Dynamics 365について説明します。 [コンテンツ パックに含まれるついて、コンテンツ パックを作成するのに使用されたエンティティとデータ モデルについて説明しますレポートおよびダッシュボードを。

<a name="accessing-the-content-pack"></a>コンテンツPackのアクセス
--------------------------

財務実績の内容パックの二つのバージョンを使用できます。 一つのバージョンは、Microsoft Dynamics Lifecycle Services (LCS)の使用して、残りはPowerBI.comから使用できます。

-   ** LCSから使用可能なバージョン: ** LCSから、財務実績の内容Packは、工程バージョン1611では、Microsoft Dynamics 365をサポートします。 LCSの共有資産のライブラリのコンテンツ パックを検索できます。 コンテンツ パックをダウンロードし、データのMicrosoft Dynamics 365に接続する方法の詳細については、" "を参照してください]、[Microsoftパートナー (能力Bi内容Microsoft partners.md) のLCSのPower BIの内容。
-   ** PowerBI.comから使用可能なバージョン: ** PowerBI.comから、財務実績の内容Pack、Microsoft Dynamics AX 7.0と7.0.1バージョンがサポートされます。 工程365 for Operationsデータを関連付けたり読み込み方法の詳細については、" "を参照してください[] (PowerBI.com能力Biホームpage.md) からアクセスPower BIの内容。

## <a name="main-account-setup"></a>重要な勘定設定
組織が責任と収益をレポートに正の金額として表示されるため、Dynamics 365 for Operationsの主要な勘定の設定が重要です。 正の金額として表示されるこれらの主なアカウントには主要な勘定タイプは、はに**職責**設定する必要があります**収益**。 これらの勘定タイプを使用すると、Microsoft Power BIによって報告は符号をリバース、正として金額を表示します。

## <a name="dashboard-and-reports-that-are-included-in-the-content-pack"></a>コンテンツ パックに含まれるレポートおよびダッシュボード
内容パックを Dynamics 365 for Operations データに接続した後に、ダッシュボードとレポートに財務データが表示されます。 はPower BIの前に使用していない場合は、そのコンフィギュレーションに関する情報を入手ことができます。[導かれるPower BI説明します] (https://powerbi.microsoft.com/en-us/guided-learning/?WT.mc_id=PBIService_GetData)のページを。 ダッシュボードには、基になるレポートに基づいて集計されたデータ タイルが含まれます。 各タイルには、組織のすべての会社間での今年度における集計情報が含まれます。 タイルの一部を挙げます。:

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

各タイルをサポートするレポートによって支持されます。 これらのレポートには、詳細情報を提供するテーブルとグラフが含まれます。 次の表にレポートを示します。

| レポート                       | レポートに含まれる情報                                                                                                                                                                                                                                                                                                          |
|-----------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 現金分析               | 法人による現金、四半期ごとに現金勘定、**メモの合計現金および現金: ** **四半期ごとに現金**レポートは、四半期の合計に開始残高は含まれません。 これは四半期ごとに転記される新しいトランザクションの合計を表示します。                                                                                |
| 現在の比率分析      | 法人による現在の比率、四半期ごとの現在の比率、現在の流動資産および負債の残高                                                                                                                                                                                                                              |
| 当座比率の分析        | 法人の高速率、四半期ごとに速い率、および現金、売掛金勘定、および現在の職責の残高                                                                                                                                                                                                                      |
| 売却済商品の原価分析 | 法人による売却済商品の原価 (COGS)、四半期ごとの今年度および昨年度の COGS、法人による COGS から売上、COGS 合計、および売上に対する COGS の割合                                                                                                                                                                                   |
| 運営資金の分析    | 法人による運営資金、四半期ごとの運営資金、現在の流動資産、現在の負債、および総運営資金                                                                                                                                                                                                                   |
| 資産および負債の分析     | 総資産利益率および法人による負債総資産比率、負債総資産比率および四半期累計期間 (現時点までの) における総資産利益率、資産、および負債                                                                                                                                                                                     |
| 利益率の分析      | 法人による実績および予算の利益率、四半期ごとの利益、利益率の割合、および利益率                                                                                                                                                                                                                       |
| 純利益の分析         | 法人による実績および予算純利益、今年度および昨年度の純利益、および純利益に対する経費の割合                                                                                                                                                                                                                       |
| 収益の分析           | 法人による実績と予算における金利税引き前利益 (EBIT)、今年度と昨年度の EBIT、収益に対する経費の割合、および実績および予算における収益に対する経費の割合                                                                                                                                                          |
| 収益の分析            | 総収益、法人による実績と予算の総収益、今年度および昨年度の総収益、法人による収益予算差異、この期間と最後の期間における総収益                                                                                                                                                 |
| 経費の分析            | 経費の合計金額、法人による合計経費予算に対する実績金額、四半期ごとの合計経費予算、勘定カテゴリごとの合計経費、および営業経費の比率                                                                                                                                                                 |
| 請求収益の分析     | 四半期ごとに、売掛金勘定合計法人によって承認、勘定合計勘定合計)、および売掛金勘定の勘定**メモの残高: **レポートは、売掛金勘定の勘定科目の開始残高は含まれません。 また、売掛金勘定に転記される新しいトランザクションの合計を表示します。 |

これらすべてのレポートのグラフとタイルはフィルター処理し、ダッシュボードに固定することができます。 Power BI のフィルター処理と固定方法の詳細については、[ダッシュボードの作成およびコンフィギュレーション](https://powerbi.microsoft.com/en-us/guided-learning/powerbi-learning-4-2-create-configure-dashboards) を参照してください。

## <a name="understanding-the-data-model-and-entities"></a>データ モデルおよびエンティティの理解
財務実績の内容のダッシュボード、レポートのデータ情報は、Dynamics 365 for Operationsデータ詰まります。 次のエンティティはコンテンツPack基準として使用されます: **集計データのエンティティ**

-   ** GeneralLedgerActivities **この–のエンティティは科目カテゴリに総勘定元帳残高を集計します。
-   ** BudgetActivities **この–のエンティティは科目カテゴリの予算残高を集計します。

**Data entities**

-   FiscalCalendars
-   MainAccounts
-   LegalEntities
-   元帳
-   ChartofAccounts

これらのエンティティがデータ モデルの計算メジャーを作成するのに使用されます。 計算メジャーはコンテンツ パックで使用されるレポートおよび主要業績評価指標(KPIs)を計算するために使用します。 既定では、コンテンツ パックにより、過去 3 年間および将来 1 年間のデータが取得されます。 追加の計算をレポートおよびダッシュボードに含めるには、[Microsoft Excel ワークブック](https://mbs.microsoft.com/customersource/global/AX/downloads/reports/msdaxfinpercontentpowerbi) を変更できます。 このワークブックはコンテンツ パックを作成するために使用された既定のデータ モデルです。 自分の変更が終了した後に、追加した情報を含む組織のコンテンツ パックとダッシュボードを作成できます。

## <a name="additional-resources"></a>追加リソース
エンティティと建物 Power BI の内容に関連する役立つリンクを次に示します:

-   [データ エンティティ](..\data-entities\data-entities.md)
-   [組織のコンテンツ パックの作成](https://powerbi.microsoft.com/en-us/documentation/powerbi-service-organizational-content-packs-introduction/)
-   [Power BI を使用したデータのモデル化](https://powerbi.microsoft.com/en-us/guided-learning/powerbi-learning-2-1-intro-modeling-data)
-   [Power BI タイルをワークスペースへ追加する](configure-power-bi-integration.md)



