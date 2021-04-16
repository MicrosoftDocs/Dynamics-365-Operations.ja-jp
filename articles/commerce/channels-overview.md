---
title: チャネルの概要
description: このトピックでは、Microsoft Dynamics 365 Commerce のチャネルの概要を表示します。
author: samjarawan
ms.date: 01/27/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: samjar
ms.search.validFrom: 2020-01-20
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: 7f5d527dd14d24c06aef874de0088bb07c49849b
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/31/2021
ms.locfileid: "5800546"
---
# <a name="channels-overview"></a><span data-ttu-id="61655-103">チャネルの概要</span><span class="sxs-lookup"><span data-stu-id="61655-103">Channels overview</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="61655-104">このトピックでは、Microsoft Dynamics 365 Commerce のチャネルの概要を表示します。</span><span class="sxs-lookup"><span data-stu-id="61655-104">This topic presents an overview of channels in Microsoft Dynamics 365 Commerce.</span></span> <span data-ttu-id="61655-105">ここでは、各チャネルを設定する前と後の、実施する必要のあるタスクについて説明します。</span><span class="sxs-lookup"><span data-stu-id="61655-105">It includes information about the tasks that you must complete both before and after you set up each channel.</span></span>

## <a name="types-of-channels"></a><span data-ttu-id="61655-106">チャネルのタイプ</span><span class="sxs-lookup"><span data-stu-id="61655-106">Types of Channels</span></span>

<span data-ttu-id="61655-107">Dynamics 365 Commerce は、小売、コール センター、およびオンライン チャネルという 3 つのチャネル タイプがサポートされています。</span><span class="sxs-lookup"><span data-stu-id="61655-107">Dynamics 365 Commerce supports three different channel types: retail, call center, and online channels.</span></span>

### <a name="retail-channels"></a><span data-ttu-id="61655-108">小売チャネル</span><span class="sxs-lookup"><span data-stu-id="61655-108">Retail channels</span></span>

<span data-ttu-id="61655-109">小売チャネルは、従来型の店舗を表します。</span><span class="sxs-lookup"><span data-stu-id="61655-109">Retail channels represent standard brick-and-mortar stores.</span></span> <span data-ttu-id="61655-110">各店舗は、独自の販売時点管理 (POS)、収入/経費勘定、およびスタッフを持つことができます。</span><span class="sxs-lookup"><span data-stu-id="61655-110">Each store can have its own point of sale (POS) registers, income and expense accounts, and staff.</span></span> 

### <a name="call-center-channels"></a><span data-ttu-id="61655-111">コール センター チャネル</span><span class="sxs-lookup"><span data-stu-id="61655-111">Call center channels</span></span>

<span data-ttu-id="61655-112">コール センター チャネルは、コール センターの注文と顧客管理を表します。</span><span class="sxs-lookup"><span data-stu-id="61655-112">Call center channels represent call center order and customer management.</span></span>

### <a name="online-channels"></a><span data-ttu-id="61655-113">オンライン チャネル</span><span class="sxs-lookup"><span data-stu-id="61655-113">Online channels</span></span>

<span data-ttu-id="61655-114">オンライン チャネルは、オンライン電子商取引店舗を表します。</span><span class="sxs-lookup"><span data-stu-id="61655-114">Online channels represent online e-Commerce storefronts.</span></span> <span data-ttu-id="61655-115">オンライン チャネルを作成した後、Microsoft Dynamics 365 Commerce サイト ビルダー ツールまたはその他のサードパーティの電子商取引ソリューションを使用してサイトを作成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="61655-115">Once an online channel is created, a site must be created using the Microsoft Dynamics 365 Commerce Site Builder tool or other third-party e-Commerce solution.</span></span>

## <a name="channel-setup-basics"></a><span data-ttu-id="61655-116">チャネル設定の基本</span><span class="sxs-lookup"><span data-stu-id="61655-116">Channel setup basics</span></span>

<span data-ttu-id="61655-117">チャネルの設定は、Commerce ツールで実行されます。</span><span class="sxs-lookup"><span data-stu-id="61655-117">Channel set up is performed in the Commerce tool.</span></span> <span data-ttu-id="61655-118">各チャネルごとに、独自の支払方法、価格グループ、製品階層、品揃え、および一連の製品を設定できます。</span><span class="sxs-lookup"><span data-stu-id="61655-118">Each channel can have its own payment methods, price groups, product hierarchies, assortments, and set of products.</span></span> <span data-ttu-id="61655-119">チャネルを作成したら、そのチャネルで配送および販売する製品を割り当てます。</span><span class="sxs-lookup"><span data-stu-id="61655-119">After you create a channel, you assign the products that you want it to carry and sell.</span></span> <span data-ttu-id="61655-120">チャネル タイプごとに、コンフィギュレーションする必要がある固有の機能セットがあります。</span><span class="sxs-lookup"><span data-stu-id="61655-120">Each channel type has a unique set of features that may need to be configured.</span></span> <span data-ttu-id="61655-121">たとえば、小売チャネルには従業員、レジスター、および顧客が割り当てられている必要があります。</span><span class="sxs-lookup"><span data-stu-id="61655-121">For example, a retail channel needs assigned employees, registers, and customers.</span></span> <span data-ttu-id="61655-122">新しいチャネルを作成したら、それを組織階層に割り当てる必要があります。</span><span class="sxs-lookup"><span data-stu-id="61655-122">Once a new channel is created, it needs to be assigned to an organization hierarchy.</span></span>

## <a name="channel-setup-prerequisites"></a><span data-ttu-id="61655-123">チャネル設定の前提条件</span><span class="sxs-lookup"><span data-stu-id="61655-123">Channel setup prerequisites</span></span>

<span data-ttu-id="61655-124">チャネルを設定する前に、チャネル タイプに基づいていくつかの前提条件タスクを完了しておく必要があります。</span><span class="sxs-lookup"><span data-stu-id="61655-124">Before you can set up a channel, you must complete some prerequisite tasks based on the channel type.</span></span> <span data-ttu-id="61655-125">詳細については、[チャネル設定の前提条件](channels-prerequisites.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="61655-125">For more information, see [Channel setup prerequisites](channels-prerequisites.md).</span></span>

## <a name="set-up-a-channel"></a><span data-ttu-id="61655-126">チャネルの設定</span><span class="sxs-lookup"><span data-stu-id="61655-126">Set up a channel</span></span>

<span data-ttu-id="61655-127">前提条件のタスクを完了した後、セットアップ手順の詳細については、次のリンクを使用してください。</span><span class="sxs-lookup"><span data-stu-id="61655-127">After you complete the prerequisite tasks, for further setup instructions, use the following links.</span></span>

- [<span data-ttu-id="61655-128">小売チャネルの設定</span><span class="sxs-lookup"><span data-stu-id="61655-128">Set up a retail channel</span></span>](channel-setup-retail.md)
- [<span data-ttu-id="61655-129">コール センターのチャネルの設定</span><span class="sxs-lookup"><span data-stu-id="61655-129">Set up a call center channel</span></span>](channel-setup-callcenter.md)
- [<span data-ttu-id="61655-130">オンライン チャネルの設定</span><span class="sxs-lookup"><span data-stu-id="61655-130">Set up an online channel</span></span>](channel-setup-online.md)

<!--
## Post-channel configuration

After you create a channel, you may need to complete some of the below tasks:

- [Add channel to an organizational hierarchy](add-channel-org-hierarchy.md)
- Set up fulfillment groups. (LINK TBD)
- Configure the POS registers for the store. (LINK TBD)
- Assign product assortments to the store. (LINK TBD)
- Process assortments to generate the list of products that are included in the assortment and to make the products available in the retail store. (LINK TBD)
- Send data such as number sequences, hardware profiles, and POS screen layouts to the Retail POS registers.(LINK TBD)
- Publish the retail store to send store data to Retail POS. (LINK TBD)
- Run the jobs to send the store data to Retail POS. (LINK TBD)
-->

## <a name="additional-resources"></a><span data-ttu-id="61655-131">追加リソース</span><span class="sxs-lookup"><span data-stu-id="61655-131">Additional resources</span></span>

[<span data-ttu-id="61655-132">チャネル設定の前提条件</span><span class="sxs-lookup"><span data-stu-id="61655-132">Channel setup prerequisites</span></span>](channels-prerequisites.md)

[<span data-ttu-id="61655-133">小売チャネルの設定</span><span class="sxs-lookup"><span data-stu-id="61655-133">Set up a retail channel</span></span>](channel-setup-retail.md)
    
[<span data-ttu-id="61655-134">オンライン チャネルの設定</span><span class="sxs-lookup"><span data-stu-id="61655-134">Set up an online channel</span></span>](channel-setup-online.md)

[<span data-ttu-id="61655-135">コール センターのチャネルの設定</span><span class="sxs-lookup"><span data-stu-id="61655-135">Set up a call center channel</span></span>](channel-setup-callcenter.md)

[<span data-ttu-id="61655-136">組織階層の設定</span><span class="sxs-lookup"><span data-stu-id="61655-136">Set up organization hierarchies</span></span>](channels-org-hierarchies.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]