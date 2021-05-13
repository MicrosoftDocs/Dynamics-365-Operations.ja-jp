---
title: Human Resources 仮想テーブルに関するよく寄せられる質問
description: このトピックでは、Human Resources 仮想エンティティに関してよく寄せられる質問の一覧を示します。
author: jaredha
ms.date: 04/22/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Developer, IT Pro
ms.reviewer: sericks
ms.search.scope: Human Resources
ms.search.region: Global
ms.author: sunilg
ms.search.validFrom: 2020-12-15
ms.dyn365.ops.version: 10.0.12
ms.openlocfilehash: 09b1bad6cfc24259d0be0400898e4a629d8b21fd
ms.sourcegitcommit: 9283caad2d0636f98579c995784abec19fda2e3f
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/22/2021
ms.locfileid: "5935847"
---
# <a name="human-resources-virtual-tables-faq"></a><span data-ttu-id="5c1e1-103">Human Resources 仮想テーブルに関するよく寄せられる質問</span><span class="sxs-lookup"><span data-stu-id="5c1e1-103">Human Resources virtual tables FAQ</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="5c1e1-104">このトピックでは、Dynamics 365 Human Resources の仮想テーブルに関してよく寄せられる質問のコレクションを示します。</span><span class="sxs-lookup"><span data-stu-id="5c1e1-104">This topic is a collection of frequently asked questions about virtual tables in Dynamics 365 Human Resources.</span></span>

> [!NOTE]
> <span data-ttu-id="5c1e1-105">Dataverse (旧 Common Data Service) および用語更新の詳細については、[Microsoft Dataverse とは何ですか?](/powerapps/maker/data-platform/data-platform-intro)を参照してください</span><span class="sxs-lookup"><span data-stu-id="5c1e1-105">For more information about Dataverse (formerly Common Data Service) and terminology updates, see [What is Microsoft Dataverse?](/powerapps/maker/data-platform/data-platform-intro)</span></span>

### <a name="can-a-solution-from-an-independent-software-vendor-isv-take-a-dependency-on-virtual-tables-what-does-the-application-lifecycle-management-alm-look-like"></a><span data-ttu-id="5c1e1-106">独立系ソフトウェアベンダー (ISV) のソリューションは、仮想テーブルに依存できますか?</span><span class="sxs-lookup"><span data-stu-id="5c1e1-106">Can a solution from an independent software vendor (ISV) take a dependency on virtual tables?</span></span> <span data-ttu-id="5c1e1-107">アプリケーション ライフサイクル管理 (ALM) はどのような外観になりますか。</span><span class="sxs-lookup"><span data-stu-id="5c1e1-107">What does the application lifecycle management (ALM) look like?</span></span>

<span data-ttu-id="5c1e1-108">はい。</span><span class="sxs-lookup"><span data-stu-id="5c1e1-108">Yes.</span></span> <span data-ttu-id="5c1e1-109">仮想テーブルはすべて Dynamics 365 HR Virtual Entities ソリューションで生成され、API によって管理されます。</span><span class="sxs-lookup"><span data-stu-id="5c1e1-109">The virtual tables are all generated in the Dynamics 365 HR Virtual Entities solution, which is API-managed.</span></span> <span data-ttu-id="5c1e1-110">ソリューションの項目は、テーブルの表示または非表示に応じて変更されます。</span><span class="sxs-lookup"><span data-stu-id="5c1e1-110">The items in the solution change as you make tables visible or hidden.</span></span> <span data-ttu-id="5c1e1-111">ただし、ソリューションは引き続き依存できる管理ソリューションです。</span><span class="sxs-lookup"><span data-stu-id="5c1e1-111">However, the solution is still a managed solution that you can take dependency on.</span></span> <span data-ttu-id="5c1e1-112">各テーブルのスキーマおよび契約が維持されます。</span><span class="sxs-lookup"><span data-stu-id="5c1e1-112">The schema and contract for each table is maintained.</span></span> <span data-ttu-id="5c1e1-113">標準 ALM フローでは、ISV ソリューションの **既存の追加** オプションを使用して、このソリューションから仮想テーブルに対する標準参照を取得するだけです。</span><span class="sxs-lookup"><span data-stu-id="5c1e1-113">The standard ALM flow just takes a standard reference to a virtual table from this solution with the ISV solution's **Add existing** option.</span></span> <span data-ttu-id="5c1e1-114">ソリューションの依存関係の欠落が、ソリューションのインポート時にチェックされます。</span><span class="sxs-lookup"><span data-stu-id="5c1e1-114">Missing dependency of the solution will be checked when the solution is imported.</span></span> <span data-ttu-id="5c1e1-115">インポート時に、特定の仮想テーブルがまだ存在しない場合は、仮想テーブルが自動的に表示されます。</span><span class="sxs-lookup"><span data-stu-id="5c1e1-115">During import, if a specified virtual table doesn't yet exist, the virtual table is automatically made visible.</span></span>

### <a name="which-tables-from-human-resources-do-users-see-in-the-catalog-in-dataverse"></a><span data-ttu-id="5c1e1-116">Dataverse のカタログでユーザーに表示される Human Resources のテーブルは何ですか?</span><span class="sxs-lookup"><span data-stu-id="5c1e1-116">Which tables from Human Resources do users see in the catalog in Dataverse?</span></span>

<span data-ttu-id="5c1e1-117">一般に、ユーザーには、**IsPublic** が **はい** に設定されているすべてのテーブルが表示されます。</span><span class="sxs-lookup"><span data-stu-id="5c1e1-117">Generally, users see all tables where **IsPublic** is set to **Yes**.</span></span> <span data-ttu-id="5c1e1-118">これらのテーブルは、Open Data Protocol (OData) で現在表示されているテーブルと同じです。</span><span class="sxs-lookup"><span data-stu-id="5c1e1-118">These tables are the same tables that are currently visible in Open Data Protocol (OData).</span></span>

### <a name="do-all-microsoft-power-platform-users-have-to-be-users-in-human-resources"></a><span data-ttu-id="5c1e1-119">すべての Microsoft Power Platform ユーザーが Human Resources のユーザーである必要がありますか?</span><span class="sxs-lookup"><span data-stu-id="5c1e1-119">Do all Microsoft Power Platform users have to be users in Human Resources?</span></span>

<span data-ttu-id="5c1e1-120">仮想テーブルを介して Human Resources データにアクセスしようとする Microsoft Power Platform のユーザーはすべて、Human Resources でユーザーとして存在している必要があります。</span><span class="sxs-lookup"><span data-stu-id="5c1e1-120">Any user of Microsoft Power Platform who tries to access Human Resources data through a virtual table must also exist as a user in Human Resources.</span></span> <span data-ttu-id="5c1e1-121">したがって、*すべて* のユーザーが Human Resources のユーザーである必要はありません。</span><span class="sxs-lookup"><span data-stu-id="5c1e1-121">So not *all* users must be users in Human Resources.</span></span> <span data-ttu-id="5c1e1-122">仮想テーブルを介して Human Resources データにアクセスするユーザーのみが Human Resources のユーザーである必要があります。</span><span class="sxs-lookup"><span data-stu-id="5c1e1-122">Only those users who access Human Resources data through virtual tables must be users in Human Resources.</span></span>

### <a name="where-do-i-find-the-catalog-table"></a><span data-ttu-id="5c1e1-123">カタログ テーブルはどこにありますか?</span><span class="sxs-lookup"><span data-stu-id="5c1e1-123">Where do I find the catalog table?</span></span>

<span data-ttu-id="5c1e1-124">テーブル カタログは、Human Resources アプリケーションの **Dataverse 統合** ページの **仮想テーブル** タブに表示されます。</span><span class="sxs-lookup"><span data-stu-id="5c1e1-124">The table catalog is listed on the **Virtual tables** tab of the **Dataverse integration** page in the Human Resources application.</span></span> <span data-ttu-id="5c1e1-125">使用可能なすべてのテーブルが、設定およびコンフィギュレーションの完了後に一覧表示されます。</span><span class="sxs-lookup"><span data-stu-id="5c1e1-125">All available tables are listed after setup and configuration is completed.</span></span> <span data-ttu-id="5c1e1-126">詳細については、[Dataverse 仮想テーブルのコンフィギュレーション](hr-admin-integration-common-data-service-virtual-entities.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="5c1e1-126">For more information, see [Configure Dataverse virtual tables](hr-admin-integration-common-data-service-virtual-entities.md).</span></span>

### <a name="is-there-a-way-to-specify-a-company-when-i-perform-data-operations-on-a-virtual-table"></a><span data-ttu-id="5c1e1-127">仮想テーブルに対してデータ操作を実行するときに会社を指定する方法はありますか?</span><span class="sxs-lookup"><span data-stu-id="5c1e1-127">Is there a way to specify a company when I perform data operations on a virtual table?</span></span>

<span data-ttu-id="5c1e1-128">はい。</span><span class="sxs-lookup"><span data-stu-id="5c1e1-128">Yes.</span></span> <span data-ttu-id="5c1e1-129">Human Resources には会社が暗黙のうちに含まれていますが、Dataverse では会社でストライプされたテーブルごとに明示的な列になっています。</span><span class="sxs-lookup"><span data-stu-id="5c1e1-129">Although the company is implicit in Human Resources, it's an explicit column on each company-striped table in Dataverse.</span></span> <span data-ttu-id="5c1e1-130">**会社コード** 列 (値は 4 文字の文字列)、または **会社** 列 (cdm\_Company へのルックアップ) のいずれかを使用できます。</span><span class="sxs-lookup"><span data-stu-id="5c1e1-130">You can use either the **Company Code** column, where the value is a four-character string, or the **Company** column, which is a lookup to cdm\_Company.</span></span> <span data-ttu-id="5c1e1-131">どちらの方法でも同じ情報が得られます。</span><span class="sxs-lookup"><span data-stu-id="5c1e1-131">Both approaches provide the same information.</span></span>

<span data-ttu-id="5c1e1-132">Dataverse Web API を介してテーブルにアクセスする場合、その会社は **データ領域 ID** プロパティ (mshr\_dataareaid) で識別されます。</span><span class="sxs-lookup"><span data-stu-id="5c1e1-132">If you're accessing the table through the Dataverse Web API, the company is identified by the **Data Area ID** property (mshr\_dataareaid).</span></span> <span data-ttu-id="5c1e1-133">このプロパティを持つ各会社固有のテーブルには、cdm\_Company テーブルへのナビゲーション プロパティがあります。</span><span class="sxs-lookup"><span data-stu-id="5c1e1-133">Each company-specific table with this property has a navigation property to the cdm\_Company table.</span></span>

### <a name="can-i-change-the-prefix-for-the-virtual-tables"></a><span data-ttu-id="5c1e1-134">仮想テーブルの接頭語を変更することはできますか?</span><span class="sxs-lookup"><span data-stu-id="5c1e1-134">Can I change the prefix for the virtual tables?</span></span>

<span data-ttu-id="5c1e1-135">No.</span><span class="sxs-lookup"><span data-stu-id="5c1e1-135">No.</span></span> <span data-ttu-id="5c1e1-136">すべての Human Resources 仮想テーブルは、Dynamics 365 HR Virtual Entities ソリューションで生成され、"mshr\_" の接頭語が付く必要があります。</span><span class="sxs-lookup"><span data-stu-id="5c1e1-136">All Human Resources virtual tables should be generated in the Dynamics 365 HR Virtual Entities solution and have the "mshr\_" prefix.</span></span> <span data-ttu-id="5c1e1-137">この接頭語は変更しないでください。</span><span class="sxs-lookup"><span data-stu-id="5c1e1-137">Don't change this prefix.</span></span> <span data-ttu-id="5c1e1-138">接頭語を変更する必要があると考えられる場合は、そのシナリオを Microsoft と共有する必要があります。</span><span class="sxs-lookup"><span data-stu-id="5c1e1-138">If you have a scenario where you believe the prefix has to be changed, you should share that scenario with Microsoft.</span></span>

### <a name="how-can-i-filter-data-in-a-power-apps-app-based-on-the-current-user-or-any-other-dynamic-criteria-such-as-today-10"></a><span data-ttu-id="5c1e1-139">Power Apps アプリのデータについては、現在のユーザーまたはその他の動的な基準 (10 日前など) に基づいてフィルター処理を行うことができますか?</span><span class="sxs-lookup"><span data-stu-id="5c1e1-139">How can I filter data in a Power Apps app, based on the current user or any other dynamic criteria, such as today-10?</span></span>

<span data-ttu-id="5c1e1-140">テーブルの RetrieveMultiple メッセージに対して前工程プラグインを作成し、その中のクエリに対する基準を変更することができます。</span><span class="sxs-lookup"><span data-stu-id="5c1e1-140">You can write a pre-operation plug-in on the RetrieveMultiple message of the table and change the criteria on the query in it.</span></span> <span data-ttu-id="5c1e1-141">または、結果を返す前に結果をフィルター処理するために、操作後のプラグインを作成することもできます。</span><span class="sxs-lookup"><span data-stu-id="5c1e1-141">Alternatively, you can write a post-operation plug-in to filter the results before they're returned.</span></span>

### <a name="how-can-i-show-in-the-same-grid-data-from-multiple-virtual-tables-that-are-joined-to-a-physical-table-record-in-dataverse"></a><span data-ttu-id="5c1e1-142">Dataverse の物理テーブル レコードに結合されている複数の仮想テーブルからのデータを、同じグリッドで表示する方法はありますか?</span><span class="sxs-lookup"><span data-stu-id="5c1e1-142">How can I show, in the same grid, data from multiple virtual tables that are joined to a physical table record in Dataverse?</span></span>

<span data-ttu-id="5c1e1-143">このアプローチは、現在 Dataverse でサポートされていません。</span><span class="sxs-lookup"><span data-stu-id="5c1e1-143">This approach isn't currently possible in Dataverse.</span></span>

### <a name="if-i-want-a-default-value-to-be-entered-in-a-field-during-pre-create-will-an-initvalue-on-the-data-table-work"></a><span data-ttu-id="5c1e1-144">事前作成時にフィールドに既定値を入力する必要がある場合は、データ テーブルの initValue は機能しますか?</span><span class="sxs-lookup"><span data-stu-id="5c1e1-144">If I want a default value to be entered in a field during pre-create, will an initValue on the data table work?</span></span>

<span data-ttu-id="5c1e1-145">はい。</span><span class="sxs-lookup"><span data-stu-id="5c1e1-145">Yes.</span></span> <span data-ttu-id="5c1e1-146">呼び出しの順序を次に示します。</span><span class="sxs-lookup"><span data-stu-id="5c1e1-146">Here's the order of calls:</span></span>

1. <span data-ttu-id="5c1e1-147">Dataverse が作成または更新メッセージを送信します。</span><span class="sxs-lookup"><span data-stu-id="5c1e1-147">Dataverse sends a create or update message.</span></span>
2. <span data-ttu-id="5c1e1-148">Human Resources エンティティおよびバッキング テーブルの既存のすべてのロジックが呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="5c1e1-148">All the existing logic on the Human Resources entity and backing tables is invoked.</span></span> <span data-ttu-id="5c1e1-149">このロジックには、値を変更する可能性がある既定値のエントリが含まれています。</span><span class="sxs-lookup"><span data-stu-id="5c1e1-149">This logic includes default value entry that might change values.</span></span>
3. <span data-ttu-id="5c1e1-150">Dataverse は、既定値が入力された列を含む、データの最新のコピーを取得するための別の取得 (単一) メッセージを送信します。</span><span class="sxs-lookup"><span data-stu-id="5c1e1-150">Dataverse sends another Retrieve (single) message to get the latest copy of the data, including any columns that default values were entered for.</span></span>

### <a name="does-the-form-business-logic-in-human-resources-get-called-through-virtual-tables"></a><span data-ttu-id="5c1e1-151">Human Resources のフォーム ビジネス ロジックは、仮想テーブルを介して呼び出されますか?</span><span class="sxs-lookup"><span data-stu-id="5c1e1-151">Does the form business logic in Human Resources get called through virtual tables?</span></span>

<span data-ttu-id="5c1e1-152">フォームに存在する Human Resources ビジネス ロジックは、仮想テーブルを介して起動されることはありません。</span><span class="sxs-lookup"><span data-stu-id="5c1e1-152">Human Resources business logic on forms isn't invoked through virtual tables.</span></span> <span data-ttu-id="5c1e1-153">代わりに、同じテーブルへの OData アクセスを行う場合と同じ動作が予想されます。</span><span class="sxs-lookup"><span data-stu-id="5c1e1-153">Instead, expect the same behavior that you get through OData access to the same tables.</span></span> <span data-ttu-id="5c1e1-154">OData (つまり、**IsPublic** が **はい** に設定されているテーブル) に公開されているテーブルは、適切に保護され、データが破損しないように確認することが必要です。</span><span class="sxs-lookup"><span data-stu-id="5c1e1-154">A table exposed to OData (that is, **IsPublic** is set to **Yes**) should have appropriate protections to ensure data can't be corrupted.</span></span> <span data-ttu-id="5c1e1-155">この保護がないテーブルがある場合、この状況はテーブルのバグを表します。</span><span class="sxs-lookup"><span data-stu-id="5c1e1-155">If any table lacks this protection, that situation represents a bug in the table.</span></span> <span data-ttu-id="5c1e1-156">OData と仮想テーブル間でテーブルの動作に違いがある場合、仮想テーブル機能のバグを示しています。</span><span class="sxs-lookup"><span data-stu-id="5c1e1-156">If you see differences in table behavior between OData and virtual tables, that situation represents a bug in the virtual table feature.</span></span>

### <a name="when-adding-records-using-virtual-tables-is-there-any-way-to-use-number-sequences"></a><span data-ttu-id="5c1e1-157">仮想テーブルを使用してレコードを追加する場合、番号順序を使用する方法はありますか?</span><span class="sxs-lookup"><span data-stu-id="5c1e1-157">When adding records using virtual tables is there any way to use number sequences?</span></span>

<span data-ttu-id="5c1e1-158">はい、Human Resources テーブルで番号順序が自動生成される場合は、仮想テーブルからも同じように機能します。</span><span class="sxs-lookup"><span data-stu-id="5c1e1-158">Yes, if the Human Resources table can auto generate number sequences, then it will work the same way from the virtual table.</span></span>

### <a name="why-doesnt-search-view-work-in-power-apps"></a><span data-ttu-id="5c1e1-159">Power Apps で「検索ビュー」が機能しないのはなぜですか?</span><span class="sxs-lookup"><span data-stu-id="5c1e1-159">Why doesn't search view work in Power Apps?</span></span>

<span data-ttu-id="5c1e1-160">テーブルの簡易検索ビューに列が追加されていない場合、検索ボックスは使用できません。</span><span class="sxs-lookup"><span data-stu-id="5c1e1-160">If there are no columns added in the quick find view for the table, then the search box does nothing.</span></span> <span data-ttu-id="5c1e1-161">回避策として、テーブルの列を 1 つ以上、簡易検索ビューに追加することができます。</span><span class="sxs-lookup"><span data-stu-id="5c1e1-161">The workaround is to add one or more columns of the table to the quick find view.</span></span>

### <a name="are-custom-fields-supported-on-virtual-tables"></a><span data-ttu-id="5c1e1-162">カスタム フィールドは仮想テーブルでサポートされていますか?</span><span class="sxs-lookup"><span data-stu-id="5c1e1-162">Are custom fields supported on virtual tables?</span></span>

<span data-ttu-id="5c1e1-163">はい。カスタム フィールドは仮想テーブルでサポートされています。</span><span class="sxs-lookup"><span data-stu-id="5c1e1-163">Yes, custom fields are supported on virtual tables.</span></span> <span data-ttu-id="5c1e1-164">最初に、仮想テーブルに関連付けられているデータ エンティティにカスタム フィールドを追加する必要があります。</span><span class="sxs-lookup"><span data-stu-id="5c1e1-164">You must first add the custom field to the data entity related to the virtual table.</span></span> <span data-ttu-id="5c1e1-165">その後、仮想テーブルを生成または更新して、カスタム フィールドをスキーマに含めます。</span><span class="sxs-lookup"><span data-stu-id="5c1e1-165">You can then generate or refresh the virtual table to include the custom field in its schema.</span></span> <span data-ttu-id="5c1e1-166">データ エンティティにカスタム フィールドを追加する方法の詳細については、「[データ エンティティのカスタム フィールドを公開](../fin-ops-core/fin-ops/get-started/user-defined-fields.md?toc=%2fdynamics365%2fhuman-resources%2ftoc.json#exposing-custom-fields-on-data-entities)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="5c1e1-166">For more information on adding custom fields to data entities, see [Exposing custom fields on data entities](../fin-ops-core/fin-ops/get-started/user-defined-fields.md?toc=%2fdynamics365%2fhuman-resources%2ftoc.json#exposing-custom-fields-on-data-entities).</span></span>

### <a name="what-do-i-do-if-i-get-an-error-that-the-dynamics-365-for-talent-user-wasnt-found"></a><span data-ttu-id="5c1e1-167">Dynamics 365 for Talent ユーザーが見つからないというエラーが発生した場合、どうしたらよいですか?</span><span class="sxs-lookup"><span data-stu-id="5c1e1-167">What do I do if I get an error that the Dynamics 365 for Talent user wasn't found?</span></span>

<span data-ttu-id="5c1e1-168">**Microsoft Dataverse 統合** ページで仮想テーブルを設定すると、アクション センターに次のようなエラー メッセージが表示される場合があります。</span><span class="sxs-lookup"><span data-stu-id="5c1e1-168">When setting up virtual tables in the **Microsoft Dataverse integration** page, you may see an error message in the Action center stating the following:</span></span>

`User Dynamics365 for Talent was not found in Finance and Operations. Please ensure this user exists.`

<span data-ttu-id="5c1e1-169">このメッセージは、仮想テーブル用に設定されたアプリに対して、Human Resources アプリケーションでアクセス許可が付与されていないことを示しています。</span><span class="sxs-lookup"><span data-stu-id="5c1e1-169">This message indicates that permissions haven't been granted in Human Resources application to the app set up for virtual tables.</span></span> <span data-ttu-id="5c1e1-170">これを解決するには、[Human Resourcesでアプリのアクセス許可を付与する](./hr-admin-integration-common-data-service-virtual-entities.md#grant-app-permissions-in-human-resources) 手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="5c1e1-170">You can resolve this by completing the steps to [Grant app permissions in Human Resources](./hr-admin-integration-common-data-service-virtual-entities.md#grant-app-permissions-in-human-resources).</span></span>

### <a name="what-do-i-do-if-the-finance-and-operations-virtual-data-source-configurations-option-isnt-available-in-my-microsoft-dataverse-environment"></a><span data-ttu-id="5c1e1-171">Finance and Operations 仮想データ ソースの構成オプションを Microsoft Dataverse 環境で使用できない場合はどうしたらよいですか?</span><span class="sxs-lookup"><span data-stu-id="5c1e1-171">What do I do if the Finance and Operations Virtual Data Source Configurations option isn't available in my Microsoft Dataverse environment?</span></span>

<span data-ttu-id="5c1e1-172">仮想テーブルの設定時に Dynamics 365 HR 仮想テーブル アプリをインストールする必要があります。このアプリにより、**Finance and Operations 仮想データ ソースの構成** オプションが追加されます。</span><span class="sxs-lookup"><span data-stu-id="5c1e1-172">During the setup of the virtual tables, you need to install the Dynamics 365 HR Virtual Table app, which adds the option for **Finance and Operations Virtual Data Source Configurations**.</span></span> <span data-ttu-id="5c1e1-173">**Microsoft Dataverse 統合** ページでのアプリのインストールの詳細については、[Dataverse 仮想テーブルの構成](https://docs.microsoft.com/dynamics365/human-resources/hr-admin-integration-common-data-service-virtual-entities#install-the-dynamics-365-hr-virtual-table-app) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="5c1e1-173">For more information about installing the app in the **Microsoft Dataverse integration** page, see [Configure Dataverse virtual tables](https://docs.microsoft.com/dynamics365/human-resources/hr-admin-integration-common-data-service-virtual-entities#install-the-dynamics-365-hr-virtual-table-app).</span></span>

<span data-ttu-id="5c1e1-174">**Microsoft Dataverse 統合** ページの **仮想テーブル アプリのインストール** アクションが正常に完了しなかった場合は、Power Platform 管理センターでアクションを実行できます。</span><span class="sxs-lookup"><span data-stu-id="5c1e1-174">If the **Install virtual table app** action on the **Microsoft Dataverse integration** page doesn't complete successfully, you can perform the action in the Power Platform admin center.</span></span>

1. <span data-ttu-id="5c1e1-175">[Power Platform 管理センター](https://admin.powerplatform.microsoft.com)を開きます。</span><span class="sxs-lookup"><span data-stu-id="5c1e1-175">Open the [Power Platform admin center](https://admin.powerplatform.microsoft.com).</span></span>

2. <span data-ttu-id="5c1e1-176">**環境** の一覧で、Human Resources のインスタンスに関連付けられている Power Apps 環境を選択します。</span><span class="sxs-lookup"><span data-stu-id="5c1e1-176">In the **Environments** list, select the Power Apps environment associated with your Human Resources instance.</span></span>

3. <span data-ttu-id="5c1e1-177">ページの **リソース** セクションで、**Dynamics 365 アプリ** を選択します。</span><span class="sxs-lookup"><span data-stu-id="5c1e1-177">In the **Resources** section of the page, select **Dynamics 365 apps**.</span></span>

4. <span data-ttu-id="5c1e1-178">**アプリのインストール** アクションを選択します。</span><span class="sxs-lookup"><span data-stu-id="5c1e1-178">Select the **Install app** action.</span></span>

5. <span data-ttu-id="5c1e1-179">**Dynamics 365 HR 仮想テーブル** を選択し、**次へ** を選択します。</span><span class="sxs-lookup"><span data-stu-id="5c1e1-179">Select **Dynamics 365 HR Virtual Table**, and then select **Next**.</span></span>

6. <span data-ttu-id="5c1e1-180">サービス使用条件に同意することを確認してマークします。</span><span class="sxs-lookup"><span data-stu-id="5c1e1-180">Review and mark to agree to the terms of service.</span></span>

7. <span data-ttu-id="5c1e1-181">**インストール** を選択します。</span><span class="sxs-lookup"><span data-stu-id="5c1e1-181">Select **Install**.</span></span>

<span data-ttu-id="5c1e1-182">インストールには数分かかります。</span><span class="sxs-lookup"><span data-stu-id="5c1e1-182">The installation takes a few minutes.</span></span> <span data-ttu-id="5c1e1-183">完了すると **Finance and Operations 仮想データ ソースの構成** エンティティをこの環境で生成されます。</span><span class="sxs-lookup"><span data-stu-id="5c1e1-183">When it completes, the **Finance and Operations Virtual Data Source Configurations** entity is generated in the environment.</span></span>

<span data-ttu-id="5c1e1-184">![Power Platform 管理センターから Dynamics 365 HR 仮想テーブル アプリをインストール](./media/hr-admin-integration-virtual-entities-power-platform-install.jpg)
[!INCLUDE[footer-include](../includes/footer-banner.md)]</span><span class="sxs-lookup"><span data-stu-id="5c1e1-184">![Install the Dynamics 365 HR Virtual Table app from the Power Platform admin center](./media/hr-admin-integration-virtual-entities-power-platform-install.jpg)
[!INCLUDE[footer-include](../includes/footer-banner.md)]</span></span>
