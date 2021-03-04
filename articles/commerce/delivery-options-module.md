---
title: 配送オプション モジュール
description: このトピックでは、配送オプション モジュールを取り上げ、 Microsoft Dynamics 365 Commerce での構成方法について説明します。
author: anupamar-ms
manager: annbe
ms.date: 08/05/2020
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
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.13
ms.openlocfilehash: f9e8df576efd1e58fde235828823f31e87ed58bf
ms.sourcegitcommit: 12d271bb26c7490e7525d9b4bbf125cdc39fef43
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/07/2020
ms.locfileid: "4413919"
---
# <a name="delivery-options-module"></a>配送オプション モジュール

[!include [banner](includes/banner.md)]

このトピックでは、配送オプション モジュールを取り上げ、 Microsoft Dynamics 365 Commerce での構成方法について説明します。

## <a name="overview"></a>概要

配送オプション モジュールを使用すると、顧客は、オンライン注文の配送や受取などの配送方法を選択できます。 配送モードを決定するには、配送先住所が必要です。 配送先住所が変更になると、配送オプションを再度取得する必要があります。 注文に店舗で受け取る品目のみが含まれる場合、このモジュールは自動的に非表示になります。

配送モードのコンフィギュレーションについては、[オンライン チャネル設定](channel-setup-online.md) と [配送モードの設定](https://docs.microsoft.com/dynamicsax-2012/appuser-itpro/set-up-modes-of-delivery) を参照してください。

各配送モードでは、関連付けられている料金を持つことができます。 オンライン ストアの諸費用を設定する方法の詳細については、[オムニ チャネルの高度な自動請求](omni-auto-charges.md) を参照してください。

Commerce バージョン 10.0.13 では、配送オプション モジュールが、**比例配分なしのヘッダー料金** と **明細行手数料での配送** 機能をサポートするように更新されました。 比例配分がオフになっている場合、電子商取引ワークフローでは、カート内の品目に対して配送の混合モードを許可しないことが予想されます (つまり、いくつかの品目は配送用に選択されていますが、他の品目は受取用に選択されています)。 **比例配分なしのヘッダー料金** 機能を使用するには、**チャネルで一貫した配送モード処理を有効にする** フラグを Commerce Headquarters でオンにする必要があります。 フラグがオンになっているとき、送料は Commerce Headquarters でのコンフィギュレーションに応じて、ヘッダー レベルまたは明細行レベルのいずれかで適用されます。

Fabrikam のテーマは、一部の品目が配送用に選択されていて、その他の品目が受取用に選択される、配送の混合モードをサポートします。 このモードでは、発送方法として選択されたすべての品目について、送料が比例配分になります。 配送の混在モードを機能させるには、最初に、**比例配分ありのヘッダー料金** 機能を Commerce Headquarters でコンフィギュレーションする必要があります。 このコンフィギュレーションの詳細については、[ヘッダー料金を販売明細行と一致するよう比例配分する](pro-rate-charges-matching-lines.md) を参照してください。

明細行品目に送料が適用される場合は、品目ごとにカート明細に表示されます。 この機能を使用するには、**明細行品目で送料を表示** プロパティをカート モジュールとチェックアウト モジュールの両方に対してオンにする必要があります。 詳細については、[カート モジュール](add-cart-module.md) と [チェックアウト モジュール](add-checkout-module.md) を参照してください。

次の図は、Fabrikam のチェックアウト ページにおける配送オプション モジュールの例を示しています。

![チェックアウトページにおける配送オプション モジュールの例](./media/ecommerce-deliveryoptions.PNG)

## <a name="delivery-options-module-properties"></a>配送オプション モジュール プロパティ

| プロパティ | 値 | 説明 |
|----------|--------|-------------|
| ヘッダー | ヘッダー テキストとヘッダー タグ (**H1**、**H2**、**H3**、**H4**、**H5**、または **H6**) | 配送オプションモジュールのオプション ヘッダー。 |
| カスタム CSS クラス名 | テキスト | 該当する場合、このモジュールをレンダリングするために使用される カスタム カスケード スタイル シート (CSS) クラス名。 |
| フィルター配送モードのオプション | **フィルター処理しない** または **非発送モード** | 配送オプション モジュールがすべての発送以外の配送モードを除外するかどうかを指定する値。 |

## <a name="add-a-delivery-options-module-to-a-checkout-page-and-set-the-required-properties"></a>チェックアウト ページに配送オプション モジュールを追加して必要なプロパティを設定する

配送オプション モジュールは、チェックアウト モジュールにのみ追加できます。 配送オプション モジュールをコンフィギュレーションしてチェックアウト ページに追加する方法の詳細については、[チェックアウト モジュール](add-checkout-module.md) を参照してください。

## <a name="additional-resources"></a>追加リソース

[カート モジュール](add-cart-module.md)

[チェックアウト モジュール](add-checkout-module.md)

[支払モジュール](payment-module.md)

[出荷先住所モジュール](ship-address-module.md)

[集荷情報モジュール](pickup-info-module.md)

[注文詳細のモジュール](order-confirmation-module.md)

[ギフト カード モジュール](add-giftcard.md)

[オンライン チャネル設定](channel-setup-online.md)

[オムニ チャネルの高度な自動請求](omni-auto-charges.md)

[ヘッダー料金を販売明細行と一致するよう比例配分する](pro-rate-charges-matching-lines.md)

[荷渡方法の設定](https://docs.microsoft.com/dynamicsax-2012/appuser-itpro/set-up-modes-of-delivery)


[!INCLUDE[footer-include](../includes/footer-banner.md)]