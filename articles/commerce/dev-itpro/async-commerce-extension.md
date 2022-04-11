---
title: ビジネス ロジックで非同期コマース (CRT) API を作成する
description: このトピックでは、非同期で実行される コマース (CRT) アプリケーション プログラミング インターフェイス (API) (つまり、要求) の作成方法について説明します。
author: mugunthanm
ms.date: 03/16/2022
ms.topic: article
audience: Developer
ms.reviewer: tfehr
ms.search.region: Global
ms.author: mumani
ms.search.validFrom: 2020-02-02
ms.dyn365.ops.version: 10.0.10
ms.openlocfilehash: 3b6880ed98214d229d8501fa30b7477fa6544485
ms.sourcegitcommit: 6fd739976b46122f9a9002309aba60edb89e5468
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/16/2022
ms.locfileid: "8453500"
---
# <a name="create-asynchronous-commerce-crt-apis-in-your-business-logic"></a>ビジネス ロジックで非同期コマース (CRT) API を作成する

[!include [banner](../../includes/banner.md)]

> [!NOTE]
> このトピックは、Microsoft Dynamics 365 Commerce バージョン 10.0.10 およびそれ以降に適用されます。

このトピックでは、新しい非同期フレームワークを使用して Commerce Runtime (CRT) 用の新しいビジネス ロジック (アプリケーション プログラミング インターフェイス、または API) を作成する方法について説明します。 コマース API フレームワークでは、拡張機能および標準のコマース ハンドラーの非同期プログラミング モデルがサポートされるようになりました。

このフレームワーク拡張機能が追加される前は、要求が同期的にのみ実行できました。 入力/出力 (I/O) 操作、データベース クエリ、またはネットワーク要求などの長い操作により、実行スレッドがブロックされました。 非同期モデルのサポートが Commerce Runtime (CRT) に追加されたので、これらの操作の非同期バージョンを使用できます。 非同期要求は、実行スレッドをブロック解除します。

コマース API フレームワークでは、拡張 CRT 要求ハンドラーの **非同期** および **待機** キーワードでサポートされる、**タスク** および **タスク\<T\>** クラスがサポートされるようになりました。 すべての新しい拡張 API に対して非同期のコマース API フレームワークを使用し、拡張機能には標準の非同期コマース API を使用する必要があります。

## <a name="async-classesinterface-added-in-the-commerce-api-framework"></a>コマース API フレームワークに追加された非同期クラス/インターフェイス

次の非同期クラスおよびインターフェイスが、コマース API フレームワークに追加されました。

| クラス/インターフェイス                     | 説明 |
|---------------------------|-------------|
| SingleAsyncRequestHandler | 1 つの要求のみをサポートする非同期ハンドラーの基本クラス。 |
| IRequestHandlerAsync      | 非同期要求ハンドラーのインターフェイス。 |
| IRequestTriggerAsync      | 要求トリガーのインターフェイス。 |
| CommerceControllerAsync   | 非同期拡張機能 Retail サーバー コントローラー クラスの基本クラス。 |
| DatabaseContext           | 非同期データベース実行メソッドの基本クラス。 |

次の非同期メソッドが、コマース API フレームワークに追加されました。

| クラス/インターフェイス           | メソッド                                              | 説明 |
|---------------------------|-----------------------------------------------------|-------------|
| `SingleAsyncRequestHandler` | `Task\<TResponse\> Process`                           | 各派生クラスによって上書きされる実行メソッド。 |
|                           | `Task\<Response\> Execute`                            | 要求ハンドラーのエントリ ポイントを表すメソッド。 |
| `IRequestHandlerAsync`      | `Task\<Response\> Execute (Request request)`          | 非同期要求ハンドラーのインターフェイス。 |
| `IRequestTriggerAsync`      | `Task OnExecuting(Request request)`                   | 要求が **IRequestHandler** によって処理される前に呼び出されるメソッド。 |
| `IRequestTriggerAsync`      | `Task OnExecuted(Request request, Response response)` | 要求が **IRequestHandler** によって処理された後に呼び出されるメソッド。 |
| `DatabaseContext`           | `async Task<Tuple<int, PagedResult<T>>> ExecuteStoredProcedureAsync<T>(string procedureName, ParameterSet parameters, QueryResultSettings resultSettings)` | 指定されたパラメーターを使用して、ストアド プロシージャを実行するメソッド。 |
| `DatabaseContext`           | `async Task<ReadOnlyCollection<T>> ExecuteNonPagedStoredProcedureAsync<T>(string procedureName, ParameterSet parameters, QueryResultSettings resultSettings) where T : CommerceEntity, new()` | 指定されたパラメーターを使用して、ストアド プロシージャを実行するメソッド。 実行はページ設定されていません。 |
|`DatabaseContext`            | `async Task<Tuple<PagedResult<T1>, ReadOnlyCollection<T2>>> ExecuteStoredProcedureAsync<T1, T2>(string procedureName, ParameterSet parameters, QueryResultSettings resultSettings) where T1 : CommerceEntity, new() where T2 : CommerceEntity, new()` | 指定されたストアド プロシージャを実行するメソッド。 |
| `DatabaseContext`                          | `async Task<Tuple<int, Tuple<PagedResult<T1>, ReadOnlyCollection<T2>>>> ExecuteStoredProcedureAsync<T1, T2>(string procedureName, ParameterSet parameters, ParameterSet outputParameters, QueryResultSettings resultSettings) where T1 : CommerceEntity, new() where T2 : CommerceEntity, new()` | 指定されたストアド プロシージャを実行するメソッド。 |
|`DatabaseContext`                        | `async Task<Tuple<PagedResult<T1>, ReadOnlyCollection<T2>, ReadOnlyCollection<T3>>> ExecuteStoredProcedureAsync<T1, T2, T3>(string procedureName, ParameterSet parameters, QueryResultSettings resultSettings) where T1 : CommerceEntity, new() where T2 : CommerceEntity, new() where T3 : CommerceEntity, new()` | 指定されたストアド プロシージャを実行するメソッド。 |
| `DatabaseContext`                          | `async Task<Tuple<int, Tuple<PagedResult<T1>, ReadOnlyCollection<T2>, ReadOnlyCollection<T3>>>> ExecuteStoredProcedureAsync<T1, T2, T3>(string procedureName, ParameterSet parameters, ParameterSet outputParameters, QueryResultSettings resultSettings) where T1 : CommerceEntity, new() where T2 : CommerceEntity, new()  where T3 : CommerceEntity, new()` | 指定されたストアド プロシージャを実行するメソッド。 |
| `DatabaseContext`                           | `async Task<Tuple<PagedResult<T1>, ReadOnlyCollection<T2>, ReadOnlyCollection<T3>, ReadOnlyCollection<T4>>> ExecuteStoredProcedureAsync<T1, T2, T3, T4>(string procedureName, ParameterSet parameters, QueryResultSettings resultSettings) where T1 : CommerceEntity, new() where T2 : CommerceEntity, new() where T3 : CommerceEntity, new() where T4 : CommerceEntity, new()` | 指定されたストアド プロシージャを実行するメソッド。 |
| `DatabaseContext`           | `async Task<Tuple<int, Tuple<PagedResult<T1>, ReadOnlyCollection<T2>, ReadOnlyCollection<T3>, ReadOnlyCollection<T4>>>> ExecuteStoredProcedureAsync<T1, T2, T3, T4>(string procedureName, ParameterSet parameters, ParameterSet outputParameters, QueryResultSettings resultSettings) where T1 : CommerceEntity, new() where T2 : CommerceEntity, new() where T3 : CommerceEntity, new() where T4 : CommerceEntity, new()` | 指定されたストアド プロシージャを実行するメソッド。 |
|`DatabaseContext`   | `async Task<Tuple<PagedResult<T1>, ReadOnlyCollection<T2>, ReadOnlyCollection<T3>, ReadOnlyCollection<T4>, ReadOnlyCollection<T5>, ReadOnlyCollection<T6>, ReadOnlyCollection<T7>, Tuple<ReadOnlyCollection<T8>>>> ExecuteStoredProcedureAsync<T1, T2, T3, T4, T5, T6, T7, T8>(string procedureName, ParameterSet parameters, QueryResultSettings resultSettings) where T1 : CommerceEntity, new() where T2 : CommerceEntity, new() where T3 : CommerceEntity, new() where T4 : CommerceEntity, new() where T5 : CommerceEntity, new() where T6 : CommerceEntity, new() where T7 : CommerceEntity, new() where T8 : CommerceEntity, new()` | 指定されたストアド プロシージャを実行するメソッド。 |
| `DatabaseContext`    | `Task<Tuple<int, Tuple<PagedResult<T1>, ReadOnlyCollection<T2>, ReadOnlyCollection<T3>, ReadOnlyCollection<T4>, ReadOnlyCollection<T5>, ReadOnlyCollection<T6>, ReadOnlyCollection<T7>, Tuple<ReadOnlyCollection<T8>>>>> ExecuteStoredProcedureAsync<T1, T2, T3, T4, T5, T6, T7, T8>(string procedureName, ParameterSet parameters, ParameterSet outputParameters, QueryResultSettings resultSettings) where T1 : CommerceEntity, new() where T2 : CommerceEntity, new() where T3 : CommerceEntity, new() where T4 : CommerceEntity, new() where T5 : CommerceEntity, new() where T6 : CommerceEntity, new() where T7 : CommerceEntity, new() where T8 : CommerceEntity, new()` | 指定されたストアド プロシージャを実行するメソッド。 |
| `DatabaseContext`       | `Task<ReadOnlyCollection<T>> ExecuteStoredProcedureScalarCollectionAsync<T>(string procedureName, ParameterSet parameters, QueryResultSettings resultSettings)`                   | 単一の結果のコレクションを返すクエリを実行します。 |
| `DatabaseContext`       | `Task<int> ExecuteStoredProcedureNonQueryAsync(string procedureName, ParameterSet parameters, QueryResultSettings resultSettings)` | 指定されたパラメーターを使用して、指定されたストアド プロシージャを実行するメソッド。 |
| DatabaseContext       | `Task<int> ExecuteStoredProcedureScalarAsync(string procedureName, ParameterSet parameters, QueryResultSettings resultSettings)` | 指定されたパラメーターを使用して戻り値を返す、ストアド プロシージャを実行するメソッド。 |
| `DatabaseContext`      | `Task OnExecuting(Request request)`                   | 指定されたパラメーターを使用して戻り値を返す、ストアド プロシージャを実行します。 |
| `DatabaseContext`      | `Task<int> ExecuteStoredProcedureScalarAsync(string procedureName, ParameterSet parameters, ParameterSet outputParameters, QueryResultSettings resultSettings)` | 指定されたパラメーターを使用して戻り値を返す、ストアド プロシージャを実行するメソッド。 |
| `DatabaseContext`       | `Task<PagedResult<T>> ReadEntityAsync<T>(IDatabaseQuery query) where T : CommerceEntity, new()`  | データベースからエンティティを読み取るメソッド。 |
| `DatabaseContext`       | `Task ExecuteNonQueryAsync(IDatabaseQuery query)`                   | 出力のないクエリを実行するメソッド。 |
| `DatabaseContext`       | `Task<T> ExecuteScalarAsync<T>(IDatabaseQuery query)`                   | 出力のないクエリを実行するメソッド。 |
| `DatabaseContext`       | `Task<ReadOnlyCollection<T>> ExecuteScalarCollectionAsync<T>(IDatabaseQuery query)`                   | 単一の結果のコレクションを返すクエリを実行するメソッド。 |

非同期実行は、次のようなシナリオでサポートされます。

+ 新しいコマース API

    - 非同期 Commerce Runtime API
    - 非同期 Retail サーバー コントローラー

+ 実行中のコマース API ハンドラーの上書き
+ プレトリガーとポストトリガー

> [!NOTE]
> 拡張機能コードに対して、要求の実行時に ConfigureAwait (いいえ) を使用することをお勧めします。

## <a name="create-a-new-asynchronous-commerce-runtime-api"></a>新しい非同期 Commerce Runtime API の作成

新しい非同期コマース API を作成するには、次の 3 つのクラスを作成する必要があります。

+ **要求** クラスを実装することにより、要求クラスを作成します。
+ **応答** クラスを実装することにより、非同期応答クラスを作成します。
+ 非同期ハンドラー クラスを作成します。

クラスを作成するには、次の手順に従います。

1. 要求クラスを作成します。

    ```C#
    namespace Contoso
    {
        namespace Commerce.Runtime.AsyncRequestSample.Messages
        {
            using System.Runtime.Serialization;
            using System;
            using Microsoft.Dynamics.Commerce.Runtime.Messages;
    
            /// <summary>
            /// Sample request for AsyncRequestSampleRequest
            /// </summary>
            [DataContract]
            public sealed class AsyncRequestSampleRequest : Request
            {
                /// <summary>
                /// Initializes a new instance of the <see cref="AsyncRequestSampleRequest"/> class.
                /// </summary>
                public AsyncRequestSampleRequest()
                {
                }
    
            }
        }
    }
    ```

2. 応答クラスを作成します。

    ```C#
    namespace Contoso
    {
        namespace Commerce.Runtime.AsyncSample.Messages
        {
            using System.Runtime.Serialization;
            using Microsoft.Dynamics.Commerce.Runtime.Messages;
            using Microsoft.Dynamics.Commerce.Runtime.DataModel;
    
            /// <summary>
            /// Defines a simple response class .
            /// </summary>
            [DataContract]
            public sealed class AsyncSampleResponse : Response
            {
                /// <summary>
                /// Initializes a new instance of the <see cref="AsyncSampleResponse"/> class.
                /// </summary>
                /// <param name="CustomerRec">Customer.</param>
                public AsyncSampleResponse(Customer customer)
                {
                    this.CustomerRec = customer;
                }
    
                /// <summary>
                /// Gets the customer related to the request.
                /// </summary>
                [DataMember]
                public Customer CustomerRec { get; private set; }
    
            }
        }
    }
    ```

3. 非同期ハンドラーを作成します。

    ```C#
    using Contoso.Commerce.Runtime.AsyncSample.Messages;
    using System.Linq;
    using System.Threading.Tasks;
    using Microsoft.Dynamics.Commerce.Runtime;
    using Microsoft.Dynamics.Commerce.Runtime.DataModel;
    using Microsoft.Dynamics.Commerce.Runtime.Services.Messages;
    
    namespace Commerce.Runtime.AsyncSample.Messages
    {
        public class AsyncSampleRequestHandler : SingleAsyncRequestHandler<AsyncSampleRequest, AsyncSampleResponse>
        {
            protected override async Task<AsyncSampleResponse> Process(AsyncSampleRequest request)
            {
                var customers = await AsyncSampleMethodGetCustomer(request.RequestContext);
    
                return new AsyncSampleResponse(customers);
            }
    
            private async Task<Customer> AsyncSampleMethodGetCustomer(RequestContext context)
            {
                //do custom logic here. Execute any custom logic or request asynchronously.
                var getCustomerRequest = new GetCustomersServiceRequest(QueryResultSettings.SingleRecord, "2001", SearchLocation.Local);
                var getCustomerResponse = await context.ExecuteAsync<GetCustomersServiceResponse>(getCustomerRequest);
                return getCustomerResponse.Customers.SingleOrDefault();
            }
        }
    }
    ```

## <a name="create-a-new-asynchronous-retail-server-controller"></a>新しい非同期 Retail サーバー コントローラーの作成

非同期の Retail サーバー コントローラー拡張機能を作成するには、次の例に示すように、**CommerceControllerAsync** クラスからコントローラー クラスを拡張します。

```C#
namespace Microsoft.Dynamics.Retail.RetailServerLibrary.ODataControllers
{
    using System.Runtime.InteropServices;
    using System.Threading.Tasks;
    using System.Web.Http.Controllers;
    using System.Web.OData;
    using Commerce.Runtime;
    using Commerce.Runtime.Client;
    using Commerce.Runtime.DataModel;

    /// <summary>
    /// The catalogs controller.
    /// </summary>
    [ComVisible(false)]
    public class CustomController : CommerceControllerAsync<MyEntity, string>
    {

        /// <summary>
        /// Gets the controller name.
        /// </summary>
        public override string ControllerName
        {
            get { return "MyEntity"; }
        }

        /// <summary>
        /// Gets the <c>MyEntity</c> entity by key.
        /// </summary>
        /// <param name="key">
        /// The key.
        /// </param>
        /// <returns>
        /// The <see cref="ScanResult"/>.
        /// </returns>
        [CommerceAuthorization(CommerceRoles.Employee)]
        protected override Task<MyEntity> GetEntityByKey(string key)
        {
            return this.GetMyEntityAsync(key);
        }

        /// <summary>
        /// Retrieves the entity information based on <see cref="key"/> input.
        /// </summary>
        /// <param name="key">key input.</param>
        /// <returns>Instance of <see cref="MyEntity"/> that contains entities found by input text.</returns>
        public async Task<MyEntity> GetMyEntityAsync(string key)
        {
            ThrowIf.Null(key, nameof(key));

            var request = new MyCustomRequest(key);
            var response = await this.runtime.ExecuteAsync<MyCustomResponse>(request).ConfigureAwait(false);
            return response.Result;
        }

    }
}
```

## <a name="override-an-out-of-box-request-handler-asynchronously"></a>標準の要求ハンドラーを非同期に上書きする

サポートされる標準の要求ハンドラーを上書きするには、このパターンに従います。

たとえば、標準の **GetScanResultRequestHandler** ハンドラーを上書きするには、ハンドラーを上書きしてから、**タスク** と **待機** を使用して応答を返します。

```C#
namespace Contoso
{
    namespace Commerce.Runtime.Workflow
    {
        using System.Linq;
        using System.Threading.Tasks;
        using Microsoft.Dynamics.Commerce.Runtime;
        using Microsoft.Dynamics.Commerce.Runtime.DataModel;
        using Microsoft.Dynamics.Commerce.Runtime.Messages;
        using Microsoft.Dynamics.Commerce.Runtime.Services.Messages;

        /// <summary>
        /// Workflow that retrieves information based on scan input.
        /// </summary>
        public class GetScanResultRequestHandler : SingleAsyncRequestHandler<GetScanResultRequest, GetScanResultResponse>
        {
            /// <summary>
            /// Executes the workflow to get scan result.
            /// </summary>
            /// <param name="request">Instance of <see cref="GetScanResultRequest"/>.</param>
            /// <returns>Instance of <see cref="GetScanResultResponse"/>.</returns>
            protected override async Task<GetScanResultResponse> Process(GetScanResultRequest request)
            {
                ThrowIf.Null(request, nameof(request));

                var getBarcodeRequest = new GetBarcodeRequest(request.ScanInfo);
                var getBarcodeResponse = request.RequestContext.Execute<GetBarcodeResponse>(getBarcodeRequest);
                Barcode barcode = getBarcodeResponse.Barcode;
                BarcodeMaskType maskType = barcode == null ? BarcodeMaskType.None : barcode.Mask.MaskType;
                ScanResult result = new ScanResult(request.ScanInfo.ScannedText) { Barcode = barcode, MaskType = maskType };

                //For this sample, we skipped lot of logic inside this method. This should be used only for reference on how to override OOB request. The logic written inside this sample is different from the actual implementation of this handler.

                result.Product = await this.GetSingleProductByItemId(request.RequestContext, barcode.ItemBarcode.ItemId, barcode.ItemBarcode.InventoryDimensionId).ConfigureAwait(false);

                return new GetScanResultResponse(result);

            }

            private async Task<SimpleProduct> GetSingleProductByItemId(RequestContext context, string itemId, string inventDimId)
            {
                //do custom logic here. Execute any custom logic or request asynchronously.

                if (string.IsNullOrWhiteSpace(itemId))
                {
                    return null;
                }

                var lookupClause = new ProductLookupClause { ItemId = itemId, InventDimensionId = inventDimId };

                var getProductRequest = new GetProductsServiceRequest(
                    context.GetPrincipal().ChannelId,
                    new[] { lookupClause },
                    QueryResultSettings.AllRecords);
                getProductRequest.SearchLocation = SearchLocation.Local;  // Scanned products must be found locally.
                var products = (await context.ExecuteAsync<GetProductsServiceResponse>(getProductRequest).ConfigureAwait(false)).Products;

                if (products.Results.IsNullOrEmpty() || products.Results.HasMultiple())
                {
                    // if product is not found or multiple products founds (not exact match) return 'null'
                    return null;
                }

                return products.Results.Single();

            }

        }
    }
}
```

## <a name="create-a-trigger-asynchronously"></a>トリガーを非同期に作成する

トリガーのロジックを非同期で実行するには、**irequesttriggerasync** インターフェイスを拡張してから、ロジックを追加します。

```C#
namespace Contoso
{
    using System;
    using System.Collections.Generic;
    using System.Composition;
    using System.Threading.Tasks;
    using Microsoft.Dynamics.Commerce.Runtime.Messages;
    using Microsoft.Dynamics.Commerce.Runtime.DataServices.Messages;

    /// <summary>
    /// Test implementation of request trigger for <see cref="TestRequest"/>.
    /// </summary>
    public class SampleRequestTriggerAsync : IRequestTriggerAsync
    {
        private readonly Func<Task> onExecutingCallback;
        private readonly Func<Task> onExecutedCallback;

        public TestRequestTriggerAsync()
        {
        }

        [ImportingConstructor]
        public TestRequestTriggerAsync([Import("OnExecutingCallback")]Func<Task> onExecutingCallback, [Import("OnExecutedCallback")]Func<Task> onExecutedCallback)
        {
            this.onExecutingCallback = onExecutingCallback;
            this.onExecutedCallback = onExecutedCallback;
        }

        /// <summary>
        /// Gets the collection of request types supported by this trigger.
        /// </summary>
        public IEnumerable<Type> SupportedRequestTypes
        {
            get
            {
                return new[]
                {
                    // Add the request for pre or post trigger execution.
                    typeof(GetCustomerDataRequest)
                };
            }
        }

        /// <summary>
        /// Invoked before request has been processed by <see cref="IRequestHandler"/>.
        /// </summary>
        /// <param name="request">The incoming request message.</param>
        /// <returns>The empty Task.</returns>
        public Task OnExecuting(Request request)
        {
            if (this.onExecutingCallback != null)
            {
                return this.onExecutingCallback();
            }

            return Task.CompletedTask;
        }

        /// <summary>
        /// Invoked after request has been processed by <see cref="IRequestHandler"/>.
        /// </summary>
        /// <param name="request">The request message processed by handler.</param>
        /// <param name="response">The response message generated by handler.</param>
        /// <returns>The empty Task.</returns>
        public Task OnExecuted(Request request, Response response)
        {
            if (this.onExecutedCallback != null)
            {
                return this.onExecutedCallback();
            }

            return Task.CompletedTask;
        }
    }
}
```

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
