---
title: EventHandlerResult を使用して応答
description: このトピックでは、IEventHandlerResult インターフェイスを実装する任意の型パラメーターを持つイベントをサブスクライブする方法について説明します。
author: MichaelFruergaardPontoppidan
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Developer
ms.reviewer: rhaertle
ms.custom: 89563
ms.assetid: ''
ms.search.region: Global
ms.author: mfp
ms.search.validFrom: 2017-07-01
ms.dyn365.ops.version: Platform update 9
ms.openlocfilehash: c11dbc0e82c27952e0defc689d6f80bde1be235e
ms.sourcegitcommit: 74e47075eab2b0b28f82b0d57f439719847ecb01
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/07/2021
ms.locfileid: "6193091"
---
# <a name="respond-by-using-eventhandlerresult"></a><span data-ttu-id="3ab53-103">EventHandlerResult を使用して応答</span><span class="sxs-lookup"><span data-stu-id="3ab53-103">Respond by using EventHandlerResult</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="3ab53-104">いくつかのデリゲート メソッドは、デリゲート ハンドラー メソッドのサブスクライブから応答を要求できるように実装されます。</span><span class="sxs-lookup"><span data-stu-id="3ab53-104">Some delegate methods are implemented so that they can request a response from subscribing delegate handler methods.</span></span> <span data-ttu-id="3ab53-105">デリゲート呼び出しロジックは、応答の受信後に実行を継続するときに潜在的なサブスクライバからの応答を使用します。</span><span class="sxs-lookup"><span data-stu-id="3ab53-105">The delegate calling logic then uses the response from a potential subscriber when it continues execution after the response has been received.</span></span> <span data-ttu-id="3ab53-106">これらのデリゲート メソッドは通常、**EventHandlerResult** パラメーターを最後のパラメーターとして持つシグネチャを持っています。</span><span class="sxs-lookup"><span data-stu-id="3ab53-106">These delegate methods usually have a signature that has an **EventHandlerResult** parameter as the last parameter.</span></span> <span data-ttu-id="3ab53-107">ただし、**EventHandlerAcceptResult** および **EventHandlerRejectResult** タイプのサポートが原因で、パラメーターは **IEventHandlerResult** インターフェイスを実装する任意のタイプになります。</span><span class="sxs-lookup"><span data-stu-id="3ab53-107">However, because of the support for the **EventHandlerAcceptResult** and **EventHandlerRejectResult** types, the parameter can be of any type that implements the **IEventHandlerResult** interface.</span></span>

+ <span data-ttu-id="3ab53-108">一般に、デリゲート ハンドラー メソッドに実装されているロジックには、サブスクライブしているロジックが応答の提供を担当していることを検証する条件を含める必要があります。</span><span class="sxs-lookup"><span data-stu-id="3ab53-108">In general, the logic that is implemented in the delegate handler method should contain a condition that verifies that the subscribing logic is responsible for providing a response.</span></span> <span data-ttu-id="3ab53-109">結果のフォームに応答を提供するロジックも含める必要があります。</span><span class="sxs-lookup"><span data-stu-id="3ab53-109">It should also include logic to provide the response in the form of a result.</span></span>
+ <span data-ttu-id="3ab53-110">デリゲート ハンドラー メソッドが **EventHandlerResult** オブジェクト パラメーターへの応答を提供する必要があるとき、サブスクライブするロジックには結果の計算または取得のためのロジックも含まれている場合があります。</span><span class="sxs-lookup"><span data-stu-id="3ab53-110">When the delegate handler method must provide the response to an **EventHandlerResult** object parameter, the subscribing logic might also contain logic to calculate or retrieve the result.</span></span>
+ <span data-ttu-id="3ab53-111">条件と応答ロジックが実装されると、条件が **true** と評価されたときのみ、結果の計算を実行する必要があります。</span><span class="sxs-lookup"><span data-stu-id="3ab53-111">When the condition and the response logic are implemented, the calculation of the result must occur only when the condition is evaluated to **true**.</span></span>
+ <span data-ttu-id="3ab53-112">すべてのサブスクライブしているデリゲート ハンドラー メソッドはデリゲートが呼び出されたときに実行されます。</span><span class="sxs-lookup"><span data-stu-id="3ab53-112">All the subscribing delegate handler methods are run when a delegate is called.</span></span> <span data-ttu-id="3ab53-113">したがって、メソッドがレスポンスの提供を担当していない場合は、メソッドを実行する間接費ができるだけ低いことを確認する必要があります。</span><span class="sxs-lookup"><span data-stu-id="3ab53-113">Therefore, you should make sure that the overhead of running your method is as low as possible when the method isn't responsible for providing a response.</span></span> <span data-ttu-id="3ab53-114">したがって、デリゲート ハンドラー メソッドが結果を提供する責任を負わない場合、できるだけ早く条件が **false** に評価されていることを確認してください。</span><span class="sxs-lookup"><span data-stu-id="3ab53-114">Therefore, make sure that the condition is evaluated to **false** as quickly as possible when your delegate handler method isn't responsible for providing a result.</span></span>

## <a name="examples"></a><span data-ttu-id="3ab53-115">例</span><span class="sxs-lookup"><span data-stu-id="3ab53-115">Examples</span></span>
<span data-ttu-id="3ab53-116">次の例は、**switch** ステートメントの形式の条件を持つデリゲート ハンドラーを示しています。</span><span class="sxs-lookup"><span data-stu-id="3ab53-116">The following example shows a delegate handler that has a condition in the form of a **switch** statement.</span></span> <span data-ttu-id="3ab53-117">デリゲート ハンドラーには結果のフォームに応答を提供するロジックがあります。</span><span class="sxs-lookup"><span data-stu-id="3ab53-117">The delegate handler also has logic to provide a response in the form of the result.</span></span> <span data-ttu-id="3ab53-118">応答するロジックは、条件が **true** に評価された場合にのみ実行されます。</span><span class="sxs-lookup"><span data-stu-id="3ab53-118">The responding logic is run only when the condition is evaluated to **true**.</span></span>

```xpp
[SubscribesTo(tableStr(InventWarehouseEntity), delegateStr(InventWarehouseEntity, validateWarehouseTypeDelegate))]
public static void validateWarehouseTypeIsSupportedStandardDelegateHandler(InventLocationType _inventLocationType, EventHandlerResult _result)
{
    switch (_inventLocationType)
    {
        case InventLocationType::Standard:
        case InventLocationType::Quarantine:
        case InventLocationType::Transit:
            _result.result(true);
            break;
    }
}
```

<span data-ttu-id="3ab53-119">デリゲート メソッドが、**EventHandlerAcceptResult** または **EventHandlerRejectResult** オブジェクト パラメーターを使用して、応答を要求するとき、サブスクライバーは、承認または否認でのみ応答することを想定します。</span><span class="sxs-lookup"><span data-stu-id="3ab53-119">When the delegate method requests a response by using an **EventHandlerAcceptResult** or an **EventHandlerRejectResult** object parameter, the subscriber is expected to respond only with an accept or a reject.</span></span> <span data-ttu-id="3ab53-120">サブスクライブ ロジックは、メッセージを Infolog に追加することもできます。</span><span class="sxs-lookup"><span data-stu-id="3ab53-120">The subscribing logic might also add messages to the Infolog.</span></span>

<span data-ttu-id="3ab53-121">次の例は、前の例に似ています。</span><span class="sxs-lookup"><span data-stu-id="3ab53-121">The following example resembles the previous example.</span></span> <span data-ttu-id="3ab53-122">ただし、デリゲート メソッドは、**EventHandlerAcceptResult** オブジェクトの使用によりおよび **受け入れ** メソッドを呼び出すことにより、応答を要求するようになります。</span><span class="sxs-lookup"><span data-stu-id="3ab53-122">However, the delegate method now requests a response by using an **EventHandlerAcceptResult** object and by calling the **accept** method.</span></span>
    
```xpp
[SubscribesTo(tableStr(InventWarehouseEntity), delegateStr(InventWarehouseEntity, validateWarehouseTypeDelegate))]
public static void validateWarehouseTypeIsSupportedStandardDelegateHandler(InventLocationType _inventLocationType, EventHandlerAcceptResult _result)
{
    switch (_inventLocationType)
    {
        case InventLocationType::Standard:
        case InventLocationType::Quarantine:
        case InventLocationType::Transit:
            _result.accept();
            break;
    }
}
```

<span data-ttu-id="3ab53-123">次の例では、**EventHandlerRejectResult** オブジェクトを使用して応答するデリゲート ハンドラー メソッドを示しています。</span><span class="sxs-lookup"><span data-stu-id="3ab53-123">The following example shows a delegate handler method that responds by using an **EventHandlerRejectResult** object.</span></span> <span data-ttu-id="3ab53-124">**EventHandlerRejectResult** オブジェクトを使用して応答するには、**reject** メソッドまたは **checkFailed** 拡張メソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="3ab53-124">To respond by using an **EventHandlerRejectResult** object, you can call the **reject** method or the **checkFailed** extension method.</span></span> <span data-ttu-id="3ab53-125">**checkFailed** メソッドを使用する場合は、情報ログに警告メッセージを追加できます。</span><span class="sxs-lookup"><span data-stu-id="3ab53-125">If you use the **checkFailed** method, you can add a warning message to the Infolog.</span></span> <span data-ttu-id="3ab53-126">内部的には、**checkFailed** メソッドは **reject** メソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="3ab53-126">Internally, the **checkFailed** method calls the **reject** method.</span></span>

```xpp
[SubscribesTo(classStr(ProdTableType), delegateStr(ProdTableType, validateWriteProdTableInventRefTypeDelegate))]
public static void validateWriteProdTableInventRefTypeDelegateHandler(ProdTable _prodTable, EventHandlerRejectResult _result)
{
    if (_prodTable.InventRefType == InventRefType::ProdLine)
    {
        if (! _prodTable.InventRefId || !_prodTable.InventRefTransId)
        {
            _result.checkFailed("@SYS19558");
        }
        ProdBOM prodBOM;
        select prodBOM
            where prodBOM.InventTransId  == _prodTable.InventRefTransId;
        if (! _prodTable.checkRefProdBOM(prodBOM))
        {
            _result.reject();
        }
    }
}
```

## <a name="guidelines"></a><span data-ttu-id="3ab53-127">ガイドライン</span><span class="sxs-lookup"><span data-stu-id="3ab53-127">Guidelines</span></span>
<span data-ttu-id="3ab53-128">前述の実例に加えて、次の一般的なガイドラインが適用されます。</span><span class="sxs-lookup"><span data-stu-id="3ab53-128">In addition to the previously described practices, the following general guidelines apply:</span></span>

- <span data-ttu-id="3ab53-129">サブスクライブしているロジックが応答を担当する場合にのみ対応します。</span><span class="sxs-lookup"><span data-stu-id="3ab53-129">Respond only when the subscribing logic is responsible for responding.</span></span> <span data-ttu-id="3ab53-130">デリゲート ハンドラー メソッドは、特定の条件が満たされたときに応答を提供するために実装されました。</span><span class="sxs-lookup"><span data-stu-id="3ab53-130">The delegate handler methods were implemented to provide a response when a specific condition is met.</span></span> <span data-ttu-id="3ab53-131">したがって、サブスクライブしているロジックは、特定の条件が満たされた場合に結果を提供する必要があります。</span><span class="sxs-lookup"><span data-stu-id="3ab53-131">Therefore, the subscribing logic must provide a result when a specific condition is met.</span></span> <span data-ttu-id="3ab53-132">サブスクライブしているロジックが応答する前に、結果オブジェクト パラメーターは既に結果が含まれているかどうかを評価することができません。</span><span class="sxs-lookup"><span data-stu-id="3ab53-132">Before the subscribing logic responds, it should not evaluate whether the result object parameter already contains a result.</span></span> <span data-ttu-id="3ab53-133">たとえば、デリゲート ハンドラー メソッドは、次の例にあるロジックに似たロジックを含めないようにする必要があります。</span><span class="sxs-lookup"><span data-stu-id="3ab53-133">For example, a delegate handler method should not contain logic that resembles the logic in the following example.</span></span> <span data-ttu-id="3ab53-134">このロジックは、メソッド実行時に **EventHandlerResult** オブジェクト パラメーターに結果がすでに含まれているかどうかを評価します。</span><span class="sxs-lookup"><span data-stu-id="3ab53-134">This logic evaluates whether the **EventHandlerResult** object parameter already contains a result when the method is run.</span></span>

    > [!WARNING]
    > <span data-ttu-id="3ab53-135">この例は、書くべきでは **ない** コードの例です。</span><span class="sxs-lookup"><span data-stu-id="3ab53-135">This example is an example of code that you should **not** write.</span></span>

    ```xpp
    [SubscribesTo(tableStr(InventWarehouseEntity), delegateStr(InventWarehouseEntity, validateWarehouseTypeDelegate))]
    public static void validateWarehouseTypeIsSupportedStandardDelegateHandler(InventLocationType _inventLocationType, EventHandlerResult _result)
    {
        // this if statement is an example of the bad practice.
        if (_result.hasResult())
        {
             return;
        }
        switch (_inventLocationType)
        {
            case InventLocationType::Standard:
            case InventLocationType::Quarantine:
            case InventLocationType::Transit:
                 _result.result(true);
                break;
        }
    }
    ```
    
- <span data-ttu-id="3ab53-136">他のサブスクライバーの代理として応答を提供しないでください。</span><span class="sxs-lookup"><span data-stu-id="3ab53-136">Don't provide a response on behalf of other subscribers.</span></span> <span data-ttu-id="3ab53-137">デリゲート ハンドラー メソッドが応答を提供する責任を負わない場合、メソッドは応答を提供できません。</span><span class="sxs-lookup"><span data-stu-id="3ab53-137">If the delegate handler method isn't responsible for providing a response, the method must not provide a response.</span></span> <span data-ttu-id="3ab53-138">条件が満たされていないときに、メソッドが応答を提供する場合は、他のサブスクライバーに代わって応答を提供しています。</span><span class="sxs-lookup"><span data-stu-id="3ab53-138">If the method provides a response when the condition isn't met, it provides a response on behalf of other subscribers.</span></span> <span data-ttu-id="3ab53-139">要求元のロジックは、サブスクライバーが応答していない状況を処理する責任を負わなければなりません。</span><span class="sxs-lookup"><span data-stu-id="3ab53-139">The requesting logic must be responsible for handling situations where no subscribers have responded.</span></span> <span data-ttu-id="3ab53-140">デリゲート ハンドラー メソッドは、次の例にあるロジックに似たロジックを含めないようにする必要があります。</span><span class="sxs-lookup"><span data-stu-id="3ab53-140">The delegate handler method must not contain logic that resembles the logic in the following example.</span></span> <span data-ttu-id="3ab53-141">このロジックは、条件が **false** と評価されたときに結果を提供します。</span><span class="sxs-lookup"><span data-stu-id="3ab53-141">This logic which provides a result when the condition is evaluated to **false**.</span></span>
    
    > [!WARNING]
    > <span data-ttu-id="3ab53-142">この例は、書くべきでは **ない** コードの例です。</span><span class="sxs-lookup"><span data-stu-id="3ab53-142">This example is an example of code that you should **not** write.</span></span>
    
    ```xpp
    [SubscribesTo(tableStr(InventWarehouseEntity), delegateStr(InventWarehouseEntity, validateWarehouseTypeDelegate))]
    public static void validateWarehouseTypeIsSupportedStandardDelegateHandler(InventLocationType _inventLocationType, EventHandlerResult _result)
    {
        switch (_inventLocationType)
        {
            case InventLocationType::Standard:
            case InventLocationType::Quarantine:
            case InventLocationType::Transit:
                _result.result(true);
                break;
            // this default block is an example of the bad practice
            default:
                _result.result(false);
                break;
        }
    }
    ```


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]