---
title: 評価とレビューのコンフィギュレーション
description: このトピックでは、Microsoft Dynamics 365 Commerce で顧客の評価とレビューを表示するように E コマース サイトを構成する方法について説明します。
author: gvrmohanreddy
manager: annbe
ms.date: 02/17/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.search.scope: Operations, Retail, Core
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: gmohanv
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: edd2082b5d2cafcb955f8e3c7762bcba523ac479
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/13/2020
ms.locfileid: "4413655"
---
# <a name="configure-ratings-and-reviews"></a>評価とレビューのコンフィギュレーション

[!include [banner](includes/banner.md)]

このトピックでは、Microsoft Dynamics 365 Commerce で顧客の評価とレビューを表示するように E コマース サイトを構成する方法について説明します。

## <a name="overview"></a>概要

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

![評価とレビューを表示するようサイトをコンフィギュレーションする](media/rnr-eCommerce-site-appsettings.png)

## <a name="link-a-product-rating-to-the-reviews-section-of-a-pdp"></a>製品評価を PDP のレビュー セクションにリンクする

製品評価は、PDP 上部にある製品タイトルの下に表示されます。 製品評価は、同じ PDP の **レビュー** セクションにリンクされるようにコンフィギュレーションできます。 

製品評価を PDP の **レビュー** セクションにリンクするには、次の手順を実行します。

1. PDP テンプレートを開きます。 
1. **購入ボックス コンテナー モジュールの設定** に移動します。
1. **購入ボックス** の **製品評価** を選択し、**クリックして完全にレビュー モジュールにリンクする** チェック ボックスをオンにします。

次の図は、このコンフィグレーションが Dynamics 365 Commerce でどのように表示されるかを示しています。

![製品評価を PDP のレビュー セクションにリンクする](media/rnr-eCommerce-buy-box-rating-summary.png)

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

[製品詳細ページに評価とレビュー モジュールをコンフィギュレーション](ratings-reviews-modules.md)

[Dynamics 365 Retail の商品評価の同期](sync-product-ratings.md)
