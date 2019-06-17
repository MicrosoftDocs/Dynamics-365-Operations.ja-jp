<?xml version="1.0" encoding="UTF-8"?>
<xliff xmlns:logoport="urn:logoport:xliffeditor:xliff-extras:1.0" xmlns:tilt="urn:logoport:xliffeditor:tilt-non-translatables:1.0" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns="urn:oasis:names:tc:xliff:document:1.2" xmlns:xliffext="urn:microsoft:content:schema:xliffextensions" version="1.2" xsi:schemaLocation="urn:oasis:names:tc:xliff:document:1.2 xliff-core-1.2-transitional.xsd">
  <file datatype="xml" source-language="en-US" original="code-migration-context-menus.md" target-language="ja-JP">
    <header>
      <tool tool-company="Microsoft" tool-version="1.0-7889195" tool-name="mdxliff" tool-id="mdxliff"/>
      <xliffext:skl_file_name>code-migration-context-menus.affa1f.52be3047cdd20ca7f17d9d980164c1a43bf0d2f8.skl</xliffext:skl_file_name>
      <xliffext:version>1.2</xliffext:version>
      <xliffext:ms.openlocfilehash>52be3047cdd20ca7f17d9d980164c1a43bf0d2f8</xliffext:ms.openlocfilehash>
      <xliffext:ms.sourcegitcommit>9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b</xliffext:ms.sourcegitcommit>
      <xliffext:ms.lasthandoff>05/15/2019</xliffext:ms.lasthandoff>
      <xliffext:ms.openlocfilepath>articles\dev-itpro\migration-upgrade\code-migration-context-menus.md</xliffext:ms.openlocfilepath>
    </header>
    <body>
      <group extype="content" id="content">
        <trans-unit xml:space="preserve" translate="yes" id="101" restype="x-metadata">
          <source>Code migration - Context menu code</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">コードの移行 - コンテキスト メニュー コード</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="102" restype="x-metadata">
          <source>A new programming model is required for context menus (shortcut menus).</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">新しいプログラミング モデルには、コンテキスト メニュー (ショートカット メニュー) が必要です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="103" restype="x-metadata">
          <source>This article outlines the process for migrating context menu code from Microsoft Dynamics AX 2012 to Microsoft Dynamics 365 for Finance and Operations.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この記事では、Microsoft DynamicsAX 2012 から Microsoft Dynamics 365 for Finance and Operations へのコンテキスト メニュー コードの移行プロセスの概要を説明します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="104" restype="x-metadata">
          <source>It also includes UX guidelines for context menus.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">また、コンテキスト メニューの UX ガイドラインも含まれます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="105">
          <source>Code migration - Context menu code</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">コードの移行 - コンテキスト メニュー コード</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="106">
          <source>A new programming model is required for context menus (shortcut menus).</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">新しいプログラミング モデルには、コンテキスト メニュー (ショートカット メニュー) が必要です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="107">
          <source>This article outlines the process for migrating context menu code from Microsoft Dynamics AX 2012 to Microsoft Dynamics 365 for Finance and Operations.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この記事では、Microsoft DynamicsAX 2012 から Microsoft Dynamics 365 for Finance and Operations へのコンテキスト メニュー コードの移行プロセスの概要を説明します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="108">
          <source>It also includes UX guidelines for context menus.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">また、コンテキスト メニューの UX ガイドラインも含まれます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="109">
          <source>In Microsoft Dynamics AX 2012 and earlier versions, developers modified right-click context menus (shortcut menus) by using the <bpt id="p1">**</bpt>PopupMenu<ept id="p1">**</ept> class.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Microsoft Dynamics AX 2012 およびそれ以前のバージョンでは、開発者が <bpt id="p1">**</bpt>PopupMenu<ept id="p1">**</ept> クラスを使用して右クリック コンテキスト メニュー (ショートカット メニュー) を変更していました。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="110">
          <source>This class relied on Microsoft Windows application programming interfaces (APIs) that aren't available on the web.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このクラスは、Web 上で利用できない Microsoft Windows アプリケーション プログラミング インターフェイス (API) に依存していました。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="111">
          <source>In Finance and Operations, the <bpt id="p1">**</bpt>ContextMenu<ept id="p1">**</ept> APIs have been created as replacements to provide similar functionality.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Finance and Operations では、同様の機能を提供する代わりに <bpt id="p1">**</bpt>ContextMenu<ept id="p1">**</ept> API が作成されました。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="112">
          <source>Previously, the <bpt id="p1">**</bpt>context()<ept id="p1">**</ept> and <bpt id="p2">**</bpt>showContextMenu()<ept id="p2">**</ept> method overrides were the entry points for modifying context menus for specific controls.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">以前は、<bpt id="p1">**</bpt>context()<ept id="p1">**</ept> メソッドと <bpt id="p2">**</bpt>showContextMenu()<ept id="p2">**</ept> メソッドのオーバーライドは、特定のコントロールのコンテキスト メニューを変更するためのエントリ ポイントでした。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="113">
          <source>These overrides typically contained code to add options to the context menu, and also to process the user’s selection.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">これらの上書きには通常、コンテキスト メニューにオプションを追加したり、ユーザーの選択を処理するためのコードが含まれていました。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="114">
          <source>The code for processing the user's selection used a wait model.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ユーザーの選択を処理するコードは、待機モデルを使用していました。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="115">
          <source>In Finance and Operations, these overrides are being removed, and the wait model is being eliminated.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Finance and Operations では、これらのオーバーライドが削除され、待機モデルは消去されています。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="116">
          <source>Instead, developers must create two overrides: <bpt id="p1">**</bpt>getContextMenuOptions()<ept id="p1">**</ept> to add options to the context menu and <bpt id="p2">**</bpt>selectedMenuOption()<ept id="p2">**</ept> to process the user’s selection.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">代わりに、開発者はオプションにコンテキスト メニューを追加する <bpt id="p1">**</bpt>getContextMenuOptions()<ept id="p1">**</ept> およびユーザーの選択を処理する <bpt id="p2">**</bpt>selectedMenuOption()<ept id="p2">**</ept> の 2 つのオーバーライドを作成する必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="117">
          <source>Migrate context menu code in Finance and Operations</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Finance and Operations でのコンテキスト メニュー コードの移行</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="118">
          <source>Migration from the <bpt id="p1">**</bpt>PopupMenu<ept id="p1">**</ept> APIs to the <bpt id="p2">**</bpt>ContextMenu<ept id="p2">**</ept> APIs can be broken down into three main steps.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>PopupMenu<ept id="p1">**</ept> API から <bpt id="p2">**</bpt>ContextMenu<ept id="p2">**</ept> API への移行は、3 つの主な段階に分けることができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="119">
          <source>Step 1.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">手順 1</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="120">
          <source>Add a constant for each menu option that must be added</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">追加する必要のあるメニュー オプションごとの定数の追加</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="121">
          <source>The old <bpt id="p1">**</bpt>insertItem()<ept id="p1">**</ept> method in the <bpt id="p2">**</bpt>PopupMenu<ept id="p2">**</ept> class returned an identifier for the menu option that was being added.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p2">**</bpt>PopupMenu<ept id="p2">**</ept> クラスの古い <bpt id="p1">**</bpt>insertItem()<ept id="p1">**</ept> メソッドは、追加されたメニュー オプションの識別子を返しました。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="122">
          <source>This identifier was saved into a variable for future reference.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この識別子は、将来の参照のために変数に保存されました。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="123">
          <source>Because developers will define the menu identifier for themselves in Finance and Operations, it's a good idea to define constants for each option to help with code readability.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">開発者は Finance and Operations でメニュー識別子を定義するため、各オプションの定数を定義してコードの可読性を高めることをお勧めします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="124">
          <source>At the form level, add a constant for each menu option that is being added to the context menu.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">フォーム レベルでは、コンテキスト メニューに追加されている各メニュー オプションの定数を追加します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="125">
          <source>The value must be unique within each context menu.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">値は各コンテキスト メニュー内で一意でなければなりません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="126">
          <source>Note that you must modify the old variable name if it conflicts with another variable on the form or control.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">フォームまたはコントロールで別の変数と競合する場合、古い変数名を変更する必要があることに注意してください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="127">
          <source>Before</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">以前</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="128">
          <source>After</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">変更後</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="129">
          <source>Step 2.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">手順 2</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="130">
          <source>Build the context menu</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">コンテキスト メニューの構築</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="131">
          <source>Construct the list of submenus and menu options, and add it to the control’s context menu.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">サブメニューとメニュー オプションのリストを構築し、コントロールのコンテキスト メニューに追加します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="132">
          <source>Add the <bpt id="p1">**</bpt>getContextMenuOptions()<ept id="p1">**</ept> method override on the control.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">コントロールの <bpt id="p1">**</bpt>getContextMenuOptions()<ept id="p1">**</ept> メソッドの上書きを追加します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="133">
          <source>Create a new context menu and a list to hold the options that you will add to the menu:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">新しいコンテキスト メニューと、メニューに追加するオプションを保持するリストを作成します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="134">
          <source>ContextMenu menu = new ContextMenu();</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ContextMenu メニュー = 新しい ContextMenu();</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="135">
          <source>List menuOptions = new List(Types::Class);</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">List menuOptions = new List(Types::Class);</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="136">
          <source>Add menu options to the list:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">一覧にメニュー オプションを追加:</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="137">
          <source>ContextMenuOption option = ContextMenuOption::Create(label,identifier);</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ContextMenuOption option = ContextMenuOption::Create(label,identifier);</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="138">
          <source>menuOptions.addEnd(option);</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">menuOptions.addEnd(option);</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="139">
          <source>Add the list of options to the menu.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">メニューにオプションのリストを追加します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="140">
          <source>menu.ContextMenuOptions(menuOptions);</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">menu.ContextMenuOptions(menuOptions);</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="141">
          <source>Modify the <bpt id="p1">**</bpt>return<ept id="p1">**</ept> statement.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>return<ept id="p1">**</ept> ステートメントを変更します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="142">
          <source>return menu.Serialize();</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">return menu.Serialize();</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="143">
          <source>Step 3.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">手順 3</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="144">
          <source>Process the user selection from the context menu</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">コンテキスト メニューからのユーザーの選択を処理</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="145">
          <source>Add the <bpt id="p1">**</bpt>selectedMenuOption()<ept id="p1">**</ept> method override on the control.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">コントロールの <bpt id="p1">**</bpt>selectedMenuOption()<ept id="p1">**</ept> メソッドの上書きを追加します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="146">
          <source>Move the <bpt id="p1">**</bpt>switch()<ept id="p1">**</ept> statement for processing options into this override.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">オプション処理用の <bpt id="p1">**</bpt>switch()<ept id="p1">**</ept> ステートメントを、このオーバーライドに移動します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="147">
          <source>Code example</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">コードの例</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="148">
          <source>This section illustrates the migration of a context menu from Dynamics AX 2012 to Finance and Operations.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このセクションでは、Dynamics AX 2012 から Finance and Operations へのコンテキスト メニューの移行について説明します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="149">
          <source>The <bpt id="p1">**</bpt>MainAccount<ept id="p1">**</ept> form is used as an example.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>MainAccount<ept id="p1">**</ept> フォームが例として使用されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="150">
          <source>Original code</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">オリジナル コピー</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="151">
          <source>Migrated code</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">移行されたコード</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="152">
          <source>UX guidelines for context menus</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">コンテキスト メニューの UX ガイドライン</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="153">
          <source>As you migrate context menus, consider the following guidelines:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">コンテキスト メニューを移行する際、次のガイドラインを考慮してください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="154">
          <source>The most important commands should be at the top of the menu.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">最も重要なコマンドは、メニューの先頭にある必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="155">
          <source>Remove commands that don't apply to the current state of the element that is the target of the right-click.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">右クリックの対象となる要素の現在の状態に適用されないコマンドを削除します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="156">
          <source>Right-click is a shortcut.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">右クリックはショートカットです。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="157">
          <source>Therefore, the commands on the context menu should <bpt id="p1">**</bpt>always<ept id="p1">**</ept> be available in other places on the page.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">したがって、コンテキスト メニューのコマンドは、<bpt id="p1">**</bpt>常に<ept id="p1">**</ept>ページの他の場所で利用できる必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="158">
          <source>Don't create submenus of context menus.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">コンテキスト メニューのサブメニューを作成しないでください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="159">
          <source>Submenus are hard to use and aren't touch-friendly.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">サブメニューは使いにくくタッチ対応ではありません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="160">
          <source>Limit the number of menu items to five.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">メニュー項目の数を 5 に制限します。</target></trans-unit>
      </group>
    </body>
  </file>
</xliff>