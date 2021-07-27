---
title: Adventure Works テーマの概要
description: このトピックでは、Adventure Works テーマの概要を示し、Microsoft Dynamics 365 Commerce のサイト ページに適用する方法を説明します。
author: anupamar-ms
ms.date: 07/08/2021
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
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: c7557a36a948de5ae877d74bbbdea78821099b82
ms.sourcegitcommit: 7e976059118938b0089e40bef948029a8c088b38
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 07/09/2021
ms.locfileid: "6479488"
---
# <a name="adventure-works-theme-overview"></a>Adventure Works テーマの概要

[!include [banner](includes/banner.md)]
[!include [banner](includes/preview-banner.md)]

このトピックでは、Adventure Works テーマの概要を示し、Microsoft Dynamics 365 Commerce のサイト ページに適用する方法を説明します。

Dynamics 365 Commerce には、Adventure Works という名前の eコマースのテーマがあります。 Adventure Works テーマは、スポーツとスポーツに関連する製品を紹介し、豊富で強化された釣り合い体験のために最適化されます。 これは、最新の外観、新しいレイアウト、およびアニメーション効果を提供し、eコマース顧客に対するオンライン買い物の経験を提供します。

Adventure Works テーマは、次の新しいワークフローを提供します。

- ビデオ プレーヤー モジュールは、追加のオプションでヘッダー、段落、およびリンク機能をサポートします。
- カートに追加アクションは、通知を提供する代わりにミニ カートを呼び出します。
- クイック ビュー モジュールは、デスクトップ ビューポートとモバイル ビューポートの両方にスライドするウィンドウです。
- 空の買い物カゴでプロモーションを紹介することができます。

Adventure Works テーマには、Commerce モジュール ライブラリに次のモジュールが含まれています:

- タイル リスト モジュール
- 対話型フィーチャー モジュール
- モジュールを登録する
- 有効な画像モジュール
- イメージ リスト モジュール

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

## <a name="additional-resources"></a>追加リソース

[モジュール ライブラリの概要](starter-kit-overview.md)

[タイル リスト モジュール](tile-list-module.md)

[対話型フィーチャー モジュール](interactive-feature-module.md)

[有効な画像モジュール](active-image-module.md)

[モジュールを登録する](subscribe-module.md)

[イメージ リスト モジュール](image-list-module.md)

[テーマ拡張](e-commerce-extensibility/theme-module-extensions.md)

[カート アイコン モジュール](cart-icon-module.md)

[B2B eコマース サイトの設定](./b2b/set-up-b2b-site.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
