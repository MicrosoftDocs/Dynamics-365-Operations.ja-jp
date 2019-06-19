---
title: X++ クラスおよびメソッド
description: このトピックでは、X++ でクラスやインターフェイスを作成および使用する方法について説明します。
author: RobinARH
manager: AnnBe
ms.date: 11/03/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Developer
ms.reviewer: robinr
ms.search.scope: Operations
ms.custom: 150303
ms.assetid: 1b2d76d1-52d9-46b2-937f-5a3b62f2d516
ms.search.region: Global
ms.author: robinr
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 8ee078c78dabcc5a0e0e36e9495b8bc9891bbc40
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/15/2019
ms.locfileid: "1544180"
---
# <a name="x-classes-and-methods"></a><span data-ttu-id="8d8c6-103">X++ クラスおよびメソッド</span><span class="sxs-lookup"><span data-stu-id="8d8c6-103">X++ classes and methods</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="8d8c6-104">このトピックでは、X++ でクラスやインターフェイスを作成および使用する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="8d8c6-104">This topic describes how to create and use classes and interfaces in X++.</span></span>

<a name="classes-in-x"></a><span data-ttu-id="8d8c6-105">X++ のクラス</span><span class="sxs-lookup"><span data-stu-id="8d8c6-105">Classes in X++</span></span>
--------------

<span data-ttu-id="8d8c6-106">*クラス*は、そのクラスから後に構築されるオブジェクトのデータとメソッドを定義するソフトウェア構造です。</span><span class="sxs-lookup"><span data-stu-id="8d8c6-106">A *class* is a software construct that defines the data and methods of the objects that are later constructed from that class.</span></span> <span data-ttu-id="8d8c6-107">構築されるオブジェクトは、*インスタンス* または *オブジェクト* と呼ばれます。</span><span class="sxs-lookup"><span data-stu-id="8d8c6-107">The objects that are constructed are known as *instances* or *objects*.</span></span> <span data-ttu-id="8d8c6-108">(このトピックでは、2 つの用語を同じ意味で使用しています。) データはオブジェクトの状態を表し、メソッドはオブジェクトの動作を表します。</span><span class="sxs-lookup"><span data-stu-id="8d8c6-108">(This topic uses the two terms interchangeably.) The data represents the state of the object, whereas the methods represent the behavior of the object.</span></span> <span data-ttu-id="8d8c6-109">*変数*にはクラスのデータが含まれます。</span><span class="sxs-lookup"><span data-stu-id="8d8c6-109">*Variables* contain the data for the class.</span></span> <span data-ttu-id="8d8c6-110">クラス内の変数は、そのクラスから構成されるオブジェクトに固有です。</span><span class="sxs-lookup"><span data-stu-id="8d8c6-110">Variables in a class are specific to objects that are constructed from that class.</span></span> <span data-ttu-id="8d8c6-111">クラス宣言から構築されたすべてのオブジェクトには、独自の変数のコピーがあります。</span><span class="sxs-lookup"><span data-stu-id="8d8c6-111">Every object that is constructed from the class declaration has its own copy of the variables.</span></span> <span data-ttu-id="8d8c6-112">これらの変数は*インスタンス変数*と呼ばれます。</span><span class="sxs-lookup"><span data-stu-id="8d8c6-112">These variables are known as *instance variables*.</span></span> <span data-ttu-id="8d8c6-113">メソッドはクラスの動作を定義します。</span><span class="sxs-lookup"><span data-stu-id="8d8c6-113">Methods define the behavior of a class.</span></span> <span data-ttu-id="8d8c6-114">データに作用する一連のステートメントです。</span><span class="sxs-lookup"><span data-stu-id="8d8c6-114">They are the sequences of statements that operate on the data.</span></span> <span data-ttu-id="8d8c6-115">通常、メソッドはクラスのインスタンス変数を操作するように宣言されます。</span><span class="sxs-lookup"><span data-stu-id="8d8c6-115">Typically, methods are declared to operate on the instance variables of the class.</span></span> <span data-ttu-id="8d8c6-116">これらのメソッドは、*instance メソッド*または *object メソッド*と呼ばれます。</span><span class="sxs-lookup"><span data-stu-id="8d8c6-116">These methods are known as *instance methods* or *object methods*.</span></span> <span data-ttu-id="8d8c6-117">また、*静的メソッド* および *静的フィールド* を宣言することができます。</span><span class="sxs-lookup"><span data-stu-id="8d8c6-117">You can also declare *static methods* and *static fields*.</span></span>

## <a name="declaration-of-classes"></a><span data-ttu-id="8d8c6-118">クラスの宣言</span><span class="sxs-lookup"><span data-stu-id="8d8c6-118">Declaration of classes</span></span>
### <a name="create-a-class-in-visual-studio"></a><span data-ttu-id="8d8c6-119">Visual Studio でのクラスの作成</span><span class="sxs-lookup"><span data-stu-id="8d8c6-119">Create a class in Visual Studio</span></span>

<span data-ttu-id="8d8c6-120">Microsoft Visual Studio でクラスを作成するには、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="8d8c6-120">Follow these steps to create a class in Microsoft Visual Studio.</span></span>

1.  <span data-ttu-id="8d8c6-121">サーバー エクスプローラーで、プロジェクトを右クリックしてから**追加**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="8d8c6-121">In Server Explorer, right-click the project, and then click **Add**.</span></span>
2.  <span data-ttu-id="8d8c6-122">**新しい項目**ダイアログ ボックスで、**クラス**を選択してからクラスの名前を入力します。</span><span class="sxs-lookup"><span data-stu-id="8d8c6-122">In the **New Item** dialog box, select **Class**, and then enter a name for the class.</span></span>
3.  <span data-ttu-id="8d8c6-123">**追加** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="8d8c6-123">Click **Add**.</span></span>

<span data-ttu-id="8d8c6-124">すべてのクラスはパブリックです。</span><span class="sxs-lookup"><span data-stu-id="8d8c6-124">All classes are public.</span></span> <span data-ttu-id="8d8c6-125">**パブリック** モディファイアーを削除すると、システムではクラスはパブリック クラスとして扱われます。</span><span class="sxs-lookup"><span data-stu-id="8d8c6-125">If you remove the **public** modifier, the system still treats the class as public.</span></span> <span data-ttu-id="8d8c6-126">クラス宣言では、**final** および **extends** などの、他の修飾子を指定することができます。</span><span class="sxs-lookup"><span data-stu-id="8d8c6-126">You can specify other modifiers on the class declaration, such as **final** and **extends**.</span></span>

### <a name="creating-variables-in-a-class"></a><span data-ttu-id="8d8c6-127">クラスで変数を作成しています</span><span class="sxs-lookup"><span data-stu-id="8d8c6-127">Creating variables in a class</span></span>

<span data-ttu-id="8d8c6-128">すべてのクラスはパブリックですが、すべてのメンバー変数は暗黙的に保護されています。</span><span class="sxs-lookup"><span data-stu-id="8d8c6-128">All classes are public, but all member variables are implicitly protected.</span></span> <span data-ttu-id="8d8c6-129">ただし、private、protected または public キーワードを使用してメンバー変数宣言を変更することができます。</span><span class="sxs-lookup"><span data-stu-id="8d8c6-129">However, you can modify the member variable declaration by using the private, protected or public keywords.</span></span> <span data-ttu-id="8d8c6-130">すべてのメンバー変数はクラスのオブジェクト インスタンスにのみ属しています。</span><span class="sxs-lookup"><span data-stu-id="8d8c6-130">All member variables belong to only object instances of the class.</span></span> <span data-ttu-id="8d8c6-131">次の例は、アクセサー メソッドを使用して変数データを公開する方法を示しています。</span><span class="sxs-lookup"><span data-stu-id="8d8c6-131">The following example shows how to use accessor methods to make the variable data public.</span></span>

    public class HasAFirstName
    {
        str firstName;
        public str getFirstName()
        {
            return firstName;
        }

        public void setFirstName(str newName)
        {
           firstName = newName;
        }
    }

## <a name="constructors"></a><span data-ttu-id="8d8c6-132">コンストラクター</span><span class="sxs-lookup"><span data-stu-id="8d8c6-132">Constructors</span></span>
<span data-ttu-id="8d8c6-133">クラスのインスタンスを作成するには、*コンストラクタ*を使用してクラスのインスタンスを生成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="8d8c6-133">To create an instance of a class, you must instantiate it by using a *constructor*.</span></span> <span data-ttu-id="8d8c6-134">既定のコンストラクターは、**新規** メソッドです。</span><span class="sxs-lookup"><span data-stu-id="8d8c6-134">The default constructor is the **new** method.</span></span>

    // Declare a variable to refer to a Point object
    Point myPoint; 

    // Create an instance of a Point object
    myPoint = new Point(); 

<span data-ttu-id="8d8c6-135">ベスト プラクティスとして、**新しい**メソッドを保護する必要があります。</span><span class="sxs-lookup"><span data-stu-id="8d8c6-135">As a best practice, you should make the **new** method protected.</span></span> <span data-ttu-id="8d8c6-136">代わりに、初期化が必要ない場合、**静的コンストラクト** メソッドをクラスのパブリック コンストラクターとして使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="8d8c6-136">Instead, if initialization isn't required, you should use a **static construct** method as the public constructor for the class.</span></span> <span data-ttu-id="8d8c6-137">それ以外の場合、**新しい静的**なメソッドを使う必要があります。</span><span class="sxs-lookup"><span data-stu-id="8d8c6-137">Otherwise, you should use a **static new** method.</span></span>

### <a name="creating-other-objects-in-a-constructor"></a><span data-ttu-id="8d8c6-138">コンストラクターでその他のオブジェクトを作成しています</span><span class="sxs-lookup"><span data-stu-id="8d8c6-138">Creating other objects in a constructor</span></span>

<span data-ttu-id="8d8c6-139">クラス コンストラクターは、クラスのインスタンスを作成するだけでなく、他のオブジェクトをインスタンス化することもできます。</span><span class="sxs-lookup"><span data-stu-id="8d8c6-139">A class constructor can instantiate other objects in addition to creating an instance of the class.</span></span> <span data-ttu-id="8d8c6-140">たとえば、次のコードは、境界を定義するため 2 つの**ポイント**オブジェクトを使用する**長方形**クラスを申告します。</span><span class="sxs-lookup"><span data-stu-id="8d8c6-140">For example, the following code declares a **Rectangle** class that uses two **Point** objects to define its bounds.</span></span>

    class Rectangle1
    {
        Point lowerLeft;
        Point upperRight;

        void new(real _topLeftX, real _topLeftY, real _bottomRightX, real _bottomRightY)
        {
            lowerLeft  = new Point(_topLeftX, _topLeftY);
            upperRight = new Point(_bottomRightX, _bottomRightY);
        }
    }

## <a name="destructors"></a><span data-ttu-id="8d8c6-141">デストラクター</span><span class="sxs-lookup"><span data-stu-id="8d8c6-141">Destructors</span></span>
<span data-ttu-id="8d8c6-142">*デストラクター*は、クラス オブジェクトを明示的に破棄するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="8d8c6-142">A *destructor* is used to explicitly destroy a class object.</span></span> <span data-ttu-id="8d8c6-143">オブジェクトはへの参照がない場合、自動的に破棄されます。</span><span class="sxs-lookup"><span data-stu-id="8d8c6-143">Objects are automatically destroyed when there are no references to them.</span></span> <span data-ttu-id="8d8c6-144">ただし、たとえば、次の方法で対象を明示的に破棄できます。</span><span class="sxs-lookup"><span data-stu-id="8d8c6-144">However, you can destroy objects explicitly in the following ways:</span></span>

-   <span data-ttu-id="8d8c6-145">**finalize** メソッドを使用します。</span><span class="sxs-lookup"><span data-stu-id="8d8c6-145">Use the **finalize** method.</span></span>
-   <span data-ttu-id="8d8c6-146">オブジェクト ハンドルを **null** に設定します。</span><span class="sxs-lookup"><span data-stu-id="8d8c6-146">Set the object handle to **null**.</span></span>

### <a name="using-the-finalize-method"></a><span data-ttu-id="8d8c6-147">finalize メソッドの使用</span><span class="sxs-lookup"><span data-stu-id="8d8c6-147">Using the finalize method</span></span>

<span data-ttu-id="8d8c6-148">オブジェクトを明示的に破棄するには **finalize** メソッドを使用します。</span><span class="sxs-lookup"><span data-stu-id="8d8c6-148">Use the **finalize** method to explicitly destroy an object.</span></span> <span data-ttu-id="8d8c6-149">**finalize** メソッドへの暗黙的な呼び出しはありません。</span><span class="sxs-lookup"><span data-stu-id="8d8c6-149">There are no implicit calls to the **finalize** method.</span></span> <span data-ttu-id="8d8c6-150">そこでステートメントを実行するメソッドを呼び出す必要があります。</span><span class="sxs-lookup"><span data-stu-id="8d8c6-150">You must call the method to run the statements in it.</span></span> <span data-ttu-id="8d8c6-151">次の例は、**finalize** メソッドの呼び出しの基本構造を示しています。</span><span class="sxs-lookup"><span data-stu-id="8d8c6-151">The following example shows the basic structure for a call to the **finalize** method.</span></span>

    // From any method in a class.
    if (condition)
    {
        // Removes object from memory.
        this.finalize(); 
    }

<span data-ttu-id="8d8c6-152">**finalize** メソッドでは、必要なクリーンアップ コードも配置する必要があります。</span><span class="sxs-lookup"><span data-stu-id="8d8c6-152">In the **finalize** method, you should also put any clean-up code that is required.</span></span> <span data-ttu-id="8d8c6-153">たとえば、クラスがダイナミックリンク ライブラリ (DLL) モジュールを使用する場合、必要ではなくなったときに DLL をリリースする**確定**メソッドを使用できます。</span><span class="sxs-lookup"><span data-stu-id="8d8c6-153">For example, if your class uses a dynamic-link library (DLL) module, you can use the **finalize** method to release the DLL when you no longer require it.</span></span> <span data-ttu-id="8d8c6-154">**finalize** メソッドは慎重に使用してください。</span><span class="sxs-lookup"><span data-stu-id="8d8c6-154">Use the **finalize** method carefully.</span></span> <span data-ttu-id="8d8c6-155">オブジェクトへの参照がある場合オブジェクトを破棄します。</span><span class="sxs-lookup"><span data-stu-id="8d8c6-155">It will destroy an object even if there are references to it.</span></span>

### <a name="setting-an-object-handle-to-null"></a><span data-ttu-id="8d8c6-156">オブジェクト ハンドルを null に設定</span><span class="sxs-lookup"><span data-stu-id="8d8c6-156">Setting an object handle to null</span></span>

<span data-ttu-id="8d8c6-157">オブジェクト ハンドルを **null** に設定してオブジェクトを終了します。</span><span class="sxs-lookup"><span data-stu-id="8d8c6-157">Set the object handle to **null** to terminate an object.</span></span> <span data-ttu-id="8d8c6-158">この方法は、他のオブジェクト ハンドルがそのオブジェクトを指していない場合にのみオブジェクトを破棄します。</span><span class="sxs-lookup"><span data-stu-id="8d8c6-158">This approach destroys an object only if no other object handles point to that object.</span></span> <span data-ttu-id="8d8c6-159">他のコードがオブジェクト ハンドルを使用していないことを確認する必要があります。</span><span class="sxs-lookup"><span data-stu-id="8d8c6-159">You should verify that other code isn't using the object handle.</span></span> <span data-ttu-id="8d8c6-160">次の例では、オブジェクト ハンドルを作成し、**null** に設定します。</span><span class="sxs-lookup"><span data-stu-id="8d8c6-160">The following example creates an object handle and then sets it to **null**.</span></span>

    // Create an object handle of the type MyObject.
    MyObject mo;
    // Create an object of MyObject type and link it to the object handle.
    mo = new myObject();
    // Terminate the object.
    mo = null;

## <a name="creating-a-subclass"></a><span data-ttu-id="8d8c6-161">サブクラスを作成しています</span><span class="sxs-lookup"><span data-stu-id="8d8c6-161">Creating a subclass</span></span>
<span data-ttu-id="8d8c6-162">*サブクラス*は拡張または他のクラスから継承されるクラスです。</span><span class="sxs-lookup"><span data-stu-id="8d8c6-162">*Subclasses* are classes that extend or inherit from other classes.</span></span> <span data-ttu-id="8d8c6-163">クラスは、他の 1 つのクラスのみ拡張することができます。</span><span class="sxs-lookup"><span data-stu-id="8d8c6-163">A class can extend only one other class.</span></span> <span data-ttu-id="8d8c6-164">複数の継承はサポートされていません。</span><span class="sxs-lookup"><span data-stu-id="8d8c6-164">Multiple inheritance isn't supported.</span></span> <span data-ttu-id="8d8c6-165">クラスを拡張する場合、サブクラスが親クラスの (*スーパークラス*) すべてのメソッドと変数を継承します。</span><span class="sxs-lookup"><span data-stu-id="8d8c6-165">If you extend a class, the subclass inherits all the methods and variables in the parent class (the *superclass*).</span></span> <span data-ttu-id="8d8c6-166">サブクラスを使用すると、より特殊な目的で既存のコードを再利用できます。</span><span class="sxs-lookup"><span data-stu-id="8d8c6-166">Subclasses let you reuse existing code for a more specific purpose.</span></span> <span data-ttu-id="8d8c6-167">したがって、設計、開発、テストの時間を節約できます。</span><span class="sxs-lookup"><span data-stu-id="8d8c6-167">Therefore, they help save you time during design, development, and testing.</span></span> <span data-ttu-id="8d8c6-168">スーパークラスの動作をカスタマイズするには、サブクラスのメソッドをオーバーライドします。</span><span class="sxs-lookup"><span data-stu-id="8d8c6-168">To customize the behavior of a superclass, override the methods in a subclass.</span></span> <span data-ttu-id="8d8c6-169">多くの場合、スーパークラスは、*基本クラス*として知られており、サブクラスは、*派生クラス*として知られています。</span><span class="sxs-lookup"><span data-stu-id="8d8c6-169">A superclass is often known as a *base class*, and a subclass is often known as a *derived class*.</span></span>

### <a name="subclass-example"></a><span data-ttu-id="8d8c6-170">サブクラスの例</span><span class="sxs-lookup"><span data-stu-id="8d8c6-170">Subclass example</span></span>

<span data-ttu-id="8d8c6-171">次の例では、まず **Point** という名前のクラスを作成します。</span><span class="sxs-lookup"><span data-stu-id="8d8c6-171">The following example first creates a class that is named **Point**.</span></span> <span data-ttu-id="8d8c6-172">その後、**Point** クラスを拡張して、**ThreePoint** という新しいクラスを作成します。</span><span class="sxs-lookup"><span data-stu-id="8d8c6-172">It then extends the **Point** class to create a new class that is named **ThreePoint**.</span></span>

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

### <a name="preventing-class-inheritance"></a><span data-ttu-id="8d8c6-173">クラスの継承を禁止する</span><span class="sxs-lookup"><span data-stu-id="8d8c6-173">Preventing class inheritance</span></span>

<span data-ttu-id="8d8c6-174">**最終** モディファイアーを使用して、クラスが継承されないようにすることができます。</span><span class="sxs-lookup"><span data-stu-id="8d8c6-174">You can prevent classes from being inherited by using the **final** modifier.</span></span>

    public final class Attribute
    {
        int objectField;
    }

## <a name="methods"></a><span data-ttu-id="8d8c6-175">メソッド</span><span class="sxs-lookup"><span data-stu-id="8d8c6-175">Methods</span></span>
<span data-ttu-id="8d8c6-176">次のコード ブロック タイプは、アプリケーション クラスの標準です。</span><span class="sxs-lookup"><span data-stu-id="8d8c6-176">The following code block types are standard for application classes:</span></span>

- <span data-ttu-id="8d8c6-177">*<strong><em>classDescription</em>* 申告ブロック</strong> – この申告ブロックには<strong>パブリック</strong>、<strong>プライベート</strong>、および<strong>拡張</strong>などのクラス モディファイアーが含まれます。</span><span class="sxs-lookup"><span data-stu-id="8d8c6-177">*<strong><em>classDescription</em>* declaration block</strong> – This declaration block contains class modifiers such as <strong>public</strong>, <strong>private</strong>, and <strong>extends</strong>.</span></span> <span data-ttu-id="8d8c6-178">これには、クラスから作成されたオブジェクトのフィールドのメンバーも含まれます。</span><span class="sxs-lookup"><span data-stu-id="8d8c6-178">It also contains the field members for objects that are constructed from the class.</span></span> <span data-ttu-id="8d8c6-179"><strong>this</strong> というキーワードを入力すると、IntelliSense にメンバーのリストを表示することができます。</span><span class="sxs-lookup"><span data-stu-id="8d8c6-179">When you type the keyword <strong>this</strong>, IntelliSense can show a list of the members.</span></span>
- <span data-ttu-id="8d8c6-180">*<strong><em>新規</em>* メソッド</strong> – このメソッドは、クラスのインスタンスを作成します。</span><span class="sxs-lookup"><span data-stu-id="8d8c6-180">*<strong><em>new</em>* method</strong> – This method creates an instance of the class.</span></span> <span data-ttu-id="8d8c6-181">コンストラクターは、<strong>新しい</strong>キーワードを使用することによってのみ呼び出すことができます。</span><span class="sxs-lookup"><span data-stu-id="8d8c6-181">The constructor can be called only by using the <strong>new</strong> keyword.</span></span> <span data-ttu-id="8d8c6-182">派生クラスは、<strong>super</strong> メソッドの参照を呼ぶことにとって、コントラクターの<strong>新しい</strong>メソッドを呼び出すことができます。</span><span class="sxs-lookup"><span data-stu-id="8d8c6-182">Derived classes can call the <strong>new</strong> method of their constructor by calling the <strong>super</strong> method reference.</span></span>
- <span data-ttu-id="8d8c6-183">*<strong><em>確定</em>* メソッド</strong> – このメソッドは、クラスのインスタンスを確定します。</span><span class="sxs-lookup"><span data-stu-id="8d8c6-183">*<strong><em>finalize</em>* method</strong> – This method finalizes an instance of the class.</span></span> <span data-ttu-id="8d8c6-184">このメソッドはデストラクター メソッドです。</span><span class="sxs-lookup"><span data-stu-id="8d8c6-184">This method is the destructor method.</span></span> <span data-ttu-id="8d8c6-185">ただし、規則のみのデストラクタです。</span><span class="sxs-lookup"><span data-stu-id="8d8c6-185">However, it's a destructor by convention only.</span></span> <span data-ttu-id="8d8c6-186">ガベージ コレクション中に <strong>finalize</strong> メソッドが自動的に呼び出されることはありません。</span><span class="sxs-lookup"><span data-stu-id="8d8c6-186">The system doesn't automatically call the <strong>finalize</strong> method during garbage collection.</span></span>

<span data-ttu-id="8d8c6-187">クラスの追加メソッドには、次のタイプがあります。</span><span class="sxs-lookup"><span data-stu-id="8d8c6-187">Additional methods for a class have the following types:</span></span>

-   <span data-ttu-id="8d8c6-188">インスタンス メソッド</span><span class="sxs-lookup"><span data-stu-id="8d8c6-188">Instance methods</span></span>
-   <span data-ttu-id="8d8c6-189">静的メソッド</span><span class="sxs-lookup"><span data-stu-id="8d8c6-189">Static methods</span></span>
-   <span data-ttu-id="8d8c6-190">主要メソッド</span><span class="sxs-lookup"><span data-stu-id="8d8c6-190">Main methods</span></span>

<span data-ttu-id="8d8c6-191">さまざまな種類の項目でメソッドを作成することができます。</span><span class="sxs-lookup"><span data-stu-id="8d8c6-191">Methods can be created on many kinds of items.</span></span> <span data-ttu-id="8d8c6-192">次にいくつか例を挙げます。</span><span class="sxs-lookup"><span data-stu-id="8d8c6-192">Here are some examples:</span></span>

-   <span data-ttu-id="8d8c6-193">クラス</span><span class="sxs-lookup"><span data-stu-id="8d8c6-193">Classes</span></span>
-   <span data-ttu-id="8d8c6-194">マップ</span><span class="sxs-lookup"><span data-stu-id="8d8c6-194">Maps</span></span>
-   <span data-ttu-id="8d8c6-195">ビュー</span><span class="sxs-lookup"><span data-stu-id="8d8c6-195">Views</span></span>
-   <span data-ttu-id="8d8c6-196">データ セット</span><span class="sxs-lookup"><span data-stu-id="8d8c6-196">Data Sets</span></span>
-   <span data-ttu-id="8d8c6-197">フォーム</span><span class="sxs-lookup"><span data-stu-id="8d8c6-197">Forms</span></span>
-   <span data-ttu-id="8d8c6-198">クエリ</span><span class="sxs-lookup"><span data-stu-id="8d8c6-198">Queries</span></span>

### <a name="instance-methods"></a><span data-ttu-id="8d8c6-199">インスタンス メソッド</span><span class="sxs-lookup"><span data-stu-id="8d8c6-199">Instance methods</span></span>

<span data-ttu-id="8d8c6-200">インスタンス メソッド、またはオブジェクト メソッドは、クラスから作成される各オブジェクトに埋め込まれます。</span><span class="sxs-lookup"><span data-stu-id="8d8c6-200">Instance methods, or object methods, are embedded in each object that is created from the class.</span></span> <span data-ttu-id="8d8c6-201">メソッドの使用前に、オブジェクトのインスタンスを作成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="8d8c6-201">You must instantiate the object before you can use the method.</span></span> <span data-ttu-id="8d8c6-202">後でインスタンス メソッドを静的メソッドに変換する場合は、クライアントを再起動する必要があります。</span><span class="sxs-lookup"><span data-stu-id="8d8c6-202">If you later convert an instance method to a static method, you must restart the client.</span></span> <span data-ttu-id="8d8c6-203">それ以外の場合、コンパイラは変更を検出しません。</span><span class="sxs-lookup"><span data-stu-id="8d8c6-203">Otherwise, the compiler doesn't detect the change.</span></span> <span data-ttu-id="8d8c6-204">インスタンス メソッドを静的メソッドに変換した後は、クラスのインスタンスからメソッドを呼び出すことができなくなります。</span><span class="sxs-lookup"><span data-stu-id="8d8c6-204">After you've converted an instance method to a static method, you can no longer call the method from the instance of the class.</span></span> <span data-ttu-id="8d8c6-205">代わりに、クラス自体からメソッドを呼び出す必要があります。</span><span class="sxs-lookup"><span data-stu-id="8d8c6-205">Instead, you must call the method from the class itself.</span></span> <span data-ttu-id="8d8c6-206">静的メソッドは、次のセクションで説明します。</span><span class="sxs-lookup"><span data-stu-id="8d8c6-206">Static methods are discussed in the next section.</span></span> <span data-ttu-id="8d8c6-207">インスタンス メソッドを呼び出すには、次の構文を使用します。</span><span class="sxs-lookup"><span data-stu-id="8d8c6-207">You use the following syntax to call instance methods.</span></span>

    ClassName objectHandleName = new ClassName();
    objectHandleName.methodName();

### <a name="static-methods"></a><span data-ttu-id="8d8c6-208">静的メソッド</span><span class="sxs-lookup"><span data-stu-id="8d8c6-208">Static methods</span></span>

<span data-ttu-id="8d8c6-209">*クラス メソッド*とも呼ばれる静的メソッドは、クラスに属しており、キーワード **static** を使用して作成されます。</span><span class="sxs-lookup"><span data-stu-id="8d8c6-209">Static methods, which are also known as *class methods*, belong to a class and are created by using the keyword **static**.</span></span> <span data-ttu-id="8d8c6-210">静的メソッドを使用する前に、オブジェクトのインスタンスを作成する必要はありません。</span><span class="sxs-lookup"><span data-stu-id="8d8c6-210">You don't have to instantiate an object before you use static methods.</span></span> <span data-ttu-id="8d8c6-211">静的メソッドは多くの場合、テーブルに格納されているデータを操作するために使用します。</span><span class="sxs-lookup"><span data-stu-id="8d8c6-211">Static methods are often used to work with data that is stored in tables.</span></span> <span data-ttu-id="8d8c6-212">メンバー変数は静的メソッドで使用できません。</span><span class="sxs-lookup"><span data-stu-id="8d8c6-212">Member variables can't be used in a static method.</span></span> <span data-ttu-id="8d8c6-213">静的メソッドを呼び出すには、次の構文を使用します。</span><span class="sxs-lookup"><span data-stu-id="8d8c6-213">You use the following syntax to call static methods.</span></span>

    ClassName::methodName();

### <a name="main-methods"></a><span data-ttu-id="8d8c6-214">主要メソッド</span><span class="sxs-lookup"><span data-stu-id="8d8c6-214">Main methods</span></span>

<span data-ttu-id="8d8c6-215">**メイン**メソッドは、メニュー オプションから直接実行されるクラス メソッドです。</span><span class="sxs-lookup"><span data-stu-id="8d8c6-215">A **main** method is a class method that is run directly from a menu option.</span></span> <span data-ttu-id="8d8c6-216">このメソッドでは、オブジェクトのインスタンスを作成してから、必要なメンバー メソッドを呼び出す必要があります。</span><span class="sxs-lookup"><span data-stu-id="8d8c6-216">The method should only create an instance of the object and then call the required member methods.</span></span> <span data-ttu-id="8d8c6-217">**\_args** パラメーターを使用して、メソッドにデータを転送できます。</span><span class="sxs-lookup"><span data-stu-id="8d8c6-217">The **\_args** parameter lets you transfer data to the method.</span></span>

    static void main (Args _args)
    {
        // Your code here.
    }

### <a name="declaration-of-methods"></a><span data-ttu-id="8d8c6-218">メソッドの宣言</span><span class="sxs-lookup"><span data-stu-id="8d8c6-218">Declaration of methods</span></span>

<span data-ttu-id="8d8c6-219">メソッドの宣言は、ヘッダーと本文で構成されます。</span><span class="sxs-lookup"><span data-stu-id="8d8c6-219">Method declarations consist of a header and a body.</span></span> <span data-ttu-id="8d8c6-220">メソッド ヘッダーは、メソッドの名前と戻り値の型、メソッド モディファイア、およびパラメーターを宣言します。</span><span class="sxs-lookup"><span data-stu-id="8d8c6-220">The method header declares the method's name and return type), the method modifiers, and parameters.</span></span> <span data-ttu-id="8d8c6-221">(戻り値の型が**無効**である可能性があります。) メソッド本体は、変数宣言、メソッド宣言、および明細書で構成されます。</span><span class="sxs-lookup"><span data-stu-id="8d8c6-221">(The return type might be **void**.) The method body consists of variable declarations, method declarations, and statements.</span></span>

### <a name="return-type"></a><span data-ttu-id="8d8c6-222">戻り値の型</span><span class="sxs-lookup"><span data-stu-id="8d8c6-222">Return type</span></span>

<span data-ttu-id="8d8c6-223">メソッドが何も返さない場合、**無効**キーワードを使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="8d8c6-223">If a method doesn't return anything, you must use the **void** keyword.</span></span> <span data-ttu-id="8d8c6-224">次の例は、2 つのメソッドを示しています。</span><span class="sxs-lookup"><span data-stu-id="8d8c6-224">The following example shows two methods.</span></span> <span data-ttu-id="8d8c6-225">1 つの方法に戻り値の型がありますが、他の方法には戻り値の型がありません。</span><span class="sxs-lookup"><span data-stu-id="8d8c6-225">One method has a return type, but the other method doesn't have a return type.</span></span>

    void methodNameNoReturnValue()
    {
        // Your code here.
    }

    // If a method returns something, you must specify the return type and include a return statement.
    int methodNameIntegerReturnValue()
    {
        return 1;
    }

### <a name="syntax"></a><span data-ttu-id="8d8c6-226">構文</span><span class="sxs-lookup"><span data-stu-id="8d8c6-226">Syntax</span></span>

<span data-ttu-id="8d8c6-227">メソッドの宣言 = *ヘッダー*  *本文*ヘッダー = **\[** *モディファイアー* **\]**  *ReturnType*  *MethodName*  **(**  *ParameterList*  **)** モディファイアー = **\[クライアント\] \[サーバー\] \[edit | display | public | protected | private\] \[static | abstract | final \]** ReturnType = *Datatype*  **| void | anytype** MethodName = *識別子* ParameterList = **\[** *パラメーター*  **{ ,**  *パラメーター*  **}\]** パラメーター = *Datatype*  *Variableidentifier*  **\[ =**  *式*  **\]** 本文 = **{\[**  *VariableDeclarations*  **\] \[** *EmbeddedFunctionDeclarations*  **\] \[**  *ステートメント*  **\] }** EmbeddedFunctionDeclaration = *ヘッダー*  **{\[**  *VariableDeclarations*  **\] \[** *ステートメント*  **\]}** **anytype** の戻り値の型を使用した場合、メソッドはあらゆるデータ型を返すことができます。</span><span class="sxs-lookup"><span data-stu-id="8d8c6-227">Method declaration = *Heading*  *Body* Heading = **\[** *Modifiers* **\]**  *ReturnType*  *MethodName*  **(**  *ParameterList*  **)** Modifiers = **\[client\] \[server\] \[edit | display | public | protected | private\] \[static | abstract | final \]** ReturnType = *Datatype*  **| void | anytype** MethodName = *Identifier* ParameterList = **\[** *Parameter*  **{ ,**  *Parameter*  **}\]** Parameter = *Datatype*  *Variableidentifier*  **\[ =**  *Expression*  **\]** Body = **{ \[**  *VariableDeclarations*  **\] \[**  *EmbeddedFunctionDeclarations*  **\] \[**  *Statements*  **\] }** EmbeddedFunctionDeclaration = *Heading*  **{\[**  *VariableDeclarations*  **\] \[**  *Statements*  **\]}** If you use the **anytype** return type, the method can return any data type.</span></span>

### <a name="example-of-a-method-that-doesnt-have-a-return-type"></a><span data-ttu-id="8d8c6-228">戻り値の型を設定していないメソッドの例</span><span class="sxs-lookup"><span data-stu-id="8d8c6-228">Example of a method that doesn't have a return type</span></span>

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

### <a name="example-of-a-method-that-has-parameters"></a><span data-ttu-id="8d8c6-229">パラメーターを持つメソッドの例</span><span class="sxs-lookup"><span data-stu-id="8d8c6-229">Example of a method that has parameters</span></span>

<span data-ttu-id="8d8c6-230">次の例では、**checkAccountBlocked** メソッドはブール値を返し、**amountCur** パラメーターで動作します。</span><span class="sxs-lookup"><span data-stu-id="8d8c6-230">In the following example, the **checkAccountBlocked** method returns a Boolean value and acts on the **amountCur** parameter.</span></span>

    boolean checkAccountBlocked(AmountCur amountCur)
    {
        if (this.blocked == CustVendorBlocked::All 
            ||(this.blocked == CustVendorBlocked::Invoice 
            && amountCur > 0 ))
        return checkFailed(strFmt("@SYS7987",this.accountNum));
        return true;
    }

## <a name="method-modifiers"></a><span data-ttu-id="8d8c6-231">メソッド modifiers</span><span class="sxs-lookup"><span data-stu-id="8d8c6-231">Method modifiers</span></span>
<span data-ttu-id="8d8c6-232">いくつかのモディファイアーは、メソッドの宣言に適用することができます。</span><span class="sxs-lookup"><span data-stu-id="8d8c6-232">Several modifiers can be applied to method declarations.</span></span> <span data-ttu-id="8d8c6-233">一部の修飾子を結合できます (たとえば、**final static**)。</span><span class="sxs-lookup"><span data-stu-id="8d8c6-233">Some of the modifiers can be combined (for example, **final static**).</span></span> <span data-ttu-id="8d8c6-234">メソッド モディファイア キーワードを次に示します。</span><span class="sxs-lookup"><span data-stu-id="8d8c6-234">Here are the method modifier keywords:</span></span>

-   <span data-ttu-id="8d8c6-235">**抽象** – メソッドは宣言されていますが、親クラスで実装されていません。</span><span class="sxs-lookup"><span data-stu-id="8d8c6-235">**abstract** – The method is declared but isn't implemented in a parent class.</span></span> <span data-ttu-id="8d8c6-236">このメソッドはサブクラスで上書きする必要があります。</span><span class="sxs-lookup"><span data-stu-id="8d8c6-236">The method must be overridden in subclasses.</span></span> <span data-ttu-id="8d8c6-237">サブクラスに親クラスに属する 1 つ以上の抽象メソッドがあり、オーバーライドされていません。そのサブクラスからオブジェクトを作成しようとすると、コンパイラ エラーが発生します。</span><span class="sxs-lookup"><span data-stu-id="8d8c6-237">If you try to create an object from a subclass where one or more abstract methods that belong to the parent class haven't been overridden, you receive a compiler error.</span></span> <span data-ttu-id="8d8c6-238">クラスは抽象クラスにすることもできます。</span><span class="sxs-lookup"><span data-stu-id="8d8c6-238">Classes can also be abstract.</span></span> <span data-ttu-id="8d8c6-239">場合によっては、抽象的な概念を表す場合でもクラスをインスタンス化しないでください。</span><span class="sxs-lookup"><span data-stu-id="8d8c6-239">Sometimes, a class should not be instantiated even though it represents an abstract concept.</span></span> <span data-ttu-id="8d8c6-240">サブクラスのみインスタンスを作成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="8d8c6-240">Only subclasses should be instantiated.</span></span> <span data-ttu-id="8d8c6-241">このタイプの基本クラスは**抽象**として宣言できます。</span><span class="sxs-lookup"><span data-stu-id="8d8c6-241">Base classes of this type can be declared as **abstract**.</span></span> <span data-ttu-id="8d8c6-242">たとえば、勘定の概念をモデル化します。</span><span class="sxs-lookup"><span data-stu-id="8d8c6-242">For example, you want to model the concept of an account.</span></span> <span data-ttu-id="8d8c6-243">実際の世界には派生クラス (勘定科目など) しか存在しないため、勘定は抽象です。</span><span class="sxs-lookup"><span data-stu-id="8d8c6-243">Accounts are abstract, because only derived classes (ledger accounts and so on) exist in the real world.</span></span> <span data-ttu-id="8d8c6-244">この例では、**勘定** クラスを**抽象**として宣言する必要があるという明確なケースについて説明します。</span><span class="sxs-lookup"><span data-stu-id="8d8c6-244">This examples describes a clear case where you should declare the **Account** class as **abstract**.</span></span>
-   <span data-ttu-id="8d8c6-245">**ディスプレイ** – メソッドの戻り値は、ページまたはレポートに表示される必要があります。</span><span class="sxs-lookup"><span data-stu-id="8d8c6-245">**display** – The method's return value should be shown on a page or a report.</span></span> <span data-ttu-id="8d8c6-246">ページまたはレポートで値を変更することはできません。</span><span class="sxs-lookup"><span data-stu-id="8d8c6-246">The value can't be modified on the page or report.</span></span> <span data-ttu-id="8d8c6-247">通常、戻り値は合計などの計算された値です。</span><span class="sxs-lookup"><span data-stu-id="8d8c6-247">Typically, the return value is a calculated value, such as a sum.</span></span>
-   <span data-ttu-id="8d8c6-248">**編集** – メソッドの戻り値のタイプは、ページで使用されるフィールドの情報を提供するために使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="8d8c6-248">**edit** – The method's return type should be used to provide information for a field that is used on a page.</span></span> <span data-ttu-id="8d8c6-249">このフィールドの値は修正できます。</span><span class="sxs-lookup"><span data-stu-id="8d8c6-249">The value in the field can be modified.</span></span>
-   <span data-ttu-id="8d8c6-250">**最終** – 同じクラスから派生したクラスのメソッドに上書きすることはできません。</span><span class="sxs-lookup"><span data-stu-id="8d8c6-250">**final** – The method can't be overridden in any class that derives from its class.</span></span>
-   <span data-ttu-id="8d8c6-251">**パブリック** – **パブリック**として宣言されるメソッドは、クラスがアクセスできるどの場所にもアクセスでき、サブクラスによって上書きすることができます。</span><span class="sxs-lookup"><span data-stu-id="8d8c6-251">**public** – Methods that are declared as **public** can be accessed anywhere that the class is accessible, and they can be overridden by subclasses.</span></span> <span data-ttu-id="8d8c6-252">アクセス修飾子を持たないメソッドは暗黙的にパブリックとなります。</span><span class="sxs-lookup"><span data-stu-id="8d8c6-252">Methods that have no access modifier are implicitly public.</span></span>
-   <span data-ttu-id="8d8c6-253">**保護されている** – **保護されている**として宣言されるメソッドは、クラスおよびメソッドが宣言されている拡張されたクラスであるサブクラスの中のメソッドからのみ呼び出すことができます。</span><span class="sxs-lookup"><span data-stu-id="8d8c6-253">**protected** – Methods that are declared as **protected** can be called only from methods in the class and in subclasses that extend the class where the method is declared.</span></span>
-   <span data-ttu-id="8d8c6-254">**プライベート** – **プライベート**として宣言されるメソッドは、プライベートメソッドが宣言されているクラスのメソッドからのみ呼び出すことができます。</span><span class="sxs-lookup"><span data-stu-id="8d8c6-254">**private** – Methods that are declared as **private** can be called only from methods in the class where the private method is declared.</span></span>
-   <span data-ttu-id="8d8c6-255">**静的** – このメソッドはクラス メソッドであり、インスタンスを実行しません。</span><span class="sxs-lookup"><span data-stu-id="8d8c6-255">**static** – The method is a class method and doesn't act on an instance.</span></span> <span data-ttu-id="8d8c6-256">静的メソッドは、インスタンス変数を参照できません。</span><span class="sxs-lookup"><span data-stu-id="8d8c6-256">Static methods can't refer to instance variables.</span></span> <span data-ttu-id="8d8c6-257">クラスのインスタンスでは呼び出されません。</span><span class="sxs-lookup"><span data-stu-id="8d8c6-257">They aren't invoked on an instance of the class.</span></span> <span data-ttu-id="8d8c6-258">代わりに、クラス名を使用して呼び出されます (たとえば、**MyClass::aStaticProcedure()**)。</span><span class="sxs-lookup"><span data-stu-id="8d8c6-258">Instead, they are invoked by using the class name (for example, **MyClass::aStaticProcedure()**).</span></span>

### <a name="methods-that-have-modifiers"></a><span data-ttu-id="8d8c6-259">モディファイアーのあるメソッド</span><span class="sxs-lookup"><span data-stu-id="8d8c6-259">Methods that have modifiers</span></span>

<span data-ttu-id="8d8c6-260">**注記:** 次の例は、メソッド ヘッダーのみを示しています。</span><span class="sxs-lookup"><span data-stu-id="8d8c6-260">**Note:** The following examples show only the method headers.</span></span>

    // A method that cannot be overridden
    final int dontAlterMe() 

    // A static method 
    static void noChange()

    // A display method that returns an integer
    display int value()

## <a name="static-class-members"></a><span data-ttu-id="8d8c6-261">静的クラス メンバー</span><span class="sxs-lookup"><span data-stu-id="8d8c6-261">Static class members</span></span>
<span data-ttu-id="8d8c6-262">静的クラス メンバーを宣言するには、**静的** キーワードを使用します。</span><span class="sxs-lookup"><span data-stu-id="8d8c6-262">You declare static class members by using the **static** keyword.</span></span> <span data-ttu-id="8d8c6-263">**static** キーワードは、**new** を呼び出す回数に関係なく、メソッドの 1 つのインスタンスだけを作成するようシステムに指示します。</span><span class="sxs-lookup"><span data-stu-id="8d8c6-263">The **static** keyword instructs the system to create only one instance of the method, regardless of the number of times that you call **new**.</span></span> <span data-ttu-id="8d8c6-264">この 1 つのインスタンスは、セッション全体で使用されます。</span><span class="sxs-lookup"><span data-stu-id="8d8c6-264">This one instance is used throughout your session.</span></span> <span data-ttu-id="8d8c6-265">一般に、静的メソッドは次の基準を満たしている場合を意図しています。</span><span class="sxs-lookup"><span data-stu-id="8d8c6-265">In general, static methods are intended for cases where the following criteria are met:</span></span>

-   <span data-ttu-id="8d8c6-266">このメソッドは、クラス内で宣言されているメンバー変数にアクセスする必要はありません。</span><span class="sxs-lookup"><span data-stu-id="8d8c6-266">The method has no reason to access the member variables that are declared in the class.</span></span>
-   <span data-ttu-id="8d8c6-267">このメソッドは、クラスのインスタンス (静的でない) メソッドを呼び出す理由はありません。</span><span class="sxs-lookup"><span data-stu-id="8d8c6-267">The method has no reason to call any instance (non-static) methods of the class.</span></span>

#### <a name="static-methods"></a><span data-ttu-id="8d8c6-268">静的メソッド</span><span class="sxs-lookup"><span data-stu-id="8d8c6-268">Static methods</span></span>

<span data-ttu-id="8d8c6-269">このセクションでは、違法コピーを防止するためにソフトウェア キー タイプを使用するシナリオについて説明します。</span><span class="sxs-lookup"><span data-stu-id="8d8c6-269">This section describes a scenario where a software key type is used to help prevent piracy.</span></span> <span data-ttu-id="8d8c6-270">ソフトウェア キーの各インスタンスには、固有の値を持つことが可能です。</span><span class="sxs-lookup"><span data-stu-id="8d8c6-270">Each instance of a software key can have its own unique value.</span></span> <span data-ttu-id="8d8c6-271">ただし、すべてのソフトウェア キーはソフトウェア キー設計のルールに準拠する必要があるため、ソフトウェア キーへの適合をテストするロジックはすべてのソフトウェア キーに対して同じです。</span><span class="sxs-lookup"><span data-stu-id="8d8c6-271">However, because all software keys must conform to the rules of software key design, the logic that tests for software key conformance is the same for all software keys.</span></span> <span data-ttu-id="8d8c6-272">したがって、適合性検証ロジックを含むメソッドは静的でなければなりません。</span><span class="sxs-lookup"><span data-stu-id="8d8c6-272">Therefore, the method that contains the conformance validation logic should be static.</span></span> <span data-ttu-id="8d8c6-273">**静的**キーワード使用して宣言されるメソッドの例を次に示します。</span><span class="sxs-lookup"><span data-stu-id="8d8c6-273">Here is an example of a method that is declared by using the **static** keyword.</span></span>

    static public boolean validateSoftwareKey(str _softwareKeyString)
    {
          // Your code here.
    }

<span data-ttu-id="8d8c6-274">次の例では、クラスで静的メソッドを呼び出す前に **SoftwareKey** クラスのインスタンスを構築する必要はありません。</span><span class="sxs-lookup"><span data-stu-id="8d8c6-274">In the following example, you don't have to construct an instance of the **SoftwareKey** class before you call a static method on the class.</span></span> <span data-ttu-id="8d8c6-275">静的な **validateSoftwareKey** メソッドを呼び出すときは、構文はそのメソッドを含むクラスの名前で始まります。</span><span class="sxs-lookup"><span data-stu-id="8d8c6-275">When you want to call the static **validateSoftwareKey** method, the syntax starts with the name of the class that contains the method.</span></span> <span data-ttu-id="8d8c6-276">コロンのペア (::) は、クラス名を静的メソッド名に接続するために使用します。</span><span class="sxs-lookup"><span data-stu-id="8d8c6-276">A pair of colons (::) is used to connect the class name to the static method name.</span></span>

    boolean yourBool = SoftwareKey::validateSoftwareKey(yourSoftwareKeyString);

#### <a name="static-fields"></a><span data-ttu-id="8d8c6-277">静的フィールド</span><span class="sxs-lookup"><span data-stu-id="8d8c6-277">Static fields</span></span>

<span data-ttu-id="8d8c6-278">静的フィールドは**静的**キーワードを使用して宣言されているフィールドです。</span><span class="sxs-lookup"><span data-stu-id="8d8c6-278">Static fields are fields that are declared by using the **static** keyword.</span></span> <span data-ttu-id="8d8c6-279">概念的には、クラスに適用され、クラスのインスタンスには適用されません。</span><span class="sxs-lookup"><span data-stu-id="8d8c6-279">Conceptually, they apply to the class, not to instances of the class.</span></span>

### <a name="static-constructors"></a><span data-ttu-id="8d8c6-280">静的コンストラクター</span><span class="sxs-lookup"><span data-stu-id="8d8c6-280">Static constructors</span></span>

<span data-ttu-id="8d8c6-281">静的コンストラクターは、静的またはインスタンス呼び出しがクラスに対して行われる前に実行されることが保証されます。</span><span class="sxs-lookup"><span data-stu-id="8d8c6-281">Static constructors are guaranteed to run before any static or instance calls are made to the class.</span></span> <span data-ttu-id="8d8c6-282">C\# では、*静的*の概念が実行中のアプリケーション ドメイン全体に関係します。</span><span class="sxs-lookup"><span data-stu-id="8d8c6-282">In C\#, the *static* concept is related to the whole executing application domain.</span></span> <span data-ttu-id="8d8c6-283">ただし、X++ では、静的コンストラクターの実行は、ユーザーのセッションに対して相対的です。</span><span class="sxs-lookup"><span data-stu-id="8d8c6-283">However, in X++, the execution of the static constructor is relative to the user’s session.</span></span> <span data-ttu-id="8d8c6-284">静的コンストラクターには、次の構文があります。</span><span class="sxs-lookup"><span data-stu-id="8d8c6-284">The static constructor has the following syntax.</span></span>

    static void TypeNew() 

<span data-ttu-id="8d8c6-285">静的コンストラクターは明示的に呼び出さないでください。</span><span class="sxs-lookup"><span data-stu-id="8d8c6-285">You never explicitly call the static constructor.</span></span> <span data-ttu-id="8d8c6-286">コンパイラは、コンストラクターがクラスの他のメソッドの前に正確に 1 回呼び出されるようにするコードを生成します。</span><span class="sxs-lookup"><span data-stu-id="8d8c6-286">The compiler will generate code to make sure that the constructor is called exactly one time before any other method on the class.</span></span> <span data-ttu-id="8d8c6-287">静的コンストラクターは、任意の静的データを初期化したり、一度だけ実行する必要のある特定のアクションを実行するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="8d8c6-287">A static constructor is used to initialize any static data or perform a particular action that must be performed only one time.</span></span> <span data-ttu-id="8d8c6-288">静的コンストラクターに指定できるパラメーターはなく、**静的**としてマークする必要があります。</span><span class="sxs-lookup"><span data-stu-id="8d8c6-288">No parameters can be provided for the static constructor, and it must be marked as **static**.</span></span> <span data-ttu-id="8d8c6-289">次の例は、静的コンストラクターを使用して単一のインスタンスを作成する方法を示しています。</span><span class="sxs-lookup"><span data-stu-id="8d8c6-289">The following example shows how to create a singleton instance by using a static constructor.</span></span>

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

<span data-ttu-id="8d8c6-290">単一は、クラスのインスタンスが 1 つしか呼び出されないことを保証します。</span><span class="sxs-lookup"><span data-stu-id="8d8c6-290">The singleton guarantees that only one instance of the class will ever be called.</span></span> <span data-ttu-id="8d8c6-291">次の例は、単一をインスタンス化する方法を示しています。</span><span class="sxs-lookup"><span data-stu-id="8d8c6-291">The following example shows how to instantiate the singleton.</span></span>

    {
        Singleton i = Singleton::Instance();
    }

## <a name="method-access-control"></a><span data-ttu-id="8d8c6-292">メソッド アクセス制御</span><span class="sxs-lookup"><span data-stu-id="8d8c6-292">Method access control</span></span>
<span data-ttu-id="8d8c6-293">その他のクラスのメソッドがお客様のクラスのメソッドを呼び出すことができるかどうかを制御するには、アクセサー キーワード **public**、**protected**、および **private** を使用します。</span><span class="sxs-lookup"><span data-stu-id="8d8c6-293">You use the accessor keywords **public**, **protected**, and **private** to control whether the methods in other classes can call the methods on your class.</span></span> <span data-ttu-id="8d8c6-294">メソッドのアクセス キーワードは、クラス継承のルールとも連携します。</span><span class="sxs-lookup"><span data-stu-id="8d8c6-294">The accessor keywords on methods also interact with the rules for class inheritance.</span></span> <span data-ttu-id="8d8c6-295">メソッドを使用するアクセサー キーワードを次に示します。</span><span class="sxs-lookup"><span data-stu-id="8d8c6-295">Here are the accessor keywords that you use with methods:</span></span>

-   <span data-ttu-id="8d8c6-296">**パブリック** – **パブリック**として宣言されるメソッドは、クラスがアクセスできるどの場所からでも呼び出すことができます。</span><span class="sxs-lookup"><span data-stu-id="8d8c6-296">**public** – Methods that are declared as **public** can be called from anywhere that the class is accessible.</span></span> <span data-ttu-id="8d8c6-297">さらに、メソッドが**最終**として宣言されていない限り、パブリック メソッドをサブクラスでオーバーライドできます。</span><span class="sxs-lookup"><span data-stu-id="8d8c6-297">In addition, a public method can be overridden by a subclass, unless the method is declared as **final**.</span></span>
-   <span data-ttu-id="8d8c6-298">**保護されている** – **保護されている**として宣言されるメソッドは、次のメソッドからのみ呼び出すことができます。</span><span class="sxs-lookup"><span data-stu-id="8d8c6-298">**protected** – Methods that are declared as **protected** can be called only from the following methods:</span></span>
    -   <span data-ttu-id="8d8c6-299">クラスのメソッド。</span><span class="sxs-lookup"><span data-stu-id="8d8c6-299">Methods in the class.</span></span>
    -   <span data-ttu-id="8d8c6-300">保護されたメソッドを含むクラスのサブクラス内のメソッド。</span><span class="sxs-lookup"><span data-stu-id="8d8c6-300">Methods in a subclass of the class that contains the protected method.</span></span> <span data-ttu-id="8d8c6-301">保護されているメソッドは、サブクラスで上書きできます。</span><span class="sxs-lookup"><span data-stu-id="8d8c6-301">Methods that are protected can be overridden in subclasses.</span></span>
-   <span data-ttu-id="8d8c6-302">**プライベート** – **プライベート**として宣言されるメソッドは、プライベートメソッドが宣言されているクラスのメソッドからのみ呼び出すことができます。</span><span class="sxs-lookup"><span data-stu-id="8d8c6-302">**private** – Methods that are declared as **private** can be called only from methods in the class where the private method is declared.</span></span> <span data-ttu-id="8d8c6-303">サブクラスでプライベート メソッドをオーバーライドできません。</span><span class="sxs-lookup"><span data-stu-id="8d8c6-303">No private method can be overridden in a subclass.</span></span> <span data-ttu-id="8d8c6-304">既定では、新しいメソッドを作成するときに、**プライベート** アクセサー キーワードがコード エディターに表示されます。</span><span class="sxs-lookup"><span data-stu-id="8d8c6-304">By default, when you create a new method, the **private** accessor keyword appears in the code editor.</span></span> <span data-ttu-id="8d8c6-305">最大限のセキュリティについては、**プライベート**が最も保守的な既定のアクセス キーワードです。</span><span class="sxs-lookup"><span data-stu-id="8d8c6-305">For maximum security, **private** is the most conservative default accessor keyword.</span></span>

### <a name="static-and-instance-methods"></a><span data-ttu-id="8d8c6-306">静的およびインスタンス メソッド</span><span class="sxs-lookup"><span data-stu-id="8d8c6-306">Static and instance methods</span></span>

<span data-ttu-id="8d8c6-307">メソッドのアクセサー キーワードは、どのメソッドが静的であるか、静的でないかに関係なく、同じクラスにある 2 つのメソッド間の呼び出しを制限することはありません。</span><span class="sxs-lookup"><span data-stu-id="8d8c6-307">The accessor keywords on methods never restrict calls between two methods that are in the same class, regardless of which method is static or non-static.</span></span> <span data-ttu-id="8d8c6-308">静的メソッドでは、**新しい**コンストラクター メソッドが**プライベート** モディファイアーで修飾されている場合でも、**新しい**コンストラクター メソッドに対する呼び出しは有効です。</span><span class="sxs-lookup"><span data-stu-id="8d8c6-308">In a static method, calls to the **new** constructor method are valid even if the **new** constructor method is decorated with the **private** modifier.</span></span> <span data-ttu-id="8d8c6-309">これらの呼び出しの構文では、**新しい**キーワードを使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="8d8c6-309">The syntax for these calls requires that the **new** keyword be used.</span></span> <span data-ttu-id="8d8c6-310">静的メソッドのコードは、クラスのインスタンス メソッドを呼び出す前に、独自のクラスのインスタンス オブジェクトを構築する必要があります。</span><span class="sxs-lookup"><span data-stu-id="8d8c6-310">The code in a static method must construct an instance object of its own class before it can call any instance methods on the class.</span></span>

### <a name="increasing-access-during-overrides"></a><span data-ttu-id="8d8c6-311">オーバーライド中のアクセス増加</span><span class="sxs-lookup"><span data-stu-id="8d8c6-311">Increasing access during overrides</span></span>

<span data-ttu-id="8d8c6-312">サブクラス内でメソッドがオーバーライドされると、オーバーライドするメソッドは少なくともオーバーライドされるメソッドと同程度のアクセスが可能なことが必要です。</span><span class="sxs-lookup"><span data-stu-id="8d8c6-312">When a method is overridden in a subclass, the overriding method must be at least as accessible as the overridden method.</span></span> <span data-ttu-id="8d8c6-313">たとえば、次のコンパイラ ルールは、サブクラスで保護されたメソッドが上書きされる時に適用されます。</span><span class="sxs-lookup"><span data-stu-id="8d8c6-313">For example, the following compiler rules apply when a protected method is overridden in a subclass:</span></span>

-   <span data-ttu-id="8d8c6-314">スーパークラスのパブリック メソッドは、サブクラスのパブリック メソッドによってのみ上書きできます。</span><span class="sxs-lookup"><span data-stu-id="8d8c6-314">A public method in a superclass can be overridden only by a public method in the subclass.</span></span>
-   <span data-ttu-id="8d8c6-315">サブクラスでは、パブリック メソッドまたは保護対象のメソッドはスーパークラスの保護対象のメソッドをオーバーライドできません。</span><span class="sxs-lookup"><span data-stu-id="8d8c6-315">In a subclass, a public or protected method can override a protected method of the superclass.</span></span>
-   <span data-ttu-id="8d8c6-316">サブクラスでは、プライベート メソッドはスーパークラスの保護対象のメソッドをオーバーライドできません。</span><span class="sxs-lookup"><span data-stu-id="8d8c6-316">In a subclass, a private method can't override a protected method of the superclass.</span></span>

## <a name="optional-parameters"></a><span data-ttu-id="8d8c6-317">オプションのパラメーター</span><span class="sxs-lookup"><span data-stu-id="8d8c6-317">Optional parameters</span></span>
<span data-ttu-id="8d8c6-318">パラメーターは、メソッド宣言で初期化することができます。</span><span class="sxs-lookup"><span data-stu-id="8d8c6-318">Parameters can be initialized in the method declaration.</span></span> <span data-ttu-id="8d8c6-319">この場合、パラメーターは*オプションのパラメーター*となります。</span><span class="sxs-lookup"><span data-stu-id="8d8c6-319">In this case, the parameter becomes an *optional parameter*.</span></span> <span data-ttu-id="8d8c6-320">メソッドの呼び出しの値が指定されていない場合は、既定値が使用されます。</span><span class="sxs-lookup"><span data-stu-id="8d8c6-320">If no value is supplied in the method call, the default value is used.</span></span> <span data-ttu-id="8d8c6-321">すべての必須パラメータは最初のオプション パラメーターの前に一覧表示する必要があります。</span><span class="sxs-lookup"><span data-stu-id="8d8c6-321">All required parameters must be listed before the first optional parameter.</span></span> <span data-ttu-id="8d8c6-322">次の例では、オプションのパラメーターを持つメソッドを作成して呼び出す方法を示しています。</span><span class="sxs-lookup"><span data-stu-id="8d8c6-322">The following examples show how to create and call a method that has optional parameters.</span></span> <span data-ttu-id="8d8c6-323">**AddThreeInts** メソッドの例は、メソッドを呼び出すときにデフォルトのパラメーターをスキップできないことを示しています。</span><span class="sxs-lookup"><span data-stu-id="8d8c6-323">The example of the **AddThreeInts** method shows that you can't skip default parameters when you call a method.</span></span>

### <a name="examples-of-optional-parameters"></a><span data-ttu-id="8d8c6-324">オプション パラメーターの例</span><span class="sxs-lookup"><span data-stu-id="8d8c6-324">Examples of optional parameters</span></span>

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

        // The CalculateAgeAsOfDate method references
        // the birthDate field, is called by the Main method, and has an 
        // optional parameter. In this example, the default value is the
        // return value of a function. 
        public real CalculateAgeAsOfDate(date _calcToDate = DateTimeUtil::getToday(DateTimeUtil::getUserPreferredTimeZone()) )  
        {
            return (_calcToDate - birthDate) / 365;
        }

        // The Main method calls the CalculateAgeAsOfDate method twice. 
        static public void Main(Args _args)
        {
            Person mc = new Person(13\5\2010);   // birthDate is initialized.
            // Optional parameter's default is used.
            print( "Age in years: " + num2str(mc.CalculateAgeAsOfDate(),2,0,0,0));
            // January 2, 2044  is the parameter value for _date.
            print "Age in years: " + num2str(mc.CalculateAgeAsOfDate(2\1\2044),2,0,0,0);
        }
    }

    // This is an example of how you cannot skip to a second optional parameter. 
    // The first method has two optional parameters. The second method is a caller 
    // of the first method. The caller wants to override only the _i3 default value, but the 
    // compiler requires that all prior optional parameters also 
    // be overridden in the call. 
    public class Additions {
        static public int AddThreeInts(int _i1, int _i2 = 2,int _i3 = 3)
        {
            return _i1 + _i2 + _i3;
        }
    }

    // The second method has a commented section showing the
    // failed attempt to accept the default of the first optional 
    // parameter (_i2) while trying to override the final optional 
    // parameter (_i3).
    static public void Main(Args _args)
    { 
        // No way to skip the first optional parameter (so it can default)
        // while also specifying the value of the second optional parameter.
        // The next statement does not compile.
        //print Additions::AddThreeInts(1, , 99);

        // Settle for overriding both optional parameters.
        print Additions::AddThreeInts(1, 2, 99);
    }

## <a name="accessor-methods"></a><span data-ttu-id="8d8c6-325">アクセサー メソッド</span><span class="sxs-lookup"><span data-stu-id="8d8c6-325">Accessor methods</span></span>
<span data-ttu-id="8d8c6-326">クラス変数はプライベートです。</span><span class="sxs-lookup"><span data-stu-id="8d8c6-326">Class variables are private.</span></span> <span data-ttu-id="8d8c6-327">クラスの内部実装の詳細を非表示にすることで、そのクラスを使用するコードを破棄することなくクラスの実装を後で変更することができます。</span><span class="sxs-lookup"><span data-stu-id="8d8c6-327">By hiding details of the internal implementation of a class, you can change the implementation of the class later without breaking any code that uses that class.</span></span> <span data-ttu-id="8d8c6-328">参照変数からデータにアクセスするには、アクセサー メソッドを作成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="8d8c6-328">To access the data from reference variables, you must create accessor methods.</span></span> <span data-ttu-id="8d8c6-329">次の例では、アクセス メソッドを使用して変数 **x** および **y** にアクセスする **Point** クラスを定義します。</span><span class="sxs-lookup"><span data-stu-id="8d8c6-329">The following example defines a **Point** class that uses accessor methods to access the variables **x** and **y**.</span></span>

    class Point
    {
        // Instance variables
        real x; 
        real y;

        //Constructor to initialize to a specific or default value
        void new(real _x=10, real _y=10) 
        {
            x = _x;
            y = _y;
        }

        //Accessor methods
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

<span data-ttu-id="8d8c6-330">これらのメソッド宣言は、**Point** クラスが外部からの変数へのアクセスを提供する方法を示しています。</span><span class="sxs-lookup"><span data-stu-id="8d8c6-330">These method declarations show how the **Point** class provides access to its variables from the outside world.</span></span> <span data-ttu-id="8d8c6-331">その他のオブジェクトは、アクセサー メソッドを使ってインスタンス変数 **Point** オブジェクトを操作できます。</span><span class="sxs-lookup"><span data-stu-id="8d8c6-331">Other objects can manipulate the instance variables of **Point** objects by using the accessor methods.</span></span>

    // Declare a variable to refer to a Point object
    Point myPoint; 
    // Create a Point object
    myPoint = new Point(); 
    // Set the x variable using the accessor method
    myPoint.setX(10.0); 
    // Set the y variable by means of the accessor method
    myPoint.setY(25.7);

<span data-ttu-id="8d8c6-332">コール スタックの深さは 100 に制限されています。</span><span class="sxs-lookup"><span data-stu-id="8d8c6-332">The depth of the call stack is limited to 100.</span></span>

## <a name="overriding-a-method"></a><span data-ttu-id="8d8c6-333">メソッドのオーバーライド</span><span class="sxs-lookup"><span data-stu-id="8d8c6-333">Overriding a method</span></span>
<span data-ttu-id="8d8c6-334">クラス内のメソッドは、それを拡張するクラスによって継承されます。</span><span class="sxs-lookup"><span data-stu-id="8d8c6-334">The methods in a class are inherited by any class that extends it.</span></span> <span data-ttu-id="8d8c6-335">継承されたメソッドの機能を変更するには、サブクラスでメソッドを作成し、そのメソッドにスーパークラスのメソッドと同じ名前とパラメーターを指定します。</span><span class="sxs-lookup"><span data-stu-id="8d8c6-335">To change the functionality of an inherited method, you can create a method in the subclass, and then give that method the same name and parameters as the method in the superclass.</span></span> <span data-ttu-id="8d8c6-336">このプロセスは、メソッドを*オーバーライドする*として知られています。</span><span class="sxs-lookup"><span data-stu-id="8d8c6-336">This process is known as *overriding* the method.</span></span> <span data-ttu-id="8d8c6-337">次の例では、**ColorAttribute** は**属性**のサブクラスであるため、**methodAttr** メソッドを継承します。</span><span class="sxs-lookup"><span data-stu-id="8d8c6-337">In the following example, **ColorAttribute** is a subclass of **Attribute** and therefore inherits the **methodAttr** method.</span></span> <span data-ttu-id="8d8c6-338">ただし、**ColorAttribute** は同じ名前および同じ数の引数を持つメソッドを定義するため、スーパークラスのメソッドは上書きされます。</span><span class="sxs-lookup"><span data-stu-id="8d8c6-338">However, because **ColorAttribute** defines a method that has the same name and the same number of arguments, the method in the superclass is overridden.</span></span>

    // Superclass: Attribute
    public class Attribute
    {
        int objectVariable;

        void methodAtt()
        {
            //Some statements
        }
    }

    // Subclass: ColorAttribute
    public class ColorAttribute extends Attribute
    {
        int addedObjectVariable;

        void methodAtt()
        {
            //Some statements
        }
    }

### <a name="preventing-method-overrides"></a><span data-ttu-id="8d8c6-339">メソッドのオーバーライドを禁止する</span><span class="sxs-lookup"><span data-stu-id="8d8c6-339">Preventing method overrides</span></span>

<span data-ttu-id="8d8c6-340">静的メソッドは、クラスごとに存在するため上書きすることはできません。</span><span class="sxs-lookup"><span data-stu-id="8d8c6-340">Static methods can't be overridden, because they exist per class.</span></span> <span data-ttu-id="8d8c6-341">他の重要なメソッドやコア メソッドがオーバーライドされないようにするには、**final** 修飾子を使用します。</span><span class="sxs-lookup"><span data-stu-id="8d8c6-341">To protect other sensitive methods, or core methods, from being overridden, use the **final** modifier.</span></span> <span data-ttu-id="8d8c6-342">次の例では、**methodAtt** が **final** として宣言されているため、**属性**を拡張するクラスでオーバーライドできません</span><span class="sxs-lookup"><span data-stu-id="8d8c6-342">In the following example, because **methodAtt** is declared as **final**, it can't be overridden in any class that extends **Attribute**.</span></span> <span data-ttu-id="8d8c6-343">**最終** に **新規** または **確定** のメソッドを指定しないでください。</span><span class="sxs-lookup"><span data-stu-id="8d8c6-343">You should not specify **new** or **finalize** methods as **final**.</span></span> <span data-ttu-id="8d8c6-344">次の例は、**final** キーワードの使用方法を示しています。</span><span class="sxs-lookup"><span data-stu-id="8d8c6-344">The following example shows how to use the **final** keyword.</span></span>

    public class Attribute
    {
        int objectVariable;

        final void methodAtt()
        {
            //Some statements
        }
    }

### <a name="overriding-vs-overloading"></a><span data-ttu-id="8d8c6-345">オーバーライドとオーバーロード</span><span class="sxs-lookup"><span data-stu-id="8d8c6-345">Overriding vs. overloading</span></span>

<span data-ttu-id="8d8c6-346">オーバーライドは、メソッドのスーパークラスの実装がそのメソッドのサブクラスの実装によって変更されるが、両方のメソッドのシグネチャが同じ場合に行われます。</span><span class="sxs-lookup"><span data-stu-id="8d8c6-346">Overriding occurs when the superclass's implementation of a method is changed by the subclass's implementation of that method, but the signatures of both methods are the same.</span></span> <span data-ttu-id="8d8c6-347">対照的に、*オーバーロード*は複数のメソッドが同じ名前を持つ場合に発生しますが、メソッドは異なるシグネチャ (戻り値の型、パラメーター リスト、または両方) を持ちます。</span><span class="sxs-lookup"><span data-stu-id="8d8c6-347">By contrast, *overloading* occurs when more than one method has the same name, but the methods have different signatures (return types, parameter lists, or both).</span></span> <span data-ttu-id="8d8c6-348">X++ はオーバーライドをサポートしますが、オーバーロードはサポートしていません。</span><span class="sxs-lookup"><span data-stu-id="8d8c6-348">X++ supports overriding, but it doesn't support overloading.</span></span>

## <a name="parameters"></a><span data-ttu-id="8d8c6-349">パラメーター</span><span class="sxs-lookup"><span data-stu-id="8d8c6-349">Parameters</span></span>
<span data-ttu-id="8d8c6-350">すべてのメソッドは独自の*スコープ*を持っています。</span><span class="sxs-lookup"><span data-stu-id="8d8c6-350">All methods have their own *scope*.</span></span> <span data-ttu-id="8d8c6-351">メソッドは、1 つ以上のパラメーターを受け取ることができます。</span><span class="sxs-lookup"><span data-stu-id="8d8c6-351">A method can take one or more parameters.</span></span> <span data-ttu-id="8d8c6-352">メソッドのスコープ内では、これらのパラメーターはローカル変数として処理され、メソッド呼び出しのパラメーターからの値で初期化されます。</span><span class="sxs-lookup"><span data-stu-id="8d8c6-352">Within the scope of the method, these parameters are treated as local variables and are initialized with a value from the parameter in the method call.</span></span> <span data-ttu-id="8d8c6-353">すべてのパラメーターは値で渡されます。</span><span class="sxs-lookup"><span data-stu-id="8d8c6-353">All parameters are passed by value.</span></span> <span data-ttu-id="8d8c6-354">元の変数の値を変更することはできません。</span><span class="sxs-lookup"><span data-stu-id="8d8c6-354">You can't change the value of the original variable.</span></span> <span data-ttu-id="8d8c6-355">メソッド内のローカル変数のみを変更することができます。</span><span class="sxs-lookup"><span data-stu-id="8d8c6-355">You can change only the local variable in the method.</span></span> <span data-ttu-id="8d8c6-356">このローカル変数は元の変数のコピーです。</span><span class="sxs-lookup"><span data-stu-id="8d8c6-356">This local variable is a copy of the original variable.</span></span>

## <a name="scope-of-variables-in-methods"></a><span data-ttu-id="8d8c6-357">メソッドでの変数の範囲</span><span class="sxs-lookup"><span data-stu-id="8d8c6-357">Scope of variables in methods</span></span>
<span data-ttu-id="8d8c6-358">スコープは、品目にアクセスできるエリアを定義します。</span><span class="sxs-lookup"><span data-stu-id="8d8c6-358">A scope defines the area in which an item can be accessed.</span></span> <span data-ttu-id="8d8c6-359">クラスで定義されている変数は、そのクラス内のメソッドで使用できます。</span><span class="sxs-lookup"><span data-stu-id="8d8c6-359">Variables that are defined in a class are available to the methods within that class.</span></span> <span data-ttu-id="8d8c6-360">メソッド内の変数は、現在のブロック内でのみアクセスできます。</span><span class="sxs-lookup"><span data-stu-id="8d8c6-360">Variables in methods can be accessed only within the current block.</span></span>

## <a name="local-functions"></a><span data-ttu-id="8d8c6-361">ローカル関数</span><span class="sxs-lookup"><span data-stu-id="8d8c6-361">Local functions</span></span>
<span data-ttu-id="8d8c6-362">メソッド内部のローカル関数を宣言することができます。</span><span class="sxs-lookup"><span data-stu-id="8d8c6-362">You can declare local functions inside a method.</span></span> <span data-ttu-id="8d8c6-363">ただし、ベスト プラクティスとしては、メソッド内のローカル機能を追加する必要はありません。</span><span class="sxs-lookup"><span data-stu-id="8d8c6-363">However, as a best practice, you shouldn't add local functions inside the method.</span></span> <span data-ttu-id="8d8c6-364">代わりに、プライベート メソッドをクラスに追加する必要があります。</span><span class="sxs-lookup"><span data-stu-id="8d8c6-364">Instead, you should add private methods to the class.</span></span> <span data-ttu-id="8d8c6-365">次の例は、2 つのローカル関数、**localFunc55b** および **localFunc66c** の有効な宣言を示しています。</span><span class="sxs-lookup"><span data-stu-id="8d8c6-365">The following example shows valid declarations of two local functions, **localFunc55b** and **localFunc66c**.</span></span> <span data-ttu-id="8d8c6-366">ローカル関数への呼び出しは、必要に応じて、この例の関数宣言の後に行われます。</span><span class="sxs-lookup"><span data-stu-id="8d8c6-366">Calls to the local functions occur after the function declarations in the example, as is required.</span></span>

    static void G_LocalFuncJob2(Args _args) 
    {
        int nn = 654;
        void localFunc55b(int _iNum)  // The local function.
        {
            str sInnerString;
            sInnerString = "String_in_localFunc55b";
            info(strFmt("localFunc55b: %1 , %2 , %3", 
                _iNum, sInnerString, nn));
        }

        void localFunc66c()
        {
            info("Printing from inside localFunc66c.");
        }

        localFunc55b(55);
        localFunc66c();
        // Next print statement would fail to compile,
        // because sInnerString is restricted to the
        // scope of the local function in which it is declared.
        // print sInnerString; 
    }
    /***  Infolog window display:
    Message (07:38:54 pm)
    localFunc55b: 55 , String_in_localFunc55b , 654
    Printing from inside localFunc66c.
    ***/

### <a name="declaration-of-local-functions"></a><span data-ttu-id="8d8c6-367">ローカルの関数の宣言</span><span class="sxs-lookup"><span data-stu-id="8d8c6-367">Declaration of local functions</span></span>

-   <span data-ttu-id="8d8c6-368">ローカル関数の宣言は、メソッド内の宣言されていないステートメントの前に物理的に先行する必要があります。</span><span class="sxs-lookup"><span data-stu-id="8d8c6-368">The declarations of local functions must physically precede any non-declaration statements in the method.</span></span>
-   <span data-ttu-id="8d8c6-369">メソッド内で 1 つ以上のローカル関数を宣言することができます。</span><span class="sxs-lookup"><span data-stu-id="8d8c6-369">You can declare more than one local function in your method.</span></span> <span data-ttu-id="8d8c6-370">ただし、すべてのローカル関数は中断のないシリーズで宣言され、セットは 1 つのセミコロン (;) で終了する必要があります。</span><span class="sxs-lookup"><span data-stu-id="8d8c6-370">However, all local functions must be declared in an uninterrupted series, and the set must be terminated by one semicolon (;).</span></span>

### <a name="variable-scope"></a><span data-ttu-id="8d8c6-371">変数のスコープ</span><span class="sxs-lookup"><span data-stu-id="8d8c6-371">Variable scope</span></span>

-   <span data-ttu-id="8d8c6-372">ローカル関数内にあるコードは、ローカル関数を含むメソッドで宣言されている変数にアクセスできます。</span><span class="sxs-lookup"><span data-stu-id="8d8c6-372">Code that is inside the local function can access variables that are declared in the method that contains the local function.</span></span>
-   <span data-ttu-id="8d8c6-373">ローカル関数の外にあるコードは、ローカル関数で宣言された変数にアクセスすることはできません。</span><span class="sxs-lookup"><span data-stu-id="8d8c6-373">Code that is outside the local function can't access variables that are declared in the local function.</span></span>

### <a name="calls-to-local-functions"></a><span data-ttu-id="8d8c6-374">ローカルの関数への呼び出し</span><span class="sxs-lookup"><span data-stu-id="8d8c6-374">Calls to local functions</span></span>

-   <span data-ttu-id="8d8c6-375">ローカル関数は、ローカル関数が宣言されているのと同じメソッド内のコードによってのみ呼び出すことができます。</span><span class="sxs-lookup"><span data-stu-id="8d8c6-375">A local function can be called only by code in the same method where the local function is declared.</span></span>
-   <span data-ttu-id="8d8c6-376">ローカル関数が、それ自体を呼び出すことはありません。</span><span class="sxs-lookup"><span data-stu-id="8d8c6-376">A local function should never call itself.</span></span> <span data-ttu-id="8d8c6-377">このような再帰は、正常に行われるコンパイルを防ぐことができます。</span><span class="sxs-lookup"><span data-stu-id="8d8c6-377">Such recursion can prevent successful compilation.</span></span>

## <a name="the-this-keyword"></a><span data-ttu-id="8d8c6-378">このキーワード</span><span class="sxs-lookup"><span data-stu-id="8d8c6-378">The this keyword</span></span>
<span data-ttu-id="8d8c6-379">**this** キーワードは、**this** キーワードが使用されるクラスやテーブルのインスタンスへの参照です。</span><span class="sxs-lookup"><span data-stu-id="8d8c6-379">The **this** keyword is a reference to the instance of the class or table where the **this** keyword is used.</span></span> <span data-ttu-id="8d8c6-380">**this** 参照が必須になることはありませんが、コードを明確にし、コード エディターで IntelliSense の動作を強化することができます。</span><span class="sxs-lookup"><span data-stu-id="8d8c6-380">The **this** reference is never required, but it can clarify your code and enhances the behavior of IntelliSense in the code editor.</span></span> <span data-ttu-id="8d8c6-381">すべての呼び出しインスタンス メソッドは**これ**を参照または変数のいずれかにより修飾される必要があります。</span><span class="sxs-lookup"><span data-stu-id="8d8c6-381">All calls to instance methods must be qualified by either the **this** reference or a variable.</span></span> <span data-ttu-id="8d8c6-382">**this** 参照は、次の情報を修飾するために使用できます。</span><span class="sxs-lookup"><span data-stu-id="8d8c6-382">The **this** reference can be used to qualify the following information:</span></span>

-   <span data-ttu-id="8d8c6-383">**this** 参照が使用されている同じクラス内の他のインスタンス (静的でない) メソッドの名前。</span><span class="sxs-lookup"><span data-stu-id="8d8c6-383">The names of other instance (non-static) methods in the same class where the **this** reference is used.</span></span> <span data-ttu-id="8d8c6-384">次に例を示します: **boolColorChanged = this.colorItOrange();**</span><span class="sxs-lookup"><span data-stu-id="8d8c6-384">Here is an example: **boolColorChanged = this.colorItOrange();**</span></span>
-   <span data-ttu-id="8d8c6-385">**this** オブジェクトによって継承されるメソッドの名前。</span><span class="sxs-lookup"><span data-stu-id="8d8c6-385">The names of methods that are inherited by the **this** object.</span></span>
-   <span data-ttu-id="8d8c6-386">**this** キーワードが使用されるメソッドを含むテーブル上のフィールドの名前。</span><span class="sxs-lookup"><span data-stu-id="8d8c6-386">The names of fields on the table that contains the method that the **this** keyword is used in.</span></span>

<span data-ttu-id="8d8c6-387">**this** 参照は、次の方法で使用できません。</span><span class="sxs-lookup"><span data-stu-id="8d8c6-387">The **this** reference can't be used in the following ways:</span></span>

-   <span data-ttu-id="8d8c6-388">**classDeclaration** コードで宣言されているメンバー変数の名前を限定することはできません。</span><span class="sxs-lookup"><span data-stu-id="8d8c6-388">It can't qualify the names of member variables that are declared in the **classDeclaration** code.</span></span>
-   <span data-ttu-id="8d8c6-389">静的メソッドで使用できません。</span><span class="sxs-lookup"><span data-stu-id="8d8c6-389">It can't be used in a static method.</span></span>
-   <span data-ttu-id="8d8c6-390">クラスやテーブルの静的メソッドの名前を限定することはできません。</span><span class="sxs-lookup"><span data-stu-id="8d8c6-390">It can't qualify the names of static methods of the class or table.</span></span>

## <a name="interfaces"></a><span data-ttu-id="8d8c6-391">インターフェイス</span><span class="sxs-lookup"><span data-stu-id="8d8c6-391">Interfaces</span></span>
<span data-ttu-id="8d8c6-392"><em>インターフェイス</em>はパブリック インスタンス メソッドのセットを指定します。</span><span class="sxs-lookup"><span data-stu-id="8d8c6-392">An <em>interface</em> is a specification for a set of public instance methods.</span></span> <span data-ttu-id="8d8c6-393">他から 1 つのクラスを派生させることなく、インターフェイスは無関係なクラス間の類似点を定義し適用します。</span><span class="sxs-lookup"><span data-stu-id="8d8c6-393">An interface defines and enforces similarities between unrelated classes without having to derive one class from the other.</span></span> <span data-ttu-id="8d8c6-394">*<strong><em>*</em>classDeclaration</strong> コード内の<strong>インターフェイス キーワード*<em>の前に</em></strong><strong>パブリック</strong> キーワード*を明示的に追加しなくても、すべてのインターフェイスはパブリックです。</span><span class="sxs-lookup"><span data-stu-id="8d8c6-394">All interfaces are public, even if you don't explicitly add the <strong>public</strong> keyword \*<strong><em>in front of the \*</em>interface</strong> keyword \*<strong><em>in the \*</em>classDeclaration</strong> code.</span></span> <span data-ttu-id="8d8c6-395">インターフェイス上のメソッドも公開されています。</span><span class="sxs-lookup"><span data-stu-id="8d8c6-395">The methods on an interface are also public.</span></span> <span data-ttu-id="8d8c6-396">この場合も、<strong>パブリック</strong>というキーワードを明示的に含めることはオプションです。</span><span class="sxs-lookup"><span data-stu-id="8d8c6-396">Once again, explicit inclusion of the keyword <strong>public</strong> is optional.</span></span> <span data-ttu-id="8d8c6-397">インターフェイスを作成するには、次の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="8d8c6-397">To create an interface, follow these steps.</span></span>

1.  <span data-ttu-id="8d8c6-398">サーバー エクスプローラーで、プロジェクトを右クリックしてから**追加**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="8d8c6-398">In Server Explorer, right-click the project, and then click **Add**.</span></span>
2.  <span data-ttu-id="8d8c6-399">**新しい項目**ダイアログ ボックスで、**インターフェイス**を選択してからインターフェイスの名前を入力します。</span><span class="sxs-lookup"><span data-stu-id="8d8c6-399">In the **New Item** dialog box, select **Interface**, and then enter a name for the interface.</span></span>
3.  <span data-ttu-id="8d8c6-400">**追加** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="8d8c6-400">Click **Add**.</span></span>

<span data-ttu-id="8d8c6-401">クラス宣言に **implements** キーワードを追加すると、そのクラスは、インターフェイスによって指定されるメソッドを宣言する必要があります。</span><span class="sxs-lookup"><span data-stu-id="8d8c6-401">When you add the **implements** keyword on a class declaration, the class must declare the methods that are specified by the interface.</span></span> <span data-ttu-id="8d8c6-402">クラス宣言では、複数のインターフェイスを実装することができます。</span><span class="sxs-lookup"><span data-stu-id="8d8c6-402">A class declaration can implement multiple interfaces.</span></span> <span data-ttu-id="8d8c6-403">**implements** キーワードの単一の発生後にインターフェイスを一覧表示し、インターフェイス名をコンマで区切ります。</span><span class="sxs-lookup"><span data-stu-id="8d8c6-403">Just list the interfaces after the single occurrence of the **implements** keyword, and separate the interface names by using commas.</span></span> <span data-ttu-id="8d8c6-404">クラスで実装するすべてのインターフェイス メソッドはクラスの**パブリック**を使用して**パブリック**キーワードを明示的に宣言する必要があります。</span><span class="sxs-lookup"><span data-stu-id="8d8c6-404">All interface methods that a class implements must be explicitly declared as **public** by using the **public** keyword in the class.</span></span> <span data-ttu-id="8d8c6-405">インターフェイスを実装するクラスも**パブリック**として宣言する必要があります。</span><span class="sxs-lookup"><span data-stu-id="8d8c6-405">A class that implements an interface must also be declared as **public**.</span></span> <span data-ttu-id="8d8c6-406">インターフェイスを**拡張**キーワードを使用して別のインターフェイスに拡張できます。</span><span class="sxs-lookup"><span data-stu-id="8d8c6-406">An interface can extend another interface by using the **extends** keyword.</span></span> <span data-ttu-id="8d8c6-407">ただし、インターフェイスは、複数のインターフェイスを拡張することはできません。</span><span class="sxs-lookup"><span data-stu-id="8d8c6-407">However, an interface can't extend more than one interface.</span></span>

### <a name="interface-example"></a><span data-ttu-id="8d8c6-408">インターフェイスの例</span><span class="sxs-lookup"><span data-stu-id="8d8c6-408">Interface example</span></span>

<span data-ttu-id="8d8c6-409">次の例では、**Automobile** クラスは **IDrivable** インターフェイスを実装しています。</span><span class="sxs-lookup"><span data-stu-id="8d8c6-409">In the following example, an **Automobile** class implements an **IDrivable** interface.</span></span> <span data-ttu-id="8d8c6-410">**is** キーワードはサポートされており、クラスがインターフェイスを実装するかどうかをテストすることができます。</span><span class="sxs-lookup"><span data-stu-id="8d8c6-410">The **is** keyword is supported and lets you test whether a class implements an interface.</span></span>

    public interface IDrivable
    {
        public int getSpeed()
        {
        }

        public void setSpeed(int newSpeed)
        {
        }
    }

    class Automobile implements IDrivable
    {
        int m_speed;

        public int getSpeed()
        {
            return m_speed;
        }

        public void setSpeed(int newSpeed)
        {
            m_speed = newSpeed;
        }
    }

    class UseAnAutomobile
    {
        void DriveAutomobile()
        {
            IDrivable yourIDrivable;
            Automobile myAutomobile;
            str sTemp = "object is not an IDrivable";

            myAutomobile = new Automobile();

            if (myAutomobile is IDrivable)
            {
                yourIDrivable = myAutomobile;
                yourIDrivable.setSpeed(42);
                sTemp = int2str(yourIDrivable.getSpeed());
            }

            Global::info(sTemp);
            return;
            // output
            // Message (06:46:33 pm)
            // 42
        }
    }

## <a name="class-library-overview"></a><span data-ttu-id="8d8c6-411">クラス ライブラリの概要</span><span class="sxs-lookup"><span data-stu-id="8d8c6-411">Class library overview</span></span>
<span data-ttu-id="8d8c6-412">*アプリケーション クラス*および*システム クラス*の、2 種類のクラスがあります。</span><span class="sxs-lookup"><span data-stu-id="8d8c6-412">There are two kinds of classes: *application classes* and *system classes*.</span></span>

-   <span data-ttu-id="8d8c6-413">**アプリケーション クラス** - これらのクラスは X++ で実装されています。</span><span class="sxs-lookup"><span data-stu-id="8d8c6-413">**Application classes** – These classes are implemented in X++.</span></span> <span data-ttu-id="8d8c6-414">これらはアプリケーション エクスプローラーの **Classes** ノードで使用できます。</span><span class="sxs-lookup"><span data-stu-id="8d8c6-414">They are available in the **Classes** node in Application Explorer.</span></span>
-   <span data-ttu-id="8d8c6-415">**システム クラス** – これらのクラスは *カーネル クラス* としても知られており、C++ では実装されています。</span><span class="sxs-lookup"><span data-stu-id="8d8c6-415">**System classes** – These classes are sometimes known as *kernel classes* and are implemented in C++.</span></span> <span data-ttu-id="8d8c6-416">アプリケーション エクスプローラーの **System Documentation** &gt; **Classes** ノードの下に一覧表示されます。</span><span class="sxs-lookup"><span data-stu-id="8d8c6-416">They are listed under the **System Documentation** &gt; **Classes** node in Application Explorer.</span></span> <span data-ttu-id="8d8c6-417">ただし、これらのクラスのソース コードは使用できません。</span><span class="sxs-lookup"><span data-stu-id="8d8c6-417">However, the source code for these classes isn't available.</span></span>

<span data-ttu-id="8d8c6-418">これらのクラスの一覧については、[API、クラス、およびテーブルの参照](api-reference.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="8d8c6-418">For a list of these classes, see [API, class, and table reference](api-reference.md).</span></span>

## <a name="substituting-application-classes-for-system-classes"></a><span data-ttu-id="8d8c6-419">システム クラス用のアプリケーション クラスの置き換え</span><span class="sxs-lookup"><span data-stu-id="8d8c6-419">Substituting application classes for system classes</span></span>
<span data-ttu-id="8d8c6-420">拡張するシステム クラスの代わりに *アプリケーション クラスの置き換え* を呼び出す必要があります。</span><span class="sxs-lookup"><span data-stu-id="8d8c6-420">You should call the *substitute application classes* instead of the system classes that they extend.</span></span> <span data-ttu-id="8d8c6-421">アプリケーション エクスプローラーの**システムのドキュメント** &gt; **クラス**で、いくつかのカーネルまたはシステム クラスの名前は小文字 *x* で始まります。</span><span class="sxs-lookup"><span data-stu-id="8d8c6-421">In Application Explorer, under **System Documentation** &gt; **Classes**, several kernel or system classes have names that begin with a lowercase *x*.</span></span> <span data-ttu-id="8d8c6-422">これらのクラスは、*x-system classes* とも呼ばれています。</span><span class="sxs-lookup"><span data-stu-id="8d8c6-422">These classes are known as *x-system classes*.</span></span> <span data-ttu-id="8d8c6-423">これらのシステム クラスの例には、**xApplication** および **xVersionControl** が存在します。</span><span class="sxs-lookup"><span data-stu-id="8d8c6-423">Examples of these system classes are **xApplication** and **xVersionControl**.</span></span> <span data-ttu-id="8d8c6-424">これらのクラスのいくつかは、アプリケーション クラスによって拡張されます。</span><span class="sxs-lookup"><span data-stu-id="8d8c6-424">Some of these classes are extended by application classes.</span></span> <span data-ttu-id="8d8c6-425">たとえば、**アプリケーション**クラスは **xApplication** システム クラスを拡張します。</span><span class="sxs-lookup"><span data-stu-id="8d8c6-425">For example, the **Application** class extends the **xApplication** system class.</span></span> <span data-ttu-id="8d8c6-426">X システム クラスから派生するクラスは、アプリケーション クラスの代用として知られています。</span><span class="sxs-lookup"><span data-stu-id="8d8c6-426">The classes that derive from x-system classes are known as substitute application classes.</span></span> <span data-ttu-id="8d8c6-427">アプリケーション エクスプローラーの**クラス** ノードで、代替アプリケーション クラスの横にあるアイコンは標準のアイコンと異なります。</span><span class="sxs-lookup"><span data-stu-id="8d8c6-427">In Application Explorer, under the **Classes** node, the icon next to the substitute application classes differs from the standard icon.</span></span>

### <a name="x-system-classes"></a><span data-ttu-id="8d8c6-428">x システム クラス</span><span class="sxs-lookup"><span data-stu-id="8d8c6-428">x-system classes</span></span>

<span data-ttu-id="8d8c6-429">代替アプリケーション クラスの一部は、クラスのインスタンスを表す特殊なグローバル変数に関連付けられます。</span><span class="sxs-lookup"><span data-stu-id="8d8c6-429">Some of the substitute application classes are associated with a special global variable that represents an instance of the class.</span></span> <span data-ttu-id="8d8c6-430">たとえば、**appl** 変数は、**アプリケーション**クラスから事前にインスタンス化されたオブジェクトを参照します。</span><span class="sxs-lookup"><span data-stu-id="8d8c6-430">For example, the **appl** variable references a pre-instantiated object from the **Application** class.</span></span> <span data-ttu-id="8d8c6-431">**appl** 変数の利点は、セッションの範囲全体にわたってシステムがオブジェクトを保持することです。</span><span class="sxs-lookup"><span data-stu-id="8d8c6-431">The advantage of the **appl** variable is that the system maintains the object throughout the scope of your session.</span></span> <span data-ttu-id="8d8c6-432">**Application** クラスのインスタンスを取得するために **new Application()** 構文を繰り返し使用した場合、コードの効率が低下します。</span><span class="sxs-lookup"><span data-stu-id="8d8c6-432">Your code would be less efficient if it repeatedly used the **new Application()** syntax to obtain an instance of the **Application** class.</span></span> <span data-ttu-id="8d8c6-433">**xApplication** システム クラスは使用しないでください。</span><span class="sxs-lookup"><span data-stu-id="8d8c6-433">You should not use the **xApplication** system class.</span></span> <span data-ttu-id="8d8c6-434">代わりに、**アプリケーション**の代替アプリケーション クラスを使用します。</span><span class="sxs-lookup"><span data-stu-id="8d8c6-434">Instead, use the **Application** substitute application class.</span></span> <span data-ttu-id="8d8c6-435">標準構文 **Application::checkForNewBatchJobs()** を使用することにより、**アプリケーション** クラスの静的メンバーを参照することができます。</span><span class="sxs-lookup"><span data-stu-id="8d8c6-435">You can reference the static members of the **Application** class by using the following standard syntax: **Application::checkForNewBatchJobs()**.</span></span> <span data-ttu-id="8d8c6-436">ただし、**アプリケーション**クラスのインスタンス メンバーを参照するには、そのクラスの **appl** 変数 (存在する場合) を使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="8d8c6-436">However, to reference the instance members of the **Application** class, you should use that class's **appl** variable, if it exists.</span></span> <span data-ttu-id="8d8c6-437">このパターンは、ほとんどの x システム クラスに適用されます。</span><span class="sxs-lookup"><span data-stu-id="8d8c6-437">This pattern applies to most of the x-system classes.</span></span> <span data-ttu-id="8d8c6-438">**セッション** 代替アプリケーション クラスは、**セッション** の特殊なグローバル変数がないため 1 つの例外です。</span><span class="sxs-lookup"><span data-stu-id="8d8c6-438">The **Session** substitute application class is one exception, because there is no special global variable for **Session**.</span></span> <span data-ttu-id="8d8c6-439">次のテーブルは、対応するアプリケーション クラスの代用を持つ x システム クラスの一覧です。</span><span class="sxs-lookup"><span data-stu-id="8d8c6-439">The following table lists the x-system classes that have a corresponding substitute application class.</span></span> <span data-ttu-id="8d8c6-440">特殊なグローバル変数は、それらを持つクラスに対しても表示されます。</span><span class="sxs-lookup"><span data-stu-id="8d8c6-440">The special global variables are also shown for those classes that have one.</span></span>

| <span data-ttu-id="8d8c6-441">アプリケーション クラス</span><span class="sxs-lookup"><span data-stu-id="8d8c6-441">Application class</span></span> | <span data-ttu-id="8d8c6-442">x システム クラス</span><span class="sxs-lookup"><span data-stu-id="8d8c6-442">x-system class</span></span>  | <span data-ttu-id="8d8c6-443">グローバル変数</span><span class="sxs-lookup"><span data-stu-id="8d8c6-443">Global variable</span></span>    |
|-------------------|-----------------|--------------------|
| <span data-ttu-id="8d8c6-444">引数</span><span class="sxs-lookup"><span data-stu-id="8d8c6-444">Args</span></span>              | <span data-ttu-id="8d8c6-445">xArgs</span><span class="sxs-lookup"><span data-stu-id="8d8c6-445">xArgs</span></span>           | <span data-ttu-id="8d8c6-446">該当なし</span><span class="sxs-lookup"><span data-stu-id="8d8c6-446">Not applicable</span></span>     |
| <span data-ttu-id="8d8c6-447">申請</span><span class="sxs-lookup"><span data-stu-id="8d8c6-447">Application</span></span>       | <span data-ttu-id="8d8c6-448">xApplication</span><span class="sxs-lookup"><span data-stu-id="8d8c6-448">xApplication</span></span>    | <span data-ttu-id="8d8c6-449">**appl**</span><span class="sxs-lookup"><span data-stu-id="8d8c6-449">**appl**</span></span>           |
| <span data-ttu-id="8d8c6-450">ClassFactory</span><span class="sxs-lookup"><span data-stu-id="8d8c6-450">ClassFactory</span></span>      | <span data-ttu-id="8d8c6-451">xClassFactory</span><span class="sxs-lookup"><span data-stu-id="8d8c6-451">xClassFactory</span></span>   | <span data-ttu-id="8d8c6-452">**classFactory**</span><span class="sxs-lookup"><span data-stu-id="8d8c6-452">**classFactory**</span></span>   |
| <span data-ttu-id="8d8c6-453">法人</span><span class="sxs-lookup"><span data-stu-id="8d8c6-453">Company</span></span>           | <span data-ttu-id="8d8c6-454">xCompany</span><span class="sxs-lookup"><span data-stu-id="8d8c6-454">xCompany</span></span>        | <span data-ttu-id="8d8c6-455">**appl.company**</span><span class="sxs-lookup"><span data-stu-id="8d8c6-455">**appl.company**</span></span>   |
| <span data-ttu-id="8d8c6-456">グローバル</span><span class="sxs-lookup"><span data-stu-id="8d8c6-456">Global</span></span>            | <span data-ttu-id="8d8c6-457">xGlobal</span><span class="sxs-lookup"><span data-stu-id="8d8c6-457">xGlobal</span></span>         | <span data-ttu-id="8d8c6-458">該当なし</span><span class="sxs-lookup"><span data-stu-id="8d8c6-458">Not applicable</span></span>     |
| <span data-ttu-id="8d8c6-459">情報</span><span class="sxs-lookup"><span data-stu-id="8d8c6-459">Info</span></span>              | <span data-ttu-id="8d8c6-460">xInfo</span><span class="sxs-lookup"><span data-stu-id="8d8c6-460">xInfo</span></span>           | <span data-ttu-id="8d8c6-461">**情報ログ**</span><span class="sxs-lookup"><span data-stu-id="8d8c6-461">**Infolog**</span></span>        |
| <span data-ttu-id="8d8c6-462">MenuFunction</span><span class="sxs-lookup"><span data-stu-id="8d8c6-462">MenuFunction</span></span>      | <span data-ttu-id="8d8c6-463">xMenuFunction</span><span class="sxs-lookup"><span data-stu-id="8d8c6-463">xMenuFunction</span></span>   | <span data-ttu-id="8d8c6-464">該当なし</span><span class="sxs-lookup"><span data-stu-id="8d8c6-464">Not applicable</span></span>     |
| <span data-ttu-id="8d8c6-465">セッション</span><span class="sxs-lookup"><span data-stu-id="8d8c6-465">Session</span></span>           | <span data-ttu-id="8d8c6-466">xSession</span><span class="sxs-lookup"><span data-stu-id="8d8c6-466">xSession</span></span>        | <span data-ttu-id="8d8c6-467">該当なし</span><span class="sxs-lookup"><span data-stu-id="8d8c6-467">Not applicable</span></span>     |
| <span data-ttu-id="8d8c6-468">VersionControl</span><span class="sxs-lookup"><span data-stu-id="8d8c6-468">VersionControl</span></span>    | <span data-ttu-id="8d8c6-469">xVersionControl</span><span class="sxs-lookup"><span data-stu-id="8d8c6-469">xVersionControl</span></span> | <span data-ttu-id="8d8c6-470">**versionControl**</span><span class="sxs-lookup"><span data-stu-id="8d8c6-470">**versionControl**</span></span> |

### <a name="example-of-x-system-classes"></a><span data-ttu-id="8d8c6-471">x システム クラスの例</span><span class="sxs-lookup"><span data-stu-id="8d8c6-471">Example of x-system classes</span></span>

<span data-ttu-id="8d8c6-472">次の例は、代替アプリケーション クラスのインスタンスを参照するいくつかの特殊な変数を使用するための構文を示しています。</span><span class="sxs-lookup"><span data-stu-id="8d8c6-472">The following example shows the syntax for using several special variables that reference instances of the substitute application classes.</span></span>

    static void UseSpecialSystemVariablesForXJob(Args _a)
    {
        TreeNode treeNode2;
        Args     args3;
        FormRun  formRun4;
        // appl variable
        print appl.buildNo();
        // company variable
        appl.company().reloadRights(); // referenced through appl
        // Infolog variable
        treeNode2 = infolog.findNode("\\forms\\custTable");
        print treeNode2.AOTgetProperty("Name");

        // classFactory variable
        args3 = new Args(formstr(vendTable));
        formRun4 = classFactory.formRunClass(args3);
        formRun4.init();
        formRun4.run();
        formRun4.detach();
        Global::info("Method is ending. This is a message in the Infolog.");
    }

## <a name="running-startup-commands"></a><span data-ttu-id="8d8c6-473">起動コマンドの実行</span><span class="sxs-lookup"><span data-stu-id="8d8c6-473">Running startup commands</span></span>
<span data-ttu-id="8d8c6-474">起動時にコマンドを実行するには、**SysStartupCmd** クラス フレームワークを使用します。</span><span class="sxs-lookup"><span data-stu-id="8d8c6-474">You use the **SysStartupCmd** class framework to run commands at startup.</span></span> <span data-ttu-id="8d8c6-475">Finance and Operations の起動時に、アプリケーション代替カーネル クラスである **Application** (**Application.startup**) および **Info** (**Info.startup**) の \***startup** メソッドへの呼び出しが行われます。</span><span class="sxs-lookup"><span data-stu-id="8d8c6-475">When Finance and Operations starts, calls are made to the **startup** methods on the application-substituted kernel classes **Application** (**Application.startup**) and **Info** (**Info.startup**).</span></span> <span data-ttu-id="8d8c6-476">**startup** メソッドは必須システムおよびバージョン固有の呼び出しで使用されるものであり、直接変更することはできません。</span><span class="sxs-lookup"><span data-stu-id="8d8c6-476">The **startup** methods are used for vital system and version-specific calls, and you must never directly modify these methods.</span></span> <span data-ttu-id="8d8c6-477">代わりに、**SysStartupCmd** フレームワークを使用します。</span><span class="sxs-lookup"><span data-stu-id="8d8c6-477">Instead, use the **SysStartupCmd** framework.</span></span> <span data-ttu-id="8d8c6-478">SYS レイヤ バージョンの **startup** メソッドが呼び出されなかった場合、深刻な問題が生じる可能性があります。</span><span class="sxs-lookup"><span data-stu-id="8d8c6-478">Serious issues can occur if the SYS layer versions of the **startup** methods aren't called.</span></span> <span data-ttu-id="8d8c6-479">次の例は、Finance and Operations の起動時に呼び出しが実行される順序を示しています。</span><span class="sxs-lookup"><span data-stu-id="8d8c6-479">The following example shows the order that calls are run in when Finance and Operations starts.</span></span>

    appl.startup() // The SysStartupCmd class is instantiated here.
    sysStartupCmd.applInit()
    super()
    sysStartupCmd.applRun()
    info.startup()
    sysStartupCmd.infoInit()
    super()
    sysStartupCmd.infoRun()

### <a name="commands-that-are-available-when-finance-and-operations-starts"></a><span data-ttu-id="8d8c6-480">Finance and Operations 起動時に使用できるコマンド</span><span class="sxs-lookup"><span data-stu-id="8d8c6-480">Commands that are available when Finance and Operations starts</span></span>

<span data-ttu-id="8d8c6-481">**SysStartupCmd.construct** メソッドは、Finance and Operations が起動したときに使用できるコマンドを一覧表示します。</span><span class="sxs-lookup"><span data-stu-id="8d8c6-481">The **SysStartupCmd.construct** method lists the commands that are available when Finance and Operations starts.</span></span> <span data-ttu-id="8d8c6-482">これらのコマンド例を次に示します。</span><span class="sxs-lookup"><span data-stu-id="8d8c6-482">Here are some of these commands:</span></span>

-   <span data-ttu-id="8d8c6-483">AutoRun</span><span class="sxs-lookup"><span data-stu-id="8d8c6-483">AutoRun</span></span>
-   <span data-ttu-id="8d8c6-484">AOTImport</span><span class="sxs-lookup"><span data-stu-id="8d8c6-484">AOTImport</span></span>
-   <span data-ttu-id="8d8c6-485">同期</span><span class="sxs-lookup"><span data-stu-id="8d8c6-485">Synchronize</span></span>

<span data-ttu-id="8d8c6-486">次の例は、Finance and Operations の起動時に新しいコマンドを実行する方法を示しています。</span><span class="sxs-lookup"><span data-stu-id="8d8c6-486">The following example shows how to run a new command when Finance and Operations starts.</span></span> <span data-ttu-id="8d8c6-487">最初に、<strong>SysStartupCmd</strong> を拡張するクラスが作成されます。</span><span class="sxs-lookup"><span data-stu-id="8d8c6-487">First, a class that extends <strong>SysStartupCmd</strong> is created.</span></span> <span data-ttu-id="8d8c6-488">この新しいクラスは特定のタスクを実行します。</span><span class="sxs-lookup"><span data-stu-id="8d8c6-488">This new class performs your specific task.</span></span> <span data-ttu-id="8d8c6-489">次に、自分のクラスを呼び出すために、<strong>SysStartupCmd</strong> の construct メソッドを変更します。</span><span class="sxs-lookup"><span data-stu-id="8d8c6-489">You then modify the construct method on <strong>SysStartupCmd</strong> to call your class.</span></span> <span data-ttu-id="8d8c6-490">Finance and Operations のコンフィギュレーション ユーティリティの<strong>一般</strong>タブにある<strong>アプリケーション起動時に実行するコマンド</strong> フィールドで、起動時に実行するコマンドを追加できます。</span><span class="sxs-lookup"><span data-stu-id="8d8c6-490">In the Finance and Operations Configuration Utility, on the <strong>General</strong> tab, in the <strong>Command to run at application startup</strong> field, you can add commands that are run at startup.</span></span> <span data-ttu-id="8d8c6-491">または、<strong>-startupcmd= *MyCommand</strong>* コマンド ライン パラメーターを使用できます。</span><span class="sxs-lookup"><span data-stu-id="8d8c6-491">Alternatively, you can use the <strong>-startupcmd= *MyCommand</strong>* command-line parameter.</span></span>

    public class SysStartupCmdAutoRun : extends SysStartupCmd 
    {
        void new(str s, str parm) 
        {
            // Your code here.
        }
    }

    // This is a framework class. Customizing this class may cause problems with future upgrades to the software.
    class SysStartupCmd
    {
        // Code delete for readability

        static SysStartupCmd construct(str startupCommand)
        {
            // Code delete for readability
            switch (s)
            {
                // Other cases delete for readability    
                case 'autorun':
                    sysStartupCmd = new SysStartupCmdAutoRun(s,parm);
                    break;
                // Other cases delete for readability
            }
            // Code delete for readability
        }
    }

## <a name="batch-processing-classes"></a><span data-ttu-id="8d8c6-492">バッチ処理クラス</span><span class="sxs-lookup"><span data-stu-id="8d8c6-492">Batch processing classes</span></span>
<span data-ttu-id="8d8c6-493">クラスを実装するには、バッチ処理システムを使用し、**RunBase** および **RunBaseBatch** クラスを拡張します。</span><span class="sxs-lookup"><span data-stu-id="8d8c6-493">You implement classes by using the batch processing system, and by extending the **RunBase** and **RunBaseBatch** classes.</span></span> <span data-ttu-id="8d8c6-494">**バッチ処理**ダイアログ ボックスから**繰り返し**ボタンを削除するには、**Args::parmEnum** メソッドを使用します。</span><span class="sxs-lookup"><span data-stu-id="8d8c6-494">To remove the **Recurrence** button from the **Batch processing** dialog box, you use the **Args::parmEnum** method.</span></span> <span data-ttu-id="8d8c6-495">サーバー バインド バッチ メソッドとして実行するクラスを指定することをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="8d8c6-495">We recommend that you designate a class to run as a server-bound batch method.</span></span> <span data-ttu-id="8d8c6-496">サーバー バインド バッチ メソッドは、以下の理由のため、サーバー バインドでないバッチ メソッドより安全です。</span><span class="sxs-lookup"><span data-stu-id="8d8c6-496">Server-bound batch methods are more secure than batch methods that aren't server-bound for the following reasons:</span></span>

-   <span data-ttu-id="8d8c6-497">このメソッドは、メソッドを送信したユーザーのアクセス許可を使用して実行されます。</span><span class="sxs-lookup"><span data-stu-id="8d8c6-497">The method is run by using the permissions of the user who submitted the method.</span></span>
-   <span data-ttu-id="8d8c6-498">このメソッドは、特定の **情報** および **グローバル** クラス メソッドのみを使用して、それを処理しているクライアントと対話できます。</span><span class="sxs-lookup"><span data-stu-id="8d8c6-498">The method can use only specific **Info** and **Global** class methods to interact with the client that is processing it.</span></span> <span data-ttu-id="8d8c6-499">この制限により、クライアントとのやり取りが制限されます。</span><span class="sxs-lookup"><span data-stu-id="8d8c6-499">This restriction limits interaction with the client.</span></span>

### <a name="enable-a-class-to-run-as-a-server-bound-batch-method"></a><span data-ttu-id="8d8c6-500">サーバー バインド バッチ メソッドとして実行するクラスを有効化</span><span class="sxs-lookup"><span data-stu-id="8d8c6-500">Enable a class to run as a server-bound batch method</span></span>

1.  <span data-ttu-id="8d8c6-501">**RunBaseBatch** クラスを拡張するクラスを作成します。</span><span class="sxs-lookup"><span data-stu-id="8d8c6-501">Create a class that extends the **RunBaseBatch** class.</span></span>
2.  <span data-ttu-id="8d8c6-502">次の例に示すように、**RunBaseBatch.runsImpersonated** メソッドをオーバーライドし、値 **true** を返します。</span><span class="sxs-lookup"><span data-stu-id="8d8c6-502">Override the **RunBaseBatch.runsImpersonated** method to return a value of **true**, as shown in the following example.</span></span>

        public boolean runsImpersonated()
        {
            return true;
        }

3.  <span data-ttu-id="8d8c6-503">クラスが次の**情報**および**グローバル**クラスのメソッドのみを呼び出すことを確認します。</span><span class="sxs-lookup"><span data-stu-id="8d8c6-503">Confirm that the class calls only the following **Info** and **Global** class methods:</span></span>
    -   <span data-ttu-id="8d8c6-504">追加</span><span class="sxs-lookup"><span data-stu-id="8d8c6-504">add</span></span>
    -   <span data-ttu-id="8d8c6-505">Info.copy</span><span class="sxs-lookup"><span data-stu-id="8d8c6-505">Info.copy</span></span>
    -   <span data-ttu-id="8d8c6-506">Info.cut</span><span class="sxs-lookup"><span data-stu-id="8d8c6-506">Info.cut</span></span>
    -   <span data-ttu-id="8d8c6-507">Info.import</span><span class="sxs-lookup"><span data-stu-id="8d8c6-507">Info.import</span></span>
    -   <span data-ttu-id="8d8c6-508">Info.export</span><span class="sxs-lookup"><span data-stu-id="8d8c6-508">Info.export</span></span>
    -   <span data-ttu-id="8d8c6-509">Info.line</span><span class="sxs-lookup"><span data-stu-id="8d8c6-509">Info.line</span></span>
    -   <span data-ttu-id="8d8c6-510">Info.num</span><span class="sxs-lookup"><span data-stu-id="8d8c6-510">Info.num</span></span>
    -   <span data-ttu-id="8d8c6-511">Global::error</span><span class="sxs-lookup"><span data-stu-id="8d8c6-511">Global::error</span></span>
    -   <span data-ttu-id="8d8c6-512">Global::info</span><span class="sxs-lookup"><span data-stu-id="8d8c6-512">Global::info</span></span>
    -   <span data-ttu-id="8d8c6-513">Global::warning</span><span class="sxs-lookup"><span data-stu-id="8d8c6-513">Global::warning</span></span>

    <span data-ttu-id="8d8c6-514">**注記:** **Info.line** および **Info.num** メソッドは、**xInfo** クラスから継承されます。</span><span class="sxs-lookup"><span data-stu-id="8d8c6-514">**Note:** The **Info.line** and **Info.num** methods are inherited from the **xInfo** class.</span></span>

### <a name="removing-the-recurrence-button-from-the-batch-processing-dialog-box"></a><span data-ttu-id="8d8c6-515">バッチ処理ダイアログ ボックスから定期的なアイテムを削除</span><span class="sxs-lookup"><span data-stu-id="8d8c6-515">Removing the Recurrence button from the batch processing dialog box</span></span>

<span data-ttu-id="8d8c6-516">バッチ処理システムを使用してクラスを実装するときは、**Args.parmEnum** メソッドを呼び出し、**NoYes::Yes** システム列挙値を渡して、**再実行**ボタンを削除できます。</span><span class="sxs-lookup"><span data-stu-id="8d8c6-516">When you implement a class by using the batch processing system, you can remove the **Recurrence** button by calling the **Args.parmEnum** method and passing the **NoYes::Yes** system enumeration value.</span></span> <span data-ttu-id="8d8c6-517">**NoYes** システム列挙は、**繰り返し** ボタンがダイアログ ボックスから削除されるかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="8d8c6-517">The **NoYes** system enumeration determines whether the **Recurrence** button is removed from the dialog box.</span></span> <span data-ttu-id="8d8c6-518">既定値は **NoYes::No** です。</span><span class="sxs-lookup"><span data-stu-id="8d8c6-518">The default value is **NoYes::No**.</span></span> <span data-ttu-id="8d8c6-519">次の例では、**InventTransferMultiShip** クラスが実装されています。</span><span class="sxs-lookup"><span data-stu-id="8d8c6-519">In the following example, the **InventTransferMultiShip** class is implemented.</span></span> <span data-ttu-id="8d8c6-520">**BatchDialog::main** メソッドは、**バッチ処理**ダイアログ ボックスを作成します。</span><span class="sxs-lookup"><span data-stu-id="8d8c6-520">The **BatchDialog::main** method creates the **Batch processing** dialog box.</span></span>

    static void noRecurrenceButton(Args _args)
    {
        Args a;
        InventTransferMultiShip inventTransferMultiShip;
        a = new Args();
        inventTransferMultiShip = InventTransferMultiShip::construct();
        a.caller(inventTransferMultiShip);
        a.parmEnum(NoYes::Yes);
        BatchDialog::main(a);
    }

## <a name="image-manipulation-classes"></a><span data-ttu-id="8d8c6-521">イメージ操作クラス</span><span class="sxs-lookup"><span data-stu-id="8d8c6-521">Image manipulation classes</span></span>
<span data-ttu-id="8d8c6-522">**Image** と **Imagelist** の 2 つのシステム クラスにより、グラフィックスとアイコンを操作できます。</span><span class="sxs-lookup"><span data-stu-id="8d8c6-522">Two system classes let you to manipulate graphics and icons: **Image** and **Imagelist**.</span></span>

- <span data-ttu-id="8d8c6-523">**Image** – このクラスでは、個々の画像の読み込み、保存、操作などができます。</span><span class="sxs-lookup"><span data-stu-id="8d8c6-523">**Image** – This class lets you load, save, and manipulate individual images.</span></span> <span data-ttu-id="8d8c6-524">たとえば、画面をキャプチャして画像として保存し、画像をトリミングまたは回転させる、または色深度を操作します。</span><span class="sxs-lookup"><span data-stu-id="8d8c6-524">For example, you can capture a screen and save it as an image, crop or rotate an image, or manipulate the color depth.</span></span>
- <span data-ttu-id="8d8c6-525"><strong>Imagelist</strong> - このクラスを使用すると、サイズや透明色などの一般的なプロパティを持つ一連の画像を操作できます。</span><span class="sxs-lookup"><span data-stu-id="8d8c6-525"><strong>Imagelist</strong> – This class lets you work with a set of images that have common properties, such as the size and transparency color.</span></span> <span data-ttu-id="8d8c6-526"><strong>ImageListAppl\_\</strong>\* アプリケーション クラス の Finance and Operations で使用されるイメージ リストを表示できます。</span><span class="sxs-lookup"><span data-stu-id="8d8c6-526">You can view the image lists that are used in Finance and Operations in the <strong>ImageListAppl\_\</strong>\* application classes.</span></span>

## <a name="query-object-model"></a><span data-ttu-id="8d8c6-527">クエリ オブジェクト モデル</span><span class="sxs-lookup"><span data-stu-id="8d8c6-527">Query object model</span></span>
<span data-ttu-id="8d8c6-528">クエリ オブジェクト モデルには、クエリの定義と実行に使用されるクラスが含まれています。</span><span class="sxs-lookup"><span data-stu-id="8d8c6-528">The query object model contains classes that are used to define and run a query.</span></span> <span data-ttu-id="8d8c6-529">クエリ オブジェクトは、クエリ データ ソース、返されるフィールド、レコード範囲、子データ ソースとの関係を定義するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="8d8c6-529">The query objects are used to define the query data source, the fields that are returned, record ranges, and relations to child data sources.</span></span> <span data-ttu-id="8d8c6-530">動的クエリをコードで作成すると、クエリ クラスの可視性が高まります。さらに、これらは、アプリケーション エクスプローラーで静的クエリを作成するときにもシーン裏で使用されます。</span><span class="sxs-lookup"><span data-stu-id="8d8c6-530">The query classes are more visible when you create a dynamic query in code, but they are also used behind the scenes when you create a static query in Application Explorer.</span></span> <span data-ttu-id="8d8c6-531">次のテーブルでは、クエリ オブジェクト モデルのクラスについて説明します。</span><span class="sxs-lookup"><span data-stu-id="8d8c6-531">The following table describes the classes in the query object model.</span></span>

| <span data-ttu-id="8d8c6-532">システム クラス</span><span class="sxs-lookup"><span data-stu-id="8d8c6-532">System class</span></span>         | <span data-ttu-id="8d8c6-533">説明</span><span class="sxs-lookup"><span data-stu-id="8d8c6-533">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
|----------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8d8c6-534">QueryRun</span><span class="sxs-lookup"><span data-stu-id="8d8c6-534">QueryRun</span></span>             | <span data-ttu-id="8d8c6-535">このクラスは、クエリを実行し、データをフェッチします。</span><span class="sxs-lookup"><span data-stu-id="8d8c6-535">This class runs the query and fetches the data.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
| <span data-ttu-id="8d8c6-536">クエリ</span><span class="sxs-lookup"><span data-stu-id="8d8c6-536">Query</span></span>                | <span data-ttu-id="8d8c6-537">このクラスはいくつかのプロパティを保持し、1 つ以上の関連するデータ ソースを持ちます。</span><span class="sxs-lookup"><span data-stu-id="8d8c6-537">This class holds some properties, and has one or more related data sources.</span></span> <span data-ttu-id="8d8c6-538">クエリの定義の最上位です。</span><span class="sxs-lookup"><span data-stu-id="8d8c6-538">It's the top level of the query definition.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                             |
| <span data-ttu-id="8d8c6-539">QueryBuildDataSource</span><span class="sxs-lookup"><span data-stu-id="8d8c6-539">QueryBuildDataSource</span></span> | <span data-ttu-id="8d8c6-540">このクラスは、クエリ内の単一のデータ ソースへのアクセスを定義します。</span><span class="sxs-lookup"><span data-stu-id="8d8c6-540">This class defines access to a single data source in the query.</span></span> <span data-ttu-id="8d8c6-541">クエリに同じレベルの 1 つ以上のデータ ソースある場合、独立した SQL ステートメントが生産され、順番に実行されます。</span><span class="sxs-lookup"><span data-stu-id="8d8c6-541">If there is more than one data source at the same level in a query, separate SQL statements are produced and are run sequentially.</span></span> <span data-ttu-id="8d8c6-542">データ ソースが別のデータ ソースの子である場合は、2 つのデータ ソース間に結合が作成されます。</span><span class="sxs-lookup"><span data-stu-id="8d8c6-542">If one data source is a child of another data source, a join is created between the two data sources.</span></span>                                                                                                                                                                                                                                            |
| <span data-ttu-id="8d8c6-543">QueryBuildFieldList</span><span class="sxs-lookup"><span data-stu-id="8d8c6-543">QueryBuildFieldList</span></span>  | <span data-ttu-id="8d8c6-544">このクラスは、データベースから返されるフィールドを定義します。</span><span class="sxs-lookup"><span data-stu-id="8d8c6-544">This class defines the fields that are returned from the database.</span></span> <span data-ttu-id="8d8c6-545">既定では、フィールド リストは動的であり、すべてのフィールドはデータ ソース テーブル、マップ、またはビューから戻されます。</span><span class="sxs-lookup"><span data-stu-id="8d8c6-545">By default, the field list is dynamic, and all fields are returned from the data source table, map, or view.</span></span> <span data-ttu-id="8d8c6-546">各データ ソースには、**QueryBuildFieldList** オブジェクトが 1 つだけあります。</span><span class="sxs-lookup"><span data-stu-id="8d8c6-546">Each data source has only one **QueryBuildFieldList** object.</span></span> <span data-ttu-id="8d8c6-547">このオブジェクトには、選択したすべてのフィールドに関する情報が含まれます。</span><span class="sxs-lookup"><span data-stu-id="8d8c6-547">This object contains information about all selected fields.</span></span> <span data-ttu-id="8d8c6-548">フィールド リスト オブジェクトで、**SUM**、**COUNT**、および **AVG** などの、集計関数を指定することができます。</span><span class="sxs-lookup"><span data-stu-id="8d8c6-548">You can specify aggregate functions, such as **SUM**, **COUNT**, and **AVG**, on the field list object.</span></span>                                                                                                                                   |
| <span data-ttu-id="8d8c6-549">QueryBuildRange</span><span class="sxs-lookup"><span data-stu-id="8d8c6-549">QueryBuildRange</span></span>      | <span data-ttu-id="8d8c6-550">このクラスは、単一フィールドに基づいて、返されるレコードのサブセットを定義します。</span><span class="sxs-lookup"><span data-stu-id="8d8c6-550">This class defines a subset of records that is returned, based on a single field.</span></span> <span data-ttu-id="8d8c6-551">範囲は、クエリ SQL ステートメントの **WHERE** 句に変換されます。</span><span class="sxs-lookup"><span data-stu-id="8d8c6-551">A range is translated into a **WHERE** clause in the query SQL statement.</span></span> <span data-ttu-id="8d8c6-552">クエリを制限するために 1 つ以上のフィールドが使用されている場合 (**WHERE**句)、データ ソースには 1 つ以上の範囲が含まれます。</span><span class="sxs-lookup"><span data-stu-id="8d8c6-552">If more than one field is used to limit the query (**WHERE** clause), the data source will contain more than one range.</span></span>                                                                                                                                                                                                                                                                 |
| <span data-ttu-id="8d8c6-553">QueryBuildDynalink</span><span class="sxs-lookup"><span data-stu-id="8d8c6-553">QueryBuildDynalink</span></span>   | <span data-ttu-id="8d8c6-554">このクラスには、外部レコードとの関係 (制限) に関する情報が含まれます。</span><span class="sxs-lookup"><span data-stu-id="8d8c6-554">This class contains information about a relation (limitation) to an external record.</span></span> <span data-ttu-id="8d8c6-555">クエリを実行すると、この情報は、クエリ SQL ステートメントの **WHERE** 句内で追加のエントリに変換されます。</span><span class="sxs-lookup"><span data-stu-id="8d8c6-555">When the query is run, this information is converted to additional entries in the **WHERE** clause of the query SQL statement.</span></span> <span data-ttu-id="8d8c6-556">このクラスは、クエリの親データ ソースにのみ存在できます。</span><span class="sxs-lookup"><span data-stu-id="8d8c6-556">This class can exist only on the parent data source of a query.</span></span> <span data-ttu-id="8d8c6-557">フォームは、2 つのデータ ソースが同期されるときにこの機能を使用します。</span><span class="sxs-lookup"><span data-stu-id="8d8c6-557">Forms use the function when two data sources are synchronized.</span></span> <span data-ttu-id="8d8c6-558">子データ ソースは、親データ ソース に対する 1 つ以上の DLL を格納します。</span><span class="sxs-lookup"><span data-stu-id="8d8c6-558">The child data source will then contain one or more DLLs to the parent data source.</span></span> <span data-ttu-id="8d8c6-559">この関数は、2 つのデータソースが 2 つの異なる形式になっていて、まだ同期されている場合でも使用されます。</span><span class="sxs-lookup"><span data-stu-id="8d8c6-559">The function is used even if the two data sources are put in two different forms but are still synchronized.</span></span> |
| <span data-ttu-id="8d8c6-560">QueryBuildLink</span><span class="sxs-lookup"><span data-stu-id="8d8c6-560">QueryBuildLink</span></span>       | <span data-ttu-id="8d8c6-561">このクラスは、結合に 2 つのデータ ソースの間の関係を指定します。</span><span class="sxs-lookup"><span data-stu-id="8d8c6-561">This class specifies the relation between the two data sources in the join.</span></span> <span data-ttu-id="8d8c6-562">このクラスは、子データ ソースにのみ存在できます。</span><span class="sxs-lookup"><span data-stu-id="8d8c6-562">This class can exist only on a child data source.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                       |

## <a name="system-classes-overview"></a><span data-ttu-id="8d8c6-563">システム クラスの概要</span><span class="sxs-lookup"><span data-stu-id="8d8c6-563">System classes overview</span></span>
<span data-ttu-id="8d8c6-564">システム クラス (またはカーネル クラス) は C++ で実装されます。</span><span class="sxs-lookup"><span data-stu-id="8d8c6-564">System classes (or kernel classes) are implemented in C++.</span></span> <span data-ttu-id="8d8c6-565">これらのクラスのソースは使用できません。</span><span class="sxs-lookup"><span data-stu-id="8d8c6-565">The source for these classes isn't available.</span></span> <span data-ttu-id="8d8c6-566">システム クラスは、次の特性を持つことができます。</span><span class="sxs-lookup"><span data-stu-id="8d8c6-566">A system class can have the following characteristics:</span></span>

-   <span data-ttu-id="8d8c6-567">静的メソッド (またはクラス メソッド)</span><span class="sxs-lookup"><span data-stu-id="8d8c6-567">Static methods (or class methods)</span></span>
-   <span data-ttu-id="8d8c6-568">動的メソッド</span><span class="sxs-lookup"><span data-stu-id="8d8c6-568">Dynamic methods</span></span>
-   <span data-ttu-id="8d8c6-569">プロパティ - これらのプロパティは、プロパティを設定するために使用されるメンバー関数です。</span><span class="sxs-lookup"><span data-stu-id="8d8c6-569">Properties – These properties are member functions that are used to set properties.</span></span> <span data-ttu-id="8d8c6-570">たとえば **LeftMargin** です。</span><span class="sxs-lookup"><span data-stu-id="8d8c6-570">An example is **LeftMargin**.</span></span>

<span data-ttu-id="8d8c6-571">システム クラスのメソッドをオーバーライドすることはできません。</span><span class="sxs-lookup"><span data-stu-id="8d8c6-571">You can't override system class methods.</span></span> <span data-ttu-id="8d8c6-572">最初からアプリケーション オブジェクトをデザインするためにシステム クラスを使用することを意図していません。</span><span class="sxs-lookup"><span data-stu-id="8d8c6-572">It isn't our intention that you will use the system classes to design your application objects from scratch.</span></span> <span data-ttu-id="8d8c6-573">代わりに、アプリケーション エクスプローラーで既存の機能を拡張または変更するために使用します。</span><span class="sxs-lookup"><span data-stu-id="8d8c6-573">Instead, use them to extend or modify the default functionality in Application Explorer.</span></span> <span data-ttu-id="8d8c6-574">たとえば、既存のレポートに追加情報を動的に追加することができます。</span><span class="sxs-lookup"><span data-stu-id="8d8c6-574">For example, you can dynamically add extra information to an existing report.</span></span> <span data-ttu-id="8d8c6-575">または、前のページでのユーザーの選択に基づいて、ページ上で使用可能なオプションを変更することができます。</span><span class="sxs-lookup"><span data-stu-id="8d8c6-575">Alternatively, you can change the options that are available on a page, based on the user's selection on a previous page.</span></span>

### <a name="collection-classes"></a><span data-ttu-id="8d8c6-576">コレクション クラス</span><span class="sxs-lookup"><span data-stu-id="8d8c6-576">Collection classes</span></span>

<span data-ttu-id="8d8c6-577">*コレクション クラス*を使用すると、リスト、セット、構造体、マップ、および配列を作成できます。</span><span class="sxs-lookup"><span data-stu-id="8d8c6-577">The *collection classes* let you create lists, sets, structs, maps, and arrays.</span></span>

### <a name="application-object-classes"></a><span data-ttu-id="8d8c6-578">アプリケーション オブジェクト クラス</span><span class="sxs-lookup"><span data-stu-id="8d8c6-578">Application object classes</span></span>

<span data-ttu-id="8d8c6-579">これらのシステム クラスは、アプリケーション エクスプローラーを使用してアプリケーションを作成するたびにアクティブ化される関数を保持します。</span><span class="sxs-lookup"><span data-stu-id="8d8c6-579">These system classes hold functions that are activated whenever you use Application Explorer to create your application.</span></span> <span data-ttu-id="8d8c6-580">たとえば、システムは、アプリケーション エクスプローラーの**設計**ノードでフォームのレイアウトを定義する時、**FormDesign** クラスを使用します。</span><span class="sxs-lookup"><span data-stu-id="8d8c6-580">For example, the system uses the **FormDesign** class when you define the layout of your form in the **Designs** node in Application Explorer.</span></span> <span data-ttu-id="8d8c6-581">これらのクラスを使用すると、アプリケーション オブジェクトを作成したり変更したりすることもできます。</span><span class="sxs-lookup"><span data-stu-id="8d8c6-581">These classes also let you to create and modify application objects.</span></span>

### <a name="integration-classes"></a><span data-ttu-id="8d8c6-582">統合クラス</span><span class="sxs-lookup"><span data-stu-id="8d8c6-582">Integration classes</span></span>

<span data-ttu-id="8d8c6-583">環境との統合は、通常、クラスによって実装されます。</span><span class="sxs-lookup"><span data-stu-id="8d8c6-583">The integration with the environment is typically implemented by classes.</span></span> <span data-ttu-id="8d8c6-584">このカテゴリ内のクラスの例を次に示します。</span><span class="sxs-lookup"><span data-stu-id="8d8c6-584">Here are some examples of the classes in this category:</span></span>

-   <span data-ttu-id="8d8c6-585">**COM** - COM オブジェクトのメソッドの呼び出しです。</span><span class="sxs-lookup"><span data-stu-id="8d8c6-585">**COM** – The call of methods on COM objects.</span></span>
-   <span data-ttu-id="8d8c6-586">**DLL** – Microsoft Windows DLL 関数の呼び出し。</span><span class="sxs-lookup"><span data-stu-id="8d8c6-586">**DLL** – The call of Microsoft Windows DLL functions.</span></span>
-   <span data-ttu-id="8d8c6-587">**IO** – 外部ファイルの読み取りと書き込みを行います。</span><span class="sxs-lookup"><span data-stu-id="8d8c6-587">**IO** – Read and write external files.</span></span>
-   <span data-ttu-id="8d8c6-588">**ODBCConnection** – 外部データベースへの Open Database Connectivity (ODBC) インターフェイス。</span><span class="sxs-lookup"><span data-stu-id="8d8c6-588">**ODBCConnection** – An Open Database Connectivity (ODBC) interface to a foreign database.</span></span>

## <a name="event-terminology-and-keywords"></a><span data-ttu-id="8d8c6-589">イベントの用語およびキーワード</span><span class="sxs-lookup"><span data-stu-id="8d8c6-589">Event terminology and keywords</span></span>
<span data-ttu-id="8d8c6-590">イベント設計パターンを使用すると、コードをさらにモジュール化して再使用可能にすることができます。</span><span class="sxs-lookup"><span data-stu-id="8d8c6-590">You can use the event design pattern to make your code more modular and reusable.</span></span> <span data-ttu-id="8d8c6-591">*イベント* という用語は、デリゲートの使用方法を説明するメタファです。</span><span class="sxs-lookup"><span data-stu-id="8d8c6-591">The term *event* is a metaphor that explains how delegates are used.</span></span> <span data-ttu-id="8d8c6-592">プログラム実行中に何か重要なことが発生したときは、他のモジュールがその発生を処理することが必要な場合があります。</span><span class="sxs-lookup"><span data-stu-id="8d8c6-592">When something important occurs during a program run, other modules might have to process the occurrence.</span></span> <span data-ttu-id="8d8c6-593">これらの重要な出来事は*イベント*と呼ばれています。</span><span class="sxs-lookup"><span data-stu-id="8d8c6-593">These important occurrences are known as *events*.</span></span> <span data-ttu-id="8d8c6-594">イベントが発生すると、プログラムは、Notifier がイベントに関する通知を送信する必要があることを、そのイベントの Notifier に指示します。</span><span class="sxs-lookup"><span data-stu-id="8d8c6-594">When an event occurs, the program tells its notifier for the event that the notifier must send notifications about the event.</span></span> <span data-ttu-id="8d8c6-595">通知は、通知のサブスクライバーであるすべてのイベント ハンドラーに送信する必要があります。</span><span class="sxs-lookup"><span data-stu-id="8d8c6-595">A notification must be sent to all the event handlers that are subscribers of the notifier.</span></span> <span data-ttu-id="8d8c6-596">プログラムがその通知機能に通知を送信するように指示するとき、そのプロセスをイベントの *発生* と呼んでいます。</span><span class="sxs-lookup"><span data-stu-id="8d8c6-596">When the program tells its notifier to send the notifications, we call that process *raising* an event.</span></span> <span data-ttu-id="8d8c6-597">次のテーブルは、イベント メタファを説明するために使用される用語を示しています。</span><span class="sxs-lookup"><span data-stu-id="8d8c6-597">The following table shows the terms that are used to describe the event metaphor.</span></span>

| <span data-ttu-id="8d8c6-598">期間</span><span class="sxs-lookup"><span data-stu-id="8d8c6-598">Term</span></span>          | <span data-ttu-id="8d8c6-599">説明</span><span class="sxs-lookup"><span data-stu-id="8d8c6-599">Description</span></span>                                                                                                               |
|---------------|---------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8d8c6-600">イベント</span><span class="sxs-lookup"><span data-stu-id="8d8c6-600">Event</span></span>         | <span data-ttu-id="8d8c6-601">追加モジュールは発生を処理するプログラム モジュールで重要な発生です。</span><span class="sxs-lookup"><span data-stu-id="8d8c6-601">An important occurrence in a program module where additional modules must process the occurrence.</span></span>                         |
| <span data-ttu-id="8d8c6-602">通知機能</span><span class="sxs-lookup"><span data-stu-id="8d8c6-602">Notifier</span></span>      | <span data-ttu-id="8d8c6-603">通知機能に登録されているすべてのイベント ハンドラーに、イベントに関する情報を送信するプログラム要素。</span><span class="sxs-lookup"><span data-stu-id="8d8c6-603">The program element that sends information about the event to all the event handlers that are subscribed to the notifier.</span></span> |
| <span data-ttu-id="8d8c6-604">サブスクライバー</span><span class="sxs-lookup"><span data-stu-id="8d8c6-604">Subscriber</span></span>    | <span data-ttu-id="8d8c6-605">イベント通知機能を登録しているプログラム機能またはメソッド。</span><span class="sxs-lookup"><span data-stu-id="8d8c6-605">The program functions or methods that are subscribed to an event notifier.</span></span>                                                |
| <span data-ttu-id="8d8c6-606">イベント ハンドラー</span><span class="sxs-lookup"><span data-stu-id="8d8c6-606">Event handler</span></span> | <span data-ttu-id="8d8c6-607">イベント通知を購読するメソッド。</span><span class="sxs-lookup"><span data-stu-id="8d8c6-607">The methods that subscribe to an event notifier.</span></span> <span data-ttu-id="8d8c6-608">適切な種類のメソッドのみ、イベント ハンドラーになることができます。</span><span class="sxs-lookup"><span data-stu-id="8d8c6-608">Only the appropriate kind of methods can be event handlers.</span></span>              |

### <a name="keywords-that-are-used-for-programming-that-uses-delegates"></a><span data-ttu-id="8d8c6-609">デリゲートを使用するプログラミングに使用されるキーワード</span><span class="sxs-lookup"><span data-stu-id="8d8c6-609">Keywords that are used for programming that uses delegates</span></span>

<span data-ttu-id="8d8c6-610">次のテーブルに、デリゲートの使用方法を説明するキーワードを示します。</span><span class="sxs-lookup"><span data-stu-id="8d8c6-610">The following table shows the keywords that describe the use of delegates.</span></span>

| <span data-ttu-id="8d8c6-611">キーワードや用語</span><span class="sxs-lookup"><span data-stu-id="8d8c6-611">Keyword or term</span></span>                         | <span data-ttu-id="8d8c6-612">区分</span><span class="sxs-lookup"><span data-stu-id="8d8c6-612">Code</span></span>                                                                     | <span data-ttu-id="8d8c6-613">説明</span><span class="sxs-lookup"><span data-stu-id="8d8c6-613">Description</span></span>                                                                                                                                                                                                                                                                             |
|-----------------------------------------|--------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8d8c6-614">デリゲート</span><span class="sxs-lookup"><span data-stu-id="8d8c6-614">delegate</span></span>                                | <span data-ttu-id="8d8c6-615">delegate myDelegate(str \_information) {}</span><span class="sxs-lookup"><span data-stu-id="8d8c6-615">delegate myDelegate(str \_information) {}</span></span>                                | <span data-ttu-id="8d8c6-616">このコードは、Microsoft MorphX クライアントのメソッド エディターでのデリゲートの外観を示しています。</span><span class="sxs-lookup"><span data-stu-id="8d8c6-616">The code shows what the delegate looks like in the method editor in the Microsoft MorphX client.</span></span> <span data-ttu-id="8d8c6-617">戻り値の型は常に**無効**なので、構文には示されていません。</span><span class="sxs-lookup"><span data-stu-id="8d8c6-617">Because the return type is always **void**, it isn't mentioned in the syntax.</span></span> <span data-ttu-id="8d8c6-618">かっこ ({}) 内にコードは使用できません。</span><span class="sxs-lookup"><span data-stu-id="8d8c6-618">No code is allowed inside the braces ({}).</span></span>                                                               |
| <span data-ttu-id="8d8c6-619">eventHandler</span><span class="sxs-lookup"><span data-stu-id="8d8c6-619">eventHandler</span></span>                            | <span data-ttu-id="8d8c6-620">myClassInstance.myDelegate += eventHandler(otherClass.myInstanceMethod);</span><span class="sxs-lookup"><span data-stu-id="8d8c6-620">myClassInstance.myDelegate += eventHandler(otherClass.myInstanceMethod);</span></span> | <span data-ttu-id="8d8c6-621">**eventHandler** キーワードの構文は **eventHandler** X++ 関数であるという印象を与えますが、それは関数ではありません。</span><span class="sxs-lookup"><span data-stu-id="8d8c6-621">Although the syntax of the **eventHandler** keyword might give the impression that **eventHandler** is an X++ function, it isn't a function.</span></span> <span data-ttu-id="8d8c6-622">**eventHandler** キーワードは、メソッドがデリゲートにサブスクライブされることをコンパイラに伝えます。</span><span class="sxs-lookup"><span data-stu-id="8d8c6-622">The **eventHandler** keyword tells the compiler that a method is being subscribed to a delegate.</span></span>                                           |
| <span data-ttu-id="8d8c6-623">デリゲートにメソッドをサブスクライブまたは追加</span><span class="sxs-lookup"><span data-stu-id="8d8c6-623">Subscribe or add a method to a delegate</span></span> | <span data-ttu-id="8d8c6-624">myClassInstance.myDelegate += eventHandler(OtherClass::aStaticMethod);</span><span class="sxs-lookup"><span data-stu-id="8d8c6-624">myClassInstance.myDelegate += eventHandler(OtherClass::aStaticMethod);</span></span>   | <span data-ttu-id="8d8c6-625">コードでは、静的メソッド **OtherClass::aStaticMethod** がデリゲートにサブスクライブされます。</span><span class="sxs-lookup"><span data-stu-id="8d8c6-625">In the code, the static method **OtherClass::aStaticMethod** becomes subscribed to the delegate.</span></span>                                                                                                                                                                                        |
| <span data-ttu-id="8d8c6-626">デリゲートの呼び出し</span><span class="sxs-lookup"><span data-stu-id="8d8c6-626">Call a delegate</span></span>                         | <span data-ttu-id="8d8c6-627">myClassInstance.myDelegate("Hello");</span><span class="sxs-lookup"><span data-stu-id="8d8c6-627">myClassInstance.myDelegate("Hello");</span></span>                                     | <span data-ttu-id="8d8c6-628">デリゲートへのこの呼び出しは、デリゲートにサブスクライブしている各メソッドを呼び出すようにデリゲートに要求します。</span><span class="sxs-lookup"><span data-stu-id="8d8c6-628">This call to the delegate prompts the delegate to call each method that is subscribed to the delegate.</span></span> <span data-ttu-id="8d8c6-629">サブスクライブされたメソッドは、デリゲートに追加されたのと同じ順序で呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="8d8c6-629">The subscribed methods are called in the same order in which they were added to the delegate.</span></span> <span data-ttu-id="8d8c6-630">1 つのサブスクライブされたメソッドは、そのデリゲードが次のメソッドを呼び出す前に完了される必要があります。</span><span class="sxs-lookup"><span data-stu-id="8d8c6-630">One subscribed method must be completed before the delegate calls the next method.</span></span> |





