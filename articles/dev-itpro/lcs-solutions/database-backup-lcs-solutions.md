<?xml version="1.0" encoding="UTF-8"?>
<xliff xmlns:logoport="urn:logoport:xliffeditor:xliff-extras:1.0" xmlns:tilt="urn:logoport:xliffeditor:tilt-non-translatables:1.0" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns="urn:oasis:names:tc:xliff:document:1.2" xmlns:xliffext="urn:microsoft:content:schema:xliffextensions" version="1.2" xsi:schemaLocation="urn:oasis:names:tc:xliff:document:1.2 xliff-core-1.2-transitional.xsd">
  <file datatype="xml" source-language="en-US" original="database-backup-lcs-solutions.md" target-language="ja-JP">
    <header>
      <tool tool-company="Microsoft" tool-version="1.0-7889195" tool-name="mdxliff" tool-id="mdxliff"/>
      <xliffext:skl_file_name>database-backup-lcs-solutions.3ee42e.2f52f0d191ef60147dd882030807af02018a9321.skl</xliffext:skl_file_name>
      <xliffext:version>1.2</xliffext:version>
      <xliffext:ms.openlocfilehash>2f52f0d191ef60147dd882030807af02018a9321</xliffext:ms.openlocfilehash>
      <xliffext:ms.sourcegitcommit>06c8dc5bc4e1c41f68e1cda141d61529768be958</xliffext:ms.sourcegitcommit>
      <xliffext:ms.lasthandoff>05/22/2019</xliffext:ms.lasthandoff>
      <xliffext:ms.openlocfilepath>articles\dev-itpro\lcs-solutions\database-backup-lcs-solutions.md</xliffext:ms.openlocfilepath>
    </header>
    <body>
      <group extype="content" id="content">
        <trans-unit xml:space="preserve" translate="yes" id="101" restype="x-metadata">
          <source>Back up the databases for Finance and Operations solutions</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Finance and Operations ソリューションのデータベースのバックアップ</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="102" restype="x-metadata">
          <source>This topic provides information about the database backup that is required for your Microsoft Dynamics Lifecycle Services (LCS) solution package.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このトピックでは、Microsoft Dynamics Lifecycle Services (LCS) ソリューション パッケージに必要なデータベースのバックアップに関する情報を提供します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="103">
          <source>Back up the databases for Finance and Operations solutions</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Finance and Operations ソリューションのデータベースのバックアップ</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="104">
          <source>A backup of the Microsoft Dynamics 365 for Finance and Operations database is required for your Microsoft Dynamics Lifecycle Services (LCS) solution package.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">バックアップを保存した Microsoft Dynamics 365 for Finance and Operations データベースに必要な Microsoft Dynamics Lifecycle Services (LCS) ソリューション パッケージします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="105">
          <source>When you back up the database, you must include the master, reference, and transactional data that is specific to your solution and industry.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">データベースをバックアップするときは、ソリューションと業界に固有のマスター、参照、およびトランザクション データを含める必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="106">
          <source>This data will be used for your pre-sales demo deployments.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このデータは販売前のデモ展開に使用されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="107">
          <source>On demo or development environments, the database is typically named AXDBRain.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">デモまたは開発環境では、データベースは通常 AXDBRain と呼ばれます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="108">
          <source>Your database backup should be no larger than 15 gigabytes (GB).</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">データベースのバックアップは、15 ギガバイト (GB) 未満にする必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="109">
          <source>Otherwise, a time-out error might occur when you try to upload the database to the Asset library in LCS.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">それ以外の場合は 、LCS でアセット ライブラリにデータベースをアップロードしようとすると、タイムアウト エラーが発生する可能性があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="110">
          <source>To compress your database backup, in Microsoft SQL Server Management Studio, on the <bpt id="p1">**</bpt>Back Up Database<ept id="p1">**</ept> page, in the <bpt id="p2">**</bpt>Set backup compression<ept id="p2">**</ept> field, select <bpt id="p3">**</bpt>Compress backup<ept id="p3">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Microsoft SQL Server Management Studio で、データベースのバックアップを圧縮するには、<bpt id="p1">**</bpt>データベースのバックアップ<ept id="p1">**</ept> ページの<bpt id="p2">**</bpt>バックアップ圧縮を設定<ept id="p2">**</ept>フィールドで、<bpt id="p3">**</bpt>バックアップの圧縮<ept id="p3">**</ept>を選択します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="111">
          <source><bpt id="p1">[</bpt><ph id="ph1">![</ph>Compress backup selected in the Set backup compression field<ept id="p1">](./media/databasebackup01.jpg)](./media/databasebackup01.jpg)</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">[</bpt><ph id="ph1">![</ph>セット バックアップ圧縮フィールドで選択されたバックアップを圧縮<ept id="p1">](./media/databasebackup01.jpg)](./media/databasebackup01.jpg)</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="112">
          <source>On demo or development environments, the database is typically called AXDBRain.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">デモまたは開発環境では、データベースは通常 AXDBRain と呼ばれます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="113">
          <source>Your database backup should be no larger than 15 gigabyte (GB).</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">データベースのバックアップは、15 ギガバイト (GB) 未満にする必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="114">
          <source>If your database is larger, a timeout error may occur when you try to upload the database to the <bpt id="p1">&lt;strong&gt;</bpt>Asset library **in Lifecycle Services (LCS). To compress your database backup, in SQL Server Management Studio, on the **Back Up Database<ept id="p1">&lt;/strong&gt;</ept> page, in the <bpt id="p2">&lt;strong&gt;</bpt>Set backup compression<ept id="p2">&lt;/strong&gt;</ept> field, select <bpt id="p3">&lt;strong&gt;</bpt>Compress backup<ept id="p3">&lt;/strong&gt;</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">データベースが大きい場合、Lifecycle Services (LCS) で<bpt id="p1">&lt;strong&gt;</bpt>アセット ライブラリ**にデータベースをアップロードしようとすると、タイムアウト エラーが発生する場合があります。データベース バックアップを圧縮するには、SQL Server Management Studio で、**データベースのバックアップ<ept id="p1">&lt;/strong&gt;</ept> ページの<bpt id="p2">&lt;strong&gt;</bpt>バックアップ圧縮の設定<ept id="p2">&lt;/strong&gt;</ept>フィールドで、<bpt id="p3">&lt;strong&gt;</bpt>バックアップの圧縮<ept id="p3">&lt;/strong&gt;</ept>を選択します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="115">
          <source><bpt id="p1">[</bpt><ph id="ph1">![</ph>databasebackup01<ept id="p1">](./media/databasebackup01.jpg)](./media/databasebackup01.jpg)</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">[</bpt><ph id="ph1">![</ph>databasebackup01<ept id="p1">](./media/databasebackup01.jpg)](./media/databasebackup01.jpg)</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="116">
          <source>Additional resources</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">追加リソース</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="117">
          <source><bpt id="p1">[</bpt>Publishing an App for Dynamics 365 for Finance and Operations in AppSource<ept id="p1">](lcs-solutions-app-source.md)</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">[</bpt>AppSource の Dynamics 365 for Finance and Operations アプリを公開<ept id="p1">](lcs-solutions-app-source.md)</ept></target></trans-unit>
      </group>
    </body>
  </file>
</xliff>