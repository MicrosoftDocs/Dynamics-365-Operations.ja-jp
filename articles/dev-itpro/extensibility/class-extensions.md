<?xml version="1.0" encoding="UTF-8"?>
<xliff xmlns:logoport="urn:logoport:xliffeditor:xliff-extras:1.0" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns="urn:oasis:names:tc:xliff:document:1.2" xmlns:xliffext="urn:microsoft:content:schema:xliffextensions" version="1.2" xsi:schemaLocation="urn:oasis:names:tc:xliff:document:1.2 xliff-core-1.2-transitional.xsd">
  <file datatype="xml" source-language="en-US" original="class-extensions.md" target-language="ja-JP">
    <header>
      <tool tool-company="Microsoft" tool-version="1.0-7889195" tool-name="mdxliff" tool-id="mdxliff"/>
      <xliffext:skl_file_name>class-extensions.fb573a.c4d1b5a7e4ff92510b466576d024cd4a4309a646.skl</xliffext:skl_file_name>
      <xliffext:version>1.2</xliffext:version>
      <xliffext:ms.openlocfilehash>c4d1b5a7e4ff92510b466576d024cd4a4309a646</xliffext:ms.openlocfilehash>
      <xliffext:ms.sourcegitcommit>9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b</xliffext:ms.sourcegitcommit>
      <xliffext:ms.lasthandoff>05/15/2019</xliffext:ms.lasthandoff>
      <xliffext:ms.openlocfilepath>articles\dev-itpro\extensibility\class-extensions.md</xliffext:ms.openlocfilepath>
    </header>
    <body>
      <group extype="content" id="content">
        <trans-unit xml:space="preserve" translate="yes" id="101" restype="x-metadata">
          <source>Class extension model in X++</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">X++ の拡張モデルのクラス</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="102" restype="x-metadata">
          <source>This article describes the new class extension model in X++.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この記事では、X++ で新しいクラス拡張モデルについて説明します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="103">
          <source>Class extension model in X++</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">X++ の拡張モデルのクラス</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="104">
          <source>This article describes the new class extension model in X++.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この記事では、X++ で新しいクラス拡張モデルについて説明します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="105">
          <source>Because over-layering is a very intrusive feature, we recommend that you not use it.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">オーバーレイは非常に侵入的な機能なので、使用しないことをお勧めします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="106">
          <source>The alternative to over-layering is extension.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">オーバーレイに代わる方法は、拡張です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="107">
          <source>Extension lets you extend existing artifacts in a new model.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">拡張子を使用すると、既存のコンポーネントを新しいモデルで拡張できます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="108">
          <source>Extensions are easier to maintain, but the amount of extension that can be done during customization is limited.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">拡張子は維持しやすいですが、カスタマイズ時に拡張できる量は限られています。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="109">
          <source>There are rich ways to extend the metadata.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">メタデータを拡張する豊富な方法があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="110">
          <source>For example, you can add new fields to a table.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">たとえば、テーブルに新しいフィールドを追加できます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="111">
          <source>This article describes how X++ code can be extended, so that you can add methods and state to artifacts that are defined in other models without recompiling those models.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この記事では、X++ コードを拡張する方法について説明し、これらのモデルを再コンパイルせずに他のモデルで定義されているコンポーネントにメソッドと状態を追加できるようにします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="112">
          <source>A similar code extension mechanism already exists for X++ and is modeled after the corresponding feature in C<ph id="ph1">\#</ph>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">X++ 用の同様のコード拡張メカニズムが存在し、C<ph id="ph1">\#</ph> で対応する機能の後でモデル化されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="113">
          <source>Under this mechanism, a class can be designated as an extension class through a naming convention and by hosting public static methods.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このメカニズムにより、クラスは、命名規則に従い public static メソッドをホストすることにより、拡張クラスとして指定することができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="114">
          <source>In the existing feature, the type of the first argument that is passed to the extension method is the type to extend.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">既存の機能では、拡張メソッドに渡される最初の引数の型は、拡張する型です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="115">
          <source>What this article describes is the next step in that direction, which offers a more capable and natural extension story.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この記事に記載する内容はその方向の次のステップであり、役に立つありのままの拡張についての説明です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="116">
          <source>In objected-oriented programming, the term <bpt id="p1">*</bpt>extend<ept id="p1">*</ept> has a well-defined meaning.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">オブジェクト指向のプログラミングで、<bpt id="p1">*</bpt>拡張<ept id="p1">*</ept>という用語には、適切に定義された意味があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="117">
          <source>If we say, "class B extends class A," we mean that B inherits from A, and the usual object-oriented rules are implied.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">「クラス B がクラス A を拡張する」である場合、B が A から継承し、通常のオブジェクト指向の規則が暗示されていることを意味します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="118">
          <source>In fact, this term is even used in the X++ syntax that is used in class declarations to express this relationship.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">実際、この用語は、この関係を表現するクラス宣言で使用される X++ 構文でも使用されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="119">
          <source>At the same time, we use the term <bpt id="p1">*</bpt>extension<ept id="p1">*</ept> to talk about metadata that has contributions from several models.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">同時に複数のモデルから寄せられたメタデータについて<bpt id="p1">*</bpt>拡張<ept id="p1">*</ept>という用語を使用して説明します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="120">
          <source>To avoid overloading the term <bpt id="p1">*</bpt>extend<ept id="p1">*</ept>, we will instead use the term <bpt id="p2">*</bpt>class augmentation<ept id="p2">*</ept> to designate the relationship between a class A in a base model and a class B in a model that depends on it, where B provides additional functionality to class A in the context of that model.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">*</bpt>拡張<ept id="p1">*</ept>という用語の過負荷を避けるために、代わりに<bpt id="p2">*</bpt>クラス強化<ept id="p2">*</ept>という用語を使用して、基本モデルのクラス A とそれに依存するモデルのクラス B の間の関係を指定します。ここで、B はそのモデルのコンテキストでクラス A に追加の機能を提供します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="121">
          <source>Nevertheless, we will also continue to use the term <bpt id="p1">*</bpt>extension class<ept id="p1">*</ept>, because it's prevalent.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ただし、<bpt id="p1">*</bpt>拡張クラス<ept id="p1">*</ept>という用語が一般的であるため、引き続き使用します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="122">
          <source>The effective class concept</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">有効なクラスの概念</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="123">
          <source>It's useful to have a term for a class that consists of the public members of the augmented artifact and all the public members of all the class extensions that augment that artifact.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">強化されたコンポーネントのパブリック メンバー、およびそのコンポーネントを強化するすべてのクラスの拡張機能のすべてのパブリック メンバーで構成されるクラスに条件を設けるために役立ちます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="124">
          <source>This class is called the effective class in a given model.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このクラスは、指定されたモデルの有効なクラスと呼ばれます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="125">
          <source>The following illustration shows an artifact, <bpt id="p1">**</bpt>MyArtifact<ept id="p1">**</ept>, that is defined in a base model, <bpt id="p2">**</bpt>MyModel<ept id="p2">**</ept>, and two dependent models that have extension classes for <bpt id="p3">**</bpt>MyArtifact<ept id="p3">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">次の図は、基本モデルで定義された、<bpt id="p1">**</bpt>MyArtifact<ept id="p1">**</ept> および <bpt id="p2">**</bpt>MyArtifact<ept id="p2">**</ept>の拡張クラスを持つ 2 つの依存モデルで定義されたコンポーネント <bpt id="p3">**</bpt>MyModel<ept id="p3">**</ept> を示しています。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="126">
          <source><bpt id="p1">[</bpt><ph id="ph1">![</ph>Artifact MyArtifact that is defined in base model MyModel, and two dependent models that have extension classes for MyArtifact<ept id="p1">](./media/extensions-11.png)](./media/extensions-11.png)</ept> In this example, the effective class is the class in the extension models that contains all the original methods and all the public artifacts from the extension classes.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">[</bpt><ph id="ph1">![</ph>ベースモデル MyModel で定義されているコンポーネント MyArtifact、および MyArtifact の拡張クラスを持つ 2 つの依存モデル<ept id="p1">](./media/extensions-11.png)](./media/extensions-11.png)</ept>この例では、有効なクラスは、すべてのオリジナルのメソッドおよび拡張クラスからのすべてのパブリック コンポーネントを含む拡張モデルのクラスです。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="127">
          <source>The effective class isn't the same in every model, because it includes only the class extensions that are defined in a given model.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">有効なクラスは、特定のモデルで定義されているクラスの拡張機能のみが含まれているため、すべてのモデルで同じではありません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="128">
          <source>The following illustration shows the effective class of <bpt id="p1">**</bpt>MyArtifact<ept id="p1">**</ept> in the <bpt id="p2">**</bpt>MyExtensionModel<ept id="p2">**</ept> model.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">次の図は、<bpt id="p1">**</bpt>MyExtensionModel<ept id="p1">**</ept> モデルの <bpt id="p2">**</bpt>MyArtifact<ept id="p2">**</ept> の有効クラスを示しています。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="129">
          <source><bpt id="p1">[</bpt><ph id="ph1">![</ph>Effective class of MyArtifact in MyExtensionModel<ept id="p1">](./media/extensions-21.png)](./media/extensions-21.png)</ept> We will describe class extensions by using a class that is named <bpt id="p2">**</bpt>MyClass<ept id="p2">**</ept> in a model that is named <bpt id="p3">**</bpt>MyModel<ept id="p3">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">[</bpt><ph id="ph1">![</ph>MyExtensionModel で MyArtifact の有効なクラス<ept id="p1">](./media/extensions-21.png)](./media/extensions-21.png)</ept> <bpt id="p3">**</bpt>MyModel<ept id="p3">**</ept> という名前のモデル内の <bpt id="p2">**</bpt>MyClass<ept id="p2">**</ept> という名前のクラスを使用して、クラス拡張について説明します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="130">
          <source>We can add new methods and state to <bpt id="p1">**</bpt>MyClass<ept id="p1">**</ept> by introducing an extension class in the extension model (<bpt id="p2">**</bpt>MyExtensionModel<ept id="p2">**</ept>) that builds on top of (that is, has a dependency on) <bpt id="p3">**</bpt>MyModel<ept id="p3">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p3">**</bpt>MyModel<ept id="p3">**</ept> の上に構築される (つまり、MyModel に依存する) 拡張モデル (<bpt id="p2">**</bpt>MyExtensionModel<ept id="p2">**</ept>) に拡張クラスを導入することで、<bpt id="p1">**</bpt>MyClass<ept id="p1">**</ept> に新しいメソッドと状態を追加できます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="131">
          <source>Extension class declarations</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">拡張子のクラス宣言</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="132">
          <source>Extension classes are classes that are adorned with the <bpt id="p1">**</bpt>ExtensionOf<ept id="p1">**</ept> attribute and that also have a name that has the <bpt id="p2">**</bpt><ph id="ph1">\_</ph>Extension<ept id="p2">**</ept> suffix.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">拡張子クラスに <bpt id="p1">**</bpt>ExtensionOf<ept id="p1">**</ept> 属性によって飾られているクラスで、<bpt id="p2">**</bpt><ph id="ph1">\_</ph>拡張子<ept id="p2">**</ept>接尾語という名も持っています。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="133">
          <source>(This restriction on the naming might be removed later.) The name of the extension class is otherwise unimportant.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">(この名前付けの制限は、後で削除される可能性があります。) 拡張クラスの名前は、それ以外の場合重要ではありません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="134">
          <source>The class augments the artifact that is specified in the <bpt id="p1">**</bpt>ExtensionOf<ept id="p1">**</ept> attribute, as shown in the following example.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このクラスは、次の例に示すように、<bpt id="p1">**</bpt>ExtensionOf<ept id="p1">**</ept> 属性で指定されたコンポーネントを補強します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="135">
          <source>Because the classes are instantiated by the runtime system, it's not meaningful to derive from the extension class.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">クラスはランタイム システムによってインスタンス化されるため、拡張クラスから派生する意味がありません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="136">
          <source>Therefore, the extension class must be marked as <bpt id="p1">**</bpt>final<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">したがって、拡張クラスは <bpt id="p1">**</bpt>final<ept id="p1">**</ept> としてマークする必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="137">
          <source>The <bpt id="p1">**</bpt>classStr<ept id="p1">**</ept> compile-time function must be used and has two purposes:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>classStr<ept id="p1">**</ept> コンパイル時関数は使用する必要があり、2 つの目的があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="138">
          <source>It produces a compilation error if the <bpt id="p1">**</bpt>MyClass<ept id="p1">**</ept> class doesn't exist.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>MyClass<ept id="p1">**</ept> クラスが存在しない場合、コンパイル エラーを生成します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="139">
          <source>The compile-time function that is used tells the compiler what kind of artifact is augmented.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">どのような種類のコンポーネントが拡張されるかをコンパイラに知らせるために使用するコンパイル時関数。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="140">
          <source>Artifact names by themselves don't uniquely identify a given artifact to augment.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">コンポーネント名単独では、拡張するために指定されたコンポーネントを一意に識別しません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="141">
          <source>For example, forms can have the same names as tables, classes, and enums.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">たとえば、フォームはテーブル、クラス、および列挙として同じ名前を持つことができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="142">
          <source>Any number of extension classes can augment a given artifact in a particular model.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">任意の数の拡張クラスが、特定のモデル内で付与されたコンポーネントを強化することができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="143">
          <source>Extension classes are never referenced directly by the programmer, only by the runtime system.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">拡張子クラスは、ランタイム システムでのみプログラマが直接参照することはありません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="144">
          <source>Extension class inheritance</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">拡張子のクラス継承</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="145">
          <source>Any class that inherits from an augmented class also inherits the effective class.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">拡張されたクラスから継承するクラスも、有効なクラスを継承します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="146">
          <source>In other words, the classes that inherit from a class that has extensions inherit the methods that are defined in the extension classes.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">つまり、拡張機能を持つクラスから継承するクラスは、拡張クラスで定義されているメソッドを継承します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="147">
          <source>Constructors</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">コンストラクター</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="148">
          <source>X++ supports both instance constructors and static constructors.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">X++ はインスタンス コンストラクターおよび静的コンストラクターの両方をサポートしています。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="149">
          <source>Instance constructors</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">インスタンス コンストラクター</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="150">
          <source>The instance constructor is the method that is named <bpt id="p1">**</bpt>new<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">インスタンス コンストラクターは、<bpt id="p1">**</bpt>new<ept id="p1">**</ept> という名前のメソッドです。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="151">
          <source>The instance constructor that is defined in an extension class can't have parameters.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">拡張クラスで定義されているインスタンス コンストラクターはパラメーターを指定できません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="152">
          <source>Instances of the extension classes are created, and the runtime system calls their constructors as required by the usage scenario.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">拡張クラスのインスタンスが作成され、ランタイム システムが使用シナリオで必要なコンストラクターを呼び出します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="153">
          <source>These constructors are never explicitly called by your code.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">これらのコンストラクターは、コードによって明示的に呼び出されることはありません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="154">
          <source>Constructors are useful for initializing the state of the extension objects.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">コンストラクターは、拡張オブジェクトの状態を初期化するのに便利です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="155">
          <source>It's guaranteed that the constructor that is provided in an extension class will be called one time before any instance method or the instance state on the extension class is accessed.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">拡張機能クラスのインスタンス メソッドまたはインスタンスの状態にアクセスする前に、拡張機能クラスに提示されているコンストラクターが 1 回呼び出されることが保証されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="156">
          <source>However, if no such references are made, the constructor isn't called.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ただし、そのような参照が行われない場合、コンストラクタは呼び出されません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="157">
          <source>Static constructors</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">静的コンストラクター</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="158">
          <source>Static constructors are the parameter-less static methods that are named <bpt id="p1">**</bpt>typenew<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">静的コンストラクターは、<bpt id="p1">**</bpt>typenew<ept id="p1">**</ept> と呼ばれるパラメーターなしの静的メソッドです。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="159">
          <source>Static constructors can be defined on extension classes.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">静的コンストラクターは、拡張クラスで定義することができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="160">
          <source>It's guaranteed that the runtime system will call the constructor before the first reference to the extension type.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ランタイム システムが拡張機能の種類を最初に参照する前にコンストラクターを呼び出すことが保証されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="161">
          <source>You can't assume any particular order of invocation for static construction among a set of extensions.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">拡張子のセットの間での静的コンストラクションの呼び出しの特定の任意の順序を想定することはできません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="162">
          <source>Methods</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">メソッド</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="163">
          <source>The public methods that are defined in extension classes provide additional functionality to the augmented class in the context of the model where the extension class is defined.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">拡張クラスで定義されているパブリック メソッドは、拡張クラスが定義されているモデルのコンテキストで、拡張クラスに追加の機能を提供します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="164">
          <source>Only public methods are exposed in this way.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この方法で、パブリック メソッドだけが公開されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="165">
          <source>You can define private methods to help implement the public methods, but those private methods aren't part of the effective class.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">パブリック メソッドの実装に役立てるためにプライベート メソッドを定義することができますが、これらのプライベート メソッドは有効なクラスの一部ではありません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="166">
          <source>Because extension classes are final, methods can't be marked as <bpt id="p1">**</bpt>protected<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">拡張クラスは最終的なものなので、メソッドを<bpt id="p1">**</bpt>保護された<ept id="p1">**</ept>ものとしてマークすることはできません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="167">
          <source>Instance methods</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">インスタンス メソッド</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="168">
          <source>The following example defines an extension method that is named <bpt id="p1">**</bpt>ExtensionMethod<ept id="p1">**</ept> and that augments <bpt id="p2">**</bpt>MyClass<ept id="p2">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">次の例では、<bpt id="p1">**</bpt>ExtensionMethod<ept id="p1">**</ept> という名前の拡張メソッドを定義し、<bpt id="p2">**</bpt>MyClass<ept id="p2">**</ept> を補強します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="169">
          <source>The public instance method (<bpt id="p1">**</bpt>ExtensionMethod<ept id="p1">**</ept>) is defined in the extension class.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">パブリック インスタンス メソッド (<bpt id="p1">**</bpt>ExtensionMethod<ept id="p1">**</ept>) は、拡張クラスで定義されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="170">
          <source>Therefore, it's available just as if it were defined in <bpt id="p1">**</bpt>MyClass<ept id="p1">**</ept> in the context of the model where the extension class is defined.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">したがって、拡張クラスが定義されているモデルのコンテキストで <bpt id="p1">**</bpt>MyClass<ept id="p1">**</ept> で定義されているかのように使用できます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="171">
          <source>The following example shows how to call the method in the model.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">次の例は、モデル内のメソッドを呼び出す方法を示しています。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="172">
          <source>Note that the instance method that is defined in the extension class is used as an instance method on the augmented artifact.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">拡張クラスで定義されているインスタンス メソッドは、強化されたコンポーネントのインスタンス メソッドとして使用されることに注意してください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="173">
          <source>An extension method can access public members only from the artifact that it augments (Access to protected methods and members is also supported if you are on platform update 9 or newer).</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">拡張メソッドは、それが補強するコンポーネントからのみパブリック メンバーにアクセスできます (プラットフォーム更新プログラム 9 またはそれ以降を使用している場合、保護されたメソッドおよびメンバーへのアクセスもサポートされています)。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="174">
          <source>This behavior is by design.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この動作は仕様です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="175">
          <source>No artifact should be able to interact directly with state and methods that are explicitly hidden through the <bpt id="p1">**</bpt>private<ept id="p1">**</ept>, or <bpt id="p2">**</bpt>internal<ept id="p2">**</ept> keywords.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">コンポーネントは、<bpt id="p1">**</bpt>private<ept id="p1">**</ept>、または <bpt id="p2">**</bpt>internal<ept id="p2">**</ept> キーワードを通じて明示的に非表示にされる状態およびメソッドと直接やり取りできるようにする必要はありません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="176">
          <source>Otherwise, direct interaction with explicitly hidden state and methods could cause malfunction by invalidating key implementation assumptions in those artifacts.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">それ以外の場合、明示的に非表示な状態とメソッドを直接操作すると、それらのコンポーネントの重要な実装の前提条件を無効にすることで障害が発生する可能性があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="177">
          <source>Methods and statements in the method body can use the <bpt id="p1">**</bpt>this<ept id="p1">**</ept> keyword.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">メソッドとメソッド本体のステートメントは、<bpt id="p1">**</bpt>this<ept id="p1">**</ept> キーワードを使用できます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="178">
          <source>In this context, the type of <bpt id="p1">**</bpt>this<ept id="p1">**</ept> is the effective class of the augmented artifact.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このコンテキストでは、<bpt id="p1">**</bpt>this<ept id="p1">**</ept> の型は強化されたコンポーネントの有効なクラスです。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="179">
          <source>Static methods</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">静的メソッド</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="180">
          <source>Methods that are defined as public and static in the extension class are available as static methods on the artifact that is augmented.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">拡張クラスでパブリックおよび静的として定義されているメソッドは、強化されているコンポーネントの静的メソッドとして使用できます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="181">
          <source>The following example shows how to call the method in the model.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">次の例は、モデル内のメソッドを呼び出す方法を示しています。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="182">
          <source>A static method can access the public static methods and state in the effective class of the augmented artifact.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">静的メソッドは、パブリックの静的メソッドおよび強化されたコンポーネントの有効なクラスの状態にアクセスできます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="183">
          <source>As an interesting side effect, static extension methods on the <bpt id="p1">**</bpt>Global<ept id="p1">**</ept> class become available in the language as functions, which are available without any prefix.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">興味深い副作用として、<bpt id="p1">**</bpt>グローバル<ept id="p1">**</ept> クラスの静的拡張メソッドは接頭語なしで利用できる関数として言語で使用可能になります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="184">
          <source>State</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">行政単位 (区画)</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="185">
          <source>In addition to providing static and instance methods to an artifact, you can add instance state and static state.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">成果物に対する静的およびインスタンス メソッドを提供することに加えて、インスタンス状態と静的状態を追加できます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="186">
          <source>Instance state</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">インスタンスの状態</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="187">
          <source>Instance state, which is state that pertains to a particular instance of an artifact, can be specified on extension classes.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">コンポーネントの特定のインスタンスに関連する状態であるインスタンスの状態は、拡張クラスで指定できます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="188">
          <source>The following example defines a state that is named <bpt id="p1">**</bpt>state<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">次の例では、<bpt id="p1">**</bpt>state<ept id="p1">**</ept> という名前の状態を定義しています。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="189">
          <source>The following example shows how to use <bpt id="p1">**</bpt>state<ept id="p1">**</ept> in your code.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">次の例は、コード内で <bpt id="p1">**</bpt>state<ept id="p1">**</ept> を使用する方法を示しています。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="190">
          <source>Static state</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">静的な状態</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="191">
          <source>Static state applies to the type instead of an instance of the type.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">静的状態は、タイプのインスタンスではなくタイプに適用されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="192">
          <source>The following example shows a static extension state.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">次の例は、静的な拡張状態を示しています。</target></trans-unit>
      </group>
    </body>
  </file>
</xliff>