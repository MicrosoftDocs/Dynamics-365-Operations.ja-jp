---
title: Dynamics 365 for Finance and Operations プラットフォーム更新プログラム 23 (2019 年 1 月) の新機能および変更された機能
description: このトピックでは、Dynamics 365 for Finance and Operation プラットフォーム更新プログラム 23 (2019 年 1 月) の新機能または変更された機能について説明します。
author: tonyafehr
manager: AnnBe
ms.date: 11/20/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Developer, IT Pro
ms.reviewer: josaw
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: tfehr
ms.search.validFrom: 2018-12-31
ms.dyn365.ops.version: Platform 23
ms.openlocfilehash: 83755747608e4f63f1de4c16c698c39ff01f88ea
ms.sourcegitcommit: f5e31c34640add6d40308ac1365cc0ee60e60e24
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 12/08/2020
ms.locfileid: "4694106"
---
# <a name="whats-new-or-changed-in-dynamics-365-for-finance-and-operations-platform-update-23-january-2019"></a><span data-ttu-id="e772c-103">Dynamics 365 for Finance and Operations プラットフォーム更新プログラム 23 (2019 年 1 月) の新機能および変更された機能</span><span class="sxs-lookup"><span data-stu-id="e772c-103">What's new or changed in Dynamics 365 for Finance and Operations platform update 23 (January 2019)</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="e772c-104">このトピックでは、Dynamics 365 for Finance and Operations プラットフォーム更新プログラム 23 の新機能または変更された機能について説明します。</span><span class="sxs-lookup"><span data-stu-id="e772c-104">This topic describes features that are either new or changed in Dynamics 365 for Finance and Operations platform update 23.</span></span> <span data-ttu-id="e772c-105">このバージョンは、7.0.5126 のビルド番号を持ちます。</span><span class="sxs-lookup"><span data-stu-id="e772c-105">This version has a build number of 7.0.5126.</span></span>

### <a name="dynamics-365-october-18-release-notes"></a><span data-ttu-id="e772c-106">Dynamics 365 2018 年 10 月リリース ノート</span><span class="sxs-lookup"><span data-stu-id="e772c-106">Dynamics 365 October '18 release notes</span></span>

<span data-ttu-id="e772c-107">当社のビジネス アプリやプラットフォームの次回および最近リリースされた機能について検討中ですか?</span><span class="sxs-lookup"><span data-stu-id="e772c-107">Wondering about upcoming and recently released capabilities in any of our business apps or platform?</span></span>

<span data-ttu-id="e772c-108">[2018 年 10 月リリース ノートを確認](https://go.microsoft.com/fwlink/?linkid=870424).</span><span class="sxs-lookup"><span data-stu-id="e772c-108">[Check out the October '18 release notes](https://go.microsoft.com/fwlink/?linkid=870424).</span></span> <span data-ttu-id="e772c-109">あらゆる詳細情報を端から端まで徹底的に捕捉して一元化しました。計画を策定する際に 1 つのドキュメントでそれらの情報を参照できます。</span><span class="sxs-lookup"><span data-stu-id="e772c-109">We've captured all the details, end to end, top to bottom, in a single document that you can use for planning.</span></span>

### <a name="platform-update-23-bug-fixes"></a><span data-ttu-id="e772c-110">プラットフォーム アップデート 23 のバグ修正プログラム</span><span class="sxs-lookup"><span data-stu-id="e772c-110">Platform update 23 bug fixes</span></span>

<span data-ttu-id="e772c-111">プラットフォーム更新 23 の一部である更新プログラムのそれぞれに含まれるバグ修正については、Lifecycle Services (LCS) にログインし、この [KB 資料](https://go.microsoft.com/fwlink/?linkid=2049368)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="e772c-111">For information about the bug fixes included in each of the updates that are part of Platform update 23, sign in to Lifecycle Services (LCS) and view this [KB article](https://go.microsoft.com/fwlink/?linkid=2049368).</span></span>

## <a name="legal-entity-filtering-using-grid-column-headers"></a><span data-ttu-id="e772c-112">グリッド列ヘッダーを使用した法人のフィルター処理</span><span class="sxs-lookup"><span data-stu-id="e772c-112">Legal entity filtering using grid column headers</span></span>

<span data-ttu-id="e772c-113">プラットフォーム更新プログラム 23 以降、会社間クエリを含むグリッドでは、グリッド内の他の列と同様、列ドロップダウン メニューを使用して、ユーザーが *法人* 列をフィルター処理できます。</span><span class="sxs-lookup"><span data-stu-id="e772c-113">Starting in Platform update 23, for grids with cross-company queries, users are able to filter the *Legal entity* column using the column drop-down menu, similar to other columns in the grid.</span></span> <span data-ttu-id="e772c-114">たとえば、ユーザーが特定の顧客のグローバル トランザクションを見ているとき、会社の小さいサブセット内のトランザクションを検索することがあります。</span><span class="sxs-lookup"><span data-stu-id="e772c-114">For example, if users are looking at the global transactions for a specific customer, they might want to find the transactions within a small subset of companies.</span></span> <span data-ttu-id="e772c-115">この機能が追加される前は、フィルターまたは並べ替えの編集ダイアログ ボックスの顧客範囲タブを使用してフィルター処理するか、ページ固有のカスタム フィルターを使用する必要がありました。</span><span class="sxs-lookup"><span data-stu-id="e772c-115">Prior to this feature, users would have had to filter using the Customer range tab on the Advanced filter or sort dialog box, or utilize page-specific custom filters.</span></span>

<span data-ttu-id="e772c-116">![法人によるフィルター](media/legalEntityFiltering.png "法人によるフィルター")</span><span class="sxs-lookup"><span data-stu-id="e772c-116">![Filter by legal entity](media/legalEntityFiltering.png "Filter by legal entity")</span></span>

## <a name="export-to-excel"></a><span data-ttu-id="e772c-117">Excel にエクスポート</span><span class="sxs-lookup"><span data-stu-id="e772c-117">Export to Excel</span></span>

<span data-ttu-id="e772c-118">プラットフォーム更新プログラム 22 では、Excel へのエクスポート機能は、Finance and Operations のグリッドから最大 100 万行をエクスポートできるように強化されました。以前の 10,000 行の制限から大幅に上昇しました。</span><span class="sxs-lookup"><span data-stu-id="e772c-118">In Platform update 22, the Export to Excel feature was improved to allow users to export up to 1 million rows from a grid in Finance and Operations, a substantial increase from the previous 10,000-row limit.</span></span>

<span data-ttu-id="e772c-119">プラットフォーム更新プログラム 23 では、この機能の強化を継続しました。</span><span class="sxs-lookup"><span data-stu-id="e772c-119">In Platform update 23, we've continued to enhance this feature.</span></span> <span data-ttu-id="e772c-120">エクスポートが完了すると、エクスポートが完了したことを知らせる通知がアクション センターに届くようになりました。</span><span class="sxs-lookup"><span data-stu-id="e772c-120">After the export completes, users will now receive a notification in the Action center alerting them that the export has finished.</span></span> <span data-ttu-id="e772c-121">通知には、エクスポートされたデータを含む Excel ファイルをダウンロードするためのリンクが含まれています。</span><span class="sxs-lookup"><span data-stu-id="e772c-121">The notification includes a link to download the Excel file containing the exported data.</span></span> <span data-ttu-id="e772c-122">リンクと通知には、エクスポートが完了した後、約 3 日間アクセスできます。</span><span class="sxs-lookup"><span data-stu-id="e772c-122">The link and notification are accessible for approximately three days after the export completes.</span></span>

## <a name="manage-access-to-network-printers-across-legal-entities"></a><span data-ttu-id="e772c-123">法人間でのネットワーク プリンターへのアクセスの管理</span><span class="sxs-lookup"><span data-stu-id="e772c-123">Manage access to network printers across legal entities</span></span>

<span data-ttu-id="e772c-124">プラットフォーム更新プログラム 23 には、ネットワーク プリンターを Dynamics 365 for Finance and Operations に登録するためのドキュメント回覧エージェント (DRA) と共に、システム管理者が使用できる **システム ネットワーク プリンター管理** フォームが含まれています。</span><span class="sxs-lookup"><span data-stu-id="e772c-124">Platform update 23 includes the **System network printers management** form that System Administrators can use, along with the Document Routing Agent (DRA) to register network printers with Dynamics 365 for Finance and Operations.</span></span>

<span data-ttu-id="e772c-125">この機能を有効にすると、**プレビュー** リンクが **システム ネットワーク プリンター** フォームに表示されます (**組織管理** \> **設定** \> **ネットワーク プリンター** で **システム ネットワーク プリンター** をクリック)。</span><span class="sxs-lookup"><span data-stu-id="e772c-125">After you have enabled this feature, a **Preview** link will appear on the **System network printers** form (**Organization administration** \> **Setup** \> **Network printers** and click **System network printers**).</span></span>

<span data-ttu-id="e772c-126">DRA を使用してネットワーク プリンターをサービスに登録すると、組織の各法人の構成情報が表示されます。</span><span class="sxs-lookup"><span data-stu-id="e772c-126">After you register the network printers with the service using the DRA, you will see the configuration information for each legal entity in the organization.</span></span>

## <a name="enabling-index-hints-in-x-again"></a><span data-ttu-id="e772c-127">X++ でのインデックス ヒントの再有効化</span><span class="sxs-lookup"><span data-stu-id="e772c-127">Enabling index hints in X++ again</span></span>

<span data-ttu-id="e772c-128">Microsoft Dynamics AX 2009 以前のバージョンでは、X++ からのインデックス ヒントがサポートされていました。</span><span class="sxs-lookup"><span data-stu-id="e772c-128">Microsoft Dynamics AX 2009 and earlier versions supported INDEX HINTS from X++.</span></span> <span data-ttu-id="e772c-129">ただし、Dynamics AX 2012 のリリース時にこれは非推奨になりました。</span><span class="sxs-lookup"><span data-stu-id="e772c-129">However, this was deprecated when Dynamics AX 2012 was released.</span></span> <span data-ttu-id="e772c-130">詳細については、[非推奨: X++ インデックス ヒント句](https://docs.microsoft.com/dynamicsax-2012/appuser-itpro/deprecated-x-index-hint-clause)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="e772c-130">For more information, see [Deprecated: X++ index hint clause](https://docs.microsoft.com/dynamicsax-2012/appuser-itpro/deprecated-x-index-hint-clause).</span></span>

<span data-ttu-id="e772c-131">これが非推奨になった主な理由は、誤ったインデックス ヒットによってクエリが破損し、クエリを解決するまでほとんど実行できないことでした。</span><span class="sxs-lookup"><span data-stu-id="e772c-131">One of the main reasons this was deprecated was because a misguided index hit could damage the queries and little could be done until the query is fixed.</span></span> <span data-ttu-id="e772c-132">現在では、数百のテナントに数千のクエリが表示され、一部のシンプルなクエリのあまり最適でないプランと共に SQL が表示されると、Finance and Operations が X++ ヒントを戻したことになります。</span><span class="sxs-lookup"><span data-stu-id="e772c-132">Now, after seeing thousands of queries in hundreds of tenants and seeing SQL come up with less optimal plans for some simple queries, Finance and Operations has brought back X++ hints.</span></span> <span data-ttu-id="e772c-133">ただし、X++ ヒントは特別な注意を払って使用してください。</span><span class="sxs-lookup"><span data-stu-id="e772c-133">However, X++ hints should only be used with extreme caution.</span></span>

<span data-ttu-id="e772c-134">既定の動作 **False** を持つ一般的な **allowIndexHint** の新しい API を追加しました。</span><span class="sxs-lookup"><span data-stu-id="e772c-134">We have added a new API on common **allowIndexHint** with a default behavior of **False**.</span></span> <span data-ttu-id="e772c-135">これにより、開発者はインデックス ヒントをオプトインして明示的に有効にできます。</span><span class="sxs-lookup"><span data-stu-id="e772c-135">This allows developers to opt-in and explicitly enable index hint.</span></span> <span data-ttu-id="e772c-136">インデックス ヒントを指定するための select ステートメントの古い構文が再利用されます。</span><span class="sxs-lookup"><span data-stu-id="e772c-136">The old syntax on the select statement for specifying index hint is reused.</span></span>

<span data-ttu-id="e772c-137">インデックス ヒントを指定する既存の X++ コードがある場合、新しい API が呼び出されるまで現在の動作は変更されません。</span><span class="sxs-lookup"><span data-stu-id="e772c-137">If there is an existing X++ code that specifies index hint, there is no change to the current behavior until the new API is invoked.</span></span> <span data-ttu-id="e772c-138">詳細については、次の例を参照してください。</span><span class="sxs-lookup"><span data-stu-id="e772c-138">See the following example for details.</span></span>

```xpp
public void testIndexHintRegularTable()
{
    SysDataAccessDBLogTestTable tbl1;
    tbl1.allowIndexHint(true);
    select generateonly tbl1 index hint PrimaryKeyIdx where tbl1.description == ''; // Send index hint to SQL server
    ...
}
```

> [!NOTE]
> <span data-ttu-id="e772c-139">インデックス ヒントは、悪影響よりもメリットの方が多いことが確信できるときのみ、慎重に使用してください。</span><span class="sxs-lookup"><span data-stu-id="e772c-139">Index hints should be used sparingly, and only when you can ensure that it causes more benefit than harm.</span></span> <span data-ttu-id="e772c-140">新しい API により、知識と経験が豊富な開発者が必要なときに適切なヒントを渡すことができるようになります。</span><span class="sxs-lookup"><span data-stu-id="e772c-140">With the new API, knowledgeable power developers are empowered to pass the right hints when needed.</span></span> <span data-ttu-id="e772c-141">経験豊富な開発者は、注意してこの新しい機能を使用してください。</span><span class="sxs-lookup"><span data-stu-id="e772c-141">Power developers should use this new feature with caution.</span></span> <span data-ttu-id="e772c-142">疑わしい場合は、インデックス ヒントを使用しないでください。</span><span class="sxs-lookup"><span data-stu-id="e772c-142">When in doubt, avoid using index hints.</span></span>

## <a name="automated-refresh-of-entity-store-opt-in"></a><span data-ttu-id="e772c-143">エンティティ格納の自動化更新 (オプトイン)</span><span class="sxs-lookup"><span data-stu-id="e772c-143">Automated refresh of Entity store (opt-in)</span></span>
<span data-ttu-id="e772c-144">更新を自分でスケジュールする代わりに、システムにエンティティ格納の更新を管理させることができます。</span><span class="sxs-lookup"><span data-stu-id="e772c-144">You can let the system manage Entity store refresh instead of scheduling the refresh yourself.</span></span> <span data-ttu-id="e772c-145">有効にすると、更新パターン (1 時間毎、1 日 2 回、毎日、または毎週) を選択できます。</span><span class="sxs-lookup"><span data-stu-id="e772c-145">When enabled, you can choose a refresh pattern (hourly, twice a day, daily, or weekly).</span></span> <span data-ttu-id="e772c-146">指定すると、システムは選択されたパターンでエンティティ格納を更新します。</span><span class="sxs-lookup"><span data-stu-id="e772c-146">When specified, the system keeps the entity store updated for the selected pattern.</span></span> <span data-ttu-id="e772c-147">システムはまた、新しい更新フォームに切り替え、ここでステータスと更新の問題が通知されます。</span><span class="sxs-lookup"><span data-stu-id="e772c-147">The system will also switch to the new update form, where you will be notified with a status and possible refresh issues.</span></span> <span data-ttu-id="e772c-148">詳細については、[エンティティ格納の自動化更新](../../dev-itpro/analytics/automated-entity-store-refresh.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="e772c-148">For more information, see [Automated Entity store refresh](../../dev-itpro/analytics/automated-entity-store-refresh.md).</span></span>

## <a name="entity-store-as-a-data-lake-private-preview"></a><span data-ttu-id="e772c-149">Data Lake としてのエンティティ格納 (プライベート プレビュー)</span><span class="sxs-lookup"><span data-stu-id="e772c-149">Entity store as a Data Lake (private preview)</span></span>
<span data-ttu-id="e772c-150">プラットフォーム更新プログラム 23 では、エンティティ格納を Data Lake として選択できます。</span><span class="sxs-lookup"><span data-stu-id="e772c-150">In Platform update 23, you can select to use Entity store as a Data Lake.</span></span> <span data-ttu-id="e772c-151">この機能が有効になると、エンティティ格納データは、Microsoft サブスクリプションでリレーショナル エンティティ格納データベースに入力されません。</span><span class="sxs-lookup"><span data-stu-id="e772c-151">When this feature is turned on, Entity store data isn't populated in the relational Entity store database in the Microsoft subscription.</span></span> <span data-ttu-id="e772c-152">代わりに、独自のサブスクリプションの Azure Data Lake Storage Gen2 アカウントに入力されます。</span><span class="sxs-lookup"><span data-stu-id="e772c-152">Instead, it's populated in an Azure Data Lake Storage Gen2 account in your own subscription.</span></span> <span data-ttu-id="e772c-153">PowerBI.com およびその他の Azure ツールのすべての機能をエンティティ格納で使用できます。</span><span class="sxs-lookup"><span data-stu-id="e772c-153">You can use the full capabilities of PowerBI.com and other Azure tools to work with Entity store.</span></span> <span data-ttu-id="e772c-154">この機能をプレビューして使用するには、[Insider プログラム](https://experience.dynamics.com/insider)に是非ご参加ください。</span><span class="sxs-lookup"><span data-stu-id="e772c-154">To preview and use this functionality, join the [Insider program](https://experience.dynamics.com/insider).</span></span>

## <a name="extensibility-enhancements"></a><span data-ttu-id="e772c-155">拡張性の強化</span><span class="sxs-lookup"><span data-stu-id="e772c-155">Extensibility enhancements</span></span>
<span data-ttu-id="e772c-156">プラットフォーム更新プログラム 23 に含まれる[プラットフォーム拡張機能の 4 番目の波](https://docs.microsoft.com/business-applications-release-notes/October18/dynamics365-finance-operations/platform-extensibility4)は、2018 年 10 月リリース ノートにドキュメントされています。</span><span class="sxs-lookup"><span data-stu-id="e772c-156">The [fourth wave of platform extensibility enhancements](https://docs.microsoft.com/business-applications-release-notes/October18/dynamics365-finance-operations/platform-extensibility4), included in Platform update 23, are documented in the October 2018 Release notes.</span></span> <span data-ttu-id="e772c-157">6 つの強化機能が詳細に説明されており、ハイライトの 1 つはクエリ データソースへの新しいリレーションの追加です。</span><span class="sxs-lookup"><span data-stu-id="e772c-157">There are six enhancements detailed, with one of the highlights being that we now allow adding new relations to query datasources.</span></span>
