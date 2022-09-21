---
title: 製品推奨事項の有効化
description: この記事では、Microsoft Dynamics 365 Commerce の顧客が使用できる人工知能-機械学習 (AI-ML) に基づいた製品推奨事項を作成する方法について説明します。
author: bebeale
ms.date: 09/08/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail, eCommerce
ms.author: bebeale
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: fc1b43fa70e6652d38b1141e2d93cf323f70a756
ms.sourcegitcommit: f88273627ba105ede27f28fe67ccec2d7f78261c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/09/2022
ms.locfileid: "9460024"
---
# <a name="enable-product-recommendations"></a>製品推奨事項の有効化

[!include [banner](includes/banner.md)]

この記事では、Microsoft Dynamics 365 Commerce の顧客が使用できる人工知能-機械学習 (AI-ML) に基づいた製品推奨事項を作成する方法について説明します。 製品推奨事項一覧の詳細については、[製品推奨事項の概要](product-recommendations.md) を参照してください。

## <a name="recommendations-pre-check"></a>推奨事項のプレチェック

1. Dynamics 365 Commerce Recommendations の有効なライセンス持っていることを確認します。
1. エンティティ格納が顧客所有の Azure Data Lake Storage Gen2 アカウントに接続されていることを確認します。 詳細については、[Azure Data Lake Storage が購入され、環境内で正常に検証されていることを確認する](enable-ADLS-environment.md) を参照してください。
1. Azure AD ID コンフィギュレーションに推奨事項のエントリが含まれていることを確認します。 このアクションを実行する方法の詳細については、以下を参照してください。
1. エンティティ格納が毎日、Azure Data Lake Storage Gen2 に更新されるようスケジュールされていることを確認します。 詳細については、[エンティティ格納の更新が自動化されていることを確認する](../fin-ops-core/dev-itpro/data-entities/entity-store-data-lake.md) を参照してください。
1. エンティティ格納の RetailSale の測定を有効にします。 このプロセスの設定に関する詳細については、[測定の使用](/dynamics365/ai/customer-insights/pm-measures)を参照してください。
1. 環境で、現在サポート対象リージョンでサービス提供リージョンとクッキング リージョンが次のように構成されていることを確認します:

    - **サポート対象クッキング リージョン:** EU/US/CA/AU。
    - **サポート対象サービス提供リージョン:** US/CA/AU。 サービス提供リージョンが既存のサポート対象リージョンのいずれかに合わない場合、推奨事項サービスは最も近いサポート対象サービス提供リージョンを選択します。

上記の手順が完了した後、推奨事項を有効にすることができます。

> [!NOTE]
> 次の手順の完了後に推奨事項が表示されない既知の問題があります。 この問題は、環境内のデータ フローの問題によって発生します。 環境に推奨事項の結果が表示されない場合は、[推奨事項用の代替データフローの設定](set-up-alternate-data-flow.md) の手順に従って、推奨事項サービスの代替データを構成します。 これらの手順を完了するには、Azure 管理者のアクセス許可が必要です。 サポートが必要な場合は、FastTrack 担当者に問い合わせください。

## <a name="azure-ad-identity-configuration"></a>Azure AD ID コンフィギュレーション

この手順は、サービスとしてのインフラストラクチャ (IaaS) 構成を実行する顧客にのみ必要です。 Azure AD ID コンフィギュレーションは、Azure Service Fabric 上で実行する顧客に対して自動的に行われますが、設定が予想どおりに構成されていることを確認することをお勧めします。

### <a name="setup"></a>設定

1. Commerce 本社で、**Azure Active Directory アプリケーション** ページを検索します。
1. **RecommendationSystemApplication-1** のエントリが存在するかどうかを確認します。 エントリが存在しない場合、次の情報を使用して作成します。

    - **クライアント ID**: d37b07e8-dd1c-4514-835d-8b918e6f9727
    - **名前**: RecommendationSystemApplication-1
    - **ユーザー ID**: RetailServiceAccount

1. ページを保存して閉じる。 

## <a name="turn-on-recommendations"></a>推奨事項を有効にする

製品推奨事項を有効にするには、次の手順を実行します。

1. Commerce Headquarters で、**機能管理** を検索します。
1. **すべて** を選択して、使用可能な機能の一覧を表示します。 
1. 検索ボックスに、**推奨事項** を入力します。
1. **製品推奨事項** 機能を選択します。
1. **製品推奨事項** プロパティ ペインで、**直ちに有効化** を選択します。

![推奨事項の有効化。](./media/FeatureManagement_Recommendations.PNG)

> [!NOTE]
> - 上記の手順により、製品推奨リストを生成するプロセスを開始します。 リストが有効になり、販売時点管理 (POS) または Dynamics 365 Commerce で表示できるようになるまでに、数時間かかる場合があります。
> - この構成により、すべての推奨事項機能が有効になるわけではありません。 「同じような商品を探す」および「同じような説明を探す」といったカスタマイズされた推奨事項などのより高度な機能は、専用の機能管理エントリによって制御されます。 Commerce 本社でこれらの機能を有効にする方法の詳細については、[パーソナライズされた推奨事項の有効化](personalized-recommendations.md)、["同じような商品を探す" 推奨事項の有効化](shop-similar-looks.md)、および ["同じような説明を探す" 推奨事項の有効化](shop-similar-description.md)を参照してください。

## <a name="configure-recommendation-list-parameters"></a>推奨リスト パラメーターのコンフィギュレーション

既定では、AI-ML ベースの製品推奨リストは推奨値を提供します。 業務の流れに合わせて、既定の推奨値を変更できます。 既定のパラメーターを変更する方法の詳細については、[AI-ML ベースの製品推奨事項結果の管理](modify-product-recommendation-results.md)を参照してください。

## <a name="include-recommendations-in-e-commerce-experiences"></a>e コマースのエクスペリエンスに推奨事項を含める

Commerce 本社で推奨事項を有効にした後、e コマース エクスペリエンスの推奨事項の結果を表示するために使用される Commerce モジュールが構成されます。 詳細については、[製品収集モジュール](product-collection-module-overview.md)を参照してください。

## <a name="show-recommendations-on-pos-devices"></a>POS デバイスの推奨事項を表示する

Commerce 本社で推奨事項を有効にした後、レイアウト ツールを使用して、推奨事項パネルをコントロール POS 画面に追加する必要があります。 このプロセスの詳細については、[POS デバイスのトランザクション画面への推奨設定コントロールの追加](add-recommendations-control-pos-screen.md) を参照してください。 

## <a name="enable-personalized-recommendations"></a>カスタマイズされた推奨事項の有効化

Dynamics 365 Commerce では、小売業者がパーソナライズされた製品推奨事項 (個人用設定とも呼ばれます) を使用可能にすることができます。 この方法で、カスタマイズされた推奨事項をオンラインの顧客エクスペリエンスおよび販売時点管理に組み込むことができます。 個人用設定機能をオンにすると、システムはユーザーの購入情報と製品情報を関連付けて、個別の製品推奨事項を生成できます。

カスタマイズされた推奨事項の詳細については、[カスタマイズされた推奨事項の有効化](personalized-recommendations.md) を参照してください。

## <a name="additional-resources"></a>追加リソース

[製品推奨事項の概要](product-recommendations.md)

[Dynamics 365 Commerce 環境で Azure Data Lake Storage を有効化する](enable-adls-environment.md)

[推奨事項用の代替データ フローの設定](set-up-alternate-data-flow.md)

[カスタマイズされた推奨事項の有効化](personalized-recommendations.md)

["同じような商品を探す" 推奨事項の有効化](shop-similar-looks.md)

[カスタマイズされた推奨事項のオプト アウト](personalization-gdpr.md)

[POS での製品推奨事項の追加](product.md)

[トランザクション画面への推奨設定の追加](add-recommendations-control-pos-screen.md)

[AI-ML 推奨事項結果の調整](modify-product-recommendation-results.md)

[収集された推奨事項の手動作成](create-editorial-recommendation-lists.md)

[推奨事項とデモ データの作成](product-recommendations-demo-data.md)

[製品推奨事項に関するよく寄せられる質問](faq-recommendations.md)




[!INCLUDE[footer-include](../includes/footer-banner.md)]
