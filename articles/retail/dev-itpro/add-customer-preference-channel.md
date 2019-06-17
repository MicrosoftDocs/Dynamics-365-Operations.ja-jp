<?xml version="1.0" encoding="UTF-8"?>
<xliff xmlns:logoport="urn:logoport:xliffeditor:xliff-extras:1.0" xmlns:tilt="urn:logoport:xliffeditor:tilt-non-translatables:1.0" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns="urn:oasis:names:tc:xliff:document:1.2" xmlns:xliffext="urn:microsoft:content:schema:xliffextensions" version="1.2" xsi:schemaLocation="urn:oasis:names:tc:xliff:document:1.2 xliff-core-1.2-transitional.xsd">
  <file datatype="xml" source-language="en-US" original="add-customer-preference-channel.md" target-language="ja-JP">
    <header>
      <tool tool-company="Microsoft" tool-version="1.0-7889195" tool-name="mdxliff" tool-id="mdxliff"/>
      <xliffext:skl_file_name>add-customer-preference-channel.a84ae2.3828997488c7e9f770dd8da6e8b906ea58600b51.skl</xliffext:skl_file_name>
      <xliffext:version>1.2</xliffext:version>
      <xliffext:ms.openlocfilehash>3828997488c7e9f770dd8da6e8b906ea58600b51</xliffext:ms.openlocfilehash>
      <xliffext:ms.sourcegitcommit>9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b</xliffext:ms.sourcegitcommit>
      <xliffext:ms.lasthandoff>05/15/2019</xliffext:ms.lasthandoff>
      <xliffext:ms.openlocfilepath>articles\retail\dev-itpro\add-customer-preference-channel.md</xliffext:ms.openlocfilepath>
    </header>
    <body>
      <group extype="content" id="content">
        <trans-unit xml:space="preserve" translate="yes" id="101" restype="x-metadata">
          <source>Add customer preference data to channel databases</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">顧客の基本設定データをチャネル データベースに追加</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="102" restype="x-metadata">
          <source>This tutorial shows how to add the RetailCustPreferences table to the commerce runtime (CRT) for the retail channel, and how to create a subjob to move the data in the new table to the channel database.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このチュートリアルでは、RetailCustPreferences テーブルを小売チャネルのコマース ランタイム (CRT) に追加する方法と、新しいテーブルのデータをチャネル データベースに移動するサブジョブを作成する方法を示します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="103">
          <source>Add customer preference data to channel databases</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">顧客の基本設定データをチャネル データベースに追加</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="104">
          <source>This topic is applicable for Dynamics 365 for Finance and Operations version 7.1 and earlier.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このトピックは、Dynamics 365 for Finance and Operations バージョン 7.1 およびそれ以前のバージョンに適用されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="105">
          <source>This implementation is not supported for versions 7.2 and higher.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">バージョン 7.2 およびそれ以上の場合は、この実装はサポートされていません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="106">
          <source>For those versions, follow the extension model without overlayering.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">これらのバージョンでは、オーバーレイせずに拡張モデルに従います。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="107">
          <source>This tutorial shows how to add the RetailCustPreferences table to the commerce runtime (CRT) for the retail channel, and how to create a subjob to move the data in the new table to the channel database.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このチュートリアルでは、RetailCustPreferences テーブルを小売チャネルのコマース ランタイム (CRT) に追加する方法と、新しいテーブルのデータをチャネル データベースに移動するサブジョブを作成する方法を示します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="108">
          <source>Add the RetailCustPreferences table in the data distribution to the CRT for the retail channel</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">小売チャネルの CRT へのデータ配布での RetailCustPreferences テーブルの追加</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="109">
          <source>The channel schema is the XML description of the data that is sent to the channel database.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">チャネル スキーマは、チャネル データベースに送信されるデータの XML 記述です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="110">
          <source>Click <bpt id="p1">**</bpt>Retail<ept id="p1">**</ept> <ph id="ph1">&amp;gt;</ph> <bpt id="p2">**</bpt>Headquarters setup<ept id="p2">**</ept> <ph id="ph2">&amp;gt;</ph> <bpt id="p3">**</bpt>Retail scheduler<ept id="p3">**</ept> <ph id="ph3">&amp;gt;</ph> <bpt id="p4">**</bpt>Retail channel schema<ept id="p4">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>小売<ept id="p1">**</ept> <ph id="ph1">&amp;gt;</ph> <bpt id="p2">**</bpt>本社の設定<ept id="p2">**</ept> <ph id="ph2">&amp;gt;</ph> <bpt id="p3">**</bpt>小売用スケジューラ<ept id="p3">**</ept> <ph id="ph3">&amp;gt;</ph> <bpt id="p4">**</bpt>小売チャネル スキーマ<ept id="p4">**</ept>の順にクリックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="111">
          <source>Select the schema name that corresponds to the channel.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">チャネルに対応するスキーマ名を選択します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="112">
          <source>Then click <bpt id="p1">**</bpt>Channel tables<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">その後、<bpt id="p1">**</bpt>チャネル テーブル<ept id="p1">**</ept> をクリックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="113">
          <source>Click <bpt id="p1">**</bpt>New<ept id="p1">**</ept>, and then, in the <bpt id="p2">**</bpt>Table name<ept id="p2">**</ept> field, enter <bpt id="p3">**</bpt>ax.RetailCustPreference<ept id="p3">**</ept> as the name of the new table.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>新規<ept id="p1">**</ept>をクリックし、<bpt id="p2">**</bpt>テーブル名<ept id="p2">**</ept>フィールドに、新しいテーブルの名前として <bpt id="p3">**</bpt>ax.RetailCustPreference<ept id="p3">**</ept> を入力します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="114">
          <source>On the <bpt id="p1">**</bpt>Channel table fields<ept id="p1">**</ept> tab, click <bpt id="p2">**</bpt>New<ept id="p2">**</ept>, and then enter the field names <bpt id="p3">**</bpt>ACCOUNTNUM<ept id="p3">**</ept>, <bpt id="p4">**</bpt>EMAILOPTIN<ept id="p4">**</ept>, and <bpt id="p5">**</bpt>RECID<ept id="p5">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>チャネル テーブル フィールド<ept id="p1">**</ept>タブで、<bpt id="p2">**</bpt>新規<ept id="p2">**</ept>をクリックし、フィールド名 <bpt id="p3">**</bpt>ACCOUNTNUM<ept id="p3">**</ept>、<bpt id="p4">**</bpt>EMAILOPTIN<ept id="p4">**</ept>、および <bpt id="p5">**</bpt>RECID<ept id="p5">**</ept> を入力します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="115">
          <source>Close the <bpt id="p1">**</bpt>Channel tables<ept id="p1">**</ept> page.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>チャネル テーブル<ept id="p1">**</ept> ページを閉じます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="116">
          <source>Create a subjob</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">サブジョブの作成</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="117">
          <source>Next, you create a subjob of the CustTable job to move data in the new table to the channel database.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">次に、チャネル データベースに新しいテーブルのデータを移動するために、CustTable ジョブのサブジョブを作成します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="118">
          <source>In Retail Headquarters, click <bpt id="p1">**</bpt>Retail<ept id="p1">**</ept> <ph id="ph1">&amp;gt;</ph> <bpt id="p2">**</bpt>Headquarters setup<ept id="p2">**</ept> <ph id="ph2">&amp;gt;</ph> <bpt id="p3">**</bpt>Retail scheduler<ept id="p3">**</ept> <ph id="ph3">&amp;gt;</ph> <bpt id="p4">**</bpt>Scheduler subjobs<ept id="p4">**</ept>, and then click <bpt id="p5">**</bpt>New<ept id="p5">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Retail Headquarters で <bpt id="p1">**</bpt>小売<ept id="p1">**</ept> <ph id="ph1">&amp;gt;</ph> <bpt id="p2">**</bpt>本社の設定<ept id="p2">**</ept> <ph id="ph2">&amp;gt;</ph> <bpt id="p3">**</bpt>小売用スケジューラ<ept id="p3">**</ept> <ph id="ph3">&amp;gt;</ph> <bpt id="p4">**</bpt>スケジューラ サブジョブ<ept id="p4">**</ept> とクリックして、そして <bpt id="p5">**</bpt>新規<ept id="p5">**</ept> をクリックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="119">
          <source>In the <bpt id="p1">**</bpt>Subjob number<ept id="p1">**</ept> and <bpt id="p2">**</bpt>Description<ept id="p2">**</ept> fields, enter <bpt id="p3">**</bpt>RetailCustPreference<ept id="p3">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>サブジョブ番号<ept id="p1">**</ept>および<bpt id="p2">**</bpt>説明<ept id="p2">**</ept>フィールドに <bpt id="p3">**</bpt>RetailCustPreference<ept id="p3">**</ept> を入力します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="120">
          <source>In the <bpt id="p1">**</bpt>Retail channel schema<ept id="p1">**</ept> field, select <bpt id="p2">**</bpt>Dynamics 365 for Retail.<ept id="p2">**</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>小売チャネル スキーマ<ept id="p1">**</ept> フィールドで、<bpt id="p2">**</bpt>Dynamics 365 for Retail<ept id="p2">**</ept> を選択します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="121">
          <source>In the <bpt id="p1">**</bpt>Channel table name<ept id="p1">**</ept> field, select <bpt id="p2">**</bpt>ax.RetailCustPreference<ept id="p2">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>チャネル テーブル名<ept id="p1">**</ept>フィールドで、<bpt id="p2">**</bpt>ax.RetailCustPreference<ept id="p2">**</ept> を選択します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="122">
          <source>In the <bpt id="p1">**</bpt>table name<ept id="p1">**</ept> field, select <bpt id="p2">**</bpt>RetailCustPreference<ept id="p2">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>テーブル名<ept id="p1">**</ept>フィールドで、<bpt id="p2">**</bpt>RetailCustPreference<ept id="p2">**</ept> を選択します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="123">
          <source>On the <bpt id="p1">**</bpt>Channel field mapping<ept id="p1">**</ept> tab, click <bpt id="p2">**</bpt>Match fields<ept id="p2">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>チャネル フィールド マッピング<ept id="p1">**</ept>タブで、<bpt id="p2">**</bpt>フィールドの照合<ept id="p2">**</ept>をクリックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="124">
          <source>The <bpt id="p1">**</bpt>From<ept id="p1">**</ept> field and <bpt id="p2">**</bpt>To<ept id="p2">**</ept> field columns are filled in.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>開始<ept id="p1">**</ept> フィールドと <bpt id="p2">**</bpt>終了<ept id="p2">**</ept> フィールドの列に入力されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="125">
          <source><bpt id="p1">**</bpt>Alternative approach, instead of using the UI in the steps above this can also accomplished in code:<ept id="p1">**</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>上記の手順で UI を使用する代わりに、代替方法として、コードで実行することもできます。<ept id="p1">**</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="126">
          <source>Start Microsoft Visual Studio, and then, in the Application Object Tree (AOT) find the <bpt id="p1">**</bpt>RetailCDXSeedData<ph id="ph1">\_</ph>AX7<ept id="p1">**</ept> class.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Microsoft Visual Studio を起動してから、アプリケーション オブジェクト ツリー (AOT) で <bpt id="p1">**</bpt>RetailCDXSeedData<ph id="ph1">\_</ph>AX7<ept id="p1">**</ept> クラスを見つけます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="127">
          <source>Add the following method.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">次のメソッドを追加します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="128">
          <source>Compile the class.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">クラスをコンパイルします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="129">
          <source>Reset Internet Information Services (IIS).</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">インターネット インフォメーション サービス (IIS) をリセットします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="130">
          <source>Switch to the client.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">クライアントに切り替えます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="131">
          <source>Click <bpt id="p1">**</bpt>Retail<ept id="p1">**</ept> <ph id="ph1">&amp;gt;</ph> <bpt id="p2">**</bpt>Headquarters setup<ept id="p2">**</ept> <ph id="ph2">&amp;gt;</ph> <bpt id="p3">**</bpt>Retail scheduler<ept id="p3">**</ept> <ph id="ph3">&amp;gt;</ph> <bpt id="p4">**</bpt>Initialize retail scheduler<ept id="p4">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>小売<ept id="p1">**</ept> <ph id="ph1">&amp;gt;</ph> <bpt id="p2">**</bpt>本社の設定<ept id="p2">**</ept> <ph id="ph2">&amp;gt;</ph> <bpt id="p3">**</bpt>小売用スケジューラ<ept id="p3">**</ept> <ph id="ph3">&amp;gt;</ph> <bpt id="p4">**</bpt>小売用スケジューラの初期化<ept id="p4">**</ept>の順にクリックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="132">
          <source>The required scheduler subjob definition is generated, and the subjob is added to the scheduler job.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">必要なスケジューラ サブジョブ定義が生成され、サブジョブがスケジューラ ジョブに追加されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="133">
          <source>Click <bpt id="p1">**</bpt>Retail<ept id="p1">**</ept> <ph id="ph1">&amp;gt;</ph> <bpt id="p2">**</bpt>Headquarters setup<ept id="p2">**</ept> <ph id="ph2">&amp;gt;</ph> <bpt id="p3">**</bpt>Retail scheduler<ept id="p3">**</ept> <ph id="ph3">&amp;gt;</ph> <bpt id="p4">**</bpt>Retail channel schema<ept id="p4">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>小売<ept id="p1">**</ept> <ph id="ph1">&amp;gt;</ph> <bpt id="p2">**</bpt>本社の設定<ept id="p2">**</ept> <ph id="ph2">&amp;gt;</ph> <bpt id="p3">**</bpt>小売用スケジューラ<ept id="p3">**</ept> <ph id="ph3">&amp;gt;</ph> <bpt id="p4">**</bpt>小売チャネル スキーマ<ept id="p4">**</ept>の順にクリックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="134">
          <source>On the <bpt id="p1">**</bpt>Retail channel schema<ept id="p1">**</ept> page, in the left navigation pane, click <bpt id="p2">**</bpt>Dynamics 365 for Retail.<ept id="p2">**</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>小売チャンネル スキーマ<ept id="p1">**</ept> ページの、左側のナビゲーション ウィンドウで、<bpt id="p2">**</bpt>Dynamics 365 for Retail<ept id="p2">**</ept> をクリックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="135">
          <source>On the <bpt id="p1">**</bpt>Retail data distribution<ept id="p1">**</ept> tab, click <bpt id="p2">**</bpt>Export<ept id="p2">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>小売データの配布<ept id="p1">**</ept>タブで、<bpt id="p2">**</bpt>エクスポート<ept id="p2">**</ept>をクリックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="136">
          <source>Follow one of these steps, depending on the browser that you're using:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">使用しているブラウザーに応じて、次のいずれかのステップを実行します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="137">
          <source>If you're using Google Chrome, you should be prompted to download an XML file.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Google Chrome を使用している場合は、XML ファイルをダウンロードするように求められる必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="138">
          <source>Save the file to a path.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ファイルをパスに保存します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="139">
          <source>If you're using Internet Explorer, a webpage will open.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Internet Explorer を使用している場合は、web ページが開きます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="140">
          <source>Right-click in the page, and then click <bpt id="p1">**</bpt>View source<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ページ内を右クリックし、<bpt id="p1">**</bpt>ソースの表示<ept id="p1">**</ept> をクリックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="141">
          <source>Then save the contents of the page source to a file path.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">次に、ページ ソースのコンテンツをファイル パスに保存します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="142">
          <source>In a text editor such as Notepad++, open the XML file that you just saved, and follow these steps.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Notepad++ などテキスト エディターで、保存した XML ファイルを開き、これらの手順に従います。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="143">
          <source>Search for the following line: <bpt id="p1">**</bpt><ph id="ph1">&amp;lt;</ph>Table name=“RetailCustTable”<ph id="ph2">&amp;gt;</ph><ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">次の行を検索します: <bpt id="p1">**</bpt><ph id="ph1">&amp;lt;</ph>Table name=“RetailCustTable”<ph id="ph2">&amp;gt;</ph><ept id="p1">**</ept>。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="144">
          <source>There are two instances, at approximately line 29 and line 744.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">29 行目前後と 744 行目前後に 2 つのインスタンスがあります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="145">
          <source>Add the following code after the last line in both <bpt id="p1">**</bpt><ph id="ph1">&amp;lt;</ph>Table name=“RetailCustTable”<ph id="ph2">&amp;gt;</ph><ept id="p1">**</ept> code blocks.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">両方の <bpt id="p1">**</bpt><ph id="ph1">&amp;lt;</ph>Table name=“RetailCustTable”<ph id="ph2">&amp;gt;</ph><ept id="p1">**</ept> コード ブロックの最後の行の後に次のコードを追加します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="146">
          <source>You add the code after the <bpt id="p1">**</bpt><ph id="ph1">&amp;lt;</ph>/Table<ph id="ph2">&amp;gt;</ph><ept id="p1">**</ept> tag.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">コードを <bpt id="p1">**</bpt><ph id="ph1">&amp;lt;</ph>/Table<ph id="ph2">&amp;gt;</ph><ept id="p1">**</ept> タグの後に追加します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="147">
          <source>After you've finished editing the file, go back to client and the <bpt id="p1">**</bpt>Retail channel schema<ept id="p1">**</ept> page.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ファイルの編集が終了した後、クライアントおよび <bpt id="p1">**</bpt>Retail チャンネル スキーマ<ept id="p1">**</ept> ページ‎に戻ります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="148">
          <source>In the left navigation pane, click <bpt id="p1">**</bpt>Dynamics 365 for Retail.<ept id="p1">**</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">左のナビゲーション ウィンドウで、<bpt id="p1">**</bpt>Dynamics 365 for Retail<ept id="p1">**</ept> をクリックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="149">
          <source>On the <bpt id="p1">**</bpt>Retail data distribution<ept id="p1">**</ept> tab, click <bpt id="p2">**</bpt>Import<ept id="p2">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>小売データの配布<ept id="p1">**</ept>タブで、<bpt id="p2">**</bpt>インポート<ept id="p2">**</ept>をクリックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="150">
          <source>In the dialog box that opens, click <bpt id="p1">**</bpt>Browse<ept id="p1">**</ept>, select the XML file that you just edited, and then click <bpt id="p2">**</bpt>OK<ept id="p2">**</ept> to import the file.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">表示されるダイアログ ボックスで、<bpt id="p1">**</bpt>参照<ept id="p1">**</ept>をクリックし、編集した XML ファイルを選択してから、<bpt id="p2">**</bpt>OK<ept id="p2">**</ept> をクリックしてファイルをインポートします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="151">
          <source>Close the <bpt id="p1">**</bpt>Retail channel schema<ept id="p1">**</ept> page.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>小売チャネル スキーマ<ept id="p1">**</ept> ページを閉じます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="152">
          <source>Click <bpt id="p1">**</bpt>Retail<ept id="p1">**</ept> <ph id="ph1">&amp;gt;</ph> <bpt id="p2">**</bpt>Headquarters setup<ept id="p2">**</ept> <ph id="ph2">&amp;gt;</ph> <bpt id="p3">**</bpt>Retail scheduler<ept id="p3">**</ept> <ph id="ph3">&amp;gt;</ph> <bpt id="p4">**</bpt>Scheduler job<ept id="p4">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>小売<ept id="p1">**</ept> <ph id="ph1">&amp;gt;</ph> <bpt id="p2">**</bpt>本社の設定<ept id="p2">**</ept> <ph id="ph2">&amp;gt;</ph> <bpt id="p3">**</bpt>小売用スケジューラ<ept id="p3">**</ept> <ph id="ph3">&amp;gt;</ph> <bpt id="p4">**</bpt>スケジューラ ジョブ<ept id="p4">**</ept>の順にクリックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="153">
          <source>On the <bpt id="p1">**</bpt>Scheduler job<ept id="p1">**</ept> page, click <bpt id="p2">**</bpt>1010<ept id="p2">**</ept> to select the “Customers” job.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>スケジューラ ジョブ<ept id="p1">**</ept>ページで、<bpt id="p2">**</bpt>1010<ept id="p2">**</ept> をクリックし、「顧客」ジョブを選択します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="154">
          <source>On the <bpt id="p1">**</bpt>Subjobs<ept id="p1">**</ept> tab, click <bpt id="p2">**</bpt>New<ept id="p2">**</ept>, and then enter <bpt id="p3">**</bpt>RetailCustPreference<ept id="p3">**</ept> as the subjob number.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>サブジョブ<ept id="p1">**</ept>タブで、<bpt id="p2">**</bpt>新規<ept id="p2">**</ept>をクリックし、<bpt id="p3">**</bpt>RetailCustPreference<ept id="p3">**</ept> をサブジョブ番号として入力します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="155">
          <source>Click <bpt id="p1">**</bpt>Save<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>保存<ept id="p1">**</ept> をクリックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="156">
          <source>On the <bpt id="p1">&lt;strong&gt;</bpt>Retail channel schema<ept id="p1">&lt;/strong&gt;</ept> page, select <bpt id="p2">**</bpt>Dynamics 365 for Retail<ept id="p2">**</ept> as the schema name, and then click <bpt id="p3">**</bpt>Generate queries<ept id="p3">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">&lt;strong&gt;</bpt>小売チャネル スキーマ<ept id="p1">&lt;/strong&gt;</ept> ページで、スキーマ名として <bpt id="p2">**</bpt>Dynamics 365 for Retail<ept id="p2">**</ept> を選択してから、<bpt id="p3">**</bpt>クエリの生成<ept id="p3">**</ept> をクリックします。</target></trans-unit>
      </group>
    </body>
  </file>
</xliff>