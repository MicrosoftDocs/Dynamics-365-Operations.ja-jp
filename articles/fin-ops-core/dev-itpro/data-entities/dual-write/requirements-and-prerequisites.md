---
title: システム要件と前提条件
description: このトピックでは、Finance and Operations アプリで二重書き込みを有効にする前に設定する必要があるシステム要件と前提条件について説明します。
author: sabinn-msft
manager: AnnBe
ms.date: 03/20/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Developer
ms.reviewer: v-douklo
ms.search.scope: Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: sabinn
ms.search.validFrom: 2020-03-20
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 474dc7a51d8d48997484f1b11fd91d0d0bc90fb5
ms.sourcegitcommit: b3df62842e62234e8eaa16992375582518976131
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/17/2020
ms.locfileid: "3818636"
---
# <a name="system-requirements-and-prerequisites"></a><span data-ttu-id="36824-103">システム要件と前提条件</span><span class="sxs-lookup"><span data-stu-id="36824-103">System requirements and prerequisites</span></span>

[!include [banner](../../includes/banner.md)]


## <a name="what-regions-are-available"></a><span data-ttu-id="36824-104">どの地域で使用できますか?</span><span class="sxs-lookup"><span data-stu-id="36824-104">What regions are available?</span></span>

<span data-ttu-id="36824-105">現時点では、次の地域におけるデュアル書き込みをサポートしています。</span><span class="sxs-lookup"><span data-stu-id="36824-105">Currently, we support dual-write in the following regions:</span></span>
    
   + <span data-ttu-id="36824-106">アジア</span><span class="sxs-lookup"><span data-stu-id="36824-106">Asia</span></span>
   + <span data-ttu-id="36824-107">オーストラリア</span><span class="sxs-lookup"><span data-stu-id="36824-107">Australia</span></span>
   + <span data-ttu-id="36824-108">カナダ</span><span class="sxs-lookup"><span data-stu-id="36824-108">Canada</span></span>
   + <span data-ttu-id="36824-109">ヨーロッパ</span><span class="sxs-lookup"><span data-stu-id="36824-109">Europe</span></span>
   + <span data-ttu-id="36824-110">インド</span><span class="sxs-lookup"><span data-stu-id="36824-110">India</span></span>
   + <span data-ttu-id="36824-111">日本</span><span class="sxs-lookup"><span data-stu-id="36824-111">Japan</span></span>
   + <span data-ttu-id="36824-112">南アフリカ</span><span class="sxs-lookup"><span data-stu-id="36824-112">South America</span></span>
   + <span data-ttu-id="36824-113">英国</span><span class="sxs-lookup"><span data-stu-id="36824-113">United Kingdom</span></span>
   + <span data-ttu-id="36824-114">米国</span><span class="sxs-lookup"><span data-stu-id="36824-114">United States</span></span>


## <a name="verify-requirements-and-grant-access"></a><span data-ttu-id="36824-115">要件を確認し、アクセスを許可する</span><span class="sxs-lookup"><span data-stu-id="36824-115">Verify requirements and grant access</span></span>

<span data-ttu-id="36824-116">二重書き込みを有効にする前に、次の手順に従って、最小システム要件を満たしていることを確認し、相互に接続する必要があるアプリへのアクセスを許可します。</span><span class="sxs-lookup"><span data-stu-id="36824-116">Before you enable dual-write, follow these steps to make sure that you meet the minimum system requirements and to grant access to the apps that must connect to each other.</span></span> <span data-ttu-id="36824-117">二重書き込み正常性チェックは、Finance and Operations アプリ環境と Common Data Service 環境をリンクする二重書き込みウィザードを完了すると、前提条件を検証します。</span><span class="sxs-lookup"><span data-stu-id="36824-117">The dual-write health check validates the prerequisites as you complete the dual-write wizard to link a Finance and Operations app environment to a Common Data Service environment.</span></span>

<span data-ttu-id="36824-118">次の図に示すように、環境の設定時に**Dynamics 365 アプリ**を**はい**に設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="36824-118">You must set **Enable Dynamics 365 apps** to **Yes** when you set up the environment, as shown in the following image.</span></span> <span data-ttu-id="36824-119">または、Common Data Service に付属している Dynamics 365 環境で、すでに **Dynamics 365 アプリを有効化する**が**はい**に設定されているモデル駆動型アプリを選択することもできます。</span><span class="sxs-lookup"><span data-stu-id="36824-119">Alternatively, you can choose a model-driven app for Dynamics 365 environment that comes with Common Data Service and already has **Enable Dynamics 365 apps** set to **Yes**.</span></span>

:::image type="content" source="media/add_database.png" alt-text="アプリ切り替えの有効化" lightbox="media/add_database_expanded.png":::

1. <span data-ttu-id="36824-121">プラットフォーム更新プログラムとアプリのバージョンを検証します。</span><span class="sxs-lookup"><span data-stu-id="36824-121">Validate the platform update and app version.</span></span>

    <span data-ttu-id="36824-122">Finance and Operations アプリ環境で、Platform update 33 (アプリ バージョン 10.0.9) 以降が実行されていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="36824-122">Make sure that your Finance and Operations app environment is running Platform update 33 (app version 10.0.9) or later.</span></span>

    <span data-ttu-id="36824-123">**関連する正常性チェックの結果:**</span><span class="sxs-lookup"><span data-stu-id="36824-123">**Related health check result:**</span></span>

    <span data-ttu-id="36824-124">*アプリのバージョンが最新です*</span><span class="sxs-lookup"><span data-stu-id="36824-124">*App version is up to date*</span></span>

    <span data-ttu-id="36824-125">*二重書き込みは、Platform Update PU 33 (アプリ バージョン 10.0.9) 以上の Finance and Operations アプリ環境でサポートされています*</span><span class="sxs-lookup"><span data-stu-id="36824-125">*Dual Write is supported on Finance and Operations app environments with Platform Update PU 33 (App version 10.0.9) or above*</span></span>

2. <span data-ttu-id="36824-126">二重書き込みコア ソリューションをインストールします。</span><span class="sxs-lookup"><span data-stu-id="36824-126">Install the dual-write core solution.</span></span>

    <span data-ttu-id="36824-127">二重書き込みコア ソリューションには、エンティティ マップのメタデータが含まれており、環境にインストールする必要があります。</span><span class="sxs-lookup"><span data-stu-id="36824-127">The dual-write core solution contains metadata for your entity maps and must be installed in your environments.</span></span>

    1. <span data-ttu-id="36824-128">Power Apps の左ウィンドウで、**Solutions**を選択します。</span><span class="sxs-lookup"><span data-stu-id="36824-128">In Power Apps, in the left pane, select **Solutions**.</span></span>
    2. <span data-ttu-id="36824-129">**AppSource を開く**を選択します。</span><span class="sxs-lookup"><span data-stu-id="36824-129">Select **Open AppSource**.</span></span>
    3. <span data-ttu-id="36824-130">**二重書き込みコア** ソリューションを選択します。</span><span class="sxs-lookup"><span data-stu-id="36824-130">Select the **Dual Write Core** solution.</span></span>
    4. <span data-ttu-id="36824-131">プロンプトに従ってソリューションをインポートします。</span><span class="sxs-lookup"><span data-stu-id="36824-131">Follow the prompts to import the solution.</span></span>

    ![二重書き込みコア ソリューションのインストール](media/dual-write-core-solution.png)

    <span data-ttu-id="36824-133">**関連する正常性チェックの結果:**</span><span class="sxs-lookup"><span data-stu-id="36824-133">**Related health check result:**</span></span>

    <span data-ttu-id="36824-134">*二重書き込みコア ソリューションが見つかりました*</span><span class="sxs-lookup"><span data-stu-id="36824-134">*The dual-write core solution was found*</span></span>

    <span data-ttu-id="36824-135">*二重書き込みコア ソリューションには、エンティティ マップのメタデータが含まれており、環境にインストールする必要があります*</span><span class="sxs-lookup"><span data-stu-id="36824-135">*The dual-write core solution contains metadata for your entity maps and must be installed in the environment*</span></span>

3. <span data-ttu-id="36824-136">Finance and Operations アプリに接続できるように Common Data Service アクセスを許可します。</span><span class="sxs-lookup"><span data-stu-id="36824-136">Grant Common Data Service access so that it can connect to a Finance and Operations app.</span></span>

    1. <span data-ttu-id="36824-137">Finance and Operations アプリのインスタンスを開き 、Azure Active Directory アプリケーションを検索して移動します。</span><span class="sxs-lookup"><span data-stu-id="36824-137">Open your instance of the Finance and Operations app, search and navigate to Azure Active Directory applications.</span></span>

    2. <span data-ttu-id="36824-138">新しいクライアント ID レコード: **6f7d0213-62b1-43a8-b7f4-ff2bb8b7b452** を追加するには、**新規**を選択します。</span><span class="sxs-lookup"><span data-stu-id="36824-138">Select **New** to add a new client ID record: **6f7d0213-62b1-43a8-b7f4-ff2bb8b7b452**.</span></span> <span data-ttu-id="36824-139">このレコードは、Common Data Service から Finance and Operations アプリへの接続に使用されるアプリのアプリケーション ID です。</span><span class="sxs-lookup"><span data-stu-id="36824-139">This record is the application ID for an app that will be used to connect from Common Data Service to the Finance and Operations app.</span></span>
    3. <span data-ttu-id="36824-140">前の2つの手順を繰り返して、別のクライアント ID レコード: **2e49aa60-1bd3-43b6-8ab6-03ada3d9f08b** を追加します。</span><span class="sxs-lookup"><span data-stu-id="36824-140">Repeat the previous two steps to add another client ID record: **2e49aa60-1bd3-43b6-8ab6-03ada3d9f08b**.</span></span>

    <span data-ttu-id="36824-141">完了したら、次の手順に従ってエンティティの一覧を更新します:</span><span class="sxs-lookup"><span data-stu-id="36824-141">When you've finished, follow these steps to refresh the list of entities:</span></span>

    1. <span data-ttu-id="36824-142">**ワークスペース \> データ管理**に移動し、**データ エンティティ** タイルを選択して、エンティティ リストが入力されていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="36824-142">Go to **Workspaces \> Data management**, select the **Data entities** tile, and make sure that the entity list is filled in.</span></span>
    2. <span data-ttu-id="36824-143">**ワークスペース \> データ管理**に移動して、**フレームワーク パラメーター** タイルを選択します。</span><span class="sxs-lookup"><span data-stu-id="36824-143">Go to **Workspaces \> Data management**, and select the **Framework parameters** tile.</span></span> <span data-ttu-id="36824-144">次に、**エンティティ** タブ (`https://<BaseFinanceandOperationsappsURL>/?cmp=USMF&mi=DM_DataManagementWorkspaceMenuItem&TableName=DMFDefinitionGroupEntity`) で、**エンティティ リストの更新**を選択します。</span><span class="sxs-lookup"><span data-stu-id="36824-144">Then, on the **Entities** tab (`https://<BaseFinanceandOperationsappsURL>/?cmp=USMF&mi=DM_DataManagementWorkspaceMenuItem&TableName=DMFDefinitionGroupEntity`), select **Refresh entities list**.</span></span>

    <span data-ttu-id="36824-145">**関連する正常性チェックの結果:**</span><span class="sxs-lookup"><span data-stu-id="36824-145">**Related health check result:**</span></span><br>
    <span data-ttu-id="36824-146">*Common Data Service は Finance and Operations アプリに接続できます*</span><span class="sxs-lookup"><span data-stu-id="36824-146">*The Common Data Service can connect to the Finance and Operations app*</span></span><br>
    <span data-ttu-id="36824-147">*二重書き込みを有効にする前に、相互に接続するアプリへのアクセスを許可する必要があります<br> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;ID 6f7d0213-62b1-43a8-b7f4-ff2bb8b7b452 のアプリ ユーザーが存在します<br> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;ID 2e49aa60-1bd3-43b6-8ab6-03ada3d9f08b のアプリ ユーザーが存在します*</span><span class="sxs-lookup"><span data-stu-id="36824-147">*Before you can enable dual-write, you must grant access to the apps to connect to each other<br> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;App user with id 6f7d0213-62b1-43a8-b7f4-ff2bb8b7b452 exists<br> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;App user with id 2e49aa60-1bd3-43b6-8ab6-03ada3d9f08b exists*</span></span>

4. <span data-ttu-id="36824-148">Common Data Service に接続できるように Finance and Operations アプリへのアクセスを許可します。</span><span class="sxs-lookup"><span data-stu-id="36824-148">Grant a Finance and Operations app access so that it can connect to Common Data Service.</span></span>

    1. <span data-ttu-id="36824-149">Power Apps で、右上隅にある**設定**ボタン (ギヤ記号) を選択し、**詳細設定 \> セキュリティ** に移動して、**ユーザー**を選択します。</span><span class="sxs-lookup"><span data-stu-id="36824-149">In Power Apps, select the **Settings** button (gear symbol) in the upper-right corner, go to **Advanced settings \> Security**, and then select **Users**.</span></span>

        ![ユーザー](media/selecting-users.png)

    2. <span data-ttu-id="36824-151">ドロップダウン メニューを使用して、ビューを **有効なユーザー** から **アプリケーション ユーザー** に変更します。</span><span class="sxs-lookup"><span data-stu-id="36824-151">Use the drop-down menu to change the view from **Enabled Users** to **Application Users**.</span></span>

        ![アプリケーション ユーザー ビューへの切り替え](media/selecting-application-users.png)

    3. <span data-ttu-id="36824-153">新しいユーザーを作成し、**ユーザー** メニューで**アプリケーション ユーザー**を選択します。</span><span class="sxs-lookup"><span data-stu-id="36824-153">Create a new user, and then, on the **User** menu, select **Application User**.</span></span>

        ![アプリケーション ユーザーへの切り替え](media/create-new-user.png)

    4. <span data-ttu-id="36824-155">**アプリケーション ID** フィールドに、**00000015-0000-0000-c000-000000000000** と入力します。</span><span class="sxs-lookup"><span data-stu-id="36824-155">In the **Application ID** field, enter **00000015-0000-0000-c000-000000000000**.</span></span> <span data-ttu-id="36824-156">このアプリケーション ID は Finance and Operations アプリ用で、アプリを Common Data Service に接続できるようにします。</span><span class="sxs-lookup"><span data-stu-id="36824-156">This application ID is for a Finance and Operations app and will enable the app to connect to Common Data Service.</span></span> <span data-ttu-id="36824-157">完了したら、プロンプトに従って他のフィールドに入力し、ユーザー アカウントを保存します。</span><span class="sxs-lookup"><span data-stu-id="36824-157">When you've finished, follow the prompts to fill in the other fields, and then save the user account.</span></span>

        ![アプリケーション ID の入力](media/add-application-id.png)

    5. <span data-ttu-id="36824-159">基本電子メール アドレスを入力します。</span><span class="sxs-lookup"><span data-stu-id="36824-159">Provide a primary email address.</span></span>
    6. <span data-ttu-id="36824-160">**ロールの管理**を選択し、**ユーザー ロールの管理**ダイアログ ボックスで**システム管理者**チェック ボックスを選択して、選択したアプリケーション ユーザーにシステム管理者権限を付与します。</span><span class="sxs-lookup"><span data-stu-id="36824-160">Select **Manage Roles**, and then, in the **Manage User Roles** dialog box, select the **System Administrator** check box to provide system admin rights to the selected application user.</span></span>

        ![システム管理者ロールの割り当て](media/manage-user-roles.png)

    7. <span data-ttu-id="36824-162">**Dynamics 365 \> 設定 \> セキュリティ**に移動し、**チーム**を選択して、**すべての所有者チーム**にビューを変更します。</span><span class="sxs-lookup"><span data-stu-id="36824-162">Go to **Dynamics 365 \> Settings \> Security**, select **Teams**, and then change the view to **All Owner Teams**.</span></span>
    8. <span data-ttu-id="36824-163">**ルートの事業単位の既定のチーム**を選択し、**ロールの管理**を選択して、**チーム ロールの管理**ダイアログ ボックスで事前にコンフィギュレーションされた**セキュリティ ロール**を選択し、二重書き込みを通して統合された各エンティティの**ユーザー**スコープに対して**読み取り**権限を付与します。</span><span class="sxs-lookup"><span data-stu-id="36824-163">Select **default team for the root Business Unit**, select **Manage Roles**, and then, in the **Manage Team Roles** dialog box, select a preconfigured **Security Role** to grant a **Read** privilege with a **User** scope for each entity integrated through dual-write.</span></span> 
    
      <span data-ttu-id="36824-164">セキュリティ ロールの作成方法に関する説明については、[カスタム セキュリティ ロールの作成またはコンフィギュレーション](https://docs.microsoft.com/power-platform/admin/database-security#create-or-configure-a-custom-security-role)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="36824-164">For instructions on how to create a Security Role, see [Create or configure a custom security role](https://docs.microsoft.com/power-platform/admin/database-security#create-or-configure-a-custom-security-role).</span></span>
      
      > [!NOTE]
      > <span data-ttu-id="36824-165">ルートの事業単位の既定チームは、二重書き込みを通して統合されたすべてのレコードの既定の所有者になります。</span><span class="sxs-lookup"><span data-stu-id="36824-165">The root business unit’s default team will become the default owner for all records integrated through dual-write.</span></span>
      > <span data-ttu-id="36824-166">そのチームにはセキュリティ ロールが割り当てられている必要があるので、ルートの事業単位のユーザーすべてがセキュリティ ロールを継承します。</span><span class="sxs-lookup"><span data-stu-id="36824-166">Because that team must be assigned a security role, this means that all users in the root business unit will inherit the security role.</span></span>
      > <span data-ttu-id="36824-167">少なくとも、**事業単位のユーザーは、そのチームが所有しているすべてのレコードに対する読み取りアクセスを持つことになります**。</span><span class="sxs-lookup"><span data-stu-id="36824-167">This means that at the very least, **users from that business unit will have read access to all the records that are owned by that team**.</span></span> <span data-ttu-id="36824-168">これが必要な動作でない場合、ユーザーがルートの事業単位のメンバーでないことを確認します。</span><span class="sxs-lookup"><span data-stu-id="36824-168">If this isn’t the desired behavior, make sure that users are not a member of the root business unit.</span></span>

    9. <span data-ttu-id="36824-169">アプリケーションID **2e49aa60-1bd3-43b6-8ab6-03ada3d9f08b** について前の 5 つの手順を繰り返します。</span><span class="sxs-lookup"><span data-stu-id="36824-169">Repeat the previous five steps for application ID **2e49aa60-1bd3-43b6-8ab6-03ada3d9f08b**.</span></span>

        ![アプリケーション ID の割り当て](media/assign-application-id.png)

    <span data-ttu-id="36824-171">**関連する正常性チェックの結果:**</span><span class="sxs-lookup"><span data-stu-id="36824-171">**Related health check result:**</span></span><br>
    <span data-ttu-id="36824-172">*Finance and Operations アプリは Common Data Service に接続できます*</span><span class="sxs-lookup"><span data-stu-id="36824-172">*The Finance and Operations app can connect to the Common Data Service*</span></span><br>
    <span data-ttu-id="36824-173">*二重書き込みを有効にする前に、相互に接続するアプリへのアクセスを許可する必要があります<br> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;ID 00000015-0000-0000-c000-000000000000 のアプリ ユーザーが存在します<br> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;ID 2e49aa60-1bd3-43b6-8ab6-03ada3d9f08b のアプリ ユーザーが存在します*</span><span class="sxs-lookup"><span data-stu-id="36824-173">*Before you can enable dual-write, you must grant access to the apps to connect to each other<br> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;App user with id 00000015-0000-0000-c000-000000000000 exists<br> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;App user with id 2e49aa60-1bd3-43b6-8ab6-03ada3d9f08b exists*</span></span>

5. <span data-ttu-id="36824-174">テナントでアプリへの同意をします。</span><span class="sxs-lookup"><span data-stu-id="36824-174">Provide app consent in the tenant.</span></span>
   <span data-ttu-id="36824-175">バージョン 1.0.16.0 以上の二重書き込みコア ソリューションの場合、この手順は不要になりました。</span><span class="sxs-lookup"><span data-stu-id="36824-175">For dual-write core solution version 1.0.16.0 or above, this step is no longer needed.</span></span>
        
    <span data-ttu-id="36824-176">**関連する正常性チェックの結果:**</span><span class="sxs-lookup"><span data-stu-id="36824-176">**Related health check result:**</span></span><br>
    <span data-ttu-id="36824-177">*テナントのアプリ*</span><span class="sxs-lookup"><span data-stu-id="36824-177">*Apps in tenant*</span></span><br>
    <span data-ttu-id="36824-178">*必要な二重書き込みアプリケーションを、テナントにインストールする必要があります。<br> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;アプリ ID: 6f7d0213-62b1-43a8-b7f4-ff2bb8b7b452<br> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;アプリ ID: 2e49aa60-1bd3-43b6-8ab6-03ada3d9f08b*</span><span class="sxs-lookup"><span data-stu-id="36824-178">*The required dual-write applications need to be installed in the tenant.<br> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;App ID: 6f7d0213-62b1-43a8-b7f4-ff2bb8b7b452<br> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;App ID: 2e49aa60-1bd3-43b6-8ab6-03ada3d9f08b*</span></span>

6. <span data-ttu-id="36824-179">二重書き込みプラグインが有効になっていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="36824-179">Make sure that the dual-write plug-ins are enabled.</span></span>

    <span data-ttu-id="36824-180">二重書き込みコア ソリューションのインストール プロセスの一部としてプラグインを有効にする必要があるため、通常この手順は必要ありません。</span><span class="sxs-lookup"><span data-stu-id="36824-180">This step isn't usually required, because the plug-ins should be enabled as part of the process of installing the dual-write core solution.</span></span> <span data-ttu-id="36824-181">ただし、正常性チェックが失敗した場合は、次の手順に従って手動で二重書き込みプラグインを有効にします:</span><span class="sxs-lookup"><span data-stu-id="36824-181">However, if the health check fails, follow these steps to manually enable the dual-write plug-ins:</span></span>

    1. <span data-ttu-id="36824-182">[Plugin Registration Tool](https://www.nuget.org/packages/Microsoft.CrmSdk.XrmTooling.PluginRegistrationTool) をダウンロードします。</span><span class="sxs-lookup"><span data-stu-id="36824-182">Download the [Plug-in Registration Tool](https://www.nuget.org/packages/Microsoft.CrmSdk.XrmTooling.PluginRegistrationTool).</span></span>

        <span data-ttu-id="36824-183">Plugin Registration Tool には、二重書き込みに関連付けられている 2 つのプラグイン アセンブリが必要です: **DualWriteRegistration.Plugins** と **DualWriteRuntime.Plugins**。</span><span class="sxs-lookup"><span data-stu-id="36824-183">In the Plugin Registration Tool, there should be two plug-in assemblies that are associated with dual-write: **DualWriteRegistration.Plugins** and **DualWriteRuntime.Plugins**.</span></span> <span data-ttu-id="36824-184">これらのアセンブリには、二重書き込みを使用する前に、順番に有効にする必要があるプラグイン ステップがあります。</span><span class="sxs-lookup"><span data-stu-id="36824-184">These assemblies have plug-in steps that must be enabled, in order, before dual-write can be used.</span></span> <span data-ttu-id="36824-185">プラグイン ステップを表示するには、プラグイン アセンブリとそのプラグイン タイプを展開します。</span><span class="sxs-lookup"><span data-stu-id="36824-185">To view the plug-in steps, expand a plug-in assembly and its plug-in types.</span></span> <span data-ttu-id="36824-186">二重書き込みプラグイン アセンブリに属するすべてのステップを有効にする必要があります。</span><span class="sxs-lookup"><span data-stu-id="36824-186">All the steps that belong to the dual-write plug-in assemblies should be enabled.</span></span>

    2. <span data-ttu-id="36824-187">ステップを有効にするには、ステップを選択したまま (または右クリック) にし、**有効**を選択します。</span><span class="sxs-lookup"><span data-stu-id="36824-187">To enable a step, select and hold the step (or right-click it), and then select **Enable**.</span></span> <span data-ttu-id="36824-188">**有効**オプションがなく、**無効**オプションのみの場合、ステップは既に有効になっており、変更する必要はありません。</span><span class="sxs-lookup"><span data-stu-id="36824-188">If no **Enable** option is available, only a **Disable** option, the step has already been enabled and doesn't have to be changed.</span></span>

        ![Plugin Registration Tool の使用](media/plugin-registration-tool.png)

    > [!NOTE]
    > <span data-ttu-id="36824-190">二重書き込みプラグイン アセンブリが見つからない場合は、二重書き込みコア ソリューションの最新バージョンをインポートします。</span><span class="sxs-lookup"><span data-stu-id="36824-190">If the dual-write plug-in assemblies can't be found, import the latest version of the dual-write core solution.</span></span>

    <span data-ttu-id="36824-191">**関連する正常性チェックの結果:**</span><span class="sxs-lookup"><span data-stu-id="36824-191">**Related health check result:**</span></span><br>
    <span data-ttu-id="36824-192">*二重書き込み登録とランタイム プラグインが有効です*</span><span class="sxs-lookup"><span data-stu-id="36824-192">*The dual-write registration and runtime plugins are enabled*</span></span><br>
    <span data-ttu-id="36824-193">*Common Data Service で CRUD 操作を確実に行うには、二重書き込みプラグインを有効にする必要があります*</span><span class="sxs-lookup"><span data-stu-id="36824-193">*To ensure listening into CRUD operations on the Common Data Service, the dual-write plugins need to be enabled*</span></span>

7. <span data-ttu-id="36824-194">**二重書き込みアプリケーション オーケストレーション ソリューション** マップ ソリューションをインストールします。</span><span class="sxs-lookup"><span data-stu-id="36824-194">Install the **Dual-write application orchestration solution** maps solution.</span></span>

    <span data-ttu-id="36824-195">Power Apps の左ウィンドウで、**ソリューション**を選択します。</span><span class="sxs-lookup"><span data-stu-id="36824-195">In Power Apps, in the left pane, select **Solutions**.</span></span> <span data-ttu-id="36824-196">**AppSource を開く**を選択し、**二重書き込みアプリケーション オーケストレーション ソリューション**という名前のソリューションを検索します。</span><span class="sxs-lookup"><span data-stu-id="36824-196">Select **Open AppSource**, and search for the solution that is named **Dual-write application orchestration solution**.</span></span> <span data-ttu-id="36824-197">ソリューションを選択し、プロンプトに従ってインポートします。</span><span class="sxs-lookup"><span data-stu-id="36824-197">Select the solution, and follow the prompts to import it.</span></span> <span data-ttu-id="36824-198">インストール後、**ソリューション**の下に新しいソリューションがいくつか表示されます。</span><span class="sxs-lookup"><span data-stu-id="36824-198">After installation, you'll find several new solutions listed under **Solutions**.</span></span> <span data-ttu-id="36824-199">詳細については、[ソリューションの概要](https://docs.microsoft.com/powerapps/maker/common-data-service/solutions-overview)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="36824-199">For more information, see [Solutions overview](https://docs.microsoft.com/powerapps/maker/common-data-service/solutions-overview).</span></span> 
 
    <span data-ttu-id="36824-200">二重書き込みコア ソリューションには、エンティティ マップのメタデータが含まれていますが、二重書き込みアプリケーション オーケストレーション ソリューションには、次の追加のマスタ データ シナリオが含まれます:</span><span class="sxs-lookup"><span data-stu-id="36824-200">While the dual-write core solution contains metadata for your entity maps, the dual-write application orchestration solution covers these additional master data scenarios:</span></span>
    
    + <span data-ttu-id="36824-201">顧客、製品、仕入先。</span><span class="sxs-lookup"><span data-stu-id="36824-201">Customers, products, and vendors.</span></span>
    + <span data-ttu-id="36824-202">見込顧客から現金などのエンド ツー エンド プロセス フロー。</span><span class="sxs-lookup"><span data-stu-id="36824-202">End-to-end process flows like prospect to cash.</span></span>
    + <span data-ttu-id="36824-203">価格設定などのオンデマンド機能。</span><span class="sxs-lookup"><span data-stu-id="36824-203">On-demand functions like pricing.</span></span>
    + <span data-ttu-id="36824-204">元帳、税、支払条件、およびスケジュールの参照データ。</span><span class="sxs-lookup"><span data-stu-id="36824-204">Reference data for ledger, tax, payment terms, and schedules.</span></span> 
    
    <span data-ttu-id="36824-205">二重の書き込みは今後も拡大し続け、関係者、プロジェクト、手持在庫など、より多くのシナリオをサポートします。</span><span class="sxs-lookup"><span data-stu-id="36824-205">Dual-write will continue to expand in the future to support more scenarios including party, project, and hands-on inventory.</span></span> <span data-ttu-id="36824-206">フレームワークは拡張可能で、数回の追加クリックで顧客中心のビジネス データ交換にも対応します。</span><span class="sxs-lookup"><span data-stu-id="36824-206">The framework is extensible and accommodates customer-centric business data exchange through a few additional clicks.</span></span>
    
    > [!NOTE]
    > <span data-ttu-id="36824-207">二重書き込みウィザードを使用して環境をリンクする場合は、次の手順の一部として **ソリューションの適用** を選択する必要があります。</span><span class="sxs-lookup"><span data-stu-id="36824-207">You must select **Apply Solution** as part of the next steps, when you use the dual-write wizard to link your environments.</span></span> <span data-ttu-id="36824-208">Power Apps ソリューション セクションでソリューション パッケージが作成されるまでに数分かかる場合があります。</span><span class="sxs-lookup"><span data-stu-id="36824-208">It may take few minutes for the solution packages to be created in Power Apps solutions section.</span></span> <span data-ttu-id="36824-209">表示されるまで待ってから、次のステップに進みます。</span><span class="sxs-lookup"><span data-stu-id="36824-209">Wait for it to appear before moving to the next step.</span></span>

8. <span data-ttu-id="36824-210">見込顧客を現金化 (P2C) するソリューションをインストールします。</span><span class="sxs-lookup"><span data-stu-id="36824-210">Uninstall the Prospect to Cash (P2C) solution.</span></span>

    <span data-ttu-id="36824-211">P2C ソリューションは、二重書き込みと同時には機能しません。</span><span class="sxs-lookup"><span data-stu-id="36824-211">The P2C solution doesn't work concurrently with dual-write.</span></span> <span data-ttu-id="36824-212">したがって、P2C ソリューションをインストールしないでください。</span><span class="sxs-lookup"><span data-stu-id="36824-212">Therefore, don't install the P2C solution.</span></span> <span data-ttu-id="36824-213">既にインストールされている場合は、二重書き込みを有効にする前にアンインストールする必要があります。</span><span class="sxs-lookup"><span data-stu-id="36824-213">If it's already installed, you must uninstall it before you enable dual-write.</span></span>

9. <span data-ttu-id="36824-214">サポートされているテナント コンフィギュレーションを指定します。</span><span class="sxs-lookup"><span data-stu-id="36824-214">Provide the supported tenant configuration.</span></span>

    <span data-ttu-id="36824-215">Finance and Operations アプリと Common Data Service が同じテナントにインストールされていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="36824-215">Make sure that the Finance and Operations app and Common Data Service are installed under the same tenant.</span></span> <span data-ttu-id="36824-216">テナント間シナリオは現在サポートされていません。</span><span class="sxs-lookup"><span data-stu-id="36824-216">Cross-tenant scenarios aren't currently supported.</span></span>

    > [!NOTE]
    > <span data-ttu-id="36824-217">バージョン 1.0.16.0 より前の二重書き込みコア ソリューションについては、変更および追加の手順の次のセクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="36824-217">For dual-write core solution versions lower than 1.0.16.0, see the following section for modifications and additional steps.</span></span> 

<span data-ttu-id="36824-218">**バージョン 1.0.16.0 より前の二重書き込みコア ソリューションのみ**</span><span class="sxs-lookup"><span data-stu-id="36824-218">**For dual-write core solution lower than version 1.0.16.0 only**</span></span>

1. <span data-ttu-id="36824-219">上記の手順 3b で、新しいクライアント ID レコード **33976c19-1db5-4c02-810e-c243db79efde** (および 6f7d0213-62b1-43a8-b7f4-ff2bb8b7b452) を作成 します。</span><span class="sxs-lookup"><span data-stu-id="36824-219">In step Step 3b above, create a new client ID record: **33976c19-1db5-4c02-810e-c243db79efde** (versus 6f7d0213-62b1-43a8-b7f4-ff2bb8b7b452).</span></span>
2. <span data-ttu-id="36824-220">テナントでアプリへの同意を追加します。</span><span class="sxs-lookup"><span data-stu-id="36824-220">Add app consent in the tenant:</span></span>

    1. <span data-ttu-id="36824-221">次のURLを開き、管理者の資格情報を使用してサインインします。</span><span class="sxs-lookup"><span data-stu-id="36824-221">Open the following URL, and sign in by using your admin credentials.</span></span> <span data-ttu-id="36824-222">同意を求めるメッセージが表示されます。</span><span class="sxs-lookup"><span data-stu-id="36824-222">You should be prompted for consent.</span></span>

        [https://login.microsoftonline.com/common/oauth2/authorize?client_id=33976c19-1db5-4c02-810e-c243db79efde&response_type=code&prompt=admin_consent](https://login.microsoftonline.com/common/oauth2/authorize?client_id=33976c19-1db5-4c02-810e-c243db79efde&response_type=code&prompt=admin_consent)

    2. <span data-ttu-id="36824-223">**受け入れる** を選択します。</span><span class="sxs-lookup"><span data-stu-id="36824-223">Select **Accept**.</span></span>

        <span data-ttu-id="36824-224">**承認** を選択することで、テナントにアプリケーション ID **33976c19-1db5-4c02-810e-c243db79efde** を持つアプリのインストールに同意したことになります。</span><span class="sxs-lookup"><span data-stu-id="36824-224">By selecting **Accept**, you indicate that you're providing consent to install the app that has application ID **33976c19-1db5-4c02-810e-c243db79efde** in your tenant.</span></span> <span data-ttu-id="36824-225">Common Data Service は、Finance and Operations アプリと通信するためにこのアプリが必要です。</span><span class="sxs-lookup"><span data-stu-id="36824-225">Common Data Service requires this app to communicate with the Finance and Operations app.</span></span>

    
    <span data-ttu-id="36824-226">**関連する正常性チェックの結果:**</span><span class="sxs-lookup"><span data-stu-id="36824-226">**Related health check result:**</span></span><br>
    <span data-ttu-id="36824-227">*テナントのアプリ*</span><span class="sxs-lookup"><span data-stu-id="36824-227">*Apps in tenant*</span></span><br>
    <span data-ttu-id="36824-228">*必要な二重書き込みアプリケーションを、テナントにインストールする必要があります。<br> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;アプリ ID: 33976c19-1db5-4c02-810e-c243db79efde<br> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;アプリ ID: 2e49aa60-1bd3-43b6-8ab6-03ada3d9f08b*</span><span class="sxs-lookup"><span data-stu-id="36824-228">*The required dual-write applications need to be installed in the tenant.<br> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;App ID: 33976c19-1db5-4c02-810e-c243db79efde<br> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;App ID: 2e49aa60-1bd3-43b6-8ab6-03ada3d9f08b*</span></span>

## <a name="next-steps"></a><span data-ttu-id="36824-229">次のステップ</span><span class="sxs-lookup"><span data-stu-id="36824-229">Next steps</span></span>

[<span data-ttu-id="36824-230">二重書き込みウィザードを使用して環境をリンクする</span><span class="sxs-lookup"><span data-stu-id="36824-230">Use the dual-write wizard to link your environments</span></span>](link-your-environment.md)
