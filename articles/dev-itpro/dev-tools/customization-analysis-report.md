<?xml version="1.0" encoding="UTF-8"?>
<xliff xmlns:logoport="urn:logoport:xliffeditor:xliff-extras:1.0" xmlns:tilt="urn:logoport:xliffeditor:tilt-non-translatables:1.0" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns="urn:oasis:names:tc:xliff:document:1.2" xmlns:xliffext="urn:microsoft:content:schema:xliffextensions" version="1.2" xsi:schemaLocation="urn:oasis:names:tc:xliff:document:1.2 xliff-core-1.2-transitional.xsd">
  <file datatype="xml" source-language="en-US" original="customization-analysis-report.md" target-language="ja-JP">
    <header>
      <tool tool-company="Microsoft" tool-version="1.0-7889195" tool-name="mdxliff" tool-id="mdxliff"/>
      <xliffext:skl_file_name>customization-analysis-report.cca5cf.55f1b6dc6f8bcb714982cb890cc76247bd09636a.skl</xliffext:skl_file_name>
      <xliffext:version>1.2</xliffext:version>
      <xliffext:ms.openlocfilehash>55f1b6dc6f8bcb714982cb890cc76247bd09636a</xliffext:ms.openlocfilehash>
      <xliffext:ms.sourcegitcommit>9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b</xliffext:ms.sourcegitcommit>
      <xliffext:ms.lasthandoff>05/15/2019</xliffext:ms.lasthandoff>
      <xliffext:ms.openlocfilepath>articles\dev-itpro\dev-tools\customization-analysis-report.md</xliffext:ms.openlocfilepath>
    </header>
    <body>
      <group extype="content" id="content">
        <trans-unit xml:space="preserve" translate="yes" id="101" restype="x-metadata">
          <source>Customization Analysis Report (CAR)</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">カスタマイズ分析のレポート (CAR)</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="102" restype="x-metadata">
          <source>This article describes how to generate a Customization Analysis Report for your model.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この記事では、モデルのカスタマイズ分析レポートを生成する方法について説明します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="103" restype="x-metadata">
          <source>It also describes some best practice rules that are included in the report, and provides suggestions for fixing errors and warnings that are associated with these rules.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">また、レポートに含まれているベスト プラクティス ルールについて説明し、これらのルールに関連付けられているエラーおよび警告を解決するための推奨事項を示します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="104">
          <source>Customization Analysis Report (CAR)</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">カスタマイズ分析のレポート (CAR)</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="105">
          <source>This article describes how to generate a Customization Analysis Report for your model.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この記事では、モデルのカスタマイズ分析レポートを生成する方法について説明します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="106">
          <source>It also describes some best practice rules that are included in the report, and provides suggestions for fixing errors and warnings that are associated with these rules.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">また、レポートに含まれているベスト プラクティス ルールについて説明し、これらのルールに関連付けられているエラーおよび警告を解決するための推奨事項を示します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="107">
          <source>What is the Customization Analysis Report?</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">カスタマイズ分析レポートとは</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="108">
          <source>The Customization Analysis Report is a tool that analyzes your customization and extension models, and runs a predefined set of best practice rules.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">カスタマイズ分析レポートは、カスタマイズおよび拡張モデルを分析し、事前定義されたベスト プラクティスのルールを実行するツールです。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="109">
          <source>The report is one of the requirements of the solution certification process.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このレポートは、ソリューション認証プロセスの要件の 1 つです。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="110">
          <source>The report is in the form of a Microsoft Excel workbook.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">レポートは、Microsoft Excel のブック形式です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="111">
          <source>How to generate the report</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">レポートを生成する方法</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="112">
          <source>To generate the Customization Analysis Report, run the following command in a development environment.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">カスタマイズ分析レポートを生成するには、開発環境で次のコマンドを実行します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="113">
          <source><bpt id="p1">**</bpt>Example<ept id="p1">**</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>例<ept id="p1">**</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="114">
          <source>The xppbp.exe tool is located in c:<ph id="ph1">\\</ph>packages<ph id="ph2">\\</ph>bin or I:<ph id="ph3">\\</ph>AosService<ph id="ph4">\\</ph>PackagesLocalDirectory<ph id="ph5">\\</ph>bin.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">xppbp.exe ツール、c:<ph id="ph1">\\</ph>packages<ph id="ph2">\\</ph>bin または I:<ph id="ph3">\\</ph>AosService<ph id="ph4">\\</ph>PackagesLocalDirectory<ph id="ph5">\\</ph>bin にあります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="115">
          <source>Issues List</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">問題リスト</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="116">
          <source>This section describes all best practice rules (errors, warnings, or informational messages) that can appear on the <bpt id="p1">**</bpt>Issues List<ept id="p1">**</ept> page of the report and provides suggestions for fixing the issues.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このセクションでは、レポートの<bpt id="p1">**</bpt>問題リスト<ept id="p1">**</ept>ページに表示されるベスト プラクティスのルール (エラー、警告、または情報メッセージ) をすべて説明し、問題を解決するための提案を示します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="117">
          <source>Issues are of the <bpt id="p1">**</bpt>metadata<ept id="p1">**</ept> or <bpt id="p2">**</bpt>code<ept id="p2">**</ept> type.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>メタデータ<ept id="p1">**</ept>または<bpt id="p2">**</bpt>コード<ept id="p2">**</ept>の型の問題です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="118">
          <source>For all <bpt id="p1">**</bpt>code<ept id="p1">**</ept> issues, keep in mind that, if the warning or error occurs in a method that you've overlaid, the lines of code that violate the rule might belong to a model in a lower layer.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">すべての<bpt id="p1">**</bpt>コード<ept id="p1">**</ept>問題に関しては、重ねたメソッドで警告またはエラーが発生する場合、ルールに違反しているコードの明細行は下位レイヤーのモデルに属していることに留意してください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="119">
          <source>In that case, you're not responsible for fixing warnings and errors in code that isn't yours.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">その場合、自分のものではないコードの警告やエラーを修正する責任はありません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="120">
          <source>BPCheckPackReturnsConnull</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">BPCheckPackReturnsConnull</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="121">
          <source>Description</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">説明</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="122">
          <source>This rule applies to all classes that implement the <bpt id="p1">**</bpt>SysPackable<ept id="p1">**</ept> interface.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このルールは、<bpt id="p1">**</bpt>SysPackable<ept id="p1">**</ept> インターフェイスを実装するすべてのクラスに適用されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="123">
          <source>It makes sure that the <bpt id="p1">**</bpt>Pack<ept id="p1">**</ept> method doesn't return <bpt id="p2">**</bpt>Connull()<ept id="p2">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">これは、<bpt id="p1">**</bpt>Pack<ept id="p1">**</ept> メソッドが <bpt id="p2">**</bpt>Connull()<ept id="p2">**</ept> を返さないことを確認します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="124">
          <source>Error message</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">エラー メッセージ</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="125">
          <source>Container pack method returns connull in a Runbase derived class</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">コンテナー パック メソッドは、Runbase 派生クラスで connull を返します</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="126">
          <source>Issue type/severity</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">出庫タイプ/重要度</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="127">
          <source>Code/Warning</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">コード/警告</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="128">
          <source>How to fix it</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">修正する方法</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="129">
          <source>Update the return value of the <bpt id="p1">**</bpt>Pack<ept id="p1">**</ept> method, or return <bpt id="p2">**</bpt>Super()<ept id="p2">**</ept> when applicable.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">該当する場合、<bpt id="p1">**</bpt>Pack<ept id="p1">**</ept> メソッドの戻り値を更新するか、<bpt id="p2">**</bpt>Super()<ept id="p2">**</ept> を返します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="130">
          <source>BPCheckParametersModified</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">BPCheckParametersModified</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="131">
          <source>Description</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">説明</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="132">
          <source>This rule fails if a parameter of a method is modified inside a method.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">メソッドのパラメーターがメソッド内で変更された場合、このルールは失敗します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="133">
          <source>Error message</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">エラー メッセージ</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="134">
          <source>Parameter 1% in method %1 are modified inside the method</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">メソッド %1 のパラメーター 1% がメソッド内で変更されています</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="135">
          <source>Issue type/severity</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">出庫タイプ/重要度</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="136">
          <source>Code/Warning</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">コード/警告</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="137">
          <source>How to fix it</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">修正する方法</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="138">
          <source>Refactor your code.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">コードをリファクターします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="139">
          <source>Parameters must be modified by the caller, not within the called method.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">呼び出されたメソッド内ではなく、呼び出し元によりパラメーターを変更する必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="140">
          <source>BPCheckSQLCode</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">BPCheckSQLCode</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="141">
          <source>Description</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">説明</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="142">
          <source>This rule fails if your X++ code contains direct SQL code.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このルールは、X++ コードに直接 SQL コードが含まれていると失敗します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="143">
          <source>Error message</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">エラー メッセージ</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="144">
          <source>SQL code found in method %1</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">メソッド %1 に SQL コードが見つかりました</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="145">
          <source>Issue type/severity</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">出庫タイプ/重要度</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="146">
          <source>Code/Warning</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">コード/警告</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="147">
          <source>How to fix it</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">修正する方法</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="148">
          <source>Refactor your code to use X++ to access the database.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">X++ を使用してデータベースにアクセスするコードをリファクタリングします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="149">
          <source>BPCheckNestedLoopInCode</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">BPCheckNestedLoopInCode</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="150">
          <source>Description</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">説明</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="151">
          <source>This rule fails if it finds a <bpt id="p1">**</bpt>while select<ept id="p1">**</ept> loop nested within a loop.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このルールは、<bpt id="p1">**</bpt>select<ept id="p1">**</ept> ループがループ内にネストされていることを検出すると失敗します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="152">
          <source>Error message</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">エラー メッセージ</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="153">
          <source>Nested data access loop found in %1 method</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">%1 メソッドに入れ子になったデータ アクセス ループが見つかりました</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="154">
          <source>Issue type/severity</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">出庫タイプ/重要度</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="155">
          <source>Code/Warning</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">コード/警告</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="156">
          <source>How to fix it</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">修正する方法</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="157">
          <source>Refactor your code to use joins instead of nested data access loops.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">入れ子になったデータ アクセス ループの代わりに結合を使うコードをリファクタリングします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="158">
          <source>If you can't refactor the code without altering the business logic of your method, document an exception when you submit your Customization Analysis Report to Microsoft.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">メソッドのビジネス ロジックを変更せずにコードをリファクターできない場合は、Microsoft にカスタマイズ分析レポートを提出するときに例外を文書化します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="159">
          <source>BPCheckInsertMethodInLoop</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">BPCheckInsertMethodInLoop</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="160">
          <source>Description</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">説明</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="161">
          <source>This rules fails if it finds a call to the method <bpt id="p1">**</bpt>insert<ept id="p1">**</ept> nested inside a loop.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このルールは、ループの中に入れ子されたメソッド <bpt id="p1">**</bpt>insert<ept id="p1">**</ept> への呼び出しを検出すると失敗します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="162">
          <source>We recommend that you use <bpt id="p1">**</bpt>InsertRecordList<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>InsertRecordList<ept id="p1">**</ept> を使用することをお勧めします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="163">
          <source>This rule doesn't apply to InMemory tables.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このルールは、InMemory テーブルには適用されません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="164">
          <source>Error message</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">エラー メッセージ</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="165">
          <source>Insert method can be replaced with RecordInsertList in method %1</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">メソッド %1 で、Insert メソッドを RecordInsertList に置き換えることができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="166">
          <source>Issue type/severity</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">出庫タイプ/重要度</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="167">
          <source>Code/Warning</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">コード/警告</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="168">
          <source>How to fix it</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">修正する方法</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="169">
          <source>Refactor your code to use set-based operations, such as <bpt id="p1">**</bpt>InsertRecordList<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>InsertRecordList<ept id="p1">**</ept> など、設定に基づく操作を使用するコードをリファクターします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="170">
          <source>BPCheckSelectwithJoin</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">BPCheckSelectwithJoin</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="171">
          <source>Description</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">説明</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="172">
          <source>This rule fails if it finds nested <bpt id="p1">**</bpt>select<ept id="p1">**</ept> statements that aren't joined.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">結合されていない入れ子になった <bpt id="p1">**</bpt>select<ept id="p1">**</ept> ステートメントが見つかった場合、このルールは失敗します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="173">
          <source>Error message</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">エラー メッセージ</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="174">
          <source>Nested select statement in %1 method can be joined</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">%1 メソッドの入れ子になった select ステートメントは結合できます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="175">
          <source>Issue type/severity</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">出庫タイプ/重要度</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="176">
          <source>Code/Warning</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">コード/警告</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="177">
          <source>How to fix it</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">修正する方法</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="178">
          <source>Refactor your code to use joins instead of a nested <bpt id="p1">**</bpt>select<ept id="p1">**</ept> statement.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">入れ子になった <bpt id="p1">**</bpt>select<ept id="p1">**</ept> ステートメントの代わりに結合を使うコードをリファクタリングします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="179">
          <source>If you can't refactor the code without altering the business logic of your method, document an exception when you submit your Customization Analysis Report to Microsoft.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">メソッドのビジネス ロジックを変更せずにコードをリファクターできない場合は、Microsoft にカスタマイズ分析レポートを提出するときに例外を文書化します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="180">
          <source>BPFunctionCallwithSelect</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">BPFunctionCallwithSelect</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="181">
          <source>Description</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">説明</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="182">
          <source>This rule fails if a function call is found within a <bpt id="p1">**</bpt>select<ept id="p1">**</ept> statement.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このルールは、<bpt id="p1">**</bpt>select<ept id="p1">**</ept> ステートメント内で関数呼び出しが見つかった場合に失敗します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="183">
          <source>Error message</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">エラー メッセージ</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="184">
          <source>Function call found in select statement in method %1</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">メソッド %1 の select ステートメントに、関数呼び出しが見つかりました</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="185">
          <source>Issue type/severity</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">出庫タイプ/重要度</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="186">
          <source>Code/Warning</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">コード/警告</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="187">
          <source>How to fix it</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">修正する方法</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="188">
          <source>Assign the function’s return value to a local variable before you call the <bpt id="p1">**</bpt>select<ept id="p1">**</ept> statement, and use the local variable in the <bpt id="p2">**</bpt>select<ept id="p2">**</ept> statement.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>選択<ept id="p1">**</ept>ステートメントを呼び出す前に、関数の戻り値をローカル変数に割り当て、<bpt id="p2">**</bpt>選択<ept id="p2">**</ept>ステートメントでローカル変数を使用します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="189">
          <source>BPCheckinvalidExecuteQuery</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">BPCheckinvalidExecuteQuery</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="190">
          <source>Description</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">説明</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="191">
          <source>This rule fails if a call to <bpt id="p1">**</bpt>addRange<ept id="p1">**</ept> is found after a call to <bpt id="p2">**</bpt>super()<ept id="p2">**</ept> in the <bpt id="p3">**</bpt>ExecuteQuery<ept id="p3">**</ept> method.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このルールは、<bpt id="p3">**</bpt>ExecuteQuery<ept id="p3">**</ept> メソッドで <bpt id="p2">**</bpt>super()<ept id="p2">**</ept> を呼び出した後に <bpt id="p1">**</bpt>addRange<ept id="p1">**</ept> への呼び出しが見つかった場合に失敗します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="192">
          <source>Error message</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">エラー メッセージ</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="193">
          <source>Add range after super() should not be added in ExecuteQuery method for form %1</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">フォーム %1 の ExecuteQuery メソッドに、super() の後に add range を追加しないでください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="194">
          <source>Issue type/severity</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">出庫タイプ/重要度</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="195">
          <source>Code/Warning</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">コード/警告</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="196">
          <source>How to fix it</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">修正する方法</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="197">
          <source>Refactor your code to avoid this pattern.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このパターンを回避するために、コードをリファクタリングします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="198">
          <source>BPCheckInvalidInitFormMethod</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">BPCheckInvalidInitFormMethod</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="199">
          <source>Description</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">説明</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="200">
          <source>This rule makes sure that you don't initialize form controls and data sources in a form’s <bpt id="p1">**</bpt>init<ept id="p1">**</ept> method before you call <bpt id="p2">**</bpt>super()<ept id="p2">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このルールは、<bpt id="p2">**</bpt>super()<ept id="p2">**</ept> を呼び出す前に、フォームのコントロールとデータソースをフォームの <bpt id="p1">**</bpt>init<ept id="p1">**</ept> メソッドで初期化しないようにします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="201">
          <source>It fails if it finds a statement that uses <bpt id="p1">**</bpt>element<ept id="p1">**</ept> or <bpt id="p2">**</bpt>this<ept id="p2">**</ept> before the call to <bpt id="p3">**</bpt>super()<ept id="p3">**</ept> (<bpt id="p4">**</bpt>this.aMethod()<ept id="p4">**</ept> or <bpt id="p5">**</bpt>element.aMethod()<ept id="p5">**</ept>).</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>element<ept id="p1">**</ept> または <bpt id="p2">**</bpt>this<ept id="p2">**</ept> を <bpt id="p3">**</bpt>super()<ept id="p3">**</ept> に対する呼び出し (<bpt id="p4">**</bpt>this.aMethod()<ept id="p4">**</ept> または <bpt id="p5">**</bpt>element.aMethod()<ept id="p5">**</ept>) の前に使用するステートメントが検出された場合に失敗します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="202">
          <source>An informational message is shown only for some allowed patterns, such as initializing number sequences (<bpt id="p1">**</bpt>numberSeqPreInit<ept id="p1">**</ept>).</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">情報メッセージは番号順序の初期化など許可されたいくつかのパターンのみを表示します (<bpt id="p1">**</bpt>numberSeqPreInit<ept id="p1">**</ept>) 。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="203">
          <source>Error message</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">エラー メッセージ</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="204">
          <source>Form element statements should not be used before super() in init method of form %1</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">フォーム要素ステートメントは、フォーム %1 の init メソッドで、super() の前に使用しないでください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="205">
          <source>Issue type/severity</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">出庫タイプ/重要度</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="206">
          <source>Code/Info or Warning</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">コード/情報または警告</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="207">
          <source>How to fix it</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">修正する方法</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="208">
          <source>Refactor your code to access form controls and data after the call to <bpt id="p1">**</bpt>super()<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>super()<ept id="p1">**</ept> の呼び出し後、コードをリファクターしてフォーム コントロールおよびデータにアクセスします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="209">
          <source>If your code doesn't initialize any form control and doesn't access any form data sources before <bpt id="p1">**</bpt>super()<ept id="p1">**</ept>, document an exception when you submit your Customization Analysis Report to Microsoft.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">コードが任意のフォーム コントロールを初期化せず、<bpt id="p1">**</bpt>super()<ept id="p1">**</ept> の前にどのフォーム データ ソースにもアクセスしない場合、Microsoft にカスタマイズ分析のレポートを送信するときに例外をまとめます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="210">
          <source>BPCheckEmptyLoop</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">BPCheckEmptyLoop</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="211">
          <source>Description</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">説明</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="212">
          <source>This rule fails if it finds loops that have no statements.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このルールは、ステートメントがないループを検出すると失敗します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="213">
          <source>Error message</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">エラー メッセージ</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="214">
          <source>Empty loop found in method %1 in class %2</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">クラス <ph id="1">%2</ph> の メソッド <ph id="2">%1</ph> で空のループが見つかりました。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="215">
          <source>Issue type/severity</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">出庫タイプ/重要度</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="216">
          <source>Code/Warning</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">コード/警告</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="217">
          <source>How to fix it</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">修正する方法</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="218">
          <source>Remove the loop from your code.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ループをコードから削除します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="219">
          <source>BPCheckLockQueryRange</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">BPCheckLockQueryRange</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="220">
          <source>Description</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">説明</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="221">
          <source>This rule fails if the code calls <bpt id="p1">**</bpt>AddRange<ept id="p1">**</ept> in the <bpt id="p2">**</bpt>init<ept id="p2">**</ept> method of the form, and doesn't set the range as locked or hidden.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">フォームの <bpt id="p2">**</bpt>init<ept id="p2">**</ept> メソッドでコードが <bpt id="p1">**</bpt>AddRange<ept id="p1">**</ept> を呼び出し、その範囲をロックまたは非表示として設定しないと、このルールは失敗します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="222">
          <source>Error message</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">エラー メッセージ</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="223">
          <source>Range should be locked or hidden in form %1</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">フォーム %1で、範囲はロックするか、非表示にする必要があります</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="224">
          <source>Issue type/severity</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">出庫タイプ/重要度</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="225">
          <source>Code/Warning</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">コード/警告</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="226">
          <source>How to fix it</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">修正する方法</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="227">
          <source>Add <bpt id="p1">**</bpt>QueryBuildRange.status(RangeStatus::Locked)<ept id="p1">**</ept> or <bpt id="p2">**</bpt>QueryBuildRange.status(RangeStatus::Hidden)<ept id="p2">**</ept> after the call to <bpt id="p3">**</bpt>AddRange<ept id="p3">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p3">**</bpt>AddRange<ept id="p3">**</ept> の呼び出しの後に、<bpt id="p1">**</bpt>QueryBuildRange.status(RangeStatus::Locked)<ept id="p1">**</ept> または <bpt id="p2">**</bpt>QueryBuildRange.status(RangeStatus::Hidden)<ept id="p2">**</ept> を追加します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="228">
          <source>BPCheckSkipStatementValidation</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">BPCheckSkipStatementValidation</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="229">
          <source>Description</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">説明</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="230">
          <source>This rule reports an informational message if it finds a set-based operation that doesn&amp;#39;t have <bpt id="p1">&lt;strong&gt;</bpt>Skip<ept id="p1">&lt;/strong&gt;</ept> statements.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このルールは、<bpt id="p1">&lt;strong&gt;</bpt>Skip<ept id="p1">&lt;/strong&gt;</ept> ステートメントを持たないセットベースの操作を検出した場合に通知メッセージを報告します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="231">
          <source>When <bpt id="p1">&lt;strong&gt;</bpt>update_recordset<ept id="p1">&lt;/strong&gt;</ept> is found, the rule checks for <bpt id="p2">&lt;strong&gt;</bpt>skipDataMethods(true)<ept id="p2">&lt;/strong&gt;</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">&lt;strong&gt;</bpt>update_recordset<ept id="p1">&lt;/strong&gt;</ept> が見つかると、ルールによって <bpt id="p2">&lt;strong&gt;</bpt>skipDataMethods(true)<ept id="p2">&lt;/strong&gt;</ept> がチェックされます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="232">
          <source>The rule applies only when the <bpt id="p1">&lt;strong&gt;</bpt>update<ept id="p1">&lt;/strong&gt;</ept> method on the table is overridden.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">テーブルの <bpt id="p1">&lt;strong&gt;</bpt>update<ept id="p1">&lt;/strong&gt;</ept> メソッドが上書きされる場合にのみルールが適用されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="233">
          <source>When <bpt id="p1">&lt;strong&gt;</bpt>insert_recordset<ept id="p1">&lt;/strong&gt;</ept> is found, the rule checks for <bpt id="p2">&lt;strong&gt;</bpt>skipDataMethods(true)<ept id="p2">&lt;/strong&gt;</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">&lt;strong&gt;</bpt>insert_recordset<ept id="p1">&lt;/strong&gt;</ept> が見つかると、ルールによって <bpt id="p2">&lt;strong&gt;</bpt>skipDataMethods(true)<ept id="p2">&lt;/strong&gt;</ept> がチェックされます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="234">
          <source>The rule applies only when the <bpt id="p1">&lt;strong&gt;</bpt>insert<ept id="p1">&lt;/strong&gt;</ept> method on the table is overridden.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">テーブルの <bpt id="p1">&lt;strong&gt;</bpt>insert<ept id="p1">&lt;/strong&gt;</ept> メソッドが上書きされる場合にのみルールが適用されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="235">
          <source>When <bpt id="p1">&lt;strong&gt;</bpt>delete_from<ept id="p1">&lt;/strong&gt;</ept> is found, the rule checks for <bpt id="p2">&lt;strong&gt;</bpt>skipDeleteActions(true)<ept id="p2">&lt;/strong&gt;</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">&lt;strong&gt;</bpt>delete_from<ept id="p1">&lt;/strong&gt;</ept> が見つかると、ルールによって <bpt id="p2">&lt;strong&gt;</bpt>skipDeleteActions(true)<ept id="p2">&lt;/strong&gt;</ept> がチェックされます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="236">
          <source>The rule applies only when the <bpt id="p1">&lt;strong&gt;</bpt>insert<ept id="p1">&lt;/strong&gt;</ept> method on the table is overridden.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">テーブルの <bpt id="p1">&lt;strong&gt;</bpt>insert<ept id="p1">&lt;/strong&gt;</ept> メソッドが上書きされる場合にのみルールが適用されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="237">
          <source>This is an informational message that highlights the need to call <bpt id="p1">&lt;strong&gt;</bpt>skip<ept id="p1">&lt;/strong&gt;</ept> methods to take full advantage of the performance gains of set-based operations.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">これは、セットベースの操作のパフォーマンス向上を最大限に活用するために、<bpt id="p1">&lt;strong&gt;</bpt>スキップ<ept id="p1">&lt;/strong&gt;</ept>メソッドを呼び出す必要があることを示す情報メッセージです。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="238">
          <source>If <bpt id="p1">&lt;strong&gt;</bpt>skip<ept id="p1">&lt;/strong&gt;</ept> methods aren&amp;#39;t used, the execution falls back to a row-by-row operation.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">&lt;strong&gt;</bpt>スキップ<ept id="p1">&lt;/strong&gt;</ept> メソッドが使用されていない場合は、実行は行ごとの操作に戻ります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="239">
          <source>Error message</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">エラー メッセージ</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="240">
          <source>Set-based operation must invoke Skip statements in method %1 in class %2; otherwise, execution will fall back to a row by row operation.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">セット ベースの操作はクラス <ph id="1">%2</ph> のメソッド <ph id="2">%1</ph> で Skip ステートメントを呼び出す必要があります。それ以外の場合、行ごとの操作にフォールバックされます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="241">
          <source>Issue type/severity</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">出庫タイプ/重要度</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="242">
          <source>Code/Information</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">コード/情報</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="243">
          <source>How to fix it</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">修正する方法</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="244">
          <source>Use <bpt id="p1">&lt;strong&gt;</bpt>skipDataMethods(true)<ept id="p1">&lt;/strong&gt;</ept> or <bpt id="p2">&lt;strong&gt;</bpt>skipDeleteActions(true)<ept id="p2">&lt;/strong&gt;</ept> when applicable.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">該当する場合は、<bpt id="p1">&lt;strong&gt;</bpt>skipDataMethods(true)<ept id="p1">&lt;/strong&gt;</ept> または <bpt id="p2">&lt;strong&gt;</bpt>skipDeleteActions(true)<ept id="p2">&lt;/strong&gt;</ept> を使用します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="245">
          <source>BPCheckNoTTSTryBlock</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">BPCheckNoTTSTryBlock</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="246">
          <source>Description</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">説明</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="247">
          <source>This rule fails if it finds a <bpt id="p1">&lt;strong&gt;</bpt>try<ept id="p1">&lt;/strong&gt;</ept> statement within a <bpt id="p2">&lt;strong&gt;</bpt>tts<ept id="p2">&lt;/strong&gt;</ept> block that isn&amp;#39;t handled correctly.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このルールは、正しく処理されない <bpt id="p2">&lt;strong&gt;</bpt>tts<ept id="p2">&lt;/strong&gt;</ept> ブロック内の <bpt id="p1">&lt;strong&gt;</bpt>try<ept id="p1">&lt;/strong&gt;</ept> ステートメントを検出すると失敗します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="248">
          <source>Error message</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">エラー メッセージ</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="249">
          <source>Tts block with Try statement does not explicitly catch exceptions in method %1</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">try 文の tts ブロックは、メソッド %1 の例外を明示的にキャッチしません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="250">
          <source>Issue type/severity</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">出庫タイプ/重要度</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="251">
          <source>Code/Warning</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">コード/警告</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="252">
          <source>How to fix it</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">修正する方法</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="253">
          <source>The following examples show when the rule will fail or pass.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">次の例では、ルールが失敗するか、合格するかを示しています。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="254">
          <source>Use these examples as guidelines to refactor your code.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">次の例を参考にして、コードをリファクタリングします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="255">
          <source>BPCheckEmptyTableMethod</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">BPCheckEmptyTableMethod</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="256">
          <source>Description</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">説明</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="257">
          <source>This rule checks for table methods that have no source code.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このルールは、ソース コードのないテーブル メソッドをチェックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="258">
          <source>Empty table methods cause record-set operations on the table to fall back to a row-by-row operation.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">空テーブルのメソッドは、テーブルのレコードセット オペレーションを行単位の操作に戻す原因となります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="259">
          <source>Error message</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">エラー メッセージ</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="260">
          <source>%1 table has an empty %2 method</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">%1 テーブルに空の %2 メソッドがあります</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="261">
          <source>Issue type/severity</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">出庫タイプ/重要度</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="262">
          <source>Code/Warning</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">コード/警告</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="263">
          <source>How to fix it</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">修正する方法</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="264">
          <source>Remove this method from your code.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このメソッドをコードから削除します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="265">
          <source>BPCheckBatchJobsEnabled</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">BPCheckBatchJobsEnabled</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="266">
          <source>Description</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">説明</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="267">
          <source>This rule makes sure that all classes that extend <bpt id="p1">**</bpt>RunBaseBatch<ept id="p1">**</ept> have a <bpt id="p2">**</bpt>canGoBatch<ept id="p2">**</ept> method that returns <bpt id="p3">**</bpt>true<ept id="p3">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このルールは、<bpt id="p1">**</bpt>RunBaseBatch<ept id="p1">**</ept> を拡張するすべてのクラスが <bpt id="p3">**</bpt>true<ept id="p3">**</ept> を返す <bpt id="p2">**</bpt>canGoBatch<ept id="p2">**</ept> メソッドを持つことを保証します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="268">
          <source>Error message</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">エラー メッセージ</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="269">
          <source>Custom job is not batch-enabled in class %1</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">カスタム ジョブがクラス %1 でバッチ対応でありません</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="270">
          <source>Issue type/severity</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">出庫タイプ/重要度</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="271">
          <source>Code/Warning</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">コード/警告</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="272">
          <source>How to fix it</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">修正する方法</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="273">
          <source>The <bpt id="p1">**</bpt>canGoBatch<ept id="p1">**</ept> method must return <bpt id="p2">**</bpt>true<ept id="p2">**</ept> for all batch classes.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>canGoBatch<ept id="p1">**</ept> メソッドは、すべてのバッチ クラスに <bpt id="p2">**</bpt>true<ept id="p2">**</ept> を返します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="274">
          <source>BPCheckDisplayMethodCached</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">BPCheckDisplayMethodCached</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="275">
          <source>Description</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">説明</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="276">
          <source>For each control that is bound to a data method, this rules fails if one of these conditions is met:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">データ メソッドにバインドされている各コントロールについては、これらの条件のいずれかが満たされている場合、このルールは失敗します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="277">
          <source>The <bpt id="p1">&lt;strong&gt;</bpt>Cache Data Method<ept id="p1">&lt;/strong&gt;</ept> property is set to <bpt id="p2">&lt;strong&gt;</bpt>Auto<ept id="p2">&lt;/strong&gt;</ept>, the corresponding table <bpt id="p3">&lt;strong&gt;</bpt>display<ept id="p3">&lt;/strong&gt;</ept><ph id="ph1">/</ph><bpt id="p4">&lt;strong&gt;</bpt>edit<ept id="p4">&lt;/strong&gt;</ept> method doesn&amp;#39;t have the <bpt id="p5">&lt;strong&gt;</bpt>SysClientCacheDataMethodAttribute<ept id="p5">&lt;/strong&gt;</ept>, and the <bpt id="p6">&lt;strong&gt;</bpt>init<ept id="p6">&lt;/strong&gt;</ept> method of the data source doesn&amp;#39;t use <bpt id="p7">&lt;strong&gt;</bpt>CacheAddMethod<ept id="p7">&lt;/strong&gt;</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">&lt;strong&gt;</bpt>データのキャッシュ方法<ept id="p1">&lt;/strong&gt;</ept>プロパティが<bpt id="p2">&lt;strong&gt;</bpt>自動<ept id="p2">&lt;/strong&gt;</ept>に設定され、対応するテーブルの <bpt id="p3">&lt;strong&gt;</bpt>display<ept id="p3">&lt;/strong&gt;</ept><ph id="ph1">/</ph><bpt id="p4">&lt;strong&gt;</bpt>edit<ept id="p4">&lt;/strong&gt;</ept> メソッドには <bpt id="p5">&lt;strong&gt;</bpt>SysClientCacheDataMethodAttribute<ept id="p5">&lt;/strong&gt;</ept> がなく、データ ソースの <bpt id="p6">&lt;strong&gt;</bpt>init<ept id="p6">&lt;/strong&gt;</ept> メソッドは <bpt id="p7">&lt;strong&gt;</bpt>CacheAddMethod<ept id="p7">&lt;/strong&gt;</ept> を使用しません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="278">
          <source>The <bpt id="p1">&lt;strong&gt;</bpt>Cache Data Method<ept id="p1">&lt;/strong&gt;</ept> property is set to <bpt id="p2">&lt;strong&gt;</bpt>No<ept id="p2">&lt;/strong&gt;</ept>, and the <bpt id="p3">&lt;strong&gt;</bpt>init<ept id="p3">&lt;/strong&gt;</ept> method of the data source doesn&amp;#39;t use <bpt id="p4">&lt;strong&gt;</bpt>CacheAddMethod<ept id="p4">&lt;/strong&gt;</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">&lt;strong&gt;</bpt>データのキャッシュ方法<ept id="p1">&lt;/strong&gt;</ept> プロパティは <bpt id="p2">&lt;strong&gt;</bpt>いいえ<ept id="p2">&lt;/strong&gt;</ept> に設定され、データ ソースの <bpt id="p3">&lt;strong&gt;</bpt>init<ept id="p3">&lt;/strong&gt;</ept> メソッドは <bpt id="p4">&lt;strong&gt;</bpt>CacheAddMethod<ept id="p4">&lt;/strong&gt;</ept> を使用しません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="279">
          <source>Error message</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">エラー メッセージ</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="280">
          <source>Display method %1 in form %2 not cached</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">フォーム <ph id="1">%2</ph> の 表示メソッド <ph id="2">%1</ph> がキャッシュされていません</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="281">
          <source>Issue type/severity</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">出庫タイプ/重要度</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="282">
          <source>Code/Warning</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">コード/警告</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="283">
          <source>How to fix it</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">修正する方法</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="284">
          <source>You can fix this warning by using one of the following patterns:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この警告は、次のいずれかのパターンを使用して修正することができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="285">
          <source>Set the <bpt id="p1">&lt;strong&gt;</bpt>Cache Data Method<ept id="p1">&lt;/strong&gt;</ept> property to <bpt id="p2">&lt;strong&gt;</bpt>Yes<ept id="p2">&lt;/strong&gt;</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">&lt;strong&gt;</bpt>キャッシュ データ メソッド<ept id="p1">&lt;/strong&gt;</ept> プロパティを <bpt id="p2">&lt;strong&gt;</bpt>はい<ept id="p2">&lt;/strong&gt;</ept> に設定します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="286">
          <source>Set the <bpt id="p1">&lt;strong&gt;</bpt>Cache Data Method<ept id="p1">&lt;/strong&gt;</ept> property to <bpt id="p2">&lt;strong&gt;</bpt>Auto<ept id="p2">&lt;/strong&gt;</ept>, and mark the data method of the table with the <bpt id="p3">&lt;strong&gt;</bpt>SysClientCacheDataMethodAttribute<ept id="p3">&lt;/strong&gt;</ept> attribute.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">&lt;strong&gt;</bpt>キャッシュ データ メソッド<ept id="p1">&lt;/strong&gt;</ept> プロパティを <bpt id="p2">&lt;strong&gt;</bpt>自動<ept id="p2">&lt;/strong&gt;</ept> に設定し、<bpt id="p3">&lt;strong&gt;</bpt>SysClientCacheDataMethodAttribute<ept id="p3">&lt;/strong&gt;</ept> 属性を使用してテーブルのデータ メソッドをマークします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="287">
          <source>Here is an example.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">次に例を示します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="288">
          <source>Use <bpt id="p1">&lt;strong&gt;</bpt>CacheAddMethod<ept id="p1">&lt;/strong&gt;</ept> in the <bpt id="p2">&lt;strong&gt;</bpt>init<ept id="p2">&lt;/strong&gt;</ept> method of the form to mark the method as cached.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">フォームの <bpt id="p2">&lt;strong&gt;</bpt>init<ept id="p2">&lt;/strong&gt;</ept> メソッドで <bpt id="p1">&lt;strong&gt;</bpt>CacheAddMethod<ept id="p1">&lt;/strong&gt;</ept> を使用すると、そのメソッドをキャッシュ済みとしてマークします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="289">
          <source>BPCheckSQLQueryInInit</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">BPCheckSQLQueryInInit</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="290">
          <source>Description</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">説明</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="291">
          <source>This rule fails if a data access query that has a <bpt id="p1">**</bpt>while<ept id="p1">**</ept> loop is found in the <bpt id="p2">**</bpt>init<ept id="p2">**</ept> method of a form.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このルールは、フォームの <bpt id="p2">**</bpt>init<ept id="p2">**</ept> メソッドで <bpt id="p1">**</bpt>while<ept id="p1">**</ept> ループを持つデータ アクセス クエリが見つかった場合に失敗します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="292">
          <source>This pattern could cause performance issues when the form is initalized.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このパターンは、フォームの初期化時にパフォーマンスの問題を引き起こす可能性があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="293">
          <source>Error message</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">エラー メッセージ</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="294">
          <source>SQL query with while loop was found in init method of form %1</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">フォーム %1 の init メソッドで、while ループを持つ SQL クエリが見つかりました</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="295">
          <source>Issue type/severity</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">出庫タイプ/重要度</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="296">
          <source>Code/Warning</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">コード/警告</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="297">
          <source>How to fix it</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">修正する方法</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="298">
          <source>Refactor your code to avoid this pattern.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このパターンを回避するために、コードをリファクタリングします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="299">
          <source>BPCheckNewQueryWithForm</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">BPCheckNewQueryWithForm</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="300">
          <source>Description</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">説明</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="301">
          <source>This rule fails if it finds the <bpt id="p1">**</bpt>new Query()<ept id="p1">**</ept> statement in the <bpt id="p2">**</bpt>init<ept id="p2">**</ept> or <bpt id="p3">**</bpt>executeQuery<ept id="p3">**</ept> method of a form.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このルールは、フォームの <bpt id="p2">**</bpt>init<ept id="p2">**</ept> または <bpt id="p3">**</bpt>executeQuery<ept id="p3">**</ept> メソッドで <bpt id="p1">**</bpt>new Query()<ept id="p1">**</ept> ステートメントを検出すると失敗します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="302">
          <source>Error message</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">エラー メッセージ</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="303">
          <source>Data source query overridden in form method %1</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">フォーム メソッド %1 で、データ ソース クエリが上書きされます</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="304">
          <source>Issue type/severity</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">出庫タイプ/重要度</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="305">
          <source>Code/Warning</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">コード/警告</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="306">
          <source>How to fix it</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">修正する方法</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="307">
          <source>Refactor your code to avoid this pattern.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このパターンを回避するために、コードをリファクタリングします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="308">
          <source>BPCheckSelectForUpdateAbsent</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">BPCheckSelectForUpdateAbsent</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="309">
          <source>Description</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">説明</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="310">
          <source>This rule fails if <bpt id="p1">**</bpt>Select ForUpdate<ept id="p1">**</ept> is used to select records, but an update isn't being performed.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>Select ForUpdate<ept id="p1">**</ept> を使用してレコードを選択したが、更新が実行されていない場合、このルールは失敗します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="311">
          <source>This rules doesn't apply to tables that are enabled for Optimistic Concurrency Control (OCC).</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このルールは、オプティミスティック同時実行制御 (OCC) が有効になっているテーブルには適用されません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="312">
          <source>Error message</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">エラー メッセージ</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="313">
          <source>Select ForUpdate not implemented in method %1</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">メソッド %1 に Select ForUpdate が実装されていません</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="314">
          <source>Issue type/severity</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">出庫タイプ/重要度</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="315">
          <source>Code/Warning</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">コード/警告</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="316">
          <source>How to fix it</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">修正する方法</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="317">
          <source>Use <bpt id="p1">**</bpt>Select<ept id="p1">**</ept> instead of <bpt id="p2">**</bpt>Select ForUpdate<ept id="p2">**</ept>, or set the <bpt id="p3">**</bpt>OCC Enabled<ept id="p3">**</ept> property to <bpt id="p4">**</bpt>Yes<ept id="p4">**</ept> on the table.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p2">**</bpt>ForUpdate を選択<ept id="p2">**</ept> の代わりに <bpt id="p1">**</bpt>選択<ept id="p1">**</ept> を使用するか、<bpt id="p3">**</bpt>OCC を有効<ept id="p3">**</ept> プロパティを <bpt id="p4">**</bpt>はい<ept id="p4">**</ept> に設定します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="318">
          <source>BPCheckTablePropertyMismatch</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">BPCheckTablePropertyMismatch</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="319">
          <source>Description</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">説明</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="320">
          <source>This rule fails when the table belongs to a table group but doesn&amp;#39;t have the appropriate <bpt id="p1">&lt;strong&gt;</bpt>Cache Lookup<ept id="p1">&lt;/strong&gt;</ept> value.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このルールは、テーブルがテーブル グループに属しているが、適切な<bpt id="p1">&lt;strong&gt;</bpt>キャッシュ ルックアップ<ept id="p1">&lt;/strong&gt;</ept>値を持たない場合に失敗します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="321">
          <source>The rule fails if one of these conditions is met:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">次の条件がすべて満たされていると、ルールは失敗します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="322">
          <source>The <bpt id="p1">&lt;strong&gt;</bpt>Table Group<ept id="p1">&lt;/strong&gt;</ept> property is set to <bpt id="p2">&lt;strong&gt;</bpt>Main<ept id="p2">&lt;/strong&gt;</ept>, and the <bpt id="p3">&lt;strong&gt;</bpt>Cache Lookup<ept id="p3">&lt;/strong&gt;</ept> property is set to <bpt id="p4">&lt;strong&gt;</bpt>NotinTTS<ept id="p4">&lt;/strong&gt;</ept> or <bpt id="p5">&lt;strong&gt;</bpt>EntireTable<ept id="p5">&lt;/strong&gt;</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">&lt;strong&gt;</bpt>テーブル グループ<ept id="p1">&lt;/strong&gt;</ept> プロパティは <bpt id="p2">&lt;strong&gt;</bpt>メイン<ept id="p2">&lt;/strong&gt;</ept> に設定され、<bpt id="p3">&lt;strong&gt;</bpt>キャッシュ ルックアップ<ept id="p3">&lt;/strong&gt;</ept> プロパティは <bpt id="p4">&lt;strong&gt;</bpt>NotinTTS<ept id="p4">&lt;/strong&gt;</ept> または <bpt id="p5">&lt;strong&gt;</bpt>EntireTable<ept id="p5">&lt;/strong&gt;</ept> に設定されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="323">
          <source>The <bpt id="p1">&lt;strong&gt;</bpt>Table Group<ept id="p1">&lt;/strong&gt;</ept> property is set to <bpt id="p2">&lt;strong&gt;</bpt>Group<ept id="p2">&lt;/strong&gt;</ept> or <bpt id="p3">&lt;strong&gt;</bpt>Parameter<ept id="p3">&lt;/strong&gt;</ept>, and the <bpt id="p4">&lt;strong&gt;</bpt>Cache Lookup<ept id="p4">&lt;/strong&gt;</ept> property is set to <bpt id="p5">&lt;strong&gt;</bpt>NotinTTS<ept id="p5">&lt;/strong&gt;</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">&lt;strong&gt;</bpt>テーブル グループ<ept id="p1">&lt;/strong&gt;</ept> プロパティは <bpt id="p2">&lt;strong&gt;</bpt>グループ<ept id="p2">&lt;/strong&gt;</ept> または <bpt id="p3">&lt;strong&gt;</bpt>パラメーター<ept id="p3">&lt;/strong&gt;</ept> に設定され、<bpt id="p4">&lt;strong&gt;</bpt>キャッシュ ルックアップ<ept id="p4">&lt;/strong&gt;</ept> プロパティは <bpt id="p5">&lt;strong&gt;</bpt>NotinTTS<ept id="p5">&lt;/strong&gt;</ept> に設定されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="324">
          <source>The <bpt id="p1">&lt;strong&gt;</bpt>Table Group<ept id="p1">&lt;/strong&gt;</ept> property is set to <bpt id="p2">&lt;strong&gt;</bpt>WorksheetHeader<ept id="p2">&lt;/strong&gt;</ept>, <bpt id="p3">&lt;strong&gt;</bpt>WorksheetLine<ept id="p3">&lt;/strong&gt;</ept>, or <bpt id="p4">&lt;strong&gt;</bpt>Transaction<ept id="p4">&lt;/strong&gt;</ept>, and the <bpt id="p5">&lt;strong&gt;</bpt>Cache Lookup<ept id="p5">&lt;/strong&gt;</ept> property is set to <bpt id="p6">&lt;strong&gt;</bpt>Found<ept id="p6">&lt;/strong&gt;</ept>, <bpt id="p7">&lt;strong&gt;</bpt>FoundAndEmpty<ept id="p7">&lt;/strong&gt;</ept>, or <bpt id="p8">&lt;strong&gt;</bpt>EntireTable<ept id="p8">&lt;/strong&gt;</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">&lt;strong&gt;</bpt>テーブル グループ<ept id="p1">&lt;/strong&gt;</ept> プロパティは <bpt id="p2">&lt;strong&gt;</bpt>WorksheetHeader<ept id="p2">&lt;/strong&gt;</ept>、<bpt id="p3">&lt;strong&gt;</bpt>WorksheetLine<ept id="p3">&lt;/strong&gt;</ept>、または <bpt id="p4">&lt;strong&gt;</bpt>Transaction<ept id="p4">&lt;/strong&gt;</ept> に設定され、<bpt id="p5">&lt;strong&gt;</bpt>キャッシュ ルックアップ<ept id="p5">&lt;/strong&gt;</ept> プロパティは <bpt id="p6">&lt;strong&gt;</bpt>Found<ept id="p6">&lt;/strong&gt;</ept>、<bpt id="p7">&lt;strong&gt;</bpt>FoundAndEmpty<ept id="p7">&lt;/strong&gt;</ept>、または <bpt id="p8">&lt;strong&gt;</bpt>EntireTable<ept id="p8">&lt;/strong&gt;</ept> に設定されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="325">
          <source>Error message</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">エラー メッセージ</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="326">
          <source>%1 table has an invalid combination of table group and cache lookup</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">%1 テーブルにテーブル グループとキャッシュ ルックアップの無効な組み合わせがあります</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="327">
          <source>Issue type/severity</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">出庫タイプ/重要度</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="328">
          <source>MetaData/Warning</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">メタデータ/警告</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="329">
          <source>How to fix it</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">修正する方法</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="330">
          <source>Set an appropriate <bpt id="p1">&lt;strong&gt;</bpt>Cache Lookup<ept id="p1">&lt;/strong&gt;</ept> value on the table.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">テーブルで適切な <bpt id="p1">&lt;strong&gt;</bpt>キャッシュ ルックアップ<ept id="p1">&lt;/strong&gt;</ept> 値を設定します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="331">
          <source>BPCheckMissingDeleteActions</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">BPCheckMissingDeleteActions</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="332">
          <source>Description</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">説明</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="333">
          <source>This rule validates that the value of either a <bpt id="p1">**</bpt>delete<ept id="p1">**</ept> action or the <bpt id="p2">**</bpt>On Delete<ept id="p2">**</ept> property of a table relation isn't equal to <bpt id="p3">**</bpt>None<ept id="p3">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このルールは、テーブル関係の<bpt id="p1">**</bpt>削除<ept id="p1">**</ept>アクションまたは<bpt id="p2">**</bpt>削除時<ept id="p2">**</ept>プロパティの値が<bpt id="p3">**</bpt>なし<ept id="p3">**</ept>と等しくないことを検証します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="334">
          <source>The rule isn't triggered when the related or current table is a tempDB, in memory table, reference table, staging table, or parameter table.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">関連するテーブルまたは現在のテーブルが tempDB、メモリ テーブル、参照テーブル、ステージング テーブル、パラメーター テーブルの場合、ルールはトリガーされません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="335">
          <source>Error message</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">エラー メッセージ</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="336">
          <source>Delete actions missing in table %1 which is related to table %2 with relation name %3</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">リレーション名 <ph id="1">%3</ph> でテーブル <ph id="4">%2</ph> に関連付けられているテーブル <ph id="3">%1</ph> に欠けているアクションを削除します</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="337">
          <source>Issue type/severity</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">出庫タイプ/重要度</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="338">
          <source>MetaData/Warning</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">メタデータ/警告</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="339">
          <source>How to fix it</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">修正する方法</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="340">
          <source>Set a <bpt id="p1">**</bpt>delete<ept id="p1">**</ept> action value that isn't equal to <bpt id="p2">**</bpt>None<ept id="p2">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p2">**</bpt>None<ept id="p2">**</ept> と等しくない <bpt id="p1">**</bpt>delete<ept id="p1">**</ept> アクションを設定します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="341">
          <source>BPCheckAddressModel</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">BPCheckAddressModel</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="342">
          <source>Description</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">説明</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="343">
          <source>This rule fails if a table field is of the <bpt id="p1">**</bpt>AddressZipCodeId<ept id="p1">**</ept> or <bpt id="p2">**</bpt>AddressStateId<ept id="p2">**</ept> type.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">テーブル フィールドが <bpt id="p1">**</bpt>AddressZipCodeId<ept id="p1">**</ept> または <bpt id="p2">**</bpt>AddressStateId<ept id="p2">**</ept> タイプの場合、このルールは失敗します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="344">
          <source>These types indicate that the code didn't uptake the newer Address framework.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">これらのタイプは、コードが新しいアドレス フレームワークを受け入れなかったことを示します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="345">
          <source>Error message</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">エラー メッセージ</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="346">
          <source>Field %1 of table %2 is not part of address location model</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">テーブル <ph id="1">%2</ph> のフィールド <ph id="2">%1</ph> は、アドレスの場所モデルの一部ではありません</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="347">
          <source>Issue type/severity</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">出庫タイプ/重要度</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="348">
          <source>MetaData/Warning</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">メタデータ/警告</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="349">
          <source>How to fix it</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">修正する方法</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="350">
          <source>Replace these types with any other appropriate EDT type in the Directory model.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">これらのタイプをディレクトリ モデルのその他の適切な EDT タイプに置き換えます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="351">
          <source>BPCheckDimensionModel</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">BPCheckDimensionModel</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="352">
          <source>Description</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">説明</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="353">
          <source>This rule fails if a table field is of the <bpt id="p1">**</bpt>Dimension<ept id="p1">**</ept> or <bpt id="p2">**</bpt>LedgerAccount<ept id="p2">**</ept> type.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">テーブル フィールドが、<bpt id="p1">**</bpt>分析コード<ept id="p1">**</ept>または <bpt id="p2">**</bpt>LedgerAccount<ept id="p2">**</ept> タイプの場合、このルールは失敗します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="354">
          <source>These types indicate that the code didn't uptake the newer Financial Dimension framework.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">これらのタイプは、コードが新しい財務分析コード フレームワークを受け入れなかったことを示します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="355">
          <source>Error message</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">エラー メッセージ</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="356">
          <source>Field %1 of table %2 is not part of financial dimension framework</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">テーブル <ph id="1">%2</ph> のフィールド <ph id="2">%1</ph> は、財務分析コード フレームワークの一部ではありません</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="357">
          <source>Issue type/severity</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">出庫タイプ/重要度</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="358">
          <source>MetaData/Warning</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">メタデータ/警告</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="359">
          <source>How to fix it</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">修正する方法</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="360">
          <source>Replace these types with any other appropriate EDT type in the Dimensions model.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">これらのタイプを分析コード モデルのその他の適切な EDT タイプに置き換えます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="361">
          <source>BPCheckNumberofNewFields</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">BPCheckNumberofNewFields</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="362">
          <source>Description</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">説明</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="363">
          <source>This rule verifies that no more than 10 fields were added to a table during the process of customizing or extending that table.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このルールは、そのテーブルのカスタマイズまたは拡張のプロセスで、テーブルに 10 個以下のフィールドが追加されたことを確認します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="364">
          <source>This rule doesn't apply to staging tables.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このルールは、ステージング テーブルには適用されません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="365">
          <source>Error message</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">エラー メッセージ</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="366">
          <source>Number of new fields in table %1 is greater than</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">次の値より大きいテーブル %1 の新しいフィールドの数</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="367">
          <source>Issue type/severity</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">出庫タイプ/重要度</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="368">
          <source>Metadata/Warning</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">メタデータ/警告</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="369">
          <source>How to fix it</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">修正する方法</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="370">
          <source>Refactor your schema and create related tables instead of adding too many fields to an existing table.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">スキーマをリファクタリングし、既存のテーブルに多数のフィールドを追加する代わりに関連するテーブルを作成します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="371">
          <source>BPCheckEnumUpgradeIssue</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">BPCheckEnumUpgradeIssue</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="372">
          <source>Description</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">説明</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="373">
          <source>This rule fails when the following condition is met: When you customize an enum (overlayer), new enum values are less than the maximum existing value + 10.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このルールは、次の条件が満たされた場合に失敗します。列挙型 (オーバーレイ) をカスタマイズすると、新しい列挙型の値は既存の最大値 + 10 未満になります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="374">
          <source>This rules doesn't apply to extensible enums.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このルールは、拡張可能な列挙型には適用されません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="375">
          <source>Error message</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">エラー メッセージ</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="376">
          <source>Enum %1 will have upgrade issues</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">列挙 %1 で、アップグレード問題があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="377">
          <source>Issue type/severity</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">出庫タイプ/重要度</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="378">
          <source>MetaData/Warning</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">メタデータ/警告</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="379">
          <source>How to fix it</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">修正する方法</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="380">
          <source>Use larger enum values, or extend the enum.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">大きな列挙値を使用するか、列挙型を拡張します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="381">
          <source>BPCheckPassiveJoinUse</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">BPCheckPassiveJoinUse</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="382">
          <source>Description</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">説明</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="383">
          <source>This rule validates that, when a form allows for pre-loading of data, the link type of tab page data sources is passive.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このルールは、フォームがデータのプリロードを許可する場合、タブ ページ データソースのリンク タイプがパッシブであることを検証します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="384">
          <source>The rule fails if all the following conditions are met:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">次の条件がすべて満たされていると、ルールは失敗します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="385">
          <source>A form has the <bpt id="p1">&lt;strong&gt;</bpt>AllowPreLoading<ept id="p1">&lt;/strong&gt;</ept> property set to <bpt id="p2">&lt;strong&gt;</bpt>Yes<ept id="p2">&lt;/strong&gt;</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">&lt;strong&gt;</bpt>Yes<ept id="p1">&lt;/strong&gt;</ept> に設定された <bpt id="p2">&lt;strong&gt;</bpt>AllowPreLoading<ept id="p2">&lt;/strong&gt;</ept> プロパティのフォームがあります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="386">
          <source>A tab page on the form is bound to a top-level data source.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">フォームのタブ ページは、最上位レベルのデータ ソースにバインドされています。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="387">
          <source>The data source’s <bpt id="p1">&lt;strong&gt;</bpt>Join Source <ept id="p1">&lt;/strong&gt;</ept>property is set.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">データ ソースの<bpt id="p1">&lt;strong&gt;</bpt>結合ソース<ept id="p1">&lt;/strong&gt;</ept>プロパティが設定されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="388">
          <source>The data source’s <bpt id="p1">&lt;strong&gt;</bpt>Link Type<ept id="p1">&lt;/strong&gt;</ept> property isn&amp;#39;t set to <bpt id="p2">&lt;strong&gt;</bpt>Passive<ept id="p2">&lt;/strong&gt;</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">データ ソースの<bpt id="p1">&lt;strong&gt;</bpt>リンク タイプ<ept id="p1">&lt;/strong&gt;</ept> プロパティが<bpt id="p2">&lt;strong&gt;</bpt>パッシブ<ept id="p2">&lt;/strong&gt;</ept>に設定されていません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="389">
          <source>Error message</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">エラー メッセージ</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="390">
          <source>New message suggest: “Use passive joins on data sources %1 bound to a tab page control in form %2”</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">新しいメッセージは、「フォーム <ph id="1">%2</ph> のタブ ページ コントロールにバインドされているデータ ソース <ph id="2">%1</ph> にパッシブ結合を使用する」ことを提案しています</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="391">
          <source>Issue type/severity</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">出庫タイプ/重要度</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="392">
          <source>MetaData/Warning</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">メタデータ/警告</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="393">
          <source>How to fix it</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">修正する方法</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="394">
          <source>Set the <bpt id="p1">&lt;strong&gt;</bpt>AllowPreLoading<ept id="p1">&lt;/strong&gt;</ept> property to <bpt id="p2">&lt;strong&gt;</bpt>No<ept id="p2">&lt;/strong&gt;</ept> on the form, or use passive joins on the data source.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">フォームで <bpt id="p1">&lt;strong&gt;</bpt>AllowPreLoading<ept id="p1">&lt;/strong&gt;</ept> プロパティを <bpt id="p2">&lt;strong&gt;</bpt>いいえ<ept id="p2">&lt;/strong&gt;</ept> に設定するか、データ ソースでパッシブ結合を使用します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="395">
          <source>Passive joins require that you explicitly program when the query of a tab page is run.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">パッシブ結合では、タブ ページのクエリの実行時に明示的にプログラミングする必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="396">
          <source>BPCheckAltenateKeyAbsent</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">BPCheckAltenateKeyAbsent</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="397">
          <source>Description</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">説明</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="398">
          <source>This rule verifies that tables that have a unique index have at least one alternate key.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このルールは、一意のインデックスを持つテーブルに少なくとも 1 つの代替キーがあることを確認します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="399">
          <source>Error message</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">エラー メッセージ</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="400">
          <source>Table %1 does not have an alternate key</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">テーブル %1 には、代替キーがありません</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="401">
          <source>Issue type/severity</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">出庫タイプ/重要度</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="402">
          <source>MetaData/Warning</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">メタデータ/警告</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="403">
          <source>How to fix it</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">修正する方法</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="404">
          <source>Set the <bpt id="p1">**</bpt>Alternate Key<ept id="p1">**</ept> property to <bpt id="p2">**</bpt>Yes<ept id="p2">**</ept> on a unique index of the table.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">テーブルの一意のインデックスで <bpt id="p1">**</bpt>代替キー<ept id="p1">**</ept> プロパティを <bpt id="p2">**</bpt>はい<ept id="p2">**</ept> に設定します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="405">
          <source>BPCheckBaseTableModified</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">BPCheckBaseTableModified</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="406">
          <source>Description</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">説明</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="407">
          <source>This rule discourages the customization (overlayering) of a list of specific base tables that are shipped by Microsoft.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このルールは、Microsoft によって出荷される特定のベース テーブルの一覧のカスタマイズ (オーバーレイ化) を推奨しません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="408">
          <source>Examples are the SourceDocumentHeader and SourceDocumentLine tables.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">例では、SourceDocumentHeader および SourceDocumentLine テーブルがあります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="409">
          <source>Error message</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">エラー メッセージ</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="410">
          <source>%1 is a base table and must not be modified</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">%1 はベース テーブルであり、変更することはできません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="411">
          <source>Issue type/severity</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">出庫タイプ/重要度</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="412">
          <source>MetaData/Warning</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">メタデータ/警告</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="413">
          <source>How to fix it</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">修正する方法</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="414">
          <source>Don't customize the table.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">テーブルをカスタマイズしないでください。</target></trans-unit>
      </group>
    </body>
  </file>
</xliff>