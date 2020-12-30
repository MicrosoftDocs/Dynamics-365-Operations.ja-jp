---
title: Microsoft Dynamics 365 アプリでは、人事管理が表示されない
description: この記事では、顧客が Microsoft Dynamics 365 アプリの中で Microsoft Dynamics 365 Human Resources アプリを表示できない場合の対処方法について説明します。
author: andreabichsel
manager: AnnBe
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-human-resources
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: cbf47b4673e1c97965bba7728e5669b7639c4d56
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/13/2020
ms.locfileid: "4419350"
---
# <a name="human-resources-doesnt-appear-in-microsoft-dynamics-365-apps"></a><span data-ttu-id="8ce7f-103">Microsoft Dynamics 365 アプリでは、人事管理が表示されない</span><span class="sxs-lookup"><span data-stu-id="8ce7f-103">Human Resources doesn't appear in Microsoft Dynamics 365 apps</span></span>

<span data-ttu-id="8ce7f-104">**問題点**</span><span class="sxs-lookup"><span data-stu-id="8ce7f-104">**Issue**</span></span>

<span data-ttu-id="8ce7f-105">顧客は、Microsoft Dynamics 365 アプリで Dynamics 365 Human Resources を表示できません。</span><span class="sxs-lookup"><span data-stu-id="8ce7f-105">The customer doesn't see Dynamics 365 Human Resources among the Microsoft Dynamics 365 apps.</span></span>

<span data-ttu-id="8ce7f-106">**解像度**</span><span class="sxs-lookup"><span data-stu-id="8ce7f-106">**Resolution**</span></span>

<span data-ttu-id="8ce7f-107">ユーザーは、Microsoft Power Apps の環境の、環境メーカー ロールに追加される必要があります。</span><span class="sxs-lookup"><span data-stu-id="8ce7f-107">The user must be added to the Environment Maker role for the environment in Microsoft Power Apps.</span></span>

1. <span data-ttu-id="8ce7f-108">Power Apps プラン 2 ライセンスを持つ管理者ユーザーは、[Power Apps 管理ポータル](https://preview.admin.powerapps.com/) を開く必要があります。</span><span class="sxs-lookup"><span data-stu-id="8ce7f-108">The admin user who has a Power Apps Plan 2 license must open the [Power Apps Admin portal](https://preview.admin.powerapps.com/).</span></span>

2. <span data-ttu-id="8ce7f-109">**環境** を選択してから、人事管理の正しい環境を選択します。</span><span class="sxs-lookup"><span data-stu-id="8ce7f-109">Select **Environments**, and select the correct environment for Human Resources.</span></span>

3. <span data-ttu-id="8ce7f-110">**セキュリティ** タブの、**環境ロール** タブで、**環境メーカー** を選択します。</span><span class="sxs-lookup"><span data-stu-id="8ce7f-110">On the **Security** tab, on the **Environment roles** tab, select **Environment Maker**.</span></span>

    ![環境ロール タブ](media/environment-roles.png)

4. <span data-ttu-id="8ce7f-112">**ユーザー** タブで、ユーザーまたは組織を追加します。</span><span class="sxs-lookup"><span data-stu-id="8ce7f-112">On the **Users** tab, add the user or your organization.</span></span>

    ![ユーザー タブ](media/environment-maker.png)

5. <span data-ttu-id="8ce7f-114">**保存** を選択します。</span><span class="sxs-lookup"><span data-stu-id="8ce7f-114">Select **Save**.</span></span>

6. <span data-ttu-id="8ce7f-115">ユーザーはこの時点で [Microsoft Dynamics 365](https://home.dynamics.com/) にサインインする必要があります。</span><span class="sxs-lookup"><span data-stu-id="8ce7f-115">The user must now sign in to [Microsoft Dynamics 365](https://home.dynamics.com/).</span></span>

7. <span data-ttu-id="8ce7f-116">**同期** を選択してユーザー アプリを更新します。</span><span class="sxs-lookup"><span data-stu-id="8ce7f-116">Select **Sync** to update the user apps.</span></span>

    ![同期ボタン](media/get-more.png)

    <span data-ttu-id="8ce7f-118">同期が完了した後、人事管理はホーム ページに表示されます。</span><span class="sxs-lookup"><span data-stu-id="8ce7f-118">After synchronization is completed, Human Resources will appear on the home page.</span></span>
