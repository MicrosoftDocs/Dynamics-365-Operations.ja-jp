---
title: Dynamics 365 Commerce の削除済みまたは推奨されない機能
description: このトピックでは、Dynamics 365 Commerce から削除された、または削除される予定の機能について説明します。
author: josaw
manager: AnnBe
ms.date: 05/04/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.author: josaw
ms.search.validFrom: 2020-04-30
ms.dyn365.ops.version: Platform update 33
ms.openlocfilehash: c47c5430a8f5d67e13c95db609a95d5ad66933ae
ms.sourcegitcommit: a8b6cd799eddaf5be9aec9ea3c2b55e2c3231652
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/05/2020
ms.locfileid: "3335279"
---
# <a name="removed-or-deprecated-features-in-dynamics-365-commerce"></a><span data-ttu-id="bd293-103">Dynamics 365 Commerce の削除済みまたは推奨されない機能</span><span class="sxs-lookup"><span data-stu-id="bd293-103">Removed or deprecated features in Dynamics 365 Commerce</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="bd293-104">このトピックでは、Dynamics 365 Commerce から削除された、または削除される予定の機能について説明します。</span><span class="sxs-lookup"><span data-stu-id="bd293-104">This topic describes features that have been removed, or that are planned for removal from Dynamics 365 Commerce.</span></span>

- <span data-ttu-id="bd293-105">*削除された*機能は製品では使用できません。</span><span class="sxs-lookup"><span data-stu-id="bd293-105">A *removed* feature is no longer available in the product.</span></span>
- <span data-ttu-id="bd293-106">*削除予定*の機能は現在開発中ではなく、将来の更新で削除される可能性があります。</span><span class="sxs-lookup"><span data-stu-id="bd293-106">A *deprecated* feature is not in active development and may be removed in a future update.</span></span>

<span data-ttu-id="bd293-107">このリストは、これらの削除および削除予定に対して、自身の計画を検討するために役立ちます。</span><span class="sxs-lookup"><span data-stu-id="bd293-107">This list is intended to help you consider these removals and deprecations for your own planning.</span></span> 

> [!NOTE]
> <span data-ttu-id="bd293-108">Finance and Operations アプリ内のオブジェクトに関する詳細情報については、[技術参照レポート](https://mbs.microsoft.com/customersource/northamerica/AX/downloads/reports/axtechrefrep)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="bd293-108">Detailed information about objects in Finance and Operations apps can be found in the [Technical reference reports](https://mbs.microsoft.com/customersource/northamerica/AX/downloads/reports/axtechrefrep).</span></span> <span data-ttu-id="bd293-109">これら異なるバージョンのレポートを比較し、Finance and Operations アプリの各バージョンで変更または削除されたオブジェクトについて確認することができます。</span><span class="sxs-lookup"><span data-stu-id="bd293-109">You can compare the different versions of these reports to learn about objects that have changed or been removed in each version of Finance and Operations apps.</span></span>

## <a name="features-removed-or-deprecated-in-the-commerce-10010-release"></a><span data-ttu-id="bd293-110">Commerce 10.0.10 リリースの削除済みまたは非推奨の機能</span><span class="sxs-lookup"><span data-stu-id="bd293-110">Features removed or deprecated in the Commerce 10.0.10 release</span></span>
### <a name="pos-operation-803---picking-and-receiving"></a><span data-ttu-id="bd293-111">POS operation 803 - ピッキングと入荷</span><span class="sxs-lookup"><span data-stu-id="bd293-111">POS operation 803 - Picking and receiving</span></span>
|   |  |
|------------|--------------------|
| <span data-ttu-id="bd293-112">**廃止 / 削除の理由**</span><span class="sxs-lookup"><span data-stu-id="bd293-112">**Reason for deprecation/removal**</span></span> | <span data-ttu-id="bd293-113">ピッキングと入庫処理は、運用面の見直しに伴い、現在は使用されていません。</span><span class="sxs-lookup"><span data-stu-id="bd293-113">Picking and receiving operations is being deprecated due to new operation redesign.</span></span> |
| <span data-ttu-id="bd293-114">**別の機能で置き換えられているか?**</span><span class="sxs-lookup"><span data-stu-id="bd293-114">**Replaced by another feature?**</span></span>   | <span data-ttu-id="bd293-115">はい。</span><span class="sxs-lookup"><span data-stu-id="bd293-115">Yes.</span></span> <span data-ttu-id="bd293-116">この機能は、インバウンド処理 (804) とアウトバウンド処理 (805) の 2 つの新しい POS 工程に置き換えられます。</span><span class="sxs-lookup"><span data-stu-id="bd293-116">It is replaced by two new POS operations: inbound operation (804) and outbound operation (805).</span></span>|
| <span data-ttu-id="bd293-117">**影響を受ける製品領域**</span><span class="sxs-lookup"><span data-stu-id="bd293-117">**Product areas affected**</span></span>         | <span data-ttu-id="bd293-118">販売時点管理（POS）アプリケーション</span><span class="sxs-lookup"><span data-stu-id="bd293-118">Point of sale (POS) application</span></span> |
| <span data-ttu-id="bd293-119">**配置オプション**</span><span class="sxs-lookup"><span data-stu-id="bd293-119">**Deployment option**</span></span>              | <span data-ttu-id="bd293-120">すべて</span><span class="sxs-lookup"><span data-stu-id="bd293-120">All</span></span> |
| <span data-ttu-id="bd293-121">**ステータス**</span><span class="sxs-lookup"><span data-stu-id="bd293-121">**Status**</span></span>                         | <span data-ttu-id="bd293-122">使用されていません：リリース 10.0.10 の時点で、ピッキングと入荷の処理は、新たな更新プログラムが適用されません。</span><span class="sxs-lookup"><span data-stu-id="bd293-122">Deprecated: As of release 10.0.10, the picking and receiving operation will no longer receive any new feature updates.</span></span> <span data-ttu-id="bd293-123">今後のリリースでは、この処理に対する重大なバグの修正のみが行われます。</span><span class="sxs-lookup"><span data-stu-id="bd293-123">Only critical bug fixes will be done for this operation in future releases.</span></span> <span data-ttu-id="bd293-124">すべてのお客様には、新しい[インバウンド処理](https://docs.microsoft.com/dynamics365/commerce/pos-inbound-inventory-operation)と[アウトバウンド処理](https://docs.microsoft.com/dynamics365/commerce/pos-outbound-inventory-operation)への移行を奨励して おり、引き続き長期的な製品ロードマップに含まれています。</span><span class="sxs-lookup"><span data-stu-id="bd293-124">All customers are encouraged to move to the new [Inbound operations](https://docs.microsoft.com/dynamics365/commerce/pos-inbound-inventory-operation) and [Outbound operations](https://docs.microsoft.com/dynamics365/commerce/pos-outbound-inventory-operation), which will continue to be part of our long-term product roadmap.</span></span> |


## <a name="features-removed-or-deprecated-in-the-commerce-1007-release"></a><span data-ttu-id="bd293-125">Commerce 10.0.7 リリースの削除済みまたは非推奨の機能</span><span class="sxs-lookup"><span data-stu-id="bd293-125">Features removed or deprecated in the Commerce 10.0.7 release</span></span>
### <a name="commerce-getproductavailabilities-and-getavailableinventorynearby-apis"></a><span data-ttu-id="bd293-126">Commerce GetProductAvailabilities と GetAvailableInventoryNearby API</span><span class="sxs-lookup"><span data-stu-id="bd293-126">Commerce GetProductAvailabilities and GetAvailableInventoryNearby API's</span></span>
|   |  |
|------------|--------------------|
| <span data-ttu-id="bd293-127">**廃止 / 削除の理由**</span><span class="sxs-lookup"><span data-stu-id="bd293-127">**Reason for deprecation/removal**</span></span> | <span data-ttu-id="bd293-128">GetProductAvailabilities と GetAvailableInventoryNearby API は、新たに最適化された API に置き換えられます。</span><span class="sxs-lookup"><span data-stu-id="bd293-128">New optimized APIs have been created to replace the GetProductAvailabilities and GetAvailableInventoryNearby APIs.</span></span> |
| <span data-ttu-id="bd293-129">**別の機能で置き換えられているか?**</span><span class="sxs-lookup"><span data-stu-id="bd293-129">**Replaced by another feature?**</span></span>   | <span data-ttu-id="bd293-130">今後は、GetEstimatedAvailabilty と GetEstimatedProductWarehouseAvailability API がご利用頂けます。</span><span class="sxs-lookup"><span data-stu-id="bd293-130">Yes: It is replaced by GetEstimatedAvailabilty and GetEstimatedProductWarehouseAvailability APIs.</span></span> |
| <span data-ttu-id="bd293-131">**影響を受ける製品領域**</span><span class="sxs-lookup"><span data-stu-id="bd293-131">**Product areas affected**</span></span>         | <span data-ttu-id="bd293-132">eコマース アプリケーション SDK</span><span class="sxs-lookup"><span data-stu-id="bd293-132">e-Commerce application SDK</span></span> |
| <span data-ttu-id="bd293-133">**配置オプション**</span><span class="sxs-lookup"><span data-stu-id="bd293-133">**Deployment option**</span></span>              | <span data-ttu-id="bd293-134">すべて</span><span class="sxs-lookup"><span data-stu-id="bd293-134">All</span></span> |
| <span data-ttu-id="bd293-135">**ステータス**</span><span class="sxs-lookup"><span data-stu-id="bd293-135">**Status**</span></span>                         | <span data-ttu-id="bd293-136">非推奨: リリース バージョン 10.0.7 の時点では、GetProductAvailabilities と GetAvailableInventoryNearby に対する新規開発は今後行われません。</span><span class="sxs-lookup"><span data-stu-id="bd293-136">Deprecated: As of release 10.0.7, there will no longer be engineering investments made for GetProductAvailabilities and GetAvailableInventoryNearby.</span></span> <span data-ttu-id="bd293-137">これら API をeコマース環境で使用している組織では、新しい GetEstimatedAvailabilty と GetEstimatedProductWarehouseAvailability API に置き換えを行い、[最適化された商品在庫計算機能 ](https://docs.microsoft.com/dynamics365/commerce/calculated-inventory-retail-channels) を有効化する必要があります。</span><span class="sxs-lookup"><span data-stu-id="bd293-137">Organizations that use these APIs in their e-Commerce deployments should convert to the new GetEstimatedAvailabilty and GetEstimatedProductWarehouseAvailability APIs and enable the [Optimized product availability calculation feature](https://docs.microsoft.com/dynamics365/commerce/calculated-inventory-retail-channels).</span></span>  |

## <a name="previous-announcements-about-removed-or-deprecated-features"></a><span data-ttu-id="bd293-138">削除済みまたは非推奨の機能に関する以前の発表</span><span class="sxs-lookup"><span data-stu-id="bd293-138">Previous announcements about removed or deprecated features</span></span>
<span data-ttu-id="bd293-139">以前のリリースで削除または非推奨になった機能の詳細については、[以前のリリースで削除または非推奨になった機能](../../fin-ops-core/dev-itpro/migration-upgrade/deprecated-features.md?toc=/dynamics365/commerce/toc.json)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="bd293-139">To learn more about features that have been removed or deprecated in previous releases, see [Removed or deprecated features in previous releases](../../fin-ops-core/dev-itpro/migration-upgrade/deprecated-features.md?toc=/dynamics365/commerce/toc.json).</span></span>
