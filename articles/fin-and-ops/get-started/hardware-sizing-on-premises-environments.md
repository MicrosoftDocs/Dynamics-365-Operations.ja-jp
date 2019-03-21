---
title: オンプレミス環境のハードウェアのサイズ設定要件
description: このトピックでは、オンプレミス環境のハードウェアのサイズ設定要件を一覧表示します。
author: kfend
manager: AnnBe
ms.date: 06/23/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 55651
ms.assetid: ''
ms.search.region: Global
ms.author: chwolf
ms.search.validFrom: 2016-08-30
ms.dyn365.ops.version: Platform update 8
ms.openlocfilehash: e11742c62ea8d10f391ed2d417024f9c80e39591
ms.sourcegitcommit: 21bbdac152e0cbb0576df9d5e6e90283175834ef
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/26/2019
ms.locfileid: "768417"
---
# <a name="hardware-sizing-requirements-for-on-premises-environments"></a><span data-ttu-id="7875d-103">オンプレミス環境のハードウェアのサイズ設定要件</span><span class="sxs-lookup"><span data-stu-id="7875d-103">Hardware sizing requirements for on-premises environments</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="7875d-104">オンプレミス環境におけるハードウェアおよびインフラストラチャのサイズ設定のプロセスを開始する前に、[システム要件](system-requirements.md)および[セットアップおよび配置の指示](../../dev-itpro/deployment/setup-deploy-on-premises-environments.md)に精通し、基盤となるインフラストラクチャを確実に把握します。</span><span class="sxs-lookup"><span data-stu-id="7875d-104">Before you begin the hardware and infrastructure sizing process for an on-premises environment, familiarize yourself with the [System requirements](system-requirements.md) and [Setup and deployment instructions](../../dev-itpro/deployment/setup-deploy-on-premises-environments.md) to gain a solid understanding off the underlying infrastructure.</span></span>

> [!NOTE]
> <span data-ttu-id="7875d-105">最適なパフォーマンスを得るには、システム設定のベストプラクティスに十分注意します。</span><span class="sxs-lookup"><span data-stu-id="7875d-105">Pay close attention to the system setup best practices for optimum performance.</span></span>

<span data-ttu-id="7875d-106">ドキュメントを確認した後、トランザクションと同時実行ユーザー量の見積および平均コア スループットに基づいて、環境のサイズを変更するプロセスを開始できます。</span><span class="sxs-lookup"><span data-stu-id="7875d-106">After you have reviewed the documentation, you can start the process of estimating your transactional and concurrent user volume and sizing your environment based on the average core throughput.</span></span>

## <a name="factors-that-affect-sizing"></a><span data-ttu-id="7875d-107">サイズ設定に影響する要因</span><span class="sxs-lookup"><span data-stu-id="7875d-107">Factors that affect sizing</span></span>

<span data-ttu-id="7875d-108">次の図に示すようにすべての要素は、サイズ設定に寄与します。</span><span class="sxs-lookup"><span data-stu-id="7875d-108">All the factors shown in the following illustration contribute to sizing.</span></span> <span data-ttu-id="7875d-109">より詳細な情報が収集されるほど、より正確にサイジングを決定することができます。</span><span class="sxs-lookup"><span data-stu-id="7875d-109">The more detailed information that is collected, the more precisely you can determine sizing.</span></span> <span data-ttu-id="7875d-110">ハードウェアのサイジングは、データをサポートしていないため、不正確になる可能性があります。</span><span class="sxs-lookup"><span data-stu-id="7875d-110">Hardware sizing, without supporting data, is likely to be inaccurate.</span></span> <span data-ttu-id="7875d-111">必要なデータの絶対最小要件は、1 時間あたりの見積ピーク トランザクション明細行数です。</span><span class="sxs-lookup"><span data-stu-id="7875d-111">The absolute minimum requirement for necessary data is the peak transaction line load per hour.</span></span>

<span data-ttu-id="7875d-112">[![オンプレミス環境のハードウェアのサイズ設定](./media/lbd-sizing-01.png)](./media/lbd-sizing-01.png)</span><span class="sxs-lookup"><span data-stu-id="7875d-112">[![Hardware sizing for on-premises environments](./media/lbd-sizing-01.png)](./media/lbd-sizing-01.png)</span></span>

<span data-ttu-id="7875d-113">左から右に見ると、サイジングを正確に推定するために必要な最初の最も重要な要素は、トランザクション プロファイルまたはトランザクション特性です。</span><span class="sxs-lookup"><span data-stu-id="7875d-113">Viewed from left to right, the first and most important factor needed to accurately estimate sizing is a transaction profile or a transaction characterization.</span></span> <span data-ttu-id="7875d-114">1 時間あたりのピーク トランザクション量を常に検索することは重要です。</span><span class="sxs-lookup"><span data-stu-id="7875d-114">It's important to always find the peak transactional volume per hour.</span></span> <span data-ttu-id="7875d-115">複数のピーク期間がある場合は、これらの期間を正確に定義する必要があります。</span><span class="sxs-lookup"><span data-stu-id="7875d-115">If there are multiple peak periods, then these periods need to be accurately defined.</span></span>

<span data-ttu-id="7875d-116">インフラストラクチャに影響を及ぼす負荷を理解するようになると、これらの要因についてさらに詳しく理解する必要があります。</span><span class="sxs-lookup"><span data-stu-id="7875d-116">As you understand the load that impacts your infrastructure, you also need to understand more detail about these factors:</span></span>

- <span data-ttu-id="7875d-117">**トランザクション** ー 通常、トランザクションにはその日または週全体で一定のピークがあります。</span><span class="sxs-lookup"><span data-stu-id="7875d-117">**Transactions** – Typically transactions have certain peaks throughout the day/week.</span></span> <span data-ttu-id="7875d-118">これは、ほとんどの場合、トランザクション タイプに依存します。</span><span class="sxs-lookup"><span data-stu-id="7875d-118">This mostly depends on the transaction type.</span></span> <span data-ttu-id="7875d-119">時間と経費のエントリーでは、通常、1 週間に 1 回ピークを示しますが、販売注文票は、その日の統合またはトリクルによって一括して入荷されることがよくあります</span><span class="sxs-lookup"><span data-stu-id="7875d-119">Time and expense entries usually show peaks once per week, whereas Sales order entries often come in bulk via integration or trickle in during the day.</span></span>
- <span data-ttu-id="7875d-120">**同時ユーザー数** – 同時ユーザー数は、サイズを設定する上で 2 番目に重要な要因です。</span><span class="sxs-lookup"><span data-stu-id="7875d-120">**Number of concurrent users** – The number of concurrent users is the second most important sizing factor.</span></span> <span data-ttu-id="7875d-121">同時ユーザー数をベースにサイズ設定の見積もりを確実に取得することはできません。したがって、これが唯一のデータであれば、およその数を見積もり、さらなるデータを入手したときにこれを再度試行します。</span><span class="sxs-lookup"><span data-stu-id="7875d-121">You cannot reliably get sizing estimates based on the number of concurrent users, so if this is the only data you have available, estimate an approximate number, and then revisit this when you have more data.</span></span> <span data-ttu-id="7875d-122">正確な同時ユーザー定義は次の通りです。</span><span class="sxs-lookup"><span data-stu-id="7875d-122">An accurate concurrent user definition means that:</span></span>

    - <span data-ttu-id="7875d-123">名前付きユーザーは同時ユーザーではありません。</span><span class="sxs-lookup"><span data-stu-id="7875d-123">Named users are not concurrent users.</span></span>
    - <span data-ttu-id="7875d-124">同時ユーザーは、常に名前付きユーザーのサブセットです。</span><span class="sxs-lookup"><span data-stu-id="7875d-124">Concurrent users are always a subset of named users.</span></span> 
    - <span data-ttu-id="7875d-125">ピーク時の負荷は、最大の同時実行のサイズを定義します。</span><span class="sxs-lookup"><span data-stu-id="7875d-125">Peak workload defines the maximum concurrency for sizing.</span></span>

    <span data-ttu-id="7875d-126">同時ユーザーのための基準は、ユーザーが次のすべての条件を満たすことです。</span><span class="sxs-lookup"><span data-stu-id="7875d-126">Criteria for concurrent users is that the user meets all the following criteria:</span></span>

    - <span data-ttu-id="7875d-127">ログオンしています。</span><span class="sxs-lookup"><span data-stu-id="7875d-127">Logged on.</span></span>
    - <span data-ttu-id="7875d-128">棚卸時の作業トランザクション/お問い合わせ。</span><span class="sxs-lookup"><span data-stu-id="7875d-128">Working transactions/inquiries at the time of counting.</span></span>
    - <span data-ttu-id="7875d-129">アイドル セッションではありません。</span><span class="sxs-lookup"><span data-stu-id="7875d-129">Not an idle session.</span></span>

- <span data-ttu-id="7875d-130">**データ構成** – これは主に、システムのセットアップと設定方法に関するものです。</span><span class="sxs-lookup"><span data-stu-id="7875d-130">**Data composition** – This is mostly about how your system will be set up and configured.</span></span> <span data-ttu-id="7875d-131">たとえば、法人の数、アイテムの数、BOM レベルの数、セキュリティ設定の複雑さなどです。</span><span class="sxs-lookup"><span data-stu-id="7875d-131">For example, how many legal entities you will have, how many items, how many BOM levels, and how complex your security setup will be.</span></span> <span data-ttu-id="7875d-132">これらの要因のそれぞれはパフォーマンスにはほとんど影響しない可能性があるため、これらの要因はインフラストラクチャに関しては賢明な選択肢を使用することで相殺できます。</span><span class="sxs-lookup"><span data-stu-id="7875d-132">Each of those factors may have a small impact on performance, so these factors can be offset by using smart choices when it comes to infrastructure.</span></span>
- <span data-ttu-id="7875d-133">**拡張機能** – カスタマイズはシンプルまたは複雑になり得ます。</span><span class="sxs-lookup"><span data-stu-id="7875d-133">**Extensions** – Customizations can be simple or complex.</span></span> <span data-ttu-id="7875d-134">カスタマイズの数と複雑さと使用の性質は、必要なインフラストラクチャのサイズにさまざまな影響を与えます。</span><span class="sxs-lookup"><span data-stu-id="7875d-134">The number of customizations and the nature of complexity and usage has a varied impact on the size of the infrastructure needed.</span></span> <span data-ttu-id="7875d-135">複雑なカスタマイズの場合は、効率性のテストだけでなく、インフラストラクチャのニーズを理解するのに役立つように、パフォーマンス評価を行うことをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="7875d-135">For complex customizations, it's advised to conduct performance evaluations to ensure that they are not only tested for efficiency but also help understand the infrastructure needs.</span></span> <span data-ttu-id="7875d-136">拡張機能が、パフォーマンスとスケーラビリティにおけるベストプラクティスに従ってコード化されていない場合、これはさらに重要です。</span><span class="sxs-lookup"><span data-stu-id="7875d-136">This is even more critical when the extensions are not coded according to best practices for performance and scalability.</span></span>
- <span data-ttu-id="7875d-137">**レポートと分析** – これらの要因には、通常、Finance and Operations データベース システムのさまざまなデータベースに対する大量のクエリの実行が含まれます。</span><span class="sxs-lookup"><span data-stu-id="7875d-137">**Reporting and analytics** – These factors typically include running heavy queries against the various databases in the Finance and Operations database systems.</span></span> <span data-ttu-id="7875d-138">高価なレポートを実行する頻度を理解し、削減することで、レポートの影響を理解するのに役立ちます。</span><span class="sxs-lookup"><span data-stu-id="7875d-138">Understanding and reducing the frequency when expensive reports run will help you understand the impact of them.</span></span>
- <span data-ttu-id="7875d-139">**サード パーティのソリューション**1 – これらのソリューションは、ISV のように、拡張と同じ意味合いと推奨事項を持っています。</span><span class="sxs-lookup"><span data-stu-id="7875d-139">**Third-party solutions** – These solutions, like ISVs, have the same implications and recommendations as extensions.</span></span>

## <a name="sizing-your-finance-and-operations-environment"></a><span data-ttu-id="7875d-140">Finance and Operations 環境のサイジング</span><span class="sxs-lookup"><span data-stu-id="7875d-140">Sizing your Finance and Operations environment</span></span>

<span data-ttu-id="7875d-141">サイズの要件を理解するには、処理する必要があるトランザクションの最大使用量を把握する必要があります。</span><span class="sxs-lookup"><span data-stu-id="7875d-141">To understand your sizing requirements, you need to know the peak volume of transactions that you need to process.</span></span> <span data-ttu-id="7875d-142">Management Reporter や SSRS などのほとんどの補助システムは、ミッション クリティカルではありません。</span><span class="sxs-lookup"><span data-stu-id="7875d-142">Most auxiliary systems, like Management Reporter or SSRS, are less mission critical.</span></span> <span data-ttu-id="7875d-143">その結果、このドキュメントは主に AOS と SQL Server に焦点を当てています。</span><span class="sxs-lookup"><span data-stu-id="7875d-143">As a result, this document focuses mostly on AOS and SQL Server.</span></span>

> [!NOTE]
> <span data-ttu-id="7875d-144">一般に、計算層はスケールアウトされ、N + 1 形式で設定する必要があります。つまり、3 つの AOS を推定する場合は、4 つ目の AOS を追加します。</span><span class="sxs-lookup"><span data-stu-id="7875d-144">In general, the compute tiers scale out and should be set up in an N+1 fashion, meaning if you estimate three AOS, add a fourth AOS.</span></span> <span data-ttu-id="7875d-145">データベース層は、常に常時使用可能な設定で設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="7875d-145">The database tier should be set up in an Always On highly-available setup.</span></span>

## <a name="sql-server-oltp"></a><span data-ttu-id="7875d-146">SQL Server (OLTP)</span><span class="sxs-lookup"><span data-stu-id="7875d-146">SQL Server (OLTP)</span></span>

### <a name="sizing"></a><span data-ttu-id="7875d-147">サイズ変更</span><span class="sxs-lookup"><span data-stu-id="7875d-147">Sizing</span></span>

- <span data-ttu-id="7875d-148">1 時間あたり DB サーバー上のコアあたり 3K 〜 15K のトランザクション明細行。</span><span class="sxs-lookup"><span data-stu-id="7875d-148">3K to 15K transaction lines per hour per core on DB server.</span></span>
- <span data-ttu-id="7875d-149">プライマリー SQL Server の一般的な AOS と SQL のコア比率 3:1。</span><span class="sxs-lookup"><span data-stu-id="7875d-149">Typical AOS-to-SQL core ratio 3:1 for the primary SQL Server.</span></span> <span data-ttu-id="7875d-150">選択された高可用性構成に基づいて、追加のコアが必要です。</span><span class="sxs-lookup"><span data-stu-id="7875d-150">Additional cores are required based on the chosen high availability configuration.</span></span>

    - <span data-ttu-id="7875d-151">データベースに重い操作を処理すると、これが 2:1 に回帰する可能性があります。</span><span class="sxs-lookup"><span data-stu-id="7875d-151">Processing database-heavy operations may regress this to 2:1.</span></span>

- <span data-ttu-id="7875d-152">次の要因には、変動が影響します。</span><span class="sxs-lookup"><span data-stu-id="7875d-152">The following factors influence variations:</span></span>

    - <span data-ttu-id="7875d-153">使用中のパラメータ設定。</span><span class="sxs-lookup"><span data-stu-id="7875d-153">Parameter settings in use.</span></span>
    - <span data-ttu-id="7875d-154">拡張機能のレベル。</span><span class="sxs-lookup"><span data-stu-id="7875d-154">Levels of extensions.</span></span>
    - <span data-ttu-id="7875d-155">データベース ログやアラートなどの追加機能の使用。</span><span class="sxs-lookup"><span data-stu-id="7875d-155">Usage of additional functionality, such as database log and alerts.</span></span> <span data-ttu-id="7875d-156">極端なデータベース ロギングにより、コアあたりのスループットは 1 時間当たり 3K 以下にさらに低下します。</span><span class="sxs-lookup"><span data-stu-id="7875d-156">Extreme database logging will further reduce throughput per hour per core below 3K lines.</span></span>
    - <span data-ttu-id="7875d-157">データ構成の複雑さ - シンプルな勘定科目表と細かい綿密な勘定科目表は、スループットに影響を与えます。</span><span class="sxs-lookup"><span data-stu-id="7875d-157">Complexity of data composition – A simple chart of accounts versus a detailed fine-grained chart of accounts has implications on throughput (as an example).</span></span>
    - <span data-ttu-id="7875d-158">トランザクションの特性。</span><span class="sxs-lookup"><span data-stu-id="7875d-158">Transaction characterization.</span></span>
    - <span data-ttu-id="7875d-159">各コアの 2 GB から 16 BG までのメモリーです。</span><span class="sxs-lookup"><span data-stu-id="7875d-159">2 GB to 16 GB memory for each core.</span></span>
    - <span data-ttu-id="7875d-160">管理リポーターや SSRS データベースなどの DB サーバー上の補助データベース。</span><span class="sxs-lookup"><span data-stu-id="7875d-160">Auxiliary databases on DB server such as Management reporter and SSRS databases.</span></span>
    - <span data-ttu-id="7875d-161">Temp DB = 物理プロセッサと同数のファイルを持つ DB サイズの 15 ％。</span><span class="sxs-lookup"><span data-stu-id="7875d-161">Temp DB = 15% of DB size, with as many files as physical processors.</span></span>
    - <span data-ttu-id="7875d-162">同時のトランザクション ボリューム/使用量の合計に基づく SAN サイズとスループット。</span><span class="sxs-lookup"><span data-stu-id="7875d-162">SAN size and throughput based on total concurrent transaction volume/usage.</span></span>

### <a name="high-availability"></a><span data-ttu-id="7875d-163">高可用性</span><span class="sxs-lookup"><span data-stu-id="7875d-163">High availability</span></span>

<span data-ttu-id="7875d-164">クラスタまたはミラーリングの設定で常に SQL Server を使用することをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="7875d-164">We recommend always utilizing SQL Server in either a cluster or mirroring setup.</span></span> <span data-ttu-id="7875d-165">2 番目の SQL ノードは、1 次ノードと同じ数のコアを持つ必要があります。</span><span class="sxs-lookup"><span data-stu-id="7875d-165">The second SQL node should have the same number of cores as the primary node.</span></span>

### <a name="active-directory-federation-services-ad-fs"></a><span data-ttu-id="7875d-166">Active Directory フェデレーション サービス (AD FS)</span><span class="sxs-lookup"><span data-stu-id="7875d-166">Active Directory Federation Services (AD FS)</span></span>

<span data-ttu-id="7875d-167">AD FS のサイズについては、[AD FS の処理能力ドキュメント](/windows-server/identity/ad-fs/design/planning-for-ad-fs-server-capacity) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="7875d-167">For AD FS sizing, see the [AD FS Server Capacity documentation](/windows-server/identity/ad-fs/design/planning-for-ad-fs-server-capacity).</span></span>

<span data-ttu-id="7875d-168">A[サイズ変更スプレッドシート](http://adfsdocs.blob.core.windows.net/adfs/ADFSCapacity2016.xlsx)は、展開内のインスタンスの数を計画するために使用できます。</span><span class="sxs-lookup"><span data-stu-id="7875d-168">A [sizing spreadsheet](http://adfsdocs.blob.core.windows.net/adfs/ADFSCapacity2016.xlsx) is available for planning the number of instances in your deployment.</span></span>

## <a name="aos-online-and-batch"></a><span data-ttu-id="7875d-169">AOS (オンラインおよびバッチ)</span><span class="sxs-lookup"><span data-stu-id="7875d-169">AOS (Online and batch)</span></span>

### <a name="sizing"></a><span data-ttu-id="7875d-170">サイズ変更</span><span class="sxs-lookup"><span data-stu-id="7875d-170">Sizing</span></span>

- <span data-ttu-id="7875d-171">トランザクションの量と使用法サイズの変更</span><span class="sxs-lookup"><span data-stu-id="7875d-171">Sizing by transaction volume/usage</span></span>

    - <span data-ttu-id="7875d-172">コアあたり 2K から 6K の明細行</span><span class="sxs-lookup"><span data-stu-id="7875d-172">2K to 6K lines per core</span></span>
    - <span data-ttu-id="7875d-173">インスタンスあたり 16 GB</span><span class="sxs-lookup"><span data-stu-id="7875d-173">16 GB per instance</span></span>
    - <span data-ttu-id="7875d-174">標準ボックス – 4 から 24 コア</span><span class="sxs-lookup"><span data-stu-id="7875d-174">Standard box – 4 to 24 cores</span></span>
    - <span data-ttu-id="7875d-175">コアあたり 10 から 15 のエンタープライズ ユーザー</span><span class="sxs-lookup"><span data-stu-id="7875d-175">10 to 15 Enterprise users per core</span></span>
    - <span data-ttu-id="7875d-176">コアあたり 15 から 25 のアクティブ ユーザー</span><span class="sxs-lookup"><span data-stu-id="7875d-176">15 to 25 Activity users per core</span></span>
    - <span data-ttu-id="7875d-177">コアあたり 25 から 50 のチーム メンバー</span><span class="sxs-lookup"><span data-stu-id="7875d-177">25 to 50 Team members per core</span></span>

- <span data-ttu-id="7875d-178">バッチ</span><span class="sxs-lookup"><span data-stu-id="7875d-178">Batch</span></span>

    - <span data-ttu-id="7875d-179">コアあたり 1 から 4 のバッチ スレッド</span><span class="sxs-lookup"><span data-stu-id="7875d-179">1 to 4 batch threads per core</span></span>
    - <span data-ttu-id="7875d-180">バッチ ウィンドウの特性に基づくサイズ</span><span class="sxs-lookup"><span data-stu-id="7875d-180">Size based on batch window characterization</span></span>

- <span data-ttu-id="7875d-181">AOS、データ管理、およびバッチは、サービス ファブリック内で同じ役割を果たすことに注意してください。</span><span class="sxs-lookup"><span data-stu-id="7875d-181">Note that the AOS, Data Management, and Batch are on the same role in the Service Fabric.</span></span> <span data-ttu-id="7875d-182">Microsoft Dynamics AX 2012 のように、これらの 3 つのワークロードをまとめてサイズ調整する必要があります。</span><span class="sxs-lookup"><span data-stu-id="7875d-182">You need to size for these three workloads combined, and not separate these like in Microsoft Dynamics AX 2012.</span></span>
- <span data-ttu-id="7875d-183">ここでは、SQL Server と同じ変動要因が適用されます。</span><span class="sxs-lookup"><span data-stu-id="7875d-183">The same variability factors for SQL Server apply here.</span></span>

### <a name="high-availability"></a><span data-ttu-id="7875d-184">高可用性</span><span class="sxs-lookup"><span data-stu-id="7875d-184">High availability</span></span>

- <span data-ttu-id="7875d-185">推測する以上に少なくとも 1 から 2 の AOS があることを確認してください。</span><span class="sxs-lookup"><span data-stu-id="7875d-185">Ensure that you have at least 1 to 2 more AOS available than you estimate.</span></span>
- <span data-ttu-id="7875d-186">少なくとも 3 から 4 つの仮想ホストが使用可能であることを確認してください。</span><span class="sxs-lookup"><span data-stu-id="7875d-186">Ensure that you have at least 3 to 4 virtual hosts available.</span></span>

## <a name="management-reporter"></a><span data-ttu-id="7875d-187">Management Reporter</span><span class="sxs-lookup"><span data-stu-id="7875d-187">Management reporter</span></span>

<span data-ttu-id="7875d-188">ほとんどの場合、広範囲に使用されない限り、2 つのノードを使用する推奨最小要件が適切に動作します。</span><span class="sxs-lookup"><span data-stu-id="7875d-188">In most cases, unless used extensively, the recommended minimum requirements using two nodes should work well.</span></span> <span data-ttu-id="7875d-189">頻繁に使用する場合にのみ、2 つ以上のノードが必要になります。</span><span class="sxs-lookup"><span data-stu-id="7875d-189">Only in cases where there is heavy use will you need more than two nodes.</span></span> <span data-ttu-id="7875d-190">必要に応じて縮尺を調整してください。</span><span class="sxs-lookup"><span data-stu-id="7875d-190">Please scale as needed.</span></span>

## <a name="sql-server-reporting-services"></a><span data-ttu-id="7875d-191">SQL Server Reporting Services</span><span class="sxs-lookup"><span data-stu-id="7875d-191">SQL Server Reporting Services</span></span>

<span data-ttu-id="7875d-192">一般的な使用可能なリリースは、1 つの SSRS ノードしか展開できません。</span><span class="sxs-lookup"><span data-stu-id="7875d-192">For the general availability release, only one SSRS node can be deployed.</span></span> <span data-ttu-id="7875d-193">テスト中に SSRS ノードを監視し、SSRS で使用可能なコアの数を必要に応じて増やします。</span><span class="sxs-lookup"><span data-stu-id="7875d-193">Monitor your SSRS node while testing and increase the number of cores available for SSRS on a need basis.</span></span> <span data-ttu-id="7875d-194">SSRS VM とは異なる仮想ホストで事前構成されたセカンダリ ノードを使用できることを確認してください。</span><span class="sxs-lookup"><span data-stu-id="7875d-194">Make sure that you have a preconfigured secondary node available on a virtual host that is different than the SSRS VM.</span></span> <span data-ttu-id="7875d-195">これは、SSRS または仮想ホストをホストする仮想マシンに問題がある場合に重要です。</span><span class="sxs-lookup"><span data-stu-id="7875d-195">This is important if there is an issue with the virtual machine that hosts SSRS or the virtual host.</span></span> <span data-ttu-id="7875d-196">この場合、交換する必要があります。</span><span class="sxs-lookup"><span data-stu-id="7875d-196">If this the case, they would need to be replaced.</span></span>

## <a name="environment-orchestrator"></a><span data-ttu-id="7875d-197">環境オーケストレーター</span><span class="sxs-lookup"><span data-stu-id="7875d-197">Environment Orchestrator</span></span>

<span data-ttu-id="7875d-198">オーケストレータ サービスは、展開および LCS との関連する通信を管理するサービスです。</span><span class="sxs-lookup"><span data-stu-id="7875d-198">The Orchestrator service is the service that manages your deployment and the related communication with LCS.</span></span> <span data-ttu-id="7875d-199">このサービスはプライマリ Service Fabric サービスとして展開され、最低 3 台の VM が必要です。</span><span class="sxs-lookup"><span data-stu-id="7875d-199">This service is deployed as the primary Service Fabric service and requires at least three VMs.</span></span> <span data-ttu-id="7875d-200">このサービスは、サービス ファブリック オーケストレーション サービスと同じ場所に配置されています。</span><span class="sxs-lookup"><span data-stu-id="7875d-200">This service is co-located with the Service Fabric orchestration services.</span></span> <span data-ttu-id="7875d-201">これはクラスタのピーク負荷に合わせて調整する必要があります。</span><span class="sxs-lookup"><span data-stu-id="7875d-201">This and should be sized to the peak load of the cluster.</span></span> <span data-ttu-id="7875d-202">詳細については、[Service Fabric クラスターの能力計画に関する考慮事項](/azure/service-fabric/service-fabric-cluster-capacity)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="7875d-202">For more information, see [Service Fabric cluster capacity planning considerations](/azure/service-fabric/service-fabric-cluster-capacity).</span></span>

## <a name="virtualization-and-oversubscription"></a><span data-ttu-id="7875d-203">仮想化と過剰加入</span><span class="sxs-lookup"><span data-stu-id="7875d-203">Virtualization and oversubscription</span></span>

<span data-ttu-id="7875d-204">AOS のようなミッション クリティカルなサービスは、コア、メモリ、ディスクなどの専用リソースを持つ仮想ホストでホストする必要があります。</span><span class="sxs-lookup"><span data-stu-id="7875d-204">Mission critical services like the AOS should be hosted on Virtual hosts that have dedicated resources – cores, memory, and disk.</span></span>
