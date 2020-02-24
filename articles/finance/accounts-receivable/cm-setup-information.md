---
title: 与信管理の設定
description: このトピックでは、与信管理に必要な設定について説明します。
author: mikefalkner
manager: AnnBe
ms.date: 09/04/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mfalkner
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: c54c74af6f2c1be9aedfa792d0676d1165fb0ab8
ms.sourcegitcommit: 6a70f9ac296158edd065d52a12703b3ce85ce5ee
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/03/2020
ms.locfileid: "3015299"
---
# <a name="credit-management-setup"></a><span data-ttu-id="66807-103">与信管理の設定</span><span class="sxs-lookup"><span data-stu-id="66807-103">Credit management setup</span></span> 

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

## <a name="credit-management-workflows"></a><span data-ttu-id="66807-104">与信管理のワークフロー</span><span class="sxs-lookup"><span data-stu-id="66807-104">Credit management workflows</span></span>

<span data-ttu-id="66807-105">**与信および取立 \> 設定 \> 与信管理ワークフロー**に移動し、与信限度額調整を管理するのに使用されるワークフローを定義します。</span><span class="sxs-lookup"><span data-stu-id="66807-105">Go to **Credit and collections \> Setup \> Credit management workflows** to define the workflows that are used to manage credit limit adjustments.</span></span>

- <span data-ttu-id="66807-106">単一の承認で与信限度額調整のバッチを承認するワークフローを作成できます。</span><span class="sxs-lookup"><span data-stu-id="66807-106">You can create a workflow that lets you approve a batch of credit limits adjustments through a single approval.</span></span>
- <span data-ttu-id="66807-107">与信限度額調整を個別に承認できるように、明細行レベルでワークフローを追加することができます。</span><span class="sxs-lookup"><span data-stu-id="66807-107">You can add a workflow at the line level, so that credit limit adjustments can be approved individually.</span></span>
- <span data-ttu-id="66807-108">保留をワークフロー プロセスに自動的に転送するリリース ワークフローを作成できます。</span><span class="sxs-lookup"><span data-stu-id="66807-108">You can create a release workflow that automatically routes holds to a workflow process.</span></span>

## <a name="blocking-rules"></a><span data-ttu-id="66807-109">ブロックのルール</span><span class="sxs-lookup"><span data-stu-id="66807-109">Blocking rules</span></span>

### <a name="ranking-payment-terms"></a><span data-ttu-id="66807-110">支払条件のランク付け</span><span class="sxs-lookup"><span data-stu-id="66807-110">Ranking payment terms</span></span>

<span data-ttu-id="66807-111">注文の支払条件が顧客の既定の支払条件と一致しない場合、販売注文を保留中にすることができます。</span><span class="sxs-lookup"><span data-stu-id="66807-111">You can put a sales order on hold if the payment terms on the order don't match the default payment terms for the customer.</span></span> <span data-ttu-id="66807-112">ただし、支払条件は異なるものの、注文を保留にする必要がないほど類似している場合もあります。</span><span class="sxs-lookup"><span data-stu-id="66807-112">However, sometimes the payment terms differ but are similar enough that you don't want to put the order on hold.</span></span> <span data-ttu-id="66807-113">支払条件をランク付けして、一部のランクを同じランクにしたり、他のランクを高くもしくは低くすることができます。</span><span class="sxs-lookup"><span data-stu-id="66807-113">You can rank payment terms so that some of them have the same rank, whereas others have a higher or lower rank.</span></span>

<span data-ttu-id="66807-114">支払条件のランキングが有効であり、注文の支払条件のランクが顧客の既定の支払条件よりも高い場合、販売注文は保留されます。</span><span class="sxs-lookup"><span data-stu-id="66807-114">If the rankings for payment terms are active, the sales orders will be put on hold if the payment terms on the order have a higher rank than the default payment terms for the customer.</span></span>

### <a name="ranking-settlement-discounts"></a><span data-ttu-id="66807-115">決済割引のランク付け</span><span class="sxs-lookup"><span data-stu-id="66807-115">Ranking settlement discounts</span></span>

<span data-ttu-id="66807-116">注文の現金割引と顧客の既定の現金割引が一致しない場合は、販売注文を保留にすることができます。</span><span class="sxs-lookup"><span data-stu-id="66807-116">You can put a sales order on hold if the cash discount on the order doesn't match the default cash discount for the customer.</span></span> <span data-ttu-id="66807-117">ただし、現金割引が異なるものの、注文を保留にする必要がないほど類似している場合もあります。</span><span class="sxs-lookup"><span data-stu-id="66807-117">However, sometimes the cash discounts differ but are similar enough that you don't want to put the order on hold.</span></span> <span data-ttu-id="66807-118">一部のランクが同じである場合や、高かったり低かったりする場合に、現金割引をランク付けできます。</span><span class="sxs-lookup"><span data-stu-id="66807-118">You can rank cash discounts so that some of them have the same rank, whereas others have a higher or lower rank.</span></span>

<span data-ttu-id="66807-119">決済割引のランキングが有効であり、注文の現金割引が顧客の既定の現金割引よりも高いランクの場合、販売注文は保留されます。</span><span class="sxs-lookup"><span data-stu-id="66807-119">If rankings for settlement discounts are active, the sales orders will be put on hold if the cash discount on the order has a higher rank than the default cash discount for the customer.</span></span>

## <a name="reasons"></a><span data-ttu-id="66807-120">理由</span><span class="sxs-lookup"><span data-stu-id="66807-120">Reasons</span></span>

<span data-ttu-id="66807-121">与信管理では、いくつかのタイプの理由が使用されます。</span><span class="sxs-lookup"><span data-stu-id="66807-121">Several types of reasons are used in Credit management:</span></span>

- <span data-ttu-id="66807-122">保留の理由は、販売注文が保留された理由を示します。</span><span class="sxs-lookup"><span data-stu-id="66807-122">Hold reasons indicate why a sales order was put on hold.</span></span>
- <span data-ttu-id="66807-123">リリースの理由は、保留からリリースされると注文に割り当てられます。</span><span class="sxs-lookup"><span data-stu-id="66807-123">Release reasons are assigned to an order when it's released from hold.</span></span>
- <span data-ttu-id="66807-124">ステータスの理由は、顧客にアカウント ステータスが割り当てられた理由を示します。</span><span class="sxs-lookup"><span data-stu-id="66807-124">Status reasons indicate why an account status was assigned to a customer.</span></span>

<span data-ttu-id="66807-125">理由は、**与信管理の理由**ページ (**与信管理\>設定\>与信管理\>与信管理の理由**) で設定できます。</span><span class="sxs-lookup"><span data-stu-id="66807-125">You can set up reasons on the **Credit management reasons** page (**Credit management \> Setup \> Credit management \> Credit management reasons**).</span></span>

1. <span data-ttu-id="66807-126">**理由タイプ** フィールドで、**保留**、**リリース**、または**ステータス**から、理由タイプを選択します。</span><span class="sxs-lookup"><span data-stu-id="66807-126">In the **Reason type** field, select the type of reason: **Hold**, **Release**, or **Status**.</span></span>
2. <span data-ttu-id="66807-127">**理由**フィールドに、理由の名前を入力します。</span><span class="sxs-lookup"><span data-stu-id="66807-127">In the **Reason** field, enter a name for the reason.</span></span>
3. <span data-ttu-id="66807-128">**説明**フィールドに、理由コードの説明を入力します。</span><span class="sxs-lookup"><span data-stu-id="66807-128">In the **Description** field, enter a description of the reason code.</span></span>

## <a name="credit-management-groups"></a><span data-ttu-id="66807-129">与信管理グループ</span><span class="sxs-lookup"><span data-stu-id="66807-129">Credit management groups</span></span>

<span data-ttu-id="66807-130">与信管理グループは、同じ与信管理プロパティを持つ顧客または顧客グループを識別するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="66807-130">Credit management groups are used to identify customers or groups of customers that have the same credit management properties.</span></span> <span data-ttu-id="66807-131">たとえば、与信管理グループを使用して、顧客のブロックおよび除外の与信管理ルールを決定できます。</span><span class="sxs-lookup"><span data-stu-id="66807-131">For example, credit management groups can be used to determine the blocking and exclusion credit management rules for customers.</span></span>

<span data-ttu-id="66807-132">**与信管理グループ** ページで与信管理グループを作成できます (**与信管理 \> 設定 > グループ設定 \> 与信管理グループ**)。</span><span class="sxs-lookup"><span data-stu-id="66807-132">You can create credit management groups on the **Credit management groups** page (**Credit management \> Setup> Groups setup \> Credit management groups**).</span></span>

1. <span data-ttu-id="66807-133">**新規**を選択して、明細行を作成します。</span><span class="sxs-lookup"><span data-stu-id="66807-133">Select **New** to create a line.</span></span>
2. <span data-ttu-id="66807-134">グループの ID を入力します。</span><span class="sxs-lookup"><span data-stu-id="66807-134">Enter an ID for the group.</span></span> <span data-ttu-id="66807-135">ID には、最大 10 文字まで入力できます。</span><span class="sxs-lookup"><span data-stu-id="66807-135">The ID can have up to 10 characters.</span></span>
3. <span data-ttu-id="66807-136">**説明**フィールドに、グループの名前を入力します。</span><span class="sxs-lookup"><span data-stu-id="66807-136">In the **Description** field, enter a name for the group.</span></span> <span data-ttu-id="66807-137">名前には、最大 60 文字まで入力できます。</span><span class="sxs-lookup"><span data-stu-id="66807-137">The name can have up to 60 characters.</span></span>

<span data-ttu-id="66807-138">**すべての顧客**ページ (**売掛金勘定 \> 顧客 \> すべての顧客**) の**与信および取立**クイック タブでは、与信管理グループが顧客に割り当てられます。</span><span class="sxs-lookup"><span data-stu-id="66807-138">The credit management group is assigned to a customer on the **Credit and collections** FastTab of the **All customers** page (**Account receivable \> Customers \> All customers**).</span></span>

## <a name="account-statuses"></a><span data-ttu-id="66807-139">勘定状態</span><span class="sxs-lookup"><span data-stu-id="66807-139">Account statuses</span></span>

<span data-ttu-id="66807-140">アカウント ステータスを作成して、顧客アカウントの与信状況を識別することができます。</span><span class="sxs-lookup"><span data-stu-id="66807-140">You can create account statuses to identify the credit standing of a customer account.</span></span> <span data-ttu-id="66807-141">請求および出荷の保留プロセスに対する状態とその影響を定義できます。</span><span class="sxs-lookup"><span data-stu-id="66807-141">You can define a status and its effect on the invoicing and delivery on-hold processes.</span></span> <span data-ttu-id="66807-142">アカウント ステータスを使用して、顧客のブロック ルールを決定することもできます。</span><span class="sxs-lookup"><span data-stu-id="66807-142">Account statuses can also be used to determine blocking rules for a customer.</span></span>

<span data-ttu-id="66807-143">**アカウント ステータス** ページ (**与信管理\> 設定 > グループ設定\>アカウント ステータス**) でアカウント ステータスを作成できます。</span><span class="sxs-lookup"><span data-stu-id="66807-143">You can create account statuses on the **Account statuses** page (**Credit management \> Setup> Groups setup \> Account statuses**).</span></span>

1. <span data-ttu-id="66807-144">アカウント ステータスを追加し、顧客の与信状況を表す説明を入力します。</span><span class="sxs-lookup"><span data-stu-id="66807-144">Add an account status, and enter a description that represents the credit standing for a customer.</span></span> <span data-ttu-id="66807-145">たとえば、**標準**を使用すると、顧客が良好な状態にあり、オープン注文が標準与信管理プロセスの対象となることを示します。</span><span class="sxs-lookup"><span data-stu-id="66807-145">For example, use **Normal** to indicate that a customer is in good standing and open orders are subject to standard credit management processing.</span></span>
2. <span data-ttu-id="66807-146">**請求**および**配送保留中**フィールドで、このアカウント ステータスを持つ顧客に対して行う保留のタイプを選択します。</span><span class="sxs-lookup"><span data-stu-id="66807-146">In the **Invoicing** and **Delivery on Hold** fields, select the type of hold that should occur for customers who have this account status.</span></span> <span data-ttu-id="66807-147">与信限度ルールが適用される場合、すべての処理を保留するか、請求書処理のみを保留するか、または処理を保留しないことできます。</span><span class="sxs-lookup"><span data-stu-id="66807-147">You can hold all processing, hold only invoice processing, or hold no processing when the credit limit rules are applied.</span></span>

## <a name="scoring-groups"></a><span data-ttu-id="66807-148">スコア グループ</span><span class="sxs-lookup"><span data-stu-id="66807-148">Scoring groups</span></span>

<span data-ttu-id="66807-149">スコアリング グループを設定して、リスク要因と、測定に使用される基準を定義できます。</span><span class="sxs-lookup"><span data-stu-id="66807-149">You can set up scoring groups to define risk factors and the criteria that are used to measure them.</span></span> <span data-ttu-id="66807-150">顧客に関する情報がスコアリング グループに適用されると、リスク要素ごとにスコアが計算され、顧客をリスク グループに入れるために使用されます。</span><span class="sxs-lookup"><span data-stu-id="66807-150">When information about a customer is applied to a scoring group, a score is calculated for each risk factor and used to put the customer in a risk group.</span></span> <span data-ttu-id="66807-151">このリスク グループを使用して、与信価値の識別と自動与信限度額の計算を行うことができます。</span><span class="sxs-lookup"><span data-stu-id="66807-151">The risk group can be used to identify credit worthiness and calculate automatic credit limits.</span></span>

<span data-ttu-id="66807-152">スコアリング グループは、**スコアリング グループ** ページ (**与信管理\>設定\>リスクの設定\>スコアリング グループ**) で作成できます。</span><span class="sxs-lookup"><span data-stu-id="66807-152">You can create scoring groups on the **Scoring groups** page (**Credit management \> Setup \> Risk setup \> Scoring groups**).</span></span>

1. <span data-ttu-id="66807-153">スコアリング グループを作成し、その名前を入力します。</span><span class="sxs-lookup"><span data-stu-id="66807-153">Create a scoring group, and enter a name for it.</span></span>
2. <span data-ttu-id="66807-154">スコアリング グループについての詳細説明を入力します。</span><span class="sxs-lookup"><span data-stu-id="66807-154">Enter a description to further describe the scoring group.</span></span>
3. <span data-ttu-id="66807-155">グループのタイプを選択します。</span><span class="sxs-lookup"><span data-stu-id="66807-155">Select a group type.</span></span> <span data-ttu-id="66807-156">事前に定義された 8 つのタイプがあります。</span><span class="sxs-lookup"><span data-stu-id="66807-156">There are eight predefined types.</span></span> <span data-ttu-id="66807-157">**ユーザー定義**を選択して、組織に適したグループ タイプを定義することもできます。</span><span class="sxs-lookup"><span data-stu-id="66807-157">You can also select **User defined** to define a group type that's better suited to your organization.</span></span>
4. <span data-ttu-id="66807-158">スコアのタイプを選択して、スコアリング グループがリスク スコアを計算する方法を定義します。</span><span class="sxs-lookup"><span data-stu-id="66807-158">Select a score type to define how the scoring group calculates the risk score.</span></span> <span data-ttu-id="66807-159">次のオプションを使用できます。</span><span class="sxs-lookup"><span data-stu-id="66807-159">The following options are available:</span></span>

    - <span data-ttu-id="66807-160">**範囲** - このオプションを使用して、スコアの計算に使用する値の範囲を定義します。</span><span class="sxs-lookup"><span data-stu-id="66807-160">**Range** – Use this option to define a range of values that should be used to calculate a score.</span></span>
    - <span data-ttu-id="66807-161">**ユーザー定義** - このオプションを使用して、スコアに使用する値の一覧を手動で定義します。</span><span class="sxs-lookup"><span data-stu-id="66807-161">**User defined** – Use this option to manually define a list of values that should be used for the score.</span></span>

5. <span data-ttu-id="66807-162">スコア タイプとして**範囲**を選択した場合は、値の範囲とそれに対応するスコアを定義する明細行を追加します。</span><span class="sxs-lookup"><span data-stu-id="66807-162">If you selected **Range** as the score type, add lines to define the range of values and the corresponding scores.</span></span>

    1. <span data-ttu-id="66807-163">**開始値**フィールドで、範囲内の最小値を指定します。</span><span class="sxs-lookup"><span data-stu-id="66807-163">In the **From value** field, specify the lowest value in the range.</span></span>
    2. <span data-ttu-id="66807-164">**終了値**フィールドで、範囲内の最高値を指定します。</span><span class="sxs-lookup"><span data-stu-id="66807-164">In the **To value** field, specify the highest value in the range.</span></span>
    3. <span data-ttu-id="66807-165">**スコア** フィールドに、指定した値が開始 / 終了の範囲内にある場合に割り当てるスコアを入力します。</span><span class="sxs-lookup"><span data-stu-id="66807-165">In the **Score** field, enter the score that should be assigned when the value that is provided is in the "from"/"to" range.</span></span>

    <span data-ttu-id="66807-166">スコア タイプとして**ユーザー定義**を選択した場合は、明細行を追加して、ユーザー定義の値とそれに対応するスコアを定義します。</span><span class="sxs-lookup"><span data-stu-id="66807-166">If you selected **User defined** as the score type, add lines to define the user-defined values and the corresponding scores.</span></span>

    1. <span data-ttu-id="66807-167">**値**フィールドに、顧客情報から提供されるユーザー定義の値を入力します。</span><span class="sxs-lookup"><span data-stu-id="66807-167">In the **Value** field, enter the user-defined value that should be provided from the customer information.</span></span>
    2. <span data-ttu-id="66807-168">**スコア** フィールドに、指定した値が開始 / 終了の範囲内にある場合に割り当てるスコアを入力します。</span><span class="sxs-lookup"><span data-stu-id="66807-168">In the **Score** field, enter the score that should be assigned when the value that is provided is in the "from"/"to" range.</span></span>

## <a name="risk-assessments"></a><span data-ttu-id="66807-169">リスク評価</span><span class="sxs-lookup"><span data-stu-id="66807-169">Risk assessments</span></span>

<span data-ttu-id="66807-170">リスクのスコアに基づいて、顧客に割り当てることができるリスク評価を定義できます。</span><span class="sxs-lookup"><span data-stu-id="66807-170">You can define risk assessments that can be assigned to customers, based on their risk score.</span></span> <span data-ttu-id="66807-171">リスク スコアは、顧客情報をスコアリング グループごとに比較することによって計算されます。</span><span class="sxs-lookup"><span data-stu-id="66807-171">A risk score is calculated by comparing customer information to each scoring group.</span></span> <span data-ttu-id="66807-172">スコアは合計され、合計スコアがリスク グループの設定値と比較されて、顧客が属するリスク グループが識別されます。</span><span class="sxs-lookup"><span data-stu-id="66807-172">The scores are summed, and the total score is compared to the values in the risk group setup to identify the risk group that the customer belongs to.</span></span> <span data-ttu-id="66807-173">次に、リスク グループ スコアを使用して、顧客の与信管理ブロックと除外ルールを定義します。</span><span class="sxs-lookup"><span data-stu-id="66807-173">The risk group score is then used to define credit management blocking and exclusion rules for the customer.</span></span>

<span data-ttu-id="66807-174">**リスク評価**ページ (**与信管理 \>設定\>リスク設定\>リスク評価**) でリスク グループを設定できます。</span><span class="sxs-lookup"><span data-stu-id="66807-174">You can set up risk groups on the **Risk assessments** page (**Credit management \> Setup \> Risk setup \> Risk assessments**).</span></span>

1. <span data-ttu-id="66807-175">リスク グループ ID を入力します。</span><span class="sxs-lookup"><span data-stu-id="66807-175">Enter a risk group ID.</span></span>
2. <span data-ttu-id="66807-176">リスク グループについての詳細説明を入力します。</span><span class="sxs-lookup"><span data-stu-id="66807-176">Enter a description to further explain the risk group.</span></span>
3. <span data-ttu-id="66807-177">リスク グループに属する顧客を決定するために使用されるスコアの範囲を入力します。</span><span class="sxs-lookup"><span data-stu-id="66807-177">Enter a range of scores that is used to determine which customers belong to the risk group.</span></span>
4. <span data-ttu-id="66807-178">リスク グループ インジケーターを選択して、リスク グループを表す記号を指定します。</span><span class="sxs-lookup"><span data-stu-id="66807-178">Select a risk group indicator to specify the symbol that represents the risk group.</span></span>

## <a name="guaranteeinsurance-types"></a><span data-ttu-id="66807-179">保証/保険タイプ</span><span class="sxs-lookup"><span data-stu-id="66807-179">Guarantee/insurance types</span></span>

<span data-ttu-id="66807-180">保証/保険タイプは、**保証/保険タイプ** ページ (**与信管理\>設定\>保証/保険設定\>保証/保険タイプ**) で設定できます。</span><span class="sxs-lookup"><span data-stu-id="66807-180">You can set up guarantee/insurance types on the **Guarantee/insurance types** page (**Credit management \> Setup \> Guarantee/insurance setup \> Guarantee/insurance types**).</span></span>

1. <span data-ttu-id="66807-181">保証人または保険会社の名前を識別する保証または保険タイプを入力します。</span><span class="sxs-lookup"><span data-stu-id="66807-181">Enter a guarantee or insurance type that identifies the name of the guarantor or insurance broker.</span></span>
2. <span data-ttu-id="66807-182">保証人/保険会社についての説明を入力します。</span><span class="sxs-lookup"><span data-stu-id="66807-182">Enter a description to describe the guarantor/insurance broker.</span></span>

## <a name="coverage-types"></a><span data-ttu-id="66807-183">補充タイプ</span><span class="sxs-lookup"><span data-stu-id="66807-183">Coverage types</span></span>

<span data-ttu-id="66807-184">補償タイプを使用すると、保険ポリシーをさらに分類できます。</span><span class="sxs-lookup"><span data-stu-id="66807-184">Coverage types can be used to further classify insurance policies.</span></span> <span data-ttu-id="66807-185">保証と共に使用することはできません。</span><span class="sxs-lookup"><span data-stu-id="66807-185">They can't be used with guarantees.</span></span>

<span data-ttu-id="66807-186">**補償タイプ** ページ (**与信管理\>設定\>保証/保険設定\>補償タイプ**) で、補償タイプを追加できます。</span><span class="sxs-lookup"><span data-stu-id="66807-186">You can add coverage types on the **Coverage types** page (**Credit management \> Setup \> Guarantee/insurance setup \> Coverage types**).</span></span>

1. <span data-ttu-id="66807-187">保険または保証として追加する補償のタイプを識別する補償タイプを入力します。</span><span class="sxs-lookup"><span data-stu-id="66807-187">Enter a coverage type to identify the type of coverage that should be added as insurance or a guarantee.</span></span>
2. <span data-ttu-id="66807-188">補償タイプの説明を入力します。</span><span class="sxs-lookup"><span data-stu-id="66807-188">Enter a description to describe of the coverage type.</span></span>

## <a name="automatic-credit-limits"></a><span data-ttu-id="66807-189">自動与信限度額</span><span class="sxs-lookup"><span data-stu-id="66807-189">Automatic credit limits</span></span>

<span data-ttu-id="66807-190">**自動与信限度額**のページ (**与信管理\>設定\>リスクの設定\>自動与信限度額**) で、自動与信限度額の基準を作成できます。</span><span class="sxs-lookup"><span data-stu-id="66807-190">You can create criteria for automatic credit limits on the **Automatic credit limits** page (**Credit management \> Setup \> Risk setup \> Automatic credit limits**).</span></span>

1. <span data-ttu-id="66807-191">自動与信限度額を割り当てるリスク グループを選択します。</span><span class="sxs-lookup"><span data-stu-id="66807-191">Select a risk group that the automatic credit limit should be assigned to.</span></span>
2. <span data-ttu-id="66807-192">自動与信限度額の通貨を選択します。</span><span class="sxs-lookup"><span data-stu-id="66807-192">Select the currency for the automatic credit limit.</span></span> <span data-ttu-id="66807-193">同じリスク グループに対して異なる通貨で複数の自動与信限度額を作成できます。</span><span class="sxs-lookup"><span data-stu-id="66807-193">You can create multiple automatic credit limits in different currencies for the same risk group.</span></span>
3. <span data-ttu-id="66807-194">この自動与信限度額に使用できる最大会社収益を表す収益金額を入力します。</span><span class="sxs-lookup"><span data-stu-id="66807-194">Enter the revenue amount that represents the maximum company revenue that can be used for this automatic credit limit.</span></span> <span data-ttu-id="66807-195">与信限度額が作成されると、収益金額が**財務**ページにある収益値 (**売掛金勘定\>すべての顧客\>顧客を選択\>全般\>統計\>財務**) と比較されます。</span><span class="sxs-lookup"><span data-stu-id="66807-195">When credit limits are created, the revenue amount is compared to a revenue value that is found on the **Financials** page (**Accounts receivable \> All customers \> Select a customer \> General \> Statistics \> Financial**).</span></span> <span data-ttu-id="66807-196">システムでは、**概要**セクションの最新の値が使用されます。</span><span class="sxs-lookup"><span data-stu-id="66807-196">The system uses the latest value in the **Overview** section.</span></span>

<span data-ttu-id="66807-197">次の手順に従って、選択した基準に基づいて生成される与信限度額を表す明細行を追加します。</span><span class="sxs-lookup"><span data-stu-id="66807-197">Follow these steps to add lines that represent the credit limit that will be generated based on the selected criteria.</span></span>

1. <span data-ttu-id="66807-198">与信限度額の計算に使用する顧客情報を定義するスコアリング グループを選択します。</span><span class="sxs-lookup"><span data-stu-id="66807-198">Select the scoring group that defines the customer information that should be used to calculate the credit limit.</span></span>
2. <span data-ttu-id="66807-199">スコアリング グループ情報を評価する方法を定義する比較演算子を選択します。</span><span class="sxs-lookup"><span data-stu-id="66807-199">Select the comparison operator that defines how the scoring group information should be evaluated.</span></span>
3. <span data-ttu-id="66807-200">スコアリング グループに対して指定されている値と比較する値を入力します。</span><span class="sxs-lookup"><span data-stu-id="66807-200">Enter the value that should be compared to the value that is specified for the scoring group.</span></span>
4. <span data-ttu-id="66807-201">スコアリング グループに対して指定された値と顧客情報が一致した場合に割り当てる与信限度額を入力します。</span><span class="sxs-lookup"><span data-stu-id="66807-201">Enter the credit limit that should be assigned if the customer information matches the value that is specified for the scoring group.</span></span> <span data-ttu-id="66807-202">たとえば、**低**スコアリング グループの自動与信限度額を作成します。</span><span class="sxs-lookup"><span data-stu-id="66807-202">For example, you create an automatic credit limit for the **Low** scoring group.</span></span> <span data-ttu-id="66807-203">業務年数がスコアリング グループの 1 つである場合は、顧客が業務 5 年以内の場合には 10 万の与信限度額を割り当て、10 年にわたって業務を行っている場合はその他に 20 万を割り当てる明細行を定義できます。</span><span class="sxs-lookup"><span data-stu-id="66807-203">If the years in business is one of the scoring groups, you can define one line that assigns a 100,000 credit limit if the customer has been in business five years and another line that assigns a 200,000 credit limit if the customer has been in business for 10 years.</span></span>
