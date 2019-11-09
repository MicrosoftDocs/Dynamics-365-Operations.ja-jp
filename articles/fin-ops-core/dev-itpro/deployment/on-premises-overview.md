---
title: オンプレミス配置の概要
description: Dynamics 365 Finance + Operations (オンプレミス) は、顧客データ センターでビジネス プロセスを実行することをサポートします。
author: kfend
manager: AnnBe
ms.date: 09/18/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Developer, IT Pro
ms.reviewer: sericks
ms.search.scope: Operations
ms.custom: 60373
ms.assetid: ''
ms.search.region: Global
ms.author: arifk
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: Platform Update 8
ms.openlocfilehash: c18c048f5409a160c4f29c30b0ea4d982b958a9f
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/27/2019
ms.locfileid: "2183387"
---
# <a name="on-premises-deployment-overview"></a><span data-ttu-id="7a768-103">オンプレミス配置の概要</span><span class="sxs-lookup"><span data-stu-id="7a768-103">On-premises deployment overview</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="7a768-104">Microsoft Dynamics 365 Finance + Operations (オンプレミス) は、顧客データ センターでビジネス プロセスを実行することをサポートします。</span><span class="sxs-lookup"><span data-stu-id="7a768-104">Microsoft Dynamics 365 Finance + Operations (on-premises) supports running business processes in customer data centers.</span></span> <span data-ttu-id="7a768-105">この配置オプションでは、アプリケーション サーバーおよび Microsoft SQL Server データベースは顧客のデータ センター内で実行されます。</span><span class="sxs-lookup"><span data-stu-id="7a768-105">With this deployment option, application servers and the Microsoft SQL Server database will run in the customer’s data center.</span></span> <span data-ttu-id="7a768-106">顧客およびパートナーは、Microsoft Dynamics Lifecycle Services (LCS) を利用して、社内展開を管理します。</span><span class="sxs-lookup"><span data-stu-id="7a768-106">Customers and partners will utilize Microsoft Dynamics Lifecycle Services (LCS) to manage their on-premises deployments.</span></span> <span data-ttu-id="7a768-107">LCS は、クラウドおよびオンプレミスでの実装のアプリケーション ライフサイクルを管理するためのツールおよびサービスを提供するアプリケーション管理ポータルです。</span><span class="sxs-lookup"><span data-stu-id="7a768-107">LCS is an application management portal that provides tools and services for managing the application lifecycle of your implementations in the cloud and on-premises.</span></span> <span data-ttu-id="7a768-108">業務プロセス モデリング、ソフトウェアの展開および修正、監視および診断などの LCS の機能は、オンプレミス配置をサポートするために使用されます。</span><span class="sxs-lookup"><span data-stu-id="7a768-108">LCS features, such as business process modeling, software deployment and patching, and monitoring and diagnostics, are used to help support on-premises deployments.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="7a768-109">Dynamics 365 Finance + Operations (オンプレミス) は、Azure を含む、任意のパブリック クラウド インフラストラクチャでサポートされていません。</span><span class="sxs-lookup"><span data-stu-id="7a768-109">Dynamics 365 Finance + Operations (on-premises) is not supported on any public cloud infrastructure, including Azure.</span></span> 

## <a name="architecture"></a><span data-ttu-id="7a768-110">アーキテクチャ</span><span class="sxs-lookup"><span data-stu-id="7a768-110">Architecture</span></span> 

<span data-ttu-id="7a768-111">オンプレミス配置オプションは、Microsoft Azure Server Service Fabric スタンドアロン クラスターを使用して、オンプレミスで実行されるクラウド コンポーネントを使用します。</span><span class="sxs-lookup"><span data-stu-id="7a768-111">The on-premises deployment option uses cloud components running on-premises using Microsoft Azure Server Service Fabric standalone clusters.</span></span> <span data-ttu-id="7a768-112">Service Fabric は、企業規模の大規模なアプリケーションを構築および管理するための次世代の Microsoft ミドルウェア プラットフォームです。</span><span class="sxs-lookup"><span data-stu-id="7a768-112">Service Fabric is the next-generation Microsoft middleware platform for building and managing enterprise-class high-scale applications.</span></span> <span data-ttu-id="7a768-113">Service Fabric スタンドアロン クラスターは、Windows Server を実行しているどのコンピューターにも展開することができます。</span><span class="sxs-lookup"><span data-stu-id="7a768-113">Service Fabric standalone clusters can be deployed on any computer that is running Windows Server.</span></span> 

<span data-ttu-id="7a768-114">オンプレミスの設置では、製造環境用クラスターとサンドボックス環境用クラスターの2つのタイプの Service Fabric スタンドアロン クラスターを定義します。</span><span class="sxs-lookup"><span data-stu-id="7a768-114">On-premises deployment defines two types of Service Fabric standalone clusters: clusters for production environments and clusters for sandbox environments.</span></span> <span data-ttu-id="7a768-115">両方のタイプのクラスターに、次のロールまたはノード タイプが配置されます。</span><span class="sxs-lookup"><span data-stu-id="7a768-115">The following roles or node types are deployed into both types of clusters:</span></span> 

- <span data-ttu-id="7a768-116">Application Object Servers (AOS) – アプリケーション機能をクライアント、バッチ、およびインポート/エクスポートのシナリオで実行する機能を提供します。</span><span class="sxs-lookup"><span data-stu-id="7a768-116">Application Object Servers (AOS) – Provides the ability to run the application functionality in client, batch, and import/export scenarios.</span></span> 
- <span data-ttu-id="7a768-117">Management Reporter (MR) – 財務レポートの機能を提供します。</span><span class="sxs-lookup"><span data-stu-id="7a768-117">Management Reporter (MR) – Provides financial reporting functionality.</span></span> 
- <span data-ttu-id="7a768-118">SQL Server Reporting Services (SSRS): ドキュメント レポート機能を提供します。</span><span class="sxs-lookup"><span data-stu-id="7a768-118">SQL Server Reporting Services (SSRS) – Provides document reporting functionality.</span></span> 
- <span data-ttu-id="7a768-119">環境オーケストレータ – LCS からオンプレミス環境管理を有効にします。</span><span class="sxs-lookup"><span data-stu-id="7a768-119">Environment Orchestrator – Enables on-premises environment management from LCS.</span></span> 

<span data-ttu-id="7a768-120">図 1 は、Service Fabric スタンドアロン クラスターで配置されるノード タイプの論理的な図を示します。</span><span class="sxs-lookup"><span data-stu-id="7a768-120">Figure 1 shows a logical diagram of the node types deployed in a Service Fabric standalone cluster.</span></span> 

<span data-ttu-id="7a768-121">[![Service fabric スタンドアロン クラスター](./media/on-premises-overview-01.png)](./media/on-premises-overview-01.png)</span><span class="sxs-lookup"><span data-stu-id="7a768-121">[![Service fabric standalone cluster](./media/on-premises-overview-01.png)](./media/on-premises-overview-01.png)</span></span>

<span data-ttu-id="7a768-122">オンプレミス配置のアプリケーション ライフサイクル管理は、LCS を通じて調整されます。</span><span class="sxs-lookup"><span data-stu-id="7a768-122">Application lifecycle management for on-premises deployments is orchestrated through LCS.</span></span> <span data-ttu-id="7a768-123">顧客は、LCS の実績のあるツールと方法を使用して、社内展開を管理することができます (図2)。</span><span class="sxs-lookup"><span data-stu-id="7a768-123">Customers can use the proven tools and methodologies in LCS to help manage their on-premises deployments (Figure 2).</span></span> <span data-ttu-id="7a768-124">開発経験は、1 ボックス VHD によるクラウド配置と同じです。</span><span class="sxs-lookup"><span data-stu-id="7a768-124">The development experience continues to be the same as in cloud deployments through 1-box VHDs.</span></span> 

<span data-ttu-id="7a768-125">[![ローカル ビジネス データ展開のアプリケーション ライフ サイクル管理](./media/on-premises-overview-02.png)](./media/on-premises-overview-02.png)</span><span class="sxs-lookup"><span data-stu-id="7a768-125">[![Application lifecycle management for Local Business Data deployments](./media/on-premises-overview-02.png)](./media/on-premises-overview-02.png)</span></span>

## <a name="data-storage"></a><span data-ttu-id="7a768-126">データ ストレージ</span><span class="sxs-lookup"><span data-stu-id="7a768-126">Data storage</span></span> 
<span data-ttu-id="7a768-127">オンプレミス配置オプションは、オンプレミスのコア顧客データを格納します。</span><span class="sxs-lookup"><span data-stu-id="7a768-127">The on-premises deployment option stores core customer data on-premises.</span></span> <span data-ttu-id="7a768-128">コア顧客データは、[Microsoft Trust Center](https://www.microsoft.com/trustcenter/privacy/how-microsoft-defines-customer-data) で提供される顧客データ定義のサブセットです。</span><span class="sxs-lookup"><span data-stu-id="7a768-128">Core customer data is a subset of the customer data definition provided in the [Microsoft Trust Center](https://www.microsoft.com/trustcenter/privacy/how-microsoft-defines-customer-data).</span></span> <span data-ttu-id="7a768-129">表 1 では、LCS、Azure Active Directory、および Microsoft Office のサインアップ ポータルなどのサービスにより、米国内にある Microsoft Azure データ センターに格納されている顧客データのカテゴリについて説明します。</span><span class="sxs-lookup"><span data-stu-id="7a768-129">Table 1 outlines the categories of customer data that are stored in Microsoft Azure data centers located in the United States by services such as LCS, Azure Active Directory, and Microsoft Office signup portal.</span></span> <span data-ttu-id="7a768-130">コア顧客データと呼ばれる他のすべての顧客データは、オンプレミスに保管されます。</span><span class="sxs-lookup"><span data-stu-id="7a768-130">All other customer data, referred to as core customer data, is stored on-premises.</span></span>  

<span data-ttu-id="7a768-131">表 1: オンプレミス環境をサポートするサービスによって、米国内にある Microsoft Azure データ センターに格納されている顧客データ。</span><span class="sxs-lookup"><span data-stu-id="7a768-131">Table 1: Customer data stored in Microsoft Azure data centers located in the United States by services supporting on-premises environments.</span></span> <span data-ttu-id="7a768-132">これらのサービスにより、サポート インシデントの初期オンボーディング、開始、追跡、サービスの更新とアップグレードが可能になります。</span><span class="sxs-lookup"><span data-stu-id="7a768-132">These services enable initial onboarding, initiation, and tracking of support incidents, and service updates and upgrades.</span></span>  


| <span data-ttu-id="7a768-133">サポート サービス</span><span class="sxs-lookup"><span data-stu-id="7a768-133">Supporting services</span></span>                   | <span data-ttu-id="7a768-134">顧客データの定義</span><span class="sxs-lookup"><span data-stu-id="7a768-134">Customer data definition</span></span>                                                                                                                                                                                                                                                            |
|---------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7a768-135">Microsoft Dynamics Lifecycle Services</span><span class="sxs-lookup"><span data-stu-id="7a768-135">Microsoft Dynamics Lifecycle Services</span></span> | <span data-ttu-id="7a768-136">プロジェクトには、プロジェクトのコンテンツおよびファイルが格納されます。</span><span class="sxs-lookup"><span data-stu-id="7a768-136">Project content and files are stored in a project.</span></span> <span data-ttu-id="7a768-137">これには、アプリケーション構成データ、コード、メタデータ、アプリケーションやビジネス プロセス モデルを構成するデータ アセットが含まれます。</span><span class="sxs-lookup"><span data-stu-id="7a768-137">This includes application configuration data, code, metadata, and data assets that comprise the application and business process models.</span></span> <span data-ttu-id="7a768-138">匿名化されたユーザー活動ログおよびオンボーディング プロセス中に収集された情報に含まれます。</span><span class="sxs-lookup"><span data-stu-id="7a768-138">Also included is anonymized user activity logs and information that is collected during the onboarding process.</span></span> |
| <span data-ttu-id="7a768-139">Microsoft Office サインアップ ポータル</span><span class="sxs-lookup"><span data-stu-id="7a768-139">Microsoft Office signup portal</span></span>        | <span data-ttu-id="7a768-140">オンボード プロセス中に収集された顧客情報。</span><span class="sxs-lookup"><span data-stu-id="7a768-140">Customer information that is collected during the onboarding process.</span></span>                                                                                                                                                                                                                                 |
| <span data-ttu-id="7a768-141">Microsoft Azure Active Directory</span><span class="sxs-lookup"><span data-stu-id="7a768-141">Microsoft Azure Active Directory</span></span>      | <span data-ttu-id="7a768-142">LCS と Azure DevOps の認証。</span><span class="sxs-lookup"><span data-stu-id="7a768-142">Authentication for LCS and Azure DevOps.</span></span>                                                                                                                                                                                                               |
  

<span data-ttu-id="7a768-143">追加のサービスまたはコンポーネントは、必要に応じてオンプレミス配置を拡張するためにコンフィギュレーションすることができます。ただし、コンフィギュレーションの選択により、コア顧客データが顧客データ センターの外部に転送される可能性があります。</span><span class="sxs-lookup"><span data-stu-id="7a768-143">Additional services or components can be configured to extend an on-premises deployment as needed; however, configuration choices may cause core customer data to be transferred outside of the customer’s data center.</span></span> <span data-ttu-id="7a768-144">たとえば、オンプレミス配置の外部サービスを統合するために使用されるデータ管理機能のコンフィギュレーションにより、オンプレミス配置外のコア顧客データが転送される可能性があります。</span><span class="sxs-lookup"><span data-stu-id="7a768-144">For example, configuring data management features that are used to integrate external services with an on-premises deployment may result in the transfer of core customer data outside the on-premises deployment.</span></span> 