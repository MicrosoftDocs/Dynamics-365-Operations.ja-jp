<?xml version="1.0" encoding="UTF-8"?>
<xliff xmlns:logoport="urn:logoport:xliffeditor:xliff-extras:1.0" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns="urn:oasis:names:tc:xliff:document:1.2" xmlns:xliffext="urn:microsoft:content:schema:xliffextensions" version="1.2" xsi:schemaLocation="urn:oasis:names:tc:xliff:document:1.2 xliff-core-1.2-transitional.xsd">
  <file datatype="xml" source-language="en-US" original="respond-event-handler-result.md" target-language="ja-JP">
    <header>
      <tool tool-company="Microsoft" tool-version="1.0-7889195" tool-name="mdxliff" tool-id="mdxliff"/>
      <xliffext:skl_file_name>respond-event-handler-result.cc1187.0c42e9dd6c4f6e583887713f267eaa579f90f8f6.skl</xliffext:skl_file_name>
      <xliffext:version>1.2</xliffext:version>
      <xliffext:ms.openlocfilehash>0c42e9dd6c4f6e583887713f267eaa579f90f8f6</xliffext:ms.openlocfilehash>
      <xliffext:ms.sourcegitcommit>9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b</xliffext:ms.sourcegitcommit>
      <xliffext:ms.lasthandoff>05/15/2019</xliffext:ms.lasthandoff>
      <xliffext:ms.openlocfilepath>articles\dev-itpro\extensibility\respond-event-handler-result.md</xliffext:ms.openlocfilepath>
    </header>
    <body>
      <group extype="content" id="content">
        <trans-unit xml:space="preserve" translate="yes" id="101" restype="x-metadata">
          <source>Respond by using EventHandlerResult</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">EventHandlerResult を使用して応答</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="102" restype="x-metadata">
          <source>This topic describes how to subscribe to events that has a parameter of any type that implements the IEventHandlerResult interface.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このトピックでは、IEventHandlerResult インターフェイスを実装する任意の型パラメーターを持つイベントをサブスクライブする方法について説明します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="103">
          <source>Respond by using EventHandlerResult</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">EventHandlerResult を使用して応答</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="104">
          <source>Some delegate methods are implemented so that they can request a response from subscribing delegate handler methods.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">いくつかのデリゲート メソッドは、デリゲート ハンドラー メソッドのサブスクライブから応答を要求できるように実装されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="105">
          <source>The delegate calling logic then uses the response from a potential subscriber when it continues execution after the response has been received.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">デリゲート呼び出しロジックは、応答の受信後に実行を継続するときに潜在的なサブスクライバからの応答を使用します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="106">
          <source>These delegate methods usually have a signature that has an <bpt id="p1">**</bpt>EventHandlerResult<ept id="p1">**</ept> parameter as the last parameter.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">これらのデリゲート メソッドは通常、<bpt id="p1">**</bpt>EventHandlerResult<ept id="p1">**</ept> パラメーターを最後のパラメーターとして持つシグネチャを持っています。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="107">
          <source>However, because of the support for the <bpt id="p1">**</bpt>EventHandlerAcceptResult<ept id="p1">**</ept> and <bpt id="p2">**</bpt>EventHandlerRejectResult<ept id="p2">**</ept> types, the parameter can be of any type that implements the <bpt id="p3">**</bpt>IEventHandlerResult<ept id="p3">**</ept> interface.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ただし、<bpt id="p1">**</bpt>EventHandlerAcceptResult<ept id="p1">**</ept> および <bpt id="p2">**</bpt>EventHandlerRejectResult<ept id="p2">**</ept> タイプのサポートが原因で、パラメーターは <bpt id="p3">**</bpt>IEventHandlerResult<ept id="p3">**</ept> インターフェイスを実装する任意のタイプになります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="108">
          <source>In general, the logic that is implemented in the delegate handler method should contain a condition that verifies that the subscribing logic is responsible for providing a response.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">一般に、デリゲート ハンドラー メソッドに実装されているロジックには、サブスクライブしているロジックが応答の提供を担当していることを検証する条件を含める必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="109">
          <source>It should also include logic to provide the response in the form of a result.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">結果のフォームに応答を提供するロジックも含める必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="110">
          <source>When the delegate handler method must provide the response to an <bpt id="p1">**</bpt>EventHandlerResult<ept id="p1">**</ept> object parameter, the subscribing logic might also contain logic to calculate or retrieve the result.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">デリゲート ハンドラー メソッドが <bpt id="p1">**</bpt>EventHandlerResult<ept id="p1">**</ept> オブジェクト パラメーターへの応答を提供する必要があるとき、サブスクライブするロジックには結果の計算または取得のためのロジックも含まれている場合があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="111">
          <source>When the condition and the response logic are implemented, the calculation of the result must occur only when the condition is evaluated to <bpt id="p1">**</bpt>true<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">条件と応答ロジックが実装されると、条件が <bpt id="p1">**</bpt>true<ept id="p1">**</ept> と評価されたときのみ、結果の計算を実行する必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="112">
          <source>All the subscribing delegate handler methods are run when a delegate is called.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">すべてのサブスクライブしているデリゲート ハンドラー メソッドはデリゲートが呼び出されたときに実行されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="113">
          <source>Therefore, you should make sure that the overhead of running your method is as low as possible when the method isn't responsible for providing a response.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">したがって、メソッドがレスポンスの提供を担当していない場合は、メソッドを実行する間接費ができるだけ低いことを確認する必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="114">
          <source>Therefore, make sure that the condition is evaluated to <bpt id="p1">**</bpt>false<ept id="p1">**</ept> as quickly as possible when your delegate handler method isn't responsible for providing a result.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">したがって、デリゲート ハンドラー メソッドが結果を提供する責任を負わない場合、できるだけ早く条件が <bpt id="p1">**</bpt>false<ept id="p1">**</ept> に評価されていることを確認してください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="115">
          <source>Examples</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">例</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="116">
          <source>The following example shows a delegate handler that has a condition in the form of a <bpt id="p1">**</bpt>switch<ept id="p1">**</ept> statement.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">次の例は、<bpt id="p1">**</bpt>switch<ept id="p1">**</ept> ステートメントの形式の条件を持つデリゲート ハンドラーを示しています。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="117">
          <source>The delegate handler also has logic to provide a response in the form of the result.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">デリゲート ハンドラーには結果のフォームに応答を提供するロジックがあります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="118">
          <source>The responding logic is run only when the condition is evaluated to <bpt id="p1">**</bpt>true<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">応答するロジックは、条件が <bpt id="p1">**</bpt>true<ept id="p1">**</ept> に評価された場合にのみ実行されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="119">
          <source>When the delegate method requests a response by using an <bpt id="p1">**</bpt>EventHandlerAcceptResult<ept id="p1">**</ept> or an <bpt id="p2">**</bpt>EventHandlerRejectResult<ept id="p2">**</ept> object parameter, the subscriber is expected to respond only with an accept or a reject.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">デリゲート メソッドが、<bpt id="p1">**</bpt>EventHandlerAcceptResult<ept id="p1">**</ept> または <bpt id="p2">**</bpt>EventHandlerRejectResult<ept id="p2">**</ept> オブジェクト パラメーターを使用して、応答を要求するとき、サブスクライバーは、承認または否認でのみ応答することを想定します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="120">
          <source>The subscribing logic might also add messages to the Infolog.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">サブスクライブ ロジックは、メッセージを Infolog に追加することもできます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="121">
          <source>The following example resembles the previous example.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">次の例は、前の例に似ています。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="122">
          <source>However, the delegate method now requests a response by using an <bpt id="p1">**</bpt>EventHandlerAcceptResult<ept id="p1">**</ept> object and by calling the <bpt id="p2">**</bpt>accept<ept id="p2">**</ept> method.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ただし、デリゲート メソッドは、<bpt id="p1">**</bpt>EventHandlerAcceptResult<ept id="p1">**</ept> オブジェクトの使用によりおよび<bpt id="p2">**</bpt>受け入れ<ept id="p2">**</ept>メソッドを呼び出すことにより、応答を要求するようになります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="123">
          <source>The following example shows a delegate handler method that responds by using an <bpt id="p1">**</bpt>EventHandlerRejectResult<ept id="p1">**</ept> object.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">次の例では、<bpt id="p1">**</bpt>EventHandlerRejectResult<ept id="p1">**</ept> オブジェクトを使用して応答するデリゲート ハンドラー メソッドを示しています。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="124">
          <source>To respond by using an <bpt id="p1">**</bpt>EventHandlerRejectResult<ept id="p1">**</ept> object, you can call the <bpt id="p2">**</bpt>reject<ept id="p2">**</ept> method or the <bpt id="p3">**</bpt>checkFailed<ept id="p3">**</ept> extension method.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>EventHandlerRejectResult<ept id="p1">**</ept> オブジェクトを使用して応答するには、<bpt id="p2">**</bpt>reject<ept id="p2">**</ept> メソッドまたは <bpt id="p3">**</bpt>checkFailed<ept id="p3">**</ept> 拡張メソッドを呼び出します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="125">
          <source>If you use the <bpt id="p1">**</bpt>checkFailed<ept id="p1">**</ept> method, you can add a warning message to the Infolog.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>checkFailed<ept id="p1">**</ept> メソッドを使用する場合は、情報ログに警告メッセージを追加できます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="126">
          <source>Internally, the <bpt id="p1">**</bpt>checkFailed<ept id="p1">**</ept> method calls the <bpt id="p2">**</bpt>reject<ept id="p2">**</ept> method.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">内部的には、<bpt id="p1">**</bpt>checkFailed<ept id="p1">**</ept> メソッドは <bpt id="p2">**</bpt>reject<ept id="p2">**</ept> メソッドを呼び出します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="127">
          <source>Guidelines</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ガイドライン</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="128">
          <source>In addition to the previously described practices, the following general guidelines apply:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">前述の実例に加えて、次の一般的なガイドラインが適用されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="129">
          <source>Respond only when the subscribing logic is responsible for responding.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">サブスクライブしているロジックが応答を担当する場合にのみ対応します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="130">
          <source>The delegate handler methods were implemented to provide a response when a specific condition is met.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">デリゲート ハンドラー メソッドは、特定の条件が満たされたときに応答を提供するために実装されました。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="131">
          <source>Therefore, the subscribing logic must provide a result when a specific condition is met.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">したがって、サブスクライブしているロジックは、特定の条件が満たされた場合に結果を提供する必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="132">
          <source>Before the subscribing logic responds, it should not evaluate whether the result object parameter already contains a result.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">サブスクライブしているロジックが応答する前に、結果オブジェクト パラメーターは既に結果が含まれているかどうかを評価することができません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="133">
          <source>For example, a delegate handler method should not contain logic that resembles the logic in the following example.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">たとえば、デリゲート ハンドラー メソッドは、次の例にあるロジックに似たロジックを含めないようにする必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="134">
          <source>This logic evaluates whether the <bpt id="p1">**</bpt>EventHandlerResult<ept id="p1">**</ept> object parameter already contains a result when the method is run.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このロジックは、メソッド実行時に <bpt id="p1">**</bpt>EventHandlerResult<ept id="p1">**</ept> オブジェクト パラメーターに結果がすでに含まれているかどうかを評価します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="135">
          <source>This example is an example of code that you should <bpt id="p1">**</bpt>not<ept id="p1">**</ept> write.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この例は、書くべきでは<bpt id="p1">**</bpt>ない<ept id="p1">**</ept>コードの例です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="136">
          <source>Don't provide a response on behalf of other subscribers.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">他のサブスクライバーの代理として応答を提供しないでください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="137">
          <source>If the delegate handler method isn't responsible for providing a response, the method must not provide a response.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">デリゲート ハンドラー メソッドが応答を提供する責任を負わない場合、メソッドは応答を提供できません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="138">
          <source>If the method provides a response when the condition isn't met, it provides a response on behalf of other subscribers.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">条件が満たされていないときに、メソッドが応答を提供する場合は、他のサブスクライバーに代わって応答を提供しています。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="139">
          <source>The requesting logic must be responsible for handling situations where no subscribers have responded.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">要求元のロジックは、サブスクライバーが応答していない状況を処理する責任を負わなければなりません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="140">
          <source>The delegate handler method must not contain logic that resembles the logic in the following example.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">デリゲート ハンドラー メソッドは、次の例にあるロジックに似たロジックを含めないようにする必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="141">
          <source>This logic which provides a result when the condition is evaluated to <bpt id="p1">**</bpt>false<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このロジックは、条件が <bpt id="p1">**</bpt>false<ept id="p1">**</ept> と評価されたときに結果を提供します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="142">
          <source>This example is an example of code that you should <bpt id="p1">**</bpt>not<ept id="p1">**</ept> write.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この例は、書くべきでは<bpt id="p1">**</bpt>ない<ept id="p1">**</ept>コードの例です。</target></trans-unit>
      </group>
    </body>
  </file>
</xliff>