---
title: コンテンツ配信ネットワーク (CDN) のサポートの追加
description: このトピックでは、Microsoft Dynamics 365 Commerce 環境にコンテンツ配信ネットワーク (CDN) を追加する方法について説明します。
author: brianshook
manager: annbe
ms.date: 07/31/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.search.scope: Operations, Retail, Core
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: brshoo
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 662d26c0157377977bd1031cd7bb13a8e692f37e
ms.sourcegitcommit: 078befcd7f3531073ab2c08b365bcf132d6477b0
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 07/31/2020
ms.locfileid: "3646042"
---
# <a name="add-support-for-a-content-delivery-network-cdn"></a><span data-ttu-id="6939e-103">コンテンツ配信ネットワーク (CDN) のサポートの追加</span><span class="sxs-lookup"><span data-stu-id="6939e-103">Add support for a content delivery network (CDN)</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="6939e-104">このトピックでは、Microsoft Dynamics 365 Commerce 環境にコンテンツ配信ネットワーク (CDN) を追加する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="6939e-104">This topic describes how to add a content delivery network (CDN) to your Microsoft Dynamics 365 Commerce environment.</span></span>

## <a name="overview"></a><span data-ttu-id="6939e-105">概要</span><span class="sxs-lookup"><span data-stu-id="6939e-105">Overview</span></span>

<span data-ttu-id="6939e-106">Dynamics 365 Commerce の E コマース環境を設定すると、CDN サービスと連携するようにコンフィギュレーションできます。</span><span class="sxs-lookup"><span data-stu-id="6939e-106">When you set up an e-Commerce environment in Dynamics 365 Commerce, you can configure it to work with your CDN service.</span></span> 

<span data-ttu-id="6939e-107">カスタム ドメインは、E コマース環境のプロビジョニング プロセス中に有効にできます。</span><span class="sxs-lookup"><span data-stu-id="6939e-107">Your custom domain can be enabled during the provisioning process for your e-Commerce environment.</span></span> <span data-ttu-id="6939e-108">また、プロビジョニング プロセスが完了した後に、サービス要求を使用して設定することもできます。</span><span class="sxs-lookup"><span data-stu-id="6939e-108">Alternatively, you can use a service request to set it up after the provisioning process is completed.</span></span> <span data-ttu-id="6939e-109">E コマース環境のプロビジョニング プロセスでは、環境に関連付けられたホスト名が生成されます。</span><span class="sxs-lookup"><span data-stu-id="6939e-109">The provisioning process for the e-Commerce environment generates a host name that is associated with the environment.</span></span> <span data-ttu-id="6939e-110">\<*e-commerce-tenant-name*\> が環境の名称となっている場合、このホスト名の形式は次のとおりです :</span><span class="sxs-lookup"><span data-stu-id="6939e-110">This host name has the following format, where \<*e-commerce-tenant-name*\> is the name of your environment:</span></span>

<span data-ttu-id="6939e-111">&lt;e-commerce-tenant-name&gt;.commerce.dynamics.com</span><span class="sxs-lookup"><span data-stu-id="6939e-111">&lt;e-commerce-tenant-name&gt;.commerce.dynamics.com</span></span>

<span data-ttu-id="6939e-112">プロビジョニング プロセス中に生成されるホスト名またはエンドポイントは、\*.commerce.dynamics.com に対してのみ Secure Sockets Layer (SSL) 証明書をサポートします。</span><span class="sxs-lookup"><span data-stu-id="6939e-112">The host name or endpoint that is generated during the provisioning process supports a Secure Sockets Layer (SSL) certificate only for \*.commerce.dynamics.com.</span></span> <span data-ttu-id="6939e-113">カスタム ドメインに対する SSL はサポートしません。</span><span class="sxs-lookup"><span data-stu-id="6939e-113">It doesn't support SSL for custom domains.</span></span> <span data-ttu-id="6939e-114">したがって、CDN のカスタム ドメインの SSL を終了し、CDN からコマースが生成したホスト名またはエンドポイントへトラフィックを転送する必要があります。</span><span class="sxs-lookup"><span data-stu-id="6939e-114">Therefore, you must terminate SSL for custom domains in your CDN and forward traffic from the CDN to the host name or endpoint that Commerce generated.</span></span> 

<span data-ttu-id="6939e-115">さらに、コマースからの *静的* (JavaScript または カスケード スタイル シート \[CSS\] ファイル) は、コマースが生成したエンドポイント (\*.commerce.dynamics.com) から提供されます。</span><span class="sxs-lookup"><span data-stu-id="6939e-115">Additionally, the *statics* (JavaScript or Cascading Style Sheets \[CSS\] files) from Commerce are served from the endpoint that Commerce generated (\*.commerce.dynamics.com).</span></span> <span data-ttu-id="6939e-116">静的は、コマースが生成したホスト名またはエンドポイントが CDN の後に配置される場合にのみキャッシュできます。</span><span class="sxs-lookup"><span data-stu-id="6939e-116">The statics can be cached only if the host name or endpoint that Commerce generated is put behind the CDN.</span></span>

## <a name="set-up-ssl"></a><span data-ttu-id="6939e-117">SSL のセットアップ</span><span class="sxs-lookup"><span data-stu-id="6939e-117">Set up SSL</span></span>

<span data-ttu-id="6939e-118">SSL が設定され、その静的が確実にキャッシュされるようにするには、環境に対してコマースが生成したホスト名に関連付けられるよう CDN をコンフィギュレーションする必要があります。</span><span class="sxs-lookup"><span data-stu-id="6939e-118">To help guarantee that SSL is set up, and that statics are cached, you must configure your CDN so that it is associated with the host name that Commerce generated for your environment.</span></span> <span data-ttu-id="6939e-119">また、次のパターンを静的に対してのみキャッシュする必要があります。</span><span class="sxs-lookup"><span data-stu-id="6939e-119">You must also cache the following pattern for statics only:</span></span> 

<span data-ttu-id="6939e-120">/\_msdyn365/\_scnr/\*</span><span class="sxs-lookup"><span data-stu-id="6939e-120">/\_msdyn365/\_scnr/\*</span></span>

<span data-ttu-id="6939e-121">指定されたカスタム ドメインを使用してコマース環境をプロビジョニングした後、またはサービス要求を使用して環境のカスタム ドメインを指定した後、カスタム ドメインをコマースが生成したホスト名またはエンドポイントに向けます。</span><span class="sxs-lookup"><span data-stu-id="6939e-121">After you provision your Commerce environment with the custom domain that is provided, or after you provide the custom domain for your environment by using a service request, point your custom domain to the host name or endpoint that Commerce generated.</span></span>

<span data-ttu-id="6939e-122">前述のように、生成したホスト名またはエンドポイントは、\*.commerce.dynamics.com に対してのみ SSL 証明書をサポートします。</span><span class="sxs-lookup"><span data-stu-id="6939e-122">As was previously mentioned, the generated host name or endpoint supports an SSL certificate only for \*.commerce.dynamics.com.</span></span> <span data-ttu-id="6939e-123">カスタム ドメインに対する SSL はサポートしません。</span><span class="sxs-lookup"><span data-stu-id="6939e-123">It doesn't support SSL for custom domains.</span></span>

## <a name="cdn-services"></a><span data-ttu-id="6939e-124">CDN サービス</span><span class="sxs-lookup"><span data-stu-id="6939e-124">CDN services</span></span>

<span data-ttu-id="6939e-125">任意の CDN サービスは、コマース環境で使用できます。</span><span class="sxs-lookup"><span data-stu-id="6939e-125">Any CDN service can be used with a Commerce environment.</span></span> <span data-ttu-id="6939e-126">次に 2 つの例を挙げます。</span><span class="sxs-lookup"><span data-stu-id="6939e-126">Here are two examples:</span></span>

- <span data-ttu-id="6939e-127">**Microsoft Azure Front Door Service** – Azure CDN ソリューション。</span><span class="sxs-lookup"><span data-stu-id="6939e-127">**Microsoft Azure Front Door Service** – The Azure CDN solution.</span></span> <span data-ttu-id="6939e-128">Azure Front Door Service の詳細については、[Azure Front Door Service のドキュメント](https://docs.microsoft.com/azure/frontdoor/) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="6939e-128">For more information about Azure Front Door Service, see [Azure Front Door Service Documentation](https://docs.microsoft.com/azure/frontdoor/).</span></span>
- <span data-ttu-id="6939e-129">**Akamai 動的サイト アクセラレータ** – 詳細については、[動的サイト アクセラレータ](https://www.akamai.com/us/en/products/performance/dynamic-site-accelerator.jsp) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="6939e-129">**Akamai Dynamic Site Accelerator** – For more information, see [Dynamic Site Accelerator](https://www.akamai.com/us/en/products/performance/dynamic-site-accelerator.jsp).</span></span>

## <a name="cdn-setup"></a><span data-ttu-id="6939e-130">CDN の設定</span><span class="sxs-lookup"><span data-stu-id="6939e-130">CDN setup</span></span>

<span data-ttu-id="6939e-131">CDN の設定プロセスは、次の一般的な手順で構成されています。</span><span class="sxs-lookup"><span data-stu-id="6939e-131">The CDN setup process consists of these general steps:</span></span>

1. <span data-ttu-id="6939e-132">フロント エンド ホストを追加します。</span><span class="sxs-lookup"><span data-stu-id="6939e-132">Add a front-end host.</span></span>
1. <span data-ttu-id="6939e-133">バック エンド プールを構成します。</span><span class="sxs-lookup"><span data-stu-id="6939e-133">Configure a backend pool.</span></span>
1. <span data-ttu-id="6939e-134">ルート指定とキャッシュのルールを設定します。</span><span class="sxs-lookup"><span data-stu-id="6939e-134">Set up rules for routing and caching.</span></span>

### <a name="add-a-front-end-host"></a><span data-ttu-id="6939e-135">フロント エンド ホストを追加する</span><span class="sxs-lookup"><span data-stu-id="6939e-135">Add a front-end host</span></span>

<span data-ttu-id="6939e-136">任意の CDN サービスを使用できますが、このトピックの例では、 Azure Front Door Service を使用します。</span><span class="sxs-lookup"><span data-stu-id="6939e-136">Any CDN service can be used, but for the example in this topic, Azure Front Door Service is used.</span></span> 

<span data-ttu-id="6939e-137">Azure Front Door Service の設定方法の詳細については、[クイックスタート: 高可用性グローバル Web アプリケーションに対する Front Door を作成する](https://docs.microsoft.com/azure/frontdoor/quickstart-create-front-door) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="6939e-137">For information about how to set up Azure Front Door Service, see [Quickstart: Create a Front Door for a highly available global web application](https://docs.microsoft.com/azure/frontdoor/quickstart-create-front-door).</span></span>

### <a name="configure-a-backend-pool-in-azure-front-door-service"></a><span data-ttu-id="6939e-138">Azure Front Door Service のバック エンド プールを構成する</span><span class="sxs-lookup"><span data-stu-id="6939e-138">Configure a backend pool in Azure Front Door Service</span></span>

<span data-ttu-id="6939e-139">Azure Front Door Service のバック エンド プールを構成するには、次の手順を実行してください。</span><span class="sxs-lookup"><span data-stu-id="6939e-139">To configure a backend pool in Azure Front Door Service, follow these steps.</span></span>

1. <span data-ttu-id="6939e-140">**&lt;ecom-tenant-name&gt;.commerce.dynamics.com** を、空のバック エンド ホスト ヘッダーを持つカスタム ホストとして、バック エンド プールに追加します。</span><span class="sxs-lookup"><span data-stu-id="6939e-140">Add **&lt;ecom-tenant-name&gt;.commerce.dynamics.com** to a backend pool as a custom host that has an empty backend host header.</span></span>
1. <span data-ttu-id="6939e-141">**負荷分散**では、既定値のままにします。</span><span class="sxs-lookup"><span data-stu-id="6939e-141">Under **Load balancing**, leave the default values.</span></span>

<span data-ttu-id="6939e-142">次の図は、バック エンド ホスト名が入力された Azure Front Door Service の**バックエンドの追加**ダイアログ ボックスを示します。</span><span class="sxs-lookup"><span data-stu-id="6939e-142">The following illustration shows the **Add a backend** dialog box in Azure Front Door Service with the backend host name entered.</span></span>

![バックエンド プール ダイアログ ボックスを追加する](./media/CDN_BackendPool.png)

<span data-ttu-id="6939e-144">次の図は、既定の負荷分散値が入力された Azure Front Door Service の**バックエンド プール の追加**ダイアログ ボックスを示します。</span><span class="sxs-lookup"><span data-stu-id="6939e-144">The following illustration shows the **Add a backend pool** dialog box in Azure Front Door Service with the default load balancing values.</span></span>

![バックエンド プールのダイアログ ボックスを継続して追加する](./media/CDN_BackendPool_2.png)

### <a name="set-up-rules-in-azure-front-door-service"></a><span data-ttu-id="6939e-146">Azure Front Door Service でルールを設定する</span><span class="sxs-lookup"><span data-stu-id="6939e-146">Set up rules in Azure Front Door Service</span></span>

<span data-ttu-id="6939e-147">Azure Front Door Service でルート指定ルールを設定するには、次の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="6939e-147">To set up a routing rule in Azure Front Door Service, follow these steps.</span></span>

1. <span data-ttu-id="6939e-148">ルート指定ルールを追加します。</span><span class="sxs-lookup"><span data-stu-id="6939e-148">Add a routing rule.</span></span>
1. <span data-ttu-id="6939e-149">**名前**フィールドに、**既定**と入力します。</span><span class="sxs-lookup"><span data-stu-id="6939e-149">In the **Name** field, enter **default**.</span></span>
1. <span data-ttu-id="6939e-150">**承認済プロトコル** フィールドで、**HTTP と HTTPS** を選択します。</span><span class="sxs-lookup"><span data-stu-id="6939e-150">In the **Accepted protocol** field, select **HTTP and HTTPS**.</span></span>
1. <span data-ttu-id="6939e-151">**フロントエンド ホスト** フィールドで、**dynamics-ecom-tenant-name.azurefd.net** を入力します。</span><span class="sxs-lookup"><span data-stu-id="6939e-151">In the **Frontend hosts** field, enter **dynamics-ecom-tenant-name.azurefd.net**.</span></span>
1. <span data-ttu-id="6939e-152">**照合するパターン**の、上のフィールドで、**/\*** と入力します。</span><span class="sxs-lookup"><span data-stu-id="6939e-152">Under **Patterns to match**, in the upper field, enter **/\***.</span></span>
1. <span data-ttu-id="6939e-153">**工順の詳細**で、**工順タイプ** オプションを**転送**に設定します。</span><span class="sxs-lookup"><span data-stu-id="6939e-153">Under **Route Details**, set the **Route type** option to **Forward**.</span></span>
1. <span data-ttu-id="6939e-154">**バックエンド プール** フィールドで、**ecom-backend** を選択します。</span><span class="sxs-lookup"><span data-stu-id="6939e-154">In the **Backend pool** field, select **ecom-backend**.</span></span>
1. <span data-ttu-id="6939e-155">**転送プロトコル** フィールド グループで、**照合要求**オプションを選択します。</span><span class="sxs-lookup"><span data-stu-id="6939e-155">In the **Forwarding protocol** field group, select the **Match request** option.</span></span> 
1. <span data-ttu-id="6939e-156">**URL Rewrite** オプションを**無効**に設定します。</span><span class="sxs-lookup"><span data-stu-id="6939e-156">Set the **URL rewrite** option to **Disabled**.</span></span>
1. <span data-ttu-id="6939e-157">**キャッシュ** オプションを**無効**に設定します。</span><span class="sxs-lookup"><span data-stu-id="6939e-157">Set the **Caching** option to **Disabled**.</span></span>

<span data-ttu-id="6939e-158">Azure Front Door Service でキャッシュ ルールを設定するには、次の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="6939e-158">To set up a caching rule in Azure Front Door Service, follow these steps.</span></span>

1. <span data-ttu-id="6939e-159">キャッシュ ルールを追加します。</span><span class="sxs-lookup"><span data-stu-id="6939e-159">Add a caching rule.</span></span>
1. <span data-ttu-id="6939e-160">**名前**フィールドに、**静的**と入力します。</span><span class="sxs-lookup"><span data-stu-id="6939e-160">In the **Name** field, enter **statics**.</span></span>
1. <span data-ttu-id="6939e-161">**承認済プロトコル** フィールドで、**HTTP と HTTPS** を選択します。</span><span class="sxs-lookup"><span data-stu-id="6939e-161">In the **Accepted protocol** field, select **HTTP and HTTPS**.</span></span>
1. <span data-ttu-id="6939e-162">**フロントエンド ホスト** フィールドで、**dynamics-ecom-tenant-name.azurefd.net** を入力します。</span><span class="sxs-lookup"><span data-stu-id="6939e-162">In the **Frontend hosts** field, enter **dynamics-ecom-tenant-name.azurefd.net**.</span></span>
1. <span data-ttu-id="6939e-163">**照合するパターン**の、上のフィールドで、**/\_msdyn365/\_scnr/\*** と入力します。</span><span class="sxs-lookup"><span data-stu-id="6939e-163">Under **Patterns to match**, in the upper field, **/\_msdyn365/\_scnr/\***.</span></span>
1. <span data-ttu-id="6939e-164">**工順の詳細**で、**工順タイプ** オプションを**転送**に設定します。</span><span class="sxs-lookup"><span data-stu-id="6939e-164">Under **Route Details**, set the **Route type** option to **Forward**.</span></span>
1. <span data-ttu-id="6939e-165">**バックエンド プール** フィールドで、**ecom-backend** を選択します。</span><span class="sxs-lookup"><span data-stu-id="6939e-165">In the **Backend pool** field, select **ecom-backend**.</span></span>
1. <span data-ttu-id="6939e-166">**転送プロトコル** フィールド グループで、**照合要求**オプションを選択します。</span><span class="sxs-lookup"><span data-stu-id="6939e-166">In the **Forwarding protocol** field group, select the **Match request** option.</span></span>
1. <span data-ttu-id="6939e-167">**URL Rewrite** オプションを**無効**に設定します。</span><span class="sxs-lookup"><span data-stu-id="6939e-167">Set the **URL rewrite** option to **Disabled**.</span></span>
1. <span data-ttu-id="6939e-168">**キャッシュ** オプションを**無効**に設定します。</span><span class="sxs-lookup"><span data-stu-id="6939e-168">Set the **Caching** option to **Disabled**.</span></span>
1. <span data-ttu-id="6939e-169">**クエリ文字列のキャッシュ動作**フィールドで、**一意の URL ごとキャッシュする**を選択します。</span><span class="sxs-lookup"><span data-stu-id="6939e-169">In the **Query string caching behavior** field, select **Cache every unique URL**.</span></span>
1. <span data-ttu-id="6939e-170">**動的な圧縮**フィールド グループで、**有効化**オプションを選択します。</span><span class="sxs-lookup"><span data-stu-id="6939e-170">In the **Dynamic compression** field group, select the **Enabled** option.</span></span>

<span data-ttu-id="6939e-171">次の図は、Azure Front Door Service の**ルールの追加**ダイアログ ボックスを示します。</span><span class="sxs-lookup"><span data-stu-id="6939e-171">The following illustration shows the **Add a rule** dialog box in Azure Front Door Service.</span></span>

![ルールの追加ダイアログ ボックス](./media/CDN_CachingRule.png)

> [!WARNING]
> <span data-ttu-id="6939e-173">使用するドメインが既に有効化されている場合は、[Microsoft Dynamics Lifecycle Services](https://lcs.dynamics.com/) の **サポート**タイルからサポートチケットを作成して、次の手順についてのサポートを受けてください。</span><span class="sxs-lookup"><span data-stu-id="6939e-173">If the domain that you will use is already active and live, create a support ticket from the **Support** tile in [Microsoft Dynamics Lifecycle Services](https://lcs.dynamics.com/) to get assistance for your next steps.</span></span> <span data-ttu-id="6939e-174">詳細については、[Finance and Operations アプまたは Lifecycle Services (LCS) のサポートを得る](../fin-ops-core/dev-itpro/lifecycle-services/lcs-support.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="6939e-174">For more information, see [Get support for Finance and Operations apps or Lifecycle Services (LCS)](../fin-ops-core/dev-itpro/lifecycle-services/lcs-support.md).</span></span>

<span data-ttu-id="6939e-175">ご利用のドメインが新しく、かつ既存のドメインではない場合は、Azure Front Door Service の構成にカスタム ドメインを追加することができます。</span><span class="sxs-lookup"><span data-stu-id="6939e-175">If your domain is new and is not a pre-existing live domain, you can add your custom domain to the configuration for Azure Front Door Service.</span></span> <span data-ttu-id="6939e-176">これにより、web トラフィックが Azure Front Door インスタンスを介してサイトに誘導されるようになります。</span><span class="sxs-lookup"><span data-stu-id="6939e-176">This will enable web traffic to direct to your site via the Azure Front Door instance.</span></span> <span data-ttu-id="6939e-177">カスタム ドメイン (たとえば、`www.fabrikam.com`) を追加するには、ドメインの正規名 (CNAME) をコンフィギュレーションする必要があります。</span><span class="sxs-lookup"><span data-stu-id="6939e-177">To add the custom domain (for example, `www.fabrikam.com`), you must configure a Canonical Name (CNAME) for the domain.</span></span>

<span data-ttu-id="6939e-178">次の図は、Azure Front Door Service の**CNAME コンフィギュレーション** ダイアログ ボックスを示します。</span><span class="sxs-lookup"><span data-stu-id="6939e-178">The following illustration shows the **CNAME configuration** dialog box in Azure Front Door Service.</span></span>

![CNAME コンフィギュレーション ダイアログ ボックス](./media/CNAME_Configuration.png)

<span data-ttu-id="6939e-180">Azure Front Door Service を使用して証明書を管理したり、カスタム ドメインに対して独自の証明書を使用したりできます。</span><span class="sxs-lookup"><span data-stu-id="6939e-180">You can use Azure Front Door Service to manage the certificate, or you can use your own certificate for the custom domain.</span></span>

<span data-ttu-id="6939e-181">次の図は、Azure Front Door Service の**カスタム ドメイン HTTPS** ダイアログ ボックスを示します。</span><span class="sxs-lookup"><span data-stu-id="6939e-181">The following illustration shows the **Custom Domain HTTPS** dialog box in Azure Front Door Service.</span></span>

![カスタム ドメイン HTTPS ダイアログ ボックス](./media/Custom_Domain_HTTPS.png)

<span data-ttu-id="6939e-183">Azure Front Door にカスタムドメインを追加する方法の詳細については、[フロント ドアにカスタム ドメインを追加する](https://docs.microsoft.com/azure/frontdoor/front-door-custom-domain)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="6939e-183">For detailed instructions on adding a custom domain to your Azure Front Door, see [Add a custom domain to your Front Door](https://docs.microsoft.com/azure/frontdoor/front-door-custom-domain).</span></span>

<span data-ttu-id="6939e-184">これにより、CDN を正しくコンフィギュレーションして、コマース サイトで使用できるようになります。</span><span class="sxs-lookup"><span data-stu-id="6939e-184">Your CDN should now be correctly configured so that it can be used with your Commerce site.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="6939e-185">追加リソース</span><span class="sxs-lookup"><span data-stu-id="6939e-185">Additional resources</span></span>

[<span data-ttu-id="6939e-186">ドメイン名のコンフィギュレーション</span><span class="sxs-lookup"><span data-stu-id="6939e-186">Configure your domain name</span></span>](configure-your-domain-name.md)

[<span data-ttu-id="6939e-187">新しい E コマース サイトの配置</span><span class="sxs-lookup"><span data-stu-id="6939e-187">Deploy a new e-Commerce site</span></span>](deploy-ecommerce-site.md)

[<span data-ttu-id="6939e-188">E コマース サイトの作成</span><span class="sxs-lookup"><span data-stu-id="6939e-188">Create an e-Commerce site</span></span>](create-ecommerce-site.md)

[<span data-ttu-id="6939e-189">チャンネルとオンライン サイトの関連付け</span><span class="sxs-lookup"><span data-stu-id="6939e-189">Associate an online site with a channel</span></span>](associate-site-online-store.md)

[<span data-ttu-id="6939e-190">robots.txt ファイルの管理</span><span class="sxs-lookup"><span data-stu-id="6939e-190">Manage robots.txt files</span></span>](manage-robots-txt-files.md)

[<span data-ttu-id="6939e-191">URL リダイレクトの一括アップロード</span><span class="sxs-lookup"><span data-stu-id="6939e-191">Upload URL redirects in bulk</span></span>](upload-bulk-redirects.md)

[<span data-ttu-id="6939e-192">B2C テナントを Commerce に 設定</span><span class="sxs-lookup"><span data-stu-id="6939e-192">Set up a B2C tenant in Commerce</span></span>](set-up-B2C-tenant.md)

[<span data-ttu-id="6939e-193">ユーザー ログイン用のカスタム ページの設定</span><span class="sxs-lookup"><span data-stu-id="6939e-193">Set up custom pages for user logins</span></span>](custom-pages-user-logins.md)

[<span data-ttu-id="6939e-194">Commerce 環境での複数の B2C テナントのコンフィギュレーション</span><span class="sxs-lookup"><span data-stu-id="6939e-194">Configure multiple B2C tenants in a Commerce environment</span></span>](configure-multi-B2C-tenants.md)

[<span data-ttu-id="6939e-195">場所に基づく店舗検出の有効化</span><span class="sxs-lookup"><span data-stu-id="6939e-195">Enable location-based store detection</span></span>](enable-store-detection.md)
