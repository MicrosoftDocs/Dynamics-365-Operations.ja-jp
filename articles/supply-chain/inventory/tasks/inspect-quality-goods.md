---
title: 商品の品質の調査
description: このトピックでは、品質指示を処理する方法について説明します。
author: perlynne
ms.date: 08/01/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: InventQualityOrderTable, InventQualityOrderLineResults, HcmWorkerLookUp
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 47e7156e5c57d5f983564cc966b4108f1180ff8d
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/01/2021
ms.locfileid: "5825918"
---
# <a name="inspect-the-quality-of-goods"></a><span data-ttu-id="77e66-103">商品の品質の調査</span><span class="sxs-lookup"><span data-stu-id="77e66-103">Inspect the quality of goods</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="77e66-104">このトピックでは、品質指示を処理する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="77e66-104">This topic explains how to process a quality order.</span></span> <span data-ttu-id="77e66-105">デモ データの会社 USMF でこのガイドを実行できます。</span><span class="sxs-lookup"><span data-stu-id="77e66-105">You can run this guide in demo data company USMF.</span></span> <span data-ttu-id="77e66-106">このサンプル手順を開始する前に、発注書 "000016" を確認し、製品受領書を転記する必要があります。</span><span class="sxs-lookup"><span data-stu-id="77e66-106">Before you start this example procedure, you need to confirm purchase order "000016" and post a product receipt.</span></span> <span data-ttu-id="77e66-107">これにより、品質指示が自動的に作成されます。</span><span class="sxs-lookup"><span data-stu-id="77e66-107">This will automatically create a quality order.</span></span> <span data-ttu-id="77e66-108">品質検査は、通常、品質検査の担当者により実行されます。</span><span class="sxs-lookup"><span data-stu-id="77e66-108">Quality inspections are typically carried out by a quality clerk.</span></span>


## <a name="select-a-quality-order"></a><span data-ttu-id="77e66-109">品質指示の選択</span><span class="sxs-lookup"><span data-stu-id="77e66-109">Select a quality order</span></span>
1. <span data-ttu-id="77e66-110">ナビゲーション ウィンドウで **モジュール > 在庫管理 > 定期処理 > 品質管理 > 品質指示** に移動します。</span><span class="sxs-lookup"><span data-stu-id="77e66-110">In the navigation pane, go to **Modules > Inventory management > Periodic tasks > Quality management > Quality orders**.</span></span>
2. <span data-ttu-id="77e66-111">この手順を開始する前に作成された品質指示を選択します。</span><span class="sxs-lookup"><span data-stu-id="77e66-111">Select the quality order that was created before you started this procedure.</span></span>  

## <a name="record-test-results"></a><span data-ttu-id="77e66-112">テスト結果の記録</span><span class="sxs-lookup"><span data-stu-id="77e66-112">Record test results</span></span>
1. <span data-ttu-id="77e66-113">**結果** を選択します。</span><span class="sxs-lookup"><span data-stu-id="77e66-113">Select **Results**.</span></span>
2. <span data-ttu-id="77e66-114">**編集** を選択します。</span><span class="sxs-lookup"><span data-stu-id="77e66-114">Select **Edit**.</span></span>
3. <span data-ttu-id="77e66-115">**結果数量** フィールドに数値を入力します。</span><span class="sxs-lookup"><span data-stu-id="77e66-115">In the **Result quantity** field, enter a number.</span></span>
4. <span data-ttu-id="77e66-116">**結果** フィールドで、ドロップダウン メニューから目的のレコードを選択します。</span><span class="sxs-lookup"><span data-stu-id="77e66-116">In the **Outcome** field, select the desired record in the drop-down menu.</span></span>  
- <span data-ttu-id="77e66-117">この例では、結果は定義済の結果に基づいています。</span><span class="sxs-lookup"><span data-stu-id="77e66-117">In this example the result is based on a pre-defined outcome.</span></span> <span data-ttu-id="77e66-118">通常、サイズまたは他の分析コードなどより詳細なテスト結果を記録します。</span><span class="sxs-lookup"><span data-stu-id="77e66-118">Normally you would record a more specific test result, for example a size or other dimension.</span></span>  
5. <span data-ttu-id="77e66-119">**保存** を選択します。</span><span class="sxs-lookup"><span data-stu-id="77e66-119">Select **Save**.</span></span>
6. <span data-ttu-id="77e66-120">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="77e66-120">Close the page.</span></span>

## <a name="validate-the-quality-order"></a><span data-ttu-id="77e66-121">品質指示を検証する</span><span class="sxs-lookup"><span data-stu-id="77e66-121">Validate the quality order</span></span>
1. <span data-ttu-id="77e66-122">**検証** を選択します。</span><span class="sxs-lookup"><span data-stu-id="77e66-122">Select **Validate**.</span></span>
2. <span data-ttu-id="77e66-123">**検証者** フィールドで、ドロップダウン メニューから検査を実行するユーザーを選択します。</span><span class="sxs-lookup"><span data-stu-id="77e66-123">In the **Validated by** field, select the user performing the inspection from the drop-down menu.</span></span>  
3. <span data-ttu-id="77e66-124">**選択** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="77e66-124">Click **Select**.</span></span>
4. <span data-ttu-id="77e66-125">**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="77e66-125">Select **OK**.</span></span>
5. <span data-ttu-id="77e66-126">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="77e66-126">Close the page.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]