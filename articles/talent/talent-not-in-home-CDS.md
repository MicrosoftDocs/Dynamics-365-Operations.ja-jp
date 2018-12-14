---
title: "Microsoft Dynamics 365 アプリ (CDS1.0) の間で Talent が表示されない"
description: "このトピックでは、顧客が Microsoft Dynamics 365 アプリの中で Microsoft Dynamics 365 for Talent アプリを表示できない場合の対処方法について説明します。"
author: Darinkramer
manager: AnnBe
ms.date: 11/02/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-365-talent
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Talent
ms.custom: 
ms.assetid: 
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2018-11-02
ms.dyn365.ops.version: Talent
ms.translationtype: HT
ms.sourcegitcommit: d3f974f94b6c327fd70b8098d24f9e1f1e1e8eeb
ms.openlocfilehash: 32ae0ab807e953bd811a557e6878b9bee79d293c
ms.contentlocale: ja-jp
ms.lasthandoff: 12/04/2018

---

# <a name="talent-doesnt-appear-among-the-microsoft-dynamics-365-apps-cds10"></a><span data-ttu-id="c2bab-103">Microsoft Dynamics 365 アプリ (CDS1.0) の間で Talent が表示されない</span><span class="sxs-lookup"><span data-stu-id="c2bab-103">Talent doesn't appear among the Microsoft Dynamics 365 apps (CDS1.0)</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="c2bab-104">**払出**</span><span class="sxs-lookup"><span data-stu-id="c2bab-104">**Issue**</span></span>

<span data-ttu-id="c2bab-105">顧客は Microsoft Dynamics 365 アプリの中で Microsoft Dynamics 365 for Talent アプリを表示できません。</span><span class="sxs-lookup"><span data-stu-id="c2bab-105">The customer doesn't see the Microsoft Dynamics 365 for Talent app among the Microsoft Dynamics 365 apps.</span></span>

<span data-ttu-id="c2bab-106">**解像度**</span><span class="sxs-lookup"><span data-stu-id="c2bab-106">**Resolution**</span></span>

<span data-ttu-id="c2bab-107">ユーザーは、Microsoft PowerApps の環境の、環境メーカー ロールに追加される必要があります。</span><span class="sxs-lookup"><span data-stu-id="c2bab-107">The user must be added to the Environment Maker role for the environment in Microsoft PowerApps.</span></span>

1. <span data-ttu-id="c2bab-108">PowerApps プラン 2 ライセンスを持つ管理者ユーザーは、[PowerApps 管理ポータル](https://preview.admin.powerapps.com/) を開く必要があります。</span><span class="sxs-lookup"><span data-stu-id="c2bab-108">The admin user who has a PowerApps Plan 2 license must open the [PowerApps Admin portal](https://preview.admin.powerapps.com/).</span></span>
2. <span data-ttu-id="c2bab-109">**環境**を選択してから、Talent の正しい環境を選択します。</span><span class="sxs-lookup"><span data-stu-id="c2bab-109">Select **Environments**, and select the correct environment for Talent.</span></span>
3. <span data-ttu-id="c2bab-110">**セキュリティ**タブの、**環境ロール**タブで、**環境メーカー**を選択します。</span><span class="sxs-lookup"><span data-stu-id="c2bab-110">On the **Security** tab, on the **Environment roles** tab, select **Environment Maker**.</span></span>

    ![環境ロール タブ](media/environment-roles.png)

4. <span data-ttu-id="c2bab-112">**ユーザー**タブで、ユーザーまたは組織を追加します。</span><span class="sxs-lookup"><span data-stu-id="c2bab-112">On the **Users** tab, add the user or your organization.</span></span>

    ![ユーザー タブ](media/environment-maker.png)

5. <span data-ttu-id="c2bab-114">**保存** を選択します。</span><span class="sxs-lookup"><span data-stu-id="c2bab-114">Select **Save**.</span></span>
6. <span data-ttu-id="c2bab-115">ユーザーはこの時点で [Microsoft Dynamics 365](https://home.dynamics.com/) にサインインする必要があります。</span><span class="sxs-lookup"><span data-stu-id="c2bab-115">The user must now sign in to [Microsoft Dynamics 365](https://home.dynamics.com/).</span></span>
7. <span data-ttu-id="c2bab-116">**同期**を選択してユーザー アプリを更新します。</span><span class="sxs-lookup"><span data-stu-id="c2bab-116">Select **Sync** to update the user apps.</span></span>

    ![同期ボタン](media/get-more.png)

    <span data-ttu-id="c2bab-118">同期が完了した後、Talent はホーム ページに表示されます。</span><span class="sxs-lookup"><span data-stu-id="c2bab-118">After synchronization is completed, Talent will appear on the home page.</span></span>

