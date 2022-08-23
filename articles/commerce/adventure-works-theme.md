---
title: Adventure Works テーマの概要
description: この記事では、Adventure Works テーマの概要を示し、Microsoft Dynamics 365 Commerce のサイト ページに適用する方法を説明します。
author: anupamar-ms
ms.date: 12/03/2021
ms.topic: overview
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.8
ms.search.industry: ''
ms.search.form: ''
ms.openlocfilehash: ae2af73a17e03ca216665e515ac4739e02944b8c
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/12/2022
ms.locfileid: "9278681"
---
# <a name="adventure-works-theme-overview"></a>Adventure Works テーマの概要

[!include [banner](includes/banner.md)]

この記事では、Adventure Works テーマの概要を示し、Microsoft Dynamics 365 Commerce のサイト ページに適用する方法を説明します。

Dynamics 365 Commerce には、Adventure Works という名前の eコマースのテーマがあります。 Adventure Works テーマは、スポーツとスポーツに関連する製品を紹介し、豊富で強化された釣り合い体験のために最適化されます。 これは、最新の外観、新しいレイアウト、およびアニメーション効果を提供し、eコマース顧客に対するオンライン買い物の経験を提供します。

## <a name="trial-environments-in-commerce"></a>Commerce での試用環境

Adventure Works テーマが企業と顧客間 (B2C) サイトおよび企業間 (B2B) サイトに配置された場合にどのようになるかを確認するには、次の試用版サイトを参照してください。

- [Adventure Works B2C サイト](https://www.adventure-works.com/)
- [Adventure Works B2B サイト](https://www.adventure-works.com/business)

## <a name="theme-capabilities"></a>テーマの機能

Adventure Works テーマは、次の新しい機能を提供します。

- ビデオ プレーヤー モジュールは、追加のストーリーテリングのためにヘッダー、段落、およびリンク機能をサポートします。
- アニメーションを通じてコンテンツの切り替えが可能になります。
- 「カートに追加」 アクションは、通知を提供する代わりにミニ カートを呼び出します。
- クイック ビュー モジュールは、デスクトップ ビューポートとモバイル ビューポートの両方にスライドするウィンドウです。
- サイト ページには新しいレイアウトがあります。 
- マーケティング コンテンツは、空の場合にカートおよびミニ カートに対してコンフィギュレーションできます。
- このミニ カートには、「50 ドルを超える注文で送料無料」 などのプロモーション メッセージが表示される
- 説明カードは、検索ページとカテゴリ ページに表示されます。

Adventure Works テーマには、Commerce モジュール ライブラリに次のストーリーテリング モジュールが含まれています。

- [タイトル リスト モジュール](tile-list-module.md)
- [対話型機能モジュール](interactive-feature-module.md)
- [有効な画像モジュール](active-image-module.md)
- [購読モジュール](subscribe-module.md)
- [画像リスト モジュール](image-list-module.md)

Adventure Works テーマは完全に応答可能であり、デスクトップ、モバイル、およびタブレットのビューポートに最適化されたエクスペリエンスを提供します。

> [!IMPORTANT]
> Adventure Works テーマおよび新しいモジュールは、Dynamics 365 Commerce バージョン 10.0.20 リリース時点で使用できます。

次の図は、Adventure Works のテーマを使用するホーム ページの例を示します。

![Adventure Works のテーマを使用するホーム ページの例](./media/aw_b2c.PNG)

次の図は、Adventure Works のテーマを使用するリスト ページの例を示します。

![Adventure Works のテーマを使用するリスト ページの例](./media/Aw_list.PNG)

次の図は、Adventure Works のテーマを使用する製品の詳細ページ (PDP) の例を示します。

![Adventure Works のテーマを使用する製品の詳細ページ (PDP) の例](./media/aw_pdp.PNG)

## <a name="use-the-adventure-works-theme-for-b2b-sites"></a>B2B サイト用の Adventure Works テーマの使用

Adventure Works テーマは、企業間 (B2B) サイトの参照テーマです。 すべての B2B のモジュールとワークフローは Adventure Works テーマで紹介されています。 B2B サイトの設定方法については、[B2B サイトの設定](./b2b/set-up-b2b-site.md)を参照してください。

次の図は、Adventure Works のテーマを使用する B2B ホーム ページの例を示します。

![Adventure Works のテーマを使用する B2B ホーム ページの例](./media/aw_b2b.PNG)

## <a name="theme-extensions"></a>テーマ拡張

Adventure Works テーマには、**表示拡張** および **モジュール定義** 拡張など、複数のテーマ拡張が含まれます。 Adventure Works テーマは、同様の拡張を構築するための参照テーマとして使用できます。 たとえば、Adventure Works テーマのリスト ページは、水平リファイナーのビュー拡張機能として実装されます。 (対照的に、Fabrikam テーマでは左ウィンドウのリファイナーが使用されます。)

同様に、他のモジュールにはモジュール定義拡張機能が含まれます。 たとえば、[買い物カゴ アイコン モジュール](cart-icon-module.md) には、モジュール定義拡張機能を使用して実装される 2 つの追加の **空の買い物カゴ** および **プロモーション コンテンツ** スロットが含まれます。 さらに、新しい **モバイル ロゴ** プロパティがヘッダー モジュールに追加され、モバイル ビューポートのロゴをサポートします。 このプロパティは、ヘッダー モジュール定義拡張機能として実装されます。

テーマ拡張機能の詳細については、[テーマ拡張](e-commerce-extensibility/theme-module-extensions.md) を参照してください。

## <a name="install-the-adventure-works-theme"></a>Adventure Works テーマのインストール

Adventure Works テーマのインストール方法については、[Adventure Works テーマのインストール](install-adventure-works.md) を参照してください。

## <a name="additional-resources"></a>追加リソース

[モジュール ライブラリの概要](starter-kit-overview.md)

[タイトル リスト モジュール](tile-list-module.md)

[対話型フィーチャー モジュール](interactive-feature-module.md)

[有効な画像モジュール](active-image-module.md)

[モジュールを登録する](subscribe-module.md)

[イメージ リスト モジュール](image-list-module.md)

[テーマ拡張](e-commerce-extensibility/theme-module-extensions.md)

[カート アイコン モジュール](cart-icon-module.md)

[B2B eコマース サイトの設定](./b2b/set-up-b2b-site.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
