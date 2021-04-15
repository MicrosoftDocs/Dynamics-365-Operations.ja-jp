---
title: ページ コンテンツのアクセシビリティの検証
description: このトピックでは、Microsoft Dynamics 365 Commerce のページ コンテンツのアクセシビリティを検証する方法について説明します。
author: josaw1
ms.date: 01/08/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.region: Global
ms.search.industry: retail
ms.author: josaw
ms.search.validFrom: 2019-12-19
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: 885696c13b0e5353e6dbd9dc21cf075d5e301786
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/31/2021
ms.locfileid: "5791634"
---
# <a name="verify-page-content-accessibility"></a>ページ コンテンツのアクセシビリティの検証

[!include [banner](includes/banner.md)]

このトピックでは、Microsoft Dynamics 365 Commerce のページ コンテンツのアクセシビリティを検証する方法について説明します。

ページの変更が完了したら、Web 上の全ユーザーがコンテンツにアクセスできることを確認する必要があります。 Commerce 作成ツールにおいて、統合された [Microsoft アクセシビリティ インサイト](https://accessibilityinsights.io/) サービスを使用することで、ページ コンテンツのアクセシビリティを簡単に確認できます。 このサービスは、ページと最新の [World Wide Web コンソーシアム (W3C) アクセシビリティ](https://www.w3.org/standards/webdesign/accessibility) ガイドラインを検証します。

[Microsoft アクセシビリティ インサイト](https://accessibilityinsights.io/) の統合は、使用する前に、テナントまたはサイト レベルで有効にする必要があります。

## <a name="turn-on-microsoft-accessibility-insights-for-all-the-sites-in-your-tenant"></a>テナント内のすべてのサイトに対する Microsoft アクセシビリティ インサイトの有効化

テナント内のすべての Commerce サイトに対する [Microsoft アクセシビリティ インサイト 統合](https://accessibilityinsights.io/) を有効にするには、次の手順を実行します。

> [!NOTE]
> テナントの設定にアクセスするには、システム管理者として Commerce にサインインする必要があります。

1. システム管理者として Commerce にサインインします。
1. 左のナビゲーション ウィンドウで、**テナントの設定** (ギア記号の横) を選択して展開します。
1. **テナントの設定** で、**機能** を選択します。
1. **アクセシビリティ チェック** オプションを **オン** にします。

## <a name="turn-on-microsoft-accessibility-insights-for-a-single-site"></a>1 つのサイトに対する Microsoft アクセシビリティ インサイトの有効化

1 つの Commerce サイトに対する [Microsoft アクセシビリティ インサイト 統合](https://accessibilityinsights.io/) を有効にするには、次の手順を実行します。

1. **サイト** で、**Fabrikam** (またはサイトの名前) を選択します。
1. 左のナビゲーション ウィンドウで、**サイト設定** を選択して展開します。
1. **サイト設定** で、**機能** を選択します。
1. **アクセシビリティ チェック** オプションを **オン** にします。

## <a name="verify-the-accessibility-of-the-content-on-the-home-page"></a>ホーム ページのコンテンツのアクセシビリティを確認する

統合された [Microsoft アクセシビリティ インサイト](https://accessibilityinsights.io/) サービスを使用して、Commerce のホーム ページのコンテンツのスキャンおよび確認をするには、次の手順を実行します。

1. **サイト** で、**Fabrikam** (またはサイトの名前) を選択します。
1. 左のナビゲーション ウィンドウで、**ページ** を選択します。
1. ホーム ページを検索、選択して、ページ エディターで開きます。
1. コマンド バーで、**アクセシビリティのチェック** を選択します。 **アクセシビリティのチェック** のページが表示されます。
1. スキャンが完了した後、レポートの内容を確認します。
1. チェックが失敗した場合、失敗したチェック項目をそれぞれ選択して展開し、詳細を表示します。
1. 確認した後、レポートを閉じるには、**アクセシビリティのチェック** ページの下部までスクロールし、**OK** を選択します。

## <a name="additional-resources"></a>追加リソース

[既存のサイト ページの変更](modify-existing-page.md)

[新しいサイト ページの追加](add-new-page.md)

[ページ レイアウトの選択](select-page-layouts.md)

[SEO メタデータの管理](manage-seo-metadata.md)

[ページの保存、プレビュー、および公開](save-preview-publish-page.md)

[製品ページの拡充](enrich-product-page.md)

[カテゴリ ランディング ページの拡充](enrich-category-page.md)

[URL のパラメーターに基いて動的な電子商取引ページを作成する](create-dynamic-pages.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
