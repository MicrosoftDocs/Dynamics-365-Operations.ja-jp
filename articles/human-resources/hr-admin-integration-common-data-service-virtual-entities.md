---
title: Common Data Service 仮想エンティティの構成
description: このトピックでは、Dynamics 365 Human Resources の仮想エンティティを構成する方法について説明します。 既存の仮想エンティティを生成および更新し、生成されたエンティティと使用可能なエンティティを分析します。
author: andreabichsel
manager: tfehr
ms.date: 11/02/2020
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
ms.openlocfilehash: 2b590faeab600d04c9d5303693ec1e9ac682250d
ms.sourcegitcommit: deb711c92251ed48cdf20ea514d03461c26a2262
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/25/2020
ms.locfileid: "4645604"
---
# <a name="configure-common-data-service-virtual-entities"></a><span data-ttu-id="a7d2e-104">Common Data Service 仮想エンティティの構成</span><span class="sxs-lookup"><span data-stu-id="a7d2e-104">Configure Common Data Service virtual entities</span></span>

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="a7d2e-105">Dynamics 365 Human Resources は Common Data Service の仮想データ ソースです。</span><span class="sxs-lookup"><span data-stu-id="a7d2e-105">Dynamics 365 Human Resources is a virtual data source in Common Data Service.</span></span> <span data-ttu-id="a7d2e-106">このサービスでは、Common Data Service および Microsoft Power Platform からの作成、読み取り、更新、および削除 (CRUD) の完全な操作が提供されます。</span><span class="sxs-lookup"><span data-stu-id="a7d2e-106">It provides full create, read, update, and delete (CRUD) operations from Common Data Service and Microsoft Power Platform.</span></span> <span data-ttu-id="a7d2e-107">仮想エンティティのデータは Common Data Service には保存されませんが、アプリケーション データベースに保存されます。</span><span class="sxs-lookup"><span data-stu-id="a7d2e-107">The data for virtual entities isn't stored in Common Data Service, but in the application database.</span></span> 

<span data-ttu-id="a7d2e-108">Common Data Service から Human Resources エンティティに対して CRUD 操作を有効にするには、エンティティを Common Data Service の仮想エンティティとして使用できるようにする必要があります。</span><span class="sxs-lookup"><span data-stu-id="a7d2e-108">To enable CRUD operations on Human Resources entities from Common Data Service, you must make the entities available as virtual entities in Common Data Service.</span></span> <span data-ttu-id="a7d2e-109">これにより、Human Resources のデータで Common Data Service と Microsoft Power Platform から CRUD 操作を実行できます。</span><span class="sxs-lookup"><span data-stu-id="a7d2e-109">This lets you perform CRUD operations from Common Data Service and Microsoft Power Platform on data that's in Human Resources.</span></span> <span data-ttu-id="a7d2e-110">また、この操作では、Human Resources のビジネス ロジックの完全な検証をサポートしているため、エンティティにデータを書き込むときにデータの整合性を確保できます。</span><span class="sxs-lookup"><span data-stu-id="a7d2e-110">The operations also support the full business logic validations of Human Resources to ensure data integrity when writing data to the entities.</span></span>

## <a name="available-virtual-entities-for-human-resources"></a><span data-ttu-id="a7d2e-111">Human Resources で使用可能な仮想エンティティ</span><span class="sxs-lookup"><span data-stu-id="a7d2e-111">Available virtual entities for Human Resources</span></span>

<span data-ttu-id="a7d2e-112">Human Resources のすべての Open Data Protocol (OData) エンティティは、Common Data Service の仮想エンティティとして使用できます。</span><span class="sxs-lookup"><span data-stu-id="a7d2e-112">All Open Data Protocol (OData) entities in Human Resources are available as virtual entities in Common Data Service.</span></span> <span data-ttu-id="a7d2e-113">また、Power Platform で使用することもできます。</span><span class="sxs-lookup"><span data-stu-id="a7d2e-113">They're also available in Power Platform.</span></span> <span data-ttu-id="a7d2e-114">データを Common Data Service にコピーまたは同期することなく、完全な CRUD 機能を備えた Human Resources からデータを使ってアプリとエクスペリエンスを直接ビルドできるようになりました。</span><span class="sxs-lookup"><span data-stu-id="a7d2e-114">You can now build apps and experiences with data directly from Human Resources with full CRUD capability, without copying or synchronizing data to Common Data Service.</span></span> <span data-ttu-id="a7d2e-115">Power Apps ポータルは、Human Resources の業務プロセスのコラボレーション シナリオを可能にする外部向けの Web サイトをビルドするために使用できます。</span><span class="sxs-lookup"><span data-stu-id="a7d2e-115">You can use Power Apps portals to build external-facing websites that enable collaboration scenarios for business processes in Human Resources.</span></span>

<span data-ttu-id="a7d2e-116">環境で有効になっている仮想エンティティの一覧を表示し、**Dynamics 365 HR 仮想エンティティ** ソリューションで [Power Apps](https://make.powerapps.com) のエンティティの操作を開始できます。</span><span class="sxs-lookup"><span data-stu-id="a7d2e-116">You can view the list of virtual entities enabled in the environment, and begin working with the entities in [Power Apps](https://make.powerapps.com), in the **Dynamics 365 HR Virtual Entities** solution.</span></span>

![Power Apps の Dynamics 365 HR 仮想エンティティ](./media/hr-admin-integration-virtual-entities-power-apps.jpg)

## <a name="virtual-entities-versus-natural-entities"></a><span data-ttu-id="a7d2e-118">仮想エンティティとナチュラル エンティティの比較</span><span class="sxs-lookup"><span data-stu-id="a7d2e-118">Virtual entities versus natural entities</span></span>

<span data-ttu-id="a7d2e-119">Human Resources の仮想エンティティは、Human Resources 向けに作成された Common Data Service のナチュラル エンティティとは異なります。</span><span class="sxs-lookup"><span data-stu-id="a7d2e-119">Virtual entities for Human Resources aren't the same as the natural Common Data Service entities created for Human Resources.</span></span> <span data-ttu-id="a7d2e-120">Human Resources のナチュラル エンティティは、Common Data Service の HCM Common ソリューションで個別に生成および管理されます。</span><span class="sxs-lookup"><span data-stu-id="a7d2e-120">The natural entities for Human Resources are generated separately and maintained in the HCM Common solution in Common Data Service.</span></span> <span data-ttu-id="a7d2e-121">ナチュラル エンティティでは、データが Common Data Service に保存され、Human Resources アプリケーション データベースとの同期が必要になります。</span><span class="sxs-lookup"><span data-stu-id="a7d2e-121">With natural entities, the data is stored in Common Data Service and requires synchronization with the Human Resources application database.</span></span>

> [!NOTE]
> <span data-ttu-id="a7d2e-122">Human Resources の Common Data Service ナチュラル エンティティの一覧については、「[Common Data Service エンティティ](https://docs.microsoft.com/dynamics365/human-resources/hr-developer-entities)」を参照してください 。</span><span class="sxs-lookup"><span data-stu-id="a7d2e-122">For a list of the natural Common Data Service entities for Human Resources, see [Common Data Service entities](https://docs.microsoft.com/dynamics365/human-resources/hr-developer-entities).</span></span>

## <a name="setup"></a><span data-ttu-id="a7d2e-123">段取り</span><span class="sxs-lookup"><span data-stu-id="a7d2e-123">Setup</span></span>

<span data-ttu-id="a7d2e-124">環境で仮想エンティティを有効にするには、次の設定手順に従います。</span><span class="sxs-lookup"><span data-stu-id="a7d2e-124">Follow these setup steps to enable virtual entities in your environment.</span></span>

### <a name="enable-virtual-entities-in-human-resources"></a><span data-ttu-id="a7d2e-125">Human Resources の仮想エンティティを有効にする</span><span class="sxs-lookup"><span data-stu-id="a7d2e-125">Enable virtual entities in Human Resources</span></span>

<span data-ttu-id="a7d2e-126">まず、**機能管理** ワークスペースで仮想エンティティを有効にする必要があります。</span><span class="sxs-lookup"><span data-stu-id="a7d2e-126">First, you must enable virtual entities in the **Feature management** workspace.</span></span>

1. <span data-ttu-id="a7d2e-127">人事管理では、**システム管理** を選択します。</span><span class="sxs-lookup"><span data-stu-id="a7d2e-127">In Human Resources, select **System administration**.</span></span>

2. <span data-ttu-id="a7d2e-128">**機能管理** タイルを選択します。</span><span class="sxs-lookup"><span data-stu-id="a7d2e-128">Select the **Feature management** tile.</span></span>

3. <span data-ttu-id="a7d2e-129">**HR/CDS の仮想エンティティのサポート** を選択し、**有効** を選択します。</span><span class="sxs-lookup"><span data-stu-id="a7d2e-129">Select **Virtual Entity support in HR/CDS**, and then select **Enable**.</span></span>

<span data-ttu-id="a7d2e-130">有効化および無効化機能に関する情報は、[機能の管理](hr-admin-manage-features.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="a7d2e-130">For more information about enabling and disabling features, see [Manage features](hr-admin-manage-features.md).</span></span>

### <a name="register-the-app-in-microsoft-azure"></a><span data-ttu-id="a7d2e-131">アプリを Microsoft Azure に登録する</span><span class="sxs-lookup"><span data-stu-id="a7d2e-131">Register the app in Microsoft Azure</span></span>

<span data-ttu-id="a7d2e-132">Microsoft ID プラットフォームがアプリとユーザーに対して認証および承認サービスを提供できるように、Azure portal で Human Resources インスタンスを登録する必要があります。</span><span class="sxs-lookup"><span data-stu-id="a7d2e-132">You must register your Human Resources instance in the Azure portal so the Microsoft identity platform can provide authentication and authorization services for the app and users.</span></span> <span data-ttu-id="a7d2e-133">Azure でのアプリの登録に関する詳細については、「[クイックスタート: Microsoft ID プラットフォームでアプリケーションを登録する](https://docs.microsoft.com/azure/active-directory/develop/quickstart-register-app)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="a7d2e-133">For more information about registering apps in Azure, see [Quickstart: Register an application with the Microsoft identity platform](https://docs.microsoft.com/azure/active-directory/develop/quickstart-register-app).</span></span>

1. <span data-ttu-id="a7d2e-134">[Microsoft Azure ポータル](https://portal.azure.com)を開きます。</span><span class="sxs-lookup"><span data-stu-id="a7d2e-134">Open the [Microsoft Azure portal](https://portal.azure.com).</span></span>

2. <span data-ttu-id="a7d2e-135">Azure サービスの一覧で、**アプリの登録** を選択します。</span><span class="sxs-lookup"><span data-stu-id="a7d2e-135">In the Azure services list, select **App registrations**.</span></span>

3. <span data-ttu-id="a7d2e-136">**新規登録** を選択します。</span><span class="sxs-lookup"><span data-stu-id="a7d2e-136">Select **New registration**.</span></span>

4. <span data-ttu-id="a7d2e-137">**名前** フィールドに、アプリの内容を示す名前を入力します。</span><span class="sxs-lookup"><span data-stu-id="a7d2e-137">In the **Name** field, enter a descriptive name for the app.</span></span> <span data-ttu-id="a7d2e-138">たとえば、**Dynamics 365 Human Resources 仮想エンティティ**。</span><span class="sxs-lookup"><span data-stu-id="a7d2e-138">For example, **Dynamics 365 Human Resources Virtual Entities**.</span></span>

5. <span data-ttu-id="a7d2e-139">**リダイレクト URI** フィールドに、Human Resources のインスタンスの名前空間 URL を入力します。</span><span class="sxs-lookup"><span data-stu-id="a7d2e-139">In the **Redirect URI** field, enter the namespace URL of your instance of Human Resources.</span></span>

6. <span data-ttu-id="a7d2e-140">**登録** を選択します。</span><span class="sxs-lookup"><span data-stu-id="a7d2e-140">Select **Register**.</span></span>

7. <span data-ttu-id="a7d2e-141">登録が完了すると、Azure portal には、**アプリケーション (クライアント) ID** を含むアプリ登録の **概要** ウィンドウが表示されます。</span><span class="sxs-lookup"><span data-stu-id="a7d2e-141">When registration completes, the Azure portal displays the app registration's **Overview** pane, which includes its **Application (client) ID**.</span></span> <span data-ttu-id="a7d2e-142">この時点で **アプリケーション (クライアント) ID** をメモします。</span><span class="sxs-lookup"><span data-stu-id="a7d2e-142">Take note of the **Application (client) ID** at this time.</span></span> <span data-ttu-id="a7d2e-143">この情報は、[仮想エンティティ データ ソースを構成する](hr-admin-integration-common-data-service-virtual-entities.md#configure-the-virtual-entity-data-source)ときに入力します。</span><span class="sxs-lookup"><span data-stu-id="a7d2e-143">You'll enter this information when you [Configure the virtual entity data source](hr-admin-integration-common-data-service-virtual-entities.md#configure-the-virtual-entity-data-source).</span></span>

8. <span data-ttu-id="a7d2e-144">左側のナビゲーション ウィンドウで、**証明書とシークレット** を選択します。</span><span class="sxs-lookup"><span data-stu-id="a7d2e-144">In the left navigation pane, select **Certificates and secrets**.</span></span>

9. <span data-ttu-id="a7d2e-145">ページの **クライアント シークレット** セクションで、**新しいクライアント シークレット** を選択します。</span><span class="sxs-lookup"><span data-stu-id="a7d2e-145">In the **Client secrets** section of the page, select **New client secret**.</span></span>

10. <span data-ttu-id="a7d2e-146">説明を入力し、期間を選択して、**追加** を選択します。</span><span class="sxs-lookup"><span data-stu-id="a7d2e-146">Provide a description, select a duration, and select **Add**.</span></span>

11. <span data-ttu-id="a7d2e-147">シークレットの値を記録します。</span><span class="sxs-lookup"><span data-stu-id="a7d2e-147">Record the secret's value.</span></span> <span data-ttu-id="a7d2e-148">この情報は、[仮想エンティティ データ ソースを構成する](hr-admin-integration-common-data-service-virtual-entities.md#configure-the-virtual-entity-data-source)ときに入力します。</span><span class="sxs-lookup"><span data-stu-id="a7d2e-148">You'll enter this information when you [Configure the virtual entity data source](hr-admin-integration-common-data-service-virtual-entities.md#configure-the-virtual-entity-data-source).</span></span>

    > [!IMPORTANT]
    > <span data-ttu-id="a7d2e-149">この時点でシークレットの値をメモしておく必要があります。</span><span class="sxs-lookup"><span data-stu-id="a7d2e-149">Be sure to take note of the secret's value at this time.</span></span> <span data-ttu-id="a7d2e-150">このページから移動すると、シークレットは再度表示されません。</span><span class="sxs-lookup"><span data-stu-id="a7d2e-150">The secret is never displayed again after you leave this page.</span></span>

### <a name="install-the-dynamics-365-hr-virtual-entity-app"></a><span data-ttu-id="a7d2e-151">Dynamics 365 HR Virtual Entity のインストール</span><span class="sxs-lookup"><span data-stu-id="a7d2e-151">Install the Dynamics 365 HR Virtual Entity app</span></span>

<span data-ttu-id="a7d2e-152">Power Apps 環境に Dynamics 365 HR Virtual Entity アプリをインストールして、仮想エンティティ ソリューション パッケージを Common Data Service にデプロイします。</span><span class="sxs-lookup"><span data-stu-id="a7d2e-152">Install the Dynamics 365 HR Virtual Entity app in your Power Apps environment to deploy the virtual entity solution package to Common Data Service.</span></span>

1. <span data-ttu-id="a7d2e-153">[Power Platform 管理センター](https://admin.powerplatform.microsoft.com)を開きます。</span><span class="sxs-lookup"><span data-stu-id="a7d2e-153">Open the [Power Platform admin center](https://admin.powerplatform.microsoft.com).</span></span>

2. <span data-ttu-id="a7d2e-154">**環境** の一覧で、Human Resources のインスタンスに関連付けられている Power Apps 環境を選択します。</span><span class="sxs-lookup"><span data-stu-id="a7d2e-154">In the **Environments** list, select the Power Apps environment associated with your Human Resources instance.</span></span>

3. <span data-ttu-id="a7d2e-155">ページの **リソース** セクションで、**Dynamics 365 アプリ** を選択します。</span><span class="sxs-lookup"><span data-stu-id="a7d2e-155">In the **Resources** section of the page, select **Dynamics 365 apps**.</span></span>

4. <span data-ttu-id="a7d2e-156">**アプリのインストール** アクションを選択します。</span><span class="sxs-lookup"><span data-stu-id="a7d2e-156">Select the **Install app** action.</span></span>

5. <span data-ttu-id="a7d2e-157">**Dynamics 365 HR Virtual Entity** を選択し、**次へ** を選択します。</span><span class="sxs-lookup"><span data-stu-id="a7d2e-157">Select **Dynamics 365 HR Virtual Entity**, and select **Next**.</span></span>

6. <span data-ttu-id="a7d2e-158">サービス使用条件に同意することを確認してマークします。</span><span class="sxs-lookup"><span data-stu-id="a7d2e-158">Review and mark to agree to the terms of service.</span></span>

7. <span data-ttu-id="a7d2e-159">**インストール** を選択します。</span><span class="sxs-lookup"><span data-stu-id="a7d2e-159">Select **Install**.</span></span>

<span data-ttu-id="a7d2e-160">インストールには数分かかります。</span><span class="sxs-lookup"><span data-stu-id="a7d2e-160">The install takes a few minutes.</span></span> <span data-ttu-id="a7d2e-161">完了したら、次の手順に進みます。</span><span class="sxs-lookup"><span data-stu-id="a7d2e-161">When it completes, continue to the next steps.</span></span>

![Power Platform 管理センターから Dynamics 365 HR Virtual Entity アプリをインストールします](./media/hr-admin-integration-virtual-entities-power-platform-install.jpg)

### <a name="configure-the-virtual-entity-data-source"></a><span data-ttu-id="a7d2e-163">仮想エンティティ データ ソースの構成</span><span class="sxs-lookup"><span data-stu-id="a7d2e-163">Configure the virtual entity data source</span></span> 

<span data-ttu-id="a7d2e-164">次の手順では、Power Apps 環境で仮想エンティティ データ ソースを構成します。</span><span class="sxs-lookup"><span data-stu-id="a7d2e-164">The next step is to configure the virtual entity data source in the Power Apps environment.</span></span> 

1. <span data-ttu-id="a7d2e-165">[Power Platform 管理センター](https://admin.powerplatform.microsoft.com)を開きます。</span><span class="sxs-lookup"><span data-stu-id="a7d2e-165">Open the [Power Platform admin center](https://admin.powerplatform.microsoft.com).</span></span>

2. <span data-ttu-id="a7d2e-166">**環境** の一覧で、Human Resources のインスタンスに関連付けられている Power Apps 環境を選択します。</span><span class="sxs-lookup"><span data-stu-id="a7d2e-166">In the **Environments** list, select the Power Apps environment associated with your Human Resources instance.</span></span>

3. <span data-ttu-id="a7d2e-167">ページの **詳細** セクションで、**環境 URL** を選択します。</span><span class="sxs-lookup"><span data-stu-id="a7d2e-167">Select the **Environment URL** in the **Details** section of the page.</span></span>

4. <span data-ttu-id="a7d2e-168">**ソリューションの正常性ハブ** で、アプリケーション ページの右上にある **高度な検索** アイコンを選択します。</span><span class="sxs-lookup"><span data-stu-id="a7d2e-168">In the **Solution Health Hub**, select the **Advanced Find** icon in the top right of the application page.</span></span>

5. <span data-ttu-id="a7d2e-169">**高度な検索** ページの **検索対象** ドロップダウン リストで、**Finance and Operations 仮想データ ソースの構成** を選択します。</span><span class="sxs-lookup"><span data-stu-id="a7d2e-169">On the **Advanced Find** page, in the **Look for** dropdown list, select **Finance and Operations Virtual Data Source Configurations**.</span></span>

6. <span data-ttu-id="a7d2e-170">**結果** を選択します。</span><span class="sxs-lookup"><span data-stu-id="a7d2e-170">Select **Results**.</span></span>

7. <span data-ttu-id="a7d2e-171">**Microsoft HR データ ソース** のレコードを選択します。</span><span class="sxs-lookup"><span data-stu-id="a7d2e-171">Select the **Microsoft HR Data Source** record.</span></span>

8. <span data-ttu-id="a7d2e-172">データ ソースの構成に必要な情報を入力します。</span><span class="sxs-lookup"><span data-stu-id="a7d2e-172">Enter the required information for the data source configuration:</span></span>

   - <span data-ttu-id="a7d2e-173">**ターゲット URL**: Human Resources の名前空間の URL。</span><span class="sxs-lookup"><span data-stu-id="a7d2e-173">**Target URL**: The URL of your Human Resources namespace.</span></span> <span data-ttu-id="a7d2e-174">ターゲット URL の形式は次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="a7d2e-174">The format of the target URL is:</span></span>
     
     <span data-ttu-id="a7d2e-175">https://\<hostname\>.hr.talent.dynamics.com/namespaces/\<namespaceID\>/</span><span class="sxs-lookup"><span data-stu-id="a7d2e-175">https://\<hostname\>.hr.talent.dynamics.com/namespaces/\<namespaceID\>/</span></span>

     <span data-ttu-id="a7d2e-176">例:</span><span class="sxs-lookup"><span data-stu-id="a7d2e-176">For example:</span></span>
     
     `https://aos.rts-sf-5ea54e35c68-westus2.hr.talent.dynamics.com/namespaces/49d24c565-8f4d-4891-b174-bf83d948ed0c/`

     >[!NOTE]
     ><span data-ttu-id="a7d2e-177">URL の末尾に "**/**" 文字を挿入し、エラーを回避します。</span><span class="sxs-lookup"><span data-stu-id="a7d2e-177">Be sure to include the "**/**" character at the end of the URL to avoid receiving an error.</span></span>

   - <span data-ttu-id="a7d2e-178">**テナント ID**: Azure Active Directory (Azure AD) テナント ID。</span><span class="sxs-lookup"><span data-stu-id="a7d2e-178">**Tenant ID**: The Azure Active Directory (Azure AD) tenant ID.</span></span>

   - <span data-ttu-id="a7d2e-179">**AAD アプリケーション ID**: Microsoft Azure ポータルに登録されているアプリケーションに対して作成されたアプリケーション (クライアント) ID。</span><span class="sxs-lookup"><span data-stu-id="a7d2e-179">**AAD Application ID**: The application (client) ID created for the application registered in the Microsoft Azure portal.</span></span> <span data-ttu-id="a7d2e-180">この情報は、[アプリを Microsoft Azure に登録する](hr-admin-integration-common-data-service-virtual-entities.md#register-the-app-in-microsoft-azure)のステップで先に取得しました。</span><span class="sxs-lookup"><span data-stu-id="a7d2e-180">You received this information earlier during the step [Register the app in Microsoft Azure](hr-admin-integration-common-data-service-virtual-entities.md#register-the-app-in-microsoft-azure).</span></span>

   - <span data-ttu-id="a7d2e-181">**AAD アプリケーション シークレット**: Microsoft Azure ポータルに登録されているアプリケーションに対して作成されたクライアント シークレット。</span><span class="sxs-lookup"><span data-stu-id="a7d2e-181">**AAD Application Secret**: The client secret created for the application registered in the Microsoft Azure portal.</span></span> <span data-ttu-id="a7d2e-182">この情報は、[アプリを Microsoft Azure に登録する](hr-admin-integration-common-data-service-virtual-entities.md#register-the-app-in-microsoft-azure)のステップで先に取得しました。</span><span class="sxs-lookup"><span data-stu-id="a7d2e-182">You received this information earlier during the step [Register the app in Microsoft Azure](hr-admin-integration-common-data-service-virtual-entities.md#register-the-app-in-microsoft-azure).</span></span>

   ![Microsoft HR データ ソース](./media/hr-admin-integration-virtual-entities-hr-data-source.jpg)

9. <span data-ttu-id="a7d2e-184">**保存して閉じる** を選択します。</span><span class="sxs-lookup"><span data-stu-id="a7d2e-184">Select **Save & Close**.</span></span>

### <a name="grant-app-permissions-in-human-resources"></a><span data-ttu-id="a7d2e-185">Human Resources でアプリのアクセス許可を付与する</span><span class="sxs-lookup"><span data-stu-id="a7d2e-185">Grant app permissions in Human Resources</span></span>

<span data-ttu-id="a7d2e-186">Human Resources でアクセス許可を付与するのは、次の 2 つの Azure AD アプリケーションです。</span><span class="sxs-lookup"><span data-stu-id="a7d2e-186">Grant permissions for the two Azure AD applications in Human Resources:</span></span>

- <span data-ttu-id="a7d2e-187">Microsoft Azure ポータルでテナント用に作成されたアプリ</span><span class="sxs-lookup"><span data-stu-id="a7d2e-187">The app created for your tenant in the Microsoft Azure portal</span></span>
- <span data-ttu-id="a7d2e-188">Power Apps 環境にインストールされた Dynamics 365 HR Virtual Entity アプリ</span><span class="sxs-lookup"><span data-stu-id="a7d2e-188">The Dynamics 365 HR Virtual Entity app installed in the Power Apps environment</span></span> 

1. <span data-ttu-id="a7d2e-189">Human Resources で、**Azure Active Directory アプリケーション** ページを開きます。</span><span class="sxs-lookup"><span data-stu-id="a7d2e-189">In Human Resources, open the **Azure Active Directory applications** page.</span></span>

2. <span data-ttu-id="a7d2e-190">**新規** を選択して、新しい申請レコードを作成します。</span><span class="sxs-lookup"><span data-stu-id="a7d2e-190">Select **New** to create a new application record:</span></span>

    - <span data-ttu-id="a7d2e-191">**クライアント ID** フィールドに、Microsoft Azure ポータルに登録したアプリのクライアント ID を入力します。</span><span class="sxs-lookup"><span data-stu-id="a7d2e-191">In the **Client ID** field, enter the client ID of the app you registered in the Microsoft Azure portal.</span></span>
    - <span data-ttu-id="a7d2e-192">**名前** フィールドに、Microsoft Azure ポータルに登録したアプリの名前を入力します。</span><span class="sxs-lookup"><span data-stu-id="a7d2e-192">In the **Name** field, enter the name of the app you registered in the Microsoft Azure portal.</span></span>
    - <span data-ttu-id="a7d2e-193">**ユーザー ID** フィールドで、管理者アクセス許可を持つユーザーのユーザー ID をHuman Resources と Power Apps 環境から選択します。</span><span class="sxs-lookup"><span data-stu-id="a7d2e-193">In the **User ID** field, select the user ID of a user with admin permissions in Human Resources and the Power Apps environment.</span></span>

3. <span data-ttu-id="a7d2e-194">**新規** を選択して、2 つ目の申請レコードを作成します。</span><span class="sxs-lookup"><span data-stu-id="a7d2e-194">Select **New** to create a second application record:</span></span>

    - <span data-ttu-id="a7d2e-195">**クライアント ID**: f9be0c49-aa22-4ec6-911a-c5da515226ff</span><span class="sxs-lookup"><span data-stu-id="a7d2e-195">**Client Id**: f9be0c49-aa22-4ec6-911a-c5da515226ff</span></span>
    - <span data-ttu-id="a7d2e-196">**名前**: Dynamics 365 HR Virtual Entity</span><span class="sxs-lookup"><span data-stu-id="a7d2e-196">**Name**: Dynamics 365 HR Virtual Entity</span></span>
    - <span data-ttu-id="a7d2e-197">**ユーザー ID** フィールドで、管理者アクセス許可を持つユーザーのユーザー ID をHuman Resources と Power Apps 環境から選択します。</span><span class="sxs-lookup"><span data-stu-id="a7d2e-197">In the **User ID** field, select the user ID of a user with admin permissions in Human Resources and the Power Apps environment.</span></span>

## <a name="generate-virtual-entities"></a><span data-ttu-id="a7d2e-198">仮想エンティティの生成</span><span class="sxs-lookup"><span data-stu-id="a7d2e-198">Generate virtual entities</span></span>

<span data-ttu-id="a7d2e-199">セットアップが完了したら、Common Data Service インスタンスで生成して有効にする仮想エンティティを選択できます。</span><span class="sxs-lookup"><span data-stu-id="a7d2e-199">When setup completes, you can select the virtual entities you want to generate and enable in your Common Data Service instance.</span></span>

1. <span data-ttu-id="a7d2e-200">Human Resources で、**Common Data Service (CDS) の統合** ページを開きます。</span><span class="sxs-lookup"><span data-stu-id="a7d2e-200">In Human Resources, open the **Common Data Service (CDS) integration** page.</span></span>

2. <span data-ttu-id="a7d2e-201">**仮想エンティティ** タブを選択します。</span><span class="sxs-lookup"><span data-stu-id="a7d2e-201">Select the **Virtual entities** tab.</span></span>

> [!NOTE]
> <span data-ttu-id="a7d2e-202">必要なすべての設定が完了すると、**仮想エンティティの有効化** トグルが自動的に **はい** に設定されます。</span><span class="sxs-lookup"><span data-stu-id="a7d2e-202">The **Enable the virtual entity** toggle will be set to **Yes** automatically when all required setup has been completed.</span></span> <span data-ttu-id="a7d2e-203">トグルが **いいえ** に設定されている場合は 、このドキュメントの前のセクションの手順を確認して、すべての前提条件の設定が完了していることを確認してください。</span><span class="sxs-lookup"><span data-stu-id="a7d2e-203">If the toggle is set to **No**, review the steps in previous sections of this document to ensure all prerequisite setup is completed.</span></span>

3. <span data-ttu-id="a7d2e-204">Common Data Service で生成するエンティティを選択します。</span><span class="sxs-lookup"><span data-stu-id="a7d2e-204">Select the entity or entities you want to generate in Common Data Service.</span></span>

4. <span data-ttu-id="a7d2e-205">**生成/更新** を選択します。</span><span class="sxs-lookup"><span data-stu-id="a7d2e-205">Select **Generate/refresh**.</span></span>

![Common Data Service の統合](./media/hr-admin-integration-common-data-service-integration.jpg)

## <a name="check-entity-generation-status"></a><span data-ttu-id="a7d2e-207">エンティティの生成状態の確認</span><span class="sxs-lookup"><span data-stu-id="a7d2e-207">Check entity generation status</span></span>

<span data-ttu-id="a7d2e-208">仮想エンティティは、非同期のバックグラウンド プロセスによって Common Data Service で生成されます。</span><span class="sxs-lookup"><span data-stu-id="a7d2e-208">Virtual entities are generated in Common Data Service through an asynchronous background process.</span></span> <span data-ttu-id="a7d2e-209">アクション センターのプロセス表示を更新します。</span><span class="sxs-lookup"><span data-stu-id="a7d2e-209">Updates on the process display in the action center.</span></span> <span data-ttu-id="a7d2e-210">エラー ログを含むプロセスの詳細については、**プロセスの自動化** ページに表示されます。</span><span class="sxs-lookup"><span data-stu-id="a7d2e-210">Details on the process, including error logs, appear in the **Process automations** page.</span></span>

1. <span data-ttu-id="a7d2e-211">Human Resources で、**プロセスの自動化** ページを開きます。</span><span class="sxs-lookup"><span data-stu-id="a7d2e-211">In Human Resources, open the **Process automations** page.</span></span>

2. <span data-ttu-id="a7d2e-212">**バックグラウンド プロセス** タブを選択し ます。</span><span class="sxs-lookup"><span data-stu-id="a7d2e-212">Select the **Background processes** tab.</span></span>

3. <span data-ttu-id="a7d2e-213">**仮想エンティティポーリング非同期操作のバックグラウンド プロセス** を選択します。</span><span class="sxs-lookup"><span data-stu-id="a7d2e-213">Select **Virtual entity poll async operation background process**.</span></span>

4. <span data-ttu-id="a7d2e-214">**最新の結果を表示する** を選択します。</span><span class="sxs-lookup"><span data-stu-id="a7d2e-214">Select **View most recent results**.</span></span>

<span data-ttu-id="a7d2e-215">スライドアウト ペインには、プロセスの最新の実行結果が表示されます。</span><span class="sxs-lookup"><span data-stu-id="a7d2e-215">The slideout pane displays the most recent execution results for the process.</span></span> <span data-ttu-id="a7d2e-216">Common Data Service から返されたエラーを含む、プロセスのログを表示することができます。</span><span class="sxs-lookup"><span data-stu-id="a7d2e-216">You can view the log for the process, including any errors returned from Common Data Service.</span></span>

## <a name="see-also"></a><span data-ttu-id="a7d2e-217">参照</span><span class="sxs-lookup"><span data-stu-id="a7d2e-217">See also</span></span>

[<span data-ttu-id="a7d2e-218">Common Data Service とは</span><span class="sxs-lookup"><span data-stu-id="a7d2e-218">What is Common Data Service?</span></span>](https://docs.microsoft.com/powerapps/maker/common-data-service/data-platform-intro)<br>
[<span data-ttu-id="a7d2e-219">エンティティ概要</span><span class="sxs-lookup"><span data-stu-id="a7d2e-219">Entity overview</span></span>](https://docs.microsoft.com/powerapps/maker/common-data-service/entity-overview)<br>
[<span data-ttu-id="a7d2e-220">エンティティの関連付けの概要</span><span class="sxs-lookup"><span data-stu-id="a7d2e-220">Entity relationships overview</span></span>](https://docs.microsoft.com/powerapps/maker/common-data-service/relationships-overview)<br>
[<span data-ttu-id="a7d2e-221">外部データ ソースのデータを含む仮想エンティティの作成と編集</span><span class="sxs-lookup"><span data-stu-id="a7d2e-221">Create and edit virtual entities that contain data from an external data source</span></span>](https://docs.microsoft.com/powerapps/maker/common-data-service/create-edit-virtual-entities)<br>
[<span data-ttu-id="a7d2e-222">Power Apps ポータルについて</span><span class="sxs-lookup"><span data-stu-id="a7d2e-222">What is Power Apps portals?</span></span>](https://docs.microsoft.com/powerapps/maker/portals/overview)<br>
[<span data-ttu-id="a7d2e-223">Power Apps でのアプリの作成の概要</span><span class="sxs-lookup"><span data-stu-id="a7d2e-223">Overview of creating apps in Power Apps</span></span>](https://docs.microsoft.com/powerapps/maker/)
