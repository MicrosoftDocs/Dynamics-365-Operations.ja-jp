---
title: 最新の Finance and Operations 更新プログラムへの移行の処理
description: このトピックでは、Microsoft Dynamics 365 for Finance and Operations の最新の更新バージョンに移行するプロセスについて説明します。
author: laneswenka
manager: AnnBe
ms.date: 04/30/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Developer, IT Pro
ms.reviewer: sericks
ms.search.scope: Operations
ms.custom: 102343
ms.assetid: e48d7424-371a-49ee-882c-07b7ceb00183
ms.search.region: Global
ms.author: laswenka
ms.search.validFrom: 2016-05-31
ms.dyn365.ops.version: Platform update 1
ms.openlocfilehash: d530c1c356342451c42b0bfb0cef48d25eaf323a
ms.sourcegitcommit: 16bfa0fd08feec1647829630401ce62ce2ffa1a4
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/02/2019
ms.locfileid: "1851653"
---
# <a name="process-for-moving-to-the-latest-update-of-finance-and-operations"></a><span data-ttu-id="a8db4-103">最新の Finance and Operations 更新プログラムへの移行の処理</span><span class="sxs-lookup"><span data-stu-id="a8db4-103">Process for moving to the latest update of Finance and Operations</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="a8db4-104">このトピックでは、Microsoft Dynamics 365 for Finance and Operations の最新のリリースに更新またはアップグレードするプロセスについて説明します。</span><span class="sxs-lookup"><span data-stu-id="a8db4-104">This topic explains the process of updating or upgrading to the latest release of Microsoft Dynamics 365 for Finance and Operations.</span></span> <span data-ttu-id="a8db4-105">プロセス全体とサポートされるシナリオを説明しますが、プロセスの各ステップに関する詳細な指示は提示しません。</span><span class="sxs-lookup"><span data-stu-id="a8db4-105">It describes the overall process and supported scenarios, but it doesn't provide detailed instructions for every step of the process.</span></span>

<span data-ttu-id="a8db4-106">Finance and Operations の各リリースの内容については、[新機能と変更点](../../fin-and-ops/get-started/whats-new-changed.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="a8db4-106">For information about the contents of each release of Finance and Operations, see [What's new or changed](../../fin-and-ops/get-started/whats-new-changed.md).</span></span>

<span data-ttu-id="a8db4-107">1 つのバージョンのサービス更新の詳細については、[1 つのバージョンのサービス更新の概要](../lifecycle-services/oneversion-overview.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="a8db4-107">For information about One Version service updates, see the [One Version service updates overview](../lifecycle-services/oneversion-overview.md).</span></span>

> [!Note]
> <span data-ttu-id="a8db4-108">Microsoft Dynamics AX 2012 から Finance and Operations へのアップグレードを検討している方は、[AX2012 から Finance and Operations へのアップグレード](upgrade-overview-2012.md) をご覧ください。</span><span class="sxs-lookup"><span data-stu-id="a8db4-108">For those looking to upgrade to Finance and Operations from Microsoft Dynamics AX 2012, please see [Upgrade from AX2012 to Finance and Operations](upgrade-overview-2012.md).</span></span>

## <a name="definitions"></a><span data-ttu-id="a8db4-109">定義</span><span class="sxs-lookup"><span data-stu-id="a8db4-109">Definitions</span></span>

- <span data-ttu-id="a8db4-110">**アップグレード**: バージョン 8.0 より前のソース環境では、Finance and Operations のある公式リリースから次のリリースに移行するプロセス。</span><span class="sxs-lookup"><span data-stu-id="a8db4-110">**Upgrade** – The process of moving from one official release of Finance and Operations to the next release, for source environments prior to version 8.0.</span></span> <span data-ttu-id="a8db4-111">例としては、7.1 から 7.3 または 7.3 から 10.0.1 への移行があります。</span><span class="sxs-lookup"><span data-stu-id="a8db4-111">Some examples are the move from 7.1 to 7.3, or from 7.3 to 10.0.1.</span></span> <span data-ttu-id="a8db4-112">プロセスには、無料サンド ボックス環境、コード アップグレード、およびデータ アップグレードの設定が含まれます。</span><span class="sxs-lookup"><span data-stu-id="a8db4-112">The process involves setup of a free sandbox environment, code upgrade, and data upgrade.</span></span>
- <span data-ttu-id="a8db4-113">**更新**: バージョン 8.0 以降のソース環境で、バイナリ パッケージを環境に適用し、Finance and Operations のある公式リリースから次のリリースに移行するプロセス。</span><span class="sxs-lookup"><span data-stu-id="a8db4-113">**Update** – The process of applying a binary package to an environment to move it from one official release of Finance and Operations to the next release, for source environments starting with version 8.0.</span></span> <span data-ttu-id="a8db4-114">このプロセスには、低いダウンタイム要件があり、データ アップグレードは含まれません。</span><span class="sxs-lookup"><span data-stu-id="a8db4-114">This process has lower downtime requirements and doesn't involve data upgrade.</span></span>

## <a name="paths-to-one-version"></a><span data-ttu-id="a8db4-115">1 つのバージョンへのパス</span><span class="sxs-lookup"><span data-stu-id="a8db4-115">Paths to One Version</span></span>
<img src="../migration-upgrade/media/OneVersion_Paths.png" width="600px" alt="Paths to One Version" />
<span data-ttu-id="a8db4-116">Finance and Operations の最新バージョンを導入するには 3 つの基本パスがあります。</span><span class="sxs-lookup"><span data-stu-id="a8db4-116">There are three primary paths to get to the latest version of Finance and Operations.</span></span>  <span data-ttu-id="a8db4-117">各パスは、詳細な手順へのリンクとともに以下で参照されます。</span><span class="sxs-lookup"><span data-stu-id="a8db4-117">Each path is referenced below with a link to detailed steps.</span></span>

### <a name="self-service-upgrade"></a><span data-ttu-id="a8db4-118">セルフサービス アップグレード</span><span class="sxs-lookup"><span data-stu-id="a8db4-118">Self-service upgrade</span></span>
<span data-ttu-id="a8db4-119">*適用可能な開始バージョン: Microsoft Dynamics 365 for Finance and Operations 7.0 (RTW)、7.1 (1611)、7.2 (2017 年 7 月)、7.3。*</span><span class="sxs-lookup"><span data-stu-id="a8db4-119">*Applicable starting version: Microsoft Dynamics 365 for Finance and Operations 7.0 (RTW), 7.1 (1611), 7.2 (July 2017), 7.3.*</span></span><br/>
<span data-ttu-id="a8db4-120">*スコープ: 複雑*</span><span class="sxs-lookup"><span data-stu-id="a8db4-120">*Scope: Complex*</span></span><br/>
<span data-ttu-id="a8db4-121">このパスには拡張機能へのコード リファクタリング、そして DevTest、サンドボックス、そして最終的には実稼働環境でのデータ アップグレードが含まれます。</span><span class="sxs-lookup"><span data-stu-id="a8db4-121">This path involves code refactoring to Extensions, and Data Upgrade in a DevTest, Sandbox, and eventually a Production environment.</span></span> 

<span data-ttu-id="a8db4-122">[セルフサービス アップグレードの実行](../migration-upgrade/self-service-upgrade.md).</span><span class="sxs-lookup"><span data-stu-id="a8db4-122">[Perform self-service upgrade](../migration-upgrade/self-service-upgrade.md).</span></span>

### <a name="rebuild-and-update"></a><span data-ttu-id="a8db4-123">再構築と更新</span><span class="sxs-lookup"><span data-stu-id="a8db4-123">Rebuild and update</span></span>
<span data-ttu-id="a8db4-124">*適用可能な開始バージョン: Microsoft Dynamics 365 for Finance and Operations 8.0*</span><span class="sxs-lookup"><span data-stu-id="a8db4-124">*Applicable starting version: Microsoft Dynamics 365 for Finance and Operations 8.0*</span></span><br/>
<span data-ttu-id="a8db4-125">*スコープ: 中程度*</span><span class="sxs-lookup"><span data-stu-id="a8db4-125">*Scope: Moderate*</span></span><br/>
<span data-ttu-id="a8db4-126">このパスは Microsoft X++ 修正プログラムを削除し、マージされた更新プログラム パッケージを作成します。</span><span class="sxs-lookup"><span data-stu-id="a8db4-126">This path involves removing Microsoft X++ hotfixes, and creating a merged update package.</span></span>

<span data-ttu-id="a8db4-127">[再構築と更新](../migration-upgrade/appupdate-80-81.md)。</span><span class="sxs-lookup"><span data-stu-id="a8db4-127">[Rebuild and update](../migration-upgrade/appupdate-80-81.md).</span></span>

### <a name="automatic-update"></a><span data-ttu-id="a8db4-128">自動更新</span><span class="sxs-lookup"><span data-stu-id="a8db4-128">Automatic update</span></span>
<span data-ttu-id="a8db4-129">*適用可能な開始バージョン: Microsoft Dynamics 365 for Finance and Operations 8.1.0+*</span><span class="sxs-lookup"><span data-stu-id="a8db4-129">*Applicable starting version: Microsoft Dynamics 365 for Finance and Operations 8.1.0+*</span></span><br/>
<span data-ttu-id="a8db4-130">*スコープ: 簡易*</span><span class="sxs-lookup"><span data-stu-id="a8db4-130">*Scope: Simple*</span></span><br/>
<span data-ttu-id="a8db4-131">このパスはプロジェクトを継続的に更新するように構成します。</span><span class="sxs-lookup"><span data-stu-id="a8db4-131">This path involves configuring your project for continuous updates.</span></span>

<span data-ttu-id="a8db4-132">[サービスの更新のコンフィギュレーション](../lifecycle-services/configure-service-updates.md)。</span><span class="sxs-lookup"><span data-stu-id="a8db4-132">[Configure service updates](../lifecycle-services/configure-service-updates.md).</span></span>

