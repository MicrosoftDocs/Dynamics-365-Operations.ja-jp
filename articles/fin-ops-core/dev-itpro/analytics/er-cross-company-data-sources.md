---
title: 電子申告 (ER) における会社間データ ソース
description: このトピックでは、電子申告 (ER) で会社間のデータ ソースを使用する方法について説明します。
author: NickSelin
ms.date: 04/23/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ERModelMappingDesigner, ERFormatMappingLegalEntityFilterTable
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.custom: 220314
ms.assetid: 2685df16-5ec8-4fd7-9495-c0f653e82567
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2018-04-01
ms.dyn365.ops.version: Release 8.0
ms.openlocfilehash: 25c665c797d0cea10cbe337e86be4a07f1f5074a
ms.sourcegitcommit: ab3f5d0da6eb0177bbad720e73c58926d686f168
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/26/2021
ms.locfileid: "5944464"
---
# <a name="cross-company-data-sources-in-electronic-reporting-er"></a><span data-ttu-id="d1f35-103">電子申告 (ER) における会社間データ ソース</span><span class="sxs-lookup"><span data-stu-id="d1f35-103">Cross-company data sources in Electronic reporting (ER)</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="d1f35-104">さまざまな形式で送信ドキュメントを生成するため、電子申告 (ER) 形式をデザインできます。</span><span class="sxs-lookup"><span data-stu-id="d1f35-104">You can design Electronic reporting (ER) formats to generate outgoing documents in various formats.</span></span> <span data-ttu-id="d1f35-105">ドキュメントを生成する際、ER 形式は、対応する ER モデル マッピングでコンフィギュレーションされたデータ ソースを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="d1f35-105">When a document is generated, an ER format calls data sources that were configured in a corresponding ER model mapping.</span></span> <span data-ttu-id="d1f35-106">レコード取得用にアプリケーション テーブルへのアクセスをコンフィギュレーションするため、**テーブル レコード** タイプの ER データ ソースを使用できます。</span><span class="sxs-lookup"><span data-stu-id="d1f35-106">To configure access to application tables for record retrieval, you can use ER data sources of the **Table records** type.</span></span> <span data-ttu-id="d1f35-107">アクセスするテーブルが共有テーブル (つまり、会社 ID なしでデータが保存されているテーブル) である場合、このデータ ソースは、すべてのレコードを返します。</span><span class="sxs-lookup"><span data-stu-id="d1f35-107">When the accessing table is a shared table (that is, a table where data is saved without a company identifier), this data source returns all records.</span></span> <span data-ttu-id="d1f35-108">アクセスするテーブルが会社固有のテーブル (つまり、会社ごとのデータが保存されるテーブル) である場合、このデータ ソースは現在の会社 (つまり、ER 形式が実行されている会社コンテキスト) に対して保存されたレコードのみを返します。</span><span class="sxs-lookup"><span data-stu-id="d1f35-108">When the accessing table is a company-dependent table (that is, a table where data is saved per company), this data source returns only the records that have been saved for the current company (that is, the company context that the ER format is running under).</span></span>

<span data-ttu-id="d1f35-109">モデル マッピングでの **テーブル レコード** タイプのデータ ソースは、会社間データ ソースとしてマークされます。</span><span class="sxs-lookup"><span data-stu-id="d1f35-109">Every data source of the **Table records** type in a model mapping can be now marked as a cross-company data source.</span></span> <span data-ttu-id="d1f35-110">したがって、アプリケーション テーブルで会社間データにアクセスするため、**テーブル レコード** タイプの ER データ ソースを使用できます。</span><span class="sxs-lookup"><span data-stu-id="d1f35-110">Therefore, you can use data sources of the **Table records** type to access cross-company data in application tables.</span></span>

<span data-ttu-id="d1f35-111">会社間としてデータ ソースをマークする場合、次の動作が発生します。</span><span class="sxs-lookup"><span data-stu-id="d1f35-111">If you mark a data source as cross-company, the following behavior occurs:</span></span>

- <span data-ttu-id="d1f35-112">CompanyInfo を除く任意の共有テーブルを参照するデータ ソースについては、データ ソースは参照テーブル内に存在するすべてのレコードを返します。</span><span class="sxs-lookup"><span data-stu-id="d1f35-112">For a data source that refers to any shared table except CompanyInfo, the data source returns all records that exist in the referenced table.</span></span> 
- <span data-ttu-id="d1f35-113">CompanyInfo テーブルを参照するデータ ソースについては、CompanyInfo が共有テーブルであっても、データ ソースは定義されるスコープから会社の ID を含むレコードを返します。</span><span class="sxs-lookup"><span data-stu-id="d1f35-113">For a data source that refers to the CompanyInfo table, even though CompanyInfo is a shared table, the data source returns the records that contain the identifier of a company from the defined scope.</span></span>
- <span data-ttu-id="d1f35-114">任意の会社固有テーブルについては、データ ソースは定義されるスコープから会社の ID を含む参照テーブルのレコードを返します。</span><span class="sxs-lookup"><span data-stu-id="d1f35-114">For any company-dependent table, the data source returns the records of the referenced table that contain the identifier of a company from the defined scope.</span></span>

<span data-ttu-id="d1f35-115">システム クエリ ダイアログ ボックスで、会社間としてマークされる任意のデータ ソースで **クエリの要求** オプションが有効とされる場合、**会社範囲** タブで 1 つ以上の会社を含むよう手動で選択できます。</span><span class="sxs-lookup"><span data-stu-id="d1f35-115">In the system query dialog box, when the **Ask for query** option is turned on for any data source that is marked as cross-company, you can manually select one or more companies to include on the **Company range** tab.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="d1f35-116">他のフィルターと同様に、ER 形式の実行時にクエリの最後の使用値として会社フィルターが保持されます。</span><span class="sxs-lookup"><span data-stu-id="d1f35-116">Like other filters, the company filter is persisted as a last-used value for queries when you run an ER format.</span></span> <span data-ttu-id="d1f35-117">データ ソースの会社間の値を変更すると、フィルターは自動的に変更されません。</span><span class="sxs-lookup"><span data-stu-id="d1f35-117">The filter isn't automatically changed if you change the cross-company value for a data source.</span></span> <span data-ttu-id="d1f35-118">別のデータ ソースに対して会社間の異なる値を使用するには、対応するユーザー固有の選択項目を削除します。</span><span class="sxs-lookup"><span data-stu-id="d1f35-118">To use a different cross-company value for another data source, delete the corresponding user-specific selection.</span></span>

<span data-ttu-id="d1f35-119">会社間としてマークされているデータ ソースごとに、ER 式で **FILTER** および **WHERE** 関数を使用してレコードを選択できます。</span><span class="sxs-lookup"><span data-stu-id="d1f35-119">For every data source that is marked as cross-company, you can select the records that you want by using the **FILTER** and **WHERE** functions in ER expressions.</span></span> <span data-ttu-id="d1f35-120">**dataAreaID** フィールドは会社 ID としても使用できます。</span><span class="sxs-lookup"><span data-stu-id="d1f35-120">The **dataAreaID** field can also be used as a company identifier.</span></span> <span data-ttu-id="d1f35-121">現在、**dataAreaID** フィールドは **FILTER** 関数が使用される際の次の条件のタイプに制限されます。</span><span class="sxs-lookup"><span data-stu-id="d1f35-121">Currently, the **dataAreaID** field is limited to the following types of conditions when the **FILTER** function is used:</span></span>

- <span data-ttu-id="d1f35-122">単一の **dataAreaID** フィールドの比較を持つ条件のみがサポートされます。</span><span class="sxs-lookup"><span data-stu-id="d1f35-122">Only conditions that have a single **dataAreaID** field comparison are supported.</span></span>
- <span data-ttu-id="d1f35-123">レコードの一覧項目に依存しない式を持つ比較のみが使用できます。</span><span class="sxs-lookup"><span data-stu-id="d1f35-123">Only comparisons that have expressions that don't depend on records list items are allowed.</span></span>

<span data-ttu-id="d1f35-124">したがって、次の式は有効です。</span><span class="sxs-lookup"><span data-stu-id="d1f35-124">Therefore, the following expression is valid.</span></span>

```ER Expression
FILTER (MyTable, MyTable.dataAreaID = $StringUserInputParameter)
While shown below expressions will not pass the validation:
FILTER (MyTable, MyTable.dataAreaID = MyTable2RecordsList.MyField)
FILTER (MyTable, 
    OR(
        MyTable.dataAreaID = $StringUserInputParameter1,
        MyTable.dataAreaID = $StringUserInputParameter2
    )
)
```

<span data-ttu-id="d1f35-125">既定では、現在のアプリケーションのすべての会社がスコープに含まれます。</span><span class="sxs-lookup"><span data-stu-id="d1f35-125">By default, the scope includes all companies of the current application.</span></span> <span data-ttu-id="d1f35-126">ただし、それは制限できます。</span><span class="sxs-lookup"><span data-stu-id="d1f35-126">However, it can be restricted.</span></span> <span data-ttu-id="d1f35-127">単一の ER 形式の会社間のデータ アクセスのスコープを制限するには、形式に特定の組織階層を割り当てます。</span><span class="sxs-lookup"><span data-stu-id="d1f35-127">To restrict the scope of cross-company data access for a single ER format, assign a specific organization hierarchy to the format.</span></span> <span data-ttu-id="d1f35-128">ER 形式用に階層が定義されると、形式が会社間データ ソースを呼び出す場合でも、割り当てられた階層に表示される法人のレコードのみが返されます。</span><span class="sxs-lookup"><span data-stu-id="d1f35-128">When a hierarchy is defined for an ER format, only records for legal entities that are presented in the assigned hierarchy are returned, even though the format calls cross-company data sources.</span></span> <span data-ttu-id="d1f35-129">既に存在しない階層への参照が ER 形式に対して定義されると、既定のスコープが適用され、形式は会社間のデータ ソースを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="d1f35-129">When a reference to a hierarchy that no longer exists is defined for an ER format, the default scope is applied, and the format calls cross-company data sources.</span></span> <span data-ttu-id="d1f35-130">この場合、すべてのアプリケーション会社のレコードが返されます。</span><span class="sxs-lookup"><span data-stu-id="d1f35-130">In this situation, records for all application companies are returned.</span></span>

<span data-ttu-id="d1f35-131">**ドラフトを使用** オプションが単一の ER 形式組織階層への割り当てに対して有効となっている場合、この階層のドラフト バージョンからの法人は、会社間のデータ ソースのスコープを識別するために使用されることに注意してください。</span><span class="sxs-lookup"><span data-stu-id="d1f35-131">Note that when the **Use draft** option is turned on for the assigned to a single ER format organization hierarchy, the legal entities from the draft version of this hierarchy will be used to identify the scope for cross-company data sources.</span></span> <span data-ttu-id="d1f35-132">ドラフト バージョンが存在しない場合、この組織階層の最後に発行されたバージョンからの法人がこれに対して使用されます。</span><span class="sxs-lookup"><span data-stu-id="d1f35-132">If the draft version does not exist, the legal entities from the last published version of this organization hierarchy will be used for this.</span></span>

<span data-ttu-id="d1f35-133">**ドラフトを使用** オプションが単一の ER 形式組織階層への割り当てに対して有効となっていない場合、この階層の最後に発行されたバージョンからの法人は、会社間のデータ ソースのスコープを識別するために使用されることに注意してください。</span><span class="sxs-lookup"><span data-stu-id="d1f35-133">Note that when the **Use draft** option is turned off for the assigned to a single ER format organization hierarchy, the legal entities from the last published version of this organization hierarchy will be used to identify the scope for cross-company data sources.</span></span> <span data-ttu-id="d1f35-134">組織階層の日付の有効性は、ER フレームワークでまだサポートされていません。</span><span class="sxs-lookup"><span data-stu-id="d1f35-134">Date effectiveness of organization hierarchies is not supported yet in the ER framework.</span></span>

<span data-ttu-id="d1f35-135">階層は、ER ワークスペースからまたは **O組織管理 \> 電子申告 \> 形式の法人フィルター** メニュー項目を使用してアクセスできる特定のページでの形式に割り当てられます。</span><span class="sxs-lookup"><span data-stu-id="d1f35-135">The hierarchy can be assigned to a format in a specific page that can be accessed from the ER workspace or by using the **Organization administration \> Electronic reporting \> Legal entity filter for formats** menu item.</span></span> <span data-ttu-id="d1f35-136">ページにアクセスするには、**形式の法人フィルターを管理** 権限 (ERMaintainFormatMappingLegalEntityFilters) がユーザーに付与される必要があります。</span><span class="sxs-lookup"><span data-stu-id="d1f35-136">To access the page, the **Maintain legal entity filters for format** privilege (ERMaintainFormatMappingLegalEntityFilters) must be granted to a user.</span></span> <span data-ttu-id="d1f35-137">ユーザーが手動でシステム クエリ ダイアログ ボックスで指定できる制限に加えて、形式に対する階層ベース法人のスコープ制限が適用されます。</span><span class="sxs-lookup"><span data-stu-id="d1f35-137">The scope restriction of hierarchy-based legal entities for the format is applied in addition to the restriction that the user can manually specify in the system query dialog box.</span></span> <span data-ttu-id="d1f35-138">これらの制限の交差部分は、形式の実行時に使用されます。</span><span class="sxs-lookup"><span data-stu-id="d1f35-138">The intersection of these restrictions is used when the format is run.</span></span>

<span data-ttu-id="d1f35-139">この機能の詳細については、7.5.4.3 IT サービス/ソリューション コンポーネントの取得/開発 (10677) 業務プロセスの一部であるタスクガイド、**会社間モードで会社固有テーブルの ER アクセス レコード** を再生し、[Microsoft ダウンロード センター](https://go.microsoft.com/fwlink/?linkid=874684) からダウンロードできます。</span><span class="sxs-lookup"><span data-stu-id="d1f35-139">To learn more about this feature, play the task guide, **ER Access records of company dependent tables in cross-company mode**, which is part of the 7.5.4.3 Acquire/Develop IT service/solution components (10677) business process, and can be downloaded from the [Microsoft Download Center](https://go.microsoft.com/fwlink/?linkid=874684).</span></span> <span data-ttu-id="d1f35-140">このタスク ガイドでは、会社間モードでアプリケーション テーブルにアクセスする ER モデル マッピングおよび ER 形式のコンフィギュレーションのプロセスについて説明します。</span><span class="sxs-lookup"><span data-stu-id="d1f35-140">This task guide walks you through the process of configuring an ER model mapping and ER format to access application tables in cross-company mode.</span></span>

<span data-ttu-id="d1f35-141">タスクガイドを完成させるには、次のファイルをダウンロードしてください。</span><span class="sxs-lookup"><span data-stu-id="d1f35-141">Download the following files to complete the task guide:</span></span>

- [<span data-ttu-id="d1f35-142">ER モデル コンフィギュレーション - CrossCompanyDataAccessModel.xml</span><span class="sxs-lookup"><span data-stu-id="d1f35-142">ER model configuration - CrossCompanyDataAccessModel.xml</span></span>](https://download.microsoft.com/download/4/2/5/4258f891-7054-4821-aedd-3721ba25fdd5/CrossCompanyDataAccessModel.xml)
- [<span data-ttu-id="d1f35-143">ER 形式コンフィギュレーション - CrossCompanyDataAccessFormat.xml</span><span class="sxs-lookup"><span data-stu-id="d1f35-143">ER format configuration - CrossCompanyDataAccessFormat.xml</span></span>](https://download.microsoft.com/download/3/2/1/321deb75-3ba9-4323-99bf-207a52c60b5c/CrossCompanyDataAccessFormat.xml)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
