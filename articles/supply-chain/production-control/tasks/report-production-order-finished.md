---
title: 製造オーダーの完了レポート
description: この手順では、製造オーダーを完了として報告する方法を示します。
author: johanhoffmann
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProdTableListPage, ProdParmReportFinished, ProdJournalTransProd
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 0a35c06874d41ac1209ab38d46227e21708dc03e
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/01/2019
ms.locfileid: "1838538"
---
# <a name="report-a-production-order-as-finished"></a><span data-ttu-id="d9ccc-103">製造オーダーの完了レポート</span><span class="sxs-lookup"><span data-stu-id="d9ccc-103">Report a production order as finished</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="d9ccc-104">この手順では、製造オーダーを完了として報告する方法を示します。</span><span class="sxs-lookup"><span data-stu-id="d9ccc-104">This procedure shows how to report a production order as finished.</span></span> <span data-ttu-id="d9ccc-105">この手順の作成に使用するデモ データの会社は USMF です。</span><span class="sxs-lookup"><span data-stu-id="d9ccc-105">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="d9ccc-106">これは、製造オーダーのライフ サイクルを説明する 7 個の手順の 6 番目です。</span><span class="sxs-lookup"><span data-stu-id="d9ccc-106">This is the sixth procedure out of seven which explains the production order lifecycle.</span></span>


## <a name="report-a-production-order-as-finished"></a><span data-ttu-id="d9ccc-107">製造オーダーの完了レポート</span><span class="sxs-lookup"><span data-stu-id="d9ccc-107">Report a production order as finished</span></span>
1. <span data-ttu-id="d9ccc-108">[生産管理] > [製造オーダー] > [すべての製造オーダー] の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="d9ccc-108">Go to Production control > Production orders > All production orders.</span></span>
    * <span data-ttu-id="d9ccc-109">[開始済] 状態を持つ製造オーダーを選択します。</span><span class="sxs-lookup"><span data-stu-id="d9ccc-109">Select a production order that has the Started status.</span></span>  
2. <span data-ttu-id="d9ccc-110">アクション ウィンドウで、[製造オーダー] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="d9ccc-110">On the Action Pane, click Production order.</span></span>
3. <span data-ttu-id="d9ccc-111">[完了レポート] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="d9ccc-111">Click Report as finished.</span></span>
    * <span data-ttu-id="d9ccc-112">このページでは、完了を報告する完成品の数量を確認できます。</span><span class="sxs-lookup"><span data-stu-id="d9ccc-112">On this page, you can confirm the quantity of the finished product to be reported as finished.</span></span>  
4. <span data-ttu-id="d9ccc-113">[一般] タブをクリックします。</span><span class="sxs-lookup"><span data-stu-id="d9ccc-113">Click the General tab.</span></span>
5. <span data-ttu-id="d9ccc-114">[良品数量] を「18」に設定します。</span><span class="sxs-lookup"><span data-stu-id="d9ccc-114">Set Good quantity to '18'.</span></span>
6. <span data-ttu-id="d9ccc-115">[不良数量] を「2」に設定します。</span><span class="sxs-lookup"><span data-stu-id="d9ccc-115">Set Error quantity to '2'.</span></span>
7. <span data-ttu-id="d9ccc-116">[エラーの原因] フィールドで、[材料] を選択します。</span><span class="sxs-lookup"><span data-stu-id="d9ccc-116">In the Error cause field, select 'Material'.</span></span>
8. <span data-ttu-id="d9ccc-117">[終了ジョブ] チェック ボックスをオンまたはオフにします。</span><span class="sxs-lookup"><span data-stu-id="d9ccc-117">Select or clear the End job check box.</span></span>
9. <span data-ttu-id="d9ccc-118">[適用エラー] チェック ボックスをオンまたはオフにします。</span><span class="sxs-lookup"><span data-stu-id="d9ccc-118">Select or clear the Accept error check box.</span></span>
10. <span data-ttu-id="d9ccc-119">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="d9ccc-119">Click OK.</span></span>

## <a name="verify-the-report-as-finished-journal"></a><span data-ttu-id="d9ccc-120">完了レポート仕訳帳の確認</span><span class="sxs-lookup"><span data-stu-id="d9ccc-120">Verify the Report as finished journal</span></span>
1. <span data-ttu-id="d9ccc-121">アクション ウィンドウで、[表示] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="d9ccc-121">On the Action Pane, click View.</span></span>
2. <span data-ttu-id="d9ccc-122">[完了報告済] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="d9ccc-122">Click Reported as finished.</span></span>
3. <span data-ttu-id="d9ccc-123">一覧で、選択された行をマークします。</span><span class="sxs-lookup"><span data-stu-id="d9ccc-123">In the list, mark the selected row.</span></span>
4. <span data-ttu-id="d9ccc-124">一覧で、選択された行のリンクをクリックします。</span><span class="sxs-lookup"><span data-stu-id="d9ccc-124">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="d9ccc-125">完了レポート仕訳帳が転記されます。</span><span class="sxs-lookup"><span data-stu-id="d9ccc-125">The Report as finished journal is posted.</span></span> <span data-ttu-id="d9ccc-126">仕訳帳に調整を加える場合は、新しい仕訳帳を作成し、この仕訳帳に手動で変更を加えることができます。</span><span class="sxs-lookup"><span data-stu-id="d9ccc-126">If you want to make adjustments to the journal, you can manually create  a new journal where you can make changes.</span></span>  

