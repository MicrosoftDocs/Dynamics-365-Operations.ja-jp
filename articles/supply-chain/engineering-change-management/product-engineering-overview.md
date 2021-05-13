---
title: エンジニアリング変更管理の概要
description: このトピックでは、製品のバージョン管理の計画と管理を支援し、製品のライフサイクルとエンジニアリング変更を管理するエンジニアリング変更管理の概要を説明します。
author: t-benebo
ms.date: 11/11/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2020-09-28
ms.dyn365.ops.version: Release 10.0.15
ms.openlocfilehash: d7c0839ffbea80904ca12d1cba7ba9880f721cdd
ms.sourcegitcommit: 57668404d61359b33e0c0280f2f7c4eb829b1ed2
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/27/2021
ms.locfileid: "5947523"
---
# <a name="engineering-change-management-overview"></a><span data-ttu-id="188fc-103">エンジニアリング変更管理の概要</span><span class="sxs-lookup"><span data-stu-id="188fc-103">Engineering change management overview</span></span>

[!include [banner](../includes/banner.md)]

## <a name="feature-summary"></a><span data-ttu-id="188fc-104">機能の概要</span><span class="sxs-lookup"><span data-stu-id="188fc-104">Feature summary</span></span>

<span data-ttu-id="188fc-105">今日のメーカーは、製品のライフサイクル、品質と信頼性の要件の高まり、および製品の安全性に重点をおいており、強力な製品データ管理、バージョン管理、およびエンジニアリング変更管理を必要としています。</span><span class="sxs-lookup"><span data-stu-id="188fc-105">Today's manufacturers require strong product data management, version control, and engineering change management to succeed in a world of constantly shrinking product lifecycles, increased quality and reliability requirements, and an increased focus on product safety.</span></span>

<span data-ttu-id="188fc-106">エンジニアリング変更管理では、製品データ管理プロセスに構造と規範を提供し、ワークフローでサポートされている制御された方法で製品を定義、リリース、および改訂できるようにします。</span><span class="sxs-lookup"><span data-stu-id="188fc-106">Engineering change management brings structure and discipline to the product data management process, and enables products to be defined, released, and revised in a controlled manner that is supported by workflows.</span></span><span data-ttu-id="188fc-107">製品のライフサイクル全体にわたって、製品バージョンやエンジニアリング変更管理を通じて文書化、影響の評価、およびエンジニアリング変更の適用を行うことができます。</span><span class="sxs-lookup"><span data-stu-id="188fc-107"> Through product versions and engineering change management, you can document, assess the impact of, and apply engineering changes throughout the whole lifecycle of a product.</span></span>

<span data-ttu-id="188fc-108">エンジニアリング変更管理は、製品のバージョン管理の計画と管理を支援し、製品のライフサイクルとエンジニアリング変更を管理するエンジニアリング変更管理に役立ちます。</span><span class="sxs-lookup"><span data-stu-id="188fc-108">Engineering change management helps you plan and manage product versioning, and manage product lifecycles and engineering changes.</span></span> <span data-ttu-id="188fc-109">主な機能を次に示します:</span><span class="sxs-lookup"><span data-stu-id="188fc-109">Here is a list of its main features:</span></span>

- <span data-ttu-id="188fc-110">製品のバージョン管理</span><span class="sxs-lookup"><span data-stu-id="188fc-110">Product versioning</span></span>
- <span data-ttu-id="188fc-111">強化された製品リリース機能により、1 つの法人 (技術会社) で製品マスター データを管理し、すべてのリリース済製品を他の法人に公開することができます</span><span class="sxs-lookup"><span data-stu-id="188fc-111">Enhanced product release functionality that lets you maintain product master data in one legal entity (the engineering company) and publish the fully configured released product to other legal entities</span></span>
- <span data-ttu-id="188fc-112">製品バージョンを有効化する前に必要な情報が入力されていることを検証するためのルール (準備完了チェック)</span><span class="sxs-lookup"><span data-stu-id="188fc-112">Rules for validating that required information is entered before a product version is activated (readiness checks)</span></span>
- <span data-ttu-id="188fc-113">リリースされた製品を特定の業務プロセスで使用できる時期をきめ細かく制御することにより、製品ライフサイクル管理を強化</span><span class="sxs-lookup"><span data-stu-id="188fc-113">Improved product lifecycle management through fine-grained control over when a released product can be used in specific business processes</span></span>
- <span data-ttu-id="188fc-114">ワークフローでサポートされているエンジニアリング変更要求</span><span class="sxs-lookup"><span data-stu-id="188fc-114">Engineering change requests that are supported by workflows</span></span>
- <span data-ttu-id="188fc-115">ワークフローでサポートされているエンジニアリング変更指示</span><span class="sxs-lookup"><span data-stu-id="188fc-115">Engineering change orders that are supported by workflows</span></span>

> [!VIDEO https://www.microsoft.com/en-us/videoplayer/embed/RE4HE6B]

<span data-ttu-id="188fc-116">前のビデオ ([Dynamics 365 Supply Chain Management の変更管理機能](https://youtu.be/N313FqvRuBc)) は、YouTube で利用可能な [Finance and Operations 再生リスト](https://www.youtube.com/playlist?list=PLcakwueIHoT_SYfIaPGoOhloFoCXiUSyW)に含まれています。</span><span class="sxs-lookup"><span data-stu-id="188fc-116">The preceding video ([Change management capabilities in Dynamics 365 Supply Chain Management](https://youtu.be/N313FqvRuBc)) is included in the [Finance and Operations playlist](https://www.youtube.com/playlist?list=PLcakwueIHoT_SYfIaPGoOhloFoCXiUSyW) available on YouTube.</span></span>

## <a name="turn-on-the-engineering-change-management-and-version-dimension-features-for-your-system"></a><span data-ttu-id="188fc-117">システムに対するエンジニアリング変更管理およびバージョン分析コード機能の有効</span><span class="sxs-lookup"><span data-stu-id="188fc-117">Turn on the engineering change management and version dimension features for your system</span></span>

<span data-ttu-id="188fc-118">エンジニアリング変更管理を使用する前に、*エンジニアリング変更管理* 機能とそのコンフィギュレーション キーの両方を有効にする必要があります。</span><span class="sxs-lookup"><span data-stu-id="188fc-118">Before you can use engineering change management, you must enable both the *Engineering Change Management* feature and its configuration key.</span></span> <span data-ttu-id="188fc-119">トランザクション内の製品のバージョン分析コードも追跡する場合 (オプション)、*製品バージョン分析コード* 機能とそのコンフィギュレーション キーも有効にする必要があります。</span><span class="sxs-lookup"><span data-stu-id="188fc-119">If you also want to track the version dimension of products in transactions (optional), then you must also enable the *Product version dimension* feature and its configuration key.</span></span>

<span data-ttu-id="188fc-120">まず、次の手順に従って機能をオンにします。</span><span class="sxs-lookup"><span data-stu-id="188fc-120">First, turn on the features by following these steps.</span></span>

1. <span data-ttu-id="188fc-121">[機能管理](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)ワークスペースに移動します。</span><span class="sxs-lookup"><span data-stu-id="188fc-121">Go to the [Feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) workspace.</span></span>
1. <span data-ttu-id="188fc-122">更新プログラムを確認します。</span><span class="sxs-lookup"><span data-stu-id="188fc-122">Check for updates.</span></span>
1. <span data-ttu-id="188fc-123">**エンジニアリング変更管理** という機能を有効にします。</span><span class="sxs-lookup"><span data-stu-id="188fc-123">Turn on the feature that is named **Engineering Change Management**.</span></span>
1. <span data-ttu-id="188fc-124">それを使用する場合は、**製品分析コード バージョン** という名前の機能も有効にします。</span><span class="sxs-lookup"><span data-stu-id="188fc-124">If you want to use it, then also turn on the feature that is named **Product dimension version**.</span></span>

<span data-ttu-id="188fc-125">次に、次の手順に従ってコンフィギュレーション キーをオンにします。</span><span class="sxs-lookup"><span data-stu-id="188fc-125">Next, turn on the configuration keys by following these steps.</span></span>

1. <span data-ttu-id="188fc-126">[メンテナンス モード](../../fin-ops-core/dev-itpro/sysadmin/maintenance-mode.md)の説明に従って、システムをメンテナンス モードにします。</span><span class="sxs-lookup"><span data-stu-id="188fc-126">Put your system into maintenance mode, as described in [Maintenance mode](../../fin-ops-core/dev-itpro/sysadmin/maintenance-mode.md).</span></span>
1. <span data-ttu-id="188fc-127">**システム管理 \> 設定 \> ライセンス コンフィギュレーション** の順にクリックします。</span><span class="sxs-lookup"><span data-stu-id="188fc-127">Go to **System administration \> Setup \> License configuration**.</span></span>
1. <span data-ttu-id="188fc-128">**取引** ノードを展開します。</span><span class="sxs-lookup"><span data-stu-id="188fc-128">Expand the **Trade** node.</span></span>
1. <span data-ttu-id="188fc-129">**エンジニアリング変更管理** チェック ボックスを選択して、主要機能のコンフィギュレーション キーを有効にします。</span><span class="sxs-lookup"><span data-stu-id="188fc-129">Enable the configuration key for the main feature by selecting the **Engineering Change Management** check box.</span></span> <span data-ttu-id="188fc-130">(サブ機能の一方または両方を無効にする場合を除いて、ノードを展開する必要はありません。)</span><span class="sxs-lookup"><span data-stu-id="188fc-130">(It isn't necessary to expand the node unless you also want to disable one or both of its sub-features.)</span></span>
1. <span data-ttu-id="188fc-131">バージョン分析コードも使用する場合は、**製品分析コード - バージョン** チェック ボックスもオンにします。</span><span class="sxs-lookup"><span data-stu-id="188fc-131">If you also want to use the version dimension, then select the **Product dimension - Version** check box.</span></span> <span data-ttu-id="188fc-132">(このチェック ボックスは一覧の下の方にあり、**エンジニアリング変更管理** ノードの下に入れ子になってはいません。)</span><span class="sxs-lookup"><span data-stu-id="188fc-132">(This check box is further down the list, not nested under the **Engineering Change Management** node.)</span></span>
1. <span data-ttu-id="188fc-133">[メンテナンス モード](../../fin-ops-core/dev-itpro/sysadmin/maintenance-mode.md)の説明に従って、メンテナンス モードをオフにします。</span><span class="sxs-lookup"><span data-stu-id="188fc-133">Turn off maintenance mode, as described in [Maintenance mode](../../fin-ops-core/dev-itpro/sysadmin/maintenance-mode.md).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="188fc-134">2022 年 4 月から、**エンジニアリング変更管理** および **製品分析コード - バージョン** の両方のライセンス キーがすべての新規インストールで既定で有効になりますが、必要に応じて無効にすることもできます。</span><span class="sxs-lookup"><span data-stu-id="188fc-134">Starting in April 2022, the license keys for both **Engineering Change Management** and **Product dimension - Version** will be enabled by default for all new installations, but you will still be able to disable them if needed.</span></span>

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
