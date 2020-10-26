---
title: Common Data Service 仮想エンティティの構成
description: このトピックでは、Dynamics 365 Human Resources の仮想エンティティを構成する方法について説明します。 既存の仮想エンティティを生成および更新し、生成されたエンティティと使用可能なエンティティを分析します。
author: andreabichsel
manager: tfehr
ms.date: 10/05/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: CDSIntegrationAdministration
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-10-05
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 0848b7556100fba38fcab0aa2a1a109e2e055fc9
ms.sourcegitcommit: b89baab13e530b5b1f079231619c628309a4742d
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/05/2020
ms.locfileid: "3959578"
---
# <a name="configure-common-data-service-virtual-entities"></a><span data-ttu-id="7ee14-104">Common Data Service 仮想エンティティの構成</span><span class="sxs-lookup"><span data-stu-id="7ee14-104">Configure Common Data Service virtual entities</span></span>

[!include [banner](includes/preview-feature.md)]

<span data-ttu-id="7ee14-105">Dynamics 365 Human Resources は Common Data Service の仮想データ ソースです。</span><span class="sxs-lookup"><span data-stu-id="7ee14-105">Dynamics 365 Human Resources is a virtual data source in Common Data Service.</span></span> <span data-ttu-id="7ee14-106">このサービスでは、Common Data Service および Microsoft Power Platform からの作成、読み取り、更新、および削除 (CRUD) の完全な操作が提供されます。</span><span class="sxs-lookup"><span data-stu-id="7ee14-106">It provides full create, read, update, and delete (CRUD) operations from Common Data Service and Microsoft Power Platform.</span></span> <span data-ttu-id="7ee14-107">仮想エンティティのデータは Common Data Service には保存されませんが、アプリケーション データベースに保存されます。</span><span class="sxs-lookup"><span data-stu-id="7ee14-107">The data for virtual entities isn't stored in Common Data Service, but in the application database.</span></span> 

<span data-ttu-id="7ee14-108">Common Data Service から Human Resources エンティティに対して CRUD 操作を有効にするには、エンティティを Common Data Service の仮想エンティティとして使用できるようにする必要があります。</span><span class="sxs-lookup"><span data-stu-id="7ee14-108">To enable CRUD operations on Human Resources entities from Common Data Service, you must make the entities available as virtual entities in Common Data Service.</span></span> <span data-ttu-id="7ee14-109">これにより、Human Resources のデータで Common Data Service と Microsoft Power Platform から CRUD 操作を実行できます。</span><span class="sxs-lookup"><span data-stu-id="7ee14-109">This lets you perform CRUD operations from Common Data Service and Microsoft Power Platform on data that's in Human Resources.</span></span> <span data-ttu-id="7ee14-110">また、この操作では、Human Resources のビジネス ロジックの完全な検証をサポートしているため、エンティティにデータを書き込むときにデータの整合性を確保できます。</span><span class="sxs-lookup"><span data-stu-id="7ee14-110">The operations also support the full business logic validations of Human Resources to ensure data integrity when writing data to the entities.</span></span>

## <a name="available-virtual-entities-for-human-resources"></a><span data-ttu-id="7ee14-111">Human Resources で使用可能な仮想エンティティ</span><span class="sxs-lookup"><span data-stu-id="7ee14-111">Available virtual entities for Human Resources</span></span>

<span data-ttu-id="7ee14-112">Human Resources のすべての Open Data Protocol (OData) エンティティは、Common Data Service の仮想エンティティとして使用できます。</span><span class="sxs-lookup"><span data-stu-id="7ee14-112">All Open Data Protocol (OData) entities in Human Resources are available as virtual entities in Common Data Service.</span></span> <span data-ttu-id="7ee14-113">また、Power Platform で使用することもできます。</span><span class="sxs-lookup"><span data-stu-id="7ee14-113">They're also available in Power Platform.</span></span> <span data-ttu-id="7ee14-114">データを Common Data Service にコピーまたは同期することなく、完全な CRUD 機能を備えた Human Resources からデータを使ってアプリとエクスペリエンスを直接ビルドできるようになりました。</span><span class="sxs-lookup"><span data-stu-id="7ee14-114">You can now build apps and experiences with data directly from Human Resources with full CRUD capability, without copying or synchronizing data to Common Data Service.</span></span> <span data-ttu-id="7ee14-115">Power Apps ポータルは、Human Resources の業務プロセスのコラボレーション シナリオを可能にする外部向けの Web サイトをビルドするために使用できます。</span><span class="sxs-lookup"><span data-stu-id="7ee14-115">You can use Power Apps portals to build external-facing websites that enable collaboration scenarios for business processes in Human Resources.</span></span>

<span data-ttu-id="7ee14-116">環境で有効になっている仮想エンティティの一覧を表示し、**Dynamics 365 HR 仮想エンティティ** ソリューションで [Power Apps](https://make.powerapps.com) のエンティティの操作を開始できます。</span><span class="sxs-lookup"><span data-stu-id="7ee14-116">You can view the list of virtual entities enabled in the environment, and begin working with the entities in [Power Apps](https://make.powerapps.com), in the **Dynamics 365 HR Virtual Entities** solution.</span></span>

![Power Apps の Dynamics 365 HR 仮想エンティティ](./media/hr-admin-integration-virtual-entities-power-apps.jpg)

## <a name="virtual-entities-versus-natural-entities"></a><span data-ttu-id="7ee14-118">仮想エンティティとナチュラル エンティティの比較</span><span class="sxs-lookup"><span data-stu-id="7ee14-118">Virtual entities versus natural entities</span></span>

<span data-ttu-id="7ee14-119">Human Resources の仮想エンティティは、Human Resources 向けに作成された Common Data Service のナチュラル エンティティとは異なります。</span><span class="sxs-lookup"><span data-stu-id="7ee14-119">Virtual entities for Human Resources aren't the same as the natural Common Data Service entities created for Human Resources.</span></span> <span data-ttu-id="7ee14-120">Human Resources のナチュラル エンティティは、Common Data Service の HCM Common ソリューションで個別に生成および管理されます。</span><span class="sxs-lookup"><span data-stu-id="7ee14-120">The natural entities for Human Resources are generated separately and maintained in the HCM Common solution in Common Data Service.</span></span> <span data-ttu-id="7ee14-121">ナチュラル エンティティでは、データが Common Data Service に保存され、Human Resources アプリケーション データベースとの同期が必要になります。</span><span class="sxs-lookup"><span data-stu-id="7ee14-121">With natural entities, the data is stored in Common Data Service and requires synchronization with the Human Resources application database.</span></span>

> [!NOTE]
> <span data-ttu-id="7ee14-122">Human Resources の Common Data Service ナチュラル エンティティの一覧については、「[Common Data Service エンティティ](https://docs.microsoft.com/dynamics365/human-resources/hr-developer-entities)」を参照してください 。</span><span class="sxs-lookup"><span data-stu-id="7ee14-122">For a list of the natural Common Data Service entities for Human Resources, see [Common Data Service entities](https://docs.microsoft.com/dynamics365/human-resources/hr-developer-entities).</span></span>

## <a name="setup"></a><span data-ttu-id="7ee14-123">段取り</span><span class="sxs-lookup"><span data-stu-id="7ee14-123">Setup</span></span>

<span data-ttu-id="7ee14-124">環境で仮想エンティティを有効にするには、次の設定手順に従います。</span><span class="sxs-lookup"><span data-stu-id="7ee14-124">Follow these setup steps to enable virtual entities in your environment.</span></span> 

### <a name="register-the-app-in-microsoft-azure"></a><span data-ttu-id="7ee14-125">アプリを Microsoft Azure に登録する</span><span class="sxs-lookup"><span data-stu-id="7ee14-125">Register the app in Microsoft Azure</span></span>

<span data-ttu-id="7ee14-126">最初に、Microsoft ID プラットフォームがアプリとユーザーに対して認証および承認サービスを提供できるように、Azure portal でアプリを登録する必要があります。</span><span class="sxs-lookup"><span data-stu-id="7ee14-126">First, you need to register the app in the Azure portal so the Microsoft identity platform can provide authentication and authorization services for the app and users.</span></span> <span data-ttu-id="7ee14-127">Azure でのアプリの登録に関する詳細については、「[クイックスタート: Microsoft ID プラットフォームでアプリケーションを登録する](https://docs.microsoft.com/azure/active-directory/develop/quickstart-register-app)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="7ee14-127">For more information about registering apps in Azure, see [Quickstart: Register an application with the Microsoft identity platform](https://docs.microsoft.com/azure/active-directory/develop/quickstart-register-app).</span></span>

1. <span data-ttu-id="7ee14-128">[Microsoft Azure ポータル](https://portal.azure.com)を開きます。</span><span class="sxs-lookup"><span data-stu-id="7ee14-128">Open the [Microsoft Azure portal](https://portal.azure.com).</span></span>

2. <span data-ttu-id="7ee14-129">Azure サービスの一覧で、**アプリの登録**を選択します。</span><span class="sxs-lookup"><span data-stu-id="7ee14-129">In the Azure services list, select **App registrations**.</span></span>

3. <span data-ttu-id="7ee14-130">**新規登録**を選択します。</span><span class="sxs-lookup"><span data-stu-id="7ee14-130">Select **New registration**.</span></span>

4. <span data-ttu-id="7ee14-131">**名前**フィールドに、アプリの内容を示す名前を入力します。</span><span class="sxs-lookup"><span data-stu-id="7ee14-131">In the **Name** field, enter a descriptive name for the app.</span></span> <span data-ttu-id="7ee14-132">たとえば、**Dynamics 365 Human Resources 仮想エンティティ**。</span><span class="sxs-lookup"><span data-stu-id="7ee14-132">For example, **Dynamics 365 Human Resources Virtual Entities**.</span></span>

5. <span data-ttu-id="7ee14-133">**リダイレクト URI** フィールドに、Human Resources のインスタンスの名前空間 URL を入力します。</span><span class="sxs-lookup"><span data-stu-id="7ee14-133">In the **Redirect URI** field, enter the namespace URL of your instance of Human Resources.</span></span>

6. <span data-ttu-id="7ee14-134">**登録** を選択します。</span><span class="sxs-lookup"><span data-stu-id="7ee14-134">Select **Register**.</span></span>

7. <span data-ttu-id="7ee14-135">登録が完了すると、Azure portal には、**アプリケーション (クライアント) ID** を含むアプリ登録の**概要**ウィンドウが表示されます。</span><span class="sxs-lookup"><span data-stu-id="7ee14-135">When registration completes, the Azure portal displays the app registration's **Overview** pane, which includes its **Application (client) ID**.</span></span> <span data-ttu-id="7ee14-136">この時点で**アプリケーション (クライアント) ID** をメモします。</span><span class="sxs-lookup"><span data-stu-id="7ee14-136">Take note of the **Application (client) ID** at this time.</span></span> <span data-ttu-id="7ee14-137">この情報は、[仮想エンティティ データ ソースを構成する](hr-admin-integration-common-data-service-virtual-entities.md#configure-the-virtual-entity-data-source)ときに入力します。</span><span class="sxs-lookup"><span data-stu-id="7ee14-137">You'll enter this information when you [Configure the virtual entity data source](hr-admin-integration-common-data-service-virtual-entities.md#configure-the-virtual-entity-data-source).</span></span>

8. <span data-ttu-id="7ee14-138">左側のナビゲーション ウィンドウで、**証明書とシークレット**を選択します。</span><span class="sxs-lookup"><span data-stu-id="7ee14-138">In the left navigation pane, select **Certificates and secrets**.</span></span>

9. <span data-ttu-id="7ee14-139">ページの**クライアント シークレット** セクションで、**新しいクライアント シークレット**を選択します。</span><span class="sxs-lookup"><span data-stu-id="7ee14-139">In the **Client secrets** section of the page, select **New client secret**.</span></span>

10. <span data-ttu-id="7ee14-140">説明を入力し、期間を選択して、**追加**を選択します。</span><span class="sxs-lookup"><span data-stu-id="7ee14-140">Provide a description, select a duration, and select **Add**.</span></span>

11. <span data-ttu-id="7ee14-141">シークレットの値を記録します。</span><span class="sxs-lookup"><span data-stu-id="7ee14-141">Record the secret's value.</span></span> <span data-ttu-id="7ee14-142">この情報は、[仮想エンティティ データ ソースを構成する](hr-admin-integration-common-data-service-virtual-entities.md#configure-the-virtual-entity-data-source)ときに入力します。</span><span class="sxs-lookup"><span data-stu-id="7ee14-142">You'll enter this information when you [Configure the virtual entity data source](hr-admin-integration-common-data-service-virtual-entities.md#configure-the-virtual-entity-data-source).</span></span>

    > [!IMPORTANT]
    > <span data-ttu-id="7ee14-143">この時点でシークレットの値をメモしておく必要があります。</span><span class="sxs-lookup"><span data-stu-id="7ee14-143">Be sure to take note of the secret's value at this time.</span></span> <span data-ttu-id="7ee14-144">このページから移動すると、シークレットは再度表示されません。</span><span class="sxs-lookup"><span data-stu-id="7ee14-144">The secret is never displayed again after you leave this page.</span></span>

### <a name="install-the-dynamics-365-hr-virtual-entity-app"></a><span data-ttu-id="7ee14-145">Dynamics 365 HR Virtual Entity のインストール</span><span class="sxs-lookup"><span data-stu-id="7ee14-145">Install the Dynamics 365 HR Virtual Entity app</span></span>

<span data-ttu-id="7ee14-146">Power Apps 環境に Dynamics 365 HR Virtual Entity アプリをインストールして、仮想エンティティ ソリューション パッケージを Common Data Service にデプロイします。</span><span class="sxs-lookup"><span data-stu-id="7ee14-146">Install the Dynamics 365 HR Virtual Entity app in your Power Apps environment to deploy the virtual entity solution package to Common Data Service.</span></span>

1. <span data-ttu-id="7ee14-147">[Power Platform 管理センター](https://admin.powerplatform.microsoft.com)を開きます。</span><span class="sxs-lookup"><span data-stu-id="7ee14-147">Open the [Power Platform admin center](https://admin.powerplatform.microsoft.com).</span></span>

2. <span data-ttu-id="7ee14-148">**環境**の一覧で、Human Resources のインスタンスに関連付けられている Power Apps 環境を選択します。</span><span class="sxs-lookup"><span data-stu-id="7ee14-148">In the **Environments** list, select the Power Apps environment associated with your Human Resources instance.</span></span>

3. <span data-ttu-id="7ee14-149">ページの**リソース** セクションで、**Dynamics 365 アプリ**を選択します。</span><span class="sxs-lookup"><span data-stu-id="7ee14-149">In the **Resources** section of the page, select **Dynamics 365 apps**.</span></span>

4. <span data-ttu-id="7ee14-150">**アプリのインストール** アクションを選択します。</span><span class="sxs-lookup"><span data-stu-id="7ee14-150">Select the **Install app** action.</span></span>

5. <span data-ttu-id="7ee14-151">**Dynamics 365 HR Virtual Entity** を選択し、**次へ**を選択します。</span><span class="sxs-lookup"><span data-stu-id="7ee14-151">Select **Dynamics 365 HR Virtual Entity**, and select **Next**.</span></span>

6. <span data-ttu-id="7ee14-152">サービス使用条件に同意することを確認してマークします。</span><span class="sxs-lookup"><span data-stu-id="7ee14-152">Review and mark to agree to the terms of service.</span></span>

7. <span data-ttu-id="7ee14-153">**インストール**を選択します。</span><span class="sxs-lookup"><span data-stu-id="7ee14-153">Select **Install**.</span></span>

<span data-ttu-id="7ee14-154">インストールには数分かかります。</span><span class="sxs-lookup"><span data-stu-id="7ee14-154">The install takes a few minutes.</span></span> <span data-ttu-id="7ee14-155">完了したら、次の手順に進みます。</span><span class="sxs-lookup"><span data-stu-id="7ee14-155">When it completes, continue to the next steps.</span></span>

![Power Platform 管理センターから Dynamics 365 HR Virtual Entity アプリをインストールします](./media/hr-admin-integration-virtual-entities-power-platform-install.jpg)

### <a name="configure-the-virtual-entity-data-source"></a><span data-ttu-id="7ee14-157">仮想エンティティ データ ソースの構成</span><span class="sxs-lookup"><span data-stu-id="7ee14-157">Configure the virtual entity data source</span></span> 

<span data-ttu-id="7ee14-158">次の手順では、Power Apps 環境で仮想エンティティ データ ソースを構成します。</span><span class="sxs-lookup"><span data-stu-id="7ee14-158">The next step is to configure the virtual entity data source in the Power Apps environment.</span></span> 

1. <span data-ttu-id="7ee14-159">[Power Platform 管理センター](https://admin.powerplatform.microsoft.com)を開きます。</span><span class="sxs-lookup"><span data-stu-id="7ee14-159">Open the [Power Platform admin center](https://admin.powerplatform.microsoft.com).</span></span>

2. <span data-ttu-id="7ee14-160">**環境**の一覧で、Human Resources のインスタンスに関連付けられている Power Apps 環境を選択します。</span><span class="sxs-lookup"><span data-stu-id="7ee14-160">In the **Environments** list, select the Power Apps environment associated with your Human Resources instance.</span></span>

3. <span data-ttu-id="7ee14-161">ページの**詳細**セクションで、**環境 URL** を選択します。</span><span class="sxs-lookup"><span data-stu-id="7ee14-161">Select the **Environment URL** in the **Details** section of the page.</span></span>

4. <span data-ttu-id="7ee14-162">**ソリューションの正常性ハブ**で、アプリケーション ページの右上にある**高度な検索**アイコンを選択します。</span><span class="sxs-lookup"><span data-stu-id="7ee14-162">In the **Solution Health Hub**, select the **Advanced Find** icon in the top right of the application page.</span></span>

5. <span data-ttu-id="7ee14-163">**高度な検索**ページの**検索対象**ドロップダウン リストで、**Finance and Operations 仮想データ ソースの構成**を選択します。</span><span class="sxs-lookup"><span data-stu-id="7ee14-163">On the **Advanced Find** page, in the **Look for** dropdown list, select **Finance and Operations Virtual Data Source Configurations**.</span></span>

6. <span data-ttu-id="7ee14-164">**結果**を選択します。</span><span class="sxs-lookup"><span data-stu-id="7ee14-164">Select **Results**.</span></span>

7. <span data-ttu-id="7ee14-165">**Microsoft HR データ ソース**のレコードを選択します。</span><span class="sxs-lookup"><span data-stu-id="7ee14-165">Select the **Microsoft HR Data Source** record.</span></span>

8. <span data-ttu-id="7ee14-166">データ ソースの構成に必要な情報を入力します。</span><span class="sxs-lookup"><span data-stu-id="7ee14-166">Enter the required information for the data source configuration.</span></span>

   - <span data-ttu-id="7ee14-167">**ターゲット URL**: Human Resources の名前空間の URL。</span><span class="sxs-lookup"><span data-stu-id="7ee14-167">**Target URL**: The URL of your Human Resources namespace.</span></span>
   - <span data-ttu-id="7ee14-168">**テナント ID**: Azure Active Directory (Azure AD) テナント ID。</span><span class="sxs-lookup"><span data-stu-id="7ee14-168">**Tenant ID**: The Azure Active Directory (Azure AD) tenant ID.</span></span>
   - <span data-ttu-id="7ee14-169">**AAD アプリケーション ID**: Microsoft Azure ポータルに登録されているアプリケーションに対して作成されたアプリケーション (クライアント) ID。</span><span class="sxs-lookup"><span data-stu-id="7ee14-169">**AAD Application ID**: The application (client) ID created for the application registered in the Microsoft Azure portal.</span></span> <span data-ttu-id="7ee14-170">この情報は、[アプリを Microsoft Azure に登録する](hr-admin-integration-common-data-service-virtual-entities.md#register-the-app-in-microsoft-azure)のステップで先に取得しました。</span><span class="sxs-lookup"><span data-stu-id="7ee14-170">You received this information earlier during the step [Register the app in Microsoft Azure](hr-admin-integration-common-data-service-virtual-entities.md#register-the-app-in-microsoft-azure).</span></span>
   - <span data-ttu-id="7ee14-171">**AAD アプリケーション シークレット**: Microsoft Azure ポータルに登録されているアプリケーションに対して作成されたクライアント シークレット。</span><span class="sxs-lookup"><span data-stu-id="7ee14-171">**AAD Application Secret**: The client secret created for the application registered in the Microsoft Azure portal.</span></span> <span data-ttu-id="7ee14-172">この情報は、[アプリを Microsoft Azure に登録する](hr-admin-integration-common-data-service-virtual-entities.md#register-the-app-in-microsoft-azure)のステップで先に取得しました。</span><span class="sxs-lookup"><span data-stu-id="7ee14-172">You received this information earlier during the step [Register the app in Microsoft Azure](hr-admin-integration-common-data-service-virtual-entities.md#register-the-app-in-microsoft-azure).</span></span>

9. <span data-ttu-id="7ee14-173">**保存して閉じる**を選択します。</span><span class="sxs-lookup"><span data-stu-id="7ee14-173">Select **Save & Close**.</span></span>

   ![Microsoft HR データ ソース](./media/hr-admin-integration-virtual-entities-hr-data-source.jpg)

### <a name="grant-app-permissions-in-human-resources"></a><span data-ttu-id="7ee14-175">Human Resources でアプリのアクセス許可を付与する</span><span class="sxs-lookup"><span data-stu-id="7ee14-175">Grant app permissions in Human Resources</span></span>

<span data-ttu-id="7ee14-176">Human Resources でアクセス許可を付与するのは、次の 2 つの Azure AD アプリケーションです。</span><span class="sxs-lookup"><span data-stu-id="7ee14-176">Grant permissions for the two Azure AD applications in Human Resources:</span></span>

- <span data-ttu-id="7ee14-177">Microsoft Azure ポータルでテナント用に作成されたアプリ</span><span class="sxs-lookup"><span data-stu-id="7ee14-177">The app created for your tenant in the Microsoft Azure portal</span></span>
- <span data-ttu-id="7ee14-178">Power Apps 環境にインストールされた Dynamics 365 HR Virtual Entity アプリ</span><span class="sxs-lookup"><span data-stu-id="7ee14-178">The Dynamics 365 HR Virtual Entity app installed in the Power Apps environment</span></span> 

1. <span data-ttu-id="7ee14-179">Human Resources で、**Azure Active Directory アプリケーション** ページを開きます。</span><span class="sxs-lookup"><span data-stu-id="7ee14-179">In Human Resources, open the **Azure Active Directory applications** page.</span></span>

2. <span data-ttu-id="7ee14-180">**新規**を選択して、新しい申請レコードを作成します。</span><span class="sxs-lookup"><span data-stu-id="7ee14-180">Select **New** to create a new application record:</span></span>

    - <span data-ttu-id="7ee14-181">**クライアント ID** フィールドに、Microsoft Azure ポータルに登録したアプリのクライアント ID を入力します。</span><span class="sxs-lookup"><span data-stu-id="7ee14-181">In the **Client ID** field, enter the client ID of the app you registered in the Microsoft Azure portal.</span></span>
    - <span data-ttu-id="7ee14-182">**名前**フィールドに、Microsoft Azure ポータルに登録したアプリの名前を入力します。</span><span class="sxs-lookup"><span data-stu-id="7ee14-182">In the **Name** field, enter the name of the app you registered in the Microsoft Azure portal.</span></span>
    - <span data-ttu-id="7ee14-183">**ユーザー ID** フィールドで、管理者アクセス許可を持つユーザーのユーザー ID をHuman Resources と Power Apps 環境から選択します。</span><span class="sxs-lookup"><span data-stu-id="7ee14-183">In the **User ID** field, select the user ID of a user with admin permissions in Human Resources and the Power Apps environment.</span></span>

3. <span data-ttu-id="7ee14-184">**新規**を選択して、2 つ目の申請レコードを作成します。</span><span class="sxs-lookup"><span data-stu-id="7ee14-184">Select **New** to create a second application record:</span></span>

    - <span data-ttu-id="7ee14-185">**クライアント ID**: f9be0c49-aa22-4ec6-911a-c5da515226ff</span><span class="sxs-lookup"><span data-stu-id="7ee14-185">**Client Id**: f9be0c49-aa22-4ec6-911a-c5da515226ff</span></span>
    - <span data-ttu-id="7ee14-186">**名前**: Dynamics 365 HR Virtual Entity</span><span class="sxs-lookup"><span data-stu-id="7ee14-186">**Name**: Dynamics 365 HR Virtual Entity</span></span>
    - <span data-ttu-id="7ee14-187">**ユーザー ID** フィールドで、管理者アクセス許可を持つユーザーのユーザー ID をHuman Resources と Power Apps 環境から選択します。</span><span class="sxs-lookup"><span data-stu-id="7ee14-187">In the **User ID** field, select the user ID of a user with admin permissions in Human Resources and the Power Apps environment.</span></span>

## <a name="generate-virtual-entities"></a><span data-ttu-id="7ee14-188">仮想エンティティの生成</span><span class="sxs-lookup"><span data-stu-id="7ee14-188">Generate virtual entities</span></span>

<span data-ttu-id="7ee14-189">セットアップが完了したら、Common Data Service インスタンスで生成して有効にする仮想エンティティを選択できます。</span><span class="sxs-lookup"><span data-stu-id="7ee14-189">When setup completes, you can select the virtual entities you want to generate and enable in your Common Data Service instance.</span></span>

1. <span data-ttu-id="7ee14-190">[Power Platform 管理センター](https://admin.powerplatform.microsoft.com)を開きます。</span><span class="sxs-lookup"><span data-stu-id="7ee14-190">Open the [Power Platform admin center](https://admin.powerplatform.microsoft.com).</span></span>

2. <span data-ttu-id="7ee14-191">**環境**の一覧で、Human Resources のインスタンスに関連付けられている Power Apps 環境を選択します。</span><span class="sxs-lookup"><span data-stu-id="7ee14-191">In the **Environments** list, select the Power Apps environment associated with your Human Resources instance.</span></span>

3. <span data-ttu-id="7ee14-192">ページの**詳細**セクションで、**環境 URL** を選択します。</span><span class="sxs-lookup"><span data-stu-id="7ee14-192">Select the **Environment URL** in the **Details** section of the page.</span></span>

4. <span data-ttu-id="7ee14-193">**ソリューションの正常性ハブ**で、ページの右上にある**高度な検索**アイコンを選択します。</span><span class="sxs-lookup"><span data-stu-id="7ee14-193">In the **Solution Health Hub**, select the **Advanced Find** icon in the top right of the page.</span></span>

5. <span data-ttu-id="7ee14-194">**高度な検索**ページの**検索対象**ドロップダウン リストで、**利用可能な HR エンティティ**を選択します。</span><span class="sxs-lookup"><span data-stu-id="7ee14-194">On the **Advanced Find** page, in the **Look for** dropdown list, select **Available HR Entities**.</span></span>

6. <span data-ttu-id="7ee14-195">フィルター オプションを使用して、有効にするエンティティを検索します。</span><span class="sxs-lookup"><span data-stu-id="7ee14-195">Use the filter options to find the entity or entities you want to enable.</span></span>

7. <span data-ttu-id="7ee14-196">リストからエンティティを選択します。</span><span class="sxs-lookup"><span data-stu-id="7ee14-196">Select an entity from the list.</span></span>

8. <span data-ttu-id="7ee14-197">エンティティ ページで、エンティティの**生成済み**のプロパティを**はい**に変更します。</span><span class="sxs-lookup"><span data-stu-id="7ee14-197">On the entity page, change the **Has Been Generated** property to **Yes** for the entity.</span></span>

9. <span data-ttu-id="7ee14-198">エンティティ ページを保存して閉じます。</span><span class="sxs-lookup"><span data-stu-id="7ee14-198">Save and close the entity page.</span></span>

> [!NOTE]
> <span data-ttu-id="7ee14-199">**複数のレコードの変更**ページを使用すると、複数の仮想エンティティを一度に生成できます。</span><span class="sxs-lookup"><span data-stu-id="7ee14-199">You can generate multiple virtual entities at once by using the **Change Multiple Records** page.</span></span> <span data-ttu-id="7ee14-200">ページで複数のレコードを選択し、リボンで**編集**を選択します。</span><span class="sxs-lookup"><span data-stu-id="7ee14-200">Select multiple records on the page, and select **Edit** on the ribbon.</span></span> <span data-ttu-id="7ee14-201">これにより、選択したすべてのレコードについて、**生成済み**のプロパティを変更できます。</span><span class="sxs-lookup"><span data-stu-id="7ee14-201">You can then change the **Has Been Generated** property for all selected records.</span></span>

![利用可能な HR エンティティ](./media/hr-admin-integration-virtual-entities-available.jpg)

> [!NOTE]
> <span data-ttu-id="7ee14-203">今後のリリースで仮想エンティティを生成するプロセスを効率化するために、Human Resources のページでプロセスが発生します。</span><span class="sxs-lookup"><span data-stu-id="7ee14-203">To streamline the process of generating virtual entities in future releases, the process will occur in a page in Human Resources.</span></span>

## <a name="see-also"></a><span data-ttu-id="7ee14-204">参照</span><span class="sxs-lookup"><span data-stu-id="7ee14-204">See also</span></span>

[<span data-ttu-id="7ee14-205">Common Data Service とは</span><span class="sxs-lookup"><span data-stu-id="7ee14-205">What is Common Data Service?</span></span>](https://docs.microsoft.com/powerapps/maker/common-data-service/data-platform-intro)<br>
[<span data-ttu-id="7ee14-206">エンティティ概要</span><span class="sxs-lookup"><span data-stu-id="7ee14-206">Entity overview</span></span>](https://docs.microsoft.com/powerapps/maker/common-data-service/entity-overview)<br>
[<span data-ttu-id="7ee14-207">エンティティの関連付けの概要</span><span class="sxs-lookup"><span data-stu-id="7ee14-207">Entity relationships overview</span></span>](https://docs.microsoft.com/powerapps/maker/common-data-service/relationships-overview)<br>
[<span data-ttu-id="7ee14-208">外部データ ソースのデータを含む仮想エンティティの作成と編集</span><span class="sxs-lookup"><span data-stu-id="7ee14-208">Create and edit virtual entities that contain data from an external data source</span></span>](https://docs.microsoft.com/powerapps/maker/common-data-service/create-edit-virtual-entities)<br>
[<span data-ttu-id="7ee14-209">Power Apps ポータルについて</span><span class="sxs-lookup"><span data-stu-id="7ee14-209">What is Power Apps portals?</span></span>](https://docs.microsoft.com/powerapps/maker/portals/overview)<br>
[<span data-ttu-id="7ee14-210">Power Apps でのアプリの作成の概要</span><span class="sxs-lookup"><span data-stu-id="7ee14-210">Overview of creating apps in Power Apps</span></span>](https://docs.microsoft.com/powerapps/maker/)
