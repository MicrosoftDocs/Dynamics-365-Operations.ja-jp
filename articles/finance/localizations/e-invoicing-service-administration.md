---
title: 電子請求管理コンポーネント
description: このトピックでは、電子請求の管理に関連するコンポーネントについて説明します。
author: gionoder
ms.date: 04/29/2021
ms.topic: article
ms.prod: ''
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
ms.openlocfilehash: 081d23c85d3555210b54597920a49e800ffe284b
ms.sourcegitcommit: 35fdcc6501e099c54a58583b1e3aba16f02a5ccc
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/04/2021
ms.locfileid: "5980926"
---
# <a name="electronic-invoicing-administration-components"></a><span data-ttu-id="0d1de-103">電子請求管理コンポーネント</span><span class="sxs-lookup"><span data-stu-id="0d1de-103">Electronic invoicing administration components</span></span>

[!include [banner](../includes/banner.md)]


<span data-ttu-id="0d1de-104">このトピックでは、電子請求の管理に関連するコンポーネントについて説明します。</span><span class="sxs-lookup"><span data-stu-id="0d1de-104">This topic provides information about the components that are related to administration of Electronic invoicing.</span></span> <span data-ttu-id="0d1de-105">また、電子請求サービスの設定方法についても説明しています。</span><span class="sxs-lookup"><span data-stu-id="0d1de-105">It also provides information about how to configure the Electronic invoicing service.</span></span>

## <a name="azure"></a><span data-ttu-id="0d1de-106">Azure</span><span class="sxs-lookup"><span data-stu-id="0d1de-106">Azure</span></span>

<span data-ttu-id="0d1de-107">Microsoft Azure を使用して、Key Vault およびストレージ アカウントのシークレットを作成します。</span><span class="sxs-lookup"><span data-stu-id="0d1de-107">Use Microsoft Azure to create the secrets for the Key Vault and storage account.</span></span> <span data-ttu-id="0d1de-108">このシークレットを、電子請求の構成で使用します。</span><span class="sxs-lookup"><span data-stu-id="0d1de-108">Then use the secrets in the configuration of Electronic invoicing.</span></span>

## <a name="lifecycle-services"></a><span data-ttu-id="0d1de-109">Lifecycle Services</span><span class="sxs-lookup"><span data-stu-id="0d1de-109">Lifecycle Services</span></span>

<span data-ttu-id="0d1de-110">Microsoft Dynamics Lifecycle Services (LCS) を使用して、LCS デプロイ プロジェクトのマイクロサービスを有効にします。</span><span class="sxs-lookup"><span data-stu-id="0d1de-110">Use Microsoft Dynamics Lifecycle Services (LCS) to enable the microservices for your LCS deployment project.</span></span>

> [!NOTE]
> <span data-ttu-id="0d1de-111">LCS にマイクロサービスをインストールするには、少なくとも Tier 2 以上の仮想マシンが必要です。</span><span class="sxs-lookup"><span data-stu-id="0d1de-111">The installation of the microservice in LCS requires at least a Tier 2 virtual machine.</span></span> <span data-ttu-id="0d1de-112">環境計画に関する詳細については、[環境計画](../../fin-ops-core/fin-ops/imp-lifecycle/environment-planning.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="0d1de-112">For more information about environment planning, see [Environment planning](../../fin-ops-core/fin-ops/imp-lifecycle/environment-planning.md).</span></span>
 

## <a name="regulatory-configuration-services"></a><span data-ttu-id="0d1de-113">Regulatory Configuration Services</span><span class="sxs-lookup"><span data-stu-id="0d1de-113">Regulatory Configuration Services</span></span>

<span data-ttu-id="0d1de-114">Dynamics 365 Regulatory Configuration Services (RCS) は、電子請求の構成に使用します。</span><span class="sxs-lookup"><span data-stu-id="0d1de-114">Dynamics 365 Regulatory Configuration Services (RCS) is the interface that is used to configure Electronic invoicing.</span></span> <span data-ttu-id="0d1de-115">環境や電子請求書機能などのリソースは、RCSで作成、管理、ホストされます。</span><span class="sxs-lookup"><span data-stu-id="0d1de-115">Resources such as environments and electronic invoicing features are created, maintained, and hosted in RCS.</span></span> <span data-ttu-id="0d1de-116">リソースの準備が整うと、電子請求サービスにリソースが公開されます。</span><span class="sxs-lookup"><span data-stu-id="0d1de-116">When the resources are ready, they are published to Electronic invoicing service.</span></span>

<span data-ttu-id="0d1de-117">RCS の登録については、[Regulatory services](https://marketing.configure.global.dynamics.com/) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="0d1de-117">For RCS sign-up, see [Regulatory services](https://marketing.configure.global.dynamics.com/).</span></span>

<span data-ttu-id="0d1de-118">RCS の詳細については、[Regulatory Configuration Services (RCS) - グローバリゼーション機能](rcs-globalization-feature.md)を参照してください</span><span class="sxs-lookup"><span data-stu-id="0d1de-118">For more information about RCS, see [Regulatory Configuration Services (RCS) - Globalization features](rcs-globalization-feature.md)</span></span>

### <a name="integration-with-electronic-invoicing"></a><span data-ttu-id="0d1de-119">電子請求との統合</span><span class="sxs-lookup"><span data-stu-id="0d1de-119">Integration with Electronic invoicing</span></span> 

<span data-ttu-id="0d1de-120">RCS を使用して電子請求書を構成するには、電子請求との通信を許可するために、RCS を構成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="0d1de-120">Before you can use RCS to configure electronic invoices, you must configure RCS to allow for communication with Electronic invoicing.</span></span> <span data-ttu-id="0d1de-121">**電子申告パラメーター** ページの **電子請求** タブでこの構成を完了します。</span><span class="sxs-lookup"><span data-stu-id="0d1de-121">You complete this configuration on the **Electronic invoicing** tab of the **Electronic reporting parameters** page.</span></span>

#### <a name="service-endpoint"></a><span data-ttu-id="0d1de-122">サービス エンドポイント</span><span class="sxs-lookup"><span data-stu-id="0d1de-122">Service endpoint</span></span>

<span data-ttu-id="0d1de-123">電子請求は、いくつかの Azure データセンターの地域で使用できます。</span><span class="sxs-lookup"><span data-stu-id="0d1de-123">Electronic invoicing is available in several Azure datacenter geographies.</span></span> <span data-ttu-id="0d1de-124">次の表に、地域ごとの可用性の一覧を示します。</span><span class="sxs-lookup"><span data-stu-id="0d1de-124">The following table lists the availability per region.</span></span>

| <span data-ttu-id="0d1de-125">Azure データ センターの地域</span><span class="sxs-lookup"><span data-stu-id="0d1de-125">Azure datacenter geography</span></span> |
|----------------------------|
| <span data-ttu-id="0d1de-126">米国</span><span class="sxs-lookup"><span data-stu-id="0d1de-126">United States</span></span>              |
| <span data-ttu-id="0d1de-127">ヨーロッパ</span><span class="sxs-lookup"><span data-stu-id="0d1de-127">Europe</span></span>                     |
| <span data-ttu-id="0d1de-128">英国</span><span class="sxs-lookup"><span data-stu-id="0d1de-128">United Kingdom</span></span>             |
| <span data-ttu-id="0d1de-129">アジア</span><span class="sxs-lookup"><span data-stu-id="0d1de-129">Asia</span></span>                       |

### <a name="service-environments"></a><span data-ttu-id="0d1de-130">サービス環境</span><span class="sxs-lookup"><span data-stu-id="0d1de-130">Service environments</span></span>

<span data-ttu-id="0d1de-131">サービス環境は、電子請求における電子請求機能の実行をサポートするために作成される論理パーティションです。</span><span class="sxs-lookup"><span data-stu-id="0d1de-131">Service environments are logical partitions that are created to support execution of the electronic invoicing features in Electronic invoicing.</span></span> <span data-ttu-id="0d1de-132">セキュリティのシークレットや電子証明書、ガバナンス (アクセス権限) は、サービス環境レベルで構成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="0d1de-132">The security secrets and digital certificates, and the governance (that is, access permissions), must be configured at the service environment level.</span></span>

<span data-ttu-id="0d1de-133">顧客は、必要な数のサービス環境を作成できます。</span><span class="sxs-lookup"><span data-stu-id="0d1de-133">Customers can create as many service environments as they want.</span></span> <span data-ttu-id="0d1de-134">顧客が作成するサービス環境は互いに依存するものではありません。</span><span class="sxs-lookup"><span data-stu-id="0d1de-134">All the service environments that a customer creates are independent of each other.</span></span>

<span data-ttu-id="0d1de-135">サービス環境は、RCS で作成・管理する必要があります。</span><span class="sxs-lookup"><span data-stu-id="0d1de-135">Service environments must be created and maintained in RCS.</span></span> <span data-ttu-id="0d1de-136">サービス環境の準備が整うと、電子請求にリソースが公開されます。</span><span class="sxs-lookup"><span data-stu-id="0d1de-136">When the service environments are ready, they must be published to Electronic invoicing.</span></span>

#### <a name="service-environment-status"></a><span data-ttu-id="0d1de-137">サービス環境の状態</span><span class="sxs-lookup"><span data-stu-id="0d1de-137">Service environment status</span></span>

<span data-ttu-id="0d1de-138">サービス環境は、状態を介して管理できます。</span><span class="sxs-lookup"><span data-stu-id="0d1de-138">Service environments can be managed through status.</span></span> <span data-ttu-id="0d1de-139">想定できるオプションは次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="0d1de-139">The possible options are:</span></span>

- <span data-ttu-id="0d1de-140">**未公開** - 環境は作成済ですが、まだ公開されていません。</span><span class="sxs-lookup"><span data-stu-id="0d1de-140">**Not published** – The environment has been created, but it hasn't yet been published.</span></span>
- <span data-ttu-id="0d1de-141">**公開済** - 環境が電子請求に公開されました。</span><span class="sxs-lookup"><span data-stu-id="0d1de-141">**Published** – The environment has been published to Electronic invoicing .</span></span>
- <span data-ttu-id="0d1de-142">**変更済** - 公開された環境の属性は変更されましたが、まだ公開されていません。</span><span class="sxs-lookup"><span data-stu-id="0d1de-142">**Changed** – The attributes of a published environment have been changed, but the changes haven't yet been published.</span></span>

#### <a name="customer-secrets"></a><span data-ttu-id="0d1de-143">顧客のシークレット</span><span class="sxs-lookup"><span data-stu-id="0d1de-143">Customer secrets</span></span>

<span data-ttu-id="0d1de-144">電子請求サービスは、企業が所有する Azure リソースにすべてのビジネス データを保存する役割を果たします。</span><span class="sxs-lookup"><span data-stu-id="0d1de-144">The Electronic invoicing service is responsible for storing all your business data in the Azure resources that your company owns.</span></span> <span data-ttu-id="0d1de-145">サービスが正常に動作し、電子請求で必要とされ生成されるすべてのビジネス データに適切にアクセスできるようにするためには、2 つの主要な Azure リソースを作成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="0d1de-145">To ensure that the service works correctly, and that all the business data that is required for and generated by Electronic invoicing is accessed appropriately, you must create two main Azure resources:</span></span>

- <span data-ttu-id="0d1de-146">電子請求書を格納する Azure ストレージ アカウント (Blob ストレージ)</span><span class="sxs-lookup"><span data-stu-id="0d1de-146">An Azure storage account (Blob storage) that will store electronic invoices</span></span>
- <span data-ttu-id="0d1de-147">証明書とストレージ アカウントの Uniform Resource Identifier (URI) を格納する Azure Key Vault</span><span class="sxs-lookup"><span data-stu-id="0d1de-147">An Azure Key Vault that will store certificates and the uniform resource identifier (URI) of the storage account</span></span>


<span data-ttu-id="0d1de-148">電子請求で使用するには、専用の Key Vault のリソースと顧客のストレージ アカウントを特別に割り当てる必要があります。</span><span class="sxs-lookup"><span data-stu-id="0d1de-148">A dedicated Key Vault and customer storage account must be allocated specifically for use with Electronic Invoicing.</span></span> <span data-ttu-id="0d1de-149">詳細については、[Azure ストレージ アカウント と Key Vault の作成](e-invoicing-create-azure-storage-account-key-vault.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="0d1de-149">For more information, see [Create an Azure storage account and a Key Vault](e-invoicing-create-azure-storage-account-key-vault.md).</span></span>

<span data-ttu-id="0d1de-150">Key Vault の正常性を監視し、警告を受信するには、Key Vault の Azure Monitor を構成します。</span><span class="sxs-lookup"><span data-stu-id="0d1de-150">To monitor the health of your Key Vault and receive alerts, configure the Azure Monitor for key Vault.</span></span> <span data-ttu-id="0d1de-151">Key Vault ログを有効にすると、Key Vault がどのように、また、いつ、だれにアクセスされたかを監視することができます。</span><span class="sxs-lookup"><span data-stu-id="0d1de-151">By enabling Key Vault logging, you can monitor how, when, and by whom your Key Vaults are accessed.</span></span> <span data-ttu-id="0d1de-152">詳細については、[Azure Key Vault の監視と警告](/azure/key-vault/general/alert)および [Key Vault ログを有効にする方法](/azure/key-vault/general/howto-logging?tabs=azure-cli) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="0d1de-152">For more information, see [Monitoring and alerting for Azure Key Vault](/azure/key-vault/general/alert) and [How to enable Key Vault logging](/azure/key-vault/general/howto-logging?tabs=azure-cli).</span></span>

<span data-ttu-id="0d1de-153">ベスト プラクティスとして、定期的にシークレットのローテーションを行います。</span><span class="sxs-lookup"><span data-stu-id="0d1de-153">As a best practice, periodically rotate the secrets.</span></span> <span data-ttu-id="0d1de-154">詳細については、[シークレット ドキュメント](/azure/key-vault/secrets/) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="0d1de-154">For more information, see [Secrets documentation](/azure/key-vault/secrets/).</span></span>

#### <a name="users"></a><span data-ttu-id="0d1de-155">ユーザー</span><span class="sxs-lookup"><span data-stu-id="0d1de-155">Users</span></span>

<span data-ttu-id="0d1de-156">各サービス環境では、電子請求で Dynamics 365 Finance と Dynamics 365 Supply Chain Management から接続できるユーザーの一覧を作成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="0d1de-156">Each service environment must list the users who can connect from Dynamics 365 Finance and Dynamics 365 Supply Chain Management in Electronic invoicing.</span></span>

#### <a name="publication"></a><span data-ttu-id="0d1de-157">公開</span><span class="sxs-lookup"><span data-stu-id="0d1de-157">Publication</span></span>

<span data-ttu-id="0d1de-158">サービス環境は、電子請求に公開した後で使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="0d1de-158">Service environments must be published to Electronic invoicing before they can be used.</span></span> <span data-ttu-id="0d1de-159">公開された環境のみが、 Finance および Supply Chain Management からアクセスできます。</span><span class="sxs-lookup"><span data-stu-id="0d1de-159">Only published environments can be accessed by Finance and Supply Chain Management.</span></span> <span data-ttu-id="0d1de-160">また、電子請求書発行サービスで属性の更新が有効になる前に、サービス環境を公開する必要があります。</span><span class="sxs-lookup"><span data-stu-id="0d1de-160">Additionally, a service environment must be published before any updates to its attributes will take effect on the electronic invoicing service.</span></span>

### <a name="connected-applications"></a><span data-ttu-id="0d1de-161">接続した申請</span><span class="sxs-lookup"><span data-stu-id="0d1de-161">Connected applications</span></span>

<span data-ttu-id="0d1de-162">接続されたアプリケーションは、RCS によって利用できる Finance および Supply Chain Management のインスタンスです。</span><span class="sxs-lookup"><span data-stu-id="0d1de-162">Connected applications are the instances of Finance and Supply Chain Management that you might want to reach through RCS.</span></span> <span data-ttu-id="0d1de-163">アプリケーションの URL とそのテナントに加え、接続されたアプリケーションには、RCS が環境に接続できる資格情報が含まれています。</span><span class="sxs-lookup"><span data-stu-id="0d1de-163">Besides the application URL and its tenant, a connected application contains the credentials that enable RCS to connect to the environment.</span></span>

<span data-ttu-id="0d1de-164">接続されたアプリケーションを通じて、Finance および Supply Chain Management の電子請求書機能の一部を構成することで、電子請求書の機能全体を機能させることができます。</span><span class="sxs-lookup"><span data-stu-id="0d1de-164">Through the connected applications, you can configure part of the electronic invoicing feature in Finance and Supply Chain Management to make the whole electronic invoicing feature work.</span></span>

## <a name="finance-and-supply-chain-management"></a><span data-ttu-id="0d1de-165">Finance および Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="0d1de-165">Finance and Supply Chain Management</span></span>

### <a name="integration-with-electronic-invoicing"></a><span data-ttu-id="0d1de-166">電子請求との統合</span><span class="sxs-lookup"><span data-stu-id="0d1de-166">Integration with Electronic invoicing</span></span>

<span data-ttu-id="0d1de-167">Finance および Supply Chain Management を使用して電子請求書アドオンを介した電子請求書を発行するには、サービスと通信ができるように構成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="0d1de-167">Before you can use Finance and Supply Chain Management to issue electronic invoices through Electronic invoicing, it must be configured to allow for communication with the service.</span></span>

#### <a name="electronic-invoicing-integration-feature"></a><span data-ttu-id="0d1de-168">電子請求統合機能</span><span class="sxs-lookup"><span data-stu-id="0d1de-168">Electronic invoicing integration feature</span></span>

<span data-ttu-id="0d1de-169">Finance および Supply Chain Management と電子請求の間の通信を有効にするには、**機能管理** ワークスペースで **電子請求の統合** 機能を有効にする必要 があります。</span><span class="sxs-lookup"><span data-stu-id="0d1de-169">To enable communication between Finance and Supply Chain Management and Electronic invoicing, you must turn on the **Electronic Invoicing integration** feature in the **Feature management** workspace.</span></span>

#### <a name="service-endpoint"></a><span data-ttu-id="0d1de-170">サービス エンドポイント</span><span class="sxs-lookup"><span data-stu-id="0d1de-170">Service endpoint</span></span>

<span data-ttu-id="0d1de-171">サービス エンドポイントは、電子請求が位置する URL です。</span><span class="sxs-lookup"><span data-stu-id="0d1de-171">The service endpoint is the URL where Electronic invoicing is located.</span></span> <span data-ttu-id="0d1de-172">サービスとの通信を可能にするには、電子請求書を発行する前にサービスのエンドポイントを Finance と Supply Chain Management に構成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="0d1de-172">Before electronic invoices can be issued, the service endpoint must be configured in Finance and Supply Chain Management to allow for communication with the service.</span></span>

<span data-ttu-id="0d1de-173">サービス エンドポイントを構成するには、**組織管理 \> 設定 \> 電子ドキュメント パラメーター** に移動し、**送信サービス** タブの **電子請求 URL** フィールドに、**サービス エンドポイント** のセクションで説明されている表に従って URL を入力します。</span><span class="sxs-lookup"><span data-stu-id="0d1de-173">To configure the service endpoint, go to **Organization administration \> Setup \> Electronic document parameter**, and then, on the **Submission services** tab, in the **Electronic invoicing URL** field, enter the URL as described in the table described in section **Service endpoint**.</span></span>

#### <a name="environments"></a><span data-ttu-id="0d1de-174">環境</span><span class="sxs-lookup"><span data-stu-id="0d1de-174">Environments</span></span>

<span data-ttu-id="0d1de-175">Finance および Supply Chain Management に入力された環境名は、RCS で作成され、電子請求に公開されている環境名を指します。</span><span class="sxs-lookup"><span data-stu-id="0d1de-175">The environment name that is entered in Finance and Supply Chain Management refers to the name of the environment that is created in RCS and published to Electronic invoicing.</span></span>

<span data-ttu-id="0d1de-176">環境は、電子請求書を発行するすべての要求に、電子請求がどの電子請求機能が要求を処理する必要があるかどうかを決定できる環境を含むように、**電子ドキュメント パラメータ** ページの **送信サービス** タブで構成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="0d1de-176">The environment must be configured on the **Submission services** tab of the **Electronic document parameter** page, so that every request to issue electronic invoices contains the environment where Electronic invoicing can determine which electronic invoicing feature must process the request.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="0d1de-177">追加リソース</span><span class="sxs-lookup"><span data-stu-id="0d1de-177">Additional resources</span></span>

- [<span data-ttu-id="0d1de-178">RCS で電子請求書を構成する</span><span class="sxs-lookup"><span data-stu-id="0d1de-178">Configure electronic invoices in RCS</span></span>](e-invoicing-configuration-rcs.md)
- [<span data-ttu-id="0d1de-179">Finance および Supply Chain Management で電子請求書を発行する</span><span class="sxs-lookup"><span data-stu-id="0d1de-179">Issue electronic invoices in Finance and Supply Chain Management</span></span>](e-invoicing-issuing-electronic-invoices-finance-supply-chain-management.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
