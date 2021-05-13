---
title: 拡張機能を使用してテーブルにメソッドを追加
description: このトピックでは、拡張機能を使用してテーブルにメソッドを追加する方法について説明します。
author: ivanv-microsoft
ms.date: 10/22/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Developer
ms.reviewer: rhaertle
ms.custom: 268724
ms.assetid: ''
ms.search.region: Global
ms.author: ivanv
ms.search.validFrom: 2017-07-01
ms.dyn365.ops.version: Platform update 4
ms.openlocfilehash: f1ce96e8889f4f341adf513a09257c33c5b6e7e4
ms.sourcegitcommit: e4992c57eea4c15ac052e9d65dddae625e3528f9
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/07/2021
ms.locfileid: "5866094"
---
# <a name="add-methods-to-tables-through-extension"></a><span data-ttu-id="bf047-103">拡張機能を使用してテーブルにメソッドを追加</span><span class="sxs-lookup"><span data-stu-id="bf047-103">Add methods to tables through extension</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="bf047-104">テーブルに関連付けられているビジネス ロジックを拡張するとき、コードをクリーンに維持するために役立つ一般的なコーディング原則はまだ適用されます。</span><span class="sxs-lookup"><span data-stu-id="bf047-104">When you extend the business logic that is related to a table, the general coding principles that help keep your code clean still apply.</span></span> <span data-ttu-id="bf047-105">したがって、最終的にアクションをテーブルの別々のメソッドにカプセル化する必要があります。</span><span class="sxs-lookup"><span data-stu-id="bf047-105">Therefore, you must eventually encapsulate actions in separate methods on the table.</span></span> <span data-ttu-id="bf047-106">Microsoft Dynamics AX 2012 では、オーバーレイ経由でテーブルに直接メソッドを追加することによってそのタスクを完了していました。</span><span class="sxs-lookup"><span data-stu-id="bf047-106">In Microsoft Dynamics AX 2012, you completed that task by adding the method directly on the table through overlayering.</span></span> <span data-ttu-id="bf047-107">拡張を使用して同じタスクを完了するには、別の方法を使用します。</span><span class="sxs-lookup"><span data-stu-id="bf047-107">To complete the same task through extension, you use a different approach.</span></span> <span data-ttu-id="bf047-108">具体的には、拡張クラスを作成します。</span><span class="sxs-lookup"><span data-stu-id="bf047-108">Specifically, you create an augmentation class.</span></span>

<span data-ttu-id="bf047-109">たとえば、**MyInventLocationId** という名前新しいフィールドが、拡張機能によって InventTable テーブルに追加されました。</span><span class="sxs-lookup"><span data-stu-id="bf047-109">For example, a new field that is named **MyInventLocationId** was added to the InventTable table through extension.</span></span> <span data-ttu-id="bf047-110">**挿入** イベント用のデータ イベント ハンドラーも作成されました。新しいフィールドに入力するロジックを実装する必要があります。</span><span class="sxs-lookup"><span data-stu-id="bf047-110">A data event handler was also created for the **Inserting** event, and you must implement the logic of filling the new field there.</span></span> <span data-ttu-id="bf047-111">そのアクションをカプセル化するには、InventTable で新しいメソッドを作成し、そのメソッドに **myDefaultInventLocationId** という名前を付けます。</span><span class="sxs-lookup"><span data-stu-id="bf047-111">To encapsulate that action, you will create a new method on InventTable and name that method **myDefaultInventLocationId**.</span></span>

<span data-ttu-id="bf047-112">最初に、拡張モデルに新しいクラスを作成します。</span><span class="sxs-lookup"><span data-stu-id="bf047-112">You first create a new class in the extension model.</span></span> <span data-ttu-id="bf047-113">このクラスは InventTable テーブルを拡張し、読みやすく理解しやすい方法でテーブルのフィールドとメソッドにアクセスできるようにします</span><span class="sxs-lookup"><span data-stu-id="bf047-113">This class will augment the InventTable table, and enable access to the table's fields and methods in a manner that is easy to read and understand.</span></span> <span data-ttu-id="bf047-114">強化クラスに正しい名前を選択することが重要です。</span><span class="sxs-lookup"><span data-stu-id="bf047-114">It's important that you choose the correct name for your augmentation class.</span></span> <span data-ttu-id="bf047-115">この名前は、展開されるすべてのモデルのすべてのタイプにわたって一意でなければなりません。</span><span class="sxs-lookup"><span data-stu-id="bf047-115">This name must be unique across all types in all models that are deployed.</span></span> <span data-ttu-id="bf047-116">詳細については、[拡張機能の名前付けのガイドライン](naming-guidelines-extensions.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="bf047-116">For more information, see [Naming guidelines for extensions](naming-guidelines-extensions.md).</span></span>

```xpp
[ExtensionOf(tableStr(InventTable))]
final class InventTableMy_Extension
{
    public void myDefaultInventLocationId()
    {
        // This would have partner specific logic to initialize the new field.
        this.MyInventLocationId = this.inventLocationId();
    }
}
```

<span data-ttu-id="bf047-117">新しいメソッドを強化クラスを追加することができるようになりました。</span><span class="sxs-lookup"><span data-stu-id="bf047-117">You can now add new methods to the augmentation class.</span></span> <span data-ttu-id="bf047-118">これらのメソッドは、テーブルに直接定義されているかのように、**InventTable** 型の変数の IntelliSense に表示されます。</span><span class="sxs-lookup"><span data-stu-id="bf047-118">These methods will then appear in IntelliSense for variables of the **InventTable** type, just as if they were defined directly on the table.</span></span> <span data-ttu-id="bf047-119">この動作は、静的メソッドとインスタンス メソッドの両方に適用されます。</span><span class="sxs-lookup"><span data-stu-id="bf047-119">This behavior applies to both static methods and instance methods.</span></span>

<span data-ttu-id="bf047-120">拡張クラスにはいくつかのルールがあります。</span><span class="sxs-lookup"><span data-stu-id="bf047-120">There are a few rules for augmentation classes:</span></span>

+ <span data-ttu-id="bf047-121">最終である必要があります。</span><span class="sxs-lookup"><span data-stu-id="bf047-121">They must be final.</span></span>
+ <span data-ttu-id="bf047-122">**\_拡張子** で接尾辞を付ける必要があります。</span><span class="sxs-lookup"><span data-stu-id="bf047-122">They must be suffixed by **\_Extension**.</span></span>
+ <span data-ttu-id="bf047-123">**[ExtensionOf()]** 属性で装飾されている必要があります。</span><span class="sxs-lookup"><span data-stu-id="bf047-123">They must be decorated with the **[ExtensionOf()]** attribute.</span></span>

<span data-ttu-id="bf047-124">たとえば、イベント ハンドラーから新しいメソッドを使用できるようになります。</span><span class="sxs-lookup"><span data-stu-id="bf047-124">Now you can use your new method, for example, from an event handler:</span></span>

```xpp
class InventTableMy_EventHandler
{
    [DataEventHandler(tableStr(InventTable), DataEventType::Inserting)]
    public static void InventTable_onInserting(Common sender, DataEventArgs e)
    {
        InventTable inventTable = sender as InventTable;
        // Call the method as if it was defined directly on InventTable.
        inventTable.myDefaultInventLocationId();
    }
}

```

> [!NOTE]
> <span data-ttu-id="bf047-125">イベント ハンドラー クラスには任意の数のイベントのハンドラーが含まれるのが一般的です。</span><span class="sxs-lookup"><span data-stu-id="bf047-125">It is common for event handler classes to contain handlers for any number of events.</span></span> <span data-ttu-id="bf047-126">ただし、イベント ハンドラーを拡張クラスに入れるのは、良い方法では **ありません**。</span><span class="sxs-lookup"><span data-stu-id="bf047-126">However, it is **not** good practice to put event handlers in augmentation classes.</span></span> <span data-ttu-id="bf047-127">そうすることで、イベント ハンドラー メソッドが拡張されたタイプのメソッドとして使用可能となります。</span><span class="sxs-lookup"><span data-stu-id="bf047-127">Doing so makes the event handler methods available as methods on the augmented type.</span></span> <span data-ttu-id="bf047-128">これは、イベント ハンドラーが、その型のメソッドとして明示的にではなく、イベントを通じて呼び出されることを意図しているので正しくありません。</span><span class="sxs-lookup"><span data-stu-id="bf047-128">This is incorrect because the event handler is intended to be called through the event, not explicitly as a method on the type.</span></span>


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]