---
title: データ エンティティの会社間動作
description: このトピックでは、データ エンティティと企業間コンセプトとの関係について説明します。 データエンティティのこの側面を理解するには、テーブルとビューが企業間の概念をどのように適用するのかを理解する必要があります。 したがって、このトピックでは、テーブルとビューの概要を説明し、データ エンティティの関連性について説明します。
author: Sunil-Garg
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Developer
ms.reviewer: sericks
ms.custom: 25371
ms.assetid: f293d97a-9f70-4c45-91d4-574731892353
ms.search.region: Global
ms.author: sunilg
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 9cfc3ec06b82c5aa22d0f1fec2eb94490876cc25
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 12/05/2020
ms.locfileid: "4679360"
---
# <a name="cross-company-behavior-of-data-entities"></a><span data-ttu-id="89c33-105">データ エンティティの会社間動作</span><span class="sxs-lookup"><span data-stu-id="89c33-105">Cross-company behavior of data entities</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="89c33-106">このトピックでは、データ エンティティと企業間コンセプトとの関係について説明します。</span><span class="sxs-lookup"><span data-stu-id="89c33-106">This topic provides information about how data entities interact with the cross-company concept.</span></span> <span data-ttu-id="89c33-107">データエンティティのこの側面を理解するには、テーブルとビューが企業間の概念をどのように適用するのかを理解する必要があります。</span><span class="sxs-lookup"><span data-stu-id="89c33-107">To understand this aspect of data entities, you must understand how tables and views apply the cross-company concept.</span></span> <span data-ttu-id="89c33-108">したがって、このトピックでは、テーブルとビューの概要を説明し、データ エンティティの関連性について説明します。</span><span class="sxs-lookup"><span data-stu-id="89c33-108">Therefore, this topic begins with a brief review of tables and views, and then explains how data entities are related.</span></span>

## <a name="review-of-tables-and-views-for-cross-company"></a><span data-ttu-id="89c33-109">会社間のテーブルとビューの確認</span><span class="sxs-lookup"><span data-stu-id="89c33-109">Review of tables and views for cross-company</span></span>

<span data-ttu-id="89c33-110">各テーブルには **SaveDataPerCompany** プロパティがあり、各ビューには **AllowCrossCompany** プロパティがあります。</span><span class="sxs-lookup"><span data-stu-id="89c33-110">Each table has a **SaveDataPerCompany** property, and each view has a **AllowCrossCompany** property.</span></span> <span data-ttu-id="89c33-111">次のテーブルにこれらの 2 つのプロパティを示します。</span><span class="sxs-lookup"><span data-stu-id="89c33-111">The following table describes these two properties.</span></span>

|      &nbsp;            | <span data-ttu-id="89c33-112">テーブル</span><span class="sxs-lookup"><span data-stu-id="89c33-112">Table</span></span> | <span data-ttu-id="89c33-113">表示</span><span class="sxs-lookup"><span data-stu-id="89c33-113">View</span></span> |
|------------------------|-------|------|
| <span data-ttu-id="89c33-114">プロパティ名</span><span class="sxs-lookup"><span data-stu-id="89c33-114">Property name</span></span>          | <span data-ttu-id="89c33-115">SaveDataPerCompany</span><span class="sxs-lookup"><span data-stu-id="89c33-115">SaveDataPerCompany</span></span> | <span data-ttu-id="89c33-116">AllowCrossCompany</span><span class="sxs-lookup"><span data-stu-id="89c33-116">AllowCrossCompany</span></span> |
| <span data-ttu-id="89c33-117">関連する CRUD モード</span><span class="sxs-lookup"><span data-stu-id="89c33-117">Relevant CRUD mode</span></span>     | <span data-ttu-id="89c33-118">CUD</span><span class="sxs-lookup"><span data-stu-id="89c33-118">CUD</span></span> | <span data-ttu-id="89c33-119">R</span><span class="sxs-lookup"><span data-stu-id="89c33-119">R</span></span> |
| <span data-ttu-id="89c33-120">効果のタイミング</span><span class="sxs-lookup"><span data-stu-id="89c33-120">Timing of effect</span></span>       | <span data-ttu-id="89c33-121">実行時間、デザイン時</span><span class="sxs-lookup"><span data-stu-id="89c33-121">Run time, Design time</span></span> | <span data-ttu-id="89c33-122">ほとんどの場合は実行時。</span><span class="sxs-lookup"><span data-stu-id="89c33-122">Run time, mostly.</span></span> <span data-ttu-id="89c33-123">デザイン時に、この設定によりビューは選択したフィールド リストに **dataAreaId** を持ちます。</span><span class="sxs-lookup"><span data-stu-id="89c33-123">At design time, this setting causes the view to have **dataAreaId** in its list of selected fields.</span></span> <span data-ttu-id="89c33-124">ただし、特定の **dataAreaId** 値のフィルターが、後の実行時に追加されます。</span><span class="sxs-lookup"><span data-stu-id="89c33-124">However, the filter for a specific **dataAreaId** value is added later, at run time.</span></span> |
| <span data-ttu-id="89c33-125">値の意味 = はい</span><span class="sxs-lookup"><span data-stu-id="89c33-125">Meaning of value = Yes</span></span> | <span data-ttu-id="89c33-126">デザイン時には、フィールドがアプリケーション オブジェクト ツリー (AOT) に表示されていなくても、システムはテーブルに **dataAreaId** フィールドを自動的に *追加* します。</span><span class="sxs-lookup"><span data-stu-id="89c33-126">At design time, the system automatically *adds* a **dataAreaId** field to the table, even though the field isn't displayed in the Application Object Tree (AOT).</span></span> <span data-ttu-id="89c33-127">テーブルのすべてのレコードには、それが所属する会社 (または法人) がタグ付けされています。</span><span class="sxs-lookup"><span data-stu-id="89c33-127">Every record in the table is tagged with the company (or legal entity) that it belongs to.</span></span> <span data-ttu-id="89c33-128">システムは自動的に SQL **Where** 句にフィルターを *追加* して、返された行セットを 1 つの **dataAreaId** 値に制限します。</span><span class="sxs-lookup"><span data-stu-id="89c33-128">The system automatically *adds* a filter to the SQL **Where** clause to limit the returned set of rows to one **dataAreaId** value.</span></span> | <span data-ttu-id="89c33-129">実行時に、システムは、基になる Microsoft SQL Server システムに送信する SQL **Select** ステートメントの **Where** 句に **dataAreaId** のフィルターを自動的に追加 *できません*。</span><span class="sxs-lookup"><span data-stu-id="89c33-129">At run time, the system does *not* automatically add a filter for **dataAreaId** on the **Where** clause of the SQL **Select** statement that it sends to the underlying Microsoft SQL Server system.</span></span> <span data-ttu-id="89c33-130">したがって、ビューからの SQL **Select** ステートメントは、*複数の* 企業のレコードを含む一連のレコードを返すことができます。</span><span class="sxs-lookup"><span data-stu-id="89c33-130">Therefore, SQL **Select** statements from the view can return a set of records that contains records for *multiple* companies.</span></span> |
| <span data-ttu-id="89c33-131">値の意味 = いいえ</span><span class="sxs-lookup"><span data-stu-id="89c33-131">Meaning of value = No</span></span>  | <span data-ttu-id="89c33-132">システムは、テーブルに **dataAreaId** フィールドを追加 *しません*。</span><span class="sxs-lookup"><span data-stu-id="89c33-132">The system does *not* add a **dataAreaId** field to the table.</span></span> <span data-ttu-id="89c33-133">テーブルは共有テーブルであると言われています。なぜならレコードには正式な会社固有のデータが含まれていないからです。</span><span class="sxs-lookup"><span data-stu-id="89c33-133">The table is said to be a shared table, because none of its records contain any formal company-specific data.</span></span> | <span data-ttu-id="89c33-134">システムは自動的に SQL **Where** 句にフィルターを *追加* して、返された行セットを 1 つの **dataAreaId** 値に制限します。</span><span class="sxs-lookup"><span data-stu-id="89c33-134">The system automatically *adds* a filter to the SQL **Where** clause to limit the returned set of rows to one **dataAreaId** value.</span></span> <span data-ttu-id="89c33-135">ただし、ビューの *ルート* データ ソースが共有テーブルである場合、**AllowCrossCompany** プロパティは無視されます。</span><span class="sxs-lookup"><span data-stu-id="89c33-135">However, the **AllowCrossCompany** property is ignored if the *root* data source of the view is a shared table.</span></span> |

## <a name="comparisons-within-allowcrosscompany--no"></a><span data-ttu-id="89c33-136">AllowCrossCompany 内の比較 = いいえ</span><span class="sxs-lookup"><span data-stu-id="89c33-136">Comparisons within AllowCrossCompany = No</span></span>
<span data-ttu-id="89c33-137">次のスクリーンショットでは、**CustomerList** ビューに 2 つのデータ ソースがあります。</span><span class="sxs-lookup"><span data-stu-id="89c33-137">In the following screenshot, the **CustomerList** view has two data sources:</span></span>

- <span data-ttu-id="89c33-138">**ルート** – CustTable、**SaveDataPerCompany** が入っているプロパティを **はい** にセットします。</span><span class="sxs-lookup"><span data-stu-id="89c33-138">**Root** – CustTable, which has its **SaveDataPerCompany** property set to **Yes**.</span></span>
- <span data-ttu-id="89c33-139">**非ルート** – DirPartyTable、**SaveDataPerCompany** が入っているプロパティを **いいえ** にセットします。</span><span class="sxs-lookup"><span data-stu-id="89c33-139">**Non-root** – DirPartyTable, which has its **SaveDataPerCompany** property set to **No**.</span></span>

<span data-ttu-id="89c33-140">[![CustomerList ビューには 2 つのデータ ソースがあります。](./media/root.png)](./media/root.png)</span><span class="sxs-lookup"><span data-stu-id="89c33-140">[![The CustomerList view has two data sources.](./media/root.png)](./media/root.png)</span></span>

<span data-ttu-id="89c33-141">次のスクリーンショットが示すように、**CustomerList** 表示は、**AllowCrossCompany** プロパティを **いいえ** に設定しています。</span><span class="sxs-lookup"><span data-stu-id="89c33-141">The **CustomerList** view has its **AllowCrossCompany** property set to **No**, as shown in the following screenshot.</span></span>

<span data-ttu-id="89c33-142">[![AllowCrossCompany プロパティはいいえに設定しています。](./media/crosscomp.png)](./media/crosscomp.png)</span><span class="sxs-lookup"><span data-stu-id="89c33-142">[![The AllowCrossCompany property is set to No.](./media/crosscomp.png)](./media/crosscomp.png)</span></span>

<span data-ttu-id="89c33-143">**CustomerList** 表示に関する前述の情報が与えられた場合、システムは、SQL **表示の作成** ステートメントを生成して実行することによって、基盤となる SQL Server システムに表示を作成します。</span><span class="sxs-lookup"><span data-stu-id="89c33-143">Given the preceding information about the **CustomerList** view, the system creates the view in the underlying SQL Server system by generating and then running the following SQL **Create View** statement.</span></span>

```sql
CREATE VIEW [dbo].[CUSTOMERLIST] 
AS 
       SELECT T1.accountnum AS ACCOUNTNUM, 
              T1.dataareaid AS DATAAREAID,  -- AllowCrossCompany =No caused this line.
              T1.partition  AS PARTITION, 
              T1.recid      AS RECID, 
              T2.partition  AS PARTITION#2, 
              T2.name       AS NAME 
       FROM   custtable T1 
              CROSS JOIN dirpartytable T2 
       WHERE ( T1.party = T2.recid 
              AND ( T1.partition = T2.partition ) ) 
```

### <a name="making-dirpartytable-the-root-data-source"></a><span data-ttu-id="89c33-144">DirPartyTable をルート データ ソースにする</span><span class="sxs-lookup"><span data-stu-id="89c33-144">Making DirPartyTable the root data source</span></span>

<span data-ttu-id="89c33-145">[![DirPartyTable をルート データ ソースにする](./media/dirpar.png)](./media/dirpar.png)</span><span class="sxs-lookup"><span data-stu-id="89c33-145">[![Making DirPartyTable the root data source](./media/dirpar.png)](./media/dirpar.png)</span></span>

<span data-ttu-id="89c33-146">**CustomerList** ビューの 2 つのデータ ソース テーブルの位置を入れ替えて、DirPartyTable テーブルをルート データ ソースにします。</span><span class="sxs-lookup"><span data-stu-id="89c33-146">By swapping the positions of the two data source tables in the **CustomerList** view, you make the DirPartyTable table the root data source.</span></span>

```sql
CREATE VIEW [dbo].[CUSTOMERLISTPARTY] 
AS 
       SELECT T1.name       AS NAME, 
              T1.partition  AS PARTITION, 
              T1.recid      AS RECID, 
              T2.partition  AS PARTITION#2, 
              T2.accountnum AS ACCOUNTNUM 
       FROM   dirpartytable T1 
              CROSS JOIN custtable T2 
       WHERE  ( T2.party = T1.recid 
              AND ( T2.partition = T1.partition ) ) 
go 
```

<span data-ttu-id="89c33-147">この場合、SQL の **ビューの作成** ステートメントは、次の 2 つの相違点を除いて同じです。</span><span class="sxs-lookup"><span data-stu-id="89c33-147">In this case, the SQL **Create View** statement is the same, except for the following two differences:</span></span>

- <span data-ttu-id="89c33-148">**FROM** 句は、最初に DirPartyTable に言及し、次に CustTable に言及します。</span><span class="sxs-lookup"><span data-stu-id="89c33-148">The **FROM** clause mentions DirPartyTable first and CustTable second.</span></span>
- <span data-ttu-id="89c33-149">**SELECT** 列には **dataAreaId** の行が含まれて *いません* (DirPartyTable の **SaveDataPerCompany** プロパティが **No** に設定されているため)。</span><span class="sxs-lookup"><span data-stu-id="89c33-149">The **SELECT** column list does *not* include the line for **dataAreaId** (because DirPartyTable has its **SaveDataPerCompany** property set to **No**.)</span></span>

## <a name="limitations-of-tables-and-views"></a><span data-ttu-id="89c33-150">テーブルおよびビューの制限</span><span class="sxs-lookup"><span data-stu-id="89c33-150">Limitations of tables and views</span></span>
<span data-ttu-id="89c33-151">場合によっては、テーブルおよびビューの会社間の管理機能は求められるほど細かい制御ではない場合があります。</span><span class="sxs-lookup"><span data-stu-id="89c33-151">In some cases, the cross-company control features of tables and views aren't as granular control as you might require.</span></span> <span data-ttu-id="89c33-152">制限を次に示します。</span><span class="sxs-lookup"><span data-stu-id="89c33-152">Here are the limitations:</span></span>

- <span data-ttu-id="89c33-153">システム **dataAreaId** フィールド以外の会社または法人フィールドは、**dataAreaId** が行うことができる方法で自動的に認識または処理することはできません。</span><span class="sxs-lookup"><span data-stu-id="89c33-153">Company or legal entity fields other than the system **dataAreaId** field can’t be recognized or treated automatically in the that way **dataAreaId** can.</span></span>
- <span data-ttu-id="89c33-154">非ルート データソースに **dataAreaId** フィールドがある場合でも、ビューに対する会社間の動作は、ルート データソースのプロパティにはあまりにも制限されています。</span><span class="sxs-lookup"><span data-stu-id="89c33-154">The cross-company behavior for views is too restricted to the properties of the root data source, even when non-root data sources have a **dataAreaId** field.</span></span>

<span data-ttu-id="89c33-155">たとえば、これは、法人情報が **LegalEntityRecId** にあり、または共有テーブルに **dataAreaId** 列がない場合に発生する可能性があります。</span><span class="sxs-lookup"><span data-stu-id="89c33-155">For example, this might happen if the legal entity information is in **LegalEntityRecId**, or if shared tables don't have a **dataAreaId** column.</span></span>

## <a name="design-time-setting-the-primarycompanycontext-property"></a><span data-ttu-id="89c33-156">デザイン時間: PrimaryCompanyContext プロパティの設定</span><span class="sxs-lookup"><span data-stu-id="89c33-156">Design time: Setting the PrimaryCompanyContext property</span></span>
<span data-ttu-id="89c33-157">データ エンティティは、テーブルの限界を克服し、企業間機能が関係する場所を表示するのに役立ちます。</span><span class="sxs-lookup"><span data-stu-id="89c33-157">Data entities help you overcome the limitations of tables and view where cross-company functionality is concerned.</span></span> <span data-ttu-id="89c33-158">データ エンティティは **PrimaryCompanyContext** プロパティがあり、会社 ID に使用するエンティティ フィールドを指定できます。</span><span class="sxs-lookup"><span data-stu-id="89c33-158">Data entities have a **PrimaryCompanyContext** property, where you can specify the entity field to use for company identification.</span></span> <span data-ttu-id="89c33-159">このプロパティは、次のような方法で柔軟性ときめ細かな制御を提供します。</span><span class="sxs-lookup"><span data-stu-id="89c33-159">This property provides flexibility and granular control in the following ways:</span></span>

- <span data-ttu-id="89c33-160">フィールドは、エンティティの任意のデータ ソースに由来することができ、ルート データ ソースのフィールドに限定されません。</span><span class="sxs-lookup"><span data-stu-id="89c33-160">The field can be from any data source of the entity and isn't limited to fields of the root data source.</span></span>
- <span data-ttu-id="89c33-161">このフィールドは、**DataAreaId** 拡張データ型 (EDT) から拡張され、基礎となるシステム **dataAreaId** フィールドに限定されない任意のフィールドにすることができます。</span><span class="sxs-lookup"><span data-stu-id="89c33-161">The field can be any field that is extended from the **DataAreaId** extended data type (EDT), and isn't limited to an underlying system **dataAreaId** field.</span></span>
- <span data-ttu-id="89c33-162">エンティティにデータ ソースとして共有テーブルのみがあるときであっても、ユーザーの特定の状況にかなう場合は、**PrimaryCompanyContext** プロパティを使用することができます。</span><span class="sxs-lookup"><span data-stu-id="89c33-162">You can use the **PrimaryCompanyContext** property even when the entity has only shared tables as its data sources, if this makes sense for your specific situation.</span></span>

<span data-ttu-id="89c33-163">次のスクリーンショットは、**FMCustGroupEntity** エンティティの **PrimaryCompanyContext** プロパティに設定された値を示しています。</span><span class="sxs-lookup"><span data-stu-id="89c33-163">The following screenshot shows the value set for the **PrimaryCompanyContext** property on the **FMCustGroupEntity** entity.</span></span>

<span data-ttu-id="89c33-164">[![PrimaryCompanyContext プロパティ](./media/prim1.png)](./media/prim1.png)</span><span class="sxs-lookup"><span data-stu-id="89c33-164">[![The PrimaryCompanyContext property](./media/prim1.png)](./media/prim1.png)</span></span>

<span data-ttu-id="89c33-165">**PrimaryCompanyContext** 値が空でない値に設定されている場合、エンティティは共有エンティティとして動作できません。</span><span class="sxs-lookup"><span data-stu-id="89c33-165">When the **PrimaryCompanyContext** value is set to a non-empty value, the entity can't behave as a shared entity.</span></span> <span data-ttu-id="89c33-166">**dataAreaId** フィールドは、SQL **Create View** ステートメントに追加されます。</span><span class="sxs-lookup"><span data-stu-id="89c33-166">The **dataAreaId** field is added to the SQL **Create View** statement.</span></span>

```sql
CREATE VIEW [dbo].[FMCUSTGROUPENTITY] 
AS 
       SELECT T1.custgroup   AS GROUPNAME, 
              T1.description AS DESCRIPTION, 
              T1.dataareaid  AS DATAAREAID,   -- dataAreaId is added. 
              T1.recversion  AS RECVERSION, 
              T1.partition   AS PARTITION, 
              T1.recid       AS RECID 
       FROM   fmcustgroup T1 
```

## <a name="run-time-the-behavior-of-data-entities-for-cross-company"></a><span data-ttu-id="89c33-167">実行時: 会社間のデータ エンティティの動作</span><span class="sxs-lookup"><span data-stu-id="89c33-167">Run time: The behavior of data entities for cross company</span></span>
<span data-ttu-id="89c33-168">X++ コードのコンテキストでは、データ エンティティの会社間の動作はテーブルの動作に似ています。</span><span class="sxs-lookup"><span data-stu-id="89c33-168">In the context of X++ code, the cross-company behavior of data entities resembles the behavior of tables.</span></span> <span data-ttu-id="89c33-169">エンティティの **PrimaryCompanyContext** プロパティが値を持たないおよびが空白の場合、エンティティが共有テーブルと同様に動作します。</span><span class="sxs-lookup"><span data-stu-id="89c33-169">If the **PrimaryCompanyContext** property for an entity has no value and is empty, the entity behaves like a shared table.</span></span>

### <a name="x-when-primarycompanycontext-is-set"></a><span data-ttu-id="89c33-170">X++ PrimaryCompanyContext が設定されている場合</span><span class="sxs-lookup"><span data-stu-id="89c33-170">X++ when PrimaryCompanyContext is set</span></span>

<span data-ttu-id="89c33-171">次のテーブルは、**PrimaryCompanyContext** プロパティがフィールド値に設定されている場合の CRUD アクセスでのデータ エンティティの動作を示しています。</span><span class="sxs-lookup"><span data-stu-id="89c33-171">The following table describes the behavior of a data entity under CRUD access when the **PrimaryCompanyContext** property is set to a field value.</span></span> <span data-ttu-id="89c33-172">X++ と OData の両方のアクセスについて説明しています。</span><span class="sxs-lookup"><span data-stu-id="89c33-172">Both X++ and OData accesses are described.</span></span>

|  &nbsp;       | <span data-ttu-id="89c33-173">X++</span><span class="sxs-lookup"><span data-stu-id="89c33-173">X++</span></span> | <span data-ttu-id="89c33-174">OData</span><span class="sxs-lookup"><span data-stu-id="89c33-174">OData</span></span> |
|-------------|-----|-------|
| <span data-ttu-id="89c33-175">読み取り (R)</span><span class="sxs-lookup"><span data-stu-id="89c33-175">Read (R)</span></span>    | <span data-ttu-id="89c33-176">既定では、結果は *常に* **dataAreaId** = 現在の会社によってフィルター処理され、会社間データは **会社間** オプションを使用して取得できます。</span><span class="sxs-lookup"><span data-stu-id="89c33-176">By default, results are *always* filtered by **dataAreaId** = current company, and cross-company data can be fetched by using the **cross company** option.</span></span> | <span data-ttu-id="89c33-177">結果は、**dataAreaId** によってフィルター処理され *ません*。</span><span class="sxs-lookup"><span data-stu-id="89c33-177">Results are *not* filtered by **dataAreaId**.</span></span> <span data-ttu-id="89c33-178">コンシューマーは明示的にフィルター処理する必要があります。</span><span class="sxs-lookup"><span data-stu-id="89c33-178">The consumer must filter explicitly.</span></span> |
| <span data-ttu-id="89c33-179">書き込み (CUD)</span><span class="sxs-lookup"><span data-stu-id="89c33-179">Write (CUD)</span></span> | <span data-ttu-id="89c33-180">データ エンティティへの CUD アクセスは、常に現在の会社のコンテキストで行われます。</span><span class="sxs-lookup"><span data-stu-id="89c33-180">CUD access to the data entity always occurs in the context of the current company.</span></span> <span data-ttu-id="89c33-181">エンティティへの会社間 CUD アクセスが必要である場合、**changeCompany** キーワードを使用します。</span><span class="sxs-lookup"><span data-stu-id="89c33-181">If cross-company CUD access to the entity is required, use the **changeCompany** keyword.</span></span> | <span data-ttu-id="89c33-182">**PrimaryCompanyContext(myDataAreaId)** フィールドの値を設定すると、エンティティへの CUD アクセスを会社のコンシューマーによって実行できます。</span><span class="sxs-lookup"><span data-stu-id="89c33-182">CUD access to the entity can be accomplished by the consumer for any company by setting the value of the **PrimaryCompanyContext(myDataAreaId)** field.</span></span> <span data-ttu-id="89c33-183">フレームワークは必要な **ChangeCompany** アクションを処理します。</span><span class="sxs-lookup"><span data-stu-id="89c33-183">The framework handles the necessary **ChangeCompany** action.</span></span> |

<span data-ttu-id="89c33-184">次の X++ コード例は、**PrimaryCompanyContext** プロパティが **dataAreaId** に設定されている、**FMCustGroupEntity** にアクセスします。</span><span class="sxs-lookup"><span data-stu-id="89c33-184">The following X++ code example accesses **FMCustGroupEntity**, which has its **PrimaryCompanyContext** property set to **dataAreaId**.</span></span>

<span data-ttu-id="89c33-185">[![PrimaryCompanyContext プロパティが DataAreaId に設定されています](./media/fmcust.png)](./media/fmcust.png)</span><span class="sxs-lookup"><span data-stu-id="89c33-185">[![PrimaryCompanyContext property set to DataAreaId](./media/fmcust.png)](./media/fmcust.png)</span></span>

<span data-ttu-id="89c33-186">[![X++ コード例は FMCustGroupEntity にアクセスします](./media/snip-550x1024.png)](./media/snip.png)</span><span class="sxs-lookup"><span data-stu-id="89c33-186">[![X++ code example accesses FMCustGroupEntity](./media/snip-550x1024.png)](./media/snip.png)</span></span>

### <a name="x-when-primarycompanycontext-is-empty"></a><span data-ttu-id="89c33-187">X++ PrimaryCompanyContext が空の場合</span><span class="sxs-lookup"><span data-stu-id="89c33-187">X++ when PrimaryCompanyContext is empty</span></span>

<span data-ttu-id="89c33-188">データ エンティティに関して **PrimaryCompanyContext** プロパティが設定されていると、ビュー スキーマに **dataAreaId** フィールドが作成され、**PrimaryCompanyContext** フィールドにマップされます。</span><span class="sxs-lookup"><span data-stu-id="89c33-188">When the **PrimaryCompanyContext** property is set on the data entity, a **dataAreaId** field is created in the view schema and mapped to the **PrimaryCompanyContext** field.</span></span> <span data-ttu-id="89c33-189">次のテーブルは、**PrimaryCompanyContext** プロパティが空の場合の CRUD アクセスでのデータ エンティティの動作を示しています。</span><span class="sxs-lookup"><span data-stu-id="89c33-189">The following table describes the behavior of a data entity under CRUD access when the **PrimaryCompanyContext** property is empty.</span></span> <span data-ttu-id="89c33-190">X++ と OData の両方のアクセスについて説明しています。</span><span class="sxs-lookup"><span data-stu-id="89c33-190">Both X++ and OData accesses are described.</span></span>

|     &nbsp;   | <span data-ttu-id="89c33-191">X++</span><span class="sxs-lookup"><span data-stu-id="89c33-191">X++</span></span>                                                                                                                              | <span data-ttu-id="89c33-192">OData</span><span class="sxs-lookup"><span data-stu-id="89c33-192">OData</span></span> |
|-------------|----------------------------------------------------------------------------------------------------------------------------------|-------|
| <span data-ttu-id="89c33-193">読み取り (R)</span><span class="sxs-lookup"><span data-stu-id="89c33-193">Read (R)</span></span>    | <span data-ttu-id="89c33-194">システム **dataAreaId** フィールドがビュー スキーマに作成されないため、結果はフィルター処理されません。</span><span class="sxs-lookup"><span data-stu-id="89c33-194">Results aren't filtered, because no system **dataAreaId** field is created on the view schema.</span></span>                                   | <span data-ttu-id="89c33-195">(R with X++ の場合と同じ)</span><span class="sxs-lookup"><span data-stu-id="89c33-195">(The same as for R with X++)</span></span> |
| <span data-ttu-id="89c33-196">書き込み (CUD)</span><span class="sxs-lookup"><span data-stu-id="89c33-196">Write (CUD)</span></span> | <span data-ttu-id="89c33-197">設定する主な企業コンテキストはありません。</span><span class="sxs-lookup"><span data-stu-id="89c33-197">There is no primary company context to set.</span></span> <span data-ttu-id="89c33-198">したがって、エンティティへの CUD アクセスは、常に現在の会社のコンテキストです。</span><span class="sxs-lookup"><span data-stu-id="89c33-198">Therefore, CUD access to the entity is always in the context of the current company.</span></span> | <span data-ttu-id="89c33-199">(CUD with X++ の場合と同じ)</span><span class="sxs-lookup"><span data-stu-id="89c33-199">(The same as for CUD with X++)</span></span> |

<span data-ttu-id="89c33-200">現在の例では、**FMCustomerGroupGlobalEntity** エンティティで **PrimaryCompanyContext** プロパティに割り当てられている値はありません。</span><span class="sxs-lookup"><span data-stu-id="89c33-200">In the current example, the **FMCustomerGroupGlobalEntity** entity has no value assigned to its **PrimaryCompanyContext** property.</span></span>

<span data-ttu-id="89c33-201">[![PrimaryCompanyContext プロパティに割り当てられている値はありません。](./media/ent1.png)](./media/ent1.png)</span><span class="sxs-lookup"><span data-stu-id="89c33-201">[![No value assigned to the PrimaryCompanyContext property.](./media/ent1.png)](./media/ent1.png)</span></span>

<span data-ttu-id="89c33-202">ただし、FMCustGroup テーブルの **dataAreaId** フィールドは、**LegalEntity** という名前の通常のフィールドとして **FMCustomerGroupGlobalEntity** にマップされます。</span><span class="sxs-lookup"><span data-stu-id="89c33-202">However, a **dataAreaId** field from the FMCustGroup table is mapped to the **FMCustomerGroupGlobalEntity** entity as a regular field that is named **LegalEntity**.</span></span> <span data-ttu-id="89c33-203">この例では、FMCustGroup テーブルは **FMCustomerGroupGlobalEntity** のルート データ ソースです。</span><span class="sxs-lookup"><span data-stu-id="89c33-203">In this example, the FMCustGroup table is the root data source for **FMCustomerGroupGlobalEntity**.</span></span> <span data-ttu-id="89c33-204">ただし、システムの自動メカニズムをバイパスする非公式な方法でこの **dataAreaId** フィールドを使用しています。</span><span class="sxs-lookup"><span data-stu-id="89c33-204">However, we are using this **dataAreaId** field in an informal way that bypasses the automatic mechanisms of the system.</span></span> <span data-ttu-id="89c33-205">これらすべての詳細は **法人** フィールドの次のスクリーンショットに表示されます。</span><span class="sxs-lookup"><span data-stu-id="89c33-205">All these details are shown in the following screenshot of the **LegalEntity** field.</span></span>

<span data-ttu-id="89c33-206">[![法人フィールド](./media/ent2.png)](./media/ent2.png)</span><span class="sxs-lookup"><span data-stu-id="89c33-206">[![LegalEntity field](./media/ent2.png)](./media/ent2.png)</span></span>

> [!NOTE]
> <span data-ttu-id="89c33-207">*法人エンティティ* および *データ エンティティ* の両方が *エンティティ* という語を使用していますが、混合しないでください。</span><span class="sxs-lookup"><span data-stu-id="89c33-207">Although the terms *legal entity* and *data entity* both use the word *entity*, don't confuse them.</span></span> <span data-ttu-id="89c33-208">法人およびデータ エンティティは、まったく異なる 2 つの概念です。</span><span class="sxs-lookup"><span data-stu-id="89c33-208">Legal entities and data entities are two entirely different concepts.</span></span> <span data-ttu-id="89c33-209">**PrimaryCompanyContext** プロパティが空のとき、SQL の **ビューの作成** ステートメントには、通常、システムの **dataAreaId** 列についての記述は含まれていません。</span><span class="sxs-lookup"><span data-stu-id="89c33-209">When the **PrimaryCompanyContext** property is empty, the SQL **Create View** statement usually contains no mention of a system **dataAreaId** column.</span></span> <span data-ttu-id="89c33-210">ただし、現在の例では、データ エンティティの **LegalEntity** 通常フィールドが原因で **dataAreaId** が「半参照」になります。</span><span class="sxs-lookup"><span data-stu-id="89c33-210">However, in the current example, **dataAreaId** is "half-mentioned" because of the **LegalEntity** regular field on the data entity.</span></span> <span data-ttu-id="89c33-211">このフィールドは、次の SQL ステートメントに表示されます。</span><span class="sxs-lookup"><span data-stu-id="89c33-211">This field is shown in the following SQL statement.</span></span>

```sql
CREATE VIEW [dbo].[FMCUSTOMERGROUPGLOBALENTITY] 
AS 
       SELECT T1.custgroup   AS NAME, 
              T1.description AS DESCRIPTION, 
              T1.dataareaid  AS LEGALENTITY,   -- dataAreadId is named LegalEntity. 
              T1.recversion  AS RECVERSION, 
              T1.partition   AS PARTITION, 
              T1.recid       AS RECID 
       FROM   fmcustgroup T1 
```

### <a name="purpose-of-this-example"></a><span data-ttu-id="89c33-212">この例の目的</span><span class="sxs-lookup"><span data-stu-id="89c33-212">Purpose of this example</span></span>

<span data-ttu-id="89c33-213">この例では、2 つの目的があります。</span><span class="sxs-lookup"><span data-stu-id="89c33-213">This example has two purposes:</span></span>

- <span data-ttu-id="89c33-214">バッキング テーブルが会社固有だとしても、共有データを既定で表示します。</span><span class="sxs-lookup"><span data-stu-id="89c33-214">Show shared data by default, even though the backing table might be company-specific.</span></span>
- <span data-ttu-id="89c33-215">**LegalEntity** という名のレギュラー フィールドを使用して、データ エンティティのコンシューマーが、フィルター処理または **dataAreaId** を適用するようにします。</span><span class="sxs-lookup"><span data-stu-id="89c33-215">Enable the consumer of the data entity to filter on or apply **dataAreaId** if this is required, by using the regular field that is named **LegalEntity**.</span></span>

### <a name="test-data"></a><span data-ttu-id="89c33-216">テスト データ</span><span class="sxs-lookup"><span data-stu-id="89c33-216">Test data</span></span>

<span data-ttu-id="89c33-217">**テーブル ブラウザー** ページの次のスクリーンショットは、X++ テスト コードが実行される前の **FMCustomerGroupGlobalEntity** エンティティにあるテスト データを示しています。</span><span class="sxs-lookup"><span data-stu-id="89c33-217">The following screenshot of the **Table browser** page shows the test data that is in the **FMCustomerGroupGlobalEntity** entity before the X++ test code is run.</span></span>

<span data-ttu-id="89c33-218">[![テーブル ブラウザー ページ](./media/ent3.png)](./media/ent3.png)</span><span class="sxs-lookup"><span data-stu-id="89c33-218">[![The Table browser page](./media/ent3.png)](./media/ent3.png)</span></span>

### <a name="x-code"></a><span data-ttu-id="89c33-219">X++ コード</span><span class="sxs-lookup"><span data-stu-id="89c33-219">X++ code</span></span>

<span data-ttu-id="89c33-220">共有エンティティと共に X++ テスト コードがどのように機能するかを次に示します。</span><span class="sxs-lookup"><span data-stu-id="89c33-220">Here's how the X++ test code works with the shared entity:</span></span>

- <span data-ttu-id="89c33-221">読み取りのために共有モードでデータ エンティティにアクセスします。</span><span class="sxs-lookup"><span data-stu-id="89c33-221">It accesses the data entity in shared mode for reads.</span></span>
- <span data-ttu-id="89c33-222">新しいレコードが作成されたときに、1 つの特定の会社があるデータ エンティティにアクセスします。</span><span class="sxs-lookup"><span data-stu-id="89c33-222">It accesses the data entity with one specific company when a new record is created.</span></span>

<span data-ttu-id="89c33-223">[![X++ テスト コード](./media/snip2.png)](./media/snip2.png)</span><span class="sxs-lookup"><span data-stu-id="89c33-223">[![X++ test code](./media/snip2.png)](./media/snip2.png)</span></span>
