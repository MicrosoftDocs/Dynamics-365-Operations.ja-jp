---
title: "チャネル データベース (DB) 拡張機能"
description: "このトピックでは、チャネル データベースを拡張する方法について説明します。"
author: mugunthanm
manager: AnnBe
ms.date: 12/14/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
audience: Developer
ms.reviewer: robinr
ms.search.scope: Operations, Retail
ms.custom: 83892
ms.search.region: Global
ms.author: mumani
ms.search.validFrom: 2017-09-15
ms.dyn365.ops.version: AX 7.0.0, Retail September 2017 update
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: 773c14db56ac179fedfdeba3ed5b274f9cc63fc9
ms.contentlocale: ja-jp
ms.lasthandoff: 05/08/2018

---

# <a name="channel-database-db-extensions"></a><span data-ttu-id="012e9-103">チャネル データベース (DB) 拡張機能</span><span class="sxs-lookup"><span data-stu-id="012e9-103">Channel database (DB) extensions</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="012e9-104">チャネル データベース (チャネル DB) は、オンライン ストアまたはブリックアンドモルタル ストアなどの 1 つまたは複数の小売チャネルからのトランザクションおよびマスターデータを保持します。</span><span class="sxs-lookup"><span data-stu-id="012e9-104">The channel database (channel DB) holds transactional and master data from one or more retail channels, such as an online store or a brick-and-mortar store.</span></span> <span data-ttu-id="012e9-105">マスター データは、Commerce Data Exchange (CDX) を使用して小売用バックオフィス (Retail HQ) からチャネル データベースに適用されます。</span><span class="sxs-lookup"><span data-stu-id="012e9-105">The master data is pushed down from the Retail Headquarters (Retail HQ) to the channel database using the commerce data exchange (CDX).</span></span> <span data-ttu-id="012e9-106">チャネル データベースに格納されたトランザクション データは、CDX を使用して本社に引き戻されます。</span><span class="sxs-lookup"><span data-stu-id="012e9-106">The transactional data stored in the channel database is pulled back to the headquarters using the CDX.</span></span>

<span data-ttu-id="012e9-107">このトピックでは、さまざまなシナリオのチャネル データベースを拡張する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="012e9-107">In this topic we explain how to extend the channel database for different scenarios.</span></span> <span data-ttu-id="012e9-108">ここで説明したステップは、Dynamics 365 for Retail、Dynamics 365 for Finance and Operations にのみ適用されます。</span><span class="sxs-lookup"><span data-stu-id="012e9-108">The steps here apply only to Dynamics 365 for Retail, Dynamics 365 for Finance and Operations.</span></span>

<span data-ttu-id="012e9-109">拡張機能のさまざまなシナリオを説明する前に、チャネル DB 拡張機能の最新の機能拡張を理解することが重要です。</span><span class="sxs-lookup"><span data-stu-id="012e9-109">Before discussing the different scenarios for extension, it's important to understand the recent enhancements to channel DB extensions.</span></span> 

<span data-ttu-id="012e9-110">アップグレード時のカスタマイズの処理の方法にいくつかの改善を加えました。</span><span class="sxs-lookup"><span data-stu-id="012e9-110">We have made some improvements to how customizations are handled during an upgrade.</span></span> <span data-ttu-id="012e9-111">以下の環境構成のいずれかを使用することをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="012e9-111">We recommend using one of the following environment configurations:</span></span>
- <span data-ttu-id="012e9-112">Microsoft Dynamics 365 for Finance and Operations, Enterprise Edition (2017 年 7 月) アプリケーション更新プログラム 5</span><span class="sxs-lookup"><span data-stu-id="012e9-112">Microsoft Dynamics 365 for Finance and Operations, Enterprise edition (July 2017) with application update 5.</span></span>
- <span data-ttu-id="012e9-113">Microsoft Dynamics 365 for Retail 7.2 アプリケーション更新プログラム 5 はすぐに入手できるようになります。</span><span class="sxs-lookup"><span data-stu-id="012e9-113">Microsoft Dynamics 365 for Retail 7.2 with application update 5, which will be available soon.</span></span>
- <span data-ttu-id="012e9-114">Microsoft Dynamics 365 for Retail 7.3 には、アプリケーション更新プログラム 5 が含まれます。</span><span class="sxs-lookup"><span data-stu-id="012e9-114">Microsoft Dynamics 365 for Retail 7.3, which includes application update 5.</span></span>
- <span data-ttu-id="012e9-115">アプリケーション更新プログラム 5 を含む Microsoft Dynamics 365 for Finance and Operations 7.3。</span><span class="sxs-lookup"><span data-stu-id="012e9-115">Microsoft Dynamics 365 for Finance and Operations 7.3, which includes application update 5.</span></span>

## <a name="ext-schema"></a><span data-ttu-id="012e9-116">Ext スキーマ</span><span class="sxs-lookup"><span data-stu-id="012e9-116">Ext Schema</span></span>

<span data-ttu-id="012e9-117">Dynamics 365 for Retail および Dynamics 365 Finance and Operations では、**ext スキーマ**と呼ばれる新しいスキーマを導入して拡張機能をサポートしました。</span><span class="sxs-lookup"><span data-stu-id="012e9-117">In Dynamics 365 for Retail and Dynamics 365 Finance and Operations we introduced a new schema called the **ext schema** to support extensions.</span></span> <span data-ttu-id="012e9-118">以前のバージョンでは、チャネル DB に拡張機能を追加する場合、CRT または AX スキーマに追加していました。</span><span class="sxs-lookup"><span data-stu-id="012e9-118">In previous versions, if you wanted to add an extension to channel DB, you would add it to the CRT or AX schema.</span></span> <span data-ttu-id="012e9-119">Dynamics 365 for Retail および Dynamics 365 for Finance and Operations バージョンでは、CRT、AX、または DBO スキーマを変更することはできません。</span><span class="sxs-lookup"><span data-stu-id="012e9-119">In Dynamics 365 for Retail and Dynamics 365 for Finance and Operations version you cannot change the CRT, AX, or DBO schemas.</span></span> <span data-ttu-id="012e9-120">すべての変更は **ext スキーマ**で行う必要があります。</span><span class="sxs-lookup"><span data-stu-id="012e9-120">All changes must be made in the **ext schema**.</span></span> <span data-ttu-id="012e9-121">CRT または AX スキーマで変更する場合は、Lifecycle Service での配置は失敗します。</span><span class="sxs-lookup"><span data-stu-id="012e9-121">If you modify anything in the CRT or AX schemas, then deployment in Lifecycle Services will fail.</span></span> <span data-ttu-id="012e9-122">CRT、AX、および DBO スキーマを変更する権限を持たないエラー レポート。</span><span class="sxs-lookup"><span data-stu-id="012e9-122">The error reports that don’t have permission to modify the CRT, AX, and DBO schemas.</span></span> 

## <a name="best-practices-for-channel-db-extensions"></a><span data-ttu-id="012e9-123">チャネル DB 拡張機能のためのベスト プラクティス</span><span class="sxs-lookup"><span data-stu-id="012e9-123">Best practices for channel DB extensions</span></span>

- <span data-ttu-id="012e9-124">CRT、AX、または DBO スキーマ内では何も変更しないでください。</span><span class="sxs-lookup"><span data-stu-id="012e9-124">Don’t modify anything in the CRT, AX, or DBO schemas.</span></span> <span data-ttu-id="012e9-125">すべての拡張シナリオで **ext スキーマ**を使用します。</span><span class="sxs-lookup"><span data-stu-id="012e9-125">Use the **ext schema** for all extension scenarios.</span></span>
- <span data-ttu-id="012e9-126">**ext schema** 内で、CRT、AX、または DBO オブジェクトにアクセスしないでください。</span><span class="sxs-lookup"><span data-stu-id="012e9-126">Don’t access any CRT, AX, or DBO objects in the **ext schema**.</span></span> <span data-ttu-id="012e9-127">任意のチャネル データベース コンポーネントにアクセスするには、商取引ランタイム データ サービスを使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="012e9-127">You must use the commerce runtime data service to access any channel DB artifacts.</span></span>

### <a name="dont-do-this"></a><span data-ttu-id="012e9-128">このようにしない</span><span class="sxs-lookup"><span data-stu-id="012e9-128">Don't do this</span></span>
<span data-ttu-id="012e9-129">以下はユーザーがしてはいけないことの例です。</span><span class="sxs-lookup"><span data-stu-id="012e9-129">The following is an example of what you should not do.</span></span> <span data-ttu-id="012e9-130">代わりに、主キーの値を取得するために CRT データ サービスを使用してから、拡張テーブルに挿入するために主キーの値を使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="012e9-130">Instead, you should use the CRT data service to get the primary key value and then use the primary key to insert into your extension table.</span></span>

```sql
MERGE INTO [ax].RETAILCUSTPREFERENCE   --DONT access ax schema object
USING (SELECT DISTINCT
tp.PARENTRECID, tp.PROPERTYVALUE as [EMAILOPTIN], ct.ACCOUNTNUM, ct.DATAAREAID
FROM @TVP_EXTENSIONPROPERTIESTABLETYPE tp
JOIN [ax].CUSTTABLE ct on ct.RECID = tp.PARENTRECID  --DONT access ax schema object
WHERE tp.PARENTRECID <> 0 and tp.PROPERTYNAME = 'EMAILOPTIN') AS SOURCE
ON [ax].RETAILCUSTPREFERENCE.RECID = SOURCE.PARENTRECID   
and [ax].RETAILCUSTPREFERENCE.DATAAREAID = SOURCE.DATAAREAID --DONT access ax schema object
and [ax].RETAILCUSTPREFERENCE.ACCOUNTNUM = SOURCE.ACCOUNTNUM
WHEN MATCHED THEN
UPDATE SET [EMAILOPTIN] = source.[EMAILOPTIN]
WHEN NOT MATCHED THEN
INSERT
(
    RECID
    ,DATAAREAID
    ,EMAILOPTIN
    ,ACCOUNTNUM
)
VALUES
(
    SOURCE.PARENTRECID
    ,SOURCE.DATAAREAID
    ,SOURCE.EMAILOPTIN
    ,SOURCE.ACCOUNTNUM
);
SELECT @i_Error = @@ERROR;
IF @i_Error <> 0
    BEGIN
    SET @i_ReturnCode = @i_Error;
    GOTO exit_label;
END;
```


### <a name="dont-do-this"></a><span data-ttu-id="012e9-131">このようにしない</span><span class="sxs-lookup"><span data-stu-id="012e9-131">Don't do this</span></span>
- <span data-ttu-id="012e9-132">拡張テーブルまたは新しいテーブルを作成する場合、すべてを ext スキーマで行う必要があります。</span><span class="sxs-lookup"><span data-stu-id="012e9-132">If you are creating extension table or new table all should be done in ext schema.</span></span>
- <span data-ttu-id="012e9-133">ビュー、手順、関数、またはデータベースのコンポーネントを変更しないでください。</span><span class="sxs-lookup"><span data-stu-id="012e9-133">Don’t modify any views, procedures, functions or any of the database artifacts.</span></span>
- <span data-ttu-id="012e9-134">拡張子からのビュー、定義されたタイプ、関数および手順を含むデータベースのコンポーネントにアクセスしたり、呼び出したりしないでください。</span><span class="sxs-lookup"><span data-stu-id="012e9-134">Don’t access or call any of any database artifacts including views, defined types, functions and procedures from your extensions.</span></span>
- <span data-ttu-id="012e9-135">データベースのアーティファクトにアクセスするには、CRT データ サービスを使用します。</span><span class="sxs-lookup"><span data-stu-id="012e9-135">To access the database artifacts, use the CRT data service.</span></span> <span data-ttu-id="012e9-136">たとえば、一部のカスタム フィールドを検索する、または仕訳帳のビューにカスタム列を表示する製品検索ビューを拡張するとします。</span><span class="sxs-lookup"><span data-stu-id="012e9-136">For example, suppose you want to extend the product search view to search some custom fields or to show custom columns in journal views.</span></span> <span data-ttu-id="012e9-137">SQL 内では、ビューまたは手順、機能を変更しないでください。</span><span class="sxs-lookup"><span data-stu-id="012e9-137">Don’t modify the views or procedures or functions in SQL.</span></span> <span data-ttu-id="012e9-138">代わりに、CRT データ サービスを使用して、投稿トリガーをオーバーライドまたは使用することによって拡張機能を実行し、拡張プロシージャを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="012e9-138">Instead, use the CRT data service and do the extension either by overriding or using post triggers and then call your extended procedures.</span></span>

```sql
CREATE VIEW [ext].[CONTOSORETAILSTOREHOURSVIEW] AS
(
    SELECT
    sdht.DAY,
    sdht.OPENTIME,
    sdht.CLOSINGTIME,
    sdht.RECID,
    rst.STORENUMBER
    FROM [ext].[CONTOSORETAILSTOREHOURSTABLE\] sdht
    INNER JOIN [ax].RETAILSTORETABLE rst ON rst.RECID = sdht.RETAILSTORETABLE  --DONT access ax schema object
)
```

## <a name="adding-extensions"></a><span data-ttu-id="012e9-139">拡張機能の追加</span><span class="sxs-lookup"><span data-stu-id="012e9-139">Adding extensions</span></span>
1. <span data-ttu-id="012e9-140">すべての拡張機能テーブルは **UserRole** および **DeployExtensibilityRole** にアクセス許可を付与する必要があります。</span><span class="sxs-lookup"><span data-stu-id="012e9-140">All the extension tables should have grant permission on **UserRole** and **DeployExtensibilityRole**.</span></span>

    ```sql
    GRANT EXECUTE ON [ext].[EXTTABLENAME] TO [DeployExtensibilityRole];
        GO
        GRANT EXECUTE ON [ext].[EXTTABLENAME] TO [UsersRole];
        GO
    ```

2. <span data-ttu-id="012e9-141">テーブルが HQ から受信するデータを送信する場合、**DataSyncUsersRole** アクセス許可を付与します。</span><span class="sxs-lookup"><span data-stu-id="012e9-141">Grant **DataSyncUsersRole** permission if your table is going to send receive data from HQ.</span></span>

    ```sql
    GRANT SELECT, INSERT, UPDATE, DELETE ON OBJECT::[ext].[EXTTABLENAME] TO [DataSyncUsersRole]
    GO
    ```

3. <span data-ttu-id="012e9-142">拡張テーブルを作成し、HQ にデータを同期させる場合は、拡張テーブルに親テーブルの主な列を含めます。</span><span class="sxs-lookup"><span data-stu-id="012e9-142">If you are creating extended table and want to sync the data back to HQ, then have the primary column of the parent table in the extended table.</span></span>
4. <span data-ttu-id="012e9-143">たとえば、**ContosoRetailTransactionTable** など、常にテーブルに接頭語を付けると、他のパートナー/ISV カスタマイズとの競合を回避できます。</span><span class="sxs-lookup"><span data-stu-id="012e9-143">Always prefix your table, for example, **ContosoRetailTransactionTable**, so that you can avoid conflicts with other partner/ISV customizations.</span></span>

## <a name="attributes"></a><span data-ttu-id="012e9-144">属性</span><span class="sxs-lookup"><span data-stu-id="012e9-144">Attributes</span></span>

<span data-ttu-id="012e9-145">顧客、顧客の注文、現金売りトランザクション、およびコール センター注文の属性をサポートするために、HQ の属性フレームワークを拡張しました。</span><span class="sxs-lookup"><span data-stu-id="012e9-145">We extended the attribute framework in HQ to support attributes for Customers, Customer orders, cash and carry transactions and call center orders.</span></span>

### <a name="customer-attributes"></a><span data-ttu-id="012e9-146">顧客属性</span><span class="sxs-lookup"><span data-stu-id="012e9-146">Customer attributes</span></span>
<span data-ttu-id="012e9-147">新しい顧客属性フレームワークでは、構成を使用して、POS または HQ 内の顧客追加/編集画面または顧客詳細画面に新しいフィールドを追加することができます。</span><span class="sxs-lookup"><span data-stu-id="012e9-147">With the new customer attribute framework, you can use configurations to add new fields to the customer add/edit or customer details screens in POS or HQ.</span></span> <span data-ttu-id="012e9-148">小売パラメーターで顧客属性グループを構成した後、POS や HQ はコードの変更やカスタマイズを行わずに新しい属性を自動的に表示します。</span><span class="sxs-lookup"><span data-stu-id="012e9-148">After configuring the customer attribute group in retail parameters, POS and HQ will automatically show up the new attribute without any code change or customization.</span></span> <span data-ttu-id="012e9-149">画面レイアウト設計者は、取引画面 (**顧客** パネル) に顧客属性を表示するようにも設定されます。</span><span class="sxs-lookup"><span data-stu-id="012e9-149">The screen layout designer will also be configured to show the customer attributes in the transaction screen - **Customer** panel.</span></span>

### <a name="order-attributes"></a><span data-ttu-id="012e9-150">注文属性</span><span class="sxs-lookup"><span data-stu-id="012e9-150">Order attributes</span></span>
<span data-ttu-id="012e9-151">属性フレームワークは、現金売りトランザクション、顧客の注文、およびコール センター注文の属性をサポートするように拡張されました。</span><span class="sxs-lookup"><span data-stu-id="012e9-151">The attribute framework was extended to support attributes in cash and carry transactions, customer orders, and call center orders.</span></span> <span data-ttu-id="012e9-152">HQ または CRT で値を直接編集して設定することができます。</span><span class="sxs-lookup"><span data-stu-id="012e9-152">You can edit and set values directly in HQ or in CRT.</span></span> <span data-ttu-id="012e9-153">これらすべてはデータベースを変更せずにコンフィギュレーションを介して実行することができます。</span><span class="sxs-lookup"><span data-stu-id="012e9-153">All this can be done through configurations, without any database changes.</span></span> <span data-ttu-id="012e9-154">(基本的な CRUD 操作は必要ではなく、主要なビジネス ロジックの属性値をカスタマイズすることができます。) 以前は、これを行うには、HQ とチャンネル DB に新しいテーブルを作成し、CRT を変更する必要がありました。</span><span class="sxs-lookup"><span data-stu-id="012e9-154">(You can customization the attribute values for core business logic, not required for basic CRUD operations.) Previously, you had to create new tables in HQ and channel DB, and then modify CRT to do this.</span></span> <span data-ttu-id="012e9-155">現在は、すべての属性の作成をコンフィギュレーションを通じて実行できるようになりました。</span><span class="sxs-lookup"><span data-stu-id="012e9-155">Now all the attribute creation can be done through configuration.</span></span> 

## <a name="adding-a-new-table"></a><span data-ttu-id="012e9-156">新しいテーブルの追加</span><span class="sxs-lookup"><span data-stu-id="012e9-156">Adding a new table</span></span>

<span data-ttu-id="012e9-157">このシナリオでは、新しいテーブルを作成し、チャネル DB に追加する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="012e9-157">In this scenario we will explain how to create a new table and add it to the channel DB.</span></span> <span data-ttu-id="012e9-158">すべての拡張コードは **ext スキーマ**へアクセスすることができます。</span><span class="sxs-lookup"><span data-stu-id="012e9-158">All extension code has access to the **ext schema**.</span></span>

1. <span data-ttu-id="012e9-159">SQL Server Management Studio デザイナーを使用するか、SQL スクリプトを使用して、**ext スキーマ**のチャネル データベースに新しいテーブルを作成します。</span><span class="sxs-lookup"><span data-stu-id="012e9-159">Create a new table in the channel database in the **ext schema** either using SQL Server Management Studio Designer or using SQL scripts.</span></span> <span data-ttu-id="012e9-160">以下は、SQL スクリプトの例です。</span><span class="sxs-lookup"><span data-stu-id="012e9-160">The following is an example SQL script.</span></span>

    ```sql
    -- Create the extension table to store the custom fields.
    IF (SELECT OBJECT_ID('[ext].[CONTOSORETAILSTOREHOURSTABLE]')) IS NULL
    BEGIN
    CREATE TABLE [ext].[CONTOSORETAILSTOREHOURSTABLE](
    [RECID] [bigint] NOT NULL,
    [DAY] [int] NOT NULL DEFAULT ((0)),
    [OPENTIME] [int] NOT NULL DEFAULT ((0)),
    [CLOSINGTIME] [int] NOT NULL DEFAULT ((0)),
    [RETAILSTORETABLE] [bigint] NOT NULL DEFAULT ((0)),
    CONSTRAINT [I_CONTOSORETAILSTOREHOURSTABLE_RECID] PRIMARY KEY CLUSTERED
    (
        [RECID] ASC
    ) WITH (PAD_INDEX = OFF, STATISTICS_NORECOMPUTE = OFF, IGNORE_DUP_KEY = OFF, ALLOW_ROW_LOCKS = ON, ALLOW_PAGE_LOCKS = ON) ON [PRIMARY]
    ) ON [PRIMARY]
    ALTER TABLE [ext].[CONTOSORETAILSTOREHOURSTABLE] WITH CHECK ADD CHECK (([RECID]<>(0)))
    END
    GO
    GRANT SELECT, INSERT, UPDATE, DELETE ON OBJECT::[ext].[CONTOSORETAILSTOREHOURSTABLE] TO [DataSyncUsersRole]
    GO

## Extending an existing table

If you are extending existing table, then you must either use attributes if supported for that entity or create and extended table (new table) with same primary key as the parent table. The following script extends a table.

```sql
CREATE TABLE [ext].[RETAILTRANSACTIONTABLE](
[TRANSACTIONID] [nvarchar](44) NOT NULL, -- FK to [crt].RETAILTRANSACTIONTABLE
[ISB2BSALES] [int] NOT NULL DEFAULT (0),
[EXTERNALID] [nvarchar](20) NOT NULL DEFAULT (''),
CONSTRAINT [EXT_RETAILTRANSACTIONTABLE_PK] PRIMARY KEY CLUSTERED
(
    [TRANSACTIONID]
) WITH (PAD_INDEX = OFF, STATISTICS_NORECOMPUTE = OFF, IGNORE_DUP_KEY = OFF, ALLOW_ROW_LOCKS = ON, ALLOW_PAGE_LOCKS = ON) ON [PRIMARY]
     ) ON [PRIMARY]
GO
GRANT INSERT ON [ext].[RETAILTRANSACTIONTABLE] TO [DataSyncUsersRole];
GO
GRANT DELETE ON [ext].[RETAILTRANSACTIONTABLE] TO [DataSyncUsersRole];
GO
GRANT UPDATE ON [ext\].[RETAILTRANSACTIONTABLE] TO [DataSyncUsersRole];
GO
GRANT SELECT ON [ext].[RETAILTRANSACTIONTABLE] TO [DataSyncUsersRole];
GO
```

## <a name="adding-new-views-stored-procedure-functions-and-defined-types"></a><span data-ttu-id="012e9-161">新しいビュー、ストアド プロシージャ、関数、定義済タイプの追加</span><span class="sxs-lookup"><span data-stu-id="012e9-161">Adding new views, stored procedure, functions, and defined types</span></span>

<span data-ttu-id="012e9-162">すべての新しいストアド プロシージャ、ビューまたは機能は **ext スキーマ**に作成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="012e9-162">All new stored procedures, views or functions must be created in the **ext schema**.</span></span> <span data-ttu-id="012e9-163">手順、ビューまたは機能から、データベース コンポーネントをアクセスするまたは呼びだすことはやめてください。</span><span class="sxs-lookup"><span data-stu-id="012e9-163">Don't access or call our database artifacts from your procedures, views, or functions.</span></span>

## <a name="deployment-checks"></a><span data-ttu-id="012e9-164">配置のチェック</span><span class="sxs-lookup"><span data-stu-id="012e9-164">Deployment checks</span></span>

<span data-ttu-id="012e9-165">配置プロセスは、データベースのコンポーネントに変更があるかどうかを判断します。</span><span class="sxs-lookup"><span data-stu-id="012e9-165">The deployment process determines if there are any modification to the database artifacts.</span></span> <span data-ttu-id="012e9-166">CRT、AX、または DBO スキーマ オブジェクトを変更しようとした場合、または SQL で直接シナリオに対してそれらにアクセスすると、展開は失敗します。</span><span class="sxs-lookup"><span data-stu-id="012e9-166">If you have attempted to modify the CRT, AX, or DBO schema objects, or access them for any scenario directly in SQL, then deployment will fail.</span></span>


