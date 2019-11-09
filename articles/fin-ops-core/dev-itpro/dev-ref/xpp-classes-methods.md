---
title: クラスおよびメソッド
description: このトピックでは、X++ でクラスを作成および使用する方法について説明します。
author: RobinARH
manager: AnnBe
ms.date: 06/17/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Developer
ms.reviewer: rhaertle
ms.search.scope: Operations
ms.custom: 150303
ms.assetid: ''
ms.search.region: Global
ms.author: rhaertle
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: f0a91371f696c76286a87882d2a674a6586052a3
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/27/2019
ms.locfileid: "2183356"
---
# <a name="classes-and-methods"></a><span data-ttu-id="d9d51-103">クラスおよびメソッド</span><span class="sxs-lookup"><span data-stu-id="d9d51-103">Classes and methods</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="d9d51-104">このトピックでは、X++ でクラスを作成および使用する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="d9d51-104">This topic describes how to create and use classes in X++.</span></span>

<span data-ttu-id="d9d51-105">*クラス* は、そのクラスから後に構築されるインスタンスのデータおよびメソッドを定義するソフトウェア構造です。</span><span class="sxs-lookup"><span data-stu-id="d9d51-105">A *class* is a software construct that defines the data and methods of the instances that are later constructed from that class.</span></span> <span data-ttu-id="d9d51-106">*クラス* は、問題のあるドメイン内の *オブジェクト* を抽象化したものです。</span><span class="sxs-lookup"><span data-stu-id="d9d51-106">The *class* is an abstraction of an *object* in the problem domain.</span></span> <span data-ttu-id="d9d51-107">この *クラス* から構築されるインスタンスは、*インスタンス* または *オブジェクト* として知られます。</span><span class="sxs-lookup"><span data-stu-id="d9d51-107">The instances that are constructed from the *class* are known as *instances* or *objects*.</span></span> <span data-ttu-id="d9d51-108">このトピックでは、*インスタンス* という用語を使用します。</span><span class="sxs-lookup"><span data-stu-id="d9d51-108">This topic uses the term *instance*.</span></span> <span data-ttu-id="d9d51-109">データはオブジェクトの状態を表し、メソッドはオブジェクトの動作を表します。</span><span class="sxs-lookup"><span data-stu-id="d9d51-109">The data represents the state of the object, whereas the methods represent the behavior of the object.</span></span> <span data-ttu-id="d9d51-110">*変数*にはクラスのデータが含まれます。</span><span class="sxs-lookup"><span data-stu-id="d9d51-110">*Variables* contain the data for the class.</span></span> <span data-ttu-id="d9d51-111">クラス宣言から構築されたすべてのインスタンスには、独自の変数のコピーがあります。</span><span class="sxs-lookup"><span data-stu-id="d9d51-111">Every instance that is constructed from the class declaration has its own copy of the variables.</span></span> <span data-ttu-id="d9d51-112">これらの変数は*インスタンス変数*と呼ばれます。</span><span class="sxs-lookup"><span data-stu-id="d9d51-112">These variables are known as *instance variables*.</span></span> <span data-ttu-id="d9d51-113">メソッドはクラスの動作を定義します。</span><span class="sxs-lookup"><span data-stu-id="d9d51-113">Methods define the behavior of a class.</span></span> <span data-ttu-id="d9d51-114">データに作用する一連の明細書です (インスタンス変数)。</span><span class="sxs-lookup"><span data-stu-id="d9d51-114">They are the sequences of statements that operate on the data (instance variables).</span></span> <span data-ttu-id="d9d51-115">規定では、メソッドはクラスのインスタンス変数に作用するように宣言されます。</span><span class="sxs-lookup"><span data-stu-id="d9d51-115">By default, methods are declared to operate on the instance variables of the class.</span></span> <span data-ttu-id="d9d51-116">これらのメソッドは、*instance メソッド*または *object メソッド*と呼ばれます。</span><span class="sxs-lookup"><span data-stu-id="d9d51-116">These methods are known as *instance methods* or *object methods*.</span></span> 

<span data-ttu-id="d9d51-117">*インスタンス変数* にアクセスできない *静的メソッド* および *静的フィールド* を宣言できます。</span><span class="sxs-lookup"><span data-stu-id="d9d51-117">You can declare *static methods* and *static fields*, that do not have access to *instance variables*.</span></span> <span data-ttu-id="d9d51-118">これらについては、[静的クラス メンバー](xpp-static-classes.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="d9d51-118">These are described in [Static class members](xpp-static-classes.md).</span></span>

## <a name="declare-a-class"></a><span data-ttu-id="d9d51-119">クラスを宣言します</span><span class="sxs-lookup"><span data-stu-id="d9d51-119">Declare a class</span></span>

<span data-ttu-id="d9d51-120">プロジェクトにクラスを追加するには、Visual Studio で **新しい項目の追加** ダイアログを使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="d9d51-120">You must use the **Add new item** dialog in Visual Studio to add a class to your project.</span></span> 

1.  <span data-ttu-id="d9d51-121">サーバー エクスプローラーで、プロジェクトを右クリックしてから**追加**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="d9d51-121">In Server Explorer, right-click the project, and then click **Add**.</span></span>
2.  <span data-ttu-id="d9d51-122">**新しい項目** のダイアログ ボックスの左側のナビゲーションで、**インストール済み > Dynamics 365 品目 > Code** の順に選択します。</span><span class="sxs-lookup"><span data-stu-id="d9d51-122">In the **New Item** dialog box, select **Installed > Dynamics 365 Items > Code** in the left navigation.</span></span> <span data-ttu-id="d9d51-123">その後、**クラス** を選択し、クラス名を入力します。</span><span class="sxs-lookup"><span data-stu-id="d9d51-123">Then select **Class**, and then enter a name for the class.</span></span>
3.  <span data-ttu-id="d9d51-124">**追加**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="d9d51-124">Click **Add**.</span></span>

<span data-ttu-id="d9d51-125">すべてのクラスはパブリックです。</span><span class="sxs-lookup"><span data-stu-id="d9d51-125">All classes are public.</span></span> <span data-ttu-id="d9d51-126">**パブリック** モディファイアーを削除すると、システムではクラスはパブリック クラスとして扱われます。</span><span class="sxs-lookup"><span data-stu-id="d9d51-126">If you remove the **public** modifier, the system still treats the class as public.</span></span> <span data-ttu-id="d9d51-127">クラス宣言では、**final** および **extends** などの、他の修飾子を指定することができます。</span><span class="sxs-lookup"><span data-stu-id="d9d51-127">You can specify other modifiers on the class declaration, such as **final** and **extends**.</span></span>

## <a name="variables"></a><span data-ttu-id="d9d51-128">変数</span><span class="sxs-lookup"><span data-stu-id="d9d51-128">Variables</span></span>

<span data-ttu-id="d9d51-129">インスタンス変数は既定で**保護**されます。</span><span class="sxs-lookup"><span data-stu-id="d9d51-129">Instance variables are **protected** by default.</span></span> <span data-ttu-id="d9d51-130">これは、同じクラスまたは [派生クラス](xpp-inheritance.md) の中でしかアクセスできないことを意味します。</span><span class="sxs-lookup"><span data-stu-id="d9d51-130">This means that they can only be accessed in the same class or [a derived class](xpp-inheritance.md).</span></span> <span data-ttu-id="d9d51-131">ただし、**秘密**、**保護**、または**パブリック**キーワードを使用してインスタンス変数宣言を変更することができます。</span><span class="sxs-lookup"><span data-stu-id="d9d51-131">You can modify and instance variable declaration by using the **private**, **protected**, or **public** keywords.</span></span> 

<span data-ttu-id="d9d51-132">次の例は、アクセサー メソッドを使用して変数データを公開する方法を示しています。</span><span class="sxs-lookup"><span data-stu-id="d9d51-132">The following example shows how to use accessor methods to make the variable data public.</span></span> <span data-ttu-id="d9d51-133">変数 **名**は保護されるため、プロテクト変数へのアクセスを許可するために、アクセサー (取得と設定) メソッドが実装されます。</span><span class="sxs-lookup"><span data-stu-id="d9d51-133">The variable **firstName** is protected, so accessor (get and set) methods are implemented to allow access to the protected variable.</span></span> <span data-ttu-id="d9d51-134">変数**姓**は公開されているため、コードで変数の値を直接取得して設定することができます。</span><span class="sxs-lookup"><span data-stu-id="d9d51-134">The variable **lastName** is public, so code can directly get and set the value of the variable.</span></span>

```X++
// This is the class definition.
public class HasAFirstName
{
    str firstName;
    public str lastName;
    public str getFirstName()
    {
        return firstName;
    }

    public void setFirstName(str newName)
    {
       firstName = newName;
    }
}

// This code creates an instance of the class and gets the variables.
public static void TestLastName()
{
    HasAFirstName hasFirstName = new HasAFirstName();
    hasFirstName.setFirstName("Dion");
    info(hasFirstName.getFirstName());
    hasFirstName.lastName = ("Townes");
    info(hasFirstName.lastName);
}
// The output is "Dion" and "Townes".
```

## <a name="constructors"></a><span data-ttu-id="d9d51-135">コンストラクター</span><span class="sxs-lookup"><span data-stu-id="d9d51-135">Constructors</span></span>

<span data-ttu-id="d9d51-136">クラスのインスタンスを作成するには、*コンストラクタ*を使用してクラスのインスタンスを生成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="d9d51-136">To create an instance of a class, you must instantiate it by using a *constructor*.</span></span> 

+ <span data-ttu-id="d9d51-137">クラスでは、**新しい** メソッド (コンストラクター) を 1 つだけ定義できます。</span><span class="sxs-lookup"><span data-stu-id="d9d51-137">You can define only one **new** method (constructor) in a class.</span></span> 
+ <span data-ttu-id="d9d51-138">コンストラクターを定義しない場合は、パラメーターのない既定のコンストラクターが、コンパイラによって自動的に作成されます。</span><span class="sxs-lookup"><span data-stu-id="d9d51-138">If you do not define a constructor, a default constructor with no parameters is created automatically by the compiler.</span></span> 
+ <span data-ttu-id="d9d51-139">既定のコンストラクターは、**新しい** メソッドでパラメーターに既定値を割り当てることによってシミュレーションできます。</span><span class="sxs-lookup"><span data-stu-id="d9d51-139">You can simulate a default constructor by assigning default values to the parameters in the **new** method.</span></span>

<span data-ttu-id="d9d51-140">次の例では、**ポイント** クラスのパラメーターなしのコンストラクターを定義しています。</span><span class="sxs-lookup"><span data-stu-id="d9d51-140">The following examples defines a parameterless constructor in the **Point** class.</span></span>

```X++
class Point
{

    // Instance variables that are public. In practice, you would probably make this protected or private 
    // and create accessor methods.
    public real x = 0.0;
    public real y = 0.0;

    void new() {
    }
}
```

<span data-ttu-id="d9d51-141">次に、クリーンな継承モデルを作成し、コードがアップグレードされたときの問題を最小限に抑える方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="d9d51-141">Following is information about how to create a clean inheritance model and minimize problems when code is upgraded:</span></span>

  - <span data-ttu-id="d9d51-142">抽象クラスでない場合、各クラスは単一のパブリック構築メソッドを持つ必要があります。</span><span class="sxs-lookup"><span data-stu-id="d9d51-142">Each class must have a single public construction method unless the class is abstract.</span></span> <span data-ttu-id="d9d51-143">初期化が不要な場合は、静的コンストラクトのメソッドを使用します。</span><span class="sxs-lookup"><span data-stu-id="d9d51-143">If no initialization is required, use a static construct method.</span></span> <span data-ttu-id="d9d51-144">それ以外の場合は、静的な **新しい** メソッドを使用します (クラスの既定のコンストラクターは保護する必要があります)。</span><span class="sxs-lookup"><span data-stu-id="d9d51-144">Otherwise, use a static **new** method (the default constructor for the class should be protected).</span></span>
  - <span data-ttu-id="d9d51-145">各クラスは少なくとも 1 つの静的 **コンストラクト** メソッドを持つ必要があります。</span><span class="sxs-lookup"><span data-stu-id="d9d51-145">Each class should have at least one static **construct** method method.</span></span>
  - <span data-ttu-id="d9d51-146">各クラスは少なくとも 1 つの **新しい** 静的メソッドを持つ必要があります。</span><span class="sxs-lookup"><span data-stu-id="d9d51-146">Each class should have at least one static **new** method.</span></span>
  - <span data-ttu-id="d9d51-147">各クラスに**新しい**メソッド (既定のコンストラクター) が必要です。</span><span class="sxs-lookup"><span data-stu-id="d9d51-147">Each class should have a **new** method (the default constructor).</span></span> <span data-ttu-id="d9d51-148">このメソッドは**保護**する必要があります。</span><span class="sxs-lookup"><span data-stu-id="d9d51-148">This method should be **protected**.</span></span>
  - <span data-ttu-id="d9d51-149">クラス変数を取得および設定するためのアクセサー メソッドを作成します。</span><span class="sxs-lookup"><span data-stu-id="d9d51-149">Create accessor methods to get and set class variables.</span></span>
  - <span data-ttu-id="d9d51-150">インスタンス化の後に実行する必要のある特殊な初期化タスクを実行するための **init** メソッドを作成します。</span><span class="sxs-lookup"><span data-stu-id="d9d51-150">Create **init** methods to carry out any specialized initialization tasks that should be carried out after instantiation.</span></span>

### <a name="create-other-objects-in-a-constructor"></a><span data-ttu-id="d9d51-151">コンストラクターでその他のオブジェクトを作成する</span><span class="sxs-lookup"><span data-stu-id="d9d51-151">Create other objects in a constructor</span></span>

<span data-ttu-id="d9d51-152">クラス コンストラクターは、クラスのインスタンスを作成するだけでなく、他のオブジェクトをインスタンス化することもできます。</span><span class="sxs-lookup"><span data-stu-id="d9d51-152">A class constructor can instantiate other objects in addition to creating an instance of the class.</span></span> <span data-ttu-id="d9d51-153">たとえば、次のコードは、境界を定義するため 2 つの**ポイント**オブジェクトを使用する**長方形**クラスを申告します。</span><span class="sxs-lookup"><span data-stu-id="d9d51-153">For example, the following code declares a **Rectangle** class that uses two **Point** objects to define its bounds.</span></span> <span data-ttu-id="d9d51-154">この場合、**ポイント** クラスには 2 つの **実数** パラメーターを持つコンストラクターが存在します。</span><span class="sxs-lookup"><span data-stu-id="d9d51-154">In this case, the **Point** class has a constructor that has two **real** parameters.</span></span>

```X++

class Point
{
    // Instance variables that are public. In practice, you would probably make this protected or private
    // and create accessor methods.
    public real x = 0.0;
    public real y = 0.0;

    // Constructor to initialize to a specific or default value
    void new(real _x = 10, real _y = 10)
    {
        x = _x;
        y = _y;
    }
}

class Rectangle
{
    public Point lowerLeft;
    public Point upperRight;

    void new(real _topLeftX = 0.0, real _topLeftY = 0.0, real _bottomRightX = 1.0, real _bottomRightY = 1.0)
    {
        lowerLeft  = new Point(_topLeftX, _topLeftY);
        upperRight = new Point(_bottomRightX, _bottomRightY);
    }

}

// This code creates two instances of the Rectangle class.
Rectangle defaultRectangle = new Rectangle();
info(any2Str(defaultRectangle.lowerLeft.x));
info(any2Str(defaultRectangle.lowerLeft.y));
// Output is "0.0" and "0.0".

Rectangle customRectangle = new Rectangle(1.0, 1.0, 2.0, 2.0);
info(any2Str(customRectangle.lowerLeft.x));
info(any2Str(customRectangle.lowerLeft.y));
// Output is "1.0" and "1.0".
```

## <a name="create-an-instance-of-an-object"></a><span data-ttu-id="d9d51-155">オブジェクトのインスタンスを作成する</span><span class="sxs-lookup"><span data-stu-id="d9d51-155">Create an instance of an object</span></span>

<span data-ttu-id="d9d51-156">コンストラクター、**新規**は、クラスの新しいインスタンスを返します。</span><span class="sxs-lookup"><span data-stu-id="d9d51-156">The constructor, **new**, returns a new instance of the class.</span></span> <span data-ttu-id="d9d51-157">次のコード例は、ポイント クラスのインスタンスを 2 つ作成する方法を示しています。</span><span class="sxs-lookup"><span data-stu-id="d9d51-157">The following code example creates two instances of the Point class.</span></span>

```X++
// Declare a variable to refer to a Point instance.
Point myPoint;

// Create an instance of the Point class.
myPoint = new Point();

// Declare and instantiate a Point instance.
Point ap = new Point();
```

## <a name="destructors"></a><span data-ttu-id="d9d51-158">デストラクター</span><span class="sxs-lookup"><span data-stu-id="d9d51-158">Destructors</span></span>
<span data-ttu-id="d9d51-159">*デストラクター* は、クラス インスタンスを明示的に破棄するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="d9d51-159">You use a *destructor* to explicitly destroy a class instance.</span></span> <span data-ttu-id="d9d51-160">インスタンスは、インスタンスに関する参照がない場合は自動的に破棄されます。</span><span class="sxs-lookup"><span data-stu-id="d9d51-160">Instances are automatically destroyed when there are no references to them.</span></span> <span data-ttu-id="d9d51-161">ただし、たとえば、次の方法で対象を明示的に破棄できます。</span><span class="sxs-lookup"><span data-stu-id="d9d51-161">However, you can destroy objects explicitly in the following ways:</span></span>

-   <span data-ttu-id="d9d51-162">**finalize** メソッドを使用します。</span><span class="sxs-lookup"><span data-stu-id="d9d51-162">Use the **finalize** method.</span></span>
-   <span data-ttu-id="d9d51-163">参照変数を **Null** に設定します。</span><span class="sxs-lookup"><span data-stu-id="d9d51-163">Set the reference variable to **null**.</span></span>

### <a name="use-the-finalize-method"></a><span data-ttu-id="d9d51-164">ファイナライズ メソッドを使用する</span><span class="sxs-lookup"><span data-stu-id="d9d51-164">Use the finalize method</span></span>

<span data-ttu-id="d9d51-165">オブジェクトを明示的に破棄するには **finalize** メソッドを使用します。</span><span class="sxs-lookup"><span data-stu-id="d9d51-165">Use the **finalize** method to explicitly destroy an object.</span></span> <span data-ttu-id="d9d51-166">**finalize** メソッドへの暗黙的な呼び出しはありません。</span><span class="sxs-lookup"><span data-stu-id="d9d51-166">There are no implicit calls to the **finalize** method.</span></span> <span data-ttu-id="d9d51-167">そこでステートメントを実行するメソッドを呼び出す必要があります。</span><span class="sxs-lookup"><span data-stu-id="d9d51-167">You must call the method to run the statements in it.</span></span> <span data-ttu-id="d9d51-168">**finalize** メソッドでは、必要なクリーンアップ コードも配置する必要があります。</span><span class="sxs-lookup"><span data-stu-id="d9d51-168">In the **finalize** method, you should also put any clean-up code that is required.</span></span> <span data-ttu-id="d9d51-169">たとえば、クラスがダイナミックリンク ライブラリ (DLL) モジュールを使用する場合、必要ではなくなったときに DLL をリリースする**確定**メソッドを使用できます。</span><span class="sxs-lookup"><span data-stu-id="d9d51-169">For example, if your class uses a dynamic-link library (DLL) module, you can use the **finalize** method to release the DLL when you no longer require it.</span></span> <span data-ttu-id="d9d51-170">**finalize** メソッドは慎重に使用してください。</span><span class="sxs-lookup"><span data-stu-id="d9d51-170">Use the **finalize** method carefully.</span></span> <span data-ttu-id="d9d51-171">オブジェクトへの参照がある場合オブジェクトを破棄します。</span><span class="sxs-lookup"><span data-stu-id="d9d51-171">It will destroy an object even if there are references to it.</span></span>

<span data-ttu-id="d9d51-172">次の例は、**finalize** メソッドの呼び出しの基本構造を示しています。</span><span class="sxs-lookup"><span data-stu-id="d9d51-172">The following example shows the basic structure for a call to the **finalize** method.</span></span>

```X++
// From any method in a class.
if (condition)
{
    // Removes object from memory.
    this.finalize(); 
}
```

### <a name="set-reference-variable-to-null"></a><span data-ttu-id="d9d51-173">参照変数を Null に設定する</span><span class="sxs-lookup"><span data-stu-id="d9d51-173">Set reference variable to null</span></span>

<span data-ttu-id="d9d51-174">参照変数を **Null** に設定してオブジェクトを終了します。</span><span class="sxs-lookup"><span data-stu-id="d9d51-174">Set the reference variable to **null** to terminate an object.</span></span> <span data-ttu-id="d9d51-175">この方法を使用すると、他の変数がそのオブジェクトをポイントしていない場合にのみオブジェクトが破棄されます。</span><span class="sxs-lookup"><span data-stu-id="d9d51-175">This approach destroys an object only if no other variables point to that object.</span></span> <span data-ttu-id="d9d51-176">他のコードが変数を使用していないことを確認する必要があります。</span><span class="sxs-lookup"><span data-stu-id="d9d51-176">You should verify that other code isn't using the variable.</span></span> <span data-ttu-id="d9d51-177">次の例では、参照変数を作成して、**Null** に設定する方法を示します。</span><span class="sxs-lookup"><span data-stu-id="d9d51-177">The following example creates an reference variable and then sets it to **null**.</span></span>

```X++
Point myPoint = new Point();
myPoint = null;
```

## <a name="methods"></a><span data-ttu-id="d9d51-178">メソッド</span><span class="sxs-lookup"><span data-stu-id="d9d51-178">Methods</span></span>

### <a name="instance-methods"></a><span data-ttu-id="d9d51-179">インスタンス メソッド</span><span class="sxs-lookup"><span data-stu-id="d9d51-179">Instance methods</span></span>

<span data-ttu-id="d9d51-180">インスタンス メソッドは、クラスから作成される各インスタンスに埋め込まれます。</span><span class="sxs-lookup"><span data-stu-id="d9d51-180">Instance methods are embedded in each instance that is created from the class.</span></span> <span data-ttu-id="d9d51-181">メソッドの使用前に、オブジェクトのインスタンスを作成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="d9d51-181">You must instantiate the object before you can use the method.</span></span> <span data-ttu-id="d9d51-182">次のコードは、インスタンス メソッドを定義して、それをインスタンスから呼び出す方法を示しています。</span><span class="sxs-lookup"><span data-stu-id="d9d51-182">The following code shows how to define an instance method and call it from an instance.</span></span>

```X++
class Square
{

    int side = 0;

    void new(int _side = 1) {
        side = _side;
    }

    int getArea() {
        return side * side;
    }

}

// This code creates an instance of Square and calls getArea.
Square square = new Square(15);
int area = square.getArea();
info(int2Str(area));
// Output is "225".
```

### <a name="static-methods"></a><span data-ttu-id="d9d51-183">静的メソッド</span><span class="sxs-lookup"><span data-stu-id="d9d51-183">Static methods</span></span>

<span data-ttu-id="d9d51-184">*クラス メソッド*とも呼ばれる静的メソッドは、クラスに属しており、キーワード **static** を使用して作成されます。</span><span class="sxs-lookup"><span data-stu-id="d9d51-184">Static methods, which are also known as *class methods*, belong to a class and are created by using the keyword **static**.</span></span> <span data-ttu-id="d9d51-185">静的メソッドを使用する前に、オブジェクトのインスタンスを作成する必要はありません。</span><span class="sxs-lookup"><span data-stu-id="d9d51-185">You don't have to instantiate an object before you use static methods.</span></span> <span data-ttu-id="d9d51-186">静的メソッドは多くの場合、テーブルに格納されているデータを操作するために使用します。</span><span class="sxs-lookup"><span data-stu-id="d9d51-186">Static methods are often used to work with data that is stored in tables.</span></span> <span data-ttu-id="d9d51-187">メンバー変数は静的メソッドで使用できません。</span><span class="sxs-lookup"><span data-stu-id="d9d51-187">Member variables can't be used in a static method.</span></span> <span data-ttu-id="d9d51-188">静的メソッドを呼び出すには、次の構文を使用します。</span><span class="sxs-lookup"><span data-stu-id="d9d51-188">You use the following syntax to call static methods.</span></span>

```X++
    ClassName::methodName();
```

<span data-ttu-id="d9d51-189">インスタンス メソッドを静的メソッドに変換する場合は、クライアントを再起動する必要があります。</span><span class="sxs-lookup"><span data-stu-id="d9d51-189">If you convert an instance method to a static method, you must restart the client.</span></span> <span data-ttu-id="d9d51-190">それ以外の場合、コンパイラは変更を検出しません。</span><span class="sxs-lookup"><span data-stu-id="d9d51-190">Otherwise, the compiler doesn't detect the change.</span></span> <span data-ttu-id="d9d51-191">インスタンス メソッドを静的メソッドに変換した後は、クラスのインスタンスからメソッドを呼び出すことができなくなります。</span><span class="sxs-lookup"><span data-stu-id="d9d51-191">After you've converted an instance method to a static method, you can no longer call the method from the instance of the class.</span></span> <span data-ttu-id="d9d51-192">代わりに、クラス自体からメソッドを呼び出す必要があります。</span><span class="sxs-lookup"><span data-stu-id="d9d51-192">Instead, you must call the method from the class itself.</span></span> <span data-ttu-id="d9d51-193">静的メソッドの詳細については、[静的クラス メンバー](xpp-static-classes.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="d9d51-193">For more information about static methods, see [Static class members](xpp-static-classes.md).</span></span>

### <a name="main-methods"></a><span data-ttu-id="d9d51-194">主要メソッド</span><span class="sxs-lookup"><span data-stu-id="d9d51-194">main methods</span></span>

<span data-ttu-id="d9d51-195">**メイン**メソッドは、メニュー オプションから直接実行されるクラス メソッドです。</span><span class="sxs-lookup"><span data-stu-id="d9d51-195">A **main** method is a class method that is run directly from a menu option.</span></span> <span data-ttu-id="d9d51-196">このメソッドでは、オブジェクトのインスタンスを作成してから、必要なメンバー メソッドを呼び出す必要があります。</span><span class="sxs-lookup"><span data-stu-id="d9d51-196">The method should only create an instance of the object and then call the required member methods.</span></span> <span data-ttu-id="d9d51-197">**\_args** パラメーターを使用して、メソッドにデータを転送できます。</span><span class="sxs-lookup"><span data-stu-id="d9d51-197">The **\_args** parameter lets you transfer data to the method.</span></span>

```X++
static void main (Args _args)
{
    // Your code here.
}
```

### <a name="declaration-of-methods"></a><span data-ttu-id="d9d51-198">メソッドの宣言</span><span class="sxs-lookup"><span data-stu-id="d9d51-198">Declaration of methods</span></span>

<span data-ttu-id="d9d51-199">メソッドの宣言は、ヘッダーと本文で構成されます。</span><span class="sxs-lookup"><span data-stu-id="d9d51-199">Method declarations consist of a header and a body.</span></span> <span data-ttu-id="d9d51-200">メソッド ヘッダーは、メソッドの名前と戻り値の型、メソッド モディファイア、およびパラメーターを宣言します。</span><span class="sxs-lookup"><span data-stu-id="d9d51-200">The method header declares the method's name and return type), the method modifiers, and parameters.</span></span> <span data-ttu-id="d9d51-201">(戻り値の型が**無効**である可能性があります。) メソッド本体は、変数宣言、メソッド宣言、および明細書で構成されます。</span><span class="sxs-lookup"><span data-stu-id="d9d51-201">(The return type might be **void**.) The method body consists of variable declarations, method declarations, and statements.</span></span>

### <a name="return-type"></a><span data-ttu-id="d9d51-202">戻り値の型</span><span class="sxs-lookup"><span data-stu-id="d9d51-202">Return type</span></span>

<span data-ttu-id="d9d51-203">各メソッドには、戻り値の型が必要です。</span><span class="sxs-lookup"><span data-stu-id="d9d51-203">A return type is required for each method.</span></span> <span data-ttu-id="d9d51-204">メソッドが何も返さない場合、**無効**キーワードを戻り値の型として使用します。</span><span class="sxs-lookup"><span data-stu-id="d9d51-204">If a method doesn't return anything, use the **void** keyword as the return type.</span></span> <span data-ttu-id="d9d51-205">次の例は、2 つのメソッドを示しています。</span><span class="sxs-lookup"><span data-stu-id="d9d51-205">The following example shows two methods.</span></span> <span data-ttu-id="d9d51-206">1 つの方法に戻り値の型がありますが、他の方法には戻り値の型がありません。</span><span class="sxs-lookup"><span data-stu-id="d9d51-206">One method has a return type, but the other method doesn't have a return type.</span></span>

```X++
    void methodNameNoReturnValue()
    {
        // Your code here.
    }

    // If a method returns something, you must specify the return type and include a return statement.
    int methodNameIntegerReturnValue()
    {
        return 1;
    }
```

### <a name="syntax"></a><span data-ttu-id="d9d51-207">構文</span><span class="sxs-lookup"><span data-stu-id="d9d51-207">Syntax</span></span>

<span data-ttu-id="d9d51-208">メソッド宣言 = *見出し*  *本文* 見出し = **\[** *モディファイアー* **\]**  *戻り値の型*  *MethodName*  **(**  *パラメーター リスト*  **)**</span><span class="sxs-lookup"><span data-stu-id="d9d51-208">Method declaration = *Heading*  *Body* Heading = **\[** *Modifiers* **\]**  *ReturnType*  *MethodName*  **(**  *ParameterList*  **)**</span></span> 

<span data-ttu-id="d9d51-209">モディファイアー = **\[クライアント\] \[サーバー\] \[編集 | 表示 | パブリック | 保護 |プライベート\] \[静的 | 抽象 | 最終\]**</span><span class="sxs-lookup"><span data-stu-id="d9d51-209">Modifiers = **\[client\] \[server\] \[edit | display | public | protected | private\] \[static | abstract | final \]**</span></span> 

<span data-ttu-id="d9d51-210">戻り値の型 = *データ型*  **| 無効 | anytype** MethodName = *識別子*</span><span class="sxs-lookup"><span data-stu-id="d9d51-210">ReturnType = *Datatype*  **| void | anytype** MethodName = *Identifier*</span></span> 

<span data-ttu-id="d9d51-211">パラメーター リスト = **\[** *パラメーター* \**{、\*\*\*パラメーター* **}\]**</span><span class="sxs-lookup"><span data-stu-id="d9d51-211">ParameterList = **\[** *Parameter*  **{ ,**  *Parameter*  **}\]**</span></span> 

<span data-ttu-id="d9d51-212">パラメーター = *データ型* *変数識別子* **\[ =**  *式*  **\]**</span><span class="sxs-lookup"><span data-stu-id="d9d51-212">Parameter = *Datatype*  *Variableidentifier*  **\[ =**  *Expression*  **\]**</span></span> 

<span data-ttu-id="d9d51-213">本文 = **{ \[**  *変数宣言*  **\] \[**  *埋め込み関数用の宣言*  **\] \[**  *明細書*  **\] }**</span><span class="sxs-lookup"><span data-stu-id="d9d51-213">Body = **{ \[**  *VariableDeclarations*  **\] \[**  *EmbeddedFunctionDeclarations*  **\] \[**  *Statements*  **\] }**</span></span> 

<span data-ttu-id="d9d51-214">埋め込み関数用の宣言 = *見出し*  **{\[**  *変数宣言*  **\] \[**  *明細書*  **\]}**</span><span class="sxs-lookup"><span data-stu-id="d9d51-214">EmbeddedFunctionDeclaration = *Heading*  **{\[**  *VariableDeclarations*  **\] \[**  *Statements*  **\]}**</span></span> 

<span data-ttu-id="d9d51-215">**Anytype** 戻り値の型を使用すると、メソッドは任意のデータ型を返すことができます。</span><span class="sxs-lookup"><span data-stu-id="d9d51-215">If you use the **anytype** return type, the method can return any data type.</span></span>

### <a name="example-of-a-method-that-doesnt-have-a-return-type"></a><span data-ttu-id="d9d51-216">戻り値の型を設定していないメソッドの例</span><span class="sxs-lookup"><span data-stu-id="d9d51-216">Example of a method that doesn't have a return type</span></span>

```X++
void update ()
{   
    // Variable declared and initialized
    CustTable this_Orig = this.orig();

    // First statement in body (begin transaction)
    ttsBegin;
    this.setNameAlias();
    // Calls super's implementation of update
    super();
    this.setAccountOnVend(this_Orig);
    if (this_Orig.custGroup != this.custGroup)
        ForecastSales::setCustGroupId(
            this.accountNum,
            this_Orig.custGroup,
            this.custGroup);
    // Commits transaction
    ttsCommit;
}
```

### <a name="example-of-a-method-that-has-parameters"></a><span data-ttu-id="d9d51-217">パラメーターを持つメソッドの例</span><span class="sxs-lookup"><span data-stu-id="d9d51-217">Example of a method that has parameters</span></span>

<span data-ttu-id="d9d51-218">次の例では、**checkAccountBlocked** メソッドはブール値を返し、**amountCur** パラメーターで動作します。</span><span class="sxs-lookup"><span data-stu-id="d9d51-218">In the following example, the **checkAccountBlocked** method returns a Boolean value and acts on the **amountCur** parameter.</span></span>

```X++
boolean checkAccountBlocked(AmountCur amountCur)
{
    if (this.blocked == CustVendorBlocked::All 
        ||(this.blocked == CustVendorBlocked::Invoice 
        && amountCur > 0 ))
    return checkFailed(strFmt("@SYS7987",this.accountNum));
    return true;
}
```

## <a name="method-modifiers"></a><span data-ttu-id="d9d51-219">メソッド modifiers</span><span class="sxs-lookup"><span data-stu-id="d9d51-219">Method modifiers</span></span>
<span data-ttu-id="d9d51-220">いくつかのモディファイアーは、メソッドの宣言に適用することができます。</span><span class="sxs-lookup"><span data-stu-id="d9d51-220">Several modifiers can be applied to method declarations.</span></span> <span data-ttu-id="d9d51-221">一部の修飾子を結合できます (たとえば、**final static**)。</span><span class="sxs-lookup"><span data-stu-id="d9d51-221">Some of the modifiers can be combined (for example, **final static**).</span></span> <span data-ttu-id="d9d51-222">メソッド モディファイア キーワードを次に示します。</span><span class="sxs-lookup"><span data-stu-id="d9d51-222">Here are the method modifier keywords:</span></span>

-   <span data-ttu-id="d9d51-223">**抽象**: メソッドは宣言されていますが、親クラスで実装されていません。</span><span class="sxs-lookup"><span data-stu-id="d9d51-223">**abstract**: The method is declared but isn't implemented in a parent class.</span></span> <span data-ttu-id="d9d51-224">このメソッドはサブクラスで上書きする必要があります。</span><span class="sxs-lookup"><span data-stu-id="d9d51-224">The method must be overridden in subclasses.</span></span> <span data-ttu-id="d9d51-225">サブクラスに親クラスに属する 1 つ以上の抽象メソッドがあり、オーバーライドされていません。そのサブクラスからオブジェクトを作成しようとすると、コンパイラ エラーが発生します。</span><span class="sxs-lookup"><span data-stu-id="d9d51-225">If you try to create an object from a subclass where one or more abstract methods that belong to the parent class haven't been overridden, you receive a compiler error.</span></span> <span data-ttu-id="d9d51-226">クラスは抽象クラスにすることもできます。</span><span class="sxs-lookup"><span data-stu-id="d9d51-226">Classes can also be abstract.</span></span> <span data-ttu-id="d9d51-227">場合によっては、抽象的な概念を表す場合でもクラスをインスタンス化しないでください。</span><span class="sxs-lookup"><span data-stu-id="d9d51-227">Sometimes, a class should not be instantiated even though it represents an abstract concept.</span></span> <span data-ttu-id="d9d51-228">サブクラスのみインスタンスを作成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="d9d51-228">Only subclasses should be instantiated.</span></span> <span data-ttu-id="d9d51-229">このタイプの基本クラスは**抽象**として宣言できます。</span><span class="sxs-lookup"><span data-stu-id="d9d51-229">Base classes of this type can be declared as **abstract**.</span></span> <span data-ttu-id="d9d51-230">たとえば、勘定の概念をモデル化します。</span><span class="sxs-lookup"><span data-stu-id="d9d51-230">For example, you want to model the concept of an account.</span></span> <span data-ttu-id="d9d51-231">実際の世界には派生クラス (勘定科目など) しか存在しないため、勘定は抽象です。</span><span class="sxs-lookup"><span data-stu-id="d9d51-231">Accounts are abstract, because only derived classes (ledger accounts and so on) exist in the real world.</span></span> <span data-ttu-id="d9d51-232">この例では、**勘定** クラスを**抽象**として宣言する必要があるという明確なケースについて説明します。</span><span class="sxs-lookup"><span data-stu-id="d9d51-232">This examples describes a clear case where you should declare the **Account** class as **abstract**.</span></span>
-   <span data-ttu-id="d9d51-233">**ディスプレイ**: メソッドの戻り値は、ページまたはレポートに表示される必要があります。</span><span class="sxs-lookup"><span data-stu-id="d9d51-233">**display**: The method's return value should be shown on a page or a report.</span></span> <span data-ttu-id="d9d51-234">ページまたはレポートで値を変更することはできません。</span><span class="sxs-lookup"><span data-stu-id="d9d51-234">The value can't be modified on the page or report.</span></span> <span data-ttu-id="d9d51-235">通常、戻り値は合計などの計算された値です。</span><span class="sxs-lookup"><span data-stu-id="d9d51-235">Typically, the return value is a calculated value, such as a sum.</span></span>
-   <span data-ttu-id="d9d51-236">**編集**: メソッドの戻り値のタイプは、ページで使用されるフィールドの情報を提供するために使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="d9d51-236">**edit**: The method's return type should be used to provide information for a field that is used on a page.</span></span> <span data-ttu-id="d9d51-237">このフィールドの値は修正できます。</span><span class="sxs-lookup"><span data-stu-id="d9d51-237">The value in the field can be modified.</span></span>
-   <span data-ttu-id="d9d51-238">**最終**: 同じクラスから派生したクラスのメソッドに上書きすることはできません。</span><span class="sxs-lookup"><span data-stu-id="d9d51-238">**final**: The method can't be overridden in any class that derives from its class.</span></span>
-   <span data-ttu-id="d9d51-239">**パブリック**: **パブリック**として宣言されるメソッドは、クラスがアクセスできるどの場所にもアクセスでき、サブクラスによって上書きすることができます。</span><span class="sxs-lookup"><span data-stu-id="d9d51-239">**public**: Methods that are declared as **public** can be accessed anywhere that the class is accessible, and they can be overridden by subclasses.</span></span> <span data-ttu-id="d9d51-240">アクセス修飾子を持たないメソッドは暗黙的にパブリックとなります。</span><span class="sxs-lookup"><span data-stu-id="d9d51-240">Methods that have no access modifier are implicitly public.</span></span>
-   <span data-ttu-id="d9d51-241">**保護**: **保護** として宣言されるメソッドは、クラス、およびメソッドが宣言されているクラスを拡張するサブクラスのメソッドからのみ呼び出すことができます。</span><span class="sxs-lookup"><span data-stu-id="d9d51-241">**protected**: Methods that are declared as **protected** can be called only from methods in the class and in subclasses that extend the class where the method is declared.</span></span>
-   <span data-ttu-id="d9d51-242">**プライベート**:  **プライベート**として宣言されるメソッドは、プライベートメソッドが宣言されているクラスのメソッドからのみ呼び出すことができます。</span><span class="sxs-lookup"><span data-stu-id="d9d51-242">**private**: Methods that are declared as **private** can be called only from methods in the class where the private method is declared.</span></span>
-   <span data-ttu-id="d9d51-243">**静的**: このメソッドはクラス メソッドであり、インスタンスを実行しません。</span><span class="sxs-lookup"><span data-stu-id="d9d51-243">**static**: The method is a class method and doesn't act on an instance.</span></span> <span data-ttu-id="d9d51-244">静的メソッドは、インスタンス変数を参照できません。</span><span class="sxs-lookup"><span data-stu-id="d9d51-244">Static methods can't refer to instance variables.</span></span> <span data-ttu-id="d9d51-245">クラスのインスタンスでは呼び出されません。</span><span class="sxs-lookup"><span data-stu-id="d9d51-245">They aren't invoked on an instance of the class.</span></span> <span data-ttu-id="d9d51-246">代わりに、クラス名を使用して呼び出されます (たとえば、**MyClass::aStaticProcedure()**)。</span><span class="sxs-lookup"><span data-stu-id="d9d51-246">Instead, they are invoked by using the class name (for example, **MyClass::aStaticProcedure()**).</span></span>

### <a name="methods-that-have-modifiers"></a><span data-ttu-id="d9d51-247">モディファイアーのあるメソッド</span><span class="sxs-lookup"><span data-stu-id="d9d51-247">Methods that have modifiers</span></span>

<span data-ttu-id="d9d51-248">次の例は、メソッドの見出しのみを示しています。</span><span class="sxs-lookup"><span data-stu-id="d9d51-248">The following examples show only the method headers.</span></span>

```X++
// A method that cannot be overridden
final int dontAlterMe() 

// A static method 
static void noChange()

// A display method that returns an integer
display int value()
```

## <a name="method-access-control"></a><span data-ttu-id="d9d51-249">メソッド アクセス制御</span><span class="sxs-lookup"><span data-stu-id="d9d51-249">Method access control</span></span>

<span data-ttu-id="d9d51-250">その他のクラスのメソッドがお客様のクラスのメソッドを呼び出すことができるかどうかを制御するには、アクセサー キーワード **public**、**protected**、および **private** を使用します。</span><span class="sxs-lookup"><span data-stu-id="d9d51-250">You use the accessor keywords **public**, **protected**, and **private** to control whether the methods in other classes can call the methods on your class.</span></span> <span data-ttu-id="d9d51-251">メソッドのアクセス キーワードは、クラス継承のルールとも連携します。</span><span class="sxs-lookup"><span data-stu-id="d9d51-251">The accessor keywords on methods also interact with the rules for class inheritance.</span></span> <span data-ttu-id="d9d51-252">メソッドを使用するアクセサー キーワードを次に示します。</span><span class="sxs-lookup"><span data-stu-id="d9d51-252">Here are the accessor keywords that you use with methods:</span></span>

-   <span data-ttu-id="d9d51-253">**パブリック** – **パブリック**として宣言されるメソッドは、クラスがアクセスできるどの場所からでも呼び出すことができます。</span><span class="sxs-lookup"><span data-stu-id="d9d51-253">**public**: Methods that are declared as **public** can be called from anywhere that the class is accessible.</span></span> <span data-ttu-id="d9d51-254">さらに、メソッドが**最終**として宣言されていない限り、パブリック メソッドをサブクラスでオーバーライドできます。</span><span class="sxs-lookup"><span data-stu-id="d9d51-254">In addition, a public method can be overridden by a subclass, unless the method is declared as **final**.</span></span>
-   <span data-ttu-id="d9d51-255">**保護**: **保護** として宣言されるメソッドは、次のメソッドからのみ呼び出すことができます。</span><span class="sxs-lookup"><span data-stu-id="d9d51-255">**protected**: Methods that are declared as **protected** can be called only from the following methods:</span></span>
    -   <span data-ttu-id="d9d51-256">クラスのメソッド。</span><span class="sxs-lookup"><span data-stu-id="d9d51-256">Methods in the class.</span></span>
    -   <span data-ttu-id="d9d51-257">保護されたメソッドを含むクラスのサブクラス内のメソッド。</span><span class="sxs-lookup"><span data-stu-id="d9d51-257">Methods in a subclass of the class that contains the protected method.</span></span> <span data-ttu-id="d9d51-258">保護されているメソッドは、サブクラスで上書きできます。</span><span class="sxs-lookup"><span data-stu-id="d9d51-258">Methods that are protected can be overridden in subclasses.</span></span>
-   <span data-ttu-id="d9d51-259">**プライベート**:  **プライベート**として宣言されるメソッドは、プライベートメソッドが宣言されているクラスのメソッドからのみ呼び出すことができます。</span><span class="sxs-lookup"><span data-stu-id="d9d51-259">**private**: Methods that are declared as **private** can be called only from methods in the class where the private method is declared.</span></span> <span data-ttu-id="d9d51-260">サブクラスでプライベート メソッドをオーバーライドできません。</span><span class="sxs-lookup"><span data-stu-id="d9d51-260">No private method can be overridden in a subclass.</span></span> <span data-ttu-id="d9d51-261">既定では、新しいメソッドを作成するときに、**プライベート** アクセサー キーワードがコード エディターに表示されます。</span><span class="sxs-lookup"><span data-stu-id="d9d51-261">By default, when you create a new method, the **private** accessor keyword appears in the code editor.</span></span> <span data-ttu-id="d9d51-262">最大限のセキュリティについては、**プライベート**が最も保守的な既定のアクセス キーワードです。</span><span class="sxs-lookup"><span data-stu-id="d9d51-262">For maximum security, **private** is the most conservative default accessor keyword.</span></span>

### <a name="static-and-instance-methods"></a><span data-ttu-id="d9d51-263">静的およびインスタンス メソッド</span><span class="sxs-lookup"><span data-stu-id="d9d51-263">Static and instance methods</span></span>

<span data-ttu-id="d9d51-264">メソッドのアクセサー キーワードは、どのメソッドが静的であるか、静的でないかに関係なく、同じクラスにある 2 つのメソッド間の呼び出しを制限することはありません。</span><span class="sxs-lookup"><span data-stu-id="d9d51-264">The accessor keywords on methods never restrict calls between two methods that are in the same class, regardless of which method is static or non-static.</span></span> <span data-ttu-id="d9d51-265">静的メソッドでは、**新しい**コンストラクター メソッドが**プライベート** モディファイアーで修飾されている場合でも、**新しい**コンストラクター メソッドに対する呼び出しは有効です。</span><span class="sxs-lookup"><span data-stu-id="d9d51-265">In a static method, calls to the **new** constructor method are valid even if the **new** constructor method is decorated with the **private** modifier.</span></span> <span data-ttu-id="d9d51-266">これらの呼び出しの構文では、**新しい**キーワードを使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="d9d51-266">The syntax for these calls requires that the **new** keyword be used.</span></span> <span data-ttu-id="d9d51-267">静的メソッドのコードは、クラスのインスタンス メソッドを呼び出す前に、独自のクラスのインスタンス オブジェクトを構築する必要があります。</span><span class="sxs-lookup"><span data-stu-id="d9d51-267">The code in a static method must construct an instance object of its own class before it can call any instance methods on the class.</span></span>

### <a name="increasing-access-during-overrides"></a><span data-ttu-id="d9d51-268">オーバーライド中のアクセス増加</span><span class="sxs-lookup"><span data-stu-id="d9d51-268">Increasing access during overrides</span></span>

<span data-ttu-id="d9d51-269">サブクラス内でメソッドがオーバーライドされると、オーバーライドするメソッドは少なくともオーバーライドされるメソッドと同程度のアクセスが可能なことが必要です。</span><span class="sxs-lookup"><span data-stu-id="d9d51-269">When a method is overridden in a subclass, the overriding method must be at least as accessible as the overridden method.</span></span> <span data-ttu-id="d9d51-270">たとえば、次のコンパイラ ルールは、サブクラスで保護されたメソッドが上書きされる時に適用されます。</span><span class="sxs-lookup"><span data-stu-id="d9d51-270">For example, the following compiler rules apply when a protected method is overridden in a subclass:</span></span>

-   <span data-ttu-id="d9d51-271">スーパークラスのパブリック メソッドは、サブクラスのパブリック メソッドによってのみ上書きできます。</span><span class="sxs-lookup"><span data-stu-id="d9d51-271">A public method in a superclass can be overridden only by a public method in the subclass.</span></span>
-   <span data-ttu-id="d9d51-272">サブクラスでは、パブリック メソッドまたは保護対象のメソッドはスーパークラスの保護対象のメソッドをオーバーライドできません。</span><span class="sxs-lookup"><span data-stu-id="d9d51-272">In a subclass, a public or protected method can override a protected method of the superclass.</span></span>
-   <span data-ttu-id="d9d51-273">サブクラスでは、プライベート メソッドはスーパークラスの保護対象のメソッドをオーバーライドできません。</span><span class="sxs-lookup"><span data-stu-id="d9d51-273">In a subclass, a private method can't override a protected method of the superclass.</span></span>

## <a name="optional-parameters"></a><span data-ttu-id="d9d51-274">オプションのパラメーター</span><span class="sxs-lookup"><span data-stu-id="d9d51-274">Optional parameters</span></span>
<span data-ttu-id="d9d51-275">パラメーターは、メソッド宣言で初期化することができます。</span><span class="sxs-lookup"><span data-stu-id="d9d51-275">Parameters can be initialized in the method declaration.</span></span> <span data-ttu-id="d9d51-276">この場合、パラメーターは*オプションのパラメーター*となります。</span><span class="sxs-lookup"><span data-stu-id="d9d51-276">In this case, the parameter becomes an *optional parameter*.</span></span> <span data-ttu-id="d9d51-277">メソッドの呼び出しの値が指定されていない場合は、既定値が使用されます。</span><span class="sxs-lookup"><span data-stu-id="d9d51-277">If no value is supplied in the method call, the default value is used.</span></span> <span data-ttu-id="d9d51-278">すべての必須パラメータは最初のオプション パラメーターの前に一覧表示する必要があります。</span><span class="sxs-lookup"><span data-stu-id="d9d51-278">All required parameters must be listed before the first optional parameter.</span></span> <span data-ttu-id="d9d51-279">次の例では、オプションのパラメーターを持つメソッドを作成して呼び出す方法を示しています。</span><span class="sxs-lookup"><span data-stu-id="d9d51-279">The following examples show how to create and call a method that has optional parameters.</span></span> <span data-ttu-id="d9d51-280">**AddThreeInts** メソッドの例は、メソッドを呼び出すときにデフォルトのパラメーターをスキップできないことを示しています。</span><span class="sxs-lookup"><span data-stu-id="d9d51-280">The example of the **AddThreeInts** method shows that you can't skip default parameters when you call a method.</span></span>

### <a name="examples-of-optional-parameters"></a><span data-ttu-id="d9d51-281">オプション パラメーターの例</span><span class="sxs-lookup"><span data-stu-id="d9d51-281">Examples of optional parameters</span></span>

<span data-ttu-id="d9d51-282">既定のパラメータを持つクラスのコード例を次に示します。</span><span class="sxs-lookup"><span data-stu-id="d9d51-282">The following code example shows a class with a default parameter.</span></span>
```X++
// This is an example of a function being used as the default.
public class Person 
{
    date birthDate;

    // The constructor that takes a date type as
    // a parameter. That value is assigned to the field member birthDate. 
    void new(date _date)
    {
        birthDate = _date;
    }

    // The CalculateAgeAsOfDate method references the birthDate field and has an
    // optional parameter. In this example, the default value is the
    // return value of a function.
    public real CalculateAgeAsOfDate(date _calcToDate = DateTimeUtil::getToday(DateTimeUtil::getUserPreferredTimeZone()) )  
    {
        return (_calcToDate - birthDate) / 365;
    }


// This code instantiates a Person and calls CalculateAgeAsOfDate.
Person person = new Person(13\5\2010);   // birthDate is initialized.
// Optional parameter's default is used.
info("Age in years: " + num2str(person.CalculateAgeAsOfDate(),2,0,0,0));
// Output is "9" in July 2019.

// January 2, 2044  is the parameter value for _date.
info("Age in years: " + num2str(person.CalculateAgeAsOfDate(2\1\2044),2,0,0,0));
// Output is "34".
}
```

<span data-ttu-id="d9d51-283">次の例では、2 番目の省略可能なパラメーターにスキップできないことを示します。</span><span class="sxs-lookup"><span data-stu-id="d9d51-283">This is an example of how you cannot skip to a second optional parameter.</span></span> <span data-ttu-id="d9d51-284">最初の方法には 2 つの省略可能なパラメーターがあります。</span><span class="sxs-lookup"><span data-stu-id="d9d51-284">The first method has two optional parameters.</span></span> <span data-ttu-id="d9d51-285">2 つ目の方法は、最初のメソッドの呼び出し元です。</span><span class="sxs-lookup"><span data-stu-id="d9d51-285">The second method is a caller of the first method.</span></span> <span data-ttu-id="d9d51-286">呼び出し元は\_i3 の既定値のみをオーバーライドすることを希望していますが、コンパイラでは、すべての前のオプション パラメーターが呼び出しでオーバーライドされている必要があります。</span><span class="sxs-lookup"><span data-stu-id="d9d51-286">The caller wants to override only the \_i3 default value, but the compiler requires that all prior optional parameters also be overridden in the call.</span></span> 

```X++
public class Additions 
{
    static public int AddThreeInts(int _i1, int _i2 = 2,int _i3 = 3)
    {
        return _i1 + _i2 + _i3;
    }
}

// This code calls the AddThreeInts method.
// No way to skip the first optional parameter (so it can default)
// while also specifying the value of the second optional parameter.
// The next statement does not compile.
// info(int2Str(Additions::AddThreeInts(1, 2, 99)));

// Settle for overriding both optional parameters.
info(int2Str(Additions::AddThreeInts(1, 2, 99)));
// Output is "102".
```

## <a name="accessor-methods"></a><span data-ttu-id="d9d51-287">アクセサー メソッド</span><span class="sxs-lookup"><span data-stu-id="d9d51-287">Accessor methods</span></span>

<span data-ttu-id="d9d51-288">クラス変数は既定で保護されます。</span><span class="sxs-lookup"><span data-stu-id="d9d51-288">Class variables are protected by default.</span></span> <span data-ttu-id="d9d51-289">クラスの内部実装の詳細を非表示にすることで、そのクラスを使用するコードを破棄することなくクラスの実装を後で変更することができます。</span><span class="sxs-lookup"><span data-stu-id="d9d51-289">By hiding details of the internal implementation of a class, you can change the implementation of the class later without breaking any code that uses that class.</span></span> <span data-ttu-id="d9d51-290">参照変数からデータにアクセスするには、アクセサー メソッドを作成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="d9d51-290">To access the data from reference variables, you must create accessor methods.</span></span> <span data-ttu-id="d9d51-291">次の例では、アクセス メソッドを使用して変数 **x** および **y** にアクセスする **Point** クラスを定義します。</span><span class="sxs-lookup"><span data-stu-id="d9d51-291">The following example defines a **Point** class that uses accessor methods to access the variables **x** and **y**.</span></span>

```X++
class Point
{
    // Instance variables
    real x; 
    real y;

    // Constructor to initialize to a specific or default value
    void new(real _x = 10, real _y = 10) 
    {
        x = _x;
        y = _y;
    }

    // Accessor methods
    void setX(real _x) 
    {
        x = _x;
    }

    void setY(real _y) 
    {
        y = _y;
    }

    real getX() 
    {
        return x;
    }

    real getY() 
    {
        return y;
    }
}
```

<span data-ttu-id="d9d51-292">これらのメソッド宣言は、**Point** クラスが外部からの変数へのアクセスを提供する方法を示しています。</span><span class="sxs-lookup"><span data-stu-id="d9d51-292">These method declarations show how the **Point** class provides access to its variables from the outside world.</span></span> <span data-ttu-id="d9d51-293">その他のオブジェクトは、アクセサー メソッドを使ってインスタンス変数 **Point** オブジェクトを操作できます。</span><span class="sxs-lookup"><span data-stu-id="d9d51-293">Other objects can manipulate the instance variables of **Point** objects by using the accessor methods.</span></span>

```X++
Point myPoint = new Point();
// Set the x variable using the accessor method.
myPoint.setX(4.0);
// Get the x variable using the accessor method.
info(any2Str(myPoint.getX()));
```

## <a name="parameters"></a><span data-ttu-id="d9d51-294">パラメーター</span><span class="sxs-lookup"><span data-stu-id="d9d51-294">Parameters</span></span>

<span data-ttu-id="d9d51-295">すべてのメソッドは独自の*スコープ*を持っています。</span><span class="sxs-lookup"><span data-stu-id="d9d51-295">All methods have their own *scope*.</span></span> <span data-ttu-id="d9d51-296">メソッドは、1 つ以上のパラメーターを受け取ることができます。</span><span class="sxs-lookup"><span data-stu-id="d9d51-296">A method can take one or more parameters.</span></span> <span data-ttu-id="d9d51-297">メソッドのスコープ内では、これらのパラメーターはローカル変数として処理され、メソッド呼び出しのパラメーターからの値で初期化されます。</span><span class="sxs-lookup"><span data-stu-id="d9d51-297">Within the scope of the method, these parameters are treated as local variables and are initialized with a value from the parameter in the method call.</span></span> <span data-ttu-id="d9d51-298">すべてのパラメーターは値で渡されるため、元の変数の値を変更することはできません。</span><span class="sxs-lookup"><span data-stu-id="d9d51-298">All parameters are passed by value, which means that you can't change the value of the original variable.</span></span> <span data-ttu-id="d9d51-299">メソッド内のローカル変数のみを変更することができます。</span><span class="sxs-lookup"><span data-stu-id="d9d51-299">You can change only the local variable in the method.</span></span> <span data-ttu-id="d9d51-300">このローカル変数は元の変数のコピーです。</span><span class="sxs-lookup"><span data-stu-id="d9d51-300">This local variable is a copy of the original variable.</span></span>

## <a name="scope-of-variables-in-methods"></a><span data-ttu-id="d9d51-301">メソッドでの変数の範囲</span><span class="sxs-lookup"><span data-stu-id="d9d51-301">Scope of variables in methods</span></span>

<span data-ttu-id="d9d51-302">スコープは、品目にアクセスできるエリアを定義します。</span><span class="sxs-lookup"><span data-stu-id="d9d51-302">A scope defines the area in which an item can be accessed.</span></span> <span data-ttu-id="d9d51-303">クラスで定義されている変数は、そのクラス内のメソッドで使用できます。</span><span class="sxs-lookup"><span data-stu-id="d9d51-303">Variables that are defined in a class are available to the methods within that class.</span></span> <span data-ttu-id="d9d51-304">メソッド内の変数は、現在のブロック内でのみアクセスできます。</span><span class="sxs-lookup"><span data-stu-id="d9d51-304">Variables in methods can be accessed only within the current block.</span></span>

## <a name="local-functions"></a><span data-ttu-id="d9d51-305">ローカル関数</span><span class="sxs-lookup"><span data-stu-id="d9d51-305">Local functions</span></span>

<span data-ttu-id="d9d51-306">メソッド内部のローカル関数を宣言することができます。</span><span class="sxs-lookup"><span data-stu-id="d9d51-306">You can declare functions inside a method.</span></span> <span data-ttu-id="d9d51-307">これは、ローカル関数と呼ばれます。</span><span class="sxs-lookup"><span data-stu-id="d9d51-307">These are called local functions.</span></span> <span data-ttu-id="d9d51-308">可能ではあるものの、ベスト プラクティスではありません。</span><span class="sxs-lookup"><span data-stu-id="d9d51-308">While possible, it is not a best practice.</span></span> <span data-ttu-id="d9d51-309">代わりに、プライベート メソッドをクラスに追加する必要があります。</span><span class="sxs-lookup"><span data-stu-id="d9d51-309">Instead, you should add private methods to the class.</span></span> 

-   <span data-ttu-id="d9d51-310">ローカル関数の宣言は、メソッド内の宣言されていないステートメントの前に物理的に先行する必要があります。</span><span class="sxs-lookup"><span data-stu-id="d9d51-310">The declarations of local functions must physically precede any non-declaration statements in the method.</span></span>
-   <span data-ttu-id="d9d51-311">メソッド内で 1 つ以上のローカル関数を宣言することができます。</span><span class="sxs-lookup"><span data-stu-id="d9d51-311">You can declare more than one local function in your method.</span></span> <span data-ttu-id="d9d51-312">ただし、すべてのローカル関数は中断のないシリーズで宣言され、セットは 1 つのセミコロン (;) で終了する必要があります。</span><span class="sxs-lookup"><span data-stu-id="d9d51-312">However, all local functions must be declared in an uninterrupted series, and the set must be terminated by one semicolon (;).</span></span>
-   <span data-ttu-id="d9d51-313">ローカル関数内にあるコードは、ローカル関数を含むメソッドで宣言されている変数にアクセスできます。</span><span class="sxs-lookup"><span data-stu-id="d9d51-313">Code that is inside the local function can access variables that are declared in the method that contains the local function.</span></span>
-   <span data-ttu-id="d9d51-314">ローカル関数の外にあるコードは、ローカル関数で宣言された変数にアクセスすることはできません。</span><span class="sxs-lookup"><span data-stu-id="d9d51-314">Code that is outside the local function can't access variables that are declared in the local function.</span></span>
-   <span data-ttu-id="d9d51-315">ローカル関数は、ローカル関数が宣言されているのと同じメソッド内のコードによってのみ呼び出すことができます。</span><span class="sxs-lookup"><span data-stu-id="d9d51-315">A local function can be called only by code in the same method where the local function is declared.</span></span>
-   <span data-ttu-id="d9d51-316">ローカル関数が、それ自体を呼び出すことはありません。</span><span class="sxs-lookup"><span data-stu-id="d9d51-316">A local function should never call itself.</span></span> <span data-ttu-id="d9d51-317">このような再帰は、正常に行われるコンパイルを防ぐことができます。</span><span class="sxs-lookup"><span data-stu-id="d9d51-317">Such recursion can prevent successful compilation.</span></span>

<span data-ttu-id="d9d51-318">次の例は、2 つのローカル関数である **localFunctionA** および **localFunctionB** の有効な宣言を示しています。</span><span class="sxs-lookup"><span data-stu-id="d9d51-318">The following example shows valid declarations of two local functions, **localFunctionA** and **localFunctionB**.</span></span> <span data-ttu-id="d9d51-319">ローカル関数への呼び出しは、必要に応じて、この例の関数宣言の後に行われます。</span><span class="sxs-lookup"><span data-stu-id="d9d51-319">Calls to the local functions occur after the function declarations in the example, as is required.</span></span>

```X++
static void StaticFunction()
{
    int number = 654;

    void localFunctionA(int _iNum)  // The local function.
    {
        str innerString = "String in localFunctionA";
        str output = strFmt("localFunctionA: %1 , %2 , %3", _iNum, innerString, number);
        info(output);
    }

    void localFunctionB()
    {
        info("Printing from inside localFunctionB.");
    }

    localFunctionA(55);
    localFunctionB();
    // Next info statement would fail to compile,
    // because innerString is restricted to the
    // scope of the local function in which it is declared.
    // print innerString;
}

// When called, the output is:
// localFunctionA: 55 , String in localFunctionA , 654
// Printing from inside localFunctionB.
```

## <a name="the-this-keyword"></a><span data-ttu-id="d9d51-320">このキーワード</span><span class="sxs-lookup"><span data-stu-id="d9d51-320">The this keyword</span></span>
<span data-ttu-id="d9d51-321">**this** キーワードは、**this** キーワードが使用されるクラスやテーブルのインスタンスへの参照です。</span><span class="sxs-lookup"><span data-stu-id="d9d51-321">The **this** keyword is a reference to the instance of the class or table where the **this** keyword is used.</span></span> <span data-ttu-id="d9d51-322">**this** 参照が必須になることはありませんが、コードを明確にし、コード エディターで IntelliSense の動作を強化することができます。</span><span class="sxs-lookup"><span data-stu-id="d9d51-322">The **this** reference is never required, but it can clarify your code and enhances the behavior of IntelliSense in the code editor.</span></span> <span data-ttu-id="d9d51-323">すべての呼び出しインスタンス メソッドは**これ**を参照または変数のいずれかにより修飾される必要があります。</span><span class="sxs-lookup"><span data-stu-id="d9d51-323">All calls to instance methods must be qualified by either the **this** reference or a variable.</span></span> <span data-ttu-id="d9d51-324">**this** 参照は、次の情報を修飾するために使用できます。</span><span class="sxs-lookup"><span data-stu-id="d9d51-324">The **this** reference can be used to qualify the following information:</span></span>

-   <span data-ttu-id="d9d51-325">**this** 参照が使用されている同じクラス内の他のインスタンス (静的でない) メソッドの名前。</span><span class="sxs-lookup"><span data-stu-id="d9d51-325">The names of other instance (non-static) methods in the same class where the **this** reference is used.</span></span> <span data-ttu-id="d9d51-326">次の例を示します: `boolColorChanged = this.colorItOrange();`</span><span class="sxs-lookup"><span data-stu-id="d9d51-326">Here is an example: `boolColorChanged = this.colorItOrange();`</span></span>
-   <span data-ttu-id="d9d51-327">**this** オブジェクトによって継承されるメソッドの名前。</span><span class="sxs-lookup"><span data-stu-id="d9d51-327">The names of methods that are inherited by the **this** object.</span></span>
-   <span data-ttu-id="d9d51-328">**this** キーワードが使用されるメソッドを含むテーブル上のフィールドの名前。</span><span class="sxs-lookup"><span data-stu-id="d9d51-328">The names of fields on the table that contains the method that the **this** keyword is used in.</span></span>

<span data-ttu-id="d9d51-329">**this** 参照は、次の方法で使用できません。</span><span class="sxs-lookup"><span data-stu-id="d9d51-329">The **this** reference can't be used in the following ways:</span></span>

-   <span data-ttu-id="d9d51-330">**classDeclaration** コードで宣言されているメンバー変数の名前を限定することはできません。</span><span class="sxs-lookup"><span data-stu-id="d9d51-330">It can't qualify the names of member variables that are declared in the **classDeclaration** code.</span></span>
-   <span data-ttu-id="d9d51-331">静的メソッドで使用できません。</span><span class="sxs-lookup"><span data-stu-id="d9d51-331">It can't be used in a static method.</span></span>
-   <span data-ttu-id="d9d51-332">クラスやテーブルの静的メソッドの名前を限定することはできません。</span><span class="sxs-lookup"><span data-stu-id="d9d51-332">It can't qualify the names of static methods of the class or table.</span></span>

## <a name="call-stack-limitation"></a><span data-ttu-id="d9d51-333">呼び出しスタック制限</span><span class="sxs-lookup"><span data-stu-id="d9d51-333">Call stack limitation</span></span>

<span data-ttu-id="d9d51-334">コール スタックの深さは 100 に制限されています。</span><span class="sxs-lookup"><span data-stu-id="d9d51-334">The depth of the call stack is limited to 100.</span></span>
