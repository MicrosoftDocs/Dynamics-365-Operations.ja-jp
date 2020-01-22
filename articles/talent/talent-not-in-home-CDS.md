---
title: Microsoft Dynamics 365 アプリ (Common Data Service 1.0) で Talent が表示されない
description: このトピックでは、顧客が Microsoft Dynamics 365 アプリの中で Microsoft Dynamics 365 Talent アプリを表示できない場合の対処方法について説明します。
author: andreabichsel
manager: AnnBe
ms.date: 11/02/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2018-11-02
ms.dyn365.ops.version: Talent
ms.openlocfilehash: a44d2e43752960d3026fa7ac92c7b261aee05448
ms.sourcegitcommit: 871707a3fd236da693a3d51f401eb0cb9d4bae39
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 12/06/2019
ms.locfileid: "2897030"
---
# <a name="talent-doesnt-appear-among-the-microsoft-dynamics-365-apps-common-data-service-10"></a><span data-ttu-id="315c2-103">Microsoft Dynamics 365 アプリ (Common Data Service 1.0) で Talent が表示されない</span><span class="sxs-lookup"><span data-stu-id="315c2-103">Talent doesn't appear among the Microsoft Dynamics 365 apps (Common Data Service 1.0)</span></span>

<span data-ttu-id="315c2-104">**問題点**</span><span class="sxs-lookup"><span data-stu-id="315c2-104">**Issue**</span></span>

<span data-ttu-id="315c2-105">顧客は、Microsoft Dynamics 365 アプリの中で Microsoft Dynamics 365 Talent アプリを表示できません。</span><span class="sxs-lookup"><span data-stu-id="315c2-105">The customer doesn't see the Microsoft Dynamics 365 Talent app among the Microsoft Dynamics 365 apps.</span></span>

<span data-ttu-id="315c2-106">**解像度**</span><span class="sxs-lookup"><span data-stu-id="315c2-106">**Resolution**</span></span>

<span data-ttu-id="315c2-107">ユーザーは、Microsoft Power Apps の環境の、環境メーカー ロールに追加される必要があります。</span><span class="sxs-lookup"><span data-stu-id="315c2-107">The user must be added to the Environment Maker role for the environment in Microsoft Power Apps.</span></span>

1. <span data-ttu-id="315c2-108">Power Apps プラン 2 ライセンスを持つ管理者ユーザーは、[Power Apps 管理ポータル](https://preview.admin.powerapps.com/) を開く必要があります。</span><span class="sxs-lookup"><span data-stu-id="315c2-108">The admin user who has a Power Apps Plan 2 license must open the [Power Apps Admin portal](https://preview.admin.powerapps.com/).</span></span>
2. <span data-ttu-id="315c2-109">**環境**を選択してから、Talent の正しい環境を選択します。</span><span class="sxs-lookup"><span data-stu-id="315c2-109">Select **Environments**, and select the correct environment for Talent.</span></span>
3. <span data-ttu-id="315c2-110">**セキュリティ**タブの、**環境ロール**タブで、**環境メーカー**を選択します。</span><span class="sxs-lookup"><span data-stu-id="315c2-110">On the **Security** tab, on the **Environment roles** tab, select **Environment Maker**.</span></span>

    ![環境ロール タブ](media/environment-roles.png)

4. <span data-ttu-id="315c2-112">**ユーザー**タブで、ユーザーまたは組織を追加します。</span><span class="sxs-lookup"><span data-stu-id="315c2-112">On the **Users** tab, add the user or your organization.</span></span>

    ![ユーザー タブ](media/environment-maker.png)

5. <span data-ttu-id="315c2-114">**保存** を選択します。</span><span class="sxs-lookup"><span data-stu-id="315c2-114">Select **Save**.</span></span>
6. <span data-ttu-id="315c2-115">ユーザーはこの時点で [Microsoft Dynamics 365](https://home.dynamics.com/) にサインインする必要があります。</span><span class="sxs-lookup"><span data-stu-id="315c2-115">The user must now sign in to [Microsoft Dynamics 365](https://home.dynamics.com/).</span></span>
7. <span data-ttu-id="315c2-116">**同期**を選択してユーザー アプリを更新します。</span><span class="sxs-lookup"><span data-stu-id="315c2-116">Select **Sync** to update the user apps.</span></span>

    ![同期ボタン](media/get-more.png)

    <span data-ttu-id="315c2-118">同期が完了した後、Talent はホーム ページに表示されます。</span><span class="sxs-lookup"><span data-stu-id="315c2-118">After synchronization is completed, Talent will appear on the home page.</span></span>
