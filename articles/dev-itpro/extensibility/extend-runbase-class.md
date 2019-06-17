<?xml version="1.0" encoding="UTF-8"?>
<xliff xmlns:logoport="urn:logoport:xliffeditor:xliff-extras:1.0" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns="urn:oasis:names:tc:xliff:document:1.2" xmlns:xliffext="urn:microsoft:content:schema:xliffextensions" version="1.2" xsi:schemaLocation="urn:oasis:names:tc:xliff:document:1.2 xliff-core-1.2-transitional.xsd">
  <file datatype="xml" source-language="en-US" original="extend-runbase-class.md" target-language="ja-JP">
    <header>
      <tool tool-company="Microsoft" tool-version="1.0-7889195" tool-name="mdxliff" tool-id="mdxliff"/>
      <xliffext:skl_file_name>extend-runbase-class.95eae3.df556ae837fcd84790fc664f2cddf373a1220bf0.skl</xliffext:skl_file_name>
      <xliffext:version>1.2</xliffext:version>
      <xliffext:ms.openlocfilehash>df556ae837fcd84790fc664f2cddf373a1220bf0</xliffext:ms.openlocfilehash>
      <xliffext:ms.sourcegitcommit>9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b</xliffext:ms.sourcegitcommit>
      <xliffext:ms.lasthandoff>05/15/2019</xliffext:ms.lasthandoff>
      <xliffext:ms.openlocfilepath>articles\dev-itpro\extensibility\extend-runbase-class.md</xliffext:ms.openlocfilepath>
    </header>
    <body>
      <group extype="content" id="content">
        <trans-unit xml:space="preserve" translate="yes" id="101" restype="x-metadata">
          <source>Extend the RunBase class</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">RunBase クラスの拡張</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="102" restype="x-metadata">
          <source>This topic contains an example that shows how a RunBase class can be augmented end to end.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このトピックには、RunBase クラスを拡張できる方法を示した例が徹底的に含まれています。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="103">
          <source>Extend the RunBase class</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">RunBase クラスの拡張</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="104">
          <source>When you extend functionality of the application suite, you will encounter classes that extend the <bpt id="p1">**</bpt>RunBase<ept id="p1">**</ept> class.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">アプリケーション スイートの機能を拡張するとき、<bpt id="p1">**</bpt>RunBase<ept id="p1">**</ept> クラスを拡張するクラスに遭遇します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="105">
          <source>This topic shows how a <bpt id="p1">**</bpt>RunBase<ept id="p1">**</ept> class can be augmented end to end.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このトピックでは、<bpt id="p1">**</bpt>RunBase<ept id="p1">**</ept> クラスをエンド・ツー・エンドで拡張する方法を示します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="106">
          <source>For example, you want to extend the SysUserLogCleanup class.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">たとえば、SysUserLogCleanup クラスを拡張します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="107">
          <source>Out of the box, this class can delete records from the SysUserLog table.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">すぐに使えるこのクラスは、SysUserLog テーブルからレコードを削除できます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="108">
          <source>However, you want to archive these records to a different table before they are deleted.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ただし、削除する前に、これらのレコードを別のテーブルにアーカイブします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="109">
          <source>The SysUserLogCleanup class is a <bpt id="p1">**</bpt>RunBase<ept id="p1">**</ept> class.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">SysUserLogCleanup クラスは、<bpt id="p1">**</bpt>RunBase<ept id="p1">**</ept> クラスです。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="110">
          <source>The <bpt id="p1">**</bpt>RunBase<ept id="p1">**</ept> class has a dialog box, where the user is prompted for parameters before the class is run.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>RunBase<ept id="p1">**</ept> クラスには、クラスを実行する前にユーザーにパラメーターを求めるダイアログ ボックスがあります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="111">
          <source>For this example, we will add a toggle button control to the dialog box, get the value of the control, act on the value in the run method, and make sure that the value is serialized via the pack and unpack methods.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この例では、ダイアログ ボックスに切り替えボタン コントロールを追加し、コントロールの値を取得して実行メソッドの値を処理し、さらに値が pack および unpack メソッドを介してシリアル化されるどうかを確認します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="112">
          <source>Serialization helps guarantee that the user’s last selection is presented again if the dialog box is reopened.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">シリアル化により、ダイアログ ボックスを再び開いた場合にユーザーの最後の選択が再表示されることが保証されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="113">
          <source>It also helps guarantee that the settings are applied if the class is run in the background.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">また、クラスがバックグラウンドで実行される場合に、設定が適用されていることを保証することもできます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="114">
          <source>To avoid collisions with other eventual extensions, we followed these best practices:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">他の最終的な拡張機能との衝突を避けるために、次のベストプラクティスに従っています。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="115">
          <source><bpt id="p1">**</bpt>Prefix members and methods<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>接頭語メンバーおよびメソッド<ept id="p1">**</ept>。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="116">
          <source>In the example, the prefix “my” is used.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">例では、接頭語「my」が使用されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="117">
          <source>This practice is important, because it helps prevent name clashes with other extensions and future versions of the augmented class.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このプラクティスは、他の拡張機能と拡張されたクラスの将来のバージョンとの名前の衝突を防ぐために重要です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="118">
          <source><bpt id="p1">**</bpt>Use RunBase.packExtension() and RunBase.unpackExtension()<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>RunBase.packExtension() および RunBase.unpackExtension() の使用<ept id="p1">**</ept>。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="119">
          <source>These methods provide serialization in a nonintrusive manner.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">これらのメソッドは、非直列的な方法でシリアル化を提供します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="120">
          <source>They enable serialization of multiple extensions of the same class.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">それらは同じクラスの複数の拡張のシリアル化を可能にします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="121">
          <source>The methods are available starting in Platform Update 5.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">これらのメソッドは、プラットフォーム Update 5 以降で使用できます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="122">
          <source>The following example shows how to implement this scenario.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">次の例は、このシナリオを実装する方法を示しています。</target></trans-unit>
      </group>
    </body>
  </file>
</xliff>