---
title: QueryRun クラス
description: このトピックでは、QueryRun クラスについて説明します。
author: robinarh
manager: tonyafehr
ms.date: 06/25/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Developer
ms.reviewer: rhaertle
ms.search.scope: Operations
ms.search.region: Global
ms.author: rhaertle
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: f0cab450ce829f2ca697e1d3762da5b837ebd616
ms.sourcegitcommit: 7b0cec2e898ef8ee33baf72f18cdd9cba0e9399c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/25/2020
ms.locfileid: "3502858"
---
# <a name="class-queryrun"></a><span data-ttu-id="eb03c-103">クラス QueryRun</span><span class="sxs-lookup"><span data-stu-id="eb03c-103">Class QueryRun</span></span>

[!include [banner](../../includes/banner.md)]

```xpp
class QueryRun extends ObjectRun
```

<span data-ttu-id="eb03c-104">QueryRun クラスは、データベース内のテーブルをスキャンし、ユーザーによって与えられている制約を満たすレコードをフェッチして、ユーザー入力からこのような制約を収集するのに役立ちます。</span><span class="sxs-lookup"><span data-stu-id="eb03c-104">The QueryRun class traverses tables in the database, fetches records that satisfy constraints that are given by the user, and helps to gather such constraints from user input.</span></span>

## <a name="remarks"></a><span data-ttu-id="eb03c-105">備考</span><span class="sxs-lookup"><span data-stu-id="eb03c-105">Remarks</span></span>

<span data-ttu-id="eb03c-106">QueryRun オブジェクトは、データベース内のテーブルをスキャンし、ユーザーが指定した制約を満たすレコードをフェッチするために使用されます。</span><span class="sxs-lookup"><span data-stu-id="eb03c-106">QueryRun objects are used to traverse tables in the database and fetch records that satisfy the constraints that are given by the user.</span></span> <span data-ttu-id="eb03c-107">QueryRun オブジェクトは、ユーザーがそのような制限を入力できるように、ユーザーと通信することができます。</span><span class="sxs-lookup"><span data-stu-id="eb03c-107">A QueryRun object may interact with the user to let the user enter such constraints.</span></span> <span data-ttu-id="eb03c-108">クエリは、レポートに表示するデータを記述してフェッチするためにレポートにより内部的に使用されます。</span><span class="sxs-lookup"><span data-stu-id="eb03c-108">Queries are used internally by reports to delineate and fetch the data to be presented in the report.</span></span> <span data-ttu-id="eb03c-109">QueryRun オブジェクトは、クエリ オブジェクト を使用してクエリの構造を定義します (たとえば、どのテーブルを検索するか、レコードをどのように並び替えるかなど)。</span><span class="sxs-lookup"><span data-stu-id="eb03c-109">A QueryRun object relies on a Query object to define the structure of the query (for example, which tables are searched and how the records are sorted).</span></span> <span data-ttu-id="eb03c-110">QueryRun オブジェクトは、クエリの動的動作を定義しますが、クエリ オブジェクトはクエリの静的特性を定義します。</span><span class="sxs-lookup"><span data-stu-id="eb03c-110">A QueryRun object defines the dynamic behavior of the query, whereas a Query object defines the static characteristics of the query.</span></span>

## <a name="examples"></a><span data-ttu-id="eb03c-111">例</span><span class="sxs-lookup"><span data-stu-id="eb03c-111">Examples</span></span>

<span data-ttu-id="eb03c-112">次の例では、アプリケーション オブジェクト ツリー (AOT) での顧客という名前のクエリがあり、そこに 1 つのデータ ソース CustTable テーブルがあると見なされます。</span><span class="sxs-lookup"><span data-stu-id="eb03c-112">In the following example, it is assumed that there is a query named Customer in the Application Object Tree (AOT), and that it has one data source, the CustTable table.</span></span>

```xpp
static void example() 
{ 
    // Create a QueryRun object from a query stored in the AOT. 
    QueryRun qr = new QueryRun ("Customer"); 
    CustTable customerRecord; 
    // Display a window enabling the user to choose which records to print. 
    if (qr.prompt()) 
    { 
        // The user clicked OK. 
        while (qr.next()) 
        { 
            // Get the fetched record. 
            CustomerRecord = qr.GetNo(1); 
            // Do something with it 
            print CustomerRecord.AccountNum; 
        } 
    } 
    else 
    { 
        // The user pressed Cancel, so do nothing. 
    } 
}
```

## <a name="methods"></a><span data-ttu-id="eb03c-113">メソッド</span><span class="sxs-lookup"><span data-stu-id="eb03c-113">Methods</span></span>

| <span data-ttu-id="eb03c-114">方法</span><span class="sxs-lookup"><span data-stu-id="eb03c-114">Method</span></span>                                                                                                         | <span data-ttu-id="eb03c-115">説明</span><span class="sxs-lookup"><span data-stu-id="eb03c-115">Description</span></span>                                                                                                                               |
|----------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="eb03c-116">public boolean allowCheck(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="eb03c-116">public boolean allowCheck(\[boolean value\])</span></span>                                                                   |                                                                                                                                           |
| <span data-ttu-id="eb03c-117">public boolean allowCrossCompany(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="eb03c-117">public boolean allowCrossCompany(\[boolean value\])</span></span>                                                            |                                                                                                                                           |
| <span data-ttu-id="eb03c-118">public boolean canPage(\[boolean skipOrderByCheck\], \[boolean throwIfNotPagable\], \[boolean isValuePaging\])</span><span class="sxs-lookup"><span data-stu-id="eb03c-118">public boolean canPage(\[boolean skipOrderByCheck\], \[boolean throwIfNotPagable\], \[boolean isValuePaging\])</span></span> |                                                                                                                                           |
| <span data-ttu-id="eb03c-119">public boolean changed(TableId table, \[int occurrence\])</span><span class="sxs-lookup"><span data-stu-id="eb03c-119">public boolean changed(TableId table, \[int occurrence\])</span></span>                                                      | <span data-ttu-id="eb03c-120">QueryRun.next メソッドの最後の呼び出し以降に、指定されたデータ ソースが新しい値をフェッチしたかどうかを判断します。</span><span class="sxs-lookup"><span data-stu-id="eb03c-120">Determines whether the specified data source has fetched a new value since the last call to the QueryRun.next method.</span></span>                     |
| <span data-ttu-id="eb03c-121">public str changedBy(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="eb03c-121">public str changedBy(\[str value\])</span></span>                                                                            | <span data-ttu-id="eb03c-122">アプリケーション オブジェクトを最後に変更したユーザーの名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="eb03c-122">Gets or sets the name of the user who last changed the application object.</span></span>                                                                |
| <span data-ttu-id="eb03c-123">public Date changedDate(\[Date value\])</span><span class="sxs-lookup"><span data-stu-id="eb03c-123">public Date changedDate(\[Date value\])</span></span>                                                                        | <span data-ttu-id="eb03c-124">アプリケーション オブジェクトが最後に変更された日付を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="eb03c-124">Gets or sets the date an application object was last changed.</span></span>                                                                             |
| <span data-ttu-id="eb03c-125">public boolean changedNo(int dataSourceNo)</span><span class="sxs-lookup"><span data-stu-id="eb03c-125">public boolean changedNo(int dataSourceNo)</span></span>                                                                     |                                                                                                                                           |
| <span data-ttu-id="eb03c-126">public str changedTime(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="eb03c-126">public str changedTime(\[str value\])</span></span>                                                                          | <span data-ttu-id="eb03c-127">アプリケーション オブジェクトが最後に変更された時刻を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="eb03c-127">Gets or sets the time an application object was last changed.</span></span>                                                                             |
| <span data-ttu-id="eb03c-128">public str createdBy(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="eb03c-128">public str createdBy(\[str value\])</span></span>                                                                            | <span data-ttu-id="eb03c-129">アプリケーション オブジェクトを作成したユーザーの名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="eb03c-129">Gets or sets the name of the user who created the application object.</span></span>                                                                     |
| <span data-ttu-id="eb03c-130">public Date creationDate(\[Date value\])</span><span class="sxs-lookup"><span data-stu-id="eb03c-130">public Date creationDate(\[Date value\])</span></span>                                                                       | <span data-ttu-id="eb03c-131">アプリケーション オブジェクトが作成された日付を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="eb03c-131">Gets or sets the date an application object was created.</span></span>                                                                                  |
| <span data-ttu-id="eb03c-132">public str creationTime(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="eb03c-132">public str creationTime(\[str value\])</span></span>                                                                         |                                                                                                                                           |
| <span data-ttu-id="eb03c-133">public str description(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="eb03c-133">public str description(\[str value\])</span></span>                                                                          |                                                                                                                                           |
| <span data-ttu-id="eb03c-134">public boolean equal(Object obj)</span><span class="sxs-lookup"><span data-stu-id="eb03c-134">public boolean equal(Object obj)</span></span>                                                                               | <span data-ttu-id="eb03c-135">指定されたオブジェクトが現在のオブジェクトと等しいかどうかを判定します。</span><span class="sxs-lookup"><span data-stu-id="eb03c-135">Determines whether the specified object is equal to the current object.</span></span>                                                                   |
| <span data-ttu-id="eb03c-136">public str form(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="eb03c-136">public str form(\[str value\])</span></span>                                                                                 |                                                                                                                                           |
| <span data-ttu-id="eb03c-137">public Common get(TableId table, \[int occurrence\])</span><span class="sxs-lookup"><span data-stu-id="eb03c-137">public Common get(TableId table, \[int occurrence\])</span></span>                                                           | <span data-ttu-id="eb03c-138">次のメソッドの前の呼び出しによってフェッチされたレコードを取得します。</span><span class="sxs-lookup"><span data-stu-id="eb03c-138">Retrieves the record fetched by the previous call to next method.</span></span>                                                                         |
| <span data-ttu-id="eb03c-139">public System.Type getImpExpDataContractType()</span><span class="sxs-lookup"><span data-stu-id="eb03c-139">public System.Type getImpExpDataContractType()</span></span>                                                                 |                                                                                                                                           |
| <span data-ttu-id="eb03c-140">public Common getNo(int dataSourceNo)</span><span class="sxs-lookup"><span data-stu-id="eb03c-140">public Common getNo(int dataSourceNo)</span></span>                                                                          | <span data-ttu-id="eb03c-141">QueryRun.next メソッドの前の呼び出しによってフェッチされたレコードを取得します。</span><span class="sxs-lookup"><span data-stu-id="eb03c-141">Retrieves the record fetched by the previous call to QueryRun.next Method.</span></span>                                                                |
| <span data-ttu-id="eb03c-142">public boolean importable()</span><span class="sxs-lookup"><span data-stu-id="eb03c-142">public boolean importable()</span></span>                                                                                    |                                                                                                                                           |
| <span data-ttu-id="eb03c-143">public boolean interactive(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="eb03c-143">public boolean interactive(\[boolean value\])</span></span>                                                                  |                                                                                                                                           |
| <span data-ttu-id="eb03c-144">public boolean isPositionPagingEnabled()</span><span class="sxs-lookup"><span data-stu-id="eb03c-144">public boolean isPositionPagingEnabled()</span></span>                                                                       |                                                                                                                                           |
| <span data-ttu-id="eb03c-145">public boolean isQueryTimedout()</span><span class="sxs-lookup"><span data-stu-id="eb03c-145">public boolean isQueryTimedout()</span></span>                                                                               |                                                                                                                                           |
| <span data-ttu-id="eb03c-146">public boolean isValueBasedPagingEnabled()</span><span class="sxs-lookup"><span data-stu-id="eb03c-146">public boolean isValueBasedPagingEnabled()</span></span>                                                                     |                                                                                                                                           |
| <span data-ttu-id="eb03c-147">public int literals(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="eb03c-147">public int literals(\[int value\])</span></span>                                                                             |                                                                                                                                           |
| <span data-ttu-id="eb03c-148">public Guid loadCsv(str fileName)</span><span class="sxs-lookup"><span data-stu-id="eb03c-148">public Guid loadCsv(str fileName)</span></span>                                                                              |                                                                                                                                           |
| <span data-ttu-id="eb03c-149">public Guid loadXml(str fileName)</span><span class="sxs-lookup"><span data-stu-id="eb03c-149">public Guid loadXml(str fileName)</span></span>                                                                              |                                                                                                                                           |
| <span data-ttu-id="eb03c-150">public str name(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="eb03c-150">public str name(\[str value\])</span></span>                                                                                 | <span data-ttu-id="eb03c-151">フォーム、レポート、テーブル、クエリ、または他のアプリケーション オブジェクトを識別するためのコードで使用される名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="eb03c-151">Gets or sets the name that is used in code to identify a form, report, table, query, or other application object.</span></span> |
| <span data-ttu-id="eb03c-152">public QueryRun newObject(AnyType source)</span><span class="sxs-lookup"><span data-stu-id="eb03c-152">public QueryRun newObject(AnyType source)</span></span>                                                                      |                                                                                                                                           |
| <span data-ttu-id="eb03c-153">public boolean next()</span><span class="sxs-lookup"><span data-stu-id="eb03c-153">public boolean next()</span></span>                                                                                          | <span data-ttu-id="eb03c-154">クエリから次のレコードを取得します。</span><span class="sxs-lookup"><span data-stu-id="eb03c-154">Retrieves the next record from the query.</span></span>                                                                                                 |
| <span data-ttu-id="eb03c-155">public int nextUniqueId(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="eb03c-155">public int nextUniqueId(\[int value\])</span></span>                                                                         |                                                                                                                                           |
| <span data-ttu-id="eb03c-156">public Guid origin(\[Guid value\])</span><span class="sxs-lookup"><span data-stu-id="eb03c-156">public Guid origin(\[Guid value\])</span></span>                                                                             |                                                                                                                                           |
| <span data-ttu-id="eb03c-157">public container pack(\[boolean doCheck\])</span><span class="sxs-lookup"><span data-stu-id="eb03c-157">public container pack(\[boolean doCheck\])</span></span>                                                                     |                                                                                                                                           |
| <span data-ttu-id="eb03c-158">public boolean prompt()</span><span class="sxs-lookup"><span data-stu-id="eb03c-158">public boolean prompt()</span></span>                                                                                        | <span data-ttu-id="eb03c-159">クエリによってフェッチするレコードを定義するためのオプションをユーザーに表示します。</span><span class="sxs-lookup"><span data-stu-id="eb03c-159">Presents, to the user, the options for defining the records to be fetched by the query.</span></span>                                                   |
| <span data-ttu-id="eb03c-160">public Query query(\[Query query\])</span><span class="sxs-lookup"><span data-stu-id="eb03c-160">public Query query(\[Query query\])</span></span>                                                                            |                                                                                                                                           |
| <span data-ttu-id="eb03c-161">public int queryType(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="eb03c-161">public int queryType(\[int value\])</span></span>                                                                            |                                                                                                                                           |
| <span data-ttu-id="eb03c-162">public boolean recordLevelSecurity(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="eb03c-162">public boolean recordLevelSecurity(\[boolean value\])</span></span>                                                          |                                                                                                                                           |
| <span data-ttu-id="eb03c-163">public ReportRun report()</span><span class="sxs-lookup"><span data-stu-id="eb03c-163">public ReportRun report()</span></span>                                                                                      |                                                                                                                                           |
| <span data-ttu-id="eb03c-164">public ReportRun reportRun()</span><span class="sxs-lookup"><span data-stu-id="eb03c-164">public ReportRun reportRun()</span></span>                                                                                   |                                                                                                                                           |
| <span data-ttu-id="eb03c-165">public boolean saved()</span><span class="sxs-lookup"><span data-stu-id="eb03c-165">public boolean saved()</span></span>                                                                                         |                                                                                                                                           |
| <span data-ttu-id="eb03c-166">public boolean saveUserSetup(\[boolean saveIt\])</span><span class="sxs-lookup"><span data-stu-id="eb03c-166">public boolean saveUserSetup(\[boolean saveIt\])</span></span>                                                               | <span data-ttu-id="eb03c-167">ユーザー設定を保存します。</span><span class="sxs-lookup"><span data-stu-id="eb03c-167">Saves the user setup.</span></span>                                                                                                                     |
| <span data-ttu-id="eb03c-168">public boolean searchable(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="eb03c-168">public boolean searchable(\[boolean value\])</span></span>                                                                   |                                                                                                                                           |
| <span data-ttu-id="eb03c-169">public boolean setCursor(Common record, \[int occurrence\])</span><span class="sxs-lookup"><span data-stu-id="eb03c-169">public boolean setCursor(Common record, \[int occurrence\])</span></span>                                                    |                                                                                                                                           |
| <span data-ttu-id="eb03c-170">public boolean setRecord(Common record, \[int occurrence\])</span><span class="sxs-lookup"><span data-stu-id="eb03c-170">public boolean setRecord(Common record, \[int occurrence\])</span></span>                                                    |                                                                                                                                           |
| <span data-ttu-id="eb03c-171">public str title(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="eb03c-171">public str title(\[str value\])</span></span>                                                                                |                                                                                                                                           |
| <span data-ttu-id="eb03c-172">public str toString()</span><span class="sxs-lookup"><span data-stu-id="eb03c-172">public str toString()</span></span>                                                                                          | <span data-ttu-id="eb03c-173">現在のオブジェクトを表す文字列を返します。</span><span class="sxs-lookup"><span data-stu-id="eb03c-173">Returns a string that represents the current object.</span></span>                                                                                      |
| <span data-ttu-id="eb03c-174">public boolean userUpdate(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="eb03c-174">public boolean userUpdate(\[boolean value\])</span></span>                                                                   |                                                                                                                                           |
| <span data-ttu-id="eb03c-175">public int version(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="eb03c-175">public int version(\[int value\])</span></span>                                                                              |                                                                                                                                           |
| <span data-ttu-id="eb03c-176">::public static int getQueryRowCount(Query query, int maxRows)</span><span class="sxs-lookup"><span data-stu-id="eb03c-176">::public static int getQueryRowCount(Query query, int maxRows)</span></span>                                                 |                                                                                                                                           |
| <span data-ttu-id="eb03c-177">::public static int runAndPopulate(Query sourceRuery, Common targetTable, Map queryAliasesAndTargetColumnsMap)</span><span class="sxs-lookup"><span data-stu-id="eb03c-177">::public static int runAndPopulate(Query sourceRuery, Common targetTable, Map queryAliasesAndTargetColumnsMap)</span></span> |                                                                                                                                           |
| <span data-ttu-id="eb03c-178">public void run()</span><span class="sxs-lookup"><span data-stu-id="eb03c-178">public void run()</span></span>                                                                                              | <span data-ttu-id="eb03c-179">ユーザーからクエリに関する情報を取得するために使用されるフォームを開いて、一致するレコードをフェッチします。</span><span class="sxs-lookup"><span data-stu-id="eb03c-179">Opens a form used to obtain information about the query from the user, and fetches the matching records.</span></span>                                  |
| <span data-ttu-id="eb03c-180">public void new(AnyType source)</span><span class="sxs-lookup"><span data-stu-id="eb03c-180">public void new(AnyType source)</span></span>                                                                                | <span data-ttu-id="eb03c-181">Object クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="eb03c-181">Initializes a new instance of the Object class.</span></span>                                                                                           |
| <span data-ttu-id="eb03c-182">public void addPageRange(\[Int64 startingPosition\], \[Int64 numberOfRecordsToFetch\])</span><span class="sxs-lookup"><span data-stu-id="eb03c-182">public void addPageRange(\[Int64 startingPosition\], \[Int64 numberOfRecordsToFetch\])</span></span>                         |                                                                                                                                           |
| <span data-ttu-id="eb03c-183">public void reset()</span><span class="sxs-lookup"><span data-stu-id="eb03c-183">public void reset()</span></span>                                                                                            |                                                                                                                                           |
| <span data-ttu-id="eb03c-184">public void setImportSession(Guid importSession)</span><span class="sxs-lookup"><span data-stu-id="eb03c-184">public void setImportSession(Guid importSession)</span></span>                                                               |                                                                                                                                           |
| <span data-ttu-id="eb03c-185">public void setQuerytimeout(int seconds, \[boolean raiseException\])</span><span class="sxs-lookup"><span data-stu-id="eb03c-185">public void setQuerytimeout(int seconds, \[boolean raiseException\])</span></span>                                           |                                                                                                                                           |
| <span data-ttu-id="eb03c-186">public void init()</span><span class="sxs-lookup"><span data-stu-id="eb03c-186">public void init()</span></span>                                                                                             |                                                                                                                                           |
| <span data-ttu-id="eb03c-187">public void enablePositionPaging(\[boolean enabled\])</span><span class="sxs-lookup"><span data-stu-id="eb03c-187">public void enablePositionPaging(\[boolean enabled\])</span></span>                                                          |                                                                                                                                           |
| <span data-ttu-id="eb03c-188">public void shred(Guid importSession)</span><span class="sxs-lookup"><span data-stu-id="eb03c-188">public void shred(Guid importSession)</span></span>                                                                          |                                                                                                                                           |
| <span data-ttu-id="eb03c-189">public void enableValueBasedPaging(\[boolean enable\])</span><span class="sxs-lookup"><span data-stu-id="eb03c-189">public void enableValueBasedPaging(\[boolean enable\])</span></span>                                                         |                                                                                                                                           |
| <span data-ttu-id="eb03c-190">public void bulkNext(\[boolean fetchAllData\])</span><span class="sxs-lookup"><span data-stu-id="eb03c-190">public void bulkNext(\[boolean fetchAllData\])</span></span>                                                                 |                                                                                                                                           |
| <span data-ttu-id="eb03c-191">public void applyValueBasedPaging(\[Common sourceCursor\], \[boolean isForward\])</span><span class="sxs-lookup"><span data-stu-id="eb03c-191">public void applyValueBasedPaging(\[Common sourceCursor\], \[boolean isForward\])</span></span>                              |                                                                                                                                           |

## <a name="method-allowcheck"></a><span data-ttu-id="eb03c-192">メソッド allowCheck</span><span class="sxs-lookup"><span data-stu-id="eb03c-192">Method allowCheck</span></span>

```xpp
public boolean allowCheck([boolean value])
```

### <a name="parameters---allowcheck"></a><span data-ttu-id="eb03c-193">パラメーター - allowCheck</span><span class="sxs-lookup"><span data-stu-id="eb03c-193">Parameters - allowCheck</span></span>

<span data-ttu-id="eb03c-194">値</span><span class="sxs-lookup"><span data-stu-id="eb03c-194">value</span></span>  

### <a name="return-value---allowcheck"></a><span data-ttu-id="eb03c-195">戻り値 - allowCheck</span><span class="sxs-lookup"><span data-stu-id="eb03c-195">Return Value - allowCheck</span></span>

## <a name="method-allowcrosscompany"></a><span data-ttu-id="eb03c-196">メソッド allowCrossCompany</span><span class="sxs-lookup"><span data-stu-id="eb03c-196">Method allowCrossCompany</span></span>

```xpp
public boolean allowCrossCompany([boolean value])
```

### <a name="parameters---allowcrosscompany"></a><span data-ttu-id="eb03c-197">パラメーター - allowCrossCompany</span><span class="sxs-lookup"><span data-stu-id="eb03c-197">Parameters - allowCrossCompany</span></span>

<span data-ttu-id="eb03c-198">値</span><span class="sxs-lookup"><span data-stu-id="eb03c-198">value</span></span>  

### <a name="return-value---allowcrosscompany"></a><span data-ttu-id="eb03c-199">戻り値 - allowCrossCompany</span><span class="sxs-lookup"><span data-stu-id="eb03c-199">Return Value - allowCrossCompany</span></span>

## <a name="method-canpage"></a><span data-ttu-id="eb03c-200">メソッド canPage</span><span class="sxs-lookup"><span data-stu-id="eb03c-200">Method canPage</span></span>

```xpp
public boolean canPage([boolean skipOrderByCheck], [boolean throwIfNotPagable], [boolean isValuePaging])
```

### <a name="parameters---canpage"></a><span data-ttu-id="eb03c-201">パラメーター - canPage</span><span class="sxs-lookup"><span data-stu-id="eb03c-201">Parameters - canPage</span></span>

<span data-ttu-id="eb03c-202">skipOrderByCheck</span><span class="sxs-lookup"><span data-stu-id="eb03c-202">skipOrderByCheck</span></span>  

<!-- -->

<span data-ttu-id="eb03c-203">throwIfNotPagable</span><span class="sxs-lookup"><span data-stu-id="eb03c-203">throwIfNotPagable</span></span>  

<!-- -->

<span data-ttu-id="eb03c-204">isValuePaging</span><span class="sxs-lookup"><span data-stu-id="eb03c-204">isValuePaging</span></span>  

### <a name="return-value---canpage"></a><span data-ttu-id="eb03c-205">戻り値 - canPage</span><span class="sxs-lookup"><span data-stu-id="eb03c-205">Return Value - canPage</span></span>

## <a name="method-changed"></a><span data-ttu-id="eb03c-206">メソッド changed</span><span class="sxs-lookup"><span data-stu-id="eb03c-206">Method changed</span></span>

<span data-ttu-id="eb03c-207">QueryRun.next メソッドの最後の呼び出し以降に、指定されたデータ ソースが新しい値をフェッチしたかどうかを判断します。</span><span class="sxs-lookup"><span data-stu-id="eb03c-207">Determines whether the specified data source has fetched a new value since the last call to the QueryRun.next method.</span></span>

```xpp
public boolean changed(TableId table, [int occurrence])
```

### <a name="parameters---changed"></a><span data-ttu-id="eb03c-208">パラメーター - changed</span><span class="sxs-lookup"><span data-stu-id="eb03c-208">Parameters - changed</span></span>

<span data-ttu-id="eb03c-209">テーブル</span><span class="sxs-lookup"><span data-stu-id="eb03c-209">table</span></span>  
<span data-ttu-id="eb03c-210">確認するデータソース (オプション)。</span><span class="sxs-lookup"><span data-stu-id="eb03c-210">The data source to check; optional.</span></span> <span data-ttu-id="eb03c-211">1 つ以上のデータ ソースが指定されたテーブルに割り当てられている場合、この引数が確認するデータ ソースを決定するために使用できます。</span><span class="sxs-lookup"><span data-stu-id="eb03c-211">If more than one data source is assigned to a given table, this argument can be used to determine which data source to check.</span></span>

<!-- -->

<span data-ttu-id="eb03c-212">occurrence</span><span class="sxs-lookup"><span data-stu-id="eb03c-212">occurrence</span></span>  
<span data-ttu-id="eb03c-213">確認するデータソース (オプション)。</span><span class="sxs-lookup"><span data-stu-id="eb03c-213">The data source to check; optional.</span></span> <span data-ttu-id="eb03c-214">1 つ以上のデータ ソースが指定されたテーブルに割り当てられている場合、この引数が確認するデータ ソースを決定するために使用できます。</span><span class="sxs-lookup"><span data-stu-id="eb03c-214">If more than one data source is assigned to a given table, this argument can be used to determine which data source to check.</span></span>

### <a name="return-value---changed"></a><span data-ttu-id="eb03c-215">戻り値 - changed</span><span class="sxs-lookup"><span data-stu-id="eb03c-215">Return Value - changed</span></span>

<span data-ttu-id="eb03c-216">QueryRun.next に対する最後の呼び出し後に指定データ ソースが変更された場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="eb03c-216">true if the specified data source has changed since the last call to QueryRun.next; otherwise, false.</span></span>

### <a name="remarks---changed"></a><span data-ttu-id="eb03c-217">備考 - changed</span><span class="sxs-lookup"><span data-stu-id="eb03c-217">Remarks - changed</span></span>

<span data-ttu-id="eb03c-218">このメソッドは、データ ソースが階層構造になっている場合に便利です。</span><span class="sxs-lookup"><span data-stu-id="eb03c-218">This method is useful when data sources are hierarchically structured.</span></span> <span data-ttu-id="eb03c-219">埋め込みデータ ソースは、何回でも変更できます (顧客トランザクションなど)。</span><span class="sxs-lookup"><span data-stu-id="eb03c-219">A more embedded data source may change many times (such as the customer transactions).</span></span> <span data-ttu-id="eb03c-220">これは、埋め込まれていないデータソース (顧客テーブルなど) が新しいレコード (別の顧客) をフェッチするたびに発生します。</span><span class="sxs-lookup"><span data-stu-id="eb03c-220">This occurs every time that a less embedded data source (such as the customer table) fetches a new record (another customer).</span></span> <span data-ttu-id="eb03c-221">この関数の代わりに changedNo メソッドを使用できます。</span><span class="sxs-lookup"><span data-stu-id="eb03c-221">The changedNo method can be used instead of this function.</span></span>

## <a name="method-changedby"></a><span data-ttu-id="eb03c-222">メソッド changedBy</span><span class="sxs-lookup"><span data-stu-id="eb03c-222">Method changedBy</span></span>

<span data-ttu-id="eb03c-223">アプリケーション オブジェクトを最後に変更したユーザーの名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="eb03c-223">Gets or sets the name of the user who last changed the application object.</span></span>

```xpp
public str changedBy([str value])
```

### <a name="parameters---changedby"></a><span data-ttu-id="eb03c-224">パラメーター - changedBy</span><span class="sxs-lookup"><span data-stu-id="eb03c-224">Parameters - changedBy</span></span>

<span data-ttu-id="eb03c-225">値</span><span class="sxs-lookup"><span data-stu-id="eb03c-225">value</span></span>  

### <a name="return-value---changedby"></a><span data-ttu-id="eb03c-226">戻り値 - changedBy</span><span class="sxs-lookup"><span data-stu-id="eb03c-226">Return Value - changedBy</span></span>

<span data-ttu-id="eb03c-227">ユーザーの名前。</span><span class="sxs-lookup"><span data-stu-id="eb03c-227">The name of the user.</span></span>

## <a name="method-changeddate"></a><span data-ttu-id="eb03c-228">メソッド changedDate</span><span class="sxs-lookup"><span data-stu-id="eb03c-228">Method changedDate</span></span>

<span data-ttu-id="eb03c-229">アプリケーション オブジェクトが最後に変更された日付を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="eb03c-229">Gets or sets the date an application object was last changed.</span></span>

```xpp
public Date changedDate([Date value])
```

### <a name="parameters---changeddate"></a><span data-ttu-id="eb03c-230">パラメーター - changedDate</span><span class="sxs-lookup"><span data-stu-id="eb03c-230">Parameters - changedDate</span></span>

<span data-ttu-id="eb03c-231">値</span><span class="sxs-lookup"><span data-stu-id="eb03c-231">value</span></span>  

### <a name="return-value---changeddate"></a><span data-ttu-id="eb03c-232">戻り値 - changedDate</span><span class="sxs-lookup"><span data-stu-id="eb03c-232">Return Value - changedDate</span></span>

<span data-ttu-id="eb03c-233">アプリケーション オブジェクトが最後に変更された日付。</span><span class="sxs-lookup"><span data-stu-id="eb03c-233">The date an application object was last changed.</span></span>

## <a name="method-changedno"></a><span data-ttu-id="eb03c-234">メソッド changedNo</span><span class="sxs-lookup"><span data-stu-id="eb03c-234">Method changedNo</span></span>

```xpp
public boolean changedNo(int dataSourceNo)
```

### <a name="parameters---changedno"></a><span data-ttu-id="eb03c-235">パラメーター - changedNo</span><span class="sxs-lookup"><span data-stu-id="eb03c-235">Parameters - changedNo</span></span>

<span data-ttu-id="eb03c-236">dataSourceNo</span><span class="sxs-lookup"><span data-stu-id="eb03c-236">dataSourceNo</span></span>  

### <a name="return-value---changedno"></a><span data-ttu-id="eb03c-237">戻り値 - changedNo</span><span class="sxs-lookup"><span data-stu-id="eb03c-237">Return Value - changedNo</span></span>

## <a name="method-changedtime"></a><span data-ttu-id="eb03c-238">メソッド changedTime</span><span class="sxs-lookup"><span data-stu-id="eb03c-238">Method changedTime</span></span>

<span data-ttu-id="eb03c-239">アプリケーション オブジェクトが最後に変更された時刻を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="eb03c-239">Gets or sets the time an application object was last changed.</span></span>

```xpp
public str changedTime([str value])
```

### <a name="parameters---changedtime"></a><span data-ttu-id="eb03c-240">パラメーター - changedTime</span><span class="sxs-lookup"><span data-stu-id="eb03c-240">Parameters - changedTime</span></span>

<span data-ttu-id="eb03c-241">値</span><span class="sxs-lookup"><span data-stu-id="eb03c-241">value</span></span>  

### <a name="return-value---changedtime"></a><span data-ttu-id="eb03c-242">戻り値 - changedTime</span><span class="sxs-lookup"><span data-stu-id="eb03c-242">Return Value - changedTime</span></span>

<span data-ttu-id="eb03c-243">アプリケーション オブジェクトが最後に変更された時間。</span><span class="sxs-lookup"><span data-stu-id="eb03c-243">The time an application object was last changed.</span></span>

## <a name="method-createdby"></a><span data-ttu-id="eb03c-244">メソッド createdBy</span><span class="sxs-lookup"><span data-stu-id="eb03c-244">Method createdBy</span></span>

<span data-ttu-id="eb03c-245">アプリケーション オブジェクトを作成したユーザーの名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="eb03c-245">Gets or sets the name of the user who created the application object.</span></span>

```xpp
public str createdBy([str value])
```

### <a name="parameters---createdby"></a><span data-ttu-id="eb03c-246">パラメーター - createdBy</span><span class="sxs-lookup"><span data-stu-id="eb03c-246">Parameters - createdBy</span></span>

<span data-ttu-id="eb03c-247">値</span><span class="sxs-lookup"><span data-stu-id="eb03c-247">value</span></span>  

### <a name="return-value---createdby"></a><span data-ttu-id="eb03c-248">戻り値 - createdBy</span><span class="sxs-lookup"><span data-stu-id="eb03c-248">Return Value - createdBy</span></span>

<span data-ttu-id="eb03c-249">ユーザーの名前。</span><span class="sxs-lookup"><span data-stu-id="eb03c-249">The name of the user.</span></span>

## <a name="method-creationdate"></a><span data-ttu-id="eb03c-250">メソッド creationDate</span><span class="sxs-lookup"><span data-stu-id="eb03c-250">Method creationDate</span></span>

<span data-ttu-id="eb03c-251">アプリケーション オブジェクトが作成された日付を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="eb03c-251">Gets or sets the date an application object was created.</span></span>

```xpp
public Date creationDate([Date value])
```

### <a name="parameters---creationdate"></a><span data-ttu-id="eb03c-252">パラメーター - creationDate</span><span class="sxs-lookup"><span data-stu-id="eb03c-252">Parameters - creationDate</span></span>

<span data-ttu-id="eb03c-253">値</span><span class="sxs-lookup"><span data-stu-id="eb03c-253">value</span></span>  

### <a name="return-value---creationdate"></a><span data-ttu-id="eb03c-254">戻り値 - creationDate</span><span class="sxs-lookup"><span data-stu-id="eb03c-254">Return Value - creationDate</span></span>

<span data-ttu-id="eb03c-255">アプリケーション オブジェクトが作成された日付。</span><span class="sxs-lookup"><span data-stu-id="eb03c-255">The date an application object was created.</span></span>

## <a name="method-creationtime"></a><span data-ttu-id="eb03c-256">メソッド creationTime</span><span class="sxs-lookup"><span data-stu-id="eb03c-256">Method creationTime</span></span>

```xpp
public str creationTime([str value])
```

### <a name="parameters---creationtime"></a><span data-ttu-id="eb03c-257">パラメーター - creationTime</span><span class="sxs-lookup"><span data-stu-id="eb03c-257">Parameters - creationTime</span></span>

<span data-ttu-id="eb03c-258">値</span><span class="sxs-lookup"><span data-stu-id="eb03c-258">value</span></span>  

### <a name="return-value---creationtime"></a><span data-ttu-id="eb03c-259">戻り値 - creationTime</span><span class="sxs-lookup"><span data-stu-id="eb03c-259">Return Value - creationTime</span></span>

## <a name="method-description"></a><span data-ttu-id="eb03c-260">メソッドの説明</span><span class="sxs-lookup"><span data-stu-id="eb03c-260">Method description</span></span>

```xpp
public str description([str value])
```

### <a name="parameters---description"></a><span data-ttu-id="eb03c-261">パラメーター - description</span><span class="sxs-lookup"><span data-stu-id="eb03c-261">Parameters - description</span></span>

<span data-ttu-id="eb03c-262">値</span><span class="sxs-lookup"><span data-stu-id="eb03c-262">value</span></span>  

### <a name="return-value---description"></a><span data-ttu-id="eb03c-263">戻り値 - description</span><span class="sxs-lookup"><span data-stu-id="eb03c-263">Return Value - description</span></span>

## <a name="method-equal"></a><span data-ttu-id="eb03c-264">メソッド equal</span><span class="sxs-lookup"><span data-stu-id="eb03c-264">Method equal</span></span>

<span data-ttu-id="eb03c-265">指定されたオブジェクトが現在のオブジェクトと等しいかどうかを判定します。</span><span class="sxs-lookup"><span data-stu-id="eb03c-265">Determines whether the specified object is equal to the current object.</span></span>

```xpp
public boolean equal(Object obj)
```

### <a name="parameters---equal"></a><span data-ttu-id="eb03c-266">パラメーター - equal</span><span class="sxs-lookup"><span data-stu-id="eb03c-266">Parameters - equal</span></span>

<span data-ttu-id="eb03c-267">obj</span><span class="sxs-lookup"><span data-stu-id="eb03c-267">obj</span></span>  

### <a name="return-value---equal"></a><span data-ttu-id="eb03c-268">戻り値 - equal</span><span class="sxs-lookup"><span data-stu-id="eb03c-268">Return Value - equal</span></span>

<span data-ttu-id="eb03c-269">指定したオブジェクトが現在のオブジェクトと等しい場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="eb03c-269">true if the specified object is equal to the current object; otherwise, false.</span></span>

### <a name="remarks---equal"></a><span data-ttu-id="eb03c-270">備考 - equal</span><span class="sxs-lookup"><span data-stu-id="eb03c-270">Remarks - equal</span></span>

<span data-ttu-id="eb03c-271">Object::equal メソッドの既定の実装では、照会の等価性のみをサポートします。</span><span class="sxs-lookup"><span data-stu-id="eb03c-271">The default implementation of the Object::equal method supports only reference equality.</span></span> <span data-ttu-id="eb03c-272">ただし、派生クラスは、値の等価性をサポートするために Object::equal メソッドをオーバーライドできます。</span><span class="sxs-lookup"><span data-stu-id="eb03c-272">However, derived classes can override the Object::equal method to support value equality.</span></span>

## <a name="method-form"></a><span data-ttu-id="eb03c-273">メソッド form</span><span class="sxs-lookup"><span data-stu-id="eb03c-273">Method form</span></span>

```xpp
public str form([str value])
```

### <a name="parameters---form"></a><span data-ttu-id="eb03c-274">パラメーター - form</span><span class="sxs-lookup"><span data-stu-id="eb03c-274">Parameters - form</span></span>

<span data-ttu-id="eb03c-275">値</span><span class="sxs-lookup"><span data-stu-id="eb03c-275">value</span></span>  

### <a name="return-value---form"></a><span data-ttu-id="eb03c-276">戻り値 - form</span><span class="sxs-lookup"><span data-stu-id="eb03c-276">Return Value - form</span></span>

## <a name="method-get"></a><span data-ttu-id="eb03c-277">メソッド get</span><span class="sxs-lookup"><span data-stu-id="eb03c-277">Method get</span></span>

<span data-ttu-id="eb03c-278">次のメソッドの前の呼び出しによってフェッチされたレコードを取得します。</span><span class="sxs-lookup"><span data-stu-id="eb03c-278">Retrieves the record fetched by the previous call to next method.</span></span>

```xpp
public Common get(TableId table, [int occurrence])
```

### <a name="parameters---get"></a><span data-ttu-id="eb03c-279">パラメーター - get</span><span class="sxs-lookup"><span data-stu-id="eb03c-279">Parameters - get</span></span>

<span data-ttu-id="eb03c-280">テーブル</span><span class="sxs-lookup"><span data-stu-id="eb03c-280">table</span></span>  
<span data-ttu-id="eb03c-281">アドレス指定されるデータソース (オプション)。</span><span class="sxs-lookup"><span data-stu-id="eb03c-281">The data source to be addressed; optional.</span></span> <span data-ttu-id="eb03c-282">指定されたテーブルを持つデータ ソースの番号。1 ベース。</span><span class="sxs-lookup"><span data-stu-id="eb03c-282">The number of the data source with the given table; 1-based.</span></span> <span data-ttu-id="eb03c-283">同じテーブルに割り当てられたデータ ソースが 1 つ以上ある場合は、この (オプションの) パラメーターを使用して、どのパラメーターを指定するかを指定できます。</span><span class="sxs-lookup"><span data-stu-id="eb03c-283">If more than one data source has the same table assigned to it, this (optional) parameter can be used to specify which one is to be addressed.</span></span> <span data-ttu-id="eb03c-284">指定されたテーブルを持つデータ ソースの数を指定します。</span><span class="sxs-lookup"><span data-stu-id="eb03c-284">It specifies the number of the data source with the given table.</span></span> <span data-ttu-id="eb03c-285">したがって、CustTable テーブルが 2 つのデータ ソースに割り当てられ、2 番目のデータ ソースが必要な場合、この引数は 2 の値である必要があります。</span><span class="sxs-lookup"><span data-stu-id="eb03c-285">Thus, if the CustTable table is assigned to two data sources, and the second data source is required, this argument should have the value 2.</span></span>

<!-- -->

<span data-ttu-id="eb03c-286">occurrence</span><span class="sxs-lookup"><span data-stu-id="eb03c-286">occurrence</span></span>  
<span data-ttu-id="eb03c-287">アドレス指定されるデータソース (オプション)。</span><span class="sxs-lookup"><span data-stu-id="eb03c-287">The data source to be addressed; optional.</span></span> <span data-ttu-id="eb03c-288">指定されたテーブルを持つデータ ソースの番号。1 ベース。</span><span class="sxs-lookup"><span data-stu-id="eb03c-288">The number of the data source with the given table; 1-based.</span></span> <span data-ttu-id="eb03c-289">同じテーブルに割り当てられたデータ ソースが 1 つ以上ある場合は、この (オプションの) パラメーターを使用して、どのパラメーターを指定するかを指定できます。</span><span class="sxs-lookup"><span data-stu-id="eb03c-289">If more than one data source has the same table assigned to it, this (optional) parameter can be used to specify which one is to be addressed.</span></span> <span data-ttu-id="eb03c-290">指定されたテーブルを持つデータ ソースの数を指定します。</span><span class="sxs-lookup"><span data-stu-id="eb03c-290">It specifies the number of the data source with the given table.</span></span> <span data-ttu-id="eb03c-291">したがって、CustTable テーブルが 2 つのデータ ソースに割り当てられ、2 番目のデータ ソースが必要な場合、この引数は 2 の値である必要があります。</span><span class="sxs-lookup"><span data-stu-id="eb03c-291">Thus, if the CustTable table is assigned to two data sources, and the second data source is required, this argument should have the value 2.</span></span>

### <a name="return-value---get"></a><span data-ttu-id="eb03c-292">戻り値 - get</span><span class="sxs-lookup"><span data-stu-id="eb03c-292">Return Value - get</span></span>

<span data-ttu-id="eb03c-293">引数で識別されるデータ ソースからフェッチされたレコードを返します。</span><span class="sxs-lookup"><span data-stu-id="eb03c-293">Returns the record fetched from the data source identified by the arguments.</span></span>

### <a name="remarks---get"></a><span data-ttu-id="eb03c-294">備考 - get</span><span class="sxs-lookup"><span data-stu-id="eb03c-294">Remarks - get</span></span>

<span data-ttu-id="eb03c-295">レコードを取得するデータ ソースは、データ ソースに割り当てられたテーブルとオプションのパラメーターによって指定されます。</span><span class="sxs-lookup"><span data-stu-id="eb03c-295">The data source from which to retrieve the record is specified by the table assigned to the data source and by an optional parameter.</span></span> <span data-ttu-id="eb03c-296">テーブル (およびオプションのパラメーター) を指定するのではなく、getNo メソッドを使用して、データ ソースの数を引数として取得できます。</span><span class="sxs-lookup"><span data-stu-id="eb03c-296">Instead of supplying the table (and optional parameter), you can use the getNo method, which takes the data source number as an argument.</span></span>

## <a name="method-getimpexpdatacontracttype"></a><span data-ttu-id="eb03c-297">メソッド getImpExpDataContractType</span><span class="sxs-lookup"><span data-stu-id="eb03c-297">Method getImpExpDataContractType</span></span>

```xpp
public System.Type getImpExpDataContractType()
```

### <a name="return-value---getimpexpdatacontracttype"></a><span data-ttu-id="eb03c-298">戻り値 - getImpExpDataContractType</span><span class="sxs-lookup"><span data-stu-id="eb03c-298">Return Value - getImpExpDataContractType</span></span>

## <a name="method-getno"></a><span data-ttu-id="eb03c-299">メソッド getNo</span><span class="sxs-lookup"><span data-stu-id="eb03c-299">Method getNo</span></span>

<span data-ttu-id="eb03c-300">QueryRun.next メソッドの前の呼び出しによってフェッチされたレコードを取得します。</span><span class="sxs-lookup"><span data-stu-id="eb03c-300">Retrieves the record fetched by the previous call to QueryRun.next Method.</span></span>

```xpp
public Common getNo(int dataSourceNo)
```

### <a name="parameters---getno"></a><span data-ttu-id="eb03c-301">パラメーター - getNo</span><span class="sxs-lookup"><span data-stu-id="eb03c-301">Parameters - getNo</span></span>

<span data-ttu-id="eb03c-302">dataSourceNo</span><span class="sxs-lookup"><span data-stu-id="eb03c-302">dataSourceNo</span></span>  
<span data-ttu-id="eb03c-303">現在選択されているレコードを取得する元のデータ ソースの番号。</span><span class="sxs-lookup"><span data-stu-id="eb03c-303">The number of the data source from which to get the currently selected record.</span></span>

### <a name="return-value---getno"></a><span data-ttu-id="eb03c-304">戻り値 - getNo</span><span class="sxs-lookup"><span data-stu-id="eb03c-304">Return Value - getNo</span></span>

<span data-ttu-id="eb03c-305">引数で識別されるデータ ソースのフェッチされたレコードを返します。</span><span class="sxs-lookup"><span data-stu-id="eb03c-305">Returns the record fetched for the data source identified by the argument.</span></span>

### <a name="remarks---getno"></a><span data-ttu-id="eb03c-306">備考 - getNo</span><span class="sxs-lookup"><span data-stu-id="eb03c-306">Remarks - getNo</span></span>

<span data-ttu-id="eb03c-307">レコードを取り出すデータ ソースは、データ ソースの番号で指定します。</span><span class="sxs-lookup"><span data-stu-id="eb03c-307">The data source from which to retrieve the record is specified by the number of the data source.</span></span> <span data-ttu-id="eb03c-308">データソースは、1 から順にカウントされます。</span><span class="sxs-lookup"><span data-stu-id="eb03c-308">The data sources are counted consecutively, starting from 1.</span></span> <span data-ttu-id="eb03c-309">代わりに QueryRun.get メソッドを使用できます。このメソッドは、データ ソースを定義するテーブル (およびオプション パラメーター) を使用して指定されます。</span><span class="sxs-lookup"><span data-stu-id="eb03c-309">The QueryRun.get Method method can be used instead; that method is supplied with the table (and an optional parameter), that defines the data source.</span></span>

### <a name="examples---getno"></a><span data-ttu-id="eb03c-310">例 - getNo</span><span class="sxs-lookup"><span data-stu-id="eb03c-310">Examples - getNo</span></span>

```xpp
{ 
    QueryRun qr; 
    // Consider a query with CustTable/CustTrans datasources. 
    // Traverse all records found in CustTable/CustTrans: 
    while (qr.next()) 
    { 
        if (qr.Changed(TableNum(CustTable)))
        { 
            // A new CustTable record 
            CustTableRecord = qr.GetNo(1); 
        } 
        if (qr.Changed(TableNum(CustTrans))) 
        { 
            // A new CustTrans record 
            CustTransRecord = qr.GetNo(1); 
        } 
    } 
}
```

## <a name="method-importable"></a><span data-ttu-id="eb03c-311">メソッド importable</span><span class="sxs-lookup"><span data-stu-id="eb03c-311">Method importable</span></span>

```xpp
public boolean importable()
```

### <a name="return-value---importable"></a><span data-ttu-id="eb03c-312">戻り値 - importable</span><span class="sxs-lookup"><span data-stu-id="eb03c-312">Return Value - importable</span></span>

## <a name="method-interactive"></a><span data-ttu-id="eb03c-313">メソッド interactive</span><span class="sxs-lookup"><span data-stu-id="eb03c-313">Method interactive</span></span>

```xpp
public boolean interactive([boolean value])
```

### <a name="parameters---interactive"></a><span data-ttu-id="eb03c-314">パラメーター - interactive</span><span class="sxs-lookup"><span data-stu-id="eb03c-314">Parameters - interactive</span></span>

<span data-ttu-id="eb03c-315">値</span><span class="sxs-lookup"><span data-stu-id="eb03c-315">value</span></span>  

### <a name="return-value---interactive"></a><span data-ttu-id="eb03c-316">戻り値 - interactive</span><span class="sxs-lookup"><span data-stu-id="eb03c-316">Return Value - interactive</span></span>

## <a name="method-ispositionpagingenabled"></a><span data-ttu-id="eb03c-317">メソッド isPositionPagingEnabled</span><span class="sxs-lookup"><span data-stu-id="eb03c-317">Method isPositionPagingEnabled</span></span>

```xpp
public boolean isPositionPagingEnabled()
```

### <a name="return-value---ispositionpagingenabled"></a><span data-ttu-id="eb03c-318">戻り値 - isPositionPagingEnabled</span><span class="sxs-lookup"><span data-stu-id="eb03c-318">Return Value - isPositionPagingEnabled</span></span>

## <a name="method-isquerytimedout"></a><span data-ttu-id="eb03c-319">メソッド isQueryTimedout</span><span class="sxs-lookup"><span data-stu-id="eb03c-319">Method isQueryTimedout</span></span>

```xpp
public boolean isQueryTimedout()
```

### <a name="return-value---isquerytimedout"></a><span data-ttu-id="eb03c-320">戻り値 - isQueryTimedout</span><span class="sxs-lookup"><span data-stu-id="eb03c-320">Return Value - isQueryTimedout</span></span>

## <a name="method-isvaluebasedpagingenabled"></a><span data-ttu-id="eb03c-321">メソッド isValueBasedPagingEnabled</span><span class="sxs-lookup"><span data-stu-id="eb03c-321">Method isValueBasedPagingEnabled</span></span>

```xpp
public boolean isValueBasedPagingEnabled()
```

### <a name="return-value---isvaluebasedpagingenabled"></a><span data-ttu-id="eb03c-322">戻り値 - isValueBasedPagingEnabled</span><span class="sxs-lookup"><span data-stu-id="eb03c-322">Return Value - isValueBasedPagingEnabled</span></span>

## <a name="method-literals"></a><span data-ttu-id="eb03c-323">メソッド literals</span><span class="sxs-lookup"><span data-stu-id="eb03c-323">Method literals</span></span>

```xpp
public int literals([int value])
```

### <a name="parameters---literals"></a><span data-ttu-id="eb03c-324">パラメーター - literals</span><span class="sxs-lookup"><span data-stu-id="eb03c-324">Parameters - literals</span></span>

<span data-ttu-id="eb03c-325">値</span><span class="sxs-lookup"><span data-stu-id="eb03c-325">value</span></span>  

### <a name="return-value---literals"></a><span data-ttu-id="eb03c-326">戻り値 - literals</span><span class="sxs-lookup"><span data-stu-id="eb03c-326">Return Value - literals</span></span>

## <a name="method-loadcsv"></a><span data-ttu-id="eb03c-327">メソッド loadCsv</span><span class="sxs-lookup"><span data-stu-id="eb03c-327">Method loadCsv</span></span>

```xpp
public Guid loadCsv(str fileName)
```

### <a name="parameters---loadcsv"></a><span data-ttu-id="eb03c-328">パラメーター - loadCsv</span><span class="sxs-lookup"><span data-stu-id="eb03c-328">Parameters - loadCsv</span></span>

<span data-ttu-id="eb03c-329">fileName</span><span class="sxs-lookup"><span data-stu-id="eb03c-329">fileName</span></span>  

### <a name="return-value---loadcsv"></a><span data-ttu-id="eb03c-330">戻り値 - loadCsv</span><span class="sxs-lookup"><span data-stu-id="eb03c-330">Return Value - loadCsv</span></span>

## <a name="method-loadxml"></a><span data-ttu-id="eb03c-331">メソッド loadXml</span><span class="sxs-lookup"><span data-stu-id="eb03c-331">Method loadXml</span></span>

```xpp
public Guid loadXml(str fileName)
```

### <a name="parameters---loadxml"></a><span data-ttu-id="eb03c-332">パラメーター - loadXml</span><span class="sxs-lookup"><span data-stu-id="eb03c-332">Parameters - loadXml</span></span>

<span data-ttu-id="eb03c-333">fileName</span><span class="sxs-lookup"><span data-stu-id="eb03c-333">fileName</span></span>  

### <a name="return-value---loadxml"></a><span data-ttu-id="eb03c-334">戻り値 - loadXml</span><span class="sxs-lookup"><span data-stu-id="eb03c-334">Return Value - loadXml</span></span>

## <a name="method-name"></a><span data-ttu-id="eb03c-335">メソッド名</span><span class="sxs-lookup"><span data-stu-id="eb03c-335">Method name</span></span>

<span data-ttu-id="eb03c-336">フォーム、レポート、テーブル、クエリ、または他のアプリケーション オブジェクトを識別するためのコードで使用される名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="eb03c-336">Gets or sets the name that is used in code to identify a form, report, table, query, or other application object.</span></span>

```xpp
public str name([str value])
```

### <a name="parameters---name"></a><span data-ttu-id="eb03c-337">パラメーター - name</span><span class="sxs-lookup"><span data-stu-id="eb03c-337">Parameters - name</span></span>

<span data-ttu-id="eb03c-338">値</span><span class="sxs-lookup"><span data-stu-id="eb03c-338">value</span></span>  

### <a name="return-value---name"></a><span data-ttu-id="eb03c-339">戻り値 - name</span><span class="sxs-lookup"><span data-stu-id="eb03c-339">Return Value - name</span></span>

<span data-ttu-id="eb03c-340">アプリケーション オブジェクトを識別するためにコードで使用される名前。</span><span class="sxs-lookup"><span data-stu-id="eb03c-340">The name that is used in code to identify an application object.</span></span>

### <a name="remarks---name"></a><span data-ttu-id="eb03c-341">備考 - name</span><span class="sxs-lookup"><span data-stu-id="eb03c-341">Remarks - name</span></span>

<span data-ttu-id="eb03c-342">オブジェクトの名前プロパティ値は、コードの競合を避けるために、次の基準を満たしている必要があります。</span><span class="sxs-lookup"><span data-stu-id="eb03c-342">The name property value of an object must meet the following criteria to avoid code conflicts:</span></span>

-   <span data-ttu-id="eb03c-343">文字で始めます。</span><span class="sxs-lookup"><span data-stu-id="eb03c-343">Begins with a letter.</span></span>
-   <span data-ttu-id="eb03c-344">250 文字を超えないでください。</span><span class="sxs-lookup"><span data-stu-id="eb03c-344">Doesn't exceed 250 characters.</span></span>
-   <span data-ttu-id="eb03c-345">数字とアンダースコア文字を含めることができます。</span><span class="sxs-lookup"><span data-stu-id="eb03c-345">Can include numbers and underscore characters.</span></span>
-   <span data-ttu-id="eb03c-346">句読点やスペースを含めることはできません。</span><span class="sxs-lookup"><span data-stu-id="eb03c-346">Cannot include punctuation or spaces.</span></span>
-   <span data-ttu-id="eb03c-347">テーブルは、拡張データ型、基本列挙型、クラスなどの他のパブリック オブジェクトと同じ名前を持つことはできません。</span><span class="sxs-lookup"><span data-stu-id="eb03c-347">Tables cannot have the same name as other public objects, such as extended data types, base enumerations, or classes.</span></span>

## <a name="method-newobject"></a><span data-ttu-id="eb03c-348">メソッド newObject</span><span class="sxs-lookup"><span data-stu-id="eb03c-348">Method newObject</span></span>

```xpp
public QueryRun newObject(AnyType source)
```

### <a name="parameters---newobject"></a><span data-ttu-id="eb03c-349">パラメーター - newObject</span><span class="sxs-lookup"><span data-stu-id="eb03c-349">Parameters - newObject</span></span>

<span data-ttu-id="eb03c-350">ソース</span><span class="sxs-lookup"><span data-stu-id="eb03c-350">source</span></span>  

### <a name="return-value---newobject"></a><span data-ttu-id="eb03c-351">戻り値 - newObject</span><span class="sxs-lookup"><span data-stu-id="eb03c-351">Return Value - newObject</span></span>

## <a name="method-next"></a><span data-ttu-id="eb03c-352">メソッド next</span><span class="sxs-lookup"><span data-stu-id="eb03c-352">Method next</span></span>

<span data-ttu-id="eb03c-353">クエリから次のレコードを取得します。</span><span class="sxs-lookup"><span data-stu-id="eb03c-353">Retrieves the next record from the query.</span></span>

```xpp
public boolean next()
```

### <a name="return-value---next"></a><span data-ttu-id="eb03c-354">戻り値 - next</span><span class="sxs-lookup"><span data-stu-id="eb03c-354">Return Value - next</span></span>

<span data-ttu-id="eb03c-355">次のレコードが利用可能で getNo メソッドまたは get メソッドで取得することができる場合は true。クエリ内に設定された制約を満たすレコードがそれ以上存在しない場合は false。</span><span class="sxs-lookup"><span data-stu-id="eb03c-355">true if the next record is available and can be fetched with the getNo method or get method; false if no there are no more records that satisfy the constraint set up in the query.</span></span>

### <a name="remarks---next"></a><span data-ttu-id="eb03c-356">備考 - next</span><span class="sxs-lookup"><span data-stu-id="eb03c-356">Remarks - next</span></span>

<span data-ttu-id="eb03c-357">変更されたメソッドまたは changedNo メソッドを使用して、指定されたデータ ソースのレコードが前回の次のメソッド呼び出しから変更されたかどうかを確認できます。</span><span class="sxs-lookup"><span data-stu-id="eb03c-357">The changed method or changedNo method can be used to check whether the record from the given data source has changed since the previous call to the next method.</span></span>

### <a name="examples---next"></a><span data-ttu-id="eb03c-358">例 - next</span><span class="sxs-lookup"><span data-stu-id="eb03c-358">Examples - next</span></span>

```xpp
{ 
    queryRun qr; 
    CustTable ct; 
    // ... 
    if (qr.prompt()) 
    { 
        while (qr.next()) 
        { 
            if (qr.Changed(tableNum(CustTable))) 
            { 
                ct = qr.Get (tableNum(CustTable)); 
                print ct.AccountNum; 
            } 
        } 
    } 
}
```

## <a name="method-nextuniqueid"></a><span data-ttu-id="eb03c-359">メソッド nextUniqueId</span><span class="sxs-lookup"><span data-stu-id="eb03c-359">Method nextUniqueId</span></span>

```xpp
public int nextUniqueId([int value])
```

### <a name="parameters---nextuniqueid"></a><span data-ttu-id="eb03c-360">パラメーター - nextUniqueId</span><span class="sxs-lookup"><span data-stu-id="eb03c-360">Parameters - nextUniqueId</span></span>

<span data-ttu-id="eb03c-361">値</span><span class="sxs-lookup"><span data-stu-id="eb03c-361">value</span></span>  

### <a name="return-value---nextuniqueid"></a><span data-ttu-id="eb03c-362">戻り値 - nextUniqueId</span><span class="sxs-lookup"><span data-stu-id="eb03c-362">Return Value - nextUniqueId</span></span>

## <a name="method-origin"></a><span data-ttu-id="eb03c-363">メソッド origin</span><span class="sxs-lookup"><span data-stu-id="eb03c-363">Method origin</span></span>

```xpp
public Guid origin([Guid value])
```

### <a name="parameters---origin"></a><span data-ttu-id="eb03c-364">パラメーター - origin</span><span class="sxs-lookup"><span data-stu-id="eb03c-364">Parameters - origin</span></span>

<span data-ttu-id="eb03c-365">値</span><span class="sxs-lookup"><span data-stu-id="eb03c-365">value</span></span>  

### <a name="return-value---origin"></a><span data-ttu-id="eb03c-366">戻り値 - origin</span><span class="sxs-lookup"><span data-stu-id="eb03c-366">Return Value - origin</span></span>

## <a name="method-pack"></a><span data-ttu-id="eb03c-367">メソッド pack</span><span class="sxs-lookup"><span data-stu-id="eb03c-367">Method pack</span></span>

```xpp
public container pack([boolean doCheck])
```

### <a name="parameters---pack"></a><span data-ttu-id="eb03c-368">パラメーター - pack</span><span class="sxs-lookup"><span data-stu-id="eb03c-368">Parameters - pack</span></span>

<span data-ttu-id="eb03c-369">doCheck</span><span class="sxs-lookup"><span data-stu-id="eb03c-369">doCheck</span></span>  

### <a name="return-value---pack"></a><span data-ttu-id="eb03c-370">戻り値 - pack</span><span class="sxs-lookup"><span data-stu-id="eb03c-370">Return Value - pack</span></span>

## <a name="method-prompt"></a><span data-ttu-id="eb03c-371">メソッド prompt</span><span class="sxs-lookup"><span data-stu-id="eb03c-371">Method prompt</span></span>

<span data-ttu-id="eb03c-372">クエリによってフェッチするレコードを定義するためのオプションをユーザーに表示します。</span><span class="sxs-lookup"><span data-stu-id="eb03c-372">Presents, to the user, the options for defining the records to be fetched by the query.</span></span>

```xpp
public boolean prompt()
```

### <a name="return-value---prompt"></a><span data-ttu-id="eb03c-373">戻り値 - prompt</span><span class="sxs-lookup"><span data-stu-id="eb03c-373">Return Value - prompt</span></span>

<span data-ttu-id="eb03c-374">ユーザーが OK をクリックして検索が続行される場合は true。ユーザーがキャンセルをクリックして検索を停止した場合は false。</span><span class="sxs-lookup"><span data-stu-id="eb03c-374">true if the user clicked OK and the search is to continue; false if the user clicked Cancel to stop the search.</span></span>

### <a name="remarks---prompt"></a><span data-ttu-id="eb03c-375">備考 - prompt</span><span class="sxs-lookup"><span data-stu-id="eb03c-375">Remarks - prompt</span></span>

<span data-ttu-id="eb03c-376">ユーザーには、フェッチされたレコードによって実行される制約を定義する範囲を与えるためのフォームが提示される。</span><span class="sxs-lookup"><span data-stu-id="eb03c-376">The user is presented with a form to give ranges that define constraints to be fulfilled by the fetched records.</span></span> <span data-ttu-id="eb03c-377">または、ユーザーは新しいフィールドを追加し、区切ったり、変更したり、並べ替えたりすることができます。</span><span class="sxs-lookup"><span data-stu-id="eb03c-377">Or the user may add new fields to delimit, change the sorting, and so on.</span></span> <span data-ttu-id="eb03c-378">このメソッドをオーバーロードすると、事前定義されたクエリ フォームではなく、アプリケーション定義の方法でユーザーにプロンプトを表示できます。</span><span class="sxs-lookup"><span data-stu-id="eb03c-378">This method can be overloaded to prompt the user in an application-defined way instead of in through the predefined query form.</span></span> <span data-ttu-id="eb03c-379">または、この方法は、フェッチされるレコードをユーザーがコントロールできないように、オーバーロードされることがあります。</span><span class="sxs-lookup"><span data-stu-id="eb03c-379">Or this method can be overloaded to avoid giving the user control over which records are fetched.</span></span> <span data-ttu-id="eb03c-380">これらの結果を生成するには、継承したメソッドを呼び出さないでください。</span><span class="sxs-lookup"><span data-stu-id="eb03c-380">To produce these results, do not call the inherited method.</span></span> <span data-ttu-id="eb03c-381">いずれの場合でも、関数はクエリが続行する場合は true、それ以外の場合は false を返す必要があります。</span><span class="sxs-lookup"><span data-stu-id="eb03c-381">In any case, the function should return true if the query is to continue, and false otherwise.</span></span>

### <a name="examples---prompt"></a><span data-ttu-id="eb03c-382">例 - prompt</span><span class="sxs-lookup"><span data-stu-id="eb03c-382">Examples - prompt</span></span>

```xpp
{ 
    QueryRun qr; 
    // ... 
    if (qr.prompt()) 
    { 
        // The user pressed OK. Go ahead and do whatever is required. 
    } 
    else 
    { 
        // The user pressed Cancel. 
    } 
}
```

## <a name="method-query"></a><span data-ttu-id="eb03c-383">メソッド query</span><span class="sxs-lookup"><span data-stu-id="eb03c-383">Method query</span></span>

```xpp
public Query query([Query query])
```

### <a name="parameters---query"></a><span data-ttu-id="eb03c-384">パラメーター - query</span><span class="sxs-lookup"><span data-stu-id="eb03c-384">Parameters - query</span></span>

<span data-ttu-id="eb03c-385">クエリ</span><span class="sxs-lookup"><span data-stu-id="eb03c-385">query</span></span>  

### <a name="return-value---query"></a><span data-ttu-id="eb03c-386">戻り値 - query</span><span class="sxs-lookup"><span data-stu-id="eb03c-386">Return Value - query</span></span>

## <a name="method-querytype"></a><span data-ttu-id="eb03c-387">メソッド queryType</span><span class="sxs-lookup"><span data-stu-id="eb03c-387">Method queryType</span></span>

```xpp
public int queryType([int value])
```

### <a name="parameters---querytype"></a><span data-ttu-id="eb03c-388">パラメーター - queryType</span><span class="sxs-lookup"><span data-stu-id="eb03c-388">Parameters - queryType</span></span>

<span data-ttu-id="eb03c-389">値</span><span class="sxs-lookup"><span data-stu-id="eb03c-389">value</span></span>  

### <a name="return-value---querytype"></a><span data-ttu-id="eb03c-390">戻り値 - queryType</span><span class="sxs-lookup"><span data-stu-id="eb03c-390">Return Value - queryType</span></span>

## <a name="method-recordlevelsecurity"></a><span data-ttu-id="eb03c-391">メソッド recordLevelSecurity</span><span class="sxs-lookup"><span data-stu-id="eb03c-391">Method recordLevelSecurity</span></span>

```xpp
public boolean recordLevelSecurity([boolean value])
```

### <a name="parameters---recordlevelsecurity"></a><span data-ttu-id="eb03c-392">パラメーター - recordLevelSecurity</span><span class="sxs-lookup"><span data-stu-id="eb03c-392">Parameters - recordLevelSecurity</span></span>

<span data-ttu-id="eb03c-393">値</span><span class="sxs-lookup"><span data-stu-id="eb03c-393">value</span></span>  

### <a name="return-value---recordlevelsecurity"></a><span data-ttu-id="eb03c-394">戻り値 - recordLevelSecurity</span><span class="sxs-lookup"><span data-stu-id="eb03c-394">Return Value - recordLevelSecurity</span></span>

## <a name="method-report"></a><span data-ttu-id="eb03c-395">メソッド report</span><span class="sxs-lookup"><span data-stu-id="eb03c-395">Method report</span></span>

```xpp
public ReportRun report()
```

### <a name="return-value---report"></a><span data-ttu-id="eb03c-396">戻り値 - report</span><span class="sxs-lookup"><span data-stu-id="eb03c-396">Return Value - report</span></span>

## <a name="method-reportrun"></a><span data-ttu-id="eb03c-397">メソッド reportRun</span><span class="sxs-lookup"><span data-stu-id="eb03c-397">Method reportRun</span></span>

```xpp
public ReportRun reportRun()
```

### <a name="return-value---reportrun"></a><span data-ttu-id="eb03c-398">戻り値 - reportRun</span><span class="sxs-lookup"><span data-stu-id="eb03c-398">Return Value - reportRun</span></span>

## <a name="method-saved"></a><span data-ttu-id="eb03c-399">メソッド saved</span><span class="sxs-lookup"><span data-stu-id="eb03c-399">Method saved</span></span>

```xpp
public boolean saved()
```

### <a name="return-value---saved"></a><span data-ttu-id="eb03c-400">戻り値 - saved</span><span class="sxs-lookup"><span data-stu-id="eb03c-400">Return Value - saved</span></span>

## <a name="method-saveusersetup"></a><span data-ttu-id="eb03c-401">メソッド saveUserSetup</span><span class="sxs-lookup"><span data-stu-id="eb03c-401">Method saveUserSetup</span></span>

<span data-ttu-id="eb03c-402">ユーザー設定を保存します。</span><span class="sxs-lookup"><span data-stu-id="eb03c-402">Saves the user setup.</span></span>

```xpp
public boolean saveUserSetup([boolean saveIt])
```

### <a name="parameters---saveusersetup"></a><span data-ttu-id="eb03c-403">パラメーター - saveUserSetup</span><span class="sxs-lookup"><span data-stu-id="eb03c-403">Parameters - saveUserSetup</span></span>

<span data-ttu-id="eb03c-404">saveIt</span><span class="sxs-lookup"><span data-stu-id="eb03c-404">saveIt</span></span>  

### <a name="return-value---saveusersetup"></a><span data-ttu-id="eb03c-405">戻り値 - saveUserSetup</span><span class="sxs-lookup"><span data-stu-id="eb03c-405">Return Value - saveUserSetup</span></span>

<span data-ttu-id="eb03c-406">設定が正常に保存された場合は true。それ以外の場合は false。</span><span class="sxs-lookup"><span data-stu-id="eb03c-406">true if the setup was successfully saved; otherwise false.</span></span>

## <a name="method-searchable"></a><span data-ttu-id="eb03c-407">メソッド searchable</span><span class="sxs-lookup"><span data-stu-id="eb03c-407">Method searchable</span></span>

```xpp
public boolean searchable([boolean value])
```

### <a name="parameters---searchable"></a><span data-ttu-id="eb03c-408">パラメーター - searchable</span><span class="sxs-lookup"><span data-stu-id="eb03c-408">Parameters - searchable</span></span>

<span data-ttu-id="eb03c-409">値</span><span class="sxs-lookup"><span data-stu-id="eb03c-409">value</span></span>  

### <a name="return-value---searchable"></a><span data-ttu-id="eb03c-410">戻り値 - searchable</span><span class="sxs-lookup"><span data-stu-id="eb03c-410">Return Value - searchable</span></span>

## <a name="method-setcursor"></a><span data-ttu-id="eb03c-411">メソッド setCursor</span><span class="sxs-lookup"><span data-stu-id="eb03c-411">Method setCursor</span></span>

```xpp
public boolean setCursor(Common record, [int occurrence])
```

### <a name="parameters---setcursor"></a><span data-ttu-id="eb03c-412">パラメーター - setCursor</span><span class="sxs-lookup"><span data-stu-id="eb03c-412">Parameters - setCursor</span></span>

<span data-ttu-id="eb03c-413">記録</span><span class="sxs-lookup"><span data-stu-id="eb03c-413">record</span></span>  

<!-- -->

<span data-ttu-id="eb03c-414">occurrence</span><span class="sxs-lookup"><span data-stu-id="eb03c-414">occurrence</span></span>  

### <a name="return-value---setcursor"></a><span data-ttu-id="eb03c-415">戻り値 - setCursor</span><span class="sxs-lookup"><span data-stu-id="eb03c-415">Return Value - setCursor</span></span>

## <a name="method-setrecord"></a><span data-ttu-id="eb03c-416">メソッド setRecord</span><span class="sxs-lookup"><span data-stu-id="eb03c-416">Method setRecord</span></span>

```xpp
public boolean setRecord(Common record, [int occurrence])
```

### <a name="parameters---setrecord"></a><span data-ttu-id="eb03c-417">パラメーター - setRecord</span><span class="sxs-lookup"><span data-stu-id="eb03c-417">Parameters - setRecord</span></span>

<span data-ttu-id="eb03c-418">記録</span><span class="sxs-lookup"><span data-stu-id="eb03c-418">record</span></span>  

<!-- -->

<span data-ttu-id="eb03c-419">occurrence</span><span class="sxs-lookup"><span data-stu-id="eb03c-419">occurrence</span></span>  

### <a name="return-value---setrecord"></a><span data-ttu-id="eb03c-420">戻り値 - setRecord</span><span class="sxs-lookup"><span data-stu-id="eb03c-420">Return Value - setRecord</span></span>

## <a name="method-title"></a><span data-ttu-id="eb03c-421">メソッド title</span><span class="sxs-lookup"><span data-stu-id="eb03c-421">Method title</span></span>

```xpp
public str title([str value])
```

### <a name="parameters---title"></a><span data-ttu-id="eb03c-422">パラメーター - title</span><span class="sxs-lookup"><span data-stu-id="eb03c-422">Parameters - title</span></span>

<span data-ttu-id="eb03c-423">値</span><span class="sxs-lookup"><span data-stu-id="eb03c-423">value</span></span>  

### <a name="return-value---title"></a><span data-ttu-id="eb03c-424">戻り値 - title</span><span class="sxs-lookup"><span data-stu-id="eb03c-424">Return Value - title</span></span>

## <a name="method-tostring"></a><span data-ttu-id="eb03c-425">メソッド toString</span><span class="sxs-lookup"><span data-stu-id="eb03c-425">Method toString</span></span>

<span data-ttu-id="eb03c-426">現在のオブジェクトを表す文字列を返します。</span><span class="sxs-lookup"><span data-stu-id="eb03c-426">Returns a string that represents the current object.</span></span>

```xpp
public str toString()
```

### <a name="return-value---tostring"></a><span data-ttu-id="eb03c-427">戻り値 - toString</span><span class="sxs-lookup"><span data-stu-id="eb03c-427">Return Value - toString</span></span>

<span data-ttu-id="eb03c-428">現在のオブジェクトを表す文字列。</span><span class="sxs-lookup"><span data-stu-id="eb03c-428">A string that represents the current object.</span></span>

### <a name="remarks---tostring"></a><span data-ttu-id="eb03c-429">備考 - toString</span><span class="sxs-lookup"><span data-stu-id="eb03c-429">Remarks - toString</span></span>

<span data-ttu-id="eb03c-430">既定の実装は、オブジェクトのクラス名を返します。</span><span class="sxs-lookup"><span data-stu-id="eb03c-430">The default implementation returns the class name of the object.</span></span> <span data-ttu-id="eb03c-431">メソッドは派生クラスで上書きできるため、そのタイプの意味のある値が返されます。</span><span class="sxs-lookup"><span data-stu-id="eb03c-431">The method can be overridden in a derived class to return values that are meaningful for that type.</span></span> <span data-ttu-id="eb03c-432">たとえば、SysMethodInfo クラスのインスタンスは、インスタンスまたは静的などのメソッド名およびメソッドのタイプを返します。</span><span class="sxs-lookup"><span data-stu-id="eb03c-432">For example, an instance of the SysMethodInfo class returns the method name and type of the method, such as instance or static.</span></span>

## <a name="method-userupdate"></a><span data-ttu-id="eb03c-433">メソッド userUpdate</span><span class="sxs-lookup"><span data-stu-id="eb03c-433">Method userUpdate</span></span>

```xpp
public boolean userUpdate([boolean value])
```

### <a name="parameters---userupdate"></a><span data-ttu-id="eb03c-434">パラメーター - userUpdate</span><span class="sxs-lookup"><span data-stu-id="eb03c-434">Parameters - userUpdate</span></span>

<span data-ttu-id="eb03c-435">値</span><span class="sxs-lookup"><span data-stu-id="eb03c-435">value</span></span>  

### <a name="return-value---userupdate"></a><span data-ttu-id="eb03c-436">戻り値 - userUpdate</span><span class="sxs-lookup"><span data-stu-id="eb03c-436">Return Value - userUpdate</span></span>

## <a name="method-version"></a><span data-ttu-id="eb03c-437">メソッド version</span><span class="sxs-lookup"><span data-stu-id="eb03c-437">Method version</span></span>

```xpp
public int version([int value])
```

### <a name="parameters---version"></a><span data-ttu-id="eb03c-438">パラメーター - version</span><span class="sxs-lookup"><span data-stu-id="eb03c-438">Parameters - version</span></span>

<span data-ttu-id="eb03c-439">値</span><span class="sxs-lookup"><span data-stu-id="eb03c-439">value</span></span>  

### <a name="return-value---version"></a><span data-ttu-id="eb03c-440">戻り値 - version</span><span class="sxs-lookup"><span data-stu-id="eb03c-440">Return Value - version</span></span>

## <a name="method-getqueryrowcount"></a><span data-ttu-id="eb03c-441">メソッド getQueryRowCount</span><span class="sxs-lookup"><span data-stu-id="eb03c-441">Method getQueryRowCount</span></span>

```xpp
public static int getQueryRowCount(Query query, int maxRows)
```

### <a name="parameters---getqueryrowcount"></a><span data-ttu-id="eb03c-442">パラメーター - getQueryRowCount</span><span class="sxs-lookup"><span data-stu-id="eb03c-442">Parameters - getQueryRowCount</span></span>

<span data-ttu-id="eb03c-443">クエリ</span><span class="sxs-lookup"><span data-stu-id="eb03c-443">query</span></span>  

<!-- -->

<span data-ttu-id="eb03c-444">maxRows</span><span class="sxs-lookup"><span data-stu-id="eb03c-444">maxRows</span></span>  

### <a name="return-value---getqueryrowcount"></a><span data-ttu-id="eb03c-445">戻り値 - getQueryRowCount</span><span class="sxs-lookup"><span data-stu-id="eb03c-445">Return Value - getQueryRowCount</span></span>

## <a name="method-runandpopulate"></a><span data-ttu-id="eb03c-446">メソッド runAndPopulate</span><span class="sxs-lookup"><span data-stu-id="eb03c-446">Method runAndPopulate</span></span>

```xpp
public static int runAndPopulate(Query sourceRuery, Common targetTable, Map queryAliasesAndTargetColumnsMap)
```

### <a name="parameters---runandpopulate"></a><span data-ttu-id="eb03c-447">パラメーター - runAndPopulate</span><span class="sxs-lookup"><span data-stu-id="eb03c-447">Parameters - runAndPopulate</span></span>

<span data-ttu-id="eb03c-448">sourceRuery</span><span class="sxs-lookup"><span data-stu-id="eb03c-448">sourceRuery</span></span>  

<!-- -->

<span data-ttu-id="eb03c-449">targetTable</span><span class="sxs-lookup"><span data-stu-id="eb03c-449">targetTable</span></span>  

<!-- -->

<span data-ttu-id="eb03c-450">queryAliasesAndTargetColumnsMap</span><span class="sxs-lookup"><span data-stu-id="eb03c-450">queryAliasesAndTargetColumnsMap</span></span>  

### <a name="return-value---runandpopulate"></a><span data-ttu-id="eb03c-451">戻り値 - runAndPopulate</span><span class="sxs-lookup"><span data-stu-id="eb03c-451">Return Value - runAndPopulate</span></span>

## <a name="method-run"></a><span data-ttu-id="eb03c-452">メソッド run</span><span class="sxs-lookup"><span data-stu-id="eb03c-452">Method run</span></span>

<span data-ttu-id="eb03c-453">ユーザーからクエリに関する情報を取得するために使用されるフォームを開いて、一致するレコードをフェッチします。</span><span class="sxs-lookup"><span data-stu-id="eb03c-453">Opens a form used to obtain information about the query from the user, and fetches the matching records.</span></span>

```xpp
public void run()
```

### <a name="remarks---run"></a><span data-ttu-id="eb03c-454">備考 - run</span><span class="sxs-lookup"><span data-stu-id="eb03c-454">Remarks - run</span></span>

<span data-ttu-id="eb03c-455">クエリを実行すると、ユーザーによって入力された制約を満たすレコードが検索されます。</span><span class="sxs-lookup"><span data-stu-id="eb03c-455">Running the query will find the records that satisfy the constraints entered by the user.</span></span> <span data-ttu-id="eb03c-456">ただし、この方法でのクエリの実行には副作用がありません。</span><span class="sxs-lookup"><span data-stu-id="eb03c-456">However, running the query in this manner has no side effects.</span></span> <span data-ttu-id="eb03c-457">扱いやすくするために、1 つ以上の継承されたメソッドをオーバーロードする必要があります。</span><span class="sxs-lookup"><span data-stu-id="eb03c-457">In order to be useful, one or more of the inherited methods must be overloaded.</span></span>

## <a name="method-new"></a><span data-ttu-id="eb03c-458">メソッド new</span><span class="sxs-lookup"><span data-stu-id="eb03c-458">Method new</span></span>

<span data-ttu-id="eb03c-459">Object クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="eb03c-459">Initializes a new instance of the Object class.</span></span>

```xpp
public void new(AnyType source)
```

### <a name="parameters---new"></a><span data-ttu-id="eb03c-460">パラメーター - new</span><span class="sxs-lookup"><span data-stu-id="eb03c-460">Parameters - new</span></span>

<span data-ttu-id="eb03c-461">ソース</span><span class="sxs-lookup"><span data-stu-id="eb03c-461">source</span></span>  

### <a name="remarks---new"></a><span data-ttu-id="eb03c-462">備考 - new</span><span class="sxs-lookup"><span data-stu-id="eb03c-462">Remarks - new</span></span>

<span data-ttu-id="eb03c-463">クエリ クラスのインスタンスを QueryRun クラスのコンストラクターに渡すと、クエリ オブジェクトのコピーが作成されます。</span><span class="sxs-lookup"><span data-stu-id="eb03c-463">When you pass an instance of the Query class into this constructor of the QueryRun class, a copy of the Query object is created.</span></span> <span data-ttu-id="eb03c-464">このクエリ オブジェクト のコピーに加えられた変更は、元のクエリ オブジェクトには影響しません。</span><span class="sxs-lookup"><span data-stu-id="eb03c-464">Changes that are made to this copy of the Query object do not affect the original Query object.</span></span>

## <a name="method-addpagerange"></a><span data-ttu-id="eb03c-465">メソッド addPageRange</span><span class="sxs-lookup"><span data-stu-id="eb03c-465">Method addPageRange</span></span>

```xpp
public void addPageRange([Int64 startingPosition], [Int64 numberOfRecordsToFetch])
```

### <a name="parameters---addpagerange"></a><span data-ttu-id="eb03c-466">パラメーター - addPageRange</span><span class="sxs-lookup"><span data-stu-id="eb03c-466">Parameters - addPageRange</span></span>

<span data-ttu-id="eb03c-467">startingPosition</span><span class="sxs-lookup"><span data-stu-id="eb03c-467">startingPosition</span></span>  

<!-- -->

<span data-ttu-id="eb03c-468">numberOfRecordsToFetch</span><span class="sxs-lookup"><span data-stu-id="eb03c-468">numberOfRecordsToFetch</span></span>  

## <a name="method-reset"></a><span data-ttu-id="eb03c-469">メソッド reset</span><span class="sxs-lookup"><span data-stu-id="eb03c-469">Method reset</span></span>

```xpp
public void reset()
```

## <a name="method-setimportsession"></a><span data-ttu-id="eb03c-470">メソッド setImportSession</span><span class="sxs-lookup"><span data-stu-id="eb03c-470">Method setImportSession</span></span>

```xpp
public void setImportSession(Guid importSession)
```

### <a name="parameters---setimportsession"></a><span data-ttu-id="eb03c-471">パラメーター - setImportSession</span><span class="sxs-lookup"><span data-stu-id="eb03c-471">Parameters - setImportSession</span></span>

<span data-ttu-id="eb03c-472">importSession</span><span class="sxs-lookup"><span data-stu-id="eb03c-472">importSession</span></span>  

## <a name="method-setquerytimeout"></a><span data-ttu-id="eb03c-473">メソッド setQuerytimeout</span><span class="sxs-lookup"><span data-stu-id="eb03c-473">Method setQuerytimeout</span></span>

```xpp
public void setQuerytimeout(int seconds, [boolean raiseException])
```

### <a name="parameters---setquerytimeout"></a><span data-ttu-id="eb03c-474">パラメーター - setQuerytimeout</span><span class="sxs-lookup"><span data-stu-id="eb03c-474">Parameters - setQuerytimeout</span></span>

<span data-ttu-id="eb03c-475">秒</span><span class="sxs-lookup"><span data-stu-id="eb03c-475">seconds</span></span>  

<!-- -->

<span data-ttu-id="eb03c-476">raiseException</span><span class="sxs-lookup"><span data-stu-id="eb03c-476">raiseException</span></span>  

## <a name="method-init"></a><span data-ttu-id="eb03c-477">メソッド init</span><span class="sxs-lookup"><span data-stu-id="eb03c-477">Method init</span></span>

```xpp
public void init()
```

## <a name="method-enablepositionpaging"></a><span data-ttu-id="eb03c-478">メソッド enablePositionPaging</span><span class="sxs-lookup"><span data-stu-id="eb03c-478">Method enablePositionPaging</span></span>

```xpp
public void enablePositionPaging([boolean enabled])
```

### <a name="parameters---enablepositionpaging"></a><span data-ttu-id="eb03c-479">パラメーター - enablePositionPaging</span><span class="sxs-lookup"><span data-stu-id="eb03c-479">Parameters - enablePositionPaging</span></span>

<span data-ttu-id="eb03c-480">有効</span><span class="sxs-lookup"><span data-stu-id="eb03c-480">enabled</span></span>  

## <a name="method-shred"></a><span data-ttu-id="eb03c-481">メソッド shred</span><span class="sxs-lookup"><span data-stu-id="eb03c-481">Method shred</span></span>

```xpp
public void shred(Guid importSession)
```

### <a name="parameters---shred"></a><span data-ttu-id="eb03c-482">パラメーター - shred</span><span class="sxs-lookup"><span data-stu-id="eb03c-482">Parameters - shred</span></span>

<span data-ttu-id="eb03c-483">importSession</span><span class="sxs-lookup"><span data-stu-id="eb03c-483">importSession</span></span>  

## <a name="method-enablevaluebasedpaging"></a><span data-ttu-id="eb03c-484">メソッド enableValueBasedPaging</span><span class="sxs-lookup"><span data-stu-id="eb03c-484">Method enableValueBasedPaging</span></span>

```xpp
public void enableValueBasedPaging([boolean enable])
```

### <a name="parameters---enablevaluebasedpaging"></a><span data-ttu-id="eb03c-485">パラメーター - enableValueBasedPaging</span><span class="sxs-lookup"><span data-stu-id="eb03c-485">Parameters - enableValueBasedPaging</span></span>

<span data-ttu-id="eb03c-486">enable</span><span class="sxs-lookup"><span data-stu-id="eb03c-486">enable</span></span>  

## <a name="method-bulknext"></a><span data-ttu-id="eb03c-487">メソッド bulkNext</span><span class="sxs-lookup"><span data-stu-id="eb03c-487">Method bulkNext</span></span>

```xpp
public void bulkNext([boolean fetchAllData])
```

### <a name="parameters---bulknext"></a><span data-ttu-id="eb03c-488">パラメーター - bulkNext</span><span class="sxs-lookup"><span data-stu-id="eb03c-488">Parameters - bulkNext</span></span>

<span data-ttu-id="eb03c-489">fetchAllData</span><span class="sxs-lookup"><span data-stu-id="eb03c-489">fetchAllData</span></span>  

## <a name="method-applyvaluebasedpaging"></a><span data-ttu-id="eb03c-490">メソッド applyValueBasedPaging</span><span class="sxs-lookup"><span data-stu-id="eb03c-490">Method applyValueBasedPaging</span></span>

```xpp
public void applyValueBasedPaging([Common sourceCursor], [boolean isForward])
```

### <a name="parameters---applyvaluebasedpaging"></a><span data-ttu-id="eb03c-491">パラメーター - applyValueBasedPaging</span><span class="sxs-lookup"><span data-stu-id="eb03c-491">Parameters - applyValueBasedPaging</span></span>

<span data-ttu-id="eb03c-492">sourceCursor</span><span class="sxs-lookup"><span data-stu-id="eb03c-492">sourceCursor</span></span>  

<!-- -->

<span data-ttu-id="eb03c-493">isForward</span><span class="sxs-lookup"><span data-stu-id="eb03c-493">isForward</span></span>  

## <a name="method-skipautoorderby"></a><span data-ttu-id="eb03c-494">メソッド skipAutoOrderBy</span><span class="sxs-lookup"><span data-stu-id="eb03c-494">Method skipAutoOrderBy</span></span>

```xpp
Specifies whether an Order By clause will be generated, in case no Order By field was specified.
public boolean skipAutoOrderBy([boolean value])

```

<span data-ttu-id="eb03c-495">先頭値</span><span class="sxs-lookup"><span data-stu-id="eb03c-495">Value</span></span>
### <a name="return-value---skipautoorderby"></a><span data-ttu-id="eb03c-496">戻り値 - skipAutoOrderBy</span><span class="sxs-lookup"><span data-stu-id="eb03c-496">Return Value - skipAutoOrderBy</span></span>
<span data-ttu-id="eb03c-497">パラメーターが指定されていない場合は現在の値、パラメーターが指定されている場合は新しい値です。</span><span class="sxs-lookup"><span data-stu-id="eb03c-497">The current value if no parameter is specified, the new value if a parameter was specified.</span></span>
### <a name="remarks---skipautoorderby"></a><span data-ttu-id="eb03c-498">備考 - skipAutoOrderBy</span><span class="sxs-lookup"><span data-stu-id="eb03c-498">Remarks - skipAutoOrderBy</span></span>
<span data-ttu-id="eb03c-499">既定では SkipAutoOrderBy は false で、プラットフォーム更新プログラム 31 以降で使用可能です。</span><span class="sxs-lookup"><span data-stu-id="eb03c-499">SkipAutoOrderBy is false by default and available in Platform update 31 and later</span></span>
