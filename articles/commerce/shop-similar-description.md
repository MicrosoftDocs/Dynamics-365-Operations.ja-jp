---
title: "\"同じような説明を探す\" 推奨事項の有効化"
description: このトピックでは、Microsoft Dynamics 365 Commerce で、"同じような説明を探す" 製品推奨事項を有効にする方法について説明します。
author: bsokolov
manager: AnnBe
ms.date: 01/13/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail, eCommerce
ms.author: bebeale
ms.search.validFrom: 2021-01-31
ms.dyn365.ops.version: 10.0.16
ms.openlocfilehash: b6b397b1f21e3dfcdb4a2b7fe67ddb541d090a97
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/15/2021
ms.locfileid: "5234392"
---
# <a name="enable-shop-similar-description-recommendations"></a>"同じような説明を探す" 推奨事項の有効化

[!include [banner](includes/banner.md)]

このトピックでは、Microsoft Dynamics 365 Commerce で、"同じような説明を探す" 製品推奨事項を有効にする方法について説明します。

Dynamics 365 Commerce の「類似した説明を探す」 のおすすめ候補機能は、人工知能と機械学習 (AI-ML) を使って、顧客が探しているものと似たような記述のある商品を推奨してくれます。 Commerce のすべての小売チャネルで「類似した説明を探す」のおすすめ候補を利用できるようにすることで、小売業者は顧客が欲しいものを簡単に見つけることができます。

「類似した説明を探す」のおすすめ候補機能は、種子製品の製品名と説明を使用して、小売業者の製品カタログから類似製品を検索して推奨します。

「類似した説明を探す」 のレコメンドは、販売時点管理 (POS) と eコマースの両方のエクスペリエンスで利用可能です。

## <a name="example-scenarios"></a>シナリオ例

以下のシナリオ例では、「類似した説明を探す」機能が提供できるお推奨タイプを示しています。

- 顧客は、レトロスタイルの角縁メガネを見て、小売業者の業界の文脈で、似たようなデザインの他のメガネのおすすめ候補のセットを受け取ります。
- 顧客は、以前に小売業者から購入したコーヒーの味を発見するために「類似した説明を探す」のおすすめ候補機能を使用しています。

## <a name="set-up-shop-similar-description-recommendations"></a>「類似した説明を探す」おすすめ候補機能の有効化

製品の推奨は、ストレージを Azure Data Lake Storage  Gen2 に移行した Commerce ユーザーのみがサポートされます。

### <a name="prerequisites"></a>必要条件

「類似した説明を探す」のおすすめ候補を顧客に表示するには、次の前提条件を満たす必要があります。

- Commerce 本社での [製品推奨を有効にします](enable-product-recommendations.md)。
- メディア サーバーが HTTPS 呼び出しをサポートしていることを確認します。

### <a name="turn-on-the-shop-similar-description-recommendations-feature"></a>「おすすめ候補」 おすすめ候補の有効化

Commerce 本部の「類似した説明を探す」おすすめ候補機能をオンにするには、以下の手順に従います。

1. **機能管理**  ワークスペースで、利用可能な機能の一覧から、**類似した説明を探す** を検索します。
1. 右側のペインで、**有効化** を選択します。

> [!NOTE]
> 機能をオンにすると、商品のおすすめ候補リストの生成を開始します。 これらのリストが利用可能になり、オンラインや POS 端末で確認できるようになるまでには、最大で 1 日かかる場合があります。
>
> この機能をオフにした場合でも、他のタイプの製品推奨事項には影響されません。 製品推奨の詳細については、[製品推奨の概要](product-recommendations.md) を参照してください。

## <a name="add-a-shop-similar-description-button-to-product-details-pages"></a>「類似した説明を探す」ボタンを製品の詳細ページに追加する

Commerce 本部のおすすめ候補機能 「類似した説明を探す」 をオンにした後、任意の商品詳細ページ (PDP) の購入ボックスに **類似した説明を探す** ボタンを追加することができます。 このボタンを選択した顧客は、視覚的に類似した商品を表示する専用の **類似した説明を探す** ページに移動します。 顧客はセレクターを使用して、製品をさらに詳細にフィルタ処理することができます。

Commerce サイト ビルダーを使用することで、**類似した説明を探す** ボタンを PDP に追加するには、次の手順に従ってください。

1. 購入ボックス モジュールを含む既存のサイト ビルダー ページを開きます。
1. 左のナビゲーション ウィンドウで、購入ボックスモジュールを選択します。
1. 右側のナビゲーション ペインで、**類似した説明を探すリンク** チェックボックスをオンにします。
1. **保存** を選択します。
1. **編集の完了** を選択してページをチェックインし、 **発行** を選択して公開します。 ページの発行後に、PDP には **類似した説明を探すリンク** ボタンが追加されます。

次の図は、サイト ビルダーの PDP 例上の **類似した説明を探すリンク** チェック ボックスと **類似した説明を探す** ボタンを示しています。

![サイト ビルダーの PDP 上で、[類似した説明を探すリンク] チェック ボックスと [類似した説明を探す] ボタンを有効化します](./media/ter_site_builder_buybox_button.png)

## <a name="additional-resources"></a>追加リソース

[製品推奨事項の概要](product-recommendations.md)

[Dynamics 365 Commerce 環境で Azure Data Lake Storage を有効化する](enable-adls-environment.md)

[製品推奨事項の有効化](enable-product-recommendations.md)

["同じような商品を探す" 推奨事項の有効化](shop-similar-looks.md)

[AI-ML 推奨事項結果の調整](modify-product-recommendation-results.md)

[収集された推奨事項の手動作成](create-editorial-recommendation-lists.md)

[製品推奨事項に関するよく寄せられる質問](faq-recommendations.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]