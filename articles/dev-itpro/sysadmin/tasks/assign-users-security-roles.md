---
title: ユーザーのセキュリティ ロールへの割り当て
description: Microsoft Dynamics 365 for Finance and Operations Enterprise Edition にアクセスするには、ユーザーをセキュリティ ロールに割り当てる必要があります。
author: maertenm
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SysSecRolesEditUsers, SysSecAssignmentQueryLookup, SysQueryForm, SysSecRoleExcludeUsers
audience: Application User
ms.reviewer: margoc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: maertenm
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 55cb085bb5170aa4894a2240a12f6ca451b922fb
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/29/2019
ms.locfileid: "349955"
---
# <a name="assign-users-to-security-roles"></a><span data-ttu-id="b10ea-103">ユーザーのセキュリティ ロールへの割り当て</span><span class="sxs-lookup"><span data-stu-id="b10ea-103">Assign users to security roles</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="b10ea-104">Microsoft Dynamics 365 for Finance and Operations Enterprise Edition にアクセスするには、ユーザーをセキュリティ ロールに割り当てる必要があります。</span><span class="sxs-lookup"><span data-stu-id="b10ea-104">To access Microsoft Dynamics 365 for Finance and Operations, Enterprise edition, users must be assigned to security roles.</span></span> <span data-ttu-id="b10ea-105">この手順では、業務データに基づいてシステム管理者がどのようにしてユーザーを自動的にロールに割り当てられるかについて説明します。</span><span class="sxs-lookup"><span data-stu-id="b10ea-105">This procedure explains how system administrators can assign users to roles automatically, based on business data.</span></span> <span data-ttu-id="b10ea-106">この手順の作成に使用するデモ データの会社は USMF です。</span><span class="sxs-lookup"><span data-stu-id="b10ea-106">The demo data company used to create this procedure is USMF.</span></span>


## <a name="automatically-assign-users-to-roles"></a><span data-ttu-id="b10ea-107">ロールへのユーザーの自動割り当て</span><span class="sxs-lookup"><span data-stu-id="b10ea-107">Automatically assign users to roles</span></span>
1. <span data-ttu-id="b10ea-108">[システム管理] > [セキュリティ] > [ユーザーをロールに割り当てる] に移動します。</span><span class="sxs-lookup"><span data-stu-id="b10ea-108">Go to System administration > Security > Assign users to roles.</span></span>
2. <span data-ttu-id="b10ea-109">ツリーで、「会計監修者」を選択します。</span><span class="sxs-lookup"><span data-stu-id="b10ea-109">In the tree, select 'Accounting supervisor'.</span></span>
    * <span data-ttu-id="b10ea-110">ルールを構成するロールを選択します。</span><span class="sxs-lookup"><span data-stu-id="b10ea-110">Select the role that you want to configure the rule for.</span></span> <span data-ttu-id="b10ea-111">この例では、会計監修者を選択します。</span><span class="sxs-lookup"><span data-stu-id="b10ea-111">In this example, select Accounting supervisor.</span></span>  
3. <span data-ttu-id="b10ea-112">[ルールの追加] をクリックして、ドロップ ダイアログを開きます。</span><span class="sxs-lookup"><span data-stu-id="b10ea-112">Click Add rule to open the drop dialog.</span></span>
4. <span data-ttu-id="b10ea-113">一覧で、目的のレコードを見つけ、選択します。</span><span class="sxs-lookup"><span data-stu-id="b10ea-113">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="b10ea-114">このルールを使用するには、クエリを選択します。</span><span class="sxs-lookup"><span data-stu-id="b10ea-114">Select the query to use for this rule.</span></span>  
5. <span data-ttu-id="b10ea-115">一覧で、選択された行のリンクをクリックします。</span><span class="sxs-lookup"><span data-stu-id="b10ea-115">In the list, click the link in the selected row.</span></span>
6. <span data-ttu-id="b10ea-116">[クエリの編集] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="b10ea-116">Click Edit query.</span></span>
    * <span data-ttu-id="b10ea-117">必要に応じてクエリを編集します。</span><span class="sxs-lookup"><span data-stu-id="b10ea-117">Edit the query, as needed.</span></span>  
7. <span data-ttu-id="b10ea-118">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="b10ea-118">Click OK.</span></span>

## <a name="exclude-users-from-automatic-role-assignment"></a><span data-ttu-id="b10ea-119">自動ロール割り当てからのユーザーの除外</span><span class="sxs-lookup"><span data-stu-id="b10ea-119">Exclude users from automatic role assignment</span></span>
1. <span data-ttu-id="b10ea-120">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="b10ea-120">Close the page.</span></span>
2. <span data-ttu-id="b10ea-121">[システム管理] > [セキュリティ] > [ユーザーをロールに割り当てる] に移動します。</span><span class="sxs-lookup"><span data-stu-id="b10ea-121">Go to System administration > Security > Assign users to roles.</span></span>
3. <span data-ttu-id="b10ea-122">ツリーで、「会計監修者」を選択します。</span><span class="sxs-lookup"><span data-stu-id="b10ea-122">In the tree, select 'Accounting supervisor'.</span></span>
    * <span data-ttu-id="b10ea-123">ロールを選択します。</span><span class="sxs-lookup"><span data-stu-id="b10ea-123">Select a role.</span></span> <span data-ttu-id="b10ea-124">この例では、会計監修者を選択します。</span><span class="sxs-lookup"><span data-stu-id="b10ea-124">For this example, select Accounting supervisor.</span></span>  
4. <span data-ttu-id="b10ea-125">[手動でのユーザーの割り当て/除外] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="b10ea-125">Click Manually assign / exclude users.</span></span>
5. <span data-ttu-id="b10ea-126">一覧で、選択された行をマークします。</span><span class="sxs-lookup"><span data-stu-id="b10ea-126">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="b10ea-127">ユーザーを選択します。</span><span class="sxs-lookup"><span data-stu-id="b10ea-127">Select a user.</span></span>  
6. <span data-ttu-id="b10ea-128">[ロールから除外] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="b10ea-128">Click Exclude from role.</span></span>
    * <span data-ttu-id="b10ea-129">[ロールから除外] をクリックして、ロールから選択したユーザーを除外できます。</span><span class="sxs-lookup"><span data-stu-id="b10ea-129">Click Exclude from role to exclude the selected users from the role.</span></span> <span data-ttu-id="b10ea-130">除外を削除するには、除外を削除するユーザーを選択して [ステータスのリセット] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="b10ea-130">To remove exclusions, select the users that you want to remove exclusions for, and then click Reset status.</span></span> <span data-ttu-id="b10ea-131">ユーザーのステータスをリセットして除外を削除した場合、ユーザーのロールが再度自動的に割り当てられます。</span><span class="sxs-lookup"><span data-stu-id="b10ea-131">When you remove an exclusion by resetting the user’s status, the user’s role is again assigned automatically.</span></span> <span data-ttu-id="b10ea-132">ただし、ステータスをリセットした場合、ユーザーはすぐにロールに割り当てられたり、ロールから除外されません。</span><span class="sxs-lookup"><span data-stu-id="b10ea-132">However, the user is not immediately assigned to the role or excluded from the role when you reset the status.</span></span> <span data-ttu-id="b10ea-133">代わりに、ユーザーは自動ロール割り当てのルールが実行される次回にロールに割り当てられたり、ロールから削除されたりします。</span><span class="sxs-lookup"><span data-stu-id="b10ea-133">Instead, the user is either assigned to the role or removed from the role the next time that the rules for automatic role assignment are run.</span></span>  

