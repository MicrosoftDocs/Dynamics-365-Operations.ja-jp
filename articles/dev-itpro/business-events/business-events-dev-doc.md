<?xml version="1.0" encoding="UTF-8"?>
<xliff xmlns:logoport="urn:logoport:xliffeditor:xliff-extras:1.0" xmlns:tilt="urn:logoport:xliffeditor:tilt-non-translatables:1.0" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns="urn:oasis:names:tc:xliff:document:1.2" xmlns:xliffext="urn:microsoft:content:schema:xliffextensions" version="1.2" xsi:schemaLocation="urn:oasis:names:tc:xliff:document:1.2 xliff-core-1.2-transitional.xsd">
  <file datatype="xml" source-language="en-US" original="business-events-dev-doc.md" target-language="ja-JP">
    <header>
      <tool tool-company="Microsoft" tool-version="1.0-7889195" tool-name="mdxliff" tool-id="mdxliff"/>
      <xliffext:skl_file_name>business-events-dev-doc.198d9c.b8cc984908e6acfcb65684234337c67de23e1411.skl</xliffext:skl_file_name>
      <xliffext:version>1.2</xliffext:version>
      <xliffext:ms.openlocfilehash>b8cc984908e6acfcb65684234337c67de23e1411</xliffext:ms.openlocfilehash>
      <xliffext:ms.sourcegitcommit>f7e1720ffa3e34c787ca0f93d561cb75cbbb540a</xliffext:ms.sourcegitcommit>
      <xliffext:ms.lasthandoff>05/23/2019</xliffext:ms.lasthandoff>
      <xliffext:ms.openlocfilepath>articles\dev-itpro\business-events\business-events-dev-doc.md</xliffext:ms.openlocfilepath>
    </header>
    <body>
      <group extype="content" id="content">
        <trans-unit xml:space="preserve" translate="yes" id="101" restype="x-metadata">
          <source>Business events developer documentation</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ビジネス イベント開発者ドキュメント</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="102" restype="x-metadata">
          <source>This topic walks you through the development process and best practices for implementing business events.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このトピックでは、ビジネス イベントを実装するための開発プロセスおよびベスト プラクティスについて説明します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="103">
          <source>Business events developer documentation</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ビジネス イベント開発者ドキュメント</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="104">
          <source>This topic walks you through the development process and best practices for implementing business events.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このトピックでは、ビジネス イベントを実装するための開発プロセスおよびベスト プラクティスについて説明します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="105">
          <source>What is a business event and what is not a business event?</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">何がビジネス イベントで、何がビジネス イベントではないか。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="106">
          <source>This question comes up every time we start to think about use cases where business events can help.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ビジネス イベントが役立つユース ケースについて考慮するたびに、この疑問が生じます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="107">
          <source>Is creation of a vendor a business event?</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">仕入先の作成はビジネス イベントですか。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="108">
          <source>Or is confirming a purchase order a business event?</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">または、発注書の確認はビジネス イベントですか。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="109">
          <source>Is it a business event if you capture the event at the table level?</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">テーブル レベルでイベントをキャプチャする場合、それはビジネス イベントですか。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="110">
          <source>Or should business events only be captured at the business logic level in a business process?</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">または、ビジネス イベントはビジネス プロセス内のビジネス ロジック レベルでのみキャプチャする必要がありますか。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="111">
          <source>These are not only valid questions, but also a key topic of discussion when planning and architecting a solution for integration.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">これらは有効な質問であるだけでなく、統合のソリューションを計画および構築するときに考察するキー トピックです。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="112">
          <source>The following guidelines can be used to help with this thought process and decision making.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">次のガイドラインは、この思考過程および決定作業を支援するために使用することができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="113">
          <source>Intent</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">目的</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="114">
          <source>The intent behind capturing the business event must be clearly understood.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ビジネス イベントのキャプチャの背後にある目的を明確に把握している必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="115">
          <source>In other words, what is the reason for capturing the business event and how it is going to be used by the recipient.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">つまり、ビジネス イベントをキャプチャする理由および受信者が使用する方法です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="116">
          <source>If the intent for capturing a business event is to take a business action outside of Finance and Operations in response to the business event happening in Finance and Operations, then this is a valid intent to capture the business event.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ビジネス イベントをキャプチャする目的が、Finance and Operations で発生したビジネス イベントに応答して Finance and Operations 外でビジネス アクションを実行することである場合は、これはビジネス イベントをキャプチャする有効な目的です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="117">
          <source>The business action that is taken in response to the business event can be to notify users about the business event and/or to call into another business application to take a business action like, creating a sales order.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ビジネス イベントに応答して実行されるビジネス アクションは、ビジネス イベントに関するユーザーの変更や、販売注文を作成するなどのビジネス アクションを実行する他のビジネス アプリケーションを呼び出すことである場合があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="118">
          <source>It is important to look at the business action generically and not base the need for a business event on the type of business action that will be taken.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ビジネス アクションを、実行するビジネス アクションの種類でのビジネス イベントに必要な基準としてではなく、汎用として考えることは重要です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="119">
          <source>If the intent of capturing the business event is to transfer data to the recipient and in effect, realizing a data export scenario, then this will not be a good use case for using business events.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ビジネス イベントをキャプチャする目的がデータを他の受信者に転送して、事実上データ エクスポート シナリオを実現することである場合、これはビジネス イベントを使用するための良いユース ケースではありません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="120">
          <source>In fact, the use of business events for data transfer use cases will be a misuse of the business events framework.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">実際、データ転送ユース ケースのビジネス イベントの使用は、ビジネス イベント フレームワークの誤用となります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="121">
          <source>Such scenarios must continue to use data export mechanisms already available in data management.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このようなシナリオでは、データ管理で既に使用可能なデータ エクスポート メカニズムを使用し続ける必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="122">
          <source>Fidelity</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">忠実性</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="123">
          <source>When the intent is clear and a legitimate need for a business event is established, the next step is to evaluate the approach that must be taken to capture the business event.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">目的がはっきりしてビジネス イベントの正当なニーズが確立されると、次のステップはビジネス イベントをキャプチャするために必要なアプローチを評価することです。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="124">
          <source>The following section summarizes the approach that must be evaluated.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">次のセクションでは、評価する必要があるアプローチを要約します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="125">
          <source>Regardless of which approach is taken, the fidelity of business events is significant to ensure the following aspects are taken care of and as a result, must influence the design choice for implementing the business event.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">どのアプローチを採用するかに関わらず、ビジネス イベントの忠実性のためには以下の点を考慮することが重要で、結果として、ビジネス イベントを実装するためのデザイン選択に影響を与えます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="126">
          <source>However, the design choice that you take to implement a business event must not influence the concept of business events--the chosen design must not be used as a decision-making tool to determine if it is a business event.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ただし、ビジネス イベントを実装するためのデザイン選択がビジネス イベントのコンセプトには影響を与えないようにします。選択されたデザインは、それがビジネス イベントであるか決定するための決定ツールとして使用すべきではありません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="127">
          <source>The intent discussed previously must be used for such decisions.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このような決定には、事前に考慮された目的を使用する必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="128">
          <source><bpt id="p1">**</bpt>Durable business events<ept id="p1">**</ept> - There should be no false business events sent to the recipient.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>堅牢なビジネス イベント<ept id="p1">**</ept> - 間違ったビジネス イベントを受信者に送信するべきではありません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="129">
          <source>If a purchase order confirmation business event was sent out, then the recipient must trust that the purchase order was indeed confirmed.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">発注書確認ビジネス イベントが送信済みの場合、受取人はその発注書が確認済みであることを信用する必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="130">
          <source>The design choice must ensure this transactional nature and hence must not take a design choice that would violate this expectation.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">デザイン選択はこの取引の性質を保証する必要があり、この予想に反するデザイン選択を採用しないようにします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="131">
          <source><bpt id="p1">**</bpt>Targeted<ept id="p1">**</ept> - Business events must be designed to optimize the consumption story for the recipient.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>目標<ept id="p1">**</ept> - ビジネス イベントは受取人に対する消費ストーリーを最適化するように設計する必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="132">
          <source>In other words, make it as easy as possible for the recipient to consume business events.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">つまり、ビジネス イベントを消費する受信者のためにできるだけ簡単にします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="133">
          <source>Hence, business events must be as specific as possible and targeted to a specific use case.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このため、ビジネス イベントは可能な限り具体的であり、特定のユース ケースを対象としている必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="134">
          <source>Business events must not be generic thereby, leaving the consumer to determine what the business event was for by trying to understand the payload.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">そのためビジネス イベントは一般的なものではなく、コンシューマーがペイロードを理解するよう試みてビジネス イベントが何であったか判断させるべきではありません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="135">
          <source>The design choice made must allow for this to be preserved.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">実行されたデザイン選択は、これが順守されるようにする必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="136">
          <source><bpt id="p1">**</bpt>Noiseless<ept id="p1">**</ept> - There should be very little effort in the design to filter out the noise.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>ノイズレス<ept id="p1">**</ept> - デザイン内でノイズを除外するための努力が最小になるようにする必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="137">
          <source>To make business events very specific, avoid writing filtering logic to filter out conditions that do not match the expected business event.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ビジネス イベントを非常に明確にするため、予期するビジネス イベントと一致しない条件を除外するフィルタ ロジックの記述を避けます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="138">
          <source>The chosen approach must be such that the point at which the business event is implemented in code is specific enough to avoid the need for any filtering of noise.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">選択したアプローチは、ビジネス イベントがコードで実装されるポイントが、ノイズのフィルター処理が必要ないほど明確である必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="139">
          <source>Any attempt to filter the noise by adding logic can not only be taxing on performance but, it may also get complicated based on specific use cases.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ロジックの追加によってノイズをフィルター処理する試みはパフォーマンスの負荷になるだけでなく、特定のユース ケースに基づき複雑になる機能性があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="140">
          <source><bpt id="p1">**</bpt>Capturing at business logic level<ept id="p1">**</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>ビジネス ロジック レベルでのキャプチャ<ept id="p1">**</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="141">
          <source><bpt id="p1">**</bpt>Capturing at table level<ept id="p1">**</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>テーブル レベルでのキャプチャ<ept id="p1">**</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="142">
          <source>Ensures durability by being in the transaction</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">トランザクション内に置いて堅牢性を確保する</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="143">
          <source>Ensures durability by being in the transaction.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">トランザクション内に置いて堅牢性を確保します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="144">
          <source>Allows for targeted business events.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">対象となるビジネス イベントを許可します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="145">
          <source>Difficult to enable targeted business events due to the lower level capturing of events.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">イベントのキャプチャが低レベルであるため対象となるビジネス イベントを有効にすることが困難です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="146">
          <source>Makes it easy to remain noiseless.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">簡単にノイズレスのままにすることができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="147">
          <source>Difficult to remain noiseless unless additional effort is taken to put sound logic in place to filter out the noise.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ノイズを除去するためのサウンド ロジックを導入する追加作業が行われるまで、ノイズレスのままにすることは困難です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="148">
          <source>Provides additional context of the business process, which can significantly improve the durability and the quality of payload.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">堅牢性およびペイロードの品質を著しく向上させる、ビジネス プロセスの追加コンテキストを提供します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="149">
          <source>Business process context is most likely lost due to the lower level capturing of events.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">イベントのキャプチャが低レベルであると、ビジネス プロセスのコンテキストが失われる可能性が高くなります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="150">
          <source>Implementing a business event</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ビジネス イベントの実装</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="151">
          <source>Implementing a business event and sending it is a fairly straightforward process:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ビジネス イベントを実装して送信することは非常に簡単なプロセスです。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="152">
          <source>Build the contract.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">契約を構築します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="153">
          <source>Build the event.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">イベントを構築します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="154">
          <source>Add code to send the event.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">イベントを送信するコードを追加します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="155">
          <source>Two classes must be implemented:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">以下の 2 つのクラスを実装する必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="156">
          <source><bpt id="p1">**</bpt>Business event<ept id="p1">**</ept> – This class extends the <bpt id="p2">**</bpt>BusinessEventsBase<ept id="p2">**</ept> class.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>ビジネス イベント<ept id="p1">**</ept> - このクラスは <bpt id="p2">**</bpt>BusinessEventsBase<ept id="p2">**</ept> クラスを拡張します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="157">
          <source>It provides support for constructing the business event, building the payload, and sending the business event.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ビジネス イベントの構築、ペイロードの構築、およびビジネス イベントの送信のサポートを提供します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="158">
          <source><bpt id="p1">**</bpt>Business event contract<ept id="p1">**</ept> – This class extends the <bpt id="p2">**</bpt>BusinessEventsContract<ept id="p2">**</ept> class.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>ビジネス イベント契約<ept id="p1">**</ept> - このクラスは <bpt id="p2">**</bpt>BusinessEventsContract<ept id="p2">**</ept> クラスを拡張します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="159">
          <source>It defines the payload of the business event and allows for population of the contract at runtime.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ビジネス イベントのペイロードを定義して、実行時に契約の作成を許可します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="160">
          <source>BusinessEventsBase extension</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">BusinessEventsBase 拡張機能</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="161">
          <source>Naming convention</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">名前付け規則</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="162">
          <source>The names of business events should follow this pattern: &lt;noun/noun phrase&gt;<ph id="ph1">&lt;past tense action&gt;</ph>BusinessEvent</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ビジネス イベントの名前は以下のパターンに従う必要があります: &lt;名詞/名詞句&gt;<ph id="ph1">&lt;past tense action&gt;</ph>BusinessEvent</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="163">
          <source><bpt id="p1">**</bpt>Examples<ept id="p1">**</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>例<ept id="p1">**</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="164">
          <source>VendorInvoicePostedBusinessEvent</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">VendorInvoicePostedBusinessEvent</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="165">
          <source>CollectionLetterSentBusinessEvent</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">CollectionLetterSentBusinessEvent</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="166">
          <source>The &lt;noun/noun phrase&gt; part of the name should comply with existing definitions for application area prefixes.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">名前の &lt;名詞/名詞句&gt; パートは、アプリケーション領域の接頭語の既存の定義に準拠する必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="167">
          <source>Implementation</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">実装</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="168">
          <source>The process of implementing a <bpt id="p1">**</bpt>BusinessEventsBase<ept id="p1">**</ept> extension is straightforward.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>BusinessEventsBase<ept id="p1">**</ept> 拡張機能を実装するプロセスは簡単です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="169">
          <source>It involves extending the <bpt id="p1">**</bpt>BusinessEventsBase<ept id="p1">**</ept> class, and implementing a static constructor method, a private <bpt id="p2">**</bpt>new<ept id="p2">**</ept> method, methods to maintain internal state, and the <bpt id="p3">**</bpt>buildContract<ept id="p3">**</ept> method.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>BusinessEventsBase<ept id="p1">**</ept> クラスの拡張、および静的コンストラクター メソッドの実装、プライベート <bpt id="p2">**</bpt>新規<ept id="p2">**</ept> メソッド、内部状態を保持するメソッド、および <bpt id="p3">**</bpt>buildContract<ept id="p3">**</ept> メソッドが含まれます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="170">
          <source>Implement a static <bpt id="p1">**</bpt>newFrom&lt;my_buffer&gt;<ept id="p1">**</ept> method.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">静的 <bpt id="p1">**</bpt>newFrom&lt;my_buffer&gt;<ept id="p1">**</ept> メソッドを実装します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="171">
          <source>The &lt;my_buffer&gt; part of the method name is typically the table buffer that is used to initialize the business event contract.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">メソッド名の &lt;my_buffer&gt; パートは通常、ビジネス イベント契約を初期化するために使用されるテーブル バッファです。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="172">
          <source>Extend the <bpt id="p1">**</bpt>BusinessEventsBase<ept id="p1">**</ept> class.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>BusinessEventsBase<ept id="p1">**</ept> クラスを拡張します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="173">
          <source>Note the <bpt id="p1">**</bpt>BusinessEvents<ept id="p1">**</ept> attribute.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>BusinessEvents<ept id="p1">**</ept> 属性に注意してください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="174">
          <source>This attribute provides the business events framework with information about the business event's contract, name, and description, and also the module that it's part of.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この属性は、ビジネス イベントの契約、名前、説明、および含まれるモジュールに関する情報を含む、ビジネス イベント フレームワークを提供します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="175">
          <source>Labels must be defined for the name and description arguments, but should be referenced without the '@' symbol to avoid storing localized data.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ラベルは、名前と説明の引数に定義する必要がありますが、ローカライズされたデータの保存を避けるため、「@」記号なしで参照する必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="176">
          <source>Implement a private <bpt id="p1">**</bpt>new<ept id="p1">**</ept> method.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">プライベート <bpt id="p1">**</bpt>新規<ept id="p1">**</ept> メソッドを実装します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="177">
          <source>This method is called only from the static constructor method.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このメソッドは静的コンストラクター メソッドからのみ呼び出されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="178">
          <source>Implement private <bpt id="p1">**</bpt>parm<ept id="p1">**</ept> methods to maintain internal state.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">内部状態を維持するプライベート <bpt id="p1">**</bpt>parm<ept id="p1">**</ept> メソッドを実装します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="179">
          <source>Implement the <bpt id="p1">**</bpt>buildContract<ept id="p1">**</ept> method.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>buildContract<ept id="p1">**</ept> メソッドを実装します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="180">
          <source>Note that you'll need an EventContract stub for this step.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このステップには EventContract スタブが必要であることに注意してください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="181">
          <source>For extensibility, the <bpt id="p1">**</bpt>buildContract<ept id="p1">**</ept> method must be attributed with the <bpt id="p2">**</bpt>Wrappable(true)<ept id="p2">**</ept> and <bpt id="p3">**</bpt>Replaceable(true)<ept id="p3">**</ept> attributes.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">拡張機能のために、<bpt id="p1">**</bpt>buildContract<ept id="p1">**</ept> メソッドは <bpt id="p2">**</bpt>Wrappable(true)<ept id="p2">**</ept> および <bpt id="p3">**</bpt>Replaceable(true)<ept id="p3">**</ept> 属性に帰属する必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="182">
          <source>The <bpt id="p1">**</bpt>buildContract<ept id="p1">**</ept> method will be called only when a business event is enabled for a company.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>buildContract<ept id="p1">**</ept> メソッドは会社のためにビジネス イベントが有効にされるときにのみ呼び出されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="183">
          <source>Here is the complete implementation of the "Sales order invoice posted" business event.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">これは、「転記された販売注文請求書」ビジネス イベントの完全な実装です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="184">
          <source>BusinessEventsContract extension</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">BusinessEventsContract 拡張機能</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="185">
          <source>A business event contract class extends the <bpt id="p1">**</bpt>BusinessEventsContract<ept id="p1">**</ept> class.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ビジネス イベント契約クラスは <bpt id="p1">**</bpt>BusinessEventsContract<ept id="p1">**</ept> クラスを拡張します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="186">
          <source>It defines and populates the payload of the business event.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ビジネス イベントのペイロードを定義および入力します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="187">
          <source>Although there is some variation across business events, the basic structure of the business event contract is consistent.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ビジネス イベントには一部の変動がありますが、ビジネス イベント契約の基本構造は一貫しています。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="188">
          <source>The process of implementing a business event contract involves extending the <bpt id="p1">**</bpt>BusinessEventContract<ept id="p1">**</ept> class, defining internal state, implementing an initialization method, implementing a static constructor method, and implementing <bpt id="p2">**</bpt>parm<ept id="p2">**</ept> methods to access the contract state.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ビジネス イベント契約の実装プロセスには、<bpt id="p1">**</bpt>BusinessEventContract<ept id="p1">**</ept> クラスの拡張、内部状態の定義、初期化メソッドの実装、静的コンストラクター メソッドの実装、および契約状態にアクセスするための <bpt id="p2">**</bpt>parm<ept id="p2">**</ept> メソッドの実装が含まれます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="189">
          <source>Extend the <bpt id="p1">**</bpt>BusinessEventContract<ept id="p1">**</ept> class.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>BusinessEventContract<ept id="p1">**</ept> クラスを拡張します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="190">
          <source>The class must be attributed with the <bpt id="p1">**</bpt>DataContract<ept id="p1">**</ept> attribute.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">クラスは <bpt id="p1">**</bpt>DataContract<ept id="p1">**</ept> 属性に帰属する必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="191">
          <source>Add private variables to hold the contract state.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">契約状態を保持するプライベート変数を追加します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="192">
          <source>Implement a private initialization method.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">プライベート初期化メソッドを実装します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="193">
          <source>The <bpt id="p1">**</bpt>initialize<ept id="p1">**</ept> method is responsible for setting the business event contract class's private state, based on data that is provided through the static constructor method.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>初期化<ept id="p1">**</ept> メソッドは、静的コンストラクター メソッドを介して提供されるデータに基づき、ビジネス イベント契約クラスのプライベート状態を設定します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="194">
          <source>Implement a static constructor method.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">静的コンストラクター メソッドを実装します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="195">
          <source>The static constructor method calls a private <bpt id="p1">**</bpt>initialize<ept id="p1">**</ept> method to initialize the private class state.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">静的コンストラクター メソッドはプライベート <bpt id="p1">**</bpt>初期化<ept id="p1">**</ept> メソッドを呼び出して、プライベート クラス状態を初期化します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="196">
          <source>Implement <bpt id="p1">**</bpt>parm<ept id="p1">**</ept> methods to access the contract state.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">契約状態にアクセスするための <bpt id="p1">**</bpt>parm<ept id="p1">**</ept> メソッドを実装します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="197">
          <source>The <bpt id="p1">**</bpt>parm<ept id="p1">**</ept> methods should be attributed with the <bpt id="p2">**</bpt>DataMember('<ph id="ph1">&lt;name&gt;</ph>')<ept id="p2">**</ept> and <bpt id="p3">**</bpt>BusinessEventsDataMember('<ph id="ph2">&lt;description&gt;</ph>')<ept id="p3">**</ept> attributes.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>parm<ept id="p1">**</ept> メソッドは <bpt id="p2">**</bpt>DataMember('<ph id="ph1">&lt;name&gt;</ph>')<ept id="p2">**</ept> および <bpt id="p3">**</bpt>BusinessEventsDataMember('<ph id="ph2">&lt;description&gt;</ph>')<ept id="p3">**</ept> 属性に帰属する必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="198">
          <source>The name that you provide on the attribute (for example <bpt id="p1">**</bpt>'InvoiceAccount'<ept id="p1">**</ept>) will be visible to data contract consumers.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">属性で提供する名前 (たとえば、 <bpt id="p1">**</bpt>'InvoiceAccount'<ept id="p1">**</ept>) はデータ契約消費者に対して表示されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="199">
          <source>The description provided in the BusinessEventsDataMember will be visible in the Business Events catalog UI when describing this contract's data members.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">BusinessEventsDataMember で指定された説明は、この契約のデータ メンバーを記述するときにビジネス イベント カタログ UI に表示されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="200">
          <source><bpt id="p1">**</bpt>RecId<ept id="p1">**</ept> values should not be part of a business event payload.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>RecId<ept id="p1">**</ept> 値はビジネス イベント ペイロードの一部にすることはできません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="201">
          <source>Use the alternate key (AK) instead.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">代わりに代替キー (AK) を使用します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="202">
          <source>Enumeration (enum) values must be converted to their symbol value before they can be published.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">列挙型 (enum) 値は、公開する前にそのシンボル値に変換する必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="203">
          <source>Use the <bpt id="p1">**</bpt>enum2Symbol<ept id="p1">**</ept> method to convert an enum's value to the symbol string.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>enum2Symbol<ept id="p1">**</ept> メソッドを使用して列挙型の値をシンボル文字列に変換します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="204">
          <source>Here is an example:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">次に例を示します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="205">
          <source>In some cases, population of the data contract's internal state will require that you implement additional retrieval methods.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">場合によっては、データ契約の内部状態の投入のために、追加の取得メソッドを実装する必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="206">
          <source>These retrieval methods should be implemented as private methods, and they should be called from the <bpt id="p1">**</bpt>initialize<ept id="p1">**</ept> method.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">これらの取得メソッドはプライベート メソッドとして実装し、<bpt id="p1">**</bpt>初期化<ept id="p1">**</ept> メソッドから呼び出す必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="207">
          <source>Here is the complete implementation of the "Sales order invoice posted" business event contract.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">これは、「転記された販売注文請求書」ビジネス イベント契約の完全な実装です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="208">
          <source>Sending a business event</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ビジネス イベントの送信</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="209">
          <source>You must modify application code so that it sends the business event at the appropriate point.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">適切なポイントでビジネス イベントを送信するようにアプリケーション コードを変更する必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="210">
          <source>Often, you can use a common point within a framework.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">多くの場合、フレームワーク内の共通ポイントを使用することができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="211">
          <source>Documents that extend <bpt id="p1">**</bpt>SourceDocument<ept id="p1">**</ept> have a common point for creating and sending a business event.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>SourceDocument<ept id="p1">**</ept> を拡張するドキュメントには、ビジネス イベントを作成および送信するための共通ポイントがあります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="212">
          <source>For more information, see the section on source document framework support below.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">詳細については、以下をサポートする元伝票フレームワークのセクションを参照してください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="213">
          <source>Other frameworks also provide common points for sending business events.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">また、他のフレームワークもビジネス イベントを送信するための共通ポイントを提供します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="214">
          <source>For example, the <bpt id="p1">**</bpt>CustVendVoucher<ept id="p1">**</ept> class hierarchy in AOT has a <bpt id="p2">**</bpt>post<ept id="p2">**</ept> method that is used to send business events that are related to posting customer or vendor vouchers.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">たとえば、AOT 内の <bpt id="p1">**</bpt>CustVendVoucher<ept id="p1">**</ept> クラス階層には、顧客または仕入先の伝票の転記に関連付けられたビジネス イベンの送信に使用される、<bpt id="p2">**</bpt>転記<ept id="p2">**</ept> メソッドがあります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="215">
          <source>Overrides of the base class implementation provide specialization of the logic for sending business events.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">基本クラス実装の上書きでは、ビジネス イベントを送信するためのロジックの特化を提供します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="216">
          <source>For an example, see <bpt id="p1">**</bpt>CustVoucher.createBusinessEvent<ept id="p1">**</ept> or <bpt id="p2">**</bpt>VendVoucher.createBusinessEvent<ept id="p2">**</ept> in AOT.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">例については、AOT の <bpt id="p1">**</bpt>CustVoucher.createBusinessEvent<ept id="p1">**</ept> または <bpt id="p2">**</bpt>VendVoucher.createBusinessEvent<ept id="p2">**</ept> を参照してください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="217">
          <source>The sending of a business event is linked to the commit of the underlying transaction.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ビジネス イベントの送信は、基になる取引のコミットにリンクされます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="218">
          <source>If the underlying transaction is aborted, the business event won't be sent.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">基になる取引が中止される場合、ビジネス イベントは送信されません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="219">
          <source>Therefore, applications can send the business event at the point where the payload information is available.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">そのため、アプリケーションはペイロード情報が使用可能なポイントでビジネス イベントを送信することができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="220">
          <source>The business events framework determines whether a business event is published to a consumer.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ビジネス イベント フレームワークは、ビジネス イベントが消費者に公開されるかどうか決定します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="221">
          <source>As a general rule, applications should always send a business event, regardless of whether the business event is enabled.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">一般的なルールとして、ビジネス イベントが有効かどうかに関わらず、アプリケーションはビジネス イベントを常に送信する必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="222">
          <source>If significant additional logic is required, or if the logic for sending a business event has a performance impact, an application can check whether a specific business event is enabled before it runs business logic that is associated with sending business events.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">重要な追加ロジックが必要な場合、またはビジネス イベントを送信するためのロジックがパフォーマンスに影響する場合は、ビジネス イベントの送信に関連付けられたビジネス ロジックを実行する前に、アプリケーションは特定のビジネス イベントが有効化されているかどうか確認することができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="223">
          <source>This check is done through the <bpt id="p1">**</bpt>BusinessEventsConfigurationReader::isBusinessEventEnabled<ept id="p1">**</ept> method.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この確認は <bpt id="p1">**</bpt>BusinessEventsConfigurationReader::isBusinessEventEnabled<ept id="p1">**</ept> メソッドを介して実行されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="224">
          <source>Source document framework support</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ソース ドキュメント フレームワークのサポート</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="225">
          <source>The source document framework supports sending business events automatically as part of the transition from an in-process state to a completed state for the document.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">元伝票フレームワークは、ドキュメントのプロセス内状態から完了状態への移行の一部として、ビジネス イベントの自動送信をサポートします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="226">
          <source>To take advantage of this capability, documents that extend the source document framework must implement an extension of the <bpt id="p1">**</bpt>SourceDocumentStateInProcess.getBusinessEvent<ept id="p1">**</ept> method to create and return the correct <bpt id="p2">**</bpt>BusinessEventsBase<ept id="p2">**</ept> extension type.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この機能を活用するには、元伝票フレームワークを拡張するドキュメントが <bpt id="p1">**</bpt>SourceDocumentStateInProcess.getBusinessEvent<ept id="p1">**</ept> メソッドの拡張機能を実装して、正確な <bpt id="p2">**</bpt>BusinessEventsBase<ept id="p2">**</ept> 拡張子タイプを作成して戻す必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="227">
          <source>Extending a business event payload</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ビジネス イベント ペイロードの拡張</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="228">
          <source>You might want to publish additional information as part of the payload of a business event.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ビジネス イベントのペイロードの一部として、追加情報を公開する場合があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="229">
          <source>To send this additional information, you must extend the business event's standard payload.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この追加情報を送信するには、ビジネス イベントの標準ペイロードを拡張する必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="230">
          <source>Example scenario</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">シナリオ例</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="231">
          <source>This example shows how to extend the <bpt id="p1">**</bpt>CustFreeTextInvoicePostedBusinessEventContract<ept id="p1">**</ept> class so that it includes a customer classification.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この例では、<bpt id="p1">**</bpt>CustFreeTextInvoicePostedBusinessEventContract<ept id="p1">**</ept> を拡張して顧客の分類を含める方法を示します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="232">
          <source>This customer classification is an industry-based custom classification.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この顧客分類は業界に基づくカスタム分類です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="233">
          <source>Step 1: Create an extended business event contract</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ステップ 1: 拡張されたビジネス イベント契約の作成</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="234">
          <source>Create a contract that consists of the standard business event contract plus any additional information that must be included in the payload.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">標準的なビジネス イベント契約、およびペイロードに含める必要がある追加情報で構成される契約を作成します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="235">
          <source>Step 2: Create an initialize method</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ステップ 2: 初期化メソッドの作成</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="236">
          <source>Create an <bpt id="p1">**</bpt>initialize<ept id="p1">**</ept> method that initializes the value of the private contract.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">プライベート契約の値を初期化する <bpt id="p1">**</bpt>初期化<ept id="p1">**</ept> メソッドを作成します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="237">
          <source>Step 3: Create a static newFrom method</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ステップ 3: 静的 newFrom メソッドの作成</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="238">
          <source>Create a static <bpt id="p1">**</bpt>newFrom<ept id="p1">**</ept> method that takes the standard contract as an argument and calls the <bpt id="p2">**</bpt>initialize<ept id="p2">**</ept> method.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">標準契約を引数として取得し <bpt id="p2">**</bpt>初期化<ept id="p2">**</ept> メソッドを呼び出す、静的 <bpt id="p1">**</bpt>newFrom<ept id="p1">**</ept> メソッドを作成します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="239">
          <source>Step 4: Map parm methods</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ステップ 4: parm メソッドのマッピング</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="240">
          <source>Copy the <bpt id="p1">**</bpt>parm<ept id="p1">**</ept> methods from the standard data contract, and modify each method so that it gets and sets values in the class's standard contract instance.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>parm<ept id="p1">**</ept> メソッドを標準データ コントラクトからコピーして、クラスの標準契約インスタンス内で値を取得およびセットするように各メソッドを修正します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="241">
          <source>Step 5: Add parms methods for additional payload data</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ステップ 5: 追加ペイロード データのために parm メソッドを追加する</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="242">
          <source>Here is the complete implementation of the extended business contract.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">これは拡張ビジネス契約の完全な実装です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="243">
          <source>Step 6: Wrap the buildContract method</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ステップ 6: buildContract メソッドをラップします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="244">
          <source>Provide a build contract implementation that calls <bpt id="p1">**</bpt>next<ept id="p1">**</ept> to load the standard business event contract and populates any payload extensions.</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">標準ビジネス イベント契約をロードしてペイロード拡張機能を投入する <bpt id="p1">**</bpt>next<ept id="p1">**</ept> を呼び出す、ビルド契約の実装を提供します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="245">
          <source>Here is the complete class.</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">これは完全なクラスです。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="246">
          <source>Extending filters to have custom fields (if supported by the middleware)</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">カスタム フィールドを持つようにフィルターを拡張する (ミドルウェアによってサポートされている場合)</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="247">
          <source>Some middleware systems allow for filtering of the events.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">一部のミドルウェア システムはイベントのフィルター処理を許可します。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="248">
          <source>For example, Azure Service Bus has a property bag that can be populated with key-value pairs.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">たとえば、Azure Service Bus にはキーと値のペアを設定できるプロパティ バッグがあります。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="249">
          <source>These key-value pairs can be used for filtering events when reading from the Azure Service Bus Queue or Topic.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">これらのキーと値のペアは、Azure Service Bus のキューやトピックからの読み込み時にイベントをフィルター処理するために使用できます。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="250">
          <source>Additionally, Azure Event Grid has filterable message properties like Subject, Event Type, and ID.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">また、Azure イベント グリッドには件名、イベント タイプ、ID などのフィルター処理されたメッセージ プロパティがあります。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="251">
          <source>To support these different properties for the different systems, the Business Events framework uses a concept called PayloadContext, which can be extended to include custom fields for filtering by the different eventing systems.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">さまざまなシステムに対してこれらの異なるプロパティをサポートするために、ビジネス イベント フレームワークは PayloadContext と呼ばれる概念を使用しており、さまざまなイベント システムによるフィルター処理に対してカスタム フィールドを含むように拡張できます。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="252">
          <source>Payload context</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">ペイロード コンテキスト</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="253">
          <source>The Business Events framework supports a concept of <bpt id="p1">*</bpt>payload context<ept id="p1">*</ept>, which provides a means for decorating messages sent by the framework with context about the payload.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">ビジネス イベント フレームワークは <bpt id="p1">*</bpt>ペイロード コンテキスト<ept id="p1">*</ept> の概念をサポートしており、フレームワークによって送信されたメッセージをペイロードに関するコンテキストで修飾する手段を提供します。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="254">
          <source>In some scenarios, additional context may be required when sending messages to endpoints, so the framework has hookpoints where the context can be overwritten and the adapters can be customized.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">シナリオによっては、エンドポイントにメッセージを送信するときに追加のコンテキストが必要になることがあります。そのため、フレームワークにはコンテキストの上書きやアダプタのカスタマイズができるフックポイントがあります。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="255">
          <source>Adding a custom payload context</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">カスタム ペイロード コンテキストの追加</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="256">
          <source>A custom payload context must extend from the class BusinessEventsCommitLogPayloadContext.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">カスタム ペイロード コンテキストは BusinessEventsCommitLogPayloadContext クラスから拡張する必要があります。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="257">
          <source>Constructing the custom payload context</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">カスタム ペイロード コンテキストの構築</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="258">
          <source>A Chain of Command (CoC) extension will need to be written for the BusinessEventsSender.buildPayloadContext method to construct the new payload context type.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">新しいペイロード コンテキスト タイプを作成するには、BusinessEventsSender.buildPayloadContext メソッドに対してコマンド チェーン (CoC) 拡張機能を記述する必要があります。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="259">
          <source>Consuming the custom payload context from an adapter</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">アダプターからカスタム ペイロード コンテキストを使用する</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="260">
          <source>Adapters that consume payload context are written in such a way that they expose CoC methods to allow consuming new payload contexts.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">ペイロード コンテキストを使用するアダプターは、CoC メソッドを公開して新しいペイロード コンテキストを使用できるように記述されます。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="261">
          <source>The following example explores what this looks like for the Service Bus adapter, which has a generic property bag that can be filtered on by the consumers of the Service Bus.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">次の例では、サービス バス アダプターの一般的なプロパティ バッグを持ち、サービス バスの消費者によってフィルター処理できるサービス バス アダプターの外観について説明します。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="262">
          <source>The BusinessEventsServiceBusAdapter has the CoC method called addProperties.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">BusinessEventsServiceBusAdapter には addProperties という CoC メソッドがあります。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="263">
          <source>Adding a custom endpoint type</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">カスタム エンドポイント タイプの追加</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="264">
          <source>The Business Events framework supports adding new endpoint types in addition to the ones that ship out of the box.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">ビジネス イベント フレームワークは出荷時のものに加え、新しいエンドポイント タイプの追加をサポートしています。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="265">
          <source>An example of how to do this is describe with the below.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">この方法の例は以下の説明を参照してください。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="266">
          <source>Add new endpoint type</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">新しいエンドポイント タイプの追加</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="267">
          <source>Each endpoint type is represented by the enum BusinessEventsEndpointType.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">各エンドポイント タイプは、列挙 BusinessEventsEndpointType によって表されます。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="268">
          <source>Adding a new endpoint starts by extending this enum, as shown in the following section.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">新しいエンドポイントの追加は、次のセクションで示すように、この列挙を拡張して開始されます。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="269">
          <source>Business event endpoint</source><target logoport:matchpercent="87" state="translated" state-qualifier="x-fuzzy-match-unedited">ビジネス イベントのエンドポイント</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="270">
          <source>Add new endpoint table to the hierarchy</source><target logoport:matchpercent="73" state="translated" state-qualifier="fuzzy-match">新しいエンドポイント テーブルを階層に追加します</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="271">
          <source>All endpoint data is stored in a hierarchy table, the root of which is BusinessEventsEndpoint.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">すべてのエンドポイント データが階層テーブルに保管され、そのルートは BusinessEventsEndpoint です。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="272">
          <source>A new endpoint table must extend this root table by setting the Support Inheritance property = Yes, and the Extends property = “BusinessEventsEndpoint” (or any other endpoint in the BusinessEventsEndpoint hierarchy).</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">新しいエンドポイント テーブルは、サポート継承プロパティ = Yes、拡張プロパティ = “BusinessEventsEndpoint” (または BusinessEventsEndpoint 階層内の他の任意のエンドポイント) を設定して、このルート テーブルを拡張する必要があります。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="273">
          <source>Business event endpoint</source><target logoport:matchpercent="100" state="translated" state-qualifier="exact-match">ビジネス イベントのエンドポイント</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="274">
          <source>The new table will then hold the definition of the custom fields needed to initialize and communicate with this endpoint in code.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">その後、新しいテーブルに、このエンドポイントとの初期化とコード内での通信に必要なカスタム フィールドの定義が保持されます。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="275">
          <source>To avoid the possibility of conflict, field names should be qualified to the specific endpoint where they belong.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">競合の可能性を回避するには、フィールド名を属している特定のエンドポイントに対して限定する必要があります。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="276">
          <source>For example, two endpoints can have the concept of a “URL” field, but to distinguish them, their names should be specific to the custom endpoint like “CustomURL”.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">たとえば、2 つのエンドポイントは "URL" フィールドの概念を持つことができますが、それらを区別するために "CustomURL" のようなカスタム エンドポイントに固有の名前にする必要があります。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="277">
          <source>Business event endpoint</source><target logoport:matchpercent="100" state="translated" state-qualifier="exact-match">ビジネス イベントのエンドポイント</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="278">
          <source>Add new EndpointAdapter class that implements IBusinessEventsEndpoint</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">IBusinessEventsEndpoint を実装する新しい EndpointAdapter クラスを追加します</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="279">
          <source>The new endpoint adapter class must implement the IBusinessEventsEndpoint interface as well as be decorated with the BusinessEventsEndpointAttribute attribute.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">新しいエンドポイント アダプター クラスでは IBusinessEventsEndpoint インターフェイスを実装し、BusinessEventsEndpointAttribute 属性で修飾する必要があります。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="280">
          <source>The initialize method should be implemented to check the type of the BusinessEventsEndpoint buffer that is passed in, and initialize when it is of the correct type for this new adapter, as shown below.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">初期化メソッドを実装して、渡された BusinessEventsEndpoint バッファーのタイプを確認し、次に示すように、この新しいアダプターに対して適切な型である場合は初期化する必要があります。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="281">
          <source>Extend the EndpointConfiguration form</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">EndpointConfiguration フォームの拡張</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="282">
          <source>Add a new group control under FormDesign/BusinessEventsEndpointConfigurationGroup/EndpointFieldsGroup/ to hold your custom field input.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">カスタム フィールド入力を保持するには FormDesign/BusinessEventsEndpointConfigurationGroup/EndpointFieldsGroup/ の下に新しいグループ コントロールを追加します。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="283">
          <source>Business event endpoint</source><target logoport:matchpercent="100" state="translated" state-qualifier="exact-match">ビジネス イベントのエンドポイント</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="284">
          <source>The custom field input should be bound to the new table and field created in the previous step.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">カスタム フィールドの入力は、前の手順で作成された新しいテーブルとフィールドにバインドする必要があります。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="285">
          <source>Create a class extension to extend the getConcreteType and showOtherFields methods of BusinessEventsEndpointConfiguration form, as shown below.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">次に示すように、BusinessEventsEndpointConfiguration フォームの getConcreteType と showOtherFields メソッドを拡張するクラス拡張機能を作成します。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="286">
          <source>Business event endpoint</source><target logoport:matchpercent="100" state="translated" state-qualifier="exact-match">ビジネス イベントのエンドポイント</target>
        </trans-unit>
      </group>
    </body>
  </file>
</xliff>