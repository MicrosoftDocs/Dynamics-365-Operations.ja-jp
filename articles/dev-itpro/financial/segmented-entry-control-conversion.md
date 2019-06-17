<?xml version="1.0" encoding="UTF-8"?>
<xliff xmlns:logoport="urn:logoport:xliffeditor:xliff-extras:1.0" xmlns:tilt="urn:logoport:xliffeditor:tilt-non-translatables:1.0" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns="urn:oasis:names:tc:xliff:document:1.2" xmlns:xliffext="urn:microsoft:content:schema:xliffextensions" version="1.2" xsi:schemaLocation="urn:oasis:names:tc:xliff:document:1.2 xliff-core-1.2-transitional.xsd">
  <file datatype="xml" source-language="en-US" original="segmented-entry-control-conversion.md" target-language="ja-JP">
    <header>
      <tool tool-company="Microsoft" tool-version="1.0-7889195" tool-name="mdxliff" tool-id="mdxliff"/>
      <xliffext:skl_file_name>segmented-entry-control-conversion.ed9c3a.f17adf415ec407d6058e0bf16d204114540cdb6a.skl</xliffext:skl_file_name>
      <xliffext:version>1.2</xliffext:version>
      <xliffext:ms.openlocfilehash>f17adf415ec407d6058e0bf16d204114540cdb6a</xliffext:ms.openlocfilehash>
      <xliffext:ms.sourcegitcommit>9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b</xliffext:ms.sourcegitcommit>
      <xliffext:ms.lasthandoff>05/15/2019</xliffext:ms.lasthandoff>
      <xliffext:ms.openlocfilepath>articles\dev-itpro\financial\segmented-entry-control-conversion.md</xliffext:ms.openlocfilepath>
    </header>
    <body>
      <group extype="content" id="content">
        <trans-unit xml:space="preserve" translate="yes" id="101" restype="x-metadata">
          <source>Migrate Segmented Entry controls</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">セグメント化されたエントリ コントロールの移行</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="102" restype="x-metadata">
          <source>This tutorial walks you through two migration scenarios for the Segmented Entry control -  a simple scenario (for the SMAServiceOrderTable form) and a complex scenario (for the LedgerJournalTransDaily form).</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このチュートリアルでは、簡単なシナリオ (SMAServiceOrderTable フォームの場合) と複雑なシナリオ (LedgerJournalTransDaily フォームの場合) の 2 つのセグメント化エントリ管理の移行シナリオについて説明します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="103">
          <source>Migrate Segmented Entry controls</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">セグメント化されたエントリ コントロールの移行</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="104">
          <source>This tutorial walks you through two migration scenarios for the Segmented Entry control -  a simple scenario (for the SMAServiceOrderTable form) and a complex scenario (for the LedgerJournalTransDaily form).</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このチュートリアルでは、簡単なシナリオ (SMAServiceOrderTable フォームの場合) と複雑なシナリオ (LedgerJournalTransDaily フォームの場合) の 2 つのセグメント化エントリ管理の移行シナリオについて説明します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="105">
          <source>Simple migration scenario – SMAServiceOrderTable form</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">簡易移行シナリオ - SMAServiceOrderTable フォーム</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="106">
          <source>Search for the <bpt id="p1">**</bpt>SMAServiceOrderTable<ept id="p1">**</ept> form in Application Explorer.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">アプリケーション エクスプローラーで <bpt id="p1">**</bpt>SMAServiceOrderTable<ept id="p1">**</ept> フォームを検索します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="107">
          <source>Add the form to the current project.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">現在のプロジェクトにフォームを追加します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="108">
          <source>Open the form in the form design view and the code editor view.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">フォーム デザイン ビューとコード エディタ ビューで、フォームを開きます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="109">
          <source>In the form design view, find the Segmented Entry control (SEC), either by manually walking the control tree or by searching for “SegmentedEntry” in the search bar below the <bpt id="p1">**</bpt>File<ept id="p1">**</ept> tab.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">フォーム デザイン ビューで、手動でコントロール ツリーを移動するか、<bpt id="p1">**</bpt>ファイル<ept id="p1">**</ept> タブの下にある検索バーで「SegmentedEntry」を検索して、セグメント化されたエントリ コントロール (SEC) を見つけます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="110">
          <source>Select the SEC, and verify the following information:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">SEC を選択し、次の情報を確認します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="111">
          <source>The type for the control, as specified in parenthesis next to the control, is <bpt id="p1">**</bpt>SegmentedEntryControl<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">コントロールの横にある括弧で指定されたコントロールのタイプは、<bpt id="p1">**</bpt>SegmentedEntryControl<ept id="p1">**</ept> です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="112">
          <source>The <bpt id="p1">**</bpt>Controller class<ept id="p1">**</ept> property is set to <bpt id="p2">**</bpt>DimensionDynamicAccountController<ept id="p2">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>コントローラー クラス<ept id="p1">**</ept> プロパティは <bpt id="p2">**</bpt>DimensionDynamicAccountController<ept id="p2">**</ept> に設定されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="113">
          <source>This property indicates the type of controller that this instance of the SEC will use.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このプロパティは、SEC のこのインスタンスが使用するコントローラーのタイプを示します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="114">
          <source>The type of controller, in turn, determines the behavior of the control.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">コントローラーのタイプによって、コントロールのビヘイビアーが決まります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="115">
          <source>Switch to the code editor view, and search for all occurrences of “TODO: (Code Upgrade) <ph id="ph1">\[</ph>Segmented entry control<ph id="ph2">\]</ph>” in the form source code.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">コード エディタ ビューに切り替え、フォーム ソース コードで "TODO: (コード アップグレード) <ph id="ph1">\[</ph>セグメント化されたエントリ コントロール<ph id="ph2">\]</ph>" のすべての事例を検索します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="116">
          <source>In the search results, ignore the first result, which points to the controller variable declaration.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">検索結果で最初の結果を無視すると、コントローラー変数申告を示します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="117">
          <source>You must fix this TODO last, after you've removed all references to the controller variable.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">制御変数への参照をすべて削除したら、最後に、この作業項目を修正する必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="118">
          <source>Go through each of the remaining TODO comments, as described in the following subsections.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">次のサブセクションでの説明にあるように、残りの各 TODO コメントが実行されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="119">
          <source>LedgerDimension data field</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">LedgerDimension データ フィールド</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="120">
          <source>(<bpt id="p1">**</bpt>Form<ept id="p1">**</ept> <ph id="ph1">&amp;gt;</ph> <bpt id="p2">**</bpt>Data sources<ept id="p2">**</ept> <ph id="ph2">&amp;gt;</ph> <bpt id="p3">**</bpt>SMAServiceOrderLine<ept id="p3">**</ept> <ph id="ph3">&amp;gt;</ph> <bpt id="p4">**</bpt>Fields<ept id="p4">**</ept> <ph id="ph4">&amp;gt;</ph> <bpt id="p5">**</bpt>LedgerDimension<ept id="p5">**</ept> <ph id="ph5">&amp;gt;</ph> <bpt id="p6">**</bpt>Methods<ept id="p6">**</ept>)</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">(<bpt id="p1">**</bpt>フォーム<ept id="p1">**</ept><ph id="ph1">&amp;gt;</ph><bpt id="p2">**</bpt>データ ソース<ept id="p2">**</ept> <ph id="ph2">&amp;gt;</ph><bpt id="p3">**</bpt>SMAServiceOrderLine<ept id="p3">**</ept><ph id="ph3">&amp;gt;</ph> <bpt id="p4">**</bpt>フィールド<ept id="p4">**</ept> <ph id="ph4">&amp;gt;</ph><bpt id="p5">**</bpt>LedgerDimension<ept id="p5">**</ept><ph id="ph5">&amp;gt;</ph> <bpt id="p6">**</bpt>方法<ept id="p6">**</ept>)</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="121">
          <source>Dynamics AX 2012</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Dynamics AX 2012</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="122">
          <source>Dynamics AX for Operations</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Dynamics AX for Operations</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="123">
          <source>Because this method only calls the <bpt id="p1">**</bpt>jumpRef()<ept id="p1">**</ept> method on the control and doesn't perform any additional processing, you can delete it.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このメソッドはコントロールの <bpt id="p1">**</bpt>jumpRef()<ept id="p1">**</ept> メソッドのみを呼び出し追加の処理は実行しないため、削除できます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="124">
          <source>ExpenseCost<ph id="ph1">\_</ph>LedgerDimension control</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ExpenseCost<ph id="ph1">\_</ph>LedgerDimension コントロール</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="125">
          <source>(Search for "ExpenseCost<ph id="ph1">\_</ph>LedgerDimension" in the search bar below the <bpt id="p1">**</bpt>Form<ept id="p1">**</ept> tab.)</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">(<bpt id="p1">**</bpt>フォーム<ept id="p1">**</ept>タブの下にある検索バーで「ExpenseCost<ph id="ph1">\_</ph>LedgerDimension」を検索してください。)</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="126">
          <source>Step 1</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ステップ１</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="127">
          <source>Dynamics AX 2012</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Dynamics AX 2012</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="128">
          <source>Dynamics AX for Operations</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Dynamics AX for Operations</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="129">
          <source>Because this method only calls the <bpt id="p1">**</bpt>jumpRef()<ept id="p1">**</ept> method on the control and doesn't performing any additional processing, you can delete it.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このメソッドはコントロールの <bpt id="p1">**</bpt>jumpRef()<ept id="p1">**</ept> メソッドのみを呼び出し追加の処理は行わないため、削除できます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="130">
          <source>Step 2</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ステップ２</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="131">
          <source>Dynamics AX 2012</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Dynamics AX 2012</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="132">
          <source>Dynamics AX for Operations</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Dynamics AX for Operations</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="133">
          <source>Because this method only calls the <bpt id="p1">**</bpt>loadSegments()<ept id="p1">**</ept> method on the control and doesn't perform any additional processing, you can delete it.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このメソッドはコントロールの <bpt id="p1">**</bpt>loadSegments()<ept id="p1">**</ept> メソッドのみを呼び出し追加の処理は実行しないため、削除できます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="134">
          <source>Step 3</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ステップ 3</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="135">
          <source>Dynamics AX 2012</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Dynamics AX 2012</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="136">
          <source>Dynamics AX for Operations</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Dynamics AX for Operations</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="137">
          <source>This method implements a custom lookup for the control.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このメソッドは、コントロールのカスタム ルックアップを実装します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="138">
          <source>Therefore, leave the method as it is.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">したがって、メソッドをそのままにします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="139">
          <source>Just remove the TODO.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">"仕事" を削除します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="140">
          <source>To hook up custom lookups, you must override the SEC’s <bpt id="p1">**</bpt>checkUseCustomLookup<ept id="p1">**</ept> method.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">カスタムのルックアップをフック アップするには、SEC の <bpt id="p1">**</bpt>checkUseCustomLookup<ept id="p1">**</ept> メソッドをオーバーライドする必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="141">
          <source>Here is an example.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">次に例を示します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="142">
          <source>Additionally, make sure that the <bpt id="p1">**</bpt>closeSelectRecord<ept id="p1">**</ept> method on the custom lookup form is overridden.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">また、カスタム ルックアップ フォームで <bpt id="p1">**</bpt>closeSelectRecord<ept id="p1">**</ept> メソッドが上書きされたことを確認してください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="143">
          <source>For an example, see the <bpt id="p1">**</bpt>CustTableLookup<ept id="p1">**</ept> form.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">例については、<bpt id="p1">**</bpt>CustTableLookup<ept id="p1">**</ept> フォームを参照してください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="144">
          <source>Step 4</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ステップ 4</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="145">
          <source>Dynamics AX 2012</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Dynamics AX 2012</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="146">
          <source>Dynamics AX for Operations</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Dynamics AX for Operations</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="147">
          <source>Because this method only calls the <bpt id="p1">**</bpt>segmentValueChanged()<ept id="p1">**</ept> method on the control and doesn't perform any additional processing, you can delete it.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このメソッドはコントロールの <bpt id="p1">**</bpt>segmentValueChanged()<ept id="p1">**</ept> メソッドのみを呼び出し追加の処理は実行しないため、削除できます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="148">
          <source>Step 5</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ステップ 5</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="149">
          <source>Dynamics AX 2012</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Dynamics AX 2012</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="150">
          <source>Dynamics AX for Operations</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Dynamics AX for Operations</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="151">
          <source>Because this method only calls the <bpt id="p1">**</bpt>validate()<ept id="p1">**</ept> method on the control and doesn't perform any additional processing, you can delete it.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このメソッドはコントロールの <bpt id="p1">**</bpt>validate()<ept id="p1">**</ept> メソッドのみを呼び出し追加の処理は実行しないため、削除できます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="152">
          <source>Controller variable declarations</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">コントローラー変数申告</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="153">
          <source>Dynamics AX 2012</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Dynamics AX 2012</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="154">
          <source>Finally, go back to the first TODO, for the controller variable declaration.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">最後に、コントローラー変数申告のため、最初の TODO に戻ります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="155">
          <source>Dynamics AX for Operations</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Dynamics AX for Operations</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="156">
          <source>The <bpt id="p1">**</bpt>dimDynamicAccountController<ept id="p1">**</ept> variable is no longer used on the form.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>dimDynamicAccountController<ept id="p1">**</ept> 変数は、フォームで使用されなくなりました。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="157">
          <source>Therefore, you can now delete it.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">したがって、削除できるようになりました。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="158">
          <source>Complex migration scenario – LedgerJournalTransDaily form</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">複雑な移行シナリオ – LedgerJournalTransDaily フォーム</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="159">
          <source>Search for the <bpt id="p1">**</bpt>LedgerJournalTransDaily<ept id="p1">**</ept> form in Application Explorer.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">アプリケーション エクスプローラーで <bpt id="p1">**</bpt>LedgerJournalTransDaily<ept id="p1">**</ept> フォームを検索します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="160">
          <source>Add the form to the current project.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">現在のプロジェクトにフォームを追加します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="161">
          <source>Open the form in the form design view and the code editor view.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">フォーム デザイン ビューとコード エディタ ビューで、フォームを開きます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="162">
          <source>In the form design view, find the SEC, either by manually walking the control tree or by searching for “SegmentedEntry” in the search bar below the <bpt id="p1">**</bpt>File<ept id="p1">**</ept> tab.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">フォーム デザイン ビューで、手動でコントロール ツリーを移動するか、<bpt id="p1">**</bpt>ファイル<ept id="p1">**</ept> タブの下にある検索バーで「SegmentedEntry」を検索して、SEC を見つけます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="163">
          <source>Select the SEC, and verify the following information:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">SEC を選択し、次の情報を確認します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="164">
          <source>The type for the control, as specified in parenthesis next to the control, is <bpt id="p1">**</bpt>SegmentedEntryControl<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">コントロールの横にある括弧で指定されたコントロールのタイプは、<bpt id="p1">**</bpt>SegmentedEntryControl<ept id="p1">**</ept> です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="165">
          <source>The <bpt id="p1">**</bpt>Controller class<ept id="p1">**</ept> property is set to <bpt id="p2">**</bpt>DimensionDynamicAccountController<ept id="p2">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>コントローラー クラス<ept id="p1">**</ept> プロパティは <bpt id="p2">**</bpt>DimensionDynamicAccountController<ept id="p2">**</ept> に設定されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="166">
          <source>This property indicates the type of controller that this instance of the SEC will use.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このプロパティは、SEC のこのインスタンスが使用するコントローラーのタイプを示します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="167">
          <source>The type of controller, in turn, determines the behavior of the control.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">コントローラーのタイプによって、コントロールのビヘイビアーが決まります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="168">
          <source>Switch to the code editor view, and search for all occurrences of “TODO: (Code Upgrade) <ph id="ph1">\[</ph>Segmented entry control<ph id="ph2">\]</ph>” in the form source code.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">コード エディタ ビューに切り替え、フォーム ソース コードで "TODO: (コード アップグレード) <ph id="ph1">\[</ph>セグメント化されたエントリ コントロール<ph id="ph2">\]</ph>" のすべての事例を検索します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="169">
          <source>In the search results, the first three results are for the controller variable declarations.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">検索結果で、最初の 3 件の結果はコントローラー変数申告用です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="170">
          <source>Look at the comments that accompany the TODOs, and make a note of the mapping that shows which SEC instance uses which controller instance.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">"仕事" を添付しているコメントを参照して、どの SEC インスタンスがどのコントローラー インスタンスを使用しているか示すマッピングを記録します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="171">
          <source>You will need this mapping when you replace method calls on the controller with method calls on the control.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このマッピングは、コントローラーでのメソッド呼び出しをコントロールでのメソッド呼び出しに置き換えるときに必要です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="172">
          <source>Here is what the controller-to-control mapping looks like:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">コントローラーからコントロールへのマッピングがどのようなものかを次に示します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="173">
          <source>dimAccountController</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">dimAccountController</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="174">
          <source>LedgerJournalTrans<ph id="ph1">\_</ph>AccountNum</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">LedgerJournalTrans<ph id="ph1">\_</ph>AccountNum</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="175">
          <source>LedgerJournalTrans<ph id="ph1">\_</ph>AccountNum1</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">LedgerJournalTrans<ph id="ph1">\_</ph>AccountNum1</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="176">
          <source>Group4<ph id="ph1">\_</ph>AccountNum</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Group4<ph id="ph1">\_</ph>AccountNum</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="177">
          <source>dimOffsetAccountController</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">dimOffsetAccountController</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="178">
          <source>GridOffsetAccount</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">GridOffsetAccount</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="179">
          <source>LedgerJournalTrans<ph id="ph1">\_</ph>OffsetAccount1</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">LedgerJournalTrans<ph id="ph1">\_</ph>OffsetAccount1</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="180">
          <source>Group4<ph id="ph1">\_</ph>OffsetAccount</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Group4<ph id="ph1">\_</ph>OffsetAccount</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="181">
          <source>dimPaymentFeeAccountController</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">dimPaymentFeeAccountController</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="182">
          <source>CustPaymJournalFee<ph id="ph1">\_</ph>CustAccount</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">CustPaymJournalFee<ph id="ph1">\_</ph>CustAccount</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="183">
          <source>You will fix these three TODO comments at the end, after you've removed all references to the controller variables.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">コントローラー変数へのすべての参照を削除した後、最後に、これらの 3 つの TODO コメントを修正します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="184">
          <source>Go through each of the remaining TODO comments, as described in the following subsections.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">次のサブセクションでの説明にあるように、残りの各 TODO コメントが実行されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="185">
          <source>LedgerDimension data field</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">LedgerDimension データ フィールド</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="186">
          <source>(<bpt id="p1">**</bpt>Form<ept id="p1">**</ept> <ph id="ph1">&amp;gt;</ph> <bpt id="p2">**</bpt>Data sources<ept id="p2">**</ept> <ph id="ph2">&amp;gt;</ph> <bpt id="p3">**</bpt>LedgerJournalTrans<ept id="p3">**</ept> <ph id="ph3">&amp;gt;</ph> <bpt id="p4">**</bpt>Fields<ept id="p4">**</ept> <ph id="ph4">&amp;gt;</ph> <bpt id="p5">**</bpt>LedgerDimension<ept id="p5">**</ept> <ph id="ph5">&amp;gt;</ph> <bpt id="p6">**</bpt>Methods<ept id="p6">**</ept>)</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">(<bpt id="p1">**</bpt>フォーム<ept id="p1">**</ept><ph id="ph1">&amp;gt;</ph><bpt id="p2">**</bpt>データ ソース<ept id="p2">**</ept> <ph id="ph2">&amp;gt;</ph><bpt id="p3">**</bpt>LedgerJournalTrans<ept id="p3">**</ept><ph id="ph3">&amp;gt;</ph> <bpt id="p4">**</bpt>フィールド<ept id="p4">**</ept> <ph id="ph4">&amp;gt;</ph><bpt id="p5">**</bpt>LedgerDimension<ept id="p5">**</ept><ph id="ph5">&amp;gt;</ph>  <bpt id="p6">**</bpt>方法<ept id="p6">**</ept>)</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="187">
          <source>Dynamics AX 2012</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Dynamics AX 2012</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="188">
          <source>Dynamics AX for Operations</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Dynamics AX for Operations</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="189">
          <source>Because this method only calls the <bpt id="p1">**</bpt>jumpRef()<ept id="p1">**</ept> method on the control and doesn't perform any additional processing, you can delete it.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このメソッドはコントロールの <bpt id="p1">**</bpt>jumpRef()<ept id="p1">**</ept> メソッドのみを呼び出し追加の処理は実行しないため、削除できます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="190">
          <source>OffsetLedgerDimension data field</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">OffsetLedgerDimension データ フィールド</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="191">
          <source>(<bpt id="p1">**</bpt>Form<ept id="p1">**</ept> <ph id="ph1">&amp;gt;</ph> <bpt id="p2">**</bpt>Data sources<ept id="p2">**</ept> <ph id="ph2">&amp;gt;</ph> <bpt id="p3">**</bpt>LedgerJournalTrans<ept id="p3">**</ept> <ph id="ph3">&amp;gt;</ph> <bpt id="p4">**</bpt>Fields<ept id="p4">**</ept> <ph id="ph4">&amp;gt;</ph> <bpt id="p5">**</bpt>OffsetLedgerDimension<ept id="p5">**</ept> <ph id="ph5">&amp;gt;</ph> <bpt id="p6">**</bpt>Methods<ept id="p6">**</ept>)</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">(<bpt id="p1">**</bpt>フォーム<ept id="p1">**</ept><ph id="ph1">&amp;gt;</ph><bpt id="p2">**</bpt>データ ソース<ept id="p2">**</ept> <ph id="ph2">&amp;gt;</ph><bpt id="p3">**</bpt>LedgerJournalTrans<ept id="p3">**</ept><ph id="ph3">&amp;gt;</ph> <bpt id="p4">**</bpt>フィールド<ept id="p4">**</ept> <ph id="ph4">&amp;gt;</ph><bpt id="p5">**</bpt>OffsetLedgerDimension<ept id="p5">**</ept><ph id="ph5">&amp;gt;</ph> <bpt id="p6">**</bpt>方法<ept id="p6">**</ept>)</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="192">
          <source>Dynamics AX 2012</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Dynamics AX 2012</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="193">
          <source>The <bpt id="p1">**</bpt>OffsetLedgerDimension<ept id="p1">**</ept> field’s <bpt id="p2">**</bpt>jumpRef()<ept id="p2">**</ept> method:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>OffsetLedgerDimension<ept id="p1">**</ept> フィールドの <bpt id="p2">**</bpt>jumpRef()<ept id="p2">**</ept> メソッド。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="194">
          <source>Dynamics AX for Operations</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Dynamics AX for Operations</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="195">
          <source>Because this method only calls the <bpt id="p1">**</bpt>jumpRef()<ept id="p1">**</ept> method on the control and doesn't perform any additional processing, you can delete it.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このメソッドはコントロールの <bpt id="p1">**</bpt>jumpRef()<ept id="p1">**</ept> メソッドのみを呼び出し追加の処理は実行しないため、削除できます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="196">
          <source>LedgerJournalTrans<ph id="ph1">\_</ph>AccountNum control</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">LedgerJournalTrans<ph id="ph1">\_</ph>AccountNum コントロール</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="197">
          <source>(Search for "LedgerJournalTrans<ph id="ph1">\_</ph>AccountNum" in the search bar below the <bpt id="p1">**</bpt>Form<ept id="p1">**</ept> tab.)</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">(<bpt id="p1">**</bpt>フォーム<ept id="p1">**</ept>タブの下にある検索バーで、「LedgerJournalTrans<ph id="ph1">\_</ph>AccountNum」を検索してください。)</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="198">
          <source>Step 1</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ステップ１</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="199">
          <source>Dynamics AX 2012</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Dynamics AX 2012</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="200">
          <source>Dynamics AX for Operations</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Dynamics AX for Operations</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="201">
          <source>Because this method only calls the <bpt id="p1">**</bpt>jumpRef()<ept id="p1">**</ept> method on the control and doesn't perform any additional processing, you can delete it.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このメソッドはコントロールの <bpt id="p1">**</bpt>jumpRef()<ept id="p1">**</ept> メソッドのみを呼び出し追加の処理は実行しないため、削除できます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="202">
          <source>Step 2</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ステップ２</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="203">
          <source>Dynamics AX 2012</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Dynamics AX 2012</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="204">
          <source>Dynamics AX for Operations</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Dynamics AX for Operations</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="205">
          <source>Update the <bpt id="p1">**</bpt>initLedger()<ept id="p1">**</ept> method.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>initLedger()<ept id="p1">**</ept> メソッドを更新します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="206">
          <source>Update the code in the <bpt id="p1">**</bpt>LedgerJournalTrans<ept id="p1">**</ept> data source’s <bpt id="p2">**</bpt>active()<ept id="p2">**</ept> method.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>LedgerJournalTrans<ept id="p1">**</ept> データ ソースの <bpt id="p2">**</bpt>active()<ept id="p2">**</ept> メソッドでコードを更新します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="207">
          <source><bpt id="p1">**</bpt>Note:<ept id="p1">**</ept> The <bpt id="p2">**</bpt>getValue()<ept id="p2">**</ept> method should be called only if the account type is set to <bpt id="p3">**</bpt>Ledger<ept id="p3">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>注記:<ept id="p1">**</ept> <bpt id="p2">**</bpt>getValue()<ept id="p2">**</ept> メソッドは、勘定タイプが<bpt id="p3">**</bpt>元帳<ept id="p3">**</ept>に設定されている場合にのみ呼び出す必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="208">
          <source>Otherwise, a call to this method will cause an invalid function call.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">それ以外の場合、このメソッドを呼び出すと、無効な関数呼び出しが発生します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="209">
          <source>Add the following code to the <bpt id="p1">**</bpt>modified()<ept id="p1">**</ept> method of the <bpt id="p2">**</bpt>LedgerJournalTrans<ept id="p2">**</ept> data source’s <bpt id="p3">**</bpt>CurrencyCode<ept id="p3">**</ept> field.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p2">**</bpt>LedgerJournalTrans<ept id="p2">**</ept> データ ソースの <bpt id="p3">**</bpt>CurrencyCode<ept id="p3">**</ept> フィールドの <bpt id="p1">**</bpt>modified()<ept id="p1">**</ept> メソッドに、次のコードを追加します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="210">
          <source>Add the following code to the <bpt id="p1">**</bpt>modified()<ept id="p1">**</ept> method of the <bpt id="p2">**</bpt>LedgerJournalTrans<ept id="p2">**</ept> data source’s <bpt id="p3">**</bpt>Company<ept id="p3">**</ept> field.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p2">**</bpt>LedgerJournalTrans<ept id="p2">**</ept> データ ソースの <bpt id="p3">**</bpt>Company<ept id="p3">**</ept> フィールドの <bpt id="p1">**</bpt>modified()<ept id="p1">**</ept> メソッドに、次のコードを追加します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="211">
          <source>Add the following code to the <bpt id="p1">**</bpt>modified()<ept id="p1">**</ept> method of the <bpt id="p2">**</bpt>LedgerJournalTrans<ept id="p2">**</ept> data source’s <bpt id="p3">**</bpt>TransDate<ept id="p3">**</ept> field.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p2">**</bpt>LedgerJournalTrans<ept id="p2">**</ept> データ ソースの <bpt id="p3">**</bpt>TransDate<ept id="p3">**</ept> フィールドの <bpt id="p1">**</bpt>modified()<ept id="p1">**</ept> メソッドに、次のコードを追加します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="212">
          <source>Delete the <bpt id="p1">**</bpt>loadSegments()<ept id="p1">**</ept> method.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>loadSegments()<ept id="p1">**</ept> メソッドを削除します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="213">
          <source>Step 3</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ステップ 3</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="214">
          <source>Dynamics AX 2012</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Dynamics AX 2012</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="215">
          <source>Dynamics AX for Operations</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Dynamics AX for Operations</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="216">
          <source>This method implements a custom lookup for the control.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このメソッドは、コントロールのカスタム ルックアップを実装します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="217">
          <source>Therefore, leave the method as it is.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">したがって、メソッドをそのままにします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="218">
          <source>Just remove the TODO.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">"仕事" を削除します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="219">
          <source>To hook up custom lookups, you must override the SEC’s <bpt id="p1">**</bpt>checkUseCustomLookup<ept id="p1">**</ept> method.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">カスタムのルックアップをフック アップするには、SEC の <bpt id="p1">**</bpt>checkUseCustomLookup<ept id="p1">**</ept> メソッドをオーバーライドする必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="220">
          <source>Additionally, make sure that the <bpt id="p1">**</bpt>closeSelectRecord<ept id="p1">**</ept> method on the custom lookup form is overridden.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">また、カスタム ルックアップ フォームで <bpt id="p1">**</bpt>closeSelectRecord<ept id="p1">**</ept> メソッドが上書きされたことを確認してください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="221">
          <source>For an example, see the <bpt id="p1">**</bpt>CustTableLookup<ept id="p1">**</ept> form.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">例については、<bpt id="p1">**</bpt>CustTableLookup<ept id="p1">**</ept> フォームを参照してください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="222">
          <source>Step 4</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ステップ 4</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="223">
          <source>Dynamics AX 2012</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Dynamics AX 2012</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="224">
          <source>Dynamics AX for Operations</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Dynamics AX for Operations</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="225">
          <source>Override the <bpt id="p1">**</bpt>onSegmentChanged()<ept id="p1">**</ept> method on the control, and add the following code to it.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">コントロールの <bpt id="p1">**</bpt>onSegmentChanged()<ept id="p1">**</ept> メソッドをオーバーライドし、次のコードを追加します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="226">
          <source>Delete the <bpt id="p1">**</bpt>segmentValueChanged()<ept id="p1">**</ept> method.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>segmentValueChanged()<ept id="p1">**</ept> メソッドを削除します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="227">
          <source><bpt id="p1">**</bpt>Note:<ept id="p1">**</ept> The preceding code for the <bpt id="p2">**</bpt>onSegmentChanged()<ept id="p2">**</ept> method will not compile, because the <bpt id="p3">**</bpt>onPrimaryAccountSegmentChanged()<ept id="p3">**</ept> method expects a controller object, but this code passes an instance of the SEC.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>注記:<ept id="p1">**</ept> <bpt id="p3">**</bpt>onPrimaryAccountSegmentChanged()<ept id="p3">**</ept> メソッドでは、コントローラー オブジェクトが必要ですが、このコードは SEC のインスタンスを渡すので、<bpt id="p2">**</bpt>onSegmentChanged()<ept id="p2">**</ept> メソッドの前のコードはコンパイルされません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="228">
          <source>To call methods on the control instance, you must change the method’s signature and its implementation accordingly.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">コントロール インスタンスでメソッドを呼び出すには、メソッドのシグネチャとその実装を適宜変更する必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="229">
          <source>This method is used by more than 50 callers.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このメソッドは、50 以上の呼び出し元が使用されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="230">
          <source>Therefore, you would also have to update all those calls.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">したがって、これらの呼び出しをすべて更新する必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="231">
          <source>Alternatively, you can add a new method that follows this guidance.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">または、このガイダンスに従うことによって新しいメソッドを追加できます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="232">
          <source>Step 5</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ステップ 5</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="233">
          <source>Dynamics AX 2012</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Dynamics AX 2012</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="234">
          <source>Dynamics AX for Operations</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Dynamics AX for Operations</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="235">
          <source>Because this method only calls the <bpt id="p1">**</bpt>validate()<ept id="p1">**</ept> method on the control and doesn't perform any additional processing, you can delete it.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このメソッドはコントロールの <bpt id="p1">**</bpt>validate()<ept id="p1">**</ept> メソッドのみを呼び出し追加の処理は実行しないため、削除できます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="236">
          <source>GridOffsetAccount control</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">GridOffsetAccount コントロール</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="237">
          <source>(Search for "GridOffsetAccount" in the search bar below the <bpt id="p1">**</bpt>Form<ept id="p1">**</ept> tab.)</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">(<bpt id="p1">**</bpt>フォーム<ept id="p1">**</ept>タブの下にある「GridOffsetAccount」を検索してください。)</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="238">
          <source>Step 1</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ステップ１</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="239">
          <source>Dynamics AX 2012</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Dynamics AX 2012</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="240">
          <source>Dynamics AX for Operations</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Dynamics AX for Operations</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="241">
          <source>Add the following code to the <bpt id="p1">**</bpt>initLedger()<ept id="p1">**</ept> method, after the code that updates the ledgerJournalTable buffer.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ledgerJournalTable バッファを更新するコードの後に、<bpt id="p1">**</bpt>initLedger()<ept id="p1">**</ept> メソッドへ次のコードを追加します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="242">
          <source>Delete the <bpt id="p1">**</bpt>gotFocus()<ept id="p1">**</ept> method.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>gotFocus()<ept id="p1">**</ept> メソッドを削除します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="243">
          <source>Step 2</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ステップ２</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="244">
          <source>Dynamics AX 2012</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Dynamics AX 2012</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="245">
          <source>Dynamics AX for Operations</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Dynamics AX for Operations</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="246">
          <source>Because this method only calls the <bpt id="p1">**</bpt>jumpRef()<ept id="p1">**</ept> method on the control and doesn't perform any additional processing, you can delete it.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このメソッドはコントロールの <bpt id="p1">**</bpt>jumpRef()<ept id="p1">**</ept> メソッドのみを呼び出し追加の処理は実行しないため、削除できます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="247">
          <source>Step 3</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ステップ 3</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="248">
          <source>Dynamics AX 2012</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Dynamics AX 2012</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="249">
          <source>Dynamics AX for Operations</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Dynamics AX for Operations</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="250">
          <source>Update the <bpt id="p1">**</bpt>initLedger()<ept id="p1">**</ept> method.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>initLedger()<ept id="p1">**</ept> メソッドを更新します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="251">
          <source><bpt id="p1">**</bpt>Note:<ept id="p1">**</ept> The <bpt id="p2">**</bpt>getValue()<ept id="p2">**</ept> method should be called only if the account type is set to <bpt id="p3">**</bpt>Ledger<ept id="p3">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>注記:<ept id="p1">**</ept> <bpt id="p2">**</bpt>getValue()<ept id="p2">**</ept> メソッドは、勘定タイプが<bpt id="p3">**</bpt>元帳<ept id="p3">**</ept>に設定されている場合にのみ呼び出す必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="252">
          <source>Otherwise, a call to this method will cause an invalid function call.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">それ以外の場合、このメソッドを呼び出すと、無効な関数呼び出しが発生します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="253">
          <source>Update the code in the <bpt id="p1">**</bpt>LedgerJournalTrans<ept id="p1">**</ept> data source’s <bpt id="p2">**</bpt>active()<ept id="p2">**</ept> method.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>LedgerJournalTrans<ept id="p1">**</ept> データ ソースの <bpt id="p2">**</bpt>active()<ept id="p2">**</ept> メソッドでコードを更新します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="254">
          <source><bpt id="p1">**</bpt>Note:<ept id="p1">**</ept> The <bpt id="p2">**</bpt>getValue()<ept id="p2">**</ept> method should be called only if the account type is set to <bpt id="p3">**</bpt>Ledger<ept id="p3">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>注記:<ept id="p1">**</ept> <bpt id="p2">**</bpt>getValue()<ept id="p2">**</ept> メソッドは、勘定タイプが<bpt id="p3">**</bpt>元帳<ept id="p3">**</ept>に設定されている場合にのみ呼び出す必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="255">
          <source>Otherwise, a call to this method will cause an invalid function call.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">それ以外の場合、このメソッドを呼び出すと、無効な関数呼び出しが発生します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="256">
          <source>Add the following code to the <bpt id="p1">**</bpt>modified()<ept id="p1">**</ept> method of the <bpt id="p2">**</bpt>LedgerJournalTrans<ept id="p2">**</ept> data source’s <bpt id="p3">**</bpt>CurrencyCode<ept id="p3">**</ept> field.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p2">**</bpt>LedgerJournalTrans<ept id="p2">**</ept> データ ソースの <bpt id="p3">**</bpt>CurrencyCode<ept id="p3">**</ept> フィールドの <bpt id="p1">**</bpt>modified()<ept id="p1">**</ept> メソッドに、次のコードを追加します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="257">
          <source>Add the following code to the <bpt id="p1">**</bpt>modified()<ept id="p1">**</ept> method of the <bpt id="p2">**</bpt>LedgerJournalTrans<ept id="p2">**</ept> data source’s <bpt id="p3">**</bpt>OffsetCompany<ept id="p3">**</ept> field.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p2">**</bpt>LedgerJournalTrans<ept id="p2">**</ept> データ ソースの <bpt id="p3">**</bpt>OffsetCompany<ept id="p3">**</ept> フィールドの <bpt id="p1">**</bpt>modified()<ept id="p1">**</ept> メソッドに、次のコードを追加します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="258">
          <source>Add the following code to the <bpt id="p1">**</bpt>modified()<ept id="p1">**</ept> method of the <bpt id="p2">**</bpt>LedgerJournalTrans<ept id="p2">**</ept> data source’s <bpt id="p3">**</bpt>TransDate<ept id="p3">**</ept> field.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p2">**</bpt>LedgerJournalTrans<ept id="p2">**</ept> データ ソースの <bpt id="p3">**</bpt>TransDate<ept id="p3">**</ept> フィールドの <bpt id="p1">**</bpt>modified()<ept id="p1">**</ept> メソッドに、次のコードを追加します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="259">
          <source>Add the following code to the <bpt id="p1">**</bpt>modified()<ept id="p1">**</ept> method of the <bpt id="p2">**</bpt>LedgerJournalTrans<ept id="p2">**</ept> data source’s <bpt id="p3">**</bpt>OffsetAccountType<ept id="p3">**</ept> field.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p2">**</bpt>LedgerJournalTrans<ept id="p2">**</ept> データ ソースの <bpt id="p3">**</bpt>OffsetAccountType<ept id="p3">**</ept> フィールドの <bpt id="p1">**</bpt>modified()<ept id="p1">**</ept> メソッドに、次のコードを追加します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="260">
          <source><bpt id="p1">**</bpt>Note:<ept id="p1">**</ept> The <bpt id="p2">**</bpt>getValue()<ept id="p2">**</ept> method should be called only if the account type is set to <bpt id="p3">**</bpt>Ledger<ept id="p3">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>注記:<ept id="p1">**</ept> <bpt id="p2">**</bpt>getValue()<ept id="p2">**</ept> メソッドは、勘定タイプが<bpt id="p3">**</bpt>元帳<ept id="p3">**</ept>に設定されている場合にのみ呼び出す必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="261">
          <source>Otherwise, a call to this method cause an invalid function call.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">それ以外の場合、このメソッドを呼び出すと、無効な関数呼び出しが発生します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="262">
          <source>Delete the <bpt id="p1">**</bpt>loadSegments()<ept id="p1">**</ept> method.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>loadSegments()<ept id="p1">**</ept> メソッドを削除します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="263">
          <source>Step 4</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ステップ 4</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="264">
          <source>Dynamics AX 2012</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Dynamics AX 2012</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="265">
          <source>Dynamics AX for Operations</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Dynamics AX for Operations</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="266">
          <source>This method implements a custom lookup for the control.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このメソッドは、コントロールのカスタム ルックアップを実装します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="267">
          <source>Therefore, keep the method, but replace the controller with the control instance.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">したがって、メソッドを保持しますが、コントローラーをコントロール インスタンスに置き換えます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="268">
          <source>In this case, because the method is overridden on the <bpt id="p1">**</bpt>GridOffsetAccount<ept id="p1">**</ept> control, even though <bpt id="p2">**</bpt>dimOffsetAccountController<ept id="p2">**</ept> was used for three different SEC instances (based on the mapping that is shown in the TODOs on controller variable declarations), we must replace the controller with only one SEC instance.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この場合、メソッドは <bpt id="p1">**</bpt>GridOffsetAccount<ept id="p1">**</ept> コントロールでオーバーライドされるため、<bpt id="p2">**</bpt>dimOffsetAccountController<ept id="p2">**</ept> が (コントローラー変数宣言の "仕事" に示されたマッピングに基づいて) 3 つの異なる SEC インスタンスに使用される場合でも、コントローラーをたった 1 つの SEC インスタンスに置き換える必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="269">
          <source>Therefore, the code will look like this.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">したがって、コードは次のようになります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="270">
          <source>To hook up custom lookups, you must override the SEC’s <bpt id="p1">**</bpt>checkUseCustomLookup<ept id="p1">**</ept> method.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">カスタムのルックアップをフック アップするには、SEC の <bpt id="p1">**</bpt>checkUseCustomLookup<ept id="p1">**</ept> メソッドをオーバーライドする必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="271">
          <source>Additionally, make sure that the <bpt id="p1">**</bpt>closeSelectRecord<ept id="p1">**</ept> method on the custom lookup form is overridden.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">また、カスタム ルックアップ フォームで <bpt id="p1">**</bpt>closeSelectRecord<ept id="p1">**</ept> メソッドが上書きされたことを確認してください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="272">
          <source>For an example, see the <bpt id="p1">**</bpt>CustTableLookup<ept id="p1">**</ept> form.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">例については、<bpt id="p1">**</bpt>CustTableLookup<ept id="p1">**</ept> フォームを参照してください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="273">
          <source>Step 5</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ステップ 5</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="274">
          <source>Dynamics AX 2012</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Dynamics AX 2012</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="275">
          <source>Dynamics AX for Operations</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Dynamics AX for Operations</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="276">
          <source>Override the <bpt id="p1">**</bpt>onSegmentChanged()<ept id="p1">**</ept> method on the control, and add the following code to it.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">コントロールの <bpt id="p1">**</bpt>onSegmentChanged()<ept id="p1">**</ept> メソッドをオーバーライドし、次のコードを追加します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="277">
          <source>Delete the <bpt id="p1">**</bpt>segmentValueChanged()<ept id="p1">**</ept> method.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>segmentValueChanged()<ept id="p1">**</ept> メソッドを削除します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="278">
          <source><bpt id="p1">**</bpt>Note:<ept id="p1">**</ept> The preceding code for the <bpt id="p2">**</bpt>onSegmentChanged()<ept id="p2">**</ept> method will not compile, because the <bpt id="p3">**</bpt>onOffsetAccountSegmentChanged()<ept id="p3">**</ept> method expects a controller object, but this code passes an instance of the SEC.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>注記:<ept id="p1">**</ept> <bpt id="p3">**</bpt>onOffsetAccountSegmentChanged()<ept id="p3">**</ept> メソッドでは、コントローラー オブジェクトが必要ですが、このコードは SEC のインスタンスを渡すので、<bpt id="p2">**</bpt>onSegmentChanged()<ept id="p2">**</ept> メソッドの前のコードはコンパイルされません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="279">
          <source>To call methods on the control instance, you must change the method’s signature and its implementation accordingly.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">コントロール インスタンスでメソッドを呼び出すには、メソッドのシグネチャとその実装を適宜変更する必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="280">
          <source>This method is used by more than 50 callers.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このメソッドは、50 以上の呼び出し元が使用されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="281">
          <source>Therefore, you would also have to update all those calls.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">したがって、これらの呼び出しをすべて更新する必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="282">
          <source>Alternatively, you can add a new method that follows this guidance.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">または、このガイダンスに従うことによって新しいメソッドを追加できます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="283">
          <source>Step 6</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ステップ 6</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="284">
          <source>Dynamics AX 2012</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Dynamics AX 2012</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="285">
          <source>Dynamics AX for Operations</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Dynamics AX for Operations</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="286">
          <source>Because this method only calls the <bpt id="p1">**</bpt>validate()<ept id="p1">**</ept> method on the control and doesn't perform any additional processing, you can delete it.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このメソッドはコントロールの <bpt id="p1">**</bpt>validate()<ept id="p1">**</ept> メソッドのみを呼び出し追加の処理は実行しないため、削除できます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="287">
          <source>LedgerJournalTrans<ph id="ph1">\_</ph>AccountNum1</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">LedgerJournalTrans<ph id="ph1">\_</ph>AccountNum1</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="288">
          <source>(Search for "LedgerJournalTrans<ph id="ph1">\_</ph>AccountNum1" in the search bar below the <bpt id="p1">**</bpt>Form<ept id="p1">**</ept> tab.)</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">(<bpt id="p1">**</bpt>フォーム<ept id="p1">**</ept>タブの下にある検索バーで、「LedgerJournalTrans<ph id="ph1">\_</ph>AccountNum1」を検索してください。)</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="289">
          <source>Step 1</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ステップ１</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="290">
          <source>Dynamics AX 2012</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Dynamics AX 2012</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="291">
          <source>Dynamics AX for Operations</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Dynamics AX for Operations</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="292">
          <source>Because this method only calls the <bpt id="p1">**</bpt>jumpRef()<ept id="p1">**</ept> method on the control and doesn't perform any additional processing, you can delete it.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このメソッドはコントロールの <bpt id="p1">**</bpt>jumpRef()<ept id="p1">**</ept> メソッドのみを呼び出し追加の処理は実行しないため、削除できます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="293">
          <source>Step 2</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ステップ２</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="294">
          <source>Dynamics AX 2012</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Dynamics AX 2012</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="295">
          <source>Dynamics AX for Operations</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Dynamics AX for Operations</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="296">
          <source>The steps for migrating this method are the same as the steps for migrating the <bpt id="p1">**</bpt>LedgerJournalTrans<ph id="ph1">\_</ph>AccountNum.loadSegments()<ept id="p1">**</ept> method.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このメソッドを移行する手順は、<bpt id="p1">**</bpt>LedgerJournalTrans<ph id="ph1">\_</ph>AccountNum.loadSegments()<ept id="p1">**</ept> メソッドを移行する手順と同じです。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="297">
          <source>Therefore, no additional steps are required.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">したがって、追加の手順は必要はありません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="298">
          <source>Delete this method.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このメソッドを削除します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="299">
          <source>Step 3</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ステップ 3</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="300">
          <source>Dynamics AX 2012</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Dynamics AX 2012</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="301">
          <source>Dynamics AX for Operations</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Dynamics AX for Operations</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="302">
          <source>This method implements a custom lookup for the control.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このメソッドは、コントロールのカスタム ルックアップを実装します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="303">
          <source>Therefore, leave the method as it is.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">したがって、メソッドをそのままにします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="304">
          <source>Just remove the TODO.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">"仕事" を削除します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="305">
          <source>To hook up custom lookups, you must override the SEC’s <bpt id="p1">**</bpt>checkUseCustomLookup<ept id="p1">**</ept> method.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">カスタムのルックアップをフック アップするには、SEC の <bpt id="p1">**</bpt>checkUseCustomLookup<ept id="p1">**</ept> メソッドをオーバーライドする必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="306">
          <source>Additionally, make sure that the <bpt id="p1">**</bpt>closeSelectRecord<ept id="p1">**</ept> method on the custom lookup is overridden.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">また、カスタム ルックアップで <bpt id="p1">**</bpt>closeSelectRecord<ept id="p1">**</ept> メソッドが上書きされたことを確認してください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="307">
          <source>For an example, see the <bpt id="p1">**</bpt>CustTableLookup<ept id="p1">**</ept> form.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">例については、<bpt id="p1">**</bpt>CustTableLookup<ept id="p1">**</ept> フォームを参照してください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="308">
          <source>Step 4</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ステップ 4</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="309">
          <source>Dynamics AX 2012</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Dynamics AX 2012</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="310">
          <source>Dynamics AX for Operations</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Dynamics AX for Operations</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="311">
          <source>Override the <bpt id="p1">**</bpt>onSegmentChanged()<ept id="p1">**</ept> method on the control, and add the following code to it.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">コントロールの <bpt id="p1">**</bpt>onSegmentChanged()<ept id="p1">**</ept> メソッドをオーバーライドし、次のコードを追加します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="312">
          <source>Delete the <bpt id="p1">**</bpt>segmentValueChanged()<ept id="p1">**</ept> method.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>segmentValueChanged()<ept id="p1">**</ept> メソッドを削除します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="313">
          <source><bpt id="p1">**</bpt>Note:<ept id="p1">**</ept> The preceding code for the <bpt id="p2">**</bpt>onSegmentChanged()<ept id="p2">**</ept> method will not compile, because the <bpt id="p3">**</bpt>onPrimaryAccountSegmentChanged()<ept id="p3">**</ept> method expects a controller object, but this code passes an instance of the SEC.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>注記:<ept id="p1">**</ept> <bpt id="p3">**</bpt>onPrimaryAccountSegmentChanged()<ept id="p3">**</ept> メソッドでは、コントローラー オブジェクトが必要ですが、このコードは SEC のインスタンスを渡すので、<bpt id="p2">**</bpt>onSegmentChanged()<ept id="p2">**</ept> メソッドの前のコードはコンパイルされません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="314">
          <source>To call methods on the control instance, you must change the method’s signature and its implementation accordingly.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">コントロール インスタンスでメソッドを呼び出すには、メソッドのシグネチャとその実装を適宜変更する必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="315">
          <source>This method is used by more than 50 callers.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このメソッドは、50 以上の呼び出し元が使用されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="316">
          <source>Therefore, you would also have to update all of those calls.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">したがって、これらの呼び出しをすべて更新する必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="317">
          <source>Alternatively, you can add a new method that follows this guidance.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">または、このガイダンスに従うことによって新しいメソッドを追加できます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="318">
          <source>Step 5</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ステップ 5</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="319">
          <source>Dynamics AX 2012</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Dynamics AX 2012</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="320">
          <source>Dynamics AX for Operations</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Dynamics AX for Operations</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="321">
          <source>Because this method only calls the <bpt id="p1">**</bpt>validate()<ept id="p1">**</ept> method on the control and doesn't perform any additional processing, you can delete it.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このメソッドはコントロールの <bpt id="p1">**</bpt>validate()<ept id="p1">**</ept> メソッドのみを呼び出し追加の処理は実行しないため、削除できます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="322">
          <source>LedgerJournalTrans<ph id="ph1">\_</ph>OffsetAccount1</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">LedgerJournalTrans<ph id="ph1">\_</ph>OffsetAccount1</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="323">
          <source>(Search for "LedgerJournalTrans<ph id="ph1">\_</ph>OffsetAccount1" in the search bar below the <bpt id="p1">**</bpt>Form<ept id="p1">**</ept> tab.)</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">(<bpt id="p1">**</bpt>フォーム<ept id="p1">**</ept>タブの下にある検索バーで、「LedgerJournalTrans<ph id="ph1">\_</ph>OffsetAccount1」を検索してください。)</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="324">
          <source>Step 1</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ステップ１</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="325">
          <source>Dynamics AX 2012</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Dynamics AX 2012</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="326">
          <source>Dynamics AX for Operations</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Dynamics AX for Operations</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="327">
          <source>Because this method only calls the <bpt id="p1">**</bpt>jumpRef()<ept id="p1">**</ept> method on the control and doesn't perform any additional processing, you can delete it.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このメソッドはコントロールの <bpt id="p1">**</bpt>jumpRef()<ept id="p1">**</ept> メソッドのみを呼び出し追加の処理は実行しないため、削除できます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="328">
          <source>Step 2</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ステップ２</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="329">
          <source>Dynamics AX 2012</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Dynamics AX 2012</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="330">
          <source>Dynamics AX for Operations</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Dynamics AX for Operations</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="331">
          <source>The migration steps for the <bpt id="p1">**</bpt>GridOffsetAccount.loadSegments()<ept id="p1">**</ept> method already made most of the changes that are required for this method.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>GridOffsetAccount.loadSegments()<ept id="p1">**</ept> メソッドの移行手順は、すでにこのメソッドに必要な変更のほとんどを行いました。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="332">
          <source>However, you must still make the following changes.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ただし、次の変更を加える必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="333">
          <source>Add a line of code to the <bpt id="p1">**</bpt>LedgerJournalTrans<ept id="p1">**</ept> data source’s <bpt id="p2">**</bpt>active<ept id="p2">**</ept> method.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>LedgerJournalTrans<ept id="p1">**</ept> データ ソースの<bpt id="p2">**</bpt>有効な<ept id="p2">**</ept>メソッドにコード行を追加します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="334">
          <source>Make the same change in the <bpt id="p1">**</bpt>modified()<ept id="p1">**</ept> method of the <bpt id="p2">**</bpt>LedgerJournalTrans<ept id="p2">**</ept> data source’s <bpt id="p3">**</bpt>OffsetAccountType<ept id="p3">**</ept> field.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p2">**</bpt>LedgerJournalTrans<ept id="p2">**</ept> データ ソースの <bpt id="p3">**</bpt>OffsetAccountType<ept id="p3">**</ept> フィールドの <bpt id="p1">**</bpt>modified()<ept id="p1">**</ept> メソッドで同じ変更を行います。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="335">
          <source>Make the same change in the <bpt id="p1">**</bpt>initLedger()<ept id="p1">**</ept> method.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>initLedger()<ept id="p1">**</ept> メソッドで同じ変更を行います。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="336">
          <source>Delete the <bpt id="p1">**</bpt>loadSegments()<ept id="p1">**</ept> method.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>loadSegments()<ept id="p1">**</ept> メソッドを削除します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="337">
          <source>Step 3</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ステップ 3</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="338">
          <source>Dynamics AX 2012</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Dynamics AX 2012</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="339">
          <source>Dynamics AX for Operations</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Dynamics AX for Operations</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="340">
          <source>This method implements a custom lookup for the control.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このメソッドは、コントロールのカスタム ルックアップを実装します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="341">
          <source>Therefore, keep the method, but replace the controller with the control instance.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">したがって、メソッドを保持しますが、コントローラーをコントロール インスタンスに置き換えます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="342">
          <source>In this case, because the method is overridden on the <bpt id="p1">**</bpt>LedgerJournalTrans<ph id="ph1">\_</ph>OffsetAccount1<ept id="p1">**</ept> control, even though <bpt id="p2">**</bpt>dimOffsetAccountController<ept id="p2">**</ept> was used for three different SEC instances (based on the mapping that is shown in the TODOs on controller variable declarations), we must replace the controller with only one SEC instance.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この場合、メソッドは <bpt id="p1">**</bpt>LedgerJournalTrans<ph id="ph1">\_</ph>OffsetAccount1<ept id="p1">**</ept> コントロールでオーバーライドされるため、<bpt id="p2">**</bpt>dimOffsetAccountController<ept id="p2">**</ept> が (コントローラー変数宣言の "仕事" に示されたマッピングに基づいて) 3 つの異なる SEC インスタンスに使用される場合でも、コントローラーをたった 1 つの SEC インスタンスに置き換える必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="343">
          <source>Therefore, the code will look like this.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">したがって、コードは次のようになります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="344">
          <source>To hook up custom lookups, you must override the SEC’s <bpt id="p1">**</bpt>checkUseCustomLookup<ept id="p1">**</ept> method.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">カスタムのルックアップをフック アップするには、SEC の <bpt id="p1">**</bpt>checkUseCustomLookup<ept id="p1">**</ept> メソッドをオーバーライドする必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="345">
          <source>Additionally, make sure that the <bpt id="p1">**</bpt>closeSelectRecord<ept id="p1">**</ept> method on the custom lookup form is overridden.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">また、カスタム ルックアップ フォームで <bpt id="p1">**</bpt>closeSelectRecord<ept id="p1">**</ept> メソッドが上書きされたことを確認してください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="346">
          <source>For an example, see the <bpt id="p1">**</bpt>CustTableLookup<ept id="p1">**</ept> form.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">例については、<bpt id="p1">**</bpt>CustTableLookup<ept id="p1">**</ept> フォームを参照してください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="347">
          <source>Step 4</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ステップ 4</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="348">
          <source>Dynamics AX 2012</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Dynamics AX 2012</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="349">
          <source>Dynamics AX for Operations</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Dynamics AX for Operations</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="350">
          <source>Override the <bpt id="p1">**</bpt>onSegmentChanged()<ept id="p1">**</ept> method on the control, and add the following code to it.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">コントロールの <bpt id="p1">**</bpt>onSegmentChanged()<ept id="p1">**</ept> メソッドをオーバーライドし、次のコードを追加します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="351">
          <source>Delete the <bpt id="p1">**</bpt>segmentValueChanged()<ept id="p1">**</ept> method.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>segmentValueChanged()<ept id="p1">**</ept> メソッドを削除します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="352">
          <source><bpt id="p1">**</bpt>Note:<ept id="p1">**</ept> The preceding code for the <bpt id="p2">**</bpt>onSegmentChanged()<ept id="p2">**</ept> method will not compile, because the <bpt id="p3">**</bpt>onOffsetAccountSegmentChanged()<ept id="p3">**</ept> method expects a controller object, but this code passes an instance of the SEC.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>注記:<ept id="p1">**</ept> <bpt id="p3">**</bpt>onOffsetAccountSegmentChanged()<ept id="p3">**</ept> メソッドでは、コントローラー オブジェクトが必要ですが、このコードは SEC のインスタンスを渡すので、<bpt id="p2">**</bpt>onSegmentChanged()<ept id="p2">**</ept> メソッドの前のコードはコンパイルされません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="353">
          <source>To call methods on the control instance, you must change the method’s signature and its implementation accordingly.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">コントロール インスタンスでメソッドを呼び出すには、メソッドのシグネチャとその実装を適宜変更する必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="354">
          <source>This method is used by more than 50 callers.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このメソッドは、50 以上の呼び出し元が使用されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="355">
          <source>Therefore, you would also have to update all those calls.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">したがって、これらの呼び出しをすべて更新する必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="356">
          <source>Alternatively, you can add a new method that follows this guidance.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">または、このガイダンスに従うことによって新しいメソッドを追加できます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="357">
          <source>Step 5</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ステップ 5</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="358">
          <source>Dynamics AX 2012</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Dynamics AX 2012</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="359">
          <source>Dynamics AX for Operations</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Dynamics AX for Operations</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="360">
          <source>Because this method only calls the <bpt id="p1">**</bpt>validate()<ept id="p1">**</ept> method on the control and doesn't perform any additional processing, you can delete it.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このメソッドはコントロールの <bpt id="p1">**</bpt>validate()<ept id="p1">**</ept> メソッドのみを呼び出し追加の処理は実行しないため、削除できます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="361">
          <source>CustPaymJournalFee<ph id="ph1">\_</ph>CustAccount</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">CustPaymJournalFee<ph id="ph1">\_</ph>CustAccount</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="362">
          <source>(Search for "CustPaymJournalFee<ph id="ph1">\_</ph>CustAccount" in the search bar below the <bpt id="p1">**</bpt>Form<ept id="p1">**</ept> tab.)</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">(<bpt id="p1">**</bpt>フォーム<ept id="p1">**</ept>タブの下にある検索バーで、「CustPaymJournalFee<ph id="ph1">\_</ph>CustAccount」を検索してください。)</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="363">
          <source>Step 1</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ステップ１</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="364">
          <source>Dynamics AX 2012</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Dynamics AX 2012</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="365">
          <source>Dynamics AX for Operations</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Dynamics AX for Operations</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="366">
          <source>Because this method only calls the <bpt id="p1">**</bpt>jumpRef()<ept id="p1">**</ept> method on the control and doesn't perform any additional processing, you can delete it.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このメソッドはコントロールの <bpt id="p1">**</bpt>jumpRef()<ept id="p1">**</ept> メソッドのみを呼び出し追加の処理は実行しないため、削除できます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="367">
          <source>Step 2</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ステップ２</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="368">
          <source>Dynamics AX 2012</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Dynamics AX 2012</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="369">
          <source>Dynamics AX for Operations</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Dynamics AX for Operations</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="370">
          <source>Update the <bpt id="p1">**</bpt>initLedger()<ept id="p1">**</ept> method.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>initLedger()<ept id="p1">**</ept> メソッドを更新します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="371">
          <source>Add the following code to the <bpt id="p1">**</bpt>CustVendPaymJournalFee<ept id="p1">**</ept> data source’s <bpt id="p2">**</bpt>active()<ept id="p2">**</ept> method.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>CustVendPaymJournalFee<ept id="p1">**</ept> データ ソースの <bpt id="p2">**</bpt>active()<ept id="p2">**</ept> メソッドに、次のコードを追加します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="372">
          <source><bpt id="p1">**</bpt>Note:<ept id="p1">**</ept> The method doesn't exist, so you must override it.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>注記:<ept id="p1">**</ept> このメソッドは存在しないため、上書きする必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="373">
          <source>Add the following code to the <bpt id="p1">**</bpt>modified()<ept id="p1">**</ept> method of the <bpt id="p2">**</bpt>CustVendPaymJournalFee<ept id="p2">**</ept> data source’s <bpt id="p3">**</bpt>FeeCurrency<ept id="p3">**</ept> field.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p2">**</bpt>CustVendPaymJournalFee<ept id="p2">**</ept> データ ソースの <bpt id="p3">**</bpt>FeeCurrency<ept id="p3">**</ept> フィールドの <bpt id="p1">**</bpt>modified()<ept id="p1">**</ept> メソッドに、次のコードを追加します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="374">
          <source><bpt id="p1">**</bpt>Note:<ept id="p1">**</ept> The method doesn't exist, so you must override it.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>注記:<ept id="p1">**</ept> このメソッドは存在しないため、上書きする必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="375">
          <source>Add the following code to the <bpt id="p1">**</bpt>LedgerJournalTrans<ept id="p1">**</ept> data source’s <bpt id="p2">**</bpt>active()<ept id="p2">**</ept> method.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>LedgerJournalTrans<ept id="p1">**</ept> データ ソースの <bpt id="p2">**</bpt>active()<ept id="p2">**</ept> メソッドに、次のコードを追加します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="376">
          <source>Add the following code to the <bpt id="p1">**</bpt>modified()<ept id="p1">**</ept> method of the <bpt id="p2">**</bpt>LedgerJournalTrans<ept id="p2">**</ept> data source’s <bpt id="p3">**</bpt>TransDate<ept id="p3">**</ept> field.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p2">**</bpt>LedgerJournalTrans<ept id="p2">**</ept> データ ソースの <bpt id="p3">**</bpt>TransDate<ept id="p3">**</ept> フィールドの <bpt id="p1">**</bpt>modified()<ept id="p1">**</ept> メソッドに、次のコードを追加します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="377">
          <source>Delete the <bpt id="p1">**</bpt>loadSegments()<ept id="p1">**</ept> method.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>loadSegments()<ept id="p1">**</ept> メソッドを削除します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="378">
          <source>Step 3</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ステップ 3</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="379">
          <source>Dynamics AX 2012</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Dynamics AX 2012</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="380">
          <source>Dynamics AX for Operations</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Dynamics AX for Operations</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="381">
          <source>This method implements a custom lookup for the control.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このメソッドは、コントロールのカスタム ルックアップを実装します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="382">
          <source>Therefore, leave the method as it is.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">したがって、メソッドをそのままにします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="383">
          <source>Just remove the TODO.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">"仕事" を削除します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="384">
          <source>To hook up custom lookups, you must override the SEC’s <bpt id="p1">**</bpt>checkUseCustomLookup<ept id="p1">**</ept> method.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">カスタムのルックアップをフック アップするには、SEC の <bpt id="p1">**</bpt>checkUseCustomLookup<ept id="p1">**</ept> メソッドをオーバーライドする必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="385">
          <source>Here is an example.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">次に例を示します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="386">
          <source>Additionally, make sure that the <bpt id="p1">**</bpt>closeSelectRecord<ept id="p1">**</ept> method on the custom lookup form is overridden.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">また、カスタム ルックアップ フォームで <bpt id="p1">**</bpt>closeSelectRecord<ept id="p1">**</ept> メソッドが上書きされたことを確認してください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="387">
          <source>For an example, see the <bpt id="p1">**</bpt>CustTableLookup<ept id="p1">**</ept> form.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">例については、<bpt id="p1">**</bpt>CustTableLookup<ept id="p1">**</ept> フォームを参照してください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="388">
          <source>Step 4</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ステップ 4</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="389">
          <source>Dynamics AX 2012</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Dynamics AX 2012</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="390">
          <source>Dynamics AX for Operations</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Dynamics AX for Operations</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="391">
          <source>Override the <bpt id="p1">**</bpt>onSegmentChanged()<ept id="p1">**</ept> method on the control, and add the following code to it.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">コントロールの <bpt id="p1">**</bpt>onSegmentChanged()<ept id="p1">**</ept> メソッドをオーバーライドし、次のコードを追加します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="392">
          <source>Delete the <bpt id="p1">**</bpt>segmentValueChanged()<ept id="p1">**</ept> method.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>segmentValueChanged()<ept id="p1">**</ept> メソッドを削除します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="393">
          <source><bpt id="p1">**</bpt>Note:<ept id="p1">**</ept> The preceding code for the <bpt id="p2">**</bpt>onSegmentChanged()<ept id="p2">**</ept> method will not compile, because the <bpt id="p3">**</bpt>onPrimaryAccountSegmentChanged()<ept id="p3">**</ept> method expects a controller object, but this code passes an instance of the SEC.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>注記:<ept id="p1">**</ept> <bpt id="p3">**</bpt>onPrimaryAccountSegmentChanged()<ept id="p3">**</ept> メソッドでは、コントローラー オブジェクトが必要ですが、このコードは SEC のインスタンスを渡すので、<bpt id="p2">**</bpt>onSegmentChanged()<ept id="p2">**</ept> メソッドの前のコードはコンパイルされません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="394">
          <source>To call methods on the control instance, you must change the method’s signature and its implementation accordingly.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">コントロール インスタンスでメソッドを呼び出すには、メソッドのシグネチャとその実装を適宜変更する必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="395">
          <source>This method is used by more than 50 callers.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このメソッドは、50 以上の呼び出し元が使用されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="396">
          <source>Therefore, you would also have to update all those calls.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">したがって、これらの呼び出しをすべて更新する必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="397">
          <source>Alternatively, you can add a new method that can follow this guidance.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">または、このガイダンスの指示に従うことによって新しいメソッドを追加することができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="398">
          <source>Step 5</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ステップ 5</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="399">
          <source>Dynamics AX 2012</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Dynamics AX 2012</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="400">
          <source>Dynamics AX for Operations</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Dynamics AX for Operations</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="401">
          <source>Because this method only calls the <bpt id="p1">**</bpt>validate()<ept id="p1">**</ept> method on the control and doesn't perform any additional processing, you can delete it.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このメソッドはコントロールの <bpt id="p1">**</bpt>validate()<ept id="p1">**</ept> メソッドのみを呼び出し追加の処理は実行しないため、削除できます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="402">
          <source>Group4<ph id="ph1">\_</ph>AccountNum</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Group4<ph id="ph1">\_</ph>AccountNum</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="403">
          <source>(Search for "Group4<ph id="ph1">\_</ph>AccountNum" in the search bar below the <bpt id="p1">**</bpt>Form<ept id="p1">**</ept> tab.)</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">(<bpt id="p1">**</bpt>フォーム<ept id="p1">**</ept>タブの下にある検索バーで「Group4<ph id="ph1">\_</ph>AccountNum」を検索してください。)</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="404">
          <source>Step 1</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ステップ１</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="405">
          <source>Dynamics AX 2012</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Dynamics AX 2012</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="406">
          <source>Dynamics AX for Operations</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Dynamics AX for Operations</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="407">
          <source>Because this method only calls the <bpt id="p1">**</bpt>jumpRef()<ept id="p1">**</ept> method on the control and doesn't perform any additional processing, you can delete it.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このメソッドはコントロールの <bpt id="p1">**</bpt>jumpRef()<ept id="p1">**</ept> メソッドのみを呼び出し追加の処理は実行しないため、削除できます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="408">
          <source>Step 2</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ステップ２</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="409">
          <source>Dynamics AX 2012</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Dynamics AX 2012</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="410">
          <source>Dynamics AX for Operations</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Dynamics AX for Operations</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="411">
          <source>The steps for migrating this method are the same as the steps for migrating the <bpt id="p1">**</bpt>LedgerJournalTrans<ph id="ph1">\_</ph>AccountNum.loadSegments()<ept id="p1">**</ept> method.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このメソッドを移行する手順は、<bpt id="p1">**</bpt>LedgerJournalTrans<ph id="ph1">\_</ph>AccountNum.loadSegments()<ept id="p1">**</ept> メソッドを移行する手順と同じです。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="412">
          <source>Therefore, no additional steps are required.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">したがって、追加の手順は必要はありません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="413">
          <source>Delete this method.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このメソッドを削除します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="414">
          <source>Step 3</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ステップ 3</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="415">
          <source>Dynamics AX 2012</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Dynamics AX 2012</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="416">
          <source>Dynamics AX for Operations</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Dynamics AX for Operations</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="417">
          <source>This method implements a custom lookup for the control.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このメソッドは、コントロールのカスタム ルックアップを実装します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="418">
          <source>Therefore, leave the method as it is.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">したがって、メソッドをそのままにします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="419">
          <source>Just remove the TODO.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">"仕事" を削除します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="420">
          <source>To hook up custom lookups, you must override the SEC’s <bpt id="p1">**</bpt>checkUseCustomLookup<ept id="p1">**</ept> method.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">カスタムのルックアップをフック アップするには、SEC の <bpt id="p1">**</bpt>checkUseCustomLookup<ept id="p1">**</ept> メソッドをオーバーライドする必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="421">
          <source>Additionally, make sure that the <bpt id="p1">**</bpt>closeSelectRecord<ept id="p1">**</ept> method on the custom lookup form is overridden.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">また、カスタム ルックアップ フォームで <bpt id="p1">**</bpt>closeSelectRecord<ept id="p1">**</ept> メソッドが上書きされたことを確認してください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="422">
          <source>For an example, see the <bpt id="p1">**</bpt>CustTableLookup<ept id="p1">**</ept> form.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">例については、<bpt id="p1">**</bpt>CustTableLookup<ept id="p1">**</ept> フォームを参照してください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="423">
          <source>Step 4</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ステップ 4</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="424">
          <source>Dynamics AX 2012</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Dynamics AX 2012</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="425">
          <source>Dynamics AX for Operations</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Dynamics AX for Operations</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="426">
          <source>Override the <bpt id="p1">**</bpt>onSegmentChanged()<ept id="p1">**</ept> method on the control, and add the following code to it.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">コントロールの <bpt id="p1">**</bpt>onSegmentChanged()<ept id="p1">**</ept> メソッドをオーバーライドし、次のコードを追加します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="427">
          <source>Delete the <bpt id="p1">**</bpt>segmentValueChanged()<ept id="p1">**</ept> method.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>segmentValueChanged()<ept id="p1">**</ept> メソッドを削除します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="428">
          <source><bpt id="p1">**</bpt>Note:<ept id="p1">**</ept> The preceding code for the <bpt id="p2">**</bpt>onSegmentChanged()<ept id="p2">**</ept> method will not compile, because the <bpt id="p3">**</bpt>onPrimaryAccountSegmentChanged()<ept id="p3">**</ept> method expects a controller object, but this code passes an instance of the SEC.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>注記:<ept id="p1">**</ept> <bpt id="p3">**</bpt>onPrimaryAccountSegmentChanged()<ept id="p3">**</ept> メソッドでは、コントローラー オブジェクトが必要ですが、このコードは SEC のインスタンスを渡すので、<bpt id="p2">**</bpt>onSegmentChanged()<ept id="p2">**</ept> メソッドの前のコードはコンパイルされません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="429">
          <source>To call methods on the control instance, you must change the method’s signature and its implementation accordingly.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">コントロール インスタンスでメソッドを呼び出すには、メソッドのシグネチャとその実装を適宜変更する必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="430">
          <source>This method is used by more than 50 callers.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このメソッドは、50 以上の呼び出し元が使用されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="431">
          <source>Therefore, you would also have to update all those calls.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">したがって、これらの呼び出しをすべて更新する必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="432">
          <source>Alternatively, you can add a new method that follows this guidance.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">または、このガイダンスに従うことによって新しいメソッドを追加できます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="433">
          <source>Step 5</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ステップ 5</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="434">
          <source>Dynamics AX 2012</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Dynamics AX 2012</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="435">
          <source>Dynamics AX for Operations</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Dynamics AX for Operations</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="436">
          <source>Because this method only calls the <bpt id="p1">**</bpt>validate()<ept id="p1">**</ept> method on the control and doesn't perform any additional processing, you can delete it.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このメソッドはコントロールの <bpt id="p1">**</bpt>validate()<ept id="p1">**</ept> メソッドのみを呼び出し追加の処理は実行しないため、削除できます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="437">
          <source>Group4<ph id="ph1">\_</ph>OffsetAccount</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Group4<ph id="ph1">\_</ph>OffsetAccount</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="438">
          <source>(Search for "Group4<ph id="ph1">\_</ph>OffsetAccount" in the search bar below the <bpt id="p1">**</bpt>Form<ept id="p1">**</ept> tab.)</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">(<bpt id="p1">**</bpt>フォーム<ept id="p1">**</ept>タブの下にある検索バーで「Group4<ph id="ph1">\_</ph>OffsetAccount」を検索してください。)</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="439">
          <source>Step 1</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ステップ１</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="440">
          <source>Dynamics AX 2012</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Dynamics AX 2012</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="441">
          <source>Dynamics AX for Operations</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Dynamics AX for Operations</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="442">
          <source>Update the code in the <bpt id="p1">**</bpt>initLedger()<ept id="p1">**</ept> method, after the code that updates the ledgerJournalTable buffer.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ledgerJournalTable バッファを更新するコードの後に、<bpt id="p1">**</bpt>initLedger()<ept id="p1">**</ept> メソッドのコードを更新します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="443">
          <source>Delete the <bpt id="p1">**</bpt>gotFocus()<ept id="p1">**</ept> method.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>gotFocus()<ept id="p1">**</ept> メソッドを削除します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="444">
          <source>Step 2</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ステップ２</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="445">
          <source>Dynamics AX 2012</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Dynamics AX 2012</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="446">
          <source>Dynamics AX for Operations</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Dynamics AX for Operations</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="447">
          <source>Because this method only calls the <bpt id="p1">**</bpt>jumpRef()<ept id="p1">**</ept> method on the control and doesn't perform any additional processing, you can delete it.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このメソッドはコントロールの <bpt id="p1">**</bpt>jumpRef()<ept id="p1">**</ept> メソッドのみを呼び出し追加の処理は実行しないため、削除できます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="448">
          <source>Step 3</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ステップ 3</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="449">
          <source>Dynamics AX 2012</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Dynamics AX 2012</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="450">
          <source>Dynamics AX for Operations</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Dynamics AX for Operations</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="451">
          <source>The migration steps for the <bpt id="p1">**</bpt>GridOffsetAccount.loadSegments()<ept id="p1">**</ept> method already made most of the changes that are required for this method.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>GridOffsetAccount.loadSegments()<ept id="p1">**</ept> メソッドの移行手順は、すでにこのメソッドに必要な変更のほとんどを行いました。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="452">
          <source>However, you must still make the following changes.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ただし、次の変更を加える必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="453">
          <source>Update the code in the <bpt id="p1">**</bpt>LedgerJournalTrans<ept id="p1">**</ept> data source’s <bpt id="p2">**</bpt>active<ept id="p2">**</ept> method.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>LedgerJournalTrans<ept id="p1">**</ept> データ ソースの <bpt id="p2">**</bpt>active<ept id="p2">**</ept> メソッドでコードを更新します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="454">
          <source>Make the same change in the <bpt id="p1">**</bpt>modified()<ept id="p1">**</ept> method of the <bpt id="p2">**</bpt>LedgerJournalTrans<ept id="p2">**</ept> data source’s <bpt id="p3">**</bpt>OffsetAccountType<ept id="p3">**</ept> field.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p2">**</bpt>LedgerJournalTrans<ept id="p2">**</ept> データ ソースの <bpt id="p3">**</bpt>OffsetAccountType<ept id="p3">**</ept> フィールドの <bpt id="p1">**</bpt>modified()<ept id="p1">**</ept> メソッドで同じ変更を行います。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="455">
          <source>Make the same change in the <bpt id="p1">**</bpt>initLedger()<ept id="p1">**</ept> method.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>initLedger()<ept id="p1">**</ept> メソッドで同じ変更を行います。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="456">
          <source>Delete the <bpt id="p1">**</bpt>loadSegments()<ept id="p1">**</ept> method.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>loadSegments()<ept id="p1">**</ept> メソッドを削除します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="457">
          <source>Step 4</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ステップ 4</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="458">
          <source>Dynamics AX 2012</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Dynamics AX 2012</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="459">
          <source>Dynamics AX for Operations</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Dynamics AX for Operations</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="460">
          <source>This method implements a custom lookup for the control.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このメソッドは、コントロールのカスタム ルックアップを実装します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="461">
          <source>Therefore, leave the method as it is.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">したがって、メソッドをそのままにします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="462">
          <source>Just remove the TODO.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">"仕事" を削除します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="463">
          <source>To hook up custom lookups, you must override the SEC’s <bpt id="p1">**</bpt>checkUseCustomLookup<ept id="p1">**</ept> method.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">カスタムのルックアップをフック アップするには、SEC の <bpt id="p1">**</bpt>checkUseCustomLookup<ept id="p1">**</ept> メソッドをオーバーライドする必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="464">
          <source>Additionally, make sure that the <bpt id="p1">**</bpt>closeSelectRecord<ept id="p1">**</ept> method on the custom lookup form is overridden.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">また、カスタム ルックアップ フォームで <bpt id="p1">**</bpt>closeSelectRecord<ept id="p1">**</ept> メソッドが上書きされたことを確認してください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="465">
          <source>For an example, see the <bpt id="p1">**</bpt>CustTableLookup<ept id="p1">**</ept> form.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">例については、<bpt id="p1">**</bpt>CustTableLookup<ept id="p1">**</ept> フォームを参照してください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="466">
          <source>Step 5</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ステップ 5</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="467">
          <source>Dynamics AX 2012</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Dynamics AX 2012</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="468">
          <source>Dynamics AX for Operations</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Dynamics AX for Operations</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="469">
          <source>Override the <bpt id="p1">**</bpt>onSegmentChanged()<ept id="p1">**</ept> method on the control, and add the following code to it.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">コントロールの <bpt id="p1">**</bpt>onSegmentChanged()<ept id="p1">**</ept> メソッドをオーバーライドし、次のコードを追加します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="470">
          <source>Delete the <bpt id="p1">**</bpt>segmentValueChanged()<ept id="p1">**</ept> method.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>segmentValueChanged()<ept id="p1">**</ept> メソッドを削除します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="471">
          <source><bpt id="p1">**</bpt>Note:<ept id="p1">**</ept> The preceding code for the <bpt id="p2">**</bpt>onSegmentChanged()<ept id="p2">**</ept> method will not compile, because the <bpt id="p3">**</bpt>onOffsetAccountSegmentChanged()<ept id="p3">**</ept> method expects a controller object, but this code passes an instance of the SEC.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>注記:<ept id="p1">**</ept> <bpt id="p3">**</bpt>onOffsetAccountSegmentChanged()<ept id="p3">**</ept> メソッドでは、コントローラー オブジェクトが必要ですが、このコードは SEC のインスタンスを渡すので、<bpt id="p2">**</bpt>onSegmentChanged()<ept id="p2">**</ept> メソッドの前のコードはコンパイルされません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="472">
          <source>To call methods on the control instance, you must change the method’s signature and its implementation accordingly.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">コントロール インスタンスでメソッドを呼び出すには、メソッドのシグネチャとその実装を適宜変更する必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="473">
          <source>This method is used by more than 50 callers.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このメソッドは、50 以上の呼び出し元が使用されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="474">
          <source>Therefore, you would also have to update all those calls.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">したがって、これらの呼び出しをすべて更新する必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="475">
          <source>Alternatively, you can add a new method that follows this guidance.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">または、このガイダンスに従うことによって新しいメソッドを追加できます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="476">
          <source>Step 6</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ステップ 6</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="477">
          <source>Dynamics AX 2012</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Dynamics AX 2012</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="478">
          <source>Dynamics AX for Operations</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Dynamics AX for Operations</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="479">
          <source>Because this method only calls the <bpt id="p1">**</bpt>validate()<ept id="p1">**</ept> method on the control and doesn't perform any additional processing, you can delete it.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このメソッドはコントロールの <bpt id="p1">**</bpt>validate()<ept id="p1">**</ept> メソッドのみを呼び出し追加の処理は実行しないため、削除できます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="480">
          <source>Additional resources</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">その他のリソース</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="481">
          <source><bpt id="p1">[</bpt>Segmented Entry control dialog support<ept id="p1">](segmented-entry-control-dialog-support.md)</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">[</bpt>セグメント化されたエントリ コントロールのダイアログのサポート<ept id="p1">](segmented-entry-control-dialog-support.md)</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="482">
          <source><bpt id="p1">[</bpt>Segmented Entry control Metadata Specification<ept id="p1">](segmented-entry-control-metadata-specification.md)</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">[</bpt>セグメント化されたエントリ コントロールのメタデータ詳細<ept id="p1">](segmented-entry-control-metadata-specification.md)</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="483">
          <source><bpt id="p1">[</bpt>Segmented Entry control Parm method Specification<ept id="p1">](segmented-entry-control-parm-method-specification.md)</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">[</bpt>セグメント化されたエントリ コントロールの Parm メソッド詳細<ept id="p1">](segmented-entry-control-parm-method-specification.md)</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="484">
          <source><bpt id="p1">[</bpt>Segmented Entry control - Migration guidance<ept id="p1">](segmented-entry-control-migration-guidance.md)</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">[</bpt>セグメント化されたエントリ コントロール - 移行のガイダンス<ept id="p1">](segmented-entry-control-migration-guidance.md)</ept></target></trans-unit>
      </group>
    </body>
  </file>
</xliff>