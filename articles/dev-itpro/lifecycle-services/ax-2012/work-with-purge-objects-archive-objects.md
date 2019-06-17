<?xml version="1.0" encoding="UTF-8"?>
<xliff xmlns:logoport="urn:logoport:xliffeditor:xliff-extras:1.0" xmlns:tilt="urn:logoport:xliffeditor:tilt-non-translatables:1.0" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns="urn:oasis:names:tc:xliff:document:1.2" xmlns:xliffext="urn:microsoft:content:schema:xliffextensions" version="1.2" xsi:schemaLocation="urn:oasis:names:tc:xliff:document:1.2 xliff-core-1.2-transitional.xsd">
  <file datatype="xml" source-language="en-US" original="work-with-purge-objects-archive-objects.md" target-language="ja-JP">
    <header>
      <tool tool-company="Microsoft" tool-version="1.0-7889195" tool-name="mdxliff" tool-id="mdxliff"/>
      <xliffext:skl_file_name>work-with-purge-objects-archive-objects.b47f7b.f02fe16d6f7917c28b6930ec8f0c338c7d47ef53.skl</xliffext:skl_file_name>
      <xliffext:version>1.2</xliffext:version>
      <xliffext:ms.openlocfilehash>f02fe16d6f7917c28b6930ec8f0c338c7d47ef53</xliffext:ms.openlocfilehash>
      <xliffext:ms.sourcegitcommit>9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b</xliffext:ms.sourcegitcommit>
      <xliffext:ms.lasthandoff>05/15/2019</xliffext:ms.lasthandoff>
      <xliffext:ms.openlocfilepath>articles\dev-itpro\lifecycle-services\ax-2012\work-with-purge-objects-archive-objects.md</xliffext:ms.openlocfilepath>
    </header>
    <body>
      <group extype="content" id="content">
        <trans-unit xml:space="preserve" translate="yes" id="101" restype="x-metadata">
          <source>Work with purge and archive objects</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">オブジェクトの削除とアーカイブを使用する</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="102" restype="x-metadata">
          <source>This topic provides information about purge and archive objects in the Intelligent Data Management Framework (IDMF).</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このトピックでは、インテリジェント データ管理フレームワーク (IDMF) のパージ オブジェクトとアーカイブ オブジェクトについて説明します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="103">
          <source>Work with purge and archive objects</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">オブジェクトの削除とアーカイブを使用する</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="104">
          <source>Add/Edit rules</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ルールの追加/編集</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="105">
          <source>A rule is the criterion that is used to filter records when a purge task or an archive task runs.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ルールは、削除タスクまたはアーカイブ タスクの実行時に、レコードをフィルター処理するために使用される基準です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="106">
          <source>This command lets you work with rules in a Purge Object or an Archive Object.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このコマンドを使用すると、削除オブジェクトまたはアーカイブ オブジェクト内のルールを操作できます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="107">
          <source>The rules generally apply to the driver table, but can also be applied to a related child table.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ルールは一般的にドライバー テーブルに適用されますが、関連する子テーブルにも適用できます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="108">
          <source>For example, the Purge Object <bpt id="p1">**</bpt>ProdJournalTable<ept id="p1">**</ept> includes a rule for the <bpt id="p2">**</bpt>ProdTable<ept id="p2">**</ept>, which is not the driver table.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">たとえば、削除オブジェクト <bpt id="p1">**</bpt>ProdJournalTable<ept id="p1">**</ept> には、<bpt id="p2">**</bpt>ProdTable<ept id="p2">**</ept> のルールが含まれ、ドライバー テーブルではありません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="109">
          <source>Regardless of how you create these rules, the "where" clause always applies to the driver table.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">これらのルールを作成する方法に関係なく、"where" 句はドライバー テーブルに常に適用されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="110">
          <source>You must understand the effect of your rule on the Purge Object or Archive Object before applying any rule.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">どのようなルールを適用する場合も、適用前にルールの削除オブジェクトまたはアーカイブ オブジェクトへの影響について理解する必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="111">
          <source>On the toolbar, click <bpt id="p1">**</bpt>Add/Edit rules<ept id="p1">**</ept> to open the <bpt id="p2">**</bpt>Add/Edit rules<ept id="p2">**</ept> window.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ツールバーで、<bpt id="p1">**</bpt>ルールの追加/編集<ept id="p1">**</ept>をクリックして、<bpt id="p2">**</bpt>ルールの追加/編集<ept id="p2">**</ept>ウィンドウを開きます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="112">
          <source>Navigation of the Add/Edit rules window</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ルールの追加/編集ウィンドウのナビゲーション</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="113">
          <source>The following tables provide descriptions for the controls in the <bpt id="p1">**</bpt>Add/Edit rules<ept id="p1">**</ept> window.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">次のテーブルで、<bpt id="p1">**</bpt>ルールの追加/編集<ept id="p1">**</ept> ウィンドウのコントロールについて説明します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="114">
          <source>Panes</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ウィンドウ</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="115">
          <source>Pane</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ウィンドウ</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="116">
          <source>Description</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">説明</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="117">
          <source><bpt id="p1">**</bpt>Rule collection<ept id="p1">**</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>ルール コレクション<ept id="p1">**</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="118">
          <source>Contains a list of the rules in the Purge Object or Archive Object, and commands to create a new rule, add an expression to the existing rule, or delete a rule or an expression.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">削除オブジェクトまたはアーカイブ オブジェクト内のルールのリスト、および新しいルールの作成、既存のルールへの式の追加、またはルールまたは式の削除のコマンドが含まれています。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="119">
          <source><bpt id="p1">**</bpt>Configure rules for purge<ept id="p1">**</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>削除のルールのコンフィギュレーション<ept id="p1">**</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="120">
          <source>Provides an area to enter or modify the rule name, description, and conditions.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ルールの名前、説明、および条件を入力または変更する領域を提供します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="121">
          <source>Also provides commands to add the rule to, or update it in, the list in the <bpt id="p1">**</bpt>Rule collection<ept id="p1">**</ept> pane.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">また、<bpt id="p1">**</bpt>ルール コレクション<ept id="p1">**</ept>ウィンドウの一覧に、ルールを追加、または更新するコマンドが提供されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="122">
          <source><bpt id="p1">**</bpt>Conditional information<ept id="p1">**</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>条件付き情報<ept id="p1">**</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="123">
          <source>Lets you specify conditions, or the selection criteria, for the Purge Object.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">削除オブジェクトの条件または選択基準を指定できます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="124">
          <source>Buttons</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ボタン</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="125">
          <source>Add/Edit rules window</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ルール ウィンドウの追加/編集</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="126">
          <source>Button</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ボタン</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="127">
          <source>Description</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">説明</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="128">
          <source><bpt id="p1">**</bpt>Save<ept id="p1">**</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>保存<ept id="p1">**</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="129">
          <source>Save the changes that you made to the list in the <bpt id="p1">**</bpt>Rule collection<ept id="p1">**</ept> pane to the database.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>ルール コレクション<ept id="p1">**</ept> ウィンドウの一覧に対して行った変更をデータベースに保存します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="130">
          <source><bpt id="p1">**</bpt>Close<ept id="p1">**</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>閉じる<ept id="p1">**</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="131">
          <source>Close the <bpt id="p1">**</bpt>Add/Edit rules<ept id="p1">**</ept> window.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>ルールの追加/編集<ept id="p1">**</ept>ウィンドウを閉じます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="132">
          <source>You are prompted to confirm the close or save your changes if you try to close the window without saving your changes.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">変更を保存せずにウィンドウを閉じようとする場合、閉じるか変更を保存するかの確認を求められます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="133">
          <source>Rule collection pane</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ルール コレクション ウィンドウ</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="134">
          <source>Button</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ボタン</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="135">
          <source>Description</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">説明</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="136">
          <source><bpt id="p1">**</bpt>New rule<ept id="p1">**</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>新規作成<ept id="p1">**</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="137">
          <source>Create a new rule.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">新しいルールの作成。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="138">
          <source>When you have multiple rules in the Purge Object or Archive Object, they form the "and" condition in the "where" clause of the SQL statement.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">削除オブジェクトまたはアーカイブ オブジェクトに複数のルールがある場合、それらのルールは、SQL ステートメントの "WHERE" 句の "AND" 条件を形成します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="139">
          <source><bpt id="p1">**</bpt>Add expression<ept id="p1">**</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>式を追加<ept id="p1">**</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="140">
          <source>Create a new expression.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">新しい式を作成します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="141">
          <source>An expression is a condition that is added to an existing rule.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">式は既存のルールに追加される条件です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="142">
          <source>An expression creates an "or" condition in the "where" clause of the SQL statement.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">式は SQL ステートメントの「where」句に「or」の条件を作成します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="143">
          <source><bpt id="p1">**</bpt>Delete<ept id="p1">**</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>削除<ept id="p1">**</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="144">
          <source>Delete the selected rule or expression.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">選択したルールまたは式を削除します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="145">
          <source>Configure rules pane</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ルール ウィンドウのコンフィギュレーション</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="146">
          <source>Button</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ボタン</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="147">
          <source>Description</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">説明</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="148">
          <source><bpt id="p1">**</bpt>Add<ept id="p1">**</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>追加<ept id="p1">**</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="149">
          <source>Add the new rule or expression to the list in the <bpt id="p1">**</bpt>Rule collection<ept id="p1">**</ept> pane.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>ルール コレクション<ept id="p1">**</ept> ウィンドウの一覧に新しいルールまたは式を追加します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="150">
          <source><bpt id="p1">**</bpt>Update<ept id="p1">**</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>更新<ept id="p1">**</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="151">
          <source>Update the selected rule or expression in the list in the <bpt id="p1">**</bpt>Rule collection<ept id="p1">**</ept> pane.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>ルール コレクション<ept id="p1">**</ept> ウィンドウの一覧で選択したルールまたは式を更新します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="152">
          <source><bpt id="p1">**</bpt>Cancel<ept id="p1">**</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>キャンセル<ept id="p1">**</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="153">
          <source>Cancel the add or update action.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">追加、または更新アクションをキャンセルします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="154">
          <source>Fields (across all panes)</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">フィールド (すべてのウィンドウ間)</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="155">
          <source>Field</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">フィールド</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="156">
          <source>Description</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">説明</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="157">
          <source><bpt id="p1">**</bpt>Rule name<ept id="p1">**</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>ルール名<ept id="p1">**</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="158">
          <source>The name of the rule or expression.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ルールまたは式の名前。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="159">
          <source><bpt id="p1">**</bpt>Rule<ept id="p1">**</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>ルール<ept id="p1">**</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="160">
          <source>The condition that you create based on the table name, the field name, and a conditional operator.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">テーブル名、フィールド名、および条件付き演算子に基づいて作成する条件。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="161">
          <source>This condition forms the "where" clause in the SQL statement.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この条件は、SQL ステートメントの「where」句を構成します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="162">
          <source><bpt id="p1">**</bpt>Rule description<ept id="p1">**</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>ルールの説明<ept id="p1">**</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="163">
          <source>A description of the rule.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ルールの説明。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="164">
          <source>Enter a new description or modify an existing description here.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">新しい説明を入力またはここに既存の説明を変更します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="165">
          <source><bpt id="p1">**</bpt>Table name<ept id="p1">**</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>テーブル名<ept id="p1">**</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="166">
          <source>The table that you select from the list of all tables in the Purge Object or Archive Object.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">削除オブジェクトまたはアーカイブ オブジェクトのすべてのテーブルのリストから選択したテーブル。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="167">
          <source><bpt id="p1">**</bpt>Field name<ept id="p1">**</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>フィールド名<ept id="p1">**</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="168">
          <source>The name of the field that you select from the list of all fields for the selected table.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">選択したテーブルのすべてのフィールドのリストから選択するフィールドの名前。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="169">
          <source><bpt id="p1">**</bpt>Condition<ept id="p1">**</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>条件<ept id="p1">**</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="170">
          <source>The condition that you place on the table and the field.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ユーザーがテーブルとフィールドに配置する条件。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="171">
          <source>The condition list changes, depending on the field selections.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">フィールドの選択に応じて、条件リストが変更されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="172">
          <source><bpt id="p1">**</bpt>Value<ept id="p1">**</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>値<ept id="p1">**</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="173">
          <source>The <bpt id="p1">**</bpt>Value<ept id="p1">**</ept> field switches between a text box and a list.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>値<ept id="p1">**</ept> フィールドは、テキスト ボックスとリストを切り替えます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="174">
          <source>You can select a value from the list, but cannot enter a value in the text box here.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">リストから値を選択することができますが、ここではテキスト ボックスに値を入力することができません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="175">
          <source>You enter the value when you create a purge task.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">削除タスクを作成する場合には、値を入力します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="176">
          <source>Walkthrough: Add or modify a rule in a Purge Object</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">チュートリアル: 削除オブジェクトへのルールの追加または削除</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="177">
          <source>This section provides a walkthrough to add or modify a rule in a Purge Object.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このセクションでは、削除オブジェクトのルールを追加または変更するためのチュートリアルを提供します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="178">
          <source><bpt id="p1">**</bpt>Caution<ept id="p1">**</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>注意<ept id="p1">**</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="179">
          <source>This walkthrough deletes and recreates an existing rule from the Purge Object for ease of learning.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このチュートリアルでは、学習を容易にするためにパージ オブジェクトから既存のルールを削除し、再作成します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="180">
          <source>You must have an excellent understanding of the database design, data flow, process flow, and application functionality of the Microsoft Dynamics AX application to work with rules.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ルールを扱うには、データベース設計、データ フロー、プロセス フロー、および Microsoft Dynamics AX アプリケーションの機能について明確に理解している必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="181">
          <source>An error can cause data corruption or application downtime requiring full database and application recovery.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">エラーは完全なデータベースおよびアプリケーションの復旧を必要とするデータの破損やアプリケーションのダウンタイムを引き起こす可能性があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="182">
          <source>Click <bpt id="p1">**</bpt>Configure<ept id="p1">**</ept> <ph id="ph1">&amp;gt;</ph> <bpt id="p2">**</bpt>Purge templates/Purge Object<ept id="p2">**</ept> <ph id="ph2">&amp;gt;</ph> <bpt id="p3">**</bpt>PurchParmTable<ept id="p3">**</ept> to open the <bpt id="p4">**</bpt>PurchParmTable<ept id="p4">**</ept> Purge Object.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>構成<ept id="p1">**</ept> <ph id="ph1">&amp;gt;</ph> <bpt id="p2">**</bpt>削除テンプレート/削除オブジェクト<ept id="p2">**</ept> <ph id="ph2">&amp;gt;</ph> <bpt id="p3">**</bpt>PurchParmTable<ept id="p3">**</ept> とクリックし、<bpt id="p4">**</bpt>PurchParmTable<ept id="p4">**</ept> 削除オブジェクトを開きます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="183">
          <source>This walkthrough assumes that you are working with the Purge Object that was created from the default purge template.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このチュートリアルでは、既定のパージ テンプレートから作成されたパージ オブジェクトを使用して作業することを前提としています。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="184">
          <source>If you have modified the Purge Object in any way, click <bpt id="p1">**</bpt>Restore<ept id="p1">**</ept> to restore the Purge Object to the original version.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">任意の方法で削除オブジェクトを変更した場合は、<bpt id="p1">**</bpt>復元<ept id="p1">**</ept>をクリックして削除オブジェクトを元のバージョンに復元します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="185">
          <source>On the toolbar, click <bpt id="p1">**</bpt>Add/Edit rules<ept id="p1">**</ept> to open the <bpt id="p2">**</bpt>Add/Edit rules<ept id="p2">**</ept> window.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ツールバーで、<bpt id="p1">**</bpt>ルールの追加/編集<ept id="p1">**</ept>をクリックして、<bpt id="p2">**</bpt>ルールの追加/編集<ept id="p2">**</ept>ウィンドウを開きます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="186">
          <source>In the <bpt id="p1">**</bpt>Rule collection<ept id="p1">**</ept> pane, click the first row in the data grid to select the rule <bpt id="p2">**</bpt>PurchParmTable.ParmJobStatus = Executed<ept id="p2">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>ルール コレクション<ept id="p1">**</ept> ウィンドウで、データ グリッドの最初の行をクリックして <bpt id="p2">**</bpt>PurchParmTable.ParmJobStatus = Executed<ept id="p2">**</ept> のルールを選択します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="187">
          <source>Click <bpt id="p1">**</bpt>Delete<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>削除<ept id="p1">**</ept> をクリックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="188">
          <source>Click <bpt id="p1">**</bpt>OK<ept id="p1">**</ept> in the <bpt id="p2">**</bpt>Delete<ept id="p2">**</ept> dialog box.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p2">**</bpt>削除<ept id="p2">**</ept>ダイアログ ボックスで、<bpt id="p1">**</bpt>OK<ept id="p1">**</ept> をクリックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="189">
          <source>Click <bpt id="p1">**</bpt>New rule<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>新しいルール<ept id="p1">**</ept>をクリックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="190">
          <source>In <bpt id="p1">**</bpt>Configure rules for purge<ept id="p1">**</ept>, set the following field values:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>削除のルールを構成<ept id="p1">**</ept>で、次のフィールド値を設定します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="191">
          <source>In the <bpt id="p1">**</bpt>Rule name<ept id="p1">**</ept> field, type Clean up.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>ルール名<ept id="p1">**</ept>フィールドに、「クリーンアップ」と入力します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="192">
          <source>In the <bpt id="p1">**</bpt>Rule description<ept id="p1">**</ept> field, type What should be cleaned up?</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>ルールの説明<ept id="p1">**</ept>フィールドに、「どれをクリーンアップする必要がありますか」と入力します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="193">
          <source>In the <bpt id="p1">**</bpt>Table name<ept id="p1">**</ept> list, select <bpt id="p2">**</bpt>PurchParmTable<ept id="p2">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>テーブル名<ept id="p1">**</ept>リストで、<bpt id="p2">**</bpt>PurchParmTable<ept id="p2">**</ept> を選択します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="194">
          <source>In the <bpt id="p1">**</bpt>Field name<ept id="p1">**</ept> list, select <bpt id="p2">**</bpt>ParmJobStatus<ept id="p2">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>フィールド名<ept id="p1">**</ept>リストで、<bpt id="p2">**</bpt>ParmJobStatus<ept id="p2">**</ept> を選択します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="195">
          <source>In the <bpt id="p1">**</bpt>Condition<ept id="p1">**</ept> list, select <bpt id="p2">**</bpt><ph id="ph1">=</ph><ept id="p2">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>条件<ept id="p1">**</ept>リストで、<bpt id="p2">**</bpt><ph id="ph1">=</ph><ept id="p2">**</ept> を選択します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="196">
          <source>In the <bpt id="p1">**</bpt>Value<ept id="p1">**</ept> field, select <bpt id="p2">**</bpt>Executed<ept id="p2">**</ept> from the list.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>値<ept id="p1">**</ept>フィールドで、リストから<bpt id="p2">**</bpt>実行済<ept id="p2">**</ept>を選択します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="197">
          <source>Click <bpt id="p1">**</bpt>Add<ept id="p1">**</ept>, and verify that the rule is added to the data grid in the <bpt id="p2">**</bpt>Rule collection<ept id="p2">**</ept> pane.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>追加<ept id="p1">**</ept>をクリックし、ルールが<bpt id="p2">**</bpt>ルール コレクション<ept id="p2">**</ept> ウィンドウのデータグリッドに追加されていることを確認します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="198">
          <source>Click <bpt id="p1">**</bpt>Save<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>保存<ept id="p1">**</ept> をクリックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="199">
          <source>In the <bpt id="p1">**</bpt>Rules<ept id="p1">**</ept> dialog box, click <bpt id="p2">**</bpt>OK<ept id="p2">**</ept> to continue.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>ルール<ept id="p1">**</ept> ダイアログ ボックスで <bpt id="p2">**</bpt>OK<ept id="p2">**</ept> をクリックして続行します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="200">
          <source>Click <bpt id="p1">**</bpt>Close<ept id="p1">**</ept> to close the window and return to the Purge Object.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>閉じる<ept id="p1">**</ept>をクリックしてウィンドウを閉じ、削除オブジェクトに戻ります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="201">
          <source>Walkthrough: Add or modify a rule in an Archive Object</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">チュートリアル: アーカイブ オブジェクトへのルールの追加または削除</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="202">
          <source>This section provides a walkthrough to add or modify a rule in an Archive Object.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このセクションでは、アーカイブ オブジェクトのルールを追加または変更するためのチュートリアルを提供します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="203">
          <source>Click <bpt id="p1">**</bpt>Configure<ept id="p1">**</ept> <ph id="ph1">&amp;gt;</ph> <bpt id="p2">**</bpt>Archive templates/Archive Objects<ept id="p2">**</ept> <ph id="ph2">&amp;gt;</ph> <bpt id="p3">**</bpt>SalesTable<ept id="p3">**</ept> to open the <bpt id="p4">**</bpt>SalesTable<ept id="p4">**</ept> Archive Object.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>構成<ept id="p1">**</ept> <ph id="ph1">&amp;gt;</ph> <bpt id="p2">**</bpt>アーカイブ テンプレート/アーカイブ オブジェクト<ept id="p2">**</ept> <ph id="ph2">&amp;gt;</ph> <bpt id="p3">**</bpt>SalesTable<ept id="p3">**</ept> とクリックして <bpt id="p4">**</bpt>SalesTable<ept id="p4">**</ept> アーカイブ オブジェクトを開きます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="204">
          <source>This walkthrough assumes that you are working with the Archive Object that was created from the default archive template.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このチュートリアルでは、既定のアーカイブ テンプレートから作成されたアーカイブ オブジェクトを使用して作業することを前提としています。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="205">
          <source>If you have modified the Archive Object in any way, use the <bpt id="p1">**</bpt>Show versions<ept id="p1">**</ept> command on the toolbar to revert to the original archive template that is included with the Data Management Framework.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">アーカイブ オブジェクトを変更した場合は、ツールバーの<bpt id="p1">**</bpt>バージョンを表示<ept id="p1">**</ept>コマンドを使用して、データ管理フレームワークに含まれている元のアーカイブ テンプレートに戻します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="206">
          <source>On the toolbar, click <bpt id="p1">**</bpt>Add/Edit rules<ept id="p1">**</ept> to open the <bpt id="p2">**</bpt>Add/Edit rules<ept id="p2">**</ept> window.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ツールバーで、<bpt id="p1">**</bpt>ルールの追加/編集<ept id="p1">**</ept>をクリックして、<bpt id="p2">**</bpt>ルールの追加/編集<ept id="p2">**</ept>ウィンドウを開きます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="207">
          <source>In the <bpt id="p1">**</bpt>Rule collection<ept id="p1">**</ept> pane, click the second row in the data grid to select the rule <bpt id="p2">**</bpt>SalesTable.SalesStatus In Canceled, Invoiced<ept id="p2">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>ルール コレクション<ept id="p1">**</ept> ウィンドウで、データ グリッドの 2 行目をクリックして <bpt id="p2">**</bpt>SalesTable.SalesStatus In Canceled, Invoiced<ept id="p2">**</ept> のルールを選択します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="208">
          <source>Click <bpt id="p1">**</bpt>Delete<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>削除<ept id="p1">**</ept> をクリックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="209">
          <source>Click <bpt id="p1">**</bpt>OK<ept id="p1">**</ept> in the <bpt id="p2">**</bpt>Delete<ept id="p2">**</ept> dialog box.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p2">**</bpt>削除<ept id="p2">**</ept>ダイアログ ボックスで、<bpt id="p1">**</bpt>OK<ept id="p1">**</ept> をクリックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="210">
          <source>In the <bpt id="p1">**</bpt>Rule collection<ept id="p1">**</ept> pane, click <bpt id="p2">**</bpt>Add expression<ept id="p2">**</ept>, and set the following field values:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>ルール コレクション<ept id="p1">**</ept>ウィンドウで、<bpt id="p2">**</bpt>拡張機能の追加<ept id="p2">**</ept>をクリックし、次のフィールド値を設定します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="211">
          <source>In the <bpt id="p1">**</bpt>Rule name<ept id="p1">**</ept> field, type Status.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>ルール名<ept id="p1">**</ept>フィールドに、「ステータス」と入力します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="212">
          <source>In the <bpt id="p1">**</bpt>Rule description<ept id="p1">**</ept> field, type Status values considered for archival.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>ルールの説明<ept id="p1">**</ept>フィールドに、アーカイブ用とみなされるステータスの値を入力します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="213">
          <source>In the <bpt id="p1">**</bpt>Conditional information<ept id="p1">**</ept> pane, set the following field values:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>条件付き情報<ept id="p1">**</ept>ウィンドウで、次のフィールド値を設定します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="214">
          <source>In the <bpt id="p1">**</bpt>Table name<ept id="p1">**</ept> list, select <bpt id="p2">**</bpt>SalesTable<ept id="p2">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>テーブル名<ept id="p1">**</ept>リストで、<bpt id="p2">**</bpt>SalesTable<ept id="p2">**</ept> を選択します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="215">
          <source>In the <bpt id="p1">**</bpt>Field name<ept id="p1">**</ept> list, select <bpt id="p2">**</bpt>SalesStatus<ept id="p2">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>フィールド名<ept id="p1">**</ept>リストで、<bpt id="p2">**</bpt>SalesStatus<ept id="p2">**</ept> を選択します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="216">
          <source>In the <bpt id="p1">**</bpt>Condition<ept id="p1">**</ept> list, select <bpt id="p2">**</bpt>In<ept id="p2">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>条件<ept id="p1">**</ept>リストで、<bpt id="p2">**</bpt>In<ept id="p2">**</ept> を選択します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="217">
          <source>In the <bpt id="p1">**</bpt>Value<ept id="p1">**</ept> field, select <bpt id="p2">**</bpt>Cancelled and Invoiced<ept id="p2">**</ept> from the list.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>値<ept id="p1">**</ept>フィールドで、リストから<bpt id="p2">**</bpt>キャンセル済および請求済<ept id="p2">**</ept>を選択します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="218">
          <source>Click <bpt id="p1">**</bpt>Add<ept id="p1">**</ept>, and verify that the rule is added to the data grid in the <bpt id="p2">**</bpt>Rule collection<ept id="p2">**</ept> pane.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>追加<ept id="p1">**</ept>をクリックし、ルールが<bpt id="p2">**</bpt>ルール コレクション<ept id="p2">**</ept> ウィンドウのデータグリッドに追加されていることを確認します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="219">
          <source>Click <bpt id="p1">**</bpt>Save<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>保存<ept id="p1">**</ept> をクリックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="220">
          <source>In the <bpt id="p1">**</bpt>Rules<ept id="p1">**</ept> dialog box, click <bpt id="p2">**</bpt>OK<ept id="p2">**</ept> to continue.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>ルール<ept id="p1">**</ept> ダイアログ ボックスで <bpt id="p2">**</bpt>OK<ept id="p2">**</ept> をクリックして続行します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="221">
          <source>Click <bpt id="p1">**</bpt>Close<ept id="p1">**</ept> to close the window and return to the Archive Object.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>閉じる<ept id="p1">**</ept>をクリックしてウィンドウを閉じ、アーカイブ オブジェクトに戻ります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="222">
          <source>Add relations</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">リレーションの追加</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="223">
          <source>This command lets you manually add a table to the Purge Object or Archive Object, and establish a relationship.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このコマンドを使用すると、削除オブジェクトまたはアーカイブ オブジェクトに手動でテーブルを追加し、関係を確立できます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="224">
          <source>You may have to manually add a relationship if you have custom tables in the Microsoft Dynamics AX application without a metadata relationship in the Application Object Tree (AOT).</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Microsoft Dynamics AX アプリケーションにアプリケーション オブジェクト ツリー (AOT) のメタデータ リレーションシップなしのカスタム テーブルがある場合、リレーションシップの手動の追加が必要な場合があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="225">
          <source>To add a relation, select a table by clicking it in the relationship tree diagram.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">リレーションを追加するには、リレーションシップ ツリー ダイアグラムでテーブルをクリックして選択します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="226">
          <source>The table you select becomes the parent table, and the table you add becomes the child in the relationship.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">選択したテーブルが親テーブルになり、追加するテーブルがリレーションシップの子になります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="227">
          <source>On the toolbar, click <bpt id="p1">**</bpt>Add relations<ept id="p1">**</ept> to open the <bpt id="p2">**</bpt>Add relations<ept id="p2">**</ept> window.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ツールバーで、<bpt id="p1">**</bpt>関係を追加<ept id="p1">**</ept>をクリックして、<bpt id="p2">**</bpt>関係を追加<ept id="p2">**</ept>ウィンドウを開きます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="228">
          <source>Navigation of the Add relations window</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">関係の追加ウィンドウのナビゲーション</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="229">
          <source>The following tables provide descriptions for the controls in the <bpt id="p1">**</bpt>Add relations<ept id="p1">**</ept> window.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">次のテーブルで、<bpt id="p1">**</bpt>関係の追加<ept id="p1">**</ept> ウィンドウのコントロールについて説明します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="230">
          <source>Panes</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ウィンドウ</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="231">
          <source>Pane</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ウィンドウ</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="232">
          <source>Description</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">説明</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="233">
          <source><bpt id="p1">**</bpt>Relationships<ept id="p1">**</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>関係<ept id="p1">**</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="234">
          <source>Provides a list of relations that you created in the Purge Object or Archive Object.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">削除オブジェクトまたはアーカイブ オブジェクトで作成した関係の一覧を提供します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="235">
          <source>Also provides commands to create a new relation or delete an existing relation.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">また、新しい関係を作成するコマンドや、既存の関係を削除するコマンドも提供します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="236">
          <source><bpt id="p1">**</bpt>Configure relations<ept id="p1">**</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>関係のコンフィギュレーション<ept id="p1">**</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="237">
          <source>Provides an area to enter or modify the relation name, description, and conditions.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">関係の名前、説明、および条件を入力または変更する領域を提供します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="238">
          <source>Also provides commands to add the relation to, or update it in, the list in the <bpt id="p1">**</bpt>Relationships<ept id="p1">**</ept> pane, or to cancel the add or update action.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">また、<bpt id="p1">**</bpt>リレーションシップ<ept id="p1">**</ept>ウィンドウの一覧にリレーションの追加、一覧内での更新や、追加または更新アクションをキャンセルしたりするためのコマンドも用意されています。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="239">
          <source>Buttons</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ボタン</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="240">
          <source>Button</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ボタン</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="241">
          <source>Description</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">説明</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="242">
          <source><bpt id="p1">**</bpt>Save<ept id="p1">**</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>保存<ept id="p1">**</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="243">
          <source>Save the changes that you made to the list in the <bpt id="p1">**</bpt>Relationships<ept id="p1">**</ept> pane to the database.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>関係<ept id="p1">**</ept> ウィンドウの一覧に対して行った変更をデータベースに保存します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="244">
          <source><bpt id="p1">**</bpt>Close<ept id="p1">**</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>閉じる<ept id="p1">**</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="245">
          <source>Close the <bpt id="p1">**</bpt>Add relations<ept id="p1">**</ept> window.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>関係の追加<ept id="p1">**</ept>ウィンドウを閉じます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="246">
          <source>If you try to close the window without saving your changes, you are prompted to confirm the close or save your changes.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">変更を保存せずにウィンドウを閉じようとする場合、閉じることを確認するメッセージまたは変更の保存を求めるメッセージが表示されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="247">
          <source>Relationships pane</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">リレーションシップ ウィンドウ</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="248">
          <source>Button</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ボタン</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="249">
          <source>Description</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">説明</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="250">
          <source><bpt id="p1">**</bpt>New relation<ept id="p1">**</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>新しい関係<ept id="p1">**</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="251">
          <source>Create a new relation, or a new condition for an existing relation.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">新しいリレーションを作成するか、既存のリレーションの新しい条件を作成します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="252">
          <source><bpt id="p1">**</bpt>Delete<ept id="p1">**</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>削除<ept id="p1">**</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="253">
          <source>Delete the selected relation or condition.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">選択した関係または条件を削除します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="254">
          <source>You cannot modify added relations.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">追加の関係を変更することはできません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="255">
          <source>You must delete the relations, and then add them again to make any changes.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">関係を削除してから、変更を加えるために、関係を再度追加する必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="256">
          <source>Configure relations pane</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">関係ウィンドウのコンフィギュレーション</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="257">
          <source>Button</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ボタン</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="258">
          <source>Description</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">説明</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="259">
          <source><bpt id="p1">**</bpt>Add<ept id="p1">**</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>追加<ept id="p1">**</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="260">
          <source>Add a new relation or condition to the list in the <bpt id="p1">**</bpt>Relationships<ept id="p1">**</ept> pane.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>リレーションシップ<ept id="p1">**</ept> ウィンドウのリストに新しい関係または条件を追加します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="261">
          <source><bpt id="p1">**</bpt>Update<ept id="p1">**</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>更新<ept id="p1">**</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="262">
          <source>Update the selected relation or condition in the list in the <bpt id="p1">**</bpt>Relationships<ept id="p1">**</ept> pane.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>リレーションシップ<ept id="p1">**</ept> ウィンドウの一覧で選択したリレーションまたは条件を更新します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="263">
          <source><bpt id="p1">**</bpt>Cancel<ept id="p1">**</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>キャンセル<ept id="p1">**</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="264">
          <source>Cancel an add or update action.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">追加または更新アクションをキャンセルします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="265">
          <source>Fields</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">フィールド</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="266">
          <source>Field</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">フィールド</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="267">
          <source>Description</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">説明</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="268">
          <source><bpt id="p1">**</bpt>Include child relations<ept id="p1">**</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>子関係を含める<ept id="p1">**</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="269">
          <source>Select this field if you have to add all the child entities of the relation that you are adding to the relationship tree.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">関係ツリーに追加する関係のすべての子エンティティを追加する必要がある場合は、このフィールドを選択します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="270">
          <source>If you clear the field, the child entities of the table you are adding are not added to the Purge Object or Archive Object.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このフィールドをクリアにすると、追加するテーブルの子エンティティは削除オブジェクトまたはアーカイブ オブジェクトに追加されません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="271">
          <source>Relationships pane</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">リレーションシップ ウィンドウ</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="272">
          <source>Field</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">フィールド</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="273">
          <source>Description</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">説明</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="274">
          <source><bpt id="p1">**</bpt>RelationsDefined<ept id="p1">**</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>RelationsDefined<ept id="p1">**</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="275">
          <source>A list of the relations in the Purge Object or Archive Object, and the conditions for each relation.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">削除オブジェクトまたはアーカイブ オブジェクトの関係、および各関係の条件の一覧。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="276">
          <source>This field becomes available in the list when you add a relation.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このフィールドは、リレーションを追加するときにリスト内で使用可能になります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="277">
          <source>Configure relations pane, Table relations area</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">関係ウィンドウのコンフィギュレーション、テーブル リレーション領域</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="278">
          <source>Field</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">フィールド</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="279">
          <source>Description</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">説明</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="280">
          <source><bpt id="p1">**</bpt>Relation name<ept id="p1">**</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>関係名<ept id="p1">**</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="281">
          <source>The name of the relation.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">リレーションの名前。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="282">
          <source>You must enter a relation name to continue.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">続行するリレーション名を入力する必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="283">
          <source><bpt id="p1">**</bpt>Table name<ept id="p1">**</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>テーブル名<ept id="p1">**</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="284">
          <source>The table that you selected in the Purge Object or Archive Object.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">削除オブジェクトまたはアーカイブ オブジェクトで選択したテーブル。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="285">
          <source>You can't change this value in the window.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ウィンドウのこの値を変更することはできません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="286">
          <source>This table is the parent entity in the relationship.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このテーブルは、リレーションシップ内の親エンティティです。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="287">
          <source><bpt id="p1">**</bpt>Field name<ept id="p1">**</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>フィールド名<ept id="p1">**</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="288">
          <source>Select the field that you want to use in the relationship.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">関係で使用するフィールドを選択します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="289">
          <source><bpt id="p1">**</bpt>Condition<ept id="p1">**</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>条件<ept id="p1">**</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="290">
          <source>By default, the condition is <bpt id="p1">**</bpt><ph id="ph1">=</ph><ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">既定では、条件は <bpt id="p1">**</bpt><ph id="ph1">=</ph><ept id="p1">**</ept> です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="291">
          <source>You cannot change the condition.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">条件は変更できません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="292">
          <source><bpt id="p1">**</bpt>Related table name<ept id="p1">**</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>関連テーブル名<ept id="p1">**</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="293">
          <source>Select the table that you are adding from the list.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">一覧から追加するテーブルを選択します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="294">
          <source>This table is the child entity in the relationship.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このテーブルは、リレーションシップ内の子エンティティです。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="295">
          <source><bpt id="p1">**</bpt>Related field name<ept id="p1">**</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>関連フィールド名<ept id="p1">**</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="296">
          <source>Select the field that you want to use in the relationship.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">関係で使用するフィールドを選択します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="297">
          <source>Configure relations pane, Conditional information area</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">関係ウィンドウのコンフィギュレーション、条件付情報エリア</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="298">
          <source>Field</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">フィールド</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="299">
          <source>Description</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">説明</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="300">
          <source><bpt id="p1">**</bpt>Table name<ept id="p1">**</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>テーブル名<ept id="p1">**</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="301">
          <source>Select a table from the list.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">一覧からテーブルを選択します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="302">
          <source>You can select either the parent or the child from the relationship.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">リレーションシップから親または子のいずれかを選択することができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="303">
          <source><bpt id="p1">**</bpt>Field name<ept id="p1">**</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>フィールド名<ept id="p1">**</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="304">
          <source>Select the field that you want to use in the condition.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">条件で使用するフィールドを選択します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="305">
          <source><bpt id="p1">**</bpt>Condition<ept id="p1">**</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>条件<ept id="p1">**</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="306">
          <source>Select the condition that you want to use.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">使用する条件を選択します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="307">
          <source><bpt id="p1">**</bpt>Value<ept id="p1">**</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>値<ept id="p1">**</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="308">
          <source>Enter the value for the condition.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">条件の値を入力します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="309">
          <source>Walkthrough: Add a relation in a Purge Object</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">チュートリアル: 削除オブジェクトへのリレーションの追加</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="310">
          <source>This section provides a walkthrough to add a relation in a Purge Object.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このセクションでは、削除オブジェクトにリレーションを追加するためのチュートリアルを提供します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="311">
          <source>Click <bpt id="p1">**</bpt>Configure<ept id="p1">**</ept> <ph id="ph1">&amp;gt;</ph> <bpt id="p2">**</bpt>Purge templates/Purge Objects<ept id="p2">**</ept>, and then select <bpt id="p3">**</bpt>ProjJournalTable<ept id="p3">**</ept> from the drop-down list.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>構成<ept id="p1">**</ept> <ph id="ph1">&amp;gt;</ph> <bpt id="p2">**</bpt>削除テンプレート/削除オブジェクト<ept id="p2">**</ept>とクリックして、ドロップダウン リストから <bpt id="p3">**</bpt>ProjJournalTable<ept id="p3">**</ept> を選択します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="312">
          <source>In the Purge Object, click the <bpt id="p1">**</bpt>ProjJournalTable<ept id="p1">**</ept> table in level 0, and then click <bpt id="p2">**</bpt>Add relations<ept id="p2">**</ept> on the toolbar.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">削除オブジェクトで、レベル 0 の <bpt id="p1">**</bpt>ProjJournalTable<ept id="p1">**</ept> テーブルをクリックしてから、ツール バーで<bpt id="p2">**</bpt>関係の追加<ept id="p2">**</ept>をクリックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="313">
          <source>In the <bpt id="p1">**</bpt>Add relations<ept id="p1">**</ept> dialog box, click <bpt id="p2">**</bpt>New relation<ept id="p2">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>関係の追加<ept id="p1">**</ept>ダイアログ ボックスで、<bpt id="p2">**</bpt>新しい関係<ept id="p2">**</ept>をクリックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="314">
          <source>In the <bpt id="p1">**</bpt>Relation name<ept id="p1">**</ept> field, enter a valid name for the relation.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>関係名<ept id="p1">**</ept>フィールドに、関係に対する有効な名前を入力します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="315">
          <source>In the <bpt id="p1">**</bpt>Table relations<ept id="p1">**</ept> area, follow these steps to add the relation:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>テーブル リレーション<ept id="p1">**</ept>領域で、これらの手順に従って関係を追加します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="316">
          <source>From <bpt id="p1">**</bpt>Field name<ept id="p1">**</ept> list, select <bpt id="p2">**</bpt>JournalId<ept id="p2">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>フィールド名<ept id="p1">**</ept>の一覧から、<bpt id="p2">**</bpt>JournalId<ept id="p2">**</ept> を選択します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="317">
          <source>From the <bpt id="p1">**</bpt>Related table<ept id="p1">**</ept> name list, select <bpt id="p2">**</bpt>JournalError<ept id="p2">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>関連テーブル<ept id="p1">**</ept>の名前リストから <bpt id="p2">**</bpt>JournalError<ept id="p2">**</ept> を選択します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="318">
          <source>From the <bpt id="p1">**</bpt>Related field name<ept id="p1">**</ept> list, select <bpt id="p2">**</bpt>JournalId<ept id="p2">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>関連フィールド名<ept id="p1">**</ept>リストから <bpt id="p2">**</bpt>JournalId<ept id="p2">**</ept> を選択します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="319">
          <source>Click <bpt id="p1">**</bpt>Add<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>追加<ept id="p1">**</ept> をクリックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="320">
          <source>In the <bpt id="p1">**</bpt>Add Relations<ept id="p1">**</ept> dialog box, click <bpt id="p2">**</bpt>New relation<ept id="p2">**</ept> to add a condition to the relation you just added.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>関係の追加<ept id="p1">**</ept>ダイアログ ボックスで、<bpt id="p2">**</bpt>新しい関係<ept id="p2">**</ept>をクリックして、今追加した関係に対する条件を追加します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="321">
          <source>In the <bpt id="p1">**</bpt>Conditional information<ept id="p1">**</ept> area, follow these steps to add a condition:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>条件付き情報<ept id="p1">**</ept>領域で、これらの手順に従って条件を追加します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="322">
          <source>From the <bpt id="p1">**</bpt>Table name<ept id="p1">**</ept> list, select a table that you want to use in the condition.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>テーブル名<ept id="p1">**</ept>リストから条件で使用するテーブルを選択します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="323">
          <source>From the <bpt id="p1">**</bpt>Field name<ept id="p1">**</ept> list, select the field that you want to use in the condition.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>フィールド名<ept id="p1">**</ept>リストから条件で使用するフィールドを選択します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="324">
          <source>From the <bpt id="p1">**</bpt>Condition<ept id="p1">**</ept> list, select the condition.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>条件<ept id="p1">**</ept>リストから、条件を選択します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="325">
          <source>From the <bpt id="p1">**</bpt>Value<ept id="p1">**</ept> list, select the value.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>値<ept id="p1">**</ept>リストから値を選択します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="326">
          <source>Click <bpt id="p1">**</bpt>Add<ept id="p1">**</ept> to add the condition to the data grid.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">条件をデータ グリッドに追加するには、<bpt id="p1">**</bpt>追加<ept id="p1">**</ept>をクリックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="327">
          <source>Click <bpt id="p1">**</bpt>Save<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>保存<ept id="p1">**</ept> をクリックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="328">
          <source>Click <bpt id="p1">**</bpt>OK<ept id="p1">**</ept> to continue.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>OK<ept id="p1">**</ept> をクリックして続行します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="329">
          <source>In the Purge Object, verify that the JournalError table you just added is shown as a child entity in level 1.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">削除オブジェクトで、追加した JournalError テーブルがレベル 1 の子エンティティで表示されていることを確認します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="330">
          <source>Save the Purge Object.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">削除オブジェクトを保存します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="331">
          <source>Walkthrough: Add a relation in an Archive Object</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">チュートリアル: アーカイブ オブジェクトへのリレーションの追加</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="332">
          <source>Click <bpt id="p1">**</bpt>Configure<ept id="p1">**</ept> <ph id="ph1">&amp;gt;</ph> <bpt id="p2">**</bpt>Archive templates/Archive Objects<ept id="p2">**</ept>, and then select <bpt id="p3">**</bpt>SalesTable<ept id="p3">**</ept> from the drop-down list.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>構成<ept id="p1">**</ept> <ph id="ph1">&amp;gt;</ph> <bpt id="p2">**</bpt>アーカイブ テンプレート/アーカイブ オブジェクト<ept id="p2">**</ept>とクリックして、ドロップダウン リストから <bpt id="p3">**</bpt>SalesTable<ept id="p3">**</ept> を選択します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="333">
          <source>In the Archive Object, click the <bpt id="p1">**</bpt>DocuRef<ept id="p1">**</ept> table in level 1, and then click <bpt id="p2">**</bpt>Add relations<ept id="p2">**</ept> on the toolbar.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">アーカイブ オブジェクトで、レベル 1 の <bpt id="p1">**</bpt>DocuRef<ept id="p1">**</ept> テーブルをクリックしてから、ツール バーで<bpt id="p2">**</bpt>関係の追加<ept id="p2">**</ept>をクリックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="334">
          <source>In the <bpt id="p1">**</bpt>Add relations<ept id="p1">**</ept> dialog box, click <bpt id="p2">**</bpt>New relation<ept id="p2">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>関係の追加<ept id="p1">**</ept>ダイアログ ボックスで、<bpt id="p2">**</bpt>新しい関係<ept id="p2">**</ept>をクリックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="335">
          <source>In the <bpt id="p1">**</bpt>Relation name<ept id="p1">**</ept> field, enter a valid name for the relation.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>関係名<ept id="p1">**</ept>フィールドに、関係に対する有効な名前を入力します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="336">
          <source>In the <bpt id="p1">**</bpt>Table relations<ept id="p1">**</ept> area, follow these steps to add the relation.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>テーブル リレーション<ept id="p1">**</ept>領域で、これらの手順に従って関係を追加します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="337">
          <source>From the <bpt id="p1">**</bpt>Field name<ept id="p1">**</ept> list, select <bpt id="p2">**</bpt>ValueRecId<ept id="p2">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>フィールド名<ept id="p1">**</ept>リストから <bpt id="p2">**</bpt>ValueRecId<ept id="p2">**</ept> を選択します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="338">
          <source>From the <bpt id="p1">**</bpt>Related table name<ept id="p1">**</ept> list, select <bpt id="p2">**</bpt>DocuValue<ept id="p2">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>関連テーブル名<ept id="p1">**</ept>リストから <bpt id="p2">**</bpt>DocuValue<ept id="p2">**</ept> を選択します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="339">
          <source>From the <bpt id="p1">**</bpt>Related field name<ept id="p1">**</ept> list, select <bpt id="p2">**</bpt>RecId<ept id="p2">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>関連フィールド名<ept id="p1">**</ept>リストから <bpt id="p2">**</bpt>RecId<ept id="p2">**</ept> を選択します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="340">
          <source>Click <bpt id="p1">**</bpt>Add<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>追加<ept id="p1">**</ept> をクリックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="341">
          <source>In the <bpt id="p1">**</bpt>Add Relations<ept id="p1">**</ept> dialog box, click <bpt id="p2">**</bpt>New relation<ept id="p2">**</ept> to add a condition to the relation you just added.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>関係の追加<ept id="p1">**</ept>ダイアログ ボックスで、<bpt id="p2">**</bpt>新しい関係<ept id="p2">**</ept>をクリックして、今追加した関係に対する条件を追加します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="342">
          <source>In the Conditional <bpt id="p1">**</bpt>information<ept id="p1">**</ept> area, follow these steps to add a condition:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">条件付き<bpt id="p1">**</bpt>情報<ept id="p1">**</ept>領域で、これらの手順に従って条件を追加します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="343">
          <source>From the <bpt id="p1">**</bpt>Table name<ept id="p1">**</ept> list, select a table that you want to use in the condition.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>テーブル名<ept id="p1">**</ept>リストから条件で使用するテーブルを選択します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="344">
          <source>From the <bpt id="p1">**</bpt>Field name<ept id="p1">**</ept> list, select the field that you want to use in the condition.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>フィールド名<ept id="p1">**</ept>リストから条件で使用するフィールドを選択します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="345">
          <source>From the <bpt id="p1">**</bpt>Condition<ept id="p1">**</ept> list, select the condition.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>条件<ept id="p1">**</ept>リストから、条件を選択します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="346">
          <source>From the <bpt id="p1">**</bpt>Value<ept id="p1">**</ept> list, select the value.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>値<ept id="p1">**</ept>リストから値を選択します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="347">
          <source>Click <bpt id="p1">**</bpt>Add<ept id="p1">**</ept> to add the condition to the data grid.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">条件をデータ グリッドに追加するには、<bpt id="p1">**</bpt>追加<ept id="p1">**</ept>をクリックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="348">
          <source>Click <bpt id="p1">**</bpt>Save<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>保存<ept id="p1">**</ept> をクリックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="349">
          <source>Click <bpt id="p1">**</bpt>OK<ept id="p1">**</ept> to continue.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>OK<ept id="p1">**</ept> をクリックして続行します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="350">
          <source>In the Archive Object, verify that the <bpt id="p1">**</bpt>DocuValue<ept id="p1">**</ept> table you just added is shown as a child entity in level 1.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">アーカイブ オブジェクトで、追加した <bpt id="p1">**</bpt>DocuValue<ept id="p1">**</ept> テーブルがレベル 1 の子エンティティで表示されていることを確認します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="351">
          <source>Save the Archive Object.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">アーカイブ オブジェクトを保存します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="352">
          <source>Export</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">輸出</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="353">
          <source>This command lets you export a Purge Object or an Archive Object to a file in XML format.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このコマンドを使用すると、削除オブジェクトまたはアーカイブ オブジェクトを XML 形式のファイルにエクスポートできます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="354">
          <source>Follow these steps to export a Purge Object:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">削除オブジェクトをエクスポートするには、これらの手順に従います。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="355">
          <source>Click <bpt id="p1">**</bpt>Configure<ept id="p1">**</ept> <ph id="ph1">&amp;gt;</ph> <bpt id="p2">**</bpt>Purge template/Purge Objects<ept id="p2">**</ept>, and then select <bpt id="p3">**</bpt>PurchParmTable<ept id="p3">**</ept> from the list.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>構成<ept id="p1">**</ept> <ph id="ph1">&amp;gt;</ph> <bpt id="p2">**</bpt>削除テンプレート/削除オブジェクト<ept id="p2">**</ept>とクリックして、リストから <bpt id="p3">**</bpt>PurchParmTable<ept id="p3">**</ept> を選択します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="356">
          <source>On the toolbar, click <bpt id="p1">**</bpt>Export<ept id="p1">**</ept> to open the <bpt id="p2">**</bpt>Export Object<ept id="p2">**</ept> dialog box.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ツールで、<bpt id="p1">**</bpt>エクスポート<ept id="p1">**</ept>をクリックして、<bpt id="p2">**</bpt>エクスポート オブジェクト<ept id="p2">**</ept>ダイアログ ボックスを開きます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="357">
          <source>By default, the file name is the driver table, which is <bpt id="p1">**</bpt>PurchParmTable<ept id="p1">**</ept> in this case.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">既定では、ファイル名はドライバー テーブルで、この場合は <bpt id="p1">**</bpt>PurchParmTable<ept id="p1">**</ept> です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="358">
          <source>Navigate to a location, and then click <bpt id="p1">**</bpt>Save<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">場所に移動してから、<bpt id="p1">**</bpt>保存<ept id="p1">**</ept>をクリックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="359">
          <source>Click <bpt id="p1">**</bpt>OK<ept id="p1">**</ept> to continue.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>OK<ept id="p1">**</ept> をクリックして続行します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="360">
          <source>Locate the saved file, and open it in a Web browser.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">保存されたファイルを検索し、Web ブラウザーで開きます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="361">
          <source>Review the file to understand the schema and its relationship to the graphical representation of the Purge Object.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">スキーマと、削除オブジェクトのグラフィカル表示とのその関係を理解するファイルを確認します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="362">
          <source><bpt id="p1">**</bpt>Note:<ept id="p1">**</ept> You can take similar steps to export an Archive Object.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>注記:<ept id="p1">**</ept> 同様の手順でアーカイブ オブジェクトをエクスポートできます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="363">
          <source><bpt id="p1">**</bpt>Note:<ept id="p1">**</ept> On the toolbar, the <bpt id="p2">**</bpt>Import<ept id="p2">**</ept> command appears before the <bpt id="p3">**</bpt>Export<ept id="p3">**</ept> command.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>注記:<ept id="p1">**</ept> ツールバーの<bpt id="p2">**</bpt>インポート<ept id="p2">**</ept>コマンドは、<bpt id="p3">**</bpt>エクスポート<ept id="p3">**</ept>コマンドの前に表示されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="364">
          <source>Import</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">インポート元</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="365">
          <source>This command lets you import a Purge Object or an Archive Object in XML format.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このコマンドを使用すると、削除オブジェクトまたはアーカイブ オブジェクトを XML 形式でインポートできます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="366">
          <source>The following walkthrough provides hands-on instruction to reinstate a modified Purge Object to the state it was in at the time of export:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">次のチュートリアルでは、変更されたパージ オブジェクトをエクスポート時の状態に復帰させる実践的な指示が提供されています。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="367">
          <source>Click <bpt id="p1">**</bpt>Configure<ept id="p1">**</ept> <ph id="ph1">&amp;gt;</ph> <bpt id="p2">**</bpt>Purge template/Purge Objects<ept id="p2">**</ept>, and then select <bpt id="p3">**</bpt>PurchParmTable<ept id="p3">**</ept> from the drop-down list.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>構成<ept id="p1">**</ept> <ph id="ph1">&amp;gt;</ph> <bpt id="p2">**</bpt>削除テンプレート/削除オブジェクト<ept id="p2">**</ept>とクリックして、ドロップダウン リストから <bpt id="p3">**</bpt>PurchParmTable<ept id="p3">**</ept> を選択します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="368">
          <source>Use the <bpt id="p1">**</bpt>Advanced<ept id="p1">**</ept> filter to filter the data grid in the <bpt id="p2">**</bpt>Remove table<ept id="p2">**</ept> pane so that it shows only tables in level 1.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>詳細<ept id="p1">**</ept> フィルターを使用して、<bpt id="p2">**</bpt>テーブル削除<ept id="p2">**</ept> ウィンドウでデータ グリッドをフィルター処理し、レベル 1 のテーブルのみを表示します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="369">
          <source>Select all tables in the data grid, and then click <bpt id="p1">**</bpt>Remove<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">データ グリッドですべてのテーブルを選択し、<bpt id="p1">**</bpt>削除<ept id="p1">**</ept> をクリックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="370">
          <source>Confirm that the relationship tree contains only <bpt id="p1">**</bpt>PurchParmTable<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">リレーションシップ ツリーに <bpt id="p1">**</bpt>PurchParmTable<ept id="p1">**</ept> のみが含まれていることを確認します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="371">
          <source>On the toolbar, click <bpt id="p1">**</bpt>Save<ept id="p1">**</ept> to save the Purge Object.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ツール バーで、<bpt id="p1">**</bpt>保存<ept id="p1">**</ept>をクリックして削除オブジェクトを保存します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="372">
          <source>Respond to the prompt, and overwrite the object.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">プロンプトに応答し、オブジェクトを上書きします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="373">
          <source>On the toolbar, click <bpt id="p1">**</bpt>Import<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ツール バーで、<bpt id="p1">**</bpt>インポート<ept id="p1">**</ept>をクリックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="374">
          <source>In the <bpt id="p1">**</bpt>Select a valid XML file<ept id="p1">**</ept> dialog box, navigate to the location of the file from the previous section, and then click <bpt id="p2">**</bpt>Open<ept id="p2">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>有効な XML ファイルを選択<ept id="p1">**</ept>ダイアログ ボックスで、前のセクションからファイルの場所に移動してから<bpt id="p2">**</bpt>開く<ept id="p2">**</ept>をクリックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="375">
          <source>Click <bpt id="p1">**</bpt>OK<ept id="p1">**</ept> to continue.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>OK<ept id="p1">**</ept> をクリックして続行します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="376">
          <source>The Purge Object is now in the same state it was in when you exported it in the previous section.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">削除オブジェクトは、前のセクションでエクスポートしたときと同じ状態になりました。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="377">
          <source><bpt id="p1">**</bpt>Note:<ept id="p1">**</ept> You can take similar steps to import an Archive Object.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>注記:<ept id="p1">**</ept> 同様の手順でアーカイブ オブジェクトをインポートできます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="378">
          <source>Save</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">保存</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="379">
          <source>This command lets you save a Purge Object, or save a newer version of an Archive Object.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このコマンドを使用すると、削除オブジェクトを保存したり、新しいバージョンのアーカイブ オブジェクトを保存できます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="380">
          <source>You must save a purge template as a Purge Object before you can use it in a purge task.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">削除タスクで使用する前に削除オブジェクトとして削除テンプレートを保存する必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="381">
          <source>You must save an archive template as an Archive Object before you can use it in an archive task.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">アーカイブ タスクで使用する前に、アーカイブ オブジェクトとしてアーカイブ テンプレートを保存する必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="382">
          <source>The archive function does not let you overwrite an existing Archive Object.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">アーカイブ機能では、既存のアーカイブ オブジェクトを上書きすることはできません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="383">
          <source>When you save an archive template or an Archive Object, you always create a new version of the Archive Object.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">アーカイブ テンプレートまたはアーカイブ オブジェクトを保存するときは、アーカイブ オブジェクトの新しいバージョンをかならず作成してください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="384">
          <source>The archive task always uses the most recent version of the Archive Object you save.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">アーカイブ タスクは常に、保存しているアーカイブ オブジェクトの最新のバージョンを使用します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="385">
          <source>Working with different versions of Archive Objects is covered in a later section of this topic.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">異なるバージョンのアーカイブ オブジェクトの作業については、このトピックの後半で説明されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="386">
          <source>Show versions</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">バージョンの表示</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="387">
          <source>This command lets you work with different versions of an Archive Object.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このコマンドを使用すると、さまざまなバージョンのアーカイブ オブジェクトで作業できます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="388">
          <source>Use the following walkthrough to understand this functionality:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この機能を理解するのにには、次のチュートリアルを使用します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="389">
          <source>Click <bpt id="p1">**</bpt>Configure<ept id="p1">**</ept> <ph id="ph1">&amp;gt;</ph> <bpt id="p2">**</bpt>Archive templates/Archive Object<ept id="p2">**</ept> <ph id="ph2">&amp;gt;</ph> <bpt id="p3">**</bpt>BankDeposit<ept id="p3">**</ept> to open the <bpt id="p4">**</bpt>BankDeposit<ept id="p4">**</ept> Archive Object.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>構成<ept id="p1">**</ept> <ph id="ph1">&amp;gt;</ph> <bpt id="p2">**</bpt>アーカイブ テンプレート/アーカイブ オブジェクト<ept id="p2">**</ept> <ph id="ph2">&amp;gt;</ph> <bpt id="p3">**</bpt>BankDeposit<ept id="p3">**</ept> とクリックして <bpt id="p4">**</bpt>BankDeposit<ept id="p4">**</ept> アーカイブ オブジェクトを開きます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="390">
          <source>Review the Archive Object to make sure that the relationship hierarchy, tables, and rules that are contained in this Archive Object apply to your Microsoft Dynamics AX implementation.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このアーカイブ オブジェクトに含まれるリレーションシップの階層構造、テーブル、およびルールが、Microsoft Dynamics AX の実装に適用されることを確認するアーカイブ オブジェクトを確認します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="391">
          <source>On the toolbar, click <bpt id="p1">**</bpt>Save<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ツール バーの <bpt id="p1">**</bpt>保存<ept id="p1">**</ept> をクリックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="392">
          <source>In the <bpt id="p1">**</bpt>Save as<ept id="p1">**</ept> dialog box, enter a name for the Archive Object.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>名前を付けて保存<ept id="p1">**</ept>ダイアログ ボックスで、アーカイブ オブジェクトの名前を入力します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="393">
          <source>You must provide a new name for this version of the Archive Object.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このバージョンの Archive Object に、新しく名前を指定する必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="394">
          <source>If the name that you provide is already used by a different version of the Archive Object, you receive an error message.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">入力した名前が既にアーカイブ オブジェクトの別のバージョンで使用されている場合、エラー メッセージが表示されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="395">
          <source>Enter BankDeposit<ph id="ph1">\_</ph>1, and then click <bpt id="p1">**</bpt>Save<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">BankDeposit<ph id="ph1">\_</ph>1 と入力し、<bpt id="p1">**</bpt>保存<ept id="p1">**</ept>をクリックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="396">
          <source>Click <bpt id="p1">**</bpt>OK<ept id="p1">**</ept> to continue.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>OK<ept id="p1">**</ept> をクリックして続行します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="397">
          <source>On the toolbar, click <bpt id="p1">**</bpt>Show versions<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ツール バーで、<bpt id="p1">**</bpt>バージョンの表示<ept id="p1">**</ept>をクリックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="398">
          <source>In the <bpt id="p1">**</bpt>Version history<ept id="p1">**</ept> dialog box, select <bpt id="p2">**</bpt>BankDeposit<ept id="p2">**</ept> from the <bpt id="p3">**</bpt>Archive template<ept id="p3">**</ept> list.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>バージョン履歴<ept id="p1">**</ept>ダイアログ ボックスで、<bpt id="p2">**</bpt>BankDeposit<ept id="p2">**</ept> を<bpt id="p3">**</bpt>アーカイブ テンプレート<ept id="p3">**</ept> リストから選択します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="399">
          <source>The Archive Object list contains the different versions of the Archive Object you saved.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">アーカイブ オブジェクトの一覧には、保存したアーカイブ オブジェクトのさまざまなバージョンが含まれています。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="400">
          <source>The list contains the most recent version at the top, and therefore you see BankDeposit<ph id="ph1">\_</ph>1 at the top of the list.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">リストには最新のバージョンが一番上に表示されているので、リストの一番上に BankDeposit<ph id="ph1">\_</ph>1 が表示されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="401">
          <source>Select any version, and then click <bpt id="p1">**</bpt>Show in the Archive Object list<ept id="p1">**</ept> to work with that version of the Archive Object.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">すべてのバージョンを選択し、<bpt id="p1">**</bpt>アーカイブ オブジェクトの一覧に表示<ept id="p1">**</ept> をクリックし、アーカイブ オブジェクトのバージョンを操作します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="402">
          <source>If you make any changes to this version and save it, the saved version becomes the most recent version and is used by the archive task at run time.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このバージョンを変更して保存すると、保存されたバージョンは最新バージョンになり、実行時にアーカイブ タスクによって使用されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="403">
          <source>Click <bpt id="p1">**</bpt>Close<ept id="p1">**</ept> to close the <bpt id="p2">**</bpt>Version history<ept id="p2">**</ept> dialog box.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>閉じる<ept id="p1">**</ept>をクリックして、<bpt id="p2">**</bpt>バージョン履歴<ept id="p2">**</ept>ダイアログ ボックスを閉じます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="404">
          <source>On the toolbar, click <bpt id="p1">**</bpt>Archive templates/Archive Object<ept id="p1">**</ept> <ph id="ph1">&amp;gt;</ph> <bpt id="p2">**</bpt>BankDeposit<ept id="p2">**</ept> to open the .</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ツールバーで、<bpt id="p1">**</bpt>アーカイブ テンプレート/アーカイブ オブジェクト<ept id="p1">**</ept> <ph id="ph1">&amp;gt;</ph> <bpt id="p2">**</bpt>BankDeposit<ept id="p2">**</ept> をクリックして開きます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="405">
          <source><bpt id="p1">**</bpt>Note:<ept id="p1">**</ept> The Data Management Framework opens the most recent version of the Archive Object that you saved.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>注記:<ept id="p1">**</ept> データ管理フレームワークは、保存したアーカイブ オブジェクトの最新バージョンを開きます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="406">
          <source>The archive task uses the most recent version of the Archive Object at run time.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">アーカイブ タスクは実行時に、アーカイブ オブジェクトの最新のバージョンを使用します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="407">
          <source>Validate all</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">すべて検証</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="408">
          <source>This command lets you programmatically validate all templates and objects.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このコマンドを使用すると、すべてのテンプレートとオブジェクトをプログラムで検証できます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="409">
          <source>The purge templates and archive templates that are included with the Data Management Framework are created based on functional validation of a standard Microsoft Dynamics AX application.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Data Management Framework に含まれている削除テンプレートとアーカイブ テンプレートは、標準の Microsoft Dynamics AX アプリケーションの機能検証に基づいて作成されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="410">
          <source>Your installation may not have the same license, configuration, and security keys.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">インストールに、同じライセンス、コンフィギュレーション、およびセキュリティ キーが含まれていないことがあります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="411">
          <source>As a result, you have to validate the default templates against your implementation before you can use them as Archive Objects or Purge Objects.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">結果として、アーカイブ オブジェクトまたは削除オブジェクトとして使用する前に、既定テンプレートを実装に対して検証する必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="412">
          <source>This command provides a programmatic way to validate all purge templates or all archive templates with a single click.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このコマンドを使用すると、すべての削除テンプレートまたはすべてのアーカイブ テンプレートをシングル クリックでプログラムで検証できます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="413">
          <source>This functionality only works with templates that are not validated yet, and ignores any previously validated templates.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この機能は、まだ検証されていないテンプレートでのみ動作し、以前に検証されたテンプレートは無視されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="414">
          <source>During the validation process, the Data Management Framework optionally removes tables from all templates and objects that have these characteristics:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">妥当性確認のプロセス中に、Data Management Framework はこれらの特性を持つすべてのテンプレートとオブジェクトからテーブルを削除することもできます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="415">
          <source>They are not in the production database of your Microsoft Dynamics AX implementation.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Microsoft Dynamics AX 実装の実稼働データベースにはありません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="416">
          <source>They have a relationship or a rule on a field that has a disabled configuration key in the production database.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">実稼働データベースに無効な構成キーがあるフィールドに、リレーションシップまたはルールがあります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="417">
          <source>They have a record count of 0 (zero).</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">0 (ゼロ) のレコード数があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="418">
          <source>On the toolbar, click <bpt id="p1">**</bpt>Validate all<ept id="p1">**</ept> to open the <bpt id="p2">**</bpt>Validate all templates and Objects<ept id="p2">**</ept> window.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ツール バーで、<bpt id="p1">**</bpt>すべて検証<ept id="p1">**</ept>をクリックして、<bpt id="p2">**</bpt>すべてのテンプレートとオブジェクトの検証<ept id="p2">**</ept>ウィンドウを開きます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="419">
          <source>Navigation of the Validate all templates and Objects window</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">すべてのテンプレートとオブジェクトの検証ウィンドウのナビゲーション</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="420">
          <source>The following tables provide descriptions for the controls in the <bpt id="p1">**</bpt>Validate all templates and Objects<ept id="p1">**</ept> window.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">次のテーブルで、<bpt id="p1">**</bpt>すべてのテンプレートとオブジェクトの検証<ept id="p1">**</ept> ウィンドウのコントロールについて説明します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="421">
          <source>Buttons</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ボタン</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="422">
          <source>Button</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ボタン</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="423">
          <source>Description</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">説明</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="424">
          <source><bpt id="p1">**</bpt>Save<ept id="p1">**</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>保存<ept id="p1">**</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="425">
          <source>Save the changes.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">変更を保存します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="426">
          <source>When you work with purge templates and Purge Objects, all existing purge templates and Purge Objects are overwritten.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">削除テンプレートと削除オブジェクトを操作するときは、すべての既存の削除テンプレートと削除オブジェクトは上書きされます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="427">
          <source>When working with archive templates and Archive Objects, you must provide a suffix.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">アーカイブ テンプレートとアーカイブ オブジェクトを使用するときは、接尾語を指定する必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="428">
          <source>The changes are saved as new versions, with a suffix value that is used for the new name.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">変更は新しいバージョンとして保存され、新しい名前に使用される接尾語値が使用されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="429">
          <source><bpt id="p1">**</bpt>Clear<ept id="p1">**</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>クリア<ept id="p1">**</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="430">
          <source>Clear the values for all the fields in the window.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ウィンドウ内のすべてのフィールドの値をクリアします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="431">
          <source><bpt id="p1">**</bpt>Close<ept id="p1">**</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>閉じる<ept id="p1">**</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="432">
          <source>Close the window.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ウィンドウを閉じます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="433">
          <source>Fields</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">フィールド</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="434">
          <source>Field</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">フィールド</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="435">
          <source>Description</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">説明</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="436">
          <source><bpt id="p1">**</bpt>Select an object type<ept id="p1">**</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>オブジェクトのタイプを選択<ept id="p1">**</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="437">
          <source>From the list, select <bpt id="p1">**</bpt>Purge<ept id="p1">**</ept> to validate all purge templates and Purge Objects.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">一覧から、<bpt id="p1">**</bpt>削除<ept id="p1">**</ept>を選択してすべての削除テンプレートと削除オブジェクトを検証します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="438">
          <source>Select <bpt id="p1">**</bpt>Archive<ept id="p1">**</ept> to validate all archive templates and Archive Objects.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>アーカイブ<ept id="p1">**</ept> を選択し、アーカイブ テンプレートとアーカイブ オブジェクトをすべて検証します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="439">
          <source><bpt id="p1">**</bpt>Suffix name<ept id="p1">**</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>接尾辞名<ept id="p1">**</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="440">
          <source>This field is only available when you select <bpt id="p1">**</bpt>Archive<ept id="p1">**</ept> from the <bpt id="p2">**</bpt>Select an object type<ept id="p2">**</ept> list.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このフィールドは、<bpt id="p2">**</bpt>オブジェクト タイプの選択<ept id="p2">**</ept>リストから<bpt id="p1">**</bpt>アーカイブ<ept id="p1">**</ept>を選択した場合にのみ使用できます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="441">
          <source>When validating objects, you overwrite existing purge templates and Purge Objects.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">オブジェクトを検証するとき、既存の削除テンプレートと削除オブジェクトを上書きします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="442">
          <source>However, you must use a suffix value to save the new versions of archive templates and Archive Objects.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ただし、接尾語値を使用してアーカイブ テンプレートとアーカイブ オブジェクトの新しいバージョンを保存する必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="443">
          <source>The suffix value is used to create a new name for the archive templates and Archive Objects.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">接尾語値は、アーカイブ テンプレートとアーカイブ オブジェクトの新しい名前を作成するために使用されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="444">
          <source>For example, if you enter 1 as the suffix name, the BankDeposit archive template is saved as BankDeposit<ph id="ph1">\_</ph>1.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">たとえば、接尾辞名として 1 を入力すると、BankDeposit アーカイブ テンプレートは BankDeposit<ph id="ph1">\_</ph>1 として保存されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="445">
          <source><bpt id="p1">**</bpt>Remove invalid tables<ept id="p1">**</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>無効なテーブルの削除<ept id="p1">**</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="446">
          <source>Select this field to remove all tables that are contained in templates and objects that are not in the production database.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">生産データベースにないテンプレートおよびオブジェクトに格納されているすべてのテーブルを削除するには、このフィールドを選択します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="447">
          <source>Removing a table from the templates and objects also removes related child tables from the relationship hierarchy, if there are any.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">テンプレートとオブジェクトからテーブルを削除すると、リレーションシップ階層からも関連する子テーブルが削除されます (ある場合)。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="448">
          <source><bpt id="p1">**</bpt>Remove tables with invalid fields<ept id="p1">**</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>無効なフィールドを含むテーブルの削除<ept id="p1">**</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="449">
          <source>The templates and objects may be using invalid fields in relationships and rules.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">テンプレートとオブジェクトは、関係やルールで無効なフィールドを使用している可能性があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="450">
          <source>A field that is not valid can be caused by your license, disabled security keys, disabled configuration keys, or incomplete post-installation tasks, such as the database synchronization.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">無効なフィールドは、ライセンス、無効なセキュリティ キー、無効なコンフィギュレーション キー、またはデータベースの同期など、未完了のインストール後のタスクによって発生する可能性があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="451">
          <source>Select this field to remove all tables that contain fields that are not valid from templates and objects.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">テンプレートおよびオブジェクトから有効でないフィールドを格納しているすべてのテーブルを削除するには、このフィールドを選択します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="452">
          <source>Removing a table from the templates and objects also removes related child tables from the relationship hierarchy, if there are any.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">テンプレートとオブジェクトからテーブルを削除すると、リレーションシップ階層からも関連する子テーブルが削除されます (ある場合)。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="453">
          <source><bpt id="p1">**</bpt>Remove tables with zero row<ept id="p1">**</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>ゼロの行を含むテーブルの削除<ept id="p1">**</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="454">
          <source>Select this field to remove all tables without rows from all templates and objects.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">すべてのテンプレートとオブジェクトから行のないすべてのテーブルを削除するには、このフィールドを選択します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="455">
          <source>Removing a table from the templates and objects also removes related child tables from the relationship hierarchy, if there are any.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">テンプレートとオブジェクトからテーブルを削除すると、リレーションシップ階層からも関連する子テーブルが削除されます (ある場合)。</target></trans-unit>
      </group>
    </body>
  </file>
</xliff>