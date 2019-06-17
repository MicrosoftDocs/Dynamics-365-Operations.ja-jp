<?xml version="1.0" encoding="UTF-8"?>
<xliff xmlns:logoport="urn:logoport:xliffeditor:xliff-extras:1.0" xmlns:tilt="urn:logoport:xliffeditor:tilt-non-translatables:1.0" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns="urn:oasis:names:tc:xliff:document:1.2" xmlns:xliffext="urn:microsoft:content:schema:xliffextensions" version="1.2" xsi:schemaLocation="urn:oasis:names:tc:xliff:document:1.2 xliff-core-1.2-transitional.xsd">
  <file datatype="xml" source-language="en-US" original="method-wrapping-coc.md" target-language="ja-JP">
    <header>
      <tool tool-company="Microsoft" tool-version="1.0-7889195" tool-name="mdxliff" tool-id="mdxliff"/>
      <xliffext:skl_file_name>method-wrapping-coc.98bedd.bfc2d9c637de579562160fc982c9de32dc162437.skl</xliffext:skl_file_name>
      <xliffext:version>1.2</xliffext:version>
      <xliffext:ms.openlocfilehash>bfc2d9c637de579562160fc982c9de32dc162437</xliffext:ms.openlocfilehash>
      <xliffext:ms.sourcegitcommit>9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b</xliffext:ms.sourcegitcommit>
      <xliffext:ms.lasthandoff>05/15/2019</xliffext:ms.lasthandoff>
      <xliffext:ms.openlocfilepath>articles\dev-itpro\extensibility\method-wrapping-coc.md</xliffext:ms.openlocfilepath>
    </header>
    <body>
      <group extype="content" id="content">
        <trans-unit xml:space="preserve" translate="yes" id="101" restype="x-metadata">
          <source>Class extension - Method wrapping and Chain of Command</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">クラスの拡張機能 - メソッドのラッピングとコマンド チェーン</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="102" restype="x-metadata">
          <source>This topic discusses how to extend the business logic of public and protected methods by using method wrapping.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このトピックでは、メソッド ラッピングを使用してパブリック メソッドと保護メソッドのビジネス ロジックを拡張する方法について説明します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="103">
          <source>Class extension via method wrapping and Chain of Command (CoC)</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">メソッドのラッピングとコマンド チェーン経由のクラスの拡張機能 (CoC)</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="104">
          <source>The functionality for class extension, or class augmentation, has been improved in Microsoft Dynamics 365 for Finance and Operations.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">クラス拡張やクラス強化の機能が、Microsoft Dynamics 365 for Finance and Operations で強化されました。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="105">
          <source>You can now wrap logic around methods that are defined in the base class that you're augmenting.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">強化対象である基本クラスで定義されたメソッド関連のロジックをラップできるようになりました。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="106">
          <source>You can extend the logic of public and protected methods without having to use event handlers.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">イベント ハンドラーを使用せずに、パブリック メソッドとプロテクト メソッドのロジックを拡張することができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="107">
          <source>When you wrap a method, you can also access public and protected methods, and variables of the base class.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">メソッドをラップするとき、基本クラスのパブリック メソッドと保護されたメソッド、および変数にもアクセスできます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="108">
          <source>In this way, you can start transactions and easily manage state variables that are associated with your class.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この方法で、トランザクションを開始し、クラスに関連付けられた状態変数を容易に管理することができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="109">
          <source>For example, a model contains the following code.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">たとえば、モデルには次のコードが含まれています。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="110">
          <source>You can now augment the functionality of the <bpt id="p1">**</bpt>doSomething<ept id="p1">**</ept> method inside an extension class by reusing the same method name.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">同じメソッド名を再利用することにより、拡張クラス内の <bpt id="p1">**</bpt>doSomething<ept id="p1">**</ept> メソッドの機能を強化することができるようになりました。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="111">
          <source>An extension class must belong to a package that references the model where the augmented class is defined.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">拡張クラスは強化されたクラスが定義されているモデルを参照するパッケージに属している必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="112">
          <source>In this example, the wrapper around <bpt id="p1">**</bpt>doSomething<ept id="p1">**</ept> and the required use of the <bpt id="p2">**</bpt>next<ept id="p2">**</ept> keyword create a Chain of Command (CoC) for the method.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この例では、<bpt id="p1">**</bpt>doSomething<ept id="p1">**</ept> のラッパーと <bpt id="p2">**</bpt>next<ept id="p2">**</ept> キーワードを必要に応じて使用することにより、メソッドのコマンド チェーン (CoC) を作成します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="113">
          <source>CoC is a design pattern where a request is handled by a series of receivers.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">CoC は、要求が一連の受信者によって処理される設計パターンです。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="114">
          <source>The pattern supports loose coupling of the sender and the receivers.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">パターンは、送信者と受信者の疎結合をサポートします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="115">
          <source>We now run the following code.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">現在は次のコードを実行します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="116">
          <source>When this code is run, the system finds any method that wraps the <bpt id="p1">**</bpt>doSomething<ept id="p1">**</ept> method.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このコードが実行されると、システムは、<bpt id="p1">**</bpt>doSomething<ept id="p1">**</ept> メソッドをラップするメソッドを検索します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="117">
          <source>The system randomly runs one of these methods, such as the <bpt id="p1">**</bpt>doSomething<ept id="p1">**</ept> method of the <bpt id="p2">**</bpt>BusinessLogic1_Extension<ept id="p2">**</ept> class.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">システムは、<bpt id="p2">**</bpt>BusinessLogic1_Extension<ept id="p2">**</ept> クラスの <bpt id="p1">**</bpt>doSomething<ept id="p1">**</ept> メソッドなど、これらのメソッドの 1 つをランダムに実行します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="118">
          <source>When the call to the next <bpt id="p1">**</bpt>doSomething<ept id="p1">**</ept> method occurs, the system randomly picks another method in the CoC.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">次の <bpt id="p1">**</bpt>doSomething<ept id="p1">**</ept> メソッドへの呼び出しが発生すると、システムは CoC 内の別のメソッドをランダムに選択します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="119">
          <source>If no more wrapped methods exist, the system calls the original implementation.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ラップされたメソッドがこれ以上ない場合は、システムは元の実装を呼び出します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="120">
          <source>Supported versions</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">サポートされているバージョン</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="121">
          <source>The functionality that is described in this topic (CoC and access to protected methods and variables) is available in Platform update 9.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このトピックで説明する機能 (CoC および保護されたメソッドと変数へのアクセス) は、Platform update 9 で利用できます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="122">
          <source>However, the class that is being augmented must also be compiled on Platform update 9 or later.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ただし、強化されているクラスは、プラットフォーム更新プログラム 9 またはそれ以降でコンパイルされる必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="123">
          <source>As of August 2017, all current releases of the applications for Finance and Operations have been compiled on Platform update 8 or earlier.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">2017 年 8 月現在、Finance and Operations のアプリケーションの現在のリリースはすべて Platform Update 8 またはそれ以前でコンパイルされています。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="124">
          <source>Therefore, to wrap a method that is defined in a base package (such as Application Suite), you must recompile that base package on Platform update 9 or later.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">したがって、基本パッケージ (Application Suite など) で定義されているメソッドをラップするには、プラットフォーム更新 9 以降でその基本パッケージを再コンパイルする必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="125">
          <source>As an example: If you create your own extension model that is augmenting a class that exists in the Application Suite model, and if you are using CoC or accessing protected methods/variables, you will need to build both Application Suite and your extension model.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">例: アプリケーション スイート モデルに存在するクラスを増補する独自の拡張モデルを作成し、CoC を使用している場合や保護されたメソッド/変数にアクセスする場合は、アプリケーション スイートと拡張モデルの両方を構築する必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="126">
          <source>You will also need to create a deployable package that includes both models in order to deploy this functionality on a runtime environment.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ランタイム環境でこの機能を配置するには、両方のモデルを含む配置可能なパッケージを作成する必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="127">
          <source>This is a temporary situation until the next release of the Dynamics 365 for Finance and Operations application.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">これは、Dynamics 365 for Finance and Operations アプリケーションの次のリリースまでの一時的な状況です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="128">
          <source>Capabilities</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">処理能力</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="129">
          <source>The following sections give more details about the capabilities of method wrapping and CoC.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">次のセクションでは、ラッピング メソッドと CoC メソッドの機能について詳しく説明します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="130">
          <source>Wrapping public and protected methods</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">パブリック メソッドと保護対象メソッドのラッピング</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="131">
          <source>Protected or public methods of classes, tables, data entities, or forms can be wrapped by using an extension class.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">クラス、テーブル、データ エンティティ、またはフォームの保護またはパブリック メソッドは、拡張子クラスを使用してラップできます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="132">
          <source>The wrapper method must have the same signature as the base method.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ラッパー メソッドは、基本メソッドと同じシグネチャを持つ必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="133">
          <source>When you augment form classes, only root-level methods can be wrapped.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">フォーム クラスを拡張するときは、ルート レベルのメソッドのみをラップできます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="134">
          <source>You can't wrap methods that are defined in nested classes.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">入れ子になったクラスで定義されているメソッドをラップすることはできません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="135">
          <source>Currently, only methods that are defined in regular classes can be wrapped.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">現在のところ、通常のクラスで定義されているメソッドのみラップできます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="136">
          <source>Methods that are defined in extension classes can't be wrapped by augmenting the extension classes.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">拡張クラスで定義されているメソッドは、拡張クラスを強化してラップできません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="137">
          <source>This capability is planned for a future update.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この機能は、将来の更新で計画されています。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="138">
          <source>What about default parameters?</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">既定のパラメーターはどうなのですか ?</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="139">
          <source>Methods that have default parameters can be wrapped by extension classes.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">既定のパラメーターを持つメソッドは、拡張クラスでラップできます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="140">
          <source>However, the method signature in the wrapper method must not include the default value of the parameter.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ただし、ラッパー メソッドのメソッド シグネチャは、パラメータの既定値を含む必要がありません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="141">
          <source>For example, the following simple class has a method that has a default parameter.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">たとえば、次の簡単なクラスには、既定のパラメーターを持つメソッドがあります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="142">
          <source>In this case, the wrapper method must resemble the following example.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この場合、ラッパー メソッドは次の例のようにする必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="143">
          <source>In the <bpt id="p1">**</bpt>APerson_Extension<ept id="p1">**</ept> extension class, notice that the <bpt id="p2">**</bpt>salute<ept id="p2">**</ept> method doesn't include the default value of the <bpt id="p3">**</bpt>message<ept id="p3">**</ept> parameter.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>APerson_Extension<ept id="p1">**</ept> 拡張子クラスで、<bpt id="p2">**</bpt>salute<ept id="p2">**</ept> メソッドが<bpt id="p3">**</bpt>メッセージ<ept id="p3">**</ept> パラメーターの既定値に含まれていないことを確認します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="144">
          <source>Wrapping instance and static methods</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">インスタンス メソッドと静的メソッドをラッピング</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="145">
          <source>Instance and static methods can be wrapped by extension classes.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">インスタンスと静的メソッドは、拡張クラスでラップできます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="146">
          <source>If a static method is the target that will be wrapped, the method in the extension must be qualified by using the <bpt id="p1">**</bpt>static<ept id="p1">**</ept> keyword.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">静的メソッドがラップされるターゲットである場合、<bpt id="p1">**</bpt>静的<ept id="p1">**</ept>キーワードを使用して拡張内のメソッドを指定する必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="147">
          <source>For example, we have the following <bpt id="p1">**</bpt>A<ept id="p1">**</ept> class.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">たとえば、次の <bpt id="p1">**</bpt>A<ept id="p1">**</ept> クラスがあります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="148">
          <source>In this case, the wrapper method must resemble the following example.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この場合、ラッパー メソッドは次の例のようにする必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="149">
          <source>The ability to wrap static methods doesn't apply to forms.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">静的メソッドをラップする機能はフォームには適用されません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="150">
          <source>In X++, a form class isn't a new class, and can't be instantiated or referenced as a normal class.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">X++ では、フォーム クラスは新しいクラスではなく、インスタンスを作成したり通常クラスとして参照したりできません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="151">
          <source>Static methods in forms don't have any semantics.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">フォーム内の静的メソッドにはセマンティクスがありません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="152">
          <source>Wrapper methods must always call next</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ラッパー メソッドは常に次を呼び出す必要があります</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="153">
          <source>Wrapper methods in an extension class must always call <bpt id="p1">**</bpt>next<ept id="p1">**</ept>, so that the next method in the chain and, finally, the original implementation are always called.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">拡張クラス内のラッパー メソッドは常に <bpt id="p1">**</bpt>次<ept id="p1">**</ept> を呼び出す必要があるため、チェーン内の次のメソッド、および最後には常に元の実装が呼び出されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="154">
          <source>This restriction helps guarantee that every method in the chain contributes to the result.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この制限により、チェーン内のすべてのメソッドが結果に寄与することが保証されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="155">
          <source>In the current implementation of this restriction, the call to <bpt id="p1">**</bpt>next<ept id="p1">**</ept> must be in the first-level statements in the method body.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この制限の現在の実装では、<bpt id="p1">**</bpt>次<ept id="p1">**</ept>の呼び出しはメソッド本体の第 1 レベルのステートメントである必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="156">
          <source>Here are some important rules:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">いくつかの重要なルールを次に示します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="157">
          <source>Calls to <bpt id="p1">**</bpt>next<ept id="p1">**</ept> can't be done conditionally inside an <bpt id="p2">**</bpt>if<ept id="p2">**</ept> statement.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p2">**</bpt>if<ept id="p2">**</ept> 文の中で、条件付きで <bpt id="p1">**</bpt>next<ept id="p1">**</ept> への呼び出しを行うことはできません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="158">
          <source>Calls to <bpt id="p1">**</bpt>next<ept id="p1">**</ept> can't be done in <bpt id="p2">**</bpt>while<ept id="p2">**</ept>, <bpt id="p3">**</bpt>do-while<ept id="p3">**</ept>, or <bpt id="p4">**</bpt>for<ept id="p4">**</ept> loop statements.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p2">**</bpt>while<ept id="p2">**</ept>、<bpt id="p3">**</bpt>do-while<ept id="p3">**</ept>、または <bpt id="p4">**</bpt>for<ept id="p4">**</ept> ループ ステートメント内で <bpt id="p1">**</bpt>next<ept id="p1">**</ept> への呼び出しを行うことはできません</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="159">
          <source>A <bpt id="p1">**</bpt>next<ept id="p1">**</ept> statement can't be preceded by a <bpt id="p2">**</bpt>return<ept id="p2">**</ept> statement.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>次<ept id="p1">**</ept>ステートメントの前に、<bpt id="p2">**</bpt>戻る<ept id="p2">**</ept>ステートメントを置くことはできません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="160">
          <source>Because logical expressions are optimized, calls to <bpt id="p1">**</bpt>next<ept id="p1">**</ept> can't occur in logical expressions.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">論理式は最適化されているため、<bpt id="p1">**</bpt>次へ<ept id="p1">**</ept>の呼び出しは論理式では実行できません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="161">
          <source>At runtime, the execution of the complete expression isn't guaranteed.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">実行時に、完全な式の実行は保証されません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="162">
          <source>If a method is replaceable, extenders don't have to unconditionally call <bpt id="p1">**</bpt>next<ept id="p1">**</ept> when wrapping the method by using chain of command.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">メソッドが置き換え可能な場合は、拡張担当者はコマンド チェーンを使用してメソッドをラップするときに無条件に <bpt id="p1">**</bpt>next<ept id="p1">**</ept> を呼び出す必要はありません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="163">
          <source>Although extenders can break the chain, the expectation is that they will only conditionally break it.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">拡張担当者はチェーンを中断できますが、条件がある場合のみ中断することが期待されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="164">
          <source>The compiler doesn't enforce calls to <bpt id="p1">**</bpt>next<ept id="p1">**</ept> for methods with the attribute, <bpt id="p2">**</bpt>Replaceable<ept id="p2">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">コンパイラは、属性 <bpt id="p2">**</bpt>Replaceable<ept id="p2">**</ept> を持つメソッドの <bpt id="p1">**</bpt>next<ept id="p1">**</ept> の呼び出しを強制しません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="165">
          <source>Wrapping a base method in an extension of a derived class</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">派生クラスの拡張で基本メソッドをラッピング</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="166">
          <source>The following example shows how to wrap a base method in an extension of a derived class.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">次の例は、派生クラスの拡張機能で基準メソッドをラップする方法を示しています。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="167">
          <source>For this example, the following class hierarchy is used.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この例では、次のクラス階層が使用されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="168">
          <source>Therefore, there is one base class, <bpt id="p1">**</bpt>A<ept id="p1">**</ept>. Two classes, <bpt id="p2">**</bpt>B<ept id="p2">**</ept> and <bpt id="p3">**</bpt>C<ept id="p3">**</ept>, are derived from <bpt id="p4">**</bpt>A<ept id="p4">**</ept>. We will augment or create an extension class of one of the derived classes (in this case, <bpt id="p5">**</bpt>B<ept id="p5">**</ept>), as shown here.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">したがって、1 つの基本クラス <bpt id="p1">**</bpt>A<ept id="p1">**</ept> があり、2 つのクラス <bpt id="p2">**</bpt>B<ept id="p2">**</ept> および <bpt id="p3">**</bpt>C<ept id="p3">**</ept> が <bpt id="p4">**</bpt>A<ept id="p4">**</ept> から派生します。ここに示すように、派生クラスの 1 つ (この場合は <bpt id="p5">**</bpt>B<ept id="p5">**</ept>) の拡張クラスを追加または作成します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="169">
          <source>Although the <bpt id="p1">**</bpt>B_Extension<ept id="p1">**</ept> class is an extension of <bpt id="p2">**</bpt>B<ept id="p2">**</ept>, and <bpt id="p3">**</bpt>B<ept id="p3">**</ept> doesn't have a method definition for the <bpt id="p4">**</bpt>salute<ept id="p4">**</ept> method, you can wrap the <bpt id="p5">**</bpt>salute<ept id="p5">**</ept> method that is defined in the base class, <bpt id="p6">**</bpt>A<ept id="p6">**</ept>. Therefore, only instances of the <bpt id="p7">**</bpt>B<ept id="p7">**</ept> class will include the wrapping of the <bpt id="p8">**</bpt>salute<ept id="p8">**</ept> method.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>B_Extension<ept id="p1">**</ept> クラスは <bpt id="p2">**</bpt>B<ept id="p2">**</ept> の拡張子ではあり、<bpt id="p3">**</bpt>B<ept id="p3">**</ept> は <bpt id="p4">**</bpt>salute<ept id="p4">**</ept> メソッドのメソッドの定義がありませんが、<bpt id="p5">**</bpt>salute<ept id="p5">**</ept> メソッドを基本クラス <bpt id="p6">**</bpt>A<ept id="p6">**</ept> で定義しラップすることができます。したがって、<bpt id="p7">**</bpt>B<ept id="p7">**</ept> クラスのインスタンスのみが <bpt id="p8">**</bpt>salute<ept id="p8">**</ept> メソッドのラッピングを含みます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="170">
          <source>Instances of the <bpt id="p1">**</bpt>A<ept id="p1">**</ept> and <bpt id="p2">**</bpt>C<ept id="p2">**</ept> classes will never call the wrapper method that is defined in the extension of the <bpt id="p3">**</bpt>B<ept id="p3">**</ept> class.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>A<ept id="p1">**</ept> クラスおよび <bpt id="p2">**</bpt>C<ept id="p2">**</ept> クラスのインスタンスは、<bpt id="p3">**</bpt>B<ept id="p3">**</ept> クラスの拡張機能に定義されているラッパー メソッドを呼び出すことはありません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="171">
          <source>This behavior becomes clearer if we implement a method that uses these three classes.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">これらの 3 つのクラスを使用するメソッドを実装すると、この動作はより明確になります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="172">
          <source>For calls to <bpt id="p1">**</bpt>a.salute(“Hi”)<ept id="p1">**</ept> and <bpt id="p2">**</bpt>c.salute(“Hi”)<ept id="p2">**</ept>, the Infolog shows only the message “Hi.”</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>a.salute(「Hi」)<ept id="p1">**</ept> および <bpt id="p2">**</bpt>c.salute(「Hi」)<ept id="p2">**</ept> の呼び出しでは、情報ログに「Hi」のメッセージのみが表示されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="173">
          <source>However, when <bpt id="p1">**</bpt>b.salute(“Hi”)<ept id="p1">**</ept> is called, the Infolog shows “Hi” followed by “B extension.”</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ただし、<bpt id="p1">**</bpt>b.salute(「Hi」)<ept id="p1">**</ept> が呼び出されると、情報ログは「Hi」に続いて 「B 拡張子」を表示します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="174">
          <source>By using this mechanism, you can wrap the original method only for specific derived classes.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このメカニズムを使用することによって、特定の派生クラスに対してのみ元の方法をラップすることができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="175">
          <source>Accessing protected members from extension classes</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">拡張クラスから保護されたメンバーへのアクセス</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="176">
          <source>As of Platform update 9, you can access protected members from extension classes.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">プラットフォーム更新プログラム 9 では、拡張クラスから保護されたメンバーにアクセスできます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="177">
          <source>These protected members include fields and methods.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">これらの保護されたメンバーには、フィールドとメソッドが含まれます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="178">
          <source>Note that this support isn't specific to wrapping methods but applies all the methods in the class extension.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このサポートは、メソッドのラップに固有ではありませんが、クラス拡張内のすべてのメソッドを適用することに注意してください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="179">
          <source>Therefore, class extensions are more powerful than they were before.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">したがって、クラス拡張は以前よりも強力です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="180">
          <source>The Hookable attribute</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Hookable 属性</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="181">
          <source>If a method is explicitly marked as <bpt id="p1">**</bpt>[Hookable(false)]<ept id="p1">**</ept>, the method can't be wrapped in an extension class.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">メソッドが <bpt id="p1">**</bpt>[Hookable(false)]<ept id="p1">**</ept> として明示的にマークされている場合、メソッドを拡張子クラスで囲むことはできません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="182">
          <source>In the following example, <bpt id="p1">**</bpt>anyMethod<ept id="p1">**</ept> can't be wrapped in a class that augments <bpt id="p2">**</bpt>AnyClass1<ept id="p2">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">次の例では、<bpt id="p1">**</bpt>anyMethod<ept id="p1">**</ept> は <bpt id="p2">**</bpt>AnyClass1<ept id="p2">**</ept> を補強するクラスでラップできません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="183">
          <source>Final methods and the Wrappable attribute</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">最終的な方法および Wrappable 属性</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="184">
          <source>Public and protected methods that are marked as <bpt id="p1">**</bpt>final<ept id="p1">**</ept> can't be wrapped in extension classes.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>final<ept id="p1">**</ept> とマークされているパブリック メソッドと保護されたメソッドは、拡張クラスでラップできません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="185">
          <source>You can override this restriction by using the <bpt id="p1">**</bpt>Wrappable<ept id="p1">**</ept> attribute and setting the attribute parameter to <bpt id="p2">**</bpt>true<ept id="p2">**</ept> (<bpt id="p3">**</bpt>[Wrappable(true)]<ept id="p3">**</ept>).</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>Wrappable<ept id="p1">**</ept> 属性を使用して属性パラメーターを <bpt id="p2">**</bpt>true<ept id="p2">**</ept> (<bpt id="p3">**</bpt>[Wrappable(true)]<ept id="p3">**</ept>) に設定することにより、この制限をオーバーライドすることができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="186">
          <source>Similarly, to override the default capability for (non-final) public or protected methods, you can mark those methods as non-wrappable (<bpt id="p1">**</bpt>[Wrappable(false)]<ept id="p1">**</ept>).</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">同様に、(最終ではない) パブリックまたは保護されたメソッドの既定の機能を無効にするには、折り返し不可としてこれらのメソッドをマークすることができます (<bpt id="p1">**</bpt>[Wrappable(false)]<ept id="p1">**</ept>)。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="187">
          <source>In the following example, the <bpt id="p1">**</bpt>doSomething<ept id="p1">**</ept> method is explicitly marked as non-wrappable, even though it's a public method.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">次の例では、<bpt id="p1">**</bpt>doSomething<ept id="p1">**</ept> メソッドは、パブリック メソッドである場合でもラップできないものとして明示的にマークされます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="188">
          <source>The <bpt id="p1">**</bpt>doSomethingElse<ept id="p1">**</ept> method is explicitly marked as wrappable, even though it's a final method.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>doSomethingElse<ept id="p1">**</ept> メソッドは、最後のメソッドであっても、折り返し可能と明示的にマークされます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="189">
          <source>Extensions of form-nested concepts such as data sources, data fields, and controls</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">データ ソース、データ フィールド、および制御といったフォームで入れ子になった概念の拡張</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="190">
          <source>In order to implement CoC methods for form-nested concepts, such as data sources, data fields, and controls, an extension class is required for each nested concept.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">データ ソース、データ フィールド、コントロールなど、フォームで入れ子になった概念の CoC メソッドを実装するため、入れ子になった各概念には拡張クラスが必要です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="191">
          <source>Form data sources</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">フォーム データ ソース</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="192">
          <source>In this example, <bpt id="p1">**</bpt>FormToExtend<ept id="p1">**</ept> is the form, <bpt id="p2">**</bpt>DataSource1<ept id="p2">**</ept> is a valid existing data source in the form, and <bpt id="p3">**</bpt>init<ept id="p3">**</ept> and <bpt id="p4">**</bpt>validateWrite<ept id="p4">**</ept> are methods that can be wrapped in the data source.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この例では、<bpt id="p1">**</bpt>FormToExtend<ept id="p1">**</ept> はフォーム、<bpt id="p2">**</bpt>DataSource1<ept id="p2">**</ept> はフォームで有効な既存のデータ ソース、<bpt id="p3">**</bpt>init<ept id="p3">**</ept> と <bpt id="p4">**</bpt>validateWrite<ept id="p4">**</ept> はデータ ソースで折り返し可能なメソッドです。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="193">
          <source>Form data fields</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">フォーム データ フィールド</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="194">
          <source>In this example, a data field is extended.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この例では、データ フィールドが拡張されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="195">
          <source><bpt id="p1">**</bpt>FormToExtend<ept id="p1">**</ept> is the form, <bpt id="p2">**</bpt>DataSource1<ept id="p2">**</ept> is a data source in the form, <bpt id="p3">**</bpt>Field1<ept id="p3">**</ept> is a field in the data source, and <bpt id="p4">**</bpt>validate<ept id="p4">**</ept> is one of many methods that can be wrapped in this nested concept.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>FormToExtend<ept id="p1">**</ept> はフォーム、<bpt id="p2">**</bpt>DataSource1<ept id="p2">**</ept> はフォームのデータ ソース、<bpt id="p3">**</bpt>Field1<ept id="p3">**</ept> はデータ ソースのフィールド、<bpt id="p4">**</bpt>validate<ept id="p4">**</ept> はこの入れ子になった概念で折り返し可能な多くのメソッドのいずれかです。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="196">
          <source>Controls</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">コントロール</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="197">
          <source>In this example, <bpt id="p1">**</bpt>FormToExtend<ept id="p1">**</ept> is the form, <bpt id="p2">**</bpt>Button1<ept id="p2">**</ept> is the button control in the form, and <bpt id="p3">**</bpt>clicked<ept id="p3">**</ept> is a method that can be wrapped on the button control.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この例では、<bpt id="p1">**</bpt>FormToExtend<ept id="p1">**</ept> はフォーム、<bpt id="p2">**</bpt>Button1<ept id="p2">**</ept> はフォーム内のボタン コントロール、<bpt id="p3">**</bpt>clicked<ept id="p3">**</ept> はボタン コントロールで折り返し可能なメソッドです。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="198">
          <source>Requirements and considerations when you write CoC methods on extensions for form-nested concepts</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">フォームで入れ子になった概念で CoC メソッドを書き込むときの要件と考慮事項</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="199">
          <source>Like other CoC methods, these methods must always call <bpt id="p1">**</bpt>next<ept id="p1">**</ept> to invoke the next method in the chain, so that the chain can go all the way to the kernel or native implementation in the runtime behavior.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">その他の CoC メソッドと同様、これらのメソッドは常に <bpt id="p1">**</bpt>next<ept id="p1">**</ept> を呼び出してチェーン内の次のメソッドを呼び出す必要があります。これにより、チェーンは実行時の動作でカーネルまたはネイティブ実装まで進むことができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="200">
          <source>The call to next is equivalent to a call to <bpt id="p1">**</bpt>super()<ept id="p1">**</ept> from the form itself to help guarantee that the base behavior in the runtime is always run as expected.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">next の呼び出しは、ランタイムにおける基本の動作が常に正常に実行されることを保証する、フォーム自体からの <bpt id="p1">**</bpt>super()<ept id="p1">**</ept> の呼び出しに相当します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="201">
          <source>Currently, the X++ editor in Microsoft Visual Studio doesn't support discovery of methods that can be wrapped.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">現時点では、Microsoft Visual Studio の X++ エディターは、折り返し可能なメソッドの検出をサポートしていません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="202">
          <source>Therefore, you must refer to the system documentation for each nested concept to identify the correct method to wrap and its exact signature.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">したがって、折り返し対象となるメソッドとその正確なシグネチャを識別するための入れ子になった各概念については、システムのドキュメントを参照する必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="203">
          <source>You <bpt id="p1">**</bpt>cannot<ept id="p1">**</ept> add CoC to wrap methods that aren't defined in the original base behavior of the nested control type.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">入れ子になったコントロール タイプの元の基本動作で定義されていないメソッドをラップする CoC を追加することは<bpt id="p1">**</bpt>できません<ept id="p1">**</ept>。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="204">
          <source>For example, you can't add <bpt id="p1">**</bpt>methodInButton1<ept id="p1">**</ept> CoC on an extension.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">たとえば、拡張において <bpt id="p1">**</bpt>methodInButton1<ept id="p1">**</ept> CoC を追加することはできません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="205">
          <source>However, from the control extension, you can make a call into this method if the method has been defined as public or protected.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ただし、制御の拡張からは、メソッドがパブリックまたは保護として定義されている場合にこのメソッドへの呼び出しを行うことができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="206">
          <source>Here is an example where the <bpt id="p1">**</bpt>Button1<ept id="p1">**</ept> control is defined in the <bpt id="p2">**</bpt>FormToExtend<ept id="p2">**</ept> form in such a way that it has the <bpt id="p3">**</bpt>methodInButton1<ept id="p3">**</ept> method.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">以下に、<bpt id="p3">**</bpt>methodInButton1<ept id="p3">**</ept> メソッドと同じように <bpt id="p1">**</bpt>Button1<ept id="p1">**</ept> コントロールが <bpt id="p2">**</bpt>FormToExtend<ept id="p2">**</ept> フォームで定義される例を示します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="207">
          <source>You do <bpt id="p1">**</bpt>not<ept id="p1">**</ept> have to recompile the module where the original form is defined to support CoC methods on nested concepts on that form from an extension.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">拡張からのそのフォームで入れ子になった概念における CoC メソッドをサポートするために元のフォームが定義されたモジュールを再コンパイルする必要は<bpt id="p1">**</bpt>ありません<ept id="p1">**</ept>。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="208">
          <source>For example, if the <bpt id="p1">**</bpt>FormToExtend<ept id="p1">**</ept> form from the previous examples is in the <bpt id="p2">**</bpt>ApplicationSuite<ept id="p2">**</ept> module, you don't have to recompile <bpt id="p3">**</bpt>ApplicationSuite<ept id="p3">**</ept> to extend it with CoC for nested concepts on that form from a different module.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">たとえば、前の例の <bpt id="p1">**</bpt>FormToExtend<ept id="p1">**</ept> フォームが <bpt id="p2">**</bpt>ApplicationSuite<ept id="p2">**</ept> モジュールにある場合、異なるモジュールからそのフォームで入れ子になった概念の CoC で拡張するために <bpt id="p3">**</bpt>ApplicationSuite<ept id="p3">**</ept> を再コンパイルする必要はありません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="209">
          <source>Extensions of tables and data entities</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">テーブルとデータ エンティティの拡張機能</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="210">
          <source>An extension class is required for each concept.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">拡張機能クラスは、概念ごとに必要です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="211">
          <source>Tables</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">テーブル</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="212">
          <source>In this example, <bpt id="p1">**</bpt>TableToExtend<ept id="p1">**</ept> is the table and <bpt id="p2">**</bpt>delete<ept id="p2">**</ept>, <bpt id="p3">**</bpt>canSubmitToWorkflow<ept id="p3">**</ept>, and <bpt id="p4">**</bpt>caption<ept id="p4">**</ept> are methods that can be wrapped in the table.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この例では、<bpt id="p1">**</bpt>TableToExtend<ept id="p1">**</ept> はテーブルであり、<bpt id="p2">**</bpt>delete<ept id="p2">**</ept>、<bpt id="p3">**</bpt>canSubmitToWorkflow<ept id="p3">**</ept>、<bpt id="p4">**</bpt>caption<ept id="p4">**</ept> はテーブルでラップできるメソッドです。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="213">
          <source>Data entities</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">データ エンティティ</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="214">
          <source>In this example, <bpt id="p1">**</bpt>DataEntityToExtend<ept id="p1">**</ept> is the data entity and <bpt id="p2">**</bpt>validateDelete<ept id="p2">**</ept> and <bpt id="p3">**</bpt>validateWrite<ept id="p3">**</ept> are methods that can be wrapped in the data entity.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この例では、<bpt id="p1">**</bpt>DataEntityToExtend<ept id="p1">**</ept> はデータ エンティティで、<bpt id="p2">**</bpt>validateDelete<ept id="p2">**</ept> および <bpt id="p3">**</bpt>validateWrite<ept id="p3">**</ept> はデータ エンティティでラップできるメソッドです。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="215">
          <source>Restrictions on wrapper methods</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ラッパー メソッドに関する制限事項</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="216">
          <source>The following sections describe restrictions on the use of CoC and method wrapping.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">次のセクションでは、CoC およびメソッド ラッピングの使用上の制限について説明します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="217">
          <source>X++ classes that are compiled by using Platform update 8 or earlier</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">プラットフォーム更新プログラム 8 またはそれ以前を使用してコンパイルされた X++ クラス</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="218">
          <source>The method wrapping feature requires specific functionality that is emitted by an X++ compiler that is part of Platform update 9 or later.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">メソッドのラッピング機能には、プラットフォーム update 9 以降の一部である X++ コンパイラによって出力される特定の機能が必要です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="219">
          <source>Methods that are compiled by using earlier versions don't have the infrastructure to support this feature.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">以前のバージョンを使用してコンパイルされたメソッドには、この機能をサポートするインフラストラクチャはありません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="220">
          <source>Methods on types nested within forms can be wrapped in Platform update 16 and later</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">プラットフォーム更新 16 以降ではフォーム内で入れ子になったタイプのメソッドをラップできます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="221">
          <source>The ability to wrap methods on types nested within forms (data sources and controls) by using class extensions was added in Platform update 16.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">クラス拡張を使用してフォーム (データ ソースとコントロール) 内で入れ子になった型のメソッドをラップする機能がプラットフォーム更新 16 で追加されました。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="222">
          <source>This means that Chain of Command can be used to provide overrides for data source methods and form control methods.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">つまり、コマンド チェーンを使用して、データ ソース メソッドおよびフォーム制御メソッドのオーバーライドを提供できます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="223">
          <source>However, wrapping (extension) of purely X++ methods on those nested types (form controls and form data sources) is not yet supported like it is on other types (forms, tables, data entities).</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ただし、これらの入れ子にされた型 (フォーム コントロールとフォーム データ ソース) の純粋な X++ メソッドのラップ (拡張) は、他の型 (フォーム、テーブル、データ エンティティ) と同様にまだサポートされていません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="224">
          <source>Currently, if a developer uses Chain of Command on purely X++ methods on types inside forms, then it compiles, but the extension methods are not invoked at runtime.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">現時点では、開発者は、フォーム内の型の純粋な X++ メソッドでコマンド チェーンを使用する場合、コンパイルしますが、実行時に拡張メソッドじゃ呼び出されません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="225">
          <source>This capability is planned for a future update.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この機能は、将来の更新で計画されています。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="226">
          <source>Unimplemented system methods on tables and data entities can be wrapped in Platform update 22 and later</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">テーブルとデータ エンティティの実装されていないシステム メソッドは、プラットフォーム更新 22 以降でラップできます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="227">
          <source>The ability to wrap methods in nested classes by using class extensions was added in Platform update 16.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">クラス拡張を使用して入れ子になったクラスでメソッドをラップする機能がプラットフォーム更新 16 で追加されました。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="228">
          <source>The concept of nested classes in X++ applies to forms for overriding data source methods and form control methods.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">X++ の入れ子になったクラスの概念は、データソース メソッドやフォームコ ントロール メソッドを上書きするためのフォームに適用されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="229">
          <source>Next calls can be put inside try/catch/finally in Platform update 21 and later</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">プラットフォーム更新 21 以降では、次の呼び出しを try/catch/finally 内に配置できます</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="230">
          <source>In a CoC extension method, the next call must not be called conditionally.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">CoC 拡張メソッドでは、次の呼び出しを条件付きで呼び出してはなりません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="231">
          <source>However, in Platform update 21 and later next calls can be placed inside a try/catch/finally to allow for standard handling of exceptions and resource cleanup.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ただし、プラットフォーム更新 21 以降では、例外およびリソースのクリーンアップの標準的な処理を許可するため、次の呼び出しを try/catch/finally 内に配置できます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="232">
          <source>Extensions of extensions are not yet supported</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">拡張機能の拡張機能はまだサポートされていません</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="233">
          <source>Currently, only methods that are defined in regular classes can be wrapped.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">現在のところ、通常のクラスで定義されているメソッドのみラップできます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="234">
          <source>Methods that are defined in extension classes can't be wrapped by augmenting the extension classes.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">拡張クラスで定義されているメソッドは、拡張クラスを強化してラップできません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="235">
          <source>This capability is planned for a future release.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この機能は、将来のリリースで計画されています。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="236">
          <source>Tooling</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ツール</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="237">
          <source>For the features that are described in this topic, the Microsoft Visual Studio X++ editor doesn't yet offer complete support for cross-references and Microsoft IntelliSense.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このトピックに記載されている機能については、Microsoft Visual Studio X++ エディターは、相互参照および Microsoft IntelliSense の完全なサポートまだ提供していません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="238">
          <source>We plan to make complete support available in Dynamics 365 for Finance and Operations Platform update 10.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Dynamics 365 for Finance and Operations プラットフォーム更新プログラム 10 で完全なサポートが利用できるようにする予定です。</target></trans-unit>
      </group>
    </body>
  </file>
</xliff>