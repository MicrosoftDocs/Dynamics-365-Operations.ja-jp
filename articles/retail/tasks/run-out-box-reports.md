--- 
title: "最初から用意されているレポートの生成および実行"
description: "このタスク ガイドを使用して、異なるワークスペースから本社の最初から用意されているレポート、および [小売 & コマース] の下にある [照会 & 販売] レポートを実行します。"
author: ashishmsft
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations, Retail
ms.search.region: Global
ms.search.industry: Retail
ms.author: asharchw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: a298ff9689b460bec0a4dcf53b3ca7de8e05fb10
ms.contentlocale: ja-jp
ms.lasthandoff: 04/13/2018

---
# <a name="generate-and-run-out-of-box-reports"></a><span data-ttu-id="f4de3-103">最初から用意されているレポートの生成および実行</span><span class="sxs-lookup"><span data-stu-id="f4de3-103">Generate and run out-of-box reports</span></span>

[!INCLUDE [task guide banner](../includes/task-guide-banner.md)]

<span data-ttu-id="f4de3-104">このタスク ガイドを使用して、異なるワークスペースから本社の最初から用意されているレポート、および [小売 & コマース] の下にある [照会 & 販売] レポートを実行します。</span><span class="sxs-lookup"><span data-stu-id="f4de3-104">Use this task guide to run out of box reports in headquarters from different workspaces and Inquiries & Sales reports located under Retail & Commerce.</span></span>



<span data-ttu-id="f4de3-105">この記録の作成に使用するデモ データの会社は USRT です。</span><span class="sxs-lookup"><span data-stu-id="f4de3-105">The demo data company used to create this recording is USRT.</span></span> <span data-ttu-id="f4de3-106">この記録は、システム管理者ロールを対象としています。</span><span class="sxs-lookup"><span data-stu-id="f4de3-106">This recording is intended for the System administrator role.</span></span>


## <a name="launch-reports-from-workspaces"></a><span data-ttu-id="f4de3-107">ワークスペースからレポートの起動</span><span class="sxs-lookup"><span data-stu-id="f4de3-107">Launch reports from workspaces</span></span>
1. <span data-ttu-id="f4de3-108">[小売りとコマース] > [製品とカテゴリ] > [カテゴリと製品の管理] に移動します。</span><span class="sxs-lookup"><span data-stu-id="f4de3-108">Go to Retail and commerce > Products and categories > Category and product management.</span></span>
2. <span data-ttu-id="f4de3-109">レポート セクションを展開または折りたたむには、矢印をクリックします。</span><span class="sxs-lookup"><span data-stu-id="f4de3-109">Click the arrow to expand or collapse the Reports section.</span></span>
3. <span data-ttu-id="f4de3-110">上位製品レポートをクリックします。</span><span class="sxs-lookup"><span data-stu-id="f4de3-110">Click Top products report.</span></span>
4. <span data-ttu-id="f4de3-111">[開始日] フィールドに日付を入力します。</span><span class="sxs-lookup"><span data-stu-id="f4de3-111">In the From date field, enter a date.</span></span>
5. <span data-ttu-id="f4de3-112">[終了日] フィールドで、日付を入力します。</span><span class="sxs-lookup"><span data-stu-id="f4de3-112">In the To date field, enter a date.</span></span>
6. <span data-ttu-id="f4de3-113">[チャンネル] フィールドで、ドロップ ダウン ボタンをクリックし、ルックアップを開きます。</span><span class="sxs-lookup"><span data-stu-id="f4de3-113">In the Channel field, click the drop-down button to open the lookup.</span></span>
7. <span data-ttu-id="f4de3-114">ツリーで、「Contoso Retail\Contoso Retail USA\Central\Houston」を選択します。</span><span class="sxs-lookup"><span data-stu-id="f4de3-114">In the tree, select 'Contoso Retail\Contoso Retail USA\Central\Houston'.</span></span>
    * <span data-ttu-id="f4de3-115">これは、[小売レポート用] の既定の小売組織階層を示します。</span><span class="sxs-lookup"><span data-stu-id="f4de3-115">This shows the default retail organization hierarchy for Retail reporting purpose.</span></span>   <span data-ttu-id="f4de3-116">[組織管理] > [組織] > [組織階層の目的] に移動し、[小売レポート] を選択し、[割り当て済の階層] で [既定の列] が選択されている階層名を確認します。</span><span class="sxs-lookup"><span data-stu-id="f4de3-116">Go to Organization administration >Organizations >Organization hierarchy purposes and choose Retail reporting and under Assigned hierarchies, check the hierarchy name for which Default column is checked.</span></span>      <span data-ttu-id="f4de3-117">デモ データの一部として (このタスクの記録に使用)、[地域ごとの小売店舗] が [小売レポート用] の既定の組織階層となっています。</span><span class="sxs-lookup"><span data-stu-id="f4de3-117">As part of demo data (used for this task recording) you would notice, Retail Stores by Region, is the default organization hierarchy for the Retail reporting purpose.</span></span>     
8. <span data-ttu-id="f4de3-118">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="f4de3-118">Click OK.</span></span>
9. <span data-ttu-id="f4de3-119">[ビュー] フィールドで、オプションを選択します。</span><span class="sxs-lookup"><span data-stu-id="f4de3-119">In the View field, select an option.</span></span>
10. <span data-ttu-id="f4de3-120">[By] フィールドで、オプションを選択します。</span><span class="sxs-lookup"><span data-stu-id="f4de3-120">In the By field, select an option.</span></span>
11. <span data-ttu-id="f4de3-121">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="f4de3-121">Click OK.</span></span>

## <a name="launch-reports-from-the-inquiries-and-sales-reports-located-under-retail--commerce-app-link"></a><span data-ttu-id="f4de3-122">[小売 & コマース] アプリ リンクの下にある照会と販売レポートからレポートを起動します。</span><span class="sxs-lookup"><span data-stu-id="f4de3-122">Launch reports from the inquiries and sales reports located under Retail & Commerce app link.</span></span>
1. <span data-ttu-id="f4de3-123">[小売とコマース] > [照会およびレポート] > [販売レポート] > [カテゴリ売上レポート] に移動します。</span><span class="sxs-lookup"><span data-stu-id="f4de3-123">Go to Retail and commerce > Inquiries and reports > Sales reports > Category sales report.</span></span>
2. <span data-ttu-id="f4de3-124">[開始日] フィールドに日付を入力します。</span><span class="sxs-lookup"><span data-stu-id="f4de3-124">In the From date field, enter a date.</span></span>
3. <span data-ttu-id="f4de3-125">[終了日] フィールドで、日付を入力します。</span><span class="sxs-lookup"><span data-stu-id="f4de3-125">In the To date field, enter a date.</span></span>
4. <span data-ttu-id="f4de3-126">[チャンネル] フィールドで、ドロップ ダウン ボタンをクリックし、ルックアップを開きます。</span><span class="sxs-lookup"><span data-stu-id="f4de3-126">In the Channel field, click the drop-down button to open the lookup.</span></span>
5. <span data-ttu-id="f4de3-127">ツリーで、「Contoso Retail\Contoso Retail USA\West\Seattle」を選択します。</span><span class="sxs-lookup"><span data-stu-id="f4de3-127">In the tree, select 'Contoso Retail\Contoso Retail USA\West\Seattle'.</span></span>
    * <span data-ttu-id="f4de3-128">これは、[小売レポート用] の既定の小売組織階層を示します。</span><span class="sxs-lookup"><span data-stu-id="f4de3-128">This shows the default retail organization hierarchy for Retail reporting purpose.</span></span>   <span data-ttu-id="f4de3-129">[組織管理] > [組織] > [組織階層の目的] に移動し、[小売レポート] を選択し、[割り当て済の階層] で [既定の列] が選択されている階層名を確認します。</span><span class="sxs-lookup"><span data-stu-id="f4de3-129">Go to Organization administration >Organizations >Organization hierarchy purposes and choose Retail reporting and under Assigned hierarchies, check the hierarchy name for which Default column is checked.</span></span>      <span data-ttu-id="f4de3-130">デモ データの一部として (このタスクの記録に使用)、[地域ごとの小売店舗] が [小売レポート用] の既定の組織階層となっています。</span><span class="sxs-lookup"><span data-stu-id="f4de3-130">As part of demo data (used for this task recording) you would notice, Retail Stores by Region, is the default organization hierarchy for the Retail reporting purpose.</span></span>     
6. <span data-ttu-id="f4de3-131">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="f4de3-131">Click OK.</span></span>
7. <span data-ttu-id="f4de3-132">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="f4de3-132">Click OK.</span></span>

## <a name="export-an-hq-reports"></a><span data-ttu-id="f4de3-133">[HQ レポート] をエクスポート</span><span class="sxs-lookup"><span data-stu-id="f4de3-133">Export an HQ reports</span></span>
1. <span data-ttu-id="f4de3-134">[小売とコマース] > [照会およびレポート] > [販売レポート] > [組織売上レポート] に移動します。</span><span class="sxs-lookup"><span data-stu-id="f4de3-134">Go to Retail and commerce > Inquiries and reports > Sales reports > Organization sales report.</span></span>
2. <span data-ttu-id="f4de3-135">[開始日] フィールドに日付を入力します。</span><span class="sxs-lookup"><span data-stu-id="f4de3-135">In the From date field, enter a date.</span></span>
3. <span data-ttu-id="f4de3-136">[終了日] フィールドで、日付を入力します。</span><span class="sxs-lookup"><span data-stu-id="f4de3-136">In the To date field, enter a date.</span></span>
4. <span data-ttu-id="f4de3-137">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="f4de3-137">Click OK.</span></span>
5. <span data-ttu-id="f4de3-138">[エクスポート] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="f4de3-138">Click Export.</span></span>
6. <span data-ttu-id="f4de3-139">PDF をクリックします。</span><span class="sxs-lookup"><span data-stu-id="f4de3-139">Click PDF.</span></span>


