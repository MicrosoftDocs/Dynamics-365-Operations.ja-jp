---
title: 製品分析コードの表示設定を適用する
description: この記事では、商品の分析コードの表示設定と、Microsoft Dynamics 365 Commerce で適用する方法について説明します。
author: anupamar-ms
ms.date: 05/28/2021
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
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: ''
ms.openlocfilehash: d7575e205a9732259b00e424f66eeadfe8c659ee
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/03/2022
ms.locfileid: "8899178"
---
# <a name="apply-display-settings-for-product-dimensions"></a>製品分析コードの表示設定を適用する

[!include [banner](includes/banner.md)]


この記事では、商品の分析コードの表示設定と、Microsoft Dynamics 365 Commerce で適用する方法について説明します。

Dynamics 365 Commerce では、製品のバリエーションを区別するために、サイズ、スタイル、カラーの分析コードをサポートしています。 通常、分析コードでは、サイズが "小"、"中"、"大"、色が "黒"、"茶" などのテキスト値として表示されます。 しかし、多くのバリエーションがある製品の場合、それぞれのバリエーションの画像を表示させる複数の選択が必要となるため、製品のバリエーションの参照が困難になります。 Commerce のバージョン 10.0.20 では、商品のバリエーションをより簡単に閲覧できるように、画像や 16 進数 (hex) コードを使って分析コードを見本として表示できるようになりました。

分析コードの定義は、Commerce のサイトビルダーの、**サイト設定 \> 拡張機能 \> 分析コードの設定** で行います。 以下の図は、サイト ビルダー内における分析コードの表示例を示しています。

![Commerce サイト ビルダーでのサイト設定例。](./dev-itpro/media/swatch_site_settings.PNG)

次の 2 つの分析コード設定を使用できます:

- **画像として表示する分析コード** - 商品詳細ページ (PDP) や検索結果一覧ページなど、eコマース サイトのページで見本として表示する寸法を指定します。 色、サイズ、スタイルの分析コードはどのような組み合わせでも見本として表示できます。 見本としての表示に分析コードが選択されている場合、Commerce モジュールのレンダリングは、利用可能な 16 進コードの見本の構成を探して選択します。 16 進コードが構成されていない場合、システム ロジックは画像の URL 見本の構成を探します。 16 進コードも画像 URL も設定されていない場合は、テキストが表示されます。

    次の図は、eコマースの PDP に色見本やサイズ見本が含まれている例です。 この例では、カラー分析コードに調整コードが構成されています。 そのため、見本は色として表示されています。 しかし、サイズの分析コードには 16 進数も画像 URL も構成されていません。 そのため、テキストは表示されます。

    ![eコマースの商品詳細ページに色見本として表示されるカラー分析コードの例。](./dev-itpro/media/swatch_pdp.png)

- **製品カードに表示する分析コード** - リストやリストページに表示される商品カードに表示する分析コードを指定します。 分析コードを製品カードに表示する前に、その分析コードに対してこの設定を有効にする必要があります。 **画像として表示する分析コード** も有効にする必要があります。 商品カードの見本選択の動作は、カラー分析コードに合わせて最適化されています。 他の分析コードの場合、見本の選択動作をカスタマイズするために、ビューの拡張機能が必要となる場合があります。

    次の図は、電子コマース サイトのリスト ページに色見本を含む商品カードがある場合の例です。

    ![eコマースの一覧ページに色見本として表示されるカラー分析コードの例。](./dev-itpro/media/swatch_searchresults.PNG)

サイトのページに見本として表示されるように製品の分析コードを設定する方法については、[製品の分析コード値を見本として表示する設定](./dev-itpro/dimensions-swatch.md)をご覧ください。

## <a name="additional-resources"></a>追加リソース

[モジュール ライブラリの概要](starter-kit-overview.md)

[検索結果モジュール](search-result-module.md)

[購入ボックス モジュール](add-buy-box.md)

[製品の分析コード値を見本として表示する設定](./dev-itpro/dimensions-swatch.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
