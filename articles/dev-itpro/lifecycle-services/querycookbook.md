<?xml version="1.0" encoding="UTF-8"?>
<xliff xmlns:logoport="urn:logoport:xliffeditor:xliff-extras:1.0" xmlns:tilt="urn:logoport:xliffeditor:tilt-non-translatables:1.0" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns="urn:oasis:names:tc:xliff:document:1.2" xmlns:xliffext="urn:microsoft:content:schema:xliffextensions" version="1.2" xsi:schemaLocation="urn:oasis:names:tc:xliff:document:1.2 xliff-core-1.2-transitional.xsd">
  <file datatype="xml" source-language="en-US" original="querycookbook.md" target-language="ja-JP">
    <header>
      <tool tool-company="Microsoft" tool-version="1.0-7889195" tool-name="mdxliff" tool-id="mdxliff"/>
      <xliffext:skl_file_name>querycookbook.483188.f4060f711a0b240ec448dd944a6032551dfda394.skl</xliffext:skl_file_name>
      <xliffext:version>1.2</xliffext:version>
      <xliffext:ms.openlocfilehash>f4060f711a0b240ec448dd944a6032551dfda394</xliffext:ms.openlocfilehash>
      <xliffext:ms.sourcegitcommit>9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b</xliffext:ms.sourcegitcommit>
      <xliffext:ms.lasthandoff>05/15/2019</xliffext:ms.lasthandoff>
      <xliffext:ms.openlocfilepath>articles\dev-itpro\lifecycle-services\querycookbook.md</xliffext:ms.openlocfilepath>
    </header>
    <body>
      <group extype="content" id="content">
        <trans-unit xml:space="preserve" translate="yes" id="101" restype="x-metadata">
          <source>Query cookbook</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">クックブックの照会</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="102" restype="x-metadata">
          <source>This topic provides details on each query under the SQL Insights tab on the Environment Monitoring page in LCS and how they should be used when troubleshooting performance issues.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このトピックでは、LCS の [環境の監視] ページにある [SQL インサイト] タブの下の各クエリの詳細と、パフォーマンスの問題のトラブルシューティングを行うときにそれらを使う方法を示します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="103">
          <source>Query cookbook</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">クックブックの照会</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="104">
          <source>This topic provides details on each query under the <bpt id="p1">**</bpt>SQL Insights<ept id="p1">**</ept> tab on the <bpt id="p2">**</bpt>Environment Monitoring<ept id="p2">**</ept> page in Lifecycle Services (LCS) and how they should be used when troubleshooting performance issues.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このトピックでは、Lifecycle Services (LCS) の <bpt id="p1">**</bpt>環境の監視<ept id="p1">**</ept> ページにある <bpt id="p2">**</bpt>SQL インサイト<ept id="p2">**</ept> タブの下の各クエリの詳細と、パフォーマンスの問題のトラブルシューティングを行うときにそれらを使う方法を示します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="105">
          <source>For details about this feature, see <bpt id="p1">[</bpt>Performance troubleshooting using tools in Lifecycle Services (LCS)<ept id="p1">](performancetroubleshooting.md)</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この機能の詳細については、<bpt id="p1">[</bpt>Lifecycle Services (LCS) でツールを使用したパフォーマンスのトラブルシューティング<ept id="p1">](performancetroubleshooting.md)</ept>を参照してください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="106">
          <source>Current blocking</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">現在のブロック</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="107">
          <source>Description</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">説明</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="108">
          <source>Lists any currently blocked queries, and also the SPID that is blocking them, how long they have been blocked, and what resource they are waiting on.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">現在ブロックされているクエリ、それらをブロックしている SPID、ブロックされている期間、待機しているリソースをリストします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="109">
          <source>This can be used in conjunction with the query to see the blocking tree, which provides a graphical overview of some of the same information.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">これは、同じ情報の一部のグラフィカルな概要を表示するブロック ツリーを表示するためのクエリと組み合わせて使用できます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="110">
          <source>Blocking by itself is normal in a healthy system and is only a problem when it becomes excessive or starts degrading business activities.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">正常なシステムでは単独でブロックするのが通常であり、過剰になったり、営業活動に悪影響を及ぼし始めたときのみ問題となります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="111">
          <source>Next steps</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">次のステップ</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="112">
          <source>Determine which process is blocked, and which process is blocking it and why.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">どのプロセスがブロックされているかを決定し、どのプロセスがブロックしているかとその理由を判別します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="113">
          <source>To resolve blocking, the only two options are to let it run and clear naturally, or to end the lead blocker process, which will roll back work.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ブロックを解決するには、実行させて自然にクリアさせるか、リード ブロッカー プロセスを終了して作業をロールバックするかの 2 つのオプションのみです。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="114">
          <source>Generally, the lead blocker should only end in situations where it is not believed that it will clear naturally (such as a bad query plan), or in situations where a critical process is unable to run and needs to be completed immediately.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">一般に、リード ブロッカーは、自然にクリアすると思われない状況 (不適切なクエリ プランの場合など) や、重要なプロセスを実行できないためにすぐに完了する必要があるような状況でのみ終了する必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="115">
          <source>To avoid the same blocking in the future, you can use indexes or plan guides, or disable lock escalation and page locks if processes are blocking each other while operating on different records.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">将来同じブロックを避けるため、インデックスまたはプラン ガイドを使用したり、各種レコードでの操作中にプロセスが互いにブロックしている場合はロック エスカレーションおよびページ ロックを無効にできます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="116">
          <source>If processes are operating on the same records, the only way to avoid blocking is by refactoring or rescheduling the processes so that they do not operate on the same records at the same time.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">プロセスが同じレコードで動作している場合、ブロックを回避するには、同時に同じレコード上で動作しないように、プロセスをリファクタリングまたは再スケジューリングする必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="117">
          <source>Current blocking tree</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">現在のブロック ツリー</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="118">
          <source>Description</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">説明</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="119">
          <source>Provides a graphical view of the SPIDs and statements that are currently causing blocking or being blocked.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">現在ブロックしているかブロックされている SPID およびステートメントのグラフィカル表示を提供します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="120">
          <source>This can be used in conjunction with the current blocking query to see more detailed information.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">これは、詳細な情報を表示するために現在のブロック クエリと組み合わせて使用できます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="121">
          <source>Blocking by itself is normal in a healthy system and is only a problem when it becomes excessive or starts degrading business activities.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">正常なシステムでは単独でブロックするのが通常であり、過剰になったり、営業活動に悪影響を及ぼし始めたときのみ問題となります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="122">
          <source>Next steps</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">次のステップ</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="123">
          <source>Determine which process is blocked, and which process is blocking it and why.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">どのプロセスがブロックされているかを決定し、どのプロセスがブロックしているかとその理由を判別します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="124">
          <source>To resolve blocking, the only two options are to let it run and clear naturally, or to end the lead blocker process, which will roll back work.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ブロックを解決するには、実行させて自然にクリアさせるか、リード ブロッカー プロセスを終了して作業をロールバックするかの 2 つのオプションのみです。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="125">
          <source>Generally, the lead blocker should only end in situations where it is believed that it will not clear naturally (such as a bad query plan), or in situations where a critical process is unable to run and needs to be completed immediately.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">一般に、リード ブロッカーは、自然にクリアしないと思われる状況 (不適切なクエリ プランの場合など) や、重要なプロセスを実行できないためにすぐに完了する必要があるような状況でのみ終了する必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="126">
          <source>To avoid the same blocking in the future, you can use indexes or plan guides, or disable lock escalation and page locks, if processes processes are blocking each other while operating on different records.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">将来同じブロックを避けるため、インデックスまたはプラン ガイドを使用したり、各種レコードでの操作中にプロセスが互いにブロックしている場合はロック エスカレーションおよびページ ロックを無効にできます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="127">
          <source>If processes are operating on the same records, the only way to avoid blocking is by refactoring or rescheduling the processes so that they do not operate on the same records at the same time.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">プロセスが同じレコードで動作している場合、ブロックを回避するには、同時に同じレコード上で動作しないように、プロセスをリファクタリングまたは再スケジューリングする必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="128">
          <source>Current DTU</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">現在の DTU</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="129">
          <source>Description</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">説明</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="130">
          <source>Provides a detailed breakdown of the current DTU by component.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">コンポーネントごとの現在の DTU の詳細を提供します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="131">
          <source>DTU is a percentage measure of total SQL load and is reported as the maximum value of any of the subcomponents.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">DTU は、合計 SQL 負荷のパーセンテージ測定であり、いずれかのサブコンポーネントの最大値として報告されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="132">
          <source>Use this query to determine which subcomponent is causing high DTU.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このクエリを使用して、高 DTU の原因となっているサブコンポーネントを決定します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="133">
          <source>High CPU is often related to bad query plans.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">高い CPU は、多くの場合不適切なクエリ プランに関連しています。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="134">
          <source>High Data I/O is often related to large imports or exports.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">高いデータ入出力は、多くの場合、大規模なにインポートまたはエクスポートに関連しています。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="135">
          <source>A high Log Write percentage is often related to bulk processes, such as reporting, which make changes to large numbers of intermediate records.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">高いログ書き込み率は、多くの場合、大量の中間レコードを変更するレポートなどのバルク プロセスに関連しています。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="136">
          <source>Next steps</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">次のステップ</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="137">
          <source>If high CPU is the cause of high DTU, view the currently running queries or most expensive queries for the last hour.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">高い CPU の原因が高い DTU の場合、現在実行中のクエリまたは最後の 1 時間の最も高価なクエリを表示します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="138">
          <source>To address the issue, get better query plans by adding indexes, changing the query, or, as a last resort, adding plan guides.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">問題に対処するには、インデックスの追加、クエリの変更、または最後の手段としてクエリ プランの追加により、クエリ プランを改善します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="139">
          <source>If high Data I/O is the cause of high DTU, look at currently running queries and also current batch jobs, and try to determine what might be writing large volumes of data.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">多数のデータ入出力の原因が高い DTU の場合、現在実行中のクエリと現在のバッチ ジョブを調べ、何が大量のデータを書き込んでいる可能性があるかを判別してみます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="140">
          <source>Consider scheduling those processes to run outside of business hours.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">営業時間外部に実行するようそれらのプロセスのスケジュール設定を検討してください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="141">
          <source>If high Log I/O is the cause of high DTU, look at currently running queries and also current batch jobs to determine what might be doing large amounts of intermediate processing.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">高いログ入出力の原因が高い DTU の場合、現在実行中のクエリと現在のバッチ ジョブを調べ、何が大量の即時処理を行っている可能性があるかを判別します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="142">
          <source>Often, high Log I/O is caused by the use of real fully logged tables as pseudo-temp tables during processing, such as in reporting.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">多くの場合、多数のログ入出力は、レポートなど、処理中に疑似一時テーブルとして実際に完全にログ記録されるテーブルを使用することで発生します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="143">
          <source>Address this by running those processes outside of business hours or by changing the processes.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">これらのプロセスを営業時間外に実行するか、プロセスを変更することによりこの問題を解決します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="144">
          <source>Currently running queries</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">現在実行中のクエリ</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="145">
          <source>Description</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">説明</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="146">
          <source>Provides a list of all queries that are currently in a state of being executed or blocked on this database, and also the total execution and wait times of each query.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このデータベースで現在実行状態またはブロック状態のすべてのクエリのリストと、各クエリの合計実行および待機時間も提供します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="147">
          <source>Queries that have high execution time and low wait time are often indicative of bad query plans.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">実行時間が長く待機時間が短いクエリは多くの場合不適切なクエリ プランであることを示します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="148">
          <source>Queries with high wait time and low execution time are indicative of blocking.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">待機時間が長くクエリと実行時間が短いクエリはブロックを示しています。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="149">
          <source>If relatively fast operations are being run many times, sometimes they can be found by running this query multiple times in a row and looking for commonly occurring queries with fast execution time.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">比較的高速な操作が何回も実行されている場合、行でこのクエリを複数回実行し、実行時間が短い頻繁に発生するクエリを探すことで見つけることができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="150">
          <source>Next steps</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">次のステップ</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="151">
          <source>If high CPU time is seen, get the query plan for the query, and also see whether other query plans that have been used for this query are more efficient.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">高い CPU 時間が見られる場合、クエリのクエリ プランを取得し、このクエリに使用されている他のクエリ プランの方が効率的かどうかも確認します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="152">
          <source>Consider addressing the issues with a new index, with a change to the query, or, as a last resort, by adding a plan guide.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">新しいクエリ、クエリの変更、または最後の手段としてプラン ガイドを追加することにより、この問題に対処することを検討してください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="153">
          <source>If high wait time is seen, view the current blocking and current blocking tree to determine why the query is blocked.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">高い待機時間が見られる場合、現在のブロックおよび現在のブロック ツリーを表示してクエリがブロックされている理由を判断します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="154">
          <source>This is occasionally addressed by disabling lock escalation or page locks if that is the cause of the blocking.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">これは、場合によっては、ロック エスカレーションまたはページ ロックを無効にすることで (これがブロックの原因の場合) 対処できます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="155">
          <source>More often, it is addressed by segmenting the work that is being performed to ensure that the same record is not processed by two queries at the same time.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">通常は、2 つのクエリにより同じレコードが同時に処理されないように、実行される作業を分割することにより対処されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="156">
          <source>Get fragmentation details</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">断片化の詳細の取得</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="157">
          <source>Description</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">説明</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="158">
          <source>Fragmentation is when the records are not stored contiguously inside of the page.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">断片化は、レコードがページの内部に連続して格納されない場合に発生します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="159">
          <source>When there is unused space between records on a page, which occurs through data modification that is made against the table and to the indexes defined on the table, this is SQL index fragmentation.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">テーブルに対して行われたデータ変更や、テーブルで定義されたインデックスにおこなわれたデータ変更を通じて発生した未使用のスペースがページ上のレコード間にある場合、これが SQL インデックスの断片化となります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="160">
          <source>Dynamics 365 for Finance and Operations uses SQL Azure DB premium SKUs which are backed by SSDs.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Dynamics 365 for Finance and Operations では SSD によってサポートされている SQL Azure DB プレミアム SKU を使用します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="161">
          <source>This means that the fragmentation does not cause the same level of issues as on a database that is backed by a SCSI drive, but it still it could cause slower performance.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">これは、断片化により、SCSI ドライブを装備したデータベースと同じ問題は発生しませんが、パフォーマンスは低下する可能性があることを意味します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="162">
          <source>With higher fragmentation, there is a higher chance that it could affect the performance of queries that use this fragmented table/index.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">断片化が増えると、この断片化したテーブルやインデックスを使用するクエリのパフォーマンスに影響を与える可能性が高くなります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="163">
          <source>Next steps</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">次のステップ</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="164">
          <source>This query shows the list of tables, indexes with their fragmentation percentage, and a recommendation to either REBUILD the index or REORG the index.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このクエリは、テーブルのリスト、断片化率を含むインデックス、インデックスの再構築またはインデックスの再編成の推奨事項を表示します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="165">
          <source>When you rebuild or reorg an index it will pack the records next to each other and avoid gaps in between, thus reducing the fragmentation.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">インデックスを再構築または再編成すると、レコードが互いに並べてパッキングされ、その間にすきまが生じないようにされるため、断片化が軽減されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="166">
          <source>Get index details</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">インデックスの詳細の取得</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="167">
          <source>Description</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">説明</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="168">
          <source>Provides details about all indexes on a given table.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">特定のテーブルのすべてのインデックスに関する詳細を提供します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="169">
          <source>This query is usually used before adding new indexes, to ensure there are no existing indexes that should be altered instead.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">通常、このクエリは、代わりに変更する必要がある既存のインデックスがないようにするため、新しいインデックスを追加する前に使用されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="170">
          <source>Next steps</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">次のステップ</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="171">
          <source>If you are adding a new index, verify that there is not an existing index that should just be adjusted instead.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">新しいインデックスを追加する場合は、代わりに調整する必要がある既存のインデックスがないことを確認します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="172">
          <source>Each new index adds overhead on all write operations.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">新しい各インデックスは、すべての書き込み操作でオーバーヘッドを追加します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="173">
          <source>Therefore, new indexes should be added sparingly.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">したがって、新しいインデックスはあまり追加しないでください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="174">
          <source>Existing indexes can occasionally cause blocking if they support page locks, and large processes running at the same time are locking pages that contain records for each process.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ページ ロックがサポートされている場合、既存のインデックスによりブロックが発生することがときどきあり、同時に実行されている大規模なプロセスは、プロセスごとのレコードを含むページをロックしています。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="175">
          <source>Disabling page locks should also be done sparingly, because it will degrade write operations that would have benefitted from page locks.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ページ ロックの無効化はあまり行わないでください。ページ ロックを活用している書き込み操作のパフォーマンスが低下する可能性があるためです。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="176">
          <source>Get lock details</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ロックの詳細の取得</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="177">
          <source>Description</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">説明</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="178">
          <source>Provides a list of all locks held by a given SPID.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">特定の SPID によって保持されているすべてのロックの一覧を示します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="179">
          <source>This is useful when a blocking tree shows that a SPID is part of a blocking chain.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">これは、SPID がブロック チェーンの一部であることをブロック ツリーが示している場合に便利です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="180">
          <source>Sometimes, this query will reveal that page locks or lock escalation are the cause of the blocking.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">場合によっては、このクエリによって、ページ ロックまたはロック エスカレーションがブロックの原因であることがわかります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="181">
          <source>Other times this query is useful for seeing how many keylocks in given tables are being held.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">それ以外の場合、このクエリは、保持されている特定のテーブル内のキーロックの数を調べるために便利です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="182">
          <source>Next steps</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">次のステップ</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="183">
          <source>If page locks or lock escalation are causing issues, they can be disabled.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ページ ロックまたはロック エスカレーションが問題の原因となっている場合、それらを無効にできます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="184">
          <source>However, this should be done cautiously, because there are valid cases where lock escalation and page locks are needed for good performance.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ただし、これは慎重に行う必要があります。高いパフォーマンスのためのロック エスカレーションおよびページ ロックが必要なことがあるためです。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="185">
          <source>If a SPID is just holding large numbers of locks, reducing the amount of data processed within one transactional scope can reduce the number of locks and therefore the chances of experiencing blocking and deadlocks.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">SPID のロックの数が多い場合、1 つのトランザクション範囲内で処理されるデータの量を減らすことで、ロックの数が減るため、ブロックやデッドロックの可能性を減らすことができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="186">
          <source>Parameters</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">パラメーター</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="187">
          <source>The SPID can be obtained either from the list of currently running queries or through the list of current blocking queries.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">SPID は、現在実行中のクエリのリストまたは現在ブロック中のクエリのリストから取得できます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="188">
          <source>No historical information about SPIDs is available because the SPID ID is only valid while the SPID is currently being executed.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">SPID に関する履歴情報はありません。SPID ID は、SPID が現在実行中のときのみ有効なためです。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="189">
          <source>List of current plan guides</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">現在のプラン ガイドの一覧</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="190">
          <source>Description</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">説明</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="191">
          <source>Provides a list of all plan guides currently installed in the database.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">データベースにインストールされているすべてのプラン ガイドの一覧を提供します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="192">
          <source>Next steps</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">次のステップ</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="193">
          <source>You can determine whether a query plan was created based on a plan guide by looking in the query plan XML.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">クエリ プラン XML で参照することで、クエリ プランがプラン ガイドに基づいて作成されたかどうかを判断することができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="194">
          <source>If the plan was generated based on a plan guide, the plan guide name will be specified in the XML.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">プラン ガイドに基づいてプランが生成された場合、プラン ガイド名は XML ファイルで指定されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="195">
          <source>If a plan guide is installed but is not being used, verify that the SQL statement text and parameter list for the plan guide are identical to the actual query.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">プラン ガイドがインストールされているが使用されていない場合、プラン ガイドの SQL ステートメントのテキスト パラメーター リストが実際のクエリと同じであることを確認します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="196">
          <source>Any differences, even in whitespace, will stop a plan guide from being used.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">違いがある場合 (空白だけでも)、プラン ガイドの使用が停止されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="197">
          <source>Get list of query ID&amp;#39;s</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">クエリ ID のリストの取得</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="198">
          <source>Description</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">説明</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="199">
          <source>If query text is known to be causing a problem, this query can be used to find the query ID for that query.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">クエリ テキストが問題の原因となっているがわかっている場合、そのクエリのクエリ ID を検索するためにこのクエリを使用できます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="200">
          <source>This can occur if the SQL statement is showing up in an error message, in tracing, or in telemetry.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">これは、SQL ステートメントがエラー メッセージ、トレース、またはテレメトリに表示されている場合に発生することがあります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="201">
          <source>After the query ID for the statement is found, it can be used for other operations, such as finding query plans or applying plan guides.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">明細書のクエリ ID が見つかったら、クエリ プランの検索やプラン ガイドの適用などの他の操作で使用できます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="202">
          <source>Next steps</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">次のステップ</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="203">
          <source>After the query ID for a given statement is found, it can be used to find previous plans for that query so that it can be optimized.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">指定したステートメントのクエリ ID が検出されら、最適化できるようにそのクエリの以前のプランを探すために使用できます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="204">
          <source>Parameters</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">パラメーター</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="205">
          <source>Provide a substring of the query statement, such as <ph id="ph1">&amp;quot;</ph>%FROM GENERALJOURNALENTRY T1%<ph id="ph2">&amp;quot;</ph>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><ph id="ph1">&amp;quot;</ph>%FROM GENERALJOURNALENTRY T1%<ph id="ph2">&amp;quot;</ph> など、クエリ ステートメントの部分文字列を指定します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="206">
          <source>Get XML for a given plan ID</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">特定のプラン ID の XML の取得</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="207">
          <source>Description</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">説明</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="208">
          <source>This provides the SQL plan in XML format for a given plan ID.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">これにより、特定のプラン ID の SQL プランが XML 形式で提供されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="209">
          <source>Next steps</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">次のステップ</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="210">
          <source>Save the XML as a .sqlplan file, and open it in SQL Server Management Studio or other plan reading tools.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">XML を .sqlplan ファイルとして保存し、SQL Server Management Studio または他のプラン閲覧ツールで開きます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="211">
          <source>From the query plan, you can often find optimizations, such as index additions, that will be beneficial.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">クエリ プランからは、インデックスの追加など、多くの場合に有益な最適化を見つけることができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="212">
          <source>The plan might have an index recommendation listed, but be cautious when applying those indexes.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">プランによりインデックスの推奨がリストされることがありますが、それらのインデックスを適用する場合に注意が必要になります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="213">
          <source>SQL will often recommend creating indexes with excessive numbers of columns to optimize a single query, which can have a negative impact on other queries or the system as a whole.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">SQL は、多くの場合、1 つのクエリを最適化するための過剰な数の列を持つインデックスを作成することを推奨します。これは、他のクエリまたはシステム全体に影響を及ぼすことがあります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="214">
          <source>View these recommended indexes as hints to begin analysis, not as something to be directly applied.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">これらの推奨インデックスは、直接適用されるものとしてではなく、分析を開始するヒントとして表示します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="215">
          <source>Parameters</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">パラメーター</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="216">
          <source>The plan ID can be obtained from a variety of sources, such as currently running queries.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">プラン ID は、現在実行中のクエリなど、さまざまなソースから入手できます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="217">
          <source>If you only have a query ID, you can use <ph id="ph1">&amp;quot;</ph>get a list of query plans for a query<ph id="ph2">&amp;quot;</ph> to figure out which plan IDs have been used for a query.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">クエリ ID のみ持つ場合、<ph id="ph1">&amp;quot;</ph>クエリのクエリ プランの一覧の取得<ph id="ph2">&amp;quot;</ph> を使って、クエリの使用されているプラン ID を調べます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="218">
          <source>Get query plan and execution stats</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">クエリ プランと実行統計の取得</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="219">
          <source>Description</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">説明</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="220">
          <source>Provides a list of plans and execution statistics for a given query.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">特定のクエリのプランおよび実行統計の一覧を提供します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="221">
          <source>This is useful for determining whether a query is obtaining multiple query plans with different performance characteristics over time.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">これは、クエリが、時間の経過と共にさまざまなパフォーマンスの特性を持つ複数のクエリ プランを取得しているかどうかを判断するのに役立ちます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="222">
          <source>Next steps</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">次のステップ</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="223">
          <source>If a query is getting multiple query plans with vastly different performance characteristics, start by retrieving and analyzing the plans to determine what is different and why one is far better than others.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">クエリがパフォーマンス特性が大幅に異なる複数のクエリ プランを取得している場合は、何が異なっていて、他のものよりずっとよい理由を調べるために、まずプランを取得して分析します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="224">
          <source>In order for SQL to use a better query plan, the best solution is to make index changes or add query hints directly in code.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">SQL で優れたクエリ プランを使用するには、最適なソリューションとして、インデックスの変更を行うかコードに直接クエリ ヒントを追加します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="225">
          <source>If indexes and query hints are not enough, as a last resort, a plan guide can be added to force the better plans always to be used.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">インデックスとクエリ ヒントが十分でない場合、最後の手段として、優れたプランが強制的に使用されるようにプラン ガイドを追加できます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="226">
          <source>Be careful when using a plan guide, because sometimes a query plan is fast for some parameter values but overly slow for other parameter values.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">クエリ プランを使用するときは注意してください。クエリ プランは、パラメーター値によって高速であったり非常に低速であったりすることがあるためです。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="227">
          <source>Parameters</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">パラメーター</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="228">
          <source>The <bpt id="p1">**</bpt>query ID<ept id="p1">**</ept> can be obtained from multiple other operations, such as currently running queries, current blocking queries, most expensive queries, and query by statement text.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>クエリ ID<ept id="p1">**</ept> は、現在実行中のクエリ、現在ブロック中のクエリ、最も高価なクエリ、およびステートメント テキストによるクエリなど、他の複数の工程から取得できます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="229">
          <source>The <bpt id="p1">**</bpt>time interval<ept id="p1">**</ept> in terms of hours will often be specified as <ph id="ph1">&amp;quot;</ph>168<ph id="ph2">&amp;quot;</ph> to show all plans for the last week or <ph id="ph3">&amp;quot;</ph>24<ph id="ph4">&amp;quot;</ph> to show all plans for the last day.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">時間数単位の<bpt id="p1">**</bpt>時間間隔<ept id="p1">**</ept>は、多くの場合、前週のすべてのプランを示すために <ph id="ph1">&amp;quot;</ph>168<ph id="ph2">&amp;quot;</ph> として、前日のすべてのプランを示すために <ph id="ph3">&amp;quot;</ph>24<ph id="ph4">&amp;quot;</ph> として指定されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="230">
          <source>Often, plans will change multiple times per week but might be stable for a few days.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">多くの場合、プランは 1 週間に複数回変更されますが、数日安定する可能性があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="231">
          <source>Therefore, selecting larger intervals here is often advantageous.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">そのため、ここでそれ以上の間隔を選択と多くの場合有利です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="232">
          <source>Get wait stats</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">待機統計の取得</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="233">
          <source>Description</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">説明</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="234">
          <source>Provides information about what a given query plan has waited on in a given time range.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">指定された時間範囲で待機した特定のクエリ プランについて説明します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="235">
          <source>This is useful when a query regularly takes longer than it should, and you have been unable to determine whether it is CPU time or blocking.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">これは、定期的にクエリに予想より時間がかかり、CPU 時間であるかブロックであるかを判断できない場合に役立ちます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="236">
          <source>Similarly, if you see blocking but need to know what kind it is, this will provide that information.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">同様に、ブロックが見られるが、その種類がわからない場合、これはその情報を提供します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="237">
          <source>Next steps</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">次のステップ</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="238">
          <source>If a plan is primarily waiting on CPU, the plan is just inefficient and needs to be fixed through the addition of indexes or hints, or by restructuring the query.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">プランが主に CPU を待機している場合、プランは非効率的なだけではなく、インデックスまたはヒントを追加するか、クエリを再構築することで修正する必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="239">
          <source>If it is waiting on lock, the query is experiencing blocking.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ロックを待機している場合、クエリでブロックが発生しています。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="240">
          <source>This is more difficult to determine unless you can see the blocking happening actively through the blocking tree query.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">これは、ブロック ツリー クエリを通じてブロックがアクティブに発生していることを確認できるのでなければ、判断するのが困難です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="241">
          <source>In this case, the next step is to evaluate the records that are being edited and try to determine what other processes could be editing the same records at the same time.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この場合は、次の手順で、編集されるレコードを評価し、同時に同じレコードを編集する他のプロセスを判断することを試みます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="242">
          <source>Often, the same query running in multiple threads at the same time will block itself.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">多くの場合、同時に複数のスレッドで実行されている同じクエリが自分自身をブロックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="243">
          <source>If it is waiting on I/O or latch, there are likely either large volumes of data being transferred or large numbers of small transactions.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">入出力またはラッチを待機している場合、大量のデータが転送されているか、多数の小規模トランザクションが発生していると考えられます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="244">
          <source>If possible, perform writes in small batches instead of just one record per transaction.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">可能であれば、トランザクションごとに 1 つのレコードではなく小規模なバッチでの書き込みを実行します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="245">
          <source>Parameters</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">パラメーター</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="246">
          <source>The plan ID can be obtained from a variety of sources, including currently running queries and the most expensive queries.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">プラン ID は、さまざまなソース (現在実行中のクエリと最も高価なクエリを含む) から入手できます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="247">
          <source>If you have a query ID, you can get plan IDs by using the query to get a list of plans for that query.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">クエリ ID がある場合、クエリを使ってそのクエリのプランのリストを取得することで、プラン ID を取得できます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="248">
          <source>Ideally, the time range should target a specific time when an issue was occurring.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">原則的には、時間の範囲は問題が発生していた特定の時間を対象とする必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="249">
          <source>For instance, if DTU was high for an hour, you should target just that hour of execution.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">たとえば、DTU が 1 時間高かった場合、その実行時間だけを対象にする必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="250">
          <source>List most expensive queries</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">最も高価なクエリのリスト</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="251">
          <source>Description</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">説明</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="252">
          <source>Provides a list of the most expensive queries during the specified period.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">指定された期間内の最も高価なクエリの一覧を提供します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="253">
          <source>The decision about which attribute should be considered when computing most expensive queries can also be provided.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">最も高価なクエリを計算するときに考慮する必要がある属性の決定を提供することもできます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="254">
          <source>This is often used when high DTU is seen for a period, to determine which query is causing the high DTU.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">これは、ある期間に高い DTU が見られる場合に、どのクエリが高い DTU の原因となっているかを調べるためによく使用されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="255">
          <source>In order to use this query effectively, it is important to determine which DTU component is being addressed.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このクエリを効果的に使用するため、処理されている DTU コンポーネントを決定するために重要です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="256">
          <source>Next steps</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">次のステップ</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="257">
          <source>View the most expensive queries by total CPU to find queries that are causing high DTU utilization.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">DTU 使用率が高い原因となっているクエリを見つけるため、合計 CPU により最も高価なクエリを表示します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="258">
          <source>These queries are usually fixed through indexes, query changes, or, as a last resort, plan guides.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">通常、これらのクエリは、インデックス、クエリの変更、または、最後の手段としてプラン ガイドを通じて修正されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="259">
          <source>View the most expensive queries by total duration to find queries that might be slowing down the user experience.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ユーザー エクスペリエンスを遅くする可能性があるクエリを見つけるには、合計期間により最も高価なクエリを表示します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="260">
          <source>If these queries also have high total CPU, fix the query plans.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">これらのクエリの合計 CPU も高い場合、クエリ プランを修正します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="261">
          <source>If they have low CPU, it is likely the result of blocking.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">CPU が低い場合、ブロックの結果の可能性があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="262">
          <source>Parameters</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">パラメーター</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="263">
          <source>For the number of hours, specify <ph id="ph1">&amp;quot;</ph>0<ph id="ph2">&amp;quot;</ph> if you are looking at currently occurring issues, such as currently high DTU.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">現在 DTU が高いなど、現在発生している問題を調べている場合、時間数として <ph id="ph1">&amp;quot;</ph>0<ph id="ph2">&amp;quot;</ph> を指定します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="264">
          <source>This will provide results for the current hour.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">これは、現在の時間の結果を提供します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="265">
          <source>If you are looking for generally high DTU over time, specify either <ph id="ph1">&amp;quot;</ph>24<ph id="ph2">&amp;quot;</ph> for the last day or <ph id="ph3">&amp;quot;</ph>168<ph id="ph4">&amp;quot;</ph> for the last week.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">時間の経過と共に全体的に高い DTU を探している場合、最後の日として <ph id="ph1">&amp;quot;</ph>24<ph id="ph2">&amp;quot;</ph> を指定するか、最後の週として <ph id="ph3">&amp;quot;</ph>168<ph id="ph4">&amp;quot;</ph> を指定します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="266">
          <source>For the ordering, select <ph id="ph1">&amp;quot;</ph>total cpu<ph id="ph2">&amp;quot;</ph> to find high DTU impact for recurring queries.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">定期的なクエリの高い DTU の影響を見つけるには、順序として <ph id="ph1">&amp;quot;</ph>合計 CPU<ph id="ph2">&amp;quot;</ph> を選択します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="267">
          <source>Select <ph id="ph1">&amp;quot;</ph>average duration<ph id="ph2">&amp;quot;</ph> to find queries that are not run often but that might be slow.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">頻繁に実行されるわけではないが低速な可能性があるクエリを見つけるには、<ph id="ph1">&amp;quot;</ph>平均期間<ph id="ph2">&amp;quot;</ph> を選択します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="268">
          <source>Select <ph id="ph1">&amp;quot;</ph>total duration<ph id="ph2">&amp;quot;</ph> to find recurring queries that might be slowing down users.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ユーザーを遅くしている可能性がある定期的なクエリを検索するには、<ph id="ph1">&amp;quot;</ph>合計期間<ph id="ph2">&amp;quot;</ph> を選択します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="269">
          <source>Create non-unique index on table</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">テーブルでの一意ではないインデックスの作成</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="270">
          <source>Background</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">バックグラウンド</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="271">
          <source>Indexes should generally be created through the standard metadata package and database synchronization.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">通常、標準メタデータ パッケージとデータベースの同期によって、インデックスを作成する必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="272">
          <source>This ensures that Sandbox and PROD, and any other environments, always share a common definition.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">これにより、サンドボックスと PROD、およびその他の環境では、常に共通の定義が共有されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="273">
          <source>Occasionally, it is necessary to install a new non-unique index at runtime to mitigate an ongoing outage or issue where a regular deployment would take too long.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">場合によっては、定期的な展開に時間がかかりすぎる継続的な停止や問題を軽減するために、実行時に新しい非固有のインデックスをインストールする必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="274">
          <source>This action can be used to install that non-unique index.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このアクションは、その非固有インデックスのインストールに使用できます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="275">
          <source>Next steps</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">次のステップ</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="276">
          <source>After specifying the index to create, the next step should be to migrate that same index definition to the next available official metadata release.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">作成するインデックスを指定したら、次のステップとして、その同じインデックス定義を次の利用可能な正式メタデータ リリースに移行する必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="277">
          <source>Duplicate indexes generally do not cause any noticeable issues.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">一般に、重複するインデックスによって大きな問題が発生することはありません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="278">
          <source>Therefore, leave the manually created index in the system until after the official index has been completely rolled out.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">したがって、正式インデックスが完全に展開されるまでは、手動で作成したインデックスをシステムに置いたままにします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="279">
          <source>Parameters</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">パラメーター</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="280">
          <source>The index name is any unique string not currently in use by an existing index on this table.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">インデックス名は、次の表の既存のインデックスにより現在使用されていない任意の一意の文字列です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="281">
          <source>For easy identification, it is recommended but not required that the index name follow the format PERF<ph id="ph1">\_</ph>IDX<ph id="ph2">\_</ph><ph id="ph3">\&amp;</ph>lt;tablename<ph id="ph4">\&amp;</ph>gt;<ph id="ph5">\_</ph><ph id="ph6">\&amp;</ph>lt;number<ph id="ph7">\&amp;</ph>gt;.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">識別しやすいように、インデックス名が形式 PERF<ph id="ph1">\_</ph>IDX<ph id="ph2">\_</ph><ph id="ph3">\&amp;</ph>lt;tablename<ph id="ph4">\&amp;</ph>gt;<ph id="ph5">\_</ph><ph id="ph6">\&amp;</ph>lt;number<ph id="ph7">\&amp;</ph>gt; に従うことが推奨されますが、必須ではありません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="282">
          <source>For instance, an index might be named PERF<ph id="ph1">\_</ph>IDX<ph id="ph2">\_</ph>LEDGERJOURNALTRANS<ph id="ph3">\_</ph>1.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">たとえば、インデックスの名前は PERF<ph id="ph1">\_</ph>IDX<ph id="ph2">\_</ph>LEDGERJOURNALTRANS<ph id="ph3">\_</ph>1 にしてください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="283">
          <source>The columns parameter is a comma-separated list of physical column names in the order that they should appear in.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">列パラメーターは、表示される順序で記載された物理的な列名のコンマ区切り一覧です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="284">
          <source>The included columns parameter is a comma-separated list of physical column names in the order that they should appear in.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">含まれる列パラメーターは、表示される順序で記載された物理的な列名のコンマ区切り一覧です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="285">
          <source>If no included columns must be specified, leave this parameter blank.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">含まれている列を指定する必要がない場合、このパラメーターを空白のままにします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="286">
          <source>Create a plan guide to force Plan ID</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">プラン ID を強制するプラン ガイドの作成</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="287">
          <source>Description</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">説明</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="288">
          <source>SQL will recompute a new plan each time the plan cache is flushed, such as when an update of statistics runs.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">SQL では、統計の更新が実行されたときなど、プラン キャッシュがフラッシュされるたびに、新しいプランを再計算します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="289">
          <source>The plan that is chosen is based on <ph id="ph1">&amp;quot;</ph>sniffing<ph id="ph2">&amp;quot;</ph> the parameters of the first execution of that query.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">選択されているプランは、そのクエリの最初の実行のパラメーターの <ph id="ph1">&amp;quot;</ph>スニッフィング<ph id="ph2">&amp;quot;</ph> に基づきます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="290">
          <source>After that, the same plan will be used, regardless of parameters.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">その後、パラメータに関係なく同じプランが使用されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="291">
          <source>For this reason, the same query might sometimes get multiple plans, some of which are far worse than others for given data distributions.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このため、同じクエリが複数のプランを取得する場合があります。その一部は、特定のデータ配分のプランよりかなり悪くなります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="292">
          <source>This action can be used to force SQL to use a specific plan, regardless of which parameters are sniffed.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このアクションは、スニッフィングされるパラメーターに関係なく、特定のプランを使用するよう SQL を強制するために使用できます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="293">
          <source>Note that this action applies only to the database that it is executed on.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このアクションは、実行されるデータベースにのみ適用されることに注意してください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="294">
          <source>Therefore, it should be used as a last resort, after the addition of indexes, hints, or code changes that will flow between development and production environments.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">したがって、開発環境と製造環境間を流れるインデックス、ヒント、またはコード変更の追加後に、最後の手段として使用する必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="295">
          <source>Next steps</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">次のステップ</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="296">
          <source>After the list of plan IDs and execution statistics for a specific query ID are found, the SQL plan for each ID should be downloaded and analyzed.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">特定のクエリ ID のプラン ID と実行統計のリストが見つかったら、各 ID の SQL プランをダウンロードして分析する必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="297">
          <source>After the best plan is determined, this script can be used to force that plan to be used, regardless of parameters.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">最適なプランが決定されたら、パラメーターに関係なく、そのプランの使用を強制するためにこのスクリプトを使用できます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="298">
          <source>Parameters</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">パラメーター</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="299">
          <source>The force<ph id="ph1">\_</ph>plan<ph id="ph2">\_</ph>id parameter is the ID of the plan that should be used going forward.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">force<ph id="ph1">\_</ph>plan<ph id="ph2">\_</ph>id パラメーターは、今後使用するプランの ID です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="300">
          <source>This can be found from the query to get all plan IDs for a given query.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">これは、特定のクエリのすべてのプラン ID を取得するクエリから見つかります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="301">
          <source>Be sure to validate that the XML of the plan is a good plan before forcing, because forcing a bad plan can have negative effects.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">強制するために、プランの XML が適切なプランであることを検証してください。不適切なプランを強制すると負の効果があるためです。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="302">
          <source>The name parameter is any unique string not currently used by an existing plan guide.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">名前パラメーターは、既存のプラン ガイドによって現在使用されていない一意の文字列です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="303">
          <source>The statement parameter is the SQL statement that should be forced.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ステートメント パラメーターは、強制する SQL ステートメントです。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="304">
          <source>This can be obtained from many other queries, including currently running queries and most expensive queries.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">これは、他の多くのクエリ (現在実行中のクエリと最も高価なクエリを含む) から入手できます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="305">
          <source>Ensure that this is copied precisely, including whitespace, because differences in whitespace will cause the plan guide not to work.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">これが正確にコピーされるようにしてください (空白など)。空白に違いが発生すると、プラン ガイドが機能しないためです。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="306">
          <source>Also, do not include the parameters for the query in this text, because they are specified separately.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">さらに、このテキストにクエリのパラメーターを含めないでください。別個に指定されるためです。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="307">
          <source>For instance, on a select query, the first characters of the statement should always be <ph id="ph1">&amp;quot;</ph>SELECT<ph id="ph2">&amp;quot;</ph>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">たとえば、選択クエリでは、ステートメントの最初の文字は必ず <ph id="ph1">&amp;quot;</ph>SELECT<ph id="ph2">&amp;quot;</ph> にしてください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="308">
          <source>The params parameter is the set of @P1, @P2, and so on, parameters for the query.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">params パラメーターは、一連の @P1、@P2 などのようなクエリのパラメーターです。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="309">
          <source>These can be obtained from other queries, including currently running queries and most expensive queries.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">これらは、他のクエリ (現在実行中のクエリと最も高価なクエリを含む) から入手できます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="310">
          <source>When pasting in the parameters, remove the outer parenthesis.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">パラメーターに貼り付ける場合、外部かっこを削除します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="311">
          <source>For instance, paste in <ph id="ph1">&amp;quot;</ph>@P1 int,@P2 nvarchar(21)<ph id="ph2">&amp;quot;</ph>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">たとえば、<ph id="ph1">&amp;quot;</ph>@P1 int、@P2 nvarchar(21)<ph id="ph2">&amp;quot;</ph> に貼り付けます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="312">
          <source>If there are no parameters for the query, leave this value blank.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">クエリのパラメーターがない場合、この値を空白のままにします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="313">
          <source>Create a plan guide to add table hints</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">テーブル ヒントを追加するプラン ガイドの作成</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="314">
          <source>Description</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">説明</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="315">
          <source>SQL will recompute a new plan each time the plan cache is flushed, such as when an update of statistics runs.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">SQL では、統計の更新が実行されたときなど、プラン キャッシュがフラッシュされるたびに、新しいプランを再計算します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="316">
          <source>The plan that is chosen is based on <ph id="ph1">&amp;quot;</ph>sniffing<ph id="ph2">&amp;quot;</ph> the parameters of the first execution of that query.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">選択されているプランは、そのクエリの最初の実行のパラメーターの <ph id="ph1">&amp;quot;</ph>スニッフィング<ph id="ph2">&amp;quot;</ph> に基づきます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="317">
          <source>After that, the same plan will be used, regardless of parameters.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">その後、パラメータに関係なく同じプランが使用されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="318">
          <source>For this reason, the same query might sometimes get multiple plans, some of which are far worse than others for given data distributions.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このため、同じクエリが複数のプランを取得する場合があります。その一部は、特定のデータ配分のプランよりかなり悪くなります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="319">
          <source>This action can be used to add specific hints to the query.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このアクションは、特定のヒントをクエリに追加するために使用できます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="320">
          <source>This is different than forcing a plan guide, because SQL will still perform parameter sniffing and occasionally select different plans.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">これは、プラン ガイドの強制とは異なります。SQL は引き続きパラメーター スニッフィングを実行し、場合によってはさまざまなプランを選択するためです。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="321">
          <source>However, the query hints will be applied in those plan computations.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ただし、クエリ ヒントはそのプランの計算に適用されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="322">
          <source>Note that this action applies only to the database that it is executed on.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このアクションは、実行されるデータベースにのみ適用されることに注意してください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="323">
          <source>Therefore, it should be used as a last resort, after the addition of indexes, hints, or code changes that will flow between development and production environments.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">したがって、開発環境と製造環境間を流れるインデックス、ヒント、またはコード変更の追加後に、最後の手段として使用する必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="324">
          <source>Next steps</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">次のステップ</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="325">
          <source>Usually, query hints are determined after looking through multiple different query plans for a given query.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">通常、特定のクエリの複数の異なるクエリ プランを検索した後クエリ ヒントが決まります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="326">
          <source>For example, if an index seek on a table always outperforms a scan, it might be beneficial to add a FORCESEEK hint.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">たとえば、テーブル上のインデックス シークのパフォーマンスが常にスキャンより高い場合、FORCESEEK ヒントを追加すると便利な場合があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="327">
          <source>After hints have been determined and tested locally, use this action to install a plan guide that will add those query hints to future executions of the query.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ヒントが決定され、ローカルでテストされたら、それらのクエリ ヒントをクエリの将来の実行に追加するプラン ガイドをインストールするためにこのアクションを使用します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="328">
          <source>Parameters</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">パラメーター</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="329">
          <source>The name parameter is any unique string not currently used by an existing plan guide.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">名前パラメーターは、既存のプラン ガイドによって現在使用されていない一意の文字列です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="330">
          <source>The statement parameter is the SQL statement that should be forced.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ステートメント パラメーターは、強制する SQL ステートメントです。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="331">
          <source>This can be obtained from many other queries, including currently running queries and most expensive queries.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">これは、他の多くのクエリ (現在実行中のクエリと最も高価なクエリを含む) から入手できます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="332">
          <source>Ensure that this is copied precisely, including whitespace, because differences in whitespace will cause the plan guide not to work.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">これが正確にコピーされるようにしてください (空白など)。空白に違いが発生すると、プラン ガイドが機能しないためです。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="333">
          <source>Also, do not include the parameters for the query in this text, because they are specified separately.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">さらに、このテキストにクエリのパラメーターを含めないでください。別個に指定されるためです。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="334">
          <source>For instance, on a select query the first characters of the statement should always be <ph id="ph1">&amp;quot;</ph>SELECT<ph id="ph2">&amp;quot;</ph>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">たとえば、選択クエリでは、ステートメントの最初の文字は必ず <ph id="ph1">&amp;quot;</ph>SELECT<ph id="ph2">&amp;quot;</ph> にしてください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="335">
          <source>The params parameter is the set of @P1, @P2, and so on, parameters for the query.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">params パラメーターは、一連の @P1、@P2 などのようなクエリのパラメーターです。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="336">
          <source>These can be obtained from other queries, including currently running queries and most expensive queries.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">これらは、他のクエリ (現在実行中のクエリと最も高価なクエリを含む) から入手できます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="337">
          <source>When pasting in the parameters, remove the outer parenthesis.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">パラメーターに貼り付ける場合、外部かっこを削除します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="338">
          <source>For instance, paste in <ph id="ph1">&amp;quot;</ph>@P1 int,@P2 nvarchar(21)<ph id="ph2">&amp;quot;</ph>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">たとえば、<ph id="ph1">&amp;quot;</ph>@P1 int、@P2 nvarchar(21)<ph id="ph2">&amp;quot;</ph> に貼り付けます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="339">
          <source>If there are no parameters for the query, leave this value blank.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">クエリのパラメーターがない場合、この値を空白のままにします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="340">
          <source>The hints to apply can be tested locally by just manually adding them to the end of a query.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">適用するヒントは、クエリの末尾に手動で追加することでローカルでテストできます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="341">
          <source>If table aliases are used, they should match the table aliases in the statement text.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">テーブル エイリアスを使用している場合、ステートメント テキストのテーブル エイリアスと一致する必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="342">
          <source>Drop index</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">インデックスの削除</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="343">
          <source>Background</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">バックグラウンド</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="344">
          <source>Usually, extra indexes on a table only add minor incremental costs.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">通常、テーブルに余分なインデックスがあっても、コストが少し増加するだけです。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="345">
          <source>But in some situations, such as high-throughput tables, the existence of an extra index can cause large performance degradation.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">しかし、場合によっては (高スループット テーブルなど)、余分なインデックスの存在により大規模なパフォーマンス低下が生じることがあります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="346">
          <source>The correct way to remove indexes is to remove them from metadata.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">インデックスを削除する適切な方法は、メタデータから削除する方法です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="347">
          <source>But if they need to be removed more aggressively to mitigate an ongoing issue, this action can be used.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">しかし、継続的な問題を軽減するために積極的に削除する必要がある場合、このアクションを使用できます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="348">
          <source>Next steps</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">次のステップ</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="349">
          <source>From the query to list all indexes for a table, determine the index name to drop.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">テーブルのすべてのインデックスを一覧表示するクエリから、削除するインデックス名を決定します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="350">
          <source>Verify that no other workloads will be negatively affected by removing this index.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このインデックスの削除により悪影響を受ける他のワークロードがないことを確認します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="351">
          <source>This is a dangerous operation to perform and might cause other workloads to regress.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この操作を実行するのは危険であり、他のワークロードが回帰する可能性があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="352">
          <source>Provide the table and the index name to drop.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">削除するテーブルとインデックスの名前を提供します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="353">
          <source>Apply the same change in other environments, such as DEV and Sandbox, ideally by removing the index in metadata to keep all environments in sync.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">原則的には、すべての環境を同期するメタデータのインデックスを削除することで、開発およびサンドボックスなどの他の環境で同じ変更を適用します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="354">
          <source>End SQL process</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">SQL プロセスの終了</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="355">
          <source>Background</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">バックグラウンド</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="356">
          <source>If a SPID is consuming too many resources and degrading the operation of other processes, it might be beneficial to end the SPID process.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">SPID が非常に多くのリソースを消費して、他のプロセスの工程が低下している場合、は、SPID プロセスを終了すると便利な場合があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="357">
          <source>This will cause the open transaction to roll back, meaning that data should not be lost, but the process might need to be manually restarted.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">これにより、未処理トランザクションがロールバックします。つまり、データは失われませんが、プロセスの手動での再起動が必要になることがあります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="358">
          <source>Note that rollback can also take a long time and consume a lot of resources if the transaction has already performed a lot of work.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">トランザクションが既に多くの作業を実行している場合、ロールバックに時間がかかり、多くのリソースを消費する可能性があることに注意してください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="359">
          <source>Therefore, this action should be used with caution.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">したがって、このアクションは注意して使用する必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="360">
          <source>Next steps</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">次のステップ</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="361">
          <source>From the blocking tree and other queries, determine which SPID should end.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ブロック ツリーやその他のクエリから、SPID が終了するかどうかを判断する必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="362">
          <source>Verify that the processing that is being performed by the SPID can end without causing harm to ongoing business operations.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">継続的な事業運営に悪影響を与えずに、SPID により実行されている処理が終了できることを確認します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="363">
          <source>Provide the SPID number to end, and roll back that operation.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">終了する SPID 番号を指定し、その操作をロールバックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="364">
          <source>Disable/enable page locks and lock escalation</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ページ ロックおよびロック エスカレーションの無効化/有効化</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="365">
          <source>Background</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">バックグラウンド</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="366">
          <source>In many situations, SQL will either take page locks (locking a full page at a time) or escalate to entire table locks (locking the whole table).</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">多くの場合、SQL はページ ロック (ページ全体を一度にロック) を取得するか、テーブル ロック全体 (テーブル全体のロック) にエスカレートします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="367">
          <source>This enables SQL to perform actions that edit a high volume of rows more efficiently.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">これにより、SQL は大量の行を効率的に編集するアクションを実行できます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="368">
          <source>However, this can cause problems and unnecessary contention in certain workloads.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ただし、これにより、特定のワークロードで問題および不要な競合が発生することがあります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="369">
          <source>Consider two large posting jobs, each running for 10 minutes and editing different rows of data that happen to reside on the same physical data page.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">2 つの大きな転記ジョブ (それぞれ 10 分を実行されており、偶然同じ物理データ ページに配置されているにさまざまなデータ行を編集している) について考えます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="370">
          <source>This might cause the two postings to serialize and to take 20 minutes because of the contention.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">これにより、2 つの転記がシリアル化され、競合が原因で 20 分かかる可能性があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="371">
          <source>This query can be used to disable lock escalation and page locks for a given table.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このクエリは、特定のテーブルのロック エスカレーションやページ ロックの無効化に使用できます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="372">
          <source>It should be used cautiously, however, because there are valid reasons for SQL to use page locks and lock escalation.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ただし、SQL がページ ロックとロック エスカレーションを使用する有効な理由があるため、慎重に使用してください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="373">
          <source>Next steps</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">次のステップ</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="374">
          <source>After determining that unnecessary contention is being experienced on a given table because of lock escalation or page locks, use this query to disable those options.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ロック エスカレーションまたはページ ロックが原因で不要な競合が特定のテーブルで発生していることを確認したら、これらのオプションを無効にするためにこのクエリを使用します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="375">
          <source>Parameters</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">パラメーター</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="376">
          <source>The table name is the physical name of the table.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">テーブル名は、テーブルの物理名です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="377">
          <source>The value of the lock escalation and page locks is either <ph id="ph1">&amp;quot;</ph>ON<ph id="ph2">&amp;quot;</ph> or <ph id="ph3">&amp;quot;</ph>OFF<ph id="ph4">&amp;quot;</ph>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ロック エスカレーションおよびページ ロックの値は、<ph id="ph1">&amp;quot;</ph>ON<ph id="ph2">&amp;quot;</ph> または <ph id="ph3">&amp;quot;</ph>OFF<ph id="ph4">&amp;quot;</ph> です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="378">
          <source>Rebuild index</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">インデックスの再構築</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="379">
          <source>Background</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">バックグラウンド</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="380">
          <source>Over time, as processes edit existing records and write new records into tables, indexes might become fragmented.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">時間の経過と共に、プロセスは既存のレコードを編集し、テーブルに新しいレコードを作成するため、インデックスが断片化する可能性があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="381">
          <source>This increases the amount of I/O necessary to process the same number of records, and might cause performance degradation.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">これにより、同じ数のレコードの処理に必要な入出力の数が増え、パフォーマンスが低下が発生する可能性があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="382">
          <source>This operation will rebuild indexes to reduce page fragmentation.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この操作は、ページの断片化を減らすためにインデックスを再構築します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="383">
          <source>This is an expensive operation and has been known to cause contention while running.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">これはコストの高い操作であり、実行中に競合が発生させることがわかっています。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="384">
          <source>Therefore, the environment should be monitored while this operation is running.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">したがって、この操作の実行中は、環境を監視してください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="385">
          <source>Next steps</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">次のステップ</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="386">
          <source>Monitor blocking and DTU in the system while this operation is running.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この操作の実行中、システムでブロックと DTU を監視します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="387">
          <source>If the system degrades unacceptably, consider ending this operation.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">システムのパフォーマンスが許容できないほど低下する場合、この操作を終了することを検討します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="388">
          <source>Remove plan guide</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">プラン ガイドの削除</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="389">
          <source>Background</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">バックグラウンド</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="390">
          <source>If plan guides have been installed and are having a negative impact, or if they just are not working, it might be necessary to remove a plan guide.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">プラン ガイドがインストールされていて、悪影響を与えている、または単に動作していない場合、場合によってはプラン ガイドを削除する必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="391">
          <source>This query enables removal of an existing plan guide.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このクエリにより、既存のプラン ガイドの削除が可能になります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="392">
          <source>Note that removing a plan guide will not affect any currently running queries until the next time they are executed.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">プラン ガイドの削除が、現在実行中のクエリが次に実行されるまでそのクエリに影響を与えないことを確認します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="393">
          <source>Next steps</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">次のステップ</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="394">
          <source>After determining which plan guide should be removed, specify the name of the plan.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">どのプラン ガイドを削除するかを決定したら、プランの名前を指定します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="395">
          <source>Parameters</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">パラメーター</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="396">
          <source>The list of existing plan guides and associated names can be found from the list of current plan guides query.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">既存のプラン ガイドおよび関連付けられている名前のリストは、現在のプラン ガイド クエリの一覧から見つけることができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="397">
          <source>Update statistics on table</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">テーブルでの統計の更新</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="398">
          <source>Background</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">バックグラウンド</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="399">
          <source>Updates statistics on the specified table.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">指定されたテーブルでの統計の更新</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="400">
          <source>Occasionally, statistics can be found to be out of date and to be causing query plan issues, such as after an import process that has skewed the statistics of the table.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">インポート プロセスによってテーブルの統計が改変された後など、場合によっては、統計が古く、クエリ プランの問題の原因となっていることがわかります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="401">
          <source>Note that this action will have a significant performance overhead while running and has also been known to cause blocking on queries that use the same table.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このアクションは実行中に大きなパフォーマンス オーバーヘッドを与え、同じテーブルを使用するクエリでブロックの原因となることも知られていることに注意してください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="402">
          <source>Therefore, it should be used sparingly and monitored while running to ensure that the system does not degrade.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">したがって、システムのパフォーマンスが低下しないようにするため、控えめに使用し、実行中は監視してください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="403">
          <source>Next steps</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">次のステップ</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="404">
          <source>While running this query, monitor both current blocking and current DTU to ensure that system performance does not degrade unacceptably.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このクエリの実行中、システムのパフォーマンスが許容できないほど低下しないように、現在のブロックと現在の DTU の両方を監視します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="405">
          <source>If it does, consider ending the update statistics command.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">低下した場合、更新統計コマンドの終了を検討してください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="406">
          <source>Parameters</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">パラメーター</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="407">
          <source>The table name parameter is the physical name of the table to update statistics for.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">テーブル名パラメーターは、統計情報を更新するテーブルの物理的な名前です。</target></trans-unit>
      </group>
    </body>
  </file>
</xliff>