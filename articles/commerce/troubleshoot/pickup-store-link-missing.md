---
title: これを選択するのオプションがカートまたは製品の詳細ページに表示されません
description: この記事には、店舗内での集荷のオプションがカート ページまたは製品の詳細ページに表示されない場合に役立つトラブルシューティング ガイドが含まれます。
author: Reza-Assadi
ms.date: 03/11/2021
ms.topic: Troubleshooting
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: rassadi
ms.search.validFrom: 2021-01-31
ms.dyn365.ops.version: 10.0.18
ms.custom: ''
ms.assetid: ''
ms.search.industry: Retail
ms.openlocfilehash: 85d102d3442e19377912cb9562010778a0575db8
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/12/2022
ms.locfileid: "9284606"
---
# <a name="pick-this-up-option-doesnt-appear-on-cart-or-product-details-pages"></a>「これを選択する」のオプションがカートまたは製品の詳細ページに表示されません

[!include [banner](../../includes/banner.md)]

この記事には、店舗内での集荷のオプションがカート ページまたは製品の詳細ページに表示されない場合に役立つトラブルシューティング ガイドが含まれます。

## <a name="description"></a>説明

**これを選択する** ボタンがカートまたは製品の詳細ページに表示されません。

次の図は、**これを選択する** ボタンを含むページの例を示しています。

![これを選択するボタン。](media/pickup-button-missing.jpg)

## <a name="resolution"></a>解決策

### <a name="enable-the-bopis-extension-in-commerce-site-builder"></a>Commerce サイト ビルダーで BOPIS 拡張子を有効にする

Commerce サイト ビルダーの「オンラインで購入する、店舗で受け取る」(BOPIS) 拡張機能を有効にするには、次の手順に従います。

1. サイトを選択します。
1. **サイトの設定** を選択し、**拡張機能** を選択します。
1. **BOPIS を無効にする** オプションがオフになっていることを確認してください。

### <a name="configure-modes-of-delivery-in-commerce-headquarters"></a>Commerce 本社の出荷モードの構成

Commerce 本社の出荷モードの構成するには、次の手順に従います。

1. **調達 \> 設定 \> 配送モード** に順に移動します。
1. **顧客の集荷** の配送モードが作成されており、製品と住所が割り当てられている必要があります。
1. **Retail と Commerce \> 本社の設定 \> パラメーター** の順に移動します。
1. 左側のナビゲーションで、**顧客注文** を選択します。
1. **配送の集荷モード** が適切に構成されていることを確認します。

### <a name="configure-customer-orders-payments"></a>顧客注文支払の構成

Commerce 本社で顧客注文支払を構成するには、次の手順に従います。

1. **Retail と Commerce \> 本社の設定 \> パラメーター** の順に移動します。
1. 左側のナビゲーションで、**顧客注文** を選択します。
1. **支払** クイック タブで、**支払条件** および **支払方法** フィールドが正しく設定されていることを確認します。

## <a name="additional-resources"></a>追加リソース

[BOPIS の構成](../cpe-bopis.md)

[顧客注文に対して複数の受け取り配送モードを有効にする](../multiple-pickup-modes.md)

[オムニチャネル Commerce 注文支払](../dev-itpro/commerce-payments.md)

[店舗セレクター モジュール](../store-selector.md)
