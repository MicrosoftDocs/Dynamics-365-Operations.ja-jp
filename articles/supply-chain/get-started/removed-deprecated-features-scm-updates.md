---
title: Dynamics 365 Supply Chain Management の削除済みまたは推奨されない機能
description: このトピックでは、Dynamics 365 Supply Chain Management から削除された、または削除される予定の機能について説明します。
author: kamaybac
manager: tfehr
ms.date: 04/30/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2020-03-03
ms.dyn365.ops.version: Platform update 33
ms.openlocfilehash: 07f37488747766dcca96884e204339b425bbd201
ms.sourcegitcommit: f64fce03ec52f844b05a9e8cac286cb201385002
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 07/16/2020
ms.locfileid: "3597119"
---
# <a name="removed-or-deprecated-features-in-dynamics-365-supply-chain-management"></a><span data-ttu-id="ae676-103">Dynamics 365 Supply Chain Management の削除済みまたは推奨されない機能</span><span class="sxs-lookup"><span data-stu-id="ae676-103">Removed or deprecated features in Dynamics 365 Supply Chain Management</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="ae676-104">このトピックは、Dynamics 365 Supply Chain Management の新規削除または非推奨機能が文書化されると更新されます。</span><span class="sxs-lookup"><span data-stu-id="ae676-104">This topic will be updated as new removed or deprecated features are documented for Dynamics 365 Supply Chain Management.</span></span>

- <span data-ttu-id="ae676-105">*削除された*機能は製品では使用できません。</span><span class="sxs-lookup"><span data-stu-id="ae676-105">A *removed* feature is no longer available in the product.</span></span>
- <span data-ttu-id="ae676-106">*削除予定*の機能は現在開発中ではなく、将来の更新で削除される可能性があります。</span><span class="sxs-lookup"><span data-stu-id="ae676-106">A *deprecated* feature is not in active development and may be removed in a future update.</span></span>

<span data-ttu-id="ae676-107">このリストは、これらの削除および削除予定に対して、自身の計画を検討するために役立ちます。</span><span class="sxs-lookup"><span data-stu-id="ae676-107">This list is intended to help you consider these removals and deprecations for your own planning.</span></span>

> [!NOTE]
> <span data-ttu-id="ae676-108">Finance and Operations アプリ内のオブジェクトに関する詳細情報については、[技術参照レポート](https://mbs.microsoft.com/customersource/northamerica/AX/downloads/reports/axtechrefrep)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="ae676-108">Detailed information about objects in Finance and Operations apps can be found in the [Technical reference reports](https://mbs.microsoft.com/customersource/northamerica/AX/downloads/reports/axtechrefrep).</span></span> <span data-ttu-id="ae676-109">これら異なるバージョンのレポートを比較し、Finance and Operations アプリの各バージョンで変更または削除されたオブジェクトについて確認することができます。</span><span class="sxs-lookup"><span data-stu-id="ae676-109">You can compare the different versions of these reports to learn about objects that have changed or been removed in each version of Finance and Operations apps.</span></span>

## <a name="features-removed-or-deprecated-in-the-supply-chain-management-10011-release"></a><span data-ttu-id="ae676-110">Supply Chain Management 10.0.11 リリースの削除済みまたは非推奨の機能</span><span class="sxs-lookup"><span data-stu-id="ae676-110">Features removed or deprecated in the Supply Chain Management 10.0.11 release</span></span>

### <a name="use-of-built-in-supply-chain-management-master-planning-engine-for-distribution-scenarios"></a><span data-ttu-id="ae676-111">配送シナリオに、組み込み型 Supply Chain Management マスター プラン エンジンを使用する</span><span class="sxs-lookup"><span data-stu-id="ae676-111">Use of built-in Supply Chain Management master planning engine for distribution scenarios</span></span>

|   |  |
|------------|--------------------|
| <span data-ttu-id="ae676-112">**廃止 / 削除の理由**</span><span class="sxs-lookup"><span data-stu-id="ae676-112">**Reason for deprecation/removal**</span></span> | <span data-ttu-id="ae676-113">マスター プランの実行中のパフォーマンスを向上させ、SQLデータベースの負荷を最小化する目的で、組み込み型 Supply Chain Management マスタープラン エンジンは、プランの最適化によって置き換えられます。</span><span class="sxs-lookup"><span data-stu-id="ae676-113">To enhance performance and minimize the SQL database load during master planning runs, the built-in Supply Chain Management master planning engine is being replaced by Planning Optimization.</span></span> <span data-ttu-id="ae676-114">プランの最適化を使用すると、オフィス時間内でも実行できる迅速な計画の実行が可能となります。</span><span class="sxs-lookup"><span data-stu-id="ae676-114">Planning Optimization allows for fast planning runs that can be performed even during office hours.</span></span> <span data-ttu-id="ae676-115">これにより、立案者は、需要またはプランのパラメーターの変更にすぐに対応できます。</span><span class="sxs-lookup"><span data-stu-id="ae676-115">This enables planners to react immediately to changes in demand or planning parameters.</span></span> |
| <span data-ttu-id="ae676-116">**別の機能で置き換えられているか?**</span><span class="sxs-lookup"><span data-stu-id="ae676-116">**Replaced by another feature?**</span></span>   | <span data-ttu-id="ae676-117">既存の組み込み Supply Chain Management 計画エンジンは、マスター計画の最適化によって置き換えられます。</span><span class="sxs-lookup"><span data-stu-id="ae676-117">Yes, Planning Optimization will replace the existing built-in Supply Chain Management master planning engine.</span></span> |
| <span data-ttu-id="ae676-118">**影響を受ける製品領域**</span><span class="sxs-lookup"><span data-stu-id="ae676-118">**Product areas affected**</span></span>         | <span data-ttu-id="ae676-119">Supply Chain Management -マスター プラン</span><span class="sxs-lookup"><span data-stu-id="ae676-119">Supply Chain Management - Master planning</span></span> |
| <span data-ttu-id="ae676-120">**配置オプション**</span><span class="sxs-lookup"><span data-stu-id="ae676-120">**Deployment option**</span></span>              | <span data-ttu-id="ae676-121">クラウドのみ。</span><span class="sxs-lookup"><span data-stu-id="ae676-121">Cloud only.</span></span> <span data-ttu-id="ae676-122">プランの最適化では、オンプレミス展開に対応していません。</span><span class="sxs-lookup"><span data-stu-id="ae676-122">Planning Optimization is not supported with on-premises deployments.</span></span> |
| <span data-ttu-id="ae676-123">**ステータス**</span><span class="sxs-lookup"><span data-stu-id="ae676-123">**Status**</span></span>                         | <span data-ttu-id="ae676-124">非推奨。</span><span class="sxs-lookup"><span data-stu-id="ae676-124">Deprecated.</span></span> <span data-ttu-id="ae676-125">2021 年の 4 月で、配布シナリオは組込型の Dynamics 365 Supply Chain Management マスター プラン エンジンではサポートされなくなります。</span><span class="sxs-lookup"><span data-stu-id="ae676-125">On April 2021, distribution scenarios will no longer be supported with the built-in Dynamics 365 Supply Chain Management master planning engine.</span></span> <span data-ttu-id="ae676-126">配分シナリオでは、顧客はマスター プランの計画にプラン最適化を使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="ae676-126">For distribution scenarios, customers must use Planning Optimization for master planning calculations.</span></span> <span data-ttu-id="ae676-127">詳細については、[プランの最適化ドキュメント](https://go.microsoft.com/fwlink/?linkid=2105830) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="ae676-127">For more information, see [Planning Optimization documentation](https://go.microsoft.com/fwlink/?linkid=2105830).</span></span> <span data-ttu-id="ae676-128">Dynamics 365 Supply Chain Management のオンプレミスの配置の顧客は、2021 年 4 月以降の配送シナリオでは引き続き Supply Chain Management のマスター プラン エンジンを使用することができます。</span><span class="sxs-lookup"><span data-stu-id="ae676-128">Customers with on-premises deployments of Dynamics 365 Supply Chain Management may continue to use the Supply Chain Management master planning engine for distribution scenarios after April 2021.</span></span> <span data-ttu-id="ae676-129">ただし、今後の機能拡張は提供されません。</span><span class="sxs-lookup"><span data-stu-id="ae676-129">However, no more feature enhancements will be provided.</span></span> |

## <a name="previous-announcements-about-removed-or-deprecated-features"></a><span data-ttu-id="ae676-130">削除済みまたは非推奨の機能に関する以前の発表</span><span class="sxs-lookup"><span data-stu-id="ae676-130">Previous announcements about removed or deprecated features</span></span>

<span data-ttu-id="ae676-131">以前のリリースで削除または非推奨になった機能の詳細については、[以前のリリースで削除または非推奨になった機能](../../fin-ops-core/dev-itpro/migration-upgrade/deprecated-features.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="ae676-131">To learn more about features that have been removed or deprecated in previous releases, see [Removed or deprecated features in previous releases](../../fin-ops-core/dev-itpro/migration-upgrade/deprecated-features.md).</span></span>
