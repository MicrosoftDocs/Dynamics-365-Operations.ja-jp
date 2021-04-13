---
title: クラスおよびメソッド
description: このトピックでは、X++ でクラスを作成および使用する方法について説明します。
author: RobinARH
ms.date: 06/17/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Developer
ms.reviewer: rhaertle
ms.custom: 150303
ms.assetid: ''
ms.search.region: Global
ms.author: rhaertle
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: c5a62115cd4ed277890d4839db9c9d7c84abd79f
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/31/2021
ms.locfileid: "5753038"
---
# <a name="classes-and-methods"></a><span data-ttu-id="709a7-103">クラスおよびメソッド</span><span class="sxs-lookup"><span data-stu-id="709a7-103">Classes and methods</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="709a7-104">このトピックでは、X++ でクラスを作成および使用する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="709a7-104">This topic describes how to create and use classes in X++.</span></span>

<span data-ttu-id="709a7-105">*クラス* は、そのクラスから後に構築されるインスタンスのデータおよびメソッドを定義するソフトウェア構造です。</span><span class="sxs-lookup"><span data-stu-id="709a7-105">A *class* is a software construct that defines the data and methods of the instances that are later constructed from that class.</span></span> <span data-ttu-id="709a7-106">*クラス* は、問題のあるドメイン内の *オブジェクト* を抽象化したものです。</span><span class="sxs-lookup"><span data-stu-id="709a7-106">The *class* is an abstraction of an *object* in the problem domain.</span></span> <span data-ttu-id="709a7-107">この *クラス* から構築されるインスタンスは、*インスタンス* または *オブジェクト* として知られます。</span><span class="sxs-lookup"><span data-stu-id="709a7-107">The instances that are constructed from the *class* are known as *instances* or *objects*.</span></span> <span data-ttu-id="709a7-108">このトピックでは、*インスタンス* という用語を使用します。</span><span class="sxs-lookup"><span data-stu-id="709a7-108">This topic uses the term *instance*.</span></span> <span data-ttu-id="709a7-109">データはオブジェクトの状態を表し、メソッドはオブジェクトの動作を表します。</span><span class="sxs-lookup"><span data-stu-id="709a7-109">The data represents the state of the object, whereas the methods represent the behavior of the object.</span></span> 

<span data-ttu-id="709a7-110">*変数* にはクラスのデータが含まれます。</span><span class="sxs-lookup"><span data-stu-id="709a7-110">*Variables* contain the data for the class.</span></span> <span data-ttu-id="709a7-111">クラス宣言から構築されたすべてのインスタンスには、独自の変数のコピーがあります。</span><span class="sxs-lookup"><span data-stu-id="709a7-111">Every instance that is constructed from the class declaration has its own copy of the variables.</span></span> <span data-ttu-id="709a7-112">これらの変数は *インスタンス変数* と呼ばれます。</span><span class="sxs-lookup"><span data-stu-id="709a7-112">These variables are known as *instance variables*.</span></span> 

<span data-ttu-id="709a7-113">メソッドはクラスの動作を定義します。</span><span class="sxs-lookup"><span data-stu-id="709a7-113">Methods define the behavior of a class.</span></span> <span data-ttu-id="709a7-114">データに作用する一連の明細書です (インスタンス変数)。</span><span class="sxs-lookup"><span data-stu-id="709a7-114">They are the sequences of statements that operate on the data (instance variables).</span></span> <span data-ttu-id="709a7-115">規定では、メソッドはクラスのインスタンス変数に作用するように宣言されます。</span><span class="sxs-lookup"><span data-stu-id="709a7-115">By default, methods are declared to operate on the instance variables of the class.</span></span> <span data-ttu-id="709a7-116">これらのメソッドは、*instance メソッド* または *object メソッド* と呼ばれます。</span><span class="sxs-lookup"><span data-stu-id="709a7-116">These methods are known as *instance methods* or *object methods*.</span></span> 

<span data-ttu-id="709a7-117">*インスタンス変数* にアクセスできない *静的メソッド* および *静的フィールド* を宣言できます。</span><span class="sxs-lookup"><span data-stu-id="709a7-117">You can declare *static methods* and *static fields*, that do not have access to *instance variables*.</span></span> <span data-ttu-id="709a7-118">これらはすべて[X++ 静的クラス](xpp-static-classes.md)に記述されています。</span><span class="sxs-lookup"><span data-stu-id="709a7-118">These are described in [X++ static classes](xpp-static-classes.md).</span></span>

## <a name="declare-a-class"></a><span data-ttu-id="709a7-119">クラスを宣言します</span><span class="sxs-lookup"><span data-stu-id="709a7-119">Declare a class</span></span>

<span data-ttu-id="709a7-120">プロジェクトにクラスを追加するには、Visual Studio で **新しい項目の追加** ダイアログを使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="709a7-120">You must use the **Add new item** dialog in Visual Studio to add a class to your project.</span></span> 

1.  <span data-ttu-id="709a7-121">サーバー エクスプローラーで、プロジェクトを右クリックしてから **追加** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="709a7-121">In Server Explorer, right-click the project, and then click **Add**.</span></span>
2.  <span data-ttu-id="709a7-122">**新しい項目** のダイアログ ボックスの左側のナビゲーションで、**インストール済み > Dynamics 365 品目 > Code** の順に選択します。</span><span class="sxs-lookup"><span data-stu-id="709a7-122">In the **New Item** dialog box, select **Installed > Dynamics 365 Items > Code** in the left navigation.</span></span> <span data-ttu-id="709a7-123">その後、**クラス** を選択し、クラス名を入力します。</span><span class="sxs-lookup"><span data-stu-id="709a7-123">Then select **Class**, and then enter a name for the class.</span></span>
3.  <span data-ttu-id="709a7-124">**追加** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="709a7-124">Click **Add**.</span></span>

<span data-ttu-id="709a7-125">すべてのクラスはパブリックです。</span><span class="sxs-lookup"><span data-stu-id="709a7-125">All classes are public.</span></span> <span data-ttu-id="709a7-126">**パブリック** モディファイアーを削除すると、システムではクラスはパブリック クラスとして扱われます。</span><span class="sxs-lookup"><span data-stu-id="709a7-126">If you remove the **public** modifier, the system still treats the class as public.</span></span> <span data-ttu-id="709a7-127">クラス宣言では、**final** および **extends** などの、他の修飾子を指定することができます。</span><span class="sxs-lookup"><span data-stu-id="709a7-127">You can specify other modifiers on the class declaration, such as **final** and **extends**.</span></span>

## <a name="variables"></a><span data-ttu-id="709a7-128">変数</span><span class="sxs-lookup"><span data-stu-id="709a7-128">Variables</span></span>

<span data-ttu-id="709a7-129">インスタンス変数は既定で **保護** されます。</span><span class="sxs-lookup"><span data-stu-id="709a7-129">Instance variables are **protected** by default.</span></span> <span data-ttu-id="709a7-130">これは、同じクラスまたは [派生クラス](xpp-inheritance.md) の中でしかアクセスできないことを意味します。</span><span class="sxs-lookup"><span data-stu-id="709a7-130">This means that they can only be accessed in the same class or [a derived class](xpp-inheritance.md).</span></span> <span data-ttu-id="709a7-131">**private**、**protected** 、または **public** キーワードを使用して、インスタンス変数宣言を変更できます。</span><span class="sxs-lookup"><span data-stu-id="709a7-131">You can modify an instance variable declaration by using the **private**, **protected**, or **public** keywords.</span></span> 

<span data-ttu-id="709a7-132">次の例は、アクセサー メソッドを使用して変数データを公開する方法を示しています。</span><span class="sxs-lookup"><span data-stu-id="709a7-132">The following example shows how to use accessor methods to make the variable data public.</span></span> <span data-ttu-id="709a7-133">変数 **名** は保護されるため、プロテクト変数へのアクセスを許可するために、アクセサー (取得と設定) メソッドが実装されます。</span><span class="sxs-lookup"><span data-stu-id="709a7-133">The variable **firstName** is protected, so accessor (get and set) methods are implemented to allow access to the protected variable.</span></span> <span data-ttu-id="709a7-134">変数 **姓** は公開されているため、コードで変数の値を直接取得して設定することができます。</span><span class="sxs-lookup"><span data-stu-id="709a7-134">The variable **lastName** is public, so code can directly get and set the value of the variable.</span></span>

```xpp
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

## <a name="constructors"></a><span data-ttu-id="709a7-135">コンストラクター</span><span class="sxs-lookup"><span data-stu-id="709a7-135">Constructors</span></span>

<span data-ttu-id="709a7-136">クラスのインスタンスを作成するには、*コンストラクタ* を使用してクラスのインスタンスを生成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="709a7-136">To create an instance of a class, you must instantiate it by using a *constructor*.</span></span> 

+ <span data-ttu-id="709a7-137">クラスでは、**新しい** メソッド (コンストラクター) を 1 つだけ定義できます。</span><span class="sxs-lookup"><span data-stu-id="709a7-137">You can define only one **new** method (constructor) in a class.</span></span> 
+ <span data-ttu-id="709a7-138">コンストラクターを定義しない場合は、パラメーターのない既定のコンストラクターが、コンパイラによって自動的に作成されます。</span><span class="sxs-lookup"><span data-stu-id="709a7-138">If you do not define a constructor, a default constructor with no parameters is created automatically by the compiler.</span></span> 
+ <span data-ttu-id="709a7-139">既定のコンストラクターは、**新しい** メソッドでパラメーターに既定値を割り当てることによってシミュレーションできます。</span><span class="sxs-lookup"><span data-stu-id="709a7-139">You can simulate a default constructor by assigning default values to the parameters in the **new** method.</span></span>

<span data-ttu-id="709a7-140">次の例では、**ポイント** クラスのパラメーターなしのコンストラクターを定義しています。</span><span class="sxs-lookup"><span data-stu-id="709a7-140">The following examples defines a parameterless constructor in the **Point** class.</span></span>

```xpp
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

<span data-ttu-id="709a7-141">次に、クリーンな継承モデルを作成し、コードがアップグレードされたときの問題を最小限に抑える方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="709a7-141">Following is information about how to create a clean inheritance model and minimize problems when code is upgraded:</span></span>

  - <span data-ttu-id="709a7-142">抽象クラスでない場合、各クラスは単一のパブリック構築メソッドを持つ必要があります。</span><span class="sxs-lookup"><span data-stu-id="709a7-142">Each class must have a single public construction method unless the class is abstract.</span></span> <span data-ttu-id="709a7-143">初期化が不要な場合は、静的コンストラクトのメソッドを使用します。</span><span class="sxs-lookup"><span data-stu-id="709a7-143">If no initialization is required, use a static construct method.</span></span> <span data-ttu-id="709a7-144">それ以外の場合は、静的な **新しい** メソッドを使用します (クラスの既定のコンストラクターは保護する必要があります)。</span><span class="sxs-lookup"><span data-stu-id="709a7-144">Otherwise, use a static **new** method (the default constructor for the class should be protected).</span></span>
  - <span data-ttu-id="709a7-145">各クラスは少なくとも 1 つの静的 **コンストラクト** メソッドを持つ必要があります。</span><span class="sxs-lookup"><span data-stu-id="709a7-145">Each class should have at least one static **construct** method method.</span></span>
  - <span data-ttu-id="709a7-146">各クラスは少なくとも 1 つの **新しい** 静的メソッドを持つ必要があります。</span><span class="sxs-lookup"><span data-stu-id="709a7-146">Each class should have at least one static **new** method.</span></span>
  - <span data-ttu-id="709a7-147">各クラスに **新しい** メソッド (既定のコンストラクター) が必要です。</span><span class="sxs-lookup"><span data-stu-id="709a7-147">Each class should have a **new** method (the default constructor).</span></span> <span data-ttu-id="709a7-148">このメソッドは **保護** する必要があります。</span><span class="sxs-lookup"><span data-stu-id="709a7-148">This method should be **protected**.</span></span>
  - <span data-ttu-id="709a7-149">クラス変数を取得および設定するためのアクセサー メソッドを作成します。</span><span class="sxs-lookup"><span data-stu-id="709a7-149">Create accessor methods to get and set class variables.</span></span>
  - <span data-ttu-id="709a7-150">インスタンス化の後に実行する必要のある特殊な初期化タスクを実行するための **init** メソッドを作成します。</span><span class="sxs-lookup"><span data-stu-id="709a7-150">Create **init** methods to carry out any specialized initialization tasks that should be carried out after instantiation.</span></span>

### <a name="create-other-objects-in-a-constructor"></a><span data-ttu-id="709a7-151">コンストラクターでその他のオブジェクトを作成する</span><span class="sxs-lookup"><span data-stu-id="709a7-151">Create other objects in a constructor</span></span>

<span data-ttu-id="709a7-152">クラス コンストラクターは、クラスのインスタンスを作成するだけでなく、他のオブジェクトをインスタンス化することもできます。</span><span class="sxs-lookup"><span data-stu-id="709a7-152">A class constructor can instantiate other objects in addition to creating an instance of the class.</span></span> <span data-ttu-id="709a7-153">たとえば、次のコードは、境界を定義するため 2 つの **ポイント** オブジェクトを使用する **長方形** クラスを申告します。</span><span class="sxs-lookup"><span data-stu-id="709a7-153">For example, the following code declares a **Rectangle** class that uses two **Point** objects to define its bounds.</span></span> <span data-ttu-id="709a7-154">この場合、**ポイント** クラスには 2 つの **実数** パラメーターを持つコンストラクターが存在します。</span><span class="sxs-lookup"><span data-stu-id="709a7-154">In this case, the **Point** class has a constructor that has two **real** parameters.</span></span>

```xpp

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

## <a name="create-an-instance-of-an-object"></a><span data-ttu-id="709a7-155">オブジェクトのインスタンスを作成する</span><span class="sxs-lookup"><span data-stu-id="709a7-155">Create an instance of an object</span></span>

<span data-ttu-id="709a7-156">コンストラクター、**新規** は、クラスの新しいインスタンスを返します。</span><span class="sxs-lookup"><span data-stu-id="709a7-156">The constructor, **new**, returns a new instance of the class.</span></span> <span data-ttu-id="709a7-157">次のコード例は、ポイント クラスのインスタンスを 2 つ作成する方法を示しています。</span><span class="sxs-lookup"><span data-stu-id="709a7-157">The following code example creates two instances of the Point class.</span></span>

```xpp
// Declare a variable to refer to a Point instance.
Point myPoint;

// Create an instance of the Point class.
myPoint = new Point();

// Declare and instantiate a Point instance.
Point ap = new Point();
```

## <a name="destructors"></a><span data-ttu-id="709a7-158">デストラクター</span><span class="sxs-lookup"><span data-stu-id="709a7-158">Destructors</span></span>
<span data-ttu-id="709a7-159">*デストラクター* は、クラス インスタンスを明示的に破棄するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="709a7-159">You use a *destructor* to explicitly destroy a class instance.</span></span> <span data-ttu-id="709a7-160">インスタンスは、インスタンスに関する参照がない場合は自動的に破棄されます。</span><span class="sxs-lookup"><span data-stu-id="709a7-160">Instances are automatically destroyed when there are no references to them.</span></span> <span data-ttu-id="709a7-161">ただし、たとえば、次の方法で対象を明示的に破棄できます。</span><span class="sxs-lookup"><span data-stu-id="709a7-161">However, you can destroy objects explicitly in the following ways:</span></span>

-   <span data-ttu-id="709a7-162">**finalize** メソッドを使用します。</span><span class="sxs-lookup"><span data-stu-id="709a7-162">Use the **finalize** method.</span></span>
-   <span data-ttu-id="709a7-163">参照変数を **Null** に設定します。</span><span class="sxs-lookup"><span data-stu-id="709a7-163">Set the reference variable to **null**.</span></span>

### <a name="use-the-finalize-method"></a><span data-ttu-id="709a7-164">ファイナライズ メソッドを使用する</span><span class="sxs-lookup"><span data-stu-id="709a7-164">Use the finalize method</span></span>

<span data-ttu-id="709a7-165">オブジェクトを明示的に破棄するには **finalize** メソッドを使用します。</span><span class="sxs-lookup"><span data-stu-id="709a7-165">Use the **finalize** method to explicitly destroy an object.</span></span> <span data-ttu-id="709a7-166">**finalize** メソッドへの暗黙的な呼び出しはありません。</span><span class="sxs-lookup"><span data-stu-id="709a7-166">There are no implicit calls to the **finalize** method.</span></span> <span data-ttu-id="709a7-167">そこでステートメントを実行するメソッドを呼び出す必要があります。</span><span class="sxs-lookup"><span data-stu-id="709a7-167">You must call the method to run the statements in it.</span></span> <span data-ttu-id="709a7-168">**finalize** メソッドでは、必要なクリーンアップ コードも配置する必要があります。</span><span class="sxs-lookup"><span data-stu-id="709a7-168">In the **finalize** method, you should also put any clean-up code that is required.</span></span> <span data-ttu-id="709a7-169">たとえば、クラスがダイナミックリンク ライブラリ (DLL) モジュールを使用する場合、必要ではなくなったときに DLL をリリースする **確定** メソッドを使用できます。</span><span class="sxs-lookup"><span data-stu-id="709a7-169">For example, if your class uses a dynamic-link library (DLL) module, you can use the **finalize** method to release the DLL when you no longer require it.</span></span> <span data-ttu-id="709a7-170">**finalize** メソッドは慎重に使用してください。</span><span class="sxs-lookup"><span data-stu-id="709a7-170">Use the **finalize** method carefully.</span></span> <span data-ttu-id="709a7-171">オブジェクトへの参照がある場合オブジェクトを破棄します。</span><span class="sxs-lookup"><span data-stu-id="709a7-171">It will destroy an object even if there are references to it.</span></span>

<span data-ttu-id="709a7-172">次の例は、**finalize** メソッドの呼び出しの基本構造を示しています。</span><span class="sxs-lookup"><span data-stu-id="709a7-172">The following example shows the basic structure for a call to the **finalize** method.</span></span>

```xpp
// From any method in a class.
if (condition)
{
    // Removes object from memory.
    this.finalize(); 
}
```

### <a name="set-reference-variable-to-null"></a><span data-ttu-id="709a7-173">参照変数を Null に設定する</span><span class="sxs-lookup"><span data-stu-id="709a7-173">Set reference variable to null</span></span>

<span data-ttu-id="709a7-174">参照変数を **Null** に設定してオブジェクトを終了します。</span><span class="sxs-lookup"><span data-stu-id="709a7-174">Set the reference variable to **null** to terminate an object.</span></span> <span data-ttu-id="709a7-175">この方法を使用すると、他の変数がそのオブジェクトをポイントしていない場合にのみオブジェクトが破棄されます。</span><span class="sxs-lookup"><span data-stu-id="709a7-175">This approach destroys an object only if no other variables point to that object.</span></span> <span data-ttu-id="709a7-176">他のコードが変数を使用していないことを確認する必要があります。</span><span class="sxs-lookup"><span data-stu-id="709a7-176">You should verify that other code isn't using the variable.</span></span> <span data-ttu-id="709a7-177">次の例では、参照変数を作成して、**Null** に設定する方法を示します。</span><span class="sxs-lookup"><span data-stu-id="709a7-177">The following example creates an reference variable and then sets it to **null**.</span></span>

```xpp
Point myPoint = new Point();
myPoint = null;
```

## <a name="methods"></a><span data-ttu-id="709a7-178">メソッド</span><span class="sxs-lookup"><span data-stu-id="709a7-178">Methods</span></span>

### <a name="instance-methods"></a><span data-ttu-id="709a7-179">インスタンス メソッド</span><span class="sxs-lookup"><span data-stu-id="709a7-179">Instance methods</span></span>

<span data-ttu-id="709a7-180">インスタンス メソッドは、クラスから作成される各インスタンスに埋め込まれます。</span><span class="sxs-lookup"><span data-stu-id="709a7-180">Instance methods are embedded in each instance that is created from the class.</span></span> <span data-ttu-id="709a7-181">メソッドの使用前に、オブジェクトのインスタンスを作成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="709a7-181">You must instantiate the object before you can use the method.</span></span> <span data-ttu-id="709a7-182">次のコードは、インスタンス メソッドを定義して、それをインスタンスから呼び出す方法を示しています。</span><span class="sxs-lookup"><span data-stu-id="709a7-182">The following code shows how to define an instance method and call it from an instance.</span></span>

```xpp
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

### <a name="static-methods"></a><span data-ttu-id="709a7-183">静的メソッド</span><span class="sxs-lookup"><span data-stu-id="709a7-183">Static methods</span></span>

<span data-ttu-id="709a7-184">*クラス メソッド* とも呼ばれる静的メソッドは、クラスに属しており、キーワード **static** を使用して作成されます。</span><span class="sxs-lookup"><span data-stu-id="709a7-184">Static methods, which are also known as *class methods*, belong to a class and are created by using the keyword **static**.</span></span> <span data-ttu-id="709a7-185">静的メソッドを使用する前に、オブジェクトのインスタンスを作成する必要はありません。</span><span class="sxs-lookup"><span data-stu-id="709a7-185">You don't have to instantiate an object before you use static methods.</span></span> <span data-ttu-id="709a7-186">静的メソッドは多くの場合、テーブルに格納されているデータを操作するために使用します。</span><span class="sxs-lookup"><span data-stu-id="709a7-186">Static methods are often used to work with data that is stored in tables.</span></span> <span data-ttu-id="709a7-187">メンバー変数は静的メソッドで使用できません。</span><span class="sxs-lookup"><span data-stu-id="709a7-187">Member variables can't be used in a static method.</span></span> 

<span data-ttu-id="709a7-188">静的メソッドを呼び出すには、次の構文を使用します。</span><span class="sxs-lookup"><span data-stu-id="709a7-188">You use the following syntax to call static methods.</span></span>

```xpp
ClassName::methodName();
```

<span data-ttu-id="709a7-189">インスタンス メソッドを静的メソッドに変換する場合は、クライアントを再起動する必要があります。</span><span class="sxs-lookup"><span data-stu-id="709a7-189">If you convert an instance method to a static method, you must restart the client.</span></span> <span data-ttu-id="709a7-190">それ以外の場合、コンパイラは変更を検出しません。</span><span class="sxs-lookup"><span data-stu-id="709a7-190">Otherwise, the compiler doesn't detect the change.</span></span> <span data-ttu-id="709a7-191">インスタンス メソッドを静的メソッドに変換した後は、クラスのインスタンスからメソッドを呼び出すことができなくなります。</span><span class="sxs-lookup"><span data-stu-id="709a7-191">After you've converted an instance method to a static method, you can no longer call the method from the instance of the class.</span></span> <span data-ttu-id="709a7-192">代わりに、クラス自体からメソッドを呼び出す必要があります。</span><span class="sxs-lookup"><span data-stu-id="709a7-192">Instead, you must call the method from the class itself.</span></span> <span data-ttu-id="709a7-193">静的メソッドの詳細については、[X++ 静的クラス](xpp-static-classes.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="709a7-193">For more information about static methods, see [X++ static classes](xpp-static-classes.md).</span></span>

### <a name="main-methods"></a><span data-ttu-id="709a7-194">主要メソッド</span><span class="sxs-lookup"><span data-stu-id="709a7-194">main methods</span></span>

<span data-ttu-id="709a7-195">**メイン** メソッドは、メニュー オプションから直接実行されるクラス メソッドです。</span><span class="sxs-lookup"><span data-stu-id="709a7-195">A **main** method is a class method that is run directly from a menu option.</span></span> <span data-ttu-id="709a7-196">このメソッドでは、オブジェクトのインスタンスを作成してから、必要なメンバー メソッドを呼び出す必要があります。</span><span class="sxs-lookup"><span data-stu-id="709a7-196">The method should only create an instance of the object and then call the required member methods.</span></span> <span data-ttu-id="709a7-197">**\_args** パラメーターを使用して、メソッドにデータを転送できます。</span><span class="sxs-lookup"><span data-stu-id="709a7-197">The **\_args** parameter lets you transfer data to the method.</span></span>

```xpp
static void main (Args _args)
{
    // Your code here.
}
```

### <a name="declaration-of-methods"></a><span data-ttu-id="709a7-198">メソッドの宣言</span><span class="sxs-lookup"><span data-stu-id="709a7-198">Declaration of methods</span></span>

<span data-ttu-id="709a7-199">メソッドの宣言は、ヘッダーと本文で構成されます。</span><span class="sxs-lookup"><span data-stu-id="709a7-199">Method declarations consist of a header and a body.</span></span> <span data-ttu-id="709a7-200">メソッド ヘッダーは、メソッドの名前と戻り値の型、メソッド モディファイア、およびパラメーターを宣言します。</span><span class="sxs-lookup"><span data-stu-id="709a7-200">The method header declares the method's name and return type), the method modifiers, and parameters.</span></span> <span data-ttu-id="709a7-201">(戻り値の型が **無効** である可能性があります。) メソッド本体は、変数宣言、メソッド宣言、および明細書で構成されます。</span><span class="sxs-lookup"><span data-stu-id="709a7-201">(The return type might be **void**.) The method body consists of variable declarations, method declarations, and statements.</span></span>

### <a name="return-type"></a><span data-ttu-id="709a7-202">戻り値の型</span><span class="sxs-lookup"><span data-stu-id="709a7-202">Return type</span></span>

<span data-ttu-id="709a7-203">各メソッドには、戻り値の型が必要です。</span><span class="sxs-lookup"><span data-stu-id="709a7-203">A return type is required for each method.</span></span> <span data-ttu-id="709a7-204">メソッドが何も返さない場合、**無効** キーワードを戻り値の型として使用します。</span><span class="sxs-lookup"><span data-stu-id="709a7-204">If a method doesn't return anything, use the **void** keyword as the return type.</span></span> 

<span data-ttu-id="709a7-205">次の例は、2 つのメソッドを示しています。</span><span class="sxs-lookup"><span data-stu-id="709a7-205">The following example shows two methods.</span></span> <span data-ttu-id="709a7-206">1 つの方法に戻り値の型がありますが、他の方法には戻り値の型がありません。</span><span class="sxs-lookup"><span data-stu-id="709a7-206">One method has a return type, but the other method doesn't have a return type.</span></span>

```xpp
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

### <a name="syntax"></a><span data-ttu-id="709a7-207">構文</span><span class="sxs-lookup"><span data-stu-id="709a7-207">Syntax</span></span>

<span data-ttu-id="709a7-208">メソッド宣言 = *見出し*  *本文* 見出し = **\[** *モディファイアー* **\]**  *戻り値の型*  *MethodName*  **(**  *パラメーター リスト*  **)**</span><span class="sxs-lookup"><span data-stu-id="709a7-208">Method declaration = *Heading*  *Body* Heading = **\[** *Modifiers* **\]**  *ReturnType*  *MethodName*  **(**  *ParameterList*  **)**</span></span> 

<span data-ttu-id="709a7-209">モディファイアー = **\[クライアント\] \[サーバー\] \[編集 | 表示 | パブリック | 保護 |プライベート\] \[静的 | 抽象 | 最終\]**</span><span class="sxs-lookup"><span data-stu-id="709a7-209">Modifiers = **\[client\] \[server\] \[edit | display | public | protected | private\] \[static | abstract | final \]**</span></span> 

<span data-ttu-id="709a7-210">ReturnType = *データ型*  **| void | anytype**</span><span class="sxs-lookup"><span data-stu-id="709a7-210">ReturnType = *Datatype*  **| void | anytype**</span></span> 

<span data-ttu-id="709a7-211">MethodName = *識別子*</span><span class="sxs-lookup"><span data-stu-id="709a7-211">MethodName = *Identifier*</span></span> 

<span data-ttu-id="709a7-212">パラメーター リスト = **\[** *パラメーター* \**{、\*\*\*パラメーター* **}\]**</span><span class="sxs-lookup"><span data-stu-id="709a7-212">ParameterList = **\[** *Parameter*  **{ ,**  *Parameter*  **}\]**</span></span> 

<span data-ttu-id="709a7-213">パラメーター = *データ型* *変数識別子* **\[ =**  *式*  **\]**</span><span class="sxs-lookup"><span data-stu-id="709a7-213">Parameter = *Datatype*  *Variableidentifier*  **\[ =**  *Expression*  **\]**</span></span> 

<span data-ttu-id="709a7-214">本文 = **{ \[**  *変数宣言*  **\] \[**  *埋め込み関数用の宣言*  **\] \[**  *明細書*  **\] }**</span><span class="sxs-lookup"><span data-stu-id="709a7-214">Body = **{ \[**  *VariableDeclarations*  **\] \[**  *EmbeddedFunctionDeclarations*  **\] \[**  *Statements*  **\] }**</span></span> 

<span data-ttu-id="709a7-215">埋め込み関数用の宣言 = *見出し*  **{\[**  *変数宣言*  **\] \[**  *明細書*  **\]}**</span><span class="sxs-lookup"><span data-stu-id="709a7-215">EmbeddedFunctionDeclaration = *Heading*  **{\[**  *VariableDeclarations*  **\] \[**  *Statements*  **\]}**</span></span> 

<span data-ttu-id="709a7-216">**Anytype** 戻り値の型を使用すると、メソッドは任意のデータ型を返すことができます。</span><span class="sxs-lookup"><span data-stu-id="709a7-216">If you use the **anytype** return type, the method can return any data type.</span></span>

### <a name="example-of-a-method-that-doesnt-have-a-return-type"></a><span data-ttu-id="709a7-217">戻り値の型を設定していないメソッドの例</span><span class="sxs-lookup"><span data-stu-id="709a7-217">Example of a method that doesn't have a return type</span></span>

```xpp
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

### <a name="example-of-a-method-that-has-parameters"></a><span data-ttu-id="709a7-218">パラメーターを持つメソッドの例</span><span class="sxs-lookup"><span data-stu-id="709a7-218">Example of a method that has parameters</span></span>

<span data-ttu-id="709a7-219">次の例では、**checkAccountBlocked** メソッドはブール値を返し、**amountCur** パラメーターで動作します。</span><span class="sxs-lookup"><span data-stu-id="709a7-219">In the following example, the **checkAccountBlocked** method returns a Boolean value and acts on the **amountCur** parameter.</span></span>

```xpp
boolean checkAccountBlocked(AmountCur amountCur)
{
    if (this.blocked == CustVendorBlocked::All 
        ||(this.blocked == CustVendorBlocked::Invoice 
        && amountCur > 0 ))
    return checkFailed(strFmt("@SYS7987",this.accountNum));
    return true;
}
```

## <a name="method-modifiers"></a><span data-ttu-id="709a7-220">メソッド modifiers</span><span class="sxs-lookup"><span data-stu-id="709a7-220">Method modifiers</span></span>
<span data-ttu-id="709a7-221">いくつかのモディファイアーは、メソッドの宣言に適用することができます。</span><span class="sxs-lookup"><span data-stu-id="709a7-221">Several modifiers can be applied to method declarations.</span></span> <span data-ttu-id="709a7-222">一部の修飾子を結合できます (たとえば、**final static**)。</span><span class="sxs-lookup"><span data-stu-id="709a7-222">Some of the modifiers can be combined (for example, **final static**).</span></span> <span data-ttu-id="709a7-223">メソッド モディファイア キーワードを次に示します。</span><span class="sxs-lookup"><span data-stu-id="709a7-223">Here are the method modifier keywords:</span></span>

-   <span data-ttu-id="709a7-224">**抽象**: メソッドは宣言されていますが、親クラスで実装されていません。</span><span class="sxs-lookup"><span data-stu-id="709a7-224">**abstract**: The method is declared but isn't implemented in a parent class.</span></span> <span data-ttu-id="709a7-225">このメソッドはサブクラスで上書きする必要があります。</span><span class="sxs-lookup"><span data-stu-id="709a7-225">The method must be overridden in subclasses.</span></span> <span data-ttu-id="709a7-226">サブクラスに親クラスに属する 1 つ以上の抽象メソッドがあり、オーバーライドされていません。そのサブクラスからオブジェクトを作成しようとすると、コンパイラ エラーが発生します。</span><span class="sxs-lookup"><span data-stu-id="709a7-226">If you try to create an object from a subclass where one or more abstract methods that belong to the parent class haven't been overridden, you receive a compiler error.</span></span> 

    <span data-ttu-id="709a7-227">クラスは抽象クラスにすることもできます。</span><span class="sxs-lookup"><span data-stu-id="709a7-227">Classes can also be abstract.</span></span> <span data-ttu-id="709a7-228">場合によっては、抽象的な概念を表す場合でもクラスをインスタンス化しないでください。</span><span class="sxs-lookup"><span data-stu-id="709a7-228">Sometimes, a class should not be instantiated even though it represents an abstract concept.</span></span> <span data-ttu-id="709a7-229">サブクラスのみインスタンスを作成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="709a7-229">Only subclasses should be instantiated.</span></span> <span data-ttu-id="709a7-230">このタイプの基本クラスは **抽象** として宣言できます。</span><span class="sxs-lookup"><span data-stu-id="709a7-230">Base classes of this type can be declared as **abstract**.</span></span> <span data-ttu-id="709a7-231">たとえば、勘定の概念をモデル化します。</span><span class="sxs-lookup"><span data-stu-id="709a7-231">For example, you want to model the concept of an account.</span></span> <span data-ttu-id="709a7-232">実際の世界には派生クラス (勘定科目など) しか存在しないため、勘定は抽象です。</span><span class="sxs-lookup"><span data-stu-id="709a7-232">Accounts are abstract, because only derived classes (ledger accounts and so on) exist in the real world.</span></span> <span data-ttu-id="709a7-233">この例では、**勘定** クラスを **抽象** として宣言する必要があるという明確なケースについて説明します。</span><span class="sxs-lookup"><span data-stu-id="709a7-233">This examples describes a clear case where you should declare the **Account** class as **abstract**.</span></span>
-   <span data-ttu-id="709a7-234">**ディスプレイ**: メソッドの戻り値は、ページまたはレポートに表示される必要があります。</span><span class="sxs-lookup"><span data-stu-id="709a7-234">**display**: The method's return value should be shown on a page or a report.</span></span> <span data-ttu-id="709a7-235">ページまたはレポートで値を変更することはできません。</span><span class="sxs-lookup"><span data-stu-id="709a7-235">The value can't be modified on the page or report.</span></span> <span data-ttu-id="709a7-236">通常、戻り値は合計などの計算された値です。</span><span class="sxs-lookup"><span data-stu-id="709a7-236">Typically, the return value is a calculated value, such as a sum.</span></span>
-   <span data-ttu-id="709a7-237">**編集**: メソッドの戻り値のタイプは、ページで使用されるフィールドの情報を提供するために使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="709a7-237">**edit**: The method's return type should be used to provide information for a field that is used on a page.</span></span> <span data-ttu-id="709a7-238">このフィールドの値は修正できます。</span><span class="sxs-lookup"><span data-stu-id="709a7-238">The value in the field can be modified.</span></span>
-   <span data-ttu-id="709a7-239">**最終**: 同じクラスから派生したクラスのメソッドに上書きすることはできません。</span><span class="sxs-lookup"><span data-stu-id="709a7-239">**final**: The method can't be overridden in any class that derives from its class.</span></span>
-   <span data-ttu-id="709a7-240">**パブリック**: **パブリック** として宣言されるメソッドは、クラスがアクセスできるどの場所にもアクセスでき、サブクラスによって上書きすることができます。</span><span class="sxs-lookup"><span data-stu-id="709a7-240">**public**: Methods that are declared as **public** can be accessed anywhere that the class is accessible, and they can be overridden by subclasses.</span></span> <span data-ttu-id="709a7-241">アクセス修飾子を持たないメソッドは暗黙的にパブリックとなります。</span><span class="sxs-lookup"><span data-stu-id="709a7-241">Methods that have no access modifier are implicitly public.</span></span>
-   <span data-ttu-id="709a7-242">**保護**: **保護** として宣言されるメソッドは、クラス、およびメソッドが宣言されているクラスを拡張するサブクラスのメソッドからのみ呼び出すことができます。</span><span class="sxs-lookup"><span data-stu-id="709a7-242">**protected**: Methods that are declared as **protected** can be called only from methods in the class and in subclasses that extend the class where the method is declared.</span></span>
-   <span data-ttu-id="709a7-243">**プライベート**:  **プライベート** として宣言されるメソッドは、プライベートメソッドが宣言されているクラスのメソッドからのみ呼び出すことができます。</span><span class="sxs-lookup"><span data-stu-id="709a7-243">**private**: Methods that are declared as **private** can be called only from methods in the class where the private method is declared.</span></span>
-   <span data-ttu-id="709a7-244">**静的**: このメソッドはクラス メソッドであり、インスタンスを実行しません。</span><span class="sxs-lookup"><span data-stu-id="709a7-244">**static**: The method is a class method and doesn't act on an instance.</span></span> <span data-ttu-id="709a7-245">静的メソッドは、インスタンス変数を参照できません。</span><span class="sxs-lookup"><span data-stu-id="709a7-245">Static methods can't refer to instance variables.</span></span> <span data-ttu-id="709a7-246">クラスのインスタンスでは呼び出されません。</span><span class="sxs-lookup"><span data-stu-id="709a7-246">They aren't invoked on an instance of the class.</span></span> <span data-ttu-id="709a7-247">代わりに、クラス名を使用して呼び出されます (たとえば、**MyClass::aStaticProcedure()**)。</span><span class="sxs-lookup"><span data-stu-id="709a7-247">Instead, they are invoked by using the class name (for example, **MyClass::aStaticProcedure()**).</span></span>

### <a name="methods-that-have-modifiers"></a><span data-ttu-id="709a7-248">モディファイアーのあるメソッド</span><span class="sxs-lookup"><span data-stu-id="709a7-248">Methods that have modifiers</span></span>

<span data-ttu-id="709a7-249">次の例は、メソッドの見出しのみを示しています。</span><span class="sxs-lookup"><span data-stu-id="709a7-249">The following examples show only the method headers.</span></span>

```xpp
// A method that cannot be overridden
final int dontAlterMe() 

// A static method 
static void noChange()

// A display method that returns an integer
display int value()
```

## <a name="method-access-control"></a><span data-ttu-id="709a7-250">メソッド アクセス制御</span><span class="sxs-lookup"><span data-stu-id="709a7-250">Method access control</span></span>

<span data-ttu-id="709a7-251">その他のクラスのメソッドがお客様のクラスのメソッドを呼び出すことができるかどうかを制御するには、アクセサー キーワード **public**、**protected**、および **private** を使用します。</span><span class="sxs-lookup"><span data-stu-id="709a7-251">You use the accessor keywords **public**, **protected**, and **private** to control whether the methods in other classes can call the methods on your class.</span></span> <span data-ttu-id="709a7-252">メソッドのアクセス キーワードは、クラス継承のルールとも連携します。</span><span class="sxs-lookup"><span data-stu-id="709a7-252">The accessor keywords on methods also interact with the rules for class inheritance.</span></span> <span data-ttu-id="709a7-253">メソッドを使用するアクセサー キーワードを次に示します。</span><span class="sxs-lookup"><span data-stu-id="709a7-253">Here are the accessor keywords that you use with methods:</span></span>

-   <span data-ttu-id="709a7-254">**パブリック** – **パブリック** として宣言されるメソッドは、クラスがアクセスできるどの場所からでも呼び出すことができます。</span><span class="sxs-lookup"><span data-stu-id="709a7-254">**public**: Methods that are declared as **public** can be called from anywhere that the class is accessible.</span></span> <span data-ttu-id="709a7-255">さらに、メソッドが **最終** として宣言されていない限り、パブリック メソッドをサブクラスでオーバーライドできます。</span><span class="sxs-lookup"><span data-stu-id="709a7-255">In addition, a public method can be overridden by a subclass, unless the method is declared as **final**.</span></span>
-   <span data-ttu-id="709a7-256">**保護**: **保護** として宣言されるメソッドは、次のメソッドからのみ呼び出すことができます。</span><span class="sxs-lookup"><span data-stu-id="709a7-256">**protected**: Methods that are declared as **protected** can be called only from the following methods:</span></span>
    -   <span data-ttu-id="709a7-257">クラスのメソッド。</span><span class="sxs-lookup"><span data-stu-id="709a7-257">Methods in the class.</span></span>
    -   <span data-ttu-id="709a7-258">保護されたメソッドを含むクラスのサブクラス内のメソッド。</span><span class="sxs-lookup"><span data-stu-id="709a7-258">Methods in a subclass of the class that contains the protected method.</span></span> <span data-ttu-id="709a7-259">保護されているメソッドは、サブクラスで上書きできます。</span><span class="sxs-lookup"><span data-stu-id="709a7-259">Methods that are protected can be overridden in subclasses.</span></span>
-   <span data-ttu-id="709a7-260">**プライベート**:  **プライベート** として宣言されるメソッドは、プライベートメソッドが宣言されているクラスのメソッドからのみ呼び出すことができます。</span><span class="sxs-lookup"><span data-stu-id="709a7-260">**private**: Methods that are declared as **private** can be called only from methods in the class where the private method is declared.</span></span> <span data-ttu-id="709a7-261">サブクラスでプライベート メソッドをオーバーライドできません。</span><span class="sxs-lookup"><span data-stu-id="709a7-261">No private method can be overridden in a subclass.</span></span> <span data-ttu-id="709a7-262">既定では、新しいメソッドを作成するときに、**プライベート** アクセサー キーワードがコード エディターに表示されます。</span><span class="sxs-lookup"><span data-stu-id="709a7-262">By default, when you create a new method, the **private** accessor keyword appears in the code editor.</span></span> <span data-ttu-id="709a7-263">最大限のセキュリティについては、**プライベート** が最も保守的な既定のアクセス キーワードです。</span><span class="sxs-lookup"><span data-stu-id="709a7-263">For maximum security, **private** is the most conservative default accessor keyword.</span></span>

### <a name="static-and-instance-methods"></a><span data-ttu-id="709a7-264">静的およびインスタンス メソッド</span><span class="sxs-lookup"><span data-stu-id="709a7-264">Static and instance methods</span></span>

<span data-ttu-id="709a7-265">メソッドのアクセサー キーワードは、どのメソッドが静的であるか、静的でないかに関係なく、同じクラスにある 2 つのメソッド間の呼び出しを制限することはありません。</span><span class="sxs-lookup"><span data-stu-id="709a7-265">The accessor keywords on methods never restrict calls between two methods that are in the same class, regardless of which method is static or non-static.</span></span> <span data-ttu-id="709a7-266">静的メソッドでは、**新しい** コンストラクター メソッドが **プライベート** モディファイアーで修飾されている場合でも、**新しい** コンストラクター メソッドに対する呼び出しは有効です。</span><span class="sxs-lookup"><span data-stu-id="709a7-266">In a static method, calls to the **new** constructor method are valid even if the **new** constructor method is decorated with the **private** modifier.</span></span> <span data-ttu-id="709a7-267">これらの呼び出しの構文では、**新しい** キーワードを使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="709a7-267">The syntax for these calls requires that the **new** keyword be used.</span></span> <span data-ttu-id="709a7-268">静的メソッドのコードは、クラスのインスタンス メソッドを呼び出す前に、独自のクラスのインスタンス オブジェクトを構築する必要があります。</span><span class="sxs-lookup"><span data-stu-id="709a7-268">The code in a static method must construct an instance object of its own class before it can call any instance methods on the class.</span></span>

### <a name="increasing-access-during-overrides"></a><span data-ttu-id="709a7-269">オーバーライド中のアクセス増加</span><span class="sxs-lookup"><span data-stu-id="709a7-269">Increasing access during overrides</span></span>

<span data-ttu-id="709a7-270">サブクラス内でメソッドがオーバーライドされると、オーバーライドするメソッドは少なくともオーバーライドされるメソッドと同程度のアクセスが可能なことが必要です。</span><span class="sxs-lookup"><span data-stu-id="709a7-270">When a method is overridden in a subclass, the overriding method must be at least as accessible as the overridden method.</span></span> <span data-ttu-id="709a7-271">たとえば、次のコンパイラ ルールは、サブクラスで保護されたメソッドが上書きされる時に適用されます。</span><span class="sxs-lookup"><span data-stu-id="709a7-271">For example, the following compiler rules apply when a protected method is overridden in a subclass:</span></span>

-   <span data-ttu-id="709a7-272">スーパークラスのパブリック メソッドは、サブクラスのパブリック メソッドによってのみ上書きできます。</span><span class="sxs-lookup"><span data-stu-id="709a7-272">A public method in a superclass can be overridden only by a public method in the subclass.</span></span>
-   <span data-ttu-id="709a7-273">サブクラスでは、パブリック メソッドまたは保護対象のメソッドはスーパークラスの保護対象のメソッドをオーバーライドできません。</span><span class="sxs-lookup"><span data-stu-id="709a7-273">In a subclass, a public or protected method can override a protected method of the superclass.</span></span>
-   <span data-ttu-id="709a7-274">サブクラスでは、プライベート メソッドはスーパークラスの保護対象のメソッドをオーバーライドできません。</span><span class="sxs-lookup"><span data-stu-id="709a7-274">In a subclass, a private method can't override a protected method of the superclass.</span></span>

## <a name="optional-parameters"></a><span data-ttu-id="709a7-275">オプションのパラメーター</span><span class="sxs-lookup"><span data-stu-id="709a7-275">Optional parameters</span></span>
<span data-ttu-id="709a7-276">パラメーターは、メソッド宣言で初期化することができます。</span><span class="sxs-lookup"><span data-stu-id="709a7-276">Parameters can be initialized in the method declaration.</span></span> <span data-ttu-id="709a7-277">この場合、パラメーターは *オプションのパラメーター* となります。</span><span class="sxs-lookup"><span data-stu-id="709a7-277">In this case, the parameter becomes an *optional parameter*.</span></span> <span data-ttu-id="709a7-278">メソッドの呼び出しの値が指定されていない場合は、既定値が使用されます。</span><span class="sxs-lookup"><span data-stu-id="709a7-278">If no value is supplied in the method call, the default value is used.</span></span> <span data-ttu-id="709a7-279">すべての必須パラメータは最初のオプション パラメーターの前に一覧表示する必要があります。</span><span class="sxs-lookup"><span data-stu-id="709a7-279">All required parameters must be listed before the first optional parameter.</span></span> <span data-ttu-id="709a7-280">次の例では、オプションのパラメーターを持つメソッドを作成して呼び出す方法を示しています。</span><span class="sxs-lookup"><span data-stu-id="709a7-280">The following examples show how to create and call a method that has optional parameters.</span></span> <span data-ttu-id="709a7-281">**AddThreeInts** メソッドの例は、メソッドを呼び出すときにデフォルトのパラメーターをスキップできないことを示しています。</span><span class="sxs-lookup"><span data-stu-id="709a7-281">The example of the **AddThreeInts** method shows that you can't skip default parameters when you call a method.</span></span>

### <a name="examples-of-optional-parameters"></a><span data-ttu-id="709a7-282">オプション パラメーターの例</span><span class="sxs-lookup"><span data-stu-id="709a7-282">Examples of optional parameters</span></span>

<span data-ttu-id="709a7-283">既定のパラメータを持つクラスのコード例を次に示します。</span><span class="sxs-lookup"><span data-stu-id="709a7-283">The following code example shows a class with a default parameter.</span></span>
```xpp
// This is an example of a function being used as the default.
class Person
{
    date birthDate;

    // The constructor that takes a date type as a parameter. 
    // That value is assigned to the field member birthDate.
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

    public static void callPerson()
    {

        Person person = new Person(13\5\2010);

        // Optional parameter's default is used.
        Info(strFmt('Age in years today is %1 years', 
                real2int(person.CalculateAgeAsOfDate())));

        // January 2, 2044  is the parameter value for _date.
        Info(strFmt('Age in years on %1 is %2 years',
                2\1\2044,
                real2int(person.CalculateAgeAsOfDate(2\1\2044))));
    }

}
```

<span data-ttu-id="709a7-284">次の例では、2 番目の省略可能なパラメーターにスキップできないことを示します。</span><span class="sxs-lookup"><span data-stu-id="709a7-284">This is an example of how you cannot skip to a second optional parameter.</span></span> <span data-ttu-id="709a7-285">**AddThreeInts** メソッドには 2 つの任意のパラメータがあります。</span><span class="sxs-lookup"><span data-stu-id="709a7-285">The **AddThreeInts** method has two optional parameters.</span></span> <span data-ttu-id="709a7-286">**callAdditions** メソッドは、**AddThreeInts** メソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="709a7-286">The **callAdditions** method calls the **AddThreeInts** method.</span></span> <span data-ttu-id="709a7-287">コメント化されたコードは、**\_i3** の既定値のみのオーバーライドを試行しますが、コンパイラでは、呼び出し時に先行するすべての任意のパラメータのオーバーライドを要求します。</span><span class="sxs-lookup"><span data-stu-id="709a7-287">The commented out code tries to override only the **\_i3** default value, but the compiler requires that all prior optional parameters also be overridden in the call.</span></span> 

```xpp
class Additions
{
    public static int AddThreeInts(int _i1, int _i2 = 2,int _i3 = 3)
    {
        return _i1 + _i2 + _i3;
    }

    public static void callAdditions()
    {
        // The next statement does not compile, because it skips the _i2 parameter.
        // info(int2Str(Additions::AddThreeInts(1, , 99)));

        // You must specify both optional parameters.
        info(int2Str(Additions::AddThreeInts(1, 2, 99)));
    }

}
```

## <a name="accessor-methods"></a><span data-ttu-id="709a7-288">アクセサー メソッド</span><span class="sxs-lookup"><span data-stu-id="709a7-288">Accessor methods</span></span>

<span data-ttu-id="709a7-289">クラス変数は既定で保護されます。</span><span class="sxs-lookup"><span data-stu-id="709a7-289">Class variables are protected by default.</span></span> <span data-ttu-id="709a7-290">クラスの内部実装の詳細を非表示にすることで、そのクラスを使用するコードを破棄することなくクラスの実装を後で変更することができます。</span><span class="sxs-lookup"><span data-stu-id="709a7-290">By hiding details of the internal implementation of a class, you can change the implementation of the class later without breaking any code that uses that class.</span></span> <span data-ttu-id="709a7-291">参照変数からデータにアクセスするには、アクセサー メソッドを作成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="709a7-291">To access the data from reference variables, you must create accessor methods.</span></span> <span data-ttu-id="709a7-292">次の例では、アクセス メソッドを使用して変数 **x** および **y** にアクセスする **Point** クラスを定義します。</span><span class="sxs-lookup"><span data-stu-id="709a7-292">The following example defines a **Point** class that uses accessor methods to access the variables **x** and **y**.</span></span>

```xpp
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

<span data-ttu-id="709a7-293">これらのメソッド宣言は、**Point** クラスが外部からの変数へのアクセスを提供する方法を示しています。</span><span class="sxs-lookup"><span data-stu-id="709a7-293">These method declarations show how the **Point** class provides access to its variables from the outside world.</span></span> <span data-ttu-id="709a7-294">その他のオブジェクトは、アクセサー メソッドを使ってインスタンス変数 **Point** オブジェクトを操作できます。</span><span class="sxs-lookup"><span data-stu-id="709a7-294">Other objects can manipulate the instance variables of **Point** objects by using the accessor methods.</span></span>

```xpp
Point myPoint = new Point();
// Set the x variable using the accessor method.
myPoint.setX(4.0);
// Get the x variable using the accessor method.
info(any2Str(myPoint.getX()));
```

## <a name="parameters"></a><span data-ttu-id="709a7-295">パラメーター</span><span class="sxs-lookup"><span data-stu-id="709a7-295">Parameters</span></span>

<span data-ttu-id="709a7-296">すべてのメソッドは独自の *スコープ* を持っています。</span><span class="sxs-lookup"><span data-stu-id="709a7-296">All methods have their own *scope*.</span></span> <span data-ttu-id="709a7-297">メソッドは、1 つ以上のパラメーターを受け取ることができます。</span><span class="sxs-lookup"><span data-stu-id="709a7-297">A method can take one or more parameters.</span></span> <span data-ttu-id="709a7-298">メソッドのスコープ内では、これらのパラメーターはローカル変数として処理され、メソッド呼び出しのパラメーターからの値で初期化されます。</span><span class="sxs-lookup"><span data-stu-id="709a7-298">Within the scope of the method, these parameters are treated as local variables and are initialized with a value from the parameter in the method call.</span></span> <span data-ttu-id="709a7-299">すべてのパラメーターは値で渡されるため、元の変数の値を変更することはできません。</span><span class="sxs-lookup"><span data-stu-id="709a7-299">All parameters are passed by value, which means that you can't change the value of the original variable.</span></span> <span data-ttu-id="709a7-300">メソッド内のローカル変数のみを変更することができます。</span><span class="sxs-lookup"><span data-stu-id="709a7-300">You can change only the local variable in the method.</span></span> <span data-ttu-id="709a7-301">このローカル変数は元の変数のコピーです。</span><span class="sxs-lookup"><span data-stu-id="709a7-301">This local variable is a copy of the original variable.</span></span>

## <a name="scope-of-variables-in-methods"></a><span data-ttu-id="709a7-302">メソッドでの変数の範囲</span><span class="sxs-lookup"><span data-stu-id="709a7-302">Scope of variables in methods</span></span>

<span data-ttu-id="709a7-303">スコープは、品目にアクセスできるエリアを定義します。</span><span class="sxs-lookup"><span data-stu-id="709a7-303">A scope defines the area in which an item can be accessed.</span></span> <span data-ttu-id="709a7-304">クラスで定義されている変数は、そのクラス内のメソッドで使用できます。</span><span class="sxs-lookup"><span data-stu-id="709a7-304">Variables that are defined in a class are available to the methods within that class.</span></span> <span data-ttu-id="709a7-305">メソッド内の変数は、現在のブロック内でのみアクセスできます。</span><span class="sxs-lookup"><span data-stu-id="709a7-305">Variables in methods can be accessed only within the current block.</span></span>

## <a name="local-functions"></a><span data-ttu-id="709a7-306">ローカル関数</span><span class="sxs-lookup"><span data-stu-id="709a7-306">Local functions</span></span>

<span data-ttu-id="709a7-307">メソッド内部のローカル関数を宣言することができます。</span><span class="sxs-lookup"><span data-stu-id="709a7-307">You can declare functions inside a method.</span></span> <span data-ttu-id="709a7-308">これは、ローカル関数と呼ばれます。</span><span class="sxs-lookup"><span data-stu-id="709a7-308">These are called local functions.</span></span> <span data-ttu-id="709a7-309">可能ではあるものの、ベスト プラクティスではありません。</span><span class="sxs-lookup"><span data-stu-id="709a7-309">While possible, it is not a best practice.</span></span> <span data-ttu-id="709a7-310">代わりに、プライベート メソッドをクラスに追加する必要があります。</span><span class="sxs-lookup"><span data-stu-id="709a7-310">Instead, you should add private methods to the class.</span></span> 

-   <span data-ttu-id="709a7-311">ローカル関数の宣言は、メソッド内の宣言されていないステートメントの前に物理的に先行する必要があります。</span><span class="sxs-lookup"><span data-stu-id="709a7-311">The declarations of local functions must physically precede any non-declaration statements in the method.</span></span>
-   <span data-ttu-id="709a7-312">メソッド内で 1 つ以上のローカル関数を宣言することができます。</span><span class="sxs-lookup"><span data-stu-id="709a7-312">You can declare more than one local function in your method.</span></span> <span data-ttu-id="709a7-313">ただし、すべてのローカル関数は中断のないシリーズで宣言され、セットは 1 つのセミコロン (;) で終了する必要があります。</span><span class="sxs-lookup"><span data-stu-id="709a7-313">However, all local functions must be declared in an uninterrupted series, and the set must be terminated by one semicolon (;).</span></span>
-   <span data-ttu-id="709a7-314">ローカル関数内にあるコードは、ローカル関数を含むメソッドで宣言されている変数にアクセスできます。</span><span class="sxs-lookup"><span data-stu-id="709a7-314">Code that is inside the local function can access variables that are declared in the method that contains the local function.</span></span>
-   <span data-ttu-id="709a7-315">ローカル関数の外にあるコードは、ローカル関数で宣言された変数にアクセスすることはできません。</span><span class="sxs-lookup"><span data-stu-id="709a7-315">Code that is outside the local function can't access variables that are declared in the local function.</span></span>
-   <span data-ttu-id="709a7-316">ローカル関数は、ローカル関数が宣言されているのと同じメソッド内のコードによってのみ呼び出すことができます。</span><span class="sxs-lookup"><span data-stu-id="709a7-316">A local function can be called only by code in the same method where the local function is declared.</span></span>
-   <span data-ttu-id="709a7-317">ローカル関数が、それ自体を呼び出すことはありません。</span><span class="sxs-lookup"><span data-stu-id="709a7-317">A local function should never call itself.</span></span> <span data-ttu-id="709a7-318">このような再帰は、正常に行われるコンパイルを防ぐことができます。</span><span class="sxs-lookup"><span data-stu-id="709a7-318">Such recursion can prevent successful compilation.</span></span>

<span data-ttu-id="709a7-319">次の例は、2 つのローカル関数である **localFunctionA** および **localFunctionB** の有効な宣言を示しています。</span><span class="sxs-lookup"><span data-stu-id="709a7-319">The following example shows valid declarations of two local functions, **localFunctionA** and **localFunctionB**.</span></span> <span data-ttu-id="709a7-320">ローカル関数への呼び出しは、必要に応じて、この例の関数宣言の後に行われます。</span><span class="sxs-lookup"><span data-stu-id="709a7-320">Calls to the local functions occur after the function declarations in the example, as is required.</span></span>

```xpp
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

## <a name="the-this-keyword"></a><span data-ttu-id="709a7-321">このキーワード</span><span class="sxs-lookup"><span data-stu-id="709a7-321">The this keyword</span></span>
<span data-ttu-id="709a7-322">**this** キーワードは、**this** キーワードが使用されるクラスやテーブルのインスタンスへの参照です。</span><span class="sxs-lookup"><span data-stu-id="709a7-322">The **this** keyword is a reference to the instance of the class or table where the **this** keyword is used.</span></span> <span data-ttu-id="709a7-323">**this** 参照が必須になることはありませんが、コードを明確にし、コード エディターで IntelliSense の動作を強化することができます。</span><span class="sxs-lookup"><span data-stu-id="709a7-323">The **this** reference is never required, but it can clarify your code and enhances the behavior of IntelliSense in the code editor.</span></span> <span data-ttu-id="709a7-324">すべての呼び出しインスタンス メソッドは **これ** を参照または変数のいずれかにより修飾される必要があります。</span><span class="sxs-lookup"><span data-stu-id="709a7-324">All calls to instance methods must be qualified by either the **this** reference or a variable.</span></span> <span data-ttu-id="709a7-325">**this** 参照は、次の情報を修飾するために使用できます。</span><span class="sxs-lookup"><span data-stu-id="709a7-325">The **this** reference can be used to qualify the following information:</span></span>

-   <span data-ttu-id="709a7-326">**this** 参照が使用されている同じクラス内の他のインスタンス (静的でない) メソッドの名前。</span><span class="sxs-lookup"><span data-stu-id="709a7-326">The names of other instance (non-static) methods in the same class where the **this** reference is used.</span></span> <span data-ttu-id="709a7-327">次の例を示します: `boolColorChanged = this.colorItOrange();`</span><span class="sxs-lookup"><span data-stu-id="709a7-327">Here is an example: `boolColorChanged = this.colorItOrange();`</span></span>
-   <span data-ttu-id="709a7-328">**this** オブジェクトによって継承されるメソッドの名前。</span><span class="sxs-lookup"><span data-stu-id="709a7-328">The names of methods that are inherited by the **this** object.</span></span>
-   <span data-ttu-id="709a7-329">**this** キーワードが使用されるメソッドを含むテーブル上のフィールドの名前。</span><span class="sxs-lookup"><span data-stu-id="709a7-329">The names of fields on the table that contains the method that the **this** keyword is used in.</span></span>

<span data-ttu-id="709a7-330">**this** 参照は、次の方法で使用できません。</span><span class="sxs-lookup"><span data-stu-id="709a7-330">The **this** reference can't be used in the following ways:</span></span>

-   <span data-ttu-id="709a7-331">**classDeclaration** コードで宣言されているメンバー変数の名前を限定することはできません。</span><span class="sxs-lookup"><span data-stu-id="709a7-331">It can't qualify the names of member variables that are declared in the **classDeclaration** code.</span></span>
-   <span data-ttu-id="709a7-332">静的メソッドで使用できません。</span><span class="sxs-lookup"><span data-stu-id="709a7-332">It can't be used in a static method.</span></span>
-   <span data-ttu-id="709a7-333">クラスやテーブルの静的メソッドの名前を限定することはできません。</span><span class="sxs-lookup"><span data-stu-id="709a7-333">It can't qualify the names of static methods of the class or table.</span></span>

## <a name="call-stack-limitation"></a><span data-ttu-id="709a7-334">呼び出しスタック制限</span><span class="sxs-lookup"><span data-stu-id="709a7-334">Call stack limitation</span></span>

<span data-ttu-id="709a7-335">コール スタックの深さは 100 に制限されています。</span><span class="sxs-lookup"><span data-stu-id="709a7-335">The depth of the call stack is limited to 100.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]