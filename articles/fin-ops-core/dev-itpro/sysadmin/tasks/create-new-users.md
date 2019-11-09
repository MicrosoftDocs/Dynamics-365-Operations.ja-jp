---
title: 新規ユーザーの作成
description: ユーザーは、ジョブの実行のためにシステムへアクセスする必要がある、組織の内部従業員、または外部顧客や仕入先です。
author: maertenm
manager: AnnBe
ms.date: 10/08/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SysUserManagement, SysDataAreaSelectLookup, SysSecUserAddRoles, SysUserMSODSUserImport
audience: Application User
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: maertenm
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 3c347a34a389c32d005cc8086c4a1349ecb8a698
ms.sourcegitcommit: d37fb09101c30858bcb975931b3d8f947d72017b
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/10/2019
ms.locfileid: "2570524"
---
# <a name="create-new-users"></a><span data-ttu-id="584a0-103">新規ユーザーの作成</span><span class="sxs-lookup"><span data-stu-id="584a0-103">Create new users</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="584a0-104">ユーザーは、ジョブの実行のためにシステムへアクセスする必要がある、組織の内部従業員、または外部顧客や仕入先です。</span><span class="sxs-lookup"><span data-stu-id="584a0-104">Users are internal employees of your organization, or external customers and vendors, who require access to the system to do their jobs.</span></span>

## <a name="associate-a-user-with-a-license-new-license-types-only"></a><span data-ttu-id="584a0-105">ユーザーをライセンスに関連付ける (新しいライセンスタイプのみ)</span><span class="sxs-lookup"><span data-stu-id="584a0-105">Associate a user with a license (new license types only)</span></span>
<span data-ttu-id="584a0-106">2019 年 10 月に追加された新しいライセンスタイプのいずれかを使用している場合は、ユーザーはライセンスに関連付けられている必要があります。</span><span class="sxs-lookup"><span data-stu-id="584a0-106">For customers who are on one of the new license types that were added in October 2019, users must be associated with a license.</span></span> <span data-ttu-id="584a0-107">ライセンスに関連付けられているユーザーは、最初にログインしたときに、ロールを持たないシステムユーザーとして自動的に追加されます。</span><span class="sxs-lookup"><span data-stu-id="584a0-107">Users who are associated with a license are automatically added as system users who have no roles the first time that they sign in.</span></span> <span data-ttu-id="584a0-108">ライセンスに関連付けられていないユーザーには、警告メッセージが表示されます。</span><span class="sxs-lookup"><span data-stu-id="584a0-108">Users who aren't associated with a licence receive a warning message.</span></span>

<span data-ttu-id="584a0-109">システム管理者は、[Microsoft 365 管理者センター](https://docs.microsoft.com/office365/admin/admin-overview/about-the-admin-center?view=o365-worldwide)で、[ユーザーにライセンスを割り当てる](https://docs.microsoft.com/office365/admin/subscriptions-and-billing/assign-licenses-to-users?view=o365-worldwide)ことができます。</span><span class="sxs-lookup"><span data-stu-id="584a0-109">System admins can [assign licenses to users](https://docs.microsoft.com/office365/admin/subscriptions-and-billing/assign-licenses-to-users?view=o365-worldwide) in the [Microsoft 365 admin center](https://docs.microsoft.com/office365/admin/admin-overview/about-the-admin-center?view=o365-worldwide).</span></span>

## <a name="add-a-new-user"></a><span data-ttu-id="584a0-110">新しいユーザーを追加する</span><span class="sxs-lookup"><span data-stu-id="584a0-110">Add a new user</span></span>
1. <span data-ttu-id="584a0-111">**システム管理 \> ユーザー \> ユーザー**の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="584a0-111">Go to **System administration \> Users \> Users**.</span></span>
2. <span data-ttu-id="584a0-112">アクション ウィンドウで、**新規**を選択します。</span><span class="sxs-lookup"><span data-stu-id="584a0-112">On the Action Pane, select **New**.</span></span>
3. <span data-ttu-id="584a0-113">**ユーザー ID** フィールドに、ユーザーの固有 ID を入力します。</span><span class="sxs-lookup"><span data-stu-id="584a0-113">In the **User ID** field, enter a unique identifier for the user.</span></span> <span data-ttu-id="584a0-114">ユーザー ID が必要です。</span><span class="sxs-lookup"><span data-stu-id="584a0-114">A user ID is required.</span></span>  
4. <span data-ttu-id="584a0-115">**ユーザー名**フィールドに、ユーザー名を入力します。</span><span class="sxs-lookup"><span data-stu-id="584a0-115">In the **User name** field, enter the user's name.</span></span>  
5. <span data-ttu-id="584a0-116">**ドメイン**フィールドに、ユーザーのドメインを入力します。</span><span class="sxs-lookup"><span data-stu-id="584a0-116">In the **Domain** field, enter the user's domain.</span></span>  
6. <span data-ttu-id="584a0-117">**エイリアス**フィールドに、ユーザーのエイリアスを入力します。</span><span class="sxs-lookup"><span data-stu-id="584a0-117">In the **Alias** field, enter the user's alias.</span></span>  
7. <span data-ttu-id="584a0-118">**法人**フィールドで、目的の会社を選択します。</span><span class="sxs-lookup"><span data-stu-id="584a0-118">In the **Company** field, select the desired company.</span></span> 
8. <span data-ttu-id="584a0-119">**ユーザーのロール**クイックタブで、**ロールの割り当て**を選択し、[ユーザーをセキュリティロールに割り当てます。](assign-users-security-roles.md)</span><span class="sxs-lookup"><span data-stu-id="584a0-119">On the **User's roles** FastTab, select **Assign roles** to [assign users to security roles](assign-users-security-roles.md)</span></span>
9. <span data-ttu-id="584a0-120">**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="584a0-120">Select **OK**.</span></span>
10. <span data-ttu-id="584a0-121">**保存** を選択します。</span><span class="sxs-lookup"><span data-stu-id="584a0-121">Select **Save**.</span></span>

## <a name="import-users"></a><span data-ttu-id="584a0-122">ユーザーのインポート</span><span class="sxs-lookup"><span data-stu-id="584a0-122">Import users</span></span>
1. <span data-ttu-id="584a0-123">アクション ウィンドウで、**ユーザーのインポート**を選択します。</span><span class="sxs-lookup"><span data-stu-id="584a0-123">On the Action Pane, select **Import users**.</span></span>
2. <span data-ttu-id="584a0-124">一覧で、選択された行をマークします。</span><span class="sxs-lookup"><span data-stu-id="584a0-124">In the list, mark the selected row.</span></span>
3. <span data-ttu-id="584a0-125">**ユーザーのインポート**を選択します。</span><span class="sxs-lookup"><span data-stu-id="584a0-125">Select **Import users**.</span></span>
4. <span data-ttu-id="584a0-126">**閉じる**を選択します。</span><span class="sxs-lookup"><span data-stu-id="584a0-126">Select **Close**.</span></span>
