---
title: Finance and Operations バージョン 8.0 での為替レート プロバイダーの作成
description: このトピックでは、Microsoft Dynamics 365 for Finance and Operations バージョン 8.0 (2018 年 4 月) で為替レート プロバイダーを設定する方法について説明します。
author: RyanCCarlson2
ms.date: 09/25/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Developer
ms.reviewer: rhaertle
ms.custom: 72153
ms.assetid: 24643037-f7a5-4acf-b3d6-9943642b618c
ms.search.region: Global
ms.author: rcarlson
ms.search.validFrom: 2018-04-02
ms.dyn365.ops.version: AX 8.0.0
ms.openlocfilehash: 1215ba272504755a43c44899ae0fba7a316e3a0a10dbdbc2f5d09233a44d2c4d
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/05/2021
ms.locfileid: "6724325"
---
# <a name="create-exchange-rate-providers-in-finance-and-operations-version-80"></a>Finance and Operations バージョン 8.0 での為替レート プロバイダーの作成

[!include [banner](../includes/banner.md)]

このトピックでは、Microsoft Dynamics 365 for Finance and Operations バージョン 8.0 (2018 年 4 月) で為替レート プロバイダーを設定するために必要なステップについて説明します。 説明のために、このトピック全体で OANDA 為替レート サービスが使用されます。

このトピックで説明している手順に従って、機能為替レート プロバイダーを作成できます。 このコードは生産コードです。 ソースは **ExchangeRateProviderOanda** クラスで見つけることができます。 必要に応じて、このトピックからそのクラスを参照することができます。

OANDA テスト アカウントを要求し、OANDA 為替レートに関する情報を受け取るには、<https://developer.oanda.com/exchange-rates-api/> にアクセスしてください。

## <a name="terminology"></a>用語
- **現在の通貨為替レートをインポート** – 為替レート プロバイダーから為替レートを取得してインポートするプロセス。 このプロセスは、バッチ処理をサポートするシステム操作です。
- **為替レート プロバイダー** - 外部ソースから為替レートを取得する担当の X++ または C# クラス。
- **為替レート プロバイダー登録** - 使用できるように、為替レート プロバイダーを有効にするプロセス。 既定では、為替レート プロバイダーは配置されると登録されません。
- **為替レート プロバイダーのコンフィギュレーション**: 使用方法を決定する為替レート プロバイダーのコンフィギュレーション設定。
- **為替レート サービス** - 発行された為替レートの一覧を提供する無料または有料の定期売買サービス。 OANDA による外貨為替レートは、為替レートを提供するサービスの例です。
- **フレームワーク** – プロバイダーからの為替レートの取得および、それら為替レートの適切なストレージを調整するインポート通貨の為替レートのフレームワーク。

## <a name="conceptualclass-model"></a>概念/クラス モデル
次の図は、為替レート プロバイダーのフレームワークを構成する主なインターフェイスとクラス、およびそれらの関係を示しています。 新しい為替レート プロバイダーは、**IExchangeRateProvider** インターフェイスから実装されている必要があります。 為替レート プロバイダーは、X++ または C# で記述されます。 X++ は .NET 言語なので、 Microsoft .NET Framework を簡単に使用できます。 C# で記述されているすべてのプロバイダーは C# プロバイダーとして認識された X++ クラスでラップする必要があります。 たとえば、ヨーロッパ為替レート プロバイダーの中央銀行は Microsoft が C# で書き出したプロバイダーです。 **ExchangeRateProviderCBOE** X++ クラスによってラップされます。

[![為替レート プロバイダー フレームワークの概念/クラス モデル。](./media/exchangerates.png)](./media/exchangerates.png)

図で表示されるインターフェイスおよびクラスを次に示します。

- **IExchangeRateProvider** – このインタフェースを実装すると、為替レート プロバイダー フレームワークがクラスを為替レート プロバイダーとして認識できるようになります。
- **IExchangeRateProviderFrameworkFactory** – このインターフェイスにより、為替レート プロバイダーは、図の中のいくつかのインターフェイスを表す様々なタイプのプロバイダー フレームワーク クラスを作成することができます。
- **IExchangeRateProviderSupportedOptions** – 為替レート プロバイダーは、レートをインポートする際にいくつかのオプションをサポートします。 為替レート プロバイダーは、このインターフェイスを使用して、サポートするオプションについてフレームワークに通知します。
- **IExchangeRateProviderConfig** – 各為替レート プロバイダーは、固有のコンフィギュレーションを持つことができます。 このインターフェイスにより、プロバイダーはこの構成を取得できます。
- **IExchangeRateProviderConfigDefaults** – 為替レート プロバイダーは、構成のデフォルト値を作成して提供できます。 **為替レート プロバイダの構成** ページ (**総勘定元帳** &gt; **為替** &gt; **レート プロバイダーの構成**)でこれらの値を変更できます。
- **IExchangeRateRequest** – このインターフェイスは、為替レートのインポートを要求する固有のデータを表します。 このデータには、日付範囲、オプション、レートを取得するための通貨ペアが含まれます。
- **IExchangeRateCalendar** – このインターフェイスは、次の作業日 (月曜日から金曜日まで) を取得する場合に使用される為替レート カレンダーを表します。
- **IExchangeRateResponse** – 為替レート プロバイダーでは、このインターフェイスを使用して、通貨のペアや、サービスから返される為替レートを格納します。
- **IExchangeRateResponseCurrencyPair** – 為替レート プロバイダーでは、このインターフェイスを使用して、サービスから返される特定の通貨ペアの詳細を格納します。
- **IExchangeRateResponseExchangeRate** – 為替レート プロバイダーでは、このインターフェイスを使用して、特定の通貨ペアに対して特定の為替レートを格納します。
- **ExchangeRateProviderOanda** - Microsoft によって実装されている為替レート プロバイダーのこの例は、為替レートを返すために OANDA サービスに接続します。

## <a name="write-an-exchange-rate-provider"></a>為替レート プロバイダーの記述
為替レート プロバイダーを作成するには、これらの手順に従います。 このコード例は、**ExchangeRateProviderOanda** クラスから取得されています。

1. 拡張機能を使用して、新しい為替レート プロバイダーを表す **ExchangeRateProvider** の拡張可能列挙体に新しい値を追加します。
2. 開発モデルで、**IExchangeRateProvider** インターフェイスを実装するクラスを作成します。

    ```xpp
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

3. クラスに、次の定数と変数宣言を追加します。 **ProviderId** の独自のグローバル一意識別子 (GUID) を提供します。

    ```xpp
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

4. **get\_Name** メソッドを実装します。 ラベルを使用して、正しい変換を有効にする必要があります。 ユーザーは、プロバイダーの構成情報を設定すると、ここで指定されている名前を変更できます。

    ```xpp
    public ExchangeRateProviderName get_Name()
    {
        return "@CurrencyExchange:Currency_ConfigField_OandaName";
    }
    ```

5. **get\_Id** メソッドを実装します。 このメソッドは、このプロバイダーを一意に識別する GUID を返します。

    ```xpp
    public ExchangeRateProviderId get_Id()
    {
        return ProviderId;
    }
    ```

6. **set\_Factory** メソッドを実装します。 為替レート プロバイダー フレームワークは、このメソッドを呼び出して、プロバイダーの **IExchangeRateProviderFrameworkFactory** インターフェイスを実装するオブジェクトを設定します。 このファクトリを使用して、前の図のインターフェイスの一部を表す新しいオブジェクトのインスタンスを作成できます。

    ```xpp
    public void set_Factory(IExchangeRateProviderFrameworkFactory _factory)
    {
        factory = _factory;
    }
    ```

7. **GetSupportedOptions** メソッドを実装します。 このメソッドは、為替レート プロバイダーは、一部のフレームワーク機能をサポートするかどうかを示します。

   - 為替レートを取得するために渡すソース通貨およびターゲット通貨を渡すことが為替レート サービスに必要な場合にのみ、**doesSupportSpecificCurrencyPairs** プロパティを **true** に設定します。 多くの為替レート サービスが、固定通貨または通貨ペアの指定されたセットを返します。 これらのサービスについては、このプロパティは **false** に設定されます。 サービス料金が課金された料金の数がクォータ数に基づく場合、**true** の値により、**IExchangeRateRequest** インターフェイスには、**為替レート** ページ (**総勘定元帳** &gt; **通貨** &gt; **為替レート**) の為替レート タイプに設定されている通貨ペアのみを含まれるようになります。 プロバイダーはその後、これらの料金をサービスから具体的に要求できるため、コストを削減できます。
   - **fixedBaseIsoCurrency** プロパティを、為替レート サービスから返される為替レートの固定ベース通貨を表す 3 文字の国際標準化機構 (ISO) 通貨コードに設定します。 為替レート サービスが固定基本通貨をサポートしていない場合は、空の文字列を返します。 たとえば、ユーロは固定基本通貨としてよく使用されます。 新しいプロバイダーを作成するときは、正しい値を選択できるように、為替レート サービスをかならず調査してください。
   - サービスが日付範囲全体を表す単一のレートを返すことができる場合、**singleRateForDateRange** プロパティを **true** に設定します。 たとえば、1 か月の平均為替レートを表す単一の為替レートを返すには、この設定を使用できます。 サービスがこの機能をサポートしていない場合は、このプロパティを **false** に設定します。

     ```xpp
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

8. **GetConfigurationDefaults** メソッドを実装します。 既定のコンフィギュレーションは、為替レート プロバイダの既定コンフィギュレーションの設定を表す名前と値の組です。 これらの設定はプロバイダーが登録されたときに自動的に読み込まれますが、ユーザーは変更できます。 これらの文字列を使用可能な値に変換する場合は、必要な対策を講じてください。 値フィールドは、SQL で暗号化フィールドとして格納されます。 したがって、アプリケーション プログラミング インターフェイス (API) などの機密データはより安全になります。

    ```xpp
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

9. **ValidateConfigurationDetail** メソッドを実装します。 このメソッドにより、為替レート プロバイダーは、**為替レート プロバイダーの構成** ページでユーザーが変更する構成情報を検証できます。

    ```xpp
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

10. **EnumNameForLookup** メソッドを実装します。 このメソッドは、為替レート プロバイダーが特定の **ExchangeRateProviderPropertyKey** キーを参照できるようにします。 適切なキーに対して列挙された既存の型の名前を返します。 この機能が必要でない場合は、空の文字列を返します。

    ```xpp
    public str EnumNameForLookup(ExchangeRateProviderPropertyKey _key)
    {
        if (_key == "@CurrencyExchange:Currency_ConfigField_QuoteType")
        {
            return enumStr(ExchangeRateProviderOANDAQuoteType);
        }
        return '';
    }
    ```

11. **GetExchangeRates** メソッドを実装します。 このメソッドは、構成情報と、**IExchangeRateRequest** インターフェイスを使用して、交換レート サービスを呼び出すとともに、**IExchangeRateResponse** クラスの適切なインスタンスを返します。 このメソッドを記述するときは、以下の重要な点を考慮します。

    - 必要なすべてのコンフィギュレーション情報は **IExchangeRateProviderConfig** インターフェイスから取得する必要があります。 そのインターフェイスの **GetPropertyValue** メソッドへの呼び出しは、入力されたプロパティキーのプロパティ値の文字列形式を提供します。 この文字列値を別の型に変換する場合は、必要な対策を講じてください。
    - 事前に必要な検証を行います。 たとえば、OANDA は、すべてのサービス コールで API キーを指定するよう要求します。 この API キーが設定されていない場合は、サービスが失敗します。 API キーが設定されていない場合は、料金をインポートする前に終了するよう適切なエラー メッセージを表示することを確認します。
    - 一部のプロバイダーには、為替レートが要求される場合に明示的な通貨の組み合わせが必要です。 これらのプロバイダーは、**IExchangeRateProviderSupportedOptions.doesSupportSpecificCurrencyPairs** プロパティを **true** に設定したプロバイダーと同じです。 この場合、**IExchangeRateRequest** インターフェイスが提示する通貨ペアを使用して、取得プロセスを動作させる必要があります。 後に続く OANDA プロバイダーの実装には、このタイプのプロバイダーの適正例が示されます。 通常、特定の通貨の組み合わせをサポートしていないプロバイダーは、固定された通貨の組み合わせのデータを返します。 この場合、**IExchangeRateRequest** インターフェイスが提示する通貨ペアは無視できます。 プロバイダーは、使用できるすべてのレートを返す必要があります。 このフレームワークは、必要な通貨ペアを自動的に作成するかどうかに関するユーザーの決定に基づいて、正しいレートをインポートします。 CentralBankOfEuropeProvider プロバイダーは、このタイプのプロバイダーの適切な例です。
    - **IExchangeRateRequest** インターフェイスには、**ImportDateType** というプロパティがあります。 このプロパティは、サービスから為替レートを取得するために使用する日付を示します。 利用可能な 2 つの値は、**CurrentDate** と **DateRange** です。

        - **CurrentDate** は、為替レート サービスから最新の為替レートを取得します。 また、プロバイダーにこの値が渡されると、フレームワークは、**IExchangeRateRequest.FromDate** および **IExchangeRateRequest.ToDate** を、要求している Application Object Server (AOS) コンピュータのシステム日付に設定します。 為替レート サービスでは、特定の日付の為替レートの取得をサポート、フレームワークが提供する日付を渡す必要があります。 ただし、代わりに為替レート サービスが最新の為替レート (日付に関係なく) を取得する呼び出しを提供する場合、返される日付が要求日より前または同じ日付であることを確認するよう検証する必要があります。
        - **DateRange** は、特定の日付範囲の為替レートを取得します。 指定された日付範囲内の為替レートのみ許可される必要があります。 為替レート サービスで、特定の日付が要求に含まれることが必要とされる場合は、このプロセスは簡単です。 ただし、代わりに為替レート サービスが有効日の範囲外の可能性がある履歴日付のグループを返す場合、プロバイダーはフレームワークに日付を戻す前に該当しない日付を除外する必要があります。

    - 為替レートが返されるときは、**IExchangeRateRequest** クラスのインスタンスが提供する日付ではなく、為替レート サービスが提供する日付を常に使用します。 この方法では、為替レート サービスが予期されていない日付のレートを返す場合があるため、返される為替レートが正しい日付に関連付けられていることを保証できます。 たとえば、将来の日付に対して為替レートが要求されると、一部のプロバイダーは、エラーをスローしたり何も返さない代わりに、最新の為替レートを返します。
    - 為替レート サービスからの為替レートを取得するときにエラーが発生する場合は、カスタム エラー メッセージをスローしないようにします。 このフレームワークは、予想される通貨ペアをプロバイダーから取得できないという一般的なエラーメッセージを投げて問題があることをユーザーに警告します。 その他のエラーのログを記録する必要がある場合、**CurrencyEventSource** を使用します。 例については、次のコードで **catch** ステートメントおよび **oandaKey** 変数に対する **IF** 条件を参照してください。。

    ```xpp
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

12. 次のヘルパー メソッドを実装します。 これらのメソッドはこの例に固有のものであり、すべてのプロバイダーに必須ではありません。

    ```xpp
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

13. **ExchangeRateProviderOanda** クラスをコンパイルします。 プロバイダーは、SysOperation の一部として実行されます。 問題をデバッグするときに、次のフレームワーク クラスおよびメソッドを理解しておくと便利です。

    - **ExchangeRateProviderFactory.initialize()** - このメソッドは、為替レート プロバイダーのインスタンスを作成し、為替レートの登録またはインポート時に呼び出されます。 プロバイダーにインスタンスが作成されていない場合、ここでデバッグを開始します。
    - **ExchangeRateProviderRegistration.initialize()** - このメソッドはプロバイダーを検索し、プロバイダーを登録できるようにします。 登録ページでプロバイダーがわからない場合は、ここでデバッグを開始します。
    - **ExchangeRateImportOperation.import()** - このメソッドでは、必要なプロバイダーを呼び出して為替レートを保存することによって、インポート プロセスを駆動します。
    - **ExchangeRateProviderConfig** - このクラスはプロバイダーのコンフィギュレーション情報へのアクセスを提供します。

## <a name="ideas-to-consider"></a>考慮する必要があるアイデア
為替レートの取得には為替レートのプロバイダーが使用するメソッドに制限がないため、このフレームワークはいくつかの興味深いシナリオを有効にします。 参照するアイデアを次に示します。

- **他の為替レート タイプからの為替レートを取得するプロバイダー** – このシナリオを実装すると、さまざまな為替レート タイプ間の為替レートの同期が可能になります。 この機能は、さまざまな元帳間の分離を維持するために、多くの為替レート タイプが存在する状況で役立ちます。
- **為替レート サービスの任意の形式を ExchangeRateResponse クラスのインスタンスに変換するために Extensible Stylesheet Language Transformations (XSLT) を使用するプロバイダー** – このシナリオを実装すると、ユーザーは為替レート サービスに必要な XSLT 変換を追加することができ、アプリケーションはそのサービスをサポートします。 プロバイダー固有のコードは必要ありません。
- **一部の為替レート プロバイダー サービスは、消費されるすべてのレートに対して料金を請求します** – このリストの最初のアイデアと、サービスから取得するレートの数の制限を組み合わせることを検討してください。 この機能は、サービスから消費される料金ごとに課金されるシナリオに役立ちます。


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]