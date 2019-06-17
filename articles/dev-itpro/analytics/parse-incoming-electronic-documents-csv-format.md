<?xml version="1.0" encoding="UTF-8"?>
<xliff xmlns:logoport="urn:logoport:xliffeditor:xliff-extras:1.0" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns="urn:oasis:names:tc:xliff:document:1.2" xmlns:xliffext="urn:microsoft:content:schema:xliffextensions" version="1.2" xsi:schemaLocation="urn:oasis:names:tc:xliff:document:1.2 xliff-core-1.2-transitional.xsd">
  <file datatype="xml" source-language="en-US" original="parse-incoming-electronic-documents-csv-format.md" target-language="ja-JP">
    <header>
      <tool tool-company="Microsoft" tool-version="1.0-7889195" tool-name="mdxliff" tool-id="mdxliff"/>
      <xliffext:skl_file_name>parse-incoming-electronic-documents-csv-format.cdcacd.55ee537e4a113091b6e95aed71b195ccf84599ae.skl</xliffext:skl_file_name>
      <xliffext:version>1.2</xliffext:version>
      <xliffext:ms.openlocfilehash>55ee537e4a113091b6e95aed71b195ccf84599ae</xliffext:ms.openlocfilehash>
      <xliffext:ms.sourcegitcommit>9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b</xliffext:ms.sourcegitcommit>
      <xliffext:ms.lasthandoff>05/15/2019</xliffext:ms.lasthandoff>
      <xliffext:ms.openlocfilepath>articles\dev-itpro\analytics\parse-incoming-electronic-documents-csv-format.md</xliffext:ms.openlocfilepath>
    </header>
    <body>
      <group extype="content" id="content">
        <trans-unit xml:space="preserve" translate="yes" id="101" restype="x-metadata">
          <source>Parse incoming documents in CSV format</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">CSV 形式で受信したドキュメントを解析する</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="102" restype="x-metadata">
          <source>This topic provides information about how to set up Electronic reporting (ER) formats to parse incoming CSV formatted documents.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このトピックでは、受信した CSV 形式のドキュメントを解析するように電子報告 (ER) 形式を設定する方法について説明します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="103">
          <source>Parse incoming documents in CSV format</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">CSV 形式で受信したドキュメントを解析する</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="104">
          <source>You can design Electronic reporting (ER) formats to parse incoming electronic documents that represent tabular data in plain text (files in CSV format) and then use the content from these documents to update application data.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">電子申告 (ER) 書式をデザインして、プレーン テキスト内 (CSV 形式のファイル) の表形式データを表す受信した電子ドキュメントを解析し、これらのドキュメントからの内容を使用してアプリケーション データを更新することができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="105">
          <source>The following approach can be used:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">次のアプローチを使用できます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="106">
          <source>Begin your format's design by adding a new root sequence element to specify that each line in the parsing file is considered a separate record.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">解析ファイル内の各明細行は別々のレコードとみなすように指定して、新しいルート シーケンス要素を追加することによりフォーマットのデザインを開始します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="107">
          <source>In the added sequence element, select the appropriate value, for example <bpt id="p1">**</bpt>New line - Windows (CR LF)<ept id="p1">**</ept>, in the <bpt id="p2">**</bpt>Special characters<ept id="p2">**</ept> field in the <bpt id="p3">**</bpt>Sequence element delimiter<ept id="p3">**</ept> field group.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">追加されたシーケンス要素で、適切な値を選択します。たとえば、<bpt id="p3">**</bpt>シーケンス要素の区切り記号<ept id="p3">**</ept>フィールド グループの<bpt id="p2">**</bpt>特殊文字<ept id="p2">**</ept>フィールドの<bpt id="p1">**</bpt>改行 - Windows (CR LF)<ept id="p1">**</ept>。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="108">
          <source>Continue your format's design by adding a nested sequence element of the added root sequence element to specify that each line in the parsing file is considered as a set of fields.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">追加されたルート シーケンス要素の入れ子になった順序要素を追加して、解析ファイル内の各行が一連のフィールドとみなされるように指定して、フォーマットのデザインを続行します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="109">
          <source>You can specify the character in the <bpt id="p1">**</bpt>Custom delimiter<ept id="p1">**</ept> field that will be recognized in the parsing line as a fields separator.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">解析明細行でフィールド区切りとして認識される <bpt id="p1">**</bpt>区切り記号<ept id="p1">**</ept> フィールドで、文字列を指定することができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="110">
          <source>You can define different field separators for different sequence elements to parse specific file lines in which fields are separated by different characters.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">異なるシーケンス要素に異なるフィールド区切りを定義して、フィールドが異なる文字で区切られている特定のファイルの明細行を解析することができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="111">
          <source>The <bpt id="p1">**</bpt>Custom delimiter<ept id="p1">**</ept> field can be left blank for certain sequence elements.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>カスタム区切り記号<ept id="p1">**</ept> フィールドは、特定のシーケンス要素では空白のままにできます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="112">
          <source>An empty field means that any file line that is parsed by using this sequence will be parsed like a .txt (fixed length text) file line.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">空のフィールドは、この順序を使用して解析されるファイル行が .txt (固定長テキスト) ファイル行のように解析されることを意味します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="113">
          <source>In the <bpt id="p1">**</bpt>Quotation application<ept id="p1">**</ept> field, select the value when you expect that some fields of any line that is parsed by this sequence element will be enclosed by certain characters.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>見積申請<ept id="p1">**</ept>フィールドで、このシーケンス要素で解析される明細行の一部のフィールドが特定の文字で囲まれることが期待される場合は値を選択します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="114">
          <source>The following options are available:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"> 次のオプションを使用できます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="115">
          <source><bpt id="p1">**</bpt>All<ept id="p1">**</ept> – Include quotation characters in the parsing line for any field of any data type.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>すべて<ept id="p1">**</ept> – 任意のデータ型の任意のフィールドについて、解析明細行の引用文字を含めます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="116">
          <source>If you select this, define the desired characters in the <bpt id="p1">**</bpt>Quotation mark<ept id="p1">**</ept> field that will be used for fields quotation.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">これを選択した場合、フィールド見積に使用される<bpt id="p1">**</bpt>引用符<ept id="p1">**</ept>フィールドで目的の文字を定義します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="117">
          <source>For example, the double quotes character.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">たとえば、二重引用符文字。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="118">
          <source><bpt id="p1">**</bpt>Text only<ept id="p1">**</ept> – Include quotation characters in the parsing line for any field of the <bpt id="p2">**</bpt>String<ept id="p2">**</ept> data type.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>テキストのみ<ept id="p1">**</ept> – は <bpt id="p2">**</bpt>文字列<ept id="p2">**</ept> データ型の任意のフィールドの解析行に引用符を含めます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="119">
          <source>If you select this, define the desired characters in the <bpt id="p1">**</bpt>Quotation mark<ept id="p1">**</ept> field that will be used for fields quotation.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">これを選択した場合、フィールド見積に使用される<bpt id="p1">**</bpt>引用符<ept id="p1">**</ept>フィールドで目的の文字を定義します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="120">
          <source><bpt id="p1">**</bpt>Derive from parent only<ept id="p1">**</ept> – Use the same <bpt id="p2">**</bpt>Quotation application<ept id="p2">**</ept> field settings that are defined for the parent sequence element.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>親のみから派生<ept id="p1">**</ept> – 親シーケンス要素に定義されている、同じ<bpt id="p2">**</bpt>見積申請<ept id="p2">**</ept>フィールド設定を使用します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="121">
          <source>Note that the <bpt id="p1">**</bpt>Quotation mark<ept id="p1">**</ept> field setting will be taken from the settings of the parent sequence element as well.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>引用符<ept id="p1">**</ept>フィールドの設定も親シーケンス要素の設定から取得されることに注意してください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="122">
          <source><bpt id="p1">**</bpt>None<ept id="p1">**</ept> – Exclude quotation characters in the parsing line for any field of any data type.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>なし<ept id="p1">**</ept> – 任意のデータ型の任意のフィールドについて、解析明細行の引用文字を除外します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="123">
          <source>Complete your format's design by adding nested elements for the added sequence element that represents the set of fields of the parsing line.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">解析明細行のフィールド セットを表す、追加されたシーケンス要素の入れ子になった要素を追加して、フォーマットのデザインを完成させます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="124">
          <source>Add the required elements of the <bpt id="p1">**</bpt>Text<ept id="p1">**</ept> group, such as <bpt id="p2">**</bpt>String<ept id="p2">**</ept>, <bpt id="p3">**</bpt>DateTime<ept id="p3">**</ept>, and <bpt id="p4">**</bpt>Numeric<ept id="p4">**</ept>, to describe the structure of the parsing line as a set of individual fields of different data types.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p2">**</bpt>文字列<ept id="p2">**</ept>、<bpt id="p3">**</bpt>DateTime<ept id="p3">**</ept>、<bpt id="p4">**</bpt>数値<ept id="p4">**</ept>のような<bpt id="p1">**</bpt>テキスト<ept id="p1">**</ept> グループの必要な要素を追加して、異なるデータ型の個々のフィールドのセットとして解析行の構造を記述することができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="125">
          <source>For each format element that represents an individual field of the parsing line, by default, nothing is selected in the <bpt id="p1">**</bpt>Multiplicity<ept id="p1">**</ept> field.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">解析の明細行の個々のフィールドを表す形式要素については、既定では、<bpt id="p1">**</bpt>多様性<ept id="p1">**</ept>フィールドでは何も選択されません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="126">
          <source>This means that the value of the field in the parsing line is considered required.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">これは、解析行のフィールドの値が必須と見なされることを意味します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="127">
          <source>In the <bpt id="p1">**</bpt>Multiplicity<ept id="p1">**</ept> field, select <bpt id="p2">**</bpt>Zero one<ept id="p2">**</ept> to consider the value of this field in the parsing line as optional.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>多様性<ept id="p1">**</ept>フィールドで、<bpt id="p2">**</bpt>ゼロ、1 つ<ept id="p2">**</ept>を選択してオプションとして解析明細行のこのフィールドの値を検討します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="128">
          <source>The data source item <bpt id="p1">**</bpt>isMatch<ept id="p1">**</ept> is available when you map this format to ER data model for each <bpt id="p2">**</bpt>String<ept id="p2">**</ept>, <bpt id="p3">**</bpt>DateTime<ept id="p3">**</ept>, or <bpt id="p4">**</bpt>Numeric<ept id="p4">**</ept> format element with the option <bpt id="p5">**</bpt>Zero one<ept id="p5">**</ept> selected in the <bpt id="p6">**</bpt>Multiplicity<ept id="p6">**</ept> field.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">データソースの品目 <bpt id="p1">**</bpt>isMatch<ept id="p1">**</ept> は、<bpt id="p2">**</bpt>多様性<ept id="p2">**</ept>フィールドで<bpt id="p3">**</bpt>ゼロ、1 つ<ept id="p3">**</ept>が選択されている場合、この形式を各<bpt id="p4">**</bpt>文字列<ept id="p4">**</ept>、<bpt id="p5">**</bpt>日時<ept id="p5">**</ept>、または<bpt id="p6">**</bpt>数値<ept id="p6">**</ept>形式要素の ER データモデルにマップすると使用できます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="129">
          <source>When this field contains a value, <bpt id="p1">**</bpt>isMatch<ept id="p1">**</ept> will return <bpt id="p2">**</bpt>True<ept id="p2">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このフィールドに値が含まれているときは、<bpt id="p1">**</bpt>isMatch<ept id="p1">**</ept> は <bpt id="p2">**</bpt>True<ept id="p2">**</ept> を返します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="130">
          <source>If there is no value in the field, it will return <bpt id="p1">**</bpt>False<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">フィールドに値がない場合は、<bpt id="p1">**</bpt>False<ept id="p1">**</ept> が返されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="131">
          <source>To learn more about this feature, play the task guide, <bpt id="p1">**</bpt>ER Create a format configuration to import data from an external CSV file<ept id="p1">**</ept> (part of the 7.5.4.3 Acquire/Develop IT service/solution components (10677) business process), which walks through how the incoming CSV file can be parsed by using the ER format to update application data.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この機能の詳細については、<bpt id="p1">**</bpt>ER 外部 CSV ファイルからデータをインポートするフォーマット構成を作成する<ept id="p1">**</ept>(「IT サービス/ソリューション コンポーネントの取得/開発 (10677)」の一部) タスク ガイドを再生してください。これは、ER フォーマットを使用して、受信した CSV ファイルを解析してアプリケーション データを更新する方法について説明しています。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="132">
          <source>Download the following files to complete the task guide mentioned above.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">上記のタスクガイドを完成させるには、次のファイルをダウンロードしてください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="133">
          <source>Title</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">肩書き</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="134">
          <source>File name</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ファイル名</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="135">
          <source>ER format configuration</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ER フォーマット構成</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="136">
          <source><bpt id="p1">[</bpt>1099formatcsv.xml<ept id="p1">](https://go.microsoft.com/fwlink/?linkid=862266)</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">[</bpt>1099formatcsv.xml<ept id="p1">](https://go.microsoft.com/fwlink/?linkid=862266)</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="137">
          <source>Sample of incoming file in .csv format</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">.csv 形式の受信ファイルのサンプル</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="138">
          <source><bpt id="p1">[</bpt>1099entriescsv.csv<ept id="p1">](https://go.microsoft.com/fwlink/?linkid=862266)</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">[</bpt>1099entriescsv.csv<ept id="p1">](https://go.microsoft.com/fwlink/?linkid=862266)</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="139">
          <source>Download the following file that is required to complete the task guide mentioned above if you have not played the task guide, <bpt id="p1">**</bpt>ER Create required configurations to import data from an external file for electronic reporting<ept id="p1">**</ept> in the current Dynamics 365 for Finance and Operation application.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">タスク ガイドを再生していない場合は、上記のタスク ガイドを完了するために必要な次のファイルをダウンロードしてください。現在の Dynamics 365 for Finance and Operation アプリケーションの <bpt id="p1">**</bpt>ER Create は電子レポート用に外部ファイルからデータをインポートするために必要な設定<ept id="p1">**</ept>。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="140">
          <source>Title</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">肩書き</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="141">
          <source>File name</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ファイル名</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="142">
          <source>ER model configuration</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ER モデル構成</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="143">
          <source><bpt id="p1">[</bpt>1099model.xml<ept id="p1">](https://go.microsoft.com/fwlink/?linkid=862266)</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">[</bpt>1099model.xml<ept id="p1">](https://go.microsoft.com/fwlink/?linkid=862266)</ept></target></trans-unit>
      </group>
    </body>
  </file>
</xliff>