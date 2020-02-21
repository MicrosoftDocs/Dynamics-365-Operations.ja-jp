---
title: Modern POS (MPOS) アーキテクチャ
description: このトピックでは、POS トポロジについて説明します。
author: RobinARH
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Developer
ms.reviewer: rhaertle
ms.search.scope: Operations, Retail
ms.custom: 83892
ms.assetid: 210953fb-4d5a-49e6-b4db-6f31b3472789
ms.search.region: Global
ms.author: meeram
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: 5334d88ab583c0a66598e50d6710130298a2e58e
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/01/2020
ms.locfileid: "3004640"
---
# <a name="modern-pos-mpos-architecture"></a><span data-ttu-id="127cf-103">Modern POS (MPOS) アーキテクチャ</span><span class="sxs-lookup"><span data-stu-id="127cf-103">Modern POS (MPOS) architecture</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="127cf-104">このトピックでは、POS トポロジについて説明します。</span><span class="sxs-lookup"><span data-stu-id="127cf-104">This topic describes the POS topology.</span></span>

<a name="modern-pos-topology"></a><span data-ttu-id="127cf-105">Modern POS トポロジ</span><span class="sxs-lookup"><span data-stu-id="127cf-105">Modern POS topology</span></span>
--------------------------

<span data-ttu-id="127cf-106">Modern 販売時点管理 (POS) のユーザーは、サポートされているラップトップ、タブレット、および電話上で、さまざまなタスクを実行できます。</span><span class="sxs-lookup"><span data-stu-id="127cf-106">Users of Modern Point of Sale (POS) can perform various tasks on supported laptops, tablets, and phones.</span></span> <span data-ttu-id="127cf-107">これらのタスクには、販売取引の処理、顧客の注文の表示、日常業務と在庫の管理、ロール ベースのレポートの表示などが含まれます。</span><span class="sxs-lookup"><span data-stu-id="127cf-107">These tasks include processing sales transactions, viewing customer orders, managing daily operations and inventory, and viewing role-based reports.</span></span> <span data-ttu-id="127cf-108">MPOS および Cloud POS の両方は Microsoft Dynamics 365 Commerce で使用できます。</span><span class="sxs-lookup"><span data-stu-id="127cf-108">Both MPOS and Cloud POS are available in Microsoft Dynamics 365 Commerce.</span></span> <span data-ttu-id="127cf-109">Cloud POS は、POS アプリケーションのホストされているバージョンです。</span><span class="sxs-lookup"><span data-stu-id="127cf-109">The Cloud POS is a hosted version of the POS app.</span></span> <span data-ttu-id="127cf-110">両方の POS クライアントは、業務機能またはデータ処理を実行しません。</span><span class="sxs-lookup"><span data-stu-id="127cf-110">Both the POS clients don't perform business functions or data processing.</span></span> <span data-ttu-id="127cf-111">すべてのビジネス機能は、Commerce Scale Unit によって提供されます。</span><span class="sxs-lookup"><span data-stu-id="127cf-111">All business functions are provided by Commerce Scale Unit.</span></span> <span data-ttu-id="127cf-112">Modern POS および Cloud POS クライアントは、クラウドに配置される Commerce Scale Unit と通信できます。</span><span class="sxs-lookup"><span data-stu-id="127cf-112">Modern POS and Cloud POS clients can communicate with Commerce Scale Units that are deployed in the cloud.</span></span> <span data-ttu-id="127cf-113">Modern POS クライアントは、Hardware Station を使用することで、キャッシュ ドロワー、クレジット カード リーダー、プリンタなどの周辺機器とも通信できます。</span><span class="sxs-lookup"><span data-stu-id="127cf-113">Modern POS client can also communicate with peripheral devices, such as cash drawers, credit card readers, and printers, by using Hardware Station.</span></span> <span data-ttu-id="127cf-114">Hardware Station は、店舗内で配置される必要があり、すべての Modern POS クライアントが同じ Hardware Station に接続できます。</span><span class="sxs-lookup"><span data-stu-id="127cf-114">Hardware Station must be deployed in your store, and all Modern POS clients can connect to the same Hardware Station.</span></span> <span data-ttu-id="127cf-115">次の図は、高レベルのトポロジを示しています。</span><span class="sxs-lookup"><span data-stu-id="127cf-115">The following diagram shows the high-level topology.</span></span> 

<span data-ttu-id="127cf-116">[![コマース トポロジ](./media/retail-topology-1024x606.png)](./media/retail-topology.png)</span><span class="sxs-lookup"><span data-stu-id="127cf-116">[![Commerce Topology](./media/retail-topology-1024x606.png)](./media/retail-topology.png)</span></span>

## <a name="modern-pos-architecture"></a><span data-ttu-id="127cf-117">Modern POS アーキテクチャ</span><span class="sxs-lookup"><span data-stu-id="127cf-117">Modern POS architecture</span></span>
<span data-ttu-id="127cf-118">ビュー、ビュー コントローラー、デバイスのレイヤーは、Modern POS を展開する予定のオペレーティング システム (Windows RT など) によって異なります。</span><span class="sxs-lookup"><span data-stu-id="127cf-118">The view, view-controller, and devices layers depend on the operating system (for example, Windows RT) that you plan to deploy Modern POS on.</span></span> <span data-ttu-id="127cf-119">他のレイヤーは、オペレーティング システムとは独立しています。</span><span class="sxs-lookup"><span data-stu-id="127cf-119">The other layers are independent of the operating system.</span></span> <span data-ttu-id="127cf-120">これらのレイヤーは、TypeScript のクラスとモジュールを使用して、ワークフローやエンティティなどの Modern POS 機能を実装します。</span><span class="sxs-lookup"><span data-stu-id="127cf-120">These layers use TypeScript classes and modules to implement Modern POS functionality such as workflows and entities.</span></span> <span data-ttu-id="127cf-121">次の図は、Modern POS のテクニカル アーキテクチャを示しています。</span><span class="sxs-lookup"><span data-stu-id="127cf-121">The following diagram shows the Modern POS technical architecture.</span></span> 

<span data-ttu-id="127cf-122">[![MPOS](./media/mpos.png)](./media/mpos.png)</span><span class="sxs-lookup"><span data-stu-id="127cf-122">[![MPOS](./media/mpos.png)](./media/mpos.png)</span></span>

## <a name="cloud-pos-and-modern-pos-architecture"></a><span data-ttu-id="127cf-123">Cloud POS および Modern POS アーキテクチャ</span><span class="sxs-lookup"><span data-stu-id="127cf-123">Cloud POS and Modern POS architecture</span></span>
<span data-ttu-id="127cf-124">Cloud POS は、Modern POS のホストされたバージョンであり、特定のデバイスまたは特定のブラウザでレンダリングされる方法のみが異なります。</span><span class="sxs-lookup"><span data-stu-id="127cf-124">Cloud POS is a hosted version of Modern POS, and varies only in the way that it is rendered on specific devices or in specific browsers.</span></span> <span data-ttu-id="127cf-125">また、Modern POS は、オフライン モードをサポートしており、したがってローカル CRT です。</span><span class="sxs-lookup"><span data-stu-id="127cf-125">Additionally, Modern POS supports offline mode and therefore a local CRT.</span></span> <span data-ttu-id="127cf-126">その他のネイティブ周辺機器のサポートは、Modern POS に固有です。</span><span class="sxs-lookup"><span data-stu-id="127cf-126">Other native peripheral support is also specific to Modern POS.</span></span> 

<span data-ttu-id="127cf-127">[![CloudPOS および MPOS](./media/cloudpos-and-mpos.png)](./media/cloudpos-and-mpos.png)</span><span class="sxs-lookup"><span data-stu-id="127cf-127">[![CloudPOS and MPOS](./media/cloudpos-and-mpos.png)](./media/cloudpos-and-mpos.png)</span></span>



