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
ms.search.scope: Operations
ms.search.region: Global
ms.author: sunilg
ms.search.validFrom: 2020-05-31
ms.dyn365.ops.version: 10.0.12
ms.openlocfilehash: bedfe89e8ef9bdb7989abf2c81f76aa9640bcc68
ms.sourcegitcommit: 4a981ee4be6d7e6c0e55541535d386bce2565cba
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 07/27/2020
ms.locfileid: "3621209"
---
# <a name="finance-and-operations-and-common-data-service-admin-reference"></a><span data-ttu-id="ca584-103">Finance and Operations および Common Data Service 管理リファレンス</span><span class="sxs-lookup"><span data-stu-id="ca584-103">Finance and Operations and Common Data Service admin reference</span></span>
[!include[banner](../includes/banner.md)]

> [!IMPORTANT]
> <span data-ttu-id="ca584-104">この機能には、[Finance and Operations](../get-started/whats-new-platform-update-10-0-12.md) および Common Data Service の更新プログラム 189 のサービスが必要です。</span><span class="sxs-lookup"><span data-stu-id="ca584-104">This functionality requires [Platform updates for version 10.0.12 of Finance and Operations apps](../get-started/whats-new-platform-update-10-0-12.md) and service update 189 for Common Data Service.</span></span> <span data-ttu-id="ca584-105">Common Data Service のリリース情報は、[最新バージョンの利用可能性](https://docs.microsoft.com/business-applications-release-notes/dynamics/released-versions/dynamics-365ce#all-version-availability)ページに発行されています。</span><span class="sxs-lookup"><span data-stu-id="ca584-105">The release information for Common Data Service is published on the [latest version availability page](https://docs.microsoft.com/business-applications-release-notes/dynamics/released-versions/dynamics-365ce#all-version-availability).</span></span>

<span data-ttu-id="ca584-106">このトピックでは、Common Data Service で Finance and Operations アプリの仮想エンティティを設定およびコンフィギュレーションする方法について手順を追って説明します。</span><span class="sxs-lookup"><span data-stu-id="ca584-106">This topic provides step-by-step instructions about how to set up and configure virtual entities for Finance and Operations apps in Common Data Service.</span></span>

## <a name="getting-the-solution"></a><span data-ttu-id="ca584-107">ソリューションの入手</span><span class="sxs-lookup"><span data-stu-id="ca584-107">Getting the solution</span></span>
<span data-ttu-id="ca584-108">Finance and Operations 仮想エンティティの Common Data Service ソリューションは、Microsoft AppSource 仮想エンティティ ソリューションからダウンロードする必要があります。</span><span class="sxs-lookup"><span data-stu-id="ca584-108">The Common Data Service solution for Finance and Operations virtual entities must be installed from Microsoft AppSource virtual entity solution.</span></span> <span data-ttu-id="ca584-109">詳細については、[Finance and Operations 仮想エンティティ](https://appsource.microsoft.com/product/dynamics-crm/mscrm.finance_and_operations_virtual_entity) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="ca584-109">For more information, see [Finance and Operations virtual entity](https://appsource.microsoft.com/product/dynamics-crm/mscrm.finance_and_operations_virtual_entity).</span></span>

<span data-ttu-id="ca584-110">次のソリューションが Common Data Service にインストールされていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="ca584-110">Ensure the following solutions are installed in Common Data Service.</span></span> <span data-ttu-id="ca584-111">これらのソリューションは、ダウンロードしたパッケージから抽出する必要があります。</span><span class="sxs-lookup"><span data-stu-id="ca584-111">These solutions must be extracted from the downloaded package.</span></span>

- <span data-ttu-id="ca584-112">**Dynamics365Company**: すべての Finance and Operations エンティティによって参照される**会社**エンティティを、PrimaryCompanyContext メタデータ値と共に追加します。</span><span class="sxs-lookup"><span data-stu-id="ca584-112">**Dynamics365Company** - This adds the **Company** entity, which is referenced by all Finance and Operations entities with a PrimaryCompanyContext metadata value.</span></span>

- <span data-ttu-id="ca584-113">**MicrosoftOperationsVESupport**: これにより、Finance and Operations 仮想エンティティ機能のコア サポートが提供されます。</span><span class="sxs-lookup"><span data-stu-id="ca584-113">**MicrosoftOperationsVESupport** - This provides the core support for the Finance and Operations virtual entity feature.</span></span>

- <span data-ttu-id="ca584-114">**MicrosoftOperationsERPCatalog**: これは、mserp_financeandoperationsentity 仮想エンティティを通じて使用できる Finance and Operations エンティティの一覧を提供します。</span><span class="sxs-lookup"><span data-stu-id="ca584-114">**MicrosoftOperationsERPCatalog** - This provides a list of available Finance and Operations entities through the mserp_financeandoperationsentity virtual entity.</span></span>

- <span data-ttu-id="ca584-115">**MicrosoftOperationsERPVE**: これは、表示されるときに生成された仮想エンティティを含む、API マネージド ソリューションです。</span><span class="sxs-lookup"><span data-stu-id="ca584-115">**MicrosoftOperationsERPVE** - This is the API-managed solution, which will contain the generated virtual entities as they are made visible.</span></span>

## <a name="authentication-and-authorization"></a><span data-ttu-id="ca584-116">認証と承認</span><span class="sxs-lookup"><span data-stu-id="ca584-116">Authentication and authorization</span></span>

<span data-ttu-id="ca584-117">ソリューションを Common Data Service 環境にインポートした後は、両方の環境を相互に接続するように設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="ca584-117">After the solutions are imported in the Common Data Service environment, both environments must be set up to connect to each other.</span></span> <span data-ttu-id="ca584-118">Common Data Service は、Azure Active Directory (AAD) アプリケーションに基づいて、サービス ツー サービス (S2S) 認証を使用して Finance and Operations を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="ca584-118">Common Data Service will call Finance and Operations using Service-to-Service (S2S) authentication, based on an Azure Active Directory (AAD) application.</span></span> <span data-ttu-id="ca584-119">この新しい AAD アプリケーションは、Common Data Service 環境の単一のインスタンスを表します。</span><span class="sxs-lookup"><span data-stu-id="ca584-119">This new AAD application represents the single instance of the Common Data Service environment.</span></span> <span data-ttu-id="ca584-120">Common Data Service と Finance and Operations の環境の組み合わせが複数存在する場合は、ペアごとに独立した AAD アプリケーションを作成して、Finance and Operations 環境と Common Data Service 環境の正しいペア間で確実に接続が確立されるようにする必要があります。</span><span class="sxs-lookup"><span data-stu-id="ca584-120">If you have multiple pairs of Common Data Service and Finance and Operations environments, separate AAD applications for each pair must be created to ensure connections are established between the correct pair of Finance and Operations and Common Data Service environments.</span></span> <span data-ttu-id="ca584-121">次の手順は、AAD アプリケーションの作成方法を示しています。</span><span class="sxs-lookup"><span data-stu-id="ca584-121">The following procedure shows the creation of the AAD application.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="ca584-122">AAD アプリケーションは、Finance and Operations と同じテナントに作成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="ca584-122">The AAD application must be created on the same tenant as Finance and Operations.</span></span>

1.  <span data-ttu-id="ca584-123"><https://portal.azure.com> **\> Azure Active Directory \> アプリの登録** に移動します。</span><span class="sxs-lookup"><span data-stu-id="ca584-123">Go to <https://portal.azure.com> **\> Azure Active Directory \> App registrations**.</span></span>

2.  <span data-ttu-id="ca584-124">**新規登録** を選択します。</span><span class="sxs-lookup"><span data-stu-id="ca584-124">Select **New Registration**.</span></span> <span data-ttu-id="ca584-125">次の情報を入力します。</span><span class="sxs-lookup"><span data-stu-id="ca584-125">Enter the following information:</span></span>

    - <span data-ttu-id="ca584-126">**名前**: 一意の名前を入力します。</span><span class="sxs-lookup"><span data-stu-id="ca584-126">**Name** - Enter a unique name.</span></span>

    - <span data-ttu-id="ca584-127">**アカウント タイプ**: **任意の Azure AD ディレクトリ**を入力します (単一またはマルチテナント)。</span><span class="sxs-lookup"><span data-stu-id="ca584-127">**Account type** - Enter **Any Azure AD directory** (single or multi-tenant).</span></span>

    - <span data-ttu-id="ca584-128">**リダイレクト URI**: 空白のままにします。</span><span class="sxs-lookup"><span data-stu-id="ca584-128">**Redirect URI** - Leave blank.</span></span>

    - <span data-ttu-id="ca584-129">**登録** を選択します。</span><span class="sxs-lookup"><span data-stu-id="ca584-129">Select **Register**.</span></span>

    - <span data-ttu-id="ca584-130">**アプリケーション (クライアント) ID** の値をメモしておきます。後の手順で必要となります。</span><span class="sxs-lookup"><span data-stu-id="ca584-130">Make note of the **Application (client) ID** value, you will need it later.</span></span>

3.  <span data-ttu-id="ca584-131">アプリケーションの対称キーを作成します。</span><span class="sxs-lookup"><span data-stu-id="ca584-131">Create a symmetric key for the application.</span></span>

    - <span data-ttu-id="ca584-132">新しく作成されたアプリケーションで **証明書とシークレット** を選択します。</span><span class="sxs-lookup"><span data-stu-id="ca584-132">Select **Certificates & secrets** in the newly created application.</span></span>

    - <span data-ttu-id="ca584-133">**新しいクライアント シークレット** を選択します。</span><span class="sxs-lookup"><span data-stu-id="ca584-133">Select **New client secret**.</span></span>

    - <span data-ttu-id="ca584-134">説明と有効期限を入力します。</span><span class="sxs-lookup"><span data-stu-id="ca584-134">Provide a description and an expiration date.</span></span>

    - <span data-ttu-id="ca584-135">**保存** を選択します。</span><span class="sxs-lookup"><span data-stu-id="ca584-135">Select **Save**.</span></span> <span data-ttu-id="ca584-136">キーが作成され、表示されます。</span><span class="sxs-lookup"><span data-stu-id="ca584-136">A key will be created and displayed.</span></span> <span data-ttu-id="ca584-137">この値を後で使用するためにコピーします。</span><span class="sxs-lookup"><span data-stu-id="ca584-137">Copy this value for later use.</span></span>

<span data-ttu-id="ca584-138">上で作成した AAD アプリケーションは、Common Data Service によって Finance and Operations アプリを呼び出すために使用されます。</span><span class="sxs-lookup"><span data-stu-id="ca584-138">The AAD application created above will be used by Common Data Service to call Finance and Operations apps.</span></span> <span data-ttu-id="ca584-139">したがって、Finance and Operations によって信頼され、Finance and Operations で適切な権限を持つユーザー アカウントに関連付けられている必要があり ます。</span><span class="sxs-lookup"><span data-stu-id="ca584-139">As such, it must be trusted by Finance and Operations and associated with a user account with the appropriate rights in Finance and Operations.</span></span> <span data-ttu-id="ca584-140">Finance and Operations では、特殊サービス ユーザーは、仮想エンティティ機能に対する権限*のみ*で作成することができます。その他の権限は必要ありません。</span><span class="sxs-lookup"><span data-stu-id="ca584-140">A special service user must be created in Finance and Operations with rights *only* to the virtual entity functionality, and no other rights.</span></span> <span data-ttu-id="ca584-141">この手順を完了すると、上で作成した AAD アプリケーションのシークレットを使用するアプリケーションによって、この Finance and Operations 環境を呼び出して仮想エンティティの機能にアクセスできるようになります。</span><span class="sxs-lookup"><span data-stu-id="ca584-141">After completing this step, any application with the secret of the AAD application create above will be able to call this Finance and Operations environment and access the virtual entity functionality.</span></span>

<span data-ttu-id="ca584-142">次の手順では、このプロセスを Finance and Operations アプリで実行していきます。</span><span class="sxs-lookup"><span data-stu-id="ca584-142">The next steps walk through this process in Finance and Operations apps.</span></span>

1.  <span data-ttu-id="ca584-143">Finance and Operations で、**システム管理 \> ユーザー \> ユーザー**の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="ca584-143">In Finance and Operations, go to **System Administration \> Users \> Users**.</span></span>

2.  <span data-ttu-id="ca584-144">**新規作成**を選択して、新しいユーザーを追加します。</span><span class="sxs-lookup"><span data-stu-id="ca584-144">Select **New** to add a new user.</span></span> <span data-ttu-id="ca584-145">次の情報を入力します。</span><span class="sxs-lookup"><span data-stu-id="ca584-145">Enter the following information:</span></span>

    - <span data-ttu-id="ca584-146">**ユーザー ID**: **cdsintegration** (または別の値) を入力します。</span><span class="sxs-lookup"><span data-stu-id="ca584-146">**User ID** - Enter **cdsintegration** (or a different value).</span></span>

    - <span data-ttu-id="ca584-147">**ユーザー名**: **cds integration** (または別の値) を入力します。</span><span class="sxs-lookup"><span data-stu-id="ca584-147">**User name** - Enter **cds integration** (or a different value).</span></span>

    - <span data-ttu-id="ca584-148">**プロバイダー**: 既定値をそのまま使います。</span><span class="sxs-lookup"><span data-stu-id="ca584-148">**Provider** - Leave at the default value.</span></span>

    - <span data-ttu-id="ca584-149">**電子メール**: **cdsintegration** (または別の値) を入力します (有効な電子メール アカウントである必要は*ありません*)。</span><span class="sxs-lookup"><span data-stu-id="ca584-149">**Email** - Enter **cdsintegration** (or a different value, does *not* need to be a valid email account).</span></span>

    - <span data-ttu-id="ca584-150">このユーザーにセキュリティ ロール **CDS 仮想エンティティ アプリケーション**を割り当てます。</span><span class="sxs-lookup"><span data-stu-id="ca584-150">Assign the security role **CDS virtual entity application** to this user.</span></span>

    - <span data-ttu-id="ca584-151">**システム ユーザー**を含む他のすべてのロールを削除します。</span><span class="sxs-lookup"><span data-stu-id="ca584-151">Remove all other roles including **System user**.</span></span>

3.  <span data-ttu-id="ca584-152">**システム管理 \> 設定 \> Azure Active Directory アプリケーション** の順に移動して Common Data Service を登録します。</span><span class="sxs-lookup"><span data-stu-id="ca584-152">Go to **System Administration \> Setup \> Azure Active Directory applications** to register Common Data Service.</span></span> 

    - <span data-ttu-id="ca584-153">新しい行を追加します。</span><span class="sxs-lookup"><span data-stu-id="ca584-153">Add a new row.</span></span>

    - <span data-ttu-id="ca584-154">**クライアント ID**: 上で作成された**アプリケーション (クライアント) ID**</span><span class="sxs-lookup"><span data-stu-id="ca584-154">**Client ID** - The **Application (client) ID** created above</span></span>

    - <span data-ttu-id="ca584-155">**名前**: **CDS 統合** (または別の名前) を入力します。</span><span class="sxs-lookup"><span data-stu-id="ca584-155">**Name** - Enter **CDS Integration** (or a different name).</span></span>

    - <span data-ttu-id="ca584-156">**ユーザー ID**: 上記で作成されたユーザー ID。</span><span class="sxs-lookup"><span data-stu-id="ca584-156">**User ID** - The user ID created above.</span></span>

<span data-ttu-id="ca584-157">プロセスの次の手順では、接続先の Finance and Operations インスタンスに Common Data Service を提供します。</span><span class="sxs-lookup"><span data-stu-id="ca584-157">The next step in the process is to provide Common Data Service with the Finance and Operations instance to connect to.</span></span> <span data-ttu-id="ca584-158">以下の手順では、プロセスのこの部分について説明します。</span><span class="sxs-lookup"><span data-stu-id="ca584-158">The following steps walk through this part of the process.</span></span>

1.  <span data-ttu-id="ca584-159">Common Data Service では、**詳細設定 \> 管理 \> 仮想エンティティ データ ソース**に移動します。</span><span class="sxs-lookup"><span data-stu-id="ca584-159">In Common Data Service, go to **Advanced Settings \> Administration \> Virtual Entity Data Sources**.</span></span>

2.  <span data-ttu-id="ca584-160">"Finance and Operations" というデータ ソースを選択します。</span><span class="sxs-lookup"><span data-stu-id="ca584-160">Select the data source named “Finance and Operations”.</span></span>

3.  <span data-ttu-id="ca584-161">上記の手順に従って情報を入力します。</span><span class="sxs-lookup"><span data-stu-id="ca584-161">Fill in the information from the steps above.</span></span>

    - <span data-ttu-id="ca584-162">**ターゲット URL**: Finance and Operations にアクセスできる URL。</span><span class="sxs-lookup"><span data-stu-id="ca584-162">**Target URL** - The URL at which you can access Finance and Operations.</span></span>

    - <span data-ttu-id="ca584-163">**OAuth URL** - https://login.windows.net/</span><span class="sxs-lookup"><span data-stu-id="ca584-163">**OAuth URL** - https://login.windows.net/</span></span>

    - <span data-ttu-id="ca584-164">**テナント ID**: "contoso.com" などのテナント。</span><span class="sxs-lookup"><span data-stu-id="ca584-164">**Tenant ID** - Your tenant, such as “contoso.com”.</span></span>

    - <span data-ttu-id="ca584-165">**AAD アプリケーション ID**: 上で作成された**アプリケーション (クライアント) ID**。</span><span class="sxs-lookup"><span data-stu-id="ca584-165">**AAD Application ID** - The **Application (client) ID** created above.</span></span>

    - <span data-ttu-id="ca584-166">**AAD アプリケーション シークレット**: 上で生成されたシークレット。</span><span class="sxs-lookup"><span data-stu-id="ca584-166">**AAD Application Secret** - The secret generated above.</span></span>

    - <span data-ttu-id="ca584-167">**AAD リソース**: 00000015-0000-0000-c000-000000000000 と入力します (これは、Finance and Operations を表す AAD アプリケーションです。常に同じ値であることを表します)。</span><span class="sxs-lookup"><span data-stu-id="ca584-167">**AAD Resource** - Enter 00000015-0000-0000-c000-000000000000 (this is the AAD application representing Finance and Operations, and should always be this same value).</span></span>

4.  <span data-ttu-id="ca584-168">変更を保存します。</span><span class="sxs-lookup"><span data-stu-id="ca584-168">Save the changes.</span></span>

## <a name="enabling-virtual-entities"></a><span data-ttu-id="ca584-169">仮想エンティティの有効化</span><span class="sxs-lookup"><span data-stu-id="ca584-169">Enabling virtual entities</span></span>

<span data-ttu-id="ca584-170">Finance and Operations には多数の OData 対応エンティティが含まれているため、既定では、エンティティは Common Data Service の仮想エンティティとしては使用できません。</span><span class="sxs-lookup"><span data-stu-id="ca584-170">Due to the large number of OData enabled entities available in Finance and Operations, by default, the entities are not available as virtual entities in Common Data Service.</span></span> <span data-ttu-id="ca584-171">次の手順では、必要に応じてエンティティを仮想にすることができます。</span><span class="sxs-lookup"><span data-stu-id="ca584-171">The following steps allow for enabling entities to be virtual, as needed.</span></span>

1. <span data-ttu-id="ca584-172">Common Data Service で、**高度な検索**に移動します。</span><span class="sxs-lookup"><span data-stu-id="ca584-172">In Common Data Service, go to **Advanced find**.</span></span>

2. <span data-ttu-id="ca584-173">[利用可能な Finance and Operations エンティティ] を探して、**結果** を選択します。</span><span class="sxs-lookup"><span data-stu-id="ca584-173">Look for “Available Finance and Operations Entities” and select **Results**.</span></span>

![カタログ](../media/fovecatalog.png)

3. <span data-ttu-id="ca584-175">有効にするエンティティを検索して開きます。</span><span class="sxs-lookup"><span data-stu-id="ca584-175">Locate and open the entity that you want to enable.</span></span>

4. <span data-ttu-id="ca584-176">**表示** を **はい** に設定して保存します。</span><span class="sxs-lookup"><span data-stu-id="ca584-176">Set **Visible** to **Yes** and save.</span></span> <span data-ttu-id="ca584-177">これにより、仮想エンティティが生成され、[高度な検索] ダイアログ ボックスなどの適切なすべてのメニューに表示されるようになります。</span><span class="sxs-lookup"><span data-stu-id="ca584-177">This will generate the virtual entity, so that it will appear in all of the appropriate menus, such as the advanced find dialog box.</span></span>

![VE の有効化](../media/foveenable.png)

## <a name="refreshing-virtual-entity-metadata"></a><span data-ttu-id="ca584-179">仮想エンティティ メタデータの更新</span><span class="sxs-lookup"><span data-stu-id="ca584-179">Refreshing virtual entity metadata</span></span>

<span data-ttu-id="ca584-180">仮想エンティティ メタデータは、Finance and Operations のエンティティ メタデータが変更されたと想定される場合に、強制的に更新できます。</span><span class="sxs-lookup"><span data-stu-id="ca584-180">The virtual entity metadata can be force-refreshed when it is expected for the entity metadata in Finance and Operations to have changed.</span></span> <span data-ttu-id="ca584-181">これを行うには、**更新** を **はい** に設定して保存します。</span><span class="sxs-lookup"><span data-stu-id="ca584-181">This can be done by setting **Refresh** to **Yes** and saving.</span></span> <span data-ttu-id="ca584-182">これにより、Finance and Operations の最新のエンティティ定義が Common Data Service に同期され、仮想エンティティが更新されます。</span><span class="sxs-lookup"><span data-stu-id="ca584-182">This will sync the latest entity definition from Finance and Operations to Common Data Service and update the virtual entity.</span></span>

<a name="referencing-virtual-entities"></a><span data-ttu-id="ca584-183">仮想エンティティの参照</span><span class="sxs-lookup"><span data-stu-id="ca584-183">Referencing virtual entities</span></span>
----------------------------

<span data-ttu-id="ca584-184">仮想エンティティはすべて MicrosoftOperationsERPVE ソリューションで生成され、API によって管理されます。</span><span class="sxs-lookup"><span data-stu-id="ca584-184">The virtual entities are all generated in the MicrosoftOperationsERPVE solution, which is API Managed.</span></span> <span data-ttu-id="ca584-185">つまり、エンティティの表示/非表示を変更してもソリューションの項目は変化しますが、それでも依存できるマネージド ソリューションになります。</span><span class="sxs-lookup"><span data-stu-id="ca584-185">That means the items in the solution change as you make entities visible/hidden, but it is still a managed solution that you can take dependency on.</span></span> <span data-ttu-id="ca584-186">標準 ALM フローでは、ISV ソリューションの **既存の追加** オプションを使用して、このソリューションから仮想エンティティに対する標準参照を取得するだけです。</span><span class="sxs-lookup"><span data-stu-id="ca584-186">The standard ALM flow would be to just take a standard reference to a virtual entity from this solution with the **Add existing** option in the ISV solution.</span></span> <span data-ttu-id="ca584-187">これにより、ソリューションの依存関係が見つからないと表示され、ソリューション インポート時にチェックされます。</span><span class="sxs-lookup"><span data-stu-id="ca584-187">It will then show as a missing dependency of the solution and be checked at solution import time.</span></span> <span data-ttu-id="ca584-188">インポート中に、指定された仮想エンティティがまだ存在しない場合は、追加の作業を必要とすることなく、自動的に表示されます。</span><span class="sxs-lookup"><span data-stu-id="ca584-188">During import if a specified virtual entity does not yet exist, it would automatically be made visible without needing additional work.</span></span>

<span data-ttu-id="ca584-189">仮想エンティティを使用するには</span><span class="sxs-lookup"><span data-stu-id="ca584-189">To consume virtual entities:</span></span>

1.  <span data-ttu-id="ca584-190">Common Data Service で通常どおり別個のソリューションを作成します。これには、消費ロジックが含められます。</span><span class="sxs-lookup"><span data-stu-id="ca584-190">Create a separate solution as usual in Common Data Service, which will contain the consuming logic.</span></span>

2.  <span data-ttu-id="ca584-191">**エンティティ \> 既存の追加** を選択します。</span><span class="sxs-lookup"><span data-stu-id="ca584-191">Select **Entities \> Add Existing**.</span></span> <span data-ttu-id="ca584-192">一覧から参照する仮想エンティティを選択します。</span><span class="sxs-lookup"><span data-stu-id="ca584-192">Select the virtual entity that you want to reference from the list.</span></span>

3.  <span data-ttu-id="ca584-193">追加する資産の選択を求めるメッセージが表示されたら、カスタマイズするフォーム、ビュー、またはその他の要素を選択し、**完了** を選択します。</span><span class="sxs-lookup"><span data-stu-id="ca584-193">When prompted to select assets to add, select any forms, views, or other elements that you want to customize, then select **Finish**.</span></span>

<span data-ttu-id="ca584-194">開発ツールから、フォームなどの既存の要素を仮想エンティティに対して変更することができます。</span><span class="sxs-lookup"><span data-stu-id="ca584-194">From the development tooling, existing elements such as forms can be modified for the virtual entity.</span></span> <span data-ttu-id="ca584-195">また、新しいフォーム、ビュー、およびその他の要素を追加することもできます。</span><span class="sxs-lookup"><span data-stu-id="ca584-195">Additionally, new forms, views, and other elements can also be added.</span></span>

![ソリューション](../media/fovesolution.png)

<span data-ttu-id="ca584-197">ソリューションをエクスポートすると、MicrosoftOperationsERPVE ソリューションで生成された仮想エンティティへのハード依存関係が含められます。</span><span class="sxs-lookup"><span data-stu-id="ca584-197">When the solution is exported, it will contain hard dependencies on the virtual entity generated in the MicrosoftOperationsERPVE solution.</span></span>
