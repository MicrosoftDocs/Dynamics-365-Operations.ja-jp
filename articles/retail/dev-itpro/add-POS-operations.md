<?xml version="1.0" encoding="UTF-8"?>
<xliff xmlns:logoport="urn:logoport:xliffeditor:xliff-extras:1.0" xmlns:tilt="urn:logoport:xliffeditor:tilt-non-translatables:1.0" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns="urn:oasis:names:tc:xliff:document:1.2" xmlns:xliffext="urn:microsoft:content:schema:xliffextensions" version="1.2" xsi:schemaLocation="urn:oasis:names:tc:xliff:document:1.2 xliff-core-1.2-transitional.xsd">
  <file datatype="xml" source-language="en-US" original="add-POS-operations.md" target-language="ja-JP">
    <header>
      <tool tool-company="Microsoft" tool-version="1.0-7889195" tool-name="mdxliff" tool-id="mdxliff"/>
      <xliffext:skl_file_name>add-POS-operations.170b8d.ce88f17248434b50a0ce5f1460735da76ad34dd5.skl</xliffext:skl_file_name>
      <xliffext:version>1.2</xliffext:version>
      <xliffext:ms.openlocfilehash>ce88f17248434b50a0ce5f1460735da76ad34dd5</xliffext:ms.openlocfilehash>
      <xliffext:ms.sourcegitcommit>9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b</xliffext:ms.sourcegitcommit>
      <xliffext:ms.lasthandoff>05/15/2019</xliffext:ms.lasthandoff>
      <xliffext:ms.openlocfilepath>articles\retail\dev-itpro\add-POS-operations.md</xliffext:ms.openlocfilepath>
    </header>
    <body>
      <group extype="content" id="content">
        <trans-unit xml:space="preserve" translate="yes" id="101" restype="x-metadata">
          <source>Add POS operations to POS layouts by using Button grid designer</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ボタン グリッドのデザイナーを使用して、POS 操作を POS レイアウトに追加</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="102" restype="x-metadata">
          <source>This topic explains how to create a new POS operation and add it to the POS layout by using Button grid designer.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このトピックでは、新しい POS 工程を作成し、ボタン グリッド デザイナーを使用して POS レイアウトに追加する方法について説明します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="103">
          <source>Add POS operations to POS layouts by using Button grid designer</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ボタン グリッドのデザイナーを使用して、POS 操作を POS レイアウトに追加</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="104">
          <source>This topic explains how to create a new point of sale (POS) operation and add it to the POS layout by using Button grid designer.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このトピックでは、新しい販売時点管理 (POS) 工程を作成し、ボタン グリッド デザイナーを使用して POS レイアウトに追加する方法について説明します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="105">
          <source>This topic applies to the following applications where Platform update 8 and the Application update 4 hotfix are installed:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このトピックは、プラットフォーム更新プログラム 8 とアプリケーション更新プログラム 4 修正プログラムがインストールされている次のアプリケーションに適用されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="106">
          <source>Microsoft Dynamics 365 for Finance and Operations</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Microsoft Dynamics 365 for Finance and Operations</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="107">
          <source>Microsoft Dynamics 365 for Retail</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Microsoft Dynamics 365 for Retail</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="108">
          <source>If you want your business logic to be run in the POS when users click a button, you should create POS operations.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ユーザーがボタンをクリックしたときに POS でビジネス ロジックを実行したい場合は、POS 操作を作成する必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="109">
          <source>POS operations can run multiple activities or workflows.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">POS 操作では複数の活動およびワークフローを実行できます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="110">
          <source>For example, they can open a new view, ask for user input, or run business logic.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">たとえば、新しいビューを開いたり、ユーザーの入力を求めたり、ビジネス ロジックを実行したりすることができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="111">
          <source>All standard and custom POS operations support pre-triggers and post-triggers.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">すべての標準およびカスタム POS 操作では、プレ トリガーおよびポスト トリガーをサポートします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="112">
          <source>If logic should be run as part of another workflow, or if no button click is required, create POS request/response application programming interfaces (APIs).</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ロジックを別のワークフローの一部として実行する必要のある場合、もしくはボタンのクリックが不要な場合は、POS 要求/応答アプリケーション プログラミング インターフェイス (API) を作成します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="113">
          <source>POS operations aren't required in these scenarios.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">POS 操作はこれらのシナリオで必須ではありません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="114">
          <source>Every operation should implement the following elements:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">毎回の操作では、次の要素を実装する必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="115">
          <source><bpt id="p1">**</bpt>Operation request<ept id="p1">**</ept> – The operation request is extended from the <bpt id="p2">**</bpt>ExtensionOperationRequestBase<ept id="p2">**</ept> class.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>操作要求<ept id="p1">**</ept> – 操作要求は、<bpt id="p2">**</bpt>ExtensionOperationRequestBase<ept id="p2">**</ept> クラスから拡張されています。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="116">
          <source>It contains all the input that is required in order to run the operation.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">操作を実行するために必要なすべての入力が含まれています。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="117">
          <source><bpt id="p1">**</bpt>Operation response<ept id="p1">**</ept> – The operation response is extended from the <bpt id="p2">**</bpt>Response<ept id="p2">**</ept> class.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>操作要求<ept id="p1">**</ept> – 操作要求は<bpt id="p2">**</bpt>応答<ept id="p2">**</ept>クラスから拡張されています。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="118">
          <source>It contains the whole response, based on execution of the operation.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">工程の実行に基づく応答全体が含まれています。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="119">
          <source><bpt id="p1">**</bpt>Operation factory<ept id="p1">**</ept> – The operation factory links the button click for the operation with the operation handler.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>操作ファクトリ<ept id="p1">**</ept> – 操作ファクトリは、操作のためのボタンのクリックを操作ハンドラーとリンクします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="120">
          <source><bpt id="p1">**</bpt>Operation handler<ept id="p1">**</ept> – The operation handler is extended from the <bpt id="p2">**</bpt>ExtensionOperationRequestHandlerBase<ept id="p2">**</ept> class.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>操作ハンドラー<ept id="p1">**</ept> – 操作ハンドラーは、<bpt id="p2">**</bpt>ExtensionOperationRequestHandlerBase<ept id="p2">**</ept> クラスから拡張されています。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="121">
          <source>It contains core logic for the operation.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">工程のコア ロジックが含まれています。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="122">
          <source>All the business logic should be written in the handler, and it should return the operation response after the operation is run.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">すべてのビジネス ロジックはハンドラーに記述され、操作実行後、工程応答に戻される必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="123">
          <source>Create a POS operation</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">POS 操作の作成</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="124">
          <source>This section explains how to create a sample operation that does simplified end-of-day (EOD) processing.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このセクションでは、簡略化された営業終了 (EOD) 処理を行うサンプル工程を作成する方法について説明します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="125">
          <source>This operation calls the standard Tender removal, Safe drop, Tender declaration, and Close shift operations in a sequence.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この操作は、シーケンス内の標準の支払/入金の削除、金庫保管、支払/入金申告、およびシフトのクローズ操作を呼び出します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="126">
          <source>Therefore, this one operation combines multiples steps.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">したがって、この 1 回の操作は、複数の手順を組み合わせたものです。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="127">
          <source>It is run based on the conditions that you define.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">定義する条件に基づいて実行されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="128">
          <source>You can create a new operation and run your own custom logic, you can call existing POS operations, such as Add item to cart and Apply line discount, or you can call existing APIs, such as Get current cart and Set extension properties.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">新しい工程を作成して独自のカスタム ロジックを実行したり、カートにアイテムを追加したり、ライン割引を適用したりするなど、既存の POS オペレーションを呼び出すことも、現在のカートを取得する、拡張プロパティを設定するなどの既存の API を呼び出すこともできます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="129">
          <source>Start Microsoft Visual Studio 2015 in administrator mode.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Microsoft Visual Studio 2015 を管理者モードで起動します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="130">
          <source>From <bpt id="p1">**</bpt>...\RetailSDK\POSOpen<ept id="p1">**</ept>, open the <bpt id="p2">**</bpt>ModernPOS<ept id="p2">**</ept> solution.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>...\RetailSDK\POSOpen<ept id="p1">**</ept> から、<bpt id="p2">**</bpt>ModernPOS<ept id="p2">**</ept> ソリューションを開きます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="131">
          <source>Under the <bpt id="p1">**</bpt>POS.Extensions<ept id="p1">**</ept> project, create a folder that is named <bpt id="p2">**</bpt>EODSample<ept id="p2">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>POS.Extensions<ept id="p1">**</ept> プロジェクトで、<bpt id="p2">**</bpt>EODSample<ept id="p2">**</ept> というフォルダーを作成します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="132">
          <source>Under the <bpt id="p1">**</bpt>EODSample<ept id="p1">**</ept> folder, create a folder that is named <bpt id="p2">**</bpt>Operations<ept id="p2">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>EODSample<ept id="p1">**</ept> フォルダーで、<bpt id="p2">**</bpt>Operations<ept id="p2">**</ept> というフォルダーを作成します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="133">
          <source>Create the operation request class</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">operation request クラスの作成</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="134">
          <source>In the <bpt id="p1">**</bpt>Operations<ept id="p1">**</ept> folder, create a typescript (.ts) file that is named <bpt id="p2">**</bpt>EndOfDayOperationRequest.ts<ept id="p2">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>工程<ept id="p1">**</ept> フォルダで、<bpt id="p2">**</bpt>EndOfDayOperationRequest.ts<ept id="p2">**</ept> という typescript (.ts) ファイルを作成します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="135">
          <source>Open the <bpt id="p1">**</bpt>EndOfDayOperationRequest.ts<ept id="p1">**</ept> file, and add the following <bpt id="p2">**</bpt>import<ept id="p2">**</ept> statements to import the relevant entities and context.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>EndOfDayOperationRequest.ts<ept id="p1">**</ept> ファイルを開き、次の <bpt id="p2">**</bpt>import<ept id="p2">**</ept> ステートメントを追加して関連するエンティティおよびコンテキストをインポートします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="136">
          <source>Add a class that is named <bpt id="p1">**</bpt>EndOfDayOperationRequest<ept id="p1">**</ept>, and extend it from the <bpt id="p2">**</bpt>ExtensionOperationRequestBase<ept id="p2">**</ept> class.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>EndOfDayOperationRequest<ept id="p1">**</ept> という名のクラスを追加し、<bpt id="p2">**</bpt>ExtensionOperationRequestBase<ept id="p2">**</ept> クラスから拡張します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="137">
          <source>In this example, the operation ID in the <bpt id="p1">**</bpt>super<ept id="p1">**</ept> method is initialized to <bpt id="p2">**</bpt>5001<ept id="p2">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この例では、<bpt id="p1">**</bpt>super<ept id="p1">**</ept> メソッドでの工程 ID が <bpt id="p2">**</bpt>5001<ept id="p2">**</ept> に初期化されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="138">
          <source>However, you can use any operation ID starting from 4001.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ただし、4001 からすべての操作 ID を使用できます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="139">
          <source>Operation IDs 0 through 4000 are reserved for internal Retail POS operations, and no two operations should have the same operation ID.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">操作 ID 0 ～ 4000 が内部の Retail POS 操作に対して引当が済んでおり、2 つの操作が同じ操作 ID を持つ必要がありません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="140">
          <source>Additionally, the custom parameters field appears in Button grid designer properties only if the operation ID is 4001 or higher.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">さらに、顧客パラメーター フィールドは工程 ID が 4001 またはそれ以上である場合にのみ、ボタン グリッド デザイナー プロパティに表示されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="141">
          <source>(You can use custom parameters field to pass parameters to the POS operation from Retail headquarters).</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">(カスタム パラメーターフィールドを使用して、小売用バックオフィスから POS 操作にパラメータを渡すことができます。)</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="142">
          <source>Create the operation response class</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">operation response クラスの作成</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="143">
          <source>In the <bpt id="p1">**</bpt>Operations<ept id="p1">**</ept> folder, create a typescript (.ts) file that is named <bpt id="p2">**</bpt>EndOfDayOperationResponse.ts<ept id="p2">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>工程<ept id="p1">**</ept> フォルダーで、<bpt id="p2">**</bpt>EndOfDayOperationResponse.ts<ept id="p2">**</ept> という typescript (.ts) ファイルを作成します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="144">
          <source>Open the <bpt id="p1">**</bpt>EndOfDayOperationResponse.ts<ept id="p1">**</ept> file, and add the following <bpt id="p2">**</bpt>import<ept id="p2">**</ept> statement to import the relevant entities and context.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>EndOfDayOperationResponse.ts<ept id="p1">**</ept> ファイルを開き、次の <bpt id="p2">**</bpt>import<ept id="p2">**</ept> ステートメントを追加して関連するエンティティおよびコンテキストをインポートします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="145">
          <source>Add a class that is named <bpt id="p1">**</bpt>EndOfDayOperationResponse<ept id="p1">**</ept>, and extend it from the <bpt id="p2">**</bpt>Response<ept id="p2">**</ept> class.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>EndOfDayOperationResponse<ept id="p1">**</ept> という名のクラスを追加し、<bpt id="p2">**</bpt>応答<ept id="p2">**</ept>クラスから拡張します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="146">
          <source>Create the operation handler class</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">operation handler クラスの作成</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="147">
          <source>In the <bpt id="p1">**</bpt>Operations<ept id="p1">**</ept> folder, create a typescript (.ts) file that is named <bpt id="p2">**</bpt>EndOfDayOperationRequestHandler.ts<ept id="p2">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>工程<ept id="p1">**</ept> フォルダーで、<bpt id="p2">**</bpt>EndOfDayOperationRequestHandler.ts<ept id="p2">**</ept> という typescript (.ts) ファイルを作成します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="148">
          <source>Open the <bpt id="p1">**</bpt>EndOfDayOperationRequestHandler.ts<ept id="p1">**</ept> file, and add the following <bpt id="p2">**</bpt>import<ept id="p2">**</ept> statements to import the relevant entities and context.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>EndOfDayOperationRequestHandler.ts<ept id="p1">**</ept> ファイルを開き、次の <bpt id="p2">**</bpt>import<ept id="p2">**</ept> ステートメントを追加して関連するエンティティおよびコンテキストをインポートします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="149">
          <source>Add a class that is named <bpt id="p1">**</bpt>EndOfDayOperationRequestHandler<ept id="p1">**</ept>, and extend it from the <bpt id="p2">**</bpt>ExtensionOperationRequestHandlerBase<ept id="p2">**</ept> class.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>EndOfDayOperationRequestHandler<ept id="p1">**</ept> という名のクラスを追加し、<bpt id="p2">**</bpt>ExtensionOperationRequestHandlerBase<ept id="p2">**</ept> クラスから拡張します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="150">
          <source>Each handler should implement two methods:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">各ハンドラーは、2 つのメソッドを実装する必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="151">
          <source>supportedRequestType</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">supportedRequestType</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="152">
          <source>executeAsync</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">executeAsync</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="153">
          <source>Add the supported request type in the class.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">サポートされている要求タイプをクラスに追加します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="154">
          <source>Implement the <bpt id="p1">**</bpt>executeAsync<ept id="p1">**</ept> method.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>executeAsync<ept id="p1">**</ept> メソッドを実装します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="155">
          <source>The overall code should look like this.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">全体的なコードは、次のようになります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="156">
          <source>Create the operation factory class</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">operation factory クラスの作成</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="157">
          <source>In the <bpt id="p1">**</bpt>Operations<ept id="p1">**</ept> folder, create a typescript (.ts) file that is named <bpt id="p2">**</bpt>EndOfDayOperationRequestFactory.ts<ept id="p2">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>工程<ept id="p1">**</ept> フォルダで、<bpt id="p2">**</bpt>EndOfDayOperationRequestFactory.ts<ept id="p2">**</ept> という typescript (.ts) ファイルを作成します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="158">
          <source>Open the <bpt id="p1">**</bpt>EndOfDayOperationRequestFactory.ts<ept id="p1">**</ept> file, and add the following <bpt id="p2">**</bpt>import<ept id="p2">**</ept> statements to import the relevant entities and context.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>EndOfDayOperationRequestFactory.ts<ept id="p1">**</ept> ファイルを開き、次の <bpt id="p2">**</bpt>import<ept id="p2">**</ept> ステートメントを追加して関連するエンティティおよびコンテキストをインポートします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="159">
          <source>Add a function to link the operation handler and the operation button.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">操作ハンドラーおよび操作ボタンをリンクする機能を追加します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="160">
          <source>The overall code should look like this.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">全体的なコードは、次のようになります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="161">
          <source>Open the <bpt id="p1">**</bpt>manifest.json<ept id="p1">**</ept> file, and paste in the following code.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>manifest.json<ept id="p1">**</ept> ファイルを開き、次のコードに貼り付けます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="162">
          <source>Open the <bpt id="p1">**</bpt>extensions.json<ept id="p1">**</ept> file under the <bpt id="p2">**</bpt>POS.Extensions<ept id="p2">**</ept> project, and update it with <bpt id="p3">**</bpt>EODSample<ept id="p3">**</ept>, so that the POS will include the extension at runtime.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>extensions.json<ept id="p1">**</ept> ファイルを <bpt id="p2">**</bpt>POS.Extensions<ept id="p2">**</ept> プロジェクトで開いて、<bpt id="p3">**</bpt>EODSample<ept id="p3">**</ept> で更新し、実行時に POS に拡張機能が含まれるようにします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="163">
          <source>Open the <bpt id="p1">**</bpt>tsconfig.json<ept id="p1">**</ept> file, and comment out the extension package folders in the exclude list.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>tsconfig.json<ept id="p1">**</ept> ファイルを開いて、拡張パッケージ フォルダーを除外リストでコメント アウトします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="164">
          <source>The POS will use this file to include or exclude the extension.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">POS では、このファイルを使用して、拡張機能を追加または除外します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="165">
          <source>By default, the list contains the whole excluded extensions list.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">既定では、リストに除外された拡張リスト全体が含まれています。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="166">
          <source>To include an extension as part of the POS, you must add the name of the extension folder and comment out the extension in the extension list, as shown here.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">拡張機能を POS の一部として含めるには、次に示すように、拡張フォルダーの名前を追加し、拡張リストの拡張をコメントアウトします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="167">
          <source>Compile and rebuild the project.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">プロジェクトをコンパイル、およびリビルドします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="168">
          <source>Add a custom operation button to the POS layout in Retail headquarters</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">小売用バックオフィス内の POS レイアウトにカスタム操作ボタンを追加します</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="169">
          <source>In Retail go to <bpt id="p1">**</bpt>Retail and commerce <ph id="ph1">&amp;gt;</ph> Channel setup <ph id="ph2">&amp;gt;</ph> POS setup <ph id="ph3">&amp;gt;</ph> POS <ph id="ph4">&amp;gt;</ph> Operations<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Retail で<bpt id="p1">**</bpt>小売りとコマース <ph id="ph1">&amp;gt;</ph> チャンネル設定 <ph id="ph2">&amp;gt;</ph> POS 設定 <ph id="ph3">&amp;gt;</ph> POS <ph id="ph4">&amp;gt;</ph> 工程<ept id="p1">**</ept>の順に移動します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="170">
          <source>Create an operation that is named <bpt id="p1">**</bpt>EOD<ept id="p1">**</ept> and that has an operation ID of <bpt id="p2">**</bpt>5001<ept id="p2">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>EOD<ept id="p1">**</ept> という工程を作成して、<bpt id="p2">**</bpt>5001<ept id="p2">**</ept> の工程 ID をもつようにします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="171">
          <source>Go to <bpt id="p1">**</bpt>Retail and commerce <ph id="ph1">&amp;gt;</ph> Channel setup <ph id="ph2">&amp;gt;</ph> POS setup <ph id="ph3">&amp;gt;</ph> POS <ph id="ph4">&amp;gt;</ph> Button grids<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>小売とコマース <ph id="ph1">&amp;gt;</ph> チャネル設定 <ph id="ph2">&amp;gt;</ph> POS 設定 <ph id="ph3">&amp;gt;</ph> POS <ph id="ph4">&amp;gt;</ph> ボタン グリッド<ept id="p1">**</ept>の順に移動します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="172">
          <source>Filter for <bpt id="p1">**</bpt>'F2W2'<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>'F2W2'<ept id="p1">**</ept> コードのフィルターです。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="173">
          <source>Select the <bpt id="p1">**</bpt>Designer<ept id="p1">**</ept> button, and then follow the instructions to install the designer.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>デザイナー<ept id="p1">**</ept>ボタンを選択し、次の手順にしたがってデザイナーをインストールします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="174">
          <source>If you're prompted for credentials, enter the Retail user name and password.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">資格情報を求めるメッセージが表示されたら、Retail のユーザー名とパスワードを入力します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="175">
          <source>Right-click in the designer area, and then select <bpt id="p1">**</bpt>Add new row<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">デザイナ領域で右クリックし、<bpt id="p1">**</bpt>新しい行の追加<ept id="p1">**</ept>を選択します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="176">
          <source>Right-click the new button, and then select <bpt id="p1">**</bpt>Button properties<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">新しいボタンを右クリックし、<bpt id="p1">**</bpt>ボタン プロパティ<ept id="p1">**</ept> を選択します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="177">
          <source>Set the <bpt id="p1">**</bpt>Action<ept id="p1">**</ept> property to <bpt id="p2">**</bpt>EOD<ept id="p2">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p2">**</bpt>EOD<ept id="p2">**</ept> に <bpt id="p1">**</bpt>アクション<ept id="p1">**</ept>プロパティを設定します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="178">
          <source>Then select <bpt id="p1">**</bpt>OK<ept id="p1">**</ept>, and close the designer.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>OK<ept id="p1">**</ept> を選択し、デザイナーを閉じます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="179">
          <source>Go to <bpt id="p1">**</bpt>Retail and commerce<ept id="p1">**</ept> <ph id="ph1">&amp;gt;</ph> <bpt id="p2">**</bpt>Retail IT<ept id="p2">**</ept> <ph id="ph2">&amp;gt;</ph> <bpt id="p3">**</bpt>Distribution schedule<ept id="p3">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>小売りとコマース<ept id="p1">**</ept> <ph id="ph1">&amp;gt;</ph> <bpt id="p2">**</bpt>小売 IT<ept id="p2">**</ept> <ph id="ph2">&amp;gt;</ph> <bpt id="p3">**</bpt>配送スケジュール<ept id="p3">**</ept> の順に移動します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="180">
          <source>Select <bpt id="p1">**</bpt>1090<ept id="p1">**</ept>, and then select <bpt id="p2">**</bpt>Run now<ept id="p2">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>1090<ept id="p1">**</ept> を選択してから、<bpt id="p2">**</bpt>今すぐ実行<ept id="p2">**</ept>を選択します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="181">
          <source>The preceding steps assume that you're using demo data.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">上記の手順では、デモ データを使用していることを前提としています。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="182">
          <source>If you aren't using demo data, create and add the button according to your custom configurations.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">デモ データを使用していない場合は、カスタム構成に従ってボタンを作成して追加します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="183">
          <source>Validate your extension</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">拡張機能の検証</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="184">
          <source>Press F5, and deploy the POS to test your customization.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">F5 キーを押し、POS を展開してカスタマイズをテストします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="185">
          <source>On the transaction screen, select the new <bpt id="p1">**</bpt>EOD<ept id="p1">**</ept> operation button, and follow the steps.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">トランザクション画面で、新しい <bpt id="p1">**</bpt>EOD<ept id="p1">**</ept> 操作ボタンを選択し、手順を実行します。</target></trans-unit>
      </group>
    </body>
  </file>
</xliff>