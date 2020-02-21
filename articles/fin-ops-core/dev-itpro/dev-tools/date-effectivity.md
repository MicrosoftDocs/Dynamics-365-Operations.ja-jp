---
title: 日付の有効期間
description: このトピックでは、データ エンティティとデータ ソースの開始日時に関する情報を提供し、エンティティの開始日時を作成する方法を示します。 また、日付の有効性が読み取りおよび書き込みアクティビティに適用される方法についても説明します。
author: Sunil-Garg
manager: AnnBe
ms.date: 12/04/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Developer
ms.reviewer: rhaertle
ms.search.scope: Operations
ms.custom: 24861
ms.assetid: 63e43066-76c7-400b-be7d-d14785e7985d
ms.search.region: Global
ms.author: sunilg
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 08a670e1a43a37cd56844e593c1e2be1ff68619b
ms.sourcegitcommit: 9f90b194c0fc751d866d3d24d57ecf1b3c5053a1
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/07/2020
ms.locfileid: "3033016"
---
# <a name="date-effectivity"></a><span data-ttu-id="f7c42-104">日付の有効期間</span><span class="sxs-lookup"><span data-stu-id="f7c42-104">Date effectivity</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="f7c42-105">このトピックでは、データ エンティティとデータ ソースの開始日時に関する情報を提供し、エンティティの開始日時を作成する方法を示します。</span><span class="sxs-lookup"><span data-stu-id="f7c42-105">This topic provides information about date-effective data entities and data sources, and shows how to create a date-effective entity.</span></span> <span data-ttu-id="f7c42-106">また、日付の有効性が読み取りおよび書き込みアクティビティに適用される方法についても説明します。</span><span class="sxs-lookup"><span data-stu-id="f7c42-106">It also explains how date effectivity applies to read and write activities.</span></span>

<span data-ttu-id="f7c42-107">データ エンティティを含む日付有効機能のデザイン パターンはさまざまです。</span><span class="sxs-lookup"><span data-stu-id="f7c42-107">There are different design patterns for date-effective features that involve data entities.</span></span> <span data-ttu-id="f7c42-108">パターンは、次の 2 つの主要なカテゴリに分類されます。</span><span class="sxs-lookup"><span data-stu-id="f7c42-108">The patterns are classified into two main categories:</span></span>

-   <span data-ttu-id="f7c42-109">**有効日エンティティ** - エンティティには少なくとも 1 つの有効日データ ソースがあり、エンティティ自体も日付が有効です。</span><span class="sxs-lookup"><span data-stu-id="f7c42-109">**Date-effective entities** – The entity has at least one date-effective data source, and the entity itself is also date effective.</span></span>
-   <span data-ttu-id="f7c42-110">**有効日の対象外のエンティティ** – エンティティ自体は、有効日ではありませんが、有効日データ ソースが含まれています。</span><span class="sxs-lookup"><span data-stu-id="f7c42-110">**Non-date-effective entities** – The entity itself is not date effective, but it does contain date-effective data sources.</span></span>

<span data-ttu-id="f7c42-111">次のセクションでは、プロパティの小さなリストとエンティティの日付を有効にする操作と有効日データ ソースを制御するメソッドについて説明します。</span><span class="sxs-lookup"><span data-stu-id="f7c42-111">The next sections describe the small list of properties and methods that control the date-effective behavior of entities and their date-effective data sources.</span></span>

## <a name="date-effective-entities"></a><span data-ttu-id="f7c42-112">有効日のエンティティ</span><span class="sxs-lookup"><span data-stu-id="f7c42-112">Date-effective entities</span></span>
<span data-ttu-id="f7c42-113">次のテーブルは、データ エンティティの日付を有効にする操作を制御するプロパティを示しています。</span><span class="sxs-lookup"><span data-stu-id="f7c42-113">The following table describes the properties that control the date-effective behavior of a data entity.</span></span>

| <span data-ttu-id="f7c42-114">エンティティのプロパティ名</span><span class="sxs-lookup"><span data-stu-id="f7c42-114">Property name of the entity</span></span> | <span data-ttu-id="f7c42-115">プロパティのノード</span><span class="sxs-lookup"><span data-stu-id="f7c42-115">Node of the property</span></span>                                    | <span data-ttu-id="f7c42-116">先頭値</span><span class="sxs-lookup"><span data-stu-id="f7c42-116">Value</span></span>       | <span data-ttu-id="f7c42-117">説明</span><span class="sxs-lookup"><span data-stu-id="f7c42-117">Description</span></span>                                                                                                                                                                                                                                                                                                                                                  |
|-----------------------------|---------------------------------------------------------|-------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f7c42-118">ValidTimeStateEnabled</span><span class="sxs-lookup"><span data-stu-id="f7c42-118">ValidTimeStateEnabled</span></span>       | <span data-ttu-id="f7c42-119">デザイナーのデータ エンティティ ノード</span><span class="sxs-lookup"><span data-stu-id="f7c42-119">Data entity node in the designer</span></span>                        | <span data-ttu-id="f7c42-120">はい (またはいいえ)</span><span class="sxs-lookup"><span data-stu-id="f7c42-120">Yes (or No)</span></span> | <span data-ttu-id="f7c42-121">値 **Yes** は、エンティティの日付を有効にします。</span><span class="sxs-lookup"><span data-stu-id="f7c42-121">The value **Yes** makes the entity date effective.</span></span> <span data-ttu-id="f7c42-122">エンティティには、**ValidFrom** および **ValidTo** フィールドが必要です。</span><span class="sxs-lookup"><span data-stu-id="f7c42-122">The entity must have **ValidFrom** and **ValidTo** fields.</span></span> <span data-ttu-id="f7c42-123">これらのフィールドは、有効日データ ソースの **ValidFrom** フィールドおよび **ValidTo** フィールドにマップされます。</span><span class="sxs-lookup"><span data-stu-id="f7c42-123">These fields are mapped to the **ValidFrom** and **ValidTo** fields of a date-effective data source.</span></span> <span data-ttu-id="f7c42-124">値 **No** は、エンティティのデータ ソースである日付有効テーブルの日付有効性の強制を無効に*しません*。</span><span class="sxs-lookup"><span data-stu-id="f7c42-124">The value **No** does *not* disable the enforcement of date effectivity on any date-effective tables that are data sources of the entity.</span></span> |
| <span data-ttu-id="f7c42-125">ValidTimeStateKey</span><span class="sxs-lookup"><span data-stu-id="f7c42-125">ValidTimeStateKey</span></span>           | <span data-ttu-id="f7c42-126">データ エンティティ ノードの下では、**キー**&gt;**EntityKey**</span><span class="sxs-lookup"><span data-stu-id="f7c42-126">Under the data entity node, **Keys** &gt; **EntityKey**</span></span> | <span data-ttu-id="f7c42-127">はい (またはいいえ)</span><span class="sxs-lookup"><span data-stu-id="f7c42-127">Yes (or No)</span></span> | <span data-ttu-id="f7c42-128">値 **Yes** は、この特定のエンティティの日付有効値を実施するために必要なキーを識別します。</span><span class="sxs-lookup"><span data-stu-id="f7c42-128">The value **Yes** identifies the key that is required to enforce the date-effective values on this particular entity.</span></span>                                                                                                                                                                                                                                        |

## <a name="read-activities"></a><span data-ttu-id="f7c42-129">読み取りアクティビティ</span><span class="sxs-lookup"><span data-stu-id="f7c42-129">Read activities</span></span>
<span data-ttu-id="f7c42-130">日付の有効期限がデータ エンティティ レベルで設定されると、エンティティからの読み取りはテーブルからの読み取りと動作が同じです。</span><span class="sxs-lookup"><span data-stu-id="f7c42-130">When date effectivity is set at the data entity level, reads from the entity behave the same way as reads from a table.</span></span> <span data-ttu-id="f7c42-131">エンティティには、システムが読み込み中に日付フィルターを適用する **ValidFrom** および **ValidTo** フィールドがあります。</span><span class="sxs-lookup"><span data-stu-id="f7c42-131">The entity has **ValidFrom** and **ValidTo** fields that the system applies date filters to during reads.</span></span>

### <a name="query-modes-and-the-validtimestate-keyword-of-x-sql-select"></a><span data-ttu-id="f7c42-132">クエリ モードと X++ SQL 選択の validtimestate キーワード</span><span class="sxs-lookup"><span data-stu-id="f7c42-132">Query modes and the validtimestate keyword of X++ SQL select</span></span>

<span data-ttu-id="f7c42-133">日付有効なエンティティは、X++ **validtimestate** キーワードの使用方法が異なる次の 3 つの*クエリモード*をサポートします。</span><span class="sxs-lookup"><span data-stu-id="f7c42-133">A date-effective entity supports the following three *query modes*, which vary in their use of the X++ **validtimestate** keyword:</span></span>

-   <span data-ttu-id="f7c42-134">**既定のモード** - 現在のレコードは、`select * from FMVehicleRateEntity; // X++ SQL.` を使用して返されます。</span><span class="sxs-lookup"><span data-stu-id="f7c42-134">**Default mode** – Current records are returned using `select * from FMVehicleRateEntity; // X++ SQL.`</span></span>
-   <span data-ttu-id="f7c42-135">**AsOfDate モード** - 指定された日付に有効なレコードは `select validtimestate(d1) * from FMVehicleRateEntity;` を使用して返されます。</span><span class="sxs-lookup"><span data-stu-id="f7c42-135">**AsOfDate mode** – Records valid for the specified date are returned using `select validtimestate(d1) * from FMVehicleRateEntity;`</span></span>
-   <span data-ttu-id="f7c42-136">**AsOfDateRange モード** - 指定された日付範囲に有効なレコードは `select validtimestate(d1,d2) * from FMVehicleRateEntity;` を使用して返されます。</span><span class="sxs-lookup"><span data-stu-id="f7c42-136">**AsOfDateRange mode** – Records valid for the specified date range are returned using `select validtimestate(d1,d2) * from FMVehicleRateEntity;`</span></span>

<span data-ttu-id="f7c42-137">**重要:** それら自体は有効日ではないデータ エンティティでも、有効日のデータ ソースがある場合には、既定のクエリ モードのみ使用できます。</span><span class="sxs-lookup"><span data-stu-id="f7c42-137">**Important:** For data entities that aren't themselves date effective, but that have a data-effective data source, only the default query mode is available.</span></span> <span data-ttu-id="f7c42-138">この概念については、この記事の後半で説明します。</span><span class="sxs-lookup"><span data-stu-id="f7c42-138">This concept is discussed later in this article.</span></span>

### <a name="applying-a-date-filter-at-the-data-source-level"></a><span data-ttu-id="f7c42-139">データ ソース レベルで日付フィルターを適用する</span><span class="sxs-lookup"><span data-stu-id="f7c42-139">Applying a date filter at the data source level</span></span>

<span data-ttu-id="f7c42-140">日付実効フィルタリングが、データ エンティティの外部、データ ソース レベルで必要とされるシナリオがあります。</span><span class="sxs-lookup"><span data-stu-id="f7c42-140">There are scenarios where date-effective filtering is required outside the data entity, at the data source level.</span></span> <span data-ttu-id="f7c42-141">たとえば、顧客エンティティ (CustTableTestEntity) にはデータ ソースとして CustTable および LogisticsPostalAddress が含まれています。LogisticsPostalAddress は日付の有効なテーブルであり、CustTable は通常のテーブルです。</span><span class="sxs-lookup"><span data-stu-id="f7c42-141">For example, the customer entity (CustTableTestEntity) contains CustTable and LogisticsPostalAddress as data sources, where LogisticsPostalAddress is a date-effective table and CustTable is a regular table.</span></span> <span data-ttu-id="f7c42-142">顧客エンティティの目的は、顧客とそのアクティブなプライマリ アドレスのリスト (プライマリ アドレスがある場合) を含めることです。</span><span class="sxs-lookup"><span data-stu-id="f7c42-142">The purpose of a customer entity is to have a list of customers and their active primary addresses, if they have primary addresses.</span></span> <span data-ttu-id="f7c42-143">したがって、顧客エンティティ自体は日付有効ではありませんが、データ ソースの 1 つに日付フィルターが必要です。</span><span class="sxs-lookup"><span data-stu-id="f7c42-143">Therefore, the customer entity itself isn't date effective, but it requires date filters on one of the data sources.</span></span> <span data-ttu-id="f7c42-144">この場合、エンティティは **ValidTimeStateEnabled** にマークされません。</span><span class="sxs-lookup"><span data-stu-id="f7c42-144">In this case, the entity isn't marked **ValidTimeStateEnabled**.</span></span> <span data-ttu-id="f7c42-145">代わりに、**日付フィルターの適用**プロパティがデータ ソースに追加されます。</span><span class="sxs-lookup"><span data-stu-id="f7c42-145">Instead, an **Apply Date Filter** property is added on the data source.</span></span> <span data-ttu-id="f7c42-146">**日付フィルターの適用**の値が**はい**に設定されている場合、日付フィルターがそのデータ ソースに自動的に適用されます。</span><span class="sxs-lookup"><span data-stu-id="f7c42-146">If the value of **Apply Date Filter** is set to **Yes**, date filters are automatically applied to that data source.</span></span> <span data-ttu-id="f7c42-147">次のテーブルでは、データ エンティティの有効日データ ソースの有効日動作を制御するプロパティについて説明します。</span><span class="sxs-lookup"><span data-stu-id="f7c42-147">The following table describes the properties that control the date-effective behavior of a date-effective data source of a data entity.</span></span>

| <span data-ttu-id="f7c42-148">データ ソースのプロパティ名</span><span class="sxs-lookup"><span data-stu-id="f7c42-148">Property name of the data source</span></span> | <span data-ttu-id="f7c42-149">プロパティのノード</span><span class="sxs-lookup"><span data-stu-id="f7c42-149">Node of the property</span></span>                             | <span data-ttu-id="f7c42-150">先頭値</span><span class="sxs-lookup"><span data-stu-id="f7c42-150">Value</span></span>       | <span data-ttu-id="f7c42-151">説明</span><span class="sxs-lookup"><span data-stu-id="f7c42-151">Description</span></span>                                                                                                                                                                                                                                                                                                    |
|----------------------------------|--------------------------------------------------|-------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f7c42-152">日付フィルターの適用</span><span class="sxs-lookup"><span data-stu-id="f7c42-152">Apply Date Filter</span></span>                | <span data-ttu-id="f7c42-153">エンティティの特定のデータ ソースのノード</span><span class="sxs-lookup"><span data-stu-id="f7c42-153">Node of any particular data source of the entity</span></span> | <span data-ttu-id="f7c42-154">はい (またはいいえ)</span><span class="sxs-lookup"><span data-stu-id="f7c42-154">Yes (or No)</span></span> | <span data-ttu-id="f7c42-155">*読み取り*で、このプロパティは、エンティティ データ ソースで日付フィルターが適用されるかどうかを制御します。</span><span class="sxs-lookup"><span data-stu-id="f7c42-155">For *reads*, this property controls whether date filters are applied on the entity data source.</span></span> <span data-ttu-id="f7c42-156">この場合、データ ソースを **ValidTimeStateEnabled** にマークする必要があります。</span><span class="sxs-lookup"><span data-stu-id="f7c42-156">In this case, the data source should be marked **ValidTimeStateEnabled**.</span></span> <span data-ttu-id="f7c42-157">このプロパティ値は、エンティティ自体が日付有効であるかどうかにかかわらず有効です。</span><span class="sxs-lookup"><span data-stu-id="f7c42-157">This property value has effect regardless of whether the entity itself is date effective.</span></span> <span data-ttu-id="f7c42-158">*書き込み*で、このプロパティは影響を与えません。</span><span class="sxs-lookup"><span data-stu-id="f7c42-158">For *writes*, this property has no effect.</span></span> |

<span data-ttu-id="f7c42-159">この記事では、これらの日付が有効なプロパティの使用方法とそれらの相互作用について説明します。</span><span class="sxs-lookup"><span data-stu-id="f7c42-159">This article describes the use of these date-effective properties and the interactions between them.</span></span>

### <a name="state-matrixes-for-reads"></a><span data-ttu-id="f7c42-160">読み取り用の状態マトリックス</span><span class="sxs-lookup"><span data-stu-id="f7c42-160">State matrixes for reads</span></span>

<span data-ttu-id="f7c42-161">このセクションは、データ エンティティからの読み取りのみに関係します。</span><span class="sxs-lookup"><span data-stu-id="f7c42-161">This section concerns only reads from the data entity.</span></span> <span data-ttu-id="f7c42-162">以下の一対の参照マトリックスは、データ エンティティとそのデータ ソースとの間に存在できる日付有効状態の組み合わせについて説明します。</span><span class="sxs-lookup"><span data-stu-id="f7c42-162">The following pair of reference matrixes describe the combinations of date-effective states that can exist between a data entity and its data source.</span></span> <span data-ttu-id="f7c42-163">各テーブルには、4 つのクラスが含まれ、各ケースでは、2 つの異なるターゲットについて説明します。</span><span class="sxs-lookup"><span data-stu-id="f7c42-163">Each table contains four cases, and each case discusses two distinct targets.</span></span> <span data-ttu-id="f7c42-164">理解しておく必要がある主要なポイントを次に示します。</span><span class="sxs-lookup"><span data-stu-id="f7c42-164">Here are the primary points that you should understand:</span></span>

-   <span data-ttu-id="f7c42-165">エンティティから指定された読み取りで、クエリ モードはエンティティと有効日データ ソースの両方で同じです。</span><span class="sxs-lookup"><span data-stu-id="f7c42-165">On any given read from the entity, the query mode is the same for both the entity and date-effective data sources.</span></span>
-   <span data-ttu-id="f7c42-166">エンティティの日付が有効ではない場合、クエリ モードは既定のモードに限定されます。</span><span class="sxs-lookup"><span data-stu-id="f7c42-166">If the entity is not date effective, the query mode is limited to the default mode.</span></span> <span data-ttu-id="f7c42-167">したがって、日付が有効なデータ ソースは現在の日付のみにアクセスされます。</span><span class="sxs-lookup"><span data-stu-id="f7c42-167">Therefore, the date-effective data source is accessed only for the current date.</span></span>
-   <span data-ttu-id="f7c42-168">有効日データ ソースで、**日付フィルターの適用**プロパティを**いいえ**に設定すると、過去、現在、未来のすべてのデータをデータソースに戻すことができます。</span><span class="sxs-lookup"><span data-stu-id="f7c42-168">On the date-effective data source, the **Apply Date Filter** property can be set to **No** to make the data source return all data – past, current, and future.</span></span>
-   <span data-ttu-id="f7c42-169">OData で、日付の有効なフィルターはデータ エンティティには適用されません。</span><span class="sxs-lookup"><span data-stu-id="f7c42-169">For OData, date-effective filters are not applied to the data entity.</span></span> <span data-ttu-id="f7c42-170">ただし、データ ソースのフィルターはすべてのコード パスに適用されます。</span><span class="sxs-lookup"><span data-stu-id="f7c42-170">However, filters on the data source are applied at all code paths.</span></span>

<span data-ttu-id="f7c42-171">A.</span><span class="sxs-lookup"><span data-stu-id="f7c42-171">A.</span></span> <span data-ttu-id="f7c42-172">エンティティは有効日で*ある*、なぜならば ValidTimeStateEnabled = はい</span><span class="sxs-lookup"><span data-stu-id="f7c42-172">Entity *is* date effective, because ValidTimeStateEnabled = Yes</span></span>

<span data-ttu-id="f7c42-173">**データ ソース*は*日付が有効**</span><span class="sxs-lookup"><span data-stu-id="f7c42-173">**Data source *is* date effective**</span></span>

<span data-ttu-id="f7c42-174">**データ ソース*は*日付が有効ではない**</span><span class="sxs-lookup"><span data-stu-id="f7c42-174">**Data source is *not* date effective**</span></span>

<span data-ttu-id="f7c42-175">**日付フィルターの適用 = はい**</span><span class="sxs-lookup"><span data-stu-id="f7c42-175">**Apply Date Filter = Yes**</span></span>

-   <span data-ttu-id="f7c42-176">**エンティティ** 日付フィルターが適用されます。</span><span class="sxs-lookup"><span data-stu-id="f7c42-176">**Entity:** Date filters are applied.</span></span> <span data-ttu-id="f7c42-177">すべてのクエリ モードがサポートされています。</span><span class="sxs-lookup"><span data-stu-id="f7c42-177">Any query mode is supported.</span></span>
-   <span data-ttu-id="f7c42-178">**データ ソース:** フィルターが適用されます。</span><span class="sxs-lookup"><span data-stu-id="f7c42-178">**Data source:** Filters are applied.</span></span> <span data-ttu-id="f7c42-179">クエリ モードはサポートされていますが、モードはエンティティのコードと同じです。</span><span class="sxs-lookup"><span data-stu-id="f7c42-179">Any query mode is supported, but the mode is the same as is coded for the entity.</span></span>

<span data-ttu-id="f7c42-180">有効日の対象外のデータ ソースは影響しません。</span><span class="sxs-lookup"><span data-stu-id="f7c42-180">Non-date-effective data sources aren't affected.</span></span>

<span data-ttu-id="f7c42-181">**日付フィルターの適用 = いいえ**</span><span class="sxs-lookup"><span data-stu-id="f7c42-181">**Apply Date Filter = No**</span></span>

-   <span data-ttu-id="f7c42-182">**エンティティ** 日付フィルターが適用されます。</span><span class="sxs-lookup"><span data-stu-id="f7c42-182">**Entity:** Date filters are applied.</span></span> <span data-ttu-id="f7c42-183">すべてのクエリ モードがサポートされています。</span><span class="sxs-lookup"><span data-stu-id="f7c42-183">Any query mode is supported.</span></span>
-   <span data-ttu-id="f7c42-184">**データ ソース:** 日付フィルターは適用されません。</span><span class="sxs-lookup"><span data-stu-id="f7c42-184">**Data source:** No date filters are applied.</span></span>

<span data-ttu-id="f7c42-185">有効日の対象外のデータ ソースは影響しません。</span><span class="sxs-lookup"><span data-stu-id="f7c42-185">Non-date-effective data sources aren't affected.</span></span>



<span data-ttu-id="f7c42-186">B.</span><span class="sxs-lookup"><span data-stu-id="f7c42-186">B.</span></span> <span data-ttu-id="f7c42-187">エンティティは有効日では*ない*、なぜならば ValidTimeStateEnabled = いいえ</span><span class="sxs-lookup"><span data-stu-id="f7c42-187">Entity is *not* date effective, because ValidTimeStateEnabled = No</span></span>

<span data-ttu-id="f7c42-188">**データ ソース*は*日付が有効**</span><span class="sxs-lookup"><span data-stu-id="f7c42-188">**Data source *is* date effective**</span></span>

<span data-ttu-id="f7c42-189">**データ ソース*は*日付が有効ではない**</span><span class="sxs-lookup"><span data-stu-id="f7c42-189">**Data source is *not* date effective**</span></span>

<span data-ttu-id="f7c42-190">**日付フィルターの適用 = はい**</span><span class="sxs-lookup"><span data-stu-id="f7c42-190">**Apply Date Filter = Yes**</span></span>

-   <span data-ttu-id="f7c42-191">**エンティティ** 日付フィルターが適用されません。</span><span class="sxs-lookup"><span data-stu-id="f7c42-191">**Entity:** No date filters are applied.</span></span>
-   <span data-ttu-id="f7c42-192">**データ ソース:** 日付フィルターが適用されます。</span><span class="sxs-lookup"><span data-stu-id="f7c42-192">**Data source:** Date filters are applied.</span></span> <span data-ttu-id="f7c42-193">既定のクエリ モードのみサポートされ、X++ **validtimestate** キーワードは省略されます。</span><span class="sxs-lookup"><span data-stu-id="f7c42-193">Only the default query mode is supported, where the X++ **validtimestate** keyword is omitted.</span></span>

<span data-ttu-id="f7c42-194">有効日の対象外のデータ ソースは影響しません。</span><span class="sxs-lookup"><span data-stu-id="f7c42-194">Non-date-effective data sources aren't affected.</span></span>

<span data-ttu-id="f7c42-195">**日付フィルターの適用 = いいえ**</span><span class="sxs-lookup"><span data-stu-id="f7c42-195">**Apply Date Filter = No**</span></span>

-   <span data-ttu-id="f7c42-196">**エンティティ** 日付フィルターが適用されません。</span><span class="sxs-lookup"><span data-stu-id="f7c42-196">**Entity:** No date filters are applied.</span></span>
-   <span data-ttu-id="f7c42-197">**データ ソース:** 日付フィルターは適用されません。</span><span class="sxs-lookup"><span data-stu-id="f7c42-197">**Data source:** No date filters are applied.</span></span>

<span data-ttu-id="f7c42-198">有効日の対象外のデータ ソースは影響しません。</span><span class="sxs-lookup"><span data-stu-id="f7c42-198">Non-date-effective data sources aren't affected.</span></span>

<span data-ttu-id="f7c42-199">次のスクリーン ショットは、**日付フィルターの適用** プロパティを **はい** に設定したものです。</span><span class="sxs-lookup"><span data-stu-id="f7c42-199">The following screen shot shows the **Apply Date Filter** property set to **Yes**.</span></span> <span data-ttu-id="f7c42-200">したがって、**Address** データ ソースの読み取りに日付フィルターが適用されます。</span><span class="sxs-lookup"><span data-stu-id="f7c42-200">Therefore, date filters will be applied to reads of the **Address** data source.</span></span> 

<span data-ttu-id="f7c42-201">[![日付フィルターの適用 = はい](./media/date1.png)](./media/date1.png)</span><span class="sxs-lookup"><span data-stu-id="f7c42-201">[![Apply Date Filter = Yes](./media/date1.png)](./media/date1.png)</span></span>

## <a name="write-activities"></a><span data-ttu-id="f7c42-202">活動の記述</span><span class="sxs-lookup"><span data-stu-id="f7c42-202">Write activities</span></span>
<span data-ttu-id="f7c42-203">このセクションでは、有効日エンティティとその有効日データ ソースの動作を設定するオプションについて説明します。</span><span class="sxs-lookup"><span data-stu-id="f7c42-203">This section describes your options for configuring the behavior of date-effective entities and their date-effective data sources.</span></span> <span data-ttu-id="f7c42-204">有効日テーブルの概念を確認し、それを有効日エンティティと対比させることから開始します。</span><span class="sxs-lookup"><span data-stu-id="f7c42-204">We will start by reviewing the concept of date-effective tables and contrasting them with date-effective entities.</span></span> <span data-ttu-id="f7c42-205">**有効日テーブル:** データが有効日テーブルに挿入または更新されると、プロセスは、**xRecord.validTimeStateUpdateMode** メソッドをテーブルバッファーで呼び出すことができます。</span><span class="sxs-lookup"><span data-stu-id="f7c42-205">**Date-effective table:** When data is inserted or updated in a date-effective table, the process has the option of calling the **xRecord.validTimeStateUpdateMode** method on the table buffer.</span></span> <span data-ttu-id="f7c42-206">このメソッドは、**ValidTimeStateUpdate** 列挙型の要素を受け入れます。</span><span class="sxs-lookup"><span data-stu-id="f7c42-206">The method accepts an element of the **ValidTimeStateUpdate** enumeration.</span></span> <span data-ttu-id="f7c42-207">使用可能な要素値を次に示します。</span><span class="sxs-lookup"><span data-stu-id="f7c42-207">Here are the available element values:</span></span>

-   <span data-ttu-id="f7c42-208">CreateNewTimePeriod</span><span class="sxs-lookup"><span data-stu-id="f7c42-208">CreateNewTimePeriod</span></span>
-   <span data-ttu-id="f7c42-209">訂正</span><span class="sxs-lookup"><span data-stu-id="f7c42-209">Correction</span></span>
-   <span data-ttu-id="f7c42-210">EffectiveBased</span><span class="sxs-lookup"><span data-stu-id="f7c42-210">EffectiveBased</span></span>

<span data-ttu-id="f7c42-211">**有効日エンティティ:** 対照的に、データが有効日データ エンティティに挿入または更新されると、**validTimeStateUpdateMode** メソッドはエンティティ レベルで使用されません。</span><span class="sxs-lookup"><span data-stu-id="f7c42-211">**Date-effective entity:** By contrast, when data is inserted or updated in a date-effective data entity, the **validTimeStateUpdateMode** method isn't used at the entity level.</span></span> <span data-ttu-id="f7c42-212">書き込みについては、データ エンティティは、テーブル レベルに有効日プロセスを残します。</span><span class="sxs-lookup"><span data-stu-id="f7c42-212">For writes, the data entity leaves the date-effective processing to the table level.</span></span> <span data-ttu-id="f7c42-213">エンティティ データ ソース上で **有効時間状態の更新** プロパティを使用すると、データ エンティティの各データ ソースのために **validTimeStateUpdateMode** メソッドを使用することを指定することができます。</span><span class="sxs-lookup"><span data-stu-id="f7c42-213">You can use the **Valid Time State Update** property on the entity data source to specify the **validTimeStateUpdateMode** method to use for each data source of the data entity.</span></span>

## <a name="creating-a-date-effective-entity"></a><span data-ttu-id="f7c42-214">日付有効なエンティティを作成しています</span><span class="sxs-lookup"><span data-stu-id="f7c42-214">Creating a date-effective entity</span></span>
<span data-ttu-id="f7c42-215">このセクションでは、有効日のあるエンティティを作成する方法を示します。</span><span class="sxs-lookup"><span data-stu-id="f7c42-215">This section shows how to create a date-effective entity.</span></span>

#### <a name="create-a-new-project"></a><span data-ttu-id="f7c42-216">新しいプロジェクトの作成</span><span class="sxs-lookup"><span data-stu-id="f7c42-216">Create a new project</span></span>

1.  <span data-ttu-id="f7c42-217">**ファイル** &gt; **新規** &gt; **プロジェクト**とクリックし、新しいプロジェクトを作成します。</span><span class="sxs-lookup"><span data-stu-id="f7c42-217">Click **File** &gt; **New** &gt; **Project** to create a new project.</span></span>
2.  <span data-ttu-id="f7c42-218">ソリューション エクスプローラーで、プロジェクトを右クリックしてから**プロパティ**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="f7c42-218">In Solution Explorer, right-click your project, and then click **Properties**.</span></span> <span data-ttu-id="f7c42-219">プロジェクトの **プロパティ ページ** ダイアログ ボックスが開きます。</span><span class="sxs-lookup"><span data-stu-id="f7c42-219">The **Property Pages** dialog box for your project opens.</span></span>
3.  <span data-ttu-id="f7c42-220">**ビルドでのデータベースの同期**プロパティの値を **True** に変更し、**OK** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="f7c42-220">Change the value of the **Synchronize database on build** property to **True**, and then click **OK**.</span></span> <span data-ttu-id="f7c42-221">このプロパティはプロジェクトごとに 1 回のみ設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="f7c42-221">You must set this property only one time per project.</span></span> 

    <span data-ttu-id="f7c42-222">[![ビルド上にデータベースを同期 =True](./media/date3.png)](./media/date3.png)</span><span class="sxs-lookup"><span data-stu-id="f7c42-222">[![Synchronize database on build = True](./media/date3.png)](./media/date3.png)</span></span>

#### <a name="add-a-new-data-entity-to-your-project"></a><span data-ttu-id="f7c42-223">プロジェクトへの新しいデータ エンティティの追加</span><span class="sxs-lookup"><span data-stu-id="f7c42-223">Add a new data entity to your project</span></span>

<span data-ttu-id="f7c42-224">**FMVehicleRateEntity** という名前の新しいエンティティを作成し、プロジェクトに追加します。</span><span class="sxs-lookup"><span data-stu-id="f7c42-224">Create a new entity that is named **FMVehicleRateEntity**, and add it to the project.</span></span>

1.  <span data-ttu-id="f7c42-225">左ウィンドウで **Microsoft Dynamics 365 アーティファクト**を選択してから、メイン ウィンドウの左側にある**データ エンティティ**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="f7c42-225">In the left pane, select **Microsoft Dynamics 365 Artifacts**, and then click **Data Entity** in the left column of the main pane.</span></span>
2.  <span data-ttu-id="f7c42-226">**追加** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="f7c42-226">Click **Add**.</span></span> <span data-ttu-id="f7c42-227">**データ エンティティ ビュー** ウィザードが起動します。</span><span class="sxs-lookup"><span data-stu-id="f7c42-227">The **Data Entity View** wizard starts.</span></span>
3.  <span data-ttu-id="f7c42-228">次のスクリーン ショットに表示される作成するデータ エンティティのプロパティ値を指定します。</span><span class="sxs-lookup"><span data-stu-id="f7c42-228">Specify the property values for the data entity that you are creating, as shown in the following screen shot.</span></span> <span data-ttu-id="f7c42-229">最も重要なフィールドは、**FMVehicleRate** を選択する **プライマリ データ ソース** です。</span><span class="sxs-lookup"><span data-stu-id="f7c42-229">The most important field is **Primary data source**, where you select **FMVehicleRate**.</span></span> 

    <span data-ttu-id="f7c42-230">[![プライマリ データ ソース =FMVehicleRate](./media/date5.png)](./media/date5.png) **次へ**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="f7c42-230">[![Primary data source = FMVehicleRate](./media/date5.png)](./media/date5.png) Click **Next**.</span></span>

4.  <span data-ttu-id="f7c42-231">プライマリ データ ソース、**FMVehicleRate** からエンティティにフィールドを追加します。</span><span class="sxs-lookup"><span data-stu-id="f7c42-231">Add fields to the entity from the primary data source, **FMVehicleRate**.</span></span>
5.  <span data-ttu-id="f7c42-232">すべてのフィールドを選択し、**完了** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="f7c42-232">Select all fields, and then click **Finish**.</span></span> 

    <span data-ttu-id="f7c42-233">[![新たに追加されたフィールドをすべて選択する](./media/date6.png)](./media/date6.png)</span><span class="sxs-lookup"><span data-stu-id="f7c42-233">[![Selecting all the newly added fields](./media/date6.png)](./media/date6.png)</span></span> 
    
    <span data-ttu-id="f7c42-234">項目がソリューション エクスプローラーのプロジェクトに追加されます。</span><span class="sxs-lookup"><span data-stu-id="f7c42-234">The items are added to the project in Solution Explorer.</span></span> 
    
    <span data-ttu-id="f7c42-235">[![ソリューション エクスプローラー内のプロジェクト](./media/date7.png)](./media/date7.png)</span><span class="sxs-lookup"><span data-stu-id="f7c42-235">[![The project in Solution Explorer](./media/date7.png)](./media/date7.png)</span></span>

#### <a name="build-your-project"></a><span data-ttu-id="f7c42-236">プロジェクトの構築</span><span class="sxs-lookup"><span data-stu-id="f7c42-236">Build your project</span></span>

1.  <span data-ttu-id="f7c42-237">**ビルド** &gt; **ソリューションのビルド**とクリックし、プロジェクトを構築します。</span><span class="sxs-lookup"><span data-stu-id="f7c42-237">Click **Build** &gt; **Build Solution** to build your project.</span></span>
2.  <span data-ttu-id="f7c42-238">ビルドにエラーが含まれていないことを確認します。</span><span class="sxs-lookup"><span data-stu-id="f7c42-238">Verify that the build has no errors.</span></span> <span data-ttu-id="f7c42-239">プロセスのこの段階では、警告を容認する必要があります。</span><span class="sxs-lookup"><span data-stu-id="f7c42-239">Warnings should be tolerated at this stage in the process.</span></span>

#### <a name="validate-the-property-values"></a><span data-ttu-id="f7c42-240">プロパティ値の検証</span><span class="sxs-lookup"><span data-stu-id="f7c42-240">Validate the property values</span></span>

-   <span data-ttu-id="f7c42-241">ソリューション エクスプローラーで、**FMVehicleRateEntity** ノードを選択し、**FMVehicleRateEntity** エンティティのプロパティを**プロパティ** ウィンドウの値と比較して確認します。</span><span class="sxs-lookup"><span data-stu-id="f7c42-241">In Solution Explorer, select the **FMVehicleRateEntity** node, and validate the properties of the **FMVehicleRateEntity** entity by comparing them to the values in the **Properties** pane.</span></span> 

    <span data-ttu-id="f7c42-242">[![プロパティ ウィンドウの値](./media/date8.png)](./media/date8.png)</span><span class="sxs-lookup"><span data-stu-id="f7c42-242">[![Values in the Properties pane](./media/date8.png)](./media/date8.png)</span></span>

#### <a name="make-your-entity-date-effective"></a><span data-ttu-id="f7c42-243">エンティティの日付を有効にする</span><span class="sxs-lookup"><span data-stu-id="f7c42-243">Make your entity date effective</span></span>

1.  <span data-ttu-id="f7c42-244">ソリューション エクスプローラーで、**FMVehicleRateEntity** ノードを右クリックしてから**開く**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="f7c42-244">In Solution Explorer, right-click the **FMVehicleRateEntity** node, and then click **Open**.</span></span> <span data-ttu-id="f7c42-245">エンティティのデザイナーが中央のウィンドウに開きます。</span><span class="sxs-lookup"><span data-stu-id="f7c42-245">The designer for the entity opens in the middle pane.</span></span> 

    <span data-ttu-id="f7c42-246">[![FMVehicleRateEntity エンティティのデザイナー](./media/date9.png)](./media/date9.png)</span><span class="sxs-lookup"><span data-stu-id="f7c42-246">[![Designer for the FMVehicleRateEntity entity](./media/date9.png)](./media/date9.png)</span></span>

2.  <span data-ttu-id="f7c42-247">**時間状態が有効であるかどうかを検証する**プロパティの値を**はい**に変更します。</span><span class="sxs-lookup"><span data-stu-id="f7c42-247">Change the value of the **Validate Time State Enabled** property to **Yes**.</span></span> 

    <span data-ttu-id="f7c42-248">[![時間状態が有効であるかどうかを検証する = はい](./media/date10.png)](./media/date10.png)</span><span class="sxs-lookup"><span data-stu-id="f7c42-248">[![Validate Time State Enabled = Yes](./media/date10.png)](./media/date10.png)</span></span>

#### <a name="configure-the-valid-time-state-update-property-for-the-date-effective-data-source"></a><span data-ttu-id="f7c42-249">有効日データソースの有効時間状態の更新プロパティのコンフィギュレーション</span><span class="sxs-lookup"><span data-stu-id="f7c42-249">Configure the Valid Time State Update property for the date-effective data source</span></span>

-   <span data-ttu-id="f7c42-250">**FMVehicleRate** データ ソースを選択し、**有効時間状態の更新** プロパティを **CreateNewTimePeriod** に設定します。</span><span class="sxs-lookup"><span data-stu-id="f7c42-250">Select the **FMVehicleRate** data source, and then set the **Valid Time State Update** property to **CreateNewTimePeriod**.</span></span> 

    <span data-ttu-id="f7c42-251">[![有効時間状態の更新 = CreateNewTimePeriod](./media/date11.png)](./media/date11.png)</span><span class="sxs-lookup"><span data-stu-id="f7c42-251">[![Valid Time State Update = CreateNewTimePeriod](./media/date11.png)](./media/date11.png)</span></span>

#### <a name="test-your-project"></a><span data-ttu-id="f7c42-252">プロジェクトをテスト</span><span class="sxs-lookup"><span data-stu-id="f7c42-252">Test your project</span></span>

-   <span data-ttu-id="f7c42-253">プロジェクトを再度構築し、次の X++ コードを実行してプロジェクトをテストします。</span><span class="sxs-lookup"><span data-stu-id="f7c42-253">Build your project again, and run the following X++ code to test your project.</span></span>

```xml
/// <summary>
    /// Runs the class with the specified arguments.
    /// </summary>
    /// <param name = "_args">The specified arguments.</param>
    public static void main(Args _args)
    {
        FMVehicleRateEntity FMVehicleRateEntity;
        FMCarClass          vehicle;
        FMVehicleModel      model;
        FMVehicleRate       vehicleRateTable;
        TransDate           d1=1\1\1999,d2=31\12\2014;

        ttsbegin;

        select count(RecId) from FMVehicleRateEntity;
        info(strfmt("Entity - Valid today before insert %1",FMVehicleRateEntity.RecId));

        select count(RecId) from vehicleRateTable;
        info(strfmt("Table - Valid today before insert %1",vehicleRateTable.RecId));

        select firstonly model;

        vehicle.VehicleModel = model.RecId;
        vehicle.VehicleId = "TestV1001";
        vehicle.insert();

            if (vehicle)
            {
                FMVehicleRateEntity.clear();
                FMVehicleRateEntity.FMVehicle_VehicleId = vehicle.VehicleId;
                FMVehicleRateEntity.ValidFrom = d1;
                FMVehicleRateEntity.ValidTo = d2;
                FMVehicleRateEntity.RatePerDay = 100;
                FMVehicleRateEntity.RatePerWeek = 600;
                FMVehicleRateEntity.insert();

                // Should increase by one as compared to before insert numbers
                select count(RecId) from FMVehicleRateEntity;
                info(strfmt("Entity - Valid today after insert %1",FMVehicleRateEntity.RecId));

                // Should increase by one as compared to before insert numbers
                select count(RecId) from vehicleRateTable;
                info(strfmt("Table - Valid today after insert %1",vehicleRateTable.RecId));

                // New record should show in count
                select validtimestate(d1) count(RecId) from FMVehicleRateEntity;
                info(strfmt("Entity - Valid 1999 %1",FMVehicleRateEntity.RecId));

                // New record should show in count
                select validtimestate(d1) count(RecId) from vehicleRateTable;
                info(strfmt("Table - Valid 1999 %1",vehicleRateTable.RecId));

                // update newly created record
                // This should split record into two - 2009 to Today, today to 2014
                // Split happens because of mode in saveEntityDatasource
                select forupdate validtimestate(d1,d2) FMVehicleRateEntity 
                     where FMVehicleRateEntity.FMVehicle_VehicleId == vehicle.VehicleId &&
                           FMVehicleRateEntity.ValidFrom == d1 &&
                           FMVehicleRateEntity.ValidTo == d2;
                FMVehicleRateEntity.RatePerDay = 200;
                FMVehicleRateEntity.update();

                // validate the split
                while select validtimestate(d1,d2) FMVehicleRateEntity
                     where FMVehicleRateEntity.FMVehicle_VehicleId == vehicle.VehicleId
                {
                    info(strfmt("Entity - %1 to %2 , RatePerDay-%3, RatePerWeek-%4",
                            FMVehicleRateEntity.ValidFrom,
                            FMVehicleRateEntity.ValidTo,
                            FMVehicleRateEntity.RatePerDay,
                            FMVehicleRateEntity.RatePerWeek));
                }
                ttsabort;
            }
        }

```



