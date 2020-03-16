---
title: Content Security Policy (CSP) の管理
description: このトピックでは、Microsoft Dynamics 365 Commerceの Content Security Policy (CSP) を管理する方法について説明します。
author: samjarawan
manager: annbe
ms.date: 10/01/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Developer
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: samjar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 08e10653362d0ef9afd223dc0d24dd9b5d25ed42
ms.sourcegitcommit: 3c1eb3d89c6ab9bd70b806ca42ef9df74cf850bc
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/12/2020
ms.locfileid: "3042793"
---
# <a name="manage-content-security-policy-csp"></a>Content Security Policy (CSP) の管理


[!include [banner](includes/banner.md)]

このトピックでは、Microsoft Dynamics 365 Commerceの Content Security Policy (CSP) を管理する方法について説明します。

## <a name="overview"></a>概要

CSP は、特定タイプの Web 攻撃の検出と軽減に役立つ追加のセキュリティ レベルです。 これらの攻撃の目的は、データの盗用からサイトの変造やマルウェアの配布まで多岐に指定できます。 CSP は、サイトページに読み込むことができるリソースを制御するのに役立つ、広範なポリシー ディレクティブのセットを提供します。 各ディレクティブは、特定のタイプのリソースに対する制限を定義します。

電子商取引サイトの CSP を有効にすると、接続、スクリプト、フォント、および未知または悪意のあるソースから発生したその他の種類のリソースをブロックすることによって、セキュリティを強化できます。 Dynamics 365 Commerce では、CSP が既定で有効になります。 ただし、ほとんどのサイトでは、追加のコンフィギュレーションが必要となる場合があります。 Dynamics 365 Commerce オンライン ソフトウェア開発キット (SDK) では、スタイル、スクリプト、およびアプリケーション プログラミング インターフェイス (API) の呼び出し元で許可されたソースの URLs における既定リストを提供します。 このリストは、コマースの**拡張性**タブで編集できます。

CSP の詳細については、[Content Security Policy Reference](https://content-security-policy.com/) を参照してください。

## <a name="csp-directives-in-commerce"></a>コマースの CSP ディレクティブ

次の CSP ディレクティブは、コマース サイトで使用できます。

| ディレクティブ   | 説明 |
|-------------|-------------|
| child-src   | このディレクティブは、**&lt;フレーム&gt;** および**&lt;iframe&gt;** などの要素を使用して読み込まれる、Web ワーカーと入れ子になったブラウジング コンテキストの有効なソースを定義します。 |
| connect-src | このディレクティブは、AJAX 要求を作成できる URLs を定義します。 |
| font-src    | このディレクティブは、フォントの有効なソースを定義します。 |
| img-src     | このディレクティブは、画像の有効なソースを定義します。 |
| media-src   | このディレクティブは、HTML5 **&lt;オーディオ&gt;** および **&lt;ビデオ&gt;** 要素などのオーディオおよびビデオの有効なソースを定義します。 |
| object-src  | このディレクティブは、**&lt;オブジェクト&gt;**、**&lt;埋め込み&gt;**、および **&lt;アプレット&gt;** の要素などのプラグインの有効なソースを定義します。 |
| script-src  | このディレクティブは、JavaScript の有効なソースを定義します。 |
| style-src   | このディレクティブは、stylesheets の有効なソースを定義します。 |

### <a name="example-configure-a-csp-directive"></a>例: CSP ディレクティブのコンフィギュレーション

次の例は、サイトから外部スクリプトを呼び出すことができるように、CSP ディレクティブを設定する方法を示しています。

1. コマースで、サイトに移動します。
1. **サイト管理**を選び、**拡張性**タブを選択します。
1. **Content Security Policy** タブの、**スクリプト -src**で**追加**をクリックし、呼び出す外部スクリプトの完全な URL を入力します。

    ![Content Security Policy タブの外部スクリプト用 URL](media/content-security-policy.png)

1. **保存と公開**を選択します。

## <a name="interpret-and-fix-csp-errors"></a>CSP エラーの解釈と修正

最初にサイトの CSP をコンフィギュレーションすると、一部のページがまったく読み込まれないか、意図したとおりに機能しない可能性があります。それは、CSP が外部接続、スクリプト、フォント、およびその他の種類のリソースの読み込みをブロックしているからです。 ただし、CSP は不要な要求または不要な要求を修正、調整、およびクリーン アップするために使用できるいくつかの有用なエラーをログに記録します。

次の図では、Web ブラウザーの開発ツールにおける CSP エラーの例を示しています。

![Web ブラウザーの開発者ツールにおける CSP エラー](media/content-security-policy-errors.png)

この例では、次の 2 つの CSP エラーがあります。

- **Eval** 関数は、任意の JavaScript を実行する可能性があるため、既定ではブロックされています。 この関数を使用するには、**'危険 -eval'** をサイトの**スクリプト -src** ディレクティブに追加します。 単一の引用符が必要です。
- 外部スタイルシートがブロックされています。 スタイルシートを外部ドメインから読み込むには、URL をサイトの**スタイル -src** ディレクティブに追加します。

次のスクリーンショットでは、コマースにて **Content Security Policy** タブの固定設定がどのように表示されるか示します。

![Content Security Policy タブの固定設定](media/content-security-policy-fixed.png)

## <a name="update-page-mocks-that-use-csp"></a>CSP を使用するページ モックの更新

開発環境でオンライン SDK を使用してモジュールをテストする場合、ページ モックを使用して CSP を追加することもできます。 ページ モックでは、トップ レベルの **"appContext"** プロパティを追加するか、または既存のトップレベルの **"appContext"** プロパティに移動して、**"contentSecurityPolicy"** という名前のプロパティを作成する必要があります。 ここでは、次の例に示すように、ディレクティブのキー / 値ペアをポリシーに追加できます。

```json
"appContext": {
    "contentSecurityPolicy": {
        "script-src": ["https://www.w3schools.com/js/myScript.js"],
        "font-src": ["https://*.commerce.dynamics.com"]
    }
}
```

> [!NOTE]
> ページ モックに CSP ポリシーを追加する場合、ページ モックには、プラットフォームによって提供される既定の CSP ポリシーは含まれません。

ページ モックで CSP を無効にするには、次のコードを使用します。

```json
"appContext": {
    "contentSecurityPolicy": {
        "disableContentSecurityPolicy": true
    }
}
```

## <a name="turn-off-csp-for-a-site"></a>サイトの CSP を無効

CSP がサイトにポリシーが適用しないようにするには、そのサイトに対してポリシーを無効にできます。

1. コマースで、サイトに移動します。
1. **サイト管理**を選び、**拡張性**タブを選択します。
1. **Content Security Policy** タブで、**コンテンツ セキュリティ ポリシーを無効にする**チェックボックスを選択します。

    ![Content Security Policy タブで、コンテンツ セキュリティ ポリシーを無効にする](media/content-security-policy-disable.png)

1. **保存と公開**を選択します。

## <a name="additional-resources"></a>追加リソース

[E コマース ユーザーとロールの管理](manage-ecommerce-users-roles.md)

[サイト ページにスクリプト コードを追加してテレメトリをサポートする](add-telemetry.md)

[サイトにおける検索エンジン最適化 (SEO) の考慮事項](search-engine-optimization-considerations.md)
