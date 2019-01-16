---
title: "ワークフローでの並列活動のコンフィギュレーション"
description: "並列活動をコンフィギュレーションするには、ワークフロー エディターで次の手順を実行します。"
author: sericks007
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.custom: 195753
ms.assetid: 6d0656df-b5af-4001-96e6-6f0fcc44d022
ms.search.region: Global
ms.author: donaldc
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 3ee5334c87b2b0acae2afa6882feca63e3b9cc8e
ms.openlocfilehash: 01c1fa876dd66ba6f0e1cdcecff56f424e117bd9
ms.contentlocale: ja-jp
ms.lasthandoff: 12/18/2018

---

# <a name="configure-parallel-activities-in-a-workflow"></a><span data-ttu-id="1b2f6-103">ワークフローでの並列活動のコンフィギュレーション</span><span class="sxs-lookup"><span data-stu-id="1b2f6-103">Configure parallel activities in a workflow</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="1b2f6-104">並列活動をコンフィギュレーションするには、ワークフロー エディターで次の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="1b2f6-104">To configure a parallel activity, complete the following procedures in the workflow editor.</span></span>

<span data-ttu-id="1b2f6-105">並列活動は、同時に実行されるワークフロー分岐から構成されます。</span><span class="sxs-lookup"><span data-stu-id="1b2f6-105">A parallel activity consists of workflow branches that run at the same time.</span></span>

## <a name="name-a-parallel-activity"></a><span data-ttu-id="1b2f6-106">並列活動の名前の設定</span><span class="sxs-lookup"><span data-stu-id="1b2f6-106">Name a parallel activity</span></span>

<span data-ttu-id="1b2f6-107">並列活動の名前を入力するには、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="1b2f6-107">Follow these steps to enter a name for a parallel activity.</span></span>

1. <span data-ttu-id="1b2f6-108">並列活動を右クリックし、**プロパティ**をクリックして、**プロパティ**フォームを開きます。</span><span class="sxs-lookup"><span data-stu-id="1b2f6-108">Right-click the parallel activity, and then click **Properties** to open the **Properties** form.</span></span>
2. <span data-ttu-id="1b2f6-109">左ウィンドウで**基本設定**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="1b2f6-109">In the left pane, click **Basic Settings**.</span></span>
3. <span data-ttu-id="1b2f6-110">**名前**フィールドに、並列活動の一意な名前を入力します。</span><span class="sxs-lookup"><span data-stu-id="1b2f6-110">In the **Name** field, enter a unique name for the parallel activity.</span></span>
4. <span data-ttu-id="1b2f6-111">**閉じる**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="1b2f6-111">Click **Close**.</span></span>

## <a name="configure-the-branches-of-a-parallel-activity"></a><span data-ttu-id="1b2f6-112">並列活動の分岐のコンフィギュレーション</span><span class="sxs-lookup"><span data-stu-id="1b2f6-112">Configure the branches of a parallel activity</span></span>

<span data-ttu-id="1b2f6-113">この並列活動の分岐を追加およびコンフィギュレーションするには、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="1b2f6-113">Follow these steps to add and configure the branches of this parallel activity.</span></span>

1. <span data-ttu-id="1b2f6-114">並列活動の分岐を表示する並列活動をダブルクリックします。</span><span class="sxs-lookup"><span data-stu-id="1b2f6-114">Double-click the parallel activity to display the branches of the parallel activity.</span></span>
2. <span data-ttu-id="1b2f6-115">分岐を追加するには、**分岐**要素を**ワークフロー要素**領域からキャンバス上の挿入ポイントにドラッグします。</span><span class="sxs-lookup"><span data-stu-id="1b2f6-115">To add a branch, drag the **Branch** element from the **Workflow elements** area to an insertion point on the canvas.</span></span> <span data-ttu-id="1b2f6-116">次の図に、挿入ポイントを示します。</span><span class="sxs-lookup"><span data-stu-id="1b2f6-116">The following figure shows an insertion point.</span></span>

    ![挿入ポイント](./media/workflow_insertionpoint.gif)

    > [!NOTE]
    > <span data-ttu-id="1b2f6-118">並列活動の分岐はすべて同時に実行されるため、分岐の順序は重要ではありません。</span><span class="sxs-lookup"><span data-stu-id="1b2f6-118">The order of the branches is not important because all the branches of a parallel activity run at the same time.</span></span>

3. <span data-ttu-id="1b2f6-119">各分岐をコンフィギュレーションするには、[並列分岐のコンフィギュレーション](configure-parallel-branch-workflow.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="1b2f6-119">To configure each branch, see [Configure a parallel branch](configure-parallel-branch-workflow.md).</span></span>

