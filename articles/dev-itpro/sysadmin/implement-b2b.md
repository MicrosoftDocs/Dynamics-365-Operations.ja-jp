---
title: "Azure Active Directory への企業間 (B2B) のユーザーをエクスポートします。"
description: "このトピックでは、Microsoft Dynamics 365 for Finance and Operations で企業間のトランザクション機能を実装する方法について説明します。"
author: sarvanisathish
manager: AnnBe
ms.date: 07/10/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
ms.search.form: B2BInvitationConfiguration
audience: developer, IT Pro
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.custom: 
ms.assetid: 
ms.search.region: Global
ms.author: sarvanis
ms.search.validFrom: 2017-10-31
ms.dyn365.ops.version: Platform update 12
ms.translationtype: HT
ms.sourcegitcommit: 55e5d957de6ef5b24c0cda59738c0755cac810b1
ms.openlocfilehash: b20839a6847e4a23e82e4a5149b57fdcdfcdb424
ms.contentlocale: ja-jp
ms.lasthandoff: 10/13/2018

---

# <a name="export-business-to-business-b2b-users-to-azure-active-directory"></a><span data-ttu-id="65028-103">Azure Active Directory への企業間 (B2B) のユーザーをエクスポートします。</span><span class="sxs-lookup"><span data-stu-id="65028-103">Export business-to-business (B2B) users to Azure Active Directory</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="65028-104">企業間 (B2B) ユーザーを Azure Active Directory (Azure AD) に自動的にエクスポートすることができます。</span><span class="sxs-lookup"><span data-stu-id="65028-104">You can automatically export business-to-business (B2B) users to Azure Active Directory (Azure AD).</span></span> 

<span data-ttu-id="65028-105">過去には、B2B ユーザーは .csv ファイルに手動でエクスポートされていました。</span><span class="sxs-lookup"><span data-stu-id="65028-105">In the past, B2B users were exported manually to a .csv file.</span></span> <span data-ttu-id="65028-106">その後、Azure AD テナントの管理者は、このファイルを使用して Azure ポータルを使用してユーザーを Azure AD に手動で追加する必要があります。</span><span class="sxs-lookup"><span data-stu-id="65028-106">Then the Azure AD tenant administrator had to use this file to manually add the users to Azure AD using the Azure portal.</span></span> 

<span data-ttu-id="65028-107">自動エクスポート機能を有効にするには、ワンタイム設定と構成プロセスを完了する必要があります。</span><span class="sxs-lookup"><span data-stu-id="65028-107">To enable the automatic export feature, a one-time setup and configuration process must be completed.</span></span> <span data-ttu-id="65028-108">このプロセスが完了したら、**Azure AD B2B ユーザーのプロビジョニング** ワークフロー タスクを使用して、Azure AD に B2B ユーザーを自動的にエクスポートできます。</span><span class="sxs-lookup"><span data-stu-id="65028-108">When the process is completed, you can use the **Provision Azure AD B2B user** workflow task to automatically export B2B users to Azure AD.</span></span>

<span data-ttu-id="65028-109">1回限りの設定とコンフィギュレーションでは、次のことが必要になります。</span><span class="sxs-lookup"><span data-stu-id="65028-109">The one-time set up and configuration means that you'll need to:</span></span> 
1. <span data-ttu-id="65028-110">Azure AD で B2B 招待サービス アプリケーションを設定します。</span><span class="sxs-lookup"><span data-stu-id="65028-110">Set up a B2B invitation service application in Azure AD.</span></span>
2. <span data-ttu-id="65028-111">Finance and Operations で B2B 招待サービスの設定のコンフィギュレーションをします。</span><span class="sxs-lookup"><span data-stu-id="65028-111">Configure the B2B invitation service settings in Finance and Operations.</span></span>

### <a name="set-up-a-b2b-invitation-service-application-in-azure-ad"></a><span data-ttu-id="65028-112">Azure AD で B2B 招待サービス アプリケーションを設定</span><span class="sxs-lookup"><span data-stu-id="65028-112">Set up a B2B invitation service application in Azure AD</span></span>
<span data-ttu-id="65028-113">Azure AD テナントのテナント管理者は、以下の手順を完了する必要があります。</span><span class="sxs-lookup"><span data-stu-id="65028-113">The tenant administrator of your Azure AD tenant will need to complete the following steps.</span></span>

1. <span data-ttu-id="65028-114">[Azure ポータル](https://portal.azure.com)にテナント管理者としてログオンします。</span><span class="sxs-lookup"><span data-stu-id="65028-114">Log on to the [Azure portal](https://portal.azure.com) as the tenant administrator.</span></span> 

2. <span data-ttu-id="65028-115">**Azure Active Directory** > **プロパティ**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="65028-115">Click **Azure Active Directory** > **Properties**.</span></span>

3. <span data-ttu-id="65028-116">**ディレクトリ ID** (これはテナント ID) をコピーし、保存します。</span><span class="sxs-lookup"><span data-stu-id="65028-116">Copy the **Directory ID** (this is the tenant ID) and save it.</span></span> <span data-ttu-id="65028-117">これは後で必要になります。</span><span class="sxs-lookup"><span data-stu-id="65028-117">You will need this later.</span></span>

4. <span data-ttu-id="65028-118">**アプリの登録** > **新しいアプリケーションの登録**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="65028-118">Click **App registrations** > **New application registration**.</span></span>

5. <span data-ttu-id="65028-119">以下の情報を入力し、**作成**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="65028-119">Enter the following information, and then click **Create**.</span></span>
    1. <span data-ttu-id="65028-120">**名前**フィールドに、アプリケーションの名前を入力します。</span><span class="sxs-lookup"><span data-stu-id="65028-120">In the **Name** field, enter the name of the application.</span></span> <span data-ttu-id="65028-121">例: **B2B 管理者アプリケーション**。</span><span class="sxs-lookup"><span data-stu-id="65028-121">For example: **B2B admin application**.</span></span>
    2. <span data-ttu-id="65028-122">**アプリケーション タイプ** フィールドで、**Web アプリ/API** を選択します。</span><span class="sxs-lookup"><span data-stu-id="65028-122">In the **Application type** field, select **Web app /API**.</span></span>
    3. <span data-ttu-id="65028-123">**サインオン URL** フィールドに、Finance and Operations の URL を入力します。</span><span class="sxs-lookup"><span data-stu-id="65028-123">In the **Sign-on URL** field, enter the URL for Finance and Operations.</span></span>
  
6. <span data-ttu-id="65028-124">**アプリの登録**タブをクリックし、新しく作成したアプリケーションをクリックし、**アプリケーション ID** をコピーして保存します。</span><span class="sxs-lookup"><span data-stu-id="65028-124">Click the **App registrations** tab, click the newly created application, copy the **Application ID**, and save it.</span></span> <span data-ttu-id="65028-125">これは後で必要になります。</span><span class="sxs-lookup"><span data-stu-id="65028-125">You will need this later.</span></span>

7. <span data-ttu-id="65028-126">**すべての設定** > **必要なアクセス許可** > **追加**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="65028-126">Click **All settings** > **Required permissions** > **Add**.</span></span>

8. <span data-ttu-id="65028-127">**API アクセスの追加**ウィンドウで、次の操作を行います。</span><span class="sxs-lookup"><span data-stu-id="65028-127">In the **Add API access** pane, do the following:</span></span>
    1. <span data-ttu-id="65028-128">**API を選択**タブをクリックします。**Microsoft Graph** をクリックし、**選択**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="65028-128">Click the **Select an API** tab. Click **Microsoft Graph**, and then click **Select**.</span></span>
    
    2. <span data-ttu-id="65028-129">**アクセス許可の選択**タブで、以下の**アプリケーションのアクセス許可**を選択します。</span><span class="sxs-lookup"><span data-stu-id="65028-129">In the **Select permissions** tab, select the following **application permissions**:</span></span>
         - <span data-ttu-id="65028-130">**ゲスト ユーザーを組織へ招待します**</span><span class="sxs-lookup"><span data-stu-id="65028-130">**Invite guest users to the organization**</span></span>
         - <span data-ttu-id="65028-131">**ディレクトリ データの読み取りと書き込み**</span><span class="sxs-lookup"><span data-stu-id="65028-131">**Read and write directory data**</span></span>
         - <span data-ttu-id="65028-132">**すべてのユーザーの完全なプロファイルの読み取りと書き込み**</span><span class="sxs-lookup"><span data-stu-id="65028-132">**Read and write all users' full profiles**</span></span>
    
    3. <span data-ttu-id="65028-133">次の委任されたアクセス許可を選択します。</span><span class="sxs-lookup"><span data-stu-id="65028-133">Select the following delegated permission:</span></span>
         - <span data-ttu-id="65028-134">**サインインし、ユーザー プロファイルを読み取ります**</span><span class="sxs-lookup"><span data-stu-id="65028-134">**Sign in and read user profile**</span></span>
     
    4. <span data-ttu-id="65028-135">**選択**および**完了**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="65028-135">Click **Select** and **Done**.</span></span>
    
9. <span data-ttu-id="65028-136">**必要なアクセス許可**ブレードで、**アクセス許可の付与**をクリックしてから、**はい**をクリックしてアクセス許可を割り当てます。</span><span class="sxs-lookup"><span data-stu-id="65028-136">In the **Required permissions** blade, click **Grant Permissions**, and then click **Yes** to assign the permissions.</span></span>

10. <span data-ttu-id="65028-137">**すべての設定** > **キー**をクリックし、次の操作を行います。</span><span class="sxs-lookup"><span data-stu-id="65028-137">Click **All settings** > **Keys**, and then do the following:</span></span> 
    1. <span data-ttu-id="65028-138">**説明**フィールドにキーの名前を入力します。</span><span class="sxs-lookup"><span data-stu-id="65028-138">Enter a name of the key in the **Description** field.</span></span>
    2. <span data-ttu-id="65028-139">**期限切れ日時** フィールドで有効期間を設定します。</span><span class="sxs-lookup"><span data-stu-id="65028-139">Set the expiration duration in the **Expires** field.</span></span>
  
11. <span data-ttu-id="65028-140">**保存** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="65028-140">Click **Save**.</span></span> <span data-ttu-id="65028-141">キーを保存すると、**値** が表示されます。</span><span class="sxs-lookup"><span data-stu-id="65028-141">Saving the key will display the **Value**.</span></span> 

    > [!WARNING]
    > <span data-ttu-id="65028-142">キーを保存した後**値**キーを必ずコピーしてください。</span><span class="sxs-lookup"><span data-stu-id="65028-142">Be sure to copy the key **Value** after saving the key.</span></span> <span data-ttu-id="65028-143">この値はブレードを離れるときには使用できません。</span><span class="sxs-lookup"><span data-stu-id="65028-143">This value will not be available when you leave the blade.</span></span>

### <a name="configure-the-b2b-invitation-service-settings-in-finance-and-operations"></a><span data-ttu-id="65028-144">Finance and Operations で B2B 招待サービスの設定のコンフィギュレーション</span><span class="sxs-lookup"><span data-stu-id="65028-144">Configure the B2B invitation service settings in Finance and Operations</span></span>

1. <span data-ttu-id="65028-145">Dynamics 365 for Finance and Operations に管理者としてサインインします。</span><span class="sxs-lookup"><span data-stu-id="65028-145">Sign in to Dynamics 365 for Finance and Operations as administrator.</span></span>

2. <span data-ttu-id="65028-146">**B2B 招待状のコンフィギュレーション** ページに移動して、**編集**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="65028-146">Navigate to the **B2B Invitation Configuration** page, and click **Edit**.</span></span>

3. <span data-ttu-id="65028-147">**有効** を選択します。</span><span class="sxs-lookup"><span data-stu-id="65028-147">Select **Enabled**.</span></span>

4. <span data-ttu-id="65028-148">**テナント ID** が**ディレクトリ ID** (前の手順の手順 3 でメモしたもの) と同じであることを確認します。</span><span class="sxs-lookup"><span data-stu-id="65028-148">Verify that the **Tenant ID** is the same as the **Directory ID** (which you noted in step 3 of the previous procedure).</span></span>

5. <span data-ttu-id="65028-149">**クライアント ID** フィールドに、**アプリケーション ID** (前の手順の手順 6 でメモしたもの) を入力します。</span><span class="sxs-lookup"><span data-stu-id="65028-149">In the **Client ID** field, enter the **Application ID** (which you noted in step 6 of the previous procedure).</span></span>

6. <span data-ttu-id="65028-150">上記手順からコピーされたキー**値**を、**アプリケーション キー**フィールドに入力します。</span><span class="sxs-lookup"><span data-stu-id="65028-150">Enter the key **Value**, copied from the above procedure, into the **Application Key** field.</span></span>

7. <span data-ttu-id="65028-151">設定を**保存します**。</span><span class="sxs-lookup"><span data-stu-id="65028-151">**Save** the settings.</span></span>

<span data-ttu-id="65028-152">これで、ワークフローで**Azure AD B2B ユーザーのプロビジョニング** ワークフロー タスクの使用を開始して、Azure AD に B2B ユーザーを自動的にエクスポートできます。</span><span class="sxs-lookup"><span data-stu-id="65028-152">Now you can start using the **Provision Azure AD B2B user** workflow task in your workflows to automatically export B2B users to Azure AD.</span></span>

