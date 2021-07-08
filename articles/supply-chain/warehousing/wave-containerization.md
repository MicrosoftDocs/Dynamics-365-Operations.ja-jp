---
title: コンテナー化
description: このトピックでは、積荷のコンテナー詰めを自動化する方法について説明します。 自動化されたコンテナー詰めは、ウェーブが処理される際に、出荷のためのコンテナーとピッキング作業を作成します。
author: Mirzaab
ms.date: 03/08/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WHSWaveTemplateTable, InventLocationIdLookup, WHSContainerType, WHSContainerGroup, WHSContainerizationTable, WHSContainerizationBreak, WHSCreateContainerBreak, WHSContainerStructure, WHSContainerTable, WHSContainerizatonHistory, WHSContainerPackingPolicyChange, WHSManifestShipmentContainers, WHSAllowedContainerTypeGroup, WHSPostMethod, WHSContainerCreateDialog, WHSContainerCloseDiag, WHSContainer
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2021-03-08
ms.dyn365.ops.version: Release 10.0.18
ms.openlocfilehash: 88e38989e3d3e46d0c43779659bc6ea2e29f08e2
ms.sourcegitcommit: 8e846b52763f90d2232ec7d427839f4722570bce
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/22/2021
ms.locfileid: "6292740"
---
# <a name="containerization"></a><span data-ttu-id="7ad65-104">コンテナー化</span><span class="sxs-lookup"><span data-stu-id="7ad65-104">Containerization</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="7ad65-105">このトピックでは、積荷のコンテナー詰めを自動化する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="7ad65-105">This topic describes how to automate the containerization of loads.</span></span> <span data-ttu-id="7ad65-106">自動化されたコンテナー詰めは、ウェーブが処理される際に、出荷のためのコンテナーとピッキング作業を作成します。</span><span class="sxs-lookup"><span data-stu-id="7ad65-106">Automated containerization creates containers and the picking work for shipments when a wave is processed.</span></span>

<span data-ttu-id="7ad65-107">コンテナー詰めを設定にするには、次を作成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="7ad65-107">To set up containerization, you must create the following:</span></span>

- <span data-ttu-id="7ad65-108">**コンテナー タイプ** ─ コンテナーの物理的特性を定義します。</span><span class="sxs-lookup"><span data-stu-id="7ad65-108">**Container type** ─ Define the physical characteristics of the containers.</span></span> <span data-ttu-id="7ad65-109">コンテナーのタイプを使用して、在庫置場やパレットなど、梱包の特定のタイプとサイズに在庫品目を梱包します。</span><span class="sxs-lookup"><span data-stu-id="7ad65-109">Use container types to pack inventory items into a specific type and size of packaging, such as bins or pallets.</span></span>
- <span data-ttu-id="7ad65-110">**コンテナー グループ** ─ 似たタイプのコンテナー タイプのグループを作成します。</span><span class="sxs-lookup"><span data-stu-id="7ad65-110">**Container groups** ─ Create groups of container types that are similar.</span></span> <span data-ttu-id="7ad65-111">たとえば、コンテナーのグループに類似したサイズ分析コードを持つコンテナーのタイプを含めることができます。</span><span class="sxs-lookup"><span data-stu-id="7ad65-111">For example, a container group can include container types that have similar size dimensions.</span></span> <span data-ttu-id="7ad65-112">コンテナーのグループは、コンテナーが梱包された順番、および各コンテナーの保管できる量に対する使用率を指定します。</span><span class="sxs-lookup"><span data-stu-id="7ad65-112">A container group specifies the sequence in which containers are packed, and the fill percentage of each container.</span></span>
- <span data-ttu-id="7ad65-113">**コンテナー ビルド テンプレート** ─ コンテナー詰めのルールを定義するテンプレートを作成します。</span><span class="sxs-lookup"><span data-stu-id="7ad65-113">**Container build template** ─ Create templates that define rules for containerization.</span></span> <span data-ttu-id="7ad65-114">たとえば、在庫およびそのほかの梱包計画を混合するルール。</span><span class="sxs-lookup"><span data-stu-id="7ad65-114">For example, rules for mixing inventory and other packing strategies.</span></span>
- <span data-ttu-id="7ad65-115">**ウェーブ テンプレート** – コンテナー詰めのピッキングの作業を作成する 1 つ以上のウェーブ テンプレートを設定します。</span><span class="sxs-lookup"><span data-stu-id="7ad65-115">**Wave templates** – Set up one or more wave templates to create the picking work for containerization.</span></span>

## <a name="create-wave-templates-for-containerization"></a><span data-ttu-id="7ad65-116">コンテナー詰めのウェーブ テンプレートを作成する</span><span class="sxs-lookup"><span data-stu-id="7ad65-116">Create wave templates for containerization</span></span>

<span data-ttu-id="7ad65-117">コンテナー詰めの 1 つ以上の出荷ウェーブ テンプレートを設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="7ad65-117">You must set up one or more shipping wave templates for containerization.</span></span> <span data-ttu-id="7ad65-118">ウェーブ テンプレートには次を決定する基準が含まれます。</span><span class="sxs-lookup"><span data-stu-id="7ad65-118">Wave templates include criteria that determine the following:</span></span>

- <span data-ttu-id="7ad65-119">ウェーブを処理する方法。</span><span class="sxs-lookup"><span data-stu-id="7ad65-119">How to process waves.</span></span> <span data-ttu-id="7ad65-120">これは手動または自動にすることができます。</span><span class="sxs-lookup"><span data-stu-id="7ad65-120">This can be either manual or automatic.</span></span>
- <span data-ttu-id="7ad65-121">ピッキングの作業を作成する方法。</span><span class="sxs-lookup"><span data-stu-id="7ad65-121">How to create picking work.</span></span> <span data-ttu-id="7ad65-122">これはウェーブ メソッドによって決定されます。</span><span class="sxs-lookup"><span data-stu-id="7ad65-122">This is determined by the wave methods.</span></span> <span data-ttu-id="7ad65-123">ウェーブ テンプレートには、**コンテナー詰め** のメソッドを含める必要があります。</span><span class="sxs-lookup"><span data-stu-id="7ad65-123">The wave template must include the **containerization** method.</span></span>
- <span data-ttu-id="7ad65-124">ウェーブに品目や配賦ラインを一致させる方法。</span><span class="sxs-lookup"><span data-stu-id="7ad65-124">How to match items or allocation lines with a wave.</span></span>

<span data-ttu-id="7ad65-125">テンプレートの詳細については、[ウェーブ テンプレート](wave-templates.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="7ad65-125">For more information, see [Wave templates](wave-templates.md).</span></span>

## <a name="create-container-types"></a><span data-ttu-id="7ad65-126">コンテナー タイプの作成</span><span class="sxs-lookup"><span data-stu-id="7ad65-126">Create container types</span></span>

<span data-ttu-id="7ad65-127">物理的なサイズの分析コードと重さの能力の最大値など、コンテナーの説明を作成するためにコンテナー タイプを使用します。</span><span class="sxs-lookup"><span data-stu-id="7ad65-127">Use container types to create descriptions of containers, including maximum values for physical size dimensions and weight capacity.</span></span> <span data-ttu-id="7ad65-128">コンテナー詰めされたウェーブが処理されると、コンテナーはコンテナーのタイプの情報に基づいて作成されます。</span><span class="sxs-lookup"><span data-stu-id="7ad65-128">When a containerized wave is processed, the containers are created based on the container type information.</span></span>

<span data-ttu-id="7ad65-129">コンテナー タイプを設定するには、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="7ad65-129">To set up a container type, follow these steps:</span></span>

1. <span data-ttu-id="7ad65-130">**倉庫管理** \> **設定** \> **コンテナー** \> **コンテナー タイプ** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="7ad65-130">Go to **Warehouse management** \> **Setup** \> **Containers** \> **Container type**.</span></span>
1. <span data-ttu-id="7ad65-131">**新規作成** を選択して、新しいコンテナー タイプを作成します。</span><span class="sxs-lookup"><span data-stu-id="7ad65-131">Select **New** to create a new container type.</span></span>
1. <span data-ttu-id="7ad65-132">コンテナー タイプの固有の識別子 (ID) と説明を入力します。</span><span class="sxs-lookup"><span data-stu-id="7ad65-132">Enter a unique identifier (ID) and description for the container type.</span></span>
1. <span data-ttu-id="7ad65-133">**風袋重量** フィールドで、コンテナーの実際のまたは見積の重量を入力します。</span><span class="sxs-lookup"><span data-stu-id="7ad65-133">In the **Tare weight** field, enter the actual or estimated weight of the container.</span></span>
1. <span data-ttu-id="7ad65-134">**最大重量** フィールドで、コンテナーが保持できる最大重量を入力します。</span><span class="sxs-lookup"><span data-stu-id="7ad65-134">In the **Maximum weight** field, enter the maximum weight that the container can hold.</span></span>
1. <span data-ttu-id="7ad65-135">**コンテナ詰め最大容量**、**コンテナ詰め最大の長さ**、**コンテナ詰め最大幅**、**コンテナ詰め最大の高さ** フィールドで、コンテナーの物理分析コードを指定します。</span><span class="sxs-lookup"><span data-stu-id="7ad65-135">In the **Containerization maximum volume**, **Containerization maximum length**, **Containerization maximum width**, and **Containerization maximum height** fields, specify the physical dimensions of the container.</span></span>

    > [!NOTE]
    > <span data-ttu-id="7ad65-136">長さと幅の値は、交換できます。</span><span class="sxs-lookup"><span data-stu-id="7ad65-136">The values for length and width are interchangeable.</span></span> <span data-ttu-id="7ad65-137">これは、必要に応じて、品目を水平またはX 軸で回転できます。</span><span class="sxs-lookup"><span data-stu-id="7ad65-137">This means that you can rotate items laterally, or on the x-axis, if needed.</span></span> <span data-ttu-id="7ad65-138">たとえば、長さ 2 フィート、幅 1 フィートの場合、長さ 1 フィート、幅 2 フィートに変更できます。</span><span class="sxs-lookup"><span data-stu-id="7ad65-138">For example, if the length is 2 feet, and the width is 1 foot, you can change the length to 1 foot and the width to 2 feet.</span></span> <span data-ttu-id="7ad65-139">これは、高さの寸法には適用されません。</span><span class="sxs-lookup"><span data-stu-id="7ad65-139">Note that this does not apply to the height dimension.</span></span> <span data-ttu-id="7ad65-140">高さの値を変更して、品目を縦に回転することはできません。</span><span class="sxs-lookup"><span data-stu-id="7ad65-140">You cannot change the height value to rotate an item vertically.</span></span>

1. <span data-ttu-id="7ad65-141">属性のフィールドのコンテナーのカスタム属性の値を選択します。</span><span class="sxs-lookup"><span data-stu-id="7ad65-141">Select custom attribute values for the container in the fields for attributes.</span></span> <span data-ttu-id="7ad65-142">属性は、品目のフィルター処理または並べ替えに使用するカスタム値です。その値は、それ以外には使用できません。</span><span class="sxs-lookup"><span data-stu-id="7ad65-142">Attributes are custom values that are used to filter or sort items based on a value that is otherwise not available.</span></span> <span data-ttu-id="7ad65-143">たとえば、特定の顧客の品目を梱包する場合は、顧客名の属性を作成できます。</span><span class="sxs-lookup"><span data-stu-id="7ad65-143">For example, if you want to pack items for a particular customer, you can create an attribute for the customer name.</span></span> <span data-ttu-id="7ad65-144">**コンテナー属性** ページで属性を作成します。</span><span class="sxs-lookup"><span data-stu-id="7ad65-144">You create attributes on the **Container attributes** page.</span></span>

## <a name="create-container-groups"></a><span data-ttu-id="7ad65-145">コンテナー グループの作成</span><span class="sxs-lookup"><span data-stu-id="7ad65-145">Create container groups</span></span>

<span data-ttu-id="7ad65-146">コンテナーのタイプの論理グループを設定できます。</span><span class="sxs-lookup"><span data-stu-id="7ad65-146">You can set up logical groups of container types.</span></span> <span data-ttu-id="7ad65-147">グループごとに、コンテナーを梱包する順番と、コンテナーに詰める割合を指定できます。</span><span class="sxs-lookup"><span data-stu-id="7ad65-147">For each group, you can specify the sequence in which to pack the containers and the percentage of the containers to fill.</span></span> <span data-ttu-id="7ad65-148">品目のサイズ分析コードは、コンテナーに適合するどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="7ad65-148">The size dimensions of the item determine whether it will fit in a container.</span></span> <span data-ttu-id="7ad65-149">品目のサイズ分析コードに最も近いコンテナーが使用されます。</span><span class="sxs-lookup"><span data-stu-id="7ad65-149">The container that is closest to the size dimensions of the item is used.</span></span> <span data-ttu-id="7ad65-150">グループにコンテナーが複数ある場合は、最大のコンテナーが 1 番目、最小のコンテナーが最後になるようにサイズで順番を並べるようにお勧めします。</span><span class="sxs-lookup"><span data-stu-id="7ad65-150">If you have multiple container types in a group, we recommend that you arrange the sequence by size, so that the largest container is first, number 1 in the sequence, and the smallest container is last.</span></span>

<span data-ttu-id="7ad65-151">コンテナー グループを設定するには、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="7ad65-151">To set up a container group, follow these steps:</span></span>

1. <span data-ttu-id="7ad65-152">**倉庫管理** \> **設定** \> **コンテナー** \> **コンテナー グループ** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="7ad65-152">Go to **Warehouse management** \> **Setup** \> **Containers** \> **Container groups**.</span></span>
1. <span data-ttu-id="7ad65-153">**新規** を選択して、コンテナー グループを作成します。</span><span class="sxs-lookup"><span data-stu-id="7ad65-153">Select **New** to create a container group.</span></span>
1. <span data-ttu-id="7ad65-154">コンテナー グループの固有 ID と説明を入力します。</span><span class="sxs-lookup"><span data-stu-id="7ad65-154">Enter a unique ID and description for the container group.</span></span>
1. <span data-ttu-id="7ad65-155">**詳細** クイックタブで、**新規** をクリックして、グループへコンテナー タイプを追加します。</span><span class="sxs-lookup"><span data-stu-id="7ad65-155">On the **Details** FastTab, select **New** to add a container type to the group.</span></span>
1. <span data-ttu-id="7ad65-156">**コンテナー タイプ** フィールドで、コンテナー タイプを選択します。</span><span class="sxs-lookup"><span data-stu-id="7ad65-156">In the **Container type** field, select a container type.</span></span>
1. <span data-ttu-id="7ad65-157">**上へ移動** または **下へ移動** を選択して、コンテナー タイプを梱包する順序を指定します。</span><span class="sxs-lookup"><span data-stu-id="7ad65-157">Select **Move up** or **Move down** to specify the sequence in which the container types are packed.</span></span>

## <a name="create-container-build-templates"></a><span data-ttu-id="7ad65-158">コンテナー構築テンプレートの作成</span><span class="sxs-lookup"><span data-stu-id="7ad65-158">Create container build templates</span></span>

<span data-ttu-id="7ad65-159">在庫の混合ルールおよび他の梱包計画など、コンテナー詰めプロセスのルールを設定できます。</span><span class="sxs-lookup"><span data-stu-id="7ad65-159">You can set up rules for the containerization process, such as inventory mixing rules and other packing strategies.</span></span> <span data-ttu-id="7ad65-160">たとえば、作業者が同じコンテナーで異なる顧客の販売注文を表す配賦ラインを梱包できないようにルールを設定できます。</span><span class="sxs-lookup"><span data-stu-id="7ad65-160">For example, you can set up a rule so that workers cannot pack allocation lines that represent sales orders from different customers in the same container.</span></span>

<span data-ttu-id="7ad65-161">コンテナー構築テンプレートを設定するには、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="7ad65-161">To set up a container build template, follow these steps.</span></span>

1. <span data-ttu-id="7ad65-162">**倉庫管理** \> **設定** \> **コンテナー** \> **コンテナー構築テンプレート** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="7ad65-162">Go to **Warehouse management** \> **Setup** \> **Containers** \> **Container build template**.</span></span>
1. <span data-ttu-id="7ad65-163">新しいコンテナー構築テンプレートを作成します。</span><span class="sxs-lookup"><span data-stu-id="7ad65-163">Create a new container build template.</span></span>
1. <span data-ttu-id="7ad65-164">**コンテナ詰め名** および **シーケンス番号** フィールドで、コンテナー詰めのテンプレートの名前と配賦ラインに一致する順番を入力します。</span><span class="sxs-lookup"><span data-stu-id="7ad65-164">In the **Containerization name** and **Sequence number** fields, enter the name of the containerization template and the order that is matched to allocation lines.</span></span>

    > [!NOTE]
    > <span data-ttu-id="7ad65-165">システムは、配賦ラインがクエリ基準を満たす最初のテンプレートを適用します。</span><span class="sxs-lookup"><span data-stu-id="7ad65-165">The system will apply the first template that the allocation line meets the query criteria for.</span></span> <span data-ttu-id="7ad65-166">つまり、リストの先頭に最も限定的な基準があるテンプレートを置きます。</span><span class="sxs-lookup"><span data-stu-id="7ad65-166">Therefore, put the template with the most specific criteria at the top of the list.</span></span> <span data-ttu-id="7ad65-167">基準が広くなれば、配賦ラインが条件を満たす可能性が高くなります。</span><span class="sxs-lookup"><span data-stu-id="7ad65-167">The broader the criteria, the more likely that an allocation line will meet the criteria.</span></span> <span data-ttu-id="7ad65-168">これにより、ラインが間違ったコンテナーに割り当てられる可能性が生じます。</span><span class="sxs-lookup"><span data-stu-id="7ad65-168">This could lead to lines being assigned to the wrong container.</span></span> <span data-ttu-id="7ad65-169">必要に応じて **上へ移動** または **下へ移動** を選択して、テンプレートの順序を変更できます。</span><span class="sxs-lookup"><span data-stu-id="7ad65-169">If needed, you can select **Move up** or **Move down** to change the sequence of templates.</span></span>

1. <span data-ttu-id="7ad65-170">**コンテナー グループ ID** フィールドで、コンテナーの作成元のコンテナーのグループを選択します。</span><span class="sxs-lookup"><span data-stu-id="7ad65-170">In the **Container group ID** field, select the container group from which to create containers.</span></span>
1. <span data-ttu-id="7ad65-171">**基準クエリ タイプ** フィールドで、梱包内容や、フィルターがクエリする基準を決定するクエリ タイプを選択します。</span><span class="sxs-lookup"><span data-stu-id="7ad65-171">In the **Base query types** field, select the query type that will determine what to pack and what to base the filter query on.</span></span> <span data-ttu-id="7ad65-172">次のオプションを使用できます。</span><span class="sxs-lookup"><span data-stu-id="7ad65-172">The following options are available:</span></span>

      - <span data-ttu-id="7ad65-173">**販売配賦ライン** ─ 販売注文に対して作成された配賦ラインを梱包します。</span><span class="sxs-lookup"><span data-stu-id="7ad65-173">**Sales allocation line** ─ Pack allocation lines that are created for sales orders.</span></span>
      - <span data-ttu-id="7ad65-174">**配賦ラインの転送** ─ 販売注文に対して作成された配賦ラインを転送します。</span><span class="sxs-lookup"><span data-stu-id="7ad65-174">**Transfer allocation line** ─ Pack allocation lines that are created for transfer orders.</span></span>
      - <span data-ttu-id="7ad65-175">**コンテナー** ─ コンテナー詰めのプロセスによりすでに作成されたコンテナーを梱包します。</span><span class="sxs-lookup"><span data-stu-id="7ad65-175">**Container** ─ Pack a container that was already created by the containerization process.</span></span> <span data-ttu-id="7ad65-176">たとえば、これは、入れ子のコンテナーに使用されます。</span><span class="sxs-lookup"><span data-stu-id="7ad65-176">For example, this is used for nesting containers.</span></span>

        > [!NOTE]
        > <span data-ttu-id="7ad65-177">入れ子のコンテナーを使用するには、コンテナー詰めメソッドを繰り返し可能にする必要があります。</span><span class="sxs-lookup"><span data-stu-id="7ad65-177">To use nesting containers, you must make the containerization method repeatable.</span></span> <span data-ttu-id="7ad65-178">テンプレートの詳細については、[ウェーブ テンプレート](wave-templates.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="7ad65-178">For more information, see [Wave templates](wave-templates.md).</span></span>

1. <span data-ttu-id="7ad65-179">**一般** クイックタブの **ウェーブ ステップ コード** フィールドで、コンテナー構築テンプレートをウェーブ テンプレートの手順にリンクするウェーブ プロセス メソッドの固有の識別子を入力します。</span><span class="sxs-lookup"><span data-stu-id="7ad65-179">On the **General** FastTab, in the **Wave step code** field, enter the unique identifier of the wave process method that links the container build template to steps in a wave template.</span></span>
1. <span data-ttu-id="7ad65-180">作業者が別のコンテナーの作業指示書から品目を梱包できるように、**分割ピッキングを許可する** チェック ボックスをオンにします。</span><span class="sxs-lookup"><span data-stu-id="7ad65-180">Select the **Allow split picks** check box to allow workers to pack items from a work order in separate containers.</span></span> <span data-ttu-id="7ad65-181">これには、数量全体がコンテナーに適合する必要があります。</span><span class="sxs-lookup"><span data-stu-id="7ad65-181">This requires that the entire quantity fits in the container.</span></span> <span data-ttu-id="7ad65-182">配賦ラインの最大測定単位が常に使用されます。</span><span class="sxs-lookup"><span data-stu-id="7ad65-182">The largest unit of measure in the allocation line is always used.</span></span>
1. <span data-ttu-id="7ad65-183">**単位ごとに梱包** フィールドで、コンテナーを表す測定単位を選択します。</span><span class="sxs-lookup"><span data-stu-id="7ad65-183">In the **Pack by unit** field, select the unit of measure that will represent the container.</span></span> <span data-ttu-id="7ad65-184">たとえば、ケースがコンテナーであることを示すことができます。</span><span class="sxs-lookup"><span data-stu-id="7ad65-184">For example, you can indicate that a case is a container.</span></span> <span data-ttu-id="7ad65-185">測定単位ごとに梱包する場合、測定単位がコンテナーであるため、コンテナー グループを指定することはできません。</span><span class="sxs-lookup"><span data-stu-id="7ad65-185">If you pack by the unit of measure, you cannot also specify a container group because the unit of measure is the container.</span></span>
1. <span data-ttu-id="7ad65-186">**コンテナー梱包計画** フィールドで、使用する梱包計画を選択します。</span><span class="sxs-lookup"><span data-stu-id="7ad65-186">In the **Container packing strategy** field, select the packing strategy to use.</span></span> <span data-ttu-id="7ad65-187">次のオプションを使用できます。</span><span class="sxs-lookup"><span data-stu-id="7ad65-187">The following options are available:</span></span>

    > [!NOTE]
    > <span data-ttu-id="7ad65-188">計画は販売配賦ラインと移動配賦ラインにのみ適用されます。</span><span class="sxs-lookup"><span data-stu-id="7ad65-188">The strategy applies only to sales allocation lines and transfer allocation lines.</span></span>

      - <span data-ttu-id="7ad65-189">**空のコンテナーすべてに梱包** システムによって、配賦ラインがコンテナー詰めのサイクル中に作成されたコンテナーに適合するかどうかが評価されます。</span><span class="sxs-lookup"><span data-stu-id="7ad65-189">**Pack into all open containers** – The system evaluates whether the allocation line will fit in any container that was created during the containerization cycle.</span></span>
      - <span data-ttu-id="7ad65-190">**現在のコンテナーにのみ梱包** – システムにより、配賦ラインが最近作成されたコンテナーに適合するかどうかが評価されます。</span><span class="sxs-lookup"><span data-stu-id="7ad65-190">**Pack into current container only** – The system only evaluates whether the allocation line will fit in the most recently created container.</span></span>

    <span data-ttu-id="7ad65-191">コンテナー梱包計画の使用方法を示す詳細と例については、[コンテナー梱包計画](container-packing-strategy-overview.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="7ad65-191">For more information and examples that show how to work with container packing strategies, see [Container packing strategies](container-packing-strategy-overview.md).</span></span>

1. <span data-ttu-id="7ad65-192">コンテナーに配賦ラインを梱包するルールを設定するには、**混合ロジック ブレーク** を選択します。</span><span class="sxs-lookup"><span data-stu-id="7ad65-192">To set up rules for packing allocation lines in containers, select **Mixing Logic Breaks**.</span></span> <span data-ttu-id="7ad65-193">たとえば、作業者が同じコンテナーの 2 種類の品目の配賦ラインを梱包できるようにするルールを作成できます。</span><span class="sxs-lookup"><span data-stu-id="7ad65-193">For example, you can create a rule that will allow workers to pack allocation lines for two different items in the same container.</span></span> <span data-ttu-id="7ad65-194">混合ルールを定義するには、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="7ad65-194">To define a mixing rule, follow these steps:</span></span>

    1. <span data-ttu-id="7ad65-195">**混合ロジック ブレーク** で、**新規作成** を選択します。</span><span class="sxs-lookup"><span data-stu-id="7ad65-195">In the **Mixing Logic Breaks** page, select **New**.</span></span>
    1. <span data-ttu-id="7ad65-196">**テーブル** フィールドで、混合ロジックの分割の基準として使用するフィールドを含むテーブルを選択します。</span><span class="sxs-lookup"><span data-stu-id="7ad65-196">In the **Table** field, select the table that contains the field to use as a criterion for the mixing logic break.</span></span>
    1. <span data-ttu-id="7ad65-197">**フィールド選択** フィールドで、混合ロジックの分割の基準として使用するフィールドを選択します。</span><span class="sxs-lookup"><span data-stu-id="7ad65-197">In the **Field Select** field, select the field to use as a criterion for the mixing logic break.</span></span>
    1. <span data-ttu-id="7ad65-198">混合ロジックの分割のすべての基準を追加するまで、次の手順を繰り返します。</span><span class="sxs-lookup"><span data-stu-id="7ad65-198">Repeat these steps until you have added all of the criteria for the mixing logic break.</span></span>

    > [!NOTE]
    > <span data-ttu-id="7ad65-199">混合ロジックを使用する場合は、フィルター基準クエリの同じフィールドで並べ替えることをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="7ad65-199">If you use mixing logic, we recommend that you sort by the same fields in the filter criteria query.</span></span> <span data-ttu-id="7ad65-200">これにより、作成するコンテナーの数が減ります。</span><span class="sxs-lookup"><span data-stu-id="7ad65-200">This will reduce the number of containers that are created.</span></span>
