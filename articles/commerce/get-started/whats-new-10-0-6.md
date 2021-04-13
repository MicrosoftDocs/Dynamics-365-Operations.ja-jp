---
title: Dynamics 365 Retail バージョン 10.0.6 の新機能および変更された機能
description: このトピックでは Dynamics 365 Retail のプレビュー中の機能について説明します。
author: josaw1
ms.date: 10/09/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Developer, IT Pro
ms.reviewer: josaw
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: josaw
ms.search.validFrom: 2019-09-30
ms.dyn365.ops.version: Release 10.0.6
ms.openlocfilehash: 84e3bf751b9360c943d1ee3b2a1fe72bf65b495e
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/31/2021
ms.locfileid: "5797158"
---
# <a name="whats-new-or-changed-in-dynamics-365-retail-version-1006"></a><span data-ttu-id="96b64-103">Dynamics 365 Retail バージョン 10.0.6 の新機能および変更された機能</span><span class="sxs-lookup"><span data-stu-id="96b64-103">What's new or changed in Dynamics 365 Retail version 10.0.6</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="96b64-104">このトピックでは、Microsoft Dynamics 365 Retail 10.0.6 の新機能または変更された機能について説明します。</span><span class="sxs-lookup"><span data-stu-id="96b64-104">This topic describes features that are new or changed in Microsoft Dynamics 365 Retail in 10.0.6.</span></span> 

<span data-ttu-id="96b64-105">Finance and Operations アプリケーションの機能については、[Finance and Operations アプリ バージョン 10.0.6 (2019 年 11 月) の新機能と変更点](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/get-started/whats-new-changed-10-0-6) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="96b64-105">To learn about the features in Finance and Operations applications, see [What's new or changed in Finance and Operations apps version 10.0.6 (November 2019)](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/get-started/whats-new-changed-10-0-6).</span></span>

## <a name="new-inventory-availability-apis-for-e-commerce-use"></a><span data-ttu-id="96b64-106">E コマース用の新しい引当可能在庫数 API</span><span class="sxs-lookup"><span data-stu-id="96b64-106">New Inventory Availability API's for E-commerce use</span></span>
<span data-ttu-id="96b64-107">4 つの新しい API が利用可能になり、E コマースまたはサード パーティのソリューションに、要求された品目と倉庫に対する手持在庫の見積を提供します。</span><span class="sxs-lookup"><span data-stu-id="96b64-107">Four new API's will be made available to provide e-commerce or 3rd party solutions with an estimation of on-hand inventory for a requested item and warehouse.</span></span>  <span data-ttu-id="96b64-108">これらの API は、現在市場にある既存の GetProductAvailabilities および GetAvailableInventoryNearby API と置き換えることを目的としています。</span><span class="sxs-lookup"><span data-stu-id="96b64-108">These API's are intended to replace the existing GetProductAvailabilities and GetAvailableInventoryNearby API's that are currently in-market.</span></span>   <span data-ttu-id="96b64-109">これらの新しい API では、パフォーマンスを向上させるための計算ロジックとキャッシングが向上します。</span><span class="sxs-lookup"><span data-stu-id="96b64-109">These new API's will have improved calculation logic and caching to improve performance.</span></span>  <span data-ttu-id="96b64-110">新しい API の名前は次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="96b64-110">The names of the new API's are:</span></span>
* <span data-ttu-id="96b64-111">GetEstimatedProductWarehouseAvailability</span><span class="sxs-lookup"><span data-stu-id="96b64-111">GetEstimatedProductWarehouseAvailability</span></span>
* <span data-ttu-id="96b64-112">GetEstimatedAvailabilityDefaultWarehouse</span><span class="sxs-lookup"><span data-stu-id="96b64-112">GetEstimatedAvailabilityDefaultWarehouse</span></span>
* <span data-ttu-id="96b64-113">GetEstimatedAvailabilityNearby</span><span class="sxs-lookup"><span data-stu-id="96b64-113">GetEstimatedAvailabilityNearby</span></span>
* <span data-ttu-id="96b64-114">GetEstimatedAvailabilityAllWarehouses</span><span class="sxs-lookup"><span data-stu-id="96b64-114">GetEstimatedAvailabilityAllWarehouses</span></span>

<span data-ttu-id="96b64-115">また、チャネル データベースで利用可能な E コマースの在庫を追跡するための新しいテーブルが追加されました。</span><span class="sxs-lookup"><span data-stu-id="96b64-115">Additionally, new tables have been added for tracking available ecommerce inventory in the channel database.</span></span>  <span data-ttu-id="96b64-116">Retail および小売用の共有パラメーターが利用可能になります。以前のバージョンに存在していた既存の高価な E コマース引当可能在庫数ロジックを無効にするこれらの新しい API とテーブルを取得するよう、それらをコンフィギュレーションする必要があります。</span><span class="sxs-lookup"><span data-stu-id="96b64-116">Retail and Retail Shared parameters will be made available that must be configured to uptake these new API's and tables turn off the existing expensive e-commerce inventory availability logic that existed in previous versions.</span></span>

### <a name="install-merchant-properties-deprecated-from-the-hardware-station-installer"></a><span data-ttu-id="96b64-117">ハードウェア ステーション インストーラーからのマーチャント プロパティのインストールは推奨されません。</span><span class="sxs-lookup"><span data-stu-id="96b64-117">Install merchant properties deprecated from the Hardware station installer</span></span>
<span data-ttu-id="96b64-118">ヘッドレス インストールの将来の拡張機能をより適切にサポートするため、ハードウェア ステーション インストール操作からマーチャント プロパティ インストーラーが削除されました。</span><span class="sxs-lookup"><span data-stu-id="96b64-118">To better support future enhancements to headless installation, the merchant properties installer has been removed from the Hardware station installation experience.</span></span> <span data-ttu-id="96b64-119">10.0.6 の新機能として、ハードウェア ステーションのマーチャント プロパティは必要に応じて、POS をハードウェア ステーションとペアリングされる際の実行時に設定され、ハードウェア ステーションが有効になるときに更新されます。</span><span class="sxs-lookup"><span data-stu-id="96b64-119">New for 10.0.6, the hardware station merchant properties will be set at runtime when the POS is paired to a hardware station and updated when the hardware station is made active, if needed.</span></span> <span data-ttu-id="96b64-120">POS とハードウェア ステーションの両方が同時に 10.0.6 に更新されていない場合、POS によるマーチャント プロパティの設定と更新は正しく機能しません。</span><span class="sxs-lookup"><span data-stu-id="96b64-120">If both the POS and hardware station are not updated to 10.0.6 at the same time, the setting and updating of merchant properties by POS will not function correctly.</span></span> <span data-ttu-id="96b64-121">つまり、ハードウェア ステーションでなく POS が更新された場合、ハードウェア ステーションが更新されるまで古いマーチャント プロパティを引き続き使用することを意味します。</span><span class="sxs-lookup"><span data-stu-id="96b64-121">This means that if the POS is updated, but not the hardware station, then the hardware station will continue to use old merchant properties until it is updated as well.</span></span> 

## <a name="additional-resources"></a><span data-ttu-id="96b64-122">追加リソース</span><span class="sxs-lookup"><span data-stu-id="96b64-122">Additional resources</span></span>

### <a name="dynamics-365-2019-release-wave-2-plan"></a><span data-ttu-id="96b64-123">Dynamics 365: 2019 リリースのウェーブ 2 プラン</span><span class="sxs-lookup"><span data-stu-id="96b64-123">Dynamics 365: 2019 release wave 2 plan</span></span>

<span data-ttu-id="96b64-124">当社のビジネス アプリやプラットフォームの次回および最近リリースされた機能について検討中ですか?</span><span class="sxs-lookup"><span data-stu-id="96b64-124">Wondering about upcoming and recently released capabilities in any of our business apps or platform?</span></span>

<span data-ttu-id="96b64-125">[Dynamics 365: 2019 リリース ウェーブ 2 プラン](https://docs.microsoft.com/dynamics365-release-plan/2019wave2/index) をご確認ください。</span><span class="sxs-lookup"><span data-stu-id="96b64-125">Check out the [Dynamics 365: 2019 release wave 2 plan](https://docs.microsoft.com/dynamics365-release-plan/2019wave2/index).</span></span> <span data-ttu-id="96b64-126">あらゆる詳細情報を端から端まで徹底的に捕捉して一元化しました。計画を策定する際に 1 つのドキュメントでそれらの情報を参照できます。</span><span class="sxs-lookup"><span data-stu-id="96b64-126">We've captured all the details, end to end, top to bottom, in a single document that you can use for planning.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]