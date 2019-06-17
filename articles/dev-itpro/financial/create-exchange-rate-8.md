<?xml version="1.0" encoding="UTF-8"?>
<xliff xmlns:logoport="urn:logoport:xliffeditor:xliff-extras:1.0" xmlns:tilt="urn:logoport:xliffeditor:tilt-non-translatables:1.0" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns="urn:oasis:names:tc:xliff:document:1.2" xmlns:xliffext="urn:microsoft:content:schema:xliffextensions" version="1.2" xsi:schemaLocation="urn:oasis:names:tc:xliff:document:1.2 xliff-core-1.2-transitional.xsd">
  <file datatype="xml" source-language="en-US" original="create-exchange-rate-8.md" target-language="ja-JP">
    <header>
      <tool tool-company="Microsoft" tool-version="1.0-7889195" tool-name="mdxliff" tool-id="mdxliff"/>
      <xliffext:skl_file_name>create-exchange-rate-8.005865.3da4544cbfdf1d6693696aec84f53737855b514a.skl</xliffext:skl_file_name>
      <xliffext:version>1.2</xliffext:version>
      <xliffext:ms.openlocfilehash>3da4544cbfdf1d6693696aec84f53737855b514a</xliffext:ms.openlocfilehash>
      <xliffext:ms.sourcegitcommit>574d4dda83dcab94728a3d35fc53ee7e2b90feb0</xliffext:ms.sourcegitcommit>
      <xliffext:ms.lasthandoff>05/22/2019</xliffext:ms.lasthandoff>
      <xliffext:ms.openlocfilepath>articles\dev-itpro\financial\create-exchange-rate-8.md</xliffext:ms.openlocfilepath>
    </header>
    <body>
      <group extype="content" id="content">
        <trans-unit xml:space="preserve" translate="yes" id="101" restype="x-metadata">
          <source>Create exchange rate providers in Finance and Operations version 8.0</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Finance and Operations バージョン 8.0 を使用した、為替レート プロバイダーの作成</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="102" restype="x-metadata">
          <source>This topic explains how to set up an exchange rate provider in Microsoft Dynamics 365 for Finance and Operations version 8.0 (April 2018).</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このトピックでは、Microsoft Dynamics 365 for Finance and Operations バージョン 8.0 (2018 年 4 月) で為替レート プロバイダーを設定する方法について説明します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="103">
          <source>Create exchange rate providers in Finance and Operations version 8.0</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Finance and Operations バージョン 8.0 を使用した為替レート プロバイダーの作成</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="104">
          <source>This topic describes the steps that are required in order to set up an exchange rate provider in Microsoft Dynamics 365 for Finance and Operations version 8.0 (April 2018).</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このトピックでは、Microsoft Dynamics 365 for Finance and Operations バージョン 8.0 (2018 年 4 月) で為替レート プロバイダーを設定するために必要なステップについて説明します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="105">
          <source>For the purpose of illustration, the OANDA exchange rate service is used throughout this topic.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">説明のために、このトピック全体で OANDA 為替レート サービスが使用されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="106">
          <source>By following the steps that are described in this topic, you can create a functional exchange rate provider.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このトピックで説明している手順に従って、機能為替レート プロバイダーを作成できます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="107">
          <source>The code is production code.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このコードは生産コードです。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="108">
          <source>You can find the source in the <bpt id="p1">**</bpt>ExchangeRateProviderOanda<ept id="p1">**</ept> class.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ソースは <bpt id="p1">**</bpt>ExchangeRateProviderOanda<ept id="p1">**</ept> クラスで見つけることができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="109">
          <source>You can reference that class as you read through this topic.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">必要に応じて、このトピックからそのクラスを参照することができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="110">
          <source>To request an OANDA test account and receive information about the OANDA exchange rate service, go to <ph id="ph1">&lt;https://developer.oanda.com/exchange-rates-api/&gt;</ph>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">OANDA テスト アカウントを要求し、OANDA 為替レートに関する情報を受け取るには、<ph id="ph1">&lt;https://developer.oanda.com/exchange-rates-api/&gt;</ph> にアクセスしてください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="111">
          <source>Terminology</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">用語</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="112">
          <source><bpt id="p1">**</bpt>Import currency exchange rates<ept id="p1">**</ept> – The process that retrieves exchange rates from exchange rate providers and imports them.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>現在の通貨為替レートをインポート<ept id="p1">**</ept> – 為替レート プロバイダーから為替レートを取得してインポートするプロセス。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="113">
          <source>This process is a system operation that supports batch processing.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このプロセスは、バッチ処理をサポートするシステム操作です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="114">
          <source><bpt id="p1">**</bpt>Exchange rate provider<ept id="p1">**</ept> – An X++ or C# class that is responsible for retrieving exchange rates from external sources.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>為替レート プロバイダー<ept id="p1">**</ept> - 外部ソースから為替レートを取得する担当の X++ または C# クラス。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="115">
          <source><bpt id="p1">**</bpt>Exchange rate provider registration<ept id="p1">**</ept> – The process of enabling an exchange rate provider so that it can be used.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>為替レート プロバイダー登録<ept id="p1">**</ept> - 使用できるように、為替レート プロバイダーを有効にするプロセス。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="116">
          <source>By default, exchange rate providers aren't registered when they are deployed.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">既定では、為替レート プロバイダーは配置されると登録されません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="117">
          <source><bpt id="p1">**</bpt>Exchange rate provider configuration<ept id="p1">**</ept> – The configuration settings of an exchange rate provider that determine how it will be used.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>為替レート プロバイダーのコンフィギュレーション<ept id="p1">**</ept>: 使用方法を決定する為替レート プロバイダーのコンフィギュレーション設定。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="118">
          <source><bpt id="p1">**</bpt>Exchange rate service<ept id="p1">**</ept> – A free or paid subscription service that provides a list of exchange rates that have been published.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>為替レート サービス<ept id="p1">**</ept> - 発行された為替レートの一覧を提供する無料または有料の定期売買サービス。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="119">
          <source>Foreign Exchange Rates Powered by OANDA is an example of a service that provides exchange rates.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">OANDA による外貨為替レートは、為替レートを提供するサービスの例です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="120">
          <source><bpt id="p1">**</bpt>The framework<ept id="p1">**</ept> – The import currency exchange rates framework that coordinates the retrieval of exchange rates from providers and appropriate storage of those exchange rates.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>フレームワーク<ept id="p1">**</ept> – プロバイダーからの為替レートの取得および、それら為替レートの適切なストレージを調整するインポート通貨の為替レートのフレームワーク。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="121">
          <source>Conceptual/class model</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">概念/クラス モデル</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="122">
          <source>The following illustration shows the main interfaces and classes that make up the exchange rate provider framework, and the relationships among them.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">次の図は、為替レート プロバイダーのフレームワークを構成する主なインターフェイスとクラス、およびそれらの関係を示しています。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="123">
          <source>New exchange rate providers should be implemented from the <bpt id="p1">**</bpt>IExchangeRateProvider<ept id="p1">**</ept> interface.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">新しい為替レート プロバイダーは、<bpt id="p1">**</bpt>IExchangeRateProvider<ept id="p1">**</ept> インターフェイスから実装されている必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="124">
          <source>Exchange rate providers are written in X++ or C#.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">為替レート プロバイダーは、X++ または C# で記述されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="125">
          <source>Because X++ is a .NET language, you can easily use the Microsoft .NET Framework.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">X++ は .NET 言語なので、 Microsoft .NET Framework を簡単に使用できます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="126">
          <source>All providers that are written in C# must be wrapped by an X++ class to be recognized as C# providers.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">C# で記述されているすべてのプロバイダーは C# プロバイダーとして認識された X++ クラスでラップする必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="127">
          <source>For example, the Central Bank of Europe exchange rate provider is a provider that Microsoft wrote in C#.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">たとえば、ヨーロッパ為替レート プロバイダーの中央銀行は Microsoft が C# で書き出したプロバイダーです。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="128">
          <source>It's wrapped by the <bpt id="p1">**</bpt>ExchangeRateProviderCBOE<ept id="p1">**</ept> X++ class.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>ExchangeRateProviderCBOE<ept id="p1">**</ept> X++ クラスによってラップされます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="129">
          <source><bpt id="p1">[</bpt><ph id="ph1">![</ph>Conceptual/class model of the exchange rate provider framework<ept id="p1">](./media/exchangerates.png)](./media/exchangerates.png)</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">[</bpt><ph id="ph1">![</ph>為替レート プロバイダー フレームワークの概念/クラス モデル<ept id="p1">](./media/exchangerates.png)](./media/exchangerates.png)</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="130">
          <source>Here are the interfaces and classes that are shown in the illustration:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">図で表示されるインターフェイスおよびクラスを次に示します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="131">
          <source><bpt id="p1">**</bpt>IExchangeRateProvider<ept id="p1">**</ept> – By implementing this interface, you enable the exchange rate provider framework to recognize a class as an exchange rate provider.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>IExchangeRateProvider<ept id="p1">**</ept> – このインタフェースを実装すると、為替レート プロバイダー フレームワークがクラスを為替レート プロバイダーとして認識できるようになります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="132">
          <source><bpt id="p1">**</bpt>IExchangeRateProviderFrameworkFactory<ept id="p1">**</ept> – This interface enables the exchange rate provider to construct various types of provider framework classes that represent some of the interfaces in the illustration.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>IExchangeRateProviderFrameworkFactory<ept id="p1">**</ept> – このインターフェイスにより、為替レート プロバイダーは、図の中のいくつかのインターフェイスを表す様々なタイプのプロバイダー フレームワーク クラスを作成することができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="133">
          <source><bpt id="p1">**</bpt>IExchangeRateProviderSupportedOptions<ept id="p1">**</ept> – The exchange rate provider supports several options when rates are imported.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>IExchangeRateProviderSupportedOptions<ept id="p1">**</ept> – 為替レート プロバイダーは、レートをインポートする際にいくつかのオプションをサポートします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="134">
          <source>The exchange rate provider uses this interface to inform the framework about the options that it supports.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">為替レート プロバイダーは、このインターフェイスを使用して、サポートするオプションについてフレームワークに通知します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="135">
          <source><bpt id="p1">**</bpt>IExchangeRateProviderConfig<ept id="p1">**</ept> – Each exchange rate provider can have a unique configuration.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>IExchangeRateProviderConfig<ept id="p1">**</ept> – 各為替レート プロバイダーは、固有のコンフィギュレーションを持つことができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="136">
          <source>This interface enables the provider to retrieve this configuration.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このインターフェイスにより、プロバイダーはこの構成を取得できます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="137">
          <source><bpt id="p1">**</bpt>IExchangeRateProviderConfigDefaults<ept id="p1">**</ept> – The exchange rate provider can create and provide default values for its configuration.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>IExchangeRateProviderConfigDefaults<ept id="p1">**</ept> – 為替レート プロバイダーは、構成のデフォルト値を作成して提供できます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="138">
          <source>Users can change these values on the <bpt id="p1">**</bpt>Configure exchange rate providers<ept id="p1">**</ept> page (<bpt id="p2">**</bpt>General ledger<ept id="p2">**</ept> <ph id="ph1">&amp;gt;</ph> <bpt id="p3">**</bpt>Currencies<ept id="p3">**</ept> <ph id="ph2">&amp;gt;</ph> <bpt id="p4">**</bpt>Configure exchange rate providers<ept id="p4">**</ept>).</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>為替レート プロバイダの構成<ept id="p1">**</ept> ページ (<bpt id="p2">**</bpt>総勘定元帳<ept id="p2">**</ept> <ph id="ph1">&amp;gt;</ph> <bpt id="p3">**</bpt>為替<ept id="p3">**</ept> <ph id="ph2">&amp;gt;</ph> <bpt id="p4">**</bpt>レート プロバイダーの構成<ept id="p4">**</ept>)でこれらの値を変更できます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="139">
          <source><bpt id="p1">**</bpt>IExchangeRateRequest<ept id="p1">**</ept> – This interface represents data that is specific to a request to import exchange rates.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>IExchangeRateRequest<ept id="p1">**</ept> – このインターフェイスは、為替レートのインポートを要求する固有のデータを表します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="140">
          <source>This data includes the date range, options, and the currency pairs to retrieve rates for.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このデータには、日付範囲、オプション、レートを取得するための通貨ペアが含まれます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="141">
          <source><bpt id="p1">**</bpt>IExchangeRateCalendar<ept id="p1">**</ept> – This interface represents an exchange rate calendar that is used to retrieve the next working day (Monday through Friday).</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>IExchangeRateCalendar<ept id="p1">**</ept> – このインターフェイスは、次の作業日 (月曜日から金曜日まで) を取得する場合に使用される為替レート カレンダーを表します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="142">
          <source><bpt id="p1">**</bpt>IExchangeRateResponse<ept id="p1">**</ept> – The exchange rate provider uses this interface to store the currency pairs and the exchange rates that are returned from the service.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>IExchangeRateResponse<ept id="p1">**</ept> – 為替レート プロバイダーでは、このインターフェイスを使用して、通貨のペアや、サービスから返される為替レートを格納します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="143">
          <source><bpt id="p1">**</bpt>IExchangeRateResponseCurrencyPair<ept id="p1">**</ept> – The exchange rate provider uses this interface to store the details for a specific currency pair that is returned from the service.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>IExchangeRateResponseCurrencyPair<ept id="p1">**</ept> – 為替レート プロバイダーでは、このインターフェイスを使用して、サービスから返される特定の通貨ペアの詳細を格納します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="144">
          <source><bpt id="p1">**</bpt>IExchangeRateResponseExchangeRate<ept id="p1">**</ept> – The exchange rate provider uses this interface to store a specific exchange rate for a specific currency pair.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>IExchangeRateResponseExchangeRate<ept id="p1">**</ept> – 為替レート プロバイダーでは、このインターフェイスを使用して、特定の通貨ペアに対して特定の為替レートを格納します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="145">
          <source><bpt id="p1">**</bpt>ExchangeRateProviderOanda<ept id="p1">**</ept> – This example of an exchange rate provider that is implemented by Microsoft connects to the OANDA service to return exchange rates.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>ExchangeRateProviderOanda<ept id="p1">**</ept> - Microsoft によって実装されている為替レート プロバイダーのこの例は、為替レートを返すために OANDA サービスに接続します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="146">
          <source>Write an exchange rate provider</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">為替レート プロバイダーの記述</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="147">
          <source>Follow these steps to create an exchange rate provider.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">為替レート プロバイダーを作成するには、これらの手順に従います。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="148">
          <source>The code examples are taken from the <bpt id="p1">**</bpt>ExchangeRateProviderOanda<ept id="p1">**</ept> class.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このコード例は、<bpt id="p1">**</bpt>ExchangeRateProviderOanda<ept id="p1">**</ept> クラスから取得されています。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="149">
          <source>Use extensions to add a new value to the <bpt id="p1">**</bpt>ExchangeRateProvider<ept id="p1">**</ept> extensible enum to represent your new exchange rate provider.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">拡張機能を使用して、新しい為替レート プロバイダーを表す <bpt id="p1">**</bpt>ExchangeRateProvider<ept id="p1">**</ept> の拡張可能列挙体に新しい値を追加します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="150">
          <source>In your development model, create a class that implements the <bpt id="p1">**</bpt>IExchangeRateProvider<ept id="p1">**</ept> interface.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">開発モデルで、<bpt id="p1">**</bpt>IExchangeRateProvider<ept id="p1">**</ept> インターフェイスを実装するクラスを作成します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="151">
          <source>Add the following constants and variable declarations to the class.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">クラスに、次の定数と変数宣言を追加します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="152">
          <source>Provide your own unique globally unique identifier (GUID) for <bpt id="p1">**</bpt>ProviderId<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>ProviderId<ept id="p1">**</ept> の独自のグローバル一意識別子 (GUID) を提供します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="153">
          <source>Implement the <bpt id="p1">**</bpt>get<ph id="ph1">\_</ph>Name<ept id="p1">**</ept> method.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>get<ph id="ph1">\_</ph>Name<ept id="p1">**</ept> メソッドを実装します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="154">
          <source>You should use a label to enable correct translation.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ラベルを使用して、正しい変換を有効にする必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="155">
          <source>When users set up the provider's configuration information, they can change the name that is provided here.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ユーザーは、プロバイダーの構成情報を設定すると、ここで指定されている名前を変更できます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="156">
          <source>Implement the <bpt id="p1">**</bpt>get<ph id="ph1">\_</ph>Id<ept id="p1">**</ept> method.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>get<ph id="ph1">\_</ph>Id<ept id="p1">**</ept> メソッドを実装します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="157">
          <source>This method returns a GUID that uniquely identifies this provider.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このメソッドは、このプロバイダーを一意に識別する GUID を返します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="158">
          <source>Implement the <bpt id="p1">**</bpt>set<ph id="ph1">\_</ph>Factory<ept id="p1">**</ept> method.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>set<ph id="ph1">\_</ph>Factory<ept id="p1">**</ept> メソッドを実装します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="159">
          <source>The exchange rate provider framework will invoke this method to set an object that implements the <bpt id="p1">**</bpt>IExchangeRateProviderFrameworkFactory<ept id="p1">**</ept> interface on your provider.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">為替レート プロバイダー フレームワークは、このメソッドを呼び出して、プロバイダーの <bpt id="p1">**</bpt>IExchangeRateProviderFrameworkFactory<ept id="p1">**</ept> インターフェイスを実装するオブジェクトを設定します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="160">
          <source>This factory can be used to instantiate new objects that represent some of the interfaces from the previous illustration.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このファクトリを使用して、前の図のインターフェイスの一部を表す新しいオブジェクトのインスタンスを作成できます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="161">
          <source>Implement the <bpt id="p1">**</bpt>GetSupportedOptions<ept id="p1">**</ept> method.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>GetSupportedOptions<ept id="p1">**</ept> メソッドを実装します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="162">
          <source>This method indicates whether the exchange rate provider supports some framework features.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このメソッドは、為替レート プロバイダーは、一部のフレームワーク機能をサポートするかどうかを示します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="163">
          <source>Set the <bpt id="p1">**</bpt>doesSupportSpecificCurrencyPairs<ept id="p1">**</ept> property to <bpt id="p2">**</bpt>true<ept id="p2">**</ept> only if the exchange rate service requires that a source currency and a destination currency be passed to get an exchange rate.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">為替レートを取得するために渡すソース通貨およびターゲット通貨を渡すことが為替レート サービスに必要な場合にのみ、<bpt id="p1">**</bpt>doesSupportSpecificCurrencyPairs<ept id="p1">**</ept> プロパティを <bpt id="p2">**</bpt>true<ept id="p2">**</ept> に設定します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="164">
          <source>Many exchange rate services return rates for a fixed currency or a given set of currency pairs.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">多くの為替レート サービスが、固定通貨または通貨ペアの指定されたセットを返します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="165">
          <source>For these services, this property should be set to <bpt id="p1">**</bpt>false<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">これらのサービスについては、このプロパティは <bpt id="p1">**</bpt>false<ept id="p1">**</ept> に設定されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="166">
          <source>If the prices that a service charges are based on quotas on the number of rates, a value of <bpt id="p1">**</bpt>true<ept id="p1">**</ept> will cause the <bpt id="p2">**</bpt>IExchangeRateRequest<ept id="p2">**</ept> interface to contain only those currency pairs that are configured for an exchange rate type on the <bpt id="p3">**</bpt>Exchange rate<ept id="p3">**</ept> page (<bpt id="p4">**</bpt>General ledger<ept id="p4">**</ept> <ph id="ph1">&amp;gt;</ph> <bpt id="p5">**</bpt>Currencies<ept id="p5">**</ept> <ph id="ph2">&amp;gt;</ph> <bpt id="p6">**</bpt>Exchange rates<ept id="p6">**</ept>).</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">サービス料金が課金された料金の数がクォータ数に基づく場合、<bpt id="p1">**</bpt>true<ept id="p1">**</ept> の値により、<bpt id="p2">**</bpt>IExchangeRateRequest<ept id="p2">**</ept> インターフェイスには、<bpt id="p3">**</bpt>為替レート<ept id="p3">**</ept> ページ (<bpt id="p4">**</bpt>総勘定元帳<ept id="p4">**</ept> <ph id="ph1">&amp;gt;</ph> <bpt id="p5">**</bpt>通貨<ept id="p5">**</ept> <ph id="ph2">&amp;gt;</ph> <bpt id="p6">**</bpt>為替レート<ept id="p6">**</ept>) の為替レート タイプに設定されている通貨ペアのみを含まれるようになります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="167">
          <source>The provider can then specifically request these rates from the service and therefore lower the cost.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">プロバイダーはその後、これらの料金をサービスから具体的に要求できるため、コストを削減できます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="168">
          <source>Set the <bpt id="p1">**</bpt>fixedBaseIsoCurrency<ept id="p1">**</ept> property to the three-character International Organization for Standardization (ISO) currency code that represents the fixed base currency of the exchange rates that are returned from the exchange rate service.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>fixedBaseIsoCurrency<ept id="p1">**</ept> プロパティを、為替レート サービスから返される為替レートの固定ベース通貨を表す 3 文字の国際標準化機構 (ISO) 通貨コードに設定します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="169">
          <source>If the exchange rate service doesn't support a fixed base currency, return an empty string.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">為替レート サービスが固定基本通貨をサポートしていない場合は、空の文字列を返します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="170">
          <source>For example, the euro is often used as a fixed base currency.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">たとえば、ユーロは固定基本通貨としてよく使用されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="171">
          <source>When you create a new provider, be sure to research the exchange rate service so that you can select the correct value.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">新しいプロバイダーを作成するときは、正しい値を選択できるように、為替レート サービスをかならず調査してください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="172">
          <source>Set the <bpt id="p1">**</bpt>singleRateForDateRange<ept id="p1">**</ept> property to <bpt id="p2">**</bpt>true<ept id="p2">**</ept> if the service can return a single rate that represents the whole date range.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">サービスが日付範囲全体を表す単一のレートを返すことができる場合、<bpt id="p1">**</bpt>singleRateForDateRange<ept id="p1">**</ept> プロパティを <bpt id="p2">**</bpt>true<ept id="p2">**</ept> に設定します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="173">
          <source>For example, you can use this setting to return a single exchange rate that represents the average exchange rate for a month.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">たとえば、1 か月の平均為替レートを表す単一の為替レートを返すには、この設定を使用できます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="174">
          <source>If the service doesn't support this functionality, set this property to <bpt id="p1">**</bpt>false<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">サービスがこの機能をサポートしていない場合は、このプロパティを <bpt id="p1">**</bpt>false<ept id="p1">**</ept> に設定します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="175">
          <source>Implement the <bpt id="p1">**</bpt>GetConfigurationDefaults<ept id="p1">**</ept> method.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>GetConfigurationDefaults<ept id="p1">**</ept> メソッドを実装します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="176">
          <source>Configuration defaults are name-value pairs that represent the default configuration settings for the exchange rate provider.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">既定のコンフィギュレーションは、為替レート プロバイダの既定コンフィギュレーションの設定を表す名前と値の組です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="177">
          <source>These settings are automatically loaded when the provider is registered, but users can change them.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">これらの設定はプロバイダーが登録されたときに自動的に読み込まれますが、ユーザーは変更できます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="178">
          <source>Take the necessary precautions when you convert these strings into usable values.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">これらの文字列を使用可能な値に変換する場合は、必要な対策を講じてください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="179">
          <source>The value field is stored as an encrypted field in SQL.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">値フィールドは、SQL で暗号化フィールドとして格納されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="180">
          <source>Therefore, sensitive data such as an application programming interface (API) key will be more secure.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">したがって、アプリケーション プログラミング インターフェイス (API) などの機密データはより安全になります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="181">
          <source>Implement the <bpt id="p1">**</bpt>ValidateConfigurationDetail<ept id="p1">**</ept> method.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>ValidateConfigurationDetail<ept id="p1">**</ept> メソッドを実装します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="182">
          <source>This method enables the exchange rate provider to validate the configuration information that the user modifies on the <bpt id="p1">**</bpt>Configure exchange rate providers<ept id="p1">**</ept> page.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このメソッドにより、為替レート プロバイダーは、<bpt id="p1">**</bpt>為替レート プロバイダーの構成<ept id="p1">**</ept>ページでユーザーが変更する構成情報を検証できます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="183">
          <source>Implement the <bpt id="p1">**</bpt>EnumNameForLookup<ept id="p1">**</ept> method.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>EnumNameForLookup<ept id="p1">**</ept> メソッドを実装します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="184">
          <source>This method enables the exchange rate provider to enable a lookup for a specific <bpt id="p1">**</bpt>ExchangeRateProviderPropertyKey<ept id="p1">**</ept> key.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このメソッドは、為替レート プロバイダーが特定の <bpt id="p1">**</bpt>ExchangeRateProviderPropertyKey<ept id="p1">**</ept> キーを参照できるようにします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="185">
          <source>Just return the name of an existing enumerated type for the appropriate key.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">適切なキーに対して列挙された既存の型の名前を返します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="186">
          <source>If this feature isn't required, return an empty string.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この機能が必要でない場合は、空の文字列を返します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="187">
          <source>Implement the <bpt id="p1">**</bpt>GetExchangeRates<ept id="p1">**</ept> method.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>GetExchangeRates<ept id="p1">**</ept> メソッドを実装します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="188">
          <source>This method uses the configuration information and the <bpt id="p1">**</bpt>IExchangeRateRequest<ept id="p1">**</ept> interface that is provided to call out to the exchange rate service and return the appropriate instance of the <bpt id="p2">**</bpt>IExchangeRateResponse<ept id="p2">**</ept> class.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このメソッドは、構成情報と、<bpt id="p1">**</bpt>IExchangeRateRequest<ept id="p1">**</ept> インターフェイスを使用して、交換レート サービスを呼び出すとともに、<bpt id="p2">**</bpt>IExchangeRateResponse<ept id="p2">**</ept> クラスの適切なインスタンスを返します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="189">
          <source>When you write this method, consider these important points:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このメソッドを記述するときは、以下の重要な点を考慮します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="190">
          <source>Any configuration information that is required should be retrieved from the <bpt id="p1">**</bpt>IExchangeRateProviderConfig<ept id="p1">**</ept> interface.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">必要なすべてのコンフィギュレーション情報は <bpt id="p1">**</bpt>IExchangeRateProviderConfig<ept id="p1">**</ept> インターフェイスから取得する必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="191">
          <source>A call to the <bpt id="p1">**</bpt>GetPropertyValue<ept id="p1">**</ept> method on that interface will provide the string representation of the property value for the property key that is provided.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">そのインターフェイスの<bpt id="p1">**</bpt>GetPropertyValue<ept id="p1">**</ept>メソッドへの呼び出しは、入力されたプロパティキーのプロパティ値の文字列形式を提供します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="192">
          <source>Take the required precautions when you convert this string value to another type.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この文字列値を別の型に変換する場合は、必要な対策を講じてください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="193">
          <source>Do any required validation up front.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">事前に必要な検証を行います。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="194">
          <source>For example, OANDA requires that an API key be supplied on every service call.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">たとえば、OANDA は、すべてのサービス コールで API キーを指定するよう要求します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="195">
          <source>If this API key isn't set, the service will fail.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この API キーが設定されていない場合は、サービスが失敗します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="196">
          <source>Verify that if the API key isn't set then, throw the appropriate error message to exit prior to importing rates.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">API キーが設定されていない場合は、料金をインポートする前に終了するよう適切なエラー メッセージを表示することを確認します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="197">
          <source>Some providers require explicit currency pairs when exchange rates are requested.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">一部のプロバイダーには、為替レートが要求される場合に明示的な通貨の組み合わせが必要です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="198">
          <source>These providers are the same providers that set the <bpt id="p1">**</bpt>IExchangeRateProviderSupportedOptions.doesSupportSpecificCurrencyPairs<ept id="p1">**</ept> property to <bpt id="p2">**</bpt>true<ept id="p2">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">これらのプロバイダーは、<bpt id="p1">**</bpt>IExchangeRateProviderSupportedOptions.doesSupportSpecificCurrencyPairs<ept id="p1">**</ept> プロパティを <bpt id="p2">**</bpt>true<ept id="p2">**</ept> に設定したプロバイダーと同じです。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="199">
          <source>In this case, you must use the currency pairs that the <bpt id="p1">**</bpt>IExchangeRateRequest<ept id="p1">**</ept> interface provides to drive the retrieval process.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この場合、<bpt id="p1">**</bpt>IExchangeRateRequest<ept id="p1">**</ept> インターフェイスが提示する通貨ペアを使用して、取得プロセスを動作させる必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="200">
          <source>The OANDA provider implementation that follows shows a good example of this type of provider.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">後に続く OANDA プロバイダーの実装には、このタイプのプロバイダーの適正例が示されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="201">
          <source>Typically, providers that don't support specific currency pairs return data for a fixed set of currency pairs.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">通常、特定の通貨の組み合わせをサポートしていないプロバイダーは、固定された通貨の組み合わせのデータを返します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="202">
          <source>In this case, the currency pairs that the <bpt id="p1">**</bpt>IExchangeRateRequest<ept id="p1">**</ept> interface provides can be ignored.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この場合、<bpt id="p1">**</bpt>IExchangeRateRequest<ept id="p1">**</ept> インターフェイスが提示する通貨ペアは無視できます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="203">
          <source>Providers should return all the rates that are available.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">プロバイダーは、使用できるすべてのレートを返す必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="204">
          <source>The framework will then import the correct rates, based on the user's decision about whether to automatically create the required currency pairs.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このフレームワークは、必要な通貨ペアを自動的に作成するかどうかに関するユーザーの決定に基づいて、正しいレートをインポートします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="205">
          <source>The CentralBankOfEuropeProvider provider is a good example of this type of provider.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">CentralBankOfEuropeProvider プロバイダーは、このタイプのプロバイダーの適切な例です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="206">
          <source>The <bpt id="p1">**</bpt>IExchangeRateRequest<ept id="p1">**</ept> interface has a property that is named <bpt id="p2">**</bpt>ImportDateType<ept id="p2">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>IExchangeRateRequest<ept id="p1">**</ept> インターフェイスには、<bpt id="p2">**</bpt>ImportDateType<ept id="p2">**</ept> というプロパティがあります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="207">
          <source>This property indicates the dates that should be used to retrieve exchange rates from the service.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このプロパティは、サービスから為替レートを取得するために使用する日付を示します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="208">
          <source>The two values that are available are <bpt id="p1">**</bpt>CurrentDate<ept id="p1">**</ept> and <bpt id="p2">**</bpt>DateRange<ept id="p2">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">利用可能な 2 つの値は、<bpt id="p1">**</bpt>CurrentDate<ept id="p1">**</ept> と <bpt id="p2">**</bpt>DateRange<ept id="p2">**</ept> です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="209">
          <source><bpt id="p1">**</bpt>CurrentDate<ept id="p1">**</ept> retrieves the most current exchange rate from the exchange rate service.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>CurrentDate<ept id="p1">**</ept> は、為替レート サービスから最新の為替レートを取得します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="210">
          <source>When this value is passed to the provider, the framework also sets <bpt id="p1">**</bpt>IExchangeRateRequest.FromDate<ept id="p1">**</ept> and <bpt id="p2">**</bpt>IExchangeRateRequest.ToDate<ept id="p2">**</ept> to the system date of the Application Object Server (AOS) computer that is making the request.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">また、プロバイダーにこの値が渡されると、フレームワークは、<bpt id="p1">**</bpt>IExchangeRateRequest.FromDate<ept id="p1">**</ept> および <bpt id="p2">**</bpt>IExchangeRateRequest.ToDate<ept id="p2">**</ept> を、要求している Application Object Server (AOS) コンピュータのシステム日付に設定します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="211">
          <source>If exchange rate services support the retrieval of exchange rates for specific dates, the date that the framework provides should be passed.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">為替レート サービスでは、特定の日付の為替レートの取得をサポート、フレームワークが提供する日付を渡す必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="212">
          <source>However, if the exchange rate service instead provides a call to get the most current exchange rate (regardless of the date), the date that is returned must be validated to make sure that it's less than or equal to the requested date.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ただし、代わりに為替レート サービスが最新の為替レート (日付に関係なく) を取得する呼び出しを提供する場合、返される日付が要求日より前または同じ日付であることを確認するよう検証する必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="213">
          <source><bpt id="p1">**</bpt>DateRange<ept id="p1">**</ept> retrieves the exchange rates for a specific date range.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>DateRange<ept id="p1">**</ept> は、特定の日付範囲の為替レートを取得します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="214">
          <source>Only exchange rates in the specified date range should be allowed.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">指定された日付範囲内の為替レートのみ許可される必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="215">
          <source>If an exchange rate service requires that specific dates be included in the request, this process is straightforward.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">為替レート サービスで、特定の日付が要求に含まれることが必要とされる場合は、このプロセスは簡単です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="216">
          <source>However, if an exchange rate service instead returns a group of historical dates that might be outside the valid range of dates, the provider must filter out the dates that aren't relevant before it passes the dates back to the framework.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ただし、代わりに為替レート サービスが有効日の範囲外の可能性がある履歴日付のグループを返す場合、プロバイダーはフレームワークに日付を戻す前に該当しない日付を除外する必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="217">
          <source>When exchange rates are returned, always use the date that the exchange rate service provides instead of the dates that the instance of the <bpt id="p1">**</bpt>IExchangeRateRequest<ept id="p1">**</ept> class supplies.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">為替レートが返されるときは、<bpt id="p1">**</bpt>IExchangeRateRequest<ept id="p1">**</ept> クラスのインスタンスが提供する日付ではなく、為替レート サービスが提供する日付を常に使用します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="218">
          <source>In this way, you help guarantee that the exchange rate that is returned is associated with the correct date, because an exchange rate service might occasionally return rates for dates that weren't expected.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この方法では、為替レート サービスが予期されていない日付のレートを返す場合があるため、返される為替レートが正しい日付に関連付けられていることを保証できます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="219">
          <source>For example, if an exchange rate is requested for a date in the future, some providers return the most recent exchange rate instead of throwing an error or returning nothing.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">たとえば、将来の日付に対して為替レートが要求されると、一部のプロバイダーは、エラーをスローしたり何も返さない代わりに、最新の為替レートを返します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="220">
          <source>If you encounter errors when you try to retrieve exchange rates from the exchange rate service, don't throw custom error messages.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">為替レート サービスからの為替レートを取得するときにエラーが発生する場合は、カスタム エラー メッセージをスローしないようにします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="221">
          <source>The framework will alert the user that there is an issue by throwing generic error messages that state that the expected currency pairs could not be retrieved from the provider.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このフレームワークは、予想される通貨ペアをプロバイダーから取得できないという一般的なエラーメッセージを投げて問題があることをユーザーに警告します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="222">
          <source>If you must log additional errors, use <bpt id="p1">**</bpt>CurrencyEventSource<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">その他のエラーのログを記録する必要がある場合、<bpt id="p1">**</bpt>CurrencyEventSource<ept id="p1">**</ept> を使用します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="223">
          <source>For an example, see the <bpt id="p1">**</bpt>catch<ept id="p1">**</ept> statement and the <bpt id="p2">**</bpt>if<ept id="p2">**</ept> condition for the <bpt id="p3">**</bpt>oandaKey<ept id="p3">**</ept> variable in the following code.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">例については、次のコードで <bpt id="p1">**</bpt>catch<ept id="p1">**</ept> ステートメントおよび <bpt id="p3">**</bpt>oandaKey<ept id="p3">**</ept> 変数に対する <bpt id="p2">**</bpt>IF<ept id="p2">**</ept> 条件を参照してください。。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="224">
          <source>Implement the following helper methods.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">次のヘルパー メソッドを実装します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="225">
          <source>These methods are specific to this example and aren't required for every provider.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">これらのメソッドはこの例に固有のものであり、すべてのプロバイダーに必須ではありません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="226">
          <source>Compile the <bpt id="p1">**</bpt>ExchangeRateProviderOanda<ept id="p1">**</ept> class.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>ExchangeRateProviderOanda<ept id="p1">**</ept> クラスをコンパイルします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="227">
          <source>The provider will be run as part of a SysOperation.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">プロバイダーは、SysOperation の一部として実行されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="228">
          <source>It's helpful to understand the following framework classes and methods when you debug issues:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">問題をデバッグするときに、次のフレームワーク クラスおよびメソッドを理解しておくと便利です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="229">
          <source><bpt id="p1">**</bpt>ExchangeRateProviderFactory.initialize()<ept id="p1">**</ept> – This method creates instances of the exchange rate providers, and is called when exchange rates are registered or imported.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>ExchangeRateProviderFactory.initialize()<ept id="p1">**</ept> - このメソッドは、為替レート プロバイダーのインスタンスを作成し、為替レートの登録またはインポート時に呼び出されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="230">
          <source>If your provider isn't instantiated, start to debug here.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">プロバイダーにインスタンスが作成されていない場合、ここでデバッグを開始します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="231">
          <source><bpt id="p1">**</bpt>ExchangeRateProviderRegistration.initialize()<ept id="p1">**</ept> – This method searches for providers, so that they can be registered.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>ExchangeRateProviderRegistration.initialize()<ept id="p1">**</ept> - このメソッドはプロバイダーを検索し、プロバイダーを登録できるようにします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="232">
          <source>If you can't see your provider on the registration page, start to debug here.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">登録ページでプロバイダーがわからない場合は、ここでデバッグを開始します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="233">
          <source><bpt id="p1">**</bpt>ExchangeRateImportOperation.import()<ept id="p1">**</ept> – This method drives the import process by calling the required provider and storing the exchange rates.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>ExchangeRateImportOperation.import()<ept id="p1">**</ept> - このメソッドでは、必要なプロバイダーを呼び出して為替レートを保存することによって、インポート プロセスを駆動します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="234">
          <source><bpt id="p1">**</bpt>ExchangeRateProviderConfig<ept id="p1">**</ept> – This class provides access to configuration information for the providers.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>ExchangeRateProviderConfig<ept id="p1">**</ept> - このクラスはプロバイダーのコンフィギュレーション情報へのアクセスを提供します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="235">
          <source>Ideas to consider</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">考慮する必要があるアイデア</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="236">
          <source>Because there are no limits to the methods that exchange rate providers use to get exchange rates, the framework enables some interesting scenarios.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">為替レートの取得には為替レートのプロバイダーが使用するメソッドに制限がないため、このフレームワークはいくつかの興味深いシナリオを有効にします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="237">
          <source>Here are some ideas that you might want to explore:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">参照するアイデアを次に示します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="238">
          <source><bpt id="p1">**</bpt>Providers that retrieve exchange rates from other exchange rate types<ept id="p1">**</ept> – If you implement this scenario, it will enable synchronization of exchange rates among various exchange rate types.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>他の為替レート タイプからの為替レートを取得するプロバイダー<ept id="p1">**</ept> – このシナリオを実装すると、さまざまな為替レート タイプ間の為替レートの同期が可能になります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="239">
          <source>This functionality can be useful in situations where many exchange rate types exist, because it will help maintain isolation between different ledgers.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この機能は、さまざまな元帳間の分離を維持するために、多くの為替レート タイプが存在する状況で役立ちます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="240">
          <source><bpt id="p1">**</bpt>Providers that use Extensible Stylesheet Language Transformations (XSLT) to transform any format for an exchange rate service into an instance of the ExchangeRateResponse class<ept id="p1">**</ept> – If you implement this scenario, users can add the XSLT transform that is required for their exchange rate service, and the application will support the service.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>為替レート サービスの任意の形式を ExchangeRateResponse クラスのインスタンスに変換するために Extensible Stylesheet Language Transformations (XSLT) を使用するプロバイダー<ept id="p1">**</ept> – このシナリオを実装すると、ユーザーは為替レート サービスに必要な XSLT 変換を追加することができ、アプリケーションはそのサービスをサポートします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="241">
          <source>Provider-specific code isn't required.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">プロバイダー固有のコードは必要ありません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="242">
          <source><bpt id="p1">**</bpt>Some exchange rate provider services charge for every rate that is consumed<ept id="p1">**</ept> – Consider combining the first idea in this list with a limit on the number of rates that you retrieve from the service.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>一部の為替レート プロバイダー サービスは、消費されるすべてのレートに対して料金を請求します<ept id="p1">**</ept> – このリストの最初のアイデアと、サービスから取得するレートの数の制限を組み合わせることを検討してください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="243">
          <source>This functionality can be useful for scenarios where you're charged for each rate that is consumed from the service.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この機能は、サービスから消費される料金ごとに課金されるシナリオに役立ちます。</target></trans-unit>
      </group>
    </body>
  </file>
</xliff>