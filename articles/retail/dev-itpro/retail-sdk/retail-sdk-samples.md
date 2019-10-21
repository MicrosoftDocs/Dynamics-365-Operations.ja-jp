---
title: Retail ソフトウェア開発キット (SDK) のサンプル
description: このトピックでは、2016 年 12 月に Retail SDK と共にリリースされた 3 つの新しいサンプルについて説明します。
author: mugunthanm
manager: AnnBe
ms.date: 09/26/2019
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
ms.openlocfilehash: 3044cfcff334294570c547396b17027ca1b3b877
ms.sourcegitcommit: 2555acfd855fc18ff3ba432ba2cf7633a8f1653c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/28/2019
ms.locfileid: "2238559"
---
# <a name="retail-software-development-kit-sdk-samples"></a><span data-ttu-id="934ba-103">Retail ソフトウェア開発キット (SDK) のサンプル</span><span class="sxs-lookup"><span data-stu-id="934ba-103">Retail software development kit (SDK) samples</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="934ba-104">このトピックでは、2016 年 12 月に Retail SDK と共にリリースされた 3 つの新しいサンプルについて説明します。</span><span class="sxs-lookup"><span data-stu-id="934ba-104">This topic describes three new samples that were released together with the Retail SDK in December 2016.</span></span>

## <a name="override-message-handler-sample"></a><span data-ttu-id="934ba-105">メッセージ ハンドラーのサンプルをオーバーライド</span><span class="sxs-lookup"><span data-stu-id="934ba-105">Override message handler sample</span></span>

<span data-ttu-id="934ba-106">**シナリオ:** Fabrikam の顧客の 1 人が顧客関係管理 (CRM) システムに参加していても、Microsoft Dynamics 365 Retail にインポートされていない場合があります。</span><span class="sxs-lookup"><span data-stu-id="934ba-106">**Scenario:** Sometimes, one of Fabrikam's customers is in the customer relationship management (CRM) system but isn't imported into Microsoft Dynamics 365 Retail.</span></span> <span data-ttu-id="934ba-107">したがって、Fabrikam は、CRM システムと POS (販売時点管理) から顧客を検索したいと考えています。</span><span class="sxs-lookup"><span data-stu-id="934ba-107">Therefore, Fabrikam wants to look up the customer from the CRM system and the point of sale (POS).</span></span> <span data-ttu-id="934ba-108">業務要件を次に示します。</span><span class="sxs-lookup"><span data-stu-id="934ba-108">Here are the business requirements:</span></span>

- <span data-ttu-id="934ba-109">CRM システムと POS から顧客を検索します。</span><span class="sxs-lookup"><span data-stu-id="934ba-109">Search for customers from the CRM system and the POS.</span></span>
- <span data-ttu-id="934ba-110">結果をマージして、Retail Modern POS (MPOS) で統合された結果セットを表示します。</span><span class="sxs-lookup"><span data-stu-id="934ba-110">Merge the results, and show a unified result set in Retail Modern POS (MPOS).</span></span>

<span data-ttu-id="934ba-111">オーバーライド メッセージ ハンドラーを使用する場合があるいくつかの状況を次に示します。</span><span class="sxs-lookup"><span data-stu-id="934ba-111">Here are some situations where you might use the override message handler:</span></span>

- <span data-ttu-id="934ba-112">在庫の更新や照会のためにサード パーティ在庫システムの使用を必要とします。</span><span class="sxs-lookup"><span data-stu-id="934ba-112">You want to use a third-party inventory system for stock updates and inquiries.</span></span>
- <span data-ttu-id="934ba-113">税金の計算のために、外部の税システムとの統合を必要としています。</span><span class="sxs-lookup"><span data-stu-id="934ba-113">You want to integrate with an external tax system for tax calculation.</span></span>
- <span data-ttu-id="934ba-114">サード パーティのロイヤルティ システムとの統合を必要としています。</span><span class="sxs-lookup"><span data-stu-id="934ba-114">You want to integrate with a third-party loyalty system.</span></span>

<span data-ttu-id="934ba-115">サンプルの基本的な作業を次に示します。</span><span class="sxs-lookup"><span data-stu-id="934ba-115">Here are the basic tasks in the sample:</span></span>

1. <span data-ttu-id="934ba-116">外部の検索が実行できるように既存の検索の動作を変更するため、既存の顧客検索要求をオーバーライドして実装します。</span><span class="sxs-lookup"><span data-stu-id="934ba-116">Override and implement the existing customer search request, because we are changing the existing search behavior so that an external search is performed.</span></span>
2. <span data-ttu-id="934ba-117">外部検索が完了した後、標準検索の要求を呼び出し、両方の結果をマージします。</span><span class="sxs-lookup"><span data-stu-id="934ba-117">After the external search is completed, call the standard search request, and merge both results.</span></span>

<span data-ttu-id="934ba-118">これらのタスクのコードを次に示します。</span><span class="sxs-lookup"><span data-stu-id="934ba-118">Here is the code for these tasks.</span></span>

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

<span data-ttu-id="934ba-119">完全なサンプルコードは、ソフトウェアの開発キット (SDK) の RetailSDK\\SampleExtensions\\CommerceRuntime\\Extensions.CustomerSearchSample フォルダーにあります。</span><span class="sxs-lookup"><span data-stu-id="934ba-119">The full sample code is in the RetailSDK\\SampleExtensions\\CommerceRuntime\\Extensions.CustomerSearchSample folder of the software development kit (SDK).</span></span>

### <a name="best-practice"></a><span data-ttu-id="934ba-120">ベスト プラクティス</span><span class="sxs-lookup"><span data-stu-id="934ba-120">Best practice</span></span>

<span data-ttu-id="934ba-121">既存の要求または応答の動作を完全に変更する場合、または標準ロジックに加えてロジックを使用する場合は、標準のメッセージ ハンドラーをオーバーライドします。</span><span class="sxs-lookup"><span data-stu-id="934ba-121">If you're planning to completely change the behavior of an existing request or response, or if you want to use your logic in addition to the standard logic, override the standard message handler.</span></span>

## <a name="request-handler-triggers-and-extension-properties-sample"></a><span data-ttu-id="934ba-122">要求ハンドラー トリガーおよび拡張プロパティのサンプル</span><span class="sxs-lookup"><span data-stu-id="934ba-122">Request handler triggers and extension properties sample</span></span>

<span data-ttu-id="934ba-123">**シナリオ:** Fabrikam が電子メール マーケティングに関する顧客電子メールの基本設定を収集します。</span><span class="sxs-lookup"><span data-stu-id="934ba-123">**Scenario:** Fabrikam wants to collect customer email preferences for email marketing.</span></span> <span data-ttu-id="934ba-124">業務要件を次に示します。</span><span class="sxs-lookup"><span data-stu-id="934ba-124">Here are the business requirements:</span></span>

- <span data-ttu-id="934ba-125">顧客の電子メールの基本設定の収集と更新をPOS から行えるようにします。</span><span class="sxs-lookup"><span data-stu-id="934ba-125">Enable a customer's email preferences to be collected and updated from the POS.</span></span>
- <span data-ttu-id="934ba-126">顧客の電子メールの基本設定はすぐに有効になります。</span><span class="sxs-lookup"><span data-stu-id="934ba-126">A customer's email preferences should become effective immediately.</span></span>

<span data-ttu-id="934ba-127">拡張機能プロパティを使用する場合があるいくつかの状況を次に示します。</span><span class="sxs-lookup"><span data-stu-id="934ba-127">Here are some situations where you might use extension properties:</span></span>

- <span data-ttu-id="934ba-128">顧客や販売注文などのエンティティの拡張を望んでいますが、新しい別のエンティティの作成を望んでいません。</span><span class="sxs-lookup"><span data-stu-id="934ba-128">You want to extend entities such as the customer and sales order, but you don't want to create a new separate entity.</span></span>
- <span data-ttu-id="934ba-129">新しいエンティティ フィールドはデータベースから読み取り、または書き込みがおこなわれますが、commerce runtime (CRT) と POS の間で送信し、クライアントで更新される必要があります。</span><span class="sxs-lookup"><span data-stu-id="934ba-129">As new entity fields are read from or written to the database, they should be sent between the commerce runtime (CRT) and the POS, and updated in the client.</span></span>
- <span data-ttu-id="934ba-130">カスタム ロジックの流れを管理するために使用できる、一時的な内部フラグが必要です。</span><span class="sxs-lookup"><span data-stu-id="934ba-130">You want temporary internal flags that can be used to control the flow of custom logic.</span></span>
- <span data-ttu-id="934ba-131">レシートを生成するときにレシート カスタマイズがアクセスする、カスタム レシート フィールドを設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="934ba-131">You want to set custom receipt fields that the receipt customization will access when receipts are generated.</span></span>

<span data-ttu-id="934ba-132">次の手順は、CRT コードの変更を示しています。</span><span class="sxs-lookup"><span data-stu-id="934ba-132">The following steps show the CRT code changes.</span></span> <span data-ttu-id="934ba-133">MPOS およびチャンネル データベースで、サンプル全体を参照してください。</span><span class="sxs-lookup"><span data-stu-id="934ba-133">For MPOS and the channel database, see the full sample.</span></span> <span data-ttu-id="934ba-134">次のサンプルは、標準的なデータベース コンポーネントへの変更が必要となった場合に前のコードとは異なることに注意してください。</span><span class="sxs-lookup"><span data-stu-id="934ba-134">Notice that the following samples differ from previous code, where changes to the standard database artifacts were required.</span></span> <span data-ttu-id="934ba-135">(たとえば、新しい列を拡張プロパティとして公開するには、ビューへの変更が必要になります。</span><span class="sxs-lookup"><span data-stu-id="934ba-135">(For example, to expose new columns as extension properties, changes to the view were required.</span></span> <span data-ttu-id="934ba-136">拡張機能のプロパティの一覧を受信し、これらのプロパティを標準フィールドと共に更新するには、ストアド プロシージャの変更が必要でした。最終的にインラインで変更されていないモデルに移行すると、データベースが更新されてもマージ競合は発生しません。</span><span class="sxs-lookup"><span data-stu-id="934ba-136">To receive a list of extension properties and update these properties together with standard fields, changes to the stored procedure were required.) Eventually, as we move to a model that doesn't have inline changes, merge conflicts should not occur even when the database is updated.</span></span> <span data-ttu-id="934ba-137">したがって、エンティティの読み込み、書き込み、更新のために個別のデータベース呼び出しを行うことをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="934ba-137">Therefore, our new recommendation is that you make separate database calls to read, write, and update entities.</span></span>

1. <span data-ttu-id="934ba-138">**エンティティの読み取り**</span><span class="sxs-lookup"><span data-stu-id="934ba-138">**Read the entity.**</span></span> <span data-ttu-id="934ba-139">**GetCustomerDataRequest** の転記トリガーを実装し、チャネル データベースから値を読み取って拡張プロパティに値を追加します。</span><span class="sxs-lookup"><span data-stu-id="934ba-139">Implement the post-trigger for **GetCustomerDataRequest**, read the value from channel database, and add the value to the extension property.</span></span>

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

2. <span data-ttu-id="934ba-140">**エンティティの書き込み。**</span><span class="sxs-lookup"><span data-stu-id="934ba-140">**Write the entity.**</span></span> <span data-ttu-id="934ba-141">**CreateOrUpdateCustomerDataRequest** のハンドラーをオーバーライドし、トランザクション スコープ内で元のリクエスト ハンドラーとカスタム ストアド プロシージャを実行します。</span><span class="sxs-lookup"><span data-stu-id="934ba-141">Override the handler for **CreateOrUpdateCustomerDataRequest** to run the original request handler and the custom stored procedure inside a transaction scope.</span></span> <span data-ttu-id="934ba-142">データベース トランザクションが必要ではない場合は、ポスト トリガーで十分です。</span><span class="sxs-lookup"><span data-stu-id="934ba-142">If the database transaction isn't required, a post-trigger suffices here.</span></span>

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

<span data-ttu-id="934ba-143">このサンプルを実行する前に、チャネル データベースでカスタム テーブル、ビュー、およびストアド プロシージャを作成することを確認します。</span><span class="sxs-lookup"><span data-stu-id="934ba-143">Before you try this sample, be sure to create the custom tables, views, and stored procedures in the channel database.</span></span> <span data-ttu-id="934ba-144">また、MPOS に関連する変更を行います。</span><span class="sxs-lookup"><span data-stu-id="934ba-144">Additionally, make the relevant changes to MPOS.</span></span> <span data-ttu-id="934ba-145">追加のコメントと共に、完全なサンプル コードが、RetailSDK\\SampleExtensions\\CommerceRuntime\\Extensions.EmailPreferenceSample フォルダーにあります。</span><span class="sxs-lookup"><span data-stu-id="934ba-145">The full sample code, together with additional comments, is in the RetailSDK\\SampleExtensions\\CommerceRuntime\\Extensions.EmailPreferenceSample folder of the SDK.</span></span> <span data-ttu-id="934ba-146">カスタム データベース アーティファクトを作成する方法の詳細については、SDK の RetailSDK\\Documents\\SampleExtensionsInstructions\\EmailPreference フォルダを参照してください。</span><span class="sxs-lookup"><span data-stu-id="934ba-146">For information about how to create custom database artifacts, see the RetailSDK\\Documents\\SampleExtensionsInstructions\\EmailPreference folder of the SDK.</span></span>

> [!NOTE]
> <span data-ttu-id="934ba-147">上記のコード サンプルと RetailSDK\\Documents\\SampleExtensionsInstructions\\emailpreference フォルダー内のサンプル スクリプトでは、[crt].EXTENSIONPROPERTIESTABLETYPE が使用されます。</span><span class="sxs-lookup"><span data-stu-id="934ba-147">The above code sample and the sample script in the RetailSDK\\Documents\\SampleExtensionsInstructions\\EmailPreference folder use [crt].EXTENSIONPROPERTIESTABLETYPE.</span></span> <span data-ttu-id="934ba-148">バージョン 7.3 以降では、ext スキーマで crt または ax スキーマのオブジェクト/データ型の使用がサポートされなくなりました。</span><span class="sxs-lookup"><span data-stu-id="934ba-148">Starting in version 7.3 we no longer support using crt or ax schema objects/data types in ext schema.</span></span> <span data-ttu-id="934ba-149">ext スキーマで、カスタム拡張テーブル プロパティ型を作成して使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="934ba-149">You must create your custom extension table property type in ext schema and use it.</span></span>

### <a name="best-practice"></a><span data-ttu-id="934ba-150">ベスト プラクティス</span><span class="sxs-lookup"><span data-stu-id="934ba-150">Best practice</span></span>

<span data-ttu-id="934ba-151">トリガーが連鎖されている場合トリガーの順序は保証されていないため、また内部キャッシュ メカニズムのために、プレトリガーは*要求*メッセージを変更してはならず、ポストトリガーは*応答*メッセージを変更できません。</span><span class="sxs-lookup"><span data-stu-id="934ba-151">Because the order of triggers isn't guaranteed when the triggers are chained, and because of the internal cache mechanism, the pre-triggers should not change the *request* message, and the post-triggers should not change the *response* message.</span></span> <span data-ttu-id="934ba-152">拡張プロパティは、コア プロパティが変更されていないため、許可されます。</span><span class="sxs-lookup"><span data-stu-id="934ba-152">Extension properties are allowed, because no core properties are being changed.</span></span> <span data-ttu-id="934ba-153">機能拡張プロパティを処理するには、プリトリガーとポストトリガーを使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="934ba-153">You should use pre-triggers and post-triggers to handle extension properties.</span></span> <span data-ttu-id="934ba-154">また、検証を行うためにプレトリガーを使用し、追加のアクションを行うためにポストトリガーを使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="934ba-154">You should also use pre-triggers to do validation and post-triggers to do additional actions.</span></span>

## <a name="custom-fields-and-custom-receipt-types-sample"></a><span data-ttu-id="934ba-155">カスタム フィールドとカスタム レシート タイプのサンプル</span><span class="sxs-lookup"><span data-stu-id="934ba-155">Custom fields and custom receipt types sample</span></span>

<span data-ttu-id="934ba-156">**シナリオ:** Fabrikam は保証のついた製品が販売されるたびに特別な領収書を印刷したいと考えています。</span><span class="sxs-lookup"><span data-stu-id="934ba-156">**Scenario:** Fabrikam wants to print a special receipt whenever products that have a warranty are sold.</span></span> <span data-ttu-id="934ba-157">販売レシートには、保証の有効期限日、保証 ID、およびその他の情報を含める必要があります。</span><span class="sxs-lookup"><span data-stu-id="934ba-157">Sales receipts should include the warranty expiration date, the warranty ID, and other information.</span></span> <span data-ttu-id="934ba-158">業務要件を次に示します。</span><span class="sxs-lookup"><span data-stu-id="934ba-158">Here are the business requirements:</span></span>

- <span data-ttu-id="934ba-159">特殊な領収書を印刷します。</span><span class="sxs-lookup"><span data-stu-id="934ba-159">Print special receipts.</span></span>
- <span data-ttu-id="934ba-160">販売レシートに、その他の保証の情報を印刷します。</span><span class="sxs-lookup"><span data-stu-id="934ba-160">Print additional warranty information on sale receipts.</span></span>

<span data-ttu-id="934ba-161">次の手順は、CRT コードの変更を示しています。</span><span class="sxs-lookup"><span data-stu-id="934ba-161">The following steps show the CRT code changes:</span></span>

1. <span data-ttu-id="934ba-162">本社 (HQ) では 2 つのカスタム レシート フィールドを作成します。保証有効期限の **EXPIRATIONDATE** と保証 ID の **WARRANTYID** です。</span><span class="sxs-lookup"><span data-stu-id="934ba-162">At the headquarters (HQ), create two custom receipt fields: **EXPIRATIONDATE** for the warranty expiration date and **WARRANTYID** for the warranty ID.</span></span> <span data-ttu-id="934ba-163">レシート形式レイアウトにこれらのフィールドを追加します。</span><span class="sxs-lookup"><span data-stu-id="934ba-163">Add these fields to the receipt format layout.</span></span>
2. <span data-ttu-id="934ba-164">カスタム フィールドを売上票または領収書フォーマットに追加するには、次のコードに示すように **GetSalesTransactionCustomReceiptFieldServiceRequest** を実装します。</span><span class="sxs-lookup"><span data-stu-id="934ba-164">To add the custom fields to the sales receipts or any receipt format, implement **GetSalesTransactionCustomReceiptFieldServiceRequest**, as shown in the following code.</span></span> <span data-ttu-id="934ba-165">このコードは、標準コードが受領フィールドを認識しない場合に呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="934ba-165">This code is called every time that the standard code doesn't recognize the receipt field.</span></span>

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

3. <span data-ttu-id="934ba-166">サンプル フィールドのロジックを追加します。</span><span class="sxs-lookup"><span data-stu-id="934ba-166">Add the logic for your sample fields.</span></span>

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

4. <span data-ttu-id="934ba-167">新しいレシート タイプを作成するには、**GetCustomReceiptsRequest** を実装します。</span><span class="sxs-lookup"><span data-stu-id="934ba-167">To create new receipt type, implement **GetCustomReceiptsRequest**.</span></span>

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

<span data-ttu-id="934ba-168">完全なサンプルコードは、ソフトウェアの開発キット (SDK) の RetailSDK\\SampleExtensions\\CommerceRuntime\\Extensions.ReceiptsSamplefolder フォルダーにあります。</span><span class="sxs-lookup"><span data-stu-id="934ba-168">The full sample code is in the RetailSDK\\SampleExtensions\\CommerceRuntime\\Extensions.ReceiptsSamplefolder folder of the SDK.</span></span>

> [!NOTE]
> <span data-ttu-id="934ba-169">クライアントから カスタム レシート タイプの印刷を指示する必要があります。</span><span class="sxs-lookup"><span data-stu-id="934ba-169">You should call the printing of the custom receipt type from the client.</span></span> <span data-ttu-id="934ba-170">詳細については、[拡張性のパターンおよびベスト プラクティス](https://youtu.be/qQkHFubENIY) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="934ba-170">For more information, see [Extensibility patterns and best practices](https://youtu.be/qQkHFubENIY).</span></span>

### <a name="best-practice"></a><span data-ttu-id="934ba-171">ベスト プラクティス</span><span class="sxs-lookup"><span data-stu-id="934ba-171">Best practice</span></span>

<span data-ttu-id="934ba-172">各カスタム受領書フィールドに対してデータベース呼び出しを行うことは避けてください。</span><span class="sxs-lookup"><span data-stu-id="934ba-172">Avoid making database calls for each custom receipt field.</span></span> <span data-ttu-id="934ba-173">代わりに、エンティティに前に設定された拡張機能プロパティを使用します。</span><span class="sxs-lookup"><span data-stu-id="934ba-173">Instead, use extension properties that were previously set on entities.</span></span> <span data-ttu-id="934ba-174">カスタムのレシート タイプは、任意のロジック (販売明細行ごと、いくつかの条件ごとに 1 回) で呼び出すことができます。</span><span class="sxs-lookup"><span data-stu-id="934ba-174">Custom receipt types can be called by any logic (per sales line, one time per some condition).</span></span> <span data-ttu-id="934ba-175">包括的なシナリオのサンプルを参照してください。</span><span class="sxs-lookup"><span data-stu-id="934ba-175">See the sample for a more complete scenario.</span></span>
