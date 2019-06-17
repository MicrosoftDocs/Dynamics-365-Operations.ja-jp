<?xml version="1.0" encoding="UTF-8"?>
<xliff xmlns:logoport="urn:logoport:xliffeditor:xliff-extras:1.0" xmlns:tilt="urn:logoport:xliffeditor:tilt-non-translatables:1.0" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns="urn:oasis:names:tc:xliff:document:1.2" xmlns:xliffext="urn:microsoft:content:schema:xliffextensions" version="1.2" xsi:schemaLocation="urn:oasis:names:tc:xliff:document:1.2 xliff-core-1.2-transitional.xsd">
  <file datatype="xml" source-language="en-US" original="upgrade-cutover-testing.md" target-language="ja-JP">
    <header>
      <tool tool-company="Microsoft" tool-version="1.0-7889195" tool-name="mdxliff" tool-id="mdxliff"/>
      <xliffext:skl_file_name>upgrade-cutover-testing.c625e2.2c24e6770fc13172074c7e44d459c03811fd262d.skl</xliffext:skl_file_name>
      <xliffext:version>1.2</xliffext:version>
      <xliffext:ms.openlocfilehash>2c24e6770fc13172074c7e44d459c03811fd262d</xliffext:ms.openlocfilehash>
      <xliffext:ms.sourcegitcommit>9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b</xliffext:ms.sourcegitcommit>
      <xliffext:ms.lasthandoff>05/15/2019</xliffext:ms.lasthandoff>
      <xliffext:ms.openlocfilepath>articles\dev-itpro\migration-upgrade\upgrade-cutover-testing.md</xliffext:ms.openlocfilepath>
    </header>
    <body>
      <group extype="content" id="content">
        <trans-unit xml:space="preserve" translate="yes" id="101" restype="x-metadata">
          <source>Upgrade from AX 2012 - Cutover testing (Mock cutover)</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">AX 2012 からのアップグレード - 切替テスト (切替モック)</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="102" restype="x-metadata">
          <source>This topic explains how to test the cutover process between turning off an AX 2012 environment and turning on Dynamics 365 for Finance and Operations.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このトピックでは、AX 2012 環境をオフにしてから Dynamics 365 for Finance and Operations をオンにするまでの切替えプロセスをテストする方法について説明します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="103">
          <source>Upgrade from AX 2012 - Cutover testing (Mock cutover)</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">AX 2012 からのアップグレード - 切替テスト (切替モック)</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="104">
          <source><bpt id="p1">*</bpt>Cutover<ept id="p1">*</ept> is the term that we use for the final process of getting a new system live.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">*</bpt>切替<ept id="p1">*</ept>という用語は、新しいシステムを稼働させる最後のプロセスに使用します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="105">
          <source>The cutover process consists of the tasks that occur after Microsoft Dynamics AX 2012 is turned off, but before Microsoft Dynamics 365 for Finance and Operations, is turned on.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">切替プロセスは、Microsoft Dynamics AX 2012 をオフにした後、かつ Microsoft Dynamics 365 for Finance and Operations をオンにする前に発生するタスクで構成されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="106">
          <source>The purpose of upgrade cutover testing (mock cutover) is to practice the cutover process, to help guarantee a smooth experience for everyone who is involved during the actual cutover to go-live.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">アップグレード切替テスト (切替モック) の目的は、切替プロセスを練習することで、実際の切替中に関係するすべての人がスムーズに作業できるようにすることです。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="107">
          <source>There are three main workstreams during a cutover:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">切替中には、3 つの主要なワーク ストリームがあります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="108">
          <source><bpt id="p1">**</bpt>Technical workstream<ept id="p1">**</ept> – This workstream includes the data upgrade execution process.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>技術的なワーク ストリーム<ept id="p1">**</ept> – このワーク ストリームには、データ アップグレードの実行プロセスが含まれています。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="109">
          <source>Your business will enforce a limit on the amount of downtime that is allowed.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">業務では、許可されているダウンタイムの金額に制限が適用されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="110">
          <source>During this downtime, neither AX 2012 nor Finance and Operations will be available.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ダウンタイムの間は、AX 2012 または Finance and Operations のいずれも利用できません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="111">
          <source>This workstream might have to tune the data upgrade procedure to meet the business's downtime limit.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このワーク ストリームでは、業務でのダウンタイム制限を満たすために、データ アップグレード手順をチューニングする必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="112">
          <source><bpt id="p1">**</bpt>Functional workstream<ept id="p1">**</ept> – This workstream includes the configuration tasks that are performed after the data upgrade is completed.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>機能的なワーク ストリーム<ept id="p1">**</ept> – このワーク ストリームには、データのアップグレードが完了した後に実行されるコンフィギュレーション タスクが含まれます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="113">
          <source>All these tasks must be documented and quantified, and a resource must be assigned, because both the functional workstream and the technical workstream must fit within the business's downtime limit.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">機能的なワークストリームと技術的なワークストリームの両方が業務のダウンタイム制限内に収まる必要があるため、これらのタスクをすべて文書化および定量化し、リソースを割り当てる必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="114">
          <source><bpt id="p1">**</bpt>AX 2012 rollback<ept id="p1">**</ept> - This workstream includes rolling back to an AX 2012 environment.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>AX 2012 ロールバック<ept id="p1">**</ept> - このワークストリームには AX 2012 環境へのロールバックが含まれています。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="115">
          <source>Although it's unlikely that you will have to roll back, it's very important that you have a tested process in case you require it.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ロールバックする必要はありませんが、必要な場合に備えてテスト済みのプロセスがあることが非常に重要です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="116">
          <source>The following illustration shows the overall process for cutover to go-live as it will occur in the production environment.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">次の図は、実稼動環境で発生するような、切替中の全体的なプロセスを示しています。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="117">
          <source>Cutover process</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">切替プロセス</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="118">
          <source>The mock cutover process is very similar to a basic data upgrade validation in a sandbox environment.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">モック カットオーバー プロセスは、サンドボックス環境での基本的なデータ アップグレードの検証と非常によく似ています。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="119">
          <source>We assume that you are familiar with that process, and have already performed it.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">そのプロセスを熟知していて、そのプロセスを既に実行済みであると仮定します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="120">
          <source>Mock cutover differs in the following ways:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">切替モックは、次の点で異なります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="121">
          <source>After you perform a data upgrade in the sandbox environment, a LCS other type service requests is needed to copy your upgraded database from the data upgrade sandbox environment into your production environment.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">サンドボックス環境でデータ更新を実行した後、アップグレードされたデータベースをデータ アップグレード サンドボックス環境から実稼働環境にコピーするには、他のタイプの LCS サービス リクエストが必要です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="122">
          <source>The email template below is provided for your use</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">以下の電子メール テンプレートは、ユーザーの使用のため提供されています。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="123">
          <source>[!Copy] This is a request for 2012 data upgrade database copy from the sandbox environment <ph id="ph1">&lt;source sandbox environment name&gt;</ph> to production.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">[!コピー] これは、サンドボックス環境<ph id="ph1">&lt;source sandbox environment name&gt;</ph>から本番環境への 2012 データ アップグレード データベース コピーの要求です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="124">
          <source>I acknowledge that this will overwrite the database currently in production.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">現在稼働中のデータベースを上書きすることに同意します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="125">
          <source>We added the following tasks:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">次のタスクを追加しました。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="126">
          <source>Perform a smoke test.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">スモーク テストを実行します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="127">
          <source>Complete application setup tasks.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">アプリケーションの設定タスクを完了します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="128">
          <source>This step can be large, depending on the functionality that is used.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このステップは、使用する機能に応じて大規模になる場合があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="129">
          <source>During this step, the functional team configures new application functionality so that it's ready to be used in the upgraded system.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このステップでは、機能チームは新しいアプリケーションの機能を構成して、アップグレードされたシステムで使用できるようにします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="130">
          <source>Allow users back in.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ユーザーがシステムに戻れるようにします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="131">
          <source>Notify your user base that the upgrade is completed and that they can use the system again.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">アップグレードが完了して、システムを再度使用できることをユーザーに通知します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="132">
          <source>In this article, we use the term <bpt id="p1">*</bpt>sandbox<ept id="p1">*</ept> to refer to a Standard or Premier Acceptance Testing (Tier 2 or 3) or higher environment connected to a SQL Azure database.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この記事では、<bpt id="p1">*</bpt>サンドボックス<ept id="p1">*</ept> という用語を使用して SQL Azure データベースに接続されている標準またはプレミア承認テスト (レベル 2 または 3)、またはより高度な環境を示します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="133">
          <source>Technical workstream</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">技術的なワーク ストリーム</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="134">
          <source>The technical workstream involves various technical team members: the database administrator (DBA), the AX 2012 system administrator, server administrators, and developers who are familiar with AX 2012 and Finance and Operations.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">技術的なワークストリームに含まれるさまざまな技術チームのメンバー: データベース管理者 (DBA)、AX 2012 のシステム管理者、サーバー管理者、AX 2012 および Finance and Operations に精通している開発者。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="135">
          <source>This topic will explain which tasks involve which roles.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このトピックでは、どのタスクがどのロールを含めるかについて説明します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="136">
          <source>During cutover testing, the technical team is focused on performance and reliability testing of the data upgrade process, to make sure that it meets the business's downtime limit.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">切替テスト中には、技術チームは、データ アップグレード プロセスのパフォーマンスと信頼性のテストに焦点を当てて、ビジネスのダウンタイム制限を満たすようにします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="137">
          <source>Many elements of hardware and software are involved in this process.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ハードウェアとソフトウェアの多くの要素がこのプロセスに関連しています。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="138">
          <source>Some of these elements are on-premises, whereas others are in the Microsoft cloud.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">これらの要素の一部はオンプレミスですが、他の要素は Microsoft クラウドに含まれています。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="139">
          <source>In addition, many elements of custom application code and standard code are involved.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">加えて、カスタム アプリケーション コードと標準コードの多くの要素が含まれています。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="140">
          <source>The result of this testing should be confidence in the cutover process for your environment.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このテストの結果は、環境の切替プロセスを信頼する必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="141">
          <source>Technical workstream process</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">技術的なワーク ストリーム プロセス</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="142">
          <source>For the technical workstream, the cutover testing process is the same as the high-level steps of the actual/go-live cutover process.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">技術的なワークストリームについては、切替テストのプロセスは、実際/稼働の切替プロセスの高レベルの手順と同じです。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="143">
          <source>For the technical workstream, the cutover testing process is the same described in <bpt id="p1">[</bpt>Upgrade from AX 2012 - Data upgrade in a sandbox environment<ept id="p1">](upgrade-data-sandbox.md)</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">技術的なワークストリームについては、切替テストのプロセスは <bpt id="p1">[</bpt>AX 2012 からのアップグレード - サンドボックス環境でのデータ アップグレード<ept id="p1">](upgrade-data-sandbox.md)</ept> で説明したものと同じです。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="144">
          <source>Functional workstream</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">機能的なワーク ストリーム</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="145">
          <source>After data upgrade, several configuration tasks will be required in the new environment.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">データのアップグレード後に、新しい環境でいくつかのコンフィギュレーション タスクが必要になります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="146">
          <source>The goal of this workstream is to document and quantify all configuration tasks, and to assign a resource to each task, to help guarantee that these tasks can be done together with the technical workstream during the downtime window.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このワーク ストリームの目的は、すべてのコンフィギュレーション タスクを文書化および定量化し、リソースを各タスクに割り当てることで、ダウンタイム期間中にこれらのタスクを機能的なワーク ストリームとともに実行できるようにすることです。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="147">
          <source>Typically, functional tasks involve changing the values of specific system parameters or other configuration data.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">通常、機能的なタスクでは、特定のシステム パラメータの値または他のコンフィギュレーション データの値の変更が含まれます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="148">
          <source>These tasks are identified through the full functional test pass, which is a separate activity from the cutover testing.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">これらのタスクは、機能テストのパス全体を通して識別されます。これは、切替テストとは別のアクティビティです。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="149">
          <source>When a task of this type is identified, it should be reviewed together with the functional resource and your developer.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このタイプのタスクが特定された場合、機能のリソースおよび開発者と共に確認する必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="150">
          <source>Larger changes might require that a new custom data upgrade script be written to update the data during the data upgrade process.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">より大きな変更を行うには、新しいカスタム データ アップグレード スクリプトを作成して、データのアップグレード プロセス中にデータを更新する必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="151">
          <source>However, the functional resource can manually run smaller changes through the new system after data upgrade.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ただし、機能のリソースは、データのアップグレード後に新しいシステムを使用して、より小さな変更を手動で実行できます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="152">
          <source>Larger changes that have new data upgrade scripts must be tested.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">新しいデータのアップグレード スクリプトを持つ、より大規模な変更をテストする必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="153">
          <source>Therefore, one or more additional iterations of the MajorVersionDataUpgrade.zip package will have to be run.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">したがって、MajorVersionDataUpgrade.zip パッケージの 1 つ以上の追加の繰り返しを実行する必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="154">
          <source>It's important that you weigh the cost of running the package again against the cost of manual data entry.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">手動のデータ入力のコストに対して、パッケージを再度実行するコストを比較検討することが重要です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="155">
          <source>For each manual change, a task must be added to the cutover plan document.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">手動による変更のたびに、切替計画ドキュメントにタスクを追加する必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="156">
          <source>This task must show the following details:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このタスクでは、次の詳細を示す必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="157">
          <source>What is the task, and what must be done?</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">タスクとは何か、また必要な作業は何か。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="158">
          <source>Who must do it?</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">そのタスクを実行するのは誰か。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="159">
          <source>How long does it take?</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">時間はどのくらいかかるか。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="160">
          <source>Add users, and perform functionl tests</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ユーザーの追加、および機能テストの実行</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="161">
          <source>When you have fully configured your environment, add users, and perform appropriate testing.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">環境を完全に構成したときは、ユーザーを追加し、適切なテストを実行します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="162">
          <source>Roll back to AX 2012</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">AX 2012 にロールバックする</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="163">
          <source>The goal of this task is to restore the database by using the backup that was made when AX 2012 was turned off, and then turn AX 2012 back on.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このタスクの目的は、AX 2012 をオフにしたときのバックアップを使用してデータベースを復元し、AX 2012 を再度オンにすることです。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="164">
          <source>The state of integrated systems might also have to be restored.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">統合システムの状態も復元する必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="165">
          <source>However, because integrated systems vary from business to business, you must plan for this scenario independently, based on your specific circumstances.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ただし、統合システムは企業間で異なるため、特定の状況に応じてこのシナリオを個別に計画する必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="166">
          <source>Although it's unlikely that you will have to roll back, it's very important that you have a tested process in case you require it.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ロールバックする必要はありませんが、必要な場合に備えてテスト済みのプロセスがあることが非常に重要です。</target></trans-unit>
      </group>
    </body>
  </file>
</xliff>