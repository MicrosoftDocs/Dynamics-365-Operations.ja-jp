<?xml version="1.0" encoding="UTF-8"?>
<xliff xmlns:logoport="urn:logoport:xliffeditor:xliff-extras:1.0" xmlns:tilt="urn:logoport:xliffeditor:tilt-non-translatables:1.0" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns="urn:oasis:names:tc:xliff:document:1.2" xmlns:xliffext="urn:microsoft:content:schema:xliffextensions" version="1.2" xsi:schemaLocation="urn:oasis:names:tc:xliff:document:1.2 xliff-core-1.2-transitional.xsd">
  <file datatype="xml" source-language="en-US" original="user-logins.md" target-language="ja-JP">
    <header>
      <tool tool-company="Microsoft" tool-version="1.0-7889195" tool-name="mdxliff" tool-id="mdxliff"/>
      <xliffext:skl_file_name>user-logins.33d3ca.42010539b63c582bfd4729175ecf8e06663bb274.skl</xliffext:skl_file_name>
      <xliffext:version>1.2</xliffext:version>
      <xliffext:ms.openlocfilehash>42010539b63c582bfd4729175ecf8e06663bb274</xliffext:ms.openlocfilehash>
      <xliffext:ms.sourcegitcommit>9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b</xliffext:ms.sourcegitcommit>
      <xliffext:ms.lasthandoff>05/15/2019</xliffext:ms.lasthandoff>
      <xliffext:ms.openlocfilepath>articles\dev-itpro\lifecycle-services\user-logins.md</xliffext:ms.openlocfilepath>
    </header>
    <body>
      <group extype="content" id="content">
        <trans-unit xml:space="preserve" translate="yes" id="101" restype="x-metadata">
          <source>Track user sign-ins</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ユーザー サインインの追跡</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="102" restype="x-metadata">
          <source>This topic explains how to create an audit log of users who have signed in and used Microsoft Dynamics 365 for Finance and Operations.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このトピックでは、Microsoft Dynamics 365 for Finance and Operations にサインインして使用するユーザーの監査ログを作成する方法について説明します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="103">
          <source>Track user sign-ins</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ユーザー サインインの追跡</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="104">
          <source>Many organizations are required to maintain an audit trail of users who have used the system.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">多くの組織は、システムを使用したユーザーの監査証跡を管理する必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="105">
          <source>This requirement can be in place for compliance reasons, or to enable trackbacks in the event of incorrect use.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この要件は、コンプライアンス上の理由から、または不適切な使用が発生した場合にトラックバックを有効にできます。 </target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="106">
          <source>In Microsoft Dynamics AX 2012, the <bpt id="p1">**</bpt>Audit log<ept id="p1">**</ept> form recorded which users accessed the Microsoft Dynamics AX environment.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Microsoft Dynamics AX 2012 では、<bpt id="p1">**</bpt>監査ログ<ept id="p1">**</ept>フォームが Microsoft Dynamics AX 環境にアクセスしたユーザーを記録していました。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="107">
          <source>In Microsoft Dynamics 365 for Finance and Operations, this information is captured in telemetry.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Microsoft Dynamics 365 for Finance and Operations では、この情報はテレメトリでキャプチャされます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="108">
          <source>IT administrators can download this information by using Microsoft Dynamics Lifecycle Services (LCS) and then move it to offline storage to maintain the audit trail of users who have signed in.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">IT 管理者は、Microsoft Dynamics Lifecycle Services (LCS) を使用して、この情報をダウンロードし、サインインしているユーザーの監査証跡を維持するためにオフライン ストレージに移動することができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="109">
          <source>To generate an audit log of users who have used the system, follow these steps.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">システムを使用したユーザーの監査ログを生成するには、次の手順を実行します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="110">
          <source>Sign in to LCS, and open the project that is associated with the Finance and Operations implementation.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">LCS にサインインし、Finance and Operations 実装に関連付けられているプロジェクトを開きます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="111">
          <source>Navigate to the production environment, and open the <bpt id="p1">**</bpt>Environment details<ept id="p1">**</ept> page.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">実稼働環境に移動して、<bpt id="p1">**</bpt>環境の詳細<ept id="p1">**</ept>ページを開きます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="112">
          <source>On the <bpt id="p1">**</bpt>Monitoring<ept id="p1">**</ept> tab, select the <bpt id="p2">**</bpt>Environment monitoring<ept id="p2">**</ept> link to open the monitoring dashboard.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>監視<ept id="p1">**</ept>タブで、<bpt id="p2">**</bpt>環境の監視<ept id="p2">**</ept>リンクを選択して、監視ダッシュボードを開きます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="113">
          <source>On the <bpt id="p1">**</bpt>Activity<ept id="p1">**</ept> tab, select <bpt id="p2">**</bpt>View raw logs<ept id="p2">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>活動<ept id="p1">**</ept>タブで、<bpt id="p2">**</bpt>未加工のログの表示<ept id="p2">**</ept>を選択します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="114">
          <source>In the <bpt id="p1">**</bpt>Query<ept id="p1">**</ept> field, select <bpt id="p2">**</bpt>User Login Events<ept id="p2">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>クエリ<ept id="p1">**</ept> フィールドで、<bpt id="p2">**</bpt>ユーザー ログイン イベント<ept id="p2">**</ept>を選択します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="115">
          <source>You see a time duration that has a start date that is set to <bpt id="p1">**</bpt>End date - 7 days<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">開始日が <bpt id="p1">**</bpt>終了日 - 7日<ept id="p1">**</ept> に設定されている期間を参照します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="116">
          <source>Set the end date, and then select <bpt id="p1">**</bpt>Search<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">終了日を設定し、<bpt id="p1">**</bpt>検索<ept id="p1">**</ept> を選択します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="117">
          <source>The search results that are returned include all users who signed in to the system during the seven days before the selected end date.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">返される検索結果には、選択した終了日より 7 日前にシステムにサインインしたすべてのユーザーが含まれます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="118">
          <source>The search results show the <bpt id="p1">**</bpt>AADUserID<ept id="p1">**</ept> value and the sign-in start and end times of the user's session.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">検索結果には、ユーザーのセッションの <bpt id="p1">**</bpt>AADUserID<ept id="p1">**</ept> 値と、サインインの開始時刻と終了時刻が表示されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="119">
          <source>To map the <bpt id="p1">**</bpt>AADUserID<ept id="p1">**</ept> value to the user's user name and email address, use the <bpt id="p2">**</bpt>Users<ept id="p2">**</ept> page in Finance and Operations (<bpt id="p3">**</bpt>System administration<ept id="p3">**</ept><ph id="ph1"> &gt; </ph><bpt id="p4">**</bpt>Users<ept id="p4">**</ept>).</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>AADUserID<ept id="p1">**</ept>の値をユーザーのユーザー名と電子メールアドレスにマップするには、Finance and Operations の <bpt id="p2">**</bpt>ユーザー<ept id="p2">**</ept> ページ (<bpt id="p3">**</bpt>システム管理<ept id="p3">**</ept><ph id="ph1"> &gt; </ph><bpt id="p4">**</bpt>ユーザー<ept id="p4">**</ept>) を使用します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="120">
          <source>To export the records and keep them for a longer period, select <bpt id="p1">**</bpt>Export grid<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">レコードをエクスポートして長期間保存するには、<bpt id="p1">**</bpt>エクスポート グリッド<ept id="p1">**</ept> を選択します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="121">
          <source>To help guarantee a complete audit trail, an IT administrator must complete this procedure every seven days.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">完全な監査証跡を保証するために、IT 管理者は 7 日ごとにこの手順を完了する必要があります。</target></trans-unit>
      </group>
    </body>
  </file>
</xliff>