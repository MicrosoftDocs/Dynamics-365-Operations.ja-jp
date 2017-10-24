---
title: "キャッシュの概要 Power BI コンテンツ"
description: "このトピックでは、キャッシュの概要 Microsoft Power BI コンテンツについて説明します。 コンテンツに含まれているレポートにアクセスする方法を説明し、コンテンツを作成するために使用したデータ モデルおよびエンティティについての情報を提供します。"
author: saraschi2
manager: AnnBe
ms.date: 06/22/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: sericks
ms.search.scope: Operations, UnifiedOperations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2017-06-30
ms.dyn365.ops.version: July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: 69eeb90387ca5765c163c7d482295ea104cc078c
ms.openlocfilehash: e891f501727842e176741953df5ef9dd0336a2d5
ms.contentlocale: ja-jp
ms.lasthandoff: 09/29/2017

---

# <a name="cash-overview-power-bi-content"></a>キャッシュの概要 Power BI コンテンツ

[!include[banner](../includes/banner.md)]

このトピックでは、**キャッシュの概要** Microsoft Power BI content について説明します。 コンテンツに含まれているレポートにアクセスする方法を説明し、コンテンツを作成するために使用したデータ モデルおよびエンティティについての情報を提供します。

## <a name="overview"></a>概要

**キャッシュの概要** Power BI コンテンツは、組織内で現金を担当する方のために作成されました。 **キャッシュの概要** Power BI コンテンツは、キャッシュ フローの可視性を提供します。 適切な意志決定を支援するための予測も提供し、キャッシュ フローの正常性が向上します。 黒字額と不足分を把握するために、法人、通貨、および銀行口座ごとにキャッシュを分析できます。

## <a name="accessing-the-power-bi-content"></a>Power BI コンテンツへのアクセス

Dynamics 365 for Finance and Operations, Enterprise Edition (2017 年 7 月) を使用している場合、**キャッシュの概要** Power BI content コンテンツからのレポートは**キャッシュの概要**および**銀行管理**ワークスペースで表示されます。

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

## <a name="extending-the-power-bi-content"></a>Power BI コンテンツの拡張
Lifecycle Services (LCS) で利用できるコンテンツ パックを使用して、Dynamics 365 にログインしない人に優れた分析を提供できます。 他のレポートまたはビジュアルを含めるよう、これらのコンテンツ パックを変更できます。次いで分析のためにコンテンツ パックを Power BI.com テナントに発行します。 

LCS の共有資産ライブラリに **現金の概要** Power BI コンテンツがあります。 コンテンツのダウンロード方法および組織で実装する方法の詳細については、「[Microsoft およびパートナーからの LCS での Power BI コンテンツ](../../dev-itpro/analytics/power-bi-content-microsoft-partners.md)」を参照してください。 Power BI コンテンツの実装方法を示すデモを視聴するには、「[Microsoft の Power BI コンテンツおよび Dynamics Lifecycle Services のパートナー](https://mix.office.com/watch/9puyb1b2xs1w)」の Office Mix を参照してください。

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

これらのエンティティは、データ モデルの計算メジャーを作成するために使用されました。 これらの計算メジャーは、**現金の概要** Power BI コンテンツで使用するためのグラフやレポートの計算に使用されます。 レポートおよびダッシュボードに追加の計算を含めるには、LCS から Power BI ファイルをダウンロードして変更できます。 このファイルはコンテンツを作成するために使用された既定のデータ モデルです。 変更後に、追加した情報を含む組織のコンテンツとダッシュボードを作成できます。


