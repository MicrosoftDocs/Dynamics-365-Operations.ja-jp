<?xml version="1.0" encoding="UTF-8"?>
<xliff xmlns:logoport="urn:logoport:xliffeditor:xliff-extras:1.0" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns="urn:oasis:names:tc:xliff:document:1.2" xmlns:xliffext="urn:microsoft:content:schema:xliffextensions" version="1.2" xsi:schemaLocation="urn:oasis:names:tc:xliff:document:1.2 xliff-core-1.2-transitional.xsd">
  <file datatype="xml" source-language="en-US" original="batch-job-SQL-defragmentation.md" target-language="ja-JP">
    <header>
      <tool tool-company="Microsoft" tool-version="1.0-7889195" tool-name="mdxliff" tool-id="mdxliff"/>
      <xliffext:skl_file_name>batch-job-SQL-defragmentation.72991d.c02a91b9c8d2e5943b2c4945769e86a6abdda0a6.skl</xliffext:skl_file_name>
      <xliffext:version>1.2</xliffext:version>
      <xliffext:ms.openlocfilehash>c02a91b9c8d2e5943b2c4945769e86a6abdda0a6</xliffext:ms.openlocfilehash>
      <xliffext:ms.sourcegitcommit>9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b</xliffext:ms.sourcegitcommit>
      <xliffext:ms.lasthandoff>05/15/2019</xliffext:ms.lasthandoff>
      <xliffext:ms.openlocfilepath>articles\dev-itpro\sysadmin\batch-job-SQL-defragmentation.md</xliffext:ms.openlocfilepath>
    </header>
    <body>
      <group extype="content" id="content">
        <trans-unit xml:space="preserve" translate="yes" id="101" restype="x-metadata">
          <source>Batch job to handle SQL index defragmentation</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">SQL インデックスの最適化を処理するバッチ ジョブ</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="102" restype="x-metadata">
          <source>This topic describes a system batch job that is used to rebuild fragmented indexes.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このトピックでは、分割されたインデックスを再構築するために使用するシステム バッチ ジョブを説明します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="103">
          <source>Batch job to handle SQL index defragmentation</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">SQL インデックスの最適化を処理するバッチ ジョブ</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="104">
          <source>In Platform update 22, a new system batch job has been introduced to rebuild fragmented indexes.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">プラットフォーム更新プログラム 22 では、断片化したインデックスを再構築する新しいシステム バッチ ジョブが導入されました。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="105">
          <source>Index fragmentation results in notable performance degradation in specific scenarios.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">インデックスの断片化により、固有のシナリオでパフォーマンスが著しく低下します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="106">
          <source>To address fragmentation issues and keep the database in a top-performing state, this batch job will rebuild highly fragmented indexes periodically at a scheduled time.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">断片化の問題に対処し、データベースを最高のパフォーマンス状態に維持するため、このバッチ ジョブはスケジュールされた時間に定期的に激しく断片化したインデックスを再構築します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="107">
          <source>By default, the job scheduled to run at 3:00 AM local time every day for a maximum of 2 hours.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">既定では、そのジョブは毎日現地時間の午前 3:00 に最大 2 時間実行されるようにスケジュールされます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="108">
          <source>If the batch job finds that not many fragmented indexes need to be rebuilt, it will complete early.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">再構築する必要がある断片化されたインデックスが多くないとバッチ ジョブが判断した場合は早期に完了します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="109">
          <source>This system job cannot be canceled.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このシステム ジョブは変更できません</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="110">
          <source>You can change the schedule and its recurrence if you want to run it weekly.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">週 1 回実行する場合は、スケジュールと頻度を変更できます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="111">
          <source>System jobs are expected to run at least once a week.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">システム ジョブは、週 1 回以上実行する必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="112">
          <source>You can change the parameter values on the <bpt id="p1">**</bpt>Adjust system job parameters<ept id="p1">**</ept> page to denote how long the job can run and how many indexes it should target, at a maximum.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>システム ジョブ パラメーターを調整<ept id="p1">**</ept> ページでパラメータの値を変更し、ジョブを実行できる期間とターゲットとできるインデックスの数を最大値で指定できます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="113">
          <source>The DTU threshold is to prevent this job from starting when the system is busy.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">DTU しきい値は、システムがビジー状態のときにこのジョブが開始するのを防ぎます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="114">
          <source>The default DTU threshold is 50,  which means that if the system is using 50 percent or more DTU during the time that the index rebuild job is scheduled to run, the job exit early without rebuilding any indexes.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">既定の DTU しきい値が 50 の場合、つまりインデックスがジョブの再構築をスケジュールされているときにシステムが 50% 以上の DTU を使用している場合、ジョブはインデックスを再構築しないで早期に終了します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="115">
          <source><bpt id="p1">![</bpt>Screenshot of Adjust system job parameters page<ept id="p1">]</ept><bpt id="p2">(media/SystemJobParameters.PNG "</bpt>Screenshot of Adjust system job parameters page<ept id="p2">")</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">![</bpt>システム ジョブ調整パラメータ ページのスクリーンショット<ept id="p1">]</ept><bpt id="p2">(media/SystemJobParameters.PNG "</bpt>システム ジョブ調整パラメータ ページのスクリーンショット<ept id="p2">")</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="116">
          <source>When this job is executing, there could be some impact on the following:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このジョブを実行すると、以下に影響を与える可能性があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="117">
          <source>The time that it takes SQL resources to process.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">SQL リソースの処理にかかる時間。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="118">
          <source>There may be blocking,</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ブロックされる場合があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="119">
          <source>Change the default scheduled time/recurrence</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">スケジュールされた既定の時間/頻度の変更</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="120">
          <source>Go to <bpt id="p1">**</bpt>System administration &gt; Inquiries &gt; Batch Jobs<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>システム管理 &gt; 照会 &gt; バッチ ジョブ<ept id="p1">**</ept> の順に移動します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="121">
          <source>Search for a job description that contains <bpt id="p1">*</bpt>index rebuild<ept id="p1">*</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">*</bpt>インデックスの再構築<ept id="p1">*</ept>を含むジョブの説明を検索します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="122">
          <source>Select the record.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">レコードを選択します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="123">
          <source>Click the menu item <bpt id="p1">**</bpt>Batch Job &gt; Recurrence<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">メニュー項目<bpt id="p1">**</bpt>バッチ ジョブ &gt; 再実行<ept id="p1">**</ept>をクリックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="124">
          <source>Change the schedule time and recurrence to suit your schedule.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">スケジュールに合うようにスケジュール時間と頻度を変更します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="125">
          <source>The results of index rebuild can be found by going to <bpt id="p1">**</bpt>System administration &gt; Inquiries &gt; Database &gt; SQL index fragmentation details<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">インデックス再構築の結果は、<bpt id="p1">**</bpt>システム管理 &gt; 照会 &gt; データベース &gt; SQLインデックスの断片化の詳細<ept id="p1">**</ept>にあります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="126">
          <source>In some cases, you may find that the before and after fragmentation number is the same or even higher.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">場合によっては、断片化の前後で番号が同じであるかそれ以上であることがあります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="127">
          <source>This is typical because Microsoft uses a less intrusive online rebuild option.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">これは、Microsoft が侵入型オンライン再構築オプションを使用しているため通常です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="128">
          <source>In the future, we plan to introduce an optional offline rebuild option.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">今後、オプションのオフライン再構築オプションの導入を計画しています。</target></trans-unit>
      </group>
    </body>
  </file>
</xliff>