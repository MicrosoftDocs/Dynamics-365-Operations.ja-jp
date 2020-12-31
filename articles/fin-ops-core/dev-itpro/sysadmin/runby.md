---
title: バッチ マネージャーのセキュリティ ロール
description: このトピックでは、バッチ ジョブの管理に使用されるバッチ管理者のセキュリティ ロールに関する情報を提供します。
author: hasaid
manager: AnnBe
ms.date: 10/25/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: IT Pro
ms.reviewer: sericks
ms.custom: 62333
ms.assetid: 6135bcf7-bf8f-42ae-b2c6-458f6538e6a4
ms.search.region: Global
ms.author: hasaid
ms.search.validFrom: 2018-08-15
ms.dyn365.ops.version: Platform update 20
ms.openlocfilehash: 67e8120a3a01d927d1e14dfa9576f1ace1216791
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 12/05/2020
ms.locfileid: "4682473"
---
# <a name="batch-manager-security-role"></a><span data-ttu-id="5dbc6-103">バッチ マネージャーのセキュリティ ロール</span><span class="sxs-lookup"><span data-stu-id="5dbc6-103">Batch manager security role</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="5dbc6-104">プラットフォーム更新 20 より前では、バッチ ジョブを管理するシステム管理者や IT 管理者セキュリティ ロールにユーザーを割り当てる必要がありました。</span><span class="sxs-lookup"><span data-stu-id="5dbc6-104">Before Platform update 20, users needed to be assigned to the system admin or IT admin security role to manage batch jobs.</span></span> <span data-ttu-id="5dbc6-105">プラットフォーム更新プログラム 20 のリリースには、より対象を絞り込んだロール、バッチ マネージャーがあります。</span><span class="sxs-lookup"><span data-stu-id="5dbc6-105">With the release of Platform update 20, there is a more targeted role, Batch manager.</span></span> <span data-ttu-id="5dbc6-106">このセキュリティ ロールでは、ユーザーはバッチ ジョブをコピーする、ジョブを実行するユーザーを変更する、ジョブを実行できる時間範囲を指定するアクセス許可を持ちます。</span><span class="sxs-lookup"><span data-stu-id="5dbc6-106">With this security role, a user now has permissions to copy batch jobs, change who will execute jobs, and specify the time ranges during which jobs can execute.</span></span> <span data-ttu-id="5dbc6-107">バッチ管理セキュリティ特権は、バッチ管理者セキュリティ ロールの一部です。これによって、ユーザーはアド ホック バッチ ジョブを作成して、他のユーザーに権限を付与できます。</span><span class="sxs-lookup"><span data-stu-id="5dbc6-107">The Batch maintain security privilege is part of the Batch manager security role and it allows a user to create an ad hoc batch job and grant privileges to other users.</span></span>

> [!NOTE]
> <span data-ttu-id="5dbc6-108">この機能は、Platform update 20 以降で利用できます。</span><span class="sxs-lookup"><span data-stu-id="5dbc6-108">This feature is available as of Platform update 20.</span></span>

## <a name="assign-the-batch-manager-role-to-a-user"></a><span data-ttu-id="5dbc6-109">バッチ管理者ロールをユーザーに割り当てる</span><span class="sxs-lookup"><span data-stu-id="5dbc6-109">Assign the Batch manager role to a user</span></span>

<span data-ttu-id="5dbc6-110">特定のユーザーにバッチ管理者のセキュリティ ロールを割り当てるには、次の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="5dbc6-110">Complete the following steps to assign the Batch manager security role to a specific user.</span></span>

1. <span data-ttu-id="5dbc6-111">**システム管理** > **セキュリティ** > **ユーザーをロールに割り当てる** を選択します。</span><span class="sxs-lookup"><span data-stu-id="5dbc6-111">Select **System administration** > **Security** > **Assign users to roles**.</span></span>

![ロールへのユーザーの割り当て](./media/assign-batchmanager-role.png) 

2. <span data-ttu-id="5dbc6-113">**バッチ ジョブ マネージャー** をクリックし、左ウィンドウで **ユーザーを手動で割り当てる/除外する** を選択します。</span><span class="sxs-lookup"><span data-stu-id="5dbc6-113">Select **Batch Job Manager**, and on the left pane, select **Manually assign/exclude user**.</span></span>

![バッチ マネージャー ロール](./media/assign-batchmanager-role-2.png) 

3. <span data-ttu-id="5dbc6-115">一覧からユーザーを選択し、**ロールに割り当て** を選択します。</span><span class="sxs-lookup"><span data-stu-id="5dbc6-115">Select a user from the list, and then select **Assign to role**.</span></span>
4. <span data-ttu-id="5dbc6-116">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="5dbc6-116">Close the page.</span></span> 

## <a name="run-by-user"></a><span data-ttu-id="5dbc6-117">実行者ユーザー</span><span class="sxs-lookup"><span data-stu-id="5dbc6-117">Run by user</span></span>

<span data-ttu-id="5dbc6-118">**実行者ユーザー** 機能により、バッチ管理者は、バッチ ジョブを実行するユーザーを指定できます。</span><span class="sxs-lookup"><span data-stu-id="5dbc6-118">The **run by user** functionality allows Batch managers to specify a user to run the batch job.</span></span> <span data-ttu-id="5dbc6-119">この機能は、現在ジョブの実行が割り当てられているユーザーを変更する場合、または別の会社にバッチ ジョブをコピーするときにユーザーをすばやく設定する場合に便利です。</span><span class="sxs-lookup"><span data-stu-id="5dbc6-119">This functionality is useful when you want to change the user who is currently assigned to run the job or if you want to quickly set a user while copying the batch jobs from one company to another.</span></span> <span data-ttu-id="5dbc6-120">この機能は、バッチ ジョブをコピーするのにも使用できます。</span><span class="sxs-lookup"><span data-stu-id="5dbc6-120">You can also use this functionality to copy batch jobs.</span></span>

![実行者ユーザー](./media/runby-user.png)  
