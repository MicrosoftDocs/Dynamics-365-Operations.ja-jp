---
title: マップ モジュール
description: このトピックでは、マップ モジュールを取り上げ、Microsoft Dynamics 365 Commerce での構成方法について説明します。
author: anupamar-ms
ms.date: 09/15/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2020-02-10
ms.dyn365.ops.version: Release 10.0.13
ms.openlocfilehash: b8c3ab0653fd5e3561d0bfbe85624d912756e2be
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/31/2021
ms.locfileid: "5794190"
---
# <a name="map-module"></a>地図モジュール

[!include [banner](includes/banner.md)]


このトピックでは、マップ モジュールを取り上げ、Microsoft Dynamics 365 Commerce での構成方法について説明します。

マップ モジュールは、[Bing Maps V8 Web コントロール](https://docs.microsoft.com/bingmaps/v8-web-control/) を使用してレンダリングされるインタラクティブなマップ上の店舗の場所を示します。 Bing Maps API キーは必須で、Commerce 本社の共有パラメータ ページに追加する必要があります。 マップ モジュールには、マップの場所を表示するためにユーザーが選択できる、道路、航空写真、路上などのさまざまなビューが用意されています。 また、ズームやユーザーの位置の使用などの操作も可能になります。

マップ モジュールは、マップにレンダリングする必要がある店舗の地理的な場所を決定するために、店舗セレクター モジュールと連携して機能します。 店舗セレクターとマップ モジュールは、ユーザーがサイト ページのいずれかのモジュールで店舗を選択したときに相互作用します。 マップ モジュールは、店舗セレクター モジュールとの相互作用を超えて、他のシナリオにも拡張できます。 ただし、モジュールのカスタマイズは必須です。

> [!NOTE]
> マップ モジュールは、Dynamics 365 Commerce 10.0.13 リリースで利用可能です。

以下の図は、店舗ロケーション ページで使用されるマップ モジュールの例を示しています。

![店舗セレクター モジュールの例](./media/ecommerce-Storelocator.PNG)

## <a name="module-properties"></a>モジュール プロパティ

| プロパティ名             | 先頭値                 | 説明 |
|---------------------------|-----------------------|-------------|
| ヘッダー | テキスト | モジュールのヘッダー。 |
| 押しピン オプション: 既定のアイコン | 画像 | マップに表示される店舗に使用する押しピンのシンボル イメージ。 |
| 押しピン オプション: アクティブ アイコン | 画像 | マップで選択された店舗に使用する押しピンのシンボル イメージ。 |
| 押しピン オプション: 既定のアイコン色 | 文字列 | マップ上の押しピン シンボル色のテキストまたは 16 進値。 |
| 押しピン オプション: アクティブ アイコン色 | 文字列 | マップ上の選択された押しピン シンボル色のテキストまたは 16 進値。 |
| インデックスの表示 | **True** または **False** | このプロパティが **True** に設定されている場合、店舗を示すすべての押しピン シンボルにインデックスが表示されます。 このインデックスは、店舗セレクター モジュールが表示するリスト表示のインデックスと一致します。 |

## <a name="add-allowed-mapping-urls-to-a-sites-content-security-policy-directives"></a>サイトのコンテンツ セキュリティ ポリシー ディレクティブに許可されたマッピング URLを追加する

マップ モジュールが Bing Maps と連携するには、サイトのコンテンツ セキュリティ ポリシー (CSP) に従って、次のマッピング URL が許可されていることを確認する必要があります。 この設定は、Commerce サイト ビルダーで、さまざまなサイト CSP ディレクティブ (**img-src** など) に許可された URL を追加することによって実行されます。 詳細については、[コンテンツ セキュリティ ポリシー](manage-csp.md)を参照してください。 

- **connect-src** ディレクティブに **&#42;.bing.com** を追加します。
- **img-src** ディレクティブに **&#42;.virtualearth.net** を追加します。
- **script-src** ディレクティブに、**&#42;.bing.com、&#42;.virtualearth.net** を追加します。
- **script style-src** ディレクティブに、**&#42;.bing.com** を追加します。

## <a name="add-a-map-module-to-a-page"></a>マップ モジュールをページに追加する

ページにマップ モジュールを構成する方法の詳細については、[店舗セレクター モジュール](store-selector.md) を参照してください。 
 
## <a name="additional-resources"></a>追加リソース

[モジュール ライブラリの概要](starter-kit-overview.md)

[購入ボックス モジュール](add-buy-box.md)

[カート モジュール](add-cart-module.md)

[店舗セレクター モジュール](store-selector.md)

[組織の Bing 地図の管理](./dev-itpro/manage-bing-maps.md)

[Bing Maps V8 Web コントロール](https://docs.microsoft.com/bingmaps/v8-web-control/)


[!INCLUDE[footer-include](../includes/footer-banner.md)]