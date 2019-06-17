<?xml version="1.0" encoding="UTF-8"?>
<xliff xmlns:logoport="urn:logoport:xliffeditor:xliff-extras:1.0" xmlns:tilt="urn:logoport:xliffeditor:tilt-non-translatables:1.0" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns="urn:oasis:names:tc:xliff:document:1.2" xmlns:xliffext="urn:microsoft:content:schema:xliffextensions" version="1.2" xsi:schemaLocation="urn:oasis:names:tc:xliff:document:1.2 xliff-core-1.2-transitional.xsd">
  <file datatype="xml" source-language="en-US" original="startup-customizations.md" target-language="ja-JP">
    <header>
      <tool tool-company="Microsoft" tool-version="1.0-7889195" tool-name="mdxliff" tool-id="mdxliff"/>
      <xliffext:skl_file_name>startup-customizations.001c55.cda6f533e01b6bf25a8f0ac9202cc8aa2ea1b979.skl</xliffext:skl_file_name>
      <xliffext:version>1.2</xliffext:version>
      <xliffext:ms.openlocfilehash>cda6f533e01b6bf25a8f0ac9202cc8aa2ea1b979</xliffext:ms.openlocfilehash>
      <xliffext:ms.sourcegitcommit>9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b</xliffext:ms.sourcegitcommit>
      <xliffext:ms.lasthandoff>05/15/2019</xliffext:ms.lasthandoff>
      <xliffext:ms.openlocfilepath>articles\dev-itpro\extensibility\startup-customizations.md</xliffext:ms.openlocfilepath>
    </header>
    <body>
      <group extype="content" id="content">
        <trans-unit xml:space="preserve" translate="yes" id="101" restype="x-metadata">
          <source>Customize application startup by using delegates</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">デリゲートを使用してアプリケーション起動をカスタマイズする</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="102" restype="x-metadata">
          <source>This topic explains how you can add new data sources to existing forms by using extensions.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このトピックでは、拡張機能を使用して、既存のフォームに新しいデータ ソースを追加する方法について説明します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="103">
          <source>Customize application startup by using delegates</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">デリゲートを使用してアプリケーション起動をカスタマイズする</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="104">
          <source>In Dynamics AX 2012, there were customization points that allowed you to subscribe to events (Application.Startup delegates) that were raised when the client was initializing.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Dynamics AX 2012 では、クライアントが初期化中に発生したイベント (Application.Startup デリゲート) をサブスクライブできるカスタマイズ ポイントがありました。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="105">
          <source>In Dynamics 365 for Finance and Operations, these events were deprecated because there is no concept of a rich client.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Dynamics 365 for Finance and Operations では、これらのイベントはリッチ クライアントの概念がないため推奨されません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="106">
          <source>On the server, only server sessions are considered, however because you can migrate logic from previous releases, new events have been added to the <bpt id="p1">**</bpt>ApplicationStartupEventManager<ept id="p1">**</ept> class.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">サーバーで、サーバー セッションのみが考慮されますが、以前のリリースからロジックを移行できるため、新しいイベントが <bpt id="p1">**</bpt>ApplicationStartupEventManager<ept id="p1">**</ept> クラスに追加されました。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="107">
          <source>The following sections highlight the new data sources that you can add to existing forms by using extensions.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">次のセクションでは、拡張機能を使用して既存のフォームに追加できる新しいデータ ソースについて説明します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="108">
          <source>static delegate void onSystemStartup()</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">static delegate void onSystemStartup()</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="109">
          <source>This event occurs when the system starts up.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このイベントは、システムの起動時に発生します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="110">
          <source>It is raised once per AOS upon startup.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">これは起動時に AOS につき 1 回発生します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="111">
          <source>static delegate void onFirstTimeUserInteractiveSessionCreated()</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">static delegate void onFirstTimeUserInteractiveSessionCreated()</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="112">
          <source>This event occurs when the system is creating an interactive session for the first time for a user.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このイベントは、ユーザーが初めてインタラクティブ セッションを作成しているときに発生します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="113">
          <source>It is raised once per user per AOS.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">これは AOS ごとのユーザーにつき 1 回発生します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="114">
          <source>static delegate void onFirstTimeUserNonInteractiveSessionCreated()</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">static delegate void onFirstTimeUserNonInteractiveSessionCreated()</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="115">
          <source>This event occurs when the system is creating a non-interactive session for the first time for a user.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このイベントは、ユーザーが初めて非インタラクティブ セッションを作成しているときに発生します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="116">
          <source>It is raised once per user per AOS.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">これは AOS ごとのユーザーにつき 1 回発生します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="117">
          <source>static delegate void onInteractiveSessionCreated()</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">static delegate void onInteractiveSessionCreated()</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="118">
          <source>This event occurs when an interactive session is created and ready for use.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このイベントは、インタラクティブ セッションが作成され、使用できる状態になったときに発生します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="119">
          <source>It is raised once per interactive session creation for any user.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">これは、すべてのユーザーのインタラクティブ セッション作成につき 1 回発生します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="120">
          <source>static delegate void onSessionCreated(boolean _isBatch, boolean _isInteractive)</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">static delegate void onSessionCreated(boolean _isBatch, boolean _isInteractive)</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="121">
          <source>This event occurs when the session is created and ready for use.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このイベントは、セッションが作成され、使用できる状態になったときに発生します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="122">
          <source>It is raised once per interactive session creation for any user.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">これは、すべてのユーザーのインタラクティブ セッション作成につき 1 回発生します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="123">
          <source><bpt id="p1">*</bpt>_isBatch<ept id="p1">*</ept> specifies whether the system is running a batch job.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">*</bpt>_isBatch<ept id="p1">*</ept> はシステムがバッチ ジョブを実行しているかどうかを指定します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="124">
          <source><bpt id="p1">*</bpt>_isInteractive<ept id="p1">*</ept> specifies whether the session is interactive.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">*</bpt>_isInteractive<ept id="p1">*</ept> はセッションが対話型であるかを指定します。</target></trans-unit>
      </group>
    </body>
  </file>
</xliff>