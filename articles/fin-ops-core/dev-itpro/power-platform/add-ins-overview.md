---
title: アドインの概要
description: このトピックでは、Finance and Operations アプリの機能を拡張するために使用できるアドインに関する情報を提供します。
author: ankugo
manager: AnnBe
ms.date: 05/20/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: IT Pro
ms.reviewer: sericks
ms.search.region: Global
ms.author: ankugo
ms.search.validFrom: 2021-02-28
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: 2fc191f3506e9179932a58b3b20a8524fb0cf042
ms.sourcegitcommit: 365092f735310990e82516110141d42aaf04e654
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/27/2021
ms.locfileid: "6103644"
---
# <a name="add-ins-overview"></a><span data-ttu-id="d0d2d-103">アドインの概要</span><span class="sxs-lookup"><span data-stu-id="d0d2d-103">Add-ins overview</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="d0d2d-104">アドインを使用すると、Finance and Operations アプリの機能を拡張できます。</span><span class="sxs-lookup"><span data-stu-id="d0d2d-104">Add-ins provide a way to extend the functionality of Finance and Operations apps.</span></span> <span data-ttu-id="d0d2d-105">すべてのアドインは、Microsoft Dynamics Lifecycle Services (LCS) のサンドボックスおよび運用環境の環境詳細ページを介してインストールされ、管理されます。</span><span class="sxs-lookup"><span data-stu-id="d0d2d-105">All add-ins are installed and managed via the environment details page for sandbox and production environments in Microsoft Dynamics Lifecycle Services (LCS).</span></span> <span data-ttu-id="d0d2d-106">アーキテクチャおよび機能のロック解除方法については、[Finance and Operations との Microsoft Power Platform 統合](overview.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="d0d2d-106">For more information about the architecture and how to unlock this feature, see [Microsoft Power Platform integration with Finance and Operations apps](overview.md).</span></span>

## <a name="what-add-ins-are-available"></a><span data-ttu-id="d0d2d-107">どのアドインで使用できますか?</span><span class="sxs-lookup"><span data-stu-id="d0d2d-107">What add-ins are available?</span></span>

<span data-ttu-id="d0d2d-108">新しいアドインは、定期的に利用できます。</span><span class="sxs-lookup"><span data-stu-id="d0d2d-108">New add-ins are made available on a regular basis.</span></span> <span data-ttu-id="d0d2d-109">ここでは、現在使用できるアドインについて説明し、各詳細へのリンクを提供します。</span><span class="sxs-lookup"><span data-stu-id="d0d2d-109">This section describes the add-ins that are currently available and provides links to more information about each.</span></span>

### <a name="planning-optimization"></a><span data-ttu-id="d0d2d-110">計画の最適化</span><span class="sxs-lookup"><span data-stu-id="d0d2d-110">Planning Optimization</span></span>

<span data-ttu-id="d0d2d-111">Microsoft Dynamics 365 Supply Chain Management の計画の最適化アドインを使用すると、マスター プランの計算を、Dynamics 365 Supply Chain Management および関連する SQL データベース以外で行うことができます。</span><span class="sxs-lookup"><span data-stu-id="d0d2d-111">The Planning Optimization Add-in for Microsoft Dynamics 365 Supply Chain Management enables master planning calculation to occur outside Dynamics 365 Supply Chain Management and the related SQL database.</span></span> <span data-ttu-id="d0d2d-112">計画の最適化機能に関連する利点として、マスター プランの実行時にパフォーマンスが向上し、SQL データベースへの影響が最小限に抑えられます。</span><span class="sxs-lookup"><span data-stu-id="d0d2d-112">The benefits that are associated with the Planning Optimization functionality include improved performance and minimal impact on the SQL database during master planning runs.</span></span> <span data-ttu-id="d0d2d-113">簡単な計画の実行は、営業時間内でも可能です。</span><span class="sxs-lookup"><span data-stu-id="d0d2d-113">Quick planning runs can be done even during office hours.</span></span> <span data-ttu-id="d0d2d-114">したがって、プランナーは、需要またはパラメータの変更に直ちに対応できます。</span><span class="sxs-lookup"><span data-stu-id="d0d2d-114">Therefore, planners can immediately react to demand or parameter changes.</span></span> <span data-ttu-id="d0d2d-115">詳細については、[Planning Optimization 概要](../../../supply-chain/master-planning/planning-optimization/planning-optimization-overview.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="d0d2d-115">To learn more, see [Planning Optimization overview](../../../supply-chain/master-planning/planning-optimization/planning-optimization-overview.md).</span></span>

### <a name="inventory-visibility"></a><span data-ttu-id="d0d2d-116">在庫品目一覧</span><span class="sxs-lookup"><span data-stu-id="d0d2d-116">Inventory Visibility</span></span>

<span data-ttu-id="d0d2d-117">Inventory Visibility Add-in は、リアルタイムで手持在庫を追跡を可能とする、独立し拡張性の高いマイクロサービスです。</span><span class="sxs-lookup"><span data-stu-id="d0d2d-117">The Inventory Visibility Add-in is an independent and highly scalable microservice that enables real-time tracking of on-hand inventory.</span></span> <span data-ttu-id="d0d2d-118">そのため、在庫の可視性をグローバルに表示できます。</span><span class="sxs-lookup"><span data-stu-id="d0d2d-118">Therefore, it provides a global view of inventory visibility.</span></span> <span data-ttu-id="d0d2d-119">詳細については、[Inventory Visibility Add-in](../../../supply-chain/inventory/inventory-visibility.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="d0d2d-119">To learn more, see [Inventory Visibility Add-in](../../../supply-chain/inventory/inventory-visibility.md).</span></span>

### <a name="export-to-azure-data-lake"></a><span data-ttu-id="d0d2d-120">Azure Data Lake へのエクスポート</span><span class="sxs-lookup"><span data-stu-id="d0d2d-120">Export to Azure Data Lake</span></span>

<span data-ttu-id="d0d2d-121">Azure Data Lake へのエクスポート機能は、Finance and Operations アプリ データを Azure Data Lake へエクスポートし、データを最新の状態に維持するマイクロサービスに基づきます。</span><span class="sxs-lookup"><span data-stu-id="d0d2d-121">The Export to Azure Data Lake feature is based on a microservice that exports Finance and Operations app data to Azure Data Lake and keeps the data fresh.</span></span> <span data-ttu-id="d0d2d-122">詳細については、[Azure Data Lake へのエキスポートの構成](../data-entities/configure-export-data-lake.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="d0d2d-122">To learn more, see [Configure export to Azure Data Lake](../data-entities/configure-export-data-lake.md).</span></span>

### <a name="iot-intelligence"></a><span data-ttu-id="d0d2d-123">IoT インテリジェンス</span><span class="sxs-lookup"><span data-stu-id="d0d2d-123">IoT Intelligence</span></span>

<span data-ttu-id="d0d2d-124">IoT インテリジェンスは、Supply Chain Management のアドインです。</span><span class="sxs-lookup"><span data-stu-id="d0d2d-124">IoT Intelligence is an add-in for Supply Chain Management.</span></span> <span data-ttu-id="d0d2d-125">また、モノのインターネット (Internet of Things: IoT) の信号を Supply Chain Management のデータと統合し、実用的な分析情報を生み出します。</span><span class="sxs-lookup"><span data-stu-id="d0d2d-125">It integrates Internet of Things (IoT) signals with data in Supply Chain Management to produce actionable insights.</span></span> <span data-ttu-id="d0d2d-126">詳細については、[IoT インテリジェンスのホーム ページ](../../../supply-chain/iot/iot-intelligence-home-page.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="d0d2d-126">To learn more, see [IoT Intelligence home page](../../../supply-chain/iot/iot-intelligence-home-page.md).</span></span>

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
