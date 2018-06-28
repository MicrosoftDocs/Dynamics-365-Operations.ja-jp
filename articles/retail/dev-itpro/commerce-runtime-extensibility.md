---
title: "Commerce Runtime および Retail サーバーの拡張機能"
description: "この記事では、コマース ランタイム (CRT) と Retail サーバーを拡張するさまざまな方法について説明します。 拡張機能プロパティのコンセプトを説明し、保持有無にかかわらず CRT エンティティに追加する方法について説明します。 また、アクションを Retail サーバー コントローラーに追加して、エンティティのコントローラーを追加する方法も示します。"
author: mugunthanm
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
audience: Developer
ms.reviewer: robinr
ms.search.scope: Operations, Retail
ms.custom: 104593
ms.assetid: 1397e679-8cd5-49f3-859a-83d342fdd275
ms.search.region: Global
ms.author: mumani
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: 879eb9f2a63a8514791f74965005ed3e22bc0de7
ms.openlocfilehash: d02d1d7db31ac3cd5a141d410439a925239f2701
ms.contentlocale: ja-jp
ms.lasthandoff: 04/20/2018

---

# <a name="commerce-runtime-and-retail-server-extensibility"></a>Commerce Runtime および Retail サーバーの拡張機能

[!include [banner](../includes/banner.md)]

この記事では、コマース ランタイム (CRT) と Retail サーバーを拡張するさまざまな方法について説明します。 拡張機能プロパティのコンセプトを説明し、保持有無にかかわらず CRT エンティティに追加する方法について説明します。 また、アクションを Retail サーバー コントローラーに追加して、エンティティのコントローラーを追加する方法も示します。

<a name="using-extension-properties-on-crt-entities"></a>CRT エンティティでの機能拡張プロパティの使用
------------------------------------------

既存の Commerce Runtime (CRT) エンティティに新しいデータを追加する 1 つの方法は、拡張プロパティを使用することです。 拡張プロパティは、エンティティのキーと値のペアです。 既定では、これらのキーと値のペアはデータベースに保持されません。 拡張プロパテーは、エンティティを拡張する最も簡単な方法と言えます。 使用できない理由がある場合を除いて、いつも最初にこのパターンを使用する必要があります。 ポリモーフィズム/継承を使用して単純なデータ メンバーをエンティティに追加することができますが、この方法は通常、解決するよりも多くの問題を引き起こします。 (しかし、特定のケースではこの方法が必要な場合があります。) 拡張プロパティを追加するには、この構文を使用する必要があります。

    entity.SetProperty("EXTENSION_PROPERTY_ADDED", true);

後でこのプロパティを読み取るには、この構文を使用します。

    bool? property = (bool?)entity.GetProperty("EXTENSION_PROPERTY_ADDED");

## <a name="using-extension-properties-on-crt-entities-with-persistence"></a>CRT エンティティでの機能拡張プロパティの永続的な使用
エンティティに追加する拡張プロパティは、オブジェクトの有効期間はメモリ内に保持されます。 さらに、拡張プロパティは、アプリケーションの境界にまたがって移動します。 たとえば、Retail Modern POS で拡張プロパティを追加し、Retail サーバー/CRT を呼び出すと、キーと値のペアがそのプロセスでも使用できます。 また、そのエンティティが Commerce Data Exchange 中に送信される場合: Real-time Service (RTS) を呼び出す、キーと値のペアは処理中でも使用可能です。 ただし、先に述べたように、既定では保持されていません。 

拡張プロパティを保持する必要がある場合は、データ モデリングを実行して、データの格納場所を適切に設計することを保証する必要があります。 新しい列を同じテーブルで使用、新しいテーブルおよび結合を使用、または他の方法を使用することができます。 推奨されるアプローチは、新しいテーブルを使用して結合することです。 この方法は、ほとんどの要件に適合します。 このアプローチでは、カスタマイザーは、すべての「書き込み」の発生および SQL コード (ストアド プロシージャ) の更新について精通する必要があり、 すべての「読み取り」の発生およびその SQL コード (SQL ビュー) の更新についても精通する必要があります。 EmailPreference サンプルは、代表的なエンド ツー エンドの例を提供します。 このサンプルでは、1 つの SQL ビューと 1 つの SQL ストアド プロシージャがカスタマイズにより変更されます。 

新しい SQL オブジェクトに適切なロールのアクセス許可を付与する必要があることに注意することが重要です。 たとえば、Commerce データ交換 (CDX) 同期ジョブに含められるべき新しいテーブルは、DataSyncUsersRole によってアクセスを許可される必要があります。 使用可能なその他のロールについては、Retail sdk\\データベース フォルダーで主要な SQL スクリプトを検査します。

    IF (SELECT OBJECT_ID('ax.RETAILCUSTPREFERENCE')) IS NULL 
    BEGIN
        CREATE TABLE [ax].[RETAILCUSTPREFERENCE](
        // removed . . . 
        ) ON [PRIMARY]
        // removed . . . 
    END
    GO

    -- grant Read/Insert/Update/Delete permission to DataSyncUserRole so CDX can function
    GRANT SELECT ON OBJECT::[ax].[RETAILCUSTPREFERENCE] TO [DataSyncUsersRole]
    GO
    GRANT INSERT ON OBJECT::[ax].[RETAILCUSTPREFERENCE] TO [DataSyncUsersRole]
    GO
    GRANT UPDATE ON OBJECT::[ax].[RETAILCUSTPREFERENCE] TO [DataSyncUsersRole]
    GO
    GRANT DELETE ON OBJECT::[ax].[RETAILCUSTPREFERENCE] TO [DataSyncUsersRole]
    GO

最後に、Retail ソフトウェアの開発キット (SDK) の Customization.settings ファイルで、カスタマイズ用の SQL 更新スクリプトを登録する必要があります。

### <a name="using-extension-properties-on-crt-request-and-response-types"></a>CRT 要求タイプおよび応答タイプでの拡張機能プロパティの使用

エンティティと同様に、要求および応答タイプを拡張することができます。

    request.SetProperty("BoolPropertyName", true);
    response.SetProperty("BoolPropertyName2", true);

    bool? BoolPropertyName = (bool?)request.GetProperty("BoolPropertyName");
    bool? BoolPropertyName2 = (bool?)response.GetProperty("BoolPropertyName2");

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

1.  Retail サーバー web.config ファイルで新しい Retail サーバー拡張を登録します:  &lt;add source="assembly" value="**Your assembly name**" /&gt;
2.  Customization.settings ファイルの新しい Retail サーバー拡張子を追加します。 このファイルは RetailSdk\\BuildTools&lt;RetailServerLibraryPathForProxyGeneration Condition="'$(RetailServerLibraryPathForProxyGeneration)' == ''"&gt;$(SdkReferencesPath)\\**Your assembly name.dll**&lt;/RetailServerLibraryPathForProxyGeneration&gt; &lt;/PropertyGroup&gt; で見つけることができます
3.  CRT および Retail サーバー拡張子 dlls の両方を小売サーバー bin フォルダーにドロップします。 新しい小売サーバー api に関連する CRT の拡張機能がある場合、小売サーバー bin フォルダーの commerceRuntime 構成ファイルにある情報をアップデートします。
4.  &lt;ソースの追加 = 「アセンブリ」値 = "**アセンブリ名**" /&gt;
5.  inetmgr を使用して小売サーバーのメタデータを参照し、エンティティが xml で公開されているかどうかを確認します。
6.  mpos/クラウド POSをコンパイルしてビルドし、プロキシを再生成します。 コンパイラ中に、mpos は小売サーバーのメタデータで定義されたすべてのエンティティを再生成します。これにより、以下のようなコマース コンテキストを使用して新しいエンティティを呼び出すことができます。

#### <a name="cross-loyalty-sample"></a>クロス ロイヤルティ サンプル。

    var request: Commerce.Proxy.Common.IDataServiceRequest = this._context.customers().getCrossLoyaltyCardDiscountAction(loyaltyCardNumber);
    return request.execute<number>();

#### <a name="store-hours-sample"></a>店舗の時間のサンプル:

    var request: Commerce.Proxy.Common.IDataServiceRequest = this._context.storeHours().getStoreDaysByStore(storeId);
    return request.execute<Commerce.Proxy.Entities.StoreDayHours[]>();

mpos で新しい小売サーバー API を呼び出す方法について詳しくは、小売 SDK POS.Extension.CrossloaylySample および POS.Extension.SToreHoursSample サンプル プロジェクトをご覧ください。




