---
title: ウェーブの作成と処理
description: このトピックでは、ウェーブを作成、処理、リリースして、積荷、出荷、製造オーダー、またはかんばんオーダーのピッキングの作業を作成する方法を説明します。
author: Mirzaab
ms.date: 03/08/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WHSWaveTemplateTable, WHSParameters, whswavetablecreatenew, WHSWaveTable, WHSWaveAttributes, WHSKanbanWaveTable, WHSWaveTableListPage, WHSKanbanWaveTableListPage, WHSProdWaveTable
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2021-03-08
ms.dyn365.ops.version: Release 10.0.18
ms.openlocfilehash: 4bf47b15b668a37f12edb3dbb842d19655fac97a
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/11/2021
ms.locfileid: "6019030"
---
# <a name="wave-creation-and-processing"></a><span data-ttu-id="c38a3-103">ウェーブの作成と処理</span><span class="sxs-lookup"><span data-stu-id="c38a3-103">Wave creation and processing</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="c38a3-104">このトピックでは、ウェーブを作成、処理、リリースして、積荷、出荷、製造オーダー、またはかんばんオーダーのピッキングの作業を作成する方法を説明します。</span><span class="sxs-lookup"><span data-stu-id="c38a3-104">This topic describes how to create, process, and release a wave to create picking work for a load, shipment, production order, or kanban order.</span></span> <span data-ttu-id="c38a3-105">次の注文タイプで必要なウェーブを作成できます。</span><span class="sxs-lookup"><span data-stu-id="c38a3-105">You can create waves for the following types of orders:</span></span>

- <span data-ttu-id="c38a3-106">**販売注文** – 販売注文の明細行を含む出荷ウェーブを使用します。</span><span class="sxs-lookup"><span data-stu-id="c38a3-106">**Sales orders** – Use shipping waves to include lines from sales orders.</span></span> <span data-ttu-id="c38a3-107">販売注文が倉庫にリリースされると、販売注文明細行をウェーブに含めることができます。</span><span class="sxs-lookup"><span data-stu-id="c38a3-107">When a sales order is released to the warehouse, the sales order lines can be included in the wave.</span></span>
- <span data-ttu-id="c38a3-108">**製造オーダー** – 製品ウェーブを使用して、製品の部品表 (BOM) の明細行を含めます。</span><span class="sxs-lookup"><span data-stu-id="c38a3-108">**Production orders** – Use production waves to include lines from the bill of materials (BOM) for a product.</span></span>
- <span data-ttu-id="c38a3-109">**かんばんオーダー** – かんばんウェーブには、かんばんオーダーのピッキング リスト明細行が含まれます。</span><span class="sxs-lookup"><span data-stu-id="c38a3-109">**Kanban orders** – Kanban waves include picking list lines from kanban orders.</span></span>

<span data-ttu-id="c38a3-110">販売注文とかんばん注文では、棚卸資産は注文が倉庫にリリースされる前に引当する必要があります。</span><span class="sxs-lookup"><span data-stu-id="c38a3-110">For sales orders and kanban orders, inventory must be reserved before the order is released to the warehouse.</span></span> <span data-ttu-id="c38a3-111">そうしなければ、品門行または配賦行はウェーブで処理することはできません。</span><span class="sxs-lookup"><span data-stu-id="c38a3-111">Otherwise, the items or allocation lines can't be processed in a wave.</span></span> <span data-ttu-id="c38a3-112">ただし、製造オーダーはもう少し柔軟です。</span><span class="sxs-lookup"><span data-stu-id="c38a3-112">However, production orders are slightly more flexible.</span></span> <span data-ttu-id="c38a3-113">製造オーダーの場合は、次のいずれかのオプションを選択できます。</span><span class="sxs-lookup"><span data-stu-id="c38a3-113">For production orders, you can choose either of the following options:</span></span>

- <span data-ttu-id="c38a3-114">注文が倉庫にリリースされる前に、すべての材料が引当される必要があります。</span><span class="sxs-lookup"><span data-stu-id="c38a3-114">Require that all materials are reserved before an order can be released to the warehouse.</span></span>
- <span data-ttu-id="c38a3-115">すべての材料を引当することができなくても、製造オーダーが倉庫にリリースされるようにします。</span><span class="sxs-lookup"><span data-stu-id="c38a3-115">Allow production orders to be released to the warehouse even though all materials can't be reserved.</span></span> <span data-ttu-id="c38a3-116">このオプションを選択する場合、追加の材料が使用可能になるときに、倉庫プロセスに手動でリリースを繰り返す必要があります。</span><span class="sxs-lookup"><span data-stu-id="c38a3-116">If you select this option, you must manually repeat the release to warehouse process when the additional materials become available.</span></span> <span data-ttu-id="c38a3-117">たとえば、生産を開始する必要がある材料があり、追加の材料が利用可能になるまで待機できる場合に役立ちます。</span><span class="sxs-lookup"><span data-stu-id="c38a3-117">For example, this is useful if you have the materials that you need to start a production, and can wait until the additional materials become available.</span></span>

<span data-ttu-id="c38a3-118">**生産管理パラメーター** ページにある **材料の予約要求** フィールド使用して、どの製造オーダー オプションを使用するかを既定で指定することができます。</span><span class="sxs-lookup"><span data-stu-id="c38a3-118">You can specify which of these production order options to use by default using the **Requirement for material reservation** field on the **Production control parameters** page.</span></span> <span data-ttu-id="c38a3-119">ただし、特定の各製造オーダーの設定は必要に応じて変更できます。</span><span class="sxs-lookup"><span data-stu-id="c38a3-119">However, you can change the setting for each specific production order as needed.</span></span> <span data-ttu-id="c38a3-120">詳細については、[ウェーブ処理の倉庫パラメータ](wave-warehouse-parameters.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="c38a3-120">For more information, see [Warehouse parameters for wave processing](wave-warehouse-parameters.md).</span></span>

## <a name="create-and-process-a-wave"></a><span data-ttu-id="c38a3-121">ウェーブの作成および処理</span><span class="sxs-lookup"><span data-stu-id="c38a3-121">Create and process a wave</span></span>

<span data-ttu-id="c38a3-122">次の図は、出荷のウェーブの作成、処理、およびリリース方法を表しています。</span><span class="sxs-lookup"><span data-stu-id="c38a3-122">The following diagram shows the flow for how shipping waves are created, processed, and released.</span></span> <span data-ttu-id="c38a3-123">番号は、このセクションの後のセクションに対応します。</span><span class="sxs-lookup"><span data-stu-id="c38a3-123">The numbers correspond to the sections later in this section.</span></span>

<span data-ttu-id="c38a3-124">![ウェーブ作成の処理](media/wave-processing-diagram.png "ウェーブ作成の処理")</span><span class="sxs-lookup"><span data-stu-id="c38a3-124">![Process for creating a wave](media/wave-processing-diagram.png "Process for creating a wave")</span></span>

### <a name="prerequisites"></a><span data-ttu-id="c38a3-125">必要条件</span><span class="sxs-lookup"><span data-stu-id="c38a3-125">Prerequisites</span></span>

<span data-ttu-id="c38a3-126">開始する前に、作成したいウェーブのタイプに必要なウェーブ テンプレートが使用できる状態である必要があります (出荷、生産、またはりかんばん)。</span><span class="sxs-lookup"><span data-stu-id="c38a3-126">Before you start, a wave template must be available for the type of wave you want to create (shipping, production, or kanban).</span></span> <span data-ttu-id="c38a3-127">ウェーブ テンプレートには、手動で実行する必要があるステップや自動的に実行されるステップなど、どのようにウェーブが生成および処理されるかに関するさまざまな設定があります。</span><span class="sxs-lookup"><span data-stu-id="c38a3-127">The wave template establishes many settings for how the wave will be generated and processed, including which steps must be done manually and which are done automatically.</span></span> <span data-ttu-id="c38a3-128">テンプレートの詳細については、[ウェーブ テンプレート](wave-templates.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="c38a3-128">For more information, see [Wave templates](wave-templates.md).</span></span>

### <a name="create-a-wave"></a><span data-ttu-id="c38a3-129">ウェーブの作成</span><span class="sxs-lookup"><span data-stu-id="c38a3-129">Create a wave</span></span>

#### <a name="automatically-create-waves-based-on-warehouse-and-order-type"></a><span data-ttu-id="c38a3-130">倉庫と注文タイプに基づいて自動的にウェーブを作成する</span><span class="sxs-lookup"><span data-stu-id="c38a3-130">Automatically create waves based on warehouse and order type</span></span>

<span data-ttu-id="c38a3-131">ウェーブを自動的に作成するには、関連する各注文タイプと倉庫に適応する [ウェーブ テンプレート](wave-templates.md) を設定します。</span><span class="sxs-lookup"><span data-stu-id="c38a3-131">To create waves automatically, set up [Wave templates](wave-templates.md) that apply for each relevant order type and warehouse.</span></span> <span data-ttu-id="c38a3-132">各テンプレートの **ウェーブ作成の自動化** オプションが *はい* に設定されているかを確認します。</span><span class="sxs-lookup"><span data-stu-id="c38a3-132">Make sure each template has the **Automate wave creation** option set to *Yes*.</span></span>

#### <a name="manually-create-waves"></a><span data-ttu-id="c38a3-133">ウェーブを手動で作成する</span><span class="sxs-lookup"><span data-stu-id="c38a3-133">Manually create waves</span></span>

<span data-ttu-id="c38a3-134">ウェーブを手動で作成するには、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="c38a3-134">To manually create a wave, follow these steps:</span></span>

1. <span data-ttu-id="c38a3-135">手動で倉庫と注文タイプのウェーブを作成したい場合、関連する [ウェーブ テンプレート](wave-templates.md) が、倉庫と注文タイプのウェーブの自動作成に設定されていないことを確認します。</span><span class="sxs-lookup"><span data-stu-id="c38a3-135">Make sure that the relevant [Wave templates](wave-templates.md) aren't set to automatically create a wave for the warehouse and order types where you want to do so manually.</span></span>
1. <span data-ttu-id="c38a3-136">作成するウェーブのタイプに応じて、次のいずれかを実行します。</span><span class="sxs-lookup"><span data-stu-id="c38a3-136">Depending on the type of wave you want to create, do one of the following:</span></span>

    - <span data-ttu-id="c38a3-137">**倉庫管理** \> **一般** \> **ウェーブ** \> **出荷ウェーブ** \> **すべてのウェーブ** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="c38a3-137">Go to **Warehouse management** \> **Common** \> **Waves** \> **Shipment waves** \> **All waves**.</span></span> <span data-ttu-id="c38a3-138">アクション ウィンドウで、**ウェーブ** を選択します。</span><span class="sxs-lookup"><span data-stu-id="c38a3-138">On the Action Pane, select **Wave**.</span></span>
    - <span data-ttu-id="c38a3-139">**倉庫管理** \> **一般** \> **ウェーブ** \> **生産ウェーブ** \> **すべての生産ウェーブ** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="c38a3-139">Go to **Warehouse management** \> **Common** \> **Waves** \> **Production waves** \> **All production waves**.</span></span> <span data-ttu-id="c38a3-140">アクション ウィンドウで、**生産ウェーブ** を選択します。</span><span class="sxs-lookup"><span data-stu-id="c38a3-140">On the Action Pane, select **Production wave**.</span></span>
    - <span data-ttu-id="c38a3-141">**倉庫管理** \> **一般** \> **ウェーブ** \> **かんばんウェーブ** \> **すべてのかんばんウェーブ** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="c38a3-141">Go to **Warehouse management** \> **Common** \> **Waves** \> **Kanban waves** \> **All kanban waves**.</span></span> <span data-ttu-id="c38a3-142">アクション ウィンドウで、**ウェーブの作成** を選択します。</span><span class="sxs-lookup"><span data-stu-id="c38a3-142">On the Action Pane, select **Create wave**.</span></span>

1. <span data-ttu-id="c38a3-143">**説明** フィールドに、ウェーブの簡単な説明を入力します。</span><span class="sxs-lookup"><span data-stu-id="c38a3-143">In the **Description** field, enter a short description of the wave.</span></span> <span data-ttu-id="c38a3-144">これはウェーブで何を処理しているかを示します。</span><span class="sxs-lookup"><span data-stu-id="c38a3-144">This should indicate what you are processing in the wave.</span></span>

1. <span data-ttu-id="c38a3-145">**ウェーブ テンプレート名** フィールドで、作成するウェーブのタイプのウェーブ テンプレートを選択します。</span><span class="sxs-lookup"><span data-stu-id="c38a3-145">In the **Wave template name** field, select the wave template for the type of wave to create.</span></span> <span data-ttu-id="c38a3-146">ウェーブ テンプレートは、ウェーブの作業の作成などのアクションを実行するウェーブの方法が含まれます。</span><span class="sxs-lookup"><span data-stu-id="c38a3-146">The wave template contains the wave methods that will perform actions such as creating work for the wave.</span></span> <span data-ttu-id="c38a3-147">たとえば、出荷ウェーブのウェーブ テンプレートは、積荷の作成、ウェーブへの明細行の割り当て、補充、およびウェーブのピッキングの作業の作成の方法を含めることができます。</span><span class="sxs-lookup"><span data-stu-id="c38a3-147">For example, the wave template for shipping waves can contain methods for creating loads, allocating lines to waves, replenishment, and creating picking work for the wave.</span></span>

1. <span data-ttu-id="c38a3-148">ウェーブの追加のクエリ基準としてウェーブ属性を使用する場合、**ウェーブ属性** フィールドで属性を選択します。</span><span class="sxs-lookup"><span data-stu-id="c38a3-148">If you want to use wave attributes as additional query criteria for the wave, select the attributes in the **Wave attributes** fields.</span></span>

### <a name="specify-what-to-include-in-a-wave"></a><span data-ttu-id="c38a3-149">ウェーブに含めるものを指定する</span><span class="sxs-lookup"><span data-stu-id="c38a3-149">Specify what to include in a wave</span></span>

<span data-ttu-id="c38a3-150">ウェーブを作成したら、コンテンツを追加することができます。</span><span class="sxs-lookup"><span data-stu-id="c38a3-150">After a wave has been created, you are ready to start adding content to it.</span></span>

> [!NOTE]
> <span data-ttu-id="c38a3-151">必要に応じて、処理後でもリリースされない限りは、ウェーブに明細行を追加できます。</span><span class="sxs-lookup"><span data-stu-id="c38a3-151">If needed, you can add lines to a wave even after it has been processed as long as it has not been released.</span></span>

#### <a name="automatically-specify-what-to-include-in-a-wave"></a><span data-ttu-id="c38a3-152">ウェーブに含めるものを自動指定する</span><span class="sxs-lookup"><span data-stu-id="c38a3-152">Automatically specify what to include in a wave</span></span>

<span data-ttu-id="c38a3-153">ウェーブを自動的に作成するには、関連する各注文タイプと倉庫に適応する [ウェーブ テンプレート](wave-templates.md) を設定します。</span><span class="sxs-lookup"><span data-stu-id="c38a3-153">To create waves automatically, set up [Wave templates](wave-templates.md) that apply for each relevant order type and warehouse.</span></span> <span data-ttu-id="c38a3-154">各テンプレートの **ウェーブ作成の自動化** オプションが *はい* に設定されているかを確認します。</span><span class="sxs-lookup"><span data-stu-id="c38a3-154">Make sure each template has the **Automate wave creation** option set to *Yes*.</span></span> <span data-ttu-id="c38a3-155">また、**オープンのウェーブに割り当て** オプションが *はい* に設定されている場合、テンプレートを使用して適用できるどのオープン ウェーブにでも明細行を割り当てることもできます。</span><span class="sxs-lookup"><span data-stu-id="c38a3-155">Alternatively, your template could automatically assign lines to any qualifying open wave if the **Assign to open waves** option is set to *Yes*.</span></span>

#### <a name="manually-specify-what-to-include-in-a-wave"></a><span data-ttu-id="c38a3-156">ウェーブに含めるものを手動指定する</span><span class="sxs-lookup"><span data-stu-id="c38a3-156">Manually specify what to include in a wave</span></span>

<span data-ttu-id="c38a3-157">ウェーブを作成したけれど、まだリリースされていない場合、ウェーブに含める項目を手動で指定できます。</span><span class="sxs-lookup"><span data-stu-id="c38a3-157">When a wave has been created but not yet released, you can manually specify what to include in it.</span></span> <span data-ttu-id="c38a3-158">手動でウェーブに明細行を追加するには、次の操作を行います。</span><span class="sxs-lookup"><span data-stu-id="c38a3-158">To add lines to a wave manually:</span></span>

1. <span data-ttu-id="c38a3-159">明細行を追加するウェーブのタイプに応じて、次を実行します。</span><span class="sxs-lookup"><span data-stu-id="c38a3-159">Depending on the type of wave to add lines to, do one of the following:</span></span>

    - <span data-ttu-id="c38a3-160">**倉庫管理** \> **一般** \> **ウェーブ** \> **出荷ウェーブ** \> **すべてのウェーブ** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="c38a3-160">Go to **Warehouse management** \> **Common** \> **Waves** \> **Shipment waves** \> **All waves**.</span></span> <span data-ttu-id="c38a3-161">アクション ウィンドウで、**ウェーブ** を選択します。</span><span class="sxs-lookup"><span data-stu-id="c38a3-161">On the Action Pane, select **Wave**.</span></span>
    - <span data-ttu-id="c38a3-162">**倉庫管理** \> **一般** \> **ウェーブ** \> **生産ウェーブ** \> **すべての生産ウェーブ** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="c38a3-162">Go to **Warehouse management** \> **Common** \> **Waves** \> **Production waves** \> **All production waves**.</span></span> <span data-ttu-id="c38a3-163">アクション ウィンドウで、**生産ウェーブ** を選択します。</span><span class="sxs-lookup"><span data-stu-id="c38a3-163">On the Action Pane, select **Production wave**.</span></span>
    - <span data-ttu-id="c38a3-164">**倉庫管理** \> **一般** \> **ウェーブ** \> **かんばんウェーブ** \> **すべてのかんばんウェーブ** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="c38a3-164">Go to **Warehouse management** \> **Common** \> **Waves** \> **Kanban waves** \> **All kanban waves**.</span></span> <span data-ttu-id="c38a3-165">アクション ウィンドウで、**ウェーブの作成** を選択します。</span><span class="sxs-lookup"><span data-stu-id="c38a3-165">On the Action Pane, select **Create wave**.</span></span>

1. <span data-ttu-id="c38a3-166">ウェーブを選択します。</span><span class="sxs-lookup"><span data-stu-id="c38a3-166">Select the wave.</span></span> <span data-ttu-id="c38a3-167">[アクション ウィンドウ] で、次のいずれかを選択します。</span><span class="sxs-lookup"><span data-stu-id="c38a3-167">On the Action Pane, select one of the following:</span></span>

      - <span data-ttu-id="c38a3-168">**出荷の管理**</span><span class="sxs-lookup"><span data-stu-id="c38a3-168">**Maintain shipments**</span></span>
      - <span data-ttu-id="c38a3-169">**生産を管理します**</span><span class="sxs-lookup"><span data-stu-id="c38a3-169">**Maintain productions**</span></span>
      - <span data-ttu-id="c38a3-170">**かんばん作業ピッキング リストを管理します**</span><span class="sxs-lookup"><span data-stu-id="c38a3-170">**Maintain kanban job picking lists**</span></span>

1. <span data-ttu-id="c38a3-171">ウィンドウの上部で、ウェーブに追加する明細行を選択し、**ウェーブに追加** を選択します。</span><span class="sxs-lookup"><span data-stu-id="c38a3-171">In the upper part of the window, select the line to add to the wave, and then select **Add to wave**.</span></span> <span data-ttu-id="c38a3-172">明細行は **ウェーブ明細行** クイックタブに移動します。</span><span class="sxs-lookup"><span data-stu-id="c38a3-172">The line is moved to the **Wave lines** FastTab.</span></span>

    <span data-ttu-id="c38a3-173">各明細行を追加する際は、この手順を繰り返します。</span><span class="sxs-lookup"><span data-stu-id="c38a3-173">Repeat this step for each line to add.</span></span> <span data-ttu-id="c38a3-174">すべての明細行を追加するには、**すべて追加** を選択します。</span><span class="sxs-lookup"><span data-stu-id="c38a3-174">To add all lines, select **Add all**.</span></span>

    > [!TIP]
    > <span data-ttu-id="c38a3-175">出荷ウェーブについては、**ウェーブ フィルター コード** フィールドでカスタム フィルターを選択すると、特定のオーダーを素早く検索できます。</span><span class="sxs-lookup"><span data-stu-id="c38a3-175">For shipment waves, you can quickly find a specific order by selecting a custom filter in the **Wave filter code** field.</span></span> <span data-ttu-id="c38a3-176">ウェーブ フィルター コードには、**ウェーブ フィルター** フォームで作成された出荷のクエリ基準が含まれます。</span><span class="sxs-lookup"><span data-stu-id="c38a3-176">Wave filter codes contain query criteria for shipments, which are created in the **Wave filters** form.</span></span> <span data-ttu-id="c38a3-177">このフィールドは、生産ウェーブやかんばんウェーブでは使用できません。</span><span class="sxs-lookup"><span data-stu-id="c38a3-177">This field is not available for production waves or kanban waves.</span></span>
    > <span data-ttu-id="c38a3-178">**オン ウェーブ** 列の緑のチェック マークは、出荷がウェーブに追加されたことを示します。</span><span class="sxs-lookup"><span data-stu-id="c38a3-178">A green check mark in the **On wave** column indicates that the shipment has been added to the wave.</span></span>

### <a name="process-the-wave-to-create-the-picking-work"></a><span data-ttu-id="c38a3-179">ウェーブを処理して、ピッキング作業を作成する</span><span class="sxs-lookup"><span data-stu-id="c38a3-179">Process the wave to create the picking work</span></span>

<span data-ttu-id="c38a3-180">ウェーブが作成され必要な明細行がすべて含められると、対応するピッキング作業を作成できます。</span><span class="sxs-lookup"><span data-stu-id="c38a3-180">After a wave has been created and contains all of its required lines, you are ready to process it to create the corresponding picking work.</span></span>

#### <a name="automatically-process-a-wave"></a><span data-ttu-id="c38a3-181">自動でウェーブを処理する</span><span class="sxs-lookup"><span data-stu-id="c38a3-181">Automatically process a wave</span></span>

<span data-ttu-id="c38a3-182">自動的にウェーブを処理するには、自動処理オプションが必要な関連する [ウェーブ テンプレート](wave-templates.md) を設定します。</span><span class="sxs-lookup"><span data-stu-id="c38a3-182">To automatically process a wave, set up the relevant [Wave templates](wave-templates.md) with the automatic processing options required.</span></span>

#### <a name="manually-process-a-wave"></a><span data-ttu-id="c38a3-183">手動でウェーブを処理する</span><span class="sxs-lookup"><span data-stu-id="c38a3-183">Manually process a wave</span></span>

<span data-ttu-id="c38a3-184">**ウェーブの状態** が *作成済み* の場合にのみウェーブを処理できます。</span><span class="sxs-lookup"><span data-stu-id="c38a3-184">You can process a wave only when the **Wave status** is *Created*.</span></span> <span data-ttu-id="c38a3-185">ウェーブを処理すると、**ウェーブの状態** が *保留* に変更されます。</span><span class="sxs-lookup"><span data-stu-id="c38a3-185">After you process a wave, the **Wave status** will be changed to *Held*.</span></span>

<span data-ttu-id="c38a3-186">必要なすべてのコンテンツを含むウェーブを手動で処理するには、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="c38a3-186">To manually process a wave that has all of its required content, follow these steps:</span></span>

1. <span data-ttu-id="c38a3-187">処理するウェーブのタイプに応じて、次のいずれかを実行します。</span><span class="sxs-lookup"><span data-stu-id="c38a3-187">Depending on the type of wave to process, do one of the following:</span></span>

    - <span data-ttu-id="c38a3-188">**倉庫管理** \> **一般** \> **ウェーブ** \> **出荷ウェーブ** \> **すべてのウェーブ** の順に選択します。</span><span class="sxs-lookup"><span data-stu-id="c38a3-188">Select **Warehouse management** \> **Common** \> **Waves** \> **Shipment waves** \> **All waves**.</span></span> <span data-ttu-id="c38a3-189">アクション ウィンドウで、**ウェーブ** を選択します。</span><span class="sxs-lookup"><span data-stu-id="c38a3-189">On the Action Pane, select **Wave**.</span></span>
    - <span data-ttu-id="c38a3-190">**倉庫管理** \> **一般** \> **ウェーブ** \> **生産ウェーブ** \> **すべての生産ウェーブ** の順に選択します。</span><span class="sxs-lookup"><span data-stu-id="c38a3-190">Select **Warehouse management** \> **Common** \> **Waves** \> **Production waves** \> **All production waves**.</span></span> <span data-ttu-id="c38a3-191">アクション ウィンドウで、**生産ウェーブ** を選択します。</span><span class="sxs-lookup"><span data-stu-id="c38a3-191">On the Action Pane, select **Production wave**.</span></span>
    - <span data-ttu-id="c38a3-192">**倉庫管理** \> **一般** \> **ウェーブ** \> **かんばんウェーブ** \> **すべてのかんばんウェーブ** の順に選択します。</span><span class="sxs-lookup"><span data-stu-id="c38a3-192">Select **Warehouse management** \> **Common** \> **Waves** \> **Kanban waves** \> **All kanban waves**.</span></span> <span data-ttu-id="c38a3-193">アクション ウィンドウで、**ウェーブの作成** を選択します。</span><span class="sxs-lookup"><span data-stu-id="c38a3-193">On the Action Pane, select **Create wave**.</span></span>

1. <span data-ttu-id="c38a3-194">処理するウェーブを選択します。</span><span class="sxs-lookup"><span data-stu-id="c38a3-194">Select the wave to process.</span></span> <span data-ttu-id="c38a3-195">アクション ウィンドウで、**プロセス** を選択します。</span><span class="sxs-lookup"><span data-stu-id="c38a3-195">On the Action Pane, select **Process**.</span></span>

### <a name="release-the-wave-to-the-warehouse-to-start-picking-and-packing"></a><span data-ttu-id="c38a3-196">倉庫にウェーブをリリースして、ピッキングおよび梱包を開始する</span><span class="sxs-lookup"><span data-stu-id="c38a3-196">Release the wave to the warehouse to start picking and packing</span></span>

<span data-ttu-id="c38a3-197">リリースする前に、ウェーブを処理する必要があります。</span><span class="sxs-lookup"><span data-stu-id="c38a3-197">You must process a wave before you can release it.</span></span> <span data-ttu-id="c38a3-198">ウェーブをリリースすると、ピッキングの作業は倉庫でできるようになります。</span><span class="sxs-lookup"><span data-stu-id="c38a3-198">When you release the wave, the picking work is available in the warehouse.</span></span> <span data-ttu-id="c38a3-199">リリース後、ウェーブをキャンセルしたり、明細行を追加したりできますが、明細行を変更することはできません。</span><span class="sxs-lookup"><span data-stu-id="c38a3-199">You can cancel a wave after it is released, and add more lines, but you can't change the lines.</span></span>

#### <a name="automatically-release-a-wave"></a><span data-ttu-id="c38a3-200">自動でウェーブをリリースする</span><span class="sxs-lookup"><span data-stu-id="c38a3-200">Automatically release a wave</span></span>

<span data-ttu-id="c38a3-201">自動的にウェーブを処理するには、自動処理オプションが必要な関連する [ウェーブ テンプレート](wave-templates.md) を設定します。</span><span class="sxs-lookup"><span data-stu-id="c38a3-201">To automatically process a wave, set up the relevant [Wave templates](wave-templates.md) with the automatic processing options required.</span></span>

#### <a name="manually-release-a-wave"></a><span data-ttu-id="c38a3-202">手動でウェーブをリリースする</span><span class="sxs-lookup"><span data-stu-id="c38a3-202">Manually release a wave</span></span>

<span data-ttu-id="c38a3-203">ウェーブを手動でリリースするには、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="c38a3-203">To release a wave manually, follow these steps:</span></span>

1. <span data-ttu-id="c38a3-204">リリースするウェーブのタイプに応じて、次のいずれかを実行します。</span><span class="sxs-lookup"><span data-stu-id="c38a3-204">Depending on the type of wave to release, do one of the following:</span></span>

      - <span data-ttu-id="c38a3-205">**倉庫管理** \> **一般** \> **ウェーブ** \> **出荷ウェーブ** \> **すべてのウェーブ** の順に選択します。</span><span class="sxs-lookup"><span data-stu-id="c38a3-205">Select **Warehouse management** \> **Common** \> **Waves** \> **Shipment waves** \> **All waves**.</span></span> <span data-ttu-id="c38a3-206">アクション ウィンドウで、**ウェーブ** を選択します。</span><span class="sxs-lookup"><span data-stu-id="c38a3-206">On the Action Pane, select **Wave**.</span></span>
      - <span data-ttu-id="c38a3-207">**倉庫管理** \> **一般** \> **ウェーブ** \> **生産ウェーブ** \> **すべての生産ウェーブ** の順に選択します。</span><span class="sxs-lookup"><span data-stu-id="c38a3-207">Select **Warehouse management** \> **Common** \> **Waves** \> **Production waves** \> **All production waves**.</span></span> <span data-ttu-id="c38a3-208">アクション ウィンドウで、**生産ウェーブ** を選択します。</span><span class="sxs-lookup"><span data-stu-id="c38a3-208">On the Action Pane, select **Production wave**.</span></span>
      - <span data-ttu-id="c38a3-209">**倉庫管理** \> **一般** \> **ウェーブ** \> **かんばんウェーブ** \> **すべてのかんばんウェーブ** の順に選択します。</span><span class="sxs-lookup"><span data-stu-id="c38a3-209">Select **Warehouse management** \> **Common** \> **Waves** \> **Kanban waves** \> **All kanban waves**.</span></span> <span data-ttu-id="c38a3-210">アクション ウィンドウで、**ウェーブの作成** を選択します。</span><span class="sxs-lookup"><span data-stu-id="c38a3-210">On the Action Pane, select **Create wave**.</span></span>

1. <span data-ttu-id="c38a3-211">リリースするウェーブを選択します。</span><span class="sxs-lookup"><span data-stu-id="c38a3-211">Select the wave to release.</span></span> <span data-ttu-id="c38a3-212">アクション ウィンドウで、**ウェーブのリリース** を選択します。</span><span class="sxs-lookup"><span data-stu-id="c38a3-212">On the Action Pane, select **Release wave**.</span></span>

## <a name="containerize-a-wave"></a><span data-ttu-id="c38a3-213">ウェーブのコンテナー詰め</span><span class="sxs-lookup"><span data-stu-id="c38a3-213">Containerize a wave</span></span>

<span data-ttu-id="c38a3-214">自動化されたコンテナー詰めは、ウェーブが処理される際に、出荷のためのコンテナーとピッキング作業を作成します。</span><span class="sxs-lookup"><span data-stu-id="c38a3-214">Automated containerization creates containers and the picking work for shipments when a wave is processed.</span></span> <span data-ttu-id="c38a3-215">設定方法の詳細については、[コンテナー詰め](wave-containerization.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="c38a3-215">For details about how to set it up, see [Containerization](wave-containerization.md).</span></span>

## <a name="work-with-the-scheduled-work-creation"></a><span data-ttu-id="c38a3-216">スケジュールされた作業の作成に関する作業</span><span class="sxs-lookup"><span data-stu-id="c38a3-216">Work with the scheduled work creation</span></span>

<span data-ttu-id="c38a3-217">*作業作成のスケジュール* 機能を有効にすると、ウェーブ処理は計画作業を作成し、最終的には新しい作業作成プロセスで使用されます。</span><span class="sxs-lookup"><span data-stu-id="c38a3-217">When the *Schedule work creation* functionality is enabled, wave processing will create planned work, which will eventually be used by the new work creation process.</span></span> <span data-ttu-id="c38a3-218">作業の作成中は、*組織全体の作業のブロック* 機能を使用して作業がブロックされます。</span><span class="sxs-lookup"><span data-stu-id="c38a3-218">During work creation, the work will be blocked using the *Organization-wide work blocking* feature.</span></span> <span data-ttu-id="c38a3-219">詳細については、[サイクル中に作業の作成をスケジュールする](configure-wave-schedule-work-creation.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="c38a3-219">For more information, see [Schedule work creation during wave](configure-wave-schedule-work-creation.md).</span></span>

<span data-ttu-id="c38a3-220">次のフローチャートは、ウェーブ処理中に計画作業がどのように作成されるかを示しています。</span><span class="sxs-lookup"><span data-stu-id="c38a3-220">The following flowchart shows how planned work is created during wave processing.</span></span>

![作業作成のスケジュール](media/schedule-work-creation-process.png)

### <a name="planned-work"></a><span data-ttu-id="c38a3-222">計画作業</span><span class="sxs-lookup"><span data-stu-id="c38a3-222">Planned work</span></span>

<span data-ttu-id="c38a3-223">**計画作業の詳細** ページ (**倉庫管理 \> 作業 \> 計画作業の詳細**) には、ウェーブ処理中に最初に作成された計画作業に関する情報が表示されます。</span><span class="sxs-lookup"><span data-stu-id="c38a3-223">The **Planned work details** page (**Warehouse management \> Work \> Planned work details**) shows information about the planned work, which is initially created during wave processing.</span></span> <span data-ttu-id="c38a3-224">以下の **プロセス状態** 値を使用できます:</span><span class="sxs-lookup"><span data-stu-id="c38a3-224">The following **Process status** values are available:</span></span>

- <span data-ttu-id="c38a3-225">**キューに設定** - 計画作業は、作業の作成に使用されるまで待機しています。</span><span class="sxs-lookup"><span data-stu-id="c38a3-225">**Queued** - The planned work is waiting to be used to create work.</span></span>
- <span data-ttu-id="c38a3-226">**完了** - 計画作業が作業の作成に使用されました。</span><span class="sxs-lookup"><span data-stu-id="c38a3-226">**Completed** - The planned work has been used to create work.</span></span>
- <span data-ttu-id="c38a3-227">**失敗** – ウェーブ処理が失敗しました。</span><span class="sxs-lookup"><span data-stu-id="c38a3-227">**Failed** – The wave processing has failed.</span></span> <span data-ttu-id="c38a3-228">計画作業は、関連する実際の作業の有無にかかわらず、**失敗** した状態になることがあります。</span><span class="sxs-lookup"><span data-stu-id="c38a3-228">Note that the planned work can be in a **Failed** state with or without related actual work.</span></span> <span data-ttu-id="c38a3-229">実際の作業作成プロセスが失敗すると、実際の作業は *キャンセル済* 状態のままになります。</span><span class="sxs-lookup"><span data-stu-id="c38a3-229">When the actual work creation process fails, the actual work remains in status *Cancelled*.</span></span>

### <a name="batch-job-for-the-work-creation-process"></a><span data-ttu-id="c38a3-230">作業作成プロセスのバッチ ジョブ</span><span class="sxs-lookup"><span data-stu-id="c38a3-230">Batch job for the work creation process</span></span>

<span data-ttu-id="c38a3-231">ウェーブを処理するバッチ ジョブを表示するには、**すべてのウェーブ** ページのアクション ペインで **バッチ ジョブ** を選択 します。</span><span class="sxs-lookup"><span data-stu-id="c38a3-231">To view the batch jobs for processing waves, select **Batch jobs** on the Action Pane on the **All waves** page.</span></span>

<span data-ttu-id="c38a3-232">ここから、各バッチ ジョブ ID のすべてのバッチ タスクの詳細を表示できます。</span><span class="sxs-lookup"><span data-stu-id="c38a3-232">From here, you can view all the batch task details for each of the batch job IDs.</span></span>

## <a name="cancel-a-wave"></a><span data-ttu-id="c38a3-233">ウェーブのキャンセル</span><span class="sxs-lookup"><span data-stu-id="c38a3-233">Cancel a wave</span></span>

<span data-ttu-id="c38a3-234">必要に応じて、処理されたウェーブをキャンセルできます。</span><span class="sxs-lookup"><span data-stu-id="c38a3-234">If needed, you can cancel a wave that has been processed.</span></span> <span data-ttu-id="c38a3-235">ウェーブと作成されたピッキングをキャンセルするには、次の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="c38a3-235">To cancel a wave, and the picking work that was created, follow these steps:</span></span>

1. <span data-ttu-id="c38a3-236">キャンセルするウェーブのタイプに応じて、次のいずれかを実行します。</span><span class="sxs-lookup"><span data-stu-id="c38a3-236">Depending on the type of wave to cancel, do one of the following:</span></span>

      - <span data-ttu-id="c38a3-237">**倉庫管理** \> **一般** \> **ウェーブ** \> **出荷ウェーブ** \> **すべてのウェーブ** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="c38a3-237">Go to **Warehouse management** \> **Common** \> **Waves** \> **Shipment waves** \> **All waves**.</span></span>
      - <span data-ttu-id="c38a3-238">**倉庫管理** \> **一般** \> **ウェーブ** \> **生産ウェーブ** \> **すべての生産ウェーブ** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="c38a3-238">Go to **Warehouse management** \> **Common** \> **Waves** \> **Production waves** \> **All production waves**.</span></span>
      - <span data-ttu-id="c38a3-239">**倉庫管理** \> **一般** \> **ウェーブ** \> **かんばんウェーブ** \> **すべてのかんばんウェーブ** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="c38a3-239">Go to **Warehouse management** \> **Common** \> **Waves** \> **Kanban waves** \> **All kanban waves**.</span></span>

1. <span data-ttu-id="c38a3-240">キャンセルするウェーブを選択します。</span><span class="sxs-lookup"><span data-stu-id="c38a3-240">Select the wave to cancel.</span></span> <span data-ttu-id="c38a3-241">アクション ペインの、**作業** タブで、**キャンセル** を選択します。</span><span class="sxs-lookup"><span data-stu-id="c38a3-241">On the Action Pane, on the **Work** tab, select **Cancel**.</span></span>

## <a name="review-wave-batch-job-details"></a><span data-ttu-id="c38a3-242">バッチ ジョブの詳細の確認</span><span class="sxs-lookup"><span data-stu-id="c38a3-242">Review wave batch job details</span></span>

<span data-ttu-id="c38a3-243">**バッチ ジョブの詳細** ページでは、バッチ ジョブと任意のウェーブに関連付けられている関連タスクを検査します。</span><span class="sxs-lookup"><span data-stu-id="c38a3-243">Use the **Wave batch job details** page to inspect the batch jobs and related tasks associated with any wave.</span></span> <span data-ttu-id="c38a3-244">これは特に、失敗したウェーブに対するトラブルシューティングを行う場合に役立ちます。</span><span class="sxs-lookup"><span data-stu-id="c38a3-244">This is especially useful for troubleshooting a wave that has failed.</span></span> <span data-ttu-id="c38a3-245">この機能がない場合、通常は管理者だけがバッチ ジョブの詳細にアクセスできます。</span><span class="sxs-lookup"><span data-stu-id="c38a3-245">Without this feature, only administrators will typically have access to batch job details.</span></span> <span data-ttu-id="c38a3-246">**ウェーブ バッチ ジョブの詳細** ページは、管理者以外のユーザーが使用することもでき、バッチ ジョブおよび関連タスクの読み取り専用ビューを表示します。</span><span class="sxs-lookup"><span data-stu-id="c38a3-246">The **Wave batch job details** page can be made available to non-admin users and provides a read-only view of batch jobs and related tasks.</span></span>

### <a name="enable-the-wave-batch-job-details-page"></a><span data-ttu-id="c38a3-247">[ウェーブ バッチ ジョブの詳細] ページの有効化</span><span class="sxs-lookup"><span data-stu-id="c38a3-247">Enable the Wave batch job details page</span></span>

<span data-ttu-id="c38a3-248">システムに **ウェーブ バッチ ジョブの詳細** ページがない場合は、[機能管理](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) に移動して、*ウェーブ バッチ ジョブの詳細* 機能をオンにします。</span><span class="sxs-lookup"><span data-stu-id="c38a3-248">If your system doesn't already include the **Wave batch job details** page, go to [Feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) and turn on the *Wave batch job details* feature.</span></span>

### <a name="use-the-wave-batch-job-details-page"></a><span data-ttu-id="c38a3-249">[ウェーブ バッチ ジョブの詳細] ページを使用する</span><span class="sxs-lookup"><span data-stu-id="c38a3-249">Use the Wave batch job details page</span></span>

<span data-ttu-id="c38a3-250">**ウェーブ バッチ ジョブの詳細** ページでは、バッチ ジョブとバッチ ジョブ タスクが混合しており、単一のバッチ ジョブとバッチ タスク リスト間を移動せずに、すべての手順を調査できます。</span><span class="sxs-lookup"><span data-stu-id="c38a3-250">The **Wave batch job details** page combines batch jobs and batch job tasks, which lets you investigate all the wave steps without needing to navigate back and forth between a single batch job and the batch tasks list.</span></span> <span data-ttu-id="c38a3-251">また、バッチ ログへアクセスすることもでき、必要なアクセス許可がある場合は **バッチ ジョブ** ページへリンクすることもできます。</span><span class="sxs-lookup"><span data-stu-id="c38a3-251">The page also provides access to the batch log and, if you have the required permissions, provides a link to the **Batch jobs** page.</span></span>

<span data-ttu-id="c38a3-252">このページを開くには、複数あるウェーブ ページからウェーブを選択し、アクション ウィンドウから **ウェーブ バッチ ジョブの詳細** を選択します。</span><span class="sxs-lookup"><span data-stu-id="c38a3-252">To open this page, select a wave on any of several different wave pages and then select **Wave batch job details** from the Action Pane.</span></span>

## <a name="review-load-validation-and-error-messages"></a><span data-ttu-id="c38a3-253">負荷の検証とエラー メッセージの確認</span><span class="sxs-lookup"><span data-stu-id="c38a3-253">Review load validation and error messages</span></span>

<span data-ttu-id="c38a3-254">ウェーブの処理中は、システムがウェーブの負荷行ごとに状態を検証し表示します。</span><span class="sxs-lookup"><span data-stu-id="c38a3-254">During wave processing, the system validates and displays the status for each load line in the wave.</span></span> <span data-ttu-id="c38a3-255">警告が発生しない場合は、次のウェーブの手順に進みます。</span><span class="sxs-lookup"><span data-stu-id="c38a3-255">If no warnings occur, it continues to the next wave step.</span></span> <span data-ttu-id="c38a3-256">警告が発生した場合は、全体のウェーブの検証が完了した後に次のエラーが表示されます。</span><span class="sxs-lookup"><span data-stu-id="c38a3-256">If warnings do occur, it instead shows the following error after it has finished validating the entire wave:</span></span>

> <span data-ttu-id="c38a3-257">ウェーブで無効な負荷行が見つかりました。</span><span class="sxs-lookup"><span data-stu-id="c38a3-257">Found invalid load lines in wave.</span></span> <span data-ttu-id="c38a3-258">無効な負荷行を削除してください。</span><span class="sxs-lookup"><span data-stu-id="c38a3-258">Please remove the invalid load lines.</span></span>

<span data-ttu-id="c38a3-259">その後、ウェーブの各負荷行に対する最終状態を確認し、再度実行する前にすべての警告を修正することができます。</span><span class="sxs-lookup"><span data-stu-id="c38a3-259">You are then able to review the final status of each load line in the wave and correct all warnings before trying again.</span></span> <span data-ttu-id="c38a3-260">こうすることで、すべての警告に一度に対処してからウェーブを再処理することができます。</span><span class="sxs-lookup"><span data-stu-id="c38a3-260">This lets you address all the warnings at once before reprocessing the wave.</span></span> <span data-ttu-id="c38a3-261">(以前のリリースでは、最初の警告の後にシステムがウェーブ処理を停止していたため、警告には 1 件ずつ対処していました。)</span><span class="sxs-lookup"><span data-stu-id="c38a3-261">(In previous releases, the system stopped processing the wave after the first warning, so you could only fix warnings one at a time.)</span></span>

<span data-ttu-id="c38a3-262">システムがウェーブ処理の状態に関するメッセージを表示する方法は、**倉庫管理パラメーター** ページで **ウェーブ処理履歴ログを作成する** オプションをどう設定したかによって異なります。</span><span class="sxs-lookup"><span data-stu-id="c38a3-262">The way the system displays your wave processing status messages depends on how you have set the **Create wave processing history log** option on the **Warehouse management parameters** page.</span></span>

- <span data-ttu-id="c38a3-263">**ウェーブ処理履歴ログを作成する** が *いいえ* に設定されている場合は、負荷行の状態に関するメッセージは **Infolog** に表示されます。</span><span class="sxs-lookup"><span data-stu-id="c38a3-263">When **Create wave processing history log** is set to *No*, the load line status messages are shown in the **Infolog**.</span></span>
- <span data-ttu-id="c38a3-264">**ウェーブ処理履歴ログを作成する** が *はい* に設定されている場合は、負荷行の状態に関するメッセージは **ウェーブ処理履歴ログ** ページに表示されます。</span><span class="sxs-lookup"><span data-stu-id="c38a3-264">When **Create wave processing history log** is set to *Yes*, the load line status messages are shown on the **Wave processing history log** page.</span></span> <span data-ttu-id="c38a3-265">ログを表示するには、**倉庫管理 \> 出荷ウェーブ \> ウェーブ処理履歴ログ** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="c38a3-265">To view the log, go to **Warehouse management \> Outbound waves \> Wave processing history log**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="c38a3-266">追加リソース</span><span class="sxs-lookup"><span data-stu-id="c38a3-266">Additional resources</span></span>

- [<span data-ttu-id="c38a3-267">ウェーブ処理のコンフィギュレーションの例</span><span class="sxs-lookup"><span data-stu-id="c38a3-267">Configure wave processing example</span></span>](tasks/configure-wave-processing.md)
- [<span data-ttu-id="c38a3-268">ウェーブ テンプレート</span><span class="sxs-lookup"><span data-stu-id="c38a3-268">Wave templates</span></span>](wave-templates.md)
- [<span data-ttu-id="c38a3-269">コンテナー化</span><span class="sxs-lookup"><span data-stu-id="c38a3-269">Containerization</span></span>](wave-containerization.md)