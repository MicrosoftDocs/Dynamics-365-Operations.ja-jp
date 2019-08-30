---
title: チャネル データベース 拡張機能
description: このトピックでは、チャネル データベースを拡張する方法について説明します。
author: mugunthanm
manager: AnnBe
ms.date: 08/12/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Developer
ms.reviewer: rhaertle
ms.search.scope: Operations, Retail
ms.custom: 83892
ms.search.region: Global
ms.author: mumani
ms.search.validFrom: 2017-09-15
ms.dyn365.ops.version: AX 7.0.0, Retail September 2017 update
ms.openlocfilehash: e0a3aa4ec83804b711d495b3556c8c43b4226508
ms.sourcegitcommit: 6545bef4584d72dd7789f2d3935cf00ac8f489b0
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/13/2019
ms.locfileid: "1871043"
---
# <a name="channel-database-extensions"></a><span data-ttu-id="bcf0d-103">チャネル データベース 拡張機能</span><span class="sxs-lookup"><span data-stu-id="bcf0d-103">Channel database extensions</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="bcf0d-104">チャネル データベース (チャネル DB) は、オンライン ストアまたはブリックアンドモルタル ストアなどの 1 つまたは複数の小売チャネルからのトランザクションおよびマスターデータを保持します。</span><span class="sxs-lookup"><span data-stu-id="bcf0d-104">The channel database (channel DB) holds transactional and master data from one or more retail channels, such as an online store or a brick-and-mortar store.</span></span> <span data-ttu-id="bcf0d-105">Commerce Data Exchange (CDX) を使用して、Retail Headquarters マスター データは (Retail HQ) からチャネル データベースにプッシュされます。</span><span class="sxs-lookup"><span data-stu-id="bcf0d-105">The master data is pushed down from the Retail Headquarters (Retail HQ) to the channel database using the commerce data exchange (CDX).</span></span> <span data-ttu-id="bcf0d-106">チャネル データベースに格納されたトランザクション データは、CDX を使用して本社に引き戻されます。</span><span class="sxs-lookup"><span data-stu-id="bcf0d-106">The transactional data stored in the channel database is pulled back to the headquarters using the CDX.</span></span>

<span data-ttu-id="bcf0d-107">このトピックでは、さまざまなシナリオのチャネル データベースを拡張する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="bcf0d-107">In this topic we explain how to extend the channel database for different scenarios.</span></span> <span data-ttu-id="bcf0d-108">以下の手順は、Dynamics 365 for Retail、Dynamics 365 for Finance and Operations にのみ適用します。</span><span class="sxs-lookup"><span data-stu-id="bcf0d-108">The steps here apply only to Dynamics 365 for Retail, Dynamics 365 for Finance and Operations.</span></span>

<span data-ttu-id="bcf0d-109">拡張機能のさまざまなシナリオを説明する前に、チャネル DB 拡張機能の最新の機能拡張を理解することが重要です。</span><span class="sxs-lookup"><span data-stu-id="bcf0d-109">Before discussing the different scenarios for extension, it's important to understand the recent enhancements to channel DB extensions.</span></span>

<span data-ttu-id="bcf0d-110">アップグレード時の拡張機能の処理の方法にいくつかの改善を加えました。</span><span class="sxs-lookup"><span data-stu-id="bcf0d-110">We have made some improvements to how extensions are handled during an upgrade.</span></span> <span data-ttu-id="bcf0d-111">以下の環境構成のいずれかを使用することをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="bcf0d-111">We recommend using one of the following environment configurations:</span></span>
- <span data-ttu-id="bcf0d-112">Microsoft Dynamics 365 for Finance and Operations, Enterprise edition (2017 年 7 月) およびアプリケーション更新プログラム 5</span><span class="sxs-lookup"><span data-stu-id="bcf0d-112">Microsoft Dynamics 365 for Finance and Operations, Enterprise edition (July 2017) with application update 5.</span></span>
- <span data-ttu-id="bcf0d-113">Microsoft Dynamics 365 for Retail 7.2 およびアプリケーション更新プログラム 5 (まもなく利用できます)</span><span class="sxs-lookup"><span data-stu-id="bcf0d-113">Microsoft Dynamics 365 for Retail 7.2 with application update 5, which will be available soon.</span></span>
- <span data-ttu-id="bcf0d-114">Microsoft Dynamics 365 for Retail 7.3 (アプリケーション更新プログラム 5 を含みます)</span><span class="sxs-lookup"><span data-stu-id="bcf0d-114">Microsoft Dynamics 365 for Retail 7.3, which includes application update 5.</span></span>
- <span data-ttu-id="bcf0d-115">Microsoft Dynamics 365 for Finance and Operations 7.3 (アプリケーション更新プログラム 5 を含みます)</span><span class="sxs-lookup"><span data-stu-id="bcf0d-115">Microsoft Dynamics 365 for Finance and Operations 7.3, which includes application update 5.</span></span>

## <a name="ext-schema"></a><span data-ttu-id="bcf0d-116">Ext スキーマ</span><span class="sxs-lookup"><span data-stu-id="bcf0d-116">Ext schema</span></span>

<span data-ttu-id="bcf0d-117">Dynamics 365 for Retail および Dynamics 365 Finance and Operations では、**ext スキーマ**と呼ばれる新しいスキーマを導入して拡張機能をサポートしました。</span><span class="sxs-lookup"><span data-stu-id="bcf0d-117">In Dynamics 365 for Retail and Dynamics 365 Finance and Operations we introduced a new schema called the **ext schema** to support extensions.</span></span> <span data-ttu-id="bcf0d-118">以前のバージョンでは、チャネル DB に拡張機能を追加する場合、CRT または AX スキーマに追加していました。</span><span class="sxs-lookup"><span data-stu-id="bcf0d-118">In previous versions, if you wanted to add an extension to channel DB, you would add it to the CRT or AX schema.</span></span> <span data-ttu-id="bcf0d-119">小売および Finance and Operations の両方のスキーマを変更CRT、AX、または DBO スキーマを変更することはできません。</span><span class="sxs-lookup"><span data-stu-id="bcf0d-119">In both Retail and Finance and Operations, you cannot change the CRT, AX, or DBO schemas.</span></span> <span data-ttu-id="bcf0d-120">すべての変更は **ext スキーマ**で行う必要があります。</span><span class="sxs-lookup"><span data-stu-id="bcf0d-120">All changes must be made in the **ext schema**.</span></span> <span data-ttu-id="bcf0d-121">CRT または AX スキーマの何かを変更すると、Lifecycle Services (LCS) での展開に失敗します。</span><span class="sxs-lookup"><span data-stu-id="bcf0d-121">If you modify anything in the CRT or AX schemas, then deployment in Lifecycle Services (LCS) will fail.</span></span> <span data-ttu-id="bcf0d-122">CRT、AX、および DBO スキーマを変更する権限がありませんというエラーが報告されます。</span><span class="sxs-lookup"><span data-stu-id="bcf0d-122">An error message states that don’t have permission to modify the CRT, AX, and DBO schemas.</span></span>

> [!NOTE]
> <span data-ttu-id="bcf0d-123">いずれかのチャネル DB フィールドの長さを伸ばす場合は、LCS で拡張機能の要求を作成し、EDT の伸長または小数点以下の精度を高める必要があります。</span><span class="sxs-lookup"><span data-stu-id="bcf0d-123">If you want to increase any channel DB field length, you must create an extensibility request in LCS, increasing the EDT length or decimal precision.</span></span> <span data-ttu-id="bcf0d-124">Dynamics 365 Finance and Operations は、変更をチャネル DB に自動的にプッシュしません。また、拡張子には、チャネル DB - CRT、AXまたは DBO スキーマでなにかを変更または修正するための許可が付与されません。</span><span class="sxs-lookup"><span data-stu-id="bcf0d-124">Dynamics 365 Finance and Operations will not automatically push the changes to the channel DB, and extensions will not have permissions to change or modify anything in the channel DB - CRT, AX or DBO schema.</span></span> <span data-ttu-id="bcf0d-125">CRT または AX スキーマの何かを変更すると、LCS での展開が失敗します。</span><span class="sxs-lookup"><span data-stu-id="bcf0d-125">If you modify anything in the CRT or AX schemas, then deployment in LCS will fail.</span></span>

## <a name="best-practices-for-channel-db-extensions"></a><span data-ttu-id="bcf0d-126">チャネル DB 拡張機能のためのベスト プラクティス</span><span class="sxs-lookup"><span data-stu-id="bcf0d-126">Best practices for channel DB extensions</span></span>

- <span data-ttu-id="bcf0d-127">CRT、AX、または DBO スキーマのいずれも変更しないでください。</span><span class="sxs-lookup"><span data-stu-id="bcf0d-127">Don’t modify anything in the CRT, AX, or DBO schemas.</span></span> <span data-ttu-id="bcf0d-128">すべての拡張シナリオで **ext スキーマ**を使用します。</span><span class="sxs-lookup"><span data-stu-id="bcf0d-128">Use the **ext schema** for all extension scenarios.</span></span>
- <span data-ttu-id="bcf0d-129">**ext schema** 内で、CRT、AX、または DBO オブジェクトにアクセスしないでください。</span><span class="sxs-lookup"><span data-stu-id="bcf0d-129">Don’t access any CRT, AX, or DBO objects in the **ext schema**.</span></span> <span data-ttu-id="bcf0d-130">任意のチャネル データベース コンポーネントにアクセスするには、商取引ランタイム データ サービスを使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="bcf0d-130">You must use the commerce runtime data service to access any channel DB artifacts.</span></span>

### <a name="dont-do-this"></a><span data-ttu-id="bcf0d-131">このようにしない</span><span class="sxs-lookup"><span data-stu-id="bcf0d-131">Don't do this</span></span>
<span data-ttu-id="bcf0d-132">以下はユーザーがしてはいけないことの例です。</span><span class="sxs-lookup"><span data-stu-id="bcf0d-132">The following is an example of what you should not do.</span></span> <span data-ttu-id="bcf0d-133">代わりに、主キーの値を取得するために CRT データ サービスを使用してから、拡張テーブルに挿入するために主キーの値を使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="bcf0d-133">Instead, you should use the CRT data service to get the primary key value and then use the primary key to insert into your extension table.</span></span>

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


### <a name="dont-do-this"></a><span data-ttu-id="bcf0d-134">このようにしない</span><span class="sxs-lookup"><span data-stu-id="bcf0d-134">Don't do this</span></span>
- <span data-ttu-id="bcf0d-135">拡張テーブルまたは新しいテーブルを作成する場合、すべてを ext スキーマで行う必要があります。</span><span class="sxs-lookup"><span data-stu-id="bcf0d-135">If you are creating extension table or new table all should be done in ext schema.</span></span>
- <span data-ttu-id="bcf0d-136">ビュー、手順、関数、またはデータベースのコンポーネントを変更しないでください。</span><span class="sxs-lookup"><span data-stu-id="bcf0d-136">Don’t modify any views, procedures, functions or any of the database artifacts.</span></span>
- <span data-ttu-id="bcf0d-137">拡張子からのビュー、定義されたタイプ、関数および手順を含むデータベースのコンポーネントにアクセスしたり、呼び出したりしないでください。</span><span class="sxs-lookup"><span data-stu-id="bcf0d-137">Don’t access or call any of any database artifacts including views, defined types, functions and procedures from your extensions.</span></span>
- <span data-ttu-id="bcf0d-138">データベースのアーティファクトにアクセスするには、CRT データ サービスを使用します。</span><span class="sxs-lookup"><span data-stu-id="bcf0d-138">To access the database artifacts, use the CRT data service.</span></span> <span data-ttu-id="bcf0d-139">たとえば、一部のカスタム フィールドを検索する、または仕訳帳のビューにカスタム列を表示する製品検索ビューを拡張するとします。</span><span class="sxs-lookup"><span data-stu-id="bcf0d-139">For example, suppose you want to extend the product search view to search some custom fields or to show custom columns in journal views.</span></span> <span data-ttu-id="bcf0d-140">SQL 内では、ビューまたは手順、機能を変更しないでください。</span><span class="sxs-lookup"><span data-stu-id="bcf0d-140">Don’t modify the views or procedures or functions in SQL.</span></span> <span data-ttu-id="bcf0d-141">代わりに、CRT データ サービスを使用して、投稿トリガーをオーバーライドまたは使用することによって拡張機能を実行し、拡張プロシージャを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="bcf0d-141">Instead, use the CRT data service and do the extension either by overriding or using post triggers and then call your extended procedures.</span></span>

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

## <a name="adding-extensions"></a><span data-ttu-id="bcf0d-142">拡張機能の追加</span><span class="sxs-lookup"><span data-stu-id="bcf0d-142">Adding extensions</span></span>
1. <span data-ttu-id="bcf0d-143">すべての拡張機能テーブルは **UserRole** および **DeployExtensibilityRole** にアクセス許可を付与する必要があります。</span><span class="sxs-lookup"><span data-stu-id="bcf0d-143">All the extension tables should have grant permission on **UserRole** and **DeployExtensibilityRole**.</span></span>

    ```sql
    GRANT EXECUTE ON [ext].[EXTTABLENAME] TO [DeployExtensibilityRole];
        GO
        GRANT EXECUTE ON [ext].[EXTTABLENAME] TO [UsersRole];
        GO
    ```

2. <span data-ttu-id="bcf0d-144">テーブルが HQ から受信するデータを送信する場合、**DataSyncUsersRole** アクセス許可を付与します。</span><span class="sxs-lookup"><span data-stu-id="bcf0d-144">Grant **DataSyncUsersRole** permission if your table is going to send receive data from HQ.</span></span>

    ```sql
    GRANT SELECT, INSERT, UPDATE, DELETE ON OBJECT::[ext].[EXTTABLENAME] TO [DataSyncUsersRole]
    GO
    ```

3. <span data-ttu-id="bcf0d-145">拡張テーブルを作成し、HQ にデータを同期させる場合は、拡張テーブルに親テーブルの主な列を含めます。</span><span class="sxs-lookup"><span data-stu-id="bcf0d-145">If you are creating extended table and want to sync the data back to HQ, then have the primary column of the parent table in the extended table.</span></span>
4. <span data-ttu-id="bcf0d-146">たとえば、**ContosoRetailTransactionTable** など、常にテーブルに接頭語を付けると、他のパートナー/ISV カスタマイズとの競合を回避できます。</span><span class="sxs-lookup"><span data-stu-id="bcf0d-146">Always prefix your table, for example, **ContosoRetailTransactionTable**, so that you can avoid conflicts with other partner/ISV customizations.</span></span>

## <a name="attributes"></a><span data-ttu-id="bcf0d-147">属性</span><span class="sxs-lookup"><span data-stu-id="bcf0d-147">Attributes</span></span>

<span data-ttu-id="bcf0d-148">顧客、顧客の注文、現金売りトランザクション、およびコール センター注文の属性をサポートするために、HQ の属性フレームワークを拡張しました。</span><span class="sxs-lookup"><span data-stu-id="bcf0d-148">We extended the attribute framework in HQ to support attributes for Customers, Customer orders, cash and carry transactions and call center orders.</span></span>

### <a name="customer-attributes"></a><span data-ttu-id="bcf0d-149">顧客属性</span><span class="sxs-lookup"><span data-stu-id="bcf0d-149">Customer attributes</span></span>
<span data-ttu-id="bcf0d-150">新しい顧客属性フレームワークでは、構成を使用して、POS または HQ 内の顧客追加/編集画面または顧客詳細画面に新しいフィールドを追加することができます。</span><span class="sxs-lookup"><span data-stu-id="bcf0d-150">With the new customer attribute framework, you can use configurations to add new fields to the customer add/edit or customer details screens in POS or HQ.</span></span> <span data-ttu-id="bcf0d-151">小売パラメーターで顧客属性グループを構成した後、POS や HQ はコードの変更やカスタマイズを行わずに新しい属性を自動的に表示します。</span><span class="sxs-lookup"><span data-stu-id="bcf0d-151">After configuring the customer attribute group in retail parameters, POS and HQ will automatically show up the new attribute without any code change or customization.</span></span> <span data-ttu-id="bcf0d-152">画面レイアウト設計者は、取引画面 (**顧客** パネル) に顧客属性を表示するようにも設定されます。</span><span class="sxs-lookup"><span data-stu-id="bcf0d-152">The screen layout designer will also be configured to show the customer attributes in the transaction screen - **Customer** panel.</span></span>

### <a name="order-attributes"></a><span data-ttu-id="bcf0d-153">注文属性</span><span class="sxs-lookup"><span data-stu-id="bcf0d-153">Order attributes</span></span>
<span data-ttu-id="bcf0d-154">属性フレームワークは、現金売りトランザクション、顧客の注文、およびコール センター注文の属性をサポートするように拡張されました。</span><span class="sxs-lookup"><span data-stu-id="bcf0d-154">The attribute framework was extended to support attributes in cash and carry transactions, customer orders, and call center orders.</span></span> <span data-ttu-id="bcf0d-155">HQ または CRT で値を直接編集して設定することができます。</span><span class="sxs-lookup"><span data-stu-id="bcf0d-155">You can edit and set values directly in HQ or in CRT.</span></span> <span data-ttu-id="bcf0d-156">これらすべてはデータベースを変更せずにコンフィギュレーションを介して実行することができます。</span><span class="sxs-lookup"><span data-stu-id="bcf0d-156">All this can be done through configurations, without any database changes.</span></span> <span data-ttu-id="bcf0d-157">(基本的な CRUD 操作は必要ではなく、主要なビジネス ロジックの属性値をカスタマイズすることができます。) 以前は、これを行うには、HQ とチャンネル DB に新しいテーブルを作成し、CRT を変更する必要がありました。</span><span class="sxs-lookup"><span data-stu-id="bcf0d-157">(You can customization the attribute values for core business logic, not required for basic CRUD operations.) Previously, you had to create new tables in HQ and channel DB, and then modify CRT to do this.</span></span> <span data-ttu-id="bcf0d-158">現在は、すべての属性の作成をコンフィギュレーションを通じて実行できるようになりました。</span><span class="sxs-lookup"><span data-stu-id="bcf0d-158">Now all the attribute creation can be done through configuration.</span></span>

## <a name="adding-a-new-table"></a><span data-ttu-id="bcf0d-159">新しいテーブルの追加</span><span class="sxs-lookup"><span data-stu-id="bcf0d-159">Adding a new table</span></span>

<span data-ttu-id="bcf0d-160">このシナリオでは、新しいテーブルを作成し、チャネル DB に追加する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="bcf0d-160">In this scenario we will explain how to create a new table and add it to the channel DB.</span></span> <span data-ttu-id="bcf0d-161">すべての拡張コードは **ext スキーマ**へアクセスすることができます。</span><span class="sxs-lookup"><span data-stu-id="bcf0d-161">All extension code has access to the **ext schema**.</span></span>

1. <span data-ttu-id="bcf0d-162">SQL Server Management Studio デザイナーを使用するか、SQL スクリプトを使用して、**ext スキーマ**のチャネル データベースに新しいテーブルを作成します。</span><span class="sxs-lookup"><span data-stu-id="bcf0d-162">Create a new table in the channel database in the **ext schema** either using SQL Server Management Studio Designer or using SQL scripts.</span></span> <span data-ttu-id="bcf0d-163">以下は、SQL スクリプトの例です。</span><span class="sxs-lookup"><span data-stu-id="bcf0d-163">The following is an example SQL script.</span></span>

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

## <a name="adding-new-views-stored-procedure-functions-and-defined-types"></a><span data-ttu-id="bcf0d-164">新しいビュー、ストアド プロシージャ、関数、定義済タイプの追加</span><span class="sxs-lookup"><span data-stu-id="bcf0d-164">Adding new views, stored procedure, functions, and defined types</span></span>

<span data-ttu-id="bcf0d-165">すべての新しいストアド プロシージャ、ビューまたは機能は **ext スキーマ**に作成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="bcf0d-165">All new stored procedures, views or functions must be created in the **ext schema**.</span></span> <span data-ttu-id="bcf0d-166">手順、ビューまたは機能から、データベース コンポーネントをアクセスするまたは呼びだすことはやめてください。</span><span class="sxs-lookup"><span data-stu-id="bcf0d-166">Don't access or call our database artifacts from your procedures, views, or functions.</span></span>

## <a name="deployment-checks"></a><span data-ttu-id="bcf0d-167">配置のチェック</span><span class="sxs-lookup"><span data-stu-id="bcf0d-167">Deployment checks</span></span>

<span data-ttu-id="bcf0d-168">配置プロセスは、データベースのコンポーネントに変更があるかどうかを判断します。</span><span class="sxs-lookup"><span data-stu-id="bcf0d-168">The deployment process determines if there are any modification to the database artifacts.</span></span> <span data-ttu-id="bcf0d-169">CRT、AX、または DBO スキーマ オブジェクトを変更しようとした場合、またはどのシナリオの場合でも SQL でそれらに直接アクセスすると、展開は失敗します。</span><span class="sxs-lookup"><span data-stu-id="bcf0d-169">If you have attempted to modify the CRT, AX, or DBO schema objects, or access them for any scenario directly in SQL, then deployment will fail.</span></span>

## <a name="extension-scripts-and-deployment"></a><span data-ttu-id="bcf0d-170">拡張スクリプトおよび展開</span><span class="sxs-lookup"><span data-stu-id="bcf0d-170">Extension scripts and deployment</span></span>

<span data-ttu-id="bcf0d-171">チャンネル データベース拡張は、1 つまたは複数の T-SQL スクリプト ファイルを作成し、[展開可能なパッケージ](./retail-sdk/retail-sdk-packaging.md)に含めることで用意されます。</span><span class="sxs-lookup"><span data-stu-id="bcf0d-171">Channel Database extensions are provided by authoring one or more T-SQL script files and including them in a [deployable package](./retail-sdk/retail-sdk-packaging.md).</span></span> <span data-ttu-id="bcf0d-172">このプロセスについては、[Retail SDK](./retail-sdk/retail-sdk-overview.md) ドキュメントで説明します。</span><span class="sxs-lookup"><span data-stu-id="bcf0d-172">This process is described in the [Retail SDK](./retail-sdk/retail-sdk-overview.md) documentation.</span></span>

<span data-ttu-id="bcf0d-173">拡張スクリプト ファイルは、[T-SQL](https://docs.microsoft.com/sql/t-sql/language-reference) を使用して記述され、[Azure SQL データベース](https://docs.microsoft.com/azure/sql-database/sql-database-features)と互換性があります。</span><span class="sxs-lookup"><span data-stu-id="bcf0d-173">Extension script files must be written using [T-SQL](https://docs.microsoft.com/sql/t-sql/language-reference) and compatible with [Azure SQL Database](https://docs.microsoft.com/azure/sql-database/sql-database-features).</span></span>
<span data-ttu-id="bcf0d-174">スクリプト ファイルの末尾は *.sql* ファイル拡張子にする必要があります。その他のファイルは無視されます。または、パッケージングまたは配置障害を引き起こす可能性があります。</span><span class="sxs-lookup"><span data-stu-id="bcf0d-174">The script files must end with the *.sql* file extension, any other files will be ignored or may induce a packaging or deployment failure.</span></span> <span data-ttu-id="bcf0d-175">Retail Store Scale Unit または Modern POS の一部としてオフラインでチャネル データベース拡張機能を展開する場合、スクリプトは、それらのコンポーネントに対して使用される SQL Express または SQL Server のバージョンの両方またはいずれかと互換性があることも必要です。</span><span class="sxs-lookup"><span data-stu-id="bcf0d-175">If you intend to deploy your Channel Database extensions as part of Retail Store Scale Unit or Modern POS offline, the scripts must also be compatible with the version of SQL Express and/or SQL Server that will be used for those components.</span></span>

<span data-ttu-id="bcf0d-176">配置とインストール中、拡張子スクリプトは、スクリプト ファイル名に基づいたアルファベット順で実行されます。</span><span class="sxs-lookup"><span data-stu-id="bcf0d-176">During deployment and installation, the extension scripts are executed in alphabetical order based on the script file name.</span></span>
<span data-ttu-id="bcf0d-177">各スクリプトは、完了するまで実行され、拡張スクリプトの完了を追跡するため、メタデータ レコードはチャンネル データベースの CRT.RETAILUPGRADEHISTORY テーブルに追加されます。</span><span class="sxs-lookup"><span data-stu-id="bcf0d-177">Each script is run to completion and then a metadata record is added to the Channel Database's CRT.RETAILUPGRADEHISTORY table to track the completion of that extension script.</span></span>
<span data-ttu-id="bcf0d-178">そのメタデータ レコードが存在する場合、その後の展開で同じチャネル データベースに対してスクリプトが再度実行されることはありません。</span><span class="sxs-lookup"><span data-stu-id="bcf0d-178">The script will not be executed again for the same Channel Database in subsequent deployments if that metadata record is present.</span></span>
<span data-ttu-id="bcf0d-179">スクリプトが実行中に失敗し、正常に完了しない場合、そのメタデータは保存されず、以降の配置でスクリプトが再実行されます。</span><span class="sxs-lookup"><span data-stu-id="bcf0d-179">If a script fails during execution and does not complete successfully, its metadata will not be stored and the script will be rerun on subsequent deployments.</span></span>

<span data-ttu-id="bcf0d-180">展開やインストールが製品の更新と組み合わされている場合、拡張スクリプトは製品の更新後に実行されます。</span><span class="sxs-lookup"><span data-stu-id="bcf0d-180">If the deployment or installation is combined with an update of the product, the extension scripts are run after the product update.</span></span>

<span data-ttu-id="bcf0d-181">正常に行われるチャネル データベース拡張を作成するには、次のガイドラインに従う必要があります。</span><span class="sxs-lookup"><span data-stu-id="bcf0d-181">To author a successful Channel Database extension, you must adhere to the following guidelines.</span></span>

### <a name="use-a-naming-convention-that-ensures-stable-order-when-sorted-alphabetically"></a><span data-ttu-id="bcf0d-182">アルファベット順に並べ替えられたときに、安定した順序が確保される名前付け規則を使用します。</span><span class="sxs-lookup"><span data-stu-id="bcf0d-182">Use a naming convention that ensures stable order when sorted alphabetically</span></span>

<span data-ttu-id="bcf0d-183">拡張スクリプトは、ファイル名に基づくアルファベット順に実行されるので、並べ替えたときに正しい実行順序が使用される名前付け規則を確立する必要があります。</span><span class="sxs-lookup"><span data-stu-id="bcf0d-183">Because extension scripts are executed in alphabetical order based on the file name, you should establish a naming convention that ensures that the correct execution order is used when sorted.</span></span>

<span data-ttu-id="bcf0d-184">1 つの例は、次のパターンを持つファイルの名前付けです: "<ISO 8601 date>_<descriptio>.sql"。ここで **<ISO 8601 date>** は ISO 8601 形式の日付で、**<description>** はスクリプトの目的を識別するための説明のテキストです。</span><span class="sxs-lookup"><span data-stu-id="bcf0d-184">One example would be naming files with the following pattern: "<ISO 8601 date>_<descriptio>.sql", where **<ISO 8601 date>** is a ISO 8601 formatted date and **<description>** is descriptive text to identify the purpose of the script.</span></span>
<span data-ttu-id="bcf0d-185">たとえば、*"20180501_CustomerDetails.sql"* と *"20181102_CustomerDetailsIndex.sql"* などです。</span><span class="sxs-lookup"><span data-stu-id="bcf0d-185">For instance, *"20180501_CustomerDetails.sql"* and *"20181102_CustomerDetailsIndex.sql"*.</span></span>
<span data-ttu-id="bcf0d-186">前者は、「顧客の詳細」機能に関連する 2018 年 5 月 1 日に作成された拡張スクリプトを表しており、後者は、2018 年 11 月 2 日に作成された以前の機能に関連するインデックスに関連付けられている拡張スクリプトです。</span><span class="sxs-lookup"><span data-stu-id="bcf0d-186">The former would represent an extension script authored on May 1, 2018 that is related to "Customer Details" feature and the latter an extension script associated to indexes related to the previous feature authored on November 2, 2018.</span></span>

<span data-ttu-id="bcf0d-187">別の単純な方法は、"0001_CustomerDetails.sql" や "0002_CustomerDetailsIndex.sql" などの差分数値接頭語を使用する方法です。</span><span class="sxs-lookup"><span data-stu-id="bcf0d-187">Another simpler alternative is to use an incremental numeric prefix, such as "0001_CustomerDetails.sql" and "0002_CustomerDetailsIndex.sql".</span></span>

<span data-ttu-id="bcf0d-188">1 つのスクリプトが正常に実行される別のスクリプトに依存している場合、アルファベット順のファイル名が必要な実行順序と一致していることを確認する方法で命名する必要があります。</span><span class="sxs-lookup"><span data-stu-id="bcf0d-188">If one script depends on another having executed successfully, you must name then in a way that ensures that the file name in alphabetical order matches the required execution order.</span></span>

### <a name="do-not-alter-extension-scripts-that-have-been-published"></a><span data-ttu-id="bcf0d-189">発行された拡張スクリプトを変更しないでください。</span><span class="sxs-lookup"><span data-stu-id="bcf0d-189">Do not alter extension scripts that have been published</span></span>

<span data-ttu-id="bcf0d-190">展開可能なパッケージまたはチャンル データベース拡張スクリプトを含むインストーラー拡張をリリースした場合、それらのスクリプトを変更しないでください。</span><span class="sxs-lookup"><span data-stu-id="bcf0d-190">If you have released a deployable package or installer extension that contains Channel Database extension scripts, do not alter those scripts.</span></span> <span data-ttu-id="bcf0d-191">拡張スクリプトは、チャネル データベース インスタンスあたり 1 回だけ実行されます。</span><span class="sxs-lookup"><span data-stu-id="bcf0d-191">Extension scripts are run only once per Channel Database instance.</span></span>
<span data-ttu-id="bcf0d-192">既にスクリプトを発行しており、それらのスクリプトがチャネル データベースに対して実行済の場合、既に実行されたスクリプトへの変更はデータベースには適用されません。</span><span class="sxs-lookup"><span data-stu-id="bcf0d-192">If you alter published scripts and those scripts may have already been run against a Channel Database, the modifications to an already executed script will not be applied to the database.</span></span>

<span data-ttu-id="bcf0d-193">代わりに、新しいスクリプト ファイル内の変更を提供します。</span><span class="sxs-lookup"><span data-stu-id="bcf0d-193">Instead, provide the modifications in a new script file.</span></span> <span data-ttu-id="bcf0d-194">依存関係の後に実行されるように、上記の名前付け規則を検討してください。</span><span class="sxs-lookup"><span data-stu-id="bcf0d-194">Consider the naming convention noted above to ensure that it runs after its dependencies.</span></span>

### <a name="do-not-remove-old-extension-scripts-that-have-been-published"></a><span data-ttu-id="bcf0d-195">発行された以前の拡張スクリプトを削除しないでください。</span><span class="sxs-lookup"><span data-stu-id="bcf0d-195">Do not remove old extension scripts that have been published</span></span>

<span data-ttu-id="bcf0d-196">展開可能なパッケージまたはインストーラー拡張機能は、データベースの拡張機能の累積的な更新を表す必要があります。</span><span class="sxs-lookup"><span data-stu-id="bcf0d-196">Your deployable package or installer extension must represent a cumulative update for your database extensions.</span></span> <span data-ttu-id="bcf0d-197">拡張機能パッケージまたはインストーラーの以前のバージョンには依存関係はありません。</span><span class="sxs-lookup"><span data-stu-id="bcf0d-197">There should be no dependencies on previous versions of an extension package or installer.</span></span> <span data-ttu-id="bcf0d-198">ユーザーは、パッケージまたは拡張機能の以前のバージョンに依存しなくても拡張機能パッケージやインストーラーを適用できる必要があります。</span><span class="sxs-lookup"><span data-stu-id="bcf0d-198">A customer should be able to apply your extension package or installer without depending on a previous version of your package or extension.</span></span>

<span data-ttu-id="bcf0d-199">拡張スクリプトが展開可能なパッケージまたはインストーラー拡張の一部として公開されている場合、パッケージまたはインストーラーの以降の更新から削除しないでください。</span><span class="sxs-lookup"><span data-stu-id="bcf0d-199">If your extension scripts have been published as part of a deployable package or installer extension, do not remove them from subsequent updates in your package or installer.</span></span> <span data-ttu-id="bcf0d-200">災害復旧、アップグレード、スケール アウト シナリオに対応するため、チャンル データベースの新しいインスタンスを同じバージョンの最後に配置された拡張機能パッケージに持ち込むために拡張パッケージを使用できます。</span><span class="sxs-lookup"><span data-stu-id="bcf0d-200">To account for disaster recovery, upgrade and scale out scenarios, extension packages may be used to bring a new instance of the Channel Database to the same version of the last deployed extension package.</span></span>

### <a name="extension-scripts-must-be-idempotent-and-reentrant"></a><span data-ttu-id="bcf0d-201">拡張スクリプトは、非べき等および再入力である必要がある</span><span class="sxs-lookup"><span data-stu-id="bcf0d-201">Extension scripts must be idempotent and reentrant</span></span>

<span data-ttu-id="bcf0d-202">拡張スクリプトはチャネル データベースあたり 1 回だけ実行されますが、スクリプトはオーサリング エラーまたはタイムアウトやトランザクション デッドロックなどの一時的な SQL エラーが原因で実行されない場合があります。</span><span class="sxs-lookup"><span data-stu-id="bcf0d-202">Although extension scripts are run only once per Channel Database, scripts may fail due to authoring errors or transient SQL errors, like time outs or transaction deadlocks.</span></span> <span data-ttu-id="bcf0d-203">拡張スクリプトは、それらの障害シナリオに対応するため、非べき等および再入力である必要があります。</span><span class="sxs-lookup"><span data-stu-id="bcf0d-203">The extension scripts must be idempotent and reentrant to account for those failure scenarios.</span></span>
<span data-ttu-id="bcf0d-204">拡張スクリプトがエラーが原因で失敗した場合、再実行できます。</span><span class="sxs-lookup"><span data-stu-id="bcf0d-204">If the extension script fails due to any error, it may be rerun.</span></span> <span data-ttu-id="bcf0d-205">スクリプトを再実行しても、データベースに悪影響を及ぼしません。</span><span class="sxs-lookup"><span data-stu-id="bcf0d-205">Rerunning the script should not adversely affect the database.</span></span>

### <a name="do-not-assume-that-the-channel-database-data-is-perennial"></a><span data-ttu-id="bcf0d-206">チャネル データベース データが永続すると仮定しない</span><span class="sxs-lookup"><span data-stu-id="bcf0d-206">Do not assume that the Channel Database data is perennial</span></span>

<span data-ttu-id="bcf0d-207">チャネル データベースは、Retail サーバーで実行される操作の記憶域サポートを提供するトランザクション データベースです。</span><span class="sxs-lookup"><span data-stu-id="bcf0d-207">The Channel Database is a transactional database that provides storage support for operations performed by Retail Server.</span></span> <span data-ttu-id="bcf0d-208">長期間保存する必要があるチャネル データベースに格納されるすべてのデータは、[Commerce Data Exchange](./cdx-extensibility.md) を通じて本社にアップロードする必要があります。</span><span class="sxs-lookup"><span data-stu-id="bcf0d-208">All data that is stored in the Channel Database that must be kept for long periods of time must be uploaded to the headquarters through the [Commerce Data Exchange](./cdx-extensibility.md).</span></span> <span data-ttu-id="bcf0d-209">本社にアップロードされたデータには、[Commerce Data Exchange リアルタイム サービス](./extend-commerce-data-exchange.md)によりアクセスすることができます。</span><span class="sxs-lookup"><span data-stu-id="bcf0d-209">Data uploaded to the headquarters can be accessed by the [Commerce Data Exchange Real-time Service](./extend-commerce-data-exchange.md).</span></span>

### <a name="do-write-backward-compatible-channel-database-extensions"></a><span data-ttu-id="bcf0d-210">後方互換性のあるチャネルデータベースの拡張機能を作成する</span><span class="sxs-lookup"><span data-stu-id="bcf0d-210">Do write backward compatible channel database extensions</span></span>

<span data-ttu-id="bcf0d-211">チャネルデータベースには後方互換性がある必要があります。</span><span class="sxs-lookup"><span data-stu-id="bcf0d-211">The Channel Database is expected to be backward compatible.</span></span> <span data-ttu-id="bcf0d-212">これにより、チャネルデータベースのみを更新して Retail サーバー または POS の更新をしなかった場合でも、既存の Retail サーバー または POS 作業は正常に機能します。</span><span class="sxs-lookup"><span data-stu-id="bcf0d-212">This means that updating only the Channel Database without updating Retail Server or POS must not prevent existing Retail Server or POS operations from functioning correctly.</span></span> <span data-ttu-id="bcf0d-213">展開を行う過程で、 Retail Cloud Scale Unitの異なるコンポーネント、 Retail Store Scale Unit、Modern POS は、決まった順番で更新処理がされます。</span><span class="sxs-lookup"><span data-stu-id="bcf0d-213">During deployment flows, the different components of your Retail Cloud Scale Unit, Retail Store Scale Unit, and Modern POS are updated in the inverse other of dependency.</span></span> <span data-ttu-id="bcf0d-214">チャネルデータベースは、最初に更新されるコンポーネントであり、Retail サーバー や POS はその次に更新されることを意味します。</span><span class="sxs-lookup"><span data-stu-id="bcf0d-214">This means that the Channel Database is the first component to be updated, and Retail Server or POS are updated next.</span></span> <span data-ttu-id="bcf0d-215">Retail サーバー や POS は正常に更新されず、各コンポーネントはこの処理がされる前の状態までロールバックされます。</span><span class="sxs-lookup"><span data-stu-id="bcf0d-215">If Retail Server or POS fails to update successfully, those components are rolled back to restore them to their previous working state.</span></span> <span data-ttu-id="bcf0d-216">このような場合であっても、データの損失を防ぐためにチャネルデータベースはロールバックされません。</span><span class="sxs-lookup"><span data-stu-id="bcf0d-216">However, in such situations, the Channel Database is not rolled back to prevent data loss.</span></span> <span data-ttu-id="bcf0d-217">ご利用の拡張機能に後方互換性がない場合、正常な展開処理が完了するまでは、これら拡張機能が正しく動作しない可能性があります。</span><span class="sxs-lookup"><span data-stu-id="bcf0d-217">If your extensions are not backward compatible, they may fail to work properly until a successful deployment is performed.</span></span>
