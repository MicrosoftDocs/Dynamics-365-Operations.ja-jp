---
title: "クラスの拡張機能 - メソッドのラッピングとコマンド チェーン"
description: "このトピックでは、メソッド ラッピングを使用してパブリック メソッドと保護メソッドのビジネス ロジックを拡張する方法について説明します。"
author: robadawy
manager: AnnBe
ms.date: 09/28/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Developer
ms.reviewer: robinr
ms.search.scope: Operations
ms.search.region: Global
ms.author: robadawy
ms.search.validFrom: 2017-08-21
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7344f460fcb443a78b254e2387fbf5c9134bf674
ms.openlocfilehash: 8a5910bf0f839c9fa18a5b045f4df52dedffb8b7
ms.contentlocale: ja-jp
ms.lasthandoff: 09/28/2018

---

# <a name="class-extension-via-method-wrapping-and-chain-of-command-coc"></a><span data-ttu-id="67d5a-103">メソッドのラッピングとコマンド チェーン経由のクラスの拡張機能 (CoC)</span><span class="sxs-lookup"><span data-stu-id="67d5a-103">Class extension via method wrapping and Chain of Command (CoC)</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="67d5a-104">クラス拡張やクラス強化の機能が、Microsoft Dynamics 365 for Finance and Operations で強化されました。</span><span class="sxs-lookup"><span data-stu-id="67d5a-104">The functionality for class extension, or class augmentation, has been improved in Microsoft Dynamics 365 for Finance and Operations.</span></span> <span data-ttu-id="67d5a-105">強化対象である基本クラスで定義されたメソッド関連のロジックをラップできるようになりました。</span><span class="sxs-lookup"><span data-stu-id="67d5a-105">You can now wrap logic around methods that are defined in the base class that you're augmenting.</span></span> <span data-ttu-id="67d5a-106">イベント ハンドラーを使用せずに、パブリック メソッドとプロテクト メソッドのロジックを拡張することができます。</span><span class="sxs-lookup"><span data-stu-id="67d5a-106">You can extend the logic of public and protected methods without having to use event handlers.</span></span> <span data-ttu-id="67d5a-107">メソッドをラップするとき、基本クラスのパブリック メソッドと保護されたメソッド、および変数にもアクセスできます。</span><span class="sxs-lookup"><span data-stu-id="67d5a-107">When you wrap a method, you can also access public and protected methods, and variables of the base class.</span></span> <span data-ttu-id="67d5a-108">この方法で、トランザクションを開始し、クラスに関連付けられた状態変数を容易に管理することができます。</span><span class="sxs-lookup"><span data-stu-id="67d5a-108">In this way, you can start transactions and easily manage state variables that are associated with your class.</span></span>

<span data-ttu-id="67d5a-109">たとえば、モデルには次のコードが含まれています。</span><span class="sxs-lookup"><span data-stu-id="67d5a-109">For example, a model contains the following code.</span></span>

```
class BusinessLogic1
{
    str DoSomething(int arg) {
    …
    }
}
```

<span data-ttu-id="67d5a-110">同じメソッド名を再利用することにより、拡張クラス内の **DoSomething** メソッドの機能を強化することができるようになりました。</span><span class="sxs-lookup"><span data-stu-id="67d5a-110">You can now augment the functionality of the **DoSomething** method inside an extension class by reusing the same method name.</span></span> <span data-ttu-id="67d5a-111">拡張クラスは強化されたクラスが定義されているモデルを参照するパッケージに属している必要があります。</span><span class="sxs-lookup"><span data-stu-id="67d5a-111">An extension class must belong to a package that references the model where the augmented class is defined.</span></span>

```
[ExtensionOf(ClassStr(BusinessLogic1))]
final class BusinessLogic1_Extension
{
    str DoSomething(int arg) {
        // Part 1
        var s = next DoSomething(arg + 4);
        // Part 2
        return s;
    }
}
```


<span data-ttu-id="67d5a-112">この例では、**DoSomething** のラッパーと **next** キーワードを必要に応じて使用することにより、メソッドのコマンド チェーン (CoC) を作成します。</span><span class="sxs-lookup"><span data-stu-id="67d5a-112">In this example, the wrapper around **DoSomething** and the required use of the **next** keyword create a Chain of Command (CoC) for the method.</span></span> <span data-ttu-id="67d5a-113">CoC は、要求が一連の受信者によって処理される設計パターンです。</span><span class="sxs-lookup"><span data-stu-id="67d5a-113">CoC is a design pattern where a request is handled by a series of receivers.</span></span> <span data-ttu-id="67d5a-114">パターンは、送信者と受信者の疎結合をサポートします。</span><span class="sxs-lookup"><span data-stu-id="67d5a-114">The pattern supports loose coupling of the sender and the receivers.</span></span>

<span data-ttu-id="67d5a-115">現在は次のコードを実行します。</span><span class="sxs-lookup"><span data-stu-id="67d5a-115">We now run the following code.</span></span>

```
BusinessLogic1 c = new BusinessLogic1();
info(c.DoSomething(33));
```

<span data-ttu-id="67d5a-116">このコードが実行されると、システムは、**DoSomething** メソッドをラップするメソッドを検索します。</span><span class="sxs-lookup"><span data-stu-id="67d5a-116">When this code is run, the system finds any method that wraps the **DoSomething** method.</span></span> <span data-ttu-id="67d5a-117">システムは、**BusinessLogic1_Extension** クラスの **DoSomething** メソッドなど、これらのメソッドの 1 つをランダムに実行します。</span><span class="sxs-lookup"><span data-stu-id="67d5a-117">The system randomly runs one of these methods, such as the **DoSomething** method of the **BusinessLogic1_Extension** class.</span></span> <span data-ttu-id="67d5a-118">次の **DoSomething** メソッドへの呼び出しが発生すると、システムは CoC 内の別のメソッドをランダムに選択します。</span><span class="sxs-lookup"><span data-stu-id="67d5a-118">When the call to the next **DoSomething** method occurs, the system randomly picks another method in the CoC.</span></span> <span data-ttu-id="67d5a-119">ラップされたメソッドがこれ以上ない場合は、システムは元の実装を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="67d5a-119">If no more wrapped methods exist, the system calls the original implementation.</span></span>

## <a name="supported-versions"></a><span data-ttu-id="67d5a-120">サポートされているバージョン</span><span class="sxs-lookup"><span data-stu-id="67d5a-120">Supported versions</span></span>
> [!IMPORTANT]
> <span data-ttu-id="67d5a-121">このトピックで説明する機能 (CoC および保護されたメソッドと変数へのアクセス) は、Platform update 9 で利用できます。</span><span class="sxs-lookup"><span data-stu-id="67d5a-121">The functionality that is described in this topic (CoC and access to protected methods and variables) is available in Platform update 9.</span></span> <span data-ttu-id="67d5a-122">ただし、強化されているクラスは、プラットフォーム更新プログラム 9 またはそれ以降でコンパイルされる必要があります。</span><span class="sxs-lookup"><span data-stu-id="67d5a-122">However, the class that is being augmented must also be compiled on Platform update 9 or later.</span></span> <span data-ttu-id="67d5a-123">2017 年 8 月現在、Finance and Operations のアプリケーションの現在のリリースはすべて Platform Update 8 またはそれ以前でコンパイルされています。</span><span class="sxs-lookup"><span data-stu-id="67d5a-123">As of August 2017, all current releases of the applications for Finance and Operations have been compiled on Platform update 8 or earlier.</span></span> <span data-ttu-id="67d5a-124">したがって、基本パッケージ (Application Suite など) で定義されているメソッドをラップするには、プラットフォーム更新 9 以降でその基本パッケージを再コンパイルする必要があります。</span><span class="sxs-lookup"><span data-stu-id="67d5a-124">Therefore, to wrap a method that is defined in a base package (such as Application Suite), you must recompile that base package on Platform update 9 or later.</span></span>
<span data-ttu-id="67d5a-125">例: アプリケーション スイート モデルに存在するクラスを増補する独自の拡張モデルを作成し、CoC を使用している場合や保護されたメソッド/変数にアクセスする場合は、アプリケーション スイートと拡張モデルの両方を構築する必要があります。</span><span class="sxs-lookup"><span data-stu-id="67d5a-125">As an example: If you create your own extension model that is augmenting a class that exists in the Application Suite model, and if you are using CoC or accessing protected methods/variables, you will need to build both Application Suite and your extension model.</span></span> <span data-ttu-id="67d5a-126">ランタイム環境でこの機能を配置するには、両方のモデルを含む配置可能なパッケージを作成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="67d5a-126">You will also need to create a deployable package that includes both models in order to deploy this functionality on a runtime environment.</span></span>
<span data-ttu-id="67d5a-127">これは、Dynamics 365 for Finance and Operations アプリケーションの次のリリースまでの一時的な状況です。</span><span class="sxs-lookup"><span data-stu-id="67d5a-127">This is a temporary situation until the next release of the Dynamics 365 for Finance and Operations application.</span></span>

## <a name="capabilities"></a><span data-ttu-id="67d5a-128">処理能力</span><span class="sxs-lookup"><span data-stu-id="67d5a-128">Capabilities</span></span>
<span data-ttu-id="67d5a-129">次のセクションでは、ラッピング メソッドと CoC メソッドの機能について詳しく説明します。</span><span class="sxs-lookup"><span data-stu-id="67d5a-129">The following sections give more details about the capabilities of method wrapping and CoC.</span></span>

### <a name="wrapping-public-and-protected-methods"></a><span data-ttu-id="67d5a-130">パブリック メソッドと保護対象メソッドのラッピング</span><span class="sxs-lookup"><span data-stu-id="67d5a-130">Wrapping public and protected methods</span></span>
<span data-ttu-id="67d5a-131">クラス、テーブル、またはフォームの保護またはパブリック メソッドは、そのクラス、テーブル、またはフォームを補足する拡張子クラスを使用してラップできます。</span><span class="sxs-lookup"><span data-stu-id="67d5a-131">Protected or public methods of classes, tables, or forms can be wrapped by using an extension class that augments that class, table, or form.</span></span> <span data-ttu-id="67d5a-132">ラッパー メソッドは、基本メソッドと同じシグネチャを持つ必要があります。</span><span class="sxs-lookup"><span data-stu-id="67d5a-132">The wrapper method must have the same signature as the base method.</span></span>

- <span data-ttu-id="67d5a-133">フォーム クラスを拡張するときは、ルート レベルのメソッドのみをラップできます。</span><span class="sxs-lookup"><span data-stu-id="67d5a-133">When you augment form classes, only root-level methods can be wrapped.</span></span> <span data-ttu-id="67d5a-134">入れ子になったクラスで定義されているメソッドをラップすることはできません。</span><span class="sxs-lookup"><span data-stu-id="67d5a-134">You can't wrap methods that are defined in nested classes.</span></span>
- <span data-ttu-id="67d5a-135">通常のクラスで定義されているメソッドのみラップできます。</span><span class="sxs-lookup"><span data-stu-id="67d5a-135">Only methods that are defined in regular classes can be wrapped.</span></span> <span data-ttu-id="67d5a-136">拡張クラスで定義されているメソッドは、拡張クラスを強化してラップできません。</span><span class="sxs-lookup"><span data-stu-id="67d5a-136">Methods that are defined in extension classes can't be wrapped by augmenting the extension classes.</span></span>

### <a name="what-about-default-parameters"></a><span data-ttu-id="67d5a-137">既定のパラメーターはどうなのですか ?</span><span class="sxs-lookup"><span data-stu-id="67d5a-137">What about default parameters?</span></span>
<span data-ttu-id="67d5a-138">既定のパラメーターを持つメソッドは、拡張クラスでラップできます。</span><span class="sxs-lookup"><span data-stu-id="67d5a-138">Methods that have default parameters can be wrapped by extension classes.</span></span> <span data-ttu-id="67d5a-139">ただし、ラッパー メソッドのメソッド シグネチャは、パラメータの既定値を含む必要がありません。</span><span class="sxs-lookup"><span data-stu-id="67d5a-139">However, the method signature in the wrapper method must not include the default value of the parameter.</span></span>

<span data-ttu-id="67d5a-140">たとえば、次の簡単なクラスには、既定のパラメーターを持つメソッドがあります。</span><span class="sxs-lookup"><span data-stu-id="67d5a-140">For example, the following simple class has a method that has a default parameter.</span></span>

``` 
class Person 
{
    Public void salute( str message = "Hi"){ }
}
```

<span data-ttu-id="67d5a-141">この場合、ラッパー メソッドは次の例のようにする必要があります。</span><span class="sxs-lookup"><span data-stu-id="67d5a-141">In this case, the wrapper method must resemble the following example.</span></span>

```
[ExtensionOf(classtr(Person))]
final class aPerson_Extension
{
    Public void salute( str message ){ }
}
```

<span data-ttu-id="67d5a-142">**APerson_Extension** 拡張子クラスで、**salute** メソッドが**メッセージ** パラメーターの既定値に含まれていないことを確認します。</span><span class="sxs-lookup"><span data-stu-id="67d5a-142">In the **aPerson_Extension** extension class, notice that the **salute** method doesn't include the default value of the **message** parameter.</span></span> 

### <a name="wrapping-instance-and-static-methods"></a><span data-ttu-id="67d5a-143">インスタンス メソッドと静的メソッドをラッピング</span><span class="sxs-lookup"><span data-stu-id="67d5a-143">Wrapping instance and static methods</span></span>
<span data-ttu-id="67d5a-144">インスタンスと静的メソッドは、拡張クラスでラップできます。</span><span class="sxs-lookup"><span data-stu-id="67d5a-144">Instance and static methods can be wrapped by extension classes.</span></span> <span data-ttu-id="67d5a-145">静的メソッドがラップされるターゲットである場合、**静的**キーワードを使用して拡張内のメソッドを指定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="67d5a-145">If a static method is the target that will be wrapped, the method in the extension must be qualified by using the **static** keyword.</span></span>

<span data-ttu-id="67d5a-146">たとえば、次の **A** クラスがあります。</span><span class="sxs-lookup"><span data-stu-id="67d5a-146">For example, we have the following **A** class.</span></span>

```
class A 
{
    public static void aStaticMethod( int parameter1)
    {
    // …
    }
}
```
 
<span data-ttu-id="67d5a-147">この場合、ラッパー メソッドは次の例のようにする必要があります。</span><span class="sxs-lookup"><span data-stu-id="67d5a-147">In this case, the wrapper method must resemble the following example.</span></span>

```
[ExtensionOf(classstr(A)]
final class An_Extension
{
    public static void aStaticMethod( int parameter1)
    {
        Next aStaticMethod( 10 );
    }
}
```

> [!IMPORTANT]
> <span data-ttu-id="67d5a-148">静的メソッドをラップする機能はフォームには適用されません。</span><span class="sxs-lookup"><span data-stu-id="67d5a-148">The ability to wrap static methods doesn't apply to forms.</span></span> <span data-ttu-id="67d5a-149">X++ では、フォーム クラスは新しいクラスではなく、インスタンスを作成したり通常クラスとして参照したりできません。</span><span class="sxs-lookup"><span data-stu-id="67d5a-149">In X++, a form class isn't a new class, and can't be instantiated or referenced as a normal class.</span></span> <span data-ttu-id="67d5a-150">フォーム内の静的メソッドにはセマンティクスがありません。</span><span class="sxs-lookup"><span data-stu-id="67d5a-150">Static methods in forms don't have any semantics.</span></span>

### <a name="wrapper-methods-must-always-call-next"></a><span data-ttu-id="67d5a-151">ラッパー メソッドは常に次を呼び出す必要があります</span><span class="sxs-lookup"><span data-stu-id="67d5a-151">Wrapper methods must always call next</span></span> 

<span data-ttu-id="67d5a-152">拡張クラス内のラッパー メソッドは常に **次** を呼び出す必要があるため、チェーン内の次のメソッド、および最後には常に元の実装が呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="67d5a-152">Wrapper methods in an extension class must always call **next**, so that the next method in the chain and, finally, the original implementation are always called.</span></span> <span data-ttu-id="67d5a-153">この制限により、チェーン内のすべてのメソッドが結果に寄与することが保証されます。</span><span class="sxs-lookup"><span data-stu-id="67d5a-153">This restriction helps guarantee that every method in the chain contributes to the result.</span></span>

<span data-ttu-id="67d5a-154">この制限の現在の実装では、**次**の呼び出しはメソッド本体の第 1 レベルのステートメントである必要があります。</span><span class="sxs-lookup"><span data-stu-id="67d5a-154">In the current implementation of this restriction, the call to **next** must be in the first-level statements in the method body.</span></span>

<span data-ttu-id="67d5a-155">いくつかの重要なルールを次に示します。</span><span class="sxs-lookup"><span data-stu-id="67d5a-155">Here are some important rules:</span></span>

- <span data-ttu-id="67d5a-156">**if** 文の中で、条件付きで **next** への呼び出しを行うことはできません。</span><span class="sxs-lookup"><span data-stu-id="67d5a-156">Calls to **next** can't be done conditionally inside an **if** statement.</span></span> 
- <span data-ttu-id="67d5a-157">**while**、**do-while**、または **for** ループ ステートメント内で **next** への呼び出しを行うことはできません</span><span class="sxs-lookup"><span data-stu-id="67d5a-157">Calls to **next** can't be done in **while**, **do-while**, or **for** loop statements.</span></span> 
- <span data-ttu-id="67d5a-158">**次**ステートメントの前に、**戻る**ステートメントを置くことはできません。</span><span class="sxs-lookup"><span data-stu-id="67d5a-158">A **next** statement can't be preceded by a **return** statement.</span></span> 
- <span data-ttu-id="67d5a-159">論理式は最適化されているため、**次へ**の呼び出しは論理式では実行できません。</span><span class="sxs-lookup"><span data-stu-id="67d5a-159">Because logical expressions are optimized, calls to **next** can't occur in logical expressions.</span></span> <span data-ttu-id="67d5a-160">実行時に、完全な式の実行は保証されません。</span><span class="sxs-lookup"><span data-stu-id="67d5a-160">At runtime, the execution of the complete expression isn't guaranteed.</span></span>

> [!NOTE]
> <span data-ttu-id="67d5a-161">メソッドの元の実装の作成者は、次への呼び出しのスキップをラッパー メソッドに明示的に許可できます。</span><span class="sxs-lookup"><span data-stu-id="67d5a-161">The author of the original implementation of a method can explicitly allow wrapper methods to skip calling next.</span></span> <span data-ttu-id="67d5a-162">ラッピングしているメソッドが [置き換え可能な] 属性でタグされている場合は、**次の**キーワードを呼び出さずにこのメソッドをラップすることができます。</span><span class="sxs-lookup"><span data-stu-id="67d5a-162">If the method you are wrapping is tagged with the [Replaceable] attribute, an extension class can wrap this method without calling the **next** keyword.</span></span> <span data-ttu-id="67d5a-163">置き換え可能なメソッドは、カスタムの実装によって安全に "置き換える" ことができるロジックを実装するメソッドです。</span><span class="sxs-lookup"><span data-stu-id="67d5a-163">Replaceable methods are methods that implement logic that can safely be "replaced" by custom implementation.</span></span> <span data-ttu-id="67d5a-164">この機能は、Platform Update 11 のリリースで利用できます。</span><span class="sxs-lookup"><span data-stu-id="67d5a-164">This functionality is available with the release of Platform update 11.</span></span> 

### <a name="wrapping-a-base-method-in-an-extension-of-a-derived-class"></a><span data-ttu-id="67d5a-165">派生クラスの拡張で基本メソッドをラッピング</span><span class="sxs-lookup"><span data-stu-id="67d5a-165">Wrapping a base method in an extension of a derived class</span></span>
<span data-ttu-id="67d5a-166">次の例は、派生クラスの拡張機能で基準メソッドをラップする方法を示しています。</span><span class="sxs-lookup"><span data-stu-id="67d5a-166">The following example shows how to wrap a base method in an extension of a derived class.</span></span> <span data-ttu-id="67d5a-167">この例では、次のクラス階層が使用されます。</span><span class="sxs-lookup"><span data-stu-id="67d5a-167">For this example, the following class hierarchy is used.</span></span>

```
class A
{
    public void salute(str message)
    {
        Info(message);
    }
}

class B extends A { }
class C extends A { }
```

<span data-ttu-id="67d5a-168">したがって、1 つの基本クラス **A** があり、2 つのクラス **B** および **C** が **A** から派生します。ここに示すように、派生クラスの 1 つ (この場合は **B**) の拡張クラスを追加または作成します。</span><span class="sxs-lookup"><span data-stu-id="67d5a-168">Therefore, there is one base class, **A**. Two classes, **B** and **C**, are derived from **A**. We will augment or create an extension class of one of the derived classes (in this case, **B**), as shown here.</span></span>

```
[Extensionof(classstr(B))]
final class aB_Extension
{
    public void salute(str message)
    {
        next salute( message );
        Info("B extension");
    }
}
```

<span data-ttu-id="67d5a-169">**aB_Extension** クラスは **B** の拡張子ではあり、**B** は **salute** メソッドのメソッドの定義がありませんが、**salute** メソッドを基本クラス **A** で定義しラップすることができます。したがって、**B** クラスのインスタンスのみが **salute** メソッドのラッピングを含みます。</span><span class="sxs-lookup"><span data-stu-id="67d5a-169">Although the **aB_Extension** class is an extension of **B**, and **B** doesn't have a method definition for the **salute** method, you can wrap the **salute** method that is defined in the base class, **A**. Therefore, only instances of the **B** class will include the wrapping of the **salute** method.</span></span> <span data-ttu-id="67d5a-170">**A** クラスおよび **C** クラスのインスタンスは、**B** クラスの拡張機能に定義されているラッパー メソッドを呼び出すことはありません。</span><span class="sxs-lookup"><span data-stu-id="67d5a-170">Instances of the **A** and **C** classes will never call the wrapper method that is defined in the extension of the **B** class.</span></span> 

<span data-ttu-id="67d5a-171">これらの 3 つのクラスを使用するメソッドを実装すると、この動作はより明確になります。</span><span class="sxs-lookup"><span data-stu-id="67d5a-171">This behavior becomes clearer if we implement a method that uses these three classes.</span></span>

```
class ProgramTest 
{
    Public static void Main( Args _args)
    {
        var a = new A( );
        var b = new B( );
        var c = new C( );

        a.salute("Hi");
        b.salute("Hi");
        c.salute("Hi");
    }
}
```

<span data-ttu-id="67d5a-172">**a.salute(「Hi」)** および **c.salute(「Hi」)** の呼び出しでは、情報ログに「Hi」のメッセージのみが表示されます。</span><span class="sxs-lookup"><span data-stu-id="67d5a-172">For calls to **a.salute(“Hi”)** and **c.salute(“Hi”)**, the Infolog shows only the message “Hi.”</span></span> <span data-ttu-id="67d5a-173">ただし、**b.salute(「Hi」)** が呼び出されると、情報ログは「Hi」に続いて 「B 拡張子」を表示します。</span><span class="sxs-lookup"><span data-stu-id="67d5a-173">However, when **b.salute(“Hi”)** is called, the Infolog shows “Hi” followed by “B extension.”</span></span> 

<span data-ttu-id="67d5a-174">このメカニズムを使用することによって、特定の派生クラスに対してのみ元の方法をラップすることができます。</span><span class="sxs-lookup"><span data-stu-id="67d5a-174">By using this mechanism, you can wrap the original method only for specific derived classes.</span></span>

### <a name="accessing-protected-members-from-extension-classes"></a><span data-ttu-id="67d5a-175">拡張クラスから保護されたメンバーへのアクセス</span><span class="sxs-lookup"><span data-stu-id="67d5a-175">Accessing protected members from extension classes</span></span>
<span data-ttu-id="67d5a-176">プラットフォーム更新プログラム 9 では、拡張クラスから保護されたメンバーにアクセスできます。</span><span class="sxs-lookup"><span data-stu-id="67d5a-176">As of Platform update 9, you can access protected members from extension classes.</span></span> <span data-ttu-id="67d5a-177">これらの保護されたメンバーには、フィールドとメソッドが含まれます。</span><span class="sxs-lookup"><span data-stu-id="67d5a-177">These protected members include fields and methods.</span></span> <span data-ttu-id="67d5a-178">このサポートは、メソッドのラップに固有ではありませんが、クラス拡張内のすべてのメソッドを適用することに注意してください。</span><span class="sxs-lookup"><span data-stu-id="67d5a-178">Note that this support isn't specific to wrapping methods but applies all the methods in the class extension.</span></span> <span data-ttu-id="67d5a-179">したがって、クラス拡張は以前よりも強力です。</span><span class="sxs-lookup"><span data-stu-id="67d5a-179">Therefore, class extensions are more powerful than they were before.</span></span>

### <a name="the-hookable-attribute"></a><span data-ttu-id="67d5a-180">Hookable 属性</span><span class="sxs-lookup"><span data-stu-id="67d5a-180">The Hookable attribute</span></span>
<span data-ttu-id="67d5a-181">メソッドが **[Hookable(false)]** として明示的にマークされている場合、メソッドを拡張子クラスで囲むことはできません。</span><span class="sxs-lookup"><span data-stu-id="67d5a-181">If a method is explicitly marked as **[Hookable(false)]**, the method can't be wrapped in an extension class.</span></span> <span data-ttu-id="67d5a-182">次の例では、**anyMethod** は **anyClass1** を補強するクラスでラップできません。</span><span class="sxs-lookup"><span data-stu-id="67d5a-182">In the following example, **anyMethod** can't be wrapped in a class that augments **anyClass1**.</span></span>

```
class anyClass1 
{
    [HookableAttribute(false)]
    public void anyMethod() {…}
}
```

### <a name="final-methods-and-the-wrappable-attribute"></a><span data-ttu-id="67d5a-183">最終的な方法および Wrappable 属性</span><span class="sxs-lookup"><span data-stu-id="67d5a-183">Final methods and the Wrappable attribute</span></span>
<span data-ttu-id="67d5a-184">**final** とマークされているパブリック メソッドと保護されたメソッドは、拡張クラスでラップできません。</span><span class="sxs-lookup"><span data-stu-id="67d5a-184">Public and protected methods that are marked as **final** can't be wrapped in extension classes.</span></span> <span data-ttu-id="67d5a-185">**Wrappable** 属性を使用して属性パラメーターを **true** (**[Wrappable(true)]**) に設定することにより、この制限をオーバーライドすることができます。</span><span class="sxs-lookup"><span data-stu-id="67d5a-185">You can override this restriction by using the **Wrappable** attribute and setting the attribute parameter to **true** (**[Wrappable(true)]**).</span></span> <span data-ttu-id="67d5a-186">同様に、(最終ではない) パブリックまたは保護されたメソッドの既定の機能を無効にするには、折り返し不可としてこれらのメソッドをマークすることができます (**[Wrappable(false)]**)。</span><span class="sxs-lookup"><span data-stu-id="67d5a-186">Similarly, to override the default capability for (non-final) public or protected methods, you can mark those methods as non-wrappable (**[Wrappable(false)]**).</span></span>

<span data-ttu-id="67d5a-187">次の例では、**doSomething** メソッドは、パブリック メソッドである場合でもラップできないものとして明示的にマークされます。</span><span class="sxs-lookup"><span data-stu-id="67d5a-187">In the following example, the **doSomething** method is explicitly marked as non-wrappable, even though it's a public method.</span></span> <span data-ttu-id="67d5a-188">**doSomethingElse** メソッドは、最後のメソッドであっても、折り返し可能と明示的にマークされます。</span><span class="sxs-lookup"><span data-stu-id="67d5a-188">The **doSomethingElse** method is explicitly marked as wrappable, even though it's a final method.</span></span>

```
class anyClass2 
{
    [Wrappable(false)]
    public void  doSomething(str message) { …}

    [Wrappable(true)]
    final public void  doSomethingElse(str message){ …}
}
```

### <a name="extensions-of-form-nested-concepts-such-as-data-sources-data-fields-and-controls"></a><span data-ttu-id="67d5a-189">データ ソース、データ フィールド、および制御といったフォームで入れ子になった概念の拡張</span><span class="sxs-lookup"><span data-stu-id="67d5a-189">Extensions of form-nested concepts such as data sources, data fields, and controls</span></span>

<span data-ttu-id="67d5a-190">データ ソース、データ フィールド、コントロールなど、フォームで入れ子になった概念の CoC メソッドを実装するため、入れ子になった各概念には拡張クラスが必要です。</span><span class="sxs-lookup"><span data-stu-id="67d5a-190">In order to implement CoC methods for form-nested concepts, such as data sources, data fields, and controls, an extension class is required for each nested concept.</span></span> 

#### <a name="form-data-sources"></a><span data-ttu-id="67d5a-191">フォーム データ ソース</span><span class="sxs-lookup"><span data-stu-id="67d5a-191">Form data sources</span></span>

<span data-ttu-id="67d5a-192">この例では、**FormToExtend** はフォーム、**DataSource1** はフォームで有効な既存のデータ ソース、**init** と **validateWrite** はデータ ソースで折り返し可能なメソッドです。</span><span class="sxs-lookup"><span data-stu-id="67d5a-192">In this example, **FormToExtend** is the form, **DataSource1** is a valid existing data source in the form, and **init** and **validateWrite** are methods that can be wrapped in the data source.</span></span>

```C#
[ExtensionOf(formdatasourcestr(FormToExtend, DataSource1))]
final class FormDataSource1_Extension
{
    public void init()
    {
        next init();
        //...
    }
 
    public boolean validateWrite()
    {
        boolean ret;
        //...
        ret = next validateWrite();
        //...
```

#### <a name="form-data-fields"></a><span data-ttu-id="67d5a-193">フォーム データ フィールド</span><span class="sxs-lookup"><span data-stu-id="67d5a-193">Form data fields</span></span>

<span data-ttu-id="67d5a-194">この例では、データ フィールドが拡張されます。</span><span class="sxs-lookup"><span data-stu-id="67d5a-194">In this example, a data field is extended.</span></span> <span data-ttu-id="67d5a-195">**FormToExtend** はフォーム、**DataSource1** はフォームのデータ ソース、**Field1** はデータ ソースのフィールド、**validate** はこの入れ子になった概念で折り返し可能な多くのメソッドのいずれかです。</span><span class="sxs-lookup"><span data-stu-id="67d5a-195">**FormToExtend** is the form, **DataSource1** is a data source in the form, **Field1** is a field in the data source, and **validate** is one of many methods that can be wrapped in this nested concept.</span></span>

```C#
[ExtensionOf(formdatafieldstr(FormToExtend, DataSource1, Field1))]
final class FormDataField1_Extension 
{ 
public boolean validate()
{
    boolean ret
    //...
    ret = next validate();
    //...
```

#### <a name="controls"></a><span data-ttu-id="67d5a-196">コントロール</span><span class="sxs-lookup"><span data-stu-id="67d5a-196">Controls</span></span>

<span data-ttu-id="67d5a-197">この例では、**FormToExtend** はフォーム、**Button1** はフォーム内のボタン コントロール、**clicked** はボタン コントロールで折り返し可能なメソッドです。</span><span class="sxs-lookup"><span data-stu-id="67d5a-197">In this example, **FormToExtend** is the form, **Button1** is the button control in the form, and **clicked** is a method that can be wrapped on the button control.</span></span>

```C#
[ExtensionOf(formcontrolstr(FormToExtend, Button1))]
final class FormButton1_Extension
{
    public void clicked()
    {
        next clicked();
        //...
```

#### <a name="requirements-and-considerations-when-you-write-coc-methods-on-extensions-for-form-nested-concepts"></a><span data-ttu-id="67d5a-198">フォームで入れ子になった概念で CoC メソッドを書き込むときの要件と考慮事項</span><span class="sxs-lookup"><span data-stu-id="67d5a-198">Requirements and considerations when you write CoC methods on extensions for form-nested concepts</span></span>

- <span data-ttu-id="67d5a-199">その他の CoC メソッドと同様、これらのメソッドは常に **next** を呼び出してチェーン内の次のメソッドを呼び出す必要があります。これにより、チェーンは実行時の動作でカーネルまたはネイティブ実装まで進むことができます。</span><span class="sxs-lookup"><span data-stu-id="67d5a-199">Like other CoC methods, these methods must always call **next** to invoke the next method in the chain, so that the chain can go all the way to the kernel or native implementation in the runtime behavior.</span></span> <span data-ttu-id="67d5a-200">next の呼び出しは、ランタイムにおける基本の動作が常に正常に実行されることを保証する、フォーム自体からの **super()** の呼び出しに相当します。</span><span class="sxs-lookup"><span data-stu-id="67d5a-200">The call to next is equivalent to a call to **super()** from the form itself to help guarantee that the base behavior in the runtime is always run as expected.</span></span>
- <span data-ttu-id="67d5a-201">現時点では、Microsoft Visual Studio の X++ エディターは、折り返し可能なメソッドの検出をサポートしていません。</span><span class="sxs-lookup"><span data-stu-id="67d5a-201">Currently, the X++ editor in Microsoft Visual Studio doesn't support discovery of methods that can be wrapped.</span></span> <span data-ttu-id="67d5a-202">したがって、折り返し対象となるメソッドとその正確なシグネチャを識別するための入れ子になった各概念については、システムのドキュメントを参照する必要があります。</span><span class="sxs-lookup"><span data-stu-id="67d5a-202">Therefore, you must refer to the system documentation for each nested concept to identify the correct method to wrap and its exact signature.</span></span>
- <span data-ttu-id="67d5a-203">入れ子になったコントロール タイプの元の基本動作で定義されていないメソッドをラップする CoC を追加することは**できません**。</span><span class="sxs-lookup"><span data-stu-id="67d5a-203">You **cannot** add CoC to wrap methods that aren't defined in the original base behavior of the nested control type.</span></span> <span data-ttu-id="67d5a-204">たとえば、拡張において **methodInButton1** CoC を追加することはできません。</span><span class="sxs-lookup"><span data-stu-id="67d5a-204">For example, you can't add **methodInButton1** CoC on an extension.</span></span> <span data-ttu-id="67d5a-205">ただし、制御の拡張からは、メソッドがパブリックまたは保護として定義されている場合にこのメソッドへの呼び出しを行うことができます。</span><span class="sxs-lookup"><span data-stu-id="67d5a-205">However, from the control extension, you can make a call into this method if the method has been defined as public or protected.</span></span> <span data-ttu-id="67d5a-206">以下に、**methodInButton1** メソッドと同じように **Button1** コントロールが **FormToExtend** フォームで定義される例を示します。</span><span class="sxs-lookup"><span data-stu-id="67d5a-206">Here is an example where the **Button1** control is defined in the **FormToExtend** form in such a way that it has the **methodInButton1** method.</span></span>

    ```C#
    [Form]
    public class FormToExtend extends FormRun
    {
        [Control("Button")]
        class Button1
        {
            public void methodInButton1 (str param1)
            {
                Info("Hi from methodInButton1");
                //...
    }
    ```

- <span data-ttu-id="67d5a-207">拡張からのそのフォームで入れ子になった概念における CoC メソッドをサポートするために元のフォームが定義されたモジュールを再コンパイルする必要は**ありません**。</span><span class="sxs-lookup"><span data-stu-id="67d5a-207">You do **not** have to recompile the module where the original form is defined to support CoC methods on nested concepts on that form from an extension.</span></span> <span data-ttu-id="67d5a-208">たとえば、前の例の **FormToExtend** フォームが **ApplicationSuite** モジュールにある場合、異なるモジュールからそのフォームで入れ子になった概念の CoC で拡張するために **ApplicationSuite** を再コンパイルする必要はありません。</span><span class="sxs-lookup"><span data-stu-id="67d5a-208">For example, if the **FormToExtend** form from the previous examples is in the **ApplicationSuite** module, you don't have to recompile **ApplicationSuite** to extend it with CoC for nested concepts on that form from a different module.</span></span>

## <a name="restrictions-on-wrapper-methods"></a><span data-ttu-id="67d5a-209">ラッパー メソッドに関する制限事項</span><span class="sxs-lookup"><span data-stu-id="67d5a-209">Restrictions on wrapper methods</span></span>
<span data-ttu-id="67d5a-210">次のセクションでは、CoC およびメソッド ラッピングの使用上の制限について説明します。</span><span class="sxs-lookup"><span data-stu-id="67d5a-210">The following sections describe restrictions on the use of CoC and method wrapping.</span></span>

### <a name="kernel-methods-cant-be-wrapped"></a><span data-ttu-id="67d5a-211">カーネル メソッドをラップすることはできません。</span><span class="sxs-lookup"><span data-stu-id="67d5a-211">Kernel methods can't be wrapped</span></span>
<span data-ttu-id="67d5a-212">カーネル クラスは、X++ クラスではありません。</span><span class="sxs-lookup"><span data-stu-id="67d5a-212">Kernel classes aren't X++ classes.</span></span> <span data-ttu-id="67d5a-213">代わりに、それらは Microsoft Dynamics 365 Unified Operations プラットフォームのカーネルで定義されているクラスです。</span><span class="sxs-lookup"><span data-stu-id="67d5a-213">Instead, they are classes that are defined in the kernel of the Microsoft Dynamics 365 Unified Operations platform.</span></span> <span data-ttu-id="67d5a-214">拡張子クラスはカーネルクラスでサポートされていますが、カーネルクラスのメソッドではメソッドのラッピングはサポートされません。</span><span class="sxs-lookup"><span data-stu-id="67d5a-214">Even though extension classes are supported for kernel classes, method wrapping isn't supported for methods of kernel classes.</span></span> <span data-ttu-id="67d5a-215">つまり、メソッドをラップする場合、基準メソッドは X++ メソッドである必要があります。</span><span class="sxs-lookup"><span data-stu-id="67d5a-215">In other words, if you want to wrap a method, the base method must be an X++ method.</span></span>

### <a name="x-classes-that-are-compiled-by-using-platform-update-8-or-earlier"></a><span data-ttu-id="67d5a-216">プラットフォーム更新プログラム 8 またはそれ以前を使用してコンパイルされた X++ クラス</span><span class="sxs-lookup"><span data-stu-id="67d5a-216">X++ classes that are compiled by using Platform update 8 or earlier</span></span> 
<span data-ttu-id="67d5a-217">メソッドのラッピング機能には、プラットフォーム update 9 以降の一部である X++ コンパイラによって出力される特定の機能が必要です。</span><span class="sxs-lookup"><span data-stu-id="67d5a-217">The method wrapping feature requires specific functionality that is emitted by an X++ compiler that is part of Platform update 9 or later.</span></span> <span data-ttu-id="67d5a-218">以前のバージョンを使用してコンパイルされたメソッドには、この機能をサポートするインフラストラクチャはありません。</span><span class="sxs-lookup"><span data-stu-id="67d5a-218">Methods that are compiled by using earlier versions don't have the infrastructure to support this feature.</span></span>

### <a name="nested-class-methods-in-forms-can-be-wrapped-in-platform-update-16-or-later"></a><span data-ttu-id="67d5a-219">プラットフォーム更新 16 以降ではフォームで入れ子になったクラス メソッドをラップ可能を参照してください</span><span class="sxs-lookup"><span data-stu-id="67d5a-219">Nested class methods in forms can be wrapped in Platform update 16 or later</span></span>
<span data-ttu-id="67d5a-220">クラス拡張を使用して入れ子になったクラスでメソッドをラップする機能がプラットフォーム更新 16 で追加されました。</span><span class="sxs-lookup"><span data-stu-id="67d5a-220">The ability to wrap methods in nested classes by using class extensions was added in Platform update 16.</span></span> <span data-ttu-id="67d5a-221">X++ の入れ子になったクラスの概念は、データソース メソッドやフォームコ ントロール メソッドを上書きするためのフォームに適用されます。</span><span class="sxs-lookup"><span data-stu-id="67d5a-221">The concept of nested classes in X++ applies to forms for overriding data source methods and form control methods.</span></span>

### <a name="tooling"></a><span data-ttu-id="67d5a-222">ツール</span><span class="sxs-lookup"><span data-stu-id="67d5a-222">Tooling</span></span>
<span data-ttu-id="67d5a-223">このトピックに記載されている機能については、Microsoft Visual Studio X++ エディターは、相互参照および Microsoft IntelliSense の完全なサポートまだ提供していません。</span><span class="sxs-lookup"><span data-stu-id="67d5a-223">For the features that are described in this topic, the Microsoft Visual Studio X++ editor doesn't yet offer complete support for cross-references and Microsoft IntelliSense.</span></span> <span data-ttu-id="67d5a-224">Dynamics 365 for Finance and Operations プラットフォーム更新プログラム 10 で完全なサポートが利用できるようにする予定です。</span><span class="sxs-lookup"><span data-stu-id="67d5a-224">We plan to make complete support available in Dynamics 365 for Finance and Operations Platform update 10.</span></span>

