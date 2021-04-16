---
title: バッチ ジョブからの出荷の確認
description: このトピックでは、出荷準備が完了した転送注文を自動的に確認するバッチ ジョブの設定方法について説明します。
author: perlynne
ms.date: 07/31/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2020-07-31
ms.dyn365.ops.version: Release 10.0.13
ms.openlocfilehash: 69e61e1c04dd72efbe1d2f028c078100e07176f6
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/01/2021
ms.locfileid: "5838445"
---
# <a name="confirm-outbound-shipments-from-batch-jobs"></a><span data-ttu-id="b6305-103">バッチ ジョブからの出荷の確認</span><span class="sxs-lookup"><span data-stu-id="b6305-103">Confirm outbound shipments from batch jobs</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="b6305-104">このトピックでは、出荷準備が完了した転送注文を自動的に確認するバッチ ジョブの設定方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="b6305-104">This topic describes how to set up a batch job that automatically confirms outbound transfer-order shipments for ready-to-ship loads.</span></span> <span data-ttu-id="b6305-105">ここで説明するバッチジョブは、販売注文に対してではなく、転送注文の出荷にのみ適用されます。</span><span class="sxs-lookup"><span data-stu-id="b6305-105">The batch job described here only applies to transfer order shipments, not to sales orders.</span></span>

## <a name="enable-the-confirm-outbound-shipments-from-batch-jobs-feature"></a><span data-ttu-id="b6305-106">バッチジョブからの出荷確認機能を有効にする</span><span class="sxs-lookup"><span data-stu-id="b6305-106">Enable the Confirm outbound shipments from batch jobs feature</span></span>

<span data-ttu-id="b6305-107">この機能を使用する前に、システム上で有効にする必要があります。</span><span class="sxs-lookup"><span data-stu-id="b6305-107">Before you can use this feature, it must be enabled on your system.</span></span> <span data-ttu-id="b6305-108">管理者は、[機能管理](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) ページで機能状態を確認し、必要に応じて有効化することができます。</span><span class="sxs-lookup"><span data-stu-id="b6305-108">Administrators can use the [Feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) page to check the feature status and enable it if needed.</span></span> <span data-ttu-id="b6305-109">この機能は次のように一覧表示されます :</span><span class="sxs-lookup"><span data-stu-id="b6305-109">The feature is listed as:</span></span>

- <span data-ttu-id="b6305-110">**モジュール** - *倉庫管理*</span><span class="sxs-lookup"><span data-stu-id="b6305-110">**Module** - *Warehouse management*</span></span>
- <span data-ttu-id="b6305-111">**機能名** - *バッチジョブから出荷を確認する*</span><span class="sxs-lookup"><span data-stu-id="b6305-111">**Feature name** - *Confirm outbound shipments from batch jobs*</span></span>

## <a name="process-outbound-shipments"></a><span data-ttu-id="b6305-112">出荷の処理</span><span class="sxs-lookup"><span data-stu-id="b6305-112">Process outbound shipments</span></span>

<span data-ttu-id="b6305-113">出荷の準備ができている積荷に対して、出荷確認の実行をスケジュール設定したバッチジョブを設定するには、次の操作を行います :</span><span class="sxs-lookup"><span data-stu-id="b6305-113">To set up a scheduled batch job to run the outbound shipment confirmation for loads that are ready to ship:</span></span>

1. <span data-ttu-id="b6305-114">**倉庫管理 \> 定期タスクは \> 出荷を処理する** に移動します。</span><span class="sxs-lookup"><span data-stu-id="b6305-114">Go to **Warehouse management \> Periodic tasks \> Process outbound shipments**.</span></span>
1. <span data-ttu-id="b6305-115">**出荷の確認** ダイアログ ボックスが開きます。</span><span class="sxs-lookup"><span data-stu-id="b6305-115">The **Confirm shipment** dialog box opens.</span></span> <span data-ttu-id="b6305-116">**対象に含めるレコード** クイック タブで、**フィルター** を選択します。</span><span class="sxs-lookup"><span data-stu-id="b6305-116">On the **Records to include** FastTab, select **Filter**.</span></span>
1. <span data-ttu-id="b6305-117">クエリ エディター ダイアログボックスが開きます。</span><span class="sxs-lookup"><span data-stu-id="b6305-117">The query editor dialog box opens.</span></span> <span data-ttu-id="b6305-118">**範囲** タブで、新しい行を追加して以下の値を設定します :</span><span class="sxs-lookup"><span data-stu-id="b6305-118">On the **Range** tab, add a row with the following values:</span></span>
    - <span data-ttu-id="b6305-119">**テーブル** - *積荷*</span><span class="sxs-lookup"><span data-stu-id="b6305-119">**Table** - *Loads*</span></span>
    - <span data-ttu-id="b6305-120">**派生テーブル** - *積荷*</span><span class="sxs-lookup"><span data-stu-id="b6305-120">**Derived table** - *Loads*</span></span>
    - <span data-ttu-id="b6305-121">**フィールド** - *積荷の状態*</span><span class="sxs-lookup"><span data-stu-id="b6305-121">**Field** - *Load status*</span></span>
    - <span data-ttu-id="b6305-122">**基準** - *積荷済*</span><span class="sxs-lookup"><span data-stu-id="b6305-122">**Criteria** - *Loaded*</span></span>
1. <span data-ttu-id="b6305-123">**OK** を選択して、**出荷確認** ダイアログ ボックスに戻ります。</span><span class="sxs-lookup"><span data-stu-id="b6305-123">Select **OK** to return to the **Confirm shipment** dialog box.</span></span>
1. <span data-ttu-id="b6305-124">**バックグラウンドで実行** クイックタブで、**バッチ処理** を **はい** に設定します。</span><span class="sxs-lookup"><span data-stu-id="b6305-124">On the **Run in the background** FastTab, set **Batch processing** to **Yes**.</span></span>
1. <span data-ttu-id="b6305-125">**バックグラウンドで実行** クイックタブで、**繰り返し** を選択します。</span><span class="sxs-lookup"><span data-stu-id="b6305-125">On the **Run in the background** FastTab, select **Recurrence**.</span></span>
1. <span data-ttu-id="b6305-126">**繰り返しの定義** ダイアログ ボックスが開きます。</span><span class="sxs-lookup"><span data-stu-id="b6305-126">The **Define recurrence** dialog box opens.</span></span> <span data-ttu-id="b6305-127">業務の要件に応じて実行スケジュールを設定します。</span><span class="sxs-lookup"><span data-stu-id="b6305-127">Set the run schedule as needed for your business.</span></span>
1. <span data-ttu-id="b6305-128">**OK** を選択して、**出荷確認** ダイアログ ボックスに戻ります。</span><span class="sxs-lookup"><span data-stu-id="b6305-128">Select **OK** to return to the **Confirm shipment** dialog box.</span></span>
1. <span data-ttu-id="b6305-129">**出荷の確認** ダイアログ ボックスの **OK** を選択し、バッチ ジョブをバッチキューに追加します。</span><span class="sxs-lookup"><span data-stu-id="b6305-129">Select **OK** on the **Confirm shipment** dialog box to add the batch job to the batch queue.</span></span>

<span data-ttu-id="b6305-130">詳細については、[バッチ処理の概要](../../fin-ops-core/dev-itpro/sysadmin/batch-processing-overview.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="b6305-130">For more information, see [Batch processing overview](../../fin-ops-core/dev-itpro/sysadmin/batch-processing-overview.md).</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]