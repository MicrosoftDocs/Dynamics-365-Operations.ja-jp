---
title: ソース データの処理および追跡
description: すべてのデータ処理は、ジョブによって実行されます。
author: ShylaThompson
manager: AnnBe
ms.date: 06/27/2017
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 4363a51549503327e7decccf38c82db6e75acd88
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/15/2021
ms.locfileid: "4990645"
---
# <a name="process-and-trace-source-data"></a><span data-ttu-id="87baf-103">ソース データの処理および追跡</span><span class="sxs-lookup"><span data-stu-id="87baf-103">Process and trace source data</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="87baf-104">すべてのデータ処理は、ジョブによって実行されます。</span><span class="sxs-lookup"><span data-stu-id="87baf-104">All data processing is run by jobs.</span></span> <span data-ttu-id="87baf-105">各ジョブおよびデータ プロバイダーの場合、プロセスが実行され、そのエントリは現在のジョブで処理されたことを記録するために、仕訳帳が作成されます。</span><span class="sxs-lookup"><span data-stu-id="87baf-105">For each job and data provider, a journal is created to document that the process has been run, and that the entries were processed in the current job.</span></span> <span data-ttu-id="87baf-106">この手順を使用して、データ ソースを設定し、特定のコスト エントリの発生元を追跡します。</span><span class="sxs-lookup"><span data-stu-id="87baf-106">Use this procedure to set up a data source and then  trace the origin of a specific cost entry.</span></span> <span data-ttu-id="87baf-107">この記録では、USP2 デモ データ会社 USP2 を使用します。</span><span class="sxs-lookup"><span data-stu-id="87baf-107">This recording uses the USP2 demo data company USP2.</span></span> <span data-ttu-id="87baf-108">このタスクを完了する前に、次のタスク ガイドを再生し確認します。「原価会計元帳の作成」、「原価管理単位を定義」、および「原価会計元帳のデータ ソースを管理」。</span><span class="sxs-lookup"><span data-stu-id="87baf-108">Before you complete this task, make sure that you play the following task guides: "Create a cost accounting ledger," "Define cost control units," and "Manage data source for the cost accounting ledger."</span></span>

1. <span data-ttu-id="87baf-109">[原価計算] > [元帳の設定] > [原価会計元帳] へ、移動します。</span><span class="sxs-lookup"><span data-stu-id="87baf-109">Go to Cost accounting > Ledger setup > Cost accounting ledgers.</span></span>
2. <span data-ttu-id="87baf-110">一覧で、目的のレコードを見つけ、選択します。</span><span class="sxs-lookup"><span data-stu-id="87baf-110">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="87baf-111">以前に作成した原価会計元帳を、選択します。</span><span class="sxs-lookup"><span data-stu-id="87baf-111">Select the cost accounting ledger that you created earlier.</span></span>  
3. <span data-ttu-id="87baf-112">[実際のバージョン] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="87baf-112">Click Actual versions.</span></span>
4. <span data-ttu-id="87baf-113">[アクション ペイン] で、[ソース データの処理] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="87baf-113">On the Action Pane, click Source data processing.</span></span>
5. <span data-ttu-id="87baf-114">[一般会計エントリ振替仕訳帳] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="87baf-114">Click General ledger entry transfer journals.</span></span>
6. <span data-ttu-id="87baf-115">一覧で、目的のレコードを見つけ、選択します。</span><span class="sxs-lookup"><span data-stu-id="87baf-115">In the list, find and select the desired record.</span></span>
7. <span data-ttu-id="87baf-116">[仕訳入力] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="87baf-116">Click Journal entries.</span></span>
8. <span data-ttu-id="87baf-117">一覧で、選択された行をマークします。</span><span class="sxs-lookup"><span data-stu-id="87baf-117">In the list, mark the selected row.</span></span>
9. <span data-ttu-id="87baf-118">[原価エントリ] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="87baf-118">Click Cost entries.</span></span>
10. <span data-ttu-id="87baf-119">[ソース エントリ] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="87baf-119">Click Source entry.</span></span>
11. <span data-ttu-id="87baf-120">[アクション ペイン] で、[ソース データの処理] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="87baf-120">On the Action Pane, click Source data processing.</span></span>
12. <span data-ttu-id="87baf-121">[一般会計] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="87baf-121">Click General ledger.</span></span>
13. <span data-ttu-id="87baf-122">[会計カレンダー 期間] フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="87baf-122">In the Fiscal calendar period field, enter or select a value.</span></span>
    * <span data-ttu-id="87baf-123">この例の場合、[会計 2017 期間 9] を選択します。</span><span class="sxs-lookup"><span data-stu-id="87baf-123">For this example, select Fiscal 2017 Period 9.</span></span>  
14. <span data-ttu-id="87baf-124">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="87baf-124">Click OK.</span></span>

