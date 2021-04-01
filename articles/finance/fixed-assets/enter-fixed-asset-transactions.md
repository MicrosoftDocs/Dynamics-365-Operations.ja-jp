---
title: 固定資産トランザクションのオプション
description: このトピックは、固定資産トランザクションの作成に使用できるさまざまな方法について説明します。
author: ShylaThompson
manager: AnnBe
ms.date: 02/07/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AssetTable, PurchCreateOrder
audience: Application User
ms.reviewer: roschlom
ms.custom: 23061
ms.assetid: 338c495b-a4d8-461e-b85b-a83faf673730
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: bd1de441cd8c5de9d3684cfe644c33dadb44f5dc
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/15/2021
ms.locfileid: "5241101"
---
# <a name="fixed-asset-transaction-options"></a><span data-ttu-id="5d59c-103">固定資産トランザクションのオプション</span><span class="sxs-lookup"><span data-stu-id="5d59c-103">Fixed asset transaction options</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="5d59c-104">このトピックは、固定資産トランザクションの作成に使用できるさまざまな方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="5d59c-104">This topic describes the different methods available to create fixed asset transactions.</span></span>

<span data-ttu-id="5d59c-105">買掛金勘定、売掛金勘定、調達、および一般会計との統合のために、固定資産を設定できます。</span><span class="sxs-lookup"><span data-stu-id="5d59c-105">You can set up Fixed assets for integration with Accounts payable, Accounts receivable, Procurement and sourcing, and General ledger.</span></span> <span data-ttu-id="5d59c-106">また、これらの項目を内部で使用する場合は、在庫管理の品目を固定資産に転送できます。</span><span class="sxs-lookup"><span data-stu-id="5d59c-106">You can also transfer items in Inventory management to Fixed assets if you want to use those items internally.</span></span>

## <a name="accounts-payable"></a><span data-ttu-id="5d59c-107">買掛金勘定</span><span class="sxs-lookup"><span data-stu-id="5d59c-107">Accounts payable</span></span>
<span data-ttu-id="5d59c-108">[仕訳伝票] ページで固定資産トランザクションを入力できます。</span><span class="sxs-lookup"><span data-stu-id="5d59c-108">You can enter Fixed assets transactions in the Journal voucher page.</span></span> <span data-ttu-id="5d59c-109">このページは、[請求仕訳帳] ページから開くことができます。</span><span class="sxs-lookup"><span data-stu-id="5d59c-109">This page can be opened from the Invoice journal page.</span></span> <span data-ttu-id="5d59c-110">また、[請求書承認仕訳帳] ページから [仕訳伝票] ページを開くことができます。</span><span class="sxs-lookup"><span data-stu-id="5d59c-110">You can also open the Journal voucher page from the Invoice approval journal page.</span></span> <span data-ttu-id="5d59c-111">[相手勘定タイプ] フィールドで、[固定資産] を選択します。</span><span class="sxs-lookup"><span data-stu-id="5d59c-111">In the Offset account type field, select Fixed assets.</span></span> <span data-ttu-id="5d59c-112">そして、[相手勘定] フィールドで固定資産番号を選択します。</span><span class="sxs-lookup"><span data-stu-id="5d59c-112">Then, in the Offset account field, select a fixed asset number.</span></span> <span data-ttu-id="5d59c-113">[固定資産] タブで、[トランザクション タイプ] フィールドと [帳簿] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="5d59c-113">On the Fixed assets tab, enter values in the Transaction type and Book fields.</span></span>

## <a name="accounts-receivable"></a><span data-ttu-id="5d59c-114">売掛金管理</span><span class="sxs-lookup"><span data-stu-id="5d59c-114">Accounts receivable</span></span>
<span data-ttu-id="5d59c-115">[自由書式の請求書] ページで固定資産トランザクションを入力できます。</span><span class="sxs-lookup"><span data-stu-id="5d59c-115">You can enter Fixed assets transactions in the Free text invoice page.</span></span>  <span data-ttu-id="5d59c-116">[自由書式の請求書] ページの [請求明細行] グリッドで明細行品目を選択します。</span><span class="sxs-lookup"><span data-stu-id="5d59c-116">In the Free text invoice page, in the Invoice lines grid, select a line item.</span></span> <span data-ttu-id="5d59c-117">[明細行の詳細] クイック タブをクリックします。</span><span class="sxs-lookup"><span data-stu-id="5d59c-117">Click the Line details FastTab.</span></span> <span data-ttu-id="5d59c-118">処分トランザクションの固定資産番号と帳簿を入力します。</span><span class="sxs-lookup"><span data-stu-id="5d59c-118">Enter the fixed asset number and book for the disposal transaction.</span></span> <span data-ttu-id="5d59c-119">自由書式の請求書の場合、固定資産トランザクション タイプは常に [処分 - 売却] です。</span><span class="sxs-lookup"><span data-stu-id="5d59c-119">For free text invoices, the fixed asset transaction type is always Disposal - sale.</span></span>

## <a name="procurement-and-sourcing"></a><span data-ttu-id="5d59c-120">調達</span><span class="sxs-lookup"><span data-stu-id="5d59c-120">Procurement and sourcing</span></span>
<span data-ttu-id="5d59c-121">[発注書] ページで固定資産トランザクションを入力できます。</span><span class="sxs-lookup"><span data-stu-id="5d59c-121">You can enter Fixed assets transactions in the Purchase order page.</span></span> <span data-ttu-id="5d59c-122">発注書の作成に必要な情報を入力し、[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="5d59c-122">Enter the required information to create a purchase order, and then click OK.</span></span> <span data-ttu-id="5d59c-123">[発注書] ページで、[明細行の詳細] クイックタブをクリックします。</span><span class="sxs-lookup"><span data-stu-id="5d59c-123">In the Purchase order page, click the Line details FastTab.</span></span> <span data-ttu-id="5d59c-124">その後、[固定資産] タブで、固定資産に関する情報を入力します。</span><span class="sxs-lookup"><span data-stu-id="5d59c-124">Then, on the Fixed assets tab, enter information about the fixed asset.</span></span> 

<span data-ttu-id="5d59c-125">既存の固定資産の取得トランザクションを転記するには、固定資産番号、帳簿とトランザクション タイプを指定します。</span><span class="sxs-lookup"><span data-stu-id="5d59c-125">To post an acquisition transaction for an existing fixed asset, specify the fixed asset number, book, and transaction type.</span></span> <span data-ttu-id="5d59c-126">この情報のいずれかが見つからない場合、固定資産は転記できません。</span><span class="sxs-lookup"><span data-stu-id="5d59c-126">The fixed asset cannot be posted if any of this information is missing.</span></span> <span data-ttu-id="5d59c-127">新しい固定資産の取得トランザクションを転記するには、[新しい固定資産?] オプションを選択し、新しい資産を割り当てる固定資産グループを選択します。</span><span class="sxs-lookup"><span data-stu-id="5d59c-127">To post an acquisition transaction for a new fixed asset, select the New fixed asset? option, and then select the fixed asset group to assign the new asset to.</span></span> <span data-ttu-id="5d59c-128">ただし、品目が標準原価在庫モデルを使用する在庫モデル グループにある場合、明細行に対して使用できる固定資産フィールドは存在しません。</span><span class="sxs-lookup"><span data-stu-id="5d59c-128">However, no fixed asset fields are available for a line if the item is in an inventory model group that uses a standard cost inventory model.</span></span> <span data-ttu-id="5d59c-129">また、 [固定資産パラメーター] ページで定義されるオプションにより、購買モジュールから取得トランザクションを転記できるかどうかが決まります。</span><span class="sxs-lookup"><span data-stu-id="5d59c-129">Additionally, the options that are defined in the Fixed assets parameters page determine whether you can post acquisition transactions from the purchasing modules.</span></span> 

<span data-ttu-id="5d59c-130">固定資産の取得に発注書または固定資産の在庫仕訳帳を使用すると、在庫金額に影響が出ます。</span><span class="sxs-lookup"><span data-stu-id="5d59c-130">When a purchase order or the Inventory to fixed assets journal is used to acquire fixed assets, the inventory value is affected.</span></span>

## <a name="general-ledger"></a><span data-ttu-id="5d59c-131">総勘定元帳</span><span class="sxs-lookup"><span data-stu-id="5d59c-131">General ledger</span></span>
<span data-ttu-id="5d59c-132">すべての固定資産トランザクション タイプは [一般仕訳帳] ページで転記できます。</span><span class="sxs-lookup"><span data-stu-id="5d59c-132">Any fixed asset transaction type can be posted in the General journal page.</span></span> <span data-ttu-id="5d59c-133">また、固定資産の仕訳帳を使用して、固定資産トランザクションを転記できます。</span><span class="sxs-lookup"><span data-stu-id="5d59c-133">You can also use journals in Fixed assets to post fixed asset transactions.</span></span>

## <a name="options-for-entering-fixed-asset-transaction-types"></a><span data-ttu-id="5d59c-134">固定資産トランザクション タイプの入力のためのオプション</span><span class="sxs-lookup"><span data-stu-id="5d59c-134">Options for entering fixed asset transaction types</span></span>


| <span data-ttu-id="5d59c-135">トランザクション タイプ</span><span class="sxs-lookup"><span data-stu-id="5d59c-135">Transaction type</span></span>                    | <span data-ttu-id="5d59c-136">モジュール</span><span class="sxs-lookup"><span data-stu-id="5d59c-136">Module</span></span>                   | <span data-ttu-id="5d59c-137">オプション</span><span class="sxs-lookup"><span data-stu-id="5d59c-137">Options</span></span>                                   |
|-------------------------------------|--------------------------|-------------------------------------------|
| <span data-ttu-id="5d59c-138">取得、取得調整</span><span class="sxs-lookup"><span data-stu-id="5d59c-138">Acquisition, Acquisition adjustment</span></span> | <span data-ttu-id="5d59c-139">固定資産</span><span class="sxs-lookup"><span data-stu-id="5d59c-139">Fixed assets</span></span>             | <span data-ttu-id="5d59c-140">固定資産、在庫の固定資産化</span><span class="sxs-lookup"><span data-stu-id="5d59c-140">Fixed assets, Inventory to fixed assets</span></span>   |
|                                     | <span data-ttu-id="5d59c-141">総勘定元帳</span><span class="sxs-lookup"><span data-stu-id="5d59c-141">General ledger</span></span>           | <span data-ttu-id="5d59c-142">一般仕訳帳</span><span class="sxs-lookup"><span data-stu-id="5d59c-142">General journal</span></span>                           |
|                                     | <span data-ttu-id="5d59c-143">買掛金勘定</span><span class="sxs-lookup"><span data-stu-id="5d59c-143">Accounts payable</span></span>         | <span data-ttu-id="5d59c-144">請求仕訳帳、請求書承認仕訳帳</span><span class="sxs-lookup"><span data-stu-id="5d59c-144">Invoice journal, Invoice approval journal</span></span> |
|                                     | <span data-ttu-id="5d59c-145">調達</span><span class="sxs-lookup"><span data-stu-id="5d59c-145">Procurement and sourcing</span></span> | <span data-ttu-id="5d59c-146">発注書</span><span class="sxs-lookup"><span data-stu-id="5d59c-146">Purchase order</span></span>                            |
| <span data-ttu-id="5d59c-147">減価償却</span><span class="sxs-lookup"><span data-stu-id="5d59c-147">Depreciation</span></span>                        | <span data-ttu-id="5d59c-148">固定資産</span><span class="sxs-lookup"><span data-stu-id="5d59c-148">Fixed assets</span></span>             | <span data-ttu-id="5d59c-149">固定資産</span><span class="sxs-lookup"><span data-stu-id="5d59c-149">Fixed assets</span></span>                              |
|                                     | <span data-ttu-id="5d59c-150">一般会計</span><span class="sxs-lookup"><span data-stu-id="5d59c-150">General ledger</span></span>           | <span data-ttu-id="5d59c-151">一般仕訳帳</span><span class="sxs-lookup"><span data-stu-id="5d59c-151">General journal</span></span>                           |
| <span data-ttu-id="5d59c-152">処分</span><span class="sxs-lookup"><span data-stu-id="5d59c-152">Disposal</span></span>                            | <span data-ttu-id="5d59c-153">固定資産</span><span class="sxs-lookup"><span data-stu-id="5d59c-153">Fixed assets</span></span>             | <span data-ttu-id="5d59c-154">固定資産</span><span class="sxs-lookup"><span data-stu-id="5d59c-154">Fixed assets</span></span>                              |
| <span data-ttu-id="5d59c-155">\*\* \*\*</span><span class="sxs-lookup"><span data-stu-id="5d59c-155">\*\* \*\*</span></span>                               | <span data-ttu-id="5d59c-156">一般会計</span><span class="sxs-lookup"><span data-stu-id="5d59c-156">General ledger</span></span>           | <span data-ttu-id="5d59c-157">一般仕訳帳</span><span class="sxs-lookup"><span data-stu-id="5d59c-157">General journal</span></span>                           |
| <span data-ttu-id="5d59c-158">\*\* \*\*</span><span class="sxs-lookup"><span data-stu-id="5d59c-158">\*\* \*\*</span></span>                               | <span data-ttu-id="5d59c-159">売掛金管理</span><span class="sxs-lookup"><span data-stu-id="5d59c-159">Accounts receivable</span></span>      | <span data-ttu-id="5d59c-160">自由書式の請求書</span><span class="sxs-lookup"><span data-stu-id="5d59c-160">Free text invoice</span></span>                         |


<span data-ttu-id="5d59c-161">減価償却トランザクション タイプの仕訳帳明細行がデータ エンティティを通じて手動で作成またはインポートされた場合、固定資産の減価償却期間の残存価額は更新されません。</span><span class="sxs-lookup"><span data-stu-id="5d59c-161">The Depreciation periods remaining value of the fixed asset is not updated when a depreciation transaction type journal line is manually created or imported through a data entity.</span></span> <span data-ttu-id="5d59c-162">この値は、減価償却提案プロセスを使用して仕訳帳明細行を作成したときに更新されます。</span><span class="sxs-lookup"><span data-stu-id="5d59c-162">This value is updated when the depreciation proposal process is used to create the journal line.</span></span>

<span data-ttu-id="5d59c-163">詳細については、「[固定資産の統合](fixed-asset-integration.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="5d59c-163">For more information, see [Fixed assets integration](fixed-asset-integration.md).</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]