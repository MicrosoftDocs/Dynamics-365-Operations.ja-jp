---
title: Retail Modern POS (MPOS) アーキテクチャ
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
ms.openlocfilehash: 223c053e3cada4eb6839cb9a285c41548073be5c
ms.sourcegitcommit: 27a98a7a0f1d2623f5236a88066f483def30889c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/01/2019
ms.locfileid: "1833736"
---
# <a name="retail-modern-pos-mpos-architecture"></a><span data-ttu-id="99e1a-103">Retail Modern POS (MPOS) アーキテクチャ</span><span class="sxs-lookup"><span data-stu-id="99e1a-103">Retail Modern POS (MPOS) architecture</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="99e1a-104">このトピックでは、POS トポロジについて説明します。</span><span class="sxs-lookup"><span data-stu-id="99e1a-104">This topic describes the POS topology.</span></span>

<a name="retail-modern-pos-topology"></a><span data-ttu-id="99e1a-105">Retail Modern POS トポロジー</span><span class="sxs-lookup"><span data-stu-id="99e1a-105">Retail Modern POS topology</span></span>
--------------------------

<span data-ttu-id="99e1a-106">Retail Modern 販売時点管理 (POS) のユーザーは、サポートされているラップトップ、タブレット、および電話上で、さまざまな小売タスクを実行できます。</span><span class="sxs-lookup"><span data-stu-id="99e1a-106">Users of Retail Modern Point of Sale (POS) can perform various retail tasks on supported laptops, tablets, and phones.</span></span> <span data-ttu-id="99e1a-107">これらのタスクには、販売取引の処理、顧客の注文の表示、日常業務と在庫の管理、ロール ベースのレポートの表示などが含まれます。</span><span class="sxs-lookup"><span data-stu-id="99e1a-107">These tasks include processing sales transactions, viewing customer orders, managing daily operations and inventory, and viewing role-based reports.</span></span> <span data-ttu-id="99e1a-108">Retail POS およびクラウド POS の両方は Microsoft Dynamics 365 for Retail で使用できます。</span><span class="sxs-lookup"><span data-stu-id="99e1a-108">Both Retail POS and Cloud POS are available in Microsoft Dynamics 365 for Retail.</span></span>  <span data-ttu-id="99e1a-109">Cloud POS は、POS アプリケーションのホストされているバージョンです。</span><span class="sxs-lookup"><span data-stu-id="99e1a-109">The Cloud POS is a hosted version of the POS app.</span></span> <span data-ttu-id="99e1a-110">両方の POS クライアントは、業務機能またはデータ処理を実行しません。</span><span class="sxs-lookup"><span data-stu-id="99e1a-110">Both the POS clients don't perform business functions or data processing.</span></span> <span data-ttu-id="99e1a-111">すべてのビジネス機能は Retail サーバーにより提供されています。</span><span class="sxs-lookup"><span data-stu-id="99e1a-111">All business functions are provided by Retail Server.</span></span> <span data-ttu-id="99e1a-112">Retail Modern POS および Cloud POS クライアントは、クラウドに配置される Retail サーバーと通信できます。</span><span class="sxs-lookup"><span data-stu-id="99e1a-112">Retail Modern POS and Cloud POS clients can communicate with Retail Servers that are deployed in the cloud.</span></span> <span data-ttu-id="99e1a-113">Retail Modern POS クライアントは、Hardware Station を使用することで、キャッシュ ドロワー、クレジット カード リーダー、プリンタなどの周辺機器とも通信できます。</span><span class="sxs-lookup"><span data-stu-id="99e1a-113">Retail Modern POS client can also communicate with peripheral devices, such as cash drawers, credit card readers, and printers, by using Hardware Station.</span></span> <span data-ttu-id="99e1a-114">ハードウェア ステーションは、店舗内で配置される必要があり、すべての Retail Modern POS クライアントが同じハードウェア ステーションに接続できます。</span><span class="sxs-lookup"><span data-stu-id="99e1a-114">Hardware Station must be deployed in your store, and all Retail Modern POS clients can connect to the same Hardware Station.</span></span> <span data-ttu-id="99e1a-115">次の図は、高レベルのトポロジを示しています。</span><span class="sxs-lookup"><span data-stu-id="99e1a-115">The following diagram shows the high-level topology.</span></span> 

<span data-ttu-id="99e1a-116">[![小売トポロジ](./media/retail-topology-1024x606.png)](./media/retail-topology.png)</span><span class="sxs-lookup"><span data-stu-id="99e1a-116">[![Retail Topology](./media/retail-topology-1024x606.png)](./media/retail-topology.png)</span></span>

## <a name="retail-modern-pos-architecture"></a><span data-ttu-id="99e1a-117">Retail Modern POS のアーキテクチャ</span><span class="sxs-lookup"><span data-stu-id="99e1a-117">Retail Modern POS architecture</span></span>
<span data-ttu-id="99e1a-118">ビュー、ビュー コントローラー、デバイスのレイヤーは、Retail Modern POS を展開する予定のオペレーティング システム (Windows RTなど) によって異なります。</span><span class="sxs-lookup"><span data-stu-id="99e1a-118">The view, view-controller, and devices layers depend on the operating system (for example, Windows RT) that you plan to deploy Retail Modern POS on.</span></span> <span data-ttu-id="99e1a-119">他のレイヤーは、オペレーティング システムとは独立しています。</span><span class="sxs-lookup"><span data-stu-id="99e1a-119">The other layers are independent of the operating system.</span></span> <span data-ttu-id="99e1a-120">これらのレイヤーは、TypeScript のクラスとモジュールを使用して、ワークフローやエンティティなどの Retail Modern POS 機能を実装します。</span><span class="sxs-lookup"><span data-stu-id="99e1a-120">These layers use TypeScript classes and modules to implement Retail Modern POS functionality such as workflows and entities.</span></span> <span data-ttu-id="99e1a-121">次の図は、Retail Modern POS のテクニカル アーキテクチャを示しています。</span><span class="sxs-lookup"><span data-stu-id="99e1a-121">The following diagram shows the Retail Modern POS technical architecture.</span></span> 

<span data-ttu-id="99e1a-122">[![MPOS](./media/mpos.png)](./media/mpos.png)</span><span class="sxs-lookup"><span data-stu-id="99e1a-122">[![MPOS](./media/mpos.png)](./media/mpos.png)</span></span>

## <a name="cloud-pos-and-retail-modern-pos-architecture"></a><span data-ttu-id="99e1a-123">クラウド POS および Retail Modern POS アーキテクチャ</span><span class="sxs-lookup"><span data-stu-id="99e1a-123">Cloud POS and Retail Modern POS architecture</span></span>
<span data-ttu-id="99e1a-124">Cloud POS は、Retail Modern POS のホストされたバージョンであり、特定のデバイスまたは特定のブラウザでレンダリングされる方法のみが異なります。</span><span class="sxs-lookup"><span data-stu-id="99e1a-124">Cloud POS is a hosted version of Retail Modern POS, and varies only in the way that it is rendered on specific devices or in specific browsers.</span></span> <span data-ttu-id="99e1a-125">また、Retail Modern POS は、オフライン モードをサポートしており、したがってローカル CRT です。</span><span class="sxs-lookup"><span data-stu-id="99e1a-125">Additionally, Retail Modern POS supports offline mode and therefore a local CRT.</span></span> <span data-ttu-id="99e1a-126">その他のネイティブ周辺機器のサポートは、Retail Modern POS に固有です。</span><span class="sxs-lookup"><span data-stu-id="99e1a-126">Other native peripheral support is also specific to Retail Modern POS.</span></span> 

<span data-ttu-id="99e1a-127">[![CloudPOS および MPOS](./media/cloudpos-and-mpos.png)](./media/cloudpos-and-mpos.png)</span><span class="sxs-lookup"><span data-stu-id="99e1a-127">[![CloudPOS and MPOS](./media/cloudpos-and-mpos.png)](./media/cloudpos-and-mpos.png)</span></span>



