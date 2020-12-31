---
title: リース ユーザー ロールの割り当て
description: このトピックでは、資産のリースに使用されるセキュリティ ロールについて説明します。 また、これらのロールにユーザーを割り当てる方法についても説明します。
author: moaamer
manager: Ann Beebe
ms.date: 10/28/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations, Retail
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: b31d0880d4f2cd2b8ad2dffcfe279421f935ed35
ms.sourcegitcommit: aeee39c01d3f93a6dfcf2013965fa975a740596a
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/28/2020
ms.locfileid: "4445395"
---
# <a name="assign-lease-user-roles"></a><span data-ttu-id="06da1-104">リース ユーザー ロールの割り当て</span><span class="sxs-lookup"><span data-stu-id="06da1-104">Assign lease user roles</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="06da1-105">このトピックでは、資産のリースに使用されるセキュリティ ロールについて説明します。</span><span class="sxs-lookup"><span data-stu-id="06da1-105">This topic describes the security roles that are used in Asset leasing.</span></span> <span data-ttu-id="06da1-106">また、これらのロールにユーザーを割り当てる方法についても説明します。</span><span class="sxs-lookup"><span data-stu-id="06da1-106">It also explains how to assign users to those roles.</span></span>

<span data-ttu-id="06da1-107">資産リースにおけるアクセスは、3 つのユーザーロールによって区別されます。</span><span class="sxs-lookup"><span data-stu-id="06da1-107">Three user roles differentiate access in Asset leasing.</span></span> <span data-ttu-id="06da1-108">1 つはリースの管理に適したロールで、もう 1 つはリースの表示に適しており、最後の 1 つはリース係の職務の実行に適しています。</span><span class="sxs-lookup"><span data-stu-id="06da1-108">One role is appropriate for maintaining leases, one is appropriate for viewing leases, and one is appropriate for performing a lease clerk's duties.</span></span> <span data-ttu-id="06da1-109">各ロールには、すべてのリース ページに対する特定のアクセス許可が与えられ、ユーザーは自分の職務に応じてリースの表示、作成、編集、または削除を行うことができます。</span><span class="sxs-lookup"><span data-stu-id="06da1-109">Each role has specific permissions for all lease pages, and each lets users view, create, edit, or delete leases, according to their job duties.</span></span>

| <span data-ttu-id="06da1-110">役割</span><span class="sxs-lookup"><span data-stu-id="06da1-110">Role</span></span>           | <span data-ttu-id="06da1-111">説明</span><span class="sxs-lookup"><span data-stu-id="06da1-111">Description</span></span> |
|----------------|-------------|
| <span data-ttu-id="06da1-112">リースの管理</span><span class="sxs-lookup"><span data-stu-id="06da1-112">Maintain Lease</span></span> | <span data-ttu-id="06da1-113">このロールのユーザーは、リースの追加、編集、削除、および表示を行うことができます。</span><span class="sxs-lookup"><span data-stu-id="06da1-113">Users in this role can add, edit, delete, and view leases.</span></span> <span data-ttu-id="06da1-114">このロールは、毎月の仕訳入力の作成と転記、および新しいリース追加のタスクを行う日常的なユーザー向けに設計されています。</span><span class="sxs-lookup"><span data-stu-id="06da1-114">This role is designed for daily users whose tasks include creating and posting monthly journal entries and adding new leases.</span></span> <span data-ttu-id="06da1-115">このロールによって、すべての資産リース機能にアクセスできるようになります。</span><span class="sxs-lookup"><span data-stu-id="06da1-115">This role gives access to all Asset leasing functionality.</span></span> |
| <span data-ttu-id="06da1-116">リースの表示</span><span class="sxs-lookup"><span data-stu-id="06da1-116">View Lease</span></span>     | <span data-ttu-id="06da1-117">このロールのユーザーは、リース レコードの表示、スケジュールの管理、およびレポートの実行のみを行うことができます。</span><span class="sxs-lookup"><span data-stu-id="06da1-117">Users in this role can only view lease records, schedules, and run reports.</span></span> <span data-ttu-id="06da1-118">新しいリースを作成したり、既存のリースを編集したり、リースに対して仕訳入力を作成したりすることはできません。</span><span class="sxs-lookup"><span data-stu-id="06da1-118">They can't create new leases, edit existing leases, or create journal entries against leases.</span></span> <span data-ttu-id="06da1-119">このロールは、リース、リースのスケジュール、およびそれらのリースに対して発生したトランザクションを表示するだけのユーザー向けに設計されています。</span><span class="sxs-lookup"><span data-stu-id="06da1-119">The role is designed for users who just have to view leases, lease schedules, and the transactions that occur against those leases.</span></span> |
| <span data-ttu-id="06da1-120">リース係</span><span class="sxs-lookup"><span data-stu-id="06da1-120">Lease Clerk</span></span>    | <span data-ttu-id="06da1-121">このロールのユーザーは、新しいリースのみを作成できます。</span><span class="sxs-lookup"><span data-stu-id="06da1-121">Users in this role can only create new leases.</span></span> <span data-ttu-id="06da1-122">既存のリースを編集または削除したり、リース　スケジュールを表示したり、またはリース仕訳入力を転記したりすることはできません。</span><span class="sxs-lookup"><span data-stu-id="06da1-122">They can't edit or delete existing leases, view lease schedules, or post leasing journal entries.</span></span> <span data-ttu-id="06da1-123">このロールは、データ入力能力を使用するユーザー向けに設計されています。</span><span class="sxs-lookup"><span data-stu-id="06da1-123">This role is designed for users who work in a data entry capacity.</span></span> |

<span data-ttu-id="06da1-124">資産リース契約で使用されるロールにユーザーを割り当てるには、次のステップに従います。</span><span class="sxs-lookup"><span data-stu-id="06da1-124">Follow these steps to assign users to the roles that are used in Asset leasing.</span></span>

1. <span data-ttu-id="06da1-125">**システム管理 \> セキュリティ \> ユーザーをロールに割り当てる** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="06da1-125">Go to **System administration \> Security \> Assign users to roles**.</span></span>
2. <span data-ttu-id="06da1-126">**リースの管理**、**リース係**、または **リースの表示** のロールを選択し、**ユーザーの手動割り当てまたは除外** を選択します。</span><span class="sxs-lookup"><span data-stu-id="06da1-126">Select the **Maintain lease**, **Lease clerk**, or **View lease** role, and then select **Manually assign/exclude users**.</span></span>
3. <span data-ttu-id="06da1-127">ロールに割り当てるユーザーを選択し、**ロールに割り当て** を選択します。</span><span class="sxs-lookup"><span data-stu-id="06da1-127">Select the user to assign to the role, and then select **Assign to role**.</span></span>
