<?xml version="1.0" encoding="UTF-8"?>
<xliff xmlns:logoport="urn:logoport:xliffeditor:xliff-extras:1.0" xmlns:tilt="urn:logoport:xliffeditor:tilt-non-translatables:1.0" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns="urn:oasis:names:tc:xliff:document:1.2" xmlns:xliffext="urn:microsoft:content:schema:xliffextensions" version="1.2" xsi:schemaLocation="urn:oasis:names:tc:xliff:document:1.2 xliff-core-1.2-transitional.xsd">
  <file datatype="xml" source-language="en-US" original="batch-server-overview.md" target-language="ja-JP">
    <header>
      <tool tool-company="Microsoft" tool-version="1.0-7889195" tool-name="mdxliff" tool-id="mdxliff"/>
      <xliffext:skl_file_name>batch-server-overview.0b989b.d758321f7a79e1d12363bd58a7477ec0d86a4dfe.skl</xliffext:skl_file_name>
      <xliffext:version>1.2</xliffext:version>
      <xliffext:ms.openlocfilehash>d758321f7a79e1d12363bd58a7477ec0d86a4dfe</xliffext:ms.openlocfilehash>
      <xliffext:ms.sourcegitcommit>9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b</xliffext:ms.sourcegitcommit>
      <xliffext:ms.lasthandoff>05/15/2019</xliffext:ms.lasthandoff>
      <xliffext:ms.openlocfilepath>articles\dev-itpro\sysadmin\batch-server-overview.md</xliffext:ms.openlocfilepath>
    </header>
    <body>
      <group extype="content" id="content">
        <trans-unit xml:space="preserve" translate="yes" id="101" restype="x-metadata">
          <source>Batch processing and batch servers</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">バッチ処理とバッチ サーバー</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="102" restype="x-metadata">
          <source>This article describes batch processing and batch servers, and how to plan for their use.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この記事では、バッチ処理とバッチ サーバー、およびその使用を計画する方法について説明します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="103">
          <source>Batch processing and batch servers</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">バッチ処理とバッチ サーバー</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="104">
          <source>This article describes batch processing and batch servers, and how to plan for their use.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この記事では、バッチ処理とバッチ サーバー、およびその使用を計画する方法について説明します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="105">
          <source>The batch framework provides an asynchronous, server-based batch processing environment that can process tasks across multiple instances of Application Object Server (AOS).</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">バッチ フレームワークは、Application Object Server (AOS) の複数のインスタンスにわたるタスクを処理できるサーバー ベースの非同期バッチ処理環境を提供します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="106">
          <source>You should become familiar with the following aspects of the batch framework:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">バッチ フレームワークの次のような側面について、よく理解しておく必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="107">
          <source>A <bpt id="p1">**</bpt>batch job<ept id="p1">**</ept> is a process that is used to achieve a specific goal.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>バッチ ジョブ<ept id="p1">**</ept>は、特定の目標を達成するために使用されるプロセスです。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="108">
          <source>A batch job consists of one or more batch tasks.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">バッチ ジョブは、1 つまたは複数のバッチ タスクで構成されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="109">
          <source>A <bpt id="p1">**</bpt>batch task<ept id="p1">**</ept> is an activity that is run by a batch job.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>バッチ タスク<ept id="p1">**</ept>は、バッチ ジョブによって実行される活動です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="110">
          <source>You can add batch tasks that have multiple types of dependencies to a batch job.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">複数の種類の依存関係を持つバッチ タスクをバッチ ジョブに追加することができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="111">
          <source>You can also configure AOS instances to run multiple threads, each of which runs a task.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">また、それぞれがタスクを実行する、複数のスレッドを実行するように AOS インスタンスを構成することができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="112">
          <source>All batch tasks that are waiting to be run can be run by any available AOS instance that is configured as a batch server.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">実行を待機しているすべてのバッチ タスクはバッチ サーバーとしてコンフィギュレーションされている使用可能なすべての AOS インスタンスによって実行できます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="113">
          <source>To improve throughput and reduce overall execution time, you can define a batch job as many tasks and then use a batch server to run the tasks against all available AOS instances.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">スループットを向上させ、全体の実行時間を短縮するには、バッチ ジョブを多数のタスクとして定義し、バッチ サーバーを使用して使用可能なすべての AOS インスタンスに対してタスクを実行します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="114">
          <source>A <bpt id="p1">**</bpt>batch group<ept id="p1">**</ept> is an attribute of a batch task.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>バッチ グループ<ept id="p1">**</ept>は、バッチ タスクの属性です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="115">
          <source>A batch group lets the administrator determine or specify which AOS instance runs the task.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">バッチ グループは、管理者がタスクを実行する AOS インスタンスを決定または指定することを可能にします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="116">
          <source>When you create a new task, it's put in the default batch group.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">新しいタスクを作成するとき、そのタスクは既定のバッチ グループに配置されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="117">
          <source>All batch servers are configured to process the default batch group and the waiting tasks from any job.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">すべてのバッチ サーバーは、任意のジョブから既定のバッチ グループおよび待機中のタスクをプロセスするためにコンフィギュレーションされています。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="118">
          <source>Additionally, you can create a named batch group, and then set an affinity between that batch group and specific AOS instances.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">また、名前付きバッチ グループを作成して、そのバッチ グループと特定の AOS インスタンスの間のアフィニティを設定できます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="119">
          <source>After you create this affinity, only the specified AOS instances will process tasks from the named batch group, and those AOS instances will process tasks from the named batch group only.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">アフィニティを作成した後は、指定された AOS インスタンスのみが名前付きバッチ グループのタスクを処理することができ、 AOS インスタンスは指定された名前付きバッチ グループからのみタスクを処理することができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="120">
          <source>You can also add the default batch group to the configured servers, if that batch group is required.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">また、バッチ グループが必要な場合、既定のバッチ グループを構成済みサーバーに追加することができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="121">
          <source>Batch server topology planning</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">バッチ サーバーのトポロジ計画</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="122">
          <source>The capacity of a batch server is based on the maximum number of threads that can run concurrently on the AOS instance.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">バッチ サーバーの能力は、AOS インスタンスで同時に実行できるスレッドの最大数に基づいています。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="123">
          <source>Each thread runs one batch task.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">各スレッドは、1 つのバッチ タスクを実行します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="124">
          <source>You can add complex dependencies between or among tasks.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">タスク間またはタスク内に複雑な依存関係を追加することができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="125">
          <source>You can run these tasks in serial steps or parallel steps, depending on the business logic and requirements.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">これらのタスクは、ビジネス ロジックおよび要件に基づき、シリアル ステップまたはパラレル ステップで実行することができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="126">
          <source>All tasks that don't have any dependencies are considered parallel tasks.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">依存関係を持っていないすべてのタスクは並列タスクと見なされます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="127">
          <source>AOS instances that are configured as batch servers periodically check for tasks that are waiting to be processed.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">バッチ サーバーとしてコンフィギュレーションされている AOS インスタンスは、処理を待機しているタスクを定期的に確認します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="128">
          <source>The batch server assigns each parallel task to a thread and starts to process the thread.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">バッチ サーバーは、各並列タスクをスレッドに割り当て、そのスレッドの処理を開始します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="129">
          <source>You can run multiple threads across multiple AOS instances.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">複数の AOS インスタンス間で複数のスレッドを実行することができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="130">
          <source>Each AOS instance automatically runs multiple threads, depending on that capacity that is defined in the configuration settings.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">各 AOS インスタンスは、構成設定で定義されているキャパシティに応じて、複数のスレッドを自動的に実行します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="131">
          <source>Therefore, parallel tasks from a job can be run on multiple threads across multiple AOS instances.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">したがって、ジョブからの並列タスクは、複数の AOS インスタンスにわたって複数のスレッドで実行できます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="132">
          <source>A batch server checks for available threads one time per minute.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">バッチ サーバーは、1 分間に 1 回使用可能なスレッドをチェックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="133">
          <source>Therefore, you might have to wait for a minute before you see that a waiting task is picked up for processing by an available thread.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">したがって、待機中のタスクが使用可能なスレッドで処理されるのを確認するまで、少し待たなければならない場合があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="134">
          <source>Batch server management planning</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">バッチ サーバーの管理計画</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="135">
          <source>All batch servers can be managed from a single location.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">すべてのバッチ サーバーは単一の場所から管理することができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="136">
          <source>One typical use of batch servers is to load balance jobs across multiple servers.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">バッチ サーバーの 1 つの一般的な使用方法は、複数のサーバー間でジョブの負荷分散を行うことです。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="137">
          <source>You can set the number of threads that the batch server will process.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">バッチ サーバーが処理するスレッド数をセットすることができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="138">
          <source>Because batch servers are also active AOS instances that service requests from Microsoft Dynamics 365 for Finance and Operations clients and other associated components, you must carefully determine when an AOS instance should be available to process batches.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">バッチ サーバーは、Microsoft Dynamics 365 for Finance and Operations のクライアントおよびその他の関連付けられたコンポーネントからサービスが要求する有効な AOS インスタンスでもあるため、AOS インスタンスがバッチ処理に利用できるようにする場合は慎重に決定する必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="139">
          <source>Walkthroughs</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">チュートリアル</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="140">
          <source>The following walkthroughs describe how tasks are processed, and how batch groups can be used to associate batch jobs with batch servers.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">次のチュートリアルでは、タスクの処理方法と、バッチ グループを使用してバッチ ジョブをバッチ ・サーバーに関連付ける方法について説明します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="141">
          <source>Batch processing of dependent tasks</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">従属タスクのバッチ処理</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="142">
          <source>For this example, you've created a job that is called JOB 1.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この例では、ジョブ 1 と呼ばれるジョブを作成しました。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="143">
          <source>As the following diagram shows, the job has seven tasks: TASK 1, TASK 2, TASK 3, TASK 4, TASK 5, TASK 6, and TASK 7.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">次の図に示すように、職務には 7 つのタスクがあります。タスク 1、タスク 2、タスク 3、タスク 4、タスク 5、タスク 6、およびタスク 7 です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="144">
          <source>A job that has dependent tasks</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">依存タスクのジョブ</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="145">
          <source>The tasks have the following dependencies:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">タスクには次の依存関係があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="146">
          <source>TASK 1 is the first task.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">タスク 1 は、最初のタスクです。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="147">
          <source>TASK 2 runs when TASK 1 is completed (regardless of the success or failure of TASK 1).</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">タスク 2 は、タスク 1 が完了すると実行されます (タスク 1 が成功したか失敗したかに関係ありません)。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="148">
          <source>TASK 3 runs when TASK 2 is successful.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">タスク 3 は、タスク 2 が正常に行われた場合に実行されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="149">
          <source>TASK 4 runs when TASK 2 is successful.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">タスク 4 は、タスク 2 が正常に行われた場合に実行されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="150">
          <source>TASK 5 runs when TASK 2 fails.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">タスク 5 は、タスク 2 が失敗したときに実行されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="151">
          <source>TASK 6 runs when TASK 3 fails.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">タスク 6 は、タスク 3 が失敗したときに実行されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="152">
          <source>TASK 7 runs when both TASK 3 and TASK 4 are successful.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">タスク 7 は、タスク 3 とタスク 4 の両方が正常に行われたときに実行されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="153">
          <source>Two batch servers, Batch1 and Batch2, are configured.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">2 つのバッチ・サーバー、Batch1 と Batch2 が構成されています。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="154">
          <source>Each server has a capacity of one thread.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">各サーバーには、1 つのスレッドの容量があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="155">
          <source>Imagine that Batch1 checks for waiting tasks, assigns TASK 1 to its thread, and starts to run TASK 1.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Batch1 が待機中のタスクをチェックし、そのスレッドにタスク 1 を割り当て、タスク 1 の実行を開始するとします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="156">
          <source>Although Batch2 and its single thread are also available, TASK 2 continues to wait until TASK 1 is completed.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Batch2 とその単一スレッドも使用可能ですが、タスク 2 はタスク 1 が完了するまで待機し続けます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="157">
          <source>As soon as TASK 1 is completed, TASK 2 is ready to be run.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">タスク 1 が完了するとすぐに、タスク 2 は実行する準備ができています。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="158">
          <source>This time, imagine that Batch2 checks for waiting tasks, assigns TASK 2 to its thread, and starts to run TASK 2.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ここでは、Batch2 が待機中のタスクをチェックし、そのスレッドにタスク 2 を割り当て、タスク 2 の実行を開始するものとします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="159">
          <source>If TASK 2 is successful, TASK 3 and TASK 4 are ready to be run.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">タスク 2 が正常に行われた場合は、タスク 3 およびタスク 4 の実行準備が整います。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="160">
          <source>This time, imagine that Batch2 checks for waiting tasks, assigns TASK 3 to its thread, and starts to run TASK 3.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ここでは、Batch2 が待機中のタスクをチェックし、そのスレッドにタスク 3 を割り当て、タスク 3 の実行を開始するものとします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="161">
          <source>Batch1 also checks for waiting tasks, assigns TASK 4 to its thread, and starts to run TASK 4.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Batch1 も待機中のタスクをチェックし、そのスレッドにタスク 4 を割り当て、タスク 4 の実行を開始します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="162">
          <source>If TASK 3 and TASK 4 are successful, one of the batch servers runs TASK 7.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">タスク 3 とタスク 4 が成功した場合は、バッチ サーバーのいずれかがタスク 7 を実行します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="163">
          <source>If TASK 2 fails, one of the batch servers runs TASK 5.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">タスク 2 が失敗すると、バッチ サーバーのいずれかがタスク 5 を実行します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="164">
          <source>If TASK 3 fails, one of the available batch servers runs TASK 6.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">タスク 3 が失敗すると、利用可能なバッチ サーバーのいずれかがタスク 6 を実行します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="165">
          <source><bpt id="p1">**</bpt>Note:<ept id="p1">**</ept> For this walkthrough, we are using Batch1 and Batch2 to explain the concept.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>注記:<ept id="p1">**</ept> このチュートリアルでは、概念を説明するために Batch1 と Batch2 を使用します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="166">
          <source>Any batch server that has available threads will start to run a waiting task.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">使用可能なスレッドを持つすべてのバッチ サーバーは、待機中のタスクの実行を開始します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="167">
          <source>You must create a batch group to determine or specify which batch job runs on which server.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">サーバー上で実行するバッチ ジョブを決定または指定するには、バッチ グループを作成する必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="168">
          <source>Batch processing that uses batch groups</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">バッチ グループを使用するバッチ処理</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="169">
          <source>This example shows how batch jobs can be processed on specific batch servers.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この例は、特定のバッチ サーバーでバッチ ジョブを処理する方法を示しています。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="170">
          <source>You have three batch servers: AOS1, AOS2, and AOS3.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">次の 3 つのバッチ サーバー、AOS1、AOS2、および AOS3 があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="171">
          <source>By default, all the batch servers process tasks from all batch jobs, depending on the number of available threads.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">既定では、すべてのバッチ サーバーは使用可能なスレッドの数に応じて、すべてのバッチ ジョブのタスクを処理します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="172">
          <source>You create a named batch group, BG1, and configure it to run on AOS2 and AOS3.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">名前付きバッチ グループ、BG1 を作成し、AOS2 および AOS3 で実行するように構成します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="173">
          <source>Therefore, tasks from jobs in BG1 will run only on AOS2 or AOS3, depending on the number available threads.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">したがって、BG1 のジョブからのタスクは、使用可能なスレッドの数に応じて、AOS2 または AOS3 でのみ実行されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="174">
          <source>AOS1 won't process tasks from jobs in BG1.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">AOS1 は、BG1 のジョブのタスクを処理しません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="175">
          <source>Likewise, AOS2 and AOS3 will process tasks from BG1 only.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">同様に、AOS2 および AOS3 は BG1 からのみタスクを処理します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="176">
          <source>You can configure AOS2 and AOS3 to process tasks from other batch groups.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">AOS2 および AOS3 を構成して他のバッチ グループからタスクを処理することができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="177">
          <source>These batch groups include the default batch group.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">これらのバッチ グループには、既定のバッチ グループが含まれています。</target></trans-unit>
      </group>
    </body>
  </file>
</xliff>