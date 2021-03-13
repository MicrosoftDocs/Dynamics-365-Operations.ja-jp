---
title: 電子請求書アドオン管理コンポーネント
description: このトピックでは、電子請求書アドオンの管理に関連するコンポーネントについて説明します。
author: gionoder
manager: AnnBe
ms.date: 01/28/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.custom: 97423
ms.assetid: ''
ms.search.region: Global
ms.author: janeaug
ms.search.validFrom: 2020-07-08
ms.dyn365.ops.version: AX 10.0.12
ms.openlocfilehash: 6f630ebb694217c3bd52378a649933a670c090f2
ms.sourcegitcommit: e88c96d1cb817a22db81856cadb563c095ab2671
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/02/2021
ms.locfileid: "5104405"
---
# <a name="electronic-invoicing-add-on-administration-components"></a><span data-ttu-id="c8722-103">電子請求書アドオン管理コンポーネント</span><span class="sxs-lookup"><span data-stu-id="c8722-103">Electronic invoicing add-on administration components</span></span>

[!include [banner](../includes/banner.md)]
[!include [banner](../includes/preview-banner.md)]

<span data-ttu-id="c8722-104">このトピックでは、電子請求書アドオンの管理に関連するコンポーネントについて説明します。</span><span class="sxs-lookup"><span data-stu-id="c8722-104">This topic provides information about the components that are related to administration of the Electronic invoicing add-on.</span></span> <span data-ttu-id="c8722-105">また、電子請求アドオン サービスの設定方法についても説明しています。</span><span class="sxs-lookup"><span data-stu-id="c8722-105">It also provides information about how to configure the Electronic invoicing add-on service.</span></span>

## <a name="azure"></a><span data-ttu-id="c8722-106">Azure</span><span class="sxs-lookup"><span data-stu-id="c8722-106">Azure</span></span>

<span data-ttu-id="c8722-107">Microsoft Azure を使用して、key vault およびストレージ アカウントのシークレットを作成します。</span><span class="sxs-lookup"><span data-stu-id="c8722-107">Use Microsoft Azure to create the secrets for the key vault and storage account.</span></span> <span data-ttu-id="c8722-108">このシークレットを、電子請求書アドオンの構成で使用します。</span><span class="sxs-lookup"><span data-stu-id="c8722-108">Then use the secrets in the configuration of the Electronic invoicing add-on.</span></span>

## <a name="lifecycle-services"></a><span data-ttu-id="c8722-109">Lifecycle Services</span><span class="sxs-lookup"><span data-stu-id="c8722-109">Lifecycle Services</span></span>

<span data-ttu-id="c8722-110">Microsoft Dynamics Lifecycle Services (LCS) を使用して、LCS デプロイ プロジェクトのマイクロサービスに対するアドオンを有効にします。</span><span class="sxs-lookup"><span data-stu-id="c8722-110">Use Microsoft Dynamics Lifecycle Services (LCS) to enable the add-on for the microservices for your LCS deployment project.</span></span>

<span data-ttu-id="c8722-111">LCS で、**プレビュー機能管理** タイルを選択し、**電子請求サービス機能** 機能を有効化します。</span><span class="sxs-lookup"><span data-stu-id="c8722-111">In LCS, select the **Preview feature management** tile, and then turn on the **e-Invoicing Service** feature.</span></span>

## <a name="regulatory-configuration-services"></a><span data-ttu-id="c8722-112">Regulatory Configuration Services</span><span class="sxs-lookup"><span data-stu-id="c8722-112">Regulatory Configuration Services</span></span>

<span data-ttu-id="c8722-113">Dynamics 365 Regulatory Configuration Services (RCS) は、電子請求書のアドオンの構成に使用します。</span><span class="sxs-lookup"><span data-stu-id="c8722-113">Dynamics 365 Regulatory Configuration Services (RCS) is the interface that is used to configure the Electronic invoicing add-on.</span></span> <span data-ttu-id="c8722-114">環境や電子請求書機能などのリソースは、RCSで作成、管理、ホストされます。</span><span class="sxs-lookup"><span data-stu-id="c8722-114">Resources such as environments and electronic invoicing features are created, maintained, and hosted in RCS.</span></span> <span data-ttu-id="c8722-115">リソースの準備が整うと、電子請求アドオン サービスにリソースが公開されます。</span><span class="sxs-lookup"><span data-stu-id="c8722-115">When the resources are ready, they are published to the Electronic invoicing add-on service.</span></span>

<span data-ttu-id="c8722-116">RCS の詳細については、[Regulatory Configuration Services (RCS) - グローバリゼーション機能](rcs-globalization-feature.md)を参照してください</span><span class="sxs-lookup"><span data-stu-id="c8722-116">For more information about RCS, see [Regulatory Configuration Services (RCS) - Globalization features](rcs-globalization-feature.md)</span></span>

### <a name="integration-with-the-electronic-invoicing-add-on"></a><span data-ttu-id="c8722-117">電子請求書アドオンとの統合</span><span class="sxs-lookup"><span data-stu-id="c8722-117">Integration with the Electronic invoicing add-on</span></span>

<span data-ttu-id="c8722-118">RCS を使用して電子請求書を構成するには、電子請求アドオンとの通信を許可するために、RCS を構成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="c8722-118">Before you can use RCS to configure electronic invoices, you must configure RCS to allow for communication with the Electronic invoicing add-on.</span></span> <span data-ttu-id="c8722-119">**電子申告パラメーター** ページの **電子請求書アドオン** タブでこの構成を完了します。</span><span class="sxs-lookup"><span data-stu-id="c8722-119">You complete this configuration on the **Electronic invoicing add-on** tab of the **Electronic reporting parameters** page.</span></span>

#### <a name="service-endpoint"></a><span data-ttu-id="c8722-120">サービス エンドポイント</span><span class="sxs-lookup"><span data-stu-id="c8722-120">Service endpoint</span></span>

<span data-ttu-id="c8722-121">電子請求アドオン エンドポイントの URL は、Azure の地理的条件によって異なる場合があります。</span><span class="sxs-lookup"><span data-stu-id="c8722-121">The URL of the Electronic invoicing add-on endpoint can vary according to the Azure datacenter geography.</span></span> <span data-ttu-id="c8722-122">次の表に、地域ごとの可用性の一覧を示します。</span><span class="sxs-lookup"><span data-stu-id="c8722-122">The following table lists the availability per region:</span></span>

| <span data-ttu-id="c8722-123">Azure データ センターの地域</span><span class="sxs-lookup"><span data-stu-id="c8722-123">Azure datacenter geography</span></span> | <span data-ttu-id="c8722-124">サービス エンドポイント URL</span><span class="sxs-lookup"><span data-stu-id="c8722-124">Service endpoint URL</span></span>                                                       |
|----------------------------|----------------------------------------------------------------------------|
| <span data-ttu-id="c8722-125">米国東部</span><span class="sxs-lookup"><span data-stu-id="c8722-125">East US</span></span>                    | `https://electronicinvoicing.eus-il301.gateway.prod.island.powerapps.com/` |
| <span data-ttu-id="c8722-126">米国西部</span><span class="sxs-lookup"><span data-stu-id="c8722-126">West US</span></span>                    | `https://electronicinvoicing.wus-il301.gateway.prod.island.powerapps.com/` |
| <span data-ttu-id="c8722-127">北ヨーロッパ</span><span class="sxs-lookup"><span data-stu-id="c8722-127">North EU</span></span>                   | `https://electronicinvoicing.neu-il301.gateway.prod.island.powerapps.com/` |
| <span data-ttu-id="c8722-128">西ヨーロッパ</span><span class="sxs-lookup"><span data-stu-id="c8722-128">West EU</span></span>                    | `https://electronicinvoicing.weu-il301.gateway.prod.island.powerapps.com/` |

#### <a name="application-id"></a><span data-ttu-id="c8722-129">アプリケーション ID</span><span class="sxs-lookup"><span data-stu-id="c8722-129">Application ID</span></span>

<span data-ttu-id="c8722-130">アプリケーション ID は、電子請求アドオン アプリケーションの ID を意味します。</span><span class="sxs-lookup"><span data-stu-id="c8722-130">The application ID is the ID of the Electronic invoicing add-on application.</span></span> <span data-ttu-id="c8722-131">この例では、値が **0cdb527f-a8d1-4bf8-9436-b352c68682b2** に固定されています。</span><span class="sxs-lookup"><span data-stu-id="c8722-131">In this case, the value is fixed: **0cdb527f-a8d1-4bf8-9436-b352c68682b2**.</span></span>

#### <a name="lcs-environment-id"></a><span data-ttu-id="c8722-132">LCS 環境の ID</span><span class="sxs-lookup"><span data-stu-id="c8722-132">LCS environment ID</span></span>

<span data-ttu-id="c8722-133">LCS 環境の ID は、組織の LCS サブスクリプションの ID を意味します。</span><span class="sxs-lookup"><span data-stu-id="c8722-133">The LCS environment ID is the ID of your organization's LCS subscription.</span></span>

### <a name="service-environments"></a><span data-ttu-id="c8722-134">サービス環境</span><span class="sxs-lookup"><span data-stu-id="c8722-134">Service environments</span></span>

<span data-ttu-id="c8722-135">サービス環境は、電子請求書アドオンにおける電子請求機能の実行をサポートするために作成される論理パーティションです。</span><span class="sxs-lookup"><span data-stu-id="c8722-135">Service environments are logical partitions that are created to support execution of the electronic invoicing features in the Electronic invoicing add-on.</span></span> <span data-ttu-id="c8722-136">セキュリティのシークレットや電子証明書、ガバナンス (アクセス権限) は、サービス環境レベルで構成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="c8722-136">The security secrets and digital certificates, and the governance (that is, access permissions), must be configured at the service environment level.</span></span>

<span data-ttu-id="c8722-137">顧客は、必要な数のサービス環境を作成できます。</span><span class="sxs-lookup"><span data-stu-id="c8722-137">Customers can create as many service environments as they want.</span></span> <span data-ttu-id="c8722-138">顧客が作成するサービス環境は互いに依存するものではありません。</span><span class="sxs-lookup"><span data-stu-id="c8722-138">All the service environments that a customer creates are independent of each other.</span></span>

<span data-ttu-id="c8722-139">サービス環境は、RCS で作成・管理する必要があります。</span><span class="sxs-lookup"><span data-stu-id="c8722-139">Service environments must be created and maintained in RCS.</span></span> <span data-ttu-id="c8722-140">サービス環境の準備が整うと、電子請求アドオンにリソースが公開されます。</span><span class="sxs-lookup"><span data-stu-id="c8722-140">When the service environments are ready, they must be published to the Electronic invoicing add-on.</span></span>

#### <a name="service-environment-status"></a><span data-ttu-id="c8722-141">サービス環境の状態</span><span class="sxs-lookup"><span data-stu-id="c8722-141">Service environment status</span></span>

<span data-ttu-id="c8722-142">サービス環境は、状態を介して管理できます。</span><span class="sxs-lookup"><span data-stu-id="c8722-142">Service environments can be managed through status.</span></span> <span data-ttu-id="c8722-143">想定できるオプションは次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="c8722-143">The possible options are:</span></span>

- <span data-ttu-id="c8722-144">**未公開** - 環境は作成済ですが、まだ公開されていません。</span><span class="sxs-lookup"><span data-stu-id="c8722-144">**Not published** – The environment has been created, but it hasn't yet been published.</span></span>
- <span data-ttu-id="c8722-145">**公開済** - 環境が電子請求書アドオンに公開されました。</span><span class="sxs-lookup"><span data-stu-id="c8722-145">**Published** – The environment has been published to the Electronic invoicing add-on.</span></span>
- <span data-ttu-id="c8722-146">**変更済** - 公開された環境の属性は変更されましたが、まだ公開されていません。</span><span class="sxs-lookup"><span data-stu-id="c8722-146">**Changed** – The attributes of a published environment have been changed, but the changes haven't yet been published.</span></span>

#### <a name="customer-secrets"></a><span data-ttu-id="c8722-147">顧客のシークレット</span><span class="sxs-lookup"><span data-stu-id="c8722-147">Customer secrets</span></span>

<span data-ttu-id="c8722-148">電子請求アドオンサービスは、企業が所有する Azure リソースにすべてのビジネス データを保存する役割を果たします。</span><span class="sxs-lookup"><span data-stu-id="c8722-148">The Electronic invoicing add-on service is responsible for storing all your business data in the Azure resources that your company owns.</span></span> <span data-ttu-id="c8722-149">サービスが正常に動作し、電子請求書アドオンで必要とされ、生成されるすべてのビジネス データにアクセスできるようにするためには、2 つの主要な Azure リソースを作成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="c8722-149">To ensure that the service works correctly, and that all the business data that is required for and generated by the Electronic invoicing add-on is accessed only by the add-on, you must create two main Azure resources:</span></span>

- <span data-ttu-id="c8722-150">電子請求書を格納する Azure ストレージ アカウント (Blob ストレージ)</span><span class="sxs-lookup"><span data-stu-id="c8722-150">An Azure storage account (Blob storage) that will store electronic invoices</span></span>
- <span data-ttu-id="c8722-151">証明書とストレージ アカウントの Uniform Resource Identifier (URI) を格納する Azure key vault</span><span class="sxs-lookup"><span data-stu-id="c8722-151">An Azure key vault that will store certificates and the uniform resource identifier (URI) of the storage account</span></span>

> [!NOTE]
> <span data-ttu-id="c8722-152">電子請求書作成アドオンで使用するには、専用の Key Vault のリソースと顧客の Blob ストレージを特別に割り当てる必要があります。</span><span class="sxs-lookup"><span data-stu-id="c8722-152">A dedicated key vault and customer storage account must be allocated specifically for use with the Electronic invoicing add-on.</span></span>

<span data-ttu-id="c8722-153">詳細については、[Azure ストレージ アカウント Key Vault リソースの作成](e-invoicing-create-azure-storage-account-key-vault.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="c8722-153">For more information, see [Create an Azure storage account and a key vault](e-invoicing-create-azure-storage-account-key-vault.md).</span></span>

#### <a name="users"></a><span data-ttu-id="c8722-154">ユーザー</span><span class="sxs-lookup"><span data-stu-id="c8722-154">Users</span></span>

<span data-ttu-id="c8722-155">各サービス環境では、電子請求書アドオンで Dynamics 365 Finance と Dynamics 365 Supply Chain Management から接続できるユーザーの一覧を作成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="c8722-155">Each service environment must list the users who can connect from Dynamics 365 Finance and Dynamics 365 Supply Chain Management in the Electronic invoicing add-on.</span></span>

#### <a name="publication"></a><span data-ttu-id="c8722-156">公開</span><span class="sxs-lookup"><span data-stu-id="c8722-156">Publication</span></span>

<span data-ttu-id="c8722-157">サービス環境は、電子請求書アドオンに公開した後で使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="c8722-157">Service environments must be published to the Electronic invoicing add-on before they can be used.</span></span> <span data-ttu-id="c8722-158">公開された環境のみが、 Finance および Supply Chain Management からアクセスできます。</span><span class="sxs-lookup"><span data-stu-id="c8722-158">Only published environments can be accessed by Finance and Supply Chain Management.</span></span> <span data-ttu-id="c8722-159">また、電子請求書発行サービスで属性の更新が有効になる前に、サービス環境を公開する必要があります。</span><span class="sxs-lookup"><span data-stu-id="c8722-159">Additionally, a service environment must be published before any updates to its attributes will take effect on the electronic invoicing service.</span></span>

### <a name="connected-applications"></a><span data-ttu-id="c8722-160">接続した申請</span><span class="sxs-lookup"><span data-stu-id="c8722-160">Connected applications</span></span>

<span data-ttu-id="c8722-161">接続されたアプリケーションは、RCS によって利用できる Finance および Supply Chain Management のインスタンスです。</span><span class="sxs-lookup"><span data-stu-id="c8722-161">Connected applications are the instances of Finance and Supply Chain Management that you might want to reach through RCS.</span></span> <span data-ttu-id="c8722-162">アプリケーションの URL とそのテナントに加え、接続されたアプリケーションには、RCS が環境に接続できる資格情報が含まれています。</span><span class="sxs-lookup"><span data-stu-id="c8722-162">Besides the application URL and its tenant, a connected application contains the credentials that enable RCS to connect to the environment.</span></span>

<span data-ttu-id="c8722-163">接続されたアプリケーションを通じて、Finance および Supply Chain Management の電子請求書機能の一部を構成することで、電子請求書の機能全体を機能させることができます。</span><span class="sxs-lookup"><span data-stu-id="c8722-163">Through the connected applications, you can configure part of the electronic invoicing feature in Finance and Supply Chain Management to make the whole electronic invoicing feature work.</span></span>

## <a name="finance-and-supply-chain-management"></a><span data-ttu-id="c8722-164">Finance および Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="c8722-164">Finance and Supply Chain Management</span></span>

### <a name="integration-with-electronic-invoicing-add-on"></a><span data-ttu-id="c8722-165">電子請求書アドオンとの統合</span><span class="sxs-lookup"><span data-stu-id="c8722-165">Integration with Electronic invoicing add-on</span></span>

<span data-ttu-id="c8722-166">Finance および Supply Chain Management を使用して電子請求書アドオンを介した電子請求書を発行するには、サービスと通信ができるようにアドオンを構成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="c8722-166">Before you can use Finance and Supply Chain Management to issue electronic invoices through the Electronic invoicing add-on, the add-on must be configured to allow for communication with the service.</span></span>

#### <a name="electronic-invoicing-add-on-integration-feature"></a><span data-ttu-id="c8722-167">電子請求書のアドオン統合機能</span><span class="sxs-lookup"><span data-stu-id="c8722-167">Electronic invoicing add-on integration feature</span></span>

<span data-ttu-id="c8722-168">Finance および Supply Chain Management と電子請求アドオンの間の通信を有効にするには、**機能管理** ワークスペースで **電子請求アドオンの統合** 機能を有効にする必要 があります。</span><span class="sxs-lookup"><span data-stu-id="c8722-168">To enable communication between Finance and Supply Chain Management and the Electronic invoicing add-on, you must turn on the **Electronic Invoicing add-on integration** feature in the **Feature management** workspace.</span></span>

#### <a name="service-endpoint"></a><span data-ttu-id="c8722-169">サービス エンドポイント</span><span class="sxs-lookup"><span data-stu-id="c8722-169">Service endpoint</span></span>

<span data-ttu-id="c8722-170">サービス エンドポイントは、電子請求書アドオンが位置する URL です。</span><span class="sxs-lookup"><span data-stu-id="c8722-170">The service endpoint is the URL where the Electronic invoicing add-on is located.</span></span> <span data-ttu-id="c8722-171">サービスとの通信を可能にするには、電子請求書を発行する前にサービスのエンドポイントを Finance と Supply Chain Management に構成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="c8722-171">Before electronic invoices can be issued, the service endpoint must be configured in Finance and Supply Chain Management to allow for communication with the service.</span></span>

<span data-ttu-id="c8722-172">サービス エンドポイントを構成するには、**組織管理 \> 設定 \> 電子ドキュメント パラメーター** に移動し、**送信サービス** タブの **電子請求アドオン URL** フィールドに、**サービス エンドポイント** のセクションで説明されている表に従って URL を入力します。</span><span class="sxs-lookup"><span data-stu-id="c8722-172">To configure the service endpoint, go to **Organization administration \> Setup \> Electronic document parameter**, and then, on the **Submission services** tab, in the **Electronic invoicing add-on URL** field, enter the URL as described in the table described in section **Service endpoint**.</span></span>

#### <a name="environments"></a><span data-ttu-id="c8722-173">環境</span><span class="sxs-lookup"><span data-stu-id="c8722-173">Environments</span></span>

<span data-ttu-id="c8722-174">Finance および Supply Chain Management に入力された環境名は、RCS で作成され、電子請求書アドオンに公開されている環境名を指します。</span><span class="sxs-lookup"><span data-stu-id="c8722-174">The environment name that is entered in Finance and Supply Chain Management refers to the name of the environment that is created in RCS and published to the Electronic invoicing add-on.</span></span>

<span data-ttu-id="c8722-175">環境は、電子請求書を発行するすべての要求に、電子請求アドオンがどの電子請求機能が要求を処理する必要があるかどうかを決定できる環境を含むように、**電子ドキュメント パラメータ** ページの **送信サービス** タブで構成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="c8722-175">The environment must be configured on the **Submission services** tab of the **Electronic document parameter** page, so that every request to issue electronic invoices contains the environment where the Electronic invoicing add-on can determine which electronic invoicing feature must process the request.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="c8722-176">追加リソース</span><span class="sxs-lookup"><span data-stu-id="c8722-176">Additional resources</span></span>

- [<span data-ttu-id="c8722-177">RCS で電子請求書を構成する</span><span class="sxs-lookup"><span data-stu-id="c8722-177">Configure electronic invoices in RCS</span></span>](e-invoicing-configuration-rcs.md)
- [<span data-ttu-id="c8722-178">Finance および Supply Chain Management で電子請求書を発行する</span><span class="sxs-lookup"><span data-stu-id="c8722-178">Issue electronic invoices in Finance and Supply Chain Management</span></span>](e-invoicing-issuing-electronic-invoices-finance-supply-chain-management.md)
