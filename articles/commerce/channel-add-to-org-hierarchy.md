---
title: 組織階層へのチャネルの追加
description: このトピックでは、Microsoft Dynamics 365 Commerce の組織階層にチャネルを追加する方法について説明します。
author: samjarawan
manager: annbe
ms.date: 01/27/2020
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
ms.openlocfilehash: 4212797d2959c4f8b0d60e6b45de76ffc3ee0dc2
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/15/2021
ms.locfileid: "5216758"
---
# <a name="add-a-channel-to-an-organizational-hierarchy"></a><span data-ttu-id="1ef7f-103">組織階層へのチャネルの追加</span><span class="sxs-lookup"><span data-stu-id="1ef7f-103">Add a channel to an organizational hierarchy</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="1ef7f-104">このトピックでは、Microsoft Dynamics 365 Commerce の組織階層にチャネルを追加する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="1ef7f-104">This topic describes how to add a channel to an organizational hierarchy in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="1ef7f-105">概要</span><span class="sxs-lookup"><span data-stu-id="1ef7f-105">Overview</span></span>

<span data-ttu-id="1ef7f-106">チャネルは、1 つ以上の組織階層に関連付けられている必要があります。</span><span class="sxs-lookup"><span data-stu-id="1ef7f-106">Channels need to be associated with one or more organizational hierarchies.</span></span> <span data-ttu-id="1ef7f-107">チャネルを作成する前に、組織階層が設定されていることを確認する必要があります。</span><span class="sxs-lookup"><span data-stu-id="1ef7f-107">Before creating channels, you need to confirm that your organizational hierarchies have been set up.</span></span>  

<span data-ttu-id="1ef7f-108">組織階層の作成方法に関する詳細は、[組織階層](channels-org-hierarchies.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="1ef7f-108">See [Organizational hierarchies](channels-org-hierarchies.md) for more details on how to create organizational hierarchies.</span></span>

## <a name="select-a-hierarchy"></a><span data-ttu-id="1ef7f-109">階層の選択</span><span class="sxs-lookup"><span data-stu-id="1ef7f-109">Select a hierarchy</span></span>

<span data-ttu-id="1ef7f-110">階層を選択するには、次の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="1ef7f-110">To select a hierarchy, follow these steps.</span></span>

1. <span data-ttu-id="1ef7f-111">ナビゲーション ウィンドウで、**モジュール \> Retail と Commerce \> チャネル設定 \> 組織階層** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="1ef7f-111">In the navigation pane, go to **Modules \> Retail and commerce \> Channel Setup \> Organization hierarchies**.</span></span>
1. <span data-ttu-id="1ef7f-112">リストから、チャネルを追加する組織階層を選択します。</span><span class="sxs-lookup"><span data-stu-id="1ef7f-112">From the list, select the organization hierarchy that you'll be adding the channel to.</span></span>
1. <span data-ttu-id="1ef7f-113">アクション ウィンドウで、**表示** を選択して階層の詳細を表示します。</span><span class="sxs-lookup"><span data-stu-id="1ef7f-113">On the action pane, select **View** to view hierarchy details.</span></span>

<span data-ttu-id="1ef7f-114">次の図は、選択した階層の組織階層の詳細を示しています。</span><span class="sxs-lookup"><span data-stu-id="1ef7f-114">The following image shows organizational hierarchy details for the selected hierarchy.</span></span>

![選択した階層の組織階層の詳細](media/channel-add-to-org-hierarchy-1.png)

## <a name="add-a-channel-to-a-hierachy-node"></a><span data-ttu-id="1ef7f-116">階層ノードへのチャネルの追加</span><span class="sxs-lookup"><span data-stu-id="1ef7f-116">Add a channel to a hierachy node</span></span>

<span data-ttu-id="1ef7f-117">階層ノードにチャネルを追加するには、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="1ef7f-117">To add a channel to a hierachy node, follow these steps.</span></span>

1. <span data-ttu-id="1ef7f-118">アクション ウィンドウで、**編集** を選択します。</span><span class="sxs-lookup"><span data-stu-id="1ef7f-118">On the action pane, select **Edit**.</span></span>
1. <span data-ttu-id="1ef7f-119">チャネルを追加する階層ノードを選択し、**挿入** ドロップダウン リストから、**小売チャネル** を選択します。</span><span class="sxs-lookup"><span data-stu-id="1ef7f-119">Select the hierachy node you want the channel added to, then from the **Insert** drop-down list, select **Retail Channel**.</span></span> 
1. <span data-ttu-id="1ef7f-120">追加するチャネルを選択し、**OK** ボタンを選択します。</span><span class="sxs-lookup"><span data-stu-id="1ef7f-120">Select the channel to add, then select the **OK** button.</span></span>
1. <span data-ttu-id="1ef7f-121">アクション ウィンドウで、**保存** を選択します。</span><span class="sxs-lookup"><span data-stu-id="1ef7f-121">On the action pane, select **Save**.</span></span>
1. <span data-ttu-id="1ef7f-122">アクション ウィンドウで、**発行** を選択し、過去の **有効日** を指定して、このアクションを直ちに有効にします。</span><span class="sxs-lookup"><span data-stu-id="1ef7f-122">On the action pane, select **Publish** and provide an **Effective date** in the past to have this action go into effect immediately.</span></span>

<span data-ttu-id="1ef7f-123">次の図は、チャネルを選択して階層ノードに追加する方法を示しています。</span><span class="sxs-lookup"><span data-stu-id="1ef7f-123">The following image shows how to select a channel to add to a hierarchy node.</span></span>

![チャネルを選択して階層ノードを追加する](media/channel-add-to-org-hierarchy-2.png)

<span data-ttu-id="1ef7f-125">次の図は、さまざまなチャネルが追加された階層を示しています。</span><span class="sxs-lookup"><span data-stu-id="1ef7f-125">The following image shows a hierarchy with various channels added.</span></span>

![さまざまなチャネルが追加された階層](media/channel-add-to-org-hierarchy-3.png)

## <a name="additional-resources"></a><span data-ttu-id="1ef7f-127">追加リソース</span><span class="sxs-lookup"><span data-stu-id="1ef7f-127">Additional resources</span></span>

[<span data-ttu-id="1ef7f-128">チャネルの概要</span><span class="sxs-lookup"><span data-stu-id="1ef7f-128">Channels overview</span></span>](channels-overview.md)

[<span data-ttu-id="1ef7f-129">チャネル設定の前提条件</span><span class="sxs-lookup"><span data-stu-id="1ef7f-129">Channel setup prerequisites</span></span>](channels-prerequisites.md)

[<span data-ttu-id="1ef7f-130">組織と組織階層の概要</span><span class="sxs-lookup"><span data-stu-id="1ef7f-130">Organizations and organizational hierarchies overview</span></span>](../fin-ops-core/fin-ops/organization-administration/organizations-organizational-hierarchies.md?toc=/dynamics365/commerce/toc.json)

[<span data-ttu-id="1ef7f-131">組織階層の計画</span><span class="sxs-lookup"><span data-stu-id="1ef7f-131">Plan your organizational hierarchy</span></span>](../fin-ops-core/fin-ops/organization-administration/plan-organizational-hierarchy.md?toc=/dynamics365/commerce/toc.json)

[<span data-ttu-id="1ef7f-132">組織階層</span><span class="sxs-lookup"><span data-stu-id="1ef7f-132">Organization hierarchies</span></span>](channels-org-hierarchies.md)

[<span data-ttu-id="1ef7f-133">小売チャネルの設定</span><span class="sxs-lookup"><span data-stu-id="1ef7f-133">Set up a retail channel</span></span>](channel-setup-retail.md)
    
[<span data-ttu-id="1ef7f-134">オンライン チャネルの設定</span><span class="sxs-lookup"><span data-stu-id="1ef7f-134">Set up an online channel</span></span>](channel-setup-online.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]