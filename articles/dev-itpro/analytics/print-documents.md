---
title: "Finance and Operations アプリケーションでの印刷"
description: "Microsoft Dynamics 365 for Finance and Operations では、ローカル プリンターまたはネットワークに接続されたデバイスのいずれかを使用してドキュメントを印刷できます。 この記事では、ドキュメントの印刷方法の概要を提供します。"
author: TJVass
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: IT Pro, Application User
ms.reviewer: sericks
ms.search.scope: Operations, Core
ms.custom: 69161
ms.assetid: 7815bddd-c4f4-4bc3-a29b-315458065374
ms.search.region: Global
ms.author: tjvass
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: 30a418e6c49849369f0a0e3ffa28f31b9b88b7e7
ms.contentlocale: ja-jp
ms.lasthandoff: 04/13/2018

---

# <a name="printing-in-finance-and-operations-applications"></a><span data-ttu-id="91d63-104">Finance and Operations アプリケーションでの印刷</span><span class="sxs-lookup"><span data-stu-id="91d63-104">Printing in Finance and Operations applications</span></span>

[!INCLUDE [banner](../includes/banner.md)]

<span data-ttu-id="91d63-105">Microsoft Dynamics 365 for Finance and Operations では、ローカル プリンターまたはネットワークに接続されたデバイスのいずれかを使用してドキュメントを印刷できます。</span><span class="sxs-lookup"><span data-stu-id="91d63-105">In Microsoft Dynamics 365 for Finance and Operations, you can print documents by using either a local printer or a network-connected device.</span></span> <span data-ttu-id="91d63-106">この記事では、ドキュメントの印刷方法の概要を提供します。</span><span class="sxs-lookup"><span data-stu-id="91d63-106">This article provides an overview of how documents are printed.</span></span>

<a name="printing-overview"></a><span data-ttu-id="91d63-107">印刷の概要</span><span class="sxs-lookup"><span data-stu-id="91d63-107">Printing overview</span></span>
-----------------

<span data-ttu-id="91d63-108">Microsoft Dynamics 365 for Finance and Operations は、事業活動をサポートするドキュメントの生成、保存、配布を簡単にする統合サービスおよびクライアント アプリケーションを提供します。</span><span class="sxs-lookup"><span data-stu-id="91d63-108">Microsoft Dynamics 365 for Finance and Operations provides integrated services and client applications that make it easy to generate, store, and distribute documents that support business activity.</span></span> <span data-ttu-id="91d63-109">Finance and Operations では、ローカル プリンターまたはネットワークに接続されたデバイスのいずれかを使用してドキュメントを印刷できます。</span><span class="sxs-lookup"><span data-stu-id="91d63-109">In Finance and Operations, you can print documents by using either a local printer or a network-connected device.</span></span> <span data-ttu-id="91d63-110">さらに、PDF ファイルまたは Microsoft Office ドキュメントとして、 Finance and Operations ページおよびクライアントから直接レポートをエクスポートできます。</span><span class="sxs-lookup"><span data-stu-id="91d63-110">In addition, you can export Finance and Operations pages and reports directly from the client, as PDF files or Microsoft Office documents.</span></span> <span data-ttu-id="91d63-111">最後に、作業負荷の分散は、ネットワーク リソースを使用して、モバイル デバイスから直接ビジネス ドキュメントを印刷できるようにします。</span><span class="sxs-lookup"><span data-stu-id="91d63-111">Finally, the distributed workload lets you print business documents directly from a mobile device by using network resources.</span></span> <span data-ttu-id="91d63-112">印刷要件が異なる場合がありますが、すべての業界は通常 Finance and Operations を使用してビジネス ドキュメントのハード コピーを作成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="91d63-112">Although printing requirements might vary, all industries typically must create hard copies of business documents by using Finance and Operations.</span></span> <span data-ttu-id="91d63-113">ホストされているアプリケーションからネットワーク デバイスでドキュメントを印刷すると、課題の一意のセットが表示されます。</span><span class="sxs-lookup"><span data-stu-id="91d63-113">Printing documents on network devices from hosted applications presents a unique set of challenges.</span></span> <span data-ttu-id="91d63-114">次にいくつか例を挙げます。</span><span class="sxs-lookup"><span data-stu-id="91d63-114">Here are some examples:</span></span>

-   <span data-ttu-id="91d63-115">プリント ドライバーは、ユーザーのデバイスで使用できない場合があります。</span><span class="sxs-lookup"><span data-stu-id="91d63-115">Print drivers might not be available on the user's device.</span></span>
-   <span data-ttu-id="91d63-116">ユーザーのデバイスは、会社のネットワークに接続していない可能性があります。</span><span class="sxs-lookup"><span data-stu-id="91d63-116">The user’s device might not be connected to the corporate network.</span></span>

<span data-ttu-id="91d63-117">専用のホストを使用して簡単な手順に従うことにより、ユーザーがネットワーク デバイス上のビジネス アプリケーションから直接印刷できるように、システム管理者は配置をコンフィギュレーションすることができます。</span><span class="sxs-lookup"><span data-stu-id="91d63-117">By using a dedicated host and following a few easy steps, system administrators can configure deployments so that users can print directly from business applications on network devices.</span></span>

### <a name="printing-scenarios-in-finance-and-operations-applications"></a><span data-ttu-id="91d63-118">Finance and Operations アプリケーションでの印刷シナリオ</span><span class="sxs-lookup"><span data-stu-id="91d63-118">Printing scenarios in Finance and Operations applications</span></span>

<span data-ttu-id="91d63-119">次の表では、Finance and Operations アプリケーションでの、3 つの主な印刷シナリオについて説明します。</span><span class="sxs-lookup"><span data-stu-id="91d63-119">The following table describes the three primary printing scenarios in Finance and Operations applications.</span></span>

| <span data-ttu-id="91d63-120">シナリオ</span><span class="sxs-lookup"><span data-stu-id="91d63-120">Scenario</span></span>                        | <span data-ttu-id="91d63-121">目標</span><span class="sxs-lookup"><span data-stu-id="91d63-121">Goal</span></span>                                                      | <span data-ttu-id="91d63-122">ソリューション</span><span class="sxs-lookup"><span data-stu-id="91d63-122">Solution</span></span>                                                                                                            |
|---------------------------------|-----------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="91d63-123">1. 表示される内容の印刷</span><span class="sxs-lookup"><span data-stu-id="91d63-123">1. Printing what you see</span></span>        | <span data-ttu-id="91d63-124">現在ブラウザに表示されている内容を印刷します。</span><span class="sxs-lookup"><span data-stu-id="91d63-124">Print what is currently shown in the browser.</span></span>             | <span data-ttu-id="91d63-125">Web ページの「プリント フレンドリー」バージョンがブラウザーで生成されます。</span><span class="sxs-lookup"><span data-stu-id="91d63-125">A “print-friendly” version of the webpage is generated for the browser.</span></span>                                             |
| <span data-ttu-id="91d63-126">2. 対話型の印刷</span><span class="sxs-lookup"><span data-stu-id="91d63-126">2. Interactive printing</span></span>         | <span data-ttu-id="91d63-127">ローカルに接続されたデバイスで正確なドキュメントを印刷します。</span><span class="sxs-lookup"><span data-stu-id="91d63-127">Print a precision document on a locally connected device.</span></span> | <span data-ttu-id="91d63-128">レポートの PDF 形式をエクスポートし、ブラウザーにダウンロードできます。</span><span class="sxs-lookup"><span data-stu-id="91d63-128">You can export a PDF version of the report and download it to the browser.</span></span>                                          |
| <span data-ttu-id="91d63-129">3. ネットワーク デバイスで印刷</span><span class="sxs-lookup"><span data-stu-id="91d63-129">3. Printing on a network device</span></span> | <span data-ttu-id="91d63-130">ドメイン プリンター デバイスに正確なドキュメントを送信します。</span><span class="sxs-lookup"><span data-stu-id="91d63-130">Send a precision document to a domain printer device.</span></span>     | <span data-ttu-id="91d63-131">正確なドキュメントは、顧客のドメイン内でホストされるサーバーで実行するクライアント アプリケーションに送信されます。</span><span class="sxs-lookup"><span data-stu-id="91d63-131">A precision document is sent to a client application that runs on a server that is hosted in the customer’s domain.</span></span> |

<span data-ttu-id="91d63-132">シナリオによってソリューションが異なるため、Finance and Operations アプリケーションは組み込みサービスおよびユーザーがその目標を達成するのためのツールを提供します。</span><span class="sxs-lookup"><span data-stu-id="91d63-132">Because the solution varies, depending on the scenario, Finance and Operations applications provide built-in services and tooling to help users accomplish their goals:</span></span>

-   <span data-ttu-id="91d63-133">**シナリオ 1** は HTML5 クライアントのブラウザーの表示によってサポートされています。</span><span class="sxs-lookup"><span data-stu-id="91d63-133">**Scenario 1** is supported by the browser’s rendering of the HTML5 client.</span></span>
-   <span data-ttu-id="91d63-134">**シナリオ 2** はクライアント アプリケーションおよび Microsoft Office 365 サービスを使用します。</span><span class="sxs-lookup"><span data-stu-id="91d63-134">**Scenario 2** uses client applications and Microsoft Office 365 services.</span></span>
-   <span data-ttu-id="91d63-135">**シナリオ 3** には、クライアント アプリケーションからおよび Microsoft Azure でホストされているサービスからのサポートが必要です。</span><span class="sxs-lookup"><span data-stu-id="91d63-135">**Scenario 3** requires support from client applications and from services that are hosted in Microsoft Azure.</span></span>

<span data-ttu-id="91d63-136">Azure サブスクリプションに配置されているプラットフォームに加えて、Finance and Operations アプリケーションは顧客に、統合された、ドキュメントを印刷するためドメインでホストされるデバイスをより使いやすくする当事者 Azure アプリケーションを提供します。</span><span class="sxs-lookup"><span data-stu-id="91d63-136">In addition to the platform that is deployed to the Azure subscription, Finance and Operations applications provide customers with an integrated, first-party Azure application that helps them more easily use domain-hosted devices to print documents.</span></span>

## <a name="service-overview"></a><span data-ttu-id="91d63-137">サービスの概要</span><span class="sxs-lookup"><span data-stu-id="91d63-137">Service overview</span></span>
<span data-ttu-id="91d63-138">ホストされるアプリケーションによって生成されるドキュメントが、ネットワークに接続されたデバイスで印刷されるのを待機している間に、Azure BLOB ストレージに保存されます。</span><span class="sxs-lookup"><span data-stu-id="91d63-138">While documents that are produced by the hosted applications are waiting to be printed on a network-connected device, they are stored in Azure blob storage.</span></span> <span data-ttu-id="91d63-139">[ドキュメント回覧エージェント](install-document-routing-agent.md) は Azure 認証を使用して、Azure サービスへのセキュリティで保護されたチャネルを確立します。</span><span class="sxs-lookup"><span data-stu-id="91d63-139">The [Document Routing Agent](install-document-routing-agent.md) uses Azure authentication to establish a secure channel to the Azure services.</span></span> <span data-ttu-id="91d63-140">**実行順序**</span><span class="sxs-lookup"><span data-stu-id="91d63-140">**Execution sequence**</span></span>

1.  <span data-ttu-id="91d63-141">レポートは Microsoft SQL Server Reporting Services (SSRS) によって生成され、Azure BLOB ストレージに保存されます。</span><span class="sxs-lookup"><span data-stu-id="91d63-141">The report is generated by Microsoft SQL Server Reporting Services (SSRS) and stored in Azure blob storage.</span></span> <span data-ttu-id="91d63-142">関連付けられているプリンター設定は、ドキュメントと共に保存されます。</span><span class="sxs-lookup"><span data-stu-id="91d63-142">Attached printer settings are stored together with the document.</span></span>
2.  <span data-ttu-id="91d63-143">ドキュメント回覧エージェントは、有効なジョブの Azure サービス バス キューを問い合わせます。</span><span class="sxs-lookup"><span data-stu-id="91d63-143">The Document Routing Agent queries the Azure Service Bus queue for active jobs.</span></span>
3.  <span data-ttu-id="91d63-144">ドキュメントがドキュメント回覧エージェントによってダウンロードされ、そのネットワーク プリンターにスプールされます。</span><span class="sxs-lookup"><span data-stu-id="91d63-144">The document is downloaded by the Document Routing Agent and spooled to the network printer.</span></span>

<span data-ttu-id="91d63-145">クライアント ベースのソリューションは、顧客が印刷ニーズに合わせてスケールを管理できるようにします。</span><span class="sxs-lookup"><span data-stu-id="91d63-145">The client-based solution lets customers manage the scale of their printing needs.</span></span> <span data-ttu-id="91d63-146">重いボリュームの印刷作業負荷を持つ顧客は、多くのドキュメント回覧エージェントをインストールして、同時印刷操作の数を増やすことができます。</span><span class="sxs-lookup"><span data-stu-id="91d63-146">Customers who have heavy-volume printing workloads can install many Document Routing Agents to increase the number of concurrent printing operations.</span></span> <span data-ttu-id="91d63-147">または、一部の顧客は、予想される印刷ニーズに対応するため、ドキュメント回覧エージェントの極めて少ないインストールを必要とします。</span><span class="sxs-lookup"><span data-stu-id="91d63-147">Alternatively, some customers require very few installations of the Document Routing Agent to handle their anticipated printing needs.</span></span>

### <a name="service-components-for-network-printing"></a><span data-ttu-id="91d63-148">ネットワーク印刷のサービス コンポーネント</span><span class="sxs-lookup"><span data-stu-id="91d63-148">Service components for network printing</span></span>

<span data-ttu-id="91d63-149">次の図は、ネットワーク印刷操作のサポートに役立つ基本的なコンポーネントを示します。</span><span class="sxs-lookup"><span data-stu-id="91d63-149">The following diagram shows the basic components that help support network printing operations.</span></span> <span data-ttu-id="91d63-150">[![ネットワーク印刷のサービス コンポーネント\_2016](./media/service-components-for-network-printing_2016.png)](./media/service-components-for-network-printing_2016.png) 1 台のプリンターを複数のドキュメント回覧エージェントに登録できることに注意してください。</span><span class="sxs-lookup"><span data-stu-id="91d63-150">[![service-components-for-network-printing\_2016](./media/service-components-for-network-printing_2016.png)](./media/service-components-for-network-printing_2016.png) Note that a single printer can be registered with multiple Document Routing Agents.</span></span> <span data-ttu-id="91d63-151">プリンターの基本設定を解決するため、ホストされているサービスは、すべてのネットワーク プリンターを一意に識別するネットワーク パスを使用します。</span><span class="sxs-lookup"><span data-stu-id="91d63-151">To resolve the printer preferences, the hosted service uses the network path that uniquely identifies every network printer.</span></span> <span data-ttu-id="91d63-152">その結果、プリンターが複数のクライアントにより登録されている場合でも、Finance and Operations アプリケーションで使用可能なプリンターの一覧で単一の選択として表示されます。</span><span class="sxs-lookup"><span data-stu-id="91d63-152">As a result, even when a printer is registered by multiple clients, it appears as a single selection in the list of printers available in Finance and Operations applications.</span></span>




