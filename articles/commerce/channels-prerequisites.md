---
title: チャネル設定の前提条件
description: このトピックでは、Microsoft Dynamics 365 Commerce のチャネル設定の前提条件における概要を示します。
author: samjarawan
manager: annbe
ms.date: 01/27/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: samjar
ms.search.validFrom: 2020-01-20
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: b861d90f1333c8f6e61a83602ed74e30b65f3dc1
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/01/2020
ms.locfileid: "3002292"
---
# <a name="channel-setup-prerequisites"></a><span data-ttu-id="e4554-103">チャネル設定の前提条件</span><span class="sxs-lookup"><span data-stu-id="e4554-103">Channel setup prerequisites</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="e4554-104">このトピックでは、Microsoft Dynamics 365 Commerce のチャネル設定の前提条件における概要を示します。</span><span class="sxs-lookup"><span data-stu-id="e4554-104">This topic presents an overview of channel setup prerequisites in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="e4554-105">概要</span><span class="sxs-lookup"><span data-stu-id="e4554-105">Overview</span></span>

<span data-ttu-id="e4554-106">Dynamics 365 Commerce チャネルを作成する前に、いくつかの前提条件タスクを完了しておく必要があります。</span><span class="sxs-lookup"><span data-stu-id="e4554-106">Before a Dynamics 365 Commerce channel can be created, several prerequisite tasks must be completed.</span></span> <span data-ttu-id="e4554-107">次の前提条件タスクの一覧は、チャネル タイプ別にまとめられています。</span><span class="sxs-lookup"><span data-stu-id="e4554-107">The following lists of prerequisite tasks are organized by channel type.</span></span>

> [!NOTE]
> <span data-ttu-id="e4554-108">一部のドキュメントはまだ作成中であり、新しいコンテンツが公開されるとリンクは更新されます。</span><span class="sxs-lookup"><span data-stu-id="e4554-108">Some documentation is still being written, and links will be updated as new content is published.</span></span>

## <a name="initialization"></a><span data-ttu-id="e4554-109">初期化</span><span class="sxs-lookup"><span data-stu-id="e4554-109">Initialization</span></span>

- [<span data-ttu-id="e4554-110">シード データの初期化</span><span class="sxs-lookup"><span data-stu-id="e4554-110">Initialize seed data</span></span>](../retail/enable-configure-retail-functionality.md)

## <a name="global-prerequisities-required-for-all-channel-types"></a><span data-ttu-id="e4554-111">すべてのチャネル タイプに必要であるグローバルな前提条件</span><span class="sxs-lookup"><span data-stu-id="e4554-111">Global prerequisities required for all channel types</span></span>

- [<span data-ttu-id="e4554-112">法人構造の定義とコンフィギュレーション</span><span class="sxs-lookup"><span data-stu-id="e4554-112">Define and configure your legal entity structure</span></span>](channels-legal-entities.md) 
- [<span data-ttu-id="e4554-113">組織階層のコンフィギュレーション</span><span class="sxs-lookup"><span data-stu-id="e4554-113">Configure your organizational hierarchy</span></span>](channels-org-hierarchies.md)
- [<span data-ttu-id="e4554-114">倉庫の設定</span><span class="sxs-lookup"><span data-stu-id="e4554-114">Set up a warehouse</span></span>](channels-setup-warehouse.md)
- [<span data-ttu-id="e4554-115">消費税のコンフィギュレーション</span><span class="sxs-lookup"><span data-stu-id="e4554-115">Configure sales tax</span></span>](https://docs.microsoft.com/en-us/dynamics365/finance/general-ledger/indirect-taxes-overview?toc=/dynamics365/commerce/toc.json)
- [<span data-ttu-id="e4554-116">電子メール通知プロファイルの設定</span><span class="sxs-lookup"><span data-stu-id="e4554-116">Set up an email notification profile</span></span>](email-notification-profiles.md)
- [<span data-ttu-id="e4554-117">番号順序の設定</span><span class="sxs-lookup"><span data-stu-id="e4554-117">Set up number sequences</span></span>](https://docs.microsoft.com/en-us/dynamics365/fin-ops-core/fin-ops/organization-administration/number-sequence-overview?toc=/dynamics365/commerce/toc.json)
- [<span data-ttu-id="e4554-118">既定の顧客およびアドレス帳の設定</span><span class="sxs-lookup"><span data-stu-id="e4554-118">Set up a default customer and address book</span></span>](default-customer.md)
<!--
- [Configure commerce parameters](commerce-parameters.md)
-->

## <a name="retail-channel-prerequisites"></a><span data-ttu-id="e4554-119">小売チャネルの前提条件</span><span class="sxs-lookup"><span data-stu-id="e4554-119">Retail channel prerequisites</span></span>

- [<span data-ttu-id="e4554-120">情報コードおよび情報コード グループ</span><span class="sxs-lookup"><span data-stu-id="e4554-120">Info codes and info code groups</span></span>](https://docs.microsoft.com/en-us/dynamics365/retail/info-codes-retail?toc=/dynamics365/commerce/toc.json)
- [<span data-ttu-id="e4554-121">小売機能プロファイルの設定</span><span class="sxs-lookup"><span data-stu-id="e4554-121">Set up a retail functionality profile</span></span>](retail-functionality-profile.md)
- [<span data-ttu-id="e4554-122">従業員のアドレス帳の設定</span><span class="sxs-lookup"><span data-stu-id="e4554-122">Set up an employee address book</span></span>](new-address-book.md)
- [<span data-ttu-id="e4554-123">画面レイアウトの設定</span><span class="sxs-lookup"><span data-stu-id="e4554-123">Set up a screen layout</span></span>](https://docs.microsoft.com/en-us/dynamics365/retail/pos-screen-layouts?toc=/dynamics365/commerce/toc.json)
- [<span data-ttu-id="e4554-124">ハードウェア ステーションの設定</span><span class="sxs-lookup"><span data-stu-id="e4554-124">Set up a hardware station</span></span>](https://docs.microsoft.com/en-us/dynamics365/retail/retail-hardware-station-configuration-installation?toc=/dynamics365/commerce/toc.json)

## <a name="call-center-channel-prerequisites"></a><span data-ttu-id="e4554-125">コール センター チャネルの前提条件</span><span class="sxs-lookup"><span data-stu-id="e4554-125">Call Center channel prerequisites</span></span>

- <span data-ttu-id="e4554-126">コール センター パラメーター</span><span class="sxs-lookup"><span data-stu-id="e4554-126">Call center parameters</span></span>
- <span data-ttu-id="e4554-127">コール センターの払戻方法</span><span class="sxs-lookup"><span data-stu-id="e4554-127">Call center refund methods</span></span>
- <span data-ttu-id="e4554-128">レンタル タイプ</span><span class="sxs-lookup"><span data-stu-id="e4554-128">Rental types</span></span>
- <span data-ttu-id="e4554-129">支払サービス</span><span class="sxs-lookup"><span data-stu-id="e4554-129">Payment services</span></span>
- <span data-ttu-id="e4554-130">注文保留コード</span><span class="sxs-lookup"><span data-stu-id="e4554-130">Order hold codes</span></span>

## <a name="online-channel-prerequisites"></a><span data-ttu-id="e4554-131">オンライン チャネルの前提条件</span><span class="sxs-lookup"><span data-stu-id="e4554-131">Online channel prerequisites</span></span>

- [<span data-ttu-id="e4554-132">オンライン機能プロファイルの作成</span><span class="sxs-lookup"><span data-stu-id="e4554-132">Create an online functionality profile</span></span>](online-functionality-profile.md)

## <a name="additional-resources"></a><span data-ttu-id="e4554-133">追加リソース</span><span class="sxs-lookup"><span data-stu-id="e4554-133">Additional resources</span></span>

[<span data-ttu-id="e4554-134">チャネルの概要</span><span class="sxs-lookup"><span data-stu-id="e4554-134">Channels overview</span></span>](channels-overview.md)

[<span data-ttu-id="e4554-135">組織と組織階層の概要</span><span class="sxs-lookup"><span data-stu-id="e4554-135">Organizations and organizational hierarchies overview</span></span>](../fin-ops-core/fin-ops/organization-administration/organizations-organizational-hierarchies.md?toc=/dynamics365/commerce/toc.json)

[<span data-ttu-id="e4554-136">組織階層の設定</span><span class="sxs-lookup"><span data-stu-id="e4554-136">Set up organization hierarchies</span></span>](channels-org-hierarchies.md)

[<span data-ttu-id="e4554-137">法人の作成</span><span class="sxs-lookup"><span data-stu-id="e4554-137">Create legal entities</span></span>](channels-legal-entities.md)

[<span data-ttu-id="e4554-138">小売チャネルの設定</span><span class="sxs-lookup"><span data-stu-id="e4554-138">Set up a retail channel</span></span>](channel-setup-retail.md)
    
[<span data-ttu-id="e4554-139">オンライン チャネルの設定</span><span class="sxs-lookup"><span data-stu-id="e4554-139">Set up an online channel</span></span>](channel-setup-online.md)
