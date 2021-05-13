---
title: 商品の品質の調査
description: このトピックでは、品質指示を処理する方法について示します。
author: perlynne
ms.date: 03/23/2021
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
ms.openlocfilehash: ec67e7864db12178c0f3cfe8b93d510a46e8a0d4
ms.sourcegitcommit: 8362f3bd32ce8b9a5af93c8e57daef732a93b19e
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2021
ms.locfileid: "5956137"
---
# <a name="inspect-the-quality-of-goods"></a><span data-ttu-id="63e80-103">商品の品質の調査</span><span class="sxs-lookup"><span data-stu-id="63e80-103">Inspect the quality of goods</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="63e80-104">このトピックでは、品質指示を処理する方法について示します。</span><span class="sxs-lookup"><span data-stu-id="63e80-104">This topic describes how to process quality orders.</span></span> <span data-ttu-id="63e80-105">品質検査は、通常、品質検査の担当者により実行されます。</span><span class="sxs-lookup"><span data-stu-id="63e80-105">Quality inspections are typically done by a quality clerk.</span></span>

<span data-ttu-id="63e80-106">標準のデモ データがインストールされている場合は、そのデータを使用してこのトピックの手順を完了できます。</span><span class="sxs-lookup"><span data-stu-id="63e80-106">If the standard demo data is installed, you can use it to complete the procedures in this topic.</span></span> <span data-ttu-id="63e80-107">デモ データを使用するには、開始する前に *USMF* 法人を選択する必要があります。</span><span class="sxs-lookup"><span data-stu-id="63e80-107">To use the demo data, select the *USMF* legal entity before you begin.</span></span> <span data-ttu-id="63e80-108">その後、発注書 *000016* を確認して、製品のレシートを転記する必要があります。</span><span class="sxs-lookup"><span data-stu-id="63e80-108">You must then confirm purchase order *000016* and post a product receipt.</span></span> <span data-ttu-id="63e80-109">品質指示は自動的に生成されます。</span><span class="sxs-lookup"><span data-stu-id="63e80-109">A quality order is automatically generated.</span></span>

## <a name="step-1-select-a-quality-order"></a><span data-ttu-id="63e80-110">手順 1: 品質指示を選択する</span><span class="sxs-lookup"><span data-stu-id="63e80-110">Step 1: Select a quality order</span></span>

<span data-ttu-id="63e80-111">品質指示を選択するには、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="63e80-111">To select a quality order, follow these steps.</span></span>

1. <span data-ttu-id="63e80-112">**在庫管理 \> 定期処理タスク \> 品質管理 \> 品質指示** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="63e80-112">Go to **Inventory management \> Periodic tasks \> Quality management \> Quality orders**.</span></span>
1. <span data-ttu-id="63e80-113">この手順を開始する前に生成された品質指示を選択します。</span><span class="sxs-lookup"><span data-stu-id="63e80-113">Select the quality order that was generated before you started this procedure.</span></span>

## <a name="step-2-record-test-results"></a><span data-ttu-id="63e80-114">手順 2: テスト結果を記録する</span><span class="sxs-lookup"><span data-stu-id="63e80-114">Step 2: Record test results</span></span>

<span data-ttu-id="63e80-115">テスト結果を記録するには、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="63e80-115">To record test results, follow these steps.</span></span>

1. <span data-ttu-id="63e80-116">**結果** を選択します。</span><span class="sxs-lookup"><span data-stu-id="63e80-116">Select **Results**.</span></span>
1. <span data-ttu-id="63e80-117">**編集** を選択します。</span><span class="sxs-lookup"><span data-stu-id="63e80-117">Select **Edit**.</span></span>
1. <span data-ttu-id="63e80-118">**結果数量** フィールドに数値を入力します。</span><span class="sxs-lookup"><span data-stu-id="63e80-118">In the **Result quantity** field, enter a number.</span></span>
1. <span data-ttu-id="63e80-119">**結果** フィールドで、目的の記録を選択します。</span><span class="sxs-lookup"><span data-stu-id="63e80-119">In the **Outcome** field, select the desired record.</span></span> <span data-ttu-id="63e80-120">この例では、結果は定義済の結果に基づいています。</span><span class="sxs-lookup"><span data-stu-id="63e80-120">In this example, the result is based on a predefined outcome.</span></span> <span data-ttu-id="63e80-121">通常、サイズまたは他の分析コードなどより詳細なテスト結果を記録します。</span><span class="sxs-lookup"><span data-stu-id="63e80-121">Usually, you will record a more specific test result, such as a size or other dimension.</span></span>
1. <span data-ttu-id="63e80-122">**保存** を選択します。</span><span class="sxs-lookup"><span data-stu-id="63e80-122">Select **Save**.</span></span>
1. <span data-ttu-id="63e80-123">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="63e80-123">Close the page.</span></span>

## <a name="step-3-validate-the-quality-order"></a><span data-ttu-id="63e80-124">手順 3: 品質指示を検証する</span><span class="sxs-lookup"><span data-stu-id="63e80-124">Step 3: Validate the quality order</span></span>

<span data-ttu-id="63e80-125">品質指示を検証するには、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="63e80-125">To validate the quality order, follow these steps.</span></span>

1. <span data-ttu-id="63e80-126">**検証** を選択します。</span><span class="sxs-lookup"><span data-stu-id="63e80-126">Select **Validate**.</span></span>
1. <span data-ttu-id="63e80-127">**検証者** フィールドで、検査を行うユーザーを選択します。</span><span class="sxs-lookup"><span data-stu-id="63e80-127">In the **Validated by** field, select the user who is doing the inspection.</span></span>
1. <span data-ttu-id="63e80-128">**選択** を選択します。</span><span class="sxs-lookup"><span data-stu-id="63e80-128">Select **Select**.</span></span>
1. <span data-ttu-id="63e80-129">**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="63e80-129">Select **OK**.</span></span>
1. <span data-ttu-id="63e80-130">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="63e80-130">Close the page.</span></span>

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
