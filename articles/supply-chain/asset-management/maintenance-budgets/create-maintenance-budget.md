---
title: メンテナンス予算の作成
description: このトピックでは、資産管理でメンテナンス予算を作成する方法について説明します。
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
ms.openlocfilehash: 99f76c684150f154404cbb241daacb7a8d05f7f9
ms.sourcegitcommit: d37fb09101c30858bcb975931b3d8f947d72017b
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/10/2019
ms.locfileid: "2571763"
---
# <a name="create-maintenance-budgets"></a><span data-ttu-id="08878-103">メンテナンス予算の作成</span><span class="sxs-lookup"><span data-stu-id="08878-103">Create maintenance budgets</span></span>

[!include [banner](../../includes/banner.md)]

 



<span data-ttu-id="08878-104">メンテナンス予算は、予防的メンテナンスに対する予定原価の概要を提供するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="08878-104">Maintenance budgets are used to provide an overview of expected costs for preventive maintenance.</span></span> <span data-ttu-id="08878-105">予算明細行は、予算期間中に開始予定日を持つメンテナンス スケジュール明細行に基づいて計算されます。</span><span class="sxs-lookup"><span data-stu-id="08878-105">Budget lines are calculated based on maintenance schedule lines that have an expected start date during the budget period.</span></span>

<span data-ttu-id="08878-106">メンテナンス予算は、資産管理の**予防的**、**修正**、および**投資**で使用される原価タイプに基づいています。</span><span class="sxs-lookup"><span data-stu-id="08878-106">Maintenance budgets are based on the cost types that are used in Asset Management: **Preventive**, **Corrective**, and **Investment**.</span></span> <span data-ttu-id="08878-107">投資メンテナンスの予算原価は、予算期間内に交換日、および関連する交換価値がある有効な資産に対して使用されます。</span><span class="sxs-lookup"><span data-stu-id="08878-107">Budget costs for investment maintenance are included for active assets that have a replacement date during the budget period and a related replacement value.</span></span> <span data-ttu-id="08878-108">過去の修正日が予算計算に含まれている場合、修繕メンテナンスの予算原価が含められます。</span><span class="sxs-lookup"><span data-stu-id="08878-108">Budget costs for corrective maintenance are included if a past corrective date is included in the budget calculation.</span></span> <span data-ttu-id="08878-109">この場合、メンテナンス予算を計算する将来の同じ期間に対して、早い期間からの修正原価が計算されます。</span><span class="sxs-lookup"><span data-stu-id="08878-109">In that case, corrective costs from an earlier period are calculated for the same future period that you calculate the maintenance budget for.</span></span>

## <a name="create-a-maintenance-budget"></a><span data-ttu-id="08878-110">メンテナンス予算の作成</span><span class="sxs-lookup"><span data-stu-id="08878-110">Create a maintenance budget</span></span>

1. <span data-ttu-id="08878-111">**資産管理** \> **照会** \> **メンテナンス予算** \> **予算**の順に選択します。</span><span class="sxs-lookup"><span data-stu-id="08878-111">Select **Asset management** \> **Inquiries** \> **Maintenance budget** \> **Budget**.</span></span>
2. <span data-ttu-id="08878-112">**予算の作成**を選択します。</span><span class="sxs-lookup"><span data-stu-id="08878-112">Select **Create budget**.</span></span>
3. <span data-ttu-id="08878-113">**メンテナンス予算**フィールドに、予算 ID を入力します。</span><span class="sxs-lookup"><span data-stu-id="08878-113">In the **Maintenance budget** field, enter a budget ID.</span></span>
4. <span data-ttu-id="08878-114">**説明**フィールドに説明を入力します。</span><span class="sxs-lookup"><span data-stu-id="08878-114">In the **Description** field, enter a description.</span></span>
4. <span data-ttu-id="08878-115">**期間**クイック タブの、**開始日**および**終了日**フィールドに、予算期間の開始日と終了日を入力します。</span><span class="sxs-lookup"><span data-stu-id="08878-115">On the **Period** FastTab, in the **From date** and **To date** fields, enter the start and end dates of the budget period.</span></span>
5. <span data-ttu-id="08878-116">前の期間の実際原価に基づいて計算される修正予算原価を含めるには、**修正開始日**フィールドに、これらの原価を含める期間の開始日を入力します。</span><span class="sxs-lookup"><span data-stu-id="08878-116">To include corrective budget costs that are calculated on the basis of actual costs from a previous period, in the **Corrective from date** field, enter the start date of the period that those costs should be included from.</span></span>
6. <span data-ttu-id="08878-117">予算で必要な詳細レベルに応じて、5 つの**グループ化**クイック タブで関連するオプションを設定します。</span><span class="sxs-lookup"><span data-stu-id="08878-117">Depending on the level of detail that is required in the budget, set the relevant options on the five **Group by** FastTabs.</span></span>
7. <span data-ttu-id="08878-118">**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="08878-118">Select **OK**.</span></span>
8. <span data-ttu-id="08878-119">**予算行**を選択して**メンテナンス予算行**ページを開きます。そこでは、期間に対して作成されたすべての予算行が表示されます。</span><span class="sxs-lookup"><span data-stu-id="08878-119">Select **Budget lines** to open **Maintenance budget lines** page, where you can view all the budget lines that have been created for the period.</span></span>
9. <span data-ttu-id="08878-120">予算を承認するには、**メンテナンス予算**ページで予算を選択し、**承認**を選択します。</span><span class="sxs-lookup"><span data-stu-id="08878-120">To approve the budget, select it on the **Maintenance budgets** page, and then select **Approve**.</span></span> <span data-ttu-id="08878-121">次に、**予算の承認**ダイアログ ボックスで、**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="08878-121">Then, in the **Approve budget** dialog box, select **OK**.</span></span> <span data-ttu-id="08878-122">**メンテナンス予算**ページの**承認者**フィールドに、ユーザーの名前が入力されます。</span><span class="sxs-lookup"><span data-stu-id="08878-122">Your name is entered in the **Approved by** field on the **Maintenance budgets** page.</span></span>

    > [!NOTE]
    > <span data-ttu-id="08878-123">メンテナンス予算を承認した後、最初に承認を削除しない限り、**メンテナンス予算行**ページの関連する明細行を再計算または調整することはできません。</span><span class="sxs-lookup"><span data-stu-id="08878-123">After you've approved a maintenance budget, you can't recalculate or adjust the related lines on the **Maintenance budget lines** page unless you first remove the approval.</span></span> <span data-ttu-id="08878-124">メンテナンス予算の承認を削除するには、**メンテナンス予算**ページで予算を選択し、**承認**を選択します。</span><span class="sxs-lookup"><span data-stu-id="08878-124">To remove the approval of a maintenance budget, select it on the **Maintenance budgets** page, and then select **Approve**.</span></span> <span data-ttu-id="08878-125">次に、**予算の承認**ダイアログ ボックスで、**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="08878-125">Then, in the **Approve budget** dialog box, select **OK**.</span></span>

![メンテナンス予算](media/01-maintenance-budgets.png)

<span data-ttu-id="08878-127">既存の予算をコピーして新しいメンテナンス予算を作成することもできます。</span><span class="sxs-lookup"><span data-stu-id="08878-127">You can also create a new maintenance budget by copying an existing budget.</span></span> <span data-ttu-id="08878-128">**メンテナンス予算**ページで、コピーする予算を選択をし、次に**コピー**を選択します。</span><span class="sxs-lookup"><span data-stu-id="08878-128">On the **Maintenance budgets** page, select the budget to copy, and then select **Copy**.</span></span> <span data-ttu-id="08878-129">この方法は、たとえば、1 か月分の予算を作成していて、それを他の月にコピーする場合などに役立ちます。</span><span class="sxs-lookup"><span data-stu-id="08878-129">This approach is useful if, for example, you've created a budget for one month and want to copy it to other months.</span></span>

> [!NOTE]
> <span data-ttu-id="08878-130">メンテナンス予算で計算されるのは、メンテナン ススケジュール行に基づく予算原価のみです。</span><span class="sxs-lookup"><span data-stu-id="08878-130">The maintenance budget calculates only budget costs based on maintenance schedule lines.</span></span> <span data-ttu-id="08878-131">同じ期間の実際原価を計算するには、**資産原価管理**ページで計算を実行します。</span><span class="sxs-lookup"><span data-stu-id="08878-131">To calculate actual costs for the same period, you can do that calculation on the **Asset cost control** page.</span></span> 
