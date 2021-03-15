---
title: キャッシュ フロー予測設定のトラブルシューティング
description: このトピックでは、キャッシュフロー予測を構成する際の質問に対する回答をご覧いただけます。 キャッシュ フロー、キャッシュ フローの更新、およびキャッシュ フロー Power BI の設定に関するよく寄せられる質問 (FAQ) を取り上げています。
author: panolte
manager: AnnBe
ms.date: 12/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerCovParameters
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: panolte
ms.search.validFrom: 2020-12-30
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: 89eb2f1bcfc73a6a7171a275532b2356e858e87c
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/15/2021
ms.locfileid: "4985290"
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

エンティティ格納の "キャッシュ フロー測定 V2" と "LedgerCovLiquidityMeasurement" 測定が構成されていることを確認します。 エンティティ格納でデータを使用する方法に関しては、[エンティティ格納を使用した Power BI 統合](../../fin-ops-core/dev-itpro/analytics/power-bi-integration-entity-store.md) を参照し、Power BI のコンテンツを表示するのに必要なすべての手順を完了していることを確認します。 詳細については、[現金の概要 Power BI コンテンツ](Cash-Overview-Power-BI-content.md) を参照してください。

## <a name="have-the-entity-store-entities-been-refreshed"></a>エンティティ格納のエンティティを更新しましたか。

データが最新かつ正確であるかを確認するために、エンティティを定期的に更新する必要があります。 特定のエンティティを手動で更新するには、**システム管理 \> 設定 \> エンティティ格納** の順に移動して、エンティティを選択してから **更新** を選択します。 データは自動的に更新することもできます。 **エンティティ格納** ページで、**自動更新を有効にする** オプションを **はい** に設定します。


[!INCLUDE[footer-include](../../includes/footer-banner.md)]