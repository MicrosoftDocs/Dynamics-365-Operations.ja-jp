<?xml version="1.0" encoding="UTF-8"?>
<xliff xmlns:logoport="urn:logoport:xliffeditor:xliff-extras:1.0" xmlns:tilt="urn:logoport:xliffeditor:tilt-non-translatables:1.0" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns="urn:oasis:names:tc:xliff:document:1.2" xmlns:xliffext="urn:microsoft:content:schema:xliffextensions" version="1.2" xsi:schemaLocation="urn:oasis:names:tc:xliff:document:1.2 xliff-core-1.2-transitional.xsd">
  <file datatype="xml" source-language="en-US" original="modern-pos-trigger-extensibility.md" target-language="ja-JP">
    <header>
      <tool tool-company="Microsoft" tool-version="1.0-7889195" tool-name="mdxliff" tool-id="mdxliff"/>
      <xliffext:skl_file_name>modern-pos-trigger-extensibility.a7078d.779376807af5294ddcd996934582d03ff57c0e7b.skl</xliffext:skl_file_name>
      <xliffext:version>1.2</xliffext:version>
      <xliffext:ms.openlocfilehash>779376807af5294ddcd996934582d03ff57c0e7b</xliffext:ms.openlocfilehash>
      <xliffext:ms.sourcegitcommit>9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b</xliffext:ms.sourcegitcommit>
      <xliffext:ms.lasthandoff>05/15/2019</xliffext:ms.lasthandoff>
      <xliffext:ms.openlocfilepath>articles\retail\dev-itpro\modern-pos-trigger-extensibility.md</xliffext:ms.openlocfilepath>
    </header>
    <body>
      <group extype="content" id="content">
        <trans-unit xml:space="preserve" translate="yes" id="101" restype="x-metadata">
          <source>Retail Modern POS (MPOS) and Cloud POS trigger extensibility</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Retail Modern POS (MPOS) およびクラウド POS のトリガー拡張機能</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="102" restype="x-metadata">
          <source>This topic explains the client-side trigger functionality in Modern POS and Cloud POS.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このトピックでは、Modern POS と Cloud POS のクライアント側のトリガー機能について説明します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="103">
          <source>Retail Modern POS (MPOS) and Cloud POS trigger extensibility</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Retail Modern POS (MPOS) およびクラウド POS のトリガー拡張機能</target></trans-unit>
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
          <source>This topic explains the client-side trigger functionality in Modern POS and Cloud POS.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このトピックでは、Modern POS と Cloud POS のクライアント側のトリガー機能について説明します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="108">
          <source>Trigger overview</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">トリガーの概要</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="109">
          <source>Triggers are events that are raised by Microsoft Dynamics 365 for Retail for Retail POS.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">トリガーは、Microsoft Dynamics 365 for Retailfor Retail POS によって発生するイベントです。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="110">
          <source>Triggers let you insert custom code before or after operations.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">トリガーを使用すると、操作の前後にカスタム コードを挿入できます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="111">
          <source>There are two kinds of triggers: pre-triggers and post-triggers.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">トリガーには事前トリガーと事後トリガーの 2 種類があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="112">
          <source>Pre-triggers</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">プレトリガー</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="113">
          <source>Post-triggers</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ポスト トリガー</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="114">
          <source>Pre-triggers can be used to insert custom code before an operation is run.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">操作を実行する前に、カスタム コードを挿入するためにプレトリガーを使用できます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="115">
          <source>For example, if a customer uses a coupon for a purchase, you can use a pre-trigger to insert custom code to validate that the coupon hasn't expired and hasn't previously been used.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">たとえば、顧客が購買のクーポンを使用する場合、有効期限が切れておらず、以前に使用されていないクーポンを検証するカスタム コードを挿入するための事前トリガーを使用できます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="116">
          <source>Post-triggers can be used to insert custom code that responds to a completed operation.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ポスト トリガーを使うと、完了した工程に応答するカスタム コードを挿入できます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="117">
          <source>For example, you can write code that runs after the <bpt id="p1">**</bpt>CustomerAdd<ept id="p1">**</ept> operation and prompts the cashier to wish the customer a happy birthday if it's the customer’s birthday.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">たとえば、<bpt id="p1">**</bpt>CustomerAdd<ept id="p1">**</ept> 操作後に実行し、顧客の誕生日である場合は、レジ担当者が顧客の幸せな誕生日を祈るよう指示するコードを記述できます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="118">
          <source>Trigger types</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">トリガーのタイプ</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="119">
          <source>In Modern POS and Cloud POS, triggers are either cancelable or non-cancelable.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Modern POS およびクラウド POS では、トリガーはキャンセル可能かキャンセル可能ではないかのいずれかです。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="120">
          <source>Cancelable</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">解約可能</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="121">
          <source>Non-cancelable</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">キャンセル不可</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="122">
          <source>Trigger implementations that extend <bpt id="p1">**</bpt>ICancelableTriggerCancelable<ept id="p1">**</ept> triggers can succeed, fail, or be canceled.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>ICancelableTriggerCancelable<ept id="p1">**</ept> トリガーを拡張するトリガー実装は、成功、失敗、または取り消しが可能です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="123">
          <source>Execution of the workflow is canceled without displaying an error.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ワークフローの実行は、エラーを表示せずにキャンセルされます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="124">
          <source>An example is a trigger to confirm that the user wants to use his or her loyalty points for tender.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">たとえば、ユーザーが支払/入金のためにロイヤルティ ポイントを使用することを確認するトリガーです。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="125">
          <source>If the user selects <bpt id="p1">**</bpt>No<ept id="p1">**</ept>, the workflow to enter loyalty information is canceled without showing an error message to the user.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ユーザーが<bpt id="p1">**</bpt>いいえ<ept id="p1">**</ept>と選択した場合、ユーザーにエラー メッセージが表示されずに、ロイヤルティ情報を入力するワークフローがキャンセルされます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="126">
          <source>Trigger implementations that extend <bpt id="p1">**</bpt>ITriggerNon-cancelable<ept id="p1">**</ept> triggers can either succeed or fail.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>ITriggerNon-cancelable<ept id="p1">**</ept> トリガーを拡張するトリガー実装は、成功または失敗のいずれかが可能です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="127">
          <source>If the trigger succeeds, the workflow continues.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">トリガーが成功した場合、ワークフローを続行します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="128">
          <source>If the trigger fails, a message appears in the UI.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">トリガーが失敗すると、UI にメッセージが表示されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="129">
          <source>An example is a trigger to support Swedish localization requirements by guiding the cashier to create separate transactions for sales and returns.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">たとえば、販売および返品のために個別のトランザクションを作成するレジ担当者に対してガイドライン指示をすることによりスウェーデン語のローカライズ要件をサポートするトリガーです。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="130">
          <source>Guidelines</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ガイドライン</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="131">
          <source><bpt id="p1">**</bpt>Trigger registration<ept id="p1">**</ept> – All triggers should be registered by using the <bpt id="p2">**</bpt>TriggerManager::register<ept id="p2">**</ept> method.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>トリガーの登録<ept id="p1">**</ept> – すべてのトリガーは、<bpt id="p2">**</bpt>TriggerManager::register<ept id="p2">**</ept> メソッドを使用して登録する必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="132">
          <source>The <bpt id="p1">**</bpt>ApplicationStart<ept id="p1">**</ept>, <bpt id="p2">**</bpt>PreLogOn<ept id="p2">**</ept>, and <bpt id="p3">**</bpt>PostLogOn<ept id="p3">**</ept> triggers must be registered inside a function that is called when the <bpt id="p4">**</bpt>DOMContentLoaded<ept id="p4">**</ept> event is raised.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>ApplicationStart<ept id="p1">**</ept>、<bpt id="p2">**</bpt>PreLogOn<ept id="p2">**</ept>、および <bpt id="p3">**</bpt>PostLogOn<ept id="p3">**</ept> トリガーは、<bpt id="p4">**</bpt>DOMContentLoaded<ept id="p4">**</ept> イベントが発生したときに呼び出される関数内で登録する必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="133">
          <source>Other triggers can be registered in the same manner, but they can also be registered conditionally.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">他のトリガーは、同じ方法で登録することができますが、条件付きで登録することもできます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="134">
          <source><bpt id="p1">**</bpt>Conditional registration<ept id="p1">**</ept> – If the decision about whether to register a trigger is based on information in the channel, the trigger can be registered conditionally.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>条件付き登録<ept id="p1">**</ept> - トリガーを登録するかどうかの決定がチャネル内の情報に基づいている場合、条件付きでトリガーを登録できます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="135">
          <source>Conditional registration should be performed inside a <bpt id="p1">**</bpt>PostLogOn<ept id="p1">**</ept> trigger.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">条件付きの登録を <bpt id="p1">**</bpt>PostLogOn<ept id="p1">**</ept> トリガー内で実行する必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="136">
          <source><bpt id="p1">**</bpt>Note:<ept id="p1">**</ept> It's important that the conditional registration be performed only during the first sign-in after the app has been loaded.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>注記:<ept id="p1">**</ept> 条件付きの登録は、アプリケーションの読み込み後最初のサインイン時にのみ実行することが重要です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="137">
          <source>For an example implementation, see the sample code later in this article.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">実装例については、この記事の後半のサンプル コードを参照してください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="138">
          <source><bpt id="p1">**</bpt>Trigger implementation<ept id="p1">**</ept> – Each trigger event that is listed in the "Supported trigger events" section has a trigger interface that is associated with it.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>トリガーの実装<ept id="p1">**</ept> – 「サポートされているトリガー イベント」セクションに一覧表示されている各トリガー イベントには、関連付けられているトリガー インターフェイスがあります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="139">
          <source>These trigger interfaces define the contract between the application and the trigger implementations.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">これらのトリガー インターフェイスは、アプリケーションとトリガー実装との間の契約を定義します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="140">
          <source>Each trigger should implement the predefined interface that is associated with the trigger event type that it's registered for.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">各トリガーは、登録されているトリガー イベント タイプに関連付けられている定義済みインターフェースを実装する必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="141">
          <source>Triggers execution workflow</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">トリガー実行ワークフロー</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="142">
          <source>The following diagram shows the execution workflow for both pre-triggers and post-triggers for the <bpt id="p1">**</bpt>ItemSaleOperation<ept id="p1">**</ept> workflow/operation.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">次の図は、<bpt id="p1">**</bpt>ItemSaleOperation<ept id="p1">**</ept> ワークフロー/操作のプリトリガーとポストトリガーの実行ワークフローを示しています。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="143">
          <source><bpt id="p1">[</bpt><ph id="ph1">![</ph>Trigger Execution Flow<ept id="p1">](./media/trigger-execution-flow.png)](./media/trigger-execution-flow.png)</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">[</bpt><ph id="ph1">![</ph>トリガー実行フロー<ept id="p1">](./media/trigger-execution-flow.png)](./media/trigger-execution-flow.png)</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="144">
          <source>Supported trigger events</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">サポートされているトリガー イベント</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="145">
          <source>Together with pre-operation and post-operation triggers that are triggered for every operation, the following triggers are supported out of the box:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">すべての操作でトリガーされる操作前後のトリガーとともに、次のトリガーがそのまま使用できます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="146">
          <source>Application triggers</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">アプリケーション トリガー</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="147">
          <source>Cancelable</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">解約可能</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="148">
          <source><bpt id="p1">**</bpt>PreLogOn<ept id="p1">**</ept> – Called before sign-in to Modern POS</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>PreLogOn<ept id="p1">**</ept> – Modern POS にサインインする前に呼び出されます</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="149">
          <source>operatorId</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">operatorId</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="150">
          <source>Non-cancelable</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">キャンセル不可</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="151">
          <source><bpt id="p1">**</bpt>ApplicationStart<ept id="p1">**</ept> – Called when the application is launched</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>ApplicationStart<ept id="p1">**</ept> - アプリケーションの起動時に呼び出される</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="152">
          <source><bpt id="p1">**</bpt>ApplicationSuspend<ept id="p1">**</ept> – Called when the application is suspended</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>ApplicationSuspend<ept id="p1">**</ept> - アプリケーションが中断されたときに呼び出される</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="153">
          <source><bpt id="p1">**</bpt>PostLogOff<ept id="p1">**</ept> – Called after the sign-out operation is completed</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>PostLogOff<ept id="p1">**</ept> – サインアウトの操作が完了した後に呼び出されます</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="154">
          <source><bpt id="p1">**</bpt>PostLogOn<ept id="p1">**</ept> – Called after the sign-in operation is completed</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>PostLogOn<ept id="p1">**</ept> – サインインの操作が完了した後に呼び出されます</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="155">
          <source>Cash management triggers</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">現金管理トリガー</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="156">
          <source>Cancelable</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">解約可能</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="157">
          <source><bpt id="p1">**</bpt>PreTenderDeclaration<ept id="p1">**</ept> – Called before the tender declaration operation is run</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>PreTenderDeclaration<ept id="p1">**</ept> – 支払/入金申告操作が実行される前に呼び出されます</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="158">
          <source>Non-cancelable</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">キャンセル不可</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="159">
          <source><bpt id="p1">**</bpt>PostTenderDeclaration<ept id="p1">**</ept> – Called as the last step in the tender declaration workflow</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>PostTenderDeclaration<ept id="p1">**</ept> – 支払/入金申告ワークフローの最後のステップとして呼び出されます</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="160">
          <source>Customer triggers</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">顧客トリガー</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="161">
          <source>Cancelable</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">解約可能</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="162">
          <source><bpt id="p1">**</bpt>PreCustomerAdd<ept id="p1">**</ept> – Called before a new customer is created</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>PreCustomerAdd<ept id="p1">**</ept> – 新しい顧客が作成される前に呼び出されます</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="163">
          <source><bpt id="p1">**</bpt>PreCustomerClear<ept id="p1">**</ept> – Called before the customer is cleared from the current transaction</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>PreCustomerClear<ept id="p1">**</ept> – 顧客が現在のトランザクションから消去される前に呼び出されます</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="164">
          <source><bpt id="p1">**</bpt>PreCustomerSearch<ept id="p1">**</ept> – Called before a search for a customer</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>PreCustomerSearch<ept id="p1">**</ept> – 顧客の検索前に呼び出されます</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="165">
          <source><bpt id="p1">**</bpt>PreCustomerSet<ept id="p1">**</ept> – Called before the customer is set on the transaction</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>PreCustomerSet<ept id="p1">**</ept> – 顧客がトランザクションを開始する前に呼び出されます</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="166">
          <source>Non-cancelable</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">キャンセル不可</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="167">
          <source><bpt id="p1">**</bpt>PostCustomerAdd<ept id="p1">**</ept> – Called after a new customer is created</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>PostCustomerAdd<ept id="p1">**</ept> – 新しい顧客が作成された後に呼び出されます</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="168">
          <source><bpt id="p1">**</bpt>PostCustomerClear<ept id="p1">**</ept> – Called after the customer is cleared from the transaction</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>PostCustomerClear<ept id="p1">**</ept> – 顧客がトランザクションから消去された後に呼び出されます</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="169">
          <source><bpt id="p1">**</bpt>PostCustomerSearch<ept id="p1">**</ept> – Called after a search for a customer</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>PostCustomerSearch<ept id="p1">**</ept> – 顧客の検索後に呼び出されます</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="170">
          <source>Discount triggers</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">割引のトリガー</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="171">
          <source>Cancelable</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">解約可能</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="172">
          <source><bpt id="p1">**</bpt>PreLineDiscountAmount<ept id="p1">**</ept> – Called during the line discount amount operation, after validation determines whether a discount can be applied</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>PreLineDiscountAmount<ept id="p1">**</ept> – 検証によって割引が適用可能かどうかが判断された後、行割引金額操作中に呼び出されます</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="173">
          <source><bpt id="p1">**</bpt>PreLineDiscountPercent<ept id="p1">**</ept> – Called during the line discount percent operation, after validation determines whether a discount can be applied</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>PreLineDiscountPercent<ept id="p1">**</ept> – 検証によって割引が適用可能かどうかが判断された後、行割引率操作中に呼び出されます</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="174">
          <source><bpt id="p1">**</bpt>PreTotalDiscountAmount<ept id="p1">**</ept> – Called during the total discount amount operation, after validation determines whether a discount can be applied</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>PreTotalDiscountAmount<ept id="p1">**</ept> – 検証によって割引が適用可能かどうかが判断された後、合計割引金額操作中に呼び出されます</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="175">
          <source><bpt id="p1">**</bpt>PreTotalDiscountPercent<ept id="p1">**</ept> – Called during the total discount percent operation, after validation determines whether a discount can be applied</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>PreTotalDiscountPercent<ept id="p1">**</ept> – 検証によって割引が適用可能かどうかが判断された後、割引金額率操作中に呼び出されます</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="176">
          <source>Non-cancelable</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">キャンセル不可</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="177">
          <source><bpt id="p1">**</bpt>PostLineDiscountAmount<ept id="p1">**</ept> - Called as the last step in the line discount amount workflow</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>PostLineDiscountAmount<ept id="p1">**</ept> - 行割引金額のワークフローの最後のステップとして呼び出されます</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="178">
          <source><bpt id="p1">**</bpt>PostLineDiscountPercent<ept id="p1">**</ept> – Called as the last step in the line discount percent workflow</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>PostLineDiscountPercent<ept id="p1">**</ept> – 行割引率のワークフローの最後のステップとして呼び出されます</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="179">
          <source><bpt id="p1">**</bpt>PostTotalDiscountAmount<ept id="p1">**</ept> – Called as the last step in the total discount amount workflow</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>PostTotalDiscountAmount<ept id="p1">**</ept> – 合計割引金額のワークフローの最後のステップとして呼び出されます</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="180">
          <source><bpt id="p1">**</bpt>PostTotalDiscountPercent<ept id="p1">**</ept> – Called as the last step in the total discount percent workflow</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>PostTotalDiscountPercent<ept id="p1">**</ept> – 合計割引率のワークフローの最後のステップとして呼び出されます</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="181">
          <source>Operation triggers</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">工程のトリガー</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="182">
          <source>Cancelable</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">解約可能</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="183">
          <source><bpt id="p1">**</bpt>PreOperation<ept id="p1">**</ept> – Called before every operation is run, before the prehandler and operation validators</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>PreOperation<ept id="p1">**</ept> – 毎回の操作を実行する前、プリハンドラーおよび操作検証の前に呼び出されます</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="184">
          <source>Non-cancelable</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">キャンセル不可</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="185">
          <source><bpt id="p1">**</bpt>OperationFailure<ept id="p1">**</ept> – Called when an operation fails, and can be used to perform recovery actions</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>OperationFailure<ept id="p1">**</ept> – 操作が失敗したときに呼び出され、復旧アクションを実行するために使用できます</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="186">
          <source><bpt id="p1">**</bpt>PostOperation<ept id="p1">**</ept> – Called when an operation is completed successfully</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>PostOperation<ept id="p1">**</ept> – 操作が正常に終了したときに呼び出されます</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="187">
          <source>Payment triggers</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">支払トリガー</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="188">
          <source>Cancelable</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">解約可能</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="189">
          <source><bpt id="p1">**</bpt>PreAddTenderLine<ept id="p1">**</ept> – Called before a tender line is added to the transaction</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>PreAddTenderLine<ept id="p1">**</ept> – 支払/入金の明細行がトランザクションに追加される前に呼び出されます</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="190">
          <source><bpt id="p1">**</bpt>PrePayment<ept id="p1">**</ept> – Called before any payment operation is started</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>PrePayment<ept id="p1">**</ept> – 支払操作が開始される前に呼び出されます</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="191">
          <source><bpt id="p1">**</bpt>PreVoidPayment<ept id="p1">**</ept> – Called before the void payment operation is started</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>PreVoidPayment<ept id="p1">**</ept> – 支払の無効化操作が開始される前に呼び出されます</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="192">
          <source>Non-cancelable</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">キャンセル不可</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="193">
          <source><bpt id="p1">**</bpt>PostPayment<ept id="p1">**</ept> – Called after the payment has been added</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>PostPayment<ept id="p1">**</ept> – 支払が追加された後に呼び出されます</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="194">
          <source><bpt id="p1">**</bpt>PostVoidPayment<ept id="p1">**</ept> – Called after the payment has been voided</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>PostVoidPayment<ept id="p1">**</ept> – 支払が無効にされた後に呼び出されます</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="195">
          <source>Printing triggers</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">印刷トリガー</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="196">
          <source>Cancelable</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">解約可能</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="197">
          <source><bpt id="p1">**</bpt>PrePrintReceiptCopy<ept id="p1">**</ept> – Called before a copy of the receipt is printed</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>PrePrintReceiptCopy<ept id="p1">**</ept> – レシートのコピーが印刷される前に呼び出されます</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="198">
          <source>Product Triggers</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">製品トリガー</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="199">
          <source>Cancelable</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">解約可能</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="200">
          <source><bpt id="p1">**</bpt>PreClearQuantity<ept id="p1">**</ept> – Called before the clear quantity operation</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>PreClearQuantity<ept id="p1">**</ept> – 数量のクリア操作前に呼び出されます</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="201">
          <source><bpt id="p1">**</bpt>PrePriceOverride<ept id="p1">**</ept> – Called before the price override operation</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>PrePriceOverride<ept id="p1">**</ept> – 価格上書き操作前に呼び出されます</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="202">
          <source><bpt id="p1">**</bpt>PreProductSale<ept id="p1">**</ept> – Called before the item sale operation</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>PreProductSale<ept id="p1">**</ept> – 品目販売操作前に呼び出されます</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="203">
          <source><bpt id="p1">**</bpt>PreReturnProduct<ept id="p1">**</ept> – Called before the return product operation</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>PreReturnProduct<ept id="p1">**</ept> – 返品操作前に呼び出されます</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="204">
          <source><bpt id="p1">**</bpt>PreSetQuantity<ept id="p1">**</ept> – Called before the set quantity operation</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>PreSetQuantity<ept id="p1">**</ept> – 数量の設定操作前に呼び出されます</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="205">
          <source><bpt id="p1">**</bpt>PreVoidProducts<ept id="p1">**</ept> – Called after the user confirms that he or she wants to void the transaction, but before the transaction is voided</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>PreVoidProducts<ept id="p1">**</ept> – ユーザーがトランザクションを無効化することを確認した後、トランザクションが無効化される前に呼び出されます</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="206">
          <source>Non-cancelable</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">キャンセル不可</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="207">
          <source><bpt id="p1">**</bpt>PostClearQuantity<ept id="p1">**</ept> – Called after the clear quantity operation</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>PostClearQuantity<ept id="p1">**</ept> – 数量のクリア操作後に呼び出されます</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="208">
          <source><bpt id="p1">**</bpt>PostPriceOverride<ept id="p1">**</ept> – Called after the price override operation</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>PostPriceOverride<ept id="p1">**</ept> – 価格上書き操作後に呼び出されます</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="209">
          <source><bpt id="p1">**</bpt>PostProductSale<ept id="p1">**</ept> – Called after the item sale operation</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>PostProductSale<ept id="p1">**</ept> – 品目販売操作後に呼び出されます</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="210">
          <source><bpt id="p1">**</bpt>PostReturnProduct<ept id="p1">**</ept> – Called after the return product operation</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>PostReturnProduct<ept id="p1">**</ept> – 返品操作後に呼び出されます</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="211">
          <source><bpt id="p1">**</bpt>PostSetQuantity<ept id="p1">**</ept> – Called after the set quantity operation</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>PostSetQuantity<ept id="p1">**</ept> – 数量の設定操作後に呼び出されます</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="212">
          <source><bpt id="p1">**</bpt>PostVoidProducts<ept id="p1">**</ept> – Called after the void products operation</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>PostVoidProducts<ept id="p1">**</ept> – 製品の無効化操作後に呼び出される</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="213">
          <source>Transaction triggers</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">トランザクションのトリガー</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="214">
          <source>Cancelable</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">解約可能</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="215">
          <source><bpt id="p1">**</bpt>PreConfirmReturnTransaction<ept id="p1">**</ept> – Called after a search for a transaction to return, but before the cart lines appear as available for return</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>PreConfirmReturnTransaction<ept id="p1">**</ept> – 返品するトランザクションを検索した後に呼び出されますが、カート明細行が返品可能と表示される前に呼び出されます</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="216">
          <source><bpt id="p1">**</bpt>PreEndTransaction<ept id="p1">**</ept> – Called before a sales transaction is completed</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>PreEndTransaction<ept id="p1">**</ept> – 販売トランザクションが完了する前に呼び出されます</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="217">
          <source><bpt id="p1">**</bpt>PreRecallTransaction<ept id="p1">**</ept> – Called before a transaction is recalled</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>PreRecallTransaction<ept id="p1">**</ept> – トランザクションが取り消される前に呼び出されます</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="218">
          <source><bpt id="p1">**</bpt>PreReturnTransaction<ept id="p1">**</ept> – Called before a transaction is returned</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>PreReturnTransaction<ept id="p1">**</ept> – トランザクションが戻される前に呼び出されます</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="219">
          <source><bpt id="p1">**</bpt>PreSuspendTransaction<ept id="p1">**</ept> – Called before a transaction is suspended</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>PreSuspendTransaction<ept id="p1">**</ept> – トランザクションが中断される前に呼び出されます</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="220">
          <source><bpt id="p1">**</bpt>PreVoidTransaction<ept id="p1">**</ept> – Called before a transaction is voided</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>PreVoidTransaction<ept id="p1">**</ept> – トランザクションが無効化される前に呼び出されます</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="221">
          <source>Non-cancelable</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">キャンセル不可</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="222">
          <source><bpt id="p1">**</bpt>BeginTransaction<ept id="p1">**</ept> – Called before a cart is created and a transaction is started</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>BeginTransaction<ept id="p1">**</ept> - カートが作成され、トランザクションが開始される前に呼び出されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="223">
          <source><bpt id="p1">**</bpt>PostEndTransaction<ept id="p1">**</ept> – Called after a sales transaction is completed</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>PostEndTransaction<ept id="p1">**</ept> – 販売トランザクションが完了した後に呼び出されます</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="224">
          <source><bpt id="p1">**</bpt>PostRecallTransaction<ept id="p1">**</ept> – Called after a transaction is recalled</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>PostRecallTransaction<ept id="p1">**</ept> – トランザクションが取り消された後に呼び出されます</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="225">
          <source><bpt id="p1">**</bpt>PostReturnTransaction<ept id="p1">**</ept> – Called after items from a transaction are added to the cart for return</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>PostReturnTransaction<ept id="p1">**</ept> – 返品のためにトランザクションの品目がカートに追加された後に呼び出されます</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="226">
          <source><bpt id="p1">**</bpt>PostSuspendTransaction<ept id="p1">**</ept> – Called after suspending a transaction</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>PostSuspendTransaction<ept id="p1">**</ept> – トランザクションを中断した後に呼び出されます</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="227">
          <source><bpt id="p1">**</bpt>PostVoidTransaction<ept id="p1">**</ept> – Called after a transaction is voided</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>PostVoidTransaction<ept id="p1">**</ept> – トランザクションが無効化された後に呼び出されます</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="228">
          <source>Trigger example implementation</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">トリガー実装の例</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="229">
          <source>The best way to understand triggers is to look at a sample implementation scenario.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">トリガーを理解する最善の方法は、サンプルの実装シナリオを調べることです。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="230">
          <source>Modern POS/Cloud POS changes to support Swedish localization requirements by using POS triggers</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">POS トリガーを使用したスウェーデン ローカライズ要件をサポートするための Modern POS/クラウド POS の変更</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="231">
          <source>Transactions can't have both return and sale operations if a fiscal register is connected.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">会計帳簿が接続されている場合、取引は返品と販売の両方の操作を行うことができません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="232">
          <source>An <bpt id="p1">**</bpt>IPreProductSaleTrigger<ept id="p1">**</ept> trigger is implemented to detect this situation if it occurs and to show a message to prompt the cashier.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>IPreProductSaleTrigger<ept id="p1">**</ept> トリガーはこの状況が発生した場合にこれを検出するように実装されまたキャッシャーに確認するメッセージを表示します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="233">
          <source>This is a requirement in Sweden.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">これは、スウェーデンの要件です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="234">
          <source>Implement an <bpt id="p1">**</bpt>IPreProductSaleTrigger<ept id="p1">**</ept> trigger to detect the situation and show a message to prompt the cashier.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>IPreProductSaleTrigger<ept id="p1">**</ept> トリガーを実装して状況を検出し、レジ担当者に確認するメッセージを表示します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="235">
          <source>Write trigger business logic in the <bpt id="p1">**</bpt>Execute<ept id="p1">**</ept> method in the implementation class.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">実装クラス内の <bpt id="p1">**</bpt>実行<ept id="p1">**</ept> メソッドにトリガー ビジネス ロジックを記述します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="236">
          <source>Register the trigger as part of the <bpt id="p1">**</bpt>PostLogonTrigger<ept id="p1">**</ept> implementation on the <bpt id="p2">**</bpt>DOMContentLoad<ept id="p2">**</ept> event.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p2">**</bpt>DOMContentLoad<ept id="p2">**</ept> イベントで <bpt id="p1">**</bpt>PostLogonTrigger<ept id="p1">**</ept> 実装の一部としてトリガーを登録します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="237">
          <source><bpt id="p1">[</bpt><ph id="ph1">![</ph>Trigger01<ept id="p1">](./media/trigger01.png)](./media/trigger01.png)</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">[</bpt><ph id="ph1">![</ph>Trigger01<ept id="p1">](./media/trigger01.png)](./media/trigger01.png)</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="238">
          <source><bpt id="p1">**</bpt>Purpose:<ept id="p1">**</ept> To customize Modern POS/Cloud POS to implement the Swedish localization requirement that the same transaction not include both sale and return lines when a fiscal register is connected.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>目的:<ept id="p1">**</ept> 最新の POS / Cloud POS を、会計登録に接続されているときに、スウェーデン語のローカライズ要件を実装して同じトランザクションに売却と返品の両方の行が含まれないようにカスタマイズします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="239">
          <source>Open a Modern POS project, and add a new TypeScript (.ts) file to add the trigger implementation.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Modern POS プロジェクトを開き、トリガーの実装を追加するために新しい TypeScript (.ts) ファイルを追加します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="240">
          <source>We are creating a new TypeScript file for our customization to keep our customization separate from the product code and make upgrades easier to manage.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">弊社のカスタマイズを製品コードから切り離してアップグレードを管理しやすくするために、カスタマイズ用の新しい TypeScript ファイルを作成します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="241">
          <source>Start Microsoft Visual Studio 2015 as an administrator.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Microsoft Visual Studio 2015 を管理者として起動します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="242">
          <source>Open the Modern POS solution from the Retail SDK directory:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Modern POS ソリューションを、Retail SDK ディレクトリから開く:</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="243">
          <source>If you're using a cloud-hosted computer, the path is I:/RetailSDK.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">クラウド ホストしているコンピュータを使用している場合、パスは I:/RetailSDK になります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="244">
          <source>If you're using a locally downloaded machine, the path is C:<ph id="ph1">\\</ph>Microsoft Dynamics AX<ph id="ph2">\\</ph>70<ph id="ph3">\\</ph>Retail SDK.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ローカルにダウンロードしたマシンを使用している場合は、パスは C:<ph id="ph1">\\</ph>Microsoft Dynamics AX<ph id="ph2">\\</ph>70<ph id="ph3">\\</ph>Retail SDK です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="245">
          <source>In POS.Core<ph id="ph1">\\</ph>Triggers<ph id="ph2">\\</ph>, create a new TypeScript file that is named <bpt id="p1">**</bpt>TriggerSample.ts<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">POS.Core<ph id="ph1">\\</ph>Triggers<ph id="ph2">\\</ph> に、<bpt id="p1">**</bpt>TriggerSample.ts<ept id="p1">**</ept> という名前の新しい TypeScript ファイルを作成します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="246">
          <source><bpt id="p1">[</bpt><ph id="ph1">![</ph>Trigger02<ept id="p1">](./media/trigger02-1024x411.png)](./media/trigger02.png)</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">[</bpt><ph id="ph1">![</ph>Trigger02<ept id="p1">](./media/trigger02-1024x411.png)](./media/trigger02.png)</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="247">
          <source>Add the following code to the TriggerSample.ts file.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">TriggerSample.ts ファイルに次のコードを追加します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="248">
          <source>Inspect the TriggerSample.ts file to see the implementation of <bpt id="p1">**</bpt>IPreProductSaleTrigger<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">TriggerSample.ts ファイルを検査して <bpt id="p1">**</bpt>IPreProductSaleTrigger<ept id="p1">**</ept> の実装を確認します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="249">
          <source>Inspect the registration of <bpt id="p1">**</bpt>ValidateProductSalePreProductSaleTrigger<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>ValidateProductSalePreProductSaleTrigger<ept id="p1">**</ept> の登録を検査します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="250">
          <source>Inspect the <bpt id="p1">**</bpt>performRegistration<ept id="p1">**</ept> method where the trigger is registered.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">トリガーが登録されている <bpt id="p1">**</bpt>performRegistration<ept id="p1">**</ept> メソッドを検査します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="251">
          <source>Inspect the registration of <bpt id="p1">**</bpt>PostLogonTrigger<ept id="p1">**</ept> on the <bpt id="p2">**</bpt>DOMContentLoad<ept id="p2">**</ept> event.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p2">**</bpt>DOMContentLoad<ept id="p2">**</ept> イベントで <bpt id="p1">**</bpt>PostLogonTrigger<ept id="p1">**</ept> の登録を検査します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="252">
          <source>Compile and rebuild Modern POS to verify the implementation:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">実装を確認するため Modern POS をコンパイル、およびリビルドします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="253">
          <source>Go to <bpt id="p1">**</bpt>Show Journal<ept id="p1">**</ept>, and select a transaction to return.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>仕訳帳の表示<ept id="p1">**</ept>に移動し、返すトランザクションを選択します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="254">
          <source>If the transaction has multiple lines, return one line.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">トランザクションに複数の明細行がある場合は、1 つの行を返します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="255">
          <source>A return line should be added in the cart.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">返品明細行は、カートに追加する必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="256">
          <source>In the left navigation pane, use product search (the search icon) to search for the text "shirt."</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">左のナビゲーション ウィンドウで、製品検索 (検索アイコン) を使用して、「シャツ」のテキストを検索します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="257">
          <source>Select one of the shirt products, and then, on the app bar, click <bpt id="p1">**</bpt>Sell now<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">シャツ製品のいずれかを選択し、アプリケーション バーで、<bpt id="p1">**</bpt>今すぐ売る<ept id="p1">**</ept> をクリックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="258">
          <source>Observe that <bpt id="p1">**</bpt>IPreProductSaleTrigger<ept id="p1">**</ept> trigger is run.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>IPreProductSaleTrigger<ept id="p1">**</ept> トリガーを実行されていることを確認します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="259">
          <source>You should receive a message that states that you can't perform a sale and a return in same transaction.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">同じトランザクションの販売および返品が実行できないことを示すメッセージが表示されるはずです。</target></trans-unit>
      </group>
    </body>
  </file>
</xliff>