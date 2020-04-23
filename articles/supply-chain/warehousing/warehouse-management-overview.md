---
title: 倉庫管理概要
description: 倉庫プロセスを監視および自動化するために、倉庫管理を使用します。
author: ShylaThompson
manager: tfehr
ms.date: 07/25/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSParameters
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 17e4429dbf3f7e5d6c737c365f0351d5c588fcd2
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/02/2020
ms.locfileid: "3204588"
---
# <a name="warehouse-management-overview"></a><span data-ttu-id="764ce-103">倉庫管理の概要</span><span class="sxs-lookup"><span data-stu-id="764ce-103">Warehouse management overview</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="764ce-104">倉庫管理モジュールは、製造、配送、および小売企業の倉庫プロセスを管理できます。</span><span class="sxs-lookup"><span data-stu-id="764ce-104">The Warehouse management module lets you manage warehouse processes in manufacturing, distribution, and retail companies.</span></span> <span data-ttu-id="764ce-105">このモジュールは、倉庫施設をいつでも最適なレベルにサポートする幅広い機能を持っています。</span><span class="sxs-lookup"><span data-stu-id="764ce-105">This module has a wide range of features to support the warehouse facility at an optimal level, at any time.</span></span> <span data-ttu-id="764ce-106">倉庫管理では、輸送、製造、品質テスト、購買、移動、販売、返品などの他のビジネス プロセスが完全に統合されます。</span><span class="sxs-lookup"><span data-stu-id="764ce-106">Warehouse management is fully integrated with other business processes such as transportation, manufacturing, quality control, purchase, transfer, sales, and returns.</span></span>

## <a name="get-started"></a><span data-ttu-id="764ce-107">使用開始</span><span class="sxs-lookup"><span data-stu-id="764ce-107">Get started</span></span>
<span data-ttu-id="764ce-108">倉庫管理の操作を開始するには、会社の業務プロセスをサポートするための通常倉庫のパラメーターの設定を完了する必要があります。</span><span class="sxs-lookup"><span data-stu-id="764ce-108">To start working with Warehouse management, you need to complete the setup of the general warehouse parameters to support the business processes of you company.</span></span>

- <span data-ttu-id="764ce-109">**倉庫管理** > **設定**ページ下の**倉庫管理パラメーター**に移動し、通常倉庫のパラメーターの設定をします。</span><span class="sxs-lookup"><span data-stu-id="764ce-109">Go to the **Warehouse management parameters** page under **Warehouse management** > **Setup** to set up general warehouse parameters.</span></span>

<span data-ttu-id="764ce-110">業務要件に従って入庫/出庫の倉庫プロセスワークフローをコンフィギュレーションする必要があります。</span><span class="sxs-lookup"><span data-stu-id="764ce-110">You must configure components for inbound and outbound warehouse process workflows according to business requirements.</span></span> <span data-ttu-id="764ce-111">コンフィギュレーションする必要がある最も重要なコンポーネントは、ウェーブ テンプレート、作業テンプレート、作業プールと場所のディレクティブです。</span><span class="sxs-lookup"><span data-stu-id="764ce-111">The most important components that you must configure are wave templates, work templates, work pools, and location directives.</span></span>

- [<span data-ttu-id="764ce-112">倉庫のコンフィギュレーションの概要</span><span class="sxs-lookup"><span data-stu-id="764ce-112">Warehouse configuration overview</span></span>](warehouse-configuration.md)
- [<span data-ttu-id="764ce-113">作業テンプレートと場所ディレクティブを使用した倉庫作業の制御</span><span class="sxs-lookup"><span data-stu-id="764ce-113">Control warehouse work by using work templates and location directives</span></span>](control-warehouse-location-directives.md)
- [<span data-ttu-id="764ce-114">倉庫作業用のモバイル デバイスの設定</span><span class="sxs-lookup"><span data-stu-id="764ce-114">Set up mobile devices for warehouse work</span></span>](configure-mobile-devices-warehouse.md)
- [<span data-ttu-id="764ce-115">発注書のプット アウェイ場所のディレクティブの設定</span><span class="sxs-lookup"><span data-stu-id="764ce-115">Set up a location directive for purchase order put-away</span></span>](../transportation/tasks/set-up-location-directive-purchase-order-put-away.md)
- [<span data-ttu-id="764ce-116">発注書の作業テンプレートの設定</span><span class="sxs-lookup"><span data-stu-id="764ce-116">Set up a work template for purchase orders</span></span>](./tasks/set-up-work-template-purchase-orders.md)

## <a name="warehouse-management-processes"></a><span data-ttu-id="764ce-117">倉庫管理プロセス</span><span class="sxs-lookup"><span data-stu-id="764ce-117">Warehouse management processes</span></span>
- <span data-ttu-id="764ce-118">販売注文、返品、移動オーダー、製造オーダー、およびかんばんの元伝票の統合されたサポート</span><span class="sxs-lookup"><span data-stu-id="764ce-118">Integrated support for source documents for sales orders, returns, transfer orders, production orders, and kanban</span></span>  
- <span data-ttu-id="764ce-119">変動、入庫、出庫材料ワークフローサポートはクエリに基づいています</span><span class="sxs-lookup"><span data-stu-id="764ce-119">Flexible, inbound and outbound material workflow support based on queries</span></span>
- <span data-ttu-id="764ce-120">製造、および輸送管理提供との完全な統合</span><span class="sxs-lookup"><span data-stu-id="764ce-120">Full integration with the Manufacturing and Transportation offerings</span></span>
- <span data-ttu-id="764ce-121">在庫限度と場所の容積測定をフルコントロール</span><span class="sxs-lookup"><span data-stu-id="764ce-121">Full control of location stocking limits and location volumetrics</span></span>
- <span data-ttu-id="764ce-122">在庫状態によって管理された在庫プロパティ</span><span class="sxs-lookup"><span data-stu-id="764ce-122">Inventory properties controlled by inventory status</span></span>
- <span data-ttu-id="764ce-123">完全バッチとシリアル品目サポート</span><span class="sxs-lookup"><span data-stu-id="764ce-123">Full batch and serial item support</span></span>
- <span data-ttu-id="764ce-124">さまざまな品目の入荷能力</span><span class="sxs-lookup"><span data-stu-id="764ce-124">Various item receiving capabilities</span></span>
- <span data-ttu-id="764ce-125">積荷の複数ピッキング</span><span class="sxs-lookup"><span data-stu-id="764ce-125">Multiple picking strategies</span></span>
- <span data-ttu-id="764ce-126">次世代バーコード スキャナーのサポート</span><span class="sxs-lookup"><span data-stu-id="764ce-126">Out-of-the-box support for the next generation of barcode scanners</span></span>
- <span data-ttu-id="764ce-127">倉庫プロセスのパレット/コンテナーのタイプ</span><span class="sxs-lookup"><span data-stu-id="764ce-127">Pallet/container types for warehouse processes</span></span>
- <span data-ttu-id="764ce-128">高度な棚卸能力</span><span class="sxs-lookup"><span data-stu-id="764ce-128">Advanced counting capabilities</span></span>
- <span data-ttu-id="764ce-129">Zebra ZPL サポートでラベルの印刷およびラベル ルート指定</span><span class="sxs-lookup"><span data-stu-id="764ce-129">Label printing and label routing with Zebra ZPL support</span></span>
- <span data-ttu-id="764ce-130">ビジネス インテリジェンスの Power BI への統合</span><span class="sxs-lookup"><span data-stu-id="764ce-130">Business intelligence integration into Power BI</span></span>
- <span data-ttu-id="764ce-131">在庫の手動、および自動移動</span><span class="sxs-lookup"><span data-stu-id="764ce-131">Manual and automatic movement of inventory</span></span>
- <span data-ttu-id="764ce-132">完全に統合された品質テスト (QMS)</span><span class="sxs-lookup"><span data-stu-id="764ce-132">Fully-integrated quality control (QMS)</span></span>
- <span data-ttu-id="764ce-133">作業者の材料取り扱いの完全なトレーサビリティ</span><span class="sxs-lookup"><span data-stu-id="764ce-133">Full traceability of workers' material handling</span></span>
- <span data-ttu-id="764ce-134">出荷ウェーブ処理</span><span class="sxs-lookup"><span data-stu-id="764ce-134">Outbound wave processing</span></span>
- <span data-ttu-id="764ce-135">手動の梱包と自動のコンテナ詰めをサポート</span><span class="sxs-lookup"><span data-stu-id="764ce-135">Manual packing and automatic containerization support</span></span>
- <span data-ttu-id="764ce-136">クラスター ピッキング</span><span class="sxs-lookup"><span data-stu-id="764ce-136">Cluster picking</span></span>
- <span data-ttu-id="764ce-137">シンプルクロスドッキング</span><span class="sxs-lookup"><span data-stu-id="764ce-137">Simple cross docking</span></span>

## <a name="additional-resources"></a><span data-ttu-id="764ce-138">追加リソース</span><span class="sxs-lookup"><span data-stu-id="764ce-138">Additional resources</span></span>
### <a name="whats-new-and-in-development"></a><span data-ttu-id="764ce-139">新機能および開発中の機能</span><span class="sxs-lookup"><span data-stu-id="764ce-139">What's new and in development</span></span>
<span data-ttu-id="764ce-140">リリースされた新機能と開発中の新機能については、[Microsoft Dynamics 365 ロードマップ](https://roadmap.dynamics.com/) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="764ce-140">Go to the [Microsoft Dynamics 365 Roadmap](https://roadmap.dynamics.com/) to see what new features have been released and what new features are in development.</span></span>

### <a name="blogs"></a><span data-ttu-id="764ce-141">ブログ</span><span class="sxs-lookup"><span data-stu-id="764ce-141">Blogs</span></span>
<span data-ttu-id="764ce-142">倉庫管理およびその他のソリューションに関する意見、ニュース、その他の情報については、「[Microsoft Dynamics 365 ブログ](https://community.dynamics.com/b/msftdynamicsblog)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="764ce-142">You can find opinions, news, and other information about Warehouse management and other solutions on the [Microsoft Dynamics 365 blog](https://community.dynamics.com/b/msftdynamicsblog).</span></span>


 

