---
title: Finance and Operations および Dataverse 管理リファレンス
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
ms.openlocfilehash: c39d18688128b999d689962b9b74e6f605f9412e
ms.sourcegitcommit: cc9921295f26804259cc9ec5137788ec9f2a4c6f
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/08/2021
ms.locfileid: "4839565"
---
# <a name="finance-and-operations-and-dataverse-admin-reference"></a><span data-ttu-id="13a37-103">Finance and Operations および Dataverse 管理リファレンス</span><span class="sxs-lookup"><span data-stu-id="13a37-103">Finance and Operations and Dataverse admin reference</span></span>

[!include[banner](../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

> [!IMPORTANT]
> <span data-ttu-id="13a37-104">この機能には、[Finance and Operations](../get-started/whats-new-platform-update-10-0-12.md) および Dataverse の更新プログラム 189 のサービスが必要です。</span><span class="sxs-lookup"><span data-stu-id="13a37-104">This functionality requires [Platform updates for version 10.0.12 of Finance and Operations apps](../get-started/whats-new-platform-update-10-0-12.md) and service update 189 for Dataverse.</span></span> <span data-ttu-id="13a37-105">Dataverse のリリース情報は、[最新バージョンの利用可能性](https://docs.microsoft.com/business-applications-release-notes/dynamics/released-versions/dynamics-365ce#all-version-availability)ページに発行されています。</span><span class="sxs-lookup"><span data-stu-id="13a37-105">The release information for Dataverse is published on the [latest version availability page](https://docs.microsoft.com/business-applications-release-notes/dynamics/released-versions/dynamics-365ce#all-version-availability).</span></span>

<span data-ttu-id="13a37-106">このトピックでは、Dataverse で Finance and Operations アプリの仮想エンティティを設定およびコンフィギュレーションする方法について手順を追って説明します。</span><span class="sxs-lookup"><span data-stu-id="13a37-106">This topic provides step-by-step instructions about how to set up and configure virtual entities for Finance and Operations apps in Dataverse.</span></span>

## <a name="getting-the-solution"></a><span data-ttu-id="13a37-107">ソリューションの入手</span><span class="sxs-lookup"><span data-stu-id="13a37-107">Getting the solution</span></span>
<span data-ttu-id="13a37-108">Finance and Operations 仮想エンティティの Dataverse ソリューションは、Microsoft AppSource 仮想エンティティ ソリューションからダウンロードする必要があります。</span><span class="sxs-lookup"><span data-stu-id="13a37-108">The Dataverse solution for Finance and Operations virtual entities must be installed from Microsoft AppSource virtual entity solution.</span></span> <span data-ttu-id="13a37-109">詳細については、[Finance and Operations 仮想エンティティ](https://appsource.microsoft.com/product/dynamics-crm/mscrm.finance_and_operations_virtual_entity) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="13a37-109">For more information, see [Finance and Operations virtual entity](https://appsource.microsoft.com/product/dynamics-crm/mscrm.finance_and_operations_virtual_entity).</span></span>

<span data-ttu-id="13a37-110">次のソリューションが Dataverse にインストールされていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="13a37-110">Ensure the following solutions are installed in Dataverse.</span></span>

- <span data-ttu-id="13a37-111">**Dynamics365Company**: すべての Finance and Operations エンティティによって参照される **会社** エンティティを、PrimaryCompanyContext メタデータ値と共に追加します。</span><span class="sxs-lookup"><span data-stu-id="13a37-111">**Dynamics365Company** - This adds the **Company** entity, which is referenced by all Finance and Operations entities with a PrimaryCompanyContext metadata value.</span></span>

- <span data-ttu-id="13a37-112">**MicrosoftOperationsVESupport**: これにより、Finance and Operations 仮想エンティティ機能のコア サポートが提供されます。</span><span class="sxs-lookup"><span data-stu-id="13a37-112">**MicrosoftOperationsVESupport** - This provides the core support for the Finance and Operations virtual entity feature.</span></span>

- <span data-ttu-id="13a37-113">**MicrosoftOperationsERPCatalog**: これは、mserp_financeandoperationsentity 仮想エンティティを通じて使用できる Finance and Operations エンティティの一覧を提供します。</span><span class="sxs-lookup"><span data-stu-id="13a37-113">**MicrosoftOperationsERPCatalog** - This provides a list of available Finance and Operations entities through the mserp_financeandoperationsentity virtual entity.</span></span>

- <span data-ttu-id="13a37-114">**MicrosoftOperationsERPVE**: これは、表示されるときに生成された仮想エンティティを含む、API マネージド ソリューションです。</span><span class="sxs-lookup"><span data-stu-id="13a37-114">**MicrosoftOperationsERPVE** - This is the API-managed solution, which will contain the generated virtual entities as they are made visible.</span></span>

## <a name="authentication-and-authorization"></a><span data-ttu-id="13a37-115">認証と承認</span><span class="sxs-lookup"><span data-stu-id="13a37-115">Authentication and authorization</span></span>

<span data-ttu-id="13a37-116">ソリューションを Dataverse 環境にインポートした後は、両方の環境を相互に接続するように設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="13a37-116">After the solutions are imported in the Dataverse environment, both environments must be set up to connect to each other.</span></span> <span data-ttu-id="13a37-117">Dataverse は、Azure Active Directory (AAD) アプリケーションに基づいて、サービス ツー サービス (S2S) 認証を使用して Finance and Operations を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="13a37-117">Dataverse will call Finance and Operations using Service-to-Service (S2S) authentication, based on an Azure Active Directory (AAD) application.</span></span> <span data-ttu-id="13a37-118">この新しい AAD アプリケーションは、Dataverse 環境の単一のインスタンスを表します。</span><span class="sxs-lookup"><span data-stu-id="13a37-118">This new AAD application represents the single instance of the Dataverse environment.</span></span> <span data-ttu-id="13a37-119">Dataverse と Finance and Operations の環境の組み合わせが複数存在する場合は、ペアごとに独立した AAD アプリケーションを作成して、Finance and Operations 環境と Dataverse 環境の正しいペア間で確実に接続が確立されるようにする必要があります。</span><span class="sxs-lookup"><span data-stu-id="13a37-119">If you have multiple pairs of Dataverse and Finance and Operations environments, separate AAD applications for each pair must be created to ensure connections are established between the correct pair of Finance and Operations and Dataverse environments.</span></span> <span data-ttu-id="13a37-120">次の手順は、AAD アプリケーションの作成方法を示しています。</span><span class="sxs-lookup"><span data-stu-id="13a37-120">The following procedure shows the creation of the AAD application.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="13a37-121">AAD アプリケーションは、Finance and Operations と同じテナントに作成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="13a37-121">The AAD application must be created on the same tenant as Finance and Operations.</span></span>

1.  <span data-ttu-id="13a37-122"><https://portal.azure.com> **\> Azure Active Directory \> アプリの登録** に移動します。</span><span class="sxs-lookup"><span data-stu-id="13a37-122">Go to <https://portal.azure.com> **\> Azure Active Directory \> App registrations**.</span></span>

2.  <span data-ttu-id="13a37-123">**新規登録** を選択します。</span><span class="sxs-lookup"><span data-stu-id="13a37-123">Select **New Registration**.</span></span> <span data-ttu-id="13a37-124">次の情報を入力します。</span><span class="sxs-lookup"><span data-stu-id="13a37-124">Enter the following information:</span></span>

    - <span data-ttu-id="13a37-125">**名前**: 一意の名前を入力します。</span><span class="sxs-lookup"><span data-stu-id="13a37-125">**Name** - Enter a unique name.</span></span>

    - <span data-ttu-id="13a37-126">**アカウント タイプ**: **任意の Azure AD ディレクトリ** を入力します (単一またはマルチテナント)。</span><span class="sxs-lookup"><span data-stu-id="13a37-126">**Account type** - Enter **Any Azure AD directory** (single or multi-tenant).</span></span>

    - <span data-ttu-id="13a37-127">**リダイレクト URI**: 空白のままにします。</span><span class="sxs-lookup"><span data-stu-id="13a37-127">**Redirect URI** - Leave blank.</span></span>

    - <span data-ttu-id="13a37-128">**登録** を選択します。</span><span class="sxs-lookup"><span data-stu-id="13a37-128">Select **Register**.</span></span>

    - <span data-ttu-id="13a37-129">**アプリケーション (クライアント) ID** の値をメモしておきます。後の手順で必要となります。</span><span class="sxs-lookup"><span data-stu-id="13a37-129">Make note of the **Application (client) ID** value, you will need it later.</span></span>

3.  <span data-ttu-id="13a37-130">アプリケーションの対称キーを作成します。</span><span class="sxs-lookup"><span data-stu-id="13a37-130">Create a symmetric key for the application.</span></span>

    - <span data-ttu-id="13a37-131">新しく作成されたアプリケーションで **証明書とシークレット** を選択します。</span><span class="sxs-lookup"><span data-stu-id="13a37-131">Select **Certificates & secrets** in the newly created application.</span></span>

    - <span data-ttu-id="13a37-132">**新しいクライアント シークレット** を選択します。</span><span class="sxs-lookup"><span data-stu-id="13a37-132">Select **New client secret**.</span></span>

    - <span data-ttu-id="13a37-133">説明と有効期限を入力します。</span><span class="sxs-lookup"><span data-stu-id="13a37-133">Provide a description and an expiration date.</span></span>

    - <span data-ttu-id="13a37-134">**保存** を選択します。</span><span class="sxs-lookup"><span data-stu-id="13a37-134">Select **Save**.</span></span> <span data-ttu-id="13a37-135">キーが作成され、表示されます。</span><span class="sxs-lookup"><span data-stu-id="13a37-135">A key will be created and displayed.</span></span> <span data-ttu-id="13a37-136">この値を後で使用するためにコピーします。</span><span class="sxs-lookup"><span data-stu-id="13a37-136">Copy this value for later use.</span></span>

<span data-ttu-id="13a37-137">上で作成した AAD アプリケーションは、Dataverse によって Finance and Operations アプリを呼び出すために使用されます。</span><span class="sxs-lookup"><span data-stu-id="13a37-137">The AAD application created above will be used by Dataverse to call Finance and Operations apps.</span></span> <span data-ttu-id="13a37-138">したがって、Finance and Operations によって信頼され、Finance and Operations で適切な権限を持つユーザー アカウントに関連付けられている必要があり ます。</span><span class="sxs-lookup"><span data-stu-id="13a37-138">As such, it must be trusted by Finance and Operations and associated with a user account with the appropriate rights in Finance and Operations.</span></span> <span data-ttu-id="13a37-139">Finance and Operations では、特殊サービス ユーザーは、仮想エンティティ機能に対する権限 *のみ* で作成することができます。その他の権限は必要ありません。</span><span class="sxs-lookup"><span data-stu-id="13a37-139">A special service user must be created in Finance and Operations with rights *only* to the virtual entity functionality, and no other rights.</span></span> <span data-ttu-id="13a37-140">この手順を完了すると、上で作成した AAD アプリケーションのシークレットを使用するアプリケーションによって、この Finance and Operations 環境を呼び出して仮想エンティティの機能にアクセスできるようになります。</span><span class="sxs-lookup"><span data-stu-id="13a37-140">After completing this step, any application with the secret of the AAD application create above will be able to call this Finance and Operations environment and access the virtual entity functionality.</span></span>

<span data-ttu-id="13a37-141">次の手順では、このプロセスを Finance and Operations アプリで実行していきます。</span><span class="sxs-lookup"><span data-stu-id="13a37-141">The next steps walk through this process in Finance and Operations apps.</span></span>

1.  <span data-ttu-id="13a37-142">Finance and Operations で、**システム管理 \> ユーザー \> ユーザー** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="13a37-142">In Finance and Operations, go to **System Administration \> Users \> Users**.</span></span>

2.  <span data-ttu-id="13a37-143">**新規作成** を選択して、新しいユーザーを追加します。</span><span class="sxs-lookup"><span data-stu-id="13a37-143">Select **New** to add a new user.</span></span> <span data-ttu-id="13a37-144">次の情報を入力します。</span><span class="sxs-lookup"><span data-stu-id="13a37-144">Enter the following information:</span></span>

    - <span data-ttu-id="13a37-145">**ユーザー ID**: **dataverseintegration** (または別の値) を入力します。</span><span class="sxs-lookup"><span data-stu-id="13a37-145">**User ID** - Enter **dataverseintegration** (or a different value).</span></span>

    - <span data-ttu-id="13a37-146">**ユーザー名** - **dataverse 統合** (または別の値) を入力します。</span><span class="sxs-lookup"><span data-stu-id="13a37-146">**User name** - Enter **dataverse integration** (or a different value).</span></span>

    - <span data-ttu-id="13a37-147">**プロバイダー** - **NonAAD** に設定します。</span><span class="sxs-lookup"><span data-stu-id="13a37-147">**Provider** - Set to **NonAAD**.</span></span>

    - <span data-ttu-id="13a37-148">**電子メール**: **dataverseintegration** (または別の値) を入力します (有効な電子メール アカウントである必要は *ありません*)。</span><span class="sxs-lookup"><span data-stu-id="13a37-148">**Email** - Enter **dataverseintegration** (or a different value, does *not* need to be a valid email account).</span></span>

    - <span data-ttu-id="13a37-149">このユーザーにセキュリティ ロール **CDS 仮想エンティティ アプリケーション** を割り当てます。</span><span class="sxs-lookup"><span data-stu-id="13a37-149">Assign the security role **CDS virtual entity application** to this user.</span></span>

    - <span data-ttu-id="13a37-150">**システム ユーザー** を含む他のすべてのロールを削除します。</span><span class="sxs-lookup"><span data-stu-id="13a37-150">Remove all other roles including **System user**.</span></span>

3.  <span data-ttu-id="13a37-151">**システム管理 \> 設定 \> Azure Active Directory アプリケーション** の順に移動して Dataverse を登録します。</span><span class="sxs-lookup"><span data-stu-id="13a37-151">Go to **System Administration \> Setup \> Azure Active Directory applications** to register Dataverse.</span></span> 

    - <span data-ttu-id="13a37-152">新しい行を追加します。</span><span class="sxs-lookup"><span data-stu-id="13a37-152">Add a new row.</span></span>

    - <span data-ttu-id="13a37-153">**クライアント ID**: 上で作成された **アプリケーション (クライアント) ID**</span><span class="sxs-lookup"><span data-stu-id="13a37-153">**Client ID** - The **Application (client) ID** created above</span></span>

    - <span data-ttu-id="13a37-154">**名前** - **Dataverse 統合** (または別の名前) を入力します。</span><span class="sxs-lookup"><span data-stu-id="13a37-154">**Name** - Enter **Dataverse Integration** (or a different name).</span></span>

    - <span data-ttu-id="13a37-155">**ユーザー ID**: 上記で作成されたユーザー ID。</span><span class="sxs-lookup"><span data-stu-id="13a37-155">**User ID** - The user ID created above.</span></span>

<span data-ttu-id="13a37-156">プロセスの次の手順では、接続先の Finance and Operations インスタンスに Dataverse を提供します。</span><span class="sxs-lookup"><span data-stu-id="13a37-156">The next step in the process is to provide Dataverse with the Finance and Operations instance to connect to.</span></span> <span data-ttu-id="13a37-157">以下の手順では、プロセスのこの部分について説明します。</span><span class="sxs-lookup"><span data-stu-id="13a37-157">The following steps walk through this part of the process.</span></span>

1.  <span data-ttu-id="13a37-158">Dataverse では、**詳細設定 \> 管理 \> 仮想エンティティ データ ソース** に移動します。</span><span class="sxs-lookup"><span data-stu-id="13a37-158">In Dataverse, go to **Advanced Settings \> Administration \> Virtual Entity Data Sources**.</span></span>

2.  <span data-ttu-id="13a37-159">"Finance and Operations" というデータ ソースを選択します。</span><span class="sxs-lookup"><span data-stu-id="13a37-159">Select the data source named “Finance and Operations”.</span></span>

3.  <span data-ttu-id="13a37-160">上記の手順に従って情報を入力します。</span><span class="sxs-lookup"><span data-stu-id="13a37-160">Fill in the information from the steps above.</span></span>

    - <span data-ttu-id="13a37-161">**ターゲット URL**: Finance and Operations にアクセスできる URL。</span><span class="sxs-lookup"><span data-stu-id="13a37-161">**Target URL** - The URL at which you can access Finance and Operations.</span></span>

    - <span data-ttu-id="13a37-162">**OAuth URL** - https://login.windows.net/</span><span class="sxs-lookup"><span data-stu-id="13a37-162">**OAuth URL** - https://login.windows.net/</span></span>

    - <span data-ttu-id="13a37-163">**テナント ID**: "contoso.com" などのテナント。</span><span class="sxs-lookup"><span data-stu-id="13a37-163">**Tenant ID** - Your tenant, such as “contoso.com”.</span></span>

    - <span data-ttu-id="13a37-164">**AAD アプリケーション ID**: 上で作成された **アプリケーション (クライアント) ID**。</span><span class="sxs-lookup"><span data-stu-id="13a37-164">**AAD Application ID** - The **Application (client) ID** created above.</span></span>

    - <span data-ttu-id="13a37-165">**AAD アプリケーション シークレット**: 上で生成されたシークレット。</span><span class="sxs-lookup"><span data-stu-id="13a37-165">**AAD Application Secret** - The secret generated above.</span></span>

    - <span data-ttu-id="13a37-166">**AAD リソース**: 00000015-0000-0000-c000-000000000000 と入力します (これは、Finance and Operations を表す AAD アプリケーションです。常に同じ値であることを表します)。</span><span class="sxs-lookup"><span data-stu-id="13a37-166">**AAD Resource** - Enter 00000015-0000-0000-c000-000000000000 (this is the AAD application representing Finance and Operations, and should always be this same value).</span></span>

4.  <span data-ttu-id="13a37-167">変更を保存します。</span><span class="sxs-lookup"><span data-stu-id="13a37-167">Save the changes.</span></span>

## <a name="enabling-virtual-entities"></a><span data-ttu-id="13a37-168">仮想エンティティの有効化</span><span class="sxs-lookup"><span data-stu-id="13a37-168">Enabling virtual entities</span></span>

<span data-ttu-id="13a37-169">Finance and Operations には多数の OData 対応エンティティが含まれているため、既定では、エンティティは Dataverse の仮想エンティティとしては使用できません。</span><span class="sxs-lookup"><span data-stu-id="13a37-169">Due to the large number of OData enabled entities available in Finance and Operations, by default, the entities are not available as virtual entities in Dataverse.</span></span> <span data-ttu-id="13a37-170">次の手順では、必要に応じてエンティティを仮想にすることができます。</span><span class="sxs-lookup"><span data-stu-id="13a37-170">The following steps allow for enabling entities to be virtual, as needed.</span></span>

1. <span data-ttu-id="13a37-171">Dataverse で、**高度な検索** に移動します (フィルター アイコン)。</span><span class="sxs-lookup"><span data-stu-id="13a37-171">In Dataverse, go to **Advanced find** (filter icon).</span></span>

2. <span data-ttu-id="13a37-172">[利用可能な Finance and Operations エンティティ] を探して、**結果** を選択します。</span><span class="sxs-lookup"><span data-stu-id="13a37-172">Look for “Available Finance and Operations Entities” and select **Results**.</span></span>

![カタログ](../media/fovecatalog.png)

3. <span data-ttu-id="13a37-174">有効にするエンティティを検索して開きます。</span><span class="sxs-lookup"><span data-stu-id="13a37-174">Locate and open the entity that you want to enable.</span></span>

4. <span data-ttu-id="13a37-175">**表示** を **はい** に設定して保存します。</span><span class="sxs-lookup"><span data-stu-id="13a37-175">Set **Visible** to **Yes** and save.</span></span> <span data-ttu-id="13a37-176">これにより、仮想エンティティが生成され、[高度な検索] ダイアログ ボックスなどの適切なすべてのメニューに表示されるようになります。</span><span class="sxs-lookup"><span data-stu-id="13a37-176">This will generate the virtual entity, so that it will appear in all of the appropriate menus, such as the advanced find dialog box.</span></span>

![VE の有効化](../media/foveenable.png)

## <a name="refreshing-virtual-entity-metadata"></a><span data-ttu-id="13a37-178">仮想エンティティ メタデータの更新</span><span class="sxs-lookup"><span data-stu-id="13a37-178">Refreshing virtual entity metadata</span></span>

<span data-ttu-id="13a37-179">仮想エンティティ メタデータは、Finance and Operations のエンティティ メタデータが変更されたと想定される場合に、強制的に更新できます。</span><span class="sxs-lookup"><span data-stu-id="13a37-179">The virtual entity metadata can be force-refreshed when it is expected for the entity metadata in Finance and Operations to have changed.</span></span> <span data-ttu-id="13a37-180">これを行うには、**更新** を **はい** に設定して保存します。</span><span class="sxs-lookup"><span data-stu-id="13a37-180">This can be done by setting **Refresh** to **Yes** and saving.</span></span> <span data-ttu-id="13a37-181">これにより、Finance and Operations の最新のエンティティ定義が Dataverse に同期され、仮想エンティティが更新されます。</span><span class="sxs-lookup"><span data-stu-id="13a37-181">This will sync the latest entity definition from Finance and Operations to Dataverse and update the virtual entity.</span></span>

<a name="referencing-virtual-entities"></a><span data-ttu-id="13a37-182">仮想エンティティの参照</span><span class="sxs-lookup"><span data-stu-id="13a37-182">Referencing virtual entities</span></span>
----------------------------

<span data-ttu-id="13a37-183">仮想エンティティはすべて MicrosoftOperationsERPVE ソリューションで生成され、API によって管理されます。</span><span class="sxs-lookup"><span data-stu-id="13a37-183">The virtual entities are all generated in the MicrosoftOperationsERPVE solution, which is API Managed.</span></span> <span data-ttu-id="13a37-184">つまり、エンティティの表示/非表示を変更してもソリューションの項目は変化しますが、それでも依存できるマネージド ソリューションになります。</span><span class="sxs-lookup"><span data-stu-id="13a37-184">That means the items in the solution change as you make entities visible/hidden, but it is still a managed solution that you can take dependency on.</span></span> <span data-ttu-id="13a37-185">標準 ALM フローでは、ISV ソリューションの **既存の追加** オプションを使用して、このソリューションから仮想エンティティに対する標準参照を取得するだけです。</span><span class="sxs-lookup"><span data-stu-id="13a37-185">The standard ALM flow would be to just take a standard reference to a virtual entity from this solution with the **Add existing** option in the ISV solution.</span></span> <span data-ttu-id="13a37-186">これにより、ソリューションの依存関係が見つからないと表示され、ソリューション インポート時にチェックされます。</span><span class="sxs-lookup"><span data-stu-id="13a37-186">It will then show as a missing dependency of the solution and be checked at solution import time.</span></span> <span data-ttu-id="13a37-187">インポート中に、指定された仮想エンティティがまだ存在しない場合は、追加の作業を必要とすることなく、自動的に表示されます。</span><span class="sxs-lookup"><span data-stu-id="13a37-187">During import if a specified virtual entity does not yet exist, it would automatically be made visible without needing additional work.</span></span>

<span data-ttu-id="13a37-188">仮想エンティティを使用するには</span><span class="sxs-lookup"><span data-stu-id="13a37-188">To consume virtual entities:</span></span>

1.  <span data-ttu-id="13a37-189">Dataverse で通常どおり別個のソリューションを作成します。これには、消費ロジックが含められます。</span><span class="sxs-lookup"><span data-stu-id="13a37-189">Create a separate solution as usual in Dataverse, which will contain the consuming logic.</span></span>

2.  <span data-ttu-id="13a37-190">**エンティティ \> 既存の追加** を選択します。</span><span class="sxs-lookup"><span data-stu-id="13a37-190">Select **Entities \> Add Existing**.</span></span> <span data-ttu-id="13a37-191">一覧から参照する仮想エンティティを選択します。</span><span class="sxs-lookup"><span data-stu-id="13a37-191">Select the virtual entity that you want to reference from the list.</span></span>

3.  <span data-ttu-id="13a37-192">追加する資産の選択を求めるメッセージが表示されたら、カスタマイズするフォーム、ビュー、またはその他の要素を選択し、**完了** を選択します。</span><span class="sxs-lookup"><span data-stu-id="13a37-192">When prompted to select assets to add, select any forms, views, or other elements that you want to customize, then select **Finish**.</span></span>

<span data-ttu-id="13a37-193">開発ツールから、フォームなどの既存の要素を仮想エンティティに対して変更することができます。</span><span class="sxs-lookup"><span data-stu-id="13a37-193">From the development tooling, existing elements such as forms can be modified for the virtual entity.</span></span> <span data-ttu-id="13a37-194">また、新しいフォーム、ビュー、およびその他の要素を追加することもできます。</span><span class="sxs-lookup"><span data-stu-id="13a37-194">Additionally, new forms, views, and other elements can also be added.</span></span>

![ソリューション](../media/fovesolution.png)

<span data-ttu-id="13a37-196">ソリューションをエクスポートすると、MicrosoftOperationsERPVE ソリューションで生成された仮想エンティティへのハード依存関係が含められます。</span><span class="sxs-lookup"><span data-stu-id="13a37-196">When the solution is exported, it will contain hard dependencies on the virtual entity generated in the MicrosoftOperationsERPVE solution.</span></span>
