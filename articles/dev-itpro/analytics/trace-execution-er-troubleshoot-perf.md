<?xml version="1.0" encoding="UTF-8"?>
<xliff xmlns:logoport="urn:logoport:xliffeditor:xliff-extras:1.0" xmlns:tilt="urn:logoport:xliffeditor:tilt-non-translatables:1.0" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns="urn:oasis:names:tc:xliff:document:1.2" xmlns:xliffext="urn:microsoft:content:schema:xliffextensions" version="1.2" xsi:schemaLocation="urn:oasis:names:tc:xliff:document:1.2 xliff-core-1.2-transitional.xsd">
  <file datatype="xml" source-language="en-US" original="trace-execution-er-troubleshoot-perf.md" target-language="ja-JP">
    <header>
      <tool tool-company="Microsoft" tool-version="1.0-7889195" tool-name="mdxliff" tool-id="mdxliff"/>
      <xliffext:skl_file_name>trace-execution-er-troubleshoot-perf.773b92.aa71db2752889bc905c22bab1cf2fa46d7ee07c7.skl</xliffext:skl_file_name>
      <xliffext:version>1.2</xliffext:version>
      <xliffext:ms.openlocfilehash>aa71db2752889bc905c22bab1cf2fa46d7ee07c7</xliffext:ms.openlocfilehash>
      <xliffext:ms.sourcegitcommit>67d00b95952faf0db580d341249d4e50be59119c</xliffext:ms.sourcegitcommit>
      <xliffext:ms.lasthandoff>05/15/2019</xliffext:ms.lasthandoff>
      <xliffext:ms.openlocfilepath>articles\dev-itpro\analytics\trace-execution-er-troubleshoot-perf.md</xliffext:ms.openlocfilepath>
    </header>
    <body>
      <group extype="content" id="content">
        <trans-unit xml:space="preserve" translate="yes" id="101" restype="x-metadata">
          <source>Trace execution of ER format to troubleshoot performance issues</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">パフォーマンス上の問題をトラブルシューティングするため ER 形式の追跡実行</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="102" restype="x-metadata">
          <source>This topic provides information about how to use the performance trace feature in Electronic reporting (ER) to troubleshoot performance issues.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">このトピックでは、パフォーマンス上の問題をトラブルシューティングするために電子申告 (ER) のパフォーマンス追跡機能を使用する方法について説明します。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="103">
          <source>Trace the execution of ER formats to troubleshoot performance issues</source><target logoport:matchpercent="90" state="translated" state-qualifier="fuzzy-match">パフォーマンス上の問題をトラブルシューティングするため ER 形式の実行を追跡します</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="104">
          <source>As part of the process of designing Electronic reporting (ER) configurations to generate electronic documents, you define the method that is used to get data out of Microsoft Dynamics 365 for Finance and Operations and enter it in the output that is generated.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">電子ドキュメントを生成するために電子申告 (ER) コンフィギュレーションをデザインするプロセスの一部として、Microsoft Dynamics 365 for Finance and Operations からデータを取得し、生成される出力に入力したりするのに使用される方法を定義します。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="105">
          <source>The ER performance trace feature helps significantly reduce the time and cost that are involved in collecting the details of ER format execution and using them to troubleshoot performance issues.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">ER パフォーマンス追跡機能を使用すると、ER 形式の実行に関する詳細の収集や、それらを使用してパフォーマンスの問題をトラブルシューティングするのにかかる時間と費用を大幅に削減できます。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="106">
          <source>This tutorial provides guidelines about how to take performance traces for executed ER formats in Finance and Operations, and how to use the information from these traces to help improve performance.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">このチュートリアルでは、Finance and Operations で実行される ER 形式のパフォーマン追跡を実行する方法、およびこれらの追跡情報を使用してパフォーマンスを向上する方法についてのガイドラインを示します。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="107">
          <source>Prerequisites</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">必要条件</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="108">
          <source>To complete the examples in this tutorial, you must have the following access:</source><target logoport:matchpercent="91" state="translated" state-qualifier="fuzzy-match">このチュートリアルの例を完了するには、次のアクセスが必要です:</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="109">
          <source>Access to Finance and Operations for one of the following roles:</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">次のロールのいずれか 1 つのために Finance and Operations にアクセスします:</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="110">
          <source>Electronic reporting developer</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">電子申告開発者</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="111">
          <source>Electronic reporting functional consultant</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">電子申告機能コンサルタント</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="112">
          <source>System administrator</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">システム管理者</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="113">
          <source>Access to the instance of Regulatory Configuration Services (RCS) that has been provisioned for the same tenant as Finance and Operations, for one of the following roles:</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">次のいずれかの役割で、Finance and Operations と同じテナントに対してプロビジョニングされている Regulatory Configuration Services (RCS) のインスタンスにアクセスします。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="114">
          <source>Electronic reporting developer</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">電子申告開発者</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="115">
          <source>Electronic reporting functional consultant</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-inherited">電子申告機能コンサルタント</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="116">
          <source>System administrator</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">システム管理者</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="117">
          <source>You must also download and locally store the following files.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">次のファイルをローカルにダウンロードして保存する必要もあります。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="118">
          <source>File</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">ファイル</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="119">
          <source>Content</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">コンテンツ</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="120">
          <source>Performance trace model.version.1</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">model.version.1 のパフォーマンス追跡</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="121">
          <source><bpt id="p1">[</bpt>Sample ER data model configuration<ept id="p1">](https://mbs.microsoft.com/customersource/Global/AX/downloads/hot-fixes/365optelecrepeg)</ept></source><target logoport:matchpercent="82" state="translated" state-qualifier="fuzzy-match"><bpt id="p1">[</bpt>ER データ モデル構成のサンプル<ept id="p1">](https://mbs.microsoft.com/customersource/Global/AX/downloads/hot-fixes/365optelecrepeg)</ept></target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="122">
          <source>Performance trace metadata.version.1</source><target logoport:matchpercent="82" state="translated" state-qualifier="fuzzy-match">metadata.version.1 のパフォーマンス追跡</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="123">
          <source><bpt id="p1">[</bpt>Sample ER metadata configuration<ept id="p1">](https://mbs.microsoft.com/customersource/Global/AX/downloads/hot-fixes/365optelecrepeg)</ept></source><target logoport:matchpercent="76" state="translated" state-qualifier="fuzzy-match"><bpt id="p1">[</bpt>ER メタデータ構成のサンプル<ept id="p1">](https://mbs.microsoft.com/customersource/Global/AX/downloads/hot-fixes/365optelecrepeg)</ept></target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="124">
          <source>Performance trace mapping.version.1.1</source><target logoport:matchpercent="75" state="translated" state-qualifier="fuzzy-match">mapping.version.1.1 のパフォーマンス追跡</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="125">
          <source><bpt id="p1">[</bpt>Sample ER model mapping configuration<ept id="p1">](https://mbs.microsoft.com/customersource/Global/AX/downloads/hot-fixes/365optelecrepeg)</ept></source><target logoport:matchpercent="82" state="translated" state-qualifier="fuzzy-match"><bpt id="p1">[</bpt>ER モデル マッピング構成のサンプル<ept id="p1">](https://mbs.microsoft.com/customersource/Global/AX/downloads/hot-fixes/365optelecrepeg)</ept></target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="126">
          <source>Performance trace format.version.1.1</source><target logoport:matchpercent="85" state="translated" state-qualifier="fuzzy-match">format.version.1.1 のパフォーマンス追跡</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="127">
          <source><bpt id="p1">[</bpt>Sample ER format configuration<ept id="p1">](https://mbs.microsoft.com/customersource/Global/AX/downloads/hot-fixes/365optelecrepeg)</ept></source><target logoport:matchpercent="79" state="translated" state-qualifier="fuzzy-match"><bpt id="p1">[</bpt>ER フォーマット構成のサンプル<ept id="p1">](https://mbs.microsoft.com/customersource/Global/AX/downloads/hot-fixes/365optelecrepeg)</ept></target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="128">
          <source>Configure ER parameters</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">ER パラメーターのコンフィギュレーション</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="129">
          <source>Each ER performance trace that is generated in Finance and Operations is stored as an attachment of the execution log record.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Finance and Operations で生成された各 ER パフォーマンス追跡は、実行ログ レコードの添付ファイルとして保管されます。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="130">
          <source>The Document management (DM) framework of Finance and Operations is used to manage these attachments.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Finance and Operations のドキュメント管理 (DM) フレームワークを使用してこれらの添付ファイルを管理します。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="131">
          <source>You must configure ER parameters in advance, to specify the DM document type that should be used to attach performance traces.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">ER パラメーターを事前にコンフィギュレーションして、パフォーマンス追跡を添付するのに使用する DM ドキュメント タイプを指定する必要があります。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="132">
          <source>In Finance and Operation, in the <bpt id="p1">**</bpt>Electronic reporting<ept id="p1">**</ept> workspace, select <bpt id="p2">**</bpt>Electronic reporting parameters<ept id="p2">**</ept>.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Finance and Operation の、<bpt id="p1">**</bpt>電子申告<ept id="p1">**</ept>ワークスペースで、<bpt id="p2">**</bpt>電子申告パラメーター<ept id="p2">**</ept>を選択します。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="133">
          <source>Then, on the <bpt id="p1">**</bpt>Electronic reporting parameters<ept id="p1">**</ept> page, on the <bpt id="p2">**</bpt>Attachments<ept id="p2">**</ept> tab, in the <bpt id="p3">**</bpt>Others<ept id="p3">**</ept> field, select the DM document type to use for performance traces.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">次に、<bpt id="p1">**</bpt>電子申告パラメーター<ept id="p1">**</ept> ページの<bpt id="p2">**</bpt>添付ファイル<ept id="p2">**</ept> タブの<bpt id="p3">**</bpt>その他<ept id="p3">**</ept>フィールドで、パフォーマンス追跡に使用する DM ドキュメント タイプを選択します。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="134">
          <source>Electronic reporting parameters page in Finance and Operations</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Finance and Operations の電子申告パラメーター ページ</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="135">
          <source>To be available in the <bpt id="p1">**</bpt>Others<ept id="p1">**</ept> lookup field, a DM document type must be configured in the following manner on the <bpt id="p2">**</bpt>Document types<ept id="p2">**</ept> page (<bpt id="p3">**</bpt>Organization administration <ph id="ph1">\&gt;</ph> Document management <ph id="ph2">\&gt;</ph> Document types<ept id="p3">**</ept>):</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt"><bpt id="p1">**</bpt>その他<ept id="p1">**</ept>ルックアップ フィールドで使用可能にするには、DM ドキュメント タイプを<bpt id="p2">**</bpt>ドキュメント タイプ<ept id="p2">**</ept> ページ (<bpt id="p3">**</bpt>組織管理 <ph id="ph1">\&gt;</ph> ドキュメント管理 <ph id="ph2">\&gt;</ph> ドキュメント タイプ<ept id="p3">**</ept>): で次のようにコンフィギュレーションする必要があります。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="136">
          <source><bpt id="p1">**</bpt>Class:<ept id="p1">**</ept> Attach file</source><target logoport:matchpercent="0" state="translated"><bpt id="p1">**</bpt>クラス:<ept id="p1">**</ept> 添付ファイル</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="137">
          <source><bpt id="p1">**</bpt>Group:<ept id="p1">**</ept> File</source><target logoport:matchpercent="94" state="translated" state-qualifier="fuzzy-match"><bpt id="p1">**</bpt>グループ:<ept id="p1">**</ept> ファイル</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="138">
          <source>Document types page in Finance and Operations</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Finance and Operations のドキュメント タイプ ページ</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="139">
          <source>The selected document type must be available in every company of the current Finance and Operations instance, because DM attachments are company-specific.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">DM 添付ファイルは会社固有であるため、選択したドキュメント タイプは、現在の Finance and Operations インスタンスのすべての会社で使用可能である必要があります。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="140">
          <source>Configure RCS parameters</source><target logoport:matchpercent="98" state="translated" state-qualifier="fuzzy-match">RCS パラメーターのコンフィギュレーション</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="141">
          <source>ER performance traces that are generated in Finance and Operations will be imported into RCS for analysis by using the ER format designer and the ER mapping designer.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Finance and Operations で生成される ER パフォーマンス追跡は、ER 形式デザイナーと ER マッピング デザイナーを使用して、分析用に RCS にインポートされます。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="142">
          <source>Because ER performance traces are stored as attachments of the execution log record that is related to the ER format, you must configure RCS parameters in advance, to specify the DM document type that should be used to attach performance traces.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">ER パフォーマンス追跡は ER 形式に関連する実行ログ レコードの添付ファイルとして格納されるため、RCS パラメーターを事前にコンフィギュレーションして、パフォーマンス追跡の添付に使用する DM ドキュメント タイプを指定する必要があります。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="143">
          <source>In the instance of RCS that has been provisioned for your company, in the <bpt id="p1">**</bpt>Electronic reporting<ept id="p1">**</ept> workspace, select <bpt id="p2">**</bpt>Electronic reporting parameters<ept id="p2">**</ept>.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">会社用にプロビジョニングされた RCS のインスタンスの、<bpt id="p1">**</bpt>電子申告<ept id="p1">**</ept>ワークスペースで、<bpt id="p2">**</bpt>電子申告パラメーター<ept id="p2">**</ept>を選択します。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="144">
          <source>Then, on the <bpt id="p1">**</bpt>Electronic reporting parameters<ept id="p1">**</ept> page, on the <bpt id="p2">**</bpt>Attachments<ept id="p2">**</ept> tab, in the <bpt id="p3">**</bpt>Others<ept id="p3">**</ept> field, select the DM document type to use for performance traces.</source>
        <target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-inherited">次に、<bpt id="p1">**</bpt>電子申告パラメーター<ept id="p1">**</ept> ページの<bpt id="p2">**</bpt>添付ファイル<ept id="p2">**</ept> タブの<bpt id="p3">**</bpt>その他<ept id="p3">**</ept>フィールドで、パフォーマンス追跡に使用する DM ドキュメント タイプを選択します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="145">
          <source>Electronic reporting parameters page in RCS</source><target logoport:matchpercent="90" state="translated" state-qualifier="fuzzy-match">RCS の電子申告パラメーター ページ</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="146">
          <source>To be available in the <bpt id="p1">**</bpt>Others<ept id="p1">**</ept> lookup field, a DM document type must be configured in the following manner on the <bpt id="p2">**</bpt>Document types<ept id="p2">**</ept> page (<bpt id="p3">**</bpt>Organization administration <ph id="ph1">\&gt;</ph> Document management <ph id="ph2">\&gt;</ph> Document types<ept id="p3">**</ept>):</source>
        <target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-inherited"><bpt id="p1">**</bpt>その他<ept id="p1">**</ept>ルックアップ フィールドで使用可能にするには、DM ドキュメント タイプを<bpt id="p2">**</bpt>ドキュメント タイプ<ept id="p2">**</ept> ページ (<bpt id="p3">**</bpt>組織管理 <ph id="ph1">\&gt;</ph> ドキュメント管理 <ph id="ph2">\&gt;</ph> ドキュメント タイプ<ept id="p3">**</ept>): で次のようにコンフィギュレーションする必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="147">
          <source><bpt id="p1">**</bpt>Class:<ept id="p1">**</ept> Attach file</source><target logoport:matchpercent="100" state="translated" state-qualifier="exact-match"><bpt id="p1">**</bpt>クラス:<ept id="p1">**</ept> 添付ファイル</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="148">
          <source><bpt id="p1">**</bpt>Group:<ept id="p1">**</ept> File</source><target logoport:matchpercent="100" state="translated" state-qualifier="exact-match"><bpt id="p1">**</bpt>グループ:<ept id="p1">**</ept> ファイル</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="149">
          <source>Design an ER solution</source><target logoport:matchpercent="68" state="translated" state-qualifier="fuzzy-match">ER ソリューションのデザイン</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="150">
          <source>Assume that you've started to design a new ER solution to generate a new report that presents vendor transactions.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">仕入先トランザクションを表示する新しいレポートを生成するため、新しい ER ソリューションのデザインを開始したとします。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="151">
          <source>Currently, you can find the transactions for a selected vendor on the <bpt id="p1">**</bpt>Vendor transactions<ept id="p1">**</ept> page (go to <bpt id="p2">**</bpt>Account payable <ph id="ph1">\&gt;</ph> Vendors <ph id="ph2">\&gt;</ph> All vendors<ept id="p2">**</ept>, select a vendor, and then, on the Action Pane, on the <bpt id="p3">**</bpt>Vendor<ept id="p3">**</ept> tab, in the <bpt id="p4">**</bpt>Transactions<ept id="p4">**</ept> group, select <bpt id="p5">**</bpt>Transactions<ept id="p5">**</ept>).</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">現時点では、選択した仕入先のトランザクションは<bpt id="p1">**</bpt>仕入先トランザクション<ept id="p1">**</ept> ページ (<bpt id="p2">**</bpt>買掛金勘定 <ph id="ph1">\&gt;</ph> 仕入先 <ph id="ph2">\&gt;</ph> すべての仕入先<ept id="p2">**</ept>に移動し、仕入先を選択してから、アクション ウィンドウの<bpt id="p3">**</bpt>仕入先<ept id="p3">**</ept>タブの<bpt id="p4">**</bpt>トランザクション<ept id="p4">**</ept> グループで、<bpt id="p5">**</bpt>トランザクション<ept id="p5">**</ept>を選択します) で検索できます。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="152">
          <source>However, you want to have all vendor transaction at the same time in one electronic document in XML format.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">ただし、XML 形式の 1 つの電子ドキュメントで、すべての仕入先トランザクションを同時に処理する必要があります。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="153">
          <source>This solution will consist of several ER configurations that contain the required data model, metadata, model mapping, and format components.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">このソリューションは、必要なデータ モデル、メタデータ、モデル マッピング、および形式コンポーネントを含むいくつかの ER コンフィギュレーションで構成されます。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="154">
          <source>Sign in to the instance of RCS that has been provisioned for your company.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">会社用にプロビジョニングされた RCS のインスタンスにサインインします。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="155">
          <source>In this tutorial, you will create and modify configurations for the <bpt id="p1">**</bpt>Litware, Inc.<ept id="p1">**</ept> sample company.</source><target logoport:matchpercent="0" state="translated">このチュートリアルでは、サンプル会社 <bpt id="p1">**</bpt>Litware, Inc.<ept id="p1">**</ept> のコンフィギュレーションを作成または変更します。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="156">
          <source>Therefore, make sure that this configuration provider has been added to RCS and selected as active.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">そのため、このコンフィギュレーション プロバイダーが RCS に追加され、有効として選択されていることを確認してください。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="157">
          <source>For instructions, see the <bpt id="p1">[</bpt>Create configuration providers and mark them as active<ept id="p1">](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/analytics/tasks/er-configuration-provider-mark-it-active-2016-11)</ept> procedure.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">手順については、<bpt id="p1">[</bpt>コンフィギュレーション プロバイダーを作成し、有効としてマークする<ept id="p1">](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/analytics/tasks/er-configuration-provider-mark-it-active-2016-11)</ept> を参照してください。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="158">
          <source>In the <bpt id="p1">**</bpt>Electronic reporting<ept id="p1">**</ept> workspace, select the <bpt id="p2">**</bpt>Reporting configurations<ept id="p2">**</ept> tile.</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>電子レポート<ept id="p1">**</ept>ワークスペースで、<bpt id="p2">**</bpt>レポート コンフィギュレーション<ept id="p2">**</ept>タイルを選択します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="159">
          <source>On the <bpt id="p1">**</bpt>Configurations<ept id="p1">**</ept> page, import the ER configurations that you downloaded as a prerequisite into RCS, in the following order: data model, metadata, model mapping, format.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt"><bpt id="p1">**</bpt>構成<ept id="p1">**</ept>ページで、前提条件としてダウンロードした ER コンフィギュレーションを RCS に次の順序でインポートします: データ モデル、メタデータ、モデル マッピング、フォーマット。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="160">
          <source>For each configuration, follow these steps:</source><target logoport:matchpercent="85" state="translated" state-qualifier="fuzzy-match">各コンフィギュレーションについて、次の手順を実行します。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="161">
          <source>On the Action Pane, select <bpt id="p1">**</bpt>Exchange <ph id="ph1">\&gt;</ph> Load from XML file<ept id="p1">**</ept>.</source><target logoport:matchpercent="0" state="translated">アクション ウィンドウで、<bpt id="p1">**</bpt>交換 <ph id="ph1">\&gt;</ph> XML ファイルからロード<ept id="p1">**</ept>を選択します。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="162">
          <source>Select <bpt id="p1">**</bpt>Browse<ept id="p1">**</ept> to select the appropriate file for the required ER configuration in XML format.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt"><bpt id="p1">**</bpt>参照<ept id="p1">**</ept>を選択して、必要な ER コンフィギュレーションに適したファイルを XML 形式で選択します。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="163">
          <source>Select <bpt id="p1">**</bpt>OK<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>OK<ept id="p1">**</ept> を選択します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="164">
          <source>Configurations page in RCS</source><target logoport:matchpercent="84" state="translated" state-qualifier="fuzzy-match">RCS の構成ページ</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="165">
          <source>Run the ER solution to trace execution</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">ER ソリューションを実行して追跡実行する</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="166">
          <source>Assume that you've finished designing the first version of the ER solution.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">ER ソリューションの最初のバージョンのデザインが完了したとします。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="167">
          <source>You now want to test it in your Finance and Operations instance and analyze execution performance.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">これにより、Finance and Operations インスタンスでテストを行い、実行パフォーマンスを分析できます。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="168">
          <source><bpt id="p1">&lt;a id='import-configuration'&gt;</bpt><ept id="p1">&lt;/a&gt;</ept>Import an ER configuration from RCS into Finance and Operations</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt"><bpt id="p1">&lt;a id='import-configuration'&gt;</bpt><ept id="p1">&lt;/a&gt;</ept>ER コンフィギュレーションを RCS から Finance and Operations にインポートする</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="169">
          <source>Sign in to your Finance and Operations instance.</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">Finance and Operations インスタンスへログインします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="170">
          <source>For this tutorial, you will import configurations from your RCS instance (where you design your ER components) into your Finance and Operations instance (where you test and finally use them).</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">このチュートリアルでは、RCS インスタンス (ER コンポーネントを設計する場所) から、Finance and Operations インスタンス (テストして最後に使用する場所) にコンフィギュレーションをインポートします。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="171">
          <source>Therefore, you must make sure that all the required artifacts have been prepared.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">したがって、必要なコンポーネントがすべて準備されたことを確認する必要があります。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="172">
          <source>For instructions, see the <bpt id="p1">[</bpt>Import Electronic reporting (ER) configurations from Regulatory Configuration Services (RCS)<ept id="p1">](https://docs.microsoft.com/en-us/dynamics365/unified-operations/dev-itpro/analytics/rcs-download-configurations)</ept> procedure.</source><target logoport:matchpercent="83" state="translated" state-qualifier="fuzzy-match">手順については、<bpt id="p1">[</bpt>規制コンフィギュレーション サービス (RCS) からの電子申告 (ER) 構成のインポート<ept id="p1">](https://docs.microsoft.com/en-us/dynamics365/unified-operations/dev-itpro/analytics/rcs-download-configurations)</ept> を参照してください。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="173">
          <source>Follow these steps to import the configurations from RCS into Finance and Operations:</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">これらの手順に従って、コンフィギュレーションを RCS から Finance and Operations にインポートします。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="174">
          <source>In the <bpt id="p1">**</bpt>Electronic reporting<ept id="p1">**</ept> workspace, on the tile for the <bpt id="p2">**</bpt>Litware, Inc.<ept id="p2">**</ept> configuration provider, select <bpt id="p3">**</bpt>Repositories<ept id="p3">**</ept>.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt"><bpt id="p1">**</bpt>電子申告<ept id="p1">**</ept>ワークスペースの、<bpt id="p2">**</bpt>Litware, inc.<ept id="p2">**</ept> コンフィギュレーション プロバイダーのタイルで、<bpt id="p3">**</bpt>リポジトリ<ept id="p3">**</ept>を選択します。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="175">
          <source>On the <bpt id="p1">**</bpt>Configuration repository<ept id="p1">**</ept> page, select the repository of the <bpt id="p2">**</bpt>RCS<ept id="p2">**</ept> type, and then select <bpt id="p3">**</bpt>Open<ept id="p3">**</ept>.</source><target logoport:matchpercent="0" state="translated"><bpt id="p1">**</bpt>コンフィギュレーション リポジトリ<ept id="p1">**</ept> ページで、<bpt id="p2">**</bpt>RCS<ept id="p2">**</ept> タイプのリポジトリを選択し、<bpt id="p3">**</bpt>開く<ept id="p3">**</ept>を選択します。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="176">
          <source>On the <bpt id="p1">**</bpt>Configurations<ept id="p1">**</ept> FastTab, select the <bpt id="p2">**</bpt>Performance trace format<ept id="p2">**</ept> configuration.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt"><bpt id="p1">**</bpt>コンフィギュレーション<ept id="p1">**</ept> クイック タブで、<bpt id="p2">**</bpt>パフォーマンス追跡形式<ept id="p2">**</ept>コンフィギュレーションを選択します。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="177">
          <source>On the <bpt id="p1">**</bpt>Versions<ept id="p1">**</ept> FastTab, select version <bpt id="p2">**</bpt>1.1<ept id="p2">**</ept> of the selected configuration, and then select <bpt id="p3">**</bpt>Import<ept id="p3">**</ept>.</source><target logoport:matchpercent="0" state="translated"><bpt id="p1">**</bpt>バージョン<ept id="p1">**</ept> クイック タブで、選択したコンフィギュレーションのバージョン <bpt id="p2">**</bpt>1.1<ept id="p2">**</ept> を選択し、<bpt id="p3">**</bpt>インポート<ept id="p3">**</ept>を選択します。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="178">
          <source>Configuration repository page in Finance and Operations</source><target logoport:matchpercent="68" state="translated" state-qualifier="fuzzy-match">Finance and Operations のコンフィギュレーション レポジトリ ページ</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="179">
          <source>The corresponding versions of the data model and model mapping configurations are automatically imported as prerequisites for the imported ER format configuration.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">データ モデルとモデル マッピングコン フィギュレーションの対応するバージョンは、インポートされた ER 形式コンフィギュレーションの前提条件として自動的にインポートされます。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="180">
          <source>Turn on the ER performance trace</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">ER パフォーマンス追跡を有効にする</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="181">
          <source>In Finance and Operations, go to <bpt id="p1">**</bpt>Organization administration <ph id="ph1">\&gt;</ph> Electronic reporting <ph id="ph2">\&gt;</ph> Configurations<ept id="p1">**</ept>.</source><target logoport:matchpercent="0" state="translated">Finance and Operations で、<bpt id="p1">**</bpt>組織管理 <ph id="ph1">\&gt;</ph> 電子申告 <ph id="ph2">\&gt;</ph> 構成<ept id="p1">**</ept>の順に移動します。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="182">
          <source>On the <bpt id="p1">**</bpt>Configurations<ept id="p1">**</ept> page, on the Action Pane, on the <bpt id="p2">**</bpt>Configurations<ept id="p2">**</ept> tab, in the <bpt id="p3">**</bpt>Advanced settings<ept id="p3">**</ept> group, select <bpt id="p4">**</bpt>User parameters<ept id="p4">**</ept>.</source><target logoport:matchpercent="72" state="translated" state-qualifier="fuzzy-match"><bpt id="p1">**</bpt>構成<ept id="p1">**</ept>ページ、アクション ウィンドウ、<bpt id="p2">**</bpt>構成<ept id="p2">**</ept>タブ、<bpt id="p3">**</bpt>詳細設定<ept id="p3">**</ept>グループで、<bpt id="p4">**</bpt>ユーザー パラメーター<ept id="p4">**</ept>を選択します。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="183">
          <source>In the <bpt id="p1">**</bpt>User parameters<ept id="p1">**</ept> dialog box, in the <bpt id="p2">**</bpt>Execution tracing<ept id="p2">**</ept> section, follow these steps:</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt"><bpt id="p1">**</bpt>ユーザー パラメーター<ept id="p1">**</ept> ダイアログ ボックスの<bpt id="p2">**</bpt>実行トレース<ept id="p2">**</ept> セクションで、次の手順を実行します。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="184">
          <source>In the <bpt id="p1">**</bpt>Execution trace format<ept id="p1">**</ept> field, select <bpt id="p2">**</bpt>Debug trace format<ept id="p2">**</ept> to start to collect the details of ER format execution.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt"><bpt id="p1">**</bpt>実行トレース形式<ept id="p1">**</ept>フィールドで、<bpt id="p2">**</bpt>デバッグ トレース形式<ept id="p2">**</ept>を選択して、ER 形式実行の詳細の収集を開始します。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="185">
          <source>When this value is selected, the performance trace will collect information about the time that is spent on the following actions:</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">この値が選択されている場合、パフォーマンス追跡によって、次のアクションに費やされた時間に関する情報が収集されます。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="186">
          <source>Running each data source in the model mapping that is called to get data</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">データを取得するために呼び出されるモデル マッピングで各データ ソースを実行する</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="187">
          <source>Processing each format item to enter data in the output that is generated</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">生成される出力にデータを入力するため各項目の形式を処理する</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="188">
          <source>You use the <bpt id="p1">**</bpt>Execution trace format<ept id="p1">**</ept> field to specify the format of the generated performance trace that the execution details are stored in for ER format and mapping elements.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt"><bpt id="p1">**</bpt>実行トレース形式<ept id="p1">**</ept>フィールドを使用して、実行詳細が ER 形式およびマッピング要素で格納される生成済パフォーマンス追跡の形式を指定します。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="189">
          <source>By selecting <bpt id="p1">**</bpt>Debug trace format<ept id="p1">**</ept> as the value, you will be able to analyze the content of the trace in ER Operation designer, and see the ER format or mapping elements that are mentioned in the trace.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt"><bpt id="p1">**</bpt>デバッグ トレース形式<ept id="p1">**</ept>を値として選択することにより、ER 操作デザイナーでトレースの内容を分析して、トレースに記載されている ER 形式またはマッピング要素を確認できます。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="190">
          <source>Set the following options to <bpt id="p1">**</bpt>Yes<ept id="p1">**</ept> to collect specific details of the execution of the ER model mapping and ER format components:</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">次のオプションを<bpt id="p1">**</bpt>はい<ept id="p1">**</ept>に設定して、ER モデル マッピングおよび ER フォーマット コンポーネントの実行に関する具体的な詳細を収集します。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="191">
          <source><bpt id="p1">**</bpt>Collect query statistics<ept id="p1">**</ept> – When this option is turned on, the performance trace will collect the following information:</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt"><bpt id="p1">**</bpt>クエリ統計情報の収集<ept id="p1">**</ept> – このオプションが有効になっている場合、パフォーマンス追跡では次の情報が収集されます。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="192">
          <source>The number of database calls that were made by data sources</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">データ ソースによって作成されたデータベース呼び出し数</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="193">
          <source>The number of duplicate calls to the database</source><target logoport:matchpercent="86" state="translated" state-qualifier="fuzzy-match">データベースに対する複製呼び出し数</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="194">
          <source>Details of the SQL statements that were used to make database calls</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">データベース呼び出しを行うために使用された SQL ステートメントの詳細</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="195">
          <source><bpt id="p1">**</bpt>Trace access of caching<ept id="p1">**</ept> – When this option is turned on, the performance trace will collect information about the ER model mapping's cache usage.</source><target logoport:matchpercent="0" state="translated"><bpt id="p1">**</bpt>キャッシュのアクセスの追跡<ept id="p1">**</ept> – このオプションが有効になっている場合、パフォーマンス追跡では ER モデル マッピングのキャッシュ使用に関する情報が収集されます。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="196">
          <source><bpt id="p1">**</bpt>Trace data access<ept id="p1">**</ept> – When this option is turned on, the performance trace will collect information about the number of calls to the database for executed data sources of the record list type.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt"><bpt id="p1">**</bpt>データ アクセスの追跡<ept id="p1">**</ept> – このオプションが有効になっている場合、パフォーマンス追跡では、レコード リスト タイプの実行されたデータ ソースに対するデータベースへの呼び出し回数に関する情報が収集されます。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="197">
          <source><bpt id="p1">**</bpt>Trace list enumeration<ept id="p1">**</ept> – When this option is turned on, the performance trace will collect information about the number of records that are requested from data sources of the record list type.</source><target logoport:matchpercent="79" state="translated" state-qualifier="fuzzy-match"><bpt id="p1">**</bpt>リスト列挙の追跡<ept id="p1">**</ept> – このオプションが有効になっている場合、パフォーマンス追跡では、レコード リスト タイプのデータ ソースから要求されたレコード数に関する情報が収集されます。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="198">
          <source>The parameters in the <bpt id="p1">**</bpt>User parameters<ept id="p1">**</ept> dialog box are specific to the user and the current company.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt"><bpt id="p1">**</bpt>ユーザー パラメーター<ept id="p1">**</ept> ダイアログ ボックスのパラメーターは、ユーザーと現在の会社に固有です。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="199">
          <source>User parameters dialog box in Finance and Operations</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Finance and Operations のユーザー パラメーター ダイアログ ボックス</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="200">
          <source><bpt id="p1">&lt;a id='run-format'&gt;</bpt><ept id="p1">&lt;/a&gt;</ept>Run the ER format</source><target logoport:matchpercent="77" state="translated" state-qualifier="fuzzy-match"><bpt id="p1">&lt;a id='run-format'&gt;</bpt><ept id="p1">&lt;/a&gt;</ept>ER 形式を実行する</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="201">
          <source>In Finance and Operations, select the <bpt id="p1">**</bpt>DEMF<ept id="p1">**</ept> company.</source><target logoport:matchpercent="73" state="translated" state-qualifier="fuzzy-match">Finance and Operations で、<bpt id="p1">**</bpt>DEMF<ept id="p1">**</ept> 会社を選択します。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="202">
          <source>Go to <bpt id="p1">**</bpt>Organization administration <ph id="ph1">\&gt;</ph> Electronic reporting <ph id="ph2">\&gt;</ph> Configurations<ept id="p1">**</ept>.</source><target logoport:matchpercent="0" state="translated"><bpt id="p1">**</bpt>組織管理 <ph id="ph1">\&gt;</ph> 電子申告 <ph id="ph2">\&gt;</ph> コンフィギュレーション<ept id="p1">**</ept>の順に移動します。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="203">
          <source>On the <bpt id="p1">**</bpt>Configurations<ept id="p1">**</ept> page, in the configuration tree, select the <bpt id="p2">**</bpt>Performance trace format<ept id="p2">**</ept> item.</source><target logoport:matchpercent="77" state="translated" state-qualifier="fuzzy-match"><bpt id="p1">**</bpt>コンフィギュレーション<ept id="p1">**</ept> ページのコンフィギュレーション ツリーで、<bpt id="p2">**</bpt>パフォーマンス追跡形式<ept id="p2">**</ept>項目を選択します。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="204">
          <source>On the Action Pane, select <bpt id="p1">**</bpt>Run<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">アクション ウィンドウで、<bpt id="p1">**</bpt>実行<ept id="p1">**</ept>を選択します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="205">
          <source>Notice that the file that is generated presents information about 265 transactions for six vendors.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">生成されるファイルによって、6 つの仕入先の 265 トランザクションに関する情報が表示されることに注意してください。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="206">
          <source>Review the execution trace</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">実行追跡の確認</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="207">
          <source><bpt id="p1">&lt;a id='export-trace'&gt;</bpt><ept id="p1">&lt;/a&gt;</ept>Export the generated trace from Finance and Operations</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt"><bpt id="p1">&lt;a id='export-trace'&gt;</bpt><ept id="p1">&lt;/a&gt;</ept> 生成された追跡を Finance and Operations からエクスポートします。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="208">
          <source>Performance traces are decoupled from the source ER format and can be serialized to an external zip file.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">パフォーマンス追跡は、ソースの ER 形式から切り離され、外部の zip ファイルにシリアル化されます。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="209">
          <source>In Finance and Operations, go to <bpt id="p1">**</bpt>Organization administration <ph id="ph1">\&gt;</ph> Electronic reporting <ph id="ph2">\&gt;</ph> Configuration debug logs<ept id="p1">**</ept>.</source><target logoport:matchpercent="88" state="translated" state-qualifier="fuzzy-match">Finance and Operations で、<bpt id="p1">**</bpt>組織管理 <ph id="ph1">\&gt;</ph> 電子申告 <ph id="ph2">\&gt;</ph> 構成デバッグ ログ<ept id="p1">**</ept>の順に移動します。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="210">
          <source>On the <bpt id="p1">**</bpt>Electronic reporting run logs<ept id="p1">**</ept> page, in the left pane, in the <bpt id="p2">**</bpt>Configuration name<ept id="p2">**</ept> field, select <bpt id="p3">**</bpt>Performance trace format<ept id="p3">**</ept> to find the log records that have been generated by the execution of the <bpt id="p4">**</bpt>Performance trace format<ept id="p4">**</ept> configuration.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt"><bpt id="p1">**</bpt>電子申告実行ログ<ept id="p1">**</ept>ページ、左ウィンドウの、<bpt id="p2">**</bpt>コンフィギュレーション名<ept id="p2">**</ept>フィールドで、<bpt id="p3">**</bpt>パフォーマンス追跡形式<ept id="p3">**</ept>を選択し、<bpt id="p4">**</bpt>パフォーマンス追跡形式<ept id="p4">**</ept>コンフィギュレーションの実行によって生成されたログ レコードを検索します。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="211">
          <source>Select the <bpt id="p1">**</bpt>Attachments<ept id="p1">**</ept> button (the paper clip symbol) in the upper-right corner of the page, or press <bpt id="p2">**</bpt>Ctrl+Shift+A<ept id="p2">**</ept>.</source><target logoport:matchpercent="0" state="translated">ページの右上隅にある<bpt id="p1">**</bpt>添付ファイル<ept id="p1">**</ept>ボタン (紙クリップ記号) を選択するか、<bpt id="p2">**</bpt>Ctrl + Shift + A<ept id="p2">**</ept> を押します。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="212">
          <source>Attachments button on the Electronic reporting run logs page in Finance and Operations</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Finance and Operations の電子申告実行ログ ページの添付ファイル ボタン</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="213">
          <source>On the <bpt id="p1">**</bpt>Attachments for Electronic reporting run logs<ept id="p1">**</ept> page, on the Action Pane, select <bpt id="p2">**</bpt>Open<ept id="p2">**</ept> to get the performance trace as a zip file and store it locally.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt"><bpt id="p1">**</bpt>電子申告実行ログの添付ファイル<ept id="p1">**</ept> ページの、アクション ウィンドウで、<bpt id="p2">**</bpt>開く<ept id="p2">**</ept>を選択してパフォーマンス追跡を zip ファイルとして取得し、ローカルに保管します。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="214">
          <source>Attachments for Electronic reporting run logs page in Finance and Operations</source><target logoport:matchpercent="85" state="translated" state-qualifier="fuzzy-match">Finance and Operations の電子申告実行ログ ページの添付ファイル</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="215">
          <source>The trace that is generated has a reference to the source ER report via a unique report identifier in <bpt id="p1">**</bpt>GUID<ept id="p1">**</ept> format only.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">生成されるトレースは、<bpt id="p1">**</bpt>GUID<ept id="p1">**</ept> 形式のみの固有のレポート ID を通じて、ソース ER レポートを参照しています。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="216">
          <source>The version numbering of the format isn't considered.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">形式のバージョン番号付けは考慮されません。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="217">
          <source>Notice that the association between the performance trace that has been generated for the executed ER format and the ER model mapping is based on the root descriptor that was used and the common data model.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">実行される ER 形式と ER モデル マッピングに対して生成されたパフォーマンス追跡間の関連付けは、使用されたルート記述子と共通データ モデルに基づいていることに注意してください。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="218">
          <source>The version numbering of the format and model mapping isn't considered.</source><target logoport:matchpercent="77" state="translated" state-qualifier="fuzzy-match">形式のバージョン番号付けおよびモデル マッピングは考慮されません。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="219">
          <source>The setting of the <bpt id="p1">**</bpt>Default for model mapping<ept id="p1">**</ept> flag for the model mapping also isn't considered.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">モデル マッピングに対する<bpt id="p1">**</bpt>モデル マッピングの既定値<ept id="p1">**</ept>フラグの設定も考慮されません。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="220">
          <source><bpt id="p1">&lt;a id='import-trace'&gt;</bpt><ept id="p1">&lt;/a&gt;</ept>Import the generated trace into RCS</source><target logoport:matchpercent="80" state="translated" state-qualifier="fuzzy-match"><bpt id="p1">&lt;a id='import-trace'&gt;</bpt><ept id="p1">&lt;/a&gt;</ept> 生成された追跡を RCS にインポートします</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="221">
          <source>In RCS, in the <bpt id="p1">**</bpt>Electronic reporting<ept id="p1">**</ept> workspace, select the <bpt id="p2">**</bpt>Reporting configurations<ept id="p2">**</ept> tile.</source><target logoport:matchpercent="94" state="translated" state-qualifier="fuzzy-match">RCS の、<bpt id="p1">**</bpt>電子レポート<ept id="p1">**</ept> ワークスペースで、<bpt id="p2">**</bpt>レポート コンフィギュレーション<ept id="p2">**</ept> タイルを選択します。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="222">
          <source>On the <bpt id="p1">**</bpt>Configurations<ept id="p1">**</ept> page, in the configuration tree, expand the <bpt id="p2">**</bpt>Performance trace model<ept id="p2">**</ept> item, and select the <bpt id="p3">**</bpt>Performance trace format<ept id="p3">**</ept> item.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt"><bpt id="p1">**</bpt>構成<ept id="p1">**</ept>ページのコンフィギュレーション ツリーで、<bpt id="p2">**</bpt>パフォーマンス追跡モデル<ept id="p2">**</ept>項目を展開し、<bpt id="p3">**</bpt>パフォーマンス追跡形式<ept id="p3">**</ept>項目を選択します。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="223">
          <source>On the Action Pane, select <bpt id="p1">**</bpt>Designer<ept id="p1">**</ept>.</source><target logoport:matchpercent="85" state="translated" state-qualifier="fuzzy-match">アクション ウィンドウで、<bpt id="p1">**</bpt>デザイナー<ept id="p1">**</ept>を選択します。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="224">
          <source>On the <bpt id="p1">**</bpt>Format designer<ept id="p1">**</ept> page, on the Action Pane, select <bpt id="p2">**</bpt>Performance trace<ept id="p2">**</ept>.</source><target logoport:matchpercent="72" state="translated" state-qualifier="fuzzy-match"><bpt id="p1">**</bpt>形式デザイナー<ept id="p1">**</ept>の、アクション ウィンドウで、<bpt id="p2">**</bpt>パフォーマンス追跡<ept id="p2">**</ept>を選択します。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="225">
          <source>In the <bpt id="p1">**</bpt>Performance trace result settings<ept id="p1">**</ept> dialog box, select <bpt id="p2">**</bpt>Import performance trace<ept id="p2">**</ept>.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt"><bpt id="p1">**</bpt>パフォーマンス追跡結果の設定<ept id="p1">**</ept>ダイアログ ボックスで、<bpt id="p2">**</bpt>パフォーマンス追跡のインポート<ept id="p2">**</ept>を選択します。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="226">
          <source>Select <bpt id="p1">**</bpt>Browse<ept id="p1">**</ept> to select the zip file that you exported from Finance and Operations earlier.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt"><bpt id="p1">**</bpt>参照<ept id="p1">**</ept>を選択して、事前に Finance and Operations からエクスポートした zip ファイルを選択します。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="227">
          <source>Select <bpt id="p1">**</bpt>OK<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>OK<ept id="p1">**</ept> を選択します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="228">
          <source>Performance trace result settings dialog box in RCS</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">RCS のパフォーマンス追跡結果の設定ダイアログ ボックス</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="229">
          <source>Use the performance trace for analysis in RCS – Format execution</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">RCS での分析に対するパフォーマンス追跡の使用 – 形式実行</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="230">
          <source>In RCS, on the <bpt id="p1">**</bpt>Format designer<ept id="p1">**</ept> page, select <bpt id="p2">**</bpt>Expand/collapse<ept id="p2">**</ept> to expand the content of all format items.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">RCS の、<bpt id="p1">**</bpt>形式デザイナー<ept id="p1">**</ept> ページで、<bpt id="p2">**</bpt>展開/折りたたみ<ept id="p2">**</ept>を選択してすべての形式項目の内容を展開します。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="231">
          <source>Notice that additional information is shown for some items of the current format:</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">現在の形式の一部の項目に関して、追加情報が表示されることに注意してください。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="232">
          <source>The actual time that was spent entering data in the generated output by using the format item</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">形式項目を使用して生成された出力にデータを入力するのに費やした実際の時間</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="233">
          <source>The same time expressed as a percentage of the total time that was spent generating the whole output</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">出力全体の生成に費やされた合計時間の割合で表される同じ時間</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="234">
          <source>Format designer page in RCS</source><target logoport:matchpercent="84" state="translated" state-qualifier="fuzzy-match">RCS の形式デザイナー ページ</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="235">
          <source>Close <bpt id="p1">**</bpt>Format designer<ept id="p1">**</ept> page.</source><target logoport:matchpercent="0" state="translated"><bpt id="p1">**</bpt>形式デザイナー<ept id="p1">**</ept> ページを閉じます。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="236">
          <source><bpt id="p1">&lt;a id='use-trace'&gt;</bpt><ept id="p1">&lt;/a&gt;</ept>Use the performance trace for analysis in RCS – Model mapping</source><target logoport:matchpercent="79" state="translated" state-qualifier="fuzzy-match"><bpt id="p1">&lt;a id='use-trace'&gt;</bpt><ept id="p1">&lt;/a&gt;</ept>RCS での分析に対するパフォーマンス追跡の使用 – モデル マッピング</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="237">
          <source>In RCS, on the <bpt id="p1">**</bpt>Configurations<ept id="p1">**</ept> page, in the configuration tree, select the <bpt id="p2">**</bpt>Performance trace mapping<ept id="p2">**</ept> item.</source><target logoport:matchpercent="85" state="translated" state-qualifier="fuzzy-match">RCS、<bpt id="p1">**</bpt>コンフィギュレーション<ept id="p1">**</ept> ページのコンフィギュレーション ツリーで、<bpt id="p2">**</bpt>パフォーマンス追跡マッピング<ept id="p2">**</ept>項目を選択します。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="238">
          <source>On the Action Pane, select <bpt id="p1">**</bpt>Designer<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="85" state="translated" state-qualifier="leveraged-inherited">アクション ウィンドウで、<bpt id="p1">**</bpt>デザイナー<ept id="p1">**</ept>を選択します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="239">
          <source>Select <bpt id="p1">**</bpt>Designer<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>デザイナー<ept id="p1">**</ept> をクリックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="240">
          <source>On the <bpt id="p1">**</bpt>Model mapping designer<ept id="p1">**</ept> page, on the Action Pane, select <bpt id="p2">**</bpt>Performance trace<ept id="p2">**</ept>.</source><target logoport:matchpercent="0" state="translated"><bpt id="p1">**</bpt>モデル マッピング デザイナー<ept id="p1">**</ept> ページの、アクション ウィンドウで、<bpt id="p2">**</bpt>パフォーマンス追跡<ept id="p2">**</ept>を選択します。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="241">
          <source>Select the trace that you imported earlier.</source><target logoport:matchpercent="0" state="translated">事前にインポートした追跡を選択します。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="242">
          <source>Select <bpt id="p1">**</bpt>OK<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>OK<ept id="p1">**</ept> を選択します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="243">
          <source>Notice that new information becomes available for some data source items of the current model mapping:</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">現在のモデル マッピングの一部のデータ ソース項目に関する、新しい情報が利用可能になることに注意してください。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="244">
          <source>The actual time that was spent getting data by using the data source</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">データ ソースを使用してデータの取得に費やした実際の時間</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="245">
          <source>The same time expressed as a percentage of the total time that was spent running the whole model mapping</source><target logoport:matchpercent="86" state="translated" state-qualifier="fuzzy-match">モデル マッピング全体の実行に費やされた合計時間の割合で表される同じ時間</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="246">
          <source>Notice that ER informs you that the current model mapping duplicates database requests while the VendTable/<ph id="ph1">\&lt;</ph>Relations/VendTrans.VendTable<ph id="ph2">\_</ph>AccountNum data source is run.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">VendTable/<ph id="ph1">\&lt;</ph>Relations/VendTrans.VendTable<ph id="ph2">\_</ph>AccountNum データ ソースの実行中は、現在のモデル マッピングがデータベース要求を重複することを ER から通知されることに注意してください。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="247">
          <source>This duplication occurs because the list of vendor transactions is called two times for each iterated vendor record:</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">この重複が発生するのは、仕入先トランザクションの一覧が、反復する仕入先レコードごとに 2 回呼び出されるためです。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="248">
          <source>One call is made to enter details of each transaction in the data model, based on configured bindings.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">1 回の呼び出しでは、構成されたバインディングに基づいて、データ モデルの各トランザクションの詳細を入力します。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="249">
          <source>One call is made to enter the calculated number of transactions per vendor in the data model.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">もう 1 回の呼び出しで、データ モデルの仕入先ごとに計算されたトランザクション数を入力します。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="250">
          <source>Message about duplicate database requests on the Model mapping designer page in RCS</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">RCS のモデル マッピング デザイナー ページで重複したデータベース要求に関するメッセージ</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="251">
          <source>The value <bpt id="p1">**</bpt><ph id="ph1">\[</ph>Q:530<ph id="ph2">\]</ph><ept id="p1">**</ept> indicates that the VendTrans table was called 530 times to return a record from that table to the VendTable/<ph id="ph3">\&lt;</ph>Relations/VendTrans.VendTable<ph id="ph4">\_</ph>AccountNum data source.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt"><bpt id="p1">**</bpt><ph id="ph1">\[</ph>Q:530<ph id="ph2">\]</ph><ept id="p1">**</ept> の値は、テーブルから VendTable/<ph id="ph3">\&lt;</ph>Relations/VendTrans.VendTable<ph id="ph4">\_</ph>AccountNum データ ソースにレコードを返すため、VendTrans テーブルが 530 回呼び出されたことを示します。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="252">
          <source>The value <bpt id="p1">**</bpt><ph id="ph1">\[</ph>530<ph id="ph2">\]</ph><ept id="p1">**</ept> indicates that the VendTable/<ph id="ph3">\&lt;</ph>Relations/VendTrans.VendTable<ph id="ph4">\_</ph>AccountNum data source was called 530 times to return a record from that data source and enter the details from it in the data model.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt"><bpt id="p1">**</bpt><ph id="ph1">\[</ph>530<ph id="ph2">\]</ph><ept id="p1">**</ept> の値は、VendTable/<ph id="ph3">\&lt;</ph>Relations/VendTrans.VendTable<ph id="ph4">\_</ph>AccountNum データ ソースが、そのデータ ソースからレコードを返し、データ モデルで詳細を入力するために 530 回呼び出されたことを示します。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="253">
          <source>We recommend that you use caching for the VendTable/<ph id="ph1">\&lt;</ph>Relations/VendTrans.VendTable<ph id="ph2">\_</ph>AccountNum data source, to reduce the number of calls that are made to get the details for 265 transactions and help improve the performance of the model mapping.</source><target logoport:matchpercent="0" state="translated">265 トランザクションの詳細を取得するための呼び出し数を減らし、モデルマッピングのパフォーマンスを向上させるため、VendTable/<ph id="ph1">\&lt;</ph>Relations/VendTrans.VendTable<ph id="ph2">\_</ph>AccountNum データ ソースに対してキャッシュを使用することをお勧めします。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="254">
          <source>It can also be useful to reduce the number of calls that are made to the LedgerTransTypeList data source.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">それは LedgerTransTypeList データ ソースに対して行われる呼び出し数を減らすのにも役立ちます。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="255">
          <source>This data source is used to associate each value of the <bpt id="p1">**</bpt>LedgerTransType<ept id="p1">**</ept> enumeration with its label.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">このデータ ソースは、<bpt id="p1">**</bpt>LedgerTransType<ept id="p1">**</ept> 列挙の各値をラベルに関連付けるために使用されます。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="256">
          <source>By using this data source, you can find an appropriate label and enter it in the data model for each vendor transaction.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">このデータ ソースを使用すると、適切なラベルを検索して、各仕入先トランザクションのデータ モデルに入力できます。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="257">
          <source>The current number of calls to this data source (9,027) is quite high for 265 transactions.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">このデータ ソースへの現在の呼び出し数 (9,027) は、265 トランザクションに対して非常に高くなっています。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="258">
          <source>Model mapping designer page in RCS, showing 9,027 calls to the data source</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">データ ソースへの 9,027 の呼び出しを示す、RCS のモデル マッピング デザイナー ページ</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="259">
          <source>Improve the model mapping based on information from the execution trace</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">実行追跡からの情報に基づいてモデル マッピングを改善する</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="260">
          <source>Modify the logic of the model mapping</source><target logoport:matchpercent="77" state="translated" state-qualifier="fuzzy-match">モデル マッピングのロジックを変更する</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="261">
          <source>Follow these steps to use caching, to help prevent duplicate calls to the database:</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">次の手順に従ってキャッシュを使用すると、データベースへの重複呼び出しを防ぐことができます。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="262">
          <source>In RCS, on the <bpt id="p1">**</bpt>Model mapping designer<ept id="p1">**</ept> page, in the <bpt id="p2">**</bpt>Data sources<ept id="p2">**</ept> pane, select the <bpt id="p3">**</bpt>VendTable<ept id="p3">**</ept> item.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">RCS、<bpt id="p1">**</bpt>モデル マッピング デザイナー<ept id="p1">**</ept> ページの、<bpt id="p2">**</bpt>データ ソース<ept id="p2">**</ept> ウィンドウで、<bpt id="p3">**</bpt>VendTable<ept id="p3">**</ept> 項目を選択します。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="263">
          <source>Select <bpt id="p1">**</bpt>Cache<ept id="p1">**</ept>.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt"><bpt id="p1">**</bpt>キャッシュ<ept id="p1">**</ept>を選択します。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="264">
          <source>Expand the <bpt id="p1">**</bpt>VendTable<ept id="p1">**</ept> item, expand the list of one-to-many relations for the VendTable data source (the <bpt id="p2">**</bpt><ph id="ph1">\&lt;</ph>Relations<ept id="p2">**</ept> item), and select the <bpt id="p3">**</bpt>VendTrans.VendTable<ph id="ph2">\_</ph>AccountNum<ept id="p3">**</ept> item.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt"><bpt id="p1">**</bpt>VendTable<ept id="p1">**</ept> 項目を展開し、VendTable データ ソース (<bpt id="p2">**</bpt><ph id="ph1">\&lt;</ph>関係<ept id="p2">**</ept>項目) の一対多の関係の一覧を展開してから、<bpt id="p3">**</bpt>VendTrans.VendTable<ph id="ph2">\_</ph>AccountNum<ept id="p3">**</ept> 項目を選択します。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="265">
          <source>Select <bpt id="p1">**</bpt>Cache<ept id="p1">**</ept>.</source><target logoport:matchpercent="100" state="translated" state-qualifier="exact-match"><bpt id="p1">**</bpt>キャッシュ<ept id="p1">**</ept>を選択します。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="266">
          <source>Caching setup to help prevent duplicate calls</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">重複呼び出しを防ぐためのキャッシュ設定</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="267">
          <source>Follow these steps to bring the LedgerTransTypeList data source into the scope of the VendTable data source:</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">LedgerTransTypeList データ ソースを VendTable データ ソースのスコープに移動するには、次の手順に従います。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="268">
          <source>In the <bpt id="p1">**</bpt>Data source types<ept id="p1">**</ept> pane, expand the <bpt id="p2">**</bpt>Functions<ept id="p2">**</ept> item, and select the <bpt id="p3">**</bpt>Calculated field<ept id="p3">**</ept> item.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt"><bpt id="p1">**</bpt>データ ソース タイプ<ept id="p1">**</ept> ウィンドウで、<bpt id="p2">**</bpt>関数<ept id="p2">**</ept>項目を展開し、<bpt id="p3">**</bpt>計算済フィールド<ept id="p3">**</ept>項目を選択します。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="269">
          <source>In the <bpt id="p1">**</bpt>Data sources<ept id="p1">**</ept> pane, select the <bpt id="p2">**</bpt>VendTable<ept id="p2">**</ept> item.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt"><bpt id="p1">**</bpt>データ ソース<ept id="p1">**</ept> ウィンドウで、<bpt id="p2">**</bpt>VendTable<ept id="p2">**</ept> 項目を選択します。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="270">
          <source>Select <bpt id="p1">**</bpt>Add<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>追加<ept id="p1">**</ept>を選択します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="271">
          <source>In the <bpt id="p1">**</bpt>Name<ept id="p1">**</ept> field, enter <bpt id="p2">**</bpt><ph id="ph1">\$</ph>TransType<ept id="p2">**</ept>.</source><target logoport:matchpercent="0" state="translated"><bpt id="p1">**</bpt>名前<ept id="p1">**</ept>フィールドで、<bpt id="p2">**</bpt><ph id="ph1">\$</ph>TransType<ept id="p2">**</ept> を入力します。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="272">
          <source>Select <bpt id="p1">**</bpt>Edit formula<ept id="p1">**</ept>.</source><target logoport:matchpercent="74" state="translated" state-qualifier="fuzzy-match"><bpt id="p1">**</bpt>式の編集<ept id="p1">**</ept>を選択します。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="273">
          <source>In the <bpt id="p1">**</bpt>Formula<ept id="p1">**</ept> field, enter <bpt id="p2">**</bpt>LedgerTransTypeList<ept id="p2">**</ept>.</source><target logoport:matchpercent="0" state="translated"><bpt id="p1">**</bpt>式<ept id="p1">**</ept>フィールドに、<bpt id="p2">**</bpt>LedgerTransTypeList<ept id="p2">**</ept> を入力します。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="274">
          <source>Select <bpt id="p1">**</bpt>Save<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>保存<ept id="p1">**</ept> を選択します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="275">
          <source>Close the <bpt id="p1">**</bpt>Formula editor<ept id="p1">**</ept> page.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt"><bpt id="p1">**</bpt>式の編集<ept id="p1">**</ept>ページを閉じます。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="276">
          <source>Click <bpt id="p1">**</bpt>OK<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>OK<ept id="p1">**</ept>をクリックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="277">
          <source>Follow these steps to do caching of the <bpt id="p1">**</bpt><ph id="ph1">\$</ph>TransType<ept id="p1">**</ept> field:</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">次の手順に従って、<bpt id="p1">**</bpt><ph id="ph1">\$</ph>TransType<ept id="p1">**</ept> フィールドをキャッシュします。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="278">
          <source>Select the <bpt id="p1">**</bpt>LedgerTransTypeList<ept id="p1">**</ept> item.</source><target logoport:matchpercent="77" state="translated" state-qualifier="fuzzy-match"><bpt id="p1">**</bpt>LedgerTransTypeList<ept id="p1">**</ept> 項目を選択します。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="279">
          <source>Select <bpt id="p1">**</bpt>Cache<ept id="p1">**</ept>.</source><target logoport:matchpercent="100" state="translated" state-qualifier="exact-match"><bpt id="p1">**</bpt>キャッシュ<ept id="p1">**</ept>を選択します。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="280">
          <source>Select the <bpt id="p1">**</bpt>VendTable.<ph id="ph1">\$</ph>TransType<ept id="p1">**</ept> item.</source><target logoport:matchpercent="0" state="translated"><bpt id="p1">**</bpt>VendTable.<ph id="ph1">\$</ph>TransType<ept id="p1">**</ept> 項目を選択します。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="281">
          <source>Select <bpt id="p1">**</bpt>Cache<ept id="p1">**</ept>.</source><target logoport:matchpercent="100" state="translated" state-qualifier="exact-match"><bpt id="p1">**</bpt>キャッシュ<ept id="p1">**</ept>を選択します。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="282">
          <source>Caching setup for the $TransType field</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">$TransType フィールドのキャッシュ設定</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="283">
          <source>Follow these steps to change the <bpt id="p1">**</bpt><ph id="ph1">\$</ph>TransTypeRecord<ept id="p1">**</ept> field so that it starts to use the cached <bpt id="p2">**</bpt><ph id="ph2">\$</ph>TransType<ept id="p2">**</ept> field:</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">次の手順に従って <bpt id="p1">**</bpt><ph id="ph1">\$</ph>TransTypeRecord<ept id="p1">**</ept> フィールドを変更し、キャッシュされた <bpt id="p2">**</bpt><ph id="ph2">\$</ph>TransType<ept id="p2">**</ept> フィールドを使用開始できるようにします。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="284">
          <source>In the <bpt id="p1">**</bpt>Data sources<ept id="p1">**</ept> pane, expand the <bpt id="p2">**</bpt>VendTable<ept id="p2">**</ept> item, expand the <bpt id="p3">**</bpt><ph id="ph1">\&lt;</ph>Relations<ept id="p3">**</ept> item, expand the <bpt id="p4">**</bpt>VendTrans.VendTable<ph id="ph2">\_</ph>AccountNum<ept id="p4">**</ept> item, and select the <bpt id="p5">**</bpt>VendTable. VendTrans.VendTable<ph id="ph3">\_</ph>AccountNum.<ph id="ph4">\$</ph>TransTypeRecord<ept id="p5">**</ept> item.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt"><bpt id="p1">**</bpt>データ ソース<ept id="p1">**</ept> ウィンドウで、<bpt id="p2">**</bpt>VendTable<ept id="p2">**</ept> 項目を展開し、<bpt id="p3">**</bpt><ph id="ph1">\&lt;</ph>関係<ept id="p3">**</ept>項目を展開し、<bpt id="p4">**</bpt>VendTrans.VendTable<ph id="ph2">\_</ph>AccountNum<ept id="p4">**</ept> 項目を展開してから、<bpt id="p5">**</bpt>VendTable. VendTrans.VendTable<ph id="ph3">\_</ph>AccountNum.<ph id="ph4">\$</ph>TransTypeRecord<ept id="p5">**</ept> 項目を選択します。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="285">
          <source>Select <bpt id="p1">**</bpt>Edit<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>編集<ept id="p1">**</ept>を選択します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="286">
          <source>Select <bpt id="p1">**</bpt>Edit formula<ept id="p1">**</ept>.</source><target logoport:matchpercent="100" state="translated" state-qualifier="exact-match"><bpt id="p1">**</bpt>式の編集<ept id="p1">**</ept>を選択します。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="287">
          <source>In the <bpt id="p1">**</bpt>Formula<ept id="p1">**</ept> field, find the following expression:</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt"><bpt id="p1">**</bpt>式<ept id="p1">**</ept>フィールドで、次の式を検索します。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="288">
          <source>FIRSTORNULL (WHERE (LedgerTransTypeList, LedgerTransTypeList.Enum = <ph id="ph1">\@</ph>.TransType))</source><target logoport:matchpercent="0" state="translated">FIRSTORNULL (WHERE (LedgerTransTypeList, LedgerTransTypeList.Enum = <ph id="ph1">\@</ph>.TransType))</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="289">
          <source>In the <bpt id="p1">**</bpt>Formula<ept id="p1">**</ept> field, enter the following expression:</source><target logoport:matchpercent="86" state="translated" state-qualifier="fuzzy-match"><bpt id="p1">**</bpt>式<ept id="p1">**</ept>フィールドで、次の式を入力します。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="290">
          <source>FIRSTORNULL (WHERE (VendTable.'<ph id="ph1">\$</ph>TransType', VendTable.'<ph id="ph2">\$</ph>TransType'.Enum = <ph id="ph3">\@</ph>.TransType)).</source><target logoport:matchpercent="0" state="translated">FIRSTORNULL (WHERE (VendTable.'<ph id="ph1">\$</ph>TransType', VendTable.'<ph id="ph2">\$</ph>TransType'.Enum = <ph id="ph3">\@</ph>.TransType)).</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="291">
          <source>Select <bpt id="p1">**</bpt>Save<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>保存<ept id="p1">**</ept> を選択します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="292">
          <source>Close the <bpt id="p1">**</bpt>Formula editor<ept id="p1">**</ept> page.</source>
        <target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-inherited"><bpt id="p1">**</bpt>式の編集<ept id="p1">**</ept>ページを閉じます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="293">
          <source>Select <bpt id="p1">**</bpt>OK<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>OK<ept id="p1">**</ept> を選択します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="294">
          <source>Select <bpt id="p1">**</bpt>Save<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>保存<ept id="p1">**</ept> を選択します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="295">
          <source>Close the <bpt id="p1">**</bpt>Model mapping designer<ept id="p1">**</ept> page.</source><target logoport:matchpercent="0" state="translated"><bpt id="p1">**</bpt>モデル マッピング デザイナー<ept id="p1">**</ept> ページを閉じます。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="296">
          <source>Close the <bpt id="p1">**</bpt>Model mappings<ept id="p1">**</ept> page.</source><target logoport:matchpercent="73" state="translated" state-qualifier="fuzzy-match"><bpt id="p1">**</bpt>モデル マッピング<ept id="p1">**</ept> ページを閉じます。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="297">
          <source>Complete the modified version of the ER model mapping</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">ER モデル マッピングの変更されたバージョンを完了する</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="298">
          <source>In RCS, on the <bpt id="p1">**</bpt>Configurations<ept id="p1">**</ept> page, on the <bpt id="p2">**</bpt>Versions<ept id="p2">**</ept> FastTab, select version <bpt id="p3">**</bpt>1.2<ept id="p3">**</ept> of the <bpt id="p4">**</bpt>Performance trace mapping<ept id="p4">**</ept> configuration.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">RCS、<bpt id="p1">**</bpt>コンフィギュレーション<ept id="p1">**</ept> ページの、<bpt id="p2">**</bpt>バージョン<ept id="p2">**</ept> クイック タブで、<bpt id="p4">**</bpt>パフォーマンス追跡マッピング<ept id="p4">**</ept> コンフィギュレーションのバージョン <bpt id="p3">**</bpt>1.2<ept id="p3">**</ept> を選択します。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="299">
          <source>Select <bpt id="p1">**</bpt>Change status<ept id="p1">**</ept>.</source><target logoport:matchpercent="0" state="translated"><bpt id="p1">**</bpt>ステータスの変更<ept id="p1">**</ept>を選択します。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="300">
          <source>Select <bpt id="p1">**</bpt>Complete<ept id="p1">**</ept>.</source><target logoport:matchpercent="0" state="translated"><bpt id="p1">**</bpt>完了<ept id="p1">**</ept>を選択します。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="301">
          <source>Import the modified ER model mapping configuration from RCS into Finance and Operations</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">変更された ER モデル マッピング コンフィギュレーションを RCS から Finance and Operations にインポートする</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="302">
          <source>Repeat the steps in the <bpt id="p1">[</bpt>Import an ER configuration from RCS into Finance and Operations<ept id="p1">](#import-configuration)</ept> section earlier in this topic to import version 1.2 of the <bpt id="p2">**</bpt>Performance trace mapping<ept id="p2">**</ept> configuration into Finance and Operations.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">このトピックの先のセクション <bpt id="p1">[</bpt>ER コンフィギュレーションを RCS から Finance and Operations にインポートする<ept id="p1">](#import-configuration)</ept> の手順を繰り返して、<bpt id="p2">**</bpt>パフォーマンス追跡マッピング<ept id="p2">**</ept> コンフィギュレーションのバージョン 1.2 を Finance and Operations にインポートします。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="303">
          <source>Run the modified ER solution to trace execution</source><target logoport:matchpercent="86" state="translated" state-qualifier="fuzzy-match">変更された ER ソリューションを実行して追跡実行する</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="304">
          <source>Run the ER format</source><target logoport:matchpercent="100" state="translated" state-qualifier="exact-match">ER 形式を実行する</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="305">
          <source>Repeat the steps in the <bpt id="p1">[</bpt>Run the ER format<ept id="p1">](#run-format)</ept> section earlier in this topic to generate a new performance trace.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">このトピックの先のセクション <bpt id="p1">[</bpt>ER 形式を実行する<ept id="p1">](#run-format)</ept> の手順を繰り返して、新しいパフォーマンス追跡を生成します。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="306">
          <source>Review the execution trace</source>
        <target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-inherited">実行追跡の確認</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="307">
          <source>Export the generated trace from Finance and Operations</source><target logoport:matchpercent="100" state="translated" state-qualifier="exact-match">生成された追跡を Finance and Operations からエクスポートする</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="308">
          <source>Repeat the steps in the <bpt id="p1">[</bpt>Export the generated trace from Finance and Operations<ept id="p1">](#export-trace)</ept> section earlier in this topic to save a new performance trace locally.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">このトピックの先のセクション <bpt id="p1">[</bpt>生成された追跡を Finance and Operations からエクスポートする<ept id="p1">](#export-trace)</ept> の手順を繰り返して、新しいパフォーマンス追跡をローカルに保存します。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="309">
          <source>Import the generated trace into RCS</source><target logoport:matchpercent="100" state="translated" state-qualifier="exact-match">生成された追跡を RCS にインポートする</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="310">
          <source>Repeat the steps in the <bpt id="p1">[</bpt>Import the generated trace into RCS<ept id="p1">](#import-trace)</ept> section earlier in this topic to import the new performance trace into RCS.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">このトピックの先のセクション <bpt id="p1">[</bpt>生成された追跡を RCS にインポートする<ept id="p1">](#import-trace)</ept> の手順を繰り返して、新しいパフォーマンス追跡を RCS にインポートします。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="311">
          <source>Use the performance trace for analysis in RCS – Model mapping</source><target logoport:matchpercent="100" state="translated" state-qualifier="exact-match">RCS での分析に対するパフォーマンス追跡の使用 – モデル マッピング</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="312">
          <source>Repeat the steps in the <bpt id="p1">[</bpt>Use the performance trace for analysis in RCS – Model mapping<ept id="p1">](#use-trace)</ept> section earlier in this topic to analyze the latest performance trace.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">このトピックの先のセクション <bpt id="p1">[</bpt>RCS での分析に対するパフォーマンス追跡の使用 – モデル マッピング<ept id="p1">](#use-trace)</ept> の手順を繰り返して、最新のパフォーマンス追跡を分析します。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="313">
          <source>Notice that the adjustments that you made to the model mapping have eliminated duplicate queries to database.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">モデル マッピングに対して行った調整によって、データベースへの重複するクエリが消去されたことに注意してください。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="314">
          <source>The number of calls to database tables and data sources for this model mapping has been also reduced.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">このモデル マッピングのデータベース テーブルおよびデータ ソースへの呼び出し数も減少しました。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="315">
          <source>Therefore, the performance of the whole ER solution has improved.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">したがって、ER ソリューション全体のパフォーマンスが向上しました。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="316">
          <source>Trace information for the VendTable data source on the Model mapping designer page in RCS</source><target logoport:matchpercent="74" state="translated" state-qualifier="fuzzy-match">RCS の、モデル マッピング デザイナー ページで、VendTable データ ソースに関する情報を追跡します。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="317">
          <source>In the trace information, the value <bpt id="p1">**</bpt><ph id="ph1">\[</ph>12<ph id="ph2">\]</ph><ept id="p1">**</ept> for the VendTable data source indicates that this data source was called 12 times.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">追跡情報で、VendTable データ ソースの <bpt id="p1">**</bpt><ph id="ph1">\[</ph>12<ph id="ph2">\]</ph><ept id="p1">**</ept> の値は、このデータソースが 12 回呼び出されたことを示します。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="318">
          <source>The value <bpt id="p1">**</bpt><ph id="ph1">\[</ph>Q:6<ph id="ph2">\]</ph><ept id="p1">**</ept> indicates that six calls were translated to database calls to the VendTable table.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt"><bpt id="p1">**</bpt><ph id="ph1">\[</ph>Q:6<ph id="ph2">\]</ph><ept id="p1">**</ept> の値は、6 つの呼び出しが VendTable テーブルへのデータベース呼び出しに変換されたことを示します。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="319">
          <source>The value <bpt id="p1">**</bpt><ph id="ph1">\[</ph>C:6<ph id="ph2">\]</ph><ept id="p1">**</ept> indicates that the records that were fetched from the database were cached, and six other calls were processed by using the cache.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt"><bpt id="p1">**</bpt><ph id="ph1">\[</ph>C:6<ph id="ph2">\]</ph><ept id="p1">**</ept> の値は、データベースからフェッチされたレコードがキャッシュされ、その他の 6 つの呼び出しがキャッシュを使用して処理されたことを示します。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="320">
          <source>Notice that the number of calls to the LedgerTransTypeList data source has been reduced from 9,027 to 240.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">LedgerTransTypeList データソースへの呼び出し数が 9,027 から 240 に減少したことに注意してください。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="321">
          <source>Trace information for the LedgerTransTypeList data source on the Model mapping designer page in RCS</source><target logoport:matchpercent="91" state="translated" state-qualifier="fuzzy-match">RCS の モデル マッピング デザイナー ページで、LedgerTransTypeList データ ソースに関する情報を追跡します。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="322">
          <source>Review the execution trace in Finance and Operations</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Finance and Operations での実行追跡の確認</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="323">
          <source>In addition to RCS, some versions of Finance and Operations might offer capabilities for an ER framework designer experience.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">RCS に加えて、Finance and Operations の一部のバージョンでは ER フレームワーク デザイナー経験に対する機能が提供される場合があります。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="324">
          <source>These versions of Finance and Operations have an <bpt id="p1">**</bpt>Enable design mode<ept id="p1">**</ept> option that can be turned on.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Finance and Operations のこれらのバージョンには<bpt id="p1">**</bpt>デザイン モードを有効にする<ept id="p1">**</ept>オプションがあり、有効にすることができます。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="325">
          <source>You can find this option on the <bpt id="p1">**</bpt>General<ept id="p1">**</ept> tab of the <bpt id="p2">**</bpt>Electronic reporting parameters<ept id="p2">**</ept> page, which you can open from the <bpt id="p3">**</bpt>Electronic reporting<ept id="p3">**</ept> workspace.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">このオプションは<bpt id="p2">**</bpt>電子申告パラメーター<ept id="p2">**</ept>ページの<bpt id="p1">**</bpt>一般<ept id="p1">**</ept>タブで検索できます。このページは<bpt id="p3">**</bpt>電子申告<ept id="p3">**</ept>ワークスペースから開くことができます。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="326">
          <source>Enable design mode option on the Electronic reporting parameters page in Finance and Operations</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Finance and Operations の電子申告パラメーター ページでデザイン モード オプションを有効にする</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="327">
          <source>If you use one of these versions of Finance and Operations, you can analyze the details of generated performance traces directly in Finance and Operations.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Finance and Operations のいずれかのバージョンを使用する場合は、生成されたパフォーマンス追跡の詳細を Finance and Operations で直接分析できます。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="328">
          <source>You don't have to export them from Finance and Operation and import them into RCS.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Finance and Operations からエクスポートして RCS にインポートする必要はありません。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="329">
          <source>Review the execution trace by using external tools</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">外部ツールを使用した実行追跡の確認</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="330">
          <source>Configure user parameters</source><target logoport:matchpercent="87" state="translated" state-qualifier="fuzzy-match">ユーザー パラメーターのコンフィギュレーション</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="331">
          <source>In Finance and Operations, go to <bpt id="p1">**</bpt>Organization administration <ph id="ph1">\&gt;</ph> Electronic reporting <ph id="ph2">\&gt;</ph> Configurations<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="0" state="translated" state-qualifier="leveraged-inherited">Finance and Operations で、<bpt id="p1">**</bpt>組織管理 <ph id="ph1">\&gt;</ph> 電子申告 <ph id="ph2">\&gt;</ph> 構成<ept id="p1">**</ept>の順に移動します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="332">
          <source>On the <bpt id="p1">**</bpt>Configurations<ept id="p1">**</ept> page, on the Action Pane, on the <bpt id="p2">**</bpt>Configurations<ept id="p2">**</ept> tab, in the <bpt id="p3">**</bpt>Advanced settings<ept id="p3">**</ept> group, select <bpt id="p4">**</bpt>User parameters<ept id="p4">**</ept>.</source>
        <target logoport:matchpercent="72" state="translated" state-qualifier="leveraged-inherited"><bpt id="p1">**</bpt>構成<ept id="p1">**</ept>ページ、アクション ウィンドウ、<bpt id="p2">**</bpt>構成<ept id="p2">**</ept>タブ、<bpt id="p3">**</bpt>詳細設定<ept id="p3">**</ept>グループで、<bpt id="p4">**</bpt>ユーザー パラメーター<ept id="p4">**</ept>を選択します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="333">
          <source>In the <bpt id="p1">**</bpt>User parameters<ept id="p1">**</ept> dialog box, in the <bpt id="p2">**</bpt>Execution tracing<ept id="p2">**</ept> section, in the <bpt id="p3">**</bpt>Execution trace format<ept id="p3">**</ept> field, select <bpt id="p4">**</bpt>PerfView XML<ept id="p4">**</ept>.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt"><bpt id="p1">**</bpt>ユーザー パラメーター<ept id="p1">**</ept> ダイアログ ボックス、<bpt id="p2">**</bpt>実行トレース<ept id="p2">**</ept> セクションの、<bpt id="p3">**</bpt>実行トレース形式<ept id="p3">**</ept>フィールドで、<bpt id="p4">**</bpt>PerfView XML<ept id="p4">**</ept> を選択します。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="334">
          <source>Run the ER format</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-inherited">ER 形式を実行する</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="335">
          <source>Repeat the steps in the <bpt id="p1">[</bpt>Run the ER format<ept id="p1">](#run-format)</ept> section earlier in this topic to generate a new performance trace.</source>
        <target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-inherited">このトピックの先のセクション <bpt id="p1">[</bpt>ER 形式を実行する<ept id="p1">](#run-format)</ept> の手順を繰り返して、新しいパフォーマンス追跡を生成します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="336">
          <source>Notice that the web browser offers a zip file for download.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Web ブラウザーによって、ダウンロード用の zip ファイルが提供されていることに注意してください。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="337">
          <source>This file contains the performance trace in PerfView format.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">このファイルには、PerfView 形式のパフォーマンス追跡が含まれています。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="338">
          <source>You can then use the PerfView performance analysis tool to analyze the details of ER format execution.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">次に、PerfView パフォーマンス分析ツールを使用して ER 形式実行の詳細を分析できます。</target>
        </trans-unit>
      </group>
    </body>
  </file>
</xliff>