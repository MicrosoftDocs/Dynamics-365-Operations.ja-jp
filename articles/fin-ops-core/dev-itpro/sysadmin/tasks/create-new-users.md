---
title: 新規ユーザーの作成
description: ユーザーは、ジョブの実行のためにシステムへアクセスする必要がある、組織の内部従業員、または外部顧客や仕入先です。
author: peakerbl
manager: AnnBe
ms.date: 06/08/2020
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
ms.openlocfilehash: 6f861b7493d039b332358be7df7d0198cbadcb7a
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 12/05/2020
ms.locfileid: "4679843"
---
# <a name="create-new-users"></a><span data-ttu-id="8bbe0-103">新規ユーザーの作成</span><span class="sxs-lookup"><span data-stu-id="8bbe0-103">Create new users</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="8bbe0-104">ユーザーは、ジョブの実行のためにシステムへアクセスする必要がある、組織の内部従業員、または外部顧客や仕入先です。</span><span class="sxs-lookup"><span data-stu-id="8bbe0-104">Users are internal employees of your organization, or external customers and vendors, who require access to the system to do their jobs.</span></span>

## <a name="associate-a-user-with-a-license-new-license-types-only"></a><span data-ttu-id="8bbe0-105">ユーザーをライセンスに関連付ける (新しいライセンスタイプのみ)</span><span class="sxs-lookup"><span data-stu-id="8bbe0-105">Associate a user with a license (new license types only)</span></span>
<span data-ttu-id="8bbe0-106">2019 年 10 月に追加された新しいライセンスタイプのいずれかを使用している場合は、ユーザーはライセンスに関連付けられている必要があります。</span><span class="sxs-lookup"><span data-stu-id="8bbe0-106">For customers who are on one of the new license types that were added in October 2019, users must be associated with a license.</span></span> <span data-ttu-id="8bbe0-107">ライセンスに関連付けられているユーザーは、最初にログインしたときに、ロールを持たないシステムユーザーとして自動的に追加されます。</span><span class="sxs-lookup"><span data-stu-id="8bbe0-107">Users who are associated with a license are automatically added as system users who have no roles the first time that they sign in.</span></span>

<span data-ttu-id="8bbe0-108">システム管理者は、[Microsoft 365 管理者センター](https://docs.microsoft.com/office365/admin/admin-overview/about-the-admin-center?view=o365-worldwide)で、[ユーザーにライセンスを割り当てる](https://docs.microsoft.com/office365/admin/subscriptions-and-billing/assign-licenses-to-users?view=o365-worldwide)ことができます。</span><span class="sxs-lookup"><span data-stu-id="8bbe0-108">System admins can [assign licenses to users](https://docs.microsoft.com/office365/admin/subscriptions-and-billing/assign-licenses-to-users?view=o365-worldwide) in the [Microsoft 365 admin center](https://docs.microsoft.com/office365/admin/admin-overview/about-the-admin-center?view=o365-worldwide).</span></span>

## <a name="associate-an-external-user-with-a-license-new-license-types-only"></a><span data-ttu-id="8bbe0-109">外部のユーザーをライセンスに関連付ける (新しいライセンスタイプのみ)</span><span class="sxs-lookup"><span data-stu-id="8bbe0-109">Associate an external user with a license (new license types only)</span></span>
<span data-ttu-id="8bbe0-110">環境が配置されたテナントの外部ユーザーは、ライセンスを割り当てることができるように、ホスト テナント ディレクトリ (Azure Active Directory (Azure AD)) に表示されている必要があります。</span><span class="sxs-lookup"><span data-stu-id="8bbe0-110">Users external to the tenant that the environment was deployed into need to be represented in the host tenant directory (Azure Active Directory (Azure AD)) so that they can be assigned licenses.</span></span> <span data-ttu-id="8bbe0-111">それら外部ユーザーは、ゲスト ユーザーとして Azure AD のテナントに追加した後、適切なライセンスを割り当てる必要があります。</span><span class="sxs-lookup"><span data-stu-id="8bbe0-111">Those external users should be added to the tenant in Azure AD as guest users and then assigned the appropriate licenses.</span></span> <span data-ttu-id="8bbe0-112">詳細については、[Azure ポータルで Azure Active Directory B2B コラボレーション ユーザーを追加する](https://docs.microsoft.com/azure/active-directory/b2b/add-users-administrator) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="8bbe0-112">For more information, see [Add Azure Active Directory B2B collaboration users in the Azure portal](https://docs.microsoft.com/azure/active-directory/b2b/add-users-administrator).</span></span>

## <a name="add-a-new-user"></a><span data-ttu-id="8bbe0-113">新しいユーザーを追加する</span><span class="sxs-lookup"><span data-stu-id="8bbe0-113">Add a new user</span></span>
1. <span data-ttu-id="8bbe0-114">**システム管理 \> ユーザー \> ユーザー** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="8bbe0-114">Go to **System administration \> Users \> Users**.</span></span>
2. <span data-ttu-id="8bbe0-115">アクション ウィンドウで、**新規** を選択します。</span><span class="sxs-lookup"><span data-stu-id="8bbe0-115">On the Action Pane, select **New**.</span></span>
3. <span data-ttu-id="8bbe0-116">**ユーザー ID** フィールドに、ユーザーの固有 ID を入力します。</span><span class="sxs-lookup"><span data-stu-id="8bbe0-116">In the **User ID** field, enter a unique identifier for the user.</span></span> <span data-ttu-id="8bbe0-117">ユーザー ID が必要です。</span><span class="sxs-lookup"><span data-stu-id="8bbe0-117">A user ID is required.</span></span>  
4. <span data-ttu-id="8bbe0-118">**ユーザー名** フィールドに、ユーザー名を入力します。</span><span class="sxs-lookup"><span data-stu-id="8bbe0-118">In the **User name** field, enter the user's name.</span></span>  
5. <span data-ttu-id="8bbe0-119">**ドメイン** フィールドに、ユーザーのドメインを入力します。</span><span class="sxs-lookup"><span data-stu-id="8bbe0-119">In the **Domain** field, enter the user's domain.</span></span>  
6. <span data-ttu-id="8bbe0-120">**エイリアス** フィールドに、ユーザーのエイリアスを入力します。</span><span class="sxs-lookup"><span data-stu-id="8bbe0-120">In the **Alias** field, enter the user's alias.</span></span>  
7. <span data-ttu-id="8bbe0-121">**法人** フィールドで、目的の会社を選択します。</span><span class="sxs-lookup"><span data-stu-id="8bbe0-121">In the **Company** field, select the desired company.</span></span> 
8. <span data-ttu-id="8bbe0-122">**ユーザーのロール** クイック タブで、**ロールの割り当て** を選択し、ユーザーをセキュリティ ロールに割り当てます。</span><span class="sxs-lookup"><span data-stu-id="8bbe0-122">On the **User's roles** FastTab, select **Assign roles** to assign users to security roles.</span></span> <span data-ttu-id="8bbe0-123">詳細については、[ユーザーのセキュリティ ロールへの割り当て](assign-users-security-roles.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="8bbe0-123">For more information, see [Assign users to security roles](assign-users-security-roles.md).</span></span>
9. <span data-ttu-id="8bbe0-124">**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="8bbe0-124">Select **OK**.</span></span>
10. <span data-ttu-id="8bbe0-125">**保存** を選択します。</span><span class="sxs-lookup"><span data-stu-id="8bbe0-125">Select **Save**.</span></span>

## <a name="import-users"></a><span data-ttu-id="8bbe0-126">ユーザーのインポート</span><span class="sxs-lookup"><span data-stu-id="8bbe0-126">Import users</span></span>
1. <span data-ttu-id="8bbe0-127">**システム管理 \> ユーザー \> ユーザー** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="8bbe0-127">Go to **System administration \> Users \> Users**.</span></span>
2. <span data-ttu-id="8bbe0-128">アクション ウィンドウで、**ユーザーのインポート** を選択します。</span><span class="sxs-lookup"><span data-stu-id="8bbe0-128">On the Action Pane, select **Import users**.</span></span>
3. <span data-ttu-id="8bbe0-129">一覧で、選択された行をマークします。</span><span class="sxs-lookup"><span data-stu-id="8bbe0-129">In the list, mark the selected row.</span></span>
4. <span data-ttu-id="8bbe0-130">**ユーザーのインポート** を選択します。</span><span class="sxs-lookup"><span data-stu-id="8bbe0-130">Select **Import users**.</span></span>
5. <span data-ttu-id="8bbe0-131">**閉じる** を選択します。</span><span class="sxs-lookup"><span data-stu-id="8bbe0-131">Select **Close**.</span></span>

