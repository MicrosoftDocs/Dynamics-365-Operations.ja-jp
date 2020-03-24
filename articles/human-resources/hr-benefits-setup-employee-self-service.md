---
title: 従業員セルフ サービスのコンフィギュレーション
description: Microsoft Dynamics 365 Human Resourcesでは、従業員セルフ サービスでトップレベル ナビゲーション用のタイルを構成できます。
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
ms.openlocfilehash: 17918fc7b894929c92c54b59b7440ab8aef980bd
ms.sourcegitcommit: f38302b9430f2ab3efe91d0a7beff946bc610e8f
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/28/2020
ms.locfileid: "3092663"
---
# <a name="configure-employee-self-service"></a><span data-ttu-id="35eab-103">従業員セルフ サービスのコンフィギュレーション</span><span class="sxs-lookup"><span data-stu-id="35eab-103">Configure employee self service</span></span>

[!include [banner](includes/preview-feature.md)]

<span data-ttu-id="35eab-104">Microsoft Dynamics 365 Human Resourcesでは、従業員セルフ サービスでトップレベル ナビゲーション用のタイルを構成できます。</span><span class="sxs-lookup"><span data-stu-id="35eab-104">In Microsoft Dynamics 365 Human Resources, you can configure tiles for top-level navigation in Employee self service.</span></span> <span data-ttu-id="35eab-105">給付金計画を並べて、登録する給付金計画をユーザーに直接示します。</span><span class="sxs-lookup"><span data-stu-id="35eab-105">Benefit plan tiles direct users to benefit plans that they are eligible to enroll in.</span></span>

## <a name="set-up-a-role-center-tile"></a><span data-ttu-id="35eab-106">ロール センター タイルを設定する</span><span class="sxs-lookup"><span data-stu-id="35eab-106">Set up a role center tile</span></span>

1. <span data-ttu-id="35eab-107">**給付金管理**ワークスペースで、**設定**の**従業員セルフサービス パラメータ**を選択します。</span><span class="sxs-lookup"><span data-stu-id="35eab-107">In the **Benefits management** workspace, under **Setup**, select **Employee self service parameters**.</span></span>

2. <span data-ttu-id="35eab-108">**ロール センター タイルの設定**タブをクリックし**新規**を選択します。</span><span class="sxs-lookup"><span data-stu-id="35eab-108">Select the **Role center tile setup** tab, and then select **New**.</span></span>

3. <span data-ttu-id="35eab-109">次のフィールドの値を指定します。</span><span class="sxs-lookup"><span data-stu-id="35eab-109">Specify values for the following fields:</span></span>

   | <span data-ttu-id="35eab-110">フィールド</span><span class="sxs-lookup"><span data-stu-id="35eab-110">Field</span></span> | <span data-ttu-id="35eab-111">説明</span><span class="sxs-lookup"><span data-stu-id="35eab-111">Description</span></span> |
   | --- | --- |
   | <span data-ttu-id="35eab-112">タイル ID</span><span class="sxs-lookup"><span data-stu-id="35eab-112">Tile ID</span></span> | <span data-ttu-id="35eab-113">タイルの一意の識別子。</span><span class="sxs-lookup"><span data-stu-id="35eab-113">The unique identifier for the tile.</span></span> |
   | <span data-ttu-id="35eab-114">タイル ラベル テキスト</span><span class="sxs-lookup"><span data-stu-id="35eab-114">Tile label text</span></span> | <span data-ttu-id="35eab-115">セルフ サービスのタイルに表示されるテキスト。</span><span class="sxs-lookup"><span data-stu-id="35eab-115">The text that will appear for the tile on Self-service.</span></span> |
   | <span data-ttu-id="35eab-116">説明</span><span class="sxs-lookup"><span data-stu-id="35eab-116">Description</span></span> | <span data-ttu-id="35eab-117">タイルの説明。</span><span class="sxs-lookup"><span data-stu-id="35eab-117">A description of the tile.</span></span> |
   | <span data-ttu-id="35eab-118">インターネット アドレス</span><span class="sxs-lookup"><span data-stu-id="35eab-118">Internet address</span></span> | <span data-ttu-id="35eab-119">従業員のセルフ サービス ページへの URL を入力します。</span><span class="sxs-lookup"><span data-stu-id="35eab-119">Enter the URL to the employee self service page.</span></span> |
   | <span data-ttu-id="35eab-120">タイル サイズ</span><span class="sxs-lookup"><span data-stu-id="35eab-120">Tile size</span></span> | <span data-ttu-id="35eab-121">タイルのサイズ: 小、中、または大。</span><span class="sxs-lookup"><span data-stu-id="35eab-121">The size of the tile: Small, Medium, or Large.</span></span> |
   | <span data-ttu-id="35eab-122">ターゲット</span><span class="sxs-lookup"><span data-stu-id="35eab-122">Target</span></span> | <span data-ttu-id="35eab-123">ページを新しいウィンドウで開くか、現在のウィンドウで開くかを指定します。</span><span class="sxs-lookup"><span data-stu-id="35eab-123">Specifies whether the page should open in a new window or the current window.</span></span> |
   | <span data-ttu-id="35eab-124">タイルの背景イメージ</span><span class="sxs-lookup"><span data-stu-id="35eab-124">Tile background image</span></span> | <span data-ttu-id="35eab-125">タイルに使用する画像の URL (オプション)。</span><span class="sxs-lookup"><span data-stu-id="35eab-125">The URL of the image to use for the tile (optional).</span></span> |
   | <span data-ttu-id="35eab-126">開始</span><span class="sxs-lookup"><span data-stu-id="35eab-126">Start</span></span> | <span data-ttu-id="35eab-127">タイルが使用可能になる開始日時。</span><span class="sxs-lookup"><span data-stu-id="35eab-127">The beginning date and time the tile should be available.</span></span> |
   | <span data-ttu-id="35eab-128">終了</span><span class="sxs-lookup"><span data-stu-id="35eab-128">End</span></span> | <span data-ttu-id="35eab-129">タイルが使用可能になる終了日時。</span><span class="sxs-lookup"><span data-stu-id="35eab-129">The end date and time the tile should be available.</span></span> |

4. <span data-ttu-id="35eab-130">**保存** を選択します。</span><span class="sxs-lookup"><span data-stu-id="35eab-130">Select **Save**.</span></span>

## <a name="set-up-a-benefit-plans-tile"></a><span data-ttu-id="35eab-131">給付金計画タイルの設定</span><span class="sxs-lookup"><span data-stu-id="35eab-131">Set up a benefit plans tile</span></span>

1. <span data-ttu-id="35eab-132">**給付金管理**ワークスペースで、**設定**の**従業員セルフサービス パラメータ**を選択します。</span><span class="sxs-lookup"><span data-stu-id="35eab-132">In the **Benefits management** workspace, under **Setup**, select **Employee self service parameters**.</span></span>

2. <span data-ttu-id="35eab-133">**給付金計画タイルの設定**タブをクリックし**新規**を選択します。</span><span class="sxs-lookup"><span data-stu-id="35eab-133">Select the **Benefit plans tile setup** tab, and then select **New**.</span></span>

3. <span data-ttu-id="35eab-134">次のフィールドの値を指定します。</span><span class="sxs-lookup"><span data-stu-id="35eab-134">Specify values for the following fields:</span></span>

   | <span data-ttu-id="35eab-135">フィールド</span><span class="sxs-lookup"><span data-stu-id="35eab-135">Field</span></span> | <span data-ttu-id="35eab-136">説明</span><span class="sxs-lookup"><span data-stu-id="35eab-136">Description</span></span> |
   | --- | --- |
   | <span data-ttu-id="35eab-137">タイル ID</span><span class="sxs-lookup"><span data-stu-id="35eab-137">Tile ID</span></span> | <span data-ttu-id="35eab-138">タイルの一意の識別子。</span><span class="sxs-lookup"><span data-stu-id="35eab-138">The unique identifier for the tile.</span></span> |
   | <span data-ttu-id="35eab-139">タイル ラベル テキスト</span><span class="sxs-lookup"><span data-stu-id="35eab-139">Tile label text</span></span> | <span data-ttu-id="35eab-140">セルフ サービスのタイルに表示されるテキスト。</span><span class="sxs-lookup"><span data-stu-id="35eab-140">The text that will appear for the tile on Self-service.</span></span> |
   | <span data-ttu-id="35eab-141">説明</span><span class="sxs-lookup"><span data-stu-id="35eab-141">Description</span></span> | <span data-ttu-id="35eab-142">タイルの説明。</span><span class="sxs-lookup"><span data-stu-id="35eab-142">A description of the tile.</span></span> |
   | <span data-ttu-id="35eab-143">インターネット アドレス</span><span class="sxs-lookup"><span data-stu-id="35eab-143">Internet address</span></span> | <span data-ttu-id="35eab-144">従業員のセルフ サービス ページへの URL を入力します。</span><span class="sxs-lookup"><span data-stu-id="35eab-144">Enter the URL to the employee self service page.</span></span> |
   | <span data-ttu-id="35eab-145">タイル サイズ</span><span class="sxs-lookup"><span data-stu-id="35eab-145">Tile size</span></span> | <span data-ttu-id="35eab-146">タイルのサイズ: 小、中、または大。</span><span class="sxs-lookup"><span data-stu-id="35eab-146">The size of the tile: Small, Medium, or Large.</span></span> |
   | <span data-ttu-id="35eab-147">ターゲット</span><span class="sxs-lookup"><span data-stu-id="35eab-147">Target</span></span> | <span data-ttu-id="35eab-148">ページを新しいウィンドウで開くか、現在のウィンドウで開くかを指定します。</span><span class="sxs-lookup"><span data-stu-id="35eab-148">Specifies whether the page should open in a new window or the current window.</span></span> |
   | <span data-ttu-id="35eab-149">タイルの背景イメージ</span><span class="sxs-lookup"><span data-stu-id="35eab-149">Tile background image</span></span> | <span data-ttu-id="35eab-150">タイルに使用する画像の URL (オプション)。</span><span class="sxs-lookup"><span data-stu-id="35eab-150">The URL of the image to use for the tile (optional).</span></span> |
   | <span data-ttu-id="35eab-151">開始</span><span class="sxs-lookup"><span data-stu-id="35eab-151">Start</span></span> | <span data-ttu-id="35eab-152">タイルが使用可能になる開始日時。</span><span class="sxs-lookup"><span data-stu-id="35eab-152">The beginning date and time the tile should be available.</span></span> |
   | <span data-ttu-id="35eab-153">終了</span><span class="sxs-lookup"><span data-stu-id="35eab-153">End</span></span> | <span data-ttu-id="35eab-154">タイルが使用可能になる終了日時。</span><span class="sxs-lookup"><span data-stu-id="35eab-154">The end date and time the tile should be available.</span></span> |

4. <span data-ttu-id="35eab-155">**保存** を選択します。</span><span class="sxs-lookup"><span data-stu-id="35eab-155">Select **Save**.</span></span>

## <a name="set-up-a-flex-credit-plan-tile"></a><span data-ttu-id="35eab-156">フレックス クレジット プラン タイルを設定する</span><span class="sxs-lookup"><span data-stu-id="35eab-156">Set up a flex credit plan tile</span></span>

1. <span data-ttu-id="35eab-157">**給付金管理**ワークスペースで、**設定**の**従業員セルフサービス パラメータ**を選択します。</span><span class="sxs-lookup"><span data-stu-id="35eab-157">In the **Benefits management** workspace, under **Setup**, select **Employee self service parameters**.</span></span>

2. <span data-ttu-id="35eab-158">**フレックス クレジット プラン タイルの設定**タブをクリックし**新規**を選択します。</span><span class="sxs-lookup"><span data-stu-id="35eab-158">Select the **Flex credit plan tile setup** tab, and then select **New**.</span></span>

3. <span data-ttu-id="35eab-159">次のフィールドの値を指定します。</span><span class="sxs-lookup"><span data-stu-id="35eab-159">Specify values for the following fields:</span></span>

   | <span data-ttu-id="35eab-160">フィールド</span><span class="sxs-lookup"><span data-stu-id="35eab-160">Field</span></span> | <span data-ttu-id="35eab-161">説明</span><span class="sxs-lookup"><span data-stu-id="35eab-161">Description</span></span> |
   | --- | --- |
   | <span data-ttu-id="35eab-162">タイル ID</span><span class="sxs-lookup"><span data-stu-id="35eab-162">Tile ID</span></span> | <span data-ttu-id="35eab-163">タイルの一意の識別子。</span><span class="sxs-lookup"><span data-stu-id="35eab-163">The unique identifier for the tile.</span></span> |
   | <span data-ttu-id="35eab-164">タイル ラベル テキスト</span><span class="sxs-lookup"><span data-stu-id="35eab-164">Tile label text</span></span> | <span data-ttu-id="35eab-165">セルフ サービスのタイルに表示されるテキスト。</span><span class="sxs-lookup"><span data-stu-id="35eab-165">The text that will appear for the tile on Self-service.</span></span> |
   | <span data-ttu-id="35eab-166">説明</span><span class="sxs-lookup"><span data-stu-id="35eab-166">Description</span></span> | <span data-ttu-id="35eab-167">タイルの説明。</span><span class="sxs-lookup"><span data-stu-id="35eab-167">A description of the tile.</span></span> |
   | <span data-ttu-id="35eab-168">インターネット アドレス</span><span class="sxs-lookup"><span data-stu-id="35eab-168">Internet address</span></span> | <span data-ttu-id="35eab-169">従業員のセルフ サービス ページへの URL を入力します。</span><span class="sxs-lookup"><span data-stu-id="35eab-169">Enter the URL to the employee self service page.</span></span> |
   | <span data-ttu-id="35eab-170">タイル サイズ</span><span class="sxs-lookup"><span data-stu-id="35eab-170">Tile size</span></span> | <span data-ttu-id="35eab-171">タイルのサイズ: 小、中、または大。</span><span class="sxs-lookup"><span data-stu-id="35eab-171">The size of the tile: Small, Medium, or Large.</span></span> |
   | <span data-ttu-id="35eab-172">ターゲット</span><span class="sxs-lookup"><span data-stu-id="35eab-172">Target</span></span> | <span data-ttu-id="35eab-173">ページを新しいウィンドウで開くか、現在のウィンドウで開くかを指定します。</span><span class="sxs-lookup"><span data-stu-id="35eab-173">Specifies whether the page should open in a new window or the current window.</span></span> |
   | <span data-ttu-id="35eab-174">タイルの背景イメージ</span><span class="sxs-lookup"><span data-stu-id="35eab-174">Tile background image</span></span> | <span data-ttu-id="35eab-175">タイルに使用する画像の URL (オプション)。</span><span class="sxs-lookup"><span data-stu-id="35eab-175">The URL of the image to use for the tile (optional).</span></span> |
   | <span data-ttu-id="35eab-176">開始</span><span class="sxs-lookup"><span data-stu-id="35eab-176">Start</span></span> | <span data-ttu-id="35eab-177">タイルが使用可能になる開始日時。</span><span class="sxs-lookup"><span data-stu-id="35eab-177">The beginning date and time the tile should be available.</span></span> |
   | <span data-ttu-id="35eab-178">終了</span><span class="sxs-lookup"><span data-stu-id="35eab-178">End</span></span> | <span data-ttu-id="35eab-179">タイルが使用可能になる終了日時。</span><span class="sxs-lookup"><span data-stu-id="35eab-179">The end date and time the tile should be available.</span></span> |

4. <span data-ttu-id="35eab-180">**保存** を選択します。</span><span class="sxs-lookup"><span data-stu-id="35eab-180">Select **Save**.</span></span>
