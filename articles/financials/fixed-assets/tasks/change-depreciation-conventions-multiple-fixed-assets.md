---
title: 複数の固定資産の減価償却方法の変更
description: このタスクは、指定した固定資産グループに適用する減価償却方法を更新します。
author: saraschi2
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SysQueryForm, SrsReportViewerForm
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: a7a79b2edf64f0063253d3f2a23b0020eceb87c0
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/29/2019
ms.locfileid: "324264"
---
# <a name="change-depreciation-conventions-for-multiple-fixed-assets"></a><span data-ttu-id="f93ac-103">複数の固定資産の減価償却方法の変更</span><span class="sxs-lookup"><span data-stu-id="f93ac-103">Change depreciation conventions for multiple fixed assets</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="f93ac-104">このタスクは、指定した固定資産グループに適用する減価償却方法を更新します。</span><span class="sxs-lookup"><span data-stu-id="f93ac-104">This task updates the depreciation convention for a specified fixed asset group.</span></span> <span data-ttu-id="f93ac-105">このタスク ガイドでは、デモ会社 USMF を使用します。</span><span class="sxs-lookup"><span data-stu-id="f93ac-105">This task guide uses the USMF demo company.</span></span>

1. <span data-ttu-id="f93ac-106">[固定資産] > [定期処理のタスク] > [一括更新] の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="f93ac-106">Go to Fixed assets > Periodic tasks > Mass update</span></span>
2. <span data-ttu-id="f93ac-107">[減価償却簿] フィールドで、ドロップ ダウン ボタンをクリックし、ルックアップを開きます。</span><span class="sxs-lookup"><span data-stu-id="f93ac-107">In the Depreciation book field, click the drop-down button to open the lookup.</span></span>
3. <span data-ttu-id="f93ac-108">一覧で、選択された行のリンクをクリックします。</span><span class="sxs-lookup"><span data-stu-id="f93ac-108">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="f93ac-109">[資産利用開始日] フィールドで、日付を入力します。</span><span class="sxs-lookup"><span data-stu-id="f93ac-109">In the Placed in service start field, enter a date.</span></span>
5. <span data-ttu-id="f93ac-110">[資産利用終了日] フィールドで、日付を入力します。</span><span class="sxs-lookup"><span data-stu-id="f93ac-110">In the Placed in service end field, enter a date.</span></span>
    * <span data-ttu-id="f93ac-111">選択した減価償却簿に含まれる資産のうち、これらの日付の間に利用されていた資産のみが更新されます。</span><span class="sxs-lookup"><span data-stu-id="f93ac-111">Only assets that are a part of the select depreciation book and that have been placed in service between these dates will be updated.</span></span>  
6. <span data-ttu-id="f93ac-112">[現在の減価償却方法] フィールドで、オプションを選択します。</span><span class="sxs-lookup"><span data-stu-id="f93ac-112">In the Current depreciation convention field, select an option.</span></span>
    * <span data-ttu-id="f93ac-113">現在の減価償却方法がある資産のみ更新されます。</span><span class="sxs-lookup"><span data-stu-id="f93ac-113">Only assets that have the current depreciation convention will be updated.</span></span>  
7. <span data-ttu-id="f93ac-114">[新規減価償却方法] フィールドで、オプションを選択します。</span><span class="sxs-lookup"><span data-stu-id="f93ac-114">In the New depreciation convention field, select an option.</span></span>
    * <span data-ttu-id="f93ac-115">レポートの検証は、任意の出力先に印刷します。</span><span class="sxs-lookup"><span data-stu-id="f93ac-115">Verify the report will print to the desired destination.</span></span>  
8. <span data-ttu-id="f93ac-116">[対象に含めるレコード] セクションを展開します。</span><span class="sxs-lookup"><span data-stu-id="f93ac-116">Expand the Records to include section.</span></span>
9. <span data-ttu-id="f93ac-117">[フィルター] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="f93ac-117">Click Filter.</span></span>
10. <span data-ttu-id="f93ac-118">リストで、[固定資産グループ] を選択します。</span><span class="sxs-lookup"><span data-stu-id="f93ac-118">In the list, select the Fixed asset group.</span></span>
11. <span data-ttu-id="f93ac-119">[基準] フィールドで、ドロップ ダウン ボタンをクリックし、ルックアップを開きます。</span><span class="sxs-lookup"><span data-stu-id="f93ac-119">In the Criteria field, click the drop-down button to open the lookup.</span></span>
12. <span data-ttu-id="f93ac-120">目的の固定資産グループを選択します。</span><span class="sxs-lookup"><span data-stu-id="f93ac-120">Select the desired Fixed asset group.</span></span>
13. <span data-ttu-id="f93ac-121">一覧で、選択された行のリンクをクリックします。</span><span class="sxs-lookup"><span data-stu-id="f93ac-121">In the list, click the link in the selected row.</span></span>
14. <span data-ttu-id="f93ac-122">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="f93ac-122">Click OK.</span></span>
15. <span data-ttu-id="f93ac-123">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="f93ac-123">Click OK.</span></span>
    *  <span data-ttu-id="f93ac-124">処理結果は、一括更新のレポートに表示されます。</span><span class="sxs-lookup"><span data-stu-id="f93ac-124">Results of the process are shown on the Mass update report.</span></span>     

