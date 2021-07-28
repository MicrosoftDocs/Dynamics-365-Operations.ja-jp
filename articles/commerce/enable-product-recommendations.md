---
title: 製品推奨事項の有効化
description: このトピックでは、Microsoft Dynamics 365 Commerce の顧客が使用できる人為知能の機械学習 (AI-ML) に基づいた製品推奨事項を作成する方法について説明します。
author: bebeale
ms.date: 08/18/2020
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
ms.openlocfilehash: 0a94a74f4eb00c24142f0390bcf352db0594ca0b
ms.sourcegitcommit: c08a9d19eed1df03f32442ddb65a2adf1473d3b6
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 07/06/2021
ms.locfileid: "6349475"
---
# <a name="enable-product-recommendations"></a>製品推奨事項の有効化

[!include [banner](includes/banner.md)]

このトピックでは、Microsoft Dynamics 365 Commerce の顧客が使用できる人為知能の機械学習 (AI-ML) に基づいた製品推奨事項を作成する方法について説明します。 製品推奨事項一覧の詳細については、[製品推奨事項の概要](product-recommendations.md) を参照してください。

## <a name="recommendations-pre-check"></a>推奨事項のプレチェック

有効にする前に、製品の推奨事項は、Azure Data Lake Storage を使用するようにストレージを移行した Commerce の顧客に対してのみサポートされていることに注意してください。 

推奨事項を有効にするには、次のコンフィギュレーションをバック オフィスで有効にする必要があります。

1. Azure Data Lake Storage が購入され、環境内で正常に検証されていることを確認します。 詳細については、[Azure Data Lake Storage が購入され、環境内で正常に検証されていることを確認する](enable-ADLS-environment.md) を参照してください。
2. エンティティ格納の更新が自動化されていることを確認します。 詳細については、[エンティティ格納の更新が自動化されていることを確認する](../fin-ops-core/dev-itpro/data-entities/entity-store-data-lake.md) を参照してください。
3. Azure AD ID コンフィギュレーションに推奨事項のエントリが含まれていることを確認します。 このアクションを実行する方法の詳細については、以下を参照してください。

さらに、RetailSale の測定が有効になっていることを確認します。 この設定プロセスの詳細については、[測定の使用](/dynamics365/ai/customer-insights/pm-measures) を参照してください。

## <a name="azure-ad-identity-configuration"></a>Azure AD ID コンフィギュレーション

この手順は、サービス (IaaS) コンフィギュレーションとしてのインフラストラクチャを実行するすべての顧客に必要です。 Service Fabric (SF) で実行している顧客については、この手順が自動的に行われ、設定が予想どおりに構成されていることを確認することをお勧めします。

### <a name="setup"></a>セットアップ

1. バック オフィスから、**Azure Active Directory アプリケーション** ページを検索します。
2. "RecommendationSystemApplication-1" のエントリが存在するかどうかを確認します。

エントリが存在しない場合は、次の情報を含む新しいエントリを追加します:

- **クライアント ID** - d37b07e8-dd1c-4514-835d-8b918e6f9727
- **名前** - RecommendationSystemApplication-1
- **ユーザー ID** - RetailServiceAccount

ページを保存して閉じる。 

## <a name="turn-on-recommendations"></a>推奨事項を有効にする

製品推奨事項を有効にするには、次の手順を実行します。

1. Commerce Headquarters で、**機能管理** を検索します。
1. **すべて** を選択して、使用可能な機能の一覧を表示します。 
1. 検索ボックスに、**推奨事項** を入力します。
1. **製品推奨事項** 機能を選択します。
1. **製品推奨事項** プロパティ ペインで、**直ちに有効化** を選択します。

![推奨事項の有効化。](./media/FeatureManagement_Recommendations.PNG)

> [!NOTE]
> この手順では、製品推奨リストを生成するプロセスを開始します。 リストが有効になり、販売時点管理 (POS) または Dynamics 365 Commerce で表示できるようになるまでに、数時間かかる場合があります。

## <a name="configure-recommendation-list-parameters"></a>推奨リスト パラメーターのコンフィギュレーション

既定では、AI-ML ベースの製品推奨リストは推奨値を提供します。 業務の流れに合わせて、既定の推奨値を変更できます。 既定のパラメーターを変更する方法の詳細については、[AI-ML ベースの製品推奨事項結果の管理](modify-product-recommendation-results.md)を参照してください。

## <a name="show-recommendations-on-pos-devices"></a>POS デバイスの推奨事項を表示する

Commerce バック オフィスで推奨事項を有効にした後、レイアウト ツールを使用して、推奨事項パネルをコントロール POS 画面に追加する必要があります。 このプロセスの詳細については、[POS デバイスのトランザクション画面への推奨設定コントロールの追加](add-recommendations-control-pos-screen.md) を参照してください。 

## <a name="enable-personalized-recommendations"></a>カスタマイズされた推奨事項の有効化

Dynamics 365 Commerce では、小売業者がパーソナライズされた製品推奨事項 (個人用設定とも呼ばれます) を使用可能にすることができます。 この方法で、カスタマイズされた推奨事項をオンラインの顧客エクスペリエンスおよび販売時点管理に組み込むことができます。 個人用設定機能をオンにすると、システムはユーザーの購入情報と製品情報を関連付けて、個別の製品推奨事項を生成できます。

カスタマイズされた推奨事項の詳細については、[カスタマイズされた推奨事項の有効化](personalized-recommendations.md) を参照してください。

## <a name="additional-resources"></a>追加リソース

[製品推奨事項の概要](product-recommendations.md)

[Dynamics 365 Commerce 環境で Azure Data Lake Storage を有効化する](enable-adls-environment.md)

[カスタマイズされた推奨事項の有効化](personalized-recommendations.md)

["類似したルックを買う" 推奨を有効にする](shop-similar-looks.md)

[カスタマイズされた推奨事項のオプト アウト](personalization-gdpr.md)

[POS での製品推奨事項の追加](product.md)

[トランザクション画面への推奨設定の追加](add-recommendations-control-pos-screen.md)

[AI-ML 推奨事項結果の調整](modify-product-recommendation-results.md)

[収集された推奨事項の手動作成](create-editorial-recommendation-lists.md)

[推奨事項とデモ データの作成](product-recommendations-demo-data.md)

[製品推奨事項に関するよく寄せられる質問](faq-recommendations.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]