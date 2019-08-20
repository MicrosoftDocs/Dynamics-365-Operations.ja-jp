---
title: 個人検索レポートを拡張
description: このトピックでは、Microsoft Dynamics 365 for Finance and Operations の担当者検索レポートを拡張するためのプロセスを説明します。
author: rschloma
manager: AnnBe
ms.date: 01/24/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: IT Pro
ms.reviewer: rhaertle
ms.search.scope: Operations
ms.search.region: Global
ms.author: rschloma
ms.search.validFrom: 2017-12-31
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 1999c276bd777ff0e93966674550de54a1678987
ms.sourcegitcommit: 27a98a7a0f1d2623f5236a88066f483def30889c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/01/2019
ms.locfileid: "1833316"
---
# <a name="extend-the-person-search-report"></a><span data-ttu-id="060c4-103">個人検索レポートの拡張</span><span class="sxs-lookup"><span data-stu-id="060c4-103">Extend the Person search report</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="060c4-104">Microsoft Dynamics 365 for Finance and Operations の担当者検索レポートは、1 人のエンティティのコレクションを管理するように設計されたインテリジェント検索プロセッサによってサポートされています。</span><span class="sxs-lookup"><span data-stu-id="060c4-104">The Person search report for Microsoft Dynamics 365 for Finance and Operations is backed by an intelligent search processor that is designed to manage a collection of entities for a single person.</span></span> <span data-ttu-id="060c4-105">担当者検索レポートは、Finance and Operations のデータを検索し、生成される識別子のセットを作成します。</span><span class="sxs-lookup"><span data-stu-id="060c4-105">The Person search report searches Finance and Operations data and creates a set of resulting identifiers.</span></span> <span data-ttu-id="060c4-106">それぞれの結果は、検索カテゴリ (たとえば、顧客) および関連するテーブルの結果レコードを参照します。</span><span class="sxs-lookup"><span data-stu-id="060c4-106">Each result references a search category (for example, Customer) and a result record in a related table.</span></span> <span data-ttu-id="060c4-107">個人検索レポートの使用の詳細については、[個人検索レポート](gdpr-person-search-report.md) トピックを参照してください。</span><span class="sxs-lookup"><span data-stu-id="060c4-107">For information about using the Person search report, refer the [Person search report](gdpr-person-search-report.md) topic.</span></span>

> [!NOTE]
> <span data-ttu-id="060c4-108">担当者検索レポートは、Finance and Operations、Microsoft Dynamics 365 for Retail、およびMicrosoft Dynamics 365 for Talent の今後のリリースで利用できるようになります。</span><span class="sxs-lookup"><span data-stu-id="060c4-108">The Person search report will be available in an upconming release for Finance and Operations, Microsoft Dynamics 365 for Retail, and Microsoft Dynamics 365 for Talent.</span></span> <span data-ttu-id="060c4-109">このトピックの Finance and Operations への参照は、Retail と Talent にも当てはまります。</span><span class="sxs-lookup"><span data-stu-id="060c4-109">References to Finance and Operations in this topic also apply to Retail and Talent.</span></span> <span data-ttu-id="060c4-110">Microsoft Dynamics AX 2012 では今のところ担当者検索レポートは使用できません。</span><span class="sxs-lookup"><span data-stu-id="060c4-110">The Person search report is not currently available for Microsoft Dynamics AX 2012.</span></span>

## <a name="add-another-entity-to-the-default-template"></a><span data-ttu-id="060c4-111">既定のテンプレートへの別のエンティティの追加</span><span class="sxs-lookup"><span data-stu-id="060c4-111">Add another entity to the default template</span></span>

<span data-ttu-id="060c4-112">任意のエンティティを既定の個人検索レポート テンプレートに追加することができます。</span><span class="sxs-lookup"><span data-stu-id="060c4-112">You can add any entity to the default Person search report template.</span></span> <span data-ttu-id="060c4-113">**データ管理**ワークスペースを開いて、**テンプレート**を選択します。</span><span class="sxs-lookup"><span data-stu-id="060c4-113">Open the **Data management** workspace, and select **Templates**.</span></span> <span data-ttu-id="060c4-114">テンプレートにエンティティを追加します。</span><span class="sxs-lookup"><span data-stu-id="060c4-114">Add the entity to the template.</span></span> <span data-ttu-id="060c4-115">追加するエンティティには、個人検索レポートをフィルター処理するために使用されるフィールドの少なくとも 1 つが含まれている必要があります。</span><span class="sxs-lookup"><span data-stu-id="060c4-115">The entity that you add must include at least one of the fields that are used to filter the Person search report.</span></span> 

## <a name="create-a-new-search-category"></a><span data-ttu-id="060c4-116">新しい検索カテゴリを作成する</span><span class="sxs-lookup"><span data-stu-id="060c4-116">Create a new search category</span></span>

1. <span data-ttu-id="060c4-117">**PersonSearchResultCategory** 列挙型を使用して、作業者と申請者のような異なるカテゴリの結果を区別します。</span><span class="sxs-lookup"><span data-stu-id="060c4-117">Use the **PersonSearchResultCategory** enumeration to distinguish different categories of results, such as workers versus applicants.</span></span>
2. <span data-ttu-id="060c4-118">新しい結果タイプを作成するには、必要に応じて**PersonSearchResultCategory** 列挙型を拡張します。</span><span class="sxs-lookup"><span data-stu-id="060c4-118">Extend the **PersonSearchResultCategory** enumeration as needed to create new result types.</span></span>

## <a name="create-search-processing-for-the-new-search-category"></a><span data-ttu-id="060c4-119">新しい検索カテゴリの検索処理を作成する</span><span class="sxs-lookup"><span data-stu-id="060c4-119">Create search processing for the new search category</span></span>

<span data-ttu-id="060c4-120">この例では、新しいプロセッサ クラスを作成します。</span><span class="sxs-lookup"><span data-stu-id="060c4-120">In this example, you will create a new processor class.</span></span>

1. <span data-ttu-id="060c4-121">新しい検索区分で **PersonSearchModule** 列挙型を拡張します。</span><span class="sxs-lookup"><span data-stu-id="060c4-121">Extend the **PersonSearchModule** enumeration with a new search area.</span></span>
2. <span data-ttu-id="060c4-122">**PersonSearchProcessor** クラスを拡張し、新しい個人検索モジュール領域をパラメータとして **PersonSearchProcessorFactoryAttribute** 属性を含むクラスを作成します。</span><span class="sxs-lookup"><span data-stu-id="060c4-122">Create a class that extends the **PersonSearchProcessor** class and includes the **PersonSearchProcessorFactoryAttribute** attribute, with the new person search module area as a parameter.</span></span> 
3. <span data-ttu-id="060c4-123">**PersonSearchProcessor** 拡張クラスで、目的の検索ロジックで **doSearch** メソッドをオーバーライドします。</span><span class="sxs-lookup"><span data-stu-id="060c4-123">In the **PersonSearchProcessor** extended class, override the **doSearch** method with your desired search logic.</span></span> <span data-ttu-id="060c4-124">次の例のように、新しいテーブル関係を作成するために **PersonSearchResult** テーブルを拡張します。</span><span class="sxs-lookup"><span data-stu-id="060c4-124">As shown in the following example, extend the **PersonSearchResult** table to create new table relationships.</span></span>

    ```
    PersonSearchResultCategory::Customer needs a relation:PersonSearchResult.ResultRecId = CustTable.RecId,PersonSearchResult.ResultTableId = CustTable.TableId
    ```

## <a name="integrate-with-the-global-address-book-optional"></a><span data-ttu-id="060c4-125">グローバル アドレス帳と統合 (オプション)</span><span class="sxs-lookup"><span data-stu-id="060c4-125">Integrate with the Global address book (Optional)</span></span>

<span data-ttu-id="060c4-126">グローバル アドレス帳と統合する場合は、検出されたパーティー番号を **PersonSearchPartyNumberTmp** テーブルに挿入します。</span><span class="sxs-lookup"><span data-stu-id="060c4-126">If you want to integrate with the Global address book, insert any discovered party numbers into the **PersonSearchPartyNumberTmp** table.</span></span> <span data-ttu-id="060c4-127">**PersonSearchProcessor** の **findPartyLink** メソッドは、当事者番号を、ユーザー、顧客、仕入先などの他の検索コンポーネントにリンクします。</span><span class="sxs-lookup"><span data-stu-id="060c4-127">The **findPartyLink** method of **PersonSearchProcessor** tries to link party numbers to other search artifacts, such as users, customers, or vendors.</span></span>

<span data-ttu-id="060c4-128">このメソッドにはデリゲート **onFindPartyLink** があり、当事者番号に基づいて検索する追加のコンポーネントを指定できます。</span><span class="sxs-lookup"><span data-stu-id="060c4-128">This method has a delegate, **onFindPartyLink**, that lets you specify additional artifacts to search, based on the party numbers.</span></span>

<span data-ttu-id="060c4-129">**PersonSearchCriteria** テーブルでは、エンド ユーザーが、システムで個人データの検索に使用するパラメーターを指定できます。</span><span class="sxs-lookup"><span data-stu-id="060c4-129">The **PersonSearchCriteria** tables let end users specify the parameters by which to search the system for personal data.</span></span>

## <a name="create-new-search-criteria"></a><span data-ttu-id="060c4-130">新しい検索基準を作成する</span><span class="sxs-lookup"><span data-stu-id="060c4-130">Create new search criteria</span></span>

<span data-ttu-id="060c4-131">新しい検索条件を必要である場合は、これらの手順に従います。</span><span class="sxs-lookup"><span data-stu-id="060c4-131">If you need new search criteria, follow these steps.</span></span>

1. <span data-ttu-id="060c4-132">**PersonSearchCriteriaName**、**PersonSearchCriteriaAddress**、および **PersonSearchCriteriaKnownId** を拡張または独自のテーブルを作成します。</span><span class="sxs-lookup"><span data-stu-id="060c4-132">Extend the **PersonSearchCriteriaName**, **PersonSearchCriteriaAddress**, and **PersonSearchCriteriaKnownId** tables, or create your own tables.</span></span>
2. <span data-ttu-id="060c4-133">新しいデータ フィールドを表示するには、**PersonSearchDialog** フォームを拡張します。</span><span class="sxs-lookup"><span data-stu-id="060c4-133">Extend the **PersonSearchDialog** form to show these new data fields.</span></span>
3. <span data-ttu-id="060c4-134">検索処理中に新しい条件を使用します。</span><span class="sxs-lookup"><span data-stu-id="060c4-134">Use the new criteria during search processing.</span></span>

<span data-ttu-id="060c4-135">**PersonSearch** フォームには、担当者の検索によって検出された結果のセットが表示されます。</span><span class="sxs-lookup"><span data-stu-id="060c4-135">The **PersonSearch** form shows the set of results that was discovered by a person search.</span></span>

## <a name="show-the-new-search-category-in-the-personsearch-form"></a><span data-ttu-id="060c4-136">PersonSearch 形式で新しい検索カテゴリを表示</span><span class="sxs-lookup"><span data-stu-id="060c4-136">Show the new search category in the PersonSearch form</span></span>

1. <span data-ttu-id="060c4-137">**PersonSearchResult** テーブルの新しいビューを作成します。</span><span class="sxs-lookup"><span data-stu-id="060c4-137">Create a new view on the **PersonSearchResult** table.</span></span> <span data-ttu-id="060c4-138">このビューは結果を新しい **PersonSearchResultCategory** に限定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="060c4-138">This view should restrict results to only your new **PersonSearchResultCategory**.</span></span>
2. <span data-ttu-id="060c4-139">ビューを結果レコードに結合させ、必要なフィールドのビューを作成します (たとえば、**PersonSearchResultCustomerView**)。</span><span class="sxs-lookup"><span data-stu-id="060c4-139">Join the view to your result record, and create the view fields that are needed (for example, **PersonSearchResultCustomerView**).</span></span>
3. <span data-ttu-id="060c4-140">新しいリレーションシップを新しいビューに作成するには、**PersonSearchResult** テーブルを拡張します。</span><span class="sxs-lookup"><span data-stu-id="060c4-140">Extend the **PersonSearchResult** table to create a new relationship to the new view.</span></span> <span data-ttu-id="060c4-141">このリレーションシップは、人物の検索 ID に結合する必要があります。</span><span class="sxs-lookup"><span data-stu-id="060c4-141">This relationship should join on the person search ID.</span></span>
4. <span data-ttu-id="060c4-142">**PersonSearch** フォームを拡張します。</span><span class="sxs-lookup"><span data-stu-id="060c4-142">Extend the **PersonSearch** form:</span></span>

    1. <span data-ttu-id="060c4-143">データ ソースとして新しいビューを追加します。</span><span class="sxs-lookup"><span data-stu-id="060c4-143">Add the new view as a data source.</span></span>
    2. <span data-ttu-id="060c4-144">結果のグリッドと**含む/除外**ボタンを使用して結果に新しいタブを追加します。</span><span class="sxs-lookup"><span data-stu-id="060c4-144">Add a new tab to the results with the result grid and the **Include/Exclude** buttons.</span></span>
    3. <span data-ttu-id="060c4-145">**含む/除外**ボタンのイベント ハンドラーを作成して **PersonSearchResult** レコードを更新します。</span><span class="sxs-lookup"><span data-stu-id="060c4-145">Create event handlers for the **Include/Exclude** buttons to update the **PersonSearchResult** records.</span></span>

        <span data-ttu-id="060c4-146">**PersonSearchEventHandler::updateMarkedOnButtonClicked()** メソッドが利便性のために用意されています。</span><span class="sxs-lookup"><span data-stu-id="060c4-146">The **PersonSearchEventHandler::updateMarkedOnButtonClicked()** method is provided for convenience.</span></span>

> [!NOTE]
> <span data-ttu-id="060c4-147">結果キャプションのレコード数を確認するには、**OnQueryExecuted** ビューのデータ ソース イベントでイベント ハンドラーを作成します。</span><span class="sxs-lookup"><span data-stu-id="060c4-147">If you want to see the record count in the result caption, create an event handler on the **OnQueryExecuted** view data source event.</span></span> <span data-ttu-id="060c4-148">次に、**PersonSearch** フォームで **setResultCountOnGridCaption()** メソッドを呼び出して、カウントを更新します。</span><span class="sxs-lookup"><span data-stu-id="060c4-148">Next, call the **setResultCountOnGridCaption()** method on the **PersonSearch** form to update the count.</span></span>

<span data-ttu-id="060c4-149">各 **PersonSearchEntityFilterRelation** レコードは、フィルターを適用する場合、条件、フィルター テーブルおよび適用するフィールドを指定します。</span><span class="sxs-lookup"><span data-stu-id="060c4-149">Each **PersonSearchEntityFilterRelation** record specifies the conditions when a filter should apply, and the filter table and field to apply.</span></span>

<span data-ttu-id="060c4-150">フィルター関係のセットは、パッケージの構築時にテンプレート メタデータと比較されます。</span><span class="sxs-lookup"><span data-stu-id="060c4-150">The set of filter relations is compared to the template metadata when the package is built.</span></span>

<span data-ttu-id="060c4-151">フィルターを作成するためには、**PersonSearchResult** レコードと一致するフィルター カテゴリが存在する必要があります。</span><span class="sxs-lookup"><span data-stu-id="060c4-151">For a filter to be created, a **PersonSearchResult** record with the matching filter category must exist.</span></span> <span data-ttu-id="060c4-152">見つかったら、**PersonSearchResult** は、フィルター値が置かれているテーブル フィールドを参照します。</span><span class="sxs-lookup"><span data-stu-id="060c4-152">After it's found, the **PersonSearchResult** references the table field where the filter value resides.</span></span>

## <a name="create-new-filters"></a><span data-ttu-id="060c4-153">新しいフィルタを作成する</span><span class="sxs-lookup"><span data-stu-id="060c4-153">Create new filters</span></span>

1. <span data-ttu-id="060c4-154">**PersonSearchEntityFilterRelation** テーブルを拡張するには、Chain of Command (COC) を使用します。</span><span class="sxs-lookup"><span data-stu-id="060c4-154">Use the Chain of Command to extend the **PersonSearchEntityFilterRelation** table.</span></span>
2. <span data-ttu-id="060c4-155">新しいフィルターのタイプとソースを決定する:</span><span class="sxs-lookup"><span data-stu-id="060c4-155">Decide on the type and source of the new filter:</span></span>

    1. <span data-ttu-id="060c4-156">フィルターが拡張データ型 (EDT) または列挙の場合は、**MetadataTypeId** をデータ型の ID に設定します。</span><span class="sxs-lookup"><span data-stu-id="060c4-156">If the filter is an extended data type (EDT) or enumeration, set the **MetadataTypeId** to the data type ID.</span></span>
    2. <span data-ttu-id="060c4-157">フィルターがソース テーブルのフィールドである場合は、ソース テーブルとソース フィールド ID を指定します。</span><span class="sxs-lookup"><span data-stu-id="060c4-157">If the filter is a source table field, specify the source table and source field IDs.</span></span>
    3. <span data-ttu-id="060c4-158">フィルターがエンティティ フィールドである場合は、エンティティ フィールド ID を指定します。</span><span class="sxs-lookup"><span data-stu-id="060c4-158">If the filter is an entity field, specify the entity field ID.</span></span>

3. <span data-ttu-id="060c4-159">フィルター テーブルとフィルター フィールドを決定します。</span><span class="sxs-lookup"><span data-stu-id="060c4-159">Decide on the filter table and filter field.</span></span>

    <span data-ttu-id="060c4-160">フィルター テーブルは、一致するカテゴリを使用した **PersonSearchResult** として使用可能でなければなりません。</span><span class="sxs-lookup"><span data-stu-id="060c4-160">The filter table must be available as a **PersonSearchResult** with a matching category.</span></span> <span data-ttu-id="060c4-161">それ以外の場合、フィルターは作成されません。</span><span class="sxs-lookup"><span data-stu-id="060c4-161">Otherwise, no filters will be created.</span></span>

4. <span data-ttu-id="060c4-162">新しいフィルター レコードを挿入します。</span><span class="sxs-lookup"><span data-stu-id="060c4-162">Insert the new filter record.</span></span>

    <span data-ttu-id="060c4-163">個人検索フレームワークが、最初にフォームが開いたときに、すべての除外の初期化を自動的に管理します。</span><span class="sxs-lookup"><span data-stu-id="060c4-163">The person search framework will automatically manage initialization of all exclusions when the form is first opened.</span></span> <span data-ttu-id="060c4-164">除外を使用すると、特定のエンティティ フィールドのフィルター構築機能を抑制できます。</span><span class="sxs-lookup"><span data-stu-id="060c4-164">Exclusions let you suppress the filter building functionality for specific entity fields.</span></span>

## <a name="create-new-exclusions"></a><span data-ttu-id="060c4-165">新しい除外を作成する</span><span class="sxs-lookup"><span data-stu-id="060c4-165">Create new exclusions</span></span>

1. <span data-ttu-id="060c4-166">**PersonSearchEntityExclusion** テーブルを拡張するには、Chain of Command (COC) を使用します。</span><span class="sxs-lookup"><span data-stu-id="060c4-166">Use the Chain of Command (COC) to extend the **PersonSearchEntityExclusion** table.</span></span>
2. <span data-ttu-id="060c4-167">**CoC メソッド**で、エンティティ、エンティティ フィールド、除外が有効かどうかを指定します。</span><span class="sxs-lookup"><span data-stu-id="060c4-167">In the **CoC method**, specify the entity, the entity field, and whether the exclusion is active.</span></span>
3. <span data-ttu-id="060c4-168">新しい除外レコードを挿入します。</span><span class="sxs-lookup"><span data-stu-id="060c4-168">Insert the new exclusion record.</span></span>

    <span data-ttu-id="060c4-169">個人検索フレームワークが、最初にフォームが開いたときに、すべての除外の初期化を自動的に管理します。</span><span class="sxs-lookup"><span data-stu-id="060c4-169">The person search framework will automatically manage initialization of all exclusions when the form is first opened.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="060c4-170">その他のリソース</span><span class="sxs-lookup"><span data-stu-id="060c4-170">Additional resources</span></span>

<span data-ttu-id="060c4-171">欧州連合の一般的なデータ保護規制 (GDPR) に基づくデータの依頼への応答の一部として、個人検索レポートを拡張している場合、この規制に関する詳細については、[Microsoft Dynamics 365 for Finance and Operations のための GDPR ガイド](./gdpr-guide.md) でご覧いただけます。</span><span class="sxs-lookup"><span data-stu-id="060c4-171">If you're extending the Person search report as part of a response to a request for data under the General Data Protection Regulation (GDPR) in the European Union, more information about that regulation is available in the [Guide to the GDPR for Microsoft Dynamics 365 for Finance and Operations](./gdpr-guide.md).</span></span>

<span data-ttu-id="060c4-172">GDPR の詳細については、[欧州連合の Web サイト](https://europa.eu/) および [Microsoft Trust Center](https://www.microsoft.com/TrustCenter/Privacy/gdpr/default.aspx) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="060c4-172">You can learn more about the GDPR on the [European Union's website](https://europa.eu/) and on the [Microsoft Trust Center](https://www.microsoft.com/TrustCenter/Privacy/gdpr/default.aspx).</span></span>


### <a name="disclaimer"></a><span data-ttu-id="060c4-173">免責事項</span><span class="sxs-lookup"><span data-stu-id="060c4-173">Disclaimer</span></span>
<span data-ttu-id="060c4-174">(c)2018 Microsoft Corporation.</span><span class="sxs-lookup"><span data-stu-id="060c4-174">(c)2018 Microsoft Corporation.</span></span> <span data-ttu-id="060c4-175">All rights reserved.</span><span class="sxs-lookup"><span data-stu-id="060c4-175">All rights reserved.</span></span> <span data-ttu-id="060c4-176">このドキュメントは、"現状のまま" 提供されます。</span><span class="sxs-lookup"><span data-stu-id="060c4-176">This document is provided "as-is."</span></span> <span data-ttu-id="060c4-177">URL およびその他のインターネット Web サイトの参照を含む、このドキュメントの情報および見解は、予告なしに変更することがあります。</span><span class="sxs-lookup"><span data-stu-id="060c4-177">Information and views expressed in this document, including URL and other Internet Web site references, may change without notice.</span></span> <span data-ttu-id="060c4-178">このドキュメントの使用上のリスクは、すべてユーザーが負うものとします。</span><span class="sxs-lookup"><span data-stu-id="060c4-178">You bear the risk of using it.</span></span> <span data-ttu-id="060c4-179">このドキュメントは、Microsoft の製品に含まれる知的財産に対する法律上の権利をお客様に付与するものではありません。</span><span class="sxs-lookup"><span data-stu-id="060c4-179">This document does not provide you with any legal rights to any intellectual property in any Microsoft product.</span></span> <span data-ttu-id="060c4-180">内部での参照を目的とする場合、このドキュメントをコピーして使用できます。</span><span class="sxs-lookup"><span data-stu-id="060c4-180">You may copy and use this document for your internal, reference purposes.</span></span> 
