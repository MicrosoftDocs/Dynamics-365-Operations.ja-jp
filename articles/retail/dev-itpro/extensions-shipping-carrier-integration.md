<?xml version="1.0" encoding="UTF-8"?>
<xliff xmlns:logoport="urn:logoport:xliffeditor:xliff-extras:1.0" xmlns:tilt="urn:logoport:xliffeditor:tilt-non-translatables:1.0" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns="urn:oasis:names:tc:xliff:document:1.2" xmlns:xliffext="urn:microsoft:content:schema:xliffextensions" version="1.2" xsi:schemaLocation="urn:oasis:names:tc:xliff:document:1.2 xliff-core-1.2-transitional.xsd">
  <file datatype="xml" source-language="en-US" original="extensions-shipping-carrier-integration.md" target-language="ja-JP">
    <header>
      <tool tool-company="Microsoft" tool-version="1.0-7889195" tool-name="mdxliff" tool-id="mdxliff"/>
      <xliffext:skl_file_name>extensions-shipping-carrier-integration.5fea6c.7fcc2a05f77f5814dbc25823967c4f61befc37e0.skl</xliffext:skl_file_name>
      <xliffext:version>1.2</xliffext:version>
      <xliffext:ms.openlocfilehash>7fcc2a05f77f5814dbc25823967c4f61befc37e0</xliffext:ms.openlocfilehash>
      <xliffext:ms.sourcegitcommit>9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b</xliffext:ms.sourcegitcommit>
      <xliffext:ms.lasthandoff>05/15/2019</xliffext:ms.lasthandoff>
      <xliffext:ms.openlocfilepath>articles\retail\dev-itpro\extensions-shipping-carrier-integration.md</xliffext:ms.openlocfilepath>
    </header>
    <body>
      <group extype="content" id="content">
        <trans-unit xml:space="preserve" translate="yes" id="101" restype="x-metadata">
          <source>Extension points for packing slips during order fulfillment</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">注文のフルフィルメント中の梱包明細の拡張ポイント</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="102" restype="x-metadata">
          <source>This topic shows how to use customizations to add extension points to packing slips during customer order fulfillment.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このトピックでは、カスタマイズを使用して、顧客注文の処理中に梱包明細に拡張ポイントを追加する方法を示します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="103">
          <source>Extension points for packing slips during order fulfillment</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">注文のフルフィルメント中の梱包明細の拡張ポイント</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="104">
          <source>When you generate packing slips for customer orders from the point of sale (POS), you might want to print the item weight on the packing slip.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">販売時点管理 (POS) から顧客注文の梱包明細を生成するとき、梱包明細に品目の重量を印刷する場合があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="105">
          <source>You might also want to add custom information about the package, information about how to call the shipping carrier for the shipping rates, or information about how to return the package.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">パッケージについてのカスタム情報、送料に関して配送業者を呼び出す方法に関する情報、またはパッケージの返却方法についての情報を追加することもできます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="106">
          <source>To handle these scenarios, extension points for the packing slip process for order fulfillment have been added in Retail headquarters, in the commerce runtime (CRT), which is the business logic layer, and in the POS.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">これらのシナリオを処理するために、受注処理のための梱包明細プロセスの延長ポイントが小売用バックオフィス、ビジネス ロジック層であるコマース ランタイム (CRT)、および POS で追加されました。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="107">
          <source>These extension points let you add custom flow and logic through extensions.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">これらの拡張ポイントを使用すると、拡張を介してカスタム フローとロジックを追加できます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="108">
          <source>POS</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">POS</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="109">
          <source>In the POS, a new request handler that is named <bpt id="p1">**</bpt>PrintPackingSlipClientRequestHandler<ept id="p1">**</ept> lets you override extensions.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">POS では、<bpt id="p1">**</bpt>PrintPackingSlipClientRequestHandler<ept id="p1">**</ept> という名前の新しい要求ハンドラーで拡張機能をオーバーライドできます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="110">
          <source>This request is called when you select the <bpt id="p1">**</bpt>Print packing slip<ept id="p1">**</ept> button in the POS.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この要求は、POS で<bpt id="p1">**</bpt>梱包明細を印刷する<ept id="p1">**</ept>ボタンを選択すると呼び出されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="111">
          <source>By overriding this request, you can use custom logic in the POS.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この要求を上書きすることによって、POS でカスタム ロジックを使用することができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="112">
          <source>For example, you can call your own printing methods and print additional information.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">たとえば、独自の印刷メソッドを呼び出し、追加情報を印刷できます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="113">
          <source>For example, by default, you can print the packing slip in PDF format.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">たとえば、既定では、PDF 形式で梱包明細を印刷することができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="114">
          <source>By overriding the POS client request, you can print the packing slip in a different format.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">POS クライアント要求を上書きすることによって、さまざまな形式で梱包明細を印刷できます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="115">
          <source>Alternatively, you can check for a specific condition, and then print or stop printing the packing slip, based on that condition.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">または、特定の条件を確認し、基本的な条件に基づいて梱包明細の印刷、または印刷停止をすることができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="116">
          <source>You can also do validation before you print, and prevent printing or custom logic.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">また、印刷前に検証を実行して、印刷ロジックまたはカスタム ロジックを止めることができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="117">
          <source>However, if you want to change the actual data that is printed, you must modify the business logic in CRT and Retail headquarters.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ただし、印刷される実際のデータを変更する場合、CRT および小売用バックオフィスでビジネス ロジックを変更する必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="118">
          <source>Override PrintPackingSlipClientRequestHandler</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">PrintPackingSlipClientRequestHandler のオーバーライド</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="119">
          <source>To override any request in the POS, use the following override handler pattern in the POS.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">POS の要求をオーバーライドするには、POS で次のオーバーライド ハンドラー パターンを使用します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="120">
          <source><bpt id="p1">**</bpt>Example<ept id="p1">**</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>例<ept id="p1">**</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="121">
          <source>After you override the request, update the manifest.json file with the new request handler information.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">要求を上書きした後は、新しい要求ハンドラー情報を含む manifest.json ファイルを更新します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="122">
          <source>CRT</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">CRT</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="123">
          <source>Similar to the POS client request handler, new requests have been added in the CRT to enable extension of custom logic.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">POS クライアントの要求ハンドラーと同様、カスタム ロジックの拡張機能を有効にするため CRT に新しい要求が追加されました。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="124">
          <source>MarkAsPickedRealtimeRequest</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">MarkAsPickedRealtimeRequest</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="125">
          <source>The <bpt id="p1">**</bpt>MarkAsPickedRealtimeRequest<ept id="p1">**</ept> request marks the fulfillment lines as picked.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>MarkAsPickedRealtimeRequest<ept id="p1">**</ept> 要求は、調達のための明細行をピッキング済みとしてマークします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="126">
          <source>You can add custom logic before the line is marked as picked.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">明細行がピッキング済みとマークされる前に、カスタム ロジックを追加することができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="127">
          <source>For example, you can change a property.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">たとえば、プロパティを変更できます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="128">
          <source>Later, the picked line information will be used to print the packing slip.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">後で、ピッキング済の明細行の情報が梱包明細の印刷に使用されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="129">
          <source>Based on your scenario, you can override this request, or add pre-triggers or post-triggers.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">シナリオに基づいて、この要求を無効にするか、プレトリガーまたはポストトリガーを追加することができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="130">
          <source>For example, for the fulfillment lines, you want to calculate item weight, and so on.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">たとえば、 フルフィルメント明細行については、品目の重量などを計算します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="131">
          <source>In this case, you can customize the service.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この場合、サービスをカスタマイズできます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="132">
          <source>If the logic that you require for your customization must be determined in Retail headquarters, you can customize at the Retail headquarters level instead of customizing in the CRT.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">小売用バック オフィスでカスタマイズを必要とするロジックを決定する必要がある場合、CRT でカスタマイズするのではなく、小売用バック オフィス レベルでカスタマイズできます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="133">
          <source>For example, you want to get the item weight for each line, but that information is available only in Retail headquarters.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">たとえば、各明細行の品目重量を取得しても、その情報は小売用バックオフィスでのみ使用できます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="134">
          <source>In this case, you can customize the relevant real-time service methods and then return the result from Retail headquarters to the CRT.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この場合、関連するリアルタイム サービスのメソッドをカスタマイズしてから、小売用バック オフィスから CRT に結果を返すことができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="135">
          <source>PackFulfillmentLinesRealtimeRequest</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">PackFulfillmentLinesRealtimeRequest</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="136">
          <source>The <bpt id="p1">**</bpt>PackFulfillmentLinesRealtimeRequest<ept id="p1">**</ept> request updates the status of the fulfillment lines to <bpt id="p2">**</bpt>Partially packed<ept id="p2">**</ept> or <bpt id="p3">**</bpt>Packed.<ept id="p3">**</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>PackFulfillmentLinesRealtimeRequest<ept id="p1">**</ept> 要求は、フルフィルメント明細行のステータスを <bpt id="p2">**</bpt>部分的に梱包済み<ept id="p2">**</ept> または <bpt id="p3">**</bpt>梱包済み<ept id="p3">**</ept> に更新します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="137">
          <source>Based on your scenario, you can override this service, or add pre-triggers or post-triggers.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">シナリオに基づいて、このサービスを無効にするか、プレトリガーまたはポストトリガーを追加することができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="138">
          <source>Retail headquarters</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">小売用バックオフィス</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="139">
          <source>In Retail headquarters new real-time service methods have been added to get the packing slip information, and to add custom information or logic through extension.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">小売用バックオフィスでは、梱包明細情報を取得して、拡張機能によってカスタム情報やロジックを追加するために、新しいリアルタイム サービス メソッドが追加されました。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="140">
          <source>If your customization requires that data or logic be done in Retail headquarters, you can customize these methods by using the extension patterns.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">カスタマイズで、データまたはロジックが小売用バックオフィスで実行されることを必須としている場合、拡張機能のパターンを使用して、これらのメソッドをカスタマイズできます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="141">
          <source>Additionally, if you require an extension scenario that uses the transaction service client class, you can call these methods from the CRT.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">また、取引サービス クライアント クラスを使用する拡張子シナリオが必要な場合は、CRT からこれらのメソッドを呼び出すことができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="142">
          <source>RetailTransactionServiceFulfillment</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">RetailTransactionServiceFulfillment</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="143">
          <source>All the new methods that are related to the packing slip process for order fulfillment were added in the <bpt id="p1">**</bpt>RetailTransactionServiceFulfillment<ept id="p1">**</ept> class.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">梱包明細プロセスに関連付けられているすべての新しいメソッドは注文のフルフィルメントにより、<bpt id="p1">**</bpt>RetailTransactionServiceFulfillment<ept id="p1">**</ept> クラスに追加されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="144">
          <source>GetPackingSlipsData</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">GetPackingSlipsData</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="145">
          <source>The <bpt id="p1">**</bpt>GetPackingSlipsData<ept id="p1">**</ept> method returns all the packing slip information by passing the sales ID as a parameter.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>GetPackingSlipsData<ept id="p1">**</ept> メソッドは、パラメーターとして販売 ID を渡すことによってすべての梱包明細情報を返します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="146">
          <source>GetFulfillmentLinesByPackingSlipId</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">GetFulfillmentLinesByPackingSlipId</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="147">
          <source>The <bpt id="p1">**</bpt>GetFulfillmentLinesByPackingSlipId<ept id="p1">**</ept> method returns the fulfillment lines, based on the packing slip ID.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>GetFulfillmentLinesByPackingSlipId<ept id="p1">**</ept> メソッドは、梱包明細 ID に基づいて調達のための明細行を返します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="148">
          <source>For example, you can use this method if you have the packing slip ID, and you want to get the sales lines that are relevant to that packing slip ID.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">たとえば、梱包明細 ID があり、その梱包明細 ID に関連する販売明細行を取得する場合、このメソッドを使用します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="149">
          <source>MarkFulfillmentLinesAsPacked</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">MarkFulfillmentLinesAsPacked</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="150">
          <source>The <bpt id="p1">**</bpt>MarkFulfillmentLinesAsPacked<ept id="p1">**</ept> method updates the status of the fulfillment lines to packed by taking the fulfillment details as a parameter in XML string format.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>MarkFulfillmentLinesAsPacked<ept id="p1">**</ept> メソッドは、調達のための詳細を XML 文字列形式でパラメーターとして取得することにより梱包される調達のための明細行のステータスを更新します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="151">
          <source>The POS calls the CRT to mark the selected lines from the POS user interface (UI) as picked.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">POS は、POS ユーザー インターフェイス (UI) の選択した明細行をピッキング済としてマークするために CRT を呼び出します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="152">
          <source>The <bpt id="p1">**</bpt>MarkAsPickedRealtimeRequest<ept id="p1">**</ept> request in the CRT then calls the <bpt id="p2">**</bpt>MarkFulfillmentLinesAsPacked<ept id="p2">**</ept> real-time service method in Retail headquarters to set the line status as <bpt id="p3">**</bpt>Packed<ept id="p3">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">CRT の <bpt id="p1">**</bpt>MarkAsPickedRealtimeRequest<ept id="p1">**</ept> 要求が小売用バックオフィスで <bpt id="p2">**</bpt>MarkFulfillmentLinesAsPacked<ept id="p2">**</ept> リアルタイム サービス メソッドを呼び出し、行のステータスを <bpt id="p3">**</bpt>梱包済み<ept id="p3">**</ept> として設定します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="153">
          <source>To add custom logic or return additional information when the line is marked as packed and returned for printing, you can customize the <bpt id="p1">**</bpt>packingSlipExtensionPoint<ept id="p1">**</ept> method.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">行が梱包済みとマークされていて印刷のために返された場合にカスタム ロジックを追加したり追加情報を返すには、<bpt id="p1">**</bpt>packingSlipExtensionPoint<ept id="p1">**</ept> メソッドをカスタマイズできます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="154">
          <source>packingSlipExtensionPoint</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">packingSlipExtensionPoint</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="155">
          <source>You can customize the <bpt id="p1">**</bpt>packingSlipExtensionPoint<ept id="p1">**</ept> method to add custom logic or return custom information together with the packing slip ID.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>packingSlipExtensionPoint<ept id="p1">**</ept> メソッドをカスタマイズして、カスタム ロジックを追加、または梱包明細 ID とともにカスタム情報を戻すことができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="156">
          <source>This custom information includes packing information or a delivery note.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このカスタム情報には、梱包情報または納品書が含まれています。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="157">
          <source>This method is typically added for extensions for custom scenarios.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このメソッドは、通常、カスタム シナリオの拡張機能に追加されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="158">
          <source>This method is called from the <bpt id="p1">**</bpt>MarkFulfillmentLinesAsPacked<ept id="p1">**</ept> method by using the chain of command extensibility point.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このメソッドは、コマンド拡張ポイントのチェーンを使用して <bpt id="p1">**</bpt>MarkFulfillmentLinesAsPacked<ept id="p1">**</ept> メソッドから呼び出されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="159">
          <source>The <bpt id="p1">**</bpt>MarkFulfillmentLinesAsPacked<ept id="p1">**</ept> method is run from the real-time service call that the CRT code makes.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>MarkFulfillmentLinesAsPacked<ept id="p1">**</ept> メソッドは、CRT コードが行うリアルタイム サービス呼び出しから実行されます。</target></trans-unit>
      </group>
    </body>
  </file>
</xliff>