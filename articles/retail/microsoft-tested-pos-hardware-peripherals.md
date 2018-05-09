---
title: "POS ハードウェアおよび周辺機器"
description: "Retail Modern POS (販売時点管理) およびクラウド POS では、複数のインターフェイスとデプロイ オプションにより、小売業者のさまざまな取引シナリオに合わせて、POS ハードウェア周辺機器を活用できます。"
author: jblucher
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
audience: Application User, IT Pro
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 215234
ms.assetid: 1893d4b3-e1b7-4b66-be58-0102addd5b36
ms.search.region: global
ms.search.industry: Retail
ms.author: jeffbl
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: 250ab6570e152ad57b4a590203e9321d89e7b5d1
ms.contentlocale: ja-jp
ms.lasthandoff: 05/08/2018

---

# <a name="pos-hardware-peripherals"></a><span data-ttu-id="cd1a3-103">POS ハードウェアおよび周辺機器</span><span class="sxs-lookup"><span data-stu-id="cd1a3-103">POS hardware peripherals</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="cd1a3-104">Retail Modern POS (販売時点管理) およびクラウド POS では、複数のインターフェイスとデプロイ オプションにより、小売業者のさまざまな取引シナリオに合わせて、POS ハードウェア周辺機器を活用できます。</span><span class="sxs-lookup"><span data-stu-id="cd1a3-104">Retail Modern point of sale (POS) and Cloud POS can utilize a wide range of POS hardware peripherals, with multiple interfaces and deployment options to achieve a retailer’s various business scenarios.</span></span> 

<span data-ttu-id="cd1a3-105">メーカーやモデルを超えて幅広いデバイスをサポートするため、POS は、OLE for Retail (OPOS)、Windows デバイス ドライバ、Windows ポイント オブ サービス アプリケーション プログラム インターフェイスなどの標準インターフェイスを使用しています。</span><span class="sxs-lookup"><span data-stu-id="cd1a3-105">To support the widest selection of devices across manufactures and models, POS utilizes standard interfaces such as OLE for Retail POS (OPOS), Windows device drivers, and Windows point of service application program interfaces (APIs).</span></span> <span data-ttu-id="cd1a3-106">通常、POS は、適切なドライバがあれば、これらのデバイスで機能します。</span><span class="sxs-lookup"><span data-stu-id="cd1a3-106">Generally, POS will work on these devices provided that the appropriate driver is supplied.</span></span> <span data-ttu-id="cd1a3-107">ただし、各メーカーやソフトウェア開発者がこれらの標準を実装する方法は異なるため、多くの場合、サポートされる機能やの動作が異なります。</span><span class="sxs-lookup"><span data-stu-id="cd1a3-107">However, because each manufacturer and software developer’s implementation of these standards can vary, there are often differences in supported capabilities or behaviors.</span></span>

<span data-ttu-id="cd1a3-108">次のリストでは Microsoft が内部テストしたデバイス モデルがクラスごとに示されています。</span><span class="sxs-lookup"><span data-stu-id="cd1a3-108">The following list includes device models, in each class, that have been tested internally by Microsoft.</span></span>

<span data-ttu-id="cd1a3-109">**OPOS デバイス**</span><span class="sxs-lookup"><span data-stu-id="cd1a3-109">**OPOS devices**</span></span>

-   <span data-ttu-id="cd1a3-110">バーコード – Motorola DS9208</span><span class="sxs-lookup"><span data-stu-id="cd1a3-110">Barcode – Motorola DS9208</span></span>
-   <span data-ttu-id="cd1a3-111">MSR – HP IDRA-334133、Magtek PN - 21073062</span><span class="sxs-lookup"><span data-stu-id="cd1a3-111">MSR – HP IDRA-334133, Magtek PN - 21073062</span></span>
-   <span data-ttu-id="cd1a3-112">LineDisplay – Epson M58DC</span><span class="sxs-lookup"><span data-stu-id="cd1a3-112">LineDisplay – Epson M58DC</span></span>
-   <span data-ttu-id="cd1a3-113">Pinpad – Verifone 1000SE</span><span class="sxs-lookup"><span data-stu-id="cd1a3-113">Pinpad – Verifone 1000SE</span></span>
-   <span data-ttu-id="cd1a3-114">Signature pad – Scriptel ST1550</span><span class="sxs-lookup"><span data-stu-id="cd1a3-114">Signature pad – Scriptel ST1550</span></span>
-   <span data-ttu-id="cd1a3-115">プリンター – EPSON TM-T88IV、TMT88V</span><span class="sxs-lookup"><span data-stu-id="cd1a3-115">Printer – EPSON TM-T88IV, TMT88V</span></span>
-   <span data-ttu-id="cd1a3-116">キャッシュ ドロワー – Star SMD2-1317BK44</span><span class="sxs-lookup"><span data-stu-id="cd1a3-116">Cash drawer – Star SMD2-1317BK44</span></span>
-   <span data-ttu-id="cd1a3-117">スケール – Datalogic Magellan 8400</span><span class="sxs-lookup"><span data-stu-id="cd1a3-117">Scale – Datalogic Magellan 8400</span></span>

<span data-ttu-id="cd1a3-118">**キーボード ウェッジ MSR**</span><span class="sxs-lookup"><span data-stu-id="cd1a3-118">**Keyboard wedge MSR**</span></span>

-   <span data-ttu-id="cd1a3-119">Magtek USB</span><span class="sxs-lookup"><span data-stu-id="cd1a3-119">Magtek USB</span></span>

<span data-ttu-id="cd1a3-120">**支払ターミナル**</span><span class="sxs-lookup"><span data-stu-id="cd1a3-120">**Payment terminal**</span></span>

-   <span data-ttu-id="cd1a3-121">Equinox L3500</span><span class="sxs-lookup"><span data-stu-id="cd1a3-121">Equinox L3500</span></span>
-   <span data-ttu-id="cd1a3-122">Verifone MX925</span><span class="sxs-lookup"><span data-stu-id="cd1a3-122">Verifone MX925</span></span>

<span data-ttu-id="cd1a3-123">**ネットワーク デバイス**</span><span class="sxs-lookup"><span data-stu-id="cd1a3-123">**Network devices**</span></span>

-   <span data-ttu-id="cd1a3-124">プリンター – Star TSP650II</span><span class="sxs-lookup"><span data-stu-id="cd1a3-124">Printer – Star TSP650II</span></span>
-   <span data-ttu-id="cd1a3-125">キャッシュ ドロワー – APG Atwood</span><span class="sxs-lookup"><span data-stu-id="cd1a3-125">Cash drawer – APG Atwood</span></span>
-   <span data-ttu-id="cd1a3-126">支払ターミナル – MX915、MX925</span><span class="sxs-lookup"><span data-stu-id="cd1a3-126">Payment terminal – MX915, MX925</span></span>

<span data-ttu-id="cd1a3-127">**MPOS ダイレクト IPC のみ**</span><span class="sxs-lookup"><span data-stu-id="cd1a3-127">**MPOS direct IPC only**</span></span>

-   <span data-ttu-id="cd1a3-128">バーコード – Honeywell 1900、HP LS2208</span><span class="sxs-lookup"><span data-stu-id="cd1a3-128">Barcode – Honeywell 1900, HP LS2208</span></span>
-   <span data-ttu-id="cd1a3-129">MSR – Magtek PN - 21073075</span><span class="sxs-lookup"><span data-stu-id="cd1a3-129">MSR – Magtek PN - 21073075</span></span>





