--- 
title: "最初から用意されているレポートを生成および実行"
description: "このタスク ガイドを使用して、異なるワークスペースから本社の最初から用意されているレポート、および [小売 & コマース] の下にある [照会 & 販売] レポートを実行します。"
author: ashishmsft
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: RetailCategoryAndProductWorkspace, RetailOrgHierarchyTreeLookup, SrsReportViewerForm
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Retail
ms.author: asharchw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 0312b8cfadd45f8e59225e9daba78b9e216cff51
ms.openlocfilehash: b42f86fc243312d18654b1a048f9dffb29afd187
ms.contentlocale: ja-jp
ms.lasthandoff: 10/16/2018

---
# <a name="generate-and-run-out-of-box-reports"></a><span data-ttu-id="320d4-103">最初から用意されているレポートを生成および実行</span><span class="sxs-lookup"><span data-stu-id="320d4-103">Generate and run out of box reports</span></span>

[!include[task guide banner](../includes/task-guide-banner.md)]

<span data-ttu-id="320d4-104">このタスク ガイドを使用して、異なるワークスペースから本社の最初から用意されているレポート、および [小売 & コマース] の下にある [照会 & 販売] レポートを実行します。</span><span class="sxs-lookup"><span data-stu-id="320d4-104">Use this task guide to run out of box reports in headquarters from different workspaces and Inquiries & Sales reports located under Retail & Commerce.</span></span>



<span data-ttu-id="320d4-105">この記録の作成に使用するデモ データの会社は USRT です。</span><span class="sxs-lookup"><span data-stu-id="320d4-105">The demo data company used to create this recording is USRT.</span></span> <span data-ttu-id="320d4-106">この記録は、システム管理者ロールを対象としています。</span><span class="sxs-lookup"><span data-stu-id="320d4-106">This recording is intended for the System administrator role.</span></span>


## <a name="launch-reports-from-workspaces"></a><span data-ttu-id="320d4-107">ワークスペースからレポートの起動</span><span class="sxs-lookup"><span data-stu-id="320d4-107">Launch reports from workspaces</span></span>
1. <span data-ttu-id="320d4-108">[小売りとコマース] > [製品とカテゴリ] > [カテゴリと製品の管理] に移動します。</span><span class="sxs-lookup"><span data-stu-id="320d4-108">Go to Retail and commerce > Products and categories > Category and product management.</span></span>
2. <span data-ttu-id="320d4-109">レポート セクションを展開または折りたたむには、矢印をクリックします。</span><span class="sxs-lookup"><span data-stu-id="320d4-109">Click the arrow to expand or collapse the Reports section.</span></span>
3. <span data-ttu-id="320d4-110">上位製品レポートをクリックします。</span><span class="sxs-lookup"><span data-stu-id="320d4-110">Click Top products report.</span></span>
4. <span data-ttu-id="320d4-111">[開始日] フィールドに日付を入力します。</span><span class="sxs-lookup"><span data-stu-id="320d4-111">In the From date field, enter a date.</span></span>
5. <span data-ttu-id="320d4-112">[終了日] フィールドで、日付を入力します。</span><span class="sxs-lookup"><span data-stu-id="320d4-112">In the To date field, enter a date.</span></span>
6. <span data-ttu-id="320d4-113">[チャンネル] フィールドで、ドロップ ダウン ボタンをクリックし、ルックアップを開きます。</span><span class="sxs-lookup"><span data-stu-id="320d4-113">In the Channel field, click the drop-down button to open the lookup.</span></span>
7. <span data-ttu-id="320d4-114">ツリーで、「Contoso Retail\Contoso Retail USA\Central\Houston」を選択します。</span><span class="sxs-lookup"><span data-stu-id="320d4-114">In the tree, select 'Contoso Retail\Contoso Retail USA\Central\Houston'.</span></span>
    * <span data-ttu-id="320d4-115">これは、[小売レポート用] の既定の小売組織階層を示します。</span><span class="sxs-lookup"><span data-stu-id="320d4-115">This shows the default retail organization hierarchy for Retail reporting purpose.</span></span>   <span data-ttu-id="320d4-116">[組織管理] > [組織] > [組織階層の目的] に移動し、[小売レポート] を選択し、[割り当て済の階層] で [既定の列] が選択されている階層名を確認します。</span><span class="sxs-lookup"><span data-stu-id="320d4-116">Go to Organization administration >Organizations >Organization hierarchy purposes and choose Retail reporting and under Assigned hierarchies, check the hierarchy name for which Default column is checked.</span></span>      <span data-ttu-id="320d4-117">デモ データの一部として (このタスクの記録に使用)、[地域ごとの小売店舗] が [小売レポート用] の既定の組織階層となっています。</span><span class="sxs-lookup"><span data-stu-id="320d4-117">As part of demo data (used for this task recording) you would notice, Retail Stores by Region, is the default organization hierarchy for the Retail reporting purpose.</span></span>     
8. <span data-ttu-id="320d4-118">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="320d4-118">Click OK.</span></span>
9. <span data-ttu-id="320d4-119">[ビュー] フィールドで、オプションを選択します。</span><span class="sxs-lookup"><span data-stu-id="320d4-119">In the View field, select an option.</span></span>
10. <span data-ttu-id="320d4-120">[By] フィールドで、オプションを選択します。</span><span class="sxs-lookup"><span data-stu-id="320d4-120">In the By field, select an option.</span></span>
11. <span data-ttu-id="320d4-121">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="320d4-121">Click OK.</span></span>

## <a name="launch-reports-from-the-inquiries-and-sales-reports-located-under-retail--commerce-app-link"></a><span data-ttu-id="320d4-122">[小売 & コマース] アプリ リンクの下にある照会と販売レポートからレポートを起動します。</span><span class="sxs-lookup"><span data-stu-id="320d4-122">Launch reports from the inquiries and sales reports located under Retail & Commerce app link.</span></span>
1. <span data-ttu-id="320d4-123">[小売とコマース] > [照会およびレポート] > [販売レポート] > [カテゴリ売上レポート] に移動します。</span><span class="sxs-lookup"><span data-stu-id="320d4-123">Go to Retail and commerce > Inquiries and reports > Sales reports > Category sales report.</span></span>
2. <span data-ttu-id="320d4-124">[開始日] フィールドに日付を入力します。</span><span class="sxs-lookup"><span data-stu-id="320d4-124">In the From date field, enter a date.</span></span>
3. <span data-ttu-id="320d4-125">[終了日] フィールドで、日付を入力します。</span><span class="sxs-lookup"><span data-stu-id="320d4-125">In the To date field, enter a date.</span></span>
4. <span data-ttu-id="320d4-126">[チャンネル] フィールドで、ドロップ ダウン ボタンをクリックし、ルックアップを開きます。</span><span class="sxs-lookup"><span data-stu-id="320d4-126">In the Channel field, click the drop-down button to open the lookup.</span></span>
5. <span data-ttu-id="320d4-127">ツリーで、「Contoso Retail\Contoso Retail USA\West\Seattle」を選択します。</span><span class="sxs-lookup"><span data-stu-id="320d4-127">In the tree, select 'Contoso Retail\Contoso Retail USA\West\Seattle'.</span></span>
    * <span data-ttu-id="320d4-128">これは、[小売レポート用] の既定の小売組織階層を示します。</span><span class="sxs-lookup"><span data-stu-id="320d4-128">This shows the default retail organization hierarchy for Retail reporting purpose.</span></span>   <span data-ttu-id="320d4-129">[組織管理] > [組織] > [組織階層の目的] に移動し、[小売レポート] を選択し、[割り当て済の階層] で [既定の列] が選択されている階層名を確認します。</span><span class="sxs-lookup"><span data-stu-id="320d4-129">Go to Organization administration >Organizations >Organization hierarchy purposes and choose Retail reporting and under Assigned hierarchies, check the hierarchy name for which Default column is checked.</span></span>      <span data-ttu-id="320d4-130">デモ データの一部として (このタスクの記録に使用)、[地域ごとの小売店舗] が [小売レポート用] の既定の組織階層となっています。</span><span class="sxs-lookup"><span data-stu-id="320d4-130">As part of demo data (used for this task recording) you would notice, Retail Stores by Region, is the default organization hierarchy for the Retail reporting purpose.</span></span>     
6. <span data-ttu-id="320d4-131">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="320d4-131">Click OK.</span></span>
7. <span data-ttu-id="320d4-132">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="320d4-132">Click OK.</span></span>

## <a name="export-an-hq-reports"></a><span data-ttu-id="320d4-133">[HQ レポート] をエクスポート</span><span class="sxs-lookup"><span data-stu-id="320d4-133">Export an HQ reports</span></span>
1. <span data-ttu-id="320d4-134">[小売とコマース] > [照会およびレポート] > [販売レポート] > [組織売上レポート] に移動します。</span><span class="sxs-lookup"><span data-stu-id="320d4-134">Go to Retail and commerce > Inquiries and reports > Sales reports > Organization sales report.</span></span>
2. <span data-ttu-id="320d4-135">[開始日] フィールドに日付を入力します。</span><span class="sxs-lookup"><span data-stu-id="320d4-135">In the From date field, enter a date.</span></span>
3. <span data-ttu-id="320d4-136">[終了日] フィールドで、日付を入力します。</span><span class="sxs-lookup"><span data-stu-id="320d4-136">In the To date field, enter a date.</span></span>
4. <span data-ttu-id="320d4-137">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="320d4-137">Click OK.</span></span>
5. <span data-ttu-id="320d4-138">[エクスポート] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="320d4-138">Click Export.</span></span>
6. <span data-ttu-id="320d4-139">PDF をクリックします。</span><span class="sxs-lookup"><span data-stu-id="320d4-139">Click PDF.</span></span>


