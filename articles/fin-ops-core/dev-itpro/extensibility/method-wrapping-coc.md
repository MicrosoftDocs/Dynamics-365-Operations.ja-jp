---
title: クラスの拡張機能 - メソッドのラッピングとコマンド チェーン
description: このトピックでは、メソッド ラッピングを使用してパブリック メソッドと保護メソッドのビジネス ロジックを拡張する方法について説明します。
author: ChrisGarty
manager: AnnBe
ms.date: 12/18/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Developer
ms.reviewer: rhaertle
ms.search.scope: Operations
ms.search.region: Global
ms.author: cgarty
ms.search.validFrom: 2017-08-21
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 08b455599e0f903e8744ca35d74fcc429111960e
ms.sourcegitcommit: 9f90b194c0fc751d866d3d24d57ecf1b3c5053a1
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/07/2020
ms.locfileid: "3033022"
---
# <a name="class-extension---method-wrapping-and-chain-of-command"></a><span data-ttu-id="4a2ad-103">クラスの拡張機能 - メソッドのラッピングとコマンド チェーン</span><span class="sxs-lookup"><span data-stu-id="4a2ad-103">Class extension - Method wrapping and Chain of Command</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="4a2ad-104">クラス拡張やクラス強化の機能が強化されました。</span><span class="sxs-lookup"><span data-stu-id="4a2ad-104">The functionality for class extension, or class augmentation, has been improved.</span></span> <span data-ttu-id="4a2ad-105">強化対象である基本クラスで定義されたメソッド関連のロジックをラップできるようになりました。</span><span class="sxs-lookup"><span data-stu-id="4a2ad-105">You can now wrap logic around methods that are defined in the base class that you're augmenting.</span></span> <span data-ttu-id="4a2ad-106">イベント ハンドラーを使用せずに、パブリック メソッドとプロテクト メソッドのロジックを拡張することができます。</span><span class="sxs-lookup"><span data-stu-id="4a2ad-106">You can extend the logic of public and protected methods without having to use event handlers.</span></span> <span data-ttu-id="4a2ad-107">メソッドをラップするとき、基本クラスのパブリック メソッドと保護されたメソッド、および変数にもアクセスできます。</span><span class="sxs-lookup"><span data-stu-id="4a2ad-107">When you wrap a method, you can also access public and protected methods, and variables of the base class.</span></span> <span data-ttu-id="4a2ad-108">この方法で、トランザクションを開始し、クラスに関連付けられた状態変数を容易に管理することができます。</span><span class="sxs-lookup"><span data-stu-id="4a2ad-108">In this way, you can start transactions and easily manage state variables that are associated with your class.</span></span>

<span data-ttu-id="4a2ad-109">たとえば、モデルには次のコードが含まれています。</span><span class="sxs-lookup"><span data-stu-id="4a2ad-109">For example, a model contains the following code.</span></span>

```xpp
class BusinessLogic1
{
    str doSomething(int arg) 
    {
        // ...
    }
}
```

<span data-ttu-id="4a2ad-110">同じメソッド名を再利用することにより、拡張クラス内の **doSomething** メソッドの機能を強化することができるようになりました。</span><span class="sxs-lookup"><span data-stu-id="4a2ad-110">You can now augment the functionality of the **doSomething** method inside an extension class by reusing the same method name.</span></span> <span data-ttu-id="4a2ad-111">拡張クラスは強化されたクラスが定義されているモデルを参照するパッケージに属している必要があります。</span><span class="sxs-lookup"><span data-stu-id="4a2ad-111">An extension class must belong to a package that references the model where the augmented class is defined.</span></span>

```xpp
[ExtensionOf(classStr(BusinessLogic1))]
final class BusinessLogic1_Extension
{
    str doSomething(int arg) 
    {
        // Part 1
        var s = next doSomething(arg + 4);
        // Part 2
        return s;
    }
}
```


<span data-ttu-id="4a2ad-112">この例では、**doSomething** のラッパーと **next** キーワードを必要に応じて使用することにより、メソッドのコマンド チェーン (CoC) を作成します。</span><span class="sxs-lookup"><span data-stu-id="4a2ad-112">In this example, the wrapper around **doSomething** and the required use of the **next** keyword create a Chain of Command (CoC) for the method.</span></span> <span data-ttu-id="4a2ad-113">CoC は、要求が一連の受信者によって処理される設計パターンです。</span><span class="sxs-lookup"><span data-stu-id="4a2ad-113">CoC is a design pattern where a request is handled by a series of receivers.</span></span> <span data-ttu-id="4a2ad-114">パターンは、送信者と受信者の疎結合をサポートします。</span><span class="sxs-lookup"><span data-stu-id="4a2ad-114">The pattern supports loose coupling of the sender and the receivers.</span></span>

<span data-ttu-id="4a2ad-115">現在は次のコードを実行します。</span><span class="sxs-lookup"><span data-stu-id="4a2ad-115">We now run the following code.</span></span>

```xpp
BusinessLogic1 object = new BusinessLogic1();
info(object.doSomething(33));
```

<span data-ttu-id="4a2ad-116">このコードが実行されると、システムは、**doSomething** メソッドをラップするメソッドを検索します。</span><span class="sxs-lookup"><span data-stu-id="4a2ad-116">When this code is run, the system finds any method that wraps the **doSomething** method.</span></span> <span data-ttu-id="4a2ad-117">システムは、**BusinessLogic1_Extension** クラスの **doSomething** メソッドなど、これらのメソッドの 1 つをランダムに実行します。</span><span class="sxs-lookup"><span data-stu-id="4a2ad-117">The system randomly runs one of these methods, such as the **doSomething** method of the **BusinessLogic1_Extension** class.</span></span> <span data-ttu-id="4a2ad-118">次の **doSomething** メソッドへの呼び出しが発生すると、システムは CoC 内の別のメソッドをランダムに選択します。</span><span class="sxs-lookup"><span data-stu-id="4a2ad-118">When the call to the next **doSomething** method occurs, the system randomly picks another method in the CoC.</span></span> <span data-ttu-id="4a2ad-119">ラップされたメソッドがこれ以上ない場合は、システムは元の実装を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="4a2ad-119">If no more wrapped methods exist, the system calls the original implementation.</span></span>

## <a name="supported-versions"></a><span data-ttu-id="4a2ad-120">サポートされているバージョン</span><span class="sxs-lookup"><span data-stu-id="4a2ad-120">Supported versions</span></span>
> [!IMPORTANT]
> <span data-ttu-id="4a2ad-121">このトピックで説明する機能 (CoC および保護されたメソッドと変数へのアクセス) は、Platform update 9 で利用できます。</span><span class="sxs-lookup"><span data-stu-id="4a2ad-121">The functionality that is described in this topic (CoC and access to protected methods and variables) is available in Platform update 9.</span></span> <span data-ttu-id="4a2ad-122">ただし、強化されているクラスは、プラットフォーム更新プログラム 9 またはそれ以降でコンパイルされる必要があります。</span><span class="sxs-lookup"><span data-stu-id="4a2ad-122">However, the class that is being augmented must also be compiled on Platform update 9 or later.</span></span> <span data-ttu-id="4a2ad-123">2017 年 8 月現在、Finance and Operations のアプリケーションの現在のリリースはすべてプラットフォーム更新プログラム 8 またはそれ以前でコンパイルされています。</span><span class="sxs-lookup"><span data-stu-id="4a2ad-123">As of August 2017, all current releases of the applications for Finance and Operations have been compiled on Platform update 8 or earlier.</span></span> <span data-ttu-id="4a2ad-124">したがって、基本パッケージ (Application Suite など) で定義されているメソッドをラップするには、プラットフォーム更新 9 以降でその基本パッケージを再コンパイルする必要があります。</span><span class="sxs-lookup"><span data-stu-id="4a2ad-124">Therefore, to wrap a method that is defined in a base package (such as Application Suite), you must recompile that base package on Platform update 9 or later.</span></span>
<span data-ttu-id="4a2ad-125">例: アプリケーション スイート モデルに存在するクラスを増補する独自の拡張モデルを作成し、CoC を使用している場合や保護されたメソッド/変数にアクセスする場合は、アプリケーション スイートと拡張モデルの両方を構築する必要があります。</span><span class="sxs-lookup"><span data-stu-id="4a2ad-125">As an example: If you create your own extension model that is augmenting a class that exists in the Application Suite model, and if you are using CoC or accessing protected methods/variables, you will need to build both Application Suite and your extension model.</span></span> <span data-ttu-id="4a2ad-126">ランタイム環境でこの機能を配置するには、両方のモデルを含む配置可能なパッケージを作成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="4a2ad-126">You will also need to create a deployable package that includes both models in order to deploy this functionality on a runtime environment.</span></span>

## <a name="capabilities"></a><span data-ttu-id="4a2ad-127">処理能力</span><span class="sxs-lookup"><span data-stu-id="4a2ad-127">Capabilities</span></span>
<span data-ttu-id="4a2ad-128">次のセクションでは、ラッピング メソッドと CoC メソッドの機能について詳しく説明します。</span><span class="sxs-lookup"><span data-stu-id="4a2ad-128">The following sections give more details about the capabilities of method wrapping and CoC.</span></span>

### <a name="wrapping-public-and-protected-methods"></a><span data-ttu-id="4a2ad-129">パブリック メソッドと保護対象メソッドのラッピング</span><span class="sxs-lookup"><span data-stu-id="4a2ad-129">Wrapping public and protected methods</span></span>
<span data-ttu-id="4a2ad-130">クラス、テーブル、データ エンティティ、またはフォームの保護またはパブリック メソッドは、拡張子クラスを使用してラップできます。</span><span class="sxs-lookup"><span data-stu-id="4a2ad-130">Protected or public methods of classes, tables, data entities, or forms can be wrapped by using an extension class.</span></span> <span data-ttu-id="4a2ad-131">ラッパー メソッドは、基本メソッドと同じシグネチャを持つ必要があります。</span><span class="sxs-lookup"><span data-stu-id="4a2ad-131">The wrapper method must have the same signature as the base method.</span></span>

- <span data-ttu-id="4a2ad-132">フォーム クラスを拡張するときは、ルート レベルのメソッドのみをラップできます。</span><span class="sxs-lookup"><span data-stu-id="4a2ad-132">When you augment form classes, only root-level methods can be wrapped.</span></span> <span data-ttu-id="4a2ad-133">入れ子になったクラスで定義されているメソッドをラップすることはできません。</span><span class="sxs-lookup"><span data-stu-id="4a2ad-133">You can't wrap methods that are defined in nested classes.</span></span>
- <span data-ttu-id="4a2ad-134">現在のところ、通常のクラスで定義されているメソッドのみラップできます。</span><span class="sxs-lookup"><span data-stu-id="4a2ad-134">Currently, only methods that are defined in regular classes can be wrapped.</span></span> <span data-ttu-id="4a2ad-135">拡張クラスで定義されているメソッドは、拡張クラスを強化してラップできません。</span><span class="sxs-lookup"><span data-stu-id="4a2ad-135">Methods that are defined in extension classes can't be wrapped by augmenting the extension classes.</span></span> <span data-ttu-id="4a2ad-136">この機能は、将来の更新で計画されています。</span><span class="sxs-lookup"><span data-stu-id="4a2ad-136">This capability is planned for a future update.</span></span>

### <a name="what-about-default-parameters"></a><span data-ttu-id="4a2ad-137">既定のパラメーターはどうなのですか ?</span><span class="sxs-lookup"><span data-stu-id="4a2ad-137">What about default parameters?</span></span>
<span data-ttu-id="4a2ad-138">既定のパラメーターを持つメソッドは、拡張クラスでラップできます。</span><span class="sxs-lookup"><span data-stu-id="4a2ad-138">Methods that have default parameters can be wrapped by extension classes.</span></span> <span data-ttu-id="4a2ad-139">ただし、ラッパー メソッドのメソッド シグネチャは、パラメータの既定値を含む必要がありません。</span><span class="sxs-lookup"><span data-stu-id="4a2ad-139">However, the method signature in the wrapper method must not include the default value of the parameter.</span></span>

<span data-ttu-id="4a2ad-140">たとえば、次の簡単なクラスには、既定のパラメーターを持つメソッドがあります。</span><span class="sxs-lookup"><span data-stu-id="4a2ad-140">For example, the following simple class has a method that has a default parameter.</span></span>

```xpp
class Person 
{
    public void salute(str message = "Hi") {...}
}
```

<span data-ttu-id="4a2ad-141">この場合、ラッパー メソッドは次の例のようにする必要があります。</span><span class="sxs-lookup"><span data-stu-id="4a2ad-141">In this case, the wrapper method must resemble the following example.</span></span>

```xpp
[ExtensionOf(classStr(Person))]
final class APerson_Extension
{
    public void salute(str message)
    {
        // ...
    }
}
```

<span data-ttu-id="4a2ad-142">**APerson_Extension** 拡張子クラスで、**salute** メソッドが**メッセージ** パラメーターの既定値に含まれていないことを確認します。</span><span class="sxs-lookup"><span data-stu-id="4a2ad-142">In the **APerson_Extension** extension class, notice that the **salute** method doesn't include the default value of the **message** parameter.</span></span> 

### <a name="wrapping-instance-and-static-methods"></a><span data-ttu-id="4a2ad-143">インスタンス メソッドと静的メソッドをラッピング</span><span class="sxs-lookup"><span data-stu-id="4a2ad-143">Wrapping instance and static methods</span></span>
<span data-ttu-id="4a2ad-144">インスタンスと静的メソッドは、拡張クラスでラップできます。</span><span class="sxs-lookup"><span data-stu-id="4a2ad-144">Instance and static methods can be wrapped by extension classes.</span></span> <span data-ttu-id="4a2ad-145">静的メソッドがラップされるターゲットである場合、**静的**キーワードを使用して拡張内のメソッドを指定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="4a2ad-145">If a static method is the target that will be wrapped, the method in the extension must be qualified by using the **static** keyword.</span></span>

<span data-ttu-id="4a2ad-146">たとえば、次の **A** クラスがあります。</span><span class="sxs-lookup"><span data-stu-id="4a2ad-146">For example, we have the following **A** class.</span></span>

```xpp
class A 
{
    public static void aStaticMethod(int parameter1)
    {
        // ...
    }
}
```
 
<span data-ttu-id="4a2ad-147">この場合、ラッパー メソッドは次の例のようにする必要があります。</span><span class="sxs-lookup"><span data-stu-id="4a2ad-147">In this case, the wrapper method must resemble the following example.</span></span>

```xpp
[ExtensionOf(classStr(A)]
final class An_Extension
{
    public static void aStaticMethod(int parameter1)
    {
        // ...
        next aStaticMethod(parameter1);
    }
}
```

> [!IMPORTANT]
> <span data-ttu-id="4a2ad-148">静的メソッドをラップする機能はフォームには適用されません。</span><span class="sxs-lookup"><span data-stu-id="4a2ad-148">The ability to wrap static methods doesn't apply to forms.</span></span> <span data-ttu-id="4a2ad-149">X++ では、フォーム クラスは新しいクラスではなく、インスタンスを作成したり通常クラスとして参照したりできません。</span><span class="sxs-lookup"><span data-stu-id="4a2ad-149">In X++, a form class isn't a new class, and can't be instantiated or referenced as a normal class.</span></span> <span data-ttu-id="4a2ad-150">フォーム内の静的メソッドにはセマンティクスがありません。</span><span class="sxs-lookup"><span data-stu-id="4a2ad-150">Static methods in forms don't have any semantics.</span></span>

### <a name="wrapper-methods-must-always-call-next"></a><span data-ttu-id="4a2ad-151">ラッパー メソッドは常に次を呼び出す必要があります</span><span class="sxs-lookup"><span data-stu-id="4a2ad-151">Wrapper methods must always call next</span></span> 

<span data-ttu-id="4a2ad-152">拡張クラス内のラッパー メソッドは常に **次** を呼び出す必要があるため、チェーン内の次のメソッド、および最後には常に元の実装が呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="4a2ad-152">Wrapper methods in an extension class must always call **next**, so that the next method in the chain and, finally, the original implementation are always called.</span></span> <span data-ttu-id="4a2ad-153">この制限により、チェーン内のすべてのメソッドが結果に寄与することが保証されます。</span><span class="sxs-lookup"><span data-stu-id="4a2ad-153">This restriction helps guarantee that every method in the chain contributes to the result.</span></span>

<span data-ttu-id="4a2ad-154">この制限の現在の実装では、**次**の呼び出しはメソッド本体の第 1 レベルのステートメントである必要があります。</span><span class="sxs-lookup"><span data-stu-id="4a2ad-154">In the current implementation of this restriction, the call to **next** must be in the first-level statements in the method body.</span></span>

<span data-ttu-id="4a2ad-155">いくつかの重要なルールを次に示します。</span><span class="sxs-lookup"><span data-stu-id="4a2ad-155">Here are some important rules:</span></span>

- <span data-ttu-id="4a2ad-156">**if** 文の中で、条件付きで **next** への呼び出しを行うことはできません。</span><span class="sxs-lookup"><span data-stu-id="4a2ad-156">Calls to **next** can't be done conditionally inside an **if** statement.</span></span> 
- <span data-ttu-id="4a2ad-157">**while**、**do-while**、または **for** ループ ステートメント内で **next** への呼び出しを行うことはできません</span><span class="sxs-lookup"><span data-stu-id="4a2ad-157">Calls to **next** can't be done in **while**, **do-while**, or **for** loop statements.</span></span> 
- <span data-ttu-id="4a2ad-158">**次**ステートメントの前に、**戻る**ステートメントを置くことはできません。</span><span class="sxs-lookup"><span data-stu-id="4a2ad-158">A **next** statement can't be preceded by a **return** statement.</span></span> 
- <span data-ttu-id="4a2ad-159">論理式は最適化されているため、**次へ**の呼び出しは論理式では実行できません。</span><span class="sxs-lookup"><span data-stu-id="4a2ad-159">Because logical expressions are optimized, calls to **next** can't occur in logical expressions.</span></span> <span data-ttu-id="4a2ad-160">実行時に、完全な式の実行は保証されません。</span><span class="sxs-lookup"><span data-stu-id="4a2ad-160">At runtime, the execution of the complete expression isn't guaranteed.</span></span>

> [!NOTE]
> <span data-ttu-id="4a2ad-161">メソッドが置き換え可能な場合は、拡張担当者はコマンド チェーンを使用してメソッドをラップするときに無条件に **next** を呼び出す必要はありません。</span><span class="sxs-lookup"><span data-stu-id="4a2ad-161">If a method is replaceable, extenders don't have to unconditionally call **next** when wrapping the method by using chain of command.</span></span> <span data-ttu-id="4a2ad-162">拡張担当者はチェーンを中断できますが、条件がある場合のみ中断することが期待されます。</span><span class="sxs-lookup"><span data-stu-id="4a2ad-162">Although extenders can break the chain, the expectation is that they will only conditionally break it.</span></span> <span data-ttu-id="4a2ad-163">コンパイラは、属性 **Replaceable** を持つメソッドの **next** の呼び出しを強制しません。</span><span class="sxs-lookup"><span data-stu-id="4a2ad-163">The compiler doesn't enforce calls to **next** for methods with the attribute, **Replaceable**.</span></span>  

### <a name="wrapping-a-base-method-in-an-extension-of-a-derived-class"></a><span data-ttu-id="4a2ad-164">派生クラスの拡張で基本メソッドをラッピング</span><span class="sxs-lookup"><span data-stu-id="4a2ad-164">Wrapping a base method in an extension of a derived class</span></span>
<span data-ttu-id="4a2ad-165">次の例は、派生クラスの拡張機能で基準メソッドをラップする方法を示しています。</span><span class="sxs-lookup"><span data-stu-id="4a2ad-165">The following example shows how to wrap a base method in an extension of a derived class.</span></span> <span data-ttu-id="4a2ad-166">この例では、次のクラス階層が使用されます。</span><span class="sxs-lookup"><span data-stu-id="4a2ad-166">For this example, the following class hierarchy is used.</span></span>

```xpp
class A
{
    public void salute(str message)
    {   
        info(message);
    }
}

class B extends A {}
class C extends A {}
```

<span data-ttu-id="4a2ad-167">したがって、1 つの基本クラス **A** があり、2 つのクラス **B** および **C** が **A** から派生します。ここに示すように、派生クラスの 1 つ (この場合は **B**) の拡張クラスを追加または作成します。</span><span class="sxs-lookup"><span data-stu-id="4a2ad-167">Therefore, there is one base class, **A**. Two classes, **B** and **C**, are derived from **A**. We will augment or create an extension class of one of the derived classes (in this case, **B**), as shown here.</span></span>

```xpp
[ExtensionOf(classStr(B))]
final class B_Extension
{
    public void salute(str message)
    {
        next salute(message);
        info("B extension");
    }
}
```

<span data-ttu-id="4a2ad-168">**B_Extension** クラスは **B** の拡張子ではあり、**B** は **salute** メソッドのメソッドの定義がありませんが、**salute** メソッドを基本クラス **A** で定義しラップすることができます。したがって、**B** クラスのインスタンスのみが **salute** メソッドのラッピングを含みます。</span><span class="sxs-lookup"><span data-stu-id="4a2ad-168">Although the **B_Extension** class is an extension of **B**, and **B** doesn't have a method definition for the **salute** method, you can wrap the **salute** method that is defined in the base class, **A**. Therefore, only instances of the **B** class will include the wrapping of the **salute** method.</span></span> <span data-ttu-id="4a2ad-169">**A** クラスおよび **C** クラスのインスタンスは、**B** クラスの拡張機能に定義されているラッパー メソッドを呼び出すことはありません。</span><span class="sxs-lookup"><span data-stu-id="4a2ad-169">Instances of the **A** and **C** classes will never call the wrapper method that is defined in the extension of the **B** class.</span></span> 

<span data-ttu-id="4a2ad-170">これらの 3 つのクラスを使用するメソッドを実装すると、この動作はより明確になります。</span><span class="sxs-lookup"><span data-stu-id="4a2ad-170">This behavior becomes clearer if we implement a method that uses these three classes.</span></span>

```xpp
class ProgramTest 
{
    public static void main(Args args)
    {
        var a = new A();
        var b = new B();
        var c = new C();

        a.salute("Hi");
        b.salute("Hi");
        c.salute("Hi");
    }
}
```

<span data-ttu-id="4a2ad-171">**a.salute(「Hi」)** および **c.salute(「Hi」)** の呼び出しでは、情報ログに「Hi」のメッセージのみが表示されます。</span><span class="sxs-lookup"><span data-stu-id="4a2ad-171">For calls to **a.salute(“Hi”)** and **c.salute(“Hi”)**, the Infolog shows only the message “Hi.”</span></span> <span data-ttu-id="4a2ad-172">ただし、**b.salute(「Hi」)** が呼び出されると、情報ログは「Hi」に続いて 「B 拡張子」を表示します。</span><span class="sxs-lookup"><span data-stu-id="4a2ad-172">However, when **b.salute(“Hi”)** is called, the Infolog shows “Hi” followed by “B extension.”</span></span> 

<span data-ttu-id="4a2ad-173">このメカニズムを使用することによって、特定の派生クラスに対してのみ元の方法をラップすることができます。</span><span class="sxs-lookup"><span data-stu-id="4a2ad-173">By using this mechanism, you can wrap the original method only for specific derived classes.</span></span>

### <a name="accessing-protected-members-from-extension-classes"></a><span data-ttu-id="4a2ad-174">拡張クラスから保護されたメンバーへのアクセス</span><span class="sxs-lookup"><span data-stu-id="4a2ad-174">Accessing protected members from extension classes</span></span>
<span data-ttu-id="4a2ad-175">プラットフォーム更新プログラム 9 では、拡張クラスから保護されたメンバーにアクセスできます。</span><span class="sxs-lookup"><span data-stu-id="4a2ad-175">As of Platform update 9, you can access protected members from extension classes.</span></span> <span data-ttu-id="4a2ad-176">これらの保護されたメンバーには、フィールドとメソッドが含まれます。</span><span class="sxs-lookup"><span data-stu-id="4a2ad-176">These protected members include fields and methods.</span></span> <span data-ttu-id="4a2ad-177">このサポートは、メソッドのラップに固有ではありませんが、クラス拡張内のすべてのメソッドを適用することに注意してください。</span><span class="sxs-lookup"><span data-stu-id="4a2ad-177">Note that this support isn't specific to wrapping methods but applies all the methods in the class extension.</span></span> <span data-ttu-id="4a2ad-178">したがって、クラス拡張は以前よりも強力です。</span><span class="sxs-lookup"><span data-stu-id="4a2ad-178">Therefore, class extensions are more powerful than they were before.</span></span>

### <a name="the-hookable-attribute"></a><span data-ttu-id="4a2ad-179">Hookable 属性</span><span class="sxs-lookup"><span data-stu-id="4a2ad-179">The Hookable attribute</span></span>
<span data-ttu-id="4a2ad-180">メソッドが **[Hookable(false)]** として明示的にマークされている場合、メソッドを拡張子クラスで囲むことはできません。</span><span class="sxs-lookup"><span data-stu-id="4a2ad-180">If a method is explicitly marked as **[Hookable(false)]**, the method can't be wrapped in an extension class.</span></span> <span data-ttu-id="4a2ad-181">次の例では、**anyMethod** は **AnyClass1** を補強するクラスでラップできません。</span><span class="sxs-lookup"><span data-stu-id="4a2ad-181">In the following example, **anyMethod** can't be wrapped in a class that augments **AnyClass1**.</span></span>

```xpp
class AnyClass1 
{
    [HookableAttribute(false)]
    public void anyMethod() {...}
}
```

### <a name="final-methods-and-the-wrappable-attribute"></a><span data-ttu-id="4a2ad-182">最終的な方法および Wrappable 属性</span><span class="sxs-lookup"><span data-stu-id="4a2ad-182">Final methods and the Wrappable attribute</span></span>
<span data-ttu-id="4a2ad-183">**final** とマークされているパブリック メソッドと保護されたメソッドは、拡張クラスでラップできません。</span><span class="sxs-lookup"><span data-stu-id="4a2ad-183">Public and protected methods that are marked as **final** can't be wrapped in extension classes.</span></span> <span data-ttu-id="4a2ad-184">**Wrappable** 属性を使用して属性パラメーターを **true** (**[Wrappable(true)]**) に設定することにより、この制限をオーバーライドすることができます。</span><span class="sxs-lookup"><span data-stu-id="4a2ad-184">You can override this restriction by using the **Wrappable** attribute and setting the attribute parameter to **true** (**[Wrappable(true)]**).</span></span> <span data-ttu-id="4a2ad-185">同様に、(最終ではない) パブリックまたは保護されたメソッドの既定の機能を無効にするには、折り返し不可としてこれらのメソッドをマークすることができます (**[Wrappable(false)]**)。</span><span class="sxs-lookup"><span data-stu-id="4a2ad-185">Similarly, to override the default capability for (non-final) public or protected methods, you can mark those methods as non-wrappable (**[Wrappable(false)]**).</span></span>

<span data-ttu-id="4a2ad-186">次の例では、**doSomething** メソッドは、パブリック メソッドである場合でもラップできないものとして明示的にマークされます。</span><span class="sxs-lookup"><span data-stu-id="4a2ad-186">In the following example, the **doSomething** method is explicitly marked as non-wrappable, even though it's a public method.</span></span> <span data-ttu-id="4a2ad-187">**doSomethingElse** メソッドは、最後のメソッドであっても、折り返し可能と明示的にマークされます。</span><span class="sxs-lookup"><span data-stu-id="4a2ad-187">The **doSomethingElse** method is explicitly marked as wrappable, even though it's a final method.</span></span>

```xpp
class AnyClass2 
{
    [Wrappable(false)]
    public void doSomething(str message) {...}

    [Wrappable(true)]
    final public void doSomethingElse(str message) {...}
}
```


### <a name="extensions-of-form-nested-concepts-such-as-data-sources-data-fields-and-controls"></a><span data-ttu-id="4a2ad-188">データ ソース、データ フィールド、および制御といったフォームで入れ子になった概念の拡張</span><span class="sxs-lookup"><span data-stu-id="4a2ad-188">Extensions of form-nested concepts such as data sources, data fields, and controls</span></span>

<span data-ttu-id="4a2ad-189">データ ソース、データ フィールド、コントロールなど、フォームで入れ子になった概念の CoC メソッドを実装するため、入れ子になった各概念には拡張クラスが必要です。</span><span class="sxs-lookup"><span data-stu-id="4a2ad-189">In order to implement CoC methods for form-nested concepts, such as data sources, data fields, and controls, an extension class is required for each nested concept.</span></span> 

#### <a name="form-data-sources"></a><span data-ttu-id="4a2ad-190">フォーム データ ソース</span><span class="sxs-lookup"><span data-stu-id="4a2ad-190">Form data sources</span></span>

<span data-ttu-id="4a2ad-191">この例では、**FormToExtend** はフォーム、**DataSource1** はフォームで有効な既存のデータ ソース、**init** と **validateWrite** はデータ ソースで折り返し可能なメソッドです。</span><span class="sxs-lookup"><span data-stu-id="4a2ad-191">In this example, **FormToExtend** is the form, **DataSource1** is a valid existing data source in the form, and **init** and **validateWrite** are methods that can be wrapped in the data source.</span></span>

```C#
[ExtensionOf(formdatasourcestr(FormToExtend, DataSource1))]
final class FormDataSource1_Extension
{
    public void init()
    {
        next init();
        //...
        //use element.FormToExtendVariable to access form's variables and datasources
        //element.FormToExtendMethod() to call form methods
    }
 
    public boolean validateWrite()
    {
        boolean ret;
        //...
        ret = next validateWrite();
        //...
        return ret;
    }
}
```

#### <a name="form-data-fields"></a><span data-ttu-id="4a2ad-192">フォーム データ フィールド</span><span class="sxs-lookup"><span data-stu-id="4a2ad-192">Form data fields</span></span>

<span data-ttu-id="4a2ad-193">この例では、データ フィールドが拡張されます。</span><span class="sxs-lookup"><span data-stu-id="4a2ad-193">In this example, a data field is extended.</span></span> <span data-ttu-id="4a2ad-194">**FormToExtend** はフォーム、**DataSource1** はフォームのデータ ソース、**Field1** はデータ ソースのフィールド、**validate** はこの入れ子になった概念で折り返し可能な多くのメソッドのいずれかです。</span><span class="sxs-lookup"><span data-stu-id="4a2ad-194">**FormToExtend** is the form, **DataSource1** is a data source in the form, **Field1** is a field in the data source, and **validate** is one of many methods that can be wrapped in this nested concept.</span></span>

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
        return ret;
    }
}
```

#### <a name="controls"></a><span data-ttu-id="4a2ad-195">コントロール</span><span class="sxs-lookup"><span data-stu-id="4a2ad-195">Controls</span></span>

<span data-ttu-id="4a2ad-196">この例では、**FormToExtend** はフォーム、**Button1** はフォーム内のボタン コントロール、**clicked** はボタン コントロールで折り返し可能なメソッドです。</span><span class="sxs-lookup"><span data-stu-id="4a2ad-196">In this example, **FormToExtend** is the form, **Button1** is the button control in the form, and **clicked** is a method that can be wrapped on the button control.</span></span>

```C#
[ExtensionOf(formControlStr(FormToExtend, Button1))]
final class FormButton1_Extension
{
    public void clicked()
    {
        next clicked();
        //...
    }
}
```

#### <a name="requirements-and-considerations-when-you-write-coc-methods-on-extensions-for-form-nested-concepts"></a><span data-ttu-id="4a2ad-197">フォームで入れ子になった概念で CoC メソッドを書き込むときの要件と考慮事項</span><span class="sxs-lookup"><span data-stu-id="4a2ad-197">Requirements and considerations when you write CoC methods on extensions for form-nested concepts</span></span>

- <span data-ttu-id="4a2ad-198">その他の CoC メソッドと同様、これらのメソッドは常に **next** を呼び出してチェーン内の次のメソッドを呼び出す必要があります。これにより、チェーンは実行時の動作でカーネルまたはネイティブ実装まで進むことができます。</span><span class="sxs-lookup"><span data-stu-id="4a2ad-198">Like other CoC methods, these methods must always call **next** to invoke the next method in the chain, so that the chain can go all the way to the kernel or native implementation in the runtime behavior.</span></span> <span data-ttu-id="4a2ad-199">next の呼び出しは、ランタイムにおける基本の動作が常に正常に実行されることを保証する、フォーム自体からの **super()** の呼び出しに相当します。</span><span class="sxs-lookup"><span data-stu-id="4a2ad-199">The call to next is equivalent to a call to **super()** from the form itself to help guarantee that the base behavior in the runtime is always run as expected.</span></span>
- <span data-ttu-id="4a2ad-200">現時点では、Microsoft Visual Studio の X++ エディターは、折り返し可能なメソッドの検出をサポートしていません。</span><span class="sxs-lookup"><span data-stu-id="4a2ad-200">Currently, the X++ editor in Microsoft Visual Studio doesn't support discovery of methods that can be wrapped.</span></span> <span data-ttu-id="4a2ad-201">したがって、折り返し対象となるメソッドとその正確なシグネチャを識別するための入れ子になった各概念については、システムのドキュメントを参照する必要があります。</span><span class="sxs-lookup"><span data-stu-id="4a2ad-201">Therefore, you must refer to the system documentation for each nested concept to identify the correct method to wrap and its exact signature.</span></span>
- <span data-ttu-id="4a2ad-202">入れ子になったコントロール タイプの元の基本動作で定義されていないメソッドをラップする CoC を追加することは**できません**。</span><span class="sxs-lookup"><span data-stu-id="4a2ad-202">You **cannot** add CoC to wrap methods that aren't defined in the original base behavior of the nested control type.</span></span> <span data-ttu-id="4a2ad-203">たとえば、拡張において **methodInButton1** CoC を追加することはできません。</span><span class="sxs-lookup"><span data-stu-id="4a2ad-203">For example, you can't add **methodInButton1** CoC on an extension.</span></span> <span data-ttu-id="4a2ad-204">ただし、制御の拡張からは、メソッドがパブリックまたは保護として定義されている場合にこのメソッドへの呼び出しを行うことができます。</span><span class="sxs-lookup"><span data-stu-id="4a2ad-204">However, from the control extension, you can make a call into this method if the method has been defined as public or protected.</span></span> <span data-ttu-id="4a2ad-205">以下に、**methodInButton1** メソッドと同じように **Button1** コントロールが **FormToExtend** フォームで定義される例を示します。</span><span class="sxs-lookup"><span data-stu-id="4a2ad-205">Here is an example where the **Button1** control is defined in the **FormToExtend** form in such a way that it has the **methodInButton1** method.</span></span>

    ```C#
    [Form]
    public class FormToExtend extends FormRun
    {
        [Control("Button")]
        class Button1
        {
            public void methodInButton1(str param1)
            {
                info("Hi from methodInButton1");
                //...
    ```

- <span data-ttu-id="4a2ad-206">拡張からのそのフォームで入れ子になった概念における CoC メソッドをサポートするために元のフォームが定義されたモジュールを再コンパイルする必要は**ありません**。</span><span class="sxs-lookup"><span data-stu-id="4a2ad-206">You do **not** have to recompile the module where the original form is defined to support CoC methods on nested concepts on that form from an extension.</span></span> <span data-ttu-id="4a2ad-207">たとえば、前の例の **FormToExtend** フォームが **ApplicationSuite** モジュールにある場合、異なるモジュールからそのフォームで入れ子になった概念の CoC で拡張するために **ApplicationSuite** を再コンパイルする必要はありません。</span><span class="sxs-lookup"><span data-stu-id="4a2ad-207">For example, if the **FormToExtend** form from the previous examples is in the **ApplicationSuite** module, you don't have to recompile **ApplicationSuite** to extend it with CoC for nested concepts on that form from a different module.</span></span>

### <a name="extensions-of-tables-and-data-entities"></a><span data-ttu-id="4a2ad-208">テーブルとデータ エンティティの拡張機能</span><span class="sxs-lookup"><span data-stu-id="4a2ad-208">Extensions of tables and data entities</span></span>

<span data-ttu-id="4a2ad-209">拡張機能クラスは、概念ごとに必要です。</span><span class="sxs-lookup"><span data-stu-id="4a2ad-209">An extension class is required for each concept.</span></span> 

#### <a name="tables"></a><span data-ttu-id="4a2ad-210">テーブル</span><span class="sxs-lookup"><span data-stu-id="4a2ad-210">Tables</span></span>

<span data-ttu-id="4a2ad-211">この例では、**TableToExtend** はテーブルであり、**delete**、**canSubmitToWorkflow**、**caption** はテーブルでラップできるメソッドです。</span><span class="sxs-lookup"><span data-stu-id="4a2ad-211">In this example, **TableToExtend** is the table and **delete**, **canSubmitToWorkflow**, and **caption** are methods that can be wrapped in the table.</span></span>

```C#
[ExtensionOf(tablestr(TableToExtend))]
final class TableToExtend_Extension
{
    public void delete()
    {
        next delete();
        //...
    }
 
     public boolean canSubmitToWorkflow(str _workflowType)
    {
        boolean ret;
        //...
        ret = next canSubmitToWorkflow(_workflowType);
        //...
        return ret;
    }
        
    public str caption()
    {
        str ret;
        //...
        ret = next caption();
        //...
        return ret;
    }
}
```

#### <a name="data-entities"></a><span data-ttu-id="4a2ad-212">データ エンティティ</span><span class="sxs-lookup"><span data-stu-id="4a2ad-212">Data entities</span></span>
<span data-ttu-id="4a2ad-213">この例では、**DataEntityToExtend** はデータ エンティティで、**validateDelete** および **validateWrite** はデータ エンティティでラップできるメソッドです。</span><span class="sxs-lookup"><span data-stu-id="4a2ad-213">In this example, **DataEntityToExtend** is the data entity and **validateDelete** and **validateWrite** are methods that can be wrapped in the data entity.</span></span>

```C#
[ExtensionOf(tableStr(DataEntityToExtend))]
final class DataEntityToExtend_Extension
{
    public boolean validateDelete()
    {
        boolean ret;
        //...
        ret = next validateDelete();
        //...
        return ret;
    }

    public boolean validateWrite()
    {
        boolean ret;
        //...
        ret = next validateWrite();
        //...
        return ret;
    }
}
```

## <a name="restrictions-on-wrapper-methods"></a><span data-ttu-id="4a2ad-214">ラッパー メソッドに関する制限事項</span><span class="sxs-lookup"><span data-stu-id="4a2ad-214">Restrictions on wrapper methods</span></span>
<span data-ttu-id="4a2ad-215">次のセクションでは、CoC およびメソッド ラッピングの使用上の制限について説明します。</span><span class="sxs-lookup"><span data-stu-id="4a2ad-215">The following sections describe restrictions on the use of CoC and method wrapping.</span></span>

### <a name="x-classes-that-are-compiled-by-using-platform-update-8-or-earlier"></a><span data-ttu-id="4a2ad-216">プラットフォーム更新プログラム 8 またはそれ以前を使用してコンパイルされた X++ クラス</span><span class="sxs-lookup"><span data-stu-id="4a2ad-216">X++ classes that are compiled by using Platform update 8 or earlier</span></span> 
<span data-ttu-id="4a2ad-217">メソッドのラッピング機能には、プラットフォーム update 9 以降の一部である X++ コンパイラによって出力される特定の機能が必要です。</span><span class="sxs-lookup"><span data-stu-id="4a2ad-217">The method wrapping feature requires specific functionality that is emitted by an X++ compiler that is part of Platform update 9 or later.</span></span> <span data-ttu-id="4a2ad-218">以前のバージョンを使用してコンパイルされたメソッドには、この機能をサポートするインフラストラクチャはありません。</span><span class="sxs-lookup"><span data-stu-id="4a2ad-218">Methods that are compiled by using earlier versions don't have the infrastructure to support this feature.</span></span>

### <a name="methods-on-types-nested-within-forms-can-be-wrapped-in-platform-update-16-and-later"></a><span data-ttu-id="4a2ad-219">プラットフォーム更新 16 以降ではフォーム内で入れ子になったタイプのメソッドをラップできます。</span><span class="sxs-lookup"><span data-stu-id="4a2ad-219">Methods on types nested within forms can be wrapped in Platform update 16 and later</span></span>
<span data-ttu-id="4a2ad-220">クラス拡張を使用してフォーム (データ ソースとコントロール) 内で入れ子になった型のメソッドをラップする機能がプラットフォーム更新 16 で追加されました。</span><span class="sxs-lookup"><span data-stu-id="4a2ad-220">The ability to wrap methods on types nested within forms (data sources and controls) by using class extensions was added in Platform update 16.</span></span> <span data-ttu-id="4a2ad-221">つまり、コマンド チェーンを使用して、データ ソース メソッドおよびフォーム制御メソッドのオーバーライドを提供できます。</span><span class="sxs-lookup"><span data-stu-id="4a2ad-221">This means that Chain of Command can be used to provide overrides for data source methods and form control methods.</span></span>

<span data-ttu-id="4a2ad-222">ただし、これらの入れ子にされた型 (フォーム コントロールとフォーム データ ソース) の純粋な X++ メソッドのラップ (拡張) は、他の型 (フォーム、テーブル、データ エンティティ) と同様にまだサポートされていません。</span><span class="sxs-lookup"><span data-stu-id="4a2ad-222">However, wrapping (extension) of purely X++ methods on those nested types (form controls and form data sources) is not yet supported like it is on other types (forms, tables, data entities).</span></span> <span data-ttu-id="4a2ad-223">現時点では、開発者は、フォーム内の型の純粋な X++ メソッドでコマンド チェーンを使用する場合、コンパイルしますが、実行時に拡張メソッドじゃ呼び出されません。</span><span class="sxs-lookup"><span data-stu-id="4a2ad-223">Currently, if a developer uses Chain of Command on purely X++ methods on types inside forms, then it compiles, but the extension methods are not invoked at runtime.</span></span> <span data-ttu-id="4a2ad-224">この機能は、将来の更新で計画されています。</span><span class="sxs-lookup"><span data-stu-id="4a2ad-224">This capability is planned for a future update.</span></span>

### <a name="unimplemented-system-methods-on-tables-and-data-entities-can-be-wrapped-in-platform-update-22-and-later"></a><span data-ttu-id="4a2ad-225">テーブルとデータ エンティティの実装されていないシステム メソッドは、プラットフォーム更新 22 以降でラップできます。</span><span class="sxs-lookup"><span data-stu-id="4a2ad-225">Unimplemented system methods on tables and data entities can be wrapped in Platform update 22 and later</span></span>
<span data-ttu-id="4a2ad-226">クラス拡張を使用して入れ子になったクラスでメソッドをラップする機能がプラットフォーム更新 16 で追加されました。</span><span class="sxs-lookup"><span data-stu-id="4a2ad-226">The ability to wrap methods in nested classes by using class extensions was added in Platform update 16.</span></span> <span data-ttu-id="4a2ad-227">X++ の入れ子になったクラスの概念は、データソース メソッドやフォームコ ントロール メソッドを上書きするためのフォームに適用されます。</span><span class="sxs-lookup"><span data-stu-id="4a2ad-227">The concept of nested classes in X++ applies to forms for overriding data source methods and form control methods.</span></span>

### <a name="next-calls-can-be-put-inside-trycatchfinally-in-platform-update-21-and-later"></a><span data-ttu-id="4a2ad-228">プラットフォーム更新 21 以降では、次の呼び出しを try/catch/finally 内に配置できます</span><span class="sxs-lookup"><span data-stu-id="4a2ad-228">Next calls can be put inside try/catch/finally in Platform update 21 and later</span></span> 
<span data-ttu-id="4a2ad-229">CoC 拡張メソッドでは、次の呼び出しを条件付きで呼び出してはなりません。</span><span class="sxs-lookup"><span data-stu-id="4a2ad-229">In a CoC extension method, the next call must not be called conditionally.</span></span> <span data-ttu-id="4a2ad-230">ただし、プラットフォーム更新 21 以降では、例外およびリソースのクリーンアップの標準的な処理を許可するため、次の呼び出しを try/catch/finally 内に配置できます。</span><span class="sxs-lookup"><span data-stu-id="4a2ad-230">However, in Platform update 21 and later next calls can be placed inside a try/catch/finally to allow for standard handling of exceptions and resource cleanup.</span></span>

```C#
    public void someMethod()
    {
        try
        {
            //...
            next updateBalances();
            //...
        }
        catch(Exception::Error)
        {
            //...
        }
    }
```

### <a name="extensions-of-extensions-are-not-yet-supported"></a><span data-ttu-id="4a2ad-231">拡張機能の拡張機能はまだサポートされていません</span><span class="sxs-lookup"><span data-stu-id="4a2ad-231">Extensions of extensions are not yet supported</span></span>
<span data-ttu-id="4a2ad-232">現在のところ、通常のクラスで定義されているメソッドのみラップできます。</span><span class="sxs-lookup"><span data-stu-id="4a2ad-232">Currently, only methods that are defined in regular classes can be wrapped.</span></span> <span data-ttu-id="4a2ad-233">拡張クラスで定義されているメソッドは、拡張クラスを強化してラップできません。</span><span class="sxs-lookup"><span data-stu-id="4a2ad-233">Methods that are defined in extension classes can't be wrapped by augmenting the extension classes.</span></span> <span data-ttu-id="4a2ad-234">この機能は、将来のリリースで計画されています。</span><span class="sxs-lookup"><span data-stu-id="4a2ad-234">This capability is planned for a future release.</span></span>

### <a name="tooling"></a><span data-ttu-id="4a2ad-235">ツール</span><span class="sxs-lookup"><span data-stu-id="4a2ad-235">Tooling</span></span>
<span data-ttu-id="4a2ad-236">このトピックに記載されている機能については、Microsoft Visual Studio X++ エディターは、相互参照および Microsoft IntelliSense の完全なサポートまだ提供していません。</span><span class="sxs-lookup"><span data-stu-id="4a2ad-236">For the features that are described in this topic, the Microsoft Visual Studio X++ editor doesn't yet offer complete support for cross-references and Microsoft IntelliSense.</span></span>
