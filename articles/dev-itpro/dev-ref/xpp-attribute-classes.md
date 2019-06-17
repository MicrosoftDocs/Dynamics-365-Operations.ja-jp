<?xml version="1.0" encoding="UTF-8"?>
<xliff xmlns:logoport="urn:logoport:xliffeditor:xliff-extras:1.0" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns="urn:oasis:names:tc:xliff:document:1.2" xmlns:xliffext="urn:microsoft:content:schema:xliffextensions" version="1.2" xsi:schemaLocation="urn:oasis:names:tc:xliff:document:1.2 xliff-core-1.2-transitional.xsd">
  <file datatype="xml" source-language="en-US" original="xpp-attribute-classes.md" target-language="ja-JP">
    <header>
      <tool tool-company="Microsoft" tool-version="1.0-7889195" tool-name="mdxliff" tool-id="mdxliff"/>
      <xliffext:skl_file_name>xpp-attribute-classes.191623.6dfeb8e739f6dc26d73501001c83eb15ee3a0fd5.skl</xliffext:skl_file_name>
      <xliffext:version>1.2</xliffext:version>
      <xliffext:ms.openlocfilehash>6dfeb8e739f6dc26d73501001c83eb15ee3a0fd5</xliffext:ms.openlocfilehash>
      <xliffext:ms.sourcegitcommit>9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b</xliffext:ms.sourcegitcommit>
      <xliffext:ms.lasthandoff>05/15/2019</xliffext:ms.lasthandoff>
      <xliffext:ms.openlocfilepath>articles\dev-itpro\dev-ref\xpp-attribute-classes.md</xliffext:ms.openlocfilepath>
    </header>
    <body>
      <group extype="content" id="content">
        <trans-unit xml:space="preserve" translate="yes" id="101" restype="x-metadata">
          <source>X++ attribute classes</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">X++ 属性クラス</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="102" restype="x-metadata">
          <source>This topic describes the use of attributes in X++.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このトピックでは、X++ での属性の使用について説明します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="103">
          <source>X++ attribute classes</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">X++ 属性クラス</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="104">
          <source>This topic describes the use of attributes in X++.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このトピックでは、X++ での属性の使用について説明します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="105">
          <source>An attribute is a non-abstract class that extends (inherits from) the <bpt id="p1">**</bpt>SysAttribute<ept id="p1">**</ept> class.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">属性は、<bpt id="p1">**</bpt>SysAttribute<ept id="p1">**</ept> クラスを拡張 (継承) する非抽象クラスです。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="106">
          <source>Attributes represent or store metadata about types and methods.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">属性は型およびメソッドに関するメタデータを表すか、または保存します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="107">
          <source>An attribute can be attached to a class, an interface, or a method of a class, interface, or table.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">属性はクラス、インターフェイス、クラスのメソッド、インターフェイスまたはテーブルに関連付けることができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="108">
          <source>Creating an attribute class</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">属性クラスを作成しています</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="109">
          <source>An attribute class can extend the <bpt id="p1">**</bpt>SysAttribute<ept id="p1">**</ept> class directly, or it can extend any descendant of the <bpt id="p2">**</bpt>SysAttribute<ept id="p2">**</ept> class.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">属性クラスは <bpt id="p1">**</bpt>SysAttribute<ept id="p1">**</ept> クラスを直接拡張したり、<bpt id="p2">**</bpt>SysAttribute<ept id="p2">**</ept> クラスのすべての子孫を拡張することもできます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="110">
          <source>The <bpt id="p1">**</bpt>SysAttribute<ept id="p1">**</ept> class cannot be used as an attribute because it is declared <bpt id="p2">**</bpt>abstract<ept id="p2">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>SysAttribute<ept id="p1">**</ept> クラスは、<bpt id="p2">**</bpt>abstract<ept id="p2">**</ept> と宣言されているため、属性として使用できません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="111">
          <source>The following example shows the declaration and design of an ordinary attribute class that you could create.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">次の例は、作成できる通常の属性クラスの宣言とデザインを示しています。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="112">
          <source>Decorating a class with an attribute</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">属性を持つクラスの修飾</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="113">
          <source>The following example shows a class and a method that are decorated with the <bpt id="p1">**</bpt>PracticeAttribute<ept id="p1">**</ept> given in the previous example.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">次の例では、前の例で与えられた <bpt id="p1">**</bpt>PracticeAttribute<ept id="p1">**</ept> で装飾されたクラスとメソッドを示しています。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="114">
          <source>If the constructor of the attribute takes no parameters, the parentheses for the parameters are optional.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">属性のコンストラクターがパラメーターを取らない場合、パラメーターのかっこはオプションになります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="115">
          <source>The attribute decoration could be <ph id="ph1">`[AnotherAttribute]`</ph> without parentheses.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">属性の修飾は、かっこのない <ph id="ph1">`[AnotherAttribute]`</ph> であり可能性があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="116">
          <source>Attribute constructors</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">属性コンストラクター</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="117">
          <source>You can enable your attribute class to store tailored metadata each time it is used to decorate a class, by having its constructor take parameters.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">コンストラクターがパラメーターを持つようにすることで、クラスを修飾するためにメタデータが使用されるたびに、属性クラスが作成済みメタデータを格納するようにできます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="118">
          <source>The parameters for the constructor must be literals of the primitive types, such as <bpt id="p1">**</bpt>int,<ept id="p1">**</ept> <bpt id="p2">**</bpt>enum,<ept id="p2">**</ept> or <bpt id="p3">**</bpt>str<ept id="p3">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">コンストラクターのパラメータは、<bpt id="p1">**</bpt>int<ept id="p1">**</ept>、<bpt id="p2">**</bpt>enum<ept id="p2">**</ept>、または <bpt id="p3">**</bpt>str<ept id="p3">**</ept> などの、プリミティブ型のリテラルにする必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="119">
          <source>The compiler does not construct an instance of the attribute class.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">コンパイラは、属性クラスのインスタンスを構築しません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="120">
          <source>It stores the name of the attribute class, plus the literal values for its constructor.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">属性クラスの名前、およびコンストラクターのリテラル値を格納します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="121">
          <source>Therefore, if the logic in an attribute constructor would throw an exception, the exception would not be found by decorating a class with the attribute.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">したがって、属性コンストラクター内のロジックが例外をスローすると、その属性を持つクラスを修飾することによって例外が見つかりません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="122">
          <source>The exception would be found later when a process looks at a class to see the attribute it is decorated with.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">例外は、後でプロセスがクラスを調べて、それが装飾されている属性を見るときに見つかります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="123">
          <source>That is when the attribute is constructed.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">属性が作成されたときです。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="124">
          <source>Naming conventions</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">名前付け規則</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="125">
          <source>All attribute classes have the suffix <bpt id="p1">**</bpt>Attribute<ept id="p1">**</ept> in their name.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">すべての属性クラスには名前に接尾語<bpt id="p1">**</bpt>属性<ept id="p1">**</ept>があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="126">
          <source>The <bpt id="p1">**</bpt>Attribute<ept id="p1">**</ept> suffix is the name convention that we recommend, but it is not a system requirement.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>属性<ept id="p1">**</ept> サフィックスは、推奨される名前付け規則ですが、システム要件ではありません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="127">
          <source>You can determine whether a class <bpt id="p1">**</bpt>extends<ept id="p1">**</ept> directly from <bpt id="p2">**</bpt>SysAttribute<ept id="p2">**</ept> by selecting the class in the <bpt id="p3">**</bpt>Application Explorer<ept id="p3">**</ept> and reviewing the <bpt id="p4">**</bpt>Extends<ept id="p4">**</ept> property in the <bpt id="p5">**</bpt>Properties<ept id="p5">**</ept> window.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p3">**</bpt>アプリケーション エクスプローラー<ept id="p3">**</ept> 内のクラスを選択して <bpt id="p5">**</bpt>プロパティ<ept id="p5">**</ept> ウインドウで <bpt id="p4">**</bpt>拡張<ept id="p4">**</ept> プロパティを確認することにより、クラスが <bpt id="p2">**</bpt>SysAttribute<ept id="p2">**</ept> から直接 <bpt id="p1">**</bpt>拡張<ept id="p1">**</ept> されるか決定することができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="128">
          <source>SysObsoleteAttribute</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">SysObsoleteAttribute</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="129">
          <source>The system provides several attributes, including the <bpt id="p1">**</bpt>SysObsoleteAttribute<ept id="p1">**</ept> class.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">システムは、<bpt id="p1">**</bpt>SysObsoleteAttribute<ept id="p1">**</ept> クラスを含むいくつかの属性を提供します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="130">
          <source>One use of the <bpt id="p1">**</bpt>SysObsoleteAttribute<ept id="p1">**</ept> class is to notify the compiler that the compile should fail if a particular method is called in the source code.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>SysObsoleteAttribute<ept id="p1">**</ept> クラスの 1 つの使用方法は、ソース コード内の特定のメソッドが呼び出された場合、コンパイルが失敗することをコンパイラに通知することです。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="131">
          <source>The compiler rejects the compile, and displays the specific message that is stored in this use of the attribute.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">コンパイラはコンパイルを拒否し、この属性の使用に格納されている特定のメッセージを表示します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="132">
          <source>The <bpt id="p1">**</bpt>SysObsoleteAttribute<ept id="p1">**</ept> class can also be used to notify the compiler to issue warning messages instead of errors.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>SysObsoleteAttribute<ept id="p1">**</ept> クラスを使用すると、エラーではなく問題の警告メッセージをコンパイラに通知することもできます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="133">
          <source>SysObsoleteAttribute code example</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">SysObsoleteAttribute コードの例</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="134">
          <source>Metadata reflection</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">メタデータ リフレクション</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="135">
          <source>You use reflection to find the attribute metadata that is attached to a class.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">クラスに関連付けられている属性メタデータを検索するには、リフレクションを使用します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="136">
          <source>The classes to use for attribute reflection are as follows:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">属性リフレクションに使用するクラスは次のとおりです。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="137">
          <source><bpt id="p1">**</bpt>DictClass<ept id="p1">**</ept> class – For classes and interfaces.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>DictClass<ept id="p1">**</ept> クラス - クラスおよびインタフェース用です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="138">
          <source><bpt id="p1">**</bpt>DictMethod<ept id="p1">**</ept> class – For methods on classes, interfaces, or tables.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>DictMethod<ept id="p1">**</ept> クラス - クラス、インターフェイス、またはテーブルのメソッド用です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="139">
          <source>On the previous reflection classes, the methods for reflecting on attribute metadata are as follows:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">前のリフレクション クラスで、属性メタデータを反映した方法は次のとおりです。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="140">
          <source><bpt id="p1">**</bpt>getAllAttributes<ept id="p1">**</ept> method</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>getAllAttributes<ept id="p1">**</ept> メソッド</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="141">
          <source><bpt id="p1">**</bpt>getAttribute<ept id="p1">**</ept> method</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>getAttribute<ept id="p1">**</ept> メソッド</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="142">
          <source><bpt id="p1">**</bpt>getAttributedClasses<ept id="p1">**</ept> method</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>getAttributedClasses<ept id="p1">**</ept> メソッド</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="143">
          <source><bpt id="p1">**</bpt>getAttributes<ept id="p1">**</ept> method</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>getAttributes<ept id="p1">**</ept> メソッド</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="144">
          <source>There is no mechanism for listing all methods or classes that are adorned with a particular attribute from X++ code.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">X++ コードから特定の属性で飾られたすべてのメソッドまたはクラスをリストするメカニズムはありません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="145">
          <source>However, because the X++ compiler records this information in the cross reference database, the information can be mined from there.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ただし、X++ コンパイラは、相互参照データベースにこの情報を記録するため、そこから情報を得ることができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="146">
          <source>Metadata reflection code example</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">メタデータ リフレクションのコードの例</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="147">
          <source>You use the <bpt id="p1">**</bpt>DictMethod<ept id="p1">**</ept> class to find the metadata value of an attribute that is decoration on a method.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">メソッドを修飾する属性のメタデータ値を検索するには、<bpt id="p1">**</bpt>DictMethod<ept id="p1">**</ept> クラスを使用します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="148">
          <source>The following code example uses the <bpt id="p1">**</bpt>SysEntryPointAttribute<ept id="p1">**</ept> class as the attribute.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">次のコード例では、<bpt id="p1">**</bpt>SysEntryPointAttribute<ept id="p1">**</ept> クラスを属性として使用しています。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="149">
          <source>It accepts your parameter values for the method name, and for the name of the class that contains the method.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">メソッド名およびそのメソッドを含むクラスの名前にパラメーター値を受け入れます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="150">
          <source>The <bpt id="p1">**</bpt>parmChecked<ept id="p1">**</ept> method is particular to the <bpt id="p2">**</bpt>SysEntryPointAttribute<ept id="p2">**</ept> class, and it is not inherited from its base class <bpt id="p3">**</bpt>SysAttribute<ept id="p3">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>parmChecked<ept id="p1">**</ept> メソッドは、<bpt id="p2">**</bpt>SysEntryPointAttribute<ept id="p2">**</ept> クラスに固有であり、基本クラス <bpt id="p3">**</bpt>SysAttribute<ept id="p3">**</ept> からから継承されません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="151">
          <source>Each attribute class can have its own method name for its metadata.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">各属性クラスは、メタデータの独自のメソッド名を持つことが可能です。</target></trans-unit>
      </group>
    </body>
  </file>
</xliff>