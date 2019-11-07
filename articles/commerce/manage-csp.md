---
title: Content Security Policy (CSP) の管理
description: このトピックでは、Microsoft Dynamics 365 Commerceの Content Security Policy (CSP) を管理する方法について説明します。
author: samjarawan
manager: annbe
ms.date: 10/01/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-retail
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
ms.openlocfilehash: 50f3ad942d5899614828dae0a0dd6d9f539c34fa
ms.sourcegitcommit: 1febba80b5a5f089d8f9c6929e07a356daa3aa86
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/23/2019
ms.locfileid: "2655152"
---
# <a name="manage-content-security-policy-csp"></a><span data-ttu-id="29a8c-103">Content Security Policy (CSP) の管理</span><span class="sxs-lookup"><span data-stu-id="29a8c-103">Manage Content Security Policy (CSP)</span></span>

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

<span data-ttu-id="29a8c-104">このトピックでは、Microsoft Dynamics 365 Commerceの Content Security Policy (CSP) を管理する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="29a8c-104">This topic describes how to manage Content Security Policy (CSP) in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="29a8c-105">概要</span><span class="sxs-lookup"><span data-stu-id="29a8c-105">Overview</span></span>

<span data-ttu-id="29a8c-106">CSP は、特定タイプの Web 攻撃の検出と軽減に役立つ追加のセキュリティ レベルです。</span><span class="sxs-lookup"><span data-stu-id="29a8c-106">CSP is an additional layer of security that helps detect and mitigate some types of web attacks.</span></span> <span data-ttu-id="29a8c-107">これらの攻撃の目的は、データの盗用からサイトの変造やマルウェアの配布まで多岐に指定できます。</span><span class="sxs-lookup"><span data-stu-id="29a8c-107">The purpose of these attacks can range from data theft, to site defacement, to the distribution of malware.</span></span> <span data-ttu-id="29a8c-108">CSP は、サイトページに読み込むことができるリソースを制御するのに役立つ、広範なポリシー ディレクティブのセットを提供します。</span><span class="sxs-lookup"><span data-stu-id="29a8c-108">CSP provides an extensive set of policy directives that help you control the resources that a site page is allowed to load.</span></span> <span data-ttu-id="29a8c-109">各ディレクティブは、特定のタイプのリソースに対する制限を定義します。</span><span class="sxs-lookup"><span data-stu-id="29a8c-109">Each directive defines the restrictions for a specific type of resource.</span></span>

<span data-ttu-id="29a8c-110">電子商取引サイトの CSP を有効にすると、接続、スクリプト、フォント、および未知または悪意のあるソースから発生したその他の種類のリソースをブロックすることによって、セキュリティを強化できます。</span><span class="sxs-lookup"><span data-stu-id="29a8c-110">When CSP is turned on for an e-Commerce site, it helps enhance security by blocking connections, scripts, fonts, and other types of resources that originate from unknown or malicious sources.</span></span> <span data-ttu-id="29a8c-111">Dynamics 365 Commerce では、CSP が既定で有効になります。</span><span class="sxs-lookup"><span data-stu-id="29a8c-111">In Dynamics 365 Commerce, CSP is turned on by default.</span></span> <span data-ttu-id="29a8c-112">ただし、ほとんどのサイトでは、追加のコンフィギュレーションが必要となる場合があります。</span><span class="sxs-lookup"><span data-stu-id="29a8c-112">However, it will likely require additional configuration for most sites.</span></span> <span data-ttu-id="29a8c-113">Dynamics 365 Commerce オンライン ソフトウェア開発キット (SDK) では、スタイル、スクリプト、およびアプリケーション プログラミング インターフェイス (API) の呼び出し元で許可されたソースの URLs における既定リストを提供します。</span><span class="sxs-lookup"><span data-stu-id="29a8c-113">The Dynamics 365 Commerce online software development kit (SDK) provides a default list of allowed source URLs that style, script, and application programming interface (API) calls can be made from.</span></span> <span data-ttu-id="29a8c-114">このリストは、コマースの**拡張性**タブで編集できます。</span><span class="sxs-lookup"><span data-stu-id="29a8c-114">You can edit this list on the **Extensibility** tab in Commerce.</span></span>

<span data-ttu-id="29a8c-115">CSP の詳細については、[Content Security Policy Reference](https://content-security-policy.com/) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="29a8c-115">For more information about CSP, see [Content Security Policy Reference](https://content-security-policy.com/).</span></span>

## <a name="csp-directives-in-commerce"></a><span data-ttu-id="29a8c-116">コマースの CSP ディレクティブ</span><span class="sxs-lookup"><span data-stu-id="29a8c-116">CSP directives in Commerce</span></span>

<span data-ttu-id="29a8c-117">次の CSP ディレクティブは、コマース サイトで使用できます。</span><span class="sxs-lookup"><span data-stu-id="29a8c-117">The following CSP directives can be used on Commerce sites.</span></span>

| <span data-ttu-id="29a8c-118">ディレクティブ</span><span class="sxs-lookup"><span data-stu-id="29a8c-118">Directive</span></span>   | <span data-ttu-id="29a8c-119">説明</span><span class="sxs-lookup"><span data-stu-id="29a8c-119">Description</span></span> |
|-------------|-------------|
| <span data-ttu-id="29a8c-120">child-src</span><span class="sxs-lookup"><span data-stu-id="29a8c-120">child-src</span></span>   | <span data-ttu-id="29a8c-121">このディレクティブは、**&lt;フレーム&gt;** および**&lt;iframe&gt;** などの要素を使用して読み込まれる、Web ワーカーと入れ子になったブラウジング コンテキストの有効なソースを定義します。</span><span class="sxs-lookup"><span data-stu-id="29a8c-121">This directive defines valid sources of web workers and nested browsing contexts that are loaded by using elements such as **&lt;frame&gt;** and **&lt;iframe&gt;**.</span></span> |
| <span data-ttu-id="29a8c-122">connect-src</span><span class="sxs-lookup"><span data-stu-id="29a8c-122">connect-src</span></span> | <span data-ttu-id="29a8c-123">このディレクティブは、AJAX 要求を作成できる URLs を定義します。</span><span class="sxs-lookup"><span data-stu-id="29a8c-123">This directive defines the URLs that AJAX requests can be made from.</span></span> |
| <span data-ttu-id="29a8c-124">font-src</span><span class="sxs-lookup"><span data-stu-id="29a8c-124">font-src</span></span>    | <span data-ttu-id="29a8c-125">このディレクティブは、フォントの有効なソースを定義します。</span><span class="sxs-lookup"><span data-stu-id="29a8c-125">This directive defines valid sources of fonts.</span></span> |
| <span data-ttu-id="29a8c-126">img-src</span><span class="sxs-lookup"><span data-stu-id="29a8c-126">img-src</span></span>     | <span data-ttu-id="29a8c-127">このディレクティブは、画像の有効なソースを定義します。</span><span class="sxs-lookup"><span data-stu-id="29a8c-127">This directive defines valid sources of images.</span></span> |
| <span data-ttu-id="29a8c-128">media-src</span><span class="sxs-lookup"><span data-stu-id="29a8c-128">media-src</span></span>   | <span data-ttu-id="29a8c-129">このディレクティブは、HTML5 **&lt;オーディオ&gt;** および **&lt;ビデオ&gt;** 要素などのオーディオおよびビデオの有効なソースを定義します。</span><span class="sxs-lookup"><span data-stu-id="29a8c-129">This directive defines valid sources of audio and video, such as HTML5 **&lt;audio&gt;** and **&lt;video&gt;** elements.</span></span> |
| <span data-ttu-id="29a8c-130">object-src</span><span class="sxs-lookup"><span data-stu-id="29a8c-130">object-src</span></span>  | <span data-ttu-id="29a8c-131">このディレクティブは、**&lt;オブジェクト&gt;**、**&lt;埋め込み&gt;**、および **&lt;アプレット&gt;** の要素などのプラグインの有効なソースを定義します。</span><span class="sxs-lookup"><span data-stu-id="29a8c-131">This directive defines valid sources of plug-ins, such as **&lt;object&gt;**, **&lt;embed&gt;**, and **&lt;applet&gt;** elements.</span></span> |
| <span data-ttu-id="29a8c-132">script-src</span><span class="sxs-lookup"><span data-stu-id="29a8c-132">script-src</span></span>  | <span data-ttu-id="29a8c-133">このディレクティブは、JavaScript の有効なソースを定義します。</span><span class="sxs-lookup"><span data-stu-id="29a8c-133">This directive defines valid sources of JavaScript.</span></span> |
| <span data-ttu-id="29a8c-134">style-src</span><span class="sxs-lookup"><span data-stu-id="29a8c-134">style-src</span></span>   | <span data-ttu-id="29a8c-135">このディレクティブは、stylesheets の有効なソースを定義します。</span><span class="sxs-lookup"><span data-stu-id="29a8c-135">This directive defines valid sources of stylesheets.</span></span> |

### <a name="example-configure-a-csp-directive"></a><span data-ttu-id="29a8c-136">例: CSP ディレクティブのコンフィギュレーション</span><span class="sxs-lookup"><span data-stu-id="29a8c-136">Example: Configure a CSP directive</span></span>

<span data-ttu-id="29a8c-137">次の例は、サイトから外部スクリプトを呼び出すことができるように、CSP ディレクティブを設定する方法を示しています。</span><span class="sxs-lookup"><span data-stu-id="29a8c-137">The following example shows how to configure a CSP directive so that an external script can be called from your site.</span></span>

1. <span data-ttu-id="29a8c-138">コマースで、サイトに移動します。</span><span class="sxs-lookup"><span data-stu-id="29a8c-138">In Commerce, go to your site.</span></span>
1. <span data-ttu-id="29a8c-139">**サイト管理**を選び、**拡張性**タブを選択します。</span><span class="sxs-lookup"><span data-stu-id="29a8c-139">Select **Site Management**, and then select the **Extensibility** tab.</span></span>
1. <span data-ttu-id="29a8c-140">**Content Security Policy** タブの、**スクリプト -src**で**追加**をクリックし、呼び出す外部スクリプトの完全な URL を入力します。</span><span class="sxs-lookup"><span data-stu-id="29a8c-140">On the **Content Security Policy** tab, under **script-src**, select **Add**, and then enter the full URL of the external script that should be called.</span></span>

    ![Content Security Policy タブの外部スクリプト用 URL](media/content-security-policy.png)

1. <span data-ttu-id="29a8c-142">**保存と公開**を選択します。</span><span class="sxs-lookup"><span data-stu-id="29a8c-142">Select **Save and Publish**.</span></span>

## <a name="interpret-and-fix-csp-errors"></a><span data-ttu-id="29a8c-143">CSP エラーの解釈と修正</span><span class="sxs-lookup"><span data-stu-id="29a8c-143">Interpret and fix CSP errors</span></span>

<span data-ttu-id="29a8c-144">最初にサイトの CSP をコンフィギュレーションすると、一部のページがまったく読み込まれないか、意図したとおりに機能しない可能性があります。それは、CSP が外部接続、スクリプト、フォント、およびその他の種類のリソースの読み込みをブロックしているからです。</span><span class="sxs-lookup"><span data-stu-id="29a8c-144">When you first configure CSP for a site, some pages probably won't be loaded at all or won't work as intended, because CSP is blocking external connections, scripts, fonts, and other types of resources from being loaded.</span></span> <span data-ttu-id="29a8c-145">ただし、CSP は不要な要求または不要な要求を修正、調整、およびクリーン アップするために使用できるいくつかの有用なエラーをログに記録します。</span><span class="sxs-lookup"><span data-stu-id="29a8c-145">Fortunately, CSP logs some helpful errors that you can use to fix, tune, and clean up unwanted or unneeded requests.</span></span>

<span data-ttu-id="29a8c-146">次の図では、Web ブラウザーの開発ツールにおける CSP エラーの例を示しています。</span><span class="sxs-lookup"><span data-stu-id="29a8c-146">The following illustration shows an example of CSP errors in a web browser's developer tools.</span></span>

![Web ブラウザーの開発者ツールにおける CSP エラー](media/content-security-policy-errors.png)

<span data-ttu-id="29a8c-148">この例では、次の 2 つの CSP エラーがあります。</span><span class="sxs-lookup"><span data-stu-id="29a8c-148">There are two CSP errors in this example:</span></span>

- <span data-ttu-id="29a8c-149">**Eval** 関数は、任意の JavaScript を実行する可能性があるため、既定ではブロックされています。</span><span class="sxs-lookup"><span data-stu-id="29a8c-149">The **Eval** function is blocked by default, because it can cause arbitrary JavaScript execution.</span></span> <span data-ttu-id="29a8c-150">この関数を使用するには、**'危険 -eval'** をサイトの**スクリプト -src** ディレクティブに追加します。</span><span class="sxs-lookup"><span data-stu-id="29a8c-150">To allow this function, add **'unsafe-eval'** to your site's **script-src** directive.</span></span> <span data-ttu-id="29a8c-151">単一の引用符が必要です。</span><span class="sxs-lookup"><span data-stu-id="29a8c-151">The single quotation marks are required.</span></span>
- <span data-ttu-id="29a8c-152">外部スタイルシートがブロックされています。</span><span class="sxs-lookup"><span data-stu-id="29a8c-152">The external stylesheet is blocked.</span></span> <span data-ttu-id="29a8c-153">スタイルシートを外部ドメインから読み込むには、URL をサイトの**スタイル -src** ディレクティブに追加します。</span><span class="sxs-lookup"><span data-stu-id="29a8c-153">To allow a stylesheet to be loaded from an external domain, add the URL to your site's **style-src** directive.</span></span>

<span data-ttu-id="29a8c-154">次のスクリーンショットでは、コマースにて **Content Security Policy** タブの固定設定がどのように表示されるか示します。</span><span class="sxs-lookup"><span data-stu-id="29a8c-154">The following screenshot shows what the fixed settings look like on the **Content Security Policy** tab in Commerce.</span></span>

![Content Security Policy タブの固定設定](media/content-security-policy-fixed.png)

## <a name="update-page-mocks-that-use-csp"></a><span data-ttu-id="29a8c-156">CSP を使用するページ モックの更新</span><span class="sxs-lookup"><span data-stu-id="29a8c-156">Update page mocks that use CSP</span></span>

<span data-ttu-id="29a8c-157">開発環境でオンライン SDK を使用してモジュールをテストする場合、ページ モックを使用して CSP を追加することもできます。</span><span class="sxs-lookup"><span data-stu-id="29a8c-157">If you're testing modules by using the online SDK in a development environment, you can also add CSP by using page mocks.</span></span> <span data-ttu-id="29a8c-158">ページ モックでは、トップ レベルの **"appContext"** プロパティを追加するか、または既存のトップレベルの **"appContext"** プロパティに移動して、**"contentSecurityPolicy"** という名前のプロパティを作成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="29a8c-158">In a page mock, you must either add a top-level **"appContext"** property or go to the existing top-level **"appContext"** property, and create a property under it that is named **"contentSecurityPolicy"**.</span></span> <span data-ttu-id="29a8c-159">ここでは、次の例に示すように、ディレクティブのキー / 値ペアをポリシーに追加できます。</span><span class="sxs-lookup"><span data-stu-id="29a8c-159">There, you can add key/value pairs of directives to policies, as shown in the following example.</span></span>

```
"appContext": {
    "contentSecurityPolicy": {
        "script-src": ["https://www.w3schools.com/js/myScript.js"],
        "font-src": ["https://*.commerce.dynamics.com"]
    }
}
```

> [!NOTE]
> <span data-ttu-id="29a8c-160">ページ モックに CSP ポリシーを追加する場合、ページ モックには、プラットフォームによって提供される既定の CSP ポリシーは含まれません。</span><span class="sxs-lookup"><span data-stu-id="29a8c-160">If you add CSP policies in a page mock, the page mock won't include any of the default CSP policies that are provided by the platform.</span></span>

<span data-ttu-id="29a8c-161">ページ モックで CSP を無効にするには、次のコードを使用します。</span><span class="sxs-lookup"><span data-stu-id="29a8c-161">You can turn off CSP in a page mock by using the following code.</span></span>

```
"appContext": {
    "contentSecurityPolicy": {
        "disableContentSecurityPolicy": true
    }
}
```

## <a name="turn-off-csp-for-a-site"></a><span data-ttu-id="29a8c-162">サイトの CSP を無効</span><span class="sxs-lookup"><span data-stu-id="29a8c-162">Turn off CSP for a site</span></span>

<span data-ttu-id="29a8c-163">CSP がサイトにポリシーが適用しないようにするには、そのサイトに対してポリシーを無効にできます。</span><span class="sxs-lookup"><span data-stu-id="29a8c-163">To prevent CSP from applying policies to your site, you can turn it off for that site.</span></span>

1. <span data-ttu-id="29a8c-164">コマースで、サイトに移動します。</span><span class="sxs-lookup"><span data-stu-id="29a8c-164">In Commerce, go to your site.</span></span>
1. <span data-ttu-id="29a8c-165">**サイト管理**を選び、**拡張性**タブを選択します。</span><span class="sxs-lookup"><span data-stu-id="29a8c-165">Select **Site Management**, and then select the **Extensibility** tab.</span></span>
1. <span data-ttu-id="29a8c-166">**Content Security Policy** タブで、**コンテンツ セキュリティ ポリシーを無効にする**チェックボックスを選択します。</span><span class="sxs-lookup"><span data-stu-id="29a8c-166">On the **Content Security Policy** tab, select the **Disable content security policy** check box.</span></span>

    ![Content Security Policy タブで、コンテンツ セキュリティ ポリシーを無効にする](media/content-security-policy-disable.png)

1. <span data-ttu-id="29a8c-168">**保存と公開**を選択します。</span><span class="sxs-lookup"><span data-stu-id="29a8c-168">Select **Save and Publish**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="29a8c-169">追加リソース</span><span class="sxs-lookup"><span data-stu-id="29a8c-169">Additional resources</span></span>

[<span data-ttu-id="29a8c-170">E コマース ユーザーとロールの管理</span><span class="sxs-lookup"><span data-stu-id="29a8c-170">Manage e-Commerce users and roles</span></span>](manage-ecommerce-users-roles.md)

[<span data-ttu-id="29a8c-171">サイト ページにスクリプト コードを追加してテレメトリをサポートする</span><span class="sxs-lookup"><span data-stu-id="29a8c-171">Add script code to site pages to support telemetry</span></span>](add-telemetry.md)

[<span data-ttu-id="29a8c-172">サイトにおける検索エンジン最適化 (SEO) の考慮事項</span><span class="sxs-lookup"><span data-stu-id="29a8c-172">Search engine optimization (SEO) considerations for your site</span></span>](search-engine-optimization-considerations.md)
