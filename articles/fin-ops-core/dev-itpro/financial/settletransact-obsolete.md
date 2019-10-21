---
title: CustTrans::settleTransaction を使用したトランザクションの決済
description: このトピックでは、新しいCustTrans::settleTransactionメソッドについて説明を行い、CustTrans::settleTransact には実装されていない新機能について説明します。
author: RobinARH
manager: AnnBe
ms.date: 06/01/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Developer
ms.reviewer: rhaertle
ms.search.scope: Operations
ms.custom: 25631
ms.assetid: 0090efe3-3fd8-4988-83df-745d25b063d3
ms.search.region: Global
ms.author: markskun
ms.search.validFrom: 2019-06-01
ms.dyn365.ops.version: AX 10.0.4
ms.openlocfilehash: 1368d58d3d0dcaeefe4531ce40a49c499d5eeac9
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/27/2019
ms.locfileid: "2183298"
---
# <a name="settle-transactions-by-using-custtranssettletransaction"></a><span data-ttu-id="3cd8e-103">CustTrans::settleTransaction を使用したトランザクションの決済</span><span class="sxs-lookup"><span data-stu-id="3cd8e-103">Settle transactions by using CustTrans::settleTransaction</span></span>

[!include [banner](../includes/banner.md)]

[!include [banner](../includes/preview-banner.md)]

## <a name="custtranssettletransact-is-obsolete"></a><span data-ttu-id="3cd8e-104">CustTrans::settleTransact が過去のものに</span><span class="sxs-lookup"><span data-stu-id="3cd8e-104">CustTrans::settleTransact is obsolete</span></span>

<span data-ttu-id="3cd8e-105">CustTransテーブルの **settleTransact** メソッドが刷新されます。</span><span class="sxs-lookup"><span data-stu-id="3cd8e-105">The **settleTransact** method on the CustTrans table has been marked as obsolete.</span></span>

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

### <a name="why-is-it-marked-as-obsolete"></a><span data-ttu-id="3cd8e-106">なぜ刷新される必要があるのか。</span><span class="sxs-lookup"><span data-stu-id="3cd8e-106">Why is it marked as obsolete?</span></span>

<span data-ttu-id="3cd8e-107">同じ顧客に対して複数の決済が同時に行われると、データベースのブロックが発生します。</span><span class="sxs-lookup"><span data-stu-id="3cd8e-107">When many settlements are done at the same time for the same customer, database blocking occurs.</span></span> <span data-ttu-id="3cd8e-108">データベースのブロックはパフォーマンスの低下につながります。</span><span class="sxs-lookup"><span data-stu-id="3cd8e-108">Database blocking affects performance.</span></span>

### <a name="what-does-the-method-do"></a><span data-ttu-id="3cd8e-109">このメソッドによってできること</span><span class="sxs-lookup"><span data-stu-id="3cd8e-109">What does the method do?</span></span>

<span data-ttu-id="3cd8e-110">**settleTransact** メソッドでは、特定の顧客に対する一連の請求書と支払の決済を行います。</span><span class="sxs-lookup"><span data-stu-id="3cd8e-110">The **settleTransact** method settles a set of invoices and payments for a specific customer.</span></span> <span data-ttu-id="3cd8e-111">決済処理では、SpecTrans テーブルの **SpecCompany**、 **SpecTableId**、 **SpecRecId** 列を使用して一連の請求書を識別します。</span><span class="sxs-lookup"><span data-stu-id="3cd8e-111">Settlement identifies this set of invoices by using the **SpecCompany**, **SpecTableId**, and **SpecRecId** columns of the SpecTrans table.</span></span> <span data-ttu-id="3cd8e-112">同時に、これらの列によって決済コンテキストが定義されます。</span><span class="sxs-lookup"><span data-stu-id="3cd8e-112">Together, the columns define a settlement context.</span></span>

<span data-ttu-id="3cd8e-113">**settleTransact** メソッドの **\_custTable** パラメータが、決済コンテキストをCustTable **DataAreaId**, **TableId**, **RecId** の値として定義します。</span><span class="sxs-lookup"><span data-stu-id="3cd8e-113">The **\_custTable** parameter of the **settleTransact** method defines the settlement context as the CustTable **DataAreaId**, **TableId**, and **RecId** values.</span></span> <span data-ttu-id="3cd8e-114">次の例は、2つのコンテキストを示しています。</span><span class="sxs-lookup"><span data-stu-id="3cd8e-114">The following example shows two contexts.</span></span>

| <span data-ttu-id="3cd8e-115">SpecCompany</span><span class="sxs-lookup"><span data-stu-id="3cd8e-115">SpecCompany</span></span> | <span data-ttu-id="3cd8e-116">SpecTableId</span><span class="sxs-lookup"><span data-stu-id="3cd8e-116">SpecTableId</span></span> | <span data-ttu-id="3cd8e-117">SpecRecId</span><span class="sxs-lookup"><span data-stu-id="3cd8e-117">SpecRecId</span></span> | <span data-ttu-id="3cd8e-118">取引</span><span class="sxs-lookup"><span data-stu-id="3cd8e-118">Transaction</span></span> |
|---|---|---|---|
| <span data-ttu-id="3cd8e-119">USMF</span><span class="sxs-lookup"><span data-stu-id="3cd8e-119">USMF</span></span> | <span data-ttu-id="3cd8e-120">7589</span><span class="sxs-lookup"><span data-stu-id="3cd8e-120">7589</span></span> | <span data-ttu-id="3cd8e-121">22565451428</span><span class="sxs-lookup"><span data-stu-id="3cd8e-121">22565451428</span></span> | <span data-ttu-id="3cd8e-122">1</span><span class="sxs-lookup"><span data-stu-id="3cd8e-122">1</span></span> |
| <span data-ttu-id="3cd8e-123">USMF</span><span class="sxs-lookup"><span data-stu-id="3cd8e-123">USMF</span></span> | <span data-ttu-id="3cd8e-124">7589</span><span class="sxs-lookup"><span data-stu-id="3cd8e-124">7589</span></span> | <span data-ttu-id="3cd8e-125">22565451428</span><span class="sxs-lookup"><span data-stu-id="3cd8e-125">22565451428</span></span> | <span data-ttu-id="3cd8e-126">2</span><span class="sxs-lookup"><span data-stu-id="3cd8e-126">2</span></span> |

## <a name="replacement-method"></a><span data-ttu-id="3cd8e-127">メソッドの更新</span><span class="sxs-lookup"><span data-stu-id="3cd8e-127">Replacement method</span></span>

<span data-ttu-id="3cd8e-128">CustTrans テーブル **settleTransaction** メソッドが メソッドの更新を行います。</span><span class="sxs-lookup"><span data-stu-id="3cd8e-128">The **settleTransaction** method on the CustTrans table is the replacement method.</span></span>

```X++
public static boolean settleTransaction(
    SpecTransExecutionContext _specTransExecutionContext,
    CustTransSettleTransactionParameters _parameters)
```

### <a name="how-blocking-will-be-avoided"></a><span data-ttu-id="3cd8e-129">ブロックがどのように回避されるか</span><span class="sxs-lookup"><span data-stu-id="3cd8e-129">How blocking will be avoided</span></span>

<span data-ttu-id="3cd8e-130">それぞれの顧客の決済に固有の決済コンテキストが付与されます。</span><span class="sxs-lookup"><span data-stu-id="3cd8e-130">Every customer settlement will get a unique settlement context.</span></span> <span data-ttu-id="3cd8e-131">決済にはそれぞれ固有のコンテキストが割り当てられるため、どのトランザクションもブロックを引き起こすことがなくなります。</span><span class="sxs-lookup"><span data-stu-id="3cd8e-131">Because each settlement that is done will have a unique context, no transaction will cause blocking.</span></span>  <span data-ttu-id="3cd8e-132">次の例は、2つのコンテキストを示しています。</span><span class="sxs-lookup"><span data-stu-id="3cd8e-132">The following example shows two contexts.</span></span> <span data-ttu-id="3cd8e-133">各コンテキストには一意の **SpecRecId** 値を持っています。</span><span class="sxs-lookup"><span data-stu-id="3cd8e-133">Each context has a unique **SpecRecId** value.</span></span>

| <span data-ttu-id="3cd8e-134">SpecCompany</span><span class="sxs-lookup"><span data-stu-id="3cd8e-134">SpecCompany</span></span> | <span data-ttu-id="3cd8e-135">SpecTableId</span><span class="sxs-lookup"><span data-stu-id="3cd8e-135">SpecTableId</span></span> | <span data-ttu-id="3cd8e-136">SpecRecId</span><span class="sxs-lookup"><span data-stu-id="3cd8e-136">SpecRecId</span></span> | <span data-ttu-id="3cd8e-137">取引</span><span class="sxs-lookup"><span data-stu-id="3cd8e-137">Transaction</span></span> |
|---|---|---|---|
| <span data-ttu-id="3cd8e-138">USMF</span><span class="sxs-lookup"><span data-stu-id="3cd8e-138">USMF</span></span> | <span data-ttu-id="3cd8e-139">7599</span><span class="sxs-lookup"><span data-stu-id="3cd8e-139">7599</span></span> | <span data-ttu-id="3cd8e-140">68719604825</span><span class="sxs-lookup"><span data-stu-id="3cd8e-140">68719604825</span></span> | <span data-ttu-id="3cd8e-141">1</span><span class="sxs-lookup"><span data-stu-id="3cd8e-141">1</span></span> |
| <span data-ttu-id="3cd8e-142">USMF</span><span class="sxs-lookup"><span data-stu-id="3cd8e-142">USMF</span></span> | <span data-ttu-id="3cd8e-143">7599</span><span class="sxs-lookup"><span data-stu-id="3cd8e-143">7599</span></span> | <span data-ttu-id="3cd8e-144">68719604826</span><span class="sxs-lookup"><span data-stu-id="3cd8e-144">68719604826</span></span> | <span data-ttu-id="3cd8e-145">2</span><span class="sxs-lookup"><span data-stu-id="3cd8e-145">2</span></span> |
    
### <a name="replacement-method-parameters"></a><span data-ttu-id="3cd8e-146">メソッドのパラメーターを更新する</span><span class="sxs-lookup"><span data-stu-id="3cd8e-146">Replacement method parameters</span></span>

<span data-ttu-id="3cd8e-147">**SpecTransExecutionContext** クラスは、一意となる決済の実行コンテキストを定義します。</span><span class="sxs-lookup"><span data-stu-id="3cd8e-147">The **SpecTransExecutionContext** class defines a unique settlement execution context.</span></span> <span data-ttu-id="3cd8e-148">これは2つの部分で構成されています。</span><span class="sxs-lookup"><span data-stu-id="3cd8e-148">It has two parts.</span></span> <span data-ttu-id="3cd8e-149">一つ目の部分は、決済の顧客または仕入先を定義します。</span><span class="sxs-lookup"><span data-stu-id="3cd8e-149">The first part defines the customer or vendor for the settlement.</span></span> <span data-ttu-id="3cd8e-150">2つ目の部分では、決済のソースを定義します。</span><span class="sxs-lookup"><span data-stu-id="3cd8e-150">The second part defines the source for the settlement.</span></span>

+ <span data-ttu-id="3cd8e-151">**newFromSource** メソッドには、顧客、仕入先、およびソースが必要となります。</span><span class="sxs-lookup"><span data-stu-id="3cd8e-151">The **newFromSource** method takes a customer or vendor and a source.</span></span> <span data-ttu-id="3cd8e-152">顧客、仕入先、ソースは常に顧客となります。</span><span class="sxs-lookup"><span data-stu-id="3cd8e-152">The customer or vendor is always the customer, and the source is always the customer.</span></span>

    ```X++
    public static SpecTransExecutionContext newFromSource(
        CustVendTable _custVendTable, 
        Common _source = _custVendTable)
    ```

+ <span data-ttu-id="3cd8e-153">**parmSpecContext** メソッドは、生成された決済コンテキストを公開します。</span><span class="sxs-lookup"><span data-stu-id="3cd8e-153">The **parmSpecContext** method exposes the settlement context that is generated.</span></span>

    ```X++
    public Common parmSpecContext()
    ```

<span data-ttu-id="3cd8e-154">**CustTransSettleTransactionParamters** には、他のメソッドパラメータが含まれています。</span><span class="sxs-lookup"><span data-stu-id="3cd8e-154">**CustTransSettleTransactionParamters** contains the other method parameters.</span></span> <span data-ttu-id="3cd8e-155">これに含まれるコンストラクターメソッドは、既定値を使用してクラスの初期化を行います。</span><span class="sxs-lookup"><span data-stu-id="3cd8e-155">It has a constructor method that initializes the class with default values.</span></span> <span data-ttu-id="3cd8e-156">その一例として **LedgerVoucher** が挙げられます。</span><span class="sxs-lookup"><span data-stu-id="3cd8e-156">An example is **LedgerVoucher**.</span></span>

### <a name="how-to-use-the-settletransaction-method"></a><span data-ttu-id="3cd8e-157">settleTransaction メソッドの使用方法</span><span class="sxs-lookup"><span data-stu-id="3cd8e-157">How to use the settleTransaction method</span></span>

<span data-ttu-id="3cd8e-158">決済は2つの部分で行われます。</span><span class="sxs-lookup"><span data-stu-id="3cd8e-158">Settlement is done in two parts.</span></span> <span data-ttu-id="3cd8e-159">はじめに、決済処理に向けて請求書と支払を選び出します。</span><span class="sxs-lookup"><span data-stu-id="3cd8e-159">First, you mark the invoices and payments for settlement.</span></span> <span data-ttu-id="3cd8e-160">次に、決済処理を行います。</span><span class="sxs-lookup"><span data-stu-id="3cd8e-160">Then you do the settlement.</span></span>

#### <a name="obsolete-code-example"></a><span data-ttu-id="3cd8e-161">古いコードの例</span><span class="sxs-lookup"><span data-stu-id="3cd8e-161">Obsolete code example</span></span>

```X++
//Mark for settlement
SpecTransManager specTransManager = SpecTransManager::construct(custTable);

specTransManager.insert(…) //Invoice(s)
specTransManager.insert(…) //Payment(s)

//Settle
CustTrans::settleTransact(recipientCustVendTable);
```

#### <a name="new-code-example"></a><span data-ttu-id="3cd8e-162">新しいコードの例</span><span class="sxs-lookup"><span data-stu-id="3cd8e-162">New code example</span></span>

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

### <a name="testing"></a><span data-ttu-id="3cd8e-163">テスト</span><span class="sxs-lookup"><span data-stu-id="3cd8e-163">Testing</span></span>

<span data-ttu-id="3cd8e-164">この機能はフライトを使用します。</span><span class="sxs-lookup"><span data-stu-id="3cd8e-164">This functionality uses flights.</span></span> <span data-ttu-id="3cd8e-165">このテストを行うには、非稼働環境にてフライトを有効にする必要があります。</span><span class="sxs-lookup"><span data-stu-id="3cd8e-165">To test it, you must turn on the flight in a non-production environment.</span></span> <span data-ttu-id="3cd8e-166">非稼動環境でフライトをオンにする方法については、 [データ管理でフライトされる機能とフライトされた機能の有効化](../data-entities/data-entities-data-packages.md#features-flighted-in-data-management-and-enabling-flighted-features).を参照してください。</span><span class="sxs-lookup"><span data-stu-id="3cd8e-166">For information about how to turn on a flight in a non-production environment, see [Features flighted in data management and enabling flighted features](../data-entities/data-entities-data-packages.md#features-flighted-in-data-management-and-enabling-flighted-features).</span></span>

<span data-ttu-id="3cd8e-167">フライトの名称は **EnableCustTransSettleTransaction**です。</span><span class="sxs-lookup"><span data-stu-id="3cd8e-167">The name of the flight is **EnableCustTransSettleTransaction**.</span></span>
