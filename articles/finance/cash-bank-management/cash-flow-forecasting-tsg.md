---
title: キャッシュ フロー予測設定のトラブルシューティング
description: このトピックでは、キャッシュフロー予測を構成する際の質問に対する回答をご覧いただけます。 キャッシュ フロー、キャッシュ フローの更新、およびキャッシュ フロー Power BI の設定に関するよく寄せられる質問 (FAQ) を取り上げています。
author: panolte
ms.date: 03/23/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: LedgerCovParameters
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: panolte
ms.search.validFrom: 2020-12-30
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: 39860a1960706aae7d223c8d2e810d39edc41b11deb80026925e6655f8e23ee8
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/05/2021
ms.locfileid: "6747182"
---
# <a name="troubleshoot-cash-flow-forecasting-setup"></a>キャッシュ フロー予測設定のトラブルシューティング

[!include [banner](../includes/banner.md)]

このトピックでは、キャッシュフロー予測を構成する際の質問に対する回答をご覧いただけます。 キャッシュ フロー、キャッシュ フローの更新、およびキャッシュ フロー Power BI の設定に関するよく寄せられる質問 (FAQ) を取り上げています。

## <a name="why-is-cash-flow-shown-for-only-one-legal-entity"></a>キャッシュ フローが単一の法人に対してのみ表示される理由

キャッシュ フロー予測は、法人ごとに構成および計算されます。 Finance 分析情報の Power BI レポートおよびキャッシュ フロー予測機能が結果を表示します。

キャッシュ フロー予測は、予測を確認したい法人ごとに設定する必要があります。 すべての法人におけるキャッシュ フロー予測の構成を確認します。 または、キャッシュ フロー予測のすべての法人の構成を確認し、予定通りに設定されているかを確認します。

## <a name="why-doesnt-power-bi-show-all-the-cash-flow-data"></a>Power BI がすべてのキャッシュ フロー データを表示しないのはなぜですか。

キャッシュ フロー予測が Power BI ビューに表示される前に、いくつかの手順を実行する必要があります。 次のチェックリストを確認し、すべての手順が完了しているかを確認します。

- 各法人のキャッシュ フローを設定します。
- 一般会計パラメーターで、システム通貨とシステムの為替レート タイプを設定します。
- 元帳の会計通貨と為替レート タイプを設定します。
- 取引通貨と会計通貨間の為替レートを入力します。
- 会計通貨とシステム通貨間の為替レートを入力します。
- 会計通貨と各銀行通貨間の為替レートを入力します。

## <a name="why-did-cash-flow-power-bi-work-in-previous-versions-but-is-now-blank"></a>以前のバージョンでキャッシュ フロー Power BI を使用できたのに、今はなぜ空白なのですか。

エンティティ格納の "キャッシュ フロー測定 V2" と "LedgerCovLiquidityMeasurement" 測定が構成されていることを確認します。 エンティティ ストアの使用方法については、[エンティティストアとのPower BI 統合](../../fin-ops-core/dev-itpro/analytics/power-bi-integration-entity-store.md)を参照してください。 Power BI コンテンツを表示するのに必要なすべての手順が完了していることを確認します。 詳細については、[現金の概要 Power BI コンテンツ](Cash-Overview-Power-BI-content.md) を参照してください。

## <a name="have-the-entity-store-entities-been-refreshed"></a>エンティティ格納のエンティティを更新しましたか。

データが最新かつ正確であるかを確認するために、エンティティを定期的に更新する必要があります。 特定のエンティティを手動で更新するには、**システム管理 \> 設定 \> エンティティ格納** の順に移動して、エンティティを選択してから **更新** を選択します。 データは自動的に更新することもできます。 **エンティティ格納** ページで、**自動更新を有効にする** オプションを **はい** に設定します。

## <a name="which-calculation-method-should-be-used-when-calculating-cash-flow-forecasts"></a>キャッシュフロー予測を計算する際に使用すべき計算方法はどれですか?

キャッシュ フロー予測計算方法には、2 つの重要な選択オプションがあります。 **新規** オプションの場合、新規ドキュメントおよび前回のバッチ ジョブ実行後に変更があったドキュメントのキャッシュ フロー予測を計算します。 このオプションは、処理するドキュメントのサブセットが小さいため、短時間で終わる傾向があります。 **合計** オプションでは、システム内のすべてのドキュメントに対してキャッシュ フロー予測を再計算します。 このオプションでは、完了する作業が多いため時間がかかります。

### <a name="how-do-i-improve-the-performance-of-the-cash-flow-forecasting-recurring-batch-job"></a>キャッシュ フロー予測の定期バッチ ジョブのパフォーマンスを向上させるにはどうすればいいですか?

キャッシュ フローは毎日一回、**新規** 計算方法を使ってオフピーク時間中に実行することを推奨しています。 週に 6 回このアプローチを使用することをお勧めします。 次に、毎週一回アクティビティが最も少ない日に、**合計** 計算方法を使ってキャッシュ フロー予測を実行します。

[!INCLUDE[footer-include](../../includes/footer-banner.md)]

