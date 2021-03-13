---
title: 製造オーダーの完了レポート
description: この手順では、製造オーダーを完了として報告する方法を示します。
author: johanhoffmann
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProdTableListPage, ProdParmReportFinished, ProdJournalTransProd, ProdSetupReportFinished
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 5d9dcdbcb89df6430fb286c253ebecfc6d885af8
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/15/2021
ms.locfileid: "5011150"
---
# <a name="report-a-production-order-as-finished"></a><span data-ttu-id="f4b8b-103">製造オーダーの完了レポート</span><span class="sxs-lookup"><span data-stu-id="f4b8b-103">Report a production order as finished</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="f4b8b-104">この手順では、製造オーダーを完了として報告する方法を示します。</span><span class="sxs-lookup"><span data-stu-id="f4b8b-104">This procedure shows how to report a production order as finished.</span></span> <span data-ttu-id="f4b8b-105">この手順の作成に使用するデモ データの会社は USMF です。</span><span class="sxs-lookup"><span data-stu-id="f4b8b-105">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="f4b8b-106">これは、製造オーダーのライフ サイクルを説明する 7 個の手順の 6 番目です。</span><span class="sxs-lookup"><span data-stu-id="f4b8b-106">This is the sixth procedure out of seven which explains the production order lifecycle.</span></span>


## <a name="report-a-production-order-as-finished"></a><span data-ttu-id="f4b8b-107">製造オーダーの完了レポート</span><span class="sxs-lookup"><span data-stu-id="f4b8b-107">Report a production order as finished</span></span>
1. <span data-ttu-id="f4b8b-108">[生産管理] > [製造オーダー] > [すべての製造オーダー] の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="f4b8b-108">Go to Production control > Production orders > All production orders.</span></span>
    * <span data-ttu-id="f4b8b-109">[開始済] 状態を持つ製造オーダーを選択します。</span><span class="sxs-lookup"><span data-stu-id="f4b8b-109">Select a production order that has the Started status.</span></span>  
2. <span data-ttu-id="f4b8b-110">アクション ウィンドウで、[製造オーダー] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="f4b8b-110">On the Action Pane, click Production order.</span></span>
3. <span data-ttu-id="f4b8b-111">[完了レポート] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="f4b8b-111">Click Report as finished.</span></span>
    * <span data-ttu-id="f4b8b-112">このページでは、完了を報告する完成品の数量を確認できます。</span><span class="sxs-lookup"><span data-stu-id="f4b8b-112">On this page, you can confirm the quantity of the finished product to be reported as finished.</span></span>  
4. <span data-ttu-id="f4b8b-113">[一般] タブをクリックします。</span><span class="sxs-lookup"><span data-stu-id="f4b8b-113">Click the General tab.</span></span>
5. <span data-ttu-id="f4b8b-114">[良品数量] を「18」に設定します。</span><span class="sxs-lookup"><span data-stu-id="f4b8b-114">Set Good quantity to '18'.</span></span>
6. <span data-ttu-id="f4b8b-115">[不良数量] を「2」に設定します。</span><span class="sxs-lookup"><span data-stu-id="f4b8b-115">Set Error quantity to '2'.</span></span>
7. <span data-ttu-id="f4b8b-116">[エラーの原因] フィールドで、[材料] を選択します。</span><span class="sxs-lookup"><span data-stu-id="f4b8b-116">In the Error cause field, select 'Material'.</span></span>
8. <span data-ttu-id="f4b8b-117">[終了ジョブ] チェック ボックスをオンまたはオフにします。</span><span class="sxs-lookup"><span data-stu-id="f4b8b-117">Select or clear the End job check box.</span></span>
9. <span data-ttu-id="f4b8b-118">[適用エラー] チェック ボックスをオンまたはオフにします。</span><span class="sxs-lookup"><span data-stu-id="f4b8b-118">Select or clear the Accept error check box.</span></span>
10. <span data-ttu-id="f4b8b-119">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="f4b8b-119">Click OK.</span></span>

## <a name="verify-the-report-as-finished-journal"></a><span data-ttu-id="f4b8b-120">完了レポート仕訳帳の確認</span><span class="sxs-lookup"><span data-stu-id="f4b8b-120">Verify the Report as finished journal</span></span>
1. <span data-ttu-id="f4b8b-121">アクション ウィンドウで、[表示] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="f4b8b-121">On the Action Pane, click View.</span></span>
2. <span data-ttu-id="f4b8b-122">[完了報告済] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="f4b8b-122">Click Reported as finished.</span></span>
3. <span data-ttu-id="f4b8b-123">一覧で、選択された行をマークします。</span><span class="sxs-lookup"><span data-stu-id="f4b8b-123">In the list, mark the selected row.</span></span>
4. <span data-ttu-id="f4b8b-124">一覧で、選択された行のリンクをクリックします。</span><span class="sxs-lookup"><span data-stu-id="f4b8b-124">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="f4b8b-125">完了レポート仕訳帳が転記されます。</span><span class="sxs-lookup"><span data-stu-id="f4b8b-125">The Report as finished journal is posted.</span></span> <span data-ttu-id="f4b8b-126">仕訳帳に調整を加える場合は、新しい仕訳帳を作成し、この仕訳帳に手動で変更を加えることができます。</span><span class="sxs-lookup"><span data-stu-id="f4b8b-126">If you want to make adjustments to the journal, you can manually create  a new journal where you can make changes.</span></span>  

