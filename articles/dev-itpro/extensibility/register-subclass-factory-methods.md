<?xml version="1.0" encoding="UTF-8"?>
<xliff xmlns:logoport="urn:logoport:xliffeditor:xliff-extras:1.0" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns="urn:oasis:names:tc:xliff:document:1.2" xmlns:xliffext="urn:microsoft:content:schema:xliffextensions" version="1.2" xsi:schemaLocation="urn:oasis:names:tc:xliff:document:1.2 xliff-core-1.2-transitional.xsd">
  <file datatype="xml" source-language="en-US" original="register-subclass-factory-methods.md" target-language="ja-JP">
    <header>
      <tool tool-company="Microsoft" tool-version="1.0-7889195" tool-name="mdxliff" tool-id="mdxliff"/>
      <xliffext:skl_file_name>register-subclass-factory-methods.febb87.5e5727319089bb30de4fbfb0e6f61596f5e9ad80.skl</xliffext:skl_file_name>
      <xliffext:version>1.2</xliffext:version>
      <xliffext:ms.openlocfilehash>5e5727319089bb30de4fbfb0e6f61596f5e9ad80</xliffext:ms.openlocfilehash>
      <xliffext:ms.sourcegitcommit>9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b</xliffext:ms.sourcegitcommit>
      <xliffext:ms.lasthandoff>05/15/2019</xliffext:ms.lasthandoff>
      <xliffext:ms.openlocfilepath>articles\dev-itpro\extensibility\register-subclass-factory-methods.md</xliffext:ms.openlocfilepath>
    </header>
    <body>
      <group extype="content" id="content">
        <trans-unit xml:space="preserve" translate="yes" id="101" restype="x-metadata">
          <source>Register subclasses for factory methods</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ファクトリ メソッドのサブクラスを登録</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="102" restype="x-metadata">
          <source>This topic describes how to register your own variations for the factories.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このトピックでは、独自のバリエーションを工場に登録する方法について説明します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="103">
          <source>Register subclasses for factory methods</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ファクトリ メソッドのサブクラスを登録</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="104">
          <source>Class inheritance is a central concept in X++, as in other object-oriented languages.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">クラス継承は、他のオブジェクト指向言語と同様に、X++ の中心的概念です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="105">
          <source>The object-oriented strategy pattern is used throughout the X++ business logic.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">オブジェクト指向戦略パターンは、X++ ビジネス ロジック全体で使用されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="106">
          <source>In this pattern, variations in behavior can be encapsulated by subclasses, and the business process uses an abstract base class or interface.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このパターンでは、動作のバリエーションをサブクラスでカプセル化することができ、業務プロセスが抽象基本クラスまたはインターフェイスを使用します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="107">
          <source>A factory method determines the variation that is used, by creating an instance of a specific subclass.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ファクトリ メソッドは、特定のサブクラスのインスタンスを作成することによって、使用されるバリエーションを決定します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="108">
          <source>This topic describes how to register your own variations for the factories.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このトピックでは、独自のバリエーションを工場に登録する方法について説明します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="109">
          <source>In X++, the factories use reflection to perform the following tasks:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">X++ では、ファクトリはリフレクションを使用して、次のタスクを実行します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="110">
          <source>Find the correct subclass.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">正しいサブクラスを検索します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="111">
          <source>The factory uses an extension framework to search all subclasses in a hierarchy for a specific set of attributes.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ファクトリは、拡張フレームワークを使用して、階層内のすべてのサブクラスで特定の属性セットを検索します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="112">
          <source>If the attributes that decorate a subclass match the parameters that were passed to the factory, that specific class is used.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">サブクラスを修飾する属性がファクトリに渡されたパラメータと一致する場合、その特定のクラスが使用されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="113">
          <source>Create an instance.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">インスタンスを作成します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="114">
          <source>After the right type is identified, reflection is used to create an instance of the class.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">正しいタイプが識別された後、リフレクションを使用してクラスのインスタンスを作成します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="115">
          <source>The following illustrations shows a typical decorated hierarchy.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">次の図は、一般的な装飾階層を示しています。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="116">
          <source>Class hierarchy that has three subclasses, each of which is decorated with an attribute</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">各サブクラスが属性で装飾されている、3 つのサブクラスを持つクラス階層</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="117">
          <source>In X++, two extension frameworks serve the same purpose.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">X++ では、2 つの拡張フレームワークは同じ目的で機能します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="118">
          <source>The implementer of the factory method determines which extension framework should be used:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ファクトリ メソッドの実装担当者は、使用する拡張フレームワークを決定します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="119">
          <source><bpt id="p1">[</bpt>SysExtension<ept id="p1">](https://blogs.msdn.microsoft.com/mfp/2013/06/12/sysextension-framework-to-the-rescue/)</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">[</bpt>SysExtension<ept id="p1">](https://blogs.msdn.microsoft.com/mfp/2013/06/12/sysextension-framework-to-the-rescue/)</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="120">
          <source>This extension framework uses custom attributes that make it easier to consume.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この拡張フレームワークは、利用しやすくするためにカスタム属性を使用します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="121">
          <source>It supports singletons that save a little performance when the same instance is created repeatedly.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">同じインスタンスが繰り返し作成されるときに、パフォーマンスを多少節約する単一をサポートします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="122">
          <source>This extension framework is especially useful for stateless subclasses.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この拡張フレームワークは、ステートレスなサブクラスに特に便利です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="123">
          <source>It seamlessly supports extensible enums that are often used to determine the variant.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">バリアントを決定するために頻繁に使用される拡張可能な列挙をシームレスにサポートしています。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="124">
          <source>SysPlugin</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">SysPlugin</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="125">
          <source>This extension framework is based on the Managed Extension Framework.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この拡張フレームワークは、Managed Extension Framework に基づいています。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="126">
          <source>The Managed Extension Framework makes the SysPlugin extension framework available to non-X++ code.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">マネージ拡張フレームワークは、SysPlugin 拡張フレームワークを非 X++ コードで使用できるようにします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="127">
          <source>It uses the <bpt id="p1">**</bpt>ExportMetadataAttribute<ept id="p1">**</ept> attribute to decorate the variants and is string-based.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>ExportMetadataAttribute<ept id="p1">**</ept> 属性を使用してバリアントを修飾し、文字列ベースとなります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="128">
          <source>It uses the <bpt id="p1">**</bpt>ExportAttribute<ept id="p1">**</ept> attribute to make the variant discoverable.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>ExportAttribute<ept id="p1">**</ept> 属性を使用してバリアントを見つけやすくします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="129">
          <source>Introduce a new variant</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">新しいバリアントの導入</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="130">
          <source>Identify the base class (or interface) of the variant that you must implement.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">実装する必要があるバリアントの基本クラス (またはインタフェース) を特定します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="131">
          <source>Create a new subclass of the base class, and implement your variation.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">基本クラスの新しいサブクラスを作成し、バリエーションを実装します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="132">
          <source>Identify which attribute is required in order to register your class.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">クラスを登録するために必要となる属性を識別します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="133">
          <source>There are two approaches:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">次の 2 つのアプローチがあります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="134">
          <source>Look for attributes that are defined on other subclasses in the hierarchy.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">階層内のその他のサブクラスで定義されている属性を検索します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="135">
          <source>Look at the implementation of the factory method.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ファクトリ メソッドの実装を確認します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="136">
          <source>That implementation will contain the attributes that the factory method is searching for.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">その実装には、ファクトリ メソッドが検索する属性が含まれます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="137">
          <source>Decorate your subclass with the attribute that was used to match your variation.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">バリエーションに一致するために使用された属性でサブクラスを修飾します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="138">
          <source><bpt id="p1">**</bpt>SysExtension example<ept id="p1">**</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>SysExtension 例<ept id="p1">**</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="139">
          <source><bpt id="p1">**</bpt>SysPlugin example<ept id="p1">**</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>SysPlugin 例<ept id="p1">**</ept></target></trans-unit>
      </group>
    </body>
  </file>
</xliff>