---
title: コンテンツ配信ネットワーク (CDN) のサポートの追加
description: このトピックでは、Microsoft Dynamics 365 Commerce 環境にコンテンツ配信ネットワーク (CDN) を追加する方法について説明します。
author: brianshook
ms.date: 03/17/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: brshoo
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: a56f675b1fb43160625101a067c74e9fcf4f714a
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/31/2021
ms.locfileid: "5797842"
---
# <a name="add-support-for-a-content-delivery-network-cdn"></a><span data-ttu-id="9eb8a-103">コンテンツ配信ネットワーク (CDN) のサポートの追加</span><span class="sxs-lookup"><span data-stu-id="9eb8a-103">Add support for a content delivery network (CDN)</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="9eb8a-104">このトピックでは、Microsoft Dynamics 365 Commerce 環境にコンテンツ配信ネットワーク (CDN) を追加する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="9eb8a-104">This topic describes how to add a content delivery network (CDN) to your Microsoft Dynamics 365 Commerce environment.</span></span>

<span data-ttu-id="9eb8a-105">Dynamics 365 Commerce の E コマース環境を設定すると、CDN サービスと連携するようにコンフィギュレーションできます。</span><span class="sxs-lookup"><span data-stu-id="9eb8a-105">When you set up an e-commerce environment in Dynamics 365 Commerce, you can configure it to work with your CDN service.</span></span> 

<span data-ttu-id="9eb8a-106">カスタム ドメインは、E コマース環境のプロビジョニング プロセス中に有効にできます。</span><span class="sxs-lookup"><span data-stu-id="9eb8a-106">Your custom domain can be enabled during the provisioning process for your e-commerce environment.</span></span> <span data-ttu-id="9eb8a-107">また、プロビジョニング プロセスが完了した後に、サービス要求を使用して設定することもできます。</span><span class="sxs-lookup"><span data-stu-id="9eb8a-107">Alternatively, you can use a service request to set it up after the provisioning process is completed.</span></span> <span data-ttu-id="9eb8a-108">E コマース環境のプロビジョニング プロセスでは、環境に関連付けられたホスト名が生成されます。</span><span class="sxs-lookup"><span data-stu-id="9eb8a-108">The provisioning process for the e-commerce environment generates a host name that is associated with the environment.</span></span> <span data-ttu-id="9eb8a-109">\<*e-commerce-tenant-name*\> が環境の名称となっている場合、このホスト名の形式は次のとおりです :</span><span class="sxs-lookup"><span data-stu-id="9eb8a-109">This host name has the following format, where \<*e-commerce-tenant-name*\> is the name of your environment:</span></span>

<span data-ttu-id="9eb8a-110">&lt;e-commerce-tenant-name&gt;.commerce.dynamics.com</span><span class="sxs-lookup"><span data-stu-id="9eb8a-110">&lt;e-commerce-tenant-name&gt;.commerce.dynamics.com</span></span>

<span data-ttu-id="9eb8a-111">プロビジョニング プロセス中に生成されるホスト名またはエンドポイントは、\*.commerce.dynamics.com に対してのみ Secure Sockets Layer (SSL) 証明書をサポートします。</span><span class="sxs-lookup"><span data-stu-id="9eb8a-111">The host name or endpoint that is generated during the provisioning process supports a Secure Sockets Layer (SSL) certificate only for \*.commerce.dynamics.com.</span></span> <span data-ttu-id="9eb8a-112">カスタム ドメインに対する SSL はサポートしません。</span><span class="sxs-lookup"><span data-stu-id="9eb8a-112">It doesn't support SSL for custom domains.</span></span> <span data-ttu-id="9eb8a-113">したがって、CDN のカスタム ドメインの SSL を終了し、CDN からコマースが生成したホスト名またはエンドポイントへトラフィックを転送する必要があります。</span><span class="sxs-lookup"><span data-stu-id="9eb8a-113">Therefore, you must terminate SSL for custom domains in your CDN and forward traffic from the CDN to the host name or endpoint that Commerce generated.</span></span> 

<span data-ttu-id="9eb8a-114">さらに、コマースからの *静的* (JavaScript または カスケード スタイル シート \[CSS\] ファイル) は、コマースが生成したエンドポイント (\*.commerce.dynamics.com) から提供されます。</span><span class="sxs-lookup"><span data-stu-id="9eb8a-114">Additionally, the *statics* (JavaScript or Cascading Style Sheets \[CSS\] files) from Commerce are served from the endpoint that Commerce generated (\*.commerce.dynamics.com).</span></span> <span data-ttu-id="9eb8a-115">静的は、コマースが生成したホスト名またはエンドポイントが CDN の後に配置される場合にのみキャッシュできます。</span><span class="sxs-lookup"><span data-stu-id="9eb8a-115">The statics can be cached only if the host name or endpoint that Commerce generated is put behind the CDN.</span></span>

## <a name="set-up-ssl"></a><span data-ttu-id="9eb8a-116">SSL を設定する</span><span class="sxs-lookup"><span data-stu-id="9eb8a-116">Set up SSL</span></span>

<span data-ttu-id="9eb8a-117">指定されたカスタム ドメインを使用してコマース環境をプロビジョニングした後、またはサービス要求を使用して環境のカスタム ドメインを指定した後は、コマースのオンボーディング チームと協力してDNS の変更を計画する必要があります。</span><span class="sxs-lookup"><span data-stu-id="9eb8a-117">After you provision your Commerce environment with the custom domain that is provided, or after you provide the custom domain for your environment by using a service request, you need to work with the Commerce onboarding team to plan the DNS changes.</span></span>

<span data-ttu-id="9eb8a-118">前述のように、生成したホスト名またはエンドポイントは、\*.commerce.dynamics.com に対してのみ SSL 証明書をサポートします。</span><span class="sxs-lookup"><span data-stu-id="9eb8a-118">As was previously mentioned, the generated host name or endpoint supports an SSL certificate only for \*.commerce.dynamics.com.</span></span> <span data-ttu-id="9eb8a-119">カスタム ドメインに対する SSL はサポートしません。</span><span class="sxs-lookup"><span data-stu-id="9eb8a-119">It doesn't support SSL for custom domains.</span></span>

## <a name="cdn-services"></a><span data-ttu-id="9eb8a-120">CDN サービス</span><span class="sxs-lookup"><span data-stu-id="9eb8a-120">CDN services</span></span>

<span data-ttu-id="9eb8a-121">任意の CDN サービスは、コマース環境で使用できます。</span><span class="sxs-lookup"><span data-stu-id="9eb8a-121">Any CDN service can be used with a Commerce environment.</span></span> <span data-ttu-id="9eb8a-122">次に 2 つの例を挙げます。</span><span class="sxs-lookup"><span data-stu-id="9eb8a-122">Here are two examples:</span></span>

- <span data-ttu-id="9eb8a-123">**Microsoft Azure Front Door Service** – Azure CDN ソリューション。</span><span class="sxs-lookup"><span data-stu-id="9eb8a-123">**Microsoft Azure Front Door Service** – The Azure CDN solution.</span></span> <span data-ttu-id="9eb8a-124">Azure Front Door Service の詳細については、[Azure Front Door Service のドキュメント](https://docs.microsoft.com/azure/frontdoor/) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="9eb8a-124">For more information about Azure Front Door Service, see [Azure Front Door Service Documentation](https://docs.microsoft.com/azure/frontdoor/).</span></span>
- <span data-ttu-id="9eb8a-125">**Akamai 動的サイト アクセラレータ** – 詳細については、[動的サイト アクセラレータ](https://www.akamai.com/us/en/products/performance/dynamic-site-accelerator.jsp) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="9eb8a-125">**Akamai Dynamic Site Accelerator** – For more information, see [Dynamic Site Accelerator](https://www.akamai.com/us/en/products/performance/dynamic-site-accelerator.jsp).</span></span>

## <a name="cdn-setup"></a><span data-ttu-id="9eb8a-126">CDN の設定</span><span class="sxs-lookup"><span data-stu-id="9eb8a-126">CDN setup</span></span>

<span data-ttu-id="9eb8a-127">CDN の設定プロセスは、次の一般的な手順で構成されています。</span><span class="sxs-lookup"><span data-stu-id="9eb8a-127">The CDN setup process consists of these general steps:</span></span>

1. <span data-ttu-id="9eb8a-128">フロント エンド ホストを追加します。</span><span class="sxs-lookup"><span data-stu-id="9eb8a-128">Add a front-end host.</span></span>
1. <span data-ttu-id="9eb8a-129">バック エンド プールを構成します。</span><span class="sxs-lookup"><span data-stu-id="9eb8a-129">Configure a backend pool.</span></span>
1. <span data-ttu-id="9eb8a-130">ルーティング規則を設定する。</span><span class="sxs-lookup"><span data-stu-id="9eb8a-130">Set up rules for routing.</span></span>

### <a name="add-a-front-end-host"></a><span data-ttu-id="9eb8a-131">フロント エンド ホストを追加する</span><span class="sxs-lookup"><span data-stu-id="9eb8a-131">Add a front-end host</span></span>

<span data-ttu-id="9eb8a-132">任意の CDN サービスを使用できますが、このトピックの例では、 Azure Front Door Service を使用します。</span><span class="sxs-lookup"><span data-stu-id="9eb8a-132">Any CDN service can be used, but for the example in this topic, Azure Front Door Service is used.</span></span> 

<span data-ttu-id="9eb8a-133">Azure Front Door Service の設定方法の詳細については、[クイックスタート: 高可用性グローバル Web アプリケーションに対する Front Door を作成する](https://docs.microsoft.com/azure/frontdoor/quickstart-create-front-door) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="9eb8a-133">For information about how to set up Azure Front Door Service, see [Quickstart: Create a Front Door for a highly available global web application](https://docs.microsoft.com/azure/frontdoor/quickstart-create-front-door).</span></span>

### <a name="configure-a-backend-pool-in-azure-front-door-service"></a><span data-ttu-id="9eb8a-134">Azure Front Door Service のバック エンド プールを構成する</span><span class="sxs-lookup"><span data-stu-id="9eb8a-134">Configure a backend pool in Azure Front Door Service</span></span>

<span data-ttu-id="9eb8a-135">Azure Front Door Service のバック エンド プールを構成するには、次の手順を実行してください。</span><span class="sxs-lookup"><span data-stu-id="9eb8a-135">To configure a backend pool in Azure Front Door Service, follow these steps.</span></span>

1. <span data-ttu-id="9eb8a-136">**&lt;ecom-tenant-name&gt;.commerce.dynamics.com** と同じバックエンドホスト ヘッダを持つカスタムホストとして、**&lt;ecom-tenant-name&gt;.commerce.dynamics.com** をバックエンドプールに追加します。</span><span class="sxs-lookup"><span data-stu-id="9eb8a-136">Add **&lt;ecom-tenant-name&gt;.commerce.dynamics.com** to a backend pool as a custom host that has a backend host header that is the same as **&lt;ecom-tenant-name&gt;.commerce.dynamics.com**.</span></span>
1. <span data-ttu-id="9eb8a-137">**負荷分散** では、既定値のままにします。</span><span class="sxs-lookup"><span data-stu-id="9eb8a-137">Under **Load balancing**, leave the default values.</span></span>
1. <span data-ttu-id="9eb8a-138">バックエンド プールの正常性チェックを無効にします。</span><span class="sxs-lookup"><span data-stu-id="9eb8a-138">Disable health checks for the backend pool.</span></span>

<span data-ttu-id="9eb8a-139">次の図は、バック エンド ホスト名が入力された Azure Front Door Service の **バックエンドの追加** ダイアログ ボックスを示します。</span><span class="sxs-lookup"><span data-stu-id="9eb8a-139">The following illustration shows the **Add a backend** dialog box in Azure Front Door Service with the backend host name entered.</span></span>

![バックエンド プール ダイアログ ボックスを追加する](./media/CDN_BackendPool.png)

<span data-ttu-id="9eb8a-141">次の図は、既定の負荷分散値が入力された Azure Front Door Service の **バックエンド プール の追加** ダイアログ ボックスを示します。</span><span class="sxs-lookup"><span data-stu-id="9eb8a-141">The following illustration shows the **Add a backend pool** dialog box in Azure Front Door Service with the default load balancing values.</span></span>

![バックエンド プールのダイアログ ボックスを継続して追加する](./media/CDN_BackendPool_2.png)

> [!NOTE]
> <span data-ttu-id="9eb8a-143">Commerce に対して独自の Azure Front Door Service サービスを設定する際は、 **正常性の検査** を無効にしてください。</span><span class="sxs-lookup"><span data-stu-id="9eb8a-143">Be sure to disable **Health Probes** when setting up your own Azure Front Door service for Commerce.</span></span>


### <a name="set-up-rules-in-azure-front-door-service"></a><span data-ttu-id="9eb8a-144">Azure Front Door Service でルールを設定する</span><span class="sxs-lookup"><span data-stu-id="9eb8a-144">Set up rules in Azure Front Door Service</span></span>

<span data-ttu-id="9eb8a-145">Azure Front Door Service でルート指定ルールを設定するには、次の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="9eb8a-145">To set up a routing rule in Azure Front Door Service, follow these steps.</span></span>

1. <span data-ttu-id="9eb8a-146">ルート指定ルールを追加します。</span><span class="sxs-lookup"><span data-stu-id="9eb8a-146">Add a routing rule.</span></span>
1. <span data-ttu-id="9eb8a-147">**名前** フィールドに、**既定** と入力します。</span><span class="sxs-lookup"><span data-stu-id="9eb8a-147">In the **Name** field, enter **default**.</span></span>
1. <span data-ttu-id="9eb8a-148">**承認済プロトコル** フィールドで、**HTTP と HTTPS** を選択します。</span><span class="sxs-lookup"><span data-stu-id="9eb8a-148">In the **Accepted protocol** field, select **HTTP and HTTPS**.</span></span>
1. <span data-ttu-id="9eb8a-149">**フロントエンド ホスト** フィールドで、**dynamics-ecom-tenant-name.azurefd.net** を入力します。</span><span class="sxs-lookup"><span data-stu-id="9eb8a-149">In the **Frontend hosts** field, enter **dynamics-ecom-tenant-name.azurefd.net**.</span></span>
1. <span data-ttu-id="9eb8a-150">**照合するパターン** の、上のフィールドで、**/\*** と入力します。</span><span class="sxs-lookup"><span data-stu-id="9eb8a-150">Under **Patterns to match**, in the upper field, enter **/\***.</span></span>
1. <span data-ttu-id="9eb8a-151">**工順の詳細** で、**工順タイプ** オプションを **転送** に設定します。</span><span class="sxs-lookup"><span data-stu-id="9eb8a-151">Under **Route Details**, set the **Route type** option to **Forward**.</span></span>
1. <span data-ttu-id="9eb8a-152">**バックエンド プール** フィールドで、**ecom-backend** を選択します。</span><span class="sxs-lookup"><span data-stu-id="9eb8a-152">In the **Backend pool** field, select **ecom-backend**.</span></span>
1. <span data-ttu-id="9eb8a-153">**転送プロトコル** フィールド グループで、**照合要求** オプションを選択します。</span><span class="sxs-lookup"><span data-stu-id="9eb8a-153">In the **Forwarding protocol** field group, select the **Match request** option.</span></span> 
1. <span data-ttu-id="9eb8a-154">**URL Rewrite** オプションを **無効** に設定します。</span><span class="sxs-lookup"><span data-stu-id="9eb8a-154">Set the **URL rewrite** option to **Disabled**.</span></span>
1. <span data-ttu-id="9eb8a-155">**キャッシュ** オプションを **無効** に設定します。</span><span class="sxs-lookup"><span data-stu-id="9eb8a-155">Set the **Caching** option to **Disabled**.</span></span>


> [!WARNING]
> <span data-ttu-id="9eb8a-156">使用するドメインが既に有効化されている場合は、[Microsoft Dynamics Lifecycle Services](https://lcs.dynamics.com/) の **サポート** タイルからサポートチケットを作成して、次の手順についてのサポートを受けてください。</span><span class="sxs-lookup"><span data-stu-id="9eb8a-156">If the domain that you will use is already active and live, create a support ticket from the **Support** tile in [Microsoft Dynamics Lifecycle Services](https://lcs.dynamics.com/) to get assistance for your next steps.</span></span> <span data-ttu-id="9eb8a-157">詳細については、[Finance and Operations アプまたは Lifecycle Services (LCS) のサポートを得る](../fin-ops-core/dev-itpro/lifecycle-services/lcs-support.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="9eb8a-157">For more information, see [Get support for Finance and Operations apps or Lifecycle Services (LCS)](../fin-ops-core/dev-itpro/lifecycle-services/lcs-support.md).</span></span>

<span data-ttu-id="9eb8a-158">ご利用のドメインが新しく、かつ既存のドメインではない場合は、Azure Front Door Service の構成にカスタム ドメインを追加することができます。</span><span class="sxs-lookup"><span data-stu-id="9eb8a-158">If your domain is new and is not a pre-existing live domain, you can add your custom domain to the configuration for Azure Front Door Service.</span></span> <span data-ttu-id="9eb8a-159">これにより、web トラフィックが Azure Front Door インスタンスを介してサイトに誘導されるようになります。</span><span class="sxs-lookup"><span data-stu-id="9eb8a-159">This will enable web traffic to direct to your site via the Azure Front Door instance.</span></span> <span data-ttu-id="9eb8a-160">カスタム ドメイン (たとえば、`www.fabrikam.com`) を追加するには、ドメインの正規名 (CNAME) をコンフィギュレーションする必要があります。</span><span class="sxs-lookup"><span data-stu-id="9eb8a-160">To add the custom domain (for example, `www.fabrikam.com`), you must configure a Canonical Name (CNAME) for the domain.</span></span>

<span data-ttu-id="9eb8a-161">次の図は、Azure Front Door Service の **CNAME コンフィギュレーション** ダイアログ ボックスを示します。</span><span class="sxs-lookup"><span data-stu-id="9eb8a-161">The following illustration shows the **CNAME configuration** dialog box in Azure Front Door Service.</span></span>

![CNAME コンフィギュレーション ダイアログ ボックス](./media/CNAME_Configuration.png)

<span data-ttu-id="9eb8a-163">Azure Front Door Service を使用して証明書を管理したり、カスタム ドメインに対して独自の証明書を使用したりできます。</span><span class="sxs-lookup"><span data-stu-id="9eb8a-163">You can use Azure Front Door Service to manage the certificate, or you can use your own certificate for the custom domain.</span></span>

<span data-ttu-id="9eb8a-164">次の図は、Azure Front Door Service の **カスタム ドメイン HTTPS** ダイアログ ボックスを示します。</span><span class="sxs-lookup"><span data-stu-id="9eb8a-164">The following illustration shows the **Custom Domain HTTPS** dialog box in Azure Front Door Service.</span></span>

![カスタム ドメイン HTTPS ダイアログ ボックス](./media/Custom_Domain_HTTPS.png)

<span data-ttu-id="9eb8a-166">Azure Front Door にカスタムドメインを追加する方法の詳細については、[フロント ドアにカスタム ドメインを追加する](https://docs.microsoft.com/azure/frontdoor/front-door-custom-domain)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="9eb8a-166">For detailed instructions on adding a custom domain to your Azure Front Door, see [Add a custom domain to your Front Door](https://docs.microsoft.com/azure/frontdoor/front-door-custom-domain).</span></span>

<span data-ttu-id="9eb8a-167">これにより、CDN を正しくコンフィギュレーションして、コマース サイトで使用できるようになります。</span><span class="sxs-lookup"><span data-stu-id="9eb8a-167">Your CDN should now be correctly configured so that it can be used with your Commerce site.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="9eb8a-168">追加リソース</span><span class="sxs-lookup"><span data-stu-id="9eb8a-168">Additional resources</span></span>

[<span data-ttu-id="9eb8a-169">コンテンツ配信ネットワークの実装オプション</span><span class="sxs-lookup"><span data-stu-id="9eb8a-169">Content delivery network implementation options</span></span>](cdn-options.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
