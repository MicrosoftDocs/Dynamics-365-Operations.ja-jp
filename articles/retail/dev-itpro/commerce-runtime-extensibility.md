---
title: Commerce Runtime (CRT) および Retail サーバーの拡張機能
description: このトピックでは、Commerce Runtime (CRT) と Retail サーバーを拡張するさまざまな方法について説明します。 拡張機能プロパティのコンセプトを説明し、保持有無にかかわらず CRT エンティティに追加する方法について説明します。 また、アクションを Retail サーバー コントローラーに追加して、エンティティのコントローラーを追加する方法も示します。
author: mugunthanm
manager: AnnBe
ms.date: 07/13/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Developer
ms.reviewer: rhaertle
ms.search.scope: Operations, Retail
ms.custom: 104593
ms.assetid: 1397e679-8cd5-49f3-859a-83d342fdd275
ms.search.region: Global
ms.author: mumani
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: 9ef963e1c4126d434573e7d90b958a4f156a3b94
ms.sourcegitcommit: 27a98a7a0f1d2623f5236a88066f483def30889c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/01/2019
ms.locfileid: "1833093"
---
# <a name="commerce-runtime-crt-and-retail-server-extensibility"></a>Commerce Runtime (CRT) および Retail サーバーの拡張機能

[!include [banner](../includes/banner.md)]

このトピックでは、Commerce Runtime (CRT) と Retail サーバーを拡張するさまざまな方法について説明します。 拡張機能プロパティのコンセプトを説明し、保持有無にかかわらず CRT エンティティに追加する方法について説明します。 また、アクションを Retail サーバー コントローラーに追加して、エンティティのコントローラーを追加する方法も示します。

CRT にはコア ビジネス ロジックが含まれています。 ビジネス ロジックを追加または変更するには、CRT をカスタマイズする必要があります。 C# を使用して、すべての CRT コードが開発およびコンパイルされ、クラス ライブラリとしてリリースされます (.NET アセンブリ)。 小売販売時点管理 (POS) はシン クライアントです。 すべてのビジネス ロジックは、CRT で行われます。 POS は、任意のビジネス ロジックを実行する CRT を呼び出し、CRT は情報を処理して POS に送り返されます。 

すべての CRT サービスは、1 つ以上の要求と応答のグループで構成されます。 POS で作業する際はいつでも、POSは Retail サーバーに要求を送り、Retail サーバーは CRT を呼び出します。 続いて CRT は要求を処理し、応答を送り返します。

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

**CRT がサポートする拡張子パターンのタイプ**

CRT 拡張パターンについて学習する前に、CRT 拡張の作成方法を理解する必要があります。 CRT は単に、C# クラス ライブラリ (.NETアセンブリ) のコレクションです。 C# でクラス ライブラリ プロジェクトを作成し、次の表に示すパターンを使用してすべての CRT 拡張を実行できます。 これらのサンプルには、適切なアセンブリ参照、Microsoft .NET Framework バージョン、アウトプット タイプ、およびビルド パラメーターが含まれているので、Microsoft が拡張のためのテンプレートとして提供するサンプルを常に使用します。 また、他のすべての必須パラメーターがコンフィギュレーション済みです。 同様のサンプルコードは、R\\RetailSDK\\SampleExtensions\\CommerceRuntime の Retail ソフトウェア開発キット (CRT) で見つけることができます。

<table>
<thead>
<tr>
<th>拡張機能のパターン</th>
<th>目的</th>
</tr>
</thead>
<tbody>
<tr>
<td>新しい CRT サービスの作成</td>
<td>新機能を作成します。</td>
</tr>
<tr>
<td>既存のサービスを上書きする</td>
<td>
<p>完全に既存の機能をオーバーライドしたり、ビジネス フローに従ってカスタマイズできます。</p>
<p>次にいくつか例を挙げます。
<ul>
<li>POS 検索機能を上書きして、ローカル データベースまたは本社で検索するのではなく、外部システムから検索する必要があります。 または、上書き、標準機能の呼び出しおよびいくつか追加カスタム ロジックの実行が可能です。</li>
<li>ローカル データベースまたは HQ、および外部システムを検索した後、最後に結果をマージまたは変更します。</li>
</ul>
</td>
</tr>
<tr>
<td>トリガー</td>
<td>
<p>任意の要求の前後に追加ロジックを実行できます。</p>
<p>前のトリガーで、カスタム ロジックなどのいくつかの検証を実行できます。</p>
<p>ポスト トリガーで、要求にいくらかのカスタム情報を追加し POS に送信できます。 または、標準機能から戻される結果の変更または追加ビジネス ロジックの実行が可能です。</p>
</ul>
</td>
</tr>
<tr>
<td>拡張プロパティ</td>
<td>
<p>任意の CRT エンティティにカスタム プロパティーを追加し、それを POS に送信することができます。 拡張プロパティはキーと値のペアです。 POS で拡張プロパティを設定すると、CRT で使用できるようになります。 同様に、CRT で拡張機能プロパティを設定する場合、POS で使用できます。 また、要求、応答、または要求コンテキストのレベルで拡張プロパティを設定することもできます。 既定では、拡張機能のプロパティはデータベースに保存されず、読み取られません。 拡張プロパティを読み取り、設定するには、カスタム コードを記述する必要があります。 ただし、そのカスタム コードは、POS と CRT 間で自動的に送信されます。</p>
<p>たとえば、POS の顧客エンティティーにいくつかの追加情報をキャプチャして表示したいとします。 この場合、顧客に対するすべてのカスタム プロパティをフェッチするポスト トリガーを追加し、拡張子プロパティとして顧客エンティティに追加し、それらの拡張機能プロパティを POS に送信できます。</p>
<p>POS から CRT に拡張機能のプロパティを送信して、カスタム テーブルに保存できます。 または、これらのプロパティに基づくいくつかのカスタム ロジックの実行または本社への送信が可能です。</p>
<p>製品、顧客、トランザクション、およびパラメーターなどのすべての CRT エンティティは、拡張機能プロパティをサポートします。</p>
<blockquote>[!NOTE]<br>
属性もまたサポートされます (コンフィギュレーション駆動型の開発)。 拡張プロパティの場合は、カスタム テーブルを作成し、データを格納する必要があります。 ただし、属性はコンフィギュレーション駆動型であり、テーブル フィールドを作成するために必須ではありません。 したがって、読み取りおよび更新操作にコードは必要ありません。</blockquote>
<p>属性についての詳細は、次のトピックを参照してください。</p>
<ul>
<li><a href="https://docs.microsoft.com/dynamics365/unified-operations/retail/dev-itpro/order-attributes">注文属性</a></li>
<li><a href="https://docs.microsoft.com/dynamics365/unified-operations/retail/dev-itpro/customer-attributes">顧客属性</a></li>
</ul>
</td>
</tr>
<tr>
<td>リアルタイム トランザクション サービスの呼び出し</td>
<td>CRT から HQ の同期呼び出しを行うことができます。</td>
</tr>
<tr>
<td>CRT データ サービス、およびエンティティ付きデータ サービス</td>
<td>チャネル データベース データ アクセスの特殊なデータ サービスおよび Retail サーバー エクスポージャのエンティティ。</td>
</tr>
</tbody>
</table>

**5 月の更新プログラム以降で、7.1 の CRT 拡張を手動で展開**

CRT を拡張すると、オンラインの **…\\RetailServer\\webroot\\bin\\Ext** フォルダーにカスタム ライブラリを配置します (POS が Retail サーバーに接続された場合)。 **CommerceRuntime.Ext.config** ファイル内で、ここに示すカスタム ライブラリ情報を使用して**構成**セクションを更新する必要があります。

```C#
<add source="assembly" value="your custom library name" />
```

たとえば、カスタム ライブラリの名前が **Contoso.Commerce.Runtime.CustomerSearchSample** の場合、**構成**セクションに次の行を追加します。

```C#
<add source="assembly" value="Contoso.Commerce.Runtime.CustomerSearchSample" />
```

オフラインの場合は、カスタム ライブラリを **…\\Program Files (x86)\\Microsoft Dynamics 365\\70\\Retail Modern POS\\ClientBroker\\ext** フォルダーに配置する必要があります。 **CommerceRuntime.MPOSOffline.ext.config** ファイル内で、ここに示すカスタム ライブラリ情報を使用して**構成**セクションを更新する必要があります。

```C#
<add source="assembly" value="your custom library name" />.
```

上記の手順は、手動による展開および開発ボックスでのテストのために使用されます。 拡張機能をパッケージ化し、生産またはユーザー受け入れテスト (UAT) に配置するには、パッケージ ドキュメントの情報を使用します。

**デバッグ CRT**

POS から CRT をデバッグするには、CRT 拡張機能プロジェクトを、オンラインの **w3wp.exe (Retail サーバーの IIS プロセス)** プロセス (POS が CRT に接続されている場合) に関連付ける必要があります。 オフラインの場合は、**dllhost.exe** プロセスに CRT 拡張プロジェクトを関連付けます。

**CRT エンティティ、依頼および応答での拡張機能プロパティの使用**

既存の CRT エンティティに新しいデータを追加する 1 つの方法は、拡張プロパティを使用することです。 拡張プロパティは、エンティティのキーと値のペアです。 既定では、これらのキーと値のペアはデータベースで保持されません。 拡張プロパティを保持するためには、カスタム コードを記述する必要があります。

**CRT エンティティでの機能拡張プロパティの永続的な使用**

エンティティに追加する任意の拡張プロパティは、シナリオしだいでオブジェクトまたはトランザクションのいずれかの有効期間の POS および CRT メモリに保持されます。 拡張プロパティは、アプリケーションの境界にもまたがって移動します。 たとえば、Retail Modern POS に拡張プロパティを追加し、Retail サーバー/CRT を呼び出すと、キーと値のペアがそのフロー全体でも使用できます。 また、そのエンティティが Commerce Data Exchange: Real-time Service を呼び出し中に送信されると、キーと値のペアは処理中に使用できます。

> [!NOTE]
> HQ では、拡張プロパティは顧客と注文に対してのみ送信されます。

ただし、既述のように、拡張プロパティは既定では保持されていません。 拡張プロパティを保持する場合は、データ モデリングを実行して、データの格納場所を適切に設計することを保証する必要があります。 新しいテーブルと結合を使用することをお勧めします。 この方法は、ほとんどの要件に適合します。 Retail SDK の EmailPreference サンプルは、代表的なエンド ツー エンドの例を提供します。

**Retail SDK のサンプル コードの場所**

…\\RetailSDK\\SampleExtensions\\CommerceRuntime\\Extensions.EmailPreferenceSample

**スクリプトの場所**

…\\RetailSDK\\ドキュメント\\SampleExtensionsInstructions\\EmailPreference

**エンティティに拡張子プロパティを設定する構文**

```C#
public virtual void SetProperty(string key, object value);
entity.SetProperty("key", value);
```

**例**

**シナリオ**

小売パラメーターに新しい拡張テーブルを作成しました。 その拡張テーブルからフィールドを読み取り、それを POS に送信したいとします。

小売チャネルのデータベースを拡張する場合は、メイン テーブルと拡張テーブルの間に主キーの関係を置くことをお勧めします。 その後、主キーを使用して拡張テーブルからデータを読み取ることができます。

**ステップ**

1. メイン テーブルに主キーの関係があるチャネル テーブル内の、Retail パラメータの拡張テーブルを作成します。 (この場合、メイン テーブルは小売共有パラメーターです。)
2. 小売パラメーターを読み取る CRT データ要求を識別します。
3. データ要求の転記トリガーを追加します。 共有パラメータ テーブルの主キーを使用して、小売共有パラメータの拡張テーブルを照会し、カスタム フィールドを読み取ることができます。

    > [!NOTE]
    > ポスト トリガー要求でエンティティの主キーを取得できます。 エンティティ オブジェクトを持つその要求、およびすべての必須フィールドを持つそのエンティティ オブジェクト。

4. カスタム フィールドを拡張プロパティとして、CRT 転記トリガーの共有パラメーター エンティティへ追加し、POS へ送信します。

**トリガーの拡張機能プロパティの読み取り**

小売パラメータ テーブルからデータを読み込む要求は、GetChannelConfigurationDataRequest です。 次の例では、この要求のポスト トリガーを追加する方法を示します。

```C#
/**
* SAMPLE CODE NOTICE
*
* THIS SAMPLE CODE IS MADE AVAILABLE AS IS. MICROSOFT MAKES NO WARRANTIES, WHETHER EXPRESS OR IMPLIED,
* OF FITNESS FOR A PARTICULAR PURPOSE, OF ACCURACY OR COMPLETENESS OF RESPONSES, OF RESULTS, OR CONDITIONS OF MERCHANTABILITY.
* THE ENTIRE RISK OF THE USE OR THE RESULTS FROM THE USE OF THIS SAMPLE CODE REMAINS WITH THE USER.
* NO TECHNICAL SUPPORT IS PROVIDED. YOU MAY NOT DISTRIBUTE THIS CODE UNLESS YOU HAVE A LICENSE AGREEMENT WITH MICROSOFT THAT ALLOWS YOU TO DO SO.
*/

namespace Contoso
{
    namespace Commerce.Runtime.EmailPreferenceSample
    {
        using System;
        using System.Collections.Generic;
        using Microsoft.Dynamics.Commerce.Runtime;
        using Microsoft.Dynamics.Commerce.Runtime.Data;
        using Microsoft.Dynamics.Commerce.Runtime.DataModel;
        using Microsoft.Dynamics.Commerce.Runtime.DataServices.Messages;
        using Microsoft.Dynamics.Commerce.Runtime.DataServices.SqlServer;
        using Microsoft.Dynamics.Commerce.Runtime.Messages;

        /// <summary>
        /// Class that implements a post trigger for the GetChannelConfigurationDataRequest request type.
        /// </summary>

        public class GetChannelConfigurationDataRequestTriggers : IRequestTrigger
        {
            /// <summary>
            /// Gets the supported requests for this trigger.
            /// </summary>

            public IEnumerable<Type> SupportedRequestTypes
            {
                get
                {
                    return new[] { typeof(GetChannelConfigurationDataRequest) };
                }
            }

            /// <summary>
            /// Post trigger code to retrieve extension properties.
            /// </summary>
            /// <param name="request">The request.</param>
            /// <param name="response">The response.</param>

            public void OnExecuted(Request request, Response response)
            {
                ThrowIf.Null(request, "request");
                ThrowIf.Null(response, "response");
                var channelConfiguration = ((SingleEntityDataServiceResponse<ChannelConfiguration>)response).Entity;
                if (channelConfiguration == null)
                {
                    return;
                }
                var query = new SqlPagedQuery(QueryResultSettings.SingleRecord)
                {
                    DatabaseSchema = "ext",
                    Select = new ColumnSet(new string[] { "CUSTOMFIELD" }),
                    From = "PARAMETERSEXTENSIONVIEW", // Create your own view to read the data from the parameter extension table by passing the primary key from the entity (in this case its Rec ID)
                    Where = "PARAMETERSRECID = @RecId AND DATAAREAID = @dataAreaId" //This query assumes I have PARAMETERSRECID, DATAAREAID and CUSTOMFIELD as new fields in the extension tables.
                };
                query.Parameters["@RecId"] = channelConfiguration.RetailParametersRecId;
                query.Parameters["@dataAreaId"] = request.RequestContext.GetChannelConfiguration().InventLocationDataAreaId;
                using (var databaseContext = new SqlServerDatabaseContext(request))
                {
                    ExtensionsEntity extensions = databaseContext.ReadEntity<ExtensionsEntity>(query).FirstOrDefault();
                    var customField = extensions != null ? extensions.GetProperty("customField") : null;
                    if (customField != null)
                    {
                        **channelConfiguration.SetProperty("CUSTOMFIELD", customField);**
                    }
                }
            }

            /// <summary>
            /// Pre trigger code.
            /// </summary>
            /// <param name="request">The request.</param>

            public void OnExecuting(Request request)
            {
            }
        }
    }
}
```

> [!NOTE]
> 新しいフィールドとテーブル、または使用している条件に基づいて、このクエリを変更する必要があります。 テーブルをデザインするときは、CRT エンティティを使用してクエリできるように、親テーブルの主キー フィールドがあることを確認します。 ほとんどの CRT エンティティには、**RecId** フィールドまたはレコードを選択するために使用される関連する別の固有フィールドなどの主キー フィールドがある必要があります。

**ハンドラーを上書きすることによる拡張プロパティの設定**

**シナリオ**

顧客用に新しい拡張テーブルを作成しました。 顧客の拡張フィールドの値が POS または CRT から来た場合は、その値をカスタム テーブルに格納します。

> [!NOTE]
> 拡張のプロパティはトリガーで、またはハンドラーを上書きすることによって設定することができます。 拡張テーブルから読み込んで拡張プロパティを設定しただけの場合、トリガーを使用することができます。

**ステップ**

1. メイン テーブルに主キーの関係があるチャネル テーブル内の、顧客の拡張テーブルを作成します。 (この場合、メイン テーブルは CustTable です。)
2. CustTable にデータを設定する CRT データ要求を識別します。
3. ハンドラを上書きし、メイン テーブル (CustTable) で値を設定する基本要求を呼び出してからテーブルを拡張します。

> [!NOTE]
> 拡張手順またはビューに必要な追加のプロパティを送信できます。

次の例では、使用される SQL スクリプトがありません。 完全なサンプル コードとスクリプトは、Retail SDK の次の場所にあります。

**Retail SDK のサンプル コードの場所**

…\\RetailSDK\\SampleExtensions\\CommerceRuntime\\Extensions.EmailPreferenceSample

**スクリプトの場所**

…\\RetailSDK\\ドキュメント\\SampleExtensionsInstructions\\EmailPreference

**例**

```C#
/**
* SAMPLE CODE NOTICE
*
* THIS SAMPLE CODE IS MADE AVAILABLE AS IS. MICROSOFT MAKES NO WARRANTIES, WHETHER EXPRESS OR IMPLIED,
* OF FITNESS FOR A PARTICULAR PURPOSE, OF ACCURACY OR COMPLETENESS OF RESPONSES, OF RESULTS, OR CONDITIONS OF MERCHANTABILITY.
* THE ENTIRE RISK OF THE USE OR THE RESULTS FROM THE USE OF THIS SAMPLE CODE REMAINS WITH THE USER.
* NO TECHNICAL SUPPORT IS PROVIDED. YOU MAY NOT DISTRIBUTE THIS CODE UNLESS YOU HAVE A LICENSE AGREEMENT WITH MICROSOFT THAT ALLOWS YOU TO DO SO.
*/

namespace Contoso
{
    namespace Commerce.Runtime.EmailPreferenceSample
    {
        using System.Transactions;
        using Microsoft.Dynamics.Commerce.Runtime;
        using Microsoft.Dynamics.Commerce.Runtime.Data.Types;
        using Microsoft.Dynamics.Commerce.Runtime.DataModel;
        using Microsoft.Dynamics.Commerce.Runtime.DataServices.Messages;
        using Microsoft.Dynamics.Commerce.Runtime.DataServices.SqlServer;

        /// <summary>
        /// Create or update customer data request handler.
        /// </summary>

        public sealed class CreateOrUpdateCustomerDataRequestHandler : SingleRequestHandler<CreateOrUpdateCustomerDataRequest, SingleEntityDataServiceResponse<Customer>>
        {
            /// <summary>
            /// Executes the workflow to create or update a customer.
            /// </summary>
            /// <param name="request">The request.</param>
            /// <returns>The response.</returns>

            protected override SingleEntityDataServiceResponse<Customer> Process(CreateOrUpdateCustomerDataRequest request)
            {
                ThrowIf.Null(request, "request");
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
                        databaseContext.ExecuteStoredProcedureNonQuery("[ext].UPDATECUSTOMEREXTENSIONPROPERTIES", parameters);
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

### <a name="using-extension-properties-on-crt-request-and-response-types"></a>CRT 要求タイプおよび応答タイプでの拡張機能プロパティの使用

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

```Typescript
let sampleExtensionProperty = <ProxyEntities.CommerceProperty>{
    Key: "sampleExtensionProperty",
    Value: <ProxyEntities.CommercePropertyValue>{
        BooleanValue: false
    }
};
this.context.runtime.executeAsync(new SaveExtensionPropertiesOnCartClientRequest([sampleExtensionProperty]));
```

**POS のカートから拡張プロパティの読み取り**

```Typescript
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

### <a name="implementing-a-new-crt-service-that-handles-multiple-new-requests"></a>複数の新しい要求を処理する新しい CRT サービスの実装

新しい CRT サービスを実装することが一般的です。 最初に、新しい要求および応答クラスを作成する必要があります。

#### <a name="creating-the-request-and-response-classes"></a>要求および応答クラスを作成しています

作業のシリアル化については、新しい要求タイプは **\[DataContract\]** および **\[DataMember\]** 属性を実装する必要があります。

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

新しい応答タイプは要求タイプに似ています。

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

次に、要求および応答タイプを使用する新しい CRT サービスを作成する必要があります。

#### <a name="creating-a-new-crt-service"></a>新しい CRT サービス注文を作成しています

1.  新しいサービスを実装します。

        public class StoreHoursDataService : IRequestHandler

2.  インターフェイスのメンバー 2 つを実装します。 **SupportedRequestTypes** メンバーは、このサービスが処理できるすべての要求の一覧を返します。 実行メソッドは、このサービスの要求が実行された場合に CRT が呼び出すメソッドです。

        public IEnumerable SupportedRequestTypes
        {
            get
            {
                return new[]
                {
                typeof(GetStoreHoursDataRequest),
                };
            }
        }

        public Response Execute(Request request);

3.  CommerceRuntime.Config ファイルで、**合成**セクション (または同等のセクション) を更新してこのサービスを登録します。 アセンブリから 1 つの型またはすべての型を登録できることに注意してください。 CommerceRuntime エンジンは、すべての IRequestHandler 派生タイプを見つけます。
4.  オプション: CommerceRuntime テスト ホストを使用してサービスのテストを行います。

### <a name="implementing-a-new-crt-service-that-handles-a-single-new-request"></a>1 つの新しい要求を処理する新しい CRT サービスの実装

単一の要求サービスを作成すると少し便利になります。

    public class CrossLoyaltyCardService : SingleRequestHandler

前の手順で説明したように登録が行われます。

### <a name="implementing-a-new-crt-service-that-overrides-the-functionality-of-an-existing-request"></a>既存の要求の機能をオーバーライドする新しい CRT サービスの実装

場合によっては、要求および応答タイプは十分ですが、サービスの実装を変更する必要があります。 新しいデータを送信する必要がある場合は、拡張機能のプロパティを使用してエンティティ、要求、または応答オブジェクトを拡張することもします。 このシナリオでは、前述のようにサービスを作成して既存の IRequestHandler 型を使用できます。 また、commerceRuntime.Config ファイルの登録は、上書きすべきサービスの登録より前にする必要があります。 この登録順序は、Managed Extensibility Framework (MEF) が拡張ダイナミック リンク ライブラリ (DLL) を読み込む方法のために重要です。 ファイルより高いタイプが優先されます。

### <a name="implementing-a-new-crt-entity-and-using-it-in-new-crt-service"></a>新しい CRT エンティティの実装および新しい CRT サービスでの使用

すべての新しいエンティティは、**CommerceEntity** タイプであることが必要です。 このタイプを使用するとき、多くの低レベルの機能は自動的に処理されます。 次の例は、StoreHours サンプルから取得したもので、データベース テーブルにバインドされたエンティティを作成する方法を示しています。 これは、通常のケースです。

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

サービスで新しいエンティティを使用する場合、プロセスは簡単です。 前述のように、派生 IRequestHandler として新しいサービスを作成します。 次に、新しいエンティティを使用するか返すかのいずれかを実行します。 次の例は、データベースからエンティティを読み取り、それを応答の一部として返す方法を示しています。

    private GetStoreHoursDataResponse GetStoreDayHours(GetStoreHoursDataRequest request)
    {
        ThrowIf.Null(request, "request");
        using (DatabaseContext databaseContext = new DatabaseContext(request.RequestContext))
        {
            var query = new SqlPagedQuery(request.QueryResultSettings)
            {
                DatabaseSchema = "crt",
                Select = new ColumnSet("DAY", "OPENTIME", "CLOSINGTIME", "RECID"),
                From = "ISVRETAILSTOREHOURSVIEW",
                Where = "STORENUMBER = @storeNumber",
            };

            query.Parameters["@storeNumber"] = request.StoreNumber;
            return new GetStoreHoursDataResponse(databaseContext.ReadEntity(query));
        }
    }

前の例では、CRT ランタイム エンジンは、登録されているデータ アダプターを介してチャンネルに自動的にクエリを作成します。 名前 **crt.ISVRetailStoreHoursView** を持つ型を照会して、コードで指定された **where** 句および列を生成します。 カスタマイザーは、カスタマイズの一部として SQL オブジェクトを提供する役割を担います。

### <a name="adding-pre-triggers-and-post-triggers-for-a-specific-request"></a>特定の要求のプレトリガーとポストトリガーの追加

場合によっては、要求の前後で必要になる処理もあります。 追加のコードを実行するために使用できる 2 つのフックがあります。 これらのフックはプレトリガーおよびポストトリガーと呼ばれます。 新しいトリガーを作成して要求に関連付けるには、これらの手順に従います。

1.  IRequestTrigger を実装する新しいトリガー クラスを作成します。

        public class GetCrossLoyaltyCardRequestTrigger : IRequestTrigger

2.  **IRequest.SupportedRequestTypes** プロパティで、このトリガーを実行する必要がある要求の一覧を返します。

        public IEnumerable SupportedRequestTypes
        {
            get
            {
                return new[] { typeof(GetCrossLoyaltyCardRequest) };
            }
        }

3.  要求の前後に呼び出される関数を実装します。

        void OnExecuted(Request request, Response response);
        void OnExecuting(Request request);

4.  commerceRuntime.Config ファイルでクラスを登録します。

## <a name="retail-server-extensibility-scenarios"></a>Retail サーバーの拡張機能シナリオ
### <a name="adding-a-new-odata-action-to-an-existing-controller"></a>既存のコントローラーへの新しい ODATA アクションの追加

最も簡単なシナリオでは、わずかに異なるユース ケースのために新しいアプリケーション プログラミング インターフェイス (API) を追加する必要があります。 このシナリオを機能させるには、継承によって新しいアクションを追加します。 Retail サーバーへの API の任意の変更については、次の手順を実行する必要があります。

1.  新しいアクションまたはコントローラーを実装します。
2.  新しい対応するメタデータを追加するためのモデル出荷時の要件を上書きします。

次の例は、Retail SDK から取得したもので、既存のコントローラーを拡張して POST アクションを持つようにする方法を示しています。

    public class MyCustomersController : CustomersController
    {
        [HttpPost]
        [CommerceAuthorization(AllowedRetailRoles = new string[] { CommerceRoles.Customer, CommerceRoles.Employee })]
        public decimal GetCrossLoyaltyCardDiscountAction(ODataActionParameters parameters)
        {
            if (parameters == null)
            {
                throw new ArgumentNullException("parameters");
            }

            var runtime = CommerceRuntimeManager.CreateRuntime(this.CommercePrincipal);
            string loyaltyCardNumber = (string)parameters["LoyaltyCardNumber"];

            GetCrossLoyaltyCardResponse resp = runtime.Execute(new GetCrossLoyaltyCardRequest(loyaltyCardNumber), null);

            string logMessage = "GetCrossLoyaltyCardAction successfully handled with card number '{0}'. Returned discount '{1}'.";
            RetailLogger.Log.ExtendedInformationalEvent(logMessage, loyaltyCardNumber, resp.Discount.ToString());
            return resp.Discount;
        }
    }

次に、モデル ファクトリをオーバーライドします。

    [Export(typeof(IEdmModelFactory))]
    [ComVisible(false)]
    public class CustomizedEdmModelFactory : CommerceModelFactory
    {
        protected override void BuildActions()
        {
            base.BuildActions();
            var var1 = CommerceModelFactory.BindEntitySetAction("GetCrossLoyaltyCardDiscountAction");
            var1.Parameter("LoyaltyCardNumber");
            var1.Returns();
        }
    }

クライアントがこの新しいカスタマイズを使用する前に、新しいモデル ファクトリ用の Retail サーバー プロキシ コードを生成するためにビルド システムを調整する必要があります。 この構成ステップはビルド システムで実行されます。 最後に、web.config ファイルを調整する必要があります。 SDK の Retail サーバーの梱包プロジェクトでは、このステップを完了する必要があります。 ローカルのテストが行われている場合、テストに使用されるローカル開発トポロジー コンピューターでこの手順を任意で実行できます。

### <a name="adding-a-new-simple-controller-for-an-entity"></a>エンティティの新しい簡単なコントローラーの追加

単純なエンティティがあり、データをフェッチするコント ローラーを必要としているとします。 例については、Retail SDK で StoreHours サンプルを参照してください。 新しい Retail サーバー コントローラーには意味があり、低レベルのすべての作業が CRT (新しいエンティティ、要求、応答、およびサービス) で実行されます。 新しいコントローラを作成するには、CommerceController から派生します。 例としてここに表示します。 コントローラー名は重要であり、エンティティの名前と一致する必要があります。

    [ComVisible(false)]
    public class StoreHoursController : CommerceController
    {
        public override string ControllerName
        {
            get { return "StoreHours"; }
        }

        [HttpPost]
        [CommerceAuthorization(AllowedRetailRoles = new string[] { CommerceRoles.Anonymous, CommerceRoles.Customer, CommerceRoles.Device, CommerceRoles.Employee })]
        public System.Web.OData.PageResult GetStoreDaysByStore(ODataActionParameters parameters)
        {
            if (parameters == null)
            {
                throw new ArgumentNullException("parameters");
            }

            var runtime = CommerceRuntimeManager.CreateRuntime(this.CommercePrincipal);

            QueryResultSettings queryResultSettings = QueryResultSettings.SingleRecord;
            queryResultSettings.Paging = new PagingInfo(10);

            var request = new GetStoreHoursDataRequest((string)parameters["StoreNumber"]) { QueryResultSettings = queryResultSettings };
            PagedResult hours = runtime.Execute(request, null).DayHours;
            return this.ProcessPagedResults(hours);
        }
    }

新しいエンティティについては、次の例に示すように、工場の **BuildEntitySets()** メソッドを上書きする必要があります。

    [Export(typeof(IEdmModelFactory))]
    [ComVisible(false)]
    public class CustomizedEdmModelFactory : CommerceModelFactory
    {
        protected override void BuildActions()
        {
            base.BuildActions();
            var action = CommerceModelFactory.BindEntitySetAction("GetStoreDaysByStore");
            action.Parameter("StoreNumber");
            action.ReturnsCollectionFromEntitySet("StoreHours");
        }

        protected override void BuildEntitySets()
        {
            base.BuildEntitySets();
            CommerceModelFactory.BuildEntitySet("StoreHours");
        }
    }

### <a name="how-to-call-the-new-retail-server-api-from-mposcloud-pos"></a>MPOS/クラウド POS から新しい小売サーバー API を呼び出す方法:

新しい小売サーバー API を呼び出す前に、以下の手順を実行してください。

1.  Retail サーバー web.config ファイルで新しい Retail サーバー拡張子を登録します: &lt;ソースの追加 =「アセンブリ」値 ="**アセンブリ名**" /&gt; は、extensionComposition セクションの下にあります。
2.  Customization.settings ファイルの新しい Retail サーバー拡張子を追加します。 このファイルは、RetailSdk\\BuildTools&lt;RetailServerLibraryPathForProxyGeneration Condition="'$(RetailServerLibraryPathForProxyGeneration)' == ''"&gt;$(SdkReferencesPath)\\**Your assembly name.dll**&lt;/RetailServerLibraryPathForProxyGeneration&gt; &lt;/PropertyGroup&gt; に存在します。
3.  CRT と Retail サーバー拡張子 dlls の両方を **…\\RetailServer\\webroot\\bin\\Ext** フォルダーに移動します。 新しい小売サーバー API に関連する CRT 拡張機能をご使用の場合、**…\\RetailServer\\webroot\\bin\\Ext** フォルダー内の CommerceRuntime.Ext.config ファイルの情報を更新してください。
4.  &lt;ソースの追加 = 「アセンブリ」値 = "**アセンブリ名**" /&gt;
5.  inetmgr を使用して小売サーバーのメタデータを参照し、エンティティが xml で公開されているかどうかを確認します。
6.  mpos/クラウド POSをコンパイルしてビルドし、プロキシを再生成します。 コンパイラ中に、mpos は小売サーバーのメタデータで定義されたすべてのエンティティを再生成します。これにより、以下のようなコマース コンテキストを使用して新しいエンティティを呼び出すことができます。

> [!NOTE]
> Retail サーバー web.config ファイルまたは Retail サーバー フォルダ内で何も変更または追加しないでください。拡張合成セクションは除外され、おそらく bin\ext フォルダにカスタム アセンブリがコピーされます。 配置時に web.config ファイル内の extensionComposition セクションのみマージされ、他のセクションはすべて上書きされ、**...\\RetailServer\\webroot\\bin\\Ext** フォルダのアセンブリのみが他のアセンブリとマージされます。 このファイルは、最新バイナリ パッケージに基づいて上書きされます。 カスタム アプリケーションの設定を追加、または、変更するのに Retail サーバー web.config ファイルは使用しません。

#### <a name="cross-loyalty-sample"></a>クロス ロイヤルティ サンプル。

    var request: Commerce.Proxy.Common.IDataServiceRequest = this._context.customers().getCrossLoyaltyCardDiscountAction(loyaltyCardNumber);
    return request.execute<number>();

#### <a name="store-hours-sample"></a>店舗の時間のサンプル:

    var request: Commerce.Proxy.Common.IDataServiceRequest = this._context.storeHours().getStoreDaysByStore(storeId);
    return request.execute<Commerce.Proxy.Entities.StoreDayHours[]>();

mpos で新しい小売サーバー API を呼び出す方法について詳しくは、小売 SDK POS.Extension.CrossloaylySample および POS.Extension.SToreHoursSample サンプル プロジェクトをご覧ください。
