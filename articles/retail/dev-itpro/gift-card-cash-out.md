<?xml version="1.0" encoding="UTF-8"?>
<xliff xmlns:logoport="urn:logoport:xliffeditor:xliff-extras:1.0" xmlns:tilt="urn:logoport:xliffeditor:tilt-non-translatables:1.0" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns="urn:oasis:names:tc:xliff:document:1.2" xmlns:xliffext="urn:microsoft:content:schema:xliffextensions" version="1.2" xsi:schemaLocation="urn:oasis:names:tc:xliff:document:1.2 xliff-core-1.2-transitional.xsd">
  <file datatype="xml" source-language="en-US" original="gift-card-cash-out.md" target-language="ja-JP">
    <header>
      <tool tool-company="Microsoft" tool-version="1.0-7889195" tool-name="mdxliff" tool-id="mdxliff"/>
      <xliffext:skl_file_name>gift-card-cash-out.8eb99d.738ac29b38fcfea0ee13687ddf3b1b8d8532637b.skl</xliffext:skl_file_name>
      <xliffext:version>1.2</xliffext:version>
      <xliffext:ms.openlocfilehash>738ac29b38fcfea0ee13687ddf3b1b8d8532637b</xliffext:ms.openlocfilehash>
      <xliffext:ms.sourcegitcommit>9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b</xliffext:ms.sourcegitcommit>
      <xliffext:ms.lasthandoff>05/15/2019</xliffext:ms.lasthandoff>
      <xliffext:ms.openlocfilepath>articles\retail\dev-itpro\gift-card-cash-out.md</xliffext:ms.openlocfilepath>
    </header>
    <body>
      <group extype="content" id="content">
        <trans-unit xml:space="preserve" translate="yes" id="101" restype="x-metadata">
          <source>Cash out gift card balance for a retail customer</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">小売顧客のギフト カードの残高を清算します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="102" restype="x-metadata">
          <source>This topic provides information about the cash out gift card functionality that is available in Microsoft Dynamics 365 for Retail.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このトピックでは、Microsoft Dynamics 365 for Retail で現在利用できる外部ギフト カード清算機能について説明します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="103">
          <source>Cash out gift card balance for a retail customer</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">小売顧客のギフト カードの残高を清算します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="104">
          <source>This topic provides an overview of the cash out gift card feature for the Dynamics 365 for Retail Modern POS (MPOS).</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このトピックは、Dynamics 365 for Retail Modern POS (MPOS) のギフト カード清算機能の概要を提供します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="105">
          <source>The purpose of the cash out feature is to allow cashiers to cash out the remaining amount on a gift card.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">清算機能の目的は、レジ担当者がギフト カードにある残額の清算を許可することです。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="106">
          <source>Retailers often need to exchange a low balance gift card for cash at the customer's request.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">小売業者は顧客の要望により、ギフト カードにあるさほど多くない残高を交換する必要がよくあります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="107">
          <source>Prerequisites</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">必要条件</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="108">
          <source>The payment connector and corresponding payment gateway or processor must support the feature.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">支払コネクタおよび対応する支払ゲートウェイまたはプロセッサは、機能をサポートする必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="109">
          <source>The <bpt id="p1">*</bpt>payment connector<ept id="p1">*</ept> is an extension which facilitates communication between Dynamics 365 for Retail (and associated components) and a payment service.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">*</bpt>支払コネクタ<ept id="p1">*</ept>は、Dynamics 365 for Retail (および関連コンポーネント) と支払サービスの間の通信を促進する拡張機能です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="110">
          <source>The connector described in this topic was implemented using the standard payments SDK.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このトピックで説明されているコネクタは、標準支払 SDK を使用して実装されています。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="111">
          <source>If the gift cards are external gift cards, the external gift card must be configured for both the Retail headquarters and the POS.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ギフト カードが外部のギフト カードの場合は、小売用バック オフィスと、POSの両方を外部のギフト カードにコンフィギュレーションする必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="112">
          <source>Before the gift card can be configured, the retailer must have an account with an external gift card service provider.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ギフト カードをコンフィギュレーションする前に、小売業者は外部のギフト カード サービス プロバイダーのアカウントが必要です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="113">
          <source>Scenarios</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">シナリオ</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="114">
          <source>The cash out gift card feature is applicable to a scenario where, for example, in Washington state, the cash out threshold is $5.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ギフト カード清算機能は、たとえば、ワシントン州では清算しきい値を $5 にする、といったシナリオに適用されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="115">
          <source>Retailers in this case will have the option to set up an operation to cash out a gift card and set the gift card balance limits under which the cash out operation can be enabled.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この場合、小売業者には、ギフト カードを清算し、清算業務が有効となるギフト カード残高の限度額の操作を設定するオプションがあります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="116">
          <source>Configure Retail headquarters</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Retail Headquarters のコンフィギュレーション</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="117">
          <source>Open the <bpt id="p1">**</bpt>All retail stores<ept id="p1">**</ept> page.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>すべての小売店舗<ept id="p1">**</ept>ページを開きます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="118">
          <source>In the list, select the <bpt id="p1">**</bpt>Houston<ept id="p1">**</ept> store.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">一覧で、<bpt id="p1">**</bpt>ヒューストン<ept id="p1">**</ept>の店舗を選択します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="119">
          <source>On the <bpt id="p1">**</bpt>Action Pane<ept id="p1">**</ept>, select <bpt id="p2">**</bpt>Set up<ept id="p2">**</ept> <ph id="ph1">&amp;gt;</ph> <bpt id="p3">**</bpt>Payment methods<ept id="p3">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>アクション ウィンドウ<ept id="p1">**</ept>で、<bpt id="p2">**</bpt>設定<ept id="p2">**</ept> <ph id="ph1">&amp;gt;</ph> <bpt id="p3">**</bpt>支払方法<ept id="p3">**</ept>を選択します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="120">
          <source>Search for <bpt id="p1">**</bpt>payment methods<ept id="p1">**</ept> to open the <bpt id="p2">**</bpt>Payment methods<ept id="p2">**</ept> page.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>支払方法<ept id="p1">**</ept> を検索して <bpt id="p2">**</bpt>支払方法<ept id="p2">**</ept> ページを開きます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="121">
          <source>Select the <bpt id="p1">**</bpt>Gift Card<ept id="p1">**</ept> payment method, and then follow these steps:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>ギフト カード<ept id="p1">**</ept>支払方法を選択し、次の手順を完了します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="122">
          <source>In the <bpt id="p1">**</bpt>Amount<ept id="p1">**</ept> FastTab section, select the <bpt id="p2">**</bpt>Cash Out Gift Card<ept id="p2">**</ept> field.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>金額<ept id="p1">**</ept>クイック タブ セクションで、<bpt id="p2">**</bpt>ギフト カードを清算<ept id="p2">**</ept>フィールドを選択します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="123">
          <source>In the <bpt id="p1">**</bpt>Cash Out Gift Card<ept id="p1">**</ept> field, enter the <bpt id="p2">**</bpt>Gift card Cash out threshold<ept id="p2">**</ept> amount.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>ギフト カードを清算<ept id="p1">**</ept>フィールドに、<bpt id="p2">**</bpt>ギフト カード清算しきい値<ept id="p2">**</ept>の額を入力します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="124">
          <source>Select <bpt id="p1">**</bpt>Save<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>保存<ept id="p1">**</ept> を選択します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="125">
          <source>Setting the Gift card threshold</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ギフト カードのしきい値を設定</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="126">
          <source>Open the <bpt id="p1">**</bpt>Button grid<ept id="p1">**</ept> page.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>ボタン グリッド<ept id="p1">**</ept>ページを開きます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="127">
          <source>In the navigation bar on the left side of the page, search for <bpt id="p1">**</bpt>F2S1M<ept id="p1">**</ept>, and select the filtered option.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ページの左側にあるナビゲーション バーで、<bpt id="p1">**</bpt>F2S1M<ept id="p1">**</ept> を検索してフィルター処理オプションを選択します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="128">
          <source>On the <bpt id="p1">**</bpt>Action Pane<ept id="p1">**</ept>, select <bpt id="p2">**</bpt>Designer<ept id="p2">**</ept> to download the button designer application.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>アクション ウィンドウ<ept id="p1">**</ept>で、<bpt id="p2">**</bpt>デザイナー<ept id="p2">**</ept>を選択し、ボタン デザイナー アプリケーションをダウンロードします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="129">
          <source>When the grid designer appears, right-click on an empty (gray) area, and then select <bpt id="p1">**</bpt>New button<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">グリッド デザイナーが表示されたら、空の (灰色) 領域を右クリックして、<bpt id="p1">**</bpt>新規作成ボタン<ept id="p1">**</ept> を選択します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="130">
          <source>New button</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">新しいボタン</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="131">
          <source>Right-click the new button, and then select <bpt id="p1">**</bpt>Button properties<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">新しいボタンを右クリックし、<bpt id="p1">**</bpt>ボタン プロパティ<ept id="p1">**</ept> を選択します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="132">
          <source>Set the <bpt id="p1">**</bpt>Action<ept id="p1">**</ept>, <bpt id="p2">**</bpt>Cash out gift card<ept id="p2">**</ept>, and <bpt id="p3">**</bpt>Text on button<ept id="p3">**</ept> properties according to the following matrix.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">次のマトリックスに従って<bpt id="p1">**</bpt>アクション<ept id="p1">**</ept>、<bpt id="p2">**</bpt>支払タイプ<ept id="p2">**</ept>、および<bpt id="p3">**</bpt>ボタンのテキスト<ept id="p3">**</ept>プロパティを設定します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="133">
          <source>Action</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">アクション</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="134">
          <source>Payment type</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">支払タイプ</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="135">
          <source>Text on button</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ボタンのテキスト</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="136">
          <source>Cash out gift card</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ギフト カードをキャッシュ アウトする</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="137">
          <source>Gift Card</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ギフト カード</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="138">
          <source>Cash out gift card</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ギフト カードをキャッシュ アウトする</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="139">
          <source>When you've finished, your button layout should resemble the following illustration.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">完了したら、ボタンのレイアウトは次の図のようになります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="140">
          <source>Completed button layout</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">完了したボタン レイアウト</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="141">
          <source>Click <bpt id="p1">**</bpt>Ok<ept id="p1">**</ept> and close the designer.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>OK<ept id="p1">**</ept> をクリックし、デザイナーを閉じます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="142">
          <source>Search for <bpt id="p1">**</bpt>Distribution Schedule<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>配送スケジュール<ept id="p1">**</ept>を検索します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="143">
          <source>In the navigation bar on the left side of the page, search for <bpt id="p1">**</bpt>1090<ept id="p1">**</ept>, <bpt id="p2">**</bpt>1115<ept id="p2">**</ept>, and <bpt id="p3">**</bpt>1070<ept id="p3">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ページの左側にあるナビゲーション バーで、<bpt id="p1">**</bpt>1090<ept id="p1">**</ept>、<bpt id="p2">**</bpt>1115<ept id="p2">**</ept>、および <bpt id="p3">**</bpt>1070<ept id="p3">**</ept> を検索します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="144">
          <source>On the <bpt id="p1">**</bpt>Action Pane<ept id="p1">**</ept>, select <bpt id="p2">**</bpt>Run now<ept id="p2">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>アクション ウィンドウ<ept id="p1">**</ept>で、<bpt id="p2">**</bpt>今すぐ実行<ept id="p2">**</ept>を選択します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="145">
          <source>Check the status of the job by searching for <bpt id="p1">**</bpt>Download sessions<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>ダウンロード セッション<ept id="p1">**</ept>を検索してジョブのステータスを確認してください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="146">
          <source>Wait until <bpt id="p1">**</bpt>Applied<ept id="p1">**</ept> appears next to all the jobs, and then close the browser.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">すべてのジョブの横に <bpt id="p1">**</bpt>適用済<ept id="p1">**</ept> が表示されるまで待ってから、ブラウザーを閉じます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="147">
          <source>Configure and test Retail Modern POS</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Retail Modern POS のコンフィギュレーションとテスト</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="148">
          <source>Start the Retail Modern POS (MPOS) application.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Retail Modern POS の申請を開始</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="149">
          <source>Sign in by using the standard credentials.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">標準の資格情報を使用してログインします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="150">
          <source>When you're prompted, select <bpt id="p1">**</bpt>Perform a non-drawer operation<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">メッセージが表示されたら、<bpt id="p1">**</bpt>ドロワー以外の操作の実行<ept id="p1">**</ept> を選択します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="151">
          <source>On the main screen, select <bpt id="p1">**</bpt>Select hardware station<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">メイン画面で、<bpt id="p1">**</bpt>ハードウェア ステーションの選択<ept id="p1">**</ept>を選択します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="152">
          <source>On the bar on the right side of the page, select <bpt id="p1">**</bpt>Manage<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ページの右側にあるバーで、<bpt id="p1">**</bpt>管理<ept id="p1">**</ept>を選択します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="153">
          <source>Turn on <bpt id="p1">**</bpt>Virtual Peripherals<ept id="p1">**</ept>, and then select <bpt id="p2">**</bpt>OK<ept id="p2">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>仮想周辺機器<ept id="p1">**</ept> をオンにし、<bpt id="p2">**</bpt>OK<ept id="p2">**</ept> を選択します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="154">
          <source>In the <bpt id="p1">**</bpt>Available paired stations<ept id="p1">**</ept> field, select <bpt id="p2">**</bpt>Virtual Peripherals<ept id="p2">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>使用可能なペアリング済ステーション<ept id="p1">**</ept> フィールドで、<bpt id="p2">**</bpt>仮想周辺機器<ept id="p2">**</ept>を選択します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="155">
          <source>You're prompted to either open a new shift or perform non-drawer operations.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">新しいシフトを開くか、非ドロワー操作を実行するように求められます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="156">
          <source>You can now open a new shift.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">新しいシフトを開くことができるようになりました。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="157">
          <source>On the main screen, select <bpt id="p1">**</bpt>Current transaction<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">メイン画面で、<bpt id="p1">**</bpt>現在のトランザクション<ept id="p1">**</ept>を選択します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="158">
          <source>Select <bpt id="p1">**</bpt>Gift cards<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>ギフト カード<ept id="p1">**</ept> を選択します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="159">
          <source>Select <bpt id="p1">**</bpt>Cash out gift card<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>ギフト カードの清算<ept id="p1">**</ept>を選択します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="160">
          <source>Enter or scan the gift number.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ギフト番号を入力もしくはスキャンします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="161">
          <source>The line for <bpt id="p1">**</bpt>gift card cash out<ept id="p1">**</ept> will be added to the <bpt id="p2">**</bpt>Current transaction<ept id="p2">**</ept> for cash out.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p2">**</bpt>現在のトランザクション<ept id="p2">**</ept>に、清算用の<bpt id="p1">**</bpt>ギフト カードの清算<ept id="p1">**</ept>行が追加されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="162">
          <source>Select the <bpt id="p1">**</bpt>Cash<ept id="p1">**</ept> payment method and the drawer will open when the transaction is completed.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>現金<ept id="p1">**</ept>支払メソッドを選択すると、トランザクションの完了時にドロワーが開きます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="163">
          <source><ph id="ph1">![</ph>Completed button layout<ph id="ph2">](./media/GiftCardCashout03.png)</ph></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><ph id="ph1">![</ph>完了したボタン レイアウト<ph id="ph2">](./media/GiftCardCashout03.png)</ph></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="164">
          <source>Troubleshooting</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">トラブルシューティング</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="165">
          <source>For all general issues, you should always consult the Modern POS or IIS Hardware Station event logs.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">すべての一般的な問題については、Modern POS または IIS ハードウェア ステーション イベント ログを常に参照してください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="166">
          <source>The logs can be found under these nodes in the Windows event log:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ログは、Windows イベント ログの以下のノードにあります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="167">
          <source><bpt id="p1">**</bpt>Application and Services Logs &gt; Microsoft &gt; Dynamics &gt; Commerce-ModernPOS<ept id="p1">**</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>Application and Services Logs &gt; Microsoft &gt; Dynamics &gt; Commerce-ModernPOS<ept id="p1">**</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="168">
          <source><bpt id="p1">**</bpt>Application and Services Logs &gt; Microsoft &gt; Dynamics &gt; Commerce-Hardware Station<ept id="p1">**</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>Application and Services Logs &gt; Microsoft &gt; Dynamics &gt; Commerce-Hardware Station<ept id="p1">**</ept></target></trans-unit>
      </group>
    </body>
  </file>
</xliff>