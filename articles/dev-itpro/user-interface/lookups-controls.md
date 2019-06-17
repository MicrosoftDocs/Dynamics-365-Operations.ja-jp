<?xml version="1.0" encoding="UTF-8"?>
<xliff xmlns:logoport="urn:logoport:xliffeditor:xliff-extras:1.0" xmlns:tilt="urn:logoport:xliffeditor:tilt-non-translatables:1.0" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns="urn:oasis:names:tc:xliff:document:1.2" xmlns:xliffext="urn:microsoft:content:schema:xliffextensions" version="1.2" xsi:schemaLocation="urn:oasis:names:tc:xliff:document:1.2 xliff-core-1.2-transitional.xsd">
  <file datatype="xml" source-language="en-US" original="lookups-controls.md" target-language="ja-JP">
    <header>
      <tool tool-company="Microsoft" tool-version="1.0-7889195" tool-name="mdxliff" tool-id="mdxliff"/>
      <xliffext:skl_file_name>lookups-controls.981698.940ac764d70a224721a4c29f4dfc76a68a8712e1.skl</xliffext:skl_file_name>
      <xliffext:version>1.2</xliffext:version>
      <xliffext:ms.openlocfilehash>940ac764d70a224721a4c29f4dfc76a68a8712e1</xliffext:ms.openlocfilehash>
      <xliffext:ms.sourcegitcommit>9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b</xliffext:ms.sourcegitcommit>
      <xliffext:ms.lasthandoff>05/15/2019</xliffext:ms.lasthandoff>
      <xliffext:ms.openlocfilepath>articles\dev-itpro\user-interface\lookups-controls.md</xliffext:ms.openlocfilepath>
    </header>
    <body>
      <group extype="content" id="content">
        <trans-unit xml:space="preserve" translate="yes" id="101" restype="x-metadata">
          <source>Lookup controls</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ルックアップ コントロール</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="102" restype="x-metadata">
          <source>This article discusses how to enable lookup behavior on controls.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この記事では、コントロールの検索動作を有効にする方法について説明します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="103" restype="x-metadata">
          <source>It also discusses how to create multi-select lookups and outlines lookup scenarios that are no longer supported.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">また、複数選択ルックアップを作成する方法について説明し、現在サポートされていないルックアップ シナリオの概要について説明します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="104">
          <source>Lookup controls</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ルックアップ コントロール</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="105">
          <source>This article discusses how to enable lookup behavior on controls.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この記事では、コントロールの検索動作を有効にする方法について説明します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="106">
          <source>It also discusses how to create multi-select lookups and outlines lookup scenarios that are no longer supported.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">また、複数選択ルックアップを作成する方法について説明し、現在サポートされていないルックアップ シナリオの概要について説明します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="107">
          <source>Enabling lookup behavior in controls</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">コントロールのルックアップ動作を有効化</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="108">
          <source>Controls bound to an Extended Data Type</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">拡張データ型にバインドされたコントロール</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="109">
          <source>Controls with their Extended Data Type property set (no FormDataSource in play) will have a lookup under the following conditions:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">拡張データ型プロパティ セット (実行中の FormDataSource が無い) を持つコントロールは、次の条件の下で検索を行います。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="110">
          <source>If the EDT has its Table Relations or Table References node populated.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">EDT にはそのテーブル リレーションまたはテーブルの参照ノードが設定されているかどうか。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="111">
          <source>If the FormHelp property is set (custom lookup); doesn’t require rule <ph id="ph1">\#</ph>1 to be true.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">FormHelp プロパティが設定されている場合、ルール <ph id="ph1">\#</ph>1 を true に設定 (カスタム ルックアップ) する必要はありません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="112">
          <source>If the control has lookup or lookupReference overridden.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">コントロールでルックアップまたは lookupReference が上書きされている場合。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="113">
          <source>Note, this rule also applies to fully unbound controls (no EDT, field, or data method).</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このルールは、完全な非連結コントロール (EDT、フィールド、またはデータ メソッドなし) にも適用されることに注意してください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="114">
          <source>This includes overrides via registerOverrideMethod and others.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">これには、registerOverrideMethod などの上書きも含まれます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="115">
          <source>Controls bound to a form data source</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">フォーム データ ソースにバインドされたコントロール</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="116">
          <source>Controls that are bound to a data source will have a lookup under the following conditions: <bpt id="p1">**</bpt>Field bound<ept id="p1">**</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">データ ソースにバインドされたコントロールは、次の条件の下で検索されます。<bpt id="p1">**</bpt>フィールド バインド<ept id="p1">**</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="117">
          <source>“lookup” or “lookupReference” (Reference Controls) methods are overridden.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">"lookup" または "lookupReference" (参照コントロール) メソッドが上書きされます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="118">
          <source>If the FormDataSource field has lookup or lookupReference overridden.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">FormDataSource フィールドでルックアップまたは lookupReference が上書きされている場合。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="119">
          <source>If the control has lookup or lookupReference overridden.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">コントロールでルックアップまたは lookupReference が上書きされている場合。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="120">
          <source>This includes overrides via registerOverrideMethod and others.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">これには、registerOverrideMethod などの上書きも含まれます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="121">
          <source>If the field has an EDT, then rule <ph id="ph1">\#</ph>2 from the "Controls bound to an Extended Data Type" section applies.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このフィールドに EDT がある場合、「拡張データ型にバインドされたコントロール」セクションのルール <ph id="ph1">\#</ph> が適用されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="122">
          <source>If the bound field maps to a relation per DBFGetRef rules.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">バインディング フィールドは、DBFGetRef ルールごとにリレーションをマップします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="123">
          <source>High level rules:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">高レベルのルール。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="124">
          <source>If there is an EDT relation backing the field, with the Table Relations node populated and Ignore EDT Relations is false on the field, the relation is used (has a lookup).</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">フィールドを支持する EDT 関係が存在し、テーブル関係ノードが入力され、Ignore EDT Relations がフィールド上で false である場合、その関係が使用されます (ルックアップがある)。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="125">
          <source>If there is a relation mapping to the field and any fixed field link conditions are satisfied, the relation is used (has a lookup).</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">フィールドに対してリレーション マッピングが使用され、任意の固定フィールド リンク条件が満たされている場合は、そのリレーションが使用されます (ルックアップがある)。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="126">
          <source>Validate must be “Yes”.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">検証は「はい」にする必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="127">
          <source>Note the special case of migrated EDT relations which occur when:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">次の場合に発生する 移行された EDT 関係の特殊なケースに注意してください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="128">
          <source>Field is backed by an EDT with the Relations node populated.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">フィールドは、関係ノードが設定される EDT によってサポートされます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="129">
          <source>Field is backed by a TABLE relation with the “EDTRelation” set to Yes.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">フィールドは、「EDTRelation」設定を「はい」にするテーブル関係によってサポートされます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="130">
          <source>The table relation link has the SourceEDT set to the appropriate EDT.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">テーブル関係リンクは SourceEDT が適切な EDT に設定されています。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="131">
          <source>You can also have cases where IgnoreEDTRelation is set to true on a field, in which case a lookup will occur only if rule <ph id="ph1">\#</ph>3.1.2 of this section is true.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">また、IgnoreEDTRelation がフィールド上で true にセットされているケースを持つことができます。このケースでは、このセクションのルール <ph id="ph1">\#</ph>3.1.2 が true である場合にのみルックアップが発生します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="132">
          <source><bpt id="p1">**</bpt>Data method bound<ept id="p1">**</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>データ メソッド バインド<ept id="p1">**</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="133">
          <source>If the return type of the data method is an EDT, then rules <ph id="ph1">\#</ph>1 and <ph id="ph2">\#</ph>2 from the "Controls bound to an Extended Data Type" section apply.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">データ メソッドの戻り値が EDT である場合、「拡張データ型にバインドされたコントロール」セクションのルール <ph id="ph1">\#</ph>1 と <ph id="ph2">\#</ph> が適用されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="134">
          <source>If the control has lookup or lookupReference overridden.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">コントロールでルックアップまたは lookupReference が上書きされている場合。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="135">
          <source>This includes overrides by using registerOverrideMethod.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">これには、registerOverrideMethod を使用した上書きも含まれます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="136">
          <source>Multiselect lookups</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">複数選択のルックアップ</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="137">
          <source>Available system forms for building multi-select lookups</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">複数選択ルックアップを構築するために利用可能なシステム フォーム</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="138">
          <source>There are currently two system forms for creating multi-select lookups:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">現在、複数選択ルックアップを作成するためのシステム フォームが 2 つあります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="139">
          <source>SysLookup – Multiselect based on an Enum.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">SysLookup: 列挙に基づいて複数選択します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="140">
          <source>SysLookupMultiselectGrid – Multiselect based on a collection of data.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">SysLookupMultiselectGrid: データの収集に基づいて複数選択します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="141">
          <source>What happened to the SysLookupMultiselect form?</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">SysLookupMultiselect フォームの変更点とは</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="142">
          <source>SysLookupMultiselect was marked for deprecation in Microsoft Dynamics AX 2012 and has been removed.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">SysLookupMultiselect は、Microsoft Dynamics AX 2012 で廃止の対象としてマークされ、削除されました。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="143">
          <source>Any use of this form for multiselect lookup scenarios should be migrated to use SysLookupMultiselectGrid.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">複数選択のルックアップ シナリオでこのフォームを使用する場合、SysLookupMultiselectGrid を使用するように移行する必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="144">
          <source>For an example, see the form tutorial<ph id="ph1">\_</ph>LookupMultiSelectGrid.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">例については、チュートリアル<ph id="ph1">\_</ph>LookupMultiSelectGrid のフォームを参照してください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="145">
          <source>Unsupported lookup scenarios</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">検索シナリオはサポートされていません</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="146">
          <source>Creating multiple lookup forms when the lookup button is used</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ルックアップ ボタンが使用されているときの複数のルックアップ フォームを作成しています</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="147">
          <source>An error may occur if you create multiple lookup forms when the lookup button is used.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ルックアップ ボタンを使用して複数のルックアップ フォームを作成する場合にエラーが発生する可能性があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="148">
          <source>For example, overriding the ‘lookup’ method and creating a new lookup form, but also calling ‘super’ (which will create another lookup form).</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">たとえば、「ルックアップ」メソッドを上書きして新しいルックアップ フォームを作成しても、「スーパー」 (別のルックアップ フォームを作成します) も呼び出します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="149">
          <source>Using SelectedControl() to determine which control is hosting a lookup</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">SelectedControl() を使用してルックアップをホストしているコントロールを決定</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="150">
          <source>Using SelectedControl() to determine which control is hosting a lookup is unsupported.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ルックアップをホストしているコントロールを決定する SelectedControl() の使用はサポートされていません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="151">
          <source>While it may work in some cases, it will fail in others.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">場合によっては動作しますが、他の場合には失敗します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="152">
          <source>For example, in disambiguation lookups, no control is selected on the parent form since the act of leaving the control is what triggers a disambiguation lookup.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">たとえば、曖昧性解消ルックアップでは、コントロールを離れる行為は、曖昧性解消ルックアップをトリガーすることであるため、親フォーム上でコントロールは選択されていません。。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="153">
          <source>As an alternative to using SelectedControl(), there are a few other ways to retrieve the control that is hosting the lookup:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">SelectedControl() を使用する代わりに、ルックアップをホストしているコントロールを取得するいくつかの方法があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="154">
          <source>Check the ‘selectTarget’ of the lookup form.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ルックアップ フォームの「selectTarget」を確認してください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="155">
          <source>Check the ‘callerFormControl’ on the lookup form args.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ルックアップ フォーム引数の「callerFormControl」を確認してください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="156">
          <source>Note that SysTableLookup::getCallerControl(Args args) encapsulates that call.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">SysTableLookup::getCallerControl(Args args) はその呼び出しをカプセル化することに注意してください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="157">
          <source>Note that the selectTarget and callerFormControl will be set automatically if the lookup form instance is spun up automatically by the kernel.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ルックアップ フォーム インスタンスがカーネルによって自動的にスピン アップされる場合、selectTarget および callerFormControl が自動的に設定されることに注意してください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="158">
          <source>If the form instance is created in app code, these can be set manually as shown below.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">フォーム インスタンスがアプリケーション コードで作成される場合、これらを次のように手動で設定できます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="159">
          <source>public void lookup() { Args args = new Args(formStr(<ph id="ph1">&lt;formName&gt;</ph>)); args.caller(element); args.callerFormControl(this); FormRun formRun = classfactory.formRunClass(args); formRun.init(); this.performFormLookup(formRun); }</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">public void lookup() { Args args = new Args(formStr(<ph id="ph1">&lt;formName&gt;</ph>)); args.caller(element); args.callerFormControl(this); FormRun formRun = classfactory.formRunClass(args); formRun.init(); this.performFormLookup(formRun); }</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="160">
          <source>Creating a slider dialog (instead of a lookup form) when the lookup button is used</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ルックアップ ボタンを使用する際のスライダーのダイアログ (ルックアップ フォームの代わりに) を作成しています</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="161">
          <source>Lookup controls should open lookup forms when the lookup button is used (not slider dialogs or other kinds of forms).</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ルックアップ ボタンを使用すると、ルックアップ コントロールによってルックアップ フォームを開く必要があります (スライダー ダイアログまたはその他の種類のフォームではありません)。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="162">
          <source>The first reason for this is product consistency.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">これの第 1 の理由は、製品の整合性を保つことです。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="163">
          <source>The second and more important reason is that opening a slider dialog from a lookup is incompatible with the new type-ahead feature in lookups.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">2 番目の重要な理由は、ルックアップからスライダー ダイアログを開くことは、ルックアップの新しい先行入力機能と互換性がないことです。</target></trans-unit>
      </group>
    </body>
  </file>
</xliff>