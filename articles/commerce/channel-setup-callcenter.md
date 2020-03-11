---
title: コール センターのチャネルの設定
description: このトピックでは、Microsoft Dynamics 365 Commerce に新しいコール センター チャネルを作成する方法について説明します。
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
ms.openlocfilehash: 42448bd54c00b8642b158f422e17d2b46ee25579
ms.sourcegitcommit: 12b9d6f2dd24e52e46487748c848864909af6967
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/14/2020
ms.locfileid: "3057882"
---
# <a name="set-up-a-call-center-channel"></a><span data-ttu-id="afd71-103">コール センターのチャネルの設定</span><span class="sxs-lookup"><span data-stu-id="afd71-103">Set up a call center channel</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="afd71-104">このトピックでは、Microsoft Dynamics 365 Commerce に新しいコール センター チャネルを作成する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="afd71-104">This topic describes how to create a new call center channel in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="afd71-105">概要</span><span class="sxs-lookup"><span data-stu-id="afd71-105">Overview</span></span>

<span data-ttu-id="afd71-106">Dynamics 365 Commerce では、コール センターはアプリケーションで定義できるチャネルのタイプです。</span><span class="sxs-lookup"><span data-stu-id="afd71-106">In Dynamics 365 Commerce, a call center is a type of channel that can be defined in the application.</span></span> <span data-ttu-id="afd71-107">コール センター エンティティのチャネルを定義すると、システムによって特定のデータと注文処理の既定値を販売注文に関連付けることができます。</span><span class="sxs-lookup"><span data-stu-id="afd71-107">Defining a channel for your call center entities allows the system to tie specific data and order processing defaults to sales orders.</span></span> <span data-ttu-id="afd71-108">会社では、Commerce の複数のコール センター チャネルを定義できます。</span><span class="sxs-lookup"><span data-stu-id="afd71-108">A company can define multiple call center channels in Commerce.</span></span> 

<span data-ttu-id="afd71-109">新しいコール センター チャネルを作成する前に、[チャネル設定の前提条件](channels-prerequisites.md) を完了していることを確認してください。</span><span class="sxs-lookup"><span data-stu-id="afd71-109">Before you create a new call center channel, ensure that you have completed the [Channel set up prerequisites](channels-prerequisites.md).</span></span>

## <a name="create-and-configure-a-new-call-center-channel"></a><span data-ttu-id="afd71-110">新しいコール センター チャネルを作成およびコンフィギュレーションする</span><span class="sxs-lookup"><span data-stu-id="afd71-110">Create and configure a new call center channel</span></span>

<span data-ttu-id="afd71-111">新しいコール センター チャネルを作成してコンフィギュレーションするには、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="afd71-111">To create and configure a new call center channel, follow these steps.</span></span>

1. <span data-ttu-id="afd71-112">ナビゲーション ウィンドウで、**モジュール \> チャネル \> コール センター \> すべてのコール センター**の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="afd71-112">In the navigation pane, go to **Modules \> Channels \> Call centers \> All call centers**.</span></span>
1. <span data-ttu-id="afd71-113">アクション ウィンドウで、**新規**を選択します。</span><span class="sxs-lookup"><span data-stu-id="afd71-113">On the action pane, select **New**.</span></span>
1. <span data-ttu-id="afd71-114">**名前**フィールドで、新しいチャネルの名前を指定します。</span><span class="sxs-lookup"><span data-stu-id="afd71-114">In the **Name** field, provide a name for the new channel.</span></span>
1. <span data-ttu-id="afd71-115">ドロップ ダウンから適切な**法人**を選択します。</span><span class="sxs-lookup"><span data-stu-id="afd71-115">Select the appropriate **Legal entity** from the drop down.</span></span>
1. <span data-ttu-id="afd71-116">ドロップ ダウンから適切な**倉庫**の場所を選択します。</span><span class="sxs-lookup"><span data-stu-id="afd71-116">Select the appropriate **Warehouse** location from the drop down.</span></span>
1. <span data-ttu-id="afd71-117">**既定の顧客**フィールドで、有効な既定の顧客を指定します。</span><span class="sxs-lookup"><span data-stu-id="afd71-117">In the **Default customer** field, provide a valid default customer.</span></span>
1. <span data-ttu-id="afd71-118">**電子メール通知プロファイル** フィールドに、有効な電子メール通知プロファイルを指定します。</span><span class="sxs-lookup"><span data-stu-id="afd71-118">In the **Email notification profile** field, provide a valid email notification profile.</span></span>
1. <span data-ttu-id="afd71-119">**価格上書き**の情報コードを指定します。</span><span class="sxs-lookup"><span data-stu-id="afd71-119">Provide a **Price override** info code.</span></span> <span data-ttu-id="afd71-120">このために、最初に情報コードを作成する必要があることに注意してください。</span><span class="sxs-lookup"><span data-stu-id="afd71-120">Note you may need to create an info code for this first.</span></span>
1. <span data-ttu-id="afd71-121">**保留コード**の情報コードを指定します。</span><span class="sxs-lookup"><span data-stu-id="afd71-121">Provide a **Hold code** info code.</span></span> <span data-ttu-id="afd71-122">このために、最初に情報コードを作成する必要があることに注意してください。</span><span class="sxs-lookup"><span data-stu-id="afd71-122">Note you may need to create an info code for this first.</span></span>
1. <span data-ttu-id="afd71-123">**クレジット**の情報コードを指定します。</span><span class="sxs-lookup"><span data-stu-id="afd71-123">Provide a **Credit** info code.</span></span> <span data-ttu-id="afd71-124">このために、最初に情報コードを作成する必要があることに注意してください。</span><span class="sxs-lookup"><span data-stu-id="afd71-124">Note you may need to create an info code for this first.</span></span>
1. <span data-ttu-id="afd71-125">**保存** を選択します。</span><span class="sxs-lookup"><span data-stu-id="afd71-125">Select **Save**.</span></span>

<span data-ttu-id="afd71-126">次の図は、新しいコール センター チャネルの作成を示しています。</span><span class="sxs-lookup"><span data-stu-id="afd71-126">The following image shows the creation of a new call center channel.</span></span>

![新しいコール センター チャネル](media/channel-setup-callcenter-1.png)

<span data-ttu-id="afd71-128">次の図は、コール センター チャネルの例を示しています。</span><span class="sxs-lookup"><span data-stu-id="afd71-128">The following image shows an example call center channel.</span></span>

![コール センター チャネルの例](media/channel-setup-callcenter-2.png)

## <a name="additional-channel-setup"></a><span data-ttu-id="afd71-130">追加のチャネル設定</span><span class="sxs-lookup"><span data-stu-id="afd71-130">Additional channel setup</span></span>

<span data-ttu-id="afd71-131">コール センター チャネルの設定に必要な追加タスクには、支払方法および荷渡方法の設定が含まれています。</span><span class="sxs-lookup"><span data-stu-id="afd71-131">Additional tasks required for call center channel setup include setting up payment methods and modes of delivery.</span></span>

<span data-ttu-id="afd71-132">次の図は、**設定**タブの**荷渡方法**および**支払方法**の設定オプションを示しています。</span><span class="sxs-lookup"><span data-stu-id="afd71-132">The following image shows **Modes of delivery** and **Payment methods** set up options on the **Set up** tab.</span></span>

![追加のコール センター チャネル設定アクション](media/channel-setup-callcenter-3.png)

### <a name="set-up-payment-methods"></a><span data-ttu-id="afd71-134">支払方法の設定</span><span class="sxs-lookup"><span data-stu-id="afd71-134">Set up payment methods</span></span>

<span data-ttu-id="afd71-135">支払方法を設定するには、このチャネルでサポートされている各支払タイプに対して、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="afd71-135">To set up payment methods, for each payment type supported on this channel follow these steps.</span></span>

1. <span data-ttu-id="afd71-136">アクション ウィンドウで、**設定**タブを選択して、**支払方法**を選択します。</span><span class="sxs-lookup"><span data-stu-id="afd71-136">On the action pane, select the **Set up** tab, and then select **Payment methods**.</span></span>
1. <span data-ttu-id="afd71-137">アクション ウィンドウで、**新規**を選択します。</span><span class="sxs-lookup"><span data-stu-id="afd71-137">On the action pane, select **New**.</span></span>
1. <span data-ttu-id="afd71-138">ナビゲーション ウィンドウで、目的の支払方法を選択します。</span><span class="sxs-lookup"><span data-stu-id="afd71-138">In the navigation pane, select a desired payment method.</span></span>
1. <span data-ttu-id="afd71-139">**全般**セクションで、**操作名**を指定し、その他の必要な設定を構成します。</span><span class="sxs-lookup"><span data-stu-id="afd71-139">In the **General** section, provide an **Operation name** and configure any other desired settings.</span></span>
1. <span data-ttu-id="afd71-140">支払タイプに必要に応じて追加の設定を構成します。</span><span class="sxs-lookup"><span data-stu-id="afd71-140">Configure any additional settings as required for the payment type.</span></span>
1. <span data-ttu-id="afd71-141">アクション ウィンドウで、**保存**を選択します。</span><span class="sxs-lookup"><span data-stu-id="afd71-141">On the action pane, select **Save**.</span></span>

<span data-ttu-id="afd71-142">次の図は、現金支払い方法の例を示しています。</span><span class="sxs-lookup"><span data-stu-id="afd71-142">The following image shows an example of a cash payment method.</span></span>

![支払方法の例](media/channel-setup-retail-5.png)

### <a name="set-up-modes-of-delivery"></a><span data-ttu-id="afd71-144">荷渡方法の設定</span><span class="sxs-lookup"><span data-stu-id="afd71-144">Set up modes of delivery</span></span>

<span data-ttu-id="afd71-145">構成されたデリバリー モードは、**アクション ウィンドウ**の**設定**タブで**デリバリー モード**を選択することによって確認できます。</span><span class="sxs-lookup"><span data-stu-id="afd71-145">You can see the configured modes of delivery by selecting **Modes of delivery** from the **Set up** tab on the **Action pane**.</span></span>  

<span data-ttu-id="afd71-146">デリバリー モードを変更または追加するには、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="afd71-146">To change or add a mode of delivery, follow these steps.</span></span>

1. <span data-ttu-id="afd71-147">ナビゲーション ウィンドウで、**モジュール \> 在庫管理 \> デリバリー モード**に移動します。</span><span class="sxs-lookup"><span data-stu-id="afd71-147">In the navigation pane, go to **Modules \> Inventory management \> Modes of delivery**.</span></span>
1. <span data-ttu-id="afd71-148">アクション ウィンドウで、**新規**を選択して新しいデリバリー モードを作成するか、既存のモードを選択します。</span><span class="sxs-lookup"><span data-stu-id="afd71-148">On the action pane, select **New** to create a new mode of delivery, or select an existing mode.</span></span>
1. <span data-ttu-id="afd71-149">**小売チャネル** セクションで、**行の追加**を選択してチャネルを追加します。</span><span class="sxs-lookup"><span data-stu-id="afd71-149">In the **Retail channels** section, select **Add line** to add the channel.</span></span> <span data-ttu-id="afd71-150">各チャネルを個別に追加する代わりに、組織ノードを使用してチャネルを追加すると、チャネルの追加を効率化できます。</span><span class="sxs-lookup"><span data-stu-id="afd71-150">Adding channels using organization nodes instead of adding each channel individually can streamline adding channels.</span></span>

<span data-ttu-id="afd71-151">次の図は、デリバリー モードの例を示しています。</span><span class="sxs-lookup"><span data-stu-id="afd71-151">The following image shows an example of a mode of delivery.</span></span>

![荷渡方法の設定](media/channel-setup-retail-7.png)

## <a name="additional-resources"></a><span data-ttu-id="afd71-153">追加リソース</span><span class="sxs-lookup"><span data-stu-id="afd71-153">Additional resources</span></span>

[<span data-ttu-id="afd71-154">チャネル設定の前提条件</span><span class="sxs-lookup"><span data-stu-id="afd71-154">Channel setup prerequisites</span></span>](channels-prerequisites.md)

[<span data-ttu-id="afd71-155">コール センターの販売機能</span><span class="sxs-lookup"><span data-stu-id="afd71-155">Call center sales functionality</span></span>](call-center-functionality.md)

[<span data-ttu-id="afd71-156">コール センターの注文処理オプションの設定</span><span class="sxs-lookup"><span data-stu-id="afd71-156">Set up call center order processing options</span></span>](set-up-order-processing-options.md)

[<span data-ttu-id="afd71-157">コール センターのカタログ</span><span class="sxs-lookup"><span data-stu-id="afd71-157">Call center catalogs</span></span>](call-center-catalogs.md)

[<span data-ttu-id="afd71-158">詐欺警告の設定および使用</span><span class="sxs-lookup"><span data-stu-id="afd71-158">Set up and work with fraud alerts</span></span>](set-up-fraud-alerts.md)

[<span data-ttu-id="afd71-159">コール センターの連続プログラムの設定</span><span class="sxs-lookup"><span data-stu-id="afd71-159">Set up continuity programs for call centers</span></span>](set-up-continuity-program.md)
