<?xml version="1.0" encoding="UTF-8"?>
<xliff xmlns:logoport="urn:logoport:xliffeditor:xliff-extras:1.0" xmlns:tilt="urn:logoport:xliffeditor:tilt-non-translatables:1.0" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns="urn:oasis:names:tc:xliff:document:1.2" xmlns:xliffext="urn:microsoft:content:schema:xliffextensions" version="1.2" xsi:schemaLocation="urn:oasis:names:tc:xliff:document:1.2 xliff-core-1.2-transitional.xsd">
  <file datatype="xml" source-language="en-US" original="pos-custom-transaction.md" target-language="ja-JP">
    <header>
      <tool tool-company="Microsoft" tool-version="1.0-7889195" tool-name="mdxliff" tool-id="mdxliff"/>
      <xliffext:skl_file_name>pos-custom-transaction.286c64.d6373f83aa4c0e64addbb17d336016ebe49e36aa.skl</xliffext:skl_file_name>
      <xliffext:version>1.2</xliffext:version>
      <xliffext:ms.openlocfilehash>d6373f83aa4c0e64addbb17d336016ebe49e36aa</xliffext:ms.openlocfilehash>
      <xliffext:ms.sourcegitcommit>9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b</xliffext:ms.sourcegitcommit>
      <xliffext:ms.lasthandoff>05/15/2019</xliffext:ms.lasthandoff>
      <xliffext:ms.openlocfilepath>articles\retail\dev-itpro\pos-custom-transaction.md</xliffext:ms.openlocfilepath>
    </header>
    <body>
      <group extype="content" id="content">
        <trans-unit xml:space="preserve" translate="yes" id="101" restype="x-metadata">
          <source>Add custom controls to Retail Modern POS (MPOS) transaction pages</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Retail Modern POS (MPOS) トランザクション ページへのカスタム コントロールの追加</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="102" restype="x-metadata">
          <source>This topic explains how to add a new custom control on a transaction page by using the screen layout designer.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このトピックでは、画面レイアウト デザイナーを使用して トランザクション ページに新しいカスタム コントロールを追加する方法について説明します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="103">
          <source>Add custom controls to Retail Modern POS (MPOS) transaction pages</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Retail Modern POS (MPOS) トランザクション ページへのカスタム コントロールの追加</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="104">
          <source>You can add more information to a transaction page by using custom controls.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">カスタム コントロールを使用して、トランザクション ページにさらに情報を追加することができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="105">
          <source>You can add a custom control to a transaction page by using the screen layout designer.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">画面レイアウト デザイナーを使用して、トランザクション ページにカスタム コントロールを追加することができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="106">
          <source>In the designer, you can use a drag-and-drop operation to add the custom control, and then set the location, height, and width of the control.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">デザイナーで、ドラッグ アンド ドロップ操作を使用してカスタム コントロールを追加してから、コントロールの位置、高さ、および幅を設定できます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="107">
          <source>You can implement business logic for the custom control in your own extensions by using the POS extension framework.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">POS 拡張フレームワークを使用して、独自の拡張機能にカスタム コントロール用ビジネス ロジックを実装することができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="108">
          <source>This topic explains how to add a new custom control that shows the details for the selected line item, the item ID, and the description.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このトピックでは、選択した行の項目、項目 ID、および説明の詳細を示す新しいカスタム コントロールを追加する方法について説明します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="109">
          <source>This topic applies to Dynamics 365 for Finance and Operations, and to Microsoft Dynamics 365 for Retail with platform update 8 and Retail App update 4 hotfix.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このトピックでは Dynamics 365 for Finance and Operations および Microsoft Dynamics 365 for Retail プラットフォーム更新 8 と Retail アプリ更新プログラム 4 修正プログラムが適用されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="110">
          <source>Add a new custom control</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">新しいカスタム コントロールの追加</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="111">
          <source>Sign in to Dynamics 365 for Retail.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Dynamics 365 for Retail へサインインします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="112">
          <source>Select <bpt id="p1">**</bpt>Retail<ept id="p1">**</ept><ph id="ph1"> &gt; </ph><bpt id="p2">**</bpt>Channel setup<ept id="p2">**</ept><ph id="ph2"> &gt; </ph><bpt id="p3">**</bpt>POS setup<ept id="p3">**</ept><ph id="ph3"> &gt; </ph><bpt id="p4">**</bpt>POS<ept id="p4">**</ept><ph id="ph4"> &gt; </ph><bpt id="p5">**</bpt>Screen layouts<ept id="p5">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>Retail<ept id="p1">**</ept><ph id="ph1"> &gt; </ph><bpt id="p2">**</bpt>チャネル設定<ept id="p2">**</ept><ph id="ph2"> &gt; </ph><bpt id="p3">**</bpt>POS 設定<ept id="p3">**</ept><ph id="ph3"> &gt; </ph><bpt id="p4">**</bpt>POS<ept id="p4">**</ept><ph id="ph4"> &gt; </ph><bpt id="p5">**</bpt>画面レイアウト<ept id="p5">**</ept>と選択します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="113">
          <source>Select the <bpt id="p1">**</bpt>F3MGR<ept id="p1">**</ept> screen layout ID, and then, on the Action Pane, select <bpt id="p2">**</bpt>Designer<ept id="p2">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>F3MGR<ept id="p1">**</ept> 画面レイアウト ID を選択した後、アクション ウィンドウで <bpt id="p2">**</bpt>デザイナー<ept id="p2">**</ept> を選択します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="114">
          <source>Select <bpt id="p1">**</bpt>1440x960 – Full layout<ept id="p1">**</ept> as the layout size, and then select <bpt id="p2">**</bpt>Layout designer<ept id="p2">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">レイアウト サイズとして <bpt id="p1">**</bpt>1440 x 960: フル レイアウト<ept id="p1">**</ept> を選択し、<bpt id="p2">**</bpt>レイアウト デザイナー<ept id="p2">**</ept> を選択します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="115">
          <source>If you're prompted to install the designer tool, select <bpt id="p1">**</bpt>Open<ept id="p1">**</ept>, and follow the installation instructions.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">デザイナー ツールをインストールするように求められたら、<bpt id="p1">**</bpt>開く<ept id="p1">**</ept> を選択し、インストール手順に従います。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="116">
          <source>When you're prompted for your Microsoft Azure Active Directory (Azure AD) credentials, enter the information to start the designer.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Azure Active Directory (Azure AD) の資格情報の入力を要求するメッセージが表示されたら、その情報を入力してデザイナーを起動します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="117">
          <source>In the designer, drag the custom control from the left pane to the page, and then adjust, resize, or reposition the custom control as you require.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">デザイナーで、カスタム コントロールを左ウィンドウからページにドラッグして、必要に応じてカスタム コントロールを調整、サイズ変更、または位置変更します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="118">
          <source>On the page, right-click the custom control, and then select <bpt id="p1">**</bpt>Customize<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ページで、カスタム コントロールを右クリックし、<bpt id="p1">**</bpt>カスタマイズ<ept id="p1">**</ept>を選択します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="119">
          <source>In the dialog box, set these properties:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ダイアログ ボックスで、これらのプロパティを設定します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="120">
          <source><bpt id="p1">**</bpt>Control Name:<ept id="p1">**</ept> lineDetails</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>コントロール名:<ept id="p1">**</ept> lineDetails</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="121">
          <source><bpt id="p1">**</bpt>Package Name:<ept id="p1">**</ept> Pos_Extensibility_Samples</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>パッケージ名:<ept id="p1">**</ept> Pos_Extensibility_Samples</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="122">
          <source><bpt id="p1">**</bpt>Publisher Name:<ept id="p1">**</ept> Contoso</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>パブリッシャー名:<ept id="p1">**</ept> Contoso</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="123">
          <source>These names should match the names in the extension manifest.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">これらの名前は、拡張子マニフェスト内の名前と一致する必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="124">
          <source>Close the designer by selecting the <bpt id="p1">**</bpt>Close<ept id="p1">**</ept> button (<bpt id="p2">**</bpt>X<ept id="p2">**</ept>).</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>閉じる<ept id="p1">**</ept>ボタン (<bpt id="p2">**</bpt>X<ept id="p2">**</ept>) を選択し、デザイナーを閉じます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="125">
          <source>When you're prompted to save your changes, select <bpt id="p1">**</bpt>Yes<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">変更の保存を求められたら、<bpt id="p1">**</bpt>はい<ept id="p1">**</ept> を選択します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="126">
          <source>If you select <bpt id="p1">**</bpt>No<ept id="p1">**</ept>, your changes won't be saved.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>いいえ<ept id="p1">**</ept>を選択した場合、変更は保存されません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="127">
          <source>Select <bpt id="p1">**</bpt>Retail<ept id="p1">**</ept><ph id="ph1"> &gt; </ph><bpt id="p2">**</bpt>Retail IT<ept id="p2">**</ept><ph id="ph2"> &gt; </ph><bpt id="p3">**</bpt>Distribution schedule<ept id="p3">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>小売<ept id="p1">**</ept><ph id="ph1"> &gt; </ph><bpt id="p2">**</bpt>小売 IT<ept id="p2">**</ept><ph id="ph2"> &gt; </ph><bpt id="p3">**</bpt>配送スケジュール<ept id="p3">**</ept> の順に選択します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="128">
          <source>Select the <bpt id="p1">**</bpt>Registers (1090)<ept id="p1">**</ept> job, and then select <bpt id="p2">**</bpt>Run now<ept id="p2">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>1090 レジスター<ept id="p1">**</ept> ジョブを選択し、<bpt id="p2">**</bpt>今すぐ実行<ept id="p2">**</ept> を選択します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="129">
          <source>Add business logic to the custom control</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">カスタム コントロールへのビジネス ロジックの追加</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="130">
          <source>Start Microsoft Visual Studio 2015 as an administrator.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Microsoft Visual Studio 2015 を管理者として起動します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="131">
          <source>Open the <bpt id="p1">**</bpt>ModernPOS<ept id="p1">**</ept> solution from <bpt id="p2">**</bpt>…\RetailSDK\POS<ept id="p2">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>ModernPOS<ept id="p1">**</ept> ソリューションを <bpt id="p2">**</bpt>…\RetailSDK\POS<ept id="p2">**</ept> から開きます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="132">
          <source>In the <bpt id="p1">**</bpt>POS.Extensions<ept id="p1">**</ept> project, create a folder that is named <bpt id="p2">**</bpt>CustomControlExtensions<ept id="p2">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>POS.Extensions<ept id="p1">**</ept> プロジェクトで、<bpt id="p2">**</bpt>CustomControlExtensions<ept id="p2">**</ept> というフォルダーを作成します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="133">
          <source>In the <bpt id="p1">**</bpt>CustomControlExtensions<ept id="p1">**</ept> folder, create a folder that is named <bpt id="p2">**</bpt>Cart<ept id="p2">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>CustomControlExtensions<ept id="p1">**</ept> フォルダーで、<bpt id="p2">**</bpt>Cart<ept id="p2">**</ept> というフォルダーを作成します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="134">
          <source>In the <bpt id="p1">**</bpt>Cart<ept id="p1">**</ept> folder, create a Typescript file that is named <bpt id="p2">**</bpt>CartViewController.ts<ept id="p2">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>カート<ept id="p1">**</ept> フォルダーで、<bpt id="p2">**</bpt>CartViewController.ts<ept id="p2">**</ept> という Typescript ファイルを作成します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="135">
          <source>In the <bpt id="p1">**</bpt>CartViewController.ts<ept id="p1">**</ept> file, add the following <bpt id="p2">**</bpt>import<ept id="p2">**</ept> statement to import the relevant entities and context.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>CartViewController.ts<ept id="p1">**</ept> ファイルで、次の <bpt id="p2">**</bpt>import<ept id="p2">**</ept> ステートメントを追加して関連するエンティティおよびコンテキストをインポートします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="136">
          <source>Create a class that is named <bpt id="p1">**</bpt>CartViewController<ept id="p1">**</ept>, and extend it from <bpt id="p2">**</bpt>CartExtensionViewControllerBase<ept id="p2">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>CartViewController<ept id="p1">**</ept> という名前のクラスを作成し、<bpt id="p2">**</bpt>CartExtensionViewControllerBase<ept id="p2">**</ept> からクラスを拡張します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="137">
          <source>The <bpt id="p1">**</bpt>CartExtensionViewControllerBase<ept id="p1">**</ept> class contains the cart and tender lines, the cart line selected handler, and the cart line cleared handler.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>CartExtensionViewControllerBase<ept id="p1">**</ept> クラスには、買い物カゴおよび支払/入金の明細行、カートの明細行の選択ハンドラー、買い物カゴの明細行がクリアされたハンドラーが含まれています。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="138">
          <source>These elements will be used to show the selected line in the custom control.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">これらの要素は、カスタム コントロールで選択した行を表示するために使用されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="139">
          <source>In the <bpt id="p1">**</bpt>CartViewController<ept id="p1">**</ept> class, add two private variables to get the selected cart lines and tender lines.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>CartViewController<ept id="p1">**</ept> クラスで、選択したカート明細行および支払/入金明細行を取得する 2 つのプライベート変数を追加します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="140">
          <source>Create a class <bpt id="p1">**</bpt>constructor<ept id="p1">**</ept> method to set the cart and tender selection information.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">カートと入金の選択情報を設定するクラス <bpt id="p1">**</bpt>コンストラクター<ept id="p1">**</ept> メソッドを作成します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="141">
          <source>The overall class should look like this.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">全体的なクラスは、次のようになります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="142">
          <source>In the <bpt id="p1">**</bpt>Cart<ept id="p1">**</ept> folder, create an HTML file that is named <bpt id="p2">**</bpt>LineDetailsCustomControl.html<ept id="p2">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>カート<ept id="p1">**</ept> フォルダーで、<bpt id="p2">**</bpt>LineDetailsCustomControl.html<ept id="p2">**</ept> という HTML ファイルを作成します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="143">
          <source>In the <bpt id="p1">**</bpt>LineDetailsCustomControl.html<ept id="p1">**</ept> file, add two text fields to show the ID and description for the selected line item.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>LineDetailsCustomControl.html<ept id="p1">**</ept> ファイルで、選択した明細行項目の ID と説明を表示する 2 つのテキスト フィールドを追加します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="144">
          <source>Delete the default code, and add the following code.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">既定のコードを削除し、次のコードを追加します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="145">
          <source>Create a class, and extend it from <bpt id="p1">**</bpt>CartViewCustomControlBase<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">クラスを作成し、<bpt id="p1">**</bpt>CartViewCustomControlBase<ept id="p1">**</ept> からクラスを拡張します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="146">
          <source>Declare the following private variables to set the cart item ID and description.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">次のプライベート変数を宣言し、買い物カゴの品目 ID と説明を設定します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="147">
          <source>Create the <bpt id="p1">**</bpt>constructor<ept id="p1">**</ept> method to initialize and get the selected handler.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>コンストラクター<ept id="p1">**</ept> メソッドを作成して、選択したハンドラーを初期化して取得します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="148">
          <source>Add the <bpt id="p1">**</bpt>onReady<ept id="p1">**</ept> method to bind the control to the specified HTML element.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>onReady<ept id="p1">**</ept> メソッドを追加して、コントロールを指定した HTML 要素にバインドします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="149">
          <source>Add the <bpt id="p1">**</bpt>init<ept id="p1">**</ept> method to set the state.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>init<ept id="p1">**</ept> メソッドを追加して状態を設定します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="150">
          <source>The overall class should look like this.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">全体的なクラスは、次のようになります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="151">
          <source>In the <bpt id="p1">**</bpt>CustomControlExtensions<ept id="p1">**</ept> folder, create a JSON file that is named <bpt id="p2">**</bpt>manifest.json<ept id="p2">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>CustomControlExtensions<ept id="p1">**</ept> フォルダーで、<bpt id="p2">**</bpt>manifest.json<ept id="p2">**</ept> という JSON ファイルを作成します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="152">
          <source>In the <bpt id="p1">**</bpt>manifest.json<ept id="p1">**</ept> file, add the following code.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>manifest.json<ept id="p1">**</ept> ファイルに次のコードを追加します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="153">
          <source>In the <bpt id="p1">**</bpt>POS.Extensions<ept id="p1">**</ept> project, open the <bpt id="p2">**</bpt>extensions.json<ept id="p2">**</ept> file, and update it with the following <bpt id="p3">**</bpt>CustomControlExtensions<ept id="p3">**</ept> samples, so that the POS includes this extension at runtime.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>POS.Extensions<ept id="p1">**</ept> プロジェクトで <bpt id="p2">**</bpt>extensions.json<ept id="p2">**</ept> ファイルを開き、次の <bpt id="p3">**</bpt>CustomControlExtensions<ept id="p3">**</ept> サンプルで更新して、POS が実行時にこの拡張機能に含まれるようにします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="154">
          <source>In the <bpt id="p1">**</bpt>tsconfig.json<ept id="p1">**</ept> file, comment out the extension package folders in the exclude list.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>tsconfig.json<ept id="p1">**</ept> ファイルで、除外リストに拡張パッケージ フォルダーをコメントアウトします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="155">
          <source>The POS uses this file to include or exclude the extension.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">POS は、このファイルを使用して、拡張機能を追加または除外します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="156">
          <source>By default, the list contains the whole excluded extensions list.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">既定では、リストに除外された拡張リスト全体が含まれています。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="157">
          <source>To include an extension as part of the POS, add the name of the extension folder, and comment out the extension in the exclude list, as shown here.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">拡張機能を POS の一部として含めるには、次に示すように、拡張フォルダーの名前を追加し、除外リストの拡張子をコメントアウトします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="158">
          <source>Compile and rebuild the project.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">プロジェクトをコンパイル、およびリビルドします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="159">
          <source>Validate the customization</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">カスタマイズの検証</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="160">
          <source>Sign in to Retail Modern POS by using <bpt id="p1">**</bpt>000160<ept id="p1">**</ept> as the operator ID and <bpt id="p2">**</bpt>123<ept id="p2">**</ept> as the password.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">オペレーター ID に <bpt id="p1">**</bpt>000160<ept id="p1">**</ept>、パスワードに <bpt id="p2">**</bpt>123<ept id="p2">**</ept> を使用して Retail Modern POS にサインインします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="161">
          <source>On the <bpt id="p1">**</bpt>Welcome<ept id="p1">**</ept> screen, select the <bpt id="p2">**</bpt>Current transaction<ept id="p2">**</ept> button.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>ようこそ<ept id="p1">**</ept>画面で、<bpt id="p2">**</bpt>現在のトランザクション<ept id="p2">**</ept>ボタンを選択します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="162">
          <source>Add any item to the transaction, and then select the line item that you added.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">トランザクションを任意の品目に追加し、追加した明細行品目を選択します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="163">
          <source>The custom control should show the ID and description for the selected line item.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">カスタム コントロールには、選択した明細行品目の ID と説明が表示されます。</target></trans-unit>
      </group>
    </body>
  </file>
</xliff>