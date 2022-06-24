---
title: 評価とレビューの構成
description: この記事では、Microsoft Dynamics 365 Commerce で顧客の評価とレビューを表示するように E コマース サイトを構成する方法について説明します。
author: gvrmohanreddy
ms.date: 02/17/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: gmohanv
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 56325eb0d6298f3b30316e104a4b3913ef860366
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/03/2022
ms.locfileid: "8862258"
---
# <a name="configure-ratings-and-reviews"></a>評価とレビューの構成

[!include [banner](includes/banner.md)]

この記事では、Microsoft Dynamics 365 Commerce で顧客の評価とレビューを表示するように E コマース サイトを構成する方法について説明します。

E コマース ウェブ サイトの評価およびレビューでは、それらの製品に対する他の顧客の意見を示すことによって、顧客が購入決定を行う前に製品について学ぶことができます。 E コマース Web サイトは、評価とレビューも製品に関する顧客フィードバックを収集するためのメカニズムです。 

## <a name="configure-a-site-to-show-ratings-and-reviews"></a>評価とレビューを表示するようサイトをコンフィギュレーションする

テナント ID、レビュー テキストの長さ、レビュー タイトルの長さなどの評価とレビューのコンフィギュレーション値は、サイト レベルでコンフィギュレーションされています。 

評価とレビューを表示するサイトをコンフィギュレーションするには、次の手順を実行します。 

1. **ホーム \> サイト** に移動します。
1. サイトの名前を選択します。 
1. **サイト 設定 \> 拡張** に移動します。 
1. **レビュー テキストの最大長** フィールドに、レビュー テキストに設定できる最大文字数を入力します (たとえば **1000**)。 
1. **レビュー タイトルの最大長** フィールドに、レビュー タイトルに設定できるの最大文字数を入力します (たとえば **55**)。 
1. **保存と公開** を選択します。 

次の図は、このコンフィグレーションが Dynamics 365 Commerce でどのように表示されるかを示しています。

![評価とレビューを表示するようサイトをコンフィギュレーションします。](media/rnr-eCommerce-site-appsettings.png)

## <a name="link-a-product-rating-to-the-reviews-section-of-a-pdp"></a>製品評価を PDP のレビュー セクションにリンクする

製品評価は、PDP 上部にある製品タイトルの下に表示されます。 製品評価は、同じ PDP の **レビュー** セクションにリンクされるようにコンフィギュレーションできます。 

製品評価を PDP の **レビュー** セクションにリンクするには、次の手順を実行します。

1. PDP テンプレートを開きます。 
1. **購入ボックス コンテナー モジュールの設定** に移動します。
1. **購入ボックス** の **製品評価** を選択し、**クリックして完全にレビュー モジュールにリンクする** チェック ボックスをオンにします。

次の図は、このコンフィグレーションが Dynamics 365 Commerce でどのように表示されるかを示しています。

![製品評価を PDP のレビュー セクションにリンクします。](media/rnr-eCommerce-buy-box-rating-summary.png)

## <a name="configure-the-link-for-the-privacy-and-policy-page"></a>プライバシーおよびポリシー ページへのリンクをコンフィギュレーションします。

プライバシーおよびポリシー ページへのリンクをコンフィギュレーションするには次の手順を実行します。

1. **ホーム \> サイト** に移動します。
1. サイトの名前を選択します。 
1. **サイト 設定 \> 拡張** に移動します。
1. **ルート** タブの **RNR プライバシーおよびポリシー** で **リンクの追加** を選択します。 リンクが既に入力されており、置き換えたい場合は、リンクを選択します。 
1. **リンクの追加** ダイアログ ボックスで、プライバシーおよびポリシー ページのリンクを選択し、**OK** を選択します。 
1. **保存と公開** を選択します。 

次の図は、このコンフィグレーションが Dynamics 365 Commerce でどのように表示されるかを示しています。

![プライバシーおよびポリシー ページへのリンクをコンフィギュレーションします。](media/rnr-eCommerce-rnr-privacy-policy-link.png)

## <a name="configure-ratings-and-reviews-modules-on-product-details-pages"></a>製品詳細ページに評価とレビュー モジュールをコンフィギュレーション

製品詳細ページの評価とレビュー モジュールのコンフィギュレーションについては、 [評価とレビュー モジュール](ratings-reviews-modules.md)を参照してください。

## <a name="additional-resources"></a>追加リソース

[評価とレビューの概要](ratings-reviews-overview.md)

[評価とレビューを使用するためのオプト イン](opt-in-ratings-reviews.md)

[評価とレビューの管理](manage-reviews.md)

[Dynamics 365 Retail の商品評価の同期](sync-product-ratings.md)

[モデレーターによる評価とレビューの手動公開を有効にする](manual-publish-rating-reviews.md)

[評価とレビューのインポートとエクスポート](import-export-reviews.md)

[サービス間認証の構成](service-to-service-auth.md)

[評価とレビューに関するよく寄せられる質問](ratings-reviews-faq.md)

[評価およびレビュー モジュール](ratings-reviews-modules.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
