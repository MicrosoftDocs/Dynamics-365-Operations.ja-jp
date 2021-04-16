---
title: ウェーブ処理用の倉庫パラメーター
description: このトピックでは、ウェーブ処理の倉庫パラメーターを設定する方法について説明します。 ウェーブ処理を使用すると、複数作業オーダーのピッキング作業を 1 つのウェーブにグループ化できます。
author: Mirzaab
ms.date: 03/08/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2021-03-08
ms.dyn365.ops.version: Release 10.0.18
ms.openlocfilehash: 77513185a3323a2e78f641d25b86b2896f9f7881
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/01/2021
ms.locfileid: "5838013"
---
# <a name="warehouse-parameters-for-wave-processing"></a><span data-ttu-id="e2da5-104">ウェーブ処理用の倉庫パラメーター</span><span class="sxs-lookup"><span data-stu-id="e2da5-104">Warehouse parameters for wave processing</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="e2da5-105">このトピックでは、ウェーブ処理の倉庫パラメーターを設定する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="e2da5-105">This topic describes how to set up warehouse parameters for wave processing.</span></span> <span data-ttu-id="e2da5-106">ウェーブ処理を使用すると、複数作業オーダーのピッキング作業を 1 つのウェーブにグループ化できます。</span><span class="sxs-lookup"><span data-stu-id="e2da5-106">You can use wave processing to group picking work for multiple work orders into a single wave.</span></span>

<span data-ttu-id="e2da5-107">作業処理を使用するには、**倉庫管理パラメータ** ページで次を指定します。</span><span class="sxs-lookup"><span data-stu-id="e2da5-107">To use wave processing, specify the following on the **Warehouse management parameters** page:</span></span>

- <span data-ttu-id="e2da5-108">バッチ ジョブを使用してウェーブを処理するかどうか。</span><span class="sxs-lookup"><span data-stu-id="e2da5-108">If you can process waves by using a batch job.</span></span>
- <span data-ttu-id="e2da5-109">ウェーブが処理されるときのログ ファイルの情報を集めるかどうか。</span><span class="sxs-lookup"><span data-stu-id="e2da5-109">If you collect information in a log file when waves are processed.</span></span>

## <a name="set-up-warehouse-management-parameters-for-wave-processing"></a><span data-ttu-id="e2da5-110">ウェーブ処理の倉庫管理パラメーターの設定</span><span class="sxs-lookup"><span data-stu-id="e2da5-110">Set up warehouse management parameters for wave processing</span></span>

<span data-ttu-id="e2da5-111">ウェーブ処理の倉庫パラメーターを設定するには、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="e2da5-111">To set up warehouse parameters for wave processing, follow these steps:</span></span>

1. <span data-ttu-id="e2da5-112">**倉庫管理** \> **設定** \> **倉庫管理パラメーター** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="e2da5-112">Go to **Warehouse management** \> **Setup** \> **Warehouse management parameters**.</span></span>

1. <span data-ttu-id="e2da5-113">**ウェーブ処理** クイック タブで、次の設定を行います。</span><span class="sxs-lookup"><span data-stu-id="e2da5-113">On the **Wave processing** FastTab, make the following settings:</span></span>

    - <span data-ttu-id="e2da5-114">**ウェーブ処理バッチ グループ** - バッチ ジョブを使用してウェーブを処理するときに使用する、バッチ グループを選択します。</span><span class="sxs-lookup"><span data-stu-id="e2da5-114">**Wave processing batch group** - Select the batch group to use when you process waves by using batch jobs.</span></span> <span data-ttu-id="e2da5-115">バッチ グループは、バッチ ジョブを実行するサーバーを指定します。</span><span class="sxs-lookup"><span data-stu-id="e2da5-115">The batch group specifies the server that batch jobs will run on.</span></span>
    - <span data-ttu-id="e2da5-116">**バッチでウェーブの処理** - バッチ ジョブでウェーブを自動処理を有効にするかどうかを選択します。</span><span class="sxs-lookup"><span data-stu-id="e2da5-116">**Process waves in batch** - Choose whether to enable waves to be automatically processed by a batch job.</span></span> <span data-ttu-id="e2da5-117">並列処理を使用するには、このオプションを *はい* に設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="e2da5-117">You must set this to *Yes* to use parallel processing.</span></span> <span data-ttu-id="e2da5-118">**ウェーブの処理** ページでバッチ ジョブで設定します。</span><span class="sxs-lookup"><span data-stu-id="e2da5-118">You set up the batch job on the **Process waves** page.</span></span> <span data-ttu-id="e2da5-119">(この一覧の最後にある注記も参照してください。)</span><span class="sxs-lookup"><span data-stu-id="e2da5-119">(See also the note at the end of this list.)</span></span>
    - <span data-ttu-id="e2da5-120">**ウェーブの処理ログを作成する** - 品目の配賦が開始および終了するごとにログ レコードを生成するかどうかを選択します。</span><span class="sxs-lookup"><span data-stu-id="e2da5-120">**Create wave progress log** - Choose whether the system should generate a log record every time allocation for an item and its dimensions begins and ends.</span></span> <span data-ttu-id="e2da5-121">このログは、最初のテスト中やトラブルシューティング時など、必要な場合にのみ有効にしてください。</span><span class="sxs-lookup"><span data-stu-id="e2da5-121">You should only enable this log when you need it, for example, during initial testing or for troubleshooting.</span></span> <span data-ttu-id="e2da5-122">詳細については、[ウェーブ配賦](wave-allocation-method.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="e2da5-122">For more information, see [Wave allocation](wave-allocation-method.md).</span></span>
    - <span data-ttu-id="e2da5-123">**ウェーブ処理履歴ログを作成する** - 保留中の配賦の並行処理中など、ウェーブの処理後にログ ファイルのウェーブに関する情報を自動的に保存するかどうかを選択します。</span><span class="sxs-lookup"><span data-stu-id="e2da5-123">**Create wave processing history log** - Choose whether to automatically save information about a wave in a log file after the wave is processed, including during the parallel processing of pending allocations.</span></span> <span data-ttu-id="e2da5-124">通常、間接費が追加されるので、この機能はトラブルシューティングにのみ有効にしてください。</span><span class="sxs-lookup"><span data-stu-id="e2da5-124">Typically you should only enable this during troubleshooting because it adds extra overhead.</span></span> <span data-ttu-id="e2da5-125">ログを表示するには、**倉庫管理 \> 出荷ウェーブ \> ウェーブ処理履歴ログ** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="e2da5-125">To view the log, go to **Warehouse management \> Outbound waves \> Wave processing history log**.</span></span> <span data-ttu-id="e2da5-126">ウェーブ処理の詳細については、[ウェーブの作成および処理](wave-processing.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="e2da5-126">For more information, see [Wave creation and processing](wave-processing.md).</span></span>
    - <span data-ttu-id="e2da5-127">**コンテナー詰め履歴ログの作成** - ウェーブの処理後に、ログ ファイル内のウェーブに対するコンテナー詰めに関する情報を自動的に保存するかどうかを選択します。</span><span class="sxs-lookup"><span data-stu-id="e2da5-127">**Create containerization history log** - Choose whether to automatically save information about containerization for a wave in a log file after the wave is processed.</span></span> <span data-ttu-id="e2da5-128">ログを表示するには、**倉庫管理 \> 梱包およびコンテナー詰め \> コンテナー詰め履歴** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="e2da5-128">To view the log, go to **Warehouse management \> Packing and containerization \> Containerization history**.</span></span>
    - <span data-ttu-id="e2da5-129">**ロックを待機 (ミリ秒)** - 配賦ステップが、他の配賦ステップでロックされたシステム リソースを待機する時間を、ミリ秒単位で入力します。</span><span class="sxs-lookup"><span data-stu-id="e2da5-129">**Wait for lock (ms)** - Enter the time, in milliseconds, that an allocation step will wait for a system resource that is locked by another allocation step.</span></span> <span data-ttu-id="e2da5-130">この時間を超えた場合、ウェーブは処理されず、エラー メッセージが表示されます。</span><span class="sxs-lookup"><span data-stu-id="e2da5-130">When this time is exceeded, the wave is not processed and an error message is displayed.</span></span>

1. <span data-ttu-id="e2da5-131">**倉庫にリリース** クイック タブで、次の設定を行います。</span><span class="sxs-lookup"><span data-stu-id="e2da5-131">On the **Release to warehouse** FastTab, make the following setting:</span></span>

    - <span data-ttu-id="e2da5-132">**バッチ失敗のエラー** - 倉庫バッチ ジョブへのリリースが失敗した場合にエラーを生成するかどうかを選択します。</span><span class="sxs-lookup"><span data-stu-id="e2da5-132">**Error on batch failure** - Choose whether to generate an error when a release to warehouse batch job fails.</span></span> <span data-ttu-id="e2da5-133">これを有効にすると、失敗したジョブの状態が *エラー* になります。</span><span class="sxs-lookup"><span data-stu-id="e2da5-133">If this is enabled, failed jobs will end with a status of *Error*.</span></span> <span data-ttu-id="e2da5-134">これを無効にすると、失敗したジョブの状態が *終了* になります。</span><span class="sxs-lookup"><span data-stu-id="e2da5-134">If this is disabled, failed jobs will end with a status of *Ended*.</span></span>

> [!NOTE]
> <span data-ttu-id="e2da5-135">ウェーブ処理に使用するウェーブ テンプレートで、ウェーブ処理を自動化する設定を指定できます。</span><span class="sxs-lookup"><span data-stu-id="e2da5-135">On the wave template that is used to process the wave, you can specify the settings that automate wave processing.</span></span> <span data-ttu-id="e2da5-136">バッチ ジョブのスケジュールを設定する場合、ウェーブ テンプレートの自動化の設定でタイミングを調整する必要があります。</span><span class="sxs-lookup"><span data-stu-id="e2da5-136">If you set up a schedule for the batch job, you should coordinate the timing with the settings for automation in the wave template.</span></span> <span data-ttu-id="e2da5-137">詳細については、[ウェーブ テンプレートの作成](wave-templates.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="e2da5-137">For more information, see [Create a wave template](wave-templates.md).</span></span>
>
> <span data-ttu-id="e2da5-138">*輸送管理* と *高度な倉庫管理* を使用する場合、ウェーブ処理時に積荷を連結するかどうか指定できます。</span><span class="sxs-lookup"><span data-stu-id="e2da5-138">If you are using *Transportation management* and *Advanced warehouse management*, you can specify whether to consolidate loads when you process a wave.</span></span> <span data-ttu-id="e2da5-139">たとえば、複数の小さな積荷を同時に出荷するときに便利です。</span><span class="sxs-lookup"><span data-stu-id="e2da5-139">For example, this is useful when several small loads can be shipped at the same time.</span></span> <span data-ttu-id="e2da5-140">ファイルを処理するときに負荷を連結するには、**積荷** タブで、**ウェーブ処理中に積荷を連結** チェック ボックスをオンにします。</span><span class="sxs-lookup"><span data-stu-id="e2da5-140">To consolidate loads when you process a wave, on the **Loads** tab, select the **Consolidate loads during wave processing** check box.</span></span></P>

## <a name="set-up-full-or-partial-reservation-for-production-waves"></a><span data-ttu-id="e2da5-141">生産ウェーブの完全または部分引当の設定</span><span class="sxs-lookup"><span data-stu-id="e2da5-141">Set up full or partial reservation for production waves</span></span>

<span data-ttu-id="e2da5-142">販売注文とかんばん注文では、棚卸資産は注文が倉庫にリリースされる前に引当する必要があります。</span><span class="sxs-lookup"><span data-stu-id="e2da5-142">For sales orders and kanban orders, inventory must be reserved before the order is released to the warehouse.</span></span> <span data-ttu-id="e2da5-143">そうしなければ、品門行または配賦行はウェーブで処理することはできません。</span><span class="sxs-lookup"><span data-stu-id="e2da5-143">Otherwise, the items or allocation lines cannot be processed in a wave.</span></span> <span data-ttu-id="e2da5-144">ただし、製造オーダーはもう少し柔軟です。</span><span class="sxs-lookup"><span data-stu-id="e2da5-144">However, production orders are slightly more flexible.</span></span> <span data-ttu-id="e2da5-145">製造オーダーでは、以下を指定できます。</span><span class="sxs-lookup"><span data-stu-id="e2da5-145">For production orders, you can specify the following:</span></span>

- <span data-ttu-id="e2da5-146">すべての材料を引当することができなくても、製造オーダーが倉庫にリリースされるようにします。</span><span class="sxs-lookup"><span data-stu-id="e2da5-146">Allow production orders to be released to the warehouse although all materials cannot be reserved.</span></span> <span data-ttu-id="e2da5-147">このオプションを選択する場合、追加の材料が使用可能になるときに、倉庫プロセスに手動でリリースを繰り返す必要があります。</span><span class="sxs-lookup"><span data-stu-id="e2da5-147">If you select this option, you must manually repeat the release to warehouse process when the additional materials become available.</span></span> <span data-ttu-id="e2da5-148">たとえば、生産を開始する必要がある材料があり、追加の材料が利用可能になるまで待機できる場合に役立ちます。</span><span class="sxs-lookup"><span data-stu-id="e2da5-148">For example, this is useful if you have the materials that you need to start a production, and can wait until the additional materials become available.</span></span>
- <span data-ttu-id="e2da5-149">注文が倉庫にリリースされる前に、すべての材料が引当される必要があります。</span><span class="sxs-lookup"><span data-stu-id="e2da5-149">Require that all materials are reserved before an order can be released to the warehouse.</span></span>

<span data-ttu-id="e2da5-150">完全引当を要求、または部分引当を許可するには、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="e2da5-150">To require full reservation or allow partial reservation, follow these steps:</span></span>

1. <span data-ttu-id="e2da5-151">**生産管理** \> **設定** \> **生産管理パラメーター** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="e2da5-151">Go to **Production control** \> **Setup** \> **Production control parameters**.</span></span>
1. <span data-ttu-id="e2da5-152">**全般** タブの **倉庫にリリース** フィールドで、既定の設定を選択します。</span><span class="sxs-lookup"><span data-stu-id="e2da5-152">On the **General** tab, in the **Release to warehouse** field, select the default setting.</span></span>
