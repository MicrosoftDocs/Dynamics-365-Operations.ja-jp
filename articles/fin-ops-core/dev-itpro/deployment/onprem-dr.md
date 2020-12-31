---
title: オンプレミスにおけるディザスター リカバリーの構成
description: このコンテンツでは、ディザスター リカバリーに向けて Dynamics 365 Finance + 操作 (オンプレミス) を構成する方法と、プライマリ データセンターとセカンダリ データセンターの切り替えプロセスを構成する方法について説明します。
author: faix
manager: AnnBe
ms.date: 09/11/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: IT Pro
ms.reviewer: sericks
ms.search.region: Global
ms.author: osfaixat
ms.search.validFrom: 2020-06-30
ms.dyn365.ops.version: 10.0.12
ms.openlocfilehash: 419aab6e0776ad186ec6cdac320a79d0a68e980d
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 12/05/2020
ms.locfileid: "4685455"
---
# <a name="on-premises-disaster-recovery-configuration"></a><span data-ttu-id="13227-103">オンプレミスにおけるディザスター リカバリーの構成</span><span class="sxs-lookup"><span data-stu-id="13227-103">On-premises disaster recovery configuration</span></span>
<span data-ttu-id="13227-104">ディザスター リカバリーは、組織のオペレーションを危険にさらす可能性のあるイベントから保護するために、Dynamics 365 Finance + 操作 (オンプレミス) をオンプレミスで導入する際に重要となる考慮事項です。</span><span class="sxs-lookup"><span data-stu-id="13227-104">Disaster recovery is an important consideration for on-premises deployments of Dynamics 365 Finance + Operations (on-premises) to protect from events that could put your organization's operations at risk.</span></span> <span data-ttu-id="13227-105">このようなイベントの例としては、機材の故障、サイバー攻撃、電気的、物理的なデータの破損などによるデータセンターの停止が含まれます。</span><span class="sxs-lookup"><span data-stu-id="13227-105">Examples of such events include equipment failures, datacenter break downs due to cyberattacks, electrical, physical, or other disasters.</span></span>

<span data-ttu-id="13227-106">ディザスター リカバリーの中心となる概念は、データ復元環境を含む2番目のデータセンターを使用することです。</span><span class="sxs-lookup"><span data-stu-id="13227-106">The core concept of disaster recovery involves the use of a second datacenter including a data recover environment.</span></span> <span data-ttu-id="13227-107">ディザスター リカバリーの計画、文書化、テストは、運用環境の設定と同様に慎重に行うことを推奨します。</span><span class="sxs-lookup"><span data-stu-id="13227-107">We recommend that you plan, document, and test disaster recovery as carefully as your production setup.</span></span>

### <a name="limitations-of-this-content"></a><span data-ttu-id="13227-108">このコンテンツの制限事項</span><span class="sxs-lookup"><span data-stu-id="13227-108">Limitations of this content</span></span>

<span data-ttu-id="13227-109">このトピックでは、以下のコンポーネントのディザスター リカバリーに関する構成の詳細については説明しません。</span><span class="sxs-lookup"><span data-stu-id="13227-109">This topic does not cover specific configuration details for disaster recovery of the following components:</span></span>
  - <span data-ttu-id="13227-110">Active Directory フェデレーション サービス (AD FS)</span><span class="sxs-lookup"><span data-stu-id="13227-110">Active Directory Federation Services (AD FS)</span></span>
  - <span data-ttu-id="13227-111">ファイルのストレージ</span><span class="sxs-lookup"><span data-stu-id="13227-111">File storage</span></span>
  - <span data-ttu-id="13227-112">SQL Server</span><span class="sxs-lookup"><span data-stu-id="13227-112">SQL Server</span></span>

> [!NOTE]
> <span data-ttu-id="13227-113">高可用性の構成については、このトピックでは説明していません。</span><span class="sxs-lookup"><span data-stu-id="13227-113">High availability configuration isn't covered in this topic.</span></span> <span data-ttu-id="13227-114">高可用性に必要な最小限の設定の詳細については、[オンプレミス配置に関するシステム要件](../../fin-ops/get-started/system-requirements-on-prem.md#minimum-infrastructure-requirements)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="13227-114">For more information about the minimum setup required for high availability, see [System requirements for on-premises deployments](../../fin-ops/get-started/system-requirements-on-prem.md#minimum-infrastructure-requirements).</span></span>

### <a name="recommendations"></a><span data-ttu-id="13227-115">推奨事項</span><span class="sxs-lookup"><span data-stu-id="13227-115">Recommendations</span></span>

<span data-ttu-id="13227-116">ディザスター リカバリー環境は、常に最新の Windows 更新プログラムで更新しておいてください。</span><span class="sxs-lookup"><span data-stu-id="13227-116">Remember to keep your disaster recovery environment updated with the latest Windows Updates.</span></span> <span data-ttu-id="13227-117">ご利用の環境には最新のセキュリティ更新プログラムが適用されている必要がありますが、障害の発生時には更新が必要となりません。</span><span class="sxs-lookup"><span data-stu-id="13227-117">Your environment should have the latest security updates and not require updates during a disaster event.</span></span>

<span data-ttu-id="13227-118">Microsoft が指定した新しい前提条件を適用していることを確認します。</span><span class="sxs-lookup"><span data-stu-id="13227-118">Ensure that you're applying new prerequisites that are specified by Microsoft.</span></span> <span data-ttu-id="13227-119">また、Service Fabric Cluster を更新して、必要に応じて証明書のローテーションを実行します。</span><span class="sxs-lookup"><span data-stu-id="13227-119">Also, keep your Service Fabric cluster updated and perform certificate rotations as required.</span></span>

<span data-ttu-id="13227-120">このトピックを読んだ後で、チームが実施する必要のある手順を文書化してください。</span><span class="sxs-lookup"><span data-stu-id="13227-120">After you've read through this topic, document the steps that need to be taken by your team.</span></span> <span data-ttu-id="13227-121">その後は、予想外の問題が発生しないよう、手順を複数回実施して、発生する可能性のあるダウンタイムを最小限に抑えてください。</span><span class="sxs-lookup"><span data-stu-id="13227-121">After you’ve done that, go through the steps multiple times to ensure that you don't encounter unexpected problems and you minimize the potential downtime.</span></span>

## <a name="overview"></a><span data-ttu-id="13227-122">概要</span><span class="sxs-lookup"><span data-stu-id="13227-122">Overview</span></span>

<span data-ttu-id="13227-123">ディザスター リカバリーの基本構成では、別のデータセンター (セカンダリ データセンター) 内に実稼働環境の複製を配置し、そのデータセンターにデータベースを複製します。</span><span class="sxs-lookup"><span data-stu-id="13227-123">The basic configuration for disaster recovery involves deploying a duplicate of the production environment within another datacenter (the secondary datacenter) and replicating databases to that datacenter.</span></span> <span data-ttu-id="13227-124">災害イベントが発生した場合、いくつかの手動の手順を実施することで、セカンダリ データセンター内の環境をオンライン状態にすることができます。</span><span class="sxs-lookup"><span data-stu-id="13227-124">If a disaster event takes place, a few manual steps can be taken to bring the environment that is within the secondary datacenter online.</span></span>

<span data-ttu-id="13227-125">以下の図では、必要となる設定の詳細を示しています。</span><span class="sxs-lookup"><span data-stu-id="13227-125">The following diagram illustrates the required setup, at a high level.</span></span>

![ディザスター リカバリー アーキテクチャ](media/DRArchitecture.png)

## <a name="environment-configuration"></a><span data-ttu-id="13227-127">環境のコンフィギュレーション</span><span class="sxs-lookup"><span data-stu-id="13227-127">Environment configuration</span></span>

<span data-ttu-id="13227-128">Lifecycle Services (LCS) では、運用環境は、**運用** と名付けた環境のスロットを使用して配置する必要があります。</span><span class="sxs-lookup"><span data-stu-id="13227-128">In Lifecycle Services (LCS), the production environment should be deployed using the environment slot named **Production**.</span></span> <span data-ttu-id="13227-129">ディザスター リカバリー環境では、LCS の追加の環境スロットが使用されません。</span><span class="sxs-lookup"><span data-stu-id="13227-129">Your disaster recovery environment will not use an additional environment slot in LCS.</span></span> <span data-ttu-id="13227-130">その代わりに、運用環境でスロットを再利用します。</span><span class="sxs-lookup"><span data-stu-id="13227-130">It will instead reuse the slot for your production environment.</span></span> 

<span data-ttu-id="13227-131">Finance and Operations AOS ノードと SQL Server は、同じデータセンター内に共存している必要があります。</span><span class="sxs-lookup"><span data-stu-id="13227-131">Finance and Operations AOS nodes and SQL Server must be co-located within the same datacenter.</span></span> <span data-ttu-id="13227-132">詳細については、[オンプレミス展開のシステム要件](../../fin-ops/get-started/system-requirements-on-prem.md#network-requirements)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="13227-132">For more information, see [System requirements for on-premises deployments](../../fin-ops/get-started/system-requirements-on-prem.md#network-requirements).</span></span>

## <a name="deploying-code-packages-to-production"></a><span data-ttu-id="13227-133">運用環境にコード パッケージを配置する</span><span class="sxs-lookup"><span data-stu-id="13227-133">Deploying code packages to production</span></span>

<span data-ttu-id="13227-134">コード パッケージを運用環境に配置する場合はディザスター リカバリー環境に配置する必要はありません。</span><span class="sxs-lookup"><span data-stu-id="13227-134">When code packages are deployed to the production environment, they don't need to be deployed to the disaster recovery environment.</span></span> <span data-ttu-id="13227-135">この環境を使用せずに、Service Fabric サービスを配置しないようにする必要があります。</span><span class="sxs-lookup"><span data-stu-id="13227-135">That environment should be unused and no Service Fabric services should be deployed.</span></span>

## <a name="environment-deployment-settings"></a><span data-ttu-id="13227-136">環境を配置する設定</span><span class="sxs-lookup"><span data-stu-id="13227-136">Environment deployment settings</span></span>

<span data-ttu-id="13227-137">ディザスター リカバリー環境は、運用環境と同様の構成にする必要があります。</span><span class="sxs-lookup"><span data-stu-id="13227-137">The disaster recovery environment should have a similar configuration as the production environment.</span></span> <span data-ttu-id="13227-138">以下の表に、ディザスター リカバリーに向けて共有される設定と固有となる設定を示します。</span><span class="sxs-lookup"><span data-stu-id="13227-138">The following table illustrates the shared and specific settings for disaster recovery.</span></span>

| <span data-ttu-id="13227-139">環境設定</span><span class="sxs-lookup"><span data-stu-id="13227-139">Environment settings</span></span> | <span data-ttu-id="13227-140">ディザスター リカバリー環境</span><span class="sxs-lookup"><span data-stu-id="13227-140">Disaster recovery environment</span></span>|
|---------------------------------|----------------|
| <span data-ttu-id="13227-141">**Active Directory の設定**</span><span class="sxs-lookup"><span data-stu-id="13227-141">**Active Directory settings**</span></span>   |                |
| <span data-ttu-id="13227-142">管理者ユーザー</span><span class="sxs-lookup"><span data-stu-id="13227-142">Administrator user</span></span>              | <span data-ttu-id="13227-143">運用環境と同等</span><span class="sxs-lookup"><span data-stu-id="13227-143">Same as production</span></span>|
| <span data-ttu-id="13227-144">AD FS URL</span><span class="sxs-lookup"><span data-stu-id="13227-144">AD FS URL</span></span>                        | <span data-ttu-id="13227-145">運用環境と同等</span><span class="sxs-lookup"><span data-stu-id="13227-145">Same as production</span></span>|
| <span data-ttu-id="13227-146">AOS の AD FS OpenId Connect クライアントID</span><span class="sxs-lookup"><span data-stu-id="13227-146">AD FS OpenId Connect client ID for AOS</span></span> | <span data-ttu-id="13227-147">運用環境と同等</span><span class="sxs-lookup"><span data-stu-id="13227-147">Same as production</span></span>|
| <span data-ttu-id="13227-148">Financial Reporting の AD FS OpenId Connect クライアントID</span><span class="sxs-lookup"><span data-stu-id="13227-148">AD FS OpenId Connect client ID for Financial Reporting</span></span> | <span data-ttu-id="13227-149">運用環境と同等</span><span class="sxs-lookup"><span data-stu-id="13227-149">Same as production</span></span>|
| <span data-ttu-id="13227-150">**SQL データベースの構成**</span><span class="sxs-lookup"><span data-stu-id="13227-150">**SQL Database configuration**</span></span>  |                 |
| <span data-ttu-id="13227-151">SQL Server の名称</span><span class="sxs-lookup"><span data-stu-id="13227-151">SQL Server name</span></span>                 | <span data-ttu-id="13227-152">運用環境と同等</span><span class="sxs-lookup"><span data-stu-id="13227-152">Same as production</span></span> |
| <span data-ttu-id="13227-153">AX データベース名</span><span class="sxs-lookup"><span data-stu-id="13227-153">AX database name</span></span>                | <span data-ttu-id="13227-154">運用環境と同等</span><span class="sxs-lookup"><span data-stu-id="13227-154">Same as production</span></span> |
| <span data-ttu-id="13227-155">Financial Reporting データベースの名前</span><span class="sxs-lookup"><span data-stu-id="13227-155">Financial Reporting database name</span></span>| <span data-ttu-id="13227-156">運用環境と同等</span><span class="sxs-lookup"><span data-stu-id="13227-156">Same as production</span></span> |
| <span data-ttu-id="13227-157">**ファイル共有設定**</span><span class="sxs-lookup"><span data-stu-id="13227-157">**File share settings**</span></span>         |                 |
| <span data-ttu-id="13227-158">ドキュメント ストアのファイル共有</span><span class="sxs-lookup"><span data-stu-id="13227-158">File share for document store</span></span>   | <span data-ttu-id="13227-159">運用環境と同等</span><span class="sxs-lookup"><span data-stu-id="13227-159">Same as production</span></span> |
| <span data-ttu-id="13227-160">ファイル共有証明書の拇印</span><span class="sxs-lookup"><span data-stu-id="13227-160">File share certificate thumbprint</span></span> | <span data-ttu-id="13227-161">運用環境と同等</span><span class="sxs-lookup"><span data-stu-id="13227-161">Same as production</span></span> |
| <span data-ttu-id="13227-162">**SSRS コンフィギュレーション設定**</span><span class="sxs-lookup"><span data-stu-id="13227-162">**SSRS configuration settings**</span></span> |                 |
| <span data-ttu-id="13227-163">SSRS インスタンスの IP アドレス</span><span class="sxs-lookup"><span data-stu-id="13227-163">IP address of SSRS instance</span></span>     | <span data-ttu-id="13227-164">異なる場合があります <sup>1</sup></span><span class="sxs-lookup"><span data-stu-id="13227-164">Can be different <sup>1</sup></span></span> |
| <span data-ttu-id="13227-165">SSRS 証明書の拇印</span><span class="sxs-lookup"><span data-stu-id="13227-165">SSRS certificate thumbprint</span></span>     | <span data-ttu-id="13227-166">運用環境と同等</span><span class="sxs-lookup"><span data-stu-id="13227-166">Same as production</span></span> |
| <span data-ttu-id="13227-167">**サービスの設定のコンフィギュレーション**</span><span class="sxs-lookup"><span data-stu-id="13227-167">**Configure service settings**</span></span>  |                 |
| <span data-ttu-id="13227-168">Dynamics 365 インスタンスの DNS ホスト名</span><span class="sxs-lookup"><span data-stu-id="13227-168">DNS host name of Dynamics 365 instance</span></span> | <span data-ttu-id="13227-169">異なる場合があります <sup>2</sup></span><span class="sxs-lookup"><span data-stu-id="13227-169">Can be different <sup>2</sup></span></span>|
| <span data-ttu-id="13227-170">AOS サービス ユーザー</span><span class="sxs-lookup"><span data-stu-id="13227-170">AOS service user</span></span>                | <span data-ttu-id="13227-171">運用環境と同等</span><span class="sxs-lookup"><span data-stu-id="13227-171">Same as production</span></span> |
| <span data-ttu-id="13227-172">MR アプリケーション サービスのユーザー</span><span class="sxs-lookup"><span data-stu-id="13227-172">MR application service user</span></span>     | <span data-ttu-id="13227-173">運用環境と同等</span><span class="sxs-lookup"><span data-stu-id="13227-173">Same as production</span></span> |
| <span data-ttu-id="13227-174">MR プロセス サービスのユーザー</span><span class="sxs-lookup"><span data-stu-id="13227-174">MR process service user</span></span>         | <span data-ttu-id="13227-175">運用環境と同等</span><span class="sxs-lookup"><span data-stu-id="13227-175">Same as production</span></span> |
| <span data-ttu-id="13227-176">MR click-once サービスのユーザー</span><span class="sxs-lookup"><span data-stu-id="13227-176">MR click-once service user</span></span>      | <span data-ttu-id="13227-177">運用環境と同等</span><span class="sxs-lookup"><span data-stu-id="13227-177">Same as production</span></span> |
| <span data-ttu-id="13227-178">**アプリケーション証明書の設定**</span><span class="sxs-lookup"><span data-stu-id="13227-178">**Application certificate settings**</span></span> |                 |
| <span data-ttu-id="13227-179">データの暗号化証明書の拇印</span><span class="sxs-lookup"><span data-stu-id="13227-179">Data encryption certificate thumbprint</span></span>| <span data-ttu-id="13227-180">運用環境と同等</span><span class="sxs-lookup"><span data-stu-id="13227-180">Same as production</span></span> |
| <span data-ttu-id="13227-181">データ署名証明書の拇印</span><span class="sxs-lookup"><span data-stu-id="13227-181">Data signing certificate thumbprint</span></span> | <span data-ttu-id="13227-182">運用環境と同等</span><span class="sxs-lookup"><span data-stu-id="13227-182">Same as production</span></span>   |
| <span data-ttu-id="13227-183">セッション認証証明書のの拇印</span><span class="sxs-lookup"><span data-stu-id="13227-183">Session authentication certificate thumbprint</span></span> | <span data-ttu-id="13227-184">運用環境と同等</span><span class="sxs-lookup"><span data-stu-id="13227-184">Same as production</span></span> |
| <span data-ttu-id="13227-185">SSL 証明書の拇印</span><span class="sxs-lookup"><span data-stu-id="13227-185">SSL certificate thumbprint</span></span>       | <span data-ttu-id="13227-186">運用環境と同等</span><span class="sxs-lookup"><span data-stu-id="13227-186">Same as production</span></span> |
| <span data-ttu-id="13227-187">Management reporter 証明書の拇印</span><span class="sxs-lookup"><span data-stu-id="13227-187">Management reporter certificate thumbprint</span></span> | <span data-ttu-id="13227-188">運用環境と同等</span><span class="sxs-lookup"><span data-stu-id="13227-188">Same as production</span></span> |

<span data-ttu-id="13227-189"><sup>1</sup> SSRS は IP が参照します。</span><span class="sxs-lookup"><span data-stu-id="13227-189"><sup>1</sup> SSRS is referenced by IP.</span></span> <span data-ttu-id="13227-190">ディザスター リカバリー環境で正確なマシンの IP を構成できない場合は、IP を別のものにすることができます。</span><span class="sxs-lookup"><span data-stu-id="13227-190">If the exact machine IP can't be configured in the disaster recovery environment, the IP can be different.</span></span>

<span data-ttu-id="13227-191"><sup>2</sup> これはネットワークの構成によって異なります。</span><span class="sxs-lookup"><span data-stu-id="13227-191"><sup>2</sup> This depends on your network configuration.</span></span> <span data-ttu-id="13227-192">他の環境へのトラフィックの流用に対応できる負荷分散装置を使用している場合は、ホスト名を同じにすることができます。</span><span class="sxs-lookup"><span data-stu-id="13227-192">If you have a load balancer that can handle diverting traffic to the other environment, then the host name can be the same.</span></span> <span data-ttu-id="13227-193">この対応ができない場合は、別のホスト名を使用します。</span><span class="sxs-lookup"><span data-stu-id="13227-193">If you're unable to do that, then use a different host name.</span></span> 

## <a name="sql-server-always-on-availability-configuration"></a><span data-ttu-id="13227-194">SQL Server の常時可用性を構成する</span><span class="sxs-lookup"><span data-stu-id="13227-194">SQL Server Always-On Availability configuration</span></span>

<span data-ttu-id="13227-195">ビジネス データ データベース (AXDB) は、通常は SQL Server の常時可用性グループ機能を使用して、セカンダリ データセンターに複製する必要があります。</span><span class="sxs-lookup"><span data-stu-id="13227-195">The business data database (AXDB) should be replicated to the secondary datacenter, typically using SQL Server Always-On availability groups feature.</span></span> <span data-ttu-id="13227-196">詳細については、[常時可用性グループ](https://docs.microsoft.com/sql/database-engine/availability-groups/windows/always-on-availability-groups-sql-server?view=sql-server-2016)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="13227-196">For more information, see [Always On availability groups](https://docs.microsoft.com/sql/database-engine/availability-groups/windows/always-on-availability-groups-sql-server?view=sql-server-2016).</span></span>

| <span data-ttu-id="13227-197">データベース</span><span class="sxs-lookup"><span data-stu-id="13227-197">Database</span></span> | <span data-ttu-id="13227-198">レプリケート済</span><span class="sxs-lookup"><span data-stu-id="13227-198">Replicated</span></span> |
|----------|------------|
| <span data-ttu-id="13227-199">業務データ (AXDB)</span><span class="sxs-lookup"><span data-stu-id="13227-199">Business data (AXDB)</span></span> | <span data-ttu-id="13227-200">有</span><span class="sxs-lookup"><span data-stu-id="13227-200">Yes</span></span> |
| <span data-ttu-id="13227-201">Financial Reporting</span><span class="sxs-lookup"><span data-stu-id="13227-201">Financial Reporting</span></span>  | <span data-ttu-id="13227-202">有</span><span class="sxs-lookup"><span data-stu-id="13227-202">Yes</span></span> |
| <span data-ttu-id="13227-203">BYODB</span><span class="sxs-lookup"><span data-stu-id="13227-203">BYODB</span></span>                | <span data-ttu-id="13227-204">有</span><span class="sxs-lookup"><span data-stu-id="13227-204">Yes</span></span> |
| <span data-ttu-id="13227-205">OrchestratorData</span><span class="sxs-lookup"><span data-stu-id="13227-205">OrchestratorData</span></span>     | <span data-ttu-id="13227-206">有</span><span class="sxs-lookup"><span data-stu-id="13227-206">Yes</span></span> |

## <a name="failing-over-to-disaster-recovery"></a><span data-ttu-id="13227-207">ディザスター リカバリーにフェイルオーバーする</span><span class="sxs-lookup"><span data-stu-id="13227-207">Failing over to disaster recovery</span></span>

### <a name="overview"></a><span data-ttu-id="13227-208">概要</span><span class="sxs-lookup"><span data-stu-id="13227-208">Overview</span></span>

<span data-ttu-id="13227-209">障害イベントが発生した場合、プライマリ データセンターが使用できなくなった場合であっても、セカンダリ データセンター内では、以下のコンポーネントが使用できます。</span><span class="sxs-lookup"><span data-stu-id="13227-209">When a disaster event occurs, the primary datacenter may be unavailable but within the secondary datacenter, the following components will be available.</span></span>

![配置設定の拇印の例](media/DRArchitectureSingle.png)

<span data-ttu-id="13227-211">障害が発生した最初の時点では、ディザスター リカバリー環境は空になります。</span><span class="sxs-lookup"><span data-stu-id="13227-211">At the initial moment of the disaster event, the disaster recovery environment will be empty.</span></span> <span data-ttu-id="13227-212">ここで存在するのは、複製された本番データのすべてを含む、構成済みの Service Fabric Cluster と SQL Server になります。</span><span class="sxs-lookup"><span data-stu-id="13227-212">The only thing present will be a configured Service Fabric cluster and SQL Server, which contain all of the replicated production data.</span></span> 

<span data-ttu-id="13227-213">ディザスター リカバリー環境をオンラインにするには、LCS を使用して運用環境で現在利用可能なものをディザスター リカバリー環境へと配置する必要があります。</span><span class="sxs-lookup"><span data-stu-id="13227-213">To bring the disaster recovery environment online, you'll need to have LCS deploy what is currently available in your Production environment into the disaster recovery environment.</span></span>

>[!IMPORTANT]
> <span data-ttu-id="13227-214">続行する前に、運用環境で Dynamics Service Fabric サービスが実行されていないことを確認してください (部分的な障害が原因で失敗しているだけの場合)。</span><span class="sxs-lookup"><span data-stu-id="13227-214">Before you continue, ensure that no Dynamics Service Fabric services are running in your production environment (in case you're only failing due to a partial disaster event).</span></span>

### <a name="deploy-the-localagent"></a><span data-ttu-id="13227-215">LocalAgent を配置する</span><span class="sxs-lookup"><span data-stu-id="13227-215">Deploy the LocalAgent</span></span>

<span data-ttu-id="13227-216">LocalAgent のインストーラーと構成ファイルを LCS からディザスター リカバリー環境にダウンロードします。</span><span class="sxs-lookup"><span data-stu-id="13227-216">Download the LocalAgent installer and configuration file from LCS to your disaster recovery environment.</span></span> <span data-ttu-id="13227-217">構成ファイルを作成後に開きます。</span><span class="sxs-lookup"><span data-stu-id="13227-217">After you have the configuration file, open it.</span></span> <span data-ttu-id="13227-218">ServiceFabric セクションの connectionEndpoint が、ディザスター リカバリー環境にあるサーバーの IP、または FQDN を指していることを確認します。</span><span class="sxs-lookup"><span data-stu-id="13227-218">Ensure that the connectionEndpoint under the serviceFabric section points to the IP or FQDN of a server in the disaster recovery environment.</span></span> <span data-ttu-id="13227-219">ファイルの変更後、そのファイルをローカルに保存し、通常どおり LocalAgent を配置します。</span><span class="sxs-lookup"><span data-stu-id="13227-219">After modifying the file, save it locally and deploy the LocalAgent as you typically would.</span></span>

>[!IMPORTANT]
> <span data-ttu-id="13227-220">LCS のコネクター設定には変更を加えないでください。</span><span class="sxs-lookup"><span data-stu-id="13227-220">Do not make changes to your connector settings in LCS.</span></span> 

<span data-ttu-id="13227-221">メインの運用環境がオンラインに戻ってくるまで、この LocalAgent は LCS がメッセージ キューに入れたすべての要求を処理します。</span><span class="sxs-lookup"><span data-stu-id="13227-221">Until your main production environment comes back online, this LocalAgent will process all requests that LCS puts into the message queue.</span></span> <span data-ttu-id="13227-222">そのため、運用環境でサービスが実行されていないことの確認が重要となります。</span><span class="sxs-lookup"><span data-stu-id="13227-222">That's why it's important that you ensure no services are running in your production environment.</span></span> <span data-ttu-id="13227-223">最終的には、オーケストレーター ノードがプライマリ データセンターに戻された際に、クラスターから LocalAgent のプロビジョニングを解除します。</span><span class="sxs-lookup"><span data-stu-id="13227-223">Eventually, when your orchestrator nodes come back up in your primary datacenter, unprovision the LocalAgent from the cluster.</span></span> 

>[!CAUTION]
> <span data-ttu-id="13227-224">LocalAgent は、一度に1つのデータセンターでのみ実行する必要があります。</span><span class="sxs-lookup"><span data-stu-id="13227-224">The LocalAgent must only be running in one datacenter at a time.</span></span> <span data-ttu-id="13227-225">この時点では、セカンダリ データセンターでのみ実行する必要があります。</span><span class="sxs-lookup"><span data-stu-id="13227-225">At this point it should only be running in your secondary datacenter.</span></span>

### <a name="prepare-your-pre-deployment-scripts-optional"></a><span data-ttu-id="13227-226">配置前スクリプトの準備 (オプション)</span><span class="sxs-lookup"><span data-stu-id="13227-226">Prepare your pre-deployment scripts (optional)</span></span>

<span data-ttu-id="13227-227">配置の構成に変更が必要な場合は、配置前スクリプトを実行する必要があります。</span><span class="sxs-lookup"><span data-stu-id="13227-227">Pre-deployment scripts are necessary when changes to the deployment configuration are required.</span></span> <span data-ttu-id="13227-228">このスクリプトでは、指定した値で config.json ファイルを修正する必要があります。</span><span class="sxs-lookup"><span data-stu-id="13227-228">This script will have to modify the config.json file with the values you specify.</span></span> <span data-ttu-id="13227-229">このスクリプトは、ユーザーが作成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="13227-229">It will be the customers' responsibility to create this script.</span></span>

<span data-ttu-id="13227-230">config.json ファイルの場所は、以下のコマンドを実行sいて確認できます。</span><span class="sxs-lookup"><span data-stu-id="13227-230">You can find the location of the config.json file by running the following command.</span></span>

  ```sql
    select Location from DeploymentInstanceArtifact where AssetId='config.json' and DeploymentInstanceId = 'LCSENVIRONMENTID'
  ```

  > [!NOTE]
  > <span data-ttu-id="13227-231">**LCSENVIRONMENTID** を環境の ID で置き換えます。</span><span class="sxs-lookup"><span data-stu-id="13227-231">Replace **LCSENVIRONMENTID** with the ID of your environment.</span></span> <span data-ttu-id="13227-232">この ID は LCS 環境の詳細ページから取得することができます。</span><span class="sxs-lookup"><span data-stu-id="13227-232">You can obtain this ID from the full details page for your environment in LCS.</span></span> 

<span data-ttu-id="13227-233">SSRS ノードの IP が異なる場合は、次の値を変更する必要があります。</span><span class="sxs-lookup"><span data-stu-id="13227-233">If the SSRS node IP is different, you'll have to modify the following values.</span></span>

```json
        "biReporting": {
          "persistentVirtualMachineIPAddressSSRS": {
            "value": "192.168.5.31"
          },
          "reportingServers": {
            "value": "192.168.5.31"
          },
```

<span data-ttu-id="13227-234">ホスト名を変更する場合は、次のように変更する必要があります。</span><span class="sxs-lookup"><span data-stu-id="13227-234">If you are changing the host name, the following modifications are required.</span></span>

```json
    "name": "AOS",
      "parameters": {
        "activeDirectory": {
          ...
          "aadValidAudience": {
            "value": "https://ax.contosoen05.com/"
          },
          ...
        "infrastructure": {
          "hostName": {
            "value": "ax.contosoen05.com"
          },
          ...
        }
    ...
    "name": "FinancialReporting",
      "parameters": {
        ...
        "aad": {
         ...
         "cookieDomain": {
            "value": "ax.contosoen05.com"
          },
          "validAudiences": {
            "value": "https://ax.contosoen05.com/"
          },
          ...
```

>[!IMPORTANT]
> <span data-ttu-id="13227-235">配置の際にホスト名の URL を変更する場合は、 AD FS サーバーが新規 URL を受け入れるように構成されていることを確認してください。</span><span class="sxs-lookup"><span data-stu-id="13227-235">If you are changing the hostname URL for your deployment, ensure that your AD FS server is configured to accept the new URL.</span></span> <span data-ttu-id="13227-236">詳細については、[複数の環境で同じ AD FS インスタンスを再利用する](./onprem-reuseadfs.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="13227-236">For more information, see [Reuse the same AD FS instance for multiple environments](./onprem-reuseadfs.md).</span></span>

<span data-ttu-id="13227-237">ファイル共有機能が運用環境とディザスター リカバリー環境で共有されている場合、この配置前スクリプトを無効化する必要があります。</span><span class="sxs-lookup"><span data-stu-id="13227-237">If the file share is shared between the production and disaster recovery environments, this pre-deployment script should be disabled.</span></span> <span data-ttu-id="13227-238">この機能は、ディザスター リカバリー環境に配置する場合にのみ有効にしてください。</span><span class="sxs-lookup"><span data-stu-id="13227-238">Only enable it when deploying to your disaster recovery environment.</span></span>

### <a name="ensure-reports-get-deployed"></a><span data-ttu-id="13227-239">レポートを確実に配置する</span><span class="sxs-lookup"><span data-stu-id="13227-239">Ensure reports get deployed</span></span>

<span data-ttu-id="13227-240">データベースは既にに正常に同期されているため、通常、同期はスキップされます。</span><span class="sxs-lookup"><span data-stu-id="13227-240">Because the database has previously been synchronized successfully, synchronization typically would be skipped.</span></span> <span data-ttu-id="13227-241">ただし、SSRS ノードが空であるため、レポートを同期するには、次の操作を実行します。</span><span class="sxs-lookup"><span data-stu-id="13227-241">However, to synchronize the reports because the SSRS node is empty, perform the following actions.</span></span>

#### <a name="version-10013-or-later"></a><span data-ttu-id="13227-242">バージョン 10.0.13 、またはそれ以降</span><span class="sxs-lookup"><span data-stu-id="13227-242">Version 10.0.13 or later</span></span>

<span data-ttu-id="13227-243">ビジネス データ データベース (AXDB) に対して次のコマンドを実行します。</span><span class="sxs-lookup"><span data-stu-id="13227-243">Run the following command against your business data database (AXDB):</span></span>

```sql
    UPDATE SF.synclog SET STATE=5, SyncStepName = 'ReportSyncstarted' WHERE CODEPACKAGEVERSION in (SELECT TOP(1) CODEPACKAGEVERSION from SF.SYNCLOG ORDER BY CREATIONDATE DESC)
```


#### <a name="version-10012-or-earlier"></a><span data-ttu-id="13227-244">バージョン 10.0.12、または以前</span><span class="sxs-lookup"><span data-stu-id="13227-244">Version 10.0.12 or earlier</span></span>

<span data-ttu-id="13227-245">ビジネス データ データベース (AXDB) に対して次のコマンドを実行します。</span><span class="sxs-lookup"><span data-stu-id="13227-245">Run the following command against your business data database (AXDB):</span></span>

```sql
    DELETE FROM SF.synclog WHERE CODEPACKAGEVERSION in (SELECT TOP(1) CODEPACKAGEVERSION from SF.SYNCLOG ORDER BY CODEPACKAGEVERSION DESC)
```

>[!NOTE]
> <span data-ttu-id="13227-246">バージョン 10.0.12、またはそれ以前のバージョンを使用している場合は、データベース全体が同期されます。</span><span class="sxs-lookup"><span data-stu-id="13227-246">If you are using version 10.0.12 or earlier, a full database synchronization will be executed.</span></span>

### <a name="deploy-your-environment"></a><span data-ttu-id="13227-247">環境の配置</span><span class="sxs-lookup"><span data-stu-id="13227-247">Deploy your environment</span></span>

<span data-ttu-id="13227-248">環境を配置するには、以下の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="13227-248">To deploy your environment, follow these instructions.</span></span> 

1. <span data-ttu-id="13227-249">LCS で、ご利用の運用環境の環境ページに移動します。</span><span class="sxs-lookup"><span data-stu-id="13227-249">In LCS, go to the environment page for your production environment.</span></span>

1. <span data-ttu-id="13227-250">**管理** を選択し、**更新の設定** を選択します。</span><span class="sxs-lookup"><span data-stu-id="13227-250">Select **Maintain** and then select **Update Settings**.</span></span>

    ![更新設定の適用](media/addf4f1d0c0a86d840a6a412f774e474.png)

1. <span data-ttu-id="13227-252">値を変更しないでください。</span><span class="sxs-lookup"><span data-stu-id="13227-252">Don't change any values.</span></span> <span data-ttu-id="13227-253">**準備** を選択します。</span><span class="sxs-lookup"><span data-stu-id="13227-253">Select **Prepare**.</span></span>

1. <span data-ttu-id="13227-254">ダウンロードと準備が完了後は、**環境の更新** ボタンが表示されます。</span><span class="sxs-lookup"><span data-stu-id="13227-254">After downloading is finished and preparation is completed, the **Update environment** button will be displayed.</span></span> <span data-ttu-id="13227-255">このボタンを選択して、環境の更新を開始します</span><span class="sxs-lookup"><span data-stu-id="13227-255">Select this button to start updating your environment</span></span>

    ![環境の更新ボタン](media/0a9d43044593450f1a828c0dd7698024.png)

1. <span data-ttu-id="13227-257">環境が配置されると、ディザスター リカバリー環境を使用できるようになります。</span><span class="sxs-lookup"><span data-stu-id="13227-257">After the environment is deployed, the disaster recovery environment is ready for use.</span></span> 

## <a name="using-your-disaster-recovery-environment"></a><span data-ttu-id="13227-258">ディザスター リカバリー環境を使用する</span><span class="sxs-lookup"><span data-stu-id="13227-258">Using your disaster recovery environment</span></span>

<span data-ttu-id="13227-259">ディザスター リカバリー環境は、通常どおり使用できます。また、更新や修正プログラムを環境に適用する必要はありません。</span><span class="sxs-lookup"><span data-stu-id="13227-259">You can use your disaster recovery environment as you typically would, except that updates or hotfixes shouldn't be applied to the environment.</span></span> <span data-ttu-id="13227-260">環境に更新プログラムを適用する必要がある場合、フェイルバックのプロセスは以下に説明するものとは異なります。</span><span class="sxs-lookup"><span data-stu-id="13227-260">If you must apply updates to your environment, your failback process will differ from the one described below.</span></span> <span data-ttu-id="13227-261">この条件下でのフェイルバックについては、このトピックでは説明しません。</span><span class="sxs-lookup"><span data-stu-id="13227-261">Failing back under this condition is not covered in this topic.</span></span>

## <a name="failing-back-to-your-production-environment"></a><span data-ttu-id="13227-262">運用環境へのフェイルバック</span><span class="sxs-lookup"><span data-stu-id="13227-262">Failing back to your production environment</span></span>

>[!IMPORTANT]
> <span data-ttu-id="13227-263">この時点では、運用環境で Dynamics Service Fabric サービスを実行する必要はありません。</span><span class="sxs-lookup"><span data-stu-id="13227-263">At this point, no Dynamics Service Fabric services should be running in your production environment.</span></span> 

<span data-ttu-id="13227-264">ディザスター リカバリー環境から運用環境への切り替えが可能なダウンタイムの時間枠を確保します。</span><span class="sxs-lookup"><span data-stu-id="13227-264">Secure a downtime window in which you can switch operation from the disaster recovery environment to the Production environment.</span></span> <span data-ttu-id="13227-265">ダウンタイムの時間枠で、ervice Fabric Explorer を介して、ディザスター リカバリー環境にあるオーケストレーター以外のすべてのノードを無効にします。</span><span class="sxs-lookup"><span data-stu-id="13227-265">In the downtime window, disable all non-Orchestrator nodes in the disaster recovery environment through Service Fabric Explorer.</span></span> <span data-ttu-id="13227-266">すべてのノードを無効化したら、SQL Server を運用データセンターにフェイルオーバーします。</span><span class="sxs-lookup"><span data-stu-id="13227-266">Once all nodes are disabled, failover your SQL Server to the production datacenter.</span></span>

<span data-ttu-id="13227-267">フェイルオーバーが発生したら、プライマリ データセンターで AOS、SSRS、MR の各ノードを起動します。</span><span class="sxs-lookup"><span data-stu-id="13227-267">After the failover has occurred, start the AOS, SSRS, and MR nodes in your primary datacenter.</span></span> <span data-ttu-id="13227-268">検証テストを実行し、環境が予想どおりに機能していることを確認します。</span><span class="sxs-lookup"><span data-stu-id="13227-268">Carry out validation tests to ensure that your environment is functioning as expected.</span></span> <span data-ttu-id="13227-269">環境が予想どおりに機能していると判断したら、ディザスター リカバリー環境から LocalAgent を削除し、運用環境に再インストールします。</span><span class="sxs-lookup"><span data-stu-id="13227-269">When you determine that your environment is working as expected, remove the LocalAgent from your disaster recovery environment and reinstall it on your Production environment.</span></span>

<span data-ttu-id="13227-270">すべての Dynamics Service Fabric サービスを手動で解除し、DR 環境をクリーンアップします。</span><span class="sxs-lookup"><span data-stu-id="13227-270">Clean up your DR environment by manually unprovisioning all Dynamics Service Fabric services.</span></span>

>[!CAUTION]
> <span data-ttu-id="13227-271">LCS のクリーンアップ機能を使用して、ディザスター リカバリー環境のクリーンアップを実行しないでください。</span><span class="sxs-lookup"><span data-stu-id="13227-271">Do not use the Cleanup functionality in LCS to perform the clean up of your disaster recovery environment.</span></span> 

### <a name="failback-checklist"></a><span data-ttu-id="13227-272">フェイルバックのチェックリスト</span><span class="sxs-lookup"><span data-stu-id="13227-272">Failback checklist</span></span>

- <span data-ttu-id="13227-273">非オーケストレーター ノードは、ディザスター リカバリー データセンターでは無効となります。</span><span class="sxs-lookup"><span data-stu-id="13227-273">Non-orchestrator nodes are disabled in disaster recovery datacenter.</span></span>
- <span data-ttu-id="13227-274">SQL Server がプライマリ データセンターにフェイルバックされます。</span><span class="sxs-lookup"><span data-stu-id="13227-274">SQL Server is failed back to primary datacenter.</span></span>
- <span data-ttu-id="13227-275">LocalAgent は、ご利用のディザスター リカバリー データ センターからアンインストールされます。</span><span class="sxs-lookup"><span data-stu-id="13227-275">LocalAgent is uninstalled in your disaster recovery datacenter.</span></span>
- <span data-ttu-id="13227-276">すべての Dynamics Service Fabric サービス (LocalAgent を含む) は、ご利用のプライマリ データセンターで実行されています。</span><span class="sxs-lookup"><span data-stu-id="13227-276">All Dynamics Service Fabric services (including LocalAgent) are running in your primary datacenter.</span></span>
- <span data-ttu-id="13227-277">ご利用のディザスター リカバリー データセンターには、Dynamics Service Fabric サービスが配置されていません。</span><span class="sxs-lookup"><span data-stu-id="13227-277">No Dynamics Service Fabric services are deployed in your disaster recovery datacenter.</span></span> 

>[!IMPORTANT]
> <span data-ttu-id="13227-278">ご利用のプライマリ環境は通常どおり機能しており、チェックリストのすべての品目が確実に検証された後でサービスを実行することができます。</span><span class="sxs-lookup"><span data-stu-id="13227-278">Your primary environment will be functioning as usual and can be serviced after you ensure that all items in the checklist are verified.</span></span>
