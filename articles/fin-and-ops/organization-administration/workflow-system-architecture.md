<?xml version="1.0" encoding="UTF-8"?>
<xliff xmlns:logoport="urn:logoport:xliffeditor:xliff-extras:1.0" xmlns:tilt="urn:logoport:xliffeditor:tilt-non-translatables:1.0" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns="urn:oasis:names:tc:xliff:document:1.2" xmlns:xliffext="urn:microsoft:content:schema:xliffextensions" version="1.2" xsi:schemaLocation="urn:oasis:names:tc:xliff:document:1.2 xliff-core-1.2-transitional.xsd">
  <file datatype="xml" source-language="en-US" original="workflow-system-architecture.md" target-language="ja-JP">
    <header>
      <tool tool-company="Microsoft" tool-version="1.0-7889195" tool-name="mdxliff" tool-id="mdxliff"/>
      <xliffext:skl_file_name>workflow-system-architecture.dad830.f8c1bb3937620ce9e71f9555067c12183b7606c4.skl</xliffext:skl_file_name>
      <xliffext:version>1.2</xliffext:version>
      <xliffext:ms.openlocfilehash>f8c1bb3937620ce9e71f9555067c12183b7606c4</xliffext:ms.openlocfilehash>
      <xliffext:ms.sourcegitcommit>9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b</xliffext:ms.sourcegitcommit>
      <xliffext:ms.lasthandoff>05/15/2019</xliffext:ms.lasthandoff>
      <xliffext:ms.openlocfilepath>articles\fin-and-ops\organization-administration\workflow-system-architecture.md</xliffext:ms.openlocfilepath>
    </header>
    <body>
      <group extype="content" id="content">
        <trans-unit xml:space="preserve" translate="yes" id="101" restype="x-metadata">
          <source>Workflow system architecture</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ワークフロー システムのアーキテクチャ</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="102" restype="x-metadata">
          <source>This article describes the architecture of the workflow system in Microsoft Dynamics 365 for Finance and Operations.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この記事では、Microsoft Dynamics 365 for Finance and Operations のワークフロー システムのアーキテクチャについて説明します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="103">
          <source>Workflow system architecture</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ワークフロー システムのアーキテクチャ</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="104">
          <source>This article describes the architecture of the workflow system in Microsoft Dynamics 365 for Finance and Operations.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この記事では、Microsoft Dynamics 365 for Finance and Operations のワークフロー システムのアーキテクチャについて説明します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="105">
          <source>The workflow infrastructure consists of two components that are hosted on Application Object Server (AOS): the X++ workflow runtime and the managed workflow runtime.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ワークフロー インフラストラクチャは、Application Object Server (AOS) でホストされる 2 つのコンポーネント (X++ ワークフロー ランタイムおよび管理ワークフロー ランタイム) から構成されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="106">
          <source>The X++ workflow runtime consists of the following components:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">X++ ワークフロー ランタイムは、次のコンポーネントで構成されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="107">
          <source>Workflow runtime application programming interface (API)</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ワークフロー ランタイム アプリケーション プログラミング インターフェイス (API)</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="108">
          <source>A messaging batch job</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">メッセージング バッチ ジョブ</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="109">
          <source>A message queue</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">メッセージ キュー</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="110">
          <source>Either the messaging batch job or the workflow runtime API can invoke the application code, if it's required.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">必要に応じて、メッセージング バッチ ジョブまたはワークフロー ランタイム API のいずれかがアプリケーション コードを呼び出すことができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="111">
          <source>The X++ workflow runtime is compiled into the Common Intermediate Language (CIL) of the Microsoft .NET Framework.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">X++ ワークフロー ランタイムは、Microsoft .NET フレームワークの CIL (共通中間言語) にコンパイルされます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="112">
          <source>The managed workflow runtime consists of the Windows Workflow Foundation and Finance and Operations extensions.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">管理ワークフロー ランタイムは、Windows Workflow Foundation および Finance and Operations の拡張機能で構成されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="113">
          <source>Logically, the workflow infrastructure is an extension of Finance and Operations and is transparent to users.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">論理的には、ワークフロー インフラストラクチャは Finance and Operations の拡張で、ユーザーにとって透過的です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="114">
          <source>Physically, both the X++ workflow and the managed workflow runtimes are hosted on AOS.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">物理的には、X++ ワークフローおよび管理ワークフローのランタイムは両方とも AOS でホストされます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="115">
          <source>The workflow infrastructure uses batch processing on AOS and .NET Interop to integrate both subsystems, and to pass messages from one subsystem to the other.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ワークフロー インフラストラクチャは AOS と .NET Interop でバッチ処理を使用して、その 2 つのサブシステムを統合し、片方のサブシステムからもう一方のサブシステムにメッセージを渡します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="116">
          <source>The X++ code that is run in the batch processor is compiled to .NET CIL.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">バッチ プロセッサで実行される X++ コードは、.NET CIL にコンパイルされます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="117">
          <source>The batch processing runs in the .NET common language runtime (CLR).</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">バッチ処理は、.NET 共通言語ランタイム (CLR) で実行されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="118">
          <source>The following figure shows the high-level architecture of the workflow infrastructure.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">次の図に、ワークフロー インフラストラクチャの高レベル アーキテクチャの概要を示します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="119">
          <source><bpt id="p1">[</bpt><ph id="ph1">![</ph>workflow<ph id="ph2">\_</ph>architecturediagram2016<ept id="p1">](./media/workflow_architecturediagram2016.png)](./media/workflow_architecturediagram2016.png)</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">[</bpt><ph id="ph1">![</ph>ワークフロー<ph id="ph2">\_</ph>architecturediagram2016<ept id="p1">](./media/workflow_architecturediagram2016.png)](./media/workflow_architecturediagram2016.png)</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="120">
          <source>Users can use the workflow pages and controls in Finance and Operations to participate in business processes.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ユーザーは、 Finance and Operations で、ワークフローのページとコントロールを使用して、業務プロセスに参加できます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="121">
          <source>Developers can create workflows for objects that they have added to Finance and Operations.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">開発者は、Finance and Operations に追加済のオブジェクトのワークフローを作成できます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="122">
          <source>The following table describes the workflow steps that occur when a user submits an expense report to the workflow system for approval.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">次の表は、ユーザーが経費精算書を承認のためにワークフロー システムに提出したときに発生するワークフロー ステップを示します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="123">
          <source>Step</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ステップ</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="124">
          <source>Runtime</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ランタイム</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="125">
          <source>Activity</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">活動</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="126">
          <source>1</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">1</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="127">
          <source>X++ workflow runtime</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">X++ ワークフロー ランタイム</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="128">
          <source>A user submits an expense report by clicking the <bpt id="p1">**</bpt>Submit<ept id="p1">**</ept> button on one of the workflow controls.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ユーザーは、ワークフローのいずれかの制御で <bpt id="p1">**</bpt>送信<ept id="p1">**</ept> をクリックして、経費精算書を送信します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="129">
          <source>This action causes X++ code to activate a workflow instance by calling the workflow runtime API.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このアクションにより、X++ コードはワークフロー ランタイム API を呼び出し、ワークフロー インスタンスが有効になります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="130">
          <source>The workflow runtime API posts a message to the message queue.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ワークフロー ランタイム API は、メッセージをメッセージ キューに書き込みます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="131">
          <source>The messaging batch job reads the message and sends a workflow activation request to the managed workflow runtime.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">メッセージング バッチ ジョブは、メッセージを読み取り、ワークフローのアクティブ化要求を管理ワークフロー ランタイムに送信します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="132">
          <source>The messaging batch job processes the message queue at one-minute intervals.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">メッセージング バッチ ジョブは 1 分間隔でメッセージ キューを処理します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="133">
          <source>2</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">2</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="134">
          <source>Managed workflow runtime</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">管理されるワークフロー ランタイム</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="135">
          <source>.NET Interop from X++ receives the message and starts a new workflow instance via Windows Workflow Foundation.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">X++ からの .NET Interop は、メッセージを受け取り、新しいワークフロー インスタンスを Windows Workflow Foundation 経由で開始します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="136">
          <source>This workflow instance performs a callback to the X++ workflow runtime API via .NET Interop to X++ CIL and posts a message that the workflow has started.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このワークフロー インスタンスは、X++ への.NET Interop CIL 経由でX++ ワークフロー ランタイム API のコールバックを実行し、ワークフローが起動されたことを示すメッセージを書き込みます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="137">
          <source>After the message is posted, the managed workflow runtime saves the idle workflow instance to the Finance and Operations database.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">メッセージが転記された後、管理されたワークフロー ランタイムはアイドル状態のワークフロー インスタンスを Finance and Operations データベースに保存します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="138">
          <source>The runtime then removes the workflow instance from memory.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">その後、ランタイムはメモリからワークフロー インスタンスを削除します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="139">
          <source>When the managed workflow runtime receives another message from the X++ workflow runtime for this workflow instance, it restores the workflow instance to memory and resumes it.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">管理ワークフロー ランタイムが、このワークフロー インスタンスに対する別のメッセージを X++ ワークフロー ランタイムから受け取ると、ワークフロー インスタンスはメモリーに復元され、再開されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="140">
          <source>Each workflow instance is unique.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">各ワークフロー インスタンスは固有です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="141">
          <source>If two users submit their expense reports for approval, two workflow instances are started.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">2 人のユーザーが承認のために経費精算書を提出すると、2 つのワークフロー インスタンスが開始されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="142">
          <source>3</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">3</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="143">
          <source>X++ workflow runtime</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">X++ ワークフロー ランタイム</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="144">
          <source>The messaging batch job reads the <bpt id="p1">**</bpt>workflow started<ept id="p1">**</ept> message from the message queue and invokes the application event handler to process a <bpt id="p2">**</bpt>workflow started<ept id="p2">**</ept> event.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">メッセージング バッチ ジョブが、<bpt id="p1">**</bpt>ワークフローで開始された<ept id="p1">**</ept>メッセージをメッセージ キューから読み取り、<bpt id="p2">**</bpt>ワークフローで開始された<ept id="p2">**</ept>イベントを処理するアプリケーション イベント ハンドラーを開始します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="145">
          <source>The batch job then posts an acknowledgment message that the event was processed.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">次に、バッチ ジョブは、イベントが処理されたことを示す確認メッセージを書き込みます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="146">
          <source>4</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">4</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="147">
          <source>Both</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">両方</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="148">
          <source>This same messaging pattern is repeated, as required, throughout the lifecycle of the workflow instance.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この同じメッセージング パターンが、ワークフロー インスタンスのライフサイクル全体で必要に応じて繰り返されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="149">
          <source>The workflow architecture helps provide a reliable and durable messaging system, and also helps guarantee that the state of the workflow is always synchronized with the state of the application.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このワークフロー アーキテクチャは、信頼できる堅牢なメッセージ システムを提供し、また、ワークフローの状態とアプリケーションの状態を常に同期させるために役立ちます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="150">
          <source>If an unexpected hardware or software failure occurs, the workflow instance state is returned to its last known saved point, and the message stays in the queue.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ハードウェアやソフトウェアに予期しない障害が発生すると、ワークフロー インスタンスの状態は最後に保存された既知の点まで戻され、メッセージはキュー内に保持されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="151">
          <source>Therefore, from an architecture perspective, the recovery model is to fix the problem and resume the workflow.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">したがって、アーキテクチャから見ると、復旧モデルは、問題の解決とワークフローの再開です。</target></trans-unit>
      </group>
    </body>
  </file>
</xliff>