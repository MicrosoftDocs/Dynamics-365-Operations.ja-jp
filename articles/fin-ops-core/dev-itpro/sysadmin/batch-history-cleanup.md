---
title: バッチジョブ履歴のクリーンアップ
description: このトピックでは、バッチ ジョブ履歴をクリーンアップする方法について情報を提供します。
author: hasaid
manager: AnnBe
ms.date: 03/12/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: IT Pro
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.custom: 62333
ms.assetid: 6135bcf7-bf8f-42ae-b2c6-458f6538e6a4
ms.search.region: Global
ms.author: hasaid
ms.search.validFrom: 2019-03-08
ms.dyn365.ops.version: Platform update 25
ms.openlocfilehash: 63b6ced4ebdb973afb44d60b1dee444e66e0046b
ms.sourcegitcommit: 75db3b75d35d27034f9b56e7119c9d0cb7666830
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/03/2019
ms.locfileid: "2550069"
---
# <a name="clean-up-the-batch-job-history"></a><span data-ttu-id="3d1db-103">バッチジョブ履歴のクリーンアップ</span><span class="sxs-lookup"><span data-stu-id="3d1db-103">Clean up the batch job history</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="3d1db-104">バッチ ジョブを実行すると、実行履歴が記録されます。</span><span class="sxs-lookup"><span data-stu-id="3d1db-104">When you run a batch job, a history is recorded.</span></span> <span data-ttu-id="3d1db-105">この履歴によって、ジョブが正しく実行されているか管理することができます。</span><span class="sxs-lookup"><span data-stu-id="3d1db-105">This history can be used to monitor the correct execution of jobs.</span></span> <span data-ttu-id="3d1db-106">複数のバッチ ジョブが作成されている場合で、特に実行頻度が高いバッチ ジョブには大量のジョブ実行履歴が生成されます。</span><span class="sxs-lookup"><span data-stu-id="3d1db-106">However, when several batch jobs have been created, especially batch jobs that have a high recurrence, lots of batch job history entries are generated.</span></span> <span data-ttu-id="3d1db-107">履歴テーブルにエントリが多すぎる場合は、将来的にジョブのパフォーマンス低下につながる可能性があります。</span><span class="sxs-lookup"><span data-stu-id="3d1db-107">Too many entries in the history table can negatively affect the performance of future jobs.</span></span>

<span data-ttu-id="3d1db-108">**システム管理**モジュールには2つのページが追加されており、バッチ ジョブ履歴のクリーンアップが容易になっています。</span><span class="sxs-lookup"><span data-stu-id="3d1db-108">Two pages that have been added to the **System administration** module make it easy to clean up the batch job history:</span></span>

- <span data-ttu-id="3d1db-109">バッチ ジョブ履歴のクリーンアップ</span><span class="sxs-lookup"><span data-stu-id="3d1db-109">Batch job history clean-up</span></span>
- <span data-ttu-id="3d1db-110">バッチ ジョブ履歴クリーンアップをカスタマイズする</span><span class="sxs-lookup"><span data-stu-id="3d1db-110">Custom batch job history clean-up</span></span>

![システム管理の定期処理タスク](./media/Menu-Cleanup.png)

> [!NOTE]
> <span data-ttu-id="3d1db-112">定期的にバッチ ジョブ履歴をクリーンアップすることと、この作業を業務時間外に行うことを推奨します。</span><span class="sxs-lookup"><span data-stu-id="3d1db-112">We recommend that you regularly clean up the batch job history, and that you do this cleanup outside of business hours.</span></span>

## <a name="batch-job-history-clean-up"></a><span data-ttu-id="3d1db-113">バッチ ジョブ履歴のクリーンアップ</span><span class="sxs-lookup"><span data-stu-id="3d1db-113">Batch job history clean-up</span></span>

<span data-ttu-id="3d1db-114">この手順では、指定した日数よりも古い履歴の全エントリを手早くクリーンアップします。</span><span class="sxs-lookup"><span data-stu-id="3d1db-114">Follow these steps to quickly clean up all history entries that are older than a specified number of days.</span></span>

1. <span data-ttu-id="3d1db-115">**システム管理の定期処理タスク** モジュールで、 **バッチ ジョブ履歴クリーンアップ** を選択します。</span><span class="sxs-lookup"><span data-stu-id="3d1db-115">On the **Periodic tasks in System administration** module, select **Batch job history clean-up**.</span></span>
2. <span data-ttu-id="3d1db-116">**履歴の範囲 (日数)** フィールドで、バッチ ジョブの履歴を保存する日数を指定します。</span><span class="sxs-lookup"><span data-stu-id="3d1db-116">In the **History limit (days)** field, specify the number of days to keep a history of batch jobs.</span></span>
3. <span data-ttu-id="3d1db-117">**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="3d1db-117">Select **OK**.</span></span>

![定期的なジョブ](./media/batch-cleanup-regular.png)

## <a name="batch-job-history-clean-up-custom"></a><span data-ttu-id="3d1db-119">バッチ ジョブ履歴のクリーンアップ (カスタマイズ)。</span><span class="sxs-lookup"><span data-stu-id="3d1db-119">Batch job history clean-up (custom)</span></span>

<span data-ttu-id="3d1db-120">カスタムのバッチ ジョブでは追加フィルターが適用され、ステータス、ジョブの概要、会社、またはユーザー名などのキーワードに基づいて抽出できます。</span><span class="sxs-lookup"><span data-stu-id="3d1db-120">The custom batch job lets you to apply additional filtering, based on criteria such as status, job description, company, or user.</span></span> <span data-ttu-id="3d1db-121">フィルター条件を追加するには、**フィルタ**ボタンを選択します。</span><span class="sxs-lookup"><span data-stu-id="3d1db-121">You can also add other filter criteria by selecting the **Filter** button.</span></span>

1. <span data-ttu-id="3d1db-122">**システム管理の定期処理タスク** モジュールで、 **バッチ ジョブ履歴クリーンアップ**  (カスマイズ) を選択します。</span><span class="sxs-lookup"><span data-stu-id="3d1db-122">On the **Periodic tasks in System administration** module, select **Batch job history clean-up (custom)**.</span></span>
2. <span data-ttu-id="3d1db-123">**履歴の範囲 (日数)** フィールドで、バッチ ジョブの履歴を保存する日数を指定します。</span><span class="sxs-lookup"><span data-stu-id="3d1db-123">In the **History limit (days)** field, specify the number of days to keep a history of batch jobs.</span></span>
3. <span data-ttu-id="3d1db-124">**レポートに含めるレコード** クイック タブで、必要なフィルタ条件を指定し **OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="3d1db-124">On the **Records to include** FastTab, specify any filter criteria that you require, and then select **OK**.</span></span>
4. <span data-ttu-id="3d1db-125">**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="3d1db-125">Select **OK**.</span></span>

![カスタマイズ ジョブ](./media/batch-cleanup-custom.png)
