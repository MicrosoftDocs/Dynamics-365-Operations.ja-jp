---
title: LinkedIn タレント ハブとの統合
description: このトピックでは、Microsoft Dynamics 365 Human Resources と LinkedIn タレント ハブ間の統合を設定する方法について説明します。
author: jaredha
manager: tfehr
ms.date: 10/20/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-10-20
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: e82b79858060f31a6310cc5abdb2faf87db2d6c2
ms.sourcegitcommit: 765056b5dc1d0a8c27e56ff2cbd310ad3349ff09
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/20/2020
ms.locfileid: "4056100"
---
# <a name="integrate-with-linkedin-talent-hub"></a><span data-ttu-id="eba6a-103">LinkedIn タレント ハブとの統合</span><span class="sxs-lookup"><span data-stu-id="eba6a-103">Integrate with LinkedIn Talent Hub</span></span>

[!include [banner](includes/preview-feature.md)]

<span data-ttu-id="eba6a-104">[LinkedIn タレント ハブ](https://business.linkedin.com/talent-solutions/talent-hub) は採用管理システム (ATS) のプラットフォームです。</span><span class="sxs-lookup"><span data-stu-id="eba6a-104">[LinkedIn Talent Hub](https://business.linkedin.com/talent-solutions/talent-hub) is an applicant tracking system (ATS) platform.</span></span> <span data-ttu-id="eba6a-105">これにより、従業員の調達、管理、雇用をすべて 1 か所で行うことができます。</span><span class="sxs-lookup"><span data-stu-id="eba6a-105">It lets you source, manage, and hire employees all in one place.</span></span> <span data-ttu-id="eba6a-106">Microsoft Dynamics 365 Human Resources を LinkedIn タレント ハブと統合することにより、職位に採用された応募者の従業員レコードを Human Resources で簡単に作成することができます。</span><span class="sxs-lookup"><span data-stu-id="eba6a-106">By integrating Microsoft Dynamics 365 Human Resources with LinkedIn Talent Hub, you can easily create employee records in Human Resources for applicants who have been hired for a position.</span></span>

## <a name="setup"></a><span data-ttu-id="eba6a-107">段取り</span><span class="sxs-lookup"><span data-stu-id="eba6a-107">Setup</span></span>

<span data-ttu-id="eba6a-108">LinkedIn タレント ハブとの統合を有効にするには、システム管理者が設定作業を完了しておく必要があります。</span><span class="sxs-lookup"><span data-stu-id="eba6a-108">A system administrator must complete setup tasks to enable integration with LinkedIn Talent Hub.</span></span> <span data-ttu-id="eba6a-109">まず、Power Apps 環境でユーザーおよびセキュリティ ロールを設定して、データを Human Resources に書き込むための適切なアクセス許可を LinkedIn タレント ハブに付与する必要があります。</span><span class="sxs-lookup"><span data-stu-id="eba6a-109">First, in the Power Apps environment, you must set up a user and security role to grant LinkedIn Talent Hub the appropriate permissions to write data into Human Resources.</span></span>

### <a name="link-your-environment-to-linkedin-talent-hub"></a><span data-ttu-id="eba6a-110">環境を LinkedIn タレント ハブにリンク</span><span class="sxs-lookup"><span data-stu-id="eba6a-110">Link your environment to LinkedIn Talent Hub</span></span>

1. <span data-ttu-id="eba6a-111">[LinkedIn タレント ハブ](https://business.linkedin.com/talent-solutions/talent-hub) を開きます。</span><span class="sxs-lookup"><span data-stu-id="eba6a-111">Open [LinkedIn Talent Hub](https://business.linkedin.com/talent-solutions/talent-hub).</span></span>

2. <span data-ttu-id="eba6a-112">ユーザー ドロップダウン メニューで、 **製品設定** を選択します。</span><span class="sxs-lookup"><span data-stu-id="eba6a-112">On the user drop-down menu, select **Product Settings**.</span></span>

3. <span data-ttu-id="eba6a-113">左のナビゲーション ペインにある **詳細** セクションで、 **統合** を選択します。</span><span class="sxs-lookup"><span data-stu-id="eba6a-113">In the left navigation pane, in the **Advanced** section, select **Integrations**.</span></span>

4. <span data-ttu-id="eba6a-114">Microsoft Dynamics 365 Human Resources の統合に対して **承認** を選択します。</span><span class="sxs-lookup"><span data-stu-id="eba6a-114">Select **Authorize** for the Microsoft Dynamics 365 Human Resources integration.</span></span>

5. <span data-ttu-id="eba6a-115">**Dynamics 365 Human Resources** ページで、LinkedIn タレント ハブをリンクする環境を選択し、 **リンク** を選択します。</span><span class="sxs-lookup"><span data-stu-id="eba6a-115">On the **Dynamics 365 Human Resources** page, select the environment to link LinkedIn Talent Hub to, and then select **Link**.</span></span>

    ![LinkedIn タレント ハブのオンボード](./media/hr-admin-integration-talent-hub-onboarding.jpg)

    > [!NOTE]
    > <span data-ttu-id="eba6a-117">ユーザー アカウントに Human Resources 環境と関連する Power Apps 環境の両方への管理者アクセス権がある環境にのみリンクできます。</span><span class="sxs-lookup"><span data-stu-id="eba6a-117">You can link only to environments where your user account has administrator access to both the Human Resources environment and the associated Power Apps environment.</span></span> <span data-ttu-id="eba6a-118">Human Resources リンク ページに環境が表示されない場合は、テナントに Human Resources 環境のライセンスがあることと、リンク ページにサインインしたユーザーに Human Resources 環境と Power Apps 環境の両方に対する管理者権限があることを確認してください。</span><span class="sxs-lookup"><span data-stu-id="eba6a-118">If no environments are listed on the Human Resources link page, make sure that you have licensed Human Resources environments on the tenant, and that the user that you signed in to the link page as has administrator permissions to both the Human Resources environment and the Power Apps environment.</span></span>

### <a name="create-a-power-apps-security-role"></a><span data-ttu-id="eba6a-119">Power Apps セキュリティ ロールを作成する</span><span class="sxs-lookup"><span data-stu-id="eba6a-119">Create a Power Apps security role</span></span>

1. <span data-ttu-id="eba6a-120">[Power Platform 管理センター](https://admin.powerplatform.microsoft.com)を開きます。</span><span class="sxs-lookup"><span data-stu-id="eba6a-120">Open the [Power Platform admin center](https://admin.powerplatform.microsoft.com).</span></span>

2. <span data-ttu-id="eba6a-121">**環境** の一覧で、LinkedIn タレント ハブのインスタンスをリンクする Human Resources 環境に関連付けられている環境を選択します。</span><span class="sxs-lookup"><span data-stu-id="eba6a-121">In the **Environments** list, select the environment that is associated with the Human Resources environment that you want to link your instance of LinkedIn Talent Hub to.</span></span>

3. <span data-ttu-id="eba6a-122">**設定** を選択します。</span><span class="sxs-lookup"><span data-stu-id="eba6a-122">Select **Settings**.</span></span>

4. <span data-ttu-id="eba6a-123">**ユーザー + アクセス許可** ノードを展開し、 **セキュリティ ロール** を選択します。</span><span class="sxs-lookup"><span data-stu-id="eba6a-123">Expand the **Users + Permissions** node, and select **Security Roles**.</span></span>

5. <span data-ttu-id="eba6a-124">**セキュリティ ロール** ページのツールバーで、 **新しいロール** を選択します。</span><span class="sxs-lookup"><span data-stu-id="eba6a-124">On the **Security Roles** page, on the toolbar, select **New role**.</span></span>

6. <span data-ttu-id="eba6a-125">**詳細** タブで、 **LinkedIn タレント ハブ HRIS の統合** など、ロールの名前を入力します。</span><span class="sxs-lookup"><span data-stu-id="eba6a-125">On the **Details** tab, enter a name for the role, such as **LinkedIn Talent Hub HRIS Integration**.</span></span>

7. <span data-ttu-id="eba6a-126">**カスタマイズ** タブで、次のエンティティに対する組織レベルの **読み取り** アクセス許可を選択します:</span><span class="sxs-lookup"><span data-stu-id="eba6a-126">On the **Customization** tab, select organization-level **Read** permission for the following entities:</span></span>

    - <span data-ttu-id="eba6a-127">エンティティ</span><span class="sxs-lookup"><span data-stu-id="eba6a-127">Entity</span></span>
    - <span data-ttu-id="eba6a-128">フィールド</span><span class="sxs-lookup"><span data-stu-id="eba6a-128">Field</span></span>
    - <span data-ttu-id="eba6a-129">続柄</span><span class="sxs-lookup"><span data-stu-id="eba6a-129">Relationship</span></span>

8. <span data-ttu-id="eba6a-130">セキュリティ ロールを保存して閉じます。</span><span class="sxs-lookup"><span data-stu-id="eba6a-130">Save and close the security role.</span></span>

### <a name="create-a-power-apps-application-user"></a><span data-ttu-id="eba6a-131">Power Apps アプリケーション ユーザーの作成</span><span class="sxs-lookup"><span data-stu-id="eba6a-131">Create a Power Apps application user</span></span>

<span data-ttu-id="eba6a-132">LinkedIn タレント ハブ アダプターに対してアプリケーション ユーザーを作成し、Power Apps 環境に候補者レコードを書き込むアクセス許可をアダプターに付与する必要があります。</span><span class="sxs-lookup"><span data-stu-id="eba6a-132">An application user must be created for the LinkedIn Talent Hub adapter to grant permissions to the adapter to write candidate records into the Power Apps environment.</span></span>

1. <span data-ttu-id="eba6a-133">[Power Platform 管理センター](https://admin.powerplatform.microsoft.com)を開きます。</span><span class="sxs-lookup"><span data-stu-id="eba6a-133">Open the [Power Platform admin center](https://admin.powerplatform.microsoft.com).</span></span>

2. <span data-ttu-id="eba6a-134">**環境** の一覧で、LinkedIn タレント ハブのインスタンスをリンクする Human Resources 環境に関連付けられている環境を選択します。</span><span class="sxs-lookup"><span data-stu-id="eba6a-134">In the **Environments** list, select the environment that is associated with the Human Resources environment that you want to link your instance of LinkedIn Talent Hub to.</span></span>

3. <span data-ttu-id="eba6a-135">**設定** を選択します。</span><span class="sxs-lookup"><span data-stu-id="eba6a-135">Select **Settings**.</span></span>

4. <span data-ttu-id="eba6a-136">**ユーザー + アクセス許可** ノードを展開し、 **ユーザー** を選択します。</span><span class="sxs-lookup"><span data-stu-id="eba6a-136">Expand the **Users + Permissions** node, and select **Users**.</span></span>

5. <span data-ttu-id="eba6a-137">**Dynamics 365 でユーザーの管理** を選択します。</span><span class="sxs-lookup"><span data-stu-id="eba6a-137">Select **Manage users in Dynamics 365**.</span></span>

6. <span data-ttu-id="eba6a-138">一覧上にあるドロップダウン メニューを使用して、ビューを既定の **有効なユーザー** ビューから **アプリケーション ユーザー** に変更します。</span><span class="sxs-lookup"><span data-stu-id="eba6a-138">Use the drop-down menu above the list to change the view from the default **Enabled Users** view to **Application Users**.</span></span>

    ![アプリケーション ユーザー ビュー](./media/hr-admin-integration-power-apps-application-users.jpg)

7. <span data-ttu-id="eba6a-140">ツール バーの **新規** を選択します。</span><span class="sxs-lookup"><span data-stu-id="eba6a-140">On the toolbar, select **New**.</span></span>

8. <span data-ttu-id="eba6a-141">**新規ユーザー** ページで、次の手順に従います:</span><span class="sxs-lookup"><span data-stu-id="eba6a-141">On the **New user** page, follow these steps:</span></span>

    1. <span data-ttu-id="eba6a-142">**ユーザー タイプ** フィールド値を **アプリケーション ユーザー** に変更します。</span><span class="sxs-lookup"><span data-stu-id="eba6a-142">Change the value of the **User type** field to **Application User**.</span></span>
    2. <span data-ttu-id="eba6a-143">**ユーザー名** フィールドを **Dynamics365 HR LinkedIn HRIS の統合** に設定します。</span><span class="sxs-lookup"><span data-stu-id="eba6a-143">Set the **User Name** field to **Dynamics365 HR LinkedIn HRIS Integration**.</span></span>
    3. <span data-ttu-id="eba6a-144">**アプリケーション ID** を **3a225c96-d62a-44ce-b3ec-bd4e8e9befef** に設定します。</span><span class="sxs-lookup"><span data-stu-id="eba6a-144">Set the **Application ID** field to **3a225c96-d62a-44ce-b3ec-bd4e8e9befef**.</span></span>
    4. <span data-ttu-id="eba6a-145">**名** 、 **姓** 、 **代表電子メール** フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="eba6a-145">Enter any value in the **First Name** , **Last Name** , and **Primary Email** fields.</span></span>
    5. <span data-ttu-id="eba6a-146">ツール バーの **保存 \& 終了** を選択します。</span><span class="sxs-lookup"><span data-stu-id="eba6a-146">On the toolbar, select **Save \& Close**.</span></span>

### <a name="assign-a-security-role-to-the-new-user"></a><span data-ttu-id="eba6a-147">セキュリティ ロールを新規ユーザーに割り当てる</span><span class="sxs-lookup"><span data-stu-id="eba6a-147">Assign a security role to the new user</span></span>

<span data-ttu-id="eba6a-148">前のセクションで新規アプリケーション ユーザーを保存して終了した後、 **ユーザーの一覧** ページに戻ります。</span><span class="sxs-lookup"><span data-stu-id="eba6a-148">After you save and close the new application user in the previous section, you're returned to the **Users list** page.</span></span>

1. <span data-ttu-id="eba6a-149">**ユーザーの一覧** ページで、ビューを **アプリケーション ユーザー** に変更します。</span><span class="sxs-lookup"><span data-stu-id="eba6a-149">On the **Users list** page, change the view to **Application Users**.</span></span>

2. <span data-ttu-id="eba6a-150">前のセクションで作成したアプリケーション ユーザーを選択します。</span><span class="sxs-lookup"><span data-stu-id="eba6a-150">Select the application user that you created in the previous section.</span></span>

3. <span data-ttu-id="eba6a-151">ツール バーの **ロールの管理** を選択します。</span><span class="sxs-lookup"><span data-stu-id="eba6a-151">On the toolbar, select **Manage Roles**.</span></span>

4. <span data-ttu-id="eba6a-152">以前に統合用に作成したセキュリティ ロールを選択します。</span><span class="sxs-lookup"><span data-stu-id="eba6a-152">Select the security role that you created earlier for the integration.</span></span>

5. <span data-ttu-id="eba6a-153">**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="eba6a-153">Select **OK**.</span></span>

### <a name="add-an-azure-active-directory-app-in-human-resources"></a><span data-ttu-id="eba6a-154">Human Resources に Azure Active Directory アプリを追加</span><span class="sxs-lookup"><span data-stu-id="eba6a-154">Add an Azure Active Directory app in Human Resources</span></span>

1. <span data-ttu-id="eba6a-155">Dynamics 365 Human Resources で、 **Azure Active Directory アプリケーション** ページを開きます。</span><span class="sxs-lookup"><span data-stu-id="eba6a-155">In Dynamics 365 Human Resources, open the **Azure Active Directory applications** page.</span></span>
2. <span data-ttu-id="eba6a-156">一覧に新規レコードを追加し、次のフィールドを設定します:</span><span class="sxs-lookup"><span data-stu-id="eba6a-156">Add a new record to the list, and set the following fields:</span></span>

    - <span data-ttu-id="eba6a-157">**クライアント ID** : **3a225c96-d62a-44ce-b3ec-bd4e8e9befef** を入力します。</span><span class="sxs-lookup"><span data-stu-id="eba6a-157">**Client ID** : Enter **3a225c96-d62a-44ce-b3ec-bd4e8e9befef**.</span></span>
    - <span data-ttu-id="eba6a-158">**名前** : 以前に作成した Power Apps セキュリティ ロール ( **LinkedIn タレント ハブ HRIS の統合** など) の名前を入力します。</span><span class="sxs-lookup"><span data-stu-id="eba6a-158">**Name** : Enter the name of the Power Apps security role that you created earlier, such as **LinkedIn Talent Hub HRIS Integration**.</span></span>
    - <span data-ttu-id="eba6a-159">**ユーザー ID** : 人事管理でデータを書き込むアクセス許可を持つユーザーを選択します。</span><span class="sxs-lookup"><span data-stu-id="eba6a-159">**User ID** : Select a user who has permissions to write data in Personnel Management.</span></span>

### <a name="create-the-entity-in-common-data-service"></a><span data-ttu-id="eba6a-160">Common Data Service でのエンティティの作成</span><span class="sxs-lookup"><span data-stu-id="eba6a-160">Create the entity in Common Data Service</span></span>

> [!IMPORTANT]
> <span data-ttu-id="eba6a-161">LinkedIn タレント ハブは、Common Data Service for Human Resources の仮想エンティティに依存します。</span><span class="sxs-lookup"><span data-stu-id="eba6a-161">The integration with LinkedIn Talent Hub depends on virtual entities in Common Data Service for Human Resources.</span></span> <span data-ttu-id="eba6a-162">設定でのこの手順の前提条件として、仮想エンティティを構成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="eba6a-162">As a prerequisite for this step in the setup, you must configure virtual entities.</span></span> <span data-ttu-id="eba6a-163">仮想エンティティの構成方法については、[Common Data Service 仮想エンティティの構成](https://docs.microsoft.com/dynamics365/human-resources/hr-admin-integration-common-data-service-virtual-entities) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="eba6a-163">For information about how to configure virtual entities, see [Configure Common Data Service virtual entities](https://docs.microsoft.com/dynamics365/human-resources/hr-admin-integration-common-data-service-virtual-entities).</span></span>

1. <span data-ttu-id="eba6a-164">Human Resources で、 **Common Data Service (CDS) の統合** ページを開きます。</span><span class="sxs-lookup"><span data-stu-id="eba6a-164">In Human Resources, open the **Common Data Service (CDS) integration** page.</span></span>

2. <span data-ttu-id="eba6a-165">**仮想エンティティ** タブを選択します。</span><span class="sxs-lookup"><span data-stu-id="eba6a-165">Select the **Virtual entities** tab.</span></span>

3. <span data-ttu-id="eba6a-166">エンティティの一覧をエンティティ ラベルでフィルターして、 **LinkedIn がエクスポートした候補者** を検索します。</span><span class="sxs-lookup"><span data-stu-id="eba6a-166">Filter the entity list by entity label to find **LinkedIn exported candidate**.</span></span>

4. <span data-ttu-id="eba6a-167">エンティティを選択し、 **生成/更新** を選択します。</span><span class="sxs-lookup"><span data-stu-id="eba6a-167">Select the entity, and then select **Generate/refresh**.</span></span>

## <a name="exporting-candidate-records"></a><span data-ttu-id="eba6a-168">候補者レコードのエクスポート</span><span class="sxs-lookup"><span data-stu-id="eba6a-168">Exporting candidate records</span></span>

<span data-ttu-id="eba6a-169">設定が完了した後、採用担当者と人事管理 (HR) 担当者は、LinkedIn タレント ハブの **HRIS へのエクスポート** 機能を使用して、採用された候補者レコードを LinkedIn タレント ハブから Human Resources にエクスポートできます。</span><span class="sxs-lookup"><span data-stu-id="eba6a-169">After the setup is completed, recruiters and Human resources (HR) professionals can use the **Export to HRIS** function in LinkedIn Talent Hub to export hired candidate records from LinkedIn Talent Hub to Human Resources.</span></span>

### <a name="export-records-from-linkedin-talent-hub"></a><span data-ttu-id="eba6a-170">LinkedIn タレント ハブからのレコードのエクスポート</span><span class="sxs-lookup"><span data-stu-id="eba6a-170">Export records from LinkedIn Talent Hub</span></span>

<span data-ttu-id="eba6a-171">候補者が採用プロセスを通過し採用された後は、その候補者レコードを LinkedIn タレント ハブから Human Resource にエクスポートできます。</span><span class="sxs-lookup"><span data-stu-id="eba6a-171">After a candidate has moved through the recruiting process and has been hired, you can export the candidate record from LinkedIn Talent Hub to Human Resources.</span></span>

1. <span data-ttu-id="eba6a-172">LinkedIn タレント ハブで、新しい従業員を採用したプロジェクトを開きます。</span><span class="sxs-lookup"><span data-stu-id="eba6a-172">In LinkedIn Talent Hub, open the project that you hired the new employee for.</span></span>

2. <span data-ttu-id="eba6a-173">候補者レコードを選択します。</span><span class="sxs-lookup"><span data-stu-id="eba6a-173">Select a candidate record.</span></span>

3. <span data-ttu-id="eba6a-174">**ステージの変更** を選択し、 **雇用** を選択します。</span><span class="sxs-lookup"><span data-stu-id="eba6a-174">Select **Change stage** , and then select **Hired**.</span></span>

4. <span data-ttu-id="eba6a-175">候補者の省略記号メニュー ( **...** ) で、 **HRIS へのエクスポート** を選択します。</span><span class="sxs-lookup"><span data-stu-id="eba6a-175">On the ellipsis menu ( **...** ) for the candidate, select **Export to HRIS**.</span></span>

5. <span data-ttu-id="eba6a-176">**HRIS へのエクスポート** ペインで、エクスポートする必要がある情報を入力します:</span><span class="sxs-lookup"><span data-stu-id="eba6a-176">In the **Export to HRIS** pane, enter the information that must be exported:</span></span>

    - <span data-ttu-id="eba6a-177">**HRIS プロバイダー** フィールドで、 **Microsoft Dynamics 365 Human Resources** を選択します。</span><span class="sxs-lookup"><span data-stu-id="eba6a-177">In the **HRIS provider** field, select **Microsoft Dynamics 365 Human Resources**.</span></span>
    - <span data-ttu-id="eba6a-178">**開始日** フィールドで、新規従業員に対する値を選択します。</span><span class="sxs-lookup"><span data-stu-id="eba6a-178">In the **Start date** field, select a value for the new employee.</span></span>
    - <span data-ttu-id="eba6a-179">**役職** フィールドに、新規従業員の役職を入力します。</span><span class="sxs-lookup"><span data-stu-id="eba6a-179">In the **Job title** field, enter a job title for the new employee's job.</span></span>
    - <span data-ttu-id="eba6a-180">**場所** フィールドに、従業員が拠点とする場所を入力します。</span><span class="sxs-lookup"><span data-stu-id="eba6a-180">In the **Location** field, enter the location where the employee will be based.</span></span>
    - <span data-ttu-id="eba6a-181">従業員の電子メール アドレスを入力または確認します。</span><span class="sxs-lookup"><span data-stu-id="eba6a-181">Enter or verify the employee's email address.</span></span>

![LinkedIn タレント ハブの HRIS ペインにエクスポート](./media/hr-admin-integration-linkedin-talent-hub-export.jpg)

## <a name="complete-onboarding-in-human-resources"></a><span data-ttu-id="eba6a-183">Human Resources でのオンボードの完了</span><span class="sxs-lookup"><span data-stu-id="eba6a-183">Complete onboarding in Human Resources</span></span>

<span data-ttu-id="eba6a-184">LinkedIn タレント ハブから Human Resources にエクスポートされた候補者レコードは、 **人事管理** ページの **採用候補者** セクションに表示されます。</span><span class="sxs-lookup"><span data-stu-id="eba6a-184">Candidate records that are exported from LinkedIn Talent Hub to Human Resources appear in the **Candidates to hire** section of the **Personnel management** page.</span></span>

1. <span data-ttu-id="eba6a-185">Human Resources で、 **人事管理** ページを開きます。</span><span class="sxs-lookup"><span data-stu-id="eba6a-185">In Human Resources, open the **Personnel management** page.</span></span>

2. <span data-ttu-id="eba6a-186">**採用候補者** セクションで、選択した候補に対して **採用** を選択します。</span><span class="sxs-lookup"><span data-stu-id="eba6a-186">In the **Candidates to hire** section, select **Hire** for the selected candidate.</span></span>

3. <span data-ttu-id="eba6a-187">**新しい作業者の採用** ダイアログ ボックスでレコードを確認し、必要な情報を追加します。</span><span class="sxs-lookup"><span data-stu-id="eba6a-187">In the **Hire new worker** dialog box, review the record, and add any required information.</span></span> <span data-ttu-id="eba6a-188">また、候補者が採用された職位番号を選択することもできます。</span><span class="sxs-lookup"><span data-stu-id="eba6a-188">You can also select the position number that the candidate has been hired for.</span></span>

<span data-ttu-id="eba6a-189">必要な情報を入力した後、従業員レコードの作成および従業員のオンボードに関する標準プロセスを続けることができます。</span><span class="sxs-lookup"><span data-stu-id="eba6a-189">After the required information has been entered, you can continue with your standard processes for creating employee records and onboarding employees.</span></span>

<span data-ttu-id="eba6a-190">次の詳細がインポートされ、新しい従業員レコードに含まれます:</span><span class="sxs-lookup"><span data-stu-id="eba6a-190">The following details are imported and included on the new employee record:</span></span>

- <span data-ttu-id="eba6a-191">名</span><span class="sxs-lookup"><span data-stu-id="eba6a-191">First name</span></span>
- <span data-ttu-id="eba6a-192">姓</span><span class="sxs-lookup"><span data-stu-id="eba6a-192">Last name</span></span>
- <span data-ttu-id="eba6a-193">雇用開始日</span><span class="sxs-lookup"><span data-stu-id="eba6a-193">Employment start date</span></span>
- <span data-ttu-id="eba6a-194">メール アドレス</span><span class="sxs-lookup"><span data-stu-id="eba6a-194">Email address</span></span>
- <span data-ttu-id="eba6a-195">電話番号</span><span class="sxs-lookup"><span data-stu-id="eba6a-195">Phone number</span></span>

## <a name="see-also"></a><span data-ttu-id="eba6a-196">参照</span><span class="sxs-lookup"><span data-stu-id="eba6a-196">See also</span></span>

[<span data-ttu-id="eba6a-197">Common Data Service 仮想エンティティの構成</span><span class="sxs-lookup"><span data-stu-id="eba6a-197">Configure Common Data Service virtual entities</span></span>](./hr-admin-integration-common-data-service-virtual-entities.md)<br>
[<span data-ttu-id="eba6a-198">Common Data Service とは</span><span class="sxs-lookup"><span data-stu-id="eba6a-198">What is Common Data Service?</span></span>](https://docs.microsoft.com/powerapps/maker/common-data-service/data-platform-intro)
