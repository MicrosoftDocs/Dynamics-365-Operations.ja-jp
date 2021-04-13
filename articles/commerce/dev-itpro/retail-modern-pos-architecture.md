---
title: Modern POS (MPOS) アーキテクチャ
description: このトピックでは、POS トポロジについて説明します。
author: RobinARH
ms.date: 06/02/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Developer
ms.reviewer: rhaertle
ms.custom: 83892
ms.assetid: 210953fb-4d5a-49e6-b4db-6f31b3472789
ms.search.region: Global
ms.author: meeram
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: e0f3d96aa95065b58667a7aac3adf59aa8cf2e4e
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/31/2021
ms.locfileid: "5794329"
---
# <a name="modern-pos-mpos-architecture"></a><span data-ttu-id="540dd-103">Modern POS (MPOS) アーキテクチャ</span><span class="sxs-lookup"><span data-stu-id="540dd-103">Modern POS (MPOS) architecture</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="540dd-104">このトピックでは、POS トポロジについて説明します。</span><span class="sxs-lookup"><span data-stu-id="540dd-104">This topic describes the POS topology.</span></span>

## <a name="modern-pos-topology"></a><span data-ttu-id="540dd-105">Modern POS トポロジ</span><span class="sxs-lookup"><span data-stu-id="540dd-105">Modern POS topology</span></span>

<span data-ttu-id="540dd-106">Modern 販売時点管理 (POS) のユーザーは、サポートされているラップトップ、タブレット、および電話上で、さまざまなタスクを実行できます。</span><span class="sxs-lookup"><span data-stu-id="540dd-106">Users of Modern Point of Sale (POS) can perform various tasks on supported laptops, tablets, and phones.</span></span> <span data-ttu-id="540dd-107">これらのタスクには、販売取引の処理、顧客の注文の表示、日常業務と在庫の管理、ロール ベースのレポートの表示などが含まれます。</span><span class="sxs-lookup"><span data-stu-id="540dd-107">These tasks include processing sales transactions, viewing customer orders, managing daily operations and inventory, and viewing role-based reports.</span></span> <span data-ttu-id="540dd-108">MPOS および Cloud POS の両方は Microsoft Dynamics 365 Commerce で使用できます。</span><span class="sxs-lookup"><span data-stu-id="540dd-108">Both MPOS and Cloud POS are available in Microsoft Dynamics 365 Commerce.</span></span> <span data-ttu-id="540dd-109">Cloud POS は、POS アプリケーションのホストされているバージョンです。</span><span class="sxs-lookup"><span data-stu-id="540dd-109">The Cloud POS is a hosted version of the POS app.</span></span> <span data-ttu-id="540dd-110">両方の POS クライアントは、業務機能またはデータ処理を実行しません。</span><span class="sxs-lookup"><span data-stu-id="540dd-110">Both the POS clients don't perform business functions or data processing.</span></span> <span data-ttu-id="540dd-111">すべてのビジネス機能は、Commerce Scale Unit によって提供されます。</span><span class="sxs-lookup"><span data-stu-id="540dd-111">All business functions are provided by Commerce Scale Unit.</span></span> <span data-ttu-id="540dd-112">Modern POS および Cloud POS クライアントは、Commerce Scale Unit と通信できます。</span><span class="sxs-lookup"><span data-stu-id="540dd-112">Modern POS and Cloud POS clients can communicate with Commerce Scale Units.</span></span> <span data-ttu-id="540dd-113">Modern POS クライアントは、Hardware Station を使用することで、キャッシュ ドロワー、クレジット カード リーダー、プリンタなどの周辺機器とも通信できます。</span><span class="sxs-lookup"><span data-stu-id="540dd-113">Modern POS client can also communicate with peripheral devices, such as cash drawers, credit card readers, and printers, by using Hardware Station.</span></span> <span data-ttu-id="540dd-114">Hardware Station は、店舗内で配置される必要があり、すべての Modern POS クライアントが同じ Hardware Station に接続できます。</span><span class="sxs-lookup"><span data-stu-id="540dd-114">Hardware Station must be deployed in your store, and all Modern POS clients can connect to the same Hardware Station.</span></span> <span data-ttu-id="540dd-115">次の図は、高レベルのトポロジを示しています。</span><span class="sxs-lookup"><span data-stu-id="540dd-115">The following diagram shows the high-level topology.</span></span>

![コマース トポロジ](./media/retail-topology-1024x606.png)

## <a name="modern-pos-architecture"></a><span data-ttu-id="540dd-117">Modern POS アーキテクチャ</span><span class="sxs-lookup"><span data-stu-id="540dd-117">Modern POS architecture</span></span>

<span data-ttu-id="540dd-118">ビュー、ビュー コントローラー、デバイスのレイヤーは、Modern POS を展開する予定のオペレーティング システム (Windows RT など) によって異なります。</span><span class="sxs-lookup"><span data-stu-id="540dd-118">The view, view-controller, and devices layers depend on the operating system (for example, Windows RT) that you plan to deploy Modern POS on.</span></span> <span data-ttu-id="540dd-119">他のレイヤーは、オペレーティング システムとは独立しています。</span><span class="sxs-lookup"><span data-stu-id="540dd-119">The other layers are independent of the operating system.</span></span> <span data-ttu-id="540dd-120">これらのレイヤーは、TypeScript のクラスとモジュールを使用して、ワークフローやエンティティなどの Modern POS 機能を実装します。</span><span class="sxs-lookup"><span data-stu-id="540dd-120">These layers use TypeScript classes and modules to implement Modern POS functionality such as workflows and entities.</span></span> <span data-ttu-id="540dd-121">次の図は、Modern POS のテクニカル アーキテクチャを示しています。</span><span class="sxs-lookup"><span data-stu-id="540dd-121">The following diagram shows the Modern POS technical architecture.</span></span>

![Modern POS アーキテクチャ](./media/mpos.png)

## <a name="cloud-pos-and-modern-pos-architecture"></a><span data-ttu-id="540dd-123">Cloud POS および Modern POS アーキテクチャ</span><span class="sxs-lookup"><span data-stu-id="540dd-123">Cloud POS and Modern POS architecture</span></span>

<span data-ttu-id="540dd-124">Cloud POS は、Modern POS のホストされたバージョンであり、特定のデバイスまたは特定のブラウザでレンダリングされる方法のみが異なります。</span><span class="sxs-lookup"><span data-stu-id="540dd-124">Cloud POS is a hosted version of Modern POS, and varies only in the way that it is rendered on specific devices or in specific browsers.</span></span> <span data-ttu-id="540dd-125">また、Modern POS は、オフライン モードをサポートしており、したがってローカル CRT です。</span><span class="sxs-lookup"><span data-stu-id="540dd-125">Additionally, Modern POS supports offline mode and therefore a local CRT.</span></span> <span data-ttu-id="540dd-126">その他のネイティブ周辺機器のサポートは、Modern POS に固有です。</span><span class="sxs-lookup"><span data-stu-id="540dd-126">Other native peripheral support is also specific to Modern POS.</span></span>

![CloudPOS および MPOS](./media/cloudpos-and-mpos.png)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]