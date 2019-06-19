---
title: ストア内トポロジを選択します。
description: このトピックでは、様々な Dynamics 365 for Retail の実店舗構成図を提供します。
author: rassadi
manager: AnnBe
ms.date: 05/13/2019
ms.topic: article
ms.prod: ''
ms.service: Dynamics-365-retail
ms.technology: ''
ms.search.form: SysAADClientTable, RetailTransactionServiceProfile
audience: IT Pro
ms.reviewer: kfend
ms.search.scope: Operations, Retail, Core
ms.custom: 44351
ms.search.region: Global
ms.author: jashanno
ms.search.validFrom: 2019-03-01
ms.openlocfilehash: aed5ff32cd9ddc7b327e550c626c38e960440b97
ms.sourcegitcommit: 987d7ef5a5df53e2272db6814fe6ef78be1a9aab
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/13/2019
ms.locfileid: "1540173"
---
# <a name="select-an-in-store-topology"></a><span data-ttu-id="76f40-103">ストア内トポロジを選択します。</span><span class="sxs-lookup"><span data-stu-id="76f40-103">Select an in-store topology</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="76f40-104">このトピックでは、様々な Dynamics 365 for Retail の実店舗構成図の概要を提供します。</span><span class="sxs-lookup"><span data-stu-id="76f40-104">This topic provides an overview of the various Dynamics 365 for Retail in-store topologies.</span></span> 

<span data-ttu-id="76f40-105"><a href="https://docs.microsoft.com/en-us/dynamics365/unified-operations/retail/dev-itpro/media/channel/instore/topology.jpg" rel="some text">![店舗の構成図で右の小売りを選択します。](media/CHANNEL/INSTORE/Topology.jpg)</a></span><span class="sxs-lookup"><span data-stu-id="76f40-105"><a href="https://docs.microsoft.com/en-us/dynamics365/unified-operations/retail/dev-itpro/media/channel/instore/topology.jpg" rel="some text">![Choose the right Retail in store topology](media/CHANNEL/INSTORE/Topology.jpg)</a></span></span>

## <a name="supported-capabilities-when-connectivity-is-lost"></a><span data-ttu-id="76f40-106">接続が失われたときにサポートしている機能</span><span class="sxs-lookup"><span data-stu-id="76f40-106">Supported capabilities when connectivity is lost</span></span>
| <span data-ttu-id="76f40-107">操作</span><span class="sxs-lookup"><span data-stu-id="76f40-107">Operation</span></span> | <span data-ttu-id="76f40-108">小売りサーバーへの接続がされていないとき</span><span class="sxs-lookup"><span data-stu-id="76f40-108">Without connectivity to Retail Server</span></span><br><span data-ttu-id="76f40-109">MPOS オフライン モード</span><span class="sxs-lookup"><span data-stu-id="76f40-109">(in MPOS Offline Mode)</span></span> | <span data-ttu-id="76f40-110">本部への接続がされていないとき</span><span class="sxs-lookup"><span data-stu-id="76f40-110">Without connectivity to HQ</span></span><br><span data-ttu-id="76f40-111">(RSSUを使用)</span><span class="sxs-lookup"><span data-stu-id="76f40-111">(using RSSU)</span></span> |
| --- | :-: | :-: |
| <span data-ttu-id="76f40-112">クロス ターミナル シフト (ビュー、中断、再開、切断など)</span><span class="sxs-lookup"><span data-stu-id="76f40-112">Cross terminal shifts (such as view, suspend, resume, close)</span></span> | | <span data-ttu-id="76f40-113">✔</span><span class="sxs-lookup"><span data-stu-id="76f40-113">✔</span></span> | 
| <span data-ttu-id="76f40-114">クロス ターミナル トランザクション (ビュー、中断、再開など)</span><span class="sxs-lookup"><span data-stu-id="76f40-114">Cross terminal transactions (such as view, suspend, resume)</span></span>  | | <span data-ttu-id="76f40-115">✔</span><span class="sxs-lookup"><span data-stu-id="76f40-115">✔</span></span> |

## <a name="supported-operations-when-connectivity-is-lost"></a><span data-ttu-id="76f40-116">接続が失われたときにサポートしている操作</span><span class="sxs-lookup"><span data-stu-id="76f40-116">Supported operations when connectivity is lost</span></span>
<span data-ttu-id="76f40-117">POSが本部との接続を失った場合にサポートしている宗さんの一覧については、 [オンラインおよびオフラインでの店頭(POS)操作](https://docs.microsoft.com/en-us/dynamics365/unified-operations/retail/pos-operations) 参照してください。。</span><span class="sxs-lookup"><span data-stu-id="76f40-117">For a list of operations that are supported when the POS loses connectivity to the HQ, see [Online and offline point of sale (POS) operations](https://docs.microsoft.com/en-us/dynamics365/unified-operations/retail/pos-operations).</span></span>

## <a name="supported-deployment-and-maintenance-capabilities"></a><span data-ttu-id="76f40-118">サポートされている導入及びメンテナンスの機能</span><span class="sxs-lookup"><span data-stu-id="76f40-118">Supported deployment and maintenance capabilities</span></span>
<span data-ttu-id="76f40-119">最新のPOSでは、大規模な一括配置をサポートしていますが、 Retail Store Scale Unit では未対応となっています。</span><span class="sxs-lookup"><span data-stu-id="76f40-119">Mass deployment is supported in Modern POS, but not in Retail Store Scale Unit.</span></span> <span data-ttu-id="76f40-120">詳細については、 [Retail セルフサービス コンポーネントの一括配置](https://docs.microsoft.com/en-us/dynamics365/unified-operations/retail/dev-itpro/retail-mass-deployment) をご参照ください。</span><span class="sxs-lookup"><span data-stu-id="76f40-120">For more information, see [Mass deployment of Retail self-service components](https://docs.microsoft.com/en-us/dynamics365/unified-operations/retail/dev-itpro/retail-mass-deployment).</span></span>

## <a name="deployed-components"></a><span data-ttu-id="76f40-121">配置可能なコンポーネント</span><span class="sxs-lookup"><span data-stu-id="76f40-121">Deployed components</span></span>
<span data-ttu-id="76f40-122">次に示すコンポーネントは、すべて1つのインストーラーを使って配置されます。</span><span class="sxs-lookup"><span data-stu-id="76f40-122">The following components are deployed through a single installer.</span></span> <span data-ttu-id="76f40-123">これらをそれぞれ個別でインストールする必要はありません。</span><span class="sxs-lookup"><span data-stu-id="76f40-123">This means that they do not need to be installed individually.</span></span>

### <a name="modern-pos"></a><span data-ttu-id="76f40-124">Modern POS</span><span class="sxs-lookup"><span data-stu-id="76f40-124">Modern POS</span></span>
| <span data-ttu-id="76f40-125">配置可能なコンポーネント</span><span class="sxs-lookup"><span data-stu-id="76f40-125">Deployed component</span></span> | <span data-ttu-id="76f40-126">コンポーネント タイプ</span><span class="sxs-lookup"><span data-stu-id="76f40-126">Component type</span></span> | <span data-ttu-id="76f40-127">摘要</span><span class="sxs-lookup"><span data-stu-id="76f40-127">Notes</span></span> |
| --- | --- | --- |
| <span data-ttu-id="76f40-128">最新のPOSアプリケーション</span><span class="sxs-lookup"><span data-stu-id="76f40-128">Modern POS App</span></span> | <span data-ttu-id="76f40-129">ユニバーサル Windows プラットフォーム アプリケーション</span><span class="sxs-lookup"><span data-stu-id="76f40-129">Universal Windows Platform (UWP) Application</span></span> | <span data-ttu-id="76f40-130">レジで稼働する最新のPOSアプリケーションです。</span><span class="sxs-lookup"><span data-stu-id="76f40-130">The Modern POS application running on the register.</span></span> |
| <span data-ttu-id="76f40-131">最新のPOS クライアント ブローカー</span><span class="sxs-lookup"><span data-stu-id="76f40-131">Modern POS Client Broker</span></span> | <span data-ttu-id="76f40-132">最新のPOSのネイティブ バイナリをホストしているCOM Surrogate</span><span class="sxs-lookup"><span data-stu-id="76f40-132">COM Surrogate hosting native binaries for the Modern POS</span></span> | <span data-ttu-id="76f40-133">オフラインモードでの操作の実行をサポートする Commerce Runtime を提供します。また、最新のPOSと本部とデータを同期するにはAsync Clientライブラリも同様に必要となります。</span><span class="sxs-lookup"><span data-stu-id="76f40-133">Hosts the Commerce Runtime to support operations to execute in offline mode as well as Async Client Libraries needed to synchronize data between the Modern POS and the HQ.</span></span> | 
| <span data-ttu-id="76f40-134">チャンネル データベース</span><span class="sxs-lookup"><span data-stu-id="76f40-134">Channel Database</span></span> | <span data-ttu-id="76f40-135">SQL データベース</span><span class="sxs-lookup"><span data-stu-id="76f40-135">SQL Database</span></span> | <span data-ttu-id="76f40-136">レジのデータを提供している特定のチャンネル データベース インスタンスを登録します。</span><span class="sxs-lookup"><span data-stu-id="76f40-136">Register specific Channel Database instance hosting data for the register.</span></span>

### <a name="retail-store-scale-unit"></a><span data-ttu-id="76f40-137">Retail Store Scale Unit</span><span class="sxs-lookup"><span data-stu-id="76f40-137">Retail store scale unit</span></span>
| <span data-ttu-id="76f40-138">インストールされたコンポーネント</span><span class="sxs-lookup"><span data-stu-id="76f40-138">Installed component</span></span> | <span data-ttu-id="76f40-139">コンポーネント タイプ</span><span class="sxs-lookup"><span data-stu-id="76f40-139">Component type</span></span> | <span data-ttu-id="76f40-140">摘要</span><span class="sxs-lookup"><span data-stu-id="76f40-140">Notes</span></span> |
| --- | --- | --- |
| <span data-ttu-id="76f40-141">Retail サーバー</span><span class="sxs-lookup"><span data-stu-id="76f40-141">Retail Server</span></span> | <span data-ttu-id="76f40-142">IIS Web サービス</span><span class="sxs-lookup"><span data-stu-id="76f40-142">IIS Web Service</span></span> | <span data-ttu-id="76f40-143">1つ以上の店舗で使用する小売 Serverのインスタンスの単位を計測します。</span><span class="sxs-lookup"><span data-stu-id="76f40-143">Scale unit specific Retail Server instance used by one or more stores.</span></span> |
| <span data-ttu-id="76f40-144">チャンネル データベース</span><span class="sxs-lookup"><span data-stu-id="76f40-144">Channel Database</span></span> | <span data-ttu-id="76f40-145">SQL データベース</span><span class="sxs-lookup"><span data-stu-id="76f40-145">SQL Database</span></span> | <span data-ttu-id="76f40-146">1つ以上の店舗で使用するデータを提供する、特定のチャンネルデータベースインスタンスの店舗単位を計測します。</span><span class="sxs-lookup"><span data-stu-id="76f40-146">Scale unit specific Store specific Channel Database instance hosting data for one or more stores.</span></span> |
| <span data-ttu-id="76f40-147">Async Client サービス</span><span class="sxs-lookup"><span data-stu-id="76f40-147">Async Client Service</span></span> | <span data-ttu-id="76f40-148">Windows サービス</span><span class="sxs-lookup"><span data-stu-id="76f40-148">Windows Service</span></span> | <span data-ttu-id="76f40-149">マスター レコード データを本部から店舗へ、取引データを店舗から本部へと同期するためのコンポーネント</span><span class="sxs-lookup"><span data-stu-id="76f40-149">Component to synchronize master record data from the HQ to the store and transactional data from the store to the HQ.</span></span> |
| <span data-ttu-id="76f40-150">クラウド POS</span><span class="sxs-lookup"><span data-stu-id="76f40-150">Cloud POS</span></span> | <span data-ttu-id="76f40-151">IIS Web サービス</span><span class="sxs-lookup"><span data-stu-id="76f40-151">IIS Web Service</span></span> | <span data-ttu-id="76f40-152">Web ブラウザーを使用して POS 機能をホストするクラウド POS アプリケーション。</span><span class="sxs-lookup"><span data-stu-id="76f40-152">Cloud POS application that hosts POS functionality through a web browser.</span></span> |

## <a name="additional-resources"></a><span data-ttu-id="76f40-153">追加リソース</span><span class="sxs-lookup"><span data-stu-id="76f40-153">Additional resources</span></span>
### <a name="mpos-offline-mode"></a><span data-ttu-id="76f40-154">MPOS オフライン モード</span><span class="sxs-lookup"><span data-stu-id="76f40-154">MPOS offline mode</span></span>
<span data-ttu-id="76f40-155">MPOS オフラインモードの詳細については、以下を参照してください。</span><span class="sxs-lookup"><span data-stu-id="76f40-155">For more information about MPOS offline mode, see:</span></span>
- [<span data-ttu-id="76f40-156">オフライン販売時点管理 (POS) の機能</span><span class="sxs-lookup"><span data-stu-id="76f40-156">Offline point of sale (POS) functionality</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/retail/pos-offline-functionality)
- [<span data-ttu-id="76f40-157">オンラインおよびオフラインでの販売時点管理 (POS) の操作</span><span class="sxs-lookup"><span data-stu-id="76f40-157">Online and offline point of sale (POS) operations</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/retail/pos-operations)
- [<span data-ttu-id="76f40-158">Retail セルフサービス コンポーネントの一括配置</span><span class="sxs-lookup"><span data-stu-id="76f40-158">Mass deployment of Retail self-service components</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/retail/dev-itpro/retail-mass-deployment)

### <a name="retail-store-scale-unit"></a><span data-ttu-id="76f40-159">Retail Store Scale Unit</span><span class="sxs-lookup"><span data-stu-id="76f40-159">Retail store scale unit</span></span> 
<span data-ttu-id="76f40-160">Retail store scale unit は、実店舗などお客様の環境に配置することが可能な、バックオフィスや本部 (HQ) への通信が切断された場合でも継続して業務を行うことをサポートするコンポーネントです。</span><span class="sxs-lookup"><span data-stu-id="76f40-160">The Retail store scale unit (RSSU) is a set of components that can be deployed in a customer environment, such as inside a store, that can support continuous operations if connectivity to the back office or headquarters (HQ) is lost.</span></span> 

<span data-ttu-id="76f40-161">詳細については、以下を参照してください。</span><span class="sxs-lookup"><span data-stu-id="76f40-161">For more information, see:</span></span>
- [<span data-ttu-id="76f40-162">Retail Store Scale Unit の設定とインストール</span><span class="sxs-lookup"><span data-stu-id="76f40-162">Configure and install retail store scale unit</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/retail/dev-itpro/retail-store-scale-unit-configuration-installation)
- [<span data-ttu-id="76f40-163">Retail Store Scale Unit</span><span class="sxs-lookup"><span data-stu-id="76f40-163">Retail Store Scale Unit</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/retail/dev-itpro/retail-store-system-begin)