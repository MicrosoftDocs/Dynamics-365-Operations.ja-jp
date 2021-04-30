---
title: Finance 分析情報のホーム ページ (プレビュー)
description: Finance 分析情報には構成可能かつ拡張可能なモデルが用意されており、会社のキャッシュフローを正確かつ的確に予測したり、未払の債権に対する支払をいつ受け取るかを予測したり、予算作成プロセスを高速化するための予算案を生成できます。 これらの機能はすべて、インテリジェントな機械学習モデルに基づいています。
author: ShivamPandey-msft
ms.date: 07/20/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 14151
ms.assetid: 3d43ba40-780c-459a-a66f-9a01d556e674
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2020-07-20
ms.dyn365.ops.version: AX 10.0.13
ms.openlocfilehash: b1f034017c2cd8736c1e3ce286924bf305961390
ms.sourcegitcommit: 7d0cfb359a4abc7392ddb3f0b3e9539c40b7204d
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/14/2021
ms.locfileid: "5898063"
---
# <a name="finance-insights-home-page-preview"></a>Finance 分析情報のホーム ページ (プレビュー)

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

Finance 分析情報には構成可能かつ拡張可能なモデルが用意されており、会社のキャッシュフローを正確かつ的確に予測したり、未払の債権に対する支払をいつ受け取るかを予測したり、予算作成プロセスを高速化するための予算案を生成できます。 これらの機能はすべて、インテリジェントな機械学習モデルに基づいています。 これらの新しい機能を、仕入先の支払および回収の自動化と組み合わせると、意思決定を推進し、現在および将来のビジネス課題に効果的に対応するための行動を取ることのできる、高度でインテリジェントな財務システムが提供されます。

Finance 分析情報のプレビューは、米国、ヨーロッパ、および英国での試用版の配置に使用できます。 Microsoft は、より多くの地域に対するサポートを段階的に追加しています。

プレビュー機能は、Tier-2 のサンドボックス環境でのみ有効にすることができます。 サンドボックス環境で作成された設定および人工知能 (AI) モデルは、運用環境に移行できません。 詳細については、[Microsoft Dynamics 365 プレビューの補足の使用条件](/dynamics365/legal/supp-dynamics365-preview#:~:text=Supplemental%20Terms%20of%20Use%20for%20Microsoft%20Dynamics%20365,%28governing%20your%20use%20of%20Microsoft%20Dynamics%20365%20Online%29.) を参照してください。

## <a name="prerequisites"></a>必要条件

このセクションでは、Finance 分析情報を使用するための要件を示します。 可能な限り、追加情報のソースへのリンクが提供されます。

### <a name="legal-requirements"></a>法的要件

プレビュー プログラムを申請するには、[Dynamics 365 Finance 契約の Finance 分析情報プレビュー](https://forms.office.com/FormsPro/Pages/ResponsePage.aspx?id=v4j5cvGGr0GRqy180BHbR56j8lZs0FdAvwT75_WNFyxUM1c0Uzc1RFpaU1RVTEwxVTNWUERPRThUSy4u) を記入してください。

### <a name="system-requirements"></a>システム要件

Finance 分析情報をプレビューするには、Tier 2 サンドボックス環境 (複数のボックス) が必要です。 環境に関するバックグラウンド情報については、[環境計画](../../fin-ops-core/fin-ops/imp-lifecycle/environment-planning.md) を参照してください。

### <a name="version-requirements"></a>バージョン要件

このドキュメントは、Finance and Operations アプリのバージョン 10.0.11 (プラットフォームの更新プログラム 35) およびそれ以降のバージョンに適用されます。

### <a name="historical-data-requirements"></a>履歴データ要件

顧客支払予測機能に使用される機械学習モデルを正しくトレーニングするには、少なくとも 1 年分の顧客請求書が必要です。

サンプル データは、Contoso デモ データ セットが設定されているデモ システムで使用できます。

### <a name="role-and-permission-requirements"></a>ロールとアクセス許可の要件

Microsoft Dynamics 365 Finance、Microsoft Dynamics Lifecycle Services (LCS)、Power Apps、Azureに変更が加えられます。 これらの環境に対して適切なアクセス許可を設定する必要があります。 対象となる変更の一部の例を次に示します。

- 新しい環境は、Microsoft Power Platform に作成されます。
- ストレージ アカウント、Key Vault、アプリケーションが Azure に作成されます。
- Active Directory テナント管理者は、Data Lake にアクセスするには、AI Builder アプリケーションを承認する必要があります。
- この機能は Dynamics 365 で有効になります。

Azure、Microsoft Dataverse、LCS のリソースを作成および管理するプロセスに関する知識は、このプロセスを完了するために役立ちます。

## <a name="configure-finance-insights"></a>Finance 分析情報のコンフィギュレーション

Finance 分析情報を使用する前に、いくつかのコンフィギュレーション ステップを完了する必要があります。 Finance 分析情報のコンフィギュレーション方法の詳細については、[Finance 分析情報のコンフィギュレーション](configure-for-fin-insites.md) を参照してください。

## <a name="create-a-data-integrator-project"></a>データ インテグレーター プロジェクトの作成

機械学習モデルで生成されるデータを Dynamics 365 Finance に渡すことができるように、データ インテグレーター プロジェクトを作成する必要があります。 そのプロジェクトを作成するステップについては、[データ インテグレーター プロジェクトの作成](create-data-integrate-project.md) を参照してください。

## <a name="enable-finance-insights-capabilities"></a>Finance 分析情報機能を有効にする

コンフィギュレーション ステップを完了し、デモ データを設定したら、使用する各機能 (顧客支払予測、キャッシュフロー予測、および予算提案) を有効にして設定する必要があります。

### <a name="enable-customer-payment-predictions"></a>顧客支払予測の有効化
デモ データを使用して顧客支払予測をテストする場合、追加のデモ データをインポートして AI モデルを正しく作成する必要があります。 

顧客支払予測を有効にするには、一連のステップを実行して、顧客が未払の請求書の支払を行う可能性がある場合や、特定の請求書の支払が見込まれる時期についての予測を生成する、組織のデータを使用する機械学習モデルを構築する必要があります。 詳細と完了する特定のステップについては、[顧客支払予測の有効化](enable-cust-paymnt-prediction.md) を参照してください。 

### <a name="enable-cash-flow-forecasting"></a>キャッシュ フロー予測の有効化
キャッシュフロー予測を有効にするには、一連のステップを実行して、組織のデータを使用してキャッシュフロー予測を生成する機械学習モデルを構築する必要があります。 詳細と完了する特定のステップについては、[キャッシュフロー予測の有効化](enable-cash-flow-forecasting.md) を参照してください 

### <a name="set-up-and-use-cash-flow-forecasting"></a>キャッシュフロー予測の設定と使用
キャッシュ フロー予測の設定と使用の詳細については、[キャッシュ フロー予測の有効化](enable-cash-flow-forecasting.md) を参照してください。 この機能の使い方についての詳細については、[キャッシュ フロー予測](cash-flow-forecast-intro.md) を参照してください。

### <a name="enable-budget-proposals"></a>予算案の有効化

予算案機能は、機械学習モデルと組織の履歴データを使用して予算案を生成します。 生成された提案は、手動のプロセスよりも効果的かつ効率的な予算編成プロセスを開始するのに役立ちます。 この機能を有効にするための具体的なステップについては、[予算提案の有効化](enable-budget-proposal.md) を参照してください。 

## <a name="using-finance-insights-features"></a>Finance 分析情報機能の使用

### <a name="using-customer-payment-predictions"></a>顧客支払予測の使用

インテリジェント キャッシュフロー予測は、Dynamics 365 Finance の既存のキャッシュフロー予測機能の上位に構築されます。 既存の機能を確認する方法については、[キャッシュフロー予測](../cash-bank-management/cash-flow-forecasting.md) を参照してください。

- 顧客支払予測によって事前に回収活動を行うために必要な情報をどのように提供するかについては、[顧客支払予測の使用](use-customer-payment-predictions.md) を参照してください。
- この機能の使用を開始した後に予測モデルの有効性を評価するのに役立つ情報については、[最初の顧客支払予測モデルを評価する](evaluate-payment-prediction.md) を参照してください。
- 予測を構築し、その結果を改善するために使用されるデータの調整に役立つ情報については、[予測モデルの改善](improve-model.md) を参照してください。

AI 予測モデルの結果についての詳細は、[機械学習モデルの結果](confusion-matrix.md) を参照してください。

### <a name="using-cash-flow-forecasts"></a>キャッシュ フロー予測の使用

キャッシュフロー予測機能は、現金の位置をより正確に見積もるために役立ちます。 

- キャッシュフロー予測の新機能については、[キャッシュフロー予測](cash-flow-forecast-intro.md) を参照してください。
- ここでキャッシュフロー予測に含める外部データのインポートについては、[外部データをキャッシュフロー予測に使用する](external-data-in-cash-flow.md) を参照してください。 
- AI モデルを使用して長期的なキャッシュフローを予測する方法の詳細については、[キャッシュフロー予測の概要](cash-position.md) を参照してください。
- キャッシュフローの位置およびキャッシュフロー予測をスナップショットとして保存する方法、およびスナップショットを実績と比較する方法については、[スナップショットの概要](payment-snapshots.md) を参照してください。

### <a name="using-budget-proposal"></a>予算案の使用

予算作成の迅速化については、[予算案](budget-proposals.md) を参照してください。 

予算案のデモデータ:

## <a name="feedback-and-support"></a>フィードバックとサポート

フィードバックの提供またはサポートが必要な場合は、[顧客支払い分析情報 (プレビュー)](mailto:fiap@microsoft.com) に電子メールを送信してください。

## <a name="privacy-notice"></a>プライバシー通知

プレビューは (1) Dynamics 365 Finance and Operations サービスを下回るプライバシーおよび少ないセキュリティ対策を使用している場合があり、(2) このサービスのためにサービス レベル アグリーメント (SLA) には含まれておらず、(3) 個人データや、その他の法律上またはコンプライアンス要件の対象となるデータの処理に使用されず、(4) サポートが制限されます。


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
