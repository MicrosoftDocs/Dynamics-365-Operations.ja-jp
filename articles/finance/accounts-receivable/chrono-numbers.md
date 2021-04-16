---
title: ドキュメントや伝票に時系列に採番する
description: このトピックでは、ドキュメントや伝票への時系列の採番方法および使用方法について説明します。
author: ikond
ms.date: 02/01/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: NumberSequenceGroup
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 401195
ms.search.region: Global
ms.author: ilyako
ms.search.validFrom: 2021-03-15
ms.dyn365.ops.version: 10.0.17
ms.openlocfilehash: fe533052b0e5b04a7d27b954ba644761c631d6d7
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/01/2021
ms.locfileid: "5838864"
---
# <a name="numbering-documents-and-vouchers-chronologically"></a><span data-ttu-id="eaa33-103">ドキュメントや伝票に時系列に採番する</span><span class="sxs-lookup"><span data-stu-id="eaa33-103">Numbering documents and vouchers chronologically</span></span>

[!include [banner](../includes/banner.md)]


<span data-ttu-id="eaa33-104">一部の国では、ドキュメントや関連する伝票に時系列で採番することが法的に義務付けられています。</span><span class="sxs-lookup"><span data-stu-id="eaa33-104">In some countries, there is a legal requirement to number documents and related vouchers in chronological order.</span></span> <span data-ttu-id="eaa33-105">時系列は期間に対応している必要があります。</span><span class="sxs-lookup"><span data-stu-id="eaa33-105">The chronology must be supported by periods.</span></span> <span data-ttu-id="eaa33-106">古い期間に属する数字はすべて、それよりも新しい期間に属する数字よりも小さくなければなりません。</span><span class="sxs-lookup"><span data-stu-id="eaa33-106">All of the numbers that belong to earlier periods must be less than the numbers that belong to later periods.</span></span> <span data-ttu-id="eaa33-107">この要件を満たす目的で、時系列の採番機能が実装されています。</span><span class="sxs-lookup"><span data-stu-id="eaa33-107">To meet this requirement, chronological numbering functionality has been implemented.</span></span> <span data-ttu-id="eaa33-108">このトピックでは、ドキュメントや伝票への時系列の採番を構成する方法および使用方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="eaa33-108">This topic explains how to configure and use chronological numbers for applicable documents and related vouchers.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="eaa33-109">必要条件</span><span class="sxs-lookup"><span data-stu-id="eaa33-109">Prerequisites</span></span>

<span data-ttu-id="eaa33-110">機能管理ワークスペースで、**時系列採番** を有効にします。</span><span class="sxs-lookup"><span data-stu-id="eaa33-110">In the Feature management workspace, turn on the **Chronological numbering** feature.</span></span> <span data-ttu-id="eaa33-111">詳細については [機能管理の概要](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="eaa33-111">For more information, see [Feature management overview](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).</span></span>

## <a name="configure-chronological-numbering"></a><span data-ttu-id="eaa33-112">時系列採番の構成</span><span class="sxs-lookup"><span data-stu-id="eaa33-112">Configure chronological numbering</span></span>

<span data-ttu-id="eaa33-113">時系列の採番は次のドキュメントに影響します。</span><span class="sxs-lookup"><span data-stu-id="eaa33-113">Chronological numbering affects the following documents.</span></span>

<span data-ttu-id="eaa33-114">**売掛金勘定**</span><span class="sxs-lookup"><span data-stu-id="eaa33-114">**Accounts receivable**</span></span>
- <span data-ttu-id="eaa33-115">顧客請求書</span><span class="sxs-lookup"><span data-stu-id="eaa33-115">Customer invoice</span></span>
- <span data-ttu-id="eaa33-116">顧客請求書伝票</span><span class="sxs-lookup"><span data-stu-id="eaa33-116">Customer invoice voucher</span></span>
- <span data-ttu-id="eaa33-117">売上訂正票</span><span class="sxs-lookup"><span data-stu-id="eaa33-117">Sales credit note</span></span>
- <span data-ttu-id="eaa33-118">売上貸方伝票</span><span class="sxs-lookup"><span data-stu-id="eaa33-118">Sales credit note voucher</span></span>
- <span data-ttu-id="eaa33-119">自由書式の請求書</span><span class="sxs-lookup"><span data-stu-id="eaa33-119">Free text invoice</span></span>
- <span data-ttu-id="eaa33-120">自由書式の請求伝票</span><span class="sxs-lookup"><span data-stu-id="eaa33-120">Free text invoice voucher</span></span>
- <span data-ttu-id="eaa33-121">自由書式の訂正票</span><span class="sxs-lookup"><span data-stu-id="eaa33-121">Free text credit note</span></span>
- <span data-ttu-id="eaa33-122">自由書式の貸方伝票</span><span class="sxs-lookup"><span data-stu-id="eaa33-122">Free text credit note voucher</span></span>
- <span data-ttu-id="eaa33-123">梱包明細</span><span class="sxs-lookup"><span data-stu-id="eaa33-123">Packing slip</span></span>
- <span data-ttu-id="eaa33-124">梱包明細伝票</span><span class="sxs-lookup"><span data-stu-id="eaa33-124">Packing slip voucher</span></span>
- <span data-ttu-id="eaa33-125">梱包明細の修正伝票</span><span class="sxs-lookup"><span data-stu-id="eaa33-125">Packing slip correction voucher</span></span>
- <span data-ttu-id="eaa33-126">利子計算書伝票</span><span class="sxs-lookup"><span data-stu-id="eaa33-126">Interest note voucher</span></span>
- <span data-ttu-id="eaa33-127">督促状伝票</span><span class="sxs-lookup"><span data-stu-id="eaa33-127">Collection letter voucher</span></span>

<span data-ttu-id="eaa33-128">**買掛金勘定**</span><span class="sxs-lookup"><span data-stu-id="eaa33-128">**Accounts payable**</span></span>
- <span data-ttu-id="eaa33-129">請求伝票</span><span class="sxs-lookup"><span data-stu-id="eaa33-129">Invoice voucher</span></span>
- <span data-ttu-id="eaa33-130">貸方伝票</span><span class="sxs-lookup"><span data-stu-id="eaa33-130">Credit note voucher</span></span>
- <span data-ttu-id="eaa33-131">製品受領伝票</span><span class="sxs-lookup"><span data-stu-id="eaa33-131">Product receipt voucher</span></span>

<span data-ttu-id="eaa33-132">**プロジェクト管理**</span><span class="sxs-lookup"><span data-stu-id="eaa33-132">**Project management**</span></span>
- <span data-ttu-id="eaa33-133">請求書</span><span class="sxs-lookup"><span data-stu-id="eaa33-133">Invoice</span></span>
- <span data-ttu-id="eaa33-134">請求伝票</span><span class="sxs-lookup"><span data-stu-id="eaa33-134">Invoice voucher</span></span>
- <span data-ttu-id="eaa33-135">訂正票</span><span class="sxs-lookup"><span data-stu-id="eaa33-135">Credit note</span></span>
- <span data-ttu-id="eaa33-136">貸方伝票</span><span class="sxs-lookup"><span data-stu-id="eaa33-136">Credit note voucher</span></span> 

### <a name="define-number-sequences"></a><span data-ttu-id="eaa33-137">番号順序の定義</span><span class="sxs-lookup"><span data-stu-id="eaa33-137">Define number sequences</span></span>

<span data-ttu-id="eaa33-138">番号順序を定義するには、**組織管理の 番号順序** > **番号順序** > **番号順序** に移動します。</span><span class="sxs-lookup"><span data-stu-id="eaa33-138">To define number sequences, go to **Organization administration** > **Number sequences** > **Number sequences**.</span></span> <span data-ttu-id="eaa33-139">必要なドキュメントの影響を受ける期間に対応できるよう、必要な数の番号順序を定義できます。</span><span class="sxs-lookup"><span data-stu-id="eaa33-139">You can define as many number sequences as required to cover the affected periods for required documents.</span></span> 

<span data-ttu-id="eaa33-140">番号順序ごとに会社を指定します。</span><span class="sxs-lookup"><span data-stu-id="eaa33-140">Specify a company for each number sequence.</span></span> <span data-ttu-id="eaa33-141">番号順序の区分は、期間の時系列順を示すように定義する必要があります。</span><span class="sxs-lookup"><span data-stu-id="eaa33-141">The segments of the number sequences must be defined so that they provide chronological order for periods.</span></span> <span data-ttu-id="eaa33-142">たとえば、区分名に特定の期間を識別する特別な接頭語を含めることができます。</span><span class="sxs-lookup"><span data-stu-id="eaa33-142">For example, the segment names can contain a special prefix that identifies a specific period.</span></span>

![番号順序の設定](media/chrono-num-sequence.jpg)

### <a name="configure-number-sequence-groups"></a><span data-ttu-id="eaa33-144">番号順序のグループを構成する</span><span class="sxs-lookup"><span data-stu-id="eaa33-144">Configure number sequence groups</span></span>

<span data-ttu-id="eaa33-145">番号順序のグループを構成するには、 **売掛金** > **設定** > **売掛金パラメータ** に移動します。</span><span class="sxs-lookup"><span data-stu-id="eaa33-145">To configure number sequence groups, go to **Accounts receivable** > **Setup** > **Accounts receivable parameters**.</span></span> <span data-ttu-id="eaa33-146">**番号順序** タブで、影響を受ける期間への対応に必要となる数の番号順序グループを定義します。</span><span class="sxs-lookup"><span data-stu-id="eaa33-146">On the **Number sequences** tab, define as many number sequences groups as required to cover the affected periods.</span></span> 

<span data-ttu-id="eaa33-147">それぞれのグループの **参照** セクションで、サポートされているドキュメント参照のいずれかを選択し、**番号順序コード** フィールドで、関連する期間に対して以前に作成された番号順序を参照します。</span><span class="sxs-lookup"><span data-stu-id="eaa33-147">For each group, in the **Reference** section, select one of the supported document references, and in the **Number sequence code** field, refer to a number sequence that was previously created for the related period.</span></span>

![番号順序グループの設定](media/chrono-num-sequence-group.jpg)

<span data-ttu-id="eaa33-149">同様に、**売掛金** と **プロジェクト管理と会計** モジュールで、番号順序グループを構成します。</span><span class="sxs-lookup"><span data-stu-id="eaa33-149">Similarly, configure number sequence groups in **Accounts payable** and **Project management and accounting** modules.</span></span>

### <a name="configure-number-sequence-groups-chronology"></a><span data-ttu-id="eaa33-150">番号順序のグループの時系列を構成する</span><span class="sxs-lookup"><span data-stu-id="eaa33-150">Configure number sequence groups chronology</span></span>

<span data-ttu-id="eaa33-151">番号順序グループの時系列を構成するには、**組織管理** > **番号順序** > **時系列番号順序グループ** に移動します。</span><span class="sxs-lookup"><span data-stu-id="eaa33-151">To configure number sequence groups chronology, go to **Organization administration** > **Number sequences** > **Chronological number sequence groups**.</span></span> <span data-ttu-id="eaa33-152">番号順序グループに使用する適用条件を定義します。</span><span class="sxs-lookup"><span data-stu-id="eaa33-152">Define the applicability conditions for number sequence groups.</span></span>

![時系列番号の設定](media/chrono-num-sequence-group-period.jpg)

| <span data-ttu-id="eaa33-154">フィールド</span><span class="sxs-lookup"><span data-stu-id="eaa33-154">Field</span></span>            | <span data-ttu-id="eaa33-155">説明</span><span class="sxs-lookup"><span data-stu-id="eaa33-155">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                   |
|---------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="eaa33-156">開始</span><span class="sxs-lookup"><span data-stu-id="eaa33-156">Effective</span></span>  | <span data-ttu-id="eaa33-157">番号順序グループへの適用開始日です。</span><span class="sxs-lookup"><span data-stu-id="eaa33-157">The start date of number sequence group applicability.</span></span> |
| <span data-ttu-id="eaa33-158">終了</span><span class="sxs-lookup"><span data-stu-id="eaa33-158">Expiration</span></span>      | <span data-ttu-id="eaa33-159">番号順序グループへの適用終了日です。</span><span class="sxs-lookup"><span data-stu-id="eaa33-159">The end date of number sequence group applicability.</span></span> <span data-ttu-id="eaa33-160">終了日を設定しない場合は、**なし** を選択します。</span><span class="sxs-lookup"><span data-stu-id="eaa33-160">If no end date is applied, select **Never**.</span></span> |
| <span data-ttu-id="eaa33-161">番号順序グループ</span><span class="sxs-lookup"><span data-stu-id="eaa33-161">Number sequence group</span></span> | <span data-ttu-id="eaa33-162">期間中にドキュメント番号の生成に使用する番号順序グループです。</span><span class="sxs-lookup"><span data-stu-id="eaa33-162">Number sequence group that will be used to generate document numbers during the period.</span></span> |
| <span data-ttu-id="eaa33-163">元の番号順序グループ</span><span class="sxs-lookup"><span data-stu-id="eaa33-163">Original number sequence group</span></span> | <span data-ttu-id="eaa33-164">この番号順序グループのコードは、ドキュメントに特定の *固定* 番号順序グループが既に割り当てられている場合、追加のフィルター処理に使用されます。</span><span class="sxs-lookup"><span data-stu-id="eaa33-164">This number sequence group code is used for additional filtering for the cases when documents already have a specific *permanent* number sequence group assigned.</span></span> <span data-ttu-id="eaa33-165">空の値は空の値と見なされます。</span><span class="sxs-lookup"><span data-stu-id="eaa33-165">An empty value is considered a specific value.</span></span> <span data-ttu-id="eaa33-166">予備割り当てグループを無視する場合は、この設定の **既定** のオプションを使用します。</span><span class="sxs-lookup"><span data-stu-id="eaa33-166">If you need to ignore a preliminary assigned group, use the **Default** option for this setup.</span></span> |
| <span data-ttu-id="eaa33-167">既定</span><span class="sxs-lookup"><span data-stu-id="eaa33-167">Default</span></span> | <span data-ttu-id="eaa33-168">有効な場合、予備的に割り当てられたドキュメント番号の順序グループを無視し、期間の開始日と終了日のみを適用分析に使用します。</span><span class="sxs-lookup"><span data-stu-id="eaa33-168">If turned on, the system ignores the preliminary assigned document number sequence group and uses only the periods start and end dates for applicability analysis.</span></span> <span data-ttu-id="eaa33-169">無効にすると、完全な組み合わせの **有効** + **期限** + **オリジナル番号の順序グループ** を選択に使用します。</span><span class="sxs-lookup"><span data-stu-id="eaa33-169">If turned off, the system uses the full combination **Effective** + **Expiration** + **Original number sequence group** for selection.</span></span> |

## <a name="document-posting"></a><span data-ttu-id="eaa33-170">ドキュメントの転記</span><span class="sxs-lookup"><span data-stu-id="eaa33-170">Document posting</span></span>
<span data-ttu-id="eaa33-171">ドキュメントを転記すると、ドキュメントを転記した日に基づいて適切な番号順序グループがドキュメントに割り当てられ、検出された番号順序に基づいてドキュメント番号を生成します。</span><span class="sxs-lookup"><span data-stu-id="eaa33-171">When you post a document, the appropriate number sequence group is assigned to the document, based on document's posting date, and then used to generate a document number based on the detected number sequence.</span></span> <span data-ttu-id="eaa33-172">番号順序グループの割り当てに関するメッセージが表示されます。</span><span class="sxs-lookup"><span data-stu-id="eaa33-172">The system provides a message regarding the number sequence group assignment.</span></span>

![ドキュメント番号](media/chrono-num-sequence-fti.jpg)

> [!NOTE]
> <span data-ttu-id="eaa33-174">一部の国では、ドキュメントの番号付けに対して既に特定のロジックが実装されています。</span><span class="sxs-lookup"><span data-stu-id="eaa33-174">For some countries, there is a specific logic already implemented for document numbering.</span></span> <span data-ttu-id="eaa33-175">この場合、国固有のロジックは、**時系列番号付け** 機能よりも優先されます。</span><span class="sxs-lookup"><span data-stu-id="eaa33-175">In this case, country-specific logic will override the **Chronological numbering** feature.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
