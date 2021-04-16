---
title: ギフト カード モジュール
description: このトピックでは、ギフト カード モジュールと、Microsoft Dynamics 365 Commerce のサイト ページにそれを追加する方法について説明します。
author: anupamar-ms
ms.date: 09/15/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: a4e4e06ab7032d68fcd36a8e80bc714ebaaac821
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/31/2021
ms.locfileid: "5797674"
---
# <a name="gift-card-module"></a>ギフト カード モジュール

[!include [banner](includes/banner.md)]

このトピックでは、ギフト カード モジュールと、Microsoft Dynamics 365 Commerce のサイト ページにそれを追加する方法について説明します。

ギフト カード モジュールは、精算モジュールで使用することができ、電子商取引で使用される一般的な支払い方法であるギフトカードを受け付けることができます。 ギフト カード モジュールは Dynamics 365、SVS、Givex ギフト カードをサポートしています。 SVS と Givex のギフト カードは、Adyen の支払プロバイダーで経由で引き換えることができます。 SVS や Givex などの外部ギフト カードのサポートの詳細については、[外部ギフト カードのサポート](./dev-itpro/gift-card.md) を参照してください。

> [!NOTE]
> 精算フロー中の SVS および Givex ギフトカードの引き換えは、Dynamics 365 Commerce のリリース バージョン 10.0.11 で使用可能です。 

ギフト カード モジュールは2つ使用できます。

- **ギフト カード** - このモジュールは、精算ページで使用でき、支払/入金としてギフトカードを使用できます。 
- **ギフト カードの残高** - このモジュールは、ギフトカードの残高を確認するために任意のページで使用できます。 このモジュールは、コマースのリリース 10.0.14 およびこれ以降でのみ利用できます。

> [!NOTE]
> ギフトカード残高チェック モジュールのサポートは、Dynamics 365 Commerce の営々ース バージョン 10.0.14 で使用可能です。

以下の図は、精算ページにおけるギフト カード モジュールの例を示しています。

![ギフト カード モジュールの例](./media/ecommerce-giftcard.PNG)

## <a name="module-properties"></a>モジュール プロパティ

- **追加フィールドの表示** - このプロパティでは、常に既定で表示されるギフト カード番号に加えて、ギフト カードを表示するフィールドを定義します。 たとえば、一部のギフト カードでは、個人識別番号 (PIN) の表示をサポートしており、他ののギフト カードでは、PIN と有効期限の表示をサポートしています。 または、このプロパティを "なし" に設定して、ギフト カード番号のみを表示し、追加フィールドは表示しないようにすることもできます。

サポートされている値:
-   暗証番号 (PIN)
-   有効期限
-   PIN と 有効期限 
-   None

## <a name="site-settings-for-gift-card-modules"></a>ギフト カード モジュールのサイト設定

コマース サイト ビルダーの **サイト設定 \> 拡張子** には、**サポートされているギフト カード タイプ** と呼ばれるギフト カード モジュール設定があります。 この設定は 3 つの値をサポートします:
- **Dynamics 365 ギフト カード** - この設定が適用されている場合、ギフト カード モジュールは Dynamics 365 ギフト カードの償還しかできなくなります。 この設定は、E コマース サイトのサインイン ユーザーに対してのみサポートされます。
- **SVS と Givex のギフト カード** - この設定が適用されている場合、ギフト カード モジュールは Givex や SVS ギフト カードの償還しかできなくなります。 この設定は、E コマース サイトのサインイン ユーザーと匿名ユーザーに対してサポートされます。
- **Dynamics 365、SVS、Givex のギフト カード** - この設定が適用されている場合、ギフト カード モジュールは Dynamics 365、Givex、SVS ギフト カードを償還できます。 この設定は、E コマース サイトのサインイン ユーザーに対してのみサポートされます。

> [!IMPORTANT]
> これらの設定は、Dynamics 365 Commerce のリリース バージョン 10.0.11 で使用可能であり 、SVS や Givex のギフトカードに対応する必要がある場合にのみ必要となります。 古いバージョンの Dynamics 365 Commerce を更新する場合は、appsettings.json ファイルを手動で更新する必要があります。 appsettings.json ファイルを更新する手順については、[SDK およびモジュール ライブラリの更新](e-commerce-extensibility/sdk-updates.md#update-the-appsettingsjson-file)を参照してください 。 

## <a name="add-a-gift-card-module-to-a-page"></a>ギフト カード モジュールをページに追加する

ギフト カード モジュールをチェックアウト ページに追加し、必要なプロパティを設定する方法については、[チェックアウト モジュール](add-checkout-module.md) を参照してください。

## <a name="additional-resources"></a>追加リソース

[買い物カゴ モジュール](add-cart-module.md)

[買い物カゴ アイコン モジュール](cart-icon-module.md)

[チェックアウト モジュール](add-checkout-module.md)

[支払モジュール](payment-module.md)

[出荷先住所モジュール](ship-address-module.md)

[配送オプション モジュール](delivery-options-module.md)

[集荷情報モジュール](pickup-info-module.md)

[注文詳細のモジュール](order-confirmation-module.md)

[外部ギフト カードのサポート](./dev-itpro/gift-card.md)

[SDK およびモジュール ライブラリの更新](e-commerce-extensibility/sdk-updates.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]