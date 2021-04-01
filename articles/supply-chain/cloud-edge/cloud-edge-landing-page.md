---
title: 製造と倉庫管理ワークロードのためのクラウドおよびエッジのスケール ユニット
description: このトピックでは、製造および倉庫管理のワークロードのクラウドおよびエッジのスケール ユニットに関する情報を提供します。
author: cabeln
manager: ''
ms.date: 10/06/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: SCM
ms.author: cabeln
ms.search.validFrom: 2020-09-23
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: fb0d8e0226b11e93503979c202da917de1df6319
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/15/2021
ms.locfileid: "5240440"
---
# <a name="cloud-and-edge-scale-units-for-manufacturing-and-warehouse-management-workloads"></a><span data-ttu-id="1dfa9-103">製造と倉庫管理ワークロードのためのクラウドおよびエッジのスケール ユニット</span><span class="sxs-lookup"><span data-stu-id="1dfa9-103">Cloud and edge scale units for manufacturing and warehouse management workloads</span></span>

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

<span data-ttu-id="1dfa9-104">クラウドおよびエッジのスケール ユニットによって、作業現場と倉庫の実行ワークロードを異なる環境間で配分できるようになります。</span><span class="sxs-lookup"><span data-stu-id="1dfa9-104">Cloud and edge scale units enable distribution of shop floor and warehouse execution workloads among different environments.</span></span> <span data-ttu-id="1dfa9-105">この機能は、パフォーマンスの向上、サービス中断の防止、アップタイムの最大化に役立ちます。</span><span class="sxs-lookup"><span data-stu-id="1dfa9-105">This functionality can help improve performance, prevent service interruptions, and maximize uptime.</span></span> <span data-ttu-id="1dfa9-106">この情報は、次のアドインによって提供されます。</span><span class="sxs-lookup"><span data-stu-id="1dfa9-106">It's provided by the following add-ins:</span></span>

- <span data-ttu-id="1dfa9-107">Dynamics 365 Supply Chain Management のクラウド スケール ユニットのアドイン</span><span class="sxs-lookup"><span data-stu-id="1dfa9-107">Cloud Scale Unit Add-in for Dynamics 365 Supply Chain Management</span></span>
- <span data-ttu-id="1dfa9-108">Dynamics 365 Supply Chain Management のエッジ スケール ユニットのアドイン</span><span class="sxs-lookup"><span data-stu-id="1dfa9-108">Edge Scale Unit Add-in for Dynamics 365 Supply Chain Management</span></span>

<span data-ttu-id="1dfa9-109">製造と流通が行われる会社は、重要な業務プロセスを年中無休 24 時間対応で実行でき、中断や規模の変更を行うことはできません。</span><span class="sxs-lookup"><span data-stu-id="1dfa9-109">Companies that work with manufacturing and distribution must be able to run key business processes 24/7, without interruption and at scale.</span></span> <span data-ttu-id="1dfa9-110">クラウドおよびエッジのスケール ユニットを使用すると、ネットワーク接続や待機時間の問題が発生した場合でも、業務上不可欠な製造および倉庫の主要なプロセスを中断することなく実行できます。</span><span class="sxs-lookup"><span data-stu-id="1dfa9-110">Cloud and edge scale units enable companies to run key mission-critical manufacturing and warehouse processes without interruption, even when faced with occasional network connectivity or latency issues.</span></span>

## <a name="public-preview-information"></a><span data-ttu-id="1dfa9-111">パブリック プレビュー情報</span><span class="sxs-lookup"><span data-stu-id="1dfa9-111">Public preview information</span></span>

<span data-ttu-id="1dfa9-112">このプレビューでは、Dynamics 365 Supply Chain Management 環境のクラウドベースのハブとして機能する環境と、クラウド スケール ユニットとして機能する 1 つの環境を提供します。</span><span class="sxs-lookup"><span data-stu-id="1dfa9-112">The preview provides one environment that functions as a cloud-based hub of your Dynamics 365 Supply Chain Management environment and one environment that functions as a cloud scale unit.</span></span>

<!-- You will also be able to use Local Business Data (LBD) to configure an on-premises environment as an edge scale unit for the hub you received as part of the preview program.-->

### <a name="preview-availability"></a><span data-ttu-id="1dfa9-113">プレビューの可用性</span><span class="sxs-lookup"><span data-stu-id="1dfa9-113">Preview availability</span></span>

<span data-ttu-id="1dfa9-114">クラウドおよびエッジのスケール ユニットのプレビューは、2020 年 10 月に Supply Chain Management の既存の顧客が使用できるようになります。</span><span class="sxs-lookup"><span data-stu-id="1dfa9-114">The preview for cloud and edge scale units becomes available for existing customers of Supply Chain Management in October 2020.</span></span>

<span data-ttu-id="1dfa9-115">[Microsoft Dynamics Lifecycle Services (LCS)](https://lcs.dynamics.com/v2) 環境でデプロイ用に 10 月のプレビュー リリース 10.0.15/プラットフォーム アップデート 39 にアクセスするには、Supply Chain Management のプレビュー アーリー アクセス プログラム (PEAP とも呼ばれる) を持っている必要があります。</span><span class="sxs-lookup"><span data-stu-id="1dfa9-115">To access the October preview release 10.0.15/Platform update 39 for deployment in your [Microsoft Dynamics Lifecycle Services (LCS)](https://lcs.dynamics.com/v2) environment, you must be part of the preview early access program (also known as PEAP) for Supply Chain Management.</span></span> <span data-ttu-id="1dfa9-116">より広範な [Dynamics Insider Program](https://experience.dynamics.com/insider) のメンバーに既になっている場合は、PEAP に参加できます。</span><span class="sxs-lookup"><span data-stu-id="1dfa9-116">You can join PEAP if you're already a member of the broader [Dynamics Insider Program](https://experience.dynamics.com/insider).</span></span> <span data-ttu-id="1dfa9-117">"Finance & Operations: Preview early access program (PEAP)" という名前の特定プログラムを選択するだけです。</span><span class="sxs-lookup"><span data-stu-id="1dfa9-117">Just select the specific program that is named "Finance & Operations: Preview early access program (PEAP)."</span></span>

> [!IMPORTANT]
> <span data-ttu-id="1dfa9-118">Supply Chain Management のスケール ユニット機能は、[Finance and Operations のクラウド + エッジ プレビューの条件](https://Aka.ms/SCMCnETerms) に合意した場合にのみ使用可能になります。</span><span class="sxs-lookup"><span data-stu-id="1dfa9-118">The scale unit capability for Supply Chain Management is made available only if you agree to the [Cloud + Edge Preview for Finance and Operations terms](https://Aka.ms/SCMCnETerms).</span></span>

### <a name="data-processing-for-the-preview"></a><span data-ttu-id="1dfa9-119">プレビューのデータ処理</span><span class="sxs-lookup"><span data-stu-id="1dfa9-119">Data processing for the preview</span></span>

<span data-ttu-id="1dfa9-120">パブリック プレビュー中に、一部の管理サービスは米国でのみでホストされます。</span><span class="sxs-lookup"><span data-stu-id="1dfa9-120">During the public preview, some management services will only be hosted in the United States.</span></span> <span data-ttu-id="1dfa9-121">ただし、この機能を使用できるようになると、Supply Chain Management でサポートされているすべての地域で、この管理サービスを利用できるようになります。</span><span class="sxs-lookup"><span data-stu-id="1dfa9-121">However, when the feature becomes generally available, these management services will be available in all geographies supported by Supply Chain Management.</span></span> <span data-ttu-id="1dfa9-122">これにより、スケール ユニット マネージャによって使用される管理情報の転送と保管に影響します。これには次のものが含まれています。</span><span class="sxs-lookup"><span data-stu-id="1dfa9-122">This affects the transfer and storage of administrative information used by the scale unit manager, including:</span></span>

- <span data-ttu-id="1dfa9-123">テナント名と ID</span><span class="sxs-lookup"><span data-stu-id="1dfa9-123">Your tenant names and IDs</span></span>
- <span data-ttu-id="1dfa9-124">自分の LCS プロジェクト ID</span><span class="sxs-lookup"><span data-stu-id="1dfa9-124">Your LCS project IDs</span></span>
- <span data-ttu-id="1dfa9-125">ログインに使用する管理者のメール</span><span class="sxs-lookup"><span data-stu-id="1dfa9-125">Administrator emails used to sign in</span></span>
- <span data-ttu-id="1dfa9-126">ハブとスケール ユニットの環境 ID</span><span class="sxs-lookup"><span data-stu-id="1dfa9-126">Environment IDs for hub and scale units</span></span>
- <span data-ttu-id="1dfa9-127">ワークロードの構成</span><span class="sxs-lookup"><span data-stu-id="1dfa9-127">Workload configurations</span></span>
- <span data-ttu-id="1dfa9-128">[マップ分析] ページに表示される収集されたメトリック (遅延時間やスループットなど)</span><span class="sxs-lookup"><span data-stu-id="1dfa9-128">Collected metrics (such as latency and throughput) which are displayed on the map analysis page</span></span>

<span data-ttu-id="1dfa9-129">米国データ センターに転送および保存されたデータは、プレビュー環境をシャットダウンしたときに削除されます。</span><span class="sxs-lookup"><span data-stu-id="1dfa9-129">Data transferred to and stored in the US data centers will be deleted when your preview environments are shut down.</span></span>

### <a name="sign-up-for-the-preview"></a><span data-ttu-id="1dfa9-130">プレビューへのサインアップ</span><span class="sxs-lookup"><span data-stu-id="1dfa9-130">Sign up for the preview</span></span>

<span data-ttu-id="1dfa9-131">Supply Chain Management のためにクラウドとエッジのプレビューを登録するには、組織が既に Supply Chain Management のクラウド環境を所有している必要があります。</span><span class="sxs-lookup"><span data-stu-id="1dfa9-131">To sign up for the cloud and edge preview for Supply Chain Management, your organization must already have a live Supply Chain Management cloud environment.</span></span>

<span data-ttu-id="1dfa9-132">スケール ユニット機能は現在、パブリック プレビューにあります。</span><span class="sxs-lookup"><span data-stu-id="1dfa9-132">The scale unit capabilities are currently in public preview.</span></span> <span data-ttu-id="1dfa9-133">サインアップを行うときには、特定のテナントに対してユーザー アカウントを使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="1dfa9-133">When you sign up, you must use a user account on the specific tenant.</span></span> <span data-ttu-id="1dfa9-134">また、プロジェクトの所有者やそのテナントの有効な Dynamics 365 LCS プロジェクトの環境管理者でもある必要があります。</span><span class="sxs-lookup"><span data-stu-id="1dfa9-134">You must also be a project owner or an environment admin in LCS for an active Dynamics 365 LCS project in that tenant.</span></span>

<span data-ttu-id="1dfa9-135">プレビューにサインアップする際には、テナントを選択し、サインアップの手順に進みます。</span><span class="sxs-lookup"><span data-stu-id="1dfa9-135">When you sign up for the preview, you will select a tenant and go through the sign-up steps.</span></span> <span data-ttu-id="1dfa9-136">Microsoft はプレビュー容量を割り当てるとすぐに、適切な LCS プロジェクトのための 2 つの環境 (ハブとスケール ユニット) の [プロビジョニングの詳細] や [プロモーション] コードを含む電子メールを送信します。</span><span class="sxs-lookup"><span data-stu-id="1dfa9-136">As soon as Microsoft can allocate preview capacity, we will send you an email that includes the provisioning details and the promotion (promo) codes for two environments (a hub and a scale unit) for the appropriate LCS project.</span></span> <span data-ttu-id="1dfa9-137">これにより、2 つの環境を、第 2 階層のサンドボックス環境として配置できるようになります。</span><span class="sxs-lookup"><span data-stu-id="1dfa9-137">You will then be able to deploy the two environments as tier-2 sandbox environments.</span></span> <span data-ttu-id="1dfa9-138">これらの環境では、プロモーション コードの作成日からの有効期間は 60 日です。</span><span class="sxs-lookup"><span data-stu-id="1dfa9-138">Those environments will be valid 60 days from the creation date of the promo codes.</span></span> <span data-ttu-id="1dfa9-139">次の段落で説明されている手順が完了するまでは、2 つの環境を使用しないでください。</span><span class="sxs-lookup"><span data-stu-id="1dfa9-139">You should not use the two environments until the step that is described in the next paragraph is completed.</span></span>

<span data-ttu-id="1dfa9-140">2 つの環境がプロモーションコードを使用して配置されていることを確認した後、いずれかの環境がハブとして機能するように構成され、もう一方がスケール ユニットとして機能するように構成されます。</span><span class="sxs-lookup"><span data-stu-id="1dfa9-140">After you confirm with Microsoft that the two environments have been deployed by using the promo codes, one of the environments will be configured to work as a hub, and the other will be configured to work as a scale unit.</span></span> <span data-ttu-id="1dfa9-141">その後、スケール ユニットを構成したり、選択した倉庫管理と製造ワークロードを [スケール ユニット マネージャー ポータル](https://aka.ms/SCMSUM) を使用して配置したりできます。</span><span class="sxs-lookup"><span data-stu-id="1dfa9-141">You can then configure the scale units and deploy selected warehouse management and manufacturing workloads by using the [Scale Unit Manager portal](https://aka.ms/SCMSUM).</span></span>

<span data-ttu-id="1dfa9-142">プレビュー環境は、60 日後に自動的に削除されます。</span><span class="sxs-lookup"><span data-stu-id="1dfa9-142">Preview environments will automatically be deleted after 60 days.</span></span> <span data-ttu-id="1dfa9-143">ただし、使用されていない可能性がある場合は、すぐに削除されることがあります。</span><span class="sxs-lookup"><span data-stu-id="1dfa9-143">However, they might be deleted sooner if it appears that they aren't being used.</span></span> <span data-ttu-id="1dfa9-144">プレビュー環境を削除した後で、サインアップしてキューに追加し、新しいプレビューをデプロイすることができます。</span><span class="sxs-lookup"><span data-stu-id="1dfa9-144">After your preview environments have been deleted, you can sign up and queue up for a new preview deployment.</span></span>

<span data-ttu-id="1dfa9-145">プレビューにサインアップするには、[スケール ユニット マネージャー ポータル](https://aka.ms/SCMSUM) に移動します。</span><span class="sxs-lookup"><span data-stu-id="1dfa9-145">To sign up for the preview, go to the [Scale Unit Manager portal](https://aka.ms/SCMSUM).</span></span>

### <a name="limitations-that-apply-during-the-preview-period"></a><span data-ttu-id="1dfa9-146">プレビュー期間中に適用される制限事項</span><span class="sxs-lookup"><span data-stu-id="1dfa9-146">Limitations that apply during the preview period</span></span>

> [!IMPORTANT]
> <span data-ttu-id="1dfa9-147">この機能のプレビュー プログラムの初期フェーズでは、Microsoft は、エッジ スケール ユニットを持つハブではなく、クラウド スケール ユニットが設定されたハブのみをサポートしています。</span><span class="sxs-lookup"><span data-stu-id="1dfa9-147">For the initial phase of the preview program for this feature, Microsoft is supporting only hubs that have cloud scale units, not hubs that have edge scale units.</span></span> <span data-ttu-id="1dfa9-148">エッジ スケール ユニットはオンプレミスでインストールされており、プログラムの今後のフェーズで使用できるようになります。</span><span class="sxs-lookup"><span data-stu-id="1dfa9-148">Edge scale units are installed on-premises and are expected to become available during an upcoming phase of the program.</span></span>

<span data-ttu-id="1dfa9-149">クラウドおよびエッジのスケール ユニットはプレビュー機能であるため、これらに関連するサービスは現在、限定された国および地域で使用できます。</span><span class="sxs-lookup"><span data-stu-id="1dfa9-149">Because cloud and edge scale units are a preview feature, services that are related to them are currently available in limited countries and regions.</span></span> <span data-ttu-id="1dfa9-150">クラウドおよびエッジのスケール ユニットを有効にすることにより、クラウドおよびエッジのスケール ユニットの構成と処理に関連するデータが米国にあるデータ センターに保存されることを理解できることを確認してください。</span><span class="sxs-lookup"><span data-stu-id="1dfa9-150">By enabling cloud and edge scale units, you affirm that you understand that some data that is related to the configuration and processing of cloud and edge scale units might be stored in a data center that is located in the United States.</span></span> <span data-ttu-id="1dfa9-151">クラウドおよびエッジのスケール ユニット を有効にすることにより、[Finance and Operations のクラウド + エッジ プレビューの条件](https://Aka.ms/SCMCnETerms) にも同意することになります。</span><span class="sxs-lookup"><span data-stu-id="1dfa9-151">By enabling cloud and edge scale units, you also agree to the [Cloud + Edge Preview for Finance and Operations terms](https://Aka.ms/SCMCnETerms).</span></span> <span data-ttu-id="1dfa9-152">クラウドおよびエッジのスケール ユニット の詳細については、[ドキュメント](https://aka.ms/scmcne) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="1dfa9-152">To learn more about cloud and edge scale units, see the [documentation](https://aka.ms/scmcne).</span></span>

<span data-ttu-id="1dfa9-153">Microsoft にとってお客様のプライバシーは重要です。</span><span class="sxs-lookup"><span data-stu-id="1dfa9-153">Your privacy is important to Microsoft.</span></span> <span data-ttu-id="1dfa9-154">詳細については、Microsoft の [プライバシーに関する声明](https://aka.ms/privacy) をお読みください。</span><span class="sxs-lookup"><span data-stu-id="1dfa9-154">To learn more, read our [Privacy Statement](https://aka.ms/privacy).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="1dfa9-155">ワークロードがスケール ユニットで使用されている場合は、すべてのビジネス機能がパブリック プレビューで完全にサポートされているわけではありません。</span><span class="sxs-lookup"><span data-stu-id="1dfa9-155">Some business functionality isn't fully supported in the public preview when workloads are used on scale units.</span></span> <span data-ttu-id="1dfa9-156">機能ワークロードの詳細については、このトピックで後述するセクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="1dfa9-156">For more information about the functional workloads, see the sections later in this topic.</span></span>

## <a name="scale-units-and-dedicated-workloads"></a><span data-ttu-id="1dfa9-157">スケール ユニットと専用ワークロード</span><span class="sxs-lookup"><span data-stu-id="1dfa9-157">Scale units and dedicated workloads</span></span>

:::image type="content" source="./media/cloud_edge-HeroDiagram.png" alt-text="スケール ユニット付き Dynamics 365":::

<span data-ttu-id="1dfa9-159">スケール ユニットは、専用の処理能力を追加することによって、Supply Chain Management の中央ハブ環境を拡張します。</span><span class="sxs-lookup"><span data-stu-id="1dfa9-159">Scale units extend your central Supply Chain Management hub environment by adding dedicated processing capacity.</span></span> <span data-ttu-id="1dfa9-160">スケール ユニットはクラウドで実行できます。</span><span class="sxs-lookup"><span data-stu-id="1dfa9-160">Scale units can run in the cloud.</span></span> <span data-ttu-id="1dfa9-161">また、ローカル施設内のエッジで実行することもできます。</span><span class="sxs-lookup"><span data-stu-id="1dfa9-161">Alternatively, they can run on the edge at your local facility premises.</span></span> <span data-ttu-id="1dfa9-162">スケール ユニットは、ハブ環境から一時的に切断できます。</span><span class="sxs-lookup"><span data-stu-id="1dfa9-162">Scale units can temporarily be disconnected from the hub environment.</span></span> <span data-ttu-id="1dfa9-163">これらが接続されている場合、スケール ユニットでは、割り当てられたワークロードの専用処理を実行するために必要なすべての情報が表示されます。</span><span class="sxs-lookup"><span data-stu-id="1dfa9-163">When they are connected, scale units receive all the information that is required to run the dedicated processing for assigned workloads.</span></span>

:::image type="content" source="media/cloud_edge-previewoptions.png" alt-text="パブリック プレビューのスケール ユニット オプション":::

<span data-ttu-id="1dfa9-165">パブリック プレビューの場合は、スケール ユニット マネージャ ポータルを使用して、選択したワークロードを使用して、クラウド スケール単位でハブ環境を構成できます。</span><span class="sxs-lookup"><span data-stu-id="1dfa9-165">For the public preview, you can configure a hub environment with selected workloads on a cloud scale unit by using the Scale Unit Manager portal.</span></span> <span data-ttu-id="1dfa9-166">ローカル ビジネス データ (LBD) オンプレミス環境へのアクセス許可を持つ参加者は、LBD 環境をエッジ スケール ユニットとして構成することもできます。</span><span class="sxs-lookup"><span data-stu-id="1dfa9-166">Preview participants who have access to a Local Business Data (LBD) on-premises environment can also configure the LBD environment as an edge scale unit.</span></span>

<span data-ttu-id="1dfa9-167">ワークロードとは、定義された一連のビジネス機能であり、除外してスケール ユニットに委任することができます。</span><span class="sxs-lookup"><span data-stu-id="1dfa9-167">A workload is a defined set of business functionality that can be factored out and delegated to a scale unit.</span></span> <span data-ttu-id="1dfa9-168">現在、プレビュー機能には次の 2 つのタイプのワークロードがあります。</span><span class="sxs-lookup"><span data-stu-id="1dfa9-168">Currently, the preview features two types of workloads:</span></span>

- <span data-ttu-id="1dfa9-169">製造実行</span><span class="sxs-lookup"><span data-stu-id="1dfa9-169">Manufacturing execution</span></span>
- <span data-ttu-id="1dfa9-170">倉庫管理</span><span class="sxs-lookup"><span data-stu-id="1dfa9-170">Warehouse management</span></span>

<span data-ttu-id="1dfa9-171">スケール ユニットごとに、各タイプのワークロードのいずれかを割り当てることができます。</span><span class="sxs-lookup"><span data-stu-id="1dfa9-171">You can assign one of each type of workload per scale unit.</span></span> 

### <a name="dedicated-manufacturing-execution-workload-capabilities-in-a-scale-unit"></a><span data-ttu-id="1dfa9-172">スケール ユニットの専用の製造実行ワークロード機能</span><span class="sxs-lookup"><span data-stu-id="1dfa9-172">Dedicated manufacturing execution workload capabilities in a scale unit</span></span>

<span data-ttu-id="1dfa9-173">エッジ ユニットがクラウドに接続されていない場合でも、製造実行のために、クラウドおよびエッジのスケール ユニットには次の機能があります。</span><span class="sxs-lookup"><span data-stu-id="1dfa9-173">For manufacturing execution, cloud and edge scale units deliver the following capabilities, even when the edge units aren't connected to the cloud:</span></span>

- <span data-ttu-id="1dfa9-174">機械オペレーターと作業現場監督は、運用生産計画にアクセスできます。</span><span class="sxs-lookup"><span data-stu-id="1dfa9-174">Machine operators and shop floor supervisors can access the operational production plan.</span></span>
- <span data-ttu-id="1dfa9-175">機械オペレーターは、個々の製造ジョブを実行することによって、計画を最新の状態に保つことができます。</span><span class="sxs-lookup"><span data-stu-id="1dfa9-175">Machine operators can keep the plan up to date by running discrete and process manufacturing jobs.</span></span>
- <span data-ttu-id="1dfa9-176">作業現場の監修者は、運用計画を調整できます。</span><span class="sxs-lookup"><span data-stu-id="1dfa9-176">The shop floor supervisor can adjust the operational plan.</span></span>
- <span data-ttu-id="1dfa9-177">作業者は、出勤と出勤の出勤と退勤をエッジで確認して、作業者の支払計算を正しく行うことができます。</span><span class="sxs-lookup"><span data-stu-id="1dfa9-177">Workers can access time and attendance for clock-in and clock-out on the edge, to ensure correct worker pay calculation.</span></span>

<span data-ttu-id="1dfa9-178">詳細については、[製造スケール ユニットのワークロードの詳細](cloud-edge-workload-manufacturing.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="1dfa9-178">For more information, see the [manufacturing scale unit workload details](cloud-edge-workload-manufacturing.md).</span></span>

### <a name="dedicated-warehouse-management-workload-capabilities-in-a-scale-unit"></a><span data-ttu-id="1dfa9-179">スケール ユニットの専用の倉庫管理ワークロード機能</span><span class="sxs-lookup"><span data-stu-id="1dfa9-179">Dedicated warehouse management workload capabilities in a scale unit</span></span>

<span data-ttu-id="1dfa9-180">倉庫管理については、エッジ ユニットがクラウドに接続されていない場合でも、クラウドおよびエッジのスケール ユニットには次の機能があります。</span><span class="sxs-lookup"><span data-stu-id="1dfa9-180">For warehouse management, cloud and edge scale units deliver the following capabilities, even when edge units aren't connected to the cloud:</span></span>

- <span data-ttu-id="1dfa9-181">選択されたウェーブ メソッドの処理は、販売注文と需要補充に対して有効化されています。</span><span class="sxs-lookup"><span data-stu-id="1dfa9-181">Processing of selected wave methods is enabled for sales orders and demand replenishment.</span></span>
- <span data-ttu-id="1dfa9-182">倉庫の作業者は、倉庫アプリを使用して販売と需要の補充倉庫作業を実行できます。</span><span class="sxs-lookup"><span data-stu-id="1dfa9-182">Warehouse workers can run sales and demand replenishment warehouse work by using the warehouse app.</span></span>
- <span data-ttu-id="1dfa9-183">倉庫の作業者は、倉庫アプリを使用して手持在庫を照会できます。</span><span class="sxs-lookup"><span data-stu-id="1dfa9-183">Warehouse workers can inquire into on-hand inventory by using the warehouse app.</span></span>
- <span data-ttu-id="1dfa9-184">倉庫の作業者は、倉庫アプリを使用して手持在庫の移動を作成および実行できます。</span><span class="sxs-lookup"><span data-stu-id="1dfa9-184">Warehouse workers can create and run inventory movements by using the warehouse app.</span></span>
- <span data-ttu-id="1dfa9-185">倉庫作業者は、倉庫アプリを使用した発注書の登録と、プットアウェイの実行をできます。</span><span class="sxs-lookup"><span data-stu-id="1dfa9-185">Warehouse workers can register purchase orders and do putaway by using the warehouse app.</span></span>

<span data-ttu-id="1dfa9-186">詳細については、[倉庫スケール ユニットのワークロードの詳細](cloud-edge-workload-warehousing.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="1dfa9-186">For more information, see the [warehouse scale unit workload details](cloud-edge-workload-warehousing.md).</span></span>

## <a name="onboard-scale-units-for-your-supply-chain-management-environment"></a><span data-ttu-id="1dfa9-187">Supply Chain Management 環境用のオンボードスケール ユニット</span><span class="sxs-lookup"><span data-stu-id="1dfa9-187">Onboard scale units for your Supply Chain Management environment</span></span>

### <a name="deploy-the-preview-for-cloud-and-edge-scale-units"></a><span data-ttu-id="1dfa9-188">クラウドおよびエッジのスケール ユニットのプレビューのデプロイ</span><span class="sxs-lookup"><span data-stu-id="1dfa9-188">Deploy the preview for cloud and edge scale units</span></span>

<span data-ttu-id="1dfa9-189">次の図は、クラウド スケール ユニットのパブリック プレビューのサインアップとプロビジョニングの流れを示しています。</span><span class="sxs-lookup"><span data-stu-id="1dfa9-189">The following illustration shows the sign-up and provisioning flow for the public preview for cloud scale units.</span></span>

:::image type="content" source="media/cloud_edge-previewsignup.png" alt-text="サインアップ手順のプレビュー":::

### <a name="select-your-lcs-project-tenant-and-the-detailed-preview-process"></a><span data-ttu-id="1dfa9-191">LCS プロジェクト テナントと詳細プレビュー プロセスの選択</span><span class="sxs-lookup"><span data-stu-id="1dfa9-191">Select your LCS project tenant and the detailed preview process</span></span>

<span data-ttu-id="1dfa9-192">パブリック プレビューでは、[スケール ユニット マネージャー ポータル](https://aka.ms/SCMSUM) は、自分のアカウントが含まれている、自分が LCS プロジェクトの所有者または環境管理者であるテナントの一覧が表示されます。</span><span class="sxs-lookup"><span data-stu-id="1dfa9-192">In the public preview, the [Scale Unit Manager portal](https://aka.ms/SCMSUM) shows the list of tenants that your account is part of, and where you're an owner or environment admin for an LCS project.</span></span>

<span data-ttu-id="1dfa9-193">探しているテナントがこの一覧に含まれていない場合、[LCS](https://lcs.dynamics.com/v2) に移動して、環境管理者か、そのテナントの LCS プロジェクトのプロジェクト所有者かを確認してください。</span><span class="sxs-lookup"><span data-stu-id="1dfa9-193">If the tenant that you're looking for isn't in this list, go to [LCS](https://lcs.dynamics.com/v2), and make sure that you're either an environment admin or a project owner of the LCS project for that tenant.</span></span> <span data-ttu-id="1dfa9-194">選択したテナントの Azure Active Directory (Azure AD) アカウントのみが、サインアップのエクスペリエンスを完了することが許可されています。</span><span class="sxs-lookup"><span data-stu-id="1dfa9-194">Note that only Azure Active Directory (Azure AD) accounts from the selected tenant are authorized to complete the sign-up experience.</span></span>

> [!NOTE]
> <span data-ttu-id="1dfa9-195">LCS に変更を適用した後は、テナントの一覧に変更が反映されるまでに最大で 30 分かかる場合があります。</span><span class="sxs-lookup"><span data-stu-id="1dfa9-195">After you apply changes to LCS, it might take up to 30 minutes for the list of tenants to reflect the changes.</span></span>

<span data-ttu-id="1dfa9-196">一覧には、テナントごとにサインアップのステータスが表示されます。</span><span class="sxs-lookup"><span data-stu-id="1dfa9-196">For each tenant, the list shows the sign-up status.</span></span>

:::image type="content" source="media/cloud_edge-Signup1.png" alt-text="テナントのサインアップ オプション":::

<span data-ttu-id="1dfa9-198">**こちらをクリックしてサインアップ** リンクを選択して、自分の LCS テナントにサインアップして、プレビューに参加できます。</span><span class="sxs-lookup"><span data-stu-id="1dfa9-198">Select the **Click here to sign up** link to sign up your LCS tenant to participate in the preview.</span></span> <span data-ttu-id="1dfa9-199">この条件は同意する必要があります。</span><span class="sxs-lookup"><span data-stu-id="1dfa9-199">You must accept the terms.</span></span> <span data-ttu-id="1dfa9-200">また、Microsoft がプレビューのサインアップ処理に関連するメールアドレスを送信できるようにする必要があります。</span><span class="sxs-lookup"><span data-stu-id="1dfa9-200">You must also supply a business email address where Microsoft can send communications that are related the preview sign-up process.</span></span>

:::image type="content" source="media/cloud_edge-Signup2.png" alt-text="テナントのサインアップ送信":::

<span data-ttu-id="1dfa9-202">Microsoft は、あなたの要求を確認し、サインアップ フォームに入力した住所にメールで次の手順を通知します。</span><span class="sxs-lookup"><span data-stu-id="1dfa9-202">Microsoft will review your request and inform you about the next steps by sending an email to the address that you supplied on the sign-up form.</span></span>

<span data-ttu-id="1dfa9-203">プレビュー プログラムへのアクセス許可が付与されると、LCS プロジェクトに対して 2 つのプロモーション コードが提供されます。</span><span class="sxs-lookup"><span data-stu-id="1dfa9-203">After you've been granted access to the preview program, you will receive two promo codes for your LCS project.</span></span> <span data-ttu-id="1dfa9-204">これにより、これらのプロモーション コードを使用して LCS に 2 つの環境を配置することができます。</span><span class="sxs-lookup"><span data-stu-id="1dfa9-204">You can now use those promo codes to deploy two environments in LCS.</span></span> <span data-ttu-id="1dfa9-205">環境では、PEAP リリース 10.0.15 かそれ以降のバージョンを使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="1dfa9-205">The environments must use PEAP release 10.0.15 or later.</span></span> <span data-ttu-id="1dfa9-206">プロモーション コードの適用が完了したら、(指示に従って) Microsoftに通知して、プレビュー機能のための環境の有効化を完了します。</span><span class="sxs-lookup"><span data-stu-id="1dfa9-206">When you've finished applying the promo codes, notify Microsoft (as instructed), so that we can finish enabling the environments for the preview features.</span></span> <span data-ttu-id="1dfa9-207">この構成手順が完了したときには、Microsoft から通知をお伝えします。</span><span class="sxs-lookup"><span data-stu-id="1dfa9-207">Microsoft will let you know when this configuration step is completed.</span></span>

<span data-ttu-id="1dfa9-208">プレビュー環境でのスケール ユニットとワークロードの構成を開始できるようになりました。</span><span class="sxs-lookup"><span data-stu-id="1dfa9-208">You can now start to configure scale units and workloads in your preview environment.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="1dfa9-209">Cloud Scale Unit を構成する際に、[スケール ユニット マネージャー ポータルで必要なステップをすべて実行](#scale-unit-manager-portal) できます。</span><span class="sxs-lookup"><span data-stu-id="1dfa9-209">When you configure cloud scale units, you can [do all the required steps in the Scale Unit Manager portal](#scale-unit-manager-portal).</span></span>
<!-- 
> If want to use edge scale units with your preview deployment, you must do all scale unit configuration in the user interface on the hub as described in [Configure the hub environment for use with edge scale units](cloud-edge-edge-scale-units-lbd.md#configure-the-hub-environment). You can't use Scale Unit Manager portal if you include an edge scale unit. -->

### <a name="manage-cloud-scale-units-and-workloads-by-using-the-scale-unit-manager-portal"></a><a name="scale-unit-manager-portal"></a><span data-ttu-id="1dfa9-210">スケール ユニット マネージャー ポータルを使用して、Cloud Scale Unit とワークロードを管理します</span><span class="sxs-lookup"><span data-stu-id="1dfa9-210">Manage cloud scale units and workloads by using the Scale Unit Manager portal</span></span>

<span data-ttu-id="1dfa9-211">[スケール ユニット マネージャー ポータル](https://aka.ms/SCMSUM) に移動して、テナント アカウントを使用してログインします。</span><span class="sxs-lookup"><span data-stu-id="1dfa9-211">Go to the [Scale Unit Manager portal](https://aka.ms/SCMSUM), and sign in by using your tenant account.</span></span> <span data-ttu-id="1dfa9-212">**スケール ユニットの構成** ページでは、ハブ環境がまだ一覧にない場合は追加できます。</span><span class="sxs-lookup"><span data-stu-id="1dfa9-212">On the **Configure scale units** page, you can add a hub environment if it isn't already listed.</span></span> <span data-ttu-id="1dfa9-213">次に、スケール ユニットとワークロードを構成するハブを選択できます。</span><span class="sxs-lookup"><span data-stu-id="1dfa9-213">You can then select the hub that you want to configure with scale units and workloads.</span></span>

:::image type="content" source="media/cloud_edge-Manage.png" alt-text="スケール ユニットとワークロードの管理体験":::

<span data-ttu-id="1dfa9-215">トポロジーで使用できる 1 つ以上のスケール ユニットを追加するには、**スケール ユニットを追加** を選択します。</span><span class="sxs-lookup"><span data-stu-id="1dfa9-215">To add one or more scale units that are available in your topology, select **Add scale units**.</span></span> <span data-ttu-id="1dfa9-216">このプレビューでは、プレビュー プログラムの一部として受け取ったいずれかのプロモーション コードから配置したクラウドのスケール ユニットが表示されます。</span><span class="sxs-lookup"><span data-stu-id="1dfa9-216">In the preview, you should see the cloud scale unit that you deployed from one of the promo codes that you received as part of the preview program.</span></span>

<!--  [!IMPORTANT]
> In the public preview, the Scale Unit Manager portal shows the cloud scale unit that you received as part of the preview program. Any edge scale unit that you created based on an LBD configuration can't be managed in the Scale Unit Manager portal yet. For configuration details, see [Deploy custom edge scale units on custom hardware using LBD](cloud-edge-edge-scale-units-lbd.md) -->

<span data-ttu-id="1dfa9-217">**定義されたワークロード** タブで、**ワークロードの作成** ボタンを使用して、倉庫管理または製造実行ワークロードをスケール ユニットの 1 つに追加します。</span><span class="sxs-lookup"><span data-stu-id="1dfa9-217">On the **Defined workloads** tab, use the **Create workload** button to add a warehouse management or manufacturing execution workload to one of your scale units.</span></span> <span data-ttu-id="1dfa9-218">各ワークロードに対して、ワークロードによって所有されるプロセスのコンテキストを指定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="1dfa9-218">For each workload, you must specify the context of the processes that will be owned by the workload.</span></span> <span data-ttu-id="1dfa9-219">倉庫管理ワークロードの場合、コンテキストは特定のサイトおよび法人の特定の倉庫になります。</span><span class="sxs-lookup"><span data-stu-id="1dfa9-219">For warehouse management workloads, the context is a specific warehouse in a specific site and legal entity.</span></span> <span data-ttu-id="1dfa9-220">製造実行ワークロードの場合、そのコンテキストは法人内の特定のサイトです。</span><span class="sxs-lookup"><span data-stu-id="1dfa9-220">For manufacturing execution workloads, the context is a specific site in a legal entity.</span></span>

:::image type="content" source="media/cloud_edge-DefineWorkload.png" alt-text="ワークロードの作成":::

> [!IMPORTANT]
> <span data-ttu-id="1dfa9-222">プレビューのスケール ユニット マネージャー ポータルでは、割り当て後にスケール ユニットからワークロードを削除したり、割り当てが行われた後でハブからスケール ユニットを割り当て解除したりすることはできません。</span><span class="sxs-lookup"><span data-stu-id="1dfa9-222">The Scale Unit Manager portal in the preview doesn't let you remove workloads from scale units or unassign a scale unit from a hub after the assignment is made.</span></span> <span data-ttu-id="1dfa9-223">割り当てを削除する必要がある場合は、連絡担当者に連絡して、プレビュー プログラムの管理を依頼してください。</span><span class="sxs-lookup"><span data-stu-id="1dfa9-223">If you must remove an assignment, reach out to your contact person for preview program management.</span></span>

<!-- ### Create an edge scale unit using your custom on-premises hardware appliance

In the public preview, you can create on-premises edge scale units on your custom hardware using the LBD environments. For details, see [Deploy custom edge scale units on custom hardware using LBD](cloud-edge-edge-scale-units-lbd.md). -->


[!INCLUDE[footer-include](../../includes/footer-banner.md)]