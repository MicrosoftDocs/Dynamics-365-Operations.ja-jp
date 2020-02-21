---
title: チャネル データベース 拡張機能
description: このトピックでは、チャネル データベースを拡張する方法について説明します。
author: mugunthanm
manager: AnnBe
ms.date: 02/03/2020
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
ms.openlocfilehash: 13c9037bd572c12b955dfed2d70418c72b3f9f46
ms.sourcegitcommit: 54baab2a04e5c534fc2d1fd67b67e23a152d4e57
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/04/2020
ms.locfileid: "3017743"
---
# <a name="channel-database-extensions"></a><span data-ttu-id="fde9c-103">チャネル データベース 拡張機能</span><span class="sxs-lookup"><span data-stu-id="fde9c-103">Channel database extensions</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="fde9c-104">チャネル データベース (チャネル DB) は、オンライン ストアまたは従来型の店舗などの 1 つまたは複数のコマース チャネルからのトランザクションおよびマスター データを保持します。</span><span class="sxs-lookup"><span data-stu-id="fde9c-104">The channel database (channel DB) holds transactional and master data from one or more commerce channels, such as an online store or a brick-and-mortar store.</span></span> <span data-ttu-id="fde9c-105">マスター データは Commerce Data Exchange (CDX) を使用して、バックオフィス (HQ) からチャネル データベースにプッシュ ダウンされます。</span><span class="sxs-lookup"><span data-stu-id="fde9c-105">The master data is pushed down from the Headquarters (HQ) to the channel database using the commerce data exchange (CDX).</span></span> <span data-ttu-id="fde9c-106">チャネル データベースに格納されたトランザクション データは、CDX を使用して本社に引き戻されます。</span><span class="sxs-lookup"><span data-stu-id="fde9c-106">The transactional data stored in the channel database is pulled back to the headquarters using the CDX.</span></span>

<span data-ttu-id="fde9c-107">このトピックでは、さまざまなシナリオのチャネル データベースを拡張する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="fde9c-107">In this topic we explain how to extend the channel database for different scenarios.</span></span> <span data-ttu-id="fde9c-108">以下の手順は、Finance and Operations、および Dynamics 365 Commerce にのみ適用します。</span><span class="sxs-lookup"><span data-stu-id="fde9c-108">The steps here apply only to Finance and Operations, and Dynamics 365 Commerce.</span></span>

<span data-ttu-id="fde9c-109">拡張機能のさまざまなシナリオを説明する前に、チャネル DB 拡張機能の最新の機能拡張を理解することが重要です。</span><span class="sxs-lookup"><span data-stu-id="fde9c-109">Before discussing the different scenarios for extension, it's important to understand the recent enhancements to channel DB extensions.</span></span>

<span data-ttu-id="fde9c-110">アップグレード時の拡張機能の処理の方法にいくつかの改善を加えました。</span><span class="sxs-lookup"><span data-stu-id="fde9c-110">We have made some improvements to how extensions are handled during an upgrade.</span></span> <span data-ttu-id="fde9c-111">以下の環境構成のいずれかを使用することをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="fde9c-111">We recommend using one of the following environment configurations:</span></span>
- <span data-ttu-id="fde9c-112">Microsoft Dynamics 365 for Finance and Operations, Enterprise edition (2017 年 7 月) およびアプリケーション更新プログラム 5</span><span class="sxs-lookup"><span data-stu-id="fde9c-112">Microsoft Dynamics 365 for Finance and Operations, Enterprise edition (July 2017) with application update 5.</span></span>
- <span data-ttu-id="fde9c-113">Microsoft Dynamics 365 Retail 7.2 およびアプリケーション更新プログラム 5 (まもなく利用できます)。</span><span class="sxs-lookup"><span data-stu-id="fde9c-113">Microsoft Dynamics 365 Retail 7.2 with application update 5, which will be available soon.</span></span>
- <span data-ttu-id="fde9c-114">Microsoft Dynamics 365 Retail 7.3 (アプリケーション更新プログラム 5 を含みます)。</span><span class="sxs-lookup"><span data-stu-id="fde9c-114">Microsoft Dynamics 365 Retail 7.3, which includes application update 5.</span></span>
- <span data-ttu-id="fde9c-115">Microsoft Dynamics 365 for Finance and Operations 7.3 (アプリケーション更新プログラム 5 を含みます)</span><span class="sxs-lookup"><span data-stu-id="fde9c-115">Microsoft Dynamics 365 for Finance and Operations 7.3, which includes application update 5.</span></span>

## <a name="ext-schema"></a><span data-ttu-id="fde9c-116">Ext スキーマ</span><span class="sxs-lookup"><span data-stu-id="fde9c-116">Ext schema</span></span>

<span data-ttu-id="fde9c-117">Finance and Operations と Commerce では、拡張機能をサポートするため、**ext スキーマ**と呼ばれる新しいスキーマを導入しました。</span><span class="sxs-lookup"><span data-stu-id="fde9c-117">In Finance and Operations and Commerce we introduced a new schema called the **ext schema** to support extensions.</span></span> <span data-ttu-id="fde9c-118">以前のバージョンでは、チャネル DB に拡張機能を追加する場合、CRT または AX スキーマに追加していました。</span><span class="sxs-lookup"><span data-stu-id="fde9c-118">In previous versions, if you wanted to add an extension to channel DB, you would add it to the CRT or AX schema.</span></span> <span data-ttu-id="fde9c-119">Finance and Operations と Commerce の両方では、CRT、AX または DBO スキーマを変更することはできません。</span><span class="sxs-lookup"><span data-stu-id="fde9c-119">In both Finance and Operations and Commerce, you cannot change the CRT, AX, or DBO schemas.</span></span> <span data-ttu-id="fde9c-120">すべての変更は **ext スキーマ**で行う必要があります。</span><span class="sxs-lookup"><span data-stu-id="fde9c-120">All changes must be made in the **ext schema**.</span></span> <span data-ttu-id="fde9c-121">CRT または AX スキーマの何かを変更すると、Lifecycle Services (LCS) での展開に失敗します。</span><span class="sxs-lookup"><span data-stu-id="fde9c-121">If you modify anything in the CRT or AX schemas, then deployment in Lifecycle Services (LCS) will fail.</span></span> <span data-ttu-id="fde9c-122">CRT、AX、および DBO スキーマを変更する権限がありませんというエラーが報告されます。</span><span class="sxs-lookup"><span data-stu-id="fde9c-122">An error message states that don’t have permission to modify the CRT, AX, and DBO schemas.</span></span>

<span data-ttu-id="fde9c-123">拡張機能をサポートするため、**ext スキーマ**と呼ばれる新しいスキーマを導入しました。</span><span class="sxs-lookup"><span data-stu-id="fde9c-123">We introduced a new schema called the **ext schema** to support extensions.</span></span> <span data-ttu-id="fde9c-124">以前のバージョンでは、チャネル DB に拡張機能を追加する場合、CRT または AX スキーマに追加していました。</span><span class="sxs-lookup"><span data-stu-id="fde9c-124">In previous versions, if you wanted to add an extension to channel DB, you would add it to the CRT or AX schema.</span></span> <span data-ttu-id="fde9c-125">Commerce と Finance and Operations の両方では、CRT、AX または DBO スキーマを変更することはできません。</span><span class="sxs-lookup"><span data-stu-id="fde9c-125">In both Commerce and Finance and Operations, you cannot change the CRT, AX, or DBO schemas.</span></span> <span data-ttu-id="fde9c-126">すべての変更は **ext スキーマ**で行う必要があります。</span><span class="sxs-lookup"><span data-stu-id="fde9c-126">All changes must be made in the **ext schema**.</span></span> <span data-ttu-id="fde9c-127">CRT または AX スキーマの何かを変更すると、Lifecycle Services (LCS) での展開に失敗します。</span><span class="sxs-lookup"><span data-stu-id="fde9c-127">If you modify anything in the CRT or AX schemas, then deployment in Lifecycle Services (LCS) will fail.</span></span> <span data-ttu-id="fde9c-128">CRT、AX、および DBO スキーマを変更する権限がありませんというエラーが報告されます。</span><span class="sxs-lookup"><span data-stu-id="fde9c-128">An error message states that don’t have permission to modify the CRT, AX, and DBO schemas.</span></span>

> [!NOTE]
> <span data-ttu-id="fde9c-129">いずれかのチャネル DB フィールドの長さを伸ばす場合は、LCS で拡張機能の要求を作成し、EDT の伸長または小数点以下の精度を高める必要があります。</span><span class="sxs-lookup"><span data-stu-id="fde9c-129">If you want to increase any channel DB field length, you must create an extensibility request in LCS, increasing the EDT length or decimal precision.</span></span> <span data-ttu-id="fde9c-130">変更はチャネル DB に自動的にプッシュされません。また、拡張子には、チャネル DB - CRT、AX、または DBO スキーマでなにかを変更または修正するための許可は付与されません。</span><span class="sxs-lookup"><span data-stu-id="fde9c-130">Changes will not be automatically pushed to the channel DB, and extensions will not have permissions to change or modify anything in the channel DB - CRT, AX or DBO schema.</span></span> <span data-ttu-id="fde9c-131">CRT または AX スキーマの何かを変更すると、LCS での展開が失敗します。</span><span class="sxs-lookup"><span data-stu-id="fde9c-131">If you modify anything in the CRT or AX schemas, then deployment in LCS will fail.</span></span>

## <a name="best-practices-for-channel-db-extensions"></a><span data-ttu-id="fde9c-132">チャネル DB 拡張機能のためのベスト プラクティス</span><span class="sxs-lookup"><span data-stu-id="fde9c-132">Best practices for channel DB extensions</span></span>

- <span data-ttu-id="fde9c-133">CRT、AX、または DBO スキーマのいずれも変更しないでください。</span><span class="sxs-lookup"><span data-stu-id="fde9c-133">Don’t modify anything in the CRT, AX, or DBO schemas.</span></span> <span data-ttu-id="fde9c-134">すべての拡張シナリオで **ext スキーマ**を使用します。</span><span class="sxs-lookup"><span data-stu-id="fde9c-134">Use the **ext schema** for all extension scenarios.</span></span>
- <span data-ttu-id="fde9c-135">使用可能な場合は、CRT、AX、または DBO オブジェクトからチャネル データベース コンポーネントに直接アクセスするのではなく、Commerce Runtime ランタイム データ サービスを介してデータを取得することをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="fde9c-135">If available, we recommend getting data through commerce runtime data services, as opposed to accessing channel DB artifacts directly from CRT, AX, or DBO objects.</span></span>

### <a name="dont-do-this"></a><span data-ttu-id="fde9c-136">このようにしない</span><span class="sxs-lookup"><span data-stu-id="fde9c-136">Don't do this</span></span>
<span data-ttu-id="fde9c-137">以下はユーザーがしてはいけないことの例です。</span><span class="sxs-lookup"><span data-stu-id="fde9c-137">The following is an example of what you should not do.</span></span> <span data-ttu-id="fde9c-138">代わりに、主キーの値を取得するために CRT データ サービスを使用してから、拡張テーブルに挿入するために主キーの値を使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="fde9c-138">Instead, you should use the CRT data service to get the primary key value and then use the primary key to insert into your extension table.</span></span>

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


### <a name="dont-do-this"></a><span data-ttu-id="fde9c-139">このようにしない</span><span class="sxs-lookup"><span data-stu-id="fde9c-139">Don't do this</span></span>
- <span data-ttu-id="fde9c-140">CRT、AX、またはDBO スキーマに新しい拡張テーブル、ビュー、または手順を作成しないでください。</span><span class="sxs-lookup"><span data-stu-id="fde9c-140">Don't create any new extension tables, views, or procs in crt, ax, or dbo schema.</span></span> <span data-ttu-id="fde9c-141">すべての拡張コンポーネントは、ext スキーマで実行する必要があります。</span><span class="sxs-lookup"><span data-stu-id="fde9c-141">All extension artifacts must be done in ext schema.</span></span> 
- <span data-ttu-id="fde9c-142">ext スキーマでは、CRT、AX、またはDBO スキーマのデータ型を使用しないでください。</span><span class="sxs-lookup"><span data-stu-id="fde9c-142">Don't use any of the crt, ax or dbo schema data types in ext schema.</span></span> <span data-ttu-id="fde9c-143">ext スキーマのカスタム タイプを作成して使用してください。</span><span class="sxs-lookup"><span data-stu-id="fde9c-143">Create custom types in ext schema and use it.</span></span>
- <span data-ttu-id="fde9c-144">ビュー、手順、関数、またはデータベース コンポーネントを修正しないでください。</span><span class="sxs-lookup"><span data-stu-id="fde9c-144">Don’t modify any views, procedures, functions, or any of the database artifacts.</span></span>
- <span data-ttu-id="fde9c-145">可能な場合は、拡張機能からのデータベース コンポーネントへのアクセスや呼び出しは回避してください。</span><span class="sxs-lookup"><span data-stu-id="fde9c-145">Avoid accessing or calling database artifacts from your extensions, if possible.</span></span> <span data-ttu-id="fde9c-146">代わりに、CRT データ サービスを使用してデータを取得します。</span><span class="sxs-lookup"><span data-stu-id="fde9c-146">Instead, use the CRT data service to get data.</span></span> <span data-ttu-id="fde9c-147">データ サービスを使用する利点は、今後データベース スキーマに重大な変更が行われた場合でも、SLA まで継続的にサポートされることです。</span><span class="sxs-lookup"><span data-stu-id="fde9c-147">The benefits of using the data service are that it will continue to be supported until the SLA, even if breaking changes are made to the database schema in the future.</span></span> <span data-ttu-id="fde9c-148">ただし、必要なデータを公開しない CRT データ サービスのインスタンスもあります。</span><span class="sxs-lookup"><span data-stu-id="fde9c-148">However, there will be instances in which the CRT data service does not expose the data that you need.</span></span> <span data-ttu-id="fde9c-149">このような場合、チャネル データベース コンポーネントに結合するビューを作成することによって、このデータにアクセスすることができます。</span><span class="sxs-lookup"><span data-stu-id="fde9c-149">In these cases, it is still possible to access this data by creating a view which joins on a channel DB artifact.</span></span> <span data-ttu-id="fde9c-150">ビューの作成は、CRT 拡張機能を使用してメモリ内で行うのではなく、データベース レベルで必要な形式のデータを構築する強力なツールになります。</span><span class="sxs-lookup"><span data-stu-id="fde9c-150">Creating views can be a powerful tool to structure the data in a format you need at a database level, as opposed to doing it in memory through CRT extensions.</span></span>


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

## <a name="adding-extensions"></a><span data-ttu-id="fde9c-151">拡張機能の追加</span><span class="sxs-lookup"><span data-stu-id="fde9c-151">Adding extensions</span></span>

1. <span data-ttu-id="fde9c-152">すべての拡張テーブルの列には、NOT NULL の制約を適用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="fde9c-152">All extension table columns must have the NOT NULL constraint enforced.</span></span> <span data-ttu-id="fde9c-153">更新の過程で、列の値が空白で更新され、NULL の値が正しく処理されない場合は、 CRT でランタイムの例外処理が発生する可能性があります。</span><span class="sxs-lookup"><span data-stu-id="fde9c-153">During upgrade, if the column value is blank it will be updated with NULL values and it may cause a runtime exception in CRT if the null value is not handled properly.</span></span>
2. <span data-ttu-id="fde9c-154">すべての拡張機能テーブルは **UserRole** および **DeployExtensibilityRole** にアクセス許可を付与する必要があります。</span><span class="sxs-lookup"><span data-stu-id="fde9c-154">All the extension tables should have grant permission on **UserRole** and **DeployExtensibilityRole**.</span></span>

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

3. <span data-ttu-id="fde9c-155">テーブルが HQ からデータを送受信する場合は、 **DataSyncUsersRole** のアクセス許可を付与します。</span><span class="sxs-lookup"><span data-stu-id="fde9c-155">Grant **DataSyncUsersRole** permission if your table is going to send or eceive data from HQ.</span></span>

    ```sql
    GRANT SELECT, INSERT, UPDATE, DELETE, ALTER ON OBJECT::[ext].[EXTTABLENAME] TO [DataSyncUsersRole]
    GO
    ```

4. <span data-ttu-id="fde9c-156">拡張テーブルを作成し、HQ にデータを同期させる場合は、拡張テーブルに親テーブルの主となる列を含めます。</span><span class="sxs-lookup"><span data-stu-id="fde9c-156">If you are creating an extended table and want to sync the data back to HQ, you need to have the primary column of the parent table in the extended table.</span></span>
5. <span data-ttu-id="fde9c-157">たとえば、 **ContosoRetailTransactionTable** などのように、常にテーブルに接頭語を付けると、他のカスタマイズとの競合を回避できます。</span><span class="sxs-lookup"><span data-stu-id="fde9c-157">Always prefix your table, for example **ContosoRetailTransactionTable**, so that you can avoid conflicts with other customizations.</span></span>

## <a name="attributes"></a><span data-ttu-id="fde9c-158">属性</span><span class="sxs-lookup"><span data-stu-id="fde9c-158">Attributes</span></span>

<span data-ttu-id="fde9c-159">顧客、顧客の注文、現金売りトランザクション、およびコール センター注文の属性をサポートするために、HQ の属性フレームワークを拡張しました。</span><span class="sxs-lookup"><span data-stu-id="fde9c-159">We extended the attribute framework in HQ to support attributes for Customers, Customer orders, cash and carry transactions and call center orders.</span></span>

### <a name="customer-attributes"></a><span data-ttu-id="fde9c-160">顧客属性</span><span class="sxs-lookup"><span data-stu-id="fde9c-160">Customer attributes</span></span>
<span data-ttu-id="fde9c-161">新しい顧客属性フレームワークでは、構成を使用して、POS または HQ 内の顧客追加/編集画面または顧客詳細画面に新しいフィールドを追加することができます。</span><span class="sxs-lookup"><span data-stu-id="fde9c-161">With the new customer attribute framework, you can use configurations to add new fields to the customer add/edit or customer details screens in POS or HQ.</span></span> <span data-ttu-id="fde9c-162">コマース パラメーターで顧客属性グループを構成した後、POS や HQ はコードの変更やカスタマイズを行わずに新しい属性を自動的に表示します。</span><span class="sxs-lookup"><span data-stu-id="fde9c-162">After configuring the customer attribute group in commerce parameters, POS and HQ will automatically show up the new attribute without any code change or customization.</span></span> <span data-ttu-id="fde9c-163">画面レイアウト設計者は、取引画面 (**顧客** パネル) に顧客属性を表示するようにも設定されます。</span><span class="sxs-lookup"><span data-stu-id="fde9c-163">The screen layout designer will also be configured to show the customer attributes in the transaction screen - **Customer** panel.</span></span>

### <a name="order-attributes"></a><span data-ttu-id="fde9c-164">注文属性</span><span class="sxs-lookup"><span data-stu-id="fde9c-164">Order attributes</span></span>
<span data-ttu-id="fde9c-165">属性フレームワークは、現金売りトランザクション、顧客の注文、およびコール センター注文の属性をサポートするように拡張されました。</span><span class="sxs-lookup"><span data-stu-id="fde9c-165">The attribute framework was extended to support attributes in cash and carry transactions, customer orders, and call center orders.</span></span> <span data-ttu-id="fde9c-166">HQ または CRT で値を直接編集して設定することができます。</span><span class="sxs-lookup"><span data-stu-id="fde9c-166">You can edit and set values directly in HQ or in CRT.</span></span> <span data-ttu-id="fde9c-167">これらすべてはデータベースを変更せずにコンフィギュレーションを介して実行することができます。</span><span class="sxs-lookup"><span data-stu-id="fde9c-167">All this can be done through configurations, without any database changes.</span></span> <span data-ttu-id="fde9c-168">(基本的な CRUD 操作は必要ではなく、主要なビジネス ロジックの属性値をカスタマイズすることができます。) 以前は、これを行うには、HQ とチャンネル DB に新しいテーブルを作成し、CRT を変更する必要がありました。</span><span class="sxs-lookup"><span data-stu-id="fde9c-168">(You can customization the attribute values for core business logic, not required for basic CRUD operations.) Previously, you had to create new tables in HQ and channel DB, and then modify CRT to do this.</span></span> <span data-ttu-id="fde9c-169">現在は、すべての属性の作成をコンフィギュレーションを通じて実行できるようになりました。</span><span class="sxs-lookup"><span data-stu-id="fde9c-169">Now all the attribute creation can be done through configuration.</span></span>

## <a name="adding-a-new-table"></a><span data-ttu-id="fde9c-170">新しいテーブルの追加</span><span class="sxs-lookup"><span data-stu-id="fde9c-170">Adding a new table</span></span>

<span data-ttu-id="fde9c-171">このシナリオでは、新しいテーブルを作成し、チャネル DB に追加する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="fde9c-171">In this scenario we will explain how to create a new table and add it to the channel DB.</span></span> <span data-ttu-id="fde9c-172">すべての拡張コードは **ext スキーマ**へアクセスすることができます。</span><span class="sxs-lookup"><span data-stu-id="fde9c-172">All extension code has access to the **ext schema**.</span></span>

- <span data-ttu-id="fde9c-173">SQL Server Management Studio デザイナーを使用するか、SQL スクリプトを使用して、**ext スキーマ**のチャネル データベースに新しいテーブルを作成します。</span><span class="sxs-lookup"><span data-stu-id="fde9c-173">Create a new table in the channel database in the **ext schema** either using SQL Server Management Studio Designer or using SQL scripts.</span></span> <span data-ttu-id="fde9c-174">以下は、SQL スクリプトの例です。</span><span class="sxs-lookup"><span data-stu-id="fde9c-174">The following is an example SQL script.</span></span>

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

## <a name="adding-new-views-stored-procedure-functions-and-defined-types"></a><span data-ttu-id="fde9c-175">新しいビュー、ストアド プロシージャ、関数、定義済タイプの追加</span><span class="sxs-lookup"><span data-stu-id="fde9c-175">Adding new views, stored procedure, functions, and defined types</span></span>

<span data-ttu-id="fde9c-176">すべての新しいストアド プロシージャ、ビューまたは機能は **ext スキーマ**に作成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="fde9c-176">All new stored procedures, views or functions must be created in the **ext schema**.</span></span> <span data-ttu-id="fde9c-177">手順、ビューまたは機能から、データベース コンポーネントをアクセスするまたは呼びだすことはやめてください。</span><span class="sxs-lookup"><span data-stu-id="fde9c-177">Don't access or call our database artifacts from your procedures, views, or functions.</span></span>

## <a name="deployment-checks"></a><span data-ttu-id="fde9c-178">配置のチェック</span><span class="sxs-lookup"><span data-stu-id="fde9c-178">Deployment checks</span></span>

<span data-ttu-id="fde9c-179">配置プロセスは、データベースのコンポーネントに変更があるかどうかを判断します。</span><span class="sxs-lookup"><span data-stu-id="fde9c-179">The deployment process determines if there are any modification to the database artifacts.</span></span> <span data-ttu-id="fde9c-180">CRT、AX、または DBO スキーマ オブジェクトを変更しようとした場合、またはどのシナリオの場合でも SQL でそれらに直接アクセスすると、展開は失敗します。</span><span class="sxs-lookup"><span data-stu-id="fde9c-180">If you have attempted to modify the CRT, AX, or DBO schema objects, or access them for any scenario directly in SQL, then deployment will fail.</span></span>

## <a name="extension-scripts-and-deployment"></a><span data-ttu-id="fde9c-181">拡張スクリプトおよび展開</span><span class="sxs-lookup"><span data-stu-id="fde9c-181">Extension scripts and deployment</span></span>

<span data-ttu-id="fde9c-182">チャンネル データベース拡張は、1 つまたは複数の T-SQL スクリプト ファイルを作成し、[展開可能なパッケージ](./retail-sdk/retail-sdk-packaging.md)に含めることで用意されます。</span><span class="sxs-lookup"><span data-stu-id="fde9c-182">Channel Database extensions are provided by authoring one or more T-SQL script files and including them in a [deployable package](./retail-sdk/retail-sdk-packaging.md).</span></span> <span data-ttu-id="fde9c-183">このプロセスについては、[Retail SDK](./retail-sdk/retail-sdk-overview.md) ドキュメントで説明します。</span><span class="sxs-lookup"><span data-stu-id="fde9c-183">This process is described in the [Retail SDK](./retail-sdk/retail-sdk-overview.md) documentation.</span></span>

<span data-ttu-id="fde9c-184">拡張スクリプト ファイルは、[T-SQL](https://docs.microsoft.com/sql/t-sql/language-reference) を使用して記述され、[Azure SQL データベース](https://docs.microsoft.com/azure/sql-database/sql-database-features)と互換性があります。</span><span class="sxs-lookup"><span data-stu-id="fde9c-184">Extension script files must be written using [T-SQL](https://docs.microsoft.com/sql/t-sql/language-reference) and compatible with [Azure SQL Database](https://docs.microsoft.com/azure/sql-database/sql-database-features).</span></span>
<span data-ttu-id="fde9c-185">スクリプト ファイルの末尾は *.sql* ファイル拡張子にする必要があります。その他のファイルは無視されます。または、パッケージングまたは配置障害を引き起こす可能性があります。</span><span class="sxs-lookup"><span data-stu-id="fde9c-185">The script files must end with the *.sql* file extension, any other files will be ignored or may induce a packaging or deployment failure.</span></span> <span data-ttu-id="fde9c-186">Commerce Scale Unit または Modern POS オフラインの一部としてチャネル データベース拡張機能を展開する場合、スクリプトは、それらのコンポーネントに対して使用される SQL Express または SQL Server のバージョンの両方またはいずれかと互換性があることも必要です。</span><span class="sxs-lookup"><span data-stu-id="fde9c-186">If you intend to deploy your Channel Database extensions as part of Commerce Scale Unit or Modern POS offline, the scripts must also be compatible with the version of SQL Express and/or SQL Server that will be used for those components.</span></span>

<span data-ttu-id="fde9c-187">配置とインストール中、拡張子スクリプトは、スクリプト ファイル名に基づいたアルファベット順で実行されます。</span><span class="sxs-lookup"><span data-stu-id="fde9c-187">During deployment and installation, the extension scripts are executed in alphabetical order based on the script file name.</span></span>
<span data-ttu-id="fde9c-188">各スクリプトは、完了するまで実行され、拡張スクリプトの完了を追跡するため、メタデータ レコードはチャンネル データベースの CRT.RETAILUPGRADEHISTORY テーブルに追加されます。</span><span class="sxs-lookup"><span data-stu-id="fde9c-188">Each script is run to completion and then a metadata record is added to the Channel Database's CRT.RETAILUPGRADEHISTORY table to track the completion of that extension script.</span></span>
<span data-ttu-id="fde9c-189">そのメタデータ レコードが存在する場合、その後の展開で同じチャネル データベースに対してスクリプトが再度実行されることはありません。</span><span class="sxs-lookup"><span data-stu-id="fde9c-189">The script will not be executed again for the same Channel Database in subsequent deployments if that metadata record is present.</span></span>
<span data-ttu-id="fde9c-190">スクリプトが実行中に失敗し、正常に完了しない場合、そのメタデータは保存されず、以降の配置でスクリプトが再実行されます。</span><span class="sxs-lookup"><span data-stu-id="fde9c-190">If a script fails during execution and does not complete successfully, its metadata will not be stored and the script will be rerun on subsequent deployments.</span></span>

<span data-ttu-id="fde9c-191">展開やインストールが製品の更新と組み合わされている場合、拡張スクリプトは製品の更新後に実行されます。</span><span class="sxs-lookup"><span data-stu-id="fde9c-191">If the deployment or installation is combined with an update of the product, the extension scripts are run after the product update.</span></span>

<span data-ttu-id="fde9c-192">正常に行われるチャネル データベース拡張を作成するには、次のガイドラインに従う必要があります。</span><span class="sxs-lookup"><span data-stu-id="fde9c-192">To author a successful Channel Database extension, you must adhere to the following guidelines.</span></span>

### <a name="use-a-naming-convention-that-ensures-stable-order-when-sorted-alphabetically"></a><span data-ttu-id="fde9c-193">アルファベット順に並べ替えられたときに、安定した順序が確保される名前付け規則を使用します。</span><span class="sxs-lookup"><span data-stu-id="fde9c-193">Use a naming convention that ensures stable order when sorted alphabetically</span></span>

<span data-ttu-id="fde9c-194">拡張スクリプトは、ファイル名に基づくアルファベット順に実行されるので、並べ替えたときに正しい実行順序が使用される名前付け規則を確立する必要があります。</span><span class="sxs-lookup"><span data-stu-id="fde9c-194">Because extension scripts are executed in alphabetical order based on the file name, you should establish a naming convention that ensures that the correct execution order is used when sorted.</span></span>

<span data-ttu-id="fde9c-195">1 つの例は、次のパターンを持つファイルの名前付けです: "<ISO 8601 date>_<descriptio>.sql"。ここで **<ISO 8601 date>** は ISO 8601 形式の日付で、**<description>** はスクリプトの目的を識別するための説明のテキストです。</span><span class="sxs-lookup"><span data-stu-id="fde9c-195">One example would be naming files with the following pattern: "<ISO 8601 date>_<descriptio>.sql", where **<ISO 8601 date>** is a ISO 8601 formatted date and **<description>** is descriptive text to identify the purpose of the script.</span></span>
<span data-ttu-id="fde9c-196">たとえば、*"20180501_CustomerDetails.sql"* と *"20181102_CustomerDetailsIndex.sql"* などです。</span><span class="sxs-lookup"><span data-stu-id="fde9c-196">For instance, *"20180501_CustomerDetails.sql"* and *"20181102_CustomerDetailsIndex.sql"*.</span></span>
<span data-ttu-id="fde9c-197">前者は、「顧客の詳細」機能に関連する 2018 年 5 月 1 日に作成された拡張スクリプトを表しており、後者は、2018 年 11 月 2 日に作成された以前の機能に関連するインデックスに関連付けられている拡張スクリプトです。</span><span class="sxs-lookup"><span data-stu-id="fde9c-197">The former would represent an extension script authored on May 1, 2018 that is related to "Customer Details" feature and the latter an extension script associated to indexes related to the previous feature authored on November 2, 2018.</span></span>

<span data-ttu-id="fde9c-198">別の単純な方法は、"0001_CustomerDetails.sql" や "0002_CustomerDetailsIndex.sql" などの差分数値接頭語を使用する方法です。</span><span class="sxs-lookup"><span data-stu-id="fde9c-198">Another simpler alternative is to use an incremental numeric prefix, such as "0001_CustomerDetails.sql" and "0002_CustomerDetailsIndex.sql".</span></span>

<span data-ttu-id="fde9c-199">1 つのスクリプトが正常に実行される別のスクリプトに依存している場合、アルファベット順のファイル名が必要な実行順序と一致していることを確認する方法で命名する必要があります。</span><span class="sxs-lookup"><span data-stu-id="fde9c-199">If one script depends on another having executed successfully, you must name then in a way that ensures that the file name in alphabetical order matches the required execution order.</span></span>

### <a name="do-not-alter-extension-scripts-that-have-been-published"></a><span data-ttu-id="fde9c-200">発行された拡張スクリプトを変更しないでください。</span><span class="sxs-lookup"><span data-stu-id="fde9c-200">Do not alter extension scripts that have been published</span></span>

<span data-ttu-id="fde9c-201">展開可能なパッケージまたはチャンル データベース拡張スクリプトを含むインストーラー拡張をリリースした場合、それらのスクリプトを変更しないでください。</span><span class="sxs-lookup"><span data-stu-id="fde9c-201">If you have released a deployable package or installer extension that contains Channel Database extension scripts, do not alter those scripts.</span></span> <span data-ttu-id="fde9c-202">拡張スクリプトは、チャネル データベース インスタンスあたり 1 回だけ実行されます。</span><span class="sxs-lookup"><span data-stu-id="fde9c-202">Extension scripts are run only once per Channel Database instance.</span></span>
<span data-ttu-id="fde9c-203">既にスクリプトを発行しており、それらのスクリプトがチャネル データベースに対して実行済の場合、既に実行されたスクリプトへの変更はデータベースには適用されません。</span><span class="sxs-lookup"><span data-stu-id="fde9c-203">If you alter published scripts and those scripts may have already been run against a Channel Database, the modifications to an already executed script will not be applied to the database.</span></span>

<span data-ttu-id="fde9c-204">代わりに、新しいスクリプト ファイル内の変更を提供します。</span><span class="sxs-lookup"><span data-stu-id="fde9c-204">Instead, provide the modifications in a new script file.</span></span> <span data-ttu-id="fde9c-205">依存関係の後に実行されるように、上記の名前付け規則を検討してください。</span><span class="sxs-lookup"><span data-stu-id="fde9c-205">Consider the naming convention noted above to ensure that it runs after its dependencies.</span></span>

### <a name="do-not-remove-old-extension-scripts-that-have-been-published"></a><span data-ttu-id="fde9c-206">発行された以前の拡張スクリプトを削除しないでください。</span><span class="sxs-lookup"><span data-stu-id="fde9c-206">Do not remove old extension scripts that have been published</span></span>

<span data-ttu-id="fde9c-207">展開可能なパッケージまたはインストーラー拡張機能は、データベースの拡張機能の累積的な更新を表す必要があります。</span><span class="sxs-lookup"><span data-stu-id="fde9c-207">Your deployable package or installer extension must represent a cumulative update for your database extensions.</span></span> <span data-ttu-id="fde9c-208">拡張機能パッケージまたはインストーラーの以前のバージョンには依存関係はありません。</span><span class="sxs-lookup"><span data-stu-id="fde9c-208">There should be no dependencies on previous versions of an extension package or installer.</span></span> <span data-ttu-id="fde9c-209">ユーザーは、パッケージまたは拡張機能の以前のバージョンに依存しなくても拡張機能パッケージやインストーラーを適用できる必要があります。</span><span class="sxs-lookup"><span data-stu-id="fde9c-209">A customer should be able to apply your extension package or installer without depending on a previous version of your package or extension.</span></span>

<span data-ttu-id="fde9c-210">拡張スクリプトが展開可能なパッケージまたはインストーラー拡張の一部として公開されている場合、パッケージまたはインストーラーの以降の更新から削除しないでください。</span><span class="sxs-lookup"><span data-stu-id="fde9c-210">If your extension scripts have been published as part of a deployable package or installer extension, do not remove them from subsequent updates in your package or installer.</span></span> <span data-ttu-id="fde9c-211">災害復旧、アップグレード、スケール アウト シナリオに対応するため、チャンル データベースの新しいインスタンスを同じバージョンの最後に配置された拡張機能パッケージに持ち込むために拡張パッケージを使用できます。</span><span class="sxs-lookup"><span data-stu-id="fde9c-211">To account for disaster recovery, upgrade and scale out scenarios, extension packages may be used to bring a new instance of the Channel Database to the same version of the last deployed extension package.</span></span>

### <a name="extension-scripts-must-be-idempotent-and-reentrant"></a><span data-ttu-id="fde9c-212">拡張スクリプトは、非べき等および再入力である必要がある</span><span class="sxs-lookup"><span data-stu-id="fde9c-212">Extension scripts must be idempotent and reentrant</span></span>

<span data-ttu-id="fde9c-213">拡張スクリプトはチャネル データベースあたり 1 回だけ実行されますが、スクリプトはオーサリング エラーまたはタイムアウトやトランザクション デッドロックなどの一時的な SQL エラーが原因で実行されない場合があります。</span><span class="sxs-lookup"><span data-stu-id="fde9c-213">Although extension scripts are run only once per Channel Database, scripts may fail due to authoring errors or transient SQL errors, like time outs or transaction deadlocks.</span></span> <span data-ttu-id="fde9c-214">拡張スクリプトは、それらの障害シナリオに対応するため、非べき等および再入力である必要があります。</span><span class="sxs-lookup"><span data-stu-id="fde9c-214">The extension scripts must be idempotent and reentrant to account for those failure scenarios.</span></span>
<span data-ttu-id="fde9c-215">拡張スクリプトがエラーが原因で失敗した場合、再実行できます。</span><span class="sxs-lookup"><span data-stu-id="fde9c-215">If the extension script fails due to any error, it may be rerun.</span></span> <span data-ttu-id="fde9c-216">スクリプトを再実行しても、データベースに悪影響を及ぼしません。</span><span class="sxs-lookup"><span data-stu-id="fde9c-216">Rerunning the script should not adversely affect the database.</span></span>

### <a name="do-not-assume-that-the-channel-database-data-is-perennial"></a><span data-ttu-id="fde9c-217">チャネル データベース データが永続すると仮定しない</span><span class="sxs-lookup"><span data-stu-id="fde9c-217">Do not assume that the Channel Database data is perennial</span></span>

<span data-ttu-id="fde9c-218">チャネル データベースは、Commerce Scale Unit で実行される操作の記憶域サポートを提供するトランザクション データベースです。</span><span class="sxs-lookup"><span data-stu-id="fde9c-218">The Channel Database is a transactional database that provides storage support for operations performed by Commerce Scale Unit.</span></span> <span data-ttu-id="fde9c-219">長期間保存する必要があるチャネル データベースに格納されるすべてのデータは、[Commerce Data Exchange](./cdx-extensibility.md) を通じて本社にアップロードする必要があります。</span><span class="sxs-lookup"><span data-stu-id="fde9c-219">All data that is stored in the Channel Database that must be kept for long periods of time must be uploaded to the headquarters through the [Commerce Data Exchange](./cdx-extensibility.md).</span></span> <span data-ttu-id="fde9c-220">本社にアップロードされたデータには、[Commerce Data Exchange リアルタイム サービス](./extend-commerce-data-exchange.md)によりアクセスすることができます。</span><span class="sxs-lookup"><span data-stu-id="fde9c-220">Data uploaded to the headquarters can be accessed by the [Commerce Data Exchange Real-time Service](./extend-commerce-data-exchange.md).</span></span>

### <a name="do-write-backward-compatible-channel-database-extensions"></a><span data-ttu-id="fde9c-221">後方互換性のあるチャネルデータベースの拡張機能を作成する</span><span class="sxs-lookup"><span data-stu-id="fde9c-221">Do write backward compatible channel database extensions</span></span>

<span data-ttu-id="fde9c-222">チャネルデータベースには後方互換性がある必要があります。</span><span class="sxs-lookup"><span data-stu-id="fde9c-222">The Channel Database is expected to be backward compatible.</span></span> <span data-ttu-id="fde9c-223">これは、Commerce Scale Unit または POS を更新せずにチャネル データベースだけを更新することにより、既存の Commerce Scale Unit または POS 操作が正常に機能するのを妨げてはならないことを意味します。</span><span class="sxs-lookup"><span data-stu-id="fde9c-223">This means that updating only the Channel Database without updating Commerce Scale Unit or POS must not prevent existing Commerce Scale Unit or POS operations from functioning correctly.</span></span> <span data-ttu-id="fde9c-224">配置フロー中は、Commerce Scale Unit と Modern POS のさまざまなコンポーネントが、依存関係なく逆で更新されます。</span><span class="sxs-lookup"><span data-stu-id="fde9c-224">During deployment flows, the different components of your Commerce Scale Unit and Modern POS are updated in the inverse other of dependency.</span></span> <span data-ttu-id="fde9c-225">これは、チャネル データベースが最初に更新されるコンポーネントで、Commerce Scale Unit または POS が次に更新されることを意味します。</span><span class="sxs-lookup"><span data-stu-id="fde9c-225">This means that the Channel Database is the first component to be updated, and Commerce Scale Unit or POS are updated next.</span></span> <span data-ttu-id="fde9c-226">Commerce Scale Unit または POS が正常に更新できなかった場合、これらのコンポーネントはロールバックされて、以前の作業状態に戻されます。</span><span class="sxs-lookup"><span data-stu-id="fde9c-226">If Commerce Scale Unit or POS fails to update successfully, those components are rolled back to restore them to their previous working state.</span></span> <span data-ttu-id="fde9c-227">このような場合であっても、データの損失を防ぐためにチャネルデータベースはロールバックされません。</span><span class="sxs-lookup"><span data-stu-id="fde9c-227">However, in such situations, the Channel Database is not rolled back to prevent data loss.</span></span> <span data-ttu-id="fde9c-228">ご利用の拡張機能に後方互換性がない場合、正常な展開処理が完了するまでは、これら拡張機能が正しく動作しない可能性があります。</span><span class="sxs-lookup"><span data-stu-id="fde9c-228">If your extensions are not backward compatible, they may fail to work properly until a successful deployment is performed.</span></span>
