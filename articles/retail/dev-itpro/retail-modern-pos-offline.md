<?xml version="1.0" encoding="UTF-8"?>
<xliff xmlns:logoport="urn:logoport:xliffeditor:xliff-extras:1.0" xmlns:tilt="urn:logoport:xliffeditor:tilt-non-translatables:1.0" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns="urn:oasis:names:tc:xliff:document:1.2" xmlns:xliffext="urn:microsoft:content:schema:xliffextensions" version="1.2" xsi:schemaLocation="urn:oasis:names:tc:xliff:document:1.2 xliff-core-1.2-transitional.xsd">
  <file datatype="xml" source-language="en-US" original="retail-modern-pos-offline.md" target-language="ja-JP">
    <header>
      <tool tool-company="Microsoft" tool-version="1.0-7889195" tool-name="mdxliff" tool-id="mdxliff"/>
      <xliffext:skl_file_name>retail-modern-pos-offline.c09c3e.8e3b2fd2e6780570e3480c25df2e7bff42b4d4da.skl</xliffext:skl_file_name>
      <xliffext:version>1.2</xliffext:version>
      <xliffext:ms.openlocfilehash>8e3b2fd2e6780570e3480c25df2e7bff42b4d4da</xliffext:ms.openlocfilehash>
      <xliffext:ms.sourcegitcommit>9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b</xliffext:ms.sourcegitcommit>
      <xliffext:ms.lasthandoff>05/15/2019</xliffext:ms.lasthandoff>
      <xliffext:ms.openlocfilepath>articles\retail\dev-itpro\retail-modern-pos-offline.md</xliffext:ms.openlocfilepath>
    </header>
    <body>
      <group extype="content" id="content">
        <trans-unit xml:space="preserve" translate="yes" id="101" restype="x-metadata">
          <source>Retail Modern POS (MPOS) in offline mode</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">オフライン モードの Retail Modern POS (MPOS)</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="102" restype="x-metadata">
          <source>This article explains how to use Retail Modern POS devices in offline mode if the Retail Server is unavailable.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この記事では、Retail サーバーが利用できない場合に、オフライン モードで Retail Modern POS デバイスを使用する方法について説明します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="103">
          <source>Retail Modern POS (MPOS) in offline mode</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">オフライン モードの Retail Modern POS (MPOS)</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="104">
          <source>This topic explains how to use Retail Modern POS devices in offline mode if the Retail Server is unavailable.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このトピックでは、Retail サーバーが利用できない場合に、オフライン モードで Retail Modern POS デバイスを使用する方法について説明します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="105">
          <source>A Retail Modern POS device will go offline if the Retail Server is unavailable.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Retail サーバーが利用できない場合、Retail Modern POS はオフラインになります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="106">
          <source>When the connection with the Retail Server is lost, the point of sale (POS) automatically switches to the offline database.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Retail サーバーとの接続が失われると、販売時点管理 (POS) はオフライン データベースに自動的に接続されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="107">
          <source>If a data request doesn't succeed within the time-out interval that is configured in the offline profile, Retail Modern POS automatically switches to the offline database and continues the sales transaction.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">オフライン プロファイルでコンフィギュレーションされたタイムアウトの間隔内でデータの要求が成功しない場合、Retail Modern POS は自動的にオフライン データベースに切り替わり、販売トランザクションを続行します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="108">
          <source>Retail Modern POS will try to reconnect to the Retail Server after the reconnect attempt interval that is configured in the offline profile.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Retail Modern POS はオフライン プロファイルでコンフィギュレーションされた再接続試行間隔の後に Retail Server への再接続を試みます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="109">
          <source>This reconnect attempt will occur only at the beginning of a transaction.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この再接続の試みは、トランザクションの開始時にのみ発生します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="110">
          <source>Determine the connection mode of Retail Modern POS</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Retail Modern POS の接続モードを決定する</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="111">
          <source>The status header of Retail Modern POS indicates the current connection status.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Retail Modern POS のステータス ヘッダーは、現在の接続状態を示します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="112">
          <source><bpt id="p1">[</bpt><ph id="ph1">![</ph>connection<ept id="p1">](./media/connection.png)](./media/connection.png)</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">[</bpt><ph id="ph1">![</ph>接続<ept id="p1">](./media/connection.png)](./media/connection.png)</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="113">
          <source>The <bpt id="p1">**</bpt>Connection status<ept id="p1">**</ept> page in Retail Modern POS shows the status of the last attempt to synchronize with the offline database.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Retail Modern POS の<bpt id="p1">**</bpt>接続ステータス<ept id="p1">**</ept>ページには、オフライン データベースと同期する前回の試みのステータスが表示されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="114">
          <source><bpt id="p1">[</bpt><ph id="ph1">![</ph>connection status<ept id="p1">](./media/connection-status.png)](./media/connection-status.png)</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">[</bpt><ph id="ph1">![</ph>接続ステータス<ept id="p1">](./media/connection-status.png)](./media/connection-status.png)</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="115">
          <source>Create a button to manually switch between online and offline modes</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">手動でオンラインとオフライン モードを切り替えるためのボタンを作成</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="116">
          <source>You can add a button to Retail Modern POS to manually switch between online and offline modes.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Retail Modern POS にオンラインとオフライン モードを手動で切り替えるボタンを追加できます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="117">
          <source>Create a button for <bpt id="p1">**</bpt>POS operation 917 – Database connection status<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>POS 操作 917 – データベース接続ステータス<ept id="p1">**</ept>のボタンを作成します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="118">
          <source>Use the button as a toggle to connect or disconnect.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">接続または切断するには、ボタンをトグルとして切り替えて使用します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="119">
          <source>Operations that can be completed when the channel database is offline</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">チャネル データベースがオフラインのときに実行できる操作</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="120">
          <source>You can complete the following operations when the channel database is offline.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">チャネル データベースがオフラインときは、次の操作を完了することができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="121">
          <source>If any functionality requires Commerce Data Exchange: Real-time Service, you receive an error message that states that the operation isn't supported.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Commerce Data Exchange: リアルタイム サービスが必要な機能があれば、操作がサポートされていないことを示すエラー メッセージが表示されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="122">
          <source>An example of this is the Inventory Lookup operation.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この例は、在庫検索操作です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="123">
          <source>While the operation will allow you to look up an item, the Real-time Service call necessary to get available inventory data from the store's warehouse and the related store's warehouses as defined in the store's Fulfillment Group will fail if there is no connectivity to HQ.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">工程では品目の検索が許可されますが、HQ への接続がない場合、店舗の調達グループで定義された店舗の倉庫と関連する店舗の倉庫から入手可能な在庫データに必要なリアルタイム サービス コールは失敗します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="124">
          <source><bpt id="p1">**</bpt>Tip:<ept id="p1">**</ept> Reports and other operations will act only on the data that is available in the offline database.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>ヒント:<ept id="p1">**</ept> オフライン データベースで使用できるデータにのみ、レポートおよびその他の操作が実行されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="125">
          <source>Operation ID</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">操作 ID</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="126">
          <source>Description</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">説明</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="127">
          <source>100</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">100</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="128">
          <source>Product sale</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">製品売上</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="129">
          <source>101</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">101</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="130">
          <source>Price check</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">価格の確認</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="131">
          <source>102</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">102</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="132">
          <source>Void product</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">製品の無効化</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="133">
          <source>103</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">103</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="134">
          <source>Product comment</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">製品コメント</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="135">
          <source>104</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">104</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="136">
          <source>Price override</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">価格変更</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="137">
          <source>105</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">105</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="138">
          <source>Set quantity</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">数量の設定</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="139">
          <source>106</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">106</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="140">
          <source>Clear quantity</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">数量のクリア</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="141">
          <source>108</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">108</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="142">
          <source>Product search</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">製品検索</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="143">
          <source>109</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">109</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="144">
          <source>Return product</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">返品</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="145">
          <source>115</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">115</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="146">
          <source>Show journal</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">仕訳帳の表示</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="147">
          <source>117</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">117</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="148">
          <source>Add loyalty card</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ロイヤルティ カードの追加</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="149">
          <source>123</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">123</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="150">
          <source>Change unit of measure</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">単位の変更</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="151">
          <source>128</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">128</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="152">
          <source>Override transaction tax from list</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">リストから取引税を上書きする</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="153">
          <source>130</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">130</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="154">
          <source>Override line product tax from list</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">リストから明細行の製品税を上書きする</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="155">
          <source>132</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">132</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="156">
          <source>Deposit override</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">預金の上書き</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="157">
          <source>134</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">134</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="158">
          <source>Add affiliation</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">所属を追加</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="159">
          <source>135</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">135</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="160">
          <source>Add affiliation from list</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">リストから所属を追加</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="161">
          <source>200</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">200</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="162">
          <source>Pay cash</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">現金で支払う</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="163">
          <source>202</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">202</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="164">
          <source>Pay customer account</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">顧客口座から支払う</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="165">
          <source>203</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">203</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="166">
          <source>Pay currency</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">各種通貨で支払う</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="167">
          <source>206</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">206</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="168">
          <source>Pay cash quick</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">現金で即支払う</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="169">
          <source>211</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">211</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="170">
          <source>Void payment</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">支払の無効化</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="171">
          <source>214</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">214</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="172">
          <source>Pay gift card</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ギフト カードで支払う</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="173">
          <source>300</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">300</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="174">
          <source>Line discount amount</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">品目割引金額</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="175">
          <source>301</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">301</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="176">
          <source>Line discount percent</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">品目割引率</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="177">
          <source>302</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">302</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="178">
          <source>Total discount amount</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">合計割引金額</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="179">
          <source>303</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">303</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="180">
          <source>Total discount percent</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">合計割引率</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="181">
          <source>500</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">500</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="182">
          <source>Void transaction</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">トランザクションの無効化</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="183">
          <source>501</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">501</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="184">
          <source>Transaction comment</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">トランザクション コメント</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="185">
          <source>503</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">503</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="186">
          <source>Suspend transaction</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">トランザクションの中断</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="187">
          <source>512</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">512</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="188">
          <source>Issue gift card</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ギフト カードの発行</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="189">
          <source>515</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">515</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="190">
          <source>Recall order</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">注文の取り消し</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="191">
          <source>519</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">519</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="192">
          <source>Add to gift card</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ギフト カードに追加</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="193">
          <source>520</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">520</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="194">
          <source>Gift card balance</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ギフト カード残高</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="195">
          <source>602</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">602</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="196">
          <source>Customer search</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">顧客検索</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="197">
          <source>603</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">603</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="198">
          <source>Customer clear</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">顧客のクリア</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="199">
          <source>612</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">612</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="200">
          <source>Customer add</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">顧客の追加</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="201">
          <source>622</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">622</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="202">
          <source>Search</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">検索</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="203">
          <source>623</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">623</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="204">
          <source>Edit customer</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">顧客の編集</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="205">
          <source>701</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">701</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="206">
          <source>Log off</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ログオフ</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="207">
          <source>703</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">703</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="208">
          <source>Lock register</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">レジスターのロック</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="209">
          <source>801</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">801</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="210">
          <source>Inventory lookup</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">在庫検索</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="211">
          <source>802</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">802</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="212">
          <source>Stock count</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">在庫数</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="213">
          <source>917</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">917</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="214">
          <source>Database connection status</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">データベース接続ステータス</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="215">
          <source>920</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">920</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="216">
          <source>Time clock</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">タイム レコーダー</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="217">
          <source>921</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">921</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="218">
          <source>View time clock entries</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">タイム レコーダー エントリの表示</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="219">
          <source>922</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">922</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="220">
          <source>View product details</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">製品の詳細表示</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="221">
          <source>1003</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">1003</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="222">
          <source>View reports</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">レポートの表示</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="223">
          <source>1052</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">1052</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="224">
          <source>Tender declaration</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">支払/入金申告</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="225">
          <source>1200</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">1200</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="226">
          <source>Declare start amount</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">開始金額の申告</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="227">
          <source>1201</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">1201</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="228">
          <source>Float entry</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">釣銭入力</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="229">
          <source>1210</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">1210</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="230">
          <source>Tender removal</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">支払/入金の削除</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="231">
          <source>1211</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">1211</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="232">
          <source>Safe drop</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">金庫保管</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="233">
          <source>1212</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">1212</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="234">
          <source>Bank drop</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">銀行入金</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="235">
          <source>Operations that can’t be completed when the channel database is offline</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">チャネル データベースがオフラインのときに実行できない操作</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="236">
          <source>You can’t complete the following operations when the channel database is offline.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">チャネル データベースがオフラインときは、次の操作を完了することができません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="237">
          <source>Operation ID</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">操作 ID</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="238">
          <source>Description</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">説明</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="239">
          <source>207</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">207</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="240">
          <source>Pay loyalty card</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ロイヤルティ カードで支払う</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="241">
          <source>707</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">707</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="242">
          <source>Activate device</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">デバイスのアクティブ化</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="243">
          <source>708</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">708</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="244">
          <source>Inactivate device</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">デバイスの無効化</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="245">
          <source>1053</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">1053</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="246">
          <source>Blind close shift</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">シフトのブラインド クローズ</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="247">
          <source>1054</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">1054</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="248">
          <source>Suspend shift</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">シフトの中断</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="249">
          <source>1055</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">1055</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="250">
          <source>Close shift</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">シフトのクローズ</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="251">
          <source>1056</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">1056</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="252">
          <source>Print X</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">X の印刷</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="253">
          <source>1057</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">1057</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="254">
          <source>Reprint Z</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">再印刷 Z</target></trans-unit>
      </group>
    </body>
  </file>
</xliff>