<?xml version="1.0" encoding="UTF-8"?>
<xliff xmlns:logoport="urn:logoport:xliffeditor:xliff-extras:1.0" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns="urn:oasis:names:tc:xliff:document:1.2" xmlns:xliffext="urn:microsoft:content:schema:xliffextensions" version="1.2" xsi:schemaLocation="urn:oasis:names:tc:xliff:document:1.2 xliff-core-1.2-transitional.xsd">
  <file datatype="xml" source-language="en-US" original="control-extensibility.md" target-language="ja-JP">
    <header>
      <tool tool-company="Microsoft" tool-version="1.0-7889195" tool-name="mdxliff" tool-id="mdxliff"/>
      <xliffext:skl_file_name>control-extensibility.d3a731.fd09487a027014423b4a0b1795deab81ca6414fd.skl</xliffext:skl_file_name>
      <xliffext:version>1.2</xliffext:version>
      <xliffext:ms.openlocfilehash>fd09487a027014423b4a0b1795deab81ca6414fd</xliffext:ms.openlocfilehash>
      <xliffext:ms.sourcegitcommit>9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b</xliffext:ms.sourcegitcommit>
      <xliffext:ms.lasthandoff>05/15/2019</xliffext:ms.lasthandoff>
      <xliffext:ms.openlocfilepath>articles\dev-itpro\user-interface\control-extensibility.md</xliffext:ms.openlocfilepath>
    </header>
    <body>
      <group extype="content" id="content">
        <trans-unit xml:space="preserve" translate="yes" id="101" restype="x-metadata">
          <source>Control extensibility</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">コントロールの拡張機能</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="102" restype="x-metadata">
          <source>This article describes the architecture that lets developers extend the user interface and also define new user interface patterns.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この記事では、開発者がユーザー インターフェイスを拡張し、新しいユーザー インターフェイス パターンを定義できるようにするアーキテクチャについて説明します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="103">
          <source>Control extensibility</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">コントロールの拡張機能</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="104">
          <source>This article describes the architecture that lets developers extend the user interface and also define new user interface patterns.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この記事では、開発者がユーザー インターフェイスを拡張し、新しいユーザー インターフェイス パターンを定義できるようにするアーキテクチャについて説明します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="105">
          <source>You can extend the existing application user interface (UI) and can also define entirely new UI patterns to create compelling new user experiences.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">既存のアプリケーション ユーザー インターフェイス (UI) を拡張、および完全に新しい UI パターンを定義して魅力的な新しいユーザー エクスペリエンスを作成することができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="106">
          <source>By using modern tools such as HTML5, CSS3, and jQuery, developers can define customized visualizations of business data and drastically enhance the program's interaction patterns.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">HTML5、CSS3、jQuery などの最新ツールを使用することにより、開発者は業務データのカスタマイズされた視覚エフェクトを定義し、プログラムの相互作用パターンを大幅に強化することができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="107">
          <source>Serverside architecture</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">サーバー側アーキテクチャ</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="108">
          <source>The Control Extensibility Framework takes advantage of the existing and familiar X++ language for developing server-side data access and business logic.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">コントロール拡張フレームワークは、サーバー側データ アクセスおよびビジネス ロジックを開発するために既存の使い慣れた X++ 言語を活用します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="109">
          <source>There are no artificial restrictions on the code that developers write to build extensible controls.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">開発者が拡張可能なコントロールを作成するために書くコードに人為的な制限はありません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="110">
          <source>Instead, developers can declaratively define the modeling experience and the run-time behavior through a set of X++ class and method attributes.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">代わりに、開発者は一連の X++ クラスおよびメソッドの属性を通じてモデリング経験およびランタイムの動作を宣言的に定義できます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="111">
          <source>A developer defines one class for the design-time behavior (the X++ Build Class) and one class for the run-time behavior (the X++ RunTime class).</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">開発者は、1 つのクラスをデザイン時の動作 (X++ Build クラス) に、1 つのクラスを実行時の動作 (X++ RunTime クラス) に定義します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="112">
          <source>In the X++ Build Class, attributes enable the definition of design-time behaviors such as custom properties in the property sheet, the addition of child controls, and extra modeling components.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">X++ ビルド クラスでは、属性によってプロパティ シートでのカスタム プロパティ、子コントロールの追加、追加のモデリング コンポーネントなどのデザイン時の動作を定義できます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="113">
          <source>In the X++ Runtime Class, attributes are used to define the run-time properties and commands that the extensible control will access from the client.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">X++ ランタイム クラスでは、拡張可能コントロールがクライアントからアクセスする実行時のプロパティとコマンドを定義するために属性が使用されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="114">
          <source>The X++ Runtime Class consumes the X++ Build Class to initialize the run-time properties, based on the values and data bindings that are specified in the property sheet.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">X++ ランタイム クラスは、プロパティ シートで指定されている値とデータ バインディングに基づき、X++ 構築クラスを使用して、実行時のプロパティを初期化します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="115">
          <source>Clientside architecture</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">クライアント側のアーキテクチャ</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="116">
          <source>The client-side behavior for the control is defined by using HTML and JavaScript.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">コントロールのクライアント側の動作は、HTML と JavaScript を使用して定義されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="117">
          <source>In the context of a Model-View-ViewModel architecture, the HTML for the control comprises the View, and the JavaScript comprises the ViewModel.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">モデル-ビュー-ViewModel アーキテクチャにおいては、コントロールの HTML が View を構成し、JavaScript が ViewModel を構成します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="118">
          <source>The Control Extensibility Framework provides an HTML-based binding syntax that enables elements in the HTML View to be bound to data fields and properties in the JavaScript ViewModel.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">コントロール拡張フレームワークは、HTML ビューの要素を JavaScript ViewModel でデータ フィールドおよびプロパティにバインドできるようにする HTML 形式のバインディング構文を提供します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="119">
          <source>In addition, the framework enables visualization behavior to be defined based on conditional expressions or logical evaluations that can react to changes in ViewModel properties or business data.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">さらに、フレームワークによって、ViewModel プロパティや業務データの変更に対処できる条件式や論理評価を基に定義する視覚化動作が可能です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="120">
          <source>The JavaScript ViewModel is automatically generated at run time, based on the properties and commands that are defined in the X++ runtime for the control.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">JavaScript ViewModel は、コントロールの X++ ランタイムで定義されているプロパティとコマンドに基づいて、実行時に自動的に生成されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="121">
          <source>This automatically generated ViewModel lets a developer define an HTML View that consumes the properties and commands that are defined in X++.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この自動的に生成された ViewModel を使用すると、開発者は X++ で定義されているプロパティとコマンドを使用する HTMLビューを定義できます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="122">
          <source>If a developer wants additional client-side properties and commands, or wants to implement visualization behavior that can't be declaratively defined in the HTML View, he or she can extend the automatically generated ViewModel.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">開発者が追加のクライアント側のプロパティとコマンドを必要とする場合や、HTML ビューで宣言的に定義できない視覚化動作を実装する場合は、自動的に生成された ViewModel を拡張することができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="123">
          <source>The developer can take advantage of the JavaScript framework in conjunction with the powerful jQuery library.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">開発者は、強力な jQuery ライブラリと組み合わせて JavaScript フレームワークを利用することができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="124">
          <source>Control extensibility architecture overview</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">コントロールの拡張機能アーキテクチャの概要</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="125">
          <source>The following diagram shows the artifacts that are involved and their relation to each other.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">次の図は、関係するコンポーネントとそれらの相互関係を示しています。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="126">
          <source><bpt id="p1">[</bpt><ph id="ph1">![</ph>Control extensibility architecture<ept id="p1">](./media/extensibilitycontrolarchitecture.png)](./media/extensibilitycontrolarchitecture.png)</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">[</bpt><ph id="ph1">![</ph>拡張性アーキテクチャのコントロール<ept id="p1">](./media/extensibilitycontrolarchitecture.png)](./media/extensibilitycontrolarchitecture.png)</ept></target></trans-unit>
      </group>
    </body>
  </file>
</xliff>