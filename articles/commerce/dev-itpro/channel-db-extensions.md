---
title: チャネル データベース 拡張機能
description: このトピックでは、チャネル データベースを拡張する方法について説明します。
author: mugunthanm
manager: AnnBe
ms.date: 06/18/2020
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
ms.openlocfilehash: bb59a4f540b2c4a29e505867af8fef7f02c539da
ms.sourcegitcommit: 6bf8602333191e5161ba3a9ceecf160c85ff7e79
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/19/2020
ms.locfileid: "3484331"
---
# <a name="channel-database-extensions"></a><span data-ttu-id="fec4c-103">チャネル データベース 拡張機能</span><span class="sxs-lookup"><span data-stu-id="fec4c-103">Channel database extensions</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="fec4c-104">チャネル データベース (チャネル DB) は、オンライン ストアまたは従来型の店舗などの 1 つまたは複数のコマース チャネルからのトランザクションおよびマスター データを保持します。</span><span class="sxs-lookup"><span data-stu-id="fec4c-104">The channel database (channel DB) holds transactional and master data from one or more commerce channels, such as an online store or a brick-and-mortar store.</span></span> <span data-ttu-id="fec4c-105">マスター データは Commerce Data Exchange (CDX) を使用して、バックオフィス (HQ) からチャネル データベースにプッシュ ダウンされます。</span><span class="sxs-lookup"><span data-stu-id="fec4c-105">The master data is pushed down from the Headquarters (HQ) to the channel database using the commerce data exchange (CDX).</span></span> <span data-ttu-id="fec4c-106">チャネル データベースに格納されたトランザクション データは、CDX を使用して本社に引き戻されます。</span><span class="sxs-lookup"><span data-stu-id="fec4c-106">The transactional data stored in the channel database is pulled back to the headquarters using the CDX.</span></span>

<span data-ttu-id="fec4c-107">このトピックでは、さまざまなシナリオのチャネル データベースを拡張する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="fec4c-107">In this topic we explain how to extend the channel database for different scenarios.</span></span> <span data-ttu-id="fec4c-108">この手順は、Dynamics 365 Finance および Commerce にのみ適用されるものです。</span><span class="sxs-lookup"><span data-stu-id="fec4c-108">The steps here apply only to Dynamics 365 Finance and Commerce.</span></span>

<span data-ttu-id="fec4c-109">拡張機能のさまざまなシナリオを説明する前に、チャネル DB 拡張機能の最新の機能拡張を理解することが重要です。</span><span class="sxs-lookup"><span data-stu-id="fec4c-109">Before discussing the different scenarios for extension, it's important to understand the recent enhancements to channel DB extensions.</span></span>

<span data-ttu-id="fec4c-110">アップグレード時の拡張機能の処理の方法にいくつかの改善を加えました。</span><span class="sxs-lookup"><span data-stu-id="fec4c-110">We have made some improvements to how extensions are handled during an upgrade.</span></span> <span data-ttu-id="fec4c-111">以下の環境構成のいずれかを使用することをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="fec4c-111">We recommend using one of the following environment configurations:</span></span>
- <span data-ttu-id="fec4c-112">Microsoft Dynamics 365 for Finance and Operations, Enterprise edition (2017 年 7 月) およびアプリケーション更新プログラム 5</span><span class="sxs-lookup"><span data-stu-id="fec4c-112">Microsoft Dynamics 365 for Finance and Operations, Enterprise edition (July 2017) with application update 5.</span></span>
- <span data-ttu-id="fec4c-113">Microsoft Dynamics 365 Retail 7.2 およびアプリケーション更新プログラム 5 はすぐに入手できるようになります。</span><span class="sxs-lookup"><span data-stu-id="fec4c-113">Microsoft Dynamics 365 Retail 7.2 with application update 5, which will be available soon.</span></span>
- <span data-ttu-id="fec4c-114">Microsoft Dynamics 365 Retail 7.3 はアプリケーション更新プログラム 5 を含みます。</span><span class="sxs-lookup"><span data-stu-id="fec4c-114">Microsoft Dynamics 365 Retail 7.3, which includes application update 5.</span></span>
- <span data-ttu-id="fec4c-115">Microsoft Dynamics 365 for Finance and Operations 7.3 (アプリケーション更新プログラム 5 を含みます)</span><span class="sxs-lookup"><span data-stu-id="fec4c-115">Microsoft Dynamics 365 for Finance and Operations 7.3, which includes application update 5.</span></span>

## <a name="ext-schema"></a><span data-ttu-id="fec4c-116">Ext スキーマ</span><span class="sxs-lookup"><span data-stu-id="fec4c-116">Ext schema</span></span>

<span data-ttu-id="fec4c-117">Finance と Commerce では、拡張機能をサポートするため、**ext スキーマ** と呼ばれる新たなスキーマを導入しました。</span><span class="sxs-lookup"><span data-stu-id="fec4c-117">In Finance and Commerce there is a now schema called the **ext schema** to support extensions.</span></span> <span data-ttu-id="fec4c-118">以前のバージョンでは、チャネル DB に拡張機能を追加する場合、CRT または AX スキーマに追加していました。</span><span class="sxs-lookup"><span data-stu-id="fec4c-118">In previous versions, if you wanted to add an extension to channel DB, you would add it to the CRT or AX schema.</span></span> <span data-ttu-id="fec4c-119">Finance と Commerce のいずれでも、CRT、AX や DBO スキーマを変更することはできません。</span><span class="sxs-lookup"><span data-stu-id="fec4c-119">In both Finance and Commerce, you cannot change the CRT, AX, or DBO schemas.</span></span> <span data-ttu-id="fec4c-120">すべての変更は **ext スキーマ**で行う必要があります。</span><span class="sxs-lookup"><span data-stu-id="fec4c-120">All changes must be made in the **ext schema**.</span></span> <span data-ttu-id="fec4c-121">CRT または AX スキーマの何かを変更すると、Lifecycle Services (LCS) での展開に失敗します。</span><span class="sxs-lookup"><span data-stu-id="fec4c-121">If you modify anything in the CRT or AX schemas, then deployment in Lifecycle Services (LCS) will fail.</span></span> <span data-ttu-id="fec4c-122">CRT、AX、および DBO スキーマを変更する権限がありません、というエラーが表示されます。</span><span class="sxs-lookup"><span data-stu-id="fec4c-122">An error message states that you don’t have permission to modify the CRT, AX, and DBO schemas.</span></span> <span data-ttu-id="fec4c-123">拡張機能には、展開の過程で CRT、AX、や DBO のスキーマ定義を読み取るアクセス許可がありません。 CRT、AX、や DBO のスキーマ定義を読み取る拡張スクリプトにクエリを含めないでください 。</span><span class="sxs-lookup"><span data-stu-id="fec4c-123">Extensions will not have permission to read the CRT, AX, and DBO schema definition during deployment, do not include any queries in the extension script to read the CRT, AX, and DBO schema definition.</span></span> 

> [!NOTE]
> <span data-ttu-id="fec4c-124">いずれかのチャネル DB フィールドの長さを伸ばす場合は、LCS で拡張機能の要求を作成し、EDT の伸長または小数点以下の精度を高める必要があります。</span><span class="sxs-lookup"><span data-stu-id="fec4c-124">If you want to increase any channel DB field length, you must create an extensibility request in LCS, increasing the EDT length or decimal precision.</span></span> <span data-ttu-id="fec4c-125">変更はチャネル DB に自動的にプッシュされません。また、拡張子には、チャネル DB - CRT、AX、または DBO スキーマでなにかを変更または修正するための許可は付与されません。</span><span class="sxs-lookup"><span data-stu-id="fec4c-125">Changes will not be automatically pushed to the channel DB, and extensions will not have permissions to change or modify anything in the channel DB - CRT, AX or DBO schema.</span></span> <span data-ttu-id="fec4c-126">CRT または AX スキーマの何かを変更すると、LCS での展開が失敗します。</span><span class="sxs-lookup"><span data-stu-id="fec4c-126">If you modify anything in the CRT or AX schemas, then deployment in LCS will fail.</span></span>

## <a name="best-practices-for-channel-db-extensions"></a><span data-ttu-id="fec4c-127">チャネル DB 拡張機能のためのベスト プラクティス</span><span class="sxs-lookup"><span data-stu-id="fec4c-127">Best practices for channel DB extensions</span></span>

- <span data-ttu-id="fec4c-128">CRT、AX、または DBO スキーマのいずれも変更しないでください。</span><span class="sxs-lookup"><span data-stu-id="fec4c-128">Don’t modify anything in the CRT, AX, or DBO schemas.</span></span> <span data-ttu-id="fec4c-129">すべての拡張シナリオで **ext スキーマ**を使用します。</span><span class="sxs-lookup"><span data-stu-id="fec4c-129">Use the **ext schema** for all extension scenarios.</span></span>
- <span data-ttu-id="fec4c-130">使用可能な場合は、CRT、AX、または DBO オブジェクトからチャネル データベース コンポーネントに直接アクセスするのではなく、Commerce Runtime データ サービスを介してデータを取得することをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="fec4c-130">If available, we recommend getting data through commerce runtime data services, as opposed to accessing channel DB artifacts directly from CRT, AX, or DBO objects.</span></span>

### <a name="dont-do-this"></a><span data-ttu-id="fec4c-131">このようにしない</span><span class="sxs-lookup"><span data-stu-id="fec4c-131">Don't do this</span></span>
<span data-ttu-id="fec4c-132">以下はユーザーがしてはいけないことの例です。</span><span class="sxs-lookup"><span data-stu-id="fec4c-132">The following is an example of what you should not do.</span></span> <span data-ttu-id="fec4c-133">代わりに、主キーの値を取得するために CRT データ サービスを使用してから、拡張テーブルに挿入するために主キーの値を使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="fec4c-133">Instead, you should use the CRT data service to get the primary key value and then use the primary key to insert into your extension table.</span></span>

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


### <a name="dont-do-this"></a><span data-ttu-id="fec4c-134">このようにしない</span><span class="sxs-lookup"><span data-stu-id="fec4c-134">Don't do this</span></span>
- <span data-ttu-id="fec4c-135">CRT、AX、またはDBO スキーマに新しい拡張テーブル、ビュー、または手順を作成しないでください。</span><span class="sxs-lookup"><span data-stu-id="fec4c-135">Don't create any new extension tables, views, or procs in crt, ax, or dbo schema.</span></span> <span data-ttu-id="fec4c-136">すべての拡張コンポーネントは、ext スキーマで実行する必要があります。</span><span class="sxs-lookup"><span data-stu-id="fec4c-136">All extension artifacts must be done in ext schema.</span></span> 
- <span data-ttu-id="fec4c-137">ext スキーマでは、CRT、AX、またはDBO スキーマのデータ型を使用しないでください。</span><span class="sxs-lookup"><span data-stu-id="fec4c-137">Don't use any of the crt, ax or dbo schema data types in ext schema.</span></span> <span data-ttu-id="fec4c-138">ext スキーマのカスタム タイプを作成して使用してください。</span><span class="sxs-lookup"><span data-stu-id="fec4c-138">Create custom types in ext schema and use it.</span></span>
- <span data-ttu-id="fec4c-139">ビュー、手順、関数、またはデータベース コンポーネントを修正しないでください。</span><span class="sxs-lookup"><span data-stu-id="fec4c-139">Don’t modify any views, procedures, functions, or any of the database artifacts.</span></span>
- <span data-ttu-id="fec4c-140">可能な場合は、拡張機能からのデータベース コンポーネントへのアクセスや呼び出しは回避してください。</span><span class="sxs-lookup"><span data-stu-id="fec4c-140">Avoid accessing or calling database artifacts from your extensions, if possible.</span></span> <span data-ttu-id="fec4c-141">代わりに、CRT データ サービスを使用してデータを取得します。</span><span class="sxs-lookup"><span data-stu-id="fec4c-141">Instead, use the CRT data service to get data.</span></span> <span data-ttu-id="fec4c-142">データ サービスを使用する利点は、今後データベース スキーマに重大な変更が行われた場合でも、SLA まで継続的にサポートされることです。</span><span class="sxs-lookup"><span data-stu-id="fec4c-142">The benefits of using the data service are that it will continue to be supported until the SLA, even if breaking changes are made to the database schema in the future.</span></span> <span data-ttu-id="fec4c-143">ただし、必要なデータを公開しない CRT データ サービスのインスタンスもあります。</span><span class="sxs-lookup"><span data-stu-id="fec4c-143">However, there will be instances in which the CRT data service does not expose the data that you need.</span></span> <span data-ttu-id="fec4c-144">このような場合、チャネル データベース コンポーネントに結合するビューを作成することによって、このデータにアクセスすることができます。</span><span class="sxs-lookup"><span data-stu-id="fec4c-144">In these cases, it is still possible to access this data by creating a view which joins on a channel DB artifact.</span></span> <span data-ttu-id="fec4c-145">ビューの作成は、CRT 拡張機能を使用してメモリ内で行うのではなく、データベース レベルで必要な形式のデータを構築する強力なツールになります。</span><span class="sxs-lookup"><span data-stu-id="fec4c-145">Creating views can be a powerful tool to structure the data in a format you need at a database level, as opposed to doing it in memory through CRT extensions.</span></span>
- <span data-ttu-id="fec4c-146">DBO スキーマ オブジェクトは Commerce scale unit の展開では使用できないため、拡張スクリプトから dbo.objects にはアクセスしないでください。</span><span class="sxs-lookup"><span data-stu-id="fec4c-146">Don't access any dbo.objects from extension scripts because dbo schema objects will not be available in Commerce scale unit deployments.</span></span>


```sql
CREATE VIEW [ext].[CONTOSORETAILSTOREHOURSVIEW] AS
(
    SELECT
    sdht.DAY,
    sdht.OPENTIME,
    sdht.CLOSINGTIME,
    sdht.RECID,
    rst.STORENUMBER
    FROM [ext].[CONTOSORETAILSTOREHOURSTABLE] sdht
    INNER JOIN [ax].RETAILSTORETABLE rst ON rst.RECID = sdht.RETAILSTORETABLE
)
```

## <a name="adding-extensions"></a><span data-ttu-id="fec4c-147">拡張機能の追加</span><span class="sxs-lookup"><span data-stu-id="fec4c-147">Adding extensions</span></span>

1. <span data-ttu-id="fec4c-148">すべての拡張テーブルの列には、NOT NULL の制約を適用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="fec4c-148">All extension table columns must have the NOT NULL constraint enforced.</span></span> <span data-ttu-id="fec4c-149">更新の過程で、列の値が空白で更新され、NULL の値が正しく処理されない場合は、 CRT でランタイムの例外処理が発生する可能性があります。</span><span class="sxs-lookup"><span data-stu-id="fec4c-149">During upgrade, if the column value is blank it will be updated with NULL values and it may cause a runtime exception in CRT if the null value is not handled properly.</span></span>
2. <span data-ttu-id="fec4c-150">すべての拡張機能テーブルは **UserRole** および **DeployExtensibilityRole** にアクセス許可を付与する必要があります。</span><span class="sxs-lookup"><span data-stu-id="fec4c-150">All the extension tables should have grant permission on **UserRole** and **DeployExtensibilityRole**.</span></span>

    ```sql
    --Tables:

    GRANT SELECT, INSERT, UPDATE, DELETE ON OBJECT::[ext].[RETAILCUSTPREFERENCE] TO [UsersRole]
    GO
    
    GRANT SELECT, INSERT, UPDATE, DELETE ON OBJECT::[ext].[RETAILCUSTPREFERENCE] TO [DeployExtensibilityRole]
    GO
    
    --Stored procedures: 
    
    GRANT EXECUTE ON [ext].[EXTSTOREDPROCEDURE] TO [UsersRole];
    GO
    
    GRANT EXECUTE ON [ext].[EXTSTOREDPROCEDURE] TO [PublishersRole];
    GO
    
    GRANT EXECUTE ON [ext].[EXTSTOREDPROCEDURE] TO [DeployExtensibilityRole];
    GO
    ```

3. <span data-ttu-id="fec4c-151">テーブルが HQ からデータを送受信する場合は、 **DataSyncUsersRole** のアクセス許可を付与します。</span><span class="sxs-lookup"><span data-stu-id="fec4c-151">Grant **DataSyncUsersRole** permission if your table is going to send or receive data from HQ.</span></span>

    ```sql
    GRANT SELECT, INSERT, UPDATE, DELETE, ALTER ON OBJECT::[ext].[EXTTABLENAME] TO [DataSyncUsersRole]
    GO
    ```

4. <span data-ttu-id="fec4c-152">拡張テーブルを作成し、HQ にデータを同期させる場合は、拡張テーブルに親テーブルの主となる列を含めます。</span><span class="sxs-lookup"><span data-stu-id="fec4c-152">If you are creating an extended table and want to sync the data back to HQ, you need to have the primary column of the parent table in the extended table.</span></span>
5. <span data-ttu-id="fec4c-153">たとえば、 **ContosoRetailTransactionTable** などのように、常にテーブルに接頭語を付けると、他のカスタマイズとの競合を回避できます。</span><span class="sxs-lookup"><span data-stu-id="fec4c-153">Always prefix your table, for example **ContosoRetailTransactionTable**, so that you can avoid conflicts with other customizations.</span></span>

## <a name="attributes"></a><span data-ttu-id="fec4c-154">属性</span><span class="sxs-lookup"><span data-stu-id="fec4c-154">Attributes</span></span>

<span data-ttu-id="fec4c-155">顧客、顧客の注文、現金売りトランザクション、およびコール センター注文の属性をサポートするために、HQ の属性フレームワークを拡張しました。</span><span class="sxs-lookup"><span data-stu-id="fec4c-155">We extended the attribute framework in HQ to support attributes for Customers, Customer orders, cash and carry transactions and call center orders.</span></span>

### <a name="customer-attributes"></a><span data-ttu-id="fec4c-156">顧客属性</span><span class="sxs-lookup"><span data-stu-id="fec4c-156">Customer attributes</span></span>
<span data-ttu-id="fec4c-157">新しい顧客属性フレームワークでは、構成を使用して、POS または HQ 内の顧客追加/編集画面または顧客詳細画面に新しいフィールドを追加することができます。</span><span class="sxs-lookup"><span data-stu-id="fec4c-157">With the new customer attribute framework, you can use configurations to add new fields to the customer add/edit or customer details screens in POS or HQ.</span></span> <span data-ttu-id="fec4c-158">コマース パラメーターで顧客属性グループを構成した後、POS や HQ はコードの変更やカスタマイズを行わずに新しい属性を自動的に表示します。</span><span class="sxs-lookup"><span data-stu-id="fec4c-158">After configuring the customer attribute group in commerce parameters, POS and HQ will automatically show up the new attribute without any code change or customization.</span></span> <span data-ttu-id="fec4c-159">画面レイアウト設計者は、取引画面 (**顧客** パネル) に顧客属性を表示するようにも設定されます。</span><span class="sxs-lookup"><span data-stu-id="fec4c-159">The screen layout designer will also be configured to show the customer attributes in the transaction screen - **Customer** panel.</span></span>

### <a name="order-attributes"></a><span data-ttu-id="fec4c-160">注文属性</span><span class="sxs-lookup"><span data-stu-id="fec4c-160">Order attributes</span></span>
<span data-ttu-id="fec4c-161">属性フレームワークは、現金売りトランザクション、顧客の注文、およびコール センター注文の属性をサポートするように拡張されました。</span><span class="sxs-lookup"><span data-stu-id="fec4c-161">The attribute framework was extended to support attributes in cash and carry transactions, customer orders, and call center orders.</span></span> <span data-ttu-id="fec4c-162">HQ または CRT で値を直接編集して設定することができます。</span><span class="sxs-lookup"><span data-stu-id="fec4c-162">You can edit and set values directly in HQ or in CRT.</span></span> <span data-ttu-id="fec4c-163">これらすべてはデータベースを変更せずにコンフィギュレーションを介して実行することができます。</span><span class="sxs-lookup"><span data-stu-id="fec4c-163">All this can be done through configurations, without any database changes.</span></span> <span data-ttu-id="fec4c-164">(基本的な CRUD 操作は必要ではなく、主要なビジネス ロジックの属性値をカスタマイズすることができます。) 以前は、これを行うには、HQ とチャンネル DB に新しいテーブルを作成し、CRT を変更する必要がありました。</span><span class="sxs-lookup"><span data-stu-id="fec4c-164">(You can customization the attribute values for core business logic, not required for basic CRUD operations.) Previously, you had to create new tables in HQ and channel DB, and then modify CRT to do this.</span></span> <span data-ttu-id="fec4c-165">現在は、すべての属性の作成をコンフィギュレーションを通じて実行できるようになりました。</span><span class="sxs-lookup"><span data-stu-id="fec4c-165">Now all the attribute creation can be done through configuration.</span></span>

## <a name="adding-a-new-table"></a><span data-ttu-id="fec4c-166">新しいテーブルの追加</span><span class="sxs-lookup"><span data-stu-id="fec4c-166">Adding a new table</span></span>

<span data-ttu-id="fec4c-167">このシナリオでは、新しいテーブルを作成し、チャネル DB に追加する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="fec4c-167">In this scenario we will explain how to create a new table and add it to the channel DB.</span></span> <span data-ttu-id="fec4c-168">すべての拡張コードは **ext スキーマ**へアクセスすることができます。</span><span class="sxs-lookup"><span data-stu-id="fec4c-168">All extension code has access to the **ext schema**.</span></span>

- <span data-ttu-id="fec4c-169">SQL Server Management Studio デザイナーを使用するか、SQL スクリプトを使用して、**ext スキーマ**のチャネル データベースに新しいテーブルを作成します。</span><span class="sxs-lookup"><span data-stu-id="fec4c-169">Create a new table in the channel database in the **ext schema** either using SQL Server Management Studio Designer or using SQL scripts.</span></span> <span data-ttu-id="fec4c-170">以下は、SQL スクリプトの例です。</span><span class="sxs-lookup"><span data-stu-id="fec4c-170">The following is an example SQL script.</span></span>

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
    [REPLICATIONCOUNTERFROMORIGIN] [int] IDENTITY(1,1) NOT NULL,
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

> [!NOTE]
> If the new extension table data needs to be pulled to Retail headquarters using Commerce Data Exchange (CDX), then the extension table must include the REPLICATIONCOUNTERFROMORIGIN identity column ([REPLICATIONCOUNTERFROMORIGIN] [int] IDENTITY(1,1) NOT NULL,). This is required for a CDX pull job. REPLICATIONCOUNTERFROMORIGIN is not required if the data is pushed from Retail headquarters to channel database, this is only needed if the data is pulled from channel database to Retail headquarters.

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

## <a name="adding-new-views-stored-procedure-functions-and-defined-types"></a><span data-ttu-id="fec4c-171">新しいビュー、ストアド プロシージャ、関数、定義済タイプの追加</span><span class="sxs-lookup"><span data-stu-id="fec4c-171">Adding new views, stored procedure, functions, and defined types</span></span>

<span data-ttu-id="fec4c-172">すべての新しいストアド プロシージャ、ビューまたは機能は **ext スキーマ**に作成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="fec4c-172">All new stored procedures, views or functions must be created in the **ext schema**.</span></span> <span data-ttu-id="fec4c-173">手順、ビューまたは機能から、データベース コンポーネントをアクセスするまたは呼びだすことはやめてください。</span><span class="sxs-lookup"><span data-stu-id="fec4c-173">Don't access or call our database artifacts from your procedures, views, or functions.</span></span>

## <a name="deployment-checks"></a><span data-ttu-id="fec4c-174">配置のチェック</span><span class="sxs-lookup"><span data-stu-id="fec4c-174">Deployment checks</span></span>

<span data-ttu-id="fec4c-175">配置プロセスは、データベースのコンポーネントに変更があるかどうかを判断します。</span><span class="sxs-lookup"><span data-stu-id="fec4c-175">The deployment process determines if there are any modification to the database artifacts.</span></span> <span data-ttu-id="fec4c-176">CRT、AX、または DBO スキーマ オブジェクトを変更しようとした場合、またはどのシナリオの場合でも SQL でそれらに直接アクセスすると、展開は失敗します。</span><span class="sxs-lookup"><span data-stu-id="fec4c-176">If you have attempted to modify the CRT, AX, or DBO schema objects, or access them for any scenario directly in SQL, then deployment will fail.</span></span>

## <a name="extension-scripts-and-deployment"></a><span data-ttu-id="fec4c-177">拡張スクリプトおよび展開</span><span class="sxs-lookup"><span data-stu-id="fec4c-177">Extension scripts and deployment</span></span>

<span data-ttu-id="fec4c-178">チャンネル データベース拡張は、1 つまたは複数の T-SQL スクリプト ファイルを作成し、[展開可能なパッケージ](./retail-sdk/retail-sdk-packaging.md)に含めることで用意されます。</span><span class="sxs-lookup"><span data-stu-id="fec4c-178">Channel Database extensions are provided by authoring one or more T-SQL script files and including them in a [deployable package](./retail-sdk/retail-sdk-packaging.md).</span></span> <span data-ttu-id="fec4c-179">このプロセスについては、[Retail SDK](./retail-sdk/retail-sdk-overview.md) ドキュメントで説明します。</span><span class="sxs-lookup"><span data-stu-id="fec4c-179">This process is described in the [Retail SDK](./retail-sdk/retail-sdk-overview.md) documentation.</span></span>

<span data-ttu-id="fec4c-180">拡張スクリプト ファイルは、[T-SQL](https://docs.microsoft.com/sql/t-sql/language-reference) を使用して記述され、[Azure SQL データベース](https://docs.microsoft.com/azure/sql-database/sql-database-features)と互換性があります。</span><span class="sxs-lookup"><span data-stu-id="fec4c-180">Extension script files must be written using [T-SQL](https://docs.microsoft.com/sql/t-sql/language-reference) and compatible with [Azure SQL Database](https://docs.microsoft.com/azure/sql-database/sql-database-features).</span></span>
<span data-ttu-id="fec4c-181">スクリプト ファイルの末尾は *.sql* ファイル拡張子にする必要があります。その他のファイルは無視されます。または、パッケージングまたは配置障害を引き起こす可能性があります。</span><span class="sxs-lookup"><span data-stu-id="fec4c-181">The script files must end with the *.sql* file extension, any other files will be ignored or may induce a packaging or deployment failure.</span></span> <span data-ttu-id="fec4c-182">Commerce Scale Unit または Modern POS オフラインの一部としてチャネル データベース拡張機能を展開する場合、スクリプトは、それらのコンポーネントに対して使用される SQL Express または SQL Server のバージョンの両方またはいずれかと互換性があることも必要です。</span><span class="sxs-lookup"><span data-stu-id="fec4c-182">If you intend to deploy your Channel Database extensions as part of Commerce Scale Unit or Modern POS offline, the scripts must also be compatible with the version of SQL Express and/or SQL Server that will be used for those components.</span></span>

<span data-ttu-id="fec4c-183">配置とインストール中、拡張子スクリプトは、スクリプト ファイル名に基づいたアルファベット順で実行されます。</span><span class="sxs-lookup"><span data-stu-id="fec4c-183">During deployment and installation, the extension scripts are executed in alphabetical order based on the script file name.</span></span>
<span data-ttu-id="fec4c-184">各スクリプトは、完了するまで実行され、拡張スクリプトの完了を追跡するため、メタデータ レコードはチャンネル データベースの CRT.RETAILUPGRADEHISTORY テーブルに追加されます。</span><span class="sxs-lookup"><span data-stu-id="fec4c-184">Each script is run to completion and then a metadata record is added to the Channel Database's CRT.RETAILUPGRADEHISTORY table to track the completion of that extension script.</span></span>
<span data-ttu-id="fec4c-185">そのメタデータ レコードが存在する場合、その後の展開で同じチャネル データベースに対してスクリプトが再度実行されることはありません。</span><span class="sxs-lookup"><span data-stu-id="fec4c-185">The script will not be executed again for the same Channel Database in subsequent deployments if that metadata record is present.</span></span>
<span data-ttu-id="fec4c-186">スクリプトが実行中に失敗し、正常に完了しない場合、そのメタデータは保存されず、以降の配置でスクリプトが再実行されます。</span><span class="sxs-lookup"><span data-stu-id="fec4c-186">If a script fails during execution and does not complete successfully, its metadata will not be stored and the script will be rerun on subsequent deployments.</span></span>

<span data-ttu-id="fec4c-187">展開やインストールが製品の更新と組み合わされている場合、拡張スクリプトは製品の更新後に実行されます。</span><span class="sxs-lookup"><span data-stu-id="fec4c-187">If the deployment or installation is combined with an update of the product, the extension scripts are run after the product update.</span></span>

<span data-ttu-id="fec4c-188">正常に行われるチャネル データベース拡張を作成するには、次のガイドラインに従う必要があります。</span><span class="sxs-lookup"><span data-stu-id="fec4c-188">To author a successful Channel Database extension, you must adhere to the following guidelines.</span></span>

### <a name="use-a-naming-convention-that-ensures-stable-order-when-sorted-alphabetically"></a><span data-ttu-id="fec4c-189">アルファベット順に並べ替えられたときに、安定した順序が確保される名前付け規則を使用します。</span><span class="sxs-lookup"><span data-stu-id="fec4c-189">Use a naming convention that ensures stable order when sorted alphabetically</span></span>

<span data-ttu-id="fec4c-190">拡張スクリプトは、ファイル名に基づくアルファベット順に実行されるので、並べ替えたときに正しい実行順序が使用される名前付け規則を確立する必要があります。</span><span class="sxs-lookup"><span data-stu-id="fec4c-190">Because extension scripts are executed in alphabetical order based on the file name, you should establish a naming convention that ensures that the correct execution order is used when sorted.</span></span>

<span data-ttu-id="fec4c-191">1 つの例は、次のパターンを持つファイルの名前付けです: "<ISO 8601 date>_<descriptio>.sql"。ここで **<ISO 8601 date>** は ISO 8601 形式の日付で、**<description>** はスクリプトの目的を識別するための説明のテキストです。</span><span class="sxs-lookup"><span data-stu-id="fec4c-191">One example would be naming files with the following pattern: "<ISO 8601 date>_<descriptio>.sql", where **<ISO 8601 date>** is a ISO 8601 formatted date and **<description>** is descriptive text to identify the purpose of the script.</span></span>
<span data-ttu-id="fec4c-192">たとえば、*"20180501_CustomerDetails.sql"* と *"20181102_CustomerDetailsIndex.sql"* などです。</span><span class="sxs-lookup"><span data-stu-id="fec4c-192">For instance, *"20180501_CustomerDetails.sql"* and *"20181102_CustomerDetailsIndex.sql"*.</span></span>
<span data-ttu-id="fec4c-193">前者は、「顧客の詳細」機能に関連する 2018 年 5 月 1 日に作成された拡張スクリプトを表しており、後者は、2018 年 11 月 2 日に作成された以前の機能に関連するインデックスに関連付けられている拡張スクリプトです。</span><span class="sxs-lookup"><span data-stu-id="fec4c-193">The former would represent an extension script authored on May 1, 2018 that is related to "Customer Details" feature and the latter an extension script associated to indexes related to the previous feature authored on November 2, 2018.</span></span>

<span data-ttu-id="fec4c-194">別の単純な方法は、"0001_CustomerDetails.sql" や "0002_CustomerDetailsIndex.sql" などの差分数値接頭語を使用する方法です。</span><span class="sxs-lookup"><span data-stu-id="fec4c-194">Another simpler alternative is to use an incremental numeric prefix, such as "0001_CustomerDetails.sql" and "0002_CustomerDetailsIndex.sql".</span></span>

<span data-ttu-id="fec4c-195">1 つのスクリプトが正常に実行される別のスクリプトに依存している場合、アルファベット順のファイル名が必要な実行順序と一致していることを確認する方法で命名する必要があります。</span><span class="sxs-lookup"><span data-stu-id="fec4c-195">If one script depends on another having executed successfully, you must name then in a way that ensures that the file name in alphabetical order matches the required execution order.</span></span>

### <a name="do-not-alter-extension-scripts-that-have-been-published"></a><span data-ttu-id="fec4c-196">発行された拡張スクリプトを変更しないでください。</span><span class="sxs-lookup"><span data-stu-id="fec4c-196">Do not alter extension scripts that have been published</span></span>

<span data-ttu-id="fec4c-197">展開可能なパッケージまたはチャンル データベース拡張スクリプトを含むインストーラー拡張をリリースした場合、それらのスクリプトを変更しないでください。</span><span class="sxs-lookup"><span data-stu-id="fec4c-197">If you have released a deployable package or installer extension that contains Channel Database extension scripts, do not alter those scripts.</span></span> <span data-ttu-id="fec4c-198">拡張スクリプトは、チャネル データベース インスタンスあたり 1 回だけ実行されます。</span><span class="sxs-lookup"><span data-stu-id="fec4c-198">Extension scripts are run only once per Channel Database instance.</span></span>
<span data-ttu-id="fec4c-199">既にスクリプトを発行しており、それらのスクリプトがチャネル データベースに対して実行済の場合、既に実行されたスクリプトへの変更はデータベースには適用されません。</span><span class="sxs-lookup"><span data-stu-id="fec4c-199">If you alter published scripts and those scripts may have already been run against a Channel Database, the modifications to an already executed script will not be applied to the database.</span></span>

<span data-ttu-id="fec4c-200">代わりに、新しいスクリプト ファイル内の変更を提供します。</span><span class="sxs-lookup"><span data-stu-id="fec4c-200">Instead, provide the modifications in a new script file.</span></span> <span data-ttu-id="fec4c-201">依存関係の後に実行されるように、上記の名前付け規則を検討してください。</span><span class="sxs-lookup"><span data-stu-id="fec4c-201">Consider the naming convention noted above to ensure that it runs after its dependencies.</span></span>

### <a name="do-not-remove-old-extension-scripts-that-have-been-published"></a><span data-ttu-id="fec4c-202">発行された以前の拡張スクリプトを削除しないでください。</span><span class="sxs-lookup"><span data-stu-id="fec4c-202">Do not remove old extension scripts that have been published</span></span>

<span data-ttu-id="fec4c-203">展開可能なパッケージまたはインストーラー拡張機能は、データベースの拡張機能の累積的な更新を表す必要があります。</span><span class="sxs-lookup"><span data-stu-id="fec4c-203">Your deployable package or installer extension must represent a cumulative update for your database extensions.</span></span> <span data-ttu-id="fec4c-204">拡張機能パッケージまたはインストーラーの以前のバージョンには依存関係はありません。</span><span class="sxs-lookup"><span data-stu-id="fec4c-204">There should be no dependencies on previous versions of an extension package or installer.</span></span> <span data-ttu-id="fec4c-205">ユーザーは、パッケージまたは拡張機能の以前のバージョンに依存しなくても拡張機能パッケージやインストーラーを適用できる必要があります。</span><span class="sxs-lookup"><span data-stu-id="fec4c-205">A customer should be able to apply your extension package or installer without depending on a previous version of your package or extension.</span></span>

<span data-ttu-id="fec4c-206">拡張スクリプトが展開可能なパッケージまたはインストーラー拡張の一部として公開されている場合、パッケージまたはインストーラーの以降の更新から削除しないでください。</span><span class="sxs-lookup"><span data-stu-id="fec4c-206">If your extension scripts have been published as part of a deployable package or installer extension, do not remove them from subsequent updates in your package or installer.</span></span> <span data-ttu-id="fec4c-207">災害復旧、アップグレード、スケール アウト シナリオに対応するため、チャンル データベースの新しいインスタンスを同じバージョンの最後に配置された拡張機能パッケージに持ち込むために拡張パッケージを使用できます。</span><span class="sxs-lookup"><span data-stu-id="fec4c-207">To account for disaster recovery, upgrade and scale out scenarios, extension packages may be used to bring a new instance of the Channel Database to the same version of the last deployed extension package.</span></span>

### <a name="extension-scripts-must-be-idempotent-and-reentrant"></a><span data-ttu-id="fec4c-208">拡張スクリプトは、非べき等および再入力である必要がある</span><span class="sxs-lookup"><span data-stu-id="fec4c-208">Extension scripts must be idempotent and reentrant</span></span>

<span data-ttu-id="fec4c-209">拡張スクリプトはチャネル データベースあたり 1 回だけ実行されますが、スクリプトはオーサリング エラーまたはタイムアウトやトランザクション デッドロックなどの一時的な SQL エラーが原因で実行されない場合があります。</span><span class="sxs-lookup"><span data-stu-id="fec4c-209">Although extension scripts are run only once per Channel Database, scripts may fail due to authoring errors or transient SQL errors, like time outs or transaction deadlocks.</span></span> <span data-ttu-id="fec4c-210">拡張スクリプトは、それらの障害シナリオに対応するため、非べき等および再入力である必要があります。</span><span class="sxs-lookup"><span data-stu-id="fec4c-210">The extension scripts must be idempotent and reentrant to account for those failure scenarios.</span></span>
<span data-ttu-id="fec4c-211">拡張スクリプトがエラーが原因で失敗した場合、再実行できます。</span><span class="sxs-lookup"><span data-stu-id="fec4c-211">If the extension script fails due to any error, it may be rerun.</span></span> <span data-ttu-id="fec4c-212">スクリプトを再実行しても、データベースに悪影響を及ぼしません。</span><span class="sxs-lookup"><span data-stu-id="fec4c-212">Rerunning the script should not adversely affect the database.</span></span>

### <a name="do-not-assume-that-the-channel-database-data-is-perennial"></a><span data-ttu-id="fec4c-213">チャネル データベース データが永続すると仮定しない</span><span class="sxs-lookup"><span data-stu-id="fec4c-213">Do not assume that the Channel Database data is perennial</span></span>

<span data-ttu-id="fec4c-214">チャネル データベースは、Commerce Scale Unit で実行される操作の記憶域サポートを提供するトランザクション データベースです。</span><span class="sxs-lookup"><span data-stu-id="fec4c-214">The Channel Database is a transactional database that provides storage support for operations performed by Commerce Scale Unit.</span></span> <span data-ttu-id="fec4c-215">長期間保存する必要があるチャネル データベースに格納されるすべてのデータは、[Commerce Data Exchange](./cdx-extensibility.md) を通じて本社にアップロードする必要があります。</span><span class="sxs-lookup"><span data-stu-id="fec4c-215">All data that is stored in the Channel Database that must be kept for long periods of time must be uploaded to the headquarters through the [Commerce Data Exchange](./cdx-extensibility.md).</span></span> <span data-ttu-id="fec4c-216">本社にアップロードされたデータには、[Commerce Data Exchange リアルタイム サービス](./extend-commerce-data-exchange.md)によりアクセスすることができます。</span><span class="sxs-lookup"><span data-stu-id="fec4c-216">Data uploaded to the headquarters can be accessed by the [Commerce Data Exchange Real-time Service](./extend-commerce-data-exchange.md).</span></span>

### <a name="do-write-backward-compatible-channel-database-extensions"></a><span data-ttu-id="fec4c-217">後方互換性のあるチャネルデータベースの拡張機能を作成する</span><span class="sxs-lookup"><span data-stu-id="fec4c-217">Do write backward compatible channel database extensions</span></span>

<span data-ttu-id="fec4c-218">チャネルデータベースには後方互換性がある必要があります。</span><span class="sxs-lookup"><span data-stu-id="fec4c-218">The Channel Database is expected to be backward compatible.</span></span> <span data-ttu-id="fec4c-219">これは、Commerce Scale Unit または POS を更新せずにチャネル データベースだけを更新することにより、既存の Commerce Scale Unit または POS 操作が正常に機能するのを妨げてはならないことを意味します。</span><span class="sxs-lookup"><span data-stu-id="fec4c-219">This means that updating only the Channel Database without updating Commerce Scale Unit or POS must not prevent existing Commerce Scale Unit or POS operations from functioning correctly.</span></span> <span data-ttu-id="fec4c-220">配置フロー中は、Commerce Scale Unit と Modern POS のさまざまなコンポーネントが、依存関係なく逆で更新されます。</span><span class="sxs-lookup"><span data-stu-id="fec4c-220">During deployment flows, the different components of your Commerce Scale Unit and Modern POS are updated in the inverse other of dependency.</span></span> <span data-ttu-id="fec4c-221">これは、チャネル データベースが最初に更新されるコンポーネントで、Commerce Scale Unit または POS が次に更新されることを意味します。</span><span class="sxs-lookup"><span data-stu-id="fec4c-221">This means that the Channel Database is the first component to be updated, and Commerce Scale Unit or POS are updated next.</span></span> <span data-ttu-id="fec4c-222">Commerce Scale Unit または POS が正常に更新できなかった場合、これらのコンポーネントはロールバックされて、以前の作業状態に戻されます。</span><span class="sxs-lookup"><span data-stu-id="fec4c-222">If Commerce Scale Unit or POS fails to update successfully, those components are rolled back to restore them to their previous working state.</span></span> <span data-ttu-id="fec4c-223">このような場合であっても、データの損失を防ぐためにチャネルデータベースはロールバックされません。</span><span class="sxs-lookup"><span data-stu-id="fec4c-223">However, in such situations, the Channel Database is not rolled back to prevent data loss.</span></span> <span data-ttu-id="fec4c-224">ご利用の拡張機能に後方互換性がない場合、正常な展開処理が完了するまでは、これら拡張機能が正しく動作しない可能性があります。</span><span class="sxs-lookup"><span data-stu-id="fec4c-224">If your extensions are not backward compatible, they may fail to work properly until a successful deployment is performed.</span></span>
