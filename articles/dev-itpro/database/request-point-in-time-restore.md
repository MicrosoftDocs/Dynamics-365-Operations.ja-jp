<?xml version="1.0" encoding="UTF-8"?>
<xliff xmlns:logoport="urn:logoport:xliffeditor:xliff-extras:1.0" xmlns:tilt="urn:logoport:xliffeditor:tilt-non-translatables:1.0" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns="urn:oasis:names:tc:xliff:document:1.2" xmlns:xliffext="urn:microsoft:content:schema:xliffextensions" version="1.2" xsi:schemaLocation="urn:oasis:names:tc:xliff:document:1.2 xliff-core-1.2-transitional.xsd">
  <file datatype="xml" source-language="en-US" original="request-point-in-time-restore.md" target-language="ja-JP">
    <header>
      <tool tool-company="Microsoft" tool-version="1.0-7889195" tool-name="mdxliff" tool-id="mdxliff"/>
      <xliffext:skl_file_name>request-point-in-time-restore.0d74ce.73da227045377f6eaebfac4fd4327050803c9ce7.skl</xliffext:skl_file_name>
      <xliffext:version>1.2</xliffext:version>
      <xliffext:ms.openlocfilehash>73da227045377f6eaebfac4fd4327050803c9ce7</xliffext:ms.openlocfilehash>
      <xliffext:ms.sourcegitcommit>9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b</xliffext:ms.sourcegitcommit>
      <xliffext:ms.lasthandoff>05/15/2019</xliffext:ms.lasthandoff>
      <xliffext:ms.openlocfilepath>articles\dev-itpro\database\request-point-in-time-restore.md</xliffext:ms.openlocfilepath>
    </header>
    <body>
      <group extype="content" id="content">
        <trans-unit xml:space="preserve" translate="yes" id="101" restype="x-metadata">
          <source>Restore databases in non-production environments</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">非実稼働環境でのデータベースの復元</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="102" restype="x-metadata">
          <source>Microsoft Dynamics 365 for Finance and Operations lets you request that a database be restored to a specific point in time that is within 35 days of your request.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Microsoft Dynamics 365 for Finance and Operations では、データベースを要求後 35 日以内の特定の時点に復元するように要求できます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="103" restype="x-metadata">
          <source>This topic describes how to request a point-in-time restore.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このトピックでは、Point-in-Time 復元を要求する方法について説明します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="104">
          <source>Restore databases in non-production environments</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">非実稼働環境でのデータベースの復元</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="105">
          <source>Microsoft Dynamics 365 for Finance and Operations lets you request that a database be restored to a specific point in time that is within 35 days of your request.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Microsoft Dynamics 365 for Finance and Operations では、データベースを要求後 35 日以内の特定の時点に復元するように要求できます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="106">
          <source>This topic describes how to request a point-in-time restore.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このトピックでは、Point-in-Time 復元を要求する方法について説明します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="107">
          <source>Point-in-time restore is a Microsoft Azure SQL Database feature that can be used with Microsoft Dynamics 365 for Finance and Operations.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ポイントインタイム復元は、Microsoft Dynamics 365 for Finance and Operations で使用できる Microsoft Azure SQL データベース機能です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="108">
          <source>A point-in-time restore resets a non-production environment to a known good state after destructive testing.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ポイントインタイム復元では、破壊試験後に、非製造環境を既知の正常な状態にリセットします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="109">
          <source>In an emergency, you can also do a point-in-time restore on a production environment.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">緊急の場合は、実稼働環境でポイントインタイム復元を実行することもできます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="110">
          <source>However, to request a production restore, don't use the process that is described in this topic.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ただし、生産復元を要求するには、このトピックに記載されているプロセスを使用しないでください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="111">
          <source>Instead, you should contact Microsoft Support.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">代わりに、Microsoft サポートに問い合わせてください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="112">
          <source>The point-in-time restore feature always creates a new database.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ポイントインタイム リストア機能により、かならず新しいデータベースが作成されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="113">
          <source>To uptake the new database into the Dynamics 365 for Finance and Operations environment, you must replace the original database with the new database.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">新しいデータベースを Dynamics 365 for Finance and Operations 環境に取り込むには、元のデータベースを新しいデータベースに置き換える必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="114">
          <source>Therefore, after you uptake the new database, all backup history is gone.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">したがって、新しいデータベースを取り込んだ後、すべてのバックアップの履歴はなくなります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="115">
          <source>History tracking will begin again from that moment.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">その時点から履歴の追跡が再び開始されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="116">
          <source><bpt id="p1">[</bpt><ph id="ph1">![</ph>Example of a database before and after a point-in-time restore<ept id="p1">](./media/pitrestorebehaviour.png)](./media/pitrestorebehaviour.png)</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">[</bpt><ph id="ph1">![</ph>ポイント イン タイム復元前後のデータベースの例<ept id="p1">](./media/pitrestorebehaviour.png)](./media/pitrestorebehaviour.png)</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="117">
          <source>Code versioning</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">コード バージョン管理</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="118">
          <source>When you're trying to determine which restore point in time to select, it's important that you consider code versioning, because the current version of the code might be incompatible with the state of the database at the restore point.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">選択する復元時点を決定するときは、コード バージョン管理を考慮することが重要です。それは、コードの現在のバージョンが復元時点のデータベースの状態と互換性がない場合があるためです。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="119">
          <source>For example, today's database is running Microsoft Dynamics 365 for Finance and Operations Platform Update 2, plus some customizations.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">たとえば、今日のデータベースは、Microsoft Dynamics 365 for Finance and Operations プラットフォーム更新プログラム 2、およびいくつかのカスタマイズを実行しています。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="120">
          <source>However, 10 days ago, the environment was running the Microsoft Dynamics AX February 2016 release, plus customizations that were created for that build.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ただし、10 日前には、2016 年 2 月にリリースされた Microsoft Dynamics AX 、さらにそのビルドを作成されたカスタマイズが環境で実行されていました。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="121">
          <source>If you try to restore the database to the state that it was in 10 days ago, but the environment is still running the most recent version of the code, the environment might not work as you expect, because the database has been upgraded.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">データベースを 10 日前の状態に復元しようとしましたが、環境でコードの最新バージョンが実行されている場合、データベースがアップグレードされているため、期待どおりに動作しない可能性があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="122">
          <source>Although you might be able to mix a version of the database and a version of the code without encountering issues, it's important that you be aware that issues can occur.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">問題を発生させることなく、データベースのバージョンとコードのバージョンを混在させることはできますが、問題が発生する可能性があることに注意してください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="123">
          <source>We recommend that, as a rule, you not mix major version releases from Microsoft, or major versions of customizations.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">一般に、Microsoft からの、またはカスタマイズのメジャー バージョンからのメジャー バージョン リリースを混同しないことをお勧めします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="124">
          <source>Here is the most common scenario where you will require a point-in-time restore:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ポイントインタイム復元を要求する最も一般的なシナリオを次に示します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="125">
          <source>User tests that are run in the sandbox environment identify some bugs.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">サンドボックス環境で実行されるユーザー テストにはいくつかのバグがあります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="126">
          <source>The bugs are fixed in a development environment, and a new build is deployed to the sandbox environment.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">バグは開発環境で修正され、新しいビルドはサンドボックス環境に展開されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="127">
          <source>You request a point-in-time restore to restore the database to a time before the tests were run, so that the database can be retested in exactly the same way.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">データベースをまったく同じ方法で再テストできるように、ポイントインタイム復元を要求して、テストを実施する前の時点にデータベースを復元します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="128">
          <source>In this case, there is mismatch of the code version and the database, because the bug fixes were deployed.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この場合、修正が配置されたため、コード バージョンとデータベースの不一致が発生します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="129">
          <source>However, this mismatch is unlikely to cause an issue.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ただし、この不一致により問題が発生することはあまりありません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="130">
          <source>Consult the developers who make the customizations to verify that you can proceed.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">カスタマイズを行う開発者に問い合わせ、進めることができることを確認してください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="131">
          <source>After the database is restored, synchronize it.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">データベースを復元した後、それを同期します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="132">
          <source>Point-in-time restore process</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ポイントインタイム復元プロセス</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="133">
          <source>The Microsoft Service Engineering team will take your environment offline, complete the point-in-time restore, and then bring the environment back online.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Microsoft サービス エンジニアリング チームは、環境をオフラインにして、ポイント イン タイム復元を実行し、環境をオンラインに戻します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="134">
          <source>You can expect the downtime period to be less than two hours.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ダウンタイム期間が 2 時間未満であると予測することができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="135">
          <source>The period after you enter your request and before our Service Engineers take action will be longer than your environment downtime.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ユーザーが要求を入力してから、マイクロソフトのサービス エンジニアが措置を講じるまでの時間が、ユーザーの環境のダウンタイムよりも長くなります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="136">
          <source>In the future, we will provide a self-service method that you can use to perform your own point-in-time restores.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">今後、独自のポイントインタイム復元を実行するために使用できるセルフ サービスのメソッドを提供する予定です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="137">
          <source>Click the hamburger icon in the upper left of the Microsoft Dynamics Lifecycle Services (LCS) window, and then select <bpt id="p1">**</bpt>Work items<ept id="p1">**</ept> in the list.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Microsoft Dynamics Lifecycle Services (LCS) ウィンドウの左上にあるハンバーガー アイコンをクリックし、一覧から<bpt id="p1">**</bpt>作業項目<ept id="p1">**</ept>を選択します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="138">
          <source><bpt id="p1">[</bpt><ph id="ph1">![</ph>Work items<ept id="p1">](./media/selectworkitems.png)](./media/selectworkitems.png)</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">[</bpt><ph id="ph1">![</ph>作業項目<ept id="p1">](./media/selectworkitems.png)](./media/selectworkitems.png)</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="139">
          <source>On the <bpt id="p1">**</bpt>Work items<ept id="p1">**</ept> page, click <bpt id="p2">**</bpt>Add<ept id="p2">**</ept> on the toolbar, and then click <bpt id="p3">**</bpt>Database point-in-time restore request<ept id="p3">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>作業項目<ept id="p1">**</ept>ページで、ツール バーの<bpt id="p2">**</bpt>追加<ept id="p2">**</ept>をクリックし、<bpt id="p3">**</bpt>データベース ポイントインタイム復元要求<ept id="p3">**</ept>をクリックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="140">
          <source><bpt id="p1">[</bpt><ph id="ph1">![</ph>Database point-in-time restore request<ept id="p1">](./media/createrequest.png)](./media/createrequest.png)</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">[</bpt><ph id="ph1">![</ph>データベース ポイントインタイム復元要求<ept id="p1">](./media/createrequest.png)](./media/createrequest.png)</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="141">
          <source>In the <bpt id="p1">**</bpt>Request for database point-in-time restore<ept id="p1">**</ept> dialog box, follow these steps:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>データベース ポイントインタイム復元要求<ept id="p1">**</ept>ダイアログ ボックスで、これらの手順に従います。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="142">
          <source>In the <bpt id="p1">**</bpt>Environment name<ept id="p1">**</ept> field, select the environment to restore.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>環境名<ept id="p1">**</ept>フィールドで、復元する環境を選択します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="143">
          <source>Only Azure SQL Database environments can be restored.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Azure SQL データベース環境のみを復元することができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="144">
          <source>Therefore, you can't select one-box environments that are based on Microsoft SQL Server.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">したがって、Microsoft SQL Server に基づく 1 つのボックス環境は選択できません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="145">
          <source>In the <bpt id="p1">**</bpt>Database<ept id="p1">**</ept> field, the database to restore is always Microsoft Dynamics AX or Microsoft Dynamics 365 for Finance and Operations.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>データベース<ept id="p1">**</ept> フィールドでは、復元するデータベースは常に Microsoft Dynamics AX または Microsoft Dynamics 365 for Finance and Operations です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="146">
          <source>Other databases, such as Entity store or Financial reporting, aren't currently supported for point-in-time restores.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">エンティティ格納や財務報告など、他のデータベースでは、ポイントインタイム復元が現在サポートされていません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="147">
          <source>Enter information in the <bpt id="p1">**</bpt>Restore point time<ept id="p1">**</ept> fields.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>特定の時点の復元<ept id="p1">**</ept>フィールドに情報を入力します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="148">
          <source>Azure SQL Database lets you restore a database to a point in time that is up to 35 days before the date when you make the request.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Azure SQL データベースを使用すると、要求を作成する日の 35 日前までの時点にデータベースを復元できます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="149">
          <source>If the environment is less than 35 days old, or if it has previously been restored, the maximum amount of time will be less.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">環境が 35 日未満の場合、または以前に復元されている場合は、最大時間が少なくなります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="150">
          <source>Enter information in the <bpt id="p1">**</bpt>Preferred downtime start date<ept id="p1">**</ept> and the <bpt id="p2">**</bpt>Preferred downtime end date<ept id="p2">**</ept> fields.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>ダウンタイム開始日を優先<ept id="p1">**</ept>および<bpt id="p2">**</bpt>ダウンタイム終了日を優先<ept id="p2">**</ept>フィールドに情報を入力します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="151">
          <source>The end date must be at least one hour after the start date.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">サイクル終了日は、サイクル開始日の少なくとも 1 時間後でなければなりません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="152">
          <source>Requests must be submitted least 24 hours before the preferred downtime window, to help guarantee that resources are available to complete the request.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">要求は、要求を完了するためにリソースを確実に使用できるようにするため、推奨されるダウンタイム期間の少なくとも 24 時間前までに送信する必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="153">
          <source>Carefully read and acknowledge the three statements that have check boxes next to them.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">チェック ボックスを隣に置いた 3 つのステートメントを注意深く読んで確認してください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="154">
          <source><bpt id="p1">[</bpt><ph id="ph1">![</ph>Request for database point-in-time restore dialog box<ept id="p1">](./media/requestform.png)](./media/requestform.png)</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">[</bpt><ph id="ph1">![</ph>データベース ポイント イン タイム復元ダイアログ ボックスの要求<ept id="p1">](./media/requestform.png)](./media/requestform.png)</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="155">
          <source>After you submit your request, you will be redirected to the list of work items.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">要求を送信した後、作業項目のリストにリダイレクトされます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="156">
          <source>Here, you can view the status of the request, or reschedule or cancel the request.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ここで、要求のステータスを表示し、または再スケジューリングし、または要求をキャンセルできます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="157">
          <source>When the Microsoft Service Engineering team has acknowledged that it can complete your request, the status of the request changes to <bpt id="p1">**</bpt>Request accepted<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Microsoft サービス エンジニア リング チームがお客様の要求を達成できることを確認したとき、その要求のステータスは <bpt id="p1">**</bpt>要求受入済<ept id="p1">**</ept> に変わります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="158">
          <source>At this point, you can follow any of these steps:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この時点で、次のいずれかの手順を実行できます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="159">
          <source>Wait for the Service Engineering team to complete the restore.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">サービス エンジニア リング チームによる復元が完了するまで待ちます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="160">
          <source>When restore is completed, the status changes to <bpt id="p1">**</bpt>Succeeded<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">復元が完了したら、ステータスが <bpt id="p1">**</bpt>"成功"<ept id="p1">**</ept> に変更されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="161">
          <source>Reschedule the request by clicking the ID, or by selecting the request and then clicking <bpt id="p1">**</bpt>Reschedule<ept id="p1">**</ept> on the toolbar.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ID をクリックするか、要求を選択してツール バーで <bpt id="p1">**</bpt>再スケジューリング<ept id="p1">**</ept> をクリックすることにより、リクエストを再スケジューリングします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="162">
          <source>You can then change the downtime windows dates and times, and the point in time to restore to.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ダウンタイム ウィンドウの日時、および復元する時点を変更することができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="163">
          <source>Cancel the request by selecting the request and then clicking <bpt id="p1">**</bpt>Cancel<ept id="p1">**</ept> on the toolbar.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">要求を選択し、ツールバーの<bpt id="p1">**</bpt>キャンセル<ept id="p1">**</ept>をクリックして、要求をキャンセルします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="164">
          <source>Enable change tracking</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">変更追跡の有効化</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="165">
          <source>If change tracking was enabled in the database, ensure to enable change tracking again in the newly restored database using the ALTER DATABASE command.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">データベースで変更追跡が有効になっている場合は、ALTER DATABASE コマンドを使用して、新しく復元したデータベースで変更追跡を再度有効にしてください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="166">
          <source>To ensure current version of the store procedure (related to change tracking) is used in the new database, you must enable/disable change tracking for a data entity in data management.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">新しいデータベースで店舗の業務手順の現在のバージョン (変更追跡に関連する) が使用されていることを確認するには、データ管理のデータ エンティティの変更追跡を有効または無効にする必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="167">
          <source>This can be done on any entity as this is needed to trigger the refresh of store procedure.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">これは、店舗の業務手順の更新をトリガーするために必要なので、どのエンティティでも実行できます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="168">
          <source>Conditions of a point-in-time restore</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ポイントインタイム復元要求の条件</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="169">
          <source>Here is the list of requirements and conditions of operation for a point-in-time restore:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ポイントインタイム復元の操作の要件および条件の一覧を次に示します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="170">
          <source>Requests must be submitted 24 hours before the desired downtime window, to help guarantee that resources will be available to complete the request.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">要求は、要求を完了するためにリソースを確実に使用できるようにするため、目的のダウンタイム期間の 24 時間前までに送信する必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="171">
          <source>A point-in-time restore erases the existing database in the target environment.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ポイントインタイム復元により、ターゲット環境の既存のデータベースが消去されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="172">
          <source>The existing database can't be recovered after the restore is completed.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">復元が完了すると、既存のデータベースを復元することはできません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="173">
          <source>The target environment will be unavailable until the refresh process is completed.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">更新プロセスが完了するまで、ターゲット環境は使用できなくなります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="174">
          <source>The point-in-time restore will affect only the Dynamics 365 for Finance and Operations database.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ポイントインタイム リストアは、Dynamics 365 for Finance and Operations データベースのみに影響します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="175">
          <source>Document handling documents that are stored in Azure blob storage won't be changed and will remain in their current state.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Azure blob storage に格納されているドキュメント処理のドキュメントは、変更されず現在の状態で残ります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="176">
          <source>The same rule applies to any documents that are stored in Azure blob storage through X++ customization.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">同様のルールは、 X++ のカスタマイズによって Azure Blob Storage に保存されているすべてのドキュメントに適用されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="177">
          <source>The Financial reporting database will also remain in the current state and must be reset after the restore is completed.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">財務諸表データベースは、現在の状態にも残ります、復元が完了した後にリセットする必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="178">
          <source>The Dynamics 365 for Finance and Operations database will be left at the precise state that it was in at the requested point in time.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Dynamics 365 for Finance and Operations データベースは、要求された時点の正確な状態のままになります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="179">
          <source>We do <bpt id="p1">**</bpt>not<ept id="p1">**</ept> withhold batches or restrict access to the restored database.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">バッチの保留または復元したデータベースへのアクセスの制限は行い <bpt id="p1">**</bpt>ません<ept id="p1">**</ept>。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="180">
          <source>LCS users who have a role of <bpt id="p1">**</bpt>Project Owner<ept id="p1">**</ept> or <bpt id="p2">**</bpt>Environment Manager<ept id="p2">**</ept> in LCS will have access to the Azure SQL Database and machine credentials for all non-production environments.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">LCS で<bpt id="p1">**</bpt>プロジェクト所有者<ept id="p1">**</ept>または<bpt id="p2">**</bpt>環境マネージャー<ept id="p2">**</ept>のロールを持つ LCS ユーザーは、すべての非実稼働環境の Azure SQL データベースとマシンの資格情報にアクセスします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="181">
          <source>To help guarantee security of the data that is copied to non-production environments, restrict membership in these roles.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">非実稼働環境にコピーされたデータのセキュリティを保証するには、これらのロールのメンバーシップを制限します。</target></trans-unit>
      </group>
    </body>
  </file>
</xliff>