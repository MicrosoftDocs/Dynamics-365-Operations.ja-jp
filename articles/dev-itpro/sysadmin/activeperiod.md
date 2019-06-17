<?xml version="1.0" encoding="UTF-8"?>
<xliff xmlns:logoport="urn:logoport:xliffeditor:xliff-extras:1.0" xmlns:tilt="urn:logoport:xliffeditor:tilt-non-translatables:1.0" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns="urn:oasis:names:tc:xliff:document:1.2" xmlns:xliffext="urn:microsoft:content:schema:xliffextensions" version="1.2" xsi:schemaLocation="urn:oasis:names:tc:xliff:document:1.2 xliff-core-1.2-transitional.xsd">
  <file datatype="xml" source-language="en-US" original="activeperiod.md" target-language="ja-JP">
    <header>
      <tool tool-company="Microsoft" tool-version="1.0-7889195" tool-name="mdxliff" tool-id="mdxliff"/>
      <xliffext:skl_file_name>activeperiod.545dae.03ae30cb14770a7f930dbb72cbd77f27b7f538f1.skl</xliffext:skl_file_name>
      <xliffext:version>1.2</xliffext:version>
      <xliffext:ms.openlocfilehash>03ae30cb14770a7f930dbb72cbd77f27b7f538f1</xliffext:ms.openlocfilehash>
      <xliffext:ms.sourcegitcommit>9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b</xliffext:ms.sourcegitcommit>
      <xliffext:ms.lasthandoff>05/15/2019</xliffext:ms.lasthandoff>
      <xliffext:ms.openlocfilepath>articles\dev-itpro\sysadmin\activeperiod.md</xliffext:ms.openlocfilepath>
    </header>
    <body>
      <group extype="content" id="content">
        <trans-unit xml:space="preserve" translate="yes" id="101" restype="x-metadata">
          <source>Active batch periods</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">有効なバッチ期間</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="102" restype="x-metadata">
          <source>This topic provides information about setting up and working with active batch periods in Microsoft Dynamics 365 for Finance and Operations.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このトピックでは、Microsoft Dynamics 365 for Finance and Operations の有効なバッチ期間のセットアップおよび作業に関する情報を説明します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="103">
          <source>Active batch periods</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">有効なバッチ期間</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="104">
          <source>With the release of Platform update 21, an additional level of control over when batch jobs execute is now available.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">プラットフォーム更新 21 のリリースでは、バッチ ジョブがいつ実行されるかの制御の追加レベルが使用できるようになりました。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="105">
          <source>Previously, it was only possible to schedule a batch job to execute every hour for a specified number of hours or until a given date.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">以前は、一定の時間数または特定の日付までの 1 時間ごとにバッチ ジョブが実行されるようにスケジュールすることのみ可能でした。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="106">
          <source>Administrators can now provide information for an additional active period, such as in the following scenarios:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">管理者は、次のシナリオなど、追加のアクティブ期間の情報を指定できるようになりました。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="107">
          <source>Specifying time ranges during which jobs within a batch group can start execution.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">バッチ グループ内のジョブが実行を開始できる期間を指定します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="108">
          <source>Selecting to run batch jobs outside of office hours only.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">営業時間外にのみバッチ ジョブを実行する場合に選択します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="109">
          <source>Setting the recurrence for anytime within the active period.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">アクティブ期間内で任意の回数の繰り返しを設定します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="110">
          <source>For example, you administrator might select to run the batch jobs every hour, but only between the hours of 6:00 PM and 8:00 AM.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">たとえば、管理者は、午後 6 時から午前 8 時の間のみ、毎時間バッチ ジョブを実行することを選択できます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="111">
          <source>This feature is available as of Platform update 21.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この機能は、Platform update 21 以降で利用できます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="112">
          <source>Set up active periods for batch jobs</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">バッチ ジョブの有効期間の設定</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="113">
          <source>Go to <bpt id="p1">**</bpt>System administration<ept id="p1">**</ept><ph id="ph1"> &gt; </ph><bpt id="p2">**</bpt>Setup<ept id="p2">**</ept><ph id="ph2"> &gt; </ph><bpt id="p3">**</bpt>Active periods for batch jobs<ept id="p3">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>システム管理<ept id="p1">**</ept><ph id="ph1"> &gt; </ph><bpt id="p2">**</bpt>設定<ept id="p2">**</ept><ph id="ph2"> &gt; </ph><bpt id="p3">**</bpt>バッチ ジョブの有効期間<ept id="p3">**</ept> に移動します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="114">
          <source>Enter the name of the batch job, and specify start and end dates that the batch job is active.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">バッチ ジョブの名前を入力し、バッチ ジョブが有効な開始日と終了日を指定します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="115">
          <source>Click <bpt id="p1">**</bpt>Save<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>保存<ept id="p1">**</ept> をクリックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="116">
          <source>Active Period Form</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">有効期間フォーム</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="117">
          <source>Assign active periods to batch jobs</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">バッチ ジョブの有効期間の割り当て</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="118">
          <source>Go to <bpt id="p1">**</bpt>System administration<ept id="p1">**</ept><ph id="ph1"> &gt; </ph><bpt id="p2">**</bpt>Inquiries<ept id="p2">**</ept><ph id="ph2"> &gt; </ph><bpt id="p3">**</bpt>Batch jobs<ept id="p3">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>システム管理<ept id="p1">**</ept><ph id="ph1"> &gt; </ph><bpt id="p2">**</bpt>照会<ept id="p2">**</ept><ph id="ph2"> &gt; </ph><bpt id="p3">**</bpt>バッチ ジョブ<ept id="p3">**</ept> の順に移動します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="119">
          <source>Select the batch job that you want to assign a period to, and click <bpt id="p1">**</bpt>Edit<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">期間を割り当てるバッチ ジョブを選択し、<bpt id="p1">**</bpt>編集<ept id="p1">**</ept> をクリックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="120">
          <source>In the <bpt id="p1">**</bpt>Active period<ept id="p1">**</ept> field, select the active period that you want to assign, and then click <bpt id="p2">**</bpt>Save<ept id="p2">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>有効期間<ept id="p1">**</ept> フィールドで、割り当てる有効期間を選択し、<bpt id="p2">**</bpt>保存<ept id="p2">**</ept> をクリックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="121">
          <source>Assign Active Period</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">有効期間の割り当て</target></trans-unit>
      </group>
    </body>
  </file>
</xliff>