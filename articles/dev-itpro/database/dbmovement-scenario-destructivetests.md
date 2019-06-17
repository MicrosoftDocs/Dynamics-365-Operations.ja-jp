<?xml version="1.0" encoding="UTF-8"?>
<xliff xmlns:logoport="urn:logoport:xliffeditor:xliff-extras:1.0" xmlns:tilt="urn:logoport:xliffeditor:tilt-non-translatables:1.0" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns="urn:oasis:names:tc:xliff:document:1.2" xmlns:xliffext="urn:microsoft:content:schema:xliffextensions" version="1.2" xsi:schemaLocation="urn:oasis:names:tc:xliff:document:1.2 xliff-core-1.2-transitional.xsd">
  <file datatype="xml" source-language="en-US" original="dbmovement-scenario-destructivetests.md" target-language="ja-JP">
    <header>
      <tool tool-company="Microsoft" tool-version="1.0-7889195" tool-name="mdxliff" tool-id="mdxliff"/>
      <xliffext:skl_file_name>dbmovement-scenario-destructivetests.3755dc.dfdb21f6a0c6194e474010acaca20c0f78a5d582.skl</xliffext:skl_file_name>
      <xliffext:version>1.2</xliffext:version>
      <xliffext:ms.openlocfilehash>dfdb21f6a0c6194e474010acaca20c0f78a5d582</xliffext:ms.openlocfilehash>
      <xliffext:ms.sourcegitcommit>9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b</xliffext:ms.sourcegitcommit>
      <xliffext:ms.lasthandoff>05/15/2019</xliffext:ms.lasthandoff>
      <xliffext:ms.openlocfilepath>articles\dev-itpro\database\dbmovement-scenario-destructivetests.md</xliffext:ms.openlocfilepath>
    </header>
    <body>
      <group extype="content" id="content">
        <trans-unit xml:space="preserve" translate="yes" id="101" restype="x-metadata">
          <source>Destructive testing</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">破壊試験</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="102" restype="x-metadata">
          <source>This topic explains a destructive testing scenario for Microsoft Dynamics 365 for Finance and Operations.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このトピックでは、Microsoft Dynamics 365 for Finance and Operations の破壊テスト シナリオについて説明します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="103">
          <source>Destructive testing</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">破壊試験</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="104">
          <source>Database movement operations are a suite of self-service actions that can be used as part of data application lifecycle management (DataALM).</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">データベース移動操作は、データ アプリケーション ライフ サイクル管理 (DataALM) の一部として使用できる一連のセルフ サービスのアクションです。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="105">
          <source>In some situations,  destructive testing must be done on an environment.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">場合によっては、環境で破壊試験を実行する必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="106">
          <source>In this context, destructive testing means that the environment is rendered no longer useful for continued testing.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このコンテキストでは、破壊試験は、環境を継続的なテストに使用できなくなったと宣言することを意味します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="107">
          <source>Destructive testing is typical in an implementation lifecycle during Conference Room Pilots.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">破壊試験は、会議室パイロット中の実装ライフ サイクルでは一般的です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="108">
          <source>This tutorial shows how to use database movement operations to facilitate destructive testing.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このチュートリアルでは、破壊試験を容易にするデータベース移動操作の使用方法を示します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="109">
          <source>In this tutorial, you will learn two approaches:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このチュートリアルでは、2 つの操作について説明します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="110">
          <source>Use a database backup asset.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">データベース バックアップ資産を使用します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="111">
          <source>Use point-in-time restore.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ポイントインタイム復元を使用します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="112">
          <source>As an example of this scenario, a customer wants to do a Conference Room Pilot and wants to start with an environment that has no transactions (that is, no sales orders or purchase orders).</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このシナリオの例として、顧客は会議室パイロットを実行しようとしており、トランザクションがない (つまり、販売注文や発注書がない) 環境で開始します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="113">
          <source>The customer will be traveling from physical warehouse to physical warehouse throughout his or her geographic region to do the same pilot, and wants the environment to be "reset" before each pilot is done.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">顧客は、同じパイロットを行うために、ユーザーの地域間で物理的な倉庫から物理的な倉庫に移動し、各パイロットが行われる前に、環境を「リセット」することを希望しています。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="114">
          <source>Prerequisites</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">必要条件</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="115">
          <source>To complete this tutorial, you must have a standard user acceptance testing (UAT) environment deployed in your project.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このチュートリアルを完了するには、プロジェクトに標準ユーザー受け入れテスト (UAT) 環境が展開されている必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="116">
          <source>Using a database backup</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">データベースのバックアップの使用</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="117">
          <source>If you've prepared a database backup (.bacpac) file that is already at the starting point for the test, the easiest approach is to upload the backup file to the <bpt id="p1">**</bpt>Database backup<ept id="p1">**</ept> section in your LCS project's Asset Library.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">すでにテストの準備ができているデータベース バックアップ (.bacpac) ファイルがある場合、最も簡単な方法は、バックアップ ファイルを LCS プロジェクトの資産ライブラリ内の<bpt id="p1">**</bpt>データベース バックアップ<ept id="p1">**</ept>セクションにアップロードすることです。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="118">
          <source>It can then be imported to your target environment as described here.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">その後、ここで説明するように、対象となる環境にインポートすることができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="119">
          <source>Database backup pros and cons</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">データベース バックアップの長所と短所</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="120">
          <source>The advantage of using backup file assets is that you can keep importing the same file to get back to the starting point for the test.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">バックアップ ファイル資産を使用する利点は、テストの開始点に戻るために、同じファイルのインポートを保持できることです。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="121">
          <source>The disadvantage is that if many configurations (for example, batch jobs) must be set after the import is completed but before users can begin, more effort will be required before each destructive testing session.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">デメリットは、インポートが完了する前かつユーザーが開始できるようになった後に多くの構成 (バッチ ジョブなど) を設定する必要がある場合、各破壊テスト セッションの前により多くの作業が必要になる点です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="122">
          <source>Using point-in-time restore</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ポイントインタイム復元の使用</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="123">
          <source>If you didn't start with a database backup (.bacpac) file but instead have the UAT environment in a known good state, you can just record the date and time in your time zone.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">データベース バックアップ (.bacpac) ファイルで開始しなかった場合に、正常な状態であることがわかっている UAT 環境がある場合、自分のタイムゾーンの日時を記録できます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="124">
          <source>You can then begin the destructive testing.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">その後、破壊試験を開始できます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="125">
          <source>Then, when the testing is completed, you can restore the environment to the previous time by using the following steps.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">次に、テストが完了したら、、次の手順を使用して、前の時点の環境を復元できます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="126">
          <source>Point-in-time restore pros and cons</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ポイントインタイム復元のメリットとデメリット</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="127">
          <source>The advantage of using point-in-time-restore is that you can avoid dealing with database backup (.bacpac) files and can reduce the time between destructive testing sessions.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ポイントタイム復元を使用する利点は、データベース バックアップ (.bacpac) ファイルの処理を回避できるため、破壊テスト セッションの間の時間を短縮できることです。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="128">
          <source>The disadvantage is that, because of current limitations of point-in-time restore, you must record a new restore date and time in your time zone after the restore is completed.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">デメリットは、ポイントインタイム復元の現在の制限により、復元が完了した後に新しい復元の日時を記録する必要があることです。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="129">
          <source>Because point-in-time restore always creates a new database, the original date and time that were used won't be available as a restore point on the new database.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ポイントインタイム復元では常に新しいデータベースが作成されるため、使用された元の日時は新しいデータベースの復元ポイントとして使用できません。</target></trans-unit>
      </group>
    </body>
  </file>
</xliff>