---
title: "\"\"同じような商品を探す\"\" 推奨事項の有効化"
description: この記事では、Microsoft Dynamics 365 Commerce で ""同じような商品を探す"" 製品推奨事項を有効にする方法について説明します。
author: bebeale
ms.date: 08/06/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgriffin
ms.search.region: global
ms.author: bebeale
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.13
ms.custom: ''
ms.assetid: ''
ms.search.industry: Retail, eCommerce
ms.search.form: ''
ms.openlocfilehash: 26eb436d889ac81cde730daca9b44d1deeda6c74
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/12/2022
ms.locfileid: "9282053"
---
# <a name="enable-shop-similar-looks-recommendations"></a>"同じような商品を探す" 推奨事項の有効化

[!include [banner](includes/banner.md)]

この記事では、Microsoft Dynamics 365 Commerce で "同じような商品を探す" 製品推奨製品を有効にする方法について説明します。

Dynamics 365 Commerce の "類似したスタイルを探す" 推奨機能は、人工知能と機械学習 (AI-ML) の機能を使用して、顧客に対して視覚的に類似した製品の推奨を提供します。 Commerce におけるすべての小売チャンネルについて、"類似したスタイルを探す" 推奨を提供することによって、小売業者は顧客が欲しいものを簡単に見つけられるようにすることで、顧客満足度を高めることができます。

"類似したスタイルを探す" 推奨の機能は、シード製品バリアントの製品画像を使用して、小売業者の製品カタログで視覚的に類似した製品を見つけて推奨します。 

"同様のスタイルを探す" 推奨事項は、販売時点管理 (POS) と電子商取引の両方の経験で使用可能です。

### <a name="example-scenarios"></a>シナリオ例

- 顧客はブラック ストライプのセーターを閲覧し、類似した赤色のセーターの推奨を受け取ります。 顧客は、最初に表示された製品の代わりに推奨された製品を選択し、類似した赤色の製品の推奨を受け取ります。 
- "類似のスタイルを探す" 推奨事項を使用する顧客は、顧客が購入しようと思っている指輪とおそろいのイヤリングを見つけます。

## <a name="enable-shop-similar-looks-recommendations-in-commerce-headquarters"></a>Commerce 本社の "類似したスタイルを探す" 推奨を有効にする

製品の推奨は、ストレージを Azure Data Lake Gen2 に移行した Commerce 顧客に対してのみサポートしています。

### <a name="prerequisites"></a>必要条件

小売業者が顧客に対して "類似したスタイルを探す" 推奨を表示するには、次の 2 つの手順を実行する必要があります。

- Commerce 本社での [製品推奨を有効にします](enable-product-recommendations.md)。
- メディア サーバーが HTTPS 呼び出しをサポートしていることを確認します。

製品画像にアクセスするための推奨エンジンでは、小売業者は製品の URL を生成する必要があります。 Commerce 本社で製品 URL を生成するには、次の手順を実行します。

1. **製品画像** に移動します。
1. アクション ウィンドウで、**メディア テンプレートの定義** を選択します。
1. **メディア テンプレートの定義** プロパティ ウィンドウで、**メディア URL** から **URL の生成** を選択します。

> [!NOTE]
> "類似のスタイルを探す" 推奨機能を有効にすると、製品推奨リストの生成プロセスが開始されます。 これらのリストを利用可能にし、オンラインおよび POS で表示するまでに、少なくとも 1 日必要な場合があります。

Commerce本社で"同様のスタイルを探す" 推奨機能を有効にするには、次の手順を実行します。

1. **機能管理** に移動します。
1. 使用可能な機能の一覧で、**同様のスタイルを探す** を選択します。
1. 右ウィンドウで、**有効化** を選択してサービスを有効にします。

次の図は、Commerce本社の **機能管理** ページの **類似したスタイルを探す** 機能を示しています。

![次の図は、Commerce 本社の機能管理ページの類似したスタイルを探す機能を示しています。](./media/enableshopsimilarlooks.png)

上記のタスクが完了すると、POS ターミナルは、**類似した製品を探す** パネルで自動的に拡張されます。 **詳細を表示** を選択すると、POS 端末のユーザーは、さらに絞り込むことができる、専用の "類似したスタイルを探す" ページに移動できます。

> [!NOTE]
> "類似のスタイルを探す" 推奨機能をオフにすると、他の製品の推奨は影響を受けません。 製品推奨の詳細については、[製品推奨の概要](product-recommendations.md) を参照してください。

## <a name="add-a-shop-similar-looks-button-to-product-details-pages-by-using-commerce-site-builder"></a>Commerce サイト ビルダーを使用することで、製品の詳細ページに [類似したスタイルを探す] ボタンを追加します。

Commerce 本社の [同様のスタイルを探す] 推奨機能を有効にすると、Commerce サイトのオプションによって、小売業者は **類似したスタイルを探す** ボタンを追加して、製品詳細ページ (PDP) 上の購入ボックスに追加することができます。 このボタンを選択した顧客は、視覚的に類似した製品を返す、専用の "類似したスタイルを探す" ページに移動します。 そこで、顧客はセレクターを使用して、製品をさらに詳細にフィルタ処理することができます。

Commerce サイト ビルダーを使用することで、**類似したスタイルを探す** ボタンを PDP に追加するには。

1. 購入ボックス モジュールを含む既存のサイト ビルダー ページを開きます。
1. 左のナビゲーション ウィンドウで、購入ボックスモジュールを選択します。
1. 右側のナビゲーション ウィンドウで、**類似したスタイルを探すリンクを有効にする** チェックボックスをオンにします。
1. **保存** を選択し、 **編集の完了** を選択してページにチェックインし、**発行** を選択して公開します。 ページの発行後に、PDP には **同様のスタイルを探す** ボタンが追加されます。

次の図は、サイト ビルダーの PDP 例上の **類似したスタイルを探すリンクを有効にする** チェック ボックスと **類似したスタイルを探す** ボタンを示しています。

![サイト ビルダーの PDP 上で、類似したスタイルを探すリンク チェック ボックスと類似したスタイルを探すボタンを有効化します。](./media/SSLecomtooling.png)

## <a name="additional-resources"></a>追加リソース

[製品推奨事項の概要](product-recommendations.md)

[Dynamics 365 Commerce 環境で Azure Data Lake Storage を有効化する](enable-adls-environment.md)

[製品推奨事項の有効化](enable-product-recommendations.md)

[カスタマイズされた推奨事項のオプト アウト](personalization-gdpr.md)

[POS での製品推奨事項の追加](product.md)

[トランザクション画面への推奨設定の追加](add-recommendations-control-pos-screen.md)

[AI-ML 推奨事項結果の調整](modify-product-recommendation-results.md)

[収集された推奨事項の手動作成](create-editorial-recommendation-lists.md)

[推奨事項とデモ データの作成](product-recommendations-demo-data.md)

[製品推奨事項に関するよく寄せられる質問](faq-recommendations.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
