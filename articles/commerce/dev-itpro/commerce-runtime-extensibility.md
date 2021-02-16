---
title: Commerce runtime (CRT) の拡張機能
description: このトピックでは、Commerce Runtime (CRT) と Retail サーバーを拡張するさまざまな方法について説明します。
author: mugunthanm
manager: AnnBe
ms.date: 11/13/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Developer
ms.reviewer: rhaertle
ms.custom: 104593
ms.assetid: 1397e679-8cd5-49f3-859a-83d342fdd275
ms.search.region: Global
ms.author: mumani
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: afd8f3e47820fbb7f1f3e621e64390e4f012f316
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 12/05/2020
ms.locfileid: "4683364"
---
# <a name="commerce-runtime-crt-extensibility"></a>Commerce runtime (CRT) の拡張機能

[!include [banner](../includes/banner.md)]

このトピックでは、Commerce Runtime (CRT) を拡張するさまざまな方法について説明します。 拡張機能プロパティのコンセプトを説明し、保持有無にかかわらず CRT エンティティに追加する方法について説明します。

CRT にはコア ビジネス ロジックが含まれています。 ビジネス ロジックを追加または変更するには、CRT をカスタマイズする必要があります。 C# を使用して、すべての CRT コードが開発され、コンパイルされてクラス ライブラリとしてリリースされます (.NET アセンブリ)。 販売時点管理 (POS) はシン クライアントです。 すべてのビジネス ロジックは、CRT で行われます。 POS は、任意のビジネス ロジックを実行する CRT を呼び出し、CRT は情報を処理して POS に送り返されます。

すべての CRT サービスは、1 つ以上の要求と応答のグループで構成されます。 POS が、Retail Server に要求を送信し、Retail Server は CRT を呼び出します。 続いて CRT は要求を処理し、応答を送り返します。

たとえば、CRT の顧客サービスには、顧客関連のすべての要求と応答が含まれており、それぞれは異なるフローで実行されています。 同様に、CRT の製品サービスには製品に関連するすべての要求と応答が含まれます。 次の表に、顧客サービスの要求を示します。

| 要求                                      | 目的                                                                          |
|----------------------------------------------|----------------------------------------------------------------------------------|
| SaveCustomerServiceRequest                   | この要求は、POS から顧客を保存する場合に呼び出されます。                        |
| GetCustomersServiceRequest                   | この要求は、選択した顧客の詳細を取得するために使用されます。                |
| CustomersSearchServiceRequest                | この要求は、POS から顧客検索を行う場合に実行されます。                      |
| GetCustomerGroupsServiceRequest              | この要求は、顧客グループの詳細を取得するために使用されます。                   |
| InitiateLinkToExistingCustomerServiceRequest | この内部要求は、下位互換性のためのものです。                             |
| FinalizeLinkToExistingCustomerServiceRequest | この内部要求は、下位互換性のためのものです。                             |
| UnlinkFromExistingCustomerServiceRequest     | この内部要求は、下位互換性のためのものです。                             |
| GetCustomerBalanceServiceRequest             | この要求は、顧客勘定の残高を取得します。                          |
| GetOrderHistoryServiceRequest                | この要求は、顧客の注文履歴を取得します。                                  |
| GetPurchaseHistoryServiceRequest             | この要求は、顧客の最近の購入履歴を取得します。                |
| CustomerSearchByFieldsServiceRequest         | フィールド (ヒント検索) を使用して顧客を検索する際に、この要求が実行されます。 |
| GetCustomerSearchFieldsServiceRequest        | この要求は、顧客検索フィールド (ヒント フィールド) の一覧を取得します。              |

## <a name="crt-extension-patterns"></a>CRT 拡張パターン

CRT 拡張パターンについて学習する前に、CRT 拡張の作成方法を理解する必要があります。 CRT は単に、C# クラス ライブラリ (.NETアセンブリ) のコレクションです。 C# でクラス ライブラリ プロジェクトを作成し、次の表に示すパターンを使用してすべての CRT 拡張を実行できます。 これらのサンプルには、適切なアセンブリ参照、Microsoft .NET Framework バージョン、アウトプット タイプ、およびビルド パラメーターが含まれているので、Microsoft が拡張のためのテンプレートとして提供するサンプルを常に使用します。 また、他のすべての必須パラメーターがコンフィギュレーション済みです。 同様のサンプルコードは、R\\RetailSDK\\SampleExtensions\\CommerceRuntime の Retail ソフトウェア開発キット (CRT) で見つけることができます。

### <a name="create-a-new-crt-service"></a>新しい CRT サービスの作成

新機能を作成します。

### <a name="override-existing-service"></a>既存のサービスを上書きする

完全に既存の機能をオーバーライドしたり、ビジネス フローに従ってカスタマイズできます。 次にいくつか例を挙げます。

+ POS 検索機能を上書きして、ローカル データベースまたは本社で検索するのではなく、外部システムから検索する必要があります。 または、上書き、標準機能の呼び出しおよびいくつか追加カスタム ロジックの実行が可能です。
+ ローカル データベースまたは HQ、および外部システムを検索した後、最後に結果をマージまたは変更します。
+ ハンドラーの上書きは避けてください。 プレトリガーまたはポストトリガーを使用すると、CRT の拡張機能のシナリオのほとんどを実装できます。 上書きが必要なのは、既存の機能を完全に置換する場合だけです。</li>

### <a name="triggers"></a>トリガー

任意の要求の前後に追加ロジックを実行できます。

前のトリガーで、カスタム ロジックなどのいくつかの検証を実行できます。

ポスト トリガーで、要求にいくらかのカスタム情報を追加し POS に送信できます。 または、標準機能から戻される結果の変更または追加ビジネス ロジックの実行が可能です。

### <a name="extension-properties"></a>拡張プロパティ

任意の CRT エンティティにカスタム プロパティーを追加し、それを POS に送信することができます。 拡張プロパティはキーと値のペアです。 POS で拡張プロパティを設定すると、CRT で使用できるようになります。 同様に、CRT で拡張機能プロパティを設定する場合、POS で使用できます。 また、要求、応答、または要求コンテキストのレベルで拡張プロパティを設定することもできます。 既定では、拡張機能のプロパティはデータベースに保存されず、読み取られません。 拡張プロパティを読み取り、設定するには、カスタム コードを記述する必要があります。 ただし、そのカスタム コードは、POS と CRT 間で自動的に送信されます。

たとえば、POS の顧客エンティティーにいくつかの追加情報をキャプチャして表示したいとします。 この場合、顧客に対するすべてのカスタム プロパティをフェッチするポスト トリガーを追加し、拡張子プロパティとして顧客エンティティに追加し、それらの拡張機能プロパティを POS に送信できます。

POS から CRT に拡張機能のプロパティを送信して、カスタム テーブルに保存できます。 または、これらのプロパティに基づくいくつかのカスタム ロジックの実行または本社への送信が可能です。

製品、顧客、トランザクション、およびパラメーターなどのすべての CRT エンティティは、拡張機能プロパティをサポートします。

> [!NOTE]
> 属性もまたサポートされます (コンフィギュレーション駆動型の開発)。 拡張プロパティの場合は、カスタム テーブルを作成し、データを格納する必要があります。 ただし、属性はコンフィギュレーション駆動型であり、テーブル フィールドを作成するために必須ではありません。 したがって、読み取りおよび更新操作にコードは必要ありません。

属性についての詳細は、次のトピックを参照してください。

+ [注文属性](order-attributes.md)
+ [顧客属性](customer-attributes.md)

### <a name="real-time-transaction-service-calls"></a>リアルタイム トランザクション サービスの呼び出し

CRT から HQ の同期呼び出しを行うことができます。

### <a name="crt-data-service-and-data-service-with-entity"></a>CRT データ サービス、およびエンティティ付きデータ サービス

チャンネル データベースからデータ/エンティティを読み取るためのデータ サービス。

> [!NOTE]
> CRT 拡張コードでは、CRT ビジネス ロジック クラス、メソッド、またはハンドラー (Runtime.Workflow、Runtime.Services、Runtime.DataServices のクラスなど) を参照したり使用したりすることはできません。 これらのクラスには、下位互換性がありません。アップグレード中に拡張機能が無効になる可能性があります。 拡張では、Runtime.*.Messages、Runtime.Framework、Runtime.Data、Runtime.Entities の要求クラス、応答クラス、エンティティ クラスのみ使用する必要があります。

## <a name="register-the-crt-extension"></a>CRT 拡張機能の登録

### <a name="online"></a>オンライン

オンラインの場合 (POS が Retail Server に接続された場合)、CRT を拡張した後、拡張ライブラリを **\\RetailServer\\webroot\\bin\\Ext** フォルダーに配置します。 **CommerceRuntime.Ext.config** ファイルの **構成** セクションを、以下の例のようにカスタム ライブラリ情報で更新します。

```xml
<add source="assembly" value="your custom library name" />
```

たとえば、カスタム ライブラリの名前が **Contoso.Commerce.Runtime.CustomerSearchSample** の場合、**構成** セクションに次の行を追加します。

```xml
<add source="assembly" value="Contoso.Commerce.Runtime.CustomerSearchSample" />
```

### <a name="offline"></a>オフライン

オフラインの場合は、CRT を拡張した後、カスタム ライブラリを **\\Program Files (x86)\\Microsoft Dynamics 365\\70\\Retail Modern POS\\ClientBroker\\ext** フォルダーに配置します。 **CommerceRuntime.MPOSOffline.ext.config** ファイルの **構成** セクションを、以下の例のようにカスタム ライブラリ情報で更新します。

```xml
<add source="assembly" value="your custom library name" />.
```

## <a name="register-the-extension-configuration-in-the-commerceruntimeextconfig-file"></a>CommerceRuntime.Ext.config ファイルに拡張コンフィギュレーションを登録する

拡張機能では、**\<settings\>** ノードの **CommerceRuntime.Ext.config** ファイルに任意のキー値のコンフィギュレーションを登録できます。

この **\<settings\>** ノードは、CommerceRuntime コンポーネントを設定するために使用されるキーと値のペアのコレクションです。 この規則では、接頭語を設定キーの前に付けて、区切り記号としてピリオド (.) を使用して、コンフィギュレーションしている機能領域を表します。 Commerce Runtime の初期化では、この規則が適用され、それ以外の場合は読み込まれないので、拡張コンフィギュレーション値の前には必ず **ext** を付ける必要があります。 追加の接頭語を追加して、制御するサブ領域を表すことができます。 次の例では、キーと値のペアを設定しています。

```xml
      <add name="ext.SalesTransaction.Storage.CartSerializationFormat" value="XML" />
```

リアルタイム サービス呼び出しでの HTTP バインドのタイムアウトについては、メソッドごとにタイムアウトを秒単位でを設定します。 このタイムアウト値は、**CommerceRuntime.config** で設定された **maxExtensionTimeoutInSeconds** によって制限されます。

```xml
<add name="ext.RealTimeServiceClient.TimeoutInSeconds.InvokeExtensionMethod.ContosoRetailStoreHours_UpdateStoreHours" value="300" />
```

CRT 拡張コンフィグからキー値を読み取るために、拡張コードは、**RequestContext.Runtime.Configuration** を使用できます。 次の例では、値を取得する方法を示します。

```csharp
 string key = context.Runtime.Configuration.GetSettingValue("ext.SalesTransaction.Storage.CartSerializationFormat") ?? string.Empty;
```

上記の手順は、手動による展開および開発ボックスでのテストのために使用されます。 拡張機能をパッケージ化し、生産またはユーザー受け入れテスト (UAT) に配置するには、パッケージ ドキュメントの情報を使用します。

## <a name="debugging-crt"></a>CRT のデバッグ

### <a name="attach-online"></a>オンラインで関連付け

POS から CRT をデバッグするには、POS が Retail Server に接続されているときに、CRT 拡張プロジェクトを、**w3wp.exe** (Retail Server の IIS プロセス) に関連付ける必要があります。

### <a name="attach-offline"></a>オフラインで関連付け

オフラインの場合は、**dllhost.exe** プロセスに CRT 拡張プロジェクトを関連付けます。

## <a name="using-extension-properties-on-crt-entities-requests-and-responses"></a>CRT エンティティ、依頼および応答での拡張プロパティの使用

既存の CRT エンティティに新しいデータを追加する 1 つの方法は、拡張プロパティを使用することです。 拡張プロパティは、エンティティのキーと値のペアです。 既定では、これらのキーと値のペアはデータベースで保持されません。 拡張プロパティを保持するためには、カスタム コードを記述する必要があります。

## <a name="using-extension-properties-on-crt-entities-with-persistence"></a>CRT エンティティでの拡張プロパティの永続的な使用

エンティティに追加する任意の拡張プロパティは、シナリオしだいでオブジェクトまたはトランザクションのいずれかの有効期間の POS および CRT メモリに保持されます。 拡張プロパティは、アプリケーションの境界にもまたがって移動します。 たとえば、Retail Modern POS に拡張プロパティを追加し、Retail Server または CRT を呼び出すと、キーと値のペアがそのフロー全体で使用できます。 また、そのエンティティが Commerce Data Exchange: Real-time Service を呼び出し中に送信されると、キーと値のペアは処理中に使用できます。

> [!NOTE]
> HQ では、拡張プロパティは顧客と注文に対してのみ送信されます。

ただし、既述のように、拡張プロパティは既定では保持されません。 拡張プロパティを保持する場合は、データ モデリングを実行して、データの格納場所を適切に設計することを保証する必要があります。 新しいテーブルと結合を使用することをお勧めします。 この方法は、ほとんどの要件に適合します。 Retail SDK の **EmailPreference** サンプルは、代表的なエンド ツー エンドの例を提供します。

**Retail SDK のサンプル コードの場所**

…\\RetailSDK\\SampleExtensions\\CommerceRuntime\\Extensions.EmailPreferenceSample

**スクリプトの場所**

…\\RetailSDK\\ドキュメント\\SampleExtensionsInstructions\\EmailPreference

**エンティティに拡張子プロパティを設定する構文**

```csharp
public virtual void SetProperty(string key, object value);
entity.SetProperty("key", value);
```

**例**

**シナリオ**

顧客エンティティおよび拡張用に作成された新しい拡張テーブルとフィールドは、拡張テーブルからそれらのフィールドを読み取り、POS に送信する必要があります。

チャネル データベースを拡張する場合は、拡張テーブルにメイン テーブルの主キーを含めることをお勧めします。 つまり、直接の関係を持たずに、主キーを使用して拡張テーブルからデータを読み取ります。

**ステップ**

1. メイン テーブルの主キーを持つチャネル データベース拡張スキーマで **顧客** エンティティの拡張テーブルを作成します。
2. **顧客** エンティティを読み取る CRT データ要求を識別します。
3. データ要求の転記トリガーを追加します。 **顧客** テーブルの主キーを使用して、拡張テーブルを照会し、カスタム フィールドを読み取ることができます。

    > [!NOTE]
    > ポスト トリガー要求でエンティティの主キーを取得できます。 エンティティ オブジェクトを持つその要求、およびすべての必須フィールドを持つそのエンティティ オブジェクト。

4. カスタム フィールドを拡張プロパティとして、CRT 転記トリガーの共有パラメーター エンティティへ追加し、POS へ送信します。

## <a name="reading-extension-properties-in-triggers"></a>トリガーの拡張機能プロパティの読み取り

顧客テーブルからデータを読み込む要求は、GetCustomerDataRequest です。 次の例では、この要求のポスト トリガーを追加する方法を示します。

```csharp
namespace Contoso
{
    namespace Commerce.Runtime.EmailPreferenceSample
    {
        using System;
        using System.Collections.Generic;
        using System.Threading.Tasks;
        using Microsoft.Dynamics.Commerce.Runtime;
        using Microsoft.Dynamics.Commerce.Runtime.Data;
        using Microsoft.Dynamics.Commerce.Runtime.DataModel;
        using Microsoft.Dynamics.Commerce.Runtime.DataServices.Messages;
        using Microsoft.Dynamics.Commerce.Runtime.Messages;

        /// <summary>
        /// Class that implements a post trigger for the GetCustomerDataRequest request type.
        /// </summary>
        public class GetCustomerTriggers : IRequestTriggerAsync
        {
            /// <summary>
            /// Gets the supported requests for this trigger.
            /// </summary>
            public IEnumerable<Type> SupportedRequestTypes
            {
                get
                {
                    return new[] { typeof(GetCustomerDataRequest) };
                }
            }

            /// <summary>
            /// Post trigger code to retrieve extension properties.
            /// </summary>
            /// <param name="request">The request.</param>
            /// <param name="response">The response.</param>
            public async Task OnExecuted(Request request, Response response)
            {
                ThrowIf.Null(request, "request");
                ThrowIf.Null(response, "response");

                var customer = ((SingleEntityDataServiceResponse<Customer>)response).Entity;

                if (customer == null)
                {
                    return;
                }

                var query = new SqlPagedQuery(QueryResultSettings.SingleRecord)
                {
                    DatabaseSchema = "ext",
                    Select = new ColumnSet(new string[] { "EMAILOPTIN" }),
                    From = "CUSTOMEREXTENSIONVIEW",
                    Where = "ACCOUNTNUM = @accountNum AND DATAAREAID = @dataAreaId"
                };

                query.Parameters["@accountNum"] = customer.AccountNumber;
                query.Parameters["@dataAreaId"] = request.RequestContext.GetChannelConfiguration().InventLocationDataAreaId;
                using (var databaseContext = new DatabaseContext(request.RequestContext))
                {
                    var extensionsResponse = await databaseContext.ReadEntityAsync<ExtensionsEntity>(query).ConfigureAwait(false);
                    ExtensionsEntity extensions = extensionsResponse.FirstOrDefault();

                    var emailOptIn = extensions != null ? extensions.GetProperty("EMAILOPTIN") : null;
                    if (emailOptIn != null)
                    {
                        customer.SetProperty("EMAILOPTIN", emailOptIn);
                    }
                }
            }

            /// <summary>
            /// Pre trigger code.
            /// </summary>
            /// <param name="request">The request.</param>
            public async Task OnExecuting(Request request)
            {
                // It's only stub to handle async signature.
                await Task.CompletedTask;
            }
        }
    }
}
```

> [!NOTE]
> 新しいフィールドとテーブル、または使用している条件に基づいて、このクエリを変更する必要があります。 テーブルをデザインするときは、CRT エンティティを使用してクエリできるように、親テーブルの主キー フィールドがあることを確認します。 ほとんどの CRT エンティティには、**RecId** フィールドまたはレコードを選択するために使用される関連する別の固有フィールドなどの主キー フィールドがある必要があります。

## <a name="saving-extension-properties-by-overriding-the-handler"></a>ハンドラーを上書きすることによる拡張プロパティの保存

**シナリオ**

顧客用に新しい拡張テーブルを作成しました。 顧客の拡張フィールドの値が POS または CRT から来た場合は、その値をカスタム テーブルに格納します。

> [!NOTE]
> 拡張のプロパティはトリガーで、またはハンドラーを上書きすることによって設定することができます。 拡張テーブルから読み込んで拡張プロパティを設定しただけの場合、トリガーを使用することができます。

**ステップ**

1. メイン テーブルに主キーの関係があるチャネル テーブル内の、顧客の拡張テーブルを作成します。 (この場合、メイン テーブルは **CustTable** です。)
2. **CustTable** にデータを設定する CRT データ要求を識別します。
3. ハンドラを上書きし、基本要求を呼び出して、メイン テーブル (**CustTable**) に値を設定してから、拡張テーブルに値を設定します。

> [!NOTE]
> 拡張コードでは、拡張手順またはビューに必要な追加のプロパティを渡すことができます。 拡張プロパティは CRT のプレトリガーまたはポストトリガーに保存できますが、CRT ハンドラーをオーバーライドする必要はありません。 ハンドラーのオーバーライドは避け、ほとんどの CRT 拡張機能のシナリオはプレトリガーまたはポストトリガーで達成できます。

次の例では、使用される SQL スクリプトがありません。 完全なサンプル コードとスクリプトは、Retail SDK の次の場所にあります。

**Retail SDK のサンプル コードの場所**

…\\RetailSDK\\SampleExtensions\\CommerceRuntime\\Extensions.EmailPreferenceSample

**スクリプトの場所**

…\\RetailSDK\\ドキュメント\\SampleExtensionsInstructions\\EmailPreference

**例**

```csharp
namespace Contoso
{
    namespace Commerce.Runtime.EmailPreferenceSample
    {
        using System.Threading.Tasks;
        using System.Transactions;
        using Microsoft.Dynamics.Commerce.Runtime;
        using Microsoft.Dynamics.Commerce.Runtime.Data;
        using Microsoft.Dynamics.Commerce.Runtime.DataModel;
        using Microsoft.Dynamics.Commerce.Runtime.DataServices.Messages;
        using Microsoft.Dynamics.Commerce.Runtime.Messages;

        /// <summary>
        /// Create or update customer data request handler.
        /// </summary>
        public sealed class CreateOrUpdateCustomerDataRequestHandler : SingleAsyncRequestHandler<CreateOrUpdateCustomerDataRequest>
        {
            /// <summary>
            /// Executes the workflow to create or update a customer.
            /// </summary>
            /// <param name="request">The request.</param>
            /// <returns>The response.</returns>
            protected override async Task<Response> Process(CreateOrUpdateCustomerDataRequest request)
            {
                ThrowIf.Null(request, "request");

                using (var databaseContext = new DatabaseContext(request.RequestContext))
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
                        parameters["@TVP_EXTENSIONPROPERTIESTABLETYPE"] = new ExtensionPropertiesExtTableType(request.Customer.RecordId, request.Customer.ExtensionProperties).DataTable;
                        await databaseContext.ExecuteStoredProcedureNonQueryAsync("[ext].UPDATECUSTOMEREXTENSIONPROPERTIES", parameters, resultSettings: null).ConfigureAwait(false);
                    }

                    transactionScope.Complete();

                    return response;
                }
            }
        }
    }
}
```

**後で読み込むプロパティを有効にする構文**

```C#
var property = entity.GetProperty("EXTENSION_PROPERTY_ADDED");
```

## <a name="using-extension-properties-on-crt-request-and-response-types"></a>CRT 要求タイプおよび応答タイプでの拡張機能プロパティの使用

エンティティと同様、拡張機能プロパティを設定および取得するために要求および応答タイプを拡張できます。 ただし、要求のライフサイクルでのみ存続し、POS では使用できなくなります。 それらをデータベースに保存する場合は、カスタム コードを記述する必要があります。

```C#
request.SetProperty("PropertyName", true);
response.SetProperty("PropertyName2", true);
var PropertyName = request.GetProperty("PropertyName");
var BoolPropertyName2 = response.GetProperty("PropertyName2");
```

**設定または POS の拡張子プロパティの読み取り**

POS で拡張プロパティーを設定して、POS アプリケーション プログラミング インターフェース (API) を使用してそれらを CRT に送信することができます。 または、エンティティ レベルで拡張機能プロパティの送信が可能です。

カート行に拡張プロパティを設定するには、SaveExtensionPropertiesOnCartLinesClientRequest を使用します。 同様に、買い物カゴ ヘッダーに対して、SaveExtensionPropertiesOnCartClientRequest を使用します。

次に例を示します。

```C#
let sampleExtensionProperty = <ProxyEntities.CommerceProperty>{
    Key: "sampleExtensionProperty",
    Value: <ProxyEntities.CommercePropertyValue>{
        BooleanValue: false
    }
};
this.context.runtime.executeAsync(new SaveExtensionPropertiesOnCartClientRequest([sampleExtensionProperty]));
```

## <a name="reading-the-extension-property-from-the-cart-in-pos"></a>POS のカートから拡張プロパティの読み取り

```typescript
let getCartRequest: GetCurrentCartClientRequest<GetCurrentCartClientResponse> = new GetCurrentCartClientRequest<GetCurrentCartClientResponse>();
return this.context.runtime.executeAsync(getCartRequest).then((value: ICancelableDataResult<GetCurrentCartClientResponse>) => {
    let cart: Commerce.Proxy.Entities.Cart = (<GetCurrentCartClientResponse>value.data).result;

    // Gets the extension property from the cart.

    let sampleExtensionPropertyValue: boolean;
    if (!ObjectExtensions.isNullOrUndefined(cart) && !ObjectExtensions.isNullOrUndefined(cart.ExtensionProperties)) {
        let SampleCommerceProperties: ProxyEntities.CommerceProperty[] = cart.ExtensionProperties.filter((extensionProperty: ProxyEntities.CommerceProperty) => {
            return extensionProperty.Key === "sampleExtensionProperty";
        });
        sampleExtensionPropertyValue = SampleCommerceProperties.length > 0 ? SampleCommerceProperties[0].Value.BooleanValue : false;
    } else {
        sampleExtensionPropertyValue = false;
    }

    //Resolve the promise according to your scenario and method.

    return Promise.resolve({ canceled: false });
});
```

同様に、製品、顧客、および住所など他のすべてのエンティティから拡張機能プロパティを読み取ることができます。

## <a name="implementing-a-new-crt-service-that-handles-multiple-new-requests"></a>複数の新しい要求を処理する新しい CRT サービスの実装

新しい CRT サービスを実装することが一般的です。 最初に、新しい要求および応答クラスを作成する必要があります。

## <a name="creating-the-request-and-response-classes"></a>要求および応答クラスを作成しています

作業のシリアル化については、新しい要求タイプは **\[DataContract\]** および **\[DataMember\]** 属性を実装する必要があります。

```C#
using System.Runtime.Serialization;
using Microsoft.Dynamics.Commerce.Runtime.Messages;

[DataContract]
public sealed class GetStoreHoursDataRequest : Request
{
    public GetStoreHoursDataRequest(string storeNumber)
    {
        this.StoreNumber = storeNumber;
    }

    [DataMember]
    public string StoreNumber { get; private set; }
}
```

新しい応答タイプは要求タイプに似ています。

```C#
[DataContract]
public sealed class GetStoreHoursDataResponse : Response
{
    public GetStoreHoursDataResponse(PagedResult dayHours)
    {
        this.DayHours = dayHours;
    }

    [DataMember]
    public PagedResult DayHours { get; private set; }
}
```

次に、要求および応答タイプを使用する新しい CRT サービスを作成する必要があります。

## <a name="creating-a-new-crt-service"></a>新しい CRT サービス注文を作成しています

1. 新しいサービスを実装します。

    ```typescript
    public class StoreHoursDataService : IRequestHandlerAsync
    ```

2. インターフェイスのメンバー 2 つを実装します。 **SupportedRequestTypes** メンバーは、このサービスが処理できるすべての要求の一覧を返します。 **実行** メソッドは、このサービスの要求が実行された場合に、CRT が呼び出すメソッドです。

  ```C#
   public IEnumerable<Type> SupportedRequestTypes
            {
                get
                {
                    return new[] 
                    {
                        typeof(GetStoreHoursDataRequest),
                     };
                }
            }

    public async Task<Response> Execute(Request request)
            {
                if (request == null)
                {
                    throw new ArgumentNullException("request");
                }

                Type reqType = request.GetType();
                if (reqType == typeof(GetStoreHoursDataRequest))
                {
                    return await this.GetStoreDayHoursAsync((GetStoreHoursDataRequest)request).ConfigureAwait(false);
                }
                else
                {
                    string message = string.Format(CultureInfo.InvariantCulture, "Request '{0}' is not supported.", reqType);
                    Console.WriteLine(message);
                    throw new NotSupportedException(message);
                }
            }

            private async Task<Response> GetStoreDayHoursAsync(GetStoreHoursDataRequest request)
            {
                ThrowIf.Null(request, "request");

                using (DatabaseContext databaseContext = new DatabaseContext(request.RequestContext))
                {
                    var query = new SqlPagedQuery(request.QueryResultSettings)
                    {
                        DatabaseSchema = "ext",
                        Select = new ColumnSet("DAY", "OPENTIME", "CLOSINGTIME", "RECID"),
                        From = "CONTOSORETAILSTOREHOURSVIEW",
                        Where = "STORENUMBER = @storeNumber",
                    };

                    query.Parameters["@storeNumber"] = request.StoreNumber;
                    return new GetStoreHoursDataResponse(await databaseContext.ReadEntityAsync<DataModel.StoreDayHours>(query).ConfigureAwait(false));
                }
            }
    ```

3. このトピックの冒頭で説明したように、CRT の拡張機能を登録します。

## <a name="implementing-a-new-crt-service-that-handles-a-single-new-request"></a>1 つの新しい要求を処理する新しい CRT サービスの実装

単一の要求サービスを作成すると少し便利になります。

```C#
public class CrossLoyaltyCardService : SingleAsyncRequestHandler<GetCrossLoyaltyCardRequest>
```

前の手順で説明したように登録が行われます。

## <a name="implementing-a-new-crt-service-that-overrides-the-functionality-of-an-existing-request"></a>既存の要求の機能をオーバーライドする新しい CRT サービスの実装

場合によっては、要求および応答タイプは十分ですが、サービスの実装を変更する必要があります。 新しいデータを送信する必要がある場合は、拡張機能のプロパティを使用してエンティティ、要求、または応答オブジェクトを拡張することもします。 このシナリオでは、前述のようにサービスを作成して既存の IRequestHandler 型を使用できます。 また、commerceRuntime.Config ファイルの登録は、上書きすべきサービスの登録より前にする必要があります。 この登録順序は、Managed Extensibility Framework (MEF) が拡張ダイナミック リンク ライブラリ (DLL) を読み込む方法のために重要です。 ファイルより高いタイプが優先されます。

## <a name="implementing-a-new-crt-entity-and-using-it-in-new-crt-service"></a>新しい CRT エンティティの実装および新しい CRT サービスでの使用

すべての新しいエンティティは、**CommerceEntity** タイプであることが必要です。 このタイプを使用するとき、多くの低レベルの機能は自動的に処理されます。 次の例は、StoreHours サンプルから取得したもので、データベース テーブルにバインドされたエンティティを作成する方法を示しています。 これは、通常のケースです。

```C#
public class StoreDayHours : CommerceEntity
{
    private const string DayColumn = "DAY";
    private const string OpenTimeColumn = "OPENTIME";
    private const string CloseTimeColumn = "CLOSINGTIME";
    private const string IdColumn = "RECID";

    public StoreDayHours()
        : base("StoreDayHours")
    {
    }

    [DataMember]
    [Column(DayColumn)]
    public int DayOfWeek
    {
        get { return (int)this[DayColumn]; }
        set { this[DayColumn] = value; }
    }

    [DataMember]
    [Column(OpenTimeColumn)]
    public int OpenTime
    {
        get { return (int)this[OpenTimeColumn]; }
        set { this[OpenTimeColumn] = value; }
    }

    [DataMember]
    [Column(CloseTimeColumn)]
    public int CloseTime
    {
        get { return (int)this[CloseTimeColumn]; }
        set { this[CloseTimeColumn] = value; }
    }

    [Key]
    [DataMember]
    [Column(IdColumn)]
    public long Id
    {
        get { return (long)this[IdColumn]; }
        set { this[IdColumn] = value; }
    }
}
```

サービスで新しいエンティティを使用する場合、プロセスは簡単です。 前述のように、派生 IRequestHandler として新しいサービスを作成します。 次に、新しいエンティティを使用するか返すかのいずれかを実行します。 次の例は、データベースからエンティティを読み取り、それを応答の一部として返す方法を示しています。

```C#
   private async Task<Response> GetStoreDayHoursAsync(GetStoreHoursDataRequest request)
            {
                ThrowIf.Null(request, "request");

                using (DatabaseContext databaseContext = new DatabaseContext(request.RequestContext))
                {
                    var query = new SqlPagedQuery(request.QueryResultSettings)
                    {
                        DatabaseSchema = "ext",
                        Select = new ColumnSet("DAY", "OPENTIME", "CLOSINGTIME", "RECID"),
                        From = "CONTOSORETAILSTOREHOURSVIEW",
                        Where = "STORENUMBER = @storeNumber",
                    };

                    query.Parameters["@storeNumber"] = request.StoreNumber;
                    return new GetStoreHoursDataResponse(await databaseContext.ReadEntityAsync<DataModel.StoreDayHours>(query).ConfigureAwait(false));
                }
            }
```


> [!NOTE]
> Commerce エンティティはスレッド セーフではありません。つまり、別のスレッドが書き込みを行っているときに、同じオブジェクトの読み取りや変更を行わないようにする必要があります。 これは、拡張コードのカスタム エンティティと OOB エンティティに適用されます。 同一の共有オブジェクトに対して読み取り/書き込みの操作を同期的に実行する場合は、2 つの異なるスレッドを使用しないでください。

前の例では、CRT ランタイム エンジンは、登録されているデータ アダプターを介してチャンネルに自動的にクエリを作成します。 名前 **crt.ISVRetailStoreHoursView** を持つ型を照会して、コードで指定された **where** 句および列を生成します。 カスタマイザーは、カスタマイズの一部として SQL オブジェクトを提供する役割を担います。

## <a name="adding-pre-triggers-and-post-triggers-for-a-specific-request"></a>特定の要求のプレトリガーとポストトリガーの追加 

CRT トリガーの拡張機能の作成方法については、[Commerce Runtime (CRT) トリガーの拡張機能](commerce-runtime-extensibility-trigger.md) を参照してください。

## <a name="retail-server-extension"></a>Retail Sever の拡張機能

新しい Retail Server API を作成する方法については、[新しい Retail Server 拡張 API の作成](retail-server-icontroller-extension.md) を参照してください。
