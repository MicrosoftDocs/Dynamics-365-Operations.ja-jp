---
title: 需要予測の概要
description: 需要予測は、販売注文からの独立要求および顧客注文のすべての減結合ポイントで依存要求を予測する場合に使用されます。 拡張された需要予測の削減ルールは、大量のカスタマイズに理想的なソリューションを提供します。
author: t-benebo
ms.date: 07/07/2020
ms.topic: overview
ms.prod: ''
ms.technology: ''
ms.search.form: ReqDemPlanCreateForecastDialog
audience: Application User
ms.reviewer: kamaybac
ms.custom:
- "72004"
- intro-internal
ms.assetid: 916707c9-1333-460f-a0fa-4e95f6fda2ad
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: benebotg
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 5c764cc186b5c8742ccfd90b5928f6625f3360c8
ms.sourcegitcommit: 28a726b3b0726ecac7620b5736f5457bc75a5f84
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/29/2022
ms.locfileid: "9065616"
---
# <a name="demand-forecasting-overview"></a>需要予測の概要

[!include [banner](../includes/banner.md)]

需要予測は、販売注文からの独立要求および顧客注文のすべての減結合ポイントで依存要求を予測する場合に使用されます。 拡張された需要予測の削減ルールは、大量のカスタマイズに理想的なソリューションを提供します。

ベースラインの予測を生成するには、履歴トランザクション集計が Azure でホストされている Microsoft Azure Machine Learning に転送されます。 このサービスはユーザー間で共有されないため、業界固有の要件に合わせて、簡単にカスタマイズできます。 Supply Chain Management を使用して、予測を視覚化し、予測を調整し、予測精度に関する主要業績評価指標 (KPI) を表示することができます。

> [!NOTE]
> Microsoft Azure Machine Learning Studio (クラシック) は、機械学習を使った予測の生成に必要です。 2021 年 12 月 1 日現在、新しい Machine Learning Studio (クラシック) のリソースは作成できません。 ただし、2024 年 8 月 31 日までは、引き続き既存の Machine Learning Studio (クラシック) のリソースを使用することができます。 最新の情報については [、Azure Machine Learning Studio](/azure/machine-learning/overview-what-is-machine-learning-studio#ml-studio-classic-vs-azure-machine-learning-studio) を参照してください。
> 
> Dynamics 365 Supply Chain Management Version 10.0.23 以降では、新しい Azure Machine Learning Studio に対応しています。

## <a name="key-features-of-demand-forecasting"></a>需要予測の主な機能

需要予測の主な特長を次に示します。

- 履歴データに基づいて統計ベースライン予測を生成します。
- 動的セットの予測分析コードを使用します。
- 需要傾向、信頼区間と予測調整を視覚化します。
- 計画プロセスで使用する調整された予測を承認します。
- 異常値を削除します。
- 予測精度の測定を作成します。

## <a name="major-themes-in-demand-forecasting"></a>需要予測の主要テーマ

3 つの主要なテーマの需要予測が実装できます。

- **モジュール性** – 需要予測はモジュールおよびコンフィギュレーションが簡単にできます。 **販売** &gt; **在庫予測** &gt; **需要予測** で構成キーの機能をオン/オフに変更できます。
- **Microsoft Stack の再利用** – Microsoft Cortana Analytics Suite の一部である Machine Learning を使用すると、アルゴリズム R または Python プログラミング言語、およびシンプルなドラッグ アンド ドロップ インターフェースを使用して、需要見積もりの試算などの予測分析実験をすばやく簡単に作成できます。
  - 需要予測実験をダウンロードし、業務要件に合わせて変更し、Azure の Web サービスとして公開し、需要予測の生成にそれらを使用することができます。 エンタープライズ レベルのユーザーとして、生産計画担当者向けに Supply Chain Management サブスクリプションを購入した場合は、この実験をダウンロードできます。
  - [Cortana Analytics Gallery](https://gallery.cortanaanalytics.com/) から現在有効な需要予測実験をダウンロードできます。 需要予測実験は Supply Chain Management と自動的に統合されるので、顧客およびパートナーは [Cortana Analytics Gallery](https://gallery.cortanaanalytics.com/) からダウンロードした実験の統合を処理する必要があります。 したがって、[Cortana Analytics Gallery](https://gallery.cortanaanalytics.com/) の実験は財務と運用の需要予測実験として使用できるほど単純ではありません。 財務と運用アプリケーション プログラム インターフェイス (API) を使用するように実験コードを修正する必要があります。
  - Microsoft Azure Machine Learning Studio (クラシック) で独自の実験を作成し、Azure のサービスとして発行、そして需要予測の生成に使用することができます。
  - 高パフォーマンスが必要でない場合、または大量のデータの処理が要求されていない場合に、Machine Learning 無料レベルを使用できます。 特に実装およびテスト フェーズの際には、このレベルから常に開始することをお勧めします。 高パフォーマンスと追加のストレージが必要な場合、Machine Learning 標準レベルを使用できます。 この層には、Azure のサブスクリプションが要求され、追加費用が含まれます。 Machine Learning 価格設定の詳細については、[Machine Learning Studio の価格](https://aka.ms/machine-learning-price-info)を参照ください。
- **減結合ポイントの予測下方修正** - すべての減結合ポイントで依存要求と独立要求の両方を予測するこの機能で、ビルドでの需要予測を作成します。

## <a name="basic-flow-in-demand-forecasting"></a>需要予測の基本フロー

次の図は、需要予測の基本フローを表示します。

[![需要予測の導入図。](./media/demand-forecasting-introduction.png)](./media/demand-forecasting-introduction.png)

需要予測の生成は、Supply Chain Management で開始されます。 Supply Chain Management トランザクション データベースからの履歴トランザクション データが収集され、ステージング テーブルに値が入力されます。 このステージング テーブルが Machine Learning サービスに後ほど提供されます。 最低限のカスタマイズで、さまざまなデータ ソースをステージング テーブルにプラグできます。 データ ソースには、Microsoft Excel ファイル、コンマ区切り値 (CSV) ファイル、および Microsoft Dynamics AX 2009 と Microsoft Dynamics AX 2012 からのデータが含まれます。 したがって、複数のシステムにまたがった履歴データを考慮する需要予測を生成できます。 ただし、品目名、販売単位などのマスター データは、さまざまなデータ ソース間でも同じである必要があります。

需要予測 Machine Learning 実験を使用すると、ベースライン予測を計算するための 5 つのタイム シリーズ の予測方法の中から最も適切なものを検索します。 予測方法のパラメーターは Supply Chain Management で管理されます。

以前の項目での、予測、履歴データ、および変更点などの需要予測が Supply Chain Management で次に利用可能です。

Supply Chain Management を使用してベースラインの予測を視覚化し修正できます。 手動調整は、予測計画で使用する前に承認する必要があります。

## <a name="limitations"></a>制限

需要予測は、予測プロセスを作成する製造業界の顧客を支援するツールです。 需要予測ソリューションの核となる機能を提供し、簡単に拡張できるように設計されています。 需要予測は、商業、卸売業、倉庫保管、輸送業、または他の専門的なサービス産業の顧客には最適ではない場合があります。

### <a name="demand-forecast-variant-conversion-limitation"></a>需要予測バリアント変換の制限

バリアント変換ごとの測定単位 (UOM) は、在庫単位が需要予測単位と異なる場合、需要予測の生成時に完全にはサポートされません。

予測の生成 ( **在庫単位 > 需要予測単位**) では、製品単位の変換を使用します。 需要予測生成の履歴データを読み込む場合、バリアント レベルで変換が定義されていても、在庫単位から需要予測単位に変換するときは製品レベルの単位変換が常に使用されます。

予測の承認の最初の部分 (**需要予測単位 > 在庫単位**) では、製品単位の変換を使用します。 予測の承認の 2 番目の部分 (**在庫単位 > 販売単位**) では、バリアント単位の変換を使用します。 生成された需要予測が承認されると、需要予測単位から在庫単位への変換は、製品レベルの単位の変換を使用して行われます。 同時に、在庫単位と販売単位の間の変換では、バリアント レベルで定義された変換が考慮されます。

需要予測単位は特定の意味を持つ必要はないことに注意してください。 "需要予測単位" と定義できます。 各製品について、在庫単位を使用して変換を 1:1 に定義できます。

## <a name="additional-resources"></a>追加リソース

- [需要予測の設定](demand-forecasting-setup.md)
- [統計ベースライン予測の生成](generate-statistical-baseline-forecast.md)
- [ベースライン予測に対して手動調整を行う](manual-adjustments-baseline-forecast.md)
- [調整された需要予測の承認](authorize-adjusted-forecast.md)
- [予測精度の監視](monitor-forecast-accuracy.md)
- [需要予測を計算するときに、トランザクション履歴データから異常値を削除](remove-historical-outliers-calculating-demand-forecast.md)
- [ビデオ: 需要予測機能の拡張](https://www.youtube.com/watch?v=4OIKIXLiNjI&feature=youtu.be)
- [ウェビナー: Azure Machine Learning を使った需要予測シリーズ](https://aka.ms/DemandForecastingwithAzureMachineLearningSeries)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]

