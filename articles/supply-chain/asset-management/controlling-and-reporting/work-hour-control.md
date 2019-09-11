---
title: 作業時間の管理
description: このトピックでは、資産管理での作業時間の管理について説明します。
author: josaw1
manager: AnnBe
ms.date: 08/23/2019
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
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 916e7b8d5d494dbae0659504957f7f0798a6834b
ms.sourcegitcommit: 2292b54e2da96f71b59ec9ccf17cd32d3d1d8b21
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2019
ms.locfileid: "1918375"
---
# <a name="work-hour-control"></a><span data-ttu-id="55371-103">作業時間の管理</span><span class="sxs-lookup"><span data-stu-id="55371-103">Work hour control</span></span>

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]

<span data-ttu-id="55371-104">資産管理では、時間を計算して、資産、機能的な場所、またはワーク オーダーの予算時間と比較した実際の時間の概要を取得できます。</span><span class="sxs-lookup"><span data-stu-id="55371-104">In Asset Management, you can calculate hours to get an overview of actual hours compared to budget hours on assets, functional locations, or work orders.</span></span> <span data-ttu-id="55371-105">実際の時間は、転記されたトランザクションに基づいています。</span><span class="sxs-lookup"><span data-stu-id="55371-105">Actual hours are based on posted transactions.</span></span>

## <a name="work-hour-control-for-assets-functional-locations-and-work-orders"></a><span data-ttu-id="55371-106">資産、機能的な場所、およびワーク オーダーの作業時間管理</span><span class="sxs-lookup"><span data-stu-id="55371-106">Work hour control for assets, functional locations, and work orders</span></span>

<span data-ttu-id="55371-107">資産、機能的な場所、およびワーク オーダーに対して行われる計算は、ほぼ同一です。</span><span class="sxs-lookup"><span data-stu-id="55371-107">The calculations made for assets, functional locations, and work orders are almost identical.</span></span> <span data-ttu-id="55371-108">唯一の違いは、資産と機能的な場所に対して、下位資産とサブ場所を計算に含めることもできるという点です。</span><span class="sxs-lookup"><span data-stu-id="55371-108">Only difference is that for assets and functional locations, you can also include sub assets and sub locations in your calculation.</span></span> <span data-ttu-id="55371-109">日付は、登録が記録されたトランザクション日付です。</span><span class="sxs-lookup"><span data-stu-id="55371-109">The date is the transaction date when the registration was recorded.</span></span>

1. <span data-ttu-id="55371-110">**資産管理** > **照会** > **資産** > **資産時間管理**または**機能的な場所の時間管理**、または**資産管理** > **照会** > **ワーク オーダー** > **ワーク オーダー時間管理**をクリックしてください。</span><span class="sxs-lookup"><span data-stu-id="55371-110">Click **Asset management** > **Inquiries** > **Assets** > **Asset hour control** or **Functional location hour control**, or **Asset management** > **Inquiries** > **Work orders** > **Work order hour control**.</span></span>

2. <span data-ttu-id="55371-111">**資産時間管理**ダイアログで。</span><span class="sxs-lookup"><span data-stu-id="55371-111">In the **Asset hour control** dialog, .</span></span>

3. <span data-ttu-id="55371-112">**資産時間管理** / **機能的な場所の時間管理** / **ワーク オーダー時間管理**ダイアログで、**開始日**と**終了日**フィールドで計算する期間を選択します。</span><span class="sxs-lookup"><span data-stu-id="55371-112">In the **Asset hour control** / **Functional location hour control** / **Work order hour control** dialog, select a period to be calculated in the **From date** and **To date** fields.</span></span>

4. <span data-ttu-id="55371-113">必要に応じて、計算に含める**財務分析コード セット**を選択します。</span><span class="sxs-lookup"><span data-stu-id="55371-113">If required, select a **Financial dimension set** to be included in the calculation.</span></span>

5. <span data-ttu-id="55371-114">ゼロ時間を含む結果を表示しない場合は、**ゼロをスキップ** トグル ボタンで「はい」を選択します。</span><span class="sxs-lookup"><span data-stu-id="55371-114">Select "Yes" on the **Skip zero** toggle button if you don't want to show results containing zero hours.</span></span>

6. <span data-ttu-id="55371-115">**レベル** フィールドを使用すると、機能的な場所に関する時間管理明細行の詳細度を指定できます。</span><span class="sxs-lookup"><span data-stu-id="55371-115">You can use the **Level** field to indicate how detailed you want the hour control lines to be regarding functional locations.</span></span> <span data-ttu-id="55371-116">たとえば、フィールドに数値 "1" を挿入し、複数レベルの機能的な場所の階層がある場合、機能的な場所に対するすべての時間管理明細行が最上位レベルに表示されます。そのため、明細行の時間が下位レベルにある機能的な場所から追加されます。</span><span class="sxs-lookup"><span data-stu-id="55371-116">For example, if you insert the number "1" in the field, and you have a multi-level functional location hierarchy, all hour control lines for a functional location will be shown on the top level, and therefore the hours on a line may be added up from functional locations located at a lower level.</span></span> <span data-ttu-id="55371-117">**レベル** フィールドに数値 "0" を挿入すると、関連するすべての機能的な場所レベルのすべての時間管理明細行を示す詳細結果が表示されます。</span><span class="sxs-lookup"><span data-stu-id="55371-117">If you insert the number "0" in the **Level** field, you will see a detailed result showing all hour control lines on all the functional location levels to which they are related.</span></span>

7. <span data-ttu-id="55371-118">**下位資産を含める**トグルボタンで「はい」を選択し、下位資産に関連する原価を別の明細行として表示します。</span><span class="sxs-lookup"><span data-stu-id="55371-118">Select "Yes" on the **Include sub assets** toggle button to show costs related to sub assets as separate lines.</span></span>

8. <span data-ttu-id="55371-119">検索を制限する場合は、**対象に含めるレコード** クイック タブで特定の資産、機能的な場所、およびワーク オーダーを選択できます。</span><span class="sxs-lookup"><span data-stu-id="55371-119">If you want to limit the search, you can select specific assets / functional locations / work orders on the **Records to include** FastTab.</span></span>

9. <span data-ttu-id="55371-120">**OK** をクリックして、計算を開始します。</span><span class="sxs-lookup"><span data-stu-id="55371-120">Click **OK** to start the calculation.</span></span>

10. <span data-ttu-id="55371-121">**資産時間管理**ページの**グループ化**アクション ウィンドウ グループで、関連するボタンをクリックすると、計算の必要な詳細レベルが表示されます。</span><span class="sxs-lookup"><span data-stu-id="55371-121">On the **Asset hour control** page, in the **Group by...** action pane groups, click the relevant buttons to show the required detail level of the calculation.</span></span> <span data-ttu-id="55371-122">選択したアクション ウィンドウ ボタンが強調表示されます。</span><span class="sxs-lookup"><span data-stu-id="55371-122">The selected action pane buttons are highlighted.</span></span> <span data-ttu-id="55371-123">ボタンをクリックして、有効または無効にします。</span><span class="sxs-lookup"><span data-stu-id="55371-123">Click on a button to activate or deactivate it.</span></span>

<span data-ttu-id="55371-124">次の図は、**資産時間管理**の計算例を示します。</span><span class="sxs-lookup"><span data-stu-id="55371-124">The figure below shows an example of an **Asset hour control** calculation.</span></span>

![図 1](media/04-controlling-and-reporting.png)

<span data-ttu-id="55371-126">時間計算を行う別の方法は、**すべての資産**または**有効な資産**で複数の資産を選択することです。</span><span class="sxs-lookup"><span data-stu-id="55371-126">Another way of making an hour calculation is to multi-select assets in **All assets** or **Active assets**.</span></span> <span data-ttu-id="55371-127">その後、**一般**クイック タブの**時間管理**ボタンをクリックします。</span><span class="sxs-lookup"><span data-stu-id="55371-127">Then, you click the **Hour control** button on the **General** FastTab.</span></span> <span data-ttu-id="55371-128">選択した資産は、**対象に含めるレコード** クイック タブの**資産**フィールドに自動的に挿入されます。</span><span class="sxs-lookup"><span data-stu-id="55371-128">The selected assets are automatically inserted in the **Asset** field on the **Records to include** FastTab.</span></span> <span data-ttu-id="55371-129">**資産時間管理**ダイアログで **OK** をクリックすると、選択した資産の計算が表示されます。</span><span class="sxs-lookup"><span data-stu-id="55371-129">Click **OK** in the **Asset hour control** dialog, and the calculation for the selected assets is shown.</span></span> <span data-ttu-id="55371-130">同じ手順を、**すべての機能的な場所**または**有効な機能的な場所**の機能的な場所、および**すべてのワーク オーダー**または**有効なワーク オーダー**のワーク オーダーに対して実行できます。</span><span class="sxs-lookup"><span data-stu-id="55371-130">The same procedure can be done for functional locations in **All functional locations** or **Active functional locations**, and for work orders in **All work orders** or **Active work orders**.</span></span>

>[!NOTE]
><span data-ttu-id="55371-131">**元の予算**フィールドでは、ワーク オーダー予測からの予算時間が表示されます。</span><span class="sxs-lookup"><span data-stu-id="55371-131">The **Original budget** field shows budget hours from the work order forecast.</span></span> <span data-ttu-id="55371-132">**実際の時間**フィールドには、ワーク オーダーの転記済時間が表示されます。</span><span class="sxs-lookup"><span data-stu-id="55371-132">The **Actual hours** field shows posted hours on work orders.</span></span> <span data-ttu-id="55371-133">**確定済み時間**フィールドには、ワーク オーダーに関連して会社が確定した時間の合計量が表示されます。</span><span class="sxs-lookup"><span data-stu-id="55371-133">The **Committed hours** field shows total amount of hours that your company is committed to in relation to work orders.</span></span>

