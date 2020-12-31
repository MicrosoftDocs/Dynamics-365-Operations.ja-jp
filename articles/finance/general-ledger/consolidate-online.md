---
title: オンライン財務連結
description: このトピックでは、一般会計でのオンライン財務連結について説明します。
author: aprilolson
manager: AnnBe
ms.date: 07/09/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2018-5-31
ms.dyn365.ops.version: 8.0.1
ms.openlocfilehash: 86be6d4cc0af3f2fd92523d4ecd3825f2383fc48
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/13/2020
ms.locfileid: "4445181"
---
# <a name="online-financial-consolidations"></a><span data-ttu-id="93a56-103">オンライン財務連結</span><span class="sxs-lookup"><span data-stu-id="93a56-103">Online financial consolidations</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="93a56-104">このトピックでは、一般会計でのオンライン財務連結について説明します。</span><span class="sxs-lookup"><span data-stu-id="93a56-104">This topic describes online financial consolidations in General ledger.</span></span> <span data-ttu-id="93a56-105">このトピックの読み取る前に、[財務連結および通貨換算の概要](financial-consolidations-currency-translation.md)のトピックを必ず読んでください。</span><span class="sxs-lookup"><span data-stu-id="93a56-105">Before you read this topic, be sure to read the [Financial consolidations and currency translation overview](financial-consolidations-currency-translation.md) topic.</span></span>

<span data-ttu-id="93a56-106">セットアップを完了した後、**連結 [オンライン]** ページで連結の詳細を入力します。</span><span class="sxs-lookup"><span data-stu-id="93a56-106">After you've completed your setup, you enter the details of the consolidation on the **Consolidate [Online]** page.</span></span> <span data-ttu-id="93a56-107">完了したら、**OK** または **バッチ** をクリックして連結を処理することができます。</span><span class="sxs-lookup"><span data-stu-id="93a56-107">When you've finished, you can click **OK** or **Batch** to process the consolidation.</span></span>

## <a name="criteria"></a><span data-ttu-id="93a56-108">基準</span><span class="sxs-lookup"><span data-stu-id="93a56-108">Criteria</span></span>
<span data-ttu-id="93a56-109">**連結 [オンライン]** ページの **基準** タブで、アカウント、期間、および連結されるデータのタイプを定義します。</span><span class="sxs-lookup"><span data-stu-id="93a56-109">On the **Criteria** tab of the **Consolidate [Online]** page, you define the accounts, the periods, and the type of data that is being consolidated.</span></span>

<span data-ttu-id="93a56-110">![基準タブ](./media/criteria-consolidate-online.png "基準タブ")</span><span class="sxs-lookup"><span data-stu-id="93a56-110">![Criteria tab](./media/criteria-consolidate-online.png "Criteria tab")</span></span>

<span data-ttu-id="93a56-111">このタブのさまざまなフィールドの説明を次に示します。</span><span class="sxs-lookup"><span data-stu-id="93a56-111">Here is an explanation of the various fields on this tab:</span></span>

- <span data-ttu-id="93a56-112">**説明** – 統合する期間の詳細な説明を入力します。</span><span class="sxs-lookup"><span data-stu-id="93a56-112">**Description** – Enter a precise description for the period that you're consolidating.</span></span>
- <span data-ttu-id="93a56-113">**主勘定** – このセクションのフィールドを使用して、処理される主勘定を定義します。</span><span class="sxs-lookup"><span data-stu-id="93a56-113">**Main account** – Use the fields in this section to define the main accounts that will be processed.</span></span>

    - <span data-ttu-id="93a56-114">**開始** および **終了** – 処理する勘定の範囲を指定します。</span><span class="sxs-lookup"><span data-stu-id="93a56-114">**From** and **To** – Specify a range of accounts to process.</span></span> <span data-ttu-id="93a56-115">このフィールドを空のままにすると、すべての会社からの勘定すべては連結会社に移動されます。</span><span class="sxs-lookup"><span data-stu-id="93a56-115">If you leave these fields blank, all accounts from all companies will be moved to the consolidation company.</span></span> <span data-ttu-id="93a56-116">したがって、4 つの会社を統合し、各会社の勘定科目表が異なる場合、4 つのすべての会社からの勘定すべてが連結会社に作成されます。</span><span class="sxs-lookup"><span data-stu-id="93a56-116">Therefore, if you're consolidating four companies, and each company has a different chart of accounts, all accounts from all four companies will be created in the consolidation company.</span></span>
    - <span data-ttu-id="93a56-117">**連結勘定の使用** – このオプションを **はい** に設定した場合、**連結勘定の選択元** フィールドが使用できるようになります。</span><span class="sxs-lookup"><span data-stu-id="93a56-117">**Use consolidation account** – If you set this option to **Yes**, the **Select consolidation account from** field becomes available.</span></span> <span data-ttu-id="93a56-118">このフィールドで、すべての勘定を **主勘定** ページで設定されている連結勘定に連結する必要があるか、または連結勘定グループの 1 つから勘定を選択したいかを選択します。</span><span class="sxs-lookup"><span data-stu-id="93a56-118">In this field, select whether all accounts should be consolidated to the consolidation account that is set on the **Main accounts** page, or whether you want to select the account from one of the consolidation account groups.</span></span>
    - <span data-ttu-id="93a56-119">**連結勘定グループ** – 連結の主勘定マッピングに使用するグループを選択します。</span><span class="sxs-lookup"><span data-stu-id="93a56-119">**Consolidation account group** – Select the group to use for the main account mapping for the consolidation.</span></span>

- <span data-ttu-id="93a56-120">**連結期間** – このセクションのフィールドを使用して、連結期間を定義します。</span><span class="sxs-lookup"><span data-stu-id="93a56-120">**Consolidation period** – Use the fields in this section to define the consolidation period.</span></span>

    - <span data-ttu-id="93a56-121">**開始** および **終了** – 連結の日付の範囲を指定します。</span><span class="sxs-lookup"><span data-stu-id="93a56-121">**From** and **To** – Specify a range of dates for the consolidation.</span></span> <span data-ttu-id="93a56-122">このフィールドを空のままにすると、会社の元帳カレンダーで定義されているすべての期間の連結が処理されます。</span><span class="sxs-lookup"><span data-stu-id="93a56-122">If you leave these fields blank, the consolidation will be processed for all periods that are defined in the ledger calendar for the company.</span></span> <span data-ttu-id="93a56-123">これらのフィールドを空白のままにすることはお勧めしません。</span><span class="sxs-lookup"><span data-stu-id="93a56-123">We don't recommend that you leave these fields blank.</span></span>
    - <span data-ttu-id="93a56-124">**実績金額を含む** – このオプションを **はい** に設定すると実績データを連結します。</span><span class="sxs-lookup"><span data-stu-id="93a56-124">**Include actual amounts** – Set this option to **Yes** to consolidate your actual data.</span></span>
    - <span data-ttu-id="93a56-125">**予算金額を含む** – このオプションを **はい** に設定すると予算登録からのデータを連結します。</span><span class="sxs-lookup"><span data-stu-id="93a56-125">**Include budget amounts** – Set this option to **Yes** to consolidate data from the budget register.</span></span>
    - <span data-ttu-id="93a56-126">**連結中に残高を再構築する** – このオプションを **はい** に設定することはお勧めしません。</span><span class="sxs-lookup"><span data-stu-id="93a56-126">**Rebuild balances during consolidation** – We don't recommend that you set this option to **Yes**.</span></span> <span data-ttu-id="93a56-127">代わりに、別のバッチ ジョブとして残高を再構築します。</span><span class="sxs-lookup"><span data-stu-id="93a56-127">Instead, rebuild balances as a separate batch job.</span></span>

- <span data-ttu-id="93a56-128">**予算モデル** – 予算データの連結を選択した場合、このセクションのフィールドを使用して、予算モデルを定義します。</span><span class="sxs-lookup"><span data-stu-id="93a56-128">**Budget models** – If you've selected to consolidate budget data, use the fields in this section to define the budget models.</span></span>

    - <span data-ttu-id="93a56-129">**開始** および **終了** – 使用するモデルの範囲を指定します。</span><span class="sxs-lookup"><span data-stu-id="93a56-129">**From** and **To** – Specify the range of models to use.</span></span>
    - <span data-ttu-id="93a56-130">**予算レート タイプ** – 予算レートのタイプを選択して、予算データの通貨換算に使用します。</span><span class="sxs-lookup"><span data-stu-id="93a56-130">**Budget rate type** – Select the type of budget rate to use for currency translation of budget data.</span></span>

## <a name="financial-dimensions"></a><span data-ttu-id="93a56-131">財務分析コード</span><span class="sxs-lookup"><span data-stu-id="93a56-131">Financial dimensions</span></span>
<span data-ttu-id="93a56-132">**財務分析コード** タブで、連結会社に含まれる必要のある分析コードを定義します。</span><span class="sxs-lookup"><span data-stu-id="93a56-132">On the **Financial dimensions** tab, you define the dimensions that should be included in the consolidation company.</span></span> <span data-ttu-id="93a56-133">分析コードを選択するには、**詳細** フィールドを **分析コード** に設定し、それから連結会社の分析コードの順序を定義します。</span><span class="sxs-lookup"><span data-stu-id="93a56-133">To select a dimension, set the **Specification** field to **Dimension**, and then define the order of the dimension in the consolidation company.</span></span>

<span data-ttu-id="93a56-134">![財務分析コード タブ](./media/financial-dimensions-cons.png "財務分析コード タブ")</span><span class="sxs-lookup"><span data-stu-id="93a56-134">![Financial dimensions tab](./media/financial-dimensions-cons.png "Financial dimensions tab")</span></span>

<span data-ttu-id="93a56-135">定義した順序に関係なく、**主勘定** は常に最初のセグメントになります。</span><span class="sxs-lookup"><span data-stu-id="93a56-135">Regardless of the order that you define, **Main account** will always be the first segment.</span></span>

## <a name="legal-entities"></a><span data-ttu-id="93a56-136">法人</span><span class="sxs-lookup"><span data-stu-id="93a56-136">Legal entities</span></span>
<span data-ttu-id="93a56-137">**法人** タブで、連結会社に含まれる必要のある会社を定義します。</span><span class="sxs-lookup"><span data-stu-id="93a56-137">On the **Legal entities** tab, you define the companies that should be included in the consolidation company.</span></span> <span data-ttu-id="93a56-138">会社の所有権割合を定義することもできます。</span><span class="sxs-lookup"><span data-stu-id="93a56-138">You also define the ownership percentage of those companies.</span></span> <span data-ttu-id="93a56-139">100 パーセント未満の所有権を指定する場合、連結会社に指定した割合がロールアップされます。</span><span class="sxs-lookup"><span data-stu-id="93a56-139">If you specify less than 100-percent ownership, the specified percentage will be rolled up to the consolidation company.</span></span> <span data-ttu-id="93a56-140">すべての換算の差額について、**自動トランザクションの勘定** ページの設定から主勘定を選択するのに **換算差額の勘定タイプ** フィールドが使用されます。</span><span class="sxs-lookup"><span data-stu-id="93a56-140">For any translation differences, the **Account type for conversion differences** field is used to select the main account from the setup on the **Accounts for automatic transactions** page.</span></span>

<span data-ttu-id="93a56-141">![法人タブ](./media/legal-entities-cons.png "法人タブ")</span><span class="sxs-lookup"><span data-stu-id="93a56-141">![Legal entities tab](./media/legal-entities-cons.png "Legal entities tab")</span></span>

<span data-ttu-id="93a56-142">![自動トランザクション ページの勘定](./media/accounts-for-automatic-cons.png "自動トランザクション ページの勘定")</span><span class="sxs-lookup"><span data-stu-id="93a56-142">![Accounts for automatic transactions page](./media/accounts-for-automatic-cons.png "Accounts for automatic transactions page")</span></span>

## <a name="elimination"></a><span data-ttu-id="93a56-143">消去</span><span class="sxs-lookup"><span data-stu-id="93a56-143">Elimination</span></span>
<span data-ttu-id="93a56-144">**消去** タブには、消去を処理するための 3 つのオプションがあります。</span><span class="sxs-lookup"><span data-stu-id="93a56-144">On the **Elimination** tab, you have three options for processing eliminations:</span></span>

- <span data-ttu-id="93a56-145">消去ルールを選択し、それから **提案オプション** フィールドで **提案のみ** を選択します。</span><span class="sxs-lookup"><span data-stu-id="93a56-145">Select the elimination rule, and then, in the **Proposal options** field, select **Proposal only**.</span></span> <span data-ttu-id="93a56-146">このオプションにより、連結プロセス中に消去が処理されますが、1 つのステップですべてを転記するわけではありません。</span><span class="sxs-lookup"><span data-stu-id="93a56-146">This option will process the elimination during the consolidation process, but it won't post everything in one step.</span></span> <span data-ttu-id="93a56-147">後で仕訳帳を転記することもできます。</span><span class="sxs-lookup"><span data-stu-id="93a56-147">You can post the journal later.</span></span>
- <span data-ttu-id="93a56-148">消去ルールを選択し、それから **提案オプション** フィールドで **転記のみ** を選択します。</span><span class="sxs-lookup"><span data-stu-id="93a56-148">Select the elimination rule, and then, in the **Proposal options** field, select **Post only**.</span></span> <span data-ttu-id="93a56-149">このオプションにより、連結プロセス中に消去が処理され、1 つのステップですべてが転記されます。</span><span class="sxs-lookup"><span data-stu-id="93a56-149">This option will process the elimination during the consolidation process and will post everything in one step.</span></span>
- <span data-ttu-id="93a56-150">消去仕訳帳を使用し、連結プロセスから消去提案を個別に実行します。</span><span class="sxs-lookup"><span data-stu-id="93a56-150">Run an elimination proposal separately from the consolidation process by using the elimination journal.</span></span>

<span data-ttu-id="93a56-151">![消去タブ](./media/elimination-cons-onl.png "消去タブ")</span><span class="sxs-lookup"><span data-stu-id="93a56-151">![Elimination tab](./media/elimination-cons-onl.png "Elimination tab")</span></span>

<span data-ttu-id="93a56-152">消去の詳細については、[消去ルール](./elimination-rules.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="93a56-152">For more information about eliminations, see [Elimination rules](./elimination-rules.md).</span></span>

## <a name="currency-translation"></a><span data-ttu-id="93a56-153">為替換算</span><span class="sxs-lookup"><span data-stu-id="93a56-153">Currency translation</span></span>
<span data-ttu-id="93a56-154">**通貨換算** タブで、法人、勘定および為替レート タイプとレートを定義します。</span><span class="sxs-lookup"><span data-stu-id="93a56-154">On the **Currency translation** tab, you define the legal entity, account and exchange rate type, and rate.</span></span> <span data-ttu-id="93a56-155">**為替レートの適用元** フィールドでは、3 つのオプションが使用可能です。</span><span class="sxs-lookup"><span data-stu-id="93a56-155">Three options are available in the **Apply exchange rate from** field:</span></span>

- <span data-ttu-id="93a56-156">**連結日** – 連結の日付は、為替レートを取得するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="93a56-156">**Consolidation date** – The date of the consolidation will be used to get the exchange rate.</span></span> <span data-ttu-id="93a56-157">このレートは、スポットまたは月末のレートに相当します。</span><span class="sxs-lookup"><span data-stu-id="93a56-157">This rate is equivalent to the spot or month-end rate.</span></span> <span data-ttu-id="93a56-158">レートのプレビューは表示されますが、編集することはできません。</span><span class="sxs-lookup"><span data-stu-id="93a56-158">You will see a preview of the rate, but you can't edit it.</span></span>
- <span data-ttu-id="93a56-159">**トランザクション日付** – 各トランザクションの日付は、為替レートを選択するのに使用されます。</span><span class="sxs-lookup"><span data-stu-id="93a56-159">**Transaction date** – The date of each transaction will be used to select an exchange rate.</span></span> <span data-ttu-id="93a56-160">ほとんどの場合、このオプションは固定資産に使用され、多くの場合、過去のレートとして参照されます。</span><span class="sxs-lookup"><span data-stu-id="93a56-160">This option is most often used for fixed assets and is often referred to as a historical rate.</span></span> <span data-ttu-id="93a56-161">勘定範囲内のさまざまなトランザクションには多くのレートがあるため、レートのプレビューは表示できません。</span><span class="sxs-lookup"><span data-stu-id="93a56-161">You can't see a preview of the rate, because there will be many rates for the various transactions in the account range.</span></span>
- <span data-ttu-id="93a56-162">**ユーザー定義レート** – このオプションを選択した後、為替レートを入力することができます。</span><span class="sxs-lookup"><span data-stu-id="93a56-162">**User defined rate** – After you select this option, you can enter the exchange rate that you want.</span></span> <span data-ttu-id="93a56-163">このオプションは平均為替レートに対して、または固定為替レートと引き換えに連結する場合に役立ちます。</span><span class="sxs-lookup"><span data-stu-id="93a56-163">This option can be useful for average exchange rates or if you're consolidating against a fixed exchange rate.</span></span>

<span data-ttu-id="93a56-164">![為替換算タブ](./media/currency-translation-cons-online.png "為替換算タブ")</span><span class="sxs-lookup"><span data-stu-id="93a56-164">![Currency translation tab](./media/currency-translation-cons-online.png "Currency translation tab")</span></span>

## <a name="additional-resources"></a><span data-ttu-id="93a56-165">追加リソース</span><span class="sxs-lookup"><span data-stu-id="93a56-165">Additional resources</span></span>

<span data-ttu-id="93a56-166">連結および通貨換算の詳細については、このトピックの親トピック、[財務連結および通貨換算の概要](./financial-consolidations-currency-translation.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="93a56-166">For more information about consolidation and currency translations, see the parent topic of this topic, [Financial consolidations and currency translation overview](./financial-consolidations-currency-translation.md).</span></span>

<span data-ttu-id="93a56-167">連結財務諸表を生成するシナリオの詳細については、[連結財務諸表の生成](./generating-consolidated-financial-statements.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="93a56-167">For information about scenarios where you might generate consolidate financial statements, see [Generate consolidated financial statements](./generating-consolidated-financial-statements.md).</span></span>
