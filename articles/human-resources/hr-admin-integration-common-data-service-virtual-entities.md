---
title: Dataverse の仮想テーブルを構成する
description: このトピックでは、Dynamics 365 Human Resources の仮想テーブルを構成する方法について説明します。 既存の仮想テーブルを生成・更新し、生成されたエンティティと使用可能なテーブルを分析します。
author: andreabichsel
ms.date: 01/25/2021
ms.topic: article
ms.prod: ''
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
ms.openlocfilehash: 04997aba427ae6013c8154593b09ae1a45a580c3
ms.sourcegitcommit: 9283caad2d0636f98579c995784abec19fda2e3f
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/22/2021
ms.locfileid: "5935756"
---
# <a name="configure-dataverse-virtual-tables"></a><span data-ttu-id="8e484-104">Dataverse の仮想テーブルを構成する</span><span class="sxs-lookup"><span data-stu-id="8e484-104">Configure Dataverse virtual tables</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="8e484-105">Dynamics 365 Human Resources は Microsoft Dataverse の仮想データ ソースです。</span><span class="sxs-lookup"><span data-stu-id="8e484-105">Dynamics 365 Human Resources is a virtual data source in Microsoft Dataverse.</span></span> <span data-ttu-id="8e484-106">このサービスでは、Dataverse および Microsoft Power Platform からの作成、読み取り、更新、および削除 (CRUD) の完全な操作が提供されます。</span><span class="sxs-lookup"><span data-stu-id="8e484-106">It provides full create, read, update, and delete (CRUD) operations from Dataverse and Microsoft Power Platform.</span></span> <span data-ttu-id="8e484-107">仮想テーブルのデータは Dataverse には格納されませんが、アプリケーション データベースに保存されます。</span><span class="sxs-lookup"><span data-stu-id="8e484-107">The data for virtual tables isn't stored in Dataverse, but in the application database.</span></span>

<span data-ttu-id="8e484-108">Dataverse から Human Resources エンティティに対して CRUD 操作を有効にするには、エンティティを Dataverse の仮想テーブルとして使用できるようにする必要があります。</span><span class="sxs-lookup"><span data-stu-id="8e484-108">To enable CRUD operations on Human Resources entities from Dataverse, you must make the entities available as virtual tables in Dataverse.</span></span> <span data-ttu-id="8e484-109">これにより、Human Resources のデータで Dataverse と Microsoft Power Platform から CRUD 操作を実行できます。</span><span class="sxs-lookup"><span data-stu-id="8e484-109">This lets you perform CRUD operations from Dataverse and Microsoft Power Platform on data that's in Human Resources.</span></span> <span data-ttu-id="8e484-110">また、この操作では、Human Resources のビジネス ロジックの完全な検証をサポートしているため、エンティティにデータを書き込むときにデータの整合性を確保できます。</span><span class="sxs-lookup"><span data-stu-id="8e484-110">The operations also support the full business logic validations of Human Resources to ensure data integrity when writing data to the entities.</span></span>

> [!NOTE]
> <span data-ttu-id="8e484-111">Human Resources エンティティは Dataverse テーブルに対応します。</span><span class="sxs-lookup"><span data-stu-id="8e484-111">Human Resources entities correspond to Dataverse tables.</span></span> <span data-ttu-id="8e484-112">Dataverse (旧 Common Data Service) および用語更新の詳細については、[Microsoft Dataverse とは何ですか?](/powerapps/maker/data-platform/data-platform-intro)を参照してください</span><span class="sxs-lookup"><span data-stu-id="8e484-112">For more information about Dataverse (formerly Common Data Service) and terminology updates, see [What is Microsoft Dataverse?](/powerapps/maker/data-platform/data-platform-intro)</span></span>

## <a name="available-virtual-tables-for-human-resources"></a><span data-ttu-id="8e484-113">Human Resources で使用可能な仮想テーブル</span><span class="sxs-lookup"><span data-stu-id="8e484-113">Available virtual tables for Human Resources</span></span>

<span data-ttu-id="8e484-114">Human Resources のすべての Open Data Protocol (OData) テーブルは、Dataverse の仮想エンティティとして使用できます。</span><span class="sxs-lookup"><span data-stu-id="8e484-114">All Open Data Protocol (OData) entities in Human Resources are available as virtual tables in Dataverse.</span></span> <span data-ttu-id="8e484-115">また、Power Platform で使用することもできます。</span><span class="sxs-lookup"><span data-stu-id="8e484-115">They're also available in Power Platform.</span></span> <span data-ttu-id="8e484-116">データを Dataverse にコピーまたは同期することなく、完全な CRUD 機能を備えた Human Resources からデータを使ってアプリとエクスペリエンスを直接ビルドできるようになりました。</span><span class="sxs-lookup"><span data-stu-id="8e484-116">You can now build apps and experiences with data directly from Human Resources with full CRUD capability, without copying or synchronizing data to Dataverse.</span></span> <span data-ttu-id="8e484-117">Power Apps ポータルは、Human Resources の業務プロセスのコラボレーション シナリオを可能にする外部向けの Web サイトをビルドするために使用できます。</span><span class="sxs-lookup"><span data-stu-id="8e484-117">You can use Power Apps portals to build external-facing websites that enable collaboration scenarios for business processes in Human Resources.</span></span>

<span data-ttu-id="8e484-118">環境で有効になっている仮想テーブルの一覧を表示し、**Dynamics 365 HR 仮想テーブル** ソリューションで [Power Apps](https://make.powerapps.com) のテーブルの操作を開始できます。</span><span class="sxs-lookup"><span data-stu-id="8e484-118">You can view the list of virtual tables enabled in the environment, and begin working with the tables in [Power Apps](https://make.powerapps.com), in the **Dynamics 365 HR Virtual Tables** solution.</span></span>

![Power Apps の Dynamics 365 HR 仮想テーブル](./media/hr-admin-integration-virtual-entities-power-apps.jpg)

## <a name="virtual-tables-versus-native-tables"></a><span data-ttu-id="8e484-120">仮想テーブルとネイティブ テーブルの対比</span><span class="sxs-lookup"><span data-stu-id="8e484-120">Virtual tables versus native tables</span></span>

<span data-ttu-id="8e484-121">Human Resources の仮想テーブルは、Human Resources 向けに作成されたネイティブの Dataverse テーブルとは異なります。</span><span class="sxs-lookup"><span data-stu-id="8e484-121">Virtual tables for Human Resources aren't the same as the native Dataverse tables created for Human Resources.</span></span> 

<span data-ttu-id="8e484-122">Human Resources のネイティブ テーブルは、Dataverse の HCM Common ソリューションで個別に生成・管理されます。</span><span class="sxs-lookup"><span data-stu-id="8e484-122">The native tables for Human Resources are generated separately and maintained in the HCM Common solution in Dataverse.</span></span> <span data-ttu-id="8e484-123">ナチュラル テーブルでは、データが Dataverse に保存され、Human Resources アプリケーション データベースとの同期が必要になります。</span><span class="sxs-lookup"><span data-stu-id="8e484-123">With native tables, the data is stored in Dataverse and requires synchronization with the Human Resources application database.</span></span>

> [!NOTE]
> <span data-ttu-id="8e484-124">Human Resources の Dataverse ナチュラル テーブルの一覧については、[Dataverse テーブル](./hr-developer-entities.md)を参照してください 。</span><span class="sxs-lookup"><span data-stu-id="8e484-124">For a list of the native Dataverse tables for Human Resources, see [Dataverse tables](./hr-developer-entities.md).</span></span>

## <a name="setup"></a><span data-ttu-id="8e484-125">段取り</span><span class="sxs-lookup"><span data-stu-id="8e484-125">Setup</span></span>

<span data-ttu-id="8e484-126">環境で仮想テーブルを有効にするには、次の設定手順に従います。</span><span class="sxs-lookup"><span data-stu-id="8e484-126">Follow these setup steps to enable virtual tables in your environment.</span></span>

### <a name="enable-virtual-tables-in-human-resources"></a><span data-ttu-id="8e484-127">Human Resources の仮想テーブルを有効にする</span><span class="sxs-lookup"><span data-stu-id="8e484-127">Enable virtual tables in Human Resources</span></span>

<span data-ttu-id="8e484-128">まず、**機能管理** ワークスペースで仮想テーブルを有効にする必要があります。</span><span class="sxs-lookup"><span data-stu-id="8e484-128">First, you must enable virtual tables in the **Feature management** workspace.</span></span>

1. <span data-ttu-id="8e484-129">人事管理では、**システム管理** を選択します。</span><span class="sxs-lookup"><span data-stu-id="8e484-129">In Human Resources, select **System administration**.</span></span>

2. <span data-ttu-id="8e484-130">**機能管理** タイルを選択します。</span><span class="sxs-lookup"><span data-stu-id="8e484-130">Select the **Feature management** tile.</span></span>

3. <span data-ttu-id="8e484-131">**Dataverse における HR の仮想テーブルのサポート** を選択し、**有効化** を選択します。</span><span class="sxs-lookup"><span data-stu-id="8e484-131">Select **Virtual table support for HR in Dataverse**, and then select **Enable**.</span></span>

<span data-ttu-id="8e484-132">有効化および無効化機能に関する情報は、[機能の管理](hr-admin-manage-features.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="8e484-132">For more information about enabling and disabling features, see [Manage features](hr-admin-manage-features.md).</span></span>

### <a name="register-the-app-in-microsoft-azure"></a><span data-ttu-id="8e484-133">アプリを Microsoft Azure に登録する</span><span class="sxs-lookup"><span data-stu-id="8e484-133">Register the app in Microsoft Azure</span></span>

<span data-ttu-id="8e484-134">Microsoft ID プラットフォームがアプリとユーザーに対して認証および承認サービスを提供できるように、Azure portal で Human Resources インスタンスを登録する必要があります。</span><span class="sxs-lookup"><span data-stu-id="8e484-134">You must register your Human Resources instance in the Azure portal so the Microsoft identity platform can provide authentication and authorization services for the app and users.</span></span> <span data-ttu-id="8e484-135">Azure でのアプリの登録に関する詳細については、「[クイックスタート: Microsoft ID プラットフォームでアプリケーションを登録する](/azure/active-directory/develop/quickstart-register-app)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="8e484-135">For more information about registering apps in Azure, see [Quickstart: Register an application with the Microsoft identity platform](/azure/active-directory/develop/quickstart-register-app).</span></span>

1. <span data-ttu-id="8e484-136">[Microsoft Azure ポータル](https://portal.azure.com)を開きます。</span><span class="sxs-lookup"><span data-stu-id="8e484-136">Open the [Microsoft Azure portal](https://portal.azure.com).</span></span>

2. <span data-ttu-id="8e484-137">Azure サービスの一覧で、**アプリの登録** を選択します。</span><span class="sxs-lookup"><span data-stu-id="8e484-137">In the Azure services list, select **App registrations**.</span></span>

3. <span data-ttu-id="8e484-138">**新規登録** を選択します。</span><span class="sxs-lookup"><span data-stu-id="8e484-138">Select **New registration**.</span></span>

4. <span data-ttu-id="8e484-139">**名前** フィールドに、アプリの内容を示す名前を入力します。</span><span class="sxs-lookup"><span data-stu-id="8e484-139">In the **Name** field, enter a descriptive name for the app.</span></span> <span data-ttu-id="8e484-140">たとえば、**Dynamics 365 Human Resources 仮想テーブル** です。</span><span class="sxs-lookup"><span data-stu-id="8e484-140">For example, **Dynamics 365 Human Resources Virtual Tables**.</span></span>

5. <span data-ttu-id="8e484-141">**リダイレクト URI** フィールドに、Human Resources のインスタンスの名前空間 URL を入力します。</span><span class="sxs-lookup"><span data-stu-id="8e484-141">In the **Redirect URI** field, enter the namespace URL of your instance of Human Resources.</span></span>

6. <span data-ttu-id="8e484-142">**登録** を選択します。</span><span class="sxs-lookup"><span data-stu-id="8e484-142">Select **Register**.</span></span>

7. <span data-ttu-id="8e484-143">登録が完了すると、Azure portal には、**アプリケーション (クライアント) ID** を含むアプリ登録の **概要** ウィンドウが表示されます。</span><span class="sxs-lookup"><span data-stu-id="8e484-143">When registration completes, the Azure portal displays the app registration's **Overview** pane, which includes its **Application (client) ID**.</span></span> <span data-ttu-id="8e484-144">この時点で **アプリケーション (クライアント) ID** をメモします。</span><span class="sxs-lookup"><span data-stu-id="8e484-144">Take note of the **Application (client) ID** at this time.</span></span> <span data-ttu-id="8e484-145">この情報は、[仮想テーブル データ ソースを構成する](hr-admin-integration-common-data-service-virtual-entities.md#configure-the-virtual-table-data-source)際に入力します。</span><span class="sxs-lookup"><span data-stu-id="8e484-145">You'll enter this information when you [Configure the virtual table data source](hr-admin-integration-common-data-service-virtual-entities.md#configure-the-virtual-table-data-source).</span></span>

8. <span data-ttu-id="8e484-146">左側のナビゲーション ウィンドウで、**証明書とシークレット** を選択します。</span><span class="sxs-lookup"><span data-stu-id="8e484-146">In the left navigation pane, select **Certificates and secrets**.</span></span>

9. <span data-ttu-id="8e484-147">ページの **クライアント シークレット** セクションで、**新しいクライアント シークレット** を選択します。</span><span class="sxs-lookup"><span data-stu-id="8e484-147">In the **Client secrets** section of the page, select **New client secret**.</span></span>

10. <span data-ttu-id="8e484-148">説明を入力し、期間を選択して、**追加** を選択します。</span><span class="sxs-lookup"><span data-stu-id="8e484-148">Provide a description, select a duration, and select **Add**.</span></span>

11. <span data-ttu-id="8e484-149">テーブルの **値** プロパティからシークレットの値を記録します。</span><span class="sxs-lookup"><span data-stu-id="8e484-149">Record the secret's value from the **Value** property of the table.</span></span> <span data-ttu-id="8e484-150">この情報は、[仮想テーブル データ ソースを構成する](hr-admin-integration-common-data-service-virtual-entities.md#configure-the-virtual-table-data-source)際に入力します。</span><span class="sxs-lookup"><span data-stu-id="8e484-150">You'll enter this information when you [Configure the virtual table data source](hr-admin-integration-common-data-service-virtual-entities.md#configure-the-virtual-table-data-source).</span></span>

    > [!IMPORTANT]
    > <span data-ttu-id="8e484-151">この時点でシークレットの値をメモしておく必要があります。</span><span class="sxs-lookup"><span data-stu-id="8e484-151">Be sure to take note of the secret's value at this time.</span></span> <span data-ttu-id="8e484-152">このページから移動すると、シークレットは再度表示されません。</span><span class="sxs-lookup"><span data-stu-id="8e484-152">The secret is never displayed again after you leave this page.</span></span>

### <a name="install-the-dynamics-365-hr-virtual-table-app"></a><span data-ttu-id="8e484-153">Dynamics 365 HR 仮想テーブル アプリのインストール</span><span class="sxs-lookup"><span data-stu-id="8e484-153">Install the Dynamics 365 HR Virtual Table app</span></span>

<span data-ttu-id="8e484-154">Power Apps 環境に Dynamics 365 HR Virtual テーブルアプリをインストールして、仮想テーブルのソリューション パッケージを Dataverse にデプロイします。</span><span class="sxs-lookup"><span data-stu-id="8e484-154">Install the Dynamics 365 HR Virtual Table app in your Power Apps environment to deploy the virtual table solution package to Dataverse.</span></span>

1. <span data-ttu-id="8e484-155">Human Resources で、**Microsoft Dataverse の統合** ページを開きます。</span><span class="sxs-lookup"><span data-stu-id="8e484-155">In Human Resources, open the **Microsoft Dataverse integration** page.</span></span>

2. <span data-ttu-id="8e484-156">**仮想テーブル** タブを選択します。</span><span class="sxs-lookup"><span data-stu-id="8e484-156">Select the **Virtual tables** tab.</span></span>

3. <span data-ttu-id="8e484-157">**テーブル アプリのインストール** を選択します。</span><span class="sxs-lookup"><span data-stu-id="8e484-157">Select **Install virtual table app**.</span></span>

### <a name="configure-the-virtual-table-data-source"></a><span data-ttu-id="8e484-158">仮想テーブル データ ソースの構成</span><span class="sxs-lookup"><span data-stu-id="8e484-158">Configure the virtual table data source</span></span>

<span data-ttu-id="8e484-159">次の手順では、Power Apps 環境で仮想テーブルのデータ ソースを構成します。</span><span class="sxs-lookup"><span data-stu-id="8e484-159">The next step is to configure the virtual table data source in the Power Apps environment.</span></span>

1. <span data-ttu-id="8e484-160">[Power Platform 管理センター](https://admin.powerplatform.microsoft.com)を開きます。</span><span class="sxs-lookup"><span data-stu-id="8e484-160">Open the [Power Platform admin center](https://admin.powerplatform.microsoft.com).</span></span>

2. <span data-ttu-id="8e484-161">**環境** の一覧で、Human Resources のインスタンスに関連付けられている Power Apps 環境を選択します。</span><span class="sxs-lookup"><span data-stu-id="8e484-161">In the **Environments** list, select the Power Apps environment associated with your Human Resources instance.</span></span>

3. <span data-ttu-id="8e484-162">ページの **詳細** セクションで、**環境 URL** を選択します。</span><span class="sxs-lookup"><span data-stu-id="8e484-162">Select the **Environment URL** in the **Details** section of the page.</span></span>

4. <span data-ttu-id="8e484-163">**ソリューションの正常性ハブ** で、アプリケーション ページの右上にある **高度な検索** アイコンを選択します。</span><span class="sxs-lookup"><span data-stu-id="8e484-163">In the **Solution Health Hub**, select the **Advanced Find** icon in the top right of the application page.</span></span>

5. <span data-ttu-id="8e484-164">**高度な検索** ページの **検索対象** ドロップダウン リストで、**Finance and Operations 仮想データ ソースの構成** を選択します。</span><span class="sxs-lookup"><span data-stu-id="8e484-164">On the **Advanced Find** page, in the **Look for** dropdown list, select **Finance and Operations Virtual Data Source Configurations**.</span></span>

   > [!NOTE]
   > <span data-ttu-id="8e484-165">前の設定手順から仮想テーブル アプリをインストールするには、数分かかる場合があります。</span><span class="sxs-lookup"><span data-stu-id="8e484-165">The installation of the virtual table app from the previous setup step can take a few minutes.</span></span> <span data-ttu-id="8e484-166">**Finance and Operations 仮想データ ソースの構成** がリストにない場合は、1 分ほど待ってからリストを更新してください。</span><span class="sxs-lookup"><span data-stu-id="8e484-166">If **Finance and Operations Virtual Data Source Configurations** isn't available in the list, wait for a minute and refresh the list.</span></span>

6. <span data-ttu-id="8e484-167">**結果** を選択します。</span><span class="sxs-lookup"><span data-stu-id="8e484-167">Select **Results**.</span></span>

7. <span data-ttu-id="8e484-168">**Microsoft HR データ ソース** のレコードを選択します。</span><span class="sxs-lookup"><span data-stu-id="8e484-168">Select the **Microsoft HR Data Source** record.</span></span>

8. <span data-ttu-id="8e484-169">データ ソースの構成に必要な情報を入力します。</span><span class="sxs-lookup"><span data-stu-id="8e484-169">Enter the required information for the data source configuration:</span></span>

   - <span data-ttu-id="8e484-170">**ターゲット URL**: Human Resources の名前空間の URL。</span><span class="sxs-lookup"><span data-stu-id="8e484-170">**Target URL**: The URL of your Human Resources namespace.</span></span> <span data-ttu-id="8e484-171">ターゲット URL の形式は次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="8e484-171">The format of the target URL is:</span></span>
     
     <span data-ttu-id="8e484-172">https://\<hostname\>.hr.talent.dynamics.com/namespaces/\<namespaceID\>/</span><span class="sxs-lookup"><span data-stu-id="8e484-172">https://\<hostname\>.hr.talent.dynamics.com/namespaces/\<namespaceID\>/</span></span>

     <span data-ttu-id="8e484-173">例:</span><span class="sxs-lookup"><span data-stu-id="8e484-173">For example:</span></span>
     
     `https://aos.rts-sf-5ea54e35c68-westus2.hr.talent.dynamics.com/namespaces/49d24c565-8f4d-4891-b174-bf83d948ed0c/`

     >[!NOTE]
     ><span data-ttu-id="8e484-174">URL の末尾に "**/**" 文字を挿入し、エラーを回避します。</span><span class="sxs-lookup"><span data-stu-id="8e484-174">Be sure to include the "**/**" character at the end of the URL to avoid receiving an error.</span></span>

   - <span data-ttu-id="8e484-175">**テナント ID**: Azure Active Directory (Azure AD) テナント ID。</span><span class="sxs-lookup"><span data-stu-id="8e484-175">**Tenant ID**: The Azure Active Directory (Azure AD) tenant ID.</span></span>

   - <span data-ttu-id="8e484-176">**AAD アプリケーション ID**: Microsoft Azure ポータルに登録されているアプリケーションに対して作成されたアプリケーション (クライアント) ID。</span><span class="sxs-lookup"><span data-stu-id="8e484-176">**AAD Application ID**: The application (client) ID created for the application registered in the Microsoft Azure portal.</span></span> <span data-ttu-id="8e484-177">この情報は、[アプリを Microsoft Azure に登録する](hr-admin-integration-common-data-service-virtual-entities.md#register-the-app-in-microsoft-azure)のステップで先に取得しました。</span><span class="sxs-lookup"><span data-stu-id="8e484-177">You received this information earlier during the step [Register the app in Microsoft Azure](hr-admin-integration-common-data-service-virtual-entities.md#register-the-app-in-microsoft-azure).</span></span>

   - <span data-ttu-id="8e484-178">**AAD アプリケーション シークレット**: Microsoft Azure ポータルに登録されているアプリケーションに対して作成されたクライアント シークレット。</span><span class="sxs-lookup"><span data-stu-id="8e484-178">**AAD Application Secret**: The client secret created for the application registered in the Microsoft Azure portal.</span></span> <span data-ttu-id="8e484-179">この情報は、[アプリを Microsoft Azure に登録する](hr-admin-integration-common-data-service-virtual-entities.md#register-the-app-in-microsoft-azure)のステップで先に取得しました。</span><span class="sxs-lookup"><span data-stu-id="8e484-179">You received this information earlier during the step [Register the app in Microsoft Azure](hr-admin-integration-common-data-service-virtual-entities.md#register-the-app-in-microsoft-azure).</span></span>

   ![Microsoft HR データ ソース](./media/hr-admin-integration-virtual-entities-hr-data-source.jpg)

9. <span data-ttu-id="8e484-181">**保存して閉じる** を選択します。</span><span class="sxs-lookup"><span data-stu-id="8e484-181">Select **Save & Close**.</span></span>

### <a name="grant-app-permissions-in-human-resources"></a><span data-ttu-id="8e484-182">Human Resources でアプリのアクセス許可を付与する</span><span class="sxs-lookup"><span data-stu-id="8e484-182">Grant app permissions in Human Resources</span></span>

<span data-ttu-id="8e484-183">Human Resources でアクセス許可を付与するのは、次の 2 つの Azure AD アプリケーションです。</span><span class="sxs-lookup"><span data-stu-id="8e484-183">Grant permissions for the two Azure AD applications in Human Resources:</span></span>

- <span data-ttu-id="8e484-184">Microsoft Azure ポータルでテナント用に作成されたアプリ</span><span class="sxs-lookup"><span data-stu-id="8e484-184">The app created for your tenant in the Microsoft Azure portal</span></span>
- <span data-ttu-id="8e484-185">Power Apps 環境にインストールされた Dynamics 365 HR 仮想テーブル アプリ</span><span class="sxs-lookup"><span data-stu-id="8e484-185">The Dynamics 365 HR Virtual Table app installed in the Power Apps environment</span></span> 

1. <span data-ttu-id="8e484-186">Human Resources で、**Azure Active Directory アプリケーション** ページを開きます。</span><span class="sxs-lookup"><span data-stu-id="8e484-186">In Human Resources, open the **Azure Active Directory applications** page.</span></span>

2. <span data-ttu-id="8e484-187">**新規** を選択して、新しい申請レコードを作成します。</span><span class="sxs-lookup"><span data-stu-id="8e484-187">Select **New** to create a new application record:</span></span>

    - <span data-ttu-id="8e484-188">**クライアント ID** フィールドに、Microsoft Azure ポータルに登録したアプリのクライアント ID を入力します。</span><span class="sxs-lookup"><span data-stu-id="8e484-188">In the **Client ID** field, enter the client ID of the app you registered in the Microsoft Azure portal.</span></span>
    - <span data-ttu-id="8e484-189">**名前** フィールドに、Microsoft Azure ポータルに登録したアプリの名前を入力します。</span><span class="sxs-lookup"><span data-stu-id="8e484-189">In the **Name** field, enter the name of the app you registered in the Microsoft Azure portal.</span></span>
    - <span data-ttu-id="8e484-190">**ユーザー ID** フィールドで、管理者アクセス許可を持つユーザーのユーザー ID をHuman Resources と Power Apps 環境から選択します。</span><span class="sxs-lookup"><span data-stu-id="8e484-190">In the **User ID** field, select the user ID of a user with admin permissions in Human Resources and the Power Apps environment.</span></span>

3. <span data-ttu-id="8e484-191">**新規** を選択して、2 つ目の申請レコードを作成します。</span><span class="sxs-lookup"><span data-stu-id="8e484-191">Select **New** to create a second application record:</span></span>

    - <span data-ttu-id="8e484-192">**クライアント ID**: f9be0c49-aa22-4ec6-911a-c5da515226ff</span><span class="sxs-lookup"><span data-stu-id="8e484-192">**Client Id**: f9be0c49-aa22-4ec6-911a-c5da515226ff</span></span>
    - <span data-ttu-id="8e484-193">**名前**: Dynamics 365 HR 仮想テーブル</span><span class="sxs-lookup"><span data-stu-id="8e484-193">**Name**: Dynamics 365 HR Virtual Table</span></span>
    - <span data-ttu-id="8e484-194">**ユーザー ID** フィールドで、管理者アクセス許可を持つユーザーのユーザー ID をHuman Resources と Power Apps 環境から選択します。</span><span class="sxs-lookup"><span data-stu-id="8e484-194">In the **User ID** field, select the user ID of a user with admin permissions in Human Resources and the Power Apps environment.</span></span>

## <a name="generate-virtual-tables"></a><span data-ttu-id="8e484-195">仮想テーブルの生成</span><span class="sxs-lookup"><span data-stu-id="8e484-195">Generate virtual tables</span></span>

<span data-ttu-id="8e484-196">設定が完了したら、Dataverse インスタンスで生成して有効にする仮想テーブルを選択できます。</span><span class="sxs-lookup"><span data-stu-id="8e484-196">When setup completes, you can select the virtual tables you want to generate and enable in your Dataverse instance.</span></span>

1. <span data-ttu-id="8e484-197">Human Resources で、**Microsoft Dataverse の統合** ページを開きます。</span><span class="sxs-lookup"><span data-stu-id="8e484-197">In Human Resources, open the **Microsoft Dataverse integration** page.</span></span>

2. <span data-ttu-id="8e484-198">**仮想テーブル** タブを選択します。</span><span class="sxs-lookup"><span data-stu-id="8e484-198">Select the **Virtual tables** tab.</span></span>

> [!NOTE]
> <span data-ttu-id="8e484-199">必要なすべての設定が完了すると、**仮想テーブルの有効化** トグルが自動的に **はい** に設定されます。</span><span class="sxs-lookup"><span data-stu-id="8e484-199">The **Enable virtual tables** toggle will be set to **Yes** automatically when all required setup has been completed.</span></span> <span data-ttu-id="8e484-200">トグルが **いいえ** に設定されている場合は 、このドキュメントの前のセクションの手順を確認して、すべての前提条件の設定が完了していることを確認してください。</span><span class="sxs-lookup"><span data-stu-id="8e484-200">If the toggle is set to **No**, review the steps in previous sections of this document to ensure all prerequisite setup is completed.</span></span>

3. <span data-ttu-id="8e484-201">Dataverse で生成するテーブルを選択します。</span><span class="sxs-lookup"><span data-stu-id="8e484-201">Select the table or tables you want to generate in Dataverse.</span></span>

4. <span data-ttu-id="8e484-202">**生成/更新** を選択します。</span><span class="sxs-lookup"><span data-stu-id="8e484-202">Select **Generate/refresh**.</span></span>

![Dataverse の統合](./media/hr-admin-integration-dataverse-integration.png)

## <a name="check-table-generation-status"></a><span data-ttu-id="8e484-204">テーブルの生成状態の確認</span><span class="sxs-lookup"><span data-stu-id="8e484-204">Check table generation status</span></span>

<span data-ttu-id="8e484-205">仮想テーブルは、非同期のバックグラウンド プロセスによって Dataverse で生成されます。</span><span class="sxs-lookup"><span data-stu-id="8e484-205">Virtual tables are generated in Dataverse through an asynchronous background process.</span></span> <span data-ttu-id="8e484-206">アクション センターのプロセス表示を更新します。</span><span class="sxs-lookup"><span data-stu-id="8e484-206">Updates on the process display in the action center.</span></span> <span data-ttu-id="8e484-207">エラー ログを含むプロセスの詳細については、**プロセスの自動化** ページに表示されます。</span><span class="sxs-lookup"><span data-stu-id="8e484-207">Details on the process, including error logs, appear in the **Process automations** page.</span></span>

1. <span data-ttu-id="8e484-208">Human Resources で、**プロセスの自動化** ページを開きます。</span><span class="sxs-lookup"><span data-stu-id="8e484-208">In Human Resources, open the **Process automations** page.</span></span>

2. <span data-ttu-id="8e484-209">**バックグラウンド プロセス** タブを選択し ます。</span><span class="sxs-lookup"><span data-stu-id="8e484-209">Select the **Background processes** tab.</span></span>

3. <span data-ttu-id="8e484-210">**仮想テーブルポーリング非同期操作のバックグラウンド プロセス** を選択します。</span><span class="sxs-lookup"><span data-stu-id="8e484-210">Select **Virtual table poll async operation background process**.</span></span>

4. <span data-ttu-id="8e484-211">**最新の結果を表示する** を選択します。</span><span class="sxs-lookup"><span data-stu-id="8e484-211">Select **View most recent results**.</span></span>

<span data-ttu-id="8e484-212">スライドアウト ペインには、プロセスの最新の実行結果が表示されます。</span><span class="sxs-lookup"><span data-stu-id="8e484-212">The slideout pane displays the most recent execution results for the process.</span></span> <span data-ttu-id="8e484-213">Dataverse から返されたエラーを含む、プロセスのログを表示することができます。</span><span class="sxs-lookup"><span data-stu-id="8e484-213">You can view the log for the process, including any errors returned from Dataverse.</span></span>

## <a name="see-also"></a><span data-ttu-id="8e484-214">参照</span><span class="sxs-lookup"><span data-stu-id="8e484-214">See also</span></span>

[<span data-ttu-id="8e484-215">Dataverse とは</span><span class="sxs-lookup"><span data-stu-id="8e484-215">What is Dataverse?</span></span>](/powerapps/maker/common-data-service/data-platform-intro)<br>
[<span data-ttu-id="8e484-216">Dataverse のテーブル</span><span class="sxs-lookup"><span data-stu-id="8e484-216">Tables in Dataverse</span></span>](/powerapps/maker/common-data-service/entity-overview)<br>
[<span data-ttu-id="8e484-217">テーブルの関連付けの概要</span><span class="sxs-lookup"><span data-stu-id="8e484-217">Table relationships overview</span></span>](/powerapps/maker/common-data-service/relationships-overview)<br>
[<span data-ttu-id="8e484-218">外部データ ソースのデータを含む仮想テーブルの作成と編集</span><span class="sxs-lookup"><span data-stu-id="8e484-218">Create and edit virtual tables that contain data from an external data source</span></span>](/powerapps/maker/common-data-service/create-edit-virtual-entities)<br>
[<span data-ttu-id="8e484-219">Power Apps ポータルについて</span><span class="sxs-lookup"><span data-stu-id="8e484-219">What is Power Apps portals?</span></span>](/powerapps/maker/portals/overview)<br>
[<span data-ttu-id="8e484-220">Power Apps でのアプリの作成の概要</span><span class="sxs-lookup"><span data-stu-id="8e484-220">Overview of creating apps in Power Apps</span></span>](/powerapps/maker/)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
