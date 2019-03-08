---
title: 職務分掌の競合の識別と解決
description: 異なるユーザーが実行する必要があるタスクを分割するルールを設定できます。
author: maertenm
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SysSecSegregationOfDutiesConflict, SysSecSegregationOfDutiesRule
audience: Application User
ms.reviewer: margoc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: maertenm
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 9d4a6bd14090213cc19a072d030bc26886c7a8d0
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/29/2019
ms.locfileid: "353106"
---
# <a name="identify-and-resolve-conflicts-in-segregation-of-duties"></a><span data-ttu-id="c5d97-103">職務分掌の競合の識別と解決</span><span class="sxs-lookup"><span data-stu-id="c5d97-103">Identify and resolve conflicts in segregation of duties</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="c5d97-104">異なるユーザーが実行する必要があるタスクを分割するルールを設定できます。</span><span class="sxs-lookup"><span data-stu-id="c5d97-104">You can set up rules to separate tasks that must be performed by different users.</span></span> <span data-ttu-id="c5d97-105">この概念は職務分掌と呼ばれます。</span><span class="sxs-lookup"><span data-stu-id="c5d97-105">This concept is named segregation of duties.</span></span> <span data-ttu-id="c5d97-106">セキュリティ ロールの定義またはユーザーのロール割り当てがルールに違反する場合、競合がログに記録されます。</span><span class="sxs-lookup"><span data-stu-id="c5d97-106">When the definition of a security role or the role assignments of a user violate the rules, the conflict is logged.</span></span> <span data-ttu-id="c5d97-107">すべての競合は、管理者が解決する必要があります。</span><span class="sxs-lookup"><span data-stu-id="c5d97-107">All conflicts must be resolved by the administrator.</span></span> <span data-ttu-id="c5d97-108">競合を識別および解決するには、次の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="c5d97-108">Complete the following procedure to identify and resolve conflicts.</span></span> <span data-ttu-id="c5d97-109">この手順の作成に使用するデモ データの会社は USMF です。</span><span class="sxs-lookup"><span data-stu-id="c5d97-109">The demo data company used to create this procedure is USMF.</span></span>


## <a name="verify-whether-user-role-assignments-comply-with-new-rules-for-segregation-of-duties"></a><span data-ttu-id="c5d97-110">ユーザー ロールの割り当てが職務分掌の新しいルールに準拠しているかどうかの確認</span><span class="sxs-lookup"><span data-stu-id="c5d97-110">Verify whether user role assignments comply with new rules for segregation of duties</span></span>
1. <span data-ttu-id="c5d97-111">[システム管理] > [セキュリティ] > [職務分掌] > [ユーザー ロール割り当ての遵守を確認] の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="c5d97-111">Go to System administration > Security > Segregation of duties > Verify compliance of user-role assignments.</span></span>
2. <span data-ttu-id="c5d97-112">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="c5d97-112">Click OK.</span></span>
    * <span data-ttu-id="c5d97-113">通知には検証結果が表示されます。</span><span class="sxs-lookup"><span data-stu-id="c5d97-113">A notification displays the results of the validation.</span></span>     <span data-ttu-id="c5d97-114">競合がある場合は、[ユーザー] ページを開き、ユーザーのロールの割り当てを変更できます。</span><span class="sxs-lookup"><span data-stu-id="c5d97-114">If there is a conflict, you can open the Users page and change the user’s role assignments.</span></span> <span data-ttu-id="c5d97-115">また、競合は、[職務分掌の競合] ページでログに記録されます。</span><span class="sxs-lookup"><span data-stu-id="c5d97-115">Conflicts are also logged on the Segregation of duties conflicts page.</span></span>     <span data-ttu-id="c5d97-116">検証プロセスをバッチ ジョブとして実行するには、バッチ処理を選択し、その他のバッチ パラメーターを設定します。</span><span class="sxs-lookup"><span data-stu-id="c5d97-116">To run the verification process as a batch job, select Batch processing, and then set the other batch parameters.</span></span> <span data-ttu-id="c5d97-117">バッチ ジョブの実行後、[職務分掌の競合] ページで競合を確認できます。</span><span class="sxs-lookup"><span data-stu-id="c5d97-117">After the batch job runs, you can review the conflicts in the Segregation of duties conflicts page.</span></span>  

## <a name="view-and-resolve-conflicting-user-role-assignments"></a><span data-ttu-id="c5d97-118">競合しているユーザー ロールの割り当ての表示と解決</span><span class="sxs-lookup"><span data-stu-id="c5d97-118">View and resolve conflicting user role assignments</span></span>
1. <span data-ttu-id="c5d97-119">[システム管理] > [セキュリティ] > [職務分掌] > [職務分掌の競合] の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="c5d97-119">Go to System administration > Security > Segregation of duties > Segregation of duties conflicts.</span></span>
    * <span data-ttu-id="c5d97-120">競合を選択し、次のボタンの 1 つをクリックします。[割り当ての拒否] – 追加したセキュリティ ロールへのユーザーの割り当てを拒否します。</span><span class="sxs-lookup"><span data-stu-id="c5d97-120">Select a conflict, and then click one of the following buttons:     Deny assignment – Deny the assignment of the user to the additional security role.</span></span> <span data-ttu-id="c5d97-121">自動ロール割り当てを拒否すると、ユーザーはロールから除外としてマークされます。</span><span class="sxs-lookup"><span data-stu-id="c5d97-121">If you deny an automatic role assignment, the user is marked as excluded from the role.</span></span> <span data-ttu-id="c5d97-122">除外されたユーザーは、ロールと関連付けられているアクセス権を付与されません。また、管理者が除外を削除するまでそのユーザーをロールに割り当てることはできません。</span><span class="sxs-lookup"><span data-stu-id="c5d97-122">The excluded user is not granted the access that is associated with the role, and the user cannot be assigned to the role until the administrator removes the exclusion.</span></span>     <span data-ttu-id="c5d97-123">[割り当ての許可] – 競合を上書きし、ユーザーが両方のセキュリティ ロールに割り当てられることを許可します。</span><span class="sxs-lookup"><span data-stu-id="c5d97-123">Allow assignment – Override the conflict, and allow the user to be assigned to both security roles.</span></span> <span data-ttu-id="c5d97-124">競合を上書きする場合は、[上書きの理由] フィールドに理由を入力する必要があります。</span><span class="sxs-lookup"><span data-stu-id="c5d97-124">If you override a conflict, you must enter a reason in the Reason for override field.</span></span>  
2. <span data-ttu-id="c5d97-125">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="c5d97-125">Close the page.</span></span>
3. <span data-ttu-id="c5d97-126">[システム管理] > [セキュリティ] > [職務分掌] > [職務分掌による未解決の競合] の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="c5d97-126">Go to System administration > Security > Segregation of duties > Segregation of duties unresolved conflicts.</span></span>
    * <span data-ttu-id="c5d97-127">競合を選択し、次のボタンの 1 つをクリックします。[割り当ての拒否] – 追加したセキュリティ ロールへのユーザーの割り当てを拒否します。</span><span class="sxs-lookup"><span data-stu-id="c5d97-127">Select a conflict, and then click one of the following buttons:     Deny assignment – Deny the assignment of the user to the additional security role.</span></span> <span data-ttu-id="c5d97-128">自動ロール割り当てを拒否すると、ユーザーはロールから除外としてマークされます。</span><span class="sxs-lookup"><span data-stu-id="c5d97-128">If you deny an automatic role assignment, the user is marked as excluded from the role.</span></span> <span data-ttu-id="c5d97-129">除外されたユーザーは、ロールと関連付けられているアクセス権を付与されません。また、管理者が除外を削除するまでそのユーザーをロールに割り当てることはできません。</span><span class="sxs-lookup"><span data-stu-id="c5d97-129">The excluded user is not granted the access that is associated with the role, and the user cannot be assigned to the role until the administrator removes the exclusion.</span></span>     <span data-ttu-id="c5d97-130">[割り当ての許可] – 競合を上書きし、ユーザーが両方のセキュリティ ロールに割り当てられることを許可します。</span><span class="sxs-lookup"><span data-stu-id="c5d97-130">Allow assignment – Override the conflict, and allow the user to be assigned to both security roles.</span></span> <span data-ttu-id="c5d97-131">競合を上書きする場合は、[上書きの理由] フィールドに理由を入力する必要があります。</span><span class="sxs-lookup"><span data-stu-id="c5d97-131">If you override a conflict, you must enter a reason in the Reason for override field.</span></span>    
4. <span data-ttu-id="c5d97-132">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="c5d97-132">Close the page.</span></span>

## <a name="verify-whether-existing-roles-comply-with-new-rules-for-segregation-of-duties"></a><span data-ttu-id="c5d97-133">既存のロールが職務分掌の新しいルールに準拠しているかどうかの確認</span><span class="sxs-lookup"><span data-stu-id="c5d97-133">Verify whether existing roles comply with new rules for segregation of duties</span></span>
1. <span data-ttu-id="c5d97-134">[システム管理] > [セキュリティ] > [職務分掌] > [職務分掌ルール] の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="c5d97-134">Go to System administration > Security > Segregation of duties > Segregation of duties rules.</span></span>
    * <span data-ttu-id="c5d97-135">ルールを選択します。</span><span class="sxs-lookup"><span data-stu-id="c5d97-135">Select a rule.</span></span>  
2. <span data-ttu-id="c5d97-136">[職務とロールの検証] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="c5d97-136">Click Validate duties and roles.</span></span>
    * <span data-ttu-id="c5d97-137">既存のロールが選択したルールに違反している場合、ロールの名前と競合する職務を示すメッセージが表示されます。</span><span class="sxs-lookup"><span data-stu-id="c5d97-137">If any existing roles violate the selected rule, a message is displayed that contains the name of the role and the names of the conflicting duties.</span></span> <span data-ttu-id="c5d97-138">管理者は、職務分掌のルールに違反しないように、セキュリティ リスクの軽減策を示すか、ロールの変更をする必要があります。</span><span class="sxs-lookup"><span data-stu-id="c5d97-138">The administrator must either indicate the mitigation for the security risk or modify the role so that it does not violate the rules for segregation of duties.</span></span>     <span data-ttu-id="c5d97-139">選択したルールに違反するロールがない場合、すべてのロールがルールに遵守していることを示すメッセージが表示されます。</span><span class="sxs-lookup"><span data-stu-id="c5d97-139">If no roles violate the selected rule, a message indicates that all roles are in compliance.</span></span>  

