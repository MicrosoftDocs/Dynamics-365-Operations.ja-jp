---
title: 作業指示書タイプ
description: このトピックでは、資産管理における作業指示書タイプについて説明します。
author: josaw1
manager: AnnBe
ms.date: 08/13/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-08-30
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 57120b51c069e49697f8ec4357265974a0d3afb4
ms.sourcegitcommit: 802dbf0a744d70f9e546632d419415b0993331ab
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/13/2019
ms.locfileid: "1874581"
---
# <a name="work-order-types"></a><span data-ttu-id="3838b-103">作業指示書タイプ</span><span class="sxs-lookup"><span data-stu-id="3838b-103">Work order types</span></span>

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]

<span data-ttu-id="3838b-104">作業指示書タイプは、作業指示書を分類するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="3838b-104">Work order types are used to categorize work orders.</span></span> <span data-ttu-id="3838b-105">例えば、予防的メンテナンスおよび修繕メンテナンスに関連する作業指示書があるとします。</span><span class="sxs-lookup"><span data-stu-id="3838b-105">For example, you might have work orders that are related to preventive maintenance or corrective maintenance.</span></span>

<span data-ttu-id="3838b-106">作業指示書タイプは、作業指示書ライフサイクル モデルとの所属を定義します。</span><span class="sxs-lookup"><span data-stu-id="3838b-106">A work order type defines an affiliation with a work order lifecycle model.</span></span> <span data-ttu-id="3838b-107">作業指示書のライフサイクル モデルでは、作業指示書に対して設定できる作業指示書ライフサイクルの状態が定義されます。</span><span class="sxs-lookup"><span data-stu-id="3838b-107">A work order lifecycle model defines the work order lifecycle states that can be set on a work order.</span></span> <span data-ttu-id="3838b-108">(作業指示書のライフサイクルの状態の例として**作成**、**処理中**、**完了済**があります)。</span><span class="sxs-lookup"><span data-stu-id="3838b-108">(Examples of work order lifecycle states include **Created**, **In Process**, and **Finished**.)</span></span>

<span data-ttu-id="3838b-109">作業指示書ライフサイクルの状態とプロジェクト ステージの詳細については、[作業指示書ライフサイクルの状態](work-order-lifecycle-states.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="3838b-109">For more information about work order lifecycle states and project stages, see [Work order lifecycle states](work-order-lifecycle-states.md).</span></span>

1. <span data-ttu-id="3838b-110">**資産管理** \> **設定** \> **作業指示書** \> **作業指示書タイプ**を選択します。</span><span class="sxs-lookup"><span data-stu-id="3838b-110">Select **Asset management** \> **Setup** \> **Work orders** \> **Work order types**.</span></span>
2. <span data-ttu-id="3838b-111">**新規作成**を選択して作業指示書タイプを作成します。</span><span class="sxs-lookup"><span data-stu-id="3838b-111">Select **New** to create a work order type.</span></span>
3. <span data-ttu-id="3838b-112">**作業指示書タイプ** フィールドで、作業指示書タイプの ID を入力します。</span><span class="sxs-lookup"><span data-stu-id="3838b-112">In the **Work order type** field, enter an ID for the work order type.</span></span>
4. <span data-ttu-id="3838b-113">**名前**フィールドに、名前を入力します。</span><span class="sxs-lookup"><span data-stu-id="3838b-113">In the **Name** field, enter a name.</span></span>
5. <span data-ttu-id="3838b-114">**作業指示書ライフサイクル モデル** フィールドで、ライフサイクル モデルを選択します。</span><span class="sxs-lookup"><span data-stu-id="3838b-114">In the **Work order lifecycle model** field, select a lifecycle model.</span></span>
5. <span data-ttu-id="3838b-115">このタイプの作業指示書に関連するすべての作業指示書ジョブを同じメンテナンス作業者にスケジュールする必要がある場合は、**1 人のメンテナンス作業者**オプションを**はい**に設定します。</span><span class="sxs-lookup"><span data-stu-id="3838b-115">Set the **One maintenance worker** option to **Yes** if all work order jobs that are related to a work order of this type should be scheduled to the same maintenance worker.</span></span>
6. <span data-ttu-id="3838b-116">**原価タイプ** フィールドで該当する場合、**修正**、**予防的**、または**投資**を選択します。</span><span class="sxs-lookup"><span data-stu-id="3838b-116">In the **Cost type** field, select **Corrective**, **Preventive**, or **Investment**, as appropriate.</span></span> <span data-ttu-id="3838b-117">作業指示書のすべての作業指示書ジョブは必ず同じ原価タイプを持つ必要があります。</span><span class="sxs-lookup"><span data-stu-id="3838b-117">All work order jobs on a work order must have the same cost type.</span></span>
7. <span data-ttu-id="3838b-118">**必須**セクションで、関連するオプションを**はい**に設定し、このタイプの作業指示書に追加される障害関連またはメンテナンス ダウンタイムなどの関連情報を指定します。</span><span class="sxs-lookup"><span data-stu-id="3838b-118">In the **Mandatory** section, set the relevant options to **Yes** to specify which fault-related or maintenance downtime–related information is added to a work order of this type.</span></span>

    > [!NOTE]
    > <span data-ttu-id="3838b-119">**必須**セクションのオプションは、**作業指示書のライフサイクルの状態**ページで**検証**クイックタブのオプションに関連しています (**資産管理** \> **設定** \> **作業指示書** \> **ライフサイクルの状態**)。</span><span class="sxs-lookup"><span data-stu-id="3838b-119">The options in the **Mandatory** section are related to the options on the **Validate** FastTab of the **Work order lifecycle states** page (**Asset management** \> **Setup** \> **Work orders** \> **Lifecycle states**).</span></span>

8. <span data-ttu-id="3838b-120">**保存** を選択します。</span><span class="sxs-lookup"><span data-stu-id="3838b-120">Select **Save**.</span></span>

![図 1](media/16-setup-for-work-orders.png)
