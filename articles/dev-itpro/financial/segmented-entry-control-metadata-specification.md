---
title: セグメント化されたエントリ コントロールのためのデザイン時メタデータ
description: セグメント化エントリ コントロールのデザイン時メタデータ プロパティについて説明します。
author: robinarh
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Developer
ms.reviewer: rhaertle
ms.search.scope: Operations
ms.custom: 25591
ms.assetid: b8c5d7a4-ee2b-4ab1-b042-88472b97f035
ms.search.region: Global
ms.author: ghenriks
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 9d40028bf62162f7e7502f5d6a88da6ee77fac65
ms.sourcegitcommit: 27a98a7a0f1d2623f5236a88066f483def30889c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/01/2019
ms.locfileid: "1833326"
---
# <a name="design-time-metadata-for-segmented-entry-controls"></a><span data-ttu-id="da11a-103">セグメント化されたエントリ コントロールのためのデザイン時メタデータ</span><span class="sxs-lookup"><span data-stu-id="da11a-103">Design-time metadata for Segmented Entry controls</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="da11a-104">セグメント化エントリ コントロールのデザイン時メタデータ プロパティについて説明します。</span><span class="sxs-lookup"><span data-stu-id="da11a-104">Describes the design-time metadata properties for Segmented Entry controls.</span></span>

<span data-ttu-id="da11a-105">セグメント化エントリ コントロールのカスタム プロパティは、コントローラー グループの下にあります。</span><span class="sxs-lookup"><span data-stu-id="da11a-105">The custom properties for the Segmented Entry control are found under the Controller group.</span></span> <span data-ttu-id="da11a-106">次に例を示します。</span><span class="sxs-lookup"><span data-stu-id="da11a-106">Here is an example.</span></span> 

<span data-ttu-id="da11a-107">[![SEC プロパティ シート例](./media/10.jpg)](./media/10.jpg)</span><span class="sxs-lookup"><span data-stu-id="da11a-107">[![SEC Property Sheet Example](./media/10.jpg)](./media/10.jpg)</span></span> 

<span data-ttu-id="da11a-108">一部のプロパティは、選択されたコントローラ クラスに基づいて編集できない場合があります。</span><span class="sxs-lookup"><span data-stu-id="da11a-108">Certain properties may be non-editable based on the Controller class that is selected.</span></span> <span data-ttu-id="da11a-109">これは、特定のプロパティのみがさまざまなコントローラー クラスのそれぞれに関連するためです。</span><span class="sxs-lookup"><span data-stu-id="da11a-109">This is because only certain properties are relevant for each of the various controller classes.</span></span>  <span data-ttu-id="da11a-110">詳細については、この記事の下部にある表を参照してください。</span><span class="sxs-lookup"><span data-stu-id="da11a-110">See the table at the bottom of this article for more details.</span></span>

##### <a name="property-details"></a><span data-ttu-id="da11a-111">プロパティの詳細</span><span class="sxs-lookup"><span data-stu-id="da11a-111">Property details</span></span>

|                                   |                                                                                   |                                                                                                                                                                                                              |
|-----------------------------------|-----------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="da11a-112">**プロパティ**</span><span class="sxs-lookup"><span data-stu-id="da11a-112">**Property**</span></span>                      | <span data-ttu-id="da11a-113">**有効な値**</span><span class="sxs-lookup"><span data-stu-id="da11a-113">**Valid values**</span></span>                                                                  | <span data-ttu-id="da11a-114">**用途**</span><span class="sxs-lookup"><span data-stu-id="da11a-114">**Usage**</span></span>                                                                                                                                                                                                    |
| <span data-ttu-id="da11a-115">勘定タイプ フィールド</span><span class="sxs-lookup"><span data-stu-id="da11a-115">Account Type Field</span></span>                | <span data-ttu-id="da11a-116">データ ソースからのフィールド。</span><span class="sxs-lookup"><span data-stu-id="da11a-116">A field from the datasource.</span></span>                                                      | <span data-ttu-id="da11a-117">使用されるアカウントの種類を決定します。</span><span class="sxs-lookup"><span data-stu-id="da11a-117">Determines the type of account used.</span></span> <span data-ttu-id="da11a-118">通常、複数セグメントの勘定科目から、Cust、Vend、Bank、Project などの他のックアップ テーブルの単一セグメント値への仕訳入力に使用します。</span><span class="sxs-lookup"><span data-stu-id="da11a-118">Typically use for journal entry from a multi-segment ledger account to single segment values from other backing tables, such as Cust, Vend, Bank, Project, and similar.</span></span> |
| <span data-ttu-id="da11a-119">コントローラー クラス</span><span class="sxs-lookup"><span data-stu-id="da11a-119">Controller Class</span></span>                  | <span data-ttu-id="da11a-120">7 つのコントローラー クラスのうちの 1 つです。</span><span class="sxs-lookup"><span data-stu-id="da11a-120">One of 7 Controller classes.</span></span> <span data-ttu-id="da11a-121">たとえば LedgerDimensionDefaultAccountController。</span><span class="sxs-lookup"><span data-stu-id="da11a-121">For example LedgerDimensionDefaultAccountController.</span></span> | <span data-ttu-id="da11a-122">セグメント化されたエントリ コントロールの動作およびパターンを決定します。</span><span class="sxs-lookup"><span data-stu-id="da11a-122">Determines the pattern and behavior of the Segmented Entry control.</span></span>                                                                                                                                          |
| <span data-ttu-id="da11a-123">財務勘定を含む</span><span class="sxs-lookup"><span data-stu-id="da11a-123">Include Financial Accounts</span></span>        | <span data-ttu-id="da11a-124">NoYes</span><span class="sxs-lookup"><span data-stu-id="da11a-124">NoYes</span></span>                                                                             | <span data-ttu-id="da11a-125">財務勘定である主勘定が有効であるかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="da11a-125">Determines if Main accounts that are Financial accounts are valid for use.</span></span>                                                                                                                                   |
| <span data-ttu-id="da11a-126">勘定合計を含む</span><span class="sxs-lookup"><span data-stu-id="da11a-126">Include Total Accounts</span></span>            | <span data-ttu-id="da11a-127">NoYes</span><span class="sxs-lookup"><span data-stu-id="da11a-127">NoYes</span></span>                                                                             | <span data-ttu-id="da11a-128">タイプが "合計" の主勘定が有効であるかどうかを判断します。</span><span class="sxs-lookup"><span data-stu-id="da11a-128">Determines if Main accounts of type Total are valid for use.</span></span>                                                                                                                                                 |
| <span data-ttu-id="da11a-129">既定の勘定です。</span><span class="sxs-lookup"><span data-stu-id="da11a-129">Is Default Account</span></span>                | <span data-ttu-id="da11a-130">TrueFalse</span><span class="sxs-lookup"><span data-stu-id="da11a-130">TrueFalse</span></span>                                                                         | <span data-ttu-id="da11a-131">動的アカウントで、アカウントが既定または完全アカウントであるべきかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="da11a-131">For a Dynamic account, determines if the account should be a default or full account.</span></span>                                                                                                                        |
| <span data-ttu-id="da11a-132">主勘定セグメントのロック</span><span class="sxs-lookup"><span data-stu-id="da11a-132">Lock Main Account Segment</span></span>         | <span data-ttu-id="da11a-133">NoYes</span><span class="sxs-lookup"><span data-stu-id="da11a-133">NoYes</span></span>                                                                             | <span data-ttu-id="da11a-134">主勘定セグメントがロックされているかどうかをコントロールします。</span><span class="sxs-lookup"><span data-stu-id="da11a-134">Controls whether the Main account segment is locked.</span></span>  <span data-ttu-id="da11a-135">通常は仕訳帳や構成に基づく配分に使用されます。</span><span class="sxs-lookup"><span data-stu-id="da11a-135">Typically used in journals and distributions based on configuration.</span></span>                                                                                   |
| <span data-ttu-id="da11a-136">転記タイプ</span><span class="sxs-lookup"><span data-stu-id="da11a-136">Posting Type</span></span>                      | <span data-ttu-id="da11a-137">LedgerPostingType 列挙の値。</span><span class="sxs-lookup"><span data-stu-id="da11a-137">A value from the LedgerPostingType enumeration.</span></span>                                   | <span data-ttu-id="da11a-138">主勘定が検証され、そのアカウントで使用される転記タイプが許可されているかどうかを確認されます。</span><span class="sxs-lookup"><span data-stu-id="da11a-138">The Main account is validated to see if the posting type is allowed to be used with that account.</span></span>                                                                                                            |
| <span data-ttu-id="da11a-139">手動入力のブロック状態の検証</span><span class="sxs-lookup"><span data-stu-id="da11a-139">Validate Blocked For Manual Entry</span></span> | <span data-ttu-id="da11a-140">NoYes</span><span class="sxs-lookup"><span data-stu-id="da11a-140">NoYes</span></span>                                                                             | <span data-ttu-id="da11a-141">分析コードの「手動入力のブロック」ステータスを優先するかを決定します。</span><span class="sxs-lookup"><span data-stu-id="da11a-141">Determines if the 'Blocked for Manual Entry' status on the dimension should be respected.</span></span>                                                                                                                    |

  <span data-ttu-id="da11a-142">このテーブルは、各コント ローラー タイプに有効なプロパティを示します ('X' とマークされたとき有効です)。</span><span class="sxs-lookup"><span data-stu-id="da11a-142">This table shows which properties are valid for each Controller type (marked with 'X' means valid).</span></span>

## <a name="validate-blocked-for-manual-entry"></a><span data-ttu-id="da11a-143">手動入力のブロック状態の検証</span><span class="sxs-lookup"><span data-stu-id="da11a-143">Validate Blocked For Manual Entry</span></span> 

<span data-ttu-id="da11a-144">BudgetLedgerDimension: はい</span><span class="sxs-lookup"><span data-stu-id="da11a-144">BudgetLedgerDimension: Yes</span></span>

<span data-ttu-id="da11a-145">BudgetPlanningLedgerDimension: はい</span><span class="sxs-lookup"><span data-stu-id="da11a-145">BudgetPlanningLedgerDimension: Yes</span></span> 

<span data-ttu-id="da11a-146">DimensionDynamicAccount: Yes</span><span class="sxs-lookup"><span data-stu-id="da11a-146">DimensionDynamicAccount: Yes</span></span>

<span data-ttu-id="da11a-147">LedgerDimensionAccount: はい</span><span class="sxs-lookup"><span data-stu-id="da11a-147">LedgerDimensionAccount: Yes</span></span>

<span data-ttu-id="da11a-148">LedgerDimensionDefaultAccount: はい</span><span class="sxs-lookup"><span data-stu-id="da11a-148">LedgerDimensionDefaultAccount: Yes</span></span>

<span data-ttu-id="da11a-149">LedgerDimensionAccountAlias: はい</span><span class="sxs-lookup"><span data-stu-id="da11a-149">LedgerDimensionAccountAlias: Yes</span></span>

## <a name="account-type-field"></a><span data-ttu-id="da11a-150">勘定タイプ フィールド</span><span class="sxs-lookup"><span data-stu-id="da11a-150">Account Type Field</span></span>     

<span data-ttu-id="da11a-151">BudgetLedgerDimension: いいえ</span><span class="sxs-lookup"><span data-stu-id="da11a-151">BudgetLedgerDimension: No</span></span>

<span data-ttu-id="da11a-152">BudgetPlanningLedgerDimension: いいえ</span><span class="sxs-lookup"><span data-stu-id="da11a-152">BudgetPlanningLedgerDimension: No</span></span>

<span data-ttu-id="da11a-153">DimensionDynamicAccount: Yes</span><span class="sxs-lookup"><span data-stu-id="da11a-153">DimensionDynamicAccount: Yes</span></span>

<span data-ttu-id="da11a-154">LedgerDimensionAccount: いいえ</span><span class="sxs-lookup"><span data-stu-id="da11a-154">LedgerDimensionAccount: No</span></span>

<span data-ttu-id="da11a-155">LedgerDimensionDefaultAccount: いいえ</span><span class="sxs-lookup"><span data-stu-id="da11a-155">LedgerDimensionDefaultAccount : No</span></span>

<span data-ttu-id="da11a-156">LedgerDimensionAccountAlias: いいえ</span><span class="sxs-lookup"><span data-stu-id="da11a-156">LedgerDimensionAccountAlias: No</span></span>

## <a name="is-default-account"></a><span data-ttu-id="da11a-157">既定の勘定です。</span><span class="sxs-lookup"><span data-stu-id="da11a-157">Is Default Account</span></span>     

<span data-ttu-id="da11a-158">BudgetLedgerDimension: いいえ</span><span class="sxs-lookup"><span data-stu-id="da11a-158">BudgetLedgerDimension: No</span></span>

<span data-ttu-id="da11a-159">BudgetPlanningLedgerDimension: いいえ</span><span class="sxs-lookup"><span data-stu-id="da11a-159">BudgetPlanningLedgerDimension: No</span></span>

<span data-ttu-id="da11a-160">DimensionDynamicAccount: Yes</span><span class="sxs-lookup"><span data-stu-id="da11a-160">DimensionDynamicAccount: Yes</span></span>

<span data-ttu-id="da11a-161">LedgerDimensionAccount: いいえ</span><span class="sxs-lookup"><span data-stu-id="da11a-161">LedgerDimensionAccount: No</span></span>

<span data-ttu-id="da11a-162">LedgerDimensionDefaultAccount: いいえ</span><span class="sxs-lookup"><span data-stu-id="da11a-162">LedgerDimensionDefaultAccount : No</span></span>

<span data-ttu-id="da11a-163">LedgerDimensionAccountAlias: いいえ</span><span class="sxs-lookup"><span data-stu-id="da11a-163">LedgerDimensionAccountAlias: No</span></span>

## <a name="lock-main-account-segment"></a><span data-ttu-id="da11a-164">主勘定セグメントのロック</span><span class="sxs-lookup"><span data-stu-id="da11a-164">Lock Main Account Segment</span></span>        

<span data-ttu-id="da11a-165">BudgetLedgerDimension: いいえ</span><span class="sxs-lookup"><span data-stu-id="da11a-165">BudgetLedgerDimension: No</span></span>

<span data-ttu-id="da11a-166">BudgetPlanningLedgerDimension: はい</span><span class="sxs-lookup"><span data-stu-id="da11a-166">BudgetPlanningLedgerDimension: Yes</span></span>

<span data-ttu-id="da11a-167">DimensionDynamicAccount: Yes</span><span class="sxs-lookup"><span data-stu-id="da11a-167">DimensionDynamicAccount: Yes</span></span>

<span data-ttu-id="da11a-168">LedgerDimensionAccount: はい</span><span class="sxs-lookup"><span data-stu-id="da11a-168">LedgerDimensionAccount: Yes</span></span>

<span data-ttu-id="da11a-169">LedgerDimensionDefaultAccount: はい</span><span class="sxs-lookup"><span data-stu-id="da11a-169">LedgerDimensionDefaultAccount: Yes</span></span>

<span data-ttu-id="da11a-170">LedgerDimensionAccountAlias: いいえ</span><span class="sxs-lookup"><span data-stu-id="da11a-170">LedgerDimensionAccountAlias: No</span></span>

## <a name="posting-type"></a><span data-ttu-id="da11a-171">転記タイプ</span><span class="sxs-lookup"><span data-stu-id="da11a-171">Posting Type</span></span> 

<span data-ttu-id="da11a-172">BudgetLedgerDimension: いいえ</span><span class="sxs-lookup"><span data-stu-id="da11a-172">BudgetLedgerDimension: No</span></span>

<span data-ttu-id="da11a-173">BudgetPlanningLedgerDimension: はい</span><span class="sxs-lookup"><span data-stu-id="da11a-173">BudgetPlanningLedgerDimension: Yes</span></span>

<span data-ttu-id="da11a-174">DimensionDynamicAccount: Yes</span><span class="sxs-lookup"><span data-stu-id="da11a-174">DimensionDynamicAccount: Yes</span></span>

<span data-ttu-id="da11a-175">LedgerDimensionAccount: はい</span><span class="sxs-lookup"><span data-stu-id="da11a-175">LedgerDimensionAccount: Yes</span></span>

<span data-ttu-id="da11a-176">LedgerDimensionDefaultAccount: はい</span><span class="sxs-lookup"><span data-stu-id="da11a-176">LedgerDimensionDefaultAccount : Yes</span></span> 

<span data-ttu-id="da11a-177">LedgerDimensionAccountAlias: はい</span><span class="sxs-lookup"><span data-stu-id="da11a-177">LedgerDimensionAccountAlias: Yes</span></span>

## <a name="include-total-accounts"></a><span data-ttu-id="da11a-178">勘定合計を含む</span><span class="sxs-lookup"><span data-stu-id="da11a-178">Include Total Accounts</span></span> 

<span data-ttu-id="da11a-179">BudgetLedgerDimension: いいえ</span><span class="sxs-lookup"><span data-stu-id="da11a-179">BudgetLedgerDimension: No</span></span>

<span data-ttu-id="da11a-180">BudgetPlanningLedgerDimension: いいえ</span><span class="sxs-lookup"><span data-stu-id="da11a-180">BudgetPlanningLedgerDimension: No</span></span>

<span data-ttu-id="da11a-181">DimensionDynamicAccount: Yes</span><span class="sxs-lookup"><span data-stu-id="da11a-181">DimensionDynamicAccount: Yes</span></span>

<span data-ttu-id="da11a-182">LedgerDimensionAccount: いいえ</span><span class="sxs-lookup"><span data-stu-id="da11a-182">LedgerDimensionAccount: No</span></span>

<span data-ttu-id="da11a-183">LedgerDimensionDefaultAccount: はい</span><span class="sxs-lookup"><span data-stu-id="da11a-183">LedgerDimensionDefaultAccount : Yes</span></span>

<span data-ttu-id="da11a-184">LedgerDimensionAccountAlias: いいえ</span><span class="sxs-lookup"><span data-stu-id="da11a-184">LedgerDimensionAccountAlias: No</span></span>

## <a name="include-financial-accounts"></a><span data-ttu-id="da11a-185">財務勘定を含む</span><span class="sxs-lookup"><span data-stu-id="da11a-185">Include Financial Accounts</span></span>       

<span data-ttu-id="da11a-186">BudgetLedgerDimension: いいえ</span><span class="sxs-lookup"><span data-stu-id="da11a-186">BudgetLedgerDimension: No</span></span>

<span data-ttu-id="da11a-187">BudgetPlanningLedgerDimension: いいえ</span><span class="sxs-lookup"><span data-stu-id="da11a-187">BudgetPlanningLedgerDimension: No</span></span>

<span data-ttu-id="da11a-188">DimensionDynamicAccount: Yes</span><span class="sxs-lookup"><span data-stu-id="da11a-188">DimensionDynamicAccount: Yes</span></span>

<span data-ttu-id="da11a-189">LedgerDimensionAccount: いいえ</span><span class="sxs-lookup"><span data-stu-id="da11a-189">LedgerDimensionAccount: No</span></span>

<span data-ttu-id="da11a-190">LedgerDimensionDefaultAccount: はい</span><span class="sxs-lookup"><span data-stu-id="da11a-190">LedgerDimensionDefaultAccount : Yes</span></span>

<span data-ttu-id="da11a-191">LedgerDimensionAccountAlias: いいえ</span><span class="sxs-lookup"><span data-stu-id="da11a-191">LedgerDimensionAccountAlias: No</span></span>


<a name="additional-resources"></a><span data-ttu-id="da11a-192">その他のリソース</span><span class="sxs-lookup"><span data-stu-id="da11a-192">Additional resources</span></span>
--------

[<span data-ttu-id="da11a-193">セグメント化されたエントリ コントロールのダイアログのサポート</span><span class="sxs-lookup"><span data-stu-id="da11a-193">Segmented Entry control dialog support</span></span>](segmented-entry-control-dialog-support.md)

[<span data-ttu-id="da11a-194">セグメント化されたエントリ コントロールの Parm メソッド詳細</span><span class="sxs-lookup"><span data-stu-id="da11a-194">Segmented Entry control Parm method Specification</span></span>](segmented-entry-control-parm-method-specification.md)

[<span data-ttu-id="da11a-195">セグメント化されたエントリ コントロールの移行</span><span class="sxs-lookup"><span data-stu-id="da11a-195">Segmented Entry control migration</span></span>](segmented-entry-control-conversion.md)

[<span data-ttu-id="da11a-196">セグメント化されたエントリ コントロール - 移行のガイダンス</span><span class="sxs-lookup"><span data-stu-id="da11a-196">Segmented Entry control - Migration guidance</span></span>](segmented-entry-control-migration-guidance.md)



