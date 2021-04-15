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
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 3e763a09e0a0f13eb7222a6ffbcb31b6230b83f4
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/31/2021
ms.locfileid: "5797938"
---
# <a name="configure-employee-self-service"></a><span data-ttu-id="3f5dc-103">従業員セルフ サービスのコンフィギュレーション</span><span class="sxs-lookup"><span data-stu-id="3f5dc-103">Configure employee self service</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="3f5dc-104">Microsoft Dynamics 365 Human Resourcesでは、従業員セルフ サービスでトップレベル ナビゲーション用のタイルを構成できます。</span><span class="sxs-lookup"><span data-stu-id="3f5dc-104">In Microsoft Dynamics 365 Human Resources, you can configure tiles for top-level navigation in Employee self service.</span></span> <span data-ttu-id="3f5dc-105">福利厚生計画タイルは、適格な福利厚生計画をユーザーに直接示します。</span><span class="sxs-lookup"><span data-stu-id="3f5dc-105">Benefit plan tiles direct users to benefit plans that they're eligible for.</span></span>

## <a name="set-up-a-benefit-plans-tile"></a><span data-ttu-id="3f5dc-106">給付金計画タイルの設定</span><span class="sxs-lookup"><span data-stu-id="3f5dc-106">Set up a benefit plans tile</span></span>

1. <span data-ttu-id="3f5dc-107">**給付金管理** ワークスペースで、**設定** の **従業員セルフサービス パラメータ** を選択します。</span><span class="sxs-lookup"><span data-stu-id="3f5dc-107">In the **Benefits management** workspace, under **Setup**, select **Employee self service parameters**.</span></span>

2. <span data-ttu-id="3f5dc-108">**給付金計画タイルの設定** タブをクリックし **新規** を選択します。</span><span class="sxs-lookup"><span data-stu-id="3f5dc-108">Select the **Benefit plans tile setup** tab, and then select **New**.</span></span>

3. <span data-ttu-id="3f5dc-109">次のフィールドの値を指定します。</span><span class="sxs-lookup"><span data-stu-id="3f5dc-109">Specify values for the following fields:</span></span>

   | <span data-ttu-id="3f5dc-110">フィールド</span><span class="sxs-lookup"><span data-stu-id="3f5dc-110">Field</span></span> | <span data-ttu-id="3f5dc-111">説明</span><span class="sxs-lookup"><span data-stu-id="3f5dc-111">Description</span></span> |
   | --- | --- |
   | <span data-ttu-id="3f5dc-112">**タイル ID**</span><span class="sxs-lookup"><span data-stu-id="3f5dc-112">**Tile ID**</span></span> | <span data-ttu-id="3f5dc-113">タイルの一意の識別子。</span><span class="sxs-lookup"><span data-stu-id="3f5dc-113">The unique identifier for the tile.</span></span> |
   | <span data-ttu-id="3f5dc-114">**タイル ラベル テキスト**</span><span class="sxs-lookup"><span data-stu-id="3f5dc-114">**Tile label text**</span></span> | <span data-ttu-id="3f5dc-115">セルフ サービスのタイルに表示されるテキスト。</span><span class="sxs-lookup"><span data-stu-id="3f5dc-115">The text that will appear for the tile on Self-service.</span></span> |
   | <span data-ttu-id="3f5dc-116">**説明**</span><span class="sxs-lookup"><span data-stu-id="3f5dc-116">**Description**</span></span> | <span data-ttu-id="3f5dc-117">タイルの説明。</span><span class="sxs-lookup"><span data-stu-id="3f5dc-117">A description of the tile.</span></span> |
   | <span data-ttu-id="3f5dc-118">**インターネット アドレス**</span><span class="sxs-lookup"><span data-stu-id="3f5dc-118">**Internet address**</span></span> | <span data-ttu-id="3f5dc-119">従業員のセルフ サービス ページへの URL を入力します。</span><span class="sxs-lookup"><span data-stu-id="3f5dc-119">Enter the URL to the employee self service page.</span></span> |
   | <span data-ttu-id="3f5dc-120">**タイル サイズ**</span><span class="sxs-lookup"><span data-stu-id="3f5dc-120">**Tile size**</span></span> | <span data-ttu-id="3f5dc-121">タイルのサイズ: 小、中、または大。</span><span class="sxs-lookup"><span data-stu-id="3f5dc-121">The size of the tile: Small, Medium, or Large.</span></span> |
   | <span data-ttu-id="3f5dc-122">**ターゲット**</span><span class="sxs-lookup"><span data-stu-id="3f5dc-122">**Target**</span></span> | <span data-ttu-id="3f5dc-123">ページを新しいウィンドウで開くか、現在のウィンドウで開くかを指定します。</span><span class="sxs-lookup"><span data-stu-id="3f5dc-123">Specifies whether the page should open in a new window or the current window.</span></span> |
   | <span data-ttu-id="3f5dc-124">**タイルの背景イメージ**</span><span class="sxs-lookup"><span data-stu-id="3f5dc-124">**Tile background image**</span></span> | <span data-ttu-id="3f5dc-125">タイルに使用する画像の URL (オプション)。</span><span class="sxs-lookup"><span data-stu-id="3f5dc-125">The URL of the image to use for the tile (optional).</span></span> |
   | <span data-ttu-id="3f5dc-126">**開始**</span><span class="sxs-lookup"><span data-stu-id="3f5dc-126">**Start**</span></span> | <span data-ttu-id="3f5dc-127">タイルが使用可能になる開始日時。</span><span class="sxs-lookup"><span data-stu-id="3f5dc-127">The beginning date and time the tile should be available.</span></span> |
   | <span data-ttu-id="3f5dc-128">**終了**</span><span class="sxs-lookup"><span data-stu-id="3f5dc-128">**End**</span></span> | <span data-ttu-id="3f5dc-129">タイルが使用可能になる終了日時。</span><span class="sxs-lookup"><span data-stu-id="3f5dc-129">The end date and time the tile should be available.</span></span> |

4. <span data-ttu-id="3f5dc-130">**保存** を選択します。</span><span class="sxs-lookup"><span data-stu-id="3f5dc-130">Select **Save**.</span></span>

## <a name="set-up-a-flex-credit-plan-tile"></a><span data-ttu-id="3f5dc-131">フレックス クレジット プラン タイルを設定する</span><span class="sxs-lookup"><span data-stu-id="3f5dc-131">Set up a flex credit plan tile</span></span>

1. <span data-ttu-id="3f5dc-132">**給付金管理** ワークスペースで、**設定** の **従業員セルフサービス パラメータ** を選択します。</span><span class="sxs-lookup"><span data-stu-id="3f5dc-132">In the **Benefits management** workspace, under **Setup**, select **Employee self service parameters**.</span></span>

2. <span data-ttu-id="3f5dc-133">**フレックス クレジット プラン タイルの設定** タブをクリックし **新規** を選択します。</span><span class="sxs-lookup"><span data-stu-id="3f5dc-133">Select the **Flex credit plan tile setup** tab, and then select **New**.</span></span>

3. <span data-ttu-id="3f5dc-134">次のフィールドの値を指定します。</span><span class="sxs-lookup"><span data-stu-id="3f5dc-134">Specify values for the following fields:</span></span>

   | <span data-ttu-id="3f5dc-135">フィールド</span><span class="sxs-lookup"><span data-stu-id="3f5dc-135">Field</span></span> | <span data-ttu-id="3f5dc-136">説明</span><span class="sxs-lookup"><span data-stu-id="3f5dc-136">Description</span></span> |
   | --- | --- |
   | <span data-ttu-id="3f5dc-137">**タイル ID**</span><span class="sxs-lookup"><span data-stu-id="3f5dc-137">**Tile ID**</span></span> | <span data-ttu-id="3f5dc-138">タイルの一意の識別子。</span><span class="sxs-lookup"><span data-stu-id="3f5dc-138">The unique identifier for the tile.</span></span> |
   | <span data-ttu-id="3f5dc-139">**タイル ラベル テキスト**</span><span class="sxs-lookup"><span data-stu-id="3f5dc-139">**Tile label text**</span></span> | <span data-ttu-id="3f5dc-140">セルフ サービスのタイルに表示されるテキスト。</span><span class="sxs-lookup"><span data-stu-id="3f5dc-140">The text that will appear for the tile on Self service.</span></span> |
   | <span data-ttu-id="3f5dc-141">**説明**</span><span class="sxs-lookup"><span data-stu-id="3f5dc-141">**Description**</span></span> | <span data-ttu-id="3f5dc-142">タイルの説明。</span><span class="sxs-lookup"><span data-stu-id="3f5dc-142">A description of the tile.</span></span> |
   | <span data-ttu-id="3f5dc-143">**インターネット アドレス**</span><span class="sxs-lookup"><span data-stu-id="3f5dc-143">**Internet address**</span></span> | <span data-ttu-id="3f5dc-144">従業員のセルフ サービス ページへの URL を入力します。</span><span class="sxs-lookup"><span data-stu-id="3f5dc-144">Enter the URL to the employee self service page.</span></span> |
   | <span data-ttu-id="3f5dc-145">**タイル サイズ**</span><span class="sxs-lookup"><span data-stu-id="3f5dc-145">**Tile size**</span></span> | <span data-ttu-id="3f5dc-146">タイルのサイズ: 小、中、または大。</span><span class="sxs-lookup"><span data-stu-id="3f5dc-146">The size of the tile: Small, Medium, or Large.</span></span> |
   | <span data-ttu-id="3f5dc-147">**ターゲット**</span><span class="sxs-lookup"><span data-stu-id="3f5dc-147">**Target**</span></span> | <span data-ttu-id="3f5dc-148">ページを新しいウィンドウで開くか、現在のウィンドウで開くかを指定します。</span><span class="sxs-lookup"><span data-stu-id="3f5dc-148">Specifies whether the page should open in a new window or the current window.</span></span> |
   | <span data-ttu-id="3f5dc-149">**タイルの背景イメージ**</span><span class="sxs-lookup"><span data-stu-id="3f5dc-149">**Tile background image**</span></span> | <span data-ttu-id="3f5dc-150">タイルに使用する画像の URL (オプション)。</span><span class="sxs-lookup"><span data-stu-id="3f5dc-150">The URL of the image to use for the tile (optional).</span></span> |
   | <span data-ttu-id="3f5dc-151">**開始**</span><span class="sxs-lookup"><span data-stu-id="3f5dc-151">**Start**</span></span> | <span data-ttu-id="3f5dc-152">タイルが使用可能になる開始日時。</span><span class="sxs-lookup"><span data-stu-id="3f5dc-152">The beginning date and time the tile should be available.</span></span> |
   | <span data-ttu-id="3f5dc-153">**終了**</span><span class="sxs-lookup"><span data-stu-id="3f5dc-153">**End**</span></span> | <span data-ttu-id="3f5dc-154">タイルが使用可能になる終了日時。</span><span class="sxs-lookup"><span data-stu-id="3f5dc-154">The end date and time the tile should be available.</span></span> |

4. <span data-ttu-id="3f5dc-155">**保存** を選択します。</span><span class="sxs-lookup"><span data-stu-id="3f5dc-155">Select **Save**.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]