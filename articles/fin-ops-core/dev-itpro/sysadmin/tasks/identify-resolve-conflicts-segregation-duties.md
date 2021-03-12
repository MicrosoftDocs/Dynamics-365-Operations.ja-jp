---
title: 職務分掌の競合の識別と解決
description: このトピックでは、職務分掌の競合の識別と解決について説明します。
author: peakerbl
manager: AnnBe
ms.date: 01/04/2021
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SysSecSegregationOfDutiesConflict, SysSecSegregationOfDutiesRule
audience: Application User
ms.reviewer: sericks
ms.search.region: Global
ms.author: peakerbl
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: deff97c7728db91089d3ea834d15de738da500fa
ms.sourcegitcommit: 316200579dd5b04ad76f276a2ed6b0f55fa8c812
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/05/2021
ms.locfileid: "4826371"
---
# <a name="identify-and-resolve-conflicts-in-segregation-of-duties"></a><span data-ttu-id="63917-103">職務分掌の競合の識別と解決</span><span class="sxs-lookup"><span data-stu-id="63917-103">Identify and resolve conflicts in segregation of duties</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="63917-104">このトピックでは、職務分掌の競合の識別と解決について説明します。</span><span class="sxs-lookup"><span data-stu-id="63917-104">This topic explains how to identify and resolve conflicts in segregation of duties.</span></span> <span data-ttu-id="63917-105">異なるユーザーが実行する必要がある職務を分割するルールを設定できます。</span><span class="sxs-lookup"><span data-stu-id="63917-105">You can set up rules to separate duties that must be performed by different users.</span></span> <span data-ttu-id="63917-106">この概念は職務分掌と呼ばれます。</span><span class="sxs-lookup"><span data-stu-id="63917-106">This concept is named segregation of duties.</span></span> <span data-ttu-id="63917-107">セキュリティ ロールの定義またはユーザーのロール割り当てがルールに違反する場合、競合がログに記録されます。</span><span class="sxs-lookup"><span data-stu-id="63917-107">When the definition of a security role or the role assignments of a user violate the rules, the conflict is logged.</span></span> <span data-ttu-id="63917-108">すべての競合は、管理者が解決する必要があります。</span><span class="sxs-lookup"><span data-stu-id="63917-108">All conflicts must be resolved by the administrator.</span></span> <span data-ttu-id="63917-109">競合を識別および解決するには、次の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="63917-109">Complete the following procedure to identify and resolve conflicts.</span></span>

<span data-ttu-id="63917-110">ルールを追加した後、既存のすべてのロールが準拠している必要があります。</span><span class="sxs-lookup"><span data-stu-id="63917-110">After a rule has been added, verify that all existing roles are compliant.</span></span> 

## <a name="verify-that-existing-roles-and-duties-comply-with-new-rules-for-segregation-of-duties"></a><span data-ttu-id="63917-111">既存のロールと職務の新しい職務分掌のルールに準拠しているかどうかの確認</span><span class="sxs-lookup"><span data-stu-id="63917-111">Verify that existing roles and duties comply with new rules for segregation of duties</span></span>
1. <span data-ttu-id="63917-112">**システム管理** > **セキュリティ** > **職務分掌**  > **職務分掌ルール** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="63917-112">Go to **System administration** > **Security** > **Segregation of duties** > **Segregation of duties rules**.</span></span>
3. <span data-ttu-id="63917-113">**職務とロールの検証** を選択します。</span><span class="sxs-lookup"><span data-stu-id="63917-113">Select **Validate duties and roles**.</span></span> <span data-ttu-id="63917-114">ロールがルールに違反している場合、ルールの名前、ロール、競合する責務の名前を示すメッセージが表示されます。</span><span class="sxs-lookup"><span data-stu-id="63917-114">If any roles violate the rules, a message is displayed that contains the name of the rule, the role, and the names of the conflicting duties.</span></span> <span data-ttu-id="63917-115">競合するロールは **セキュリティ構成** を使用して変更する必要があります。また、競合する職務を含めすることはできません。</span><span class="sxs-lookup"><span data-stu-id="63917-115">Conflicting roles must be modified using **Security configuration** and can't include conflicting duties.</span></span> <span data-ttu-id="63917-116">選択したルールに違反するロールがない場合、すべてのロールが遵守していることを示すメッセージが表示されます。</span><span class="sxs-lookup"><span data-stu-id="63917-116">If no roles violate the selected rule, a message indicates that all roles comply.</span></span>   

> [!NOTE]
> <span data-ttu-id="63917-117">この検証は、選択したルールに対するみ実行されます。</span><span class="sxs-lookup"><span data-stu-id="63917-117">The validation is only performed for the selected rule.</span></span> <span data-ttu-id="63917-118">各ルールのコンプライアンスを検証することが重要です。</span><span class="sxs-lookup"><span data-stu-id="63917-118">It is important to validate compliance for each rule.</span></span>   

<span data-ttu-id="63917-119">役割を作成または変更すると、職務分掌のルールが自動的に適用されます。</span><span class="sxs-lookup"><span data-stu-id="63917-119">When you create or modify a role, the rules for segregation of duties are automatically enforced.</span></span> <span data-ttu-id="63917-120">競合する職務をロールに割り当てすることはできません。</span><span class="sxs-lookup"><span data-stu-id="63917-120">You cannot assign conflicting duties to a role.</span></span>

<span data-ttu-id="63917-121">次に、既存のすべてのロールの割り当てが準拠している必要があります。</span><span class="sxs-lookup"><span data-stu-id="63917-121">Next, verify that all existing role assignments are compliant.</span></span>

## <a name="verify-that-user-role-assignments-comply-with-new-rules-for-segregation-of-duties"></a><span data-ttu-id="63917-122">ユーザー ロールの割り当てが職務分掌の新しいルールに準拠しているかどうかの確認</span><span class="sxs-lookup"><span data-stu-id="63917-122">Verify that user role assignments comply with new rules for segregation of duties</span></span>
1. <span data-ttu-id="63917-123">**システム管理 > セキュリティ > 職務分掌 > ユーザー ロール割り当ての遵守を確認** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="63917-123">Go to **System administration > Security > Segregation of duties > Verify compliance of user-role assignments**.</span></span>
2. <span data-ttu-id="63917-124">**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="63917-124">Select **OK**.</span></span> <span data-ttu-id="63917-125">通知には検証結果が表示されます。</span><span class="sxs-lookup"><span data-stu-id="63917-125">A notification displays the results of the validation.</span></span> <span data-ttu-id="63917-126">競合は、**職務分掌の未解決の競合** ページにも記録されます。</span><span class="sxs-lookup"><span data-stu-id="63917-126">Conflicts are logged on the **Segregation of duties unresolved conflicts** page.</span></span>   

<span data-ttu-id="63917-127">ユーザーをロールに割り当てると、職務分掌のルールが自動的に適用されます。</span><span class="sxs-lookup"><span data-stu-id="63917-127">When you assign users to roles, the rules for segregation of duties are automatically enforced.</span></span> <span data-ttu-id="63917-128">競合する職務を含むロールにユーザーを割り当てると、エラー メッセージが表示されます。</span><span class="sxs-lookup"><span data-stu-id="63917-128">If you try to assign a user to roles that contain conflicting duties, you receive an error message.</span></span> <span data-ttu-id="63917-129">その後、競合を解決するには、追加のロールの割り当てを拒否または許可する必要があります。</span><span class="sxs-lookup"><span data-stu-id="63917-129">You must then resolve the conflict by denying or allowing the additional role assignment.</span></span> <span data-ttu-id="63917-130">追加のロールは、割り当てが許可された後に割り当てられます。</span><span class="sxs-lookup"><span data-stu-id="63917-130">The additional role will be assigned after the assignment is allowed.</span></span> 

> [!NOTE]
> <span data-ttu-id="63917-131">Active Directory ドメイン グループに基づいてロールが割り当てられているユーザーの競合は検証されません。</span><span class="sxs-lookup"><span data-stu-id="63917-131">Conflicts are currently not verified for users that are assigned roles based on the Active Directory Domain groups.</span></span>

## <a name="view-and-resolve-conflicting-user-role-assignments"></a><span data-ttu-id="63917-132">競合しているユーザー ロールの割り当ての表示と解決</span><span class="sxs-lookup"><span data-stu-id="63917-132">View and resolve conflicting user role assignments</span></span>
1. <span data-ttu-id="63917-133">**システム管理** > **セキュリティ** > **職務分掌** > **職務分掌の未解決の競合** へ移動します。</span><span class="sxs-lookup"><span data-stu-id="63917-133">Go to **System administration** > **Security** > **Segregation of duties** > **Segregation of duties unresolved conflicts**.</span></span> 
2. <span data-ttu-id="63917-134">競合を選択して、次のアクションのいずれかを選択します。</span><span class="sxs-lookup"><span data-stu-id="63917-134">Select a conflict, and then select one of the following actions:</span></span> 

  - <span data-ttu-id="63917-135">**割り当てを拒否**: これにより、追加のセキュリティ ロールに対するユーザーの割り当てが拒否されます。</span><span class="sxs-lookup"><span data-stu-id="63917-135">**Deny assignment**: This will deny the assignment of the user to the additional security role.</span></span> <span data-ttu-id="63917-136">自動ロール割り当てを拒否すると、ユーザーはロールから除外としてマークされます。</span><span class="sxs-lookup"><span data-stu-id="63917-136">If you deny an automatic role assignment, the user is marked as excluded from the role.</span></span> <span data-ttu-id="63917-137">除外されたユーザーは、ロールと関連付けられているアクセス権を付与されません。また、管理者が除外を削除するまでそのユーザーをロールに割り当てることはできません。</span><span class="sxs-lookup"><span data-stu-id="63917-137">The excluded user isn't granted the access associated with the role and can't be assigned to the role until the administrator removes the exclusion.</span></span> 
-  <span data-ttu-id="63917-138">**割り当ての許可**: これは競合を上書きし、ユーザーが追加のセキュリティ ロールに割り当てられることを許可します。</span><span class="sxs-lookup"><span data-stu-id="63917-138">**Allow assignment**: This will override the conflict and allow the user to be assigned to the additional security role.</span></span> <span data-ttu-id="63917-139">競合を上書きする場合は、**上書きの理由** フィールドに理由を入力する必要があります。</span><span class="sxs-lookup"><span data-stu-id="63917-139">If you override a conflict, you must enter a reason in the **Reason for override** field.</span></span> <span data-ttu-id="63917-140">上書きされた役割の割り当てはすべて、**職務分掌の競合** ページで表示できます。</span><span class="sxs-lookup"><span data-stu-id="63917-140">All overridden role assignments can be viewed on the **Segregation of duties conflicts** page.</span></span>  

> [!NOTE]
> <span data-ttu-id="63917-141">同じユーザーについて複数の競合が表示される場合は、ユーザー レコードを選択し、**ユーザー** ページで割り当てられたロール を評価します。</span><span class="sxs-lookup"><span data-stu-id="63917-141">If several conflicts are listed for the same user, select the user record and evaluate assigned roles on the **Users** page.</span></span> <span data-ttu-id="63917-142">この競合を回避するには、各ルールを追加または変更した後で検証します。</span><span class="sxs-lookup"><span data-stu-id="63917-142">To avoid this conflict, validate each rule after it's added or modified.</span></span>
