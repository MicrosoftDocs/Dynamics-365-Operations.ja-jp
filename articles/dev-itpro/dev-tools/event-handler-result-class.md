<?xml version="1.0" encoding="UTF-8"?>
<xliff xmlns:logoport="urn:logoport:xliffeditor:xliff-extras:1.0" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns="urn:oasis:names:tc:xliff:document:1.2" xmlns:xliffext="urn:microsoft:content:schema:xliffextensions" version="1.2" xsi:schemaLocation="urn:oasis:names:tc:xliff:document:1.2 xliff-core-1.2-transitional.xsd">
  <file datatype="xml" source-language="en-US" original="event-handler-result-class.md" target-language="ja-JP">
    <header>
      <tool tool-company="Microsoft" tool-version="1.0-7889195" tool-name="mdxliff" tool-id="mdxliff"/>
      <xliffext:skl_file_name>event-handler-result-class.1d8b82.808601cf8736434d37306d48a389af1178238d4b.skl</xliffext:skl_file_name>
      <xliffext:version>1.2</xliffext:version>
      <xliffext:ms.openlocfilehash>808601cf8736434d37306d48a389af1178238d4b</xliffext:ms.openlocfilehash>
      <xliffext:ms.sourcegitcommit>9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b</xliffext:ms.sourcegitcommit>
      <xliffext:ms.lasthandoff>05/15/2019</xliffext:ms.lasthandoff>
      <xliffext:ms.openlocfilepath>articles\dev-itpro\dev-tools\event-handler-result-class.md</xliffext:ms.openlocfilepath>
    </header>
    <body>
      <group extype="content" id="content">
        <trans-unit xml:space="preserve" translate="yes" id="101" restype="x-metadata">
          <source>EventHandlerResult classes in request or response scenarios</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">要求または応答シナリオの EventHandlerResult クラス</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="102" restype="x-metadata">
          <source>This topic describes how to use EventHandlerResult classes with delegate methods.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このトピックでは、デリゲート メソッドで EventHandlerResult クラスを使用する方法について説明します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="103">
          <source>EventHandlerResult classes in request or response scenarios</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">要求または応答シナリオの EventHandlerResult クラス</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="104">
          <source>Delegate methods and delegate handler methods can be declared to support a request/response scenario, where the delegate calling logic requests the subscribers to provide a response.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">デリゲート メソッドとデリゲート ハンドラー メソッドは、デリゲート呼び出しロジックがサブスクライバに応答を要求する要求/応答シナリオをサポートするために宣言することができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="105">
          <source>To support this scenario the <bpt id="p1">**</bpt>EventHandlerResult<ept id="p1">**</ept> class is most often passed as a parameter, and the delegate handler methods provide their result using one of the result methods on the class.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このシナリオをサポートするために、<bpt id="p1">**</bpt>EventHandlerResult<ept id="p1">**</ept> クラスがパラメーターとして渡されることが最も多く、デリゲート ハンドラー メソッドがクラスの result メソッドの 1 つを使用して結果を提供します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="106">
          <source>However, the <bpt id="p1">**</bpt>EventHandlerResult<ept id="p1">**</ept> class can only contain a single result, so if multiple subscribers provide their individual result, the last respondent wins, and the results from the previous subscribers are overwritten.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ただし、<bpt id="p1">**</bpt>EventHandlerResult<ept id="p1">**</ept> クラスは単一の結果のみを含むため、複数のサブスクライバが個々の結果を提供する場合は、最後の回答者が獲得し、前のサブスクライバからの結果が上書きされます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="107">
          <source>Before the functionality described in this topic was introduced (platform update 5), there was no mechanism to ensure that, at most, a single subscriber provided a result, and that no results were lost if there were multiple subscribers.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このトピックで説明されている機能が導入される前 (プラットフォーム更新プログラム 5) は、最大でも単一のサブスクライバーが結果を提供し、複数のサブスクライバーが存在すると結果が失われないことを保証するメカニズムはありませんでした。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="108">
          <source>Ensuring, at most, one response</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">最大で 1 つの応答を確認</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="109">
          <source>In platform update 5, the <bpt id="p1">**</bpt>EventHandlerResult<ept id="p1">**</ept> class has an additional static constructor which ensures that the logic fails if more than one subscriber provides a result.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">プラットフォーム更新プログラム 5 では、1 つ以上のサブスクライバーが結果を提示している場合にロジックが失敗することを確認する追加の静的コンストラクターが、<bpt id="p1">**</bpt>EventHandlerResult<ept id="p1">**</ept> クラスにあります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="110">
          <source>The new constructor is named <bpt id="p1">**</bpt>newSingleResponse<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">新しいコンストラクターの名前は、<bpt id="p1">**</bpt>newSingleResponse<ept id="p1">**</ept>。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="111">
          <source>When instantiating an <bpt id="p1">**</bpt>EventHandlerResult<ept id="p1">**</ept> object using this method, the framework will throw an exception as soon as a second delegate handler method attempts to provide a result.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このメソッドを使用して <bpt id="p1">**</bpt>EventHandlerResult<ept id="p1">**</ept> オブジェクトをインスタンス化したとき、2 番目のデリゲート ハンドラー メソッドが結果を提供しようとすると、このフレームワークはただちに例外をスローします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="112">
          <source>IEventHandlerResultValidator interface</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">IEventHandlerResultValidator インターフェイス</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="113">
          <source>The validation in the <bpt id="p1">**</bpt>EventHandlerResult<ept id="p1">**</ept> class is handled by injecting an object of a type that implements the <bpt id="p2">**</bpt>IEventHandlerResultValidator<ept id="p2">**</ept> interface.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>EventHandlerResult<ept id="p1">**</ept> クラスの検証は、<bpt id="p2">**</bpt>IEventHandlerResultValidator<ept id="p2">**</ept> インターフェイスを実装するタイプのオブジェクトを挿入することで処理されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="114">
          <source>When instantiating the <bpt id="p1">**</bpt>EventHandlerResult<ept id="p1">**</ept> object using the <bpt id="p2">**</bpt>newSingleResponse<ept id="p2">**</ept> static constructor, an <bpt id="p3">**</bpt>EventHandlerSingleResponseValidator<ept id="p3">**</ept> object is instantiated and injected into the <bpt id="p4">**</bpt>EventHandlerResult<ept id="p4">**</ept> object, and the injected object becomes responsible for validating any result provided to the <bpt id="p5">**</bpt>EventhandlerResult<ept id="p5">**</ept> object.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p2">**</bpt>newSingleResponse<ept id="p2">**</ept> 静的コンストラクターを使用して <bpt id="p1">**</bpt>EventHandlerResult<ept id="p1">**</ept> オブジェクトをインスタンス化するとき、<bpt id="p3">**</bpt>EventHandlerSingleResponseValidator<ept id="p3">**</ept> オブジェクトがインスタンス化されて <bpt id="p4">**</bpt>EventHandlerResult<ept id="p4">**</ept> オブジェクトに挿入され、その挿入されたオブジェクトが <bpt id="p5">**</bpt>EventhandlerResult<ept id="p5">**</ept> オブジェクトに提供される結果の検証を担当します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="115">
          <source>Other validation classes can be implemented by having the class implement the <bpt id="p1">**</bpt>IEventHandlerResultValidator<ept id="p1">**</ept> interface, and injecting it into the <bpt id="p2">**</bpt>EventHandlerResult<ept id="p2">**</ept> class by instantiating the <bpt id="p3">**</bpt>EventHandlerResult<ept id="p3">**</ept> object using another new static constructor named <bpt id="p4">**</bpt>newWithResultValidator<ept id="p4">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">他の検証クラスは、クラスで <bpt id="p1">**</bpt>IEventHandlerResultValidator<ept id="p1">**</ept> インターフェイスを実装することにより実装され、<bpt id="p4">**</bpt>newWithResultValidator<ept id="p4">**</ept> という別の新しい静的コンストラクターを使って <bpt id="p3">**</bpt>EventHandlerResult<ept id="p3">**</ept> オブジェクトをインスタンス化することにより <bpt id="p2">**</bpt>EventHandlerResult<ept id="p2">**</ept> クラスに挿入できます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="116">
          <source>The constructor takes an argument of type <bpt id="p1">**</bpt>IEventHandlerResultValidator<ept id="p1">**</ept>, which makes it possible to inject any validator object as long as it implements the <bpt id="p2">**</bpt>IEventHandlerResultValidator<ept id="p2">**</ept> interface.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">コンストラクターは、<bpt id="p1">**</bpt>IEventHandlerResultValidator<ept id="p1">**</ept> 型の引数をとります。これにより <bpt id="p2">**</bpt>IEventHandlerResultValidator<ept id="p2">**</ept> インターフェイスを実装している限り、任意の検証オブジェクトを挿入できます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="117">
          <source>For example, the <bpt id="p1">**</bpt>newSingleResponse<ept id="p1">**</ept> static constructor simply delegates the instantiation to the <bpt id="p2">**</bpt>newWithResultValidator<ept id="p2">**</ept> static constructor like this.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">たとえば、<bpt id="p1">**</bpt>newSingleResponse<ept id="p1">**</ept> 静的コンストラクターは単にインスタンス化を <bpt id="p2">**</bpt>newWithResultValidator<ept id="p2">**</ept> 静的コンストラクターに委任し、次のようになります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="118">
          <source>Accept and reject request/response scenarios</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">要求/応答シナリオを承認して拒否する</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="119">
          <source>In certain request/response scenarios, the subscriber is only expected to provide their acceptance or rejection.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">特定の要求/応答シナリオでは、サブスクライバーは承認または拒否を提示することのみ期待されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="120">
          <source>Using the <bpt id="p1">**</bpt>EventHandlerResult<ept id="p1">**</ept> class to request acceptance/rejection can be confusing, if the subscriber is only expected to respond with a Boolean value.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">サブスクライバーがブール値での応答のみを期待している場合、受入/拒否の要求に <bpt id="p1">**</bpt>EventHandlerResult<ept id="p1">**</ept> クラスを使用することは分かりにくい可能性があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="121">
          <source>In a validation scenario, for example, should the subscriber only respond with Boolean false, when validation fails, or should the subscriber also respond with Boolean true, if validation succeeds?</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">たとえば、検証シナリオで、検証が失敗した場合にサブスクライバーはブール値 false でのみ応答すべきか、また検証が成功した場合にサブスクライバーがブール値 true で応答すべきかがあります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="122">
          <source>If the response is gathered using an <bpt id="p1">**</bpt>EventHandlerResult<ept id="p1">**</ept> object, then the second subscriber that validates and replies with Boolean true, might overwrite the Boolean false from the first subscriber.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>EventHandlerResult<ept id="p1">**</ept> オブジェクトを使用して応答が収集される場合、第二のサブスクライバーが true のブール値で検証し、応答すると、第一サブスクライバーの false のブール値が上書きされる可能性があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="123">
          <source>To mitigate this confusion, two new result type classes have been introduced in Platform update 5: <bpt id="p1">**</bpt>EventHandlerAcceptResult<ept id="p1">**</ept> and <bpt id="p2">**</bpt>EventHandlerRejectResult<ept id="p2">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この混乱を軽減するために、<bpt id="p1">**</bpt>EventHandlerAcceptResult<ept id="p1">**</ept> と <bpt id="p2">**</bpt>EventHandlerRejectResult<ept id="p2">**</ept> の 2 つの新しい結果型クラスがプラットフォーム更新プログラム 5 に導入されました。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="124">
          <source>When using the <bpt id="p1">**</bpt>EventHandlerAcceptResult<ept id="p1">**</ept> class, the delegate handler method can only respond by calling the <bpt id="p2">**</bpt>accept<ept id="p2">**</ept> method.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>EventHandlerAcceptResult<ept id="p1">**</ept> クラスを使用するとき、デリゲート ハンドラー メソッドは <bpt id="p2">**</bpt>承認<ept id="p2">**</ept> メソッドの呼び出しによってのみ応答できます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="125">
          <source>When using the <bpt id="p1">**</bpt>EventHandlerRejectResult<ept id="p1">**</ept> class, only the <bpt id="p2">**</bpt>reject<ept id="p2">**</ept> method can be called.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>EventHandlerRejectResult<ept id="p1">**</ept> クラスを使用するとき、<bpt id="p2">**</bpt>否認<ept id="p2">**</ept> メソッドのみを呼び出すことができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="126">
          <source>The two new classes also contain a <bpt id="p1">**</bpt>newSingleResponse<ept id="p1">**</ept> static constructor for use in scenarios where, at most, one subscriber is allowed to respond with their rejection or acceptance.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">2 つの新しいクラスには、最大で 1 つのサブスクライバーが拒否または承認で応答するシナリオで使用するための <bpt id="p1">**</bpt>newSingleResponse<ept id="p1">**</ept> 静的コンストラクターも含まれています。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="127">
          <source>Whether any subscriber has responded can still be answered by querying the <bpt id="p1">**</bpt>hasResult<ept id="p1">**</ept> method, and the acceptance/rejection is queried by calling either the <bpt id="p2">**</bpt>isAccepted<ept id="p2">**</ept> or <bpt id="p3">**</bpt>isRejected<ept id="p3">**</ept> methods for the <bpt id="p4">**</bpt>EventHandlerAcceptResult<ept id="p4">**</ept> and <bpt id="p5">**</bpt>EventHandlerRejectResult<ept id="p5">**</ept> classes, respectively.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">いずれかのサブスクライバーが応答したかどうかは <bpt id="p1">**</bpt>hasResult<ept id="p1">**</ept> メソッドをクエリすることによってまだ回答できます。承認/否認は、<bpt id="p4">**</bpt>EventHandlerAcceptResult<ept id="p4">**</ept> および <bpt id="p5">**</bpt>EventHandlerRejectResult<ept id="p5">**</ept> クラスの <bpt id="p2">**</bpt>isAccepted<ept id="p2">**</ept> または <bpt id="p3">**</bpt>isRejected<ept id="p3">**</ept> のいずれかのメソッドをそれぞれ呼び出すことによってクエリされます。</target></trans-unit>
      </group>
    </body>
  </file>
</xliff>