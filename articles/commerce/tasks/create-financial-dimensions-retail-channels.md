---
title: 小売チャネルの財務分析コードの作成と店舗の分析コード値のコンフィギュレーション
description: この手順は、分析コード値を使用するコマース チャネルの財務分析コードの作成と店舗の財務分析コード値のコンフィギュレーションのステップについて説明します。
author: jashanno
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations, Retail
ms.search.region: Global
ms.search.industry: Retail
ms.author: jashanno
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 79abb6875e2f5b101410ca004b525c4b881621a2
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/01/2020
ms.locfileid: "3023171"
---
# <a name="create-financial-dimensions-for-retail-channels-and-configure-dimension-values-on-stores"></a><span data-ttu-id="2d026-103">小売チャネルの財務分析コードの作成と店舗の分析コード値のコンフィギュレーション</span><span class="sxs-lookup"><span data-stu-id="2d026-103">Create financial dimensions for retail channels and configure dimension values on stores</span></span>

[!include [task guide banner](../includes/task-guide-banner.md)]

<span data-ttu-id="2d026-104">この手順は、分析コード値を使用するコマース チャネルの財務分析コードの作成と店舗の財務分析コード値のコンフィギュレーションのステップについて説明します。</span><span class="sxs-lookup"><span data-stu-id="2d026-104">This procedure walks through creating a commerce channel financial dimension with dimension values and steps to configure financial dimension values on stores.</span></span> <span data-ttu-id="2d026-105">このトピックには、分析コード セットおよび勘定構造の作成などの関連手順は含まれません。</span><span class="sxs-lookup"><span data-stu-id="2d026-105">The topic does not include other related steps, such as creating dimension sets and account structures.</span></span> <span data-ttu-id="2d026-106">この手順では、デモ データの会社 USRT を使用します。</span><span class="sxs-lookup"><span data-stu-id="2d026-106">This procedure uses the USRT company in demo data.</span></span>

1. <span data-ttu-id="2d026-107">[総勘定元帳] > [勘定科目表] > [分析コード] > [財務分析コード] に移動します。</span><span class="sxs-lookup"><span data-stu-id="2d026-107">Go to General ledger > Chart of accounts > Dimensions > Financial dimensions.</span></span>
2. <span data-ttu-id="2d026-108">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="2d026-108">Click New.</span></span>
3. <span data-ttu-id="2d026-109">値の使用元フィールドで、'コマース チャネル' を選択します。</span><span class="sxs-lookup"><span data-stu-id="2d026-109">In the Use values from field, select 'Commerce channels'.</span></span>
4. <span data-ttu-id="2d026-110">[分析コード名] フィールドで、値を入力します。</span><span class="sxs-lookup"><span data-stu-id="2d026-110">In the Dimension name field, type a value.</span></span>
5. <span data-ttu-id="2d026-111">[有効化] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="2d026-111">Click Activate.</span></span>
6. <span data-ttu-id="2d026-112">[閉じる] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="2d026-112">Click Close.</span></span>
7. <span data-ttu-id="2d026-113">[有効化] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="2d026-113">Click Activate.</span></span>
8. <span data-ttu-id="2d026-114">[分析コード値] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="2d026-114">Click Dimension values.</span></span>
9. <span data-ttu-id="2d026-115">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="2d026-115">Close the page.</span></span>
10. <span data-ttu-id="2d026-116">[保存] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="2d026-116">Click Save.</span></span>
11. <span data-ttu-id="2d026-117">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="2d026-117">Close the page.</span></span>
12. <span data-ttu-id="2d026-118">Retail および Commerce > チャネル > 店舗 > すべての店舗の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="2d026-118">Go to Retail and Commerce > Channels > Stores > All stores.</span></span>
13. <span data-ttu-id="2d026-119">一覧で、選択された行のリンクをクリックします。</span><span class="sxs-lookup"><span data-stu-id="2d026-119">In the list, click the link in the selected row.</span></span>
14. <span data-ttu-id="2d026-120">[財務分析コード] セクションの展開を切り替えます。</span><span class="sxs-lookup"><span data-stu-id="2d026-120">Toggle the expansion of the Financial dimensions section.</span></span>
15. <span data-ttu-id="2d026-121">[編集] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="2d026-121">Click Edit.</span></span>
16. <span data-ttu-id="2d026-122">コマース チャネル フィールドで、ドロップ ダウン ボタンをクリックし、ルックアップを開きます。</span><span class="sxs-lookup"><span data-stu-id="2d026-122">In the Commerce channel field, click the drop-down button to open the lookup.</span></span>
17. <span data-ttu-id="2d026-123">リストで、更新された店舗の分析コード値を参照して選択します。</span><span class="sxs-lookup"><span data-stu-id="2d026-123">In the list, find and select the dimension value for the store being updated.</span></span>
18. <span data-ttu-id="2d026-124">一覧で、選択された行のリンクをクリックします。</span><span class="sxs-lookup"><span data-stu-id="2d026-124">In the list, click the link in the selected row.</span></span>
19. <span data-ttu-id="2d026-125">CostCenter フィールドで、ドロップ ダウン ボタンをクリックし、ルックアップを開きます。</span><span class="sxs-lookup"><span data-stu-id="2d026-125">In the CostCenter field, click the drop-down button to open the lookup.</span></span>
20. <span data-ttu-id="2d026-126">一覧で、目的のレコードを見つけ、選択します。</span><span class="sxs-lookup"><span data-stu-id="2d026-126">In the list, find and select the desired record.</span></span>
21. <span data-ttu-id="2d026-127">一覧で、選択された行のリンクをクリックします。</span><span class="sxs-lookup"><span data-stu-id="2d026-127">In the list, click the link in the selected row.</span></span>
22. <span data-ttu-id="2d026-128">[部門] フィールドで、ドロップ ダウン ボタンをクリックし、ルックアップを開きます。</span><span class="sxs-lookup"><span data-stu-id="2d026-128">In the Department field, click the drop-down button to open the lookup.</span></span>
23. <span data-ttu-id="2d026-129">一覧で、目的のレコードを見つけ、選択します。</span><span class="sxs-lookup"><span data-stu-id="2d026-129">In the list, find and select the desired record.</span></span>
24. <span data-ttu-id="2d026-130">一覧で、選択された行のリンクをクリックします。</span><span class="sxs-lookup"><span data-stu-id="2d026-130">In the list, click the link in the selected row.</span></span>
25. <span data-ttu-id="2d026-131">[保存] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="2d026-131">Click Save.</span></span>

