<?xml version="1.0" encoding="UTF-8"?>
<xliff xmlns:logoport="urn:logoport:xliffeditor:xliff-extras:1.0" xmlns:tilt="urn:logoport:xliffeditor:tilt-non-translatables:1.0" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns="urn:oasis:names:tc:xliff:document:1.2" xmlns:xliffext="urn:microsoft:content:schema:xliffextensions" version="1.2" xsi:schemaLocation="urn:oasis:names:tc:xliff:document:1.2 xliff-core-1.2-transitional.xsd">
  <file datatype="xml" source-language="en-US" original="commerce-runtime-extensibility.md" target-language="ja-JP">
    <header>
      <tool tool-company="Microsoft" tool-version="1.0-7889195" tool-name="mdxliff" tool-id="mdxliff"/>
      <xliffext:skl_file_name>commerce-runtime-extensibility.b6cecf.138612221bb6e17ae354a194cd3df7d70b3ce543.skl</xliffext:skl_file_name>
      <xliffext:version>1.2</xliffext:version>
      <xliffext:ms.openlocfilehash>138612221bb6e17ae354a194cd3df7d70b3ce543</xliffext:ms.openlocfilehash>
      <xliffext:ms.sourcegitcommit>9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b</xliffext:ms.sourcegitcommit>
      <xliffext:ms.lasthandoff>05/15/2019</xliffext:ms.lasthandoff>
      <xliffext:ms.openlocfilepath>articles\retail\dev-itpro\commerce-runtime-extensibility.md</xliffext:ms.openlocfilepath>
    </header>
    <body>
      <group extype="content" id="content">
        <trans-unit xml:space="preserve" translate="yes" id="101" restype="x-metadata">
          <source>Commerce runtime (CRT) and Retail Server extensibility</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Commerce Runtime (CRT) および Retail サーバーの拡張機能</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="102" restype="x-metadata">
          <source>This topic describes various ways that you can extend the commerce runtime (CRT) and Retail Server.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このトピックでは、Commerce Runtime (CRT) と Retail サーバーを拡張するさまざまな方法について説明します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="103" restype="x-metadata">
          <source>It explains the concept of extension properties, and shows how to add them to a CRT entity both with and without persistence.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">拡張機能プロパティのコンセプトを説明し、保持有無にかかわらず CRT エンティティに追加する方法について説明します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="104" restype="x-metadata">
          <source>It also shows how to add an action to a Retail Server controller and add a controller for an entity.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">また、アクションを Retail サーバー コントローラーに追加して、エンティティのコントローラーを追加する方法も示します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="105">
          <source>Commerce runtime (CRT) and Retail Server extensibility</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Commerce Runtime (CRT) および Retail サーバーの拡張機能</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="106">
          <source>This topic describes various ways that you can extend the commerce runtime (CRT) and Retail Server.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このトピックでは、Commerce Runtime (CRT) と Retail サーバーを拡張するさまざまな方法について説明します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="107">
          <source>It explains the concept of extension properties, and shows how to add them to a CRT entity both with and without persistence.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">拡張機能プロパティのコンセプトを説明し、保持有無にかかわらず CRT エンティティに追加する方法について説明します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="108">
          <source>It also shows how to add an action to a Retail Server controller and add a controller for an entity.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">また、アクションを Retail サーバー コントローラーに追加して、エンティティのコントローラーを追加する方法も示します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="109">
          <source>CRT contains the core business logic.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">CRT にはコア ビジネス ロジックが含まれています。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="110">
          <source>If you want to add or modify any business logic, you should customize CRT.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ビジネス ロジックを追加または変更するには、CRT をカスタマイズする必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="111">
          <source>All the CRT code is developed by using C#, and it's then compiled and released as class libraries (.NET assemblies).</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">C# を使用して、すべての CRT コードが開発およびコンパイルされ、クラス ライブラリとしてリリースされます (.NET アセンブリ)。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="112">
          <source>Retail point of sale (POS) is a thin client.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">小売販売時点管理 (POS) はシン クライアントです。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="113">
          <source>All the business logic is done in CRT.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">すべてのビジネス ロジックは、CRT で行われます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="114">
          <source>POS calls CRT to perform any business logic, and CRT processes the information and then sends it back to POS.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">POS は、任意のビジネス ロジックを実行する CRT を呼び出し、CRT は情報を処理して POS に送り返されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="115">
          <source>Every CRT service consists of a group of one or more requests and responses.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">すべての CRT サービスは、1 つ以上の要求と応答のグループで構成されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="116">
          <source>Any time that you do something in POS, POS sends a request to Retail Server, and Retail Server calls CRT.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">POS で作業する際はいつでも、POSは Retail サーバーに要求を送り、Retail サーバーは CRT を呼び出します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="117">
          <source>CRT then processes the request and sends back the response.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">続いて CRT は要求を処理し、応答を送り返します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="118">
          <source>For example, the Customer service in CRT contains all the customer-related requests and responses, each of which is run in a different flow.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">たとえば、CRT の顧客サービスには、顧客関連のすべての要求と応答が含まれており、それぞれは異なるフローで実行されています。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="119">
          <source>Likewise, the Product service in CRT contain all the product-related requests and responses.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">同様に、CRT の製品サービスには製品に関連するすべての要求と応答が含まれます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="120">
          <source>The following table shows the requests in the Customer service.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">次の表に、顧客サービスの要求を示します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="121">
          <source>Request</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">要求</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="122">
          <source>Purpose</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">目的</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="123">
          <source>SaveCustomerServiceRequest</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">SaveCustomerServiceRequest</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="124">
          <source>This request is called when you save a customer from POS.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この要求は、POS から顧客を保存する場合に呼び出されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="125">
          <source>GetCustomersServiceRequest</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">GetCustomersServiceRequest</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="126">
          <source>This request is used to get the details of the selected customer.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この要求は、選択した顧客の詳細を取得するために使用されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="127">
          <source>CustomersSearchServiceRequest</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">CustomersSearchServiceRequest</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="128">
          <source>This request is run when you do a customer search from POS.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この要求は、POS から顧客検索を行う場合に実行されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="129">
          <source>GetCustomerGroupsServiceRequest</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">GetCustomerGroupsServiceRequest</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="130">
          <source>This request is used to get the details of the customer group.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この要求は、顧客グループの詳細を取得するために使用されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="131">
          <source>InitiateLinkToExistingCustomerServiceRequest</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">InitiateLinkToExistingCustomerServiceRequest</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="132">
          <source>This internal request is for backward compatibility.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この内部要求は、下位互換性のためのものです。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="133">
          <source>FinalizeLinkToExistingCustomerServiceRequest</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">FinalizeLinkToExistingCustomerServiceRequest</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="134">
          <source>This internal request is for backward compatibility.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この内部要求は、下位互換性のためのものです。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="135">
          <source>UnlinkFromExistingCustomerServiceRequest</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">UnlinkFromExistingCustomerServiceRequest</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="136">
          <source>This internal request is for backward compatibility.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この内部要求は、下位互換性のためのものです。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="137">
          <source>GetCustomerBalanceServiceRequest</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">GetCustomerBalanceServiceRequest</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="138">
          <source>This request gets the balance for the customer account.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この要求は、顧客勘定の残高を取得します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="139">
          <source>GetOrderHistoryServiceRequest</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">GetOrderHistoryServiceRequest</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="140">
          <source>This request gets the customer's order history.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この要求は、顧客の注文履歴を取得します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="141">
          <source>GetPurchaseHistoryServiceRequest</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">GetPurchaseHistoryServiceRequest</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="142">
          <source>This request gets the history of the customer's recent purchases.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この要求は、顧客の最近の購入履歴を取得します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="143">
          <source>CustomerSearchByFieldsServiceRequest</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">CustomerSearchByFieldsServiceRequest</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="144">
          <source>This request is run when you search for customers by using fields (hint search).</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">フィールド (ヒント検索) を使用して顧客を検索する際に、この要求が実行されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="145">
          <source>GetCustomerSearchFieldsServiceRequest</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">GetCustomerSearchFieldsServiceRequest</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="146">
          <source>This request gets the list of customer search fields (hint fields).</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この要求は、顧客検索フィールド (ヒント フィールド) の一覧を取得します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="147">
          <source><bpt id="p1">**</bpt>Types of extension patterns that CRT supports<ept id="p1">**</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>CRT がサポートする拡張子パターンのタイプ<ept id="p1">**</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="148">
          <source>Before you learn about the CRT extension patterns, you should understand how a CRT extension can be created.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">CRT 拡張パターンについて学習する前に、CRT 拡張の作成方法を理解する必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="149">
          <source>CRT is just a collection of C# class libraries (.NET assemblies).</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">CRT は単に、C# クラス ライブラリ (.NETアセンブリ) のコレクションです。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="150">
          <source>You can create a class library project in C# and do all the CRT extension by using the patterns that are shown in the following table.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">C# でクラス ライブラリ プロジェクトを作成し、次の表に示すパターンを使用してすべての CRT 拡張を実行できます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="151">
          <source>Always use the samples that Microsoft provides as template for your extension, because these samples have the correct assembly references, Microsoft .NET Framework version, output type, and build parameters.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">これらのサンプルには、適切なアセンブリ参照、Microsoft .NET Framework バージョン、アウトプット タイプ、およびビルド パラメーターが含まれているので、Microsoft が拡張のためのテンプレートとして提供するサンプルを常に使用します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="152">
          <source>Additionally, all the other required parameters are preconfigured.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">また、他のすべての必須パラメーターがコンフィギュレーション済みです。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="153">
          <source>You can find the CRT sample extension in the Retail software development kit (SDK), at …<ph id="ph1">\\</ph>RetailSDK<ph id="ph2">\\</ph>SampleExtensions<ph id="ph3">\\</ph>CommerceRuntime.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">同様のサンプルコードは、R<ph id="ph1">\\</ph>RetailSDK<ph id="ph2">\\</ph>SampleExtensions<ph id="ph3">\\</ph>CommerceRuntime の Retail ソフトウェア開発キット (CRT) で見つけることができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="154">
          <source>Extensibility pattern</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">拡張機能のパターン</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="155">
          <source>Purpose</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">目的</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="156">
          <source>Create a new CRT service</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">新しい CRT サービスの作成</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="157">
          <source>Create a new functionality/feature.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">新機能を作成します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="158">
          <source>Override existing Service</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">既存のサービスを上書きする</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="159">
          <source>You can completely override existing functionality or customize it according to your business flow.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">完全に既存の機能をオーバーライドしたり、ビジネス フローに従ってカスタマイズできます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="160">
          <source>Here are some examples:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">次にいくつか例を挙げます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="161">
          <source>You want to override the POS search functionality to search from an external system instead of searching in a local database or HQ.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">POS 検索機能を上書きして、ローカル データベースまたは本社で検索するのではなく、外部システムから検索する必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="162">
          <source>Alternatively, you can do an override, call the standard functionality, and do some additional custom logic.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">または、上書き、標準機能の呼び出しおよびいくつか追加カスタム ロジックの実行が可能です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="163">
          <source>Search for a customer in a local database or HQ, and in an external system, and then finally merge or modify the result.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ローカル データベースまたは HQ、および外部システムを検索した後、最後に結果をマージまたは変更します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="164">
          <source>Triggers</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">トリガー</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="165">
          <source>You can execute additional logic before or after any request.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">任意の要求の前後に追加ロジックを実行できます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="166">
          <source>In the pre-trigger, you can do some validation, custom logic, and so on.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">前のトリガーで、カスタム ロジックなどのいくつかの検証を実行できます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="167">
          <source>In the post-trigger, you can add some custom information to the request and send it to POS.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ポスト トリガーで、要求にいくらかのカスタム情報を追加し POS に送信できます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="168">
          <source>Alternatively, you can modify the result that is returned from the standard functionality or do some additional business logic.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">または、標準機能から戻される結果の変更または追加ビジネス ロジックの実行が可能です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="169">
          <source>Extension properties</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">拡張プロパティ</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="170">
          <source>You can add custom properties to any CRT entity and send it to POS.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">任意の CRT エンティティにカスタム プロパティーを追加し、それを POS に送信することができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="171">
          <source>Extension properties are key-value pairs.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">拡張プロパティはキーと値のペアです。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="172">
          <source>If you set an extension property in POS, it will be available in CRT.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">POS で拡張プロパティを設定すると、CRT で使用できるようになります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="173">
          <source>Likewise, if you set an extension property in CRT, it will be available in POS.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">同様に、CRT で拡張機能プロパティを設定する場合、POS で使用できます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="174">
          <source>You can also set extension properties at the level of the request, the response, or the request context.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">また、要求、応答、または要求コンテキストのレベルで拡張プロパティを設定することもできます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="175">
          <source>By default, extension properties aren't stored in and read from the database.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">既定では、拡張機能のプロパティはデータベースに保存されず、読み取られません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="176">
          <source>To read or set extension properties, you must write custom code.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">拡張プロパティを読み取り、設定するには、カスタム コードを記述する必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="177">
          <source>However, that custom code is automatically sent between POS and CRT.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ただし、そのカスタム コードは、POS と CRT 間で自動的に送信されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="178">
          <source>For example, you want to capture and show some additional information to the customer entity in POS.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">たとえば、POS の顧客エンティティーにいくつかの追加情報をキャプチャして表示したいとします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="179">
          <source>In this case, you can add a post-trigger to fetch all your custom properties for customer, add them to the customer entity as extension properties, and send those extension properties to POS.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この場合、顧客に対するすべてのカスタム プロパティをフェッチするポスト トリガーを追加し、拡張子プロパティとして顧客エンティティに追加し、それらの拡張機能プロパティを POS に送信できます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="180">
          <source>You can also send extension properties from POS to CRT and store them in your custom table.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">POS から CRT に拡張機能のプロパティを送信して、カスタム テーブルに保存できます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="181">
          <source>Alternatively, you can do some custom logic based on those properties, or send it to HQ.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">または、これらのプロパティに基づくいくつかのカスタム ロジックの実行または本社への送信が可能です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="182">
          <source>All CRT entities, such as products, customers, transactions, and parameters, support extension properties.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">製品、顧客、トランザクション、およびパラメーターなどのすべての CRT エンティティは、拡張機能プロパティをサポートします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="183">
          <source>Attributes are also supported (configuration-driven development).</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">属性もまたサポートされます (コンフィギュレーション駆動型の開発)。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="184">
          <source>For extension properties, you must create a custom table and store the data.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">拡張プロパティの場合は、カスタム テーブルを作成し、データを格納する必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="185">
          <source>However, attributes are configuration-driven and aren't required in order to create table fields.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ただし、属性はコンフィギュレーション駆動型であり、テーブル フィールドを作成するために必須ではありません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="186">
          <source>Therefore, no code is required for read and update operations.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">したがって、読み取りおよび更新操作にコードは必要ありません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="187">
          <source>For details about the attributes, see the following topics:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">属性についての詳細は、次のトピックを参照してください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="188">
          <source><bpt id="p1">&lt;a href="https://docs.microsoft.com/en-us/dynamics365/unified-operations/retail/dev-itpro/order-attributes"&gt;</bpt>Order attributes<ept id="p1">&lt;/a&gt;</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">&lt;a href="https://docs.microsoft.com/en-us/dynamics365/unified-operations/retail/dev-itpro/order-attributes"&gt;</bpt>注文属性<ept id="p1">&lt;/a&gt;</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="189">
          <source><bpt id="p1">&lt;a href="https://docs.microsoft.com/en-us/dynamics365/unified-operations/retail/dev-itpro/customer-attributes"&gt;</bpt>Customer attributes<ept id="p1">&lt;/a&gt;</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">&lt;a href="https://docs.microsoft.com/en-us/dynamics365/unified-operations/retail/dev-itpro/customer-attributes"&gt;</bpt>顧客属性<ept id="p1">&lt;/a&gt;</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="190">
          <source>Real-time transaction service calls</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">リアルタイム トランザクション サービスの呼び出し</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="191">
          <source>You can do synchronous call from CRT to HQ.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">CRT から HQ の同期呼び出しを行うことができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="192">
          <source>CRT data service and data service with entity</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">CRT データ サービス、およびエンティティ付きデータ サービス</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="193">
          <source>Specialized data service for channel database data access and entity for Retail Server exposures.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">チャネル データベース データ アクセスの特殊なデータ サービスおよび Retail サーバー エクスポージャのエンティティ。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="194">
          <source><bpt id="p1">**</bpt>Manually deploying the CRT extension for 7.1 with May update and later<ept id="p1">**</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>5 月の更新プログラム以降で、7.1 の CRT 拡張を手動で展開<ept id="p1">**</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="195">
          <source>After you extend CRT, you should put the custom library in the <bpt id="p1">**</bpt>…<ph id="ph1">\\</ph>RetailServer<ph id="ph2">\\</ph>webroot<ph id="ph3">\\</ph>bin<ph id="ph4">\\</ph>Ext<ept id="p1">**</ept> folder for online (that is, when POS is connected to Retail Server).</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">CRT を拡張すると、オンラインの <bpt id="p1">**</bpt>…<ph id="ph1">\\</ph>RetailServer<ph id="ph2">\\</ph>webroot<ph id="ph3">\\</ph>bin<ph id="ph4">\\</ph>Ext<ept id="p1">**</ept> フォルダーにカスタム ライブラリを配置します (POS が Retail サーバーに接続された場合)。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="196">
          <source>You should also update the <bpt id="p1">**</bpt>composition<ept id="p1">**</ept> section in the <bpt id="p2">**</bpt>CommerceRuntime.Ext.config<ept id="p2">**</ept> file with the custom library information, as shown here.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p2">**</bpt>CommerceRuntime.Ext.config<ept id="p2">**</ept> ファイル内で、ここに示すカスタム ライブラリ情報を使用して<bpt id="p1">**</bpt>構成<ept id="p1">**</ept>セクションを更新する必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="197">
          <source>For example, if the name of your custom library is <bpt id="p1">**</bpt>Contoso.Commerce.Runtime.CustomerSearchSample<ept id="p1">**</ept>, add the following line in the <bpt id="p2">**</bpt>composition<ept id="p2">**</ept> section.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">たとえば、カスタム ライブラリの名前が <bpt id="p1">**</bpt>Contoso.Commerce.Runtime.CustomerSearchSample<ept id="p1">**</ept> の場合、<bpt id="p2">**</bpt>構成<ept id="p2">**</ept>セクションに次の行を追加します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="198">
          <source>For offline, you should you put the custom library in the <bpt id="p1">**</bpt>…<ph id="ph1">\\</ph>Program Files (x86)<ph id="ph2">\\</ph>Microsoft Dynamics 365<ph id="ph3">\\</ph>70<ph id="ph4">\\</ph>Retail Modern POS<ph id="ph5">\\</ph>ClientBroker<ph id="ph6">\\</ph>ext<ept id="p1">**</ept> folder.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">オフラインの場合は、カスタム ライブラリを <bpt id="p1">**</bpt>…<ph id="ph1">\\</ph>Program Files (x86)<ph id="ph2">\\</ph>Microsoft Dynamics 365<ph id="ph3">\\</ph>70<ph id="ph4">\\</ph>Retail Modern POS<ph id="ph5">\\</ph>ClientBroker<ph id="ph6">\\</ph>ext<ept id="p1">**</ept> フォルダーに配置する必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="199">
          <source>You should also update the <bpt id="p1">**</bpt>composition<ept id="p1">**</ept> section in the <bpt id="p2">**</bpt>CommerceRuntime.MPOSOffline.ext.config<ept id="p2">**</ept> file with the custom library information, as shown here.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p2">**</bpt>CommerceRuntime.MPOSOffline.ext.config<ept id="p2">**</ept> ファイル内で、ここに示すカスタム ライブラリ情報を使用して<bpt id="p1">**</bpt>構成<ept id="p1">**</ept>セクションを更新する必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="200">
          <source>The preceding steps are used for manual deployment and testing in your development box.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">上記の手順は、手動による展開および開発ボックスでのテストのために使用されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="201">
          <source>To package the extension and deploy it to production or user acceptance testing (UAT), use the information in the packaging document.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">拡張機能をパッケージ化し、生産またはユーザー受け入れテスト (UAT) に配置するには、パッケージ ドキュメントの情報を使用します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="202">
          <source><bpt id="p1">**</bpt>Debugging CRT<ept id="p1">**</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>デバッグ CRT<ept id="p1">**</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="203">
          <source>To debug CRT from POS, you should attach the CRT extension project to the <bpt id="p1">**</bpt>w3wp.exe (IIS process for Retail server)<ept id="p1">**</ept> process for online (that is, when POS is connected to CRT).</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">POS から CRT をデバッグするには、CRT 拡張機能プロジェクトを、オンラインの <bpt id="p1">**</bpt>w3wp.exe (Retail サーバーの IIS プロセス)<ept id="p1">**</ept> プロセス (POS が CRT に接続されている場合) に関連付ける必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="204">
          <source>For offline, attach the CRT extension project to the <bpt id="p1">**</bpt>dllhost.exe<ept id="p1">**</ept> process.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">オフラインの場合は、<bpt id="p1">**</bpt>dllhost.exe<ept id="p1">**</ept> プロセスに CRT 拡張プロジェクトを関連付けます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="205">
          <source><bpt id="p1">**</bpt>Using extension properties on CRT entities and requests and responses<ept id="p1">**</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>CRT エンティティ、依頼および応答での拡張機能プロパティの使用<ept id="p1">**</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="206">
          <source>One way to add new data to an existing CRT entity is to use extension properties.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">既存の CRT エンティティに新しいデータを追加する 1 つの方法は、拡張プロパティを使用することです。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="207">
          <source>Extension properties are key-value pairs on the entity.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">拡張プロパティは、エンティティのキーと値のペアです。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="208">
          <source>By default, these key-value pairs aren't persisted in the database.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">既定では、これらのキーと値のペアはデータベースで保持されません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="209">
          <source>To persist an extension property, you must write custom code.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">拡張プロパティを保持するためには、カスタム コードを記述する必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="210">
          <source><bpt id="p1">**</bpt>Using extension properties on CRT entities with persistence<ept id="p1">**</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>CRT エンティティでの機能拡張プロパティの永続的な使用<ept id="p1">**</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="211">
          <source>Any extension property that you add to an entity stays in memory for POS and CRT for the lifetime of either the object or the transaction, depending on the scenario.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">エンティティに追加する任意の拡張プロパティは、シナリオしだいでオブジェクトまたはトランザクションのいずれかの有効期間の POS および CRT メモリに保持されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="212">
          <source>The extension property also travels across application boundaries.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">拡張プロパティは、アプリケーションの境界にもまたがって移動します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="213">
          <source>For example, if you add an extension property in Retail Modern POS and then call Retail Server/CRT, the key-value pair is also available during the whole flow.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">たとえば、Retail Modern POS に拡張プロパティを追加し、Retail サーバー/CRT を呼び出すと、キーと値のペアがそのフロー全体でも使用できます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="214">
          <source>Additionally, if that entity is sent to during a call to Commerce Data Exchange: Real-time Service, the key-value pair is available during the process.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">また、そのエンティティが Commerce Data Exchange: Real-time Service を呼び出し中に送信されると、キーと値のペアは処理中に使用できます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="215">
          <source>For HQ, extension properties are sent only for customers and orders.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">HQ では、拡張プロパティは顧客と注文に対してのみ送信されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="216">
          <source>However, as was mentioned earlier, the extension property isn't persisted by default.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ただし、既述のように、拡張プロパティは既定では保持されていません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="217">
          <source>If you want to persist an extension property, you must do data modeling to help guarantee that you make the correct design choices about where the data should reside.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">拡張プロパティを保持する場合は、データ モデリングを実行して、データの格納場所を適切に設計することを保証する必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="218">
          <source>We recommend that you use a new table and a join.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">新しいテーブルと結合を使用することをお勧めします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="219">
          <source>This approach fits most requirements well.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この方法は、ほとんどの要件に適合します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="220">
          <source>The EmailPreference sample in the Retail SDK provides a good end-to-end example.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Retail SDK の EmailPreference サンプルは、代表的なエンド ツー エンドの例を提供します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="221">
          <source><bpt id="p1">**</bpt>Location of the sample code in the Retail SDK<ept id="p1">**</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>Retail SDK のサンプル コードの場所<ept id="p1">**</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="222">
          <source>…<ph id="ph1">\\</ph>RetailSDK<ph id="ph2">\\</ph>SampleExtensions<ph id="ph3">\\</ph>CommerceRuntime<ph id="ph4">\\</ph>Extensions.EmailPreferenceSample</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">…<ph id="ph1">\\</ph>RetailSDK<ph id="ph2">\\</ph>SampleExtensions<ph id="ph3">\\</ph>CommerceRuntime<ph id="ph4">\\</ph>Extensions.EmailPreferenceSample</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="223">
          <source><bpt id="p1">**</bpt>Location of the scripts<ept id="p1">**</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>スクリプトの場所<ept id="p1">**</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="224">
          <source>…<ph id="ph1">\\</ph>RetailSDK<ph id="ph2">\\</ph>Documents<ph id="ph3">\\</ph>SampleExtensionsInstructions<ph id="ph4">\\</ph>EmailPreference</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">…<ph id="ph1">\\</ph>RetailSDK<ph id="ph2">\\</ph>ドキュメント<ph id="ph3">\\</ph>SampleExtensionsInstructions<ph id="ph4">\\</ph>EmailPreference</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="225">
          <source><bpt id="p1">**</bpt>Syntax to set an extension property on an entity<ept id="p1">**</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>エンティティに拡張子プロパティを設定する構文<ept id="p1">**</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="226">
          <source><bpt id="p1">**</bpt>Example<ept id="p1">**</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>例<ept id="p1">**</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="227">
          <source><bpt id="p1">**</bpt>Scenario<ept id="p1">**</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>シナリオ<ept id="p1">**</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="228">
          <source>You created a new extension table for Retail parameters.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">小売パラメーターに新しい拡張テーブルを作成しました。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="229">
          <source>You want to read a field from that extension table and send it to POS.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">その拡張テーブルからフィールドを読み取り、それを POS に送信したいとします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="230">
          <source>When you extend the retail channel database, it's always a good idea to have a primary key relation between the main table and the extension table.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">小売チャネルのデータベースを拡張する場合は、メイン テーブルと拡張テーブルの間に主キーの関係を置くことをお勧めします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="231">
          <source>You can then read the data from the extension table by using the primary key.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">その後、主キーを使用して拡張テーブルからデータを読み取ることができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="232">
          <source><bpt id="p1">**</bpt>Steps<ept id="p1">**</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>ステップ<ept id="p1">**</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="233">
          <source>Create the extension table for Retail parameters in the channel table that has the primary key relation to the main table.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">メイン テーブルに主キーの関係があるチャネル テーブル内の、Retail パラメータの拡張テーブルを作成します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="234">
          <source>(In this case, the main table is Retail shared parameters.)</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">(この場合、メイン テーブルは小売共有パラメーターです。)</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="235">
          <source>Identify the CRT data request that reads the Retail parameters.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">小売パラメーターを読み取る CRT データ要求を識別します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="236">
          <source>Add a post-trigger for the data request.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">データ要求の転記トリガーを追加します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="237">
          <source>You will then be able to use the primary key of the shared parameters table to query your extension table for Retail shared parameters and read the custom fields.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">共有パラメータ テーブルの主キーを使用して、小売共有パラメータの拡張テーブルを照会し、カスタム フィールドを読み取ることができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="238">
          <source>You can get the primary key for the entity in the post-trigger request.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ポスト トリガー要求でエンティティの主キーを取得できます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="239">
          <source>That request will have the entity object, and that entity object will have all the required fields.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">エンティティ オブジェクトを持つその要求、およびすべての必須フィールドを持つそのエンティティ オブジェクト。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="240">
          <source>Add the custom fields as extension properties to the shared parameters entity in the CRT post-trigger, and send it to POS.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">カスタム フィールドを拡張プロパティとして、CRT 転記トリガーの共有パラメーター エンティティへ追加し、POS へ送信します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="241">
          <source><bpt id="p1">**</bpt>Reading extension properties in triggers<ept id="p1">**</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>トリガーの拡張機能プロパティの読み取り<ept id="p1">**</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="242">
          <source>The request that reads the data from the Retail parameters table is GetChannelConfigurationDataRequest.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">小売パラメータ テーブルからデータを読み込む要求は、GetChannelConfigurationDataRequest です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="243">
          <source>The following example shows how you can add a post-trigger for this request.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">次の例では、この要求のポスト トリガーを追加する方法を示します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="244">
          <source>You must change this query, based on your new field and table, or whatever condition you're using.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">新しいフィールドとテーブル、または使用している条件に基づいて、このクエリを変更する必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="245">
          <source>When you design the table, make sure that you have the primary key field from the parent table, so that you can query it by using the CRT entity.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">テーブルをデザインするときは、CRT エンティティを使用してクエリできるように、親テーブルの主キー フィールドがあることを確認します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="246">
          <source>Most CRT entities should have the primary key field in them, such as the <bpt id="p1">**</bpt>RecId<ept id="p1">**</ept> field or another relevant unique field that is used to select the record.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ほとんどの CRT エンティティには、<bpt id="p1">**</bpt>RecId<ept id="p1">**</ept> フィールドまたはレコードを選択するために使用される関連する別の固有フィールドなどの主キー フィールドがある必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="247">
          <source><bpt id="p1">**</bpt>Setting extension properties by overriding the handler<ept id="p1">**</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>ハンドラーを上書きすることによる拡張プロパティの設定<ept id="p1">**</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="248">
          <source><bpt id="p1">**</bpt>Scenario<ept id="p1">**</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>シナリオ<ept id="p1">**</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="249">
          <source>You created a new extension table for Customer.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">顧客用に新しい拡張テーブルを作成しました。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="250">
          <source>When values for the extension field for customer come from POS or CRT, you want to store the values in your custom table.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">顧客の拡張フィールドの値が POS または CRT から来た場合は、その値をカスタム テーブルに格納します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="251">
          <source>You can set extension properties either in a trigger or by overriding the handler.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">拡張のプロパティはトリガーで、またはハンドラーを上書きすることによって設定することができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="252">
          <source>If you just set some extension properties by reading from your extension table, you can use triggers.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">拡張テーブルから読み込んで拡張プロパティを設定しただけの場合、トリガーを使用することができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="253">
          <source><bpt id="p1">**</bpt>Steps<ept id="p1">**</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>ステップ<ept id="p1">**</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="254">
          <source>Create your extension table for Customers in the channel table that has the primary key relation to the main table.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">メイン テーブルに主キーの関係があるチャネル テーブル内の、顧客の拡張テーブルを作成します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="255">
          <source>(In this case, the main table is CustTable.)</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">(この場合、メイン テーブルは CustTable です。)</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="256">
          <source>Identify the CRT data request that sets data in CustTable.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">CustTable にデータを設定する CRT データ要求を識別します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="257">
          <source>Override the handler, and call the base request to set values in the main table (CustTable) and then the extension table.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ハンドラを上書きし、メイン テーブル (CustTable) で値を設定する基本要求を呼び出してからテーブルを拡張します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="258">
          <source>You can send any additional properties that you want to your extension procedure or view.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">拡張手順またはビューに必要な追加のプロパティを送信できます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="259">
          <source>The example that follows doesn't have the SQL scripts that are used.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">次の例では、使用される SQL スクリプトがありません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="260">
          <source>You can find the full sample code and scripts at the following locations in the Retail SDK.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">完全なサンプル コードとスクリプトは、Retail SDK の次の場所にあります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="261">
          <source><bpt id="p1">**</bpt>Location of the sample code in the Retail SDK<ept id="p1">**</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>Retail SDK のサンプル コードの場所<ept id="p1">**</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="262">
          <source>…<ph id="ph1">\\</ph>RetailSDK<ph id="ph2">\\</ph>SampleExtensions<ph id="ph3">\\</ph>CommerceRuntime<ph id="ph4">\\</ph>Extensions.EmailPreferenceSample</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">…<ph id="ph1">\\</ph>RetailSDK<ph id="ph2">\\</ph>SampleExtensions<ph id="ph3">\\</ph>CommerceRuntime<ph id="ph4">\\</ph>Extensions.EmailPreferenceSample</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="263">
          <source><bpt id="p1">**</bpt>Location of the scripts<ept id="p1">**</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>スクリプトの場所<ept id="p1">**</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="264">
          <source>…<ph id="ph1">\\</ph>RetailSDK<ph id="ph2">\\</ph>Documents<ph id="ph3">\\</ph>SampleExtensionsInstructions<ph id="ph4">\\</ph>EmailPreference</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">…<ph id="ph1">\\</ph>RetailSDK<ph id="ph2">\\</ph>ドキュメント<ph id="ph3">\\</ph>SampleExtensionsInstructions<ph id="ph4">\\</ph>EmailPreference</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="265">
          <source><bpt id="p1">**</bpt>Example<ept id="p1">**</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>例<ept id="p1">**</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="266">
          <source><bpt id="p1">**</bpt>Syntax to enable the property to be read later<ept id="p1">**</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>後で読み込むプロパティを有効にする構文<ept id="p1">**</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="267">
          <source>Using extension properties on CRT request and response types</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">CRT 要求タイプおよび応答タイプでの拡張機能プロパティの使用</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="268">
          <source>Like entities, request and response types can be extended to set and get extension properties.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">エンティティと同様、拡張機能プロパティを設定および取得するために要求および応答タイプを拡張できます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="269">
          <source>However, they will persist only for the lifecycle of the request and won't be available in POS.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ただし、要求のライフサイクルでのみ存続し、POS では使用できなくなります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="270">
          <source>If you want to save them to the database, you must write custom code.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">それらをデータベースに保存する場合は、カスタム コードを記述する必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="271">
          <source><bpt id="p1">**</bpt>Setting or reading extension properties in POS<ept id="p1">**</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>設定または POS の拡張子プロパティの読み取り<ept id="p1">**</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="272">
          <source>You can set extension properties in POS and send them to CRT by using the POS application programming interfaces (APIs).</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">POS で拡張プロパティーを設定して、POS アプリケーション プログラミング インターフェース (API) を使用してそれらを CRT に送信することができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="273">
          <source>Alternatively, you can send extension properties at the entity level.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">または、エンティティ レベルで拡張機能プロパティの送信が可能です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="274">
          <source>To set an extension property on the cart line, you use SaveExtensionPropertiesOnCartLinesClientRequest.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">カート行に拡張プロパティを設定するには、SaveExtensionPropertiesOnCartLinesClientRequest を使用します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="275">
          <source>Likewise, for the cart header, you use SaveExtensionPropertiesOnCartClientRequest.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">同様に、買い物カゴ ヘッダーに対して、SaveExtensionPropertiesOnCartClientRequest を使用します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="276">
          <source>Here is an example.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">次に例を示します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="277">
          <source><bpt id="p1">**</bpt>Reading the extension property from the cart in POS<ept id="p1">**</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>POS のカートから拡張プロパティの読み取り<ept id="p1">**</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="278">
          <source>Likewise, you can read the extension property from all the other entities, such as products, customers, and addresses.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">同様に、製品、顧客、および住所など他のすべてのエンティティから拡張機能プロパティを読み取ることができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="279">
          <source>Implementing a new CRT service that handles multiple new requests</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">複数の新しい要求を処理する新しい CRT サービスの実装</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="280">
          <source>It's a typical case to implement a new CRT service.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">新しい CRT サービスを実装することが一般的です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="281">
          <source>First, you must create new request and response classes.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">最初に、新しい要求および応答クラスを作成する必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="282">
          <source>Creating the request and response classes</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">要求および応答クラスを作成しています</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="283">
          <source>For serialization to work, the new request type must implement the <bpt id="p1">**</bpt><ph id="ph1">\[</ph>DataContract<ph id="ph2">\]</ph><ept id="p1">**</ept> and <bpt id="p2">**</bpt><ph id="ph3">\[</ph>DataMember<ph id="ph4">\]</ph><ept id="p2">**</ept> attributes.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">作業のシリアル化については、新しい要求タイプは <bpt id="p1">**</bpt><ph id="ph1">\[</ph>DataContract<ph id="ph2">\]</ph><ept id="p1">**</ept> および <bpt id="p2">**</bpt><ph id="ph3">\[</ph>DataMember<ph id="ph4">\]</ph><ept id="p2">**</ept> 属性を実装する必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="284">
          <source>The new response type resembles the request type.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">新しい応答タイプは要求タイプに似ています。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="285">
          <source>Next, you must create a new CRT service that uses the request and response types.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">次に、要求および応答タイプを使用する新しい CRT サービスを作成する必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="286">
          <source>Creating a new CRT service</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">新しい CRT サービス注文を作成しています</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="287">
          <source>Implement the new service.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">新しいサービスを実装します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="288">
          <source>Implement two members of the interface.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">インターフェイスのメンバー 2 つを実装します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="289">
          <source>The <bpt id="p1">**</bpt>SupportedRequestTypes<ept id="p1">**</ept> member returns a list of all requests that this service can handle.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>SupportedRequestTypes<ept id="p1">**</ept> メンバーは、このサービスが処理できるすべての要求の一覧を返します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="290">
          <source>The execute method is the method that the CRT calls for you if a request for this service is run.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">実行メソッドは、このサービスの要求が実行された場合に CRT が呼び出すメソッドです。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="291">
          <source>In the commerceRuntime.Config file, update the <bpt id="p1">**</bpt>composition<ept id="p1">**</ept> section (or the equivalent section) to register this service.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">CommerceRuntime.Config ファイルで、<bpt id="p1">**</bpt>合成<ept id="p1">**</ept>セクション (または同等のセクション) を更新してこのサービスを登録します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="292">
          <source>Note that you can register single types or all types from an assembly.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">アセンブリから 1 つの型またはすべての型を登録できることに注意してください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="293">
          <source>The CommerceRuntime engine will find all IRequestHandler derived types.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">CommerceRuntime エンジンは、すべての IRequestHandler 派生タイプを見つけます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="294">
          <source>Optional: Use the CommerceRuntime Test Host to do a test run of your service.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">オプション: CommerceRuntime テスト ホストを使用してサービスのテストを行います。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="295">
          <source>Implementing a new CRT service that handles a single new request</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">1 つの新しい要求を処理する新しい CRT サービスの実装</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="296">
          <source>It’s slightly easier to create a single-request service.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">単一の要求サービスを作成すると少し便利になります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="297">
          <source>Registration is done as described in the previous procedure.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">前の手順で説明したように登録が行われます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="298">
          <source>Implementing a new CRT service that overrides the functionality of an existing request</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">既存の要求の機能をオーバーライドする新しい CRT サービスの実装</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="299">
          <source>In some cases, the request and response types are sufficient, but the service implementation must be changed.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">場合によっては、要求および応答タイプは十分ですが、サービスの実装を変更する必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="300">
          <source>If some new data must be transmitted, you can also extend entity, request, or response objects by using extension properties.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">新しいデータを送信する必要がある場合は、拡張機能のプロパティを使用してエンティティ、要求、または応答オブジェクトを拡張することもします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="301">
          <source>In this scenario, you can create the service as described earlier and use the existing IRequestHandler types.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このシナリオでは、前述のようにサービスを作成して既存の IRequestHandler 型を使用できます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="302">
          <source>Additionally, registration in the commerceRuntime.Config file must precede registration of the service that should be overridden.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">また、commerceRuntime.Config ファイルの登録は、上書きすべきサービスの登録より前にする必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="303">
          <source>This registration order is important because of the way that the Managed Extensibility Framework (MEF) loads the extension dynamic-link libraries (DLLs).</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この登録順序は、Managed Extensibility Framework (MEF) が拡張ダイナミック リンク ライブラリ (DLL) を読み込む方法のために重要です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="304">
          <source>The types that are higher in the file win.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ファイルより高いタイプが優先されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="305">
          <source>Implementing a new CRT entity and using it in new CRT service</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">新しい CRT エンティティの実装および新しい CRT サービスでの使用</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="306">
          <source>Any new entity must be of the <bpt id="p1">**</bpt>CommerceEntity<ept id="p1">**</ept> type.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">すべての新しいエンティティは、<bpt id="p1">**</bpt>CommerceEntity<ept id="p1">**</ept> タイプであることが必要です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="307">
          <source>When you use this type, lots of low-level functionality is automatically handled for you.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このタイプを使用するとき、多くの低レベルの機能は自動的に処理されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="308">
          <source>The following example, which is taken from the StoreHours sample, shows how to create an entity that is bound to the database table.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">次の例は、StoreHours サンプルから取得したもので、データベース テーブルにバインドされたエンティティを作成する方法を示しています。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="309">
          <source>This is the usual case.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">これは、通常のケースです。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="310">
          <source>When you want to use the new entity in a service, the process is straightforward.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">サービスで新しいエンティティを使用する場合、プロセスは簡単です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="311">
          <source>As described earlier, you create a new service as a derived IRequestHandler.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">前述のように、派生 IRequestHandler として新しいサービスを作成します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="312">
          <source>Then either use or return the new entity.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">次に、新しいエンティティを使用するか返すかのいずれかを実行します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="313">
          <source>The following example shows how to read the entity from the database and return it as part of the response.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">次の例は、データベースからエンティティを読み取り、それを応答の一部として返す方法を示しています。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="314">
          <source>For the preceding example, the CRT runtime engine automatically makes a query to the channel database via the registered data adapter.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">前の例では、CRT ランタイム エンジンは、登録されているデータ アダプターを介してチャンネルに自動的にクエリを作成します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="315">
          <source>It queries a type that has the name <bpt id="p1">**</bpt>crt.ISVRetailStoreHoursView<ept id="p1">**</ept>, and generates a <bpt id="p2">**</bpt>where<ept id="p2">**</ept> clause and columns as specified in the code.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">名前 <bpt id="p1">**</bpt>crt.ISVRetailStoreHoursView<ept id="p1">**</ept> を持つ型を照会して、コードで指定された <bpt id="p2">**</bpt>where<ept id="p2">**</ept> 句および列を生成します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="316">
          <source>The customizer is responsible for providing the SQL objects as part of the customization.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">カスタマイザーは、カスタマイズの一部として SQL オブジェクトを提供する役割を担います。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="317">
          <source>Adding pre-triggers and post-triggers for a specific request</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">特定の要求のプレトリガーとポストトリガーの追加</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="318">
          <source>In some cases, some processing must be done before or after a request is handled.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">場合によっては、要求の前後で必要になる処理もあります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="319">
          <source>There are two hooks that can be used to run additional code.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">追加のコードを実行するために使用できる 2 つのフックがあります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="320">
          <source>These hooks are called pre-triggers and post-triggers.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">これらのフックはプレトリガーおよびポストトリガーと呼ばれます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="321">
          <source>Follow these steps to create new triggers and associate them with a request.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">新しいトリガーを作成して要求に関連付けるには、これらの手順に従います。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="322">
          <source>Create a new trigger class that implements IRequestTrigger.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">IRequestTrigger を実装する新しいトリガー クラスを作成します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="323">
          <source>In the <bpt id="p1">**</bpt>IRequest.SupportedRequestTypes<ept id="p1">**</ept> property, return the list of requests that this trigger should be run for.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>IRequest.SupportedRequestTypes<ept id="p1">**</ept> プロパティで、このトリガーを実行する必要がある要求の一覧を返します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="324">
          <source>Implement the functions that are called before and after the request.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">要求の前後に呼び出される関数を実装します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="325">
          <source>Register the class in the commerceRuntime.Config file.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">commerceRuntime.Config ファイルでクラスを登録します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="326">
          <source>Retail Server extensibility scenarios</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Retail サーバーの拡張機能シナリオ</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="327">
          <source>Adding a new ODATA action to an existing controller</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">既存のコントローラーへの新しい ODATA アクションの追加</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="328">
          <source>In the easiest scenario, you must add a new application programming interface (API) for a slightly different use case.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">最も簡単なシナリオでは、わずかに異なるユース ケースのために新しいアプリケーション プログラミング インターフェイス (API) を追加する必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="329">
          <source>To make this scenario work, you can add the new action through inheritance.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このシナリオを機能させるには、継承によって新しいアクションを追加します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="330">
          <source>For any changes to the APIs to Retail Server, you must follow these steps.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Retail サーバーへの API の任意の変更については、次の手順を実行する必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="331">
          <source>Implement the new action or controller.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">新しいアクションまたはコントローラーを実装します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="332">
          <source>Override the requirements of the model factory to add the new corresponding metadata.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">新しい対応するメタデータを追加するためのモデル出荷時の要件を上書きします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="333">
          <source>The following example, which is taken from the Retail SDK, shows how to extend an existing controller so that it has a POST action.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">次の例は、Retail SDK から取得したもので、既存のコントローラーを拡張して POST アクションを持つようにする方法を示しています。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="334">
          <source>Next, override the model factory.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">次に、モデル ファクトリをオーバーライドします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="335">
          <source>Before clients can use this new customization, you must adjust the build system to generate the Retail Server proxy code for the new model factory.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">クライアントがこの新しいカスタマイズを使用する前に、新しいモデル ファクトリ用の Retail サーバー プロキシ コードを生成するためにビルド システムを調整する必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="336">
          <source>This configuration step is done in the build system.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この構成ステップはビルド システムで実行されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="337">
          <source>Finally, you must adjust the web.config file.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">最後に、web.config ファイルを調整する必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="338">
          <source>You must complete this step in the packaging project for Retail Server in the SDK.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">SDK の Retail サーバーの梱包プロジェクトでは、このステップを完了する必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="339">
          <source>If local tests will be done, you can also optionally complete this step on the local development topology machine that is used for testing.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ローカルのテストが行われている場合、テストに使用されるローカル開発トポロジー コンピューターでこの手順を任意で実行できます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="340">
          <source>Adding a new simple controller for an entity</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">エンティティの新しい簡単なコントローラーの追加</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="341">
          <source>Suppose that you have a simple entity and require a controller to fetch the data.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">単純なエンティティがあり、データをフェッチするコント ローラーを必要としているとします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="342">
          <source>For an example, see the StoreHours sample in the Retail SDK.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">例については、Retail SDK で StoreHours サンプルを参照してください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="343">
          <source>A new Retail Server controller makes sense, and all the low-level work is done in the CRT (new entity, request, response, and service).</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">新しい Retail サーバー コントローラーには意味があり、低レベルのすべての作業が CRT (新しいエンティティ、要求、応答、およびサービス) で実行されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="344">
          <source>To create a new controller, you derive from CommerceController.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">新しいコントローラを作成するには、CommerceController から派生します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="345">
          <source>An example is shown here.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">例としてここに表示します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="346">
          <source>The controller name is important and must match the name of the entity.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">コントローラー名は重要であり、エンティティの名前と一致する必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="347">
          <source>For new entities, you must also override the factory’s <bpt id="p1">**</bpt>BuildEntitySets()<ept id="p1">**</ept> method, as shown in the following example.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">新しいエンティティについては、次の例に示すように、工場の <bpt id="p1">**</bpt>BuildEntitySets()<ept id="p1">**</ept> メソッドを上書きする必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="348">
          <source>How to call the new retail server API from MPOS/Cloud POS:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">MPOS/クラウド POS から新しい小売サーバー API を呼び出す方法:</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="349">
          <source>Before calling the new retail server API please make sure you have performed the below steps:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">新しい小売サーバー API を呼び出す前に、以下の手順を実行してください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="350">
          <source>Register your new retail server extension in Retail server web.config file:  <ph id="ph1">&amp;lt;</ph>add source="assembly" value="<bpt id="p1">**</bpt>Your assembly name<ept id="p1">**</ept>" /<ph id="ph2">&amp;gt;</ph> under the extensionComposition section.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Retail サーバー web.config ファイルで新しい Retail サーバー拡張子を登録します: <ph id="ph1">&amp;lt;</ph>ソースの追加 =「アセンブリ」値 ="<bpt id="p1">**</bpt>アセンブリ名<ept id="p1">**</ept>" /<ph id="ph2">&amp;gt;</ph> は、extensionComposition セクションの下にあります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="351">
          <source>Add the new retail server extension in the Customization.settings file.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Customization.settings ファイルの新しい Retail サーバー拡張子を追加します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="352">
          <source>You can find this file in RetailSdk<ph id="ph1">\\</ph>BuildTools<ph id="ph2">&amp;lt;</ph>RetailServerLibraryPathForProxyGeneration Condition="'$(RetailServerLibraryPathForProxyGeneration)' == ''"<ph id="ph3">&amp;gt;</ph>$(SdkReferencesPath)<ph id="ph4">\\</ph><bpt id="p1">**</bpt>Your assembly name.dll<ept id="p1">**</ept><ph id="ph5">&amp;lt;</ph>/RetailServerLibraryPathForProxyGeneration<ph id="ph6">&amp;gt;</ph> <ph id="ph7">&amp;lt;</ph>/PropertyGroup<ph id="ph8">&amp;gt;</ph></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このファイルは、RetailSdk<ph id="ph1">\\</ph>BuildTools<ph id="ph2">&amp;lt;</ph>RetailServerLibraryPathForProxyGeneration Condition="'$(RetailServerLibraryPathForProxyGeneration)' == ''"<ph id="ph3">&amp;gt;</ph>$(SdkReferencesPath)<ph id="ph4">\\</ph><bpt id="p1">**</bpt>Your assembly name.dll<ept id="p1">**</ept><ph id="ph5">&amp;lt;</ph>/RetailServerLibraryPathForProxyGeneration<ph id="ph6">&amp;gt;</ph> <ph id="ph7">&amp;lt;</ph>/PropertyGroup<ph id="ph8">&amp;gt;</ph> に存在します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="353">
          <source>Move both the CRT and Retail server extension dlls into the <bpt id="p1">**</bpt>…<ph id="ph1">\\</ph>RetailServer<ph id="ph2">\\</ph>webroot<ph id="ph3">\\</ph>bin<ph id="ph4">\\</ph>Ext<ept id="p1">**</ept> folder.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">CRT と Retail サーバー拡張子 dlls の両方を <bpt id="p1">**</bpt>…<ph id="ph1">\\</ph>RetailServer<ph id="ph2">\\</ph>webroot<ph id="ph3">\\</ph>bin<ph id="ph4">\\</ph>Ext<ept id="p1">**</ept> フォルダーに移動します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="354">
          <source>If you have a CRT extension that is related to the new retail server API, then update that information in the CommerceRuntime.Ext.config file in the <bpt id="p1">**</bpt>…<ph id="ph1">\\</ph>RetailServer<ph id="ph2">\\</ph>webroot<ph id="ph3">\\</ph>bin<ph id="ph4">\\</ph>Ext<ept id="p1">**</ept> folder.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">新しい小売サーバー API に関連する CRT 拡張機能をご使用の場合、<bpt id="p1">**</bpt>…<ph id="ph1">\\</ph>RetailServer<ph id="ph2">\\</ph>webroot<ph id="ph3">\\</ph>bin<ph id="ph4">\\</ph>Ext<ept id="p1">**</ept> フォルダー内の CommerceRuntime.Ext.config ファイルの情報を更新してください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="355">
          <source><ph id="ph1">&amp;lt;</ph>add source="assembly" value="<bpt id="p1">**</bpt>Your assembly name<ept id="p1">**</ept>" /<ph id="ph2">&amp;gt;</ph></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><ph id="ph1">&amp;lt;</ph>ソースの追加 = 「アセンブリ」値 = "<bpt id="p1">**</bpt>アセンブリ名<ept id="p1">**</ept>" /<ph id="ph2">&amp;gt;</ph></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="356">
          <source>Use inetmgr to browse to the retail server metadata and verify whether your entity is exposed in the xml.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">inetmgr を使用して小売サーバーのメタデータを参照し、エンティティが xml で公開されているかどうかを確認します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="357">
          <source>Compile and build the mpos/Cloud POS to regenerate the proxy.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">mpos/クラウド POSをコンパイルしてビルドし、プロキシを再生成します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="358">
          <source>During compile mpos regenerates all the entities defined in the retail server metadata, so that you can call the new entities using the commerce context like below:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">コンパイラ中に、mpos は小売サーバーのメタデータで定義されたすべてのエンティティを再生成します。これにより、以下のようなコマース コンテキストを使用して新しいエンティティを呼び出すことができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="359">
          <source>Do not change or add anything in the Retail server web.config file or Retail server folder, with the expection of the extension composition section and possibly to copy custom assemblies in the bin\ext folder.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Retail サーバー web.config ファイルまたは Retail サーバー フォルダ内で何も変更または追加しないでください。拡張合成セクションは除外され、おそらく bin\ext フォルダにカスタム アセンブリがコピーされます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="360">
          <source>During deployment, only the extensionComposition section in the web.config file will be merged, all the other sections will be overwritten and only the assemblies in the <bpt id="p1">**</bpt>...<ph id="ph1">\\</ph>RetailServer<ph id="ph2">\\</ph>webroot<ph id="ph3">\\</ph>bin<ph id="ph4">\\</ph>Ext<ept id="p1">**</ept> folder be merged with other assemblies.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">配置時に web.config ファイル内の extensionComposition セクションのみマージされ、他のセクションはすべて上書きされ、<bpt id="p1">**</bpt>...<ph id="ph1">\\</ph>RetailServer<ph id="ph2">\\</ph>webroot<ph id="ph3">\\</ph>bin<ph id="ph4">\\</ph>Ext<ept id="p1">**</ept> フォルダのアセンブリのみが他のアセンブリとマージされます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="361">
          <source>This file will be overwritten based on the latest binary package.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このファイルは、最新バイナリ パッケージに基づいて上書きされます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="362">
          <source>Do not use the Retail server web.config file to add or modify any custom app settings.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">カスタム アプリケーションの設定を追加、または、変更するのに Retail サーバー web.config ファイルは使用しません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="363">
          <source>Cross loyalty sample:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">クロス ロイヤルティ サンプル。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="364">
          <source>Store hours sample:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">店舗の時間のサンプル:</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="365">
          <source>Please refer the retail SDK POS.Extension.CrossloaylySample and POS.Extension.SToreHoursSample sample projects for more details on how to call the new retail server api in mpos.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">mpos で新しい小売サーバー API を呼び出す方法について詳しくは、小売 SDK POS.Extension.CrossloaylySample および POS.Extension.SToreHoursSample サンプル プロジェクトをご覧ください。</target></trans-unit>
      </group>
    </body>
  </file>
</xliff>