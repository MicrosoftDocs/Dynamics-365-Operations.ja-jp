---
title: "セグメント化されたエントリ コントロールのメタデータ"
description: "セグメント化エントリ コントロールのデザイン時メタデータ プロパティについて説明します。"
author: twheeloc
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Developer
ms.reviewer: robinr
ms.search.scope: Operations
ms.custom: 25591
ms.assetid: b8c5d7a4-ee2b-4ab1-b042-88472b97f035
ms.search.region: Global
ms.author: ghenriks
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: 84bc177c20f22137eca16c63b0406425dcaa77ab
ms.contentlocale: ja-jp
ms.lasthandoff: 05/08/2018

---

# <a name="segmented-entry-control-metadata"></a><span data-ttu-id="4002b-103">セグメント化されたエントリ コントロールのメタデータ</span><span class="sxs-lookup"><span data-stu-id="4002b-103">Segmented entry control metadata</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="4002b-104">セグメント化エントリ コントロールのデザイン時メタデータ プロパティについて説明します。</span><span class="sxs-lookup"><span data-stu-id="4002b-104">Describes the design-time metadata properties for Segmented Entry controls.</span></span>

<span data-ttu-id="4002b-105">セグメント化エントリ コントロールのカスタム プロパティは、コントローラー グループの下にあります。</span><span class="sxs-lookup"><span data-stu-id="4002b-105">The custom properties for the Segmented Entry control are found under the Controller group.</span></span> <span data-ttu-id="4002b-106">次に例を示します。</span><span class="sxs-lookup"><span data-stu-id="4002b-106">Here is an example.</span></span> 

<span data-ttu-id="4002b-107">[![SEC プロパティ シート例](./media/10.jpg)](./media/10.jpg)</span><span class="sxs-lookup"><span data-stu-id="4002b-107">[![SEC Property Sheet Example](./media/10.jpg)](./media/10.jpg)</span></span> 

<span data-ttu-id="4002b-108">一部のプロパティは、選択されたコントローラ クラスに基づいて編集できない場合があります。</span><span class="sxs-lookup"><span data-stu-id="4002b-108">Certain properties may be non-editable based on the Controller class that is selected.</span></span> <span data-ttu-id="4002b-109">これは、特定のプロパティのみがさまざまなコントローラー クラスのそれぞれに関連するためです。</span><span class="sxs-lookup"><span data-stu-id="4002b-109">This is because only certain properties are relevant for each of the various controller classes.</span></span>  <span data-ttu-id="4002b-110">詳細については、この記事の下部にある表を参照してください。</span><span class="sxs-lookup"><span data-stu-id="4002b-110">See the table at the bottom of this article for more details.</span></span>

##### <a name="property-details"></a><span data-ttu-id="4002b-111">プロパティの詳細</span><span class="sxs-lookup"><span data-stu-id="4002b-111">Property details</span></span>

|                                   |                                                                                   |                                                                                                                                                                                                              |
|-----------------------------------|-----------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4002b-112">**プロパティ**</span><span class="sxs-lookup"><span data-stu-id="4002b-112">**Property**</span></span>                      | <span data-ttu-id="4002b-113">**有効な値**</span><span class="sxs-lookup"><span data-stu-id="4002b-113">**Valid values**</span></span>                                                                  | <span data-ttu-id="4002b-114">**用途**</span><span class="sxs-lookup"><span data-stu-id="4002b-114">**Usage**</span></span>                                                                                                                                                                                                    |
| <span data-ttu-id="4002b-115">勘定タイプ フィールド</span><span class="sxs-lookup"><span data-stu-id="4002b-115">Account Type Field</span></span>                | <span data-ttu-id="4002b-116">データ ソースからのフィールド。</span><span class="sxs-lookup"><span data-stu-id="4002b-116">A field from the datasource.</span></span>                                                      | <span data-ttu-id="4002b-117">使用されるアカウントの種類を決定します。</span><span class="sxs-lookup"><span data-stu-id="4002b-117">Determines the type of account used.</span></span> <span data-ttu-id="4002b-118">通常、複数セグメントの勘定科目から、Cust、Vend、Bank、Project などの他のックアップ テーブルの単一セグメント値への仕訳入力に使用します。</span><span class="sxs-lookup"><span data-stu-id="4002b-118">Typically use for journal entry from a multi-segment ledger account to single segment values from other backing tables, such as Cust, Vend, Bank, Project, and similar.</span></span> |
| <span data-ttu-id="4002b-119">コントローラー クラス</span><span class="sxs-lookup"><span data-stu-id="4002b-119">Controller Class</span></span>                  | <span data-ttu-id="4002b-120">7 つのコントローラー クラスのうちの 1 つです。</span><span class="sxs-lookup"><span data-stu-id="4002b-120">One of 7 Controller classes.</span></span> <span data-ttu-id="4002b-121">たとえば LedgerDimensionDefaultAccountController。</span><span class="sxs-lookup"><span data-stu-id="4002b-121">For example LedgerDimensionDefaultAccountController.</span></span> | <span data-ttu-id="4002b-122">セグメント化されたエントリ コントロールの動作およびパターンを決定します。</span><span class="sxs-lookup"><span data-stu-id="4002b-122">Determines the pattern and behavior of the Segmented Entry control.</span></span>                                                                                                                                          |
| <span data-ttu-id="4002b-123">財務勘定を含む</span><span class="sxs-lookup"><span data-stu-id="4002b-123">Include Financial Accounts</span></span>        | <span data-ttu-id="4002b-124">NoYes</span><span class="sxs-lookup"><span data-stu-id="4002b-124">NoYes</span></span>                                                                             | <span data-ttu-id="4002b-125">財務勘定である主勘定が有効であるかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="4002b-125">Determines if Main accounts that are Financial accounts are valid for use.</span></span>                                                                                                                                   |
| <span data-ttu-id="4002b-126">勘定合計を含む</span><span class="sxs-lookup"><span data-stu-id="4002b-126">Include Total Accounts</span></span>            | <span data-ttu-id="4002b-127">NoYes</span><span class="sxs-lookup"><span data-stu-id="4002b-127">NoYes</span></span>                                                                             | <span data-ttu-id="4002b-128">タイプが "合計" の主勘定が有効であるかどうかを判断します。</span><span class="sxs-lookup"><span data-stu-id="4002b-128">Determines if Main accounts of type Total are valid for use.</span></span>                                                                                                                                                 |
| <span data-ttu-id="4002b-129">既定の勘定です。</span><span class="sxs-lookup"><span data-stu-id="4002b-129">Is Default Account</span></span>                | <span data-ttu-id="4002b-130">TrueFalse</span><span class="sxs-lookup"><span data-stu-id="4002b-130">TrueFalse</span></span>                                                                         | <span data-ttu-id="4002b-131">動的アカウントで、アカウントが既定または完全アカウントであるべきかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="4002b-131">For a Dynamic account, determines if the account should be a default or full account.</span></span>                                                                                                                        |
| <span data-ttu-id="4002b-132">主勘定セグメントのロック</span><span class="sxs-lookup"><span data-stu-id="4002b-132">Lock Main Account Segment</span></span>         | <span data-ttu-id="4002b-133">NoYes</span><span class="sxs-lookup"><span data-stu-id="4002b-133">NoYes</span></span>                                                                             | <span data-ttu-id="4002b-134">主勘定セグメントがロックされているかどうかをコントロールします。</span><span class="sxs-lookup"><span data-stu-id="4002b-134">Controls whether the Main account segment is locked.</span></span>  <span data-ttu-id="4002b-135">通常は仕訳帳や構成に基づく配分に使用されます。</span><span class="sxs-lookup"><span data-stu-id="4002b-135">Typically used in journals and distributions based on configuration.</span></span>                                                                                   |
| <span data-ttu-id="4002b-136">転記タイプ</span><span class="sxs-lookup"><span data-stu-id="4002b-136">Posting Type</span></span>                      | <span data-ttu-id="4002b-137">LedgerPostingType 列挙の値。</span><span class="sxs-lookup"><span data-stu-id="4002b-137">A value from the LedgerPostingType enumeration.</span></span>                                   | <span data-ttu-id="4002b-138">主勘定が検証され、そのアカウントで使用される転記タイプが許可されているかどうかを確認されます。</span><span class="sxs-lookup"><span data-stu-id="4002b-138">The Main account is validated to see if the posting type is allowed to be used with that account.</span></span>                                                                                                            |
| <span data-ttu-id="4002b-139">手動入力のブロック状態の検証</span><span class="sxs-lookup"><span data-stu-id="4002b-139">Validate Blocked For Manual Entry</span></span> | <span data-ttu-id="4002b-140">NoYes</span><span class="sxs-lookup"><span data-stu-id="4002b-140">NoYes</span></span>                                                                             | <span data-ttu-id="4002b-141">分析コードの「手動入力のブロック」ステータスを優先するかを決定します。</span><span class="sxs-lookup"><span data-stu-id="4002b-141">Determines if the 'Blocked for Manual Entry' status on the dimension should be respected.</span></span>                                                                                                                    |

  <span data-ttu-id="4002b-142">このテーブルは、各コント ローラー タイプに有効なプロパティを示します ('X' とマークされたとき有効です)。</span><span class="sxs-lookup"><span data-stu-id="4002b-142">This table shows which properties are valid for each Controller type (marked with 'X' means valid).</span></span>

## <a name="validate-blocked-for-manual-entry"></a><span data-ttu-id="4002b-143">手動入力のブロック状態の検証</span><span class="sxs-lookup"><span data-stu-id="4002b-143">Validate Blocked For Manual Entry</span></span> 

<span data-ttu-id="4002b-144">BudgetLedgerDimension: はい</span><span class="sxs-lookup"><span data-stu-id="4002b-144">BudgetLedgerDimension: Yes</span></span>

<span data-ttu-id="4002b-145">BudgetPlanningLedgerDimension: はい</span><span class="sxs-lookup"><span data-stu-id="4002b-145">BudgetPlanningLedgerDimension: Yes</span></span> 

<span data-ttu-id="4002b-146">DimensionDynamicAccount: Yes</span><span class="sxs-lookup"><span data-stu-id="4002b-146">DimensionDynamicAccount: Yes</span></span>

<span data-ttu-id="4002b-147">LedgerDimensionAccount: はい</span><span class="sxs-lookup"><span data-stu-id="4002b-147">LedgerDimensionAccount: Yes</span></span>

<span data-ttu-id="4002b-148">LedgerDimensionDefaultAccount: はい</span><span class="sxs-lookup"><span data-stu-id="4002b-148">LedgerDimensionDefaultAccount: Yes</span></span>

<span data-ttu-id="4002b-149">LedgerDimensionAccountAlias: はい</span><span class="sxs-lookup"><span data-stu-id="4002b-149">LedgerDimensionAccountAlias: Yes</span></span>

## <a name="account-type-field"></a><span data-ttu-id="4002b-150">勘定タイプ フィールド</span><span class="sxs-lookup"><span data-stu-id="4002b-150">Account Type Field</span></span>     

<span data-ttu-id="4002b-151">BudgetLedgerDimension: いいえ</span><span class="sxs-lookup"><span data-stu-id="4002b-151">BudgetLedgerDimension: No</span></span>

<span data-ttu-id="4002b-152">BudgetPlanningLedgerDimension: いいえ</span><span class="sxs-lookup"><span data-stu-id="4002b-152">BudgetPlanningLedgerDimension: No</span></span>

<span data-ttu-id="4002b-153">DimensionDynamicAccount: Yes</span><span class="sxs-lookup"><span data-stu-id="4002b-153">DimensionDynamicAccount: Yes</span></span>

<span data-ttu-id="4002b-154">LedgerDimensionAccount: いいえ</span><span class="sxs-lookup"><span data-stu-id="4002b-154">LedgerDimensionAccount: No</span></span>

<span data-ttu-id="4002b-155">LedgerDimensionDefaultAccount: いいえ</span><span class="sxs-lookup"><span data-stu-id="4002b-155">LedgerDimensionDefaultAccount : No</span></span>

<span data-ttu-id="4002b-156">LedgerDimensionAccountAlias: いいえ</span><span class="sxs-lookup"><span data-stu-id="4002b-156">LedgerDimensionAccountAlias: No</span></span>

## <a name="is-default-account"></a><span data-ttu-id="4002b-157">既定の勘定です。</span><span class="sxs-lookup"><span data-stu-id="4002b-157">Is Default Account</span></span>     

<span data-ttu-id="4002b-158">BudgetLedgerDimension: いいえ</span><span class="sxs-lookup"><span data-stu-id="4002b-158">BudgetLedgerDimension: No</span></span>

<span data-ttu-id="4002b-159">BudgetPlanningLedgerDimension: いいえ</span><span class="sxs-lookup"><span data-stu-id="4002b-159">BudgetPlanningLedgerDimension: No</span></span>

<span data-ttu-id="4002b-160">DimensionDynamicAccount: Yes</span><span class="sxs-lookup"><span data-stu-id="4002b-160">DimensionDynamicAccount: Yes</span></span>

<span data-ttu-id="4002b-161">LedgerDimensionAccount: いいえ</span><span class="sxs-lookup"><span data-stu-id="4002b-161">LedgerDimensionAccount: No</span></span>

<span data-ttu-id="4002b-162">LedgerDimensionDefaultAccount: いいえ</span><span class="sxs-lookup"><span data-stu-id="4002b-162">LedgerDimensionDefaultAccount : No</span></span>

<span data-ttu-id="4002b-163">LedgerDimensionAccountAlias: いいえ</span><span class="sxs-lookup"><span data-stu-id="4002b-163">LedgerDimensionAccountAlias: No</span></span>

## <a name="lock-main-account-segment"></a><span data-ttu-id="4002b-164">主勘定セグメントのロック</span><span class="sxs-lookup"><span data-stu-id="4002b-164">Lock Main Account Segment</span></span>        

<span data-ttu-id="4002b-165">BudgetLedgerDimension: いいえ</span><span class="sxs-lookup"><span data-stu-id="4002b-165">BudgetLedgerDimension: No</span></span>

<span data-ttu-id="4002b-166">BudgetPlanningLedgerDimension: はい</span><span class="sxs-lookup"><span data-stu-id="4002b-166">BudgetPlanningLedgerDimension: Yes</span></span>

<span data-ttu-id="4002b-167">DimensionDynamicAccount: Yes</span><span class="sxs-lookup"><span data-stu-id="4002b-167">DimensionDynamicAccount: Yes</span></span>

<span data-ttu-id="4002b-168">LedgerDimensionAccount: はい</span><span class="sxs-lookup"><span data-stu-id="4002b-168">LedgerDimensionAccount: Yes</span></span>

<span data-ttu-id="4002b-169">LedgerDimensionDefaultAccount: はい</span><span class="sxs-lookup"><span data-stu-id="4002b-169">LedgerDimensionDefaultAccount: Yes</span></span>

<span data-ttu-id="4002b-170">LedgerDimensionAccountAlias: いいえ</span><span class="sxs-lookup"><span data-stu-id="4002b-170">LedgerDimensionAccountAlias: No</span></span>

## <a name="posting-type"></a><span data-ttu-id="4002b-171">転記タイプ</span><span class="sxs-lookup"><span data-stu-id="4002b-171">Posting Type</span></span> 

<span data-ttu-id="4002b-172">BudgetLedgerDimension: いいえ</span><span class="sxs-lookup"><span data-stu-id="4002b-172">BudgetLedgerDimension: No</span></span>

<span data-ttu-id="4002b-173">BudgetPlanningLedgerDimension: はい</span><span class="sxs-lookup"><span data-stu-id="4002b-173">BudgetPlanningLedgerDimension: Yes</span></span>

<span data-ttu-id="4002b-174">DimensionDynamicAccount: Yes</span><span class="sxs-lookup"><span data-stu-id="4002b-174">DimensionDynamicAccount: Yes</span></span>

<span data-ttu-id="4002b-175">LedgerDimensionAccount: はい</span><span class="sxs-lookup"><span data-stu-id="4002b-175">LedgerDimensionAccount: Yes</span></span>

<span data-ttu-id="4002b-176">LedgerDimensionDefaultAccount: はい</span><span class="sxs-lookup"><span data-stu-id="4002b-176">LedgerDimensionDefaultAccount : Yes</span></span> 

<span data-ttu-id="4002b-177">LedgerDimensionAccountAlias: はい</span><span class="sxs-lookup"><span data-stu-id="4002b-177">LedgerDimensionAccountAlias: Yes</span></span>

## <a name="include-total-accounts"></a><span data-ttu-id="4002b-178">勘定合計を含む</span><span class="sxs-lookup"><span data-stu-id="4002b-178">Include Total Accounts</span></span> 

<span data-ttu-id="4002b-179">BudgetLedgerDimension: いいえ</span><span class="sxs-lookup"><span data-stu-id="4002b-179">BudgetLedgerDimension: No</span></span>

<span data-ttu-id="4002b-180">BudgetPlanningLedgerDimension: いいえ</span><span class="sxs-lookup"><span data-stu-id="4002b-180">BudgetPlanningLedgerDimension: No</span></span>

<span data-ttu-id="4002b-181">DimensionDynamicAccount: Yes</span><span class="sxs-lookup"><span data-stu-id="4002b-181">DimensionDynamicAccount: Yes</span></span>

<span data-ttu-id="4002b-182">LedgerDimensionAccount: いいえ</span><span class="sxs-lookup"><span data-stu-id="4002b-182">LedgerDimensionAccount: No</span></span>

<span data-ttu-id="4002b-183">LedgerDimensionDefaultAccount: はい</span><span class="sxs-lookup"><span data-stu-id="4002b-183">LedgerDimensionDefaultAccount : Yes</span></span>

<span data-ttu-id="4002b-184">LedgerDimensionAccountAlias: いいえ</span><span class="sxs-lookup"><span data-stu-id="4002b-184">LedgerDimensionAccountAlias: No</span></span>

## <a name="include-financial-accounts"></a><span data-ttu-id="4002b-185">財務勘定を含む</span><span class="sxs-lookup"><span data-stu-id="4002b-185">Include Financial Accounts</span></span>       

<span data-ttu-id="4002b-186">BudgetLedgerDimension: いいえ</span><span class="sxs-lookup"><span data-stu-id="4002b-186">BudgetLedgerDimension: No</span></span>

<span data-ttu-id="4002b-187">BudgetPlanningLedgerDimension: いいえ</span><span class="sxs-lookup"><span data-stu-id="4002b-187">BudgetPlanningLedgerDimension: No</span></span>

<span data-ttu-id="4002b-188">DimensionDynamicAccount: Yes</span><span class="sxs-lookup"><span data-stu-id="4002b-188">DimensionDynamicAccount: Yes</span></span>

<span data-ttu-id="4002b-189">LedgerDimensionAccount: いいえ</span><span class="sxs-lookup"><span data-stu-id="4002b-189">LedgerDimensionAccount: No</span></span>

<span data-ttu-id="4002b-190">LedgerDimensionDefaultAccount: はい</span><span class="sxs-lookup"><span data-stu-id="4002b-190">LedgerDimensionDefaultAccount : Yes</span></span>

<span data-ttu-id="4002b-191">LedgerDimensionAccountAlias: いいえ</span><span class="sxs-lookup"><span data-stu-id="4002b-191">LedgerDimensionAccountAlias: No</span></span>


<a name="additional-resources"></a><span data-ttu-id="4002b-192">その他のリソース</span><span class="sxs-lookup"><span data-stu-id="4002b-192">Additional resources</span></span>
--------

[<span data-ttu-id="4002b-193">セグメント化されたエントリ コントロールのダイアログのサポート</span><span class="sxs-lookup"><span data-stu-id="4002b-193">Segmented Entry control dialog support</span></span>](segmented-entry-control-dialog-support.md)

[<span data-ttu-id="4002b-194">セグメント化されたエントリ コントロールの Parm メソッド詳細</span><span class="sxs-lookup"><span data-stu-id="4002b-194">Segmented Entry control Parm method Specification</span></span>](segmented-entry-control-parm-method-specification.md)

[<span data-ttu-id="4002b-195">セグメント化されたエントリ コントロールの移行</span><span class="sxs-lookup"><span data-stu-id="4002b-195">Segmented Entry control migration</span></span>](segmented-entry-control-conversion.md)

[<span data-ttu-id="4002b-196">セグメント化されたエントリ コントロール - 移行のガイダンス</span><span class="sxs-lookup"><span data-stu-id="4002b-196">Segmented Entry control - Migration guidance</span></span>](segmented-entry-control-migration-guidance.md)




