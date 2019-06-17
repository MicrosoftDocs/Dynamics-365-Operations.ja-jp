<?xml version="1.0" encoding="UTF-8"?>
<xliff xmlns:logoport="urn:logoport:xliffeditor:xliff-extras:1.0" xmlns:tilt="urn:logoport:xliffeditor:tilt-non-translatables:1.0" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns="urn:oasis:names:tc:xliff:document:1.2" xmlns:xliffext="urn:microsoft:content:schema:xliffextensions" version="1.2" xsi:schemaLocation="urn:oasis:names:tc:xliff:document:1.2 xliff-core-1.2-transitional.xsd">
  <file datatype="xml" source-language="en-US" original="run-test-data-transfer-tool-beta.md" target-language="ja-JP">
    <header>
      <tool tool-company="Microsoft" tool-version="1.0-7889195" tool-name="mdxliff" tool-id="mdxliff"/>
      <xliffext:skl_file_name>run-test-data-transfer-tool-beta.1f5773.ce39c8e14565bcc3babf3051cf5d8caf0d92accf.skl</xliffext:skl_file_name>
      <xliffext:version>1.2</xliffext:version>
      <xliffext:ms.openlocfilehash>ce39c8e14565bcc3babf3051cf5d8caf0d92accf</xliffext:ms.openlocfilehash>
      <xliffext:ms.sourcegitcommit>9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b</xliffext:ms.sourcegitcommit>
      <xliffext:ms.lasthandoff>05/15/2019</xliffext:ms.lasthandoff>
      <xliffext:ms.openlocfilepath>articles\dev-itpro\lifecycle-services\ax-2012\run-test-data-transfer-tool-beta.md</xliffext:ms.openlocfilepath>
    </header>
    <body>
      <group extype="content" id="content">
        <trans-unit xml:space="preserve" translate="yes" id="101" restype="x-metadata">
          <source>Run the Test Data Transfer Tool (beta)</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">テスト データ転送ツール (ベータ) の実行</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="102" restype="x-metadata">
          <source>This topic provides information about how to run the Test Data Transfer Tool in Microsoft Dynamics AX.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このトピックでは、Microsoft Dynamics AX でデータ転送ツールのテストを実行する方法について説明します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="103">
          <source>Run the Test Data Transfer Tool (beta)</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">テスト データ転送ツール (ベータ) の実行</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="104">
          <source>Security and permissions</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">セキュリティおよびアクセス許可</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="105">
          <source>The Test Data Transfer Tool (beta) requires only Microsoft SQL Server permissions.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">テスト データ転送ツール (ベータ) には、Microsoft SQL Server アクセス許可のみが必要です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="106">
          <source>The Test Data Transfer Tool (beta) does not in any way recognize the security mechanisms that are built into Microsoft Dynamics AX.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">テスト データ転送ツール (ベータ) では、Microsoft Dynamics AX に組み込まれているセキュリティ メカニズムはまったく認識されません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="107">
          <source>If you have permission to execute <bpt id="p1">**</bpt>SELECT<ept id="p1">**</ept> statements in SQL Server Management Studio or to use the SQL Server bulk copy tool (bcp) to export data, you have the permissions that are required to export data by using the Test Data Transfer Tool (beta).</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>SELECT<ept id="p1">**</ept> ステートメントを SQL Server Management Studio で実行する権限がある場合、または SQL Server 一括コピー ツール (bcp) を使用してデータをエクスポートする権限がある場合は、テスト データ転送ツール (ベータ) を使用してデータをエクスポートするために必要なアクセス許可が与えられます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="108">
          <source>The following SQL Server permissions are required during export:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">エクスポート時には、次の SQL Server のアクセス許可が必要です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="109">
          <source>Read permission to the sys schema to read tables, indexes, and sysdatabases</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">テーブル、インデックス、および sysdatabases を読み取るための sys スキーマへの読み取りのアクセス許可</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="110">
          <source>Read permission to the ModelElements view</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ModelElements ビューへの読み取りアクセス許可</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="111">
          <source>Read permission to the SQLDictionary table</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">SQLDictionary テーブルへの読み取りアクセス許可</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="112">
          <source>Read permission to the ElementType table</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ElementType テーブルへの読み取りアクセス許可</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="113">
          <source>Read permission to the ModelElement table</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ModelElement テーブルへの読み取りアクセス許可</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="114">
          <source>Read permission to the table that you are exporting</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">エクスポート先テーブルの読み取りアクセス許可</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="115">
          <source>If you have permission to execute <bpt id="p1">**</bpt>SELECT<ept id="p1">**</ept> statements and <bpt id="p2">**</bpt>BULK INSERT<ept id="p2">**</ept> statements in SQL Server Management Studio, you have the permissions that are required to import data by using the tool.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">SQL Server Management Studio の <bpt id="p1">**</bpt>SELECT<ept id="p1">**</ept> ステートメントおよび <bpt id="p2">**</bpt>BULK INSERT<ept id="p2">**</ept> ステートメントを実行する権限がある場合は、ツールを使用してデータをインポートするために必要なアクセス許可が与えられています。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="116">
          <source>The following SQL Server permissions are required during import:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">インポート時には、次の SQL Server のアクセス許可が必要です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="117">
          <source>Read permission to the sys schema to read tables, indexes, and sysdatabases</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">テーブル、インデックス、および sysdatabases を読み取るための sys スキーマへの読み取りのアクセス許可</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="118">
          <source>Read permission to the ModelElements view</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ModelElements ビューへの読み取りアクセス許可</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="119">
          <source>Read permission to the SQLDictionary table</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">SQLDictionary テーブルへの読み取りアクセス許可</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="120">
          <source>Read permission to the ElementType table</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ElementType テーブルへの読み取りアクセス許可</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="121">
          <source>Read permission to the ModelElement table</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ModelElement テーブルへの読み取りアクセス許可</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="122">
          <source>Read/write permission to the SYSTEMSEQUENCES table</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">SYSTEMSEQUENCES テーブルの読み取り/書き込みアクセス許可</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="123">
          <source>Write permission to the table that you are importing</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">インポート先テーブルのアクセス許可を記述</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="124">
          <source>Permission to execute <bpt id="p1">**</bpt>ALTER INDEX<ept id="p1">**</ept> on the table that you are importing, if the data violates unique index constraints and you want the index to be disabled automatically</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">インポートするテーブルで <bpt id="p1">**</bpt>ALTER INDEX<ept id="p1">**</ept> を実行するアクセス許可。データが固有のインデックス制約に違反し、インデックスを自動的に無効化する場合。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="125">
          <source>Appropriate permissions for any SQL commands that are found in the <ph id="ph1">\[</ph>Import<ph id="ph2">\]</ph> directory</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><ph id="ph1">\[</ph>インポート<ph id="ph2">\]</ph>ディレクトリにある SQL コマンドに対する適切なアクセス許可</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="126">
          <source>Run the tool</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ツールを実行</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="127">
          <source>You must run the Test Data Transfer Tool (beta) from a system that has the SQL Server client tools installed, so that the bcp utility is in the command-prompt path.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">bcp ユーティリティがコマンド プロンプト パスに含まれるように、SQL Server クライアント ツールがインストールされているシステムからテスト データ転送ツール (beta) を実行する必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="128">
          <source>You must run the tool directly from the computer that is hosting the database during import.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このツールは、インポート中にデータベースをホストしているコンピューターから直接実行する必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="129">
          <source>To run the Test Data Transfer Tool (beta), follow these steps.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">テスト データ転送ツール (ベータ) を実行するには、次の手順を実行します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="130">
          <source>Stop the instance of Microsoft Dynamics AX Application Object Server (AOS).</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Microsoft Dynamics AX Application Object Server (AOS) のインスタンスを停止します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="131">
          <source>Run the Test Data Transfer Tool (beta) (DP.exe).</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">テスト データ転送ツール (ベータ) を実行します (DP.exe)。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="132">
          <source>Include arguments that describe the action to take.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">実行するアクションを記述する引数を含めます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="133">
          <source>As the tool runs, the following information is displayed:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ツールの実行では、次の情報が表示されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="134">
          <source>The tool’s progress</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ツールの進捗状況</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="135">
          <source>The number of tables that must still be processed</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">まだ処理する必要があるテーブルの数</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="136">
          <source>The number of errors that have occurred</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">発生したエラー数</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="137">
          <source>After processing is completed, the tool writes the DPLog.xml log file to the current directory.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">処理が完了した後、ツールは、現在のディレクトリに DPLog.xml ログ ファイルを書き込みます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="138">
          <source>To find errors, search for ‘failed’ in the log file.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">エラーを見つけるには、ログ ファイルで ‘failed’ を検索します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="139">
          <source>Syntax</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">構文</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="140">
          <source>All arguments are optional.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">すべての引数はオプションです。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="141">
          <source>Parameter</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">パラメーター</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="142">
          <source>Default value</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">既定値</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="143">
          <source>Description</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">説明</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="144">
          <source><bpt id="p1">*</bpt>direction<ept id="p1">*</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">*</bpt>方向<ept id="p1">*</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="145">
          <source>EXPORT</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">エクスポート</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="146">
          <source>Specify EXPORT to export data or IMPORT to import data.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">データをエクスポートには EXPORT、データをインポートするには IMPORT を指定します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="147">
          <source><bpt id="p1">*</bpt>directory<ept id="p1">*</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">*</bpt>ディレクトリ<ept id="p1">*</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="148">
          <source>The current directory</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">現在のディレクトリ</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="149">
          <source>Specify the directory from which the data should be exported or to which the data should be imported.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">データのエクスポート元またはデータのインポート先のディレクトリを指定します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="150">
          <source><bpt id="p1">*</bpt>database<ept id="p1">*</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">*</bpt>データベース<ept id="p1">*</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="151">
          <source>AXDB</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">AXDB</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="152">
          <source>The name of the database.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">データベースの名前です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="153">
          <source><bpt id="p1">*</bpt>server<ept id="p1">*</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">*</bpt>サーバー<ept id="p1">*</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="154">
          <source>The current computer</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">現在のコンピューター</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="155">
          <source>Specify the computer name or instance name of the SQL Server computer that is hosting the Microsoft Dynamics AX database.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Microsoft Dynamics AX データベースをホストしている SQL Server コンピューターのコンピューター名またはインスタンス名を指定します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="156">
          <source>To specify an instance name, enter it in the format ServerNameInstanceName.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">インスタンス名を指定するには、ServerNameInstanceName の形式で入力します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="157">
          <source>If you have a named instance on a local computer, you can use the format localhostInstanceName or InstanceName.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ローカル コンピューターの名前付きインスタンスがある場合は、localhostInstanceName または InstanceName という形式を使用できます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="158">
          <source>You can view a summary of the command-line options by using the following command.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">コマンド ライン オプションの概要を表示するには、次のコマンドを使用できます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="159">
          <source>Stop the tool</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ツールを停止</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="160">
          <source>To stop the tool, press Ctrl+C.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ツールを停止するには、Ctrl キーを押しながら C キーを押します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="161">
          <source>The tool finishes the tables that it is currently working on and then closes.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ツールは、現在作業中のテーブルを終了して終了します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="162">
          <source>Overview of data export and import</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">データのエクスポートとインポートの概要</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="163">
          <source>The Test Data Transfer Tool (beta) exports and imports three files for each Microsoft Dynamics AX table.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">テスト データ転送ツール (ベータ) は、Microsoft Dynamics AX のテーブルごとに 3 つのファイルをエクスポートおよびインポートします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="164">
          <source>If tables have dependencies in Microsoft Dynamics AX, these files support the capability of the tool to export and import the tables independently of related tables.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">テーブルに Microsoft Dynamics AX での依存関係がある場合、これらのファイルは、関連テーブルに関係なくテーブルをエクスポートおよびインポートするためのツールの機能をサポートします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="165">
          <source>The following diagram shows the export and import process.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">次の図は、エクスポートとインポートのプロセスを示しています。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="166">
          <source>Process of exporting and importing data</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">データのエクスポートとインポートを実行するプロセス</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="167">
          <source>Export and import process</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">プロセスをエキスポートおよびインポート</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="168">
          <source>The following table describes the three types of files.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">次のテーブルでは、ファイルの 3 つのタイプについて説明します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="169">
          <source>File type</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ファイル タイプ</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="170">
          <source>Description</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">説明</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="171">
          <source>.out</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">.out</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="172">
          <source>A bcp data file that contains table data.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">テーブル データを含む bcp データ ファイル。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="173">
          <source>Columns are separated by \ #&amp;#124;EOC&amp;#124;<ph id="ph1">\#</ph>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">列は \ #&amp;#124;EOC&amp;#124;<ph id="ph1">\#</ph> で区切られます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="174">
          <source>Rows are separated by <ph id="ph1">\#</ph> &amp;#124;EOR &amp;#124;<ph id="ph2">\#</ph>n.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">列は <ph id="ph1">\#</ph> &amp;#124;EOR &amp;#124;<ph id="ph2">\#</ph>n で区切られます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="175">
          <source>.xml</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">.xml</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="176">
          <source>A bcp data file that contains the table metadata (column descriptions).</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">テーブル メタデータ (列の説明) を含む bcp データ ファイル。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="177">
          <source>.outmodel</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">.outmodel</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="178">
          <source>A file that contains metadata that is specific to Microsoft Dynamics AX.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Microsoft Dynamics AX に固有のメタデータを含むファイルです。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="179">
          <source>This metadata includes all names and IDs of the table and its fields.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このメタデータには、テーブルとそのフィールドのすべての名前と ID が含まれます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="180">
          <source>This file also includes the <bpt id="p1">**</bpt>elementType<ept id="p1">**</ept> attribute, which stores the names and IDs of any Microsoft Dynamics AX tables, classes, or extended data types that are referenced by the table.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このファイルには、<bpt id="p1">**</bpt>elementType<ept id="p1">**</ept> 属性も含まれています。この属性は、テーブルで参照される Microsoft Dynamics AX のテーブル、クラス、または拡張データ型の名前と ID を格納します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="181">
          <source>This information is used during import to match up fields that have been renamed.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この情報は、インポート中に名前が変更されたフィールドを照合するために使用されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="182">
          <source>The information is also used to update the table IDs, class IDs, or data type IDs so that those IDs match the IDs in the target database.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">また、これらの ID がターゲット データベース内の ID と一致するように、テーブル ID、クラス ID、またはデータ タイプ ID を更新するためにも使用されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="183">
          <source>Data in the .outmodel file is constructed from the Metadata.xml file.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">.outmodel ファイルのデータは、Metadata.xml ファイルから作成されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="184">
          <source>This file is generated by an X++ job that you run from Microsoft Dynamics AX on the source database.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このファイルは、ソース データベースの Microsoft Dynamics AX から実行する X++ ジョブによって生成されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="185">
          <source>When the Test Data Transfer Tool (beta) exports data, the Metadata.xml file is used to identify table relationships and EDT references that require additional information during import.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">テスト データ転送ツール (beta) がデータをエクスポートするとき、インポート時に追加情報を必要とする、テーブルのリレーションシップおよび EDT 参照を識別するために Metadata.xml ファイルが使用されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="186">
          <source>This additional information is included in the .outmodel file that the tool exports.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この追加情報は、ツールがエクスポートする .outmodel ファイルに含まれています。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="187">
          <source>It is important that you maintain an updated .outmodel file in some scenarios, such as scenarios that involve table inheritance.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">テーブルの継承に関連するシナリオなど一部のシナリオでは、更新された .outmodel ファイルを維持することが重要です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="188">
          <source>Each row in the <bpt id="p1">**</bpt>SuperType<ept id="p1">**</ept> table includes an <bpt id="p2">**</bpt>InstanceRelationType<ept id="p2">**</ept> column that contains the Microsoft Dynamics AX ID of the <bpt id="p3">**</bpt>SubType<ept id="p3">**</ept> table for that row.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>SuperType<ept id="p1">**</ept> テーブルの各行は、その行の <bpt id="p3">**</bpt>SubType<ept id="p3">**</ept> テーブルの Microsoft Dynamics AX ID を含む <bpt id="p2">**</bpt>InstanceRelationType<ept id="p2">**</ept> コラムが含まれます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="189">
          <source>Because the Microsoft Dynamics AX IDs can change over time, the data in the .out file can become inaccurate.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Microsoft Dynamics AX の ID は時間経過に伴い変更可能であるため、.out ファイルのデータは不正確になる場合があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="190">
          <source>The Test Data Transfer Tool (beta) uses information from the Metadata.xml file to avoid this situation and to make sure that the data is imported correctly.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">テスト データ転送ツール (ベータ) は、Metadata.xml ファイルからの情報を使用して、この状況を回避し、データが正しくインポートされるようにします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="191">
          <source>When you import files, make sure that the Metadata.xml file is current.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ファイルをインポートするときは、Metadata.xml ファイルが最新であることを確認します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="192">
          <source>During the import process, the tool uses the .outmodel file to recognize the relationships.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">インポート プロセス中に、ツールは .outmodel ファイルを使用して関係を認識します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="193">
          <source>The tool then queries Microsoft Dynamics AX to make sure that the data is imported correctly.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このツールは、Microsoft Dynamics AX にクエリを実行して、データが正しくインポートされるようにします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="194">
          <source>For example, the .outmodel file indicates that the value to insert into the <bpt id="p1">**</bpt>InstanceRelationType<ept id="p1">**</ept> column is <bpt id="p2">**</bpt>1234<ept id="p2">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">たとえば、.outmodel ファイルは、<bpt id="p1">**</bpt>InstanceRelationType<ept id="p1">**</ept> 列に挿入する値が <bpt id="p2">**</bpt>1234<ept id="p2">**</ept> であることを示します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="195">
          <source>However, the tool recognizes that new tables have been added to the new Microsoft Dynamics AX ID for which the subtype table is <bpt id="p1">**</bpt>1235<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ただし、ツールは、サブタイプ テーブルが <bpt id="p1">**</bpt>1235<ept id="p1">**</ept> である新しい Microsoft Dynamics AX ID に新しいテーブルが追加されたことを認識します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="196">
          <source>When you use a Metadata.xml file that is out of date, the data is usually imported and exported without any errors.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">期限が切れている Metadata.xml ファイルを使用したとき、データは通常、エラーを発生させずにインポートおよびエクスポートされます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="197">
          <source>This lack of errors can make it difficult to diagnose issues.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このエラーの欠如は、問題の診断を困難にする可能性があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="198">
          <source>The Microsoft Dynamics AX IDs that are included in the .out file are typically correct.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">.out ファイルに含まれている Microsoft Dynamics AX ID は、通常正確です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="199">
          <source>However, when a table’s Microsoft Dynamics AX ID changes, the data import is completed successfully, but incorrect values are added in the Microsoft Dynamics AX ID field.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ただし、テーブルの Microsoft Dynamics AX ID が変更されると、データ インポートが正常に完了しても、不正確な値が Microsoft Dynamics AX ID フィールドに追加されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="200">
          <source>For example, payroll data contains some inheritance tables that are related to the setup of an employee’s payroll tax.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">たとえば、給与データには、従業員の給与税の設定に関連するいくつかの継承テーブルが含まれます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="201">
          <source>If you load data that was exported by using an outdated Metadata.xml file, several issues occur that involve the inheritance relationships in the tables.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">古い Metadata.xml ファイルを使用してエクスポートされたデータを読み込むと、テーブルの継承関係を含むいくつかの問題が発生します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="202">
          <source>When you are running Microsoft Dynamics AX as an administrator, the inheritance relationships can be correctly resolved, and the payroll payments are then generated correctly.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Microsoft Dynamics AX を管理者として実行している場合は、継承関係を正しく解決できるし、給与支払が正常に生成されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="203">
          <source>However, if you are running Microsoft Dynamics AX as a non-administrator, the X++ code does not read the records from the database.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ただし、Microsoft Dynamics AX を非管理者として実行する場合、X++ コードはデータベースからのレコードを読み取りません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="204">
          <source>Therefore, the payroll payments that are generated do not include any taxes.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">したがって、生成される給与支払には税金は含まれません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="205">
          <source>Exporting data</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">データのエクスポート</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="206">
          <source>The procedure for exporting data consists of the following general steps:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">データをエクスポートする手順は、次の一般的なステップで構成されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="207">
          <source>Generate a Metadata.xml file.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Metadata.xml ファイルを生成します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="208">
          <source>Determine which data to export.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">エクスポートするデータを決定します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="209">
          <source>Run the tool.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ツールを実行します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="210">
          <source>Generate the Metadata.xml file</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Metadata.xml ファイルを生成します</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="211">
          <source>Before you use the Test Data Transfer Tool (beta) to export data, you must generate the Metadata.xml file on the source system.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">テスト データ転送ツール (ベータ) を使用してデータをエクスポートする前に、ソース システムで Metadata.xml ファイルを生成する必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="212">
          <source>The Metadata.xml file is used only during export.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Metadata.xml ファイルは、エクスポート中にのみ使用されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="213">
          <source>The Metadata.xml file can become out of date if you do not update it periodically.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Metadata.xml ファイルは、定期的に更新されない場合に古くなる可能性があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="214">
          <source>If the file is out of date, the exported data might not contain the <bpt id="p1">**</bpt>elementType<ept id="p1">**</ept> attribute, and the import might not update the IDs to match the IDs in the target database.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ファイルの有効期限が切れている場合、エクスポートしたデータに<bpt id="p1">**</bpt>要素型<ept id="p1">**</ept>属性が含まれていない可能性があり、インポートによって、ターゲット データベースで ID が一致するように ID がアップデートされない可能性があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="215">
          <source>You must update the file manually.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">手動でファイルを更新する必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="216">
          <source>To update the Metadata.xml file, follow these steps.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Metadata.xml ファイルを更新するには、次の手順を実行します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="217">
          <source>Import the MetadataXMLGenerator.xpo from the same folder that DP.exe is stored in, and then run the MetadataXMLGenerator job.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">DP.exe が格納されている同じフォルダーの MetadataXMLGenerator.xpo をインポートしてから、MetadataXMLGenerator ジョブを実行します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="218">
          <source>A new Metadata.xml file is created in a temporary folder on your computer.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">新しい Metadata.xml ファイルは、コンピューター上の一時フォルダーに作成されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="219">
          <source>Locate the new Metadata.xml file in one of the following ways:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">次の方法のいずれかで新しい Metadata.xml ファイルを検索します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="220">
          <source>When the MetadataXMLGenerator job is completed, the path of the new Metadata.xml file is provided in the Infolog.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">MetadataXMLGenerator ジョブが完了すると、新しい Metadata.xml ファイルのパスが情報ログに用意されています。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="221">
          <source>Open a Command Prompt window, and enter <bpt id="p1">**</bpt>echo %temp%<ept id="p1">**</ept> to view the path of the temporary folder where the Metadata.xml file is stored.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">コマンド プロンプト ウィンドウを開いて <bpt id="p1">**</bpt>echo %temp%<ept id="p1">**</ept> と入力し、Metadata.xml ファイルが保存されている一時フォルダーのパスを表示します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="222">
          <source>Navigate to the temporary folder, and then copy the Metadata.xml file to the subfolder where the Test Data Transfer Tool (beta) is installed.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">一時フォルダーに移動してから、テスト データ転送ツール (ベータ) がインストールされているサブフォルダーに Metadata.xml ファイルをコピーします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="223">
          <source>If there is an existing Metadata.xml file in the <ph id="ph1">\[</ph>Lists<ph id="ph2">\]</ph> subfolder, overwrite the existing Metadata.xml file by using the Metadata.xml file that you just generated.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><ph id="ph1">\[</ph>リスト<ph id="ph2">\]</ph> サブフォルダーに既存の Metadata.xml ファイルがある場合、生成された Metadata.xml ファイルを使用することによって、既存のエクスポートできるファイルを上書きします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="224">
          <source>Choose data to export</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">エクスポートするデータの選択</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="225">
          <source>The Test Data Transfer Tool (beta) is designed to export all data from all tables in the database, unless tables, columns, or rows are filtered out of the exported data.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">テスト データ転送ツール (ベータ) は、データベース内のすべてのテーブルのすべてのデータをエクスポートするように設計されています。ただし、エクスポートしたデータから、テーブル、列、または行がフィルタ処理により除かれている場合があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="226">
          <source>The tool is preconfigured to include a set of filters that filter out many tables.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このツールは、多くのテーブルを除外するフィルターのセットを含むように事前設定されています。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="227">
          <source>The preconfigured filters are based on the following guidelines:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">コンフィギュレーション済のフィルターは、次のガイドラインに基づいています。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="228">
          <source>Do not export tables that contain code or models.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">コードやモデルを含むテーブルをエクスポートしないでください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="229">
          <source>Do not export security settings.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">セキュリティ設定をエクスポートしないでください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="230">
          <source>Do not export computer-specific data.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">コンピューターの固有データをエクスポートしないでください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="231">
          <source>Do not export user-specific data.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ユーザーの固有データをエクスポートしないでください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="232">
          <source>Do not export temp tables.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">一時的なテーブルをエクスポートしないでください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="233">
          <source>These filters might not be complete or appropriate for your requirements.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">これらのフィルタは、要件に完全ではないかもしれません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="234">
          <source>For example, you might want to export some of the data that is filtered out by default, or you might have additional tables that should not be exported.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">たとえば、既定でフィルター除外されるデータの一部をエクスポートする、またはエクスポートされない追加のテーブルがある場合があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="235">
          <source>If a table contains a <bpt id="p1">**</bpt>RecVersion<ept id="p1">**</ept> column, the Test Data Transfer Tool (beta) ignores the current value in the table and always exports the table by using the value 1.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">テーブルが含まれている場合、<bpt id="p1">**</bpt>RecVersion<ept id="p1">**</ept>列で、テスト データ転送ツール (beta) テーブルで現在の値を無視し、常に1の値を使用して、テーブルをエクスポートします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="236">
          <source>This feature makes it much easier to compare .out files and see only meaningful differences.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この機能を使用すると、.out ファイルを比較して意味のある違いのみを簡単に確認できます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="237">
          <source>This feature is especially useful when you keep your data in a version control system.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この機能は、データをバージョン管理システムに保存する場合に特に便利です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="238">
          <source>Most Microsoft Dynamics AX tables contain a <bpt id="p1">**</bpt>RecVersion<ept id="p1">**</ept> column.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ほとんどの Microsoft Dynamics AX テーブルには、<bpt id="p1">**</bpt>RecVersion<ept id="p1">**</ept> 列が含まれます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="239">
          <source>The following table describes the export strategies that are used in the standard exclude files and the Filters.xml file.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">次のテーブルでは、標準除外ファイルと Filters.xml ファイルで使用されるエクスポート方法について説明します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="240">
          <source>Content of the table</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">テーブルのコンテンツ</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="241">
          <source>Export strategy</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">戦略をエクスポート</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="242">
          <source>Reason</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">理由</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="243">
          <source>Code, system data, or user data that is not connected to the business data</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">業務データに接続されていないコード、システム データ、またはユーザー データ</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="244">
          <source>Exclude this table from export.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">エクスポートからテーブルを除外</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="245">
          <source>This strategy prevents data from being unintentionally changed when business data is imported.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この戦略により、ビジネス データのインポート時に意図しないデータの変更が防止されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="246">
          <source>Cached values that are calculated from business data</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">業務データから計算されるキャッシュされた値</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="247">
          <source>Export an empty .out file.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">空の .out ファイルをエクスポートします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="248">
          <source>This strategy helps control the content of the table when the table is imported, because the content depends on business data.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この戦略は、コンテンツがビジネス データに依存するため、テーブルをインポートするときにテーブルのコンテンツを制御するのに役立ちます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="249">
          <source>An .out file is required, but we do not want to store values that can be recalculated from the source data.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">.out ファイルは必須ですが、ソース データから再計算することができる値を格納しないためです。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="250">
          <source>Therefore, an empty .out file is exported.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">したがって、空の .out ファイルがエクスポートされます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="251">
          <source>Export data</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">データのエクスポート</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="252">
          <source>After you have generated the Metadata.xml file and chosen the data to export, you can export the file.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Metadata.xml ファイルを生成し、エクスポートするデータを選択した後、ファイルをエクスポートできます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="253">
          <source>The Test Data Transfer Tool (beta) does not create any temporary files during export.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">テスト データ転送ツール (ベータ) では、エクスポート中に一時ファイルは作成されません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="254">
          <source>The Test Data Transfer Tool (beta) generates SQL statements from the content of the <ph id="ph1">\[</ph>Lists<ph id="ph2">\]</ph>Filters.xml file.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">テスト データ転送ツール (ベータ) は、<ph id="ph1">\[</ph>リスト<ph id="ph2">\]</ph>Filters.xml ファイルの内容から SQL ステートメントを生成します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="255">
          <source>In particular, the content of the <ph id="ph1">&amp;lt;</ph>filter<ph id="ph2">&amp;gt;</ph> element can contain arbitrary SQL statements that are executed in your user context during export.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">特に、<ph id="ph1">&amp;lt;</ph>フィルター<ph id="ph2">&amp;gt;</ph>要素の内容には、エクスポート中にユーザーのコンテキストで実行される任意の SQL ステートメントを含むことができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="256">
          <source>Make sure that you thoroughly test all changes to the Filters.xml file before you modify it.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">変更する前に Filters.xml ファイルへのすべての変更を十分にテストしてください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="257">
          <source>Export filtering</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">フィルタリングをエクスポート</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="258">
          <source>When you export data by using the Microsoft Dynamics AX 2012 Test Data Transfer Tool (beta), you can prevent the tool from exporting data in three ways:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Microsoft Dynamics AX 2012 テスト データ転送ツール (beta) を使用してデータをエクスポートするとき、次の 3 つの方法で、このツールによるデータのエクスポートを回避できます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="259">
          <source>Exclude  or include tables</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">テーブルを除外または含む</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="260">
          <source>Exclude columns</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">列を除外</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="261">
          <source>Exclude rows</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">行を除外</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="262">
          <source>Create an exclude file to exclude tables from the export</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">エクスポートからテーブルを除外する除外ファイルを作成する</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="263">
          <source>To exclude a table or a set of tables from the exported data, follow these steps.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">エクスポートされたデータからテーブルまたはテーブルのセットを除外するには、次の手順を実行します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="264">
          <source>Add a text file in the <ph id="ph1">\[</ph>Lists<ph id="ph2">\]</ph> directory.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><ph id="ph1">\[</ph>一覧表示<ph id="ph2">\]</ph>ディレクトリのテキスト ファイルを追加します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="265">
          <source>The file name must start with <bpt id="p1">**</bpt>Exclude –<ept id="p1">**</ept> (the space and hyphen are part of the name), and the file name extension must be <bpt id="p2">**</bpt>.txt<ept id="p2">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ファイル名は、<bpt id="p1">**</bpt>Exclude –<ept id="p1">**</ept> (スペースとハイフンは名前の一部です) で始まり、ファイル名の拡張子は <bpt id="p2">**</bpt>.txt<ept id="p2">**</ept> でなければなりません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="266">
          <source>You can also modify an existing file.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">また、既存のファイルを変更することができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="267">
          <source>In the text file, add a line that contains a regular expression that matches the name of the table or tables to exclude from the export.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">テキスト ファイルで、エクスポートから除外するテーブルの名前に一致する正規表現を含む行を追加します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="268">
          <source>When a table is excluded, no files are created for that table during the export.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">テーブルが除外されると、エクスポート時にそのテーブルに対してファイルが作成されません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="269">
          <source>The regular expression that you provide is matched against the name of the table as that name appears in the SQL Server database.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">指定した正規表現は、その名前が SQL Server データベースに表示されるため、テーブルの名前と照合されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="270">
          <source>Differences in capitalization are disregarded.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">大文字と小文字の違いは無視されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="271">
          <source>Additionally, the Test Data Transfer Tool (beta) adds anchors to the regular expression from the exclude file to make sure that tables are excluded only if the whole name matches the regular expression.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">また、テスト データ転送ツール (ベータ) は、除外ファイルから正規表現にアンカーを追加して、名前全体が正規表現と一致する場合にのみテーブルが除外されていることを確認します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="272">
          <source>The tool uses Microsoft .NET regular expression syntax.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このツールでは、Microsoft .NET 正規表現構文を使用します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="273">
          <source>The exclude file format lets you enter blank lines, so that you can create separate groups for expressions in a single file.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">除外ファイル形式では空白行を入力できるため、1 つのファイルで式のグループを個別に作成できます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="274">
          <source>The file format also lets you enter single-line comments (where the line starts with //), so that you can provide comments that describe why the tables have been excluded.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ファイル形式では、(行が // で始まる) 単一行のコメントを入力できるため、表が除外された理由を説明するコメントを入力できます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="275">
          <source>Examples of excluding tables from the export</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">エクスポートからテーブルを除外する例</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="276">
          <source>To exclude only the table that is named SysVersionControlParameters, use the following regular expression.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">SysVersionControlParameters という名前のテーブルのみを除外するには、次の正規表現を使用します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="277">
          <source>// Exclude 1 table SYSVERSIONCONTROLPARAMETERS</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">// SYSVERSIONCONTROLPARAMETERS のテーブルを除外します</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="278">
          <source>To exclude all tables that have names that start with SysVersionControl, use the following regular expression.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">SysVersionControl で始まる名前を持つすべてのテーブルを除外するには、次の正規表現を使用します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="279">
          <source>// Exclude multiple tables SYSVERSIONCONTROL.*</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">// SYSVERSIONCONTROL* の複数のテーブルを除外します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="280">
          <source>Including tables in the export</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">エクスポートにテーブルを含める</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="281">
          <source>Typically, you specify the data that is exported by describing the tables that you do not want to export.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">通常、エクスポートしないテーブルを記述してエクスポートするデータを指定します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="282">
          <source>However, if you want to describe the tables that you do want to export, you can use a regular expression in an exclude list.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ただし、エクスポートするテーブルを記述する場合、除外リストで正規表現を使用できます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="283">
          <source>Just create a regular expression that matches all tables except the tables that you want to export.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">エクスポートするテーブル以外のすべてのテーブルに一致する正規表現を作成します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="284">
          <source>The following table describes the syntax that you can include in your regular expression.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">次のテーブルに、正規表現に含めることができる構文を示します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="285">
          <source>Regular expression syntax</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">正規表現の構文</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="286">
          <source>Description</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">説明</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="287">
          <source>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="288">
          <source>Match any single character.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">任意の 1 文字と一致します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="289">
          <source>Match the previous expression zero or more times.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">前の式と 0 回以上一致します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="290">
          <source>(?<ph id="ph1">&amp;lt;</ph>!</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">(?<ph id="ph1">&amp;lt;</ph>!</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="291">
          <source>subexpression)</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">subexpression)</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="292">
          <source>Prevent a match if the end of the previously matched content matches the subexpression.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">以前に一致したコンテンツの末尾が部分式と一致する場合は、一致を禁止します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="293">
          <source>This expression is known as a zero-width negative lookbehind assertion.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この式は、ゼロ幅後読みアサーションと呼ばれます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="294">
          <source>Match the start of the string.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">文字列の開始と一致します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="295">
          <source>To specify tables, first define a regular expression that starts with .<ph id="ph1">\*</ph> to match all tables.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">テーブルを指定するには、最初に <ph id="ph1">\*</ph> で始まる正規表現を定義して、すべてのテーブルに一致させます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="296">
          <source>Then append a zero-width negative lookbehind assertion for each table that you want to export.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">次に、エクスポートするテーブルごとに幅ゼロの負の lookbehind アサーションを追加します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="297">
          <source>The subexpression in each assertion is the name of the table that is anchored to the start of the string.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">各アサーションの部分式は、文字列の先頭に固定されているテーブルの名前です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="298">
          <source>For example, to export only the InventTable and DocuRef tables, use the following regular expression.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">たとえば、InventTable および DocuRef テーブルのみをエクスポートするには、次の正規表現を使用します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="299">
          <source>// Match all tables except InventTable and DocuRef .*(?&lt;!^InventTable)(?&lt;!^DocuRef)</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">// InventTable および DocuRef を除くすべてのテーブルに一致させます。*(?&lt;!^InventTable)(?&lt;!^DocuRef)</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="300">
          <source>For each additional table that you want to export, append (?<ph id="ph1">&amp;lt;</ph>!^NameOfTable) to the same regular expression.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">エクスポートする追加のテーブルごとに、同じ正規表現に (?<ph id="ph1">&amp;lt;</ph>!^ NameOfTable) を追加します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="301">
          <source>Exclude columns from the export</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">エクスポートから列を除外</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="302">
          <source>To exclude a column or columns from the exported data, follow these steps.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">エクスポートされたデータから列を除外するには、次の手順を実行します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="303">
          <source>Open <bpt id="p1">**</bpt><ph id="ph1">\[</ph>Lists<ph id="ph2">\]</ph>Filters.xml<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt><ph id="ph1">\[</ph>Lists<ph id="ph2">\]</ph>Filters.xml<ept id="p1">**</ept> を開きます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="304">
          <source>Add a <ph id="ph1">&amp;lt;</ph>table<ph id="ph2">&amp;gt;</ph> element that has a <bpt id="p1">**</bpt>name<ept id="p1">**</ept> attribute.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>名前<ept id="p1">**</ept>属性を持つ<ph id="ph1">&amp;lt;</ph>テーブル<ph id="ph2">&amp;gt;</ph>要素を追加します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="305">
          <source>The value of the <bpt id="p1">**</bpt>name<ept id="p1">**</ept> attribute is the name of the table that contains the columns to exclude.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>name<ept id="p1">**</ept> 属性の値は、除外する列を含むテーブルの名前です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="306">
          <source>Add an <ph id="ph1">&amp;lt;</ph>exclude<ph id="ph2">&amp;gt;</ph> element in the <ph id="ph3">&amp;lt;</ph>table<ph id="ph4">&amp;gt;</ph> element.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><ph id="ph3">&amp;lt;</ph>テーブル<ph id="ph4">&amp;gt;</ph>要素の<ph id="ph1">&amp;lt;</ph>除外<ph id="ph2">&amp;gt;</ph>要素を追加します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="307">
          <source>For each column that you want to exclude from the export for this table, add a <ph id="ph1">&amp;lt;</ph>field<ph id="ph2">&amp;gt;</ph> element.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このテーブルでエクスポートから除外する各列に対して、<ph id="ph1">&amp;lt;</ph>フィールド<ph id="ph2">&amp;gt;</ph> 要素を追加します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="308">
          <source>The content of the <ph id="ph1">&amp;lt;</ph>field<ph id="ph2">&amp;gt;</ph> element is the name of the column to exclude.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><ph id="ph1">&amp;lt;</ph>フィールド<ph id="ph2">&amp;gt;</ph> 要素のコンテンツは、除外する列の名前です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="309">
          <source>There can be only one <ph id="ph1">&amp;lt;</ph>exclude<ph id="ph2">&amp;gt;</ph> element per table.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">テーブルごとに指定できる <ph id="ph1">&amp;lt;</ph>exclude<ph id="ph2">&amp;gt;</ph> 要素は 1 つだけです。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="310">
          <source>Example of excluding columns from the export</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">エクスポートから列を除外する例</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="311">
          <source>To exclude the <bpt id="p1">**</bpt>BackingEntityTableId<ept id="p1">**</ept>, <bpt id="p2">**</bpt>BackingEntityKeyFieldId<ept id="p2">**</ept>, and <bpt id="p3">**</bpt>BackingEntityValueFieldId<ept id="p3">**</ept> columns when you export the <bpt id="p4">**</bpt>DimensionAttribute<ept id="p4">**</ept> table, include an entry such as this in Filters.xml.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p4">**</bpt>DimensionAttribute<ept id="p4">**</ept> テーブルをエクスポートするときに、<bpt id="p1">**</bpt>BackingEntityTableId<ept id="p1">**</ept>、<bpt id="p2">**</bpt>BackingEntityKeyFieldId<ept id="p2">**</ept>、<bpt id="p3">**</bpt>BackingEntityValueFieldId<ept id="p3">**</ept> 列を除外するには、次のようなエントリを Filters.xml に含めます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="312">
          <source><bpt id="p1">&lt;exclude&gt;</bpt> <bpt id="p2">&lt;field&gt;</bpt>BackingEntityTableId<ept id="p2">&lt;/field&gt;</ept> <bpt id="p3">&lt;field&gt;</bpt>BackingEntityKeyFieldId<ept id="p3">&lt;/field&gt;</ept> <bpt id="p4">&lt;field&gt;</bpt>BackingEntityValueFieldId<ept id="p4">&lt;/field&gt;</ept> <ept id="p1">&lt;/exclude&gt;</ept><ph id="ph1">
</ph><ph id="ph2">      </ph></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">&lt;exclude&gt;</bpt> <bpt id="p2">&lt;field&gt;</bpt>BackingEntityTableId<ept id="p2">&lt;/field&gt;</ept> <bpt id="p3">&lt;field&gt;</bpt>BackingEntityKeyFieldId<ept id="p3">&lt;/field&gt;</ept> <bpt id="p4">&lt;field&gt;</bpt>BackingEntityValueFieldId<ept id="p4">&lt;/field&gt;</ept> <ept id="p1">&lt;/exclude&gt;</ept><ph id="ph1">
</ph><ph id="ph2">      </ph></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="313">
          <source>Exclude rows from the export</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">エクスポートから行を除外</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="314">
          <source>To exclude rows from the exported data, follow these steps.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">エクスポートされたデータから行を除外するには、次の手順を実行します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="315">
          <source>Open <ph id="ph1">\[</ph>Lists<ph id="ph2">\]</ph>Filters.xml.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><ph id="ph1">\[</ph>Lists<ph id="ph2">\]</ph>Filters.xml を開きます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="316">
          <source>Add a <ph id="ph1">&amp;lt;</ph>table<ph id="ph2">&amp;gt;</ph> element that has a <bpt id="p1">**</bpt>name<ept id="p1">**</ept> attribute.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>名前<ept id="p1">**</ept>属性を持つ<ph id="ph1">&amp;lt;</ph>テーブル<ph id="ph2">&amp;gt;</ph>要素を追加します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="317">
          <source>The value of the <bpt id="p1">**</bpt>name<ept id="p1">**</ept> attribute is the name of the table that contains the columns to exclude.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>name<ept id="p1">**</ept> 属性の値は、除外する列を含むテーブルの名前です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="318">
          <source>Add a <ph id="ph1">&amp;lt;</ph>filter<ph id="ph2">&amp;gt;</ph> element in the <ph id="ph3">&amp;lt;</ph>table<ph id="ph4">&amp;gt;</ph> element.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><ph id="ph3">&amp;lt;</ph>テーブル<ph id="ph4">&amp;gt;</ph>要素の<ph id="ph1">&amp;lt;</ph>フィルター<ph id="ph2">&amp;gt;</ph>要素を追加します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="319">
          <source>The content of the <ph id="ph1">&amp;lt;</ph>filter<ph id="ph2">&amp;gt;</ph> element should be an SQL statement that describes the rows to export.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><ph id="ph1">&amp;lt;</ph>フィルター<ph id="ph2">&amp;gt;</ph> 要素のコンテンツは、エクスポートする行を記述する SQL ステートメントである必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="320">
          <source>The <ph id="ph1">&amp;lt;</ph>filter<ph id="ph2">&amp;gt;</ph> element is like an SQL WHERE clause, but each column name should be wrapped in a <ph id="ph3">&amp;lt;</ph>field<ph id="ph4">&amp;gt;</ph> element.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><ph id="ph1">&amp;lt;</ph>filter<ph id="ph2">&amp;gt;</ph> 要素は SQL WHERE 句と似ていますが、各列名は <ph id="ph3">&amp;lt;</ph>field<ph id="ph4">&amp;gt;</ph> ステートメントで囲む必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="321">
          <source>There can be only one <ph id="ph1">&amp;lt;</ph>filter<ph id="ph2">&amp;gt;</ph> element per table.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">テーブルごとに指定できる <ph id="ph1">&amp;lt;</ph>filter<ph id="ph2">&amp;gt;</ph> 要素は 1 つだけです。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="322">
          <source>You can filter based on multiple columns in the table.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">テーブル内の複数の列に基づきフィルター処理することができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="323">
          <source>You cannot filter based on data in other tables.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">他のテーブルのデータに基づいてフィルター処理することはできません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="324">
          <source>Users often want to exclude all rows from the export.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ユーザーは、エクスポートからすべての行を削除することが必要な場合がよくあります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="325">
          <source>You can easily exclude all rows by using a filter that always evaluates to false.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">常に false に評価されるフィルターを使用することにより、すべての行を簡単に除外することができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="326">
          <source>In the standard filters that we supply, a filter of 0 = 1 is the idiom for tables that we want to export as empty.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">供給している標準フィルターで、0 = 1 のフィルターは空でエクスポートするテーブルの慣用句です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="327">
          <source>However, when this technique is used, the Test Data Transfer Tool (beta) still creates files for the table during export, even if the .out file does not contain any data.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">しかし、この技術を使用すると、テスト データ転送ツール (ベータ) では、.out ファイルにデータが含まれていない場合でも、エクスポート時にテーブルの表が作成されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="328">
          <source>This behavior is unlike the behavior when you exclude the whole table by using an entry in an exclude file.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この動作は、除外ファイルのエントリを使用してテーブル全体を除外した場合の動作とは異なります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="329">
          <source>Examples of excluding rows from the export</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">エクスポートから行を除外する例</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="330">
          <source>To export only those rows in <bpt id="p1">**</bpt>SysLastValue<ept id="p1">**</ept> where the <bpt id="p2">**</bpt>UserID<ept id="p2">**</ept> is blank, include the following entry in Filters.xml.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p2">**</bpt>UserID<ept id="p2">**</ept> が空白の <bpt id="p1">**</bpt>SysLastValue<ept id="p1">**</ept> の行のみをエクスポートするには、Filters.xml に次のエントリを含めます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="331">
          <source><bpt id="p1">&lt;filter&gt;</bpt><bpt id="p2">&lt;field&gt;</bpt>UserID<ept id="p2">&lt;/field&gt;</ept> = ''<ept id="p1">&lt;/filter&gt;</ept><ph id="ph1">
</ph><ph id="ph2">      </ph></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">&lt;filter&gt;</bpt><bpt id="p2">&lt;field&gt;</bpt>UserID<ept id="p2">&lt;/field&gt;</ept> = ''<ept id="p1">&lt;/filter&gt;</ept><ph id="ph1">
</ph><ph id="ph2">      </ph></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="332">
          <source>In this case, you can imagine that the SQL query that defines the rows to export is SELECT <ph id="ph1">\*</ph> FROM SysLastValue WHERE UserID = ''.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この場合、エクスポートするために行を定義する SQL クエリは SELECT <ph id="ph1">\*</ph> FROM SysLastValue WHERE UserID = '' であることが想像できます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="333">
          <source>To prevent all rows in SysPersonalization from being exported, include the following entry in Filters.xml.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">SysPersonalization のすべての行がエクスポートされないようにするには、Filters.xml に次のエントリを含めます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="334">
          <source><bpt id="p1">&lt;filter&gt;</bpt>0 = 1<ept id="p1">&lt;/filter&gt;</ept><ph id="ph1">
</ph><ph id="ph2">      </ph></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">&lt;filter&gt;</bpt>0 = 1<ept id="p1">&lt;/filter&gt;</ept><ph id="ph1">
</ph><ph id="ph2">      </ph></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="335">
          <source>In this case, you can imagine that the SQL query that defines the rows to export is SELECT <ph id="ph1">\*</ph> FROM SysPersonalization WHERE 0 = 1.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この場合、エクスポートするために行を定義する SQL クエリは SELECT <ph id="ph1">\*</ph> FROM SysPersonalization WHERE 0 = 1 であることが想像できます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="336">
          <source>Importing data</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">データのインポート</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="337">
          <source>The Test Data Transfer Tool (beta) is designed to try to import all the data in the directory that you specify.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">テスト データ転送ツール (ベータ) は、指定したディレクトリ内のすべてのデータのインポートを試みるように設計されています。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="338">
          <source>The tool does not perform any filtering during import.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このツールはインポート中にフィルタリングを実行しません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="339">
          <source>The only exception to this rule is the <bpt id="p1">**</bpt>SystemSequences<ept id="p1">**</ept> table.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このルールの唯一の例外は、<bpt id="p1">**</bpt>SystemSequences<ept id="p1">**</ept> テーブルです。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="340">
          <source>The tool exports the <bpt id="p1">**</bpt>SystemSequences<ept id="p1">**</ept> table just like any other table.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このツールは他のテーブルと同様に <bpt id="p1">**</bpt>SystemSequences<ept id="p1">**</ept> テーブルをエクスポートします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="341">
          <source>However, during import, the tool ignores any data that you supply for this table.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ただし、インポート中に、このテーブル用に供給する任意のデータはツールにより無視されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="342">
          <source>Instead, the tool updates the <bpt id="p1">**</bpt>SystemSequences<ept id="p1">**</ept> table in the database for each table that is imported if the next <bpt id="p2">**</bpt>RecID<ept id="p2">**</ept> value for that table in the <bpt id="p3">**</bpt>SystemSequences<ept id="p3">**</ept> table is less than the maximum <bpt id="p4">**</bpt>RecID<ept id="p4">**</ept> in the table that is being imported.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">代わりに、<bpt id="p3">**</bpt>SystemSequences<ept id="p3">**</ept> テーブルの次の <bpt id="p2">**</bpt>RecID<ept id="p2">**</ept> の値が、インポートされているテーブルの最大 <bpt id="p4">**</bpt>RecID<ept id="p4">**</ept> よりも低い場合、ツールはインポートされる各テーブルについてデータベースで <bpt id="p1">**</bpt>SystemSequences<ept id="p1">**</ept> テーブルを更新します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="343">
          <source>As each table is imported, the tool also makes any adjustments that are required to the other ID values that are stored in the <bpt id="p1">**</bpt>SystemSequences<ept id="p1">**</ept> table.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">各テーブルがインポートされると、ツールは <bpt id="p1">**</bpt>SystemSequences<ept id="p1">**</ept> テーブルに格納されている他の ID 値に必要な調整も行います。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="344">
          <source>You can import a table that has no rows in the .out file.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">.out ファイルで行を持たないテーブルをインポートすることができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="345">
          <source>You can also not import a table at all.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">テーブルをまったくインポートしないこともできます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="346">
          <source>These two operations are not the same.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">これら 2 つの工程は同じではありません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="347">
          <source>When you import a table that has no rows, the existing data in that table is deleted.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">行を持たないテーブルをインポートするとき、そのテーブル内の既存のデータは削除されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="348">
          <source>However, if you do not import a table at all, the existing data in that table is untouched.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ただし、テーブルを全くインポートしない場合、そのテーブルの既存のデータは変更されません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="349">
          <source>For each table that must be imported, the tool performs the following actions:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">インポートする必要があるテーブルごとに、ツールは以下のアクションを実行します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="350">
          <source>The tool searches for a table in the target database that has the same origin GUID.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ツールは、同じ起点 GUID を持つターゲット データベース内のテーブルを検索します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="351">
          <source>If such a table exists, the tool uses that table as the target of the import.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このようなテーブルが存在する場合、ツールは、インポートの対象としてそのテーブルを使用します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="352">
          <source>If no such table exists, the tool tries to find a table in the target database that has the same name.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">そのようなテーブルが存在しない場合、ツールは、同じ名前であるターゲット データベース内のテーブルを検索しようとします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="353">
          <source>If such a table exists, the tool uses that table as the target of the import.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このようなテーブルが存在する場合、ツールは、インポートの対象としてそのテーブルを使用します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="354">
          <source>If no target table can be found, the table is not imported, and no error is produced.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">対象となるテーブルが見つからない場合は、テーブルはインポートされず、エラーは生成されません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="355">
          <source>When a target table has been identified, the tool creates a new temporary version of the .out file that matches the columns in the target table.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ターゲット テーブルが特定されると、ターゲット テーブル内の列に一致する .out ファイルの新しい一時的なバージョンがツールによって作成されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="356">
          <source>For each column in the source table, the tool first searches for the matching column in the target table by using the origin GUID of the field.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ソース テーブル内の各列で、ツールは最初に、フィールドの GUID の発生元を使用して、ターゲット テーブルで対応する列を検索します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="357">
          <source>If no origin-based match is found, columns are matched by using the field names.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">発生元に基づく一致が見つからない場合は、フィールド名を使用して列が一致します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="358">
          <source>If there are columns in the source table that do not have matching columns in the target table, the data for those columns is ignored, and no error is produced.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ターゲット テーブル内で一致した列がないソース テーブル内に列がある場合は、それらの列のデータは無視され、エラーは生成されません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="359">
          <source>If there are columns in the target table that do not have matching columns in the source table, default values are used.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ソース テーブル内に一致した列がないターゲット テーブル内に列がある場合は、既定値が使用されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="360">
          <source>In most cases, the default values are 0 (zero) or empty values that match the data type of the target column.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ほとんどの場合、既定値は 0 (ゼロ) またはターゲット列のデータ型と一致する空の列です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="361">
          <source>However, if the target column is named <bpt id="p1">**</bpt>InstanceRelationType<ept id="p1">**</ept>, the default value is the table ID of the target table.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ただし、ターゲット列が <bpt id="p1">**</bpt>InstanceRelationType<ept id="p1">**</ept> と名付けられる場合、既定値はターゲット テーブルのテーブル ID です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="362">
          <source>For any column that is known to refer to a Microsoft Dynamics AX entity by the entity’s table ID, class ID, or extended data type ID, the tool updates the ID to match the ID of the same entity in the target database.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">エンティティのテーブル ID、クラス ID、または拡張データ型 ID により Microsoft Dynamics AX のエンティティを参照することで知られる任意の列に関しては、ツールはターゲット データベースで同じエンティティの ID と一致する ID を更新します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="363">
          <source>The tool first maps the ID in the source data to the origin of the entity at the time of export.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このツールは、まず、エクスポート時にソースデータの ID をエンティティの起点にマッピングします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="364">
          <source>The tool then uses the origin of the entity to obtain the ID in the target database.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ツールは、エンティティの原点を使用して、ターゲット データベース内の ID を取得します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="365">
          <source>If the entity cannot be found in the target system, the original ID is used, and no error is produced.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ターゲット システムで、事業体が見つからない場合に元の ID を使用すると、エラーは生成されません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="366">
          <source>During import, if data is not imported because of an index violation in a non-clustered index, the tool tries to disable the index and then retries the import.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">インポート中に、クラスター化されていないインデックスのインデックス違反のためにデータがインポートされなかった場合、ツールはインデックスを無効にしてからインポートを再試行します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="367">
          <source>In this case, an error is reported in the log file, even if the data is successfully imported after the index was disabled.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この場合、インデックスを無効にされた後にデータが正常にインポートされた場合でも、ログ ファイルにエラーが報告されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="368">
          <source>Import example</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">インポートの例</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="369">
          <source>The following example shows how to import all files in the <bpt id="p1">**</bpt>Import<ph id="ph1">\_</ph>March2013<ept id="p1">**</ept> directory.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">次の例は、<bpt id="p1">**</bpt>Import<ph id="ph1">\_</ph>March2013<ept id="p1">**</ept> ディレクトリにあるすべてのファイルをインポートする方法を示しています。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="370">
          <source>DP.exe IMPORT Import_March2013 AXTestDB</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">DP.exe インポート Import_March2013 AXTestDB</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="371">
          <source>Files used during import</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">インポート中に使用されるファイル</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="372">
          <source>This section describes the files that are used by the Test Data Transfer Tool (beta) during the import process.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このセクションでは、インポート処理中にテスト データ転送ツール (ベータ版) で使用されるファイルについて説明します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="373">
          <source>Temporary files</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">一時ファイル</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="374">
          <source>The Test Data Transfer Tool (beta) can import data into tables that have many kinds of changes, such as columns that have been added, removed, or renamed.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">テスト データ転送ツール (beta) は、追加、削除、または名前変更が実行された列などの多くの種類の変更を含むテーブルにデータをインポートできます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="375">
          <source>To enable this functionality, the tool writes a modified version of the .out file to a temporary location on disk and passes this file to bcp to import.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この機能を有効にするには、修正されたバージョンの .out ファイルをディスクの一時的な場所に書き込み、このファイルを bcp に渡してインポートします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="376">
          <source>Then, when the import is completed, the tool deletes the temporary file.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">インポートが完了すると、ツールは一時ファイルを削除します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="377">
          <source>The name of the temporary file is generated by calling <bpt id="p1">**</bpt>Path.GetTempPath()<ept id="p1">**</ept> and <bpt id="p2">**</bpt>Path.GetRandomFileName()<ept id="p2">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">一時ファイルの名前は、<bpt id="p1">**</bpt>Path.GetTempPath()<ept id="p1">**</ept> および <bpt id="p2">**</bpt>Path.GetRandomFileName()<ept id="p2">**</ept> を呼び出すことによって生成されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="378">
          <source>Typically, the temporary files are deleted even when run-time errors occur.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">通常、一時ファイルは実行時エラーが発生しても削除されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="379">
          <source>However, in rare situations, such as when a power outage occurs during import, the temporary files can be written and not deleted.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ただし、インポート中に停電が発生する場合などのまれな状況では、一時ファイルに書き込まれ、削除はされません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="380">
          <source>Because the files are written to the current user’s temporary path, this issue should not cause unexpected information disclosure.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ファイルが現在のユーザーの一時的なパスに書き込まれるため、この問題により予期せぬ情報開示が発生しないようにする必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="381">
          <source>However, depending on the importance of the information that you are importing and on your organization’s data handling policies, you might have to know about this risk.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ただし、インポートする情報の重要度によって、および組織のデータ処理のポリシーによっては、このリスクについて理解しておく必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="382">
          <source>.sql files</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">.sql ファイル</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="383">
          <source>The Test Data Transfer Tool (beta) lets you execute arbitrary SQL statements in your user context by adding .sql files to the <ph id="ph1">\[</ph>Import<ph id="ph2">\]</ph> folder.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">テスト データ転送ツール (ベータ) では、.sql ファイルを <ph id="ph1">\[</ph>インポート<ph id="ph2">\]</ph> フォルダに追加すると、ユーザーのコンテキストで任意の SQL ステートメントを実行できます。。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="384">
          <source>Add only .sql files that come from a trusted source.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">信頼済のソースから .sql ファイルだけを追加します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="385">
          <source>.out files, .outmodel files, and .xml files</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">.out ファイル、.outmodel ファイル、および .xml ファイル</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="386">
          <source>The Test Data Transfer Tool (beta) generates SQL statements from the names of the .out files and from the content of the other files in the directory that contains the data to import.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">テスト データ転送ツール (ベータ) は、.out ファイルの名前から、およびインポートするデータを含むディレクトリ内のその他のファイルの内容から SQL ステートメントを生成します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="387">
          <source>The content that is pulled from those files and used to generate SQL statements is expected to represent table names.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">これらのファイルから取得され、SQL ステートメントを生成するために使用されるコンテンツは、テーブル名を表す必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="388">
          <source>To prevent SQL injection attacks, the tool validates and escapes the data before that data is used to create the SQL queries.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">SQL インジェクション攻撃を防ぐため、ツールは SQL クエリを作成する前にデータの検証とエスケープを行います。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="389">
          <source>However, we still recommend that you accept data only from trusted sources.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ただし、信頼できるソースからのみデータを受け入れることを引き続きお勧めします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="390">
          <source>Run SQL scripts after import</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">インポート後に SQL スクリプトを実行</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="391">
          <source>The Test Data Transfer Tool (beta) lets you run SQL scripts after you complete the import.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">テスト データ転送ツール (ベータ) では、インポートを完了した後に SQL スクリプトを実行できます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="392">
          <source>Any modifications that you have to make to imported data can be completed by using the SQL scripts.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">インポートされたデータに対して行う変更は、SQL スクリプトを使用することによって完了できます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="393">
          <source>Before you complete your data import, write the SQL script, and then save the file as an .sql file in the <ph id="ph1">\[</ph>Import<ph id="ph2">\]</ph> subfolder in the same location as the tool.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">データのインポートを完了する前に、SQL スクリプトを作成し、ツールと同じ場所にある<ph id="ph1">\[</ph>インポート<ph id="ph2">\]</ph> サブフォルダーに .sql ファイルとして保存します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="394">
          <source>When the import is completed, the tool automatically runs the SQL script file that you have stored in the <ph id="ph1">\[</ph>Import<ph id="ph2">\]</ph> folder.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">インポートが完了したら、ツールは、<ph id="ph1">\[</ph>インポート<ph id="ph2">\]</ph> フォルダに保存されている SQL スクリプト ファイルを自動的に実行します。</target></trans-unit>
      </group>
    </body>
  </file>
</xliff>