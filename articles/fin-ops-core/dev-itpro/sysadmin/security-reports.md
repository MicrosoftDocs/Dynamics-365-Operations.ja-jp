---
title: 最初から用意されているセキュリティ レポート
description: このトピックでは、環境内で実行されている一連のセキュリティ ロールと、各ロールに割り当てられているユーザーを理解するのに役立つセキュリティ レポートについて説明します。
author: peakerbl
ms.date: 08/14/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: SysSecConfiguration, SrsReportViewerForm
audience: IT Pro
ms.reviewer: sericks
ms.search.region: Global
ms.author: peakerbl
ms.search.validFrom: 2017-06-30
ms.dyn365.ops.version: Platform update 8
ms.openlocfilehash: 276e4832547296bb2023473710644092600c7bb3
ms.sourcegitcommit: ff09736563d3cd2bc74c7664edd1767b218401cb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/04/2021
ms.locfileid: "6189230"
---
# <a name="out-of-box-security-reports"></a><span data-ttu-id="33b1a-103">最初から用意されているセキュリティ レポート</span><span class="sxs-lookup"><span data-stu-id="33b1a-103">Out-of-box security reports</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="33b1a-104">Finance and Operations では、環境内で実行されている一連のセキュリティ ロールと、各ロールに割り当てられている一連のユーザーを理解するのに役立つ豊富なセキュリティ レポートが用意されています。</span><span class="sxs-lookup"><span data-stu-id="33b1a-104">Finance and Operations provides a set of rich security reports to help you understand the set of security roles running in your environment and the set of users assigned to each role.</span></span> <span data-ttu-id="33b1a-105">このトピックで説明するレポートに加えて、開発者は、すべてのロールの **Visual Studio  > Dynamics 365 > アドイン > 表示 関連のオブジェクトおよびライセンス** を使用して、すべてのロールで使用できるすべてのユーザー セキュリティ特権がすべての含まれたブックを生成できます。</span><span class="sxs-lookup"><span data-stu-id="33b1a-105">In addition to the reports noted in this topic, developers can generate a workbook containing all user security privileges for all roles using **Visual Studio > Dynamics 365 > Addins > View related objects and licenses for all roles**.</span></span>

<span data-ttu-id="33b1a-106">これらのセキュリティ レポートはそれぞれ、 **システム管理 \> 照会 \> セキュリティ** で見つかる場合があります。</span><span class="sxs-lookup"><span data-stu-id="33b1a-106">Each of the security reports can be found under **System administration \> Inquiries \> Security.**</span></span> <span data-ttu-id="33b1a-107">各レポートの説明は下で用意されています。</span><span class="sxs-lookup"><span data-stu-id="33b1a-107">A description of each report is provided below.</span></span>

## <a name="user-role-assignments"></a><span data-ttu-id="33b1a-108">ユーザー ロールの割り当て</span><span class="sxs-lookup"><span data-stu-id="33b1a-108">User role assignments</span></span>

<span data-ttu-id="33b1a-109">**ユーザー ロールの割り当て** レポートは、システムにおける現在のユーザー ロールの割り当てのビューを生成します。</span><span class="sxs-lookup"><span data-stu-id="33b1a-109">The **User role assignments** report generates a view of the current user role assignments in your system.</span></span> <span data-ttu-id="33b1a-110">既定では、ロールが割り当てられているすべてのユーザーがレポートに含まれます。</span><span class="sxs-lookup"><span data-stu-id="33b1a-110">By default, the report includes all users with roles assigned.</span></span> <span data-ttu-id="33b1a-111">必要に応じて、レポートを生成するときにユーザーのリストを入力することによって、レポートを特定のユーザーのセットに限定することができます。</span><span class="sxs-lookup"><span data-stu-id="33b1a-111">You can optionally limit the report to a specific set of users by entering a list of users when generating the report.</span></span> <span data-ttu-id="33b1a-112">**ユーザー ロールの割り当て** パラメータ ウィンドウで、**対象に含めるレコード** > **フィルター** に移動します。</span><span class="sxs-lookup"><span data-stu-id="33b1a-112">On the **User role assignments** parameters pane, go to **Records to include** > **Filter.**</span></span> <span data-ttu-id="33b1a-113">ここから、レポートが生成されるユーザーのリストに対してフィルターを追加または削除できます。</span><span class="sxs-lookup"><span data-stu-id="33b1a-113">From here you can add or remove filters to the list of users the report will be generated for.</span></span>

![ユーザー ロールの割り当て](media/User-role-assignments.PNG)

<span data-ttu-id="33b1a-115">レポート内の各ユーザーに対して、法人または組織レベルで任意の制限と共に、ロールの一覧が提供されます。</span><span class="sxs-lookup"><span data-stu-id="33b1a-115">For each user in the report a list of roles is provided, along with any restrictions at the legal entity or organization level.</span></span>

## <a name="role-to-user-assignments"></a><span data-ttu-id="33b1a-116">ユーザーへのロールの割り当て</span><span class="sxs-lookup"><span data-stu-id="33b1a-116">Role to user assignments</span></span> 

<span data-ttu-id="33b1a-117">**ユーザーへのロールの割り当て** レポートは、ロールの割り当ての集計を提供します。</span><span class="sxs-lookup"><span data-stu-id="33b1a-117">The **Role to user assignment** report provides an aggregation of role assignments.</span></span> <span data-ttu-id="33b1a-118">レポートのロールを展開すると、ロールに割り当てられたユーザーの一覧が表示され、ユーザー名を展開すると、ロールが適用された制限が表示されます。</span><span class="sxs-lookup"><span data-stu-id="33b1a-118">Expanding a role in the report shows the list of users assigned to the role, and expanding the user name shows any restrictions the role has applied.</span></span> <span data-ttu-id="33b1a-119">**ユーザー ロールの割り当て** レポートで説明したように、ユーザーのセットをフィルタリングするのと同じ方法をこのレポートに適用できます。</span><span class="sxs-lookup"><span data-stu-id="33b1a-119">The same method for filtering the set of users can be applied to this report as described for the **User role assignments** report.</span></span>

![ユーザーへのロールの割り当て](media/role-to-user-assignments.png)

## <a name="security-role-access"></a><span data-ttu-id="33b1a-121">セキュリティ ロール アクセス</span><span class="sxs-lookup"><span data-stu-id="33b1a-121">Security role access</span></span>

<span data-ttu-id="33b1a-122">**セキュリティ ロールのアクセス権** レポートには、各セキュリティ ロールの有効なアクセス許可が表示されます。</span><span class="sxs-lookup"><span data-stu-id="33b1a-122">The **Security role access** report provides a view of the effective permissions for each security role.</span></span> <span data-ttu-id="33b1a-123">このレポートには、ロールに含まれるすべてのサブロール、職務、および権限全体にタイプごとにグループ化された権限のフラット化されたリストが表示されます。</span><span class="sxs-lookup"><span data-stu-id="33b1a-123">This report provides a flattened list of permissions grouped by type across all sub-roles, duties, and privileges contained in the role.</span></span>

<span data-ttu-id="33b1a-124">**セキュリティ ロール アクセス** レポートをバックアップしているデータ セットは非常に大きく、レポートの実行に時間がかかることがあります。</span><span class="sxs-lookup"><span data-stu-id="33b1a-124">The data set backing the **Security role access** report can be very large, causing the report to take some time to run.</span></span> <span data-ttu-id="33b1a-125">前回レポートが実行されてからセキュリティ ロールへの変更がなかった場合は、レポート パラメーター ウィンドウの **コレクションを再構築** オプションを **いいえ** に設定すると、レポート構築がスキップされます。</span><span class="sxs-lookup"><span data-stu-id="33b1a-125">If there have been no changes to security roles since the last time the report was run, you can skip building the report by setting the **Rebuild collection** option to **No** on the report parameters pane.</span></span> <span data-ttu-id="33b1a-126">これにより、既存のデータ セットからのレポートがレンダリングされます。</span><span class="sxs-lookup"><span data-stu-id="33b1a-126">This will render the report from the existing data set.</span></span> <span data-ttu-id="33b1a-127">レポートの実行が初めてである場合、または役割の定義が変更される可能性が場合、**コレクションの再構築** オプションを **はい** に設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="33b1a-127">If it is the first time the report has run, or there could be changes to the role definitions, the **Rebuild collection** option should be set to **Yes**.</span></span> <span data-ttu-id="33b1a-128">必要に応じて、**対象に含めるレコード** の下にフィルターを追加することにより、ロールをレポートに含めるように制限することができます。</span><span class="sxs-lookup"><span data-stu-id="33b1a-128">You can optionally limit the roles to be included in the report by adding a filter under **Records to include**.</span></span>

![セキュリティ ロール アクセス](media/security-role-access.png)

<span data-ttu-id="33b1a-130">ロールを展開すると、ロールがアクセスできるオブジェクトのカテゴリが表示されます。</span><span class="sxs-lookup"><span data-stu-id="33b1a-130">Expanding a role shows the category of objects the role has access to.</span></span> <span data-ttu-id="33b1a-131">オブジェクトタイプの 1 つを展開すると、ロールに含まれるタイプの各オブジェクトの詳細なリストが表示されます。</span><span class="sxs-lookup"><span data-stu-id="33b1a-131">Expanding one of the object types will show a detailed list of each object of that type included in the role.</span></span>

## <a name="security-duty-assignments"></a><span data-ttu-id="33b1a-132">セキュリティ職務権限の割り当て</span><span class="sxs-lookup"><span data-stu-id="33b1a-132">Security duty assignments</span></span>

<span data-ttu-id="33b1a-133">**セキュリティ職務権限割り当て** レポートには、ロール内に含まれるすべての職務権限のビューが表示されます。</span><span class="sxs-lookup"><span data-stu-id="33b1a-133">The **Security duty assignments** report provides a view of all the duties contained within a role.</span></span> <span data-ttu-id="33b1a-134">このレポートは、任意の役割のコレクションで実行されるように構成され、職務分掌が役割間で確実に維持されます。</span><span class="sxs-lookup"><span data-stu-id="33b1a-134">This report can be configured to run on any collection of roles to ensure that segregation of duties is maintained between roles.</span></span> <span data-ttu-id="33b1a-135">既定では、すべてのロールがレポートに含まれます。</span><span class="sxs-lookup"><span data-stu-id="33b1a-135">By default, the report will include all roles.</span></span> <span data-ttu-id="33b1a-136">含まれるロールを制限するには、**含めるレコード** セクションに記載されているフィルタ処理を活用します。</span><span class="sxs-lookup"><span data-stu-id="33b1a-136">To limit the roles included, leverage the filtering provided in the **Records to include** section.</span></span>

![セキュリティ職務権限の割り当て](media/security-duty-assignments.png)

<span data-ttu-id="33b1a-138">**セキュリティ職務権限割り当て** レポートのロール展開では、役割に割り当てられた各職務権限および職務権限の詳細が表示されます。</span><span class="sxs-lookup"><span data-stu-id="33b1a-138">Expanding a role in the **Security duty assignments** report will show each duty assigned to the role, along with details of the duty.</span></span>

## <a name="batch-processing-of-reports"></a><span data-ttu-id="33b1a-139">レポートのバッチ処理</span><span class="sxs-lookup"><span data-stu-id="33b1a-139">Batch processing of reports</span></span>
<span data-ttu-id="33b1a-140">上記のレポートのいずれかを、バッチ ジョブとして実行するように設定するには、レポートのパラメータ ウィンドウの **バックグラウンドで実行** セクションに移動します。</span><span class="sxs-lookup"><span data-stu-id="33b1a-140">Any of the above reports can be set to run as a batch job by going to the **Run in the background** section of the report's parameter pane.</span></span> <span data-ttu-id="33b1a-141">**バッチ処理** を **はい** に設定し、バッチ タスクジョブ名、バッチ グループ、ジョブをプライベートまたは重大なとして実行するかどうかを指定します。</span><span class="sxs-lookup"><span data-stu-id="33b1a-141">Set **Batch processing** to **Yes**, then provide a batch task job name, batch group, and whether the job should run as Private or Critical.</span></span> <span data-ttu-id="33b1a-142">バッチ タスクが実行されると、レポートが作成されます。</span><span class="sxs-lookup"><span data-stu-id="33b1a-142">The report will then be created when the batch task runs.</span></span>

![レポートのバッチ処理](media/a6142c903497381171bf6c6b27495895.png)



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]