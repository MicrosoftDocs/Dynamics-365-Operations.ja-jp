---
title: Dataverse の仮想テーブルを構成する
description: このトピックでは、Dynamics 365 Human Resources の仮想テーブルを構成する方法について説明します。 既存の仮想テーブルを生成・更新し、生成されたエンティティと使用可能なテーブルを分析します。
author: andreabichsel
manager: tfehr
ms.date: 01/25/2021
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
ms.openlocfilehash: d8780be777c9a204fcb95950f5679a5711aee298
ms.sourcegitcommit: 6affb3316be757c99e1fe9c7c7b312b93c483408
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/17/2021
ms.locfileid: "5465825"
---
# <a name="configure-dataverse-virtual-tables"></a><span data-ttu-id="6a9d1-104">Dataverse の仮想テーブルを構成する</span><span class="sxs-lookup"><span data-stu-id="6a9d1-104">Configure Dataverse virtual tables</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="6a9d1-105">Dynamics 365 Human Resources は Microsoft Dataverse の仮想データ ソースです。</span><span class="sxs-lookup"><span data-stu-id="6a9d1-105">Dynamics 365 Human Resources is a virtual data source in Microsoft Dataverse.</span></span> <span data-ttu-id="6a9d1-106">このサービスでは、Dataverse および Microsoft Power Platform からの作成、読み取り、更新、および削除 (CRUD) の完全な操作が提供されます。</span><span class="sxs-lookup"><span data-stu-id="6a9d1-106">It provides full create, read, update, and delete (CRUD) operations from Dataverse and Microsoft Power Platform.</span></span> <span data-ttu-id="6a9d1-107">仮想テーブルのデータは Dataverse には格納されませんが、アプリケーション データベースに保存されます。</span><span class="sxs-lookup"><span data-stu-id="6a9d1-107">The data for virtual tables isn't stored in Dataverse, but in the application database.</span></span>

<span data-ttu-id="6a9d1-108">Dataverse から Human Resources エンティティに対して CRUD 操作を有効にするには、エンティティを Dataverse の仮想テーブルとして使用できるようにする必要があります。</span><span class="sxs-lookup"><span data-stu-id="6a9d1-108">To enable CRUD operations on Human Resources entities from Dataverse, you must make the entities available as virtual tables in Dataverse.</span></span> <span data-ttu-id="6a9d1-109">これにより、Human Resources のデータで Dataverse と Microsoft Power Platform から CRUD 操作を実行できます。</span><span class="sxs-lookup"><span data-stu-id="6a9d1-109">This lets you perform CRUD operations from Dataverse and Microsoft Power Platform on data that's in Human Resources.</span></span> <span data-ttu-id="6a9d1-110">また、この操作では、Human Resources のビジネス ロジックの完全な検証をサポートしているため、エンティティにデータを書き込むときにデータの整合性を確保できます。</span><span class="sxs-lookup"><span data-stu-id="6a9d1-110">The operations also support the full business logic validations of Human Resources to ensure data integrity when writing data to the entities.</span></span>

> [!NOTE]
> <span data-ttu-id="6a9d1-111">Human Resources エンティティは Dataverse テーブルに対応します。</span><span class="sxs-lookup"><span data-stu-id="6a9d1-111">Human Resources entities correspond to Dataverse tables.</span></span> <span data-ttu-id="6a9d1-112">Dataverse (旧 Common Data Service) および用語更新の詳細については、[Microsoft Dataverse とは何ですか?](https://docs.microsoft.com/powerapps/maker/data-platform/data-platform-intro)を参照してください</span><span class="sxs-lookup"><span data-stu-id="6a9d1-112">For more information about Dataverse (formerly Common Data Service) and terminology updates, see [What is Microsoft Dataverse?](https://docs.microsoft.com/powerapps/maker/data-platform/data-platform-intro)</span></span>

## <a name="available-virtual-tables-for-human-resources"></a><span data-ttu-id="6a9d1-113">Human Resources で使用可能な仮想テーブル</span><span class="sxs-lookup"><span data-stu-id="6a9d1-113">Available virtual tables for Human Resources</span></span>

<span data-ttu-id="6a9d1-114">Human Resources のすべての Open Data Protocol (OData) テーブルは、Dataverse の仮想エンティティとして使用できます。</span><span class="sxs-lookup"><span data-stu-id="6a9d1-114">All Open Data Protocol (OData) entities in Human Resources are available as virtual tables in Dataverse.</span></span> <span data-ttu-id="6a9d1-115">また、Power Platform で使用することもできます。</span><span class="sxs-lookup"><span data-stu-id="6a9d1-115">They're also available in Power Platform.</span></span> <span data-ttu-id="6a9d1-116">データを Dataverse にコピーまたは同期することなく、完全な CRUD 機能を備えた Human Resources からデータを使ってアプリとエクスペリエンスを直接ビルドできるようになりました。</span><span class="sxs-lookup"><span data-stu-id="6a9d1-116">You can now build apps and experiences with data directly from Human Resources with full CRUD capability, without copying or synchronizing data to Dataverse.</span></span> <span data-ttu-id="6a9d1-117">Power Apps ポータルは、Human Resources の業務プロセスのコラボレーション シナリオを可能にする外部向けの Web サイトをビルドするために使用できます。</span><span class="sxs-lookup"><span data-stu-id="6a9d1-117">You can use Power Apps portals to build external-facing websites that enable collaboration scenarios for business processes in Human Resources.</span></span>

<span data-ttu-id="6a9d1-118">環境で有効になっている仮想テーブルの一覧を表示し、**Dynamics 365 HR 仮想テーブル** ソリューションで [Power Apps](https://make.powerapps.com) のテーブルの操作を開始できます。</span><span class="sxs-lookup"><span data-stu-id="6a9d1-118">You can view the list of virtual tables enabled in the environment, and begin working with the tables in [Power Apps](https://make.powerapps.com), in the **Dynamics 365 HR Virtual Tables** solution.</span></span>

![Power Apps の Dynamics 365 HR 仮想テーブル](./media/hr-admin-integration-virtual-entities-power-apps.jpg)

## <a name="virtual-tables-versus-native-tables"></a><span data-ttu-id="6a9d1-120">仮想テーブルとネイティブ テーブルの対比</span><span class="sxs-lookup"><span data-stu-id="6a9d1-120">Virtual tables versus native tables</span></span>

<span data-ttu-id="6a9d1-121">Human Resources の仮想テーブルは、Human Resources 向けに作成されたネイティブの Dataverse テーブルとは異なります。</span><span class="sxs-lookup"><span data-stu-id="6a9d1-121">Virtual tables for Human Resources aren't the same as the native Dataverse tables created for Human Resources.</span></span> 

<span data-ttu-id="6a9d1-122">Human Resources のネイティブ テーブルは、Dataverse の HCM Common ソリューションで個別に生成・管理されます。</span><span class="sxs-lookup"><span data-stu-id="6a9d1-122">The native tables for Human Resources are generated separately and maintained in the HCM Common solution in Dataverse.</span></span> <span data-ttu-id="6a9d1-123">ナチュラル テーブルでは、データが Dataverse に保存され、Human Resources アプリケーション データベースとの同期が必要になります。</span><span class="sxs-lookup"><span data-stu-id="6a9d1-123">With native tables, the data is stored in Dataverse and requires synchronization with the Human Resources application database.</span></span>

> [!NOTE]
> <span data-ttu-id="6a9d1-124">Human Resources の Dataverse ナチュラル テーブルの一覧については、[Dataverse テーブル](https://docs.microsoft.com/dynamics365/human-resources/hr-developer-entities)を参照してください 。</span><span class="sxs-lookup"><span data-stu-id="6a9d1-124">For a list of the native Dataverse tables for Human Resources, see [Dataverse tables](https://docs.microsoft.com/dynamics365/human-resources/hr-developer-entities).</span></span>

## <a name="setup"></a><span data-ttu-id="6a9d1-125">段取り</span><span class="sxs-lookup"><span data-stu-id="6a9d1-125">Setup</span></span>

<span data-ttu-id="6a9d1-126">環境で仮想テーブルを有効にするには、次の設定手順に従います。</span><span class="sxs-lookup"><span data-stu-id="6a9d1-126">Follow these setup steps to enable virtual tables in your environment.</span></span>

### <a name="enable-virtual-tables-in-human-resources"></a><span data-ttu-id="6a9d1-127">Human Resources の仮想テーブルを有効にする</span><span class="sxs-lookup"><span data-stu-id="6a9d1-127">Enable virtual tables in Human Resources</span></span>

<span data-ttu-id="6a9d1-128">まず、**機能管理** ワークスペースで仮想テーブルを有効にする必要があります。</span><span class="sxs-lookup"><span data-stu-id="6a9d1-128">First, you must enable virtual tables in the **Feature management** workspace.</span></span>

1. <span data-ttu-id="6a9d1-129">人事管理では、**システム管理** を選択します。</span><span class="sxs-lookup"><span data-stu-id="6a9d1-129">In Human Resources, select **System administration**.</span></span>

2. <span data-ttu-id="6a9d1-130">**機能管理** タイルを選択します。</span><span class="sxs-lookup"><span data-stu-id="6a9d1-130">Select the **Feature management** tile.</span></span>

3. <span data-ttu-id="6a9d1-131">**Dataverse における HR の仮想テーブルのサポート** を選択し、**有効化** を選択します。</span><span class="sxs-lookup"><span data-stu-id="6a9d1-131">Select **Virtual table support for HR in Dataverse**, and then select **Enable**.</span></span>

<span data-ttu-id="6a9d1-132">有効化および無効化機能に関する情報は、[機能の管理](hr-admin-manage-features.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="6a9d1-132">For more information about enabling and disabling features, see [Manage features](hr-admin-manage-features.md).</span></span>

### <a name="register-the-app-in-microsoft-azure"></a><span data-ttu-id="6a9d1-133">アプリを Microsoft Azure に登録する</span><span class="sxs-lookup"><span data-stu-id="6a9d1-133">Register the app in Microsoft Azure</span></span>

<span data-ttu-id="6a9d1-134">Microsoft ID プラットフォームがアプリとユーザーに対して認証および承認サービスを提供できるように、Azure portal で Human Resources インスタンスを登録する必要があります。</span><span class="sxs-lookup"><span data-stu-id="6a9d1-134">You must register your Human Resources instance in the Azure portal so the Microsoft identity platform can provide authentication and authorization services for the app and users.</span></span> <span data-ttu-id="6a9d1-135">Azure でのアプリの登録に関する詳細については、「[クイックスタート: Microsoft ID プラットフォームでアプリケーションを登録する](https://docs.microsoft.com/azure/active-directory/develop/quickstart-register-app)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="6a9d1-135">For more information about registering apps in Azure, see [Quickstart: Register an application with the Microsoft identity platform](https://docs.microsoft.com/azure/active-directory/develop/quickstart-register-app).</span></span>

1. <span data-ttu-id="6a9d1-136">[Microsoft Azure ポータル](https://portal.azure.com)を開きます。</span><span class="sxs-lookup"><span data-stu-id="6a9d1-136">Open the [Microsoft Azure portal](https://portal.azure.com).</span></span>

2. <span data-ttu-id="6a9d1-137">Azure サービスの一覧で、**アプリの登録** を選択します。</span><span class="sxs-lookup"><span data-stu-id="6a9d1-137">In the Azure services list, select **App registrations**.</span></span>

3. <span data-ttu-id="6a9d1-138">**新規登録** を選択します。</span><span class="sxs-lookup"><span data-stu-id="6a9d1-138">Select **New registration**.</span></span>

4. <span data-ttu-id="6a9d1-139">**名前** フィールドに、アプリの内容を示す名前を入力します。</span><span class="sxs-lookup"><span data-stu-id="6a9d1-139">In the **Name** field, enter a descriptive name for the app.</span></span> <span data-ttu-id="6a9d1-140">たとえば、**Dynamics 365 Human Resources 仮想テーブル** です。</span><span class="sxs-lookup"><span data-stu-id="6a9d1-140">For example, **Dynamics 365 Human Resources Virtual Tables**.</span></span>

5. <span data-ttu-id="6a9d1-141">**リダイレクト URI** フィールドに、Human Resources のインスタンスの名前空間 URL を入力します。</span><span class="sxs-lookup"><span data-stu-id="6a9d1-141">In the **Redirect URI** field, enter the namespace URL of your instance of Human Resources.</span></span>

6. <span data-ttu-id="6a9d1-142">**登録** を選択します。</span><span class="sxs-lookup"><span data-stu-id="6a9d1-142">Select **Register**.</span></span>

7. <span data-ttu-id="6a9d1-143">登録が完了すると、Azure portal には、**アプリケーション (クライアント) ID** を含むアプリ登録の **概要** ウィンドウが表示されます。</span><span class="sxs-lookup"><span data-stu-id="6a9d1-143">When registration completes, the Azure portal displays the app registration's **Overview** pane, which includes its **Application (client) ID**.</span></span> <span data-ttu-id="6a9d1-144">この時点で **アプリケーション (クライアント) ID** をメモします。</span><span class="sxs-lookup"><span data-stu-id="6a9d1-144">Take note of the **Application (client) ID** at this time.</span></span> <span data-ttu-id="6a9d1-145">この情報は、[仮想テーブル データ ソースを構成する](hr-admin-integration-common-data-service-virtual-entities.md#configure-the-virtual-table-data-source)際に入力します。</span><span class="sxs-lookup"><span data-stu-id="6a9d1-145">You'll enter this information when you [Configure the virtual table data source](hr-admin-integration-common-data-service-virtual-entities.md#configure-the-virtual-table-data-source).</span></span>

8. <span data-ttu-id="6a9d1-146">左側のナビゲーション ウィンドウで、**証明書とシークレット** を選択します。</span><span class="sxs-lookup"><span data-stu-id="6a9d1-146">In the left navigation pane, select **Certificates and secrets**.</span></span>

9. <span data-ttu-id="6a9d1-147">ページの **クライアント シークレット** セクションで、**新しいクライアント シークレット** を選択します。</span><span class="sxs-lookup"><span data-stu-id="6a9d1-147">In the **Client secrets** section of the page, select **New client secret**.</span></span>

10. <span data-ttu-id="6a9d1-148">説明を入力し、期間を選択して、**追加** を選択します。</span><span class="sxs-lookup"><span data-stu-id="6a9d1-148">Provide a description, select a duration, and select **Add**.</span></span>

11. <span data-ttu-id="6a9d1-149">シークレットの値を記録します。</span><span class="sxs-lookup"><span data-stu-id="6a9d1-149">Record the secret's value.</span></span> <span data-ttu-id="6a9d1-150">この情報は、[仮想テーブル データ ソースを構成する](hr-admin-integration-common-data-service-virtual-entities.md#configure-the-virtual-table-data-source)際に入力します。</span><span class="sxs-lookup"><span data-stu-id="6a9d1-150">You'll enter this information when you [Configure the virtual table data source](hr-admin-integration-common-data-service-virtual-entities.md#configure-the-virtual-table-data-source).</span></span>

    > [!IMPORTANT]
    > <span data-ttu-id="6a9d1-151">この時点でシークレットの値をメモしておく必要があります。</span><span class="sxs-lookup"><span data-stu-id="6a9d1-151">Be sure to take note of the secret's value at this time.</span></span> <span data-ttu-id="6a9d1-152">このページから移動すると、シークレットは再度表示されません。</span><span class="sxs-lookup"><span data-stu-id="6a9d1-152">The secret is never displayed again after you leave this page.</span></span>

### <a name="install-the-dynamics-365-hr-virtual-table-app"></a><span data-ttu-id="6a9d1-153">Dynamics 365 HR 仮想テーブル アプリのインストール</span><span class="sxs-lookup"><span data-stu-id="6a9d1-153">Install the Dynamics 365 HR Virtual Table app</span></span>

<span data-ttu-id="6a9d1-154">Power Apps 環境に Dynamics 365 HR Virtual テーブルアプリをインストールして、仮想テーブルのソリューション パッケージを Dataverse にデプロイします。</span><span class="sxs-lookup"><span data-stu-id="6a9d1-154">Install the Dynamics 365 HR Virtual Table app in your Power Apps environment to deploy the virtual table solution package to Dataverse.</span></span>

1. <span data-ttu-id="6a9d1-155">[Power Platform 管理センター](https://admin.powerplatform.microsoft.com)を開きます。</span><span class="sxs-lookup"><span data-stu-id="6a9d1-155">Open the [Power Platform admin center](https://admin.powerplatform.microsoft.com).</span></span>

2. <span data-ttu-id="6a9d1-156">**環境** の一覧で、Human Resources のインスタンスに関連付けられている Power Apps 環境を選択します。</span><span class="sxs-lookup"><span data-stu-id="6a9d1-156">In the **Environments** list, select the Power Apps environment associated with your Human Resources instance.</span></span>

3. <span data-ttu-id="6a9d1-157">ページの **リソース** セクションで、**Dynamics 365 アプリ** を選択します。</span><span class="sxs-lookup"><span data-stu-id="6a9d1-157">In the **Resources** section of the page, select **Dynamics 365 apps**.</span></span>

4. <span data-ttu-id="6a9d1-158">**アプリのインストール** アクションを選択します。</span><span class="sxs-lookup"><span data-stu-id="6a9d1-158">Select the **Install app** action.</span></span>

5. <span data-ttu-id="6a9d1-159">**Dynamics 365 HR 仮想テーブル** を選択し、**次へ** を選択します。</span><span class="sxs-lookup"><span data-stu-id="6a9d1-159">Select **Dynamics 365 HR Virtual Table**, and select **Next**.</span></span>

6. <span data-ttu-id="6a9d1-160">サービス使用条件に同意することを確認してマークします。</span><span class="sxs-lookup"><span data-stu-id="6a9d1-160">Review and mark to agree to the terms of service.</span></span>

7. <span data-ttu-id="6a9d1-161">**インストール** を選択します。</span><span class="sxs-lookup"><span data-stu-id="6a9d1-161">Select **Install**.</span></span>

<span data-ttu-id="6a9d1-162">インストールには数分かかります。</span><span class="sxs-lookup"><span data-stu-id="6a9d1-162">The install takes a few minutes.</span></span> <span data-ttu-id="6a9d1-163">完了したら、次の手順に進みます。</span><span class="sxs-lookup"><span data-stu-id="6a9d1-163">When it completes, continue to the next steps.</span></span>

![Power Platform 管理センターから Dynamics 365 HR 仮想テーブル アプリをインストールします](./media/hr-admin-integration-virtual-entities-power-platform-install.jpg)

### <a name="configure-the-virtual-table-data-source"></a><span data-ttu-id="6a9d1-165">仮想テーブル データ ソースの構成</span><span class="sxs-lookup"><span data-stu-id="6a9d1-165">Configure the virtual table data source</span></span> 

<span data-ttu-id="6a9d1-166">次の手順では、Power Apps 環境で仮想テーブルのデータ ソースを構成します。</span><span class="sxs-lookup"><span data-stu-id="6a9d1-166">The next step is to configure the virtual table data source in the Power Apps environment.</span></span> 

1. <span data-ttu-id="6a9d1-167">[Power Platform 管理センター](https://admin.powerplatform.microsoft.com)を開きます。</span><span class="sxs-lookup"><span data-stu-id="6a9d1-167">Open the [Power Platform admin center](https://admin.powerplatform.microsoft.com).</span></span>

2. <span data-ttu-id="6a9d1-168">**環境** の一覧で、Human Resources のインスタンスに関連付けられている Power Apps 環境を選択します。</span><span class="sxs-lookup"><span data-stu-id="6a9d1-168">In the **Environments** list, select the Power Apps environment associated with your Human Resources instance.</span></span>

3. <span data-ttu-id="6a9d1-169">ページの **詳細** セクションで、**環境 URL** を選択します。</span><span class="sxs-lookup"><span data-stu-id="6a9d1-169">Select the **Environment URL** in the **Details** section of the page.</span></span>

4. <span data-ttu-id="6a9d1-170">**ソリューションの正常性ハブ** で、アプリケーション ページの右上にある **高度な検索** アイコンを選択します。</span><span class="sxs-lookup"><span data-stu-id="6a9d1-170">In the **Solution Health Hub**, select the **Advanced Find** icon in the top right of the application page.</span></span>

5. <span data-ttu-id="6a9d1-171">**高度な検索** ページの **検索対象** ドロップダウン リストで、**Finance and Operations 仮想データ ソースの構成** を選択します。</span><span class="sxs-lookup"><span data-stu-id="6a9d1-171">On the **Advanced Find** page, in the **Look for** dropdown list, select **Finance and Operations Virtual Data Source Configurations**.</span></span>

6. <span data-ttu-id="6a9d1-172">**結果** を選択します。</span><span class="sxs-lookup"><span data-stu-id="6a9d1-172">Select **Results**.</span></span>

7. <span data-ttu-id="6a9d1-173">**Microsoft HR データ ソース** のレコードを選択します。</span><span class="sxs-lookup"><span data-stu-id="6a9d1-173">Select the **Microsoft HR Data Source** record.</span></span>

8. <span data-ttu-id="6a9d1-174">データ ソースの構成に必要な情報を入力します。</span><span class="sxs-lookup"><span data-stu-id="6a9d1-174">Enter the required information for the data source configuration:</span></span>

   - <span data-ttu-id="6a9d1-175">**ターゲット URL**: Human Resources の名前空間の URL。</span><span class="sxs-lookup"><span data-stu-id="6a9d1-175">**Target URL**: The URL of your Human Resources namespace.</span></span> <span data-ttu-id="6a9d1-176">ターゲット URL の形式は次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="6a9d1-176">The format of the target URL is:</span></span>
     
     <span data-ttu-id="6a9d1-177">https://\<hostname\>.hr.talent.dynamics.com/namespaces/\<namespaceID\>/</span><span class="sxs-lookup"><span data-stu-id="6a9d1-177">https://\<hostname\>.hr.talent.dynamics.com/namespaces/\<namespaceID\>/</span></span>

     <span data-ttu-id="6a9d1-178">例:</span><span class="sxs-lookup"><span data-stu-id="6a9d1-178">For example:</span></span>
     
     `https://aos.rts-sf-5ea54e35c68-westus2.hr.talent.dynamics.com/namespaces/49d24c565-8f4d-4891-b174-bf83d948ed0c/`

     >[!NOTE]
     ><span data-ttu-id="6a9d1-179">URL の末尾に "**/**" 文字を挿入し、エラーを回避します。</span><span class="sxs-lookup"><span data-stu-id="6a9d1-179">Be sure to include the "**/**" character at the end of the URL to avoid receiving an error.</span></span>

   - <span data-ttu-id="6a9d1-180">**テナント ID**: Azure Active Directory (Azure AD) テナント ID。</span><span class="sxs-lookup"><span data-stu-id="6a9d1-180">**Tenant ID**: The Azure Active Directory (Azure AD) tenant ID.</span></span>

   - <span data-ttu-id="6a9d1-181">**AAD アプリケーション ID**: Microsoft Azure ポータルに登録されているアプリケーションに対して作成されたアプリケーション (クライアント) ID。</span><span class="sxs-lookup"><span data-stu-id="6a9d1-181">**AAD Application ID**: The application (client) ID created for the application registered in the Microsoft Azure portal.</span></span> <span data-ttu-id="6a9d1-182">この情報は、[アプリを Microsoft Azure に登録する](hr-admin-integration-common-data-service-virtual-entities.md#register-the-app-in-microsoft-azure)のステップで先に取得しました。</span><span class="sxs-lookup"><span data-stu-id="6a9d1-182">You received this information earlier during the step [Register the app in Microsoft Azure](hr-admin-integration-common-data-service-virtual-entities.md#register-the-app-in-microsoft-azure).</span></span>

   - <span data-ttu-id="6a9d1-183">**AAD アプリケーション シークレット**: Microsoft Azure ポータルに登録されているアプリケーションに対して作成されたクライアント シークレット。</span><span class="sxs-lookup"><span data-stu-id="6a9d1-183">**AAD Application Secret**: The client secret created for the application registered in the Microsoft Azure portal.</span></span> <span data-ttu-id="6a9d1-184">この情報は、[アプリを Microsoft Azure に登録する](hr-admin-integration-common-data-service-virtual-entities.md#register-the-app-in-microsoft-azure)のステップで先に取得しました。</span><span class="sxs-lookup"><span data-stu-id="6a9d1-184">You received this information earlier during the step [Register the app in Microsoft Azure](hr-admin-integration-common-data-service-virtual-entities.md#register-the-app-in-microsoft-azure).</span></span>

   ![Microsoft HR データ ソース](./media/hr-admin-integration-virtual-entities-hr-data-source.jpg)

9. <span data-ttu-id="6a9d1-186">**保存して閉じる** を選択します。</span><span class="sxs-lookup"><span data-stu-id="6a9d1-186">Select **Save & Close**.</span></span>

### <a name="grant-app-permissions-in-human-resources"></a><span data-ttu-id="6a9d1-187">Human Resources でアプリのアクセス許可を付与する</span><span class="sxs-lookup"><span data-stu-id="6a9d1-187">Grant app permissions in Human Resources</span></span>

<span data-ttu-id="6a9d1-188">Human Resources でアクセス許可を付与するのは、次の 2 つの Azure AD アプリケーションです。</span><span class="sxs-lookup"><span data-stu-id="6a9d1-188">Grant permissions for the two Azure AD applications in Human Resources:</span></span>

- <span data-ttu-id="6a9d1-189">Microsoft Azure ポータルでテナント用に作成されたアプリ</span><span class="sxs-lookup"><span data-stu-id="6a9d1-189">The app created for your tenant in the Microsoft Azure portal</span></span>
- <span data-ttu-id="6a9d1-190">Power Apps 環境にインストールされた Dynamics 365 HR 仮想テーブル アプリ</span><span class="sxs-lookup"><span data-stu-id="6a9d1-190">The Dynamics 365 HR Virtual Table app installed in the Power Apps environment</span></span> 

1. <span data-ttu-id="6a9d1-191">Human Resources で、**Azure Active Directory アプリケーション** ページを開きます。</span><span class="sxs-lookup"><span data-stu-id="6a9d1-191">In Human Resources, open the **Azure Active Directory applications** page.</span></span>

2. <span data-ttu-id="6a9d1-192">**新規** を選択して、新しい申請レコードを作成します。</span><span class="sxs-lookup"><span data-stu-id="6a9d1-192">Select **New** to create a new application record:</span></span>

    - <span data-ttu-id="6a9d1-193">**クライアント ID** フィールドに、Microsoft Azure ポータルに登録したアプリのクライアント ID を入力します。</span><span class="sxs-lookup"><span data-stu-id="6a9d1-193">In the **Client ID** field, enter the client ID of the app you registered in the Microsoft Azure portal.</span></span>
    - <span data-ttu-id="6a9d1-194">**名前** フィールドに、Microsoft Azure ポータルに登録したアプリの名前を入力します。</span><span class="sxs-lookup"><span data-stu-id="6a9d1-194">In the **Name** field, enter the name of the app you registered in the Microsoft Azure portal.</span></span>
    - <span data-ttu-id="6a9d1-195">**ユーザー ID** フィールドで、管理者アクセス許可を持つユーザーのユーザー ID をHuman Resources と Power Apps 環境から選択します。</span><span class="sxs-lookup"><span data-stu-id="6a9d1-195">In the **User ID** field, select the user ID of a user with admin permissions in Human Resources and the Power Apps environment.</span></span>

3. <span data-ttu-id="6a9d1-196">**新規** を選択して、2 つ目の申請レコードを作成します。</span><span class="sxs-lookup"><span data-stu-id="6a9d1-196">Select **New** to create a second application record:</span></span>

    - <span data-ttu-id="6a9d1-197">**クライアント ID**: f9be0c49-aa22-4ec6-911a-c5da515226ff</span><span class="sxs-lookup"><span data-stu-id="6a9d1-197">**Client Id**: f9be0c49-aa22-4ec6-911a-c5da515226ff</span></span>
    - <span data-ttu-id="6a9d1-198">**名前**: Dynamics 365 HR 仮想テーブル</span><span class="sxs-lookup"><span data-stu-id="6a9d1-198">**Name**: Dynamics 365 HR Virtual Table</span></span>
    - <span data-ttu-id="6a9d1-199">**ユーザー ID** フィールドで、管理者アクセス許可を持つユーザーのユーザー ID をHuman Resources と Power Apps 環境から選択します。</span><span class="sxs-lookup"><span data-stu-id="6a9d1-199">In the **User ID** field, select the user ID of a user with admin permissions in Human Resources and the Power Apps environment.</span></span>

## <a name="generate-virtual-tables"></a><span data-ttu-id="6a9d1-200">仮想テーブルの生成</span><span class="sxs-lookup"><span data-stu-id="6a9d1-200">Generate virtual tables</span></span>

<span data-ttu-id="6a9d1-201">設定が完了したら、Dataverse インスタンスで生成して有効にする仮想テーブルを選択できます。</span><span class="sxs-lookup"><span data-stu-id="6a9d1-201">When setup completes, you can select the virtual tables you want to generate and enable in your Dataverse instance.</span></span>

1. <span data-ttu-id="6a9d1-202">Human Resources で、**Dataverse の統合** ページを開きます。</span><span class="sxs-lookup"><span data-stu-id="6a9d1-202">In Human Resources, open the **Dataverse integration** page.</span></span>

2. <span data-ttu-id="6a9d1-203">**仮想テーブル** タブを選択します。</span><span class="sxs-lookup"><span data-stu-id="6a9d1-203">Select the **Virtual tables** tab.</span></span>

> [!NOTE]
> <span data-ttu-id="6a9d1-204">必要なすべての設定が完了すると、**仮想テーブルの有効化** トグルが自動的に **はい** に設定されます。</span><span class="sxs-lookup"><span data-stu-id="6a9d1-204">The **Enable virtual tables** toggle will be set to **Yes** automatically when all required setup has been completed.</span></span> <span data-ttu-id="6a9d1-205">トグルが **いいえ** に設定されている場合は 、このドキュメントの前のセクションの手順を確認して、すべての前提条件の設定が完了していることを確認してください。</span><span class="sxs-lookup"><span data-stu-id="6a9d1-205">If the toggle is set to **No**, review the steps in previous sections of this document to ensure all prerequisite setup is completed.</span></span>

3. <span data-ttu-id="6a9d1-206">Dataverse で生成するテーブルを選択します。</span><span class="sxs-lookup"><span data-stu-id="6a9d1-206">Select the table or tables you want to generate in Dataverse.</span></span>

4. <span data-ttu-id="6a9d1-207">**生成/更新** を選択します。</span><span class="sxs-lookup"><span data-stu-id="6a9d1-207">Select **Generate/refresh**.</span></span>

![Dataverse の統合](./media/hr-admin-integration-common-data-service-integration.jpg)

## <a name="check-table-generation-status"></a><span data-ttu-id="6a9d1-209">テーブルの生成状態の確認</span><span class="sxs-lookup"><span data-stu-id="6a9d1-209">Check table generation status</span></span>

<span data-ttu-id="6a9d1-210">仮想テーブルは、非同期のバックグラウンド プロセスによって Dataverse で生成されます。</span><span class="sxs-lookup"><span data-stu-id="6a9d1-210">Virtual tables are generated in Dataverse through an asynchronous background process.</span></span> <span data-ttu-id="6a9d1-211">アクション センターのプロセス表示を更新します。</span><span class="sxs-lookup"><span data-stu-id="6a9d1-211">Updates on the process display in the action center.</span></span> <span data-ttu-id="6a9d1-212">エラー ログを含むプロセスの詳細については、**プロセスの自動化** ページに表示されます。</span><span class="sxs-lookup"><span data-stu-id="6a9d1-212">Details on the process, including error logs, appear in the **Process automations** page.</span></span>

1. <span data-ttu-id="6a9d1-213">Human Resources で、**プロセスの自動化** ページを開きます。</span><span class="sxs-lookup"><span data-stu-id="6a9d1-213">In Human Resources, open the **Process automations** page.</span></span>

2. <span data-ttu-id="6a9d1-214">**バックグラウンド プロセス** タブを選択し ます。</span><span class="sxs-lookup"><span data-stu-id="6a9d1-214">Select the **Background processes** tab.</span></span>

3. <span data-ttu-id="6a9d1-215">**仮想テーブルポーリング非同期操作のバックグラウンド プロセス** を選択します。</span><span class="sxs-lookup"><span data-stu-id="6a9d1-215">Select **Virtual table poll async operation background process**.</span></span>

4. <span data-ttu-id="6a9d1-216">**最新の結果を表示する** を選択します。</span><span class="sxs-lookup"><span data-stu-id="6a9d1-216">Select **View most recent results**.</span></span>

<span data-ttu-id="6a9d1-217">スライドアウト ペインには、プロセスの最新の実行結果が表示されます。</span><span class="sxs-lookup"><span data-stu-id="6a9d1-217">The slideout pane displays the most recent execution results for the process.</span></span> <span data-ttu-id="6a9d1-218">Dataverse から返されたエラーを含む、プロセスのログを表示することができます。</span><span class="sxs-lookup"><span data-stu-id="6a9d1-218">You can view the log for the process, including any errors returned from Dataverse.</span></span>

## <a name="see-also"></a><span data-ttu-id="6a9d1-219">参照</span><span class="sxs-lookup"><span data-stu-id="6a9d1-219">See also</span></span>

[<span data-ttu-id="6a9d1-220">Dataverse とは</span><span class="sxs-lookup"><span data-stu-id="6a9d1-220">What is Dataverse?</span></span>](https://docs.microsoft.com/powerapps/maker/common-data-service/data-platform-intro)<br>
[<span data-ttu-id="6a9d1-221">Dataverse のテーブル</span><span class="sxs-lookup"><span data-stu-id="6a9d1-221">Tables in Dataverse</span></span>](https://docs.microsoft.com/powerapps/maker/common-data-service/entity-overview)<br>
[<span data-ttu-id="6a9d1-222">テーブルの関連付けの概要</span><span class="sxs-lookup"><span data-stu-id="6a9d1-222">Table relationships overview</span></span>](https://docs.microsoft.com/powerapps/maker/common-data-service/relationships-overview)<br>
[<span data-ttu-id="6a9d1-223">外部データ ソースのデータを含む仮想テーブルの作成と編集</span><span class="sxs-lookup"><span data-stu-id="6a9d1-223">Create and edit virtual tables that contain data from an external data source</span></span>](https://docs.microsoft.com/powerapps/maker/common-data-service/create-edit-virtual-entities)<br>
[<span data-ttu-id="6a9d1-224">Power Apps ポータルについて</span><span class="sxs-lookup"><span data-stu-id="6a9d1-224">What is Power Apps portals?</span></span>](https://docs.microsoft.com/powerapps/maker/portals/overview)<br>
[<span data-ttu-id="6a9d1-225">Power Apps でのアプリの作成の概要</span><span class="sxs-lookup"><span data-stu-id="6a9d1-225">Overview of creating apps in Power Apps</span></span>](https://docs.microsoft.com/powerapps/maker/)


[!INCLUDE[footer-include](../includes/footer-banner.md)]