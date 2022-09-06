---
title: Commerce Runtime (CRT) の拡張機能
description: この記事では、Commerce Runtime (CRT) と Retail Server を拡張するさまざまな方法について説明します。
author: josaw1
ms.date: 08/31/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Developer
ms.reviewer: josaw
ms.search.region: Global
ms.author: josaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.custom: 104593
ms.assetid: 1397e679-8cd5-49f3-859a-83d342fdd275
ms.openlocfilehash: aa0d5faafd737fbdd073318fc801d48b05431c80
ms.sourcegitcommit: 09d4805aea6d148de47c8ca38d8244bbce9786ce
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/31/2022
ms.locfileid: "9386954"
---
# <a name="commerce-runtime-crt-extensibility"></a>Commerce Runtime (CRT) の拡張機能

[!include [banner](../includes/banner.md)]

この記事では、Commerce Runtime (CRT) を拡張するさまざまな方法について説明します。 ここでは、拡張プロパティの概念について説明し、CRT エンティティに加えて拡張プロパティに永続性を持たせる方法、および持たせないようにする方法を説明します。

CRT にはコア ビジネス ロジックが含まれています。 ビジネス ロジックを追加または変更するには、CRT をカスタマイズする必要があります。 C# を使用して、すべての CRT コードが開発され、コンパイルされてクラス ライブラリとしてリリースされます (.NET アセンブリ)。 販売時点管理 (POS) はシン クライアントです。 すべてのビジネス ロジックは、CRT で行われます。 POS は、任意のビジネス ロジックを実行する CRT を呼び出し、CRT は情報を処理して POS に送り返されます。

すべての CRT サービスは、1 つ以上の要求と応答のグループで構成されます。 POS が、Retail Server に要求を送信し、Retail Server は CRT を呼び出します。 続いて CRT は要求を処理し、応答を送り返します。

たとえば、CRT の製品サービスには、製品関連のすべての要求と応答が含まれており、それぞれは異なるフローで実行されています。 同様に、CRT の顧客サービスには、顧客関連のすべての要求と応答が含まれています。 次の表に、顧客サービスの要求を示します。

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

CRT 拡張パターンについて学習する前に、CRT 拡張の作成方法を理解する必要があります。 CRT は単に、C# クラス ライブラリ (.NETアセンブリ) のコレクションです。 C# でクラス ライブラリ プロジェクトを作成し、次のサブセクションに示すパターンを使用してすべての CRT 拡張を実行できます。 これらのサンプルには、適切なアセンブリ参照、Microsoft .NET Framework バージョン、アウトプット タイプ、およびビルド パラメーターが含まれているので、Microsoft が拡張のためのテンプレートとして提供するサンプルを常に使用します。 また、他のすべての必須パラメーターがコンフィギュレーション済みです。 同様のサンプルコードは、R\\RetailSDK\\SampleExtensions\\CommerceRuntime の Retail ソフトウェア開発キット (CRT) で見つけることができます。

> [!NOTE]
> バージョン 10.0.19 の場合は、CRT 拡張プロジェクトのすべてのクラス ライブラリで .NET Standard 2.0 をターゲット フレームワークとして使用する必要があります。

### <a name="create-a-new-crt-service"></a>新しい CRT サービスの作成

新しい機能または新しい仕様を作成できます。

### <a name="override-the-existing-service"></a>既存のサービスを上書きする

完全に既存の機能をオーバーライドしたり、ビジネス フローに従ってカスタマイズできます。 次にいくつか例を挙げます。

+ 検索機能を上書きして、すぐに使用できる検索機能の代わりに、外部システムから検索する必要があります。

必要な場合に限り、ハンドラーを上書きする必要はありません。 代わりに、プレトリガーまたはポストトリガーを使用して、CRT の拡張機能のシナリオを実装します。 

### <a name="executing-the-next-crt-handler---chain-of-handlers"></a>次の CRT ハンドラの実行 - ハンドラーのチェーン

プラットフォーム更新プログラムのバージョン 10.0.19 以降を使用して、CRT フレームワークは **ExecuteNextAsync** および **GetNextAsyncRequestHandler** をサポートします。 これらのメソッドを使用して、上書きされた拡張機能コードで基本要求およびハンドラーを実行します。 **CommerceRuntime.Ext.config** ファイルに一覧表示された注文に基づいて、CRT フレームワークも同じハンドラを複数回実行することができます。

#### <a name="executenextasync"></a>ExecuteNextAsync

**ExecuteNextAsync** メソッドを使用して、要求を上書きし、基本要求を上書きします。 上書きでは、たとえば拡張子プロパティを設定するなど、カスタム ロジックを追加できます。 たとえば、**顧客** の保存要求を上書きし、**ExecuteNextAsync** を使用して最初に基本顧客要求に電話をし、次に追加ロジックを追加して顧客拡張機能のプロパティを保存します。

#### <a name="getnextasyncrequesthandler"></a>GetNextAsyncRequestHandler

ハンドラを上書きし、基本ハンドラを呼び出してすぐに使えるロジックを実行してカスタム ロジックを使い基本ハンドラの結果を変更する場合は、**GetNextAsyncRequestHandler** を使用します。 

たとえば、すぐに使える Azure Search ハンドラーを使用して **製品** を検索し、さらにロジックを追加し在庫に基づいて結果を変更できます。 カスタム検索結果を含めるか、結果をフィルタ処理することができます。

### <a name="nothandledresponse"></a>NotHandledResponse

上書きされたハンドラーで、基本ハンドラーを実行し、カスタム ロジックの代わりに基本応答を返す場合は、**NotHandledResponse()** を返します。 **Not HandlerdResponse** が返された場合、CRT フレームワークはすぐに使えるハンドラーを実行します。 **NotHandlerdResponse** は、特定の条件でのみカスタム ロジックを実行するシナリオで使用できます (そうではない場合は、基本ハンドラー ロジックを実行します)。

### <a name="crt-data-service-and-data-service-with-entities"></a>CRT データ サービス、およびエンティティ付きデータ サービス

CRT データ サービスを使用してチャネル データベースからデータまたはエンティティを読み取ります。

> [!NOTE]
> CRT 拡張コードでは、CRT ビジネス ロジック クラス、メソッド、またはハンドラー (**Runtime.Workflow**、**Runtime.Services**、**Runtime.DataServices** のクラスなど) を参照したり使用したりすることはできません。 これらのクラスには下位互換性がないので、アップグレード中に拡張機能が無効になる可能性があります。 拡張では、**Runtime.\*.Messages**、**Runtime.Framework**、**Runtime.Data**、**Runtime.Entities** の要求クラス、応答クラス、エンティティ クラスのみ使用する必要があります。

### <a name="triggers"></a>トリガー

任意の要求の前後に追加ロジックを実行できます。

前のトリガーで、カスタム ロジックなどのいくつかの検証を実行できます。

ポスト トリガーで、要求にいくらかのカスタム情報を追加し POS に送信できます。 または、標準機能から戻される結果の変更または追加ビジネス ロジックの実行が可能です。

CRT トリガーの拡張機能の作成方法については、[Commerce Runtime (CRT) トリガーの拡張機能](commerce-runtime-extensibility-trigger.md) を参照してください。

### <a name="extension-properties"></a>拡張プロパティ

任意の CRT エンティティにカスタム プロパティーを追加し、それを POS に送信することができます。 拡張プロパティはキーと値のペアです。 POS で拡張プロパティを設定すると、CRT で使用できるようになります。 同様に、CRT で拡張機能プロパティを設定する場合、POS で使用できます。 また、要求、応答、または要求コンテキストのレベルで拡張プロパティを設定することもできます。 既定では、拡張機能のプロパティはデータベースに保存されず、読み取られません。 拡張プロパティを読み取り、設定するには、カスタム コードを記述する必要があります。 ただし、そのカスタム コードは、POS と CRT 間で自動的に送信されます。

たとえば、POS の顧客エンティティにいくつかの追加情報をキャプチャして表示したいとします。 この場合、顧客に対するすべてのカスタム プロパティをフェッチするポスト トリガーを追加し、拡張プロパティとして顧客エンティティに追加し、それらの拡張機能プロパティを POS に送信できます。

POS から CRT に拡張機能のプロパティを送信して、カスタム テーブルに保存できます。 または、これらのプロパティに基づくいくつかのカスタム ロジックの実行または Commerce 本社への送信が可能です。

製品、顧客、トランザクション、およびパラメーターなどのすべての CRT エンティティは、拡張機能プロパティをサポートします。

> [!NOTE]
> 属性もまたサポートされます (コンフィギュレーション駆動型の開発)。 拡張プロパティの場合は、カスタム テーブルを作成し、データを格納する必要があります。 ただし、属性はコンフィギュレーション駆動型であり、テーブル フィールドを作成する場合は必須ではありません。 したがって、読み取りおよび更新操作にコードは必要ありません。

属性についての詳細は、次の記事を参照してください:

+ [注文属性](order-attributes.md)
+ [顧客属性](customer-attributes.md)

### <a name="extend-commerce-data-exchange---real-time-service-classes"></a>Commerce Data Exchange - リアルタイム サービス クラスの拡張

CRT から Commerce 本部の同期呼び出しを行うことができます。

Commerce Data Exchange - リアル タイム サービスを拡張する方法についての詳細は、[Commerce Data Exchange - リアル タイム サービスの拡張](extend-commerce-data-exchange.md) を参照してください。

## <a name="retail-server-extension"></a>Retail Server の拡張機能

新しい Retail Server API を作成する方法については、[新しい Retail Server 拡張 API の作成](retail-server-icontroller-extension.md) を参照してください。

## <a name="exception-handling"></a>例外処理

拡張子コードに `try...catch` ステートメントを追加して例外を処理し、それを Application Insights に記録するかクライアント アプリケーションに反映することができます。 エラー メッセージをクライアントに反映する場合は、CRT または Retail Server から集計された例外を返したりしません。 代わりに、個々のタスク レベルで例外を受け取り、再実行します。 詳細については、以下の記事を参照してください。

+ [例外処理 (タスク並列ライブラリ)](/dotnet/standard/parallel-programming/exception-handling-task-parallel-library)。
+ [拡張イベントを Application Insights に記録する](commerce-application-insights.md)
+ [Commerce の拡張リソースおよびラベル ファイルをローカライズ](extension-resource-localization.md) して、クライアント アプリケーション で CRT 例外を記録および表示します。

## <a name="register-the-crt-extension"></a>CRT 拡張機能の登録

### <a name="online"></a>オンライン

オンライン モードの場合 (POS が Retail Server に接続された場合)、CRT の拡張を終了後、拡張ライブラリを **\\RetailServer\\webroot\\bin\\Ext** フォルダーに配置します。 **CommerceRuntime.Ext.config** ファイルの **構成** セクションを、以下の例のようにカスタム ライブラリ情報で更新します。

```xml
<add source="assembly" value="your custom library name" />
```

たとえば、カスタム ライブラリの名前が **Contoso.Commerce.Runtime.CustomerSearchSample** の場合、**構成** セクションに次の行を追加します。

```xml
<add source="assembly" value="Contoso.Commerce.Runtime.CustomerSearchSample" />
```

### <a name="offline"></a>オフライン

オフライン モードの場合は、CRT の拡張を終了後、カスタム ライブラリを **\\Program Files (x86)\\Microsoft Dynamics 365\\70\\Retail Modern POS\\ClientBroker\\ext** フォルダーに配置します。 **CommerceRuntime.MPOSOffline.ext.config** ファイルの **構成** セクションを、以下の例のようにカスタム ライブラリ情報で更新します。

```xml
<add source="assembly" value="your custom library name" />.
```

## <a name="register-the-extension-configuration-in-the-commerceruntimeextconfig-file"></a>CommerceRuntime.Ext.config ファイルに拡張コンフィギュレーションを登録する

拡張機能では、**\<settings\>** ノードの **CommerceRuntime.Ext.config** ファイルにキー値のコンフィギュレーションを登録できます。

**\<settings\>** ノードは、CommerceRuntime コンポーネントを設定するために使用されるキーと値のペアのコレクションです。 この規則では、設定用のキーにそのキーが構成している機能領域を表す接頭語を付け、接頭語とキーの区切りとしてピリオド (.) を使用します。 CRT の初期化では、この規則が適用されるので、拡張コンフィギュレーション値の前には必ず **ext** を付ける必要があります。 その接頭語を持たない拡張子は読み込まれません。 追加の接頭語を追加して、キーの構成サブ領域を表すことができます。 次の例では、キーと値のペアを示しています。

```xml
<add name="ext.SalesTransaction.Storage.CartSerializationFormat" value="XML" />
```

Commerce Data Exchange - リアルタイム サービスへの呼び出しでの HTTP バインドのタイムアウトについては、メソッドごとにタイムアウトを秒単位でを設定します。 このタイムアウト値は、**CommerceRuntime.config** で設定された **maxExtensionTimeoutInSeconds** 値によって制限されます。

```xml
<add name="ext.RealTimeServiceClient.TimeoutInSeconds.InvokeExtensionMethod.ContosoRetailStoreHours_UpdateStoreHours" value="300" />
```

CRT 拡張コンフィグレーションからキー値を読み取るために、**RequestContext.Runtime.Configuration** を使用できます。 次の例では、値を取得する方法を示します。

```csharp
string key = context.Runtime.Configuration.GetSettingValue("ext.SalesTransaction.Storage.CartSerializationFormat") ?? string.Empty;
```

上記の手順は、手動による展開および開発ボックスでのテストのために使用されます。 拡張機能をパッケージ化し、生産またはユーザー受け入れテスト (UAT) に配置するには、パッケージ ドキュメントの情報を使用します。

## <a name="debug-crt"></a>デバッグ CRT

### <a name="attach-the-crt-extension-project-online"></a>CRT 拡張 Project Online を関連付ける

POS から CRT をデバッグするには、POS が Retail Server に接続されているときに、CRT 拡張プロジェクトを **w3wp.exe** プロセス (Retail Server の インターネット インフォメーション サービス \[IIS\] プロセス) に関連付けます。

### <a name="attach-the-crt-extension-project-offline"></a>オフラインで CRT 拡張プロジェクトを関連付ける

オフライン デバッグの場合は、**dllhost.exe** プロセスに CRT 拡張プロジェクトを関連付けます。

> [!NOTE]
> CRT 拡張コードでは、CRT ビジネス ロジック クラス、メソッド、またはハンドラー (**Runtime.Workflow**、**Runtime.Services**、**Runtime.DataServices** のクラスなど) を参照したり使用したりすることはできません。 これらのクラスには下位互換性がないので、アップグレード中に拡張機能が無効になる可能性があります。 拡張では、**Runtime.\*.Messages**、**Runtime.Framework**、**Runtime.Data**、**Runtime.Entities** の要求クラス、応答クラス、エンティティ クラスのみ使用する必要があります。

## <a name="sample-to-create-a-new-crt-service-class"></a>新しい CRT サービス クラス作成のサンプル

新しいサービス クラスを作成し、1 つ以上の要求または応答を実装できます。 この方法を使用して新しい機能を作成します。

新しい CRT サービスに次のクラスを実装します。

- **クラスのリクエスト** – このクラスは、POS、Retail サーバー、e コマース、CRT ワークフロー クラスの作業の要求を行います。
- **応答クラス** – このクラスは、呼び出し元の要求に基づいて、応答を返します。
- **ハンドラー クラス** – このクラスには、要求のコア ロジックが含まれます。 ハンドラー クラスで、他の要求を呼び出して、カスタム ロジック、および他のタスクを実行できます。

作業のシリアル化については、新しい要求タイプは **\[DataContract\]** および **\[DataMember\]** 属性を実装する必要があります。

> [!NOTE]
> - 拡張機能コードに対して、要求の実行時に **ConfigureAwait(false)** を使用することをお勧めします。
> - CRT データベース拡張機能での Microsoft 分散トランザクション コーディネーター (MSDTC) の使用はサポートされていません。
> - 既存の CRT 要求および応答を TransactionScope でラッピングすると、同じトランザクション内で複数のデータベース接続が開かれているため、データベースの例外が発生する可能性があるため、避けてください。 また、パフォーマンスを改善するには、読み取りシナリオに TransactionScope を使用しないようにしてください。 代わりに、**TransactionSyncAsyncFlowOption.Enabled** を指定して、非同期呼び出しを適切に許可します。


### <a name="request-class"></a>クラスのリクエスト

```csharp
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

### <a name="response-class"></a>応答クラス

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

## <a name="create-a-new-crt-service-class"></a>新しい CRT サービス クラスの作成

1. 新しいサービスを実装します。

    ```csharp
    public class StoreHoursDataService : IRequestHandlerAsync
    ```

2. インターフェイスのメンバー 2 つを実装します。 **SupportedRequestTypes** メンバーは、このサービスが処理できるすべての要求の一覧を返します。 **実行** メソッドは、このサービスの要求が実行された場合に、CRT が呼び出すメソッドです。

    ```csharp
    public IEnumerable<Type> SupportedRequestTypes
            {
                get
                {
                  return new[] 
                  {
                        typeof(GetStoreHoursDataRequest),
                        typeof(UpdateStoreDayHoursDataRequest),
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
                else if (reqType == typeof(UpdateStoreDayHoursDataRequest))
                {
                    return await this.UpdateStoreDayHoursAsync((UpdateStoreDayHoursDataRequest)request).ConfigureAwait(false);
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
            
            private async Task<Response> UpdateStoreDayHoursAsync(UpdateStoreDayHoursDataRequest request)
            {
                ThrowIf.Null(request, "request");
                ThrowIf.Null(request.StoreDayHours, "request.StoreDayHours");
                if (request.StoreDayHours.DayOfWeek < 1 || request.StoreDayHours.DayOfWeek > 7)
                {
                    throw new DataValidationException(DataValidationErrors.Microsoft_Dynamics_Commerce_Runtime_ValueOutOfRange);
                }

                InvokeExtensionMethodRealtimeRequest extensionRequest = new InvokeExtensionMethodRealtimeRequest(
                    "ContosoRetailStoreHours_UpdateStoreHours",
                    request.StoreDayHours.Id,
                    request.StoreDayHours.DayOfWeek,
                    request.StoreDayHours.OpenTime,
                    request.StoreDayHours.CloseTime);
                InvokeExtensionMethodRealtimeResponse response = await request.RequestContext.ExecuteAsync<InvokeExtensionMethodRealtimeResponse>(extensionRequest).ConfigureAwait(false);
                ReadOnlyCollection<object> results = response.Result;

                long recId = Convert.ToInt64(results[0]);

                using (var databaseContext = new DatabaseContext(request.RequestContext))
                {
                    ParameterSet parameters = new ParameterSet();
                    parameters["@bi_Id"] = recId;
                    parameters["@i_Day"] = request.StoreDayHours.DayOfWeek;
                    parameters["@i_OpenTime"] = request.StoreDayHours.OpenTime;
                    parameters["@i_ClosingTime"] = request.StoreDayHours.CloseTime;
                    await databaseContext.ExecuteStoredProcedureNonQueryAsync("[ext].UPDATESTOREDAYHOURS", parameters, resultSettings: null).ConfigureAwait(false);
                }

                return new UpdateStoreDayHoursDataResponse(request.StoreDayHours);
            }
    ```

3. この記事で先に説明されたように、 CRT 拡張子を登録します。

前のサンプル コードに、**UpdateStoreDayHoursDataRequest** と **UpdateStoreDayHoursDataResponse** の実装がありません。 完全なサンプル コードは、Retail SDK の **RetailSDK\\SampleExtensions\\CommerceRuntime\\Extensions.StoreHoursSample** フォルダーで使用可能です。

## <a name="implement-a-new-crt-service-that-handles-a-single-new-request"></a>1 つの新しい要求を処理する新しい CRT サービスの実装

単一の要求サービスを作成すると少し便利になります。

```C#
namespace Contoso
{
    namespace Commerce.Runtime.CrossLoyaltySample
    {
        using System;
        using System.Threading.Tasks;
        using Messages;
        using Microsoft.Dynamics.Commerce.Runtime;
        using Microsoft.Dynamics.Commerce.Runtime.Messages;

        /// <summary>
        /// Service class responsible executing the service requests.
        /// </summary>
        public class CrossLoyaltyCardService : SingleAsyncRequestHandler<GetCrossLoyaltyCardRequest>
        {
            /// <summary>
            /// Process method. 
            /// </summary>
            /// <param name="request">The request with the loyalty number.</param>
            /// <returns>The discount value.</returns>
            protected override async Task<Response> Process(GetCrossLoyaltyCardRequest request)
            {
                if (request == null)
                {
                    throw new ArgumentNullException("request");
                }

                var serviceResponse = new GetCrossLoyaltyCardResponse(0);

                //Business logic

                return await Task.FromResult(serviceResponse);
            }
        }
    }
}
```

## <a name="implement-a-crt-service-that-overrides-the-functionality-of-an-existing-request"></a>既存の要求の機能をオーバーライドする CRT サービスの実装

場合によっては要求タイプと応答タイプで十分ですが、別のロジックを実行するには標準のサービス実装ロジックを変更する必要があります。また、外部サービスと統合してそのロジックを実行する必要があります。 既定の実装のオーバーライドは、ロジックを完全に置換する場合にのみ行う必要があります。 たとえば、標準の税の実装を使用するのではなくサード パーティの税ロジックを使用する場合は、税サービス要求を上書きします。 その他のシナリオのほとんどは、要求にプレ トリガーまたはポスト トリガーを追加することで達成できます。 要求を上書きしないようにしてください。 要求を上書きすると、カスタム ロジックが実行され、この上書きされた要求で行われる将来の拡張機能が利用できない可能性があります。

また、**commerceRuntime.ext.Config** ファイルの登録は、上書きすべきサービスの登録より前にする必要があります。 この登録順序は、Managed Extensibility Framework (MEF) が拡張ダイナミック リンク ライブラリ (DLL) を読み込む方法のために重要です。 ファイルより高いタイプが優先されます。

ハンドラーを上書きするには、ハンドラー名に基づいてハンドラーを実行する場合に `SingleAsyncRequestHandler<TRequest>` または **INamedRequestHandlerAsync** を実装します。

### <a name="sample-code-that-shows-how-to-override-createorupdatecustomerdatarequest-using-the-singleasyncrequesthandler"></a>SingleAsyncRequestHandler を使用した CreateOrUpdateCustomerDataRequestを 上書きする方法を示すサンプル コード 

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

                return new SingleEntityDataServiceResponse<Customer>(customer);
            }
        }
    }
}
```

### <a name="sample-code-on-how-to-override-the-handlers-which-are-implemented-based-on-handler-name-implement-the-inamedrequesthandlerasync"></a>ハンドラー名に基づいて実装されたハンドラーを上書きする方法のサンプル コード、INamedRequestSyncrAsync を実装します。 

```C#
    public class SampleGetProductSearchResultshandler : INamedRequestHandlerAsync
    {
        /// <summary>
        /// Gets the supported requests types.
        /// </summary>
        public IEnumerable<Type> SupportedRequestTypes
        {
            get
            {
                return new[] { typeof(GetProductSearchResultsServiceRequest), };
            }
        }

        public string HandlerName
        {
            get
            {
                return "CommerceProductSearch";
            }
        }

        public async Task<Response> Execute(Request request)
        {
            ThrowIf.Null(request, nameof(request));
            Type requestType = request.GetType();
            Response response = null;

            if (requestType == typeof(GetProductSearchResultsServiceRequest))
            {
                //Implement the logic here
            }

            return response;
        }
    }

```



## <a name="run-the-base-handler-in-the-extension"></a>拡張機能で基本ハンドラーを実行する

### <a name="executing-the-next-crt-handler---chain-of-handlers"></a>次の CRT ハンドラの実行 - ハンドラーのチェーン

#### <a name="executenextasync"></a>ExecuteNextAsync

**ExecuteNextAsync** メソッドを使用して、要求を上書きし基本要求を呼び出し、そしてカスタム ロジックを追加して拡張機能プロパティを設定できます。 たとえば、**顧客** の保存要求を上書きし、**ExecuteNextAsync** を使用して最初に基本顧客要求に電話をし、次に追加ロジックを追加して顧客拡張機能のプロパティを保存できます。

```csharp
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
        {
            // Execute original functionality to save the customer.
            var response = await this.ExecuteNextAsync<SingleEntityDataServiceResponse<Customer>>(request).ConfigureAwait(false);

            // Execute additional functionality to save the customer's extension properties.
            if (!request.Customer.ExtensionProperties.IsNullOrEmpty())
            {
                // The stored procedure will determine which extension properties are saved to which tables.
                ParameterSet parameters = new ParameterSet();
                parameters["@TVP_EXTENSIONPROPERTIESTABLETYPE"] = new ExtensionPropertiesExtTableType(request.Customer.RecordId, request.Customer.ExtensionProperties).DataTable;
                await databaseContext.ExecuteStoredProcedureNonQueryAsync("[ext].UPDATECUSTOMEREXTENSIONPROPERTIES", parameters, resultSettings: null).ConfigureAwait(false);
            }

            return response;
        }
    }
}
```

#### <a name="getnextasyncrequesthandler"></a>GetNextAsyncRequestHandler

ハンドラを上書きし、基本ハンドラを呼び出して OOB ロジックを実行してカスタム ロジックを使い基本ハンドラの結果を変更する場合は、**GetNextAsyncRequestHandler** を使用します。 たとえば、すぐに使える Azure Search ハンドラーを使用して製品を検索し、顧客検索結果まを含めるか結果をフィルターするかで、さらにロジックを追加し在庫に基づいて結果を変更できます。

```csharp

protected override async Task<Response> Process(SaveSalesTransactionDataRequest request)
{
    ThrowIf.Null(request, "request");

    // The extension should do nothing If fiscal registration is enabled and legacy extension were used to run registration process.
    if (!string.IsNullOrEmpty(request.RequestContext.GetChannelConfiguration().FiscalRegistrationProcessId))
    {
        return new NotHandledResponse();
    }

    NullResponse response;

    using (var databaseContext = new DatabaseContext(request.RequestContext))
    {
        // Execute original logic.
        var requestHandler = request.RequestContext.Runtime.GetNextAsyncRequestHandler(request.GetType(), this);
        response = await request.RequestContext.Runtime.ExecuteAsync<NullResponse>(request, request.RequestContext, requestHandler, false).ConfigureAwait(false);

        // Extension logic.
        if (request.RequestContext.GetChannelConfiguration().CountryRegionISOCode == CountryRegionISOCode.FR)
        {
            response = await SaveSalesTransactionExtAsync(request).ConfigureAwait(false);
        }

    }

    return response;
}
```

### <a name="nothandledresponse"></a>NotHandledResponse

一部のシナリオでは、オーバーライドされたロジックで基本ハンドラーを実行する場合、**new NotHandledResponse()** を返すことによって基本ハンドラーを実行できます。 **NotHandledResponse** が返された場合、CRT フレームワークは、基本または帯域外ロジックの実行を要求する拡張機能を使用するため、 帯域外ハンドラーを実行します。

```csharp
private Response GetCustomReceiptFieldForSalesTransactionReceipts(GetLocalizationCustomReceiptFieldServiceRequest request)
{
    ThrowIf.Null(request.SalesOrder, nameof(request.SalesOrder));

    string receiptFieldName = request.CustomReceiptField;
    string receiptFieldValue = string.Empty;

    if (request.SalesOrder.TaxCalculationType == TaxCalculationType.GTE)
    {
        switch (receiptFieldName)
        {
            case "Sample":
                receiptFieldValue = this.GetGstRegistrationNumber(request);
                break;
            default:
                return new NotHandledResponse();
        }
    }
    else
    {
        return new NotHandledResponse();
    }

    int receiptFieldLength = request.ReceiptItemInfo == null ? 0 : request.ReceiptItemInfo.Length;
    var returnValue = ReceiptStringUtils.WrapString(receiptFieldValue, receiptFieldLength);

    return new GetCustomReceiptFieldServiceResponse(returnValue);
}
```

## <a name="run-an-extension-request-for-a-channel-type"></a>チャネル タイプに対して拡張要求を実行する

場合によっては、拡張要求を特定のチャネル タイプに対してのみ実行する必要があります。 たとえば、要求はオンライン チャネルに対して実行する必要がありますが、小売チャネル (物理店舗) については実行する必要がありません。 このような場合は、要求を実行する前にチャネル タイプを確認します。 その後、カスタム ロジックを実行するか、**NotHandledResponse()** を呼び出して基本ロジックを実行します。

```csharp
if (requestContext.GetChannel().OrgUnitType == RetailChannelType.RetailStore)
{
    // run your extension code here.
}
else
{
    return new NotHandledResponse();
}
```

## <a name="implement-a-new-crt-entity-and-use-it-in-the-new-crt-service"></a>新しい CRT エンティティの実装および新しい CRT サービスでの使用

すべての新しいエンティティは、**CommerceEntity** タイプから継承する必要があります。 このタイプを使用するとき、多くの低レベルの機能は自動的に処理されます。 次の例は **StoreHours** サンプルから取得されます。 データベース テーブルにバインドされたエンティティを作成する方法を示します。 このシナリオは共通です。

```csharp
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

サービスで新しいエンティティを使用する場合、プロセスは簡単です。 この記事で前述されているように、**IRequestHandler** から派生した新しいサービスを作成します。 次に、新しいエンティティを使用するか返すかのいずれかを実行します。 次の例は、データベースからエンティティを読み取り、それを応答の一部として返す方法を示しています。

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
> Commerce エンティティは、スレッド セーフです。 したがって、別のスレッドが書き込みを行っている時、同じオブジェクトを読み取りまたは変更する必要はありません。 この制限は、拡張コードのカスタム エンティティと標準エンティティに適用されます。 同一の共有オブジェクトに対して読み取り/書き込みの操作を同期的に実行する場合は、2 つの異なるスレッドを使用しないでください。

前の例では、CRT ランタイム エンジンは、登録されているデータ アダプターを介してチャンネルに自動的にクエリを作成します。 名前 **crt.ISVRetailStoreHoursView** を持つ型を照会して、コードで指定された **where** 句および列を生成します。 カスタマイザーは、カスタマイズの一部として SQL オブジェクトを提供する役割を担います。

## <a name="using-extension-properties-on-crt-entities-requests-and-responses"></a>CRT エンティティ、依頼および応答での拡張プロパティの使用

既存の CRT エンティティに新しいデータを追加する 1 つの方法は、拡張プロパティを使用することです。 拡張プロパティは、エンティティのキーと値のペアです。 既定では、これらのキーと値のペアはデータベースで保持されません。 拡張プロパティを保持するためには、カスタム コードを記述する必要があります。

## <a name="using-extension-properties-on-crt-entities-with-persistence"></a>CRT エンティティでの拡張プロパティの永続的な使用

エンティティに追加する任意の拡張プロパティは、シナリオしだいでオブジェクトまたはトランザクションのいずれかの有効期間の POS および CRT メモリに保持されます。 拡張プロパティは、アプリケーションの境界にもまたがって移動します。 たとえば、Retail Modern POS に拡張プロパティを追加し、Retail Server または CRT を呼び出すと、キーと値のペアがそのフロー全体で使用できます。 また、そのエンティティが Commerce Data Exchange - リアルタイム サービス を呼び出し中に送信されると、キーと値のペアは処理中に使用できます。

> [!NOTE]
> Commerce 本社では、拡張プロパティは顧客と注文に対してのみ送信されます。

ただし、既述のように、拡張プロパティは既定では保持されていません。 拡張プロパティを保持する場合は、データ モデリングを実行して、データの格納場所を適切に設計することを確認する必要があります。 新しいテーブルと結合を使用することをお勧めします。 この方法は、ほとんどの要件に適合します。 Retail SDK の **EmailPreference** サンプルは、代表的なエンド ツー エンドの例を提供します。

### <a name="location-of-the-sample-code-in-the-retail-sdk"></a>Retail SDK のサンプル コードの場所

…\\RetailSDK\\SampleExtensions\\CommerceRuntime\\Extensions.EmailPreferenceSample

### <a name="location-of-the-scripts"></a>スクリプトの場所

…\\RetailSDK\\ドキュメント\\SampleExtensionsInstructions\\EmailPreference

### <a name="syntax-to-set-an-extension-property-on-an-entity"></a>エンティティに拡張子プロパティを設定する構文

```csharp
public virtual void SetProperty(string key, object value);
entity.SetProperty("key", value);
```

### <a name="example"></a>例

#### <a name="scenario"></a>シナリオ

顧客エンティティおよび拡張用に作成された新しい拡張テーブルとフィールドは、拡張テーブルからそれらのフィールドを読み取り、POS に送信する必要があります。

チャネル データベースを拡張する場合は、拡張テーブルにメイン テーブルの主キーを含めることをお勧めします。 つまり、直接の関係を持たずに、主キーを使用して拡張テーブルからデータを読み取ります。

#### <a name="steps"></a>ステップ

1. メイン テーブルの主キーを持つチャネル データベース拡張スキーマで 顧客 エンティティの拡張テーブルを作成します。
2. 顧客エンティティを読み取る CRT データ要求を識別します。
3. データ要求の転記トリガーを追加します。 顧客 テーブルの主キーを使用して、拡張テーブルを照会し、カスタム フィールドを読み取ることができます。

    > [!NOTE]
    > ポスト トリガー要求でエンティティの主キーを取得できます。 エンティティ オブジェクトを持つその要求、およびすべての必須フィールドを持つそのエンティティ オブジェクト。

4. カスタム フィールドを拡張プロパティとして、CRT 転記トリガーの共有パラメーター エンティティへ追加し、POS へ送信します。

## <a name="reading-extension-properties-in-triggers"></a>トリガーの拡張機能プロパティの読み取り

顧客テーブルからデータを読み込む要求は、**GetCustomerDataRequest** です。 次の例では、この要求のポスト トリガーを追加する方法を示します。

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

### <a name="scenario"></a>シナリオ

顧客用に新しい拡張テーブルを作成しました。 顧客の拡張フィールドの値が POS または CRT から来た場合は、その値をカスタム テーブルに格納します。

> [!NOTE]
> 拡張のプロパティはトリガーで、またはハンドラーを上書きすることによって設定することができます。 拡張テーブルから読み込んで拡張プロパティを設定しただけの場合、トリガーを使用することができます。

### <a name="steps"></a>ステップ

1. メイン テーブルに主キーの関係があるチャネル テーブル内の、顧客の拡張テーブルを作成します。 (この場合、メイン テーブルは CustTable です。)
2. CustTable にデータを設定する CRT データ要求を識別します。
3. ハンドラーを上書きし、メイン テーブル (CustTable) で値を設定する基本要求を呼び出してから、拡張テーブルで値を設定する基本要求を呼び出します。

> [!NOTE]
> 拡張コードでは、拡張手順またはビューに必要な追加のプロパティを渡すことができます。 拡張プロパティは、CRT プレ トリガーまたはポスト トリガーに保存できます。 CRT ハンドラーを上書きする必要はありません。 ハンドラーのオーバーライドは避けます。ほとんどの CRT 拡張機能のシナリオはプレ トリガーまたはポスト トリガーで達成できます。

次の例では、使用される SQL スクリプトがありません。 完全なサンプル コードとスクリプトは、Retail SDK の次の場所にあります。

### <a name="location-of-the-sample-code-in-the-retail-sdk"></a>Retail SDK のサンプル コードの場所

…\\RetailSDK\\SampleExtensions\\CommerceRuntime\\Extensions.EmailPreferenceSample

### <a name="location-of-the-scripts"></a>スクリプトの場所

…\\RetailSDK\\ドキュメント\\SampleExtensionsInstructions\\EmailPreference

### <a name="example"></a>例

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

                    return response;
                }
            }
        }
    }
}
```

### <a name="syntax-to-enable-the-property-to-be-read-later"></a>後で読み込むプロパティを有効にする構文

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

### <a name="setting-or-reading-extension-properties-in-pos"></a>設定または POS の拡張子プロパティの読み取り

POS で拡張プロパティーを設定して、POS API を使用してそれらを CRT に送信することができます。 または、エンティティ レベルで拡張機能プロパティの送信が可能です。

カート行に拡張プロパティを設定するには、**SaveExtensionPropertiesOnCartLinesClientRequest** を使用します。 同様に、買い物カゴ ヘッダーに対して、**SaveExtensionPropertiesOnCartClientRequest** を使用します。

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


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
