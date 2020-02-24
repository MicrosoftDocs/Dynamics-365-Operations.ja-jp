---
title: 最初から用意されているレポートを生成および実行
description: このタスク ガイドを使用して、異なるワークスペースからバックオフィスの最初から用意されているレポート、およびコマースの照会 & 販売レポートを実行します。
author: ashishmsft
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: RetailCategoryAndProductWorkspace, RetailOrgHierarchyTreeLookup, SrsReportViewerForm
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Retail
ms.author: asharchw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 5f9931a39e4ca2141ed5b43086226c7fcc7cbd7c
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/01/2020
ms.locfileid: "3023145"
---
# <a name="generate-and-run-out-of-box-reports"></a><span data-ttu-id="92b53-103">最初から用意されているレポートを生成および実行</span><span class="sxs-lookup"><span data-stu-id="92b53-103">Generate and run out of box reports</span></span>

[!include[task guide banner](../includes/task-guide-banner.md)]

<span data-ttu-id="92b53-104">このタスク ガイドを使用して、異なるワークスペースからバックオフィスの最初から用意されているレポート、およびコマースの照会 & 販売レポートを実行します。</span><span class="sxs-lookup"><span data-stu-id="92b53-104">Use this task guide to run out of box reports in Headquarters from different workspaces and Inquiries & Sales reports located in Commerce.</span></span>

<span data-ttu-id="92b53-105">この記録の作成に使用するデモ データの会社は USRT です。</span><span class="sxs-lookup"><span data-stu-id="92b53-105">The demo data company used to create this recording is USRT.</span></span> <span data-ttu-id="92b53-106">この記録は、システム管理者ロールを対象としています。</span><span class="sxs-lookup"><span data-stu-id="92b53-106">This recording is intended for the System administrator role.</span></span>

## <a name="launch-reports-from-workspaces"></a><span data-ttu-id="92b53-107">ワークスペースからレポートの起動</span><span class="sxs-lookup"><span data-stu-id="92b53-107">Launch reports from workspaces</span></span>
1. <span data-ttu-id="92b53-108">Retail とコマース > 製品とカテゴリ > カテゴリと製品の管理に移動します。</span><span class="sxs-lookup"><span data-stu-id="92b53-108">Go to Retail and Commerce > Products and categories > Category and product management.</span></span>
2. <span data-ttu-id="92b53-109">レポート セクションを展開または折りたたむには、矢印をクリックします。</span><span class="sxs-lookup"><span data-stu-id="92b53-109">Click the arrow to expand or collapse the Reports section.</span></span>
3. <span data-ttu-id="92b53-110">上位製品レポートをクリックします。</span><span class="sxs-lookup"><span data-stu-id="92b53-110">Click Top products report.</span></span>
4. <span data-ttu-id="92b53-111">[開始日] フィールドに日付を入力します。</span><span class="sxs-lookup"><span data-stu-id="92b53-111">In the From date field, enter a date.</span></span>
5. <span data-ttu-id="92b53-112">[終了日] フィールドで、日付を入力します。</span><span class="sxs-lookup"><span data-stu-id="92b53-112">In the To date field, enter a date.</span></span>
6. <span data-ttu-id="92b53-113">[チャンネル] フィールドで、ドロップ ダウン ボタンをクリックし、ルックアップを開きます。</span><span class="sxs-lookup"><span data-stu-id="92b53-113">In the Channel field, click the drop-down button to open the lookup.</span></span>
7. <span data-ttu-id="92b53-114">ツリーで、「Contoso Retail\Contoso Retail USA\Central\Houston」を選択します。</span><span class="sxs-lookup"><span data-stu-id="92b53-114">In the tree, select 'Contoso Retail\Contoso Retail USA\Central\Houston'.</span></span>
    * <span data-ttu-id="92b53-115">これは、コマース レポート用の既定の組織階層を示します。</span><span class="sxs-lookup"><span data-stu-id="92b53-115">This shows the default organization hierarchy for Commerce reporting purpose.</span></span>   <span data-ttu-id="92b53-116">組織管理 > 組織 > 組織階層の目的に移動し、コマース レポートを選択し、割り当て済の階層で既定の列が選択されている階層名を確認します。</span><span class="sxs-lookup"><span data-stu-id="92b53-116">Go to Organization administration > Organizations > Organization hierarchy purposes and choose Commerce reporting and under Assigned hierarchies, check the hierarchy name for which Default column is checked.</span></span> <span data-ttu-id="92b53-117">デモ データの一部として (このタスクの記録に使用)、地域ごとの店舗がレポート用の既定の組織階層となっています。</span><span class="sxs-lookup"><span data-stu-id="92b53-117">As part of demo data (used for this task recording) you would notice, Stores by Region, is the default organization hierarchy for the reporting purpose.</span></span>     
8. <span data-ttu-id="92b53-118">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="92b53-118">Click OK.</span></span>
9. <span data-ttu-id="92b53-119">[ビュー] フィールドで、オプションを選択します。</span><span class="sxs-lookup"><span data-stu-id="92b53-119">In the View field, select an option.</span></span>
10. <span data-ttu-id="92b53-120">[By] フィールドで、オプションを選択します。</span><span class="sxs-lookup"><span data-stu-id="92b53-120">In the By field, select an option.</span></span>
11. <span data-ttu-id="92b53-121">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="92b53-121">Click OK.</span></span>

## <a name="launch-reports-from-the-inquiries-and-sales-reports"></a><span data-ttu-id="92b53-122">照会および販売レポートからのレポートを開始します</span><span class="sxs-lookup"><span data-stu-id="92b53-122">Launch reports from the inquiries and sales reports</span></span>
1. <span data-ttu-id="92b53-123">Retail とコマース > 照会およびレポート > 販売レポート > カテゴリ売上レポートに移動します。</span><span class="sxs-lookup"><span data-stu-id="92b53-123">Go to Retail and Commerce > Inquiries and reports > Sales reports > Category sales report.</span></span>
2. <span data-ttu-id="92b53-124">[開始日] フィールドに日付を入力します。</span><span class="sxs-lookup"><span data-stu-id="92b53-124">In the From date field, enter a date.</span></span>
3. <span data-ttu-id="92b53-125">[終了日] フィールドで、日付を入力します。</span><span class="sxs-lookup"><span data-stu-id="92b53-125">In the To date field, enter a date.</span></span>
4. <span data-ttu-id="92b53-126">[チャンネル] フィールドで、ドロップ ダウン ボタンをクリックし、ルックアップを開きます。</span><span class="sxs-lookup"><span data-stu-id="92b53-126">In the Channel field, click the drop-down button to open the lookup.</span></span>
5. <span data-ttu-id="92b53-127">ツリーで、「Contoso Retail\Contoso Retail USA\West\Seattle」を選択します。</span><span class="sxs-lookup"><span data-stu-id="92b53-127">In the tree, select 'Contoso Retail\Contoso Retail USA\West\Seattle'.</span></span>
    * <span data-ttu-id="92b53-128">これは、コマース レポート用の既定の組織階層を示します。</span><span class="sxs-lookup"><span data-stu-id="92b53-128">This shows the default organization hierarchy for Commerce reporting purpose.</span></span> <span data-ttu-id="92b53-129">組織管理 > 組織 > 組織階層の目的に移動し、コマース レポートを選択し、割り当て済の階層で既定の列が選択されている階層名を確認します。</span><span class="sxs-lookup"><span data-stu-id="92b53-129">Go to Organization administration > Organizations > Organization hierarchy purposes and choose Commerce reporting and under Assigned hierarchies, check the hierarchy name for which Default column is checked.</span></span> <span data-ttu-id="92b53-130">デモ データの一部として (このタスクの記録に使用)、地域ごとの店舗がレポート用の既定の組織階層となっています。</span><span class="sxs-lookup"><span data-stu-id="92b53-130">As part of demo data (used for this task recording) you would notice, Stores by Region, is the default organization hierarchy for the reporting purpose.</span></span>     
6. <span data-ttu-id="92b53-131">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="92b53-131">Click OK.</span></span>
7. <span data-ttu-id="92b53-132">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="92b53-132">Click OK.</span></span>

## <a name="export-an-hq-reports"></a><span data-ttu-id="92b53-133">[HQ レポート] をエクスポート</span><span class="sxs-lookup"><span data-stu-id="92b53-133">Export an HQ reports</span></span>
1. <span data-ttu-id="92b53-134">Retail とコマース > 照会およびレポート > 販売レポート > 組織売上レポートに移動します。</span><span class="sxs-lookup"><span data-stu-id="92b53-134">Go to Retail and Commerce > Inquiries and reports > Sales reports > Organization sales report.</span></span>
2. <span data-ttu-id="92b53-135">[開始日] フィールドに日付を入力します。</span><span class="sxs-lookup"><span data-stu-id="92b53-135">In the From date field, enter a date.</span></span>
3. <span data-ttu-id="92b53-136">[終了日] フィールドで、日付を入力します。</span><span class="sxs-lookup"><span data-stu-id="92b53-136">In the To date field, enter a date.</span></span>
4. <span data-ttu-id="92b53-137">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="92b53-137">Click OK.</span></span>
5. <span data-ttu-id="92b53-138">[エクスポート] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="92b53-138">Click Export.</span></span>
6. <span data-ttu-id="92b53-139">PDF をクリックします。</span><span class="sxs-lookup"><span data-stu-id="92b53-139">Click PDF.</span></span>

