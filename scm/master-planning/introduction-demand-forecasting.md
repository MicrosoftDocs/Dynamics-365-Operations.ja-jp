---
title: "需要予測の概要"
description: "需要予測は、販売注文からの独立要求および顧客注文のすべての減結合ポイントで依存要求を予測する場合に使用されます。 高度な需要予測の減少のルールで複数のカスタマイズに最適なソリューションを提供します。"
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: ReqDemPlanCreateForecastDialog
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 72004
ms.assetid: 916707c9-1333-460f-a0fa-4e95f6fda2ad
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: roxanad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 9ccbe5815ebb54e00265e130be9c82491aebabce
ms.openlocfilehash: 9152616b81e7873426f296376b5e57c94439379d
ms.lasthandoff: 03/31/2017


---

# <a name="demand-forecasting-overview"></a>需要予測の概要

需要予測は、販売注文からの独立要求および顧客注文のすべての減結合ポイントで依存要求を予測する場合に使用されます。 高度な需要予測の減少のルールで複数のカスタマイズに最適なソリューションを提供します。

ベースラインの予測を生成するには、履歴トランザクション集計が Azure でホストされている Microsoft Azure Machine Learning サービスに転送されます。 このサービスはユーザー間で共有されないため、業界固有の要件に合わせて、簡単にカスタマイズできます。 予測を視覚化、予測を調整して、予測の正確に関する主要業績評価指標(KPIs)を表示できる操作と同様に、Dynamics 365 for Operationsを使用できます。

## <a name="key-features-of-demand-forecasting"></a>需要予測の主な機能
需要予測の主な特長を次に示します。

-   履歴データに基づいて統計ベースライン予測を生成します。
-   動的セットの予測分析コードを使用します。
-   需要傾向、信頼区間と予測調整を視覚化します。
-   計画プロセスで使用する調整された予測を承認します。
-   異常値を削除します。
-   予測精度の測定を作成します。

## <a name="major-themes-in-demand-forecasting"></a>需要予測の主要テーマ
3 つの主要なテーマの需要予測が実装できます。

-   [**モジュール性**] – 需要予測はモジュールおよびコンフィギュレーションが簡単にできます。 変更**取引** **在庫予測によって**機能をコンフィギュレーション キーの &gt; 断続的に回転 &gt; させることができます。**需要予測**。
-   ** Microsoftスタックの再使用** – Microsoftは2015年12月2の機械学習のプラットフォームを起動させました。 これでは、CortanaのAnalytics Suite一部である機械学習は、アルゴリズムにRまたは大蛇のプログラム言語と簡単なドラッグ アンド ドロップ インターフェイス使用して予言する分析の実験を、要求の計算の実験など、作成することを迅速かつ簡単に有効になります。
    -   工程の需要予測の実験365 for Operationsをダウンロードし、業務要件を変更し、Azure Webサービスとして請求する発行、需要予測を生成するのに使用できます。 実験は、エンタープライズ レベルのユーザーとして生産の計画者の工程の定期売買365 for Operationsをダウンロード購入している場合に使用できます。
    -   [Cortana Analytics Gallery](https://gallery.cortanaanalytics.com/) から現在有効な需要予測実験をダウンロードできます。 工程の需要予測の実験365 for Operationsが365 for Operationsで自動的に統合する場合は、顧客やパートナーは、ダウンロードする実験の統合を処理できるものがあります[CortanaのAnalyticsのギャラリー] (https://gallery.cortanaanalytics.com/)。 したがって、の実験[CortanaのAnalyticsのギャラリー] (https://gallery.cortanaanalytics.com/)、工程の需要予測の実験のDynamics 365として使用するように簡単ではありません。 これらは、工程のアプリケーション プログラミング インターフェイス(API)に365 for Operationsを使用するように実験のコードを変更する必要があります。
    -   Microsoft Azure Machine Learning Studio で独自の実験を作成し、Azure のサービスとして発行、そして需要予測の生成に使用することができます。
    -   高パフォーマンスが必要でない場合、または大量のデータの処理が要求されていない場合に、Machine Learning 無料レベルを使用できます。 特に実装およびテスト フェーズの際には、このレベルから常に開始することをお勧めします。 高パフォーマンスと追加のストレージが必要な場合、Machine Learning 標準レベルを使用できます。 この層には、Azure のサブスクリプションが要求され、追加費用が含まれます。 Machine Learning 価格設定の詳細については、<http://aka.ms/machine-learning-price-info>を参照ください。
-   **、結合リリース時点で減少**、結合リリース時点で別、独立した要求の両方を予測するように、この機能の工程の面積365 for Operationsの–の需要予測を予測します。

## <a name="basic-flow-in-demand-forecasting"></a>需要予測の基本フロー
次の図は、需要予測の基本フローを表示します。 

[![需要予測の概要の図] (。/media/demand予測Introduction.png) ] (。/media/demand予測introduction.png) 

需要予測の生成は、Dynamics 365 for Operationsで開始されます。 工程のトランザクションのデータベース365 for Operationsの履歴トランザクション データはは、ステージング テーブルを入力しました。 このステージング テーブルが機械学習サービスにユーザーが入れられます。 最小のカスタマイズを実行して、ステージング テーブルにさまざまなデータ ソースを差し込むことができます。 データ ソースは、Microsoft Dynamics AX 2009、Microsoft Dynamics AX 2012からMicrosoft Excelファイル (コンマ区切り値の(CSV)ファイルおよびデータを含めることができます。 したがって、複数システム間でだデータ履歴を考慮した需要予測を生成できます。 ただし、品目名、販売単位などのマスター データは、さまざまなデータ ソース間でも同じである必要があります。

工程の需要予測の機械学習の実験のDynamics 365を使用して基準の予測を計算、5つの時系列予測方法に最も適切なが検索されます。 これらの予測方法のパラメータは、Dynamics 365 for Operationsで管理されます。 

予測、履歴データ、および以前の繰り返しの需要予測に対して行われた変更は、Dynamics 365 for Operationsに使用できます。 

視覚化および基準の予測を変更できるアクションと同様に、Dynamics 365 for Operationsを使用できます。 手動調整は、予測計画で使用する前に承認する必要があります。

## <a name="limitations"></a>制限
Dynamics 365 for Operationsの需要予測は、製造工業の顧客が予測プロセスを作成するのに役立つツールです。 また、簡単に追加することがあり、需要予測ソリューションのコア機能を提供し、設計されています。 需要予測では、卸売、倉庫、配送、またはそのほかの専門サービスなど、企業の顧客の最も適切なではないかもしがあります。

<a name="see-also"></a>参照
--------

[Demand forecasting setup](demand-forecasting-setup.md)

[Generating a statistical baseline forecast](generate-statistical-baseline-forecast.md)

[Making manual adjustments to the baseline forecast](manual-adjustments-baseline-forecast.md)

[Authorizing the adjusted forecast](authorize-adjusted-forecast.md)

[Monitoring forecast accuracy](monitor-forecast-accuracy.md)

[Remove outliers from historical transaction data when calculating a demand forecast](remove-historical-outliers-calculating-demand-forecast.md)


