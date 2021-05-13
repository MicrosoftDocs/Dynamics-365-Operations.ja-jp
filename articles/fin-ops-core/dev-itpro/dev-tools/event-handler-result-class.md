---
title: 要求または応答シナリオの EventHandlerResult クラス
description: このトピックでは、デリゲート メソッドで EventHandlerResult クラスを使用する方法について説明します。
author: RobinARH
ms.date: 06/20/2017
ms.topic: article
audience: Developer
ms.reviewer: rhaertle
ms.assetid: 3b2a9b85-f779-4358-b347-7b11a8e7960c
ms.search.region: Global
ms.author: rhaertle
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 56e972d67e8056b9b2a41de2419f882bb7604689
ms.sourcegitcommit: e4992c57eea4c15ac052e9d65dddae625e3528f9
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/07/2021
ms.locfileid: "5866340"
---
# <a name="eventhandlerresult-classes-in-request-or-response-scenarios"></a><span data-ttu-id="3964e-103">要求または応答シナリオの EventHandlerResult クラス</span><span class="sxs-lookup"><span data-stu-id="3964e-103">EventHandlerResult classes in request or response scenarios</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="3964e-104">デリゲート メソッドとデリゲート ハンドラー メソッドは、デリゲート呼び出しロジックがサブスクライバに応答を要求する要求/応答シナリオをサポートするために宣言することができます。</span><span class="sxs-lookup"><span data-stu-id="3964e-104">Delegate methods and delegate handler methods can be declared to support a request/response scenario, where the delegate calling logic requests the subscribers to provide a response.</span></span> <span data-ttu-id="3964e-105">このシナリオをサポートするために、**EventHandlerResult** クラスがパラメーターとして渡されることが最も多く、デリゲート ハンドラー メソッドがクラスの result メソッドの 1 つを使用して結果を提供します。</span><span class="sxs-lookup"><span data-stu-id="3964e-105">To support this scenario the **EventHandlerResult** class is most often passed as a parameter, and the delegate handler methods provide their result using one of the result methods on the class.</span></span> <span data-ttu-id="3964e-106">ただし、**EventHandlerResult** クラスは単一の結果のみを含むため、複数のサブスクライバが個々の結果を提供する場合は、最後の回答者が獲得し、前のサブスクライバからの結果が上書きされます。</span><span class="sxs-lookup"><span data-stu-id="3964e-106">However, the **EventHandlerResult** class can only contain a single result, so if multiple subscribers provide their individual result, the last respondent wins, and the results from the previous subscribers are overwritten.</span></span>

<span data-ttu-id="3964e-107">このトピックで説明されている機能が導入される前 (プラットフォーム更新プログラム 5) は、最大でも単一のサブスクライバーが結果を提供し、複数のサブスクライバーが存在すると結果が失われないことを保証するメカニズムはありませんでした。</span><span class="sxs-lookup"><span data-stu-id="3964e-107">Before the functionality described in this topic was introduced (platform update 5), there was no mechanism to ensure that, at most, a single subscriber provided a result, and that no results were lost if there were multiple subscribers.</span></span>

## <a name="ensuring-at-most-one-response"></a><span data-ttu-id="3964e-108">最大で 1 つの応答を確認</span><span class="sxs-lookup"><span data-stu-id="3964e-108">Ensuring, at most, one response</span></span>

<span data-ttu-id="3964e-109">プラットフォーム更新プログラム 5 では、1 つ以上のサブスクライバーが結果を提示している場合にロジックが失敗することを確認する追加の静的コンストラクターが、**EventHandlerResult** クラスにあります。</span><span class="sxs-lookup"><span data-stu-id="3964e-109">In platform update 5, the **EventHandlerResult** class has an additional static constructor which ensures that the logic fails if more than one subscriber provides a result.</span></span> <span data-ttu-id="3964e-110">新しいコンストラクターの名前は、**newSingleResponse**。</span><span class="sxs-lookup"><span data-stu-id="3964e-110">The new constructor is named **newSingleResponse**.</span></span> <span data-ttu-id="3964e-111">このメソッドを使用して **EventHandlerResult** オブジェクトをインスタンス化したとき、2 番目のデリゲート ハンドラー メソッドが結果を提供しようとすると、このフレームワークはただちに例外をスローします。</span><span class="sxs-lookup"><span data-stu-id="3964e-111">When instantiating an **EventHandlerResult** object using this method, the framework will throw an exception as soon as a second delegate handler method attempts to provide a result.</span></span>

```xpp
EventHandlerResult result = EventHandlerResult::newSingleResponse();
this.validateWarehouseTypeDelegate(this.WarehouseType, result);
```

## <a name="ieventhandlerresultvalidator-interface"></a><span data-ttu-id="3964e-112">IEventHandlerResultValidator インターフェイス</span><span class="sxs-lookup"><span data-stu-id="3964e-112">IEventHandlerResultValidator interface</span></span>

<span data-ttu-id="3964e-113">**EventHandlerResult** クラスの検証は、**IEventHandlerResultValidator** インターフェイスを実装するタイプのオブジェクトを挿入することで処理されます。</span><span class="sxs-lookup"><span data-stu-id="3964e-113">The validation in the **EventHandlerResult** class is handled by injecting an object of a type that implements the **IEventHandlerResultValidator** interface.</span></span> <span data-ttu-id="3964e-114">**newSingleResponse** 静的コンストラクターを使用して **EventHandlerResult** オブジェクトをインスタンス化するとき、**EventHandlerSingleResponseValidator** オブジェクトがインスタンス化されて **EventHandlerResult** オブジェクトに挿入され、その挿入されたオブジェクトが **EventhandlerResult** オブジェクトに提供される結果の検証を担当します。</span><span class="sxs-lookup"><span data-stu-id="3964e-114">When instantiating the **EventHandlerResult** object using the **newSingleResponse** static constructor, an **EventHandlerSingleResponseValidator** object is instantiated and injected into the **EventHandlerResult** object, and the injected object becomes responsible for validating any result provided to the **EventhandlerResult** object.</span></span> <span data-ttu-id="3964e-115">他の検証クラスは、クラスで **IEventHandlerResultValidator** インターフェイスを実装することにより実装され、**newWithResultValidator** という別の新しい静的コンストラクターを使って **EventHandlerResult** オブジェクトをインスタンス化することにより **EventHandlerResult** クラスに挿入できます。</span><span class="sxs-lookup"><span data-stu-id="3964e-115">Other validation classes can be implemented by having the class implement the **IEventHandlerResultValidator** interface, and injecting it into the **EventHandlerResult** class by instantiating the **EventHandlerResult** object using another new static constructor named **newWithResultValidator**.</span></span> <span data-ttu-id="3964e-116">コンストラクターは、**IEventHandlerResultValidator** 型の引数をとります。これにより **IEventHandlerResultValidator** インターフェイスを実装している限り、任意の検証オブジェクトを挿入できます。</span><span class="sxs-lookup"><span data-stu-id="3964e-116">The constructor takes an argument of type **IEventHandlerResultValidator**, which makes it possible to inject any validator object as long as it implements the **IEventHandlerResultValidator** interface.</span></span>

<span data-ttu-id="3964e-117">たとえば、**newSingleResponse** 静的コンストラクターは単にインスタンス化を **newWithResultValidator** 静的コンストラクターに委任し、次のようになります。</span><span class="sxs-lookup"><span data-stu-id="3964e-117">For example, the **newSingleResponse** static constructor simply delegates the instantiation to the **newWithResultValidator** static constructor like this.</span></span>

```xpp
return EventHandlerResult::newWithResultValidator(EventHandlerSingleResponseValidator::construct());
```

## <a name="accept-and-reject-requestresponse-scenarios"></a><span data-ttu-id="3964e-118">要求/応答シナリオを承認して拒否する</span><span class="sxs-lookup"><span data-stu-id="3964e-118">Accept and reject request/response scenarios</span></span>

<span data-ttu-id="3964e-119">特定の要求/応答シナリオでは、サブスクライバーは承認または拒否を提示することのみ期待されます。</span><span class="sxs-lookup"><span data-stu-id="3964e-119">In certain request/response scenarios, the subscriber is only expected to provide their acceptance or rejection.</span></span> <span data-ttu-id="3964e-120">サブスクライバーがブール値での応答のみを期待している場合、受入/拒否の要求に **EventHandlerResult** クラスを使用することは分かりにくい可能性があります。</span><span class="sxs-lookup"><span data-stu-id="3964e-120">Using the **EventHandlerResult** class to request acceptance/rejection can be confusing, if the subscriber is only expected to respond with a Boolean value.</span></span> <span data-ttu-id="3964e-121">たとえば、検証シナリオで、検証が失敗した場合にサブスクライバーはブール値 false でのみ応答すべきか、また検証が成功した場合にサブスクライバーがブール値 true で応答すべきかがあります。</span><span class="sxs-lookup"><span data-stu-id="3964e-121">In a validation scenario, for example, should the subscriber only respond with Boolean false, when validation fails, or should the subscriber also respond with Boolean true, if validation succeeds?</span></span> <span data-ttu-id="3964e-122">**EventHandlerResult** オブジェクトを使用して応答が収集される場合、第二のサブスクライバーが true のブール値で検証し、応答すると、第一サブスクライバーの false のブール値が上書きされる可能性があります。</span><span class="sxs-lookup"><span data-stu-id="3964e-122">If the response is gathered using an **EventHandlerResult** object, then the second subscriber that validates and replies with Boolean true, might overwrite the Boolean false from the first subscriber.</span></span>

<span data-ttu-id="3964e-123">この混乱を軽減するために、**EventHandlerAcceptResult** と **EventHandlerRejectResult** の 2 つの新しい結果型クラスがプラットフォーム更新プログラム 5 に導入されました。</span><span class="sxs-lookup"><span data-stu-id="3964e-123">To mitigate this confusion, two new result type classes have been introduced in Platform update 5: **EventHandlerAcceptResult** and **EventHandlerRejectResult**.</span></span>

<span data-ttu-id="3964e-124">**EventHandlerAcceptResult** クラスを使用するとき、デリゲート ハンドラー メソッドは **承認** メソッドの呼び出しによってのみ応答できます。</span><span class="sxs-lookup"><span data-stu-id="3964e-124">When using the **EventHandlerAcceptResult** class, the delegate handler method can only respond by calling the **accept** method.</span></span> <span data-ttu-id="3964e-125">**EventHandlerRejectResult** クラスを使用するとき、**否認** メソッドのみを呼び出すことができます。</span><span class="sxs-lookup"><span data-stu-id="3964e-125">When using the **EventHandlerRejectResult** class, only the **reject** method can be called.</span></span>

```xpp
[SubscribesTo(tableStr(InventWarehouseEntity), delegateStr(InventWarehouseEntity, validateWarehouseTypeDelegate))]
public static void validateWarehouseTypeIsSupportedStandardDelegateHandler(
    InventLocationType _inventLocationType, 
    EventHandlerAcceptResult _result)
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

<span data-ttu-id="3964e-126">2 つの新しいクラスには、最大で 1 つのサブスクライバーが拒否または承認で応答するシナリオで使用するための **newSingleResponse** 静的コンストラクターも含まれています。</span><span class="sxs-lookup"><span data-stu-id="3964e-126">The two new classes also contain a **newSingleResponse** static constructor for use in scenarios where, at most, one subscriber is allowed to respond with their rejection or acceptance.</span></span> <span data-ttu-id="3964e-127">いずれかのサブスクライバーが応答したかどうかは **hasResult** メソッドをクエリすることによってまだ回答できます。承認/否認は、**EventHandlerAcceptResult** および **EventHandlerRejectResult** クラスの **isAccepted** または **isRejected** のいずれかのメソッドをそれぞれ呼び出すことによってクエリされます。</span><span class="sxs-lookup"><span data-stu-id="3964e-127">Whether any subscriber has responded can still be answered by querying the **hasResult** method, and the acceptance/rejection is queried by calling either the **isAccepted** or **isRejected** methods for the **EventHandlerAcceptResult** and **EventHandlerRejectResult** classes, respectively.</span></span>

```xpp
boolean ret = false;
EventHandlerAcceptResult result = EventHandlerAcceptResult::newSingleResponse(); 
this.validateWarehouseTypeDelegate(this.WarehouseType, result);
if (result.hasResult())
{
    ret = result.isAccepted();
}
```


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]