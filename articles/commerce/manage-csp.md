---
title: Content Security Policy (CSP) の管理
description: このトピックでは、Microsoft Dynamics 365 Commerceの コンテンツ セキュリティ ポリシー (CSP) を管理する方法について説明します。
author: samjarawan
ms.date: 11/13/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Developer
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: samjar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 530b0656af60a904746f3222390eb346dcf12959
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/31/2021
ms.locfileid: "5801905"
---
# <a name="manage-content-security-policy-csp"></a><span data-ttu-id="da57e-103">コンテンツ セキュリティ ポリシー (CSP) の管理</span><span class="sxs-lookup"><span data-stu-id="da57e-103">Manage Content Security Policy (CSP)</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="da57e-104">このトピックでは、Microsoft Dynamics 365 Commerceの コンテンツ セキュリティ ポリシー (CSP) を管理する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="da57e-104">This topic describes how to manage Content Security Policy (CSP) in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="da57e-105">CSP は、特定タイプの Web 攻撃の検出と軽減に役立つ追加のセキュリティ レベルです。</span><span class="sxs-lookup"><span data-stu-id="da57e-105">CSP is an additional layer of security that helps detect and mitigate some types of web attacks.</span></span> <span data-ttu-id="da57e-106">これらの攻撃の目的は、データの盗用からサイトの変造やマルウェアの配布まで多岐に指定できます。</span><span class="sxs-lookup"><span data-stu-id="da57e-106">The purpose of these attacks can range from data theft, to site defacement, to the distribution of malware.</span></span> <span data-ttu-id="da57e-107">CSP は、サイトページに読み込むことができるリソースを制御するのに役立つ、広範なポリシー ディレクティブのセットを提供します。</span><span class="sxs-lookup"><span data-stu-id="da57e-107">CSP provides an extensive set of policy directives that help you control the resources that a site page is allowed to load.</span></span> <span data-ttu-id="da57e-108">各ディレクティブは、特定のタイプのリソースに対する制限を定義します。</span><span class="sxs-lookup"><span data-stu-id="da57e-108">Each directive defines the restrictions for a specific type of resource.</span></span>

<span data-ttu-id="da57e-109">電子商取引サイトの CSP を有効にすると、接続、スクリプト、フォント、および未知または悪意のあるソースから発生したその他の種類のリソースをブロックすることによって、セキュリティを強化できます。</span><span class="sxs-lookup"><span data-stu-id="da57e-109">When CSP is turned on for an e-Commerce site, it helps enhance security by blocking connections, scripts, fonts, and other types of resources that originate from unknown or malicious sources.</span></span> <span data-ttu-id="da57e-110">Dynamics 365 Commerce では、CSP が既定で有効になります。</span><span class="sxs-lookup"><span data-stu-id="da57e-110">In Dynamics 365 Commerce, CSP is turned on by default.</span></span> <span data-ttu-id="da57e-111">ただし、ほとんどのサイトでは、追加のコンフィギュレーションが必要となる場合があります。</span><span class="sxs-lookup"><span data-stu-id="da57e-111">However, it will likely require additional configuration for most sites.</span></span> <span data-ttu-id="da57e-112">Dynamics 365 Commerce オンライン ソフトウェア開発キット (SDK) では、スタイル、スクリプト、およびアプリケーション プログラミング インターフェイス (API) の呼び出し元で許可されたソースの URLs における既定リストを提供します。</span><span class="sxs-lookup"><span data-stu-id="da57e-112">The Dynamics 365 Commerce online software development kit (SDK) provides a default list of allowed source URLs that style, script, and application programming interface (API) calls can be made from.</span></span> <span data-ttu-id="da57e-113">サイトビルダー ツールの **拡張** タブで、このリストを編集できます。</span><span class="sxs-lookup"><span data-stu-id="da57e-113">You can edit this list on the **Extensions** tab in the site builder tool.</span></span>

<span data-ttu-id="da57e-114">CSP の詳細については、[Content Security Policy Reference](https://content-security-policy.com/) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="da57e-114">For more information about CSP, see [Content Security Policy Reference](https://content-security-policy.com/).</span></span>

## <a name="csp-settings"></a><span data-ttu-id="da57e-115">CSP 設定</span><span class="sxs-lookup"><span data-stu-id="da57e-115">CSP settings</span></span>

### <a name="turn-off-csp-for-a-site"></a><span data-ttu-id="da57e-116">サイトの CSP を無効</span><span class="sxs-lookup"><span data-stu-id="da57e-116">Turn off CSP for a site</span></span>

<span data-ttu-id="da57e-117">CSP がサイトにポリシーが適用しないようにするには、サイト ビルダーのそのサイトに対してポリシーを無効にできます。</span><span class="sxs-lookup"><span data-stu-id="da57e-117">To prevent CSP from applying policies to your site, you can turn it off for that site in site builder.</span></span>

<span data-ttu-id="da57e-118">サイトの CSP を無効にするには、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="da57e-118">To turn off CSP for a site, follow these steps.</span></span>

1. <span data-ttu-id="da57e-119">サイト ビルダーで、作業しているサイトを選択します。</span><span class="sxs-lookup"><span data-stu-id="da57e-119">In site builder, select the site you are working on.</span></span>
1. <span data-ttu-id="da57e-120">**サイト設定** を選択し、**拡張** タブを選択します。</span><span class="sxs-lookup"><span data-stu-id="da57e-120">Select **Site settings**, and then select the **Extensions** tab.</span></span>
1. <span data-ttu-id="da57e-121">**コンテンツ セキュリティ ポリシー** タブで、**コンテンツ セキュリティ ポリシーを無効にする** チェック ボックスを選択します。</span><span class="sxs-lookup"><span data-stu-id="da57e-121">On the **Content security policy** tab, select the **Disable content security policy** check box.</span></span>

    ![Content Security Policy タブで、コンテンツ セキュリティ ポリシーを無効にする](media/content-security-policy-disable.png)

1. <span data-ttu-id="da57e-123">**保存と公開** を選択します。</span><span class="sxs-lookup"><span data-stu-id="da57e-123">Select **Save and publish**.</span></span>

### <a name="enable-report-only-mode"></a><span data-ttu-id="da57e-124">レポートのみモードの有効化</span><span class="sxs-lookup"><span data-stu-id="da57e-124">Enable report only mode</span></span>

<span data-ttu-id="da57e-125">CSP が有効になっている場合、コンテンツ セキュリティ ポリシーは適用されませんが、すべての違反がレポート URI ディレクティブで指定された URI に報告されます。</span><span class="sxs-lookup"><span data-stu-id="da57e-125">If CSP is enabled, content security policy will not be enforced, but any violations will be reported to URIs specified by the report-uri directive.</span></span>

<span data-ttu-id="da57e-126">レポートのみのモードを有効化するには、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="da57e-126">To enable report only mode, follow these steps.</span></span>

1. <span data-ttu-id="da57e-127">サイト ビルダーで、作業しているサイトを選択します。</span><span class="sxs-lookup"><span data-stu-id="da57e-127">In site builder, select the site you are working on.</span></span>
1. <span data-ttu-id="da57e-128">**サイト設定** を選択し、**拡張** タブを選択します。</span><span class="sxs-lookup"><span data-stu-id="da57e-128">Select **Site settings**, and then select the **Extensions** tab.</span></span>
1. <span data-ttu-id="da57e-129">**コンテンツ セキュリティ ポリシー** タブで、**レポートのみのモードの有効化** チェック ボックスを選択します。</span><span class="sxs-lookup"><span data-stu-id="da57e-129">On the **Content security policy** tab, select the **Enable report only mode** check box.</span></span>

### <a name="enable-nonce"></a><span data-ttu-id="da57e-130">Nonce を有効にする</span><span class="sxs-lookup"><span data-stu-id="da57e-130">Enable nonce</span></span>

<span data-ttu-id="da57e-131">Nonce (1 回だけ使用する番号) を有効にすると、[インライン スクリプト モジュール](e-commerce-extensibility/script-injector.md) 内で特定されたものを除き、すべてのインライン スクリプトの実行がブロックされます。</span><span class="sxs-lookup"><span data-stu-id="da57e-131">Enabling nonce (number used once) will block the execution of all inline scripts except those specified within the [inline script](e-commerce-extensibility/script-injector.md) module.</span></span> <span data-ttu-id="da57e-132">一意の暗号 Nonce が生成され、CSP ヘッダーで特定された各スクリプトに追加されます。</span><span class="sxs-lookup"><span data-stu-id="da57e-132">A unique cryptographic nonce is generated and added to each script specified in the CSP header.</span></span>

<span data-ttu-id="da57e-133">Nonce を有効にするには、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="da57e-133">To enable nonce, follow these steps.</span></span>

1. <span data-ttu-id="da57e-134">サイト ビルダーで、作業しているサイトを選択します。</span><span class="sxs-lookup"><span data-stu-id="da57e-134">In site builder, select the site you are working on.</span></span>
1. <span data-ttu-id="da57e-135">**サイト設定** を選択し、**拡張** タブを選択します。</span><span class="sxs-lookup"><span data-stu-id="da57e-135">Select **Site settings**, and then select the **Extensions** tab.</span></span>
1. <span data-ttu-id="da57e-136">**コンテンツ セキュリティ ポリシー** タブで、**Nonce の有効化** チェック ボックスを選択します。</span><span class="sxs-lookup"><span data-stu-id="da57e-136">On the **Content security policy** tab, select the **Enable Nonce** check box.</span></span>

## <a name="csp-directives-in-commerce"></a><span data-ttu-id="da57e-137">コマースの CSP ディレクティブ</span><span class="sxs-lookup"><span data-stu-id="da57e-137">CSP directives in Commerce</span></span>

<span data-ttu-id="da57e-138">次の CSP ディレクティブは、コマース サイトで使用できます。</span><span class="sxs-lookup"><span data-stu-id="da57e-138">The following CSP directives can be used on Commerce sites.</span></span>

| <span data-ttu-id="da57e-139">ディレクティブ</span><span class="sxs-lookup"><span data-stu-id="da57e-139">Directive</span></span>   | <span data-ttu-id="da57e-140">説明</span><span class="sxs-lookup"><span data-stu-id="da57e-140">Description</span></span> |
|-------------|-------------|
| <span data-ttu-id="da57e-141">child-src</span><span class="sxs-lookup"><span data-stu-id="da57e-141">child-src</span></span>   | <span data-ttu-id="da57e-142">このディレクティブは、**\<frame\>** および **\<iframe\>** などの要素を使用して読み込まれる、Web ワーカーと入れ子になったブラウジング コンテキストの有効なソースを定義します。</span><span class="sxs-lookup"><span data-stu-id="da57e-142">This directive defines valid sources of web workers and nested browsing contexts that are loaded by using elements such as **\<frame\>** and **\<iframe\>**.</span></span> |
| <span data-ttu-id="da57e-143">connect-src</span><span class="sxs-lookup"><span data-stu-id="da57e-143">connect-src</span></span> | <span data-ttu-id="da57e-144">このディレクティブは、AJAX 要求を作成できる URLs を定義します。</span><span class="sxs-lookup"><span data-stu-id="da57e-144">This directive defines the URLs that AJAX requests can be made from.</span></span> |
| <span data-ttu-id="da57e-145">font-src</span><span class="sxs-lookup"><span data-stu-id="da57e-145">font-src</span></span>    | <span data-ttu-id="da57e-146">このディレクティブは、フォントの有効なソースを定義します。</span><span class="sxs-lookup"><span data-stu-id="da57e-146">This directive defines valid sources of fonts.</span></span> |
| <span data-ttu-id="da57e-147">frame-ancestors</span><span class="sxs-lookup"><span data-stu-id="da57e-147">frame-ancestors</span></span> | <span data-ttu-id="da57e-148">このディレクティブは、**\<frame\>**、**\<iframe\>**、**\<object\>**、**\<embed\>**、または **\<applet\>** 要素を使用してページに埋め込むことができる有効な親を指定します。</span><span class="sxs-lookup"><span data-stu-id="da57e-148">This directive specifies valid parents that may embed a page using **\<frame\>**, **\<iframe\>**, **\<object\>**, **\<embed\>**, or **\<applet\>** elements.</span></span> <span data-ttu-id="da57e-149">このディレクティブを「なし」に設定することは、"X-Frame-Options: DENY" ディレクティブ (旧バージョンのブラウザーでもサポートされています) を指定することと似ています。</span><span class="sxs-lookup"><span data-stu-id="da57e-149">Setting this directive to "none" is similar to specifying the "X-Frame-Options: DENY" directive (which is also supported in older browsers).</span></span> |
| <span data-ttu-id="da57e-150">frame-src</span><span class="sxs-lookup"><span data-stu-id="da57e-150">frame-src</span></span>   | <span data-ttu-id="da57e-151">このディレクティブは、**\<frame\>** および **\<iframe\>** などの要素を使用して読み込まれる、入れ子になったブラウジング コンテキストの有効なソースを定義します。</span><span class="sxs-lookup"><span data-stu-id="da57e-151">This directive defines valid sources for nested browsing context loading using elements such as **\<frame\>** and **\<iframe\>**.</span></span> |
| <span data-ttu-id="da57e-152">img-src</span><span class="sxs-lookup"><span data-stu-id="da57e-152">img-src</span></span>     | <span data-ttu-id="da57e-153">このディレクティブは、画像の有効なソースを定義します。</span><span class="sxs-lookup"><span data-stu-id="da57e-153">This directive defines valid sources of images.</span></span> |
| <span data-ttu-id="da57e-154">media-src</span><span class="sxs-lookup"><span data-stu-id="da57e-154">media-src</span></span>   | <span data-ttu-id="da57e-155">このディレクティブは、HTML5 **\<audio\>** および **\<video\>** 要素などのオーディオおよびビデオの有効なソースを定義します。</span><span class="sxs-lookup"><span data-stu-id="da57e-155">This directive defines valid sources of audio and video, such as HTML5 **\<audio\>** and **\<video\>** elements.</span></span> |
| <span data-ttu-id="da57e-156">object-src</span><span class="sxs-lookup"><span data-stu-id="da57e-156">object-src</span></span>  | <span data-ttu-id="da57e-157">このディレクティブは、**\<object\>**、**\<embed\>**、および **\<applet\>** 要素などのプラグインの有効なソースを定義します。</span><span class="sxs-lookup"><span data-stu-id="da57e-157">This directive defines valid sources of plug-ins, such as **\<object\>**, **\<embed\>**, and **\<applet\>** elements.</span></span> |
| <span data-ttu-id="da57e-158">report-uri</span><span class="sxs-lookup"><span data-stu-id="da57e-158">report-uri</span></span>  | <span data-ttu-id="da57e-159">このディレクティブは、ブラウザーが CSP 違反レポートを転記する URI を定義します。</span><span class="sxs-lookup"><span data-stu-id="da57e-159">This directive defines URI(s) that the browser will post CSP violation reports to.</span></span> <span data-ttu-id="da57e-160">これらの違反レポートは、指定された URI に HTTP POST 要求を通じて送信される JSON ドキュメントで構成されます。</span><span class="sxs-lookup"><span data-stu-id="da57e-160">These violation reports consist of JSON documents sent via an HTTP POST request to the specified URI.</span></span> |
| <span data-ttu-id="da57e-161">script-src</span><span class="sxs-lookup"><span data-stu-id="da57e-161">script-src</span></span>  | <span data-ttu-id="da57e-162">このディレクティブは、JavaScript の有効なソースを定義します。</span><span class="sxs-lookup"><span data-stu-id="da57e-162">This directive defines valid sources of JavaScript.</span></span> |
| <span data-ttu-id="da57e-163">style-src</span><span class="sxs-lookup"><span data-stu-id="da57e-163">style-src</span></span>   | <span data-ttu-id="da57e-164">このディレクティブは、stylesheets の有効なソースを定義します。</span><span class="sxs-lookup"><span data-stu-id="da57e-164">This directive defines valid sources of stylesheets.</span></span> |

### <a name="example-configure-a-csp-directive"></a><span data-ttu-id="da57e-165">例: CSP ディレクティブのコンフィギュレーション</span><span class="sxs-lookup"><span data-stu-id="da57e-165">Example: Configure a CSP directive</span></span>

<span data-ttu-id="da57e-166">次の例の手順は、サイトから外部スクリプトを呼び出すことができるように、CSP ディレクティブを設定する方法を示しています。</span><span class="sxs-lookup"><span data-stu-id="da57e-166">The following example procedure shows how to configure a CSP directive so that an external script can be called from your site.</span></span>

1. <span data-ttu-id="da57e-167">サイト ビルダーで、作業しているサイトを選択します。</span><span class="sxs-lookup"><span data-stu-id="da57e-167">In site builder, select the site you are working on.</span></span>
1. <span data-ttu-id="da57e-168">**サイト設定** を選択し、**拡張** タブを選択します。</span><span class="sxs-lookup"><span data-stu-id="da57e-168">Select **Site settings**, and then select the **Extensions** tab.</span></span>
1. <span data-ttu-id="da57e-169">**コンテンツ セキュリティ ポリシー** タブの、**script-src** で **追加** を選択し、呼び出す外部スクリプトの完全な URL を入力します。</span><span class="sxs-lookup"><span data-stu-id="da57e-169">On the **Content security policy** tab, under **script-src**, select **Add**, and then enter the full URL of the external script that should be called.</span></span>

    ![Content Security Policy タブの外部スクリプト用 URL](media/content-security-policy.png)

1. <span data-ttu-id="da57e-171">**保存と公開** を選択します。</span><span class="sxs-lookup"><span data-stu-id="da57e-171">Select **Save and publish**.</span></span>

## <a name="interpret-and-fix-csp-errors"></a><span data-ttu-id="da57e-172">CSP エラーの解釈と修正</span><span class="sxs-lookup"><span data-stu-id="da57e-172">Interpret and fix CSP errors</span></span>

<span data-ttu-id="da57e-173">最初にサイトの CSP をコンフィギュレーションすると、一部のページがまったく読み込まれないか、意図したとおりに機能しない可能性があります。それは、CSP が外部接続、スクリプト、フォント、およびその他の種類のリソースの読み込みをブロックしているからです。</span><span class="sxs-lookup"><span data-stu-id="da57e-173">When you first configure CSP for a site, some pages probably won't be loaded at all or won't work as intended, because CSP is blocking external connections, scripts, fonts, and other types of resources from being loaded.</span></span> <span data-ttu-id="da57e-174">ただし、CSP は不要な要求または不要な要求を修正、調整、およびクリーン アップするために使用できるいくつかの有用なエラーをログに記録します。</span><span class="sxs-lookup"><span data-stu-id="da57e-174">Fortunately, CSP logs some helpful errors that you can use to fix, tune, and clean up unwanted or unneeded requests.</span></span>

<span data-ttu-id="da57e-175">次の図では、Web ブラウザーの開発ツールにおける CSP エラーの例を示しています。</span><span class="sxs-lookup"><span data-stu-id="da57e-175">The following illustration shows an example of CSP errors in a web browser's developer tools.</span></span>

![Web ブラウザーの開発者ツールにおける CSP エラー](media/content-security-policy-errors.png)

<span data-ttu-id="da57e-177">この例では、次の 2 つの CSP エラーがあります。</span><span class="sxs-lookup"><span data-stu-id="da57e-177">There are two CSP errors in this example:</span></span>

- <span data-ttu-id="da57e-178">**Eval** 関数は、任意の JavaScript を実行する可能性があるため、既定ではブロックされています。</span><span class="sxs-lookup"><span data-stu-id="da57e-178">The **Eval** function is blocked by default, because it can cause arbitrary JavaScript execution.</span></span> <span data-ttu-id="da57e-179">この関数を使用するには、**'危険 -eval'** をサイトの **スクリプト -src** ディレクティブに追加します。</span><span class="sxs-lookup"><span data-stu-id="da57e-179">To allow this function, add **'unsafe-eval'** to your site's **script-src** directive.</span></span> <span data-ttu-id="da57e-180">単一の引用符が必要です。</span><span class="sxs-lookup"><span data-stu-id="da57e-180">The single quotation marks are required.</span></span>
- <span data-ttu-id="da57e-181">外部スタイルシートがブロックされています。</span><span class="sxs-lookup"><span data-stu-id="da57e-181">The external stylesheet is blocked.</span></span> <span data-ttu-id="da57e-182">スタイルシートを外部ドメインから読み込むには、URL をサイトの **スタイル -src** ディレクティブに追加します。</span><span class="sxs-lookup"><span data-stu-id="da57e-182">To allow a stylesheet to be loaded from an external domain, add the URL to your site's **style-src** directive.</span></span>

<span data-ttu-id="da57e-183">次のスクリーンショットでは、コマースにて **Content Security Policy** タブの固定設定がどのように表示されるか示します。</span><span class="sxs-lookup"><span data-stu-id="da57e-183">The following screenshot shows what the fixed settings look like on the **Content Security Policy** tab in Commerce.</span></span>

![Content Security Policy タブの固定設定](media/content-security-policy-fixed.png)

## <a name="update-page-mocks-that-use-csp"></a><span data-ttu-id="da57e-185">CSP を使用するページ モックの更新</span><span class="sxs-lookup"><span data-stu-id="da57e-185">Update page mocks that use CSP</span></span>

<span data-ttu-id="da57e-186">開発環境でオンライン SDK を使用してモジュールをテストする場合、ページ モックを使用して CSP を追加することもできます。</span><span class="sxs-lookup"><span data-stu-id="da57e-186">If you're testing modules by using the online SDK in a development environment, you can also add CSP by using page mocks.</span></span> <span data-ttu-id="da57e-187">ページ モックでは、トップ レベルの **"appContext"** プロパティを追加するか、または既存のトップレベルの **"appContext"** プロパティに移動して、**"contentSecurityPolicy"** という名前のプロパティを作成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="da57e-187">In a page mock, you must either add a top-level **"appContext"** property or go to the existing top-level **"appContext"** property, and create a property under it that is named **"contentSecurityPolicy"**.</span></span> <span data-ttu-id="da57e-188">ここでは、次の例に示すように、ディレクティブのキー / 値ペアをポリシーに追加できます。</span><span class="sxs-lookup"><span data-stu-id="da57e-188">There, you can add key/value pairs of directives to policies, as shown in the following example.</span></span>

```json
"appContext": {
    "contentSecurityPolicy": {
        "script-src": ["https://www.w3schools.com/js/myScript.js"],
        "font-src": ["https://*.commerce.dynamics.com"]
    }
}
```

> [!NOTE]
> <span data-ttu-id="da57e-189">ページ モックに CSP ポリシーを追加する場合、ページ モックには、プラットフォームによって提供される既定の CSP ポリシーは含まれません。</span><span class="sxs-lookup"><span data-stu-id="da57e-189">If you add CSP policies in a page mock, the page mock won't include any of the default CSP policies that are provided by the platform.</span></span>

<span data-ttu-id="da57e-190">ページ モックで CSP を無効にするには、次のコードを使用します。</span><span class="sxs-lookup"><span data-stu-id="da57e-190">You can turn off CSP in a page mock by using the following code.</span></span>

```json
"appContext": {
    "contentSecurityPolicy": {
        "disableContentSecurityPolicy": true
    }
}
```

## <a name="additional-resources"></a><span data-ttu-id="da57e-191">追加リソース</span><span class="sxs-lookup"><span data-stu-id="da57e-191">Additional resources</span></span>

[<span data-ttu-id="da57e-192">E コマース ユーザーとロールの管理</span><span class="sxs-lookup"><span data-stu-id="da57e-192">Manage e-Commerce users and roles</span></span>](manage-ecommerce-users-roles.md)

[<span data-ttu-id="da57e-193">サイト ページにスクリプト コードを追加してテレメトリをサポートする</span><span class="sxs-lookup"><span data-stu-id="da57e-193">Add script code to site pages to support telemetry</span></span>](add-telemetry.md)

[<span data-ttu-id="da57e-194">サイトにおける検索エンジン最適化 (SEO) の考慮事項</span><span class="sxs-lookup"><span data-stu-id="da57e-194">Search engine optimization (SEO) considerations for your site</span></span>](search-engine-optimization-considerations.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
