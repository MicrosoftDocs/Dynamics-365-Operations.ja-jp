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
ms.openlocfilehash: 8938dd257aeb8b72f90ec15a435bb56ae5db876a
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/27/2019
ms.locfileid: "2183303"
---
# <a name="migrate-segmented-entry-controls"></a><span data-ttu-id="c25f6-103">セグメント化されたエントリ コントロールの移行</span><span class="sxs-lookup"><span data-stu-id="c25f6-103">Migrate Segmented Entry controls</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="c25f6-104">このチュートリアルでは、簡単なシナリオ (SMAServiceOrderTable フォームの場合) と複雑なシナリオ (LedgerJournalTransDaily フォームの場合) の 2 つのセグメント化エントリ管理の移行シナリオについて説明します。</span><span class="sxs-lookup"><span data-stu-id="c25f6-104">This tutorial walks you through two migration scenarios for the Segmented Entry control -  a simple scenario (for the SMAServiceOrderTable form) and a complex scenario (for the LedgerJournalTransDaily form).</span></span>

<a name="simple-migration-scenario--smaserviceordertable-form"></a><span data-ttu-id="c25f6-105">簡易移行シナリオ - SMAServiceOrderTable フォーム</span><span class="sxs-lookup"><span data-stu-id="c25f6-105">Simple migration scenario – SMAServiceOrderTable form</span></span>
-----------------------------------------------------

1.  <span data-ttu-id="c25f6-106">アプリケーション エクスプローラーで **SMAServiceOrderTable** フォームを検索します。</span><span class="sxs-lookup"><span data-stu-id="c25f6-106">Search for the **SMAServiceOrderTable** form in Application Explorer.</span></span>
2.  <span data-ttu-id="c25f6-107">現在のプロジェクトにフォームを追加します。</span><span class="sxs-lookup"><span data-stu-id="c25f6-107">Add the form to the current project.</span></span>
3.  <span data-ttu-id="c25f6-108">フォーム デザイン ビューとコード エディタ ビューで、フォームを開きます。</span><span class="sxs-lookup"><span data-stu-id="c25f6-108">Open the form in the form design view and the code editor view.</span></span>
4.  <span data-ttu-id="c25f6-109">フォーム デザイン ビューで、手動でコントロール ツリーを移動するか、**ファイル** タブの下にある検索バーで「SegmentedEntry」を検索して、セグメント化されたエントリ コントロール (SEC) を見つけます。</span><span class="sxs-lookup"><span data-stu-id="c25f6-109">In the form design view, find the Segmented Entry control (SEC), either by manually walking the control tree or by searching for “SegmentedEntry” in the search bar below the **File** tab.</span></span>
5.  <span data-ttu-id="c25f6-110">SEC を選択し、次の情報を確認します。</span><span class="sxs-lookup"><span data-stu-id="c25f6-110">Select the SEC, and verify the following information:</span></span>
    -   <span data-ttu-id="c25f6-111">コントロールの横にある括弧で指定されたコントロールのタイプは、**SegmentedEntryControl** です。</span><span class="sxs-lookup"><span data-stu-id="c25f6-111">The type for the control, as specified in parenthesis next to the control, is **SegmentedEntryControl**.</span></span>
    -   <span data-ttu-id="c25f6-112">**コントローラー クラス** プロパティは **DimensionDynamicAccountController** に設定されます。</span><span class="sxs-lookup"><span data-stu-id="c25f6-112">The **Controller class** property is set to **DimensionDynamicAccountController**.</span></span> <span data-ttu-id="c25f6-113">このプロパティは、SEC のこのインスタンスが使用するコントローラーのタイプを示します。</span><span class="sxs-lookup"><span data-stu-id="c25f6-113">This property indicates the type of controller that this instance of the SEC will use.</span></span> <span data-ttu-id="c25f6-114">コントローラーのタイプによって、コントロールのビヘイビアーが決まります。</span><span class="sxs-lookup"><span data-stu-id="c25f6-114">The type of controller, in turn, determines the behavior of the control.</span></span>

6.  <span data-ttu-id="c25f6-115">コード エディタ ビューに切り替え、フォーム ソース コードで "TODO: (コード アップグレード) \[セグメント化されたエントリ コントロール\]" のすべての事例を検索します。</span><span class="sxs-lookup"><span data-stu-id="c25f6-115">Switch to the code editor view, and search for all occurrences of “TODO: (Code Upgrade) \[Segmented entry control\]” in the form source code.</span></span>
7.  <span data-ttu-id="c25f6-116">検索結果で最初の結果を無視すると、コントローラー変数申告を示します。</span><span class="sxs-lookup"><span data-stu-id="c25f6-116">In the search results, ignore the first result, which points to the controller variable declaration.</span></span> <span data-ttu-id="c25f6-117">制御変数への参照をすべて削除したら、最後に、この作業項目を修正する必要があります。</span><span class="sxs-lookup"><span data-stu-id="c25f6-117">You must fix this TODO last, after you've removed all references to the controller variable.</span></span>
8.  <span data-ttu-id="c25f6-118">次のサブセクションでの説明にあるように、残りの各 TODO コメントが実行されます。</span><span class="sxs-lookup"><span data-stu-id="c25f6-118">Go through each of the remaining TODO comments, as described in the following subsections.</span></span>

### <a name="ledgerdimension-data-field"></a><span data-ttu-id="c25f6-119">LedgerDimension データ フィールド</span><span class="sxs-lookup"><span data-stu-id="c25f6-119">LedgerDimension data field</span></span>

<span data-ttu-id="c25f6-120">(**フォーム**&gt;**データ ソース** &gt;**SMAServiceOrderLine**&gt; **フィールド** &gt;**LedgerDimension**&gt; **方法**)</span><span class="sxs-lookup"><span data-stu-id="c25f6-120">(**Form** &gt; **Data sources** &gt; **SMAServiceOrderLine** &gt; **Fields** &gt; **LedgerDimension** &gt; **Methods**)</span></span>

##### <a name="dynamics-ax-2012"></a><span data-ttu-id="c25f6-121">Dynamics AX 2012</span><span class="sxs-lookup"><span data-stu-id="c25f6-121">Dynamics AX 2012</span></span>

    /* TODO: (Code Upgrade) [Segmented entry control] This method can be removed if there is no custom implementation */
    public void jumpRef()
    {
        ExpenseCost_LedgerDimension.jumpRef();
    }

##### <a name="dynamics-ax-for-operations"></a><span data-ttu-id="c25f6-122">Dynamics AX for Operations</span><span class="sxs-lookup"><span data-stu-id="c25f6-122">Dynamics AX for Operations</span></span>

<span data-ttu-id="c25f6-123">このメソッドはコントロールの **jumpRef()** メソッドのみを呼び出し追加の処理は実行しないため、削除できます。</span><span class="sxs-lookup"><span data-stu-id="c25f6-123">Because this method only calls the **jumpRef()** method on the control and doesn't perform any additional processing, you can delete it.</span></span>

### <a name="expensecost_ledgerdimension-control"></a><span data-ttu-id="c25f6-124">ExpenseCost\_LedgerDimension コントロール</span><span class="sxs-lookup"><span data-stu-id="c25f6-124">ExpenseCost\_LedgerDimension control</span></span>

<span data-ttu-id="c25f6-125">(**フォーム**タブの下にある検索バーで「ExpenseCost\_LedgerDimension」を検索してください。)</span><span class="sxs-lookup"><span data-stu-id="c25f6-125">(Search for "ExpenseCost\_LedgerDimension" in the search bar below the **Form** tab.)</span></span>

#### <a name="step-1"></a><span data-ttu-id="c25f6-126">ステップ１</span><span class="sxs-lookup"><span data-stu-id="c25f6-126">Step 1</span></span>

##### <a name="dynamics-ax-2012"></a><span data-ttu-id="c25f6-127">Dynamics AX 2012</span><span class="sxs-lookup"><span data-stu-id="c25f6-127">Dynamics AX 2012</span></span>

    /* TODO: (Code Upgrade) [Segmented entry control] This method can be removed if there is no custom implementation */
    public void jumpRef()
    {
        ExpenseCost_LedgerDimension.jumpRef();
    }

##### <a name="dynamics-ax-for-operations"></a><span data-ttu-id="c25f6-128">Dynamics AX for Operations</span><span class="sxs-lookup"><span data-stu-id="c25f6-128">Dynamics AX for Operations</span></span>

<span data-ttu-id="c25f6-129">このメソッドはコントロールの **jumpRef()** メソッドのみを呼び出し追加の処理は行わないため、削除できます。</span><span class="sxs-lookup"><span data-stu-id="c25f6-129">Because this method only calls the **jumpRef()** method on the control and doesn't performing any additional processing, you can delete it.</span></span>

#### <a name="step-2"></a><span data-ttu-id="c25f6-130">ステップ２</span><span class="sxs-lookup"><span data-stu-id="c25f6-130">Step 2</span></span>

##### <a name="dynamics-ax-2012"></a><span data-ttu-id="c25f6-131">Dynamics AX 2012</span><span class="sxs-lookup"><span data-stu-id="c25f6-131">Dynamics AX 2012</span></span>

    /* TODO: (Code Upgrade) [Segmented entry control] For custom implementation, code in this method needs to be moved elsewhere based on the migration guidance */
    public void loadSegments()
    {
        super();
        /* TODO: (Code Upgrade) [Segmented entry control] Replace this based on the migration guidance */
        // dimDynamicAccountController.loadSegments();
    }

##### <a name="dynamics-ax-for-operations"></a><span data-ttu-id="c25f6-132">Dynamics AX for Operations</span><span class="sxs-lookup"><span data-stu-id="c25f6-132">Dynamics AX for Operations</span></span>

<span data-ttu-id="c25f6-133">このメソッドはコントロールの **loadSegments()** メソッドのみを呼び出し追加の処理は実行しないため、削除できます。</span><span class="sxs-lookup"><span data-stu-id="c25f6-133">Because this method only calls the **loadSegments()** method on the control and doesn't perform any additional processing, you can delete it.</span></span>

#### <a name="step-3"></a><span data-ttu-id="c25f6-134">ステップ 3</span><span class="sxs-lookup"><span data-stu-id="c25f6-134">Step 3</span></span>

##### <a name="dynamics-ax-2012"></a><span data-ttu-id="c25f6-135">Dynamics AX 2012</span><span class="sxs-lookup"><span data-stu-id="c25f6-135">Dynamics AX 2012</span></span>

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

##### <a name="dynamics-ax-for-operations"></a><span data-ttu-id="c25f6-136">Dynamics AX for Operations</span><span class="sxs-lookup"><span data-stu-id="c25f6-136">Dynamics AX for Operations</span></span>

<span data-ttu-id="c25f6-137">このメソッドは、コントロールのカスタム ルックアップを実装します。</span><span class="sxs-lookup"><span data-stu-id="c25f6-137">This method implements a custom lookup for the control.</span></span> <span data-ttu-id="c25f6-138">したがって、メソッドをそのままにします。</span><span class="sxs-lookup"><span data-stu-id="c25f6-138">Therefore, leave the method as it is.</span></span> <span data-ttu-id="c25f6-139">"仕事" を削除します。</span><span class="sxs-lookup"><span data-stu-id="c25f6-139">Just remove the TODO.</span></span> <span data-ttu-id="c25f6-140">カスタムのルックアップをフック アップするには、SEC の **checkUseCustomLookup** メソッドをオーバーライドする必要があります。</span><span class="sxs-lookup"><span data-stu-id="c25f6-140">To hook up custom lookups, you must override the SEC’s **checkUseCustomLookup** method.</span></span> <span data-ttu-id="c25f6-141">次に例を示します。</span><span class="sxs-lookup"><span data-stu-id="c25f6-141">Here is an example.</span></span>

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

<span data-ttu-id="c25f6-142">また、カスタム ルックアップ フォームで **closeSelectRecord** メソッドが上書きされたことを確認してください。</span><span class="sxs-lookup"><span data-stu-id="c25f6-142">Additionally, make sure that the **closeSelectRecord** method on the custom lookup form is overridden.</span></span> <span data-ttu-id="c25f6-143">例については、**CustTableLookup** フォームを参照してください。</span><span class="sxs-lookup"><span data-stu-id="c25f6-143">For an example, see the **CustTableLookup** form.</span></span>

#### <a name="step-4"></a><span data-ttu-id="c25f6-144">ステップ 4</span><span class="sxs-lookup"><span data-stu-id="c25f6-144">Step 4</span></span>

##### <a name="dynamics-ax-2012"></a><span data-ttu-id="c25f6-145">Dynamics AX 2012</span><span class="sxs-lookup"><span data-stu-id="c25f6-145">Dynamics AX 2012</span></span>

    /* TODO: (Code Upgrade) [Segmented entry control] For custom implementation, code in this method needs to be moved elsewhere based on the migration guidance */
    public void segmentValueChanged(SegmentValueChangedEventArgs _e)
    {
        super(_e);
        /* TODO: (Code Upgrade) [Segmented entry control] Replace this based on the migration guidance */
        // dimDynamicAccountController.segmentValueChanged(_e);
    }

##### <a name="dynamics-ax-for-operations"></a><span data-ttu-id="c25f6-146">Dynamics AX for Operations</span><span class="sxs-lookup"><span data-stu-id="c25f6-146">Dynamics AX for Operations</span></span>

<span data-ttu-id="c25f6-147">このメソッドはコントロールの **segmentValueChanged()** メソッドのみを呼び出し追加の処理は実行しないため、削除できます。</span><span class="sxs-lookup"><span data-stu-id="c25f6-147">Because this method only calls the **segmentValueChanged()** method on the control and doesn't perform any additional processing, you can delete it.</span></span>

#### <a name="step-5"></a><span data-ttu-id="c25f6-148">ステップ 5</span><span class="sxs-lookup"><span data-stu-id="c25f6-148">Step 5</span></span>

##### <a name="dynamics-ax-2012"></a><span data-ttu-id="c25f6-149">Dynamics AX 2012</span><span class="sxs-lookup"><span data-stu-id="c25f6-149">Dynamics AX 2012</span></span>

    /* TODO: (Code Upgrade) [Segmented entry control] This method can be removed if there is no custom implementation */
    public boolean validate()
    {
        boolean isValid;
        isValid = super();
        /* TODO: (Code Upgrade) [Segmented entry control] This statement can be removed if there is no custom logic */
        // isValid = dimDynamicAccountController.validate() && isValid;
        return isValid;
    }

##### <a name="dynamics-ax-for-operations"></a><span data-ttu-id="c25f6-150">Dynamics AX for Operations</span><span class="sxs-lookup"><span data-stu-id="c25f6-150">Dynamics AX for Operations</span></span>

<span data-ttu-id="c25f6-151">このメソッドはコントロールの **validate()** メソッドのみを呼び出し追加の処理は実行しないため、削除できます。</span><span class="sxs-lookup"><span data-stu-id="c25f6-151">Because this method only calls the **validate()** method on the control and doesn't perform any additional processing, you can delete it.</span></span>

### <a name="controller-variable-declarations"></a><span data-ttu-id="c25f6-152">コントローラー変数申告</span><span class="sxs-lookup"><span data-stu-id="c25f6-152">Controller variable declarations</span></span>

##### <a name="dynamics-ax-2012"></a><span data-ttu-id="c25f6-153">Dynamics AX 2012</span><span class="sxs-lookup"><span data-stu-id="c25f6-153">Dynamics AX 2012</span></span>

<span data-ttu-id="c25f6-154">最後に、コントローラー変数申告のため、最初の TODO に戻ります。</span><span class="sxs-lookup"><span data-stu-id="c25f6-154">Finally, go back to the first TODO, for the controller variable declaration.</span></span>

    /* TODO: (Code Upgrade) [Segmented entry control] Replace this based on the migration guidance */
    /* 'dimDynamicAccountController' controller object is used with 'ExpenseCost_LedgerDimension' segmented entry controls.*/
    DimensionDynamicAccountController dimDynamicAccountController;

##### <a name="dynamics-ax-for-operations"></a><span data-ttu-id="c25f6-155">Dynamics AX for Operations</span><span class="sxs-lookup"><span data-stu-id="c25f6-155">Dynamics AX for Operations</span></span>

<span data-ttu-id="c25f6-156">**dimDynamicAccountController** 変数は、フォームで使用されなくなりました。</span><span class="sxs-lookup"><span data-stu-id="c25f6-156">The **dimDynamicAccountController** variable is no longer used on the form.</span></span> <span data-ttu-id="c25f6-157">したがって、削除できるようになりました。</span><span class="sxs-lookup"><span data-stu-id="c25f6-157">Therefore, you can now delete it.</span></span>

## <a name="complex-migration-scenario--ledgerjournaltransdaily-form"></a><span data-ttu-id="c25f6-158">複雑な移行シナリオ – LedgerJournalTransDaily フォーム</span><span class="sxs-lookup"><span data-stu-id="c25f6-158">Complex migration scenario – LedgerJournalTransDaily form</span></span>
1.  <span data-ttu-id="c25f6-159">アプリケーション エクスプローラーで **LedgerJournalTransDaily** フォームを検索します。</span><span class="sxs-lookup"><span data-stu-id="c25f6-159">Search for the **LedgerJournalTransDaily** form in Application Explorer.</span></span>
2.  <span data-ttu-id="c25f6-160">現在のプロジェクトにフォームを追加します。</span><span class="sxs-lookup"><span data-stu-id="c25f6-160">Add the form to the current project.</span></span>
3.  <span data-ttu-id="c25f6-161">フォーム デザイン ビューとコード エディタ ビューで、フォームを開きます。</span><span class="sxs-lookup"><span data-stu-id="c25f6-161">Open the form in the form design view and the code editor view.</span></span>
4.  <span data-ttu-id="c25f6-162">フォーム デザイン ビューで、手動でコントロール ツリーを移動するか、**ファイル** タブの下にある検索バーで「SegmentedEntry」を検索して、SEC を見つけます。</span><span class="sxs-lookup"><span data-stu-id="c25f6-162">In the form design view, find the SEC, either by manually walking the control tree or by searching for “SegmentedEntry” in the search bar below the **File** tab.</span></span>
5.  <span data-ttu-id="c25f6-163">SEC を選択し、次の情報を確認します。</span><span class="sxs-lookup"><span data-stu-id="c25f6-163">Select the SEC, and verify the following information:</span></span>
    -   <span data-ttu-id="c25f6-164">コントロールの横にある括弧で指定されたコントロールのタイプは、**SegmentedEntryControl** です。</span><span class="sxs-lookup"><span data-stu-id="c25f6-164">The type for the control, as specified in parenthesis next to the control, is **SegmentedEntryControl**.</span></span>
    -   <span data-ttu-id="c25f6-165">**コントローラー クラス** プロパティは **DimensionDynamicAccountController** に設定されます。</span><span class="sxs-lookup"><span data-stu-id="c25f6-165">The **Controller class** property is set to **DimensionDynamicAccountController**.</span></span> <span data-ttu-id="c25f6-166">このプロパティは、SEC のこのインスタンスが使用するコントローラーのタイプを示します。</span><span class="sxs-lookup"><span data-stu-id="c25f6-166">This property indicates the type of controller that this instance of the SEC will use.</span></span> <span data-ttu-id="c25f6-167">コントローラーのタイプによって、コントロールのビヘイビアーが決まります。</span><span class="sxs-lookup"><span data-stu-id="c25f6-167">The type of controller, in turn, determines the behavior of the control.</span></span>

6.  <span data-ttu-id="c25f6-168">コード エディタ ビューに切り替え、フォーム ソース コードで "TODO: (コード アップグレード) \[セグメント化されたエントリ コントロール\]" のすべての事例を検索します。</span><span class="sxs-lookup"><span data-stu-id="c25f6-168">Switch to the code editor view, and search for all occurrences of “TODO: (Code Upgrade) \[Segmented entry control\]” in the form source code.</span></span>
7.  <span data-ttu-id="c25f6-169">検索結果で、最初の 3 件の結果はコントローラー変数申告用です。</span><span class="sxs-lookup"><span data-stu-id="c25f6-169">In the search results, the first three results are for the controller variable declarations.</span></span> <span data-ttu-id="c25f6-170">"仕事" を添付しているコメントを参照して、どの SEC インスタンスがどのコントローラー インスタンスを使用しているか示すマッピングを記録します。</span><span class="sxs-lookup"><span data-stu-id="c25f6-170">Look at the comments that accompany the TODOs, and make a note of the mapping that shows which SEC instance uses which controller instance.</span></span> <span data-ttu-id="c25f6-171">このマッピングは、コントローラーでのメソッド呼び出しをコントロールでのメソッド呼び出しに置き換えるときに必要です。</span><span class="sxs-lookup"><span data-stu-id="c25f6-171">You will need this mapping when you replace method calls on the controller with method calls on the control.</span></span> <span data-ttu-id="c25f6-172">コントローラーからコントロールへのマッピングがどのようなものかを次に示します。</span><span class="sxs-lookup"><span data-stu-id="c25f6-172">Here is what the controller-to-control mapping looks like:</span></span>
    1.  <span data-ttu-id="c25f6-173">dimAccountController</span><span class="sxs-lookup"><span data-stu-id="c25f6-173">dimAccountController</span></span>
        1.  <span data-ttu-id="c25f6-174">LedgerJournalTrans\_AccountNum</span><span class="sxs-lookup"><span data-stu-id="c25f6-174">LedgerJournalTrans\_AccountNum</span></span>
        2.  <span data-ttu-id="c25f6-175">LedgerJournalTrans\_AccountNum1</span><span class="sxs-lookup"><span data-stu-id="c25f6-175">LedgerJournalTrans\_AccountNum1</span></span>
        3.  <span data-ttu-id="c25f6-176">Group4\_AccountNum</span><span class="sxs-lookup"><span data-stu-id="c25f6-176">Group4\_AccountNum</span></span>

    2.  <span data-ttu-id="c25f6-177">dimOffsetAccountController</span><span class="sxs-lookup"><span data-stu-id="c25f6-177">dimOffsetAccountController</span></span>
        1.  <span data-ttu-id="c25f6-178">GridOffsetAccount</span><span class="sxs-lookup"><span data-stu-id="c25f6-178">GridOffsetAccount</span></span>
        2.  <span data-ttu-id="c25f6-179">LedgerJournalTrans\_OffsetAccount1</span><span class="sxs-lookup"><span data-stu-id="c25f6-179">LedgerJournalTrans\_OffsetAccount1</span></span>
        3.  <span data-ttu-id="c25f6-180">Group4\_OffsetAccount</span><span class="sxs-lookup"><span data-stu-id="c25f6-180">Group4\_OffsetAccount</span></span>

    3.  <span data-ttu-id="c25f6-181">dimPaymentFeeAccountController</span><span class="sxs-lookup"><span data-stu-id="c25f6-181">dimPaymentFeeAccountController</span></span>
        1.  <span data-ttu-id="c25f6-182">CustPaymJournalFee\_CustAccount</span><span class="sxs-lookup"><span data-stu-id="c25f6-182">CustPaymJournalFee\_CustAccount</span></span>

    <span data-ttu-id="c25f6-183">コントローラー変数へのすべての参照を削除した後、最後に、これらの 3 つの TODO コメントを修正します。</span><span class="sxs-lookup"><span data-stu-id="c25f6-183">You will fix these three TODO comments at the end, after you've removed all references to the controller variables.</span></span>
8.  <span data-ttu-id="c25f6-184">次のサブセクションでの説明にあるように、残りの各 TODO コメントが実行されます。</span><span class="sxs-lookup"><span data-stu-id="c25f6-184">Go through each of the remaining TODO comments, as described in the following subsections.</span></span>

### <a name="ledgerdimension-data-field"></a><span data-ttu-id="c25f6-185">LedgerDimension データ フィールド</span><span class="sxs-lookup"><span data-stu-id="c25f6-185">LedgerDimension data field</span></span>

<span data-ttu-id="c25f6-186">(**フォーム**&gt;**データ ソース** &gt;**LedgerJournalTrans**&gt; **フィールド** &gt;**LedgerDimension**&gt;  **方法**)</span><span class="sxs-lookup"><span data-stu-id="c25f6-186">(**Form** &gt; **Data sources** &gt; **LedgerJournalTrans** &gt; **Fields** &gt; **LedgerDimension** &gt; **Methods**)</span></span>

##### <a name="dynamics-ax-2012"></a><span data-ttu-id="c25f6-187">Dynamics AX 2012</span><span class="sxs-lookup"><span data-stu-id="c25f6-187">Dynamics AX 2012</span></span>

    /* TODO: (Code Upgrade) [Segmented entry control] This method can be removed if there is no custom implementation */
    // </GEEPL>
    public void jumpRef()
    {
        LedgerJournalTrans_AccountNum.jumpRef();
        LedgerJournalTrans_AccountNum1.jumpRef();
        Group4_AccountNum.jumpRef();
    }

##### <a name="dynamics-ax-for-operations"></a><span data-ttu-id="c25f6-188">Dynamics AX for Operations</span><span class="sxs-lookup"><span data-stu-id="c25f6-188">Dynamics AX for Operations</span></span>

<span data-ttu-id="c25f6-189">このメソッドはコントロールの **jumpRef()** メソッドのみを呼び出し追加の処理は実行しないため、削除できます。</span><span class="sxs-lookup"><span data-stu-id="c25f6-189">Because this method only calls the **jumpRef()** method on the control and doesn't perform any additional processing, you can delete it.</span></span>

### <a name="offsetledgerdimension-data-field"></a><span data-ttu-id="c25f6-190">OffsetLedgerDimension データ フィールド</span><span class="sxs-lookup"><span data-stu-id="c25f6-190">OffsetLedgerDimension data field</span></span>

<span data-ttu-id="c25f6-191">(**フォーム**&gt;**データ ソース** &gt;**LedgerJournalTrans**&gt; **フィールド** &gt;**OffsetLedgerDimension**&gt; **方法**)</span><span class="sxs-lookup"><span data-stu-id="c25f6-191">(**Form** &gt; **Data sources** &gt; **LedgerJournalTrans** &gt; **Fields** &gt; **OffsetLedgerDimension** &gt; **Methods**)</span></span>

##### <a name="dynamics-ax-2012"></a><span data-ttu-id="c25f6-192">Dynamics AX 2012</span><span class="sxs-lookup"><span data-stu-id="c25f6-192">Dynamics AX 2012</span></span>

<span data-ttu-id="c25f6-193">**OffsetLedgerDimension** フィールドの **jumpRef()** メソッド。</span><span class="sxs-lookup"><span data-stu-id="c25f6-193">The **OffsetLedgerDimension** field’s **jumpRef()** method:</span></span>

    /* TODO: (Code Upgrade) [Segmented entry control] This method can be removed if there is no custom implementation */
    public void jumpRef()
    {
        GridOffsetAccount.jumpRef();
        LedgerJournalTrans_OffsetAccount1.jumpRef();
        Group4_OffsetAccount.jumpRef();
    }

##### <a name="dynamics-ax-for-operations"></a><span data-ttu-id="c25f6-194">Dynamics AX for Operations</span><span class="sxs-lookup"><span data-stu-id="c25f6-194">Dynamics AX for Operations</span></span>

<span data-ttu-id="c25f6-195">このメソッドはコントロールの **jumpRef()** メソッドのみを呼び出し追加の処理は実行しないため、削除できます。</span><span class="sxs-lookup"><span data-stu-id="c25f6-195">Because this method only calls the **jumpRef()** method on the control and doesn't perform any additional processing, you can delete it.</span></span>

### <a name="ledgerjournaltrans_accountnum-control"></a><span data-ttu-id="c25f6-196">LedgerJournalTrans\_AccountNum コントロール</span><span class="sxs-lookup"><span data-stu-id="c25f6-196">LedgerJournalTrans\_AccountNum control</span></span>

<span data-ttu-id="c25f6-197">(**フォーム**タブの下にある検索バーで、「LedgerJournalTrans\_AccountNum」を検索してください。)</span><span class="sxs-lookup"><span data-stu-id="c25f6-197">(Search for "LedgerJournalTrans\_AccountNum" in the search bar below the **Form** tab.)</span></span>

#### <a name="step-1"></a><span data-ttu-id="c25f6-198">ステップ１</span><span class="sxs-lookup"><span data-stu-id="c25f6-198">Step 1</span></span>

##### <a name="dynamics-ax-2012"></a><span data-ttu-id="c25f6-199">Dynamics AX 2012</span><span class="sxs-lookup"><span data-stu-id="c25f6-199">Dynamics AX 2012</span></span>

    /* TODO: (Code Upgrade) [Segmented entry control] This method can be removed if there is no custom implementation */
    public void jumpRef()
    {
        LedgerJournalTrans_AccountNum.jumpRef();
        LedgerJournalTrans_AccountNum1.jumpRef();
        Group4_AccountNum.jumpRef();
    }

##### <a name="dynamics-ax-for-operations"></a><span data-ttu-id="c25f6-200">Dynamics AX for Operations</span><span class="sxs-lookup"><span data-stu-id="c25f6-200">Dynamics AX for Operations</span></span>

<span data-ttu-id="c25f6-201">このメソッドはコントロールの **jumpRef()** メソッドのみを呼び出し追加の処理は実行しないため、削除できます。</span><span class="sxs-lookup"><span data-stu-id="c25f6-201">Because this method only calls the **jumpRef()** method on the control and doesn't perform any additional processing, you can delete it.</span></span>

#### <a name="step-2"></a><span data-ttu-id="c25f6-202">ステップ２</span><span class="sxs-lookup"><span data-stu-id="c25f6-202">Step 2</span></span>

##### <a name="dynamics-ax-2012"></a><span data-ttu-id="c25f6-203">Dynamics AX 2012</span><span class="sxs-lookup"><span data-stu-id="c25f6-203">Dynamics AX 2012</span></span>

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

##### <a name="dynamics-ax-for-operations"></a><span data-ttu-id="c25f6-204">Dynamics AX for Operations</span><span class="sxs-lookup"><span data-stu-id="c25f6-204">Dynamics AX for Operations</span></span>

1.  <span data-ttu-id="c25f6-205">**initLedger()** メソッドを更新します。</span><span class="sxs-lookup"><span data-stu-id="c25f6-205">Update the **initLedger()** method.</span></span>

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

2.  <span data-ttu-id="c25f6-206">**LedgerJournalTrans** データ ソースの **active()** メソッドでコードを更新します。</span><span class="sxs-lookup"><span data-stu-id="c25f6-206">Update the code in the **LedgerJournalTrans** data source’s **active()** method.</span></span> <span data-ttu-id="c25f6-207">**注記:** **getValue()** メソッドは、勘定タイプが**元帳**に設定されている場合にのみ呼び出す必要があります。</span><span class="sxs-lookup"><span data-stu-id="c25f6-207">**Note:** The **getValue()** method should be called only if the account type is set to **Ledger**.</span></span> <span data-ttu-id="c25f6-208">それ以外の場合、このメソッドを呼び出すと、無効な関数呼び出しが発生します。</span><span class="sxs-lookup"><span data-stu-id="c25f6-208">Otherwise, a call to this method will cause an invalid function call.</span></span>

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

3.  <span data-ttu-id="c25f6-209">**LedgerJournalTrans** データ ソースの **CurrencyCode** フィールドの **modified()** メソッドに、次のコードを追加します。</span><span class="sxs-lookup"><span data-stu-id="c25f6-209">Add the following code to the **modified()** method of the **LedgerJournalTrans** data source’s **CurrencyCode** field.</span></span>

        LedgerJournalTrans_AccountNum.parmCurrency(ledgerJournalTrans.CurrencyCode);
        LedgerJournalTrans_AccountNum1.parmCurrency(ledgerJournalTrans.CurrencyCode);
        Group4_AccountNum.parmCurrency(ledgerJournalTrans.CurrencyCode);

4.  <span data-ttu-id="c25f6-210">**LedgerJournalTrans** データ ソースの **Company** フィールドの **modified()** メソッドに、次のコードを追加します。</span><span class="sxs-lookup"><span data-stu-id="c25f6-210">Add the following code to the **modified()** method of the **LedgerJournalTrans** data source’s **Company** field.</span></span>

        LedgerJournalTrans_AccountNum.parmDataAreaId(ledgerJournalTrans.Company ? ledgerJournalTrans.Company : curext());
        LedgerJournalTrans_AccountNum1.parmDataAreaId(ledgerJournalTrans.Company ? ledgerJournalTrans.Company : curext());
        Group4_AccountNum.parmDataAreaId(ledgerJournalTrans.Company ? ledgerJournalTrans.Company : curext());

5.  <span data-ttu-id="c25f6-211">**LedgerJournalTrans** データ ソースの **TransDate** フィールドの **modified()** メソッドに、次のコードを追加します。</span><span class="sxs-lookup"><span data-stu-id="c25f6-211">Add the following code to the **modified()** method of the **LedgerJournalTrans** data source’s **TransDate** field.</span></span>

        LedgerJournalTrans_AccountNum.parmControlDate(ledgerJournalTrans.TransDate);
        LedgerJournalTrans_AccountNum1.parmControlDate(ledgerJournalTrans.TransDate);
        Group4_AccountNum.parmControlDate(ledgerJournalTrans.TransDate);

6.  <span data-ttu-id="c25f6-212">**loadSegments()** メソッドを削除します。</span><span class="sxs-lookup"><span data-stu-id="c25f6-212">Delete the **loadSegments()** method.</span></span>

#### <a name="step-3"></a><span data-ttu-id="c25f6-213">ステップ 3</span><span class="sxs-lookup"><span data-stu-id="c25f6-213">Step 3</span></span>

##### <a name="dynamics-ax-2012"></a><span data-ttu-id="c25f6-214">Dynamics AX 2012</span><span class="sxs-lookup"><span data-stu-id="c25f6-214">Dynamics AX 2012</span></span>

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

##### <a name="dynamics-ax-for-operations"></a><span data-ttu-id="c25f6-215">Dynamics AX for Operations</span><span class="sxs-lookup"><span data-stu-id="c25f6-215">Dynamics AX for Operations</span></span>

<span data-ttu-id="c25f6-216">このメソッドは、コントロールのカスタム ルックアップを実装します。</span><span class="sxs-lookup"><span data-stu-id="c25f6-216">This method implements a custom lookup for the control.</span></span> <span data-ttu-id="c25f6-217">したがって、メソッドをそのままにします。</span><span class="sxs-lookup"><span data-stu-id="c25f6-217">Therefore, leave the method as it is.</span></span> <span data-ttu-id="c25f6-218">"仕事" を削除します。</span><span class="sxs-lookup"><span data-stu-id="c25f6-218">Just remove the TODO.</span></span> <span data-ttu-id="c25f6-219">カスタムのルックアップをフック アップするには、SEC の **checkUseCustomLookup** メソッドをオーバーライドする必要があります。</span><span class="sxs-lookup"><span data-stu-id="c25f6-219">To hook up custom lookups, you must override the SEC’s **checkUseCustomLookup** method.</span></span> <span data-ttu-id="c25f6-220">また、カスタム ルックアップ フォームで **closeSelectRecord** メソッドが上書きされたことを確認してください。</span><span class="sxs-lookup"><span data-stu-id="c25f6-220">Additionally, make sure that the **closeSelectRecord** method on the custom lookup form is overridden.</span></span> <span data-ttu-id="c25f6-221">例については、**CustTableLookup** フォームを参照してください。</span><span class="sxs-lookup"><span data-stu-id="c25f6-221">For an example, see the **CustTableLookup** form.</span></span>

#### <a name="step-4"></a><span data-ttu-id="c25f6-222">ステップ 4</span><span class="sxs-lookup"><span data-stu-id="c25f6-222">Step 4</span></span>

##### <a name="dynamics-ax-2012"></a><span data-ttu-id="c25f6-223">Dynamics AX 2012</span><span class="sxs-lookup"><span data-stu-id="c25f6-223">Dynamics AX 2012</span></span>

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

##### <a name="dynamics-ax-for-operations"></a><span data-ttu-id="c25f6-224">Dynamics AX for Operations</span><span class="sxs-lookup"><span data-stu-id="c25f6-224">Dynamics AX for Operations</span></span>

1.  <span data-ttu-id="c25f6-225">コントロールの **onSegmentChanged()** メソッドをオーバーライドし、次のコードを追加します。</span><span class="sxs-lookup"><span data-stu-id="c25f6-225">Override the **onSegmentChanged()** method on the control, and add the following code to it.</span></span>

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

2.  <span data-ttu-id="c25f6-226">**segmentValueChanged()** メソッドを削除します。</span><span class="sxs-lookup"><span data-stu-id="c25f6-226">Delete the **segmentValueChanged()** method.</span></span> <span data-ttu-id="c25f6-227">**注記:** **onPrimaryAccountSegmentChanged()** メソッドでは、コントローラー オブジェクトが必要ですが、このコードは SEC のインスタンスを渡すので、**onSegmentChanged()** メソッドの前のコードはコンパイルされません。</span><span class="sxs-lookup"><span data-stu-id="c25f6-227">**Note:** The preceding code for the **onSegmentChanged()** method will not compile, because the **onPrimaryAccountSegmentChanged()** method expects a controller object, but this code passes an instance of the SEC.</span></span> <span data-ttu-id="c25f6-228">コントロール インスタンスでメソッドを呼び出すには、メソッドのシグネチャとその実装を適宜変更する必要があります。</span><span class="sxs-lookup"><span data-stu-id="c25f6-228">To call methods on the control instance, you must change the method’s signature and its implementation accordingly.</span></span> <span data-ttu-id="c25f6-229">このメソッドは、50 以上の呼び出し元が使用されます。</span><span class="sxs-lookup"><span data-stu-id="c25f6-229">This method is used by more than 50 callers.</span></span> <span data-ttu-id="c25f6-230">したがって、これらの呼び出しをすべて更新する必要があります。</span><span class="sxs-lookup"><span data-stu-id="c25f6-230">Therefore, you would also have to update all those calls.</span></span> <span data-ttu-id="c25f6-231">または、このガイダンスに従うことによって新しいメソッドを追加できます。</span><span class="sxs-lookup"><span data-stu-id="c25f6-231">Alternatively, you can add a new method that follows this guidance.</span></span>

#### <a name="step-5"></a><span data-ttu-id="c25f6-232">ステップ 5</span><span class="sxs-lookup"><span data-stu-id="c25f6-232">Step 5</span></span>

##### <a name="dynamics-ax-2012"></a><span data-ttu-id="c25f6-233">Dynamics AX 2012</span><span class="sxs-lookup"><span data-stu-id="c25f6-233">Dynamics AX 2012</span></span>

    /* TODO: (Code Upgrade) [Segmented entry control] This method can be removed if there is no custom implementation */
    public boolean validate()
    {
        boolean isValid;
        isValid = super();

        /* TODO: (Code Upgrade) [Segmented entry control] This statement can be removed if there is no custom logic */
        // isValid = dimAccountController.validate() && isValid;
        return isValid;
    }

##### <a name="dynamics-ax-for-operations"></a><span data-ttu-id="c25f6-234">Dynamics AX for Operations</span><span class="sxs-lookup"><span data-stu-id="c25f6-234">Dynamics AX for Operations</span></span>

<span data-ttu-id="c25f6-235">このメソッドはコントロールの **validate()** メソッドのみを呼び出し追加の処理は実行しないため、削除できます。</span><span class="sxs-lookup"><span data-stu-id="c25f6-235">Because this method only calls the **validate()** method on the control and doesn't perform any additional processing, you can delete it.</span></span>

### <a name="gridoffsetaccount-control"></a><span data-ttu-id="c25f6-236">GridOffsetAccount コントロール</span><span class="sxs-lookup"><span data-stu-id="c25f6-236">GridOffsetAccount control</span></span>

<span data-ttu-id="c25f6-237">(**フォーム**タブの下にある「GridOffsetAccount」を検索してください。)</span><span class="sxs-lookup"><span data-stu-id="c25f6-237">(Search for "GridOffsetAccount" in the search bar below the **Form** tab.)</span></span>

#### <a name="step-1"></a><span data-ttu-id="c25f6-238">ステップ１</span><span class="sxs-lookup"><span data-stu-id="c25f6-238">Step 1</span></span>

##### <a name="dynamics-ax-2012"></a><span data-ttu-id="c25f6-239">Dynamics AX 2012</span><span class="sxs-lookup"><span data-stu-id="c25f6-239">Dynamics AX 2012</span></span>

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

##### <a name="dynamics-ax-for-operations"></a><span data-ttu-id="c25f6-240">Dynamics AX for Operations</span><span class="sxs-lookup"><span data-stu-id="c25f6-240">Dynamics AX for Operations</span></span>

1.  <span data-ttu-id="c25f6-241">ledgerJournalTable バッファを更新するコードの後に、**initLedger()** メソッドへ次のコードを追加します。</span><span class="sxs-lookup"><span data-stu-id="c25f6-241">Add the following code to the **initLedger()** method, after the code that updates the ledgerJournalTable buffer.</span></span>

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

2.  <span data-ttu-id="c25f6-242">**gotFocus()** メソッドを削除します。</span><span class="sxs-lookup"><span data-stu-id="c25f6-242">Delete the **gotFocus()** method.</span></span>

#### <a name="step-2"></a><span data-ttu-id="c25f6-243">ステップ２</span><span class="sxs-lookup"><span data-stu-id="c25f6-243">Step 2</span></span>

##### <a name="dynamics-ax-2012"></a><span data-ttu-id="c25f6-244">Dynamics AX 2012</span><span class="sxs-lookup"><span data-stu-id="c25f6-244">Dynamics AX 2012</span></span>

    /* TODO: (Code Upgrade) [Segmented entry control] This method can be removed if there is no custom implementation */
    public void jumpRef()
    {
        GridOffsetAccount.jumpRef();
        LedgerJournalTrans_OffsetAccount1.jumpRef();
        Group4_OffsetAccount.jumpRef();
    }

##### <a name="dynamics-ax-for-operations"></a><span data-ttu-id="c25f6-245">Dynamics AX for Operations</span><span class="sxs-lookup"><span data-stu-id="c25f6-245">Dynamics AX for Operations</span></span>

<span data-ttu-id="c25f6-246">このメソッドはコントロールの **jumpRef()** メソッドのみを呼び出し追加の処理は実行しないため、削除できます。</span><span class="sxs-lookup"><span data-stu-id="c25f6-246">Because this method only calls the **jumpRef()** method on the control and doesn't perform any additional processing, you can delete it.</span></span>

#### <a name="step-3"></a><span data-ttu-id="c25f6-247">ステップ 3</span><span class="sxs-lookup"><span data-stu-id="c25f6-247">Step 3</span></span>

##### <a name="dynamics-ax-2012"></a><span data-ttu-id="c25f6-248">Dynamics AX 2012</span><span class="sxs-lookup"><span data-stu-id="c25f6-248">Dynamics AX 2012</span></span>

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

##### <a name="dynamics-ax-for-operations"></a><span data-ttu-id="c25f6-249">Dynamics AX for Operations</span><span class="sxs-lookup"><span data-stu-id="c25f6-249">Dynamics AX for Operations</span></span>

1.  <span data-ttu-id="c25f6-250">**initLedger()** メソッドを更新します。</span><span class="sxs-lookup"><span data-stu-id="c25f6-250">Update the **initLedger()** method.</span></span> <span data-ttu-id="c25f6-251">**注記:** **getValue()** メソッドは、勘定タイプが**元帳**に設定されている場合にのみ呼び出す必要があります。</span><span class="sxs-lookup"><span data-stu-id="c25f6-251">**Note:** The **getValue()** method should be called only if the account type is set to **Ledger**.</span></span> <span data-ttu-id="c25f6-252">それ以外の場合、このメソッドを呼び出すと、無効な関数呼び出しが発生します。</span><span class="sxs-lookup"><span data-stu-id="c25f6-252">Otherwise, a call to this method will cause an invalid function call.</span></span>

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

2.  <span data-ttu-id="c25f6-253">**LedgerJournalTrans** データ ソースの **active()** メソッドでコードを更新します。</span><span class="sxs-lookup"><span data-stu-id="c25f6-253">Update the code in the **LedgerJournalTrans** data source’s **active()** method.</span></span> <span data-ttu-id="c25f6-254">**注記:** **getValue()** メソッドは、勘定タイプが**元帳**に設定されている場合にのみ呼び出す必要があります。</span><span class="sxs-lookup"><span data-stu-id="c25f6-254">**Note:** The **getValue()** method should be called only if the account type is set to **Ledger**.</span></span> <span data-ttu-id="c25f6-255">それ以外の場合、このメソッドを呼び出すと、無効な関数呼び出しが発生します。</span><span class="sxs-lookup"><span data-stu-id="c25f6-255">Otherwise, a call to this method will cause an invalid function call.</span></span>

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

3.  <span data-ttu-id="c25f6-256">**LedgerJournalTrans** データ ソースの **CurrencyCode** フィールドの **modified()** メソッドに、次のコードを追加します。</span><span class="sxs-lookup"><span data-stu-id="c25f6-256">Add the following code to the **modified()** method of the **LedgerJournalTrans** data source’s **CurrencyCode** field.</span></span>

        GridOffsetAccount.parmCurrency(ledgerJournalTrans.CurrencyCode);
        LedgerJournalTrans_OffsetAccount1.parmCurrency(ledgerJournalTrans.CurrencyCode);
        Group4_OffsetAccount.parmCurrency(ledgerJournalTrans.CurrencyCode);

4.  <span data-ttu-id="c25f6-257">**LedgerJournalTrans** データ ソースの **OffsetCompany** フィールドの **modified()** メソッドに、次のコードを追加します。</span><span class="sxs-lookup"><span data-stu-id="c25f6-257">Add the following code to the **modified()** method of the **LedgerJournalTrans** data source’s **OffsetCompany** field.</span></span>

        GridOffsetAccount.parmDataAreaId(ledgerJournalTrans.getOffsetCompany());
        LedgerJournalTrans_OffsetAccount1.parmDataAreaId(ledgerJournalTrans.getOffsetCompany());
        Group4_OffsetAccount.parmDataAreaId(ledgerJournalTrans.getOffsetCompany());

5.  <span data-ttu-id="c25f6-258">**LedgerJournalTrans** データ ソースの **TransDate** フィールドの **modified()** メソッドに、次のコードを追加します。</span><span class="sxs-lookup"><span data-stu-id="c25f6-258">Add the following code to the **modified()** method of the **LedgerJournalTrans** data source’s **TransDate** field.</span></span>

        GridOffsetAccount.parmControlDate(ledgerJournalTrans.TransDate);
        LedgerJournalTrans_OffsetAccount1.parmControlDate(ledgerJournalTrans.TransDate);
        Group4_OffsetAccount.parmControlDate(ledgerJournalTrans.TransDate);

6.  <span data-ttu-id="c25f6-259">**LedgerJournalTrans** データ ソースの **OffsetAccountType** フィールドの **modified()** メソッドに、次のコードを追加します。</span><span class="sxs-lookup"><span data-stu-id="c25f6-259">Add the following code to the **modified()** method of the **LedgerJournalTrans** data source’s **OffsetAccountType** field.</span></span> <span data-ttu-id="c25f6-260">**注記:** **getValue()** メソッドは、勘定タイプが**元帳**に設定されている場合にのみ呼び出す必要があります。</span><span class="sxs-lookup"><span data-stu-id="c25f6-260">**Note:** The **getValue()** method should be called only if the account type is set to **Ledger**.</span></span> <span data-ttu-id="c25f6-261">それ以外の場合、このメソッドを呼び出すと、無効な関数呼び出しが発生します。</span><span class="sxs-lookup"><span data-stu-id="c25f6-261">Otherwise, a call to this method cause an invalid function call.</span></span>

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

7.  <span data-ttu-id="c25f6-262">**loadSegments()** メソッドを削除します。</span><span class="sxs-lookup"><span data-stu-id="c25f6-262">Delete the **loadSegments()** method.</span></span>

#### <a name="step-4"></a><span data-ttu-id="c25f6-263">ステップ 4</span><span class="sxs-lookup"><span data-stu-id="c25f6-263">Step 4</span></span>

##### <a name="dynamics-ax-2012"></a><span data-ttu-id="c25f6-264">Dynamics AX 2012</span><span class="sxs-lookup"><span data-stu-id="c25f6-264">Dynamics AX 2012</span></span>

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

##### <a name="dynamics-ax-for-operations"></a><span data-ttu-id="c25f6-265">Dynamics AX for Operations</span><span class="sxs-lookup"><span data-stu-id="c25f6-265">Dynamics AX for Operations</span></span>

<span data-ttu-id="c25f6-266">このメソッドは、コントロールのカスタム ルックアップを実装します。</span><span class="sxs-lookup"><span data-stu-id="c25f6-266">This method implements a custom lookup for the control.</span></span> <span data-ttu-id="c25f6-267">したがって、メソッドを保持しますが、コントローラーをコントロール インスタンスに置き換えます。</span><span class="sxs-lookup"><span data-stu-id="c25f6-267">Therefore, keep the method, but replace the controller with the control instance.</span></span> <span data-ttu-id="c25f6-268">この場合、メソッドは **GridOffsetAccount** コントロールでオーバーライドされるため、**dimOffsetAccountController** が (コントローラー変数宣言の "仕事" に示されたマッピングに基づいて) 3 つの異なる SEC インスタンスに使用される場合でも、コントローラーをたった 1 つの SEC インスタンスに置き換える必要があります。</span><span class="sxs-lookup"><span data-stu-id="c25f6-268">In this case, because the method is overridden on the **GridOffsetAccount** control, even though **dimOffsetAccountController** was used for three different SEC instances (based on the mapping that is shown in the TODOs on controller variable declarations), we must replace the controller with only one SEC instance.</span></span> <span data-ttu-id="c25f6-269">したがって、コードは次のようになります。</span><span class="sxs-lookup"><span data-stu-id="c25f6-269">Therefore, the code will look like this.</span></span>

    public void lookup()
    {
        // Find the current segment index value
        int currentSegmentIndex = GridOffsetAccount.getCurrentSegmentIndex();
        if ((ledgerJournalTrans.OffsetAccountType == LedgerJournalACType::Ledger && GridOffsetAccount.getDimensionAttributeByControlIndex(currentSegmentIndex) != DimensionAttribute::getWellKnownDimensionAttribute(DimensionAttributeType::MainAccount)) || !ledgerJournalEngine.offsetAccountNumLookUp(gridOffsetAccount, ledgerJournalTrans))
        {
            super();
        }
    }

<span data-ttu-id="c25f6-270">カスタムのルックアップをフック アップするには、SEC の **checkUseCustomLookup** メソッドをオーバーライドする必要があります。</span><span class="sxs-lookup"><span data-stu-id="c25f6-270">To hook up custom lookups, you must override the SEC’s **checkUseCustomLookup** method.</span></span> <span data-ttu-id="c25f6-271">また、カスタム ルックアップ フォームで **closeSelectRecord** メソッドが上書きされたことを確認してください。</span><span class="sxs-lookup"><span data-stu-id="c25f6-271">Additionally, make sure that the **closeSelectRecord** method on the custom lookup form is overridden.</span></span> <span data-ttu-id="c25f6-272">例については、**CustTableLookup** フォームを参照してください。</span><span class="sxs-lookup"><span data-stu-id="c25f6-272">For an example, see the **CustTableLookup** form.</span></span>

#### <a name="step-5"></a><span data-ttu-id="c25f6-273">ステップ 5</span><span class="sxs-lookup"><span data-stu-id="c25f6-273">Step 5</span></span>

##### <a name="dynamics-ax-2012"></a><span data-ttu-id="c25f6-274">Dynamics AX 2012</span><span class="sxs-lookup"><span data-stu-id="c25f6-274">Dynamics AX 2012</span></span>

    /* TODO: (Code Upgrade) [Segmented entry control] For custom implementation, code in this method needs to be moved elsewhere based on the migration guidance */
    public void segmentValueChanged(SegmentValueChangedEventArgs _e)
    {
        super(_e);
        /* TODO: (Code Upgrade) [Segmented entry control] Replace this based on the migration guidance */
        // dimOffsetAccountController.segmentValueChanged(_e);
        currentOffsetMainAccountId = ledgerJournalEngine.onOffsetAccountSegmentChanged(dimOffsetAccountController, currentOffsetMainAccountId, ledgerJournalTrans);
    }

##### <a name="dynamics-ax-for-operations"></a><span data-ttu-id="c25f6-275">Dynamics AX for Operations</span><span class="sxs-lookup"><span data-stu-id="c25f6-275">Dynamics AX for Operations</span></span>

1.  <span data-ttu-id="c25f6-276">コントロールの **onSegmentChanged()** メソッドをオーバーライドし、次のコードを追加します。</span><span class="sxs-lookup"><span data-stu-id="c25f6-276">Override the **onSegmentChanged()** method on the control, and add the following code to it.</span></span>

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

2.  <span data-ttu-id="c25f6-277">**segmentValueChanged()** メソッドを削除します。</span><span class="sxs-lookup"><span data-stu-id="c25f6-277">Delete the **segmentValueChanged()** method.</span></span> <span data-ttu-id="c25f6-278">**注記:** **onOffsetAccountSegmentChanged()** メソッドでは、コントローラー オブジェクトが必要ですが、このコードは SEC のインスタンスを渡すので、**onSegmentChanged()** メソッドの前のコードはコンパイルされません。</span><span class="sxs-lookup"><span data-stu-id="c25f6-278">**Note:** The preceding code for the **onSegmentChanged()** method will not compile, because the **onOffsetAccountSegmentChanged()** method expects a controller object, but this code passes an instance of the SEC.</span></span> <span data-ttu-id="c25f6-279">コントロール インスタンスでメソッドを呼び出すには、メソッドのシグネチャとその実装を適宜変更する必要があります。</span><span class="sxs-lookup"><span data-stu-id="c25f6-279">To call methods on the control instance, you must change the method’s signature and its implementation accordingly.</span></span> <span data-ttu-id="c25f6-280">このメソッドは、50 以上の呼び出し元が使用されます。</span><span class="sxs-lookup"><span data-stu-id="c25f6-280">This method is used by more than 50 callers.</span></span> <span data-ttu-id="c25f6-281">したがって、これらの呼び出しをすべて更新する必要があります。</span><span class="sxs-lookup"><span data-stu-id="c25f6-281">Therefore, you would also have to update all those calls.</span></span> <span data-ttu-id="c25f6-282">または、このガイダンスに従うことによって新しいメソッドを追加できます。</span><span class="sxs-lookup"><span data-stu-id="c25f6-282">Alternatively, you can add a new method that follows this guidance.</span></span>

#### <a name="step-6"></a><span data-ttu-id="c25f6-283">ステップ 6</span><span class="sxs-lookup"><span data-stu-id="c25f6-283">Step 6</span></span>

##### <a name="dynamics-ax-2012"></a><span data-ttu-id="c25f6-284">Dynamics AX 2012</span><span class="sxs-lookup"><span data-stu-id="c25f6-284">Dynamics AX 2012</span></span>

    /* TODO: (Code Upgrade) [Segmented entry control] This method can be removed if there is no custom implementation */
    public boolean validate()
    {
        boolean isValid;
        isValid = super();

        /* TODO: (Code Upgrade) [Segmented entry control] This statement can be removed if there is no custom logic */
        // isValid = dimOffsetAccountController.validate() && isValid;
        return isValid;
    }

##### <a name="dynamics-ax-for-operations"></a><span data-ttu-id="c25f6-285">Dynamics AX for Operations</span><span class="sxs-lookup"><span data-stu-id="c25f6-285">Dynamics AX for Operations</span></span>

<span data-ttu-id="c25f6-286">このメソッドはコントロールの **validate()** メソッドのみを呼び出し追加の処理は実行しないため、削除できます。</span><span class="sxs-lookup"><span data-stu-id="c25f6-286">Because this method only calls the **validate()** method on the control and doesn't perform any additional processing, you can delete it.</span></span>

### <a name="ledgerjournaltrans_accountnum1"></a><span data-ttu-id="c25f6-287">LedgerJournalTrans\_AccountNum1</span><span class="sxs-lookup"><span data-stu-id="c25f6-287">LedgerJournalTrans\_AccountNum1</span></span>

<span data-ttu-id="c25f6-288">(**フォーム**タブの下にある検索バーで、「LedgerJournalTrans\_AccountNum1」を検索してください。)</span><span class="sxs-lookup"><span data-stu-id="c25f6-288">(Search for "LedgerJournalTrans\_AccountNum1" in the search bar below the **Form** tab.)</span></span>

#### <a name="step-1"></a><span data-ttu-id="c25f6-289">ステップ１</span><span class="sxs-lookup"><span data-stu-id="c25f6-289">Step 1</span></span>

##### <a name="dynamics-ax-2012"></a><span data-ttu-id="c25f6-290">Dynamics AX 2012</span><span class="sxs-lookup"><span data-stu-id="c25f6-290">Dynamics AX 2012</span></span>

    /* TODO: (Code Upgrade) [Segmented entry control] This method can be removed if there is no custom implementation */
    public void jumpRef()
    {
        LedgerJournalTrans_AccountNum.jumpRef();
        LedgerJournalTrans_AccountNum1.jumpRef();
        Group4_AccountNum.jumpRef();
    }

##### <a name="dynamics-ax-for-operations"></a><span data-ttu-id="c25f6-291">Dynamics AX for Operations</span><span class="sxs-lookup"><span data-stu-id="c25f6-291">Dynamics AX for Operations</span></span>

<span data-ttu-id="c25f6-292">このメソッドはコントロールの **jumpRef()** メソッドのみを呼び出し追加の処理は実行しないため、削除できます。</span><span class="sxs-lookup"><span data-stu-id="c25f6-292">Because this method only calls the **jumpRef()** method on the control and doesn't perform any additional processing, you can delete it.</span></span>

#### <a name="step-2"></a><span data-ttu-id="c25f6-293">ステップ２</span><span class="sxs-lookup"><span data-stu-id="c25f6-293">Step 2</span></span>

##### <a name="dynamics-ax-2012"></a><span data-ttu-id="c25f6-294">Dynamics AX 2012</span><span class="sxs-lookup"><span data-stu-id="c25f6-294">Dynamics AX 2012</span></span>

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

##### <a name="dynamics-ax-for-operations"></a><span data-ttu-id="c25f6-295">Dynamics AX for Operations</span><span class="sxs-lookup"><span data-stu-id="c25f6-295">Dynamics AX for Operations</span></span>

<span data-ttu-id="c25f6-296">このメソッドを移行する手順は、**LedgerJournalTrans\_AccountNum.loadSegments()** メソッドを移行する手順と同じです。</span><span class="sxs-lookup"><span data-stu-id="c25f6-296">The steps for migrating this method are the same as the steps for migrating the **LedgerJournalTrans\_AccountNum.loadSegments()** method.</span></span> <span data-ttu-id="c25f6-297">したがって、追加の手順は必要はありません。</span><span class="sxs-lookup"><span data-stu-id="c25f6-297">Therefore, no additional steps are required.</span></span> <span data-ttu-id="c25f6-298">このメソッドを削除します。</span><span class="sxs-lookup"><span data-stu-id="c25f6-298">Delete this method.</span></span>

#### <a name="step-3"></a><span data-ttu-id="c25f6-299">ステップ 3</span><span class="sxs-lookup"><span data-stu-id="c25f6-299">Step 3</span></span>

##### <a name="dynamics-ax-2012"></a><span data-ttu-id="c25f6-300">Dynamics AX 2012</span><span class="sxs-lookup"><span data-stu-id="c25f6-300">Dynamics AX 2012</span></span>

    /* TODO: (Code Upgrade) [Segmented entry control] Fix controller usage, if any, in this method based on the migration guidance */
    public void lookup()
    {
        if (!ledgerJournalEngine.accountNumLookup(ledgerJournalTrans_AccountNum1, ledgerJournalTrans))
        {
            super();
        }
    }

##### <a name="dynamics-ax-for-operations"></a><span data-ttu-id="c25f6-301">Dynamics AX for Operations</span><span class="sxs-lookup"><span data-stu-id="c25f6-301">Dynamics AX for Operations</span></span>

<span data-ttu-id="c25f6-302">このメソッドは、コントロールのカスタム ルックアップを実装します。</span><span class="sxs-lookup"><span data-stu-id="c25f6-302">This method implements a custom lookup for the control.</span></span> <span data-ttu-id="c25f6-303">したがって、メソッドをそのままにします。</span><span class="sxs-lookup"><span data-stu-id="c25f6-303">Therefore, leave the method as it is.</span></span> <span data-ttu-id="c25f6-304">"仕事" を削除します。</span><span class="sxs-lookup"><span data-stu-id="c25f6-304">Just remove the TODO.</span></span> <span data-ttu-id="c25f6-305">カスタムのルックアップをフック アップするには、SEC の **checkUseCustomLookup** メソッドをオーバーライドする必要があります。</span><span class="sxs-lookup"><span data-stu-id="c25f6-305">To hook up custom lookups, you must override the SEC’s **checkUseCustomLookup** method.</span></span> <span data-ttu-id="c25f6-306">また、カスタム ルックアップで **closeSelectRecord** メソッドが上書きされたことを確認してください。</span><span class="sxs-lookup"><span data-stu-id="c25f6-306">Additionally, make sure that the **closeSelectRecord** method on the custom lookup is overridden.</span></span> <span data-ttu-id="c25f6-307">例については、**CustTableLookup** フォームを参照してください。</span><span class="sxs-lookup"><span data-stu-id="c25f6-307">For an example, see the **CustTableLookup** form.</span></span>

#### <a name="step-4"></a><span data-ttu-id="c25f6-308">ステップ 4</span><span class="sxs-lookup"><span data-stu-id="c25f6-308">Step 4</span></span>

##### <a name="dynamics-ax-2012"></a><span data-ttu-id="c25f6-309">Dynamics AX 2012</span><span class="sxs-lookup"><span data-stu-id="c25f6-309">Dynamics AX 2012</span></span>

    /* TODO: (Code Upgrade) [Segmented entry control] For custom implementation, code in this method needs to be moved elsewhere based on the migration guidance */
    public void segmentValueChanged(SegmentValueChangedEventArgs _e)
    {
        super(_e);
        /* TODO: (Code Upgrade) [Segmented entry control] Replace this based on the migration guidance */
        // dimAccountController.segmentValueChanged(_e);
        currentMainAccountId = ledgerJournalEngine.onPrimaryAccountSegmentChanged(dimAccountController, currentMainAccountId, ledgerJournalTrans);
    }

##### <a name="dynamics-ax-for-operations"></a><span data-ttu-id="c25f6-310">Dynamics AX for Operations</span><span class="sxs-lookup"><span data-stu-id="c25f6-310">Dynamics AX for Operations</span></span>

1.  <span data-ttu-id="c25f6-311">コントロールの **onSegmentChanged()** メソッドをオーバーライドし、次のコードを追加します。</span><span class="sxs-lookup"><span data-stu-id="c25f6-311">Override the **onSegmentChanged()** method on the control, and add the following code to it.</span></span>

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

2.  <span data-ttu-id="c25f6-312">**segmentValueChanged()** メソッドを削除します。</span><span class="sxs-lookup"><span data-stu-id="c25f6-312">Delete the **segmentValueChanged()** method.</span></span> <span data-ttu-id="c25f6-313">**注記:** **onPrimaryAccountSegmentChanged()** メソッドでは、コントローラー オブジェクトが必要ですが、このコードは SEC のインスタンスを渡すので、**onSegmentChanged()** メソッドの前のコードはコンパイルされません。</span><span class="sxs-lookup"><span data-stu-id="c25f6-313">**Note:** The preceding code for the **onSegmentChanged()** method will not compile, because the **onPrimaryAccountSegmentChanged()** method expects a controller object, but this code passes an instance of the SEC.</span></span> <span data-ttu-id="c25f6-314">コントロール インスタンスでメソッドを呼び出すには、メソッドのシグネチャとその実装を適宜変更する必要があります。</span><span class="sxs-lookup"><span data-stu-id="c25f6-314">To call methods on the control instance, you must change the method’s signature and its implementation accordingly.</span></span> <span data-ttu-id="c25f6-315">このメソッドは、50 以上の呼び出し元が使用されます。</span><span class="sxs-lookup"><span data-stu-id="c25f6-315">This method is used by more than 50 callers.</span></span> <span data-ttu-id="c25f6-316">したがって、これらの呼び出しをすべて更新する必要があります。</span><span class="sxs-lookup"><span data-stu-id="c25f6-316">Therefore, you would also have to update all of those calls.</span></span> <span data-ttu-id="c25f6-317">または、このガイダンスに従うことによって新しいメソッドを追加できます。</span><span class="sxs-lookup"><span data-stu-id="c25f6-317">Alternatively, you can add a new method that follows this guidance.</span></span>

#### <a name="step-5"></a><span data-ttu-id="c25f6-318">ステップ 5</span><span class="sxs-lookup"><span data-stu-id="c25f6-318">Step 5</span></span>

##### <a name="dynamics-ax-2012"></a><span data-ttu-id="c25f6-319">Dynamics AX 2012</span><span class="sxs-lookup"><span data-stu-id="c25f6-319">Dynamics AX 2012</span></span>

    /* TODO: (Code Upgrade) [Segmented entry control] This method can be removed if there is no custom implementation */
    public boolean validate()
    {
        boolean isValid;
        isValid = super();
        /* TODO: (Code Upgrade) [Segmented entry control] This statement can be removed if there is no custom logic */
        // isValid = dimAccountController.validate() && isValid;
        return isValid;
    }

##### <a name="dynamics-ax-for-operations"></a><span data-ttu-id="c25f6-320">Dynamics AX for Operations</span><span class="sxs-lookup"><span data-stu-id="c25f6-320">Dynamics AX for Operations</span></span>

<span data-ttu-id="c25f6-321">このメソッドはコントロールの **validate()** メソッドのみを呼び出し追加の処理は実行しないため、削除できます。</span><span class="sxs-lookup"><span data-stu-id="c25f6-321">Because this method only calls the **validate()** method on the control and doesn't perform any additional processing, you can delete it.</span></span>

### <a name="ledgerjournaltrans_offsetaccount1"></a><span data-ttu-id="c25f6-322">LedgerJournalTrans\_OffsetAccount1</span><span class="sxs-lookup"><span data-stu-id="c25f6-322">LedgerJournalTrans\_OffsetAccount1</span></span>

<span data-ttu-id="c25f6-323">(**フォーム**タブの下にある検索バーで、「LedgerJournalTrans\_OffsetAccount1」を検索してください。)</span><span class="sxs-lookup"><span data-stu-id="c25f6-323">(Search for "LedgerJournalTrans\_OffsetAccount1" in the search bar below the **Form** tab.)</span></span>

#### <a name="step-1"></a><span data-ttu-id="c25f6-324">ステップ１</span><span class="sxs-lookup"><span data-stu-id="c25f6-324">Step 1</span></span>

##### <a name="dynamics-ax-2012"></a><span data-ttu-id="c25f6-325">Dynamics AX 2012</span><span class="sxs-lookup"><span data-stu-id="c25f6-325">Dynamics AX 2012</span></span>

    /* TODO: (Code Upgrade) [Segmented entry control] This method can be removed if there is no custom implementation */
    public void jumpRef()
    {
        GridOffsetAccount.jumpRef();
        LedgerJournalTrans_OffsetAccount1.jumpRef();
        Group4_OffsetAccount.jumpRef();
    }

##### <a name="dynamics-ax-for-operations"></a><span data-ttu-id="c25f6-326">Dynamics AX for Operations</span><span class="sxs-lookup"><span data-stu-id="c25f6-326">Dynamics AX for Operations</span></span>

<span data-ttu-id="c25f6-327">このメソッドはコントロールの **jumpRef()** メソッドのみを呼び出し追加の処理は実行しないため、削除できます。</span><span class="sxs-lookup"><span data-stu-id="c25f6-327">Because this method only calls the **jumpRef()** method on the control and doesn't perform any additional processing, you can delete it.</span></span>

#### <a name="step-2"></a><span data-ttu-id="c25f6-328">ステップ２</span><span class="sxs-lookup"><span data-stu-id="c25f6-328">Step 2</span></span>

##### <a name="dynamics-ax-2012"></a><span data-ttu-id="c25f6-329">Dynamics AX 2012</span><span class="sxs-lookup"><span data-stu-id="c25f6-329">Dynamics AX 2012</span></span>

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

##### <a name="dynamics-ax-for-operations"></a><span data-ttu-id="c25f6-330">Dynamics AX for Operations</span><span class="sxs-lookup"><span data-stu-id="c25f6-330">Dynamics AX for Operations</span></span>

<span data-ttu-id="c25f6-331">**GridOffsetAccount.loadSegments()** メソッドの移行手順は、すでにこのメソッドに必要な変更のほとんどを行いました。</span><span class="sxs-lookup"><span data-stu-id="c25f6-331">The migration steps for the **GridOffsetAccount.loadSegments()** method already made most of the changes that are required for this method.</span></span> <span data-ttu-id="c25f6-332">ただし、次の変更を加える必要があります。</span><span class="sxs-lookup"><span data-stu-id="c25f6-332">However, you must still make the following changes.</span></span>

1.  <span data-ttu-id="c25f6-333">**LedgerJournalTrans** データ ソースの**有効な**メソッドにコード行を追加します。</span><span class="sxs-lookup"><span data-stu-id="c25f6-333">Add a line of code to the **LedgerJournalTrans** data source’s **active** method.</span></span>

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

2.  <span data-ttu-id="c25f6-334">**LedgerJournalTrans** データ ソースの **OffsetAccountType** フィールドの **modified()** メソッドで同じ変更を行います。</span><span class="sxs-lookup"><span data-stu-id="c25f6-334">Make the same change in the **modified()** method of the **LedgerJournalTrans** data source’s **OffsetAccountType** field.</span></span>

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

3.  <span data-ttu-id="c25f6-335">**initLedger()** メソッドで同じ変更を行います。</span><span class="sxs-lookup"><span data-stu-id="c25f6-335">Make the same change in the **initLedger()** method.</span></span>

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

4.  <span data-ttu-id="c25f6-336">**loadSegments()** メソッドを削除します。</span><span class="sxs-lookup"><span data-stu-id="c25f6-336">Delete the **loadSegments()** method.</span></span>

#### <a name="step-3"></a><span data-ttu-id="c25f6-337">ステップ 3</span><span class="sxs-lookup"><span data-stu-id="c25f6-337">Step 3</span></span>

##### <a name="dynamics-ax-2012"></a><span data-ttu-id="c25f6-338">Dynamics AX 2012</span><span class="sxs-lookup"><span data-stu-id="c25f6-338">Dynamics AX 2012</span></span>

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

##### <a name="dynamics-ax-for-operations"></a><span data-ttu-id="c25f6-339">Dynamics AX for Operations</span><span class="sxs-lookup"><span data-stu-id="c25f6-339">Dynamics AX for Operations</span></span>

<span data-ttu-id="c25f6-340">このメソッドは、コントロールのカスタム ルックアップを実装します。</span><span class="sxs-lookup"><span data-stu-id="c25f6-340">This method implements a custom lookup for the control.</span></span> <span data-ttu-id="c25f6-341">したがって、メソッドを保持しますが、コントローラーをコントロール インスタンスに置き換えます。</span><span class="sxs-lookup"><span data-stu-id="c25f6-341">Therefore, keep the method, but replace the controller with the control instance.</span></span> <span data-ttu-id="c25f6-342">この場合、メソッドは **LedgerJournalTrans\_OffsetAccount1** コントロールでオーバーライドされるため、**dimOffsetAccountController** が (コントローラー変数宣言の "仕事" に示されたマッピングに基づいて) 3 つの異なる SEC インスタンスに使用される場合でも、コントローラーをたった 1 つの SEC インスタンスに置き換える必要があります。</span><span class="sxs-lookup"><span data-stu-id="c25f6-342">In this case, because the method is overridden on the **LedgerJournalTrans\_OffsetAccount1** control, even though **dimOffsetAccountController** was used for three different SEC instances (based on the mapping that is shown in the TODOs on controller variable declarations), we must replace the controller with only one SEC instance.</span></span> <span data-ttu-id="c25f6-343">したがって、コードは次のようになります。</span><span class="sxs-lookup"><span data-stu-id="c25f6-343">Therefore, the code will look like this.</span></span>

    public void lookup()
    {
        // Find the current segment index value
        int currentSegmentIndex = LedgerJournalTrans_OffsetAccount1.getCurrentSegmentIndex();
        if ((ledgerJournalTrans.OffsetAccountType == LedgerJournalACType::Ledger && LedgerJournalTrans_OffsetAccount1.getDimensionAttributeByControlIndex(currentSegmentIndex) != DimensionAttribute::getWellKnownDimensionAttribute(DimensionAttributeType::MainAccount)) || !ledgerJournalEngine.offsetAccountNumLookUp(ledgerJournalTrans_OffsetAccount1, ledgerJournalTrans))
        {
            super();
        }
    }

<span data-ttu-id="c25f6-344">カスタムのルックアップをフック アップするには、SEC の **checkUseCustomLookup** メソッドをオーバーライドする必要があります。</span><span class="sxs-lookup"><span data-stu-id="c25f6-344">To hook up custom lookups, you must override the SEC’s **checkUseCustomLookup** method.</span></span> <span data-ttu-id="c25f6-345">また、カスタム ルックアップ フォームで **closeSelectRecord** メソッドが上書きされたことを確認してください。</span><span class="sxs-lookup"><span data-stu-id="c25f6-345">Additionally, make sure that the **closeSelectRecord** method on the custom lookup form is overridden.</span></span> <span data-ttu-id="c25f6-346">例については、**CustTableLookup** フォームを参照してください。</span><span class="sxs-lookup"><span data-stu-id="c25f6-346">For an example, see the **CustTableLookup** form.</span></span>

#### <a name="step-4"></a><span data-ttu-id="c25f6-347">ステップ 4</span><span class="sxs-lookup"><span data-stu-id="c25f6-347">Step 4</span></span>

##### <a name="dynamics-ax-2012"></a><span data-ttu-id="c25f6-348">Dynamics AX 2012</span><span class="sxs-lookup"><span data-stu-id="c25f6-348">Dynamics AX 2012</span></span>

    /* TODO: (Code Upgrade) [Segmented entry control] For custom implementation, code in this method needs to be moved elsewhere based on the migration guidance */
    public void segmentValueChanged(SegmentValueChangedEventArgs _e)
    {
        super(_e);

        /* TODO: (Code Upgrade) [Segmented entry control] Replace this based on the migration guidance */
        // dimOffsetAccountController.segmentValueChanged(_e);
        currentOffsetMainAccountId = ledgerJournalEngine.onOffsetAccountSegmentChanged(dimOffsetAccountController, currentOffsetMainAccountId, ledgerJournalTrans);
    }

##### <a name="dynamics-ax-for-operations"></a><span data-ttu-id="c25f6-349">Dynamics AX for Operations</span><span class="sxs-lookup"><span data-stu-id="c25f6-349">Dynamics AX for Operations</span></span>

1.  <span data-ttu-id="c25f6-350">コントロールの **onSegmentChanged()** メソッドをオーバーライドし、次のコードを追加します。</span><span class="sxs-lookup"><span data-stu-id="c25f6-350">Override the **onSegmentChanged()** method on the control, and add the following code to it.</span></span>

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

2.  <span data-ttu-id="c25f6-351">**segmentValueChanged()** メソッドを削除します。</span><span class="sxs-lookup"><span data-stu-id="c25f6-351">Delete the **segmentValueChanged()** method.</span></span> <span data-ttu-id="c25f6-352">**注記:** **onOffsetAccountSegmentChanged()** メソッドでは、コントローラー オブジェクトが必要ですが、このコードは SEC のインスタンスを渡すので、**onSegmentChanged()** メソッドの前のコードはコンパイルされません。</span><span class="sxs-lookup"><span data-stu-id="c25f6-352">**Note:** The preceding code for the **onSegmentChanged()** method will not compile, because the **onOffsetAccountSegmentChanged()** method expects a controller object, but this code passes an instance of the SEC.</span></span> <span data-ttu-id="c25f6-353">コントロール インスタンスでメソッドを呼び出すには、メソッドのシグネチャとその実装を適宜変更する必要があります。</span><span class="sxs-lookup"><span data-stu-id="c25f6-353">To call methods on the control instance, you must change the method’s signature and its implementation accordingly.</span></span> <span data-ttu-id="c25f6-354">このメソッドは、50 以上の呼び出し元が使用されます。</span><span class="sxs-lookup"><span data-stu-id="c25f6-354">This method is used by more than 50 callers.</span></span> <span data-ttu-id="c25f6-355">したがって、これらの呼び出しをすべて更新する必要があります。</span><span class="sxs-lookup"><span data-stu-id="c25f6-355">Therefore, you would also have to update all those calls.</span></span> <span data-ttu-id="c25f6-356">または、このガイダンスに従うことによって新しいメソッドを追加できます。</span><span class="sxs-lookup"><span data-stu-id="c25f6-356">Alternatively, you can add a new method that follows this guidance.</span></span>

#### <a name="step-5"></a><span data-ttu-id="c25f6-357">ステップ 5</span><span class="sxs-lookup"><span data-stu-id="c25f6-357">Step 5</span></span>

##### <a name="dynamics-ax-2012"></a><span data-ttu-id="c25f6-358">Dynamics AX 2012</span><span class="sxs-lookup"><span data-stu-id="c25f6-358">Dynamics AX 2012</span></span>

    /* TODO: (Code Upgrade) [Segmented entry control] This method can be removed if there is no custom implementation */
    public boolean validate()
    {
        boolean isValid;
        isValid = super();

        /* TODO: (Code Upgrade) [Segmented entry control] This statement can be removed if there is no custom logic */
        // isValid = dimOffsetAccountController.validate() && isValid;
        return isValid;
    }

##### <a name="dynamics-ax-for-operations"></a><span data-ttu-id="c25f6-359">Dynamics AX for Operations</span><span class="sxs-lookup"><span data-stu-id="c25f6-359">Dynamics AX for Operations</span></span>

<span data-ttu-id="c25f6-360">このメソッドはコントロールの **validate()** メソッドのみを呼び出し追加の処理は実行しないため、削除できます。</span><span class="sxs-lookup"><span data-stu-id="c25f6-360">Because this method only calls the **validate()** method on the control and doesn't perform any additional processing, you can delete it.</span></span>

### <a name="custpaymjournalfee_custaccount"></a><span data-ttu-id="c25f6-361">CustPaymJournalFee\_CustAccount</span><span class="sxs-lookup"><span data-stu-id="c25f6-361">CustPaymJournalFee\_CustAccount</span></span>

<span data-ttu-id="c25f6-362">(**フォーム**タブの下にある検索バーで、「CustPaymJournalFee\_CustAccount」を検索してください。)</span><span class="sxs-lookup"><span data-stu-id="c25f6-362">(Search for "CustPaymJournalFee\_CustAccount" in the search bar below the **Form** tab.)</span></span>

#### <a name="step-1"></a><span data-ttu-id="c25f6-363">ステップ１</span><span class="sxs-lookup"><span data-stu-id="c25f6-363">Step 1</span></span>

##### <a name="dynamics-ax-2012"></a><span data-ttu-id="c25f6-364">Dynamics AX 2012</span><span class="sxs-lookup"><span data-stu-id="c25f6-364">Dynamics AX 2012</span></span>

    /* TODO: (Code Upgrade) [Segmented entry control] This method can be removed if there is no custom implementation */
    public void jumpRef()
    {
        CustPaymJournalFee_CustAccount.jumpRef();
    }

##### <a name="dynamics-ax-for-operations"></a><span data-ttu-id="c25f6-365">Dynamics AX for Operations</span><span class="sxs-lookup"><span data-stu-id="c25f6-365">Dynamics AX for Operations</span></span>

<span data-ttu-id="c25f6-366">このメソッドはコントロールの **jumpRef()** メソッドのみを呼び出し追加の処理は実行しないため、削除できます。</span><span class="sxs-lookup"><span data-stu-id="c25f6-366">Because this method only calls the **jumpRef()** method on the control and doesn't perform any additional processing, you can delete it.</span></span>

#### <a name="step-2"></a><span data-ttu-id="c25f6-367">ステップ２</span><span class="sxs-lookup"><span data-stu-id="c25f6-367">Step 2</span></span>

##### <a name="dynamics-ax-2012"></a><span data-ttu-id="c25f6-368">Dynamics AX 2012</span><span class="sxs-lookup"><span data-stu-id="c25f6-368">Dynamics AX 2012</span></span>

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

##### <a name="dynamics-ax-for-operations"></a><span data-ttu-id="c25f6-369">Dynamics AX for Operations</span><span class="sxs-lookup"><span data-stu-id="c25f6-369">Dynamics AX for Operations</span></span>

1.  <span data-ttu-id="c25f6-370">**initLedger()** メソッドを更新します。</span><span class="sxs-lookup"><span data-stu-id="c25f6-370">Update the **initLedger()** method.</span></span>

        ledgerJournalTable = element.args().record();
        journalNum = ledgerJournalTable.JournalNum;
        LedgerJournalTrans_AccountNum.parmJournalName(ledgerJournalTable.JournalName);
        LedgerJournalTrans_AccountNum1.parmJournalName(ledgerJournalTable.JournalName); Group4_AccountNum.parmJournalName(ledgerJournalTable.JournalName); CustPaymJournalFee_CustAccount.parmJournalName(ledgerJournalTable.JournalName);
        . . .

2.  <span data-ttu-id="c25f6-371">**CustVendPaymJournalFee** データ ソースの **active()** メソッドに、次のコードを追加します。</span><span class="sxs-lookup"><span data-stu-id="c25f6-371">Add the following code to the **CustVendPaymJournalFee** data source’s **active()** method.</span></span> <span data-ttu-id="c25f6-372">**注記:** このメソッドは存在しないため、上書きする必要があります。</span><span class="sxs-lookup"><span data-stu-id="c25f6-372">**Note:** The method doesn't exist, so you must override it.</span></span>

        CustPaymJournalFee_CustAccount.parmCurrency(custVendPaymJournalFee.FeeCurrency);

3.  <span data-ttu-id="c25f6-373">**CustVendPaymJournalFee** データ ソースの **FeeCurrency** フィールドの **modified()** メソッドに、次のコードを追加します。</span><span class="sxs-lookup"><span data-stu-id="c25f6-373">Add the following code to the **modified()** method of the **CustVendPaymJournalFee** data source’s **FeeCurrency** field.</span></span> <span data-ttu-id="c25f6-374">**注記:** このメソッドは存在しないため、上書きする必要があります。</span><span class="sxs-lookup"><span data-stu-id="c25f6-374">**Note:** The method doesn't exist, so you must override it.</span></span>

        CustPaymJournalFee_CustAccount.parmCurrency(custVendPaymJournalFee.FeeCurrency);

4.  <span data-ttu-id="c25f6-375">**LedgerJournalTrans** データ ソースの **active()** メソッドに、次のコードを追加します。</span><span class="sxs-lookup"><span data-stu-id="c25f6-375">Add the following code to the **LedgerJournalTrans** data source’s **active()** method.</span></span>

        CustPaymJournalFee_CustAccount.parmControlDate(ledgerJournalTrans.TransDate);

5.  <span data-ttu-id="c25f6-376">**LedgerJournalTrans** データ ソースの **TransDate** フィールドの **modified()** メソッドに、次のコードを追加します。</span><span class="sxs-lookup"><span data-stu-id="c25f6-376">Add the following code to the **modified()** method of the **LedgerJournalTrans** data source’s **TransDate** field.</span></span>

        CustPaymJournalFee_CustAccount.parmControlDate(ledgerJournalTrans.TransDate);

6.  <span data-ttu-id="c25f6-377">**loadSegments()** メソッドを削除します。</span><span class="sxs-lookup"><span data-stu-id="c25f6-377">Delete the **loadSegments()** method.</span></span>

#### <a name="step-3"></a><span data-ttu-id="c25f6-378">ステップ 3</span><span class="sxs-lookup"><span data-stu-id="c25f6-378">Step 3</span></span>

##### <a name="dynamics-ax-2012"></a><span data-ttu-id="c25f6-379">Dynamics AX 2012</span><span class="sxs-lookup"><span data-stu-id="c25f6-379">Dynamics AX 2012</span></span>

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

##### <a name="dynamics-ax-for-operations"></a><span data-ttu-id="c25f6-380">Dynamics AX for Operations</span><span class="sxs-lookup"><span data-stu-id="c25f6-380">Dynamics AX for Operations</span></span>

<span data-ttu-id="c25f6-381">このメソッドは、コントロールのカスタム ルックアップを実装します。</span><span class="sxs-lookup"><span data-stu-id="c25f6-381">This method implements a custom lookup for the control.</span></span> <span data-ttu-id="c25f6-382">したがって、メソッドをそのままにします。</span><span class="sxs-lookup"><span data-stu-id="c25f6-382">Therefore, leave the method as it is.</span></span> <span data-ttu-id="c25f6-383">"仕事" を削除します。</span><span class="sxs-lookup"><span data-stu-id="c25f6-383">Just remove the TODO.</span></span> <span data-ttu-id="c25f6-384">カスタムのルックアップをフック アップするには、SEC の **checkUseCustomLookup** メソッドをオーバーライドする必要があります。</span><span class="sxs-lookup"><span data-stu-id="c25f6-384">To hook up custom lookups, you must override the SEC’s **checkUseCustomLookup** method.</span></span> <span data-ttu-id="c25f6-385">次に例を示します。</span><span class="sxs-lookup"><span data-stu-id="c25f6-385">Here is an example.</span></span>

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

<span data-ttu-id="c25f6-386">また、カスタム ルックアップ フォームで **closeSelectRecord** メソッドが上書きされたことを確認してください。</span><span class="sxs-lookup"><span data-stu-id="c25f6-386">Additionally, make sure that the **closeSelectRecord** method on the custom lookup form is overridden.</span></span> <span data-ttu-id="c25f6-387">例については、**CustTableLookup** フォームを参照してください。</span><span class="sxs-lookup"><span data-stu-id="c25f6-387">For an example, see the **CustTableLookup** form.</span></span>

#### <a name="step-4"></a><span data-ttu-id="c25f6-388">ステップ 4</span><span class="sxs-lookup"><span data-stu-id="c25f6-388">Step 4</span></span>

##### <a name="dynamics-ax-2012"></a><span data-ttu-id="c25f6-389">Dynamics AX 2012</span><span class="sxs-lookup"><span data-stu-id="c25f6-389">Dynamics AX 2012</span></span>

    /* TODO: (Code Upgrade) [Segmented entry control] For custom implementation, code in this method needs to be moved elsewhere based on the migration guidance */
    public void segmentValueChanged(SegmentValueChangedEventArgs _e)
    {
        super(_e);

        /* TODO: (Code Upgrade) [Segmented entry control] Replace this based on the migration guidance */
        // dimPaymentFeeAccountController.segmentValueChanged(_e);
        currentPaymentFeeMainAccountId = ledgerJournalEngine.onPrimaryAccountSegmentChanged(dimPaymentFeeAccountController, currentPaymentFeeMainAccountId, ledgerJournalTrans);
    }

##### <a name="dynamics-ax-for-operations"></a><span data-ttu-id="c25f6-390">Dynamics AX for Operations</span><span class="sxs-lookup"><span data-stu-id="c25f6-390">Dynamics AX for Operations</span></span>

1.  <span data-ttu-id="c25f6-391">コントロールの **onSegmentChanged()** メソッドをオーバーライドし、次のコードを追加します。</span><span class="sxs-lookup"><span data-stu-id="c25f6-391">Override the **onSegmentChanged()** method on the control, and add the following code to it.</span></span>

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

2.  <span data-ttu-id="c25f6-392">**segmentValueChanged()** メソッドを削除します。</span><span class="sxs-lookup"><span data-stu-id="c25f6-392">Delete the **segmentValueChanged()** method.</span></span> <span data-ttu-id="c25f6-393">**注記:** **onPrimaryAccountSegmentChanged()** メソッドでは、コントローラー オブジェクトが必要ですが、このコードは SEC のインスタンスを渡すので、**onSegmentChanged()** メソッドの前のコードはコンパイルされません。</span><span class="sxs-lookup"><span data-stu-id="c25f6-393">**Note:** The preceding code for the **onSegmentChanged()** method will not compile, because the **onPrimaryAccountSegmentChanged()** method expects a controller object, but this code passes an instance of the SEC.</span></span> <span data-ttu-id="c25f6-394">コントロール インスタンスでメソッドを呼び出すには、メソッドのシグネチャとその実装を適宜変更する必要があります。</span><span class="sxs-lookup"><span data-stu-id="c25f6-394">To call methods on the control instance, you must change the method’s signature and its implementation accordingly.</span></span> <span data-ttu-id="c25f6-395">このメソッドは、50 以上の呼び出し元が使用されます。</span><span class="sxs-lookup"><span data-stu-id="c25f6-395">This method is used by more than 50 callers.</span></span> <span data-ttu-id="c25f6-396">したがって、これらの呼び出しをすべて更新する必要があります。</span><span class="sxs-lookup"><span data-stu-id="c25f6-396">Therefore, you would also have to update all those calls.</span></span> <span data-ttu-id="c25f6-397">または、このガイダンスの指示に従うことによって新しいメソッドを追加することができます。</span><span class="sxs-lookup"><span data-stu-id="c25f6-397">Alternatively, you can add a new method that can follow this guidance.</span></span>

#### <a name="step-5"></a><span data-ttu-id="c25f6-398">ステップ 5</span><span class="sxs-lookup"><span data-stu-id="c25f6-398">Step 5</span></span>

##### <a name="dynamics-ax-2012"></a><span data-ttu-id="c25f6-399">Dynamics AX 2012</span><span class="sxs-lookup"><span data-stu-id="c25f6-399">Dynamics AX 2012</span></span>

    /* TODO: (Code Upgrade) [Segmented entry control] This method can be removed if there is no custom implementation */
    public boolean validate()
    {
        boolean isValid;
        isValid = super();

        /* TODO: (Code Upgrade) [Segmented entry control] This statement can be removed if there is no custom logic */
        // isValid = dimPaymentFeeAccountController.validate() && isValid;
        return isValid;
    }

##### <a name="dynamics-ax-for-operations"></a><span data-ttu-id="c25f6-400">Dynamics AX for Operations</span><span class="sxs-lookup"><span data-stu-id="c25f6-400">Dynamics AX for Operations</span></span>

<span data-ttu-id="c25f6-401">このメソッドはコントロールの **validate()** メソッドのみを呼び出し追加の処理は実行しないため、削除できます。</span><span class="sxs-lookup"><span data-stu-id="c25f6-401">Because this method only calls the **validate()** method on the control and doesn't perform any additional processing, you can delete it.</span></span>

### <a name="group4_accountnum"></a><span data-ttu-id="c25f6-402">Group4\_AccountNum</span><span class="sxs-lookup"><span data-stu-id="c25f6-402">Group4\_AccountNum</span></span>

<span data-ttu-id="c25f6-403">(**フォーム**タブの下にある検索バーで「Group4\_AccountNum」を検索してください。)</span><span class="sxs-lookup"><span data-stu-id="c25f6-403">(Search for "Group4\_AccountNum" in the search bar below the **Form** tab.)</span></span>

#### <a name="step-1"></a><span data-ttu-id="c25f6-404">ステップ１</span><span class="sxs-lookup"><span data-stu-id="c25f6-404">Step 1</span></span>

##### <a name="dynamics-ax-2012"></a><span data-ttu-id="c25f6-405">Dynamics AX 2012</span><span class="sxs-lookup"><span data-stu-id="c25f6-405">Dynamics AX 2012</span></span>

    /* TODO: (Code Upgrade) [Segmented entry control] This method can be removed if there is no custom implementation */
    public void jumpRef()
    {
        LedgerJournalTrans_AccountNum.jumpRef();
        LedgerJournalTrans_AccountNum1.jumpRef();
        Group4_AccountNum.jumpRef();
    }

##### <a name="dynamics-ax-for-operations"></a><span data-ttu-id="c25f6-406">Dynamics AX for Operations</span><span class="sxs-lookup"><span data-stu-id="c25f6-406">Dynamics AX for Operations</span></span>

<span data-ttu-id="c25f6-407">このメソッドはコントロールの **jumpRef()** メソッドのみを呼び出し追加の処理は実行しないため、削除できます。</span><span class="sxs-lookup"><span data-stu-id="c25f6-407">Because this method only calls the **jumpRef()** method on the control and doesn't perform any additional processing, you can delete it.</span></span>

#### <a name="step-2"></a><span data-ttu-id="c25f6-408">ステップ２</span><span class="sxs-lookup"><span data-stu-id="c25f6-408">Step 2</span></span>

##### <a name="dynamics-ax-2012"></a><span data-ttu-id="c25f6-409">Dynamics AX 2012</span><span class="sxs-lookup"><span data-stu-id="c25f6-409">Dynamics AX 2012</span></span>

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

##### <a name="dynamics-ax-for-operations"></a><span data-ttu-id="c25f6-410">Dynamics AX for Operations</span><span class="sxs-lookup"><span data-stu-id="c25f6-410">Dynamics AX for Operations</span></span>

<span data-ttu-id="c25f6-411">このメソッドを移行する手順は、**LedgerJournalTrans\_AccountNum.loadSegments()** メソッドを移行する手順と同じです。</span><span class="sxs-lookup"><span data-stu-id="c25f6-411">The steps for migrating this method are the same as the steps for migrating the **LedgerJournalTrans\_AccountNum.loadSegments()** method.</span></span> <span data-ttu-id="c25f6-412">したがって、追加の手順は必要はありません。</span><span class="sxs-lookup"><span data-stu-id="c25f6-412">Therefore, no additional steps are required.</span></span> <span data-ttu-id="c25f6-413">このメソッドを削除します。</span><span class="sxs-lookup"><span data-stu-id="c25f6-413">Delete this method.</span></span>

#### <a name="step-3"></a><span data-ttu-id="c25f6-414">ステップ 3</span><span class="sxs-lookup"><span data-stu-id="c25f6-414">Step 3</span></span>

##### <a name="dynamics-ax-2012"></a><span data-ttu-id="c25f6-415">Dynamics AX 2012</span><span class="sxs-lookup"><span data-stu-id="c25f6-415">Dynamics AX 2012</span></span>

    /* TODO: (Code Upgrade) [Segmented entry control] Fix controller usage, if any, in this method based on the migration guidance */
    public void lookup()
    {
        if (!ledgerJournalEngine.accountNumLookup(group4_AccountNum, ledgerJournalTrans))
        {
            super();
        }
    }

##### <a name="dynamics-ax-for-operations"></a><span data-ttu-id="c25f6-416">Dynamics AX for Operations</span><span class="sxs-lookup"><span data-stu-id="c25f6-416">Dynamics AX for Operations</span></span>

<span data-ttu-id="c25f6-417">このメソッドは、コントロールのカスタム ルックアップを実装します。</span><span class="sxs-lookup"><span data-stu-id="c25f6-417">This method implements a custom lookup for the control.</span></span> <span data-ttu-id="c25f6-418">したがって、メソッドをそのままにします。</span><span class="sxs-lookup"><span data-stu-id="c25f6-418">Therefore, leave the method as it is.</span></span> <span data-ttu-id="c25f6-419">"仕事" を削除します。</span><span class="sxs-lookup"><span data-stu-id="c25f6-419">Just remove the TODO.</span></span> <span data-ttu-id="c25f6-420">カスタムのルックアップをフック アップするには、SEC の **checkUseCustomLookup** メソッドをオーバーライドする必要があります。</span><span class="sxs-lookup"><span data-stu-id="c25f6-420">To hook up custom lookups, you must override the SEC’s **checkUseCustomLookup** method.</span></span> <span data-ttu-id="c25f6-421">また、カスタム ルックアップ フォームで **closeSelectRecord** メソッドが上書きされたことを確認してください。</span><span class="sxs-lookup"><span data-stu-id="c25f6-421">Additionally, make sure that the **closeSelectRecord** method on the custom lookup form is overridden.</span></span> <span data-ttu-id="c25f6-422">例については、**CustTableLookup** フォームを参照してください。</span><span class="sxs-lookup"><span data-stu-id="c25f6-422">For an example, see the **CustTableLookup** form.</span></span>

#### <a name="step-4"></a><span data-ttu-id="c25f6-423">ステップ 4</span><span class="sxs-lookup"><span data-stu-id="c25f6-423">Step 4</span></span>

##### <a name="dynamics-ax-2012"></a><span data-ttu-id="c25f6-424">Dynamics AX 2012</span><span class="sxs-lookup"><span data-stu-id="c25f6-424">Dynamics AX 2012</span></span>

    /* TODO: (Code Upgrade) [Segmented entry control] For custom implementation, code in this method needs to be moved elsewhere based on the migration guidance */
    public void segmentValueChanged(SegmentValueChangedEventArgs _e)
    {
        super(_e);

        /* TODO: (Code Upgrade) [Segmented entry control] Replace this based on the migration guidance */
        // dimAccountController.segmentValueChanged(_e);
        currentMainAccountId = ledgerJournalEngine.onPrimaryAccountSegmentChanged(dimAccountController, currentMainAccountId, ledgerJournalTrans);
    }

##### <a name="dynamics-ax-for-operations"></a><span data-ttu-id="c25f6-425">Dynamics AX for Operations</span><span class="sxs-lookup"><span data-stu-id="c25f6-425">Dynamics AX for Operations</span></span>

1.  <span data-ttu-id="c25f6-426">コントロールの **onSegmentChanged()** メソッドをオーバーライドし、次のコードを追加します。</span><span class="sxs-lookup"><span data-stu-id="c25f6-426">Override the **onSegmentChanged()** method on the control, and add the following code to it.</span></span>

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

2.  <span data-ttu-id="c25f6-427">**segmentValueChanged()** メソッドを削除します。</span><span class="sxs-lookup"><span data-stu-id="c25f6-427">Delete the **segmentValueChanged()** method.</span></span> <span data-ttu-id="c25f6-428">**注記:** **onPrimaryAccountSegmentChanged()** メソッドでは、コントローラー オブジェクトが必要ですが、このコードは SEC のインスタンスを渡すので、**onSegmentChanged()** メソッドの前のコードはコンパイルされません。</span><span class="sxs-lookup"><span data-stu-id="c25f6-428">**Note:** The preceding code for the **onSegmentChanged()** method will not compile, because the **onPrimaryAccountSegmentChanged()** method expects a controller object, but this code passes an instance of the SEC.</span></span> <span data-ttu-id="c25f6-429">コントロール インスタンスでメソッドを呼び出すには、メソッドのシグネチャとその実装を適宜変更する必要があります。</span><span class="sxs-lookup"><span data-stu-id="c25f6-429">To call methods on the control instance, you must change the method’s signature and its implementation accordingly.</span></span> <span data-ttu-id="c25f6-430">このメソッドは、50 以上の呼び出し元が使用されます。</span><span class="sxs-lookup"><span data-stu-id="c25f6-430">This method is used by more than 50 callers.</span></span> <span data-ttu-id="c25f6-431">したがって、これらの呼び出しをすべて更新する必要があります。</span><span class="sxs-lookup"><span data-stu-id="c25f6-431">Therefore, you would also have to update all those calls.</span></span> <span data-ttu-id="c25f6-432">または、このガイダンスに従うことによって新しいメソッドを追加できます。</span><span class="sxs-lookup"><span data-stu-id="c25f6-432">Alternatively, you can add a new method that follows this guidance.</span></span>

#### <a name="step-5"></a><span data-ttu-id="c25f6-433">ステップ 5</span><span class="sxs-lookup"><span data-stu-id="c25f6-433">Step 5</span></span>

##### <a name="dynamics-ax-2012"></a><span data-ttu-id="c25f6-434">Dynamics AX 2012</span><span class="sxs-lookup"><span data-stu-id="c25f6-434">Dynamics AX 2012</span></span>

    /* TODO: (Code Upgrade) [Segmented entry control] This method can be removed if there is no custom implementation */
    public boolean validate()
    {
        boolean isValid;
        isValid = super();

        /* TODO: (Code Upgrade) [Segmented entry control] This statement can be removed if there is no custom logic */
        // isValid = dimAccountController.validate() && isValid;
        return isValid;
    }

##### <a name="dynamics-ax-for-operations"></a><span data-ttu-id="c25f6-435">Dynamics AX for Operations</span><span class="sxs-lookup"><span data-stu-id="c25f6-435">Dynamics AX for Operations</span></span>

<span data-ttu-id="c25f6-436">このメソッドはコントロールの **validate()** メソッドのみを呼び出し追加の処理は実行しないため、削除できます。</span><span class="sxs-lookup"><span data-stu-id="c25f6-436">Because this method only calls the **validate()** method on the control and doesn't perform any additional processing, you can delete it.</span></span>

### <a name="group4_offsetaccount"></a><span data-ttu-id="c25f6-437">Group4\_OffsetAccount</span><span class="sxs-lookup"><span data-stu-id="c25f6-437">Group4\_OffsetAccount</span></span>

<span data-ttu-id="c25f6-438">(**フォーム**タブの下にある検索バーで「Group4\_OffsetAccount」を検索してください。)</span><span class="sxs-lookup"><span data-stu-id="c25f6-438">(Search for "Group4\_OffsetAccount" in the search bar below the **Form** tab.)</span></span>

#### <a name="step-1"></a><span data-ttu-id="c25f6-439">ステップ１</span><span class="sxs-lookup"><span data-stu-id="c25f6-439">Step 1</span></span>

##### <a name="dynamics-ax-2012"></a><span data-ttu-id="c25f6-440">Dynamics AX 2012</span><span class="sxs-lookup"><span data-stu-id="c25f6-440">Dynamics AX 2012</span></span>

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

##### <a name="dynamics-ax-for-operations"></a><span data-ttu-id="c25f6-441">Dynamics AX for Operations</span><span class="sxs-lookup"><span data-stu-id="c25f6-441">Dynamics AX for Operations</span></span>

1.  <span data-ttu-id="c25f6-442">ledgerJournalTable バッファを更新するコードの後に、**initLedger()** メソッドのコードを更新します。</span><span class="sxs-lookup"><span data-stu-id="c25f6-442">Update the code in the **initLedger()** method, after the code that updates the ledgerJournalTable buffer.</span></span>

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

2.  <span data-ttu-id="c25f6-443">**gotFocus()** メソッドを削除します。</span><span class="sxs-lookup"><span data-stu-id="c25f6-443">Delete the **gotFocus()** method.</span></span>

#### <a name="step-2"></a><span data-ttu-id="c25f6-444">ステップ２</span><span class="sxs-lookup"><span data-stu-id="c25f6-444">Step 2</span></span>

##### <a name="dynamics-ax-2012"></a><span data-ttu-id="c25f6-445">Dynamics AX 2012</span><span class="sxs-lookup"><span data-stu-id="c25f6-445">Dynamics AX 2012</span></span>

    /* TODO: (Code Upgrade) [Segmented entry control] This method can be removed if there is no custom implementation */
    public void jumpRef()
    {
        GridOffsetAccount.jumpRef();
        LedgerJournalTrans_OffsetAccount1.jumpRef();
        Group4_OffsetAccount.jumpRef();
    }

##### <a name="dynamics-ax-for-operations"></a><span data-ttu-id="c25f6-446">Dynamics AX for Operations</span><span class="sxs-lookup"><span data-stu-id="c25f6-446">Dynamics AX for Operations</span></span>

<span data-ttu-id="c25f6-447">このメソッドはコントロールの **jumpRef()** メソッドのみを呼び出し追加の処理は実行しないため、削除できます。</span><span class="sxs-lookup"><span data-stu-id="c25f6-447">Because this method only calls the **jumpRef()** method on the control and doesn't perform any additional processing, you can delete it.</span></span>

#### <a name="step-3"></a><span data-ttu-id="c25f6-448">ステップ 3</span><span class="sxs-lookup"><span data-stu-id="c25f6-448">Step 3</span></span>

##### <a name="dynamics-ax-2012"></a><span data-ttu-id="c25f6-449">Dynamics AX 2012</span><span class="sxs-lookup"><span data-stu-id="c25f6-449">Dynamics AX 2012</span></span>

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

##### <a name="dynamics-ax-for-operations"></a><span data-ttu-id="c25f6-450">Dynamics AX for Operations</span><span class="sxs-lookup"><span data-stu-id="c25f6-450">Dynamics AX for Operations</span></span>

<span data-ttu-id="c25f6-451">**GridOffsetAccount.loadSegments()** メソッドの移行手順は、すでにこのメソッドに必要な変更のほとんどを行いました。</span><span class="sxs-lookup"><span data-stu-id="c25f6-451">The migration steps for the **GridOffsetAccount.loadSegments()** method already made most of the changes that are required for this method.</span></span> <span data-ttu-id="c25f6-452">ただし、次の変更を加える必要があります。</span><span class="sxs-lookup"><span data-stu-id="c25f6-452">However, you must still make the following changes.</span></span>

1.  <span data-ttu-id="c25f6-453">**LedgerJournalTrans** データ ソースの **active** メソッドでコードを更新します。</span><span class="sxs-lookup"><span data-stu-id="c25f6-453">Update the code in the **LedgerJournalTrans** data source’s **active** method.</span></span>

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

2.  <span data-ttu-id="c25f6-454">**LedgerJournalTrans** データ ソースの **OffsetAccountType** フィールドの **modified()** メソッドで同じ変更を行います。</span><span class="sxs-lookup"><span data-stu-id="c25f6-454">Make the same change in the **modified()** method of the **LedgerJournalTrans** data source’s **OffsetAccountType** field.</span></span>

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

3.  <span data-ttu-id="c25f6-455">**initLedger()** メソッドで同じ変更を行います。</span><span class="sxs-lookup"><span data-stu-id="c25f6-455">Make the same change in the **initLedger()** method.</span></span>

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

4.  <span data-ttu-id="c25f6-456">**loadSegments()** メソッドを削除します。</span><span class="sxs-lookup"><span data-stu-id="c25f6-456">Delete the **loadSegments()** method.</span></span>

#### <a name="step-4"></a><span data-ttu-id="c25f6-457">ステップ 4</span><span class="sxs-lookup"><span data-stu-id="c25f6-457">Step 4</span></span>

##### <a name="dynamics-ax-2012"></a><span data-ttu-id="c25f6-458">Dynamics AX 2012</span><span class="sxs-lookup"><span data-stu-id="c25f6-458">Dynamics AX 2012</span></span>

    /* TODO: (Code Upgrade) [Segmented entry control] Fix controller usage, if any, in this method based on the migration guidance */
    public void lookup()
    {
        if (!ledgerJournalEngine.offsetAccountNumLookUp(group4_OffsetAccount, ledgerJournalTrans))
        {
            super();
        }
    }

##### <a name="dynamics-ax-for-operations"></a><span data-ttu-id="c25f6-459">Dynamics AX for Operations</span><span class="sxs-lookup"><span data-stu-id="c25f6-459">Dynamics AX for Operations</span></span>

<span data-ttu-id="c25f6-460">このメソッドは、コントロールのカスタム ルックアップを実装します。</span><span class="sxs-lookup"><span data-stu-id="c25f6-460">This method implements a custom lookup for the control.</span></span> <span data-ttu-id="c25f6-461">したがって、メソッドをそのままにします。</span><span class="sxs-lookup"><span data-stu-id="c25f6-461">Therefore, leave the method as it is.</span></span> <span data-ttu-id="c25f6-462">"仕事" を削除します。</span><span class="sxs-lookup"><span data-stu-id="c25f6-462">Just remove the TODO.</span></span> <span data-ttu-id="c25f6-463">カスタムのルックアップをフック アップするには、SEC の **checkUseCustomLookup** メソッドをオーバーライドする必要があります。</span><span class="sxs-lookup"><span data-stu-id="c25f6-463">To hook up custom lookups, you must override the SEC’s **checkUseCustomLookup** method.</span></span> <span data-ttu-id="c25f6-464">また、カスタム ルックアップ フォームで **closeSelectRecord** メソッドが上書きされたことを確認してください。</span><span class="sxs-lookup"><span data-stu-id="c25f6-464">Additionally, make sure that the **closeSelectRecord** method on the custom lookup form is overridden.</span></span> <span data-ttu-id="c25f6-465">例については、**CustTableLookup** フォームを参照してください。</span><span class="sxs-lookup"><span data-stu-id="c25f6-465">For an example, see the **CustTableLookup** form.</span></span>

#### <a name="step-5"></a><span data-ttu-id="c25f6-466">ステップ 5</span><span class="sxs-lookup"><span data-stu-id="c25f6-466">Step 5</span></span>

##### <a name="dynamics-ax-2012"></a><span data-ttu-id="c25f6-467">Dynamics AX 2012</span><span class="sxs-lookup"><span data-stu-id="c25f6-467">Dynamics AX 2012</span></span>

    /* TODO: (Code Upgrade) [Segmented entry control] For custom implementation, code in this method needs to be moved elsewhere based on the migration guidance */
    public void segmentValueChanged(SegmentValueChangedEventArgs _e)
    {
        super(_e);

        /* TODO: (Code Upgrade) [Segmented entry control] Replace this based on the migration guidance */
        // dimOffsetAccountController.segmentValueChanged(_e);
        currentOffsetMainAccountId = ledgerJournalEngine.onOffsetAccountSegmentChanged(dimOffsetAccountController, currentOffsetMainAccountId, ledgerJournalTrans);
    }

##### <a name="dynamics-ax-for-operations"></a><span data-ttu-id="c25f6-468">Dynamics AX for Operations</span><span class="sxs-lookup"><span data-stu-id="c25f6-468">Dynamics AX for Operations</span></span>

1.  <span data-ttu-id="c25f6-469">コントロールの **onSegmentChanged()** メソッドをオーバーライドし、次のコードを追加します。</span><span class="sxs-lookup"><span data-stu-id="c25f6-469">Override the **onSegmentChanged()** method on the control, and add the following code to it.</span></span>

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

2.  <span data-ttu-id="c25f6-470">**segmentValueChanged()** メソッドを削除します。</span><span class="sxs-lookup"><span data-stu-id="c25f6-470">Delete the **segmentValueChanged()** method.</span></span> <span data-ttu-id="c25f6-471">**注記:** **onOffsetAccountSegmentChanged()** メソッドでは、コントローラー オブジェクトが必要ですが、このコードは SEC のインスタンスを渡すので、**onSegmentChanged()** メソッドの前のコードはコンパイルされません。</span><span class="sxs-lookup"><span data-stu-id="c25f6-471">**Note:** The preceding code for the **onSegmentChanged()** method will not compile, because the **onOffsetAccountSegmentChanged()** method expects a controller object, but this code passes an instance of the SEC.</span></span> <span data-ttu-id="c25f6-472">コントロール インスタンスでメソッドを呼び出すには、メソッドのシグネチャとその実装を適宜変更する必要があります。</span><span class="sxs-lookup"><span data-stu-id="c25f6-472">To call methods on the control instance, you must change the method’s signature and its implementation accordingly.</span></span> <span data-ttu-id="c25f6-473">このメソッドは、50 以上の呼び出し元が使用されます。</span><span class="sxs-lookup"><span data-stu-id="c25f6-473">This method is used by more than 50 callers.</span></span> <span data-ttu-id="c25f6-474">したがって、これらの呼び出しをすべて更新する必要があります。</span><span class="sxs-lookup"><span data-stu-id="c25f6-474">Therefore, you would also have to update all those calls.</span></span> <span data-ttu-id="c25f6-475">または、このガイダンスに従うことによって新しいメソッドを追加できます。</span><span class="sxs-lookup"><span data-stu-id="c25f6-475">Alternatively, you can add a new method that follows this guidance.</span></span>

#### <a name="step-6"></a><span data-ttu-id="c25f6-476">ステップ 6</span><span class="sxs-lookup"><span data-stu-id="c25f6-476">Step 6</span></span>

##### <a name="dynamics-ax-2012"></a><span data-ttu-id="c25f6-477">Dynamics AX 2012</span><span class="sxs-lookup"><span data-stu-id="c25f6-477">Dynamics AX 2012</span></span>

    /* TODO: (Code Upgrade) [Segmented entry control] This method can be removed if there is no custom implementation */
    public boolean validate()
    {
        boolean isValid;
        isValid = super();

        /* TODO: (Code Upgrade) [Segmented entry control] This statement can be removed if there is no custom logic */
        // isValid = dimOffsetAccountController.validate() && isValid;
        return isValid;
    }

##### <a name="dynamics-ax-for-operations"></a><span data-ttu-id="c25f6-478">Dynamics AX for Operations</span><span class="sxs-lookup"><span data-stu-id="c25f6-478">Dynamics AX for Operations</span></span>

<span data-ttu-id="c25f6-479">このメソッドはコントロールの **validate()** メソッドのみを呼び出し追加の処理は実行しないため、削除できます。</span><span class="sxs-lookup"><span data-stu-id="c25f6-479">Because this method only calls the **validate()** method on the control and doesn't perform any additional processing, you can delete it.</span></span>

<a name="additional-resources"></a><span data-ttu-id="c25f6-480">その他のリソース</span><span class="sxs-lookup"><span data-stu-id="c25f6-480">Additional resources</span></span>
--------

[<span data-ttu-id="c25f6-481">セグメント化されたエントリ コントロールのダイアログのサポート</span><span class="sxs-lookup"><span data-stu-id="c25f6-481">Segmented Entry control dialog support</span></span>](segmented-entry-control-dialog-support.md)

[<span data-ttu-id="c25f6-482">セグメント化されたエントリ コントロールのメタデータ詳細</span><span class="sxs-lookup"><span data-stu-id="c25f6-482">Segmented Entry control Metadata Specification</span></span>](segmented-entry-control-metadata-specification.md)

[<span data-ttu-id="c25f6-483">セグメント化されたエントリ コントロールの Parm メソッド詳細</span><span class="sxs-lookup"><span data-stu-id="c25f6-483">Segmented Entry control Parm method Specification</span></span>](segmented-entry-control-parm-method-specification.md)

[<span data-ttu-id="c25f6-484">セグメント化されたエントリ コントロール - 移行のガイダンス</span><span class="sxs-lookup"><span data-stu-id="c25f6-484">Segmented Entry control - Migration guidance</span></span>](segmented-entry-control-migration-guidance.md)



