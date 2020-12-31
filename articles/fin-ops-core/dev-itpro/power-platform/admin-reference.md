---
title: Finance and Operations および Common Data Service 管理リファレンス
description: このトピックでは、Finance and Operations の仮想エンティティの設定およびコンフィギュレーションについて説明します。
author: Sunil-Garg
manager: AnnBe
ms.date: 07/13/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Developer, IT Pro
ms.reviewer: sericks
ms.search.region: Global
ms.author: sunilg
ms.search.validFrom: 2020-05-31
ms.dyn365.ops.version: 10.0.12
ms.openlocfilehash: 7826201478c676243e330a3ce6302b8fbb63222d
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 12/05/2020
ms.locfileid: "4680422"
---
# <a name="finance-and-operations-and-common-data-service-admin-reference"></a><span data-ttu-id="89c1b-103">Finance and Operations および Common Data Service 管理リファレンス</span><span class="sxs-lookup"><span data-stu-id="89c1b-103">Finance and Operations and Common Data Service admin reference</span></span>

[!include[banner](../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

> [!IMPORTANT]
> <span data-ttu-id="89c1b-104">この機能には、[Finance and Operations](../get-started/whats-new-platform-update-10-0-12.md) および Common Data Service の更新プログラム 189 のサービスが必要です。</span><span class="sxs-lookup"><span data-stu-id="89c1b-104">This functionality requires [Platform updates for version 10.0.12 of Finance and Operations apps](../get-started/whats-new-platform-update-10-0-12.md) and service update 189 for Common Data Service.</span></span> <span data-ttu-id="89c1b-105">Common Data Service のリリース情報は、[最新バージョンの利用可能性](https://docs.microsoft.com/business-applications-release-notes/dynamics/released-versions/dynamics-365ce#all-version-availability)ページに発行されています。</span><span class="sxs-lookup"><span data-stu-id="89c1b-105">The release information for Common Data Service is published on the [latest version availability page](https://docs.microsoft.com/business-applications-release-notes/dynamics/released-versions/dynamics-365ce#all-version-availability).</span></span>

<span data-ttu-id="89c1b-106">このトピックでは、Common Data Service で Finance and Operations アプリの仮想エンティティを設定およびコンフィギュレーションする方法について手順を追って説明します。</span><span class="sxs-lookup"><span data-stu-id="89c1b-106">This topic provides step-by-step instructions about how to set up and configure virtual entities for Finance and Operations apps in Common Data Service.</span></span>

## <a name="getting-the-solution"></a><span data-ttu-id="89c1b-107">ソリューションの入手</span><span class="sxs-lookup"><span data-stu-id="89c1b-107">Getting the solution</span></span>
<span data-ttu-id="89c1b-108">Finance and Operations 仮想エンティティの Common Data Service ソリューションは、Microsoft AppSource 仮想エンティティ ソリューションからダウンロードする必要があります。</span><span class="sxs-lookup"><span data-stu-id="89c1b-108">The Common Data Service solution for Finance and Operations virtual entities must be installed from Microsoft AppSource virtual entity solution.</span></span> <span data-ttu-id="89c1b-109">詳細については、[Finance and Operations 仮想エンティティ](https://appsource.microsoft.com/product/dynamics-crm/mscrm.finance_and_operations_virtual_entity) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="89c1b-109">For more information, see [Finance and Operations virtual entity](https://appsource.microsoft.com/product/dynamics-crm/mscrm.finance_and_operations_virtual_entity).</span></span>

<span data-ttu-id="89c1b-110">次のソリューションが Common Data Service にインストールされていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="89c1b-110">Ensure the following solutions are installed in Common Data Service.</span></span>

- <span data-ttu-id="89c1b-111">**Dynamics365Company**: すべての Finance and Operations エンティティによって参照される **会社** エンティティを、PrimaryCompanyContext メタデータ値と共に追加します。</span><span class="sxs-lookup"><span data-stu-id="89c1b-111">**Dynamics365Company** - This adds the **Company** entity, which is referenced by all Finance and Operations entities with a PrimaryCompanyContext metadata value.</span></span>

- <span data-ttu-id="89c1b-112">**MicrosoftOperationsVESupport**: これにより、Finance and Operations 仮想エンティティ機能のコア サポートが提供されます。</span><span class="sxs-lookup"><span data-stu-id="89c1b-112">**MicrosoftOperationsVESupport** - This provides the core support for the Finance and Operations virtual entity feature.</span></span>

- <span data-ttu-id="89c1b-113">**MicrosoftOperationsERPCatalog**: これは、mserp_financeandoperationsentity 仮想エンティティを通じて使用できる Finance and Operations エンティティの一覧を提供します。</span><span class="sxs-lookup"><span data-stu-id="89c1b-113">**MicrosoftOperationsERPCatalog** - This provides a list of available Finance and Operations entities through the mserp_financeandoperationsentity virtual entity.</span></span>

- <span data-ttu-id="89c1b-114">**MicrosoftOperationsERPVE**: これは、表示されるときに生成された仮想エンティティを含む、API マネージド ソリューションです。</span><span class="sxs-lookup"><span data-stu-id="89c1b-114">**MicrosoftOperationsERPVE** - This is the API-managed solution, which will contain the generated virtual entities as they are made visible.</span></span>

## <a name="authentication-and-authorization"></a><span data-ttu-id="89c1b-115">認証と承認</span><span class="sxs-lookup"><span data-stu-id="89c1b-115">Authentication and authorization</span></span>

<span data-ttu-id="89c1b-116">ソリューションを Common Data Service 環境にインポートした後は、両方の環境を相互に接続するように設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="89c1b-116">After the solutions are imported in the Common Data Service environment, both environments must be set up to connect to each other.</span></span> <span data-ttu-id="89c1b-117">Common Data Service は、Azure Active Directory (AAD) アプリケーションに基づいて、サービス ツー サービス (S2S) 認証を使用して Finance and Operations を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="89c1b-117">Common Data Service will call Finance and Operations using Service-to-Service (S2S) authentication, based on an Azure Active Directory (AAD) application.</span></span> <span data-ttu-id="89c1b-118">この新しい AAD アプリケーションは、Common Data Service 環境の単一のインスタンスを表します。</span><span class="sxs-lookup"><span data-stu-id="89c1b-118">This new AAD application represents the single instance of the Common Data Service environment.</span></span> <span data-ttu-id="89c1b-119">Common Data Service と Finance and Operations の環境の組み合わせが複数存在する場合は、ペアごとに独立した AAD アプリケーションを作成して、Finance and Operations 環境と Common Data Service 環境の正しいペア間で確実に接続が確立されるようにする必要があります。</span><span class="sxs-lookup"><span data-stu-id="89c1b-119">If you have multiple pairs of Common Data Service and Finance and Operations environments, separate AAD applications for each pair must be created to ensure connections are established between the correct pair of Finance and Operations and Common Data Service environments.</span></span> <span data-ttu-id="89c1b-120">次の手順は、AAD アプリケーションの作成方法を示しています。</span><span class="sxs-lookup"><span data-stu-id="89c1b-120">The following procedure shows the creation of the AAD application.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="89c1b-121">AAD アプリケーションは、Finance and Operations と同じテナントに作成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="89c1b-121">The AAD application must be created on the same tenant as Finance and Operations.</span></span>

1.  <span data-ttu-id="89c1b-122"><https://portal.azure.com> **\> Azure Active Directory \> アプリの登録** に移動します。</span><span class="sxs-lookup"><span data-stu-id="89c1b-122">Go to <https://portal.azure.com> **\> Azure Active Directory \> App registrations**.</span></span>

2.  <span data-ttu-id="89c1b-123">**新規登録** を選択します。</span><span class="sxs-lookup"><span data-stu-id="89c1b-123">Select **New Registration**.</span></span> <span data-ttu-id="89c1b-124">次の情報を入力します。</span><span class="sxs-lookup"><span data-stu-id="89c1b-124">Enter the following information:</span></span>

    - <span data-ttu-id="89c1b-125">**名前**: 一意の名前を入力します。</span><span class="sxs-lookup"><span data-stu-id="89c1b-125">**Name** - Enter a unique name.</span></span>

    - <span data-ttu-id="89c1b-126">**アカウント タイプ**: **任意の Azure AD ディレクトリ** を入力します (単一またはマルチテナント)。</span><span class="sxs-lookup"><span data-stu-id="89c1b-126">**Account type** - Enter **Any Azure AD directory** (single or multi-tenant).</span></span>

    - <span data-ttu-id="89c1b-127">**リダイレクト URI**: 空白のままにします。</span><span class="sxs-lookup"><span data-stu-id="89c1b-127">**Redirect URI** - Leave blank.</span></span>

    - <span data-ttu-id="89c1b-128">**登録** を選択します。</span><span class="sxs-lookup"><span data-stu-id="89c1b-128">Select **Register**.</span></span>

    - <span data-ttu-id="89c1b-129">**アプリケーション (クライアント) ID** の値をメモしておきます。後の手順で必要となります。</span><span class="sxs-lookup"><span data-stu-id="89c1b-129">Make note of the **Application (client) ID** value, you will need it later.</span></span>

3.  <span data-ttu-id="89c1b-130">アプリケーションの対称キーを作成します。</span><span class="sxs-lookup"><span data-stu-id="89c1b-130">Create a symmetric key for the application.</span></span>

    - <span data-ttu-id="89c1b-131">新しく作成されたアプリケーションで **証明書とシークレット** を選択します。</span><span class="sxs-lookup"><span data-stu-id="89c1b-131">Select **Certificates & secrets** in the newly created application.</span></span>

    - <span data-ttu-id="89c1b-132">**新しいクライアント シークレット** を選択します。</span><span class="sxs-lookup"><span data-stu-id="89c1b-132">Select **New client secret**.</span></span>

    - <span data-ttu-id="89c1b-133">説明と有効期限を入力します。</span><span class="sxs-lookup"><span data-stu-id="89c1b-133">Provide a description and an expiration date.</span></span>

    - <span data-ttu-id="89c1b-134">**保存** を選択します。</span><span class="sxs-lookup"><span data-stu-id="89c1b-134">Select **Save**.</span></span> <span data-ttu-id="89c1b-135">キーが作成され、表示されます。</span><span class="sxs-lookup"><span data-stu-id="89c1b-135">A key will be created and displayed.</span></span> <span data-ttu-id="89c1b-136">この値を後で使用するためにコピーします。</span><span class="sxs-lookup"><span data-stu-id="89c1b-136">Copy this value for later use.</span></span>

<span data-ttu-id="89c1b-137">上で作成した AAD アプリケーションは、Common Data Service によって Finance and Operations アプリを呼び出すために使用されます。</span><span class="sxs-lookup"><span data-stu-id="89c1b-137">The AAD application created above will be used by Common Data Service to call Finance and Operations apps.</span></span> <span data-ttu-id="89c1b-138">したがって、Finance and Operations によって信頼され、Finance and Operations で適切な権限を持つユーザー アカウントに関連付けられている必要があり ます。</span><span class="sxs-lookup"><span data-stu-id="89c1b-138">As such, it must be trusted by Finance and Operations and associated with a user account with the appropriate rights in Finance and Operations.</span></span> <span data-ttu-id="89c1b-139">Finance and Operations では、特殊サービス ユーザーは、仮想エンティティ機能に対する権限 *のみ* で作成することができます。その他の権限は必要ありません。</span><span class="sxs-lookup"><span data-stu-id="89c1b-139">A special service user must be created in Finance and Operations with rights *only* to the virtual entity functionality, and no other rights.</span></span> <span data-ttu-id="89c1b-140">この手順を完了すると、上で作成した AAD アプリケーションのシークレットを使用するアプリケーションによって、この Finance and Operations 環境を呼び出して仮想エンティティの機能にアクセスできるようになります。</span><span class="sxs-lookup"><span data-stu-id="89c1b-140">After completing this step, any application with the secret of the AAD application create above will be able to call this Finance and Operations environment and access the virtual entity functionality.</span></span>

<span data-ttu-id="89c1b-141">次の手順では、このプロセスを Finance and Operations アプリで実行していきます。</span><span class="sxs-lookup"><span data-stu-id="89c1b-141">The next steps walk through this process in Finance and Operations apps.</span></span>

1.  <span data-ttu-id="89c1b-142">Finance and Operations で、**システム管理 \> ユーザー \> ユーザー** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="89c1b-142">In Finance and Operations, go to **System Administration \> Users \> Users**.</span></span>

2.  <span data-ttu-id="89c1b-143">**新規作成** を選択して、新しいユーザーを追加します。</span><span class="sxs-lookup"><span data-stu-id="89c1b-143">Select **New** to add a new user.</span></span> <span data-ttu-id="89c1b-144">次の情報を入力します。</span><span class="sxs-lookup"><span data-stu-id="89c1b-144">Enter the following information:</span></span>

    - <span data-ttu-id="89c1b-145">**ユーザー ID**: **cdsintegration** (または別の値) を入力します。</span><span class="sxs-lookup"><span data-stu-id="89c1b-145">**User ID** - Enter **cdsintegration** (or a different value).</span></span>

    - <span data-ttu-id="89c1b-146">**ユーザー名**: **cds integration** (または別の値) を入力します。</span><span class="sxs-lookup"><span data-stu-id="89c1b-146">**User name** - Enter **cds integration** (or a different value).</span></span>

    - <span data-ttu-id="89c1b-147">**プロバイダー**: 既定値をそのまま使います。</span><span class="sxs-lookup"><span data-stu-id="89c1b-147">**Provider** - Leave at the default value.</span></span>

    - <span data-ttu-id="89c1b-148">**電子メール**: **cdsintegration** (または別の値) を入力します (有効な電子メール アカウントである必要は *ありません*)。</span><span class="sxs-lookup"><span data-stu-id="89c1b-148">**Email** - Enter **cdsintegration** (or a different value, does *not* need to be a valid email account).</span></span>

    - <span data-ttu-id="89c1b-149">このユーザーにセキュリティ ロール **CDS 仮想エンティティ アプリケーション** を割り当てます。</span><span class="sxs-lookup"><span data-stu-id="89c1b-149">Assign the security role **CDS virtual entity application** to this user.</span></span>

    - <span data-ttu-id="89c1b-150">**システム ユーザー** を含む他のすべてのロールを削除します。</span><span class="sxs-lookup"><span data-stu-id="89c1b-150">Remove all other roles including **System user**.</span></span>

3.  <span data-ttu-id="89c1b-151">**システム管理 \> 設定 \> Azure Active Directory アプリケーション** の順に移動して Common Data Service を登録します。</span><span class="sxs-lookup"><span data-stu-id="89c1b-151">Go to **System Administration \> Setup \> Azure Active Directory applications** to register Common Data Service.</span></span> 

    - <span data-ttu-id="89c1b-152">新しい行を追加します。</span><span class="sxs-lookup"><span data-stu-id="89c1b-152">Add a new row.</span></span>

    - <span data-ttu-id="89c1b-153">**クライアント ID**: 上で作成された **アプリケーション (クライアント) ID**</span><span class="sxs-lookup"><span data-stu-id="89c1b-153">**Client ID** - The **Application (client) ID** created above</span></span>

    - <span data-ttu-id="89c1b-154">**名前**: **CDS 統合** (または別の名前) を入力します。</span><span class="sxs-lookup"><span data-stu-id="89c1b-154">**Name** - Enter **CDS Integration** (or a different name).</span></span>

    - <span data-ttu-id="89c1b-155">**ユーザー ID**: 上記で作成されたユーザー ID。</span><span class="sxs-lookup"><span data-stu-id="89c1b-155">**User ID** - The user ID created above.</span></span>

<span data-ttu-id="89c1b-156">プロセスの次の手順では、接続先の Finance and Operations インスタンスに Common Data Service を提供します。</span><span class="sxs-lookup"><span data-stu-id="89c1b-156">The next step in the process is to provide Common Data Service with the Finance and Operations instance to connect to.</span></span> <span data-ttu-id="89c1b-157">以下の手順では、プロセスのこの部分について説明します。</span><span class="sxs-lookup"><span data-stu-id="89c1b-157">The following steps walk through this part of the process.</span></span>

1.  <span data-ttu-id="89c1b-158">Common Data Service では、**詳細設定 \> 管理 \> 仮想エンティティ データ ソース** に移動します。</span><span class="sxs-lookup"><span data-stu-id="89c1b-158">In Common Data Service, go to **Advanced Settings \> Administration \> Virtual Entity Data Sources**.</span></span>

2.  <span data-ttu-id="89c1b-159">"Finance and Operations" というデータ ソースを選択します。</span><span class="sxs-lookup"><span data-stu-id="89c1b-159">Select the data source named “Finance and Operations”.</span></span>

3.  <span data-ttu-id="89c1b-160">上記の手順に従って情報を入力します。</span><span class="sxs-lookup"><span data-stu-id="89c1b-160">Fill in the information from the steps above.</span></span>

    - <span data-ttu-id="89c1b-161">**ターゲット URL**: Finance and Operations にアクセスできる URL。</span><span class="sxs-lookup"><span data-stu-id="89c1b-161">**Target URL** - The URL at which you can access Finance and Operations.</span></span>

    - <span data-ttu-id="89c1b-162">**OAuth URL** - https://login.windows.net/</span><span class="sxs-lookup"><span data-stu-id="89c1b-162">**OAuth URL** - https://login.windows.net/</span></span>

    - <span data-ttu-id="89c1b-163">**テナント ID**: "contoso.com" などのテナント。</span><span class="sxs-lookup"><span data-stu-id="89c1b-163">**Tenant ID** - Your tenant, such as “contoso.com”.</span></span>

    - <span data-ttu-id="89c1b-164">**AAD アプリケーション ID**: 上で作成された **アプリケーション (クライアント) ID**。</span><span class="sxs-lookup"><span data-stu-id="89c1b-164">**AAD Application ID** - The **Application (client) ID** created above.</span></span>

    - <span data-ttu-id="89c1b-165">**AAD アプリケーション シークレット**: 上で生成されたシークレット。</span><span class="sxs-lookup"><span data-stu-id="89c1b-165">**AAD Application Secret** - The secret generated above.</span></span>

    - <span data-ttu-id="89c1b-166">**AAD リソース**: 00000015-0000-0000-c000-000000000000 と入力します (これは、Finance and Operations を表す AAD アプリケーションです。常に同じ値であることを表します)。</span><span class="sxs-lookup"><span data-stu-id="89c1b-166">**AAD Resource** - Enter 00000015-0000-0000-c000-000000000000 (this is the AAD application representing Finance and Operations, and should always be this same value).</span></span>

4.  <span data-ttu-id="89c1b-167">変更を保存します。</span><span class="sxs-lookup"><span data-stu-id="89c1b-167">Save the changes.</span></span>

## <a name="enabling-virtual-entities"></a><span data-ttu-id="89c1b-168">仮想エンティティの有効化</span><span class="sxs-lookup"><span data-stu-id="89c1b-168">Enabling virtual entities</span></span>

<span data-ttu-id="89c1b-169">Finance and Operations には多数の OData 対応エンティティが含まれているため、既定では、エンティティは Common Data Service の仮想エンティティとしては使用できません。</span><span class="sxs-lookup"><span data-stu-id="89c1b-169">Due to the large number of OData enabled entities available in Finance and Operations, by default, the entities are not available as virtual entities in Common Data Service.</span></span> <span data-ttu-id="89c1b-170">次の手順では、必要に応じてエンティティを仮想にすることができます。</span><span class="sxs-lookup"><span data-stu-id="89c1b-170">The following steps allow for enabling entities to be virtual, as needed.</span></span>

1. <span data-ttu-id="89c1b-171">Common Data Service で、**高度な検索** に移動します (フィルター アイコン)。</span><span class="sxs-lookup"><span data-stu-id="89c1b-171">In Common Data Service, go to **Advanced find** (filter icon).</span></span>

2. <span data-ttu-id="89c1b-172">[利用可能な Finance and Operations エンティティ] を探して、**結果** を選択します。</span><span class="sxs-lookup"><span data-stu-id="89c1b-172">Look for “Available Finance and Operations Entities” and select **Results**.</span></span>

![カタログ](../media/fovecatalog.png)

3. <span data-ttu-id="89c1b-174">有効にするエンティティを検索して開きます。</span><span class="sxs-lookup"><span data-stu-id="89c1b-174">Locate and open the entity that you want to enable.</span></span>

4. <span data-ttu-id="89c1b-175">**表示** を **はい** に設定して保存します。</span><span class="sxs-lookup"><span data-stu-id="89c1b-175">Set **Visible** to **Yes** and save.</span></span> <span data-ttu-id="89c1b-176">これにより、仮想エンティティが生成され、[高度な検索] ダイアログ ボックスなどの適切なすべてのメニューに表示されるようになります。</span><span class="sxs-lookup"><span data-stu-id="89c1b-176">This will generate the virtual entity, so that it will appear in all of the appropriate menus, such as the advanced find dialog box.</span></span>

![VE の有効化](../media/foveenable.png)

## <a name="refreshing-virtual-entity-metadata"></a><span data-ttu-id="89c1b-178">仮想エンティティ メタデータの更新</span><span class="sxs-lookup"><span data-stu-id="89c1b-178">Refreshing virtual entity metadata</span></span>

<span data-ttu-id="89c1b-179">仮想エンティティ メタデータは、Finance and Operations のエンティティ メタデータが変更されたと想定される場合に、強制的に更新できます。</span><span class="sxs-lookup"><span data-stu-id="89c1b-179">The virtual entity metadata can be force-refreshed when it is expected for the entity metadata in Finance and Operations to have changed.</span></span> <span data-ttu-id="89c1b-180">これを行うには、**更新** を **はい** に設定して保存します。</span><span class="sxs-lookup"><span data-stu-id="89c1b-180">This can be done by setting **Refresh** to **Yes** and saving.</span></span> <span data-ttu-id="89c1b-181">これにより、Finance and Operations の最新のエンティティ定義が Common Data Service に同期され、仮想エンティティが更新されます。</span><span class="sxs-lookup"><span data-stu-id="89c1b-181">This will sync the latest entity definition from Finance and Operations to Common Data Service and update the virtual entity.</span></span>

<a name="referencing-virtual-entities"></a><span data-ttu-id="89c1b-182">仮想エンティティの参照</span><span class="sxs-lookup"><span data-stu-id="89c1b-182">Referencing virtual entities</span></span>
----------------------------

<span data-ttu-id="89c1b-183">仮想エンティティはすべて MicrosoftOperationsERPVE ソリューションで生成され、API によって管理されます。</span><span class="sxs-lookup"><span data-stu-id="89c1b-183">The virtual entities are all generated in the MicrosoftOperationsERPVE solution, which is API Managed.</span></span> <span data-ttu-id="89c1b-184">つまり、エンティティの表示/非表示を変更してもソリューションの項目は変化しますが、それでも依存できるマネージド ソリューションになります。</span><span class="sxs-lookup"><span data-stu-id="89c1b-184">That means the items in the solution change as you make entities visible/hidden, but it is still a managed solution that you can take dependency on.</span></span> <span data-ttu-id="89c1b-185">標準 ALM フローでは、ISV ソリューションの **既存の追加** オプションを使用して、このソリューションから仮想エンティティに対する標準参照を取得するだけです。</span><span class="sxs-lookup"><span data-stu-id="89c1b-185">The standard ALM flow would be to just take a standard reference to a virtual entity from this solution with the **Add existing** option in the ISV solution.</span></span> <span data-ttu-id="89c1b-186">これにより、ソリューションの依存関係が見つからないと表示され、ソリューション インポート時にチェックされます。</span><span class="sxs-lookup"><span data-stu-id="89c1b-186">It will then show as a missing dependency of the solution and be checked at solution import time.</span></span> <span data-ttu-id="89c1b-187">インポート中に、指定された仮想エンティティがまだ存在しない場合は、追加の作業を必要とすることなく、自動的に表示されます。</span><span class="sxs-lookup"><span data-stu-id="89c1b-187">During import if a specified virtual entity does not yet exist, it would automatically be made visible without needing additional work.</span></span>

<span data-ttu-id="89c1b-188">仮想エンティティを使用するには</span><span class="sxs-lookup"><span data-stu-id="89c1b-188">To consume virtual entities:</span></span>

1.  <span data-ttu-id="89c1b-189">Common Data Service で通常どおり別個のソリューションを作成します。これには、消費ロジックが含められます。</span><span class="sxs-lookup"><span data-stu-id="89c1b-189">Create a separate solution as usual in Common Data Service, which will contain the consuming logic.</span></span>

2.  <span data-ttu-id="89c1b-190">**エンティティ \> 既存の追加** を選択します。</span><span class="sxs-lookup"><span data-stu-id="89c1b-190">Select **Entities \> Add Existing**.</span></span> <span data-ttu-id="89c1b-191">一覧から参照する仮想エンティティを選択します。</span><span class="sxs-lookup"><span data-stu-id="89c1b-191">Select the virtual entity that you want to reference from the list.</span></span>

3.  <span data-ttu-id="89c1b-192">追加する資産の選択を求めるメッセージが表示されたら、カスタマイズするフォーム、ビュー、またはその他の要素を選択し、**完了** を選択します。</span><span class="sxs-lookup"><span data-stu-id="89c1b-192">When prompted to select assets to add, select any forms, views, or other elements that you want to customize, then select **Finish**.</span></span>

<span data-ttu-id="89c1b-193">開発ツールから、フォームなどの既存の要素を仮想エンティティに対して変更することができます。</span><span class="sxs-lookup"><span data-stu-id="89c1b-193">From the development tooling, existing elements such as forms can be modified for the virtual entity.</span></span> <span data-ttu-id="89c1b-194">また、新しいフォーム、ビュー、およびその他の要素を追加することもできます。</span><span class="sxs-lookup"><span data-stu-id="89c1b-194">Additionally, new forms, views, and other elements can also be added.</span></span>

![ソリューション](../media/fovesolution.png)

<span data-ttu-id="89c1b-196">ソリューションをエクスポートすると、MicrosoftOperationsERPVE ソリューションで生成された仮想エンティティへのハード依存関係が含められます。</span><span class="sxs-lookup"><span data-stu-id="89c1b-196">When the solution is exported, it will contain hard dependencies on the virtual entity generated in the MicrosoftOperationsERPVE solution.</span></span>
