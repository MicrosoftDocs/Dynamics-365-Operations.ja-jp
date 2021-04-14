---
title: 小売チャネルの財務分析コードの作成と店舗の分析コード値のコンフィギュレーション
description: この手順は、分析コード値を使用するコマース チャネルの財務分析コードの作成と店舗の財務分析コード値のコンフィギュレーションのステップについて説明します。
author: jashanno
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.region: Global
ms.search.industry: Retail
ms.author: jashanno
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 0212d3bd808b2a46fa30e8b2bdaa3c0b52ca0dd6
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/31/2021
ms.locfileid: "5790935"
---
# <a name="create-financial-dimensions-for-retail-channels-and-configure-dimension-values-on-stores"></a><span data-ttu-id="6b197-103">小売チャネルの財務分析コードの作成と店舗の分析コード値のコンフィギュレーション</span><span class="sxs-lookup"><span data-stu-id="6b197-103">Create financial dimensions for retail channels and configure dimension values on stores</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="6b197-104">この手順は、分析コード値を使用するコマース チャネルの財務分析コードの作成と店舗の財務分析コード値のコンフィギュレーションのステップについて説明します。</span><span class="sxs-lookup"><span data-stu-id="6b197-104">This procedure walks through creating a commerce channel financial dimension with dimension values and steps to configure financial dimension values on stores.</span></span> <span data-ttu-id="6b197-105">このトピックには、分析コード セットおよび勘定構造の作成などの関連手順は含まれません。</span><span class="sxs-lookup"><span data-stu-id="6b197-105">The topic does not include other related steps, such as creating dimension sets and account structures.</span></span> <span data-ttu-id="6b197-106">この手順では、デモ データの会社 USRT を使用します。</span><span class="sxs-lookup"><span data-stu-id="6b197-106">This procedure uses the USRT company in demo data.</span></span>

1. <span data-ttu-id="6b197-107">[総勘定元帳] > [勘定科目表] > [分析コード] > [財務分析コード] に移動します。</span><span class="sxs-lookup"><span data-stu-id="6b197-107">Go to General ledger > Chart of accounts > Dimensions > Financial dimensions.</span></span>
2. <span data-ttu-id="6b197-108">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="6b197-108">Click New.</span></span>
3. <span data-ttu-id="6b197-109">値の使用元フィールドで、'コマース チャネル' を選択します。</span><span class="sxs-lookup"><span data-stu-id="6b197-109">In the Use values from field, select 'Commerce channels'.</span></span>
4. <span data-ttu-id="6b197-110">[分析コード名] フィールドで、値を入力します。</span><span class="sxs-lookup"><span data-stu-id="6b197-110">In the Dimension name field, type a value.</span></span>
5. <span data-ttu-id="6b197-111">[有効化] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="6b197-111">Click Activate.</span></span>
6. <span data-ttu-id="6b197-112">[閉じる] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="6b197-112">Click Close.</span></span>
7. <span data-ttu-id="6b197-113">[有効化] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="6b197-113">Click Activate.</span></span>
8. <span data-ttu-id="6b197-114">[分析コード値] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="6b197-114">Click Dimension values.</span></span>
9. <span data-ttu-id="6b197-115">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="6b197-115">Close the page.</span></span>
10. <span data-ttu-id="6b197-116">[保存] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="6b197-116">Click Save.</span></span>
11. <span data-ttu-id="6b197-117">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="6b197-117">Close the page.</span></span>
12. <span data-ttu-id="6b197-118">Retail および Commerce > チャネル > 店舗 > すべての店舗の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="6b197-118">Go to Retail and Commerce > Channels > Stores > All stores.</span></span>
13. <span data-ttu-id="6b197-119">一覧で、選択された行のリンクをクリックします。</span><span class="sxs-lookup"><span data-stu-id="6b197-119">In the list, click the link in the selected row.</span></span>
14. <span data-ttu-id="6b197-120">[財務分析コード] セクションの展開を切り替えます。</span><span class="sxs-lookup"><span data-stu-id="6b197-120">Toggle the expansion of the Financial dimensions section.</span></span>
15. <span data-ttu-id="6b197-121">[編集] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="6b197-121">Click Edit.</span></span>
16. <span data-ttu-id="6b197-122">コマース チャネル フィールドで、ドロップ ダウン ボタンをクリックし、ルックアップを開きます。</span><span class="sxs-lookup"><span data-stu-id="6b197-122">In the Commerce channel field, click the drop-down button to open the lookup.</span></span>
17. <span data-ttu-id="6b197-123">リストで、更新された店舗の分析コード値を参照して選択します。</span><span class="sxs-lookup"><span data-stu-id="6b197-123">In the list, find and select the dimension value for the store being updated.</span></span>
18. <span data-ttu-id="6b197-124">一覧で、選択された行のリンクをクリックします。</span><span class="sxs-lookup"><span data-stu-id="6b197-124">In the list, click the link in the selected row.</span></span>
19. <span data-ttu-id="6b197-125">CostCenter フィールドで、ドロップ ダウン ボタンをクリックし、ルックアップを開きます。</span><span class="sxs-lookup"><span data-stu-id="6b197-125">In the CostCenter field, click the drop-down button to open the lookup.</span></span>
20. <span data-ttu-id="6b197-126">一覧で、目的のレコードを見つけ、選択します。</span><span class="sxs-lookup"><span data-stu-id="6b197-126">In the list, find and select the desired record.</span></span>
21. <span data-ttu-id="6b197-127">一覧で、選択された行のリンクをクリックします。</span><span class="sxs-lookup"><span data-stu-id="6b197-127">In the list, click the link in the selected row.</span></span>
22. <span data-ttu-id="6b197-128">[部門] フィールドで、ドロップ ダウン ボタンをクリックし、ルックアップを開きます。</span><span class="sxs-lookup"><span data-stu-id="6b197-128">In the Department field, click the drop-down button to open the lookup.</span></span>
23. <span data-ttu-id="6b197-129">一覧で、目的のレコードを見つけ、選択します。</span><span class="sxs-lookup"><span data-stu-id="6b197-129">In the list, find and select the desired record.</span></span>
24. <span data-ttu-id="6b197-130">一覧で、選択された行のリンクをクリックします。</span><span class="sxs-lookup"><span data-stu-id="6b197-130">In the list, click the link in the selected row.</span></span>
25. <span data-ttu-id="6b197-131">[保存] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="6b197-131">Click Save.</span></span>



[!INCLUDE[footer-include](../../includes/footer-banner.md)]