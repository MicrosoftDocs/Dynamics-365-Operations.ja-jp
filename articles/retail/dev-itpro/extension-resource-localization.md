<?xml version="1.0" encoding="UTF-8"?>
<xliff xmlns:logoport="urn:logoport:xliffeditor:xliff-extras:1.0" xmlns:tilt="urn:logoport:xliffeditor:tilt-non-translatables:1.0" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns="urn:oasis:names:tc:xliff:document:1.2" xmlns:xliffext="urn:microsoft:content:schema:xliffextensions" version="1.2" xsi:schemaLocation="urn:oasis:names:tc:xliff:document:1.2 xliff-core-1.2-transitional.xsd">
  <file datatype="xml" source-language="en-US" original="extension-resource-localization.md" target-language="ja-JP">
    <header>
      <tool tool-company="Microsoft" tool-version="1.0-7889195" tool-name="mdxliff" tool-id="mdxliff"/>
      <xliffext:skl_file_name>extension-resource-localization.5d41dd.116cd847aa50eec7edbe13e7f51ed89cec290e72.skl</xliffext:skl_file_name>
      <xliffext:version>1.2</xliffext:version>
      <xliffext:ms.openlocfilehash>116cd847aa50eec7edbe13e7f51ed89cec290e72</xliffext:ms.openlocfilehash>
      <xliffext:ms.sourcegitcommit>9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b</xliffext:ms.sourcegitcommit>
      <xliffext:ms.lasthandoff>05/15/2019</xliffext:ms.lasthandoff>
      <xliffext:ms.openlocfilepath>articles\retail\dev-itpro\extension-resource-localization.md</xliffext:ms.openlocfilepath>
    </header>
    <body>
      <group extype="content" id="content">
        <trans-unit xml:space="preserve" translate="yes" id="101" restype="x-metadata">
          <source>Localize Retail extension resources and label files</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Retail 拡張リソースおよびラベル ファイルのローカライズ</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="102" restype="x-metadata">
          <source>This topic explains how to modify POS UI labels, POS messages, receipt labels, and error message for Retail server or CRT.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このトピックでは、POS UI ラベル、POS メッセージ、入庫ラベル、および Retail サーバーまたは CRT のエラー メッセージを変更する方法について説明します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="103" restype="x-metadata">
          <source>It also explains how you can add custom error messages for Retail server or CRT.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Retail サーバーまたは CRT のカスタム エラー メッセージを追加する方法についても説明します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="104">
          <source>Localize Retail extension resources and label files</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Retail 拡張リソースおよびラベル ファイルのローカライズ</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="105">
          <source>This topic explains how to modify labels in the point of sale (POS) user interface (UI), POS messages (error, warning, and information), receipt labels, and error messages for Retail server or Commerce Runtime Services (CRT).</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このトピックでは、販売時点管理 (POS) ユーザー インターフェイス (UI)、POS メッセージ (エラー、警告、および情報)、入庫ラベル、および Retail サーバーまたは Commerce Runtime のサービス (CRT) のエラー メッセージの点にラベルを変更する方法について説明します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="106">
          <source>You can also add custom error messages for Retail server or CRT in the same way.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Retail サーバーまたは CRT のカスタム エラー メッセージを、同じ方法で追加することもできます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="107">
          <source>However, for new POS extension labels, you should use the localization framework in the POS extension.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ただし、新しい POS 拡張ラベルの場合は、POS 拡張のローカライズ フレームワークを使用します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="108">
          <source>This topic is applicable to Microsoft Dynamics 365 for Finance and Operations 7.2 with the latest update, Microsoft Dynamics 365 for Retail 7.2 with the latest update, and to later versions.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このトピックは、 最新の更新プログラムが適用された Microsoft Dynamics 365 for Finance and Operations 7.2、最新の更新プログラムが適用された Microsoft Dynamics 365 for Retail 7.2 とそれ以降のバージョンに適用されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="109">
          <source>Retail POS labels and messages (error, warning, and information)</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Retail POS ラベルおよびメッセージ (エラー、警告、および情報)</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="110">
          <source>This section explains how to modify POS UI labels and POS messages by overriding the default strings.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このセクションでは、既定の文字列を上書きすることによって、POS UI ラベルおよび POS メッセージを変更する方法について説明します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="111">
          <source>Override POS UI labels and messages</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">POS UI ラベルおよびメッセージの上書き</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="112">
          <source>You can override the default strings in the POS by using the language text entries on the <bpt id="p1">**</bpt>Language text<ept id="p1">**</ept> page.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>言語テキスト<ept id="p1">**</ept> ページの言語テキスト エントリを使用して、POS の既定の文字列を上書きすることができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="113">
          <source>Follow these steps to change POS strings.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">POS 文字列を変更するには、次の手順を実行します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="114">
          <source>Sign in to Retail or Finance and Operations.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Retail または Finance and Operations へのサインイン</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="115">
          <source>Go to <bpt id="p1">**</bpt>Retail <ph id="ph1">&amp;gt;</ph> Channel setup <ph id="ph2">&amp;gt;</ph> POS setup <ph id="ph3">&amp;gt;</ph> POS profiles <ph id="ph4">&amp;gt;</ph> Language text<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>小売 <ph id="ph1">&amp;gt;</ph> チャネル設定 <ph id="ph2">&amp;gt;</ph> POS 設定 <ph id="ph3">&amp;gt;</ph> POS プロファイル <ph id="ph4">&amp;gt;</ph> 言語テキスト<ept id="p1">**</ept>の順に移動します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="116">
          <source>On the <bpt id="p1">**</bpt>Language text<ept id="p1">**</ept> page, on the <bpt id="p2">**</bpt>POS<ept id="p2">**</ept> tab, in the <bpt id="p3">**</bpt>POS language text<ept id="p3">**</ept> grid, select the <bpt id="p4">**</bpt>Add<ept id="p4">**</ept> button to add the language ID, text ID, and text for the string that you want to override.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>言語テキスト<ept id="p1">**</ept>ページの、<bpt id="p2">**</bpt>POS<ept id="p2">**</ept> タブの <bpt id="p3">**</bpt>POS 言語テキスト<ept id="p3">**</ept>グリッドで、<bpt id="p4">**</bpt>追加<ept id="p4">**</ept>ボタンを選択して言語 ID、テキスト ID、および上書きする文字列のテキストを追加します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="117">
          <source>For example, you want to change the label of the <bpt id="p1">**</bpt>Operator ID<ept id="p1">**</ept> field on the POS sign-in page to <bpt id="p2">**</bpt>Employee ID<ept id="p2">**</ept> for US English (en-us).</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">たとえば、POS サインイン ページの<bpt id="p1">**</bpt>オペレーター ID<ept id="p1">**</ept> フィールドのラベルを、アメリカ英語 (en-us) の<bpt id="p2">**</bpt>従業員 ID<ept id="p2">**</ept> に変更したいとします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="118">
          <source>In this case, add the following entry in the <bpt id="p1">**</bpt>POS language text<ept id="p1">**</ept> grid.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この場合、<bpt id="p1">**</bpt>POS 言語テキスト<ept id="p1">**</ept>グリッドで次のエントリを追加します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="119">
          <source>Language ID</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">言語 ID</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="120">
          <source>Text ID</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">テキスト ID</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="121">
          <source>Text</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">テキスト</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="122">
          <source>en-us</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ja</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="123">
          <source>502</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">502</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="124">
          <source>Employee ID</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">従業員 ID</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="125">
          <source>For information about how to get the text ID for POS strings, see the next section.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">POS 文字列のテキスト ID を取得する方法の詳細については、次のセクションを参照してください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="126">
          <source>On the Action Pane, select <bpt id="p1">**</bpt>Save<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">アクション ウィンドウで、<bpt id="p1">**</bpt>保存<ept id="p1">**</ept>を選択します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="127">
          <source>Go to <bpt id="p1">**</bpt>Retail <ph id="ph1">&amp;gt;</ph> Retail IT <ph id="ph2">&amp;gt;</ph> Distribution schedule<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>小売 <ph id="ph1">&amp;gt;</ph> 小売 IT <ph id="ph2">&amp;gt;</ph> 配送スケジュール<ept id="p1">**</ept>の順に移動します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="128">
          <source>Select the <bpt id="p1">**</bpt>Registers<ept id="p1">**</ept> (<bpt id="p2">**</bpt>1090<ept id="p2">**</ept>) job, and then select <bpt id="p3">**</bpt>Run now<ept id="p3">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>レジスター<ept id="p1">**</ept> (<bpt id="p2">**</bpt>1090<ept id="p2">**</ept>) ジョブを選択し、<bpt id="p3">**</bpt>今すぐ実行<ept id="p3">**</ept>を選択します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="129">
          <source>After the data is pushed, sign off, and then sign in to Cloud POS or Modern POS to see the changed labels.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">データをプッシュ後、クラウド POS または Modern POS でログインし、変更済のラベルを表示します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="130">
          <source>Get the text ID for POS strings</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">POS 文字列のテキスト ID を取得します</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="131">
          <source>To get the text ID for a POS string, you must run the POS by using the Retail software development kit (SDK) in Debug mode.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">POS 文字列のテキスト ID を取得するには、デバッグ モードで Retail ソフトウェア開発キット (SDK) を使用して、POS を実行する必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="132">
          <source>In the POS, text IDs are referred to as string IDs.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">POS では、テキスト ID を文字列 ID と呼びます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="133">
          <source>Start Microsoft Visual Studio 2015 in Administrator mode.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Microsoft Visual Studio 2015 を管理者モードで起動します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="134">
          <source>Open <bpt id="p1">**</bpt>ModernPOS<ept id="p1">**</ept> solution from <bpt id="p2">**</bpt>…<ph id="ph1">\\</ph>RetailSDK<ph id="ph2">\\</ph>POS<ept id="p2">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>ModernPOS<ept id="p1">**</ept> ソリューションを <bpt id="p2">**</bpt>…<ph id="ph1">\\</ph>RetailSDK<ph id="ph2">\\</ph>POS<ept id="p2">**</ept> から開きます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="135">
          <source>Set the <bpt id="p1">**</bpt>Solution configuration<ept id="p1">**</ept> property to <bpt id="p2">**</bpt>Debug<ept id="p2">**</ept>, the <bpt id="p3">**</bpt>Solution platforms<ept id="p3">**</ept> property to <bpt id="p4">**</bpt>x86<ept id="p4">**</ept>, and the <bpt id="p5">**</bpt>Deploy<ept id="p5">**</ept> property to <bpt id="p6">**</bpt>Local machine<ept id="p6">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>ソリューション構成<ept id="p1">**</ept>プロパティを<bpt id="p2">**</bpt>デバッグ<ept id="p2">**</ept>に、<bpt id="p3">**</bpt>ソリューション プラットフォーム<ept id="p3">**</ept>プロパティを <bpt id="p4">**</bpt>x86<ept id="p4">**</ept> に、および<bpt id="p5">**</bpt>配置<ept id="p5">**</ept>プロパティを<bpt id="p6">**</bpt>ローカル コンピューター<ept id="p6">**</ept>に設定します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="136">
          <source>Compile and build the solution, and then select <bpt id="p1">**</bpt>Deploy <ph id="ph1">\&gt;</ph> Local Machine<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ソリューションをコンパイル、およびビルドしてから、<bpt id="p1">**</bpt>配置<ph id="ph1">\&gt;</ph>ローカル コンピューター<ept id="p1">**</ept>を選択します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="137">
          <source>After the POS is deployed, sign in to it by using your operator ID and password.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">POS 配置後、オペレーター ID およびパスワードを使いログインします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="138">
          <source>Select the <bpt id="p1">**</bpt>Settings<ept id="p1">**</ept> button in the upper right of the POS window.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">POS ウィンドウの右上で<bpt id="p1">**</bpt>設定<ept id="p1">**</ept>ボタンを選択します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="139">
          <source>On the <bpt id="p1">**</bpt>Settings<ept id="p1">**</ept> page, under <bpt id="p2">**</bpt>Developer mode<ept id="p2">**</ept>, set the <bpt id="p3">**</bpt>Developer Mode<ept id="p3">**</ept> option to <bpt id="p4">**</bpt>Yes<ept id="p4">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>設定<ept id="p1">**</ept>ページの<bpt id="p2">**</bpt>開発者モード<ept id="p2">**</ept>で、<bpt id="p3">**</bpt>開発者モード<ept id="p3">**</ept>オプションを<bpt id="p4">**</bpt>はい<ept id="p4">**</ept>に設定します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="140">
          <source>Set the <bpt id="p1">**</bpt>Show Strings IDs<ept id="p1">**</ept> option to <bpt id="p2">**</bpt>Yes<ept id="p2">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>文字列 ID の表示<ept id="p1">**</ept>オプションを<bpt id="p2">**</bpt>はい<ept id="p2">**</ept>に設定します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="141">
          <source>Sign out of the POS, and then sign in again.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">POS からサインアウトし、再度サインインします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="142">
          <source>The POS now shows the strings IDs in front of all the labels and messages.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">POS には、すべてのラベルとメッセージの前に文字列 ID が表示されるようになります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="143">
          <source>Troubleshooting</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">トラブルシューティング</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="144">
          <source>If the <bpt id="p1">**</bpt>Developer Mode<ept id="p1">**</ept> option doesn't appear on the <bpt id="p2">**</bpt>Settings<ept id="p2">**</ept> page in the POS, verify that you're running in Debug mode.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>開発者モード<ept id="p1">**</ept>オプションが POS の<bpt id="p2">**</bpt>設定<ept id="p2">**</ept>ページに表示されない場合は、デバッグ モードで動作していることを確認してください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="145">
          <source>Open the <bpt id="p1">**</bpt>pos.js<ept id="p1">**</ept> file, and verify that <bpt id="p2">**</bpt>Config.isDebugMode<ept id="p2">**</ept> is set to <bpt id="p3">**</bpt>true<ept id="p3">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>pos.js<ept id="p1">**</ept> ファイルを開き、<bpt id="p2">**</bpt>Config.isDebugMode<ept id="p2">**</ept> が <bpt id="p3">**</bpt>true<ept id="p3">**</ept> に設定されていることを確認します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="146">
          <source>If it's set to <bpt id="p1">**</bpt>false<ept id="p1">**</ept>, change the value to <bpt id="p2">**</bpt>true<ept id="p2">**</ept>, and then deploy the POS again.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>false<ept id="p1">**</ept> に設定されている場合、値を <bpt id="p2">**</bpt>true<ept id="p2">**</ept> に変更し、再度 POS を配置します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="147">
          <source>You should edit the pos.js file <bpt id="p1">**</bpt>only<ept id="p1">**</ept> to do quick testing and to get string IDs.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">クイック テストを行い、文字列 ID を取得するために、pos.js ファイル<bpt id="p1">**</bpt>のみ<ept id="p1">**</ept>を編集する必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="148">
          <source>In these cases, after you edit the file, you should revert your changes.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">そのような場合、ファイルを編集した後に、変更内容を元に戻す必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="149">
          <source>Any changes that you make in Microsoft cores files will be overridden during deployment.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Microsoft のコア ファイルに加えた変更は展開中に上書きされます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="150">
          <source>Therefore, you will lose the changes.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">そのため、変更は失われます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="151">
          <source>Additionally, future versions might not support editing the pos.js file.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">また、将来のバージョンでは、pos.js ファイルの編集をサポートしない可能性があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="152">
          <source>Retail server or CRT error messages, or receipt strings</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Retail サーバーや CRT エラー メッセージ、または入庫文字列</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="153">
          <source>This section explains how to modify Retail server or CRT error messages, or receipt strings, by overriding the default strings.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このセクションでは、既定の文字列を上書きすることによって Retail サーバーまたは CRT エラー メッセージ、または入庫文字列を変更する方法について説明します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="154">
          <source>It also explains how you can add new, custom Retail server or CRT error messages, or receipt strings.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">新規、Retail サーバーまたは CRT のカスタム エラー メッセージ、または入庫文字列を追加する方法についても説明します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="155">
          <source>Override Retail server or CRT error messages, or receipt strings</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Retail サーバーや CRT エラー メッセージ、または入庫文字列を上書き</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="156">
          <source>Sign in to Retail or Finance and Operations.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Retail または Finance and Operations へのサインイン</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="157">
          <source>Go to <bpt id="p1">**</bpt>Retail <ph id="ph1">\&gt;</ph> Channel setup <ph id="ph2">\&gt;</ph> POS setup <ph id="ph3">\&gt;</ph> POS profiles <ph id="ph4">\&gt;</ph> Language text<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>小売 <ph id="ph1">\&gt;</ph> チャネル設定 <ph id="ph2">\&gt;</ph> POS 設定 <ph id="ph3">\&gt;</ph> POS プロファイル <ph id="ph4">\&gt;</ph> 言語テキスト<ept id="p1">**</ept>の順に移動します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="158">
          <source>On the <bpt id="p1">**</bpt>Language text<ept id="p1">**</ept> page, on the <bpt id="p2">**</bpt>Retail server<ept id="p2">**</ept> tab, in the <bpt id="p3">**</bpt>Retail server language text<ept id="p3">**</ept> grid, click the <bpt id="p4">**</bpt>Add<ept id="p4">**</ept> button to add the language ID, text ID, and text for the string that you want to override.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>言語テキスト<ept id="p1">**</ept>ページの、<bpt id="p2">**</bpt>Retail サーバー<ept id="p2">**</ept>タブの <bpt id="p3">**</bpt>Retail サーバー言語テキスト<ept id="p3">**</ept>グリッドで、<bpt id="p4">**</bpt>追加<ept id="p4">**</ept>ボタンをクリックして言語 ID、テキスト ID、および上書きする文字列のテキストを追加します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="159">
          <source>For example, when users enter an incorrect user name or password during sign-in, the POS shows the following error message: "We didn't recognize the user name or password.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">たとえば、サインイン中にユーザーが間違ったユーザー名またはパスワードを入力すると、POS に次のエラー メッセージが表示されます: 「ユーザー名またはパスワードが認識されませんでした。」</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="160">
          <source>Please try again."</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">もう一度やり直してください。」</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="161">
          <source>For US English, you want to change the message to "Please enter valid user name or password."</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">英語 (US) では、メッセージを「有効なユーザー名またはパスワードを入力してください」に変更します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="162">
          <source>In this case, add the following entry in the <bpt id="p1">**</bpt>Retail server language text<ept id="p1">**</ept> grid.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この場合、<bpt id="p1">**</bpt>Retail サーバー 言語テキスト<ept id="p1">**</ept>グリッドで次のエントリを追加します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="163">
          <source>Language ID</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">言語 ID</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="164">
          <source>Text ID</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">テキスト ID</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="165">
          <source>Text</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">テキスト</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="166">
          <source>en-us</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ja</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="167">
          <source>Microsoft<ph id="ph1">\_</ph>Dynamics<ph id="ph2">\_</ph>Commerce<ph id="ph3">\_</ph>Runtime<ph id="ph4">\_</ph>InvalidAuthenticationCredentials</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Microsoft<ph id="ph1">\_</ph>Dynamics<ph id="ph2">\_</ph>Commerce<ph id="ph3">\_</ph>Runtime<ph id="ph4">\_</ph>InvalidAuthenticationCredentials</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="168">
          <source>Please enter valid user name or password</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">有効なユーザー名またはパスワードを入力してください</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="169">
          <source>For information about how to get the text ID for Retail server or CRT error messages, and receipt strings, see the next section.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Retail サーバーまたは CRT エラー メッセージのテキスト ID、および入庫文字列を取得する方法の詳細については、次のセクションを参照してください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="170">
          <source>On the Action Pane, select <bpt id="p1">**</bpt>Save<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">アクション ウィンドウで、<bpt id="p1">**</bpt>保存<ept id="p1">**</ept>を選択します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="171">
          <source>Go to <bpt id="p1">**</bpt>Retail <ph id="ph1">\&gt;</ph> Retail IT <ph id="ph2">\&gt;</ph> Distribution schedule<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>小売 <ph id="ph1">\&gt;</ph> 小売 IT <ph id="ph2">\&gt;</ph> 配送スケジュール<ept id="p1">**</ept>の順に移動します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="172">
          <source>Select the <bpt id="p1">**</bpt>Registers<ept id="p1">**</ept> (<bpt id="p2">**</bpt>1090<ept id="p2">**</ept>) job, and then select <bpt id="p3">**</bpt>Run now<ept id="p3">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>レジスター<ept id="p1">**</ept> (<bpt id="p2">**</bpt>1090<ept id="p2">**</ept>) ジョブを選択し、<bpt id="p3">**</bpt>今すぐ実行<ept id="p3">**</ept>を選択します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="173">
          <source>Get the text ID for Retail server or CRT messages, or receipt strings</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Retail サーバーまたは CRT メッセージ、または入庫文字列のためのテキスト ID を取得します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="174">
          <source>Go to <bpt id="p1">**</bpt>…<ph id="ph1">\\</ph>RetailSDK<ph id="ph2">\\</ph>Documents<ph id="ph3">\\</ph>Resources<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>…<ph id="ph1">\\</ph>RetailSDK<ph id="ph2">\\</ph>ドキュメント<ph id="ph3">\\</ph>リソース<ept id="p1">**</ept>に移動します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="175">
          <source>In Visual Studio, open one of the following resource files:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Visual Studio で、次のリソース ファイルのいずれかを開きます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="176">
          <source><bpt id="p1">**</bpt>To modify Retail server or CRT error messages:<ept id="p1">**</ept> RuntimeExceptionMessages.resx</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>Retail server または CRT エラー メッセージを変更する:<ept id="p1">**</ept> RuntimeExceptionMessages.resx</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="177">
          <source><bpt id="p1">**</bpt>To modify receipt strings:<ept id="p1">**</ept> RuntimeReceiptMessages.resx</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>入力された文字列の変更:<ept id="p1">**</ept> RuntimeReceiptMessages.resx</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="178">
          <source>For every message in the resource file, Visual Studio shows a name and a value.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">リソース ファイル内のすべてのメッセージについて、Visual Studio は名前と値を表示します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="179">
          <source>In the <bpt id="p1">**</bpt>Value<ept id="p1">**</ept> column, search for the text that you want to change.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>値<ept id="p1">**</ept>列で、変更するテキストを検索します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="180">
          <source>Copy the name that corresponds to that value.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">その値に対応する名前をコピーします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="181">
          <source>You enter this name as the text ID in the <bpt id="p1">**</bpt>Retail server language text<ept id="p1">**</ept> grid.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この名前をテキストID として <bpt id="p1">**</bpt>Retail サーバー言語テキスト<ept id="p1">**</ept> グリッドに入力します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="182">
          <source>Add custom Retail server or CRT error messages, or receipt strings</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">カスタム Retail サーバーまたは CRT エラー メッセージ、または入庫文字列を追加</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="183">
          <source>You can also add new Retail server or CRT error messages, or new receipt strings, in the <bpt id="p1">**</bpt>Retail server language text<ept id="p1">**</ept> grid.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">新しい Retail サーバーまたは CRT エラー メッセージ、または、新しい入庫文字列を <bpt id="p1">**</bpt>Retail サーバー言語テキスト<ept id="p1">**</ept> グリッドに追加することもできます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="184">
          <source>In this way, you support localization instead of hard-coding everything in the code.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この方法で、コード内のハードコーディングのすべての代わりにローカライズをサポートします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="185">
          <source>The text ID of all your new messages must start with <bpt id="p1">**</bpt>Microsoft<ph id="ph1">\_</ph>Dynamics<ph id="ph2">\_</ph>Commerce<ph id="ph3">\_</ph><ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">すべてのメッセージのテキスト ID は <bpt id="p1">**</bpt>Microsoft<ph id="ph1">\_</ph>Dynamics<ph id="ph2">\_</ph>Commerce<ph id="ph3">\_</ph><ept id="p1">**</ept> から始まる必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="186">
          <source>For example, you want to add a new exception message in US English (en-us) and UK English (en-uk).</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">たとえば、アメリカ英語 (en-us) と英国英語 (en-uk) で新しい例外メッセージを追加したいとします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="187">
          <source>In this case, add entries that resemble the follow entries in the <bpt id="p1">**</bpt>Retail server language text<ept id="p1">**</ept> grid.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この場合、<bpt id="p1">**</bpt>Retail サーバー言語テキスト<ept id="p1">**</ept>グリッドでの次のエントリに類似したエントリを追加します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="188">
          <source>Language ID</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">言語 ID</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="189">
          <source>Text ID</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">テキスト ID</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="190">
          <source>Text</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">テキスト</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="191">
          <source>en-us</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ja</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="192">
          <source>Microsoft_Dynamics_Commerce_CustomId1</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Microsoft_Dynamics_Commerce_CustomId1</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="193">
          <source>My new message in US English</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">アメリカ英語での新しいメッセージ</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="194">
          <source>en-uk</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">en-uk</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="195">
          <source>Microsoft_Dynamics_Commerce_CustomId1</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Microsoft_Dynamics_Commerce_CustomId1</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="196">
          <source>My new message in UK English</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">英国英語での新しいメッセージ</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="197">
          <source>In this example, <bpt id="p1">**</bpt>CustomId1<ept id="p1">**</ept> is the text ID for the new message.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この例では、<bpt id="p1">**</bpt>CustomId1<ept id="p1">**</ept> が新しいメッセージのテキスト ID です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="198">
          <source>You can use any text ID that you want, provided that it starts with <bpt id="p1">**</bpt>Microsoft_Dynamics_Commerce_<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">使用したい任意のテキスト ID を使用することができます。ただし、<bpt id="p1">**</bpt>Microsoft_Dynamics_Commerce_<ept id="p1">**</ept> で始まる場合に限ります</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="199">
          <source>The following example shows how to use this new message in your CRT extension code.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">次の例では、この新しいメッセージを CRT 拡張コードで使用する方法を示します。</target></trans-unit>
      </group>
    </body>
  </file>
</xliff>