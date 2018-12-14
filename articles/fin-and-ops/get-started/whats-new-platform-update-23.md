---
title: "Dynamics 365 for Finance and Operations プラットフォーム更新プログラム 23 (2018 年 12 月) の新機能および変更された機能"
description: "このトピックでは、Dynamics 365 for Finance and Operations プラットフォーム更新プログラム 23 (2018 年 12 月) の新機能または変更された機能について説明します。"
author: tonyafehr
manager: AnnBe
ms.date: 12/04/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Developer, IT Pro
ms.reviewer: tfehr
ms.search.scope: Operations
ms.custom: 
ms.assetid: 
ms.search.region: Global
ms.author: tfehr
ms.search.validFrom: 2018-12-31
ms.dyn365.ops.version: Platform 23
ms.translationtype: HT
ms.sourcegitcommit: 99c10649d7683265fcac86c1825c5a965bbdb415
ms.openlocfilehash: 9dd6394133890bbc9a97c6cb512313e4052c1e4b
ms.contentlocale: ja-jp
ms.lasthandoff: 12/04/2018

---
# <a name="whats-new-or-changed-in-dynamics-365-for-finance-and-operations-platform-update-23-december-2018"></a><span data-ttu-id="c5d79-103">Dynamics 365 for Finance and Operations プラットフォーム更新プログラム 23 (2018 年 12 月) の新機能および変更された機能</span><span class="sxs-lookup"><span data-stu-id="c5d79-103">What's new or changed in Dynamics 365 for Finance and Operations platform update 23 (December 2018)</span></span>

[!include [banner](../includes/banner.md)]
[!include [banner](../includes/preview-banner.md)]

<span data-ttu-id="c5d79-104">このトピックでは、Dynamics 365 for Finance and Operations プラットフォーム更新プログラム 23 の新機能または変更された機能について説明します。</span><span class="sxs-lookup"><span data-stu-id="c5d79-104">This topic describes features that are either new or changed in Dynamics 365 for Finance and Operations platform update 23.</span></span> <span data-ttu-id="c5d79-105">このバージョンは、7.0.5126 のビルド番号を持ちます。</span><span class="sxs-lookup"><span data-stu-id="c5d79-105">This version has a build number of 7.0.5126.</span></span>

### <a name="dynamics-365-october-18-release-notes"></a><span data-ttu-id="c5d79-106">Dynamics 365 2018 年 10 月リリース ノート</span><span class="sxs-lookup"><span data-stu-id="c5d79-106">Dynamics 365 October '18 release notes</span></span>
<span data-ttu-id="c5d79-107">当社のビジネス アプリやプラットフォームの次回および最近リリースされた機能について検討中ですか?</span><span class="sxs-lookup"><span data-stu-id="c5d79-107">Wondering about upcoming and recently released capabilities in any of our business apps or platform?</span></span> 

<span data-ttu-id="c5d79-108">[2018 年 10 月リリース ノートを確認](https://go.microsoft.com/fwlink/?linkid=870424).</span><span class="sxs-lookup"><span data-stu-id="c5d79-108">[Check out the October '18 release notes](https://go.microsoft.com/fwlink/?linkid=870424).</span></span> <span data-ttu-id="c5d79-109">あらゆる詳細情報を端から端まで徹底的に捕捉して一元化しました。計画を策定する際に 1 つのドキュメントでそれらの情報を参照できます。</span><span class="sxs-lookup"><span data-stu-id="c5d79-109">We've captured all the details, end to end, top to bottom, in a single document that you can use for planning.</span></span> 

### <a name="platform-update-23-bug-fixes"></a><span data-ttu-id="c5d79-110">プラットフォーム アップデート 23 のバグ修正プログラム</span><span class="sxs-lookup"><span data-stu-id="c5d79-110">Platform update 23 bug fixes</span></span>
<span data-ttu-id="c5d79-111">プラットフォーム更新 23 の一部である更新プログラムのそれぞれに含まれるバグ修正については、Lifecycle Services (LCS) にログインし、この [KB 資料](https://go.microsoft.com/fwlink/?linkid=) (**未公開**) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="c5d79-111">For information about the bug fixes included in each of the updates that are part of Platform update 23, sign in to Lifecycle Services (LCS) and view this [KB article](https://go.microsoft.com/fwlink/?linkid=) (**not yet available**).</span></span>

## <a name="legal-entity-filtering-using-grid-column-headers"></a><span data-ttu-id="c5d79-112">グリッド列ヘッダーを使用した法人のフィルター処理</span><span class="sxs-lookup"><span data-stu-id="c5d79-112">Legal entity filtering using grid column headers</span></span>
<span data-ttu-id="c5d79-113">プラットフォーム更新プログラム 23 以降、会社間クエリを含むグリッドでは、グリッド内の他の列と同様、列ドロップダウン メニューを使用して、ユーザーが *法人* 列をフィルター処理できます。</span><span class="sxs-lookup"><span data-stu-id="c5d79-113">Starting in Platform update 23, for grids with cross-company queries, users are able to filter the *Legal entity* column using the column drop-down menu, similar to other columns in the grid.</span></span> <span data-ttu-id="c5d79-114">たとえば、ユーザーが特定の顧客のグローバル トランザクションを見ているとき、会社の小さいサブセット内のトランザクションを検索することがあります。</span><span class="sxs-lookup"><span data-stu-id="c5d79-114">For example, if a user is looking at the global transactions for a specific customer, he might want to find the transactions within a small subset of companies.</span></span> <span data-ttu-id="c5d79-115">この機能が追加される前は、[フィルターまたは並べ替えの編集] ダイアログ ボックスの [顧客範囲] タブを使用してフィルタ処理するか、ページ固有のカスタム フィルターを使用する必要がありました。</span><span class="sxs-lookup"><span data-stu-id="c5d79-115">Prior to this feature, he would have had to filter using the Customer range tab on the Advanced filter or sort dialog box, or utilize page-specific custom filters.</span></span>

<span data-ttu-id="c5d79-116">![法人によるフィルター処理](media/legalEntityFiltering.png  "法人によるフィルター処理")</span><span class="sxs-lookup"><span data-stu-id="c5d79-116">![Filter by legal entity](media/legalEntityFiltering.png  "Filter by legal entity")</span></span>

## <a name="export-to-excel"></a><span data-ttu-id="c5d79-117">Excel にエクスポート</span><span class="sxs-lookup"><span data-stu-id="c5d79-117">Export to Excel</span></span>
<span data-ttu-id="c5d79-118">プラットフォーム更新プログラム 22 では、Excel へのエクスポート機能は、Finance and Operations のグリッドから最大 100 万行をエクスポートできるように強化されました。以前の 10,000 行の制限から大幅に上昇しました。</span><span class="sxs-lookup"><span data-stu-id="c5d79-118">In Platform update 22, the Export to Excel feature was improved to allow users to export up to 1 million rows from a grid in Finance and Operations, a substantial increase from the previous 10,000-row limit.</span></span> 

<span data-ttu-id="c5d79-119">プラットフォーム更新プログラム 23 では、この機能の強化を継続しました。</span><span class="sxs-lookup"><span data-stu-id="c5d79-119">In Platform update 23, we've continued to enhance this feature.</span></span> <span data-ttu-id="c5d79-120">エクスポートが完了すると、エクスポートが完了したことを知らせる通知がアクション センターに届くようになりました。</span><span class="sxs-lookup"><span data-stu-id="c5d79-120">After the export completes, users will now receive a notification in the Action center alerting them that the export has finished.</span></span> <span data-ttu-id="c5d79-121">通知には、エクスポートされたデータを含む Excel ファイルをダウンロードするためのリンクが含まれています。</span><span class="sxs-lookup"><span data-stu-id="c5d79-121">The notification includes a link to download the Excel file containing the exported data.</span></span> <span data-ttu-id="c5d79-122">リンクと通知には、エクスポートが完了した後、約 3 日間アクセスできます。</span><span class="sxs-lookup"><span data-stu-id="c5d79-122">The link and notification are accessible for approximately three days after the export completes.</span></span> 

## <a name="manage-access-to-network-printers-across-legal-entities"></a><span data-ttu-id="c5d79-123">法人間でのネットワーク プリンターへのアクセスの管理</span><span class="sxs-lookup"><span data-stu-id="c5d79-123">Manage access to network printers across legal entities</span></span>
<span data-ttu-id="c5d79-124">新しいシステム管理ユーティリティへのアクセスは、Carbon Flighting Service によって管理されます。</span><span class="sxs-lookup"><span data-stu-id="c5d79-124">Access to the new System administration utility is managed by the Carbon Flighting Service.</span></span> <span data-ttu-id="c5d79-125">プラットフォーム更新プログラム 23 には、ネットワーク プリンターを Dynamics 365 for Finance and Operations に登録するためのドキュメント回覧エージェント (DRA) と共に、システム管理者が使用できる**システム ネットワーク プリンター管理**フォームが含まれています。</span><span class="sxs-lookup"><span data-stu-id="c5d79-125">Platform update 23 includes the **System network printers management** form that System Administrators can use, along with the Document Routing Agent (DRA) to register network printers with Dynamics 365 for Finance and Operations.</span></span>

<span data-ttu-id="c5d79-126">この機能を有効にすると、**プレビュー** リンクが **システム ネットワーク プリンター** フォームに表示されます (**組織管理** > **設定** > **ネットワーク プリンター** で **システム ネットワーク プリンター** をクリック)。</span><span class="sxs-lookup"><span data-stu-id="c5d79-126">After you have enabled this feature, a **Preview** link will appear on the **System network printers** form (**Organization administration** > **Setup** > **Network printers** and click **System network printers**).</span></span> <span data-ttu-id="c5d79-127">DRA を使用してネットワーク プリンターをサービスに登録すると、組織の各法人の構成情報が表示されます。</span><span class="sxs-lookup"><span data-stu-id="c5d79-127">After you register the network printers with the service using the DRA, you will see the configuration information for each legal entity in the organization.</span></span>

## <a name="enabling-index-hints-in-x-again"></a><span data-ttu-id="c5d79-128">X++ でのインデックス ヒントの再有効化</span><span class="sxs-lookup"><span data-stu-id="c5d79-128">Enabling index hints in X++ again</span></span>
<span data-ttu-id="c5d79-129">Microsoft Dynamics AX 2009 以前のバージョンでは、X++ からのインデックス ヒントがサポートされていました。</span><span class="sxs-lookup"><span data-stu-id="c5d79-129">Microsoft Dynamics AX 2009 and earlier versions supported INDEX HINTS from X++.</span></span> <span data-ttu-id="c5d79-130">ただし、Dynamics AX 2012 のリリース時にこれは非推奨になりました。</span><span class="sxs-lookup"><span data-stu-id="c5d79-130">However, this was deprecated when Dynamics AX 2012 was released.</span></span> <span data-ttu-id="c5d79-131">詳細については、[非推奨: X++ インデックス ヒント句](https://docs.microsoft.com/dynamicsax-2012/appuser-itpro/deprecated-x-index-hint-clause)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="c5d79-131">For more information, see [Deprecated: X++ index hint clause](https://docs.microsoft.com/dynamicsax-2012/appuser-itpro/deprecated-x-index-hint-clause).</span></span>

<span data-ttu-id="c5d79-132">これが非推奨になった主な理由は、誤ったインデックス ヒットによってクエリが破損し、クエリを解決するまでほとんど実行できないことでした。</span><span class="sxs-lookup"><span data-stu-id="c5d79-132">One of the main reasons this was deprecated was because a misguided index hit could damage the queries and little could be done until the query is fixed.</span></span> <span data-ttu-id="c5d79-133">現在では、数百のテナントに数千のクエリが表示され、一部のシンプルなクエリのあまり最適でないプランと共に SQL が表示されると、Finance and Operations が X++ ヒントを戻したことになります。</span><span class="sxs-lookup"><span data-stu-id="c5d79-133">Now, after seeing thousands of queries in hundreds of tenants and seeing SQL come up with less optimal plans for some simple queries, Finance and Operations has brought back X++ hints.</span></span> <span data-ttu-id="c5d79-134">しかし、X++ ヒントは特別な注意を払って使用してください。</span><span class="sxs-lookup"><span data-stu-id="c5d79-134">However, X++ hints should only be used with extremem caution.</span></span>  

<span data-ttu-id="c5d79-135">既定の動作 **False** を持つ一般的な **allowIndexHint** の新しい API を追加しました。</span><span class="sxs-lookup"><span data-stu-id="c5d79-135">We have added a new API on common **allowIndexHint** with a default behavior of **False**.</span></span> <span data-ttu-id="c5d79-136">これにより、開発者はインデックス ヒントをオプトインして明示的に有効にできます。</span><span class="sxs-lookup"><span data-stu-id="c5d79-136">This allows developers to opt-in and explicitly enable index hint.</span></span> <span data-ttu-id="c5d79-137">インデックス ヒントを指定するための select ステートメントの古い構文が再利用されます。</span><span class="sxs-lookup"><span data-stu-id="c5d79-137">The old syntax on the select statement for specifying index hint is reused.</span></span>
<span data-ttu-id="c5d79-138">インデックス ヒントを指定する既存の X++ コードがある場合、新しい API が呼び出されるまで現在の動作は変更されません。</span><span class="sxs-lookup"><span data-stu-id="c5d79-138">If there is an existing X++ code that specifies index hint, there is no change to the current behavior until the new API is invoked.</span></span> <span data-ttu-id="c5d79-139">詳細については、次の例を参照してください。</span><span class="sxs-lookup"><span data-stu-id="c5d79-139">See the following example for details.</span></span>

    public void testIndexHintRegularTable()
        {
            SysDataAccessDBLogTestTable tbl1;
            tbl1.allowIndexHint(true);
            select generateonly tbl1 index hint PrimaryKeyIdx where tbl1.description == ''; // Send index hint to SQL server
         ………..

        }

> [!NOTE]
> <span data-ttu-id="c5d79-140">インデックス ヒントは、悪影響よりもメリットの方が多いことが確信できるときのみ、慎重に使用してください。</span><span class="sxs-lookup"><span data-stu-id="c5d79-140">Index hints should be used sparingly, and only when you can ensure that it causes more benefit than harm.</span></span> <span data-ttu-id="c5d79-141">新しい API により、知識と経験が豊富な開発者が必要なときに適切なヒントを渡すことができるようになります。</span><span class="sxs-lookup"><span data-stu-id="c5d79-141">With the new API, knowledgeable power developers are empowered to pass the right hints when needed.</span></span> <span data-ttu-id="c5d79-142">経験豊富な開発者は、注意してこの新しい機能を使用してください。</span><span class="sxs-lookup"><span data-stu-id="c5d79-142">Power developers should use this new feature with caution.</span></span> <span data-ttu-id="c5d79-143">疑わしい場合は、インデックス ヒントを使用しないでください。</span><span class="sxs-lookup"><span data-stu-id="c5d79-143">When in doubt, avoid using index hints.</span></span>

