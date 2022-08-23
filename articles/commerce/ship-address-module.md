---
title: 出荷先住所モジュール
description: この記事では、出荷先住所モジュールを取り上げ、Microsoft Dynamics 365 Commerce での構成方法について説明します。
author: anupamar-ms
ms.date: 02/11/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.13
ms.custom: ''
ms.assetid: ''
ms.openlocfilehash: 48e6909b4dac9722830a83ec3a63a58876768d7e
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/12/2022
ms.locfileid: "9275008"
---
# <a name="shipping-address-module"></a>出荷先住所モジュール

[!include [banner](includes/banner.md)]

この記事では、出荷先住所モジュールを取り上げ、Microsoft Dynamics 365 Commerce で構成する方法について説明します。

出荷先住所モジュールにより、顧客がチェックアウト フロー中に注文の出荷先住所を追加または選択できます。 顧客がサインインしている場合、その顧客用に以前に保存されたすべての住所が表示され、そこから選ぶことができます。 顧客は、新しい住所を追加することもできます。 出荷先住所モジュールは、出荷を必要とする注文のすべての品目に対して使用されます。

Commerce 本社では、国や地域ごとに送付先住所の形式を定義することができます。その後、送付先住所モジュールは、国/地域に固有のルールを適用します。

顧客がチェックアウト フロー中に送付先住所を入力する場合、オプションでその住所を基本住所として保存することができます。 このオプションは、顧客がログインしている場合にのみ表示されます。

送付先住所モジュールでは住所検証はおこないませんが、この機能はカスタマイズを通じて実装できます。

以下の図は、精算ページのす新規送付先住所モジュールの例を示しています。

![精算ページの出荷先住所モジュールの例。](./media/ecommerce-shippingaddress.PNG)

## <a name="module-properties"></a>モジュール プロパティ

| プロパティ名 | 値 | 説明 |
|---------------|--------|-------------|
| ヘッダー | ヘッダー テキストとヘッダー タグ (**H1**、**H2**、**H3**、**H4**、**H5**、または **H6**) | 出荷先住所モジュールのオプション ヘッダー。 |
| 住所タイプを表示する | **True** または **False** | このオプションのプロパティが **True** に設定されている場合は、**自宅** や **勤務先** などの住所タイプが表示されます。 住所タイプが指定されていない場合、住所は **タイプ**=**その他** として自動的に保存され ます。 |
| 自動提案の有効化| **True** または **False** | このオプションのプロパティが **True** に設定されている場合は、住所の自動提案が提供されます。 これらの提案は、Bing Maps を利用しています。 サイトに Bing Maps を統合する設定方法の詳細については、[店舗のセレクター モジュール](store-selector.md) を参照してください。 この機能は、Commerce バージョン 10.0.15 リリース以降で使用できます。|
|自動提案のオプション| 数| 住所の自動提案が有効になっている場合は、提供する必要のある提案の最大数など、追加のオプションを指定できます。|

## <a name="add-a-shipping-address-module-to-a-checkout-page-and-set-the-required-properties"></a>精算ページに出荷先住所モジュールを追加して必要なプロパティを設定する

出荷先住所モジュールは、精算モジュールにのみ追加できます。 出荷先住所モジュールをコンフィギュレーションして精算ページに追加する方法の詳細については、[精算モジュール](add-checkout-module.md) を参照してください。

## <a name="additional-resources"></a>追加リソース

[買い物カゴ モジュール](add-cart-module.md)

[カート アイコン モジュール](cart-icon-module.md)

[チェックアウト モジュール](add-checkout-module.md)

[支払モジュール](payment-module.md)

[配送オプション モジュール](delivery-options-module.md)

[集荷情報モジュール](pickup-info-module.md)

[注文詳細モジュール](order-confirmation-module.md)

[ギフト カード モジュール](add-giftcard.md)

[店舗セレクター モジュール](store-selector.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
