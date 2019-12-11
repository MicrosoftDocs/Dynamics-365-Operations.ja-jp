---
title: コンテンツ配信ネットワーク (CDN) のサポートの追加
description: このトピックでは、Microsoft Dynamics 365 Commerce 環境にコンテンツ配信ネットワーク (CDN) を追加する方法について説明します。
author: brianshook
manager: annbe
ms.date: 10/01/2019
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
ms.openlocfilehash: fb757672fffb56892837c066d552773908dd1ec1
ms.sourcegitcommit: 295d940a345879b3dfc5991e387b91c7257019ea
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/01/2019
ms.locfileid: "2696971"
---
# <a name="add-support-for-a-content-delivery-network-cdn"></a><span data-ttu-id="101df-103">コンテンツ配信ネットワーク (CDN) のサポートの追加</span><span class="sxs-lookup"><span data-stu-id="101df-103">Add support for a content delivery network (CDN)</span></span>

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

<span data-ttu-id="101df-104">このトピックでは、Microsoft Dynamics 365 Commerce 環境にコンテンツ配信ネットワーク (CDN) を追加する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="101df-104">This topic describes how to add a content delivery network (CDN) to your Microsoft Dynamics 365 Commerce environment.</span></span>

## <a name="overview"></a><span data-ttu-id="101df-105">概要</span><span class="sxs-lookup"><span data-stu-id="101df-105">Overview</span></span>

<span data-ttu-id="101df-106">Dynamics 365 Commerce の E コマース環境を設定すると、CDN サービスと連携するようにコンフィギュレーションできます。</span><span class="sxs-lookup"><span data-stu-id="101df-106">When you set up an e-Commerce environment in Dynamics 365 Commerce, you can configure it to work with your CDN service.</span></span> 

<span data-ttu-id="101df-107">カスタム ドメインは、E コマース環境のプロビジョニング プロセス中に有効にできます。</span><span class="sxs-lookup"><span data-stu-id="101df-107">Your custom domain can be enabled during the provisioning process for your e-Commerce environment.</span></span> <span data-ttu-id="101df-108">また、プロビジョニング プロセスが完了した後に、サービス要求を使用して設定することもできます。</span><span class="sxs-lookup"><span data-stu-id="101df-108">Alternatively, you can use a service request to set it up after the provisioning process is completed.</span></span> <span data-ttu-id="101df-109">E コマース環境のプロビジョニング プロセスでは、環境に関連付けられたホスト名が生成されます。</span><span class="sxs-lookup"><span data-stu-id="101df-109">The provisioning process for the e-Commerce environment generates a host name that is associated with the environment.</span></span> <span data-ttu-id="101df-110">このホスト名の形式は次のとおりです。*e-commerce-tenant-name* は、環境の名前です。</span><span class="sxs-lookup"><span data-stu-id="101df-110">This host name has the following format, where *e-commerce-tenant-name* is the name of your environment:</span></span>

<span data-ttu-id="101df-111">&lt;e-commerce-tenant-name&gt;.commerce.dynamics.com</span><span class="sxs-lookup"><span data-stu-id="101df-111">&lt;e-commerce-tenant-name&gt;.commerce.dynamics.com</span></span>

<span data-ttu-id="101df-112">プロビジョニング プロセス中に生成されるホスト名またはエンドポイントは、\*.commerce.dynamics.com に対してのみ Secure Sockets Layer (SSL) 証明書をサポートします。</span><span class="sxs-lookup"><span data-stu-id="101df-112">The host name or endpoint that is generated during the provisioning process supports a Secure Sockets Layer (SSL) certificate only for \*.commerce.dynamics.com.</span></span> <span data-ttu-id="101df-113">カスタム ドメインに対する SSL はサポートしません。</span><span class="sxs-lookup"><span data-stu-id="101df-113">It doesn't support SSL for custom domains.</span></span> <span data-ttu-id="101df-114">したがって、CDN のカスタム ドメインの SSL を終了し、CDN からコマースが生成したホスト名またはエンドポイントへトラフィックを転送する必要があります。</span><span class="sxs-lookup"><span data-stu-id="101df-114">Therefore, you must terminate SSL for custom domains in your CDN and forward traffic from the CDN to the host name or endpoint that Commerce generated.</span></span> 

<span data-ttu-id="101df-115">さらに、コマースからの *静的* (JavaScript または カスケード スタイル シート \[CSS\] ファイル) は、コマースが生成したエンドポイント (\*.commerce.dynamics.com) から提供されます。</span><span class="sxs-lookup"><span data-stu-id="101df-115">Additionally, the *statics* (JavaScript or Cascading Style Sheets \[CSS\] files) from Commerce are served from the endpoint that Commerce generated (\*.commerce.dynamics.com).</span></span> <span data-ttu-id="101df-116">静的は、コマースが生成したホスト名またはエンドポイントが CDN の後に配置される場合にのみキャッシュできます。</span><span class="sxs-lookup"><span data-stu-id="101df-116">The statics can be cached only if the host name or endpoint that Commerce generated is put behind the CDN.</span></span>

## <a name="set-up-ssl"></a><span data-ttu-id="101df-117">SSL のセットアップ</span><span class="sxs-lookup"><span data-stu-id="101df-117">Set up SSL</span></span>

<span data-ttu-id="101df-118">SSL が設定され、その静的が確実にキャッシュされるようにするには、環境に対してコマースが生成したホスト名に関連付けられるよう CDN をコンフィギュレーションする必要があります。</span><span class="sxs-lookup"><span data-stu-id="101df-118">To help guarantee that SSL is set up, and that statics are cached, you must configure your CDN so that it is associated with the host name that Commerce generated for your environment.</span></span> <span data-ttu-id="101df-119">また、次のパターンを静的に対してのみキャッシュする必要があります。</span><span class="sxs-lookup"><span data-stu-id="101df-119">You must also cache the following pattern for statics only:</span></span> 

<span data-ttu-id="101df-120">/\_msdyn365/\_scnr/\*</span><span class="sxs-lookup"><span data-stu-id="101df-120">/\_msdyn365/\_scnr/\*</span></span>

<span data-ttu-id="101df-121">指定されたカスタム ドメインを使用してコマース環境をプロビジョニングした後、またはサービス要求を使用して環境のカスタム ドメインを指定した後、カスタム ドメインをコマースが生成したホスト名またはエンドポイントに向けます。</span><span class="sxs-lookup"><span data-stu-id="101df-121">After you provision your Commerce environment with the custom domain that is provided, or after you provide the custom domain for your environment by using a service request, point your custom domain to the host name or endpoint that Commerce generated.</span></span>

<span data-ttu-id="101df-122">前述のように、生成したホスト名またはエンドポイントは、\*.commerce.dynamics.com に対してのみ SSL 証明書をサポートします。</span><span class="sxs-lookup"><span data-stu-id="101df-122">As was previously mentioned, the generated host name or endpoint supports an SSL certificate only for \*.commerce.dynamics.com.</span></span> <span data-ttu-id="101df-123">カスタム ドメインに対する SSL はサポートしません。</span><span class="sxs-lookup"><span data-stu-id="101df-123">It doesn't support SSL for custom domains.</span></span>

## <a name="cdn-services"></a><span data-ttu-id="101df-124">CDN サービス</span><span class="sxs-lookup"><span data-stu-id="101df-124">CDN services</span></span>

<span data-ttu-id="101df-125">任意の CDN サービスは、コマース環境で使用できます。</span><span class="sxs-lookup"><span data-stu-id="101df-125">Any CDN service can be used with a Commerce environment.</span></span> <span data-ttu-id="101df-126">次に 2 つの例を挙げます。</span><span class="sxs-lookup"><span data-stu-id="101df-126">Here are two examples:</span></span>

- <span data-ttu-id="101df-127">**Microsoft Azure Front Door Service** – Azure CDN ソリューション。</span><span class="sxs-lookup"><span data-stu-id="101df-127">**Microsoft Azure Front Door Service** – The Azure CDN solution.</span></span> <span data-ttu-id="101df-128">Azure Front Door Service の詳細については、[Azure Front Door Service のドキュメント](https://docs.microsoft.com/azure/frontdoor/) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="101df-128">For more information about Azure Front Door Service, see [Azure Front Door Service Documentation](https://docs.microsoft.com/azure/frontdoor/).</span></span>
- <span data-ttu-id="101df-129">**Akamai 動的サイト アクセラレータ** – 詳細については、[動的サイト アクセラレータ](https://www.akamai.com/us/en/products/performance/dynamic-site-accelerator.jsp) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="101df-129">**Akamai Dynamic Site Accelerator** – For more information, see [Dynamic Site Accelerator](https://www.akamai.com/us/en/products/performance/dynamic-site-accelerator.jsp).</span></span>

## <a name="cdn-setup"></a><span data-ttu-id="101df-130">CDN の設定</span><span class="sxs-lookup"><span data-stu-id="101df-130">CDN setup</span></span>

<span data-ttu-id="101df-131">CDN の設定プロセスは、次の一般的な手順で構成されています。</span><span class="sxs-lookup"><span data-stu-id="101df-131">The CDN setup process consists of these general steps:</span></span>

1. <span data-ttu-id="101df-132">フロント エンド ホストを追加します。</span><span class="sxs-lookup"><span data-stu-id="101df-132">Add a front-end host.</span></span>
1. <span data-ttu-id="101df-133">バック エンド プールをコンフィギュレーションします。</span><span class="sxs-lookup"><span data-stu-id="101df-133">Configure a back-end pool.</span></span>
1. <span data-ttu-id="101df-134">ルート指定とキャッシュのルールを設定します。</span><span class="sxs-lookup"><span data-stu-id="101df-134">Set up rules for routing and caching.</span></span>

### <a name="add-a-front-end-host"></a><span data-ttu-id="101df-135">フロント エンド ホストを追加する</span><span class="sxs-lookup"><span data-stu-id="101df-135">Add a front-end host</span></span>

<span data-ttu-id="101df-136">任意の CDN サービスを使用できますが、このトピックの例では、 Azure Front Door Service を使用します。</span><span class="sxs-lookup"><span data-stu-id="101df-136">Any CDN service can be used, but for the example in this topic, Azure Front Door Service is used.</span></span> 

<span data-ttu-id="101df-137">Azure Front Door Service の設定方法の詳細については、[クイックスタート: 高可用性グローバル Web アプリケーションに対する Front Door を作成する](https://docs.microsoft.com/azure/frontdoor/quickstart-create-front-door) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="101df-137">For information about how to set up Azure Front Door Service, see [Quickstart: Create a Front Door for a highly available global web application](https://docs.microsoft.com/azure/frontdoor/quickstart-create-front-door).</span></span>

### <a name="configure-a-back-end-pool-in-azure-front-door-service"></a><span data-ttu-id="101df-138">Azure Front Door Service のバック エンド プールをコンフィギュレーションする</span><span class="sxs-lookup"><span data-stu-id="101df-138">Configure a back-end pool in Azure Front Door Service</span></span>

<span data-ttu-id="101df-139">Azure Front Door Service のバック エンド プールをコンフィギュレーションするには、次の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="101df-139">To configure a back-end pool in Azure Front Door Service, follow these steps.</span></span>

1. <span data-ttu-id="101df-140">**&lt;ecom-tenant-name&gt;.commerce.dynamics.com** を、バック エンド ホスト ヘッダーが空であるカスタム ホストとして、バック エンド プールに追加します。</span><span class="sxs-lookup"><span data-stu-id="101df-140">Add **&lt;ecom-tenant-name&gt;.commerce.dynamics.com** to a back-end pool as a custom host that has an empty back-end host header.</span></span>
1. <span data-ttu-id="101df-141">**正常性プローブ**の下の、**パス** フィールドに、**/keepalive** と入力します。</span><span class="sxs-lookup"><span data-stu-id="101df-141">Under **Health probes**, in the **Path** field, enter **/keepalive**.</span></span>
1. <span data-ttu-id="101df-142">**間隔 (秒)** フィールドに、**255** と入力します。</span><span class="sxs-lookup"><span data-stu-id="101df-142">In the **Intervals (seconds)** field, enter **255**.</span></span>
1. <span data-ttu-id="101df-143">**負荷分散**では、既定値のままにします。</span><span class="sxs-lookup"><span data-stu-id="101df-143">Under **Load balancing**, leave the default values.</span></span>

<span data-ttu-id="101df-144">次の図は、Azure Front Door Service の**バックエンド プールの追加**ダイアログ ボックスを示します。</span><span class="sxs-lookup"><span data-stu-id="101df-144">The following illustration shows the **Add a backend pool** dialog box in Azure Front Door Service.</span></span>

![バックエンド プール ダイアログ ボックスを追加する](./media/CDN_BackendPool.png)

### <a name="set-up-rules-in-azure-front-door-service"></a><span data-ttu-id="101df-146">Azure Front Door Service でルールを設定する</span><span class="sxs-lookup"><span data-stu-id="101df-146">Set up rules in Azure Front Door Service</span></span>

<span data-ttu-id="101df-147">Azure Front Door Service でルート指定ルールを設定するには、次の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="101df-147">To set up a routing rule in Azure Front Door Service, follow these steps.</span></span>

1. <span data-ttu-id="101df-148">ルート指定ルールを追加します。</span><span class="sxs-lookup"><span data-stu-id="101df-148">Add a routing rule.</span></span>
1. <span data-ttu-id="101df-149">**名前**フィールドに、**既定**と入力します。</span><span class="sxs-lookup"><span data-stu-id="101df-149">In the **Name** field, enter **default**.</span></span>
1. <span data-ttu-id="101df-150">**承認済プロトコル** フィールドで、**HTTP と HTTPS** を選択します。</span><span class="sxs-lookup"><span data-stu-id="101df-150">In the **Accepted protocol** field, select **HTTP and HTTPS**.</span></span>
1. <span data-ttu-id="101df-151">**フロントエンド ホスト** フィールドで、**dynamics-ecom-tenant-name.azurefd.net** を入力します。</span><span class="sxs-lookup"><span data-stu-id="101df-151">In the **Frontend hosts** field, enter **dynamics-ecom-tenant-name.azurefd.net**.</span></span>
1. <span data-ttu-id="101df-152">**照合するパターン**の、上のフィールドで、**/\*** と入力します。</span><span class="sxs-lookup"><span data-stu-id="101df-152">Under **Patterns to match**, in the upper field, enter **/\***.</span></span>
1. <span data-ttu-id="101df-153">**工順の詳細**で、**工順タイプ** オプションを**転送**に設定します。</span><span class="sxs-lookup"><span data-stu-id="101df-153">Under **Route Details**, set the **Route type** option to **Forward**.</span></span>
1. <span data-ttu-id="101df-154">**バックエンド プール** フィールドで、**ecom-backend** を選択します。</span><span class="sxs-lookup"><span data-stu-id="101df-154">In the **Backend pool** field, select **ecom-backend**.</span></span>
1. <span data-ttu-id="101df-155">**転送プロトコル** フィールド グループで、**照合要求**オプションを選択します。</span><span class="sxs-lookup"><span data-stu-id="101df-155">In the **Forwarding protocol** field group, select the **Match request** option.</span></span> 
1. <span data-ttu-id="101df-156">**URL Rewrite** オプションを**無効**に設定します。</span><span class="sxs-lookup"><span data-stu-id="101df-156">Set the **URL rewrite** option to **Disabled**.</span></span>
1. <span data-ttu-id="101df-157">**キャッシュ** オプションを**無効**に設定します。</span><span class="sxs-lookup"><span data-stu-id="101df-157">Set the **Caching** option to **Disabled**.</span></span>

<span data-ttu-id="101df-158">Azure Front Door Service でキャッシュ ルールを設定するには、次の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="101df-158">To set up a caching rule in Azure Front Door Service, follow these steps.</span></span>

1. <span data-ttu-id="101df-159">キャッシュ ルールを追加します。</span><span class="sxs-lookup"><span data-stu-id="101df-159">Add a caching rule.</span></span>
1. <span data-ttu-id="101df-160">**名前**フィールドに、**静的**と入力します。</span><span class="sxs-lookup"><span data-stu-id="101df-160">In the **Name** field, enter **statics**.</span></span>
1. <span data-ttu-id="101df-161">**承認済プロトコル** フィールドで、**HTTP と HTTPS** を選択します。</span><span class="sxs-lookup"><span data-stu-id="101df-161">In the **Accepted protocol** field, select **HTTP and HTTPS**.</span></span>
1. <span data-ttu-id="101df-162">**フロントエンド ホスト** フィールドで、**dynamics-ecom-tenant-name.azurefd.net** を入力します。</span><span class="sxs-lookup"><span data-stu-id="101df-162">In the **Frontend hosts** field, enter **dynamics-ecom-tenant-name.azurefd.net**.</span></span>
1. <span data-ttu-id="101df-163">**照合するパターン**の、上のフィールドで、**/\_msdyn365/\_scnr/\*** と入力します。</span><span class="sxs-lookup"><span data-stu-id="101df-163">Under **Patterns to match**, in the upper field, **/\_msdyn365/\_scnr/\***.</span></span>
1. <span data-ttu-id="101df-164">**工順の詳細**で、**工順タイプ** オプションを**転送**に設定します。</span><span class="sxs-lookup"><span data-stu-id="101df-164">Under **Route Details**, set the **Route type** option to **Forward**.</span></span>
1. <span data-ttu-id="101df-165">**バックエンド プール** フィールドで、**ecom-backend** を選択します。</span><span class="sxs-lookup"><span data-stu-id="101df-165">In the **Backend pool** field, select **ecom-backend**.</span></span>
1. <span data-ttu-id="101df-166">**転送プロトコル** フィールド グループで、**照合要求**オプションを選択します。</span><span class="sxs-lookup"><span data-stu-id="101df-166">In the **Forwarding protocol** field group, select the **Match request** option.</span></span>
1. <span data-ttu-id="101df-167">**URL Rewrite** オプションを**無効**に設定します。</span><span class="sxs-lookup"><span data-stu-id="101df-167">Set the **URL rewrite** option to **Disabled**.</span></span>
1. <span data-ttu-id="101df-168">**キャッシュ** オプションを**無効**に設定します。</span><span class="sxs-lookup"><span data-stu-id="101df-168">Set the **Caching** option to **Disabled**.</span></span>
1. <span data-ttu-id="101df-169">**クエリ文字列のキャッシュ動作**フィールドで、**一意の URL ごとキャッシュする**を選択します。</span><span class="sxs-lookup"><span data-stu-id="101df-169">In the **Query string caching behavior** field, select **Cache every unique URL**.</span></span>
1. <span data-ttu-id="101df-170">**動的な圧縮**フィールド グループで、**有効化**オプションを選択します。</span><span class="sxs-lookup"><span data-stu-id="101df-170">In the **Dynamic compression** field group, select the **Enabled** option.</span></span>

<span data-ttu-id="101df-171">次の図は、Azure Front Door Service の**ルールの追加**ダイアログ ボックスを示します。</span><span class="sxs-lookup"><span data-stu-id="101df-171">The following illustration shows the **Add a rule** dialog box in Azure Front Door Service.</span></span>

![ルールの追加ダイアログ ボックス](./media/CDN_CachingRule.png)

<span data-ttu-id="101df-173">この初期コンフィギュレーションを展開した後、Azure Front Door Service のコンフィギュレーションにカスタム ドメインを追加する必要があります。</span><span class="sxs-lookup"><span data-stu-id="101df-173">After this initial configuration is deployed, you must add your custom domain to the configuration for Azure Front Door Service.</span></span> <span data-ttu-id="101df-174">カスタム ドメイン (たとえば、`www.fabrikam.com`) を追加するには、ドメインの正規名 (CNAME) をコンフィギュレーションする必要があります。</span><span class="sxs-lookup"><span data-stu-id="101df-174">To add the custom domain (for example, `www.fabrikam.com`), you must configure a Canonical Name (CNAME) for the domain.</span></span>

<span data-ttu-id="101df-175">次の図は、Azure Front Door Service の**CNAME コンフィギュレーション** ダイアログ ボックスを示します。</span><span class="sxs-lookup"><span data-stu-id="101df-175">The following illustration shows the **CNAME configuration** dialog box in Azure Front Door Service.</span></span>

![CNAME コンフィギュレーション ダイアログ ボックス](./media/CNAME_Configuration.png)

> [!NOTE]
> <span data-ttu-id="101df-177">使用するドメインが既にアクティブで稼働している場合、Azure Front Door Service でこのドメインを有効にしてテストを設定するよう、サポートにお問い合わせください。</span><span class="sxs-lookup"><span data-stu-id="101df-177">If the domain that you will use is already active and live, contact support to enable this domain with Azure Front Door Service to set up a test.</span></span>

<span data-ttu-id="101df-178">Azure Front Door Service を使用して証明書を管理したり、カスタム ドメインに対して独自の証明書を使用したりできます。</span><span class="sxs-lookup"><span data-stu-id="101df-178">You can use Azure Front Door Service to manage the certificate, or you can use your own certificate for the custom domain.</span></span>

<span data-ttu-id="101df-179">次の図は、Azure Front Door Service の**カスタム ドメイン HTTPS** ダイアログ ボックスを示します。</span><span class="sxs-lookup"><span data-stu-id="101df-179">The following illustration shows the **Custom Domain HTTPS** dialog box in Azure Front Door Service.</span></span>

![カスタム ドメイン HTTPS ダイアログ ボックス](./media/Custom_Domain_HTTPS.png)

<span data-ttu-id="101df-181">これにより、CDN を正しくコンフィギュレーションして、コマース サイトで使用できるようになります。</span><span class="sxs-lookup"><span data-stu-id="101df-181">Your CDN should now be correctly configured so that it can be used with your Commerce site.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="101df-182">追加リソース</span><span class="sxs-lookup"><span data-stu-id="101df-182">Additional resources</span></span>

[<span data-ttu-id="101df-183">オンライン ストアの概要</span><span class="sxs-lookup"><span data-stu-id="101df-183">Online store overview</span></span>](online-store-overview.md)

[<span data-ttu-id="101df-184">E コマース サイトの作成</span><span class="sxs-lookup"><span data-stu-id="101df-184">Create an e-Commerce site</span></span>](create-ecommerce-site.md)

[<span data-ttu-id="101df-185">新しい E コマース サイトの配置</span><span class="sxs-lookup"><span data-stu-id="101df-185">Deploy a new e-Commerce site</span></span>](deploy-ecommerce-site.md)

[<span data-ttu-id="101df-186">チャンネルとオンライン サイトの関連付け</span><span class="sxs-lookup"><span data-stu-id="101df-186">Associate an online site with a channel</span></span>](associate-site-online-store.md)

[<span data-ttu-id="101df-187">ドメイン名のコンフィギュレーション</span><span class="sxs-lookup"><span data-stu-id="101df-187">Configure your domain name</span></span>](configure-your-domain-name.md)

[<span data-ttu-id="101df-188">場所に基づく店舗検出の有効化</span><span class="sxs-lookup"><span data-stu-id="101df-188">Enable location-based store detection</span></span>](enable-store-detection.md)

[<span data-ttu-id="101df-189">ユーザー ログイン用のカスタム ページの設定</span><span class="sxs-lookup"><span data-stu-id="101df-189">Set up custom pages for user logins</span></span>](custom-pages-user-logins.md)
