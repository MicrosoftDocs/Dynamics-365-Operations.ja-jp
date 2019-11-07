---
title: Retail ソフトウェア開発キット (SDK) のサンプル
description: このトピックでは、2016 年 12 月に Retail SDK と共にリリースされた 3 つの新しいサンプルについて説明します。
author: mugunthanm
manager: AnnBe
ms.date: 10/22/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Developer
ms.reviewer: rhaertle
ms.search.scope: Operations, Retail
ms.custom: 266164
ms.assetid: d24470fd-07ad-4c3f-b23a-3f6c1401edc6
ms.search.region: Global
ms.author: mumani
ms.search.validFrom: 2016-08-30
ms.dyn365.ops.version: Platform update 2
ms.openlocfilehash: a88dddd6d4ceb105a3f29c750fd1c72d43441ff6
ms.sourcegitcommit: fb66731f05207094149a6bc7b8549a4dabbb071a
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/22/2019
ms.locfileid: "2652000"
---
# <a name="retail-software-development-kit-sdk-samples"></a>Retail ソフトウェア開発キット (SDK) のサンプル

[!include [banner](../../includes/banner.md)]

このトピックでは、2016 年 12 月に Retail SDK と共にリリースされた 3 つの新しいサンプルについて説明します。

## <a name="override-message-handler-sample"></a>メッセージ ハンドラーのサンプルをオーバーライド

**シナリオ:** Fabrikam の顧客の 1 人が顧客関係管理 (CRM) システムに参加していても、Microsoft Dynamics 365 Retail にインポートされていない場合があります。 したがって、Fabrikam は、CRM システムと POS (販売時点管理) から顧客を検索したいと考えています。 業務要件を次に示します。

- CRM システムと POS から顧客を検索します。
- 結果をマージして、Retail Modern POS (MPOS) で統合された結果セットを表示します。

オーバーライド メッセージ ハンドラーを使用する場合があるいくつかの状況を次に示します。

- 在庫の更新や照会のためにサード パーティ在庫システムの使用を必要とします。
- 税金の計算のために、外部の税システムとの統合を必要としています。
- サード パーティのロイヤルティ システムとの統合を必要としています。

サンプルの基本的な作業を次に示します。

1. 外部の検索が実行できるように既存の検索の動作を変更するため、既存の顧客検索要求をオーバーライドして実装します。
2. 外部検索が完了した後、標準検索の要求を呼び出し、両方の結果をマージします。

これらのタスクのコードを次に示します。

```
public sealed class CustomerSearchRequestHandler : SingleRequestHandler<CustomersSearchRequest, CustomersSearchResponse>
{
    /// <summary>
    /// Executes the workflow to retrieve customer information.
    /// </summary>
    /// <param name="request">The request.</param>
    /// <returns>The response.</returns>
    protected override CustomersSearchResponse Process(CustomersSearchRequest request)
    {
        ThrowIf.Null(request, "request");
        ThrowIf.Null(request.Criteria, "request.Criteria");
        // Execute custom customer search logic here.
        CustomersSearchResponse externalResponse = this.ExternalCustomerSearch(request.Criteria.Keyword);
        // Execute original customer search logic.
        var requestHandler = new Microsoft.Dynamics.Commerce.Runtime.Workflow.CustomerSearchRequestHandler();
        CustomersSearchResponse originalResponse = 
            request.RequestContext.Runtime.Execute<CustomersSearchResponse>(request, request.RequestContext, requestHandler, skipRequestTriggers: false);
        return new CustomersSearchResponse(externalResponse.Customers.Union(originalResponse.Customers).AsPagedResult());
    }
}
```

完全なサンプルコードは、ソフトウェアの開発キット (SDK) の RetailSDK\\SampleExtensions\\CommerceRuntime\\Extensions.CustomerSearchSample フォルダーにあります。

### <a name="best-practice"></a>ベスト プラクティス

既存の要求または応答の動作を完全に変更する場合、または標準ロジックに加えてロジックを使用する場合は、標準のメッセージ ハンドラーをオーバーライドします。

## <a name="request-handler-triggers-and-extension-properties-sample"></a>要求ハンドラー トリガーおよび拡張プロパティのサンプル

**シナリオ:** Fabrikam が電子メール マーケティングに関する顧客電子メールの基本設定を収集します。 業務要件を次に示します。

- 顧客の電子メールの基本設定の収集と更新をPOS から行えるようにします。
- 顧客の電子メールの基本設定はすぐに有効になります。

拡張機能プロパティを使用する場合があるいくつかの状況を次に示します。

- 顧客や販売注文などのエンティティの拡張を望んでいますが、新しい別のエンティティの作成を望んでいません。
- 新しいエンティティ フィールドはデータベースから読み取り、または書き込みがおこなわれますが、commerce runtime (CRT) と POS の間で送信し、クライアントで更新される必要があります。
- カスタム ロジックの流れを管理するために使用できる、一時的な内部フラグが必要です。
- レシートを生成するときにレシート カスタマイズがアクセスする、カスタム レシート フィールドを設定する必要があります。

次の手順は、CRT コードの変更を示しています。 MPOS およびチャンネル データベースで、サンプル全体を参照してください。 次のサンプルは、標準的なデータベース コンポーネントへの変更が必要となった場合に前のコードとは異なることに注意してください。 (たとえば、新しい列を拡張プロパティとして公開するには、ビューへの変更が必要になります。 拡張機能のプロパティの一覧を受信し、これらのプロパティを標準フィールドと共に更新するには、ストアド プロシージャの変更が必要でした。最終的にインラインで変更されていないモデルに移行すると、データベースが更新されてもマージ競合は発生しません。 したがって、エンティティの読み込み、書き込み、更新のために個別のデータベース呼び出しを行うことをお勧めします。

1. **エンティティの読み取り** **GetCustomerDataRequest** の転記トリガーを実装し、チャネル データベースから値を読み取って拡張プロパティに値を追加します。

    ```
    public class GetCustomerTriggers : IRequestTrigger
    {
        public IEnumerable<Type> SupportedRequestTypes
        {
            get { return new[] { typeof(GetCustomerDataRequest) }; }
        }
        public void OnExecuted(Request request, Response response)
        {
            // Check if default handler found a customer.
            var customer = ((SingleEntityDataServiceResponse<Customer>)response).Entity;
            if (customer == null)
            {
                return;
            }
            // Read from a custom view mapped to a custom table.
            var query = new SqlPagedQuery(QueryResultSettings.SingleRecord)
            {
                Select = new ColumnSet(new string[] { "EMAILOPTIN" }),
                From = "CUSTOMEREXTENSIONVIEW",
                Where = "ACCOUNTNUM = @accountNum AND DATAAREAID = @dataAreaId"
            };
            query.Parameters["@accountNum"] = customer.AccountNumber;
            query.Parameters["@dataAreaId"] = request.RequestContext.GetChannelConfiguration().InventLocationDataAreaId;
            using (var databaseContext = new SqlServerDatabaseContext(request))
            {
                // Use ExtensionEntity which will map all columns to extension properties.
                ExtensionsEntity extensions = databaseContext.ReadEntity<ExtensionsEntity>(query).FirstOrDefault();
                var emailOptIn = extensions != null ? extensions.GetProperty("EMAILOPTIN") : null;
                // If the EmailOptIn is found, set it at a new extension property at the Customer.
                if (emailOptIn != null)
                {
                    customer.SetProperty("EMAILOPTIN", emailOptIn);
                }
            }
        }
    }
    ```

2. **エンティティの書き込み。** **CreateOrUpdateCustomerDataRequest** のハンドラーをオーバーライドし、トランザクション スコープ内で元のリクエスト ハンドラーとカスタム ストアド プロシージャを実行します。 データベース トランザクションが必要ではない場合は、ポスト トリガーで十分です。

    ```
    protected override SingleEntityDataServiceResponse<Customer> Process(CreateOrUpdateCustomerDataRequest request)
    {
        using (var databaseContext = new SqlServerDatabaseContext(request))
        using (var transactionScope = new TransactionScope())
        {
            // Execute original functionality to save the customer.
            var requestHandler = new Microsoft.Dynamics.Commerce.Runtime.DataServices.SqlServer.CustomerSqlServerDataService();
            var response = (SingleEntityDataServiceResponse<Customer>)requestHandler.Execute(request);
            // Execute additional functionality to save the customer's extension properties.
            if (!request.Customer.ExtensionProperties.IsNullOrEmpty())
            {
                // The stored procedure will determine which extension properties are saved to which tables.
                ParameterSet parameters = new ParameterSet();
                parameters["@TVP_EXTENSIONPROPERTIESTABLETYPE"] = new ExtensionPropertiesTableType(request.Customer.RecordId, request.Customer.ExtensionProperties).DataTable;
                databaseContext.ExecuteStoredProcedureNonQuery("UPDATECUSTOMEREXTENSIONPROPERTIES", parameters);
            }
            transactionScope.Complete();
            return response;
        }
    }
    ```

このサンプルを実行する前に、チャネル データベースでカスタム テーブル、ビュー、およびストアド プロシージャを作成することを確認します。 また、MPOS に関連する変更を行います。 追加のコメントと共に、完全なサンプル コードが、RetailSDK\\SampleExtensions\\CommerceRuntime\\Extensions.EmailPreferenceSample フォルダーにあります。 カスタム データベース アーティファクトを作成する方法の詳細については、SDK の RetailSDK\\Documents\\SampleExtensionsInstructions\\EmailPreference フォルダを参照してください。

> [!NOTE]
> 上記のコード サンプルと RetailSDK\\Documents\\SampleExtensionsInstructions\\emailpreference フォルダー内のサンプル スクリプトでは、[crt].EXTENSIONPROPERTIESTABLETYPE が使用されます。 バージョン 7.3 以降では、ext スキーマで crt または ax スキーマのオブジェクト/データ型の使用がサポートされなくなりました。 ext スキーマで、カスタム拡張テーブル プロパティ型を作成して使用する必要があります。

### <a name="best-practice"></a>ベスト プラクティス

トリガーが連鎖されている場合トリガーの順序は保証されていないため、また内部キャッシュ メカニズムのために、プレトリガーは*要求*メッセージを変更してはならず、ポストトリガーは*応答*メッセージを変更できません。 拡張プロパティは、コア プロパティが変更されていないため、許可されます。 機能拡張プロパティを処理するには、プリトリガーとポストトリガーを使用する必要があります。 また、検証を行うためにプレトリガーを使用し、追加のアクションを行うためにポストトリガーを使用する必要があります。

## <a name="custom-fields-and-custom-receipt-types-sample"></a>カスタム フィールドとカスタム レシート タイプのサンプル

**シナリオ:** Fabrikam は保証のついた製品が販売されるたびに特別な領収書を印刷したいと考えています。 販売レシートには、保証の有効期限日、保証 ID、およびその他の情報を含める必要があります。 業務要件を次に示します。

- 特殊な領収書を印刷します。
- 販売レシートに、その他の保証の情報を印刷します。

次の手順は、CRT コードの変更を示しています。

1. 本社 (HQ) では 2 つのカスタム レシート フィールドを作成します。保証有効期限の **EXPIRATIONDATE** と保証 ID の **WARRANTYID** です。 レシート形式レイアウトにこれらのフィールドを追加します。
2. カスタム フィールドを売上票または領収書フォーマットに追加するには、次のコードに示すように **GetSalesTransactionCustomReceiptFieldServiceRequest** を実装します。 このコードは、標準コードが受領フィールドを認識しない場合に呼び出されます。

    ```
    public IEnumerable<Type> SupportedRequestTypes
    {
        get
        {
            return new[] { typeof(GetSalesTransactionCustomReceiptFieldServiceRequest) };
        }
    }
    public Response Execute(Request request)
    {
        Type requestedType = request.GetType();
        if (requestedType == typeof(GetSalesTransactionCustomReceiptFieldServiceRequest))
        {
            return this.GetCustomReceiptFieldForSalesTransactionReceipts( (GetSalesTransactionCustomReceiptFieldServiceRequest)request);
        }
        throw new NotSupportedException(string.Format("Request '{0}' is not supported.", request.GetType()));
    }
    ```

3. サンプル フィールドのロジックを追加します。

    ```
    private GetCustomReceiptFieldServiceResponse GetCustomReceiptFieldForSalesTransactionReceipts( GetSalesTransactionCustomReceiptFieldServiceRequest request)
    {
        string receiptFieldName = request.CustomReceiptField;
        string returnValue = string.Empty;
        switch (receiptFieldName)
        {
            case "WARRANTYID":
                {
                    // Write your logic
                }
                break;
            case "EXPIRATIONDATE":
                {
                    // Write your logic
                }
                break;
        }
        return new GetCustomReceiptFieldServiceResponse(returnValue);
    }
    ```

4. 新しいレシート タイプを作成するには、**GetCustomReceiptsRequest** を実装します。

    ```
    protected override GetReceiptResponse Process(GetCustomReceiptsRequest request)
    {
        Collection<Receipt> result = new Collection<Receipt>();
            // 2. Now we can handle any additional receipt here.
        switch (request.ReceiptRetrievalCriteria.ReceiptType)
        {
            // An example of getting custom receipts.
            case ReceiptType.CustomReceipt1:
                {
                    IEnumerable<Receipt> customReceipts = this.GetCustomReceipts(salesOrder, request.ReceiptRetrievalCriteria);
                        result.AddRange(customReceipts);
                }
                break;
            default:
                // Add more logic to handle more types of custom receipt types.
                break;
        }
        return new GetReceiptResponse(new ReadOnlyCollection<Receipt>(result));
    }
    ```

完全なサンプルコードは、ソフトウェアの開発キット (SDK) の RetailSDK\\SampleExtensions\\CommerceRuntime\\Extensions.ReceiptsSamplefolder フォルダーにあります。

> [!NOTE]
> クライアントから カスタム レシート タイプの印刷を指示する必要があります。 詳細については、[POS からのカスタム レシートの印刷](https://docs.microsoft.com/dynamics365/retail/dev-itpro/pos-trigger-printing) を参照してください。

### <a name="best-practice"></a>ベスト プラクティス

各カスタム受領書フィールドに対してデータベース呼び出しを行うことは避けてください。 代わりに、エンティティに前に設定された拡張機能プロパティを使用します。 カスタムのレシート タイプは、任意のロジック (販売明細行ごと、いくつかの条件ごとに 1 回) で呼び出すことができます。 包括的なシナリオのサンプルを参照してください。
