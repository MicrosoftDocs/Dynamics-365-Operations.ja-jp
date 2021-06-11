---
title: Dataverse 仮想テーブル クエリの最適化
description: Dataverse 仮想テーブル クエリのパフォーマンスの最適化およびトラブルシューティング
author: andreabichsel
ms.date: 04/02/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: jaredha
ms.search.validFrom: 2021-04-02
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 66fb9f2b50079b5eb4eb16da17b8a473d687d354
ms.sourcegitcommit: 879ee8a10e6158885795dce4b3db5077540eec41
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/18/2021
ms.locfileid: "6054911"
---
# <a name="optimize-dataverse-virtual-table-queries"></a><span data-ttu-id="3dc12-103">Dataverse 仮想テーブル クエリの最適化</span><span class="sxs-lookup"><span data-stu-id="3dc12-103">Optimize Dataverse virtual table queries</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

## <a name="issue"></a><span data-ttu-id="3dc12-104">出庫</span><span class="sxs-lookup"><span data-stu-id="3dc12-104">Issue</span></span>

### <a name="overview"></a><span data-ttu-id="3dc12-105">概要</span><span class="sxs-lookup"><span data-stu-id="3dc12-105">Overview</span></span>

<span data-ttu-id="3dc12-106">Dataverse 仮想テーブルを使用して Dynamics 365 Human Resources との統合やその他のデータ接続を開発する場合、仮想テーブルに対するクエリでパフォーマンスの問題が発生する可能性があります。</span><span class="sxs-lookup"><span data-stu-id="3dc12-106">When using Dataverse virtual tables to develop integrations and other data connections with Dynamics 365 Human Resources, you can experience performance issues with queries against the virtual tables.</span></span> <span data-ttu-id="3dc12-107">クエリの実行が遅い場合、さまざまなクライアントまたはインターフェイスで発生する可能性があります。</span><span class="sxs-lookup"><span data-stu-id="3dc12-107">The slow query execution can occur across various clients or interfaces.</span></span> <span data-ttu-id="3dc12-108">たとえば、次のような状況で問題が発生する可能性があります。</span><span class="sxs-lookup"><span data-stu-id="3dc12-108">For example, you may experience the issue in the following circumstances:</span></span>

- <span data-ttu-id="3dc12-109">Dataverse Web API を介して仮想テーブルをクエリする場合</span><span class="sxs-lookup"><span data-stu-id="3dc12-109">When querying a virtual table through the Dataverse Web API</span></span>
- <span data-ttu-id="3dc12-110">仮想テーブルに対して Power App を作成する場合</span><span class="sxs-lookup"><span data-stu-id="3dc12-110">When creating a Power App against a virtual table</span></span>
- <span data-ttu-id="3dc12-111">仮想テーブルで Power BI レポートを作成する場合</span><span class="sxs-lookup"><span data-stu-id="3dc12-111">When building a Power BI report on a virtual table</span></span>

<span data-ttu-id="3dc12-112">これらのインターフェースはすべて、パフォーマンスの問題を表面化する可能性があります。</span><span class="sxs-lookup"><span data-stu-id="3dc12-112">All these interfaces have the potential to surface the performance issue.</span></span>

<span data-ttu-id="3dc12-113">Human Resources の Dataverse 仮想テーブルでパフォーマンスが低下する原因の 1 つは、テーブルの[ナビゲーション プロパティ](/powerapps/developer/data-platform/webapi/web-api-types-operations#navigation-properties) に関連する仮想テーブルの外部キー列です。</span><span class="sxs-lookup"><span data-stu-id="3dc12-113">One cause of slow performance with Dataverse virtual tables for Human Resources is the foreign key columns of the virtual table related to the table's [navigation properties](/powerapps/developer/data-platform/webapi/web-api-types-operations#navigation-properties).</span></span> <span data-ttu-id="3dc12-114">仮想テーブルのナビゲーション プロパティが作成されると、関連する仮想テーブルのキー列のキーの値を表す外部キー列がテーブルに自動的に追加されます。</span><span class="sxs-lookup"><span data-stu-id="3dc12-114">When navigation properties are created for a virtual table, a foreign key column is automatically added to the table to represent the value of the key for the related virtual table's key column.</span></span> <span data-ttu-id="3dc12-115">たとえば、**_mshr_fk_person_id_value** 列は、**mshr_dirpersonentity** エンティティの外部キー プロパティを使用して **mshr_hcmworkerbaseentity** エンティティに追加されます。</span><span class="sxs-lookup"><span data-stu-id="3dc12-115">For example, the **_mshr_fk_person_id_value** column is added to the **mshr_hcmworkerbaseentity** entity with the foreign key property from the **mshr_dirpersonentity** entity.</span></span> <span data-ttu-id="3dc12-116">これらの外部キー列の値がテーブルでどのように維持されるかにより、値をフェッチすると、仮想テーブルに対するクエリのパフォーマンスに悪影響を与える可能性があります。</span><span class="sxs-lookup"><span data-stu-id="3dc12-116">Because of how the values for these foreign key columns are maintained in a table, fetching the values can have a negative impact on the performance of a query against the virtual table.</span></span>

### <a name="potential-symptoms"></a><span data-ttu-id="3dc12-117">潜在的な現象</span><span class="sxs-lookup"><span data-stu-id="3dc12-117">Potential symptoms</span></span>

<span data-ttu-id="3dc12-118">この影響が見られる例は、作業者 (**mshr_hcmworkerentity**) または基本作業者 (**mshr_hcmworkerbaseentity**) エンティティに対するクエリです。</span><span class="sxs-lookup"><span data-stu-id="3dc12-118">An example where you may see this impact is in queries against the Worker (**mshr_hcmworkerentity**) or Base worker (**mshr_hcmworkerbaseentity**) entity.</span></span> <span data-ttu-id="3dc12-119">さまざまな方法でパフォーマンスの問題が発生する可能性があります。</span><span class="sxs-lookup"><span data-stu-id="3dc12-119">You may see the performance issue manifest itself in a few different ways:</span></span>

- <span data-ttu-id="3dc12-120">**クエリの実行が遅い**: 仮想テーブルに対するクエリは予期された結果を返す場合がありますが、クエリの実行が完了するまでに予想よりも時間がかかります。</span><span class="sxs-lookup"><span data-stu-id="3dc12-120">**Slow query execution**: The query against the virtual table may return the expected results, but take longer than expected to complete execution of the query.</span></span>
- <span data-ttu-id="3dc12-121">**クエリのタイムアウト**: クエリがタイムアウトし、「Finance and Operations を呼び出すためのトークンが取得されましたが、Finance and Operations はタイプ InternalServerError のエラーを返す」場合があります。</span><span class="sxs-lookup"><span data-stu-id="3dc12-121">**Query timeout**: The query may time out and return the following error: "A token was obtained to call Finance and Operations, but Finance and Operations returned an error of type InternalServerError."</span></span>
- <span data-ttu-id="3dc12-122">**予期しないエラー**: クエリは、「予期しないエラーが発生しました」というメッセージとともにエラー タイプ 400 を返す場合があります。</span><span class="sxs-lookup"><span data-stu-id="3dc12-122">**Unexpected error**: The query may return an error type 400 with the following message: "An unexpected error occurred."</span></span>

  ![HcmWorkerBaseEntity のエラー タイプ 400](./media/HcmWorkerBaseEntityErrorType400.png)

- <span data-ttu-id="3dc12-124">**調整**: クエリはサーバー リソースを過剰に使用し、調整の対象になる可能性があります。</span><span class="sxs-lookup"><span data-stu-id="3dc12-124">**Throttling**: The query may overuse server resources, and become subject to throttling.</span></span> <span data-ttu-id="3dc12-125">この場合、クエリは次のエラーを返します: 「Finance and Operations を呼び出すためのトークンが取得されましたが、Finance and Operations はタイプ 429 のエラーを返しました。」</span><span class="sxs-lookup"><span data-stu-id="3dc12-125">In this case, the query returns the following error: "A token was obtained to call Finance and Operations, but Finance and Operations returned an error of type 429."</span></span> <span data-ttu-id="3dc12-126">Human Resources の調整の詳細については [スロットリングに関するよく寄せられる質問](./hr-admin-integration-throttling-faq.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="3dc12-126">For more information in throttling in Human Resources, see [Throttling FAQ](./hr-admin-integration-throttling-faq.md).</span></span>

  ![HcmWorkerBaseEntity のエラー タイプ 429](./media/HcmWorkerBaseEntityErrorType429.png)

## <a name="resolution"></a><span data-ttu-id="3dc12-128">解像度</span><span class="sxs-lookup"><span data-stu-id="3dc12-128">Resolution</span></span>

### <a name="limit-the-number-of-columns-included-in-your-data-query"></a><span data-ttu-id="3dc12-129">データ クエリに含める列の数の制限</span><span class="sxs-lookup"><span data-stu-id="3dc12-129">Limit the number of columns included in your data query</span></span>

<span data-ttu-id="3dc12-130">仮想テーブルの場合、クエリ パフォーマンスを向上させる可能性が最も高い方法の 1 つは、クエリで選択される列の数を制限することです。</span><span class="sxs-lookup"><span data-stu-id="3dc12-130">With virtual tables, one of the methods with the greatest potential to improve query performance is to limit the number of columns selected in the query.</span></span> <span data-ttu-id="3dc12-131">クエリ パフォーマンスを最適化するための一般的なガイダンスは、クエリで返される列を必要なプロパティのみに制限することです。</span><span class="sxs-lookup"><span data-stu-id="3dc12-131">The general guidance for optimizing query performance is to limit the columns returned in your query to only those properties that you need.</span></span> <span data-ttu-id="3dc12-132">これは特に、仮想テーブルの外部キー列に当てはまります。</span><span class="sxs-lookup"><span data-stu-id="3dc12-132">This is particularly true with the foreign key columns on virtual tables.</span></span> <span data-ttu-id="3dc12-133">統合またはレポートに外部キー列の値が必要ない場合は、外部キー列を除いて、必要な列のみを選択するようにクエリを構成します。</span><span class="sxs-lookup"><span data-stu-id="3dc12-133">If you don't need the values in the foreign key columns for your integration or report, then structure the query to select only the columns you need, excluding the foreign key columns.</span></span>

#### <a name="selecting-columns-in-an-odata-query"></a><span data-ttu-id="3dc12-134">OData クエリで列の選択</span><span class="sxs-lookup"><span data-stu-id="3dc12-134">Selecting columns in an OData query</span></span>

<span data-ttu-id="3dc12-135">Dataverse Web API を介して仮想テーブルをクエリする場合、**$select** システム クエリ オプションを使用してクエリに含まれる列の数を制限し、結果を返す必要がある列を定義できます。</span><span class="sxs-lookup"><span data-stu-id="3dc12-135">When querying a virtual table through the Dataverse Web API, you can limit the number of columns included in the query by using the **$select** system query option, and define the columns for which you need results returned.</span></span> <span data-ttu-id="3dc12-136">パフォーマンスを最大限に高めるには、外部キー列 (**_mshr_FK_** 接頭語を持つ列) をクエリから除外します。</span><span class="sxs-lookup"><span data-stu-id="3dc12-136">To maximize performance, exclude foreign key columns (those with the **_mshr_FK_** prefix) from the query.</span></span>

<span data-ttu-id="3dc12-137">たとえば、次の **mshr_hcmworkerbaseentity** エンティティに対するクエリには、外部キー値を除き、**$select** クエリ オプション句に含まれる列のみが含まれます。</span><span class="sxs-lookup"><span data-stu-id="3dc12-137">For example, the following query against the **mshr_hcmworkerbaseentity** entity will include only the columns included in the **$select** query option clause, excluding foreign key values.</span></span> <span data-ttu-id="3dc12-138">これにより、すべてのテーブル列を含むクエリのパフォーマンスが大幅に向上します。</span><span class="sxs-lookup"><span data-stu-id="3dc12-138">This provides significant improvements in performance over a query that includes all table columns.</span></span>

```http
GET [Organization URI]/api/data/v9.1/mshr_hcmworkerbaseentities?$select=mshr_name, mshr_firstname, mshr_gender, mshr_partynumber, mshr_phoneticfirstname, mshr_deceaseddate, mshr_nationalitycountryregion, mshr_allowrehire, mshr_electroniclocationid, mshr_middlename, mshr_knownas, mshr_professionaltitle, mshr_nativelanguageid, mshr_disabledverificationdate, mshr_personalsuffix, mshr_lastnameprefix, mshr_personbirthcity, mshr_personaltitle, mshr_phoneticlastname, mshr_namesequencedisplayas, mshr_personbirthcountryregion, mshr_isdisabled, mshr_birthdate, mshr_professionalsuffix, mshr_isfulltimestudent, mshr_education, mshr_namealias, mshr_phoneticmiddlename, mshr_personnelnumber, mshr_hcmworkerbaseentityid, mshr_motherbirthcountryregion, mshr_fatherbirthcountryregion, mshr_lastname, mshr_languageid, mshr_partytype, mshr_ethnicoriginid, mshr_citizenshipcountryregion HTTP/1.1
Accept: application/json
OData-MaxVersion: 4.0
OData-Version: 4.0
```

<span data-ttu-id="3dc12-139">選択する列の数を制限するという推奨事項は、**$expand** クエリ オプションを使用して、ナビゲーション プロパティを介して関連する仮想テーブルにクエリを展開する場合にも適用されます。</span><span class="sxs-lookup"><span data-stu-id="3dc12-139">The recommendation to limit the number of columns selected also applies when using the **$expand** query option to expand the query to related virtual tables through navigation properties.</span></span> <span data-ttu-id="3dc12-140">たとえば、次のクエリには、**mshr_hcmworkerbaseentity** エンティティの列と、**mshr_dirpersonentity** エンティティの拡張列が含まれています。</span><span class="sxs-lookup"><span data-stu-id="3dc12-140">For example, the following query includes columns from the **mshr_hcmworkerbaseentity** entity with expanded columns from the **mshr_dirpersonentity** entity.</span></span> <span data-ttu-id="3dc12-141">**$select** クエリ オプションは **$expand** クエリ オプション句に含まれます。</span><span class="sxs-lookup"><span data-stu-id="3dc12-141">Note that the **$select** query option is also included in the **$expand** query option clause.</span></span>

```http
GET [Organization URI]/api/data/v9.1/mshr_hcmworkerbaseentities?$select=mshr_name, mshr_firstname, mshr_gender, mshr_partynumber, mshr_phoneticfirstname, mshr_deceaseddate, mshr_nationalitycountryregion, mshr_allowrehire, mshr_electroniclocationid, mshr_middlename, mshr_knownas&$expand=mshr_FK_Person_id($select=mshr_addressstreet, mshr_addresscity, mshr_addressstate, mshr_addresszipcode) HTTP/1.1
Accept: application/json
OData-MaxVersion: 4.0
OData-Version: 4.0
```

<span data-ttu-id="3dc12-142">**$expand** クエリ オプション句で **$select** クエリ オプションを使用してデータを取得する場合、エンティティ間のナビゲーション プロパティが多対一の関係の場合は、通常のパフォーマンスが向上します。</span><span class="sxs-lookup"><span data-stu-id="3dc12-142">When using this method of retrieving data with the **$select** query option in the **$expand** query option clause, you will typically see greater performance improvements when the navigation property between the entities is a many-to-one relationship.</span></span> <span data-ttu-id="3dc12-143">一対多の関係を展開する場合、クエリ実行時間の同じ減少が見られない場合があります。</span><span class="sxs-lookup"><span data-stu-id="3dc12-143">You may not see the same decrease in query execution time when expanding a one-to-many relationship.</span></span> <span data-ttu-id="3dc12-144">Dataverse 仮想テーブルのリレーションシップの定義の詳細については 、[テーブル リレーションシップ](/powerapps/maker/data-platform/create-edit-entity-relationships) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="3dc12-144">For more information on relationship definition for Dataverse virtual tables, see [Table relationships](/powerapps/maker/data-platform/create-edit-entity-relationships).</span></span>

<span data-ttu-id="3dc12-145">Dataverse Web APIで **$select** および **$expand** システム クエリ オプションを使用する方法の詳細については、[クエリで関連エンティティレコードを取得する](/powerapps/developer/data-platform/webapi/retrieve-related-entities-query) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="3dc12-145">For more information on using the **$select** and **$expand** system query options in the Dataverse Web API, see [Retrieve related entity records with a query](/powerapps/developer/data-platform/webapi/retrieve-related-entities-query).</span></span>

#### <a name="selecting-columns-in-power-bi"></a><span data-ttu-id="3dc12-146">Power BI で列を選択します</span><span class="sxs-lookup"><span data-stu-id="3dc12-146">Selecting columns in Power BI</span></span>

<span data-ttu-id="3dc12-147">Dataverse 仮想テーブルに対して Power BI レポートを構築する際にパフォーマンスが低下が見られる場合、レポートのテーブルから選択した列から外部キー列を除外することでパフォーマンスを改善できます。</span><span class="sxs-lookup"><span data-stu-id="3dc12-147">If you experience any of the aforementioned indications of slow performance when building a Power BI report against a Dataverse virtual table, you can improve the performance by excluding foreign key columns from the columns selected from the table for the report.</span></span> <span data-ttu-id="3dc12-148">たとえば、Power BI Desktop を使用して **mshr_hcmworkerbaseentity** エンティティに対してレポートを作成する場合は、次の手順を使用して、レポート クエリに含めたい列を選択できます。</span><span class="sxs-lookup"><span data-stu-id="3dc12-148">For example, if you are using Power BI Desktop to create a report against the **mshr_hcmworkerbaseentity** entity, you can use the following steps to select the columns you want included in the report query.</span></span>

1. <span data-ttu-id="3dc12-149">Power BI Desktop で、アクション リボンの **データの取得** ドロップダウン リストから **詳細...** を選択します。</span><span class="sxs-lookup"><span data-stu-id="3dc12-149">In Power BI Desktop, select **More...** from the **Get data** drop-down list on the action ribbon.</span></span>
2. <span data-ttu-id="3dc12-150">**データの取得** ウィンドウで、検索ボックスの **Common Data Service** に入力し、**Common Data Service** コネクタを選択して、**接続** を選択します。</span><span class="sxs-lookup"><span data-stu-id="3dc12-150">In the **Get Data** window, enter **Common Data Service** in the search box, select the **Common Data Service** connector, and select **Connect**.</span></span>
3. <span data-ttu-id="3dc12-151">Common Data Service ウィンドウの **サーバーの URL** に Dataverse 環境の組織 URI を入力し **OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="3dc12-151">In the **Server Url** field of the Common Data Service window, enter the organization URI for your Dataverse environment, and select **OK**.</span></span>
  
   ![Dataverse 環境の URI を入力](./media/PowerBIDataverseURLSetup.png)
  
4. <span data-ttu-id="3dc12-153">ナビゲーター ウィンドウで、**エンティティ** ノードを展開します。</span><span class="sxs-lookup"><span data-stu-id="3dc12-153">In the Navigator window, expand the **Entities** node.</span></span>
5. <span data-ttu-id="3dc12-154">検索ボックスに **mshr_hcmworkerbaseentity** を入力し、エンティティを選択します。</span><span class="sxs-lookup"><span data-stu-id="3dc12-154">In the search box, enter **mshr_hcmworkerbaseentity**, and select the entity.</span></span>
6. <span data-ttu-id="3dc12-155">**データの変革** を選択します。</span><span class="sxs-lookup"><span data-stu-id="3dc12-155">Select **Transform Data**.</span></span>
7. <span data-ttu-id="3dc12-156">高度なクエリ エディター ウィンドウで、**高度なエディター** を選択します。</span><span class="sxs-lookup"><span data-stu-id="3dc12-156">In the Power Query Editor window, select **Advanced Editor**.</span></span>
8. <span data-ttu-id="3dc12-157">**高度なエディター** ウィンドウで、クエリを以下のように更新し、必要に応じて列を追加または削除します。</span><span class="sxs-lookup"><span data-stu-id="3dc12-157">In the **Advanced Editor** window, update the query to look like the below, adding or removing any columns to the array as needed.</span></span>

   ```
   let
     Source = Cds.Entities("[Your Organization URI]", [ReorderColumns=null, UseFormattedValue=null]),
     entities = Source{[Group="entities"]}[Data],
     mshr_hcmworkerbaseentities = entities{[EntitySetName="mshr_hcmworkerbaseentities"]}[Data],
     selectedWorkerBaseEntityColumns=Table.SelectColumns(mshr_hcmworkerbaseentities,{"mshr_name","mshr_partynumber", "mshr_professionaltitle","mshr_birthdate"})
   in
     selectedWorkerBaseEntityColumns
   ```
   ![高度なクエリ エディターの詳細エディターでクエリを更新します](./media/HcmWorkerBaseEntityPowerQueryEditor.png)

9. <span data-ttu-id="3dc12-159">**完了** を選択します。</span><span class="sxs-lookup"><span data-stu-id="3dc12-159">Select **Done**.</span></span>

   > [!NOTE]
   > <span data-ttu-id="3dc12-160">更新前にクエリからタイプ 429 のエラーを以前に受け取った場合は、クエリを更新して正常に完了する前に、再試行期間を待つ必要がある場合があります。</span><span class="sxs-lookup"><span data-stu-id="3dc12-160">If you previously received an error of type 429 from the query prior to updating, you may need to wait for the retry period prior to refreshing the query for it to complete successully.</span></span>

10. <span data-ttu-id="3dc12-161">高度なクエリ エディター アクション リボンで **閉じる & 適用** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="3dc12-161">Click **Close & Apply** on the Power Query Editor action ribbon.</span></span>

<span data-ttu-id="3dc12-162">仮想テーブルから選択した列に対して Power BI レポートの構築を開始できます。</span><span class="sxs-lookup"><span data-stu-id="3dc12-162">You're then able to begin building your Power BI report against the columns selected from the virtual table.</span></span>

#### <a name="selecting-columns-in-power-apps"></a><span data-ttu-id="3dc12-163">Power Apps で列を選択します</span><span class="sxs-lookup"><span data-stu-id="3dc12-163">Selecting columns in Power Apps</span></span>

<span data-ttu-id="3dc12-164">Dataverse Web API クエリおよび Power BI と同様に、関連するテーブルの列をアプリから除外することにより、Dataverse 仮想テーブルに基づく Power Apps のクエリ パフォーマンスを向上させることができます。</span><span class="sxs-lookup"><span data-stu-id="3dc12-164">Similar to Dataverse Web API queries and Power BI, you can improve query performance for Power Apps based on Dataverse virtual tables by excluding columns of related tables from your app.</span></span> <span data-ttu-id="3dc12-165">関連テーブルの列がページに含まれている場合、データをフェッチするために作成されたリ要求 URL には、関連テーブルの外部キー プロパティが含まれます。</span><span class="sxs-lookup"><span data-stu-id="3dc12-165">If any columns from a related table have been included on a page, then the request URL constructed to fetch the data will include foreign key properties of the related table.</span></span> <span data-ttu-id="3dc12-166">これは、上記の [OData クエリで列を選択](#selecting-columns-in-power-apps) した例のように、追加のデータ ルックアップが発生してパフォーマンスを低下させます。</span><span class="sxs-lookup"><span data-stu-id="3dc12-166">This, as in the examples of [Selecting columns in an OData Query](#selecting-columns-in-power-apps) above, reduces performance by causing additional data lookups.</span></span>

<span data-ttu-id="3dc12-167">これを回避するために、関連するテーブルのデータ フィールドが Power App のどのデータ フォームにも含まれていないことを検証できます。</span><span class="sxs-lookup"><span data-stu-id="3dc12-167">To work around this, you can validate that no data fields from related tables have been included on any data form of your Power App.</span></span>

1. <span data-ttu-id="3dc12-168">ツリー ビュー ペインで、画面のデータ フォームを選択します。</span><span class="sxs-lookup"><span data-stu-id="3dc12-168">In the Tree view pane, select the data form for the screen.</span></span>
2. <span data-ttu-id="3dc12-169">**プロパティ** ペインで、**フィールド** プロパティで **編集** を選択します。</span><span class="sxs-lookup"><span data-stu-id="3dc12-169">In the **Properties** pane, select **Edit** on the **Fields** property.</span></span>
3. <span data-ttu-id="3dc12-170">**データ** ペインで、選択したフィールドのいずれもデータ ソースの仮想テーブルのフィールドではないことを確認します。</span><span class="sxs-lookup"><span data-stu-id="3dc12-170">In the **Data** pane, verify that none of the selected fields are fields of the virtual table of the data source.</span></span>

<span data-ttu-id="3dc12-171">たとえば、アプリのページに含まれるデータ フィールドの 1 つが、**作業者** が関連テーブルである **ThisItem.Worker.Name** などの別のテーブルを参照している場合、データのフェッチのパフォーマンスが低下しする可能性があります。</span><span class="sxs-lookup"><span data-stu-id="3dc12-171">For example, if one of the data fields included on a page in the app references another table, such as **ThisItem.Worker.Name**, where **Worker** is the related table, there is a potential for reduced performance in fetching the data.</span></span>

<span data-ttu-id="3dc12-172">[Power Apps 監視](/powerapps/maker/monitor-overview) を使用すると、必要な列だけが Power App のデータを取得するためにクエリに含まれている必要があります。</span><span class="sxs-lookup"><span data-stu-id="3dc12-172">You can use the [Power Apps Monitor](/powerapps/maker/monitor-overview) to ensure that only the columns you need are being included in the query to get the data for the Power App.</span></span> <span data-ttu-id="3dc12-173">getRows 操作用に作成された URL を表示して、アプリ用に選択した列がデータの取得に最適であることを確認できます。</span><span class="sxs-lookup"><span data-stu-id="3dc12-173">You can view the URL constructed for the getRows operation to ensure the columns you have selected for your app will be optimal for retrieving the data.</span></span>

![Power Apps 監視を使用した getData 操作の分析](./media/HcmWorkerBaseEntityPowerAppsMonitor.png)

### <a name="filtering-the-data-query"></a><span data-ttu-id="3dc12-175">データ クエリのフィルター処理</span><span class="sxs-lookup"><span data-stu-id="3dc12-175">Filtering the data query</span></span>

<span data-ttu-id="3dc12-176">クエリの実行のパフォーマンスを改善するもう 1 つの方法は、クエリ結果で返されるレコードの数を制限する方法です。</span><span class="sxs-lookup"><span data-stu-id="3dc12-176">Another method for improving query execution performance is to limit the number of records returned in the query results.</span></span> <span data-ttu-id="3dc12-177">これを行うには、結果をフィルタリングして、必要なレコードのみを受信するようにします。</span><span class="sxs-lookup"><span data-stu-id="3dc12-177">You can do this by filtering the results to ensure that you are only receiving the records you need.</span></span>

<span data-ttu-id="3dc12-178">クエリ データのフィルター処理の詳細については、[フィルタ結果](/powerapps/developer/data-platform/webapi/query-data-web-api#filter-results) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="3dc12-178">See [Filter results](/powerapps/developer/data-platform/webapi/query-data-web-api#filter-results) for more information on filtering query data.</span></span>

### <a name="limiting-the-page-size-of-the-query"></a><span data-ttu-id="3dc12-179">クエリのページ サイズの制限</span><span class="sxs-lookup"><span data-stu-id="3dc12-179">Limiting the page size of the query</span></span>

<span data-ttu-id="3dc12-180">大規模なデータ セットを使用している場合は、データ クエリに `odata.maxpagesize` 優先設定ヘッダーーを追加することで、クエリ結果を複数のページに分割できます。</span><span class="sxs-lookup"><span data-stu-id="3dc12-180">If you're working with large data sets, you can divide query results into multiple pages by adding the `odata.maxpagesize` preference header to data queries.</span></span>

<span data-ttu-id="3dc12-181">ページングの詳細については、[ページに返すエンティティの数の指定](/powerapps/developer/data-platform/webapi/query-data-web-api#specify-the-number-of-entities-to-return-in-a-page) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="3dc12-181">For more information on paging, see [Specify the number of entities to return in a page](/powerapps/developer/data-platform/webapi/query-data-web-api#specify-the-number-of-entities-to-return-in-a-page).</span></span>

## <a name="see-also"></a><span data-ttu-id="3dc12-182">参照</span><span class="sxs-lookup"><span data-stu-id="3dc12-182">See also</span></span>

- [<span data-ttu-id="3dc12-183">構成 Dataverse 仮想テーブル</span><span class="sxs-lookup"><span data-stu-id="3dc12-183">Configure Dataverse virtual tables</span></span>](hr-admin-integration-common-data-service-virtual-entities.md)
- [<span data-ttu-id="3dc12-184">Human Resources 仮想テーブルに関するよく寄せられる質問</span><span class="sxs-lookup"><span data-stu-id="3dc12-184">Human Resources virtual tables FAQ</span></span>](hr-admin-virtual-entity-faq.md)
- [<span data-ttu-id="3dc12-185">スロットリングに関するよく寄せられる質問</span><span class="sxs-lookup"><span data-stu-id="3dc12-185">Throttling FAQ</span></span>](./hr-admin-integration-throttling-faq.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]