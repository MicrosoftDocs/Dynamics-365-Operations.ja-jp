---
title: 新規ユーザーの作成
description: ユーザーは、ジョブの実行のためにシステムへアクセスする必要がある、組織の内部従業員、または外部顧客や仕入先です。
author: peakerbl
manager: AnnBe
ms.date: 01/12/2021
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SysUserManagement, SysDataAreaSelectLookup, SysSecUserAddRoles, SysUserMSODSUserImport
audience: Application User
ms.reviewer: sericks
ms.search.region: Global
ms.author: peakerbl
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: ca062ddd49f1c206c503fb6160ed436fe2d6f7e9
ms.sourcegitcommit: 9e27a097b7eb3c8f2df66011ccc597ad18bc5445
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/13/2021
ms.locfileid: "4878660"
---
# <a name="create-new-users"></a><span data-ttu-id="20d8f-103">新規ユーザーの作成</span><span class="sxs-lookup"><span data-stu-id="20d8f-103">Create new users</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="20d8f-104">Finance and Operations アプリにアクセスするには、まず **ユーザー** ページ (**システム管理 \> ユーザー \> ユーザー**) に追加する必要があります。</span><span class="sxs-lookup"><span data-stu-id="20d8f-104">Before you can access Finance and Operations apps, you must first be added to the **Users** page (**System administration \> Users \> Users**).</span></span> <span data-ttu-id="20d8f-105">ユーザーには、組織の内部従業員、または外部顧客や仕入先が含まれます。</span><span class="sxs-lookup"><span data-stu-id="20d8f-105">Users include internal employees of your organization, or external customers and vendors.</span></span> <span data-ttu-id="20d8f-106">ユーザーは手動でインポートまたは追加できます。</span><span class="sxs-lookup"><span data-stu-id="20d8f-106">Users can be imported or added manually.</span></span> <span data-ttu-id="20d8f-107">すべてのユーザーは、準拠して使用するために正しいライセンスを取得する必要があります。</span><span class="sxs-lookup"><span data-stu-id="20d8f-107">All users must be correctly licensed for compliant use.</span></span>

<span data-ttu-id="20d8f-108">Finance and Operations アプリの購入方法とライセンスの取得方法については、[Microsoft Dynamics 365 ライセンス ガイド](https://go.microsoft.com/fwlink/?LinkId=866544&amp;clcid=0x409) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="20d8f-108">For information about how to buy and license for Finance and Operations apps, see [Microsoft Dynamics 365 Licensing Guide](https://go.microsoft.com/fwlink/?LinkId=866544&amp;clcid=0x409).</span></span>

## <a name="assign-a-license-to-a-user"></a><span data-ttu-id="20d8f-109">ライセンスのユーザーへの割り当て</span><span class="sxs-lookup"><span data-stu-id="20d8f-109">Assign a license to a user</span></span>
<span data-ttu-id="20d8f-110">システム管理者は、[Microsoft 365 管理者センター](https://docs.microsoft.com/office365/admin/admin-overview/about-the-admin-center?view=o365-worldwide)で、[ユーザーにライセンスを割り当てる](https://docs.microsoft.com/office365/admin/subscriptions-and-billing/assign-licenses-to-users?view=o365-worldwide)ことができます。</span><span class="sxs-lookup"><span data-stu-id="20d8f-110">System admins can [assign licenses to users](https://docs.microsoft.com/office365/admin/subscriptions-and-billing/assign-licenses-to-users?view=o365-worldwide) in the [Microsoft 365 admin center](https://docs.microsoft.com/office365/admin/admin-overview/about-the-admin-center?view=o365-worldwide).</span></span>

## <a name="add-an-external-user-in-azure-ad-and-assign-a-license"></a><span data-ttu-id="20d8f-111">Azure AD への外部ユーザーの追加とライセンスの割り当て</span><span class="sxs-lookup"><span data-stu-id="20d8f-111">Add an external user in Azure AD and assign a license</span></span> 
<span data-ttu-id="20d8f-112">外部ユーザーがライセンスを割り当てできるよう、テナント ディレクトリ (Azure Active Directory (Azure AD)) に表示される必要があります。</span><span class="sxs-lookup"><span data-stu-id="20d8f-112">External users must be represented in your tenant directory (Azure Active Directory (Azure AD)) so that they can be assigned licenses.</span></span> <span data-ttu-id="20d8f-113">それら外部ユーザーは、ゲスト ユーザーとして Azure AD のテナントに追加した後、適切なライセンスを割り当てる必要があります。</span><span class="sxs-lookup"><span data-stu-id="20d8f-113">Those external users should be added to the tenant in Azure AD as guest users and then assigned the appropriate licenses.</span></span> <span data-ttu-id="20d8f-114">Finance and Operations アプリの要件は、ゲスト ユーザーの会社が Azure AD を使用することです。</span><span class="sxs-lookup"><span data-stu-id="20d8f-114">A requirement for Finance and Operations apps is that the guest user's company must use Azure AD.</span></span> <span data-ttu-id="20d8f-115">詳細については、[Azure ポータルで Azure Active Directory B2B コラボレーション ユーザーを追加する](https://docs.microsoft.com/azure/active-directory/b2b/add-users-administrator) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="20d8f-115">For more information, see [Add Azure Active Directory B2B collaboration users in the Azure portal](https://docs.microsoft.com/azure/active-directory/b2b/add-users-administrator).</span></span>

## <a name="import-new-users-from-azure-ad"></a><span data-ttu-id="20d8f-116">Azure AD からの新規ユーザーのインポート</span><span class="sxs-lookup"><span data-stu-id="20d8f-116">Import new users from Azure AD</span></span> 
1. <span data-ttu-id="20d8f-117">**システム管理** \> **ユーザー** \> **ユーザー** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="20d8f-117">Go to **System administration** \> **User** \> **Users**.</span></span>
2. <span data-ttu-id="20d8f-118">アクション ウィンドウで、**ユーザーのインポート** を選択します。</span><span class="sxs-lookup"><span data-stu-id="20d8f-118">On the Action Pane, select **Import users**.</span></span>
3. <span data-ttu-id="20d8f-119">インポートされるユーザーを選択します。</span><span class="sxs-lookup"><span data-stu-id="20d8f-119">Select the users to be imported.</span></span> <span data-ttu-id="20d8f-120">この一覧には、現在この環境のユーザーではない Azure AD ユーザーが含まれています。</span><span class="sxs-lookup"><span data-stu-id="20d8f-120">The list includes Azure AD users that are currently not users in this environment.</span></span>
4. <span data-ttu-id="20d8f-121">**ユーザーのインポート** を選択します。</span><span class="sxs-lookup"><span data-stu-id="20d8f-121">Select **Import users**.</span></span>
5. <span data-ttu-id="20d8f-122">**閉じる** を選択します。</span><span class="sxs-lookup"><span data-stu-id="20d8f-122">Select **Close**.</span></span>

> [!NOTE]
> <span data-ttu-id="20d8f-123">**会社** フィールドの値は、管理者の現在のセッション会社に基づいて設定されます。インポート後に、必要に応じロールと組織を割り当てる必要があります。</span><span class="sxs-lookup"><span data-stu-id="20d8f-123">The value for the **Company** field will be set based on the current session company for the admin. After import, you must assign roles and organizations as applicable.</span></span> <span data-ttu-id="20d8f-124">詳細については、[ユーザーのセキュリティ ロールへの割り当て](assign-users-security-roles.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="20d8f-124">For more information, see [Assign users to security roles](assign-users-security-roles.md).</span></span> <span data-ttu-id="20d8f-125">条件付きで、ユーザーを **個人** に関連付けたり、言語などのユーザー オプションを更新したりする必要がある場合もあります。</span><span class="sxs-lookup"><span data-stu-id="20d8f-125">Conditionally, it might also be required to associate the user with a **Person** and to update user options such as language.</span></span>

## <a name="manually-add-a-new-user"></a><span data-ttu-id="20d8f-126">新規ユーザーを手動で追加</span><span class="sxs-lookup"><span data-stu-id="20d8f-126">Manually add a new user</span></span>
1. <span data-ttu-id="20d8f-127">**システム管理** \> **ユーザー** \> **ユーザー** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="20d8f-127">Go to **System administration** \> **Users** \> **Users**.</span></span>
2. <span data-ttu-id="20d8f-128">アクション ウィンドウで、**新規** を選択します。</span><span class="sxs-lookup"><span data-stu-id="20d8f-128">On the Action Pane, select **New**.</span></span>
3. <span data-ttu-id="20d8f-129">**ユーザー ID** フィールドに、ユーザーの固有 ID を入力します。</span><span class="sxs-lookup"><span data-stu-id="20d8f-129">In the **User ID** field, enter a unique identifier for the user.</span></span>   
4. <span data-ttu-id="20d8f-130">**ユーザー名** フィールドに、ユーザー名を入力します。</span><span class="sxs-lookup"><span data-stu-id="20d8f-130">In the **User name** field, enter the user's name.</span></span>  
5. <span data-ttu-id="20d8f-131">**プロバイダー** フィールドで:</span><span class="sxs-lookup"><span data-stu-id="20d8f-131">In the **Provider** field:</span></span>
 - <span data-ttu-id="20d8f-132">内部ユーザーについては、既定値を使用します。</span><span class="sxs-lookup"><span data-stu-id="20d8f-132">For internal users, use the defaulted value.</span></span> <span data-ttu-id="20d8f-133">例: https://sts.windows.net/ で始まる Azure AD テナント。</span><span class="sxs-lookup"><span data-stu-id="20d8f-133">For example, your Azure AD tenant prefixed with https://sts.windows.net/.</span></span>  
 - <span data-ttu-id="20d8f-134">Service-2-Service accounts アカウントなどの Azure AD 以外のユーザーの場合は、基本テキスト値を入力します。</span><span class="sxs-lookup"><span data-stu-id="20d8f-134">For non-Azure AD users, such as Service-2-Service accounts, enter a basic text value.</span></span> <span data-ttu-id="20d8f-135">例: NA。</span><span class="sxs-lookup"><span data-stu-id="20d8f-135">For example, NA.</span></span> <span data-ttu-id="20d8f-136">この値は、有効な ID プロバイダ値が使用された場合にエラーが発生する可能性がある不正な認証呼び出しを回避するのに役立ちます。</span><span class="sxs-lookup"><span data-stu-id="20d8f-136">This value will help avoid incorrect authentication calls that might result in errors if a valid identity provider value is used.</span></span>  
 - <span data-ttu-id="20d8f-137">外部ユーザーまたはゲスト ユーザーの場合は、Azure AD テナント名を https://sts.windows.net/ の後に追加します。</span><span class="sxs-lookup"><span data-stu-id="20d8f-137">For external or guest users, add their Azure AD tenant name after https://sts.windows.net/.</span></span>
6. <span data-ttu-id="20d8f-138">**電子メール** フィールドに、ユーザーの完全な電子メール/ユーザー プリンシパル名を入力します。</span><span class="sxs-lookup"><span data-stu-id="20d8f-138">In the **Email** field, enter the user's full Email/User Principle Name.</span></span>  
7. <span data-ttu-id="20d8f-139">**会社** フィールドで、ユーザーの既定の起動時に開く会社を選択します。</span><span class="sxs-lookup"><span data-stu-id="20d8f-139">In the **Company** field, select the default startup company for the user.</span></span> 
8. <span data-ttu-id="20d8f-140">**保存** を選択します。</span><span class="sxs-lookup"><span data-stu-id="20d8f-140">Select **Save**.</span></span>

<span data-ttu-id="20d8f-141">ユーザー レコードを保存すると、ID プロバイダーとテレメトリ ID の値が [Microsoft Graph](https://docs.microsoft.com/graph/overview) 呼び出しに基づいて更新されます。</span><span class="sxs-lookup"><span data-stu-id="20d8f-141">The values for Identity provider and Telemetry ID will be updated based on a [Microsoft graph](https://docs.microsoft.com/graph/overview) call, when the user record is saved.</span></span> <span data-ttu-id="20d8f-142">テレメトリ ID は、Azure AD のオブジェクト ID/セキュリティ識別子 (SID) に基づきます。</span><span class="sxs-lookup"><span data-stu-id="20d8f-142">The Telemetry ID is based on the user's Object ID/Security Identifier (SID) in Azure AD.</span></span>

> [!NOTE]
> <span data-ttu-id="20d8f-143">ユーザーを追加した後で、必要に応じロールと組織を割り当てる必要があります。</span><span class="sxs-lookup"><span data-stu-id="20d8f-143">After you add a user, you must assign roles and organizations as applicable.</span></span> <span data-ttu-id="20d8f-144">詳細については、[ユーザーのセキュリティ ロールへの割り当て](assign-users-security-roles.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="20d8f-144">For more information, see [Assign users to security roles](assign-users-security-roles.md).</span></span> <span data-ttu-id="20d8f-145">条件付きで、ユーザーを **個人** に関連付けたり、言語などの **ユーザー オプション** を更新したりする必要がある場合もあります。</span><span class="sxs-lookup"><span data-stu-id="20d8f-145">Conditionally, it might also be required to associate the user with a **Person** and to update **User options** such as language.</span></span>

## <a name="change-a-user-id"></a><span data-ttu-id="20d8f-146">ユーザー ID の変更</span><span class="sxs-lookup"><span data-stu-id="20d8f-146">Change a user ID</span></span>
<span data-ttu-id="20d8f-147">ユーザー ID を変更するには、データベース内のキーの名前を変更する必要があります。</span><span class="sxs-lookup"><span data-stu-id="20d8f-147">To change a user ID, you must rename the key in the database.</span></span> <span data-ttu-id="20d8f-148">この手順を使用してユーザー ID を変更すると、すべての関連するユーザー設定が変更され、新しいユーザー ID を使用します。</span><span class="sxs-lookup"><span data-stu-id="20d8f-148">When you change a user ID by using this procedure, all related user settings are modified to use the new user ID.</span></span> <span data-ttu-id="20d8f-149">たとえば、**SysLastValue** テーブルの使用状況情報は、新しいユーザー ID を参照するために更新されます。</span><span class="sxs-lookup"><span data-stu-id="20d8f-149">For example, the usage information in the **SysLastValue** table is updated to reference the new user ID.</span></span>

> [!NOTE]
> <span data-ttu-id="20d8f-150">ユーザー ID は、ユーザー情報テーブルの主キーです。</span><span class="sxs-lookup"><span data-stu-id="20d8f-150">The user ID is the primary key of the user information table.</span></span> <span data-ttu-id="20d8f-151">主キーへのすべての参照もデータベースで更新されるため、既存のユーザーが主キーの名前を変更するには時間がかかる場合があります。</span><span class="sxs-lookup"><span data-stu-id="20d8f-151">Renaming the primary key can take some time for existing users because all references to the key are also updated in the database.</span></span> 

1. <span data-ttu-id="20d8f-152">**システム管理 \> ユーザー \> ユーザー** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="20d8f-152">Go to **System administration \> Users \> Users**.</span></span>
2. <span data-ttu-id="20d8f-153">一覧でユーザーを選択し、**オプション\> レコード情報** を選択します。</span><span class="sxs-lookup"><span data-stu-id="20d8f-153">Select a user in the list and select **Options\> Record info**.</span></span>
3. <span data-ttu-id="20d8f-154">**名前の変更** を選択します。</span><span class="sxs-lookup"><span data-stu-id="20d8f-154">Select **Rename**.</span></span>
4. <span data-ttu-id="20d8f-155">ユーザー ID に新しい固有の値を入力し、**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="20d8f-155">Enter a new and unique value for the User ID, and then select **OK**.</span></span> 
5. <span data-ttu-id="20d8f-156">**はい** を選択して確認します。</span><span class="sxs-lookup"><span data-stu-id="20d8f-156">Select **Yes** to confirm.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="20d8f-157">追加リソース</span><span class="sxs-lookup"><span data-stu-id="20d8f-157">Additional resources</span></span>

<span data-ttu-id="20d8f-158">B2B ユーザーを実装するための詳細なオプションについては、[B2B ユーザーの Azure AD へのエクスポート](../implement-b2b.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="20d8f-158">For more options to implement B2B users, see [Export B2B users to Azure AD](../implement-b2b.md).</span></span>

<span data-ttu-id="20d8f-159">コンフィギュレーション済システム アカウントの詳細については、[コンフィギュレーション済みのシステム アカウント](../pre-configured-system-accounts.md) を参照してください</span><span class="sxs-lookup"><span data-stu-id="20d8f-159">For information about preconfigured system accounts, see [Preconfigured system accounts](../pre-configured-system-accounts.md)</span></span>
