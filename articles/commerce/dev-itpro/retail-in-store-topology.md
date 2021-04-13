---
title: ストア内トポロジを選択します。
description: このトピックでは、様々な Dynamics 365 Commerce の実店舗構成図を提供します。
author: rassadi
ms.date: 06/02/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: SysAADClientTable, RetailTransactionServiceProfile
audience: IT Pro
ms.reviewer: rhaertle
ms.custom: 44351
ms.search.region: Global
ms.author: jashanno
ms.search.validFrom: 2019-03-01
ms.openlocfilehash: 11d138e8cb1d08c2506593c55e787f462ae1b2a8
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/31/2021
ms.locfileid: "5797207"
---
# <a name="select-an-in-store-topology"></a><span data-ttu-id="ce5d3-103">ストア内トポロジを選択します。</span><span class="sxs-lookup"><span data-stu-id="ce5d3-103">Select an in-store topology</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="ce5d3-104">このトピックでは、様々な Dynamics 365 Commerce の実店舗構成図の概要を提供します。</span><span class="sxs-lookup"><span data-stu-id="ce5d3-104">This topic provides an overview of the various Dynamics 365 Commerce in-store topologies.</span></span> 

<span data-ttu-id="ce5d3-105"><a href="https://docs.microsoft.com/dynamics365/unified-operations/retail/dev-itpro/media/channel/instore/topology.jpg" rel="some text">![右側の店舗の構成図を選択する](media/CHANNEL/INSTORE/Topology.jpg)</a></span><span class="sxs-lookup"><span data-stu-id="ce5d3-105"><a href="https://docs.microsoft.com/dynamics365/unified-operations/retail/dev-itpro/media/channel/instore/topology.jpg" rel="some text">![Choose the right store topology](media/CHANNEL/INSTORE/Topology.jpg)</a></span></span>

## <a name="supported-capabilities-when-connectivity-is-lost"></a><span data-ttu-id="ce5d3-106">接続が失われたときにサポートしている機能</span><span class="sxs-lookup"><span data-stu-id="ce5d3-106">Supported capabilities when connectivity is lost</span></span>
| <span data-ttu-id="ce5d3-107">操作</span><span class="sxs-lookup"><span data-stu-id="ce5d3-107">Operation</span></span> | <span data-ttu-id="ce5d3-108">Commerce Scale Unit への接続がされていないとき</span><span class="sxs-lookup"><span data-stu-id="ce5d3-108">Without connectivity to Commerce Scale Unit</span></span><br><span data-ttu-id="ce5d3-109">MPOS オフライン モード</span><span class="sxs-lookup"><span data-stu-id="ce5d3-109">(in MPOS Offline Mode)</span></span> | <span data-ttu-id="ce5d3-110">本部への接続がされていないとき</span><span class="sxs-lookup"><span data-stu-id="ce5d3-110">Without connectivity to HQ</span></span><br><span data-ttu-id="ce5d3-111">(Commerce Scale Unit (自己ホスト))</span><span class="sxs-lookup"><span data-stu-id="ce5d3-111">(Commerce Scale Unit (self-hosted))</span></span> |
| --- | :-: | :-: |
| <span data-ttu-id="ce5d3-112">クロス ターミナル シフト (ビュー、中断、再開、切断など)</span><span class="sxs-lookup"><span data-stu-id="ce5d3-112">Cross terminal shifts (such as view, suspend, resume, close)</span></span> | | <span data-ttu-id="ce5d3-113">✔</span><span class="sxs-lookup"><span data-stu-id="ce5d3-113">✔</span></span> | 
| <span data-ttu-id="ce5d3-114">クロス ターミナル トランザクション (ビュー、中断、再開など)</span><span class="sxs-lookup"><span data-stu-id="ce5d3-114">Cross terminal transactions (such as view, suspend, resume)</span></span>  | | <span data-ttu-id="ce5d3-115">✔</span><span class="sxs-lookup"><span data-stu-id="ce5d3-115">✔</span></span> |

## <a name="supported-operations-when-connectivity-is-lost"></a><span data-ttu-id="ce5d3-116">接続が失われたときにサポートしている操作</span><span class="sxs-lookup"><span data-stu-id="ce5d3-116">Supported operations when connectivity is lost</span></span>
<span data-ttu-id="ce5d3-117">POSが本部との接続を失った場合にサポートしている宗さんの一覧については、 [オンラインおよびオフラインでの店頭(POS)操作](https://docs.microsoft.com/dynamics365/unified-operations/retail/pos-operations) 参照してください。。</span><span class="sxs-lookup"><span data-stu-id="ce5d3-117">For a list of operations that are supported when the POS loses connectivity to the HQ, see [Online and offline point of sale (POS) operations](https://docs.microsoft.com/dynamics365/unified-operations/retail/pos-operations).</span></span>

## <a name="supported-deployment-and-maintenance-capabilities"></a><span data-ttu-id="ce5d3-118">サポートされている導入及びメンテナンスの機能</span><span class="sxs-lookup"><span data-stu-id="ce5d3-118">Supported deployment and maintenance capabilities</span></span>
<span data-ttu-id="ce5d3-119">一括配置は Modern POS ではサポートされますが、Commerce Scale Unit ではサポートされません。</span><span class="sxs-lookup"><span data-stu-id="ce5d3-119">Mass deployment is supported in Modern POS, but not in Commerce Scale Unit.</span></span> <span data-ttu-id="ce5d3-120">詳細については、 [セルフサービス コンポーネントの一括配置](https://docs.microsoft.com/dynamics365/unified-operations/retail/dev-itpro/retail-mass-deployment) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="ce5d3-120">For more information, see [Mass deployment of self-service components](https://docs.microsoft.com/dynamics365/unified-operations/retail/dev-itpro/retail-mass-deployment).</span></span>

## <a name="deployed-components"></a><span data-ttu-id="ce5d3-121">配置可能なコンポーネント</span><span class="sxs-lookup"><span data-stu-id="ce5d3-121">Deployed components</span></span>
<span data-ttu-id="ce5d3-122">次に示すコンポーネントは、すべて1つのインストーラーを使って配置されます。</span><span class="sxs-lookup"><span data-stu-id="ce5d3-122">The following components are deployed through a single installer.</span></span> <span data-ttu-id="ce5d3-123">これらをそれぞれ個別でインストールする必要はありません。</span><span class="sxs-lookup"><span data-stu-id="ce5d3-123">This means that they do not need to be installed individually.</span></span>

### <a name="modern-pos"></a><span data-ttu-id="ce5d3-124">Modern POS</span><span class="sxs-lookup"><span data-stu-id="ce5d3-124">Modern POS</span></span>
| <span data-ttu-id="ce5d3-125">配置可能なコンポーネント</span><span class="sxs-lookup"><span data-stu-id="ce5d3-125">Deployed component</span></span> | <span data-ttu-id="ce5d3-126">コンポーネント タイプ</span><span class="sxs-lookup"><span data-stu-id="ce5d3-126">Component type</span></span> | <span data-ttu-id="ce5d3-127">摘要</span><span class="sxs-lookup"><span data-stu-id="ce5d3-127">Notes</span></span> |
| --- | --- | --- |
| <span data-ttu-id="ce5d3-128">最新のPOSアプリケーション</span><span class="sxs-lookup"><span data-stu-id="ce5d3-128">Modern POS App</span></span> | <span data-ttu-id="ce5d3-129">ユニバーサル Windows プラットフォーム アプリケーション</span><span class="sxs-lookup"><span data-stu-id="ce5d3-129">Universal Windows Platform (UWP) Application</span></span> | <span data-ttu-id="ce5d3-130">レジで稼働する最新のPOSアプリケーションです。</span><span class="sxs-lookup"><span data-stu-id="ce5d3-130">The Modern POS application running on the register.</span></span> |
| <span data-ttu-id="ce5d3-131">最新のPOS クライアント ブローカー</span><span class="sxs-lookup"><span data-stu-id="ce5d3-131">Modern POS Client Broker</span></span> | <span data-ttu-id="ce5d3-132">最新のPOSのネイティブ バイナリをホストしているCOM Surrogate</span><span class="sxs-lookup"><span data-stu-id="ce5d3-132">COM Surrogate hosting native binaries for the Modern POS</span></span> | <span data-ttu-id="ce5d3-133">オフラインモードでの操作の実行をサポートする Commerce Runtime を提供します。また、最新のPOSと本部とデータを同期するにはAsync Clientライブラリも同様に必要となります。</span><span class="sxs-lookup"><span data-stu-id="ce5d3-133">Hosts the Commerce Runtime to support operations to execute in offline mode as well as Async Client Libraries needed to synchronize data between the Modern POS and the HQ.</span></span> | 
| <span data-ttu-id="ce5d3-134">チャンネル データベース</span><span class="sxs-lookup"><span data-stu-id="ce5d3-134">Channel Database</span></span> | <span data-ttu-id="ce5d3-135">SQL データベース</span><span class="sxs-lookup"><span data-stu-id="ce5d3-135">SQL Database</span></span> | <span data-ttu-id="ce5d3-136">レジのデータを提供している特定のチャンネル データベース インスタンスを登録します。</span><span class="sxs-lookup"><span data-stu-id="ce5d3-136">Register specific Channel Database instance hosting data for the register.</span></span>

### <a name="commerce-scale-unit-self-hosted"></a><span data-ttu-id="ce5d3-137">Commerce Scale Unit (自己ホスト)</span><span class="sxs-lookup"><span data-stu-id="ce5d3-137">Commerce Scale Unit (self-hosted)</span></span>
| <span data-ttu-id="ce5d3-138">インストールされたコンポーネント</span><span class="sxs-lookup"><span data-stu-id="ce5d3-138">Installed component</span></span> | <span data-ttu-id="ce5d3-139">コンポーネント タイプ</span><span class="sxs-lookup"><span data-stu-id="ce5d3-139">Component type</span></span> | <span data-ttu-id="ce5d3-140">摘要</span><span class="sxs-lookup"><span data-stu-id="ce5d3-140">Notes</span></span> |
| --- | --- | --- |
| <span data-ttu-id="ce5d3-141">Commerce Scale Unit (自己ホスト)</span><span class="sxs-lookup"><span data-stu-id="ce5d3-141">Commerce Scale Unit (self-hosted)</span></span> | <span data-ttu-id="ce5d3-142">IIS Web サービス</span><span class="sxs-lookup"><span data-stu-id="ce5d3-142">IIS Web Service</span></span> | <span data-ttu-id="ce5d3-143">1 つ以上の店舗で使用する Commerce Scale Unit (自己ホスト) のインスタンスの単位を計測します。</span><span class="sxs-lookup"><span data-stu-id="ce5d3-143">Scale unit specific Commerce Scale Unit (self-hosted) instance used by one or more stores.</span></span> |
| <span data-ttu-id="ce5d3-144">チャンネル データベース</span><span class="sxs-lookup"><span data-stu-id="ce5d3-144">Channel Database</span></span> | <span data-ttu-id="ce5d3-145">SQL データベース</span><span class="sxs-lookup"><span data-stu-id="ce5d3-145">SQL Database</span></span> | <span data-ttu-id="ce5d3-146">1つ以上の店舗で使用するデータを提供する、特定のチャンネルデータベースインスタンスの店舗単位を計測します。</span><span class="sxs-lookup"><span data-stu-id="ce5d3-146">Scale unit specific Store specific Channel Database instance hosting data for one or more stores.</span></span> |
| <span data-ttu-id="ce5d3-147">Async Client サービス</span><span class="sxs-lookup"><span data-stu-id="ce5d3-147">Async Client Service</span></span> | <span data-ttu-id="ce5d3-148">Windows サービス</span><span class="sxs-lookup"><span data-stu-id="ce5d3-148">Windows Service</span></span> | <span data-ttu-id="ce5d3-149">マスター レコード データを本部から店舗へ、取引データを店舗から本部へと同期するためのコンポーネント</span><span class="sxs-lookup"><span data-stu-id="ce5d3-149">Component to synchronize master record data from the HQ to the store and transactional data from the store to the HQ.</span></span> |
| <span data-ttu-id="ce5d3-150">クラウド POS</span><span class="sxs-lookup"><span data-stu-id="ce5d3-150">Cloud POS</span></span> | <span data-ttu-id="ce5d3-151">IIS Web サービス</span><span class="sxs-lookup"><span data-stu-id="ce5d3-151">IIS Web Service</span></span> | <span data-ttu-id="ce5d3-152">Web ブラウザーを使用して POS 機能をホストするクラウド POS アプリケーション。</span><span class="sxs-lookup"><span data-stu-id="ce5d3-152">Cloud POS application that hosts POS functionality through a web browser.</span></span> |

## <a name="additional-resources"></a><span data-ttu-id="ce5d3-153">追加リソース</span><span class="sxs-lookup"><span data-stu-id="ce5d3-153">Additional resources</span></span>
### <a name="mpos-offline-mode"></a><span data-ttu-id="ce5d3-154">MPOS オフライン モード</span><span class="sxs-lookup"><span data-stu-id="ce5d3-154">MPOS offline mode</span></span>
<span data-ttu-id="ce5d3-155">MPOS オフラインモードの詳細については、以下を参照してください。</span><span class="sxs-lookup"><span data-stu-id="ce5d3-155">For more information about MPOS offline mode, see:</span></span>
- [<span data-ttu-id="ce5d3-156">オフライン販売時点管理 (POS) の機能</span><span class="sxs-lookup"><span data-stu-id="ce5d3-156">Offline point of sale (POS) functionality</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/retail/pos-offline-functionality)
- [<span data-ttu-id="ce5d3-157">オンラインおよびオフラインでの販売時点管理 (POS) の操作</span><span class="sxs-lookup"><span data-stu-id="ce5d3-157">Online and offline point of sale (POS) operations</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/retail/pos-operations)
- [<span data-ttu-id="ce5d3-158">セルフサービス コンポーネントの一括配置</span><span class="sxs-lookup"><span data-stu-id="ce5d3-158">Mass deployment of self-service components</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/retail/dev-itpro/retail-mass-deployment)

### <a name="commerce-scale-unit-self-hosted"></a><span data-ttu-id="ce5d3-159">Commerce Scale Unit (自己ホスト)</span><span class="sxs-lookup"><span data-stu-id="ce5d3-159">Commerce Scale Unit (self-hosted)</span></span>
<span data-ttu-id="ce5d3-160">Commerce Scale Unit (自己ホスト) は、実店舗などお客様の環境に配置することが可能な、バックオフィスや本部 (HQ) への通信が切断された場合でも継続して業務を行うことをサポートするコンポーネントです。</span><span class="sxs-lookup"><span data-stu-id="ce5d3-160">The Commerce Scale Unit (self-hosted) is a set of components that can be deployed in a customer environment, such as inside a store, that can support continuous operations if connectivity to the back office or headquarters (HQ) is lost.</span></span> 

<span data-ttu-id="ce5d3-161">詳細については、以下を参照してください。</span><span class="sxs-lookup"><span data-stu-id="ce5d3-161">For more information, see:</span></span>
- [<span data-ttu-id="ce5d3-162">Commerce Scale Unit のコンフィギュレーションとインストール (自己ホスト)</span><span class="sxs-lookup"><span data-stu-id="ce5d3-162">Configure and install Commerce Scale Unit (self-hosted)</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/retail/dev-itpro/retail-store-scale-unit-configuration-installation)
- [<span data-ttu-id="ce5d3-163">Commerce Scale Unit (自己ホスト)</span><span class="sxs-lookup"><span data-stu-id="ce5d3-163">Commerce Scale Unit (self-hosted)</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/retail/dev-itpro/retail-store-system-begin)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]