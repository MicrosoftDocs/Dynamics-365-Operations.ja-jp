---
title: E コマース プラットフォーム ソフトウェア開発キット (SDK)
description: このトピックでは、電子商取引プラットフォーム SDK について説明します。
author: mugunthanm
ms.date: 07/09/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Developer
ms.reviewer: rhaertle
ms.custom: 18101
ms.assetid: c0b1740b-1cbb-47c4-94e8-779cde8411af
ms.search.region: Global
ms.author: mumani
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: e209ddc7481201a7445cccc619ae5c83f7d187ed
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/31/2021
ms.locfileid: "5793011"
---
#  <a name="e-commerce-platform-software-development-kit-sdk"></a><span data-ttu-id="0ee62-103">E コマース プラットフォーム ソフトウェア開発キット (SDK)</span><span class="sxs-lookup"><span data-stu-id="0ee62-103">e-Commerce platform software development kit (SDK)</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="0ee62-104">このトピックでは、電子商取引プラットフォーム SDK について説明します。</span><span class="sxs-lookup"><span data-stu-id="0ee62-104">This topic describes the e-Commerce Platform SDK.</span></span> <span data-ttu-id="0ee62-105">E コマース プラットフォーム ソフトウェア開発キット (SDK) は、次のコンポーネントで構成されています。</span><span class="sxs-lookup"><span data-stu-id="0ee62-105">The e-Commerce Platform software development kit (SDK) consists of the following components:</span></span>

-   <span data-ttu-id="0ee62-106">フレームワーク</span><span class="sxs-lookup"><span data-stu-id="0ee62-106">Framework</span></span>
-   <span data-ttu-id="0ee62-107">コントロール</span><span class="sxs-lookup"><span data-stu-id="0ee62-107">Controls</span></span>
-   <span data-ttu-id="0ee62-108">発行 (バージョン 1661 以上でサポートされます: [Retail サーバーでのサービス間認証のサポート](https://community.dynamics.com/ax/b/axforretail/archive/2016/09/24/support-for-service-to-service-authentication-in-retail-server))</span><span class="sxs-lookup"><span data-stu-id="0ee62-108">Publishing (only supported in version 1661 and higher: [Support for Service to Service authentication in Retail Server](https://community.dynamics.com/ax/b/axforretail/archive/2016/09/24/support-for-service-to-service-authentication-in-retail-server))</span></span>
-   <span data-ttu-id="0ee62-109">サンプル ASP.NET Web サイト</span><span class="sxs-lookup"><span data-stu-id="0ee62-109">Sample ASP.NET website</span></span>

## <a name="use-the-sample-aspnet-website"></a><span data-ttu-id="0ee62-110">サンプル ASP.NET Web サイトの使用</span><span class="sxs-lookup"><span data-stu-id="0ee62-110">Use the sample ASP.NET website</span></span>


### <a name="download-the-retail-sdk"></a><span data-ttu-id="0ee62-111">Retail SDK をダウンロード</span><span class="sxs-lookup"><span data-stu-id="0ee62-111">Download the Retail SDK</span></span>

<span data-ttu-id="0ee62-112">Retail SDK は、開発環境と、Retail SDK フォルダーにある修正プログラム パッケージで使用できます。</span><span class="sxs-lookup"><span data-stu-id="0ee62-112">The Retail SDK is available in development environments, and in hotfix packages in a Retail SDK folder.</span></span>

- <span data-ttu-id="0ee62-113">開発インスタンスから SDK を取得すると、構成および使用の準備がすぐに整います。</span><span class="sxs-lookup"><span data-stu-id="0ee62-113">If you get the SDK from a development instance, it is immediately ready for configuration and use.</span></span> <span data-ttu-id="0ee62-114">詳細については、「[アクセス インスタンス](../../dev-itpro/dev-tools/access-instances.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="0ee62-114">For more information, see [Access instances](../../dev-itpro/dev-tools/access-instances.md).</span></span> 
- <span data-ttu-id="0ee62-115">修正プログラムから SDK を取得する場合は、修正プログラムのパッケージでは圧縮フォルダとして含まれています。</span><span class="sxs-lookup"><span data-stu-id="0ee62-115">If you get the SDK from a hotfix, it is included in the hotfix package as a zipped folder.</span></span> <span data-ttu-id="0ee62-116">修正プログラムは累積的であり、その他のすべての修正プログラムが含まれています。</span><span class="sxs-lookup"><span data-stu-id="0ee62-116">Hotfixes are cumulative and include all other fixes.</span></span> 

<span data-ttu-id="0ee62-117">Visual Studio Online などのソース管理システムに SDK を配置することをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="0ee62-117">We recommend that you put the SDK in a source control system such as Visual Studio Online.</span></span>

### <a name="use-the-retail-sdk-to-create-the-sample-aspnet-website"></a><span data-ttu-id="0ee62-118">Retail SDK を使用して、サンプル ASP.NET Web サイトを作成する</span><span class="sxs-lookup"><span data-stu-id="0ee62-118">Use the Retail SDK to create the sample ASP.NET website</span></span>
1.  <span data-ttu-id="0ee62-119">管理者モードで Visual Studio を開きます。</span><span class="sxs-lookup"><span data-stu-id="0ee62-119">Open Visual Studio in Admin mode.</span></span> <span data-ttu-id="0ee62-120">この手順は、inetpub フォルダーにパブリッシュするために必要です。</span><span class="sxs-lookup"><span data-stu-id="0ee62-120">This step is necessary for publishing to the inetpub folder.</span></span>
2.  <span data-ttu-id="0ee62-121">C:\\Microsoft Dynamics AX70\\RetailSdkOnlineStoreOnlineStore.sln を開き、すべてのフレームワーク コンポーネントを含めます。</span><span class="sxs-lookup"><span data-stu-id="0ee62-121">Open C:\\Microsoft Dynamics AX70\\RetailSdkOnlineStoreOnlineStore.sln contains all the framework components.</span></span>
3.  <span data-ttu-id="0ee62-122">サンプルのオンライン ストアは C:\\Microsoft Dynamics AX70\\RetailSdkSampleExtensionsOnlineStore にあります。</span><span class="sxs-lookup"><span data-stu-id="0ee62-122">The sample online store is available at C:\\Microsoft Dynamics AX70\\RetailSdkSampleExtensionsOnlineStore.</span></span>
4.  <span data-ttu-id="0ee62-123">Visual Studio 内から Web ストア フロントをコンパイルし、公開します。</span><span class="sxs-lookup"><span data-stu-id="0ee62-123">Compile and publish the web store front, from within Visual Studio.</span></span>
5.  <span data-ttu-id="0ee62-124">IIS マネージャーから RetailStorefrontWebSite のパスを更新します。</span><span class="sxs-lookup"><span data-stu-id="0ee62-124">Update the path of the RetailStorefrontWebSite from IIS Manager.</span></span>
    -  <span data-ttu-id="0ee62-125">既定の設定によって作成された RetailStorefrontWebSite は C:\\Microsoft Dynamics AX70\\Retail Store Front\\Package を指定することに注意してください。</span><span class="sxs-lookup"><span data-stu-id="0ee62-125">Note that RetailStorefrontWebSite created by the default setup points to C:\\Microsoft Dynamics AX70\\Retail Store Front\\Package.</span></span>
    -  <span data-ttu-id="0ee62-126">ただし、RetailSDK から Web ストアフロントを公開すると、C:\\inetpub\\RetailWeb\\Storefront でファイルがドロップされます。</span><span class="sxs-lookup"><span data-stu-id="0ee62-126">However, the publishing of the web storefront from RetailSDK will drop the files at C:\\inetpub\\RetailWeb\\Storefront.</span></span>
    -  <span data-ttu-id="0ee62-127">したがって、RetailStorefrontWebSite の物理パスは、以前と同じポートで Web ストア フロントにアクセスする「C:\\inetpub\\RetailWeb\\Storefront」にポイントするように更新される必要があります。</span><span class="sxs-lookup"><span data-stu-id="0ee62-127">Hence, the physical path of the RetailStorefrontWebSite must be updated to point to “C:\\inetpub\\RetailWeb\\Storefront” to access web storefront on the same ports as before.</span></span> <span data-ttu-id="0ee62-128">もう 1 つのオプションは、新しい Web サイトを作成し inetpub 場所を指すことです。</span><span class="sxs-lookup"><span data-stu-id="0ee62-128">Another option would be to create a new website and have that point to the inetpub location.</span></span>

6.  <span data-ttu-id="0ee62-129">`http://localhost:55080` を参照、または `https://usnconeboxax1ecom.cloud.onebox.dynamics.com/` にアクセスして、テスト ASP.NET Web サイトを表示します。</span><span class="sxs-lookup"><span data-stu-id="0ee62-129">Browse to `http://localhost:55080` or access `https://usnconeboxax1ecom.cloud.onebox.dynamics.com/` to see a test ASP.NET website.</span></span>

### <a name="enable-anonymous-access"></a><span data-ttu-id="0ee62-130">匿名アクセスの有効化</span><span class="sxs-lookup"><span data-stu-id="0ee62-130">Enable anonymous access</span></span>

<span data-ttu-id="0ee62-131">E コマース Web サイトでは、匿名アクセスが正常に機能するように許可する必要があります。</span><span class="sxs-lookup"><span data-stu-id="0ee62-131">E-Commerce websites must allow anonymous access to work correctly.</span></span> <span data-ttu-id="0ee62-132">アプリケーション設定にある Commerce Scale Unit web.config ファイルに次のキーを追加して、匿名アクセスが有効であることを確認にします。</span><span class="sxs-lookup"><span data-stu-id="0ee62-132">Ensure that anonymous access is enabled by adding the following key in the Commerce Scale Unit web.config file under app settings.</span></span>

`
add key="IsAnonymousEnabled" value="true"
`

### <a name="externally-accessing-the-aspnet-website"></a><span data-ttu-id="0ee62-133">ASP.NET Web サイトに外部からアクセス</span><span class="sxs-lookup"><span data-stu-id="0ee62-133">Externally accessing the ASP.NET website</span></span>

<span data-ttu-id="0ee62-134">これらのいずれかが当てはまる場合は、次の構成の変更が必要になります。</span><span class="sxs-lookup"><span data-stu-id="0ee62-134">The following configuration changes will be required if either of these conditions applies:</span></span>

-   <span data-ttu-id="0ee62-135">E コマース サーバーと同じボックス上にはないブラウザー内から Web ストア フロントにアクセスしています。</span><span class="sxs-lookup"><span data-stu-id="0ee62-135">You are accessing web storefront from within a browser that is not on the same box as the e-Commerce server.</span></span>
-   <span data-ttu-id="0ee62-136">E コマース サーバーおよび Commerce Scale Unit は 2 つの異なるボックス上にあります。</span><span class="sxs-lookup"><span data-stu-id="0ee62-136">The e-Commerce server and Commerce Scale Unit are on two different boxes.</span></span>

<span data-ttu-id="0ee62-137">RetailStorefrontWebSite の web.config ファイル内の "retailServerUrl" を更新する必要があります。</span><span class="sxs-lookup"><span data-stu-id="0ee62-137">You will need to update the “retailServerUrl” inside the web.config file of the RetailStorefrontWebSite.</span></span> <span data-ttu-id="0ee62-138">ローカル ホストの代わりにマシン名を使用するには、次の 2 つのフィールドを更新する必要があります。</span><span class="sxs-lookup"><span data-stu-id="0ee62-138">The following two fields will need to be updated to use the machine name instead of local host:</span></span>

```xml
retailServerUrl=<http://localhost:35080/RetailServer/V1>
<add key="RetailServerRoot" value="<http://localhost:35080/RetailServer/V1>" />
```

<span data-ttu-id="0ee62-139">Web ストア フロントを HTTPS 経由でアクセスする場合は、前述の Url を同等の HTTPS に更新する必要があります。</span><span class="sxs-lookup"><span data-stu-id="0ee62-139">If you are accessing the web storefront over HTTPS, then you will need to update the above URLs to the HTTPS equivalent.</span></span>

### <a name="operating-unit-or-channel-configuration"></a><span data-ttu-id="0ee62-140">作業単位またはチャンネルのコンフィギュレーション</span><span class="sxs-lookup"><span data-stu-id="0ee62-140">Operating unit or channel configuration</span></span>

<span data-ttu-id="0ee62-141">E コマースの Web サイトは、web.configで指定された作業単位数 (チャネル) で動作します。これを変更するには、以下の OU \# を変更します。</span><span class="sxs-lookup"><span data-stu-id="0ee62-141">The e-Commerce website will operate on an operating unit number(channel) specified in the web.config. To change it, change the OU \# below.</span></span> <span data-ttu-id="0ee62-142">Fabrikam はデモ データ内で「077」であることに注意してください。</span><span class="sxs-lookup"><span data-stu-id="0ee62-142">Note that Fabrikam is “077” in the demo data.</span></span> <span data-ttu-id="0ee62-143">RetailStorefrontWebSite の web.config 内の "retailServerUrl" を更新する必要があります。</span><span class="sxs-lookup"><span data-stu-id="0ee62-143">You will need to update the “retailServerUrl” inside web.config of the RetailStorefrontWebSite.</span></span> <span data-ttu-id="0ee62-144">ローカル ホストの代わりにマシン名を使用するには、次の 2 つのフィールドを更新する必要があります。</span><span class="sxs-lookup"><span data-stu-id="0ee62-144">The following two fields will need to be updated to use the machine name instead of local host:</span></span>

```xml
<ecommerceControls productUrlFormat="/Pages/ProductDetails/ProductDetails.aspx?itemId={0}" retailServerUrl="http://localhost:35080/RetailServer/V1" operatingUnitNumber="068">
<add key="OperatingUnitNumber" value="068" />
```

## <a name="configure-authentication-providers"></a><span data-ttu-id="0ee62-145">認証プロバイダーのコンフィギュレーション</span><span class="sxs-lookup"><span data-stu-id="0ee62-145">Configure authentication providers</span></span>
### <a name="authentication-providers-that-you-are-using"></a><span data-ttu-id="0ee62-146">使用している認証プロバイダー</span><span class="sxs-lookup"><span data-stu-id="0ee62-146">Authentication providers that you are using</span></span>

<span data-ttu-id="0ee62-147">E コマース プラットフォームは、認証のためのメカニズムとして OpenID を使用します。</span><span class="sxs-lookup"><span data-stu-id="0ee62-147">The e-Commerce platform uses OpenID as the mechanism for authentication.</span></span> <span data-ttu-id="0ee62-148">以下のテーブルに選択した任意の OpenID プロバイダーを登録することにより、この作業を実行することができます。</span><span class="sxs-lookup"><span data-stu-id="0ee62-148">You can register any OpenID provider of your choice to the tables below to make this work.</span></span> <span data-ttu-id="0ee62-149">必要に応じて、テストにログインすることができます。</span><span class="sxs-lookup"><span data-stu-id="0ee62-149">You can then log in to test as needed.</span></span>

1.  <span data-ttu-id="0ee62-150">web.config ファイルを編集し、次のように変更してください。</span><span class="sxs-lookup"><span data-stu-id="0ee62-150">Edit the web.config file and change it to the following.</span></span>

    ```xml
    redirectUrl=https://usnconeboxax1ecom.cloud.onebox.dynamics.com/en/Pages/OauthV2Redirect/OauthV2Redirect.aspx
    ```
    
    <span data-ttu-id="0ee62-151">後続のステップは、追加プロバイダーを登録する場合にのみ行う必要があります。</span><span class="sxs-lookup"><span data-stu-id="0ee62-151">The subsequent steps should only be done to register additional providers.</span></span>

2.  <span data-ttu-id="0ee62-152">**Retail 共有パラメーター -&gt; ID プロバイダーを開く** フォームは、追加プロバイダーを登録するために使用できます。</span><span class="sxs-lookup"><span data-stu-id="0ee62-152">The **Retail Shared Parameters -&gt; Open ID Providers** form can be used to register additional providers.</span></span>
3.  <span data-ttu-id="0ee62-153">配送スケジュール 1110 を実行します。</span><span class="sxs-lookup"><span data-stu-id="0ee62-153">Run distribution schedule 1110.</span></span>



[!INCLUDE[footer-include](../../includes/footer-banner.md)]