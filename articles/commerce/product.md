---
title: POS で製品推奨事項を追加する
description: この記事では、POS (販売時点管理) デバイスでの製品推奨事項の使用について説明します。
author: bebeale
ms.date: 09/08/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: RetailParameters
audience: Application User
ms.reviewer: josaw
ms.custom: 259664
ms.assetid: 5dd8db08-cd96-4f7e-9e65-b05ca815d580
ms.search.region: global
ms.search.industry: Retail
ms.author: asharchw
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 170e2bf18aefc79a796620818c7100ff8e6e689a
ms.sourcegitcommit: f88273627ba105ede27f28fe67ccec2d7f78261c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/09/2022
ms.locfileid: "9460059"
---
# <a name="add-product-recommendations-on-pos"></a>POS で製品推奨事項を追加する

[!include [banner](includes/banner.md)]

製品の推奨事項は、本質的に、すべてのコマース スペースにまたがる変形力のあるビジネス アプリケーションであり、リッチで魅力的な、カスタマイズされた製品検索エクスペリエンスを作成します。 POS にこの機能を実装するには、[POS デバイスに推奨事項を追加する方法](add-recommendations-control-pos-screen.md)の手順に従ってください。 

製品推奨機能の詳細については、[製品推奨事項の概要](../commerce/product-recommendations.md)を参照してください。 

## <a name="scenarios"></a>シナリオ

製品推奨事項は、以下の POS シナリオで使用可能です。 これらは、Cloud POS または Modern POS (MPOS) で利用できます。

1. **製品の詳細** ページ:

    - 店舗スタッフが、異なるチャネル間で以前のトランザクションを調べるときに **製品の詳細** ページを参照する場合、推奨事項サービスは、一緒に購入される可能性が高い追加アイテムを提案します。 サービスのアドオンに応じて、以前に購買履歴を持つユーザーに対してカスタマイズされたすすめ候補と、製品に対して **同様の外観を持つものを買う** と **同様の説明のものを買う** の推奨事項を表示できます。

    [![製品詳細ページの推奨事項。](./media/proddetails.png)](./media/proddetails.png)

2. **トランザクション** ページ:

    - 推奨エンジンは、一緒に頻繁に購入されるバスケット内の品目の一覧全体に基づいて、品目を提案します。

    > [!NOTE]
    > **トランザクション** ページに推奨事項を表示するには、小売業者は Dynamics 365 Commerce の画面レイアウトを更新する必要があります。 **推奨事項** コントロールは、**トランザクション** ページにドロップする必要があります。

    [![トランザクション ページの推奨事項。](./media/transactionscreenmultipleproductslargemessengersbag-5.jpg)](./media/transactionscreenmultipleproductslargemessengersbag-5.jpg)

## <a name="configure-commerce-to-enable-pos-recommendations"></a>コマースをコンフィギュレーションして POS 推奨事項を有効化する 

製品の推奨事項を設定するには、[製品の推奨事項を有効にする](../commerce/enable-product-recommendations.md) の手順に従って、Commerce 製品の推奨事項のプロビジョニング プロセスが完了している必要があります。 デフォルトでは、準備手順が完了してデータが正常にクック処理された後、**製品の詳細** ページと **顧客の詳細** ページの両方に推奨事項が表示されます。 

## <a name="add-recommendations-to-the-transaction-screen"></a>トランザクション画面への推奨事項の追加

1. トランザクション画面に推奨事項を追加するには、[トランザクション画面に推奨事項を追加する](add-recommendations-control-pos-screen.md) の手順に従います。
1. POS 画面レイアウト デザイナーで行われた変更を反映するには、Commerce Headquarters でチャンネル構成ジョブ **1070** を実行します。

> [!NOTE] 
> RecoMock コンマ区切り値 (CSV) ファイルを使用して POS の推奨事項を有効にする場合は、レイアウト マネージャを構成する前に、CSV ファイルを Microsoft Dynamics Lifecycle Services (LCS) 資産ライブラリに配置する必要があります。 RecoMock CSV ファイルを使用する場合は、推奨事項を有効にする必要があります。 CSV ファイルは、デモ専用としてのみ使用できます。 アドオンの在庫管理単位 (SKU) を購入することなく、デモ目的で推奨事項のリストの外観を変更する顧客やソリューションの形式を変更する場合に推奨されます。

## <a name="additional-resources"></a>追加リソース

[製品推奨事項の概要](product-recommendations.md)

[Dynamics 365 Commerce 環境で Azure Data Lake Storage を有効化する](enable-adls-environment.md)

[製品推奨事項の有効化](enable-product-recommendations.md)

[カスタマイズされた推奨事項の有効化](personalized-recommendations.md)

[カスタマイズされた推奨事項のオプト アウト](personalization-gdpr.md)

["類似したルックを買う" 推奨を有効にする](shop-similar-looks.md)

[トランザクション画面への推奨事項の追加](add-recommendations-control-pos-screen.md)

[AI-ML 推奨事項結果の調整](modify-product-recommendation-results.md)

[収集された推奨事項の手動作成](create-editorial-recommendation-lists.md)

[推奨事項とデモ データの作成](product-recommendations-demo-data.md)

[製品推奨事項に関するよく寄せられる質問](faq-recommendations.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
