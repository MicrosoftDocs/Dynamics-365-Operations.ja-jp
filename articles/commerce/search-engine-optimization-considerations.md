---
title: サイトにおける検索エンジン最適化 (SEO) の考慮事項
description: このトピックでは、サイトの開発から運用における、検索エンジンの最適化 (SEO) の考慮事項について説明します。
author: psimolin
ms.date: 05/25/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgri
ms.search.region: Global
ms.author: psimolin
ms.search.validFrom: 2019-10-31
ms.openlocfilehash: 2f90581766dba3d3a671df52ec08339a1a0fd7dc
ms.sourcegitcommit: 9dd2d32fc303023a509d58ec7b5935f89d1e9c6d
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/26/2022
ms.locfileid: "8806408"
---
# <a name="search-engine-optimization-seo-considerations-for-your-site"></a>サイトにおける検索エンジンの最適化 (SEO) の考慮事項


[!include [banner](includes/banner.md)]

このトピックでは、サイトの開発から運用における、検索エンジンの最適化 (SEO) の考慮事項について説明します。

## <a name="a-site-that-is-under-development"></a>開発中のサイト

検索エンジンが開発中のサイトにインデックスを付けないようにするには、すべてのサイト ページに **noindex** および **nofollow** メタ タグを設定する必要があります。 次のメタ タグの入力を含む[メタタグ モジュール](metatags-module.md) に基づいてフラグメントを作成し、そのフラグメントがサイトで使用されるすべてのテンプレートの HTML \<head\>セクションに追加されるようにすることをお勧めします。

```html
<meta name="robots" content="noindex,nofollow" /> 
```

## <a name="soft-launch-of-a-site"></a>サイトのソフト起動

「ソフト起動」中、完全な起動が行われる前は、限られた対象者またはマーケットに Web サイトが使用可能になります。 Web サイトのソフト起動を行う場合、**noindex** メタ タグの配置を検討する必要があります。 この方法で、ソフト起動が確実に制限された対象者だけに限定されるようにできます。

## <a name="a-site-that-is-in-production"></a>運用中のサイト

サイトが運用中の場合、すべてのサイト ページが正しくタグ付けされていることを確認する必要があります。 Microsoft Dynamics 365 Commerce は、ページに入力された情報を使用して、ページのすべての SEO 情報を表示します。 カテゴリ ページの概要、リスト ページの概要、および製品ページの概要のモジュールは、この機能を提供します。

検索エンジンのインデックスを最適化するために、レンダリング フレームワークは、Dynamics 365 Commerce およびモジュール固有の情報でコンフィギュレーションされた SEO プロパティからの両方の情報を使用します。 運用中のサイトの場合、robots.txt ファイルによりサイト全体のインデックスを作成することができ、公開したサイト マップ ドキュメントへのリンクを含んでいる必要があります。 **サイトの設定 \> サイト マップの有効化** で、サイト マップ生成の機能をオンにする必要があります。

### <a name="page-seo-settings-for-internal-preview-limited-audiences-and-all-audiences"></a>内部プレビュー、制限された対象者、およびすべての対象者に対するページの SEO 設定

Dynamics 365 Commerce は、ビジュアル ページ ビルダーの「What You See Is What You Get」 (WYSIWYG) 認証のプレビューをサポートしているので、作成者は情報がサイト訪問者に表示されるか心配することなく、ページ コンテンツを準備することができます。 ページを公開する必要はあるが、エクスポージャは制限する必要がある場合、検索エンジンでインデックスが作成されないようにするために **noindex** メタ タグが必要です。 ページがすべての対象者に準備されている場合、検索エンジン インデックスの効率を最大にするために、すべての基本的な SEO メタ データが存在する必要があります。 また、**nolimit** メタ タグを削除する必要があります。

## <a name="additional-resources"></a>追加リソース

[E コマース ユーザーとロールの管理](manage-ecommerce-users-roles.md)

[サイト ページにスクリプト コードを追加してテレメトリをサポートする](add-telemetry.md)

[コンテンツ セキュリティ ポリシー (CSP) の管理](manage-csp.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
