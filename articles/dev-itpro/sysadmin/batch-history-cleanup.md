---
title: バッチジョブ履歴のクリーンアップ
description: ここではMicrosoft Dynamics 365 for Finance and Operationsにおいて、バッチ ジョブ履歴をクリーンアップする方法について情報を提供します。
author: hasaid
manager: AnnBe
ms.date: 03/12/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: IT Pro
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 62333
ms.assetid: 6135bcf7-bf8f-42ae-b2c6-458f6538e6a4
ms.search.region: Global
ms.author: hasaid
ms.search.validFrom: 2019-03-08
ms.dyn365.ops.version: Platform update 25
ms.openlocfilehash: 1fbb7dd6daea1ff2f5c44558e6f3705c6876458b
ms.sourcegitcommit: 2b890cd7a801055ab0ca24398efc8e4e777d4d8c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/07/2019
ms.locfileid: "1537335"
---
# <a name="clean-up-the-job-batch-history"></a><span data-ttu-id="4de69-103">バッチジョブ履歴のクリーンアップ</span><span class="sxs-lookup"><span data-stu-id="4de69-103">Clean up the job batch history</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="4de69-104">バッチ ジョブを実行すると、実行履歴が記録されます。</span><span class="sxs-lookup"><span data-stu-id="4de69-104">When you run a batch job, a history is recorded.</span></span> <span data-ttu-id="4de69-105">この履歴によって、ジョブが正しく実行されているか管理することができます。</span><span class="sxs-lookup"><span data-stu-id="4de69-105">This history can be used to monitor the correct execution of jobs.</span></span> <span data-ttu-id="4de69-106">複数のバッチ ジョブが作成されている場合で、特に実行頻度が高いバッチ ジョブには大量のジョブ実行履歴が生成されます。</span><span class="sxs-lookup"><span data-stu-id="4de69-106">However, when several batch jobs have been created, especially batch jobs that have a high recurrence, lots of batch job history entries are generated.</span></span> <span data-ttu-id="4de69-107">履歴テーブルにエントリが多すぎる場合は、将来的にジョブのパフォーマンス低下につながる可能性があります。</span><span class="sxs-lookup"><span data-stu-id="4de69-107">Too many entries in the history table can negatively affect the performance of future jobs.</span></span>

<span data-ttu-id="4de69-108">**システム管理**モジュールには2つのページが追加されており、バッチ ジョブ履歴のクリーンアップが容易になっています。</span><span class="sxs-lookup"><span data-stu-id="4de69-108">Two pages that have been added to the **System administration** module make it easy to clean up the batch job history:</span></span>

- <span data-ttu-id="4de69-109">バッチ ジョブ履歴のクリーンアップ</span><span class="sxs-lookup"><span data-stu-id="4de69-109">Batch job history clean-up</span></span>
- <span data-ttu-id="4de69-110">バッチ ジョブ履歴クリーンアップをカスタマイズする</span><span class="sxs-lookup"><span data-stu-id="4de69-110">Custom batch job history clean-up</span></span>

![システム管理の定期処理タスク](./media/Menu-Cleanup.png)

> [!NOTE]
> <span data-ttu-id="4de69-112">定期的にバッチ ジョブ履歴をクリーンアップすることと、この作業を業務時間外に行うことを推奨します。</span><span class="sxs-lookup"><span data-stu-id="4de69-112">We recommend that you regularly clean up the batch job history, and that you do this cleanup outside of business hours.</span></span>

## <a name="batch-job-history-clean-up"></a><span data-ttu-id="4de69-113">バッチ ジョブ履歴のクリーンアップ</span><span class="sxs-lookup"><span data-stu-id="4de69-113">Batch job history clean-up</span></span>

<span data-ttu-id="4de69-114">この手順では、指定した日数よりも古い履歴の全エントリを手早くクリーンアップします。</span><span class="sxs-lookup"><span data-stu-id="4de69-114">Follow these steps to quickly clean up all history entries that are older than a specified number of days.</span></span>

1. <span data-ttu-id="4de69-115">**システム管理の定期処理タスク** モジュールで、 **バッチ ジョブ履歴クリーンアップ** を選択します。</span><span class="sxs-lookup"><span data-stu-id="4de69-115">On the **Periodic tasks in System administration** module, select **Batch job history clean-up**.</span></span>
2. <span data-ttu-id="4de69-116">**履歴の範囲 (日数)** フィールドで、バッチ ジョブの履歴を保存する日数を指定します。</span><span class="sxs-lookup"><span data-stu-id="4de69-116">In the **History limit (days)** field, specify the number of days to keep a history of batch jobs.</span></span>
3. <span data-ttu-id="4de69-117">**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="4de69-117">Select **OK**.</span></span>

![定期的なジョブ](./media/batch-cleanup-regular.png)

## <a name="batch-job-history-clean-up-custom"></a><span data-ttu-id="4de69-119">バッチ ジョブ履歴のクリーンアップ (カスタマイズ)。</span><span class="sxs-lookup"><span data-stu-id="4de69-119">Batch job history clean-up (custom)</span></span>

<span data-ttu-id="4de69-120">カスタムのバッチ ジョブでは追加フィルターが適用され、ステータス、ジョブの概要、会社、またはユーザー名などのキーワードに基づいて抽出できます。</span><span class="sxs-lookup"><span data-stu-id="4de69-120">The custom batch job lets you to apply additional filtering, based on criteria such as status, job description, company, or user.</span></span> <span data-ttu-id="4de69-121">フィルター条件を追加するには、**フィルタ**ボタンを選択します。</span><span class="sxs-lookup"><span data-stu-id="4de69-121">You can also add other filter criteria by selecting the **Filter** button.</span></span>

1. <span data-ttu-id="4de69-122">**システム管理の定期処理タスク** モジュールで、 **バッチ ジョブ履歴クリーンアップ**  (カスマイズ) を選択します。</span><span class="sxs-lookup"><span data-stu-id="4de69-122">On the **Periodic tasks in System administration** module, select **Batch job history clean-up (custom)**.</span></span>
2. <span data-ttu-id="4de69-123">**履歴の範囲 (日数)** フィールドで、バッチ ジョブの履歴を保存する日数を指定します。</span><span class="sxs-lookup"><span data-stu-id="4de69-123">In the **History limit (days)** field, specify the number of days to keep a history of batch jobs.</span></span>
3. <span data-ttu-id="4de69-124">**レポートに含めるレコード** クイック タブで、必要なフィルタ条件を指定し **OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="4de69-124">On the **Records to include** FastTab, specify any filter criteria that you require, and then select **OK**.</span></span>
4. <span data-ttu-id="4de69-125">**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="4de69-125">Select **OK**.</span></span>

![カスタマイズ ジョブ](./media/batch-cleanup-custom.png)
