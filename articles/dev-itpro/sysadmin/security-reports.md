---
title: "すぐに使えるセキュリティ レポート"
description: "Dynamics 365 for Finance and Operations では、環境内で実行されている一連のセキュリティ ロールと、各ロールに割り当てられている一連のユーザーを理解するのに役立つ豊富なセキュリティ レポートが用意されています。"
author: maertenm
manager: AnnBe
ms.date: 06/23/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
ms.search.form: SysSecConfiguration, SrsReportViewerForm
audience: IT Pro
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: maertenm
ms.search.validFrom: 2017-06-30
ms.dyn365.ops.version: Platform update 8
ms.translationtype: HT
ms.sourcegitcommit: e782d33f3748524491dace28008cd9148ae70529
ms.openlocfilehash: 55abffcc0f9f40289fca156ed53021da50c3a91b
ms.contentlocale: ja-jp
ms.lasthandoff: 08/09/2018

---

# <a name="out-of-box-security-reports"></a><span data-ttu-id="01886-103">すぐに使えるセキュリティ レポート</span><span class="sxs-lookup"><span data-stu-id="01886-103">Out-of-box security reports</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="01886-104">Dynamics 365 for Finance and Operations では、環境内で実行されている一連のセキュリティ ロールと、各ロールに割り当てられている一連のユーザーを理解するのに役立つ豊富なセキュリティ レポートが用意されています。</span><span class="sxs-lookup"><span data-stu-id="01886-104">Dynamics 365 for Finance and Operations provides a set of rich security reports to help you understand the set of security roles running in your environment and the set of users assigned to each role.</span></span> <span data-ttu-id="01886-105">これらのレポートはそれぞれ、下位の **System administration \> Inquiries \> Security.** にあります。</span><span class="sxs-lookup"><span data-stu-id="01886-105">Each of these reports can be found under **System administration \> Inquiries \> Security.**</span></span> <span data-ttu-id="01886-106">各レポートの説明は下で用意されています。</span><span class="sxs-lookup"><span data-stu-id="01886-106">A description of each report is provided below.</span></span>

<a name="user-role-assignments"></a><span data-ttu-id="01886-107">ユーザー ロールの割り当て</span><span class="sxs-lookup"><span data-stu-id="01886-107">User role assignments</span></span>
----------------------------

<span data-ttu-id="01886-108">**ユーザー ロールの割り当て** レポートは、システムにおける現在のユーザー ロールの割り当てのビューを生成します。</span><span class="sxs-lookup"><span data-stu-id="01886-108">The **User role assignments** report generates a view of the current user role assignments in your system.</span></span> <span data-ttu-id="01886-109">既定では、ロールが割り当てられているすべてのユーザーがレポートに含まれます。</span><span class="sxs-lookup"><span data-stu-id="01886-109">By default, the report includes all users with roles assigned.</span></span> <span data-ttu-id="01886-110">必要に応じて、レポートを生成するときにユーザーのリストを入力することによって、レポートを特定のユーザーのセットに限定することができます。</span><span class="sxs-lookup"><span data-stu-id="01886-110">You can optionally limit the report to a specific set of users by entering a list of users when generating the report.</span></span> <span data-ttu-id="01886-111">**ユーザー ロールの割り当て**パラメータ ウィンドウで、**対象に含めるレコード** > **フィルター**に移動します。</span><span class="sxs-lookup"><span data-stu-id="01886-111">On the **User role assignments** parameters pane, go to **Records to include** > **Filter.**</span></span> <span data-ttu-id="01886-112">ここから、レポートが生成されるユーザーのリストに対してフィルターを追加または削除できます。</span><span class="sxs-lookup"><span data-stu-id="01886-112">From here you can add or remove filters to the list of users the report will be generated for.</span></span>

![ユーザー ロールの割り当て](media/User-role-assignments.PNG)

<span data-ttu-id="01886-114">レポート内の各ユーザーに対して、法人または組織レベルで任意の制限と共に、ロールの一覧が提供されます。</span><span class="sxs-lookup"><span data-stu-id="01886-114">For each user in the report a list of roles is provided, along with any restrictions at the legal entity or organization level.</span></span>

<a name="role-to-user-assignments"></a><span data-ttu-id="01886-115">ユーザーへのロールの割り当て</span><span class="sxs-lookup"><span data-stu-id="01886-115">Role to user assignments</span></span> 
-------------------------

<span data-ttu-id="01886-116">**ユーザーへのロールの割り当て** レポートは、ロールの割り当ての集計を提供します。</span><span class="sxs-lookup"><span data-stu-id="01886-116">The **Role to user assignment** report provides an aggregation of role assignments.</span></span> <span data-ttu-id="01886-117">レポートのロールを展開すると、ロールに割り当てられたユーザーの一覧が表示され、ユーザー名を展開すると、ロールが適用された制限が表示されます。</span><span class="sxs-lookup"><span data-stu-id="01886-117">Expanding a role in the report shows the list of users assigned to the role, and expanding the user name shows any restrictions the role has applied.</span></span> <span data-ttu-id="01886-118">**ユーザー ロールの割り当て**レポートで説明したように、ユーザーのセットをフィルタリングするのと同じ方法をこのレポートに適用できます。</span><span class="sxs-lookup"><span data-stu-id="01886-118">The same method for filtering the set of users can be applied to this report as described for the **User role assignments** report.</span></span>

![ユーザーへのロールの割り当て](media/role-to-user-assignments.png)

<a name="security-role-access"></a><span data-ttu-id="01886-120">セキュリティ ロール アクセス</span><span class="sxs-lookup"><span data-stu-id="01886-120">Security role access</span></span>
--------------------

<span data-ttu-id="01886-121">**セキュリティ ロールのアクセス権** レポートには、各セキュリティ ロールの有効なアクセス許可が表示されます。</span><span class="sxs-lookup"><span data-stu-id="01886-121">The **Security role access** report provides a view of the effective permissions for each security role.</span></span> <span data-ttu-id="01886-122">このレポートには、ロールに含まれるすべてのサブロール、職務、および権限全体にタイプごとにグループ化された権限のフラット化されたリストが表示されます。</span><span class="sxs-lookup"><span data-stu-id="01886-122">This report provides a flattened list of permissions grouped by type across all sub-roles, duties, and privileges contained in the role.</span></span>

<span data-ttu-id="01886-123">**セキュリティ ロール アクセス** レポートをバックアップしているデータ セットは非常に大きく、レポートの実行に時間がかかることがあります。</span><span class="sxs-lookup"><span data-stu-id="01886-123">The data set backing the **Security role access** report can be very large, causing the report to take some time to run.</span></span> <span data-ttu-id="01886-124">前回レポートが実行されてからセキュリティ ロールへの変更がなかった場合は、レポート パラメーター ウィンドウの**コレクションを再構築**オプションを**いいえ**に設定すると、レポート構築がスキップされます。</span><span class="sxs-lookup"><span data-stu-id="01886-124">If there have been no changes to security roles since the last time the report was run, you can skip building the report by setting the **Rebuild collection** option to **No** on the report parameters pane.</span></span> <span data-ttu-id="01886-125">これにより、既存のデータ セットからのレポートがレンダリングされます。</span><span class="sxs-lookup"><span data-stu-id="01886-125">This will render the report from the existing data set.</span></span> <span data-ttu-id="01886-126">レポートの実行が初めてである場合、または役割の定義が変更される可能性が場合、**コレクションの再構築**オプションを**はい**に設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="01886-126">If it is the first time the report has run, or there could be changes to the role definitions, the **Rebuild collection** option should be set to **Yes**.</span></span> <span data-ttu-id="01886-127">必要に応じて、**対象に含めるレコード** の下にフィルターを追加することにより、ロールをレポートに含めるように制限することができます。</span><span class="sxs-lookup"><span data-stu-id="01886-127">You can optionally limit the roles to be included in the report by adding a filter under **Records to include**.</span></span>

![セキュリティ ロール アクセス](media/security-role-access.png)

<span data-ttu-id="01886-129">ロールを展開すると、ロールがアクセスできるオブジェクトのカテゴリが表示されます。</span><span class="sxs-lookup"><span data-stu-id="01886-129">Expanding a role shows the category of objects the role has access to.</span></span> <span data-ttu-id="01886-130">オブジェクトタイプの 1 つを展開すると、ロールに含まれるタイプの各オブジェクトの詳細なリストが表示されます。</span><span class="sxs-lookup"><span data-stu-id="01886-130">Expanding one of the object types will show a detailed list of each object of that type included in the role.</span></span>

<a name="security-duty-assignments"></a><span data-ttu-id="01886-131">セキュリティ職務権限の割り当て</span><span class="sxs-lookup"><span data-stu-id="01886-131">Security duty assignments</span></span>
-------------------------

<span data-ttu-id="01886-132">**セキュリティ職務権限割り当て** レポートには、ロール内に含まれるすべての職務権限のビューが表示されます。</span><span class="sxs-lookup"><span data-stu-id="01886-132">The **Security duty assignments** report provides a view of all the duties contained within a role.</span></span> <span data-ttu-id="01886-133">このレポートは、任意の役割のコレクションで実行されるように構成され、職務分掌が役割間で確実に維持されます。</span><span class="sxs-lookup"><span data-stu-id="01886-133">This report can be configured to run on any collection of roles to ensure that segregation of duties is maintained between roles.</span></span> <span data-ttu-id="01886-134">既定では、すべてのロールがレポートに含まれます。</span><span class="sxs-lookup"><span data-stu-id="01886-134">By default, the report will include all roles.</span></span> <span data-ttu-id="01886-135">含まれるロールを制限するには、**含めるレコード** セクションに記載されているフィルタ処理を活用します。</span><span class="sxs-lookup"><span data-stu-id="01886-135">To limit the roles included, leverage the filtering provided in the **Records to include** section.</span></span>

![セキュリティ職務権限の割り当て](media/security-duty-assignments.png)

<span data-ttu-id="01886-137">**セキュリティ職務権限割り当て**レポートのロール展開では、役割に割り当てられた各職務権限および職務権限の詳細が表示されます。</span><span class="sxs-lookup"><span data-stu-id="01886-137">Expanding a role in the **Security duty assignments** report will show each duty assigned to the role, along with details of the duty.</span></span>

## <a name="batch-processing-of-reports"></a><span data-ttu-id="01886-138">レポートのバッチ処理</span><span class="sxs-lookup"><span data-stu-id="01886-138">Batch processing of reports</span></span>
<span data-ttu-id="01886-139">上記のレポートのいずれかを、バッチ ジョブとして実行するように設定するには、レポートのパラメータ ウィンドウの**バックグラウンドで実行**セクションに移動します。</span><span class="sxs-lookup"><span data-stu-id="01886-139">Any of the above reports can be set to run as a batch job by going to the **Run in the background** section of the report's parameter pane.</span></span> <span data-ttu-id="01886-140">**バッチ処理** を **はい** に設定し、バッチ タスクジョブ名、バッチ グループ、ジョブをプライベートまたは重大なとして実行するかどうかを指定します。</span><span class="sxs-lookup"><span data-stu-id="01886-140">Set **Batch processing** to **Yes**, then provide a batch task job name, batch group, and whether the job should run as Private or Critical.</span></span> <span data-ttu-id="01886-141">バッチ タスクが実行されると、レポートが作成されます。</span><span class="sxs-lookup"><span data-stu-id="01886-141">The report will then be created when the batch task runs.</span></span>

![レポートのバッチ処理](media/a6142c903497381171bf6c6b27495895.png)


