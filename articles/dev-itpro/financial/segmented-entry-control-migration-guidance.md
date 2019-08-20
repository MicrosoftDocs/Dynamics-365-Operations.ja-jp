---
title: セグメント化されたエントリ コントロールの移行のガイダンス
description: このトピックでは、セグメント化エントリ コントロールを Microsoft Dynamics AX 2012 のパターンから Microsoft Dynamics AX の新しいパターンに移行するプロセスについて説明します。
author: robinarh
manager: AnnBe
ms.date: 11/10/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Developer
ms.reviewer: rhaertle
ms.search.scope: Operations
ms.custom: 25651
ms.assetid: eea675a0-d9d8-453d-9f5a-70c833a7a0d6
ms.search.region: Global
ms.author: ghenriks
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: ccdcbeef63afde1f1e8578d66fe40e69cbe16702
ms.sourcegitcommit: 27a98a7a0f1d2623f5236a88066f483def30889c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/01/2019
ms.locfileid: "1833324"
---
# <a name="migration-guidance-for-segmented-entry-controls"></a><span data-ttu-id="3e8f8-103">セグメント化されたエントリ コントロールに関する移行ガイダンス</span><span class="sxs-lookup"><span data-stu-id="3e8f8-103">Migration guidance for Segmented Entry controls</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="3e8f8-104">このトピックでは、セグメント化エントリ コントロールを Microsoft Dynamics AX 2012 のパターンから Microsoft Dynamics AX の新しいパターンに移行するプロセスについて説明します。</span><span class="sxs-lookup"><span data-stu-id="3e8f8-104">This topic guides you through the process of migrating a Segmented Entry control from the Microsoft Dynamics AX 2012 pattern to the new pattern in Microsoft Dynamics AX.</span></span>

<span data-ttu-id="3e8f8-105">新しい設計の目標は、コントロールの実装をカプセル化し、コントロールをサポートするクラスとやり取りするフォームを必要としないことです。</span><span class="sxs-lookup"><span data-stu-id="3e8f8-105">The goal of the new design is to encapsulate the control implementation and not require that forms interact with the classes that back the control.</span></span> <span data-ttu-id="3e8f8-106">したがって、Microsoft Dynamics AX で、<em>すべてのフォームは、**セグメント化されたエントリ</em>* コントロール インスタンス<em>のアプリケーション プログラミング インターフェイス (API) とのみ対話する必要があります。それらは、コントローラー クラス (\*\*LedgerDimensionAccountController</em>* や <strong>DimensionDynamicAccountController</strong> など) と直接対話してはなりません。</span><span class="sxs-lookup"><span data-stu-id="3e8f8-106">Therefore, in Microsoft Dynamics AX, <em>all forms should interact only with the application programming interface (API) of the \**Segmented Entry</em>* control instance<em>. They should not interact directly with the controller classes (such as \**LedgerDimensionAccountController</em>* and <strong>DimensionDynamicAccountController</strong>).</span></span> <span data-ttu-id="3e8f8-107">コントローラー上で以前に操作または呼び出された任意のプロパティは、コントロール上で呼び出される必要があります。</span><span class="sxs-lookup"><span data-stu-id="3e8f8-107">Any property that was previously manipulated or called on the controller must now be called on the control.</span></span> <span data-ttu-id="3e8f8-108"><strong>メモ :</strong></span><span class="sxs-lookup"><span data-stu-id="3e8f8-108"><strong>Notes:</strong></span></span>

-   <span data-ttu-id="3e8f8-109">一部の API は、コントローラーとコントロールで命名方法が違います。</span><span class="sxs-lookup"><span data-stu-id="3e8f8-109">Some APIs have naming differences between the controller and the control.</span></span> <span data-ttu-id="3e8f8-110">次のテーブルにこれらの API の一覧を示します。</span><span class="sxs-lookup"><span data-stu-id="3e8f8-110">The following table lists these APIs.</span></span>
    <span data-ttu-id="3e8f8-111">**コントローラー メソッド (旧)**
    **コントロール メソッド (新)** parmDate parmControlDate parmFilterLedgerPostingType parmPostingType parmDimensionAccountStorageUsage parmDimensionAccountStorageUsageType</span><span class="sxs-lookup"><span data-stu-id="3e8f8-111">**Controller Method (old)**
    **Control Method (new)** parmDate parmControlDate parmFilterLedgerPostingType parmPostingType parmDimensionAccountStorageUsage parmDimensionAccountStorageUsageType</span></span>
-   <span data-ttu-id="3e8f8-112">**例**</span><span class="sxs-lookup"><span data-stu-id="3e8f8-112">**Example**</span></span>
    -   <span data-ttu-id="3e8f8-113">**以前:** controller.parmDate(systemDateGet())</span><span class="sxs-lookup"><span data-stu-id="3e8f8-113">**Before:** controller.parmDate(systemDateGet())</span></span>
    -   <span data-ttu-id="3e8f8-114">**以後:** LedgerAccount.parmControlDate(systemDateGet());</span><span class="sxs-lookup"><span data-stu-id="3e8f8-114">**After:** LedgerAccount.parmControlDate(systemDateGet());</span></span>

    <span data-ttu-id="3e8f8-115">この例では、**コントローラー** &gt; **LedgerDimensionAccountController** インスタンスと **LedgerAccount** &gt; 新しい**セグメント化エントリ** コントロールのインスタンス</span><span class="sxs-lookup"><span data-stu-id="3e8f8-115">In this example, **controller** &gt; **LedgerDimensionAccountController** instance and **LedgerAccount** &gt; new **Segmented Entry** control instance</span></span>
-   <span data-ttu-id="3e8f8-116">コントロールやデータ フィールドでオーバーライドされたメソッドでは、コード アップグレード ルールが、コントローラーのメソッドの呼び出しを、特定のコントローラーを使用していた各コントロール インスタンスのメソッドの呼び出しに置き換えます。</span><span class="sxs-lookup"><span data-stu-id="3e8f8-116">In methods that have been overridden on controls and data fields, the code upgrade rule replaces method calls on the controllers with method calls on each control instance that was using a particular controller.</span></span> <span data-ttu-id="3e8f8-117">**例**</span><span class="sxs-lookup"><span data-stu-id="3e8f8-117">**Example**</span></span>
    -   <span data-ttu-id="3e8f8-118">**以前:**</span><span class="sxs-lookup"><span data-stu-id="3e8f8-118">**Before:**</span></span>

            Public void jumpRef()
            {
                ledgerDimensionDefaultAccountcontroller.jumpRef();
            }

    -   <span data-ttu-id="3e8f8-119">**以後:**</span><span class="sxs-lookup"><span data-stu-id="3e8f8-119">**After:**</span></span>

            Public void jumpRef()
            {
                segmentedEntryControl1.jumpRef();
                segmentedEntryControl2.jumpRef();
            }

    <span data-ttu-id="3e8f8-120">これらの変更は、他の場所に移動する必要があるコードをコピーして貼り付ける方が簡単になるように行われています (例: **loadSegments()** およびその他の類似メソッドの一部のインスタンス)。</span><span class="sxs-lookup"><span data-stu-id="3e8f8-120">These changes are made so that it's easier to copy and paste code that must be moved elsewhere (for example, in some instances of **loadSegments()** and other such methods).</span></span> <span data-ttu-id="3e8f8-121">メソッドを削除するかどうか決定するときは、この変更を無視することができます。</span><span class="sxs-lookup"><span data-stu-id="3e8f8-121">You can ignore this change when you decide whether the method can be deleted.</span></span> <span data-ttu-id="3e8f8-122">決定内容は、メソッドにカスタム ロジックにあるかどうかによって異なります。</span><span class="sxs-lookup"><span data-stu-id="3e8f8-122">Your decision should depend on whether the method has any custom logic.</span></span>
-   <span data-ttu-id="3e8f8-123">コードのアップグレード スクリプトは、コントローラーがメソッド内でインスタンス化されるケースを処理しません。</span><span class="sxs-lookup"><span data-stu-id="3e8f8-123">The code upgrade script does not handle cases where a controller is instantiated within a method.</span></span> <span data-ttu-id="3e8f8-124">このような場合は、手動で移行する必要があります。</span><span class="sxs-lookup"><span data-stu-id="3e8f8-124">These cases must be migrated manually.</span></span>
-   <span data-ttu-id="3e8f8-125">Microsoft Dynamics AX 2012 の MRU 機能は、Dynamics AX で削除されました。置き換えの予定はありません。</span><span class="sxs-lookup"><span data-stu-id="3e8f8-125">The MRU functionality from Microsoft Dynamics AX 2012 has been removed in Dynamics AX and won't be replaced.</span></span>
-   <span data-ttu-id="3e8f8-126">**parmTaxCode** が削除されました。</span><span class="sxs-lookup"><span data-stu-id="3e8f8-126">**parmTaxCode** has been removed.</span></span> <span data-ttu-id="3e8f8-127">交換はありません。</span><span class="sxs-lookup"><span data-stu-id="3e8f8-127">There is no replacement.</span></span>

## <a name="properties"></a><span data-ttu-id="3e8f8-128">プロパティ</span><span class="sxs-lookup"><span data-stu-id="3e8f8-128">Properties</span></span>
<span data-ttu-id="3e8f8-129">**セグメント化エントリ**コントロールのカスタム プロパティは、**コントローラー**の下にあります。</span><span class="sxs-lookup"><span data-stu-id="3e8f8-129">The custom properties for the **Segmented Entry** control are found under **Controller**.</span></span> <span data-ttu-id="3e8f8-130">次のスクリーン ショットは、例を示します。</span><span class="sxs-lookup"><span data-stu-id="3e8f8-130">The following screen shot shows an example.</span></span> <span data-ttu-id="3e8f8-131">[![111](./media/111.png)](./media/111.png) すべてのプロパティがすべての**コント ローラー**クラス タイプに適用されるわけではありません。</span><span class="sxs-lookup"><span data-stu-id="3e8f8-131">[![111](./media/111.png)](./media/111.png) Not all properties apply to all **Controller** class types.</span></span> <span data-ttu-id="3e8f8-132">選択したコントローラー クラスに適用されないプロパティは無効になります。</span><span class="sxs-lookup"><span data-stu-id="3e8f8-132">Properties that don't apply to a selected controller class will be disabled.</span></span> <span data-ttu-id="3e8f8-133">次のテーブルは、それぞれのプロパティに関する詳細を示します。</span><span class="sxs-lookup"><span data-stu-id="3e8f8-133">The following table provides details about the properties.</span></span>

<span data-ttu-id="3e8f8-134">**プロパティ**</span><span class="sxs-lookup"><span data-stu-id="3e8f8-134">**Property**</span></span>

<span data-ttu-id="3e8f8-135">**有効な値**</span><span class="sxs-lookup"><span data-stu-id="3e8f8-135">**Valid Values**</span></span>

<span data-ttu-id="3e8f8-136">**用途**</span><span class="sxs-lookup"><span data-stu-id="3e8f8-136">**Usage**</span></span>

<span data-ttu-id="3e8f8-137">勘定タイプ フィールド</span><span class="sxs-lookup"><span data-stu-id="3e8f8-137">Account Type Field</span></span>

<span data-ttu-id="3e8f8-138">データ ソースからのフィールド。</span><span class="sxs-lookup"><span data-stu-id="3e8f8-138">A field from the datasource.</span></span>

<span data-ttu-id="3e8f8-139">使用されるアカウントの種類を決定します。</span><span class="sxs-lookup"><span data-stu-id="3e8f8-139">Determines the type of account used.</span></span> <span data-ttu-id="3e8f8-140">通常、複数セグメントの勘定科目から、Cust、Vend、Bank、Project などの他のックアップ テーブルの単一セグメント値への仕訳入力に使用されます。</span><span class="sxs-lookup"><span data-stu-id="3e8f8-140">Typically utilized for journal entry from a multi-segment ledger account to single segment values from other backing tables such as Cust, Vend, Bank, Project and similar.</span></span>

<span data-ttu-id="3e8f8-141">コントローラー クラス</span><span class="sxs-lookup"><span data-stu-id="3e8f8-141">Controller Class</span></span>

<span data-ttu-id="3e8f8-142">6 つのコントローラー クラスのうちの 1 つです。</span><span class="sxs-lookup"><span data-stu-id="3e8f8-142">One of 6 Controller classes.</span></span> <span data-ttu-id="3e8f8-143">たとえば LedgerDimensionDefaultAccountController。</span><span class="sxs-lookup"><span data-stu-id="3e8f8-143">For example LedgerDimensionDefaultAccountController.</span></span>

<span data-ttu-id="3e8f8-144">セグメント化されたエントリ コントロールの動作およびパターンを決定します。</span><span class="sxs-lookup"><span data-stu-id="3e8f8-144">Determines the pattern and behavior of the Segmented Entry control.</span></span> <span data-ttu-id="3e8f8-145">このプロパティの詳細については以下で説明します。</span><span class="sxs-lookup"><span data-stu-id="3e8f8-145">More information about this property is provided below.</span></span>

<span data-ttu-id="3e8f8-146">財務勘定を含む</span><span class="sxs-lookup"><span data-stu-id="3e8f8-146">Include Financial Accounts</span></span>

<span data-ttu-id="3e8f8-147">NoYes</span><span class="sxs-lookup"><span data-stu-id="3e8f8-147">NoYes</span></span>

<span data-ttu-id="3e8f8-148">財務勘定である主勘定が有効であるかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="3e8f8-148">Determines if Main accounts that are Financial accounts are valid for use.</span></span>

<span data-ttu-id="3e8f8-149">勘定合計を含む</span><span class="sxs-lookup"><span data-stu-id="3e8f8-149">Include Total Accounts</span></span>

<span data-ttu-id="3e8f8-150">NoYes</span><span class="sxs-lookup"><span data-stu-id="3e8f8-150">NoYes</span></span>

<span data-ttu-id="3e8f8-151">タイプが "合計" の主勘定が有効であるかどうかを判断します。</span><span class="sxs-lookup"><span data-stu-id="3e8f8-151">Determines if Main accounts of type Total are valid for use.</span></span>

<span data-ttu-id="3e8f8-152">既定の勘定です。</span><span class="sxs-lookup"><span data-stu-id="3e8f8-152">Is Default Account</span></span>

<span data-ttu-id="3e8f8-153">TrueFalse</span><span class="sxs-lookup"><span data-stu-id="3e8f8-153">TrueFalse</span></span>

<span data-ttu-id="3e8f8-154">動的アカウントで、アカウントが既定または完全アカウントであるべきかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="3e8f8-154">For a Dynamic account, determines if the account should be a default or full account.</span></span>

<span data-ttu-id="3e8f8-155">主勘定セグメントのロック</span><span class="sxs-lookup"><span data-stu-id="3e8f8-155">Lock Main Account Segment</span></span>

<span data-ttu-id="3e8f8-156">NoYes</span><span class="sxs-lookup"><span data-stu-id="3e8f8-156">NoYes</span></span>

<span data-ttu-id="3e8f8-157">主勘定セグメントがロックされているかどうかをコントロールします。</span><span class="sxs-lookup"><span data-stu-id="3e8f8-157">Controls whether the Main account segment is locked.</span></span> <span data-ttu-id="3e8f8-158">通常は仕訳帳や構成に基づく配分に使用されます。</span><span class="sxs-lookup"><span data-stu-id="3e8f8-158">Typically used in journals and distributions based upon configuration.</span></span>

<span data-ttu-id="3e8f8-159">転記タイプ</span><span class="sxs-lookup"><span data-stu-id="3e8f8-159">Posting Type</span></span>

<span data-ttu-id="3e8f8-160">LedgerPostingType 列挙の値。</span><span class="sxs-lookup"><span data-stu-id="3e8f8-160">A value from the LedgerPostingType enumeration.</span></span>

<span data-ttu-id="3e8f8-161">主勘定が検証され、そのアカウントで使用される転記タイプが許可されているかどうかを確認されます。</span><span class="sxs-lookup"><span data-stu-id="3e8f8-161">The Main account is validated to see if the posting type is allowed to be used with that account.</span></span>

<span data-ttu-id="3e8f8-162">手動入力のブロック状態の検証</span><span class="sxs-lookup"><span data-stu-id="3e8f8-162">Validate Blocked For Manual Entry</span></span>

<span data-ttu-id="3e8f8-163">NoYes</span><span class="sxs-lookup"><span data-stu-id="3e8f8-163">NoYes</span></span>

<span data-ttu-id="3e8f8-164">分析コードの「手動入力のブロック」ステータスを優先するかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="3e8f8-164">Determines if the 'Blocked for Manual Entry' status on the dimension should be respected or not.</span></span>

## <a name="controller-class-property"></a><span data-ttu-id="3e8f8-165">コントローラー クラス プロパティ</span><span class="sxs-lookup"><span data-stu-id="3e8f8-165">Controller class property</span></span>
<span data-ttu-id="3e8f8-166">次のテーブルは、それぞれのコントローラーに関する詳細を示します。</span><span class="sxs-lookup"><span data-stu-id="3e8f8-166">The following table provides details about each controller.</span></span>

<span data-ttu-id="3e8f8-167">**コントローラー**</span><span class="sxs-lookup"><span data-stu-id="3e8f8-167">**Controller**</span></span>

<span data-ttu-id="3e8f8-168">**詳細**</span><span class="sxs-lookup"><span data-stu-id="3e8f8-168">**Details**</span></span>

<span data-ttu-id="3e8f8-169">BudgetLedgerDimension</span><span class="sxs-lookup"><span data-stu-id="3e8f8-169">BudgetLedgerDimension</span></span>

<span data-ttu-id="3e8f8-170">このコントローラーは、セグメント化された入力コントロールのデータ入力の予算に基づくサポートを提供します。</span><span class="sxs-lookup"><span data-stu-id="3e8f8-170">This Controller provides budget based support for data entry in the Segmented Entry control.</span></span> <span data-ttu-id="3e8f8-171">このコント ローラーを使用するときは、勘定構造をセグメント化エントリ コントロールに提供する必要があります。</span><span class="sxs-lookup"><span data-stu-id="3e8f8-171">When using this controller, an Account Structure must be provided to the Segmented Entry control.</span></span>

<span data-ttu-id="3e8f8-172">BudgetPlanningLedgerDimension</span><span class="sxs-lookup"><span data-stu-id="3e8f8-172">BudgetPlanningLedgerDimension</span></span>

<span data-ttu-id="3e8f8-173">このコントローラーは、セグメント化された入力コントロールのデータ入力の予算計画に基づくサポートを提供します。</span><span class="sxs-lookup"><span data-stu-id="3e8f8-173">This Controller provides budget planning based support for data entry in the Segmented Entry control.</span></span> <span data-ttu-id="3e8f8-174">このコント ローラーを使用するときは、勘定構造をセグメント化エントリ コントロールに提供する必要があります。</span><span class="sxs-lookup"><span data-stu-id="3e8f8-174">When using this controller, an Account Structure must be provided to the Segmented Entry control.</span></span>

<span data-ttu-id="3e8f8-175">DimensionDynamicAccount</span><span class="sxs-lookup"><span data-stu-id="3e8f8-175">DimensionDynamicAccount</span></span>

<span data-ttu-id="3e8f8-176">このコントローラーは、セグメント化された入力コントロールの複数のアカウント タイプのサポートを提供します。</span><span class="sxs-lookup"><span data-stu-id="3e8f8-176">This Controller provides support for multiple account types in the Segmented Entry control.</span></span>

<span data-ttu-id="3e8f8-177">LedgerDimensionAccountAlias</span><span class="sxs-lookup"><span data-stu-id="3e8f8-177">LedgerDimensionAccountAlias</span></span>

<span data-ttu-id="3e8f8-178">このコントローラーは、セグメント化された入力コントロールのアカウント エイリアスのサポートを提供します。</span><span class="sxs-lookup"><span data-stu-id="3e8f8-178">This Controller provides support for account aliases in the Segmented Entry control</span></span>

<span data-ttu-id="3e8f8-179">LedgerDimensionAccount</span><span class="sxs-lookup"><span data-stu-id="3e8f8-179">LedgerDimensionAccount</span></span>

<span data-ttu-id="3e8f8-180">このコントローラーは、セグメント化された入力コントロールの複数のセグメントのデータ入力のサポートを提供します。</span><span class="sxs-lookup"><span data-stu-id="3e8f8-180">This Controller provides support for multi-segment data entry in the Segmented Entry control.</span></span>

<span data-ttu-id="3e8f8-181">LedgerDimensionDefaultAccount</span><span class="sxs-lookup"><span data-stu-id="3e8f8-181">LedgerDimensionDefaultAccount</span></span>

<span data-ttu-id="3e8f8-182">このコントローラーは、セグメント化された入力コントロールの既定のアカウントのサポートを提供します。</span><span class="sxs-lookup"><span data-stu-id="3e8f8-182">This Controller provides support for default accounts in the Segmented Entry control.</span></span>

## <a name="migration-steps"></a><span data-ttu-id="3e8f8-183">移行ステップ</span><span class="sxs-lookup"><span data-stu-id="3e8f8-183">Migration steps</span></span>
### <a name="step-1"></a><span data-ttu-id="3e8f8-184">ステップ１</span><span class="sxs-lookup"><span data-stu-id="3e8f8-184">Step 1</span></span>

#### <a name="ax-2012"></a><span data-ttu-id="3e8f8-185">AX 2012</span><span class="sxs-lookup"><span data-stu-id="3e8f8-185">AX 2012</span></span>

<span data-ttu-id="3e8f8-186">**SegmentedEntry** は任意のコントロールの横にあるタイプとして表示され、**SegmentedEntryControl** と変更します。</span><span class="sxs-lookup"><span data-stu-id="3e8f8-186">If **SegmentedEntry** appears as the type next to any control, change it to **SegmentedEntryControl**.</span></span> <span data-ttu-id="3e8f8-187">[![SegmentMigrate01](./media/segmentmigrate01.png)](./media/segmentmigrate01.png)</span><span class="sxs-lookup"><span data-stu-id="3e8f8-187">[![SegmentMigrate01](./media/segmentmigrate01.png)](./media/segmentmigrate01.png)</span></span>

#### <a name="dynamics-ax"></a><span data-ttu-id="3e8f8-188">Dynamics AX</span><span class="sxs-lookup"><span data-stu-id="3e8f8-188">Dynamics AX</span></span>

<span data-ttu-id="3e8f8-189">簡単な方法は古いコントロールの名前に「\_旧」を追加し、新しいコントロール (コントロールの元の名前がある必要があります) を付け加え、すべての設定を移行した後、古いコントロールを削除します。</span><span class="sxs-lookup"><span data-stu-id="3e8f8-189">An easy method is to append "\_old" to the name of the old control, add the new control (which should have the original name of the control), migrate all the settings over, and then delete the old control.</span></span> <span data-ttu-id="3e8f8-190">**注記:** コントロールを参照するテストおよび他のコードが破損しないようにするには、新しいコントロールが古いコントロールと同じ名前であることを確認します。</span><span class="sxs-lookup"><span data-stu-id="3e8f8-190">**Note:** To prevent tests and other code that references the control from breaking, make sure that the new control has the same name as the old control.</span></span> <span data-ttu-id="3e8f8-191">新しいコントロールを追加するには、**Segmented Entry** コントロールを含む親コントロールを右クリックし、**New** &gt; **SegmentedEntryControl** を選択します。</span><span class="sxs-lookup"><span data-stu-id="3e8f8-191">To add the new control, right-click the parent control that will contain the **Segmented Entry** control, and then select **New** &gt; **SegmentedEntryControl**.</span></span> <span data-ttu-id="3e8f8-192">[![SegmentMigrate02](./media/segmentmigrate02-623x1024.png)](./media/segmentmigrate02.png) 次のスクリーンショットは、新しいコントロールの外観を示しています。</span><span class="sxs-lookup"><span data-stu-id="3e8f8-192">[![SegmentMigrate02](./media/segmentmigrate02-623x1024.png)](./media/segmentmigrate02.png) The following screen shot shows how new control will look.</span></span> <span data-ttu-id="3e8f8-193">[![SegmentMigrate03](./media/segmentmigrate03.png)](./media/segmentmigrate03.png)</span><span class="sxs-lookup"><span data-stu-id="3e8f8-193">[![SegmentMigrate03](./media/segmentmigrate03.png)](./media/segmentmigrate03.png)</span></span>

### <a name="step-2"></a><span data-ttu-id="3e8f8-194">ステップ２</span><span class="sxs-lookup"><span data-stu-id="3e8f8-194">Step 2</span></span>

#### <a name="ax-2012"></a><span data-ttu-id="3e8f8-195">AX 2012</span><span class="sxs-lookup"><span data-stu-id="3e8f8-195">AX 2012</span></span>

<span data-ttu-id="3e8f8-196"> **jumpRef()** コントロール/メソッドをオーバーライドします。</span><span class="sxs-lookup"><span data-stu-id="3e8f8-196">Override the  **jumpRef()** control/field method.</span></span>

    public void jumpRef()
    {
        ledgerDimensionDefaultAccountController.jumpRef();
    }

#### <a name="dynamics-ax"></a><span data-ttu-id="3e8f8-197">Dynamics AX</span><span class="sxs-lookup"><span data-stu-id="3e8f8-197">Dynamics AX</span></span>

<span data-ttu-id="3e8f8-198">他の機能が含まれなくなった場合は **jumpRef()** メソッドを完全に削除します。</span><span class="sxs-lookup"><span data-stu-id="3e8f8-198">Remove the **jumpRef()** method completely if it contains no other functionality.</span></span> <span data-ttu-id="3e8f8-199">その他のカスタム **jumpRef** 機能がある場合は、それをそのままにします。</span><span class="sxs-lookup"><span data-stu-id="3e8f8-199">If there is other custom **jumpRef** functionality, leave that.</span></span> <span data-ttu-id="3e8f8-200">ただし、**jumpRef** がコントロールによって自動的に処理されます。</span><span class="sxs-lookup"><span data-stu-id="3e8f8-200">However, **jumpRef** is otherwise automatically handled by the control.</span></span>

### <a name="step-3"></a><span data-ttu-id="3e8f8-201">ステップ 3</span><span class="sxs-lookup"><span data-stu-id="3e8f8-201">Step 3</span></span>

#### <a name="ax-2012"></a><span data-ttu-id="3e8f8-202">AX 2012</span><span class="sxs-lookup"><span data-stu-id="3e8f8-202">AX 2012</span></span>

<span data-ttu-id="3e8f8-203">**loadAutoCompleteData()** コントロール メソッドをオーバーライドします。</span><span class="sxs-lookup"><span data-stu-id="3e8f8-203">Override the **loadAutoCompleteData()** control method.</span></span>

    public void loadAutoCompleteData(LoadAutoCompleteDataEventArgs _e)
    {
        ledgerDimensionDefaultAccountController.loadAutoCompleteData(_e);
        super(_e);
    }

#### <a name="dynamics-ax"></a><span data-ttu-id="3e8f8-204">Dynamics AX</span><span class="sxs-lookup"><span data-stu-id="3e8f8-204">Dynamics AX</span></span>

<span data-ttu-id="3e8f8-205">**loadAutoCompleteData()** メソッドを削除します。</span><span class="sxs-lookup"><span data-stu-id="3e8f8-205">Remove the **loadAutoCompleteData()** method.</span></span>

### <a name="step-4"></a><span data-ttu-id="3e8f8-206">ステップ 4</span><span class="sxs-lookup"><span data-stu-id="3e8f8-206">Step 4</span></span>

#### <a name="ax-2012"></a><span data-ttu-id="3e8f8-207">AX 2012</span><span class="sxs-lookup"><span data-stu-id="3e8f8-207">AX 2012</span></span>

<span data-ttu-id="3e8f8-208">**loadSegments()** コントロール メソッドをオーバーライドします。</span><span class="sxs-lookup"><span data-stu-id="3e8f8-208">Override the **loadSegments()** control method.</span></span>

    public void loadSegments()
    {
        super();
        ledgerDimensionDefaultAccountController.loadSegments();
        ledgerDimensionDefaultAccountController.parmControl(this);
    }

#### <a name="dynamics-ax"></a><span data-ttu-id="3e8f8-209">Dynamics AX</span><span class="sxs-lookup"><span data-stu-id="3e8f8-209">Dynamics AX</span></span>

<span data-ttu-id="3e8f8-210">**loadSegments()** メソッドが、コントローラーの **loadSegments()** および **parmControl()** メソッドを呼ぶ以外に何もしない場合は、それを削除します。</span><span class="sxs-lookup"><span data-stu-id="3e8f8-210">If the **loadSegments()** method does nothing except call the controller's **loadSegments()** and **parmControl()** methods, remove it.</span></span> <span data-ttu-id="3e8f8-211">ただし、**parmControl()** 呼び出しに渡される SEC コントロール インスタンスをメモしておきます。</span><span class="sxs-lookup"><span data-stu-id="3e8f8-211">However, make a note of the SEC control instance that is passed to the **parmControl()** call.</span></span> <span data-ttu-id="3e8f8-212">呼び出されていたメソッドは、そのインスタンスで呼び出される必要があります。</span><span class="sxs-lookup"><span data-stu-id="3e8f8-212">The methods that were being called will now have to be called on that instance.</span></span>

### <a name="step-5"></a><span data-ttu-id="3e8f8-213">ステップ 5</span><span class="sxs-lookup"><span data-stu-id="3e8f8-213">Step 5</span></span>

#### <a name="ax-2012"></a><span data-ttu-id="3e8f8-214">AX 2012</span><span class="sxs-lookup"><span data-stu-id="3e8f8-214">AX 2012</span></span>

<span data-ttu-id="3e8f8-215">**loadSegments()** コントロール メソッドをオーバーライドします。</span><span class="sxs-lookup"><span data-stu-id="3e8f8-215">Override the **loadSegments()** control method.</span></span>

    public void loadSegments()
    {
        super();
        dimAccountController.parmControl(this);
        dimAccountController.parmJournalName(ledgerJournalTable.JournalName);
        dimAccountController.parmCurrency(ledgerJournalTrans.CurrencyCode);
        dimAccountController.parmDataAreaId(ledgerJournalTrans.Company ? ledgerJournalTrans.Company : curext());
        dimAccountController.parmDate(ledgerJournalTrans.TransDate);
        dimAccountController.parmTaxCode(ledgerJournalTrans.TaxCode);

        dimAccountController.loadSegments();
    }

#### <a name="dynamics-ax"></a><span data-ttu-id="3e8f8-216">Dynamics AX</span><span class="sxs-lookup"><span data-stu-id="3e8f8-216">Dynamics AX</span></span>

<span data-ttu-id="3e8f8-217">**loadSegments()** メソッドがコントローラーでのパラメーターを設定するために使用された場合、**パラメーター** メソッドへの呼び出しは、**パラメーター** メソッドのソースを変更することができるすべての場所に移動する必要があります。</span><span class="sxs-lookup"><span data-stu-id="3e8f8-217">If the **loadSegments()** method was used to set parameters on the controller, the calls to **parm** method must be moved to every location where the source of the **parm** method can change.</span></span> <span data-ttu-id="3e8f8-218">ほとんどの場合、これらの場所は対応するデータ フィールドの **modified()** メソッドおよび/またはデータ ソースの **active()** メソッドです。</span><span class="sxs-lookup"><span data-stu-id="3e8f8-218">In most cases, these locations are the **modified()** method on the corresponding data field and/or the **active()** method on the data source.</span></span> <span data-ttu-id="3e8f8-219">たとえば、**loadSegments()** の移行したコードの一部は、左側で上書きをし、次のようになります。</span><span class="sxs-lookup"><span data-stu-id="3e8f8-219">For example, some of the migrated code for the **loadSegments()** override on the left would look like this.</span></span>

    dimAccountController.parmControl(this) -> No longer needed.

<span data-ttu-id="3e8f8-220">**parmControl()** 呼び出しに渡される SEC コントロール インスタンスをメモしておきます。</span><span class="sxs-lookup"><span data-stu-id="3e8f8-220">Make a note of the SEC control instance that is passed on to the **parmControl()** call.</span></span> <span data-ttu-id="3e8f8-221">コントローラー上で呼び出されていたメソッドは、そのインスタンスで呼び出される必要があります。</span><span class="sxs-lookup"><span data-stu-id="3e8f8-221">The methods that were being called on the controller will now have to be called on that instance.</span></span>

    dimAccountController.parmJournalName(ledgerJournalTable.JournalName) ->
    LedgerJournalTable data source,
    JournalName field,
    public void modified()
    {
        .parmJournalName(ledgerJournalTable.JournalName);
    }

<span data-ttu-id="3e8f8-222">**LedgerJournalTable データ ソース**</span><span class="sxs-lookup"><span data-stu-id="3e8f8-222">**LedgerJournalTable data source**</span></span>

    public void active()
    {
        .parmJournalName(ledgerJournalTable.JournalName);
    }

<span data-ttu-id="3e8f8-223">**注記:** **loadSegments()** メソッドからすべてのコードを削除したら、そのメソッドを削除できます。</span><span class="sxs-lookup"><span data-stu-id="3e8f8-223">**Note:** After you've moved all the code out of the **loadSegments()** method, you can delete the method.</span></span>

### <a name="step-6"></a><span data-ttu-id="3e8f8-224">ステップ 6</span><span class="sxs-lookup"><span data-stu-id="3e8f8-224">Step 6</span></span>

#### <a name="ax-2012"></a><span data-ttu-id="3e8f8-225">AX 2012</span><span class="sxs-lookup"><span data-stu-id="3e8f8-225">AX 2012</span></span>

<span data-ttu-id="3e8f8-226">**loadSegments()** コントロール メソッドをオーバーライドします。</span><span class="sxs-lookup"><span data-stu-id="3e8f8-226">Override the **loadSegments()** control method.</span></span> <span data-ttu-id="3e8f8-227">場合によっては、**loadSegments()** メソッドは、テーブル バッファを使用してコントローラーでパラメーターを設定することがありますが、そのテーブル バッファはフォーム上のデータ ソースではありません。</span><span class="sxs-lookup"><span data-stu-id="3e8f8-227">In some cases, the **loadSegments()** method might use a table buffer to set parameters on the controller, but that table buffer isn't a data source on the form.</span></span> <span data-ttu-id="3e8f8-228">たとえば、**LedgerJournalTransDaily** フォームでは、**loadSegments()** の元の実装は次のようになります。</span><span class="sxs-lookup"><span data-stu-id="3e8f8-228">For example, on the **LedgerJournalTransDaily** form, the original implementation of **loadSegments()** looked like this.</span></span>

    public void loadSegments()
    {
        super();

        dimAccountController.parmControl(this);
        dimAccountController.parmJournalName(ledgerJournalTable.JournalName);
        dimAccountController.parmCurrency(ledgerJournalTrans.CurrencyCode);
        dimAccountController.parmDataAreaId(ledgerJournalTrans.Company ? ledgerJournalTrans.Company : curext());
        dimAccountController.parmDate(ledgerJournalTrans.TransDate);
        dimAccountController.parmTaxCode(ledgerJournalTrans.TaxCode);

        dimAccountController.loadSegments();

        currentMainAccountId = dimAccountController.getValue(DimensionAttribute::getMainAccountDimensionAttribute());
    }

<span data-ttu-id="3e8f8-229">**JournalName** プロパティは、ledgerJournalTable バッファから設定されますが、LedgerJournalTable テーブルはフォームのデータ ソースではないことに注意してください。</span><span class="sxs-lookup"><span data-stu-id="3e8f8-229">Note that the **JournalName** property is set from the ledgerJournalTable buffer, but the LedgerJournalTable table isn't a data source on the form.</span></span>

#### <a name="dynamics-ax"></a><span data-ttu-id="3e8f8-230">Dynamics AX</span><span class="sxs-lookup"><span data-stu-id="3e8f8-230">Dynamics AX</span></span>

<span data-ttu-id="3e8f8-231">このような場合、そのコードをデータ ソースの **active()** メソッド、またはデータ フィールドの **modified()** メソッドに移動できません。</span><span class="sxs-lookup"><span data-stu-id="3e8f8-231">In such cases, you can't move that code to either the **active()** method of a data source or the **modified()** method on the data field.</span></span> <span data-ttu-id="3e8f8-232">代わりに、テーブル バッファが設定されている場所を特定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="3e8f8-232">Instead, you should identify where the table buffer is being set.</span></span> <span data-ttu-id="3e8f8-233">たとえば、**LedgerJournalTransDaily** フォームの元の実装では、ledgerJournalTable バッファはフォームの **initLedger()** メソッドで設定されました。</span><span class="sxs-lookup"><span data-stu-id="3e8f8-233">For example, in the original implementation of the **LedgerJournalTransDaily** form, the ledgerJournalTable buffer was set in the **initLedger()** method on the form.</span></span> <span data-ttu-id="3e8f8-234">**parmJournalName()** に渡される値は、バッファが **initLedger()** メソッドで再割り当てされる場合のみ変更できることを明らかにする必要があります。</span><span class="sxs-lookup"><span data-stu-id="3e8f8-234">It should be evident that the value that is passed to **parmJournalName()** can change only when the buffer is reassigned in the **initLedger()** method.</span></span> <span data-ttu-id="3e8f8-235">したがって、バッファを割り当てた後、コードを **initLedger()** メソッドに移動する必要があります。</span><span class="sxs-lookup"><span data-stu-id="3e8f8-235">Therefore, code would have to be moved to the **initLedger()** method after the assignment of the buffer.</span></span> <span data-ttu-id="3e8f8-236">また、一般的なガイドラインに従って、コントロールインスタンスに対して **parmJournalName()** メソッドが呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="3e8f8-236">Also, in accordance with the general guidelines, the **parmJournalName()** method would be called on the control instance.</span></span>

    void initLedger()
    {
        TransDate   dateFrom   = dateNull();
        TransDate   dateTo     = systemDateGet();

        if (element.args().dataset() == tableNum(LedgerJournalTable))
        {
            ledgerJournalTable = element.args().record();
            LedgerJournalTrans_AccountNum.parmJournalName(ledgerJournalTable.JournalName);
            LedgerJournalTrans_AccountNum1.parmJournalName(ledgerJournalTable.JournalName);
            GridOffsetAccount.parmJournalName(ledgerJournalTable.JournalName);
            LedgerJournalTrans_OffsetAccount1.parmJournalName(ledgerJournalTable.JournalName);
            ...
        }
        ...
    }

### <a name="step-7"></a><span data-ttu-id="3e8f8-237">ステップ 7</span><span class="sxs-lookup"><span data-stu-id="3e8f8-237">Step 7</span></span>

#### <a name="ax-2012"></a><span data-ttu-id="3e8f8-238">AX 2012</span><span class="sxs-lookup"><span data-stu-id="3e8f8-238">AX 2012</span></span>

<span data-ttu-id="3e8f8-239">**segmentValueChanged()** コントロール メソッドをオーバーライドします。</span><span class="sxs-lookup"><span data-stu-id="3e8f8-239">Override the **segmentValueChanged()** control method.</span></span>

    public void segmentValueChanged(SegmentValueChangedEventArgs _e)
    {
        super(_e);
        ledgerDimensionDefaultAccountController.segmentValueChanged(_e);
    }

#### <a name="dynamics-ax"></a><span data-ttu-id="3e8f8-240">Dynamics AX</span><span class="sxs-lookup"><span data-stu-id="3e8f8-240">Dynamics AX</span></span>

<span data-ttu-id="3e8f8-241">**segmentValueChanged()** を実装した場合に、コントローラー上で **super()** と **segmentValueChanged()** メソッドを呼び出す以外何も起こらない場合は、メソッドを削除することができます。</span><span class="sxs-lookup"><span data-stu-id="3e8f8-241">If the implementation of **segmentValueChanged()** does nothing except call **super()** and the **segmentValueChanged()** method on the controller, you can remove the method.</span></span>

### <a name="step-8"></a><span data-ttu-id="3e8f8-242">ステップ 8</span><span class="sxs-lookup"><span data-stu-id="3e8f8-242">Step 8</span></span>

#### <a name="ax-2012"></a><span data-ttu-id="3e8f8-243">AX 2012</span><span class="sxs-lookup"><span data-stu-id="3e8f8-243">AX 2012</span></span>

<span data-ttu-id="3e8f8-244">**segmentValueChanged()** コントロール メソッドをオーバーライドします。</span><span class="sxs-lookup"><span data-stu-id="3e8f8-244">Override the **segmentValueChanged()** control method.</span></span>

    public void segmentValueChanged(SegmentValueChangedEventArgs _e)
    {
        super(_e);

        dimOffsetAccountController.segmentValueChanged(_e);
        currentOffsetMainAccountId = ledgerJournalEngine.onOffsetAccountSegmentChanged(dimOffsetAccountController, currentOffsetMainAccountId, ledgerJournalTrans);
    }

#### <a name="dynamics-ax"></a><span data-ttu-id="3e8f8-245">Dynamics AX</span><span class="sxs-lookup"><span data-stu-id="3e8f8-245">Dynamics AX</span></span>

<span data-ttu-id="3e8f8-246">**segmentValueChanged()** の実装に追加のロジックがある場合、次に示すように、メソッドを **onSegmentChanged()** メソッドに置き換える必要があります。</span><span class="sxs-lookup"><span data-stu-id="3e8f8-246">If the implementation of **segmentValueChanged()** has additional logic, you must replace the method with the **onSegmentChanged()** method, as shown here.</span></span>

    public void onSegmentChanged(DimensionControlSegment _segment)
    {
        currentOffsetMainAccountId = ledgerJournalEngine.onOffsetAccountSegmentChanged(this, currentOffsetMainAccountId, ledgerJournalTrans);
    }

<span data-ttu-id="3e8f8-247">**メモ :**</span><span class="sxs-lookup"><span data-stu-id="3e8f8-247">**Notes:**</span></span>

-   <span data-ttu-id="3e8f8-248">**onSegmentChanged()** メソッドを追加するには、次の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="3e8f8-248">To add the **onSegmentChanged()** method, follow these steps:</span></span>
    1.  <span data-ttu-id="3e8f8-249">メソッドを追加するには、**セグメント化されたエントリ**コントロールを展開します。</span><span class="sxs-lookup"><span data-stu-id="3e8f8-249">Expand the **Segmented Entry** control to add the method to.</span></span>
    2.  <span data-ttu-id="3e8f8-250">**メソッド** ノードをクリックし、**オーバーライド** &gt; **onSegmentChanged** を選択します。</span><span class="sxs-lookup"><span data-stu-id="3e8f8-250">Right-click the **Methods** node, and then select **Override** &gt; **onSegmentChanged**.</span></span>
-   <span data-ttu-id="3e8f8-251">新しいメソッドは、**super()** またはコントロールまたはコントローラーのいずれかの他のメソッドを呼び出す必要はありません。</span><span class="sxs-lookup"><span data-stu-id="3e8f8-251">The new method doesn't have to call **super()** or any other method on either the control or the controller.</span></span>

### <a name="step-9"></a><span data-ttu-id="3e8f8-252">ステップ 9</span><span class="sxs-lookup"><span data-stu-id="3e8f8-252">Step 9</span></span>

#### <a name="ax-2012"></a><span data-ttu-id="3e8f8-253">AX 2012</span><span class="sxs-lookup"><span data-stu-id="3e8f8-253">AX 2012</span></span>

<span data-ttu-id="3e8f8-254">**validate()** コントロール メソッドをオーバーライドします。</span><span class="sxs-lookup"><span data-stu-id="3e8f8-254">Override the **validate()** control method.</span></span>

    public boolean validate()
    {
        boolean isValid;
        isValid = super();
        isValid = ledgerDimensionDefaultAccountController.validate() && isValid;

        return isValid;
    }

#### <a name="dynamics-ax"></a><span data-ttu-id="3e8f8-255">Dynamics AX</span><span class="sxs-lookup"><span data-stu-id="3e8f8-255">Dynamics AX</span></span>

<span data-ttu-id="3e8f8-256">追加の検証がある場合以外は、**validate()** メソッドを削除します。</span><span class="sxs-lookup"><span data-stu-id="3e8f8-256">Remove the **validate()** method, unless you have additional validation.</span></span> <span data-ttu-id="3e8f8-257">**super()** 呼び出しは、このコードが行っていたすべてのことを行います。</span><span class="sxs-lookup"><span data-stu-id="3e8f8-257">The **super()** call does everything that this code used to do.</span></span> <span data-ttu-id="3e8f8-258">したがって、保持している新しいコードのみを残しておいてください。</span><span class="sxs-lookup"><span data-stu-id="3e8f8-258">Therefore, keep only any new code that you have.</span></span>

### <a name="step-10"></a><span data-ttu-id="3e8f8-259">ステップ 10</span><span class="sxs-lookup"><span data-stu-id="3e8f8-259">Step 10</span></span>

#### <a name="ax-2012"></a><span data-ttu-id="3e8f8-260">AX 2012</span><span class="sxs-lookup"><span data-stu-id="3e8f8-260">AX 2012</span></span>

<span data-ttu-id="3e8f8-261">**lookup()** コントロール メソッドをオーバーライドします。</span><span class="sxs-lookup"><span data-stu-id="3e8f8-261">Override the **lookup()** control method.</span></span>

    public void lookup()
    {
        switch (emplParameters_RU.BankCloseACType)
        {
        case LedgerJournalACType::Bank:
            BankAccountTable::lookupBankAccount(this);
            break;
        case LedgerJournalACType::Cust:
            CustTable::lookupCustomer(this);
            break;
        case LedgerJournalACType::FixedAssets:
            AssetTable::lookupAccountNum(this);
            break;
        case LedgerJournalACType::Ledger:
            super();
            break;
        case LedgerJournalACType::Project:
            ProjTable::lookupProjId(this, emplParameters_RU);
            break;
        case LedgerJournalACType::Vend:
            VendTable::lookupVendor(this);
            break;
        default:
            super();
            break;
        }
    }

#### <a name="dynamics-ax"></a><span data-ttu-id="3e8f8-262">Dynamics AX</span><span class="sxs-lookup"><span data-stu-id="3e8f8-262">Dynamics AX</span></span>

<span data-ttu-id="3e8f8-263">**lookup()** メソッドをそのままにします。</span><span class="sxs-lookup"><span data-stu-id="3e8f8-263">Leave the **lookup()** method as it is.</span></span>

### <a name="step-11"></a><span data-ttu-id="3e8f8-264">ステップ 11</span><span class="sxs-lookup"><span data-stu-id="3e8f8-264">Step 11</span></span>

#### <a name="ax-2012"></a><span data-ttu-id="3e8f8-265">AX 2012</span><span class="sxs-lookup"><span data-stu-id="3e8f8-265">AX 2012</span></span>

<span data-ttu-id="3e8f8-266"> **lookupReference()** コントロール メソッドをオーバーライドします。</span><span class="sxs-lookup"><span data-stu-id="3e8f8-266">Override the **lookupReference()** control method.</span></span>

    public Common lookupReference()
    {
        Common ret;
        ret = super();
        return ret;
    }

#### <a name="dynamics-ax"></a><span data-ttu-id="3e8f8-267">Dynamics AX</span><span class="sxs-lookup"><span data-stu-id="3e8f8-267">Dynamics AX</span></span>

<span data-ttu-id="3e8f8-268">**lookupReference()** メソッドが既定の実装を使用している場合、それを削除することができます。</span><span class="sxs-lookup"><span data-stu-id="3e8f8-268">If the **lookupReference()** method uses the default implementation, you can delete it.</span></span>

### <a name="step-12"></a><span data-ttu-id="3e8f8-269">ステップ 12</span><span class="sxs-lookup"><span data-stu-id="3e8f8-269">Step 12</span></span>

#### <a name="ax-2012"></a><span data-ttu-id="3e8f8-270">AX 2012</span><span class="sxs-lookup"><span data-stu-id="3e8f8-270">AX 2012</span></span>

<span data-ttu-id="3e8f8-271">**modified()** コントロール メソッドをオーバーライドします。</span><span class="sxs-lookup"><span data-stu-id="3e8f8-271">Override the **modified()** control method.</span></span>

    public boolean modified()
    {
        boolean ret;

        ret = super();

        if (tmpCurrencyLedgerGainLossAccount.LedgerDimension)
        {
            tmpCurrencyLedgerGainLossAccount.AccountName =
            MainAccount::getLocalizedNameByMainAccountId(
            DimensionStorage::getMainAccountNumFromLedgerDimension(
            tmpCurrencyLedgerGainLossAccount.LedgerDimension), ledger.ChartOfAccounts);
        }
        else
        {
            tmpCurrencyLedgerGainLossAccount.AccountName = '';
        }

        return ret;
    }

#### <a name="dynamics-ax"></a><span data-ttu-id="3e8f8-272">Dynamics AX</span><span class="sxs-lookup"><span data-stu-id="3e8f8-272">Dynamics AX</span></span>

<span data-ttu-id="3e8f8-273">**modified()** メソッドをそのままにします。</span><span class="sxs-lookup"><span data-stu-id="3e8f8-273">Leave the **modified()** method as it is.</span></span>

### <a name="step-13"></a><span data-ttu-id="3e8f8-274">ステップ 13</span><span class="sxs-lookup"><span data-stu-id="3e8f8-274">Step 13</span></span>

#### <a name="ax-2012"></a><span data-ttu-id="3e8f8-275">AX 2012</span><span class="sxs-lookup"><span data-stu-id="3e8f8-275">AX 2012</span></span>

<span data-ttu-id="3e8f8-276">**gotFocus()** コントロール メソッドをオーバーライドします。</span><span class="sxs-lookup"><span data-stu-id="3e8f8-276">Override the **gotFocus()** control method.</span></span>

    void gotFocus()
    {
        super();
        if (ledgerJournalTable.FixedOffsetAccount)
        {
            ledgerJournalTrans_OffsetAccount.allowEdit(ledgerJournalTrans.OffsetAccountType == LedgerJournalACType::Ledger);
        }
        else if (!ledgerJournalTrans_OffsetAccount.allowEdit())
        {
            ledgerJournalTrans_OffsetAccount.allowEdit(true);
        }
    }

#### <a name="dynamics-ax"></a><span data-ttu-id="3e8f8-277">Dynamics AX</span><span class="sxs-lookup"><span data-stu-id="3e8f8-277">Dynamics AX</span></span>

<span data-ttu-id="3e8f8-278">このアプローチは、**loadSegments()** メソッドのアプローチに似ています。</span><span class="sxs-lookup"><span data-stu-id="3e8f8-278">The approach is similar to the approach for the **loadSegments()** method.</span></span> <span data-ttu-id="3e8f8-279">**parm** メソッドのソースが変更できるすべての場所にコードを移動する必要があります。</span><span class="sxs-lookup"><span data-stu-id="3e8f8-279">The code must be moved to every location where the source of the **parm** method can change.</span></span> <span data-ttu-id="3e8f8-280">ほとんどの場合、これらの場所は対応するデータ フィールドの **modified()** メソッドおよび/またはデータ ソースの **active()** メソッドです。</span><span class="sxs-lookup"><span data-stu-id="3e8f8-280">In most cases, these locations are the **modified()** method on the corresponding data field and/or the **active()** method on the data source.</span></span> <span data-ttu-id="3e8f8-281">たとえば、上記のコードでは、移行したコードはこのようになります。</span><span class="sxs-lookup"><span data-stu-id="3e8f8-281">For example, for the preceding code, the migrated code would look like this.</span></span>

    LedgerJournalTable data source,
    FixedOffsetAccount field
    public void modified()
    {
        if (ledgerJournalTable.FixedOffsetAccount)
        {
            ledgerJournalTrans_OffsetAccount.allowEdit(ledgerJournalTrans.OffsetAccountType == LedgerJournalACType::Ledger);
        }
        else if (!ledgerJournalTrans_OffsetAccount.allowEdit())
        {
            ledgerJournalTrans_OffsetAccount.allowEdit(true);
        }
    }

    LedgerJournalTrans data source,
    OffsetAccountType field
    public void modified()
    {
        if (ledgerJournalTable.FixedOffsetAccount)
        {
            ledgerJournalTrans_OffsetAccount.allowEdit(ledgerJournalTrans.OffsetAccountType == LedgerJournalACType::Ledger);
        }
            else if (!ledgerJournalTrans_OffsetAccount.allowEdit())
        {
            ledgerJournalTrans_OffsetAccount.allowEdit(true);
        }
    }

    LedgerJournalTrans data source:
    public void active()
    {
        if (ledgerJournalTable.FixedOffsetAccount)
        {
            ledgerJournalTrans_OffsetAccount.allowEdit(ledgerJournalTrans.OffsetAccountType == LedgerJournalACType::Ledger);
        }
        else if (!ledgerJournalTrans_OffsetAccount.allowEdit())
        {
            ledgerJournalTrans_OffsetAccount.allowEdit(true);
        }
    }

    LedgerJournalTable data source:
    public void active()
    {
        if (ledgerJournalTable.FixedOffsetAccount)
        {
            ledgerJournalTrans_OffsetAccount.allowEdit(ledgerJournalTrans.OffsetAccountType == LedgerJournalACType::Ledger);
        }
        else if (!ledgerJournalTrans_OffsetAccount.allowEdit())
        {
            ledgerJournalTrans_OffsetAccount.allowEdit(true);
        }
    }

<span data-ttu-id="3e8f8-282">**注記:** **gotFocus()** メソッドからすべてのコードを削除したら、そのメソッドを削除できます。</span><span class="sxs-lookup"><span data-stu-id="3e8f8-282">**Note:** After all the code has been moved out of the **gotFocus()** method, you can delete the method.</span></span>

### <a name="step-14"></a><span data-ttu-id="3e8f8-283">ステップ 14</span><span class="sxs-lookup"><span data-stu-id="3e8f8-283">Step 14</span></span>

#### <a name="ax-2012"></a><span data-ttu-id="3e8f8-284">AX 2012</span><span class="sxs-lookup"><span data-stu-id="3e8f8-284">AX 2012</span></span>

<span data-ttu-id="3e8f8-285">フォーム **init()** メソッド:</span><span class="sxs-lookup"><span data-stu-id="3e8f8-285">In the form **init()** method:</span></span>

    ledgerDimensionDefaultAccountController = LedgerDimensionDefaultAccountController::construct(vendParameters_ds, fieldStr(VendParameters, ClearingLedgerDimension));

#### <a name="dynamics-ax"></a><span data-ttu-id="3e8f8-286">Dynamics AX</span><span class="sxs-lookup"><span data-stu-id="3e8f8-286">Dynamics AX</span></span>

<span data-ttu-id="3e8f8-287">コントロールで以下のプロパティを設定します。</span><span class="sxs-lookup"><span data-stu-id="3e8f8-287">Set the following properties on the control:</span></span>

-   <span data-ttu-id="3e8f8-288">**データ ソース**</span><span class="sxs-lookup"><span data-stu-id="3e8f8-288">**Data Source**</span></span>
-   <span data-ttu-id="3e8f8-289">**参照フィールド**</span><span class="sxs-lookup"><span data-stu-id="3e8f8-289">**Reference Field**</span></span>
-   <span data-ttu-id="3e8f8-290">**コントローラー クラス**</span><span class="sxs-lookup"><span data-stu-id="3e8f8-290">**Controller Class**</span></span>

<span data-ttu-id="3e8f8-291">[![SegmentMigrate04](./media/segmentmigrate04.png)](./media/segmentmigrate04.png) [![SegmentMigrate05](./media/segmentmigrate05.png)](./media/segmentmigrate05.png) **注記:** コントロールが動作するためにはコントローラー クラスが必要です。</span><span class="sxs-lookup"><span data-stu-id="3e8f8-291">[![SegmentMigrate04](./media/segmentmigrate04.png)](./media/segmentmigrate04.png) [![SegmentMigrate05](./media/segmentmigrate05.png)](./media/segmentmigrate05.png) **Note:** A controller class is required for the control to work.</span></span> <span data-ttu-id="3e8f8-292">したがって、**Controller Class** プロパティが設定されていないと、ランタイム エラーがスローされます。</span><span class="sxs-lookup"><span data-stu-id="3e8f8-292">Therefore, a run-time error will be thrown if the **Controller Class** property isn't set.</span></span>

### <a name="step-15"></a><span data-ttu-id="3e8f8-293">ステップ 15</span><span class="sxs-lookup"><span data-stu-id="3e8f8-293">Step 15</span></span>

#### <a name="ax-2012"></a><span data-ttu-id="3e8f8-294">AX 2012</span><span class="sxs-lookup"><span data-stu-id="3e8f8-294">AX 2012</span></span>

    ledgerDimensionAccountController.setValues(ledgerJournalTrans.DefaultDimension, false);

#### <a name="dynamics-ax"></a><span data-ttu-id="3e8f8-295">Dynamics AX</span><span class="sxs-lookup"><span data-stu-id="3e8f8-295">Dynamics AX</span></span>

<span data-ttu-id="3e8f8-296">分析コードの指定子のマップを作成してから、**セグメント化されたエントリ**コントロールの **setDimensionSpecifiers** メソッドに送信する必要があります。</span><span class="sxs-lookup"><span data-stu-id="3e8f8-296">A map of the dimension specifiers must be created that can then be sent into the **Segmented Entry** control's **setDimensionSpecifiers** method.</span></span>

    Map defaultDimensionSpecifiers = LedgerDimensionDefaultingEngine::getDefaultDimensionSpecifiers(ledgerJournalTable.DefaultDimension);

    TmpLedgerJournalSplitLines_LedgerAccount.setDimensionSpecifiers(defaultDimensionSpecifiers, false);

<span data-ttu-id="3e8f8-297">**注記:** 分析コードの指定子のマップに何かを追加してからコントロールに送ることができます。</span><span class="sxs-lookup"><span data-stu-id="3e8f8-297">**Note:** You can add anything to the dimension specifiers map before it's sent to the control.</span></span> <span data-ttu-id="3e8f8-298">新しいマップをここで作成することもできます。</span><span class="sxs-lookup"><span data-stu-id="3e8f8-298">You can also create a new map here.</span></span> <span data-ttu-id="3e8f8-299">(同様のロジックに関しては、**LedgerJournalEngine** クラス内の **onSegmentChangedForPrimaryAccount** メソッドを参照してください。)</span><span class="sxs-lookup"><span data-stu-id="3e8f8-299">(See the **onSegmentChangedForPrimaryAccount** method in the **LedgerJournalEngine** class for similar logic.)</span></span>

### <a name="step-16"></a><span data-ttu-id="3e8f8-300">ステップ 16</span><span class="sxs-lookup"><span data-stu-id="3e8f8-300">Step 16</span></span>

#### <a name="ax-2012"></a><span data-ttu-id="3e8f8-301">AX 2012</span><span class="sxs-lookup"><span data-stu-id="3e8f8-301">AX 2012</span></span>

<span data-ttu-id="3e8f8-302">**parmControl()** メソッド呼び出し:(これらは通常、フォームの **init()** メソッドまたはコントロールで上書きされたメソッドのうちの 1 つに存在します。)</span><span class="sxs-lookup"><span data-stu-id="3e8f8-302">**parmControl()** method calls: (These are typically present in the form's **init()** method or one of the methods that are overridden on the control.)</span></span>

    ledgerDimensionDefaultAccountController.parmControl(clearingAccount);

#### <a name="dynamics-ax"></a><span data-ttu-id="3e8f8-303">Dynamics AX</span><span class="sxs-lookup"><span data-stu-id="3e8f8-303">Dynamics AX</span></span>

<span data-ttu-id="3e8f8-304">必要がなくなったため、このコード行を削除します。</span><span class="sxs-lookup"><span data-stu-id="3e8f8-304">Remove this line of code, because it's no longer required.</span></span> <span data-ttu-id="3e8f8-305">ただし、最初にどのコントローラーがどのコントロールで使用されるかを記録します。</span><span class="sxs-lookup"><span data-stu-id="3e8f8-305">However, first make a note of which controller is used with which control.</span></span> <span data-ttu-id="3e8f8-306">たとえば、この場合、ledgerDimensionDefaultAccountController が ClearingAccount SEC で使用されています。</span><span class="sxs-lookup"><span data-stu-id="3e8f8-306">For example, in this case, ledgerDimensionDefaultAccountController is being used with the ClearingAccount SEC.</span></span> <span data-ttu-id="3e8f8-307">マッピングは、コントロールでコントローラー オブジェクトのメソッド呼び出しを対応するメソッド呼び出しに置き換える場合、およびデザイン時にプロパティを設定する場合に必要です。</span><span class="sxs-lookup"><span data-stu-id="3e8f8-307">A mapping is required when you replace method calls on controller objects with corresponding method calls on the control, and when you set the properties at design time.</span></span>

### <a name="step-17"></a><span data-ttu-id="3e8f8-308">ステップ 17</span><span class="sxs-lookup"><span data-stu-id="3e8f8-308">Step 17</span></span>

#### <a name="ax-2012"></a><span data-ttu-id="3e8f8-309">AX 2012</span><span class="sxs-lookup"><span data-stu-id="3e8f8-309">AX 2012</span></span>

<span data-ttu-id="3e8f8-310">フォーム **init()** メソッド:</span><span class="sxs-lookup"><span data-stu-id="3e8f8-310">In the form **init()** method:</span></span>

    ledgerDimensionDefaultAccountController.parmFilterLedgerPostingType(LedgerPostingType::VendSettlement);

#### <a name="dynamics-ax"></a><span data-ttu-id="3e8f8-311">Dynamics AX</span><span class="sxs-lookup"><span data-stu-id="3e8f8-311">Dynamics AX</span></span>

<span data-ttu-id="3e8f8-312">これは、コントロールの**転記タイプ**プロパティです。</span><span class="sxs-lookup"><span data-stu-id="3e8f8-312">This is the **Posting Type** property on the control.</span></span> <span data-ttu-id="3e8f8-313">**PostingType** プロパティを設定する必要があるコントロールは、**parmControl()** 呼び出しを見て派生したマッピングの詳細から判別できます。</span><span class="sxs-lookup"><span data-stu-id="3e8f8-313">The control that the **PostingType** property must be set on can be determined from the mapping details that are derived by looking at the **parmControl()** call.</span></span> <span data-ttu-id="3e8f8-314">[![SegmentMigrate06](./media/segmentmigrate06.png)](./media/segmentmigrate06.png) これらのプロパティは、コントロール インスタンスで **parm** メソッドを介してコードで設定することもできます。</span><span class="sxs-lookup"><span data-stu-id="3e8f8-314">[![SegmentMigrate06](./media/segmentmigrate06.png)](./media/segmentmigrate06.png) These properties can also be set in code, through corresponding **parm** methods on the control instance.</span></span> <span data-ttu-id="3e8f8-315">次に例を示します。</span><span class="sxs-lookup"><span data-stu-id="3e8f8-315">Here's an example.</span></span>

    ClearingAccount.parmPostingType(LedgerPostingType::VendSettlement);

### <a name="step-18"></a><span data-ttu-id="3e8f8-316">ステップ 18</span><span class="sxs-lookup"><span data-stu-id="3e8f8-316">Step 18</span></span>

#### <a name="ax-2012"></a><span data-ttu-id="3e8f8-317">AX 2012</span><span class="sxs-lookup"><span data-stu-id="3e8f8-317">AX 2012</span></span>

<span data-ttu-id="3e8f8-318">元帳分析コードのデータ ソース フィールドで **resolveReference()** をオーバーライドします。</span><span class="sxs-lookup"><span data-stu-id="3e8f8-318">Override **resolveReference()** in the data source field for the ledger dimension.</span></span> <span data-ttu-id="3e8f8-319">[![SegmentMigrate07](./media/segmentmigrate07.png)](./media/segmentmigrate07.png)</span><span class="sxs-lookup"><span data-stu-id="3e8f8-319">[![SegmentMigrate07](./media/segmentmigrate07.png)](./media/segmentmigrate07.png)</span></span>

#### <a name="dynamics-ax"></a><span data-ttu-id="3e8f8-320">Dynamics AX</span><span class="sxs-lookup"><span data-stu-id="3e8f8-320">Dynamics AX</span></span>

<span data-ttu-id="3e8f8-321">不要になったので、このコードを削除してください。</span><span class="sxs-lookup"><span data-stu-id="3e8f8-321">Delete this code, because it's no longer required.</span></span> <span data-ttu-id="3e8f8-322">コントロールこれを自動的に処理します。</span><span class="sxs-lookup"><span data-stu-id="3e8f8-322">The control handles this automatically.</span></span>

### <a name="step-19"></a><span data-ttu-id="3e8f8-323">ステップ 19</span><span class="sxs-lookup"><span data-stu-id="3e8f8-323">Step 19</span></span>

#### <a name="ax-2012"></a><span data-ttu-id="3e8f8-324">AX 2012</span><span class="sxs-lookup"><span data-stu-id="3e8f8-324">AX 2012</span></span>

<span data-ttu-id="3e8f8-325">フォームは、**parm** メソッドを通じてコントローラーのプロパティを設定します。</span><span class="sxs-lookup"><span data-stu-id="3e8f8-325">The form sets properties on the controller through **parm** methods.</span></span>

#### <a name="dynamics-ax"></a><span data-ttu-id="3e8f8-326">Dynamics AX</span><span class="sxs-lookup"><span data-stu-id="3e8f8-326">Dynamics AX</span></span>

<span data-ttu-id="3e8f8-327">一般に、コントローラー クラスに以前設定されていたプロパティをコントロールに直接設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="3e8f8-327">In general, any property that was previously set on the controller class should now be set directly on the control.</span></span> <span data-ttu-id="3e8f8-328">このプロパティを設定する必要があるコントロールは、**parmControl()** 呼び出しを見て派生したマッピングの詳細から判断できます。</span><span class="sxs-lookup"><span data-stu-id="3e8f8-328">The control that the property must be set on can be determined from the mapping details that are derived by looking at the **parmControl()** call.</span></span> <span data-ttu-id="3e8f8-329">また、**セグメント化エントリ** コントロールの場合、Microsoft Visual Studio の**プロパティ** ダイアログ ボックスで使用できるプロパティは、コントロール インスタンスで対応する **parm** メソッドを使用して、コードで設定することもできます。</span><span class="sxs-lookup"><span data-stu-id="3e8f8-329">Additionally, for the **Segmented Entry** control, any property that is available in the **Properties** dialog box in Microsoft Visual Studio can also be set in code, through the corresponding **parm** method on the control instance.</span></span>

### <a name="step-20"></a><span data-ttu-id="3e8f8-330">ステップ 20</span><span class="sxs-lookup"><span data-stu-id="3e8f8-330">Step 20</span></span>

#### <a name="ax-2012"></a><span data-ttu-id="3e8f8-331">AX 2012</span><span class="sxs-lookup"><span data-stu-id="3e8f8-331">AX 2012</span></span>

<span data-ttu-id="3e8f8-332">フォームは、コントロールの **currentSegmentIndex()** メソッドを使用します。</span><span class="sxs-lookup"><span data-stu-id="3e8f8-332">The form uses the control's **currentSegmentIndex()** method.</span></span>

    dimOffetAssetController. getDimensionAttributeByControlIndex(currentSegmentIndex);

#### <a name="dynamics-ax"></a><span data-ttu-id="3e8f8-333">Dynamics AX</span><span class="sxs-lookup"><span data-stu-id="3e8f8-333">Dynamics AX</span></span>

<span data-ttu-id="3e8f8-334">一般に、コントローラー クラスに以前設定されていたプロパティをコントロールに直接設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="3e8f8-334">In general, any property that was previously set on the controller class should now be set directly on the control.</span></span> <span data-ttu-id="3e8f8-335">このプロパティを設定する必要があるコントロールは、**parmControl()** 呼び出しを見て派生したマッピングの詳細から判断できます。</span><span class="sxs-lookup"><span data-stu-id="3e8f8-335">The control that the property must be set on can be determined from the mapping details that are derived by looking at the **parmControl()** call.</span></span> <span data-ttu-id="3e8f8-336">また、**セグメント化エントリ** コントロールの場合、Visual Studio の**プロパティ** ダイアログ ボックスで使用できるプロパティは、コントロール インスタンスで対応する **parm** メソッドを使用して、コードで設定することもできます。</span><span class="sxs-lookup"><span data-stu-id="3e8f8-336">Additionally, for the **Segmented Entry** control, any property that is available in the **Properties** dialog box in Visual Studio can also be set in code, through the corresponding **parm** method on the control instance.</span></span>

### <a name="step-21"></a><span data-ttu-id="3e8f8-337">ステップ 21</span><span class="sxs-lookup"><span data-stu-id="3e8f8-337">Step 21</span></span>

#### <a name="ax-2012"></a><span data-ttu-id="3e8f8-338">AX 2012</span><span class="sxs-lookup"><span data-stu-id="3e8f8-338">AX 2012</span></span>

<span data-ttu-id="3e8f8-339">このフォームは、コントローラー オブジェクトのメソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="3e8f8-339">The form calls methods on the controller object.</span></span> <span data-ttu-id="3e8f8-340">次に例を示します。</span><span class="sxs-lookup"><span data-stu-id="3e8f8-340">Here's an example.</span></span>

    dimOffetAssetController. getDimensionAttributeByControlIndex(currentSegmentIndex);

#### <a name="dynamics-ax"></a><span data-ttu-id="3e8f8-341">Dynamics AX</span><span class="sxs-lookup"><span data-stu-id="3e8f8-341">Dynamics AX</span></span>

<span data-ttu-id="3e8f8-342">コントローラー上のすべてのメソッド呼び出しはコントロール上のメソッド呼び出しに置き換える必要があります。</span><span class="sxs-lookup"><span data-stu-id="3e8f8-342">All method calls on the controller must be replaced with method calls on the control.</span></span> <span data-ttu-id="3e8f8-343">この例では、代わりにコントロールで **getDimensionAttributeByControlIndex()** メソッドを使用します。</span><span class="sxs-lookup"><span data-stu-id="3e8f8-343">For this example, use the **getDimensionAttributeByControlIndex()** method on the control instead.</span></span>

    segmentedEntryControl. getDimensionAttributeByControlIndex();

### <a name="step-22"></a><span data-ttu-id="3e8f8-344">ステップ 22</span><span class="sxs-lookup"><span data-stu-id="3e8f8-344">Step 22</span></span>

#### <a name="ax-2012"></a><span data-ttu-id="3e8f8-345">AX 2012</span><span class="sxs-lookup"><span data-stu-id="3e8f8-345">AX 2012</span></span>

<span data-ttu-id="3e8f8-346">**DimensionDynamicAccountController** で、勘定タイプはコンストラクターを通して指定されます。</span><span class="sxs-lookup"><span data-stu-id="3e8f8-346">For **DimensionDynamicAccountController**, the account type is specified through the constructor.</span></span>

    DimensionDynamicAccountController::construct(ledgerJournalTrans_ds, fieldStr(LedgerJournalTrans, LedgerDimension), fieldStr(LedgerJournalTrans, AccountType));

#### <a name="dynamics-ax"></a><span data-ttu-id="3e8f8-347">Dynamics AX</span><span class="sxs-lookup"><span data-stu-id="3e8f8-347">Dynamics AX</span></span>

<span data-ttu-id="3e8f8-348">この機能を実装するには、2 つのメソッドがあります。</span><span class="sxs-lookup"><span data-stu-id="3e8f8-348">There are two methods for implementing this functionality.</span></span> <span data-ttu-id="3e8f8-349">これらのメソッドは相互に排他的なため、状況に応じてそれらのメソッドのうち 1 つのみを使用してください。</span><span class="sxs-lookup"><span data-stu-id="3e8f8-349">These methods are mutually exclusive, so use only one of them, depending on the situation:</span></span>

-   <span data-ttu-id="3e8f8-350">**セグメント化されたエントリー**コントロールについては、**プロパティ**ダイアログ ボックスで、**勘定タイプ フィールド**プロパティを勘定タイプを提供するデータ ソース フィールドに設定します。</span><span class="sxs-lookup"><span data-stu-id="3e8f8-350">For the **Segmented Entry** control, in the **Properties** dialog box, set the **Account Type Field** property to the data source field that will provide the account type.</span></span> <span data-ttu-id="3e8f8-351">これが推奨されるメソッドです。</span><span class="sxs-lookup"><span data-stu-id="3e8f8-351">This is the preferred method.</span></span> <span data-ttu-id="3e8f8-352">**注記:** **super()** 呼び出しが、**勘定タイプ フィールド** プロパティにバインドされているフィールドの **modified()** メソッドから削除されている場合、このメソッドは機能しません。</span><span class="sxs-lookup"><span data-stu-id="3e8f8-352">**Note:** If the **super()** call has been removed from the **modified()** method for the field that is bound to the **Account Type Field** property, this method won't work.</span></span> <span data-ttu-id="3e8f8-353">**LedgerJournalTransDaily** などのいくつかの仕訳帳フォームで、この問題が確認されました。</span><span class="sxs-lookup"><span data-stu-id="3e8f8-353">We have seen this issue in some journal forms, such as **LedgerJournalTransDaily**.</span></span> <span data-ttu-id="3e8f8-354">このような場合、**super()** コールバックを **modified()** メソッドに追加するか、2 つ目のメソッドを使用します。</span><span class="sxs-lookup"><span data-stu-id="3e8f8-354">In such cases, either add the **super()** call back to the **modified()** method, or use the second method.</span></span>
-   <span data-ttu-id="3e8f8-355">コントロールで **parmAccountTypeEnumValue()** メソッドを呼び出すことにより、勘定タイプを手動で設定します。</span><span class="sxs-lookup"><span data-stu-id="3e8f8-355">Set the account type manually by calling the **parmAccountTypeEnumValue()** method on the control.</span></span> <span data-ttu-id="3e8f8-356">次に例を示します。</span><span class="sxs-lookup"><span data-stu-id="3e8f8-356">Here's an example.</span></span>

        LedgerJournalTrans_AccountNum.parmAccountTypeEnumValue(enum2int(ledgerJournalTrans.AccountType));

    <span data-ttu-id="3e8f8-357">**注記:** **parmAccountTypeEnumValue()** への呼び出しは、勘定タイプを提供するフィールドの、データソースの **active()** メソッド、および **modified()** メソッドの両方に入力する必要があります。</span><span class="sxs-lookup"><span data-stu-id="3e8f8-357">**Note:** The call to **parmAccountTypeEnumValue()** must be put in both the data source's **active()** method and the **modified()** method of the field that will provide the account type.</span></span>

### <a name="step-23"></a><span data-ttu-id="3e8f8-358">ステップ 23</span><span class="sxs-lookup"><span data-stu-id="3e8f8-358">Step 23</span></span>

#### <a name="ax-2012"></a><span data-ttu-id="3e8f8-359">AX 2012</span><span class="sxs-lookup"><span data-stu-id="3e8f8-359">AX 2012</span></span>

<span data-ttu-id="3e8f8-360">フォームには定義されている変数があります。</span><span class="sxs-lookup"><span data-stu-id="3e8f8-360">The form has a variable that is defined.</span></span>

    LedgerDimensionDefaultAccountController ledgerDimensionDefaultAccountController;

#### <a name="dynamics-ax"></a><span data-ttu-id="3e8f8-361">Dynamics AX</span><span class="sxs-lookup"><span data-stu-id="3e8f8-361">Dynamics AX</span></span>

<span data-ttu-id="3e8f8-362">コントローラーが必要なくなったため、これを削除します。</span><span class="sxs-lookup"><span data-stu-id="3e8f8-362">Remove this, because the controller is no longer required.</span></span>

### <a name="step-24"></a><span data-ttu-id="3e8f8-363">ステップ 24</span><span class="sxs-lookup"><span data-stu-id="3e8f8-363">Step 24</span></span>

#### <a name="ax-2012"></a><span data-ttu-id="3e8f8-364">AX 2012</span><span class="sxs-lookup"><span data-stu-id="3e8f8-364">AX 2012</span></span>

<span data-ttu-id="3e8f8-365">**parmCurrentLedgerCOA()** メソッド呼び出し:(これらは通常、フォームの **init()** メソッドまたはコントロールで上書きされたメソッドのうちの 1 つに存在します。)</span><span class="sxs-lookup"><span data-stu-id="3e8f8-365">**parmCurrentLedgerCOA()** method calls: (These are typically present in the form's **init()** method or one of the methods that are overridden on the control.)</span></span>

    ledgerDimensionDefaultAccountController.parmCurrentLedgerCOA(LedgerCOA::current());

#### <a name="dynamics-ax"></a><span data-ttu-id="3e8f8-366">Dynamics AX</span><span class="sxs-lookup"><span data-stu-id="3e8f8-366">Dynamics AX</span></span>

<span data-ttu-id="3e8f8-367">ほとんどの場合に必要がなくなったため、このコード行を削除します。</span><span class="sxs-lookup"><span data-stu-id="3e8f8-367">Remove this line of code, because it's no longer required in most cases.</span></span> <span data-ttu-id="3e8f8-368">この線を削除する前に、**LedgerCOA** 値がその情報から派生するため、データ領域 ID がパラメーターとしてコントローラーに正しく渡されていることを確認してください。</span><span class="sxs-lookup"><span data-stu-id="3e8f8-368">Before you delete this line, make sure that the data area ID is correctly passed in to the controller as a parameter, because the **LedgerCOA** value will be derived from that information.</span></span> <span data-ttu-id="3e8f8-369">データ領域 ID が渡されない場合は、**parmCurrentLedgerCOA(â€¦)** を **parmDataAreaId(â€¦)** で交換し、通常は **curext()** または会社のアカウント管理のために範囲を制御する別のテーブル フィールドである適切な **SelectableDataArea** 値を渡します。</span><span class="sxs-lookup"><span data-stu-id="3e8f8-369">If the data area ID is not passed in, replace **parmCurrentLedgerCOA(â€¦)** with **parmDataAreaId(â€¦)**, and pass the appropriate **SelectableDataArea** value, which is usually **curext()** or another table field that controls the scope of the company for the account control.</span></span> <span data-ttu-id="3e8f8-370">フォームにデータ領域のコンテキストはありませんが、現在の **LedgerCOA** 値のみがある場合、既定のアカウント コント ローラーだけで動作する必要があります。</span><span class="sxs-lookup"><span data-stu-id="3e8f8-370">If the form has no data area context but only a current **LedgerCOA** value, it should be working only with the default account controller.</span></span> <span data-ttu-id="3e8f8-371">企業には無関係ですが、特定の勘定科目表 (COA) (**MainAccount** および **Allocations** など) にスコープされているフォームがいくつかあります。</span><span class="sxs-lookup"><span data-stu-id="3e8f8-371">There are only a few forms that are agnostic of a company, but that are scoped to a specific chart of accounts (COA) (for example, **MainAccount** and **Allocations**).</span></span> <span data-ttu-id="3e8f8-372">そのような場合、**parmCurrentLedgerCOA** が、既定のアカウント コントローラー タイプ セットを持つ**セグメント化エントリ** コントロール インスタンスで呼び出される必要があります。</span><span class="sxs-lookup"><span data-stu-id="3e8f8-372">In these cases, **parmCurrentLedgerCOA** should be called on the **Segmented Entry** control instance that has a default account controller type set.</span></span>

### <a name="step-25"></a><span data-ttu-id="3e8f8-373">ステップ 25</span><span class="sxs-lookup"><span data-stu-id="3e8f8-373">Step 25</span></span>

#### <a name="ax-2012"></a><span data-ttu-id="3e8f8-374">AX 2012</span><span class="sxs-lookup"><span data-stu-id="3e8f8-374">AX 2012</span></span>

<span data-ttu-id="3e8f8-375">**parmIncludeFinancialAccounts(NoYes)** メソッド呼び出し:</span><span class="sxs-lookup"><span data-stu-id="3e8f8-375">**parmIncludeFinancialAccounts(NoYes)** method calls:</span></span>

    LedgerDimensionDefaultAccountController.parmIncludeFinancialAccounts(NoYes::Yes);

#### <a name="dynamics-ax"></a><span data-ttu-id="3e8f8-376">Dynamics AX</span><span class="sxs-lookup"><span data-stu-id="3e8f8-376">Dynamics AX</span></span>

<span data-ttu-id="3e8f8-377">このコード行は不要になり、**セグメント化されたエントリ**コントロールのプロパティを使用して直接設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="3e8f8-377">This line of code is no longer required and should be set directly via a property on the **Segmented Entry** control.</span></span> <span data-ttu-id="3e8f8-378">**注記:** フレームワークのバグのため、これを明示的に設定しないと、以前の動作では、構築中に暗黙的に**はい**が割り当てられていましたが、勘定分析コードの既定のアカウント コントローラーに**いいえ**が割り当てられます。</span><span class="sxs-lookup"><span data-stu-id="3e8f8-378">**Note:** Because of a framework bug, if you don't set this explicitly, **No** will be assigned on a ledger dimension default account controller, whereas the previous behavior was to implicitly assign **Yes** during construction.</span></span> <span data-ttu-id="3e8f8-379">この操作は、プロパティとして手動で設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="3e8f8-379">You must set this manually as a property.</span></span> <span data-ttu-id="3e8f8-380">または、**ダイアログ**クラスへの、**parm** メソッドがまだ明示的に呼び出されるはずです。</span><span class="sxs-lookup"><span data-stu-id="3e8f8-380">Alternatively, for a **dialog** class, the **parm** method should still be explicitly called.</span></span>

### <a name="step-26"></a><span data-ttu-id="3e8f8-381">ステップ 26</span><span class="sxs-lookup"><span data-stu-id="3e8f8-381">Step 26</span></span>

#### <a name="ax-2012"></a><span data-ttu-id="3e8f8-382">AX 2012</span><span class="sxs-lookup"><span data-stu-id="3e8f8-382">AX 2012</span></span>

<span data-ttu-id="3e8f8-383">**セグメント化エントリ** コントロールのアカウントタイプを提供するデータフィールドの **変更済み** メソッドのコードは、コントロールが動的アカウントコントロールとして使用されている場合、このようになります。</span><span class="sxs-lookup"><span data-stu-id="3e8f8-383">The code for the **modified** method of the data field that provides the account type for the **Segmented Entry** control might look like this when the control is used as a dynamic account control.</span></span>

    public void modified()
    {
        super();

        // Lock the main account segment if "Fixed offset account" is selected in Journal Names
        if (ledgerJournalTable.OffsetAccountType == LedgerJournalACType::Ledger)
        {
            controller.parmLockMainAccountSegment(ledgerJournalTable.FixedOffsetAccount);
        }
    }

#### <a name="dynamics-ax"></a><span data-ttu-id="3e8f8-384">Dynamics AX</span><span class="sxs-lookup"><span data-stu-id="3e8f8-384">Dynamics AX</span></span>

<span data-ttu-id="3e8f8-385">このデータ フィールドの **modified** メソッドは、**参照** フィールドとして **セグメント化されたエントリ** コントロールにバインドされた勘定分析コード フィールドをクリアしなければならなくなりました。</span><span class="sxs-lookup"><span data-stu-id="3e8f8-385">The **modified** method of this data field must now clear the ledger dimension field that is bound to the **Segmented Entry** control as a **Reference** field.</span></span> <span data-ttu-id="3e8f8-386">たとえば、**セグメント化されたエントリ**コントロールの名前が **OffsetAccount** である場合、このコントロールの**参照**フィールド プロパティが **LedgerDimension** に設定され、上記のコード内の**変更**メソッドが次のように変更される必要があります。</span><span class="sxs-lookup"><span data-stu-id="3e8f8-386">For example, if the name of the **Segmented Entry** control is **OffsetAccount**, and the **Reference** field property for this control is set to **LedgerDimension**, the **modified** method in the preceding code should be changed as follows.</span></span>

    public void modified()
    {
        super();

        OffsetAccount.LedgerDimension = 0;

        // Lock the main account segment if "Fixed offset account" is selected in Journal Names
        if (ledgerJournalTable.OffsetAccountType == LedgerJournalACType::Ledger)
        {
            OffsetAccount.parmLockMainAccountSegment(ledgerJournalTable.FixedOffsetAccount);
        }
    }

<span data-ttu-id="3e8f8-387">追加の明細行は、勘定タイプが変更されたときにコントロールをクリアするために必要です。</span><span class="sxs-lookup"><span data-stu-id="3e8f8-387">The additional line is required to clear the control when the account type is changed.</span></span>

### <a name="step-27"></a><span data-ttu-id="3e8f8-388">ステップ 27</span><span class="sxs-lookup"><span data-stu-id="3e8f8-388">Step 27</span></span>

#### <a name="ax-2012"></a><span data-ttu-id="3e8f8-389">AX 2012</span><span class="sxs-lookup"><span data-stu-id="3e8f8-389">AX 2012</span></span>

<span data-ttu-id="3e8f8-390">コントローラーで **parmAccountStructure()** メソッドを呼び出すことができます。</span><span class="sxs-lookup"><span data-stu-id="3e8f8-390">You can call the **parmAccountStructure()** method on the controller.</span></span>

    fromBudgetPlanningLedgerDimensionController.parmAccountStructureId(accountStructureIdLocal);

#### <a name="dynamics-ax"></a><span data-ttu-id="3e8f8-391">Dynamics AX</span><span class="sxs-lookup"><span data-stu-id="3e8f8-391">Dynamics AX</span></span>

<span data-ttu-id="3e8f8-392">このメソッドは 2 つの異なるメソッドで置き換えられます。</span><span class="sxs-lookup"><span data-stu-id="3e8f8-392">This method is replaced by two different methods.</span></span> <span data-ttu-id="3e8f8-393">また、新しいメソッドの目的は、古いメソッドの逆です: 古いメソッドは検証を無効にしましたが、新しいメソッドはそれを有効にします。</span><span class="sxs-lookup"><span data-stu-id="3e8f8-393">Additionally, the purpose of the new methods is the opposite of the old method: the old method turned validation off, whereas the new methods turn it on.</span></span> <span data-ttu-id="3e8f8-394">したがって、コードを移行するときは、新しいメソッドの Boolean パラメーターを逆にする必要があります。</span><span class="sxs-lookup"><span data-stu-id="3e8f8-394">Therefore, when you migrate code, you must reverse the Boolean parameter for the new methods.</span></span> <span data-ttu-id="3e8f8-395">たとえば、上記のコードでメソッドの呼び出しについては、新しいメソッドはこのようになります。</span><span class="sxs-lookup"><span data-stu-id="3e8f8-395">For example, for the method call in the preceding code, the new methods would look like this.</span></span>

    ToBudgetTransactionLine_LedgerDimension.parmDoValueActiveDatesValidation(false);

    ToBudgetTransactionLine_LedgerDimension.parmDoValueSuspendedValidation(false);

### <a name="step-28"></a><span data-ttu-id="3e8f8-396">ステップ 28</span><span class="sxs-lookup"><span data-stu-id="3e8f8-396">Step 28</span></span>

#### <a name="ax-2012"></a><span data-ttu-id="3e8f8-397">AX 2012</span><span class="sxs-lookup"><span data-stu-id="3e8f8-397">AX 2012</span></span>

<span data-ttu-id="3e8f8-398">以下のコントローラーで **parmAccountStructure()** メソッドを呼び出すことができます。</span><span class="sxs-lookup"><span data-stu-id="3e8f8-398">You can call the **parmAccountStructure()** method on the controller:</span></span>

    fromBudgetPlanningLedgerDimensionController.parmAccountStructureId(accountStructureIdLocal);

#### <a name="dynamics-ax"></a><span data-ttu-id="3e8f8-399">Dynamics AX</span><span class="sxs-lookup"><span data-stu-id="3e8f8-399">Dynamics AX</span></span>

<span data-ttu-id="3e8f8-400">**parmAccountStructureId()** メソッドは、コントロール上に存在しません。</span><span class="sxs-lookup"><span data-stu-id="3e8f8-400">The **parmAccountStructureId()** method doesn't exist on the control.</span></span> <span data-ttu-id="3e8f8-401">代わりに、個別の **getAccountStructure()** および **setAccountStructure()** メソッドがあります。</span><span class="sxs-lookup"><span data-stu-id="3e8f8-401">Instead, separate **getAccountStructure()** and **setAccountStructure()** methods exist.</span></span> <span data-ttu-id="3e8f8-402">したがって、**parmAccountStructureId()** 呼び出しは、**parm** メソッドがどのように使用されていたかに応じて、**get** メソッドまたは **set** メソッドで置き換えられる必要があります。</span><span class="sxs-lookup"><span data-stu-id="3e8f8-402">Therefore, the **parmAccountStructureId()** call must be replaced by the **get** or **set** method, depending on how the **parm** method was used.</span></span> <span data-ttu-id="3e8f8-403">たとえば、上記のコードで **parm** メソッドはセッターとして呼び出されたので、呼び出しは**設定**メソッドへの呼び出しによって置換される必要があります。</span><span class="sxs-lookup"><span data-stu-id="3e8f8-403">For example, the **parm** method in the preceding code was called as a setter, so the call should be replaced by a call to the **set** method.</span></span>

    ToBudgetPlanningTransactionLine_LedgerDimension.setAccountStructureId(accountStructureIdLocal);

### <a name="step-29"></a><span data-ttu-id="3e8f8-404">ステップ 29</span><span class="sxs-lookup"><span data-stu-id="3e8f8-404">Step 29</span></span>

#### <a name="ax-2012"></a><span data-ttu-id="3e8f8-405">AX 2012</span><span class="sxs-lookup"><span data-stu-id="3e8f8-405">AX 2012</span></span>

    parmSkipSuspendedAndActiveDateValidation:

#### <a name="dynamics-ax"></a><span data-ttu-id="3e8f8-406">Dynamics AX</span><span class="sxs-lookup"><span data-stu-id="3e8f8-406">Dynamics AX</span></span>

<span data-ttu-id="3e8f8-407">このメソッドは 2 つの異なるメソッドで置き換えられます。</span><span class="sxs-lookup"><span data-stu-id="3e8f8-407">This method is replaced by two different methods.</span></span> <span data-ttu-id="3e8f8-408">また、新しいメソッドの目的は、古いメソッドの逆です: 古いメソッドは検証を無効にしましたが、新しいメソッドはそれを有効にします。</span><span class="sxs-lookup"><span data-stu-id="3e8f8-408">Additionally, the purpose of the new methods is opposite of the old method: the old method turned validation off, whereas the new methods turn it on.</span></span> <span data-ttu-id="3e8f8-409">したがって、コードを移行するときは、新しいメソッドの Boolean パラメーターを逆にする必要があります。</span><span class="sxs-lookup"><span data-stu-id="3e8f8-409">Therefore, when you migrate code, you must reverse the Boolean parameter for the new methods.</span></span> <span data-ttu-id="3e8f8-410">たとえば、上記のコードでメソッドの呼び出しについては、新しいメソッドはこのようになります。</span><span class="sxs-lookup"><span data-stu-id="3e8f8-410">For example, for the method call in the preceding code, the new methods would look like this.</span></span>

    ToBudgetTransactionLine_LedgerDimension.parmDoValueActiveDatesValidation(false);

    ToBudgetTransactionLine_LedgerDimension.parmDoValueSuspendedValidation(false);

### <a name="step-30"></a><span data-ttu-id="3e8f8-411">ステップ 30</span><span class="sxs-lookup"><span data-stu-id="3e8f8-411">Step 30</span></span>

#### <a name="ax-2012"></a><span data-ttu-id="3e8f8-412">AX 2012</span><span class="sxs-lookup"><span data-stu-id="3e8f8-412">AX 2012</span></span>

<span data-ttu-id="3e8f8-413">通常は **loadSegments()** メソッド内でコントローラーの **loadFromId** メソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="3e8f8-413">Typically, call the **loadFromId** method on the controller in the **loadSegments()** method.</span></span>

    ledgerDimensionDefaultAccountControllerResourceIssueOffset.loadFromId(wrkCtrTable.ResourceIssueOffsetLedgerDimension);

#### <a name="dynamics-ax"></a><span data-ttu-id="3e8f8-414">Dynamics AX</span><span class="sxs-lookup"><span data-stu-id="3e8f8-414">Dynamics AX</span></span>

<span data-ttu-id="3e8f8-415">このメソッドは推奨されておらず、使用しないでください。</span><span class="sxs-lookup"><span data-stu-id="3e8f8-415">This method has been deprecated and must not be used.</span></span> <span data-ttu-id="3e8f8-416">このメソッドに対するすべての呼び出しを削除する必要があります。</span><span class="sxs-lookup"><span data-stu-id="3e8f8-416">You should delete all calls to this method.</span></span>

### <a name="migrating-a-segmented-entry-control-on-a-dialog"></a><span data-ttu-id="3e8f8-417">ダイアログ上のセグメント化エントリ コントロールの移行</span><span class="sxs-lookup"><span data-stu-id="3e8f8-417">Migrating a Segmented Entry control on a dialog</span></span>

<span data-ttu-id="3e8f8-418">ダイアログ上の新しい**セグメント化されたエントリ** コントロールの取得パターンは Dynamics AX で変更されています。</span><span class="sxs-lookup"><span data-stu-id="3e8f8-418">The uptake pattern for the new **Segmented Entry** control on a dialog has changed in Dynamics AX.</span></span> <span data-ttu-id="3e8f8-419">コントローラー クラス API とのやり取りではなく、**SegmentedEntryControlBuild** クラスとやり取りしてダイアログと SEC をリンクする必要があります。</span><span class="sxs-lookup"><span data-stu-id="3e8f8-419">Instead of interacting with the controller class API, you must now interact with the **SegmentedEntryControlBuild** class to link the SEC with the dialog.</span></span> <span data-ttu-id="3e8f8-420">このセクションでは、異なるコントローラー タイプのダイアログで SEC を使用するためのコード パターンを示します。</span><span class="sxs-lookup"><span data-stu-id="3e8f8-420">This section shows the code patterns for using SEC on a dialog with different controller types.</span></span> <span data-ttu-id="3e8f8-421">**注記:** Dynamics AX ではヘルプ テキストが不要になるため、ダイアログ フィールドにヘルプ テキストを設定する必要はありません。</span><span class="sxs-lookup"><span data-stu-id="3e8f8-421">**Note:** Help text is no longer required in Dynamics AX, so you don't have to set the Help text on dialog fields.</span></span>

-   <span data-ttu-id="3e8f8-422">**動的アカウント:**</span><span class="sxs-lookup"><span data-stu-id="3e8f8-422">**Dynamic account:**</span></span>
    -   <span data-ttu-id="3e8f8-423">**以前:**</span><span class="sxs-lookup"><span data-stu-id="3e8f8-423">**Before:**</span></span>

            // Creating the dialog field for the SEC
            dialogDynamicAccountType = _dialog.addFieldValue(enumStr(LedgerJournalACTypeForPaymProposal), defaultOffsetAccountType, "@SYS115164", "@SYS115165");
            dialogDynamicAccount = _dialog.addFieldValue(extendedTypeStr(LedgerDimensionBase), defaultOffsetLedgerDimension, "@SYS115166", "@SYS115167");
            dimensionDynamicAccountController = DimensionDynamicAccountController::constructForDialog(dialogDynamicAccount, dialogDynamicAccountType, enumStr(LedgerJournalACTypeForPaymProposal));
                       dimensionDynamicAccountController.parmIsDefaultAccount(true);

            public void dialogPostRun(DialogRunBase _dialog)
            {
            …

            dialogDynamicAccountType.registerOverrideMethod('modified', 'accountType_Modified', this);

            ...
            }

            private boolean accountType_Modified(FormComboBoxControl _formComboBoxControl)
            {
             boolean valueWasModified;

             valueWasModified = _formComboBoxControl.modified();
             if (valueWasModified)
             {
             dialogDynamicAccount.value(0);
                        }

             return valueWasModified;
            }

    -   <span data-ttu-id="3e8f8-424">**以後:**</span><span class="sxs-lookup"><span data-stu-id="3e8f8-424">**After:**</span></span>

            // Creating the dialog field for the SEC
            protected Object dialog()
            {
            ...        

            // Create the account type dialog field
            dialogDynamicAccountType = _dialog.addFieldValue(enumStr(LedgerJournalACTypeForPaymProposal), defaultOffsetAccountType, "@SYS115164", "@SYS115165");
            // Create the SEC dialog field
            dialogDynamicAccount = SegmentedEntryControlBuild::addToDialog(dialog, classstr(DimensionDynamicAccountControl), extendedTypeStr(LedgerDimensionBase), "@SYS115166", defaultOffsetLedgerDimension);

            // Provide account type information for the SEC field
            SegmentedEntryControlBuild::initDialogFieldAccountType(dialogDynamicAccount, enumStr(LedgerJournalACTypeForPaymProposal) , defaultOffsetAccountType);
            // Set additional parameters on the SEC dialog field
            SegmentedEntryControlBuild segmentedEntryControlBuild = dialogDynamicAccount.control(); 
            segmentedEntryControlBuild.parmIsDefaultAccount(true);

            …
            }

            // Override for modified method of the Account type checkbox to update the SEC when account type is changed
            public int accountType_selectionChange(FormComboBoxControl _formComboBoxControl)
            {
            SegmentedEntryControl secDDAC = dialogDynamicAccount.control();
            accountType = _formComboBoxControl.selection();

            // This is the backing variable used to pack the account specified via the SEC
            ledgerDimensionDynamicAccount = 0; 
            // Clear the SEC value
            secDDAC.clearReference();                     

            // Specify the new account type to the SEC; this is an additional step needed for the AX SEC
            secDDAC.parmAccountTypeEnumValue(enum2int(accountType));

            return true;
            }

            // Set default account type based on value read from SysLastValue
            public void dialogPostRun(DialogRunBase _dialog)
            {
            …
            // Default any previously saved account type info
            secDDAC = dialogDynamicAccount.control();
            secDDAC.parmAccountTypeEnumValue(enum2int(accountType));
            ….
            }

-   <span data-ttu-id="3e8f8-425">**勘定科目:**</span><span class="sxs-lookup"><span data-stu-id="3e8f8-425">**Ledger account:**</span></span>
    -   <span data-ttu-id="3e8f8-426">**以前:**</span><span class="sxs-lookup"><span data-stu-id="3e8f8-426">**Before:**</span></span>

            dialogFeeLedgerDimension = dialog.addFieldValue(extendedtypestr(LedgerDimensionAccount),feeLedgerDimension,"@SYS119703", "@SYS85534");
            ledgerDimensionAccountController = LedgerDimensionAccountController::constructForDialog(dialogFeeLedgerDimension);

    -   <span data-ttu-id="3e8f8-427">**以後:**</span><span class="sxs-lookup"><span data-stu-id="3e8f8-427">**After:**</span></span>

            DialogField dialogLedgerAccount = SegmentedEntryControlBuild::addToDialog(dialog, classstr(LedgerDimensionAccountControl), extendedTypeStr(LedgerDimensionAccount), "@SYS119703", feeLedgerDimension);

-   <span data-ttu-id="3e8f8-428">**既定の勘定:**</span><span class="sxs-lookup"><span data-stu-id="3e8f8-428">**Default account:**</span></span>
    -   <span data-ttu-id="3e8f8-429">**以前:**</span><span class="sxs-lookup"><span data-stu-id="3e8f8-429">**Before:**</span></span>

            dialogInterCompanyLedgerDimension = dialog.addFieldValue(extendedTypeStr(LedgerDimensionDefaultAccount),interCompanyLedgerDimension, "@SYS21687", "@SYS85534");
            ledgerDimensionDefaultAccountController = LedgerDimensionDefaultAccountController::constructForDialog(dialogInterCompanyLedgerDimension);

    -   <span data-ttu-id="3e8f8-430">**以後:**</span><span class="sxs-lookup"><span data-stu-id="3e8f8-430">**After:**</span></span>

            DialogField dialogDefaultAccount = SegmentedEntryControlBuild::addToDialog(dialog, classstr(LedgerDimensionDefaultAccountControl), extendedTypeStr(LedgerDimensionDefaultAccount), "@SYS21687", interCompanyLedgerDimension);

-   <span data-ttu-id="3e8f8-431">**予算:**</span><span class="sxs-lookup"><span data-stu-id="3e8f8-431">**Budget:**</span></span>
    -   <span data-ttu-id="3e8f8-432">**以前:** 既存のプログラム ソース コード内でダイアログ シナリオの**予算計画**コントローラー (**BudgetLedgerDimensionController**) の取り込みは見つかりませんでした。</span><span class="sxs-lookup"><span data-stu-id="3e8f8-432">**Before:** No uptake of the **Budget** controller (**BudgetLedgerDimensionController**) for a dialog scenario was found in the existing program source code.</span></span>
    -   <span data-ttu-id="3e8f8-433">**以後:**</span><span class="sxs-lookup"><span data-stu-id="3e8f8-433">**After:**</span></span>

            DialogField dialogBudget = SegmentedEntryControlBuild::addToDialog(dialog, classstr(BudgetLedgerDimensionControl), extendedTypeStr(LedgerDimensionBudget), 'Budget', ledgerDimensionBudget);

    <span data-ttu-id="3e8f8-434">**メモ :**</span><span class="sxs-lookup"><span data-stu-id="3e8f8-434">**Notes:**</span></span>
    -   <span data-ttu-id="3e8f8-435">新しい API を使用すると、ダイアログ フィールドを設定しているときに、ラベル (前述の例では **予算**) を指定できます。</span><span class="sxs-lookup"><span data-stu-id="3e8f8-435">The new API lets you specify the label (**Budget** in the preceding example) while you set up the dialog field.</span></span>
    -   <span data-ttu-id="3e8f8-436">コントロールのデフォルト値は、**ledgerDimensionBudget** 変数で指定します。</span><span class="sxs-lookup"><span data-stu-id="3e8f8-436">The default value for the control is specified via the **ledgerDimensionBudget** variable.</span></span>
    -   <span data-ttu-id="3e8f8-437">**予算** コントローラーを用いて、使用する勘定構造を指定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="3e8f8-437">You must specify the account structure that should be used with the **Budget** controller.</span></span> <span data-ttu-id="3e8f8-438">**Dialog** クラスは、ユーザーが勘定構造を選択し (SEC の外部で)、選択した勘定構造を SEC で設定する方法を実装する必要があります。</span><span class="sxs-lookup"><span data-stu-id="3e8f8-438">The **Dialog** class must implement a way for the user to select the account structure (outside of the SEC) and set the selected account structure on the SEC.</span></span>
-   <span data-ttu-id="3e8f8-439">**予算計画:**</span><span class="sxs-lookup"><span data-stu-id="3e8f8-439">**Budget planning:**</span></span>
    -   <span data-ttu-id="3e8f8-440">**以前:** 既存のプログラム ソース コード内でダイアログ シナリオの**予算計画**コントローラー (**BudgetPlanningLedgerDimensionController**) の取り込みは見つかりませんでした。</span><span class="sxs-lookup"><span data-stu-id="3e8f8-440">**Before:** No uptake of the **Budget planning** controller (**BudgetPlanningLedgerDimensionController**) for a dialog scenario was found in the existing program source code.</span></span>
    -   <span data-ttu-id="3e8f8-441">**以後:**</span><span class="sxs-lookup"><span data-stu-id="3e8f8-441">**After:**</span></span>

            DialogField dialogBudgetPlanning = SegmentedEntryControlBuild::addToDialog(dialog, classstr(BudgetPlanningLedgerDimensionControl), extendedTypeStr(LedgerDimensionBudgetPlanning), 'Budget planning', ledgerDimensionBudgetPlanning);

    <span data-ttu-id="3e8f8-442">**メモ :**</span><span class="sxs-lookup"><span data-stu-id="3e8f8-442">**Notes:**</span></span>
    -   <span data-ttu-id="3e8f8-443">新しい API を使用すると、ダイアログ フィールドを設定しているときに、ラベル (前述の例では **予算計画**) を指定できます。</span><span class="sxs-lookup"><span data-stu-id="3e8f8-443">The new API lets you specify the label (**Budget planning** in the preceding example) while you set up the dialog field.</span></span>
    -   <span data-ttu-id="3e8f8-444">コントロールのデフォルト値は、**ledgerDimensionBudgetPlanning** 変数で指定します。</span><span class="sxs-lookup"><span data-stu-id="3e8f8-444">The default value for the control is specified via the **ledgerDimensionBudgetPlanning** variable.</span></span>
    -   <span data-ttu-id="3e8f8-445">**予算計画** コントローラーを用いて、使用する勘定構造を指定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="3e8f8-445">You must specify the account structure that should be used with the **Budget planning** controller.</span></span> <span data-ttu-id="3e8f8-446">**Dialog** クラスは、ユーザーが勘定構造を選択し (SEC の外部で)、選択した勘定構造を SEC で設定する方法を実装する必要があります。</span><span class="sxs-lookup"><span data-stu-id="3e8f8-446">The **Dialog** class must implement a way for the user to select the account structure (outside of the SEC) and set the selected account structure on the SEC.</span></span>


<a name="additional-resources"></a><span data-ttu-id="3e8f8-447">その他のリソース</span><span class="sxs-lookup"><span data-stu-id="3e8f8-447">Additional resources</span></span>
--------

[<span data-ttu-id="3e8f8-448">セグメント化されたエントリ コントロールのダイアログのサポート</span><span class="sxs-lookup"><span data-stu-id="3e8f8-448">Segmented Entry control dialog support</span></span>](segmented-entry-control-dialog-support.md)

[<span data-ttu-id="3e8f8-449">セグメント化されたエントリ コントロールのメタデータ詳細</span><span class="sxs-lookup"><span data-stu-id="3e8f8-449">Segmented Entry control Metadata Specification</span></span>](segmented-entry-control-metadata-specification.md)

[<span data-ttu-id="3e8f8-450">セグメント化されたエントリ コントロールの Parm メソッド詳細</span><span class="sxs-lookup"><span data-stu-id="3e8f8-450">Segmented Entry control Parm method Specification</span></span>](segmented-entry-control-parm-method-specification.md)

[<span data-ttu-id="3e8f8-451">セグメント化されたエントリ コントロールの移行</span><span class="sxs-lookup"><span data-stu-id="3e8f8-451">Segmented Entry control migration</span></span>](segmented-entry-control-conversion.md)




