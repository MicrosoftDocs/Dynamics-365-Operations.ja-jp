---
title: Microsoft Dynamics 365 アプリでは、人事管理が表示されない
description: この記事では、顧客が Microsoft Dynamics 365 アプリの中で Microsoft Dynamics 365 Human Resources アプリを表示できない場合の対処方法について説明します。
author: andreabichsel
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
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
ms.openlocfilehash: 658c6a4f17c022c3d0e3e49d16eb89624c4be27c
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/31/2021
ms.locfileid: "5803972"
---
# <a name="human-resources-doesnt-appear-in-microsoft-dynamics-365-apps"></a><span data-ttu-id="f8167-103">Microsoft Dynamics 365 アプリでは、人事管理が表示されない</span><span class="sxs-lookup"><span data-stu-id="f8167-103">Human Resources doesn't appear in Microsoft Dynamics 365 apps</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="f8167-104">**問題点**</span><span class="sxs-lookup"><span data-stu-id="f8167-104">**Issue**</span></span>

<span data-ttu-id="f8167-105">顧客は、Microsoft Dynamics 365 アプリで Dynamics 365 Human Resources を表示できません。</span><span class="sxs-lookup"><span data-stu-id="f8167-105">The customer doesn't see Dynamics 365 Human Resources among the Microsoft Dynamics 365 apps.</span></span>

<span data-ttu-id="f8167-106">**解像度**</span><span class="sxs-lookup"><span data-stu-id="f8167-106">**Resolution**</span></span>

<span data-ttu-id="f8167-107">ユーザーは、Microsoft Power Apps の環境の、環境メーカー ロールに追加される必要があります。</span><span class="sxs-lookup"><span data-stu-id="f8167-107">The user must be added to the Environment Maker role for the environment in Microsoft Power Apps.</span></span>

1. <span data-ttu-id="f8167-108">Power Apps プラン 2 ライセンスを持つ管理者ユーザーは、[Power Apps 管理ポータル](https://preview.admin.powerapps.com/) を開く必要があります。</span><span class="sxs-lookup"><span data-stu-id="f8167-108">The admin user who has a Power Apps Plan 2 license must open the [Power Apps Admin portal](https://preview.admin.powerapps.com/).</span></span>

2. <span data-ttu-id="f8167-109">**環境** を選択してから、人事管理の正しい環境を選択します。</span><span class="sxs-lookup"><span data-stu-id="f8167-109">Select **Environments**, and select the correct environment for Human Resources.</span></span>

3. <span data-ttu-id="f8167-110">**セキュリティ** タブの、**環境ロール** タブで、**環境メーカー** を選択します。</span><span class="sxs-lookup"><span data-stu-id="f8167-110">On the **Security** tab, on the **Environment roles** tab, select **Environment Maker**.</span></span>

    ![環境ロール タブ](media/environment-roles.png)

4. <span data-ttu-id="f8167-112">**ユーザー** タブで、ユーザーまたは組織を追加します。</span><span class="sxs-lookup"><span data-stu-id="f8167-112">On the **Users** tab, add the user or your organization.</span></span>

    ![ユーザー タブ](media/environment-maker.png)

5. <span data-ttu-id="f8167-114">**保存** を選択します。</span><span class="sxs-lookup"><span data-stu-id="f8167-114">Select **Save**.</span></span>

6. <span data-ttu-id="f8167-115">ユーザーはこの時点で [Microsoft Dynamics 365](https://home.dynamics.com/) にサインインする必要があります。</span><span class="sxs-lookup"><span data-stu-id="f8167-115">The user must now sign in to [Microsoft Dynamics 365](https://home.dynamics.com/).</span></span>

7. <span data-ttu-id="f8167-116">**同期** を選択してユーザー アプリを更新します。</span><span class="sxs-lookup"><span data-stu-id="f8167-116">Select **Sync** to update the user apps.</span></span>

    ![同期ボタン](media/get-more.png)

    <span data-ttu-id="f8167-118">同期が完了した後、人事管理はホーム ページに表示されます。</span><span class="sxs-lookup"><span data-stu-id="f8167-118">After synchronization is completed, Human Resources will appear on the home page.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]