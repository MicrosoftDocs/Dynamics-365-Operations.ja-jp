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
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: brshoo
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: d653b072eca134c765a5db5659b228648fc13c4a
ms.sourcegitcommit: 3fe4d9a33447aa8a62d704fbbf18aeb9cb667baa
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/12/2021
ms.locfileid: "5582722"
---
# <a name="add-support-for-a-content-delivery-network-cdn"></a><span data-ttu-id="68190-103">コンテンツ配信ネットワーク (CDN) のサポートの追加</span><span class="sxs-lookup"><span data-stu-id="68190-103">Add support for a content delivery network (CDN)</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="68190-104">このトピックでは、Microsoft Dynamics 365 Commerce 環境にコンテンツ配信ネットワーク (CDN) を追加する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="68190-104">This topic describes how to add a content delivery network (CDN) to your Microsoft Dynamics 365 Commerce environment.</span></span>

<span data-ttu-id="68190-105">Dynamics 365 Commerce の E コマース環境を設定すると、CDN サービスと連携するようにコンフィギュレーションできます。</span><span class="sxs-lookup"><span data-stu-id="68190-105">When you set up an e-commerce environment in Dynamics 365 Commerce, you can configure it to work with your CDN service.</span></span> 

<span data-ttu-id="68190-106">カスタム ドメインは、E コマース環境のプロビジョニング プロセス中に有効にできます。</span><span class="sxs-lookup"><span data-stu-id="68190-106">Your custom domain can be enabled during the provisioning process for your e-commerce environment.</span></span> <span data-ttu-id="68190-107">また、プロビジョニング プロセスが完了した後に、サービス要求を使用して設定することもできます。</span><span class="sxs-lookup"><span data-stu-id="68190-107">Alternatively, you can use a service request to set it up after the provisioning process is completed.</span></span> <span data-ttu-id="68190-108">E コマース環境のプロビジョニング プロセスでは、環境に関連付けられたホスト名が生成されます。</span><span class="sxs-lookup"><span data-stu-id="68190-108">The provisioning process for the e-commerce environment generates a host name that is associated with the environment.</span></span> <span data-ttu-id="68190-109">\<*e-commerce-tenant-name*\> が環境の名称となっている場合、このホスト名の形式は次のとおりです :</span><span class="sxs-lookup"><span data-stu-id="68190-109">This host name has the following format, where \<*e-commerce-tenant-name*\> is the name of your environment:</span></span>

<span data-ttu-id="68190-110">&lt;e-commerce-tenant-name&gt;.commerce.dynamics.com</span><span class="sxs-lookup"><span data-stu-id="68190-110">&lt;e-commerce-tenant-name&gt;.commerce.dynamics.com</span></span>

<span data-ttu-id="68190-111">プロビジョニング プロセス中に生成されるホスト名またはエンドポイントは、\*.commerce.dynamics.com に対してのみ Secure Sockets Layer (SSL) 証明書をサポートします。</span><span class="sxs-lookup"><span data-stu-id="68190-111">The host name or endpoint that is generated during the provisioning process supports a Secure Sockets Layer (SSL) certificate only for \*.commerce.dynamics.com.</span></span> <span data-ttu-id="68190-112">カスタム ドメインに対する SSL はサポートしません。</span><span class="sxs-lookup"><span data-stu-id="68190-112">It doesn't support SSL for custom domains.</span></span> <span data-ttu-id="68190-113">したがって、CDN のカスタム ドメインの SSL を終了し、CDN からコマースが生成したホスト名またはエンドポイントへトラフィックを転送する必要があります。</span><span class="sxs-lookup"><span data-stu-id="68190-113">Therefore, you must terminate SSL for custom domains in your CDN and forward traffic from the CDN to the host name or endpoint that Commerce generated.</span></span> 

<span data-ttu-id="68190-114">さらに、コマースからの *静的* (JavaScript または カスケード スタイル シート \[CSS\] ファイル) は、コマースが生成したエンドポイント (\*.commerce.dynamics.com) から提供されます。</span><span class="sxs-lookup"><span data-stu-id="68190-114">Additionally, the *statics* (JavaScript or Cascading Style Sheets \[CSS\] files) from Commerce are served from the endpoint that Commerce generated (\*.commerce.dynamics.com).</span></span> <span data-ttu-id="68190-115">静的は、コマースが生成したホスト名またはエンドポイントが CDN の後に配置される場合にのみキャッシュできます。</span><span class="sxs-lookup"><span data-stu-id="68190-115">The statics can be cached only if the host name or endpoint that Commerce generated is put behind the CDN.</span></span>

## <a name="set-up-ssl"></a><span data-ttu-id="68190-116">SSL のセットアップ</span><span class="sxs-lookup"><span data-stu-id="68190-116">Set up SSL</span></span>

<span data-ttu-id="68190-117">SSL が設定され、その静的が確実にキャッシュされるようにするには、環境に対してコマースが生成したホスト名に関連付けられるよう CDN をコンフィギュレーションする必要があります。</span><span class="sxs-lookup"><span data-stu-id="68190-117">To help guarantee that SSL is set up, and that statics are cached, you must configure your CDN so that it is associated with the host name that Commerce generated for your environment.</span></span> <span data-ttu-id="68190-118">また、次のパターンを静的に対してのみキャッシュする必要があります。</span><span class="sxs-lookup"><span data-stu-id="68190-118">You must also cache the following pattern for statics only:</span></span> 

<span data-ttu-id="68190-119">/\_msdyn365/\_scnr/\*</span><span class="sxs-lookup"><span data-stu-id="68190-119">/\_msdyn365/\_scnr/\*</span></span>

<span data-ttu-id="68190-120">指定されたカスタム ドメインを使用してコマース環境をプロビジョニングした後、またはサービス要求を使用して環境のカスタム ドメインを指定した後、カスタム ドメインをコマースが生成したホスト名またはエンドポイントに向けます。</span><span class="sxs-lookup"><span data-stu-id="68190-120">After you provision your Commerce environment with the custom domain that is provided, or after you provide the custom domain for your environment by using a service request, point your custom domain to the host name or endpoint that Commerce generated.</span></span>

<span data-ttu-id="68190-121">前述のように、生成したホスト名またはエンドポイントは、\*.commerce.dynamics.com に対してのみ SSL 証明書をサポートします。</span><span class="sxs-lookup"><span data-stu-id="68190-121">As was previously mentioned, the generated host name or endpoint supports an SSL certificate only for \*.commerce.dynamics.com.</span></span> <span data-ttu-id="68190-122">カスタム ドメインに対する SSL はサポートしません。</span><span class="sxs-lookup"><span data-stu-id="68190-122">It doesn't support SSL for custom domains.</span></span>

## <a name="cdn-services"></a><span data-ttu-id="68190-123">CDN サービス</span><span class="sxs-lookup"><span data-stu-id="68190-123">CDN services</span></span>

<span data-ttu-id="68190-124">任意の CDN サービスは、コマース環境で使用できます。</span><span class="sxs-lookup"><span data-stu-id="68190-124">Any CDN service can be used with a Commerce environment.</span></span> <span data-ttu-id="68190-125">次に 2 つの例を挙げます。</span><span class="sxs-lookup"><span data-stu-id="68190-125">Here are two examples:</span></span>

- <span data-ttu-id="68190-126">**Microsoft Azure Front Door Service** – Azure CDN ソリューション。</span><span class="sxs-lookup"><span data-stu-id="68190-126">**Microsoft Azure Front Door Service** – The Azure CDN solution.</span></span> <span data-ttu-id="68190-127">Azure Front Door Service の詳細については、[Azure Front Door Service のドキュメント](https://docs.microsoft.com/azure/frontdoor/) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="68190-127">For more information about Azure Front Door Service, see [Azure Front Door Service Documentation](https://docs.microsoft.com/azure/frontdoor/).</span></span>
- <span data-ttu-id="68190-128">**Akamai 動的サイト アクセラレータ** – 詳細については、[動的サイト アクセラレータ](https://www.akamai.com/us/en/products/performance/dynamic-site-accelerator.jsp) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="68190-128">**Akamai Dynamic Site Accelerator** – For more information, see [Dynamic Site Accelerator](https://www.akamai.com/us/en/products/performance/dynamic-site-accelerator.jsp).</span></span>

## <a name="cdn-setup"></a><span data-ttu-id="68190-129">CDN の設定</span><span class="sxs-lookup"><span data-stu-id="68190-129">CDN setup</span></span>

<span data-ttu-id="68190-130">CDN の設定プロセスは、次の一般的な手順で構成されています。</span><span class="sxs-lookup"><span data-stu-id="68190-130">The CDN setup process consists of these general steps:</span></span>

1. <span data-ttu-id="68190-131">フロント エンド ホストを追加します。</span><span class="sxs-lookup"><span data-stu-id="68190-131">Add a front-end host.</span></span>
1. <span data-ttu-id="68190-132">バック エンド プールを構成します。</span><span class="sxs-lookup"><span data-stu-id="68190-132">Configure a backend pool.</span></span>
1. <span data-ttu-id="68190-133">ルート指定とキャッシュのルールを設定します。</span><span class="sxs-lookup"><span data-stu-id="68190-133">Set up rules for routing and caching.</span></span>

### <a name="add-a-front-end-host"></a><span data-ttu-id="68190-134">フロント エンド ホストを追加する</span><span class="sxs-lookup"><span data-stu-id="68190-134">Add a front-end host</span></span>

<span data-ttu-id="68190-135">任意の CDN サービスを使用できますが、このトピックの例では、 Azure Front Door Service を使用します。</span><span class="sxs-lookup"><span data-stu-id="68190-135">Any CDN service can be used, but for the example in this topic, Azure Front Door Service is used.</span></span> 

<span data-ttu-id="68190-136">Azure Front Door Service の設定方法の詳細については、[クイックスタート: 高可用性グローバル Web アプリケーションに対する Front Door を作成する](https://docs.microsoft.com/azure/frontdoor/quickstart-create-front-door) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="68190-136">For information about how to set up Azure Front Door Service, see [Quickstart: Create a Front Door for a highly available global web application](https://docs.microsoft.com/azure/frontdoor/quickstart-create-front-door).</span></span>

### <a name="configure-a-backend-pool-in-azure-front-door-service"></a><span data-ttu-id="68190-137">Azure Front Door Service のバック エンド プールを構成する</span><span class="sxs-lookup"><span data-stu-id="68190-137">Configure a backend pool in Azure Front Door Service</span></span>

<span data-ttu-id="68190-138">Azure Front Door Service のバック エンド プールを構成するには、次の手順を実行してください。</span><span class="sxs-lookup"><span data-stu-id="68190-138">To configure a backend pool in Azure Front Door Service, follow these steps.</span></span>

1. <span data-ttu-id="68190-139">**&lt;ecom-tenant-name&gt;.commerce.dynamics.com** を、空のバック エンド ホスト ヘッダーを持つカスタム ホストとして、バック エンド プールに追加します。</span><span class="sxs-lookup"><span data-stu-id="68190-139">Add **&lt;ecom-tenant-name&gt;.commerce.dynamics.com** to a backend pool as a custom host that has an empty backend host header.</span></span>
1. <span data-ttu-id="68190-140">**負荷分散** では、既定値のままにします。</span><span class="sxs-lookup"><span data-stu-id="68190-140">Under **Load balancing**, leave the default values.</span></span>

<span data-ttu-id="68190-141">次の図は、バック エンド ホスト名が入力された Azure Front Door Service の **バックエンドの追加** ダイアログ ボックスを示します。</span><span class="sxs-lookup"><span data-stu-id="68190-141">The following illustration shows the **Add a backend** dialog box in Azure Front Door Service with the backend host name entered.</span></span>

![バックエンド プール ダイアログ ボックスを追加する](./media/CDN_BackendPool.png)

<span data-ttu-id="68190-143">次の図は、既定の負荷分散値が入力された Azure Front Door Service の **バックエンド プール の追加** ダイアログ ボックスを示します。</span><span class="sxs-lookup"><span data-stu-id="68190-143">The following illustration shows the **Add a backend pool** dialog box in Azure Front Door Service with the default load balancing values.</span></span>

![バックエンド プールのダイアログ ボックスを継続して追加する](./media/CDN_BackendPool_2.png)

### <a name="set-up-rules-in-azure-front-door-service"></a><span data-ttu-id="68190-145">Azure Front Door Service でルールを設定する</span><span class="sxs-lookup"><span data-stu-id="68190-145">Set up rules in Azure Front Door Service</span></span>

<span data-ttu-id="68190-146">Azure Front Door Service でルート指定ルールを設定するには、次の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="68190-146">To set up a routing rule in Azure Front Door Service, follow these steps.</span></span>

1. <span data-ttu-id="68190-147">ルート指定ルールを追加します。</span><span class="sxs-lookup"><span data-stu-id="68190-147">Add a routing rule.</span></span>
1. <span data-ttu-id="68190-148">**名前** フィールドに、**既定** と入力します。</span><span class="sxs-lookup"><span data-stu-id="68190-148">In the **Name** field, enter **default**.</span></span>
1. <span data-ttu-id="68190-149">**承認済プロトコル** フィールドで、**HTTP と HTTPS** を選択します。</span><span class="sxs-lookup"><span data-stu-id="68190-149">In the **Accepted protocol** field, select **HTTP and HTTPS**.</span></span>
1. <span data-ttu-id="68190-150">**フロントエンド ホスト** フィールドで、**dynamics-ecom-tenant-name.azurefd.net** を入力します。</span><span class="sxs-lookup"><span data-stu-id="68190-150">In the **Frontend hosts** field, enter **dynamics-ecom-tenant-name.azurefd.net**.</span></span>
1. <span data-ttu-id="68190-151">**照合するパターン** の、上のフィールドで、**/\*** と入力します。</span><span class="sxs-lookup"><span data-stu-id="68190-151">Under **Patterns to match**, in the upper field, enter **/\***.</span></span>
1. <span data-ttu-id="68190-152">**工順の詳細** で、**工順タイプ** オプションを **転送** に設定します。</span><span class="sxs-lookup"><span data-stu-id="68190-152">Under **Route Details**, set the **Route type** option to **Forward**.</span></span>
1. <span data-ttu-id="68190-153">**バックエンド プール** フィールドで、**ecom-backend** を選択します。</span><span class="sxs-lookup"><span data-stu-id="68190-153">In the **Backend pool** field, select **ecom-backend**.</span></span>
1. <span data-ttu-id="68190-154">**転送プロトコル** フィールド グループで、**照合要求** オプションを選択します。</span><span class="sxs-lookup"><span data-stu-id="68190-154">In the **Forwarding protocol** field group, select the **Match request** option.</span></span> 
1. <span data-ttu-id="68190-155">**URL Rewrite** オプションを **無効** に設定します。</span><span class="sxs-lookup"><span data-stu-id="68190-155">Set the **URL rewrite** option to **Disabled**.</span></span>
1. <span data-ttu-id="68190-156">**キャッシュ** オプションを **無効** に設定します。</span><span class="sxs-lookup"><span data-stu-id="68190-156">Set the **Caching** option to **Disabled**.</span></span>

<span data-ttu-id="68190-157">Azure Front Door Service でキャッシュ ルールを設定するには、次の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="68190-157">To set up a caching rule in Azure Front Door Service, follow these steps.</span></span>

1. <span data-ttu-id="68190-158">キャッシュ ルールを追加します。</span><span class="sxs-lookup"><span data-stu-id="68190-158">Add a caching rule.</span></span>
1. <span data-ttu-id="68190-159">**名前** フィールドに、**静的** と入力します。</span><span class="sxs-lookup"><span data-stu-id="68190-159">In the **Name** field, enter **statics**.</span></span>
1. <span data-ttu-id="68190-160">**承認済プロトコル** フィールドで、**HTTP と HTTPS** を選択します。</span><span class="sxs-lookup"><span data-stu-id="68190-160">In the **Accepted protocol** field, select **HTTP and HTTPS**.</span></span>
1. <span data-ttu-id="68190-161">**フロントエンド ホスト** フィールドで、**dynamics-ecom-tenant-name.azurefd.net** を入力します。</span><span class="sxs-lookup"><span data-stu-id="68190-161">In the **Frontend hosts** field, enter **dynamics-ecom-tenant-name.azurefd.net**.</span></span>
1. <span data-ttu-id="68190-162">**照合するパターン** の、上のフィールドで、**/\_msdyn365/\_scnr/\*** と入力します。</span><span class="sxs-lookup"><span data-stu-id="68190-162">Under **Patterns to match**, in the upper field, **/\_msdyn365/\_scnr/\***.</span></span>
1. <span data-ttu-id="68190-163">**工順の詳細** で、**工順タイプ** オプションを **転送** に設定します。</span><span class="sxs-lookup"><span data-stu-id="68190-163">Under **Route Details**, set the **Route type** option to **Forward**.</span></span>
1. <span data-ttu-id="68190-164">**バックエンド プール** フィールドで、**ecom-backend** を選択します。</span><span class="sxs-lookup"><span data-stu-id="68190-164">In the **Backend pool** field, select **ecom-backend**.</span></span>
1. <span data-ttu-id="68190-165">**転送プロトコル** フィールド グループで、**照合要求** オプションを選択します。</span><span class="sxs-lookup"><span data-stu-id="68190-165">In the **Forwarding protocol** field group, select the **Match request** option.</span></span>
1. <span data-ttu-id="68190-166">**URL Rewrite** オプションを **無効** に設定します。</span><span class="sxs-lookup"><span data-stu-id="68190-166">Set the **URL rewrite** option to **Disabled**.</span></span>
1. <span data-ttu-id="68190-167">**キャッシュ** オプションを **無効** に設定します。</span><span class="sxs-lookup"><span data-stu-id="68190-167">Set the **Caching** option to **Disabled**.</span></span>
1. <span data-ttu-id="68190-168">**クエリ文字列のキャッシュ動作** フィールドで、**一意の URL ごとキャッシュする** を選択します。</span><span class="sxs-lookup"><span data-stu-id="68190-168">In the **Query string caching behavior** field, select **Cache every unique URL**.</span></span>
1. <span data-ttu-id="68190-169">**動的な圧縮** フィールド グループで、**有効化** オプションを選択します。</span><span class="sxs-lookup"><span data-stu-id="68190-169">In the **Dynamic compression** field group, select the **Enabled** option.</span></span>

<span data-ttu-id="68190-170">次の図は、Azure Front Door Service の **ルールの追加** ダイアログ ボックスを示します。</span><span class="sxs-lookup"><span data-stu-id="68190-170">The following illustration shows the **Add a rule** dialog box in Azure Front Door Service.</span></span>

![ルールの追加ダイアログ ボックス](./media/CDN_CachingRule.png)

> [!WARNING]
> <span data-ttu-id="68190-172">使用するドメインが既に有効化されている場合は、[Microsoft Dynamics Lifecycle Services](https://lcs.dynamics.com/) の **サポート** タイルからサポートチケットを作成して、次の手順についてのサポートを受けてください。</span><span class="sxs-lookup"><span data-stu-id="68190-172">If the domain that you will use is already active and live, create a support ticket from the **Support** tile in [Microsoft Dynamics Lifecycle Services](https://lcs.dynamics.com/) to get assistance for your next steps.</span></span> <span data-ttu-id="68190-173">詳細については、[Finance and Operations アプまたは Lifecycle Services (LCS) のサポートを得る](../fin-ops-core/dev-itpro/lifecycle-services/lcs-support.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="68190-173">For more information, see [Get support for Finance and Operations apps or Lifecycle Services (LCS)](../fin-ops-core/dev-itpro/lifecycle-services/lcs-support.md).</span></span>

<span data-ttu-id="68190-174">ご利用のドメインが新しく、かつ既存のドメインではない場合は、Azure Front Door Service の構成にカスタム ドメインを追加することができます。</span><span class="sxs-lookup"><span data-stu-id="68190-174">If your domain is new and is not a pre-existing live domain, you can add your custom domain to the configuration for Azure Front Door Service.</span></span> <span data-ttu-id="68190-175">これにより、web トラフィックが Azure Front Door インスタンスを介してサイトに誘導されるようになります。</span><span class="sxs-lookup"><span data-stu-id="68190-175">This will enable web traffic to direct to your site via the Azure Front Door instance.</span></span> <span data-ttu-id="68190-176">カスタム ドメイン (たとえば、`www.fabrikam.com`) を追加するには、ドメインの正規名 (CNAME) をコンフィギュレーションする必要があります。</span><span class="sxs-lookup"><span data-stu-id="68190-176">To add the custom domain (for example, `www.fabrikam.com`), you must configure a Canonical Name (CNAME) for the domain.</span></span>

<span data-ttu-id="68190-177">次の図は、Azure Front Door Service の **CNAME コンフィギュレーション** ダイアログ ボックスを示します。</span><span class="sxs-lookup"><span data-stu-id="68190-177">The following illustration shows the **CNAME configuration** dialog box in Azure Front Door Service.</span></span>

![CNAME コンフィギュレーション ダイアログ ボックス](./media/CNAME_Configuration.png)

<span data-ttu-id="68190-179">Azure Front Door Service を使用して証明書を管理したり、カスタム ドメインに対して独自の証明書を使用したりできます。</span><span class="sxs-lookup"><span data-stu-id="68190-179">You can use Azure Front Door Service to manage the certificate, or you can use your own certificate for the custom domain.</span></span>

<span data-ttu-id="68190-180">次の図は、Azure Front Door Service の **カスタム ドメイン HTTPS** ダイアログ ボックスを示します。</span><span class="sxs-lookup"><span data-stu-id="68190-180">The following illustration shows the **Custom Domain HTTPS** dialog box in Azure Front Door Service.</span></span>

![カスタム ドメイン HTTPS ダイアログ ボックス](./media/Custom_Domain_HTTPS.png)

<span data-ttu-id="68190-182">Azure Front Door にカスタムドメインを追加する方法の詳細については、[フロント ドアにカスタム ドメインを追加する](https://docs.microsoft.com/azure/frontdoor/front-door-custom-domain)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="68190-182">For detailed instructions on adding a custom domain to your Azure Front Door, see [Add a custom domain to your Front Door](https://docs.microsoft.com/azure/frontdoor/front-door-custom-domain).</span></span>

<span data-ttu-id="68190-183">これにより、CDN を正しくコンフィギュレーションして、コマース サイトで使用できるようになります。</span><span class="sxs-lookup"><span data-stu-id="68190-183">Your CDN should now be correctly configured so that it can be used with your Commerce site.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="68190-184">追加リソース</span><span class="sxs-lookup"><span data-stu-id="68190-184">Additional resources</span></span>

[<span data-ttu-id="68190-185">コンテンツ配信ネットワークの実装オプション</span><span class="sxs-lookup"><span data-stu-id="68190-185">Content delivery network implementation options</span></span>](cdn-options.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
