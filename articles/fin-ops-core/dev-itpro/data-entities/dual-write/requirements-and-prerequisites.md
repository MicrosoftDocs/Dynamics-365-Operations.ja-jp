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
ms.openlocfilehash: a022230c65b4c05ff6aeb4a6a50f28def17ae01c
ms.sourcegitcommit: e69cfc74e9dbce64ae0e1ab7cd441e5ae6efd4c9
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/08/2020
ms.locfileid: "3353676"
---
# <a name="system-requirements-and-prerequisites"></a><span data-ttu-id="890b6-103">システム要件と前提条件</span><span class="sxs-lookup"><span data-stu-id="890b6-103">System requirements and prerequisites</span></span>

[!include [banner](../../includes/banner.md)]



## <a name="verify-requirements-and-grant-access"></a><span data-ttu-id="890b6-104">要件を確認し、アクセスを許可する</span><span class="sxs-lookup"><span data-stu-id="890b6-104">Verify requirements and grant access</span></span>

<span data-ttu-id="890b6-105">二重書き込みを有効にする前に、次の手順に従って、最小システム要件を満たしていることを確認し、相互に接続する必要があるアプリへのアクセスを許可します。</span><span class="sxs-lookup"><span data-stu-id="890b6-105">Before you enable dual-write, follow these steps to make sure that you meet the minimum system requirements and to grant access to the apps that must connect to each other.</span></span> <span data-ttu-id="890b6-106">二重書き込み正常性チェックは、Finance and Operations アプリ環境と Common Data Service 環境をリンクする二重書き込みウィザードを完了すると、前提条件を検証します。</span><span class="sxs-lookup"><span data-stu-id="890b6-106">The dual-write health check validates the prerequisites as you complete the dual-write wizard to link a Finance and Operations app environment to a Common Data Service environment.</span></span>

1. <span data-ttu-id="890b6-107">プラットフォーム更新プログラムとアプリのバージョンを検証します。</span><span class="sxs-lookup"><span data-stu-id="890b6-107">Validate the platform update and app version.</span></span>

    <span data-ttu-id="890b6-108">Finance and Operations アプリ環境で、Platform update 33 (アプリ バージョン 10.0.9) 以降が実行されていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="890b6-108">Make sure that your Finance and Operations app environment is running Platform update 33 (app version 10.0.9) or later.</span></span>

    <span data-ttu-id="890b6-109">**関連する正常性チェックの結果:**</span><span class="sxs-lookup"><span data-stu-id="890b6-109">**Related health check result:**</span></span>

    <span data-ttu-id="890b6-110">*アプリのバージョンが最新です*</span><span class="sxs-lookup"><span data-stu-id="890b6-110">*App version is up to date*</span></span>

    <span data-ttu-id="890b6-111">*二重書き込みは、Platform Update PU 33 (アプリ バージョン 10.0.9) 以上の Finance and Operationsアプリ環境でサポートされています*</span><span class="sxs-lookup"><span data-stu-id="890b6-111">*Dual Write is supported on Finance and Operations app environments with Platform Update PU 33 (App version 10.0.9) or above*</span></span>

2. <span data-ttu-id="890b6-112">二重書き込みコア ソリューションをインストールします。</span><span class="sxs-lookup"><span data-stu-id="890b6-112">Install the dual-write core solution.</span></span>

    <span data-ttu-id="890b6-113">二重書き込みコア ソリューションには、エンティティ マップのメタデータが含まれており、環境にインストールする必要があります。</span><span class="sxs-lookup"><span data-stu-id="890b6-113">The dual-write core solution contains metadata for your entity maps and must be installed in your environments.</span></span>

    1. <span data-ttu-id="890b6-114">Power Apps の左ウィンドウで、**ソリューション** を選択します。</span><span class="sxs-lookup"><span data-stu-id="890b6-114">In Power Apps, in the left pane, select **Solutions**.</span></span>
    2. <span data-ttu-id="890b6-115">**AppSource を開く** を選択します。</span><span class="sxs-lookup"><span data-stu-id="890b6-115">Select **Open AppSource**.</span></span>
    3. <span data-ttu-id="890b6-116">**二重書き込みコア** ソリューションを選択します。</span><span class="sxs-lookup"><span data-stu-id="890b6-116">Select the **Dual Write Core** solution.</span></span>
    4. <span data-ttu-id="890b6-117">プロンプトに従ってソリューションをインポートします。</span><span class="sxs-lookup"><span data-stu-id="890b6-117">Follow the prompts to import the solution.</span></span>

    ![二重書き込みコア ソリューションのインストール](media/dual-write-core-solution.png)

    <span data-ttu-id="890b6-119">**関連する正常性チェックの結果:**</span><span class="sxs-lookup"><span data-stu-id="890b6-119">**Related health check result:**</span></span>

    <span data-ttu-id="890b6-120">*二重書き込みコア ソリューションが見つかりました*</span><span class="sxs-lookup"><span data-stu-id="890b6-120">*The dual-write core solution was found*</span></span>

    <span data-ttu-id="890b6-121">*二重書き込みコア ソリューションには、エンティティ マップのメタデータが含まれており、環境にインストールする必要があります*</span><span class="sxs-lookup"><span data-stu-id="890b6-121">*The dual-write core solution contains metadata for your entity maps and must be installed in the environment*</span></span>

3. <span data-ttu-id="890b6-122">Finance and Operations アプリに接続できるように Common Data Service アクセスを許可します。</span><span class="sxs-lookup"><span data-stu-id="890b6-122">Grant Common Data Service access so that it can connect to a Finance and Operations app.</span></span>

    1. <span data-ttu-id="890b6-123">次の URL を使用して Finance and Operations アプリのインスタンスを開きます。</span><span class="sxs-lookup"><span data-stu-id="890b6-123">Open your instance of the Finance and Operations app by using the following URL.</span></span> <span data-ttu-id="890b6-124">**\<BaseFinanceandOperationsappsURL\>** をインスタンスに置き換えます。</span><span class="sxs-lookup"><span data-stu-id="890b6-124">Replace **\<BaseFinanceandOperationsappsURL\>** with your instance.</span></span>

        `https://<BaseFinanceandOperationsappsURL>/?cmp=DAT&mi=SysAADClientTable`

    2. <span data-ttu-id="890b6-125">新しいクライアント ID レコード: **33976c19-1db5-4c02-810e-c243db79efde** を追加するには、**新規** を選択します。</span><span class="sxs-lookup"><span data-stu-id="890b6-125">Select **New** to add a new client ID record: **33976c19-1db5-4c02-810e-c243db79efde**.</span></span> <span data-ttu-id="890b6-126">このレコードは、Common Data Service から Finance and Operations アプリへの接続に使用されるアプリのアプリケーション ID です。</span><span class="sxs-lookup"><span data-stu-id="890b6-126">This record is the application ID for an app that will be used to connect from Common Data Service to the Finance and Operations app.</span></span>
    3. <span data-ttu-id="890b6-127">前の2つの手順を繰り返して、別のクライアント ID レコード: **2e49aa60-1bd3-43b6-8ab6-03ada3d9f08b** を追加します。</span><span class="sxs-lookup"><span data-stu-id="890b6-127">Repeat the previous two steps to add another client ID record: **2e49aa60-1bd3-43b6-8ab6-03ada3d9f08b**.</span></span>

        ![別のクライアント ID レコードの追加](media/another-client-id-record.png)

    <span data-ttu-id="890b6-129">完了したら、次の手順に従ってエンティティの一覧を更新します:</span><span class="sxs-lookup"><span data-stu-id="890b6-129">When you've finished, follow these steps to refresh the list of entities:</span></span>

    1. <span data-ttu-id="890b6-130">**ワークスペース \> データ管理** に移動し、**データ エンティティ** タイルを選択して、エンティティ リストが入力されていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="890b6-130">Go to **Workspaces \> Data management**, select the **Data entities** tile, and make sure that the entity list is filled in.</span></span>
    2. <span data-ttu-id="890b6-131">**ワークスペース \> データ管理** に移動して、**フレームワーク パラメーター** タイルを選択します。</span><span class="sxs-lookup"><span data-stu-id="890b6-131">Go to **Workspaces \> Data management**, and select the **Framework parameters** tile.</span></span> <span data-ttu-id="890b6-132">次に、**エンティティ** タブ (`https://<BaseFinanceandOperationsappsURL>/?cmp=USMF&mi=DM_DataManagementWorkspaceMenuItem&TableName=DMFDefinitionGroupEntity`) で、**エンティティ リストの更新** を選択します。</span><span class="sxs-lookup"><span data-stu-id="890b6-132">Then, on the **Entities** tab (`https://<BaseFinanceandOperationsappsURL>/?cmp=USMF&mi=DM_DataManagementWorkspaceMenuItem&TableName=DMFDefinitionGroupEntity`), select **Refresh entities list**.</span></span>

    <span data-ttu-id="890b6-133">**関連する正常性チェックの結果:**</span><span class="sxs-lookup"><span data-stu-id="890b6-133">**Related health check result:**</span></span>

    <span data-ttu-id="890b6-134">*Common Data Service は Finance and Operations アプリに接続できます*</span><span class="sxs-lookup"><span data-stu-id="890b6-134">*The Common Data Service can connect to the Finance and Operations app*</span></span>

    <span data-ttu-id="890b6-135">*二重書き込みを有効にする前に、相互に接続するアプリへのアクセスを許可する必要があります<br> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;アプリ ID 33976c19-1db5-4c02-810e-c243db79efde が存在します<br> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;アプリ ID 2e49aa60-1bd3-43b6-8ab6-03ada3d9f08b が存在します<br> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;ID 33976c19-1db5-4c02-810e-c243db79efde のアプリ ユーザーが存在します<br> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;ID 2e49aa60-1bd3-43b6-8ab6-03ada3d9f08b のアプリ ユーザーが存在します*</span><span class="sxs-lookup"><span data-stu-id="890b6-135">*Before you can enable dual-write, you must grant access to the apps to connect to each other<br> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;App id 33976c19-1db5-4c02-810e-c243db79efde exists<br> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;App id 2e49aa60-1bd3-43b6-8ab6-03ada3d9f08b exists<br> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;App user with id 33976c19-1db5-4c02-810e-c243db79efde exists<br> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;App user with id 2e49aa60-1bd3-43b6-8ab6-03ada3d9f08b exists*</span></span>

4. <span data-ttu-id="890b6-136">Common Data Service に接続できるように Finance and Operations アプリへのアクセスを許可します。</span><span class="sxs-lookup"><span data-stu-id="890b6-136">Grant a Finance and Operations app access so that it can connect to Common Data Service.</span></span>

    1. <span data-ttu-id="890b6-137">Power Apps で、右上隅にある **設定** ボタン (ギヤ記号) を選択し、**詳細設定 \> セキュリティ** に移動して、**ユーザー** を選択します。</span><span class="sxs-lookup"><span data-stu-id="890b6-137">In Power Apps, select the **Settings** button (gear symbol) in the upper-right corner, go to **Advanced settings \> Security**, and then select **Users**.</span></span>

        ![ユーザー](media/selecting-users.png)

    2. <span data-ttu-id="890b6-139">ドロップダウン メニューを使用して、ビューを **有効なユーザー** から **アプリケーション ユーザー** に変更します。</span><span class="sxs-lookup"><span data-stu-id="890b6-139">Use the drop-down menu to change the view from **Enabled Users** to **Application Users**.</span></span>

        ![アプリケーション ユーザー ビューへの切り替え](media/selecting-application-users.png)

    3. <span data-ttu-id="890b6-141">新しいユーザーを作成し、**ユーザー** メニューで **アプリケーション ユーザー** を選択します。</span><span class="sxs-lookup"><span data-stu-id="890b6-141">Create a new user, and then, on the **User** menu, select **Application User**.</span></span>

        ![アプリケーション ユーザーへの切り替え](media/create-new-user.png)

    4. <span data-ttu-id="890b6-143">**アプリケーション ID** フィールドに、**00000015-0000-0000-c000-000000000000** と入力します。</span><span class="sxs-lookup"><span data-stu-id="890b6-143">In the **Application ID** field, enter **00000015-0000-0000-c000-000000000000**.</span></span> <span data-ttu-id="890b6-144">このアプリケーション ID は Finance and Operations アプリ用で、アプリを Common Data Service に接続できるようにします。</span><span class="sxs-lookup"><span data-stu-id="890b6-144">This application ID is for a Finance and Operations app and will enable the app to connect to Common Data Service.</span></span> <span data-ttu-id="890b6-145">完了したら、プロンプトに従って他のフィールドに入力し、ユーザー アカウントを保存します。</span><span class="sxs-lookup"><span data-stu-id="890b6-145">When you've finished, follow the prompts to fill in the other fields, and then save the user account.</span></span>

        ![アプリケーション ID の入力](media/add-application-id.png)

    5. <span data-ttu-id="890b6-147">基本電子メール アドレスを入力します。</span><span class="sxs-lookup"><span data-stu-id="890b6-147">Provide a primary email address.</span></span>
    6. <span data-ttu-id="890b6-148">**ロールの管理** を選択し、**ユーザー ロールの管理** ダイアログ ボックスで **システム管理者** チェック ボックスを選択して、選択したアプリケーション ユーザーにシステム管理者権限を付与します。</span><span class="sxs-lookup"><span data-stu-id="890b6-148">Select **Manage Roles**, and then, in the **Manage User Roles** dialog box, select the **System Administrator** check box to provide system admin rights to the selected application user.</span></span>

        ![システム管理者ロールの割り当て](media/manage-user-roles.png)

    7. <span data-ttu-id="890b6-150">**Dynamics 365 \> 設定 \> セキュリティ**に移動し、**チーム** を選択して、**すべてのチーム** にビューを変更します。</span><span class="sxs-lookup"><span data-stu-id="890b6-150">Go to **Dynamics 365 \> Settings \> Security**, select **Teams**, and then change the view to **All Teams**.</span></span>
    8. <span data-ttu-id="890b6-151">ルートの事業単位/組織を選択して、**ロールの管理** を選択し、**チームロールの管理** ダイアログ ボックスで **システム管理者** チェック ボックスを選択して、必要なシステム管理者権限を割り当てます。</span><span class="sxs-lookup"><span data-stu-id="890b6-151">Select the root business unit/organization, select **Manage Roles**, and then, in the **Manage Team Roles** dialog box, select the **System Administrator** check box to assign the required system admin rights.</span></span>

        ![システム管理者ロールの割り当て](media/assign-system-admin-role.png)

    9. <span data-ttu-id="890b6-153">アプリケーションID **2e49aa60-1bd3-43b6-8ab6-03ada3d9f08b** について前の 5 つの手順を繰り返します。</span><span class="sxs-lookup"><span data-stu-id="890b6-153">Repeat the previous five steps for application ID **2e49aa60-1bd3-43b6-8ab6-03ada3d9f08b**.</span></span>

        ![アプリケーション ID の割り当て](media/assign-application-id.png)

    <span data-ttu-id="890b6-155">**関連する正常性チェックの結果:**</span><span class="sxs-lookup"><span data-stu-id="890b6-155">**Related health check result:**</span></span>

    <span data-ttu-id="890b6-156">*Finance and Operations アプリは Common Data Service に接続できます*</span><span class="sxs-lookup"><span data-stu-id="890b6-156">*The Finance and Operations app can connect to the Common Data Service*</span></span>

    <span data-ttu-id="890b6-157">*二重書き込みを有効にする前に、相互に接続するアプリへのアクセスを許可する必要があります<br> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;ID 00000015-0000-0000-c000-000000000000 のアプリ ユーザーが存在します<br> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;ID 2e49aa60-1bd3-43b6-8ab6-03ada3d9f08b のアプリ ユーザーが存在します*</span><span class="sxs-lookup"><span data-stu-id="890b6-157">*Before you can enable dual-write, you must grant access to the apps to connect to each other<br> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;App user with id 00000015-0000-0000-c000-000000000000 exists<br> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;App user with id 2e49aa60-1bd3-43b6-8ab6-03ada3d9f08b exists*</span></span>

5. <span data-ttu-id="890b6-158">テナントでアプリへの同意をします。</span><span class="sxs-lookup"><span data-stu-id="890b6-158">Provide app consent in the tenant.</span></span>

    <span data-ttu-id="890b6-159">必要なアプリの同意をしてください。</span><span class="sxs-lookup"><span data-stu-id="890b6-159">Make sure that you provide the required app consent.</span></span>

    1. <span data-ttu-id="890b6-160">次のURLを開き、管理者の資格情報を使用してサインインします。</span><span class="sxs-lookup"><span data-stu-id="890b6-160">Open the following URL, and sign in by using your admin credentials.</span></span> <span data-ttu-id="890b6-161">同意を求めるメッセージが表示されます。</span><span class="sxs-lookup"><span data-stu-id="890b6-161">You should be prompted for consent.</span></span>

        [https://login.microsoftonline.com/common/oauth2/authorize?client_id=33976c19-1db5-4c02-810e-c243db79efde&response_type=code&prompt=admin_consent](https://login.microsoftonline.com/common/oauth2/authorize?client_id=33976c19-1db5-4c02-810e-c243db79efde&response_type=code&prompt=admin_consent)

    2. <span data-ttu-id="890b6-162">**受け入れる** を選択します。</span><span class="sxs-lookup"><span data-stu-id="890b6-162">Select **Accept**.</span></span>

        <span data-ttu-id="890b6-163">**承認** を選択することで、テナントにアプリケーション ID **33976c19-1db5-4c02-810e-c243db79efde** を持つアプリのインストールに同意したことになります。</span><span class="sxs-lookup"><span data-stu-id="890b6-163">By selecting **Accept**, you indicate that you're providing consent to install the app that has application ID **33976c19-1db5-4c02-810e-c243db79efde** in your tenant.</span></span> <span data-ttu-id="890b6-164">Common Data Service は、Finance and Operations アプリと通信するためにこのアプリが必要です。</span><span class="sxs-lookup"><span data-stu-id="890b6-164">Common Data Service requires this app to communicate with the Finance and Operations app.</span></span>

    3. <span data-ttu-id="890b6-165">アプリケーション ID **2e49aa60-1bd3-43b6-8ab6-03ada3d9f08b** について前の 2 つの手順を繰り返します。</span><span class="sxs-lookup"><span data-stu-id="890b6-165">Repeat the previous two steps for application ID **2e49aa60-1bd3-43b6-8ab6-03ada3d9f08b**.</span></span>

    <span data-ttu-id="890b6-166">**関連する正常性チェックの結果:**</span><span class="sxs-lookup"><span data-stu-id="890b6-166">**Related health check result:**</span></span>

    <span data-ttu-id="890b6-167">*テナントのアプリ*</span><span class="sxs-lookup"><span data-stu-id="890b6-167">*Apps in tenant*</span></span>

    <span data-ttu-id="890b6-168">*必要な二重書き込みアプリケーションを、テナントにインストールする必要があります。<br> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;アプリ ID: 33976c19-1db5-4c02-810e-c243db79efde<br> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;アプリ ID: 2e49aa60-1bd3-43b6-8ab6-03ada3d9f08b*</span><span class="sxs-lookup"><span data-stu-id="890b6-168">*The required dual-write applications need to be installed in the tenant.<br> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;App ID: 33976c19-1db5-4c02-810e-c243db79efde<br> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;App ID: 2e49aa60-1bd3-43b6-8ab6-03ada3d9f08b*</span></span>

6. <span data-ttu-id="890b6-169">二重書き込みプラグインが有効になっていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="890b6-169">Make sure that the dual-write plug-ins are enabled.</span></span>

    <span data-ttu-id="890b6-170">二重書き込みコア ソリューションのインストール プロセスの一部としてプラグインを有効にする必要があるため、通常この手順は必要ありません。</span><span class="sxs-lookup"><span data-stu-id="890b6-170">This step isn't usually required, because the plug-ins should be enabled as part of the process of installing the dual-write core solution.</span></span> <span data-ttu-id="890b6-171">ただし、正常性チェックが失敗した場合は、次の手順に従って手動で二重書き込みプラグインを有効にします:</span><span class="sxs-lookup"><span data-stu-id="890b6-171">However, if the health check fails, follow these steps to manually enable the dual-write plug-ins:</span></span>

    1. <span data-ttu-id="890b6-172">[Plugin Registration Tool](https://www.nuget.org/packages/Microsoft.CrmSdk.XrmTooling.PluginRegistrationTool) をダウンロードします。</span><span class="sxs-lookup"><span data-stu-id="890b6-172">Download the [Plug-in Registration Tool](https://www.nuget.org/packages/Microsoft.CrmSdk.XrmTooling.PluginRegistrationTool).</span></span>

        <span data-ttu-id="890b6-173">Plugin Registration Tool には、二重書き込みに関連付けられている 2 つのプラグイン アセンブリが必要です: **DualWriteRegistration.Plugins** と **DualWriteRuntime.Plugins**。</span><span class="sxs-lookup"><span data-stu-id="890b6-173">In the Plugin Registration Tool, there should be two plug-in assemblies that are associated with dual-write: **DualWriteRegistration.Plugins** and **DualWriteRuntime.Plugins**.</span></span> <span data-ttu-id="890b6-174">これらのアセンブリには、二重書き込みを使用する前に、順番に有効にする必要があるプラグイン ステップがあります。</span><span class="sxs-lookup"><span data-stu-id="890b6-174">These assemblies have plug-in steps that must be enabled, in order, before dual-write can be used.</span></span> <span data-ttu-id="890b6-175">プラグイン ステップを表示するには、プラグイン アセンブリとそのプラグイン タイプを展開します。</span><span class="sxs-lookup"><span data-stu-id="890b6-175">To view the plug-in steps, expand a plug-in assembly and its plug-in types.</span></span> <span data-ttu-id="890b6-176">二重書き込みプラグイン アセンブリに属するすべてのステップを有効にする必要があります。</span><span class="sxs-lookup"><span data-stu-id="890b6-176">All the steps that belong to the dual-write plug-in assemblies should be enabled.</span></span>

    2. <span data-ttu-id="890b6-177">ステップを有効にするには、ステップを選択したまま (または右クリック) にし、**有効** を選択します。</span><span class="sxs-lookup"><span data-stu-id="890b6-177">To enable a step, select and hold the step (or right-click it), and then select **Enable**.</span></span> <span data-ttu-id="890b6-178">**有効** オプションがなく、**無効** オプションのみの場合、ステップは既に有効になっており、変更する必要はありません。</span><span class="sxs-lookup"><span data-stu-id="890b6-178">If no **Enable** option is available, only a **Disable** option, the step has already been enabled and doesn't have to be changed.</span></span>

        ![Plugin Registration Tool の使用](media/plugin-registration-tool.png)

    > [!NOTE]
    > <span data-ttu-id="890b6-180">二重書き込みプラグイン アセンブリが見つからない場合は、二重書き込みコア ソリューションの最新バージョンをインポートします。</span><span class="sxs-lookup"><span data-stu-id="890b6-180">If the dual-write plug-in assemblies can't be found, import the latest version of the dual-write core solution.</span></span>

    <span data-ttu-id="890b6-181">**関連する正常性チェックの結果:**</span><span class="sxs-lookup"><span data-stu-id="890b6-181">**Related health check result:**</span></span>

    <span data-ttu-id="890b6-182">*二重書き込み登録とランタイム プラグインが有効です*</span><span class="sxs-lookup"><span data-stu-id="890b6-182">*The dual-write registration and runtime plugins are enabled*</span></span>

    <span data-ttu-id="890b6-183">*Common Data Service で CRUD 操作を確実に行うには、二重書き込みプラグインを有効にする必要があります*</span><span class="sxs-lookup"><span data-stu-id="890b6-183">*To ensure listening into CRUD operations on the Common Data Service, the dual-write plugins need to be enabled*</span></span>

7. <span data-ttu-id="890b6-184">見込顧客を現金化 (P2C) するソリューションをインストールします。</span><span class="sxs-lookup"><span data-stu-id="890b6-184">Uninstall the Prospect to Cash (P2C) solution.</span></span>

    <span data-ttu-id="890b6-185">P2C ソリューションは、二重書き込みと同時には機能しません。</span><span class="sxs-lookup"><span data-stu-id="890b6-185">The P2C solution doesn't work concurrently with dual-write.</span></span> <span data-ttu-id="890b6-186">したがって、P2C ソリューションをインストールしないでください。</span><span class="sxs-lookup"><span data-stu-id="890b6-186">Therefore, don't install the P2C solution.</span></span> <span data-ttu-id="890b6-187">既にインストールされている場合は、二重書き込みを有効にする前にアンインストールする必要があります。</span><span class="sxs-lookup"><span data-stu-id="890b6-187">If it's already installed, you must uninstall it before you enable dual-write.</span></span>

8. <span data-ttu-id="890b6-188">サポートされているテナント コンフィギュレーションを指定します。</span><span class="sxs-lookup"><span data-stu-id="890b6-188">Provide the supported tenant configuration.</span></span>

    <span data-ttu-id="890b6-189">Finance and Operations アプリと Common Data Service が同じテナントにインストールされていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="890b6-189">Make sure that the Finance and Operations app and Common Data Service are installed under the same tenant.</span></span> <span data-ttu-id="890b6-190">テナント間シナリオは現在サポートされていません。</span><span class="sxs-lookup"><span data-stu-id="890b6-190">Cross-tenant scenarios aren't currently supported.</span></span>


## <a name="next-steps"></a><span data-ttu-id="890b6-191">次のステップ</span><span class="sxs-lookup"><span data-stu-id="890b6-191">Next steps</span></span>

[<span data-ttu-id="890b6-192">二重書き込みウィザードを使用して環境をリンクする</span><span class="sxs-lookup"><span data-stu-id="890b6-192">Use the dual-write wizard to link your environments</span></span>](link-your-environment.md)
