---
title: 店舗セレクター モジュール
description: このトピックでは、店舗セレクター モジュールと、Microsoft Dynamics 365 Commerce のサイト ページにそれを追加する方法について説明します。
author: anupamar-ms
manager: annbe
ms.date: 03/19/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2020-02-10
ms.dyn365.ops.version: ''
ms.openlocfilehash: 8efc2345ded52bfaee2d400815795906f326f4fd
ms.sourcegitcommit: de5af1912201dd70aa85fdcad0b184c42405802e
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/21/2020
ms.locfileid: "3157343"
---
# <a name="store-selector-module"></a>店舗セレクター モジュール

[!include [banner](includes/banner.md)]

このトピックでは、店舗セレクター モジュールと、Microsoft Dynamics 365 Commerce のサイト ページにそれを追加する方法について説明します。

## <a name="overview"></a>概要

店舗セレクター モジュールは、"オンラインで購入し、店舗でピックアップ" (BOPIS) 顧客シナリオに使用されます。 製品のピックアップが可能な店舗の一覧と、各店舗の営業時間と製品在庫が表示されます。

店舗セレクター モジュールでは、店舗を検索するために、製品のコンテキストと検索場所が必要があります。 検索場所が存在しない場合は、顧客が同意をした顧客のブラウザーの場所が規定で使用されます。 このモジュールには入力ボックスがあり、顧客が場所 (郵便番号、または市町村と都道府県) を入力して、近くにある店舗を検索できます。

ストア セレクター モジュールは、Bing Maps 位置情報アプリケーション プログラミング インターフェイス (API) と統合され、場所を緯度と経度に変換します。 Bing Maps API キーは必須で、Dynamics 365 Commerce の Commerce の共有パラメータ ページに追加する必要があります。

店舗セレクター モジュールは、製品の詳細ページ (PDP) の購入ボックス モジュールに追加して、製品がピックアップできる店舗を表示できます。 また、カート モジュールに追加することもできます。 カート モジュールに追加されると、店舗セレクター モジュールに各カート品目に対するピックアップ オプションが表示されます。 さらに、カスタムコードを使用して、拡張機能とカスタマイズによって、このモジュールを他のページまたはモジュールに追加することもできます。

BOPIS シナリオが機能するためには、"顧客ピックアップ" デリバリー モードを使用して製品をコンフィギュレーションする必要があります。 それ以外の場合、このモジュールは個々のページでは表示されません。 デリバリー モードをコンフィギュレーションする方法の詳細については、[デリバリーの設定モード](https://docs.microsoft.com/dynamicsax-2012/appuser-itpro/set-up-modes-of-delivery) を参照してください。

次の図は、PDP で使用される店舗セレクター モジュールの例を示しています。

![店舗セレクター モジュールの例](./media/BOPIS.PNG)

## <a name="store-selector-module-usage-in-e-commerce"></a>E-コマースの店舗セレクター モジュールの使用方法

- 店舗セレクター モジュールを製品の詳細ページ (PDP) で使用し、製品がピックアップできる近隣の店舗を探すことができます。
- 店舗セレクター モジュールをカート ページで使用し、ピックアップが使用できるカートの製品がある店舗を探すことができます。

## <a name="store-selector-module-properties"></a>店舗セレクター モジュールのプロパティ

| プロパティ名             | 先頭値                 | 説明 |
|---------------------------|-----------------------|-------------|
| 検索半径 | 番号 | 店舗の検索半径をマイル単位で定義します。 値が指定されていない場合は、既定の検索半径 (50マイル) が使用されます。|
|サービス条件 | URL    |  Bing Maps サービスに必要なサービス URL の条件。 |

## <a name="add-a-store-selector-module-to-a-page"></a>店舗セレクター モジュールをページに追加する

店舗セレクター モジュールには製品のコンテキストが必要であるため、購入ボックスとカート モジュール内でのみ使用できます。 ストア セレクター モジュールは、これらのモジュールの外では機能しません。

- 購入ボックス モジュールに店舗セレクター モジュールを追加する方法の詳細については、[購入ボックス モジュール](add-buy-box.md) を参照してください。 
- カート モジュールに店舗セレクター モジュールを追加する方法の詳細については、[カート モジュール](add-cart-module.md) を参照してください

## <a name="additional-resources"></a>追加リソース

[スタート キットの概要](starter-kit-overview.md)

[購入ボックス モジュール](add-buy-box.md)

[買い物カゴ モジュール](add-cart-module.md)

[PDP のクイック ツアー](quick-tour-pdp.md)

[カートとチェックアウトのクイック ツアー](quick-tour-cart-checkout.md)

[荷渡方法の設定](https://docs.microsoft.com/dynamicsax-2012/appuser-itpro/set-up-modes-of-delivery)
