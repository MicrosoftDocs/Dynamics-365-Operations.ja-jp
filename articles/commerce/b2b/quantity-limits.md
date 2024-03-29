---
title: B2B eコマース サイトの製品数量制限の設定
description: この記事では、企業間 (B2B) の eコマース サイトに対して製品の数量制限を設定する方法について説明します。
author: josaw1
ms.date: 01/20/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: josaw
ms.search.validFrom: 2021-01-31
ms.dyn365.ops.version: 10.0.14
ms.search.industry: retail
ms.search.form: RetailOperations
ms.openlocfilehash: 76a7ad2c3095d1402ff214dbfee26b344b492681
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/12/2022
ms.locfileid: "9275681"
---
# <a name="set-product-quantity-limits-for-b2b-e-commerce-sites"></a>B2B eコマース サイトの製品数量制限の設定

[!include [banner](../../includes/banner.md)]

この記事では、企業間 (B2B) の eコマース サイトに対して製品の数量制限を設定する方法について説明します。

ほとんどの製品には、グループ化を定義する単位を持っています。 このグループは、製品の販売方法に影響します。 商品によっては、数量のグループが追加されている場合があります。 このグループにより、製品を個別の単位として販売できるか、複数の単位として販売できるか、また、従う必要がある最小または最大の注文数量制限があるかどうかを決定します。

数量制限機能を使用することで、Microsoft Dynamics 365 Commerce で設定されている最小、最大、複数、標準の数量 (既定の注文設定または Commerce サイト ビルダーのサイト設定) が、eコマースで発注された顧客の注文に適用されます。 製品数量の制限は、販売時点管理 (POS) およびコール センターでは現在サポートされていません。

多くの小売業者は、様々な製品や条件を満たすための顧客注文 (特別注文と呼ばれる場合もあります) のオプションを提供しています。 以下に一般的なシナリオを挙げます。

- 顧客は、特定のバリエーションの製品をいくつかの倍数で販売したいと考えています。
- 顧客は、その製品を購入した店舗または場所とは異なる店舗または場所から製品の集荷を希望しています。 しかし、店舗の梱包基準は、オンライン販売流通の梱包基準とは異なります。
- 顧客は、購入できる商品の数量に上限がある限定商品を購入したいと考えています。

## <a name="turn-on-the-default-order-settings-feature-in-commerce-headquarters"></a>Commerce 本部の既定の注文設定機能をオンにする

商品の数量制限を設定する前に、Commerce 本部で既定の注文設定機能をオンにしておく必要があります。

既定の注文設定機能を有効にするには、以下の手順に従います。

1. **システム管理者 \> ワークスペース \> フィーチャー管理** の順に移動します。
1. **顧客注文でサイトと既定の注文設定をサポートする** 機能を探して選択します。
1. 右ウィンドウの下で、**今すぐ有効化** を選択します。 

## <a name="define-quantity-settings"></a>数量設定の定義 

**既定の注文設定** ページで、数量の設定を定義できます。

数量設定を定義するには、次の手順に従います。 

1. 製品 **小売とコマース \> 製品とカテゴリー \> カテゴリー別に製品を販売する** に移動します。
1. リリース済製品を選択します。
1. アクション ペインで、**在庫の管理** タブの **注文設定** グループで、**既定の注文設定** を選択します。 
1. **既定の注文設定** ページの **販売注文** クイック タブの **販売数量**  セクションで、製品の販売数量を設定します。

    - **複数** - 製品を複数の数量で購入できます。
    - **最小注文数量** - 購入する必要がある製品の最小数です。
    - **最大注文数量** - 購入可能な製品の最大数量です。
    - **標準注文数量** - 商品選択時に自動的に入力される既定の数量です。

## <a name="turn-on-the-b2b-order-quantity-limits-feature-in-commerce-site-builder"></a>Commerce サイトビルダーの B2B 注文数量制限機能をオンにする

Commerce サイトビルダーの B2B 注文数量制限機能を有効にするには、以下の手順に従います。

1. **サイト 設定 \> 拡張機能** に移動します
1. **注文数量制限の有効化** で、ドロップダウン メニューの **B2B 顧客に対して有効化** を選択します。 

> [!NOTE] 
> 更新されたサイトビルダーの設定は、app.settings.json ファイルが更新された後にのみ有効になります。 詳細については、[SDK およびモジュール ライブラリの更新プログラム](../e-commerce-extensibility/sdk-updates.md#update-the-appsettingsjson-file)を参照してください。

## <a name="additional-resources"></a>追加リソース

[B2B eコマース サイトの設定](set-up-b2b-site.md)

[顧客階層を使用した B2B ビジネス パートナーの管理](partners-customer-hierarchies.md)

[B2B eコマース サイトでのビジネス パートナー ユーザーの管理](manage-b2b-users.md)

[B2B eコマース サイト用の顧客アカウントの支払方法の構成](payment-method.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
