---
title: "キャッシュの概要 Power BI コンテンツ"
description: "このトピックでは、キャッシュの概要 Microsoft Power BI コンテンツについて説明します。 コンテンツに含まれているレポートにアクセスする方法を説明し、コンテンツを作成するために使用したデータ モデルおよびエンティティについての情報を提供します。"
author: saraschi2
manager: AnnBe
ms.date: 12/19/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: BankTreasurerWorkspace
audience: Application User
ms.reviewer: sericks
ms.search.scope: Operations, Core
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2017-06-30
ms.dyn365.ops.version: July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: cb43245afe578341251b140383a3b03ba2abd962
ms.openlocfilehash: 5d02a009ca988f91a212e467d4f9784248bbae76
ms.contentlocale: ja-jp
ms.lasthandoff: 12/19/2017

---

# <a name="cash-overview-power-bi-content"></a>キャッシュの概要 Power BI コンテンツ

[!include[banner](../includes/banner.md)]

このトピックでは、**キャッシュの概要** Microsoft Power BI content について説明します。 コンテンツに含まれているレポートにアクセスする方法を説明し、コンテンツを作成するために使用したデータ モデルおよびエンティティについての情報を提供します。

## <a name="overview"></a>概要

**キャッシュの概要** Power BI コンテンツは、組織内で現金を担当する方のために作成されました。 **キャッシュの概要** Power BI コンテンツは、キャッシュ フローの可視性を提供します。 適切な意志決定を支援するための予測も提供し、キャッシュ フローの正常性が向上します。 黒字額と不足分を把握するために、法人、通貨、および銀行口座ごとにキャッシュを分析できます。

## <a name="accessing-the-power-bi-content"></a>Power BI コンテンツへのアクセス

**現金の概要** Power BI コンテンツからのレポートが、**現金の概要** および **銀行管理** ワークスペースで表示されます。

データでキャッシュ フロー予測レポートを表示するには、まず、現金および銀行管理領域から**キャッシュ フロー予測の計算** 機能を使用して、予測計算プロセスを実行する必要があります。  これは、予測に含める会社ごとに完了する必要があります。  [**エンティティ格納**] ページで [LedgerCovLiquidityMeasurement] 集計の測定を更新する必要があります。  

説明するには、[**データの生成**] ページをデモ データ モジュールから使用し、キャッシュ フロー予測デモ データを追加できます。  このスクリプトは、キャッシュ フロー予測テーブルにデータを挿入して、レポートに必要な情報をすばやく入力します。  このモジュールは、デモ データ スイート モデルが環境に展開されている場合にのみ使用できます。 

## <a name="reports-that-are-included-in-the-power-bi-content"></a>Power BI コンテンツに含まれるレポート
次の表は、**キャッシュの概要** Power BI コンテンツの各レポート ページに表示されるメトリックスの詳細について説明しています。

| レポート                                | コンテンツ |
|---------------------------------------|----------|
| 現金の概要 – すべての会社         | <ul><li>システム通貨の現金収支</li><li>予測される通貨残高</li><li>システム通貨での銀行預金残高の合計</li><li>法人ごとの残高</li><li>銀行口座通貨での、現在の実績対予測残高</li></ul> |
| 現金の概要 – 現在の会社       | <ul><li>会計通貨の現金収支</li><li>予測される通貨残高</li><li>会計通貨での銀行預金残高の合計</li><li>銀行口座通貨での、現在の実績対予測残高</li></ul> |
| 予測されるキャッシュ フロー – すべての会社    | <ul><li>システム通貨の現金収支</li><li>日次予測の集計</li><li>予測の詳細</li></ul> |
| キャッシュ フロー予測 – 会社通貨 | <ul><li>会計通貨の現金収支</li><li>日次予測の集計</li><li>予測の詳細</li></ul> |
| 通貨予測                     | <ul><li>予測される通貨残高</li><li>日次通貨集計</li><li>予測の詳細</li></ul> |
| 銀行預金残高                         | <ul><li>システム通貨での銀行預金残高の合計</li><li>法人ごとの残高</li><li>銀行口座通貨での、現在の実績対予測残高</li><li>銀行口座ごとの残高</li><li>通貨別残高</li></ul> |


## <a name="understanding-the-data-model-and-entities"></a>データ モデルおよびエンティティの理解

次の表に、**現金の概要** Power BI コンテンツが基づいているエンティティを示します。

| エンティティ                                                                          | コンテンツ |
|---------------------------------------------------------------------------------|----------|
| LedgerCovLiquidityMeasurement\_Company                                          | レポートをフィルター処理する会社 |
| LedgerCovLiquidityMeasurement\_Date                                             | レポートをフィルター処理する日付 |
| LedgerCovLiquidityMeasurement\_LedgerCovForecastActual                          | 実際の口座残高対最後に予測した銀行預金残高 |
| LedgerCovLiquidityMeasurement\_LedgerCovLiquidity                               | 予測トランザクションの詳細 |
| LedgerCovLiquidityMeasurement\_LedgerCovLiquidityInflowOutflowBalanceCompany    | 各会社の会計通貨を使用したキャッシュ インフロー、アウトフロー、および残高 |
| LedgerCovLiquidityMeasurement\_LedgerCovLiquidityInflowOutflowBalanceEnterprise | 全ての会社に関して、システム通貨を使用したキャッシュ インフロー、アウトフロー、および残高 |
| LedgerCovLiquidityMeasurement\_LedgerCovLiquidityTransactionCurrency            | トランザクション通貨を使用した、トランザクション正味金額および通貨残高の集計 |



