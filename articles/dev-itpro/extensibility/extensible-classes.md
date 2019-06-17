<?xml version="1.0" encoding="UTF-8"?>
<xliff xmlns:logoport="urn:logoport:xliffeditor:xliff-extras:1.0" xmlns:tilt="urn:logoport:xliffeditor:tilt-non-translatables:1.0" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns="urn:oasis:names:tc:xliff:document:1.2" xmlns:xliffext="urn:microsoft:content:schema:xliffextensions" version="1.2" xsi:schemaLocation="urn:oasis:names:tc:xliff:document:1.2 xliff-core-1.2-transitional.xsd">
  <file datatype="xml" source-language="en-US" original="extensible-classes.md" target-language="ja-JP">
    <header>
      <tool tool-company="Microsoft" tool-version="1.0-7889195" tool-name="mdxliff" tool-id="mdxliff"/>
      <xliffext:skl_file_name>extensible-classes.284c3a.312e6af1f510b96269b1d19f61e08530946ea8e6.skl</xliffext:skl_file_name>
      <xliffext:version>1.2</xliffext:version>
      <xliffext:ms.openlocfilehash>312e6af1f510b96269b1d19f61e08530946ea8e6</xliffext:ms.openlocfilehash>
      <xliffext:ms.sourcegitcommit>9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b</xliffext:ms.sourcegitcommit>
      <xliffext:ms.lasthandoff>05/15/2019</xliffext:ms.lasthandoff>
      <xliffext:ms.openlocfilepath>articles\dev-itpro\extensibility\extensible-classes.md</xliffext:ms.openlocfilepath>
    </header>
    <body>
      <group extype="content" id="content">
        <trans-unit xml:space="preserve" translate="yes" id="101" restype="x-metadata">
          <source>Write extensible classes</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">拡張可能クラスの書き込み</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="102" restype="x-metadata">
          <source>This topic provides information about how to write extensible classes.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このトピックでは、拡張可能クラスを書き込む方法について説明します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="103">
          <source>Write extensible classes</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">拡張可能クラスの書き込み</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="104">
          <source>A class and its methods should have a single responsibility.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">クラスとそのメソッドには、単一の責任が必要です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="105">
          <source>Keep the following in mind in order to design classes that are resilient to changes in the long run.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">長期的な変更に耐えるクラスをデザインするために以下の点に留意してください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="106">
          <source>Class should have:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">クラスに必要なもの:</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="107">
          <source>A clear purpose</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">明確な目的</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="108">
          <source>Good names (class name and method names)</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">適切な名前 (クラス名およびメソッド名)</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="109">
          <source>Only methods that should be extended are exposed for extensibility, i.e. the key rule is allow extending as little as necessary.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">拡張する必要があるメソッドのみ拡張性のために公開されます。つまり、主要なルールは、できる限り拡張を最小限にすることです。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="110">
          <source>Every public and protected method is an extensibility point in X++.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">すべてのパブリックおよび保護メソッドが X++ における拡張性ポイントとなります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="111">
          <source>Every time that a new method is introduced, downstream consumers get a new way to inject additional logic into the method.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">新しいメソッドを導入するたびに、ダウンストリーム ユーザーはメソッドに追加のロジックを挿入する新しい方法を取得します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="112">
          <source>Example</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">例</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="113">
          <source><bpt id="p1">**</bpt>Non-extensible code<ept id="p1">**</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>拡張不可コード<ept id="p1">**</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="114">
          <source><bpt id="p1">**</bpt>Extensible code<ept id="p1">**</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>拡張可能コード<ept id="p1">**</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="115">
          <source>Class hierarchies</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">クラス階層</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="116">
          <source>For new or existing class hierarchies where a factory pattern can be used, the SysExtension framework enables easy extensions.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">出荷時のパターンを使用できる新規または既存のクラス階層の場合、SysExtension フレームワークにより簡単に拡張可能になります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="117">
          <source>Because these extensions are truly decoupled, new subclasses can be added without requiring any changes to the base class.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">これらの拡張は完全に切り離されるため、基本クラスに変更を加えなくても新しいサブクラスを追加することができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="118">
          <source>Therefore, less code is required.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">したがってより少ないコードが必要です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="119">
          <source>Additionally, because the contract of the construct remains the same, there is no change to the public application programming interface (API).</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">さらに、コストラクトのコントラクトが変わらないので、パブリック アプリケーション プログラミング インターフェイス (API) への変更はありません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="120">
          <source>Therefore, refactoring involves low risk.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">したがって、リファクタリングは低リスクです。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="121">
          <source>Some existing factory methods might not instantiate subclasses by using the instance constructor.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">いくつかの既存のファクトリ メソッドは、インスタンス コンストラクターを使用してサブクラスをインスタンス化しない可能性があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="122">
          <source>Instead, they might call a static constructor, such as <bpt id="p1">**</bpt>construct<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">代わりに、<bpt id="p1">**</bpt>コンストラクト<ept id="p1">**</ept>などの静的コンストラクターを呼び出すことができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="123">
          <source>If the SysExtension framework is used for these factory methods, a breaking change occurs, because the static constructors on the subclasses are no longer invoked.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">これらのファクトリ メソッドに SysExtension フレームワークが使用される場合、重大な変更が発生します。サブクラスの静的コンストラクターが呼び出されなくなるためです。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="124">
          <source>In these situations, use the SysExtension framework only for the default case.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このような場合は、既定のケースにのみ SysExtension フレームワークを使用します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="125">
          <source>For more information about class hierarchies, see the following blog posts:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">クラス階層構造の詳細については、次のブログ記事を参照してください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="126">
          <source><bpt id="p1">[</bpt>SysExtension Framework – to the rescue<ept id="p1">](https://blogs.msdn.microsoft.com/mfp/2013/06/12/sysextension-framework-to-the-rescue/)</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">[</bpt>SysExtension フレームワーク – 問題発生時<ept id="p1">](https://blogs.msdn.microsoft.com/mfp/2013/06/12/sysextension-framework-to-the-rescue/)</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="127">
          <source><bpt id="p1">[</bpt>Embrace the extensions mindset with Dynamics 365 for Finance and Operations #2 – SysExtension framework<ept id="p1">](https://blogs.msdn.microsoft.com/axinthefield/embrace-the-extensions-mindset-with-dynamics-365-for-finance-and-operations-2-sysextension-framework/)</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">[</bpt>Dynamics 365 for Finance and Operations への拡張機能のご要望の採用 #2 - SysExtension フレームワーク<ept id="p1">](https://blogs.msdn.microsoft.com/axinthefield/embrace-the-extensions-mindset-with-dynamics-365-for-finance-and-operations-2-sysextension-framework/)</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="128">
          <source>Deprecation</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">廃止</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="129">
          <source>If a class or a public or protected method is no longer required, always use a warning first to notify consumers that the method is obsolete.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">クラスまたはパブリックまたは保護メソッドが不要になった場合、必ずまず警告を使用し、メソッドが廃止されたことをユーザーに通知します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="130">
          <source>Then, when all consumers have had the chance to uptake the changes or the new API, the method can be deprecated.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">次に、すべてのユーザーは、変更または新しい API を取り込むことができ、メソッドを廃止できます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="131">
          <source>Deprecation of classes and methods (or removal of class members in other cases) is a breaking change.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">クラスおよびメソッドの廃止 (または、それ以外の場合はクラス メンバーの削除) は、大きな変更点です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="132">
          <source>For more information, see <bpt id="p1">[</bpt>Breaking changes<ept id="p1">](breaking-changes.md)</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">詳細については、<bpt id="p1">[</bpt>重大な変更<ept id="p1">](breaking-changes.md)</ept>を参照してください。</target></trans-unit>
      </group>
    </body>
  </file>
</xliff>