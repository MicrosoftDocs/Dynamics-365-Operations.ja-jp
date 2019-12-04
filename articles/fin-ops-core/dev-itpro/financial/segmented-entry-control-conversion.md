---
title: セグメント化されたエントリ コントロールの移行
description: このチュートリアルでは、簡単なシナリオ (SMAServiceOrderTable フォームの場合) と複雑なシナリオ (LedgerJournalTransDaily フォームの場合) の 2 つのセグメント化エントリ管理の移行シナリオについて説明します。
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
ms.custom: 25611
ms.assetid: 82e953d0-878e-4a3f-a91b-7375017a2810
ms.search.region: Global
ms.author: ghenriks
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 6d8b9beca9ff32fb3238775df8af1da8a50c7573
ms.sourcegitcommit: 57bc7e17682e2edb5e1766496b7a22f4621819dd
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/18/2019
ms.locfileid: "2811715"
---
# <a name="migrate-segmented-entry-controls"></a><span data-ttu-id="2649a-103">セグメント化されたエントリ コントロールの移行</span><span class="sxs-lookup"><span data-stu-id="2649a-103">Migrate Segmented Entry controls</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="2649a-104">このチュートリアルでは、簡単なシナリオ (SMAServiceOrderTable フォームの場合) と複雑なシナリオ (LedgerJournalTransDaily フォームの場合) の 2 つのセグメント化エントリ管理の移行シナリオについて説明します。</span><span class="sxs-lookup"><span data-stu-id="2649a-104">This tutorial walks you through two migration scenarios for the Segmented Entry control -  a simple scenario (for the SMAServiceOrderTable form) and a complex scenario (for the LedgerJournalTransDaily form).</span></span>

<a name="simple-migration-scenario--smaserviceordertable-form"></a><span data-ttu-id="2649a-105">簡易移行シナリオ - SMAServiceOrderTable フォーム</span><span class="sxs-lookup"><span data-stu-id="2649a-105">Simple migration scenario – SMAServiceOrderTable form</span></span>
-----------------------------------------------------

1.  <span data-ttu-id="2649a-106">アプリケーション エクスプローラーで **SMAServiceOrderTable** フォームを検索します。</span><span class="sxs-lookup"><span data-stu-id="2649a-106">Search for the **SMAServiceOrderTable** form in Application Explorer.</span></span>
2.  <span data-ttu-id="2649a-107">現在のプロジェクトにフォームを追加します。</span><span class="sxs-lookup"><span data-stu-id="2649a-107">Add the form to the current project.</span></span>
3.  <span data-ttu-id="2649a-108">フォーム デザイン ビューとコード エディタ ビューで、フォームを開きます。</span><span class="sxs-lookup"><span data-stu-id="2649a-108">Open the form in the form design view and the code editor view.</span></span>
4.  <span data-ttu-id="2649a-109">フォーム デザイン ビューで、手動でコントロール ツリーを移動するか、**ファイル** タブの下にある検索バーで「SegmentedEntry」を検索して、セグメント化されたエントリ コントロール (SEC) を見つけます。</span><span class="sxs-lookup"><span data-stu-id="2649a-109">In the form design view, find the Segmented Entry control (SEC), either by manually walking the control tree or by searching for “SegmentedEntry” in the search bar below the **File** tab.</span></span>
5.  <span data-ttu-id="2649a-110">SEC を選択し、次の情報を確認します。</span><span class="sxs-lookup"><span data-stu-id="2649a-110">Select the SEC, and verify the following information:</span></span>
    -   <span data-ttu-id="2649a-111">コントロールの横にある括弧で指定されたコントロールのタイプは、**SegmentedEntryControl** です。</span><span class="sxs-lookup"><span data-stu-id="2649a-111">The type for the control, as specified in parenthesis next to the control, is **SegmentedEntryControl**.</span></span>
    -   <span data-ttu-id="2649a-112">**コントローラー クラス** プロパティは **DimensionDynamicAccountController** に設定されます。</span><span class="sxs-lookup"><span data-stu-id="2649a-112">The **Controller class** property is set to **DimensionDynamicAccountController**.</span></span> <span data-ttu-id="2649a-113">このプロパティは、SEC のこのインスタンスが使用するコントローラーのタイプを示します。</span><span class="sxs-lookup"><span data-stu-id="2649a-113">This property indicates the type of controller that this instance of the SEC will use.</span></span> <span data-ttu-id="2649a-114">コントローラーのタイプによって、コントロールのビヘイビアーが決まります。</span><span class="sxs-lookup"><span data-stu-id="2649a-114">The type of controller, in turn, determines the behavior of the control.</span></span>

6.  <span data-ttu-id="2649a-115">コード エディタ ビューに切り替え、フォーム ソース コードで "TODO: (コード アップグレード) \[セグメント化されたエントリ コントロール\]" のすべての事例を検索します。</span><span class="sxs-lookup"><span data-stu-id="2649a-115">Switch to the code editor view, and search for all occurrences of “TODO: (Code Upgrade) \[Segmented entry control\]” in the form source code.</span></span>
7.  <span data-ttu-id="2649a-116">検索結果で最初の結果を無視すると、コントローラー変数申告を示します。</span><span class="sxs-lookup"><span data-stu-id="2649a-116">In the search results, ignore the first result, which points to the controller variable declaration.</span></span> <span data-ttu-id="2649a-117">制御変数への参照をすべて削除したら、最後に、この作業項目を修正する必要があります。</span><span class="sxs-lookup"><span data-stu-id="2649a-117">You must fix this TODO last, after you've removed all references to the controller variable.</span></span>
8.  <span data-ttu-id="2649a-118">次のサブセクションでの説明にあるように、残りの各 TODO コメントが実行されます。</span><span class="sxs-lookup"><span data-stu-id="2649a-118">Go through each of the remaining TODO comments, as described in the following subsections.</span></span>

### <a name="ledgerdimension-data-field"></a><span data-ttu-id="2649a-119">LedgerDimension データ フィールド</span><span class="sxs-lookup"><span data-stu-id="2649a-119">LedgerDimension data field</span></span>

<span data-ttu-id="2649a-120">(**フォーム**&gt;**データ ソース** &gt;**SMAServiceOrderLine**&gt; **フィールド** &gt;**LedgerDimension**&gt; **方法**)</span><span class="sxs-lookup"><span data-stu-id="2649a-120">(**Form** &gt; **Data sources** &gt; **SMAServiceOrderLine** &gt; **Fields** &gt; **LedgerDimension** &gt; **Methods**)</span></span>

##### <a name="dynamics-ax-2012"></a><span data-ttu-id="2649a-121">Dynamics AX 2012</span><span class="sxs-lookup"><span data-stu-id="2649a-121">Dynamics AX 2012</span></span>

    /* TODO: (Code Upgrade) [Segmented entry control] This method can be removed if there is no custom implementation */
    public void jumpRef()
    {
        ExpenseCost_LedgerDimension.jumpRef();
    }

##### <a name="dynamics-ax-for-operations"></a><span data-ttu-id="2649a-122">Dynamics AX for Operations</span><span class="sxs-lookup"><span data-stu-id="2649a-122">Dynamics AX for Operations</span></span>

<span data-ttu-id="2649a-123">このメソッドはコントロールの **jumpRef()** メソッドのみを呼び出し追加の処理は実行しないため、削除できます。</span><span class="sxs-lookup"><span data-stu-id="2649a-123">Because this method only calls the **jumpRef()** method on the control and doesn't perform any additional processing, you can delete it.</span></span>

### <a name="expensecost_ledgerdimension-control"></a><span data-ttu-id="2649a-124">ExpenseCost\_LedgerDimension コントロール</span><span class="sxs-lookup"><span data-stu-id="2649a-124">ExpenseCost\_LedgerDimension control</span></span>

<span data-ttu-id="2649a-125">(**フォーム**タブの下にある検索バーで「ExpenseCost\_LedgerDimension」を検索してください。)</span><span class="sxs-lookup"><span data-stu-id="2649a-125">(Search for "ExpenseCost\_LedgerDimension" in the search bar below the **Form** tab.)</span></span>

#### <a name="step-1"></a><span data-ttu-id="2649a-126">ステップ１</span><span class="sxs-lookup"><span data-stu-id="2649a-126">Step 1</span></span>

##### <a name="dynamics-ax-2012"></a><span data-ttu-id="2649a-127">Dynamics AX 2012</span><span class="sxs-lookup"><span data-stu-id="2649a-127">Dynamics AX 2012</span></span>

    /* TODO: (Code Upgrade) [Segmented entry control] This method can be removed if there is no custom implementation */
    public void jumpRef()
    {
        ExpenseCost_LedgerDimension.jumpRef();
    }

##### <a name="dynamics-ax-for-operations"></a><span data-ttu-id="2649a-128">Dynamics AX for Operations</span><span class="sxs-lookup"><span data-stu-id="2649a-128">Dynamics AX for Operations</span></span>

<span data-ttu-id="2649a-129">このメソッドはコントロールの **jumpRef()** メソッドのみを呼び出し追加の処理は行わないため、削除できます。</span><span class="sxs-lookup"><span data-stu-id="2649a-129">Because this method only calls the **jumpRef()** method on the control and doesn't performing any additional processing, you can delete it.</span></span>

#### <a name="step-2"></a><span data-ttu-id="2649a-130">ステップ２</span><span class="sxs-lookup"><span data-stu-id="2649a-130">Step 2</span></span>

##### <a name="dynamics-ax-2012"></a><span data-ttu-id="2649a-131">Dynamics AX 2012</span><span class="sxs-lookup"><span data-stu-id="2649a-131">Dynamics AX 2012</span></span>

    /* TODO: (Code Upgrade) [Segmented entry control] For custom implementation, code in this method needs to be moved elsewhere based on the migration guidance */
    public void loadSegments()
    {
        super();
        /* TODO: (Code Upgrade) [Segmented entry control] Replace this based on the migration guidance */
        // dimDynamicAccountController.loadSegments();
    }

##### <a name="dynamics-ax-for-operations"></a><span data-ttu-id="2649a-132">Dynamics AX for Operations</span><span class="sxs-lookup"><span data-stu-id="2649a-132">Dynamics AX for Operations</span></span>

<span data-ttu-id="2649a-133">このメソッドはコントロールの **loadSegments()** メソッドのみを呼び出し追加の処理は実行しないため、削除できます。</span><span class="sxs-lookup"><span data-stu-id="2649a-133">Because this method only calls the **loadSegments()** method on the control and doesn't perform any additional processing, you can delete it.</span></span>

#### <a name="step-3"></a><span data-ttu-id="2649a-134">ステップ 3</span><span class="sxs-lookup"><span data-stu-id="2649a-134">Step 3</span></span>

##### <a name="dynamics-ax-2012"></a><span data-ttu-id="2649a-135">Dynamics AX 2012</span><span class="sxs-lookup"><span data-stu-id="2649a-135">Dynamics AX 2012</span></span>

    /* TODO: (Code Upgrade) [Segmented entry control] Fix controller usage, if any, in this method based on the migration guidance */
    public void lookup()
    {
        switch (smaServiceOrderLine.OffsetAccountTypeExpense)
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
            case LedgerJournalACType::Project:
                ProjTable::lookupProjId(this, smaServiceOrderLine);
                break;
            case LedgerJournalACType::Vend:
                VendTable::lookupVendor(this);
                break;
            default:
                super();
                break;
            }
    }

##### <a name="dynamics-ax-for-operations"></a><span data-ttu-id="2649a-136">Dynamics AX for Operations</span><span class="sxs-lookup"><span data-stu-id="2649a-136">Dynamics AX for Operations</span></span>

<span data-ttu-id="2649a-137">このメソッドは、コントロールのカスタム ルックアップを実装します。</span><span class="sxs-lookup"><span data-stu-id="2649a-137">This method implements a custom lookup for the control.</span></span> <span data-ttu-id="2649a-138">したがって、メソッドをそのままにします。</span><span class="sxs-lookup"><span data-stu-id="2649a-138">Therefore, leave the method as it is.</span></span> <span data-ttu-id="2649a-139">"仕事" を削除します。</span><span class="sxs-lookup"><span data-stu-id="2649a-139">Just remove the TODO.</span></span> <span data-ttu-id="2649a-140">カスタムのルックアップをフック アップするには、SEC の **checkUseCustomLookup** メソッドをオーバーライドする必要があります。</span><span class="sxs-lookup"><span data-stu-id="2649a-140">To hook up custom lookups, you must override the SEC’s **checkUseCustomLookup** method.</span></span> <span data-ttu-id="2649a-141">次に例を示します。</span><span class="sxs-lookup"><span data-stu-id="2649a-141">Here is an example.</span></span>

    public boolean checkUseCustomLookup(int _accountTypeEnumValue, int _secondaryAccountTypeEnumValue)
    {
        boolean ret;
        switch(_accountTypeEnumValue)
        {
            case LedgerJournalACType::Bank:
            case LedgerJournalACType::Cust:
            case LedgerJournalACType::FixedAssets:
            case LedgerJournalACType::Project:
            case LedgerJournalACType::Vend:
                ret = true;
                break;
            default:
                ret = false;
        }
        return ret;
     }

<span data-ttu-id="2649a-142">また、カスタム ルックアップ フォームで **closeSelectRecord** メソッドが上書きされたことを確認してください。</span><span class="sxs-lookup"><span data-stu-id="2649a-142">Additionally, make sure that the **closeSelectRecord** method on the custom lookup form is overridden.</span></span> <span data-ttu-id="2649a-143">例については、**CustTableLookup** フォームを参照してください。</span><span class="sxs-lookup"><span data-stu-id="2649a-143">For an example, see the **CustTableLookup** form.</span></span>

#### <a name="step-4"></a><span data-ttu-id="2649a-144">ステップ 4</span><span class="sxs-lookup"><span data-stu-id="2649a-144">Step 4</span></span>

##### <a name="dynamics-ax-2012"></a><span data-ttu-id="2649a-145">Dynamics AX 2012</span><span class="sxs-lookup"><span data-stu-id="2649a-145">Dynamics AX 2012</span></span>

    /* TODO: (Code Upgrade) [Segmented entry control] For custom implementation, code in this method needs to be moved elsewhere based on the migration guidance */
    public void segmentValueChanged(SegmentValueChangedEventArgs _e)
    {
        super(_e);
        /* TODO: (Code Upgrade) [Segmented entry control] Replace this based on the migration guidance */
        // dimDynamicAccountController.segmentValueChanged(_e);
    }

##### <a name="dynamics-ax-for-operations"></a><span data-ttu-id="2649a-146">Dynamics AX for Operations</span><span class="sxs-lookup"><span data-stu-id="2649a-146">Dynamics AX for Operations</span></span>

<span data-ttu-id="2649a-147">このメソッドはコントロールの **segmentValueChanged()** メソッドのみを呼び出し追加の処理は実行しないため、削除できます。</span><span class="sxs-lookup"><span data-stu-id="2649a-147">Because this method only calls the **segmentValueChanged()** method on the control and doesn't perform any additional processing, you can delete it.</span></span>

#### <a name="step-5"></a><span data-ttu-id="2649a-148">ステップ 5</span><span class="sxs-lookup"><span data-stu-id="2649a-148">Step 5</span></span>

##### <a name="dynamics-ax-2012"></a><span data-ttu-id="2649a-149">Dynamics AX 2012</span><span class="sxs-lookup"><span data-stu-id="2649a-149">Dynamics AX 2012</span></span>

    /* TODO: (Code Upgrade) [Segmented entry control] This method can be removed if there is no custom implementation */
    public boolean validate()
    {
        boolean isValid;
        isValid = super();
        /* TODO: (Code Upgrade) [Segmented entry control] This statement can be removed if there is no custom logic */
        // isValid = dimDynamicAccountController.validate() && isValid;
        return isValid;
    }

##### <a name="dynamics-ax-for-operations"></a><span data-ttu-id="2649a-150">Dynamics AX for Operations</span><span class="sxs-lookup"><span data-stu-id="2649a-150">Dynamics AX for Operations</span></span>

<span data-ttu-id="2649a-151">このメソッドはコントロールの **validate()** メソッドのみを呼び出し追加の処理は実行しないため、削除できます。</span><span class="sxs-lookup"><span data-stu-id="2649a-151">Because this method only calls the **validate()** method on the control and doesn't perform any additional processing, you can delete it.</span></span>

### <a name="controller-variable-declarations"></a><span data-ttu-id="2649a-152">コントローラー変数申告</span><span class="sxs-lookup"><span data-stu-id="2649a-152">Controller variable declarations</span></span>

##### <a name="dynamics-ax-2012"></a><span data-ttu-id="2649a-153">Dynamics AX 2012</span><span class="sxs-lookup"><span data-stu-id="2649a-153">Dynamics AX 2012</span></span>

<span data-ttu-id="2649a-154">最後に、コントローラー変数申告のため、最初の TODO に戻ります。</span><span class="sxs-lookup"><span data-stu-id="2649a-154">Finally, go back to the first TODO, for the controller variable declaration.</span></span>

    /* TODO: (Code Upgrade) [Segmented entry control] Replace this based on the migration guidance */
    /* 'dimDynamicAccountController' controller object is used with 'ExpenseCost_LedgerDimension' segmented entry controls.*/
    DimensionDynamicAccountController dimDynamicAccountController;

##### <a name="dynamics-ax-for-operations"></a><span data-ttu-id="2649a-155">Dynamics AX for Operations</span><span class="sxs-lookup"><span data-stu-id="2649a-155">Dynamics AX for Operations</span></span>

<span data-ttu-id="2649a-156">**dimDynamicAccountController** 変数は、フォームで使用されなくなりました。</span><span class="sxs-lookup"><span data-stu-id="2649a-156">The **dimDynamicAccountController** variable is no longer used on the form.</span></span> <span data-ttu-id="2649a-157">したがって、削除できるようになりました。</span><span class="sxs-lookup"><span data-stu-id="2649a-157">Therefore, you can now delete it.</span></span>

## <a name="complex-migration-scenario--ledgerjournaltransdaily-form"></a><span data-ttu-id="2649a-158">複雑な移行シナリオ – LedgerJournalTransDaily フォーム</span><span class="sxs-lookup"><span data-stu-id="2649a-158">Complex migration scenario – LedgerJournalTransDaily form</span></span>
1.  <span data-ttu-id="2649a-159">アプリケーション エクスプローラーで **LedgerJournalTransDaily** フォームを検索します。</span><span class="sxs-lookup"><span data-stu-id="2649a-159">Search for the **LedgerJournalTransDaily** form in Application Explorer.</span></span>
2.  <span data-ttu-id="2649a-160">現在のプロジェクトにフォームを追加します。</span><span class="sxs-lookup"><span data-stu-id="2649a-160">Add the form to the current project.</span></span>
3.  <span data-ttu-id="2649a-161">フォーム デザイン ビューとコード エディタ ビューで、フォームを開きます。</span><span class="sxs-lookup"><span data-stu-id="2649a-161">Open the form in the form design view and the code editor view.</span></span>
4.  <span data-ttu-id="2649a-162">フォーム デザイン ビューで、手動でコントロール ツリーを移動するか、**ファイル** タブの下にある検索バーで「SegmentedEntry」を検索して、SEC を見つけます。</span><span class="sxs-lookup"><span data-stu-id="2649a-162">In the form design view, find the SEC, either by manually walking the control tree or by searching for “SegmentedEntry” in the search bar below the **File** tab.</span></span>
5.  <span data-ttu-id="2649a-163">SEC を選択し、次の情報を確認します。</span><span class="sxs-lookup"><span data-stu-id="2649a-163">Select the SEC, and verify the following information:</span></span>
    -   <span data-ttu-id="2649a-164">コントロールの横にある括弧で指定されたコントロールのタイプは、**SegmentedEntryControl** です。</span><span class="sxs-lookup"><span data-stu-id="2649a-164">The type for the control, as specified in parenthesis next to the control, is **SegmentedEntryControl**.</span></span>
    -   <span data-ttu-id="2649a-165">**コントローラー クラス** プロパティは **DimensionDynamicAccountController** に設定されます。</span><span class="sxs-lookup"><span data-stu-id="2649a-165">The **Controller class** property is set to **DimensionDynamicAccountController**.</span></span> <span data-ttu-id="2649a-166">このプロパティは、SEC のこのインスタンスが使用するコントローラーのタイプを示します。</span><span class="sxs-lookup"><span data-stu-id="2649a-166">This property indicates the type of controller that this instance of the SEC will use.</span></span> <span data-ttu-id="2649a-167">コントローラーのタイプによって、コントロールのビヘイビアーが決まります。</span><span class="sxs-lookup"><span data-stu-id="2649a-167">The type of controller, in turn, determines the behavior of the control.</span></span>

6.  <span data-ttu-id="2649a-168">コード エディタ ビューに切り替え、フォーム ソース コードで "TODO: (コード アップグレード) \[セグメント化されたエントリ コントロール\]" のすべての事例を検索します。</span><span class="sxs-lookup"><span data-stu-id="2649a-168">Switch to the code editor view, and search for all occurrences of “TODO: (Code Upgrade) \[Segmented entry control\]” in the form source code.</span></span>
7.  <span data-ttu-id="2649a-169">検索結果で、最初の 3 件の結果はコントローラー変数申告用です。</span><span class="sxs-lookup"><span data-stu-id="2649a-169">In the search results, the first three results are for the controller variable declarations.</span></span> <span data-ttu-id="2649a-170">"仕事" を添付しているコメントを参照して、どの SEC インスタンスがどのコントローラー インスタンスを使用しているか示すマッピングを記録します。</span><span class="sxs-lookup"><span data-stu-id="2649a-170">Look at the comments that accompany the TODOs, and make a note of the mapping that shows which SEC instance uses which controller instance.</span></span> <span data-ttu-id="2649a-171">このマッピングは、コントローラーでのメソッド呼び出しをコントロールでのメソッド呼び出しに置き換えるときに必要です。</span><span class="sxs-lookup"><span data-stu-id="2649a-171">You will need this mapping when you replace method calls on the controller with method calls on the control.</span></span> <span data-ttu-id="2649a-172">コントローラーからコントロールへのマッピングがどのようなものかを次に示します。</span><span class="sxs-lookup"><span data-stu-id="2649a-172">Here is what the controller-to-control mapping looks like:</span></span>
    1.  <span data-ttu-id="2649a-173">dimAccountController</span><span class="sxs-lookup"><span data-stu-id="2649a-173">dimAccountController</span></span>
        1.  <span data-ttu-id="2649a-174">LedgerJournalTrans\_AccountNum</span><span class="sxs-lookup"><span data-stu-id="2649a-174">LedgerJournalTrans\_AccountNum</span></span>
        2.  <span data-ttu-id="2649a-175">LedgerJournalTrans\_AccountNum1</span><span class="sxs-lookup"><span data-stu-id="2649a-175">LedgerJournalTrans\_AccountNum1</span></span>
        3.  <span data-ttu-id="2649a-176">Group4\_AccountNum</span><span class="sxs-lookup"><span data-stu-id="2649a-176">Group4\_AccountNum</span></span>

    2.  <span data-ttu-id="2649a-177">dimOffsetAccountController</span><span class="sxs-lookup"><span data-stu-id="2649a-177">dimOffsetAccountController</span></span>
        1.  <span data-ttu-id="2649a-178">GridOffsetAccount</span><span class="sxs-lookup"><span data-stu-id="2649a-178">GridOffsetAccount</span></span>
        2.  <span data-ttu-id="2649a-179">LedgerJournalTrans\_OffsetAccount1</span><span class="sxs-lookup"><span data-stu-id="2649a-179">LedgerJournalTrans\_OffsetAccount1</span></span>
        3.  <span data-ttu-id="2649a-180">Group4\_OffsetAccount</span><span class="sxs-lookup"><span data-stu-id="2649a-180">Group4\_OffsetAccount</span></span>

    3.  <span data-ttu-id="2649a-181">dimPaymentFeeAccountController</span><span class="sxs-lookup"><span data-stu-id="2649a-181">dimPaymentFeeAccountController</span></span>
        1.  <span data-ttu-id="2649a-182">CustPaymJournalFee\_CustAccount</span><span class="sxs-lookup"><span data-stu-id="2649a-182">CustPaymJournalFee\_CustAccount</span></span>

    <span data-ttu-id="2649a-183">コントローラー変数へのすべての参照を削除した後、最後に、これらの 3 つの TODO コメントを修正します。</span><span class="sxs-lookup"><span data-stu-id="2649a-183">You will fix these three TODO comments at the end, after you've removed all references to the controller variables.</span></span>
8.  <span data-ttu-id="2649a-184">次のサブセクションでの説明にあるように、残りの各 TODO コメントが実行されます。</span><span class="sxs-lookup"><span data-stu-id="2649a-184">Go through each of the remaining TODO comments, as described in the following subsections.</span></span>

### <a name="ledgerdimension-data-field"></a><span data-ttu-id="2649a-185">LedgerDimension データ フィールド</span><span class="sxs-lookup"><span data-stu-id="2649a-185">LedgerDimension data field</span></span>

<span data-ttu-id="2649a-186">(**フォーム**&gt;**データ ソース** &gt;**LedgerJournalTrans**&gt; **フィールド** &gt;**LedgerDimension**&gt;  **方法**)</span><span class="sxs-lookup"><span data-stu-id="2649a-186">(**Form** &gt; **Data sources** &gt; **LedgerJournalTrans** &gt; **Fields** &gt; **LedgerDimension** &gt; **Methods**)</span></span>

##### <a name="dynamics-ax-2012"></a><span data-ttu-id="2649a-187">Dynamics AX 2012</span><span class="sxs-lookup"><span data-stu-id="2649a-187">Dynamics AX 2012</span></span>

    /* TODO: (Code Upgrade) [Segmented entry control] This method can be removed if there is no custom implementation */
    // </GEEPL>
    public void jumpRef()
    {
        LedgerJournalTrans_AccountNum.jumpRef();
        LedgerJournalTrans_AccountNum1.jumpRef();
        Group4_AccountNum.jumpRef();
    }

##### <a name="dynamics-ax-for-operations"></a><span data-ttu-id="2649a-188">Dynamics AX for Operations</span><span class="sxs-lookup"><span data-stu-id="2649a-188">Dynamics AX for Operations</span></span>

<span data-ttu-id="2649a-189">このメソッドはコントロールの **jumpRef()** メソッドのみを呼び出し追加の処理は実行しないため、削除できます。</span><span class="sxs-lookup"><span data-stu-id="2649a-189">Because this method only calls the **jumpRef()** method on the control and doesn't perform any additional processing, you can delete it.</span></span>

### <a name="offsetledgerdimension-data-field"></a><span data-ttu-id="2649a-190">OffsetLedgerDimension データ フィールド</span><span class="sxs-lookup"><span data-stu-id="2649a-190">OffsetLedgerDimension data field</span></span>

<span data-ttu-id="2649a-191">(**フォーム**&gt;**データ ソース** &gt;**LedgerJournalTrans**&gt; **フィールド** &gt;**OffsetLedgerDimension**&gt; **方法**)</span><span class="sxs-lookup"><span data-stu-id="2649a-191">(**Form** &gt; **Data sources** &gt; **LedgerJournalTrans** &gt; **Fields** &gt; **OffsetLedgerDimension** &gt; **Methods**)</span></span>

##### <a name="dynamics-ax-2012"></a><span data-ttu-id="2649a-192">Dynamics AX 2012</span><span class="sxs-lookup"><span data-stu-id="2649a-192">Dynamics AX 2012</span></span>

<span data-ttu-id="2649a-193">**OffsetLedgerDimension** フィールドの **jumpRef()** メソッド。</span><span class="sxs-lookup"><span data-stu-id="2649a-193">The **OffsetLedgerDimension** field’s **jumpRef()** method:</span></span>

    /* TODO: (Code Upgrade) [Segmented entry control] This method can be removed if there is no custom implementation */
    public void jumpRef()
    {
        GridOffsetAccount.jumpRef();
        LedgerJournalTrans_OffsetAccount1.jumpRef();
        Group4_OffsetAccount.jumpRef();
    }

##### <a name="dynamics-ax-for-operations"></a><span data-ttu-id="2649a-194">Dynamics AX for Operations</span><span class="sxs-lookup"><span data-stu-id="2649a-194">Dynamics AX for Operations</span></span>

<span data-ttu-id="2649a-195">このメソッドはコントロールの **jumpRef()** メソッドのみを呼び出し追加の処理は実行しないため、削除できます。</span><span class="sxs-lookup"><span data-stu-id="2649a-195">Because this method only calls the **jumpRef()** method on the control and doesn't perform any additional processing, you can delete it.</span></span>

### <a name="ledgerjournaltrans_accountnum-control"></a><span data-ttu-id="2649a-196">LedgerJournalTrans\_AccountNum コントロール</span><span class="sxs-lookup"><span data-stu-id="2649a-196">LedgerJournalTrans\_AccountNum control</span></span>

<span data-ttu-id="2649a-197">(**フォーム**タブの下にある検索バーで、「LedgerJournalTrans\_AccountNum」を検索してください。)</span><span class="sxs-lookup"><span data-stu-id="2649a-197">(Search for "LedgerJournalTrans\_AccountNum" in the search bar below the **Form** tab.)</span></span>

#### <a name="step-1"></a><span data-ttu-id="2649a-198">ステップ１</span><span class="sxs-lookup"><span data-stu-id="2649a-198">Step 1</span></span>

##### <a name="dynamics-ax-2012"></a><span data-ttu-id="2649a-199">Dynamics AX 2012</span><span class="sxs-lookup"><span data-stu-id="2649a-199">Dynamics AX 2012</span></span>

    /* TODO: (Code Upgrade) [Segmented entry control] This method can be removed if there is no custom implementation */
    public void jumpRef()
    {
        LedgerJournalTrans_AccountNum.jumpRef();
        LedgerJournalTrans_AccountNum1.jumpRef();
        Group4_AccountNum.jumpRef();
    }

##### <a name="dynamics-ax-for-operations"></a><span data-ttu-id="2649a-200">Dynamics AX for Operations</span><span class="sxs-lookup"><span data-stu-id="2649a-200">Dynamics AX for Operations</span></span>

<span data-ttu-id="2649a-201">このメソッドはコントロールの **jumpRef()** メソッドのみを呼び出し追加の処理は実行しないため、削除できます。</span><span class="sxs-lookup"><span data-stu-id="2649a-201">Because this method only calls the **jumpRef()** method on the control and doesn't perform any additional processing, you can delete it.</span></span>

#### <a name="step-2"></a><span data-ttu-id="2649a-202">ステップ２</span><span class="sxs-lookup"><span data-stu-id="2649a-202">Step 2</span></span>

##### <a name="dynamics-ax-2012"></a><span data-ttu-id="2649a-203">Dynamics AX 2012</span><span class="sxs-lookup"><span data-stu-id="2649a-203">Dynamics AX 2012</span></span>

    /* TODO: (Code Upgrade) [Segmented entry control] For custom implementation, code in this method needs to be moved elsewhere based on the migration guidance */
    public void loadSegments()
    {
        super();
        LedgerJournalTrans_AccountNum.parmJournalName(ledgerJournalTable.JournalName);
        LedgerJournalTrans_AccountNum1.parmJournalName(ledgerJournalTable.JournalName);
        Group4_AccountNum.parmJournalName(ledgerJournalTable.JournalName);
        LedgerJournalTrans_AccountNum.parmCurrency(ledgerJournalTrans.CurrencyCode);
        LedgerJournalTrans_AccountNum1.parmCurrency(ledgerJournalTrans.CurrencyCode);
        Group4_AccountNum.parmCurrency(ledgerJournalTrans.CurrencyCode);
        LedgerJournalTrans_AccountNum.parmDataAreaId(ledgerJournalTrans.Company ? ledgerJournalTrans.Company : curext());
        LedgerJournalTrans_AccountNum1.parmDataAreaId(ledgerJournalTrans.Company ? ledgerJournalTrans.Company : curext());
        Group4_AccountNum.parmDataAreaId(ledgerJournalTrans.Company ? ledgerJournalTrans.Company : curext());
        LedgerJournalTrans_AccountNum.parmControlDate(ledgerJournalTrans.TransDate);
        LedgerJournalTrans_AccountNum1.parmControlDate(ledgerJournalTrans.TransDate);
        Group4_AccountNum.parmControlDate(ledgerJournalTrans.TransDate);

        /* TODO: (Code Upgrade) [Segmented entry control] Replace this based on the migration guidance */
        // dimAccountController.loadSegments();
        currentMainAccountId = dimAccountController.getValue(DimensionAttribute::getWellKnownDimensionAttribute(DimensionAttributeType::MainAccount));
    }

##### <a name="dynamics-ax-for-operations"></a><span data-ttu-id="2649a-204">Dynamics AX for Operations</span><span class="sxs-lookup"><span data-stu-id="2649a-204">Dynamics AX for Operations</span></span>

1.  <span data-ttu-id="2649a-205">**initLedger()** メソッドを更新します。</span><span class="sxs-lookup"><span data-stu-id="2649a-205">Update the **initLedger()** method.</span></span>

        void initLedger()
        {
            TransDate   dateFrom   = dateNull();
            TransDate   dateTo     = systemDateGet();
            if (element.args().dataset() == tableNum(LedgerJournalTable))
            {
                ledgerJournalTable = element.args().record();
                journalNum         = ledgerJournalTable.JournalNum;
                LedgerJournalTrans_AccountNum.parmJournalName(ledgerJournalTable.JournalName);
                LedgerJournalTrans_AccountNum1.parmJournalName(ledgerJournalTable.JournalName);
                Group4_AccountNum.parmJournalName(ledgerJournalTable.JournalName);
        . . .

2.  <span data-ttu-id="2649a-206">**LedgerJournalTrans** データ ソースの **active()** メソッドでコードを更新します。</span><span class="sxs-lookup"><span data-stu-id="2649a-206">Update the code in the **LedgerJournalTrans** data source’s **active()** method.</span></span> <span data-ttu-id="2649a-207">**注記:** **getValue()** メソッドは、勘定タイプが**元帳**に設定されている場合にのみ呼び出す必要があります。</span><span class="sxs-lookup"><span data-stu-id="2649a-207">**Note:** The **getValue()** method should be called only if the account type is set to **Ledger**.</span></span> <span data-ttu-id="2649a-208">それ以外の場合、このメソッドを呼び出すと、無効な関数呼び出しが発生します。</span><span class="sxs-lookup"><span data-stu-id="2649a-208">Otherwise, a call to this method will cause an invalid function call.</span></span>

        . . .
        LedgerJournalTrans_AccountNum.parmCurrency(ledgerJournalTrans.CurrencyCode);
        LedgerJournalTrans_AccountNum1.parmCurrency(ledgerJournalTrans.CurrencyCode);
        Group4_AccountNum.parmCurrency(ledgerJournalTrans.CurrencyCode);
        LedgerJournalTrans_AccountNum.parmDataAreaId(ledgerJournalTrans.Company ? ledgerJournalTrans.Company : curext());
        LedgerJournalTrans_AccountNum1.parmDataAreaId(ledgerJournalTrans.Company ? ledgerJournalTrans.Company : curext());
        Group4_AccountNum.parmDataAreaId(ledgerJournalTrans.Company ? ledgerJournalTrans.Company : curext());
        LedgerJournalTrans_AccountNum.parmControlDate(ledgerJournalTrans.TransDate);
        LedgerJournalTrans_AccountNum1.parmControlDate(ledgerJournalTrans.TransDate);
        Group4_AccountNum.parmControlDate(ledgerJournalTrans.TransDate);
        if (ledgerJournalTrans.AccountType == LedgerJournalACType::Ledger)
        {
            currentMainAccountId = LedgerJournalTrans_AccountNum.getValue(DimensionAttribute::getWellKnownDimensionAttribute(DimensionAttributeType::MainAccount));
        }
        else
        {
            currentMainAccountId = 0;
        }
        return ret;

3.  <span data-ttu-id="2649a-209">**LedgerJournalTrans** データ ソースの **CurrencyCode** フィールドの **modified()** メソッドに、次のコードを追加します。</span><span class="sxs-lookup"><span data-stu-id="2649a-209">Add the following code to the **modified()** method of the **LedgerJournalTrans** data source’s **CurrencyCode** field.</span></span>

        LedgerJournalTrans_AccountNum.parmCurrency(ledgerJournalTrans.CurrencyCode);
        LedgerJournalTrans_AccountNum1.parmCurrency(ledgerJournalTrans.CurrencyCode);
        Group4_AccountNum.parmCurrency(ledgerJournalTrans.CurrencyCode);

4.  <span data-ttu-id="2649a-210">**LedgerJournalTrans** データ ソースの **Company** フィールドの **modified()** メソッドに、次のコードを追加します。</span><span class="sxs-lookup"><span data-stu-id="2649a-210">Add the following code to the **modified()** method of the **LedgerJournalTrans** data source’s **Company** field.</span></span>

        LedgerJournalTrans_AccountNum.parmDataAreaId(ledgerJournalTrans.Company ? ledgerJournalTrans.Company : curext());
        LedgerJournalTrans_AccountNum1.parmDataAreaId(ledgerJournalTrans.Company ? ledgerJournalTrans.Company : curext());
        Group4_AccountNum.parmDataAreaId(ledgerJournalTrans.Company ? ledgerJournalTrans.Company : curext());

5.  <span data-ttu-id="2649a-211">**LedgerJournalTrans** データ ソースの **TransDate** フィールドの **modified()** メソッドに、次のコードを追加します。</span><span class="sxs-lookup"><span data-stu-id="2649a-211">Add the following code to the **modified()** method of the **LedgerJournalTrans** data source’s **TransDate** field.</span></span>

        LedgerJournalTrans_AccountNum.parmControlDate(ledgerJournalTrans.TransDate);
        LedgerJournalTrans_AccountNum1.parmControlDate(ledgerJournalTrans.TransDate);
        Group4_AccountNum.parmControlDate(ledgerJournalTrans.TransDate);

6.  <span data-ttu-id="2649a-212">**loadSegments()** メソッドを削除します。</span><span class="sxs-lookup"><span data-stu-id="2649a-212">Delete the **loadSegments()** method.</span></span>

#### <a name="step-3"></a><span data-ttu-id="2649a-213">ステップ 3</span><span class="sxs-lookup"><span data-stu-id="2649a-213">Step 3</span></span>

##### <a name="dynamics-ax-2012"></a><span data-ttu-id="2649a-214">Dynamics AX 2012</span><span class="sxs-lookup"><span data-stu-id="2649a-214">Dynamics AX 2012</span></span>

    /* TODO: (Code Upgrade) [Segmented entry control] Fix controller usage, if any, in this method based on the migration guidance */
    public void lookup()
    {
        // Polish sale disposal may require to filter asset that are not
        // marked for sale. lookupAccountNum method needs the ledgerJournalTrans_Asset.TransType
        // value to filter appropriately the assets. Thus, ledgerJournalTrans_Asset is
        // passed to accountNumLookup metho jumpRef d.
        // <GEEPL>
        if (!ledgerJournalEngine.accountNumLookup(ledgerJournalTrans_AccountNum,
            ledgerJournalTrans,
            ledgerJournalTrans.OffsetAccountType,
            ledgerJournalTrans.parmOffsetAccount(),
            ledgerJournalTrans_Asset))
        {
            super();
        }
        // </GEEPL>
    }

##### <a name="dynamics-ax-for-operations"></a><span data-ttu-id="2649a-215">Dynamics AX for Operations</span><span class="sxs-lookup"><span data-stu-id="2649a-215">Dynamics AX for Operations</span></span>

<span data-ttu-id="2649a-216">このメソッドは、コントロールのカスタム ルックアップを実装します。</span><span class="sxs-lookup"><span data-stu-id="2649a-216">This method implements a custom lookup for the control.</span></span> <span data-ttu-id="2649a-217">したがって、メソッドをそのままにします。</span><span class="sxs-lookup"><span data-stu-id="2649a-217">Therefore, leave the method as it is.</span></span> <span data-ttu-id="2649a-218">"仕事" を削除します。</span><span class="sxs-lookup"><span data-stu-id="2649a-218">Just remove the TODO.</span></span> <span data-ttu-id="2649a-219">カスタムのルックアップをフック アップするには、SEC の **checkUseCustomLookup** メソッドをオーバーライドする必要があります。</span><span class="sxs-lookup"><span data-stu-id="2649a-219">To hook up custom lookups, you must override the SEC’s **checkUseCustomLookup** method.</span></span> <span data-ttu-id="2649a-220">また、カスタム ルックアップ フォームで **closeSelectRecord** メソッドが上書きされたことを確認してください。</span><span class="sxs-lookup"><span data-stu-id="2649a-220">Additionally, make sure that the **closeSelectRecord** method on the custom lookup form is overridden.</span></span> <span data-ttu-id="2649a-221">例については、**CustTableLookup** フォームを参照してください。</span><span class="sxs-lookup"><span data-stu-id="2649a-221">For an example, see the **CustTableLookup** form.</span></span>

#### <a name="step-4"></a><span data-ttu-id="2649a-222">ステップ 4</span><span class="sxs-lookup"><span data-stu-id="2649a-222">Step 4</span></span>

##### <a name="dynamics-ax-2012"></a><span data-ttu-id="2649a-223">Dynamics AX 2012</span><span class="sxs-lookup"><span data-stu-id="2649a-223">Dynamics AX 2012</span></span>

    /* TODO: (Code Upgrade) [Segmented entry control] For custom implementation, code in this method needs to be moved elsewhere based on the migration guidance */
    public void segmentValueChanged(SegmentValueChangedEventArgs _e)
    {
        // <GIN>
        if (TaxWithholdParameters_IN::checkTaxParameters()
            && ledgerJournalTrans.TaxWithholdCode_IN != '')
        {
            if (Box::okCancel("@GLS222698",
                DialogButton::Cancel) == DialogButton::Cancel)
            {
                return;
            }
        }
        // </GIN>
        super(_e);

        /* TODO: (Code Upgrade) [Segmented entry control] Replace this based on the migration guidance */
        // dimAccountController.segmentValueChanged(_e);
        currentMainAccountId = ledgerJournalEngine.onPrimaryAccountSegmentChanged(dimAccountController, currentMainAccountId, ledgerJournalTrans);
    }

##### <a name="dynamics-ax-for-operations"></a><span data-ttu-id="2649a-224">Dynamics AX for Operations</span><span class="sxs-lookup"><span data-stu-id="2649a-224">Dynamics AX for Operations</span></span>

1.  <span data-ttu-id="2649a-225">コントロールの **onSegmentChanged()** メソッドをオーバーライドし、次のコードを追加します。</span><span class="sxs-lookup"><span data-stu-id="2649a-225">Override the **onSegmentChanged()** method on the control, and add the following code to it.</span></span>

        /// <summary>
        /// Event handler for the segment changed event.
        /// </summary>
        /// <param name = "_segment">The segment that has been changed.</param>
        public void onSegmentChanged(DimensionControlSegment _segment)
        {
            super(_segment);

            // <GIN>
            if (TaxWithholdParameters_IN::checkTaxParameters()
                && ledgerJournalTrans.TaxWithholdCode_IN != '')
            {
                if (Box::okCancel("@GLS222698",
                    DialogButton::Cancel) == DialogButton::Cancel)
                {
                    return;
                }
            }

            // </GIN>
            if (_segment.parmName() == mainAccountDimAttrName)
            {
                previousMainAccountId = currentMainAccountId;
            }
            currentMainAccountId = ledgerJournalEngine.onPrimaryAccountSegmentChanged(LedgerJournalTrans_AccountNum, currentMainAccountId, ledgerJournalTrans);
        }

2.  <span data-ttu-id="2649a-226">**segmentValueChanged()** メソッドを削除します。</span><span class="sxs-lookup"><span data-stu-id="2649a-226">Delete the **segmentValueChanged()** method.</span></span> <span data-ttu-id="2649a-227">**注記:** **onPrimaryAccountSegmentChanged()** メソッドでは、コントローラー オブジェクトが必要ですが、このコードは SEC のインスタンスを渡すので、**onSegmentChanged()** メソッドの前のコードはコンパイルされません。</span><span class="sxs-lookup"><span data-stu-id="2649a-227">**Note:** The preceding code for the **onSegmentChanged()** method will not compile, because the **onPrimaryAccountSegmentChanged()** method expects a controller object, but this code passes an instance of the SEC.</span></span> <span data-ttu-id="2649a-228">コントロール インスタンスでメソッドを呼び出すには、メソッドのシグネチャとその実装を適宜変更する必要があります。</span><span class="sxs-lookup"><span data-stu-id="2649a-228">To call methods on the control instance, you must change the method’s signature and its implementation accordingly.</span></span> <span data-ttu-id="2649a-229">このメソッドは、50 以上の呼び出し元が使用されます。</span><span class="sxs-lookup"><span data-stu-id="2649a-229">This method is used by more than 50 callers.</span></span> <span data-ttu-id="2649a-230">したがって、これらの呼び出しをすべて更新する必要があります。</span><span class="sxs-lookup"><span data-stu-id="2649a-230">Therefore, you would also have to update all those calls.</span></span> <span data-ttu-id="2649a-231">または、このガイダンスに従うことによって新しいメソッドを追加できます。</span><span class="sxs-lookup"><span data-stu-id="2649a-231">Alternatively, you can add a new method that follows this guidance.</span></span>

#### <a name="step-5"></a><span data-ttu-id="2649a-232">ステップ 5</span><span class="sxs-lookup"><span data-stu-id="2649a-232">Step 5</span></span>

##### <a name="dynamics-ax-2012"></a><span data-ttu-id="2649a-233">Dynamics AX 2012</span><span class="sxs-lookup"><span data-stu-id="2649a-233">Dynamics AX 2012</span></span>

    /* TODO: (Code Upgrade) [Segmented entry control] This method can be removed if there is no custom implementation */
    public boolean validate()
    {
        boolean isValid;
        isValid = super();

        /* TODO: (Code Upgrade) [Segmented entry control] This statement can be removed if there is no custom logic */
        // isValid = dimAccountController.validate() && isValid;
        return isValid;
    }

##### <a name="dynamics-ax-for-operations"></a><span data-ttu-id="2649a-234">Dynamics AX for Operations</span><span class="sxs-lookup"><span data-stu-id="2649a-234">Dynamics AX for Operations</span></span>

<span data-ttu-id="2649a-235">このメソッドはコントロールの **validate()** メソッドのみを呼び出し追加の処理は実行しないため、削除できます。</span><span class="sxs-lookup"><span data-stu-id="2649a-235">Because this method only calls the **validate()** method on the control and doesn't perform any additional processing, you can delete it.</span></span>

### <a name="gridoffsetaccount-control"></a><span data-ttu-id="2649a-236">GridOffsetAccount コントロール</span><span class="sxs-lookup"><span data-stu-id="2649a-236">GridOffsetAccount control</span></span>

<span data-ttu-id="2649a-237">(**フォーム**タブの下にある「GridOffsetAccount」を検索してください。)</span><span class="sxs-lookup"><span data-stu-id="2649a-237">(Search for "GridOffsetAccount" in the search bar below the **Form** tab.)</span></span>

#### <a name="step-1"></a><span data-ttu-id="2649a-238">ステップ１</span><span class="sxs-lookup"><span data-stu-id="2649a-238">Step 1</span></span>

##### <a name="dynamics-ax-2012"></a><span data-ttu-id="2649a-239">Dynamics AX 2012</span><span class="sxs-lookup"><span data-stu-id="2649a-239">Dynamics AX 2012</span></span>

    /* TODO: (Code Upgrade) [Segmented entry control] For custom implementation, code in this method needs to be moved elsewhere based on the migration guidance */
    void gotFocus()
    {
        super();
        if (ledgerJournalTable.FixedOffsetAccount)
        {
            gridOffsetAccount.allowEdit(ledgerJournalTrans.OffsetAccountType == LedgerJournalACType::Ledger);
        }
        else if (!gridOffsetAccount.allowEdit())
        {
            gridOffsetAccount.allowEdit(true);
        }
    }

##### <a name="dynamics-ax-for-operations"></a><span data-ttu-id="2649a-240">Dynamics AX for Operations</span><span class="sxs-lookup"><span data-stu-id="2649a-240">Dynamics AX for Operations</span></span>

1.  <span data-ttu-id="2649a-241">ledgerJournalTable バッファを更新するコードの後に、**initLedger()** メソッドへ次のコードを追加します。</span><span class="sxs-lookup"><span data-stu-id="2649a-241">Add the following code to the **initLedger()** method, after the code that updates the ledgerJournalTable buffer.</span></span>

        . . .
        if (element.args().dataset() == tableNum(LedgerJournalTable))
        {
            ledgerJournalTable = element.args().record();
            journalNum         = ledgerJournalTable.JournalNum;
            LedgerJournalTrans_AccountNum.parmJournalName(ledgerJournalTable.JournalName);
            LedgerJournalTrans_AccountNum1.parmJournalName(ledgerJournalTable.JournalName);
            Group4_AccountNum.parmJournalName(ledgerJournalTable.JournalName);
            if (ledgerJournalTable.FixedOffsetAccount)
            {               
                gridOffsetAccount.allowEdit(ledgerJournalTrans.OffsetAccountType == LedgerJournalACType::Ledger);
            }
            else if (!gridOffsetAccount.allowEdit())
            {
                gridOffsetAccount.allowEdit(true);
            }
        . . .

2.  <span data-ttu-id="2649a-242">**gotFocus()** メソッドを削除します。</span><span class="sxs-lookup"><span data-stu-id="2649a-242">Delete the **gotFocus()** method.</span></span>

#### <a name="step-2"></a><span data-ttu-id="2649a-243">ステップ２</span><span class="sxs-lookup"><span data-stu-id="2649a-243">Step 2</span></span>

##### <a name="dynamics-ax-2012"></a><span data-ttu-id="2649a-244">Dynamics AX 2012</span><span class="sxs-lookup"><span data-stu-id="2649a-244">Dynamics AX 2012</span></span>

    /* TODO: (Code Upgrade) [Segmented entry control] This method can be removed if there is no custom implementation */
    public void jumpRef()
    {
        GridOffsetAccount.jumpRef();
        LedgerJournalTrans_OffsetAccount1.jumpRef();
        Group4_OffsetAccount.jumpRef();
    }

##### <a name="dynamics-ax-for-operations"></a><span data-ttu-id="2649a-245">Dynamics AX for Operations</span><span class="sxs-lookup"><span data-stu-id="2649a-245">Dynamics AX for Operations</span></span>

<span data-ttu-id="2649a-246">このメソッドはコントロールの **jumpRef()** メソッドのみを呼び出し追加の処理は実行しないため、削除できます。</span><span class="sxs-lookup"><span data-stu-id="2649a-246">Because this method only calls the **jumpRef()** method on the control and doesn't perform any additional processing, you can delete it.</span></span>

#### <a name="step-3"></a><span data-ttu-id="2649a-247">ステップ 3</span><span class="sxs-lookup"><span data-stu-id="2649a-247">Step 3</span></span>

##### <a name="dynamics-ax-2012"></a><span data-ttu-id="2649a-248">Dynamics AX 2012</span><span class="sxs-lookup"><span data-stu-id="2649a-248">Dynamics AX 2012</span></span>

    /* TODO: (Code Upgrade) [Segmented entry control] For custom implementation, code in this method needs to be moved elsewhere based on the migration guidance */
    public void loadSegments()
    {
        super();
        GridOffsetAccount.parmJournalName(ledgerJournalTable.JournalName);
        LedgerJournalTrans_OffsetAccount1.parmJournalName(ledgerJournalTable.JournalName);
        Group4_OffsetAccount.parmJournalName(ledgerJournalTable.JournalName);
        GridOffsetAccount.parmCurrency(ledgerJournalTrans.CurrencyCode);
        LedgerJournalTrans_OffsetAccount1.parmCurrency(ledgerJournalTrans.CurrencyCode);
        Group4_OffsetAccount.parmCurrency(ledgerJournalTrans.CurrencyCode);
        GridOffsetAccount.parmDataAreaId(ledgerJournalTrans.getOffsetCompany());
        LedgerJournalTrans_OffsetAccount1.parmDataAreaId(ledgerJournalTrans.getOffsetCompany());
        Group4_OffsetAccount.parmDataAreaId(ledgerJournalTrans.getOffsetCompany());
        GridOffsetAccount.parmControlDate(ledgerJournalTrans.TransDate);
        LedgerJournalTrans_OffsetAccount1.parmControlDate(ledgerJournalTrans.TransDate);
        Group4_OffsetAccount.parmControlDate(ledgerJournalTrans.TransDate);

        /* TODO: (Code Upgrade) [Segmented entry control] Replace this based on the migration guidance */
        // dimOffsetAccountController.loadSegments();
        currentOffsetMainAccountId = dimOffsetAccountController.getValue(DimensionAttribute::getWellKnownDimensionAttribute(DimensionAttributeType::MainAccount));

        // Lock the main account segment if "Fixed offset account" is selected in Journal Names
        if (ledgerJournalTrans.OffsetAccountType == LedgerJournalACType::Ledger)
        {
            GridOffsetAccount.parmLockMainAccountSegment(ledgerJournalTable.FixedOffsetAccount);
            LedgerJournalTrans_OffsetAccount1.parmLockMainAccountSegment(ledgerJournalTable.FixedOffsetAccount);
            Group4_OffsetAccount.parmLockMainAccountSegment(ledgerJournalTable.FixedOffsetAccount);
        }
    }

##### <a name="dynamics-ax-for-operations"></a><span data-ttu-id="2649a-249">Dynamics AX for Operations</span><span class="sxs-lookup"><span data-stu-id="2649a-249">Dynamics AX for Operations</span></span>

1.  <span data-ttu-id="2649a-250">**initLedger()** メソッドを更新します。</span><span class="sxs-lookup"><span data-stu-id="2649a-250">Update the **initLedger()** method.</span></span> <span data-ttu-id="2649a-251">**注記:** **getValue()** メソッドは、勘定タイプが**元帳**に設定されている場合にのみ呼び出す必要があります。</span><span class="sxs-lookup"><span data-stu-id="2649a-251">**Note:** The **getValue()** method should be called only if the account type is set to **Ledger**.</span></span> <span data-ttu-id="2649a-252">それ以外の場合、このメソッドを呼び出すと、無効な関数呼び出しが発生します。</span><span class="sxs-lookup"><span data-stu-id="2649a-252">Otherwise, a call to this method will cause an invalid function call.</span></span>

        void initLedger()
        {
            TransDate   dateFrom   = dateNull();
            TransDate   dateTo     = systemDateGet();
            if (element.args().dataset() == tableNum(LedgerJournalTable))
            {
                ledgerJournalTable = element.args().record();
                journalNum         = ledgerJournalTable.JournalNum;
                GridOffsetAccount.parmJournalName(ledgerJournalTable.JournalName);
                LedgerJournalTrans_OffsetAccount1.parmJournalName(ledgerJournalTable.JournalName);
                Group4_OffsetAccount.parmJournalName(ledgerJournalTable.JournalName);
                if (ledgerJournalTrans.OffsetAccountType == LedgerJournalACType::Ledger)
                {
                    currentOffsetMainAccountId = GridOffsetAccount.getValue(DimensionAttribute::getWellKnownDimensionAttribute(DimensionAttributeType::MainAccount));
                }
                else
                {
                    currentOffsetMainAccountId = 0;
                }

                // Lock the main account segment if "Fixed offset account" is selected in Journal Names
                if (ledgerJournalTrans.OffsetAccountType == LedgerJournalACType::Ledger)
                {
                    GridOffsetAccount.parmLockMainAccountSegment(ledgerJournalTable.FixedOffsetAccount);
                }
        . . .

2.  <span data-ttu-id="2649a-253">**LedgerJournalTrans** データ ソースの **active()** メソッドでコードを更新します。</span><span class="sxs-lookup"><span data-stu-id="2649a-253">Update the code in the **LedgerJournalTrans** data source’s **active()** method.</span></span> <span data-ttu-id="2649a-254">**注記:** **getValue()** メソッドは、勘定タイプが**元帳**に設定されている場合にのみ呼び出す必要があります。</span><span class="sxs-lookup"><span data-stu-id="2649a-254">**Note:** The **getValue()** method should be called only if the account type is set to **Ledger**.</span></span> <span data-ttu-id="2649a-255">それ以外の場合、このメソッドを呼び出すと、無効な関数呼び出しが発生します。</span><span class="sxs-lookup"><span data-stu-id="2649a-255">Otherwise, a call to this method will cause an invalid function call.</span></span>

        . . .
        GridOffsetAccount.parmCurrency(ledgerJournalTrans.CurrencyCode);
        LedgerJournalTrans_OffsetAccount1.parmCurrency(ledgerJournalTrans.CurrencyCode);
        Group4_OffsetAccount.parmCurrency(ledgerJournalTrans.CurrencyCode);
        GridOffsetAccount.parmDataAreaId(ledgerJournalTrans.getOffsetCompany());
        LedgerJournalTrans_OffsetAccount1.parmDataAreaId(ledgerJournalTrans.getOffsetCompany());
        Group4_OffsetAccount.parmDataAreaId(ledgerJournalTrans.getOffsetCompany());
        GridOffsetAccount.parmControlDate(ledgerJournalTrans.TransDate);
        LedgerJournalTrans_OffsetAccount1.parmControlDate(ledgerJournalTrans.TransDate);
        Group4_OffsetAccount.parmControlDate(ledgerJournalTrans.TransDate);
        if (ledgerJournalTrans.OffsetAccountType == LedgerJournalACType::Ledger)
        {
            currentOffsetMainAccountId = GridOffsetAccount.getValue( DimensionAttribute::getWellKnownDimensionAttribute(DimensionAttributeType::MainAccount));
        }
        else
        {
            currentOffsetMainAccountId = 0;
        }

        // Lock the main account segment if "Fixed offset account" is selected in Journal Names
        if (ledgerJournalTrans.OffsetAccountType == LedgerJournalACType::Ledger)
        { 
            GridOffsetAccount.parmLockMainAccountSegment(ledgerJournalTable.FixedOffsetAccount);
        }
        return ret;

3.  <span data-ttu-id="2649a-256">**LedgerJournalTrans** データ ソースの **CurrencyCode** フィールドの **modified()** メソッドに、次のコードを追加します。</span><span class="sxs-lookup"><span data-stu-id="2649a-256">Add the following code to the **modified()** method of the **LedgerJournalTrans** data source’s **CurrencyCode** field.</span></span>

        GridOffsetAccount.parmCurrency(ledgerJournalTrans.CurrencyCode);
        LedgerJournalTrans_OffsetAccount1.parmCurrency(ledgerJournalTrans.CurrencyCode);
        Group4_OffsetAccount.parmCurrency(ledgerJournalTrans.CurrencyCode);

4.  <span data-ttu-id="2649a-257">**LedgerJournalTrans** データ ソースの **OffsetCompany** フィールドの **modified()** メソッドに、次のコードを追加します。</span><span class="sxs-lookup"><span data-stu-id="2649a-257">Add the following code to the **modified()** method of the **LedgerJournalTrans** data source’s **OffsetCompany** field.</span></span>

        GridOffsetAccount.parmDataAreaId(ledgerJournalTrans.getOffsetCompany());
        LedgerJournalTrans_OffsetAccount1.parmDataAreaId(ledgerJournalTrans.getOffsetCompany());
        Group4_OffsetAccount.parmDataAreaId(ledgerJournalTrans.getOffsetCompany());

5.  <span data-ttu-id="2649a-258">**LedgerJournalTrans** データ ソースの **TransDate** フィールドの **modified()** メソッドに、次のコードを追加します。</span><span class="sxs-lookup"><span data-stu-id="2649a-258">Add the following code to the **modified()** method of the **LedgerJournalTrans** data source’s **TransDate** field.</span></span>

        GridOffsetAccount.parmControlDate(ledgerJournalTrans.TransDate);
        LedgerJournalTrans_OffsetAccount1.parmControlDate(ledgerJournalTrans.TransDate);
        Group4_OffsetAccount.parmControlDate(ledgerJournalTrans.TransDate);

6.  <span data-ttu-id="2649a-259">**LedgerJournalTrans** データ ソースの **OffsetAccountType** フィールドの **modified()** メソッドに、次のコードを追加します。</span><span class="sxs-lookup"><span data-stu-id="2649a-259">Add the following code to the **modified()** method of the **LedgerJournalTrans** data source’s **OffsetAccountType** field.</span></span> <span data-ttu-id="2649a-260">**注記:** **getValue()** メソッドは、勘定タイプが**元帳**に設定されている場合にのみ呼び出す必要があります。</span><span class="sxs-lookup"><span data-stu-id="2649a-260">**Note:** The **getValue()** method should be called only if the account type is set to **Ledger**.</span></span> <span data-ttu-id="2649a-261">それ以外の場合、このメソッドを呼び出すと、無効な関数呼び出しが発生します。</span><span class="sxs-lookup"><span data-stu-id="2649a-261">Otherwise, a call to this method cause an invalid function call.</span></span>

        if (ledgerJournalTrans.OffsetAccountType == LedgerJournalACType::Ledger)
        {
            currentOffsetMainAccountId = GridOffsetAccount.getValue( DimensionAttribute::getWellKnownDimensionAttribute(DimensionAttributeType::MainAccount));
        }
        else
        {
            currentOffsetMainAccountId = 0;
        }

        // Lock the main account segment if "Fixed offset account" is selected in Journal Names
        if (ledgerJournalTrans.OffsetAccountType == LedgerJournalACType::Ledger)
        {
            GridOffsetAccount.parmLockMainAccountSegment(ledgerJournalTable.FixedOffsetAccount);
        }

7.  <span data-ttu-id="2649a-262">**loadSegments()** メソッドを削除します。</span><span class="sxs-lookup"><span data-stu-id="2649a-262">Delete the **loadSegments()** method.</span></span>

#### <a name="step-4"></a><span data-ttu-id="2649a-263">ステップ 4</span><span class="sxs-lookup"><span data-stu-id="2649a-263">Step 4</span></span>

##### <a name="dynamics-ax-2012"></a><span data-ttu-id="2649a-264">Dynamics AX 2012</span><span class="sxs-lookup"><span data-stu-id="2649a-264">Dynamics AX 2012</span></span>

    /* TODO: (Code Upgrade) [Segmented entry control] Fix controller usage, if any, in this method based on the migration guidance */
    public void lookup()
    {
        // Find the current segment index value
        int currentSegmentIndex = dimOffsetAccountController.parmControl().currentSegmentIndex();
        if ((ledgerJournalTrans.OffsetAccountType == LedgerJournalACType::Ledger &&
            dimOffsetAccountController.getDimensionAttributeByControlIndex(currentSegmentIndex) != DimensionAttribute::getWellKnownDimensionAttribute(DimensionAttributeType::MainAccount)) ||
            !ledgerJournalEngine.offsetAccountNumLookUp(gridOffsetAccount, ledgerJournalTrans))
        {
            super();
        }
    }

##### <a name="dynamics-ax-for-operations"></a><span data-ttu-id="2649a-265">Dynamics AX for Operations</span><span class="sxs-lookup"><span data-stu-id="2649a-265">Dynamics AX for Operations</span></span>

<span data-ttu-id="2649a-266">このメソッドは、コントロールのカスタム ルックアップを実装します。</span><span class="sxs-lookup"><span data-stu-id="2649a-266">This method implements a custom lookup for the control.</span></span> <span data-ttu-id="2649a-267">したがって、メソッドを保持しますが、コントローラーをコントロール インスタンスに置き換えます。</span><span class="sxs-lookup"><span data-stu-id="2649a-267">Therefore, keep the method, but replace the controller with the control instance.</span></span> <span data-ttu-id="2649a-268">この場合、メソッドは **GridOffsetAccount** コントロールでオーバーライドされるため、**dimOffsetAccountController** が (コントローラー変数宣言の "仕事" に示されたマッピングに基づいて) 3 つの異なる SEC インスタンスに使用される場合でも、コントローラーをたった 1 つの SEC インスタンスに置き換える必要があります。</span><span class="sxs-lookup"><span data-stu-id="2649a-268">In this case, because the method is overridden on the **GridOffsetAccount** control, even though **dimOffsetAccountController** was used for three different SEC instances (based on the mapping that is shown in the TODOs on controller variable declarations), we must replace the controller with only one SEC instance.</span></span> <span data-ttu-id="2649a-269">したがって、コードは次のようになります。</span><span class="sxs-lookup"><span data-stu-id="2649a-269">Therefore, the code will look like this.</span></span>

    public void lookup()
    {
        // Find the current segment index value
        int currentSegmentIndex = GridOffsetAccount.getCurrentSegmentIndex();
        if ((ledgerJournalTrans.OffsetAccountType == LedgerJournalACType::Ledger && GridOffsetAccount.getDimensionAttributeByControlIndex(currentSegmentIndex) != DimensionAttribute::getWellKnownDimensionAttribute(DimensionAttributeType::MainAccount)) || !ledgerJournalEngine.offsetAccountNumLookUp(gridOffsetAccount, ledgerJournalTrans))
        {
            super();
        }
    }

<span data-ttu-id="2649a-270">カスタムのルックアップをフック アップするには、SEC の **checkUseCustomLookup** メソッドをオーバーライドする必要があります。</span><span class="sxs-lookup"><span data-stu-id="2649a-270">To hook up custom lookups, you must override the SEC’s **checkUseCustomLookup** method.</span></span> <span data-ttu-id="2649a-271">また、カスタム ルックアップ フォームで **closeSelectRecord** メソッドが上書きされたことを確認してください。</span><span class="sxs-lookup"><span data-stu-id="2649a-271">Additionally, make sure that the **closeSelectRecord** method on the custom lookup form is overridden.</span></span> <span data-ttu-id="2649a-272">例については、**CustTableLookup** フォームを参照してください。</span><span class="sxs-lookup"><span data-stu-id="2649a-272">For an example, see the **CustTableLookup** form.</span></span>

#### <a name="step-5"></a><span data-ttu-id="2649a-273">ステップ 5</span><span class="sxs-lookup"><span data-stu-id="2649a-273">Step 5</span></span>

##### <a name="dynamics-ax-2012"></a><span data-ttu-id="2649a-274">Dynamics AX 2012</span><span class="sxs-lookup"><span data-stu-id="2649a-274">Dynamics AX 2012</span></span>

    /* TODO: (Code Upgrade) [Segmented entry control] For custom implementation, code in this method needs to be moved elsewhere based on the migration guidance */
    public void segmentValueChanged(SegmentValueChangedEventArgs _e)
    {
        super(_e);
        /* TODO: (Code Upgrade) [Segmented entry control] Replace this based on the migration guidance */
        // dimOffsetAccountController.segmentValueChanged(_e);
        currentOffsetMainAccountId = ledgerJournalEngine.onOffsetAccountSegmentChanged(dimOffsetAccountController, currentOffsetMainAccountId, ledgerJournalTrans);
    }

##### <a name="dynamics-ax-for-operations"></a><span data-ttu-id="2649a-275">Dynamics AX for Operations</span><span class="sxs-lookup"><span data-stu-id="2649a-275">Dynamics AX for Operations</span></span>

1.  <span data-ttu-id="2649a-276">コントロールの **onSegmentChanged()** メソッドをオーバーライドし、次のコードを追加します。</span><span class="sxs-lookup"><span data-stu-id="2649a-276">Override the **onSegmentChanged()** method on the control, and add the following code to it.</span></span>

        /// <summary>
        /// Event handler for the segment changed event.
        /// </summary>
        /// <param name = "_segment">The segment that was modified.</param>
        public void onSegmentChanged(DimensionControlSegment _segment)
        {
            super(_segment);
            currentOffsetMainAccountId = ledgerJournalEngine.onOffsetAccountSegmentChanged(
            GridOffsetAccount, currentOffsetMainAccountId, ledgerJournalTrans);
        }

2.  <span data-ttu-id="2649a-277">**segmentValueChanged()** メソッドを削除します。</span><span class="sxs-lookup"><span data-stu-id="2649a-277">Delete the **segmentValueChanged()** method.</span></span> <span data-ttu-id="2649a-278">**注記:** **onOffsetAccountSegmentChanged()** メソッドでは、コントローラー オブジェクトが必要ですが、このコードは SEC のインスタンスを渡すので、**onSegmentChanged()** メソッドの前のコードはコンパイルされません。</span><span class="sxs-lookup"><span data-stu-id="2649a-278">**Note:** The preceding code for the **onSegmentChanged()** method will not compile, because the **onOffsetAccountSegmentChanged()** method expects a controller object, but this code passes an instance of the SEC.</span></span> <span data-ttu-id="2649a-279">コントロール インスタンスでメソッドを呼び出すには、メソッドのシグネチャとその実装を適宜変更する必要があります。</span><span class="sxs-lookup"><span data-stu-id="2649a-279">To call methods on the control instance, you must change the method’s signature and its implementation accordingly.</span></span> <span data-ttu-id="2649a-280">このメソッドは、50 以上の呼び出し元が使用されます。</span><span class="sxs-lookup"><span data-stu-id="2649a-280">This method is used by more than 50 callers.</span></span> <span data-ttu-id="2649a-281">したがって、これらの呼び出しをすべて更新する必要があります。</span><span class="sxs-lookup"><span data-stu-id="2649a-281">Therefore, you would also have to update all those calls.</span></span> <span data-ttu-id="2649a-282">または、このガイダンスに従うことによって新しいメソッドを追加できます。</span><span class="sxs-lookup"><span data-stu-id="2649a-282">Alternatively, you can add a new method that follows this guidance.</span></span>

#### <a name="step-6"></a><span data-ttu-id="2649a-283">ステップ 6</span><span class="sxs-lookup"><span data-stu-id="2649a-283">Step 6</span></span>

##### <a name="dynamics-ax-2012"></a><span data-ttu-id="2649a-284">Dynamics AX 2012</span><span class="sxs-lookup"><span data-stu-id="2649a-284">Dynamics AX 2012</span></span>

    /* TODO: (Code Upgrade) [Segmented entry control] This method can be removed if there is no custom implementation */
    public boolean validate()
    {
        boolean isValid;
        isValid = super();

        /* TODO: (Code Upgrade) [Segmented entry control] This statement can be removed if there is no custom logic */
        // isValid = dimOffsetAccountController.validate() && isValid;
        return isValid;
    }

##### <a name="dynamics-ax-for-operations"></a><span data-ttu-id="2649a-285">Dynamics AX for Operations</span><span class="sxs-lookup"><span data-stu-id="2649a-285">Dynamics AX for Operations</span></span>

<span data-ttu-id="2649a-286">このメソッドはコントロールの **validate()** メソッドのみを呼び出し追加の処理は実行しないため、削除できます。</span><span class="sxs-lookup"><span data-stu-id="2649a-286">Because this method only calls the **validate()** method on the control and doesn't perform any additional processing, you can delete it.</span></span>

### <a name="ledgerjournaltrans_accountnum1"></a><span data-ttu-id="2649a-287">LedgerJournalTrans\_AccountNum1</span><span class="sxs-lookup"><span data-stu-id="2649a-287">LedgerJournalTrans\_AccountNum1</span></span>

<span data-ttu-id="2649a-288">(**フォーム**タブの下にある検索バーで、「LedgerJournalTrans\_AccountNum1」を検索してください。)</span><span class="sxs-lookup"><span data-stu-id="2649a-288">(Search for "LedgerJournalTrans\_AccountNum1" in the search bar below the **Form** tab.)</span></span>

#### <a name="step-1"></a><span data-ttu-id="2649a-289">ステップ１</span><span class="sxs-lookup"><span data-stu-id="2649a-289">Step 1</span></span>

##### <a name="dynamics-ax-2012"></a><span data-ttu-id="2649a-290">Dynamics AX 2012</span><span class="sxs-lookup"><span data-stu-id="2649a-290">Dynamics AX 2012</span></span>

    /* TODO: (Code Upgrade) [Segmented entry control] This method can be removed if there is no custom implementation */
    public void jumpRef()
    {
        LedgerJournalTrans_AccountNum.jumpRef();
        LedgerJournalTrans_AccountNum1.jumpRef();
        Group4_AccountNum.jumpRef();
    }

##### <a name="dynamics-ax-for-operations"></a><span data-ttu-id="2649a-291">Dynamics AX for Operations</span><span class="sxs-lookup"><span data-stu-id="2649a-291">Dynamics AX for Operations</span></span>

<span data-ttu-id="2649a-292">このメソッドはコントロールの **jumpRef()** メソッドのみを呼び出し追加の処理は実行しないため、削除できます。</span><span class="sxs-lookup"><span data-stu-id="2649a-292">Because this method only calls the **jumpRef()** method on the control and doesn't perform any additional processing, you can delete it.</span></span>

#### <a name="step-2"></a><span data-ttu-id="2649a-293">ステップ２</span><span class="sxs-lookup"><span data-stu-id="2649a-293">Step 2</span></span>

##### <a name="dynamics-ax-2012"></a><span data-ttu-id="2649a-294">Dynamics AX 2012</span><span class="sxs-lookup"><span data-stu-id="2649a-294">Dynamics AX 2012</span></span>

    /* TODO: (Code Upgrade) [Segmented entry control] For custom implementation, code in this method needs to be moved elsewhere based on the migration guidance */
    public void loadSegments()
    {
        super();
        LedgerJournalTrans_AccountNum.parmJournalName(ledgerJournalTable.JournalName);
        LedgerJournalTrans_AccountNum1.parmJournalName(ledgerJournalTable.JournalName);
        Group4_AccountNum.parmJournalName(ledgerJournalTable.JournalName);
        LedgerJournalTrans_AccountNum.parmCurrency(ledgerJournalTrans.CurrencyCode);
        LedgerJournalTrans_AccountNum1.parmCurrency(ledgerJournalTrans.CurrencyCode);
        Group4_AccountNum.parmCurrency(ledgerJournalTrans.CurrencyCode);
        LedgerJournalTrans_AccountNum.parmDataAreaId(ledgerJournalTrans.Company ? ledgerJournalTrans.Company : curext());
        LedgerJournalTrans_AccountNum1.parmDataAreaId(ledgerJournalTrans.Company ? ledgerJournalTrans.Company : curext());
        Group4_AccountNum.parmDataAreaId(ledgerJournalTrans.Company ? ledgerJournalTrans.Company : curext());
        LedgerJournalTrans_AccountNum.parmControlDate(ledgerJournalTrans.TransDate);
        LedgerJournalTrans_AccountNum1.parmControlDate(ledgerJournalTrans.TransDate);
        Group4_AccountNum.parmControlDate(ledgerJournalTrans.TransDate);

        /* TODO: (Code Upgrade) [Segmented entry control] Replace this based on the migration guidance */
        // dimAccountController.loadSegments();
        currentMainAccountId = dimAccountController.getValue(DimensionAttribute::getWellKnownDimensionAttribute(DimensionAttributeType::MainAccount));
    }

##### <a name="dynamics-ax-for-operations"></a><span data-ttu-id="2649a-295">Dynamics AX for Operations</span><span class="sxs-lookup"><span data-stu-id="2649a-295">Dynamics AX for Operations</span></span>

<span data-ttu-id="2649a-296">このメソッドを移行する手順は、**LedgerJournalTrans\_AccountNum.loadSegments()** メソッドを移行する手順と同じです。</span><span class="sxs-lookup"><span data-stu-id="2649a-296">The steps for migrating this method are the same as the steps for migrating the **LedgerJournalTrans\_AccountNum.loadSegments()** method.</span></span> <span data-ttu-id="2649a-297">したがって、追加の手順は必要はありません。</span><span class="sxs-lookup"><span data-stu-id="2649a-297">Therefore, no additional steps are required.</span></span> <span data-ttu-id="2649a-298">このメソッドを削除します。</span><span class="sxs-lookup"><span data-stu-id="2649a-298">Delete this method.</span></span>

#### <a name="step-3"></a><span data-ttu-id="2649a-299">ステップ 3</span><span class="sxs-lookup"><span data-stu-id="2649a-299">Step 3</span></span>

##### <a name="dynamics-ax-2012"></a><span data-ttu-id="2649a-300">Dynamics AX 2012</span><span class="sxs-lookup"><span data-stu-id="2649a-300">Dynamics AX 2012</span></span>

    /* TODO: (Code Upgrade) [Segmented entry control] Fix controller usage, if any, in this method based on the migration guidance */
    public void lookup()
    {
        if (!ledgerJournalEngine.accountNumLookup(ledgerJournalTrans_AccountNum1, ledgerJournalTrans))
        {
            super();
        }
    }

##### <a name="dynamics-ax-for-operations"></a><span data-ttu-id="2649a-301">Dynamics AX for Operations</span><span class="sxs-lookup"><span data-stu-id="2649a-301">Dynamics AX for Operations</span></span>

<span data-ttu-id="2649a-302">このメソッドは、コントロールのカスタム ルックアップを実装します。</span><span class="sxs-lookup"><span data-stu-id="2649a-302">This method implements a custom lookup for the control.</span></span> <span data-ttu-id="2649a-303">したがって、メソッドをそのままにします。</span><span class="sxs-lookup"><span data-stu-id="2649a-303">Therefore, leave the method as it is.</span></span> <span data-ttu-id="2649a-304">"仕事" を削除します。</span><span class="sxs-lookup"><span data-stu-id="2649a-304">Just remove the TODO.</span></span> <span data-ttu-id="2649a-305">カスタムのルックアップをフック アップするには、SEC の **checkUseCustomLookup** メソッドをオーバーライドする必要があります。</span><span class="sxs-lookup"><span data-stu-id="2649a-305">To hook up custom lookups, you must override the SEC’s **checkUseCustomLookup** method.</span></span> <span data-ttu-id="2649a-306">また、カスタム ルックアップで **closeSelectRecord** メソッドが上書きされたことを確認してください。</span><span class="sxs-lookup"><span data-stu-id="2649a-306">Additionally, make sure that the **closeSelectRecord** method on the custom lookup is overridden.</span></span> <span data-ttu-id="2649a-307">例については、**CustTableLookup** フォームを参照してください。</span><span class="sxs-lookup"><span data-stu-id="2649a-307">For an example, see the **CustTableLookup** form.</span></span>

#### <a name="step-4"></a><span data-ttu-id="2649a-308">ステップ 4</span><span class="sxs-lookup"><span data-stu-id="2649a-308">Step 4</span></span>

##### <a name="dynamics-ax-2012"></a><span data-ttu-id="2649a-309">Dynamics AX 2012</span><span class="sxs-lookup"><span data-stu-id="2649a-309">Dynamics AX 2012</span></span>

    /* TODO: (Code Upgrade) [Segmented entry control] For custom implementation, code in this method needs to be moved elsewhere based on the migration guidance */
    public void segmentValueChanged(SegmentValueChangedEventArgs _e)
    {
        super(_e);
        /* TODO: (Code Upgrade) [Segmented entry control] Replace this based on the migration guidance */
        // dimAccountController.segmentValueChanged(_e);
        currentMainAccountId = ledgerJournalEngine.onPrimaryAccountSegmentChanged(dimAccountController, currentMainAccountId, ledgerJournalTrans);
    }

##### <a name="dynamics-ax-for-operations"></a><span data-ttu-id="2649a-310">Dynamics AX for Operations</span><span class="sxs-lookup"><span data-stu-id="2649a-310">Dynamics AX for Operations</span></span>

1.  <span data-ttu-id="2649a-311">コントロールの **onSegmentChanged()** メソッドをオーバーライドし、次のコードを追加します。</span><span class="sxs-lookup"><span data-stu-id="2649a-311">Override the **onSegmentChanged()** method on the control, and add the following code to it.</span></span>

        /// <summary>
        /// The event handler when a segment is modified.
        /// </summary>
        /// <param name = "_segment">The segment that was modified.</param>
        public void onSegmentChanged(DimensionControlSegment _segment)
        {
            super(_segment);
            currentMainAccountId = ledgerJournalEngine.onPrimaryAccountSegmentChanged(
            LedgerJournalTrans_AccountNum1, currentMainAccountId, ledgerJournalTrans);
        }

2.  <span data-ttu-id="2649a-312">**segmentValueChanged()** メソッドを削除します。</span><span class="sxs-lookup"><span data-stu-id="2649a-312">Delete the **segmentValueChanged()** method.</span></span> <span data-ttu-id="2649a-313">**注記:** **onPrimaryAccountSegmentChanged()** メソッドでは、コントローラー オブジェクトが必要ですが、このコードは SEC のインスタンスを渡すので、**onSegmentChanged()** メソッドの前のコードはコンパイルされません。</span><span class="sxs-lookup"><span data-stu-id="2649a-313">**Note:** The preceding code for the **onSegmentChanged()** method will not compile, because the **onPrimaryAccountSegmentChanged()** method expects a controller object, but this code passes an instance of the SEC.</span></span> <span data-ttu-id="2649a-314">コントロール インスタンスでメソッドを呼び出すには、メソッドのシグネチャとその実装を適宜変更する必要があります。</span><span class="sxs-lookup"><span data-stu-id="2649a-314">To call methods on the control instance, you must change the method’s signature and its implementation accordingly.</span></span> <span data-ttu-id="2649a-315">このメソッドは、50 以上の呼び出し元が使用されます。</span><span class="sxs-lookup"><span data-stu-id="2649a-315">This method is used by more than 50 callers.</span></span> <span data-ttu-id="2649a-316">したがって、これらの呼び出しをすべて更新する必要があります。</span><span class="sxs-lookup"><span data-stu-id="2649a-316">Therefore, you would also have to update all of those calls.</span></span> <span data-ttu-id="2649a-317">または、このガイダンスに従うことによって新しいメソッドを追加できます。</span><span class="sxs-lookup"><span data-stu-id="2649a-317">Alternatively, you can add a new method that follows this guidance.</span></span>

#### <a name="step-5"></a><span data-ttu-id="2649a-318">ステップ 5</span><span class="sxs-lookup"><span data-stu-id="2649a-318">Step 5</span></span>

##### <a name="dynamics-ax-2012"></a><span data-ttu-id="2649a-319">Dynamics AX 2012</span><span class="sxs-lookup"><span data-stu-id="2649a-319">Dynamics AX 2012</span></span>

    /* TODO: (Code Upgrade) [Segmented entry control] This method can be removed if there is no custom implementation */
    public boolean validate()
    {
        boolean isValid;
        isValid = super();
        /* TODO: (Code Upgrade) [Segmented entry control] This statement can be removed if there is no custom logic */
        // isValid = dimAccountController.validate() && isValid;
        return isValid;
    }

##### <a name="dynamics-ax-for-operations"></a><span data-ttu-id="2649a-320">Dynamics AX for Operations</span><span class="sxs-lookup"><span data-stu-id="2649a-320">Dynamics AX for Operations</span></span>

<span data-ttu-id="2649a-321">このメソッドはコントロールの **validate()** メソッドのみを呼び出し追加の処理は実行しないため、削除できます。</span><span class="sxs-lookup"><span data-stu-id="2649a-321">Because this method only calls the **validate()** method on the control and doesn't perform any additional processing, you can delete it.</span></span>

### <a name="ledgerjournaltrans_offsetaccount1"></a><span data-ttu-id="2649a-322">LedgerJournalTrans\_OffsetAccount1</span><span class="sxs-lookup"><span data-stu-id="2649a-322">LedgerJournalTrans\_OffsetAccount1</span></span>

<span data-ttu-id="2649a-323">(**フォーム**タブの下にある検索バーで、「LedgerJournalTrans\_OffsetAccount1」を検索してください。)</span><span class="sxs-lookup"><span data-stu-id="2649a-323">(Search for "LedgerJournalTrans\_OffsetAccount1" in the search bar below the **Form** tab.)</span></span>

#### <a name="step-1"></a><span data-ttu-id="2649a-324">ステップ１</span><span class="sxs-lookup"><span data-stu-id="2649a-324">Step 1</span></span>

##### <a name="dynamics-ax-2012"></a><span data-ttu-id="2649a-325">Dynamics AX 2012</span><span class="sxs-lookup"><span data-stu-id="2649a-325">Dynamics AX 2012</span></span>

    /* TODO: (Code Upgrade) [Segmented entry control] This method can be removed if there is no custom implementation */
    public void jumpRef()
    {
        GridOffsetAccount.jumpRef();
        LedgerJournalTrans_OffsetAccount1.jumpRef();
        Group4_OffsetAccount.jumpRef();
    }

##### <a name="dynamics-ax-for-operations"></a><span data-ttu-id="2649a-326">Dynamics AX for Operations</span><span class="sxs-lookup"><span data-stu-id="2649a-326">Dynamics AX for Operations</span></span>

<span data-ttu-id="2649a-327">このメソッドはコントロールの **jumpRef()** メソッドのみを呼び出し追加の処理は実行しないため、削除できます。</span><span class="sxs-lookup"><span data-stu-id="2649a-327">Because this method only calls the **jumpRef()** method on the control and doesn't perform any additional processing, you can delete it.</span></span>

#### <a name="step-2"></a><span data-ttu-id="2649a-328">ステップ２</span><span class="sxs-lookup"><span data-stu-id="2649a-328">Step 2</span></span>

##### <a name="dynamics-ax-2012"></a><span data-ttu-id="2649a-329">Dynamics AX 2012</span><span class="sxs-lookup"><span data-stu-id="2649a-329">Dynamics AX 2012</span></span>

    /* TODO: (Code Upgrade) [Segmented entry control] For custom implementation, code in this method needs to be moved elsewhere based on the migration guidance */
    public void loadSegments()
    {
        super();
        GridOffsetAccount.parmJournalName(ledgerJournalTable.JournalName);
        LedgerJournalTrans_OffsetAccount1.parmJournalName(ledgerJournalTable.JournalName);
        Group4_OffsetAccount.parmJournalName(ledgerJournalTable.JournalName);
        GridOffsetAccount.parmCurrency(ledgerJournalTrans.CurrencyCode);
        LedgerJournalTrans_OffsetAccount1.parmCurrency(ledgerJournalTrans.CurrencyCode);
        Group4_OffsetAccount.parmCurrency(ledgerJournalTrans.CurrencyCode);
        GridOffsetAccount.parmDataAreaId(ledgerJournalTrans.getOffsetCompany());
        LedgerJournalTrans_OffsetAccount1.parmDataAreaId(ledgerJournalTrans.getOffsetCompany());
        Group4_OffsetAccount.parmDataAreaId(ledgerJournalTrans.getOffsetCompany());
        GridOffsetAccount.parmControlDate(ledgerJournalTrans.TransDate);
        LedgerJournalTrans_OffsetAccount1.parmControlDate(ledgerJournalTrans.TransDate);
        Group4_OffsetAccount.parmControlDate(ledgerJournalTrans.TransDate);

        /* TODO: (Code Upgrade) [Segmented entry control] Replace this based on the migration guidance */
        // dimOffsetAccountController.loadSegments();
        currentOffsetMainAccountId = dimOffsetAccountController.getValue(DimensionAttribute::getWellKnownDimensionAttribute(DimensionAttributeType::MainAccount));
        // Lock the main account segment if "Fixed offset account" is selected in Journal Names
        if (ledgerJournalTrans.OffsetAccountType == LedgerJournalACType::Ledger)
        {
            GridOffsetAccount.parmLockMainAccountSegment(ledgerJournalTable.FixedOffsetAccount);
            LedgerJournalTrans_OffsetAccount1.parmLockMainAccountSegment(ledgerJournalTable.FixedOffsetAccount);
            Group4_OffsetAccount.parmLockMainAccountSegment(ledgerJournalTable.FixedOffsetAccount);
        }
    }

##### <a name="dynamics-ax-for-operations"></a><span data-ttu-id="2649a-330">Dynamics AX for Operations</span><span class="sxs-lookup"><span data-stu-id="2649a-330">Dynamics AX for Operations</span></span>

<span data-ttu-id="2649a-331">**GridOffsetAccount.loadSegments()** メソッドの移行手順は、すでにこのメソッドに必要な変更のほとんどを行いました。</span><span class="sxs-lookup"><span data-stu-id="2649a-331">The migration steps for the **GridOffsetAccount.loadSegments()** method already made most of the changes that are required for this method.</span></span> <span data-ttu-id="2649a-332">ただし、次の変更を加える必要があります。</span><span class="sxs-lookup"><span data-stu-id="2649a-332">However, you must still make the following changes.</span></span>

1.  <span data-ttu-id="2649a-333">**LedgerJournalTrans** データ ソースの**有効な**メソッドにコード行を追加します。</span><span class="sxs-lookup"><span data-stu-id="2649a-333">Add a line of code to the **LedgerJournalTrans** data source’s **active** method.</span></span>

        if (ledgerJournalTrans.OffsetAccountType == LedgerJournalACType::Ledger)
        {
            currentOffsetMainAccountId = GridOffsetAccount.getValue(
            DimensionAttribute::getWellKnownDimensionAttribute(DimensionAttributeType::MainAccount));
        }
        else
        {
            currentOffsetMainAccountId = 0;
        }

        // Lock the main account segment if "Fixed offset account" is selected in Journal Names
        if (ledgerJournalTrans.OffsetAccountType == LedgerJournalACType::Ledger)
        {
            GridOffsetAccount.parmLockMainAccountSegment(ledgerJournalTable.FixedOffsetAccount);
            LedgerJournalTrans_OffsetAccount1.parmLockMainAccountSegment(ledgerJournalTable.FixedOffsetAccount);
        }

2.  <span data-ttu-id="2649a-334">**LedgerJournalTrans** データ ソースの **OffsetAccountType** フィールドの **modified()** メソッドで同じ変更を行います。</span><span class="sxs-lookup"><span data-stu-id="2649a-334">Make the same change in the **modified()** method of the **LedgerJournalTrans** data source’s **OffsetAccountType** field.</span></span>

        if (ledgerJournalTrans.OffsetAccountType == LedgerJournalACType::Ledger)
        {
            currentOffsetMainAccountId = GridOffsetAccount.getValue(DimensionAttribute::getWellKnownDimensionAttribute(DimensionAttributeType::MainAccount));
        }
        else
        {
            currentOffsetMainAccountId = 0;
        }

        // Lock the main account segment if "Fixed offset account" is selected in Journal Names
        if (ledgerJournalTrans.OffsetAccountType == LedgerJournalACType::Ledger)
        {
            GridOffsetAccount.parmLockMainAccountSegment(ledgerJournalTable.FixedOffsetAccount);
            LedgerJournalTrans_OffsetAccount1.parmLockMainAccountSegment(ledgerJournalTable.FixedOffsetAccount);
        }

3.  <span data-ttu-id="2649a-335">**initLedger()** メソッドで同じ変更を行います。</span><span class="sxs-lookup"><span data-stu-id="2649a-335">Make the same change in the **initLedger()** method.</span></span>

        if (ledgerJournalTrans.OffsetAccountType == LedgerJournalACType::Ledger)
        {
            currentOffsetMainAccountId = GridOffsetAccount.getValue( DimensionAttribute::getWellKnownDimensionAttribute(DimensionAttributeType::MainAccount));
        }
        else
        {
            currentOffsetMainAccountId = 0;
        }

        // Lock the main account segment if "Fixed offset account" is selected in Journal Names
        if (ledgerJournalTrans.OffsetAccountType == LedgerJournalACType::Ledger)
        {
            GridOffsetAccount.parmLockMainAccountSegment(ledgerJournalTable.FixedOffsetAccount);
            LedgerJournalTrans_OffsetAccount1.parmLockMainAccountSegment(ledgerJournalTable.FixedOffsetAccount);
        }

4.  <span data-ttu-id="2649a-336">**loadSegments()** メソッドを削除します。</span><span class="sxs-lookup"><span data-stu-id="2649a-336">Delete the **loadSegments()** method.</span></span>

#### <a name="step-3"></a><span data-ttu-id="2649a-337">ステップ 3</span><span class="sxs-lookup"><span data-stu-id="2649a-337">Step 3</span></span>

##### <a name="dynamics-ax-2012"></a><span data-ttu-id="2649a-338">Dynamics AX 2012</span><span class="sxs-lookup"><span data-stu-id="2649a-338">Dynamics AX 2012</span></span>

    /* TODO: (Code Upgrade) [Segmented entry control] Fix controller usage, if any, in this method based on the migration guidance */
    public void lookup()
    {
        // Find the current segment index value
        int currentSegmentIndex = dimOffsetAccountController.parmControl().currentSegmentIndex();
        if ((ledgerJournalTrans.OffsetAccountType == LedgerJournalACType::Ledger &&
            dimOffsetAccountController.getDimensionAttributeByControlIndex(currentSegmentIndex) != DimensionAttribute::getWellKnownDimensionAttribute(DimensionAttributeType::MainAccount)) ||
            !ledgerJournalEngine.offsetAccountNumLookUp(ledgerJournalTrans_OffsetAccount1, ledgerJournalTrans))
        {
            super();
        }
    }

##### <a name="dynamics-ax-for-operations"></a><span data-ttu-id="2649a-339">Dynamics AX for Operations</span><span class="sxs-lookup"><span data-stu-id="2649a-339">Dynamics AX for Operations</span></span>

<span data-ttu-id="2649a-340">このメソッドは、コントロールのカスタム ルックアップを実装します。</span><span class="sxs-lookup"><span data-stu-id="2649a-340">This method implements a custom lookup for the control.</span></span> <span data-ttu-id="2649a-341">したがって、メソッドを保持しますが、コントローラーをコントロール インスタンスに置き換えます。</span><span class="sxs-lookup"><span data-stu-id="2649a-341">Therefore, keep the method, but replace the controller with the control instance.</span></span> <span data-ttu-id="2649a-342">この場合、メソッドは **LedgerJournalTrans\_OffsetAccount1** コントロールでオーバーライドされるため、**dimOffsetAccountController** が (コントローラー変数宣言の "仕事" に示されたマッピングに基づいて) 3 つの異なる SEC インスタンスに使用される場合でも、コントローラーをたった 1 つの SEC インスタンスに置き換える必要があります。</span><span class="sxs-lookup"><span data-stu-id="2649a-342">In this case, because the method is overridden on the **LedgerJournalTrans\_OffsetAccount1** control, even though **dimOffsetAccountController** was used for three different SEC instances (based on the mapping that is shown in the TODOs on controller variable declarations), we must replace the controller with only one SEC instance.</span></span> <span data-ttu-id="2649a-343">したがって、コードは次のようになります。</span><span class="sxs-lookup"><span data-stu-id="2649a-343">Therefore, the code will look like this.</span></span>

    public void lookup()
    {
        // Find the current segment index value
        int currentSegmentIndex = LedgerJournalTrans_OffsetAccount1.getCurrentSegmentIndex();
        if ((ledgerJournalTrans.OffsetAccountType == LedgerJournalACType::Ledger && LedgerJournalTrans_OffsetAccount1.getDimensionAttributeByControlIndex(currentSegmentIndex) != DimensionAttribute::getWellKnownDimensionAttribute(DimensionAttributeType::MainAccount)) || !ledgerJournalEngine.offsetAccountNumLookUp(ledgerJournalTrans_OffsetAccount1, ledgerJournalTrans))
        {
            super();
        }
    }

<span data-ttu-id="2649a-344">カスタムのルックアップをフック アップするには、SEC の **checkUseCustomLookup** メソッドをオーバーライドする必要があります。</span><span class="sxs-lookup"><span data-stu-id="2649a-344">To hook up custom lookups, you must override the SEC’s **checkUseCustomLookup** method.</span></span> <span data-ttu-id="2649a-345">また、カスタム ルックアップ フォームで **closeSelectRecord** メソッドが上書きされたことを確認してください。</span><span class="sxs-lookup"><span data-stu-id="2649a-345">Additionally, make sure that the **closeSelectRecord** method on the custom lookup form is overridden.</span></span> <span data-ttu-id="2649a-346">例については、**CustTableLookup** フォームを参照してください。</span><span class="sxs-lookup"><span data-stu-id="2649a-346">For an example, see the **CustTableLookup** form.</span></span>

#### <a name="step-4"></a><span data-ttu-id="2649a-347">ステップ 4</span><span class="sxs-lookup"><span data-stu-id="2649a-347">Step 4</span></span>

##### <a name="dynamics-ax-2012"></a><span data-ttu-id="2649a-348">Dynamics AX 2012</span><span class="sxs-lookup"><span data-stu-id="2649a-348">Dynamics AX 2012</span></span>

    /* TODO: (Code Upgrade) [Segmented entry control] For custom implementation, code in this method needs to be moved elsewhere based on the migration guidance */
    public void segmentValueChanged(SegmentValueChangedEventArgs _e)
    {
        super(_e);

        /* TODO: (Code Upgrade) [Segmented entry control] Replace this based on the migration guidance */
        // dimOffsetAccountController.segmentValueChanged(_e);
        currentOffsetMainAccountId = ledgerJournalEngine.onOffsetAccountSegmentChanged(dimOffsetAccountController, currentOffsetMainAccountId, ledgerJournalTrans);
    }

##### <a name="dynamics-ax-for-operations"></a><span data-ttu-id="2649a-349">Dynamics AX for Operations</span><span class="sxs-lookup"><span data-stu-id="2649a-349">Dynamics AX for Operations</span></span>

1.  <span data-ttu-id="2649a-350">コントロールの **onSegmentChanged()** メソッドをオーバーライドし、次のコードを追加します。</span><span class="sxs-lookup"><span data-stu-id="2649a-350">Override the **onSegmentChanged()** method on the control, and add the following code to it.</span></span>

        /// <summary>
        /// The event handler when a segment is modified.
        /// </summary>
        /// <param name = "_segment">The segment that was modified.</param>
        public void onSegmentChanged(DimensionControlSegment _segment)
        {
            super(_segment);
            currentOffsetMainAccountId = ledgerJournalEngine.onOffsetAccountSegmentChanged(
            LedgerJournalTrans_OffsetAccount1, currentOffsetMainAccountId, ledgerJournalTrans);
        }

2.  <span data-ttu-id="2649a-351">**segmentValueChanged()** メソッドを削除します。</span><span class="sxs-lookup"><span data-stu-id="2649a-351">Delete the **segmentValueChanged()** method.</span></span> <span data-ttu-id="2649a-352">**注記:** **onOffsetAccountSegmentChanged()** メソッドでは、コントローラー オブジェクトが必要ですが、このコードは SEC のインスタンスを渡すので、**onSegmentChanged()** メソッドの前のコードはコンパイルされません。</span><span class="sxs-lookup"><span data-stu-id="2649a-352">**Note:** The preceding code for the **onSegmentChanged()** method will not compile, because the **onOffsetAccountSegmentChanged()** method expects a controller object, but this code passes an instance of the SEC.</span></span> <span data-ttu-id="2649a-353">コントロール インスタンスでメソッドを呼び出すには、メソッドのシグネチャとその実装を適宜変更する必要があります。</span><span class="sxs-lookup"><span data-stu-id="2649a-353">To call methods on the control instance, you must change the method’s signature and its implementation accordingly.</span></span> <span data-ttu-id="2649a-354">このメソッドは、50 以上の呼び出し元が使用されます。</span><span class="sxs-lookup"><span data-stu-id="2649a-354">This method is used by more than 50 callers.</span></span> <span data-ttu-id="2649a-355">したがって、これらの呼び出しをすべて更新する必要があります。</span><span class="sxs-lookup"><span data-stu-id="2649a-355">Therefore, you would also have to update all those calls.</span></span> <span data-ttu-id="2649a-356">または、このガイダンスに従うことによって新しいメソッドを追加できます。</span><span class="sxs-lookup"><span data-stu-id="2649a-356">Alternatively, you can add a new method that follows this guidance.</span></span>

#### <a name="step-5"></a><span data-ttu-id="2649a-357">ステップ 5</span><span class="sxs-lookup"><span data-stu-id="2649a-357">Step 5</span></span>

##### <a name="dynamics-ax-2012"></a><span data-ttu-id="2649a-358">Dynamics AX 2012</span><span class="sxs-lookup"><span data-stu-id="2649a-358">Dynamics AX 2012</span></span>

    /* TODO: (Code Upgrade) [Segmented entry control] This method can be removed if there is no custom implementation */
    public boolean validate()
    {
        boolean isValid;
        isValid = super();

        /* TODO: (Code Upgrade) [Segmented entry control] This statement can be removed if there is no custom logic */
        // isValid = dimOffsetAccountController.validate() && isValid;
        return isValid;
    }

##### <a name="dynamics-ax-for-operations"></a><span data-ttu-id="2649a-359">Dynamics AX for Operations</span><span class="sxs-lookup"><span data-stu-id="2649a-359">Dynamics AX for Operations</span></span>

<span data-ttu-id="2649a-360">このメソッドはコントロールの **validate()** メソッドのみを呼び出し追加の処理は実行しないため、削除できます。</span><span class="sxs-lookup"><span data-stu-id="2649a-360">Because this method only calls the **validate()** method on the control and doesn't perform any additional processing, you can delete it.</span></span>

### <a name="custpaymjournalfee_custaccount"></a><span data-ttu-id="2649a-361">CustPaymJournalFee\_CustAccount</span><span class="sxs-lookup"><span data-stu-id="2649a-361">CustPaymJournalFee\_CustAccount</span></span>

<span data-ttu-id="2649a-362">(**フォーム**タブの下にある検索バーで、「CustPaymJournalFee\_CustAccount」を検索してください。)</span><span class="sxs-lookup"><span data-stu-id="2649a-362">(Search for "CustPaymJournalFee\_CustAccount" in the search bar below the **Form** tab.)</span></span>

#### <a name="step-1"></a><span data-ttu-id="2649a-363">ステップ１</span><span class="sxs-lookup"><span data-stu-id="2649a-363">Step 1</span></span>

##### <a name="dynamics-ax-2012"></a><span data-ttu-id="2649a-364">Dynamics AX 2012</span><span class="sxs-lookup"><span data-stu-id="2649a-364">Dynamics AX 2012</span></span>

    /* TODO: (Code Upgrade) [Segmented entry control] This method can be removed if there is no custom implementation */
    public void jumpRef()
    {
        CustPaymJournalFee_CustAccount.jumpRef();
    }

##### <a name="dynamics-ax-for-operations"></a><span data-ttu-id="2649a-365">Dynamics AX for Operations</span><span class="sxs-lookup"><span data-stu-id="2649a-365">Dynamics AX for Operations</span></span>

<span data-ttu-id="2649a-366">このメソッドはコントロールの **jumpRef()** メソッドのみを呼び出し追加の処理は実行しないため、削除できます。</span><span class="sxs-lookup"><span data-stu-id="2649a-366">Because this method only calls the **jumpRef()** method on the control and doesn't perform any additional processing, you can delete it.</span></span>

#### <a name="step-2"></a><span data-ttu-id="2649a-367">ステップ２</span><span class="sxs-lookup"><span data-stu-id="2649a-367">Step 2</span></span>

##### <a name="dynamics-ax-2012"></a><span data-ttu-id="2649a-368">Dynamics AX 2012</span><span class="sxs-lookup"><span data-stu-id="2649a-368">Dynamics AX 2012</span></span>

    /* TODO: (Code Upgrade) [Segmented entry control] For custom implementation, code in this method needs to be moved elsewhere based on the migration guidance */
    public void loadSegments()
    {
        super();
        CustPaymJournalFee_CustAccount.parmJournalName(ledgerJournalTable.JournalName);
        CustPaymJournalFee_CustAccount.parmCurrency(custVendPaymJournalFee.FeeCurrency);
        CustPaymJournalFee_CustAccount.parmControlDate(ledgerJournalTrans.TransDate);

        /* TODO: (Code Upgrade) [Segmented entry control] Replace this based on the migration guidance */
        // dimPaymentFeeAccountController.loadSegments();
        currentPaymentFeeMainAccountId = dimPaymentFeeAccountController.getValue(DimensionAttribute::getWellKnownDimensionAttribute(DimensionAttributeType::MainAccount));
    }

##### <a name="dynamics-ax-for-operations"></a><span data-ttu-id="2649a-369">Dynamics AX for Operations</span><span class="sxs-lookup"><span data-stu-id="2649a-369">Dynamics AX for Operations</span></span>

1.  <span data-ttu-id="2649a-370">**initLedger()** メソッドを更新します。</span><span class="sxs-lookup"><span data-stu-id="2649a-370">Update the **initLedger()** method.</span></span>

        ledgerJournalTable = element.args().record();
        journalNum = ledgerJournalTable.JournalNum;
        LedgerJournalTrans_AccountNum.parmJournalName(ledgerJournalTable.JournalName);
        LedgerJournalTrans_AccountNum1.parmJournalName(ledgerJournalTable.JournalName); Group4_AccountNum.parmJournalName(ledgerJournalTable.JournalName); CustPaymJournalFee_CustAccount.parmJournalName(ledgerJournalTable.JournalName);
        . . .

2.  <span data-ttu-id="2649a-371">**CustVendPaymJournalFee** データ ソースの **active()** メソッドに、次のコードを追加します。</span><span class="sxs-lookup"><span data-stu-id="2649a-371">Add the following code to the **CustVendPaymJournalFee** data source’s **active()** method.</span></span> <span data-ttu-id="2649a-372">**注記:** このメソッドは存在しないため、上書きする必要があります。</span><span class="sxs-lookup"><span data-stu-id="2649a-372">**Note:** The method doesn't exist, so you must override it.</span></span>

        CustPaymJournalFee_CustAccount.parmCurrency(custVendPaymJournalFee.FeeCurrency);

3.  <span data-ttu-id="2649a-373">**CustVendPaymJournalFee** データ ソースの **FeeCurrency** フィールドの **modified()** メソッドに、次のコードを追加します。</span><span class="sxs-lookup"><span data-stu-id="2649a-373">Add the following code to the **modified()** method of the **CustVendPaymJournalFee** data source’s **FeeCurrency** field.</span></span> <span data-ttu-id="2649a-374">**注記:** このメソッドは存在しないため、上書きする必要があります。</span><span class="sxs-lookup"><span data-stu-id="2649a-374">**Note:** The method doesn't exist, so you must override it.</span></span>

        CustPaymJournalFee_CustAccount.parmCurrency(custVendPaymJournalFee.FeeCurrency);

4.  <span data-ttu-id="2649a-375">**LedgerJournalTrans** データ ソースの **active()** メソッドに、次のコードを追加します。</span><span class="sxs-lookup"><span data-stu-id="2649a-375">Add the following code to the **LedgerJournalTrans** data source’s **active()** method.</span></span>

        CustPaymJournalFee_CustAccount.parmControlDate(ledgerJournalTrans.TransDate);

5.  <span data-ttu-id="2649a-376">**LedgerJournalTrans** データ ソースの **TransDate** フィールドの **modified()** メソッドに、次のコードを追加します。</span><span class="sxs-lookup"><span data-stu-id="2649a-376">Add the following code to the **modified()** method of the **LedgerJournalTrans** data source’s **TransDate** field.</span></span>

        CustPaymJournalFee_CustAccount.parmControlDate(ledgerJournalTrans.TransDate);

6.  <span data-ttu-id="2649a-377">**loadSegments()** メソッドを削除します。</span><span class="sxs-lookup"><span data-stu-id="2649a-377">Delete the **loadSegments()** method.</span></span>

#### <a name="step-3"></a><span data-ttu-id="2649a-378">ステップ 3</span><span class="sxs-lookup"><span data-stu-id="2649a-378">Step 3</span></span>

##### <a name="dynamics-ax-2012"></a><span data-ttu-id="2649a-379">Dynamics AX 2012</span><span class="sxs-lookup"><span data-stu-id="2649a-379">Dynamics AX 2012</span></span>

    /* TODO: (Code Upgrade) [Segmented entry control] Fix controller usage, if any, in this method based on the migration guidance */
    public void lookup()
    {
        if (custVendPaymJournalFee.Module == ModuleCustVend::Cust)
        {
            if (custVendPaymJournalFee.LedgerJournalACType == LedgerJournalACType::Cust)
            {
                CustTable::lookupCustomer(this, ledgerJournalTrans.Company);
            }
            else if (custVendPaymJournalFee.LedgerJournalACType == LedgerJournalACType::Ledger)
            {
                super();
            }
        }
        else if (custVendPaymJournalFee.Module == ModuleCustVend::Vend)
        {
            if (custVendPaymJournalFee.LedgerJournalACType == LedgerJournalACType::Vend)
            {
                VendTable::lookupVendor(this, ledgerJournalTrans.Company);
            }
            else if (custVendPaymJournalFee.LedgerJournalACType == LedgerJournalACType::Ledger)
            {
                super();
            }
        }
    }

##### <a name="dynamics-ax-for-operations"></a><span data-ttu-id="2649a-380">Dynamics AX for Operations</span><span class="sxs-lookup"><span data-stu-id="2649a-380">Dynamics AX for Operations</span></span>

<span data-ttu-id="2649a-381">このメソッドは、コントロールのカスタム ルックアップを実装します。</span><span class="sxs-lookup"><span data-stu-id="2649a-381">This method implements a custom lookup for the control.</span></span> <span data-ttu-id="2649a-382">したがって、メソッドをそのままにします。</span><span class="sxs-lookup"><span data-stu-id="2649a-382">Therefore, leave the method as it is.</span></span> <span data-ttu-id="2649a-383">"仕事" を削除します。</span><span class="sxs-lookup"><span data-stu-id="2649a-383">Just remove the TODO.</span></span> <span data-ttu-id="2649a-384">カスタムのルックアップをフック アップするには、SEC の **checkUseCustomLookup** メソッドをオーバーライドする必要があります。</span><span class="sxs-lookup"><span data-stu-id="2649a-384">To hook up custom lookups, you must override the SEC’s **checkUseCustomLookup** method.</span></span> <span data-ttu-id="2649a-385">次に例を示します。</span><span class="sxs-lookup"><span data-stu-id="2649a-385">Here is an example.</span></span>

    public boolean checkUseCustomLookup(int _accountTypeEnumValue, int _secondaryAccountTypeEnumValue)
    {
        boolean ret;
        switch(_accountTypeEnumValue)
        {
            case LedgerJournalACType::Bank:
            case LedgerJournalACType::Cust:
            case LedgerJournalACType::FixedAssets:
            case LedgerJournalACType::Project:
            case LedgerJournalACType::Vend:
                ret = true;
                break;
            default:
                ret = false;
        }
        return ret;
    }

<span data-ttu-id="2649a-386">また、カスタム ルックアップ フォームで **closeSelectRecord** メソッドが上書きされたことを確認してください。</span><span class="sxs-lookup"><span data-stu-id="2649a-386">Additionally, make sure that the **closeSelectRecord** method on the custom lookup form is overridden.</span></span> <span data-ttu-id="2649a-387">例については、**CustTableLookup** フォームを参照してください。</span><span class="sxs-lookup"><span data-stu-id="2649a-387">For an example, see the **CustTableLookup** form.</span></span>

#### <a name="step-4"></a><span data-ttu-id="2649a-388">ステップ 4</span><span class="sxs-lookup"><span data-stu-id="2649a-388">Step 4</span></span>

##### <a name="dynamics-ax-2012"></a><span data-ttu-id="2649a-389">Dynamics AX 2012</span><span class="sxs-lookup"><span data-stu-id="2649a-389">Dynamics AX 2012</span></span>

    /* TODO: (Code Upgrade) [Segmented entry control] For custom implementation, code in this method needs to be moved elsewhere based on the migration guidance */
    public void segmentValueChanged(SegmentValueChangedEventArgs _e)
    {
        super(_e);

        /* TODO: (Code Upgrade) [Segmented entry control] Replace this based on the migration guidance */
        // dimPaymentFeeAccountController.segmentValueChanged(_e);
        currentPaymentFeeMainAccountId = ledgerJournalEngine.onPrimaryAccountSegmentChanged(dimPaymentFeeAccountController, currentPaymentFeeMainAccountId, ledgerJournalTrans);
    }

##### <a name="dynamics-ax-for-operations"></a><span data-ttu-id="2649a-390">Dynamics AX for Operations</span><span class="sxs-lookup"><span data-stu-id="2649a-390">Dynamics AX for Operations</span></span>

1.  <span data-ttu-id="2649a-391">コントロールの **onSegmentChanged()** メソッドをオーバーライドし、次のコードを追加します。</span><span class="sxs-lookup"><span data-stu-id="2649a-391">Override the **onSegmentChanged()** method on the control, and add the following code to it.</span></span>

        /// <summary>
        /// The event handler when a segment is modified.
        /// </summary>
        /// <param name = "_segment">The segment that was modified.</param>
        public void onSegmentChanged(DimensionControlSegment _segment)
        {
            super(_segment);
            currentPaymentFeeMainAccountId = ledgerJournalEngine.onPrimaryAccountSegmentChanged(
            CustPaymJournalFee_CustAccount, currentPaymentFeeMainAccountId, ledgerJournalTrans);
        }

2.  <span data-ttu-id="2649a-392">**segmentValueChanged()** メソッドを削除します。</span><span class="sxs-lookup"><span data-stu-id="2649a-392">Delete the **segmentValueChanged()** method.</span></span> <span data-ttu-id="2649a-393">**注記:** **onPrimaryAccountSegmentChanged()** メソッドでは、コントローラー オブジェクトが必要ですが、このコードは SEC のインスタンスを渡すので、**onSegmentChanged()** メソッドの前のコードはコンパイルされません。</span><span class="sxs-lookup"><span data-stu-id="2649a-393">**Note:** The preceding code for the **onSegmentChanged()** method will not compile, because the **onPrimaryAccountSegmentChanged()** method expects a controller object, but this code passes an instance of the SEC.</span></span> <span data-ttu-id="2649a-394">コントロール インスタンスでメソッドを呼び出すには、メソッドのシグネチャとその実装を適宜変更する必要があります。</span><span class="sxs-lookup"><span data-stu-id="2649a-394">To call methods on the control instance, you must change the method’s signature and its implementation accordingly.</span></span> <span data-ttu-id="2649a-395">このメソッドは、50 以上の呼び出し元が使用されます。</span><span class="sxs-lookup"><span data-stu-id="2649a-395">This method is used by more than 50 callers.</span></span> <span data-ttu-id="2649a-396">したがって、これらの呼び出しをすべて更新する必要があります。</span><span class="sxs-lookup"><span data-stu-id="2649a-396">Therefore, you would also have to update all those calls.</span></span> <span data-ttu-id="2649a-397">または、このガイダンスの指示に従うことによって新しいメソッドを追加することができます。</span><span class="sxs-lookup"><span data-stu-id="2649a-397">Alternatively, you can add a new method that can follow this guidance.</span></span>

#### <a name="step-5"></a><span data-ttu-id="2649a-398">ステップ 5</span><span class="sxs-lookup"><span data-stu-id="2649a-398">Step 5</span></span>

##### <a name="dynamics-ax-2012"></a><span data-ttu-id="2649a-399">Dynamics AX 2012</span><span class="sxs-lookup"><span data-stu-id="2649a-399">Dynamics AX 2012</span></span>

    /* TODO: (Code Upgrade) [Segmented entry control] This method can be removed if there is no custom implementation */
    public boolean validate()
    {
        boolean isValid;
        isValid = super();

        /* TODO: (Code Upgrade) [Segmented entry control] This statement can be removed if there is no custom logic */
        // isValid = dimPaymentFeeAccountController.validate() && isValid;
        return isValid;
    }

##### <a name="dynamics-ax-for-operations"></a><span data-ttu-id="2649a-400">Dynamics AX for Operations</span><span class="sxs-lookup"><span data-stu-id="2649a-400">Dynamics AX for Operations</span></span>

<span data-ttu-id="2649a-401">このメソッドはコントロールの **validate()** メソッドのみを呼び出し追加の処理は実行しないため、削除できます。</span><span class="sxs-lookup"><span data-stu-id="2649a-401">Because this method only calls the **validate()** method on the control and doesn't perform any additional processing, you can delete it.</span></span>

### <a name="group4_accountnum"></a><span data-ttu-id="2649a-402">Group4\_AccountNum</span><span class="sxs-lookup"><span data-stu-id="2649a-402">Group4\_AccountNum</span></span>

<span data-ttu-id="2649a-403">(**フォーム**タブの下にある検索バーで「Group4\_AccountNum」を検索してください。)</span><span class="sxs-lookup"><span data-stu-id="2649a-403">(Search for "Group4\_AccountNum" in the search bar below the **Form** tab.)</span></span>

#### <a name="step-1"></a><span data-ttu-id="2649a-404">ステップ１</span><span class="sxs-lookup"><span data-stu-id="2649a-404">Step 1</span></span>

##### <a name="dynamics-ax-2012"></a><span data-ttu-id="2649a-405">Dynamics AX 2012</span><span class="sxs-lookup"><span data-stu-id="2649a-405">Dynamics AX 2012</span></span>

    /* TODO: (Code Upgrade) [Segmented entry control] This method can be removed if there is no custom implementation */
    public void jumpRef()
    {
        LedgerJournalTrans_AccountNum.jumpRef();
        LedgerJournalTrans_AccountNum1.jumpRef();
        Group4_AccountNum.jumpRef();
    }

##### <a name="dynamics-ax-for-operations"></a><span data-ttu-id="2649a-406">Dynamics AX for Operations</span><span class="sxs-lookup"><span data-stu-id="2649a-406">Dynamics AX for Operations</span></span>

<span data-ttu-id="2649a-407">このメソッドはコントロールの **jumpRef()** メソッドのみを呼び出し追加の処理は実行しないため、削除できます。</span><span class="sxs-lookup"><span data-stu-id="2649a-407">Because this method only calls the **jumpRef()** method on the control and doesn't perform any additional processing, you can delete it.</span></span>

#### <a name="step-2"></a><span data-ttu-id="2649a-408">ステップ２</span><span class="sxs-lookup"><span data-stu-id="2649a-408">Step 2</span></span>

##### <a name="dynamics-ax-2012"></a><span data-ttu-id="2649a-409">Dynamics AX 2012</span><span class="sxs-lookup"><span data-stu-id="2649a-409">Dynamics AX 2012</span></span>

    /* TODO: (Code Upgrade) [Segmented entry control] For custom implementation, code in this method needs to be moved elsewhere based on the migration guidance */
    public void loadSegments()
    {
        super();
        LedgerJournalTrans_AccountNum.parmJournalName(ledgerJournalTable.JournalName);
        LedgerJournalTrans_AccountNum1.parmJournalName(ledgerJournalTable.JournalName);
        Group4_AccountNum.parmJournalName(ledgerJournalTable.JournalName);
        LedgerJournalTrans_AccountNum.parmCurrency(ledgerJournalTrans.CurrencyCode);
        LedgerJournalTrans_AccountNum1.parmCurrency(ledgerJournalTrans.CurrencyCode);
        Group4_AccountNum.parmCurrency(ledgerJournalTrans.CurrencyCode);
        LedgerJournalTrans_AccountNum.parmDataAreaId(ledgerJournalTrans.Company ? ledgerJournalTrans.Company : curext());
        LedgerJournalTrans_AccountNum1.parmDataAreaId(ledgerJournalTrans.Company ? ledgerJournalTrans.Company : curext());
        Group4_AccountNum.parmDataAreaId(ledgerJournalTrans.Company ? ledgerJournalTrans.Company : curext());
        LedgerJournalTrans_AccountNum.parmControlDate(ledgerJournalTrans.TransDate);
        LedgerJournalTrans_AccountNum1.parmControlDate(ledgerJournalTrans.TransDate);
        Group4_AccountNum.parmControlDate(ledgerJournalTrans.TransDate);

        /* TODO: (Code Upgrade) [Segmented entry control] Replace this based on the migration guidance */
        // dimAccountController.loadSegments();
        currentMainAccountId = dimAccountController.getValue(DimensionAttribute::getWellKnownDimensionAttribute(DimensionAttributeType::MainAccount));
    }

##### <a name="dynamics-ax-for-operations"></a><span data-ttu-id="2649a-410">Dynamics AX for Operations</span><span class="sxs-lookup"><span data-stu-id="2649a-410">Dynamics AX for Operations</span></span>

<span data-ttu-id="2649a-411">このメソッドを移行する手順は、**LedgerJournalTrans\_AccountNum.loadSegments()** メソッドを移行する手順と同じです。</span><span class="sxs-lookup"><span data-stu-id="2649a-411">The steps for migrating this method are the same as the steps for migrating the **LedgerJournalTrans\_AccountNum.loadSegments()** method.</span></span> <span data-ttu-id="2649a-412">したがって、追加の手順は必要はありません。</span><span class="sxs-lookup"><span data-stu-id="2649a-412">Therefore, no additional steps are required.</span></span> <span data-ttu-id="2649a-413">このメソッドを削除します。</span><span class="sxs-lookup"><span data-stu-id="2649a-413">Delete this method.</span></span>

#### <a name="step-3"></a><span data-ttu-id="2649a-414">ステップ 3</span><span class="sxs-lookup"><span data-stu-id="2649a-414">Step 3</span></span>

##### <a name="dynamics-ax-2012"></a><span data-ttu-id="2649a-415">Dynamics AX 2012</span><span class="sxs-lookup"><span data-stu-id="2649a-415">Dynamics AX 2012</span></span>

    /* TODO: (Code Upgrade) [Segmented entry control] Fix controller usage, if any, in this method based on the migration guidance */
    public void lookup()
    {
        if (!ledgerJournalEngine.accountNumLookup(group4_AccountNum, ledgerJournalTrans))
        {
            super();
        }
    }

##### <a name="dynamics-ax-for-operations"></a><span data-ttu-id="2649a-416">Dynamics AX for Operations</span><span class="sxs-lookup"><span data-stu-id="2649a-416">Dynamics AX for Operations</span></span>

<span data-ttu-id="2649a-417">このメソッドは、コントロールのカスタム ルックアップを実装します。</span><span class="sxs-lookup"><span data-stu-id="2649a-417">This method implements a custom lookup for the control.</span></span> <span data-ttu-id="2649a-418">したがって、メソッドをそのままにします。</span><span class="sxs-lookup"><span data-stu-id="2649a-418">Therefore, leave the method as it is.</span></span> <span data-ttu-id="2649a-419">"仕事" を削除します。</span><span class="sxs-lookup"><span data-stu-id="2649a-419">Just remove the TODO.</span></span> <span data-ttu-id="2649a-420">カスタムのルックアップをフック アップするには、SEC の **checkUseCustomLookup** メソッドをオーバーライドする必要があります。</span><span class="sxs-lookup"><span data-stu-id="2649a-420">To hook up custom lookups, you must override the SEC’s **checkUseCustomLookup** method.</span></span> <span data-ttu-id="2649a-421">また、カスタム ルックアップ フォームで **closeSelectRecord** メソッドが上書きされたことを確認してください。</span><span class="sxs-lookup"><span data-stu-id="2649a-421">Additionally, make sure that the **closeSelectRecord** method on the custom lookup form is overridden.</span></span> <span data-ttu-id="2649a-422">例については、**CustTableLookup** フォームを参照してください。</span><span class="sxs-lookup"><span data-stu-id="2649a-422">For an example, see the **CustTableLookup** form.</span></span>

#### <a name="step-4"></a><span data-ttu-id="2649a-423">ステップ 4</span><span class="sxs-lookup"><span data-stu-id="2649a-423">Step 4</span></span>

##### <a name="dynamics-ax-2012"></a><span data-ttu-id="2649a-424">Dynamics AX 2012</span><span class="sxs-lookup"><span data-stu-id="2649a-424">Dynamics AX 2012</span></span>

    /* TODO: (Code Upgrade) [Segmented entry control] For custom implementation, code in this method needs to be moved elsewhere based on the migration guidance */
    public void segmentValueChanged(SegmentValueChangedEventArgs _e)
    {
        super(_e);

        /* TODO: (Code Upgrade) [Segmented entry control] Replace this based on the migration guidance */
        // dimAccountController.segmentValueChanged(_e);
        currentMainAccountId = ledgerJournalEngine.onPrimaryAccountSegmentChanged(dimAccountController, currentMainAccountId, ledgerJournalTrans);
    }

##### <a name="dynamics-ax-for-operations"></a><span data-ttu-id="2649a-425">Dynamics AX for Operations</span><span class="sxs-lookup"><span data-stu-id="2649a-425">Dynamics AX for Operations</span></span>

1.  <span data-ttu-id="2649a-426">コントロールの **onSegmentChanged()** メソッドをオーバーライドし、次のコードを追加します。</span><span class="sxs-lookup"><span data-stu-id="2649a-426">Override the **onSegmentChanged()** method on the control, and add the following code to it.</span></span>

        /// <summary>
        /// The event handler for the segment change event.
        /// </summary>
        /// <param name = "_segment">The segment that was modified.</param>
        public void onSegmentChanged(DimensionControlSegment _segment)
        {
            super(_segment);
            if (_segment.parmName() == mainAccountDimAttrName)
            {
                previousMainAccountId = currentMainAccountId;
            }
            currentMainAccountId = ledgerJournalEngine.onPrimaryAccountSegmentChanged(Group4_AccountNum, currentMainAccountId, ledgerJournalTrans);
        }

2.  <span data-ttu-id="2649a-427">**segmentValueChanged()** メソッドを削除します。</span><span class="sxs-lookup"><span data-stu-id="2649a-427">Delete the **segmentValueChanged()** method.</span></span> <span data-ttu-id="2649a-428">**注記:** **onPrimaryAccountSegmentChanged()** メソッドでは、コントローラー オブジェクトが必要ですが、このコードは SEC のインスタンスを渡すので、**onSegmentChanged()** メソッドの前のコードはコンパイルされません。</span><span class="sxs-lookup"><span data-stu-id="2649a-428">**Note:** The preceding code for the **onSegmentChanged()** method will not compile, because the **onPrimaryAccountSegmentChanged()** method expects a controller object, but this code passes an instance of the SEC.</span></span> <span data-ttu-id="2649a-429">コントロール インスタンスでメソッドを呼び出すには、メソッドのシグネチャとその実装を適宜変更する必要があります。</span><span class="sxs-lookup"><span data-stu-id="2649a-429">To call methods on the control instance, you must change the method’s signature and its implementation accordingly.</span></span> <span data-ttu-id="2649a-430">このメソッドは、50 以上の呼び出し元が使用されます。</span><span class="sxs-lookup"><span data-stu-id="2649a-430">This method is used by more than 50 callers.</span></span> <span data-ttu-id="2649a-431">したがって、これらの呼び出しをすべて更新する必要があります。</span><span class="sxs-lookup"><span data-stu-id="2649a-431">Therefore, you would also have to update all those calls.</span></span> <span data-ttu-id="2649a-432">または、このガイダンスに従うことによって新しいメソッドを追加できます。</span><span class="sxs-lookup"><span data-stu-id="2649a-432">Alternatively, you can add a new method that follows this guidance.</span></span>

#### <a name="step-5"></a><span data-ttu-id="2649a-433">ステップ 5</span><span class="sxs-lookup"><span data-stu-id="2649a-433">Step 5</span></span>

##### <a name="dynamics-ax-2012"></a><span data-ttu-id="2649a-434">Dynamics AX 2012</span><span class="sxs-lookup"><span data-stu-id="2649a-434">Dynamics AX 2012</span></span>

    /* TODO: (Code Upgrade) [Segmented entry control] This method can be removed if there is no custom implementation */
    public boolean validate()
    {
        boolean isValid;
        isValid = super();

        /* TODO: (Code Upgrade) [Segmented entry control] This statement can be removed if there is no custom logic */
        // isValid = dimAccountController.validate() && isValid;
        return isValid;
    }

##### <a name="dynamics-ax-for-operations"></a><span data-ttu-id="2649a-435">Dynamics AX for Operations</span><span class="sxs-lookup"><span data-stu-id="2649a-435">Dynamics AX for Operations</span></span>

<span data-ttu-id="2649a-436">このメソッドはコントロールの **validate()** メソッドのみを呼び出し追加の処理は実行しないため、削除できます。</span><span class="sxs-lookup"><span data-stu-id="2649a-436">Because this method only calls the **validate()** method on the control and doesn't perform any additional processing, you can delete it.</span></span>

### <a name="group4_offsetaccount"></a><span data-ttu-id="2649a-437">Group4\_OffsetAccount</span><span class="sxs-lookup"><span data-stu-id="2649a-437">Group4\_OffsetAccount</span></span>

<span data-ttu-id="2649a-438">(**フォーム**タブの下にある検索バーで「Group4\_OffsetAccount」を検索してください。)</span><span class="sxs-lookup"><span data-stu-id="2649a-438">(Search for "Group4\_OffsetAccount" in the search bar below the **Form** tab.)</span></span>

#### <a name="step-1"></a><span data-ttu-id="2649a-439">ステップ１</span><span class="sxs-lookup"><span data-stu-id="2649a-439">Step 1</span></span>

##### <a name="dynamics-ax-2012"></a><span data-ttu-id="2649a-440">Dynamics AX 2012</span><span class="sxs-lookup"><span data-stu-id="2649a-440">Dynamics AX 2012</span></span>

    /* TODO: (Code Upgrade) [Segmented entry control] For custom implementation, code in this method needs to be moved elsewhere based on the migration guidance */
    void gotFocus()
    {
        super();
        if (ledgerJournalTable.FixedOffsetAccount)
        {
            group4_OffsetAccount.allowEdit(ledgerJournalTrans.OffsetAccountType == LedgerJournalACType::Ledger);
        }
        else if (!group4_OffsetAccount.allowEdit())
        {
            group4_OffsetAccount.allowEdit(true);
        }
    }

##### <a name="dynamics-ax-for-operations"></a><span data-ttu-id="2649a-441">Dynamics AX for Operations</span><span class="sxs-lookup"><span data-stu-id="2649a-441">Dynamics AX for Operations</span></span>

1.  <span data-ttu-id="2649a-442">ledgerJournalTable バッファを更新するコードの後に、**initLedger()** メソッドのコードを更新します。</span><span class="sxs-lookup"><span data-stu-id="2649a-442">Update the code in the **initLedger()** method, after the code that updates the ledgerJournalTable buffer.</span></span>

        . . .
        if (ledgerJournalTable.FixedOffsetAccount)
        {
            gridOffsetAccount.allowEdit(ledgerJournalTrans.OffsetAccountType == LedgerJournalACType::Ledger); group4_OffsetAccount.allowEdit(ledgerJournalTrans.OffsetAccountType == LedgerJournalACType::Ledger);
        }
        else if (!gridOffsetAccount.allowEdit())
        {
            gridOffsetAccount.allowEdit(true);
            group4_OffsetAccount.allowEdit(true);
        }
        . . .

2.  <span data-ttu-id="2649a-443">**gotFocus()** メソッドを削除します。</span><span class="sxs-lookup"><span data-stu-id="2649a-443">Delete the **gotFocus()** method.</span></span>

#### <a name="step-2"></a><span data-ttu-id="2649a-444">ステップ２</span><span class="sxs-lookup"><span data-stu-id="2649a-444">Step 2</span></span>

##### <a name="dynamics-ax-2012"></a><span data-ttu-id="2649a-445">Dynamics AX 2012</span><span class="sxs-lookup"><span data-stu-id="2649a-445">Dynamics AX 2012</span></span>

    /* TODO: (Code Upgrade) [Segmented entry control] This method can be removed if there is no custom implementation */
    public void jumpRef()
    {
        GridOffsetAccount.jumpRef();
        LedgerJournalTrans_OffsetAccount1.jumpRef();
        Group4_OffsetAccount.jumpRef();
    }

##### <a name="dynamics-ax-for-operations"></a><span data-ttu-id="2649a-446">Dynamics AX for Operations</span><span class="sxs-lookup"><span data-stu-id="2649a-446">Dynamics AX for Operations</span></span>

<span data-ttu-id="2649a-447">このメソッドはコントロールの **jumpRef()** メソッドのみを呼び出し追加の処理は実行しないため、削除できます。</span><span class="sxs-lookup"><span data-stu-id="2649a-447">Because this method only calls the **jumpRef()** method on the control and doesn't perform any additional processing, you can delete it.</span></span>

#### <a name="step-3"></a><span data-ttu-id="2649a-448">ステップ 3</span><span class="sxs-lookup"><span data-stu-id="2649a-448">Step 3</span></span>

##### <a name="dynamics-ax-2012"></a><span data-ttu-id="2649a-449">Dynamics AX 2012</span><span class="sxs-lookup"><span data-stu-id="2649a-449">Dynamics AX 2012</span></span>

    /* TODO: (Code Upgrade) [Segmented entry control] For custom implementation, code in this method needs to be moved elsewhere based on the migration guidance */
    public void loadSegments()
    {
        super();
        GridOffsetAccount.parmJournalName(ledgerJournalTable.JournalName);
        LedgerJournalTrans_OffsetAccount1.parmJournalName(ledgerJournalTable.JournalName);
        Group4_OffsetAccount.parmJournalName(ledgerJournalTable.JournalName);
        GridOffsetAccount.parmCurrency(ledgerJournalTrans.CurrencyCode);
        LedgerJournalTrans_OffsetAccount1.parmCurrency(ledgerJournalTrans.CurrencyCode);
        Group4_OffsetAccount.parmCurrency(ledgerJournalTrans.CurrencyCode);
        GridOffsetAccount.parmDataAreaId(ledgerJournalTrans.getOffsetCompany());
        LedgerJournalTrans_OffsetAccount1.parmDataAreaId(ledgerJournalTrans.getOffsetCompany());
        Group4_OffsetAccount.parmDataAreaId(ledgerJournalTrans.getOffsetCompany());
        GridOffsetAccount.parmControlDate(ledgerJournalTrans.TransDate);
        LedgerJournalTrans_OffsetAccount1.parmControlDate(ledgerJournalTrans.TransDate);
        Group4_OffsetAccount.parmControlDate(ledgerJournalTrans.TransDate);

        /* TODO: (Code Upgrade) [Segmented entry control] Replace this based on the migration guidance */
        // dimOffsetAccountController.loadSegments();
        currentOffsetMainAccountId = dimOffsetAccountController.getValue(DimensionAttribute::getWellKnownDimensionAttribute(DimensionAttributeType::MainAccount));

        // Lock the main account segment if "Fixed offset account" is selected in Journal Names
        if (ledgerJournalTrans.OffsetAccountType == LedgerJournalACType::Ledger)
        {
            GridOffsetAccount.parmLockMainAccountSegment(ledgerJournalTable.FixedOffsetAccount);
            LedgerJournalTrans_OffsetAccount1.parmLockMainAccountSegment(ledgerJournalTable.FixedOffsetAccount);
            Group4_OffsetAccount.parmLockMainAccountSegment(ledgerJournalTable.FixedOffsetAccount);
        }
    }

##### <a name="dynamics-ax-for-operations"></a><span data-ttu-id="2649a-450">Dynamics AX for Operations</span><span class="sxs-lookup"><span data-stu-id="2649a-450">Dynamics AX for Operations</span></span>

<span data-ttu-id="2649a-451">**GridOffsetAccount.loadSegments()** メソッドの移行手順は、すでにこのメソッドに必要な変更のほとんどを行いました。</span><span class="sxs-lookup"><span data-stu-id="2649a-451">The migration steps for the **GridOffsetAccount.loadSegments()** method already made most of the changes that are required for this method.</span></span> <span data-ttu-id="2649a-452">ただし、次の変更を加える必要があります。</span><span class="sxs-lookup"><span data-stu-id="2649a-452">However, you must still make the following changes.</span></span>

1.  <span data-ttu-id="2649a-453">**LedgerJournalTrans** データ ソースの **active** メソッドでコードを更新します。</span><span class="sxs-lookup"><span data-stu-id="2649a-453">Update the code in the **LedgerJournalTrans** data source’s **active** method.</span></span>

        if (ledgerJournalTrans.OffsetAccountType == LedgerJournalACType::Ledger)
        {
            currentOffsetMainAccountId = GridOffsetAccount.getValue(DimensionAttribute::getWellKnownDimensionAttribute(DimensionAttributeType::MainAccount));
        }
        else
        {
            currentOffsetMainAccountId = 0;
        }

        // Lock the main account segment if "Fixed offset account" is selected in Journal Names
        if (ledgerJournalTrans.OffsetAccountType == LedgerJournalACType::Ledger)
        {
            GridOffsetAccount.parmLockMainAccountSegment(ledgerJournalTable.FixedOffsetAccount);
            LedgerJournalTrans_OffsetAccount1.parmLockMainAccountSegment(ledgerJournalTable.FixedOffsetAccount);
            Group4_OffsetAccount.parmLockMainAccountSegment(ledgerJournalTable.FixedOffsetAccount);
        }

2.  <span data-ttu-id="2649a-454">**LedgerJournalTrans** データ ソースの **OffsetAccountType** フィールドの **modified()** メソッドで同じ変更を行います。</span><span class="sxs-lookup"><span data-stu-id="2649a-454">Make the same change in the **modified()** method of the **LedgerJournalTrans** data source’s **OffsetAccountType** field.</span></span>

        if (ledgerJournalTrans.OffsetAccountType == LedgerJournalACType::Ledger)
        {
            currentOffsetMainAccountId = GridOffsetAccount.getValue(DimensionAttribute::getWellKnownDimensionAttribute(DimensionAttributeType::MainAccount));
        }
        else
        {
            currentOffsetMainAccountId = 0;
        }
        // Lock the main account segment if "Fixed offset account" is selected in Journal Names
        if (ledgerJournalTrans.OffsetAccountType == LedgerJournalACType::Ledger)
        {
            GridOffsetAccount.parmLockMainAccountSegment(ledgerJournalTable.FixedOffsetAccount);
            LedgerJournalTrans_OffsetAccount1.parmLockMainAccountSegment(ledgerJournalTable.FixedOffsetAccount);
            Group4_OffsetAccount.parmLockMainAccountSegment(ledgerJournalTable.FixedOffsetAccount);
        }

3.  <span data-ttu-id="2649a-455">**initLedger()** メソッドで同じ変更を行います。</span><span class="sxs-lookup"><span data-stu-id="2649a-455">Make the same change in the **initLedger()** method.</span></span>

        if (ledgerJournalTrans.OffsetAccountType == LedgerJournalACType::Ledger)
        {
            currentOffsetMainAccountId = GridOffsetAccount.getValue(DimensionAttribute::getWellKnownDimensionAttribute(DimensionAttributeType::MainAccount));
        }
        else
        {
            currentOffsetMainAccountId = 0;
        }
        // Lock the main account segment if "Fixed offset account" is selected in Journal Names
        if (ledgerJournalTrans.OffsetAccountType == LedgerJournalACType::Ledger)
        {
            GridOffsetAccount.parmLockMainAccountSegment(ledgerJournalTable.FixedOffsetAccount);
            LedgerJournalTrans_OffsetAccount1.parmLockMainAccountSegment(ledgerJournalTable.FixedOffsetAccount);
            Group4_OffsetAccount.parmLockMainAccountSegment(ledgerJournalTable.FixedOffsetAccount);
        }

4.  <span data-ttu-id="2649a-456">**loadSegments()** メソッドを削除します。</span><span class="sxs-lookup"><span data-stu-id="2649a-456">Delete the **loadSegments()** method.</span></span>

#### <a name="step-4"></a><span data-ttu-id="2649a-457">ステップ 4</span><span class="sxs-lookup"><span data-stu-id="2649a-457">Step 4</span></span>

##### <a name="dynamics-ax-2012"></a><span data-ttu-id="2649a-458">Dynamics AX 2012</span><span class="sxs-lookup"><span data-stu-id="2649a-458">Dynamics AX 2012</span></span>

    /* TODO: (Code Upgrade) [Segmented entry control] Fix controller usage, if any, in this method based on the migration guidance */
    public void lookup()
    {
        if (!ledgerJournalEngine.offsetAccountNumLookUp(group4_OffsetAccount, ledgerJournalTrans))
        {
            super();
        }
    }

##### <a name="dynamics-ax-for-operations"></a><span data-ttu-id="2649a-459">Dynamics AX for Operations</span><span class="sxs-lookup"><span data-stu-id="2649a-459">Dynamics AX for Operations</span></span>

<span data-ttu-id="2649a-460">このメソッドは、コントロールのカスタム ルックアップを実装します。</span><span class="sxs-lookup"><span data-stu-id="2649a-460">This method implements a custom lookup for the control.</span></span> <span data-ttu-id="2649a-461">したがって、メソッドをそのままにします。</span><span class="sxs-lookup"><span data-stu-id="2649a-461">Therefore, leave the method as it is.</span></span> <span data-ttu-id="2649a-462">"仕事" を削除します。</span><span class="sxs-lookup"><span data-stu-id="2649a-462">Just remove the TODO.</span></span> <span data-ttu-id="2649a-463">カスタムのルックアップをフック アップするには、SEC の **checkUseCustomLookup** メソッドをオーバーライドする必要があります。</span><span class="sxs-lookup"><span data-stu-id="2649a-463">To hook up custom lookups, you must override the SEC’s **checkUseCustomLookup** method.</span></span> <span data-ttu-id="2649a-464">また、カスタム ルックアップ フォームで **closeSelectRecord** メソッドが上書きされたことを確認してください。</span><span class="sxs-lookup"><span data-stu-id="2649a-464">Additionally, make sure that the **closeSelectRecord** method on the custom lookup form is overridden.</span></span> <span data-ttu-id="2649a-465">例については、**CustTableLookup** フォームを参照してください。</span><span class="sxs-lookup"><span data-stu-id="2649a-465">For an example, see the **CustTableLookup** form.</span></span>

#### <a name="step-5"></a><span data-ttu-id="2649a-466">ステップ 5</span><span class="sxs-lookup"><span data-stu-id="2649a-466">Step 5</span></span>

##### <a name="dynamics-ax-2012"></a><span data-ttu-id="2649a-467">Dynamics AX 2012</span><span class="sxs-lookup"><span data-stu-id="2649a-467">Dynamics AX 2012</span></span>

    /* TODO: (Code Upgrade) [Segmented entry control] For custom implementation, code in this method needs to be moved elsewhere based on the migration guidance */
    public void segmentValueChanged(SegmentValueChangedEventArgs _e)
    {
        super(_e);

        /* TODO: (Code Upgrade) [Segmented entry control] Replace this based on the migration guidance */
        // dimOffsetAccountController.segmentValueChanged(_e);
        currentOffsetMainAccountId = ledgerJournalEngine.onOffsetAccountSegmentChanged(dimOffsetAccountController, currentOffsetMainAccountId, ledgerJournalTrans);
    }

##### <a name="dynamics-ax-for-operations"></a><span data-ttu-id="2649a-468">Dynamics AX for Operations</span><span class="sxs-lookup"><span data-stu-id="2649a-468">Dynamics AX for Operations</span></span>

1.  <span data-ttu-id="2649a-469">コントロールの **onSegmentChanged()** メソッドをオーバーライドし、次のコードを追加します。</span><span class="sxs-lookup"><span data-stu-id="2649a-469">Override the **onSegmentChanged()** method on the control, and add the following code to it.</span></span>

        /// <summary>
        /// The event handler for the segment change event.
        /// </summary>
        /// <param name = "_segment">The segment that was modified.</param>
        public void onSegmentChanged(DimensionControlSegment _segment)
        {
            super(_segment);
            currentOffsetMainAccountId = ledgerJournalEngine.onOffsetAccountSegmentChanged(
            Group4_OffsetAccount, currentOffsetMainAccountId, ledgerJournalTrans);
        }

2.  <span data-ttu-id="2649a-470">**segmentValueChanged()** メソッドを削除します。</span><span class="sxs-lookup"><span data-stu-id="2649a-470">Delete the **segmentValueChanged()** method.</span></span> <span data-ttu-id="2649a-471">**注記:** **onOffsetAccountSegmentChanged()** メソッドでは、コントローラー オブジェクトが必要ですが、このコードは SEC のインスタンスを渡すので、**onSegmentChanged()** メソッドの前のコードはコンパイルされません。</span><span class="sxs-lookup"><span data-stu-id="2649a-471">**Note:** The preceding code for the **onSegmentChanged()** method will not compile, because the **onOffsetAccountSegmentChanged()** method expects a controller object, but this code passes an instance of the SEC.</span></span> <span data-ttu-id="2649a-472">コントロール インスタンスでメソッドを呼び出すには、メソッドのシグネチャとその実装を適宜変更する必要があります。</span><span class="sxs-lookup"><span data-stu-id="2649a-472">To call methods on the control instance, you must change the method’s signature and its implementation accordingly.</span></span> <span data-ttu-id="2649a-473">このメソッドは、50 以上の呼び出し元が使用されます。</span><span class="sxs-lookup"><span data-stu-id="2649a-473">This method is used by more than 50 callers.</span></span> <span data-ttu-id="2649a-474">したがって、これらの呼び出しをすべて更新する必要があります。</span><span class="sxs-lookup"><span data-stu-id="2649a-474">Therefore, you would also have to update all those calls.</span></span> <span data-ttu-id="2649a-475">または、このガイダンスに従うことによって新しいメソッドを追加できます。</span><span class="sxs-lookup"><span data-stu-id="2649a-475">Alternatively, you can add a new method that follows this guidance.</span></span>

#### <a name="step-6"></a><span data-ttu-id="2649a-476">ステップ 6</span><span class="sxs-lookup"><span data-stu-id="2649a-476">Step 6</span></span>

##### <a name="dynamics-ax-2012"></a><span data-ttu-id="2649a-477">Dynamics AX 2012</span><span class="sxs-lookup"><span data-stu-id="2649a-477">Dynamics AX 2012</span></span>

    /* TODO: (Code Upgrade) [Segmented entry control] This method can be removed if there is no custom implementation */
    public boolean validate()
    {
        boolean isValid;
        isValid = super();

        /* TODO: (Code Upgrade) [Segmented entry control] This statement can be removed if there is no custom logic */
        // isValid = dimOffsetAccountController.validate() && isValid;
        return isValid;
    }

##### <a name="dynamics-ax-for-operations"></a><span data-ttu-id="2649a-478">Dynamics AX for Operations</span><span class="sxs-lookup"><span data-stu-id="2649a-478">Dynamics AX for Operations</span></span>

<span data-ttu-id="2649a-479">このメソッドはコントロールの **validate()** メソッドのみを呼び出し追加の処理は実行しないため、削除できます。</span><span class="sxs-lookup"><span data-stu-id="2649a-479">Because this method only calls the **validate()** method on the control and doesn't perform any additional processing, you can delete it.</span></span>

<a name="additional-resources"></a><span data-ttu-id="2649a-480">追加リソース</span><span class="sxs-lookup"><span data-stu-id="2649a-480">Additional resources</span></span>
--------

[<span data-ttu-id="2649a-481">ダイアログのセグメント化されたエントリ コントロールのサポート</span><span class="sxs-lookup"><span data-stu-id="2649a-481">Support for Segmented Entry controls on dialogs</span></span>](segmented-entry-control-dialog-support.md)

[<span data-ttu-id="2649a-482">セグメント化されたエントリ コントロールのデザイン時メタデータ</span><span class="sxs-lookup"><span data-stu-id="2649a-482">Design-time metadata for Segmented Entry controls</span></span>](segmented-entry-control-metadata-specification.md)

[<span data-ttu-id="2649a-483">セグメント化されたエントリ コントロールの Parm メソッド</span><span class="sxs-lookup"><span data-stu-id="2649a-483">Parm methods for Segmented Entry controls</span></span>](segmented-entry-control-parm-method-specification.md)

[<span data-ttu-id="2649a-484">セグメント化されたエントリ コントロールに関する移行ガイダンス</span><span class="sxs-lookup"><span data-stu-id="2649a-484">Migration guidance for Segmented Entry controls</span></span>](segmented-entry-control-migration-guidance.md)



