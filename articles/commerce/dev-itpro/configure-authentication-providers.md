---
title: 認証プロバイダーのコンフィギュレーション
description: このトピックでは、新しい OpenID 認証プロバイダを構成するためのプロセスの概要を示します。
author: kfend
ms.date: 11/14/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Developer, IT Pro
ms.reviewer: rhaertle
ms.custom: 31241
ms.assetid: fef883f3-981a-4bba-9a41-d9dde63b0cd0
ms.search.region: Global
ms.author: meeram
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: 4477499686bf37610e1c44e9db5e11e4d61eb3f2
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/31/2021
ms.locfileid: "5791217"
---
# <a name="configure-authentication-providers"></a><span data-ttu-id="51848-103">認証プロバイダーのコンフィギュレーション</span><span class="sxs-lookup"><span data-stu-id="51848-103">Configure authentication providers</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="51848-104">このトピックでは、新しい OpenID 認証プロバイダを構成するためのプロセスの概要を示します。</span><span class="sxs-lookup"><span data-stu-id="51848-104">This topic provides an overview of the process for configuring a new OpenID authentication provider.</span></span>

<span data-ttu-id="51848-105">E コマース プラットフォームは、認証のためのメカニズムとして業界標準の [OpenID Connect](https://openid.net/connect/) を使用します。</span><span class="sxs-lookup"><span data-stu-id="51848-105">The E-Commerce platform uses industry-standard [OpenID Connect](https://openid.net/connect/) as the mechanism for authentication.</span></span> <span data-ttu-id="51848-106">この記事では、オンライン ストアで使用される OpenID プロバイダーを登録するために使用するページについて説明します。</span><span class="sxs-lookup"><span data-stu-id="51848-106">This article covers the pages that you use to register the OpenID providers that are used in an online store.</span></span> <span data-ttu-id="51848-107">Commerce Scale Unit は、認証された顧客をサポートするメカニズムとして OpenID Connect を使用します。</span><span class="sxs-lookup"><span data-stu-id="51848-107">Commerce Scale Unit uses OpenID Connect as the mechanism to support authenticated customers.</span></span> <span data-ttu-id="51848-108">OpenID 接続は、シンプルで発展した ID プロバイダーとして、OAuth 2.0 に加えて広く受け入れられている標準です。</span><span class="sxs-lookup"><span data-stu-id="51848-108">OpenID Connect is a universally accepted standard that acts as simple and evolved identity provider on top of OAuth 2.0.</span></span> <span data-ttu-id="51848-109">Commerce Scale Unit は、Microsoft Azure アクセス制御サービスを通じてすぐに使用できる OpenID プロバイダー、およびその他の個別に使用可能なプロバイダーの両方と統合することができます。</span><span class="sxs-lookup"><span data-stu-id="51848-109">Commerce Scale Unit can be integrated with both ready-to-use OpenID providers through the Microsoft Azure Access Control service and other independently available providers.</span></span> <span data-ttu-id="51848-110">さらに、OpenID 接続をサポートするカスタム プロバイダーを統合および登録できます。</span><span class="sxs-lookup"><span data-stu-id="51848-110">In addition, any custom providers that support OpenID connect can be integrated and registered.</span></span> <span data-ttu-id="51848-111">次の図は、Commerce Scale Unit と電子商取引のフロント エンド サーバーの間で発生し、後続の呼び出しで認証トークンを渡すステップ バイ ステップのハンドシェイクを示しています。</span><span class="sxs-lookup"><span data-stu-id="51848-111">The following illustration shows the step-by-step handshake that occurs between the Commerce Scale Unit and the E-Commerce front-end server to pass the authentication token for subsequent calls.</span></span> 

<span data-ttu-id="51848-112">[![OpenId](./media/openid-1024x540.png)](./media/openid.png)</span><span class="sxs-lookup"><span data-stu-id="51848-112">[![OpenId](./media/openid-1024x540.png)](./media/openid.png)</span></span> 

<span data-ttu-id="51848-113">Commerce Scale Unit で使用できるようにするため、OpenID プロバイダーを登録するプロセスのチュートリアルを次に示します。</span><span class="sxs-lookup"><span data-stu-id="51848-113">Here is a walkthrough of the process for registering OpenID providers so that they can be used in Commerce Scale Unit.</span></span>

1.  <span data-ttu-id="51848-114">Retail and Commerce IT ワークスペースから、**コマース共有パラメーター** &gt; **OpenID プロバイダー** に移動します。</span><span class="sxs-lookup"><span data-stu-id="51848-114">From the Retail and Commerce IT workspace, go to **Commerce shared parameters** &gt; **OpenID providers**.</span></span> <span data-ttu-id="51848-115">**OpenID プロバイダー** ページを使用すると追加プロバイダーを登録することができます。</span><span class="sxs-lookup"><span data-stu-id="51848-115">You can use the **OpenID providers** page to register additional providers.</span></span> <span data-ttu-id="51848-116">サポートする各プロバイダーについては、OpenID プロバイダーの詳細および依存する関係者の詳細を入力します。</span><span class="sxs-lookup"><span data-stu-id="51848-116">For every provider that you support, enter the details of the OpenID provider and the details of the relying parties.</span></span> <span data-ttu-id="51848-117">Commerce Scale Unit は、この情報を使用し、認証トークンを要求して後続の呼び出しに使用します。</span><span class="sxs-lookup"><span data-stu-id="51848-117">Commerce Scale Unit uses this information to request and use an authentication token for subsequent calls.</span></span>
2.  <span data-ttu-id="51848-118">配送スケジュール 1110 を実行します。</span><span class="sxs-lookup"><span data-stu-id="51848-118">Run distribution schedule 1110.</span></span>
3.  <span data-ttu-id="51848-119">テスト オンライン ストアについては、次の例に示すように、正しいリダイレクト URL とドメインを指定できるように web.config ファイルを編集します。</span><span class="sxs-lookup"><span data-stu-id="51848-119">For the test online store, edit the web.config file so that it specifies the correct redirect URL and domain, as shown in the following example.</span></span> <span data-ttu-id="51848-120">第三者のオンライン ストアを使用している場合、この情報を必要に応じて保存できます。</span><span class="sxs-lookup"><span data-stu-id="51848-120">If you're using a third-party online store, this information can be stored as required.</span></span>

    ```xml
    redirectUrl=https://usnconeboxax1ecom.cloud.onebox.dynamics.com/en/Pages/OauthV2Redirect/OauthV2Redirect.aspx
    ```


[!INCLUDE[footer-include](../../includes/footer-banner.md)]