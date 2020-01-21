---
title: X++ 継承
description: このトピックでは、X++ の継承について説明します。
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
ms.openlocfilehash: cf5c44ec2442fe12dd992811919bce845d2e9405
ms.sourcegitcommit: 7eae20185944ff7394531173490a286a61092323
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 12/03/2019
ms.locfileid: "2872645"
---
# <a name="x-inheritance"></a><span data-ttu-id="15ab9-103">X++ 継承</span><span class="sxs-lookup"><span data-stu-id="15ab9-103">X++ inheritance</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="15ab9-104">このトピックでは、X++ の継承について、サブクラスを作成する方法とメソッドを上書きする方法を含めて説明します。</span><span class="sxs-lookup"><span data-stu-id="15ab9-104">This topic describes inheritance in X++, including how to create a subclass and override a method.</span></span>

## <a name="creating-a-subclass"></a><span data-ttu-id="15ab9-105">サブクラスを作成しています</span><span class="sxs-lookup"><span data-stu-id="15ab9-105">Creating a subclass</span></span>
<span data-ttu-id="15ab9-106">*サブクラス*は拡張または他のクラスから継承されるクラスです。</span><span class="sxs-lookup"><span data-stu-id="15ab9-106">*Subclasses* are classes that extend or inherit from other classes.</span></span> <span data-ttu-id="15ab9-107">クラスは、他の 1 つのクラスのみ拡張することができます。</span><span class="sxs-lookup"><span data-stu-id="15ab9-107">A class can extend only one other class.</span></span> <span data-ttu-id="15ab9-108">複数の継承はサポートされていません。</span><span class="sxs-lookup"><span data-stu-id="15ab9-108">Multiple inheritance isn't supported.</span></span> <span data-ttu-id="15ab9-109">クラスを拡張する場合、サブクラスが親クラスの (*スーパークラス*) すべてのメソッドと変数を継承します。</span><span class="sxs-lookup"><span data-stu-id="15ab9-109">If you extend a class, the subclass inherits all the methods and variables in the parent class (the *superclass*).</span></span> <span data-ttu-id="15ab9-110">サブクラスを使用すると、より特殊な目的で既存のコードを再利用できます。</span><span class="sxs-lookup"><span data-stu-id="15ab9-110">Subclasses let you reuse existing code for a more specific purpose.</span></span> <span data-ttu-id="15ab9-111">したがって、設計、開発、テストの時間を節約できます。</span><span class="sxs-lookup"><span data-stu-id="15ab9-111">Therefore, they help save you time during design, development, and testing.</span></span> <span data-ttu-id="15ab9-112">スーパークラスの動作をカスタマイズするには、サブクラスのメソッドをオーバーライドします。</span><span class="sxs-lookup"><span data-stu-id="15ab9-112">To customize the behavior of a superclass, override the methods in a subclass.</span></span> <span data-ttu-id="15ab9-113">多くの場合、スーパークラスは、*基本クラス*として知られており、サブクラスは、*派生クラス*として知られています。</span><span class="sxs-lookup"><span data-stu-id="15ab9-113">A superclass is often known as a *base class*, and a subclass is often known as a *derived class*.</span></span>

### <a name="subclass-example"></a><span data-ttu-id="15ab9-114">サブクラスの例</span><span class="sxs-lookup"><span data-stu-id="15ab9-114">Subclass example</span></span>

<span data-ttu-id="15ab9-115">次の例では、まず **Point** という名前のクラスを作成します。</span><span class="sxs-lookup"><span data-stu-id="15ab9-115">The following example first creates a class that is named **Point**.</span></span> <span data-ttu-id="15ab9-116">その後、**Point** クラスを拡張して、**ThreePoint** という新しいクラスを作成します。</span><span class="sxs-lookup"><span data-stu-id="15ab9-116">It then extends the **Point** class to create a new class that is named **ThreePoint**.</span></span>

```xpp
class Point
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
}

class ThreePoint extends Point
{
    // Additional instance fields z. Fields x and y are inherited.
    real z; 

    // Constructor is overridden to initialize z.
    void new(real _x, real _y, real _z)
    {
        // Initialize the fields.
        super(_x, _y); 
        z = _z;
    }
}
```

### <a name="preventing-class-inheritance"></a><span data-ttu-id="15ab9-117">クラスの継承を禁止する</span><span class="sxs-lookup"><span data-stu-id="15ab9-117">Preventing class inheritance</span></span>

<span data-ttu-id="15ab9-118">**最終** モディファイアーを使用して、クラスが継承されないようにすることができます。</span><span class="sxs-lookup"><span data-stu-id="15ab9-118">You can prevent classes from being inherited by using the **final** modifier.</span></span>

```xpp
public final class Attribute
{
    int objectField;
}
```

## <a name="overriding-a-method"></a><span data-ttu-id="15ab9-119">メソッドのオーバーライド</span><span class="sxs-lookup"><span data-stu-id="15ab9-119">Overriding a method</span></span>
<span data-ttu-id="15ab9-120">クラス内のメソッドは、そのクラスを拡張するクラスによって継承されます。</span><span class="sxs-lookup"><span data-stu-id="15ab9-120">The methods in a class are inherited by any class that extends the class.</span></span> <span data-ttu-id="15ab9-121">継承されたメソッドの機能を変更するには、サブクラスでメソッドを作成し、そのメソッドにスーパークラスのメソッドと同じ名前およびパラメーターを指定します。</span><span class="sxs-lookup"><span data-stu-id="15ab9-121">To change the functionality of an inherited method, you create a method in the subclass, and then give that method the same name and parameters as the method in the superclass.</span></span> <span data-ttu-id="15ab9-122">このプロセスは、メソッドを*オーバーライドする*として知られています。</span><span class="sxs-lookup"><span data-stu-id="15ab9-122">This process is known as *overriding* the method.</span></span> <span data-ttu-id="15ab9-123">次の例では、**ColorAttribute** は**属性**のサブクラスであるため、**methodAttr** メソッドを継承します。</span><span class="sxs-lookup"><span data-stu-id="15ab9-123">In the following example, **ColorAttribute** is a subclass of **Attribute** and therefore inherits the **methodAttr** method.</span></span> <span data-ttu-id="15ab9-124">ただし、**ColorAttribute** は同じ名前および同じ数の引数を持つメソッドを定義するため、スーパークラスのメソッドは上書きされます。</span><span class="sxs-lookup"><span data-stu-id="15ab9-124">However, because **ColorAttribute** defines a method that has the same name and the same number of arguments, the method in the superclass is overridden.</span></span>

<span data-ttu-id="15ab9-125">サブクラスのインスタンスを作成するとき、スーパークラスの型の変数またはサブクラスの型の変数のいずれかに照会を割り当てることができます。</span><span class="sxs-lookup"><span data-stu-id="15ab9-125">When you instantiate the subclass, you can assign the reference to either a variable of the superclass type or the subclass type.</span></span> <span data-ttu-id="15ab9-126">変数の型に関係なく、上書きされたメソッドが呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="15ab9-126">Regardless of the type of the variable, the overridden method is called.</span></span> 

<span data-ttu-id="15ab9-127">次のコード例は、サブクラスが **書き込み** メソッドを上書きします。</span><span class="sxs-lookup"><span data-stu-id="15ab9-127">In the following code example, the subclass overrides the **write** method.</span></span> <span data-ttu-id="15ab9-128">2 つの変数、**ポイント** する両方の型が作成されます。</span><span class="sxs-lookup"><span data-stu-id="15ab9-128">Two variables, both of type **Point** are created.</span></span> <span data-ttu-id="15ab9-129">一方に **1 ポイント** オブジェクトが割り当てられ、もう一方には、**3 ポイント** オブジェクトが割り当てられます。</span><span class="sxs-lookup"><span data-stu-id="15ab9-129">One is assigned a **Point** object, the other is assigned a **ThreePoint** object.</span></span> <span data-ttu-id="15ab9-130">**書き込み** メソッドが **3 ポイント** オブジェクトに対して呼び出されるとき、このメソッドの **3 ポイント** バージョンが呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="15ab9-130">When the **write** method is called on the **ThreePoint** object, the **ThreePoint** version of the method is called.</span></span>

```xpp
class Point
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

    void write()
    {
        info("(" + any2Str(x) + ", " + any2Str(y) + ")");
    }
}

class ThreePoint extends Point
{
    // Additional instance fields z. Fields x and y are inherited.
    real z;

    // Constructor is overridden to initialize z.
    void new(real _x, real _y, real _z)
    {
        // Initialize the fields.
        super(_x, _y);
        z = _z;
    }

    void write()
    {
        info("(" + any2Str(x) + ", " + any2Str(y) + ", " + any2Str(z) + ")");
    }

}

// Code that creates Point objects and calls the write method.
Point point2 = new Point(1.0, 2.0);
Point point3 = new ThreePoint(3.0, 4.0, 5.0);

point2.write();
// Output is "(1.0, 2.0)".

point3.write();
// Output is "(3.0, 4.0, 5.0)".
```


### <a name="preventing-method-overrides"></a><span data-ttu-id="15ab9-131">メソッドのオーバーライドを禁止する</span><span class="sxs-lookup"><span data-stu-id="15ab9-131">Preventing method overrides</span></span>

<span data-ttu-id="15ab9-132">静的メソッドは、クラスごとに存在するため上書きすることはできません。</span><span class="sxs-lookup"><span data-stu-id="15ab9-132">Static methods can't be overridden, because they exist per class.</span></span> <span data-ttu-id="15ab9-133">他の重要なメソッドやコア メソッドがオーバーライドされないようにするには、**final** 修飾子を使用します。</span><span class="sxs-lookup"><span data-stu-id="15ab9-133">To protect other sensitive methods, or core methods, from being overridden, use the **final** modifier.</span></span> <span data-ttu-id="15ab9-134">次の例では、**methodAtt** が **final** として宣言されているため、**属性**を拡張するクラスでオーバーライドできません</span><span class="sxs-lookup"><span data-stu-id="15ab9-134">In the following example, because **methodAtt** is declared as **final**, it can't be overridden in any class that extends **Attribute**.</span></span> <span data-ttu-id="15ab9-135">**最終** に **新規** または **確定** のメソッドを指定しないでください。</span><span class="sxs-lookup"><span data-stu-id="15ab9-135">You should not specify **new** or **finalize** methods as **final**.</span></span> 

<span data-ttu-id="15ab9-136">次の例は、**final** キーワードの使用方法を示しています。</span><span class="sxs-lookup"><span data-stu-id="15ab9-136">The following example shows how to use the **final** keyword.</span></span>

```xpp
public class Attribute
{
    int objectVariable;

    final void methodAtt()
    {
        //Some statements
    }
}
```

### <a name="overriding-vs-overloading"></a><span data-ttu-id="15ab9-137">オーバーライドとオーバーロード</span><span class="sxs-lookup"><span data-stu-id="15ab9-137">Overriding vs. overloading</span></span>

<span data-ttu-id="15ab9-138">オーバーライドは、メソッドのスーパークラスの実装がそのメソッドのサブクラスの実装によって変更されるが、両方のメソッドのシグネチャが同じ場合に行われます。</span><span class="sxs-lookup"><span data-stu-id="15ab9-138">Overriding occurs when the superclass's implementation of a method is changed by the subclass's implementation of that method, but the signatures of both methods are the same.</span></span> 

<span data-ttu-id="15ab9-139">対照的に、*オーバーロード*は複数のメソッドが同じ名前を持つ場合に発生しますが、メソッドは異なるシグネチャ (戻り値の型、パラメーター リスト、または両方) を持ちます。</span><span class="sxs-lookup"><span data-stu-id="15ab9-139">By contrast, *overloading* occurs when more than one method has the same name, but the methods have different signatures (return types, parameter lists, or both).</span></span> <span data-ttu-id="15ab9-140">X++ はオーバーライドをサポートしますが、オーバーロードはサポートしていません。</span><span class="sxs-lookup"><span data-stu-id="15ab9-140">X++ supports overriding, but it doesn't support overloading.</span></span>

