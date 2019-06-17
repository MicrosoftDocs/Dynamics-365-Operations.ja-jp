<?xml version="1.0" encoding="UTF-8"?>
<xliff xmlns:logoport="urn:logoport:xliffeditor:xliff-extras:1.0" xmlns:tilt="urn:logoport:xliffeditor:tilt-non-translatables:1.0" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns="urn:oasis:names:tc:xliff:document:1.2" xmlns:xliffext="urn:microsoft:content:schema:xliffextensions" version="1.2" xsi:schemaLocation="urn:oasis:names:tc:xliff:document:1.2 xliff-core-1.2-transitional.xsd">
  <file datatype="xml" source-language="en-US" original="custom-fields-mobile.md" target-language="ja-JP">
    <header>
      <tool tool-company="Microsoft" tool-version="1.0-d915bc8" tool-name="mdxliff" tool-id="mdxliff"/>
      <xliffext:skl_file_name>custom-fields-mobile.2a9e5e.4343c875da05641c57b7784bf52f1c814dd26d20.skl</xliffext:skl_file_name>
      <xliffext:version>1.2</xliffext:version>
      <xliffext:ms.openlocfilehash>4343c875da05641c57b7784bf52f1c814dd26d20</xliffext:ms.openlocfilehash>
      <xliffext:ms.sourcegitcommit>19859d8566a8c7840066b2c10c6b08b67f1b83f4</xliffext:ms.sourcegitcommit>
      <xliffext:ms.lasthandoff>06/04/2019</xliffext:ms.lasthandoff>
      <xliffext:ms.openlocfilepath>articles\financials\project-management\custom-fields-mobile.md</xliffext:ms.openlocfilepath>
    </header>
    <body>
      <group extype="content" id="content">
        <trans-unit xml:space="preserve" translate="yes" id="101" restype="x-metadata">
          <source>Implement custom fields for the Microsoft Dynamics 365 Project Timesheet mobile app on iOS and Android</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">iOS および Android 用 Microsoft Dynamics 365 Project Timesheet モバイル アプリのカスタム フィールドの実装</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="102" restype="x-metadata">
          <source>This topic provides common patterns for using extensions to implement custom fields.</source><target logoport:matchpercent="101" state="translated" state-qualifier="id-match">このトピックでは、拡張機能を使用してカスタム フィールドを実装するための共通のパターンを示します。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="103">
          <source>Implement custom fields for the Microsoft Dynamics 365 Project Timesheet mobile app on iOS and Android</source>
        <target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-inherited">iOS および Android 用 Microsoft Dynamics 365 Project Timesheet モバイル アプリのカスタム フィールドの実装</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="104">
          <source>This topic provides common patterns for using extensions to implement custom fields.</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-inherited">このトピックでは、拡張機能を使用してカスタム フィールドを実装するための共通のパターンを示します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="105">
          <source>The following topics are covered:</source><target logoport:matchpercent="101" state="translated" state-qualifier="id-match">トピックの対象は次のとおりです。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="106">
          <source>The various data types that the custom field framework supports</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">カスタム フィールド フレームワークでサポートされるさまざまなデータ型</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="107">
          <source>How to show read-only or editable fields on timesheet entries, and save user-provided values back to the database</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">タイムシート エントリに読み取り専用または編集可能なフィールドを表示し、ユーザーが入力した値をデータベースに再保存する方法</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="108">
          <source>How to show read-only fields on the timesheet header</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">タイムシート ヘッダーに読み取り専用フィールドを表示する方法</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="109">
          <source>How to integrate other custom business logic to enter default values in fields and do additional validation</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">他のカスタム ビジネス ロジックを統合して、フィールドに既定値を入力し、追加の検証を行う方法</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="110">
          <source>Audience</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">対象者</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="111">
          <source>This topic is intended for developers who are integrating their custom fields into the Microsoft Dynamics 365 Project Timesheet mobile application that is available for Apple iOS and Google Android.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">このトピックは、Apple iOS および Google Android で利用可能な Microsoft Dynamics 365 Project Timesheet モバイル アプリケーションにカスタムフィールドを統合する開発者を対象としています。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="112">
          <source>The assumption is that readers are familiar with X++ development and project timesheet functionality.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">読者が X++ 開発とプロジェクト タイムシート機能をよく使用していることを前提としています。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="113">
          <source>Data contract – TSTimesheetCustomField X++ class</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">データ契約 – TSTimesheetCustomField X++ クラス</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="114">
          <source>The <bpt id="p1">**</bpt>TSTimesheetCustomField<ept id="p1">**</ept> class is the X++ data contract class that represents information about a custom field for timesheet functionality.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt"><bpt id="p1">**</bpt>TSTimesheetCustomField<ept id="p1">**</ept> クラスは、X++ データ契約クラスで、タイムシート機能のカスタム フィールドに関する情報を表します。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="115">
          <source>Lists of the custom field objects are passed on both the TSTimesheetDetails data contract and the TSTimesheetEntry data contract to show custom fields in the mobile app.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">モバイル アプリにカスタム フィールドを表示するために、TSTimesheetDetails データ契約と TSTimesheetEntry データ契約の両方にカスタム フィールド オブジェクトのリストが渡されます。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="116">
          <source><bpt id="p1">**</bpt>TSTimesheetDetails<ept id="p1">**</ept> - The timesheet header contract.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt"><bpt id="p1">**</bpt>TSTimesheetDetails<ept id="p1">**</ept> - タイムシートのヘッダー契約。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="117">
          <source><bpt id="p1">**</bpt>TSTimesheetEntry<ept id="p1">**</ept> - The timesheet transaction contract.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt"><bpt id="p1">**</bpt>TSTimesheetEntry<ept id="p1">**</ept> - タイムシートのトランザクション契約。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="118">
          <source>Groups of these objects that have the same project information and <bpt id="p1">**</bpt>timesheetLineRecId<ept id="p1">**</ept> value constitute a line.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">同じプロジェクト情報と <bpt id="p1">**</bpt>timesheetLineRecId<ept id="p1">**</ept> 値を持つオブジェクトのグループが 1 つの明細行を構成します。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="119">
          <source>fieldBaseType (Types)</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">fieldBaseType (タイプ)</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="120">
          <source>The <bpt id="p1">**</bpt>FieldBaseType<ept id="p1">**</ept> property on the <bpt id="p2">**</bpt>TsTimesheetCustom<ept id="p2">**</ept> object determines the type of the field that appears in the app.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt"><bpt id="p2">**</bpt>TsTimesheetCustom<ept id="p2">**</ept> オブジェクトの <bpt id="p1">**</bpt>FieldBaseType<ept id="p1">**</ept> プロパティによって、アプリに表示されるフィールドのタイプが決定されます。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="121">
          <source>The following <bpt id="p1">**</bpt>Types<ept id="p1">**</ept> values that are supported.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">次の<bpt id="p1">**</bpt>タイプ<ept id="p1">**</ept>の値がサポートされます。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="122">
          <source>Types value</source><target logoport:matchpercent="81" state="translated" state-qualifier="fuzzy-match">タイプの値</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="123">
          <source>Type</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">型</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="124">
          <source>Notes</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">摘要</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="125">
          <source>0</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">0</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="126">
          <source>String (and Enum)</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">文字列 (および列挙)</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="127">
          <source>The field appears as a text field.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">このフィールドは、テキスト フィールドとして表示されます。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="128">
          <source>1</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">1</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="129">
          <source>Integer</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">整数</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="130">
          <source>The value is shown as a number without decimal places.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">この値は、小数点以下を含まない数字として表示されます。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="131">
          <source>2</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">2</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="132">
          <source>Real</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">実績</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="133">
          <source>The value is shown as a number that has decimal places.</source><target logoport:matchpercent="84" state="translated" state-qualifier="fuzzy-match">この値は、小数点以下を含む数字として表示されます。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="134">
          <source>To show the real value as a currency in the app, use the <bpt id="p1">**</bpt>fieldExtenededType<ept id="p1">**</ept> property.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">アプリで通貨として実数値を表示するには、<bpt id="p1">**</bpt>fieldExtenededType<ept id="p1">**</ept> プロパティを使用します。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="135">
          <source>You can use the <bpt id="p1">**</bpt>numberOfDecimals<ept id="p1">**</ept> property to set the number of decimal places that are shown.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt"><bpt id="p1">**</bpt>numberOfDecimals<ept id="p1">**</ept> プロパティを使用し、表示される小数点以下の桁数を設定することができます。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="136">
          <source>3</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">3</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="137">
          <source>Date</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">日</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="138">
          <source>Date formats are determined by the user's <bpt id="p1">**</bpt>Date, times, and number format<ept id="p1">**</ept> setting that is specified under <bpt id="p2">**</bpt>Language and country/region preference<ept id="p2">**</ept> in <bpt id="p3">**</bpt>User options<ept id="p3">**</ept>.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">日付の形式は、<bpt id="p3">**</bpt>ユーザー オプション<ept id="p3">**</ept>の<bpt id="p2">**</bpt>言語と国/地域の基本設定<ept id="p2">**</ept>の下で指定される、ユーザーの<bpt id="p1">**</bpt>日付、時刻、および数字の形式<ept id="p1">**</ept>の設定によって決定されます。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="139">
          <source>4</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">4</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="140">
          <source>Boolean</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">ブール型</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="141">
          <source>15</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">15</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="142">
          <source>GUID</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">GUID</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="143">
          <source>16</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">16</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="144">
          <source>Int64</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">Int64</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="145">
          <source>If the <bpt id="p1">**</bpt>stringOptions<ept id="p1">**</ept> property isn't provided on the <bpt id="p2">**</bpt>TSTimesheetCustomField<ept id="p2">**</ept> object, a free-text field is provided to the user.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt"><bpt id="p1">**</bpt>stringOptions<ept id="p1">**</ept> プロパティが <bpt id="p2">**</bpt>TSTimesheetCustomField<ept id="p2">**</ept> オブジェクトで指定されていない場合、自由書式のフィールドがユーザーに提供されます。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="146">
          <source>The <bpt id="p1">**</bpt>stringLength<ept id="p1">**</ept> property can be used to set the maximum string length that users can enter.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt"><bpt id="p1">**</bpt>stringLength<ept id="p1">**</ept> プロパティを使用し、ユーザーが入力できる最大文字列長を設定することができます。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="147">
          <source>If the <bpt id="p1">**</bpt>stringOptions<ept id="p1">**</ept> property is provided on the <bpt id="p2">**</bpt>TSTimesheetCustomField<ept id="p2">**</ept> object, those list elements are the only values that users can select by using option buttons (radio buttons).</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt"><bpt id="p1">**</bpt>stringOptions<ept id="p1">**</ept> プロパティが <bpt id="p2">**</bpt>TSTimesheetCustomField<ept id="p2">**</ept> オブジェクトで指定された場合、これらのリスト要素が、ユーザーがオプション ボタン (ラジオ ボタン) を使用して選択できる唯一の値になります。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="148">
          <source>In this case, the string field can act as an enum value for the purpose of user entry.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">この場合、文字列フィールドは、ユーザーの入力を目的とする列挙値として機能します。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="149">
          <source>To save the value to the database as an enum, manually map the string value back to the enum value before you save to the database by using chain of command (see the “Use chain of command on the TSTimesheetEntryService class to save a timesheet entry from the app back to the database” section later in this topic for an example).</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">データベースに値を列挙として保存するには、コマンド チェーンを使用してデータベースに保存する前に、手動で文字列値を列挙値にマップします (このトピックで後述する「TSTimesheetEntryService クラスでコマンド チェーンを使用し、アプリからデータベースにタイムシート エントリを再保存する」のセクションの例を参照してください)。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="150">
          <source>fieldExtendedType (TSCustomFieldExtendedType)</source><target logoport:matchpercent="0" state="translated">fieldExtendedType (TSCustomFieldExtendedType)</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="151">
          <source>You can use this property to format real values as currency.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">このプロパティを使用して、通貨として実数値の書式設定をすることができます。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="152">
          <source>This approach is applicable only when the <bpt id="p1">**</bpt>fieldBaseType<ept id="p1">**</ept> value is <bpt id="p2">**</bpt>Real<ept id="p2">**</ept>.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">この方法は、<bpt id="p1">**</bpt>fieldBaseType<ept id="p1">**</ept> の値が<bpt id="p2">**</bpt>実数<ept id="p2">**</ept>である場合にのみ適用されます。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="153">
          <source><bpt id="p1">**</bpt>TSCustomFieldExtendedType:None<ept id="p1">**</ept> – No formatting is applied.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt"><bpt id="p1">**</bpt>TSCustomFieldExtendedType:None<ept id="p1">**</ept> – 書式設定は適用されません。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="154">
          <source><bpt id="p1">**</bpt>TSCustomFieldExtendedType::Currency<ept id="p1">**</ept> – Format the value as currency.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt"><bpt id="p1">**</bpt>TSCustomFieldExtendedType::Currency<ept id="p1">**</ept> – 通貨として値の書式設定します。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="155">
          <source>When currency formatting is active, the <bpt id="p1">**</bpt>stringValue<ept id="p1">**</ept> field can be used pass the currency code that should be shown in the app.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">通貨の書式設定が有効な場合、<bpt id="p1">**</bpt>stringValue<ept id="p1">**</ept> フィールドを使用してアプリに表示する通貨コードを渡すことができます。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="156">
          <source>The value is a read-only value.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">値は読み取り専用です。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="157">
          <source>The <bpt id="p1">**</bpt>realValue<ept id="p1">**</ept> field contains the money amount that should be saved to the database.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt"><bpt id="p1">**</bpt>realValue<ept id="p1">**</ept> フィールドには、データベースに保存する必要のある金額が含まれています。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="158">
          <source>fieldSection (TSCustomFieldSection)</source><target logoport:matchpercent="0" state="translated">fieldSection (TSCustomFieldSection)</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="159">
          <source>You can use this property specify where the custom field should appear in the app.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">このプロパティを使用して、カスタム フィールドを必要のあるアプリ内の場所を指定することができます。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="160">
          <source><bpt id="p1">**</bpt>TSCustomFieldSection::Header<ept id="p1">**</ept> – The field will appear in the <bpt id="p2">**</bpt>View more details<ept id="p2">**</ept> section in the app.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt"><bpt id="p1">**</bpt>TSCustomFieldSection::Header<ept id="p1">**</ept> – このフィールドはアプリの<bpt id="p2">**</bpt>詳細を表示<ept id="p2">**</ept>セクションに表示されます。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="161">
          <source>These fields are always read-only.</source><target logoport:matchpercent="83" state="translated" state-qualifier="fuzzy-match">これらのフィールドは、常に読み取り専用です。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="162">
          <source><bpt id="p1">**</bpt>TSCustomFieldSection::Line<ept id="p1">**</ept> – The field will appear after all the out-of-box line fields on timesheet entries.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt"><bpt id="p1">**</bpt>TSCustomFieldSection::Line<ept id="p1">**</ept> – このフィールドはタイムシート エントリで最初から用意されている明細行フィールドすべての後に表示されます。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="163">
          <source>These fields can be either editable or read-only.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">これらのフィールドは、編集可能または読み取り専用のいずれかになります。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="164">
          <source>fieldName (FieldNameShort)</source><target logoport:matchpercent="0" state="translated">fieldName (FieldNameShort)</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="165">
          <source>This property identifies the field when values that the app provides are saved back to the database.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">このプロパティにより、アプリによって指定される値がデータベースに再保存される時にフィールドを識別します。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="166">
          <source>tableName (TableNameShort)</source><target logoport:matchpercent="0" state="translated">tableName (TableNameShort)</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="167">
          <source>This property identifies the field when values that the app provides are saved back to the database.</source>
        <target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-inherited">このプロパティにより、アプリによって指定される値がデータベースに再保存される時にフィールドを識別します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="168">
          <source>isEditable (NoYes)</source><target logoport:matchpercent="0" state="translated">isEditable (NoYes)</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="169">
          <source>Set this property to <bpt id="p1">**</bpt>Yes<ept id="p1">**</ept> to specify that the field in the timesheet entry section should be editable by users.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">このプロパティを<bpt id="p1">**</bpt>はい<ept id="p1">**</ept>に設定し、ユーザーが編集可能なタイムシート エントリ セクションのフィールドを指定することができます。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="170">
          <source>Set the property to <bpt id="p1">**</bpt>No<ept id="p1">**</ept> to make the field read-only.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">このプロパティを<bpt id="p1">**</bpt>いいえ<ept id="p1">**</ept>に設定し、フィールドを読み取り専用にすることができます。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="171">
          <source>isMandatory (NoYes)</source><target logoport:matchpercent="0" state="translated">isMandatory (NoYes)</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="172">
          <source>Set this property to <bpt id="p1">**</bpt>Yes<ept id="p1">**</ept> to specify that the field in the timesheet entry section should be mandatory.</source><target logoport:matchpercent="87" state="translated" state-qualifier="fuzzy-match">このプロパティを<bpt id="p1">**</bpt>はい<ept id="p1">**</ept>に設定し、タイムシート エントリ セクションの必須のフィールドを指定することができます。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="173">
          <source>label (str)</source><target logoport:matchpercent="0" state="translated">label (str)</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="174">
          <source>This property specifies the label that is shown next the field in the app.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">このプロパティにより、アプリのフィールドの次に表示されるラベルを指定します。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="175">
          <source>stringOptions (List of Strings)</source><target logoport:matchpercent="0" state="translated">stringOptions (文字列のリスト)</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="176">
          <source>This property is applicable only when <bpt id="p1">**</bpt>fieldBaseType<ept id="p1">**</ept> is set to <bpt id="p2">**</bpt>String<ept id="p2">**</ept>.</source><target logoport:matchpercent="72" state="translated" state-qualifier="fuzzy-match">このプロパティは、<bpt id="p1">**</bpt>fieldBaseType<ept id="p1">**</ept> が<bpt id="p2">**</bpt>文字列<ept id="p2">**</ept>に設定されている場合にのみ適用されます。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="177">
          <source>If <bpt id="p1">**</bpt>stringOptions<ept id="p1">**</ept> is set, the string values that are available for selection via option buttons (radio buttons) are specified by the strings in the list.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt"><bpt id="p1">**</bpt>stringOptions<ept id="p1">**</ept> が設定されている場合、オプション ボタン (ラジオ ボタン) により選択可能な文字列値は、リストの文字列によって指定されます。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="178">
          <source>If no strings are provided, free-text entry in the string field is allowed (see the “Use chain of command on the TSTimesheetEntryService class to save a timesheet entry from the app back to the database” section later in this topic for an example).</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">文字列が指定されなかった場合、文字列フィールドの自由書式のテキストが許可されます (このトピックで後述する「TSTimesheetEntryService クラスでコマンド チェーンを使用し、アプリからデータベースにタイムシート エントリを再保存する」のセクションの例を参照してください)。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="179">
          <source>stringLength (int)</source><target logoport:matchpercent="0" state="translated">stringLength (int)</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="180">
          <source>This property specifies the maximum length for a string field.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">このプロパティにより、文字列フィールドの長さの最大値を指定します。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="181">
          <source>It's applicable only when <bpt id="p1">**</bpt>fieldBaseType<ept id="p1">**</ept> is set to <bpt id="p2">**</bpt>String<ept id="p2">**</ept>.</source><target logoport:matchpercent="79" state="translated" state-qualifier="fuzzy-match"><bpt id="p1">**</bpt>fieldBaseType<ept id="p1">**</ept> が<bpt id="p2">**</bpt>文字列<ept id="p2">**</ept>に設定されている場合にのみ適用されます。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="182">
          <source>numberOfDecimals (int)</source><target logoport:matchpercent="0" state="translated">numberOfDecimals (int)</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="183">
          <source>This property specifies the number of decimal places that are shown for a real field.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">このプロパティにより、実数フィールドに表示される小数点以下の桁数を指定します。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="184">
          <source>It's applicable only when <bpt id="p1">**</bpt>fieldBaseType<ept id="p1">**</ept> is set to <bpt id="p2">**</bpt>Real<ept id="p2">**</ept>.</source><target logoport:matchpercent="89" state="translated" state-qualifier="fuzzy-match"><bpt id="p1">**</bpt>fieldBaseType<ept id="p1">**</ept> が<bpt id="p2">**</bpt>実数<ept id="p2">**</ept>に設定されている場合にのみ適用されます。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="185">
          <source>orderSequence (int)</source><target logoport:matchpercent="0" state="translated">orderSequence (int)</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="186">
          <source>This property controls the order in which the custom fields are shown in the app when more than one custom field is specified.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">このプロパティにより、複数のカスタム フィールドが指定された場合に、カスタム フィールドがアプリに表示される順序を制御します。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="187">
          <source>Fields that have lower numbers are shown first.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">番号が小さいフィールドが最初に表示されます。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="188">
          <source>booleanValue (boolean)</source><target logoport:matchpercent="0" state="translated">booleanValue (ブール型)</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="189">
          <source>For fields of the <bpt id="p1">**</bpt>Boolean<ept id="p1">**</ept> type, this property passes the Boolean value of the field between the server and the app.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt"><bpt id="p1">**</bpt>ブール型<ept id="p1">**</ept>のタイプのフィールドの場合、このプロパティはサーバーとアプリの間でフィールドのブール値を渡します。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="190">
          <source>guidValue (guid)</source><target logoport:matchpercent="0" state="translated">guidValue (guid)</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="191">
          <source>For fields of the <bpt id="p1">**</bpt>GUID<ept id="p1">**</ept> type, this property passes the globally unique identifier (GUID) value of the field between the server and the app.</source><target logoport:matchpercent="81" state="translated" state-qualifier="fuzzy-match"><bpt id="p1">**</bpt>GUID<ept id="p1">**</ept> のタイプのフィールドの場合、このプロパティはサーバーとアプリの間でフィールドのグローバル一意識別子 (GUID) を渡します。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="192">
          <source>int64Value (int64)</source><target logoport:matchpercent="0" state="translated">int64Value (int64)</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="193">
          <source>For fields of the <bpt id="p1">**</bpt>Int64<ept id="p1">**</ept> type, this property passes the int64 value of the field between the server and the app.</source><target logoport:matchpercent="89" state="translated" state-qualifier="fuzzy-match"><bpt id="p1">**</bpt>Int64<ept id="p1">**</ept> タイプのフィールドの場合、このプロパティはサーバーとアプリの間でフィールドの int64 値を渡します。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="194">
          <source>intValue (int)</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">intValue (int)</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="195">
          <source>For fields of the <bpt id="p1">**</bpt>Int<ept id="p1">**</ept> type, this property passes the int value of the field between the server and the app.</source><target logoport:matchpercent="92" state="translated" state-qualifier="fuzzy-match"><bpt id="p1">**</bpt>Int<ept id="p1">**</ept> タイプのフィールドの場合、このプロパティはサーバーとアプリの間でフィールドの int 値を渡します。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="196">
          <source>realValue (real)</source><target logoport:matchpercent="0" state="translated">realValue (実数)</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="197">
          <source>For fields of the <bpt id="p1">**</bpt>Real<ept id="p1">**</ept> type, this property passes the real value of the field between the server and the app .</source><target logoport:matchpercent="89" state="translated" state-qualifier="fuzzy-match"><bpt id="p1">**</bpt>実数<ept id="p1">**</ept>タイプのフィールドの場合、このプロパティはサーバーとアプリの間でフィールドの実数値を渡します。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="198">
          <source>stringValue (str)</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">stringValue (str)</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="199">
          <source>For fields of the <bpt id="p1">**</bpt>String<ept id="p1">**</ept> type, this property passes the string value of the field between the server and the app.</source><target logoport:matchpercent="89" state="translated" state-qualifier="fuzzy-match"><bpt id="p1">**</bpt>文字列<ept id="p1">**</ept>タイプのフィールドの場合、このプロパティはサーバーとアプリの間でフィールドの文字列値を渡します。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="200">
          <source>It's also used for fields of the <bpt id="p1">**</bpt>Real<ept id="p1">**</ept> type that are formatted as currency.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">通貨として書式設定された<bpt id="p1">**</bpt>実数<ept id="p1">**</ept>タイプのフィールドにも使用されます。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="201">
          <source>For those fields, the property is used to pass the currency code to the app.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">これらのフィールドについて、このプロパティはアプリに通貨コードを渡すために使用されます。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="202">
          <source>dateValue (date)</source><target logoport:matchpercent="0" state="translated">dateValue (日付)</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="203">
          <source>For fields of the <bpt id="p1">**</bpt>Date<ept id="p1">**</ept> type, this property passes the date value of the field between the server and the app.</source><target logoport:matchpercent="89" state="translated" state-qualifier="fuzzy-match"><bpt id="p1">**</bpt>日付<ept id="p1">**</ept>タイプのフィールドの場合、このプロパティはサーバーとアプリの間でフィールドの日付値を渡します。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="204">
          <source>Show and save a custom field in the timesheet entry section</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">タイムシート エントリ セクションのカスタム フィールドの表示および保存</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="205">
          <source>Below is a screenshot from the mobile app of a timesheet entry creation.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">タイムシート エントリを作成するモバイル アプリのスクリーンショットを次に示します。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="206">
          <source>It shows the out-of-box fields and a custom field in the "Time entry" section called "Test string" with an enum value of "Second option" already set.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">「テスト文字列」と呼ばれる「時間エントリ」に最初から用意されているフィールドとカスタム フィールドが、すでに設定されている「2 番目のオプション」の列挙値と共に表示されます。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="207">
          <source>Test string custom field in the app</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">アプリのテスト文字列のカスタム フィールド</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="208">
          <source>Below is a screenshot from the mobile app of the user selecting one of the enum options available for the "Test string" custom field.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">「テスト文字列」のカスタム フィールドで使用可能な列挙オプションのいずれかを選択しているユーザーのモバイル アプリのスクリーンショットは次のとおりです。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="209">
          <source>The two options are "First option" and "Second option" shown as radio buttons.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">ラジオ ボタンとして表示されている「1 番目のオプション」と「2 番目のオプション」の 2 つのオプションがあります。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="210">
          <source>The second option is currently selected.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">現在、2 番目のオプションが選択されています。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="211">
          <source>Option buttons (radio buttons) for the Test string custom field</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">テスト文字列のカスタム フィールドのオプション ボタン (ラジオ ボタン)</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="212">
          <source>Extend the TSTimesheetLine table so that it has a custom field</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">カスタム フィールドが含まれるように TSTimesheetLine テーブルを拡張します。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="213">
          <source>In typical scenarios, it's likely that the data for a custom field in the timesheet entry section will be saved to the TSTimesheetLine table.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">一般的なシナリオでは、タイムシート エントリ セクションのカスタム フィールドのデータが TSTimesheetLine テーブルに保存されることがあります。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="214">
          <source>However, other tables can be used if the data can be retrieved based on a TSTimesheetTrans record that is provided, or if it doesn't have specific record context (for example, if the field is set as read-only in the project parameters).</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">ただし、他のテーブルは、指定された TSTimesheetTrans レコードに基づいてデータが取得された場合、またはTSTimesheetTransレコードに基づいてデータを取得できる場合、または固有のレコード コンテキストを持たない場合に使用されます (たとえば、プロジェクト パラメーターでフィールドが読み取り専用として設定されている場合です)。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="215">
          <source>Note that custom fields don't have to have any backing database records.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">カスタム フィールドには、バッキングのデータベース レコードを持つ必要がないことに注意してください。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="216">
          <source>They can be dynamically generated based on X++ logic.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">X++ ロジックに基づいて動的に生成することができます。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="217">
          <source>This approach can be useful in read-only scenarios (see the “Use chain of command on the TSTimesheetDetails class, buildCustomFieldListForHeader method to fill in timesheet details” section for an example of dynamically generated custom field values.)</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">この方法は読み取り専用のシナリオで役に立ちます (動的に生成されたカスタム フィールド値の例については、「TSTimesheetDetails クラスでコマンド チェーンを使用し、buildCustomFieldListForHeader メソッドによりタイムシートの詳細を入力する」のセクションを参照してください。)</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="218">
          <source>Below is a screenshot from Visual Studio of the Application Object Tree.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">アプリケーション オブジェクト ツリーの Visual Studio のスクリーンショットを次に示します。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="219">
          <source>It shows an extension of the TSTimesheetLine table with the TestLineString field added as a custom field.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">TSTimesheetLine テーブルの拡張機能とカスタム フィールドとして追加された TestLineString フィールドを表示します。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="220">
          <source>Line string</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">行文字列</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="221">
          <source>Use chain of command on the buildCustomFieldList method of the TSTimesheetSettings class to show a field in the timesheet entry section</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">TSTimesheetSettings クラスの buildCustomFieldList メソッドのコマンド チェーンを使用して、タイムシート エントリ セクションにフィールドを表示します。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="222">
          <source>This code controls the display settings for the field in the app.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">このコードにより、アプリのフィールドの表示設定を制御します。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="223">
          <source>For example, it controls the type of field, the label, whether the field is mandatory, and what section the field appears in.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">たとえば、フィールドのタイプ、ラベル、フィールドが必須であるかどうか、またフィールドが表示されるセクションを制御します。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="224">
          <source>The following example shows a string field on time entries.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">次の例は、時間入力の文字列フィールドを示します。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="225">
          <source>This field has two options, <bpt id="p1">**</bpt>First option<ept id="p1">**</ept> and <bpt id="p2">**</bpt>Second option<ept id="p2">**</ept>, that are available via option buttons (radio buttons).</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">このフィールドには、<bpt id="p1">**</bpt>1 番目のオプション<ept id="p1">**</ept>と<bpt id="p2">**</bpt>2 番目のオプション<ept id="p2">**</ept>の 2 つのオプションがあり、オプション ボタン (ラジオ ボタン) を介して使用可能です。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="226">
          <source>The field in the app is associated with the <bpt id="p1">**</bpt>TestLineString<ept id="p1">**</ept> field that is added to the TSTimesheetLine table.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">アプリのフィールドは、TSTimesheetLine テーブルに追加される <bpt id="p1">**</bpt>TestLineString<ept id="p1">**</ept> フィールドに関連付けられています。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="227">
          <source>Note the use of the <bpt id="p1">**</bpt>TSTimesheetCustomField::newFromMetatdata()<ept id="p1">**</ept> method to simplify the initialization of the custom field properties: <bpt id="p2">**</bpt>fieldBaseType<ept id="p2">**</ept>, <bpt id="p3">**</bpt>tableName<ept id="p3">**</ept>, <bpt id="p4">**</bpt>fieldname<ept id="p4">**</ept>, <bpt id="p5">**</bpt>label<ept id="p5">**</ept>, <bpt id="p6">**</bpt>isEditable<ept id="p6">**</ept>, <bpt id="p7">**</bpt>isMandatory<ept id="p7">**</ept>, <bpt id="p8">**</bpt>stringLength<ept id="p8">**</ept>, and <bpt id="p9">**</bpt>numberOfDecimals<ept id="p9">**</ept>.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt"><bpt id="p1">**</bpt>TSTimesheetCustomField::newFromMetatdata()<ept id="p1">**</ept> メソッドを使用して、<bpt id="p2">**</bpt>fieldBaseType<ept id="p2">**</ept>、<bpt id="p3">**</bpt>tableName<ept id="p3">**</ept>、<bpt id="p4">**</bpt>fieldname<ept id="p4">**</ept>、<bpt id="p5">**</bpt>label<ept id="p5">**</ept>、<bpt id="p6">**</bpt>isEditable<ept id="p6">**</ept>、<bpt id="p7">**</bpt>isMandatory<ept id="p7">**</ept>、<bpt id="p8">**</bpt>stringLength<ept id="p8">**</ept>、および <bpt id="p9">**</bpt>numberOfDecimals<ept id="p9">**</ept> のカスタム フィールド プロパティの初期化を簡略化することに注意してください。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="228">
          <source>You can also set these parameters manually, as you prefer.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">これらのパラメーターは、必要に応じて手動で設定することもできます。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="229">
          <source>Use chain of command on the buildCustomFieldListForEntry method of the TSTimesheetEntry class to enter values in a timesheet entry</source><target logoport:matchpercent="75" state="translated" state-qualifier="fuzzy-match">TSTimesheetEntry クラスの buildCustomFieldListForEntry メソッドのコマンド チェーンを使用して、タイムシート エントリに値を入力します。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="230">
          <source>The <bpt id="p1">**</bpt>buildCustomFieldListForEntry<ept id="p1">**</ept> method is used to enter values on the saved timesheet lines in the mobile app.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt"><bpt id="p1">**</bpt>buildCustomFieldListForEntry<ept id="p1">**</ept> メソッドは、モバイル アプリの保存されたタイムシートの明細行に値を入力するために使用されます。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="231">
          <source>It takes a TSTimesheetTrans record as a parameter.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">TSTimesheetTrans レコードをパラメーターとして使用します。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="232">
          <source>Fields from that record can be used to fill in the custom field value in the app.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">レコードのフィールドを使用して、アプリのカスタム フィールドの値を入力することができます。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="233">
          <source>Use chain of command on the TSTimesheetEntryService class to save a timesheet entry from the app back to the database</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">TSTimesheetEntryService クラスのコマンド チェーンを使用して、アプリからデータベースにタイムシートのエントリを再保存します。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="234">
          <source>To save a custom field back to the database in typical usage, you must extend multiple methods:</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">通常の方法でデータベースにカスタム フィールドを再保存するには、複数のメソッドを拡張する必要があります。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="235">
          <source>The <bpt id="p1">**</bpt>timesheetLineNeedsUpdating<ept id="p1">**</ept> method is used to determine whether the line record has been changed by the user in the app and must be saved to the database.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt"><bpt id="p1">**</bpt>timesheetLineNeedsUpdating<ept id="p1">**</ept> メソッドを使用して、明細行レコードがアプリでユーザーによって変更されたかどうか、およびデータベースに保存する必要があるかどうかを特定します。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="236">
          <source>If performance isn't a concern, this method can be simplified so that it always returns <bpt id="p1">**</bpt>true<ept id="p1">**</ept>.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">パフォーマンスが問題にならない場合は、このメソッドを簡略化し、常に <bpt id="p1">**</bpt>True<ept id="p1">**</ept> を返すようにすることができます。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="237">
          <source>The <bpt id="p1">**</bpt>populateTimesheetLineFromEntryDuringCreate<ept id="p1">**</ept> and <bpt id="p2">**</bpt>populateTimesheetLineFromEntryDuringUpdate<ept id="p2">**</ept> methods can be extended so that they enter values in the TSTimesheetLine database record from the TSTimesheetEntry data contract record that is provided.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt"><bpt id="p1">**</bpt>populateTimesheetLineFromEntryDuringCreate<ept id="p1">**</ept> および <bpt id="p2">**</bpt>populateTimesheetLineFromEntryDuringUpdate<ept id="p2">**</ept> メソッドを拡張し、指定された TSTimesheetEntry データ コントラクト レコードから TSTimesheetLine データベース レコードに値を入力できるようにすることができます。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="238">
          <source>In the example that follows, notice how the mapping between the database field and the entry field is manually done via X++ code.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">次の例では、データベース フィールドと入力フィールドの間のマッピングが X++ コードを介して手動で行われる方法に注意してください。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="239">
          <source>The <bpt id="p1">**</bpt>populateTimesheetWeekFromEntry<ept id="p1">**</ept> method can also be extended if the custom field that is mapped to the <bpt id="p2">**</bpt>TSTimesheetEntry<ept id="p2">**</ept> object must write back to the TSTimesheetLineweek database table.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt"><bpt id="p2">**</bpt>TSTimesheetEntry<ept id="p2">**</ept> オブジェクトにマップされているカスタム フィールドを TSTimesheetLineweek データベース テーブル に再書き込みする必要がある場合、<bpt id="p1">**</bpt>populateTimesheetWeekFromEntry<ept id="p1">**</ept> メソッドは拡張することもできます。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="240">
          <source>The following example saves the <bpt id="p1">**</bpt>firstOption<ept id="p1">**</ept> or <bpt id="p2">**</bpt>secondOption<ept id="p2">**</ept> value that the user selects to the database as a raw string value.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">次の例では、ユーザーが未加工の文字列値としてデータベースに選択した <bpt id="p1">**</bpt>firstOption<ept id="p1">**</ept> または <bpt id="p2">**</bpt>secondOption<ept id="p2">**</ept> の値を保存します。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="241">
          <source>If the database field is a field of the <bpt id="p1">**</bpt>Enum<ept id="p1">**</ept> type, those values can be manually mapped to an enum value and then saved to an enum field on the database table.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">データベース フィールドが<bpt id="p1">**</bpt>列挙<ept id="p1">**</ept>タイプのフィールドである場合、これらの値を手動で列挙値にマップし、データベース テーブルの列挙フィールドに保存することができます。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="242">
          <source>Show a custom field in the timesheet header section</source><target logoport:matchpercent="75" state="translated" state-qualifier="fuzzy-match">タイムシート ヘッダー セクションのカスタム フィールドの表示</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="243">
          <source>Below is a screenshot from the mobile app of a user viewing a timesheet.</source><target logoport:matchpercent="82" state="translated" state-qualifier="fuzzy-match">ユーザーがタイムシートを表示しているモバイル アプリのスクリーンショットを次に示します。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="244">
          <source>The "More information" button has been selected in the upper-right corner to show the "View more details" option.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">「詳細を表示」オプションを表示するために、右上隅にある「詳細情報」ボタンが選択されています。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="245">
          <source>View more details command</source><target logoport:matchpercent="77" state="translated" state-qualifier="fuzzy-match">詳細なコマンドを表示</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="246">
          <source>Below is a screenshot from the mobile app showing the “More” section of a timesheet.</source><target logoport:matchpercent="75" state="translated" state-qualifier="fuzzy-match">タイムシートの「詳細」セクションを表示しているモバイル アプリのスクリーンショットを次に示します。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="247">
          <source>A custom field called “Utilization rate of this timesheet (computed custom field)” has been added to the timesheet header section.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">「このタイムシートの稼動率 (計算されたカスタム フィールド)」と呼ばれるカスタム フィールドがタイムシートのヘッダー セクションに追加されました。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="248">
          <source>A read-only value of "0.667" is set on the custom field.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">「0.667」の読み取り専用値がカスタム フィールドに設定されています。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="249">
          <source>More section</source><target logoport:matchpercent="79" state="translated" state-qualifier="fuzzy-match">詳細セクション</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="250">
          <source>Extend the TSTimesheetTable table so that it has a custom field</source><target logoport:matchpercent="90" state="translated" state-qualifier="fuzzy-match">カスタム フィールドが含まれるように TSTimesheetTable テーブルを拡張します。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="251">
          <source>In typical scenarios, it's likely that the data for a custom field in the header section will be pulled from the TSTimesheetHeader table.</source><target logoport:matchpercent="82" state="translated" state-qualifier="fuzzy-match">一般的なシナリオでは、ヘッダー セクションのカスタム フィールドのデータが TSTimesheetHeader テーブルから引き出されることがあります。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="252">
          <source>However, other tables can be used if the data can be retrieved based on a TSTimesheetTable record that is provided, or if it doesn't have specific record context (for example, if the field is set as read-only in the project parameters).</source><target logoport:matchpercent="97" state="translated" state-qualifier="fuzzy-match">ただし、他のテーブルは、指定された TSTimesheetTable のレコードに基づいてデータが取得された場合、またはTSTimesheetTransレコードに基づいてデータを取得できる場合、または固有のレコード コンテキストを持たない場合に使用されます (たとえば、プロジェクト パラメーターでフィールドが読み取り専用として設定されている場合です)。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="253">
          <source>Note that custom fields don't have to have any backing database records.</source>
        <target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-inherited">カスタム フィールドには、バッキングのデータベース レコードを持つ必要がないことに注意してください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="254">
          <source>They can be dynamically generated based on X++ logic.</source>
        <target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-inherited">X++ ロジックに基づいて動的に生成することができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="255">
          <source>The example that follows shows this approach.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">次の例はこの方法を示しています。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="256">
          <source>Fields in the header section are always read-only in the app.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">ヘッダー セクションのフィールドは、アプリでは常に読み取り専用です。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="257">
          <source>Use chain of command on the buildCustomFieldList method of the TSTimesheetSettings class to show a field in the header section</source><target logoport:matchpercent="89" state="translated" state-qualifier="fuzzy-match">TSTimesheetSettings クラスの buildCustomFieldList メソッドのコマンド チェーンを使用して、ヘッダー セクションにフィールドを表示します。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="258">
          <source>This code controls the display settings for the field in the app.</source>
        <target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-inherited">このコードにより、アプリのフィールドの表示設定を制御します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="259">
          <source>For example, it controls the type of field, the label, whether the field is mandatory, and what section the field appears in.</source>
        <target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-inherited">たとえば、フィールドのタイプ、ラベル、フィールドが必須であるかどうか、またフィールドが表示されるセクションを制御します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="260">
          <source>The following example shows a computed value in the header section in the app.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">次の例では、アプリのヘッダー セクションに計算された値を表示します。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="261">
          <source>Use chain of command on the buildCustomFieldListForHeader method of the TSTimesheetDetails class to fill in timesheet details</source><target logoport:matchpercent="75" state="translated" state-qualifier="fuzzy-match">TSTimesheetDetails クラスの buildCustomFieldListForHeader メソッドのコマンド チェーンを使用して、タイムシートの詳細を記入します。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="262">
          <source>The <bpt id="p1">**</bpt>buildCustomFieldListForHeader<ept id="p1">**</ept> method is used to fill in the timesheet header details in the mobile app.</source><target logoport:matchpercent="71" state="translated" state-qualifier="fuzzy-match"><bpt id="p1">**</bpt>buildCustomFieldListForHeader<ept id="p1">**</ept> メソッドは、モバイル アプリのタイムシート ヘッダーの詳細を記入するために使用されます。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="263">
          <source>It takes a TSTimesheetTable record as a parameter.</source><target logoport:matchpercent="87" state="translated" state-qualifier="fuzzy-match">TSTimesheetTable レコードをパラメーターとして使用します。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="264">
          <source>Fields from that record can be used to fill in the custom field value in the app.</source>
        <target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-inherited">レコードのフィールドを使用して、アプリのカスタム フィールドの値を入力することができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="265">
          <source>The following example doesn't read any values from the database.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">次の例では、データベースから値を読み取ることができません。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="266">
          <source>Instead, it uses X++ logic to generate a computed value that is then shown in the app.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">代わりに、X++ ロジックを使用して、アプリに表示される計算値を生成します。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="267">
          <source>Other configurability/extensibility opportunities</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">他のコンフィギュレーションの可能性または機能拡張の機会</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="268">
          <source>Adding additional validation for the app</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">アプリへの追加検証の追加</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="269">
          <source>Existing logic for timesheet functionality at the database level will still work as expected.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">タイムシート機能に対するデータベース レベルでの既存のロジックは、期待どおりに動作します。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="270">
          <source>To interrupt the completion of save or submit operations and show a specific error message, you can add <bpt id="p1">**</bpt>throw error("message to user")<ept id="p1">**</ept> to the code via a chain of command extension.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">保存または送信操作の完了を中断して特定のエラー メッセージを表示するために、コマンド チェーン拡張機能を介してコードに<bpt id="p1">**</bpt>エラーをスロー (「ユーザーへのメッセージ」)<ept id="p1">**</ept> を追加することができます。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="271">
          <source>Here are three examples of useful extensible methods:</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">便利で拡張可能なメソッドの 3 つの例を示します。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="272">
          <source>If <bpt id="p1">**</bpt>validateWrite<ept id="p1">**</ept> on the TSTimesheetLine table returns <bpt id="p2">**</bpt>false<ept id="p2">**</ept> during a save operation for a timesheet line, an error message is shown in the mobile app.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">タイムシートの明細行に対する保存操作中に TSTimesheetLine テーブルの <bpt id="p1">**</bpt>validateWrite<ept id="p1">**</ept> が <bpt id="p2">**</bpt>False<ept id="p2">**</ept> を返す場合、エラー メッセージがモバイル アプリに表示されます。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="273">
          <source>If <bpt id="p1">**</bpt>validateSubmit<ept id="p1">**</ept> on the TSTimesheetTable table returns <bpt id="p2">**</bpt>false<ept id="p2">**</ept> during timesheet submission in the app, an error message is shown to the user.</source><target logoport:matchpercent="72" state="translated" state-qualifier="fuzzy-match">アプリでタイムシートの送信中に TSTimesheetTable テーブルの <bpt id="p1">**</bpt>validateSubmit<ept id="p1">**</ept> が <bpt id="p2">**</bpt>False<ept id="p2">**</ept> を返す場合、エラー メッセージがユーザーに表示されます。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="274">
          <source>Logic that fills in fields (for example, <bpt id="p1">**</bpt>Line Property<ept id="p1">**</ept>) during the <bpt id="p2">**</bpt>insert<ept id="p2">**</ept> method on the TSTimesheetLine table will still run.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">TSTimesheetLine テーブルの<bpt id="p2">**</bpt>挿入<ept id="p2">**</ept>メソッドの実行中にフィールドを入力するロジック (たとえば、<bpt id="p1">**</bpt>明細行プロパティ<ept id="p1">**</ept>) も実行されます。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="275">
          <source>Hiding and marking out-of-box fields as read-only via configuration</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">コンフィギュレーションにより、最初から用意されているフィールドを非表示また読み取り専用としてマーキング</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="276">
          <source>From the project parameters, you can make out-of-box fields read-only or hidden in the mobile app.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">プロジェクト パラメーターから、最初から用意されているフィールドをモバイル アプリで読み取り専用または非表示にすることができます。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="277">
          <source>Set the options in the <bpt id="p1">**</bpt>Mobile timesheets<ept id="p1">**</ept> section on the <bpt id="p2">**</bpt>Timesheet<ept id="p2">**</ept> tab of the <bpt id="p3">**</bpt>Project management and accounting parameters<ept id="p3">**</ept> page.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt"><bpt id="p3">**</bpt>プロジェクト管理と会計パラメーター<ept id="p3">**</ept> ページの<bpt id="p2">**</bpt>タイムシート<ept id="p2">**</ept> タブで、<bpt id="p1">**</bpt>モバイル タイムシート<ept id="p1">**</ept> セクションのオプションを設定します。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="278">
          <source>Project parameters</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">プロジェクト パラメーター</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="279">
          <source>Changing the activities that are available for selection via extensions</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">拡張機能を介して選択可能な活動の変更</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="280">
          <source>The activities that are available for selection for a project are filled in via the <bpt id="p1">**</bpt>getActivitiesForProject()<ept id="p1">**</ept> and <bpt id="p2">**</bpt>getActivityQuery()<ept id="p2">**</ept> methods in the <bpt id="p3">**</bpt>TsTimesheetProjectService<ept id="p3">**</ept> class.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">プロジェクトに対して選択可能な活動は、<bpt id="p3">**</bpt>TsTimesheetProjectService<ept id="p3">**</ept> クラスの <bpt id="p1">**</bpt>getActivitiesForProject()<ept id="p1">**</ept> および <bpt id="p2">**</bpt>getActivityQuery()<ept id="p2">**</ept> メソッドを介して入力されます。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="281">
          <source>You can use chain of command to change this behavior to match your business scenario for the activities that are available for selection for a specific project.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">コマンド チェーンを使用してこの動作を変更し、特定のプロジェクトに対して選択可能な活動のビジネス シナリオに一致させることができます。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="282">
          <source>Entering a default project category on timesheet entries</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">タイムシート エントリに既定のプロジェクト カテゴリを入力する</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="283">
          <source>Entry of a default project category on timesheet entries occurs at three levels.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">タイムシート エントリの既定のプロジェクト カテゴリの入力は、3 つのレベルで発生します。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="284">
          <source>You can use chain of command to extend the behavior at any or all of these levels to achieve the desired behavior.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">コマンド チェーンを使用してこれらのレベルのいずれかまたはすべてにおける動作を拡張することにより、目的の動作を実現することができます。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="285">
          <source>The following hierarchy is used:</source><target logoport:matchpercent="82" state="translated" state-qualifier="fuzzy-match">次の階層が使用されます。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="286">
          <source>The app tries to put the default category from the project resource.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">アプリは、プロジェクト リソースからの既定のカテゴリの配置を試みます。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="287">
          <source>This default category is set in the <bpt id="p1">**</bpt>getCurrentUserResource<ept id="p1">**</ept> and <bpt id="p2">**</bpt>getDelegatedResourcesForCurrentUser<ept id="p2">**</ept> methods in the <bpt id="p3">**</bpt>TSTimesheetSettingsService<ept id="p3">**</ept> class.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">この既定のカテゴリは、<bpt id="p3">**</bpt>TSTimesheetSettingsService<ept id="p3">**</ept> クラスの <bpt id="p1">**</bpt>getCurrentUserResource<ept id="p1">**</ept> および <bpt id="p2">**</bpt>getDelegatedResourcesForCurrentUser<ept id="p2">**</ept> メソッドで設定されます。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="288">
          <source>If the default category isn't provided at the project resource level, the app tries to pull it from the project activity.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">プロジェクト リソース レベルで既定のカテゴリが指定されていない場合、アプリはプロジェクト活動からの取得を試みます。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="289">
          <source>This default category is set in the <bpt id="p1">**</bpt>getActivitiesForProject<ept id="p1">**</ept> method in the <bpt id="p2">**</bpt>TSTimesheetProjectService<ept id="p2">**</ept> class.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">この既定のカテゴリは、<bpt id="p2">**</bpt>TSTimesheetProjectService<ept id="p2">**</ept> クラスの <bpt id="p1">**</bpt>getActivitiesForProject<ept id="p1">**</ept> メソッドで設定されます。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="290">
          <source>If the default category isn't provided at the project activity level, the default category it taken from the project parameters.</source><target logoport:matchpercent="82" state="translated" state-qualifier="fuzzy-match">プロジェクト活動レベルで既定のカテゴリが指定されていない場合、既定のカテゴリはプロジェクトのパラメーターから取得されます。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="291">
          <source>This default category is set in the <bpt id="p1">**</bpt>getProjectDetailsbyRule<ept id="p1">**</ept> method in the <bpt id="p2">**</bpt>TSTimesheetProjectService<ept id="p2">**</ept> class.</source><target logoport:matchpercent="91" state="translated" state-qualifier="fuzzy-match">この既定のカテゴリは、<bpt id="p2">**</bpt>TSTimesheetProjectService<ept id="p2">**</ept> クラスの <bpt id="p1">**</bpt>getProjectDetailsbyRule<ept id="p1">**</ept> メソッドで設定されます。</target>
        </trans-unit>
      </group>
    </body>
  </file>
</xliff>