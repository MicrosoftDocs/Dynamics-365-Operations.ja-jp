---
title: "Finance and Operations バージョン 8.0 を使用した、為替レート プロバイダーの作成"
description: "このトピックでは、Microsoft Dynamics 365 for Finance and Operations バージョン 8.0 (2018年4月) で為替レート プロバイダーを設定する方法について説明します。"
author: aolson
manager: AnnBe
ms.date: 04/02/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Developer
ms.reviewer: shylaw
ms.search.scope: Operations
ms.custom: 72153
ms.assetid: 24643037-f7a5-4acf-b3d6-9943642b618c
ms.search.region: Global
ms.author: jbye
ms.search.validFrom: 2018-04-02
ms.dyn365.ops.version: AX 8.0.0
ms.translationtype: HT
ms.sourcegitcommit: d9747ba144d56c9410846769e5465372c89ea111
ms.openlocfilehash: 13d14e4a11ff43668233dcce6fc1b305080a8c43
ms.contentlocale: ja-jp
ms.lasthandoff: 08/09/2018

---

# <a name="create-exchange-rate-providers-in-finance-and-operations-version-80"></a><span data-ttu-id="49658-103">Finance and Operations バージョン 8.0 を使用した、為替レート プロバイダーの作成</span><span class="sxs-lookup"><span data-stu-id="49658-103">Create exchange rate providers in Finance and Operations version 8.0</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="49658-104">このトピックでは、Microsoft Dynamics 365 for Finance and Operations バージョン 8.0 (2018年4月) で為替レート プロバイダーを設定するのに必要な手順について説明します。</span><span class="sxs-lookup"><span data-stu-id="49658-104">This topic describes the steps that are required in order to set up an exchange rate provider in Microsoft Dynamics 365 for Finance and Operations version 8.0 (April 2018).</span></span> <span data-ttu-id="49658-105">説明のために、このトピック全体で OANDA 為替レート サービスが使用されます。</span><span class="sxs-lookup"><span data-stu-id="49658-105">For the purpose of illustration, the OANDA exchange rate service is used throughout this topic.</span></span>

<span data-ttu-id="49658-106">このトピックで説明している手順に従って、機能為替レート プロバイダーを作成できます。</span><span class="sxs-lookup"><span data-stu-id="49658-106">By following the steps that are described in this topic, you can create a functional exchange rate provider.</span></span> <span data-ttu-id="49658-107">このコードは生産コードです。</span><span class="sxs-lookup"><span data-stu-id="49658-107">The code is production code.</span></span> <span data-ttu-id="49658-108">ソースは **ExchangeRateProviderOanda** クラスで見つけることができます。</span><span class="sxs-lookup"><span data-stu-id="49658-108">You can find the source in the **ExchangeRateProviderOanda** class.</span></span> <span data-ttu-id="49658-109">必要に応じて、このトピックからそのクラスを参照することができます。</span><span class="sxs-lookup"><span data-stu-id="49658-109">You can reference that class as you read through this topic.</span></span>

<span data-ttu-id="49658-110">OANDA テスト アカウントを要求し、OANDA 為替レートに関する情報を受け取るには、<http://developer.oanda.com/exchange-rates-api/> にアクセスしてください。</span><span class="sxs-lookup"><span data-stu-id="49658-110">To request an OANDA test account and receive information about the OANDA exchange rate service, go to <http://developer.oanda.com/exchange-rates-api/>.</span></span>

## <a name="terminology"></a><span data-ttu-id="49658-111">用語</span><span class="sxs-lookup"><span data-stu-id="49658-111">Terminology</span></span>
- <span data-ttu-id="49658-112">**現在の通貨為替レートをインポート** – 為替レート プロバイダーから為替レートを取得してインポートするプロセス。</span><span class="sxs-lookup"><span data-stu-id="49658-112">**Import currency exchange rates** – The process that retrieves exchange rates from exchange rate providers and imports them.</span></span> <span data-ttu-id="49658-113">このプロセスは、バッチ処理をサポートするシステム操作です。</span><span class="sxs-lookup"><span data-stu-id="49658-113">This process is a system operation that supports batch processing.</span></span>
- <span data-ttu-id="49658-114">**為替レート プロバイダー** - 外部ソースから為替レートを取得する担当の X++ または C# クラス。</span><span class="sxs-lookup"><span data-stu-id="49658-114">**Exchange rate provider** – An X++ or C# class that is responsible for retrieving exchange rates from external sources.</span></span>
- <span data-ttu-id="49658-115">**為替レート プロバイダー登録** - 使用できるように、為替レート プロバイダーを有効にするプロセス。</span><span class="sxs-lookup"><span data-stu-id="49658-115">**Exchange rate provider registration** – The process of enabling an exchange rate provider so that it can be used.</span></span> <span data-ttu-id="49658-116">既定では、為替レート プロバイダーは配置されると登録されません。</span><span class="sxs-lookup"><span data-stu-id="49658-116">By default, exchange rate providers aren't registered when they are deployed.</span></span>
- <span data-ttu-id="49658-117">**為替レート プロバイダーのコンフィギュレーション**: 使用方法を決定する為替レート プロバイダーのコンフィギュレーション設定。</span><span class="sxs-lookup"><span data-stu-id="49658-117">**Exchange rate provider configuration** – The configuration settings of an exchange rate provider that determine how it will be used.</span></span>
- <span data-ttu-id="49658-118">**為替レート サービス** - 発行された為替レートの一覧を提供する無料または有料の定期売買サービス。</span><span class="sxs-lookup"><span data-stu-id="49658-118">**Exchange rate service** – A free or paid subscription service that provides a list of exchange rates that have been published.</span></span> <span data-ttu-id="49658-119">OANDA による外貨為替レートは、為替レートを提供するサービスの例です。</span><span class="sxs-lookup"><span data-stu-id="49658-119">Foreign Exchange Rates Powered by OANDA is an example of a service that provides exchange rates.</span></span>
- <span data-ttu-id="49658-120">**フレームワーク** – プロバイダーからの為替レートの取得および、それら為替レートの適切なストレージを調整するインポート通貨の為替レートのフレームワーク。</span><span class="sxs-lookup"><span data-stu-id="49658-120">**The framework** – The import currency exchange rates framework that coordinates the retrieval of exchange rates from providers and appropriate storage of those exchange rates.</span></span>

## <a name="conceptualclass-model"></a><span data-ttu-id="49658-121">概念/クラス モデル</span><span class="sxs-lookup"><span data-stu-id="49658-121">Conceptual/class model</span></span>
<span data-ttu-id="49658-122">次の図は、為替レート プロバイダーのフレームワークを構成する主なインターフェイスとクラス、およびそれらの関係を示しています。</span><span class="sxs-lookup"><span data-stu-id="49658-122">The following illustration shows the main interfaces and classes that make up the exchange rate provider framework, and the relationships among them.</span></span> <span data-ttu-id="49658-123">新しい為替レート プロバイダーは、**IExchangeRateProvider** インターフェイスから実装されている必要があります。</span><span class="sxs-lookup"><span data-stu-id="49658-123">New exchange rate providers should be implemented from the **IExchangeRateProvider** interface.</span></span> <span data-ttu-id="49658-124">為替レート プロバイダーは、X++ または C# で記述されます。</span><span class="sxs-lookup"><span data-stu-id="49658-124">Exchange rate providers are written in X++ or C#.</span></span> <span data-ttu-id="49658-125">X++ は .NET 言語なので、 Microsoft .NET Framework を簡単に使用できます。</span><span class="sxs-lookup"><span data-stu-id="49658-125">Because X++ is a .NET language, you can easily use the Microsoft .NET Framework.</span></span> <span data-ttu-id="49658-126">C# で記述されているすべてのプロバイダーは C# プロバイダーとして認識された X++ クラスでラップする必要があります。</span><span class="sxs-lookup"><span data-stu-id="49658-126">All providers that are written in C# must be wrapped by an X++ class to be recognized as C# providers.</span></span> <span data-ttu-id="49658-127">たとえば、ヨーロッパ為替レート プロバイダーの中央銀行は Microsoft が C# で書き出したプロバイダーです。</span><span class="sxs-lookup"><span data-stu-id="49658-127">For example, the Central Bank of Europe exchange rate provider is a provider that Microsoft wrote in C#.</span></span> <span data-ttu-id="49658-128">**ExchangeRateProviderCBOE** X++ クラスによってラップされます。</span><span class="sxs-lookup"><span data-stu-id="49658-128">It's wrapped by the **ExchangeRateProviderCBOE** X++ class.</span></span>

<span data-ttu-id="49658-129">[![為替レート プロバイダー フレームワークの概念/クラス モデル](./media/exchangerates.png)](./media/exchangerates.png)</span><span class="sxs-lookup"><span data-stu-id="49658-129">[![Conceptual/class model of the exchange rate provider framework](./media/exchangerates.png)](./media/exchangerates.png)</span></span>

<span data-ttu-id="49658-130">図で表示されるインターフェイスおよびクラスを次に示します。</span><span class="sxs-lookup"><span data-stu-id="49658-130">Here are the interfaces and classes that are shown in the illustration:</span></span>

- <span data-ttu-id="49658-131">**IExchangeRateProvider** – このインタフェースを実装すると、為替レート プロバイダー フレームワークがクラスを為替レート プロバイダーとして認識できるようになります。</span><span class="sxs-lookup"><span data-stu-id="49658-131">**IExchangeRateProvider** – By implementing this interface, you enable the exchange rate provider framework to recognize a class as an exchange rate provider.</span></span>
- <span data-ttu-id="49658-132">**IExchangeRateProviderFrameworkFactory** – このインターフェイスにより、為替レート プロバイダーは、図の中のいくつかのインターフェイスを表す様々なタイプのプロバイダー フレームワーク クラスを作成することができます。</span><span class="sxs-lookup"><span data-stu-id="49658-132">**IExchangeRateProviderFrameworkFactory** – This interface enables the exchange rate provider to construct various types of provider framework classes that represent some of the interfaces in the illustration.</span></span>
- <span data-ttu-id="49658-133">**IExchangeRateProviderSupportedOptions** – 為替レート プロバイダーは、レートをインポートする際にいくつかのオプションをサポートします。</span><span class="sxs-lookup"><span data-stu-id="49658-133">**IExchangeRateProviderSupportedOptions** – The exchange rate provider supports several options when rates are imported.</span></span> <span data-ttu-id="49658-134">為替レート プロバイダーは、このインターフェイスを使用して、サポートするオプションについてフレームワークに通知します。</span><span class="sxs-lookup"><span data-stu-id="49658-134">The exchange rate provider uses this interface to inform the framework about the options that it supports.</span></span>
- <span data-ttu-id="49658-135">**IExchangeRateProviderConfig** – 各為替レート プロバイダーは、固有のコンフィギュレーションを持つことができます。</span><span class="sxs-lookup"><span data-stu-id="49658-135">**IExchangeRateProviderConfig** – Each exchange rate provider can have a unique configuration.</span></span> <span data-ttu-id="49658-136">このインターフェイスにより、プロバイダーはこの構成を取得できます。</span><span class="sxs-lookup"><span data-stu-id="49658-136">This interface enables the provider to retrieve this configuration.</span></span>
- <span data-ttu-id="49658-137">**IExchangeRateProviderConfigDefaults** – 為替レート プロバイダーは、構成のデフォルト値を作成して提供できます。</span><span class="sxs-lookup"><span data-stu-id="49658-137">**IExchangeRateProviderConfigDefaults** – The exchange rate provider can create and provide default values for its configuration.</span></span> <span data-ttu-id="49658-138">**為替レート プロバイダの構成** ページ (**総勘定元帳** &gt; **為替** &gt; **レート プロバイダーの構成**)でこれらの値を変更できます。</span><span class="sxs-lookup"><span data-stu-id="49658-138">Users can change these values on the **Configure exchange rate providers** page (**General ledger** &gt; **Currencies** &gt; **Configure exchange rate providers**).</span></span>
- <span data-ttu-id="49658-139">**IExchangeRateRequest** – このインターフェイスは、為替レートのインポートを要求する固有のデータを表します。</span><span class="sxs-lookup"><span data-stu-id="49658-139">**IExchangeRateRequest** – This interface represents data that is specific to a request to import exchange rates.</span></span> <span data-ttu-id="49658-140">このデータには、日付範囲、オプション、レートを取得するための通貨ペアが含まれます。</span><span class="sxs-lookup"><span data-stu-id="49658-140">This data includes the date range, options, and the currency pairs to retrieve rates for.</span></span>
- <span data-ttu-id="49658-141">**IExchangeRateCalendar** – このインターフェイスは、次の作業日 (月曜日から金曜日まで) を取得する場合に使用される為替レート カレンダーを表します。</span><span class="sxs-lookup"><span data-stu-id="49658-141">**IExchangeRateCalendar** – This interface represents an exchange rate calendar that is used to retrieve the next working day (Monday through Friday).</span></span>
- <span data-ttu-id="49658-142">**IExchangeRateResponse** – 為替レート プロバイダーでは、このインターフェイスを使用して、通貨のペアや、サービスから返される為替レートを格納します。</span><span class="sxs-lookup"><span data-stu-id="49658-142">**IExchangeRateResponse** – The exchange rate provider uses this interface to store the currency pairs and the exchange rates that are returned from the service.</span></span>
- <span data-ttu-id="49658-143">**IExchangeRateResponseCurrencyPair** – 為替レート プロバイダーでは、このインターフェイスを使用して、サービスから返される特定の通貨ペアの詳細を格納します。</span><span class="sxs-lookup"><span data-stu-id="49658-143">**IExchangeRateResponseCurrencyPair** – The exchange rate provider uses this interface to store the details for a specific currency pair that is returned from the service.</span></span>
- <span data-ttu-id="49658-144">**IExchangeRateResponseExchangeRate** – 為替レート プロバイダーでは、このインターフェイスを使用して、特定の通貨ペアに対して特定の為替レートを格納します。</span><span class="sxs-lookup"><span data-stu-id="49658-144">**IExchangeRateResponseExchangeRate** – The exchange rate provider uses this interface to store a specific exchange rate for a specific currency pair.</span></span>
- <span data-ttu-id="49658-145">**ExchangeRateProviderOanda** - Microsoft によって実装されている為替レート プロバイダーのこの例は、為替レートを返すために OANDA サービスに接続します。</span><span class="sxs-lookup"><span data-stu-id="49658-145">**ExchangeRateProviderOanda** – This example of an exchange rate provider that is implemented by Microsoft connects to the OANDA service to return exchange rates.</span></span>

## <a name="write-an-exchange-rate-provider"></a><span data-ttu-id="49658-146">為替レート プロバイダーの記述</span><span class="sxs-lookup"><span data-stu-id="49658-146">Write an exchange rate provider</span></span>
<span data-ttu-id="49658-147">為替レート プロバイダーを作成するには、これらの手順に従います。</span><span class="sxs-lookup"><span data-stu-id="49658-147">Follow these steps to create an exchange rate provider.</span></span> <span data-ttu-id="49658-148">このコード例は、**ExchangeRateProviderOanda** クラスから取得されています。</span><span class="sxs-lookup"><span data-stu-id="49658-148">The code examples are taken from the **ExchangeRateProviderOanda** class.</span></span>

1. <span data-ttu-id="49658-149">拡張機能を使用して、新しい為替レート プロバイダーを表す **ExchangeRateProvider** の拡張可能列挙体に新しい値を追加します。</span><span class="sxs-lookup"><span data-stu-id="49658-149">Use extensions to add a new value to the **ExchangeRateProvider** extensible enum to represent your new exchange rate provider.</span></span>
2. <span data-ttu-id="49658-150">**通貨**モデルで、**IExchangeRateProvider** インターフェイスを実装するクラスを作成します。</span><span class="sxs-lookup"><span data-stu-id="49658-150">In the **Currency** model, create a class that implements the **IExchangeRateProvider** interface.</span></span>

    ```
    using Microsoft.Dynamics.ApplicationSuite.FinancialManagement.Currency.Framework;
    using Microsoft.Dynamics.Currency.Instrumentation;
    using System.Collections;
    using System.ComponentModel.Composition;
    /// <summary>
    /// The <c>ExchangeRateProviderOanda</c> class is an exchange rate provider for OANDA.
    /// </summary>
    [ExportMetadataAttribute(enumStr(ExchangeRateProvider), 
    ExchangeRateProvider::OANDA), ExportAttribute('Microsoft.Dynamics.ApplicationSuite.FinancialManagement.Currency.Framework.IExchangeRateProvider')]
    class ExchangeRateProviderOanda implements IExchangeRateProvider
    {
    }
    ```

3. <span data-ttu-id="49658-151">クラスに、次の定数と変数宣言を追加します。</span><span class="sxs-lookup"><span data-stu-id="49658-151">Add the following constants and variable declarations to the class.</span></span> <span data-ttu-id="49658-152">**ProviderId** の独自のグローバル一意識別子 (GUID) を提供します。</span><span class="sxs-lookup"><span data-stu-id="49658-152">Provide your own unique globally unique identifier (GUID) for **ProviderId**.</span></span>

    ```
    private const ExchangeRateProviderPropertyKey ServiceURL = 'https://www.oanda.com/rates/api/v1/rates/%1.xml?quote=%2&start=%3&end=%4&fields=%5&decimal_places=%6';
    private const ExchangeRateProviderId ProviderId = '795500B1-4258-4343-868C-433CE390848C';
    private const str OANDADateFormat = 'yyyy-MM-dd';
    private const str HttpWebRequestMethod = 'GET';
    private const str HttpWebRequestContentType = 'application/xml';
    private const str HttpHeaderAuthorization = 'Authorization';
    private const str KeyTokenPrefix = 'Bearer ';
    private const str XPathQuote = '//response/quotes/quote';
    private const str XPathAverageBid = '//bid';
    private const str XPathAverageAsk = '//ask';
    private const str XPathLowBid = '//low_bid';
    private const str XPathLowAsk = '//low_ask';
    private const str XPathMidpoint = '//midpoint';
    private const str XPathDate = '//quote/date';
    private const str XPathHighBid = '//high_bid';
    private const str XPathHighAsk = '//high_ask';
    private const str QuoteParameterAverages = 'averages';
    private const str QuoteParameterLows = 'lows';
    private const str QuoteParameterMidPoint = 'midpoint';
    private const str QuoteParameterHighs = 'highs';
    IExchangeRateProviderFrameworkFactory factory;
    ```

4. <span data-ttu-id="49658-153">**get\_Name** メソッドを実装します。</span><span class="sxs-lookup"><span data-stu-id="49658-153">Implement the **get\_Name** method.</span></span> <span data-ttu-id="49658-154">ラベルを使用して、正しい変換を有効にする必要があります。</span><span class="sxs-lookup"><span data-stu-id="49658-154">You should use a label to enable correct translation.</span></span> <span data-ttu-id="49658-155">ユーザーは、プロバイダーの構成情報を設定すると、ここで指定されている名前を変更できます。</span><span class="sxs-lookup"><span data-stu-id="49658-155">When users set up the provider's configuration information, they can change the name that is provided here.</span></span>

    ```
    public ExchangeRateProviderName get_Name()
    {
        return "@CurrencyExchange:Currency_ConfigField_OandaName";
    }
    ```

5. <span data-ttu-id="49658-156">**get\_Id** メソッドを実装します。</span><span class="sxs-lookup"><span data-stu-id="49658-156">Implement the **get\_Id** method.</span></span> <span data-ttu-id="49658-157">このメソッドは、このプロバイダーを一意に識別する GUID を返します。</span><span class="sxs-lookup"><span data-stu-id="49658-157">This method returns a GUID that uniquely identifies this provider.</span></span>

    ```
    public ExchangeRateProviderId get_Id()
    {
        return ProviderId;
    }
    ```

6. <span data-ttu-id="49658-158">**set\_Factory** メソッドを実装します。</span><span class="sxs-lookup"><span data-stu-id="49658-158">Implement the **set\_Factory** method.</span></span> <span data-ttu-id="49658-159">為替レート プロバイダー フレームワークは、このメソッドを呼び出して、プロバイダーの **IExchangeRateProviderFrameworkFactory** インターフェイスを実装するオブジェクトを設定します。</span><span class="sxs-lookup"><span data-stu-id="49658-159">The exchange rate provider framework will invoke this method to set an object that implements the **IExchangeRateProviderFrameworkFactory** interface on your provider.</span></span> <span data-ttu-id="49658-160">このファクトリを使用して、前の図のインターフェイスの一部を表す新しいオブジェクトのインスタンスを作成できます。</span><span class="sxs-lookup"><span data-stu-id="49658-160">This factory can be used to instantiate new objects that represent some of the interfaces from the previous illustration.</span></span>

    ```
    public void set_Factory(IExchangeRateProviderFrameworkFactory _factory)
    {
        factory = _factory;
    }
    ```

7. <span data-ttu-id="49658-161">**GetSupportedOptions** メソッドを実装します。</span><span class="sxs-lookup"><span data-stu-id="49658-161">Implement the **GetSupportedOptions** method.</span></span> <span data-ttu-id="49658-162">このメソッドは、為替レート プロバイダーは、一部のフレームワーク機能をサポートするかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="49658-162">This method indicates whether the exchange rate provider supports some framework features.</span></span>

   - <span data-ttu-id="49658-163">為替レートを取得するために渡すソース通貨およびターゲット通貨を渡すことが為替レート サービスに必要な場合にのみ、**doesSupportSpecificCurrencyPairs** プロパティを **true** に設定します。</span><span class="sxs-lookup"><span data-stu-id="49658-163">Set the **doesSupportSpecificCurrencyPairs** property to **true** only if the exchange rate service requires that a source currency and a destination currency be passed to get an exchange rate.</span></span> <span data-ttu-id="49658-164">多くの為替レート サービスが、固定通貨または通貨ペアの指定されたセットを返します。</span><span class="sxs-lookup"><span data-stu-id="49658-164">Many exchange rate services return rates for a fixed currency or a given set of currency pairs.</span></span> <span data-ttu-id="49658-165">これらのサービスについては、このプロパティは **false** に設定されます。</span><span class="sxs-lookup"><span data-stu-id="49658-165">For these services, this property should be set to **false**.</span></span> <span data-ttu-id="49658-166">サービス料金が課金された料金の数がクォータ数に基づく場合、**true** の値により、**IExchangeRateRequest** インターフェイスには、**為替レート** ページ (**総勘定元帳** &gt; **通貨** &gt; **為替レート**) の為替レート タイプに設定されている通貨ペアのみを含まれるようになります。</span><span class="sxs-lookup"><span data-stu-id="49658-166">If the prices that a service charges are based on quotas on the number of rates, a value of **true** will cause the **IExchangeRateRequest** interface to contain only those currency pairs that are configured for an exchange rate type on the **Exchange rate** page (**General ledger** &gt; **Currencies** &gt; **Exchange rates**).</span></span> <span data-ttu-id="49658-167">プロバイダーはその後、これらの料金をサービスから具体的に要求できるため、コストを削減できます。</span><span class="sxs-lookup"><span data-stu-id="49658-167">The provider can then specifically request these rates from the service and therefore lower the cost.</span></span>
   - <span data-ttu-id="49658-168">**fixedBaseIsoCurrency** プロパティを、為替レート サービスから返される為替レートの固定ベース通貨を表す 3 文字の国際標準化機構 (ISO) 通貨コードに設定します。</span><span class="sxs-lookup"><span data-stu-id="49658-168">Set the **fixedBaseIsoCurrency** property to the three-character International Organization for Standardization (ISO) currency code that represents the fixed base currency of the exchange rates that are returned from the exchange rate service.</span></span> <span data-ttu-id="49658-169">為替レート サービスが固定基本通貨をサポートしていない場合は、空の文字列を返します。</span><span class="sxs-lookup"><span data-stu-id="49658-169">If the exchange rate service doesn't support a fixed base currency, return an empty string.</span></span> <span data-ttu-id="49658-170">たとえば、ユーロは固定基本通貨としてよく使用されます。</span><span class="sxs-lookup"><span data-stu-id="49658-170">For example, the euro is often used as a fixed base currency.</span></span> <span data-ttu-id="49658-171">新しいプロバイダーを作成するときは、正しい値を選択できるように、為替レート サービスをかならず調査してください。</span><span class="sxs-lookup"><span data-stu-id="49658-171">When you create a new provider, be sure to research the exchange rate service so that you can select the correct value.</span></span>
   - <span data-ttu-id="49658-172">サービスが日付範囲全体を表す単一のレートを返すことができる場合、**singleRateForDateRange** プロパティを **true** に設定します。</span><span class="sxs-lookup"><span data-stu-id="49658-172">Set the **singleRateForDateRange** property to **true** if the service can return a single rate that represents the whole date range.</span></span> <span data-ttu-id="49658-173">たとえば、1 か月の平均為替レートを表す単一の為替レートを返すには、この設定を使用できます。</span><span class="sxs-lookup"><span data-stu-id="49658-173">For example, you can use this setting to return a single exchange rate that represents the average exchange rate for a month.</span></span> <span data-ttu-id="49658-174">サービスがこの機能をサポートしていない場合は、このプロパティを **false** に設定します。</span><span class="sxs-lookup"><span data-stu-id="49658-174">If the service doesn't support this functionality, set this property to **false**.</span></span>

     ```
     public IExchangeRateProviderSupportedOptions GetSupportedOptions()
     {
       IExchangeRateProviderSupportedOptions options = factory.CreateExchangeRateProviderSupportedOptions();
       options.set_doesSupportSpecificCurrencyPairs(true);
       options.set_doesSupportSpecificDates(false);
       options.set_fixedBaseIsoCurrency('');
       options.set_singleRateForDateRange(true);
       options.set_doesSupportPreventImportOnNationalHoliday(false);
     return options;
     ```

8. <span data-ttu-id="49658-175">**GetConfigurationDefaults** メソッドを実装します。</span><span class="sxs-lookup"><span data-stu-id="49658-175">Implement the **GetConfigurationDefaults** method.</span></span> <span data-ttu-id="49658-176">既定のコンフィギュレーションは、為替レート プロバイダの既定コンフィギュレーションの設定を表す名前と値の組です。</span><span class="sxs-lookup"><span data-stu-id="49658-176">Configuration defaults are name-value pairs that represent the default configuration settings for the exchange rate provider.</span></span> <span data-ttu-id="49658-177">これらの設定はプロバイダーが登録されたときに自動的に読み込まれますが、ユーザーは変更できます。</span><span class="sxs-lookup"><span data-stu-id="49658-177">These settings are automatically loaded when the provider is registered, but users can change them.</span></span> <span data-ttu-id="49658-178">これらの文字列を使用可能な値に変換する場合は、必要な対策を講じてください。</span><span class="sxs-lookup"><span data-stu-id="49658-178">Take the necessary precautions when you convert these strings into usable values.</span></span> <span data-ttu-id="49658-179">値フィールドは、SQL で暗号化フィールドとして格納されます。</span><span class="sxs-lookup"><span data-stu-id="49658-179">The value field is stored as an encrypted field in SQL.</span></span> <span data-ttu-id="49658-180">したがって、アプリケーション プログラミング インターフェイス (API) などの機密データはより安全になります。</span><span class="sxs-lookup"><span data-stu-id="49658-180">Therefore, sensitive data such as an application programming interface (API) key will be more secure.</span></span>

    ```
    public IExchangeRateProviderConfigDefaults GetConfigurationDefaults()
    {
        IExchangeRateProviderConfigDefaults configurationDefaults = factory.CreateExchangeRateProviderConfigDefaults();
        configurationDefaults.addNameValueConfigurationPair("@CurrencyExchange:Currency_ConfigField_ServiceTimeout", '5000');
        configurationDefaults.addNameValueConfigurationPair("@CurrencyExchange:Currency_ConfigField_OandaAPIKey", '');
        configurationDefaults.addNameValueConfigurationPair("@CurrencyExchange:Currency_ConfigField_DecimalPlaces", '5');
        configurationDefaults.addNameValueConfigurationPair("("@CurrencyExchange:Currency_ConfigField_QuoteTypeLocked", '1');
        return configurationDefaults;
    }
    ```

9. <span data-ttu-id="49658-181">**ValidateConfigurationDetail** メソッドを実装します。</span><span class="sxs-lookup"><span data-stu-id="49658-181">Implement the **ValidateConfigurationDetail** method.</span></span> <span data-ttu-id="49658-182">このメソッドにより、為替レート プロバイダーは、**為替レート プロバイダーの構成**ページでユーザーが変更する構成情報を検証できます。</span><span class="sxs-lookup"><span data-stu-id="49658-182">This method enables the exchange rate provider to validate the configuration information that the user modifies on the **Configure exchange rate providers** page.</span></span>

    ```
    public boolean ValidateConfigurationDetail(ExchangeRateProviderPropertyKey _key, ExchangeRateProviderPropertyValue _value)
    {
        boolean result = true;
        switch (_key)
        {
            case "@CurrencyExchange:Currency_ConfigField_DecimalPlaces":
                int decimals = str2Int(_value);
                if ((decimals > 12) || (decimals < 1))
                {
                    CurrencyEventSource eventSource = CurrencyEventSource::Log;
                    eventSource.ImportExchangeRateMark("@CurrencyExchange:Currency_ConfigMessage_DecimalPlacesInvalid");
                    error("@CurrencyExchange:Currency_ConfigMessage_DecimalPlacesInvalid");
                    result = false;
                }
                break;
            case "@CurrencyExchange:Currency_ConfigField_OandaAPIKey":
                if (_value == '')
                {
                    CurrencyEventSource eventSource = CurrencyEventSource::Log;
                    eventSource.ImportExchangeRateMark("@CurrencyExchange:Currency_ConfigMessage_OANDAKeyRequired");
                    warning("@CurrencyExchange:Currency_ConfigMessage_OANDAKeyRequired");
                }
                break;
        }
        return result;
    }
    ```

10. <span data-ttu-id="49658-183">**EnumNameForLookup** メソッドを実装します。</span><span class="sxs-lookup"><span data-stu-id="49658-183">Implement the **EnumNameForLookup** method.</span></span> <span data-ttu-id="49658-184">このメソッドは、為替レート プロバイダーが特定の **ExchangeRateProviderPropertyKey** キーを参照できるようにします。</span><span class="sxs-lookup"><span data-stu-id="49658-184">This method enables the exchange rate provider to enable a lookup for a specific **ExchangeRateProviderPropertyKey** key.</span></span> <span data-ttu-id="49658-185">適切なキーに対して列挙された既存の型の名前を返します。</span><span class="sxs-lookup"><span data-stu-id="49658-185">Just return the name of an existing enumerated type for the appropriate key.</span></span> <span data-ttu-id="49658-186">この機能が必要でない場合は、空の文字列を返します。</span><span class="sxs-lookup"><span data-stu-id="49658-186">If this feature isn't required, return an empty string.</span></span>

    ```
    public str EnumNameForLookup(ExchangeRateProviderPropertyKey _key)
    {
        if (_key == "@CurrencyExchange:Currency_ConfigField_QuoteType")
        {
            return enumStr(ExchangeRateProviderOANDAQuoteType);
        }
        return '';
    }
    ```

11. <span data-ttu-id="49658-187">**GetExchangeRates** メソッドを実装します。</span><span class="sxs-lookup"><span data-stu-id="49658-187">Implement the **GetExchangeRates** method.</span></span> <span data-ttu-id="49658-188">このメソッドは、構成情報と、**IExchangeRateRequest** インターフェイスを使用して、交換レート サービスを呼び出すとともに、**IExchangeRateResponse** クラスの適切なインスタンスを返します。</span><span class="sxs-lookup"><span data-stu-id="49658-188">This method uses the configuration information and the **IExchangeRateRequest** interface that is provided to call out to the exchange rate service and return the appropriate instance of the **IExchangeRateResponse** class.</span></span> <span data-ttu-id="49658-189">このメソッドを記述するときは、以下の重要な点を考慮します。</span><span class="sxs-lookup"><span data-stu-id="49658-189">When you write this method, consider these important points:</span></span>

    - <span data-ttu-id="49658-190">必要なすべてのコンフィギュレーション情報は **IExchangeRateProviderConfig** インターフェイスから取得する必要があります。</span><span class="sxs-lookup"><span data-stu-id="49658-190">Any configuration information that is required should be retrieved from the **IExchangeRateProviderConfig** interface.</span></span> <span data-ttu-id="49658-191">そのインターフェイスの**GetPropertyValue**メソッドへの呼び出しは、入力されたプロパティキーのプロパティ値の文字列形式を提供します。</span><span class="sxs-lookup"><span data-stu-id="49658-191">A call to the **GetPropertyValue** method on that interface will provide the string representation of the property value for the property key that is provided.</span></span> <span data-ttu-id="49658-192">この文字列値を別の型に変換する場合は、必要な対策を講じてください。</span><span class="sxs-lookup"><span data-stu-id="49658-192">Take the required precautions when you convert this string value to another type.</span></span>
    - <span data-ttu-id="49658-193">事前に必要な検証を行います。</span><span class="sxs-lookup"><span data-stu-id="49658-193">Do any required validation up front.</span></span> <span data-ttu-id="49658-194">たとえば、OANDA は、すべてのサービス コールで API キーを指定するよう要求します。</span><span class="sxs-lookup"><span data-stu-id="49658-194">For example, OANDA requires that an API key be supplied on every service call.</span></span> <span data-ttu-id="49658-195">この API キーが設定されていない場合は、サービスが失敗します。</span><span class="sxs-lookup"><span data-stu-id="49658-195">If this API key isn't set, the service will fail.</span></span> <span data-ttu-id="49658-196">API キーが設定されていない場合は、料金をインポートする前に終了するよう適切なエラー メッセージを表示することを確認します。</span><span class="sxs-lookup"><span data-stu-id="49658-196">Verify that if the API key isn't set then, throw the appropriate error message to exit prior to importing rates.</span></span>
    - <span data-ttu-id="49658-197">一部のプロバイダーには、為替レートが要求される場合に明示的な通貨の組み合わせが必要です。</span><span class="sxs-lookup"><span data-stu-id="49658-197">Some providers require explicit currency pairs when exchange rates are requested.</span></span> <span data-ttu-id="49658-198">これらのプロバイダーは、**IExchangeRateProviderSupportedOptions.doesSupportSpecificCurrencyPairs** プロパティを **true** に設定したプロバイダーと同じです。</span><span class="sxs-lookup"><span data-stu-id="49658-198">These providers are the same providers that set the **IExchangeRateProviderSupportedOptions.doesSupportSpecificCurrencyPairs** property to **true**.</span></span> <span data-ttu-id="49658-199">この場合、**IExchangeRateRequest** インターフェイスが提示する通貨ペアを使用して、取得プロセスを動作させる必要があります。</span><span class="sxs-lookup"><span data-stu-id="49658-199">In this case, you must use the currency pairs that the **IExchangeRateRequest** interface provides to drive the retrieval process.</span></span> <span data-ttu-id="49658-200">後に続く OANDA プロバイダーの実装には、このタイプのプロバイダーの適正例が示されます。</span><span class="sxs-lookup"><span data-stu-id="49658-200">The OANDA provider implementation that follows shows a good example of this type of provider.</span></span> <span data-ttu-id="49658-201">通常、特定の通貨の組み合わせをサポートしていないプロバイダーは、固定された通貨の組み合わせのデータを返します。</span><span class="sxs-lookup"><span data-stu-id="49658-201">Typically, providers that don't support specific currency pairs return data for a fixed set of currency pairs.</span></span> <span data-ttu-id="49658-202">この場合、**IExchangeRateRequest** インターフェイスが提示する通貨ペアは無視できます。</span><span class="sxs-lookup"><span data-stu-id="49658-202">In this case, the currency pairs that the **IExchangeRateRequest** interface provides can be ignored.</span></span> <span data-ttu-id="49658-203">プロバイダーは、使用できるすべてのレートを返す必要があります。</span><span class="sxs-lookup"><span data-stu-id="49658-203">Providers should return all the rates that are available.</span></span> <span data-ttu-id="49658-204">このフレームワークは、必要な通貨ペアを自動的に作成するかどうかに関するユーザーの決定に基づいて、正しいレートをインポートします。</span><span class="sxs-lookup"><span data-stu-id="49658-204">The framework will then import the correct rates, based on the user's decision about whether to automatically create the required currency pairs.</span></span> <span data-ttu-id="49658-205">CentralBankOfEuropeProvider プロバイダーは、このタイプのプロバイダーの適切な例です。</span><span class="sxs-lookup"><span data-stu-id="49658-205">The CentralBankOfEuropeProvider provider is a good example of this type of provider.</span></span>
    - <span data-ttu-id="49658-206">**IExchangeRateRequest** インターフェイスには、**ImportDateType** というプロパティがあります。</span><span class="sxs-lookup"><span data-stu-id="49658-206">The **IExchangeRateRequest** interface has a property that is named **ImportDateType**.</span></span> <span data-ttu-id="49658-207">このプロパティは、サービスから為替レートを取得するために使用する日付を示します。</span><span class="sxs-lookup"><span data-stu-id="49658-207">This property indicates the dates that should be used to retrieve exchange rates from the service.</span></span> <span data-ttu-id="49658-208">利用可能な 2 つの値は、**CurrentDate** と **DateRange** です。</span><span class="sxs-lookup"><span data-stu-id="49658-208">The two values that are available are **CurrentDate** and **DateRange**.</span></span>

        - <span data-ttu-id="49658-209">**CurrentDate** は、為替レート サービスから最新の為替レートを取得します。</span><span class="sxs-lookup"><span data-stu-id="49658-209">**CurrentDate** retrieves the most current exchange rate from the exchange rate service.</span></span> <span data-ttu-id="49658-210">また、プロバイダーにこの値が渡されると、フレームワークは、**IExchangeRateRequest.FromDate** および **IExchangeRateRequest.ToDate** を、要求している Application Object Server (AOS) コンピュータのシステム日付に設定します。</span><span class="sxs-lookup"><span data-stu-id="49658-210">When this value is passed to the provider, the framework also sets **IExchangeRateRequest.FromDate** and **IExchangeRateRequest.ToDate** to the system date of the Application Object Server (AOS) computer that is making the request.</span></span> <span data-ttu-id="49658-211">為替レート サービスでは、特定の日付の為替レートの取得をサポート、フレームワークが提供する日付を渡す必要があります。</span><span class="sxs-lookup"><span data-stu-id="49658-211">If exchange rate services support the retrieval of exchange rates for specific dates, the date that the framework provides should be passed.</span></span> <span data-ttu-id="49658-212">ただし、代わりに為替レート サービスが最新の為替レート (日付に関係なく) を取得する呼び出しを提供する場合、返される日付が要求日より前または同じ日付であることを確認するよう検証する必要があります。</span><span class="sxs-lookup"><span data-stu-id="49658-212">However, if the exchange rate service instead provides a call to get the most current exchange rate (regardless of the date), the date that is returned must be validated to make sure that it's less than or equal to the requested date.</span></span>
        - <span data-ttu-id="49658-213">**DateRange** は、特定の日付範囲の為替レートを取得します。</span><span class="sxs-lookup"><span data-stu-id="49658-213">**DateRange** retrieves the exchange rates for a specific date range.</span></span> <span data-ttu-id="49658-214">指定された日付範囲内の為替レートのみ許可される必要があります。</span><span class="sxs-lookup"><span data-stu-id="49658-214">Only exchange rates in the specified date range should be allowed.</span></span> <span data-ttu-id="49658-215">為替レート サービスで、特定の日付が要求に含まれることが必要とされる場合は、このプロセスは簡単です。</span><span class="sxs-lookup"><span data-stu-id="49658-215">If an exchange rate service requires that specific dates be included in the request, this process is straightforward.</span></span> <span data-ttu-id="49658-216">ただし、代わりに為替レート サービスが有効日の範囲外の可能性がある履歴日付のグループを返す場合、プロバイダーはフレームワークに日付を戻す前に該当しない日付を除外する必要があります。</span><span class="sxs-lookup"><span data-stu-id="49658-216">However, if an exchange rate service instead returns a group of historical dates that might be outside the valid range of dates, the provider must filter out the dates that aren't relevant before it passes the dates back to the framework.</span></span>

    - <span data-ttu-id="49658-217">為替レートが返されるときは、**IExchangeRateRequest** クラスのインスタンスが提供する日付ではなく、為替レート サービスが提供する日付を常に使用します。</span><span class="sxs-lookup"><span data-stu-id="49658-217">When exchange rates are returned, always use the date that the exchange rate service provides instead of the dates that the instance of the **IExchangeRateRequest** class supplies.</span></span> <span data-ttu-id="49658-218">この方法では、為替レート サービスが予期されていない日付のレートを返す場合があるため、返される為替レートが正しい日付に関連付けられていることを保証できます。</span><span class="sxs-lookup"><span data-stu-id="49658-218">In this way, you help guarantee that the exchange rate that is returned is associated with the correct date, because an exchange rate service might occasionally return rates for dates that weren't expected.</span></span> <span data-ttu-id="49658-219">たとえば、将来の日付に対して為替レートが要求されると、一部のプロバイダーは、エラーをスローしたり何も返さない代わりに、最新の為替レートを返します。</span><span class="sxs-lookup"><span data-stu-id="49658-219">For example, if an exchange rate is requested for a date in the future, some providers return the most recent exchange rate instead of throwing an error or returning nothing.</span></span>
    - <span data-ttu-id="49658-220">為替レート サービスからの為替レートを取得するときにエラーが発生する場合は、カスタム エラー メッセージをスローしないようにします。</span><span class="sxs-lookup"><span data-stu-id="49658-220">If you encounter errors when you try to retrieve exchange rates from the exchange rate service, don't throw custom error messages.</span></span> <span data-ttu-id="49658-221">このフレームワークは、予想される通貨ペアをプロバイダーから取得できないという一般的なエラーメッセージを投げて問題があることをユーザーに警告します。</span><span class="sxs-lookup"><span data-stu-id="49658-221">The framework will alert the user that there is an issue by throwing generic error messages that state that the expected currency pairs could not be retrieved from the provider.</span></span> <span data-ttu-id="49658-222">その他のエラーのログを記録する必要がある場合、**CurrencyEventSource** を使用します。</span><span class="sxs-lookup"><span data-stu-id="49658-222">If you must log additional errors, use **CurrencyEventSource**.</span></span> <span data-ttu-id="49658-223">例については、次のコードで **catch** ステートメントおよび **oandaKey** 変数に対する **IF** 条件を参照してください。。</span><span class="sxs-lookup"><span data-stu-id="49658-223">For an example, see the **catch** statement and the **if** condition for the **oandaKey** variable in the following code.</span></span>

    ```
    public IExchangeRateResponse GetExchangeRates(IExchangeRateRequest _request, IExchangeRateProviderConfig _config)
    {
        System.Exception exception;
        // cache configuration and request properties locally for performance
        ExchangeRateProviderPropertyValue oandaKey = _config.GetPropertyValue(this.get_Id(), "@CurrencyExchange:Currency_ConfigField_OandaAPIKey");
        if (oandaKey == '')
        {
            CurrencyEventSource eventSource = CurrencyEventSource::Log;
            eventSource.ImportRatesException("@CurrencyExchange:Currency_ConfigMessage_OANDAKeyRequired", "");
            throw error("@CurrencyExchange:Currency_ConfigMessage_OANDAKeyRequired");
        }
        int decimalPlaces = str2Int(_config.GetPropertyValue(this.get_Id(), "@CurrencyExchange:Currency_ConfigField_DecimalPlaces"));
        int serviceTimeout = str2int(_config.getPropertyValue(this.get_Id(), "@CurrencyExchange:Currency_ConfigField_ServiceTimeout"));
        boolean singleRateForDateRange = _request.get_SingleRateForDateRange();
        ExchangeRateProviderOANDAQuoteType quoteType = str2Int(_config.getPropertyValue(this.get_Id(), "@CurrencyExchange:Currency_ConfigField_QuoteTypeLocked"));
        str quoteTypeParameterForOANDA = this.getQuoteTypeParameterForURL(quoteType);
        List rates = new List(Types::Real);
        List dates = new List(Types::Date);
        System.TimeZone localTimeZone = System.TimeZone::get_CurrentTimeZone();
        System.DateTime toUTCDate = localTimeZone.ToUniversalTime(_request.get_ToDate());
        str toDateForRequest = toUTCDate.ToString(OANDADateFormat);
        IExchangeRateResponse response = factory.CreateExchangeRateResponse();
        // Iterate over the requested currency pairs. This is only required for providers
        // that support specific currency pairs.
        IEnumerator currencyPairsEnumerator = _request.GetEnumerator();
        while(currencyPairsEnumerator.MoveNext())
        {
            URL OandaUrl = ServiceURL;
            // This loop will either execute once if singleRateForDateRange is true; otherwise, it will
            // execute once for each day. If we make a single request for multiple dates
            // then OANDA will return an average rate for the date range.
            System.DateTime fromDate = _request.get_FromDate();
            int compareResult = fromDate.CompareTo(_request.get_ToDate());
            while (compareResult <= 0)
            {
                IExchangeRateRequestCurrencyPair currencyPairRequest = currencyPairsEnumerator.Current;
                IExchangeRateResponseCurrencyPair currencyPairResponse = factory.CreateExchangeRateResponseCurrencyPair();
                currencyPairResponse.set_FromCurrency(currencyPairRequest.get_FromCurrency());
                currencyPairResponse.set_ToCurrency(currencyPairRequest.get_ToCurrency());
                // All rates are requested with a display factor of 1 for this provider. If the rates
                // internally are represented using a different exchange rate display factor, the
                // framework will make the necessary adjustments when saving the exchange rates.
                currencyPairResponse.set_ExchangeRateDisplayFactor(ExchangeRateDisplayFactor::One);
                // convert to UTC which is required by OANDA
                System.DateTime fromUTCDate = localTimeZone.ToUniversalTime(fromDate);
                str fromDateForRequest = fromUTCDate.ToString(OANDADateFormat);
                // Build the request URL.
                str oandaRequestString;
                if (singleRateForDateRange)
                {
                    // getting an average rate for the date range so we invoke the service
                    // only once per currency pair using the from and to date
                    oandaRequestString = strFmt(OandaUrl,
                        currencyPairRequest.get_FromCurrency(),
                        currencyPairRequest.get_ToCurrency(),
                        fromDateForRequest,
                        toDateForRequest,
                        quoteTypeParameterForOANDA,
                        decimalPlaces);
                }
                else
                {
                    // invoke the service once for each day.
                    oandaRequestString = strFmt(OandaUrl,
                        currencyPairRequest.get_FromCurrency(),
                        currencyPairRequest.get_ToCurrency(),
                        fromDateForRequest,
                        fromDateForRequest,
                        quoteTypeParameterForOANDA,
                        decimalPlaces);
                }
                // Configure the request for OANDA.
                System.Net.HttpWebRequest httpWebRequest = System.Net.WebRequest::CreateHttp(oandaRequestString);
                httpWebRequest.set_Method(HttpWebRequestMethod);
                httpWebRequest.set_ContentType(HttpWebRequestContentType);
                httpWebRequest.set_Timeout(serviceTimeout);
                // Authentication
                System.Net.WebHeaderCollection webCollection = httpWebRequest.get_Headers();
                webCollection.Add(HttpHeaderAuthorization, KeyTokenPrefix + oandaKey);
                try
                {
                    // Invoke the service
                    System.Net.WebResponse webResponse;
                    webResponse = httpWebRequest.GetResponse();
                    // Retrieve the XML response.
                    System.IO.Stream stream = webResponse.GetResponseStream();
                    System.IO.StreamReader streamReader = new System.IO.StreamReader(stream);
                    str XMLOut = streamReader.ReadToEnd();
                    // Parse the XML to retrieve the rate and date.
                    this.processResult(quoteType, singleRateForDateRange, _request.get_FromDate(), XMLOut, rates, dates);
                    ListEnumerator rateEnumerator = rates.getEnumerator();
                    ListEnumerator dateEnumerator = dates.getEnumerator();
                    // Create the Exchange Rate Provider Response.
                    rateEnumerator.moveNext();
                    dateEnumerator.moveNext();
                    CurrencyExchangeRate exchangeRate = rateEnumerator.current();
                    date currentDate = dateEnumerator.current();
                    if (currentDate != dateNull() && exchangeRate)
                    {
                        IExchangeRateResponseExchangeRate exchangeRateResponse = factory.CreateExchangeRateResponseExchangeRate();
                        exchangeRateResponse.set_ValidFrom(currentDate);
                        exchangeRateResponse.set_ExchangeRate(exchangeRate);
                        currencyPairResponse.addExchangeRate(exchangeRateResponse);
                    }
                }
                catch(exception)
                {
                    CurrencyEventSource eventSource = CurrencyEventSource::Log;
                    eventSource.ImportRatesException(exception.Message, Exception.StackTrace);
                }
                response.addOrUpdateCurrencyPair(currencyPairResponse);
                rates = new List(Types::Real);
                dates = new List(Types::Date);
                fromDate = fromDate.AddDays(1);
                if (singleRateForDateRange)
                {
                    // getting an average rate across the date range so we invoke the service
                    // only once per currency pair
                    compareResult = 1;
                }
                else
                {
                    compareResult = fromDate.CompareTo(_request.get_ToDate());
                }
            }
        }
        return response;
    ```

12. <span data-ttu-id="49658-224">次のヘルパー メソッドを実装します。</span><span class="sxs-lookup"><span data-stu-id="49658-224">Implement the following helper methods.</span></span> <span data-ttu-id="49658-225">これらのメソッドはこの例に固有のものであり、すべてのプロバイダーに必須ではありません。</span><span class="sxs-lookup"><span data-stu-id="49658-225">These methods are specific to this example and aren't required for every provider.</span></span>

    ```
    private str getQuoteTypeParameterForURL(IExchangeRateProviderConfig _config)
    {
        ExchangeRateProviderOANDAQuoteType quoteType = 
            str2Int(_config.getPropertyValue(this.get_Id(), "@CurrencyExchange:Currency_ConfigField_QuoteType"));
        str quoteTypeParameter;
        switch (quoteType)
        {
            case ExchangeRateProviderOANDAQuoteType::AverageAsk:
            case ExchangeRateProviderOANDAQuoteType::AverageBid:
                quoteTypeParameter = QuoteParameterAverages;
                break;
            case ExchangeRateProviderOANDAQuoteType::LowAsk:
            case ExchangeRateProviderOANDAQuoteType::LowBid:
                quoteTypeParameter = QuoteParameterLows;
                break;
            case ExchangeRateProviderOANDAQuoteType::MidPoint:
                quoteTypeParameter = QuoteParameterMidPoint;
                break;
            case ExchangeRateProviderOANDAQuoteType::HighAsk:
            case ExchangeRateProviderOANDAQuoteType::HighBid:
                quoteTypeParameter = QuoteParameterHighs;
                break;
        }
        return quoteTypeParameter;
    }
    private void readRate(IExchangeRateProviderConfig _config, System.Xml.XmlNode _xmlQuoteNode, List _rates)
    {
        System.Xml.XmlNode xmlRateNode;
        CurrencyExchangeRate exchangeRate;
        str value;
        ExchangeRateProviderOANDAQuoteType quoteType = str2Int(_config.getPropertyValue(this.get_Id(), "@CurrencyExchange:Currency_ConfigField_QuoteType"));
        // Find the exchange rate
        switch (quoteType)
        {
            case ExchangeRateProviderOANDAQuoteType::AverageBid:
                xmlRateNode = _xmlQuoteNode.SelectSingleNode(XPathAverageBid);
                break;
            case ExchangeRateProviderOANDAQuoteType::AverageAsk:
                xmlRateNode = _xmlQuoteNode.SelectSingleNode(XPathAverageAsk);
                break;
            case ExchangeRateProviderOANDAQuoteType::LowBid:
                xmlRateNode = _xmlQuoteNode.SelectSingleNode(XPathLowBid);
                break;
            case ExchangeRateProviderOANDAQuoteType::LowAsk:
                xmlRateNode = _xmlQuoteNode.SelectSingleNode(XPathLowAsk);
                break;
            case ExchangeRateProviderOANDAQuoteType::MidPoint:
                xmlRateNode = _xmlQuoteNode.SelectSingleNode(XPathMidpoint);
                break;
            case ExchangeRateProviderOANDAQuoteType::HighBid:
                xmlRateNode = _xmlQuoteNode.SelectSingleNode(XPathHighBid);
                break;
            case ExchangeRateProviderOANDAQuoteType::HighAsk:
                xmlRateNode = _xmlQuoteNode.SelectSingleNode(XPathHighAsk);
                break;
        }
        if (xmlRateNode)
        {
            value = xmlRateNode.get_InnerText();
            exchangeRate = str2num(value);
            if (exchangeRate)
            {
                _rates.addEnd(exchangeRate);
            }
        }
    }
    private void processResult(IExchangeRateProviderConfig _config, boolean _singleRateForDateRange, System.DateTime _defaultDate, 
        str _xmlString, List _rates, List _dates)
    {
        System.Xml.XmlDocument xmlDom = new System.Xml.XmlDocument();
        System.Xml.XmlNode xmlQuoteNode, xmlDateNode;
        ValidFromDate exchangeDate;
        str value;
        xmlDom.LoadXml(_xmlString);
        // Find the Quote
        xmlQuoteNode = xmlDom.SelectSingleNode(XPathQuote);
        if (xmlQuoteNode)
        {
            this.readRate(_config, xmlQuoteNode, _rates);
            // Find the date of the exchange rate.
            xmlDateNode = xmlQuoteNode.SelectSingleNode(XPathDate);
            if (xmlDateNode || _singleRateForDateRange)
            {
                if (xmlDateNode)
                {
                    value = xmlDateNode.get_InnerText();
                }
                if (value)
                {
                    // convert the date from UTC to local timezone.
                    exchangeDate = System.DateTime::Parse(value, System.Globalization.CultureInfo::get_CurrentUICulture(),
                        System.Globalization.DateTimeStyles::AssumeUniversal);
                    if (exchangeDate)
                    {
                        _dates.addEnd(exchangeDate);
                    }
                }
                else if (!value && _singleRateForDateRange)
                {
                    exchangeDate = _defaultDate;
                    _dates.addEnd(exchangeDate);
                }
            }
        }
    }
    ```

13. <span data-ttu-id="49658-226">**ExchangeRateProviderOanda** クラスをコンパイルします。</span><span class="sxs-lookup"><span data-stu-id="49658-226">Compile the **ExchangeRateProviderOanda** class.</span></span> <span data-ttu-id="49658-227">プロバイダーは、SysOperation の一部として実行されます。</span><span class="sxs-lookup"><span data-stu-id="49658-227">The provider will be run as part of a SysOperation.</span></span> <span data-ttu-id="49658-228">問題をデバッグするときに、次のフレームワーク クラスおよびメソッドを理解しておくと便利です。</span><span class="sxs-lookup"><span data-stu-id="49658-228">It's helpful to understand the following framework classes and methods when you debug issues:</span></span>

    - <span data-ttu-id="49658-229">**ExchangeRateProviderFactory.initialize()** - このメソッドは、為替レート プロバイダーのインスタンスを作成し、為替レートの登録またはインポート時に呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="49658-229">**ExchangeRateProviderFactory.initialize()** – This method creates instances of the exchange rate providers, and is called when exchange rates are registered or imported.</span></span> <span data-ttu-id="49658-230">プロバイダーにインスタンスが作成されていない場合、ここでデバッグを開始します。</span><span class="sxs-lookup"><span data-stu-id="49658-230">If your provider isn't instantiated, start to debug here.</span></span>
    - <span data-ttu-id="49658-231">**ExchangeRateProviderRegistration.initialize()** - このメソッドはプロバイダーを検索し、プロバイダーを登録できるようにします。</span><span class="sxs-lookup"><span data-stu-id="49658-231">**ExchangeRateProviderRegistration.initialize()** – This method searches for providers, so that they can be registered.</span></span> <span data-ttu-id="49658-232">登録ページでプロバイダーがわからない場合は、ここでデバッグを開始します。</span><span class="sxs-lookup"><span data-stu-id="49658-232">If you can't see your provider on the registration page, start to debug here.</span></span>
    - <span data-ttu-id="49658-233">**ExchangeRateImportOperation.import()** - このメソッドでは、必要なプロバイダーを呼び出して為替レートを保存することによって、インポート プロセスを駆動します。</span><span class="sxs-lookup"><span data-stu-id="49658-233">**ExchangeRateImportOperation.import()** – This method drives the import process by calling the required provider and storing the exchange rates.</span></span>
    - <span data-ttu-id="49658-234">**ExchangeRateProviderConfig** - このクラスはプロバイダーのコンフィギュレーション情報へのアクセスを提供します。</span><span class="sxs-lookup"><span data-stu-id="49658-234">**ExchangeRateProviderConfig** – This class provides access to configuration information for the providers.</span></span>

## <a name="ideas-to-consider"></a><span data-ttu-id="49658-235">考慮する必要があるアイデア</span><span class="sxs-lookup"><span data-stu-id="49658-235">Ideas to consider</span></span>
<span data-ttu-id="49658-236">為替レートの取得には為替レートのプロバイダーが使用するメソッドに制限がないため、このフレームワークはいくつかの興味深いシナリオを有効にします。</span><span class="sxs-lookup"><span data-stu-id="49658-236">Because there are no limits to the methods that exchange rate providers use to get exchange rates, the framework enables some interesting scenarios.</span></span> <span data-ttu-id="49658-237">参照するアイデアを次に示します。</span><span class="sxs-lookup"><span data-stu-id="49658-237">Here are some ideas that you might want to explore:</span></span>

- <span data-ttu-id="49658-238">**他の為替レート タイプからの為替レートを取得するプロバイダー** – このシナリオを実装すると、さまざまな為替レート タイプ間の為替レートの同期が可能になります。</span><span class="sxs-lookup"><span data-stu-id="49658-238">**Providers that retrieve exchange rates from other exchange rate types** – If you implement this scenario, it will enable synchronization of exchange rates among various exchange rate types.</span></span> <span data-ttu-id="49658-239">この機能は、さまざまな元帳間の分離を維持するために、多くの為替レート タイプが存在する状況で役立ちます。</span><span class="sxs-lookup"><span data-stu-id="49658-239">This functionality can be useful in situations where many exchange rate types exist, because it will help maintain isolation between different ledgers.</span></span>
- <span data-ttu-id="49658-240">**為替レート サービスの任意の形式を ExchangeRateResponse クラスのインスタンスに変換するために Extensible Stylesheet Language Transformations (XSLT) を使用するプロバイダー** – このシナリオを実装すると、ユーザーは為替レート サービスに必要な XSLT 変換を追加することができ、アプリケーションはそのサービスをサポートします。</span><span class="sxs-lookup"><span data-stu-id="49658-240">**Providers that use Extensible Stylesheet Language Transformations (XSLT) to transform any format for an exchange rate service into an instance of the ExchangeRateResponse class** – If you implement this scenario, users can add the XSLT transform that is required for their exchange rate service, and the application will support the service.</span></span> <span data-ttu-id="49658-241">プロバイダー固有のコードは必要ありません。</span><span class="sxs-lookup"><span data-stu-id="49658-241">Provider-specific code isn't required.</span></span>
- <span data-ttu-id="49658-242">**一部の為替レート プロバイダー サービスは、消費されるすべてのレートに対して料金を請求します** – このリストの最初のアイデアと、サービスから取得するレートの数の制限を組み合わせることを検討してください。</span><span class="sxs-lookup"><span data-stu-id="49658-242">**Some exchange rate provider services charge for every rate that is consumed** – Consider combining the first idea in this list with a limit on the number of rates that you retrieve from the service.</span></span> <span data-ttu-id="49658-243">この機能は、サービスから消費される料金ごとに課金されるシナリオに役立ちます。</span><span class="sxs-lookup"><span data-stu-id="49658-243">This functionality can be useful for scenarios where you're charged for each rate that is consumed from the service.</span></span>

