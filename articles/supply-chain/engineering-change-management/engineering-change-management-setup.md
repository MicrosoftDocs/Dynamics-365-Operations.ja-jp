---
title: エンジニアリング変更管理の共通の値の設定
description: このトピックでは、エンジニアリングの変更管理のさまざまな部分のパラメータに使用される共通の値を設定する方法について説明します。
author: t-benebo
manager: tfehr
ms.date: 09/28/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EngChgProductParameters, EngChgEcmSeverityTable, EngChgEcmSeverityRuleSet, EngChgEcmSeverityLookup,EngChgEcmSeverityChart,EngChgEcmRequestSeverityChart,EngChgEcmPriorityTable, EngChgEcmPriorityLookup, EngChgEcmPriorityChart, EngChgEcmMaterialDisposition, EngChgEcmEH
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2020-09-28
ms.dyn365.ops.version: Release 10.0.15
ms.openlocfilehash: b46bc10f8b75a58b8baefd88aa6a0b79c59d6544
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/15/2021
ms.locfileid: "5005405"
---
# <a name="establish-common-values-for-engineering-change-management"></a><span data-ttu-id="d8877-103">エンジニアリング変更管理の共通の値の設定</span><span class="sxs-lookup"><span data-stu-id="d8877-103">Establish common values for engineering change management</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="d8877-104">エンジニアリング変更管理を設定するときは、ユーザーインターフェイス (UI) の他の部分でドロップダウンリストに入力するために使用される、いくつかの値のコレクションを設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="d8877-104">When you set up engineering change management, you must establish several collections of values that will be used to fill in drop-down lists in other parts of the user interface (UI).</span></span> <span data-ttu-id="d8877-105">これらの値は、生産する製品のタイプと、特定の業務ニーズに応じて指定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="d8877-105">You should specify these values according to the types of products that you produce and your specific business needs.</span></span>

## <a name="engineering-change-categories"></a><span data-ttu-id="d8877-106">エンジニアリング変更カテゴリ</span><span class="sxs-lookup"><span data-stu-id="d8877-106">Engineering change categories</span></span>

<span data-ttu-id="d8877-107">エンジニアリング変更のカテゴリを使用して、エンジニアリング変更オーダーを整理することで、管理と確認が容易になります。</span><span class="sxs-lookup"><span data-stu-id="d8877-107">You use engineering change categories to organize your engineering change orders, so that they are easier to manage and review.</span></span> <span data-ttu-id="d8877-108">たとえば、カテゴリに応じてワークフローを設定すると、特定の部門が提案された変更を確認する必要がある場合などに便利です。</span><span class="sxs-lookup"><span data-stu-id="d8877-108">For example, you might find it useful to set up a workflow where, depending on the category, a specific department must review the proposed changes.</span></span> <span data-ttu-id="d8877-109">したがって、エンジニアリング変更オーダーには **カテゴリ** フィールドが含まれています。</span><span class="sxs-lookup"><span data-stu-id="d8877-109">Therefore, the engineering change order includes a **Category** field.</span></span>

<span data-ttu-id="d8877-110">会社で使用される技術変更カテゴリのコレクションを確立するには、**エンジニアリング変更管理 \> 設定 \> エンジニアリングの変更管理 \> 技術の変更カテゴリ** に移動します。</span><span class="sxs-lookup"><span data-stu-id="d8877-110">To establish the collection of engineering change categories that is used in your company, go to **Engineering change management \> Setup \> Engineering change management \> Engineering change categories**.</span></span> <span data-ttu-id="d8877-111">その後、アクション ペインのボタンを使用して、値を追加、削除、編集し、ドロップダウンリストに表示される順序に並べ替えたりできます。</span><span class="sxs-lookup"><span data-stu-id="d8877-111">You can then use the buttons on the Action Pane to add, remove, and edit values, and to arrange them into the order in which they should appear in the drop-down lists where they are shown.</span></span>

## <a name="engineering-change-priorities"></a><span data-ttu-id="d8877-112">エンジニアリング変更の優先順位</span><span class="sxs-lookup"><span data-stu-id="d8877-112">Engineering change priorities</span></span>

<span data-ttu-id="d8877-113">エンジニアリング変更の優先順位は、エンジニアリング変更オーダーの重要性または緊急性を示すために使用します。</span><span class="sxs-lookup"><span data-stu-id="d8877-113">You use engineering change priorities to indicate the importance or urgency of an engineering change order.</span></span> <span data-ttu-id="d8877-114">また、設計変更オーダーの重要性を追跡して、最初に処理する必要があるオーダーや速度を容易に識別できるようにするために役立ちます。</span><span class="sxs-lookup"><span data-stu-id="d8877-114">They can help you keep track of the importance of an engineering change order, so that you can easily identify which orders should be processed first, and how quickly.</span></span>

<span data-ttu-id="d8877-115">会社で使用されるエンジニアリング変更優先度のコレクションを確立するには、**エンジニアリング変更管理 \> 設定 \> エンジニアリングの変更管理 \> エンジニアリング変更優先度** に移動します。</span><span class="sxs-lookup"><span data-stu-id="d8877-115">To establish the collection of engineering change priorities that is used in your company, go to **Engineering change management \> Setup \> Engineering change management \> Engineering change priorities**.</span></span> <span data-ttu-id="d8877-116">その後、アクション ペインのボタンを使用して、値を追加、削除、編集し、ドロップダウンリストに表示される順序に並べ替えたりできます。</span><span class="sxs-lookup"><span data-stu-id="d8877-116">You can then use the buttons on the Action Pane to add, remove, and edit values, and to arrange them into the order in which they should appear in the drop-down lists where they are shown.</span></span>

## <a name="engineering-change-reasons"></a><span data-ttu-id="d8877-117">エンジニアリング変更理由</span><span class="sxs-lookup"><span data-stu-id="d8877-117">Engineering change reasons</span></span>

<span data-ttu-id="d8877-118">エンジニアリング変更の理由は、変更オーダーの原因や性質を示します。</span><span class="sxs-lookup"><span data-stu-id="d8877-118">Engineering change reasons indicate the cause or nature of the change in the change order.</span></span>

<span data-ttu-id="d8877-119">会社で使用されるエンジニアリング変更理由のコレクションを確立するには、**エンジニアリング変更管理 \> 設定 \> エンジニアリングの変更管理 \> エンジニアリング変更理由** に移動します。</span><span class="sxs-lookup"><span data-stu-id="d8877-119">To establish the collection of engineering change reasons that is used in your company, go to **Engineering change management \> Setup \> Engineering change management \> Engineering change reasons**.</span></span> <span data-ttu-id="d8877-120">その後、アクション ペインのボタンを使用して、値を追加、削除、編集し、ドロップダウンリストに表示される順序に並べ替えたりできます。</span><span class="sxs-lookup"><span data-stu-id="d8877-120">You can then use the buttons on the Action Pane to add, remove, and edit values, and to arrange them into the order in which they should appear in the drop-down lists where they are shown.</span></span>

## <a name="material-disposal-codes"></a><span data-ttu-id="d8877-121">材料廃棄コード</span><span class="sxs-lookup"><span data-stu-id="d8877-121">Material disposal codes</span></span>

<span data-ttu-id="d8877-122">材料処分コードを使用して、完成品で使用されている材料、または特定の方法で処分する必要がある、または通常のごみ箱に入れる前に処置を必要とするコンポーネントを分類します。</span><span class="sxs-lookup"><span data-stu-id="d8877-122">You use material disposal codes to categorize materials that are used in your finished goods, or components that must be disposed of in a specific way or require some treatment before they can be added to your regular trash.</span></span> <span data-ttu-id="d8877-123">関連する製品をエンジニアリングの変更オーダーに追加するときに、変更の詳細の一部として処分コードを割り当てることができます。</span><span class="sxs-lookup"><span data-stu-id="d8877-123">When you add a relevant product to an engineering change order, you can assign a disposal code as part of the change details.</span></span>

<span data-ttu-id="d8877-124">会社で使用される材料処分コードのコレクションを確立するには、**エンジニアリング変更管理 \> 設定 \> エンジニアリングの変更管理 \> 材料処分コード** に移動します。</span><span class="sxs-lookup"><span data-stu-id="d8877-124">To establish the collection of material disposal codes that is used in your company, go to **Engineering change management \> Setup \> Engineering change management \> Material disposal codes**.</span></span> <span data-ttu-id="d8877-125">その後、アクション ペインのボタンを使用して、値を追加、削除、編集し、ドロップダウンリストに表示される順序に並べ替えたりできます。</span><span class="sxs-lookup"><span data-stu-id="d8877-125">You can then use the buttons on the Action Pane to add, remove, and edit values, and to arrange them into the order in which they should appear in the drop-down lists where they are shown.</span></span>

## <a name="received-customer-approval"></a><span data-ttu-id="d8877-126">顧客の承認を受け取りました</span><span class="sxs-lookup"><span data-stu-id="d8877-126">Received customer approval</span></span>

<span data-ttu-id="d8877-127">特定の顧客の製品を設計する場合、多くの場合、製品を準備完了として設定できるようにする前に、設計と仕様を検証する必要があります。</span><span class="sxs-lookup"><span data-stu-id="d8877-127">When you design products for a specific customer, the design and specifications often must be validated before the product can be set as ready.</span></span> <span data-ttu-id="d8877-128">**受信した顧客の承認** フィールドを使用すると、顧客の承認プロセスで製品がどの段階にあるのかや、承認が受け入れられたかどうかを示すことができます。</span><span class="sxs-lookup"><span data-stu-id="d8877-128">The **Received customer approval** field lets you indicate how far in the customer approval process the product is and/or whether the approval has been received.</span></span>

<span data-ttu-id="d8877-129">会社で使用される受信した顧客の承認のコレクションを確立するには、**エンジニアリング変更管理 \> 設定 \> エンジニアリングの変更管理 \> 受信した顧客の承認** に移動します。</span><span class="sxs-lookup"><span data-stu-id="d8877-129">To establish the collection of received customer approval values that is used in your company, go to **Engineering change management \> Setup \> Engineering change management \> Received customer approval**.</span></span> <span data-ttu-id="d8877-130">その後、アクション ペインのボタンを使用して、値を追加、削除、編集し、ドロップダウンリストに表示される順序に並べ替えたりできます。</span><span class="sxs-lookup"><span data-stu-id="d8877-130">You can then use the buttons on the Action Pane to add, remove, and edit values, and to arrange them into the order in which they should appear in the drop-down lists where they are shown.</span></span>

## <a name="engineering-change--environmental-health-and-safety-codes"></a><span data-ttu-id="d8877-131">エンジニアリング変更 - 環境の健全性と安全コード</span><span class="sxs-lookup"><span data-stu-id="d8877-131">Engineering change – Environmental health and safety codes</span></span>

<span data-ttu-id="d8877-132">製品の製造時に、標準の環境健全性や安全の対策、または会社固有の規制や手順を考慮する必要がある場合は、環境の健全性と安全の対策を定義することができます。</span><span class="sxs-lookup"><span data-stu-id="d8877-132">If any standard environmental health and safety regulations, or company-specific regulations or procedures, must be considered in the manufacture of a product, you can use the environmental health and safety codes to define them.</span></span> <span data-ttu-id="d8877-133">エンジニアリング変更オーダーでは、影響を受ける製品の詳細を編集する際に、製品の製造に適用するコードを指定できます。</span><span class="sxs-lookup"><span data-stu-id="d8877-133">In the engineering change order, you can indicate which codes apply to the manufacture of a product while you edit the details of the affected product.</span></span>

<span data-ttu-id="d8877-134">会社で使用される正常性と安全値のコレクションを確立するには、**エンジニアリング変更管理 \> 設定 \> エンジニアリングの変更管理 \> エンジニアリング変更 - 環境の健全性および安全の対策** に移動します。</span><span class="sxs-lookup"><span data-stu-id="d8877-134">To establish the collection of health and safety values that is used in your company, go to **Engineering change management \> Setup \> Engineering change management \> Engineering change - Environmental health and safety codes**.</span></span> <span data-ttu-id="d8877-135">その後、アクション ペインのボタンを使用して、値を追加、削除、編集し、ドロップダウンリストに表示される順序に並べ替えたりできます。</span><span class="sxs-lookup"><span data-stu-id="d8877-135">You can then use the buttons on the Action Pane to add, remove, and edit values, and to arrange them into the order in which they should appear in the drop-down lists where they are shown.</span></span>

## <a name="engineering-change-severities"></a><span data-ttu-id="d8877-136">エンジニアリング変更の重大度</span><span class="sxs-lookup"><span data-stu-id="d8877-136">Engineering change severities</span></span>

<span data-ttu-id="d8877-137">技術変更の重大度を使用して、エンジニアリング変更オーダーの製品に適用される影響レベルを指定します。</span><span class="sxs-lookup"><span data-stu-id="d8877-137">You use engineering change severities to indicate the level of impact that applies to the products in an engineering change order.</span></span>

<span data-ttu-id="d8877-138">会社で使用されるエンジニアリング変更重大度のコレクションを確立するには、**エンジニアリング変更管理 \> 設定 \> エンジニアリングの変更管理 \> エンジニアリング変更重大度** に移動します。</span><span class="sxs-lookup"><span data-stu-id="d8877-138">To establish the collection of engineering change severities that is used in your company, go to **Engineering change management \> Setup \> Engineering change management \> Engineering change severities**.</span></span> <span data-ttu-id="d8877-139">その後、アクション ペインのボタンを使用して、値を追加、削除、編集し、ドロップダウンリストに表示される順序に並べ替えたりできます。</span><span class="sxs-lookup"><span data-stu-id="d8877-139">You can then use the buttons on the Action Pane to add, remove, and edit values, and to arrange them into the order in which they should appear in the drop-down lists where they are shown.</span></span>

<span data-ttu-id="d8877-140">作成する各重大度レベルに適用されるルールを設定できます。</span><span class="sxs-lookup"><span data-stu-id="d8877-140">You can establish rules that apply to each severity level that you create.</span></span> <span data-ttu-id="d8877-141">これらのルールを割り当てる方法についての情報は、次のセクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="d8877-141">For more information about how to assign these rules, see the next section.</span></span>

## <a name="engineering-change-severity-rule-sets"></a><span data-ttu-id="d8877-142">エンジニアリング変更の重大度ルール セット</span><span class="sxs-lookup"><span data-stu-id="d8877-142">Engineering change severity rule sets</span></span>

<span data-ttu-id="d8877-143">エンジニアリング変更の重大度ルール セットを使用して、変更オーダーの重大度を自動的に計算するために使用できるルールのグループを、影響を受ける製品の変更のタイプによって設定します。</span><span class="sxs-lookup"><span data-stu-id="d8877-143">You use engineering change severity rule sets to establish a group of rules that you can use to automatically calculate the severity of the change order, based on the type of changes in the affected products.</span></span> <span data-ttu-id="d8877-144">この重大度ルールを使用するには、**エンジニアリング変更管理パラメータ** ページを開き、**重大度ルール** フィールドを *計算* または *自動的に計算* に設定します。</span><span class="sxs-lookup"><span data-stu-id="d8877-144">To use the severity rules, open the **Engineering change management parameters** page, and set the **Severity rule** field to *Calculate* or *Calculate automatically*.</span></span>

<span data-ttu-id="d8877-145">システムが重大度を評価すると、ページに表示されている順序 (上から下) で規則が処理されます。</span><span class="sxs-lookup"><span data-stu-id="d8877-145">When the system evaluates severity, it processes the rules in the order in which they appear on the page, from top to bottom.</span></span> <span data-ttu-id="d8877-146">ルールを選択してその優先順位を確立するには、ルール セット内のすべてのルールが満たされている必要があります。</span><span class="sxs-lookup"><span data-stu-id="d8877-146">For a rule to be selected and have its priority established, all the rules in a rule set must be met.</span></span>

<span data-ttu-id="d8877-147">定義した各変更の重大度レベルに適用されるルールを設定するには、**エンジニアリング変更管理 \> 設定 \> エンジニアリング変更管理 \> エンジニアリング変更重大度ルール セット** に移動します。</span><span class="sxs-lookup"><span data-stu-id="d8877-147">To set up the rules that apply to each change severity level that you've defined, go to **Engineering change management \> Setup \> Engineering change management \> Engineering change severity rule sets**.</span></span> <span data-ttu-id="d8877-148">そして、次の手順のいずれかを実行します。</span><span class="sxs-lookup"><span data-stu-id="d8877-148">Then follow one of these steps.</span></span>

- <span data-ttu-id="d8877-149">新しいルール セットを作成するには、アクション ペインで **新規** を選択し、次のセクションで後に説明されているフィールドを設定します。</span><span class="sxs-lookup"><span data-stu-id="d8877-149">To create a new rule set, select **New** on the Action Pane, and then set the fields as described later in this section.</span></span>
- <span data-ttu-id="d8877-150">既存のルール セットを編集するには、リスト ペインでルール セットを選択し、アクション ペインで **編集** を選択して、次のセクションで後に説明されている通りフィールドを設定します。</span><span class="sxs-lookup"><span data-stu-id="d8877-150">To edit an existing rule set, select it in the list pane, select **Edit** on the Action Pane, and then set the fields as described later in this section.</span></span>
- <span data-ttu-id="d8877-151">既存のルール セットを削除するには、リスト ペインでルール セットを選択し、アクション ペインで **削除** を選択します。</span><span class="sxs-lookup"><span data-stu-id="d8877-151">To delete an existing rule set, select it in the list pane, and then select **Delete** on the Action Pane.</span></span>
- <span data-ttu-id="d8877-152">ルール セットの一覧を並べ替えるには、[リスト] ペインでルール セットを選択し、アクション ペインの **上へ** ボタンと **下へ** ボタンを使用して位置変更をします。</span><span class="sxs-lookup"><span data-stu-id="d8877-152">To rearrange the list of rule sets, select a rule set in the list pane, and then use the **Up** and **Down** buttons on the Action Pane to reposition it.</span></span>

<span data-ttu-id="d8877-153">各ルール セットで、次のフィールドを設定します。</span><span class="sxs-lookup"><span data-stu-id="d8877-153">For each rule set, set the following field:</span></span>

- <span data-ttu-id="d8877-154">**重大度** - ルールを確立する重大度レベルを選択します。</span><span class="sxs-lookup"><span data-stu-id="d8877-154">**Severity** – Select the severity level to establish rules for.</span></span> <span data-ttu-id="d8877-155">レベルを作成して名前を付けるには、**技術変更の重大度** ページを使用します。</span><span class="sxs-lookup"><span data-stu-id="d8877-155">You use the **Engineering change severities** page to create and name the levels.</span></span> <span data-ttu-id="d8877-156">(詳細については、前のセクションを参照してください。)</span><span class="sxs-lookup"><span data-stu-id="d8877-156">(For more information, see the previous section.)</span></span>

<span data-ttu-id="d8877-157">現在の重大度の設定に対してルールを追加または削除するには、**ルール** クイックタブのボタンを使用します。</span><span class="sxs-lookup"><span data-stu-id="d8877-157">Use the buttons on the **Rules** FastTab to add or remove a rule for the current severity setting.</span></span> <span data-ttu-id="d8877-158">各ルールには、**ルール** フィールドと **名前** フィールドがあります。</span><span class="sxs-lookup"><span data-stu-id="d8877-158">Each rule has a **Rule** field and a **Name** field.</span></span> <span data-ttu-id="d8877-159">このルールはシステムによって設定され、製品に対して設定できる変更のタイプを示します。</span><span class="sxs-lookup"><span data-stu-id="d8877-159">The rules are established by the system and indicate the types of changes that a product can have.</span></span> <span data-ttu-id="d8877-160">この名前は変更のタイプを示します。</span><span class="sxs-lookup"><span data-stu-id="d8877-160">The name indicates the type of change.</span></span>
