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
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: cc98e2c6bb7c3ce33dc4710a8bceda4d6387f99d
ms.contentlocale: ja-jp
ms.lasthandoff: 05/08/2018

---

# <a name="commerce-runtime-and-retail-server-extensibility"></a><span data-ttu-id="aeac1-105">Commerce Runtime および Retail サーバーの拡張機能</span><span class="sxs-lookup"><span data-stu-id="aeac1-105">Commerce runtime and Retail Server extensibility</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="aeac1-106">この記事では、コマース ランタイム (CRT) と Retail サーバーを拡張するさまざまな方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="aeac1-106">This article describes various ways that you can extend the commerce runtime (CRT) and Retail Server.</span></span> <span data-ttu-id="aeac1-107">拡張機能プロパティのコンセプトを説明し、保持有無にかかわらず CRT エンティティに追加する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="aeac1-107">It explains the concept of extension properties, and shows how to add them to a CRT entity both with and without persistence.</span></span> <span data-ttu-id="aeac1-108">また、アクションを Retail サーバー コントローラーに追加して、エンティティのコントローラーを追加する方法も示します。</span><span class="sxs-lookup"><span data-stu-id="aeac1-108">It also shows how to add an action to a Retail Server controller and add a controller for an entity.</span></span>

<a name="using-extension-properties-on-crt-entities"></a><span data-ttu-id="aeac1-109">CRT エンティティでの機能拡張プロパティの使用</span><span class="sxs-lookup"><span data-stu-id="aeac1-109">Using extension properties on CRT entities</span></span>
------------------------------------------

<span data-ttu-id="aeac1-110">既存の Commerce Runtime (CRT) エンティティに新しいデータを追加する 1 つの方法は、拡張プロパティを使用することです。</span><span class="sxs-lookup"><span data-stu-id="aeac1-110">One way to add new data to an existing commerce runtime (CRT) entity is to use extension properties.</span></span> <span data-ttu-id="aeac1-111">拡張プロパティは、エンティティのキーと値のペアです。</span><span class="sxs-lookup"><span data-stu-id="aeac1-111">Extension properties are key-value pairs on the entity.</span></span> <span data-ttu-id="aeac1-112">既定では、これらのキーと値のペアはデータベースに保持されません。</span><span class="sxs-lookup"><span data-stu-id="aeac1-112">By default, these key-value pairs aren't persisted into the database.</span></span> <span data-ttu-id="aeac1-113">拡張プロパテーは、エンティティを拡張する最も簡単な方法と言えます。</span><span class="sxs-lookup"><span data-stu-id="aeac1-113">Extension properties provide the easiest and, it can be argued, the most useful way to extend entities.</span></span> <span data-ttu-id="aeac1-114">使用できない理由がある場合を除いて、いつも最初にこのパターンを使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="aeac1-114">You should always try to use this pattern first, unless something prevents you from using it.</span></span> <span data-ttu-id="aeac1-115">ポリモーフィズム/継承を使用して単純なデータ メンバーをエンティティに追加することができますが、この方法は通常、解決するよりも多くの問題を引き起こします。</span><span class="sxs-lookup"><span data-stu-id="aeac1-115">Although you can use polymorphism/inheritance to add simple data members to entities, this approach usually causes more issues than it solves.</span></span> <span data-ttu-id="aeac1-116">(しかし、特定のケースではこの方法が必要な場合があります。) 拡張プロパティを追加するには、この構文を使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="aeac1-116">(Nevertheless, this approach might be required for specific cases.) To add an extension property, you must use this syntax.</span></span>

    entity.SetProperty("EXTENSION_PROPERTY_ADDED", true);

<span data-ttu-id="aeac1-117">後でこのプロパティを読み取るには、この構文を使用します。</span><span class="sxs-lookup"><span data-stu-id="aeac1-117">To enable the property to be read later, you can use this syntax.</span></span>

    bool? property = (bool?)entity.GetProperty("EXTENSION_PROPERTY_ADDED");

## <a name="using-extension-properties-on-crt-entities-with-persistence"></a><span data-ttu-id="aeac1-118">CRT エンティティでの機能拡張プロパティの永続的な使用</span><span class="sxs-lookup"><span data-stu-id="aeac1-118">Using extension properties on CRT entities with persistence</span></span>
<span data-ttu-id="aeac1-119">エンティティに追加する拡張プロパティは、オブジェクトの有効期間はメモリ内に保持されます。</span><span class="sxs-lookup"><span data-stu-id="aeac1-119">Any extension property that you add to an entity stays in memory for the lifetime of the object.</span></span> <span data-ttu-id="aeac1-120">さらに、拡張プロパティは、アプリケーションの境界にまたがって移動します。</span><span class="sxs-lookup"><span data-stu-id="aeac1-120">Additionally, the extension property travels across application boundaries.</span></span> <span data-ttu-id="aeac1-121">たとえば、Retail Modern POS で拡張プロパティを追加し、Retail サーバー/CRT を呼び出すと、キーと値のペアがそのプロセスでも使用できます。</span><span class="sxs-lookup"><span data-stu-id="aeac1-121">For example, if you add an extension property in Retail Modern POS and then call Retail Server/the CRT, the key-value pair is also available in that process.</span></span> <span data-ttu-id="aeac1-122">また、そのエンティティが Commerce Data Exchange 中に送信される場合: Real-time Service (RTS) を呼び出す、キーと値のペアは処理中でも使用可能です。</span><span class="sxs-lookup"><span data-stu-id="aeac1-122">Additionally, if that entity is sent to during a Commerce Data Exchange: Real-time Service (RTS) call, the key-value pair is also available in the process.</span></span> <span data-ttu-id="aeac1-123">ただし、先に述べたように、既定では保持されていません。</span><span class="sxs-lookup"><span data-stu-id="aeac1-123">However, as we mentioned earlier, it isn't persisted by default.</span></span> 

<span data-ttu-id="aeac1-124">拡張プロパティを保持する必要がある場合は、データ モデリングを実行して、データの格納場所を適切に設計することを保証する必要があります。</span><span class="sxs-lookup"><span data-stu-id="aeac1-124">If you must persist an extension property, you must do data modeling to help guarantee that you make the right design choices about where the data should reside.</span></span> <span data-ttu-id="aeac1-125">新しい列を同じテーブルで使用、新しいテーブルおよび結合を使用、または他の方法を使用することができます。</span><span class="sxs-lookup"><span data-stu-id="aeac1-125">You can use a new column in the same table, you can use a new table and a join, or you can use another approach.</span></span> <span data-ttu-id="aeac1-126">推奨されるアプローチは、新しいテーブルを使用して結合することです。</span><span class="sxs-lookup"><span data-stu-id="aeac1-126">The recommended approach is to use a new table and a join.</span></span> <span data-ttu-id="aeac1-127">この方法は、ほとんどの要件に適合します。</span><span class="sxs-lookup"><span data-stu-id="aeac1-127">This approach fits most requirements well.</span></span> <span data-ttu-id="aeac1-128">このアプローチでは、カスタマイザーは、すべての「書き込み」の発生および SQL コード (ストアド プロシージャ) の更新について精通する必要があり、 すべての「読み取り」の発生およびその SQL コード (SQL ビュー) の更新についても精通する必要があります。</span><span class="sxs-lookup"><span data-stu-id="aeac1-128">For this approach, the customizer must learn where all “writes” occur and update the SQL code (stored procedures), and must also learn where all the “reads” occur and update that SQL code (SQL view).</span></span> <span data-ttu-id="aeac1-129">EmailPreference サンプルは、代表的なエンド ツー エンドの例を提供します。</span><span class="sxs-lookup"><span data-stu-id="aeac1-129">The EmailPreference sample provides a good end-to-end example.</span></span> <span data-ttu-id="aeac1-130">このサンプルでは、1 つの SQL ビューと 1 つの SQL ストアド プロシージャがカスタマイズにより変更されます。</span><span class="sxs-lookup"><span data-stu-id="aeac1-130">In that sample, a single SQL view and a single SQL stored procedure are changed via customization.</span></span> 

<span data-ttu-id="aeac1-131">新しい SQL オブジェクトに適切なロールのアクセス許可を付与する必要があることに注意することが重要です。</span><span class="sxs-lookup"><span data-stu-id="aeac1-131">It's important to note that new SQL objects must have the correct role permissions granted.</span></span> <span data-ttu-id="aeac1-132">たとえば、Commerce データ交換 (CDX) 同期ジョブに含められるべき新しいテーブルは、DataSyncUsersRole によってアクセスを許可される必要があります。</span><span class="sxs-lookup"><span data-stu-id="aeac1-132">For example, a new table that must be included in Commerce Data Exchange (CDX) synchronization jobs must be granted access by DataSyncUsersRole.</span></span> <span data-ttu-id="aeac1-133">使用可能なその他のロールについては、Retail sdk\\データベース フォルダーで主要な SQL スクリプトを検査します。</span><span class="sxs-lookup"><span data-stu-id="aeac1-133">For other roles that are available, inspect the main SQL script in the Retail Sdk\\Database folder.</span></span>

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

<span data-ttu-id="aeac1-134">最後に、Retail ソフトウェアの開発キット (SDK) の Customization.settings ファイルで、カスタマイズ用の SQL 更新スクリプトを登録する必要があります。</span><span class="sxs-lookup"><span data-stu-id="aeac1-134">Finally, the SQL update script for your customization must be registered in the Customization.settings file for the Retail software development kit (SDK).</span></span>

### <a name="using-extension-properties-on-crt-request-and-response-types"></a><span data-ttu-id="aeac1-135">CRT 要求タイプおよび応答タイプでの拡張機能プロパティの使用</span><span class="sxs-lookup"><span data-stu-id="aeac1-135">Using extension properties on CRT request and response types</span></span>

<span data-ttu-id="aeac1-136">エンティティと同様に、要求および応答タイプを拡張することができます。</span><span class="sxs-lookup"><span data-stu-id="aeac1-136">Like entities, request and response types can be extended.</span></span>

    request.SetProperty("BoolPropertyName", true);
    response.SetProperty("BoolPropertyName2", true);

    bool? BoolPropertyName = (bool?)request.GetProperty("BoolPropertyName");
    bool? BoolPropertyName2 = (bool?)response.GetProperty("BoolPropertyName2");

### <a name="implementing-a-new-crt-service-that-handles-multiple-new-requests"></a><span data-ttu-id="aeac1-137">複数の新しい要求を処理する新しい CRT サービスの実装</span><span class="sxs-lookup"><span data-stu-id="aeac1-137">Implementing a new CRT service that handles multiple new requests</span></span>

<span data-ttu-id="aeac1-138">新しい CRT サービスを実装することが一般的です。</span><span class="sxs-lookup"><span data-stu-id="aeac1-138">It's a typical case to implement a new CRT service.</span></span> <span data-ttu-id="aeac1-139">最初に、新しい要求および応答クラスを作成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="aeac1-139">First, you must create new request and response classes.</span></span>

#### <a name="creating-the-request-and-response-classes"></a><span data-ttu-id="aeac1-140">要求および応答クラスを作成しています</span><span class="sxs-lookup"><span data-stu-id="aeac1-140">Creating the request and response classes</span></span>

<span data-ttu-id="aeac1-141">作業のシリアル化については、新しい要求タイプは **\[DataContract\]** および **\[DataMember\]** 属性を実装する必要があります。</span><span class="sxs-lookup"><span data-stu-id="aeac1-141">For serialization to work, the new request type must implement the **\[DataContract\]** and **\[DataMember\]** attributes.</span></span>

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

<span data-ttu-id="aeac1-142">新しい応答タイプは要求タイプに似ています。</span><span class="sxs-lookup"><span data-stu-id="aeac1-142">The new response type resembles the request type.</span></span>

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

<span data-ttu-id="aeac1-143">次に、要求および応答タイプを使用する新しい CRT サービスを作成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="aeac1-143">Next, you must create a new CRT service that uses the request and response types.</span></span>

#### <a name="creating-a-new-crt-service"></a><span data-ttu-id="aeac1-144">新しい CRT サービス注文を作成しています</span><span class="sxs-lookup"><span data-stu-id="aeac1-144">Creating a new CRT service</span></span>

1.  <span data-ttu-id="aeac1-145">新しいサービスを実装します。</span><span class="sxs-lookup"><span data-stu-id="aeac1-145">Implement the new service.</span></span>

        public class StoreHoursDataService : IRequestHandler

2.  <span data-ttu-id="aeac1-146">インターフェイスのメンバー 2 つを実装します。</span><span class="sxs-lookup"><span data-stu-id="aeac1-146">Implement two members of the interface.</span></span> <span data-ttu-id="aeac1-147">**SupportedRequestTypes** メンバーは、このサービスが処理できるすべての要求の一覧を返します。</span><span class="sxs-lookup"><span data-stu-id="aeac1-147">The **SupportedRequestTypes** member returns a list of all requests that this service can handle.</span></span> <span data-ttu-id="aeac1-148">実行メソッドは、このサービスの要求が実行された場合に CRT が呼び出すメソッドです。</span><span class="sxs-lookup"><span data-stu-id="aeac1-148">The execute method is the method that the CRT calls for you if a request for this service is run.</span></span>

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

3.  <span data-ttu-id="aeac1-149">CommerceRuntime.Config ファイルで、**合成**セクション (または同等のセクション) を更新してこのサービスを登録します。</span><span class="sxs-lookup"><span data-stu-id="aeac1-149">In the commerceRuntime.Config file, update the **composition** section (or the equivalent section) to register this service.</span></span> <span data-ttu-id="aeac1-150">アセンブリから 1 つの型またはすべての型を登録できることに注意してください。</span><span class="sxs-lookup"><span data-stu-id="aeac1-150">Note that you can register single types or all types from an assembly.</span></span> <span data-ttu-id="aeac1-151">CommerceRuntime エンジンは、すべての IRequestHandler 派生タイプを見つけます。</span><span class="sxs-lookup"><span data-stu-id="aeac1-151">The CommerceRuntime engine will find all IRequestHandler derived types.</span></span>
4.  <span data-ttu-id="aeac1-152">オプション: CommerceRuntime テスト ホストを使用してサービスのテストを行います。</span><span class="sxs-lookup"><span data-stu-id="aeac1-152">Optional: Use the CommerceRuntime Test Host to do a test run of your service.</span></span>

### <a name="implementing-a-new-crt-service-that-handles-a-single-new-request"></a><span data-ttu-id="aeac1-153">1 つの新しい要求を処理する新しい CRT サービスの実装</span><span class="sxs-lookup"><span data-stu-id="aeac1-153">Implementing a new CRT service that handles a single new request</span></span>

<span data-ttu-id="aeac1-154">単一の要求サービスを作成すると少し便利になります。</span><span class="sxs-lookup"><span data-stu-id="aeac1-154">It’s slightly easier to create a single-request service.</span></span>

    public class CrossLoyaltyCardService : SingleRequestHandler

<span data-ttu-id="aeac1-155">前の手順で説明したように登録が行われます。</span><span class="sxs-lookup"><span data-stu-id="aeac1-155">Registration is done as described in the previous procedure.</span></span>

### <a name="implementing-a-new-crt-service-that-overrides-the-functionality-of-an-existing-request"></a><span data-ttu-id="aeac1-156">既存の要求の機能をオーバーライドする新しい CRT サービスの実装</span><span class="sxs-lookup"><span data-stu-id="aeac1-156">Implementing a new CRT service that overrides the functionality of an existing request</span></span>

<span data-ttu-id="aeac1-157">場合によっては、要求および応答タイプは十分ですが、サービスの実装を変更する必要があります。</span><span class="sxs-lookup"><span data-stu-id="aeac1-157">In some cases, the request and response types are sufficient, but the service implementation must be changed.</span></span> <span data-ttu-id="aeac1-158">新しいデータを送信する必要がある場合は、拡張機能のプロパティを使用してエンティティ、要求、または応答オブジェクトを拡張することもします。</span><span class="sxs-lookup"><span data-stu-id="aeac1-158">If some new data must be transmitted, you can also extend entity, request, or response objects by using extension properties.</span></span> <span data-ttu-id="aeac1-159">このシナリオでは、前述のようにサービスを作成して既存の IRequestHandler 型を使用できます。</span><span class="sxs-lookup"><span data-stu-id="aeac1-159">In this scenario, you can create the service as described earlier and use the existing IRequestHandler types.</span></span> <span data-ttu-id="aeac1-160">また、commerceRuntime.Config ファイルの登録は、上書きすべきサービスの登録より前にする必要があります。</span><span class="sxs-lookup"><span data-stu-id="aeac1-160">Additionally, registration in the commerceRuntime.Config file must precede registration of the service that should be overridden.</span></span> <span data-ttu-id="aeac1-161">この登録順序は、Managed Extensibility Framework (MEF) が拡張ダイナミック リンク ライブラリ (DLL) を読み込む方法のために重要です。</span><span class="sxs-lookup"><span data-stu-id="aeac1-161">This registration order is important because of the way that the Managed Extensibility Framework (MEF) loads the extension dynamic-link libraries (DLLs).</span></span> <span data-ttu-id="aeac1-162">ファイルより高いタイプが優先されます。</span><span class="sxs-lookup"><span data-stu-id="aeac1-162">The types that are higher in the file win.</span></span>

### <a name="implementing-a-new-crt-entity-and-using-it-in-new-crt-service"></a><span data-ttu-id="aeac1-163">新しい CRT エンティティの実装および新しい CRT サービスでの使用</span><span class="sxs-lookup"><span data-stu-id="aeac1-163">Implementing a new CRT entity and using it in new CRT service</span></span>

<span data-ttu-id="aeac1-164">すべての新しいエンティティは、**CommerceEntity** タイプであることが必要です。</span><span class="sxs-lookup"><span data-stu-id="aeac1-164">Any new entity must be of the **CommerceEntity** type.</span></span> <span data-ttu-id="aeac1-165">このタイプを使用するとき、多くの低レベルの機能は自動的に処理されます。</span><span class="sxs-lookup"><span data-stu-id="aeac1-165">When you use this type, lots of low-level functionality is automatically handled for you.</span></span> <span data-ttu-id="aeac1-166">次の例は、StoreHours サンプルから取得したもので、データベース テーブルにバインドされたエンティティを作成する方法を示しています。</span><span class="sxs-lookup"><span data-stu-id="aeac1-166">The following example, which is taken from the StoreHours sample, shows how to create an entity that is bound to the database table.</span></span> <span data-ttu-id="aeac1-167">これは、通常のケースです。</span><span class="sxs-lookup"><span data-stu-id="aeac1-167">This is the usual case.</span></span>

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

<span data-ttu-id="aeac1-168">サービスで新しいエンティティを使用する場合、プロセスは簡単です。</span><span class="sxs-lookup"><span data-stu-id="aeac1-168">When you want to use the new entity in a service, the process is straightforward.</span></span> <span data-ttu-id="aeac1-169">前述のように、派生 IRequestHandler として新しいサービスを作成します。</span><span class="sxs-lookup"><span data-stu-id="aeac1-169">As described earlier, you create a new service as a derived IRequestHandler.</span></span> <span data-ttu-id="aeac1-170">次に、新しいエンティティを使用するか返すかのいずれかを実行します。</span><span class="sxs-lookup"><span data-stu-id="aeac1-170">Then either use or return the new entity.</span></span> <span data-ttu-id="aeac1-171">次の例は、データベースからエンティティを読み取り、それを応答の一部として返す方法を示しています。</span><span class="sxs-lookup"><span data-stu-id="aeac1-171">The following example shows how to read the entity from the database and return it as part of the response.</span></span>

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

<span data-ttu-id="aeac1-172">前の例では、CRT ランタイム エンジンは、登録されているデータ アダプターを介してチャンネルに自動的にクエリを作成します。</span><span class="sxs-lookup"><span data-stu-id="aeac1-172">For the preceding example, the CRT runtime engine automatically makes a query to the channel database via the registered data adapter.</span></span> <span data-ttu-id="aeac1-173">名前 **crt.ISVRetailStoreHoursView** を持つ型を照会して、コードで指定された **where** 句および列を生成します。</span><span class="sxs-lookup"><span data-stu-id="aeac1-173">It queries a type that has the name **crt.ISVRetailStoreHoursView**, and generates a **where** clause and columns as specified in the code.</span></span> <span data-ttu-id="aeac1-174">カスタマイザーは、カスタマイズの一部として SQL オブジェクトを提供する役割を担います。</span><span class="sxs-lookup"><span data-stu-id="aeac1-174">The customizer is responsible for providing the SQL objects as part of the customization.</span></span>

### <a name="adding-pre-triggers-and-post-triggers-for-a-specific-request"></a><span data-ttu-id="aeac1-175">特定の要求のプレトリガーとポストトリガーの追加</span><span class="sxs-lookup"><span data-stu-id="aeac1-175">Adding pre-triggers and post-triggers for a specific request</span></span>

<span data-ttu-id="aeac1-176">場合によっては、要求の前後で必要になる処理もあります。</span><span class="sxs-lookup"><span data-stu-id="aeac1-176">In some cases, some processing must be done before or after a request is handled.</span></span> <span data-ttu-id="aeac1-177">追加のコードを実行するために使用できる 2 つのフックがあります。</span><span class="sxs-lookup"><span data-stu-id="aeac1-177">There are two hooks that can be used to run additional code.</span></span> <span data-ttu-id="aeac1-178">これらのフックはプレトリガーおよびポストトリガーと呼ばれます。</span><span class="sxs-lookup"><span data-stu-id="aeac1-178">These hooks are called pre-triggers and post-triggers.</span></span> <span data-ttu-id="aeac1-179">新しいトリガーを作成して要求に関連付けるには、これらの手順に従います。</span><span class="sxs-lookup"><span data-stu-id="aeac1-179">Follow these steps to create new triggers and associate them with a request.</span></span>

1.  <span data-ttu-id="aeac1-180">IRequestTrigger を実装する新しいトリガー クラスを作成します。</span><span class="sxs-lookup"><span data-stu-id="aeac1-180">Create a new trigger class that implements IRequestTrigger.</span></span>

        public class GetCrossLoyaltyCardRequestTrigger : IRequestTrigger

2.  <span data-ttu-id="aeac1-181">**IRequest.SupportedRequestTypes** プロパティで、このトリガーを実行する必要がある要求の一覧を返します。</span><span class="sxs-lookup"><span data-stu-id="aeac1-181">In the **IRequest.SupportedRequestTypes** property, return the list of requests that this trigger should be run for.</span></span>

        public IEnumerable SupportedRequestTypes
        {
            get
            {
                return new[] { typeof(GetCrossLoyaltyCardRequest) };
            }
        }

3.  <span data-ttu-id="aeac1-182">要求の前後に呼び出される関数を実装します。</span><span class="sxs-lookup"><span data-stu-id="aeac1-182">Implement the functions that are called before and after the request.</span></span>

        void OnExecuted(Request request, Response response);
        void OnExecuting(Request request);

4.  <span data-ttu-id="aeac1-183">commerceRuntime.Config ファイルでクラスを登録します。</span><span class="sxs-lookup"><span data-stu-id="aeac1-183">Register the class in the commerceRuntime.Config file.</span></span>

## <a name="retail-server-extensibility-scenarios"></a><span data-ttu-id="aeac1-184">Retail サーバーの拡張機能シナリオ</span><span class="sxs-lookup"><span data-stu-id="aeac1-184">Retail Server extensibility scenarios</span></span>
### <a name="adding-a-new-odata-action-to-an-existing-controller"></a><span data-ttu-id="aeac1-185">既存のコントローラーへの新しい ODATA アクションの追加</span><span class="sxs-lookup"><span data-stu-id="aeac1-185">Adding a new ODATA action to an existing controller</span></span>

<span data-ttu-id="aeac1-186">最も簡単なシナリオでは、わずかに異なるユース ケースのために新しいアプリケーション プログラミング インターフェイス (API) を追加する必要があります。</span><span class="sxs-lookup"><span data-stu-id="aeac1-186">In the easiest scenario, you must add a new application programming interface (API) for a slightly different use case.</span></span> <span data-ttu-id="aeac1-187">このシナリオを機能させるには、継承によって新しいアクションを追加します。</span><span class="sxs-lookup"><span data-stu-id="aeac1-187">To make this scenario work, you can add the new action through inheritance.</span></span> <span data-ttu-id="aeac1-188">Retail サーバーへの API の任意の変更については、次の手順を実行する必要があります。</span><span class="sxs-lookup"><span data-stu-id="aeac1-188">For any changes to the APIs to Retail Server, you must follow these steps.</span></span>

1.  <span data-ttu-id="aeac1-189">新しいアクションまたはコントローラーを実装します。</span><span class="sxs-lookup"><span data-stu-id="aeac1-189">Implement the new action or controller.</span></span>
2.  <span data-ttu-id="aeac1-190">新しい対応するメタデータを追加するためのモデル出荷時の要件を上書きします。</span><span class="sxs-lookup"><span data-stu-id="aeac1-190">Override the requirements of the model factory to add the new corresponding metadata.</span></span>

<span data-ttu-id="aeac1-191">次の例は、Retail SDK から取得したもので、既存のコントローラーを拡張して POST アクションを持つようにする方法を示しています。</span><span class="sxs-lookup"><span data-stu-id="aeac1-191">The following example, which is taken from the Retail SDK, shows how to extend an existing controller so that it has a POST action.</span></span>

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

<span data-ttu-id="aeac1-192">次に、モデル ファクトリをオーバーライドします。</span><span class="sxs-lookup"><span data-stu-id="aeac1-192">Next, override the model factory.</span></span>

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

<span data-ttu-id="aeac1-193">クライアントがこの新しいカスタマイズを使用する前に、新しいモデル ファクトリ用の Retail サーバー プロキシ コードを生成するためにビルド システムを調整する必要があります。</span><span class="sxs-lookup"><span data-stu-id="aeac1-193">Before clients can use this new customization, you must adjust the build system to generate the Retail Server proxy code for the new model factory.</span></span> <span data-ttu-id="aeac1-194">この構成ステップはビルド システムで実行されます。</span><span class="sxs-lookup"><span data-stu-id="aeac1-194">This configuration step is done in the build system.</span></span> <span data-ttu-id="aeac1-195">最後に、web.config ファイルを調整する必要があります。</span><span class="sxs-lookup"><span data-stu-id="aeac1-195">Finally, you must adjust the web.config file.</span></span> <span data-ttu-id="aeac1-196">SDK の Retail サーバーの梱包プロジェクトでは、このステップを完了する必要があります。</span><span class="sxs-lookup"><span data-stu-id="aeac1-196">You must complete this step in the packaging project for Retail Server in the SDK.</span></span> <span data-ttu-id="aeac1-197">ローカルのテストが行われている場合、テストに使用されるローカル開発トポロジー コンピューターでこの手順を任意で実行できます。</span><span class="sxs-lookup"><span data-stu-id="aeac1-197">If local tests will be done, you can also optionally complete this step on the local development topology machine that is used for testing.</span></span>

### <a name="adding-a-new-simple-controller-for-an-entity"></a><span data-ttu-id="aeac1-198">エンティティの新しい簡単なコントローラーの追加</span><span class="sxs-lookup"><span data-stu-id="aeac1-198">Adding a new simple controller for an entity</span></span>

<span data-ttu-id="aeac1-199">単純なエンティティがあり、データをフェッチするコント ローラーを必要としているとします。</span><span class="sxs-lookup"><span data-stu-id="aeac1-199">Suppose that you have a simple entity and require a controller to fetch the data.</span></span> <span data-ttu-id="aeac1-200">例については、Retail SDK で StoreHours サンプルを参照してください。</span><span class="sxs-lookup"><span data-stu-id="aeac1-200">For an example, see the StoreHours sample in the Retail SDK.</span></span> <span data-ttu-id="aeac1-201">新しい Retail サーバー コントローラーには意味があり、低レベルのすべての作業が CRT (新しいエンティティ、要求、応答、およびサービス) で実行されます。</span><span class="sxs-lookup"><span data-stu-id="aeac1-201">A new Retail Server controller makes sense, and all the low-level work is done in the CRT (new entity, request, response, and service).</span></span> <span data-ttu-id="aeac1-202">新しいコントローラを作成するには、CommerceController から派生します。</span><span class="sxs-lookup"><span data-stu-id="aeac1-202">To create a new controller, you derive from CommerceController.</span></span> <span data-ttu-id="aeac1-203">例としてここに表示します。</span><span class="sxs-lookup"><span data-stu-id="aeac1-203">An example is shown here.</span></span> <span data-ttu-id="aeac1-204">コントローラー名は重要であり、エンティティの名前と一致する必要があります。</span><span class="sxs-lookup"><span data-stu-id="aeac1-204">The controller name is important and must match the name of the entity.</span></span>

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

<span data-ttu-id="aeac1-205">新しいエンティティについては、次の例に示すように、工場の **BuildEntitySets()** メソッドを上書きする必要があります。</span><span class="sxs-lookup"><span data-stu-id="aeac1-205">For new entities, you must also override the factory’s **BuildEntitySets()** method, as shown in the following example.</span></span>

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

### <a name="how-to-call-the-new-retail-server-api-from-mposcloud-pos"></a><span data-ttu-id="aeac1-206">MPOS/クラウド POS から新しい小売サーバー API を呼び出す方法:</span><span class="sxs-lookup"><span data-stu-id="aeac1-206">How to call the new retail server API from MPOS/Cloud POS:</span></span>

<span data-ttu-id="aeac1-207">新しい小売サーバー API を呼び出す前に、以下の手順を実行してください。</span><span class="sxs-lookup"><span data-stu-id="aeac1-207">Before calling the new retail server API please make sure you have performed the below steps:</span></span>

1.  <span data-ttu-id="aeac1-208">Retail サーバー web.config ファイルで新しい Retail サーバー拡張を登録します:  &lt;add source="assembly" value="**Your assembly name**" /&gt;</span><span class="sxs-lookup"><span data-stu-id="aeac1-208">Register your new retail server extension in Retail server web.config file:  &lt;add source="assembly" value="**Your assembly name**" /&gt;</span></span>
2.  <span data-ttu-id="aeac1-209">Customization.settings ファイルの新しい Retail サーバー拡張子を追加します。</span><span class="sxs-lookup"><span data-stu-id="aeac1-209">Add the new retail server extension in the Customization.settings file.</span></span> <span data-ttu-id="aeac1-210">このファイルは RetailSdk\\BuildTools&lt;RetailServerLibraryPathForProxyGeneration Condition="'$(RetailServerLibraryPathForProxyGeneration)' == ''"&gt;$(SdkReferencesPath)\\**Your assembly name.dll**&lt;/RetailServerLibraryPathForProxyGeneration&gt; &lt;/PropertyGroup&gt; で見つけることができます</span><span class="sxs-lookup"><span data-stu-id="aeac1-210">You can find this file in RetailSdk\\BuildTools&lt;RetailServerLibraryPathForProxyGeneration Condition="'$(RetailServerLibraryPathForProxyGeneration)' == ''"&gt;$(SdkReferencesPath)\\**Your assembly name.dll**&lt;/RetailServerLibraryPathForProxyGeneration&gt; &lt;/PropertyGroup&gt;</span></span>
3.  <span data-ttu-id="aeac1-211">CRT および Retail サーバー拡張子 dlls の両方を小売サーバー bin フォルダーにドロップします。</span><span class="sxs-lookup"><span data-stu-id="aeac1-211">Drop both the CRT and Retail server extension dlls into the retail server bin folder.</span></span> <span data-ttu-id="aeac1-212">新しい小売サーバー api に関連する CRT の拡張機能がある場合、小売サーバー bin フォルダーの commerceRuntime 構成ファイルにある情報をアップデートします。</span><span class="sxs-lookup"><span data-stu-id="aeac1-212">If you have any CRT extension that is related to the new retail server api then update that information in commerceRuntime configuration file under retail server bin folder.</span></span>
4.  <span data-ttu-id="aeac1-213">&lt;ソースの追加 = 「アセンブリ」値 = "**アセンブリ名**" /&gt;</span><span class="sxs-lookup"><span data-stu-id="aeac1-213">&lt;add source="assembly" value="**Your assembly name**" /&gt;</span></span>
5.  <span data-ttu-id="aeac1-214">inetmgr を使用して小売サーバーのメタデータを参照し、エンティティが xml で公開されているかどうかを確認します。</span><span class="sxs-lookup"><span data-stu-id="aeac1-214">Use inetmgr to browse to the retail server metadata and verify whether your entity is exposed in the xml.</span></span>
6.  <span data-ttu-id="aeac1-215">mpos/クラウド POSをコンパイルしてビルドし、プロキシを再生成します。</span><span class="sxs-lookup"><span data-stu-id="aeac1-215">Compile and build the mpos/Cloud POS to regenerate the proxy.</span></span> <span data-ttu-id="aeac1-216">コンパイラ中に、mpos は小売サーバーのメタデータで定義されたすべてのエンティティを再生成します。これにより、以下のようなコマース コンテキストを使用して新しいエンティティを呼び出すことができます。</span><span class="sxs-lookup"><span data-stu-id="aeac1-216">During compile mpos regenerates all the entities defined in the retail server metadata, so that you can call the new entities using the commerce context like below:</span></span>

#### <a name="cross-loyalty-sample"></a><span data-ttu-id="aeac1-217">クロス ロイヤルティ サンプル。</span><span class="sxs-lookup"><span data-stu-id="aeac1-217">Cross loyalty sample:</span></span>

    var request: Commerce.Proxy.Common.IDataServiceRequest = this._context.customers().getCrossLoyaltyCardDiscountAction(loyaltyCardNumber);
    return request.execute<number>();

#### <a name="store-hours-sample"></a><span data-ttu-id="aeac1-218">店舗の時間のサンプル:</span><span class="sxs-lookup"><span data-stu-id="aeac1-218">Store hours sample:</span></span>

    var request: Commerce.Proxy.Common.IDataServiceRequest = this._context.storeHours().getStoreDaysByStore(storeId);
    return request.execute<Commerce.Proxy.Entities.StoreDayHours[]>();

<span data-ttu-id="aeac1-219">mpos で新しい小売サーバー API を呼び出す方法について詳しくは、小売 SDK POS.Extension.CrossloaylySample および POS.Extension.SToreHoursSample サンプル プロジェクトをご覧ください。</span><span class="sxs-lookup"><span data-stu-id="aeac1-219">Please refer the retail SDK POS.Extension.CrossloaylySample and POS.Extension.SToreHoursSample sample projects for more details on how to call the new retail server api in mpos.</span></span>




