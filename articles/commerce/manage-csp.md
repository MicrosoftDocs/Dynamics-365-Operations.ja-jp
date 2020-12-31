---
title: Content Security Policy (CSP) の管理
description: このトピックでは、Microsoft Dynamics 365 Commerceの Content Security Policy (CSP) を管理する方法について説明します。
author: samjarawan
manager: annbe
ms.date: 11/13/2020
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
ms.openlocfilehash: 2950e62e6bbdea614e1141738513bf983b224a5e
ms.sourcegitcommit: deb711c92251ed48cdf20ea514d03461c26a2262
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/25/2020
ms.locfileid: "4645936"
---
# <a name="manage-content-security-policy-csp"></a><span data-ttu-id="cd69b-103">Content Security Policy (CSP) の管理</span><span class="sxs-lookup"><span data-stu-id="cd69b-103">Manage Content Security Policy (CSP)</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="cd69b-104">このトピックでは、Microsoft Dynamics 365 Commerceの Content Security Policy (CSP) を管理する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="cd69b-104">This topic describes how to manage Content Security Policy (CSP) in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="cd69b-105">概要</span><span class="sxs-lookup"><span data-stu-id="cd69b-105">Overview</span></span>

<span data-ttu-id="cd69b-106">CSP は、特定タイプの Web 攻撃の検出と軽減に役立つ追加のセキュリティ レベルです。</span><span class="sxs-lookup"><span data-stu-id="cd69b-106">CSP is an additional layer of security that helps detect and mitigate some types of web attacks.</span></span> <span data-ttu-id="cd69b-107">これらの攻撃の目的は、データの盗用からサイトの変造やマルウェアの配布まで多岐に指定できます。</span><span class="sxs-lookup"><span data-stu-id="cd69b-107">The purpose of these attacks can range from data theft, to site defacement, to the distribution of malware.</span></span> <span data-ttu-id="cd69b-108">CSP は、サイトページに読み込むことができるリソースを制御するのに役立つ、広範なポリシー ディレクティブのセットを提供します。</span><span class="sxs-lookup"><span data-stu-id="cd69b-108">CSP provides an extensive set of policy directives that help you control the resources that a site page is allowed to load.</span></span> <span data-ttu-id="cd69b-109">各ディレクティブは、特定のタイプのリソースに対する制限を定義します。</span><span class="sxs-lookup"><span data-stu-id="cd69b-109">Each directive defines the restrictions for a specific type of resource.</span></span>

<span data-ttu-id="cd69b-110">電子商取引サイトの CSP を有効にすると、接続、スクリプト、フォント、および未知または悪意のあるソースから発生したその他の種類のリソースをブロックすることによって、セキュリティを強化できます。</span><span class="sxs-lookup"><span data-stu-id="cd69b-110">When CSP is turned on for an e-Commerce site, it helps enhance security by blocking connections, scripts, fonts, and other types of resources that originate from unknown or malicious sources.</span></span> <span data-ttu-id="cd69b-111">Dynamics 365 Commerce では、CSP が既定で有効になります。</span><span class="sxs-lookup"><span data-stu-id="cd69b-111">In Dynamics 365 Commerce, CSP is turned on by default.</span></span> <span data-ttu-id="cd69b-112">ただし、ほとんどのサイトでは、追加のコンフィギュレーションが必要となる場合があります。</span><span class="sxs-lookup"><span data-stu-id="cd69b-112">However, it will likely require additional configuration for most sites.</span></span> <span data-ttu-id="cd69b-113">Dynamics 365 Commerce オンライン ソフトウェア開発キット (SDK) では、スタイル、スクリプト、およびアプリケーション プログラミング インターフェイス (API) の呼び出し元で許可されたソースの URLs における既定リストを提供します。</span><span class="sxs-lookup"><span data-stu-id="cd69b-113">The Dynamics 365 Commerce online software development kit (SDK) provides a default list of allowed source URLs that style, script, and application programming interface (API) calls can be made from.</span></span> <span data-ttu-id="cd69b-114">サイトビルダー ツールの **拡張** タブで、このリストを編集できます。</span><span class="sxs-lookup"><span data-stu-id="cd69b-114">You can edit this list on the **Extensions** tab in the site builder tool.</span></span>

<span data-ttu-id="cd69b-115">CSP の詳細については、[Content Security Policy Reference](https://content-security-policy.com/) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="cd69b-115">For more information about CSP, see [Content Security Policy Reference](https://content-security-policy.com/).</span></span>

## <a name="csp-settings"></a><span data-ttu-id="cd69b-116">CSP 設定</span><span class="sxs-lookup"><span data-stu-id="cd69b-116">CSP settings</span></span>

### <a name="turn-off-csp-for-a-site"></a><span data-ttu-id="cd69b-117">サイトの CSP を無効</span><span class="sxs-lookup"><span data-stu-id="cd69b-117">Turn off CSP for a site</span></span>

<span data-ttu-id="cd69b-118">CSP がサイトにポリシーが適用しないようにするには、サイト ビルダーのそのサイトに対してポリシーを無効にできます。</span><span class="sxs-lookup"><span data-stu-id="cd69b-118">To prevent CSP from applying policies to your site, you can turn it off for that site in site builder.</span></span>

<span data-ttu-id="cd69b-119">サイトの CSP を無効にするには、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="cd69b-119">To turn off CSP for a site, follow these steps.</span></span>

1. <span data-ttu-id="cd69b-120">サイト ビルダーで、作業しているサイトを選択します。</span><span class="sxs-lookup"><span data-stu-id="cd69b-120">In site builder, select the site you are working on.</span></span>
1. <span data-ttu-id="cd69b-121">**サイト設定** を選択し、**拡張** タブを選択します。</span><span class="sxs-lookup"><span data-stu-id="cd69b-121">Select **Site settings**, and then select the **Extensions** tab.</span></span>
1. <span data-ttu-id="cd69b-122">**コンテンツ セキュリティ ポリシー** タブで、**コンテンツ セキュリティ ポリシーを無効にする** チェック ボックスを選択します。</span><span class="sxs-lookup"><span data-stu-id="cd69b-122">On the **Content security policy** tab, select the **Disable content security policy** check box.</span></span>

    ![Content Security Policy タブで、コンテンツ セキュリティ ポリシーを無効にする](media/content-security-policy-disable.png)

1. <span data-ttu-id="cd69b-124">**保存と公開** を選択します。</span><span class="sxs-lookup"><span data-stu-id="cd69b-124">Select **Save and publish**.</span></span>

### <a name="enable-report-only-mode"></a><span data-ttu-id="cd69b-125">レポートのみモードの有効化</span><span class="sxs-lookup"><span data-stu-id="cd69b-125">Enable report only mode</span></span>

<span data-ttu-id="cd69b-126">CSP が有効になっている場合、コンテンツ セキュリティ ポリシーは適用されませんが、すべての違反がレポート URI ディレクティブで指定された URI に報告されます。</span><span class="sxs-lookup"><span data-stu-id="cd69b-126">If CSP is enabled, content security policy will not be enforced, but any violations will be reported to URIs specified by the report-uri directive.</span></span>

<span data-ttu-id="cd69b-127">レポートのみのモードを有効化するには、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="cd69b-127">To enable report only mode, follow these steps.</span></span>

1. <span data-ttu-id="cd69b-128">サイト ビルダーで、作業しているサイトを選択します。</span><span class="sxs-lookup"><span data-stu-id="cd69b-128">In site builder, select the site you are working on.</span></span>
1. <span data-ttu-id="cd69b-129">**サイト設定** を選択し、**拡張** タブを選択します。</span><span class="sxs-lookup"><span data-stu-id="cd69b-129">Select **Site settings**, and then select the **Extensions** tab.</span></span>
1. <span data-ttu-id="cd69b-130">**コンテンツ セキュリティ ポリシー** タブで、**レポートのみのモードの有効化** チェック ボックスを選択します。</span><span class="sxs-lookup"><span data-stu-id="cd69b-130">On the **Content security policy** tab, select the **Enable report only mode** check box.</span></span>

### <a name="enable-nonce"></a><span data-ttu-id="cd69b-131">Nonce を有効にする</span><span class="sxs-lookup"><span data-stu-id="cd69b-131">Enable nonce</span></span>

<span data-ttu-id="cd69b-132">Nonce (1 回だけ使用する番号) を有効にすると、[インライン スクリプト モジュール](e-commerce-extensibility/script-injector.md) 内で特定されたものを除き、すべてのインライン スクリプトの実行がブロックされます。</span><span class="sxs-lookup"><span data-stu-id="cd69b-132">Enabling nonce (number used once) will block the execution of all inline scripts except those specified within the [inline script](e-commerce-extensibility/script-injector.md) module.</span></span> <span data-ttu-id="cd69b-133">一意の暗号 Nonce が生成され、CSP ヘッダーで特定された各スクリプトに追加されます。</span><span class="sxs-lookup"><span data-stu-id="cd69b-133">A unique cryptographic nonce is generated and added to each script specified in the CSP header.</span></span>

<span data-ttu-id="cd69b-134">Nonce を有効にするには、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="cd69b-134">To enable nonce, follow these steps.</span></span>

1. <span data-ttu-id="cd69b-135">サイト ビルダーで、作業しているサイトを選択します。</span><span class="sxs-lookup"><span data-stu-id="cd69b-135">In site builder, select the site you are working on.</span></span>
1. <span data-ttu-id="cd69b-136">**サイト設定** を選択し、**拡張** タブを選択します。</span><span class="sxs-lookup"><span data-stu-id="cd69b-136">Select **Site settings**, and then select the **Extensions** tab.</span></span>
1. <span data-ttu-id="cd69b-137">**コンテンツ セキュリティ ポリシー** タブで、**Nonce の有効化** チェック ボックスを選択します。</span><span class="sxs-lookup"><span data-stu-id="cd69b-137">On the **Content security policy** tab, select the **Enable Nonce** check box.</span></span>

## <a name="csp-directives-in-commerce"></a><span data-ttu-id="cd69b-138">コマースの CSP ディレクティブ</span><span class="sxs-lookup"><span data-stu-id="cd69b-138">CSP directives in Commerce</span></span>

<span data-ttu-id="cd69b-139">次の CSP ディレクティブは、コマース サイトで使用できます。</span><span class="sxs-lookup"><span data-stu-id="cd69b-139">The following CSP directives can be used on Commerce sites.</span></span>

| <span data-ttu-id="cd69b-140">ディレクティブ</span><span class="sxs-lookup"><span data-stu-id="cd69b-140">Directive</span></span>   | <span data-ttu-id="cd69b-141">説明</span><span class="sxs-lookup"><span data-stu-id="cd69b-141">Description</span></span> |
|-------------|-------------|
| <span data-ttu-id="cd69b-142">child-src</span><span class="sxs-lookup"><span data-stu-id="cd69b-142">child-src</span></span>   | <span data-ttu-id="cd69b-143">このディレクティブは、**\<frame\>** および **\<iframe\>** などの要素を使用して読み込まれる、Web ワーカーと入れ子になったブラウジング コンテキストの有効なソースを定義します。</span><span class="sxs-lookup"><span data-stu-id="cd69b-143">This directive defines valid sources of web workers and nested browsing contexts that are loaded by using elements such as **\<frame\>** and **\<iframe\>**.</span></span> |
| <span data-ttu-id="cd69b-144">connect-src</span><span class="sxs-lookup"><span data-stu-id="cd69b-144">connect-src</span></span> | <span data-ttu-id="cd69b-145">このディレクティブは、AJAX 要求を作成できる URLs を定義します。</span><span class="sxs-lookup"><span data-stu-id="cd69b-145">This directive defines the URLs that AJAX requests can be made from.</span></span> |
| <span data-ttu-id="cd69b-146">font-src</span><span class="sxs-lookup"><span data-stu-id="cd69b-146">font-src</span></span>    | <span data-ttu-id="cd69b-147">このディレクティブは、フォントの有効なソースを定義します。</span><span class="sxs-lookup"><span data-stu-id="cd69b-147">This directive defines valid sources of fonts.</span></span> |
| <span data-ttu-id="cd69b-148">frame-ancestors</span><span class="sxs-lookup"><span data-stu-id="cd69b-148">frame-ancestors</span></span> | <span data-ttu-id="cd69b-149">このディレクティブは、**\<frame\>**、**\<iframe\>**、**\<object\>**、**\<embed\>**、または **\<applet\>** 要素を使用してページに埋め込むことができる有効な親を指定します。</span><span class="sxs-lookup"><span data-stu-id="cd69b-149">This directive specifies valid parents that may embed a page using **\<frame\>**, **\<iframe\>**, **\<object\>**, **\<embed\>**, or **\<applet\>** elements.</span></span> <span data-ttu-id="cd69b-150">このディレクティブを「なし」に設定することは、"X-Frame-Options: DENY" ディレクティブ (旧バージョンのブラウザーでもサポートされています) を指定することと似ています。</span><span class="sxs-lookup"><span data-stu-id="cd69b-150">Setting this directive to "none" is similar to specifying the "X-Frame-Options: DENY" directive (which is also supported in older browsers).</span></span> |
| <span data-ttu-id="cd69b-151">frame-src</span><span class="sxs-lookup"><span data-stu-id="cd69b-151">frame-src</span></span>   | <span data-ttu-id="cd69b-152">このディレクティブは、**\<frame\>** および **\<iframe\>** などの要素を使用して読み込まれる、入れ子になったブラウジング コンテキストの有効なソースを定義します。</span><span class="sxs-lookup"><span data-stu-id="cd69b-152">This directive defines valid sources for nested browsing context loading using elements such as **\<frame\>** and **\<iframe\>**.</span></span> |
| <span data-ttu-id="cd69b-153">img-src</span><span class="sxs-lookup"><span data-stu-id="cd69b-153">img-src</span></span>     | <span data-ttu-id="cd69b-154">このディレクティブは、画像の有効なソースを定義します。</span><span class="sxs-lookup"><span data-stu-id="cd69b-154">This directive defines valid sources of images.</span></span> |
| <span data-ttu-id="cd69b-155">media-src</span><span class="sxs-lookup"><span data-stu-id="cd69b-155">media-src</span></span>   | <span data-ttu-id="cd69b-156">このディレクティブは、HTML5 **\<audio\>** および **\<video\>** 要素などのオーディオおよびビデオの有効なソースを定義します。</span><span class="sxs-lookup"><span data-stu-id="cd69b-156">This directive defines valid sources of audio and video, such as HTML5 **\<audio\>** and **\<video\>** elements.</span></span> |
| <span data-ttu-id="cd69b-157">object-src</span><span class="sxs-lookup"><span data-stu-id="cd69b-157">object-src</span></span>  | <span data-ttu-id="cd69b-158">このディレクティブは、**\<object\>**、**\<embed\>**、および **\<applet\>** 要素などのプラグインの有効なソースを定義します。</span><span class="sxs-lookup"><span data-stu-id="cd69b-158">This directive defines valid sources of plug-ins, such as **\<object\>**, **\<embed\>**, and **\<applet\>** elements.</span></span> |
| <span data-ttu-id="cd69b-159">report-uri</span><span class="sxs-lookup"><span data-stu-id="cd69b-159">report-uri</span></span>  | <span data-ttu-id="cd69b-160">このディレクティブは、ブラウザーが CSP 違反レポートを転記する URI を定義します。</span><span class="sxs-lookup"><span data-stu-id="cd69b-160">This directive defines URI(s) that the browser will post CSP violation reports to.</span></span> <span data-ttu-id="cd69b-161">これらの違反レポートは、指定された URI に HTTP POST 要求を通じて送信される JSON ドキュメントで構成されます。</span><span class="sxs-lookup"><span data-stu-id="cd69b-161">These violation reports consist of JSON documents sent via an HTTP POST request to the specified URI.</span></span> |
| <span data-ttu-id="cd69b-162">script-src</span><span class="sxs-lookup"><span data-stu-id="cd69b-162">script-src</span></span>  | <span data-ttu-id="cd69b-163">このディレクティブは、JavaScript の有効なソースを定義します。</span><span class="sxs-lookup"><span data-stu-id="cd69b-163">This directive defines valid sources of JavaScript.</span></span> |
| <span data-ttu-id="cd69b-164">style-src</span><span class="sxs-lookup"><span data-stu-id="cd69b-164">style-src</span></span>   | <span data-ttu-id="cd69b-165">このディレクティブは、stylesheets の有効なソースを定義します。</span><span class="sxs-lookup"><span data-stu-id="cd69b-165">This directive defines valid sources of stylesheets.</span></span> |

### <a name="example-configure-a-csp-directive"></a><span data-ttu-id="cd69b-166">例: CSP ディレクティブのコンフィギュレーション</span><span class="sxs-lookup"><span data-stu-id="cd69b-166">Example: Configure a CSP directive</span></span>

<span data-ttu-id="cd69b-167">次の例の手順は、サイトから外部スクリプトを呼び出すことができるように、CSP ディレクティブを設定する方法を示しています。</span><span class="sxs-lookup"><span data-stu-id="cd69b-167">The following example procedure shows how to configure a CSP directive so that an external script can be called from your site.</span></span>

1. <span data-ttu-id="cd69b-168">サイト ビルダーで、作業しているサイトを選択します。</span><span class="sxs-lookup"><span data-stu-id="cd69b-168">In site builder, select the site you are working on.</span></span>
1. <span data-ttu-id="cd69b-169">**サイト設定** を選択し、**拡張** タブを選択します。</span><span class="sxs-lookup"><span data-stu-id="cd69b-169">Select **Site settings**, and then select the **Extensions** tab.</span></span>
1. <span data-ttu-id="cd69b-170">**コンテンツ セキュリティ ポリシー** タブの、**script-src** で **追加** を選択し、呼び出す外部スクリプトの完全な URL を入力します。</span><span class="sxs-lookup"><span data-stu-id="cd69b-170">On the **Content security policy** tab, under **script-src**, select **Add**, and then enter the full URL of the external script that should be called.</span></span>

    ![Content Security Policy タブの外部スクリプト用 URL](media/content-security-policy.png)

1. <span data-ttu-id="cd69b-172">**保存と公開** を選択します。</span><span class="sxs-lookup"><span data-stu-id="cd69b-172">Select **Save and publish**.</span></span>

## <a name="interpret-and-fix-csp-errors"></a><span data-ttu-id="cd69b-173">CSP エラーの解釈と修正</span><span class="sxs-lookup"><span data-stu-id="cd69b-173">Interpret and fix CSP errors</span></span>

<span data-ttu-id="cd69b-174">最初にサイトの CSP をコンフィギュレーションすると、一部のページがまったく読み込まれないか、意図したとおりに機能しない可能性があります。それは、CSP が外部接続、スクリプト、フォント、およびその他の種類のリソースの読み込みをブロックしているからです。</span><span class="sxs-lookup"><span data-stu-id="cd69b-174">When you first configure CSP for a site, some pages probably won't be loaded at all or won't work as intended, because CSP is blocking external connections, scripts, fonts, and other types of resources from being loaded.</span></span> <span data-ttu-id="cd69b-175">ただし、CSP は不要な要求または不要な要求を修正、調整、およびクリーン アップするために使用できるいくつかの有用なエラーをログに記録します。</span><span class="sxs-lookup"><span data-stu-id="cd69b-175">Fortunately, CSP logs some helpful errors that you can use to fix, tune, and clean up unwanted or unneeded requests.</span></span>

<span data-ttu-id="cd69b-176">次の図では、Web ブラウザーの開発ツールにおける CSP エラーの例を示しています。</span><span class="sxs-lookup"><span data-stu-id="cd69b-176">The following illustration shows an example of CSP errors in a web browser's developer tools.</span></span>

![Web ブラウザーの開発者ツールにおける CSP エラー](media/content-security-policy-errors.png)

<span data-ttu-id="cd69b-178">この例では、次の 2 つの CSP エラーがあります。</span><span class="sxs-lookup"><span data-stu-id="cd69b-178">There are two CSP errors in this example:</span></span>

- <span data-ttu-id="cd69b-179">**Eval** 関数は、任意の JavaScript を実行する可能性があるため、既定ではブロックされています。</span><span class="sxs-lookup"><span data-stu-id="cd69b-179">The **Eval** function is blocked by default, because it can cause arbitrary JavaScript execution.</span></span> <span data-ttu-id="cd69b-180">この関数を使用するには、**'危険 -eval'** をサイトの **スクリプト -src** ディレクティブに追加します。</span><span class="sxs-lookup"><span data-stu-id="cd69b-180">To allow this function, add **'unsafe-eval'** to your site's **script-src** directive.</span></span> <span data-ttu-id="cd69b-181">単一の引用符が必要です。</span><span class="sxs-lookup"><span data-stu-id="cd69b-181">The single quotation marks are required.</span></span>
- <span data-ttu-id="cd69b-182">外部スタイルシートがブロックされています。</span><span class="sxs-lookup"><span data-stu-id="cd69b-182">The external stylesheet is blocked.</span></span> <span data-ttu-id="cd69b-183">スタイルシートを外部ドメインから読み込むには、URL をサイトの **スタイル -src** ディレクティブに追加します。</span><span class="sxs-lookup"><span data-stu-id="cd69b-183">To allow a stylesheet to be loaded from an external domain, add the URL to your site's **style-src** directive.</span></span>

<span data-ttu-id="cd69b-184">次のスクリーンショットでは、コマースにて **Content Security Policy** タブの固定設定がどのように表示されるか示します。</span><span class="sxs-lookup"><span data-stu-id="cd69b-184">The following screenshot shows what the fixed settings look like on the **Content Security Policy** tab in Commerce.</span></span>

![Content Security Policy タブの固定設定](media/content-security-policy-fixed.png)

## <a name="update-page-mocks-that-use-csp"></a><span data-ttu-id="cd69b-186">CSP を使用するページ モックの更新</span><span class="sxs-lookup"><span data-stu-id="cd69b-186">Update page mocks that use CSP</span></span>

<span data-ttu-id="cd69b-187">開発環境でオンライン SDK を使用してモジュールをテストする場合、ページ モックを使用して CSP を追加することもできます。</span><span class="sxs-lookup"><span data-stu-id="cd69b-187">If you're testing modules by using the online SDK in a development environment, you can also add CSP by using page mocks.</span></span> <span data-ttu-id="cd69b-188">ページ モックでは、トップ レベルの **"appContext"** プロパティを追加するか、または既存のトップレベルの **"appContext"** プロパティに移動して、**"contentSecurityPolicy"** という名前のプロパティを作成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="cd69b-188">In a page mock, you must either add a top-level **"appContext"** property or go to the existing top-level **"appContext"** property, and create a property under it that is named **"contentSecurityPolicy"**.</span></span> <span data-ttu-id="cd69b-189">ここでは、次の例に示すように、ディレクティブのキー / 値ペアをポリシーに追加できます。</span><span class="sxs-lookup"><span data-stu-id="cd69b-189">There, you can add key/value pairs of directives to policies, as shown in the following example.</span></span>

```json
"appContext": {
    "contentSecurityPolicy": {
        "script-src": ["https://www.w3schools.com/js/myScript.js"],
        "font-src": ["https://*.commerce.dynamics.com"]
    }
}
```

> [!NOTE]
> <span data-ttu-id="cd69b-190">ページ モックに CSP ポリシーを追加する場合、ページ モックには、プラットフォームによって提供される既定の CSP ポリシーは含まれません。</span><span class="sxs-lookup"><span data-stu-id="cd69b-190">If you add CSP policies in a page mock, the page mock won't include any of the default CSP policies that are provided by the platform.</span></span>

<span data-ttu-id="cd69b-191">ページ モックで CSP を無効にするには、次のコードを使用します。</span><span class="sxs-lookup"><span data-stu-id="cd69b-191">You can turn off CSP in a page mock by using the following code.</span></span>

```json
"appContext": {
    "contentSecurityPolicy": {
        "disableContentSecurityPolicy": true
    }
}
```

## <a name="additional-resources"></a><span data-ttu-id="cd69b-192">追加リソース</span><span class="sxs-lookup"><span data-stu-id="cd69b-192">Additional resources</span></span>

[<span data-ttu-id="cd69b-193">E コマース ユーザーとロールの管理</span><span class="sxs-lookup"><span data-stu-id="cd69b-193">Manage e-Commerce users and roles</span></span>](manage-ecommerce-users-roles.md)

[<span data-ttu-id="cd69b-194">サイト ページにスクリプト コードを追加してテレメトリをサポートする</span><span class="sxs-lookup"><span data-stu-id="cd69b-194">Add script code to site pages to support telemetry</span></span>](add-telemetry.md)

[<span data-ttu-id="cd69b-195">サイトにおける検索エンジン最適化 (SEO) の考慮事項</span><span class="sxs-lookup"><span data-stu-id="cd69b-195">Search engine optimization (SEO) considerations for your site</span></span>](search-engine-optimization-considerations.md)
