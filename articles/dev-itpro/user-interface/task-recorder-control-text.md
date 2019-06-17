<?xml version="1.0" encoding="UTF-8"?>
<xliff xmlns:logoport="urn:logoport:xliffeditor:xliff-extras:1.0" xmlns:tilt="urn:logoport:xliffeditor:tilt-non-translatables:1.0" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns="urn:oasis:names:tc:xliff:document:1.2" xmlns:xliffext="urn:microsoft:content:schema:xliffextensions" version="1.2" xsi:schemaLocation="urn:oasis:names:tc:xliff:document:1.2 xliff-core-1.2-transitional.xsd">
  <file datatype="xml" source-language="en-US" original="task-recorder-control-text.md" target-language="ja-JP">
    <header>
      <tool tool-company="Microsoft" tool-version="1.0-7889195" tool-name="mdxliff" tool-id="mdxliff"/>
      <xliffext:skl_file_name>task-recorder-control-text.16dd1e.bfc8b5b36bacd90ba36cacfe7b925a7b812caf3d.skl</xliffext:skl_file_name>
      <xliffext:version>1.2</xliffext:version>
      <xliffext:ms.openlocfilehash>bfc8b5b36bacd90ba36cacfe7b925a7b812caf3d</xliffext:ms.openlocfilehash>
      <xliffext:ms.sourcegitcommit>9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b</xliffext:ms.sourcegitcommit>
      <xliffext:ms.lasthandoff>05/15/2019</xliffext:ms.lasthandoff>
      <xliffext:ms.openlocfilepath>articles\dev-itpro\user-interface\task-recorder-control-text.md</xliffext:ms.openlocfilepath>
    </header>
    <body>
      <group extype="content" id="content">
        <trans-unit xml:space="preserve" translate="yes" id="101" restype="x-metadata">
          <source>Control the text that Task Recorder generates for a control</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">コントロールに対してタスク レコーダーが生成するテキストの制御</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="102" restype="x-metadata">
          <source>This article describes how Task recorder determines what instruction label to generate for controls.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この記事では、タスク レコーダーがコントロールに対して生成する命令ラベルを決定する方法について説明します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="103" restype="x-metadata">
          <source>It then explains how you can make sure that these labels are meaningful for the user.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">また、これらのラベルがユーザーにとって意味があることを確認できる方法について説明します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="104">
          <source>Control the text that Task Recorder generates for a control</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">コントロールに対してタスク レコーダーが生成するテキストの制御</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="105">
          <source>This article describes how Task recorder determines what instruction label to generate for controls.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この記事では、タスク レコーダーがコントロールに対して生成する命令ラベルを決定する方法について説明します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="106">
          <source>It then explains how you can make sure that these labels are meaningful for the user.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">また、これらのラベルがユーザーにとって意味があることを確認できる方法について説明します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="107">
          <source>Every control must have useful and meaningful instruction labels, so that the task guide, Microsoft Word document, and Help content meet Content Publishing standards for readability.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">タスク ガイド、Microsoft Word 文書、およびヘルプ コンテンツは、可読性のためにコンテンツ作成標準に適合するように、すべてのコントロールには有用で意味のある指示ラベルが必要です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="108">
          <source>We must first define two terms:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">最初に、次の 2 つの項目を定義する必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="109">
          <source><bpt id="p1">**</bpt>Control label<ept id="p1">**</ept> – The value that comes from the label property on the control.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>コントロール ラベル<ept id="p1">**</ept> - コントロールのラベル プロパティから取得される値です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="110">
          <source><bpt id="p1">**</bpt>Instruction label<ept id="p1">**</ept> – The label that a control instructs Task recorder to use when it's describing how to use that control (for example, “Click OK” or “In the First name field, enter ‘John’”).</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>命令ラベル<ept id="p1">**</ept> – コントロールがそのコントロールの使用方法について記述する際にタスク レコーダーに指示するラベル (「OK をクリック」、「ファーストネームフィールドに「John」と入力します」など)。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="111">
          <source>When a control logs an event to Task recorder, three methods can be used to determine the instruction label that is shown to the user:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">コントロールがタスク レコーダーにイベントを記録するとき、次の 3 つの方法を使用して、ユーザーに表示される命令ラベルを決定できます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="112">
          <source>As part of logging the Task recorder event, the control might specify an exact instruction label ID to use.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">タスク レコーダー イベントのログの一部として、コントロールは使用する正確な命令ラベル ID を指定することがあります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="113">
          <source>As a best practice, here is how label IDs should be named: <ph id="ph1">\[</ph>client control type name<ph id="ph2">\]</ph><ph id="ph3">\_</ph><ph id="ph4">\[</ph>property or command name<ph id="ph5">\]</ph> For manual specification of an instruction label ID, see the code example later in this article (<bpt id="p1">**</bpt>OptionalInstructionLabelIDOverride<ept id="p1">**</ept>).</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ベスト プラクティスとして、ラベル ID に名前を付ける方法は以下のとおりです。<ph id="ph1">\[</ph>クライアント コントロール タイプ名<ph id="ph2">\]</ph><ph id="ph3">\_</ph><ph id="ph4">\[</ph>プロパティまたはコマンド名<ph id="ph5">\]</ph>指示ラベル ID の手動仕様については、この記事の後半のコード例を参照してください (<bpt id="p1">**</bpt>OptionalInstructionLabelIDOverride<ept id="p1">**</ept>)。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="114">
          <source>If the control doesn't explicitly specify an instruction label ID, Task recorder looks in the SysTaskRecorderLabel file to try to find an existing instruction label ID that fits the following naming syntax: <ph id="ph1">\[</ph>client control type name<ph id="ph2">\]</ph><ph id="ph3">\_</ph><ph id="ph4">\[</ph>property or command name<ph id="ph5">\]</ph> If an instruction label ID of this type is found, Task recorder uses it.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">コントロールが命令ラベル ID を明示的に指定していない場合、Task Recorder は SysTaskRecorderLabel ファイルを参照して、次の命名構文に適合する既存の命令ラベル ID を検索しようとします: <ph id="ph1">\[</ph>client control type name<ph id="ph2">\]</ph><ph id="ph3">\_</ph><ph id="ph4">\[</ph>property or command name<ph id="ph5">\]</ph>。このタイプの命令ラベル ID が見つかった場合、タスク レコーダーはそれを使用します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="115">
          <source>If a label can't be determined by using the preceding methods, Task recorder falls back to a more general-purpose instruction label.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ラベルが、上記の方法を使用して特定できない場合、タスク レコーダは、より汎用的な指示ラベルに転用されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="116">
          <source>The general purpose instruction labels are in the SysTaskRecorder label file.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">一般的な指示ラベルは、SysTaskRecorder ラベル ファイルにあります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="117">
          <source>There is one general-purpose instruction label for commands and another for properties.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">コマンド用の汎用命令ラベルが 1つ とプロパティ用の汎用命令ラベルがもう 1 つあります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="118">
          <source>Here is the general purpose instruction label for commands:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">コマンドの一般的な指示ラベルを次に示します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="119">
          <source><bpt id="p1">**</bpt>Label ID:<ept id="p1">**</ept> CommandUserAction</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>ラベル ID:<ept id="p1">**</ept> CommandUserAction</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="120">
          <source><bpt id="p1">**</bpt>Label string:<ept id="p1">**</ept> %2 the %1</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>ラベル文字列:<ept id="p1">**</ept> %2 %1</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="121">
          <source>Here is the general purpose instruction label for properties:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">プロパティの一般的な指示ラベルを次に示します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="122">
          <source><bpt id="p1">**</bpt>Label ID:<ept id="p1">**</ept> PropertySetValue</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>ラベル ID:<ept id="p1">**</ept> PropertySetValue</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="123">
          <source><bpt id="p1">**</bpt>Label string:<ept id="p1">**</ept> In the %1 field, enter %2</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>ラベル文字列:<ept id="p1">**</ept> %1 フィールドに %2 と入力する</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="124">
          <source>When Task recorder has determined which instruction label to use (via one of the preceding three methods), it strFormats the label by using the following arguments:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">タスク レコーダーは、(前の 3 つの方法のいずれかで) 使用する命令ラベルを決定すると、次の引数を使用してそのラベルの文字列の書式設定を行います。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="125">
          <source><bpt id="p1">**</bpt>%1<ept id="p1">**</ept> – This argument is the control label.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>%1<ept id="p1">**</ept> – この引数は、コントロール ラベルです。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="126">
          <source>Task recorder gets the control label by inspecting the label on the intractable.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">タスク レコーダーは、対話可能なラベルを調べることによってコントロール ラベルを取得します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="127">
          <source>However, a control can override this label and provide its own label.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ただし、コントロールはこのラベルを上書きし、個々のラベルを提供します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="128">
          <source>See the code example later in this article (<bpt id="p1">**</bpt>OptionalControlLabelOverride<ept id="p1">**</ept>).</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この記事の後半のサンプル コードを参照してください (<bpt id="p1">**</bpt>OptionalControlLabelOverride<ept id="p1">**</ept>)。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="129">
          <source><bpt id="p1">**</bpt>%2<ept id="p1">**</ept> –  This argument is either the value (for properties) or the command name (for commands).</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>%2<ept id="p1">**</ept> – この引数は、値 (プロパティの場合) またはコマンド名 (コマンドの場合) のいずれかです。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="130">
          <source>This value will be the value that the control sent to Task recorder as part of logging the event.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この値は、イベントのロギングの一部として、コントロールがタスク レコーダーに送信した値になります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="131">
          <source>However, the raw data value can be ugly or meaningless to an end user.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ただし、生データの値は、エンドユーザーにとって醜いまたは意味がないものです。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="132">
          <source>Therefore, a control can also provide a more user-friendly version of the value that Task recorder can display instead of the raw data value.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">したがって、コントロールでは、未処理のデータ値の代わりにタスク レコーダーが表示できる値のユーザー フレンドリなバージョンを提供することもできます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="133">
          <source>See the code example later in this article (<bpt id="p1">**</bpt>OptionalValueLabelOverride<ept id="p1">**</ept>).</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この記事の後半のサンプル コードを参照してください (<bpt id="p1">**</bpt>OptionalValueLabelOverride<ept id="p1">**</ept>)。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="134">
          <source><bpt id="p1">**</bpt>%3<ept id="p1">**</ept>–<bpt id="p2">**</bpt>%5<ept id="p2">**</ept> – These are command arguments and are used rarely.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>%3<ept id="p1">**</ept>–<bpt id="p2">**</bpt>%5<ept id="p2">**</ept> – これらはコマンド引数であり、めったに使用されません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="135">
          <source>However, grids use them to record the row number, for example.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ただし、たとえば、グリッドはそれらを使用して行番号を記録します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="136">
          <source>Case study</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">事例研究</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="137">
          <source>Let's use the Checkbox control as a case study for improvement.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">改善の事例研究のようにチェック ボックス コントロールを使用しましょう。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="138">
          <source>Currently, an instruction label isn't specified for the Checkbox via either method 1 or method 2 (see the previous section of this article).</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">現在、方法 1 または方法 2 (この記事の前のセクションを参照) のいずれかを介するチェックボックスに対して命令ラベルが指定されていません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="139">
          <source>Therefore, the general-purpose property instruction label is used instead.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">したがって、代わりに汎用プロパティ命令ラベルが使用されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="140">
          <source>If someone records selecting the Checkbox for a field that is named <bpt id="p1">**</bpt>Show infolog on failure<ept id="p1">**</ept>, the Task recorder output currently looks like this:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">他のユーザーが、<bpt id="p1">**</bpt>失敗した場合に情報ログを表示する<ept id="p1">**</ept>という名前のフィールドのチェック ボックスをオンにし記録する場合、現在の出荷タスク レコーダーは次のようになります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="141">
          <source>In the Show infolog on failure field, enter True.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">失敗時に情報ログ表示フィールドで、True と入力します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="142">
          <source>However, typical end users might not know what it means to set a Checkbox to <bpt id="p1">**</bpt>True<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ただし、通常エンド ユーザーは、チェック ボックスを <bpt id="p1">**</bpt>True<ept id="p1">**</ept> に設定することの意味を理解していない場合があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="143">
          <source>Therefore, a suggested improvement is for the Checkbox to produce a label that looks like this:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">したがって、次のようなラベルを生成するためのチェック ボックスの改善が推奨されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="144">
          <source>Check Show infolog on failure.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">失敗時に情報ログ表示をチェックしてください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="145">
          <source>To make this improvement, someone must add a new label ID.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">こうした改善を行うには、新しいラベル ID を追加する必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="146">
          <source>That user must then use the label ID when the event is logged to Task recorder by using method 1:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">その後、イベントがメソッド 1 を使用してタスク レコーダーにログオンしているときに、そのユーザーはラベル ID を使用する必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="147">
          <source><bpt id="p1">**</bpt>Label ID:<ept id="p1">**</ept> Checkbox<ph id="ph1">\_</ph>Value</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>ラベル ID:<ept id="p1">**</ept> Checkbox<ph id="ph1">\_</ph>Value</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="148">
          <source><bpt id="p1">**</bpt>Label string:<ept id="p1">**</ept> "%2 %1."</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>ラベル文字列:<ept id="p1">**</ept> 「%2 %1」</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="149">
          <source>This change produces output that looks like this:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この変更により、次のような出力が生成されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="150">
          <source>True Show infolog on failure.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">失敗時に infolog を表示します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="151">
          <source>This isn't quite what we want to see.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">これは見たいものではありません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="152">
          <source>Therefore, in addition, when the Checkbox logs the property change event to Task recorder, it should pass in a specific <bpt id="p1">*</bpt>value label<ept id="p1">*</ept> that says either “Check” or “Uncheck.”</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">したがって、チェックボックスがプロパティ変更イベントをタスク レコーダーに記録すると、「チェック」または「チェック解除」のいずれかを示す特定の&lt;<bpt id="p1">*</bpt>値ラベル<ept id="p1">*</ept>を渡す必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="153">
          <source>If the control explicitly specifies a value label, Task recorder will use that value label instead of the raw data value that was recorded (<bpt id="p1">**</bpt>True<ept id="p1">**</ept> or <bpt id="p2">**</bpt>False<ept id="p2">**</ept>, in this case).</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">コントロールが明示的に値ラベルを指定した場合、タスク レコーダーは記録された生データ値 (この場合は <bpt id="p1">**</bpt>True<ept id="p1">**</ept> または <bpt id="p2">**</bpt>False<ept id="p2">**</ept>) の代わりにその値ラベルを使用します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="154">
          <source>See the code example later in this article (<bpt id="p1">**</bpt>OptionalValueLabelOverride<ept id="p1">**</ept>).</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この記事の後半のサンプル コードを参照してください (<bpt id="p1">**</bpt>OptionalValueLabelOverride<ept id="p1">**</ept>)。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="155">
          <source>After the user creates the new label and specifies the value label when the event is logged to Task recorder, the control will have suitable text output:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ユーザーが新しいラベルを作成し、イベントがタスク レコーダーに記録されたときの値ラベルを指定すると、コントロールは適切なテキスト出力を行います。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="156">
          <source>Check Show infolog on failure.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">失敗時に情報ログ表示をチェックしてください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="157">
          <source>Finally, the Checkbox should have a second instruction label for “example value” usage of the Checkbox.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">最後に、チェック ボックスには、チェック ボックスの「例の値」を使用するため、2 番目の命令ラベルが必要です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="158">
          <source>“Example value” represents a special way that Task recorder displays an instruction label to the user.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">「値の例」は、タスク レコーダーがユーザーに対して指示ラベルを表示する特別な方法を示します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="159">
          <source>The author of the task recording can specify whether the task guide should instruct users to enter the same values that were entered when the guide was recorded, or whether the task guide should instruct users to enter their own values that are specific to their business requirements.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">タスク記録の作成者は、タスク ガイドが、ガイドが記録されたときに入力されたものと同じ値を入力することをユーザーに指示するかどうか、またはビジネス要件に固有の独自の値を入力することをユーザーに指示するかどうかを指定できます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="160">
          <source>Example value instruction labels have the following label ID syntax: <ph id="ph1">\[</ph>client control type name<ph id="ph2">\]</ph><ph id="ph3">\_</ph><ph id="ph4">\[</ph>property name<ph id="ph5">\]</ph><ph id="ph6">\_</ph>Example For the Checkbox example, the value label would look like this:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">値指示ラベルの例では、以下のラベル ID 構文が表示されます。<ph id="ph1">\[</ph>クライアント コントロール タイプ名<ph id="ph2">\]</ph><ph id="ph3">\_</ph><ph id="ph4">\[</ph>プロパティ名<ph id="ph5">\]</ph><ph id="ph6">\_</ph>チェックボックス例に対する例。値ラベルは次のようになります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="161">
          <source><bpt id="p1">**</bpt>Label ID:<ept id="p1">**</ept> Checkbox<ph id="ph1">\_</ph>Value<ph id="ph2">\_</ph>Example</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>ラベル ID:<ept id="p1">**</ept> Checkbox<ph id="ph1">\_</ph>Value<ph id="ph2">\_</ph>Example</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="162">
          <source><bpt id="p1">**</bpt>Label string:<ept id="p1">**</ept> “Check or uncheck the %1 field.”</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>ラベル文字列:<ept id="p1">**</ept> 「%1 フィールドをオンまたはオフにします」。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="163">
          <source>The following code example shows how property change events are logged to Task recorder by an X++ control.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">次のコード例は、X++ コントロールによってプロパティ変更イベントがタスク レコーダーに記録される様子を示しています。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="164">
          <source>Similar application programming interfaces (APIs) exist for C++ kernel controls.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">C++ カーネル コントロールには、同様のアプリケーション プログラミング インターフェイス (API) が存在します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="165">
          <source>Command events have a similar API.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">コマンド イベントに、同種の API があります。</target></trans-unit>
      </group>
    </body>
  </file>
</xliff>