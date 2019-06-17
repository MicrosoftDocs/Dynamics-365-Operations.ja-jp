<?xml version="1.0" encoding="UTF-8"?>
<xliff xmlns:logoport="urn:logoport:xliffeditor:xliff-extras:1.0" xmlns:tilt="urn:logoport:xliffeditor:tilt-non-translatables:1.0" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns="urn:oasis:names:tc:xliff:document:1.2" xmlns:xliffext="urn:microsoft:content:schema:xliffextensions" version="1.2" xsi:schemaLocation="urn:oasis:names:tc:xliff:document:1.2 xliff-core-1.2-transitional.xsd">
  <file datatype="xml" source-language="en-US" original="adyen-connector-listPI.md" target-language="ja-JP">
    <header>
      <tool tool-company="Microsoft" tool-version="1.0-7889195" tool-name="mdxliff" tool-id="mdxliff"/>
      <xliffext:skl_file_name>adyen-connector-listPI.ea619b.32170f52137b6811cab9b414b8733ffc9ed1ae0c.skl</xliffext:skl_file_name>
      <xliffext:version>1.2</xliffext:version>
      <xliffext:ms.openlocfilehash>32170f52137b6811cab9b414b8733ffc9ed1ae0c</xliffext:ms.openlocfilehash>
      <xliffext:ms.sourcegitcommit>45eeca48c6cb4f3f94d61392f4f99a52dc443a97</xliffext:ms.sourcegitcommit>
      <xliffext:ms.lasthandoff>05/24/2019</xliffext:ms.lasthandoff>
      <xliffext:ms.openlocfilepath>articles\retail\dev-itpro\adyen-connector-listPI.md</xliffext:ms.openlocfilepath>
    </header>
    <body>
      <group extype="content" id="content">
        <trans-unit xml:space="preserve" translate="yes" id="101" restype="x-metadata">
          <source>Saving online payment instruments with the Adyen connector</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Adyen コネクタでオンライン支払手段を保存する</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="102" restype="x-metadata">
          <source>This topic describes how to save payment instruments by using the Adyen connector for e-commerce.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">このトピックでは、電子商取引の Adyen コネクタを使用して支払手段を保存する方法を説明します。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="103">
          <source>Saving online payments with the Adyen connector</source><target logoport:matchpercent="84" state="translated" state-qualifier="fuzzy-match">Adyen コネクタでオンライン支払を保存する</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="104">
          <source>This topic describes the setup and functionality that are related to saving payment instruments when you use the Adyen "card not present" payment connector for the Dynmics e-Commerce platform.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">このトピックでは、Dynamics 電子商取引プラットフォームで Adyen の "カードが存在しない" 支払コネクタを使用している場合に、支払手段の保存に関連する設定と機能について説明します。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="105">
          <source>Key terms</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">重要な用語</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="106">
          <source>Term</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">相談</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="107">
          <source>Description</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">説明</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="108">
          <source>Token</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">トークン</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="109">
          <source>A string of data that a payment processor provides as a reference.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">支払プロセッサが参照として提供する一連のデータ。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="110">
          <source>Tokens can represent payment card numbers, payment authorizations, and previous payment captures.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">トークンは、支払カード番号、支払認証、前回の支払キャプチャを表すことができます。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="111">
          <source>Tokens are important because they help keep sensitive data out of the point of sale (POS) system.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">トークンは、販売時点管理 (POS) システムの外で機密データを保持するのに役立つため重要です。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="112">
          <source>Card token</source><target logoport:matchpercent="68" state="translated" state-qualifier="fuzzy-match">カードのトークン</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="113">
          <source>A token that a payment processor provides for storage in the POS system.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">POS システムのストレージに対して支払プロセッサが提供するトークン。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="114">
          <source>The card token, or card reference, can be used only by the merchant who receives it</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">カードのトークン (またはカードの参照) は、それを受け取る販売者のみが使用できます。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="115">
          <source>Authorization (Auth) token</source><target logoport:matchpercent="69" state="translated" state-qualifier="fuzzy-match">承認 (認証) トークン</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="116">
          <source>After a POS system makes an authorization request to a payment processor, the payment processor provides a unique ID to the POS system as part of the response to that request.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">POS システムが支払プロセッサに承認要求をした後、支払プロセッサはその要求に対する応答の一部として POS システムに固有の ID を提供します。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="117">
          <source>This authorization token, or authorization reference, can be used later, when the processor is called to perform actions such as reversing or voiding the authorization.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">承認を取り消したり無効にしたりするなどのアクションを実行するためにプロセッサが呼び出されたときに、この承認トークンや承認参照を後で使用できます</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="118">
          <source>However, an authorization token is most often used to capture funds when an order is fulfilled or when a transaction is being finalized.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">ただし、承認トークンは、注文が履行されたとき、またはトランザクションが確定したときに、資金を取得するために最もよく使用されます。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="119">
          <source>List PI</source><target logoport:matchpercent="98" state="translated" state-qualifier="fuzzy-match">リスト PI</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="120">
          <source>A frequently used generic name for the capability that is described in this topic.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">このトピックで説明されている機能に対して頻繁に使用される一般名。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="121">
          <source>List PI refers to the ability to save payment instruments and to list previously used payment instruments during future checkouts that are done through the same e-commerce website.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">リスト PI は、同じ電子商取引 Web サイトを通じて行われる将来のチェックアウト中に、支払手段を保存し、以前に使用された支払手段を一覧にする機能を意味します。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="122">
          <source>Named user</source><target logoport:matchpercent="80" state="translated" state-qualifier="fuzzy-match">名前付きユーザー</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="123">
          <source>An e-commerce customer who is signed in to the online storefront at the time of checkout.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">チェックアウト時にオンライン ストアフロントにログインしている電子商取引の顧客。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="124">
          <source>Named users have a unique customer ID, and their online purchases are always mapped to the same customer ID whenever they are signed in to the online storefront.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">名前付きユーザーは一意の顧客 ID を持ち、オンライン ストアフロントにログインするたびにそのオンライン購入が常に同じ顧客 ID にマップされます。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="125">
          <source>Overview</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">概要</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="126">
          <source>When e-commerce orders are created, retailers often offer to save the customer's payment card information so that it can be used for future transactions.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">電子商取引の注文を作成する場合、小売企業は将来のトランザクションで使用できるように顧客の支払カード情報を保存するよう促すことがよくあります。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="127">
          <source>This topic explains how that capability ("List PI") is delivered through the Microsoft Dynamics 365 Payment Connector for Adyen.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">このトピックでは、この機能 ("リストPI") が Adyen の Microsoft Dynamics 365 支払コネクタを通じて配送される方法を説明します。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="128">
          <source>Although the Adyen payment connector supports this capability out of the box, third-party payment connectors require customization.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Adyen 支払コネクタはこの機能をそのままではサポートしておらず、サード パーティの支払コネクタについてはカスタマイズが必要です。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="129">
          <source>Additionally, not all payment processors might support the same method of saving payment card information.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">また、すべての支払プロセッサが同じ方法で支払カード情報の保存をサポートしているとは限りません。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="130">
          <source>The out-of-box implementation of the List PI capability relies on the payment processor to keep a mapping of an online customer's unique ID to the payment instruments that have previously been processed through that payment connector.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">リスト PI 機能の初期状態の実装では、支払プロセッサを使用して、その支払コネクタで既に処理された支払手段に対して、オンライン顧客の一意な ID のマッピングを保持する必要があります。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="131">
          <source>Only customers who are signed in to the website as named users have the option to save their payment card information for their next online visit.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">名前付きユーザーとして Web サイトにログインしている顧客のみに、支払カード情報を次回のオンライン訪問のために保存するオプションがあります。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="132">
          <source>Customers who use a "guest checkout" option when they create an online order won't be able to save payment card information for future transactions.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">"ゲスト チェックアウト" オプションを使用してオンライン注文を作成する顧客は、将来のトランザクションに対して支払カードの情報を保存できません。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="133">
          <source>Prerequisites</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">必要条件</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="134">
          <source>The List PI capability requires the following elements:</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">リスト PI 機能には次の要素が必要です:</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="135">
          <source>An e-commerce integration with Microsoft Dynamics 365 for Retail</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">電子商取引と Microsoft Dynamics 365 for Retail の統合</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="136">
          <source>A payment connector that is compatible with the List PI capability</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">リスト PI 機能と互換性のある支払コネクタ</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="137">
          <source>A payment processor that maps unique customer IDs to the payment instruments that the customers want that payment processor to save</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">顧客がその支払プロセッサに保存させたい支払手段に一意の顧客 ID をマッピングする支払プロセッサ</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="138">
          <source>For more information about how to implement payment connectors and the Retail software development kit (SDK) in general, visit the <bpt id="p1">[</bpt>Retail for IT pros and developers home page<ept id="p1">](https://docs.microsoft.com/dynamics365/unified-operations/retail/dev-itpro/dev-retail-home-page#payment-connectors)</ept>.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">一般的な支払コネクタと小売ソフトウェア開発キット (SDK) の実装方法の詳細については、<bpt id="p1">[</bpt>IT プロおよび開発者向けの小売ホーム ページ<ept id="p1">](https://docs.microsoft.com/dynamics365/unified-operations/retail/dev-itpro/dev-retail-home-page#payment-connectors)</ept> にアクセスしてください。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="139">
          <source>Setup</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">セットアップ</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="140">
          <source>The List PI capability requires the following components and setup steps:</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">リスト PI 機能には次のコンポーネントと設定手順が必要です:</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="141">
          <source><bpt id="p1">**</bpt>E-commerce integration<ept id="p1">**</ept> – An online storefront integration with Retail is required.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt"><bpt id="p1">**</bpt>電子商取引の統合<ept id="p1">**</ept> – オンライン ストアフロントと小売の統合が必要です。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="142">
          <source>For more information about the Retail e-Commerce SDK, see <bpt id="p1">[</bpt>e-Commerce platform software development kit (SDK)<ept id="p1">](https://docs.microsoft.com/dynamics365/unified-operations/retail/dev-itpro/ecommerce-platform-sdk)</ept>.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">小売の電子商取引 SDK の詳細は <bpt id="p1">[</bpt>電子商取引プラットフォーム ソフトウェア開発キット (SDK)<ept id="p1">](https://docs.microsoft.com/dynamics365/unified-operations/retail/dev-itpro/ecommerce-platform-sdk)</ept> を参照してください。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="143">
          <source><bpt id="p1">**</bpt>Online payments configuration<ept id="p1">**</ept> – The Dynamics 365 Payment Connector for Adyen supports List PI out of the box.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt"><bpt id="p1">**</bpt>オンライン支払コンフィギュレーション<ept id="p1">**</ept> – Adyen の Dynamics 365 支払コネクタは、そのままでリスト PI をサポートします。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="144">
          <source>For information about how to configure payments for online stores, see <bpt id="p1">[</bpt>Dynamics 365 Payment Connector for Adyen<ept id="p1">](https://docs.microsoft.com/dynamics365/unified-operations/retail/dev-itpro/adyen-connector?tabs=8-1-3#e-commerce)</ept>.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">オンライン ストアの支払いを構成する方法については <bpt id="p1">[</bpt>Adyen の Dynamics 365 支払コネクタ<ept id="p1">](https://docs.microsoft.com/dynamics365/unified-operations/retail/dev-itpro/adyen-connector?tabs=8-1-3#e-commerce)</ept> を参照してください。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="145">
          <source>In addition to completing the ecommerce setup steps that are described in that topic, you must set the <bpt id="p1">**</bpt>Allow saving payment information in e-commerce<ept id="p1">**</ept> option in the Payment accounts fasttab of the <bpt id="p2">**</bpt>Online store<ept id="p2">**</ept> form to <bpt id="p3">**</bpt>Yes<ept id="p3">**</ept>.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">このトピックで説明されている電子商取引の設定手順を完了することに加えて、<bpt id="p2">**</bpt>オンライン ストア<ept id="p2">**</ept> フォームの支払口座クイック タブの <bpt id="p1">**</bpt>電子商取引で支払情報の保存を許可する<ept id="p1">**</ept> オプションを <bpt id="p3">**</bpt>はい<ept id="p3">**</ept> に設定する必要があります。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="146">
          <source><bpt id="p1">**</bpt>Omni-channel payments configuration<ept id="p1">**</ept> – In the back office, go to <bpt id="p2">**</bpt>Retail <ph id="ph1">\&gt;</ph> Headquarters setup <ph id="ph2">\&gt;</ph> Parameters <ph id="ph3">\&gt;</ph> Retail shared parameters<ept id="p2">**</ept>.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt"><bpt id="p1">**</bpt>オムニ チャネルの支払コンフィギュレーション<ept id="p1">**</ept> – バック オフィスで <bpt id="p2">**</bpt>小売 <ph id="ph1">\&gt;</ph> 本社の設定 <ph id="ph2">\&gt;</ph> パラメーター <ph id="ph3">\&gt;</ph> 小売共有パラメーター<ept id="p2">**</ept> に移動します。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="147">
          <source>Then, on the <bpt id="p1">**</bpt>Omni-channel payments<ept id="p1">**</ept> tab, set the <bpt id="p2">**</bpt>Use omni-channel payments<ept id="p2">**</ept> option to <bpt id="p3">**</bpt>Yes<ept id="p3">**</ept>.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">次に <bpt id="p1">**</bpt>オムニ チャネルの支払<ept id="p1">**</ept> タブで <bpt id="p2">**</bpt>オムニ チャネルの支払を使用する<ept id="p2">**</ept> オプションを <bpt id="p3">**</bpt>はい<ept id="p3">**</ept> に設定します。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="148">
          <source>Functional experience</source><target logoport:matchpercent="68" state="translated" state-qualifier="fuzzy-match">機能のエクスペリエンス</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="149">
          <source>Guest checkout</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">ゲスト チェックアウト</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="150">
          <source>When e-commerce visitors choose to check out as guests, customer records aren't created during checkout, and the customers can't save payment instruments for their next visit.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">電子商取引の訪問者がゲストとしてチェックアウトを選択した場合、チェックアウト時に顧客レコードが作成されず、顧客は次の訪問時に支払手段を保存できません。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="151">
          <source>Named user checkout</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">名前付きユーザー チェックアウト</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="152">
          <source>When named users (signed-in customers) go to the payment step of the checkout process, they will experience the List PI capability.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">名前付きユーザー (サインインした顧客) が、チェックアウト プロセスの支払手順に進むとリスト PI 機能を経験します。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="153">
          <source>The first time that a named user checks out, a <bpt id="p1">**</bpt>Save for my next payment<ept id="p1">**</ept> check box appears in the section where credit card information is entered.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">名前付きユーザーが初めてチェックアウトしたとき、クレジットカード情報が入力されるセクションに <bpt id="p1">**</bpt>次回の支払のために保存する<ept id="p1">**</ept> チェック ボックスが表示されます。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="154">
          <source>Save for my next payment option</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">[次回の支払のために保存する] オプション</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="155">
          <source>If this check box is selected, when a new credit card is submitted for payment, the named user's unique customer ID is sent to the payment processor, and the credit card is securely saved and mapped to the that unique customer ID.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">このチェックボックスが選択された場合、支払のために新しいクレジットカードを送信すると、名前付きユーザーの一意の顧客 ID が支払プロセッサに送信され、クレジットカードが安全に保存されてその一意の顧客 ID にマップされます。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="156">
          <source>If the same customer signs in during future visits to the storefront, he or she will be able to select the same credit card for payment at checkout.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">同じ顧客が将来ストアフロントを訪れる際にサインインした場合、チェックアウト時の支払いに同じクレジットカードを選択ができます。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="157">
          <source>Previously saved payment instrument</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">以前に保存された支払手段</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="158">
          <source>Order fulfillment and processing</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">注文のフルフィルメントと処理</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="159">
          <source>E-Commerce orders where the customer applied a tender line by using the List PI capability work in the same way as orders that were created without using a saved card payment.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">顧客がリスト PI 機能を使用して支払/入金明細行を適用した電子商取引の注文は、保存されたカード支払を使用せずに作成された注文と同じように機能します。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="160">
          <source>From the standpoint of order processing and fulfillment, the two types of payment are indistinguishable.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">注文処理およびフルフィルメントの観点から 2 種類の支払を区別できません。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="161">
          <source>Details of eCommerce payment card tokenization</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">電子商取引の支払カード トークン化の詳細</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="162">
          <source>Standard flow</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">標準フロー</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="163">
          <source>In Retail e-Commerce integrations, the payment card is typically entered as part of the checkout process and is saved together with the order before finalization.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">小売の電子商取引の統合で、支払カードはチェックアウト プロセスの一部として通常は入力され、完了前の注文と共に保存されます。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="164">
          <source>The card details are entered directly on a payment acceptance page that a payment processor provides.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">カードの詳細は、支払プロセッサが提供する支払承認ページに直接入力されます。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="165">
          <source>After card details are entered and the customer moves on to the next step of the checkout process, the processor creates a token that is used later in the order creation process.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">カードの詳細を入力し、チェックアウト プロセスの次のステップに進むと、プロセッサが注文作成プロセスで使用するトークンを作成します。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="166">
          <source>When the customer finalizes the online order, the payment card token is sent to the payment processor as part of an authorization request.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">顧客がオンライン注文を終了すると、承認要求の一部として支払カード トークンが支払プロセッサに送信されます。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="167">
          <source>If the payment authorization request is successful, the payment processor replies by sending an authorization token.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">支払承認要求が成功した場合、支払プロセッサは承認トークンを送信して返信します。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="168">
          <source>This authorization token is saved together with the customer's order and is referenced when that order is fulfilled from the back office.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">この承認トークンは顧客の注文と共に保存され、その注文がバック オフィスから履行されるときに参照されます。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="169">
          <source>List PI flow</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">リスト PI のフロー</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="170">
          <source>The main difference between the standard flow and the List PI flow is that the customer doesn't have to enter the full credit card number.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">標準フローとリスト PI フローの主な違いは、顧客がクレジットカード番号を完全に入力する必要がないことです。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="171">
          <source>Instead, the customer just has to select a previously saved credit card and provide the Card Verification Value (CVV number).</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">代わりに顧客は以前に保存したクレジット カードを選択し、カード検証値 (CVV 番号) を提供するだけです。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="172">
          <source>If the customer provides the correct CVV number and moves on to the next step of the checkout process, the payment processor provides a payment card token that will be included in the authorization request.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">顧客が正しい CVV 番号を提供し、チェックアウト プロセスの次の手順に進むと、支払プロセッサが承認要求を含む支払カード トークンを提供します。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="173">
          <source>Related articles</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">関連記事</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="174">
          <source><bpt id="p1">[</bpt>Payments FAQ<ept id="p1">](https://docs.microsoft.com/dynamics365/unified-operations/retail/dev-itpro/payments-retail)</ept></source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">[</bpt>支払に関するよく寄せられる質問<ept id="p1">](https://docs.microsoft.com/dynamics365/unified-operations/retail/dev-itpro/payments-retail)</ept></target></trans-unit>
      </group>
    </body>
  </file>
</xliff>