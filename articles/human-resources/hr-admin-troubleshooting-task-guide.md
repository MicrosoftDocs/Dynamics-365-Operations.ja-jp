---
title: LCS にタスク ガイドを保存して再生する
description: この記事では、タスク Guides を Microsoft Dynamics Lifecycle Services (LCS) に保存し、それらを再生する方法について説明します。
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
ms.openlocfilehash: 51ffdb508f09ceaaefb458cd614b9c64604eb639
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/31/2021
ms.locfileid: "5797914"
---
# <a name="save-task-guides-to-lcs-and-replay-them"></a><span data-ttu-id="bbe09-103">LCS にタスク ガイドを保存して再生する</span><span class="sxs-lookup"><span data-stu-id="bbe09-103">Save task guides to LCS and replay them</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="bbe09-104">**環境の詳細**</span><span class="sxs-lookup"><span data-stu-id="bbe09-104">**Environment details**</span></span> 

<span data-ttu-id="bbe09-105">Microsoft Dynamics Lifecycle Services (LCS) 経由で配置された Microsoft Dynamics 365 Human Resources</span><span class="sxs-lookup"><span data-stu-id="bbe09-105">Microsoft Dynamics 365 Human Resources, which was deployed via Microsoft Dynamics Lifecycle Services (LCS)</span></span>

<span data-ttu-id="bbe09-106">**払出**</span><span class="sxs-lookup"><span data-stu-id="bbe09-106">**Issue**</span></span>

<span data-ttu-id="bbe09-107">顧客は自分の LCS プロジェクトに新しいタスクの記録を保存し、保存されているタスク ガイドを再生することを希望しています。</span><span class="sxs-lookup"><span data-stu-id="bbe09-107">The customer wants to save new task recordings to his or her LCS project, and then replay the saved task guides.</span></span>

<span data-ttu-id="bbe09-108">**解像度**</span><span class="sxs-lookup"><span data-stu-id="bbe09-108">**Resolution**</span></span>

<span data-ttu-id="bbe09-109">LCS にタスク記録を保存するには、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="bbe09-109">Follow these steps to save a task recording to LCS.</span></span>

1. <span data-ttu-id="bbe09-110">LCS にサインインして、プロジェクトを選択します。</span><span class="sxs-lookup"><span data-stu-id="bbe09-110">Sign in to LCS, and select the project.</span></span>
2. <span data-ttu-id="bbe09-111">**ビジネス プロセス モデラー** タイルを選択します。</span><span class="sxs-lookup"><span data-stu-id="bbe09-111">Select the **Business process modeler** tile.</span></span>
3. <span data-ttu-id="bbe09-112">「更新された BPM エクスペリエンス。」でページを表示する</span><span class="sxs-lookup"><span data-stu-id="bbe09-112">View the page in the "Updated BPM experience."</span></span>
4. <span data-ttu-id="bbe09-113">ライブラリを選択してから、**コピー** を選択します。</span><span class="sxs-lookup"><span data-stu-id="bbe09-113">Select a library, and then select **Copy**.</span></span>
5. <span data-ttu-id="bbe09-114">ビジネス プロセス モデラー (BPM) モデルの名前を入力します。</span><span class="sxs-lookup"><span data-stu-id="bbe09-114">Enter a name for the Business process modeler (BPM) model.</span></span>
6. <span data-ttu-id="bbe09-115">LCS から人事管理にログインします。</span><span class="sxs-lookup"><span data-stu-id="bbe09-115">Sign in to Human Resources from LCS.</span></span>
7. <span data-ttu-id="bbe09-116">**検索** フィールドで、**ヘルプ** と入力します。</span><span class="sxs-lookup"><span data-stu-id="bbe09-116">In the **Search** field, enter **help**.</span></span> <span data-ttu-id="bbe09-117">Lifecycle Services ヘルプが開きます。</span><span class="sxs-lookup"><span data-stu-id="bbe09-117">Lifecycle Services Help is opened.</span></span>
8. <span data-ttu-id="bbe09-118">Lifecycle Services のヘルプ構成の **更新** ボタンを選択します。</span><span class="sxs-lookup"><span data-stu-id="bbe09-118">Select the **Refresh** button for Lifecycle Services Help configuration.</span></span>

    <span data-ttu-id="bbe09-119">新しい有効な BPM ライブラリが表示されます。</span><span class="sxs-lookup"><span data-stu-id="bbe09-119">Your new BPM library should appear, and it should be active.</span></span>

9. <span data-ttu-id="bbe09-120">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="bbe09-120">Close the page.</span></span>
10. <span data-ttu-id="bbe09-121">タスク記録を作成します。</span><span class="sxs-lookup"><span data-stu-id="bbe09-121">Create a task recording.</span></span>
11. <span data-ttu-id="bbe09-122">完了したら、**Lifecycle Services に保存** を選択します。</span><span class="sxs-lookup"><span data-stu-id="bbe09-122">When you've finished, select **Save to Lifecycle Services**.</span></span>

    ![Lifecycle Services に保存](media/task-guides.png)

12. <span data-ttu-id="bbe09-124">タスク記録を保存する BPM ライブラリとノードを選択します。</span><span class="sxs-lookup"><span data-stu-id="bbe09-124">Select the BPM library and node to save the task recording to.</span></span>

<span data-ttu-id="bbe09-125">LCS からタスク ガイドを再生するにはこれらの手順に従います。</span><span class="sxs-lookup"><span data-stu-id="bbe09-125">Follow these steps to replay a task guide from LCS.</span></span>

1. <span data-ttu-id="bbe09-126">タスク レコーダーを開始します。</span><span class="sxs-lookup"><span data-stu-id="bbe09-126">Start Task recorder.</span></span>
2. <span data-ttu-id="bbe09-127">**LCS から開く** を選択します。</span><span class="sxs-lookup"><span data-stu-id="bbe09-127">Select **Open from LCS**.</span></span>
3. <span data-ttu-id="bbe09-128">タスク ガイドが保存されているライブラリと BPM ノードを選択します。</span><span class="sxs-lookup"><span data-stu-id="bbe09-128">Select the library and the BPM node that have the saved task guide.</span></span>
4. <span data-ttu-id="bbe09-129">タスク ガイドを開きます。</span><span class="sxs-lookup"><span data-stu-id="bbe09-129">Open the task guide.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]