---
title: CustTrans::settleTransaction を使用したトランザクションの決済
description: このトピックでは、新しいCustTrans::settleTransactionメソッドについて説明を行い、CustTrans::settleTransact には実装されていない新機能について説明します。
author: RobinARH
ms.date: 06/01/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Developer
ms.reviewer: rhaertle
ms.custom: 25631
ms.assetid: 0090efe3-3fd8-4988-83df-745d25b063d3
ms.search.region: Global
ms.author: markskun
ms.search.validFrom: 2019-06-01
ms.dyn365.ops.version: AX 10.0.4
ms.openlocfilehash: 5bfc178f2a7d8c86ad8e60ab38f14915afc6a6d6
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/31/2021
ms.locfileid: "5747973"
---
# <a name="settle-transactions-by-using-custtranssettletransaction"></a><span data-ttu-id="e99ec-103">CustTrans::settleTransaction を使用したトランザクションの決済</span><span class="sxs-lookup"><span data-stu-id="e99ec-103">Settle transactions by using CustTrans::settleTransaction</span></span>

[!include [banner](../includes/banner.md)]

[!include [banner](../includes/preview-banner.md)]

## <a name="custtranssettletransact-is-obsolete"></a><span data-ttu-id="e99ec-104">CustTrans::settleTransact が過去のものに</span><span class="sxs-lookup"><span data-stu-id="e99ec-104">CustTrans::settleTransact is obsolete</span></span>

<span data-ttu-id="e99ec-105">CustTransテーブルの **settleTransact** メソッドが刷新されます。</span><span class="sxs-lookup"><span data-stu-id="e99ec-105">The **settleTransact** method on the CustTrans table has been marked as obsolete.</span></span>

```X++
public static boolean settleTransact(
CustTable _custTable,
    LedgerVoucher _ledgerVoucher = null,
    boolean _balancePostingProfile = true,
    SettleDatePrinc _saveDatePrinciple = SettleDatePrinc::DateOfPayment,
    TransDate _saveDate = dateNull()
    ,DimSettlementType_RU _dimSettlementType = DimSettlementType_RU::None
    ,CustTrans _parentCustTrans = null)
```

### <a name="what-does-obsolete-mean"></a><span data-ttu-id="e99ec-106">廃止とはなにか?</span><span class="sxs-lookup"><span data-stu-id="e99ec-106">What does obsolete mean?</span></span>

<span data-ttu-id="e99ec-107">メソッドが廃止としてマークされている場合、コードが不要になり、最終的に製品から削除される予定ということです。</span><span class="sxs-lookup"><span data-stu-id="e99ec-107">When a method is marked as obsolete, it means the code is no longer required and we plan to eventually remove it from the product.</span></span> <span data-ttu-id="e99ec-108">多くの場合、廃止メソッドは使用できる代替メソッドを推奨します。</span><span class="sxs-lookup"><span data-stu-id="e99ec-108">The obsolete method will often recommend an alternative method that can be used.</span></span> <span data-ttu-id="e99ec-109">参照コードは、引き続き廃止メソッドと共に正常に動作します。</span><span class="sxs-lookup"><span data-stu-id="e99ec-109">The referencing code will continue to work as expected with the obsolete method.</span></span> <span data-ttu-id="e99ec-110">直接的なアクションは必要ありません。</span><span class="sxs-lookup"><span data-stu-id="e99ec-110">No immediate action is required.</span></span> <span data-ttu-id="e99ec-111">ただし、置換メソッドを使用するには、参照コードをリファクタリングする必要があります。</span><span class="sxs-lookup"><span data-stu-id="e99ec-111">But, referencing code should be refactored to use the replacement method.</span></span>

<span data-ttu-id="e99ec-112">廃止プロセスの詳細については、[メソッドおよびメタデータ要素の廃止](../migration-upgrade/deprecation-deletion-apis.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="e99ec-112">For more information about obsolete processes, see [Deprecation of methods and metadata elements](../migration-upgrade/deprecation-deletion-apis.md).</span></span>

### <a name="why-is-it-marked-as-obsolete"></a><span data-ttu-id="e99ec-113">なぜ刷新される必要があるのか。</span><span class="sxs-lookup"><span data-stu-id="e99ec-113">Why is it marked as obsolete?</span></span>

<span data-ttu-id="e99ec-114">同じ顧客に対して複数の決済が同時に行われると、データベースのブロックが発生します。</span><span class="sxs-lookup"><span data-stu-id="e99ec-114">When many settlements are done at the same time for the same customer, database blocking occurs.</span></span> <span data-ttu-id="e99ec-115">データベースのブロックはパフォーマンスの低下につながります。</span><span class="sxs-lookup"><span data-stu-id="e99ec-115">Database blocking affects performance.</span></span>

### <a name="what-does-the-method-do"></a><span data-ttu-id="e99ec-116">このメソッドによってできること</span><span class="sxs-lookup"><span data-stu-id="e99ec-116">What does the method do?</span></span>

<span data-ttu-id="e99ec-117">**settleTransact** メソッドでは、特定の顧客に対する一連の請求書と支払の決済を行います。</span><span class="sxs-lookup"><span data-stu-id="e99ec-117">The **settleTransact** method settles a set of invoices and payments for a specific customer.</span></span> <span data-ttu-id="e99ec-118">決済処理では、SpecTrans テーブルの **SpecCompany**、 **SpecTableId**、 **SpecRecId** 列を使用して一連の請求書を識別します。</span><span class="sxs-lookup"><span data-stu-id="e99ec-118">Settlement identifies this set of invoices by using the **SpecCompany**, **SpecTableId**, and **SpecRecId** columns of the SpecTrans table.</span></span> <span data-ttu-id="e99ec-119">同時に、これらの列によって決済コンテキストが定義されます。</span><span class="sxs-lookup"><span data-stu-id="e99ec-119">Together, the columns define a settlement context.</span></span>

<span data-ttu-id="e99ec-120">**settleTransact** メソッドの **\_custTable** パラメータが、決済コンテキストをCustTable **DataAreaId**, **TableId**, **RecId** の値として定義します。</span><span class="sxs-lookup"><span data-stu-id="e99ec-120">The **\_custTable** parameter of the **settleTransact** method defines the settlement context as the CustTable **DataAreaId**, **TableId**, and **RecId** values.</span></span> <span data-ttu-id="e99ec-121">次の例は、2つのコンテキストを示しています。</span><span class="sxs-lookup"><span data-stu-id="e99ec-121">The following example shows two contexts.</span></span>

| <span data-ttu-id="e99ec-122">SpecCompany</span><span class="sxs-lookup"><span data-stu-id="e99ec-122">SpecCompany</span></span> | <span data-ttu-id="e99ec-123">SpecTableId</span><span class="sxs-lookup"><span data-stu-id="e99ec-123">SpecTableId</span></span> | <span data-ttu-id="e99ec-124">SpecRecId</span><span class="sxs-lookup"><span data-stu-id="e99ec-124">SpecRecId</span></span> | <span data-ttu-id="e99ec-125">取引</span><span class="sxs-lookup"><span data-stu-id="e99ec-125">Transaction</span></span> |
|---|---|---|---|
| <span data-ttu-id="e99ec-126">USMF</span><span class="sxs-lookup"><span data-stu-id="e99ec-126">USMF</span></span> | <span data-ttu-id="e99ec-127">7589</span><span class="sxs-lookup"><span data-stu-id="e99ec-127">7589</span></span> | <span data-ttu-id="e99ec-128">22565451428</span><span class="sxs-lookup"><span data-stu-id="e99ec-128">22565451428</span></span> | <span data-ttu-id="e99ec-129">1</span><span class="sxs-lookup"><span data-stu-id="e99ec-129">1</span></span> |
| <span data-ttu-id="e99ec-130">USMF</span><span class="sxs-lookup"><span data-stu-id="e99ec-130">USMF</span></span> | <span data-ttu-id="e99ec-131">7589</span><span class="sxs-lookup"><span data-stu-id="e99ec-131">7589</span></span> | <span data-ttu-id="e99ec-132">22565451428</span><span class="sxs-lookup"><span data-stu-id="e99ec-132">22565451428</span></span> | <span data-ttu-id="e99ec-133">2</span><span class="sxs-lookup"><span data-stu-id="e99ec-133">2</span></span> |

## <a name="replacement-method"></a><span data-ttu-id="e99ec-134">メソッドの更新</span><span class="sxs-lookup"><span data-stu-id="e99ec-134">Replacement method</span></span>

<span data-ttu-id="e99ec-135">CustTrans テーブル **settleTransaction** メソッドが メソッドの更新を行います。</span><span class="sxs-lookup"><span data-stu-id="e99ec-135">The **settleTransaction** method on the CustTrans table is the replacement method.</span></span>

```X++
public static boolean settleTransaction(
    SpecTransExecutionContext _specTransExecutionContext,
    CustTransSettleTransactionParameters _parameters)
```

### <a name="how-blocking-will-be-avoided"></a><span data-ttu-id="e99ec-136">ブロックがどのように回避されるか</span><span class="sxs-lookup"><span data-stu-id="e99ec-136">How blocking will be avoided</span></span>

<span data-ttu-id="e99ec-137">それぞれの顧客の決済に固有の決済コンテキストが付与されます。</span><span class="sxs-lookup"><span data-stu-id="e99ec-137">Every customer settlement will get a unique settlement context.</span></span> <span data-ttu-id="e99ec-138">決済にはそれぞれ固有のコンテキストが割り当てられるため、どのトランザクションもブロックを引き起こすことがなくなります。</span><span class="sxs-lookup"><span data-stu-id="e99ec-138">Because each settlement that is done will have a unique context, no transaction will cause blocking.</span></span>  <span data-ttu-id="e99ec-139">次の例は、2つのコンテキストを示しています。</span><span class="sxs-lookup"><span data-stu-id="e99ec-139">The following example shows two contexts.</span></span> <span data-ttu-id="e99ec-140">各コンテキストには一意の **SpecRecId** 値を持っています。</span><span class="sxs-lookup"><span data-stu-id="e99ec-140">Each context has a unique **SpecRecId** value.</span></span>

| <span data-ttu-id="e99ec-141">SpecCompany</span><span class="sxs-lookup"><span data-stu-id="e99ec-141">SpecCompany</span></span> | <span data-ttu-id="e99ec-142">SpecTableId</span><span class="sxs-lookup"><span data-stu-id="e99ec-142">SpecTableId</span></span> | <span data-ttu-id="e99ec-143">SpecRecId</span><span class="sxs-lookup"><span data-stu-id="e99ec-143">SpecRecId</span></span> | <span data-ttu-id="e99ec-144">取引</span><span class="sxs-lookup"><span data-stu-id="e99ec-144">Transaction</span></span> |
|---|---|---|---|
| <span data-ttu-id="e99ec-145">USMF</span><span class="sxs-lookup"><span data-stu-id="e99ec-145">USMF</span></span> | <span data-ttu-id="e99ec-146">7599</span><span class="sxs-lookup"><span data-stu-id="e99ec-146">7599</span></span> | <span data-ttu-id="e99ec-147">68719604825</span><span class="sxs-lookup"><span data-stu-id="e99ec-147">68719604825</span></span> | <span data-ttu-id="e99ec-148">1</span><span class="sxs-lookup"><span data-stu-id="e99ec-148">1</span></span> |
| <span data-ttu-id="e99ec-149">USMF</span><span class="sxs-lookup"><span data-stu-id="e99ec-149">USMF</span></span> | <span data-ttu-id="e99ec-150">7599</span><span class="sxs-lookup"><span data-stu-id="e99ec-150">7599</span></span> | <span data-ttu-id="e99ec-151">68719604826</span><span class="sxs-lookup"><span data-stu-id="e99ec-151">68719604826</span></span> | <span data-ttu-id="e99ec-152">2</span><span class="sxs-lookup"><span data-stu-id="e99ec-152">2</span></span> |
    
### <a name="replacement-method-parameters"></a><span data-ttu-id="e99ec-153">メソッドのパラメーターを更新する</span><span class="sxs-lookup"><span data-stu-id="e99ec-153">Replacement method parameters</span></span>

<span data-ttu-id="e99ec-154">**SpecTransExecutionContext** クラスは、一意となる決済の実行コンテキストを定義します。</span><span class="sxs-lookup"><span data-stu-id="e99ec-154">The **SpecTransExecutionContext** class defines a unique settlement execution context.</span></span> <span data-ttu-id="e99ec-155">これは2つの部分で構成されています。</span><span class="sxs-lookup"><span data-stu-id="e99ec-155">It has two parts.</span></span> <span data-ttu-id="e99ec-156">一つ目の部分は、決済の顧客または仕入先を定義します。</span><span class="sxs-lookup"><span data-stu-id="e99ec-156">The first part defines the customer or vendor for the settlement.</span></span> <span data-ttu-id="e99ec-157">2つ目の部分では、決済のソースを定義します。</span><span class="sxs-lookup"><span data-stu-id="e99ec-157">The second part defines the source for the settlement.</span></span>

+ <span data-ttu-id="e99ec-158">**newFromSource** メソッドには、顧客、仕入先、およびソースが必要となります。</span><span class="sxs-lookup"><span data-stu-id="e99ec-158">The **newFromSource** method takes a customer or vendor and a source.</span></span> <span data-ttu-id="e99ec-159">顧客、仕入先、ソースは常に顧客となります。</span><span class="sxs-lookup"><span data-stu-id="e99ec-159">The customer or vendor is always the customer, and the source is always the customer.</span></span>

    ```X++
    public static SpecTransExecutionContext newFromSource(
        CustVendTable _custVendTable, 
        Common _source = _custVendTable)
    ```

+ <span data-ttu-id="e99ec-160">**parmSpecContext** メソッドは、生成された決済コンテキストを公開します。</span><span class="sxs-lookup"><span data-stu-id="e99ec-160">The **parmSpecContext** method exposes the settlement context that is generated.</span></span>

    ```X++
    public Common parmSpecContext()
    ```

<span data-ttu-id="e99ec-161">**CustTransSettleTransactionParamters** には、他のメソッドパラメータが含まれています。</span><span class="sxs-lookup"><span data-stu-id="e99ec-161">**CustTransSettleTransactionParamters** contains the other method parameters.</span></span> <span data-ttu-id="e99ec-162">これに含まれるコンストラクターメソッドは、既定値を使用してクラスの初期化を行います。</span><span class="sxs-lookup"><span data-stu-id="e99ec-162">It has a constructor method that initializes the class with default values.</span></span> <span data-ttu-id="e99ec-163">その一例として **LedgerVoucher** が挙げられます。</span><span class="sxs-lookup"><span data-stu-id="e99ec-163">An example is **LedgerVoucher**.</span></span>

### <a name="how-to-use-the-settletransaction-method"></a><span data-ttu-id="e99ec-164">settleTransaction メソッドの使用方法</span><span class="sxs-lookup"><span data-stu-id="e99ec-164">How to use the settleTransaction method</span></span>

<span data-ttu-id="e99ec-165">決済は2つの部分で行われます。</span><span class="sxs-lookup"><span data-stu-id="e99ec-165">Settlement is done in two parts.</span></span> <span data-ttu-id="e99ec-166">はじめに、決済処理に向けて請求書と支払を選び出します。</span><span class="sxs-lookup"><span data-stu-id="e99ec-166">First, you mark the invoices and payments for settlement.</span></span> <span data-ttu-id="e99ec-167">次に、決済処理を行います。</span><span class="sxs-lookup"><span data-stu-id="e99ec-167">Then you do the settlement.</span></span>

#### <a name="obsolete-code-example"></a><span data-ttu-id="e99ec-168">古いコードの例</span><span class="sxs-lookup"><span data-stu-id="e99ec-168">Obsolete code example</span></span>

```X++
//Mark for settlement
SpecTransManager specTransManager = SpecTransManager::construct(custTable);

specTransManager.insert(…) //Invoice(s)
specTransManager.insert(…) //Payment(s)

//Settle
CustTrans::settleTransact(recipientCustVendTable);
```

#### <a name="new-code-example"></a><span data-ttu-id="e99ec-169">新しいコードの例</span><span class="sxs-lookup"><span data-stu-id="e99ec-169">New code example</span></span>

```X++
//Mark for settlement
SpecTransExecutionContext specTransExecutionContext = SpecTransExecutionContext::newFromSource(custTable);
specTransManager = SpecTransManager::construct(specTransExecutionContext.parmSpecContext());

specTransManager.insert(…) //Invoice(s)
specTransManager.insert(…) //Payment(s)

//Settle
CustTrans::settleTransaction(
    specTransExecutionContext,
    CustTransSettleTransactionParameters::construct());
```

### <a name="testing"></a><span data-ttu-id="e99ec-170">テスト</span><span class="sxs-lookup"><span data-stu-id="e99ec-170">Testing</span></span>

<span data-ttu-id="e99ec-171">この機能はフライトを使用します。</span><span class="sxs-lookup"><span data-stu-id="e99ec-171">This functionality uses flights.</span></span> <span data-ttu-id="e99ec-172">このテストを行うには、非稼働環境にてフライトを有効にする必要があります。</span><span class="sxs-lookup"><span data-stu-id="e99ec-172">To test it, you must turn on the flight in a non-production environment.</span></span> <span data-ttu-id="e99ec-173">非稼動環境でフライトをオンにする方法については、[データ管理の概要](../data-entities/data-entities-data-packages.md#features-flighted-in-data-management-and-enabling-flighted-features).を参照してください。</span><span class="sxs-lookup"><span data-stu-id="e99ec-173">For information about how to turn on a flight in a non-production environment, see [Data management overview](../data-entities/data-entities-data-packages.md#features-flighted-in-data-management-and-enabling-flighted-features).</span></span>

<span data-ttu-id="e99ec-174">フライトの名称は **EnableCustTransSettleTransaction** です。</span><span class="sxs-lookup"><span data-stu-id="e99ec-174">The name of the flight is **EnableCustTransSettleTransaction**.</span></span>

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
