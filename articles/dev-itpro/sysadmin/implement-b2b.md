---
title: "Dynamics 365 for Finance and Operations の B2B機能"
description: "このトピックでは、Microsoft Dynamics 365 for Finance and Operations で企業間のトランザクション機能を実装する方法について説明します。"
author: sarvanisathish
manager: AnnBe
ms.date: 10/11/2017
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
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: ab204395214768c7846e65f11f072ea47067f45b
ms.contentlocale: ja-jp
ms.lasthandoff: 05/08/2018

---

# <a name="export-b2b-users-to-azure-ad"></a><span data-ttu-id="4785f-103">B2B ユーザーの Azure AD へのエクスポート</span><span class="sxs-lookup"><span data-stu-id="4785f-103">Export B2B users to Azure AD</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="4785f-104">企業間 (B2B) ユーザーを Azure Active Directory (Azure AD) に自動的にエクスポートすることができます。</span><span class="sxs-lookup"><span data-stu-id="4785f-104">You can automatically export business-to-business (B2B) users to Azure Active Directory (Azure AD).</span></span> 

<span data-ttu-id="4785f-105">過去には、B2B ユーザーは .csv ファイルに手動でエクスポートされていました。</span><span class="sxs-lookup"><span data-stu-id="4785f-105">In the past, B2B users were exported manually to a .csv file.</span></span> <span data-ttu-id="4785f-106">その後、Azure AD テナントの管理者は、このファイルを使用して Azure ポータルを使用してユーザーを Azure AD に手動で追加する必要があります。</span><span class="sxs-lookup"><span data-stu-id="4785f-106">Then the Azure AD tenant administrator had to use this file to manually add the users to Azure AD using the Azure portal.</span></span> 

<span data-ttu-id="4785f-107">自動エクスポート機能を有効にするには、ワンタイム設定と構成プロセスを完了する必要があります。</span><span class="sxs-lookup"><span data-stu-id="4785f-107">To enable the automatic export feature, a one-time setup and configuration process must be completed.</span></span> <span data-ttu-id="4785f-108">このプロセスが完了したら、**新しいユーザーのプロビジョニング** ワークフロー タスクを使用して、Azure AD に B2B ユーザーを自動的にエクスポートできます。</span><span class="sxs-lookup"><span data-stu-id="4785f-108">When the process is completed, you can use the **Provision new user** workflow task to automatically export B2B users to Azure AD.</span></span>

<span data-ttu-id="4785f-109">1回限りの設定とコンフィギュレーションでは、次のことが必要になります。</span><span class="sxs-lookup"><span data-stu-id="4785f-109">The one-time set up and configuration means that you'll need to:</span></span> 
1. <span data-ttu-id="4785f-110">Azure AD で B2B 招待サービス アプリケーションを設定します。</span><span class="sxs-lookup"><span data-stu-id="4785f-110">Set up a B2B invitation service application in Azure AD.</span></span>
2. <span data-ttu-id="4785f-111">Finance and Operations で B2B 招待サービスの設定のコンフィギュレーションをします。</span><span class="sxs-lookup"><span data-stu-id="4785f-111">Configure the B2B invitation service settings in Finance and Operations.</span></span>

### <a name="set-up-a-b2b-invitation-service-application-in-azure-ad"></a><span data-ttu-id="4785f-112">Azure AD で B2B 招待サービス アプリケーションを設定</span><span class="sxs-lookup"><span data-stu-id="4785f-112">Set up a B2B invitation service application in Azure AD</span></span>
<span data-ttu-id="4785f-113">Azure AD テナントのテナント管理者は、以下の手順を完了する必要があります。</span><span class="sxs-lookup"><span data-stu-id="4785f-113">The tenant administrator of your Azure AD tenant will need to complete the following steps.</span></span>

1. <span data-ttu-id="4785f-114">[Azure ポータル](https://portal.azure.com)にテナント管理者としてログオンします。</span><span class="sxs-lookup"><span data-stu-id="4785f-114">Log on to the [Azure portal](https://portal.azure.com) as the tenant administrator.</span></span> 

2. <span data-ttu-id="4785f-115">**Azure Active Directory** > **プロパティ**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="4785f-115">Click **Azure Active Directory** > **Properties**.</span></span>

3. <span data-ttu-id="4785f-116">**ディレクトリ ID** (これはテナント ID) をコピーし、保存します。</span><span class="sxs-lookup"><span data-stu-id="4785f-116">Copy the **Directory ID** (this is the tenant ID) and save it.</span></span> <span data-ttu-id="4785f-117">これは後で必要になります。</span><span class="sxs-lookup"><span data-stu-id="4785f-117">You will need this later.</span></span>

4. <span data-ttu-id="4785f-118">**アプリの登録** > **新しいアプリケーションの登録**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="4785f-118">Click **App registrations** > **New application registration**.</span></span>

5. <span data-ttu-id="4785f-119">以下の情報を入力し、**作成**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="4785f-119">Enter the following information, and then click **Create**.</span></span>
    1. <span data-ttu-id="4785f-120">**名前**フィールドに、アプリケーションの名前を入力します。</span><span class="sxs-lookup"><span data-stu-id="4785f-120">In the **Name** field, enter the name of the application.</span></span> <span data-ttu-id="4785f-121">例: **B2B 管理者アプリケーション**。</span><span class="sxs-lookup"><span data-stu-id="4785f-121">For example: **B2B admin application**.</span></span>
    2. <span data-ttu-id="4785f-122">**アプリケーション タイプ** フィールドで、**Web アプリ/API** を選択します。</span><span class="sxs-lookup"><span data-stu-id="4785f-122">In the **Application type** field, select **Web app /API**.</span></span>
    3. <span data-ttu-id="4785f-123">**サインオン URL** フィールドに、Finance and Operations の URL を入力します。</span><span class="sxs-lookup"><span data-stu-id="4785f-123">In the **Sign-on URL** field, enter the URL for Finance and Operations.</span></span>
  
6. <span data-ttu-id="4785f-124">**アプリの登録**タブをクリックし、新しく作成したアプリケーションをクリックし、**アプリケーション ID** をコピーして保存します。</span><span class="sxs-lookup"><span data-stu-id="4785f-124">Click the **App registrations** tab, click the newly created application, copy the **Application ID**, and save it.</span></span> <span data-ttu-id="4785f-125">これは後で必要になります。</span><span class="sxs-lookup"><span data-stu-id="4785f-125">You will need this later.</span></span>

7. <span data-ttu-id="4785f-126">**すべての設定** > **必要なアクセス許可** > **追加**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="4785f-126">Click **All settings** > **Required permissions** > **Add**.</span></span>

8. <span data-ttu-id="4785f-127">**API アクセスの追加**ウィンドウで、次の操作を行います。</span><span class="sxs-lookup"><span data-stu-id="4785f-127">In the **Add API access** pane, do the following:</span></span>
    1. <span data-ttu-id="4785f-128">**API を選択**タブをクリックします。**Microsoft Graph** をクリックし、**選択**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="4785f-128">Click the **Select an API** tab. Click **Microsoft Graph**, and then click **Select**.</span></span>
    
    2. <span data-ttu-id="4785f-129">**アクセス許可の選択**タブで、次のアプリケーションのアクセス許可を選択します。</span><span class="sxs-lookup"><span data-stu-id="4785f-129">In the **Select permissions** tab, select the following application permissions:</span></span>
         - <span data-ttu-id="4785f-130">**すべてのユーザーの完全なプロファイルの読み取りと書き込み**</span><span class="sxs-lookup"><span data-stu-id="4785f-130">**Read and write all users' full profiles**</span></span>
         - <span data-ttu-id="4785f-131">**ディレクトリ データの読み取りと書き込み**</span><span class="sxs-lookup"><span data-stu-id="4785f-131">**Read and write directory data**</span></span>
    
    3. <span data-ttu-id="4785f-132">次の委任されたアクセス許可を選択します。</span><span class="sxs-lookup"><span data-stu-id="4785f-132">Select the following delegated permission:</span></span>
         - <span data-ttu-id="4785f-133">**サインインし、ユーザー プロファイルを読み取ります**</span><span class="sxs-lookup"><span data-stu-id="4785f-133">**Sign in and read user profile**</span></span>
     
    4. <span data-ttu-id="4785f-134">**選択**および**完了**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="4785f-134">Click **Select** and **Done**.</span></span>
    
9. <span data-ttu-id="4785f-135">**必要なアクセス許可**ブレードで、**アクセス許可の付与**をクリックしてから、**はい**をクリックしてアクセス許可を割り当てます。</span><span class="sxs-lookup"><span data-stu-id="4785f-135">In the **Required permissions** blade, click **Grant Permissions**, and then click **Yes** to assign the permissions.</span></span>

10. <span data-ttu-id="4785f-136">**すべての設定** > **キー**をクリックし、次の操作を行います。</span><span class="sxs-lookup"><span data-stu-id="4785f-136">Click **All settings** > **Keys**, and then do the following:</span></span> 
    1. <span data-ttu-id="4785f-137">**説明**フィールドにキーの名前を入力します。</span><span class="sxs-lookup"><span data-stu-id="4785f-137">Enter a name of the key in the **Description** field.</span></span>
    2. <span data-ttu-id="4785f-138">**期限切れ日時** フィールドで有効期間を設定します。</span><span class="sxs-lookup"><span data-stu-id="4785f-138">Set the expiration duration in the **Expires** field.</span></span>
  
11. <span data-ttu-id="4785f-139">**保存** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="4785f-139">Click **Save**.</span></span> <span data-ttu-id="4785f-140">キーを保存すると、**値** が表示されます。</span><span class="sxs-lookup"><span data-stu-id="4785f-140">Saving the key will display the **Value**.</span></span> 

    > [!WARNING]
    > <span data-ttu-id="4785f-141">キーを保存した後**値**キーを必ずコピーしてください。</span><span class="sxs-lookup"><span data-stu-id="4785f-141">Be sure to copy the key **Value** after saving the key.</span></span> <span data-ttu-id="4785f-142">この値はブレードを離れるときには使用できません。</span><span class="sxs-lookup"><span data-stu-id="4785f-142">This value will not be available when you leave the blade.</span></span>

### <a name="configure-the-b2b-invitation-service-settings-in-finance-and-operations"></a><span data-ttu-id="4785f-143">Finance and Operations で B2B 招待サービスの設定のコンフィギュレーション</span><span class="sxs-lookup"><span data-stu-id="4785f-143">Configure the B2B invitation service settings in Finance and Operations</span></span>

1. <span data-ttu-id="4785f-144">Dynamics 365 for Finance and Operations に管理者としてサインインします。</span><span class="sxs-lookup"><span data-stu-id="4785f-144">Sign in to Dynamics 365 for Finance and Operations as administrator.</span></span>

2. <span data-ttu-id="4785f-145">**B2B 招待状のコンフィギュレーション** ページに移動して、**編集**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="4785f-145">Navigate to the **B2B Invitation Configuration** page, and click **Edit**.</span></span>

3. <span data-ttu-id="4785f-146">**有効** を選択します。</span><span class="sxs-lookup"><span data-stu-id="4785f-146">Select **Enabled**.</span></span>

4. <span data-ttu-id="4785f-147">**テナント ID** が**ディレクトリ ID** (前の手順の手順 3 でメモしたもの) と同じであることを確認します。</span><span class="sxs-lookup"><span data-stu-id="4785f-147">Verify that the **Tenant ID** is the same as the **Directory ID** (which you noted in step 3 of the previous procedure).</span></span>

5. <span data-ttu-id="4785f-148">**クライアント ID** フィールドに、**アプリケーション ID** (前の手順の手順 6 でメモしたもの) を入力します。</span><span class="sxs-lookup"><span data-stu-id="4785f-148">In the **Client ID** field, enter the **Application ID** (which you noted in step 6 of the previous procedure).</span></span>

6. <span data-ttu-id="4785f-149">上記手順からコピーされたキー**値**を、**アプリケーション キー**フィールドに入力します。</span><span class="sxs-lookup"><span data-stu-id="4785f-149">Enter the key **Value**, copied from the above procedure, into the **Application Key** field.</span></span>

7. <span data-ttu-id="4785f-150">設定を**保存します**。</span><span class="sxs-lookup"><span data-stu-id="4785f-150">**Save** the settings.</span></span>

<span data-ttu-id="4785f-151">これで、ワークフローで**新しいユーザーのプロビジョニング** ワークフロー タスクの使用を開始して、Azure AD に B2B ユーザーを自動的にエクスポートできます。</span><span class="sxs-lookup"><span data-stu-id="4785f-151">Now you can start using the **Provision new users** workflow task in your workflows to automatically export B2B users to Azure AD.</span></span>

