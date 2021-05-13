---
title: 税金が伝票の間違った勘定科目に転記される
description: このトピックでは、税金が伝票の間違った勘定科目に転記される際に役立つトラブルシューティング情報を提供します。
author: qire
manager: beya
ms.date: 04/12/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application user
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: wangchen
ms.search.validFrom: 2021-04-01
ms.dyn365.ops.version: 10.0.1
ms.openlocfilehash: 0404d71f0492e188ed5da62387bb90a336e69c5a
ms.sourcegitcommit: 57668404d61359b33e0c0280f2f7c4eb829b1ed2
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/27/2021
ms.locfileid: "5947669"
---
# <a name="tax-is-posted-to-the-wrong-ledger-account-in-the-voucher"></a><span data-ttu-id="2541e-103">税金が伝票の間違った勘定科目に転記される</span><span class="sxs-lookup"><span data-stu-id="2541e-103">Tax is posted to the wrong ledger account in the voucher</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="2541e-104">転記時に、税金が伝票の間違った勘定科目に転記される場合があります。</span><span class="sxs-lookup"><span data-stu-id="2541e-104">During posting, tax might be posted to the wrong ledger account in the voucher.</span></span> <span data-ttu-id="2541e-105">この問題のトラブルシューティングを行う場合は、必要に応じて次のセクションの手順に従います。</span><span class="sxs-lookup"><span data-stu-id="2541e-105">To troubleshoot this issue, follow the steps in the following sections as required.</span></span> <span data-ttu-id="2541e-106">このトピックの例では、販売注文をビジネス ドキュメントとして使用します。</span><span class="sxs-lookup"><span data-stu-id="2541e-106">The examples in this topic use a sales order as the business document.</span></span>

## <a name="find-the-tax-code-of-the-incorrectly-posted-tax-transaction"></a><span data-ttu-id="2541e-107">間違って転記された税トランザクションの税コードの検索</span><span class="sxs-lookup"><span data-stu-id="2541e-107">Find the tax code of the incorrectly posted tax transaction</span></span>

1. <span data-ttu-id="2541e-108">**伝票トランザクション** ページで、使用するトランザクションを選択し、**転記済消費税** を選択します。</span><span class="sxs-lookup"><span data-stu-id="2541e-108">On the **Voucher transactions** page, select the transaction that you want to work with, and then select **Posted sales tax**.</span></span>

    <span data-ttu-id="2541e-109">[![伝票トランザクション ページの転記済消費税ボタン](./media/tax-posted-to-wrong-ledger-account-Picture1.png)](./media/tax-posted-to-wrong-ledger-account-Picture1.png)</span><span class="sxs-lookup"><span data-stu-id="2541e-109">[![Posted sales tax button on the Voucher transactions page](./media/tax-posted-to-wrong-ledger-account-Picture1.png)](./media/tax-posted-to-wrong-ledger-account-Picture1.png)</span></span>

2. <span data-ttu-id="2541e-110">**消費税コード** フィールドの値を確認します。</span><span class="sxs-lookup"><span data-stu-id="2541e-110">Review the value in the **Sales tax code** field.</span></span> <span data-ttu-id="2541e-111">この例の場合、**VAT 19** です。</span><span class="sxs-lookup"><span data-stu-id="2541e-111">In this example, it's **VAT 19**.</span></span>

    <span data-ttu-id="2541e-112">[![転記済消費税ページの消費税コード フィールド](./media/tax-posted-to-wrong-ledger-account-Picture2.png)](./media/tax-posted-to-wrong-ledger-account-Picture2.png)</span><span class="sxs-lookup"><span data-stu-id="2541e-112">[![Sales tax code field on the Posted sales tax page](./media/tax-posted-to-wrong-ledger-account-Picture2.png)](./media/tax-posted-to-wrong-ledger-account-Picture2.png)</span></span>

## <a name="check-the-ledger-posting-group-of-the-tax-code"></a><span data-ttu-id="2541e-113">税コードの元帳転記グループの確認</span><span class="sxs-lookup"><span data-stu-id="2541e-113">Check the ledger posting group of the tax code</span></span>

1. <span data-ttu-id="2541e-114">**税** \> **間接税** \> **消費税** \> **消費税コード** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="2541e-114">Go to **Tax** \> **Indirect taxes** \> **Sales tax** \> **Sales tax codes**.</span></span>
2. <span data-ttu-id="2541e-115">税コードを検索して選択し、**元帳転記グループ** フィールドの値を確認します。</span><span class="sxs-lookup"><span data-stu-id="2541e-115">Find and select the tax code, and then review the value in the **Ledger posting group** field.</span></span> <span data-ttu-id="2541e-116">この例の場合、**VAT** です。</span><span class="sxs-lookup"><span data-stu-id="2541e-116">In this example, it's **VAT**.</span></span>

    <span data-ttu-id="2541e-117">[![消費税コード ページの元帳転記グループ フィールド](./media/tax-posted-to-wrong-ledger-account-Picture3.png)](./media/tax-posted-to-wrong-ledger-account-Picture3.png)</span><span class="sxs-lookup"><span data-stu-id="2541e-117">[![Ledger posting group field on the Sales tax codes page](./media/tax-posted-to-wrong-ledger-account-Picture3.png)](./media/tax-posted-to-wrong-ledger-account-Picture3.png)</span></span>

3. <span data-ttu-id="2541e-118">**元帳転記グループ** フィールドの値は、リンクです。</span><span class="sxs-lookup"><span data-stu-id="2541e-118">The value in the **Ledger posting group** field is a link.</span></span> <span data-ttu-id="2541e-119">グループのコンフィギュレーションの詳細を表示するには、リンクを選択します。</span><span class="sxs-lookup"><span data-stu-id="2541e-119">To view the details of the group's configuration, select the link.</span></span> <span data-ttu-id="2541e-120">または、フィールドを選択したまま (または右クリック) にして、**詳細の表示** を選択します。</span><span class="sxs-lookup"><span data-stu-id="2541e-120">Alternatively, select and hold (or right-click) in the field, and then select **View details**.</span></span>

    <span data-ttu-id="2541e-121">[![詳細を表示コマンド](./media/tax-posted-to-wrong-ledger-account-Picture4.png)](./media/tax-posted-to-wrong-ledger-account-Picture4.png)</span><span class="sxs-lookup"><span data-stu-id="2541e-121">[![View details command](./media/tax-posted-to-wrong-ledger-account-Picture4.png)](./media/tax-posted-to-wrong-ledger-account-Picture4.png)</span></span>

4. <span data-ttu-id="2541e-122">**消費税支払** フィールドで、トランザクション タイプに従って勘定番号が正しいか確認します。</span><span class="sxs-lookup"><span data-stu-id="2541e-122">In the **Sales tax payable** field, verify that the account number is correct, according to the transaction type.</span></span> <span data-ttu-id="2541e-123">正しくない場合は、転記する適切な勘定を選択します。</span><span class="sxs-lookup"><span data-stu-id="2541e-123">If it isn't, select the correct account to post to.</span></span> <span data-ttu-id="2541e-124">この例では、販売注文の消費税は消費税支払の勘定 222200 に転記されます。</span><span class="sxs-lookup"><span data-stu-id="2541e-124">In this example, the sales tax of the sales order should be posted to sales tax payable account 222200.</span></span>

    <span data-ttu-id="2541e-125">[![元帳転記グループ ページの消費税支払フィールド](./media/tax-posted-to-wrong-ledger-account-Picture5.png)](./media/tax-posted-to-wrong-ledger-account-Picture5.png)</span><span class="sxs-lookup"><span data-stu-id="2541e-125">[![Sales tax payable field on the Ledger posting groups page](./media/tax-posted-to-wrong-ledger-account-Picture5.png)](./media/tax-posted-to-wrong-ledger-account-Picture5.png)</span></span>

    <span data-ttu-id="2541e-126">次の表に、**元帳転記グループ** ページの各フィールドに関する情報を示します。</span><span class="sxs-lookup"><span data-stu-id="2541e-126">The following table provides information about each field on the **Ledger posting groups** page.</span></span>

    | <span data-ttu-id="2541e-127">フィールド</span><span class="sxs-lookup"><span data-stu-id="2541e-127">Field</span></span>                  | <span data-ttu-id="2541e-128">説明</span><span class="sxs-lookup"><span data-stu-id="2541e-128">Description</span></span> |
    |------------------------|-------------|
    | <span data-ttu-id="2541e-129">消費税支払</span><span class="sxs-lookup"><span data-stu-id="2541e-129">Sales tax payable</span></span>      | <span data-ttu-id="2541e-130">税務当局に消費税を支払う主勘定。</span><span class="sxs-lookup"><span data-stu-id="2541e-130">The main account for outgoing sales taxes that are payable to the tax authority.</span></span> |
    | <span data-ttu-id="2541e-131">消費税収入</span><span class="sxs-lookup"><span data-stu-id="2541e-131">Sales tax receivable</span></span>   | <span data-ttu-id="2541e-132">税務当局から税金を受け取る主勘定。</span><span class="sxs-lookup"><span data-stu-id="2541e-132">The main account for incoming taxes that are received from the tax authority.</span></span> |
    | <span data-ttu-id="2541e-133">使用税経費</span><span class="sxs-lookup"><span data-stu-id="2541e-133">Use tax expense</span></span>        | <span data-ttu-id="2541e-134">仕入先が、欧州連合 (EU) の逆請求の商品及びサービス税 (GST) または統合売上税 (HST) の一部として税務当局に申告または報告しない、控除可能な使用税を転記するために使用する主勘定。</span><span class="sxs-lookup"><span data-stu-id="2541e-134">The main account that is used to post deductible use taxes that vendors don't claim or report to the tax authority as part of European Union (EU) reverse charge Goods and Services Tax (GST)/Harmonized Sales Tax (HST).</span></span> <span data-ttu-id="2541e-135">**使用税** は、トランザクションに使用する消費税グループの消費税コードに対して選択する必要があります。</span><span class="sxs-lookup"><span data-stu-id="2541e-135">**Use tax** must be selected for the sales tax code in the sales tax group that is used in the transaction.</span></span> <span data-ttu-id="2541e-136">このフィールドは、**総勘定元帳のパラメーター** ページの **売上税課税ルールの適用** が選択されている場合には使用できません。</span><span class="sxs-lookup"><span data-stu-id="2541e-136">This field isn't available if **Apply sales tax taxation rules** is selected on the **General ledger parameters** page.</span></span> |
    | <span data-ttu-id="2541e-137">使用税支払勘定</span><span class="sxs-lookup"><span data-stu-id="2541e-137">Use tax payable</span></span>        | <span data-ttu-id="2541e-138">税務当局に支払う使用税を転記するために使用する主勘定。</span><span class="sxs-lookup"><span data-stu-id="2541e-138">The main account that is used to post incoming use taxes that are payable to tax authorities.</span></span> |
    | <span data-ttu-id="2541e-139">決済勘定</span><span class="sxs-lookup"><span data-stu-id="2541e-139">Settlement account</span></span>     | <span data-ttu-id="2541e-140">**使用税支払勘定** および **消費税収入** フィールドで指定された勘定科目の正味残高を転記するために使用する主勘定。</span><span class="sxs-lookup"><span data-stu-id="2541e-140">The main account that is used to post the net balance of the ledger accounts that are specified in the **Use tax payable** and **Sales tax receivable** fields.</span></span> |
    | <span data-ttu-id="2541e-141">仕入先現金割引</span><span class="sxs-lookup"><span data-stu-id="2541e-141">Vendor cash discount</span></span>   | <span data-ttu-id="2541e-142">この元帳転記グループと関連付けられた消費税コードについての現金割引を転記するために使用する主勘定。</span><span class="sxs-lookup"><span data-stu-id="2541e-142">The main account that is used to post a cash discount for sales tax codes that are associated with this ledger posting group.</span></span> |
    | <span data-ttu-id="2541e-143">顧客現金割引</span><span class="sxs-lookup"><span data-stu-id="2541e-143">Customer case discount</span></span> | <span data-ttu-id="2541e-144">この元帳転記グループと関連付けられた消費税コードについての現金割引を転記するために使用する主勘定。</span><span class="sxs-lookup"><span data-stu-id="2541e-144">The main account that is used to post a cash discount for sales tax codes that are associated with this ledger posting group.</span></span> |

    <span data-ttu-id="2541e-145">詳細については、[売上税の元帳転記グループの設定](tasks/set-up-ledger-posting-groups-sales-tax.md)を参照してください</span><span class="sxs-lookup"><span data-stu-id="2541e-145">For more information, see, [Set up Ledger posting groups for sales tax](tasks/set-up-ledger-posting-groups-sales-tax.md)</span></span>

## <a name="debug-in-code-to-check-ledger-dimensions"></a><span data-ttu-id="2541e-146">コードをデバッグして勘定分析コードを確認する</span><span class="sxs-lookup"><span data-stu-id="2541e-146">Debug in code to check ledger dimensions</span></span>

<span data-ttu-id="2541e-147">このコードでは、転記勘定は勘定分析コードによって決まります。</span><span class="sxs-lookup"><span data-stu-id="2541e-147">In the code, the posting account is determined by the ledger dimension.</span></span> <span data-ttu-id="2541e-148">勘定分析コードは、勘定のレコード ID をデータベースに保存します。</span><span class="sxs-lookup"><span data-stu-id="2541e-148">The ledger dimension saves the record ID of an account in the database.</span></span>

1. <span data-ttu-id="2541e-149">販売注文の場合、**Tax::saveAndPost()** および **Tax::post()** メソッドにブレークポイントを追加します。</span><span class="sxs-lookup"><span data-stu-id="2541e-149">For a sales order, add a breakpoint at the **Tax::saveAndPost()** and **Tax::post()** methods.</span></span> <span data-ttu-id="2541e-150">**\_ledgerDimension** の値に注意してください。</span><span class="sxs-lookup"><span data-stu-id="2541e-150">Pay attention to the value of **\_ledgerDimension**.</span></span>

    <span data-ttu-id="2541e-151">[![ブレークポイントが設定された販売注文コード サンプル](./media/tax-posted-to-wrong-ledger-account-Picture6.png)](./media/tax-posted-to-wrong-ledger-account-Picture6.png)</span><span class="sxs-lookup"><span data-stu-id="2541e-151">[![Sales order code sample that has a breakpoint](./media/tax-posted-to-wrong-ledger-account-Picture6.png)](./media/tax-posted-to-wrong-ledger-account-Picture6.png)</span></span>

    <span data-ttu-id="2541e-152">発注書の場合は、**TaxPost::saveAndPost()** および **TaxPost::postToTaxTrans()** メソッドにブレークポイントを追加します。</span><span class="sxs-lookup"><span data-stu-id="2541e-152">For a purchase order, add a breakpoint at the **TaxPost::saveAndPost()** and **TaxPost::postToTaxTrans()** methods.</span></span> <span data-ttu-id="2541e-153">**\_ledgerDimension** の値に注意してください。</span><span class="sxs-lookup"><span data-stu-id="2541e-153">Pay attention to the value of **\_ledgerDimension**.</span></span>

    <span data-ttu-id="2541e-154">[![ブレークポイントが設定された発注書コード サンプル](./media/tax-posted-to-wrong-ledger-account-Picture7.png)](./media/tax-posted-to-wrong-ledger-account-Picture7.png)</span><span class="sxs-lookup"><span data-stu-id="2541e-154">[![Purchase order code sample that has a breakpoint](./media/tax-posted-to-wrong-ledger-account-Picture7.png)](./media/tax-posted-to-wrong-ledger-account-Picture7.png)</span></span>

2. <span data-ttu-id="2541e-155">次の SQL クエリを実行して、勘定分析コードで保存されるレコード ID に基づいて、データベース内の勘定の表示値を検索します。</span><span class="sxs-lookup"><span data-stu-id="2541e-155">Run the following SQL query to find the display value of the account in the database, based on the record ID that is saved by the ledger dimension.</span></span>

    ```sql
    select * from DIMENSIONATTRIBUTEVALUECOMBINATION where recid={the value of _ledgerDimension}
    ```

    <span data-ttu-id="2541e-156">[![レコード ID の表示値](./media/tax-posted-to-wrong-ledger-account-Picture8.png)](./media/tax-posted-to-wrong-ledger-account-Picture8.png)</span><span class="sxs-lookup"><span data-stu-id="2541e-156">[![Display value of the record ID](./media/tax-posted-to-wrong-ledger-account-Picture8.png)](./media/tax-posted-to-wrong-ledger-account-Picture8.png)</span></span>

3. <span data-ttu-id="2541e-157">コール スタックを確認して、**_ledgerDimension** の値が割り当てられている場所を検索します。</span><span class="sxs-lookup"><span data-stu-id="2541e-157">Examine the callstack to find where the **_ledgerDimension** value is assigned.</span></span> <span data-ttu-id="2541e-158">通常、この値は **TmpTaxWorkTrans** から取得されます。</span><span class="sxs-lookup"><span data-stu-id="2541e-158">Usually, the value is from **TmpTaxWorkTrans**.</span></span> <span data-ttu-id="2541e-159">この場合、**TmpTaxWorkTrans::insert()** および **TmpTaxWorkTrans::update()** にブレークポイントを追加して、値が割り当てられている場所を検索する必要があります。</span><span class="sxs-lookup"><span data-stu-id="2541e-159">In this case, you should add a breakpoint at **TmpTaxWorkTrans::insert()** and **TmpTaxWorkTrans::update()** to find where the value assigned.</span></span>

## <a name="determine-whether-customization-exists"></a><span data-ttu-id="2541e-160">カスタマイズが存在するかどうかの確認</span><span class="sxs-lookup"><span data-stu-id="2541e-160">Determine whether customization exists</span></span>

<span data-ttu-id="2541e-161">前のセクションの手順を完了し、問題が見つからなかった場合は、カスタマイズが存在するかどうかを確認します。</span><span class="sxs-lookup"><span data-stu-id="2541e-161">If you've completed the steps in the previous sections but have found no issue, determine whether customization exists.</span></span> <span data-ttu-id="2541e-162">カスタマイズが存在しない場合、さらにサポートを受けるために Microsoft サービス要求を作成します。</span><span class="sxs-lookup"><span data-stu-id="2541e-162">If no customization exists, create a Microsoft service request for further support.</span></span>

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
