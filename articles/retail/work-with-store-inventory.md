<?xml version="1.0" encoding="UTF-8"?>
<xliff xmlns:logoport="urn:logoport:xliffeditor:xliff-extras:1.0" xmlns:tilt="urn:logoport:xliffeditor:tilt-non-translatables:1.0" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns="urn:oasis:names:tc:xliff:document:1.2" xmlns:xliffext="urn:microsoft:content:schema:xliffextensions" version="1.2" xsi:schemaLocation="urn:oasis:names:tc:xliff:document:1.2 xliff-core-1.2-transitional.xsd">
  <file datatype="xml" source-language="en-US" original="work-with-store-inventory.md" target-language="ja-JP">
    <header>
      <tool tool-company="Microsoft" tool-version="1.0-7889195" tool-name="mdxliff" tool-id="mdxliff"/>
      <xliffext:skl_file_name>work-with-store-inventory.418f90.551a8408aa730bc1916f1c57b7cfd773966ce8bf.skl</xliffext:skl_file_name>
      <xliffext:version>1.2</xliffext:version>
      <xliffext:ms.openlocfilehash>551a8408aa730bc1916f1c57b7cfd773966ce8bf</xliffext:ms.openlocfilehash>
      <xliffext:ms.sourcegitcommit>e2fb0846fcc6298050a0ec82c302e5eb5254e0b5</xliffext:ms.sourcegitcommit>
      <xliffext:ms.lasthandoff>05/27/2019</xliffext:ms.lasthandoff>
      <xliffext:ms.openlocfilepath>articles\retail\work-with-store-inventory.md</xliffext:ms.openlocfilepath>
    </header>
    <body>
      <group extype="content" id="content">
        <trans-unit xml:space="preserve" translate="yes" id="101" restype="x-metadata">
          <source>Store inventory management</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">店舗在庫管理</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="102" restype="x-metadata">
          <source>This topic describes the types of documents that you can use to manage inventory.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このトピックでは、在庫の管理に使用できるドキュメントのタイプについて説明します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="103">
          <source>Store inventory management</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">店舗在庫管理</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="104">
          <source>When working with inventory in Dynamics 365 for Retail and using the POS application, it is important to note that POS provides limited support for inventory dimensions and certain inventory item types.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Dynamics 365 for Retail で在庫処理および POS アプリケーションを使用する場合、POS は在庫分析コードおよび特定の在庫品目タイプに対して限定的なサポートを提供することに注意することが重要です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="105">
          <source>The POS solution does not support the following item configurations:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">POS ソリューションは、以下の品目構成をサポートしません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="106">
          <source>BOM items (except kit products, which utilize some components of the BOM framework)</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">BOM 品目 (BOM フレームワークの一部のコンポーネントを利用するキット製品を除く)</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="107">
          <source>Catch weight items</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">CW 品目</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="108">
          <source>Batch-controlled items</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">バッチ管理されている品目</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="109">
          <source>The POS application currently does not support the following tracking dimensions in the POS:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">POS アプリケーションは現在、POS の次の追跡用分析コードをサポートしていません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="110">
          <source>Batch tracking dimension</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">バッチ追跡用分析コード</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="111">
          <source>Owner dimension</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">所有者分析コード</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="112">
          <source>The POS solution provides limited support for the following dimensions.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">POS ソリューションは、以下の分析コードに対して限定的なサポートを提供します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="113">
          <source>Limited support indicates that the POS may default some of these dimensions into inventory transactions automatically based on warehouse/store setup configuration.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">限定的なサポートということは、POS が倉庫/店舗のセットアップ構成に基づいて自動的に在庫トランザクションにこれらの分析コードのいくつかを既定設定する可能性を示しています。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="114">
          <source>POS will not fully support the dimensions in the way they are supported if a sales transaction is manually entered into the ERP.</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">POSは、販売トランザクションが手動で ERP に入力された場合のような方法で分析コードを完全にはサポートしません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="115">
          <source><bpt id="p1">**</bpt>Warehouse Location<ept id="p1">**</ept> – Users will not have the ability to manage the receiving warehouse location for items received into a store warehouse when the store has not been configured to use the warehouse management process.</source><target logoport:matchpercent="98" state="translated" state-qualifier="fuzzy-match"><bpt id="p1">**</bpt>倉庫の場所<ept id="p1">**</ept> – 店舗が倉庫管理プロセスを使用するよう構成されていない場合、ユーザーは、店舗の倉庫入荷された品目について、入荷倉庫の場所を管理することはできなくなります。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="116">
          <source>A default receiving location defined on the store warehouse will be used for these items.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">これらの品目に対しては、店舗の倉庫で定義されている既定の入荷場所が使用されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="117">
          <source>If the warehouse management process has been enabled for the store, limited support that prompts the user to choose a receiving location for the entire receipt will be triggered.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">店舗に対して倉庫管理プロセスが有効になっている場合、入荷全体の入荷場所を選択するようユーザーに促す制限付きサポートが発生します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="118">
          <source>Items sold from the store will always be sold out of the default retail location as defined on the store warehouse setup.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">店舗で販売された品目は、常に店舗倉庫の設定で定義された既定の小売場所から販売されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="119">
          <source>The location for managing return inventory can be controlled through default return location definition on the store warehouse or based on return reason codes as defined in the return location policy.</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">返品在庫を管理する場所は、店舗倉庫における既定の返品場所の定義により、また返品場所のポリシーに定義されている返品理由コードに基づいて制御されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="120">
          <source><bpt id="p1">**</bpt>License plate<ept id="p1">**</ept> – License plates are only applicable when <bpt id="p2">**</bpt>Use warehouse management process<ept id="p2">**</ept> has been enabled on the item and the store warehouse.</source><target logoport:matchpercent="98" state="translated" state-qualifier="fuzzy-match"><bpt id="p1">**</bpt>ライセンス プレート<ept id="p1">**</ept> – ライセンス プレートは商品と店舗倉庫で<bpt id="p2">**</bpt>倉庫管理プロセスを使用<ept id="p2">**</ept>が有効になっている場合にのみ適用可能。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="121">
          <source>In POS, if inventory is received into a store warehouse where the warehouse management process has been enabled, and the location chosen to receive the item into is tied to a location profile that requires license plate control, the POS application will systematically apply a license plate to the receiving line.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">POS では、倉庫管理プロセスが有効になっている店舗倉庫に在庫が入庫し、品目を入荷するように選択されている場所がライセンス プレート制御を必要とする場所プロファイルに関連付けられている場合、POSアプリケーションは体系的にライセンス プレートを入荷明細行に適用します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="122">
          <source>Users in POS will not have the ability to change or manage this license plate data.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">POS のユーザーは、このライセンス プレート データの変更または管理をすることはできません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="123">
          <source>If full management of license plates is required, it is suggested the store use the WMS mobile application or the back office ERP client to manage the receipt of these items.</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">ライセンス プレートの完全な管理が必要な場合、店舗は WMS モバイル アプリケーションまたはバック オフィス ERP クライアントを使用して、品目の入荷を管理するよう推奨されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="124">
          <source><bpt id="p1">**</bpt>Serial number<ept id="p1">**</ept> – The POS application has limited support for single serial number to be registered on a transaction sales line for orders created in POS with serialized items.</source><target logoport:matchpercent="98" state="translated" state-qualifier="fuzzy-match"><bpt id="p1">**</bpt>シリアル番号<ept id="p1">**</ept> – POS アプリケーションでは、POS でシリアル化した品目と共に作成された注文のトランザクション販売明細行には 1 つのシリアル番号が登録されるようにサポートが制限されています。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="125">
          <source>This serial number is not validated against registered serial numbers already in inventory.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このシリアル番号は、既に在庫に登録されているシリアル番号に対しては検証されていません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="126">
          <source>If a sales order is created in the call center channel or fulfilled through the ERP and multiple serial numbers are registered to a single sales line during the fulfillment process in the ERP, these serial numbers will not be able to be applied or validated if a return is processed in POS for these orders.</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">販売注文がコール センター チャネルで作成された場合またはERPにより履行され、ERP のフルフィルメント プロセスにおいて複数のシリアル番号が 1 つの販売明細行に登録された場合、これらの注文に対して POS で返品が処理されている時はシリアル番号は適用されないか検証されません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="127">
          <source><bpt id="p1">**</bpt>Inventory status<ept id="p1">**</ept> – For items that use the warehouse management process and require an inventory status, this status field is not able to be set or modified through the POS application.</source><target logoport:matchpercent="98" state="translated" state-qualifier="fuzzy-match"><bpt id="p1">**</bpt>在庫状態<ept id="p1">**</ept> – 倉庫管理プロセスを使用し、在庫状態が必要な品目の場合、このステータスフィールドは POS アプリケーションにより設定または変更することはできません。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="128">
          <source>The default inventory status as defined on the store warehouse configuration will be used when items are received into inventory.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">店舗倉庫コンフィギュレーションで定義されている既定の在庫ステータスは、品目が在庫に入荷される時に使用されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="129">
          <source>All organizations must test item configurations through POS in development or test environments before deploying them to production.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">すべての組織は、POS を通して本番環境の展開前に、開発環境またはテスト環境で品目コンフィギュレーションをテストする必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="130">
          <source>Test your items by performing regular cash and carry sales transacting and creating customer orders (if applicable) through the POS with your items.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">通常の現金払いの販売トランザクションを実行したり、POS を通して商品の顧客注文(該当する場合)を作成したりして、品目のテストをします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="131">
          <source>Testing must include running a full statement posting processes in your test environment and verifying that there are no issues.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">テストには、テスト環境で明細書転記プロセスを完全に実行し、問題がないことを確認する必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="132">
          <source>Configuring items in a way that is not supported by the POS application, without proper testing, can result in your statement posting process failing in production without an easy way to correct the issues.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">適切なテストを行わずに、POS アプリケーションでサポートされていない方法でアイテムを構成すると、問題を修正する簡単な方法がないまま、明細書転記プロセスが生産に失敗する可能性があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="133">
          <source>Partner or customer customizations to the application may optionally be considered to allow these posting processes to successfully complete.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">アプリケーションに対するパートナーまたは顧客のカスタマイズは、これらの転記プロセスが正常に完了させるために必要に応じて考慮することができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="134">
          <source>If customizations are not needed, the organization must ensure that the product configuration of your products has been done in a way that is supported by the standard POS application/order creation/statement posting process.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">カスタマイズが不要な場合、組織は標準の POS アプリケーション/注文の作成/明細書転記プロセスでサポートされている方法で製品の製品コンフィギュレーションが行われていることを確認する必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="135">
          <source>Purchase orders</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">発注書</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="136">
          <source>Purchase orders are created at the head office.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">発注書は本社で作成されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="137">
          <source>If a retail warehouse is included in the purchase order header, the order can be received at the store by using Modern POS (MPOS) or Cloud POS in Microsoft Dynamics 365 for Retail through the <bpt id="p1">**</bpt>Picking/Receiving<ept id="p1">**</ept> operation.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">小売倉庫が発注書ヘッダーに含まれている場合、Microsoft Dynamics 365 for Retail の Modern POS (MPOS) または Cloud POS を使用し、<bpt id="p1">**</bpt>ピッキング/入庫<ept id="p1">**</ept>操作により、注文を店舗で受け取ることができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="138">
          <source>After the quantities that are received at the store are entered in the <bpt id="p1">**</bpt>Receive Now<ept id="p1">**</ept> field in POS for the purchase order document, they can be saved locally or committed.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">店舗で入荷された数量が、発注書ドキュメント内の POS の<bpt id="p1">**</bpt>今すぐ入荷<ept id="p1">**</ept>フィールドに入力された後、ローカルへの保存または確定を行うことができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="139">
          <source>Saving this data locally has no effect on in-stock inventory.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このデータをローカルに保存しても、在庫には影響しません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="140">
          <source>Saving should be done only if the user is not ready to post the receipt to HQ and just needs a way to temporarily store the previously entered <bpt id="p1">**</bpt>Receive Now<ept id="p1">**</ept> data.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">保存は、ユーザーが HQ に入荷を転記する準備ができておらず、前回入力した<bpt id="p1">**</bpt>今すぐ入荷<ept id="p1">**</ept>データを一時的に保存する方法が必要である場合にのみ行う必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="141">
          <source>This saves the receive now data locally to the user's channel database.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">これにより、今すぐ入荷データがローカルのユーザーのチャネル データベースに保存されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="142">
          <source>After the document is processed using the <bpt id="p1">**</bpt>Commit<ept id="p1">**</ept> option, the <bpt id="p2">**</bpt>Receive Now<ept id="p2">**</ept> data is sent to HQ and the purchase order receipt will be posted.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>確定<ept id="p1">**</ept>オプションを使用してドキュメントを処理した後、<bpt id="p2">**</bpt>今すぐ入荷<ept id="p2">**</ept>データが HQ に送信され、発注書受入が転記されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="143">
          <source>Transfer orders</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">移動オーダー</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="144">
          <source>A transfer order can specify that a particular store is the location that items can be shipped from or the location the inventory will be received into.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">移動オーダーは、特定の店舗が品目の出荷元となる場所または在庫の入荷場所となるように指定できます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="145">
          <source>If the POS user is the shipping warehouse for a transfer order, they will be able to enter <bpt id="p1">**</bpt>Ship Now<ept id="p1">**</ept> quantities from POS.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">POS ユーザーが移動オーダーに対する出荷倉庫である場合、POS から<bpt id="p1">**</bpt>今すぐ出荷<ept id="p1">**</ept>の数量を入力することができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="146">
          <source>The data entered by the shipping store can be saved locally or committed.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">出荷店舗で入力されたデータは、ローカルに保存するか、または確定することができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="147">
          <source>When saved locally, no updates are made to the transfer order document in HQ.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ローカルに保存された場合、HQ 内の移動オーダー ドキュメントに更新は行われません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="148">
          <source>Saving should be done only if the user is not ready to post the shipment to HQ and needs a way to temporarily store the previously entered <bpt id="p1">**</bpt>Ship Now<ept id="p1">**</ept> data.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">保存は、ユーザーが HQ に出荷を転記する準備ができておらず、前回入力した<bpt id="p1">**</bpt>今すぐ出荷<ept id="p1">**</ept>データを一時的に保存する方法が必要である場合にのみ行う必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="149">
          <source>After the store is ready to confirm shipment, the <bpt id="p1">**</bpt>Commit<ept id="p1">**</ept> option should be selected.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">店舗で出荷を確認する準備ができた後、<bpt id="p1">**</bpt>確定<ept id="p1">**</ept>オプションを選択する必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="150">
          <source>This posts the shipment of the transfer order in HQ so that the receiving warehouse will now be able to receive against it.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">これにより、HQ 内の移動オーダーの出荷が転記され、それから入荷倉庫は入庫できるようになります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="151">
          <source>If the POS user is the receiving warehouse for a transfer order, they will be able to enter the <bpt id="p1">**</bpt>Receive Now<ept id="p1">**</ept> quantities from POS.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">POS ユーザーが移動オーダーに対する入荷倉庫である場合、POS から<bpt id="p1">**</bpt>今すぐ入荷<ept id="p1">**</ept>の数量を入力することができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="152">
          <source>The data entered by the receiving store can be saved locally or committed.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">入荷店舗で入力されたデータは、ローカルに保存するか、または確定することができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="153">
          <source>Saving should be done only if the user is not ready to post the receipt to HQ and needs a way to temporarily store the previously entered <bpt id="p1">**</bpt>Receive Now<ept id="p1">**</ept> data.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">保存は、ユーザーが HQ に入荷を転記する準備ができておらず、前回入力した<bpt id="p1">**</bpt>今すぐ入荷<ept id="p1">**</ept>データを一時的に保存する方法が必要である場合にのみ行う必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="154">
          <source>This saves the receive now data locally to the user's channel database.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">これにより、今すぐ入荷データがローカルのユーザーのチャネル データベースに保存されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="155">
          <source>After the document is processed using the <bpt id="p1">**</bpt>Commit<ept id="p1">**</ept> option, the <bpt id="p2">**</bpt>Receive Now<ept id="p2">**</ept> data is sent to HQ and the transfer order receipt will be posted.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>確定<ept id="p1">**</ept>オプションを使用してドキュメントを処理した後、<bpt id="p2">**</bpt>今すぐ入荷<ept id="p2">**</ept>データが HQ に送信され、移動オーダー入荷が転記されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="156">
          <source>It's important to note that the receiving store will be restricted to only being able to commit receive quantities that are equal to or less than shipped quantities.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">入荷店舗は、出荷数量以下の入荷数量のみ確定できるように制限されていることに注意する必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="157">
          <source>An attempt to receive quantities on a transfer order that have not previously shipped will result in errors and the receipt will not be confirmed in HQ.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">まだ出荷されていない移動オーダーの数量を入荷しようとするとエラーが発生し、HQ では入荷は確認されません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="158">
          <source>Stock counts</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">在庫数</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="159">
          <source>Stock counts can be either scheduled or unscheduled.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">在庫棚卸は、計画済または計画外のいずれかです。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="160">
          <source>Scheduled stock counts are initiated at the head office, which specifies the items that must be counted.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">計画済の在庫棚卸は、棚卸を行う必要がある品目を指定する本社で開始されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="161">
          <source>The head office creates a counting document that can be received at the store, where the quantities of actual on-hand stock are entered in MPOS or Cloud POS.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">本社で店舗に送信可能な棚卸ドキュメントが作成され、実際の手持在庫数量が店舗で MPOS またはクラウド POS に入力されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="162">
          <source>Unscheduled stock counts are initiated at a store, and the quantities of actual on-hand stock are updated in either MPOS or Cloud POS.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">手動在庫棚卸は店舗で開始され、MPOS またはクラウド POS で実際の手持在庫数量が更新されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="163">
          <source>Unlike scheduled stock counts, unscheduled stock counts do not have a predefined list of items.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">計画済在庫棚卸とは異なり、計画外在庫棚卸に品目の定義済リストはありません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="164">
          <source>When a stock count of either type is completed, it is committed and sent to the head office.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">いずれかのタイプの在庫棚卸が完了すると、その在庫棚卸が確定され、本社に送信されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="165">
          <source>At the head office, the count is validated and posted as a separate step.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">本社でその在庫棚卸が検証され、別のステップとして転記されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="166">
          <source>Inventory lookup</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">在庫検索</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="167">
          <source>The current product quantity on hand for multiple stores and warehouses can be viewed on the <bpt id="p1">**</bpt>Inventory lookup<ept id="p1">**</ept> page.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">複数の店舗および倉庫の現在の手持在庫製品の数量は、<bpt id="p1">**</bpt>在庫検索<ept id="p1">**</ept>ページで表示できます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="168">
          <source>In addition to the current quantity on hand, the future available to promise (ATP) quantities can be viewed for each individual store.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">手持在庫の現在の数量に加えて、将来の納期回答可能在庫 (ATP) 数量は、各店舗ごとに表示できます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="169">
          <source>To do so, select the store that you want to view the ATP for and then click <bpt id="p1">**</bpt>Show store availability<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">これを行うには、表示したい ATP の店舗を選択して、次に <bpt id="p1">**</bpt>店舗の使用可能性を表示<ept id="p1">**</ept> をクリックします。</target></trans-unit>
      </group>
    </body>
  </file>
</xliff>