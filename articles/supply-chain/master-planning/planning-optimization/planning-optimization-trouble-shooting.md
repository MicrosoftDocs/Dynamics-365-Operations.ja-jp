---
title: 計画最適化のトラブルシューティング
description: このトピックでは、計画の最適化を実行する際に発生する可能性がある問題の修正方法について説明します。
author: ChristianRytt
manager: tfehr
ms.date: 05/07/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqCreatePlanWorkspace
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2020-5-7
ms.dyn365.ops.version: AX 10.0.9
ms.openlocfilehash: c3dd0bf262f65aac2359c05ff954bdfbd294353f
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/13/2020
ms.locfileid: "4431743"
---
# <a name="troubleshoot-planning-optimization"></a><span data-ttu-id="1c4d5-103">計画最適化のトラブルシューティング</span><span class="sxs-lookup"><span data-stu-id="1c4d5-103">Troubleshoot Planning Optimization</span></span> 

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="1c4d5-104">このトピックでは、計画の最適化を実行する際に発生する可能性がある一般的な問題の修正方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="1c4d5-104">This topic describes how to fix common issues that you might encounter while working with Planning Optimization.</span></span>

## <a name="installation-of-the-planning-optimization-add-in-doesnt-complete"></a><span data-ttu-id="1c4d5-105">計画の最適化アドインのインストールが完了しない</span><span class="sxs-lookup"><span data-stu-id="1c4d5-105">Installation of the Planning Optimization add-in doesn't complete</span></span>

<span data-ttu-id="1c4d5-106">計画の最適化には、Dynamics 365 Supply Chain Management バージョン 10.0.7 以降で、Lifecycle Services (LCS) が有効な高可用性環境、Tier 2 以上（OneBox 環境ではありません）が必要です。</span><span class="sxs-lookup"><span data-stu-id="1c4d5-106">Planning Optimization requires a Lifecycle Services (LCS) enabled, high-availability environment, tier 2 or higher (not a OneBox environment), with Dynamics 365 Supply Chain Management version 10.0.7 or later.</span></span> <span data-ttu-id="1c4d5-107">アドインを OneBox 環境にインストールしようとしても、インストールが完了しない。</span><span class="sxs-lookup"><span data-stu-id="1c4d5-107">If you try to install the add-in on a OneBox environment, the installation won't complete.</span></span>

<span data-ttu-id="1c4d5-108">**修正**: インストールをキャンセルし、高可用性環境、Tier 2 以上 (OneBox 環境ではありません) を使用します。</span><span class="sxs-lookup"><span data-stu-id="1c4d5-108">**Fix**: Cancel the installation and use a high-availability environment, tier 2 or higher (not a OneBox environment).</span></span>

## <a name="planning-of-batch-jobs-fails-when-planning-optimization-is-enabled"></a><span data-ttu-id="1c4d5-109">計画の最適化を有効にすると、バッチジョブの計画が失敗する</span><span class="sxs-lookup"><span data-stu-id="1c4d5-109">Planning of batch jobs fails when Planning Optimization is enabled</span></span>

<span data-ttu-id="1c4d5-110">計画の最適化を有効にすると、組み込みのマスター プラン エンジンが自動的に無効になる。</span><span class="sxs-lookup"><span data-stu-id="1c4d5-110">When you enable Planning Optimization, the built-in master planning engine is automatically disabled.</span></span> <span data-ttu-id="1c4d5-111">組み込みの Supply Chain Management 計画エンジン用に作成されたマスター計画バッチ ジョブは、計画の最適化が有効な状態でトリガーされると失敗します。</span><span class="sxs-lookup"><span data-stu-id="1c4d5-111">Master planning batch jobs that were created for the built-in Supply Chain Management planning engine will fail if they are triggered while Planning Optimization is enabled.</span></span> <span data-ttu-id="1c4d5-112">*この操作は、計画の最適化が有効な場合に対応していないマスター計画をトリガーしました* のようなメッセージが表示される場合があります。</span><span class="sxs-lookup"><span data-stu-id="1c4d5-112">You may receive an error message such as *This operation triggered master planning that isn't supported when Planning Optimization is enabled*.</span></span>

<span data-ttu-id="1c4d5-113">**修正**:組み込みの Supply Chain Management プラン エンジンに対して作成されたすべてのマスター計画バッチ ジョブをキャンセルします。</span><span class="sxs-lookup"><span data-stu-id="1c4d5-113">**Fix**: Cancel all master planning batch jobs that were created for the built-in Supply Chain Management planning engine.</span></span>

## <a name="planning-optimization-results-are-different-from-earlier-results"></a><span data-ttu-id="1c4d5-114">計画の最適化の結果が、以前の結果とは異なる</span><span class="sxs-lookup"><span data-stu-id="1c4d5-114">Planning Optimization results are different from earlier results</span></span>

<span data-ttu-id="1c4d5-115">計画の最適化は、一部の領域における組み込みマスタープランのデザインとは異なります。</span><span class="sxs-lookup"><span data-stu-id="1c4d5-115">Planning Optimization differs from the built-in master planning design in some areas.</span></span> <span data-ttu-id="1c4d5-116">また、保留されている機能が原因で発生することもあります。</span><span class="sxs-lookup"><span data-stu-id="1c4d5-116">This can also be caused by pending features.</span></span>

<span data-ttu-id="1c4d5-117">**修正** : [分析計画の最適化] を実行して結果を分析し、関連ドキュメントを参照して影響を理解してください。</span><span class="sxs-lookup"><span data-stu-id="1c4d5-117">**Fix**: Run Planning Optimization fit analysis and then analyze the results while referring to the related documentation to understand the impact.</span></span> <span data-ttu-id="1c4d5-118">詳細については、[計画の最適化フィット分析](planning-optimization-fit-analysis.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="1c4d5-118">For more information, see [Planning Optimization fit analysis](planning-optimization-fit-analysis.md).</span></span>

## <a name="master-planning-doesnt-respect-the-coverage-time-fence"></a><span data-ttu-id="1c4d5-119">マスター計画では、補充タイム フェンスを考慮しません</span><span class="sxs-lookup"><span data-stu-id="1c4d5-119">Master planning doesn't respect the coverage time fence</span></span>

<span data-ttu-id="1c4d5-120">これは、最適化の計画の保留中の機能が原因で発生します。</span><span class="sxs-lookup"><span data-stu-id="1c4d5-120">This is caused by a pending feature for Planning Optimization.</span></span>

<span data-ttu-id="1c4d5-121">**修正**: 保留機能が利用できるようになるまで、計画された注文をフィルター処理または削除して、補充タイムフェンス以外からの提案を削除します。</span><span class="sxs-lookup"><span data-stu-id="1c4d5-121">**Fix**: Until the pending feature is available, filter or delete planned orders to remove supply suggestions outside of the coverage time fence.</span></span>

## <a name="cant-enable-planning-optimization"></a><span data-ttu-id="1c4d5-122">計画の最適化を有効化できない</span><span class="sxs-lookup"><span data-stu-id="1c4d5-122">Can't enable Planning Optimization</span></span>

<span data-ttu-id="1c4d5-123">**計画の最適化** を使用する設定を **はい** にする前に、**接続ステータス** を **接続済** とする必要があります。</span><span class="sxs-lookup"><span data-stu-id="1c4d5-123">The **Connection status** must be **Connected** before you can set **Use Planning Optimization** to **Yes**.</span></span> <span data-ttu-id="1c4d5-124">詳細については、[計画の最適化を開始する](get-started.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="1c4d5-124">For more information, see [Get started with Planning Optimization](get-started.md).</span></span>

<span data-ttu-id="1c4d5-125">**修正** : 計画最適化アドインが正常にインストールされていることを確認してください。</span><span class="sxs-lookup"><span data-stu-id="1c4d5-125">**Fix**: Make sure that the Planning Optimization add-in was installed successfully.</span></span>

## <a name="error-message-is-shown-during-ctp"></a><span data-ttu-id="1c4d5-126">CTP の実行中にエラーメッセージが表示される</span><span class="sxs-lookup"><span data-stu-id="1c4d5-126">Error message is shown during CTP</span></span>

<span data-ttu-id="1c4d5-127">計画の最適化が有効化されているときに、販売注文から生産可能在庫量 (CTP)を実行しようとすると、次のようなエラーメッセージが表示されます : *この操作は、プランニングの最適化が有効な場合に対応していないマスター計画をトリガーしました*。</span><span class="sxs-lookup"><span data-stu-id="1c4d5-127">If you try to run capable to promise (CTP) from a sales order when Planning Optimization is enabled, you will receive the following error message: *This operation triggered master planning that isn't supported when the Planning Optimization is enabled*.</span></span>

<span data-ttu-id="1c4d5-128">これは、製造オーダー サポートの一環として計画されている保留機能に関連しています。</span><span class="sxs-lookup"><span data-stu-id="1c4d5-128">This is related to a pending feature that is planned as part of the support for production orders.</span></span>

<span data-ttu-id="1c4d5-129">**修正 :** 計画の最適化を有効にしている場合は、CTP サポートが利用できるようになるまでは、CTP の計算を回避します。</span><span class="sxs-lookup"><span data-stu-id="1c4d5-129">**Fix:** Avoid CTP calculations when Planning Optimization is enabled until CTP support is available.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="1c4d5-130">追加リソース</span><span class="sxs-lookup"><span data-stu-id="1c4d5-130">Additional resources</span></span>

[<span data-ttu-id="1c4d5-131">計画最適化の開始</span><span class="sxs-lookup"><span data-stu-id="1c4d5-131">Get started with Planning Optimization</span></span>](get-started.md)

[<span data-ttu-id="1c4d5-132">計画最適化適合分析</span><span class="sxs-lookup"><span data-stu-id="1c4d5-132">Planning Optimization fit analysis</span></span>](planning-optimization-fit-analysis.md)
