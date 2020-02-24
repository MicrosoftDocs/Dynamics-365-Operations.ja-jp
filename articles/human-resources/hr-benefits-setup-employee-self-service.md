---
title: 従業員のセルフ サービスを構成する
description: ''
author: andreabichsel
manager: AnnBe
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: e44a35071b8d0987e6c949fb11312204317b44a1
ms.sourcegitcommit: 40163705a134c9874fd33be80c7ae59ccce22c21
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/03/2020
ms.locfileid: "3009685"
---
# <a name="configure-employee-self-service"></a><span data-ttu-id="28f20-102">従業員のセルフ サービスを構成する</span><span class="sxs-lookup"><span data-stu-id="28f20-102">Configure employee self service</span></span>

[!include [banner](includes/preview-feature.md)]

<span data-ttu-id="28f20-103">Microsoft Dynamics 365 Human Resourcesでは、従業員セルフ サービスでトップレベル ナビゲーション用のタイルを構成できます。</span><span class="sxs-lookup"><span data-stu-id="28f20-103">In Microsoft Dynamics 365 Human Resources, you can configure tiles for top-level navigation in Employee self service.</span></span> <span data-ttu-id="28f20-104">給付金計画を並べて、登録する給付金計画をユーザーに直接示します。</span><span class="sxs-lookup"><span data-stu-id="28f20-104">Benefit plan tiles direct users to benefit plans that they are eligible to enroll in.</span></span>

## <a name="set-up-a-role-center-tile"></a><span data-ttu-id="28f20-105">ロール センター タイルを設定する</span><span class="sxs-lookup"><span data-stu-id="28f20-105">Set up a role center tile</span></span>

1. <span data-ttu-id="28f20-106">**給付金管理**ワークスペースで、**設定**の**従業員セルフサービス パラメータ**を選択します。</span><span class="sxs-lookup"><span data-stu-id="28f20-106">In the **Benefits management** workspace, under **Setup**, select **Employee self service parameters**.</span></span>

2. <span data-ttu-id="28f20-107">**ロール センター タイルの設定**タブをクリックし**新規**を選択します。</span><span class="sxs-lookup"><span data-stu-id="28f20-107">Select the **Role center tile setup** tab, and then select **New**.</span></span>

3. <span data-ttu-id="28f20-108">次のフィールドの値を指定します。</span><span class="sxs-lookup"><span data-stu-id="28f20-108">Specify values for the following fields:</span></span>

   | <span data-ttu-id="28f20-109">フィールド</span><span class="sxs-lookup"><span data-stu-id="28f20-109">Field</span></span> | <span data-ttu-id="28f20-110">説明</span><span class="sxs-lookup"><span data-stu-id="28f20-110">Description</span></span> |
   | --- | --- |
   | <span data-ttu-id="28f20-111">タイル ID</span><span class="sxs-lookup"><span data-stu-id="28f20-111">Tile ID</span></span> | <span data-ttu-id="28f20-112">タイルの一意の識別子。</span><span class="sxs-lookup"><span data-stu-id="28f20-112">The unique identifier for the tile.</span></span> |
   | <span data-ttu-id="28f20-113">タイル ラベル テキスト</span><span class="sxs-lookup"><span data-stu-id="28f20-113">Tile label text</span></span> | <span data-ttu-id="28f20-114">セルフ サービスのタイルに表示されるテキスト。</span><span class="sxs-lookup"><span data-stu-id="28f20-114">The text that will appear for the tile on Self-service.</span></span> |
   | <span data-ttu-id="28f20-115">説明</span><span class="sxs-lookup"><span data-stu-id="28f20-115">Description</span></span> | <span data-ttu-id="28f20-116">タイルの説明。</span><span class="sxs-lookup"><span data-stu-id="28f20-116">A description of the tile.</span></span> |
   | <span data-ttu-id="28f20-117">インターネット アドレス</span><span class="sxs-lookup"><span data-stu-id="28f20-117">Internet address</span></span> | <span data-ttu-id="28f20-118">従業員のセルフ サービス ページへの URL を入力します。</span><span class="sxs-lookup"><span data-stu-id="28f20-118">Enter the URL to the employee self service page.</span></span> |
   | <span data-ttu-id="28f20-119">タイル サイズ</span><span class="sxs-lookup"><span data-stu-id="28f20-119">Tile size</span></span> | <span data-ttu-id="28f20-120">タイルのサイズ: 小、中、または大。</span><span class="sxs-lookup"><span data-stu-id="28f20-120">The size of the tile: Small, Medium, or Large.</span></span> |
   | <span data-ttu-id="28f20-121">ターゲット</span><span class="sxs-lookup"><span data-stu-id="28f20-121">Target</span></span> | <span data-ttu-id="28f20-122">ページを新しいウィンドウで開くか、現在のウィンドウで開くかを指定します。</span><span class="sxs-lookup"><span data-stu-id="28f20-122">Specifies whether the page should open in a new window or the current window.</span></span> |
   | <span data-ttu-id="28f20-123">タイルの背景イメージ</span><span class="sxs-lookup"><span data-stu-id="28f20-123">Tile background image</span></span> | <span data-ttu-id="28f20-124">タイルに使用する画像の URL (オプション)。</span><span class="sxs-lookup"><span data-stu-id="28f20-124">The URL of the image to use for the tile (optional).</span></span> |
   | <span data-ttu-id="28f20-125">開始</span><span class="sxs-lookup"><span data-stu-id="28f20-125">Start</span></span> | <span data-ttu-id="28f20-126">タイルが使用可能になる開始日時。</span><span class="sxs-lookup"><span data-stu-id="28f20-126">The beginning date and time the tile should be available.</span></span> |
   | <span data-ttu-id="28f20-127">終了</span><span class="sxs-lookup"><span data-stu-id="28f20-127">End</span></span> | <span data-ttu-id="28f20-128">タイルが使用可能になる終了日時。</span><span class="sxs-lookup"><span data-stu-id="28f20-128">The end date and time the tile should be available.</span></span> |

4. <span data-ttu-id="28f20-129">**保存** を選択します。</span><span class="sxs-lookup"><span data-stu-id="28f20-129">Select **Save**.</span></span>

## <a name="set-up-a-benefit-plans-tile"></a><span data-ttu-id="28f20-130">給付金計画タイルの設定</span><span class="sxs-lookup"><span data-stu-id="28f20-130">Set up a benefit plans tile</span></span>

1. <span data-ttu-id="28f20-131">**給付金管理**ワークスペースで、**設定**の**従業員セルフサービス パラメータ**を選択します。</span><span class="sxs-lookup"><span data-stu-id="28f20-131">In the **Benefits management** workspace, under **Setup**, select **Employee self service parameters**.</span></span>

2. <span data-ttu-id="28f20-132">**給付金計画タイルの設定**タブをクリックし**新規**を選択します。</span><span class="sxs-lookup"><span data-stu-id="28f20-132">Select the **Benefit plans tile setup** tab, and then select **New**.</span></span>

3. <span data-ttu-id="28f20-133">次のフィールドの値を指定します。</span><span class="sxs-lookup"><span data-stu-id="28f20-133">Specify values for the following fields:</span></span>

   | <span data-ttu-id="28f20-134">フィールド</span><span class="sxs-lookup"><span data-stu-id="28f20-134">Field</span></span> | <span data-ttu-id="28f20-135">説明</span><span class="sxs-lookup"><span data-stu-id="28f20-135">Description</span></span> |
   | --- | --- |
   | <span data-ttu-id="28f20-136">タイル ID</span><span class="sxs-lookup"><span data-stu-id="28f20-136">Tile ID</span></span> | <span data-ttu-id="28f20-137">タイルの一意の識別子。</span><span class="sxs-lookup"><span data-stu-id="28f20-137">The unique identifier for the tile.</span></span> |
   | <span data-ttu-id="28f20-138">タイル ラベル テキスト</span><span class="sxs-lookup"><span data-stu-id="28f20-138">Tile label text</span></span> | <span data-ttu-id="28f20-139">セルフ サービスのタイルに表示されるテキスト。</span><span class="sxs-lookup"><span data-stu-id="28f20-139">The text that will appear for the tile on Self-service.</span></span> |
   | <span data-ttu-id="28f20-140">説明</span><span class="sxs-lookup"><span data-stu-id="28f20-140">Description</span></span> | <span data-ttu-id="28f20-141">タイルの説明。</span><span class="sxs-lookup"><span data-stu-id="28f20-141">A description of the tile.</span></span> |
   | <span data-ttu-id="28f20-142">インターネット アドレス</span><span class="sxs-lookup"><span data-stu-id="28f20-142">Internet address</span></span> | <span data-ttu-id="28f20-143">従業員のセルフ サービス ページへの URL を入力します。</span><span class="sxs-lookup"><span data-stu-id="28f20-143">Enter the URL to the employee self service page.</span></span> |
   | <span data-ttu-id="28f20-144">タイル サイズ</span><span class="sxs-lookup"><span data-stu-id="28f20-144">Tile size</span></span> | <span data-ttu-id="28f20-145">タイルのサイズ: 小、中、または大。</span><span class="sxs-lookup"><span data-stu-id="28f20-145">The size of the tile: Small, Medium, or Large.</span></span> |
   | <span data-ttu-id="28f20-146">ターゲット</span><span class="sxs-lookup"><span data-stu-id="28f20-146">Target</span></span> | <span data-ttu-id="28f20-147">ページを新しいウィンドウで開くか、現在のウィンドウで開くかを指定します。</span><span class="sxs-lookup"><span data-stu-id="28f20-147">Specifies whether the page should open in a new window or the current window.</span></span> |
   | <span data-ttu-id="28f20-148">タイルの背景イメージ</span><span class="sxs-lookup"><span data-stu-id="28f20-148">Tile background image</span></span> | <span data-ttu-id="28f20-149">タイルに使用する画像の URL (オプション)。</span><span class="sxs-lookup"><span data-stu-id="28f20-149">The URL of the image to use for the tile (optional).</span></span> |
   | <span data-ttu-id="28f20-150">開始</span><span class="sxs-lookup"><span data-stu-id="28f20-150">Start</span></span> | <span data-ttu-id="28f20-151">タイルが使用可能になる開始日時。</span><span class="sxs-lookup"><span data-stu-id="28f20-151">The beginning date and time the tile should be available.</span></span> |
   | <span data-ttu-id="28f20-152">終了</span><span class="sxs-lookup"><span data-stu-id="28f20-152">End</span></span> | <span data-ttu-id="28f20-153">タイルが使用可能になる終了日時。</span><span class="sxs-lookup"><span data-stu-id="28f20-153">The end date and time the tile should be available.</span></span> |

4. <span data-ttu-id="28f20-154">**保存** を選択します。</span><span class="sxs-lookup"><span data-stu-id="28f20-154">Select **Save**.</span></span>

## <a name="set-up-a-flex-credit-plan-tile"></a><span data-ttu-id="28f20-155">フレックス クレジット プラン タイルを設定する</span><span class="sxs-lookup"><span data-stu-id="28f20-155">Set up a flex credit plan tile</span></span>

1. <span data-ttu-id="28f20-156">**給付金管理**ワークスペースで、**設定**の**従業員セルフサービス パラメータ**を選択します。</span><span class="sxs-lookup"><span data-stu-id="28f20-156">In the **Benefits management** workspace, under **Setup**, select **Employee self service parameters**.</span></span>

2. <span data-ttu-id="28f20-157">**フレックス クレジット プラン タイルの設定**タブをクリックし**新規**を選択します。</span><span class="sxs-lookup"><span data-stu-id="28f20-157">Select the **Flex credit plan tile setup** tab, and then select **New**.</span></span>

3. <span data-ttu-id="28f20-158">次のフィールドの値を指定します。</span><span class="sxs-lookup"><span data-stu-id="28f20-158">Specify values for the following fields:</span></span>

   | <span data-ttu-id="28f20-159">フィールド</span><span class="sxs-lookup"><span data-stu-id="28f20-159">Field</span></span> | <span data-ttu-id="28f20-160">説明</span><span class="sxs-lookup"><span data-stu-id="28f20-160">Description</span></span> |
   | --- | --- |
   | <span data-ttu-id="28f20-161">タイル ID</span><span class="sxs-lookup"><span data-stu-id="28f20-161">Tile ID</span></span> | <span data-ttu-id="28f20-162">タイルの一意の識別子。</span><span class="sxs-lookup"><span data-stu-id="28f20-162">The unique identifier for the tile.</span></span> |
   | <span data-ttu-id="28f20-163">タイル ラベル テキスト</span><span class="sxs-lookup"><span data-stu-id="28f20-163">Tile label text</span></span> | <span data-ttu-id="28f20-164">セルフ サービスのタイルに表示されるテキスト。</span><span class="sxs-lookup"><span data-stu-id="28f20-164">The text that will appear for the tile on Self-service.</span></span> |
   | <span data-ttu-id="28f20-165">説明</span><span class="sxs-lookup"><span data-stu-id="28f20-165">Description</span></span> | <span data-ttu-id="28f20-166">タイルの説明。</span><span class="sxs-lookup"><span data-stu-id="28f20-166">A description of the tile.</span></span> |
   | <span data-ttu-id="28f20-167">インターネット アドレス</span><span class="sxs-lookup"><span data-stu-id="28f20-167">Internet address</span></span> | <span data-ttu-id="28f20-168">従業員のセルフ サービス ページへの URL を入力します。</span><span class="sxs-lookup"><span data-stu-id="28f20-168">Enter the URL to the employee self service page.</span></span> |
   | <span data-ttu-id="28f20-169">タイル サイズ</span><span class="sxs-lookup"><span data-stu-id="28f20-169">Tile size</span></span> | <span data-ttu-id="28f20-170">タイルのサイズ: 小、中、または大。</span><span class="sxs-lookup"><span data-stu-id="28f20-170">The size of the tile: Small, Medium, or Large.</span></span> |
   | <span data-ttu-id="28f20-171">ターゲット</span><span class="sxs-lookup"><span data-stu-id="28f20-171">Target</span></span> | <span data-ttu-id="28f20-172">ページを新しいウィンドウで開くか、現在のウィンドウで開くかを指定します。</span><span class="sxs-lookup"><span data-stu-id="28f20-172">Specifies whether the page should open in a new window or the current window.</span></span> |
   | <span data-ttu-id="28f20-173">タイルの背景イメージ</span><span class="sxs-lookup"><span data-stu-id="28f20-173">Tile background image</span></span> | <span data-ttu-id="28f20-174">タイルに使用する画像の URL (オプション)。</span><span class="sxs-lookup"><span data-stu-id="28f20-174">The URL of the image to use for the tile (optional).</span></span> |
   | <span data-ttu-id="28f20-175">開始</span><span class="sxs-lookup"><span data-stu-id="28f20-175">Start</span></span> | <span data-ttu-id="28f20-176">タイルが使用可能になる開始日時。</span><span class="sxs-lookup"><span data-stu-id="28f20-176">The beginning date and time the tile should be available.</span></span> |
   | <span data-ttu-id="28f20-177">終了</span><span class="sxs-lookup"><span data-stu-id="28f20-177">End</span></span> | <span data-ttu-id="28f20-178">タイルが使用可能になる終了日時。</span><span class="sxs-lookup"><span data-stu-id="28f20-178">The end date and time the tile should be available.</span></span> |

4. <span data-ttu-id="28f20-179">**保存** を選択します。</span><span class="sxs-lookup"><span data-stu-id="28f20-179">Select **Save**.</span></span>
