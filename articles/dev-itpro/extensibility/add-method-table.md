<?xml version="1.0" encoding="UTF-8"?>
<xliff xmlns:logoport="urn:logoport:xliffeditor:xliff-extras:1.0" xmlns:tilt="urn:logoport:xliffeditor:tilt-non-translatables:1.0" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns="urn:oasis:names:tc:xliff:document:1.2" xmlns:xliffext="urn:microsoft:content:schema:xliffextensions" version="1.2" xsi:schemaLocation="urn:oasis:names:tc:xliff:document:1.2 xliff-core-1.2-transitional.xsd">
  <file datatype="xml" source-language="en-US" original="add-method-table.md" target-language="ja-JP">
    <header>
      <tool tool-company="Microsoft" tool-version="1.0-7889195" tool-name="mdxliff" tool-id="mdxliff"/>
      <xliffext:skl_file_name>add-method-table.453edf.67f58f863104af56b6f96cd1bcc7a92db7013982.skl</xliffext:skl_file_name>
      <xliffext:version>1.2</xliffext:version>
      <xliffext:ms.openlocfilehash>67f58f863104af56b6f96cd1bcc7a92db7013982</xliffext:ms.openlocfilehash>
      <xliffext:ms.sourcegitcommit>9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b</xliffext:ms.sourcegitcommit>
      <xliffext:ms.lasthandoff>05/15/2019</xliffext:ms.lasthandoff>
      <xliffext:ms.openlocfilepath>articles\dev-itpro\extensibility\add-method-table.md</xliffext:ms.openlocfilepath>
    </header>
    <body>
      <group extype="content" id="content">
        <trans-unit xml:space="preserve" translate="yes" id="101" restype="x-metadata">
          <source>Add methods to tables through extension</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">拡張機能を使用してテーブルにメソッドを追加</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="102" restype="x-metadata">
          <source>This topic describes how to add a method to a table by using an extension.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このトピックでは、拡張機能を使用してテーブルにメソッドを追加する方法について説明します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="103">
          <source>Add methods to tables through extension</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">拡張機能を使用してテーブルにメソッドを追加</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="104">
          <source>When you extend the business logic that is related to a table, the general coding principles that help keep your code clean still apply.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">テーブルに関連付けられているビジネス ロジックを拡張するとき、コードをクリーンに維持するために役立つ一般的なコーディング原則はまだ適用されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="105">
          <source>Therefore, you must eventually encapsulate actions in separate methods on the table.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">したがって、最終的にアクションをテーブルの別々のメソッドにカプセル化する必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="106">
          <source>In Microsoft Dynamics AX 2012, you completed that task by adding the method directly on the table through overlayering.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Microsoft Dynamics AX 2012 では、オーバーレイ経由でテーブルに直接メソッドを追加することによってそのタスクを完了していました。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="107">
          <source>To complete the same task through extension, you use a different approach.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">拡張を使用して同じタスクを完了するには、別の方法を使用します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="108">
          <source>Specifically, you create an augmentation class.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">具体的には、拡張クラスを作成します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="109">
          <source>For example, a new field that is named <bpt id="p1">**</bpt>MyInventLocationId<ept id="p1">**</ept> was added to the InventTable table through extension.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">たとえば、<bpt id="p1">**</bpt>MyInventLocationId<ept id="p1">**</ept> という名前新しいフィールドが、拡張機能によって InventTable テーブルに追加されました。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="110">
          <source>A data event handler was also created for the <bpt id="p1">**</bpt>Inserting<ept id="p1">**</ept> event, and you must implement the logic of filling the new field there.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>挿入<ept id="p1">**</ept>イベント用のデータ イベント ハンドラーも作成されました。新しいフィールドに入力するロジックを実装する必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="111">
          <source>To encapsulate that action, you will create a new method on InventTable and name that method <bpt id="p1">**</bpt>myDefaultInventLocationId<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">そのアクションをカプセル化するには、InventTable で新しいメソッドを作成し、そのメソッドに <bpt id="p1">**</bpt>myDefaultInventLocationId<ept id="p1">**</ept> という名前を付けます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="112">
          <source>You first create a new class in the extension model.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">最初に、拡張モデルに新しいクラスを作成します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="113">
          <source>This class will augment the InventTable table, and enable access to the table's fields and methods in a manner that is easy to read and understand.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このクラスは InventTable テーブルを拡張し、読みやすく理解しやすい方法でテーブルのフィールドとメソッドにアクセスできるようにします</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="114">
          <source>It's important that you choose the correct name for your augmentation class.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">強化クラスに正しい名前を選択することが重要です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="115">
          <source>This name must be unique across all types in all models that are deployed.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この名前は、展開されるすべてのモデルのすべてのタイプにわたって一意でなければなりません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="116">
          <source>For more information, see <bpt id="p1">[</bpt>Naming guidelines for model extensions<ept id="p1">](naming-guidelines-extensions.md)</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">詳細については、<bpt id="p1">[</bpt>モデル拡張機能の名前付けガイドライン<ept id="p1">](naming-guidelines-extensions.md)</ept> を参照してください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="117">
          <source>You can now add new methods to the augmentation class.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">新しいメソッドを強化クラスを追加することができるようになりました。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="118">
          <source>These methods will then appear in IntelliSense for variables of the <bpt id="p1">**</bpt>InventTable<ept id="p1">**</ept> type, just as if they were defined directly on the table.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">これらのメソッドは、テーブルに直接定義されているかのように、<bpt id="p1">**</bpt>InventTable<ept id="p1">**</ept> 型の変数の IntelliSense に表示されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="119">
          <source>This behavior applies to both static methods and instance methods.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この動作は、静的メソッドとインスタンス メソッドの両方に適用されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="120">
          <source>There are a few rules for augmentation classes:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">拡張クラスにはいくつかのルールがあります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="121">
          <source>They must be final.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">最終である必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="122">
          <source>They must be suffixed by <bpt id="p1">**</bpt><ph id="ph1">\_</ph>Extension<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt><ph id="ph1">\_</ph>拡張子<ept id="p1">**</ept>で接尾辞を付ける必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="123">
          <source>They must be decorated with the <bpt id="p1">**</bpt>[ExtensionOf()]<ept id="p1">**</ept> attribute.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>[ExtensionOf()]<ept id="p1">**</ept> 属性で装飾されている必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="124">
          <source>Now you can use your new method, for example, from an event handler:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">たとえば、イベント ハンドラーから新しいメソッドを使用できるようになります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="125">
          <source>It is common for event handler classes to contain handlers for any number of events.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">イベント ハンドラー クラスには任意の数のイベントのハンドラーが含まれるのが一般的です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="126">
          <source>However, it is <bpt id="p1">**</bpt>not<ept id="p1">**</ept> good practice to put event handlers in augmentation classes.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ただし、イベント ハンドラーを拡張クラスに入れるのは、良い方法では<bpt id="p1">**</bpt>ありません<ept id="p1">**</ept>。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="127">
          <source>Doing so makes the event handler methods available as methods on the augmented type.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">そうすることで、イベント ハンドラー メソッドが拡張されたタイプのメソッドとして使用可能となります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="128">
          <source>This is incorrect because the event handler is intended to be called through the event, not explicitly as a method on the type.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">これは、イベント ハンドラーが、その型のメソッドとして明示的にではなく、イベントを通じて呼び出されることを意図しているので正しくありません。</target></trans-unit>
      </group>
    </body>
  </file>
</xliff>