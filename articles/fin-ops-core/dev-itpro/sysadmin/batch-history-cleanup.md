---
title: バッチジョブ履歴のクリーンアップ
description: このトピックでは、バッチ ジョブ履歴をクリーンアップする方法について情報を提供します。
author: Peakerbl
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
ms.author: peakerbl
ms.search.validFrom: 2019-03-08
ms.dyn365.ops.version: Platform update 25
ms.openlocfilehash: a31654a2b27809c09a48f25f7a70c99ab58b4c67
ms.sourcegitcommit: 65f4b8a751670a7fe9ef4cb8b218213f792d57a2
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/09/2020
ms.locfileid: "2945432"
---
# <a name="clean-up-the-batch-job-history"></a><span data-ttu-id="0dbfd-103">バッチジョブ履歴のクリーンアップ</span><span class="sxs-lookup"><span data-stu-id="0dbfd-103">Clean up the batch job history</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="0dbfd-104">バッチ ジョブを実行すると、実行履歴が記録されます。</span><span class="sxs-lookup"><span data-stu-id="0dbfd-104">When you run a batch job, a history is recorded.</span></span> <span data-ttu-id="0dbfd-105">この履歴によって、ジョブが正しく実行されているか管理することができます。</span><span class="sxs-lookup"><span data-stu-id="0dbfd-105">This history can be used to monitor the correct execution of jobs.</span></span> <span data-ttu-id="0dbfd-106">複数のバッチ ジョブが作成されている場合で、特に実行頻度が高いバッチ ジョブには大量のジョブ実行履歴が生成されます。</span><span class="sxs-lookup"><span data-stu-id="0dbfd-106">However, when several batch jobs have been created, especially batch jobs that have a high recurrence, lots of batch job history entries are generated.</span></span> <span data-ttu-id="0dbfd-107">履歴テーブルにエントリが多すぎる場合は、将来的にジョブのパフォーマンス低下につながる可能性があります。</span><span class="sxs-lookup"><span data-stu-id="0dbfd-107">Too many entries in the history table can negatively affect the performance of future jobs.</span></span>

<span data-ttu-id="0dbfd-108">**システム管理**モジュールには2つのページが追加されており、バッチ ジョブ履歴のクリーンアップが容易になっています。</span><span class="sxs-lookup"><span data-stu-id="0dbfd-108">Two pages that have been added to the **System administration** module make it easy to clean up the batch job history:</span></span>

- <span data-ttu-id="0dbfd-109">バッチ ジョブ履歴のクリーンアップ</span><span class="sxs-lookup"><span data-stu-id="0dbfd-109">Batch job history clean-up</span></span>
- <span data-ttu-id="0dbfd-110">バッチ ジョブ履歴クリーンアップをカスタマイズする</span><span class="sxs-lookup"><span data-stu-id="0dbfd-110">Custom batch job history clean-up</span></span>

![システム管理の定期処理タスク](./media/Menu-Cleanup.png)

> [!NOTE]
> <span data-ttu-id="0dbfd-112">定期的にバッチ ジョブ履歴をクリーンアップすることと、この作業を業務時間外に行うことを推奨します。</span><span class="sxs-lookup"><span data-stu-id="0dbfd-112">We recommend that you regularly clean up the batch job history, and that you do this cleanup outside of business hours.</span></span>

## <a name="batch-job-history-clean-up"></a><span data-ttu-id="0dbfd-113">バッチ ジョブ履歴のクリーンアップ</span><span class="sxs-lookup"><span data-stu-id="0dbfd-113">Batch job history clean-up</span></span>

<span data-ttu-id="0dbfd-114">この手順では、指定した日数よりも古い履歴の全エントリを手早くクリーンアップします。</span><span class="sxs-lookup"><span data-stu-id="0dbfd-114">Follow these steps to quickly clean up all history entries that are older than a specified number of days.</span></span>

1. <span data-ttu-id="0dbfd-115">**システム管理の定期処理タスク** モジュールで、 **バッチ ジョブ履歴クリーンアップ** を選択します。</span><span class="sxs-lookup"><span data-stu-id="0dbfd-115">On the **Periodic tasks in System administration** module, select **Batch job history clean-up**.</span></span>
2. <span data-ttu-id="0dbfd-116">**履歴の範囲 (日数)** フィールドで、バッチ ジョブの履歴を保存する日数を指定します。</span><span class="sxs-lookup"><span data-stu-id="0dbfd-116">In the **History limit (days)** field, specify the number of days to keep a history of batch jobs.</span></span>
3. <span data-ttu-id="0dbfd-117">**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="0dbfd-117">Select **OK**.</span></span>

![定期的なジョブ](./media/batch-cleanup-regular.png)

## <a name="batch-job-history-clean-up-custom"></a><span data-ttu-id="0dbfd-119">バッチ ジョブ履歴のクリーンアップ (カスタマイズ)。</span><span class="sxs-lookup"><span data-stu-id="0dbfd-119">Batch job history clean-up (custom)</span></span>

<span data-ttu-id="0dbfd-120">カスタムのバッチ ジョブでは追加フィルターが適用され、ステータス、ジョブの概要、会社、またはユーザー名などのキーワードに基づいて抽出できます。</span><span class="sxs-lookup"><span data-stu-id="0dbfd-120">The custom batch job lets you to apply additional filtering, based on criteria such as status, job description, company, or user.</span></span> <span data-ttu-id="0dbfd-121">フィルター条件を追加するには、**フィルタ**ボタンを選択します。</span><span class="sxs-lookup"><span data-stu-id="0dbfd-121">You can also add other filter criteria by selecting the **Filter** button.</span></span>

1. <span data-ttu-id="0dbfd-122">**システム管理の定期処理タスク** モジュールで、 **バッチ ジョブ履歴クリーンアップ**  (カスマイズ) を選択します。</span><span class="sxs-lookup"><span data-stu-id="0dbfd-122">On the **Periodic tasks in System administration** module, select **Batch job history clean-up (custom)**.</span></span>
2. <span data-ttu-id="0dbfd-123">**履歴の範囲 (日数)** フィールドで、バッチ ジョブの履歴を保存する日数を指定します。</span><span class="sxs-lookup"><span data-stu-id="0dbfd-123">In the **History limit (days)** field, specify the number of days to keep a history of batch jobs.</span></span>
3. <span data-ttu-id="0dbfd-124">**レポートに含めるレコード** クイック タブで、必要なフィルタ条件を指定し **OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="0dbfd-124">On the **Records to include** FastTab, specify any filter criteria that you require, and then select **OK**.</span></span>
4. <span data-ttu-id="0dbfd-125">**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="0dbfd-125">Select **OK**.</span></span>

![カスタマイズ ジョブ](./media/batch-cleanup-custom.png)
