---
title: メンテナンス チェックリスト
description: このトピックでは資産管理のメンテナンス チェックリストについて説明します。
author: josaw1
manager: AnnBe
ms.date: 08/15/2019
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
ms.search.validFrom: 2019-08-15
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 325ff1fa0811d6aac5189cc69f21483fce6b3e8f
ms.sourcegitcommit: f5bfa3212bc3ef7d944a358ef08fe8863fd93b91
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/16/2019
ms.locfileid: "1875762"
---
# <a name="maintenance-checklists"></a><span data-ttu-id="fab93-103">メンテナンス チェックリスト</span><span class="sxs-lookup"><span data-stu-id="fab93-103">Maintenance checklists</span></span>


[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]

<span data-ttu-id="fab93-104">メンテナンス チェックリストは、メンテナンス作業タイプに対して設定され、作業指示書で作業する際に使用されます。</span><span class="sxs-lookup"><span data-stu-id="fab93-104">Maintenance checklists are set up on maintenance job types and used when you work on a work order.</span></span> <span data-ttu-id="fab93-105">メンテナンス チェックリストの入力は、作業指示書を完了するための一部です。</span><span class="sxs-lookup"><span data-stu-id="fab93-105">Filling out maintenance checklists is part of completing a work order.</span></span> <span data-ttu-id="fab93-106">**メンテナンス作業タイプの既定**フォームのメンテナンス作業タイプでメンテナンス チェックリストを設定する方法の詳細については、[メンテナンス作業タイプカテゴリおよびメンテナンス作業タイプ、メンテナンス作業タイプ バリエント、メンテナンス作業の取引、およびメンテナンス チェックリスト](../setup-for-work-orders/job-groups-and-job-types-variants-trades-and-checklists.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="fab93-106">See the [Maintenance job type categories and maintenance job types, maintenance job type variants, maintenance job trades, and maintenance checklists](../setup-for-work-orders/job-groups-and-job-types-variants-trades-and-checklists.md) section for more information on how to set up maintenance checklists on maintenance job types in the **Maintenance job type defaults** form.</span></span>

<span data-ttu-id="fab93-107">作業指示書のメンテナンス チェックリストを使用する場合は、メンテナンス作業タイプに関連する事前定義されたメンテナンス チェックリストに記入できます。</span><span class="sxs-lookup"><span data-stu-id="fab93-107">When you work with maintenance checklists on a work order, you can fill out the predefined maintenance checklists that are related to maintenance job types.</span></span> <span data-ttu-id="fab93-108">また、メンテナンス チェックリストを追加することもできます。</span><span class="sxs-lookup"><span data-stu-id="fab93-108">It is also possible to add additional maintenance checklists.</span></span>

## <a name="fill-out-a-maintenance-checklist"></a><span data-ttu-id="fab93-109">メンテナンス チェックリストへの記入</span><span class="sxs-lookup"><span data-stu-id="fab93-109">Fill out a maintenance checklist</span></span>

1. <span data-ttu-id="fab93-110">**資産管理** > **共通** > **作業指示書** > **すべての作業指示書**または**有効な作業指示書**の順にクリックします。</span><span class="sxs-lookup"><span data-stu-id="fab93-110">Click **Asset management** > **Common** > **Work orders** > **All work orders** or **Active work orders**.</span></span>

2. <span data-ttu-id="fab93-111">作業指示書を選択し、**メンテナンス チェックリスト**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="fab93-111">Select the work order and click **Maintenance checklist**.</span></span>

3. <span data-ttu-id="fab93-112">**作業指示書のメンテナンス作業チェックリスト**には、すべての作業指示書ジョブのメンテナンス チェックリストが表示されます。</span><span class="sxs-lookup"><span data-stu-id="fab93-112">In **Work order maintenance job checklist**, you see maintenance checklists for all work order jobs.</span></span> <span data-ttu-id="fab93-113">作業指示書ジョブに異なるメンテナンス作業タイプがある場合は、メンテナンス チェックリストは各作業指示書ジョブごとに異なる場合があります。</span><span class="sxs-lookup"><span data-stu-id="fab93-113">If the work order jobs have different maintenance job types, the maintenance checklists may be different on each work order job.</span></span> <span data-ttu-id="fab93-114">関連するメンテナンス チェックリストで使用する作業指示書ジョブを選択します。</span><span class="sxs-lookup"><span data-stu-id="fab93-114">Select a work order job to work with the related maintenance checklist.</span></span> <span data-ttu-id="fab93-115">選択したメンテナンスチェックリスト明細行の詳細が**明細行の詳細**クイック タブに表示されます。</span><span class="sxs-lookup"><span data-stu-id="fab93-115">Details of a selected maintenance checklist line are shown on the **Line details** FastTab.</span></span>

4. <span data-ttu-id="fab93-116">すべてのメンテナンス チェックリスト明細行を、一度に 1 つずつ、表示されている順番に入力します。</span><span class="sxs-lookup"><span data-stu-id="fab93-116">Complete all the maintenance checklist lines, one at a time, in the sequential order they are shown.</span></span> <span data-ttu-id="fab93-117">「ヘッダー」タイプのメンテナンス チェックリスト明細行は、下に表示されるメンテナンス チェックリスト明細行をグループ化するための見出しとして使用されます。</span><span class="sxs-lookup"><span data-stu-id="fab93-117">A maintenance checklist line of type "Header" is used as a heading to group the maintenance checklist lines below.</span></span> <span data-ttu-id="fab93-118">ヘッダーの入力は必須ではありませんが、すべてのメンテナンス チェックリスト明細行タイプについて、ヘッダーに**メモ**を追加することができます。</span><span class="sxs-lookup"><span data-stu-id="fab93-118">You are not required to fill out a header, but as for all maintenance checklist line types, it is possible to add a **Note** to the header.</span></span>

5. <span data-ttu-id="fab93-119">指示がメンテナンス チェックリスト明細行に関連している場合は、**指示**チェック ボックスがオンになります。</span><span class="sxs-lookup"><span data-stu-id="fab93-119">If instructions are related to a maintenance checklist line, the **Instructions** check box is selected.</span></span> <span data-ttu-id="fab93-120">**明細行の詳細**クイック タブの**指示**セクションで、選択したメンテナンス チェックリスト明細行の指示を読みます。</span><span class="sxs-lookup"><span data-stu-id="fab93-120">Read instructions for the selected maintenance checklist line on the **Line details** FastTab > **Instructions** section.</span></span>

6. <span data-ttu-id="fab93-121">メンテナンス チェックリストの明細行を完成させるために必要な情報は、関連するメンテナンス チェックリストのタイプによって異なります。</span><span class="sxs-lookup"><span data-stu-id="fab93-121">The information required to complete a maintenance checklist line may vary, depending on the related maintenance checklist type.</span></span> <span data-ttu-id="fab93-122">**明細行の詳細**クイック タブのフィールドに入力して、メンテナンス チェックリストの明細行を完成させます。</span><span class="sxs-lookup"><span data-stu-id="fab93-122">You complete a maintenance checklist line by filling out the fields on the **Line details** FastTab.</span></span> <span data-ttu-id="fab93-123">たとえば、明細行のタイプが「テキスト」の場合は、そのチェックリストの明細行の結果を説明する**メモ**を追加します。</span><span class="sxs-lookup"><span data-stu-id="fab93-123">For example, on a line of type "Text", you add a **Note** explaining what was the result of that checklist line.</span></span> <span data-ttu-id="fab93-124">「測定」タイプの明細行には、機器で読み取った**カウンター値**を追加し、必要に応じて**メモ**を追加することもできます。</span><span class="sxs-lookup"><span data-stu-id="fab93-124">On a line of type "Measurement", you add the **Counter value** you read on the equipment, and you can also add a **Note**, if required.</span></span>

- <span data-ttu-id="fab93-125">メンテナンス チェックリストの明細行を完了したら、その明細行の**チェック済**チェック ボックスをオンにして、完了としてマークします。</span><span class="sxs-lookup"><span data-stu-id="fab93-125">When you have completed a maintenance checklist line, select the **Checked** check box on the line to mark it as completed.</span></span> <span data-ttu-id="fab93-126">メンテナンス チェックリストの明細行が作業指示書ジョブに関係ないために破棄する場合は、明細行の**該当なし**チェック ボックスをオンにします。</span><span class="sxs-lookup"><span data-stu-id="fab93-126">If you want to discard a maintenance checklist line because it's not relevant for the work order job, select the **N/A** check box on the line.</span></span> <span data-ttu-id="fab93-127">メンテナンス チェックリストの明細行が**必須**としてマークされている場合は、「チェック済」または「該当なし」としてマークする必要があります。</span><span class="sxs-lookup"><span data-stu-id="fab93-127">If a maintenance checklist line is marked **Mandatory**, you must mark it as either "Checked" or "N/A".</span></span>  
- <span data-ttu-id="fab93-128">作業指示書が[有効](../setup-for-work-orders/work-order-lifecycle-states.md) なライフサイクルの状態にある場合にのみ、メンテナンス チェックリストの登録を更新できます。</span><span class="sxs-lookup"><span data-stu-id="fab93-128">You can only update maintenance checklist registrations if the work order is in an [Active](../setup-for-work-orders/work-order-lifecycle-states.md) lifecycle state.</span></span>  


## <a name="add-a-maintenance-checklist-line"></a><span data-ttu-id="fab93-129">メンテナンス チェックリストの明細行の追加</span><span class="sxs-lookup"><span data-stu-id="fab93-129">Add a maintenance checklist line</span></span>

<span data-ttu-id="fab93-130">メンテナンス チェックリストは、メンテナンス作業タイプの既定の定義から作成され、作業指示書ジョブに転送されます。</span><span class="sxs-lookup"><span data-stu-id="fab93-130">Maintenance checklists are created from the definition on the maintenance job type default and transferred to a work order job.</span></span> <span data-ttu-id="fab93-131">必要に応じて、メンテナンス チェックリストの明細行を作業指示書ジョブに追加することができます。</span><span class="sxs-lookup"><span data-stu-id="fab93-131">If required, you can add maintenance checklist lines to a work order job.</span></span> <span data-ttu-id="fab93-132">手動で追加されたメンテナンス チェックリストの明細行は参照の「手動」を取得します。</span><span class="sxs-lookup"><span data-stu-id="fab93-132">Manually added maintenance checklist lines get the reference "Manual".</span></span>

1. <span data-ttu-id="fab93-133">**作業指示書のメンテナンス作業チェックリスト**では、メンテナンス チェックリストを追加する作業指示書ジョブを選択します。</span><span class="sxs-lookup"><span data-stu-id="fab93-133">In **Work order maintenance job checklist**, select the work order job for which you want to add a maintenance checklist.</span></span>

2. <span data-ttu-id="fab93-134">**メンテナンス チェックリスト明細行**クイック タブで、選択したメンテナンス チェックリストの明細行の後に新しい明細行を挿入する場合は、メンテナンス チェックリストの明細行を選択し、キーボードの下矢印ボタンを押します。</span><span class="sxs-lookup"><span data-stu-id="fab93-134">On the **Maintenance checklist lines** FastTab, select a maintenance checklist line and press the arrow-down button on your keyboard if you want to insert a new line after the selected maintenance checklist line.</span></span> <span data-ttu-id="fab93-135">シーケンスの次の番号は**行番号**フィールドに自動的に挿入されます。</span><span class="sxs-lookup"><span data-stu-id="fab93-135">The next number in the sequence is automatically inserted in the **Line number** field.</span></span> <span data-ttu-id="fab93-136">選択したメンテナンス チェックリストの明細行の上に新しい明細行を挿入する場合は、メンテナンス チェックリストの明細行を選択し、**明細行の追加**ボタンをクリックします。</span><span class="sxs-lookup"><span data-stu-id="fab93-136">You can also select a maintenance checklist line and click the **Add line** button if you want to insert a new line above the selected maintenance checklist line.</span></span>

3. <span data-ttu-id="fab93-137">メンテナンス チェックリストの明細行の名前を、**名前**フィールドに挿入します。</span><span class="sxs-lookup"><span data-stu-id="fab93-137">Insert a name for the maintenance checklist line in the **Name** field.</span></span>

4. <span data-ttu-id="fab93-138">**タイプ** フィールドで、メンテナンス チェックリスト行のタイプを選択します。</span><span class="sxs-lookup"><span data-stu-id="fab93-138">In the **Type** field, select a type for the maintenance checklist line.</span></span> <span data-ttu-id="fab93-139">各メンテナンス チェックリスト タイプについて、関連するフィールドが**行の詳細**クイック タブに表示されます。</span><span class="sxs-lookup"><span data-stu-id="fab93-139">For each maintenance checklist type, the related fields are shown on the **Line details** FastTab.</span></span>  
  <span data-ttu-id="fab93-140">a.</span><span class="sxs-lookup"><span data-stu-id="fab93-140">a.</span></span> <span data-ttu-id="fab93-141">「テキスト」は、メンテナンス チェックリストの明細行に実行する処理の説明文を追加するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="fab93-141">"Text" is used to add a maintenance checklist line with a text description of what to do.</span></span> <span data-ttu-id="fab93-142">作業者に何かを確認または検査させたいが、特定の (測定可能な) 結果が期待できない場合は、このメンテナンス チェックリスト タイプを使用できます。</span><span class="sxs-lookup"><span data-stu-id="fab93-142">This maintenance checklist type can be used if you want a worker to check or inspect something, without expecting a specific (measurable) result.</span></span> <span data-ttu-id="fab93-143">**明細行の詳細**クイック タブの**指示**セクションで、実行する処理の説明を挿入します。</span><span class="sxs-lookup"><span data-stu-id="fab93-143">Insert a description of what to do in the **Instructions** section on the **Line details** FastTab.</span></span> <span data-ttu-id="fab93-144">b.</span><span class="sxs-lookup"><span data-stu-id="fab93-144">b.</span></span> <span data-ttu-id="fab93-145">「ヘッダー」は、ヘッダーの下に表示されるメンテナンス チェックリストの明細行をグループ化するための見出しとして使用されます。</span><span class="sxs-lookup"><span data-stu-id="fab93-145">"Header" is used as a heading to group the maintenance checklist lines shown below the header.</span></span> <span data-ttu-id="fab93-146">これは、特定の領域に分割できるメンテナンス チェックリストの明細行が複数ある場合に役立ちます。</span><span class="sxs-lookup"><span data-stu-id="fab93-146">This is useful if you have several maintenance checklist lines that can be divided into specific areas.</span></span> <span data-ttu-id="fab93-147">**名前**フィールドに内容を示す名前を挿入します。</span><span class="sxs-lookup"><span data-stu-id="fab93-147">Insert a descriptive name in the **Name** field.</span></span>  
  <span data-ttu-id="fab93-148">c.</span><span class="sxs-lookup"><span data-stu-id="fab93-148">c.</span></span> <span data-ttu-id="fab93-149">「テンプレート」は、作業指示書ジョブにメンテナンス チェックリストの明細行を手動で追加する場合には適用できません。</span><span class="sxs-lookup"><span data-stu-id="fab93-149">"Template" is not applicable when you add a maintenance checklist line manually on a work order job.</span></span>  
  <span data-ttu-id="fab93-150">d.</span><span class="sxs-lookup"><span data-stu-id="fab93-150">d.</span></span> <span data-ttu-id="fab93-151">「変数」は、メンテナンス チェックリストの明細行の範囲内で可能な結果を定義するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="fab93-151">"Variable" is used to define a possible result in a range on a maintenance checklist line.</span></span> <span data-ttu-id="fab93-152">メンテナンス チェックリストの変数の設定については、[メンテナンス作業タイプ カテゴリとメンテナンス作業タイプ、メンテナンス作業タイプ バリアント、メンテナンス作業取引、およびメンテナンス チェックリスト](../setup-for-work-orders/job-groups-and-job-types-variants-trades-and-checklists.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="fab93-152">The setup of maintenance checklist variables is described in [Maintenance job type categories and maintenance job types, maintenance job type variants, maintenance job trades, and maintenance checklists](../setup-for-work-orders/job-groups-and-job-types-variants-trades-and-checklists.md).</span></span> <span data-ttu-id="fab93-153">**名前**フィールドに、変数を説明する名前を挿入します。</span><span class="sxs-lookup"><span data-stu-id="fab93-153">Insert a name to describe the variable in the **Name** field.</span></span> <span data-ttu-id="fab93-154">**変数**フィールドで、変数を選択します。</span><span class="sxs-lookup"><span data-stu-id="fab93-154">Select the variable in the **Variable** field.</span></span> <span data-ttu-id="fab93-155">**明細行の詳細**クイック タブの**指示**セクションで、実行する処理の説明を挿入します。</span><span class="sxs-lookup"><span data-stu-id="fab93-155">Insert a description of what to do in the **Instructions** section on the **Line details** FastTab.</span></span>  
  <span data-ttu-id="fab93-156">e.</span><span class="sxs-lookup"><span data-stu-id="fab93-156">e.</span></span> <span data-ttu-id="fab93-157">「測定」は、特定の測定を記録するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="fab93-157">"Measurement" is used to record a specific measurement.</span></span> <span data-ttu-id="fab93-158">**名前**フィールドに、測定の名前を挿入します。</span><span class="sxs-lookup"><span data-stu-id="fab93-158">Insert a name for the measurement in the **Name** field.</span></span> <span data-ttu-id="fab93-159">**明細行の詳細**クイック タブで、**カウンター**および**単位**を選択します。</span><span class="sxs-lookup"><span data-stu-id="fab93-159">On the **Line details** FastTab, select **Counter** and **Unit**.</span></span> <span data-ttu-id="fab93-160">**指示**セクションに、実行する処理の説明を挿入します。</span><span class="sxs-lookup"><span data-stu-id="fab93-160">Insert a description of what to do in the **Instructions** section.</span></span>  

5. <span data-ttu-id="fab93-161">メンテナンス チェックリストの明細行を手動で追加したら、上記のセクションの説明に従って明細行に入力します。</span><span class="sxs-lookup"><span data-stu-id="fab93-161">When you are done adding maintenance checklist lines manually, fill out the lines as described in the section above.</span></span>

>[!NOTE]
><span data-ttu-id="fab93-162">**作業指示書のメンテナンス作業チェックリスト** では、「作業タイプ」という参照を含むメンテナンス チェックリストの明細行を削除することはできません。</span><span class="sxs-lookup"><span data-stu-id="fab93-162">In **Work order maintenance job checklist**, you can't delete maintenance checklist lines with the reference "Job type".</span></span> <span data-ttu-id="fab93-163">ユーザーまたは他のメンテナンス作業者が手動で作成した、「手動」という参照を含むメンテナンス チェックリストの明細行のみを削除することができます。</span><span class="sxs-lookup"><span data-stu-id="fab93-163">You can only delete maintenance checklist lines with the reference "Manual", which you or other maintenance workers have created manually.</span></span>


![図 1](media/14-work-orders.png)
