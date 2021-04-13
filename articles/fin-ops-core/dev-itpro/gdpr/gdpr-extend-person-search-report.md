---
title: 個人検索レポートを拡張
description: このトピックでは、Finance and Operations の担当者検索レポートを拡張するためのプロセスを説明します。
author: rschloma
ms.date: 01/24/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: IT Pro
ms.reviewer: rhaertle
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2017-12-31
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: cadbac9d876b37b32e8ddb4768dfdcf8f685e245
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/31/2021
ms.locfileid: "5750930"
---
# <a name="extend-the-person-search-report"></a><span data-ttu-id="7418b-103">個人検索レポートの拡張</span><span class="sxs-lookup"><span data-stu-id="7418b-103">Extend the Person search report</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="7418b-104">Finance and Operations アプリの担当者検索レポートは、1 人のエンティティのコレクションを管理するように設計されたインテリジェント検索プロセッサによってサポートされています。</span><span class="sxs-lookup"><span data-stu-id="7418b-104">The Person search report for Finance and Operations apps is backed by an intelligent search processor that is designed to manage a collection of entities for a single person.</span></span> <span data-ttu-id="7418b-105">担当者検索レポートは、Finance and Operations のデータを検索し、生成される識別子のセットを作成します。</span><span class="sxs-lookup"><span data-stu-id="7418b-105">The Person search report searches Finance and Operations data and creates a set of resulting identifiers.</span></span> <span data-ttu-id="7418b-106">それぞれの結果は、検索カテゴリ (たとえば、顧客) および関連するテーブルの結果レコードを参照します。</span><span class="sxs-lookup"><span data-stu-id="7418b-106">Each result references a search category (for example, Customer) and a result record in a related table.</span></span> <span data-ttu-id="7418b-107">個人検索レポートの使用の詳細については、[個人検索レポート](gdpr-person-search-report.md) トピックを参照してください。</span><span class="sxs-lookup"><span data-stu-id="7418b-107">For information about using the Person search report, refer the [Person search report](gdpr-person-search-report.md) topic.</span></span>

> [!NOTE]
> <span data-ttu-id="7418b-108">個人検索は、Dynamics 365 Finance、Supply Chain Management、コマース、および人事管理に対して使用できます。</span><span class="sxs-lookup"><span data-stu-id="7418b-108">The Person search is available for Dynamics 365 Finance, Supply Chain Management, Commerce, and Human Resources.</span></span> <span data-ttu-id="7418b-109">Microsoft Dynamics AX 2012 では今のところ担当者検索レポートは使用できません。</span><span class="sxs-lookup"><span data-stu-id="7418b-109">The Person search report is not currently available for Microsoft Dynamics AX 2012.</span></span>

## <a name="add-another-entity-to-the-default-template"></a><span data-ttu-id="7418b-110">既定のテンプレートへの別のエンティティの追加</span><span class="sxs-lookup"><span data-stu-id="7418b-110">Add another entity to the default template</span></span>

<span data-ttu-id="7418b-111">任意のエンティティを既定の個人検索レポート テンプレートに追加することができます。</span><span class="sxs-lookup"><span data-stu-id="7418b-111">You can add any entity to the default Person search report template.</span></span> <span data-ttu-id="7418b-112">**データ管理** ワークスペースを開いて、**テンプレート** を選択します。</span><span class="sxs-lookup"><span data-stu-id="7418b-112">Open the **Data management** workspace, and select **Templates**.</span></span> <span data-ttu-id="7418b-113">テンプレートにエンティティを追加します。</span><span class="sxs-lookup"><span data-stu-id="7418b-113">Add the entity to the template.</span></span> <span data-ttu-id="7418b-114">追加するエンティティには、個人検索レポートをフィルター処理するために使用されるフィールドの少なくとも 1 つが含まれている必要があります。</span><span class="sxs-lookup"><span data-stu-id="7418b-114">The entity that you add must include at least one of the fields that are used to filter the Person search report.</span></span> 

## <a name="create-a-new-search-category"></a><span data-ttu-id="7418b-115">新しい検索カテゴリを作成する</span><span class="sxs-lookup"><span data-stu-id="7418b-115">Create a new search category</span></span>

1. <span data-ttu-id="7418b-116">**PersonSearchResultCategory** 列挙型を使用して、作業者と申請者のような異なるカテゴリの結果を区別します。</span><span class="sxs-lookup"><span data-stu-id="7418b-116">Use the **PersonSearchResultCategory** enumeration to distinguish different categories of results, such as workers versus applicants.</span></span>
2. <span data-ttu-id="7418b-117">新しい結果タイプを作成するには、必要に応じて **PersonSearchResultCategory** 列挙型を拡張します。</span><span class="sxs-lookup"><span data-stu-id="7418b-117">Extend the **PersonSearchResultCategory** enumeration as needed to create new result types.</span></span>

## <a name="create-search-processing-for-the-new-search-category"></a><span data-ttu-id="7418b-118">新しい検索カテゴリの検索処理を作成する</span><span class="sxs-lookup"><span data-stu-id="7418b-118">Create search processing for the new search category</span></span>

<span data-ttu-id="7418b-119">この例では、新しいプロセッサ クラスを作成します。</span><span class="sxs-lookup"><span data-stu-id="7418b-119">In this example, you will create a new processor class.</span></span>

1. <span data-ttu-id="7418b-120">新しい検索区分で **PersonSearchModule** 列挙型を拡張します。</span><span class="sxs-lookup"><span data-stu-id="7418b-120">Extend the **PersonSearchModule** enumeration with a new search area.</span></span>
2. <span data-ttu-id="7418b-121">**PersonSearchProcessor** クラスを拡張し、新しい個人検索モジュール領域をパラメータとして **PersonSearchProcessorFactoryAttribute** 属性を含むクラスを作成します。</span><span class="sxs-lookup"><span data-stu-id="7418b-121">Create a class that extends the **PersonSearchProcessor** class and includes the **PersonSearchProcessorFactoryAttribute** attribute, with the new person search module area as a parameter.</span></span> 
3. <span data-ttu-id="7418b-122">**PersonSearchProcessor** 拡張クラスで、目的の検索ロジックで **doSearch** メソッドをオーバーライドします。</span><span class="sxs-lookup"><span data-stu-id="7418b-122">In the **PersonSearchProcessor** extended class, override the **doSearch** method with your desired search logic.</span></span> <span data-ttu-id="7418b-123">次の例のように、新しいテーブル関係を作成するために **PersonSearchResult** テーブルを拡張します。</span><span class="sxs-lookup"><span data-stu-id="7418b-123">As shown in the following example, extend the **PersonSearchResult** table to create new table relationships.</span></span>

    ```xpp
    PersonSearchResultCategory::Customer needs a relation:PersonSearchResult.ResultRecId = CustTable.RecId,PersonSearchResult.ResultTableId = CustTable.TableId
    ```

## <a name="integrate-with-the-global-address-book-optional"></a><span data-ttu-id="7418b-124">グローバル アドレス帳と統合 (オプション)</span><span class="sxs-lookup"><span data-stu-id="7418b-124">Integrate with the Global address book (Optional)</span></span>

<span data-ttu-id="7418b-125">グローバル アドレス帳と統合する場合は、検出されたパーティー番号を **PersonSearchPartyNumberTmp** テーブルに挿入します。</span><span class="sxs-lookup"><span data-stu-id="7418b-125">If you want to integrate with the Global address book, insert any discovered party numbers into the **PersonSearchPartyNumberTmp** table.</span></span> <span data-ttu-id="7418b-126">**PersonSearchProcessor** の **findPartyLink** メソッドは、当事者番号を、ユーザー、顧客、仕入先などの他の検索コンポーネントにリンクします。</span><span class="sxs-lookup"><span data-stu-id="7418b-126">The **findPartyLink** method of **PersonSearchProcessor** tries to link party numbers to other search artifacts, such as users, customers, or vendors.</span></span>

<span data-ttu-id="7418b-127">このメソッドにはデリゲート **onFindPartyLink** があり、当事者番号に基づいて検索する追加のコンポーネントを指定できます。</span><span class="sxs-lookup"><span data-stu-id="7418b-127">This method has a delegate, **onFindPartyLink**, that lets you specify additional artifacts to search, based on the party numbers.</span></span>

<span data-ttu-id="7418b-128">**PersonSearchCriteria** テーブルでは、エンド ユーザーが、システムで個人データの検索に使用するパラメーターを指定できます。</span><span class="sxs-lookup"><span data-stu-id="7418b-128">The **PersonSearchCriteria** tables let end users specify the parameters by which to search the system for personal data.</span></span>

## <a name="create-new-search-criteria"></a><span data-ttu-id="7418b-129">新しい検索基準を作成する</span><span class="sxs-lookup"><span data-stu-id="7418b-129">Create new search criteria</span></span>

<span data-ttu-id="7418b-130">新しい検索条件を必要である場合は、これらの手順に従います。</span><span class="sxs-lookup"><span data-stu-id="7418b-130">If you need new search criteria, follow these steps.</span></span>

1. <span data-ttu-id="7418b-131">**PersonSearchCriteriaName**、**PersonSearchCriteriaAddress**、および **PersonSearchCriteriaKnownId** を拡張または独自のテーブルを作成します。</span><span class="sxs-lookup"><span data-stu-id="7418b-131">Extend the **PersonSearchCriteriaName**, **PersonSearchCriteriaAddress**, and **PersonSearchCriteriaKnownId** tables, or create your own tables.</span></span>
2. <span data-ttu-id="7418b-132">新しいデータ フィールドを表示するには、**PersonSearchDialog** フォームを拡張します。</span><span class="sxs-lookup"><span data-stu-id="7418b-132">Extend the **PersonSearchDialog** form to show these new data fields.</span></span>
3. <span data-ttu-id="7418b-133">検索処理中に新しい条件を使用します。</span><span class="sxs-lookup"><span data-stu-id="7418b-133">Use the new criteria during search processing.</span></span>

<span data-ttu-id="7418b-134">**PersonSearch** フォームには、担当者の検索によって検出された結果のセットが表示されます。</span><span class="sxs-lookup"><span data-stu-id="7418b-134">The **PersonSearch** form shows the set of results that was discovered by a person search.</span></span>

## <a name="show-the-new-search-category-in-the-personsearch-form"></a><span data-ttu-id="7418b-135">PersonSearch 形式で新しい検索カテゴリを表示</span><span class="sxs-lookup"><span data-stu-id="7418b-135">Show the new search category in the PersonSearch form</span></span>

1. <span data-ttu-id="7418b-136">**PersonSearchResult** テーブルの新しいビューを作成します。</span><span class="sxs-lookup"><span data-stu-id="7418b-136">Create a new view on the **PersonSearchResult** table.</span></span> <span data-ttu-id="7418b-137">このビューは結果を新しい **PersonSearchResultCategory** に限定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="7418b-137">This view should restrict results to only your new **PersonSearchResultCategory**.</span></span>
2. <span data-ttu-id="7418b-138">ビューを結果レコードに結合させ、必要なフィールドのビューを作成します (たとえば、**PersonSearchResultCustomerView**)。</span><span class="sxs-lookup"><span data-stu-id="7418b-138">Join the view to your result record, and create the view fields that are needed (for example, **PersonSearchResultCustomerView**).</span></span>
3. <span data-ttu-id="7418b-139">新しいリレーションシップを新しいビューに作成するには、**PersonSearchResult** テーブルを拡張します。</span><span class="sxs-lookup"><span data-stu-id="7418b-139">Extend the **PersonSearchResult** table to create a new relationship to the new view.</span></span> <span data-ttu-id="7418b-140">このリレーションシップは、人物の検索 ID に結合する必要があります。</span><span class="sxs-lookup"><span data-stu-id="7418b-140">This relationship should join on the person search ID.</span></span>
4. <span data-ttu-id="7418b-141">**PersonSearch** フォームを拡張します。</span><span class="sxs-lookup"><span data-stu-id="7418b-141">Extend the **PersonSearch** form:</span></span>

    1. <span data-ttu-id="7418b-142">データ ソースとして新しいビューを追加します。</span><span class="sxs-lookup"><span data-stu-id="7418b-142">Add the new view as a data source.</span></span>
    2. <span data-ttu-id="7418b-143">結果のグリッドと **含む/除外** ボタンを使用して結果に新しいタブを追加します。</span><span class="sxs-lookup"><span data-stu-id="7418b-143">Add a new tab to the results with the result grid and the **Include/Exclude** buttons.</span></span>
    3. <span data-ttu-id="7418b-144">**含む/除外** ボタンのイベント ハンドラーを作成して **PersonSearchResult** レコードを更新します。</span><span class="sxs-lookup"><span data-stu-id="7418b-144">Create event handlers for the **Include/Exclude** buttons to update the **PersonSearchResult** records.</span></span>

        <span data-ttu-id="7418b-145">**PersonSearchEventHandler::updateMarkedOnButtonClicked()** メソッドが利便性のために用意されています。</span><span class="sxs-lookup"><span data-stu-id="7418b-145">The **PersonSearchEventHandler::updateMarkedOnButtonClicked()** method is provided for convenience.</span></span>

> [!NOTE]
> <span data-ttu-id="7418b-146">結果キャプションのレコード数を確認するには、**OnQueryExecuted** ビューのデータ ソース イベントでイベント ハンドラーを作成します。</span><span class="sxs-lookup"><span data-stu-id="7418b-146">If you want to see the record count in the result caption, create an event handler on the **OnQueryExecuted** view data source event.</span></span> <span data-ttu-id="7418b-147">次に、**PersonSearch** フォームで **setResultCountOnGridCaption()** メソッドを呼び出して、カウントを更新します。</span><span class="sxs-lookup"><span data-stu-id="7418b-147">Next, call the **setResultCountOnGridCaption()** method on the **PersonSearch** form to update the count.</span></span>

<span data-ttu-id="7418b-148">各 **PersonSearchEntityFilterRelation** レコードは、フィルターを適用する場合、条件、フィルター テーブルおよび適用するフィールドを指定します。</span><span class="sxs-lookup"><span data-stu-id="7418b-148">Each **PersonSearchEntityFilterRelation** record specifies the conditions when a filter should apply, and the filter table and field to apply.</span></span>

<span data-ttu-id="7418b-149">フィルター関係のセットは、パッケージの構築時にテンプレート メタデータと比較されます。</span><span class="sxs-lookup"><span data-stu-id="7418b-149">The set of filter relations is compared to the template metadata when the package is built.</span></span>

<span data-ttu-id="7418b-150">フィルターを作成するためには、**PersonSearchResult** レコードと一致するフィルター カテゴリが存在する必要があります。</span><span class="sxs-lookup"><span data-stu-id="7418b-150">For a filter to be created, a **PersonSearchResult** record with the matching filter category must exist.</span></span> <span data-ttu-id="7418b-151">見つかったら、**PersonSearchResult** は、フィルター値が置かれているテーブル フィールドを参照します。</span><span class="sxs-lookup"><span data-stu-id="7418b-151">After it's found, the **PersonSearchResult** references the table field where the filter value resides.</span></span>

## <a name="create-new-filters"></a><span data-ttu-id="7418b-152">新しいフィルタを作成する</span><span class="sxs-lookup"><span data-stu-id="7418b-152">Create new filters</span></span>

1. <span data-ttu-id="7418b-153">**PersonSearchEntityFilterRelation** テーブルを拡張するには、Chain of Command (COC) を使用します。</span><span class="sxs-lookup"><span data-stu-id="7418b-153">Use the Chain of Command to extend the **PersonSearchEntityFilterRelation** table.</span></span>
2. <span data-ttu-id="7418b-154">新しいフィルターのタイプとソースを決定する:</span><span class="sxs-lookup"><span data-stu-id="7418b-154">Decide on the type and source of the new filter:</span></span>

    1. <span data-ttu-id="7418b-155">フィルターが拡張データ型 (EDT) または列挙の場合は、**MetadataTypeId** をデータ型の ID に設定します。</span><span class="sxs-lookup"><span data-stu-id="7418b-155">If the filter is an extended data type (EDT) or enumeration, set the **MetadataTypeId** to the data type ID.</span></span>
    2. <span data-ttu-id="7418b-156">フィルターがソース テーブルのフィールドである場合は、ソース テーブルとソース フィールド ID を指定します。</span><span class="sxs-lookup"><span data-stu-id="7418b-156">If the filter is a source table field, specify the source table and source field IDs.</span></span>
    3. <span data-ttu-id="7418b-157">フィルターがエンティティ フィールドである場合は、エンティティ フィールド ID を指定します。</span><span class="sxs-lookup"><span data-stu-id="7418b-157">If the filter is an entity field, specify the entity field ID.</span></span>

3. <span data-ttu-id="7418b-158">フィルター テーブルとフィルター フィールドを決定します。</span><span class="sxs-lookup"><span data-stu-id="7418b-158">Decide on the filter table and filter field.</span></span>

    <span data-ttu-id="7418b-159">フィルター テーブルは、一致するカテゴリを使用した **PersonSearchResult** として使用可能でなければなりません。</span><span class="sxs-lookup"><span data-stu-id="7418b-159">The filter table must be available as a **PersonSearchResult** with a matching category.</span></span> <span data-ttu-id="7418b-160">それ以外の場合、フィルターは作成されません。</span><span class="sxs-lookup"><span data-stu-id="7418b-160">Otherwise, no filters will be created.</span></span>

4. <span data-ttu-id="7418b-161">新しいフィルター レコードを挿入します。</span><span class="sxs-lookup"><span data-stu-id="7418b-161">Insert the new filter record.</span></span>

    <span data-ttu-id="7418b-162">個人検索フレームワークが、最初にフォームが開いたときに、すべての除外の初期化を自動的に管理します。</span><span class="sxs-lookup"><span data-stu-id="7418b-162">The person search framework will automatically manage initialization of all exclusions when the form is first opened.</span></span> <span data-ttu-id="7418b-163">除外を使用すると、特定のエンティティ フィールドのフィルター構築機能を抑制できます。</span><span class="sxs-lookup"><span data-stu-id="7418b-163">Exclusions let you suppress the filter building functionality for specific entity fields.</span></span>

## <a name="create-new-exclusions"></a><span data-ttu-id="7418b-164">新しい除外を作成する</span><span class="sxs-lookup"><span data-stu-id="7418b-164">Create new exclusions</span></span>

1. <span data-ttu-id="7418b-165">**PersonSearchEntityExclusion** テーブルを拡張するには、Chain of Command (COC) を使用します。</span><span class="sxs-lookup"><span data-stu-id="7418b-165">Use the Chain of Command (COC) to extend the **PersonSearchEntityExclusion** table.</span></span>
2. <span data-ttu-id="7418b-166">**CoC メソッド** で、エンティティ、エンティティ フィールド、除外が有効かどうかを指定します。</span><span class="sxs-lookup"><span data-stu-id="7418b-166">In the **CoC method**, specify the entity, the entity field, and whether the exclusion is active.</span></span>
3. <span data-ttu-id="7418b-167">新しい除外レコードを挿入します。</span><span class="sxs-lookup"><span data-stu-id="7418b-167">Insert the new exclusion record.</span></span>

    <span data-ttu-id="7418b-168">個人検索フレームワークが、最初にフォームが開いたときに、すべての除外の初期化を自動的に管理します。</span><span class="sxs-lookup"><span data-stu-id="7418b-168">The person search framework will automatically manage initialization of all exclusions when the form is first opened.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="7418b-169">その他のリソース</span><span class="sxs-lookup"><span data-stu-id="7418b-169">Additional resources</span></span>

<span data-ttu-id="7418b-170">欧州連合の一般的なデータ保護規則 (GDPR) に基づくデータの依頼への応答の一部として、個人検索レポートを拡張している場合、この規則に関する詳細については、[一般データ保護規則の概要](./gdpr-guide.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="7418b-170">If you're extending the Person search report as part of a response to a request for data under the General Data Protection Regulation (GDPR) in the European Union, more information about that regulation is available in the [General Data Protection Regulation overview](./gdpr-guide.md).</span></span>

<span data-ttu-id="7418b-171">GDPR の詳細については、[欧州連合の Web サイト](https://europa.eu/) および [Microsoft Trust Center](https://www.microsoft.com/TrustCenter/Privacy/gdpr/default.aspx) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="7418b-171">You can learn more about the GDPR on the [European Union's website](https://europa.eu/) and on the [Microsoft Trust Center](https://www.microsoft.com/TrustCenter/Privacy/gdpr/default.aspx).</span></span>


### <a name="disclaimer"></a><span data-ttu-id="7418b-172">免責事項</span><span class="sxs-lookup"><span data-stu-id="7418b-172">Disclaimer</span></span>
<span data-ttu-id="7418b-173">(c)2018 Microsoft Corporation.</span><span class="sxs-lookup"><span data-stu-id="7418b-173">(c)2018 Microsoft Corporation.</span></span> <span data-ttu-id="7418b-174">All rights reserved.</span><span class="sxs-lookup"><span data-stu-id="7418b-174">All rights reserved.</span></span> <span data-ttu-id="7418b-175">このドキュメントは、"現状のまま" 提供されます。</span><span class="sxs-lookup"><span data-stu-id="7418b-175">This document is provided "as-is."</span></span> <span data-ttu-id="7418b-176">URL およびその他のインターネット Web サイトの参照を含む、このドキュメントの情報および見解は、予告なしに変更することがあります。</span><span class="sxs-lookup"><span data-stu-id="7418b-176">Information and views expressed in this document, including URL and other Internet Web site references, may change without notice.</span></span> <span data-ttu-id="7418b-177">このドキュメントの使用上のリスクは、すべてユーザーが負うものとします。</span><span class="sxs-lookup"><span data-stu-id="7418b-177">You bear the risk of using it.</span></span> <span data-ttu-id="7418b-178">このドキュメントは、Microsoft の製品に含まれる知的財産に対する法律上の権利をお客様に付与するものではありません。</span><span class="sxs-lookup"><span data-stu-id="7418b-178">This document does not provide you with any legal rights to any intellectual property in any Microsoft product.</span></span> <span data-ttu-id="7418b-179">内部での参照を目的とする場合、このドキュメントをコピーして使用できます。</span><span class="sxs-lookup"><span data-stu-id="7418b-179">You may copy and use this document for your internal, reference purposes.</span></span> 


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]