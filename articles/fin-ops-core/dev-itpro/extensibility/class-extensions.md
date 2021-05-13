---
title: X++ の拡張モデルのクラス
description: この記事では、X++ で新しいクラス拡張モデルについて説明します。
author: pvillads
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Developer
ms.reviewer: rhaertle
ms.custom: 89563
ms.assetid: 271dabb1-ecb8-497f-b866-397733a954b8
ms.search.region: Global
ms.author: pvillads
ms.search.validFrom: 2016-05-31
ms.dyn365.ops.version: Platform update 1
ms.openlocfilehash: 0c8a28f108a41cd50df10f9d59aaf4d012bfd272
ms.sourcegitcommit: e4992c57eea4c15ac052e9d65dddae625e3528f9
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/07/2021
ms.locfileid: "5865922"
---
# <a name="class-extension-model-in-x"></a><span data-ttu-id="a51d1-103">X++ の拡張モデルのクラス</span><span class="sxs-lookup"><span data-stu-id="a51d1-103">Class extension model in X++</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="a51d1-104">この記事では、X++ で新しいクラス拡張モデルについて説明します。</span><span class="sxs-lookup"><span data-stu-id="a51d1-104">This article describes the new class extension model in X++.</span></span>

<span data-ttu-id="a51d1-105">オーバーレイは非常に侵入的な機能なので、使用しないことをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="a51d1-105">Because over-layering is a very intrusive feature, we recommend that you not use it.</span></span> <span data-ttu-id="a51d1-106">オーバーレイに代わる方法は、拡張です。</span><span class="sxs-lookup"><span data-stu-id="a51d1-106">The alternative to over-layering is extension.</span></span> <span data-ttu-id="a51d1-107">拡張子を使用すると、既存のコンポーネントを新しいモデルで拡張できます。</span><span class="sxs-lookup"><span data-stu-id="a51d1-107">Extension lets you extend existing artifacts in a new model.</span></span> <span data-ttu-id="a51d1-108">拡張子は維持しやすいですが、カスタマイズ時に拡張できる量は限られています。</span><span class="sxs-lookup"><span data-stu-id="a51d1-108">Extensions are easier to maintain, but the amount of extension that can be done during customization is limited.</span></span> <span data-ttu-id="a51d1-109">メタデータを拡張する豊富な方法があります。</span><span class="sxs-lookup"><span data-stu-id="a51d1-109">There are rich ways to extend the metadata.</span></span> <span data-ttu-id="a51d1-110">たとえば、テーブルに新しいフィールドを追加できます。</span><span class="sxs-lookup"><span data-stu-id="a51d1-110">For example, you can add new fields to a table.</span></span> <span data-ttu-id="a51d1-111">この記事では、X++ コードを拡張する方法について説明し、これらのモデルを再コンパイルせずに他のモデルで定義されているコンポーネントにメソッドと状態を追加できるようにします。</span><span class="sxs-lookup"><span data-stu-id="a51d1-111">This article describes how X++ code can be extended, so that you can add methods and state to artifacts that are defined in other models without recompiling those models.</span></span> <span data-ttu-id="a51d1-112">X++ 用の同様のコード拡張メカニズムが存在し、C\# で対応する機能の後でモデル化されます。</span><span class="sxs-lookup"><span data-stu-id="a51d1-112">A similar code extension mechanism already exists for X++ and is modeled after the corresponding feature in C\#.</span></span> <span data-ttu-id="a51d1-113">このメカニズムにより、クラスは、命名規則に従い public static メソッドをホストすることにより、拡張クラスとして指定することができます。</span><span class="sxs-lookup"><span data-stu-id="a51d1-113">Under this mechanism, a class can be designated as an extension class through a naming convention and by hosting public static methods.</span></span> <span data-ttu-id="a51d1-114">既存の機能では、拡張メソッドに渡される最初の引数の型は、拡張する型です。</span><span class="sxs-lookup"><span data-stu-id="a51d1-114">In the existing feature, the type of the first argument that is passed to the extension method is the type to extend.</span></span> <span data-ttu-id="a51d1-115">この記事に記載する内容はその方向の次のステップであり、役に立つありのままの拡張についての説明です。</span><span class="sxs-lookup"><span data-stu-id="a51d1-115">What this article describes is the next step in that direction, which offers a more capable and natural extension story.</span></span> <span data-ttu-id="a51d1-116">オブジェクト指向のプログラミングでは、*拡張* という用語には、明確に定義された意味があります。</span><span class="sxs-lookup"><span data-stu-id="a51d1-116">In object-oriented programming, the term *extend* has a well-defined meaning.</span></span> <span data-ttu-id="a51d1-117">「クラス B がクラス A を拡張する」と表現する場合、B は A が B の親のクラスであることを A から継承し、通常のオブジェクト指向ルールが暗黙的に適用されます。</span><span class="sxs-lookup"><span data-stu-id="a51d1-117">If we say, "class B extends class A," we mean that B inherits from A, that A is B's parent class, and the usual object-oriented rules are implied.</span></span> <span data-ttu-id="a51d1-118">実際、この用語は、この関係を表現するクラス宣言で使用される X++ 構文でも使用されます。</span><span class="sxs-lookup"><span data-stu-id="a51d1-118">In fact, this term is even used in the X++ syntax that is used in class declarations to express this relationship.</span></span> <span data-ttu-id="a51d1-119">同時に複数のモデルから寄せられたメタデータについて *拡張* という用語を使用して説明します。</span><span class="sxs-lookup"><span data-stu-id="a51d1-119">At the same time, we use the term *extension* to talk about metadata that has contributions from several models.</span></span> <span data-ttu-id="a51d1-120">*拡張* という用語の多用を避ける目的で、*クラス強化* という代替用語を使用して、基本モデルのクラス A とそれに依存するモデルのクラス B の間の関係を指定します。ここで、B はそのモデルのコンテキストでクラス A に追加の機能を提供します。</span><span class="sxs-lookup"><span data-stu-id="a51d1-120">To avoid further overloading the term *extend*, we will instead use the term *class augmentation* to designate the relationship between a class A in a base model and a class B in a model that depends on it, where B provides additional functionality to class A in the context of that model.</span></span> <span data-ttu-id="a51d1-121">ただし、*拡張クラス* という用語が一般的であるため、引き続き使用します。</span><span class="sxs-lookup"><span data-stu-id="a51d1-121">Nevertheless, we will also continue to use the term *extension class*, because it's prevalent.</span></span>

## <a name="the-effective-class-concept"></a><span data-ttu-id="a51d1-122">有効なクラスの概念</span><span class="sxs-lookup"><span data-stu-id="a51d1-122">The effective class concept</span></span>
<span data-ttu-id="a51d1-123">強化されたコンポーネントのパブリック メンバー、およびそのコンポーネントを強化するすべてのクラスの拡張機能のすべてのパブリック メンバーで構成されるクラスに条件を設けるために役立ちます。</span><span class="sxs-lookup"><span data-stu-id="a51d1-123">It's useful to have a term for a class that consists of the public members of the augmented artifact and all the public members of all the class extensions that augment that artifact.</span></span> <span data-ttu-id="a51d1-124">このクラスは、指定されたモデルの有効なクラスと呼ばれます。</span><span class="sxs-lookup"><span data-stu-id="a51d1-124">This class is called the effective class in a given model.</span></span> <span data-ttu-id="a51d1-125">次の図は、基本モデルで定義された、**MyArtifact** および **MyArtifact** の拡張クラスを持つ 2 つの依存モデルで定義されたコンポーネント **MyModel** を示しています。</span><span class="sxs-lookup"><span data-stu-id="a51d1-125">The following illustration shows an artifact, **MyArtifact**, that is defined in a base model, **MyModel**, and two dependent models that have extension classes for **MyArtifact**.</span></span>

<span data-ttu-id="a51d1-126">[![ベースモデル MyModel で定義されているコンポーネント MyArtifact、および MyArtifact の拡張クラスを持つ 2 つの依存モデル](./media/extensions-11.png)](./media/extensions-11.png)</span><span class="sxs-lookup"><span data-stu-id="a51d1-126">[![Artifact MyArtifact that is defined in base model MyModel, and two dependent models that have extension classes for MyArtifact](./media/extensions-11.png)](./media/extensions-11.png)</span></span>

<span data-ttu-id="a51d1-127">この例では、有効なクラスはすべてのオリジナルのメソッドおよび拡張クラスからのすべてのパブリック コンポーネントを含む拡張モデルのクラスです。</span><span class="sxs-lookup"><span data-stu-id="a51d1-127">In this example, the effective class is the class in the extension models that contains all the original methods and all the public artifacts from the extension classes.</span></span> <span data-ttu-id="a51d1-128">有効なクラスは、特定のモデルで定義されたクラスの拡張のみを含むため、すべてのモデルで同じではありません。</span><span class="sxs-lookup"><span data-stu-id="a51d1-128">The effective class isn't the same in every model because it includes only the class extensions that are defined in a given model.</span></span> <span data-ttu-id="a51d1-129">次の図は、**MyExtensionModel** モデルの **MyArtifact** の有効クラスを示しています。</span><span class="sxs-lookup"><span data-stu-id="a51d1-129">The following illustration shows the effective class of **MyArtifact** in the **MyExtensionModel** model.</span></span>

<span data-ttu-id="a51d1-130">[![MyExtensionModel の MyArtifact の有効クラス](./media/extensions-21.png)](./media/extensions-21.png)</span><span class="sxs-lookup"><span data-stu-id="a51d1-130">[![Effective class of MyArtifact in MyExtensionModel](./media/extensions-21.png)](./media/extensions-21.png)</span></span>

<span data-ttu-id="a51d1-131">**MyModel** という名前のモデル内の **MyClass** という名前のクラスを使用して、クラス拡張について説明します。</span><span class="sxs-lookup"><span data-stu-id="a51d1-131">We will describe class extensions by using a class that is named **MyClass** in a model that is named **MyModel**.</span></span>

```xpp
class MyClass
{
    public int mycState;
    public str mycMethod(int _arg)
    {
        // ...
    }
}
```

<span data-ttu-id="a51d1-132">**MyModel** の上に構築される (つまり、MyModel に依存する) 拡張モデル (**MyExtensionModel**) に拡張クラスを導入することで、**MyClass** に新しいメソッドと状態を追加できます。</span><span class="sxs-lookup"><span data-stu-id="a51d1-132">We can add new methods and state to **MyClass** by introducing an extension class in the extension model (**MyExtensionModel**) that builds on top of (that is, has a dependency on) **MyModel**.</span></span>

## <a name="extension-class-declarations"></a><span data-ttu-id="a51d1-133">拡張子のクラス宣言</span><span class="sxs-lookup"><span data-stu-id="a51d1-133">Extension class declarations</span></span>
<span data-ttu-id="a51d1-134">拡張クラスは、 **ExtensionOf** 属性で修飾されており、また、**\_拡張子** の接尾辞を持つ名称も持つ最終クラスです。</span><span class="sxs-lookup"><span data-stu-id="a51d1-134">Extension classes are final classes that are adorned with the **ExtensionOf** attribute and that also have a name that has the **\_Extension** suffix.</span></span> <span data-ttu-id="a51d1-135">(この名前付けの制限は、後で削除される可能性があります。) 拡張クラスの名前は、それ以外の場合重要ではありません。</span><span class="sxs-lookup"><span data-stu-id="a51d1-135">(This restriction on the naming might be removed later.) The name of the extension class is otherwise unimportant.</span></span> <span data-ttu-id="a51d1-136">このクラスは、次の例に示すように、**ExtensionOf** 属性のパラメーターで指定されたコンポーネントを補強します。</span><span class="sxs-lookup"><span data-stu-id="a51d1-136">The class augments the artifact that is specified in the parameter of the **ExtensionOf** attribute, as shown in the following example.</span></span>

```xpp
[ExtensionOf(classStr(MyClass))]
final class MyClass_Extension
{
    private void new()
    {
    }
}
```

<span data-ttu-id="a51d1-137">クラスはランタイム システムによってインスタンス化されるため、拡張クラスから派生する意味がありません。</span><span class="sxs-lookup"><span data-stu-id="a51d1-137">Because the classes are instantiated by the runtime system, it's not meaningful to derive from the extension class.</span></span> <span data-ttu-id="a51d1-138">したがって、拡張クラスは **final** としてマークする必要があります。</span><span class="sxs-lookup"><span data-stu-id="a51d1-138">Therefore, the extension class must be marked as **final**.</span></span> <span data-ttu-id="a51d1-139">拡張クラス **MyClass_Extension** は、指定されたクラス (**MyClass**) を拡張しません。</span><span class="sxs-lookup"><span data-stu-id="a51d1-139">The extension class **MyClass_Extension** does not extend the designated class (**MyClass**).</span></span> <span data-ttu-id="a51d1-140">したがって、**MyClass_Extension** の **MyClass** からメソッドをオーバーライドすることはできません。</span><span class="sxs-lookup"><span data-stu-id="a51d1-140">Therefore, you cannot override methods from **MyClass** in **MyClass_Extension**.</span></span> <span data-ttu-id="a51d1-141">補強クラスを指定するには、**classStr** コンパイル時関数を使用する必要があり、これは次の 2 つの目的に使用できます。</span><span class="sxs-lookup"><span data-stu-id="a51d1-141">The **classStr** compile-time function must be used to designate the augmented class, and it serves two purposes:</span></span>

-   <span data-ttu-id="a51d1-142">**MyClass** クラスが存在しない場合、コンパイル エラーを生成します。</span><span class="sxs-lookup"><span data-stu-id="a51d1-142">It produces a compilation error if the **MyClass** class doesn't exist.</span></span>
-   <span data-ttu-id="a51d1-143">どのような種類のコンポーネントが拡張されるかをコンパイラに知らせるために使用するコンパイル時関数。</span><span class="sxs-lookup"><span data-stu-id="a51d1-143">The compile-time function that is used tells the compiler what kind of artifact is augmented.</span></span> <span data-ttu-id="a51d1-144">コンポーネント名単独では、拡張するために指定されたコンポーネントを一意に識別しません。</span><span class="sxs-lookup"><span data-stu-id="a51d1-144">Artifact names by themselves don't uniquely identify a given artifact to augment.</span></span> <span data-ttu-id="a51d1-145">たとえば、フォームはテーブル、クラス、および列挙として同じ名前を持つことができます。</span><span class="sxs-lookup"><span data-stu-id="a51d1-145">For example, forms can have the same names as tables, classes, and enums.</span></span>

<span data-ttu-id="a51d1-146">任意の数の拡張クラスが、特定のモデル内で付与されたコンポーネントを強化することができます。</span><span class="sxs-lookup"><span data-stu-id="a51d1-146">Any number of extension classes can augment a given artifact in a particular model.</span></span> <span data-ttu-id="a51d1-147">拡張子クラスは、ランタイム システムでのみプログラマが直接参照することはありません。</span><span class="sxs-lookup"><span data-stu-id="a51d1-147">Extension classes are never referenced directly by the programmer, only by the runtime system.</span></span>

## <a name="extension-class-inheritance"></a><span data-ttu-id="a51d1-148">拡張子のクラス継承</span><span class="sxs-lookup"><span data-stu-id="a51d1-148">Extension class inheritance</span></span>
<span data-ttu-id="a51d1-149">拡張されたクラスから継承するクラスも、有効なクラスを継承します。</span><span class="sxs-lookup"><span data-stu-id="a51d1-149">Any class that inherits from an augmented class also inherits the effective class.</span></span> <span data-ttu-id="a51d1-150">つまり、拡張機能を持つクラスから継承するクラスは、拡張クラスで定義されているメソッドを継承します。</span><span class="sxs-lookup"><span data-stu-id="a51d1-150">In other words, the classes that inherit from a class that has extensions inherit the methods that are defined in the extension classes.</span></span>

## <a name="constructors"></a><span data-ttu-id="a51d1-151">コンストラクター</span><span class="sxs-lookup"><span data-stu-id="a51d1-151">Constructors</span></span>
<span data-ttu-id="a51d1-152">X++ はインスタンス コンストラクターおよび静的コンストラクターの両方をサポートしています。</span><span class="sxs-lookup"><span data-stu-id="a51d1-152">X++ supports both instance constructors and static constructors.</span></span>

### <a name="instance-constructors"></a><span data-ttu-id="a51d1-153">インスタンス コンストラクター</span><span class="sxs-lookup"><span data-stu-id="a51d1-153">Instance constructors</span></span>

<span data-ttu-id="a51d1-154">インスタンス コンストラクターは、**new** という名前のメソッドです。</span><span class="sxs-lookup"><span data-stu-id="a51d1-154">The instance constructor is the method that is named **new**.</span></span> <span data-ttu-id="a51d1-155">コンストラクターは、拡張オブジェクトの状態を初期化するのに便利です。</span><span class="sxs-lookup"><span data-stu-id="a51d1-155">Constructors are useful for initializing the state of the extension objects.</span></span> <span data-ttu-id="a51d1-156">拡張クラスで定義されているインスタンス コンストラクターはパラメーターを指定できません。</span><span class="sxs-lookup"><span data-stu-id="a51d1-156">The instance constructor that is defined in an extension class can't have parameters.</span></span> <span data-ttu-id="a51d1-157">拡張クラスのインスタンスが作成され、ランタイム システムが使用シナリオで必要なコンストラクターを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="a51d1-157">Instances of the extension classes are created, and the runtime system calls their constructors as required by the usage scenario.</span></span> <span data-ttu-id="a51d1-158">これらのコンストラクターは、コードによって明示的に呼び出されることはありません。</span><span class="sxs-lookup"><span data-stu-id="a51d1-158">These constructors are never explicitly called by your code.</span></span>  <span data-ttu-id="a51d1-159">拡張機能クラスのインスタンス メソッドまたはインスタンスの状態にアクセスする前に、拡張機能クラスに提示されているコンストラクターが必ず一度呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="a51d1-159">It's guaranteed that the constructor that is provided in an extension class will be called once before any instance method or the instance state on the extension class is accessed.</span></span> <span data-ttu-id="a51d1-160">ただし、そのような参照が行われない場合、コンストラクタは呼び出されません。</span><span class="sxs-lookup"><span data-stu-id="a51d1-160">However, if no such references are made, the constructor isn't called.</span></span>

### <a name="static-constructors"></a><span data-ttu-id="a51d1-161">静的コンストラクター</span><span class="sxs-lookup"><span data-stu-id="a51d1-161">Static constructors</span></span>

<span data-ttu-id="a51d1-162">静的コンストラクターは、**typenew** と呼ばれるパラメーターなしの静的メソッドです。</span><span class="sxs-lookup"><span data-stu-id="a51d1-162">Static constructors are the parameter-less static methods that are named **typenew**.</span></span> <span data-ttu-id="a51d1-163">静的コンストラクターは、拡張クラスで定義することができます。</span><span class="sxs-lookup"><span data-stu-id="a51d1-163">Static constructors can be defined on extension classes.</span></span> <span data-ttu-id="a51d1-164">ランタイム システムが拡張機能の種類を最初に参照する前に必ず一度コンストラクターが呼び出されることが保証されます。</span><span class="sxs-lookup"><span data-stu-id="a51d1-164">It's guaranteed that the runtime system will call the constructor exactly once before the first reference to the extension type.</span></span> <span data-ttu-id="a51d1-165">拡張子のセットの間での静的コンストラクションの呼び出しの特定の任意の順序を想定することはできません。</span><span class="sxs-lookup"><span data-stu-id="a51d1-165">You can't assume any particular order of invocation for static construction among a set of extensions.</span></span> <span data-ttu-id="a51d1-166">つまり、静的コンストラクター内の他のクラスから静的データを参照する場合には注意する必要があります。</span><span class="sxs-lookup"><span data-stu-id="a51d1-166">This means that you should be careful about referencing static data from other classes in static constructors.</span></span>

## <a name="methods"></a><span data-ttu-id="a51d1-167">メソッド</span><span class="sxs-lookup"><span data-stu-id="a51d1-167">Methods</span></span>
<span data-ttu-id="a51d1-168">拡張クラスで定義されているパブリック メソッドは、拡張クラスが定義されているモデルのコンテキストで、拡張クラスに追加の機能を提供します。</span><span class="sxs-lookup"><span data-stu-id="a51d1-168">The public methods that are defined in extension classes provide additional functionality to the augmented class in the context of the model where the extension class is defined.</span></span> <span data-ttu-id="a51d1-169">この方法で、パブリック メソッドだけが公開されます。</span><span class="sxs-lookup"><span data-stu-id="a51d1-169">Only public methods are exposed in this way.</span></span> <span data-ttu-id="a51d1-170">パブリック メソッドの実装に役立てるためにプライベート メソッドを定義することができますが、これらのプライベート メソッドは有効なクラスの一部ではありません。</span><span class="sxs-lookup"><span data-stu-id="a51d1-170">You can define private methods to help implement the public methods, but those private methods aren't part of the effective class.</span></span> <span data-ttu-id="a51d1-171">拡張クラスは最終的版であるため、メソッドを **保護された** ものとしてマークすることはできません。</span><span class="sxs-lookup"><span data-stu-id="a51d1-171">Because extension classes are final, methods should not be marked as **protected**.</span></span>

### <a name="instance-methods"></a><span data-ttu-id="a51d1-172">インスタンス メソッド</span><span class="sxs-lookup"><span data-stu-id="a51d1-172">Instance methods</span></span>

<span data-ttu-id="a51d1-173">次の例では、あるクラス内の **ExtensionMethod**  という名前の拡張メソッドを定義し、**MyClass** を補強します。</span><span class="sxs-lookup"><span data-stu-id="a51d1-173">The following example defines an extension method named **ExtensionMethod** in a class that augments **MyClass**.</span></span>

```xpp
[ExtensionOf(classStr(MyClass))]
final class MyClass_Extension
{
    private void new()
    {
    }
    public int ExtensionMethod(int arg)
    {
    }
}
```

<span data-ttu-id="a51d1-174">パブリック インスタンス メソッド (**ExtensionMethod**) は、拡張クラスで定義されます。</span><span class="sxs-lookup"><span data-stu-id="a51d1-174">The public instance method (**ExtensionMethod**) is defined in the extension class.</span></span> <span data-ttu-id="a51d1-175">したがって、拡張クラスが定義されているモデルのコンテキストで **MyClass** で定義されているかのように使用できます。</span><span class="sxs-lookup"><span data-stu-id="a51d1-175">Therefore, it's available just as if it were defined in **MyClass** in the context of the model where the extension class is defined.</span></span> <span data-ttu-id="a51d1-176">次の例は、モデル内のメソッドを呼び出す方法を示しています。</span><span class="sxs-lookup"><span data-stu-id="a51d1-176">The following example shows how to call the method in the model.</span></span>

```xpp
MyClass c = new MyClass();
print c.ExtensionMethod(32);
```

<span data-ttu-id="a51d1-177">拡張クラスで定義されているインスタンス メソッドは、強化されたコンポーネントのインスタンス メソッドとして使用されることに注意してください。</span><span class="sxs-lookup"><span data-stu-id="a51d1-177">Note that the instance method that is defined in the extension class is used as an instance method on the augmented artifact.</span></span> <span data-ttu-id="a51d1-178">拡張メソッドは、拡張をする成果物からのみパブリック メンバーと保護されたメンバーにアクセスできます。</span><span class="sxs-lookup"><span data-stu-id="a51d1-178">An extension method can access public and protected members only from the artifact that it augments.</span></span> <span data-ttu-id="a51d1-179">この動作は仕様です。</span><span class="sxs-lookup"><span data-stu-id="a51d1-179">This behavior is by design.</span></span> <span data-ttu-id="a51d1-180">コンポーネントは、**private**、または **internal** キーワードを通じて明示的に非表示にされる状態およびメソッドと直接やり取りできるようにする必要はありません。</span><span class="sxs-lookup"><span data-stu-id="a51d1-180">No artifact should be able to interact directly with state and methods that are explicitly hidden through the **private**, or **internal** keywords.</span></span> <span data-ttu-id="a51d1-181">それ以外の場合、明示的に非表示な状態とメソッドを直接操作すると、それらのコンポーネントの重要な実装の前提条件を無効にすることで障害が発生する可能性があります。</span><span class="sxs-lookup"><span data-stu-id="a51d1-181">Otherwise, direct interaction with explicitly hidden state and methods could cause malfunction by invalidating key implementation assumptions in those artifacts.</span></span> <span data-ttu-id="a51d1-182">メソッドとメソッド本体のステートメントは、**this** キーワードを使用できます。</span><span class="sxs-lookup"><span data-stu-id="a51d1-182">Methods and statements in the method body can use the **this** keyword.</span></span> <span data-ttu-id="a51d1-183">このコンテキストでは、**this** の型は強化されたコンポーネントの有効なクラスです。</span><span class="sxs-lookup"><span data-stu-id="a51d1-183">In this context, the type of **this** is the effective class of the augmented artifact.</span></span>

### <a name="static-methods"></a><span data-ttu-id="a51d1-184">静的メソッド</span><span class="sxs-lookup"><span data-stu-id="a51d1-184">Static methods</span></span>

<span data-ttu-id="a51d1-185">拡張クラスでパブリックおよび静的として定義されているメソッドは、強化されているコンポーネントの静的メソッドとして使用できます。</span><span class="sxs-lookup"><span data-stu-id="a51d1-185">Methods that are defined as public and static in the extension class are available as static methods on the artifact that is augmented.</span></span>

```xpp
[ExtensionOf(classStr(MyClass))]
final class MyClass_Extension
{
    private void new()
    {
    }
    public int method1(int arg)
    {
    }
    public static real CelsiusToFahrenheit(real celsius)
    {
        return (celsius * 9.0 / 5.0) + 32.0;
    }
}
```

<span data-ttu-id="a51d1-186">次の例は、モデル内のメソッドを呼び出す方法を示しています。</span><span class="sxs-lookup"><span data-stu-id="a51d1-186">The following example shows how to call the method in the model.</span></span>

```xpp
var temp = MyClass::CelsiusToFahrenheit(20.0);
```

<span data-ttu-id="a51d1-187">静的メソッドは、パブリックの静的メソッドおよび強化されたコンポーネントの有効なクラスの状態にアクセスできます。</span><span class="sxs-lookup"><span data-stu-id="a51d1-187">A static method can access the public static methods and state in the effective class of the augmented artifact.</span></span> <span data-ttu-id="a51d1-188">興味深い副作用として、**グローバル** クラスの静的拡張メソッドは接頭語なしで利用できる関数として言語で使用可能になります。</span><span class="sxs-lookup"><span data-stu-id="a51d1-188">As an interesting side effect, static extension methods on the **Global** class become available in the language as functions, which are available without any prefix.</span></span>

## <a name="state"></a><span data-ttu-id="a51d1-189">行政単位 (区画)</span><span class="sxs-lookup"><span data-stu-id="a51d1-189">State</span></span>
<span data-ttu-id="a51d1-190">成果物に対する静的およびインスタンス メソッドを提供することに加えて、インスタンス状態と静的状態を追加できます。</span><span class="sxs-lookup"><span data-stu-id="a51d1-190">In addition to providing static and instance methods to an artifact, you can add instance state and static state.</span></span>

### <a name="instance-state"></a><span data-ttu-id="a51d1-191">インスタンスの状態</span><span class="sxs-lookup"><span data-stu-id="a51d1-191">Instance state</span></span>

<span data-ttu-id="a51d1-192">コンポーネントの特定のインスタンスに関連する状態であるインスタンスの状態は、拡張クラスで指定できます。</span><span class="sxs-lookup"><span data-stu-id="a51d1-192">Instance state, which is state that pertains to a particular instance of an artifact, can be specified on extension classes.</span></span> <span data-ttu-id="a51d1-193">次の例では、**state** という名前の状態を定義しています。</span><span class="sxs-lookup"><span data-stu-id="a51d1-193">The following example defines a state that is named **state**.</span></span>

```xpp
[ExtensionOf(classStr(MyClass))]
final class MyClass_Extension
{
    public int state;
    private void new()
    {
    }
}
```

<span data-ttu-id="a51d1-194">次の例は、コード内で **state** を使用する方法を示しています。</span><span class="sxs-lookup"><span data-stu-id="a51d1-194">The following example shows how to use **state** in your code.</span></span>

```xpp
MyClass c = new MyClass();
c.state = 12;
```

### <a name="static-state"></a><span data-ttu-id="a51d1-195">静的な状態</span><span class="sxs-lookup"><span data-stu-id="a51d1-195">Static state</span></span>

<span data-ttu-id="a51d1-196">静的な状態は、タイプのインスタンスではなく、タイプに対して適用されます。</span><span class="sxs-lookup"><span data-stu-id="a51d1-196">Static state applies to the type, not instances of the type.</span></span> <span data-ttu-id="a51d1-197">次の例では、拡張 クラスで **staticState** という静的メンバーを定義して、 **MyClass** のクラスを拡張します。</span><span class="sxs-lookup"><span data-stu-id="a51d1-197">The following example defines a static member called **staticState** in the Extension class augmenting the **MyClass** class.</span></span>

```xpp
[ExtensionOf(classStr(MyClass))]
final class MyClass_Extension
{
    public int state;
    public static int staticState;
    static void TypeNew()
    {
        staticState = 77;
    }
}
```




[!INCLUDE[footer-include](../../../includes/footer-banner.md)]