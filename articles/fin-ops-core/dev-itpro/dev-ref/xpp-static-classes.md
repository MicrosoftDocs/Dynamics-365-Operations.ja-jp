---
title: X++ 静的クラス
description: このトピックでは、 X++ の静的クラスについて説明します。
author: RobinARH
manager: AnnBe
ms.date: 12/02/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Developer
ms.reviewer: rhaertle
ms.custom: 150303
ms.search.region: Global
ms.author: rhaertle
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: cb0735a20985c3b1d2464231f50f202c34586f09
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/13/2020
ms.locfileid: "4408728"
---
# <a name="x-static-classes"></a><span data-ttu-id="579f2-103">X++ 静的クラス</span><span class="sxs-lookup"><span data-stu-id="579f2-103">X++ static classes</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="579f2-104">このトピックでは、 X++ の静的クラス メンバーについて説明します。</span><span class="sxs-lookup"><span data-stu-id="579f2-104">This topic describes static class members in X++.</span></span> <span data-ttu-id="579f2-105">一般に、静的メソッドは次のような場合を対象とします。</span><span class="sxs-lookup"><span data-stu-id="579f2-105">In general, static methods are intended for these cases:</span></span>

-   <span data-ttu-id="579f2-106">このメソッドは、クラス内で宣言されているメンバー変数にアクセスする必要はありません。</span><span class="sxs-lookup"><span data-stu-id="579f2-106">The method has no reason to access the member variables that are declared in the class.</span></span>
-   <span data-ttu-id="579f2-107">このメソッドは、クラスのインスタンス (静的でない) メソッドを呼び出す理由はありません。</span><span class="sxs-lookup"><span data-stu-id="579f2-107">The method has no reason to call any instance (non-static) methods of the class.</span></span>

<span data-ttu-id="579f2-108">静的クラス メンバーを宣言するには、**静的** キーワードを使用します。</span><span class="sxs-lookup"><span data-stu-id="579f2-108">You declare static class members by using the **static** keyword.</span></span> <span data-ttu-id="579f2-109">**静的** キーワードは、存在するクラスのインスタンス数に関係なく、メソッドの 1 つのインスタンスだけを作成するようシステムに指示します。</span><span class="sxs-lookup"><span data-stu-id="579f2-109">The **static** keyword instructs the system to create only one instance of the method, regardless of the number of instances of the class there are.</span></span> <span data-ttu-id="579f2-110">この 1 つのインスタンスは、セッション全体で使用されます。</span><span class="sxs-lookup"><span data-stu-id="579f2-110">This one instance is used throughout your session.</span></span> 

### <a name="static-methods"></a><span data-ttu-id="579f2-111">静的メソッド</span><span class="sxs-lookup"><span data-stu-id="579f2-111">Static methods</span></span>

<span data-ttu-id="579f2-112">このセクションでは、違法コピーを防止するためにソフトウェア キー タイプを使用するシナリオについて説明します。</span><span class="sxs-lookup"><span data-stu-id="579f2-112">This section describes a scenario where a software key type is used to help prevent piracy.</span></span> <span data-ttu-id="579f2-113">ソフトウェア キーの各インスタンスには、固有の値を持つことが可能です。</span><span class="sxs-lookup"><span data-stu-id="579f2-113">Each instance of a software key can have its own unique value.</span></span> <span data-ttu-id="579f2-114">ただし、すべてのソフトウェア キーはソフトウェア キー設計のルールに準拠する必要があるため、ソフトウェア キーへの適合をテストするロジックはすべてのソフトウェア キーに対して同じです。</span><span class="sxs-lookup"><span data-stu-id="579f2-114">Because all software keys must conform to the rules of software key design, the logic that tests for software key conformance is the same for all software keys.</span></span> <span data-ttu-id="579f2-115">したがって、適合性検証ロジックを含むメソッドは静的でなければなりません。</span><span class="sxs-lookup"><span data-stu-id="579f2-115">Therefore, the method that contains the conformance validation logic should be static.</span></span> 

<span data-ttu-id="579f2-116">**静的** キーワード使用して宣言されるメソッドの例を次に示します。</span><span class="sxs-lookup"><span data-stu-id="579f2-116">Here is an example of a method that is declared by using the **static** keyword.</span></span>

```xpp
public class SoftwareKey
{
    static public boolean validateSoftwareKey(str _softwareKeyString)
    {
        // Your code here.
        return false;
    }
}
```

<span data-ttu-id="579f2-117">次の例では、クラスで静的メソッドを呼び出す前に **SoftwareKey** クラスのインスタンスを構築する必要はありません。</span><span class="sxs-lookup"><span data-stu-id="579f2-117">In the following example, you don't have to construct an instance of the **SoftwareKey** class before you call a static method on the class.</span></span> <span data-ttu-id="579f2-118">静的な **validateSoftwareKey** メソッドを呼び出すときは、構文はそのメソッドを含むクラスの名前で始まります。</span><span class="sxs-lookup"><span data-stu-id="579f2-118">When you want to call the static **validateSoftwareKey** method, the syntax starts with the name of the class that contains the method.</span></span> <span data-ttu-id="579f2-119">コロンのペア (::) は、クラス名を静的メソッド名に接続するために使用します。</span><span class="sxs-lookup"><span data-stu-id="579f2-119">A pair of colons (::) is used to connect the class name to the static method name.</span></span>

```xpp
boolean yourBool = SoftwareKey::validateSoftwareKey(yourSoftwareKeyString);
```

### <a name="static-fields"></a><span data-ttu-id="579f2-120">静的フィールド</span><span class="sxs-lookup"><span data-stu-id="579f2-120">Static fields</span></span>

<span data-ttu-id="579f2-121">静的フィールドは、**静的** キーワードを使用して宣言される変数です。</span><span class="sxs-lookup"><span data-stu-id="579f2-121">Static fields are variables that are declared by using the **static** keyword.</span></span> <span data-ttu-id="579f2-122">概念的には、クラスに適用され、クラスのインスタンスには適用されません。</span><span class="sxs-lookup"><span data-stu-id="579f2-122">Conceptually, they apply to the class, not to instances of the class.</span></span>

## <a name="static-constructors"></a><span data-ttu-id="579f2-123">静的コンストラクター</span><span class="sxs-lookup"><span data-stu-id="579f2-123">Static constructors</span></span>

<span data-ttu-id="579f2-124">静的コンストラクターは、静的またはインスタンス呼び出しがクラスに対して行われる前に実行されることが保証されます。</span><span class="sxs-lookup"><span data-stu-id="579f2-124">A static constructor is guaranteed to run before any static or instance calls are made to the class.</span></span> <span data-ttu-id="579f2-125">静的コンストラクターの実行は、ユーザーのセッションに対して相対的です。</span><span class="sxs-lookup"><span data-stu-id="579f2-125">The execution of the static constructor is relative to the user’s session.</span></span> <span data-ttu-id="579f2-126">静的コンストラクターには、次の構文があります。</span><span class="sxs-lookup"><span data-stu-id="579f2-126">The static constructor has the following syntax.</span></span>

```xpp
static void TypeNew()
```

<span data-ttu-id="579f2-127">静的コンストラクターは明示的に呼び出さないでください。</span><span class="sxs-lookup"><span data-stu-id="579f2-127">You never explicitly call the static constructor.</span></span> <span data-ttu-id="579f2-128">コンパイラは、コンストラクターがクラスの他のメソッドの前に正確に 1 回呼び出されるようにするコードを生成します。</span><span class="sxs-lookup"><span data-stu-id="579f2-128">The compiler will generate code to make sure that the constructor is called exactly one time before any other method on the class.</span></span> <span data-ttu-id="579f2-129">静的コンストラクターは、任意の静的データを初期化したり、一度だけ実行する必要のある特定のアクションを実行するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="579f2-129">A static constructor is used to initialize any static data or perform a particular action that must be performed only one time.</span></span> <span data-ttu-id="579f2-130">静的コンストラクターに指定できるパラメーターはなく、**静的** としてマークする必要があります。</span><span class="sxs-lookup"><span data-stu-id="579f2-130">No parameters can be provided for the static constructor, and it must be marked as **static**.</span></span> 

<span data-ttu-id="579f2-131">次のコード例は、静的コンストラクターを使用して単一のインスタンスを作成する方法を示しています。</span><span class="sxs-lookup"><span data-stu-id="579f2-131">The following code example shows how to create a singleton instance by using a static constructor.</span></span>

```xpp
public class Singleton
{
    private static Singleton instance;

    private void new()
    {
    }

    static void TypeNew()
    {
        instance = new Singleton();
    }

    public static Singleton Instance()
    {
        return Singleton::instance;
    }
}
```

<span data-ttu-id="579f2-132">単一は、クラスのインスタンスが 1 つしか呼び出されないことを保証します。</span><span class="sxs-lookup"><span data-stu-id="579f2-132">The singleton guarantees that only one instance of the class will ever be called.</span></span> <span data-ttu-id="579f2-133">次の例は、単一をインスタンス化する方法を示しています。</span><span class="sxs-lookup"><span data-stu-id="579f2-133">The following example shows how to instantiate the singleton.</span></span>

```xpp
Singleton i = Singleton::Instance();
```

## <a name="static-methods"></a><span data-ttu-id="579f2-134">静的メソッド</span><span class="sxs-lookup"><span data-stu-id="579f2-134">Static methods</span></span>

<span data-ttu-id="579f2-135">*クラス メソッド* とも呼ばれる静的メソッドは、クラスに属しており、キーワード **static** を使用して作成されます。</span><span class="sxs-lookup"><span data-stu-id="579f2-135">Static methods, which are also known as *class methods*, belong to a class and are created by using the keyword **static**.</span></span> <span data-ttu-id="579f2-136">静的メソッドを使用する前に、オブジェクトのインスタンスを作成する必要はありません。</span><span class="sxs-lookup"><span data-stu-id="579f2-136">You don't have to instantiate an object before you use static methods.</span></span> <span data-ttu-id="579f2-137">静的メソッドは多くの場合、テーブルに格納されているデータを操作するために使用します。</span><span class="sxs-lookup"><span data-stu-id="579f2-137">Static methods are often used to work with data that is stored in tables.</span></span> <span data-ttu-id="579f2-138">メンバー変数は静的メソッドで使用できません。</span><span class="sxs-lookup"><span data-stu-id="579f2-138">Member variables can't be used in a static method.</span></span> <span data-ttu-id="579f2-139">静的メソッドを呼び出すには、次の構文を使用します。</span><span class="sxs-lookup"><span data-stu-id="579f2-139">You use the following syntax to call static methods.</span></span>

```xpp
ClassName::methodName();
```

## <a name="static-and-instance-methods"></a><span data-ttu-id="579f2-140">静的およびインスタンス メソッド</span><span class="sxs-lookup"><span data-stu-id="579f2-140">Static and instance methods</span></span>

<span data-ttu-id="579f2-141">メソッドのアクセサー キーワードは、どのメソッドが静的であるか、静的でないかに関係なく、同じクラスにある 2 つのメソッド間の呼び出しを制限することはありません。</span><span class="sxs-lookup"><span data-stu-id="579f2-141">The accessor keywords on methods never restrict calls between two methods that are in the same class, regardless of which method is static or non-static.</span></span> <span data-ttu-id="579f2-142">静的メソッドでは、**新しい** コンストラクター メソッドが **プライベート** モディファイアーで修飾されている場合でも、**新しい** コンストラクター メソッドに対する呼び出しは有効です。</span><span class="sxs-lookup"><span data-stu-id="579f2-142">In a static method, calls to the **new** constructor method are valid even if the **new** constructor method is decorated with the **private** modifier.</span></span> <span data-ttu-id="579f2-143">これらの呼び出しの構文では、**新しい** キーワードを使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="579f2-143">The syntax for these calls requires that the **new** keyword be used.</span></span> <span data-ttu-id="579f2-144">静的メソッドのコードは、クラスのインスタンス メソッドを呼び出す前に、独自のクラスのインスタンス オブジェクトを構築する必要があります。</span><span class="sxs-lookup"><span data-stu-id="579f2-144">The code in a static method must construct an instance object of its own class before it can call any instance methods on the class.</span></span>

