---
title: ユーザーのセキュリティ ロールへの割り当て
description: Finance and Operations アプリにアクセスするには、ユーザーをセキュリティ ロールに割り当てる必要があります。
author: Peakerbl
ms.date: 05/06/2020
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: SysSecRolesEditUsers, SysSecAssignmentQueryLookup, SysQueryForm, SysSecRoleExcludeUsers
audience: Application User
ms.reviewer: sericks
ms.search.region: Global
ms.author: peakerbl
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: bb4b143400a1f092c8f7a15bbb047eda52a4a4d8
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/31/2021
ms.locfileid: "5745888"
---
# <a name="assign-users-to-security-roles"></a><span data-ttu-id="8f024-103">ユーザーのセキュリティ ロールへの割り当て</span><span class="sxs-lookup"><span data-stu-id="8f024-103">Assign users to security roles</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="8f024-104">Finance and Operations アプリで一般的な機能以外のものを使用する場合は、ユーザーがセキュリティ ロールに割り当てられている必要があります。</span><span class="sxs-lookup"><span data-stu-id="8f024-104">To use anything other than common capabilities in Finance and Operations apps, users must be assigned to security roles.</span></span> <span data-ttu-id="8f024-105">ルールやビジネスデータに基づいて、ユーザーを自動的にロールに割り当てたり、自動ロール割り当てからユーザーを除外したり、ユーザーを手動でロールに追加することができます。</span><span class="sxs-lookup"><span data-stu-id="8f024-105">You can assign users to roles automatically, based on rules and business data, exclude users from automatic role assignment, or add users to roles manually.</span></span>

## <a name="automatically-assign-users-to-roles"></a><span data-ttu-id="8f024-106">ロールへのユーザーの自動割り当て</span><span class="sxs-lookup"><span data-stu-id="8f024-106">Automatically assign users to roles</span></span>
<span data-ttu-id="8f024-107">この手順では、業務データに基づいてシステム管理者がどのようにしてユーザーを自動的にロールに割り当てられるかについて説明します。</span><span class="sxs-lookup"><span data-stu-id="8f024-107">This procedure explains how system administrators can automatically assign users to roles, based on business data.</span></span> 
1. <span data-ttu-id="8f024-108">**ナビゲーション ウィンドウ > モジュール > システム管理 > セキュリティ > ユーザーをロールに割り当てる** に移動します。</span><span class="sxs-lookup"><span data-stu-id="8f024-108">Go to **Navigation pane > Modules > System administration > Security > Assign users to roles**.</span></span>
2. <span data-ttu-id="8f024-109">ツリーで、「会計監修者」を選択します。</span><span class="sxs-lookup"><span data-stu-id="8f024-109">In the tree, select 'Accounting supervisor'.</span></span> <span data-ttu-id="8f024-110">ルールを構成するロールを選択します。</span><span class="sxs-lookup"><span data-stu-id="8f024-110">Select the role that you want to configure the rule for.</span></span> <span data-ttu-id="8f024-111">この例では、会計監修者を選択します。</span><span class="sxs-lookup"><span data-stu-id="8f024-111">In this example, select Accounting supervisor.</span></span> 
3. <span data-ttu-id="8f024-112">**ルートの追加** を選択して、ダイアログ メニューを開きます。</span><span class="sxs-lookup"><span data-stu-id="8f024-112">Select **Add rule** to open the dialog menu.</span></span>
4. <span data-ttu-id="8f024-113">**クエリの選択** 一覧で、目的のレコードを見つけ、選択します。</span><span class="sxs-lookup"><span data-stu-id="8f024-113">In the **Select a query** list, find and select the desired record.</span></span> <span data-ttu-id="8f024-114">このルールを使用するには、クエリを選択します。</span><span class="sxs-lookup"><span data-stu-id="8f024-114">Select the query to use for this rule.</span></span>  
5. <span data-ttu-id="8f024-115">**メンバーシップ ルール名** 一覧で、選択された行のリンクをクリックします。</span><span class="sxs-lookup"><span data-stu-id="8f024-115">In the **Membership rule name** list, click the link in the selected row.</span></span>
6. <span data-ttu-id="8f024-116">**クエリの編集** を選択します。</span><span class="sxs-lookup"><span data-stu-id="8f024-116">Select **Edit query**.</span></span> <span data-ttu-id="8f024-117">必要に応じてクエリを編集します。</span><span class="sxs-lookup"><span data-stu-id="8f024-117">Edit the query, as needed.</span></span>  
7. <span data-ttu-id="8f024-118">**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="8f024-118">Select **OK**.</span></span>
8. <span data-ttu-id="8f024-119">**自動ロール割り当ての実行** を選択します。</span><span class="sxs-lookup"><span data-stu-id="8f024-119">Select **Run automatic role assignment**.</span></span>
9. <span data-ttu-id="8f024-120">ナビゲーション ウィンドウ **> モジュール > システム管理 > ユーザー > ユーザー** の順に進みます (別のブラウザー タブで行うことが望ましい)。</span><span class="sxs-lookup"><span data-stu-id="8f024-120">Go to **Navigation pane > Modules > System administration > Users > Users** (ideally in a separate browser tab).</span></span>
10. <span data-ttu-id="8f024-121">さまざまなユーザーに割り当てられているロールを確認して、ロール割り当てクエリが正しいことを確認します。</span><span class="sxs-lookup"><span data-stu-id="8f024-121">Review the roles assigned to various users to confirm that the role assignment query was correct.</span></span> <span data-ttu-id="8f024-122">必要に応じて調整して再実行します。</span><span class="sxs-lookup"><span data-stu-id="8f024-122">Adjust and re-run if needed.</span></span>

## <a name="exclude-users-from-automatic-role-assignment"></a><span data-ttu-id="8f024-123">自動ロール割り当てからのユーザーの除外</span><span class="sxs-lookup"><span data-stu-id="8f024-123">Exclude users from automatic role assignment</span></span>
1. <span data-ttu-id="8f024-124">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="8f024-124">Close the page.</span></span>
2. <span data-ttu-id="8f024-125">**ナビゲーション ウィンドウ > モジュール > システム管理 > セキュリティ > ユーザーをロールに割り当てる** に移動します。</span><span class="sxs-lookup"><span data-stu-id="8f024-125">Go to **Navigation pane > Modules > System administration > Security > Assign users to roles**.</span></span>
3. <span data-ttu-id="8f024-126">ツリーで、「会計監修者」を選択します。</span><span class="sxs-lookup"><span data-stu-id="8f024-126">In the tree, select 'Accounting supervisor'.</span></span> <span data-ttu-id="8f024-127">ロールを選択します。</span><span class="sxs-lookup"><span data-stu-id="8f024-127">Select a role.</span></span> <span data-ttu-id="8f024-128">この例では、会計監修者を選択します。</span><span class="sxs-lookup"><span data-stu-id="8f024-128">For this example, select Accounting supervisor.</span></span>  
4. <span data-ttu-id="8f024-129">**ロールに割り当てられたユーザー** メニューで、**手動でのユーザーの割り当て/除外** を選択します。</span><span class="sxs-lookup"><span data-stu-id="8f024-129">In the **Users assigned to role** menu, select **Manually assign / exclude users**.</span></span>
5. <span data-ttu-id="8f024-130">**ユーザーをロールに割り当てる、またはユーザーをロールから除外する** の一覧で、選択された行をマークします。</span><span class="sxs-lookup"><span data-stu-id="8f024-130">In the **Assign users to or exclude users from role** list, mark the selected row.</span></span> <span data-ttu-id="8f024-131">ユーザーを選択します。</span><span class="sxs-lookup"><span data-stu-id="8f024-131">Select a user.</span></span>  
6. <span data-ttu-id="8f024-132">**アクション ウィンドウ** で、**ロールから除外** を選択します。</span><span class="sxs-lookup"><span data-stu-id="8f024-132">On the **Action pane**, select **Exclude from role**.</span></span>
7. <span data-ttu-id="8f024-133">**ロールから除外する** を選択して、ロールから選択したユーザーを除外できます。</span><span class="sxs-lookup"><span data-stu-id="8f024-133">Select **Exclude from role** to exclude the selected users from the role.</span></span> <span data-ttu-id="8f024-134">除外を削除するには、除外を削除するユーザーを選択して **ステータスのリセット** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="8f024-134">To remove exclusions, select the users that you want to remove exclusions for, and then click **Reset status**.</span></span> <span data-ttu-id="8f024-135">ユーザーのステータスをリセットして除外を削除すると、ユーザーのロールが再び自動的に割り当てられます。</span><span class="sxs-lookup"><span data-stu-id="8f024-135">When you remove an exclusion by resetting the user's status, the user's role is assigned automatically.</span></span> <span data-ttu-id="8f024-136">ただし、ステータスをリセットした場合、ユーザーはすぐにロールに割り当てられたり、ロールから除外されません。</span><span class="sxs-lookup"><span data-stu-id="8f024-136">However, the user is not immediately assigned to the role or excluded from the role when you reset the status.</span></span> <span data-ttu-id="8f024-137">代わりに、ユーザーは自動ロール割り当てのルールが実行される次回にロールに割り当てられたり、ロールから削除されたりします。</span><span class="sxs-lookup"><span data-stu-id="8f024-137">Instead, the user is either assigned to the role or removed from the role the next time that the rules for automatic role assignment are run.</span></span>  

## <a name="manually-assign-users-to-roles"></a><span data-ttu-id="8f024-138">ユーザーにロールを手動で割り当てる</span><span class="sxs-lookup"><span data-stu-id="8f024-138">Manually assign users to roles</span></span>
<span data-ttu-id="8f024-139">セキュリティ ロールに手動で割り当てられたユーザーは、管理者が手動で削除する必要があります。</span><span class="sxs-lookup"><span data-stu-id="8f024-139">Users who are manually assigned to security roles must also be manually removed by the administrator.</span></span> <span data-ttu-id="8f024-140">自動ロール割り当てのルールは、これらのユーザーを削除しません。</span><span class="sxs-lookup"><span data-stu-id="8f024-140">These users are not removed from roles by rules for automatic role assignment.</span></span>

1. <span data-ttu-id="8f024-141">**ナビゲーション ウィンドウ > モジュール > システム管理 > セキュリティ > ユーザーをロールに割り当てる** に移動します。</span><span class="sxs-lookup"><span data-stu-id="8f024-141">Go to **Navigation pane > Modules > System administration > Security > Assign users to roles**.</span></span>
2. <span data-ttu-id="8f024-142">**ロールに割り当てられたユーザー** メニューで、**手動でユーザーを割り当てる/除外する** を選択します。</span><span class="sxs-lookup"><span data-stu-id="8f024-142">In the tree, select a role, and in the **Users assigned to role** menu, select **Manually assign / exclude users**.</span></span>
4. <span data-ttu-id="8f024-143">**手動でユーザーを割り当てる/除外する** では、ロールが割り当てられていないユーザーが、**割り当てモード** が **なし** に設定された状態で表示され ます。</span><span class="sxs-lookup"><span data-stu-id="8f024-143">In the **Assign users to or exclude users from role**, users that have not been assigned the role are listed with the **Assignment mode** set to **None**.</span></span> <span data-ttu-id="8f024-144">ロールを割り当てる 1 人または複数のユーザーを選択します。</span><span class="sxs-lookup"><span data-stu-id="8f024-144">Select one or more users that should be assigned the role.</span></span>
5. <span data-ttu-id="8f024-145">**アクション ウィンドウ** で、**ロールに割り当てる** を選択します。</span><span class="sxs-lookup"><span data-stu-id="8f024-145">On the **Action pane**, select **Assign to role**.</span></span> <span data-ttu-id="8f024-146">**割り当てモード** は **手動** に更新され、ユーザーは新しいロールが割り当てられるようになります。</span><span class="sxs-lookup"><span data-stu-id="8f024-146">The **Assignment mode** is updated to **Manual** and the users now have a new role assigned.</span></span>


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]