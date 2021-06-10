---
title: 従業員セルフ サービスのコンフィギュレーション
description: Microsoft Dynamics 365 Human Resourcesでは、従業員セルフ サービスでトップレベル ナビゲーション用のタイルを構成できます。
author: andreabichsel
ms.date: 04/06/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: BenefitWorkspace, HcmBenefitSummaryPart
audience: Application User
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 1f0d39b30b7c8d0a5729ebe3b1ed9e0d569a6660
ms.sourcegitcommit: 879ee8a10e6158885795dce4b3db5077540eec41
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/18/2021
ms.locfileid: "6052988"
---
# <a name="configure-employee-self-service"></a><span data-ttu-id="ced28-103">従業員セルフ サービスのコンフィギュレーション</span><span class="sxs-lookup"><span data-stu-id="ced28-103">Configure employee self service</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="ced28-104">Microsoft Dynamics 365 Human Resourcesでは、従業員セルフ サービスでトップレベル ナビゲーション用のタイルを構成できます。</span><span class="sxs-lookup"><span data-stu-id="ced28-104">In Microsoft Dynamics 365 Human Resources, you can configure tiles for top-level navigation in Employee self service.</span></span> <span data-ttu-id="ced28-105">福利厚生計画タイルは、適格な福利厚生計画をユーザーに直接示します。</span><span class="sxs-lookup"><span data-stu-id="ced28-105">Benefit plan tiles direct users to benefit plans that they're eligible for.</span></span>

## <a name="set-up-a-benefit-plans-tile"></a><span data-ttu-id="ced28-106">給付金計画タイルの設定</span><span class="sxs-lookup"><span data-stu-id="ced28-106">Set up a benefit plans tile</span></span>

1. <span data-ttu-id="ced28-107">**給付金管理** ワークスペースで、**設定** の **従業員セルフサービス パラメータ** を選択します。</span><span class="sxs-lookup"><span data-stu-id="ced28-107">In the **Benefits management** workspace, under **Setup**, select **Employee self service parameters**.</span></span>

2. <span data-ttu-id="ced28-108">**給付金計画タイルの設定** タブをクリックし **新規** を選択します。</span><span class="sxs-lookup"><span data-stu-id="ced28-108">Select the **Benefit plans tile setup** tab, and then select **New**.</span></span>

3. <span data-ttu-id="ced28-109">次のフィールドの値を指定します。</span><span class="sxs-lookup"><span data-stu-id="ced28-109">Specify values for the following fields:</span></span>

   | <span data-ttu-id="ced28-110">フィールド</span><span class="sxs-lookup"><span data-stu-id="ced28-110">Field</span></span> | <span data-ttu-id="ced28-111">説明</span><span class="sxs-lookup"><span data-stu-id="ced28-111">Description</span></span> |
   | --- | --- |
   | <span data-ttu-id="ced28-112">**タイル ID**</span><span class="sxs-lookup"><span data-stu-id="ced28-112">**Tile ID**</span></span> | <span data-ttu-id="ced28-113">タイルの一意の識別子。</span><span class="sxs-lookup"><span data-stu-id="ced28-113">The unique identifier for the tile.</span></span> |
   | <span data-ttu-id="ced28-114">**タイル ラベル テキスト**</span><span class="sxs-lookup"><span data-stu-id="ced28-114">**Tile label text**</span></span> | <span data-ttu-id="ced28-115">セルフ サービスのタイルに表示されるテキスト。</span><span class="sxs-lookup"><span data-stu-id="ced28-115">The text that will appear for the tile on Self-service.</span></span> |
   | <span data-ttu-id="ced28-116">**説明**</span><span class="sxs-lookup"><span data-stu-id="ced28-116">**Description**</span></span> | <span data-ttu-id="ced28-117">タイルの説明。</span><span class="sxs-lookup"><span data-stu-id="ced28-117">A description of the tile.</span></span> |
   | <span data-ttu-id="ced28-118">**インターネット アドレス**</span><span class="sxs-lookup"><span data-stu-id="ced28-118">**Internet address**</span></span> | <span data-ttu-id="ced28-119">従業員のセルフ サービス ページへの URL を入力します。</span><span class="sxs-lookup"><span data-stu-id="ced28-119">Enter the URL to the employee self service page.</span></span> |
   | <span data-ttu-id="ced28-120">**タイル サイズ**</span><span class="sxs-lookup"><span data-stu-id="ced28-120">**Tile size**</span></span> | <span data-ttu-id="ced28-121">タイルのサイズ: 小、中、または大。</span><span class="sxs-lookup"><span data-stu-id="ced28-121">The size of the tile: Small, Medium, or Large.</span></span> |
   | <span data-ttu-id="ced28-122">**ターゲット**</span><span class="sxs-lookup"><span data-stu-id="ced28-122">**Target**</span></span> | <span data-ttu-id="ced28-123">ページを新しいウィンドウで開くか、現在のウィンドウで開くかを指定します。</span><span class="sxs-lookup"><span data-stu-id="ced28-123">Specifies whether the page should open in a new window or the current window.</span></span> |
   | <span data-ttu-id="ced28-124">**タイルの背景イメージ**</span><span class="sxs-lookup"><span data-stu-id="ced28-124">**Tile background image**</span></span> | <span data-ttu-id="ced28-125">タイルに使用する画像の URL (オプション)。</span><span class="sxs-lookup"><span data-stu-id="ced28-125">The URL of the image to use for the tile (optional).</span></span> |
   | <span data-ttu-id="ced28-126">**開始**</span><span class="sxs-lookup"><span data-stu-id="ced28-126">**Start**</span></span> | <span data-ttu-id="ced28-127">タイルが使用可能になる開始日時。</span><span class="sxs-lookup"><span data-stu-id="ced28-127">The beginning date and time the tile should be available.</span></span> |
   | <span data-ttu-id="ced28-128">**終了**</span><span class="sxs-lookup"><span data-stu-id="ced28-128">**End**</span></span> | <span data-ttu-id="ced28-129">タイルが使用可能になる終了日時。</span><span class="sxs-lookup"><span data-stu-id="ced28-129">The end date and time the tile should be available.</span></span> |

4. <span data-ttu-id="ced28-130">**保存** を選択します。</span><span class="sxs-lookup"><span data-stu-id="ced28-130">Select **Save**.</span></span>

## <a name="set-up-a-flex-credit-plan-tile"></a><span data-ttu-id="ced28-131">フレックス クレジット プラン タイルを設定する</span><span class="sxs-lookup"><span data-stu-id="ced28-131">Set up a flex credit plan tile</span></span>

1. <span data-ttu-id="ced28-132">**給付金管理** ワークスペースで、**設定** の **従業員セルフサービス パラメータ** を選択します。</span><span class="sxs-lookup"><span data-stu-id="ced28-132">In the **Benefits management** workspace, under **Setup**, select **Employee self service parameters**.</span></span>

2. <span data-ttu-id="ced28-133">**フレックス クレジット プラン タイルの設定** タブをクリックし **新規** を選択します。</span><span class="sxs-lookup"><span data-stu-id="ced28-133">Select the **Flex credit plan tile setup** tab, and then select **New**.</span></span>

3. <span data-ttu-id="ced28-134">次のフィールドの値を指定します。</span><span class="sxs-lookup"><span data-stu-id="ced28-134">Specify values for the following fields:</span></span>

   | <span data-ttu-id="ced28-135">フィールド</span><span class="sxs-lookup"><span data-stu-id="ced28-135">Field</span></span> | <span data-ttu-id="ced28-136">説明</span><span class="sxs-lookup"><span data-stu-id="ced28-136">Description</span></span> |
   | --- | --- |
   | <span data-ttu-id="ced28-137">**タイル ID**</span><span class="sxs-lookup"><span data-stu-id="ced28-137">**Tile ID**</span></span> | <span data-ttu-id="ced28-138">タイルの一意の識別子。</span><span class="sxs-lookup"><span data-stu-id="ced28-138">The unique identifier for the tile.</span></span> |
   | <span data-ttu-id="ced28-139">**タイル ラベル テキスト**</span><span class="sxs-lookup"><span data-stu-id="ced28-139">**Tile label text**</span></span> | <span data-ttu-id="ced28-140">セルフ サービスのタイルに表示されるテキスト。</span><span class="sxs-lookup"><span data-stu-id="ced28-140">The text that will appear for the tile on Self service.</span></span> |
   | <span data-ttu-id="ced28-141">**説明**</span><span class="sxs-lookup"><span data-stu-id="ced28-141">**Description**</span></span> | <span data-ttu-id="ced28-142">タイルの説明。</span><span class="sxs-lookup"><span data-stu-id="ced28-142">A description of the tile.</span></span> |
   | <span data-ttu-id="ced28-143">**インターネット アドレス**</span><span class="sxs-lookup"><span data-stu-id="ced28-143">**Internet address**</span></span> | <span data-ttu-id="ced28-144">従業員のセルフ サービス ページへの URL を入力します。</span><span class="sxs-lookup"><span data-stu-id="ced28-144">Enter the URL to the employee self service page.</span></span> |
   | <span data-ttu-id="ced28-145">**タイル サイズ**</span><span class="sxs-lookup"><span data-stu-id="ced28-145">**Tile size**</span></span> | <span data-ttu-id="ced28-146">タイルのサイズ: 小、中、または大。</span><span class="sxs-lookup"><span data-stu-id="ced28-146">The size of the tile: Small, Medium, or Large.</span></span> |
   | <span data-ttu-id="ced28-147">**ターゲット**</span><span class="sxs-lookup"><span data-stu-id="ced28-147">**Target**</span></span> | <span data-ttu-id="ced28-148">ページを新しいウィンドウで開くか、現在のウィンドウで開くかを指定します。</span><span class="sxs-lookup"><span data-stu-id="ced28-148">Specifies whether the page should open in a new window or the current window.</span></span> |
   | <span data-ttu-id="ced28-149">**タイルの背景イメージ**</span><span class="sxs-lookup"><span data-stu-id="ced28-149">**Tile background image**</span></span> | <span data-ttu-id="ced28-150">タイルに使用する画像の URL (オプション)。</span><span class="sxs-lookup"><span data-stu-id="ced28-150">The URL of the image to use for the tile (optional).</span></span> |
   | <span data-ttu-id="ced28-151">**開始**</span><span class="sxs-lookup"><span data-stu-id="ced28-151">**Start**</span></span> | <span data-ttu-id="ced28-152">タイルが使用可能になる開始日時。</span><span class="sxs-lookup"><span data-stu-id="ced28-152">The beginning date and time the tile should be available.</span></span> |
   | <span data-ttu-id="ced28-153">**終了**</span><span class="sxs-lookup"><span data-stu-id="ced28-153">**End**</span></span> | <span data-ttu-id="ced28-154">タイルが使用可能になる終了日時。</span><span class="sxs-lookup"><span data-stu-id="ced28-154">The end date and time the tile should be available.</span></span> |

4. <span data-ttu-id="ced28-155">**保存** を選択します。</span><span class="sxs-lookup"><span data-stu-id="ced28-155">Select **Save**.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]