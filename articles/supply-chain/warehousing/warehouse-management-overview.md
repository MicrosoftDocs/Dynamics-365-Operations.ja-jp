---
title: 倉庫管理概要
description: 倉庫プロセスを監視および自動化するために、倉庫管理を使用します。
author: ShylaThompson
manager: AnnBe
ms.date: 07/25/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSParameters
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: c900ef715b62484c1fb6576b7f0c97cdea4e4284
ms.sourcegitcommit: e286572ce94a9442a5b3076c3ff5b429be0ed512
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/06/2019
ms.locfileid: "1865139"
---
# <a name="warehouse-management-overview"></a><span data-ttu-id="6fe33-103">倉庫管理概要</span><span class="sxs-lookup"><span data-stu-id="6fe33-103">Warehouse management overview</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="6fe33-104">Dynamics 365 for Finance and Operations の倉庫管理モジュールは、製造、配送、および小売企業の倉庫プロセスを管理できます。</span><span class="sxs-lookup"><span data-stu-id="6fe33-104">The Warehouse management module for Dynamics 365 for Finance and Operations lets you manage warehouse processes in manufacturing, distribution, and retail companies.</span></span> <span data-ttu-id="6fe33-105">このモジュールは、倉庫施設をいつでも最適なレベルにサポートする幅広い機能を持っています。</span><span class="sxs-lookup"><span data-stu-id="6fe33-105">This module has a wide range of features to support the warehouse facility at an optimal level, at any time.</span></span> <span data-ttu-id="6fe33-106">倉庫管理は、輸送、製造、品質テスト、購買、移動、販売、返品などの他のビジネス プロセスが Finance and Operations で完全に統合されます。</span><span class="sxs-lookup"><span data-stu-id="6fe33-106">Warehouse management is fully integrated with other business processes in Finance and Operations such as transportation, manufacturing, quality control, purchase, transfer, sales, and returns.</span></span>

## <a name="get-started"></a><span data-ttu-id="6fe33-107">使用開始</span><span class="sxs-lookup"><span data-stu-id="6fe33-107">Get started</span></span>
<span data-ttu-id="6fe33-108">倉庫管理の操作を開始するには、会社の業務プロセスをサポートするための通常倉庫のパラメーターの設定を完了する必要があります。</span><span class="sxs-lookup"><span data-stu-id="6fe33-108">To start working with Warehouse management, you need to complete the setup of the general warehouse parameters to support the business processes of you company.</span></span>

- <span data-ttu-id="6fe33-109">**倉庫管理** > **設定**ページ下の**倉庫管理パラメーター**に移動し、通常倉庫のパラメーターの設定をします。</span><span class="sxs-lookup"><span data-stu-id="6fe33-109">Go to the **Warehouse management parameters** page under **Warehouse management** > **Setup** to set up general warehouse parameters.</span></span>

<span data-ttu-id="6fe33-110">業務要件に従って入庫/出庫の倉庫プロセスワークフローをコンフィギュレーションする必要があります。</span><span class="sxs-lookup"><span data-stu-id="6fe33-110">You must configure components for inbound and outbound warehouse process workflows according to business requirements.</span></span> <span data-ttu-id="6fe33-111">コンフィギュレーションする必要がある最も重要なコンポーネントは、ウェーブ テンプレート、作業テンプレート、作業プールと場所のディレクティブです。</span><span class="sxs-lookup"><span data-stu-id="6fe33-111">The most important components that you must configure are wave templates, work templates, work pools, and location directives.</span></span>

- [<span data-ttu-id="6fe33-112">倉庫のコンフィギュレーション</span><span class="sxs-lookup"><span data-stu-id="6fe33-112">Warehouse configuration</span></span>](warehouse-configuration.md)
- [<span data-ttu-id="6fe33-113">作業テンプレートと場所ディレクティブを使用した倉庫作業の制御</span><span class="sxs-lookup"><span data-stu-id="6fe33-113">Control warehouse work by using work templates and location directives</span></span>](control-warehouse-location-directives.md)
- [<span data-ttu-id="6fe33-114">倉庫作業用のモバイル デバイスの設定</span><span class="sxs-lookup"><span data-stu-id="6fe33-114">Set up mobile devices for warehouse work</span></span>](configure-mobile-devices-warehouse.md)
- [<span data-ttu-id="6fe33-115">発注書のプット アウェイ場所のディレクティブの設定</span><span class="sxs-lookup"><span data-stu-id="6fe33-115">Set up a location directive for purchase order put-away</span></span>](../transportation/tasks/set-up-location-directive-purchase-order-put-away.md)
- [<span data-ttu-id="6fe33-116">発注書の作業テンプレートの設定</span><span class="sxs-lookup"><span data-stu-id="6fe33-116">Set up a work template for purchase orders</span></span>](./tasks/set-up-work-template-purchase-orders.md)

## <a name="warehouse-management-processes"></a><span data-ttu-id="6fe33-117">倉庫管理プロセス</span><span class="sxs-lookup"><span data-stu-id="6fe33-117">Warehouse management processes</span></span>
- <span data-ttu-id="6fe33-118">販売注文、返品、移動オーダー、製造オーダー、およびかんばんの元伝票の統合されたサポート</span><span class="sxs-lookup"><span data-stu-id="6fe33-118">Integrated support for source documents for sales orders, returns, transfer orders, production orders, and kanban</span></span>  
- <span data-ttu-id="6fe33-119">変動、入庫、出庫材料ワークフローサポートはクエリに基づいています</span><span class="sxs-lookup"><span data-stu-id="6fe33-119">Flexible, inbound and outbound material workflow support based on queries</span></span>
- <span data-ttu-id="6fe33-120">製造、および輸送管理提供との完全な統合</span><span class="sxs-lookup"><span data-stu-id="6fe33-120">Full integration with the Manufacturing and Transportation offerings</span></span>
- <span data-ttu-id="6fe33-121">在庫限度と場所の容積測定をフルコントロール</span><span class="sxs-lookup"><span data-stu-id="6fe33-121">Full control of location stocking limits and location volumetrics</span></span>
- <span data-ttu-id="6fe33-122">在庫状態によって管理された在庫プロパティ</span><span class="sxs-lookup"><span data-stu-id="6fe33-122">Inventory properties controlled by inventory status</span></span>
- <span data-ttu-id="6fe33-123">完全バッチとシリアル品目サポート</span><span class="sxs-lookup"><span data-stu-id="6fe33-123">Full batch and serial item support</span></span>
- <span data-ttu-id="6fe33-124">さまざまな品目の入荷能力</span><span class="sxs-lookup"><span data-stu-id="6fe33-124">Various item receiving capabilities</span></span>
- <span data-ttu-id="6fe33-125">積荷の複数ピッキング</span><span class="sxs-lookup"><span data-stu-id="6fe33-125">Multiple picking strategies</span></span>
- <span data-ttu-id="6fe33-126">次世代バーコード スキャナーのサポート</span><span class="sxs-lookup"><span data-stu-id="6fe33-126">Out-of-the-box support for the next generation of barcode scanners</span></span>
- <span data-ttu-id="6fe33-127">倉庫プロセスのパレット/コンテナーのタイプ</span><span class="sxs-lookup"><span data-stu-id="6fe33-127">Pallet/container types for warehouse processes</span></span>
- <span data-ttu-id="6fe33-128">高度な棚卸能力</span><span class="sxs-lookup"><span data-stu-id="6fe33-128">Advanced counting capabilities</span></span>
- <span data-ttu-id="6fe33-129">Zebra ZPL サポートでラベルの印刷およびラベル ルート指定</span><span class="sxs-lookup"><span data-stu-id="6fe33-129">Label printing and label routing with Zebra ZPL support</span></span>
- <span data-ttu-id="6fe33-130">ビジネス インテリジェンスの Power BI への統合</span><span class="sxs-lookup"><span data-stu-id="6fe33-130">Business intelligence integration into Power BI</span></span>
- <span data-ttu-id="6fe33-131">在庫の手動、および自動移動</span><span class="sxs-lookup"><span data-stu-id="6fe33-131">Manual and automatic movement of inventory</span></span>
- <span data-ttu-id="6fe33-132">完全に統合された品質テスト (QMS)</span><span class="sxs-lookup"><span data-stu-id="6fe33-132">Fully-integrated quality control (QMS)</span></span>
- <span data-ttu-id="6fe33-133">作業者の材料取り扱いの完全なトレーサビリティ</span><span class="sxs-lookup"><span data-stu-id="6fe33-133">Full traceability of workers' material handling</span></span>
- <span data-ttu-id="6fe33-134">出荷ウェーブ処理</span><span class="sxs-lookup"><span data-stu-id="6fe33-134">Outbound wave processing</span></span>
- <span data-ttu-id="6fe33-135">手動の梱包と自動のコンテナ詰めをサポート</span><span class="sxs-lookup"><span data-stu-id="6fe33-135">Manual packing and automatic containerization support</span></span>
- <span data-ttu-id="6fe33-136">クラスター ピッキング</span><span class="sxs-lookup"><span data-stu-id="6fe33-136">Cluster picking</span></span>
- <span data-ttu-id="6fe33-137">シンプルクロスドッキング</span><span class="sxs-lookup"><span data-stu-id="6fe33-137">Simple cross docking</span></span>

## <a name="additional-resources"></a><span data-ttu-id="6fe33-138">追加リソース</span><span class="sxs-lookup"><span data-stu-id="6fe33-138">Additional resources</span></span>
### <a name="whats-new-and-in-development"></a><span data-ttu-id="6fe33-139">新機能および開発中の機能</span><span class="sxs-lookup"><span data-stu-id="6fe33-139">What's new and in development</span></span>
<span data-ttu-id="6fe33-140">リリースされた新機能と開発中の新機能については、[Microsoft Dynamics 365 ロードマップ](https://roadmap.dynamics.com/) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="6fe33-140">Go to the [Microsoft Dynamics 365 Roadmap](https://roadmap.dynamics.com/) to see what new features have been released and what new features are in development.</span></span>

### <a name="blogs"></a><span data-ttu-id="6fe33-141">ブログ</span><span class="sxs-lookup"><span data-stu-id="6fe33-141">Blogs</span></span>
<span data-ttu-id="6fe33-142">倉庫管理およびその他のソリューションに関する意見、ニュース、その他の情報については、「[Microsoft Dynamics 365 ブログ](https://community.dynamics.com/b/msftdynamicsblog)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="6fe33-142">You can find opinions, news, and other information about Warehouse management and other solutions on the [Microsoft Dynamics 365 blog](https://community.dynamics.com/b/msftdynamicsblog).</span></span>


 

