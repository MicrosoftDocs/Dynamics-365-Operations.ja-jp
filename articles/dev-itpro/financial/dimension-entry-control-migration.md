<?xml version="1.0" encoding="UTF-8"?>
<xliff xmlns:logoport="urn:logoport:xliffeditor:xliff-extras:1.0" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns="urn:oasis:names:tc:xliff:document:1.2" xmlns:xliffext="urn:microsoft:content:schema:xliffextensions" version="1.2" xsi:schemaLocation="urn:oasis:names:tc:xliff:document:1.2 xliff-core-1.2-transitional.xsd">
  <file datatype="xml" source-language="en-US" original="dimension-entry-control-migration.md" target-language="ja-JP">
    <header>
      <tool tool-company="Microsoft" tool-version="1.0-7889195" tool-name="mdxliff" tool-id="mdxliff"/>
      <xliffext:skl_file_name>dimension-entry-control-migration.a8f54c.3c5f12bc04d2b2b7298381484062b62ace81ef71.skl</xliffext:skl_file_name>
      <xliffext:version>1.2</xliffext:version>
      <xliffext:ms.openlocfilehash>3c5f12bc04d2b2b7298381484062b62ace81ef71</xliffext:ms.openlocfilehash>
      <xliffext:ms.sourcegitcommit>9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b</xliffext:ms.sourcegitcommit>
      <xliffext:ms.lasthandoff>05/15/2019</xliffext:ms.lasthandoff>
      <xliffext:ms.openlocfilepath>articles\dev-itpro\financial\dimension-entry-control-migration.md</xliffext:ms.openlocfilepath>
    </header>
    <body>
      <group extype="content" id="content">
        <trans-unit xml:space="preserve" translate="yes" id="101" restype="x-metadata">
          <source>Migrate default dimensions controls to Dimension Entry controls</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">既定の分析コード コントロールを分析コード エントリ コントロールに移行する</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="102" restype="x-metadata">
          <source>This topic describes the steps necessary to migrate default dimensions controls to Dimension Entry controls after code upgrade is run.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このトピックでは、コードのアップグレードを実行した後、既定の分析コード コントロールを分析コード エントリ コントロールに移行するために必要な手順について説明します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="103" restype="x-metadata">
          <source>It uses the PurchTable form as an example.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">例として、PurchTable フォームを使用します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="104">
          <source>Migrate default dimensions controls to Dimension Entry controls</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">既定の分析コード コントロールを分析コード エントリ コントロールに移行する</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="105">
          <source>This topic describes the steps necessary to migrate default dimensions controls to Dimension Entry controls after code upgrade is run.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このトピックでは、コードのアップグレードを実行した後、既定の分析コード コントロールを分析コード エントリ コントロールに移行するために必要な手順について説明します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="106">
          <source>It uses the PurchTable form as an example.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">例として、PurchTable フォームを使用します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="107">
          <source>Simple migration scenario - PurchTable form</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">簡易移行シナリオ - PurchTable フォーム</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="108">
          <source>Search for the <bpt id="p1">**</bpt>PurchTable<ept id="p1">**</ept> form in the <bpt id="p2">**</bpt>Application Explorer<ept id="p2">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p2">**</bpt>アプリケーション エクスプローラー<ept id="p2">**</ept>で <bpt id="p1">**</bpt>PurchTable<ept id="p1">**</ept> フォームを検索します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="109">
          <source>Add the form to the current project.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">現在のプロジェクトにフォームを追加します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="110">
          <source>Open the form in the designer and code editor view.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">デザイナーとコード エディタ ビューで、フォームを開きます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="111">
          <source>In the form design view</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">フォームのデザイン ビューで</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="112">
          <source>Locate the dimension entry controls (DECs), either by manually in the control tree or by searching for "DimensionEntry" in the search bar below the <bpt id="p1">**</bpt>File<ept id="p1">**</ept> tab.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">コントロール ツリーから手動で、または<bpt id="p1">**</bpt>ファイル<ept id="p1">**</ept> タブ下の検索バーで「DimensionEntry」を検索して、分析コード エントリ コントロール (DEC) を検索します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="113">
          <source>Select the first <bpt id="p1">**</bpt>DEC<ept id="p1">**</ept> (DimensionEntryControlHeader) and verify the following:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">最初の <bpt id="p1">**</bpt>DEC<ept id="p1">**</ept> (DimensionEntryControlHeader) を選択し、以下を確認します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="114">
          <source>The type for the control, specified in parenthesis next the control, is Dimension Entry Control.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">コントロールの横にある括弧で指定されたコントロールのタイプは、Dimension Entry Control です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="115">
          <source>The Controller class property is blank.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Controller クラスのプロパティは空白になります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="116">
          <source>This property indicates what type of controller will be used by this instance of DEC, which in turn governs the behavior of the control.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このプロパティは、DEC のこのインスタンスで使用されるコントローラーのタイプを示し、これによってコントロールの動作が決まります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="117">
          <source>When this property is blank, the controller is determined by the EDT of the field specified in the <bpt id="p1">**</bpt>Value Data<ept id="p1">**</ept> field (in this case, the <bpt id="p2">**</bpt>DefaultDimension<ept id="p2">**</ept> field on the <bpt id="p3">**</bpt>PurchTable<ept id="p3">**</ept> table).</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このプロパティが空白のときは、コントローラーは、<bpt id="p1">**</bpt>値のデータ<ept id="p1">**</ept> フィールド (この場合は、<bpt id="p3">**</bpt>PurchTable<ept id="p3">**</ept> テーブルの <bpt id="p2">**</bpt>DefaultDimension<ept id="p2">**</ept> フィールド) で指定されたフィールドの EDT によって決定されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="118">
          <source>Search for the <bpt id="p1">**</bpt>PurchTable<ept id="p1">**</ept> table in the Application Explorer.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">アプリケーション エクスプローラーで <bpt id="p1">**</bpt>PurchTable<ept id="p1">**</ept> テーブルを検索します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="119">
          <source>Right-click <bpt id="p1">**</bpt>PurchTable<ept id="p1">**</ept> and select <bpt id="p2">**</bpt>Open Designer<ept id="p2">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>PurchTable<ept id="p1">**</ept> を右クリックし、<bpt id="p2">**</bpt>デザイナーを開く<ept id="p2">**</ept> を選択します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="120">
          <source>Expand the <bpt id="p1">**</bpt>Fields<ept id="p1">**</ept> node and select the <bpt id="p2">**</bpt>DefaultDimension<ept id="p2">**</ept> field.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>フィールド<ept id="p1">**</ept>ノードを展開し、<bpt id="p2">**</bpt>DefaultDimension<ept id="p2">**</ept> フィールドを選択します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="121">
          <source>The EDT property of this field is set to LedgerDefaultDimensionValueSet.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このフィールドの EDT プロパティは、LedgerDefaultDimensionValueSet に設定されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="122">
          <source>This EDT implies that this control will use the LedgerDefaultDimensionEntryController.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この EDT では、このコントロールが LedgerDefaultDimensionEntryController を使用することを意味します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="123">
          <source>Back in the <bpt id="p1">**</bpt>PurchTable<ept id="p1">**</ept> form design view, select the second <bpt id="p2">**</bpt>DEC<ept id="p2">**</ept> (DimensionEntryControlLine) and verify the following:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>PurchTable<ept id="p1">**</ept> フォーム デザイン ビューに戻って、2 番目の <bpt id="p2">**</bpt>DEC<ept id="p2">**</ept> (DimensionEntryControlLine) を選択し、次の事項を確認してください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="124">
          <source>The type for the control, specified in parenthesis next to the control, is Dimension Entry Control.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">コントロールの横にある括弧で指定されたコントロールのタイプは、Dimension Entry Control です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="125">
          <source>The Controller class property is blank.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Controller クラスのプロパティは空白になります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="126">
          <source>The controller will be determined by the EDT of the field specified in the <bpt id="p1">**</bpt>Value Data<ept id="p1">**</ept> Field, as it was for the DEC.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">コントローラーは、DEC の場合と同様に、<bpt id="p1">**</bpt>値データ<ept id="p1">**</ept> フィールドで指定されたフィールドの EDT によって決定されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="127">
          <source>Switch to the code editor view.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">コード エディター ビューに切り替えます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="128">
          <source>Search for all occurrences of "TODO: (Code Upgrade) <ph id="ph1">\[</ph>Dimension entry control<ph id="ph2">\]</ph>" in the form source code.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">フォーム ソース コードで、"TODO: (Code Upgrade) <ph id="ph1">\[</ph>Dimension entry control<ph id="ph2">\]</ph>" のすべての事例を検索します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="129">
          <source>Go through each of the remaining TODO comments as follows.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">残りの各 TODO コメントの実行は、次のようになります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="130">
          <source>Data source PurchTable</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">データ ソース PurchTable</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="131">
          <source><bpt id="p1">**</bpt>(Form <ph id="ph1">&amp;gt;</ph> Data sources <ph id="ph2">&amp;gt;</ph> PurchTable <ph id="ph3">&amp;gt;</ph> Methods<ept id="p1">**</ept>)</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>(フォーム <ph id="ph1">&amp;gt;</ph> データ ソース <ph id="ph2">&amp;gt;</ph> PurchTable <ph id="ph3">&amp;gt;</ph> メソッド<ept id="p1">**</ept>)</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="132">
          <source>Before</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">以前</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="133">
          <source>After</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">変更後</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="134">
          <source><ph id="ph1">/</ph><ph id="ph2">\*</ph> TODO: (Code Upgrade) <ph id="ph3">\[</ph>Dimension entry control<ph id="ph4">\]</ph> Replace this based on the migration guidance.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><ph id="ph1">/</ph><ph id="ph2">\*</ph> TODO: (コード アップグレード) <ph id="ph3">\[</ph>分析コード エントリ コントロール<ph id="ph4">\]</ph> 移行ガイダンスに基づいてこれを置き換えます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="135">
          <source><ph id="ph1">\*</ph>/DimensionEntryControlHeader.reactivate();</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><ph id="ph1">\*</ph>/DimensionEntryControlHeader.reactivate();</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="136">
          <source>Because this method call doesn’t have a parm method called before it, it can be deleted.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このメソッド呼び出しには前に呼び出された parm メソッドがないため、削除することができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="137">
          <source>The Dimension Entry Control only needs to be reactivated if the company or displayed dimension set changes.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">分析コード エントリ コントロールは、会社または表示されている分析コード セットが変化した場合にのみ再度有効化する必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="138">
          <source>As a general rule with reactivate method calls, if it may not be needed, remove the call and test the control to make sure it works correctly.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">メソッド呼び出しの再有効化の一般的なルールとして、必要でない場合は、呼び出しを削除し、正常に動作することを確認するためにコントロールをテストします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="139">
          <source>If it doesn’t, add the reactivate call back.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">そうでない場合は、再アクティブ化コール バックを追加します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="140">
          <source>Data field OrderAccount</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">データ フィールド OrderAccount</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="141">
          <source>(<bpt id="p1">**</bpt>Form <ph id="ph1">&amp;gt;</ph> Data sources <ph id="ph2">&amp;gt;</ph> PurchTable <ph id="ph3">&amp;gt;</ph> Fields <ph id="ph4">&amp;gt;</ph> OrderAccount <ph id="ph5">&amp;gt;</ph> Methods<ept id="p1">**</ept>)</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">(<bpt id="p1">**</bpt>フォーム<ph id="ph1">&amp;gt;</ph>データ ソース <ph id="ph2">&amp;gt;</ph>PurchTable<ph id="ph3">&amp;gt;</ph> フィールド <ph id="ph4">&amp;gt;</ph>OrderAccount<ph id="ph5">&amp;gt;</ph> 方法<ept id="p1">**</ept>)</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="142">
          <source>Before</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">以前</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="143">
          <source>After</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">変更後</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="144">
          <source><ph id="ph1">/</ph><ph id="ph2">\*</ph> TODO: (Code Upgrade) <ph id="ph3">\[</ph>Dimension entry control<ph id="ph4">\]</ph> Replace this based on the migration guidance.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><ph id="ph1">/</ph><ph id="ph2">\*</ph> TODO: (コード アップグレード) <ph id="ph3">\[</ph>分析コード エントリ コントロール<ph id="ph4">\]</ph> 移行ガイダンスに基づいてこれを置き換えます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="145">
          <source><ph id="ph1">\*</ph>/DimensionEntryControlHeader.reactivate();</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><ph id="ph1">\*</ph>/DimensionEntryControlHeader.reactivate();</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="146">
          <source>Because this method call doesn’t have a parm method called before it, it can be deleted.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このメソッド呼び出しには前に呼び出された parm メソッドがないため、削除することができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="147">
          <source>The Dimension Entry Control only needs to be reactivated if the company or displayed dimension set changes.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">分析コード エントリ コントロールは、会社または表示されている分析コード セットが変化した場合にのみ再度有効化する必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="148">
          <source>Data field ProjId</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">データ フィールド ProjId</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="149">
          <source>(<bpt id="p1">**</bpt>Form <ph id="ph1">&amp;gt;</ph> Data sources <ph id="ph2">&amp;gt;</ph> PurchTable <ph id="ph3">&amp;gt;</ph> Fields <ph id="ph4">&amp;gt;</ph> ProjId <ph id="ph5">&amp;gt;</ph> Methods<ept id="p1">**</ept>)</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">(<bpt id="p1">**</bpt>フォーム<ph id="ph1">&amp;gt;</ph>データ ソース <ph id="ph2">&amp;gt;</ph>PurchTable<ph id="ph3">&amp;gt;</ph> フィールド <ph id="ph4">&amp;gt;</ph>ProjId<ph id="ph5">&amp;gt;</ph> 方法<ept id="p1">**</ept>)</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="150">
          <source>Before</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">以前</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="151">
          <source>After</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">変更後</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="152">
          <source><ph id="ph1">/</ph><ph id="ph2">\*</ph> TODO: (Code Upgrade) <ph id="ph3">\[</ph>Dimension entry control<ph id="ph4">\]</ph> Replace this based on the migration guidance.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><ph id="ph1">/</ph><ph id="ph2">\*</ph> TODO: (コード アップグレード) <ph id="ph3">\[</ph>分析コード エントリ コントロール<ph id="ph4">\]</ph> 移行ガイダンスに基づいてこれを置き換えます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="153">
          <source><ph id="ph1">\*</ph>/DimensionEntryControlHeader.reactivate();</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><ph id="ph1">\*</ph>/DimensionEntryControlHeader.reactivate();</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="154">
          <source>Because this method call does not have a parm method called before it, it can be deleted.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このメソッドの呼び出しには前に呼び出された parm メソッドがないため、削除することができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="155">
          <source>The Dimension Entry Control only needs to be reactivated if the company or displayed dimension set changes.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">分析コード エントリ コントロールは、会社または表示されている分析コード セットが変化した場合にのみ再度有効化する必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="156">
          <source>The entire modified() method can be deleted as well because the super() call is all that remains.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">super() 呼び出しがすべて残っているため、modified() メソッド全体を削除することもできます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="157">
          <source>The ProjId class can be removed because there are no methods in it.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">メソッドが含まれていないため、ProjId クラスを削除することができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="158">
          <source>Data field VendGroup</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">データ フィールド VendGroup</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="159">
          <source>(<bpt id="p1">**</bpt>Form <ph id="ph1">&amp;gt;</ph> Data sources <ph id="ph2">&amp;gt;</ph> PurchTable <ph id="ph3">&amp;gt;</ph> Fields <ph id="ph4">&amp;gt;</ph> VendGroup <ph id="ph5">&amp;gt;</ph> Methods<ept id="p1">**</ept>)</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">(<bpt id="p1">**</bpt>フォーム<ph id="ph1">&amp;gt;</ph>データ ソース <ph id="ph2">&amp;gt;</ph>PurchTable<ph id="ph3">&amp;gt;</ph> フィールド <ph id="ph4">&amp;gt;</ph>VendGroup<ph id="ph5">&amp;gt;</ph> 方法<ept id="p1">**</ept>)</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="160">
          <source>Before</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">以前</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="161">
          <source>After</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">変更後</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="162">
          <source><ph id="ph1">/</ph><ph id="ph2">\*</ph> TODO: (Code Upgrade) <ph id="ph3">\[</ph>Dimension entry control<ph id="ph4">\]</ph> Replace this based on the migration guidance.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><ph id="ph1">/</ph><ph id="ph2">\*</ph> TODO: (コード アップグレード) <ph id="ph3">\[</ph>分析コード エントリ コントロール<ph id="ph4">\]</ph> 移行ガイダンスに基づいてこれを置き換えます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="163">
          <source><ph id="ph1">\*</ph>/DimensionEntryControlHeader.reactivate();</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><ph id="ph1">\*</ph>/DimensionEntryControlHeader.reactivate();</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="164">
          <source>Because this method call doesn’t have a parm method called before it, it can be deleted.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このメソッド呼び出しには前に呼び出された parm メソッドがないため、削除することができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="165">
          <source>The Dimension Entry Control only needs to be reactivated if the company or displayed dimension set changes.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">分析コード エントリ コントロールは、会社または表示されている分析コード セットが変化した場合にのみ再度有効化する必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="166">
          <source>The entire modified() method and VendGroup class can be deleted as well.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">modified() メソッドと VendGroup クラス全体を削除することもできます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="167">
          <source>Data source PurchLine</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">データ ソース PurchLine</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="168">
          <source>(<bpt id="p1">**</bpt>Form <ph id="ph1">&amp;gt;</ph> Data sources <ph id="ph2">&amp;gt;</ph> PurchLine <ph id="ph3">&amp;gt;</ph> Methods<ept id="p1">**</ept>)</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">(<bpt id="p1">**</bpt>フォーム<ph id="ph1">&amp;gt;</ph>データ ソース <ph id="ph2">&amp;gt;</ph>PurchLine<ph id="ph3">&amp;gt;</ph> 方法<ept id="p1">**</ept>)</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="169">
          <source>Before</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">以前</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="170">
          <source>After</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">変更後</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="171">
          <source><ph id="ph1">/</ph><ph id="ph2">\*</ph> TODO: (Code Upgrade) <ph id="ph3">\[</ph>Dimension entry control<ph id="ph4">\]</ph> Replace this based on the migration guidance.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><ph id="ph1">/</ph><ph id="ph2">\*</ph> TODO: (コード アップグレード) <ph id="ph3">\[</ph>分析コード エントリ コントロール<ph id="ph4">\]</ph> 移行ガイダンスに基づいてこれを置き換えます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="172">
          <source><ph id="ph1">\*</ph>/DimensionEntryControlLine.reactivate();<bpt id="p1">**</bpt>Note:<ept id="p1">**</ept> This is the reactivate method call in the itemIdModified method on the data source.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><ph id="ph1">\*</ph>/DimensionEntryControlLine.reactivate();<bpt id="p1">**</bpt>注記:<ept id="p1">**</ept> これはデータソースの itemIdModified メソッドにおけるメソッド呼び出しの再有効化です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="173">
          <source>Because this method call doesn’t have a parm method called before it, it can be deleted.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このメソッド呼び出しには前に呼び出された parm メソッドがないため、削除することができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="174">
          <source>The Dimension Entry Control only needs to be reactivated if the company or displayed dimension set changes.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">分析コード エントリ コントロールは、会社または表示されている分析コード セットが変化した場合にのみ再度有効化する必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="175">
          <source><ph id="ph1">/</ph><ph id="ph2">\*</ph> TODO: (Code Upgrade) <ph id="ph3">\[</ph>Dimension entry control<ph id="ph4">\]</ph> Replace this based on the migration guidance.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><ph id="ph1">/</ph><ph id="ph2">\*</ph> TODO: (コード アップグレード) <ph id="ph3">\[</ph>分析コード エントリ コントロール<ph id="ph4">\]</ph> 移行ガイダンスに基づいてこれを置き換えます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="176">
          <source><ph id="ph1">\*</ph>/DimensionEntryControlLine.reactivate();<bpt id="p1">**</bpt>Note:<ept id="p1">**</ept> This is the reactivate method call in the create() method on the data source.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><ph id="ph1">\*</ph>/DimensionEntryControlLine.reactivate();<bpt id="p1">**</bpt>注記:<ept id="p1">**</ept> これはデータソースの create() メソッドにおけるメソッド呼び出しの再有効化です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="177">
          <source>Because this method call doesn’t have a parm method called before it, it can be deleted.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このメソッド呼び出しには前に呼び出された parm メソッドがないため、削除することができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="178">
          <source>The Dimension Entry Control only needs to be reactivated if the company or displayed dimension set changes.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">分析コード エントリ コントロールは、会社または表示されている分析コード セットが変化した場合にのみ再度有効化する必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="179">
          <source>Data field AssetGroup</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">データ フィールド AssetGroup</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="180">
          <source>(<bpt id="p1">**</bpt>Form <ph id="ph1">&amp;gt;</ph> Data sources <ph id="ph2">&amp;gt;</ph> PurchLine <ph id="ph3">&amp;gt;</ph> Fields <ph id="ph4">&amp;gt;</ph> AssetGroup <ph id="ph5">&amp;gt;</ph> Methods<ept id="p1">**</ept>)</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">(<bpt id="p1">**</bpt>フォーム<ph id="ph1">&amp;gt;</ph>データ ソース <ph id="ph2">&amp;gt;</ph>PurchLine<ph id="ph3">&amp;gt;</ph> フィールド <ph id="ph4">&amp;gt;</ph>AssetGroup<ph id="ph5">&amp;gt;</ph> 方法<ept id="p1">**</ept>)</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="181">
          <source>Before</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">以前</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="182">
          <source>After</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">変更後</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="183">
          <source><ph id="ph1">/</ph><ph id="ph2">\*</ph> TODO: (Code Upgrade) <ph id="ph3">\[</ph>Dimension entry control<ph id="ph4">\]</ph> Replace this based on the migration guidance.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><ph id="ph1">/</ph><ph id="ph2">\*</ph> TODO: (コード アップグレード) <ph id="ph3">\[</ph>分析コード エントリ コントロール<ph id="ph4">\]</ph> 移行ガイダンスに基づいてこれを置き換えます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="184">
          <source><ph id="ph1">\*</ph>/DimensionEntryControlLine.reactivate();</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><ph id="ph1">\*</ph>/DimensionEntryControlLine.reactivate();</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="185">
          <source>Because this method call does not have a parm method called before it, it can be deleted.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このメソッドの呼び出しには前に呼び出された parm メソッドがないため、削除することができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="186">
          <source>The Dimension Entry Control only needs to be reactivated if the company or displayed dimension set changes.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">分析コード エントリ コントロールは、会社または表示されている分析コード セットが変化した場合にのみ再度有効化する必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="187">
          <source>The entire modified() method and AssetGroup class can be deleted as well.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">modified() メソッドと AssetGroup クラス全体を削除することもできます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="188">
          <source>Data field AssetId(<bpt id="p1">**</bpt>Form <ph id="ph1">&amp;gt;</ph> Data sources <ph id="ph2">&amp;gt;</ph> PurchLine <ph id="ph3">&amp;gt;</ph> Fields <ph id="ph4">&amp;gt;</ph> AssetId <ph id="ph5">&amp;gt;</ph> Methods<ept id="p1">**</ept>)</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">データ フィールドの AssetId (<bpt id="p1">**</bpt>フォーム <ph id="ph1">&amp;gt;</ph> データ ソース <ph id="ph2">&amp;gt;</ph>PurchLine <ph id="ph3">&amp;gt;</ph> フィールド <ph id="ph4">&amp;gt;</ph> AssetId <ph id="ph5">&amp;gt;</ph> 方法<ept id="p1">**</ept>)</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="189">
          <source>Before</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">以前</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="190">
          <source>After</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">変更後</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="191">
          <source><ph id="ph1">/</ph><ph id="ph2">\*</ph> TODO: (Code Upgrade) <ph id="ph3">\[</ph>Dimension entry control<ph id="ph4">\]</ph> Replace this based on the migration guidance.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><ph id="ph1">/</ph><ph id="ph2">\*</ph> TODO: (コード アップグレード) <ph id="ph3">\[</ph>分析コード エントリ コントロール<ph id="ph4">\]</ph> 移行ガイダンスに基づいてこれを置き換えます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="192">
          <source><ph id="ph1">\*</ph>/DimensionEntryControlLine.reactivate();</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><ph id="ph1">\*</ph>/DimensionEntryControlLine.reactivate();</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="193">
          <source>Because this method call does not have a parm method called before it, it can be deleted.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このメソッドの呼び出しには前に呼び出された parm メソッドがないため、削除することができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="194">
          <source>The Dimension Entry Control only needs to be reactivated if the company or displayed dimension set changes.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">分析コード エントリ コントロールは、会社または表示されている分析コード セットが変化した場合にのみ再度有効化する必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="195">
          <source>Data field ProcurementCategory</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">データ フィールド ProcurementCategory</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="196">
          <source>(<bpt id="p1">**</bpt>Form <ph id="ph1">&amp;gt;</ph> Data sources <ph id="ph2">&amp;gt;</ph> PurchLine <ph id="ph3">&amp;gt;</ph> Fields <ph id="ph4">&amp;gt;</ph> ProcurementCategory <ph id="ph5">&amp;gt;</ph> Methods<ept id="p1">**</ept>)</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">(<bpt id="p1">**</bpt>フォーム<ph id="ph1">&amp;gt;</ph>データ ソース <ph id="ph2">&amp;gt;</ph>PurchLine<ph id="ph3">&amp;gt;</ph> フィールド <ph id="ph4">&amp;gt;</ph>ProcurementCategory<ph id="ph5">&amp;gt;</ph> 方法<ept id="p1">**</ept>)</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="197">
          <source>Before</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">以前</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="198">
          <source>After</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">変更後</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="199">
          <source><ph id="ph1">/</ph><ph id="ph2">\*</ph> TODO: (Code Upgrade) <ph id="ph3">\[</ph>Dimension entry control<ph id="ph4">\]</ph> Replace this based on the migration guidance.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><ph id="ph1">/</ph><ph id="ph2">\*</ph> TODO: (コード アップグレード) <ph id="ph3">\[</ph>分析コード エントリ コントロール<ph id="ph4">\]</ph> 移行ガイダンスに基づいてこれを置き換えます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="200">
          <source><ph id="ph1">\*</ph>/DimensionEntryControlLine.reactivate();</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><ph id="ph1">\*</ph>/DimensionEntryControlLine.reactivate();</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="201">
          <source>Because this method call doesn’t have a parm method called before it, it can be deleted.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このメソッド呼び出しには前に呼び出された parm メソッドがないため、削除することができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="202">
          <source>The Dimension Entry Control only needs to be reactivated if the company or displayed dimension set changes.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">分析コード エントリ コントロールは、会社または表示されている分析コード セットが変化した場合にのみ再度有効化する必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="203">
          <source>Data field ProjId</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">データ フィールド ProjId</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="204">
          <source>(<bpt id="p1">**</bpt>Form <ph id="ph1">&amp;gt;</ph> Data sources <ph id="ph2">&amp;gt;</ph> PurchLine <ph id="ph3">&amp;gt;</ph> Fields <ph id="ph4">&amp;gt;</ph> ProjId <ph id="ph5">&amp;gt;</ph> Methods<ept id="p1">**</ept>)</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">(<bpt id="p1">**</bpt>フォーム<ph id="ph1">&amp;gt;</ph>データ ソース <ph id="ph2">&amp;gt;</ph>PurchLine<ph id="ph3">&amp;gt;</ph> フィールド <ph id="ph4">&amp;gt;</ph>ProjId<ph id="ph5">&amp;gt;</ph> 方法<ept id="p1">**</ept>)</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="205">
          <source>Before</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">以前</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="206">
          <source>After</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">変更後</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="207">
          <source><ph id="ph1">/</ph><ph id="ph2">\*</ph> TODO: (Code Upgrade) <ph id="ph3">\[</ph>Dimension entry control<ph id="ph4">\]</ph> Replace this based on the migration guidance.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><ph id="ph1">/</ph><ph id="ph2">\*</ph> TODO: (コード アップグレード) <ph id="ph3">\[</ph>分析コード エントリ コントロール<ph id="ph4">\]</ph> 移行ガイダンスに基づいてこれを置き換えます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="208">
          <source><ph id="ph1">\*</ph>/DimensionEntryControlLine.reactivate();</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><ph id="ph1">\*</ph>/DimensionEntryControlLine.reactivate();</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="209">
          <source>Because this method call doesn’t have a parm method called before it, it can be deleted.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このメソッド呼び出しには前に呼び出された parm メソッドがないため、削除することができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="210">
          <source>The Dimension Entry Control only needs to be reactivated if the company or displayed dimension set changes.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">分析コード エントリ コントロールは、会社または表示されている分析コード セットが変化した場合にのみ再度有効化する必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="211">
          <source>TabPage TabFinancialDimensionsLine</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">TabPage TabFinancialDimensionsLine</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="212">
          <source>(Search for TabFinancialDimensionsLine in the search bar below the form tab)</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">(フォーム タブの下にある検索バーで「TabFinancialDimensionsLine」を検索してください。)</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="213">
          <source>Before</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">以前</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="214">
          <source>After</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">変更後</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="215">
          <source><ph id="ph1">/</ph><ph id="ph2">\*</ph> TODO: (Code Upgrade) <ph id="ph3">\[</ph>Dimension entry control<ph id="ph4">\]</ph> This method can be removed if there is no custom implementation <ph id="ph5">\*</ph>///dimensionDefaultingControllerLine.pageActivated();</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><ph id="ph1">/</ph><ph id="ph2">\*</ph> TODO: (コード アップグレード) <ph id="ph3">\[</ph>分析コード エントリ コントロール<ph id="ph4">\]</ph> この方法は、カスタム実装がない場合に削除することができます <ph id="ph5">\*</ph>///dimensionDefaultingControllerHeader.pageActivated()</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="216">
          <source>The pageActivated method no longer needs to be called.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">pageActivated メソッドをもう呼び出す必要はありません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="217">
          <source>This entire method and the TabFinancialDimensionsLine class can be removed because there is no custom logic in the pageActivated method.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この全メソッドと TabFinancialDimensionsLine クラスは、pageActivated メソッドにカスタム ロジックがないため削除できます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="218">
          <source>TabPage TabFinancialDimensionsHeader</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">TabPage TabFinancialDimensionsHeader</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="219">
          <source>(Search for TabFinancialDimensionsHeader in the search bar below the form tab)</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">(フォーム タブの下にある検索バーで「TabFinancialDimensionsHeader」を検索してください。)</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="220">
          <source>Before</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">以前</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="221">
          <source>After</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">変更後</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="222">
          <source><ph id="ph1">/</ph><ph id="ph2">\*</ph> TODO: (Code Upgrade) <ph id="ph3">\[</ph>Dimension entry control<ph id="ph4">\]</ph> This method can be removed if there is no custom implementation <ph id="ph5">\*</ph>///dimensionDefaultingControllerHeader.pageActivated();</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><ph id="ph1">/</ph><ph id="ph2">\*</ph> TODO: (コード アップグレード) <ph id="ph3">\[</ph>分析コード エントリ コントロール<ph id="ph4">\]</ph> この方法は、カスタム実装がない場合に削除することができます <ph id="ph5">\*</ph>///dimensionDefaultingControllerHeader.pageActivated()</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="223">
          <source>The pageActivated method no longer needs to be called.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">pageActivated メソッドをもう呼び出す必要はありません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="224">
          <source>This entire method and the TabFinancialDimensionsHeader class can be removed because there is no custom logic in the pageActivated method.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この全メソッドと TabFinancialDimensionsHeader クラスは、pageActivated メソッドにカスタム ロジックがないため削除できます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="225">
          <source>Additional resources</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">その他のリソース</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="226">
          <source><bpt id="p1">[</bpt>Dimension Entry control uptake<ept id="p1">](dimension-entry-control-uptake.md)</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">[</bpt>分析コード エントリ コントロールの取得<ept id="p1">](dimension-entry-control-uptake.md)</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="227">
          <source><bpt id="p1">[</bpt>Dimension Entry control dialog support<ept id="p1">](dimension-entry-control-dialog-support.md)</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">[</bpt>分析コード エントリ コントロール ダイアログのサポート<ept id="p1">](dimension-entry-control-dialog-support.md)</ept></target></trans-unit>
      </group>
    </body>
  </file>
</xliff>