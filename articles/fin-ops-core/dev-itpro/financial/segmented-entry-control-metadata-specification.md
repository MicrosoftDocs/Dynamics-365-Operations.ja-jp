---
title: セグメント化されたエントリ コントロールのためのデザイン時メタデータ
description: セグメント化エントリ コントロールのデザイン時メタデータ プロパティについて説明します。
author: robinarh
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Developer
ms.reviewer: rhaertle
ms.custom: 25591
ms.assetid: b8c5d7a4-ee2b-4ab1-b042-88472b97f035
ms.search.region: Global
ms.author: ghenriks
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: e39cad1bda1b757dcd3d45ada48453df4431c750
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/31/2021
ms.locfileid: "5750958"
---
# <a name="design-time-metadata-for-segmented-entry-controls"></a><span data-ttu-id="06014-103">セグメント化されたエントリ コントロールのためのデザイン時メタデータ</span><span class="sxs-lookup"><span data-stu-id="06014-103">Design-time metadata for Segmented Entry controls</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="06014-104">セグメント化エントリ コントロールのデザイン時メタデータ プロパティについて説明します。</span><span class="sxs-lookup"><span data-stu-id="06014-104">Describes the design-time metadata properties for Segmented Entry controls.</span></span>

<span data-ttu-id="06014-105">セグメント化エントリ コントロールのカスタム プロパティは、コントローラー グループの下にあります。</span><span class="sxs-lookup"><span data-stu-id="06014-105">The custom properties for the Segmented Entry control are found under the Controller group.</span></span> <span data-ttu-id="06014-106">次に例を示します。</span><span class="sxs-lookup"><span data-stu-id="06014-106">Here is an example.</span></span>

<span data-ttu-id="06014-107">[![SEC プロパティ シート例](./media/10.jpg)](./media/10.jpg)</span><span class="sxs-lookup"><span data-stu-id="06014-107">[![SEC Property Sheet Example](./media/10.jpg)](./media/10.jpg)</span></span>

<span data-ttu-id="06014-108">一部のプロパティは、選択されたコントローラ クラスに基づいて編集できない場合があります。</span><span class="sxs-lookup"><span data-stu-id="06014-108">Certain properties may be non-editable based on the Controller class that is selected.</span></span> <span data-ttu-id="06014-109">これは、特定のプロパティのみがさまざまなコントローラー クラスのそれぞれに関連するためです。</span><span class="sxs-lookup"><span data-stu-id="06014-109">This is because only certain properties are relevant for each of the various controller classes.</span></span>  <span data-ttu-id="06014-110">詳細については、[有効なプロパティ](#valid-properties) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="06014-110">For more information, see [Valid properties](#valid-properties).</span></span>

## <a name="property-details"></a><span data-ttu-id="06014-111">プロパティの詳細</span><span class="sxs-lookup"><span data-stu-id="06014-111">Property details</span></span>

| <span data-ttu-id="06014-112">プロパティ</span><span class="sxs-lookup"><span data-stu-id="06014-112">Property</span></span> | <span data-ttu-id="06014-113">有効な値</span><span class="sxs-lookup"><span data-stu-id="06014-113">Valid values</span></span>   | <span data-ttu-id="06014-114">用途</span><span class="sxs-lookup"><span data-stu-id="06014-114">Usage</span></span>            |
|----------------|--------------------------|------------------------------------|
| <span data-ttu-id="06014-115">勘定タイプ フィールド</span><span class="sxs-lookup"><span data-stu-id="06014-115">Account Type Field</span></span>                | <span data-ttu-id="06014-116">データ ソースからのフィールド。</span><span class="sxs-lookup"><span data-stu-id="06014-116">A field from the data source.</span></span>                                                      | <span data-ttu-id="06014-117">使用されるアカウントの種類を決定します。</span><span class="sxs-lookup"><span data-stu-id="06014-117">Determines the type of account used.</span></span> <span data-ttu-id="06014-118">通常、複数セグメントの勘定科目から、Cust、Vend、Bank、Project などの他のバッキング テーブルの単一セグメント値への仕訳入力に使用します。</span><span class="sxs-lookup"><span data-stu-id="06014-118">Typically used for journal entry from a multi-segment ledger account to single segment values from other backing tables, such as Cust, Vend, Bank, Project, and similar.</span></span> |
| <span data-ttu-id="06014-119">コントローラー クラス</span><span class="sxs-lookup"><span data-stu-id="06014-119">Controller Class</span></span>                  | <span data-ttu-id="06014-120">7 つのコントローラー クラスのうちの 1 つです。</span><span class="sxs-lookup"><span data-stu-id="06014-120">One of 7 Controller classes.</span></span> <span data-ttu-id="06014-121">たとえば LedgerDimensionDefaultAccountController です。</span><span class="sxs-lookup"><span data-stu-id="06014-121">For example, LedgerDimensionDefaultAccountController.</span></span> | <span data-ttu-id="06014-122">セグメント化されたエントリ コントロールの動作およびパターンを決定します。</span><span class="sxs-lookup"><span data-stu-id="06014-122">Determines the pattern and behavior of the Segmented Entry control.</span></span>                                                                                                                                          |
| <span data-ttu-id="06014-123">財務勘定を含む</span><span class="sxs-lookup"><span data-stu-id="06014-123">Include Financial Accounts</span></span>        | <span data-ttu-id="06014-124">NoYes</span><span class="sxs-lookup"><span data-stu-id="06014-124">NoYes</span></span>                                                                             | <span data-ttu-id="06014-125">財務勘定である主勘定が有効であるかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="06014-125">Determines if Main accounts that are Financial accounts are valid for use.</span></span>                                                                                                                                   |
| <span data-ttu-id="06014-126">勘定合計を含む</span><span class="sxs-lookup"><span data-stu-id="06014-126">Include Total Accounts</span></span>            | <span data-ttu-id="06014-127">NoYes</span><span class="sxs-lookup"><span data-stu-id="06014-127">NoYes</span></span>                                                                             | <span data-ttu-id="06014-128">タイプが "合計" の主勘定が有効であるかどうかを判断します。</span><span class="sxs-lookup"><span data-stu-id="06014-128">Determines if Main accounts of type Total are valid for use.</span></span>                                                                                                                                                 |
| <span data-ttu-id="06014-129">既定の勘定です。</span><span class="sxs-lookup"><span data-stu-id="06014-129">Is Default Account</span></span>                | <span data-ttu-id="06014-130">TrueFalse</span><span class="sxs-lookup"><span data-stu-id="06014-130">TrueFalse</span></span>                                                                         | <span data-ttu-id="06014-131">動的アカウントで、アカウントが既定または完全アカウントであるべきかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="06014-131">For a Dynamic account, determines if the account should be a default or full account.</span></span>                                                                                                                        |
| <span data-ttu-id="06014-132">主勘定セグメントのロック</span><span class="sxs-lookup"><span data-stu-id="06014-132">Lock Main Account Segment</span></span>         | <span data-ttu-id="06014-133">NoYes</span><span class="sxs-lookup"><span data-stu-id="06014-133">NoYes</span></span>                                                                             | <span data-ttu-id="06014-134">主勘定セグメントがロックされているかどうかをコントロールします。</span><span class="sxs-lookup"><span data-stu-id="06014-134">Controls whether the Main account segment is locked.</span></span>  <span data-ttu-id="06014-135">通常は仕訳帳や構成に基づく配分に使用されます。</span><span class="sxs-lookup"><span data-stu-id="06014-135">Typically used in journals and distributions based on configuration.</span></span>                                                                                   |
| <span data-ttu-id="06014-136">転記タイプ</span><span class="sxs-lookup"><span data-stu-id="06014-136">Posting Type</span></span>                      | <span data-ttu-id="06014-137">LedgerPostingType 列挙の値。</span><span class="sxs-lookup"><span data-stu-id="06014-137">A value from the LedgerPostingType enumeration.</span></span>                                   | <span data-ttu-id="06014-138">主勘定が検証され、そのアカウントで転記タイプを使用できるかどうかが確認されます。</span><span class="sxs-lookup"><span data-stu-id="06014-138">The Main account is validated to see if the posting type can be with that account.</span></span>                                                                                                            |
| <span data-ttu-id="06014-139">手動入力のブロック状態の検証</span><span class="sxs-lookup"><span data-stu-id="06014-139">Validate Blocked For Manual Entry</span></span> | <span data-ttu-id="06014-140">NoYes</span><span class="sxs-lookup"><span data-stu-id="06014-140">NoYes</span></span>                                                                             | <span data-ttu-id="06014-141">分析コードの「手動入力のブロック」ステータスを優先するかを決定します。</span><span class="sxs-lookup"><span data-stu-id="06014-141">Determines if the 'Blocked for Manual Entry' status on the dimension should be respected.</span></span>                                                                                                                    |

## <a name="valid-properties"></a><span data-ttu-id="06014-142">有効なプロパティ</span><span class="sxs-lookup"><span data-stu-id="06014-142">Valid properties</span></span>

<span data-ttu-id="06014-143">次のセクションでは、各コントローラー タイプに対して有効なプロパティを示します。</span><span class="sxs-lookup"><span data-stu-id="06014-143">The following sections show which properties are valid for each Controller type.</span></span>

### <a name="validate-blocked-for-manual-entry"></a><span data-ttu-id="06014-144">手動入力のブロック状態の検証</span><span class="sxs-lookup"><span data-stu-id="06014-144">Validate Blocked For Manual Entry</span></span>

<span data-ttu-id="06014-145">BudgetLedgerDimension: はい</span><span class="sxs-lookup"><span data-stu-id="06014-145">BudgetLedgerDimension: Yes</span></span>

<span data-ttu-id="06014-146">BudgetPlanningLedgerDimension: はい</span><span class="sxs-lookup"><span data-stu-id="06014-146">BudgetPlanningLedgerDimension: Yes</span></span>

<span data-ttu-id="06014-147">DimensionDynamicAccount: Yes</span><span class="sxs-lookup"><span data-stu-id="06014-147">DimensionDynamicAccount: Yes</span></span>

<span data-ttu-id="06014-148">LedgerDimensionAccount: はい</span><span class="sxs-lookup"><span data-stu-id="06014-148">LedgerDimensionAccount: Yes</span></span>

<span data-ttu-id="06014-149">LedgerDimensionDefaultAccount: はい</span><span class="sxs-lookup"><span data-stu-id="06014-149">LedgerDimensionDefaultAccount: Yes</span></span>

<span data-ttu-id="06014-150">LedgerDimensionAccountAlias: はい</span><span class="sxs-lookup"><span data-stu-id="06014-150">LedgerDimensionAccountAlias: Yes</span></span>

### <a name="account-type-field"></a><span data-ttu-id="06014-151">勘定タイプ フィールド</span><span class="sxs-lookup"><span data-stu-id="06014-151">Account Type Field</span></span>

<span data-ttu-id="06014-152">BudgetLedgerDimension: いいえ</span><span class="sxs-lookup"><span data-stu-id="06014-152">BudgetLedgerDimension: No</span></span>

<span data-ttu-id="06014-153">BudgetPlanningLedgerDimension: いいえ</span><span class="sxs-lookup"><span data-stu-id="06014-153">BudgetPlanningLedgerDimension: No</span></span>

<span data-ttu-id="06014-154">DimensionDynamicAccount: Yes</span><span class="sxs-lookup"><span data-stu-id="06014-154">DimensionDynamicAccount: Yes</span></span>

<span data-ttu-id="06014-155">LedgerDimensionAccount: いいえ</span><span class="sxs-lookup"><span data-stu-id="06014-155">LedgerDimensionAccount: No</span></span>

<span data-ttu-id="06014-156">LedgerDimensionDefaultAccount: いいえ</span><span class="sxs-lookup"><span data-stu-id="06014-156">LedgerDimensionDefaultAccount: No</span></span>

<span data-ttu-id="06014-157">LedgerDimensionAccountAlias: いいえ</span><span class="sxs-lookup"><span data-stu-id="06014-157">LedgerDimensionAccountAlias: No</span></span>

### <a name="is-default-account"></a><span data-ttu-id="06014-158">既定の勘定です。</span><span class="sxs-lookup"><span data-stu-id="06014-158">Is Default Account</span></span>

<span data-ttu-id="06014-159">BudgetLedgerDimension: いいえ</span><span class="sxs-lookup"><span data-stu-id="06014-159">BudgetLedgerDimension: No</span></span>

<span data-ttu-id="06014-160">BudgetPlanningLedgerDimension: いいえ</span><span class="sxs-lookup"><span data-stu-id="06014-160">BudgetPlanningLedgerDimension: No</span></span>

<span data-ttu-id="06014-161">DimensionDynamicAccount: Yes</span><span class="sxs-lookup"><span data-stu-id="06014-161">DimensionDynamicAccount: Yes</span></span>

<span data-ttu-id="06014-162">LedgerDimensionAccount: いいえ</span><span class="sxs-lookup"><span data-stu-id="06014-162">LedgerDimensionAccount: No</span></span>

<span data-ttu-id="06014-163">LedgerDimensionDefaultAccount: いいえ</span><span class="sxs-lookup"><span data-stu-id="06014-163">LedgerDimensionDefaultAccount: No</span></span>

<span data-ttu-id="06014-164">LedgerDimensionAccountAlias: いいえ</span><span class="sxs-lookup"><span data-stu-id="06014-164">LedgerDimensionAccountAlias: No</span></span>

### <a name="lock-main-account-segment"></a><span data-ttu-id="06014-165">主勘定セグメントのロック</span><span class="sxs-lookup"><span data-stu-id="06014-165">Lock Main Account Segment</span></span>

<span data-ttu-id="06014-166">BudgetLedgerDimension: いいえ</span><span class="sxs-lookup"><span data-stu-id="06014-166">BudgetLedgerDimension: No</span></span>

<span data-ttu-id="06014-167">BudgetPlanningLedgerDimension: はい</span><span class="sxs-lookup"><span data-stu-id="06014-167">BudgetPlanningLedgerDimension: Yes</span></span>

<span data-ttu-id="06014-168">DimensionDynamicAccount: Yes</span><span class="sxs-lookup"><span data-stu-id="06014-168">DimensionDynamicAccount: Yes</span></span>

<span data-ttu-id="06014-169">LedgerDimensionAccount: はい</span><span class="sxs-lookup"><span data-stu-id="06014-169">LedgerDimensionAccount: Yes</span></span>

<span data-ttu-id="06014-170">LedgerDimensionDefaultAccount: はい</span><span class="sxs-lookup"><span data-stu-id="06014-170">LedgerDimensionDefaultAccount: Yes</span></span>

<span data-ttu-id="06014-171">LedgerDimensionAccountAlias: いいえ</span><span class="sxs-lookup"><span data-stu-id="06014-171">LedgerDimensionAccountAlias: No</span></span>

### <a name="posting-type"></a><span data-ttu-id="06014-172">転記タイプ</span><span class="sxs-lookup"><span data-stu-id="06014-172">Posting Type</span></span>

<span data-ttu-id="06014-173">BudgetLedgerDimension: いいえ</span><span class="sxs-lookup"><span data-stu-id="06014-173">BudgetLedgerDimension: No</span></span>

<span data-ttu-id="06014-174">BudgetPlanningLedgerDimension: はい</span><span class="sxs-lookup"><span data-stu-id="06014-174">BudgetPlanningLedgerDimension: Yes</span></span>

<span data-ttu-id="06014-175">DimensionDynamicAccount: Yes</span><span class="sxs-lookup"><span data-stu-id="06014-175">DimensionDynamicAccount: Yes</span></span>

<span data-ttu-id="06014-176">LedgerDimensionAccount: はい</span><span class="sxs-lookup"><span data-stu-id="06014-176">LedgerDimensionAccount: Yes</span></span>

<span data-ttu-id="06014-177">LedgerDimensionDefaultAccount: はい</span><span class="sxs-lookup"><span data-stu-id="06014-177">LedgerDimensionDefaultAccount: Yes</span></span>

<span data-ttu-id="06014-178">LedgerDimensionAccountAlias: はい</span><span class="sxs-lookup"><span data-stu-id="06014-178">LedgerDimensionAccountAlias: Yes</span></span>

### <a name="include-total-accounts"></a><span data-ttu-id="06014-179">勘定合計を含む</span><span class="sxs-lookup"><span data-stu-id="06014-179">Include Total Accounts</span></span>

<span data-ttu-id="06014-180">BudgetLedgerDimension: いいえ</span><span class="sxs-lookup"><span data-stu-id="06014-180">BudgetLedgerDimension: No</span></span>

<span data-ttu-id="06014-181">BudgetPlanningLedgerDimension: いいえ</span><span class="sxs-lookup"><span data-stu-id="06014-181">BudgetPlanningLedgerDimension: No</span></span>

<span data-ttu-id="06014-182">DimensionDynamicAccount: Yes</span><span class="sxs-lookup"><span data-stu-id="06014-182">DimensionDynamicAccount: Yes</span></span>

<span data-ttu-id="06014-183">LedgerDimensionAccount: いいえ</span><span class="sxs-lookup"><span data-stu-id="06014-183">LedgerDimensionAccount: No</span></span>

<span data-ttu-id="06014-184">LedgerDimensionDefaultAccount: はい</span><span class="sxs-lookup"><span data-stu-id="06014-184">LedgerDimensionDefaultAccount: Yes</span></span>

<span data-ttu-id="06014-185">LedgerDimensionAccountAlias: いいえ</span><span class="sxs-lookup"><span data-stu-id="06014-185">LedgerDimensionAccountAlias: No</span></span>

### <a name="include-financial-accounts"></a><span data-ttu-id="06014-186">財務勘定を含む</span><span class="sxs-lookup"><span data-stu-id="06014-186">Include Financial Accounts</span></span>

<span data-ttu-id="06014-187">BudgetLedgerDimension: いいえ</span><span class="sxs-lookup"><span data-stu-id="06014-187">BudgetLedgerDimension: No</span></span>

<span data-ttu-id="06014-188">BudgetPlanningLedgerDimension: いいえ</span><span class="sxs-lookup"><span data-stu-id="06014-188">BudgetPlanningLedgerDimension: No</span></span>

<span data-ttu-id="06014-189">DimensionDynamicAccount: Yes</span><span class="sxs-lookup"><span data-stu-id="06014-189">DimensionDynamicAccount: Yes</span></span>

<span data-ttu-id="06014-190">LedgerDimensionAccount: いいえ</span><span class="sxs-lookup"><span data-stu-id="06014-190">LedgerDimensionAccount: No</span></span>

<span data-ttu-id="06014-191">LedgerDimensionDefaultAccount: はい</span><span class="sxs-lookup"><span data-stu-id="06014-191">LedgerDimensionDefaultAccount: Yes</span></span>

<span data-ttu-id="06014-192">LedgerDimensionAccountAlias: いいえ</span><span class="sxs-lookup"><span data-stu-id="06014-192">LedgerDimensionAccountAlias: No</span></span>

## <a name="additional-resources"></a><span data-ttu-id="06014-193">追加リソース</span><span class="sxs-lookup"><span data-stu-id="06014-193">Additional resources</span></span>

[<span data-ttu-id="06014-194">ダイアログのセグメント化されたエントリ コントロールのサポート</span><span class="sxs-lookup"><span data-stu-id="06014-194">Support for Segmented Entry controls on dialogs</span></span>](segmented-entry-control-dialog-support.md)

[<span data-ttu-id="06014-195">セグメント化されたエントリ コントロールの Parm メソッド</span><span class="sxs-lookup"><span data-stu-id="06014-195">Parm methods for Segmented Entry controls</span></span>](segmented-entry-control-parm-method-specification.md)

[<span data-ttu-id="06014-196">セグメント化されたエントリ コントロールの移行</span><span class="sxs-lookup"><span data-stu-id="06014-196">Migrate Segmented Entry controls</span></span>](segmented-entry-control-conversion.md)

[<span data-ttu-id="06014-197">セグメント化されたエントリ コントロールに関する移行ガイダンス</span><span class="sxs-lookup"><span data-stu-id="06014-197">Migration guidance for Segmented Entry controls</span></span>](segmented-entry-control-migration-guidance.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]