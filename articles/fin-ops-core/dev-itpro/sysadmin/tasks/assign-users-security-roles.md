---
title: ユーザーのセキュリティ ロールへの割り当て
description: Finance and Operations アプリにアクセスするには、ユーザーをセキュリティ ロールに割り当てる必要があります。
author: ChrisGarty
manager: AnnBe
ms.date: 11/14/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SysSecRolesEditUsers, SysSecAssignmentQueryLookup, SysQueryForm, SysSecRoleExcludeUsers
audience: Application User
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: cgarty
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: e4f4ef4535de9e371829c2d86d4fdc1400510c7b
ms.sourcegitcommit: 6aa74f66f1abd3a7977050a5339b0b17e62ff053
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/15/2019
ms.locfileid: "2807999"
---
# <a name="assign-users-to-security-roles"></a><span data-ttu-id="00af5-103">ユーザーのセキュリティ ロールへの割り当て</span><span class="sxs-lookup"><span data-stu-id="00af5-103">Assign users to security roles</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="00af5-104">一般的な能力以外のものを使用する場合は、ユーザーがセキュリティ ロールに割り当てられている必要があります。</span><span class="sxs-lookup"><span data-stu-id="00af5-104">To use anything other than common capabilities, users must be assigned to security roles.</span></span> <span data-ttu-id="00af5-105">この手順では、業務データに基づいてシステム管理者がどのようにしてユーザーを自動的にロールに割り当てられるかについて説明します。</span><span class="sxs-lookup"><span data-stu-id="00af5-105">This procedure explains how system administrators can automatically assign users to roles, based on business data.</span></span> 

## <a name="automatically-assign-users-to-roles"></a><span data-ttu-id="00af5-106">ロールへのユーザーの自動割り当て</span><span class="sxs-lookup"><span data-stu-id="00af5-106">Automatically assign users to roles</span></span>
1. <span data-ttu-id="00af5-107">**ナビゲーション ウィンドウ > モジュール > システム管理 > セキュリティ > ユーザーをロールに割り当てる**に移動します。</span><span class="sxs-lookup"><span data-stu-id="00af5-107">Go to **Navigation pane > Modules > System administration > Security > Assign users to roles**.</span></span>
2. <span data-ttu-id="00af5-108">ツリーで、「会計監修者」を選択します。</span><span class="sxs-lookup"><span data-stu-id="00af5-108">In the tree, select 'Accounting supervisor'.</span></span> <span data-ttu-id="00af5-109">ルールを構成するロールを選択します。</span><span class="sxs-lookup"><span data-stu-id="00af5-109">Select the role that you want to configure the rule for.</span></span> <span data-ttu-id="00af5-110">この例では、会計監修者を選択します。</span><span class="sxs-lookup"><span data-stu-id="00af5-110">In this example, select Accounting supervisor.</span></span> 
3. <span data-ttu-id="00af5-111">**ルールの追加**をクリックして、ドロップ ダイアログを開きます。</span><span class="sxs-lookup"><span data-stu-id="00af5-111">Click **Add rule** to open the drop dialog.</span></span>
4. <span data-ttu-id="00af5-112">**クエリの選択**一覧で、目的のレコードを見つけ、選択します。</span><span class="sxs-lookup"><span data-stu-id="00af5-112">In the **Select a query**list, find and select the desired record.</span></span> <span data-ttu-id="00af5-113">このルールを使用するには、クエリを選択します。</span><span class="sxs-lookup"><span data-stu-id="00af5-113">Select the query to use for this rule.</span></span>  
5. <span data-ttu-id="00af5-114">**メンバーシップ ルール名**一覧で、選択された行のリンクをクリックします。</span><span class="sxs-lookup"><span data-stu-id="00af5-114">In the **Membership rule name** list, click the link in the selected row.</span></span>
6. <span data-ttu-id="00af5-115">**クエリの編集**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="00af5-115">Click **Edit query**.</span></span> <span data-ttu-id="00af5-116">必要に応じてクエリを編集します。</span><span class="sxs-lookup"><span data-stu-id="00af5-116">Edit the query, as needed.</span></span>  
7. <span data-ttu-id="00af5-117">**OK**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="00af5-117">Click **OK**.</span></span>
8. <span data-ttu-id="00af5-118">**自動ロール割り当ての実行**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="00af5-118">Click **Run automatic role assignment**.</span></span>
9. <span data-ttu-id="00af5-119">ナビゲーション ウィンドウ **> モジュール > システム管理 > ユーザー > ユーザー** の順に進みます (別のブラウザー タブで行うことが望ましい)。</span><span class="sxs-lookup"><span data-stu-id="00af5-119">Go to **Navigation pane > Modules > System administration > Users > Users** (ideally in a separate browser tab).</span></span>
10. <span data-ttu-id="00af5-120">さまざまなユーザーに割り当てられているロールを確認して、ロール割り当てクエリが正しいことを確認します。</span><span class="sxs-lookup"><span data-stu-id="00af5-120">Review the roles assigned to various users to confirm that the role assignment query was correct.</span></span> <span data-ttu-id="00af5-121">必要に応じて調整して再実行します。</span><span class="sxs-lookup"><span data-stu-id="00af5-121">Adjust and re-run if needed.</span></span>

## <a name="exclude-users-from-automatic-role-assignment"></a><span data-ttu-id="00af5-122">自動ロール割り当てからのユーザーの除外</span><span class="sxs-lookup"><span data-stu-id="00af5-122">Exclude users from automatic role assignment</span></span>
1. <span data-ttu-id="00af5-123">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="00af5-123">Close the page.</span></span>
2. <span data-ttu-id="00af5-124">**ナビゲーション ウィンドウ > モジュール > システム管理 > セキュリティ > ユーザーをロールに割り当てる**に移動します。</span><span class="sxs-lookup"><span data-stu-id="00af5-124">Go to **Navigation pane > Modules > System administration > Security > Assign users to roles**.</span></span>
3. <span data-ttu-id="00af5-125">ツリーで、「会計監修者」を選択します。</span><span class="sxs-lookup"><span data-stu-id="00af5-125">In the tree, select 'Accounting supervisor'.</span></span> <span data-ttu-id="00af5-126">ロールを選択します。</span><span class="sxs-lookup"><span data-stu-id="00af5-126">Select a role.</span></span> <span data-ttu-id="00af5-127">この例では、会計監修者を選択します。</span><span class="sxs-lookup"><span data-stu-id="00af5-127">For this example, select Accounting supervisor.</span></span>  
4. <span data-ttu-id="00af5-128">**ロールに割り当てられたユーザー** メニューで、**手動でのユーザーの割り当て/除外**を選択します。</span><span class="sxs-lookup"><span data-stu-id="00af5-128">In the **Users assigned to role** menu, select **Manually assign / exclude users**.</span></span>
5. <span data-ttu-id="00af5-129">**ユーザーをロールに割り当てる、またはユーザーをロールから除外する**の一覧で、選択された行をマークします。</span><span class="sxs-lookup"><span data-stu-id="00af5-129">In the **Assign users to or exclude users from role** list, mark the selected row.</span></span> <span data-ttu-id="00af5-130">ユーザーを選択します。</span><span class="sxs-lookup"><span data-stu-id="00af5-130">Select a user.</span></span>  
6. <span data-ttu-id="00af5-131">**アクション ウィンドウ**で、**ロールから除外**を選択します。</span><span class="sxs-lookup"><span data-stu-id="00af5-131">On the **Action pane**, select **Exclude from role**.</span></span>
    
    <span data-ttu-id="00af5-132">**ロールから除外**をクリックして、ロールから選択したユーザーを除外できます。</span><span class="sxs-lookup"><span data-stu-id="00af5-132">Click **Exclude from role** to exclude the selected users from the role.</span></span> <span data-ttu-id="00af5-133">除外を削除するには、除外を削除するユーザーを選択して**ステータスのリセット**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="00af5-133">To remove exclusions, select the users that you want to remove exclusions for, and then click **Reset status**.</span></span> <span data-ttu-id="00af5-134">ユーザーのステータスをリセットして除外を削除した場合、ユーザーのロールが再度自動的に割り当てられます。</span><span class="sxs-lookup"><span data-stu-id="00af5-134">When you remove an exclusion by resetting the user’s status, the user’s role is again assigned automatically.</span></span> <span data-ttu-id="00af5-135">ただし、ステータスをリセットした場合、ユーザーはすぐにロールに割り当てられたり、ロールから除外されません。</span><span class="sxs-lookup"><span data-stu-id="00af5-135">However, the user is not immediately assigned to the role or excluded from the role when you reset the status.</span></span> <span data-ttu-id="00af5-136">代わりに、ユーザーは自動ロール割り当てのルールが実行される次回にロールに割り当てられたり、ロールから削除されたりします。</span><span class="sxs-lookup"><span data-stu-id="00af5-136">Instead, the user is either assigned to the role or removed from the role the next time that the rules for automatic role assignment are run.</span></span>  
