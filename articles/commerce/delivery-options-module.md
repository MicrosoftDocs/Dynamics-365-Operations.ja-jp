---
title: 配送オプション モジュール
description: この記事では、配送オプション モジュールを取り上げ、Microsoft Dynamics 365 Commerce での構成方法について説明します。
author: anupamar-ms
ms.date: 02/24/2022
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
ms.openlocfilehash: c3fb60c61878fc790a44178fabc8a7be5809806b
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/12/2022
ms.locfileid: "9268450"
---
# <a name="delivery-options-module"></a>配送オプション モジュール

[!include [banner](includes/banner.md)]

この記事では、配送オプション モジュールを取り上げ、Microsoft Dynamics 365 Commerce での構成方法について説明します。

配送オプション モジュールを使用すると、顧客は、オンライン注文の配送や受取などの配送方法を選択できます。 配送モードを決定するには、配送先住所が必要です。 配送先住所が変更になると、配送オプションを再度取得する必要があります。 注文に店舗で受け取る品目のみが含まれる場合、このモジュールは自動的に非表示になります。

配送モードのコンフィギュレーションについては、[オンライン チャネル設定](channel-setup-online.md) と [配送モードの設定](/dynamicsax-2012/appuser-itpro/set-up-modes-of-delivery) を参照してください。

各配送モードでは、関連付けられている料金を持つことができます。 オンライン ストアの諸費用を設定する方法の詳細については、[オムニ チャネルの高度な自動請求](omni-auto-charges.md) を参照してください。

Commerce バージョン 10.0.13 では、配送オプション モジュールが、**比例配分なしのヘッダー料金** と **明細行手数料での配送** 機能をサポートするように更新されました。 比例配分がオフになっている場合、電子商取引ワークフローでは、カート内の品目に対して配送の混合モードを許可しないことが予想されます (つまり、いくつかの品目は配送用に選択されていますが、他の品目は受取用に選択されています)。 **比例配分なしのヘッダー料金** 機能を使用するには、**チャネルで一貫した配送モード処理を有効にする** フラグが Commerce 本社でオンになっている必要があります。 機能フラグがオンになっているとき、送料は Commerce 本社でのコンフィギュレーションに応じて、ヘッダー レベルまたは明細行レベルのいずれかで適用されます。

Fabrikam のテーマは、一部の品目が配送用に選択されていて、その他の品目が受取用に選択される、配送の混合モードをサポートします。 このモードでは、発送方法として選択されたすべての品目について、送料が比例配分になります。 配送の混在モードを機能させるには、最初に、**比例配分ありのヘッダー料金** 機能を Commerce Headquarters でコンフィギュレーションする必要があります。 このコンフィギュレーションの詳細については、[ヘッダー料金を販売明細行と一致するよう比例配分する](pro-rate-charges-matching-lines.md) を参照してください。

明細行品目に送料が適用される場合は、品目ごとにカート明細に表示されます。 この機能を使用するには、**明細行品目で送料を表示** プロパティをカート モジュールとチェックアウト モジュールの両方に対してオンにする必要があります。 詳細については、[カート モジュール](add-cart-module.md) と [チェックアウト モジュール](add-checkout-module.md) を参照してください。

次の図は、Fabrikam のチェックアウト ページにおける配送オプション モジュールの例を示しています。

![チェックアウトページにおける配送オプション モジュールの例。](./media/ecommerce-deliveryoptions.PNG)

## <a name="delivery-options-module-properties"></a>配送オプション モジュール プロパティ

| プロパティ | 値 | 説明 |
|----------|--------|-------------|
| ヘッダー | ヘッダー テキストとヘッダー タグ (**H1**、**H2**、**H3**、**H4**、**H5**、または **H6**) | 配送オプションモジュールのオプション ヘッダー。 |
| カスタム CSS クラス名 | テキスト | 該当する場合、このモジュールをレンダリングするために使用される カスタム カスケード スタイル シート (CSS) クラス名。 |
| フィルター配送モードのオプション | **フィルター処理しない** または **非発送モード** | 配送オプション モジュールがすべての発送以外の配送モードを除外するかどうかを指定する値。 |
| 配送オプションの自動選択 | **フィルター処理しない**、**配送オプションを自動選択して集計を表示する**、または **配送オプションを自動選択して集計を表示しない** | このプロパティは、ユーザーが選択しなくても、最初に使用可能な配送オプションを自動的にチェック アウトに適用します。 このオプションは、使用可能な配送オプションが 1 つしかない場合にのみ使用します。 このプロパティは、Commerce バージョン 10.0.19 リリース以降でサポートされています。 |

## <a name="add-a-delivery-options-module-to-a-checkout-page-and-set-the-required-properties"></a>チェックアウト ページに配送オプション モジュールを追加して必要なプロパティを設定する

配送オプション モジュールは、チェックアウト モジュールにのみ追加できます。 配送オプション モジュールをコンフィギュレーションしてチェックアウト ページに追加する方法の詳細については、[チェックアウト モジュール](add-checkout-module.md) を参照してください。

> [!NOTE]
> 配送処理に一貫性がなかったり、eコマース チャネルで比例しないヘッダー レベルの料金が表示されない場合があります。 これらの問題を解決するガイダンスについては、[e コマース チャネルにおける一貫した配信モードの取り扱いを可能にする](consistent-delivery-mode-handling.md) を参照してください。

## <a name="additional-resources"></a>追加リソース

[買い物カゴ モジュール](add-cart-module.md)

[チェックアウト モジュール](add-checkout-module.md)

[支払モジュール](payment-module.md)

[出荷先住所モジュール](ship-address-module.md)

[集荷情報モジュール](pickup-info-module.md)

[注文詳細のモジュール](order-confirmation-module.md)

[ギフト カード モジュール](add-giftcard.md)

[オンライン チャネル設定](channel-setup-online.md)

[オムニ チャネルの高度な自動請求](omni-auto-charges.md)

[ヘッダー料金を販売明細行と一致するよう比例配分する](pro-rate-charges-matching-lines.md)

[荷渡方法の設定](/dynamicsax-2012/appuser-itpro/set-up-modes-of-delivery)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
