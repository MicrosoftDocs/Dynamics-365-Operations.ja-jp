---
title: "要求または応答シナリオの EventHandlerResult クラス"
description: "このトピックでは、デリゲート メソッドで EventHandlerResult クラスを使用する方法について説明します。"
author: RobinARH
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Developer
ms.reviewer: robinr
ms.search.scope: Operations
ms.assetid: 3b2a9b85-f779-4358-b347-7b11a8e7960c
ms.search.region: Global
ms.author: robinr
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: 5ebc4a7e3c26a5678dc94833727a60802dc00847
ms.contentlocale: ja-jp
ms.lasthandoff: 05/08/2018

---

# <a name="eventhandlerresult-classes-in-request-or-response-scenarios"></a><span data-ttu-id="ea30f-103">要求または応答シナリオの EventHandlerResult クラス</span><span class="sxs-lookup"><span data-stu-id="ea30f-103">EventHandlerResult classes in request or response scenarios</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="ea30f-104">デリゲート メソッドとデリゲート ハンドラー メソッドは、デリゲート呼び出しロジックがサブスクライバに応答を要求する要求/応答シナリオをサポートするために宣言することができます。</span><span class="sxs-lookup"><span data-stu-id="ea30f-104">Delegate methods and delegate handler methods can be declared to support a request/response scenario, where the delegate calling logic requests the subscribers to provide a response.</span></span> <span data-ttu-id="ea30f-105">このシナリオをサポートするために、**EventHandlerResult** クラスがパラメーターとして渡されることが最も多く、デリゲート ハンドラー メソッドがクラスの result メソッドの 1 つを使用して結果を提供します。</span><span class="sxs-lookup"><span data-stu-id="ea30f-105">To support this scenario the **EventHandlerResult** class is most often passed as a parameter, and the delegate handler methods provide their result using one of the result methods on the class.</span></span> <span data-ttu-id="ea30f-106">ただし、**EventHandlerResult** クラスは単一の結果のみを含むため、複数のサブスクライバが個々の結果を提供する場合は、最後の回答者が獲得し、前のサブスクライバからの結果が上書きされます。</span><span class="sxs-lookup"><span data-stu-id="ea30f-106">However, the **EventHandlerResult** class can only contain a single result, so if multiple subscribers provide their individual result, the last respondent wins, and the results from the previous subscribers are overwritten.</span></span>

<span data-ttu-id="ea30f-107">このトピックで説明されている機能が導入される前 (プラットフォーム更新プログラム 5) は、最大でも単一のサブスクライバーが結果を提供し、複数のサブスクライバーが存在すると結果が失われないことを保証するメカニズムはありませんでした。</span><span class="sxs-lookup"><span data-stu-id="ea30f-107">Before the functionality described in this topic was introduced (platform update 5), there was no mechanism to ensure that, at most, a single subscriber provided a result, and that no results were lost if there were multiple subscribers.</span></span>

## <a name="ensuring-at-most-one-response"></a><span data-ttu-id="ea30f-108">最大で 1 つの応答を確認</span><span class="sxs-lookup"><span data-stu-id="ea30f-108">Ensuring, at most, one response</span></span>

<span data-ttu-id="ea30f-109">プラットフォーム更新プログラム 5 では、1 つ以上のサブスクライバーが結果を提示している場合にロジックが失敗することを確認する追加の静的コンストラクターが、**EventHandlerResult** クラスにあります。</span><span class="sxs-lookup"><span data-stu-id="ea30f-109">In platform update 5, the **EventHandlerResult** class has an additional static constructor which ensures that the logic fails if more than one subscriber provides a result.</span></span> <span data-ttu-id="ea30f-110">新しいコンストラクターの名前は、**newSingleResponse**。</span><span class="sxs-lookup"><span data-stu-id="ea30f-110">The new constructor is named **newSingleResponse**.</span></span> <span data-ttu-id="ea30f-111">このメソッドを使用して **EventHandlerResult** オブジェクトをインスタンス化したとき、2 番目のデリゲート ハンドラー メソッドが結果を提供しようとすると、このフレームワークはただちに例外をスローします。</span><span class="sxs-lookup"><span data-stu-id="ea30f-111">When instantiating an **EventHandlerResult** object using this method, the framework will throw an exception as soon as a second delegate handler method attempts to provide a result.</span></span>

    EventHandlerResult result = EventHandlerResult::newSingleResponse();
    this.validateWarehouseTypeDelegate(this.WarehouseType, result);

## <a name="ieventhandlerresultvalidator-interface"></a><span data-ttu-id="ea30f-112">IEventHandlerResultValidator インターフェイス</span><span class="sxs-lookup"><span data-stu-id="ea30f-112">IEventHandlerResultValidator interface</span></span>

<span data-ttu-id="ea30f-113"><strong>EventHandlerResult</strong> クラスの検証は、<strong>IEventHandlerResultValidator</strong> インターフェイスを実装するタイプのオブジェクトを挿入することで処理されます。</span><span class="sxs-lookup"><span data-stu-id="ea30f-113">The validation in the <strong>EventHandlerResult</strong> class is handled by injecting an object of a type that implements the <strong>IEventHandlerResultValidator</strong> interface.</span></span> <span data-ttu-id="ea30f-114"><strong>newSingleResponse</strong> 静的コンストラクターを使用して <strong>EventHandlerResult</strong> オブジェクトをインスタンス化するとき、<strong>EventHandlerSingleResponseValidator</strong> オブジェクトがインスタンス化されて <strong>EventHandlerResult</strong> オブジェクトに挿入され、その挿入されたオブジェクトが <strong>EventhandlerResult</strong> オブジェクトに提供される結果の検証を担当します。</span><span class="sxs-lookup"><span data-stu-id="ea30f-114">When instantiating the <strong>EventHandlerResult</strong> object using the <strong>newSingleResponse</strong> static constructor, an <strong>EventHandlerSingleResponseValidator</strong> object is instantiated and injected into the <strong>EventHandlerResult</strong> object, and the injected object becomes responsible for validating any result provided to the <strong>EventhandlerResult</strong> object.</span></span> <span data-ttu-id="ea30f-115">他の検証クラスは、クラスで <strong>IEventHandlerResultValidator** インターフェイスを実装することにより実装し、<strong>newWithResultValidator</strong> という別の新しい静的コンストラクターを使って <strong>EventHandlerResult</strong> オブジェクトをインスタンス化することにより **EventHandlerResult</strong> クラスに挿入できます。</span><span class="sxs-lookup"><span data-stu-id="ea30f-115">Other validation classes can be implemented by having the class implement the <strong>IEventHandlerResultValidator **interface, and injecting it into the **EventHandlerResult</strong> class by instantiating the <strong>EventHandlerResult</strong> object using another new static constructor named <strong>newWithResultValidator</strong>.</span></span> <span data-ttu-id="ea30f-116">コンストラクターは、<strong>IEventHandlerResultValidator</strong> 型の引数をとります。これにより、<strong>IEventHandlerResultValidator** インターフェイス**を実装している限り、任意の検証ソフト オブジェクトを挿入できます。</strong>。</span><span class="sxs-lookup"><span data-stu-id="ea30f-116">The constructor takes an argument of type <strong>IEventHandlerResultValidator</strong>, which makes it possible to inject any validator object as long as it implements the <strong>IEventHandlerResultValidator **interface</strong>.**</span></span>

<span data-ttu-id="ea30f-117">たとえば、<strong>newSingleResponse</strong> 静的コンストラクターは単にインスタンス化を **newWithResultValidator** 静的コンストラクターに委任し、次のようになります。</span><span class="sxs-lookup"><span data-stu-id="ea30f-117">For example, the <strong>newSingleResponse</strong> static constructor simply delegates the instantiation to the **newWithResultValidator** static constructor like this.</span></span>

    return EventHandlerResult::newWithResultValidator(EventHandlerSingleResponseValidator::construct());

## <a name="accept-and-reject-requestresponse-scenarios"></a><span data-ttu-id="ea30f-118">要求/応答シナリオを承認して拒否する</span><span class="sxs-lookup"><span data-stu-id="ea30f-118">Accept and reject request/response scenarios</span></span>

<span data-ttu-id="ea30f-119">特定の要求/応答シナリオでは、サブスクライバーは承認または拒否を提示することのみ期待されます。</span><span class="sxs-lookup"><span data-stu-id="ea30f-119">In certain request/response scenarios, the subscriber is only expected to provide their acceptance or rejection.</span></span> <span data-ttu-id="ea30f-120">サブスクライバーがブール値での応答のみを期待している場合、受入/拒否の要求に **EventHandlerResult** クラスを使用することは分かりにくい可能性があります。</span><span class="sxs-lookup"><span data-stu-id="ea30f-120">Using the **EventHandlerResult** class to request acceptance/rejection can be confusing, if the subscriber is only expected to respond with a Boolean value.</span></span> <span data-ttu-id="ea30f-121">たとえば、検証シナリオで、検証が失敗した場合にサブスクライバーはブール値 false でのみ応答すべきか、また検証が成功した場合にサブスクライバーがブール値 true で応答すべきかがあります。</span><span class="sxs-lookup"><span data-stu-id="ea30f-121">In a validation scenario, for example, should the subscriber only respond with Boolean false, when validation fails, or should the subscriber also respond with Boolean true, if validation succeeds?</span></span> <span data-ttu-id="ea30f-122">**EventHandlerResult** オブジェクトを使用して応答が収集される場合、第二のサブスクライバーが true のブール値で検証し、応答すると、第一サブスクライバーの false のブール値が上書きされる可能性があります。</span><span class="sxs-lookup"><span data-stu-id="ea30f-122">If the response is gathered using an **EventHandlerResult** object, then the second subscriber that validates and replies with Boolean true, might overwrite the Boolean false from the first subscriber.</span></span>

<span data-ttu-id="ea30f-123">この混乱を軽減するために、**EventHandlerAcceptResult** と **EventHandlerRejectResult** の 2 つの新しい結果型クラスがプラットフォーム更新プログラム 5 に導入されました。</span><span class="sxs-lookup"><span data-stu-id="ea30f-123">To mitigate this confusion, two new result type classes have been introduced in platform update 5: **EventHandlerAcceptResult** and **EventHandlerRejectResult**.</span></span>

<span data-ttu-id="ea30f-124">**EventHandlerAcceptResult** クラスを使用するとき、デリゲート ハンドラー メソッドは **承認** メソッドの呼び出しによってのみ応答できます。</span><span class="sxs-lookup"><span data-stu-id="ea30f-124">When using the **EventHandlerAcceptResult** class, the delegate handler method can only respond by calling the **accept** method.</span></span> <span data-ttu-id="ea30f-125">**EventHandlerRejectResult** クラスを使用するとき、**否認** メソッドのみを呼び出すことができます。</span><span class="sxs-lookup"><span data-stu-id="ea30f-125">When using the **EventHandlerRejectResult** class, only the **reject** method can be called.</span></span>

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

<span data-ttu-id="ea30f-126">2 つの新しいクラスには、最大で 1 つのサブスクライバーが拒否または承認で応答するシナリオで使用するための <strong>newSingleResponse</strong> 静的コンストラクターも含まれています。</span><span class="sxs-lookup"><span data-stu-id="ea30f-126">The two new classes also contain a <strong>newSingleResponse</strong> static constructor for use in scenarios where, at most, one subscriber is allowed to respond with their rejection or acceptance.</span></span> <span data-ttu-id="ea30f-127">いずれかのサブスクライバーが応答したかどうかは <strong>hasResult</strong> メソッドをクエリすることによってまだ回答できます。承認/否認は、<strong>EventHandlerAcceptResult ** および </strong>EventHandlerRejectResult ** クラスの <strong>isAccepted</strong> または <strong>isRejected</strong> のいずれかのメソッドをそれぞれ呼び出すことによってクエリされます。</span><span class="sxs-lookup"><span data-stu-id="ea30f-127">Whether any subscriber has responded can still be answered by querying the <strong>hasResult</strong> method, and the acceptance/rejection is queried by calling either the <strong>isAccepted</strong> or <strong>isRejected</strong> methods for the <strong>EventHandlerAcceptResult **and</strong> EventHandlerRejectResult **classes, respectively.</span></span>

    boolean ret = false;
    EventHandlerAcceptResult result = EventHandlerAcceptResult::newSingleResponse(); 
    this.validateWarehouseTypeDelegate(this.WarehouseType, result);
    if (result.hasResult())
    {
        ret = result.isAccepted();
    }



