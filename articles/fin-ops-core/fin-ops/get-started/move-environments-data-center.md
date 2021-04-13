---
title: データ センター間で環境を移動する
description: このトピックでは、Microsoft によって管理されている環境を別の Microsoft Azure データ センターに移動する方法について説明します。
author: ClaudiaBetz-Haubold
ms.date: 06/04/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: IT Pro
ms.reviewer: sericks
ms.search.region: Global
ms.author: chaubold
ms.search.validFrom: 2018-05-30
ms.dyn365.ops.version: AX 7.0
ms.openlocfilehash: f048a1437c5416de5cdd03c416ba5962259822a7
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/31/2021
ms.locfileid: "5749183"
---
# <a name="move-environments-between-data-centers"></a><span data-ttu-id="dc0dc-103">データ センター間で環境を移動する</span><span class="sxs-lookup"><span data-stu-id="dc0dc-103">Move environments between data centers</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="dc0dc-104">場合によっては、Microsoftによって管理されている環境を別の Microsoft Azure データ センターに移動する必要が生じることがあります。</span><span class="sxs-lookup"><span data-stu-id="dc0dc-104">Occasionally, you must move environments that are managed by Microsoft to a different Microsoft Azure data center.</span></span> <span data-ttu-id="dc0dc-105">この移動が必要になる場合のいくつかのシナリオを次に示します。</span><span class="sxs-lookup"><span data-stu-id="dc0dc-105">Here are some scenarios where this move might be required:</span></span>

- <span data-ttu-id="dc0dc-106">使用するデータ センターは、環境が当初配置されていたときには使用できませんでした。</span><span class="sxs-lookup"><span data-stu-id="dc0dc-106">The data center that you planned to use wasn't available when the environments were originally deployed.</span></span>
- <span data-ttu-id="dc0dc-107">プロジェクト作成者は、環境が本来配置された以前に、最適なデータ センターを決定するための十分な調査を行っていません。</span><span class="sxs-lookup"><span data-stu-id="dc0dc-107">The project creators didn't do enough research to determine the best data center before the environments were originally deployed.</span></span>
- <span data-ttu-id="dc0dc-108">顧客はその操作の物理的な場所を移動し、ワイド エリア ネットワーク (WAN) 接続がより短い待機時間を提供するデータ センターにより近くなります。</span><span class="sxs-lookup"><span data-stu-id="dc0dc-108">The customer moves the physical location of its operations, and the wide area network (WAN) connection is now closer to a data center that provides lower latency.</span></span>

<span data-ttu-id="dc0dc-109">Microsoft により同じデータ センターですべての環境を維持するよう求められます。</span><span class="sxs-lookup"><span data-stu-id="dc0dc-109">Microsoft asks that you keep all your environments in the same data center.</span></span> <span data-ttu-id="dc0dc-110">環境を別のデータ センターに移行する場合、最終的にはすべての環境を同じデータ センターに展開することを計画する必要があります。</span><span class="sxs-lookup"><span data-stu-id="dc0dc-110">When you move environments to a different data center, you should plan to eventually have all environments deployed in the same data center.</span></span>

<span data-ttu-id="dc0dc-111">環境が展開されているデータ センターを Microsoft Dynamics Lifecycle Services (LCS) の **環境の管理** ページ上で確認できます。</span><span class="sxs-lookup"><span data-stu-id="dc0dc-111">You can verify the data center that an environment is deployed to on the **Manage environments** page in Microsoft Dynamics Lifecycle Services (LCS).</span></span>

<span data-ttu-id="dc0dc-112">データ センターを変更するには、すべての環境を再配置する必要があります。</span><span class="sxs-lookup"><span data-stu-id="dc0dc-112">To change the data center, you must redeploy all environments.</span></span> <span data-ttu-id="dc0dc-113">サンド ボックス環境 (サンド ボックスのスタンダード承認テスト環境、およびサンド ボックスの開発およびテスト環境) のプロセスは実稼動環境のプロセスとは異なります。</span><span class="sxs-lookup"><span data-stu-id="dc0dc-113">The process differs for sandbox environments (sandbox standard acceptance test environments, and sandbox develop and test environments) and production environments.</span></span>

## <a name="move-sandbox-environments"></a><span data-ttu-id="dc0dc-114">サンドボックス環境の移動</span><span class="sxs-lookup"><span data-stu-id="dc0dc-114">Move sandbox environments</span></span>

<span data-ttu-id="dc0dc-115">この移動はセルフサービスのアクションなので、パートナーや顧客は Microsoft の関与なしで既存のサンドボックス環境を移動する必要があります。</span><span class="sxs-lookup"><span data-stu-id="dc0dc-115">Because this move is a self-service action, the partner and/or customer must move the existing sandbox environments without Microsoft involvement.</span></span> <span data-ttu-id="dc0dc-116">このアクションには、パートナーまたは顧客のリソースの側でわずかな作業量が必要ですが、エンド ツー エンド プロセスの完了には数日かかることがあります。</span><span class="sxs-lookup"><span data-stu-id="dc0dc-116">Although this action requires little effort on the part of the partner or customer resources, completion of the end-to-end process might require a few days.</span></span> <span data-ttu-id="dc0dc-117">環境間でデータの移動を効率化するには、移動を開始する前に、最適な順序を決定するために計画を作成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="dc0dc-117">To streamline the data movement between environments, you should develop a plan to determine the best sequence before you begin the move.</span></span>

### <a name="save-data"></a><span data-ttu-id="dc0dc-118">データの保存</span><span class="sxs-lookup"><span data-stu-id="dc0dc-118">Save data</span></span>

<span data-ttu-id="dc0dc-119">移動を開始する前に、データを保存する必要があります。</span><span class="sxs-lookup"><span data-stu-id="dc0dc-119">Before you begin the move, you must save your data.</span></span>

- <span data-ttu-id="dc0dc-120">**Microsoft SQL Server に基づくレベル 1 環境データベース:** データベースのバックアップを作成します。</span><span class="sxs-lookup"><span data-stu-id="dc0dc-120">**Tier 1 environment database that is based on Microsoft SQL Server:** Make a backup of the database.</span></span>
- <span data-ttu-id="dc0dc-121">**Azure SQL データベースに基づくレベル 2 およびそれ以上の環境:** 次のオプションのいずれかを選択します。</span><span class="sxs-lookup"><span data-stu-id="dc0dc-121">**Tier 2 and higher environments that are based on Azure SQL Database:** Choose one of the following options:</span></span>

    - <span data-ttu-id="dc0dc-122">**オプション 1:** [データベース 移動工程のホームページ](../../dev-itpro/database/dbmovement-operations.md) のトピックに一覧表示されているプロセスを確認します。</span><span class="sxs-lookup"><span data-stu-id="dc0dc-122">**Option 1:** Review the processes that are listed in the [Database movement operations home page](../../dev-itpro/database/dbmovement-operations.md) topic.</span></span>
    - <span data-ttu-id="dc0dc-123">**オプション 2:** Azure サブスクリプションを持っている場合、サブスクリプションの下に Azure SQL データベースのコピーを保存してください。</span><span class="sxs-lookup"><span data-stu-id="dc0dc-123">**Option 2:** If you have an Azure subscription, save a copy of the Azure SQL database under that subscription.</span></span>
    - <span data-ttu-id="dc0dc-124">**オプション 3:** Azure SQL データベース環境を複数持ってる場合、1 つの環境を再配置し、古い環境をデータ センターに残してから、環境間でデータベース更新の要求をします。</span><span class="sxs-lookup"><span data-stu-id="dc0dc-124">**Option 3:** If you have multiple Azure SQL database environments, redeploy one environment, leave the remaining environments in the old data center, and then request a database refresh between the environments.</span></span>
    - <span data-ttu-id="dc0dc-125">**オプション 4:** データ パッケージとしてデータを保存し、再配置が完了した後にパッケージをインポートします。</span><span class="sxs-lookup"><span data-stu-id="dc0dc-125">**Option 4:** Save data as data packages, and then import the packages after the redeployment is completed.</span></span>

### <a name="move-the-environments"></a><span data-ttu-id="dc0dc-126">環境の移動</span><span class="sxs-lookup"><span data-stu-id="dc0dc-126">Move the environments</span></span>

<span data-ttu-id="dc0dc-127">データ保存後、これらの手順に従ってください。</span><span class="sxs-lookup"><span data-stu-id="dc0dc-127">After you've saved your data, follow these steps.</span></span>

1. <span data-ttu-id="dc0dc-128">コードのすべてのパッケージが LCS でアセット ライブラリにアップロードされていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="dc0dc-128">Verify that all code packages have been uploaded to the Asset library in LCS.</span></span>
2. <span data-ttu-id="dc0dc-129">各環境について、次の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="dc0dc-129">For each environment, follow these steps:</span></span>

    1. <span data-ttu-id="dc0dc-130">LCS で **完全な詳細** を選択します。</span><span class="sxs-lookup"><span data-stu-id="dc0dc-130">In LCS, select **Full details**.</span></span>
    2. <span data-ttu-id="dc0dc-131">環境を停止してから、環境が停止した時に、**割り当て解除** を選択します。</span><span class="sxs-lookup"><span data-stu-id="dc0dc-131">Stop the environment, and then, when the environment has stopped, select **Deallocate**.</span></span>
    3. <span data-ttu-id="dc0dc-132">割り当て解除が完了した後、**削除** を選択します。</span><span class="sxs-lookup"><span data-stu-id="dc0dc-132">After the deallocation is completed, select **Delete**.</span></span>
    4. <span data-ttu-id="dc0dc-133">この環境が削除された後、**構成** を選択し、環境を再配置します。</span><span class="sxs-lookup"><span data-stu-id="dc0dc-133">After the environment is deleted, select **Configure** to redeploy the environment.</span></span>
    5. <span data-ttu-id="dc0dc-134">**地理/場所** フィールドで、使用するデータ センターを選択します。</span><span class="sxs-lookup"><span data-stu-id="dc0dc-134">In the **Geography/location** field, select the data center to use.</span></span>
    6. <span data-ttu-id="dc0dc-135">環境が再配置された後は、コード パッケージを適用します。</span><span class="sxs-lookup"><span data-stu-id="dc0dc-135">After the environment is deployed, apply the code packages.</span></span>
    7. <span data-ttu-id="dc0dc-136">再配置された環境がビルド環境として使用されている場合は、 [継続的なビルドとテストの自動化をサポートする環境を配置して使用](../../dev-itpro/perf-test/continuous-build-test-automation.md) に記載されている必要なコンフィギュレーションを完了します。</span><span class="sxs-lookup"><span data-stu-id="dc0dc-136">If the redeployed environment is used as the build environment, complete the required configurations that are described in [Deploy and use an environment that supports continuous build and test automation](../../dev-itpro/perf-test/continuous-build-test-automation.md).</span></span>
    8. <span data-ttu-id="dc0dc-137">データを復元します。</span><span class="sxs-lookup"><span data-stu-id="dc0dc-137">Restore the data.</span></span>

> [!NOTE]
> - <span data-ttu-id="dc0dc-138">サンド ボックス環境では、Azure BLOB ストレージに格納されているファイルの移動はサポートされていません。</span><span class="sxs-lookup"><span data-stu-id="dc0dc-138">The movement of files that are stored in Azure Blob Storage isn't supported in sandbox environments.</span></span>
> - <span data-ttu-id="dc0dc-139">コマース顧客は、移動後にコンポーネントが正常に機能するため追加の手順が必要であることに注意する必要があります。</span><span class="sxs-lookup"><span data-stu-id="dc0dc-139">Commerce customers should be aware that extra steps are required for components to work correctly after a move.</span></span> <span data-ttu-id="dc0dc-140">詳細については、 [データ管理の概要](../../dev-itpro/data-entities/data-entities-data-packages.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="dc0dc-140">For more information, see [Data management overview](../../dev-itpro/data-entities/data-entities-data-packages.md).</span></span>

## <a name="move-production-environments"></a><span data-ttu-id="dc0dc-141">実稼働環境の移動</span><span class="sxs-lookup"><span data-stu-id="dc0dc-141">Move production environments</span></span>

<span data-ttu-id="dc0dc-142">実稼働環境を既に配置している場合は、すべてのサンドボックス環境の移動が完了した後に、実稼働環境を別のデータセンターに移動するためのサポート要求を開く必要があります。</span><span class="sxs-lookup"><span data-stu-id="dc0dc-142">If you already have a production environment deployed, you must open a Support request to move the production environment to another data center after you've finished moving all the sandbox environments.</span></span> <span data-ttu-id="dc0dc-143">このシナリオはまれであり、移動を完了するための自動/セルフサービス アクションはありません。</span><span class="sxs-lookup"><span data-stu-id="dc0dc-143">This scenario is rare, and there is no automated/self-service action to complete the move.</span></span> <span data-ttu-id="dc0dc-144">このシナリオでは、Azure BLOB ストレージに格納されているファイルも移動されます。</span><span class="sxs-lookup"><span data-stu-id="dc0dc-144">In this scenario, files that are stored in Azure Blob Storage will also be moved.</span></span> <span data-ttu-id="dc0dc-145">実稼働環境を別のデータ センターに移動するために必要な保守ウィンドウとダウンタイムの詳細については、次を参照してください。[サービスの説明](https://go.microsoft.com/fwlink/?LinkId=867755&clcid=0x409)と関連するサービス レベル契約 (SLA) のドキュメント。</span><span class="sxs-lookup"><span data-stu-id="dc0dc-145">For information about the maintenance window and downtime that are required in order to move a production environment to a different data center, see [Service Description](https://go.microsoft.com/fwlink/?LinkId=867755&clcid=0x409) and the related service-level agreement (SLA) documents.</span></span>


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]