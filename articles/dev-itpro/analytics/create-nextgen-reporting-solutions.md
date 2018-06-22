---
title: "レポート ソリューションの作成"
description: "このチュートリアルでは、データをエクスポートしてレポートを作成する方法、定義済みのビューを展開してチャートにナビゲーションを追加する方法、フリーフォームのレポート デザイナーを使用する方法、およびパラメータの操作方法をカスタマイズする方法について説明します。"
author: TJVass
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Developer
ms.reviewer: robinr
ms.search.scope: Operations
ms.custom: 21551
ms.assetid: 2e1c96f8-46c9-428e-bb3d-6791f2a954ef
ms.search.region: Global
ms.author: tjvass
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: 76151c6559c769c3cde37538089a1364dee08286
ms.contentlocale: ja-jp
ms.lasthandoff: 05/08/2018

---

# <a name="create-reporting-solutions"></a><span data-ttu-id="9d27a-103">レポート ソリューションの作成</span><span class="sxs-lookup"><span data-stu-id="9d27a-103">Create reporting solutions</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="9d27a-104">このチュートリアルでは、データをエクスポートしてレポートを作成する方法、定義済みのビューを展開してチャートにナビゲーションを追加する方法、フリーフォームのレポート デザイナーを使用する方法、およびパラメータの操作方法をカスタマイズする方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="9d27a-104">This tutorial shows how to export data and create a report, expand predefined views and add navigation to charts, use the free-form report designer, and customize the parameter experience.</span></span>

<a name="prerequisites"></a><span data-ttu-id="9d27a-105">前提条件</span><span class="sxs-lookup"><span data-stu-id="9d27a-105">Prerequisites</span></span>
-------------

<span data-ttu-id="9d27a-106">このチュートリアルでは、Microsoft Dynamics 365 for Finance and Operations 環境にアクセスし、インスタンスの管理者としてプロビジョニングされる必要があります。</span><span class="sxs-lookup"><span data-stu-id="9d27a-106">For this tutorial, you must access the Microsoft Dynamics 365 for Finance and Operations environment, and you must be provisioned as an administrator on the instance.</span></span>

## <a name="key-concepts"></a><span data-ttu-id="9d27a-107">重要な概念</span><span class="sxs-lookup"><span data-stu-id="9d27a-107">Key concepts</span></span>
-   <span data-ttu-id="9d27a-108">Finance and Operations でレポートを作成および使用するさまざまな方法を説明する</span><span class="sxs-lookup"><span data-stu-id="9d27a-108">Describe the various ways reports can be created and consumed in Finance and Operations</span></span>
-   <span data-ttu-id="9d27a-109">フォームおよびワークスペースの埋め込みの集計レポートへの対話機能の追加</span><span class="sxs-lookup"><span data-stu-id="9d27a-109">Add interactivity to embedded aggregate reports in forms and workspaces</span></span>
-   <span data-ttu-id="9d27a-110">フレームワーク拡張を使用して、SSRS ベースのビジネス文書のパラメーター エクスペリエンスをカスタマイズする</span><span class="sxs-lookup"><span data-stu-id="9d27a-110">Use framework extensions to customize the parameter experience for SSRS based business documents</span></span>
-   <span data-ttu-id="9d27a-111">Microsoft Excel を含む外部のツールを使用してレポートを作成するリスト ページのデータをエクスポート</span><span class="sxs-lookup"><span data-stu-id="9d27a-111">Export List Page data to create reports with external tools including Microsoft Excel</span></span>
-   <span data-ttu-id="9d27a-112">Visual Studio 2015 で強化された開発ツールを使用して最新のレポート デザインを作成する</span><span class="sxs-lookup"><span data-stu-id="9d27a-112">Author modern report designs using enhanced developer tooling in Visual Studio 2015</span></span>

## <a name="whats-new-in-reporting"></a><span data-ttu-id="9d27a-113">レポートの新機能とは</span><span class="sxs-lookup"><span data-stu-id="9d27a-113">What's new in Reporting?</span></span>
-   <span data-ttu-id="9d27a-114">AX フォームおよびレポートへの埋め込みレポート ドリルスルー ナビゲーション</span><span class="sxs-lookup"><span data-stu-id="9d27a-114">Embedded report drill-through navigations to AX forms and reports</span></span>
-   <span data-ttu-id="9d27a-115">埋め込みレポートのドリルダウン リンクを使用したレポート間の移動</span><span class="sxs-lookup"><span data-stu-id="9d27a-115">Navigate between reports using embedded report drill-through links</span></span>
-   <span data-ttu-id="9d27a-116">ユーザー設定の印刷設定のサポートを含む複数のドキュメント ルーティング サービスの拡張機能</span><span class="sxs-lookup"><span data-stu-id="9d27a-116">Several Document Routing Service enhancements including support for custom print settings</span></span>
-   <span data-ttu-id="9d27a-117">導入されたドキュメント ブランド管理の管理ツール</span><span class="sxs-lookup"><span data-stu-id="9d27a-117">Introduced Document Brand Management administrative tools</span></span>
-   <span data-ttu-id="9d27a-118">埋め込みチャート コントロールを通じて使用可能な追加の視覚エフェクト</span><span class="sxs-lookup"><span data-stu-id="9d27a-118">Additional visualizations available through the Embedded Charting Control</span></span>
-   <span data-ttu-id="9d27a-119">レポート本文の日付と金額は、「日付、時刻、および数字の形式」のユーザー設定に基づいて書式設定されます</span><span class="sxs-lookup"><span data-stu-id="9d27a-119">Dates and Amounts in the report body are formatted based on the "Date, time, and number format" user setting</span></span>
-   <span data-ttu-id="9d27a-120">ネットワーク印刷監視フォーム</span><span class="sxs-lookup"><span data-stu-id="9d27a-120">Network Print monitoring form</span></span>
-   <span data-ttu-id="9d27a-121">VS クエリ選択ツールを通じてサポートする必要があるテーブル拡張</span><span class="sxs-lookup"><span data-stu-id="9d27a-121">Table extensions need to be supported through the VS Query picker</span></span>

## <a name="what-is-a-report-in-the-finance-and-operations"></a><span data-ttu-id="9d27a-122">Finance and Operation で「レポート」とは何ですか ?</span><span class="sxs-lookup"><span data-stu-id="9d27a-122">What is a report in the Finance and Operations?</span></span>
<span data-ttu-id="9d27a-123">レポートは、単に構造化されたデータ セットの表示として定義することができます。</span><span class="sxs-lookup"><span data-stu-id="9d27a-123">Reports can be defined simply as any visualization of a structured data set.</span></span> <span data-ttu-id="9d27a-124">これには、表形式のレイアウトで提示されたトランザクション データと集約情報の高度なグラフィカル ビューが含まれます。</span><span class="sxs-lookup"><span data-stu-id="9d27a-124">This may include transactional data presented in a tabular layout and advanced graphical views of aggregate information.</span></span> <span data-ttu-id="9d27a-125">この広範な定義を考慮するために、Finance and Operations では、複雑なビジネス要件を満たすレポートを作成するためのツールをいくつか提供しています。</span><span class="sxs-lookup"><span data-stu-id="9d27a-125">To account for this broad definition, Finance and Operations offers several tools to produce reports to satisfy complex business requirements.</span></span> <span data-ttu-id="9d27a-126">ERP におけるレポートの一般的なアプリケーションは次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="9d27a-126">Some common applications of reports in an ERP include:</span></span>

-   <span data-ttu-id="9d27a-127">転記処理の一部としてトランザクション ドキュメントのアーカイブと作成をしています</span><span class="sxs-lookup"><span data-stu-id="9d27a-127">Creating and archiving transactional documents as part of a posting process</span></span>
-   <span data-ttu-id="9d27a-128">製造から倉庫管理、販売へとオーダーを追跡するための梱包明細の生成</span><span class="sxs-lookup"><span data-stu-id="9d27a-128">Producing packing slips for tracking orders from Manufacturing to Warehousing to Sales</span></span>
-   <span data-ttu-id="9d27a-129">主要業績評価測定の監視およびデータの傾向を提示</span><span class="sxs-lookup"><span data-stu-id="9d27a-129">Monitoring key performance metrics and surfacing trends in data</span></span>
-   <span data-ttu-id="9d27a-130">フィルター処理された検索を通じたクライアントのナビゲーション</span><span class="sxs-lookup"><span data-stu-id="9d27a-130">Navigating the client through filtered searches</span></span>
-   <span data-ttu-id="9d27a-131">顧客および従業員に高度なブランド ドキュメントを配布</span><span class="sxs-lookup"><span data-stu-id="9d27a-131">Distributing heavily branded documents to customers and employees</span></span>
-   <span data-ttu-id="9d27a-132">企業の状態を明確に示し方法でデータを抽出</span><span class="sxs-lookup"><span data-stu-id="9d27a-132">Extracting data in such a way that it articulates the health of a business</span></span>

<span data-ttu-id="9d27a-133">開発者にとって最も難しいのは、顧客の要件を考慮して、*適切な* ビジネス インテリジェンスの視覚化ツールを選択することです。</span><span class="sxs-lookup"><span data-stu-id="9d27a-133">The most difficult task for developers is selecting the *right* Business Intelligence visualization tool for the job, given a customer’s requirements.</span></span> <span data-ttu-id="9d27a-134">これを行うには、レポート作成に使用できるツールを使用して、提供される機能を理解することが重要です。</span><span class="sxs-lookup"><span data-stu-id="9d27a-134">To accomplish this, it’s important to understand the capabilities offered through the tools that are available for creating reports.</span></span> <span data-ttu-id="9d27a-135">Finance and Operations では、次の基本的なレポート要件をサポートするためのツールがあります。</span><span class="sxs-lookup"><span data-stu-id="9d27a-135">In the Finance and Operations, we offer tooling to support the following basic reporting requirements:</span></span>

-   <span data-ttu-id="9d27a-136">**Excel 統合** - Microsoft Excel を使用したデータ管理と分析が可能</span><span class="sxs-lookup"><span data-stu-id="9d27a-136">**Excel Integration** - Allows data management and analysis using Microsoft Excel</span></span>
-   <span data-ttu-id="9d27a-137">**埋め込み分析** - グラフやグリッドなどのネイティブ コントロールを使用してワークスペースに集計データを追加する</span><span class="sxs-lookup"><span data-stu-id="9d27a-137">**Embedded Analytics** - Add aggregate data to a Workspaces using native controls like charts and grids</span></span>
-   <span data-ttu-id="9d27a-138">**レポート サービス** - SSRS ベースのソリューションを使用して精度が必要なビジネス ドキュメントを作成します</span><span class="sxs-lookup"><span data-stu-id="9d27a-138">**Reporting Services** - Create business documents that require precision using SSRS-based solutions</span></span>
-   <span data-ttu-id="9d27a-139">**Power BI 統合** - どこにでもアクセスできる作成者とレポートの共有</span><span class="sxs-lookup"><span data-stu-id="9d27a-139">**Power BI Integration** - Author and share reports that can be accessed anywhere</span></span>
-   <span data-ttu-id="9d27a-140">**Management Reporter** – 財務諸表を作成するユーザーを支援するように設計されています。</span><span class="sxs-lookup"><span data-stu-id="9d27a-140">**Management Reporter** – Designed to help users create financial reports</span></span>

<span data-ttu-id="9d27a-141">次のテーブルを使用して、これらのレポート ツールの基本特性を比較できます。</span><span class="sxs-lookup"><span data-stu-id="9d27a-141">The following table can be used to compare the basic characteristics of these reporting tools:</span></span>

| <span data-ttu-id="9d27a-142">TOOL</span><span class="sxs-lookup"><span data-stu-id="9d27a-142">TOOL</span></span>                  | <span data-ttu-id="9d27a-143">AUTHOR</span><span class="sxs-lookup"><span data-stu-id="9d27a-143">AUTHOR</span></span> | <span data-ttu-id="9d27a-144">TARGET</span><span class="sxs-lookup"><span data-stu-id="9d27a-144">TARGET</span></span> | <span data-ttu-id="9d27a-145">DATA</span><span class="sxs-lookup"><span data-stu-id="9d27a-145">DATA</span></span>                     | <span data-ttu-id="9d27a-146">消費</span><span class="sxs-lookup"><span data-stu-id="9d27a-146">CONSUMPTION</span></span>   | <span data-ttu-id="9d27a-147">デザイナー</span><span class="sxs-lookup"><span data-stu-id="9d27a-147">DESIGNER</span></span> |
|---------------------------|------------|------------|------------------------------|-------------------|--------------|
| <span data-ttu-id="9d27a-148">Excel</span><span class="sxs-lookup"><span data-stu-id="9d27a-148">Excel</span></span>               | <span data-ttu-id="9d27a-149">Power User</span><span class="sxs-lookup"><span data-stu-id="9d27a-149">Power User</span></span> | <span data-ttu-id="9d27a-150">Power User</span><span class="sxs-lookup"><span data-stu-id="9d27a-150">Power User</span></span> | <span data-ttu-id="9d27a-151">トランザクションの</span><span class="sxs-lookup"><span data-stu-id="9d27a-151">Transactional</span></span>                | <span data-ttu-id="9d27a-152">外部品目番号</span><span class="sxs-lookup"><span data-stu-id="9d27a-152">External</span></span>          | <span data-ttu-id="9d27a-153">自由書式</span><span class="sxs-lookup"><span data-stu-id="9d27a-153">Free form</span></span>    |
| <span data-ttu-id="9d27a-154">組み込み型 BI</span><span class="sxs-lookup"><span data-stu-id="9d27a-154">Embedded BI</span></span>         | <span data-ttu-id="9d27a-155">開発者</span><span class="sxs-lookup"><span data-stu-id="9d27a-155">Developer</span></span>  | <span data-ttu-id="9d27a-156">すべてのユーザー</span><span class="sxs-lookup"><span data-stu-id="9d27a-156">All users</span></span>  | <span data-ttu-id="9d27a-157">集約</span><span class="sxs-lookup"><span data-stu-id="9d27a-157">Aggregates</span></span>                   | <span data-ttu-id="9d27a-158">内部</span><span class="sxs-lookup"><span data-stu-id="9d27a-158">Internal</span></span>          | <span data-ttu-id="9d27a-159">モデル化済み</span><span class="sxs-lookup"><span data-stu-id="9d27a-159">Modeled</span></span>      |
| <span data-ttu-id="9d27a-160">SSRS レポート</span><span class="sxs-lookup"><span data-stu-id="9d27a-160">SSRS Report</span></span>         | <span data-ttu-id="9d27a-161">開発者</span><span class="sxs-lookup"><span data-stu-id="9d27a-161">Developer</span></span>  | <span data-ttu-id="9d27a-162">すべてのユーザー</span><span class="sxs-lookup"><span data-stu-id="9d27a-162">All users</span></span>  | <span data-ttu-id="9d27a-163">トランザクションと集計</span><span class="sxs-lookup"><span data-stu-id="9d27a-163">Transactional and Aggregates</span></span> | <span data-ttu-id="9d27a-164">内部/外部</span><span class="sxs-lookup"><span data-stu-id="9d27a-164">Internal/External</span></span> | <span data-ttu-id="9d27a-165">自由書式</span><span class="sxs-lookup"><span data-stu-id="9d27a-165">Free form</span></span>    |
| <span data-ttu-id="9d27a-166">パワー BI</span><span class="sxs-lookup"><span data-stu-id="9d27a-166">Power BI</span></span>            | <span data-ttu-id="9d27a-167">Power User</span><span class="sxs-lookup"><span data-stu-id="9d27a-167">Power User</span></span> | <span data-ttu-id="9d27a-168">すべてのユーザー</span><span class="sxs-lookup"><span data-stu-id="9d27a-168">All users</span></span>  | <span data-ttu-id="9d27a-169">集約</span><span class="sxs-lookup"><span data-stu-id="9d27a-169">Aggregates</span></span>                   | <span data-ttu-id="9d27a-170">内部/外部</span><span class="sxs-lookup"><span data-stu-id="9d27a-170">Internal/External</span></span> | <span data-ttu-id="9d27a-171">自由書式</span><span class="sxs-lookup"><span data-stu-id="9d27a-171">Free form</span></span>    |
| <span data-ttu-id="9d27a-172">Management Reporter</span><span class="sxs-lookup"><span data-stu-id="9d27a-172">Management Reporter</span></span> | <span data-ttu-id="9d27a-173">Power User</span><span class="sxs-lookup"><span data-stu-id="9d27a-173">Power User</span></span> | <span data-ttu-id="9d27a-174">Power User</span><span class="sxs-lookup"><span data-stu-id="9d27a-174">Power User</span></span> | <span data-ttu-id="9d27a-175">トランザクションの</span><span class="sxs-lookup"><span data-stu-id="9d27a-175">Transactional</span></span>                | <span data-ttu-id="9d27a-176">外部品目番号</span><span class="sxs-lookup"><span data-stu-id="9d27a-176">External</span></span>          | <span data-ttu-id="9d27a-177">モデル化済み</span><span class="sxs-lookup"><span data-stu-id="9d27a-177">Modeled</span></span>      |

## <a name="create-a-report-using-list-pages"></a><span data-ttu-id="9d27a-178">リスト ページを使用してレポートを作成する</span><span class="sxs-lookup"><span data-stu-id="9d27a-178">Create a report using List Pages</span></span>
<span data-ttu-id="9d27a-179">このセクションでは、エンティティの詳細フォームに表示される Finance and Operations のデータをエクスポートするプロセスについて説明します。</span><span class="sxs-lookup"><span data-stu-id="9d27a-179">In this section, we'll walk you through the process of exporting Finance and Operations data displayed in an entity details form.</span></span> <span data-ttu-id="9d27a-180">ここで、Finance and Operations の各フォームが、Excel の権限を使用して管理および分析するデータのソースとして表示される方法について示します。</span><span class="sxs-lookup"><span data-stu-id="9d27a-180">Here we’ll demonstrate how every form in Finance and Operations can be viewed as a source of data for management and analysis using the power of Excel.</span></span>

### <a name="create-an-analysis-report-based-on-all-rentals-in-fleet-management-that-are-marked-as-complete"></a><span data-ttu-id="9d27a-181">完了とマークされているフリート管理のすべてのレンタルに基づいて分析レポートを作成する</span><span class="sxs-lookup"><span data-stu-id="9d27a-181">Create an analysis report based on all rentals in Fleet Management that are marked as complete</span></span>

1.  <span data-ttu-id="9d27a-182">Internet Explorer を開き、Finance and Operations インスタンスの基本 URLに移動してサインインします。</span><span class="sxs-lookup"><span data-stu-id="9d27a-182">Open Internet Explorer, and navigate to your Finance and Operations instance base URL and sign in.</span></span>
    1.  <span data-ttu-id="9d27a-183">クラウド環境では、ベース URL は LCS から取得されます。</span><span class="sxs-lookup"><span data-stu-id="9d27a-183">On the cloud environment, the base URL is obtained from LCS</span></span>
    2.  <span data-ttu-id="9d27a-184">ローカル VM の、基準 URL は https://usnconeboxax1aos.cloud.onebox.dynamics.comです</span><span class="sxs-lookup"><span data-stu-id="9d27a-184">On a local VM, the base URL is https://usnconeboxax1aos.cloud.onebox.dynamics.com</span></span>

2.  <span data-ttu-id="9d27a-185">ダッシュ ボードで、右にスクロールし、**予約管理**タイルをクリックします。</span><span class="sxs-lookup"><span data-stu-id="9d27a-185">On the Dashboard, scroll to the far right, and click the **Reservation management** tile.</span></span>
3.  <span data-ttu-id="9d27a-186">**概要** セクションで、**すべてのレンタル** タイルをクリックします。</span><span class="sxs-lookup"><span data-stu-id="9d27a-186">Under the **Summary** section, click on the **All rentals** tile.</span></span>
4.  <span data-ttu-id="9d27a-187">メイン グリッドの横にあるフィルター アイコンをクリックして、**フィルター**ウィンドウを展開します。</span><span class="sxs-lookup"><span data-stu-id="9d27a-187">Expand the **Filters** pane by clicking on the Filters icon next to the main grid.</span></span>
5.  <span data-ttu-id="9d27a-188">**フィルター フィールドの追加**をクリックし、次にドロップダウン リストの**ステータス**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="9d27a-188">Click **Add a filter field**, and then select **Status** in the drop-down list.</span></span>
6.  <span data-ttu-id="9d27a-189">状態フィルター フィールドの**完了**を入力し、**適用**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="9d27a-189">Enter **Complete** in the Status filter field, and then click **Apply**.</span></span>
7.  <span data-ttu-id="9d27a-190">ページの操作バーを展開し、**Office で開く**をクリックして、次に**レンタル**を選択します。</span><span class="sxs-lookup"><span data-stu-id="9d27a-190">Expand the page action bar, click **Open in Office**, and then select **Rentals**.</span></span>

    <span data-ttu-id="9d27a-191">[![FMRentals エクスポート](./media/fmrentals-export.png)](./media/fmrentals-export.png)</span><span class="sxs-lookup"><span data-stu-id="9d27a-191">[![FMRentals export](./media/fmrentals-export.png)](./media/fmrentals-export.png)</span></span> 

    <span data-ttu-id="9d27a-192">データをエクスポートした後、Excel ツールのパワーと柔軟性を使用して、プレゼンテーション、または追加の分析のレポートを作成できます。</span><span class="sxs-lookup"><span data-stu-id="9d27a-192">After the data has been exported, you can use the power and flexibility of the Excel tools to create reports for presentation or additional analysis.</span></span> <span data-ttu-id="9d27a-193">Excel で作成したセルフサービス レポートの例を次に示します。</span><span class="sxs-lookup"><span data-stu-id="9d27a-193">The following is an example of a self-service report authored with Excel.</span></span> <span data-ttu-id="9d27a-194">[![FMRentals 分析](./media/fmrentals-analysis-1024x775.png)](./media/fmrentals-analysis.png)</span><span class="sxs-lookup"><span data-stu-id="9d27a-194">[![FMRentals analysis](./media/fmrentals-analysis-1024x775.png)](./media/fmrentals-analysis.png)</span></span>

1.  <span data-ttu-id="9d27a-195">ブラウザー セッションおよびエクスポートされた Excel ファイルを閉じます。</span><span class="sxs-lookup"><span data-stu-id="9d27a-195">Close the browser session and the exported Excel file.</span></span>

### <a name="advantages-of-list-pages"></a><span data-ttu-id="9d27a-196">リスト ページのメリット</span><span class="sxs-lookup"><span data-stu-id="9d27a-196">Advantages of List Pages</span></span>

-   <span data-ttu-id="9d27a-197">外部レポートおよび Excel のような分析ツールを使用する、トランザクション ビジネス データにアクセスするための柔軟性のあるソース</span><span class="sxs-lookup"><span data-stu-id="9d27a-197">Flexible source for accessing transactional business data using external reporting and analytical tools like Excel</span></span>
-   <span data-ttu-id="9d27a-198">エンドユーザーが開発者を必要とせずに、必要なデータ セットをモデル化できるよう許可します。</span><span class="sxs-lookup"><span data-stu-id="9d27a-198">Allows end-users to model the data sets they need without requiring a developer</span></span>
-   <span data-ttu-id="9d27a-199">リアルタイムのビジネス情報への直接アクセス</span><span class="sxs-lookup"><span data-stu-id="9d27a-199">Direct access to real-time business information</span></span>

## <a name="expand-predefined-views-and-add-navigation-to-charts"></a><span data-ttu-id="9d27a-200">定義済みのビューを展開し、グラフへのナビゲーションを追加</span><span class="sxs-lookup"><span data-stu-id="9d27a-200">Expand predefined views and add navigation to charts</span></span>
<span data-ttu-id="9d27a-201">ビジネス インテリジェンスは組織のすべてのレベルで役に立ちます。</span><span class="sxs-lookup"><span data-stu-id="9d27a-201">Business Intelligence can be useful at every level of an organization.</span></span> <span data-ttu-id="9d27a-202">埋め込みコントロールを使用して、ターゲット ペルソナに基づいて最も関連性の高い情報を提供します。</span><span class="sxs-lookup"><span data-stu-id="9d27a-202">Use embedded controls to elevate the most relevant information based on the target persona.</span></span> <span data-ttu-id="9d27a-203">Microsoft Dynamics 365 for Finance and Operations のネイティブ コントロールは、通知された意思決定を許可する集計データと対話する直観的かつ便利な方法をユーザーに提供します。</span><span class="sxs-lookup"><span data-stu-id="9d27a-203">Native controls in Microsoft Dynamics 365 for Finance and Operations offer users an intuitive and convenient way of interacting with aggregate data allowing for informed decision making.</span></span>

### <a name="create-development-project"></a><span data-ttu-id="9d27a-204">開発プロジェクトの作成</span><span class="sxs-lookup"><span data-stu-id="9d27a-204">Create development project</span></span>

1.  <span data-ttu-id="9d27a-205">デスクトップで、**Visual Studio 2015** ショートカットを右クリックし、**管理者として実行**を選択して開発環境を開きます。</span><span class="sxs-lookup"><span data-stu-id="9d27a-205">On the Desktop, right-click the **Visual Studio 2015** shortcut, and select **Run as administrator** to open the development environment.</span></span>
2.  <span data-ttu-id="9d27a-206">ツール バーで、**表示**をクリックし、**アプリケーション エクスプローラー**を選択します。</span><span class="sxs-lookup"><span data-stu-id="9d27a-206">On the toolbar, click **View**, and then select **Application Explorer**</span></span>
3.  <span data-ttu-id="9d27a-207">**フリート管理**モジュールで、**アプリケーション エクスプローラー**を使用して **FMReservationsReport** フォームを検索します。</span><span class="sxs-lookup"><span data-stu-id="9d27a-207">Use the **Application Explorer** to search for the **FMReservationsReport** form in the **Fleet Management** module.</span></span>
4.  <span data-ttu-id="9d27a-208">**アプリケーション エクスプローラーの**検索結果で、**FMReservationsReport** フォームを右クリックしてから、**新しいプロジェクトに追加**を選択します。</span><span class="sxs-lookup"><span data-stu-id="9d27a-208">In the **Application Explorer’s** search results, right-click **FMReservationsReport** form, and then select **Add to new project**.</span></span>
5.  <span data-ttu-id="9d27a-209">**Finance and Operations プロジェクト** テンプレートを選択し、**OK** をクリックしてプロジェクトを作成します。</span><span class="sxs-lookup"><span data-stu-id="9d27a-209">Select the **Finance and Operations Project** template, and then click **OK** to create the project.</span></span>
6.  <span data-ttu-id="9d27a-210">**ソリューション エクスプローラー**で **FMReservationsReport** メニュー項目を右クリックしてから、**スタートアップ オブジェクトとして設定**を選択します。</span><span class="sxs-lookup"><span data-stu-id="9d27a-210">In **Solution Explorer**, right-click **FMReservationsReport** menu item, and then select **Set as startup object.**</span></span>
7.  <span data-ttu-id="9d27a-211">**Ctrl+Shift+B** キーを押して、プロジェクトを保存およびビルドします。</span><span class="sxs-lookup"><span data-stu-id="9d27a-211">Press **Ctrl+Shift+B** to save and build the project.</span></span>
8.  <span data-ttu-id="9d27a-212">**Ctrl + F5** キーを押して、レポートを含むフォームを読み込みます。</span><span class="sxs-lookup"><span data-stu-id="9d27a-212">Press **Ctrl + F5** to load the form containing the report.</span></span>

    <span data-ttu-id="9d27a-213">[![FMCustomer アクティビティ](./media/fmcustomer-activity-300x224.png)](./media/fmcustomer-activity.png)</span><span class="sxs-lookup"><span data-stu-id="9d27a-213">[![FMCustomer activity](./media/fmcustomer-activity-300x224.png)](./media/fmcustomer-activity.png)</span></span> 

<span data-ttu-id="9d27a-214">この時点で、集計データの事前に定義されたグラフのビジュアル化のコレクションがあります。</span><span class="sxs-lookup"><span data-stu-id="9d27a-214">At this point, you have a collection of pre-defined chart visualizations of Aggregate data.</span></span> <span data-ttu-id="9d27a-215">コントロールは、ホバー テキスト、シリーズ フィルタリング、タッチ拡張などの基本的な対話型機能を提供します。</span><span class="sxs-lookup"><span data-stu-id="9d27a-215">The controls offer basic interactive features like hover text, series filtering, and touch expansion.</span></span> <span data-ttu-id="9d27a-216">ただし、より良いユーザー対話が要求されるのは、多くの場合適切なことです。</span><span class="sxs-lookup"><span data-stu-id="9d27a-216">However, it is often appropriate that a greater degree of user interactivity is required.</span></span>

### <a name="change-the-default-chart-type-for-the-visualization"></a><span data-ttu-id="9d27a-217">視覚化のための既定のグラフ タイプの変更</span><span class="sxs-lookup"><span data-stu-id="9d27a-217">Change the default chart type for the visualization</span></span>

1.  <span data-ttu-id="9d27a-218">ブラウザー セッションを終了して、Visual Studio プロジェクトに戻ります。</span><span class="sxs-lookup"><span data-stu-id="9d27a-218">Close the browser session and return to the Visual Studio project.</span></span>
2.  <span data-ttu-id="9d27a-219">**アプリケーション エクスプローラー**を開いて、**FMReservationsByCustPart** フォームを右クリックしてから、**プロジェクトに追加**を選択します。</span><span class="sxs-lookup"><span data-stu-id="9d27a-219">Open the **Application Explorer**, locate the **FMReservationsByCustPart** form, right-click, and then select **Add to project**.</span></span>
3.  <span data-ttu-id="9d27a-220">**FMReservationsByCustPart** フォーム デザイナーを開きます。</span><span class="sxs-lookup"><span data-stu-id="9d27a-220">Open the **FMReservationsByCustPart** form designer.</span></span>
4.  <span data-ttu-id="9d27a-221">**ReservationsByCust** グラフ定義の**シリーズ** コレクションへのアクセス。</span><span class="sxs-lookup"><span data-stu-id="9d27a-221">Access the **Series** collection in the **ReservationsByCust** chart definition.</span></span>
5.  <span data-ttu-id="9d27a-222">**SysBuildChatMeasure1** シリーズ定義を選択</span><span class="sxs-lookup"><span data-stu-id="9d27a-222">Select the **SysBuildChatMeasure1** series definition</span></span>
6.  <span data-ttu-id="9d27a-223">**プロパティ** ウィンドウで**外観**セクションを検索します。</span><span class="sxs-lookup"><span data-stu-id="9d27a-223">Locate the **Appearance** section in the **Properties** window.</span></span>
7.  <span data-ttu-id="9d27a-224">**グラフ タイプ**の値を更新し、**Pie** を選択します。</span><span class="sxs-lookup"><span data-stu-id="9d27a-224">Update the **Chart type** value and select **Pie**</span></span>
8.  <span data-ttu-id="9d27a-225">Ctrl+Shift+B キーを押して、プロジェクトを保存およびリビルドします。</span><span class="sxs-lookup"><span data-stu-id="9d27a-225">Press Ctrl+Shift+B to save and rebuild the project.</span></span>
9.  <span data-ttu-id="9d27a-226">Ctrl + F5 キーを押してレポートを実行します。</span><span class="sxs-lookup"><span data-stu-id="9d27a-226">Press Ctrl + F5 to run the report.</span></span>

<span data-ttu-id="9d27a-227">**顧客別引当** ビューは、顧客間のレンタル活動を比較するタスクを簡略化するため、円グラフを使用して集計データ セットを視覚化するようになりました。</span><span class="sxs-lookup"><span data-stu-id="9d27a-227">The **Reservations by customer** view now visualizes the aggregate data set using a Pie chart to simplify the task of comparing rental activity across customers.</span></span> 

<span data-ttu-id="9d27a-228">[![FMCustomer アクティビティ 2](./media/fmcustomer-activity-2-1024x733.png)](./media/fmcustomer-activity-2.png)</span><span class="sxs-lookup"><span data-stu-id="9d27a-228">[![FMCustomer activity 2](./media/fmcustomer-activity-2-1024x733.png)](./media/fmcustomer-activity-2.png)</span></span> 

<span data-ttu-id="9d27a-229">追加の機能を以下に示します。</span><span class="sxs-lookup"><span data-stu-id="9d27a-229">Additional functions include:</span></span>

-   <span data-ttu-id="9d27a-230">モデル化されたプロパティを使用したコンテキスト ドリル スルー ナビゲーションの定義</span><span class="sxs-lookup"><span data-stu-id="9d27a-230">Define contextual drill-through navigations using modeled properties</span></span>
-   <span data-ttu-id="9d27a-231">X++ フォーム ロジックを使用したドリルスルー リンクの管理</span><span class="sxs-lookup"><span data-stu-id="9d27a-231">Manage drill-through links using X++ form logic</span></span>

### <a name="advantages-of-embedded-aggregate-visualizations"></a><span data-ttu-id="9d27a-232">埋め込み集計視覚エフェクトのメリット</span><span class="sxs-lookup"><span data-stu-id="9d27a-232">Advantages of embedded aggregate visualizations</span></span>

-   <span data-ttu-id="9d27a-233">組織のあらゆるレベルで、情報に基づく意思決定を促進するためにシンプルで直感的に設計されています</span><span class="sxs-lookup"><span data-stu-id="9d27a-233">Designed to be simple and intuitive to promote informed decisions at every level of the organization</span></span>
-   <span data-ttu-id="9d27a-234">コンシューマーのニーズに合わせて調整された、事前に定義されたビュー</span><span class="sxs-lookup"><span data-stu-id="9d27a-234">Pre-defined views tailored to meet the needs of the consumer</span></span>
-   <span data-ttu-id="9d27a-235">ユーザーがデータの主要業績評価のトレンドを認識できるよう補強する</span><span class="sxs-lookup"><span data-stu-id="9d27a-235">Augments the user’s ability to recognize key performance trends in the data</span></span>

## <a name="using-the-freeform-report-designer"></a><span data-ttu-id="9d27a-236">自由形式レポート デザイナーの使用</span><span class="sxs-lookup"><span data-stu-id="9d27a-236">Using the freeform report designer</span></span>
<span data-ttu-id="9d27a-237">SSRS は、引き続き ERP アプリケーションの高度なビジネス ドキュメント ソリューションを作成するためのプラットフォームです。</span><span class="sxs-lookup"><span data-stu-id="9d27a-237">SSRS continues to be the platform for producing advanced Business Document solutions for your ERP application.</span></span> <span data-ttu-id="9d27a-238">ホストされたサービスは、統合されたパラメーター経験を持つ大量かつ高度なトランザクション レポート用に設計されています。</span><span class="sxs-lookup"><span data-stu-id="9d27a-238">The hosted service is designed for high volume and heavily transactional reports with an integrated parameter experience.</span></span> <span data-ttu-id="9d27a-239">Document Printing & Distribution Services によってサポートされており、これらのソリューションは電子メール、印刷、アーカイブ、およびバルク配分向けの正確なドキュメントを作成するのに最適です。</span><span class="sxs-lookup"><span data-stu-id="9d27a-239">Backed by the Document Printing & Distribution Services, these solutions are ideal for producing precision documents which are intended for email, printing, archive, and bulk distribution.</span></span>

### <a name="open-the-precision-designer"></a><span data-ttu-id="9d27a-240">Precision Designer を開く</span><span class="sxs-lookup"><span data-stu-id="9d27a-240">Open the Precision Designer</span></span>

1.  <span data-ttu-id="9d27a-241">ブラウザー セッションを終了して、Visual Studio プロジェクトに戻ります。</span><span class="sxs-lookup"><span data-stu-id="9d27a-241">Close the browser session and return to the Visual Studio project.</span></span>
2.  <span data-ttu-id="9d27a-242">有効なプロジェクトを閉じるには、**ファイル** &gt; **ソリューションを閉じる**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="9d27a-242">Click **File** &gt; **Close Solution**, to close the active project.</span></span>
3.  <span data-ttu-id="9d27a-243">**アプリケーション エクスプ ローラー**を使用して、**FMRentalsByCust** という名前のオブジェクトを検索します。</span><span class="sxs-lookup"><span data-stu-id="9d27a-243">Use the **Application Explorer** to search for objects with **FMRentalsByCust** in the name</span></span>
4.  <span data-ttu-id="9d27a-244">**アプリケーション エクスプローラーの**検索結果で、**クラス**、**出力メニュー項目**、および **FMRentalsByCustomer** レポートをすべて選択します。</span><span class="sxs-lookup"><span data-stu-id="9d27a-244">In the **Application Explorer’s** search results, select all **Classes**, the **Output Menu Item**, and the **FMRentalsByCustomer** report</span></span>
5.  <span data-ttu-id="9d27a-245">右クリックし、**新しいプロジェクトに追加** を選択します。</span><span class="sxs-lookup"><span data-stu-id="9d27a-245">Right-click and then select **Add to new project**.</span></span>
6.  <span data-ttu-id="9d27a-246">**Dynamics 365** テンプレートを選択し、**OK** をクリックしてプロジェクトを作成します。</span><span class="sxs-lookup"><span data-stu-id="9d27a-246">Select the **Dynamics 365** template, and then click **OK** to create the project.</span></span>
7.  <span data-ttu-id="9d27a-247">**ソリューション エクスプローラー**で、**FMRentalsByCustomer** レポートをダブルクリックしてデザイナーを開きます。</span><span class="sxs-lookup"><span data-stu-id="9d27a-247">In **Solution Explorer**, double-click on the **FMRentalsByCustomer** report to open the designer.</span></span>
8.  <span data-ttu-id="9d27a-248">デザイナー定義のリストを表示するには、デザイナーの**デザイナー**コレクションを展開します。</span><span class="sxs-lookup"><span data-stu-id="9d27a-248">Expand the **Designs** collection in the designer to view the list of design definitions</span></span>
9.  <span data-ttu-id="9d27a-249">精密なデザイナーを使いレポート定義を表示するには、**Report** デザインをダブルクリックします。</span><span class="sxs-lookup"><span data-stu-id="9d27a-249">Double-click on the **Report** design to view the report definition using the Precision Designer</span></span>

<span data-ttu-id="9d27a-250">[![レポート デザイナー](./media/report-designer-1024x665.png)](./media/report-designer.png)</span><span class="sxs-lookup"><span data-stu-id="9d27a-250">[![Report designer](./media/report-designer-1024x665.png)](./media/report-designer.png)</span></span> 

<span data-ttu-id="9d27a-251">上記は、Visual Studio 2015 Precision Designer を使用して表示される FMRentalsByCustomer レポート デザイン定義のスクリーン ショットです。</span><span class="sxs-lookup"><span data-stu-id="9d27a-251">The above is a screen-shot of the FMRentalsByCustomer report design definition as viewed using the Visual Studio 2015 Precision Designer.</span></span> <span data-ttu-id="9d27a-252">Precision Designer には、レポートのコンテンツおよびレイアウトをカスタマイズできる組み込みツールが備わった、自由書式デザイン サーフェイスが用意されています。</span><span class="sxs-lookup"><span data-stu-id="9d27a-252">The Precision Designer offers a free-form design surface with built-in tools that allow you to customize the content and layout of the report.</span></span> <span data-ttu-id="9d27a-253">また、埋め込み VB コードを活用して、実行時デザイン操作を作成し、ユーザーとの対話をサポートすることができます。</span><span class="sxs-lookup"><span data-stu-id="9d27a-253">You can also take advantage of embedded VB code to create run-time design manipulations and support user interactions.</span></span> <span data-ttu-id="9d27a-254">統合されたツールとして、開発者は AX EDT に基づいてレポート本文のデータをフォーマットするために AX ラベルとパブリック API を参照することができます。</span><span class="sxs-lookup"><span data-stu-id="9d27a-254">As an integrated tool, developers are able to reference AX labels and public APIs to format data in the report body based on AX EDTs.</span></span> <span data-ttu-id="9d27a-255">MSDN には、SSRS 書式設定機能に関連する豊富な開発者ドキュメントが用意されています。</span><span class="sxs-lookup"><span data-stu-id="9d27a-255">MSDN offers a rich collection of developer documentation related to SSRS formatting capabilities.</span></span> <span data-ttu-id="9d27a-256">有効 SSRS レポートを設計する基本的な方法については、[Reporting Services レポート (SSRS)](https://msdn.microsoft.com/en-us/library/bb522712.aspx) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="9d27a-256">See the article [Reporting Services Reports (SSRS)](https://msdn.microsoft.com/en-us/library/bb522712.aspx) on for a good primer on designing effective SSRS reports.</span></span>

## <a name="customizing-the-parameter-experience"></a><span data-ttu-id="9d27a-257">パラメータ経験のカスタマイズ</span><span class="sxs-lookup"><span data-stu-id="9d27a-257">Customizing the parameter experience</span></span>
<span data-ttu-id="9d27a-258">レポート フレームワークは、モデル化されたソリューションを使用して対処できない要件を持つ先進的なソリューションを促進するため、サービスの拡張機能を通じて柔軟性を提供します。</span><span class="sxs-lookup"><span data-stu-id="9d27a-258">The Reporting Framework offers flexibility through service extensions to facilitate advanced solutions with requirements that cannot be addressed using a modeled solution.</span></span> <span data-ttu-id="9d27a-259">VS デザイナーを使用して、基本的なパラメーターの書式設定、グループ化、入力の検証を追加します。</span><span class="sxs-lookup"><span data-stu-id="9d27a-259">Use the VS designer to add basic parameter formatting, grouping, and input validation.</span></span> <span data-ttu-id="9d27a-260">X++ ベースのデータ コントラクト検証はより高度なシナリオで使用可能です。</span><span class="sxs-lookup"><span data-stu-id="9d27a-260">X++ based data contract validation is available for more advanced scenarios.</span></span> <span data-ttu-id="9d27a-261">ユーザー インターフェイス (UI) ビルダ クラスを追加して、レポートを実行する前にセッション入力を促すパラメータ ウィンドウをカスタマイズすることを検討してください。</span><span class="sxs-lookup"><span data-stu-id="9d27a-261">Consider adding User Interface (UI) Builder Classes to customize the parameter pane used to prompt for session inputs before running a report.</span></span> <span data-ttu-id="9d27a-262">これらのカスタム拡張機能は、次の機能に有効です。</span><span class="sxs-lookup"><span data-stu-id="9d27a-262">These custom extensions are effective for addressing the following functions:</span></span>

-   <span data-ttu-id="9d27a-263">ダイアログ フィールド イベントのオーバーライド</span><span class="sxs-lookup"><span data-stu-id="9d27a-263">Overriding dialog field events</span></span>
-   <span data-ttu-id="9d27a-264">レポート パラメーター インラインの検証</span><span class="sxs-lookup"><span data-stu-id="9d27a-264">Validating report parameters inline</span></span>
-   <span data-ttu-id="9d27a-265">ダイアログ フィールドにカスタマイズされた参照の追加</span><span class="sxs-lookup"><span data-stu-id="9d27a-265">Adding customized lookups to dialog fields</span></span>
-   <span data-ttu-id="9d27a-266">ダイアログ管理のレイアウトの変更</span><span class="sxs-lookup"><span data-stu-id="9d27a-266">Changing the layout of the dialog controls</span></span>
-   <span data-ttu-id="9d27a-267">画像を含むカスタム コントロールの追加</span><span class="sxs-lookup"><span data-stu-id="9d27a-267">Adding custom controls including images</span></span>

### <a name="defining-parameters-defaulting-using-code"></a><span data-ttu-id="9d27a-268">コードを使用してパラメータを既定設定を定義する</span><span class="sxs-lookup"><span data-stu-id="9d27a-268">Defining parameters defaulting using code</span></span>

1.  <span data-ttu-id="9d27a-269">**ソリューション エクスプローラー**で、**FMRentalsByCustUIBuilder** クラスをダブルクリックしてデザイナーを開きます。</span><span class="sxs-lookup"><span data-stu-id="9d27a-269">In **Solution Explorer**, double-click on the **FMRentalsByCustUIBuilder** class to open the designer.</span></span>
1.  <span data-ttu-id="9d27a-270">クラス**構築**メソッドを検索して、次のように初期化コードを更新します</span><span class="sxs-lookup"><span data-stu-id="9d27a-270">Locate the class **build** method and update the initialization code as follows</span></span>

        public void build()
        {
            Dialog dialogLocal = this.dialog();
            contract = this.dataContractObject() as FMRentalsByCustContract;// associate dialog field with data contract method
            this.addDialogField(methodStr(FMRentalsByCustContract, parmCustGroupId), contract);dialogLocal.addGroup("@SYS41297");
            fromDateField = this.addDialogField(methodStr(FMRentalsByCustContract, parmFromDate), contract);
            toDateField = this.addDialogField(methodStr(FMRentalsByCustContract, parmToDate), contract);// set the default date range values
            fromDateField.value(today() - 365);
            toDateField.value(today());
        }

1.  <span data-ttu-id="9d27a-271">Ctrl+Shift+B キーを押して、プロジェクトを保存およびリビルドします。</span><span class="sxs-lookup"><span data-stu-id="9d27a-271">Press Ctrl+Shift+B to save and rebuild the project.</span></span>
1.  <span data-ttu-id="9d27a-272">Ctrl + F5 キーを押してレポートを実行します。</span><span class="sxs-lookup"><span data-stu-id="9d27a-272">Press Ctrl + F5 to run the report.</span></span>

<span data-ttu-id="9d27a-273">[![FMRentalsByCust コントロール](./media/fmrentalsbycust-controls-1024x691.png)](./media/fmrentalsbycust-controls.png)</span><span class="sxs-lookup"><span data-stu-id="9d27a-273">[![FMRentalsByCust controls](./media/fmrentalsbycust-controls-1024x691.png)](./media/fmrentalsbycust-controls.png)</span></span> 

<span data-ttu-id="9d27a-274">上記のパラメーター初期化コードは、今日の日付に関連したレポート実行の既定値を設定します。</span><span class="sxs-lookup"><span data-stu-id="9d27a-274">The parameter initialization code above sets the default values of the report execution relative to today’s date.</span></span> <span data-ttu-id="9d27a-275">フレームワークのレポート パラメーターの既定処理をオーバーライドするには UIBuilder クラスを使用します。</span><span class="sxs-lookup"><span data-stu-id="9d27a-275">Use the classes UIBuilder to override the framework’s default handling of report parameters.</span></span> <span data-ttu-id="9d27a-276">追加の拡張機能のシナリオがサポートされています。</span><span class="sxs-lookup"><span data-stu-id="9d27a-276">Additional extension scenarios supported:</span></span>

-   <span data-ttu-id="9d27a-277">コントローラー クラスを使用したセッション コンテキストに基づいてクエリ範囲を自動的に設定する</span><span class="sxs-lookup"><span data-stu-id="9d27a-277">Automatically set query ranges based on session context using Controller classes</span></span>
-   <span data-ttu-id="9d27a-278">共有メニュー項目を使用して実行時にレポートのデザインを選択する</span><span class="sxs-lookup"><span data-stu-id="9d27a-278">Select report designs at runtime using a shared menu item</span></span>
-   <span data-ttu-id="9d27a-279">ビジネス ロジックを使用したレポートのデータ コントラクトの値の変更</span><span class="sxs-lookup"><span data-stu-id="9d27a-279">Modify report data contract values using business logic</span></span>

<span data-ttu-id="9d27a-280">**注記:** この例では、RDP ベースのレポートを使用する UIBuilder 拡張子を示しています。</span><span class="sxs-lookup"><span data-stu-id="9d27a-280">**Note:** This example demonstrates a UIBuilder extension with an RDP-based based report.</span></span> <span data-ttu-id="9d27a-281">UIBuilder 拡張子を含むクエリ基準の例は、**FMCustomerList** レポートを表示します。</span><span class="sxs-lookup"><span data-stu-id="9d27a-281">For a Query based example that includes a UIBuilder extension, view the **FMCustomerList** report.</span></span>

## <a name="using-vb-code-to-manage-running-balances"></a><span data-ttu-id="9d27a-282">VB コードを使用して実行中の残高の管理</span><span class="sxs-lookup"><span data-stu-id="9d27a-282">Using VB code to manage running balances</span></span>
<span data-ttu-id="9d27a-283">レポート フレームワークは、モデル化されたソリューションを使用して対処できない要件を持つ先進的なソリューションを促進するため、サービスの拡張機能を通じて柔軟性を提供します。</span><span class="sxs-lookup"><span data-stu-id="9d27a-283">The Reporting Framework offers flexibility through service extensions to facilitate advanced solutions with requirements that cannot be addressed using a modeled solution.</span></span> <span data-ttu-id="9d27a-284">VS デザイナーを使用して、基本的なパラメーターの書式設定、グループ化、入力の検証を追加します。</span><span class="sxs-lookup"><span data-stu-id="9d27a-284">Use the VS designer to add basic parameter formatting, grouping, and input validation.</span></span> <span data-ttu-id="9d27a-285">X++ ベースのデータ コントラクト検証はより高度なシナリオで使用可能です。</span><span class="sxs-lookup"><span data-stu-id="9d27a-285">X++ based data contract validation is available for more advanced scenarios.</span></span> <span data-ttu-id="9d27a-286">ユーザー インターフェイス (UI) ビルダ クラスを追加して、レポートを実行する前にセッション入力を促すパラメータ ウィンドウをカスタマイズすることを検討してください。</span><span class="sxs-lookup"><span data-stu-id="9d27a-286">Consider adding User Interface (UI) Builder Classes to customize the parameter pane used to prompt for session inputs before running a report.</span></span> <span data-ttu-id="9d27a-287">これらのカスタム拡張機能は、次の機能に有効です。</span><span class="sxs-lookup"><span data-stu-id="9d27a-287">These custom extensions are effective for addressing the following functions:</span></span>

-   <span data-ttu-id="9d27a-288">ダイアログ フィールド イベントのオーバーライド</span><span class="sxs-lookup"><span data-stu-id="9d27a-288">Overriding dialog field events</span></span>
-   <span data-ttu-id="9d27a-289">レポート パラメーター インラインの検証</span><span class="sxs-lookup"><span data-stu-id="9d27a-289">Validating report parameters inline</span></span>
-   <span data-ttu-id="9d27a-290">ダイアログ フィールドにカスタマイズされた参照の追加</span><span class="sxs-lookup"><span data-stu-id="9d27a-290">Adding customized lookups to dialog fields</span></span>
-   <span data-ttu-id="9d27a-291">ダイアログ管理のレイアウトの変更</span><span class="sxs-lookup"><span data-stu-id="9d27a-291">Changing the layout of the dialog controls</span></span>
-   <span data-ttu-id="9d27a-292">画像を含むカスタム コントロールの追加</span><span class="sxs-lookup"><span data-stu-id="9d27a-292">Adding custom controls including images</span></span>

### <a name="import-the-section-resources"></a><span data-ttu-id="9d27a-293">セクション リソースをインポートします。</span><span class="sxs-lookup"><span data-stu-id="9d27a-293">Import the section resources</span></span>

1.  <span data-ttu-id="9d27a-294">ブラウザー セッションを終了して、Visual Studio プロジェクトに戻ります。</span><span class="sxs-lookup"><span data-stu-id="9d27a-294">Close the browser session and return to the Visual Studio project.</span></span>
2.  <span data-ttu-id="9d27a-295">ツールバーで、**DYNAMICS AX** をクリックし、**プロジェクトのインポート…** を選択します。</span><span class="sxs-lookup"><span data-stu-id="9d27a-295">On the toolbar, click **DYNAMICS AX**, and then select **Import Project…**</span></span>
3.  <span data-ttu-id="9d27a-296">ファイル名ウィンドウで、C:\\FmLab\\Lab10-3 を参照して、**FMRentalDetailsReport.axpp** を選択してから**開く**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="9d27a-296">In the File name window, browse to C:\\FmLab\\Lab10-3, select **FMRentalDetailsReport.axpp**, and then click **Open**.</span></span>
4.  <span data-ttu-id="9d27a-297">プロジェクト ファイルの場所テキスト ボックスに、C:\\FmLab\\Lab10-3 と入力します。</span><span class="sxs-lookup"><span data-stu-id="9d27a-297">In the Project file location text box, enter C:\\FmLab\\Lab10-3.</span></span>
5.  <span data-ttu-id="9d27a-298">**現在のソリューション** オプション ボタンをオンにします。</span><span class="sxs-lookup"><span data-stu-id="9d27a-298">Select the **Current solution** radio button.</span></span>
6.  <span data-ttu-id="9d27a-299">**OK** をクリックして閉じます。</span><span class="sxs-lookup"><span data-stu-id="9d27a-299">Click **OK** to close.</span></span> <span data-ttu-id="9d27a-300">プロジェクトがインポートされてを開くまで待機します。</span><span class="sxs-lookup"><span data-stu-id="9d27a-300">Wait for the project to be imported and opened.</span></span>
7.  <span data-ttu-id="9d27a-301">**ソリューション エクスプローラー**で新しいプロジェクトを選択して右クリックしてから、**スタートアップ オブジェクトとして設定**を選択します。</span><span class="sxs-lookup"><span data-stu-id="9d27a-301">In the **Solution Explorer**, select the new project, right-click, and then select **Set as startup project.**</span></span>
8.  <span data-ttu-id="9d27a-302">**ソリューション エクスプローラー**で **FMRentalDetails** メニュー項目を右クリックしてから、**スタートアップ オブジェクトとして設定**を選択します。</span><span class="sxs-lookup"><span data-stu-id="9d27a-302">In the **Solution Explorer**, right-click **FMRentalDetails** menu item, and then select **Set as startup object.**</span></span>
9.  <span data-ttu-id="9d27a-303">ソリューション エクスプローラーでプロジェクトを選択し、右クリックしてから **レポートの展開** を選択します。</span><span class="sxs-lookup"><span data-stu-id="9d27a-303">Select the Project in Solution Explorer, right-click, and then select **Deploy Reports**</span></span>
10. <span data-ttu-id="9d27a-304">**Ctrl + F5** キーを押してレポートを表示します。</span><span class="sxs-lookup"><span data-stu-id="9d27a-304">Press **Ctrl + F5** to view the report.</span></span>

<span data-ttu-id="9d27a-305">[![FMRentalDetails レポート](./media/fmrentaldetails-report.png)](./media/fmrentaldetails-report.png)</span><span class="sxs-lookup"><span data-stu-id="9d27a-305">[![FMRentalDetails report](./media/fmrentaldetails-report.png)](./media/fmrentaldetails-report.png)</span></span> 

<span data-ttu-id="9d27a-306">このレポートでは、埋め込み VB スクリプトを使用して、実行中の合計を追跡し、前のページの残高を有効なページで参照できるようにします。</span><span class="sxs-lookup"><span data-stu-id="9d27a-306">This report uses embedded VB script to keep track of running totals so that the balances from the previous page can be referenced on the active page.</span></span> <span data-ttu-id="9d27a-307">レポートの VB コードを検査するには、Precision Designer でレポート デザインを読み込み、**レポート プロパティ** にアクセスし、**コード** セクションを選択します。</span><span class="sxs-lookup"><span data-stu-id="9d27a-307">To inspect report’s VB code, load the report design in the Precision Designer, access the **Report Properties**, and then select the **Code** section.</span></span> <span data-ttu-id="9d27a-308">ここで、レポートのヘッダーおよびフッター内で実行されているバランスを表すレポート デザインによって参照されるいくつかの機能が表示されます。</span><span class="sxs-lookup"><span data-stu-id="9d27a-308">Here you’ll see several functions referenced by the report designs to surface running balances within the report headers and footers.</span></span>

### <a name="advantages-of-ssrs-reports"></a><span data-ttu-id="9d27a-309">SSRS レポートのメリット</span><span class="sxs-lookup"><span data-stu-id="9d27a-309">Advantages of SSRS reports</span></span>

-   <span data-ttu-id="9d27a-310">電子メール サポート、バッチによるスケジュール実行、および印刷アーカイブを含む組み込みのバック オフィス ドキュメント管理機能</span><span class="sxs-lookup"><span data-stu-id="9d27a-310">Built-in back office document management capabilities including email support, scheduled executions via Batch, and Print Archive</span></span>
-   <span data-ttu-id="9d27a-311">Finance and Operations フォームやその他のレポートへドリルダウン ナビゲーション可能なパラメーター化されたビュー</span><span class="sxs-lookup"><span data-stu-id="9d27a-311">Parameterized views with drill-through navigations to Finance and Operations forms and other reports</span></span>
-   <span data-ttu-id="9d27a-312">地方自治体が規制するビジネス慣行に準拠した正確なドキュメントの作成に使用</span><span class="sxs-lookup"><span data-stu-id="9d27a-312">Used to produce precision documents for compliance with local regulatory business practices</span></span>





