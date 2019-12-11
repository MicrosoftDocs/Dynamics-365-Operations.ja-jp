---
title: サイトにおける検索エンジン最適化 (SEO) の考慮事項
description: このトピックでは、サイトの開発から運用における、検索エンジンの最適化 (SEO) の考慮事項について説明します。
author: psimolin
manager: annbe
ms.date: 10/01/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: psimolin
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: b35d0cb606e1b17a0258ea3fcb6287988d83091c
ms.sourcegitcommit: 295d940a345879b3dfc5991e387b91c7257019ea
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/01/2019
ms.locfileid: "2698214"
---
# <a name="search-engine-optimization-seo-considerations-for-your-site"></a>サイトにおける検索エンジン最適化 (SEO) の考慮事項

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

このトピックでは、サイトの開発から運用における、検索エンジンの最適化 (SEO) の考慮事項について説明します。

## <a name="a-site-that-is-under-development"></a>開発中のサイト

サイトが開発中の間、検索エンジンがページにインデックスを付けず、サイトの開発バージョンをキャッシュに保存しないようにするために、すべてのサイト ページに **NOINDEX** および **NOFOLLOW** メタ タグがある必要があります。 このコンフィギュレーションを実行するには、既定のメタ タグのモジュールをサイト ページのテンプレートに追加する必要があります。 既定のメタ タグのプロパティは、ページ エディターの SEO プロパティ セクションで使用可能になります。 これらのプロパティを使用して、メタ タグを管理できます。

## <a name="soft-launch-of-a-site"></a>サイトのソフト起動

「ソフト起動」中、完全な起動が行われる前は、限られた対象者またはマーケットに Web サイトが使用可能になります。 Web サイトのソフト起動を行う場合、**NOINDEX** メタ タグの配置を検討する必要があります。 この方法で、ソフト起動が確実に制限された対象者だけに限定されるようにできます。

## <a name="a-site-that-is-in-production"></a>運用中のサイト

サイトが運用中の場合、すべてのサイト ページが正しくタグ付けされていることを確認する必要があります。 Microsoft Dynamics 365 Commerce は、ページに入力された情報を使用して、ページのすべての SEO 情報を表示します。 カテゴリ ページの概要、リスト ページの概要、および製品ページの概要のモジュールは、この機能を提供します。

検索エンジンのインデックスを最適化するために、レンダリング フレームワークは、Dynamics 365 Commerce およびモジュール固有の情報でコンフィギュレーションされた SEO プロパティからの両方の情報を使用します。 運用中のサイトの場合、robots.txt ファイルによりサイト全体のインデックスを作成することができ、公開したサイト マップ ドキュメントへのリンクを含んでいる必要があります。 **サイトの設定 \> サイト マップの有効化**で、サイト マップ生成の機能をオンにする必要があります。

### <a name="page-seo-settings-for-internal-preview-limited-audiences-and-all-audiences"></a>内部プレビュー、制限された対象者、およびすべての対象者に対するページの SEO 設定

Dynamics 365 Commerce は 「What You See Is What You Get」 (WYSIWYG) 認証のプレビューをサポートしているので、作成者は情報がサイト訪問者に表示されるか心配することなく、ページ コンテンツを準備することができます。 ページを公開する必要はあるが、エクスポージャは制限する必要がある場合、検索エンジンでインデックスが作成されないようにするために **NOINDEX** メタ タグが必要です。 ページがすべての対象者に準備されている場合、検索エンジン インデックスの効率を最大にするために、すべての基本的な SEO メタ データが存在する必要があります。 また、**NOLIMIT** メタ タグを削除する必要があります。

## <a name="additional-resources"></a>追加リソース

[E コマース ユーザーとロールの管理](manage-ecommerce-users-roles.md)

[サイト ページにスクリプト コードを追加してテレメトリをサポートする](add-telemetry.md)

[コンテンツ セキュリティ ポリシー (CSP) の管理](manage-csp.md)
