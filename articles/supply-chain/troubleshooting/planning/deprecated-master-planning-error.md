---
title: 組み込みのマスター プラン エンジンを実行するとエラーが表示されます
description: 非推奨の組み込みのマスター プラン エンジンを実行するとエラー メッセージが表示されます。
author: ankubik
ms.date: 06/10/2021
ms.topic: troubleshooting
ms.search.form: Dialog_ReqCalcScheduleItemTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: ankubik
ms.search.validFrom: 2021-06-10
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 9c950292a4f43319d21a7deafdfb341b7bef15d8
ms.sourcegitcommit: 18ca2df785e9656fdd4e8c0734eca2b2624fda10
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/22/2021
ms.locfileid: "6294120"
---
# <a name="you-receive-an-error-when-running-the-built-in-master-planning-engine"></a><span data-ttu-id="e9ac2-103">組み込みのマスター プラン エンジンを実行するとエラーが表示されます</span><span class="sxs-lookup"><span data-stu-id="e9ac2-103">You receive an error when running the built-in master planning engine</span></span>

<span data-ttu-id="e9ac2-104">エラー コード: ReqCalcScheduleItemTablePlanningOptimizationFitError</span><span class="sxs-lookup"><span data-stu-id="e9ac2-104">Error code: ReqCalcScheduleItemTablePlanningOptimizationFitError</span></span>

## <a name="symptoms"></a><span data-ttu-id="e9ac2-105">現象</span><span class="sxs-lookup"><span data-stu-id="e9ac2-105">Symptoms</span></span>

<span data-ttu-id="e9ac2-106">非推奨の組み込みを使用してマスター プランを実行すると次のエラー メッセージが表示されます。</span><span class="sxs-lookup"><span data-stu-id="e9ac2-106">When you run master planning by using the deprecated built-in master planning engine, you receive the following error message:</span></span>

> <span data-ttu-id="e9ac2-107">このエラー メッセージが表示されるのは、組み込みマスター プラン エンジンが、計画の最適化によってサポートされているシナリオに使用されたためです。</span><span class="sxs-lookup"><span data-stu-id="e9ac2-107">You receive this error message because the built-in master planning engine was used for scenarios supported by Planning Optimization.</span></span> <span data-ttu-id="e9ac2-108">現在の組み込みのマスター プランは非推奨であるため、今すぐ計画の最適化に移行する必要があります。</span><span class="sxs-lookup"><span data-stu-id="e9ac2-108">You should migrate to Planning Optimization now, as the current built-in master planning will be deprecated.</span></span> <span data-ttu-id="e9ac2-109">このマスター プランの実行が正常に完了したことを確認します。</span><span class="sxs-lookup"><span data-stu-id="e9ac2-109">Note that this master planning run did complete successfully.</span></span> <span data-ttu-id="e9ac2-110">移行が保留中の機能に強い依存関係がある場合は、組み込みのマスター プラン エンジンの使用を継続することはできません。</span><span class="sxs-lookup"><span data-stu-id="e9ac2-110">In case your migration has strong dependencies on pending features, an exception to continued usage of the built-in master planning engine can be requested.</span></span> <span data-ttu-id="e9ac2-111">次のアンケートに記入して開始し、必要に応じて、計画の最適化への移行に関連する例外を要求してください。</span><span class="sxs-lookup"><span data-stu-id="e9ac2-111">Please complete the following questionnaire to get started and, if relevant, request an exception from migration to Planning Optimization.</span></span> [<span data-ttu-id="e9ac2-112">計画の最適化の移行と例外に関するアンケート</span><span class="sxs-lookup"><span data-stu-id="e9ac2-112">Planning Optimization migration and exception questionnaire</span></span>](https://go.microsoft.com/fwlink/?linkid=2144962)

## <a name="cause"></a><span data-ttu-id="e9ac2-113">原因</span><span class="sxs-lookup"><span data-stu-id="e9ac2-113">Cause</span></span>

<span data-ttu-id="e9ac2-114">計画を実行し、製造制御機能を使用しない場合は、計画の最適化への移行を考慮する必要があります。</span><span class="sxs-lookup"><span data-stu-id="e9ac2-114">If you run planning and don't use production control features, you should consider migrating to Planning Optimization.</span></span> <span data-ttu-id="e9ac2-115">組み込みのマスター プラン エンジンは非推奨になります。</span><span class="sxs-lookup"><span data-stu-id="e9ac2-115">The built-in master planning engine is being deprecated.</span></span> <span data-ttu-id="e9ac2-116">したがって、エラー メッセージを受け取ることなしに引き続き使用するには、Microsoft からの例外を適用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="e9ac2-116">Therefore, if you want to continue to use it without receiving the error message, you must apply for an exception from Microsoft.</span></span>

## <a name="resolution"></a><span data-ttu-id="e9ac2-117">解決策</span><span class="sxs-lookup"><span data-stu-id="e9ac2-117">Resolution</span></span>

<span data-ttu-id="e9ac2-118">計画の最適化に移行する方法の詳細、または例外を適用して非推奨の組み込みのプラン エンジンを引き続き使用できるようにする方法についての詳細については、[マスター プランの計画の最適化への移行](/dynamics365/supply-chain/master-planning/new-master-planning-engine) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="e9ac2-118">For more information about how to migrate to Planning Optimization, or how to apply for an exception so that you can continue to use the deprecated built-in planning engine instead, see [Migration to Planning Optimization for master planning](/dynamics365/supply-chain/master-planning/new-master-planning-engine).</span></span>
