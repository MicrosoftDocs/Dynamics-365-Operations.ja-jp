<?xml version="1.0" encoding="UTF-8"?>
<xliff xmlns:logoport="urn:logoport:xliffeditor:xliff-extras:1.0" xmlns:tilt="urn:logoport:xliffeditor:tilt-non-translatables:1.0" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns="urn:oasis:names:tc:xliff:document:1.2" xmlns:xliffext="urn:microsoft:content:schema:xliffextensions" version="1.2" xsi:schemaLocation="urn:oasis:names:tc:xliff:document:1.2 xliff-core-1.2-transitional.xsd">
  <file datatype="xml" source-language="en-US" original="pos-dual-display-extension.md" target-language="ja-JP">
    <header>
      <tool tool-company="Microsoft" tool-version="1.0-7889195" tool-name="mdxliff" tool-id="mdxliff"/>
      <xliffext:skl_file_name>pos-dual-display-extension.47ab81.cc8c73d0f1f00eb1efb3084811ccd47aefc3a16e.skl</xliffext:skl_file_name>
      <xliffext:version>1.2</xliffext:version>
      <xliffext:ms.openlocfilehash>cc8c73d0f1f00eb1efb3084811ccd47aefc3a16e</xliffext:ms.openlocfilehash>
      <xliffext:ms.sourcegitcommit>9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b</xliffext:ms.sourcegitcommit>
      <xliffext:ms.lasthandoff>05/15/2019</xliffext:ms.lasthandoff>
      <xliffext:ms.openlocfilepath>articles\retail\dev-itpro\pos-dual-display-extension.md</xliffext:ms.openlocfilepath>
    </header>
    <body>
      <group extype="content" id="content">
        <trans-unit xml:space="preserve" translate="yes" id="101" restype="x-metadata">
          <source>Extend the point of sale (POS) Dual display view</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">販売時点管理 (POS) デュアル ディスプレイ ビューの拡張</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="102" restype="x-metadata">
          <source>This topic explains how to extend the POS Dual display view so that it shows custom information.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このトピックでは、ユーザー情報が表示されるように、POS デュアル ディスプレイ ビューを拡張する方法について説明します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="103">
          <source>Extend the point of sale (POS) Dual display view</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">販売時点管理 (POS) デュアル ディスプレイ ビューの拡張</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="104">
          <source>This topic explains how to extend the point of sale (POS) Dual display view so that it shows custom information.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このトピックでは、ユーザー情報が表示されるように、販売時点管理 (POS) デュアル ディスプレイ ビューを拡張する方法について説明します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="105">
          <source>This topic is applicable to Microsoft Dynamics 365 for Finance and Operations 7.2 or Microsoft Dynamics 365 for Retail 7.2 with KB 4091080, and later versions.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このトピックでは、Microsoft Dynamics 365 for Finance and Operations 7.2 または Microsoft Dynamics 365 for Retail 7.2 および KB 4091080 とそれ以降のバージョンが適用されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="106">
          <source>You can extend the POS Dual display view by adding a custom control.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">POS デュアル ディスプレイ ビューを拡張するには、カスタム コントロールを追加します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="107">
          <source>In the custom control, you can add images, POS data lists, labels, and so on, to show custom information.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">カスタム コントロールでは、カスタム情報を表示する画像、POS データ リスト、ラベルなどを追加できます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="108">
          <source>You can extend the POS Dual display view only by adding a custom control.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">POS デュアル ディスプレイ ビューのみを拡張するには、カスタム コントロールを追加します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="109">
          <source>The custom control will override the standard content that is shown in the POS Dual display view.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">カスタム コントロールは、POS デュアル ディスプレイ ビューに表示される標準的な内容を上書きします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="110">
          <source>Required steps</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">必要なステップ</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="111">
          <source>Here is an overview of the steps that are required in order to customize the POS Dual display view.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">POS デュアル ディスプレイ ビューをカスタマイズするために必要な手順の概要を示します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="112">
          <source>Configure the hardware profile to enable dual display.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">デュアル ディスプレイを有効にするハードウェア プロファイルをコンフィギュレーションします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="113">
          <source>Create a folder in the POS.Extensions project for extension of the POS Dual display view.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">POS.Extensions プロジェクトに、POS デュアル ディスプレイ ビューの拡張ためのフォルダを作成します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="114">
          <source>Add a new custom control that includes custom information.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">カスタム情報を含む新しいカスタム コントロールを追加します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="115">
          <source>Update the manifest.json and extensions.json files with the extension of the POS Dual display view.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">POS デュアル ディスプレイ ビューの拡張子を使用して、manifest.json ファイルと extensions.json ファイルを更新します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="116">
          <source>Deploy the changes, and validate the customization.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">変更を配置し、カスタマイズを検証します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="117">
          <source>Scenario or business problem</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">シナリオまたはビジネスの問題</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="118">
          <source>You will add a custom control column in the POS Dual display view to show the cart details and information about the customer and the store employee.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">POS デュアル ディスプレイ ビューにカスタム コントロール列を追加して、カートの詳細と顧客および店舗の従業員に関する情報を表示します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="119">
          <source>Configure the hardware profile to enable dual display</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">デュアル ディスプレイを有効にするハードウェア プロファイルをコンフィギュレーションします</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="120">
          <source>Sign in to Retail or Finance and Operations.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Retail または Finance and Operations へのサインイン</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="121">
          <source>Go to <bpt id="p1">**</bpt>Retail <ph id="ph1">\&gt;</ph> Channel setup <ph id="ph2">\&gt;</ph> POS setup <ph id="ph3">\&gt;</ph> POS profiles <ph id="ph4">\&gt;</ph> Hardware profiles<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>小売 <ph id="ph1">\&gt;</ph> チャネル設定 <ph id="ph2">\&gt;</ph> POS 設定 <ph id="ph3">\&gt;</ph> POS プロファイル <ph id="ph4">\&gt;</ph> ハードウェア プロファイル<ept id="p1">**</ept>の順に移動します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="122">
          <source>Select the hardware profile that is linked to your register.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">レジスタにリンクしているハードウェア プロファイルを選択します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="123">
          <source>On the <bpt id="p1">**</bpt>Dual display<ept id="p1">**</ept> tab, set the <bpt id="p2">**</bpt>Dual display in use<ept id="p2">**</ept> option to <bpt id="p3">**</bpt>Yes<ept id="p3">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>デュアル ディスプレイ<ept id="p1">**</ept>タブで、<bpt id="p2">**</bpt>デュアル ディスプレイの使用<ept id="p2">**</ept>オプションを<bpt id="p3">**</bpt>はい<ept id="p3">**</ept>に設定します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="124">
          <source>Go to <bpt id="p1">**</bpt>Retail <ph id="ph1">\&gt;</ph> Retail IT <ph id="ph2">\&gt;</ph> Distribution schedule<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>小売 <ph id="ph1">\&gt;</ph> 小売 IT <ph id="ph2">\&gt;</ph> 配送スケジュール<ept id="p1">**</ept>の順に移動します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="125">
          <source>Select the <bpt id="p1">**</bpt>Registers<ept id="p1">**</ept> (<bpt id="p2">**</bpt>1090<ept id="p2">**</ept>) job, and then select <bpt id="p3">**</bpt>Run now<ept id="p3">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>レジスター<ept id="p1">**</ept> (<bpt id="p2">**</bpt>1090<ept id="p2">**</ept>) ジョブを選択し、<bpt id="p3">**</bpt>今すぐ実行<ept id="p3">**</ept>を選択します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="126">
          <source>You can find the end-to-end (E2E) sample in …<ph id="ph1">\\</ph>RetailSDK<ph id="ph2">\\</ph>POS<ph id="ph3">\\</ph>Extensions<ph id="ph4">\\</ph>DualDisplaySample.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">エンド ツー エンド (E2E) サンプルを <ph id="ph1">\\</ph>RetailSDK<ph id="ph2">\\</ph>POS<ph id="ph3">\\</ph>拡張機能<ph id="ph4">\\</ph>DualDisplaySample で検索できます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="127">
          <source>Add a new custom control for extension of the POS Dual display view</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">POS デュアル ディスプレイ ビューの拡張子の新しいカスタム コントロールを追加</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="128">
          <source>Start Microsoft Visual Studio 2015 in Administrator mode.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Microsoft Visual Studio 2015 を管理者モードで起動します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="129">
          <source>Open the <bpt id="p1">**</bpt>ModernPOS<ept id="p1">**</ept> solution from <bpt id="p2">**</bpt>…<ph id="ph1">\\</ph>RetailSDK<ph id="ph2">\\</ph>POS<ept id="p2">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>ModernPOS<ept id="p1">**</ept> ソリューションを <bpt id="p2">**</bpt>…<ph id="ph1">\\</ph>RetailSDK<ph id="ph2">\\</ph>POS<ept id="p2">**</ept> から開きます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="130">
          <source>Under the <bpt id="p1">**</bpt>POS.Extensions<ept id="p1">**</ept> project, create a folder that is named <bpt id="p2">**</bpt>DualDisplayExtension<ept id="p2">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>POS.Extensions<ept id="p1">**</ept> プロジェクトで、<bpt id="p2">**</bpt>DualDisplayExtension<ept id="p2">**</ept> というフォルダーを作成します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="131">
          <source>Under the <bpt id="p1">**</bpt>DualDisplayExtension<ept id="p1">**</ept> folder, create a folder that is named <bpt id="p2">**</bpt>CustomControl<ept id="p2">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>DualDisplayExtension<ept id="p1">**</ept> フォルダーで、<bpt id="p2">**</bpt>CustomControl<ept id="p2">**</ept> というフォルダーを作成します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="132">
          <source>In the <bpt id="p1">**</bpt>CustomControl<ept id="p1">**</ept> folder, create a HTML file that is named <bpt id="p2">**</bpt>DualDisplayCustomControl.html<ept id="p2">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>CustomControl<ept id="p1">**</ept> フォルダーで、<bpt id="p2">**</bpt>DualDisplayCustomControl.html<ept id="p2">**</ept> という HTML ファイルを作成します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="133">
          <source>In the HTML file, you will add a data list control to show the cart details, and text controls to show the total amount, customer name, employee name, and sign-in status.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">HTML ファイルで、買い物カゴの詳細を表示するデータ リスト コントロール、合計金額、顧客名、従業員名、およびサインイン ステータスを表示するテキスト コントロールを追加します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="134">
          <source>Copy the following code, and paste it into the <bpt id="p1">**</bpt>DualDisplayCustomControl.html<ept id="p1">**</ept> file.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">次のコードをコピーして、<bpt id="p1">**</bpt>DualDisplayCustomControl.html<ept id="p1">**</ept> ファイルに貼り付けます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="135">
          <source>Next, you will add the resource file that is used to localize the field name.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">次に、フィールド名をローカライズするために使用されるリソース ファイルを追加します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="136">
          <source>Under the <bpt id="p1">**</bpt>DualDisplayExtension<ept id="p1">**</ept> folder, create a folder that is named <bpt id="p2">**</bpt>Resources<ept id="p2">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>DualDisplayExtension<ept id="p1">**</ept> フォルダーで、<bpt id="p2">**</bpt>Resources<ept id="p2">**</ept> というフォルダーを作成します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="137">
          <source>Under the <bpt id="p1">**</bpt>Resources<ept id="p1">**</ept> folder, create a folder that is named <bpt id="p2">**</bpt>Strings<ept id="p2">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>Resources<ept id="p1">**</ept> フォルダーで、<bpt id="p2">**</bpt>Strings<ept id="p2">**</ept> というフォルダーを作成します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="138">
          <source>Under the <bpt id="p1">**</bpt>Strings<ept id="p1">**</ept> folder, create a folder that is named <bpt id="p2">**</bpt>en-US<ept id="p2">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>Strings<ept id="p1">**</ept> フォルダーで、<bpt id="p2">**</bpt>en-US<ept id="p2">**</ept> というフォルダーを作成します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="139">
          <source>In the en-US folder add a new resources file and and change the file extension and name to resources.resjson and inside the resources.resjson file copy paste the below resource strings.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">en-US フォルダで新しいリソース ファイルを追加し、ファイル拡張子を resources.resjson に変更し、および resources.resjson ファイルの中身をコピーし以下のリソース文字列に貼り付けます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="140">
          <source>In the <bpt id="p1">**</bpt>CustomControl<ept id="p1">**</ept> folder, create a TypeScript file (.ts file) that is named <bpt id="p2">**</bpt>DualDisplayCustomControl.ts<ept id="p2">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>CustomControl<ept id="p1">**</ept> フォルダーで、<bpt id="p2">**</bpt>DualDisplayCustomControl.html<ept id="p2">**</ept> という TypeScript ファイル (.ts file) を作成します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="141">
          <source>Copy the following code, and paste it into the <bpt id="p1">**</bpt>DualDisplayCustomControl.ts<ept id="p1">**</ept> file.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">次のコードをコピーして、<bpt id="p1">**</bpt>DualDisplayCustomControl.ts<ept id="p1">**</ept> ファイルに貼り付けます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="142">
          <source>This code imports the relevant entities and context.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このコードは関連するエンティティおよびコンテキストをインポートします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="143">
          <source>In the <bpt id="p1">**</bpt>DualDisplayCustomControl.ts<ept id="p1">**</ept> file, create a class that is named <bpt id="p2">**</bpt>DualDisplayCustomControl<ept id="p2">**</ept>, and extend it from the <bpt id="p3">**</bpt>DualDisplayCustomControlBase<ept id="p3">**</ept> class.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>DualDisplayCustomControl.ts<ept id="p1">**</ept> ファイルで、<bpt id="p2">**</bpt>DualDisplayCustomControl<ept id="p2">**</ept> というクラスを作成し、<bpt id="p3">**</bpt>DualDisplayCustomControlBase<ept id="p3">**</ept> クラスから拡張します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="144">
          <source>You extend from the <bpt id="p1">**</bpt>DualDisplayCustomControlBase<ept id="p1">**</ept> class to get all the events that are exposed for dual display.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>DualDisplayCustomControlBase<ept id="p1">**</ept> クラスから拡張し、デュアル ディスプレイで公開されているすべてのイベントを取得します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="145">
          <source>Inside the <bpt id="p1">**</bpt>DualDisplayCustomControl<ept id="p1">**</ept> class, add the following variables to get the cart, customer, and employee details.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>DualDisplayCustomControl<ept id="p1">**</ept> クラス内で、買い物カゴ、顧客、および従業員の詳細を取得するのに次の変数を追加します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="146">
          <source>Create a class constructor method to initialize all the variables.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">クラスのコンストラクター メソッドを作成して、すべての変数を初期化します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="147">
          <source>Add the <bpt id="p1">**</bpt>onReady<ept id="p1">**</ept> method to bind the control to the specified HTML element.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>onReady<ept id="p1">**</ept> メソッドを追加して、コントロールを指定した HTML 要素にバインドします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="148">
          <source>Add the <bpt id="p1">**</bpt>init<ept id="p1">**</ept> method to initialize all the controls.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">すべてのコントロールを初期化する <bpt id="p1">**</bpt>init<ept id="p1">**</ept> メソッドを追加します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="149">
          <source>Here is what the overall class should look like.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">全体のクラスがどのように見えるかを次に示します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="150">
          <source>In the <bpt id="p1">**</bpt>DualDisplayExtension<ept id="p1">**</ept> folder, create a JavaScript Object Notation (JSON) file (.json file) that is named <bpt id="p2">**</bpt>manifest.json<ept id="p2">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>DualDisplayExtension<ept id="p1">**</ept> フォルダーで、<bpt id="p2">**</bpt>manifest.json<ept id="p2">**</ept> という名前の JavaScript Object Notation (JSON) ファイル (.json ファイル) を作成します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="151">
          <source>Copy the following code, and paste it into the <bpt id="p1">**</bpt>manifest.json<ept id="p1">**</ept> file.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">次のコードをコピーして、<bpt id="p1">**</bpt>manifest.json<ept id="p1">**</ept> ファイルに貼り付けます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="152">
          <source>Delete the default generated code before you copy this code.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このコードをコピーする前に、既定で生成されたコードを削除してください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="153">
          <source>Open the <bpt id="p1">**</bpt>extensions.json<ept id="p1">**</ept> file under the <bpt id="p2">**</bpt>POS.Extensions<ept id="p2">**</ept> project, and update it with the <bpt id="p3">**</bpt>DualDisplayExtension<ept id="p3">**</ept> samples.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>extensions.json<ept id="p1">**</ept>ファイルを <bpt id="p2">**</bpt>POS.Extensions<ept id="p2">**</ept> プロジェクトで開いて、<bpt id="p3">**</bpt>DualDisplayExtension<ept id="p3">**</ept> サンプルで更新します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="154">
          <source>In that way, the POS will include this extension during runtime.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このようにして、実行時に POS にこの拡張が含まれます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="155">
          <source>Open the <bpt id="p1">**</bpt>tsconfig.json<ept id="p1">**</ept> file, and comment out the extension package folders in the exclude list.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>tsconfig.json<ept id="p1">**</ept> ファイルを開いて、拡張パッケージ フォルダーを除外リストでコメント アウトします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="156">
          <source>The POS will use this file to include or exclude the extension.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">POS では、このファイルを使用して、拡張機能を追加または除外します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="157">
          <source>By default, the list contains all the excluded extensions.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">既定では、リストにすべての除外された拡張子が含まれています。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="158">
          <source>If you want to include an extension as part of the POS, add the name of the extension folder, and comment out the extension in the extension list, as shown here.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">拡張機能を POS の一部として含めるには、次に示すように、拡張フォルダーの名前を追加し、拡張リストの拡張をコメント アウトします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="159">
          <source>Compile and rebuild the project.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">プロジェクトをコンパイル、およびリビルドします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="160">
          <source>Validate the customization</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">カスタマイズの検証</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="161">
          <source>Sign in to Retail Modern POS by using <bpt id="p1">**</bpt>000160<ept id="p1">**</ept> as the operator ID and <bpt id="p2">**</bpt>123<ept id="p2">**</ept> as the password.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">オペレーター ID に <bpt id="p1">**</bpt>000160<ept id="p1">**</ept>、パスワードに <bpt id="p2">**</bpt>123<ept id="p2">**</ept> を使用して Retail Modern POS にサインインします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="162">
          <source>On the welcome screen, select the <bpt id="p1">**</bpt>Current transaction<ept id="p1">**</ept> button.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ようこそ画面で、<bpt id="p1">**</bpt>現在のトランザクション<ept id="p1">**</ept>ボタンを選択します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="163">
          <source>Add any item to the transaction.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">品目をトランザクションに追加します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="164">
          <source>For example, add item number <bpt id="p1">**</bpt>0005<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">たとえば、品目番号 <bpt id="p1">**</bpt>0005<ept id="p1">**</ept> を追加します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="165">
          <source>Add any customer to transaction.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">顧客をトランザクションへ追加します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="166">
          <source>For example, add <bpt id="p1">**</bpt>Karen Berg<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">たとえば、<bpt id="p1">**</bpt>Karen Berg<ept id="p1">**</ept> を追加します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="167">
          <source>The dual display should show the cart, total, employee, and customer details.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">デュアル ディスプレイには、買い物カゴ、合計、従業員、および顧客の詳細が表示される必要があります。</target></trans-unit>
      </group>
    </body>
  </file>
</xliff>