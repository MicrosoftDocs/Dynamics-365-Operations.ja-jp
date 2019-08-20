---
title: サービス認証問題のトラブルシューティング
description: このトピックでは、サービス認証に関する問題を解決するためのヒントをいくつか示します。
author: nimakms
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Developer
ms.reviewer: sericks
ms.search.scope: Operations
ms.custom: 195943
ms.assetid: 0c22fad3-be0a-4111-97c0-2f3fadfd5f6b
ms.search.region: Global
ms.author: nimak
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 7c2edd582d6fdbc554ba2fe4aa7ffb5d9763f55a
ms.sourcegitcommit: 16bfa0fd08feec1647829630401ce62ce2ffa1a4
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/02/2019
ms.locfileid: "1848169"
---
# <a name="troubleshoot-service-authentication-issues"></a><span data-ttu-id="a17c0-103">サービス認証問題のトラブルシューティング</span><span class="sxs-lookup"><span data-stu-id="a17c0-103">Troubleshoot service authentication issues</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="a17c0-104">このトピックでは、サービス認証に関する問題を解決するためのヒントをいくつか示します。</span><span class="sxs-lookup"><span data-stu-id="a17c0-104">This topic provides some tips for troubleshooting issues that involve service authentication.</span></span>

<span data-ttu-id="a17c0-105">サービス認証の問題をトラブルシューティングする場合、もっともよく発生する問題の解決に役立ついくつかの基本的な共通の手順があります。</span><span class="sxs-lookup"><span data-stu-id="a17c0-105">When you troubleshoot service authentication issues, there are a few basic and common procedures that can help resolve the issues that are most often encountered.</span></span> <span data-ttu-id="a17c0-106">また、これらの手順では、認証メカニズムの仕組みを実際に実演します。</span><span class="sxs-lookup"><span data-stu-id="a17c0-106">These procedures also provide a hands-on demonstration of how the authentication mechanism works.</span></span> <span data-ttu-id="a17c0-107">このトピックでは手順を説明し、これまでに生じたいくつかの一般的な問題を一覧表示しています。</span><span class="sxs-lookup"><span data-stu-id="a17c0-107">This topic includes instructions and also lists a few common issues that users have encountered so far.</span></span>

## <a name="inspect-the-jwt"></a><span data-ttu-id="a17c0-108">JWT を検査します。</span><span class="sxs-lookup"><span data-stu-id="a17c0-108">Inspect the JWT</span></span>
### <a name="capture-the-jwt-from-an-http-request"></a><span data-ttu-id="a17c0-109">HTTP 要求から JWT をキャプチャします。</span><span class="sxs-lookup"><span data-stu-id="a17c0-109">Capture the JWT from an HTTP request</span></span>

1. <span data-ttu-id="a17c0-110">Fiddler を <https://www.telerik.com/fiddler> からダウンロードします。</span><span class="sxs-lookup"><span data-stu-id="a17c0-110">Download Fiddler from <https://www.telerik.com/fiddler>.</span></span>
2. <span data-ttu-id="a17c0-111">クライアントから HTTPS トラフィックを監視するには、HTTPS キャプチャを設定します。</span><span class="sxs-lookup"><span data-stu-id="a17c0-111">Set up HTTPS capture to watch the HTTPS traffic from the client.</span></span>
3. <span data-ttu-id="a17c0-112">未処理認証 (OAuth) JSON Web トークン (JWT) を検索します。</span><span class="sxs-lookup"><span data-stu-id="a17c0-112">Find the Open Authorization (OAuth) JSON Web Token (JWT).</span></span> <span data-ttu-id="a17c0-113">これは、「ベアラー」セグメントのない HTTP「認証」ヘッダーの値です。</span><span class="sxs-lookup"><span data-stu-id="a17c0-113">It's the value of the HTTP "Authorization" header without the "bearer" segment.</span></span>

### <a name="use-a-deserializer-tool-to-look-at-the-token-contents"></a><span data-ttu-id="a17c0-114">逆シリアル化ツールを使用してトークンの内容を確認</span><span class="sxs-lookup"><span data-stu-id="a17c0-114">Use a deserializer tool to look at the token contents</span></span>

1. <span data-ttu-id="a17c0-115"><https://jwt.io> に移動し、入力パネルに JWT を貼り付けます。</span><span class="sxs-lookup"><span data-stu-id="a17c0-115">Go to <https://jwt.io>, and paste the JWT into the input panel.</span></span>
2. <span data-ttu-id="a17c0-116">名前と値の組でコンテンツを表示します。</span><span class="sxs-lookup"><span data-stu-id="a17c0-116">View the contents in the form of name-value pairs.</span></span> <span data-ttu-id="a17c0-117">次の例を参照してください。</span><span class="sxs-lookup"><span data-stu-id="a17c0-117">See the example that follows.</span></span>
3. <span data-ttu-id="a17c0-118">次の情報が正しいことを確認します。</span><span class="sxs-lookup"><span data-stu-id="a17c0-118">Verify that the following information is correct:</span></span>

    - <span data-ttu-id="a17c0-119">**"aud"** - 値は、Microsoft Azure Active Directory (Azure AD) リソースという概念に対応します。</span><span class="sxs-lookup"><span data-stu-id="a17c0-119">**"aud"** – The value corresponds to the Microsoft Azure Active Directory (Azure AD) resource concept.</span></span> <span data-ttu-id="a17c0-120">「aud」を含む典型的な問題を以下に示します。</span><span class="sxs-lookup"><span data-stu-id="a17c0-120">Here are some typical issues that involve "aud":</span></span>

        - <span data-ttu-id="a17c0-121">JWT の **"aud"** セグメントには、末尾にスラッシュを持つ URI が含まれています。</span><span class="sxs-lookup"><span data-stu-id="a17c0-121">The **"aud"** segment of the JWT contains a URI that has a trailing slash.</span></span>
        - <span data-ttu-id="a17c0-122">JWT の **"aud"** セグメントには、大文字と小文字の間違ったスタイルを使用する URI が含まれています。</span><span class="sxs-lookup"><span data-stu-id="a17c0-122">The **"aud"** segment of the JWT contains a URI that uses an incorrect capitalization style.</span></span> <span data-ttu-id="a17c0-123">URI は、すべて小文字であることが必要です。</span><span class="sxs-lookup"><span data-stu-id="a17c0-123">The URI must be all lowercase.</span></span>

    - <span data-ttu-id="a17c0-124">**"appid"** - 値は Azure AD ネイティブ クライアント アプリ ID (またはサービス アプリ ID) に対応します。</span><span class="sxs-lookup"><span data-stu-id="a17c0-124">**"appid"** – The value corresponds to the Azure AD Native Client App ID (or Service App ID).</span></span>
    - <span data-ttu-id="a17c0-125">**"upn"** - 値はネイティブ クライアント アプリケーションを通じて認証されているユーザーに対応します。</span><span class="sxs-lookup"><span data-stu-id="a17c0-125">**"upn"** – The value corresponds to the user who is being authenticated through a Native Client App.</span></span>

<span data-ttu-id="a17c0-126">次の図は、JWT のコンテンツの例を示します。</span><span class="sxs-lookup"><span data-stu-id="a17c0-126">The following illustration shows an example of the contents of the JWT.</span></span>

<span data-ttu-id="a17c0-127">[![JWT の例](./media/serviceauthenticationtroubleshooting01.png)](./media/serviceauthenticationtroubleshooting01.png)</span><span class="sxs-lookup"><span data-stu-id="a17c0-127">[![Example of a JWT](./media/serviceauthenticationtroubleshooting01.png)](./media/serviceauthenticationtroubleshooting01.png)</span></span>

## <a name="review-the-event-logs"></a><span data-ttu-id="a17c0-128">イベント ログを確認</span><span class="sxs-lookup"><span data-stu-id="a17c0-128">Review the event logs</span></span>
<span data-ttu-id="a17c0-129">また、仮想マシン (VM) に対するアクセス権限がある場合、インスタンス マシンのイベント ログを確認することができます。</span><span class="sxs-lookup"><span data-stu-id="a17c0-129">You can also look at the event logs of the instance machine, if you have access to the virtual machine (VM).</span></span>

1. <span data-ttu-id="a17c0-130">**実行** ウィンドウから **eventvwr** コマンドを実行してイベント ビューアーを起動します。</span><span class="sxs-lookup"><span data-stu-id="a17c0-130">Start Event Viewer by running the **eventvwr** command from the **Run** window.</span></span>
2. <span data-ttu-id="a17c0-131">次のチャンネルに移動します。</span><span class="sxs-lookup"><span data-stu-id="a17c0-131">Go to the following channels:</span></span>

    - <span data-ttu-id="a17c0-132">アプリケーションとサービス ログ &gt; Microsoft &gt; Dynamics &gt; AX-IntegrationServices &gt; Channel:Operational (Microsoft-Dynamics-AX-IntegrationServices/運用)</span><span class="sxs-lookup"><span data-stu-id="a17c0-132">Application and Services Logs &gt; Microsoft &gt; Dynamics &gt; AX-IntegrationServices &gt; Channel:Operational (Microsoft-Dynamics-AX-IntegrationServices/Operational)</span></span>
    - <span data-ttu-id="a17c0-133">アプリケーションとサービス ログ &gt; Microsoft &gt; Dynamics &gt; AX-SystemRuntime &gt; Channel:Operational (Microsoft-Dynamics-AX-SystemRuntime/運用)</span><span class="sxs-lookup"><span data-stu-id="a17c0-133">Application and Services Logs &gt; Microsoft &gt; Dynamics &gt; AX-SystemRuntime &gt; Channel:Operational (Microsoft-Dynamics-AX-SystemRuntime/Operational)</span></span>

## <a name="other-approaches"></a><span data-ttu-id="a17c0-134">その他の方法</span><span class="sxs-lookup"><span data-stu-id="a17c0-134">Other approaches</span></span>
- <span data-ttu-id="a17c0-135">OAuth がコンフィギュレーションされる方法の詳細については、[サービス エンドポイント](services-home-page.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="a17c0-135">For more information about how OAuth is configured, see [Service endpoints](services-home-page.md).</span></span>
- <span data-ttu-id="a17c0-136">また、自分自身のクライアント コードを使用して、並列でサービスの呼び出しを試みることができます。</span><span class="sxs-lookup"><span data-stu-id="a17c0-136">You can also try to call the service in parallel by using your own client code.</span></span> <span data-ttu-id="a17c0-137">公開されたサンプル コードは <https://github.com/Microsoft/Dynamics-AX-Integration> で入手できます。</span><span class="sxs-lookup"><span data-stu-id="a17c0-137">The sample code that we published is available at <https://github.com/Microsoft/Dynamics-AX-Integration>.</span></span>
- <span data-ttu-id="a17c0-138">2 番目のメソッドが動作する場合は、それぞれのメソッドで JWT を比較できます。</span><span class="sxs-lookup"><span data-stu-id="a17c0-138">If the second method works, you can compare the JWTs from each method.</span></span>

## <a name="known-issues"></a><span data-ttu-id="a17c0-139">既知の問題</span><span class="sxs-lookup"><span data-stu-id="a17c0-139">Known issues</span></span>
### <a name="aadsts65001-the-user-or-administrator-hasnt-consented-to-use-the-application"></a><span data-ttu-id="a17c0-140">AADSTS65001: ユーザーまたは管理者がアプリケーションの使用に同意していない</span><span class="sxs-lookup"><span data-stu-id="a17c0-140">AADSTS65001: The user or administrator hasn't consented to use the application</span></span>

- <span data-ttu-id="a17c0-141">JWT の **"aud"** セグメントには、末尾にスラッシュを持つ URI が含まれている可能性があります。</span><span class="sxs-lookup"><span data-stu-id="a17c0-141">The **"aud"** segment of the JWT might contain a URI that has a trailing slash.</span></span> <span data-ttu-id="a17c0-142">スラッシュを削除する必要があります。</span><span class="sxs-lookup"><span data-stu-id="a17c0-142">The slash must be removed.</span></span>
- <span data-ttu-id="a17c0-143">JWT の **"aud"** セグメントには、大文字と小文字の間違ったスタイルを使用する URI が含まれている可能性があります。</span><span class="sxs-lookup"><span data-stu-id="a17c0-143">The **"aud"** segment of the JWT might contain a URI that uses an incorrect capitalization style.</span></span> <span data-ttu-id="a17c0-144">URI は、すべて小文字であることが必要です。</span><span class="sxs-lookup"><span data-stu-id="a17c0-144">The URI must be all lowercase.</span></span>
