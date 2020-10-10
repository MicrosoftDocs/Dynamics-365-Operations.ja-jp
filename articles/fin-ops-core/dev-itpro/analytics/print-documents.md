---
title: ドキュメントの印刷の概要
description: ローカル プリンターまたはネットワークに接続されたデバイスのいずれかを使用してドキュメントを印刷できます。 この記事では、ドキュメントの印刷方法の概要を提供します。
author: TJVass
manager: AnnBe
ms.date: 07/25/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: IT Pro, Application User
ms.reviewer: kfend
ms.search.scope: Operations, Core
ms.custom: 69161
ms.assetid: 7815bddd-c4f4-4bc3-a29b-315458065374
ms.search.region: Global
ms.author: tjvass
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 25996cbccf3e9eec6fc29b80b8241e89b5b6b4a5
ms.sourcegitcommit: 71ec2f48185b8104ca52ff70df52263ce5f87f26
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/25/2020
ms.locfileid: "3893282"
---
# <a name="document-printing-overview"></a><span data-ttu-id="57608-104">ドキュメントの印刷の概要</span><span class="sxs-lookup"><span data-stu-id="57608-104">Document printing overview</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="57608-105">ローカル プリンターまたはネットワークに接続されたデバイスのいずれかを使用してドキュメントを印刷できます。</span><span class="sxs-lookup"><span data-stu-id="57608-105">You can print documents by using either a local printer or a network-connected device.</span></span> <span data-ttu-id="57608-106">この記事では、ドキュメントの印刷方法の概要を提供します。</span><span class="sxs-lookup"><span data-stu-id="57608-106">This article provides an overview of how documents are printed.</span></span>

## <a name="printing-overview"></a><span data-ttu-id="57608-107">印刷の概要</span><span class="sxs-lookup"><span data-stu-id="57608-107">Printing overview</span></span>

<span data-ttu-id="57608-108">アプリケーションは、事業活動をサポートするドキュメントの生成、保存、配布を簡単にする統合サービスおよびクライアント アプリケーションを提供します。</span><span class="sxs-lookup"><span data-stu-id="57608-108">The application provides integrated services and client applications that make it easy to generate, store, and distribute documents that support business activity.</span></span> <span data-ttu-id="57608-109">ローカル プリンターまたはネットワークに接続されたデバイスのいずれかを使用してドキュメントを印刷できます。</span><span class="sxs-lookup"><span data-stu-id="57608-109">You can print documents by using either a local printer or a network-connected device.</span></span> <span data-ttu-id="57608-110">さらに、PDF ファイルまたは Microsoft Office ドキュメントとして、ページおよびクライアントから直接レポートをエクスポートできます。</span><span class="sxs-lookup"><span data-stu-id="57608-110">In addition, you can export pages and reports directly from the client, as PDF files or Microsoft Office documents.</span></span> <span data-ttu-id="57608-111">最後に、作業負荷の分散は、ネットワーク リソースを使用して、モバイル デバイスから直接ビジネス ドキュメントを印刷できるようにします。</span><span class="sxs-lookup"><span data-stu-id="57608-111">Finally, the distributed workload lets you print business documents directly from a mobile device by using network resources.</span></span> <span data-ttu-id="57608-112">印刷要件が異なる場合がありますが、すべての業界は通常アプリケーションを使用してビジネス ドキュメントのハード コピーを作成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="57608-112">Although printing requirements might vary, all industries typically must create hard copies of business documents by using the application.</span></span> <span data-ttu-id="57608-113">ホストされているアプリケーションからネットワーク デバイスでドキュメントを印刷すると、課題の一意のセットが表示されます。</span><span class="sxs-lookup"><span data-stu-id="57608-113">Printing documents on network devices from hosted applications presents a unique set of challenges.</span></span> <span data-ttu-id="57608-114">次にいくつか例を挙げます。</span><span class="sxs-lookup"><span data-stu-id="57608-114">Here are some examples:</span></span>

- <span data-ttu-id="57608-115">プリント ドライバーは、ユーザーのデバイスで使用できない場合があります。</span><span class="sxs-lookup"><span data-stu-id="57608-115">Print drivers might not be available on the user's device.</span></span>
- <span data-ttu-id="57608-116">ユーザーのデバイスは、会社のネットワークに接続していない可能性があります。</span><span class="sxs-lookup"><span data-stu-id="57608-116">The user's device might not be connected to the corporate network.</span></span>

<span data-ttu-id="57608-117">専用のホストを使用して簡単な手順に従うことにより、ユーザーがネットワーク デバイス上のビジネス アプリケーションから直接印刷できるように、システム管理者は配置をコンフィギュレーションすることができます。</span><span class="sxs-lookup"><span data-stu-id="57608-117">By using a dedicated host and following a few easy steps, system administrators can configure deployments so that users can print directly from business applications on network devices.</span></span>

### <a name="application-printing-scenarios"></a><span data-ttu-id="57608-118">アプリケーション印刷のシナリオ</span><span class="sxs-lookup"><span data-stu-id="57608-118">Application printing scenarios</span></span> 

<span data-ttu-id="57608-119">次の表では、3つの主要な印刷シナリオについて説明します。</span><span class="sxs-lookup"><span data-stu-id="57608-119">The following table describes the three primary printing scenarios.</span></span>

| <span data-ttu-id="57608-120">シナリオ</span><span class="sxs-lookup"><span data-stu-id="57608-120">Scenario</span></span>                        | <span data-ttu-id="57608-121">目標</span><span class="sxs-lookup"><span data-stu-id="57608-121">Goal</span></span>                                                      | <span data-ttu-id="57608-122">ソリューション</span><span class="sxs-lookup"><span data-stu-id="57608-122">Solution</span></span> |
|---------------------------------|-----------------------------------------------------------|----------|
| <span data-ttu-id="57608-123">1. 表示される内容の印刷</span><span class="sxs-lookup"><span data-stu-id="57608-123">1. Printing what you see</span></span>        | <span data-ttu-id="57608-124">現在ブラウザに表示されている内容を印刷します。</span><span class="sxs-lookup"><span data-stu-id="57608-124">Print what is currently shown in the browser.</span></span>             | <span data-ttu-id="57608-125">Web ページの「プリント フレンドリー」バージョンがブラウザーで生成されます。</span><span class="sxs-lookup"><span data-stu-id="57608-125">A "print-friendly" version of the webpage is generated for the browser.</span></span> |
| <span data-ttu-id="57608-126">2. 対話型の印刷</span><span class="sxs-lookup"><span data-stu-id="57608-126">2. Interactive printing</span></span>         | <span data-ttu-id="57608-127">ローカルに接続されたデバイスで正確なドキュメントを印刷します。</span><span class="sxs-lookup"><span data-stu-id="57608-127">Print a precision document on a locally connected device.</span></span> | <span data-ttu-id="57608-128">レポートの PDF 形式をエクスポートし、ブラウザーにダウンロードできます。</span><span class="sxs-lookup"><span data-stu-id="57608-128">You can export a PDF version of the report and download it to the browser.</span></span> |
| <span data-ttu-id="57608-129">3. ネットワーク デバイスで印刷</span><span class="sxs-lookup"><span data-stu-id="57608-129">3. Printing on a network device</span></span> | <span data-ttu-id="57608-130">ドメイン プリンター デバイスに正確なドキュメントを送信します。</span><span class="sxs-lookup"><span data-stu-id="57608-130">Send a precision document to a domain printer device.</span></span>     | <span data-ttu-id="57608-131">正確なドキュメントは、顧客のドメイン内でホストされるサーバーで実行するクライアント アプリケーションに送信されます。</span><span class="sxs-lookup"><span data-stu-id="57608-131">A precision document is sent to a client application that runs on a server that is hosted in the customer's domain.</span></span> |

<span data-ttu-id="57608-132">シナリオによってソリューションが異なるため、アプリケーションは組み込みサービスおよびユーザーがその目標を達成するのためのツールを提供します。</span><span class="sxs-lookup"><span data-stu-id="57608-132">Because the solution varies, depending on the scenario, applications provide built-in services and tooling to help users accomplish their goals:</span></span>

- <span data-ttu-id="57608-133">**シナリオ 1** は HTML5 クライアントのブラウザーの表示によってサポートされています。</span><span class="sxs-lookup"><span data-stu-id="57608-133">**Scenario 1** is supported by the browser's rendering of the HTML5 client.</span></span>
- <span data-ttu-id="57608-134">**シナリオ 2** は、クライアント アプリケーションおよび Microsoft 365 サービスを使用します。</span><span class="sxs-lookup"><span data-stu-id="57608-134">**Scenario 2** uses client applications and Microsoft 365 services.</span></span>
- <span data-ttu-id="57608-135">**シナリオ 3** には、クライアント アプリケーションからおよび Microsoft Azure でホストされているサービスからのサポートが必要です。</span><span class="sxs-lookup"><span data-stu-id="57608-135">**Scenario 3** requires support from client applications and from services that are hosted in Microsoft Azure.</span></span>

<span data-ttu-id="57608-136">Azure サブスクリプションに配置されているプラットフォームに加えて、Finance and Operations アプリケーションは顧客に、統合された、ドキュメントを印刷するためドメインでホストされるデバイスをより使いやすくするファースト パーティ Azure アプリケーションを提供します。</span><span class="sxs-lookup"><span data-stu-id="57608-136">In addition to the platform that is deployed to the Azure subscription, Finance and Operations applications provide customers with an integrated, first-party Azure application that helps them more easily use domain-hosted devices to print documents.</span></span>

## <a name="service-overview"></a><span data-ttu-id="57608-137">サービスの概要</span><span class="sxs-lookup"><span data-stu-id="57608-137">Service overview</span></span>
<span data-ttu-id="57608-138">ホストされるアプリケーションによって生成されるドキュメントが、ネットワークに接続されたデバイスで印刷されるのを待機している間に、Azure BLOB ストレージに保存されます。</span><span class="sxs-lookup"><span data-stu-id="57608-138">While documents that are produced by the hosted applications are waiting to be printed on a network-connected device, they are stored in Azure blob storage.</span></span> <span data-ttu-id="57608-139">[ネットワーク印刷を有効にするため、ドキュメント回覧エージェントをインストールする](install-document-routing-agent.md) は Azure 認証を使用して、Azure サービスへのセキュリティで保護されたチャネルを確立します。</span><span class="sxs-lookup"><span data-stu-id="57608-139">The [Install the Document Routing Agent to enable network printing](install-document-routing-agent.md) uses Azure authentication to establish a secure channel to the Azure services.</span></span>

<span data-ttu-id="57608-140">**実行順序**</span><span class="sxs-lookup"><span data-stu-id="57608-140">**Execution sequence**</span></span>

1. <span data-ttu-id="57608-141">レポートは Microsoft SQL Server Reporting Services (SSRS) によって生成され、Azure BLOB ストレージに保存されます。</span><span class="sxs-lookup"><span data-stu-id="57608-141">The report is generated by Microsoft SQL Server Reporting Services (SSRS) and stored in Azure blob storage.</span></span> <span data-ttu-id="57608-142">関連付けられているプリンター設定は、ドキュメントと共に保存されます。</span><span class="sxs-lookup"><span data-stu-id="57608-142">Attached printer settings are stored together with the document.</span></span>
2. <span data-ttu-id="57608-143">ドキュメント回覧エージェントは、有効なジョブの Azure サービス バス キューを問い合わせます。</span><span class="sxs-lookup"><span data-stu-id="57608-143">The Document Routing Agent queries the Azure Service Bus queue for active jobs.</span></span>
3. <span data-ttu-id="57608-144">ドキュメントがドキュメント回覧エージェントによってダウンロードされ、そのネットワーク プリンターにスプールされます。</span><span class="sxs-lookup"><span data-stu-id="57608-144">The document is downloaded by the Document Routing Agent and spooled to the network printer.</span></span>

<span data-ttu-id="57608-145">クライアント ベースのソリューションは、顧客が印刷ニーズに合わせてスケールを管理できるようにします。</span><span class="sxs-lookup"><span data-stu-id="57608-145">The client-based solution lets customers manage the scale of their printing needs.</span></span> <span data-ttu-id="57608-146">重いボリュームの印刷作業負荷を持つ顧客は、多くのドキュメント回覧エージェントをインストールして、同時印刷操作の数を増やすことができます。</span><span class="sxs-lookup"><span data-stu-id="57608-146">Customers who have heavy-volume printing workloads can install many Document Routing Agents to increase the number of concurrent printing operations.</span></span> <span data-ttu-id="57608-147">または、一部の顧客は、予想される印刷ニーズに対応するため、ドキュメント回覧エージェントの極めて少ないインストールを必要とします。</span><span class="sxs-lookup"><span data-stu-id="57608-147">Alternatively, some customers require very few installations of the Document Routing Agent to handle their anticipated printing needs.</span></span>

### <a name="service-components-for-network-printing"></a><span data-ttu-id="57608-148">ネットワーク印刷のサービス コンポーネント</span><span class="sxs-lookup"><span data-stu-id="57608-148">Service components for network printing</span></span>

<span data-ttu-id="57608-149">次の図は、ネットワーク印刷操作のサポートに役立つ基本的なコンポーネントを示します。</span><span class="sxs-lookup"><span data-stu-id="57608-149">The following diagram shows the basic components that help support network printing operations.</span></span>

<span data-ttu-id="57608-150">[![service-components-for-network-printing\_2016](./media/service-components-for-network-printing_2016.png)](./media/service-components-for-network-printing_2016.png)</span><span class="sxs-lookup"><span data-stu-id="57608-150">[![service-components-for-network-printing\_2016](./media/service-components-for-network-printing_2016.png)](./media/service-components-for-network-printing_2016.png)</span></span>

<span data-ttu-id="57608-151">複数のドキュメント回覧エージェントを使用して単一のプリンターを登録できることに注意してください。</span><span class="sxs-lookup"><span data-stu-id="57608-151">Note that a single printer can be registered with multiple Document Routing Agents.</span></span> <span data-ttu-id="57608-152">プリンターの基本設定を解決するため、ホストされているサービスは、すべてのネットワーク プリンターを一意に識別するネットワーク パスを使用します。</span><span class="sxs-lookup"><span data-stu-id="57608-152">To resolve the printer preferences, the hosted service uses the network path that uniquely identifies every network printer.</span></span> <span data-ttu-id="57608-153">その結果、プリンターが複数のクライアントにより登録されている場合でも、アプリケーションで使用可能なプリンターの一覧で単一の選択として表示されます。</span><span class="sxs-lookup"><span data-stu-id="57608-153">As a result, even when a printer is registered by multiple clients, it appears as a single selection in the list of printers available in applications.</span></span>
