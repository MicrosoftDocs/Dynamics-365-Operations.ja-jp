---
title: 原価会計元帳のデータ ソースの管理
description: 原価会計元帳の一般会計データ ソースを管理するには、この手順を使用します。
author: ShylaThompson
manager: AnnBe
ms.date: 06/27/2017
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 543c1cd4bbb35e51e17d5e0c7c588d87fbe3c106
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/27/2019
ms.locfileid: "2187708"
---
# <a name="manage-a-data-source-for-the-cost-accounting-ledger"></a><span data-ttu-id="b431b-103">原価会計元帳のデータ ソースの管理</span><span class="sxs-lookup"><span data-stu-id="b431b-103">Manage a data source for the cost accounting ledger</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="b431b-104">原価会計元帳の一般会計データ ソースを管理するには、この手順を使用します。</span><span class="sxs-lookup"><span data-stu-id="b431b-104">Use this procedure to manage the general ledger data source for a cost accounting ledger.</span></span> <span data-ttu-id="b431b-105">このタスクを完了する前に、タスク ガイドの「原価会計元帳の作成」と「原価管理単位を定義」を再生し確認します。</span><span class="sxs-lookup"><span data-stu-id="b431b-105">Before you complete this task, make sure that you play the "Create a cost accounting ledger" and "Define cost control units" task guides.</span></span> <span data-ttu-id="b431b-106">この記録では、USP2 デモ データ会社を使用します。</span><span class="sxs-lookup"><span data-stu-id="b431b-106">This recording uses the USP2 demo data company.</span></span>

1. <span data-ttu-id="b431b-107">[原価計算] > [元帳の設定] > [原価会計元帳] へ、移動します。</span><span class="sxs-lookup"><span data-stu-id="b431b-107">Go to Cost accounting > Ledger setup > Cost accounting ledgers.</span></span>
2. <span data-ttu-id="b431b-108">一覧で、目的のレコードを見つけ、選択します。</span><span class="sxs-lookup"><span data-stu-id="b431b-108">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="b431b-109">[実際のバージョン] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="b431b-109">Click Actual versions.</span></span>
4. <span data-ttu-id="b431b-110">[アクション] ウィンドウで、[管理] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="b431b-110">On the Action Pane, click Manage.</span></span>
5. <span data-ttu-id="b431b-111">[一般会計] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="b431b-111">Click General ledger.</span></span>
6. <span data-ttu-id="b431b-112">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="b431b-112">Click New.</span></span>
7. <span data-ttu-id="b431b-113">[名前] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="b431b-113">In the Name field, type a value.</span></span>
8. <span data-ttu-id="b431b-114">[データ プロバイダー] フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="b431b-114">In the Data provider field, enter or select a value.</span></span>
    * <span data-ttu-id="b431b-115">この例の場合、[Dynamics 365 Finance - 一般会計エントリ] を選択します。</span><span class="sxs-lookup"><span data-stu-id="b431b-115">For this example, select Dynamics 365 Finance - General ledger entries.</span></span>  
9. <span data-ttu-id="b431b-116">[原価要素分析コード] フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="b431b-116">In the Cost element dimension field, enter or select a value.</span></span>
    * <span data-ttu-id="b431b-117">この例の場合、[原価要素] を選択します。</span><span class="sxs-lookup"><span data-stu-id="b431b-117">For this example, select Cost elements.</span></span>  
10. <span data-ttu-id="b431b-118">[保存] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="b431b-118">Click Save.</span></span>
11. <span data-ttu-id="b431b-119">[コンフィギュレーション データー プロバイダー] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="b431b-119">Click Configure data provider.</span></span>
12. <span data-ttu-id="b431b-120">[法人] フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="b431b-120">In the Legal entity field, enter or select a value.</span></span>
    * <span data-ttu-id="b431b-121">この例の場合、[USP2] を選択します。</span><span class="sxs-lookup"><span data-stu-id="b431b-121">For this example, select USP2.</span></span>  
13. <span data-ttu-id="b431b-122">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="b431b-122">Click New.</span></span>
14. <span data-ttu-id="b431b-123">[転記階層] フィールドで、[現行] を選択します。</span><span class="sxs-lookup"><span data-stu-id="b431b-123">In the Posting layer field, select Current.</span></span>
15. <span data-ttu-id="b431b-124">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="b431b-124">Click OK.</span></span>
