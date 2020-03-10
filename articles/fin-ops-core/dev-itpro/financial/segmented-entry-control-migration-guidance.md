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
ms.openlocfilehash: 839feeb0999dabfef3df627cef8d64ac501ac091
ms.sourcegitcommit: a356299be9a593990d9948b3a6b754bd058a5b3b
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/21/2020
ms.locfileid: "3080756"
---
# <a name="migration-guidance-for-segmented-entry-controls"></a><span data-ttu-id="60412-103">セグメント化されたエントリ コントロールに関する移行ガイダンス</span><span class="sxs-lookup"><span data-stu-id="60412-103">Migration guidance for Segmented Entry controls</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="60412-104">このトピックでは、セグメント化エントリ コントロールを Microsoft Dynamics AX 2012 のパターンから Microsoft Dynamics AX の新しいパターンに移行するプロセスについて説明します。</span><span class="sxs-lookup"><span data-stu-id="60412-104">This topic guides you through the process of migrating a Segmented Entry control from the Microsoft Dynamics AX 2012 pattern to the new pattern in Microsoft Dynamics AX.</span></span>

<span data-ttu-id="60412-105">新しい設計の目標は、コントロールの実装をカプセル化し、コントロールをサポートするクラスとやり取りするフォームを必要としないことです。</span><span class="sxs-lookup"><span data-stu-id="60412-105">The goal of the new design is to encapsulate the control implementation and not require that forms interact with the classes that back the control.</span></span> <span data-ttu-id="60412-106">したがって、Microsoft Dynamics AX で、<em> すべてのフォームは、**セグメント化されたエントリ** コントロール インスタンスのアプリケーション プログラミング インターフェイス (API) とのみ対話する必要があります。それらは、コントローラー クラス (**LedgerDimensionAccountController** や **DimensionDynamicAccountController** など)</em> と直接対話してはなりません。</span><span class="sxs-lookup"><span data-stu-id="60412-106">Therefore, in Microsoft Dynamics AX, <em>all forms should interact only with the application programming interface (API) of the **Segmented Entry** control instance. They should not interact directly with the controller classes (such as **LedgerDimensionAccountController** and **DimensionDynamicAccountController**)</em>.</span></span> <span data-ttu-id="60412-107">コントローラー上で以前に操作または呼び出された任意のプロパティは、コントロール上で呼び出される必要があります。</span><span class="sxs-lookup"><span data-stu-id="60412-107">Any property that was previously manipulated or called on the controller must now be called on the control.</span></span> 

<span data-ttu-id="60412-108">**メモ :**</span><span class="sxs-lookup"><span data-stu-id="60412-108">**Notes:**</span></span>

-   <span data-ttu-id="60412-109">一部の API は、コントローラーとコントロールで命名方法が違います。</span><span class="sxs-lookup"><span data-stu-id="60412-109">Some APIs have naming differences between the controller and the control.</span></span> <span data-ttu-id="60412-110">次のテーブルにこれらの API の一覧を示します。</span><span class="sxs-lookup"><span data-stu-id="60412-110">The following table lists these APIs.</span></span>

    | <span data-ttu-id="60412-111">コントローラ メソッド (旧)</span><span class="sxs-lookup"><span data-stu-id="60412-111">Controller method (old)</span></span> | <span data-ttu-id="60412-112">コントロール メソッド (新)</span><span class="sxs-lookup"><span data-stu-id="60412-112">Control method (new)</span></span> |
    |-------------------------|--------------------|
    | <span data-ttu-id="60412-113">parmDate</span><span class="sxs-lookup"><span data-stu-id="60412-113">parmDate</span></span> | <span data-ttu-id="60412-114">parmControlDate</span><span class="sxs-lookup"><span data-stu-id="60412-114">parmControlDate</span></span> | 
    | <span data-ttu-id="60412-115">parmFilterLedgerPostingType</span><span class="sxs-lookup"><span data-stu-id="60412-115">parmFilterLedgerPostingType</span></span> | <span data-ttu-id="60412-116">parmPostingType</span><span class="sxs-lookup"><span data-stu-id="60412-116">parmPostingType</span></span>| 
    | <span data-ttu-id="60412-117">parmDimensionAccountStorageUsage</span><span class="sxs-lookup"><span data-stu-id="60412-117">parmDimensionAccountStorageUsage</span></span> | <span data-ttu-id="60412-118">parmDimensionAccountStorageUsageType</span><span class="sxs-lookup"><span data-stu-id="60412-118">parmDimensionAccountStorageUsageType</span></span> | 
    
-   <span data-ttu-id="60412-119">**例**</span><span class="sxs-lookup"><span data-stu-id="60412-119">**Example**</span></span>
    -   <span data-ttu-id="60412-120">**以前:** controller.parmDate(systemDateGet())</span><span class="sxs-lookup"><span data-stu-id="60412-120">**Before:** controller.parmDate(systemDateGet())</span></span>
    -   <span data-ttu-id="60412-121">**以後:** LedgerAccount.parmControlDate(systemDateGet());</span><span class="sxs-lookup"><span data-stu-id="60412-121">**After:** LedgerAccount.parmControlDate(systemDateGet());</span></span>

    <span data-ttu-id="60412-122">この例では、**コントローラー** &gt; **LedgerDimensionAccountController** インスタンスと **LedgerAccount** &gt; 新規**セグメント化エントリ** コントロールのインスタンス</span><span class="sxs-lookup"><span data-stu-id="60412-122">In this example, **controller** &gt; **LedgerDimensionAccountController** instance and **LedgerAccount** &gt; new **Segmented Entry** control instance.</span></span>
-   <span data-ttu-id="60412-123">コントロールやデータ フィールドでオーバーライドされたメソッドでは、コード アップグレード ルールが、コントローラーのメソッドの呼び出しを、特定のコントローラーを使用していた各コントロール インスタンスのメソッドの呼び出しに置き換えます。</span><span class="sxs-lookup"><span data-stu-id="60412-123">In methods that have been overridden on controls and data fields, the code upgrade rule replaces method calls on the controllers with method calls on each control instance that was using a particular controller.</span></span> 

-   <span data-ttu-id="60412-124">**例**</span><span class="sxs-lookup"><span data-stu-id="60412-124">**Example**</span></span>
    -   <span data-ttu-id="60412-125">**以前:**</span><span class="sxs-lookup"><span data-stu-id="60412-125">**Before:**</span></span>

        ```xpp
        Public void jumpRef()
        {
            ledgerDimensionDefaultAccountcontroller.jumpRef();
        }
        ```

    -   <span data-ttu-id="60412-126">**以後:**</span><span class="sxs-lookup"><span data-stu-id="60412-126">**After:**</span></span>

        ```xpp
        Public void jumpRef()
        {
            segmentedEntryControl1.jumpRef();
            segmentedEntryControl2.jumpRef();
        }
        ```

    <span data-ttu-id="60412-127">これらの変更は、他の場所に移動する必要があるコードをコピーして貼り付ける方が簡単になるように行われています (例: **loadSegments()** およびその他の類似メソッドの一部のインスタンス)。</span><span class="sxs-lookup"><span data-stu-id="60412-127">These changes are made so that it's easier to copy and paste code that must be moved elsewhere (for example, in some instances of **loadSegments()** and other such methods).</span></span> <span data-ttu-id="60412-128">メソッドを削除するかどうか決定するときは、この変更を無視することができます。</span><span class="sxs-lookup"><span data-stu-id="60412-128">You can ignore this change when you decide whether the method can be deleted.</span></span> <span data-ttu-id="60412-129">決定内容は、メソッドにカスタム ロジックにあるかどうかによって異なります。</span><span class="sxs-lookup"><span data-stu-id="60412-129">Your decision should depend on whether the method has any custom logic.</span></span>
-   <span data-ttu-id="60412-130">コードのアップグレード スクリプトは、コントローラーがメソッド内でインスタンス化されるケースを処理しません。</span><span class="sxs-lookup"><span data-stu-id="60412-130">The code upgrade script does not handle cases where a controller is instantiated within a method.</span></span> <span data-ttu-id="60412-131">このような場合は、手動で移行する必要があります。</span><span class="sxs-lookup"><span data-stu-id="60412-131">These cases must be migrated manually.</span></span>
-   <span data-ttu-id="60412-132">Microsoft Dynamics AX 2012 の MRU 機能は、Dynamics AX で削除されました。置き換えの予定はありません。</span><span class="sxs-lookup"><span data-stu-id="60412-132">The MRU functionality from Microsoft Dynamics AX 2012 has been removed in Dynamics AX and won't be replaced.</span></span>
-   <span data-ttu-id="60412-133">**parmTaxCode** が削除されました。</span><span class="sxs-lookup"><span data-stu-id="60412-133">**parmTaxCode** has been removed.</span></span> <span data-ttu-id="60412-134">交換はありません。</span><span class="sxs-lookup"><span data-stu-id="60412-134">There is no replacement.</span></span>

## <a name="properties"></a><span data-ttu-id="60412-135">プロパティ</span><span class="sxs-lookup"><span data-stu-id="60412-135">Properties</span></span>
<span data-ttu-id="60412-136">**セグメント化エントリ**コントロールのカスタム プロパティは、**コントローラー**の下にあります。</span><span class="sxs-lookup"><span data-stu-id="60412-136">The custom properties for the **Segmented Entry** control are found under **Controller**.</span></span> <span data-ttu-id="60412-137">次のスクリーン ショットは、例を示します。</span><span class="sxs-lookup"><span data-stu-id="60412-137">The following screen shot shows an example.</span></span> 

<span data-ttu-id="60412-138">[![111](./media/111.png)](./media/111.png)</span><span class="sxs-lookup"><span data-stu-id="60412-138">[![111](./media/111.png)](./media/111.png)</span></span> 

<span data-ttu-id="60412-139">すべてのプロパティがすべての **コントローラー** クラス タイプに適用されるわけではありません。</span><span class="sxs-lookup"><span data-stu-id="60412-139">Not all properties apply to all **Controller** class types.</span></span> <span data-ttu-id="60412-140">選択したコントローラー クラスに適用されないプロパティは無効になります。</span><span class="sxs-lookup"><span data-stu-id="60412-140">Properties that don't apply to a selected controller class will be disabled.</span></span> <span data-ttu-id="60412-141">次のテーブルは、それぞれのプロパティに関する詳細を示します。</span><span class="sxs-lookup"><span data-stu-id="60412-141">The following table provides details about the properties.</span></span>

| <span data-ttu-id="60412-142">プロパティ</span><span class="sxs-lookup"><span data-stu-id="60412-142">Property</span></span>           | <span data-ttu-id="60412-143">有効な値</span><span class="sxs-lookup"><span data-stu-id="60412-143">Valid values</span></span>      | <span data-ttu-id="60412-144">用途</span><span class="sxs-lookup"><span data-stu-id="60412-144">Usage</span></span>           |
|-------------------------|--------------------|--------------------|
| <span data-ttu-id="60412-145">勘定タイプ フィールド</span><span class="sxs-lookup"><span data-stu-id="60412-145">Account Type Field</span></span> | <span data-ttu-id="60412-146">データ ソースからのフィールド。</span><span class="sxs-lookup"><span data-stu-id="60412-146">A field from the datasource.</span></span> | <span data-ttu-id="60412-147">使用されるアカウントの種類を決定します。</span><span class="sxs-lookup"><span data-stu-id="60412-147">Determines the type of account used.</span></span> <span data-ttu-id="60412-148">通常、複数セグメントの勘定科目から、Cust、Vend、Bank、Project などの他のックアップ テーブルの単一セグメント値への仕訳入力に使用されます。</span><span class="sxs-lookup"><span data-stu-id="60412-148">Typically utilized for journal entry from a multi-segment ledger account to single segment values from other backing tables such as Cust, Vend, Bank, Project and similar.</span></span> | 
| <span data-ttu-id="60412-149">コントローラー クラス</span><span class="sxs-lookup"><span data-stu-id="60412-149">Controller Class</span></span> | <span data-ttu-id="60412-150">6 つのコントローラー クラスのうちの 1 つです。</span><span class="sxs-lookup"><span data-stu-id="60412-150">One of 6 Controller classes.</span></span> <span data-ttu-id="60412-151">たとえば LedgerDimensionDefaultAccountController です。</span><span class="sxs-lookup"><span data-stu-id="60412-151">For example, LedgerDimensionDefaultAccountController.</span></span> | <span data-ttu-id="60412-152">セグメント化されたエントリ コントロールの動作およびパターンを決定します。</span><span class="sxs-lookup"><span data-stu-id="60412-152">Determines the pattern and behavior of the Segmented Entry control.</span></span> <span data-ttu-id="60412-153">このプロパティの詳細については以下で説明します。</span><span class="sxs-lookup"><span data-stu-id="60412-153">More information about this property is provided below.</span></span> | 
| <span data-ttu-id="60412-154">財務勘定を含む</span><span class="sxs-lookup"><span data-stu-id="60412-154">Include Financial Accounts</span></span> | <span data-ttu-id="60412-155">NoYes</span><span class="sxs-lookup"><span data-stu-id="60412-155">NoYes</span></span> | <span data-ttu-id="60412-156">財務勘定である主勘定が有効であるかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="60412-156">Determines if Main accounts that are Financial accounts are valid for use.</span></span> | 
| <span data-ttu-id="60412-157">勘定合計を含む</span><span class="sxs-lookup"><span data-stu-id="60412-157">Include Total Accounts</span></span> | <span data-ttu-id="60412-158">NoYes</span><span class="sxs-lookup"><span data-stu-id="60412-158">NoYes</span></span> | <span data-ttu-id="60412-159">タイプが "合計" の主勘定が有効であるかどうかを判断します。</span><span class="sxs-lookup"><span data-stu-id="60412-159">Determines if Main accounts of type Total are valid for use.</span></span> | 
| <span data-ttu-id="60412-160">既定の勘定です。</span><span class="sxs-lookup"><span data-stu-id="60412-160">Is Default Account</span></span> | <span data-ttu-id="60412-161">TrueFalse</span><span class="sxs-lookup"><span data-stu-id="60412-161">TrueFalse</span></span> | <span data-ttu-id="60412-162">動的アカウントで、アカウントが既定または完全アカウントであるべきかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="60412-162">For a Dynamic account, determines if the account should be a default or full account.</span></span> | 
| <span data-ttu-id="60412-163">主勘定セグメントのロック</span><span class="sxs-lookup"><span data-stu-id="60412-163">Lock Main Account Segment</span></span> | <span data-ttu-id="60412-164">NoYes</span><span class="sxs-lookup"><span data-stu-id="60412-164">NoYes</span></span> | <span data-ttu-id="60412-165">主勘定セグメントがロックされているかどうかをコントロールします。</span><span class="sxs-lookup"><span data-stu-id="60412-165">Controls whether the Main account segment is locked.</span></span> <span data-ttu-id="60412-166">通常は仕訳帳や構成に基づく配分に使用されます。</span><span class="sxs-lookup"><span data-stu-id="60412-166">Typically used in journals and distributions based upon configuration.</span></span> | 
| <span data-ttu-id="60412-167">転記タイプ</span><span class="sxs-lookup"><span data-stu-id="60412-167">Posting Type</span></span> | <span data-ttu-id="60412-168">LedgerPostingType 列挙の値。</span><span class="sxs-lookup"><span data-stu-id="60412-168">A value from the LedgerPostingType enumeration.</span></span> | <span data-ttu-id="60412-169">主勘定が検証され、そのアカウントで使用される転記タイプが許可されているかどうかを確認されます。</span><span class="sxs-lookup"><span data-stu-id="60412-169">The Main account is validated to see if the posting type is allowed to be used with that account.</span></span> | 
| <span data-ttu-id="60412-170">手動入力のブロック状態の検証</span><span class="sxs-lookup"><span data-stu-id="60412-170">Validate Blocked For Manual Entry</span></span> | <span data-ttu-id="60412-171">NoYes</span><span class="sxs-lookup"><span data-stu-id="60412-171">NoYes</span></span> | <span data-ttu-id="60412-172">分析コードの「手動入力のブロック」ステータスを優先するかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="60412-172">Determines if the 'Blocked for Manual Entry' status on the dimension should be respected or not.</span></span> | 


## <a name="controller-class-property"></a><span data-ttu-id="60412-173">コントローラー クラス プロパティ</span><span class="sxs-lookup"><span data-stu-id="60412-173">Controller class property</span></span>
<span data-ttu-id="60412-174">次のテーブルは、それぞれのコントローラーに関する詳細を示します。</span><span class="sxs-lookup"><span data-stu-id="60412-174">The following table provides details about each controller.</span></span>

| <span data-ttu-id="60412-175">コントローラー</span><span class="sxs-lookup"><span data-stu-id="60412-175">Controller</span></span>           | <span data-ttu-id="60412-176">詳細情報</span><span class="sxs-lookup"><span data-stu-id="60412-176">Details</span></span>      | 
|-------------------------|--------------------|
| <span data-ttu-id="60412-177">BudgetLedgerDimension</span><span class="sxs-lookup"><span data-stu-id="60412-177">BudgetLedgerDimension</span></span> | <span data-ttu-id="60412-178">このコントローラーは、セグメント化された入力コントロールのデータ入力の予算に基づくサポートを提供します。</span><span class="sxs-lookup"><span data-stu-id="60412-178">This Controller provides budget based support for data entry in the Segmented Entry control.</span></span> <span data-ttu-id="60412-179">このコント ローラーを使用するときは、勘定構造をセグメント化エントリ コントロールに提供する必要があります。</span><span class="sxs-lookup"><span data-stu-id="60412-179">When using this controller, an Account Structure must be provided to the Segmented Entry control.</span></span> |
| <span data-ttu-id="60412-180">BudgetPlanningLedgerDimension</span><span class="sxs-lookup"><span data-stu-id="60412-180">BudgetPlanningLedgerDimension</span></span> | <span data-ttu-id="60412-181">このコントローラーは、セグメント化された入力コントロールのデータ入力の予算計画に基づくサポートを提供します。</span><span class="sxs-lookup"><span data-stu-id="60412-181">This Controller provides budget planning based support for data entry in the Segmented Entry control.</span></span> <span data-ttu-id="60412-182">このコント ローラーを使用するときは、勘定構造をセグメント化エントリ コントロールに提供する必要があります。</span><span class="sxs-lookup"><span data-stu-id="60412-182">When using this controller, an Account Structure must be provided to the Segmented Entry control.</span></span> |
| <span data-ttu-id="60412-183">DimensionDynamicAccount</span><span class="sxs-lookup"><span data-stu-id="60412-183">DimensionDynamicAccount</span></span> | <span data-ttu-id="60412-184">このコントローラーは、セグメント化された入力コントロールの複数のアカウント タイプのサポートを提供します。</span><span class="sxs-lookup"><span data-stu-id="60412-184">This Controller provides support for multiple account types in the Segmented Entry control.</span></span> |
| <span data-ttu-id="60412-185">LedgerDimensionAccountAlias</span><span class="sxs-lookup"><span data-stu-id="60412-185">LedgerDimensionAccountAlias</span></span> | <span data-ttu-id="60412-186">このコントローラーは、セグメント化された入力コントロールのアカウント エイリアスのサポートを提供します。</span><span class="sxs-lookup"><span data-stu-id="60412-186">This Controller provides support for account aliases in the Segmented Entry control</span></span> |
| <span data-ttu-id="60412-187">LedgerDimensionAccount</span><span class="sxs-lookup"><span data-stu-id="60412-187">LedgerDimensionAccount</span></span> | <span data-ttu-id="60412-188">このコントローラーは、セグメント化された入力コントロールの複数のセグメントのデータ入力のサポートを提供します。</span><span class="sxs-lookup"><span data-stu-id="60412-188">This Controller provides support for multi-segment data entry in the Segmented Entry control.</span></span> |
| <span data-ttu-id="60412-189">LedgerDimensionDefaultAccount</span><span class="sxs-lookup"><span data-stu-id="60412-189">LedgerDimensionDefaultAccount</span></span> | <span data-ttu-id="60412-190">このコントローラーは、セグメント化された入力コントロールの既定のアカウントのサポートを提供します。</span><span class="sxs-lookup"><span data-stu-id="60412-190">This Controller provides support for default accounts in the Segmented Entry control.</span></span> |

## <a name="migration-steps"></a><span data-ttu-id="60412-191">移行ステップ</span><span class="sxs-lookup"><span data-stu-id="60412-191">Migration steps</span></span>
### <a name="step-1"></a><span data-ttu-id="60412-192">ステップ１</span><span class="sxs-lookup"><span data-stu-id="60412-192">Step 1</span></span>

#### <a name="ax-2012"></a><span data-ttu-id="60412-193">AX 2012</span><span class="sxs-lookup"><span data-stu-id="60412-193">AX 2012</span></span>

<span data-ttu-id="60412-194">**SegmentedEntry** は任意のコントロールの横にあるタイプとして表示され、**SegmentedEntryControl** と変更します。</span><span class="sxs-lookup"><span data-stu-id="60412-194">If **SegmentedEntry** appears as the type next to any control, change it to **SegmentedEntryControl**.</span></span> 

<span data-ttu-id="60412-195">[![SegmentMigrate01](./media/segmentmigrate01.png)](./media/segmentmigrate01.png)</span><span class="sxs-lookup"><span data-stu-id="60412-195">[![SegmentMigrate01](./media/segmentmigrate01.png)](./media/segmentmigrate01.png)</span></span>

#### <a name="dynamics-ax"></a><span data-ttu-id="60412-196">Dynamics AX</span><span class="sxs-lookup"><span data-stu-id="60412-196">Dynamics AX</span></span>

<span data-ttu-id="60412-197">簡単な方法は古いコントロールの名前に「\_旧」を追加し、新しいコントロール (コントロールの元の名前がある必要があります) を付け加え、すべての設定を移行した後、古いコントロールを削除します。</span><span class="sxs-lookup"><span data-stu-id="60412-197">An easy method is to append "\_old" to the name of the old control, add the new control (which should have the original name of the control), migrate all the settings over, and then delete the old control.</span></span> 

> [!NOTE] 
> <span data-ttu-id="60412-198">コントロールを参照するテストおよび他のコードが破損しないようにするには、新しいコントロールが古いコントロールと同じ名前であることを確認します。</span><span class="sxs-lookup"><span data-stu-id="60412-198">To prevent tests and other code that references the control from breaking, make sure that the new control has the same name as the old control.</span></span> <span data-ttu-id="60412-199">新しいコントロールを追加するには、**Segmented Entry** コントロールを含む親コントロールを右クリックし、**New** &gt; **SegmentedEntryControl** を選択します。</span><span class="sxs-lookup"><span data-stu-id="60412-199">To add the new control, right-click the parent control that will contain the **Segmented Entry** control, and then select **New** &gt; **SegmentedEntryControl**.</span></span> 

<span data-ttu-id="60412-200">[![SegmentMigrate02](./media/segmentmigrate02-623x1024.png)](./media/segmentmigrate02.png)</span><span class="sxs-lookup"><span data-stu-id="60412-200">[![SegmentMigrate02](./media/segmentmigrate02-623x1024.png)](./media/segmentmigrate02.png)</span></span> 

<span data-ttu-id="60412-201">次のスクリーンショットは、新しいコントロールの外観を示しています。</span><span class="sxs-lookup"><span data-stu-id="60412-201">The following screen shot shows how new control will look.</span></span> 

<span data-ttu-id="60412-202">[![SegmentMigrate03](./media/segmentmigrate03.png)](./media/segmentmigrate03.png)</span><span class="sxs-lookup"><span data-stu-id="60412-202">[![SegmentMigrate03](./media/segmentmigrate03.png)](./media/segmentmigrate03.png)</span></span>

### <a name="step-2"></a><span data-ttu-id="60412-203">ステップ２</span><span class="sxs-lookup"><span data-stu-id="60412-203">Step 2</span></span>

#### <a name="ax-2012"></a><span data-ttu-id="60412-204">AX 2012</span><span class="sxs-lookup"><span data-stu-id="60412-204">AX 2012</span></span>

<span data-ttu-id="60412-205"> **jumpRef()** コントロール/メソッドをオーバーライドします。</span><span class="sxs-lookup"><span data-stu-id="60412-205">Override the  **jumpRef()** control/field method.</span></span>

```xpp
public void jumpRef()
{
    ledgerDimensionDefaultAccountController.jumpRef();
}
```

#### <a name="dynamics-ax"></a><span data-ttu-id="60412-206">Dynamics AX</span><span class="sxs-lookup"><span data-stu-id="60412-206">Dynamics AX</span></span>

<span data-ttu-id="60412-207">他の機能が含まれなくなった場合は **jumpRef()** メソッドを完全に削除します。</span><span class="sxs-lookup"><span data-stu-id="60412-207">Remove the **jumpRef()** method completely if it contains no other functionality.</span></span> <span data-ttu-id="60412-208">その他のカスタム **jumpRef** 機能がある場合は、それをそのままにします。</span><span class="sxs-lookup"><span data-stu-id="60412-208">If there is other custom **jumpRef** functionality, leave that.</span></span> <span data-ttu-id="60412-209">ただし、**jumpRef** がコントロールによって自動的に処理されます。</span><span class="sxs-lookup"><span data-stu-id="60412-209">However, **jumpRef** is otherwise automatically handled by the control.</span></span>

### <a name="step-3"></a><span data-ttu-id="60412-210">ステップ 3</span><span class="sxs-lookup"><span data-stu-id="60412-210">Step 3</span></span>

#### <a name="ax-2012"></a><span data-ttu-id="60412-211">AX 2012</span><span class="sxs-lookup"><span data-stu-id="60412-211">AX 2012</span></span>

<span data-ttu-id="60412-212">**loadAutoCompleteData()** コントロール メソッドをオーバーライドします。</span><span class="sxs-lookup"><span data-stu-id="60412-212">Override the **loadAutoCompleteData()** control method.</span></span>

```xpp
public void loadAutoCompleteData(LoadAutoCompleteDataEventArgs _e)
{
    ledgerDimensionDefaultAccountController.loadAutoCompleteData(_e);
    super(_e);
}
```

#### <a name="dynamics-ax"></a><span data-ttu-id="60412-213">Dynamics AX</span><span class="sxs-lookup"><span data-stu-id="60412-213">Dynamics AX</span></span>

<span data-ttu-id="60412-214">**loadAutoCompleteData()** メソッドを削除します。</span><span class="sxs-lookup"><span data-stu-id="60412-214">Remove the **loadAutoCompleteData()** method.</span></span>

### <a name="step-4"></a><span data-ttu-id="60412-215">ステップ 4</span><span class="sxs-lookup"><span data-stu-id="60412-215">Step 4</span></span>

#### <a name="ax-2012"></a><span data-ttu-id="60412-216">AX 2012</span><span class="sxs-lookup"><span data-stu-id="60412-216">AX 2012</span></span>

<span data-ttu-id="60412-217">**loadSegments()** コントロール メソッドをオーバーライドします。</span><span class="sxs-lookup"><span data-stu-id="60412-217">Override the **loadSegments()** control method.</span></span>

```xpp
public void loadSegments()
{
    super();
    ledgerDimensionDefaultAccountController.loadSegments();
    ledgerDimensionDefaultAccountController.parmControl(this);
}
```

#### <a name="dynamics-ax"></a><span data-ttu-id="60412-218">Dynamics AX</span><span class="sxs-lookup"><span data-stu-id="60412-218">Dynamics AX</span></span>

<span data-ttu-id="60412-219">**loadSegments()** メソッドが、コントローラーの **loadSegments()** および **parmControl()** メソッドを呼ぶ以外に何もしない場合は、それを削除します。</span><span class="sxs-lookup"><span data-stu-id="60412-219">If the **loadSegments()** method does nothing except call the controller's **loadSegments()** and **parmControl()** methods, remove it.</span></span> <span data-ttu-id="60412-220">ただし、**parmControl()** 呼び出しに渡される SEC コントロール インスタンスをメモしておきます。</span><span class="sxs-lookup"><span data-stu-id="60412-220">However, make a note of the SEC control instance that is passed to the **parmControl()** call.</span></span> <span data-ttu-id="60412-221">呼び出されていたメソッドは、そのインスタンスで呼び出される必要があります。</span><span class="sxs-lookup"><span data-stu-id="60412-221">The methods that were being called will now have to be called on that instance.</span></span>

### <a name="step-5"></a><span data-ttu-id="60412-222">ステップ 5</span><span class="sxs-lookup"><span data-stu-id="60412-222">Step 5</span></span>

#### <a name="ax-2012"></a><span data-ttu-id="60412-223">AX 2012</span><span class="sxs-lookup"><span data-stu-id="60412-223">AX 2012</span></span>

<span data-ttu-id="60412-224">**loadSegments()** コントロール メソッドをオーバーライドします。</span><span class="sxs-lookup"><span data-stu-id="60412-224">Override the **loadSegments()** control method.</span></span>

```xpp
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
```

#### <a name="dynamics-ax"></a><span data-ttu-id="60412-225">Dynamics AX</span><span class="sxs-lookup"><span data-stu-id="60412-225">Dynamics AX</span></span>

<span data-ttu-id="60412-226">**loadSegments()** メソッドがコントローラーでのパラメーターを設定するために使用された場合、**パラメーター** メソッドへの呼び出しは、**パラメーター** メソッドのソースを変更することができるすべての場所に移動する必要があります。</span><span class="sxs-lookup"><span data-stu-id="60412-226">If the **loadSegments()** method was used to set parameters on the controller, the calls to **parm** method must be moved to every location where the source of the **parm** method can change.</span></span> <span data-ttu-id="60412-227">ほとんどの場合、これらの場所は対応するデータ フィールドの **modified()** メソッドおよび/またはデータ ソースの **active()** メソッドです。</span><span class="sxs-lookup"><span data-stu-id="60412-227">In most cases, these locations are the **modified()** method on the corresponding data field and/or the **active()** method on the data source.</span></span> <span data-ttu-id="60412-228">たとえば、**loadSegments()** の移行したコードの一部は、左側で上書きをし、次のようになります。</span><span class="sxs-lookup"><span data-stu-id="60412-228">For example, some of the migrated code for the **loadSegments()** override on the left would look like this.</span></span>

```xpp
dimAccountController.parmControl(this) -> No longer needed.
```

<span data-ttu-id="60412-229">**parmControl()** 呼び出しに渡される SEC コントロール インスタンスをメモしておきます。</span><span class="sxs-lookup"><span data-stu-id="60412-229">Make a note of the SEC control instance that is passed on to the **parmControl()** call.</span></span> <span data-ttu-id="60412-230">コントローラー上で呼び出されていたメソッドは、そのインスタンスで呼び出される必要があります。</span><span class="sxs-lookup"><span data-stu-id="60412-230">The methods that were being called on the controller will now have to be called on that instance.</span></span>

```xpp
dimAccountController.parmJournalName(ledgerJournalTable.JournalName) ->
LedgerJournalTable data source,
JournalName field,
public void modified()
{
    .parmJournalName(ledgerJournalTable.JournalName);
}
```

<span data-ttu-id="60412-231">**LedgerJournalTable データ ソース**</span><span class="sxs-lookup"><span data-stu-id="60412-231">**LedgerJournalTable data source**</span></span>

    public void active()
    {
        .parmJournalName(ledgerJournalTable.JournalName);
    }

> [!NOTE]
> <span data-ttu-id="60412-232">**loadSegments()** メソッドからすべてのコードを削除したら、そのメソッドを削除できます。</span><span class="sxs-lookup"><span data-stu-id="60412-232">After you've moved all the code out of the **loadSegments()** method, you can delete the method.</span></span>

### <a name="step-6"></a><span data-ttu-id="60412-233">ステップ 6</span><span class="sxs-lookup"><span data-stu-id="60412-233">Step 6</span></span>

#### <a name="ax-2012"></a><span data-ttu-id="60412-234">AX 2012</span><span class="sxs-lookup"><span data-stu-id="60412-234">AX 2012</span></span>

<span data-ttu-id="60412-235">**loadSegments()** コントロール メソッドをオーバーライドします。</span><span class="sxs-lookup"><span data-stu-id="60412-235">Override the **loadSegments()** control method.</span></span> <span data-ttu-id="60412-236">場合によっては、**loadSegments()** メソッドは、テーブル バッファを使用してコントローラーでパラメーターを設定することがありますが、そのテーブル バッファはフォーム上のデータ ソースではありません。</span><span class="sxs-lookup"><span data-stu-id="60412-236">In some cases, the **loadSegments()** method might use a table buffer to set parameters on the controller, but that table buffer isn't a data source on the form.</span></span> <span data-ttu-id="60412-237">たとえば、**LedgerJournalTransDaily** フォームでは、**loadSegments()** の元の実装は次のようになります。</span><span class="sxs-lookup"><span data-stu-id="60412-237">For example, on the **LedgerJournalTransDaily** form, the original implementation of **loadSegments()** looked like this.</span></span>

```xpp
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
```

<span data-ttu-id="60412-238">**JournalName** プロパティは、ledgerJournalTable バッファから設定されますが、LedgerJournalTable テーブルはフォームのデータ ソースではないことに注意してください。</span><span class="sxs-lookup"><span data-stu-id="60412-238">Note that the **JournalName** property is set from the ledgerJournalTable buffer, but the LedgerJournalTable table isn't a data source on the form.</span></span>

#### <a name="dynamics-ax"></a><span data-ttu-id="60412-239">Dynamics AX</span><span class="sxs-lookup"><span data-stu-id="60412-239">Dynamics AX</span></span>

<span data-ttu-id="60412-240">このような場合、そのコードをデータ ソースの **active()** メソッド、またはデータ フィールドの **modified()** メソッドに移動できません。</span><span class="sxs-lookup"><span data-stu-id="60412-240">In such cases, you can't move that code to either the **active()** method of a data source or the **modified()** method on the data field.</span></span> <span data-ttu-id="60412-241">代わりに、テーブル バッファが設定されている場所を特定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="60412-241">Instead, you should identify where the table buffer is being set.</span></span> <span data-ttu-id="60412-242">たとえば、**LedgerJournalTransDaily** フォームの元の実装では、ledgerJournalTable バッファはフォームの **initLedger()** メソッドで設定されました。</span><span class="sxs-lookup"><span data-stu-id="60412-242">For example, in the original implementation of the **LedgerJournalTransDaily** form, the ledgerJournalTable buffer was set in the **initLedger()** method on the form.</span></span> <span data-ttu-id="60412-243">**parmJournalName()** に渡される値は、バッファが **initLedger()** メソッドで再割り当てされる場合のみ変更できることを明らかにする必要があります。</span><span class="sxs-lookup"><span data-stu-id="60412-243">It should be evident that the value that is passed to **parmJournalName()** can change only when the buffer is reassigned in the **initLedger()** method.</span></span> <span data-ttu-id="60412-244">したがって、バッファを割り当てた後、コードを **initLedger()** メソッドに移動する必要があります。</span><span class="sxs-lookup"><span data-stu-id="60412-244">Therefore, code would have to be moved to the **initLedger()** method after the assignment of the buffer.</span></span> <span data-ttu-id="60412-245">また、一般的なガイドラインに従って、コントロールインスタンスに対して **parmJournalName()** メソッドが呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="60412-245">Also, in accordance with the general guidelines, the **parmJournalName()** method would be called on the control instance.</span></span>

```xpp
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
```

### <a name="step-7"></a><span data-ttu-id="60412-246">ステップ 7</span><span class="sxs-lookup"><span data-stu-id="60412-246">Step 7</span></span>

#### <a name="ax-2012"></a><span data-ttu-id="60412-247">AX 2012</span><span class="sxs-lookup"><span data-stu-id="60412-247">AX 2012</span></span>

<span data-ttu-id="60412-248">**segmentValueChanged()** コントロール メソッドをオーバーライドします。</span><span class="sxs-lookup"><span data-stu-id="60412-248">Override the **segmentValueChanged()** control method.</span></span>

```xpp
public void segmentValueChanged(SegmentValueChangedEventArgs _e)
{
    super(_e);
    ledgerDimensionDefaultAccountController.segmentValueChanged(_e);
}
```

#### <a name="dynamics-ax"></a><span data-ttu-id="60412-249">Dynamics AX</span><span class="sxs-lookup"><span data-stu-id="60412-249">Dynamics AX</span></span>

<span data-ttu-id="60412-250">**segmentValueChanged()** を実装した場合に、コントローラー上で **super()** と **segmentValueChanged()** メソッドを呼び出す以外何も起こらない場合は、メソッドを削除することができます。</span><span class="sxs-lookup"><span data-stu-id="60412-250">If the implementation of **segmentValueChanged()** does nothing except call **super()** and the **segmentValueChanged()** method on the controller, you can remove the method.</span></span>

### <a name="step-8"></a><span data-ttu-id="60412-251">ステップ 8</span><span class="sxs-lookup"><span data-stu-id="60412-251">Step 8</span></span>

#### <a name="ax-2012"></a><span data-ttu-id="60412-252">AX 2012</span><span class="sxs-lookup"><span data-stu-id="60412-252">AX 2012</span></span>

<span data-ttu-id="60412-253">**segmentValueChanged()** コントロール メソッドをオーバーライドします。</span><span class="sxs-lookup"><span data-stu-id="60412-253">Override the **segmentValueChanged()** control method.</span></span>

```xpp
public void segmentValueChanged(SegmentValueChangedEventArgs _e)
{
    super(_e);

    dimOffsetAccountController.segmentValueChanged(_e);
    currentOffsetMainAccountId = ledgerJournalEngine.onOffsetAccountSegmentChanged(dimOffsetAccountController, currentOffsetMainAccountId, ledgerJournalTrans);
}
```

#### <a name="dynamics-ax"></a><span data-ttu-id="60412-254">Dynamics AX</span><span class="sxs-lookup"><span data-stu-id="60412-254">Dynamics AX</span></span>

<span data-ttu-id="60412-255">**segmentValueChanged()** の実装に追加のロジックがある場合、次に示すように、メソッドを **onSegmentChanged()** メソッドに置き換える必要があります。</span><span class="sxs-lookup"><span data-stu-id="60412-255">If the implementation of **segmentValueChanged()** has additional logic, you must replace the method with the **onSegmentChanged()** method, as shown here.</span></span>

```xpp
public void onSegmentChanged(DimensionControlSegment _segment)
{
    currentOffsetMainAccountId = ledgerJournalEngine.onOffsetAccountSegmentChanged(this, currentOffsetMainAccountId, ledgerJournalTrans);
}
```

<span data-ttu-id="60412-256">**メモ :**</span><span class="sxs-lookup"><span data-stu-id="60412-256">**Notes:**</span></span>

-   <span data-ttu-id="60412-257">**onSegmentChanged()** メソッドを追加するには、次の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="60412-257">To add the **onSegmentChanged()** method, follow these steps:</span></span>
    1.  <span data-ttu-id="60412-258">メソッドを追加するには、**セグメント化されたエントリ**コントロールを展開します。</span><span class="sxs-lookup"><span data-stu-id="60412-258">Expand the **Segmented Entry** control to add the method to.</span></span>
    2.  <span data-ttu-id="60412-259">**メソッド** ノードをクリックし、**オーバーライド** &gt; **onSegmentChanged** を選択します。</span><span class="sxs-lookup"><span data-stu-id="60412-259">Right-click the **Methods** node, and then select **Override** &gt; **onSegmentChanged**.</span></span>
-   <span data-ttu-id="60412-260">新しいメソッドは、**super()** またはコントロールまたはコントローラーのいずれかの他のメソッドを呼び出す必要はありません。</span><span class="sxs-lookup"><span data-stu-id="60412-260">The new method doesn't have to call **super()** or any other method on either the control or the controller.</span></span>

### <a name="step-9"></a><span data-ttu-id="60412-261">ステップ 9</span><span class="sxs-lookup"><span data-stu-id="60412-261">Step 9</span></span>

#### <a name="ax-2012"></a><span data-ttu-id="60412-262">AX 2012</span><span class="sxs-lookup"><span data-stu-id="60412-262">AX 2012</span></span>

<span data-ttu-id="60412-263">**validate()** コントロール メソッドをオーバーライドします。</span><span class="sxs-lookup"><span data-stu-id="60412-263">Override the **validate()** control method.</span></span>

```xpp
public boolean validate()
{
    boolean isValid;
    isValid = super();
    isValid = ledgerDimensionDefaultAccountController.validate() && isValid;

    return isValid;
}
```

#### <a name="dynamics-ax"></a><span data-ttu-id="60412-264">Dynamics AX</span><span class="sxs-lookup"><span data-stu-id="60412-264">Dynamics AX</span></span>

<span data-ttu-id="60412-265">追加の検証がある場合以外は、**validate()** メソッドを削除します。</span><span class="sxs-lookup"><span data-stu-id="60412-265">Remove the **validate()** method, unless you have additional validation.</span></span> <span data-ttu-id="60412-266">**super()** 呼び出しは、このコードが行っていたすべてのことを行います。</span><span class="sxs-lookup"><span data-stu-id="60412-266">The **super()** call does everything that this code used to do.</span></span> <span data-ttu-id="60412-267">したがって、保持している新しいコードのみを残しておいてください。</span><span class="sxs-lookup"><span data-stu-id="60412-267">Therefore, keep only any new code that you have.</span></span>

### <a name="step-10"></a><span data-ttu-id="60412-268">ステップ 10</span><span class="sxs-lookup"><span data-stu-id="60412-268">Step 10</span></span>

#### <a name="ax-2012"></a><span data-ttu-id="60412-269">AX 2012</span><span class="sxs-lookup"><span data-stu-id="60412-269">AX 2012</span></span>

<span data-ttu-id="60412-270">**lookup()** コントロール メソッドをオーバーライドします。</span><span class="sxs-lookup"><span data-stu-id="60412-270">Override the **lookup()** control method.</span></span>

```xpp
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
```

#### <a name="dynamics-ax"></a><span data-ttu-id="60412-271">Dynamics AX</span><span class="sxs-lookup"><span data-stu-id="60412-271">Dynamics AX</span></span>

<span data-ttu-id="60412-272">**lookup()** メソッドをそのままにします。</span><span class="sxs-lookup"><span data-stu-id="60412-272">Leave the **lookup()** method as it is.</span></span>

### <a name="step-11"></a><span data-ttu-id="60412-273">ステップ 11</span><span class="sxs-lookup"><span data-stu-id="60412-273">Step 11</span></span>

#### <a name="ax-2012"></a><span data-ttu-id="60412-274">AX 2012</span><span class="sxs-lookup"><span data-stu-id="60412-274">AX 2012</span></span>

<span data-ttu-id="60412-275"> **lookupReference()** コントロール メソッドをオーバーライドします。</span><span class="sxs-lookup"><span data-stu-id="60412-275">Override the **lookupReference()** control method.</span></span>

```xpp
public Common lookupReference()
{
    Common ret;
    ret = super();
    return ret;
}
```

#### <a name="dynamics-ax"></a><span data-ttu-id="60412-276">Dynamics AX</span><span class="sxs-lookup"><span data-stu-id="60412-276">Dynamics AX</span></span>

<span data-ttu-id="60412-277">**lookupReference()** メソッドが既定の実装を使用している場合、それを削除することができます。</span><span class="sxs-lookup"><span data-stu-id="60412-277">If the **lookupReference()** method uses the default implementation, you can delete it.</span></span>

### <a name="step-12"></a><span data-ttu-id="60412-278">ステップ 12</span><span class="sxs-lookup"><span data-stu-id="60412-278">Step 12</span></span>

#### <a name="ax-2012"></a><span data-ttu-id="60412-279">AX 2012</span><span class="sxs-lookup"><span data-stu-id="60412-279">AX 2012</span></span>

<span data-ttu-id="60412-280">**modified()** コントロール メソッドをオーバーライドします。</span><span class="sxs-lookup"><span data-stu-id="60412-280">Override the **modified()** control method.</span></span>

```xpp
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
```

#### <a name="dynamics-ax"></a><span data-ttu-id="60412-281">Dynamics AX</span><span class="sxs-lookup"><span data-stu-id="60412-281">Dynamics AX</span></span>

<span data-ttu-id="60412-282">**modified()** メソッドをそのままにします。</span><span class="sxs-lookup"><span data-stu-id="60412-282">Leave the **modified()** method as it is.</span></span>

### <a name="step-13"></a><span data-ttu-id="60412-283">ステップ 13</span><span class="sxs-lookup"><span data-stu-id="60412-283">Step 13</span></span>

#### <a name="ax-2012"></a><span data-ttu-id="60412-284">AX 2012</span><span class="sxs-lookup"><span data-stu-id="60412-284">AX 2012</span></span>

<span data-ttu-id="60412-285">**gotFocus()** コントロール メソッドをオーバーライドします。</span><span class="sxs-lookup"><span data-stu-id="60412-285">Override the **gotFocus()** control method.</span></span>

```xpp
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
```

#### <a name="dynamics-ax"></a><span data-ttu-id="60412-286">Dynamics AX</span><span class="sxs-lookup"><span data-stu-id="60412-286">Dynamics AX</span></span>

<span data-ttu-id="60412-287">このアプローチは、**loadSegments()** メソッドのアプローチに似ています。</span><span class="sxs-lookup"><span data-stu-id="60412-287">The approach is similar to the approach for the **loadSegments()** method.</span></span> <span data-ttu-id="60412-288">**parm** メソッドのソースが変更できるすべての場所にコードを移動する必要があります。</span><span class="sxs-lookup"><span data-stu-id="60412-288">The code must be moved to every location where the source of the **parm** method can change.</span></span> <span data-ttu-id="60412-289">ほとんどの場合、これらの場所は対応するデータ フィールドの **modified()** メソッドおよび/またはデータ ソースの **active()** メソッドです。</span><span class="sxs-lookup"><span data-stu-id="60412-289">In most cases, these locations are the **modified()** method on the corresponding data field and/or the **active()** method on the data source.</span></span> <span data-ttu-id="60412-290">たとえば、上記のコードでは、移行したコードはこのようになります。</span><span class="sxs-lookup"><span data-stu-id="60412-290">For example, for the preceding code, the migrated code would look like this.</span></span>

```xpp
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
```

> [!NOTE] 
> <span data-ttu-id="60412-291">**gotFocus()** メソッドからすべてのコードを削除したら、そのメソッドを削除できます。</span><span class="sxs-lookup"><span data-stu-id="60412-291">After all the code has been moved out of the **gotFocus()** method, you can delete the method.</span></span>

### <a name="step-14"></a><span data-ttu-id="60412-292">ステップ 14</span><span class="sxs-lookup"><span data-stu-id="60412-292">Step 14</span></span>

#### <a name="ax-2012"></a><span data-ttu-id="60412-293">AX 2012</span><span class="sxs-lookup"><span data-stu-id="60412-293">AX 2012</span></span>

<span data-ttu-id="60412-294">フォーム **init()** メソッド:</span><span class="sxs-lookup"><span data-stu-id="60412-294">In the form **init()** method:</span></span>

```xpp
ledgerDimensionDefaultAccountController = LedgerDimensionDefaultAccountController::construct(vendParameters_ds, fieldStr(VendParameters, ClearingLedgerDimension));
```

#### <a name="dynamics-ax"></a><span data-ttu-id="60412-295">Dynamics AX</span><span class="sxs-lookup"><span data-stu-id="60412-295">Dynamics AX</span></span>

<span data-ttu-id="60412-296">コントロールで以下のプロパティを設定します。</span><span class="sxs-lookup"><span data-stu-id="60412-296">Set the following properties on the control:</span></span>

-   <span data-ttu-id="60412-297">**データ ソース**</span><span class="sxs-lookup"><span data-stu-id="60412-297">**Data Source**</span></span>
-   <span data-ttu-id="60412-298">**参照フィールド**</span><span class="sxs-lookup"><span data-stu-id="60412-298">**Reference Field**</span></span>
-   <span data-ttu-id="60412-299">**コントローラー クラス**</span><span class="sxs-lookup"><span data-stu-id="60412-299">**Controller Class**</span></span>

<span data-ttu-id="60412-300">[![SegmentMigrate04](./media/segmentmigrate04.png)](./media/segmentmigrate04.png)</span><span class="sxs-lookup"><span data-stu-id="60412-300">[![SegmentMigrate04](./media/segmentmigrate04.png)](./media/segmentmigrate04.png)</span></span> 

<span data-ttu-id="60412-301">[![SegmentMigrate05](./media/segmentmigrate05.png)](./media/segmentmigrate05.png)</span><span class="sxs-lookup"><span data-stu-id="60412-301">[![SegmentMigrate05](./media/segmentmigrate05.png)](./media/segmentmigrate05.png)</span></span> 

> [!NOTE]
> <span data-ttu-id="60412-302">コントロールが機能するには、コントローラクラスが必要です。</span><span class="sxs-lookup"><span data-stu-id="60412-302">A controller class is required for the control to work.</span></span> <span data-ttu-id="60412-303">したがって、**Controller Class** プロパティが設定されていないと、ランタイム エラーがスローされます。</span><span class="sxs-lookup"><span data-stu-id="60412-303">Therefore, a run-time error will be thrown if the **Controller Class** property isn't set.</span></span>

### <a name="step-15"></a><span data-ttu-id="60412-304">ステップ 15</span><span class="sxs-lookup"><span data-stu-id="60412-304">Step 15</span></span>

#### <a name="ax-2012"></a><span data-ttu-id="60412-305">AX 2012</span><span class="sxs-lookup"><span data-stu-id="60412-305">AX 2012</span></span>

```xpp
ledgerDimensionAccountController.setValues(ledgerJournalTrans.DefaultDimension, false);
```

#### <a name="dynamics-ax"></a><span data-ttu-id="60412-306">Dynamics AX</span><span class="sxs-lookup"><span data-stu-id="60412-306">Dynamics AX</span></span>

<span data-ttu-id="60412-307">分析コードの指定子のマップを作成してから、**セグメント化されたエントリ**コントロールの **setDimensionSpecifiers** メソッドに送信する必要があります。</span><span class="sxs-lookup"><span data-stu-id="60412-307">A map of the dimension specifiers must be created that can then be sent into the **Segmented Entry** control's **setDimensionSpecifiers** method.</span></span>

```xpp
Map defaultDimensionSpecifiers = LedgerDimensionDefaultingEngine::getDefaultDimensionSpecifiers(ledgerJournalTable.DefaultDimension);

TmpLedgerJournalSplitLines_LedgerAccount.setDimensionSpecifiers(defaultDimensionSpecifiers, false);
```

> [!NOTE]
> <span data-ttu-id="60412-308">分析コードの指定子のマップに何かを追加してからコントロールに送ることができます。</span><span class="sxs-lookup"><span data-stu-id="60412-308">You can add anything to the dimension specifiers map before it's sent to the control.</span></span> <span data-ttu-id="60412-309">新しいマップをここで作成することもできます。</span><span class="sxs-lookup"><span data-stu-id="60412-309">You can also create a new map here.</span></span> <span data-ttu-id="60412-310">(同様のロジックに関しては、**LedgerJournalEngine** クラス内の **onSegmentChangedForPrimaryAccount** メソッドを参照してください。)</span><span class="sxs-lookup"><span data-stu-id="60412-310">(See the **onSegmentChangedForPrimaryAccount** method in the **LedgerJournalEngine** class for similar logic.)</span></span>

### <a name="step-16"></a><span data-ttu-id="60412-311">ステップ 16</span><span class="sxs-lookup"><span data-stu-id="60412-311">Step 16</span></span>

#### <a name="ax-2012"></a><span data-ttu-id="60412-312">AX 2012</span><span class="sxs-lookup"><span data-stu-id="60412-312">AX 2012</span></span>

<span data-ttu-id="60412-313">**parmControl()** メソッド呼び出し:(これらは通常、フォームの **init()** メソッドまたはコントロールで上書きされたメソッドのうちの 1 つに存在します。)</span><span class="sxs-lookup"><span data-stu-id="60412-313">**parmControl()** method calls: (These are typically present in the form's **init()** method or one of the methods that are overridden on the control.)</span></span>

```xpp
ledgerDimensionDefaultAccountController.parmControl(clearingAccount);
```

#### <a name="dynamics-ax"></a><span data-ttu-id="60412-314">Dynamics AX</span><span class="sxs-lookup"><span data-stu-id="60412-314">Dynamics AX</span></span>

<span data-ttu-id="60412-315">必要がなくなったため、このコード行を削除します。</span><span class="sxs-lookup"><span data-stu-id="60412-315">Remove this line of code, because it's no longer required.</span></span> <span data-ttu-id="60412-316">ただし、最初にどのコントローラーがどのコントロールで使用されるかを記録します。</span><span class="sxs-lookup"><span data-stu-id="60412-316">However, first make a note of which controller is used with which control.</span></span> <span data-ttu-id="60412-317">たとえば、この場合、ledgerDimensionDefaultAccountController が ClearingAccount SEC で使用されています。</span><span class="sxs-lookup"><span data-stu-id="60412-317">For example, in this case, ledgerDimensionDefaultAccountController is being used with the ClearingAccount SEC.</span></span> <span data-ttu-id="60412-318">マッピングは、コントロールでコントローラー オブジェクトのメソッド呼び出しを対応するメソッド呼び出しに置き換える場合、およびデザイン時にプロパティを設定する場合に必要です。</span><span class="sxs-lookup"><span data-stu-id="60412-318">A mapping is required when you replace method calls on controller objects with corresponding method calls on the control, and when you set the properties at design time.</span></span>

### <a name="step-17"></a><span data-ttu-id="60412-319">ステップ 17</span><span class="sxs-lookup"><span data-stu-id="60412-319">Step 17</span></span>

#### <a name="ax-2012"></a><span data-ttu-id="60412-320">AX 2012</span><span class="sxs-lookup"><span data-stu-id="60412-320">AX 2012</span></span>

<span data-ttu-id="60412-321">フォーム **init()** メソッド:</span><span class="sxs-lookup"><span data-stu-id="60412-321">In the form **init()** method:</span></span>

```xpp
ledgerDimensionDefaultAccountController.parmFilterLedgerPostingType(LedgerPostingType::VendSettlement);
```

#### <a name="dynamics-ax"></a><span data-ttu-id="60412-322">Dynamics AX</span><span class="sxs-lookup"><span data-stu-id="60412-322">Dynamics AX</span></span>

<span data-ttu-id="60412-323">これは、コントロールの**転記タイプ**プロパティです。</span><span class="sxs-lookup"><span data-stu-id="60412-323">This is the **Posting Type** property on the control.</span></span> <span data-ttu-id="60412-324">**PostingType** プロパティを設定する必要があるコントロールは、**parmControl()** 呼び出しを見て派生したマッピングの詳細から判別できます。</span><span class="sxs-lookup"><span data-stu-id="60412-324">The control that the **PostingType** property must be set on can be determined from the mapping details that are derived by looking at the **parmControl()** call.</span></span> 

<span data-ttu-id="60412-325">[![SegmentMigrate06](./media/segmentmigrate06.png)](./media/segmentmigrate06.png)</span><span class="sxs-lookup"><span data-stu-id="60412-325">[![SegmentMigrate06](./media/segmentmigrate06.png)](./media/segmentmigrate06.png)</span></span> 

<span data-ttu-id="60412-326">これらのプロパティは、コントロール インスタンスで **parm** メソッドを介してコードで設定することもできます。</span><span class="sxs-lookup"><span data-stu-id="60412-326">These properties can also be set in code, through corresponding **parm** methods on the control instance.</span></span> <span data-ttu-id="60412-327">次に例を示します。</span><span class="sxs-lookup"><span data-stu-id="60412-327">Here's an example.</span></span>

```xpp
ClearingAccount.parmPostingType(LedgerPostingType::VendSettlement);
```

### <a name="step-18"></a><span data-ttu-id="60412-328">ステップ 18</span><span class="sxs-lookup"><span data-stu-id="60412-328">Step 18</span></span>

#### <a name="ax-2012"></a><span data-ttu-id="60412-329">AX 2012</span><span class="sxs-lookup"><span data-stu-id="60412-329">AX 2012</span></span>

<span data-ttu-id="60412-330">元帳分析コードのデータ ソース フィールドで **resolveReference()** をオーバーライドします。</span><span class="sxs-lookup"><span data-stu-id="60412-330">Override **resolveReference()** in the data source field for the ledger dimension.</span></span> 

<span data-ttu-id="60412-331">[![SegmentMigrate07](./media/segmentmigrate07.png)](./media/segmentmigrate07.png)</span><span class="sxs-lookup"><span data-stu-id="60412-331">[![SegmentMigrate07](./media/segmentmigrate07.png)](./media/segmentmigrate07.png)</span></span>

#### <a name="dynamics-ax"></a><span data-ttu-id="60412-332">Dynamics AX</span><span class="sxs-lookup"><span data-stu-id="60412-332">Dynamics AX</span></span>

<span data-ttu-id="60412-333">不要になったので、このコードを削除してください。</span><span class="sxs-lookup"><span data-stu-id="60412-333">Delete this code, because it's no longer required.</span></span> <span data-ttu-id="60412-334">コントロールこれを自動的に処理します。</span><span class="sxs-lookup"><span data-stu-id="60412-334">The control handles this automatically.</span></span>

### <a name="step-19"></a><span data-ttu-id="60412-335">ステップ 19</span><span class="sxs-lookup"><span data-stu-id="60412-335">Step 19</span></span>

#### <a name="ax-2012"></a><span data-ttu-id="60412-336">AX 2012</span><span class="sxs-lookup"><span data-stu-id="60412-336">AX 2012</span></span>

<span data-ttu-id="60412-337">フォームは、**parm** メソッドを通じてコントローラーのプロパティを設定します。</span><span class="sxs-lookup"><span data-stu-id="60412-337">The form sets properties on the controller through **parm** methods.</span></span>

#### <a name="dynamics-ax"></a><span data-ttu-id="60412-338">Dynamics AX</span><span class="sxs-lookup"><span data-stu-id="60412-338">Dynamics AX</span></span>

<span data-ttu-id="60412-339">一般に、コントローラー クラスに以前設定されていたプロパティをコントロールに直接設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="60412-339">In general, any property that was previously set on the controller class should now be set directly on the control.</span></span> <span data-ttu-id="60412-340">このプロパティを設定する必要があるコントロールは、**parmControl()** 呼び出しを見て派生したマッピングの詳細から判断できます。</span><span class="sxs-lookup"><span data-stu-id="60412-340">The control that the property must be set on can be determined from the mapping details that are derived by looking at the **parmControl()** call.</span></span> <span data-ttu-id="60412-341">また、**セグメント化エントリ** コントロールの場合、Microsoft Visual Studio の**プロパティ** ダイアログ ボックスで使用できるプロパティは、コントロール インスタンスで対応する **parm** メソッドを使用して、コードで設定することもできます。</span><span class="sxs-lookup"><span data-stu-id="60412-341">Additionally, for the **Segmented Entry** control, any property that is available in the **Properties** dialog box in Microsoft Visual Studio can also be set in code, through the corresponding **parm** method on the control instance.</span></span>

### <a name="step-20"></a><span data-ttu-id="60412-342">ステップ 20</span><span class="sxs-lookup"><span data-stu-id="60412-342">Step 20</span></span>

#### <a name="ax-2012"></a><span data-ttu-id="60412-343">AX 2012</span><span class="sxs-lookup"><span data-stu-id="60412-343">AX 2012</span></span>

<span data-ttu-id="60412-344">フォームは、コントロールの **currentSegmentIndex()** メソッドを使用します。</span><span class="sxs-lookup"><span data-stu-id="60412-344">The form uses the control's **currentSegmentIndex()** method.</span></span>

```xpp
dimOffetAssetController. getDimensionAttributeByControlIndex(currentSegmentIndex);
```

#### <a name="dynamics-ax"></a><span data-ttu-id="60412-345">Dynamics AX</span><span class="sxs-lookup"><span data-stu-id="60412-345">Dynamics AX</span></span>

<span data-ttu-id="60412-346">一般に、コントローラー クラスに以前設定されていたプロパティをコントロールに直接設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="60412-346">In general, any property that was previously set on the controller class should now be set directly on the control.</span></span> <span data-ttu-id="60412-347">このプロパティを設定する必要があるコントロールは、**parmControl()** 呼び出しを見て派生したマッピングの詳細から判断できます。</span><span class="sxs-lookup"><span data-stu-id="60412-347">The control that the property must be set on can be determined from the mapping details that are derived by looking at the **parmControl()** call.</span></span> <span data-ttu-id="60412-348">また、**セグメント化エントリ** コントロールの場合、Visual Studio の**プロパティ** ダイアログ ボックスで使用できるプロパティは、コントロール インスタンスで対応する **parm** メソッドを使用して、コードで設定することもできます。</span><span class="sxs-lookup"><span data-stu-id="60412-348">Additionally, for the **Segmented Entry** control, any property that is available in the **Properties** dialog box in Visual Studio can also be set in code, through the corresponding **parm** method on the control instance.</span></span>

### <a name="step-21"></a><span data-ttu-id="60412-349">ステップ 21</span><span class="sxs-lookup"><span data-stu-id="60412-349">Step 21</span></span>

#### <a name="ax-2012"></a><span data-ttu-id="60412-350">AX 2012</span><span class="sxs-lookup"><span data-stu-id="60412-350">AX 2012</span></span>

<span data-ttu-id="60412-351">このフォームは、コントローラー オブジェクトのメソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="60412-351">The form calls methods on the controller object.</span></span> <span data-ttu-id="60412-352">次に例を示します。</span><span class="sxs-lookup"><span data-stu-id="60412-352">Here's an example.</span></span>

```xpp
dimOffetAssetController. getDimensionAttributeByControlIndex(currentSegmentIndex);
```

#### <a name="dynamics-ax"></a><span data-ttu-id="60412-353">Dynamics AX</span><span class="sxs-lookup"><span data-stu-id="60412-353">Dynamics AX</span></span>

<span data-ttu-id="60412-354">コントローラー上のすべてのメソッド呼び出しはコントロール上のメソッド呼び出しに置き換える必要があります。</span><span class="sxs-lookup"><span data-stu-id="60412-354">All method calls on the controller must be replaced with method calls on the control.</span></span> <span data-ttu-id="60412-355">この例では、代わりにコントロールで **getDimensionAttributeByControlIndex()** メソッドを使用します。</span><span class="sxs-lookup"><span data-stu-id="60412-355">For this example, use the **getDimensionAttributeByControlIndex()** method on the control instead.</span></span>

```xpp
segmentedEntryControl. getDimensionAttributeByControlIndex();
```

### <a name="step-22"></a><span data-ttu-id="60412-356">ステップ 22</span><span class="sxs-lookup"><span data-stu-id="60412-356">Step 22</span></span>

#### <a name="ax-2012"></a><span data-ttu-id="60412-357">AX 2012</span><span class="sxs-lookup"><span data-stu-id="60412-357">AX 2012</span></span>

<span data-ttu-id="60412-358">**DimensionDynamicAccountController** で、勘定タイプはコンストラクターを通して指定されます。</span><span class="sxs-lookup"><span data-stu-id="60412-358">For **DimensionDynamicAccountController**, the account type is specified through the constructor.</span></span>

```xpp
DimensionDynamicAccountController::construct(ledgerJournalTrans_ds, fieldStr(LedgerJournalTrans, LedgerDimension), fieldStr(LedgerJournalTrans, AccountType));
```

#### <a name="dynamics-ax"></a><span data-ttu-id="60412-359">Dynamics AX</span><span class="sxs-lookup"><span data-stu-id="60412-359">Dynamics AX</span></span>

<span data-ttu-id="60412-360">この機能を実装するには、2 つのメソッドがあります。</span><span class="sxs-lookup"><span data-stu-id="60412-360">There are two methods for implementing this functionality.</span></span> <span data-ttu-id="60412-361">これらのメソッドは相互に排他的なため、状況に応じてそれらのメソッドのうち 1 つのみを使用してください。</span><span class="sxs-lookup"><span data-stu-id="60412-361">These methods are mutually exclusive, so use only one of them, depending on the situation:</span></span>

-   <span data-ttu-id="60412-362">**セグメント化されたエントリー**コントロールについては、**プロパティ**ダイアログ ボックスで、**勘定タイプ フィールド**プロパティを勘定タイプを提供するデータ ソース フィールドに設定します。</span><span class="sxs-lookup"><span data-stu-id="60412-362">For the **Segmented Entry** control, in the **Properties** dialog box, set the **Account Type Field** property to the data source field that will provide the account type.</span></span> <span data-ttu-id="60412-363">これが推奨されるメソッドです。</span><span class="sxs-lookup"><span data-stu-id="60412-363">This is the preferred method.</span></span> 

    > [!NOTE]
    > <span data-ttu-id="60412-364">**super()** 呼び出しが、**口座タイプ フィールド** プロパティにバインドされているフィールドの **modified()** メソッドから削除されている場合、このメソッドは機能しません。</span><span class="sxs-lookup"><span data-stu-id="60412-364">If the **super()** call has been removed from the **modified()** method for the field that is bound to the **Account Type Field** property, this method won't work.</span></span> <span data-ttu-id="60412-365">**LedgerJournalTransDaily** などのいくつかの仕訳帳フォームで、この問題が確認されました。</span><span class="sxs-lookup"><span data-stu-id="60412-365">We have seen this issue in some journal forms, such as **LedgerJournalTransDaily**.</span></span> <span data-ttu-id="60412-366">このような場合、**super()** コールバックを **modified()** メソッドに追加するか、2 つ目のメソッドを使用します。</span><span class="sxs-lookup"><span data-stu-id="60412-366">In such cases, either add the **super()** call back to the **modified()** method, or use the second method.</span></span>
-   <span data-ttu-id="60412-367">コントロールで **parmAccountTypeEnumValue()** メソッドを呼び出すことにより、勘定タイプを手動で設定します。</span><span class="sxs-lookup"><span data-stu-id="60412-367">Set the account type manually by calling the **parmAccountTypeEnumValue()** method on the control.</span></span> <span data-ttu-id="60412-368">次に例を示します。</span><span class="sxs-lookup"><span data-stu-id="60412-368">Here's an example.</span></span>

    ```xpp
    LedgerJournalTrans_AccountNum.parmAccountTypeEnumValue(enum2int(ledgerJournalTrans.AccountType));
    ```

    > [!NOTE] 
    > <span data-ttu-id="60412-369">**parmAccountTypeEnumValue()** への呼び出しは、勘定タイプを提供するフィールドの、データソースの **active()** メソッド、および **modified()** メソッドの両方に入力する必要があります。</span><span class="sxs-lookup"><span data-stu-id="60412-369">The call to **parmAccountTypeEnumValue()** must be put in both the data source's **active()** method and the **modified()** method of the field that will provide the account type.</span></span>

### <a name="step-23"></a><span data-ttu-id="60412-370">ステップ 23</span><span class="sxs-lookup"><span data-stu-id="60412-370">Step 23</span></span>

#### <a name="ax-2012"></a><span data-ttu-id="60412-371">AX 2012</span><span class="sxs-lookup"><span data-stu-id="60412-371">AX 2012</span></span>

<span data-ttu-id="60412-372">フォームには定義されている変数があります。</span><span class="sxs-lookup"><span data-stu-id="60412-372">The form has a variable that is defined.</span></span>

```xpp
LedgerDimensionDefaultAccountController ledgerDimensionDefaultAccountController;
```

#### <a name="dynamics-ax"></a><span data-ttu-id="60412-373">Dynamics AX</span><span class="sxs-lookup"><span data-stu-id="60412-373">Dynamics AX</span></span>

<span data-ttu-id="60412-374">コントローラーが必要なくなったため、これを削除します。</span><span class="sxs-lookup"><span data-stu-id="60412-374">Remove this, because the controller is no longer required.</span></span>

### <a name="step-24"></a><span data-ttu-id="60412-375">ステップ 24</span><span class="sxs-lookup"><span data-stu-id="60412-375">Step 24</span></span>

#### <a name="ax-2012"></a><span data-ttu-id="60412-376">AX 2012</span><span class="sxs-lookup"><span data-stu-id="60412-376">AX 2012</span></span>

<span data-ttu-id="60412-377">**parmCurrentLedgerCOA()** メソッド呼び出し:(これらは通常、フォームの **init()** メソッドまたはコントロールで上書きされたメソッドのうちの 1 つに存在します。)</span><span class="sxs-lookup"><span data-stu-id="60412-377">**parmCurrentLedgerCOA()** method calls: (These are typically present in the form's **init()** method or one of the methods that are overridden on the control.)</span></span>

```xpp
ledgerDimensionDefaultAccountController.parmCurrentLedgerCOA(LedgerCOA::current());
```

#### <a name="dynamics-ax"></a><span data-ttu-id="60412-378">Dynamics AX</span><span class="sxs-lookup"><span data-stu-id="60412-378">Dynamics AX</span></span>

<span data-ttu-id="60412-379">ほとんどの場合に必要がなくなったため、このコード行を削除します。</span><span class="sxs-lookup"><span data-stu-id="60412-379">Remove this line of code, because it's no longer required in most cases.</span></span> <span data-ttu-id="60412-380">この線を削除する前に、**LedgerCOA** 値がその情報から派生するため、データ領域 ID がパラメーターとしてコントローラーに正しく渡されていることを確認してください。</span><span class="sxs-lookup"><span data-stu-id="60412-380">Before you delete this line, make sure that the data area ID is correctly passed in to the controller as a parameter, because the **LedgerCOA** value will be derived from that information.</span></span> <span data-ttu-id="60412-381">データ領域 ID が渡されない場合は、**parmCurrentLedgerCOA()** を **parmDataAreaId()** で交換し、通常は **curext()** または会社のアカウント管理のために範囲を制御する別のテーブル フィールドである適切な **SelectableDataArea** 値を渡します。</span><span class="sxs-lookup"><span data-stu-id="60412-381">If the data area ID is not passed in, replace **parmCurrentLedgerCOA()** with **parmDataAreaId()**, and pass the appropriate **SelectableDataArea** value, which is usually **curext()** or another table field that controls the scope of the company for the account control.</span></span> <span data-ttu-id="60412-382">フォームにデータ領域のコンテキストはありませんが、現在の **LedgerCOA** 値のみがある場合、既定のアカウント コント ローラーだけで動作する必要があります。</span><span class="sxs-lookup"><span data-stu-id="60412-382">If the form has no data area context but only a current **LedgerCOA** value, it should be working only with the default account controller.</span></span> <span data-ttu-id="60412-383">企業には無関係ですが、特定の勘定科目表 (COA) (**MainAccount** および **Allocations** など) にスコープされているフォームがいくつかあります。</span><span class="sxs-lookup"><span data-stu-id="60412-383">There are only a few forms that are agnostic of a company, but that are scoped to a specific chart of accounts (COA) (for example, **MainAccount** and **Allocations**).</span></span> <span data-ttu-id="60412-384">そのような場合、**parmCurrentLedgerCOA** が、既定のアカウント コントローラー タイプ セットを持つ**セグメント化エントリ** コントロール インスタンスで呼び出される必要があります。</span><span class="sxs-lookup"><span data-stu-id="60412-384">In these cases, **parmCurrentLedgerCOA** should be called on the **Segmented Entry** control instance that has a default account controller type set.</span></span>

### <a name="step-25"></a><span data-ttu-id="60412-385">ステップ 25</span><span class="sxs-lookup"><span data-stu-id="60412-385">Step 25</span></span>

#### <a name="ax-2012"></a><span data-ttu-id="60412-386">AX 2012</span><span class="sxs-lookup"><span data-stu-id="60412-386">AX 2012</span></span>

<span data-ttu-id="60412-387">**parmIncludeFinancialAccounts(NoYes)** メソッド呼び出し:</span><span class="sxs-lookup"><span data-stu-id="60412-387">**parmIncludeFinancialAccounts(NoYes)** method calls:</span></span>

```xpp
LedgerDimensionDefaultAccountController.parmIncludeFinancialAccounts(NoYes::Yes);
```

#### <a name="dynamics-ax"></a><span data-ttu-id="60412-388">Dynamics AX</span><span class="sxs-lookup"><span data-stu-id="60412-388">Dynamics AX</span></span>

<span data-ttu-id="60412-389">このコード行は不要になり、**セグメント化されたエントリ**コントロールのプロパティを使用して直接設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="60412-389">This line of code is no longer required and should be set directly via a property on the **Segmented Entry** control.</span></span> 

> [!NOTE]
> <span data-ttu-id="60412-390">フレームワークのバグのため、これを明示的に設定しないと、以前の動作では、構築中に暗黙的に **はい** が割り当てられていましたが、勘定分析コードの既定のアカウント コントローラーに **いいえ** が割り当てられます。</span><span class="sxs-lookup"><span data-stu-id="60412-390">Because of a framework bug, if you don't set this explicitly, **No** will be assigned on a ledger dimension default account controller, whereas the previous behavior was to implicitly assign **Yes** during construction.</span></span> <span data-ttu-id="60412-391">この操作は、プロパティとして手動で設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="60412-391">You must set this manually as a property.</span></span> <span data-ttu-id="60412-392">または、**ダイアログ**クラスへの、**parm** メソッドがまだ明示的に呼び出されるはずです。</span><span class="sxs-lookup"><span data-stu-id="60412-392">Alternatively, for a **dialog** class, the **parm** method should still be explicitly called.</span></span>

### <a name="step-26"></a><span data-ttu-id="60412-393">ステップ 26</span><span class="sxs-lookup"><span data-stu-id="60412-393">Step 26</span></span>

#### <a name="ax-2012"></a><span data-ttu-id="60412-394">AX 2012</span><span class="sxs-lookup"><span data-stu-id="60412-394">AX 2012</span></span>

<span data-ttu-id="60412-395">**セグメント化エントリ** コントロールのアカウントタイプを提供するデータフィールドの **変更済み** メソッドのコードは、コントロールが動的アカウントコントロールとして使用されている場合、このようになります。</span><span class="sxs-lookup"><span data-stu-id="60412-395">The code for the **modified** method of the data field that provides the account type for the **Segmented Entry** control might look like this when the control is used as a dynamic account control.</span></span>

```xpp
public void modified()
{
    super();

    // Lock the main account segment if "Fixed offset account" is selected in Journal Names
    if (ledgerJournalTable.OffsetAccountType == LedgerJournalACType::Ledger)
    {
        controller.parmLockMainAccountSegment(ledgerJournalTable.FixedOffsetAccount);
    }
}
```

#### <a name="dynamics-ax"></a><span data-ttu-id="60412-396">Dynamics AX</span><span class="sxs-lookup"><span data-stu-id="60412-396">Dynamics AX</span></span>

<span data-ttu-id="60412-397">このデータ フィールドの **modified** メソッドは、**参照** フィールドとして **セグメント化されたエントリ** コントロールにバインドされた勘定分析コード フィールドをクリアしなければならなくなりました。</span><span class="sxs-lookup"><span data-stu-id="60412-397">The **modified** method of this data field must now clear the ledger dimension field that is bound to the **Segmented Entry** control as a **Reference** field.</span></span> <span data-ttu-id="60412-398">たとえば、**セグメント化されたエントリ**コントロールの名前が **OffsetAccount** である場合、このコントロールの**参照**フィールド プロパティが **LedgerDimension** に設定され、上記のコード内の**変更**メソッドが次のように変更される必要があります。</span><span class="sxs-lookup"><span data-stu-id="60412-398">For example, if the name of the **Segmented Entry** control is **OffsetAccount**, and the **Reference** field property for this control is set to **LedgerDimension**, the **modified** method in the preceding code should be changed as follows.</span></span>

```xpp
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
```

<span data-ttu-id="60412-399">追加の明細行は、勘定タイプが変更されたときにコントロールをクリアするために必要です。</span><span class="sxs-lookup"><span data-stu-id="60412-399">The additional line is required to clear the control when the account type is changed.</span></span>

### <a name="step-27"></a><span data-ttu-id="60412-400">ステップ 27</span><span class="sxs-lookup"><span data-stu-id="60412-400">Step 27</span></span>

#### <a name="ax-2012"></a><span data-ttu-id="60412-401">AX 2012</span><span class="sxs-lookup"><span data-stu-id="60412-401">AX 2012</span></span>

<span data-ttu-id="60412-402">コントローラーで **parmAccountStructure()** メソッドを呼び出すことができます。</span><span class="sxs-lookup"><span data-stu-id="60412-402">You can call the **parmAccountStructure()** method on the controller.</span></span>

```xpp
fromBudgetPlanningLedgerDimensionController.parmAccountStructureId(accountStructureIdLocal);
```

#### <a name="dynamics-ax"></a><span data-ttu-id="60412-403">Dynamics AX</span><span class="sxs-lookup"><span data-stu-id="60412-403">Dynamics AX</span></span>

<span data-ttu-id="60412-404">このメソッドは 2 つの異なるメソッドで置き換えられます。</span><span class="sxs-lookup"><span data-stu-id="60412-404">This method is replaced by two different methods.</span></span> <span data-ttu-id="60412-405">また、新しいメソッドの目的は、古いメソッドの逆です: 古いメソッドは検証を無効にしましたが、新しいメソッドはそれを有効にします。</span><span class="sxs-lookup"><span data-stu-id="60412-405">Additionally, the purpose of the new methods is the opposite of the old method: the old method turned validation off, whereas the new methods turn it on.</span></span> <span data-ttu-id="60412-406">したがって、コードを移行するときは、新しいメソッドの Boolean パラメーターを逆にする必要があります。</span><span class="sxs-lookup"><span data-stu-id="60412-406">Therefore, when you migrate code, you must reverse the Boolean parameter for the new methods.</span></span> <span data-ttu-id="60412-407">たとえば、上記のコードでメソッドの呼び出しについては、新しいメソッドはこのようになります。</span><span class="sxs-lookup"><span data-stu-id="60412-407">For example, for the method call in the preceding code, the new methods would look like this.</span></span>

```xpp
ToBudgetTransactionLine_LedgerDimension.parmDoValueActiveDatesValidation(false);

ToBudgetTransactionLine_LedgerDimension.parmDoValueSuspendedValidation(false);
```
### <a name="step-28"></a><span data-ttu-id="60412-408">ステップ 28</span><span class="sxs-lookup"><span data-stu-id="60412-408">Step 28</span></span>

#### <a name="ax-2012"></a><span data-ttu-id="60412-409">AX 2012</span><span class="sxs-lookup"><span data-stu-id="60412-409">AX 2012</span></span>

<span data-ttu-id="60412-410">以下のコントローラーで **parmAccountStructure()** メソッドを呼び出すことができます。</span><span class="sxs-lookup"><span data-stu-id="60412-410">You can call the **parmAccountStructure()** method on the controller:</span></span>

```xpp
fromBudgetPlanningLedgerDimensionController.parmAccountStructureId(accountStructureIdLocal);
```

#### <a name="dynamics-ax"></a><span data-ttu-id="60412-411">Dynamics AX</span><span class="sxs-lookup"><span data-stu-id="60412-411">Dynamics AX</span></span>

<span data-ttu-id="60412-412">**parmAccountStructureId()** メソッドは、コントロール上に存在しません。</span><span class="sxs-lookup"><span data-stu-id="60412-412">The **parmAccountStructureId()** method doesn't exist on the control.</span></span> <span data-ttu-id="60412-413">代わりに、個別の **getAccountStructure()** および **setAccountStructure()** メソッドがあります。</span><span class="sxs-lookup"><span data-stu-id="60412-413">Instead, separate **getAccountStructure()** and **setAccountStructure()** methods exist.</span></span> <span data-ttu-id="60412-414">したがって、**parmAccountStructureId()** 呼び出しは、**parm** メソッドがどのように使用されていたかに応じて、**get** メソッドまたは **set** メソッドで置き換えられる必要があります。</span><span class="sxs-lookup"><span data-stu-id="60412-414">Therefore, the **parmAccountStructureId()** call must be replaced by the **get** or **set** method, depending on how the **parm** method was used.</span></span> <span data-ttu-id="60412-415">たとえば、上記のコードで **parm** メソッドはセッターとして呼び出されたので、呼び出しは**設定**メソッドへの呼び出しによって置換される必要があります。</span><span class="sxs-lookup"><span data-stu-id="60412-415">For example, the **parm** method in the preceding code was called as a setter, so the call should be replaced by a call to the **set** method.</span></span>

```xpp
ToBudgetPlanningTransactionLine_LedgerDimension.setAccountStructureId(accountStructureIdLocal);
```

### <a name="step-29"></a><span data-ttu-id="60412-416">ステップ 29</span><span class="sxs-lookup"><span data-stu-id="60412-416">Step 29</span></span>

#### <a name="ax-2012"></a><span data-ttu-id="60412-417">AX 2012</span><span class="sxs-lookup"><span data-stu-id="60412-417">AX 2012</span></span>

```xpp
parmSkipSuspendedAndActiveDateValidation:
```

#### <a name="dynamics-ax"></a><span data-ttu-id="60412-418">Dynamics AX</span><span class="sxs-lookup"><span data-stu-id="60412-418">Dynamics AX</span></span>

<span data-ttu-id="60412-419">このメソッドは 2 つの異なるメソッドで置き換えられます。</span><span class="sxs-lookup"><span data-stu-id="60412-419">This method is replaced by two different methods.</span></span> <span data-ttu-id="60412-420">また、新しいメソッドの目的は、古いメソッドの逆です: 古いメソッドは検証を無効にしましたが、新しいメソッドはそれを有効にします。</span><span class="sxs-lookup"><span data-stu-id="60412-420">Additionally, the purpose of the new methods is opposite of the old method: the old method turned validation off, whereas the new methods turn it on.</span></span> <span data-ttu-id="60412-421">したがって、コードを移行するときは、新しいメソッドの Boolean パラメーターを逆にする必要があります。</span><span class="sxs-lookup"><span data-stu-id="60412-421">Therefore, when you migrate code, you must reverse the Boolean parameter for the new methods.</span></span> <span data-ttu-id="60412-422">たとえば、上記のコードでメソッドの呼び出しについては、新しいメソッドはこのようになります。</span><span class="sxs-lookup"><span data-stu-id="60412-422">For example, for the method call in the preceding code, the new methods would look like this.</span></span>

```xpp
ToBudgetTransactionLine_LedgerDimension.parmDoValueActiveDatesValidation(false);

ToBudgetTransactionLine_LedgerDimension.parmDoValueSuspendedValidation(false);
```

### <a name="step-30"></a><span data-ttu-id="60412-423">ステップ 30</span><span class="sxs-lookup"><span data-stu-id="60412-423">Step 30</span></span>

#### <a name="ax-2012"></a><span data-ttu-id="60412-424">AX 2012</span><span class="sxs-lookup"><span data-stu-id="60412-424">AX 2012</span></span>

<span data-ttu-id="60412-425">通常は **loadSegments()** メソッド内でコントローラーの **loadFromId** メソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="60412-425">Typically, call the **loadFromId** method on the controller in the **loadSegments()** method.</span></span>

```xpp
ledgerDimensionDefaultAccountControllerResourceIssueOffset.loadFromId(wrkCtrTable.ResourceIssueOffsetLedgerDimension);
```

#### <a name="dynamics-ax"></a><span data-ttu-id="60412-426">Dynamics AX</span><span class="sxs-lookup"><span data-stu-id="60412-426">Dynamics AX</span></span>

<span data-ttu-id="60412-427">このメソッドは推奨されておらず、使用しないでください。</span><span class="sxs-lookup"><span data-stu-id="60412-427">This method has been deprecated and must not be used.</span></span> <span data-ttu-id="60412-428">このメソッドに対するすべての呼び出しを削除する必要があります。</span><span class="sxs-lookup"><span data-stu-id="60412-428">You should delete all calls to this method.</span></span>

### <a name="migrating-a-segmented-entry-control-on-a-dialog"></a><span data-ttu-id="60412-429">ダイアログ上のセグメント化エントリ コントロールの移行</span><span class="sxs-lookup"><span data-stu-id="60412-429">Migrating a Segmented Entry control on a dialog</span></span>

<span data-ttu-id="60412-430">ダイアログ上の新しい**セグメント化されたエントリ** コントロールの取得パターンは Dynamics AX で変更されています。</span><span class="sxs-lookup"><span data-stu-id="60412-430">The uptake pattern for the new **Segmented Entry** control on a dialog has changed in Dynamics AX.</span></span> <span data-ttu-id="60412-431">コントローラー クラス API とのやり取りではなく、**SegmentedEntryControlBuild** クラスとやり取りしてダイアログと SEC をリンクする必要があります。</span><span class="sxs-lookup"><span data-stu-id="60412-431">Instead of interacting with the controller class API, you must now interact with the **SegmentedEntryControlBuild** class to link the SEC with the dialog.</span></span> <span data-ttu-id="60412-432">このセクションでは、異なるコントローラー タイプのダイアログで SEC を使用するためのコード パターンを示します。</span><span class="sxs-lookup"><span data-stu-id="60412-432">This section shows the code patterns for using SEC on a dialog with different controller types.</span></span> 

> [!NOTE] 
> <span data-ttu-id="60412-433">Dynamics  AX ではヘルプ テキストが不要になるため、ダイアログ フィールドにヘルプ テキストを設定する必要はありません。</span><span class="sxs-lookup"><span data-stu-id="60412-433">Help text is no longer required in Dynamics AX, so you don't have to set the Help text on dialog fields.</span></span>

-   <span data-ttu-id="60412-434">**動的アカウント:**</span><span class="sxs-lookup"><span data-stu-id="60412-434">**Dynamic account:**</span></span>
    -   <span data-ttu-id="60412-435">**以前:**</span><span class="sxs-lookup"><span data-stu-id="60412-435">**Before:**</span></span>

        ```xpp
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
        ```

    -   <span data-ttu-id="60412-436">**以後:**</span><span class="sxs-lookup"><span data-stu-id="60412-436">**After:**</span></span>

        ```xpp
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
        ```

-   <span data-ttu-id="60412-437">**勘定科目:**</span><span class="sxs-lookup"><span data-stu-id="60412-437">**Ledger account:**</span></span>
    -   <span data-ttu-id="60412-438">**以前:**</span><span class="sxs-lookup"><span data-stu-id="60412-438">**Before:**</span></span>

        ```xpp
        dialogFeeLedgerDimension = dialog.addFieldValue(extendedtypestr(LedgerDimensionAccount),feeLedgerDimension,"@SYS119703", "@SYS85534");
        ledgerDimensionAccountController = LedgerDimensionAccountController::constructForDialog(dialogFeeLedgerDimension);
        ```

    -   <span data-ttu-id="60412-439">**以後:**</span><span class="sxs-lookup"><span data-stu-id="60412-439">**After:**</span></span>

        ```xpp
        DialogField dialogLedgerAccount = SegmentedEntryControlBuild::addToDialog(dialog, classstr(LedgerDimensionAccountControl), extendedTypeStr(LedgerDimensionAccount), "@SYS119703", feeLedgerDimension);
        ```

-   <span data-ttu-id="60412-440">**既定の勘定:**</span><span class="sxs-lookup"><span data-stu-id="60412-440">**Default account:**</span></span>
    -   <span data-ttu-id="60412-441">**以前:**</span><span class="sxs-lookup"><span data-stu-id="60412-441">**Before:**</span></span>

        ```xpp
        dialogInterCompanyLedgerDimension = dialog.addFieldValue(extendedTypeStr(LedgerDimensionDefaultAccount),interCompanyLedgerDimension, "@SYS21687", "@SYS85534");
        ledgerDimensionDefaultAccountController = LedgerDimensionDefaultAccountController::constructForDialog(dialogInterCompanyLedgerDimension);
        ```

    -   <span data-ttu-id="60412-442">**以後:**</span><span class="sxs-lookup"><span data-stu-id="60412-442">**After:**</span></span>

        ```xpp
        DialogField dialogDefaultAccount = SegmentedEntryControlBuild::addToDialog(dialog, classstr(LedgerDimensionDefaultAccountControl), extendedTypeStr(LedgerDimensionDefaultAccount), "@SYS21687", interCompanyLedgerDimension);
        ```

-   <span data-ttu-id="60412-443">**予算:**</span><span class="sxs-lookup"><span data-stu-id="60412-443">**Budget:**</span></span>
    -   <span data-ttu-id="60412-444">**以前:** 既存のプログラム ソース コード内でダイアログ シナリオの**予算計画**コントローラー (**BudgetLedgerDimensionController**) の取り込みは見つかりませんでした。</span><span class="sxs-lookup"><span data-stu-id="60412-444">**Before:** No uptake of the **Budget** controller (**BudgetLedgerDimensionController**) for a dialog scenario was found in the existing program source code.</span></span>
    -   <span data-ttu-id="60412-445">**以後:**</span><span class="sxs-lookup"><span data-stu-id="60412-445">**After:**</span></span>

        ```xpp
        DialogField dialogBudget = SegmentedEntryControlBuild::addToDialog(dialog, classstr(BudgetLedgerDimensionControl), extendedTypeStr(LedgerDimensionBudget), 'Budget', ledgerDimensionBudget);
        ```

    <span data-ttu-id="60412-446">**メモ :**</span><span class="sxs-lookup"><span data-stu-id="60412-446">**Notes:**</span></span>
    -   <span data-ttu-id="60412-447">新しい API を使用すると、ダイアログ フィールドを設定しているときに、ラベル (前述の例では **予算**) を指定できます。</span><span class="sxs-lookup"><span data-stu-id="60412-447">The new API lets you specify the label (**Budget** in the preceding example) while you set up the dialog field.</span></span>
    -   <span data-ttu-id="60412-448">コントロールのデフォルト値は、**ledgerDimensionBudget** 変数で指定します。</span><span class="sxs-lookup"><span data-stu-id="60412-448">The default value for the control is specified via the **ledgerDimensionBudget** variable.</span></span>
    -   <span data-ttu-id="60412-449">**予算** コントローラーを用いて、使用する勘定構造を指定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="60412-449">You must specify the account structure that should be used with the **Budget** controller.</span></span> <span data-ttu-id="60412-450">**Dialog** クラスは、ユーザーが勘定構造を選択し (SEC の外部で)、選択した勘定構造を SEC で設定する方法を実装する必要があります。</span><span class="sxs-lookup"><span data-stu-id="60412-450">The **Dialog** class must implement a way for the user to select the account structure (outside of the SEC) and set the selected account structure on the SEC.</span></span>
-   <span data-ttu-id="60412-451">**予算計画:**</span><span class="sxs-lookup"><span data-stu-id="60412-451">**Budget planning:**</span></span>
    -   <span data-ttu-id="60412-452">**以前:** 既存のプログラム ソース コード内でダイアログ シナリオの**予算計画**コントローラー (**BudgetPlanningLedgerDimensionController**) の取り込みは見つかりませんでした。</span><span class="sxs-lookup"><span data-stu-id="60412-452">**Before:** No uptake of the **Budget planning** controller (**BudgetPlanningLedgerDimensionController**) for a dialog scenario was found in the existing program source code.</span></span>
    -   <span data-ttu-id="60412-453">**以後:**</span><span class="sxs-lookup"><span data-stu-id="60412-453">**After:**</span></span>

        ```xpp
        DialogField dialogBudgetPlanning = SegmentedEntryControlBuild::addToDialog(dialog, classstr(BudgetPlanningLedgerDimensionControl), extendedTypeStr(LedgerDimensionBudgetPlanning), 'Budget planning', ledgerDimensionBudgetPlanning);
        ```
        
    <span data-ttu-id="60412-454">**メモ :**</span><span class="sxs-lookup"><span data-stu-id="60412-454">**Notes:**</span></span>
    -   <span data-ttu-id="60412-455">新しい API を使用すると、ダイアログ フィールドを設定しているときに、ラベル (前述の例では **予算計画**) を指定できます。</span><span class="sxs-lookup"><span data-stu-id="60412-455">The new API lets you specify the label (**Budget planning** in the preceding example) while you set up the dialog field.</span></span>
    -   <span data-ttu-id="60412-456">コントロールのデフォルト値は、**ledgerDimensionBudgetPlanning** 変数で指定します。</span><span class="sxs-lookup"><span data-stu-id="60412-456">The default value for the control is specified via the **ledgerDimensionBudgetPlanning** variable.</span></span>
    -   <span data-ttu-id="60412-457">**予算計画** コントローラーを用いて、使用する勘定構造を指定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="60412-457">You must specify the account structure that should be used with the **Budget planning** controller.</span></span> <span data-ttu-id="60412-458">**Dialog** クラスは、ユーザーが勘定構造を選択し (SEC の外部で)、選択した勘定構造を SEC で設定する方法を実装する必要があります。</span><span class="sxs-lookup"><span data-stu-id="60412-458">The **Dialog** class must implement a way for the user to select the account structure (outside of the SEC) and set the selected account structure on the SEC.</span></span>


<a name="additional-resources"></a><span data-ttu-id="60412-459">追加リソース</span><span class="sxs-lookup"><span data-stu-id="60412-459">Additional resources</span></span>
--------

[<span data-ttu-id="60412-460">ダイアログのセグメント化されたエントリ コントロールのサポート</span><span class="sxs-lookup"><span data-stu-id="60412-460">Support for Segmented Entry controls on dialogs</span></span>](segmented-entry-control-dialog-support.md)

[<span data-ttu-id="60412-461">セグメント化されたエントリ コントロールのデザイン時メタデータ</span><span class="sxs-lookup"><span data-stu-id="60412-461">Design-time metadata for Segmented Entry controls</span></span>](segmented-entry-control-metadata-specification.md)

[<span data-ttu-id="60412-462">セグメント化されたエントリ コントロールの Parm メソッド</span><span class="sxs-lookup"><span data-stu-id="60412-462">Parm methods for Segmented Entry controls</span></span>](segmented-entry-control-parm-method-specification.md)

[<span data-ttu-id="60412-463">セグメント化されたエントリ コントロールの移行</span><span class="sxs-lookup"><span data-stu-id="60412-463">Migrate Segmented Entry controls</span></span>](segmented-entry-control-conversion.md)




