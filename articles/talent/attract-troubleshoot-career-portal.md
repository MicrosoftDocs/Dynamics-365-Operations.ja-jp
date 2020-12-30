---
title: Attract ユーザーがキャリア ポータルから仕事に応募できない
description: このトピックでは、Attract ユーザーが求人ポータルからジョブに応募できない問題のトラブルシューティング方法について説明します。
author: andreabichsel
manager: AnnBe
ms.date: 09/23/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Core, Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-09-23
ms.dyn365.ops.version: Platform update 24
ms.openlocfilehash: e1d72bef6d8bbe15e27326f66341915ba44a09b4
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/13/2020
ms.locfileid: "4461723"
---
# <a name="attract-users-cant-apply-for-jobs-from-career-portal"></a><span data-ttu-id="c818c-103">Attract ユーザーがキャリア ポータルから仕事に応募できない</span><span class="sxs-lookup"><span data-stu-id="c818c-103">Attract users can't apply for jobs from career portal</span></span>

[!include [banner](includes/banner.md)]

## <a name="issue"></a><span data-ttu-id="c818c-104">出庫</span><span class="sxs-lookup"><span data-stu-id="c818c-104">Issue</span></span>

<span data-ttu-id="c818c-105">Attract ユーザーがキャリア ポータルからジョブに応募できません。</span><span class="sxs-lookup"><span data-stu-id="c818c-105">Attract users can't apply for jobs from the career portal.</span></span> <span data-ttu-id="c818c-106">Dynamics 365 Talent: Attract で作成したジョブに応募しようとすると、ブラウザーがページを読込んだままになり、アクションが実行されません。</span><span class="sxs-lookup"><span data-stu-id="c818c-106">When they try to apply for a job that was created in Dynamics 365 Talent: Attract, the browser loads the page continuously and doesn't complete the action.</span></span>

## <a name="cause"></a><span data-ttu-id="c818c-107">原因</span><span class="sxs-lookup"><span data-stu-id="c818c-107">Cause</span></span>

<span data-ttu-id="c818c-108">この問題は、Talent Relationship チームが Talent ユーザー ロールを持っていない場合に発生します。</span><span class="sxs-lookup"><span data-stu-id="c818c-108">This problem occurs when the Talent Relationship Team doesn't have the Talent user role.</span></span>

## <a name="resolution"></a><span data-ttu-id="c818c-109">解像度</span><span class="sxs-lookup"><span data-stu-id="c818c-109">Resolution</span></span>

<span data-ttu-id="c818c-110">Talent ユーザー ロールを Talent Relationship チームに割り当ててください。</span><span class="sxs-lookup"><span data-stu-id="c818c-110">Assign the Talent user role to the Talent Relationship Team.</span></span>

1. <span data-ttu-id="c818c-111">[Power Platform 管理センター](https://admin.powerplatform.microsoft.com) に次のいずれかの管理者資格情報を使用してログインします。</span><span class="sxs-lookup"><span data-stu-id="c818c-111">Sign in to the [Power Platform admin center](https://admin.powerplatform.microsoft.com) with any of the following admin credentials:</span></span>

   - <span data-ttu-id="c818c-112">Dynamics 365 管理者</span><span class="sxs-lookup"><span data-stu-id="c818c-112">Dynamics 365 admin</span></span>
   - <span data-ttu-id="c818c-113">Global 管理者</span><span class="sxs-lookup"><span data-stu-id="c818c-113">Global admin</span></span>
   - <span data-ttu-id="c818c-114">Power Platform 管理者</span><span class="sxs-lookup"><span data-stu-id="c818c-114">Power Platform admin</span></span>

2. <span data-ttu-id="c818c-115">ナビゲーション ペインで、**環境** を選択し、Talent ユーザー ロールを Talent Relationship チームに割り当てる環境を選択します。</span><span class="sxs-lookup"><span data-stu-id="c818c-115">In the navigation pane, select **Environments**, and then select the environment in which to assign the Talent user role to the Talent Relationship Team.</span></span>

   ![環境の選択](./media/attract-troubleshoot-career-portal-select-environment.png)

3. <span data-ttu-id="c818c-117">**環境** ペインで、**環境 URL** を選択し、環境管理者ポータルにログインします (たとえば、https:<orgname> .crm.dynamics.com)。</span><span class="sxs-lookup"><span data-stu-id="c818c-117">In the **Environments** pane, select the **Environment URL** and sign in to the environment's admin portal (for example, https:<orgname>.crm.dynamics.com).</span></span>

4. <span data-ttu-id="c818c-118">**設定**、**システム**、**セキュリティ** の順に選択します。</span><span class="sxs-lookup"><span data-stu-id="c818c-118">Select **Settings**, select **System**, and then select **Security**.</span></span>

   ![セキュリティに移動する](./media/attract-troubleshoot-career-portal-security.png)

5. <span data-ttu-id="c818c-120">**チーム** を選択します。</span><span class="sxs-lookup"><span data-stu-id="c818c-120">Select **Teams**.</span></span>

   ![チームの選択](./media/attract-troubleshoot-career-portal-security-teams.png)

6. <span data-ttu-id="c818c-122">検索ボックスで **Talent Relationship チーム** を検索し、検索結果からチームを選択します。</span><span class="sxs-lookup"><span data-stu-id="c818c-122">Search for **Talent Relationship Team** in the search box, and then select the team from the search results.</span></span>

7. <span data-ttu-id="c818c-123">リボンから **ロールの管理** を選択します。</span><span class="sxs-lookup"><span data-stu-id="c818c-123">Select **MANAGE ROLES** from the ribbon.</span></span>

8. <span data-ttu-id="c818c-124">**チーム ロールの管理** ダイアログで、使用可能なロールの一覧から **Talent ユーザー** を選択し、**OK** を選択してロールを適用します。</span><span class="sxs-lookup"><span data-stu-id="c818c-124">In the **Manage Team Roles** dialog, select **Talent user** from the list of available roles, and then select **OK** to apply the role.</span></span>

   ![ロールの適用](./media/attract-troubleshoot-career-portal-apply-role.png)

9. <span data-ttu-id="c818c-126">次のように変更をテストします。</span><span class="sxs-lookup"><span data-stu-id="c818c-126">Test your changes:</span></span>

   1. <span data-ttu-id="c818c-127">新しいブラウザ ウィンドウから、キャリア ポータルにログインします。</span><span class="sxs-lookup"><span data-stu-id="c818c-127">Sign in to the career portal from a new browser window.</span></span>
   2. <span data-ttu-id="c818c-128">このジョブを求人ポータルから適用します。</span><span class="sxs-lookup"><span data-stu-id="c818c-128">Apply for the job from the career portal.</span></span> 