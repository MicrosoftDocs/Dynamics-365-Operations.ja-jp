---
title: X++ イベントの用語およびキーワード
description: このトピックでは、X++ のイベント用語とキーワードについて説明します。
author: robinarh
manager: AnnBe
ms.date: 06/18/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Developer
ms.reviewer: rhaertle
ms.search.scope: Operations
ms.custom: 150303
ms.assetid: 1b2d76d1-52d9-46b2-937f-5a3b62f2d516
ms.search.region: Global
ms.author: rhaertle
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 4c45b319504fcf68eff281e303464fab80f02f7c
ms.sourcegitcommit: 7eae20185944ff7394531173490a286a61092323
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 12/03/2019
ms.locfileid: "2872648"
---
# <a name="x-event-terminology-and-keywords"></a><span data-ttu-id="27140-103">X++ イベントの用語およびキーワード</span><span class="sxs-lookup"><span data-stu-id="27140-103">X++ event terminology and keywords</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="27140-104">このトピックでは、X++ のイベント用語とキーワードについて説明します。</span><span class="sxs-lookup"><span data-stu-id="27140-104">This topic describes event terminology and keywords in X++.</span></span> 

<span data-ttu-id="27140-105">イベント設計パターンを使用すると、コードをさらにモジュール化して再使用可能にすることができます。</span><span class="sxs-lookup"><span data-stu-id="27140-105">You can use the event design pattern to make your code more modular and reusable.</span></span> <span data-ttu-id="27140-106">*イベント* という用語は、デリゲートの使用方法を説明するメタファです。</span><span class="sxs-lookup"><span data-stu-id="27140-106">The term *event* is a metaphor that explains how delegates are used.</span></span> <span data-ttu-id="27140-107">プログラム実行中に何か重要なことが発生したときは、他のモジュールがその発生を処理することが必要な場合があります。</span><span class="sxs-lookup"><span data-stu-id="27140-107">When something important occurs during a program run, other modules might have to process the occurrence.</span></span> <span data-ttu-id="27140-108">これらの重要な出来事は*イベント*と呼ばれています。</span><span class="sxs-lookup"><span data-stu-id="27140-108">These important occurrences are known as *events*.</span></span> <span data-ttu-id="27140-109">イベントが発生すると、プログラムは、Notifier がイベントに関する通知を送信する必要があることを、そのイベントの Notifier に指示します。</span><span class="sxs-lookup"><span data-stu-id="27140-109">When an event occurs, the program tells its notifier for the event that the notifier must send notifications about the event.</span></span> <span data-ttu-id="27140-110">通知は、通知のサブスクライバーであるすべてのイベント ハンドラーに送信する必要があります。</span><span class="sxs-lookup"><span data-stu-id="27140-110">A notification must be sent to all the event handlers that are subscribers of the notifier.</span></span> <span data-ttu-id="27140-111">プログラムがその通知機能に通知を送信するように指示するとき、そのプロセスをイベントの *発生* と呼んでいます。</span><span class="sxs-lookup"><span data-stu-id="27140-111">When the program tells its notifier to send the notifications, we call that process *raising* an event.</span></span> 

<span data-ttu-id="27140-112">次のテーブルは、イベント メタファを説明するために使用される用語を示しています。</span><span class="sxs-lookup"><span data-stu-id="27140-112">The following table shows the terms that are used to describe the event metaphor.</span></span>

| <span data-ttu-id="27140-113">期間</span><span class="sxs-lookup"><span data-stu-id="27140-113">Term</span></span>          | <span data-ttu-id="27140-114">説明</span><span class="sxs-lookup"><span data-stu-id="27140-114">Description</span></span>                                                 |
|---------------|-------------------------------------------------------------|
| <span data-ttu-id="27140-115">イベント</span><span class="sxs-lookup"><span data-stu-id="27140-115">Event</span></span>         | <span data-ttu-id="27140-116">追加モジュールは発生を処理するプログラム モジュールで重要な発生です。</span><span class="sxs-lookup"><span data-stu-id="27140-116">An important occurrence in a program module where additional modules must process the occurrence.</span></span>    |
| <span data-ttu-id="27140-117">通知機能</span><span class="sxs-lookup"><span data-stu-id="27140-117">Notifier</span></span>      | <span data-ttu-id="27140-118">通知機能に登録されているすべてのイベント ハンドラーに、イベントに関する情報を送信するプログラム要素。</span><span class="sxs-lookup"><span data-stu-id="27140-118">The program element that sends information about the event to all the event handlers that are subscribed to the notifier.</span></span> |
| <span data-ttu-id="27140-119">サブスクライバー</span><span class="sxs-lookup"><span data-stu-id="27140-119">Subscriber</span></span>    | <span data-ttu-id="27140-120">イベント通知機能を登録しているプログラム機能またはメソッド。</span><span class="sxs-lookup"><span data-stu-id="27140-120">The program functions or methods that are subscribed to an event notifier.</span></span>                          |
| <span data-ttu-id="27140-121">イベント ハンドラー</span><span class="sxs-lookup"><span data-stu-id="27140-121">Event handler</span></span> | <span data-ttu-id="27140-122">イベント通知を購読するメソッド。</span><span class="sxs-lookup"><span data-stu-id="27140-122">The methods that subscribe to an event notifier.</span></span> <span data-ttu-id="27140-123">適切な種類のメソッドのみ、イベント ハンドラーになることができます。</span><span class="sxs-lookup"><span data-stu-id="27140-123">Only the appropriate kind of methods can be event handlers.</span></span>  |

## <a name="keywords-that-are-used-for-programming-that-uses-delegates"></a><span data-ttu-id="27140-124">デリゲートを使用するプログラミングに使用されるキーワード</span><span class="sxs-lookup"><span data-stu-id="27140-124">Keywords that are used for programming that uses delegates</span></span>

<span data-ttu-id="27140-125">次のテーブルに、デリゲートの使用方法を説明するキーワードを示します。</span><span class="sxs-lookup"><span data-stu-id="27140-125">The following table shows the keywords that describe the use of delegates.</span></span>

| <span data-ttu-id="27140-126">キーワードや用語</span><span class="sxs-lookup"><span data-stu-id="27140-126">Keyword or term</span></span>           | <span data-ttu-id="27140-127">区分</span><span class="sxs-lookup"><span data-stu-id="27140-127">Code</span></span>      | <span data-ttu-id="27140-128">説明</span><span class="sxs-lookup"><span data-stu-id="27140-128">Description</span></span>           |
|---------------------------|-----------|-----------------------|
| <span data-ttu-id="27140-129">デリゲート</span><span class="sxs-lookup"><span data-stu-id="27140-129">delegate</span></span>                                | `delegate myDelegate(str information) {}`                                | <span data-ttu-id="27140-130">このコードは、コード エディターでのデリゲートの外観を示しています。</span><span class="sxs-lookup"><span data-stu-id="27140-130">The code shows what the delegate looks like in the code editor.</span></span> <span data-ttu-id="27140-131">戻り値の型は常に**無効**なので、構文には示されていません。</span><span class="sxs-lookup"><span data-stu-id="27140-131">Because the return type is always **void**, it isn't mentioned in the syntax.</span></span> <span data-ttu-id="27140-132">かっこ ({}) 内にコードは使用できません。</span><span class="sxs-lookup"><span data-stu-id="27140-132">No code is allowed inside the braces ({}).</span></span>                                                               |
| <span data-ttu-id="27140-133">eventHandler</span><span class="sxs-lookup"><span data-stu-id="27140-133">eventHandler</span></span>                            | `myClassInstance.myDelegate += eventHandler(otherClass.myInstanceMethod);` | <span data-ttu-id="27140-134">**eventHandler** キーワードの構文は **eventHandler** X++ 関数であるという印象を与えますが、それは関数ではありません。</span><span class="sxs-lookup"><span data-stu-id="27140-134">Although the syntax of the **eventHandler** keyword might give the impression that **eventHandler** is an X++ function, it isn't a function.</span></span> <span data-ttu-id="27140-135">**eventHandler** キーワードは、メソッドがデリゲートにサブスクライブされることをコンパイラに伝えます。</span><span class="sxs-lookup"><span data-stu-id="27140-135">The **eventHandler** keyword tells the compiler that a method is being subscribed to a delegate.</span></span>         |
| <span data-ttu-id="27140-136">デリゲートにメソッドをサブスクライブまたは追加</span><span class="sxs-lookup"><span data-stu-id="27140-136">Subscribe or add a method to a delegate</span></span> | `myClassInstance.myDelegate += eventHandler(OtherClass::aStaticMethod);`   | <span data-ttu-id="27140-137">コードでは、静的メソッド **OtherClass::aStaticMethod** がデリゲートにサブスクライブされます。</span><span class="sxs-lookup"><span data-stu-id="27140-137">In the code, the static method **OtherClass::aStaticMethod** becomes subscribed to the delegate.</span></span>              |
| <span data-ttu-id="27140-138">デリゲートの呼び出し</span><span class="sxs-lookup"><span data-stu-id="27140-138">Call a delegate</span></span>                         | `myClassInstance.myDelegate("Hello");`                                     | <span data-ttu-id="27140-139">デリゲートへのこの呼び出しは、デリゲートにサブスクライブしている各メソッドを呼び出すようにデリゲートに要求します。</span><span class="sxs-lookup"><span data-stu-id="27140-139">This call to the delegate prompts the delegate to call each method that is subscribed to the delegate.</span></span> <span data-ttu-id="27140-140">サブスクライブされたメソッドは、デリゲートに追加されたのと同じ順序で呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="27140-140">The subscribed methods are called in the same order in which they were added to the delegate.</span></span> <span data-ttu-id="27140-141">1 つのサブスクライブされたメソッドは、そのデリゲードが次のメソッドを呼び出す前に完了される必要があります。</span><span class="sxs-lookup"><span data-stu-id="27140-141">One subscribed method must be completed before the delegate calls the next method.</span></span> |

## <a name="example"></a><span data-ttu-id="27140-142">例</span><span class="sxs-lookup"><span data-stu-id="27140-142">Example</span></span>

<span data-ttu-id="27140-143">次のコード例の 2 つのクラスは、イベントの定義方法、イベントのサブスクライブ方法、およびイベントを発生させる方法を示しています。</span><span class="sxs-lookup"><span data-stu-id="27140-143">The two classes in the following code example demonstrate how to define an event, subscribe to an event, and raise an event.</span></span> <span data-ttu-id="27140-144">**PointWithEvent** クラスは、**移動** されたデリゲートを定義します。</span><span class="sxs-lookup"><span data-stu-id="27140-144">The **PointWithEvent** class defines a delegate, **moved**.</span></span> <span data-ttu-id="27140-145">**移動** メソッドは、**移動** されたデリゲートを呼び出し、その結果、イベントをサブスクライブしているすべてのオブジェクトに通知します。</span><span class="sxs-lookup"><span data-stu-id="27140-145">The **move** method calls the **moved** delegate, thereby notifing any objects that have subscribed to the event.</span></span> <span data-ttu-id="27140-146">**PointKeeper** クラスは、**writeMove** メソッドを定義し、そのメソッドを、**createandmove** メソッドで作成された **ポイント** インスタンスの **移動** されたデリゲートのイベント ハンドラーとして割り当てます。</span><span class="sxs-lookup"><span data-stu-id="27140-146">The **PointKeeper** class defines the **writeMove** method and assigns it as the event handler for the **moved** delegate of the **Point** instance created in the **createAndMove** method.</span></span> 

```xpp
class PointWithEvent
{
    // Instance fields.
    real x;
    real y;

    // Constructor to initialize fields x and y.
    void new(real _x, real _y)
    {
        x = _x;
        y = _y;
    }

    void move(real x_offset, real y_offset)
    {
        x += x_offset;
        y += y_offset;
        this.moved(abs(x_offset) + abs(y_offset));
    }

    delegate void moved(real distance)
    {
    }

}

class PointKeeper
{

    public void createAndMove()
    {
        PointWithEvent point = new PointWithEvent(1.0, 2.0);

        point.moved += eventhandler(this.writeMove);

        point.move(4.0, 5.0);
        // Output is "9.0".
    }

    public void writeMove(real distance)
    {
        info(any2Str(distance));
    }

}
```
