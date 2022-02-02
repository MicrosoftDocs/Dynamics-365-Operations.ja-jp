---
title: Finance Insights ホーム ページ
description: Finance insights には構成可能かつ拡張可能なモデルが用意されており、会社のキャッシュフローを正確かつ的確に予測したり、未払の債権に対する支払をいつ受け取るかを予測したり、予算作成プロセスを高速化するための予算案を生成できます。 これらの機能はすべて、インテリジェントな機械学習モデルに基づいています。
author: ShivamPandey-msft
ms.date: 11/15/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: twheeloc
ms.custom:
- "14151"
- intro-internal
ms.assetid: 3d43ba40-780c-459a-a66f-9a01d556e674
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2020-07-20
ms.dyn365.ops.version: AX 10.0.13
ms.openlocfilehash: 8cc7b2d733cdcf1adef2885b7900ea312a10d98c
ms.sourcegitcommit: 133aa728b8a795eaeaef22544f76478da2bd1df9
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/13/2022
ms.locfileid: "7968813"
---
# <a name="finance-insights-home-page"></a>Finance Insights ホーム ページ

[!include [banner](../includes/banner.md)]

Finance Insights には構成可能かつ拡張可能なソリューションが用意されており、会社のキャッシュ フローを的確に予測したり、未払の債権に対する支払をいつ受け取るかを予測したり、予算作成プロセスを高速化するための予算案を生成できます。 これらの機能では、インテリジェントな機械学習テンプレートを使用して、提供されたデータ (ビューローからの消費者レポート情報など、サード パーティからのデータを含む) を使用してモデルを構築します。 これらのインテリジェントな機能は、意思決定に役立ち、現在および予想されるビジネス上の課題に効果的に対応するための行動を支援します。 ユーザーは、Finance Insights で使用または出力されるデータについて責任を負います。

> [!NOTE]
> Finance Insights は、アメリカ合衆国、カナダ、イギリス、ヨーロッパ、アジア太平洋、日本、オーストラリア、ニュージーランドで配置することができます。 Microsoft は、より多くの地域に対するサポートを段階的に追加しています。

## <a name="prerequisites"></a>必要条件

このセクションでは、Finance insights を使用するための要件を示します。 可能な限り、追加情報のソースへのリンクが提供されます。

### <a name="legal-requirements"></a>法的要件

プレビュー プログラムを申請するには、[Dynamics 365 Finance 契約の Finance insights プレビュー](https://forms.office.com/FormsPro/Pages/ResponsePage.aspx?id=v4j5cvGGr0GRqy180BHbR56j8lZs0FdAvwT75_WNFyxUM1c0Uzc1RFpaU1RVTEwxVTNWUERPRThUSy4u) を記入してください。

### <a name="system-requirements"></a>システム要件

財務分析情報をプレビューするには、Tier 2 環境 (複数のボックス) が必要です。 環境に関するバックグラウンド情報については、[環境計画](../../fin-ops-core/fin-ops/imp-lifecycle/environment-planning.md) を参照してください。

### <a name="version-requirements"></a>バージョン要件

このトピックは、Microsoft Dynamics 365 Finance バージョン 10.0.21 およびそれ以降に適用されます。

### <a name="historical-data-requirements"></a>履歴データ要件

顧客支払予測機能に使用される機械学習モデルを正しくトレーニングするには、少なくとも 1 年分の顧客請求書が必要です。 キャッシュ フロー予測では、3 年間の履歴データが推奨されます。 インテリジェントな予算案では、3 年間の予算履歴や実績が推奨されます。

## <a name="configure-finance-insights"></a>Finance insights のコンフィギュレーション

Finance Insights を使用する前に、コンフィギュレーション ステップを完了する必要があります。 Finance 分析情報のコンフィギュレーション方法の詳細については、[Finance 分析情報のコンフィギュレーション](configure-for-fin-insites.md) を参照してください。

## <a name="create-a-data-integrator-project"></a>データ インテグレーター プロジェクトの作成

機械学習モデルで生成されるデータを Dynamics 365 Finance に渡すことができるように、データ インテグレーター プロジェクトを作成する必要があります。 そのプロジェクトを作成するステップについては、[データ インテグレーター プロジェクトの作成](create-data-integrate-project.md) を参照してください。

## <a name="enable-finance-insights-capabilities"></a>Finance insights の機能を有効にする

コンフィギュレーション ステップを完了し、デモ データを設定したら、使用する各機能 (顧客支払予測、キャッシュフロー予測、および予算提案) を有効にして設定する必要があります。

### <a name="enable-customer-payment-predictions"></a>顧客支払予測の有効化
デモ データを使用して顧客支払予測をテストする場合、追加のデモ データをインポートして AI モデルを正しく作成する必要があります。 

顧客支払予測を有効にするには、一連のステップを実行して、顧客が未払の請求書の支払を行う可能性がある場合や、特定の請求書の支払が見込まれる時期についての予測を生成する、組織のデータを使用する機械学習モデルを構築する必要があります。 詳細と完了する特定のステップについては、[顧客支払予測の有効化](enable-cust-paymnt-prediction.md) を参照してください。 

### <a name="enable-cash-flow-forecasting"></a>キャッシュ フロー予測の有効化
キャッシュフロー予測を有効にするには、一連のステップを実行して、組織のデータを使用してキャッシュフロー予測を生成する機械学習モデルを構築する必要があります。 詳細と完了する特定のステップについては、[キャッシュフロー予測の有効化](enable-cash-flow-forecasting.md) を参照してください。

### <a name="enable-budget-proposals"></a>予算案の有効化

予算案機能は、機械学習モデルと組織の履歴データを使用して予算案を生成します。 生成された提案は、手動のプロセスよりも効果的かつ効率的な予算編成プロセスを開始するのに役立ちます。 この機能を有効にするための具体的なステップについては、[予算提案の有効化](enable-budget-proposal.md) を参照してください。 

## <a name="using-finance-insights-features"></a>Finance insights の機能の使用

### <a name="using-customer-payment-predictions"></a>顧客支払予測の使用

- 顧客支払予測によって事前に回収活動を開始するために必要な情報をどのように提供するかについては、[顧客支払予測の使用](use-customer-payment-predictions.md) を参照してください。
- この機能の使用を開始した後に予測モデルの有効性を評価するのに役立つ情報については、[最初の顧客支払予測モデルを評価する](evaluate-payment-prediction.md) を参照してください。
- 予測を構築し、その結果を改善するために使用されるデータの調整に役立つ情報については、[予測モデルの改善](improve-model.md) を参照してください。
- AI 予測モデルの結果についての詳細は、[機械学習モデルの結果](confusion-matrix.md) を参照してください。

### <a name="using-cash-flow-forecasts"></a>キャッシュ フロー予測の使用

キャッシュフロー予測機能は、現金の位置をより正確に見積もるために役立ちます。 インテリジェント キャッシュフロー予測は、Dynamics 365 Finance の既存のキャッシュフロー予測機能の上位に構築されます。 既存の機能を確認する方法については、[キャッシュフロー予測](../cash-bank-management/cash-flow-forecasting.md) を参照してください。

- キャッシュ フロー予測の新機能については、[キャッシュ フロー予測](cash-flow-forecast-intro.md) を参照してください。
- ここでキャッシュフロー予測に含める外部データのインポートについては、[外部データをキャッシュフロー予測に使用する](external-data-in-cash-flow.md) を参照してください。 
- AI モデルを使用して短期的なキャッシュフローを予測する方法の詳細については、[キャッシュ ポジション](cash-position.md) を参照してください。
- キャッシュフローの位置およびキャッシュフロー予測をスナップショットとして保存する方法、およびスナップショットを実績と比較する方法については、[スナップショットの概要](payment-snapshots.md) を参照してください。

### <a name="using-budget-proposal"></a>予算案の使用

予算作成の迅速化については、[予算案](budget-proposals.md) を参照してください。 

## <a name="feedback-and-support"></a>フィードバックとサポート

フィードバックに興味のある方、サポートが必要な方は、[Finance Insights](mailto:fiap@microsoft.com) にメールでお問い合わせください。

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
