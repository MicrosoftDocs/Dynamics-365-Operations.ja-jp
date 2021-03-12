---
title: チャネル設定の前提条件
description: このトピックでは、Microsoft Dynamics 365 Commerce のチャネル設定の前提条件における概要を示します。
author: samjarawan
manager: annbe
ms.date: 02/21/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: samjar
ms.search.validFrom: 2020-01-20
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: 0705efac4659f96ebca1c67f6f0ab8d23c99d81e
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/15/2021
ms.locfileid: "4997703"
---
# <a name="channel-setup-prerequisites"></a><span data-ttu-id="7c677-103">チャネル設定の前提条件</span><span class="sxs-lookup"><span data-stu-id="7c677-103">Channel setup prerequisites</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="7c677-104">このトピックでは、Microsoft Dynamics 365 Commerce のチャネル設定の前提条件における概要を示します。</span><span class="sxs-lookup"><span data-stu-id="7c677-104">This topic presents an overview of channel setup prerequisites in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="7c677-105">概要</span><span class="sxs-lookup"><span data-stu-id="7c677-105">Overview</span></span>

<span data-ttu-id="7c677-106">Dynamics 365 Commerce チャネルを作成する前に、いくつかの前提条件タスクを完了しておく必要があります。</span><span class="sxs-lookup"><span data-stu-id="7c677-106">Before a Dynamics 365 Commerce channel can be created, several prerequisite tasks must be completed.</span></span> <span data-ttu-id="7c677-107">次の前提条件タスクの一覧は、チャネル タイプ別にまとめられています。</span><span class="sxs-lookup"><span data-stu-id="7c677-107">The following lists of prerequisite tasks are organized by channel type.</span></span>

> [!NOTE]
> <span data-ttu-id="7c677-108">一部のドキュメントはまだ作成中であり、新しいコンテンツが公開されるとリンクは更新されます。</span><span class="sxs-lookup"><span data-stu-id="7c677-108">Some documentation is still being written, and links will be updated as new content is published.</span></span>

## <a name="initialization"></a><span data-ttu-id="7c677-109">初期化</span><span class="sxs-lookup"><span data-stu-id="7c677-109">Initialization</span></span>

- [<span data-ttu-id="7c677-110">シード データの初期化</span><span class="sxs-lookup"><span data-stu-id="7c677-110">Initialize seed data</span></span>](enable-configure-retail-functionality.md)

## <a name="global-prerequisities-required-for-all-channel-types"></a><span data-ttu-id="7c677-111">すべてのチャネル タイプに必要であるグローバルな前提条件</span><span class="sxs-lookup"><span data-stu-id="7c677-111">Global prerequisities required for all channel types</span></span>

- [<span data-ttu-id="7c677-112">法人構造の定義とコンフィギュレーション</span><span class="sxs-lookup"><span data-stu-id="7c677-112">Define and configure your legal entity structure</span></span>](channels-legal-entities.md) 
- [<span data-ttu-id="7c677-113">組織階層のコンフィギュレーション</span><span class="sxs-lookup"><span data-stu-id="7c677-113">Configure your organizational hierarchy</span></span>](channels-org-hierarchies.md)
- [<span data-ttu-id="7c677-114">倉庫の設定</span><span class="sxs-lookup"><span data-stu-id="7c677-114">Set up a warehouse</span></span>](channels-setup-warehouse.md)
- [<span data-ttu-id="7c677-115">消費税のコンフィギュレーション</span><span class="sxs-lookup"><span data-stu-id="7c677-115">Configure sales tax</span></span>](../finance/general-ledger/indirect-taxes-overview.md?toc=/dynamics365/commerce/toc.json)
- [<span data-ttu-id="7c677-116">電子メール通知プロファイルの設定</span><span class="sxs-lookup"><span data-stu-id="7c677-116">Set up an email notification profile</span></span>](email-notification-profiles.md)
- [<span data-ttu-id="7c677-117">番号順序の設定</span><span class="sxs-lookup"><span data-stu-id="7c677-117">Set up number sequences</span></span>](../fin-ops-core/fin-ops/organization-administration/number-sequence-overview.md?toc=/dynamics365/commerce/toc.json)
- [<span data-ttu-id="7c677-118">既定の顧客およびアドレス帳の設定</span><span class="sxs-lookup"><span data-stu-id="7c677-118">Set up a default customer and address book</span></span>](default-customer.md)
<!--
- [Configure commerce parameters](commerce-parameters.md)
-->

## <a name="retail-channel-prerequisites"></a><span data-ttu-id="7c677-119">小売チャネルの前提条件</span><span class="sxs-lookup"><span data-stu-id="7c677-119">Retail channel prerequisites</span></span>

- [<span data-ttu-id="7c677-120">情報コードおよび情報コード グループ</span><span class="sxs-lookup"><span data-stu-id="7c677-120">Info codes and info code groups</span></span>](info-codes-retail.md)
- [<span data-ttu-id="7c677-121">小売機能プロファイルの設定</span><span class="sxs-lookup"><span data-stu-id="7c677-121">Set up a retail functionality profile</span></span>](retail-functionality-profile.md)
- [<span data-ttu-id="7c677-122">従業員のアドレス帳の設定</span><span class="sxs-lookup"><span data-stu-id="7c677-122">Set up an employee address book</span></span>](new-address-book.md)
- [<span data-ttu-id="7c677-123">画面レイアウトの設定</span><span class="sxs-lookup"><span data-stu-id="7c677-123">Set up a screen layout</span></span>](pos-screen-layouts.md)
- [<span data-ttu-id="7c677-124">ハードウェア ステーションの設定</span><span class="sxs-lookup"><span data-stu-id="7c677-124">Set up a hardware station</span></span>](retail-hardware-station-configuration-installation.md)

## <a name="call-center-channel-prerequisites"></a><span data-ttu-id="7c677-125">コール センター チャネルの前提条件</span><span class="sxs-lookup"><span data-stu-id="7c677-125">Call Center channel prerequisites</span></span>

- <span data-ttu-id="7c677-126">コール センター パラメーター</span><span class="sxs-lookup"><span data-stu-id="7c677-126">Call center parameters</span></span>
- [<span data-ttu-id="7c677-127">通話センター注文と払戻支払の方法</span><span class="sxs-lookup"><span data-stu-id="7c677-127">Call center order and refund payment methods</span></span>](work-with-payments.md)
- [<span data-ttu-id="7c677-128">デリバリーのコール センター モードと諸費用</span><span class="sxs-lookup"><span data-stu-id="7c677-128">Call center modes of delivery and charges</span></span>](configure-call-center-delivery.md)

## <a name="online-channel-prerequisites"></a><span data-ttu-id="7c677-129">オンライン チャネルの前提条件</span><span class="sxs-lookup"><span data-stu-id="7c677-129">Online channel prerequisites</span></span>

- [<span data-ttu-id="7c677-130">オンライン機能プロファイルの作成</span><span class="sxs-lookup"><span data-stu-id="7c677-130">Create an online functionality profile</span></span>](online-functionality-profile.md)

## <a name="additional-resources"></a><span data-ttu-id="7c677-131">追加リソース</span><span class="sxs-lookup"><span data-stu-id="7c677-131">Additional resources</span></span>

[<span data-ttu-id="7c677-132">チャネルの概要</span><span class="sxs-lookup"><span data-stu-id="7c677-132">Channels overview</span></span>](channels-overview.md)

[<span data-ttu-id="7c677-133">組織と組織階層の概要</span><span class="sxs-lookup"><span data-stu-id="7c677-133">Organizations and organizational hierarchies overview</span></span>](../fin-ops-core/fin-ops/organization-administration/organizations-organizational-hierarchies.md?toc=/dynamics365/commerce/toc.json)

[<span data-ttu-id="7c677-134">組織階層の設定</span><span class="sxs-lookup"><span data-stu-id="7c677-134">Set up organization hierarchies</span></span>](channels-org-hierarchies.md)

[<span data-ttu-id="7c677-135">法人の作成</span><span class="sxs-lookup"><span data-stu-id="7c677-135">Create legal entities</span></span>](channels-legal-entities.md)

[<span data-ttu-id="7c677-136">小売チャネルの設定</span><span class="sxs-lookup"><span data-stu-id="7c677-136">Set up a retail channel</span></span>](channel-setup-retail.md)
    
[<span data-ttu-id="7c677-137">オンライン チャネルの設定</span><span class="sxs-lookup"><span data-stu-id="7c677-137">Set up an online channel</span></span>](channel-setup-online.md)
