---
title: エラー管理
description: このトピックでは、資産管理のエラー管理について説明します。
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
ms.search.validFrom: 2018-08-30
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 78c062f9982ca7b18fa00d60928089d09a5d552d
ms.sourcegitcommit: d37fb09101c30858bcb975931b3d8f947d72017b
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/10/2019
ms.locfileid: "2570958"
---
# <a name="fault-management"></a><span data-ttu-id="5ec03-103">エラー管理</span><span class="sxs-lookup"><span data-stu-id="5ec03-103">Fault management</span></span>

[!include [banner](../../includes/banner.md)]

 

<span data-ttu-id="5ec03-104">資産管理では、エラー デザイナーを使用して、エラー現象、エラー領域、および障害タイプを資産タイプに応じて設定することができます。</span><span class="sxs-lookup"><span data-stu-id="5ec03-104">In Asset Management, you can use the fault designer to set up fault symptoms, fault areas, and fault types on asset types.</span></span> <span data-ttu-id="5ec03-105">これにより、資産上で検出されたエラーを管理できるようになります。</span><span class="sxs-lookup"><span data-stu-id="5ec03-105">In this way, you can manage faults that are detected on assets.</span></span> <span data-ttu-id="5ec03-106">また、エラーの原因と修正に関する提案は、作業指示書に従って登録することができます。</span><span class="sxs-lookup"><span data-stu-id="5ec03-106">Additionally, fault causes and suggestions for fixing faults can be registered on a work order.</span></span>

<span data-ttu-id="5ec03-107">エラー登録と管理のプロセスは、この手順で構成されます。</span><span class="sxs-lookup"><span data-stu-id="5ec03-107">The process for fault registration and management consists of these steps.</span></span>

1. <span data-ttu-id="5ec03-108">資産タイプに関して発生する可能性のあるエラー現象、エラー領域、およびエラー タイプの一覧を作成します。</span><span class="sxs-lookup"><span data-stu-id="5ec03-108">Create a list of fault symptoms, fault areas, and fault types that might occur on your asset types.</span></span>
2. <span data-ttu-id="5ec03-109">エラー デザイナーでは、現象、エラー領域、およびエラー タイプを設定します。</span><span class="sxs-lookup"><span data-stu-id="5ec03-109">In the fault designer, set up symptoms, fault areas, and fault types.</span></span>

<span data-ttu-id="5ec03-110">ここでは、エラー現象、エラー領域、エラー タイプの違いを理解するのに役立つ例を示します。</span><span class="sxs-lookup"><span data-stu-id="5ec03-110">Here are some examples to help you understand the difference between fault symptoms, fault areas, and fault types.</span></span>

<span data-ttu-id="5ec03-111">**エラー現象:**</span><span class="sxs-lookup"><span data-stu-id="5ec03-111">**Fault symptoms:**</span></span>

- <span data-ttu-id="5ec03-112">バランスのとれていない電圧</span><span class="sxs-lookup"><span data-stu-id="5ec03-112">Unbalanced voltages</span></span>
- <span data-ttu-id="5ec03-113">ショート サーキット</span><span class="sxs-lookup"><span data-stu-id="5ec03-113">Short circuit</span></span>
- <span data-ttu-id="5ec03-114">騒音</span><span class="sxs-lookup"><span data-stu-id="5ec03-114">Noise</span></span>
- <span data-ttu-id="5ec03-115">リーク</span><span class="sxs-lookup"><span data-stu-id="5ec03-115">Leak</span></span>
- <span data-ttu-id="5ec03-116">振動</span><span class="sxs-lookup"><span data-stu-id="5ec03-116">Vibrations</span></span>

<span data-ttu-id="5ec03-117">**エラー領域:**</span><span class="sxs-lookup"><span data-stu-id="5ec03-117">**Fault areas:**</span></span>

- <span data-ttu-id="5ec03-118">電気</span><span class="sxs-lookup"><span data-stu-id="5ec03-118">Electrical</span></span>
- <span data-ttu-id="5ec03-119">機械</span><span class="sxs-lookup"><span data-stu-id="5ec03-119">Mechanical</span></span>
- <span data-ttu-id="5ec03-120">油圧</span><span class="sxs-lookup"><span data-stu-id="5ec03-120">Hydraulic</span></span>
- <span data-ttu-id="5ec03-121">エアー</span><span class="sxs-lookup"><span data-stu-id="5ec03-121">Pneumatic</span></span>

<span data-ttu-id="5ec03-122">**エラー タイプ:**</span><span class="sxs-lookup"><span data-stu-id="5ec03-122">**Fault types:**</span></span>

- <span data-ttu-id="5ec03-123">メイン ステーター巻線の不良</span><span class="sxs-lookup"><span data-stu-id="5ec03-123">Faulty main stator winding</span></span>
- <span data-ttu-id="5ec03-124">ダイオードの不良</span><span class="sxs-lookup"><span data-stu-id="5ec03-124">Faulty diode</span></span>
- <span data-ttu-id="5ec03-125">巻線の汚れ</span><span class="sxs-lookup"><span data-stu-id="5ec03-125">Dirty windings</span></span>
- <span data-ttu-id="5ec03-126">発電機の欠陥</span><span class="sxs-lookup"><span data-stu-id="5ec03-126">Defective generator</span></span>
- <span data-ttu-id="5ec03-127">センサーの欠陥</span><span class="sxs-lookup"><span data-stu-id="5ec03-127">Defective sensor</span></span>

## <a name="create-fault-symptoms"></a><span data-ttu-id="5ec03-128">エラー現象を作成</span><span class="sxs-lookup"><span data-stu-id="5ec03-128">Create fault symptoms</span></span>

<span data-ttu-id="5ec03-129">エラー デザイナーで使用できる現象の一覧を作成するには、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="5ec03-129">Follow these steps to create a list of symptoms that can be used in the fault designer.</span></span>

1. <span data-ttu-id="5ec03-130">**資産管理** \> **設定** \> **エラー** \> **エラー現象**を選択します。</span><span class="sxs-lookup"><span data-stu-id="5ec03-130">Select **Asset management** \> **Setup** \> **Fault** \> **Fault symptoms**.</span></span>
2. <span data-ttu-id="5ec03-131">**新規**を選択してレコードを作成します。</span><span class="sxs-lookup"><span data-stu-id="5ec03-131">Select **New** to create a record.</span></span>
3. <span data-ttu-id="5ec03-132">**エラー現象**フィールドに、エラー現象の名前を入力します。</span><span class="sxs-lookup"><span data-stu-id="5ec03-132">In the **Fault symptom** field, enter a name for the fault symptom.</span></span>
4. <span data-ttu-id="5ec03-133">**説明**フィールドに説明を入力します。</span><span class="sxs-lookup"><span data-stu-id="5ec03-133">In the **Description** field, enter a description.</span></span>
5. <span data-ttu-id="5ec03-134">**保存** を選択します。</span><span class="sxs-lookup"><span data-stu-id="5ec03-134">Select **Save**.</span></span>

## <a name="create-fault-areas"></a><span data-ttu-id="5ec03-135">エラー領域を作成</span><span class="sxs-lookup"><span data-stu-id="5ec03-135">Create fault areas</span></span>

<span data-ttu-id="5ec03-136">エラー デザイナーで使用できる領域または場所の一覧を作成するには、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="5ec03-136">Follow these steps to create a list of areas or locations that can be used in the fault designer.</span></span>

1. <span data-ttu-id="5ec03-137">**資産管理** \> **設定** \> **エラー** \> **エラー領域**を選択します。</span><span class="sxs-lookup"><span data-stu-id="5ec03-137">Select **Asset management** \> **Setup** \> **Fault** \> **Fault areas**.</span></span>
2. <span data-ttu-id="5ec03-138">**新規**を選択してレコードを作成します。</span><span class="sxs-lookup"><span data-stu-id="5ec03-138">Select **New** to create a record.</span></span>
3. <span data-ttu-id="5ec03-139">**エラー領域**フィールドに、エラー領域の名前を入力します。</span><span class="sxs-lookup"><span data-stu-id="5ec03-139">In the **Fault area** field, enter a name for the fault area.</span></span>
4. <span data-ttu-id="5ec03-140">**説明**フィールドに説明を入力します。</span><span class="sxs-lookup"><span data-stu-id="5ec03-140">In the **Description** field, enter a description.</span></span>
5. <span data-ttu-id="5ec03-141">**保存** を選択します。</span><span class="sxs-lookup"><span data-stu-id="5ec03-141">Select **Save**.</span></span>

## <a name="create-fault-types"></a><span data-ttu-id="5ec03-142">エラー タイプを作成</span><span class="sxs-lookup"><span data-stu-id="5ec03-142">Create fault types</span></span>

<span data-ttu-id="5ec03-143">エラー デザイナーで使用できるエラー タイプの一覧を作成するには、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="5ec03-143">Follow these steps to create a list of fault types that can be used in the fault designer.</span></span>

1. <span data-ttu-id="5ec03-144">**資産管理** \> **設定** \> **エラー** \> **エラー タイプ**を選択します。</span><span class="sxs-lookup"><span data-stu-id="5ec03-144">Select **Asset management** \> **Setup** \> **Fault** \> **Fault types**.</span></span>
2. <span data-ttu-id="5ec03-145">**新規**を選択してレコードを作成します。</span><span class="sxs-lookup"><span data-stu-id="5ec03-145">Select **New** to create a record.</span></span>
3. <span data-ttu-id="5ec03-146">**エラー タイプ**フィールドに、エラー タイプの名前を入力します。</span><span class="sxs-lookup"><span data-stu-id="5ec03-146">In the **Fault type** field, enter a name for the fault type.</span></span>
4. <span data-ttu-id="5ec03-147">**説明**フィールドに説明を入力します。</span><span class="sxs-lookup"><span data-stu-id="5ec03-147">In the **Description** field, enter a description.</span></span>
5. <span data-ttu-id="5ec03-148">**保存** を選択します。</span><span class="sxs-lookup"><span data-stu-id="5ec03-148">Select **Save**.</span></span>

## <a name="set-up-the-fault-designer"></a><span data-ttu-id="5ec03-149">エラー デザイナーの設定</span><span class="sxs-lookup"><span data-stu-id="5ec03-149">Set up the fault designer</span></span>

<span data-ttu-id="5ec03-150">エラー デザイナーでは、資産タイプに対してエラーのデータを設定します。</span><span class="sxs-lookup"><span data-stu-id="5ec03-150">In the fault designer, you set up fault data on asset types.</span></span>

1. <span data-ttu-id="5ec03-151">**資産管理** \> **設定** \> **エラー** \> **エラー デザイナー**を選択します。</span><span class="sxs-lookup"><span data-stu-id="5ec03-151">Select **Asset management** \> **Setup** \> **Fault** \> **Fault designer**.</span></span>
2. <span data-ttu-id="5ec03-152">左のウィンドウで、エラー レコードを設定する資産のタイプを選択します。</span><span class="sxs-lookup"><span data-stu-id="5ec03-152">In the left pane, select the type of asset to set up a fault record for.</span></span>
3. <span data-ttu-id="5ec03-153">**エラー現象**クイックタブで、**行の追加**を選択し、**エラー現象**フィールドで、エラー現象を選びます。</span><span class="sxs-lookup"><span data-stu-id="5ec03-153">On the **Fault symptom** FastTab, select **Add line**, and then, in the **Fault symptom** field, select a fault symptom.</span></span>
4. <span data-ttu-id="5ec03-154">**エラー領域**クイックタブで、**行の追加**を選択し、**エラー領域**フィールドで、エラー領域を選びます。</span><span class="sxs-lookup"><span data-stu-id="5ec03-154">On the **Fault area** FastTab, select **Add line**, and then, in the **Fault area** field select a fault area.</span></span>
5. <span data-ttu-id="5ec03-155">**エラー タイプ**クイックタブで、**行の追加**を選択し、**エラー タイプ**フィールドで、エラー タイプを選びます。</span><span class="sxs-lookup"><span data-stu-id="5ec03-155">On the **Fault type** FastTab, select **Add line**, and then, in the **Fault type** field, select a fault type.</span></span>
6. <span data-ttu-id="5ec03-156">選択した資産タイプの既存のエラー現象、領域、およびタイプの組み合わせをすばやく作成するには、**エラーの組み合わせを作成**を選択します。</span><span class="sxs-lookup"><span data-stu-id="5ec03-156">To quickly create combinations of all existing fault symptoms, areas, and types for the selected asset type, select **Create fault combinations**.</span></span> <span data-ttu-id="5ec03-157">この機能は、エラー現象、領域、およびタイプを多数追加している場合に役立ちます。</span><span class="sxs-lookup"><span data-stu-id="5ec03-157">This function is useful if you've added many fault symptoms, areas, and types.</span></span> <span data-ttu-id="5ec03-158">資産タイプに関連しない組み合わせの明細行は、新しい明細行を手動で作成するよりも簡単に削除できます。</span><span class="sxs-lookup"><span data-stu-id="5ec03-158">It's easier to delete the lines for any combinations that aren't relevant to the asset type than to create new lines manually.</span></span>

    > [!NOTE]
    > <span data-ttu-id="5ec03-159">1 つの資産タイプから選択した資産タイプに対するエラー現象、領域、タイプの設定をコピーするには、**資産タイプからコピー**を選択します。</span><span class="sxs-lookup"><span data-stu-id="5ec03-159">To copy the setup of fault symptoms, areas, and types from one asset type to the selected asset type, select **Copy from asset type**.</span></span>

7. <span data-ttu-id="5ec03-160">**保存**をクリックして、変更を保存します。</span><span class="sxs-lookup"><span data-stu-id="5ec03-160">Select **Save** to save your changes.</span></span>

![エラー デザイナーのページ](media/21-setup-for-work-orders.png)

## <a name="create-fault-causes"></a><span data-ttu-id="5ec03-162">エラー原因タイプを作成</span><span class="sxs-lookup"><span data-stu-id="5ec03-162">Create fault causes</span></span>

<span data-ttu-id="5ec03-163">次の手順に従って、既知のエラー原因の一覧を作成し、それを作業指示書またはメンテナンス要求に追加できます。</span><span class="sxs-lookup"><span data-stu-id="5ec03-163">Follow these steps to create a list of known fault causes that can be added to a work order or a maintenance request.</span></span>

1. <span data-ttu-id="5ec03-164">**資産管理** \> **設定** \> **エラー** \> **エラー原因**を選択します。</span><span class="sxs-lookup"><span data-stu-id="5ec03-164">Select **Asset management** \> **Setup** \> **Fault** \> **Fault causes**.</span></span>
2. <span data-ttu-id="5ec03-165">**新規**を選択してレコードを作成します。</span><span class="sxs-lookup"><span data-stu-id="5ec03-165">Select **New** to create a record.</span></span>
3. <span data-ttu-id="5ec03-166">**エラー原因**フィールドに、エラー原因の名前を入力します。</span><span class="sxs-lookup"><span data-stu-id="5ec03-166">In the **Fault cause** field, enter a name for the fault cause.</span></span>
4. <span data-ttu-id="5ec03-167">**説明**フィールドに説明を入力します。</span><span class="sxs-lookup"><span data-stu-id="5ec03-167">In the **Description** field, enter a description.</span></span>
5. <span data-ttu-id="5ec03-168">**保存** を選択します。</span><span class="sxs-lookup"><span data-stu-id="5ec03-168">Select **Save**.</span></span>

## <a name="create-fault-remedies"></a><span data-ttu-id="5ec03-169">エラー救済を作成</span><span class="sxs-lookup"><span data-stu-id="5ec03-169">Create fault remedies</span></span>

<span data-ttu-id="5ec03-170">次の手順に従って、救済と修復に向けた提案の一覧を作成し、それを作業指示書またはメンテナンス要求に追加できます。</span><span class="sxs-lookup"><span data-stu-id="5ec03-170">Follow these steps to create a list of suggestions for remedy and repair that can be added to a work order or a maintenance request.</span></span>

1. <span data-ttu-id="5ec03-171">**資産管理** \> **設定** \> **エラー** \> **エラー救済**を選択します。</span><span class="sxs-lookup"><span data-stu-id="5ec03-171">Select **Asset management** \> **Setup** \> **Fault** \> **Fault remedies**.</span></span>
2. <span data-ttu-id="5ec03-172">**新規**を選択してレコードを作成します。</span><span class="sxs-lookup"><span data-stu-id="5ec03-172">Select **New** to create a record.</span></span>
3. <span data-ttu-id="5ec03-173">**エラー救済**フィールドに、エラーの救済の名前を入力します。</span><span class="sxs-lookup"><span data-stu-id="5ec03-173">In the **Fault remedy** field, enter a name for the fault remedy.</span></span>
4. <span data-ttu-id="5ec03-174">**説明**フィールドに説明を入力します。</span><span class="sxs-lookup"><span data-stu-id="5ec03-174">In the **Description** field, enter a description.</span></span>
5. <span data-ttu-id="5ec03-175">**保存** を選択します。</span><span class="sxs-lookup"><span data-stu-id="5ec03-175">Select **Save**.</span></span>

> [!NOTE]
> <span data-ttu-id="5ec03-176">エラー現象、領域、タイプ、原因、および救済の名前は必要に応じて変更できます。</span><span class="sxs-lookup"><span data-stu-id="5ec03-176">You can change the names of your fault symptoms, areas, types, causes, and remedies as you require.</span></span> <span data-ttu-id="5ec03-177">名前の変更は、関連するエラー登録に自動的に反映されます。</span><span class="sxs-lookup"><span data-stu-id="5ec03-177">The name changes are automatically reflected in the related fault registrations.</span></span>
