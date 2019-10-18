---
title: 販売時点管理 (POS) の画面レイアウト
description: このトピックでは、Dynamics 365 Retail POS (販売時点管理) の画面レイアウトに関する情報を提供します。
author: jblucher
manager: AnnBe
ms.date: 05/20/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: RetailTillLayout
audience: Application user
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 90573
ms.assetid: a6868f93-02ed-4928-9f6a-3b7383e7e399
ms.search.region: global
ms.search.industry: Retail
ms.author: jeffbl
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: 4852ec9b347f119a1007b63476b8609a3e38ba57
ms.sourcegitcommit: f87de0f949b5d60993b19e0f61297f02d42b5bef
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2019
ms.locfileid: "2025278"
---
# <a name="screen-layouts-for-the-point-of-sale-pos"></a><span data-ttu-id="6a587-103">販売時点管理 (POS) の画面レイアウト</span><span class="sxs-lookup"><span data-stu-id="6a587-103">Screen layouts for the point of sale (POS)</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="6a587-104">このトピックでは、Dynamics 365 Retail POS (販売時点管理) の画面レイアウトに関する情報を提供します。</span><span class="sxs-lookup"><span data-stu-id="6a587-104">This topic provides information about screen layouts for Dynamics 365 Retail point of sale (POS) experiences.</span></span>

<span data-ttu-id="6a587-105">Retail POS のユーザー インターフェイス (UI) は、店舗、レジスター、および/またはユーザーに割り当てられた視覚プロファイルと画面レイアウトの組み合わせを使用してコンフィギュレーションできます。</span><span class="sxs-lookup"><span data-stu-id="6a587-105">The Retail POS user interface (UI) can be configured by using a combination of visual profiles and screen layouts that are assigned to stores, registers, and/or users.</span></span>

<span data-ttu-id="6a587-106">次の図は、POS UI のコンフィギュレーション可能な側面を構成するさまざまなエンティティ間の関係を示します。</span><span class="sxs-lookup"><span data-stu-id="6a587-106">The following illustration shows the relationships among the various entities that make up the configurable aspects of the POS UI.</span></span>

![POS 画面レイアウト エンティティ](../retail/media/POS-layout-configuration-entities-diagram.png)

## <a name="visual-profile"></a><span data-ttu-id="6a587-108">ビジュアル プロファイル</span><span class="sxs-lookup"><span data-stu-id="6a587-108">Visual profile</span></span>

<span data-ttu-id="6a587-109">視覚プロファイルはレジスターに割り当てられ、レジスター固有でユーザー間で共有される視覚要素を指定します。</span><span class="sxs-lookup"><span data-stu-id="6a587-109">Visual profiles are assigned to registers, and they specify the visual elements that are register-specific and shared across users.</span></span> <span data-ttu-id="6a587-110">レジスターにサインインするユーザーには、同じテーマ、色、および画像が表示されます。</span><span class="sxs-lookup"><span data-stu-id="6a587-110">Every user who signs in to the register sees the same theme, colors, and images.</span></span>

![Light テーマの POS ようこそ画面](../retail/media/POS-Welcome-Screen-with-Light-theme.png)

![Dark テーマの POS トランザクション画面](../retail/media/POS-Transaction-Screen-with-Dark-theme.png)

- <span data-ttu-id="6a587-113">**プロファイル番号** – プロファイル番号は、視覚プロファイルの固有識別子です。</span><span class="sxs-lookup"><span data-stu-id="6a587-113">**Profile number** – The profile number is the unique identifier of the visual profile.</span></span>
- <span data-ttu-id="6a587-114">**説明** – 状況に合った正しいプロファイルを特定するのに役立つ、わかりやすい名前を指定できます。</span><span class="sxs-lookup"><span data-stu-id="6a587-114">**Description** – You can specify a meaningful name that will help identify the correct profile for your situation.</span></span>
- <span data-ttu-id="6a587-115">**テーマ** – Light または Dark アプリケーション テーマを選択できます。</span><span class="sxs-lookup"><span data-stu-id="6a587-115">**Theme** – You can select between the Light and Dark application themes.</span></span> <span data-ttu-id="6a587-116">テーマは、アプリケーション全体で、フォントと背景の色に影響します。</span><span class="sxs-lookup"><span data-stu-id="6a587-116">The theme affects the font and background colors throughout the application.</span></span>
- <span data-ttu-id="6a587-117">**アクセント色** – アクセント色は、タイル、コマンド ボタン、またはハイパーリンクなどの固有の視覚要素を、区別または強調表示するために POS 全体で使用されます。</span><span class="sxs-lookup"><span data-stu-id="6a587-117">**Accent color** – The accent color is used throughout the POS to differentiate or highlight specific visual elements, such as tiles, command buttons, and hyperlinks.</span></span> <span data-ttu-id="6a587-118">通常、これらの要素は実行可能です。</span><span class="sxs-lookup"><span data-stu-id="6a587-118">Typically, these elements are actionable.</span></span>
- <span data-ttu-id="6a587-119">**ヘッダーの色** – 小売業者のブランドの要件を満たすようにページ ヘッダーの色をコンフィギュレーションすることができます。</span><span class="sxs-lookup"><span data-stu-id="6a587-119">**Header color** – You can configure the color of the page header to meet the retailer's branding requirements.</span></span> <span data-ttu-id="6a587-120">この機能は Retail バージョン 1611 でのみ使用することができます。</span><span class="sxs-lookup"><span data-stu-id="6a587-120">This feature is available only in Retail version 1611.</span></span>
- <span data-ttu-id="6a587-121">**日時を表示** – 有効な場合、現在の日時が POS ヘッダーに表示されます。</span><span class="sxs-lookup"><span data-stu-id="6a587-121">**Show date/time** – When enbled, the current date and time will be displayed in the POS header.</span></span>
- <span data-ttu-id="6a587-122">**ログイン バックグラウンド** – サインイン画面の背景画像を指定できます。</span><span class="sxs-lookup"><span data-stu-id="6a587-122">**Login backgrounds** – You can specify a background image for the sign-in screen.</span></span> <span data-ttu-id="6a587-123">大容量のファイルの保存と読み込みは、アプリケーションの動作やパフォーマンスに影響を与える可能性があるため、背景画像のファイル サイズはできるだけ小さくする必要があります。</span><span class="sxs-lookup"><span data-stu-id="6a587-123">The file size of background images should be kept as small as possible, because storing and loading large files can affect application behavior and performance.</span></span>
- <span data-ttu-id="6a587-124">**アプリケーションの背景** - アプリケーション全体で無地のテーマ色の代わりに使用されている背景画像を指定できます。</span><span class="sxs-lookup"><span data-stu-id="6a587-124">**Application background** – You can specify a background image that is used instead of the solid theme color throughout the application.</span></span> <span data-ttu-id="6a587-125">ログイン バックグラウンドに関しては、ファイル サイズをできる限り小さくする必要があります。</span><span class="sxs-lookup"><span data-stu-id="6a587-125">As for login backgrounds, the file size should be kept as small as possible.</span></span>

## <a name="screen-layouts"></a><span data-ttu-id="6a587-126">画面レイアウト</span><span class="sxs-lookup"><span data-stu-id="6a587-126">Screen layouts</span></span>

<span data-ttu-id="6a587-127">画面レイアウト構成によって、POS ようこそ画面および**トランザクション**画面での UI コントロールのアクション、コンテンツ、および配置が決定されます。</span><span class="sxs-lookup"><span data-stu-id="6a587-127">Screen layout configurations determine the actions, content, and placement of UI controls on the POS welcome screen and **Transaction** screen.</span></span>

![POS 画面レイアウト表示](../retail/media/POS-Screen-Layout-View.png)

- <span data-ttu-id="6a587-129">**ようこそ画面** – ほとんどの場合、ようこそ画面は、ユーザーが初めて POS にサインインするときに表示されるページです。</span><span class="sxs-lookup"><span data-stu-id="6a587-129">**Welcome screen** – In most cases, the welcome screen is the page that users see when they first sign in to the POS.</span></span> <span data-ttu-id="6a587-130">ようこそ画面は、ブランド イメージと、POS 操作へのアクセスを提供するボタン グリッドで構成することができます。</span><span class="sxs-lookup"><span data-stu-id="6a587-130">The welcome screen can consist of a branding image and button grids that provide access to POS operations.</span></span> <span data-ttu-id="6a587-131">通常、現在のトランザクションに固有でない操作はこのスクリーンに表示されます。</span><span class="sxs-lookup"><span data-stu-id="6a587-131">Typically, operations that aren't specific to the current transaction are put on this screen.</span></span>

    ![POS ようこそ画面](../retail/media/POS-Welcome-Screen.png)

- <span data-ttu-id="6a587-133">**トランザクション画面** – **トランザクション**画面は、販売トランザクションおよび注文処理のための POS のメイン画面です。</span><span class="sxs-lookup"><span data-stu-id="6a587-133">**Transaction screen** – The **Transaction** screen is the main screen in the POS for processing sales transactions and orders.</span></span> <span data-ttu-id="6a587-134">コンテンツやレイアウトは、画面レイアウト デザイナーを使用してコンフィギュレーションします。</span><span class="sxs-lookup"><span data-stu-id="6a587-134">The content and layout are configured by using the screen layout designer.</span></span>

    ![POS トランザクション画面](../retail/media/POS-Transaction-Screen.png)

- <span data-ttu-id="6a587-136">**既定のスタート画面** – 一部の小売業者は、サインイン後にレジ担当者が**トランザクション**画面に直接移動することを好みます。</span><span class="sxs-lookup"><span data-stu-id="6a587-136">**Default start screen** – Some retailers prefer that cashiers go directly to the **Transaction** screen after sign-in.</span></span> <span data-ttu-id="6a587-137">**既定のスタート画面**設定では、各画面レイアウトのサインイン後に表示される既定の画面を指定できます。</span><span class="sxs-lookup"><span data-stu-id="6a587-137">The **Default start screen** setting lets you specify the default screen that appears after sign-in for each screen layout.</span></span>

### <a name="assignment"></a><span data-ttu-id="6a587-138">割り当て</span><span class="sxs-lookup"><span data-stu-id="6a587-138">Assignment</span></span>

<span data-ttu-id="6a587-139">画面レイアウトは、店舗、レジスター、またはユーザー レベルで割り当てることができます。</span><span class="sxs-lookup"><span data-stu-id="6a587-139">Screen layouts can be assigned at the store, register, or user level.</span></span> <span data-ttu-id="6a587-140">ユーザーの割り当てはレジスターと店舗の割り当てを上書きし、レジスターの割り当ては店舗の割り当てを上書きします。</span><span class="sxs-lookup"><span data-stu-id="6a587-140">The user assignment overrides the register and store assignments, and the register assignment overrides the store assignment.</span></span> <span data-ttu-id="6a587-141">すべてのユーザーがレジスターまたはロールに関係なく同じレイアウトを使用する単純なシナリオでは、画面レイアウトは店舗レベルでのみ設定できます。</span><span class="sxs-lookup"><span data-stu-id="6a587-141">In a simple scenario where all users use the same layout, regardless of register or role, the screen layout can be set only at the store level.</span></span> <span data-ttu-id="6a587-142">特定のレジスターまたはユーザーが特殊なレイアウトを必要とするシナリオでは、それらのレイアウトを割り当てることができます。</span><span class="sxs-lookup"><span data-stu-id="6a587-142">In scenarios where specific registers or users require specialized layouts, those layouts can be assigned.</span></span>

### <a name="layout-sizes"></a><span data-ttu-id="6a587-143">レイアウト サイズ</span><span class="sxs-lookup"><span data-stu-id="6a587-143">Layout sizes</span></span>

<span data-ttu-id="6a587-144">POS UI の大部分は応答可能で、レイアウトは画面のサイズや向きに基づいて自動的にサイズを変更、調整されます。</span><span class="sxs-lookup"><span data-stu-id="6a587-144">Most aspects of the POS UI are responsive, and the layout is automatically resized and adjusted based on the screen size and orientation.</span></span> <span data-ttu-id="6a587-145">ただし、POS **トランザクション**画面は予想されるすべての画面解像度用にコンフィギュレーションする必要があります。</span><span class="sxs-lookup"><span data-stu-id="6a587-145">However, the POS **Transaction** screen must be configured for every screen resolution that is expected.</span></span>

<span data-ttu-id="6a587-146">起動時に、POS アプリケーションはデバイス用にコンフィギュレーションされたものに最も近いレイアウト サイズを自動的に選択します。</span><span class="sxs-lookup"><span data-stu-id="6a587-146">At startup, the POS application automatically selects the closest layout size that is configured for the device.</span></span> <span data-ttu-id="6a587-147">画面レイアウトは、ランドスケープとポートレート両方のモード、およびフルサイズとコンパクト両方のデバイスのコンフィギュレーションを含めることもできます。</span><span class="sxs-lookup"><span data-stu-id="6a587-147">A screen layout can also contain configurations for both landscape and portrait modes, and for both full-size and compact devices.</span></span> <span data-ttu-id="6a587-148">したがって、ユーザーは店舗内で使用されるさまざまなサイズとフォーム係数で使用する 1 つの画面レイアウトに割り当てられます。</span><span class="sxs-lookup"><span data-stu-id="6a587-148">Therefore, users can be assigned to a single screen layout that works across various sizes and form factors that are used in the store.</span></span>

![POS のレイアウト サイズ](../retail/media/POS-Screen-Layout-Sizes.png)

- <span data-ttu-id="6a587-150">**名前** – 画面のサイズを識別するために、わかりやすい名前を入力することができます。</span><span class="sxs-lookup"><span data-stu-id="6a587-150">**Name** – You can enter a meaningful name to identify the screen size.</span></span>
- <span data-ttu-id="6a587-151">**レイアウト タイプ** – POS アプリケーションは、特定のデバイスに最適なユーザー エクスペリエンスを提供する各種のモードでその UI を表示することができます。</span><span class="sxs-lookup"><span data-stu-id="6a587-151">**Layout type** – The POS application can show its UI in various modes to provide the best user experience on a given device.</span></span>

    - <span data-ttu-id="6a587-152">**Modern POS – Full** – 通常、フル レイアウトはデスクトップ モニターまたはタブレットなどの大型ディスプレイに最適です。</span><span class="sxs-lookup"><span data-stu-id="6a587-152">**Modern POS – Full** – Full layouts are typically best for larger displays, such as desktop monitors and tablets.</span></span> <span data-ttu-id="6a587-153">含める UI 要素を選択し、要素のサイズと配置を指定し、詳細なプロパティをコンフィギュレーションできます。</span><span class="sxs-lookup"><span data-stu-id="6a587-153">You can select the UI elements to include, specify the size and placement of those elements, and configure their detailed properties.</span></span> <span data-ttu-id="6a587-154">フル レイアウトは、縦向きおよび横向きの両方のコンフィギュレーションをサポートします。</span><span class="sxs-lookup"><span data-stu-id="6a587-154">Full layouts support both portrait and landscape configurations.</span></span>
    - <span data-ttu-id="6a587-155">**Modern POS – Compact** – コンパクト レイアウトは、通常、携帯電話や小型タブレットに最適です。</span><span class="sxs-lookup"><span data-stu-id="6a587-155">**Modern POS – Compact** – Compact layouts are typically best for phones and small tablets.</span></span> <span data-ttu-id="6a587-156">コンパクト デバイスの設計の可能性は限られています。</span><span class="sxs-lookup"><span data-stu-id="6a587-156">The design possibilities for compact devices are limited.</span></span> <span data-ttu-id="6a587-157">領収書および合計パネルの列とフィールドをコンフィギュレーションできます。</span><span class="sxs-lookup"><span data-stu-id="6a587-157">You can configure the columns and fields for the receipt and totals panels.</span></span>

- <span data-ttu-id="6a587-158">**幅/高さ** – これらの値は、レイアウトで想定されるピクセル単位の有効な画面のサイズを表します。</span><span class="sxs-lookup"><span data-stu-id="6a587-158">**Width/Height** – These values represent the effective screen size, in pixels, that is expected for the layout.</span></span> <span data-ttu-id="6a587-159">一部のオペレーティング システムは、高解像度ディスプレイに拡大と縮小を使用することに注意してください。</span><span class="sxs-lookup"><span data-stu-id="6a587-159">Remember that some operating systems use scaling for high-resolution displays.</span></span>

> [!TIP]
> <span data-ttu-id="6a587-160">アプリで解決策を表示することによって、POS 画面に必要なレイアウト サイズがわかります。</span><span class="sxs-lookup"><span data-stu-id="6a587-160">You can learn the layout size that is required for a POS screen by viewing the resolution in the app.</span></span> <span data-ttu-id="6a587-161">POS を起動し、**設定\>セッション情報**に移動します。</span><span class="sxs-lookup"><span data-stu-id="6a587-161">Start the POS, and go to **Settings \> Session information**.</span></span> <span data-ttu-id="6a587-162">POS は、現在読み込まれている画面レイアウト、レイアウトのサイズ、およびアプリのウィンドウの解像度を表示します。</span><span class="sxs-lookup"><span data-stu-id="6a587-162">POS shows the screen layout that is currently loaded, the layout size, and the resolution of the app window.</span></span>

![POS のレイアウト サイズ](../retail/media/POS-Session-Information.png)

### <a name="button-grids"></a><span data-ttu-id="6a587-164">ボタン グリッド</span><span class="sxs-lookup"><span data-stu-id="6a587-164">Button grids</span></span>

<span data-ttu-id="6a587-165">画面レイアウトでのレイアウト サイズごとに、POS ようこそ画面と**トランザクション**画面のボタン グリッドをコンフィギュレーションし、割り当てることができます。</span><span class="sxs-lookup"><span data-stu-id="6a587-165">For each layout size in a screen layout, you can configure and assign button grids for the POS welcome screen and **Transaction** screen.</span></span> <span data-ttu-id="6a587-166">ようこそ画面のボタン グリッドは、左から右へ、最も小さい番号 (ようこそ画面 1) から最も大きい番号へ自動的にレイアウトされます。</span><span class="sxs-lookup"><span data-stu-id="6a587-166">Button grids for the welcome screen are automatically laid out from left to right, from the lowest number (Welcome screen 1) to the highest number.</span></span>

<span data-ttu-id="6a587-167">フル POS レイアウトでは、ボタン グリッドの配置は画面レイアウト デザイナーで指定されます。</span><span class="sxs-lookup"><span data-stu-id="6a587-167">In Full POS layouts, the placement of button grids is specified in the screen layout designer.</span></span>

<span data-ttu-id="6a587-168">コンパクト POS レイアウトでは、ボタン グリッドは上から下へ、最も小さい番号 (トランザクション画面 1) から最も大きい番号へ自動的にレイアウトされます。</span><span class="sxs-lookup"><span data-stu-id="6a587-168">In Compact POS layouts, the button grids are automatically laid out from top to bottom, from the lowest number (Transaction screen 1) to the highest number.</span></span> <span data-ttu-id="6a587-169">**アクション**メニューからアクセスできます。</span><span class="sxs-lookup"><span data-stu-id="6a587-169">They can be accessed on the **Actions** menu.</span></span>

![コンパクト レイアウトのボタン グリッド](../retail/media/Compact-View-Button-Grids.png)

### <a name="images"></a><span data-ttu-id="6a587-171">イメージ</span><span class="sxs-lookup"><span data-stu-id="6a587-171">Images</span></span>

<span data-ttu-id="6a587-172">画面レイアウトでの各レイアウト サイズで、POS UI に含めるための画像を指定できます。</span><span class="sxs-lookup"><span data-stu-id="6a587-172">For each layout size in a screen layout, you can specify images to include in the POS UI.</span></span> <span data-ttu-id="6a587-173">フル POS レイアウトには、ようこそ画面に 1 つの画像を指定できます。</span><span class="sxs-lookup"><span data-stu-id="6a587-173">For Full POS layouts, a single image can be specified for the welcome screen.</span></span> <span data-ttu-id="6a587-174">この画像は、左側に最初の UI 要素として表示されます。</span><span class="sxs-lookup"><span data-stu-id="6a587-174">This image appears as the first UI element on the left.</span></span> <span data-ttu-id="6a587-175">**トランザクション**画面で、タブの画像、またはロゴとして画像を使用することができます。</span><span class="sxs-lookup"><span data-stu-id="6a587-175">On the **Transaction** screen, images can be used as tab images or as a logo.</span></span> <span data-ttu-id="6a587-176">コンパクト POS レイアウトは、これらの画像を使用しません。</span><span class="sxs-lookup"><span data-stu-id="6a587-176">Compact POS layouts don't use these images.</span></span>

### <a name="screen-layout-designer"></a><span data-ttu-id="6a587-177">画面レイアウト デザイナー</span><span class="sxs-lookup"><span data-stu-id="6a587-177">Screen layout designer</span></span>

<span data-ttu-id="6a587-178">画面レイアウト デザイナーでは、POS **トランザクション**画面のさまざまな側面をポートレートおよびランドスケープ両方のモードで、またフルおよびコンパクト両方のレイアウトで、レイアウト サイズごとにコンフィギュレーションできます。</span><span class="sxs-lookup"><span data-stu-id="6a587-178">The screen layout designer lets you configure various aspects of the POS **Transaction** screen for each layout size, in both portrait and landscape modes, and for both Full and Compact layouts.</span></span> <span data-ttu-id="6a587-179">画面レイアウト デザイナーは、ユーザーがアクセスするたびに ClickOnce の配置テクノロジーを使用してアプリケーションの最新バージョンをダウンロード、インストール、および起動します。</span><span class="sxs-lookup"><span data-stu-id="6a587-179">The screen layout designer uses the ClickOnce deployment technology to download, install, and start the latest version of the application every time that users access it.</span></span> <span data-ttu-id="6a587-180">必ず ClickOnce のブラウザの要件を確認してください。</span><span class="sxs-lookup"><span data-stu-id="6a587-180">Be sure to check the browser requirements for ClickOnce.</span></span> <span data-ttu-id="6a587-181">Google Chrome などの一部のブラウザーでは、拡張機能が必要です。</span><span class="sxs-lookup"><span data-stu-id="6a587-181">Some browsers, such as Google Chrome, require extensions.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="6a587-182">POS で定義され、使用されている各レイアウト サイズの画面レイアウトをコンフィギュレーションする必要があります。</span><span class="sxs-lookup"><span data-stu-id="6a587-182">You must configure a screen layout for each layout size that is defined and that is used by the POS.</span></span>

### <a name="full-layout-designer"></a><span data-ttu-id="6a587-183">フル レイアウト デザイナー</span><span class="sxs-lookup"><span data-stu-id="6a587-183">Full layout designer</span></span>

<span data-ttu-id="6a587-184">フル レイアウト デザイナーでは、ユーザーは UI コントロールを POS **トランザクション**画面にドラッグし、それらのコントロールの設定をコンフィギュレーションできます。</span><span class="sxs-lookup"><span data-stu-id="6a587-184">The Full layout designer lets users drag UI controls onto the POS **Transaction** screen and configure the settings of those controls.</span></span>

![POS フル レイアウト デザイナー (ランドスケープ モード)](../retail/media/POS-Full-Layout-Designer-Landscape.png)

- <span data-ttu-id="6a587-186">**インポート レイアウト/エクスポート レイアウト** – POS 画面レイアウト デザインを環境間で簡単に再利用して共有できるように、XML ファイルとしてエクスポートおよびインポートできます。</span><span class="sxs-lookup"><span data-stu-id="6a587-186">**Import layout/Export layout** – You can export and import POS screen layout designs as XML files, so that you can easily reuse and share them across environments.</span></span> <span data-ttu-id="6a587-187">正しいレイアウト サイズのレイアウト デザインをインポートすることが重要です。</span><span class="sxs-lookup"><span data-stu-id="6a587-187">It's important that you import layout designs for the correct layout sizes.</span></span> <span data-ttu-id="6a587-188">それ以外の場合、UI 要素が画面に正しく収まらない場合があります。</span><span class="sxs-lookup"><span data-stu-id="6a587-188">Otherwise, UI elements might not fit correctly on the screen.</span></span>
- <span data-ttu-id="6a587-189">**ランドスケープ/ポートレート** – POS デバイスでユーザーがランドスケープ モードとポートレート モードを切り替えることができる場合は、各モードの画面レイアウトを定義する必要があります。</span><span class="sxs-lookup"><span data-stu-id="6a587-189">**Landscape/Portrait** – If the POS device lets users switch between landscape and portrait modes, you must define a screen layout for each mode.</span></span> <span data-ttu-id="6a587-190">POS は自動的にスクリーン ローテーションを検出し、正しいレイアウトを示します。</span><span class="sxs-lookup"><span data-stu-id="6a587-190">The POS automatically detects screen rotation and shows the correct layout.</span></span>
- <span data-ttu-id="6a587-191">**レイアウト グリッド** – POS レイアウト デザイナーは 4 ピクセル グリッドを使用します。</span><span class="sxs-lookup"><span data-stu-id="6a587-191">**Layout grid** – The POS layout designer uses a 4-pixel grid.</span></span> <span data-ttu-id="6a587-192">UI は、コンテンツを正しく配置するために、グリッドに「スナップ」をコントロールします。</span><span class="sxs-lookup"><span data-stu-id="6a587-192">UI controls "snap" to the grid to help you correctly align the content.</span></span>
- <span data-ttu-id="6a587-193">**デザイナー ズーム** – デザイナー ビューをズームインおよびズームアウトして、POS 画面のコンテンツの表示を向上できます。</span><span class="sxs-lookup"><span data-stu-id="6a587-193">**Designer zoom** – You can zoom the designer view in and out to better view the content on the POS screen.</span></span> <span data-ttu-id="6a587-194">この機能は、POS 画面の解像度がデザイナーで使用されている画面の解像度と大幅に異なる場合に便利です。</span><span class="sxs-lookup"><span data-stu-id="6a587-194">This feature is useful when the screen resolution on the POS differs greatly from the resolution of the screen that is used in the designer.</span></span>
- <span data-ttu-id="6a587-195">**ナビゲーション バーの表示/非表示** – フル POS レイアウトでは、**トランザクション**画面に左側のナビゲーション バーを表示するかどうかを選択できます。</span><span class="sxs-lookup"><span data-stu-id="6a587-195">**Show/hide navigation bar** – For Full POS layouts, you can select whether the left navigation bar is visible on the **Transaction** screen.</span></span> <span data-ttu-id="6a587-196">この機能は、表示の解像度が低い場合に便利です。</span><span class="sxs-lookup"><span data-stu-id="6a587-196">This feature is helpful for displays that have a lower resolution.</span></span> <span data-ttu-id="6a587-197">可視性を設定するには、デザイナー内のナビゲーション バーを右クリックし、**常に表示**チェック ボックスをオンまたはオフにします。</span><span class="sxs-lookup"><span data-stu-id="6a587-197">To set the visibility, right-click the navigation bar in the designer, and select or clear the **Always visible** check box.</span></span> <span data-ttu-id="6a587-198">ナビゲーション バーが表示されていない場合でも、POS ユーザーは左上のメニューを使用することでアクセスできます。</span><span class="sxs-lookup"><span data-stu-id="6a587-198">If the navigation bar is hidden, POS users can still access it by using the menu in the upper left.</span></span>

    ![ナビゲーション バーの表示/非表示](../retail/media/Navigation-Bar.PNG)

- <span data-ttu-id="6a587-200">**POS コントロール** – POS レイアウト デザイナーは次のコントロールをサポートします。</span><span class="sxs-lookup"><span data-stu-id="6a587-200">**POS controls** – The POS layout designer supports the following controls.</span></span> <span data-ttu-id="6a587-201">右クリックしてショートカット メニューを使用することで、多くのコントロールをコンフィギュレーションできます。</span><span class="sxs-lookup"><span data-stu-id="6a587-201">You can configure many controls by right-clicking and using the shortcut menu.</span></span>

    ![POS UI コントロール](../retail/media/POS-UI-Controls.png)

    - <span data-ttu-id="6a587-203">**テンキー** – テンキーは、POS **トランザクション**画面のユーザー入力の主なメカニズムです。</span><span class="sxs-lookup"><span data-stu-id="6a587-203">**Number pad** – The number pad is the main mechanism for user input on the POS **Transaction** screen.</span></span> <span data-ttu-id="6a587-204">コントロールをコンフィギュレーションして、完全なテンキーが表示されるようにします。</span><span class="sxs-lookup"><span data-stu-id="6a587-204">You can configure the control so that the full number pad is shown.</span></span> <span data-ttu-id="6a587-205">このオプションは、タッチ スクリーン デバイスに最適です。</span><span class="sxs-lookup"><span data-stu-id="6a587-205">This option is ideal for touchscreen devices.</span></span> <span data-ttu-id="6a587-206">また、入力フィールドのみが表示されるようにコンフィギュレーションすることもできます。</span><span class="sxs-lookup"><span data-stu-id="6a587-206">Alternatively, you can configure it so that only the input field is shown.</span></span> <span data-ttu-id="6a587-207">この場合、物理的なキーボードは入力に使用されます。</span><span class="sxs-lookup"><span data-stu-id="6a587-207">In this case, a physical keyboard is used for input.</span></span> <span data-ttu-id="6a587-208">テンキーの設定は、フル レイアウトでのみ使用できます。</span><span class="sxs-lookup"><span data-stu-id="6a587-208">The number pad settings are available only for Full layouts.</span></span> <span data-ttu-id="6a587-209">コンパクト レイアウトでは、完全なテンキーは常に**トランザクション**画面に表示されます。</span><span class="sxs-lookup"><span data-stu-id="6a587-209">For Compact layouts, the full number pad is always shown on the **Transaction** screen.</span></span>
    - <span data-ttu-id="6a587-210">**合計パネル** – 合計パネルを 1 列または 2 列でコンフィギュレーションして、行数、割引額、料金、小計、および税金などの値を表示できます。</span><span class="sxs-lookup"><span data-stu-id="6a587-210">**Totals panel** – You can configure the totals panel in either one column or two columns, to show values such as the line count, discount amount, charges, subtotal, and tax.</span></span> <span data-ttu-id="6a587-211">コンパクト レイアウトは、1 つの列だけをサポートします。</span><span class="sxs-lookup"><span data-stu-id="6a587-211">Compact layouts support only a single column.</span></span>
    - <span data-ttu-id="6a587-212">**入庫パネル** – 入庫パネルには、POS で処理された製品およびサービスの販売明細行、支払明細行、および配送情報が含まれています。</span><span class="sxs-lookup"><span data-stu-id="6a587-212">**Receipt panel** – The receipt panel contains the sales lines, payment lines, and delivery information for the products and services that are processed in the POS.</span></span> <span data-ttu-id="6a587-213">列、幅、および配置を指定できます。</span><span class="sxs-lookup"><span data-stu-id="6a587-213">You can specify columns, widths, and placement.</span></span> <span data-ttu-id="6a587-214">コンパクト レイアウトでは、メイン明細行の下の行に表示される追加の情報をコンフィギュレーションすることもできます。</span><span class="sxs-lookup"><span data-stu-id="6a587-214">In Compact layouts, you can also configure additional information that appears in the row under the main line.</span></span>
    - <span data-ttu-id="6a587-215">**顧客カード** – 顧客カードには、現在のトランザクションに関連付けられている顧客に関する情報が表示されます。</span><span class="sxs-lookup"><span data-stu-id="6a587-215">**Customer card** – The customer card shows information about the customer who is associated with the current transaction.</span></span> <span data-ttu-id="6a587-216">顧客カードをコンフィギュレーションして、追加情報を非表示または表示することができます。</span><span class="sxs-lookup"><span data-stu-id="6a587-216">You can configure the customer card to hide or show additional information.</span></span>
    - <span data-ttu-id="6a587-217">**タブ コントロール** – タブ コントロールは画面レイアウト上に置くことができ、テンキー、顧客カード、ボタン グリッドなどの他のコントロールも配置することができます。</span><span class="sxs-lookup"><span data-stu-id="6a587-217">**Tab control** – You can add the tab control to a screen layout, and then put other controls, such as the number pad, customer card, or button grids, in it.</span></span> <span data-ttu-id="6a587-218">タブ コントロールは、画面により多くのコンテンツを収めるのを助けるコンテナーです。</span><span class="sxs-lookup"><span data-stu-id="6a587-218">The tab control is a container that helps you fit more content on the screen.</span></span> <span data-ttu-id="6a587-219">タブ コントロールは、フル レイアウトでのみ使用できます。</span><span class="sxs-lookup"><span data-stu-id="6a587-219">The tab control is available only for Full layouts.</span></span>
    - <span data-ttu-id="6a587-220">**画像** – イメージ コントロールを使用して、店舗のロゴやその他のブランド イメージを**トランザクション**画面に表示することができます。</span><span class="sxs-lookup"><span data-stu-id="6a587-220">**Image** – You can use the image control to show the store's logo or another branding image on the **Transaction** screen.</span></span> <span data-ttu-id="6a587-221">イメージ コントロールは、フル レイアウトでのみ使用できます。</span><span class="sxs-lookup"><span data-stu-id="6a587-221">The image control is available only for Full layouts.</span></span>
    - <span data-ttu-id="6a587-222">**お勧めの製品** – お勧めの製品コントロールが環境用に構成されている場合は、機械学習に基づく製品候補を表示します。</span><span class="sxs-lookup"><span data-stu-id="6a587-222">**Recommended products** – If the recommended products control is configured for the environment, it shows product suggestions, based on machine learning.</span></span>
    - <span data-ttu-id="6a587-223">**カスタム コントロール** – カスタム コントロールは、画面レイアウト内のプレース ホルダーとして機能し、カスタム コンテンツ用のスペースを確保できるようにします。</span><span class="sxs-lookup"><span data-stu-id="6a587-223">**Custom control** – The custom control acts as a placeholder in the screen layout and lets you reserve space for custom content.</span></span> <span data-ttu-id="6a587-224">カスタム コントロールは、フル レイアウトでのみ使用できます。</span><span class="sxs-lookup"><span data-stu-id="6a587-224">The custom control is available only for Full layouts.</span></span>

### <a name="compact-layout-designer"></a><span data-ttu-id="6a587-225">コンパクト レイアウト デザイナー</span><span class="sxs-lookup"><span data-stu-id="6a587-225">Compact layout designer</span></span>

<span data-ttu-id="6a587-226">フル レイアウト デザイナーと同様、コンパクト レイアウト デザイナーでは電話や小さなタブレット用の POS 画面レイアウトをコンフィギュレーションできます。</span><span class="sxs-lookup"><span data-stu-id="6a587-226">Like the Full layout designer, the Compact layout designer lets you configure the POS screen layout for phones and small tablets.</span></span> <span data-ttu-id="6a587-227">ただし、この場合は、レイアウト自体は固定されています。</span><span class="sxs-lookup"><span data-stu-id="6a587-227">However, in this case, the layout itself is fixed.</span></span> <span data-ttu-id="6a587-228">右クリックしてショートカット メニューを使用することで、レイアウトのコントロールをコンフィギュレーションできます。</span><span class="sxs-lookup"><span data-stu-id="6a587-228">You can configure the controls in the layout by right-clicking and using the shortcut menu.</span></span> <span data-ttu-id="6a587-229">ただし、追加のコンテンツにドラッグ アンド ドロップ操作を使用することはできません。</span><span class="sxs-lookup"><span data-stu-id="6a587-229">However, you can't use drag-and-drop operations for additional content.</span></span>

![コンパクト レイアウト デザイナー](../retail/media/Compact-Layout-Designer.png)

### <a name="button-grid-designer"></a><span data-ttu-id="6a587-231">ボタン グリッド デザイナー</span><span class="sxs-lookup"><span data-stu-id="6a587-231">Button grid designer</span></span>

<span data-ttu-id="6a587-232">ボタン グリッドのデザイナーにより、フルおよびコンパクト両方のレイアウトの、POS ようこそ画面および**トランザクション**画面で使用可能なボタン グリッドをコンフィギュレーションできます。</span><span class="sxs-lookup"><span data-stu-id="6a587-232">The button grid designer lets you configure button grids that can be used on the POS welcome screen and **Transaction** screen for both Full and Compact layouts.</span></span> <span data-ttu-id="6a587-233">さまざまなレイアウトとレイアウト タイプで、同じボタン グリッドを使用できます。</span><span class="sxs-lookup"><span data-stu-id="6a587-233">The same button grid can be used across layouts and layout types.</span></span> <span data-ttu-id="6a587-234">画面レイアウト デザイナーと同様、ボタン グリッド デザイナーは、ユーザーがアクセスするたびに ClickOnce の配置テクノロジーを使用してアプリケーションの最新バージョンをダウンロード、インストール、および起動します。</span><span class="sxs-lookup"><span data-stu-id="6a587-234">Like the screen layout designer, the button grid designer uses the ClickOnce deployment technology to download, install, and start the latest version of the application every time that users access it.</span></span> <span data-ttu-id="6a587-235">必ず ClickOnce のブラウザの要件を確認してください。</span><span class="sxs-lookup"><span data-stu-id="6a587-235">Be sure to check the browser requirements for ClickOnce.</span></span> <span data-ttu-id="6a587-236">Google Chrome などの一部のブラウザーでは、拡張機能が必要です。</span><span class="sxs-lookup"><span data-stu-id="6a587-236">Some browsers, such as Google Chrome, require extensions.</span></span>

![ボタン グリッド デザイナー](../retail/media/Button-Grid-Designer.png)

- <span data-ttu-id="6a587-238">**新しいボタン** – クリックして、ボタン グリッドに新しいボタンを追加します。</span><span class="sxs-lookup"><span data-stu-id="6a587-238">**New button** – Click to add a new button to the button grid.</span></span> <span data-ttu-id="6a587-239">既定では、新しいボタンはグリッドの左上隅に表示されます。</span><span class="sxs-lookup"><span data-stu-id="6a587-239">By default, new buttons appear in the upper-left corner of the grid.</span></span> <span data-ttu-id="6a587-240">ただし、レイアウトにドラッグしてボタンを並べ替えることもできます。</span><span class="sxs-lookup"><span data-stu-id="6a587-240">However, you can arrange buttons by dragging them in the layout.</span></span>

    > [!IMPORTANT]
    > <span data-ttu-id="6a587-241">ボタン グリッドのコンテンツは重複することがあります。</span><span class="sxs-lookup"><span data-stu-id="6a587-241">The contents of the button grid can overlap.</span></span> <span data-ttu-id="6a587-242">ボタンを並べ替えた場合は、その他のボタンと重複していないかを確認します。</span><span class="sxs-lookup"><span data-stu-id="6a587-242">When you arrange buttons, make sure that they don't hide other buttons.</span></span>

- <span data-ttu-id="6a587-243">**新しいデザイン** – クリックすると、行および列ごとのボタンの数を指定して、ボタン グリッド レイアウトを自動的に設定します。</span><span class="sxs-lookup"><span data-stu-id="6a587-243">**New design** – Click to automatically set up a button grid layout by specifying the number of buttons per row and column.</span></span>
- <span data-ttu-id="6a587-244">**ボタン プロパティ** – ボタンを右クリックし、ショートカット メニューを使用することで、ボタン プロパティをコンフィギュレーションできます。</span><span class="sxs-lookup"><span data-stu-id="6a587-244">**Button properties** – You can configure button properties by right-clicking the button and using the shortcut menu.</span></span>

    > [!IMPORTANT]
    > <span data-ttu-id="6a587-245">一部のボタン グリッドの設定は、Retail Modern POS やクラウド POS ではなく、エンタープライズ POS にのみ適用されます。</span><span class="sxs-lookup"><span data-stu-id="6a587-245">Some button grid settings apply only to Enterprise POS, not to Retail Modern POS or Cloud POS.</span></span>

    ![ボタン グリッドのボタン プロパティ](../retail/media/Button-grid-button-properties.png)

    - <span data-ttu-id="6a587-247">**アクション** – 該当する POS の操作の一覧で、POS でボタンがクリックされるときに呼び出される操作を選択します。</span><span class="sxs-lookup"><span data-stu-id="6a587-247">**Action** – In the list of applicable POS operations, select the operation that is invoked when the button is clicked in the POS.</span></span>

        <span data-ttu-id="6a587-248">サポートされている POS 操作の一覧については、[オンラインおよびオフラインでの POS 操作](pos-operations.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="6a587-248">For the list of supported POS operations, see [POS operations, online and offline](pos-operations.md).</span></span>

    - <span data-ttu-id="6a587-249">**アクション パラメーター** – 一部の POS 操作は呼び出されるとき、追加のパラメーターを使用します。</span><span class="sxs-lookup"><span data-stu-id="6a587-249">**Action parameters** – Some POS operations use additional parameters when they are invoked.</span></span> <span data-ttu-id="6a587-250">たとえば、製品の追加の操作の際、ユーザーは追加する製品を指定できます。</span><span class="sxs-lookup"><span data-stu-id="6a587-250">For example, for the Add product operation, users can specify the product to add.</span></span>
    - <span data-ttu-id="6a587-251">**ボタン テキスト** – POS のボタンに表示されるテキストを指定します。</span><span class="sxs-lookup"><span data-stu-id="6a587-251">**Button text** – Specify the text that appears on the button in the POS.</span></span>
    - <span data-ttu-id="6a587-252">**ボタン テキストの非表示** – このチェック ボックスを使用して、ボタンのテキストを表示または非表示にします。</span><span class="sxs-lookup"><span data-stu-id="6a587-252">**Hide button text** – Use this check box to hide or show the button text.</span></span> <span data-ttu-id="6a587-253">ボタン テキストは多くの場合、アイコンのみが表示される小さなボタンのために非表示になっています。</span><span class="sxs-lookup"><span data-stu-id="6a587-253">Button text is often hidden for small buttons that show only an icon.</span></span>
    - <span data-ttu-id="6a587-254">**ツール ヒント** – ユーザーがボタンの上にマウスを重ねるときに表示される追加のヘルプ テキストを指定します。</span><span class="sxs-lookup"><span data-stu-id="6a587-254">**Tooltip** – Specify additional Help text that appears when users mouse over the button.</span></span>
    - <span data-ttu-id="6a587-255">**列内のサイズ/行内のサイズ** – ボタンの高さと幅を指定できます。</span><span class="sxs-lookup"><span data-stu-id="6a587-255">**Size in columns/Size in rows** – You can specify how tall and wide the button is.</span></span>

        ![行および列内の POS ボタン サイズ](../retail/media/POS-Button-Sizes-In-Rows-And-Columns.png)

    - <span data-ttu-id="6a587-257">**カスタム フォント** – **POS のカスタム フォントの有効化**チェック ボックスを選択するとき、POS の既定のシステム フォント以外のフォントを指定することができます。</span><span class="sxs-lookup"><span data-stu-id="6a587-257">**Custom font** – When you select the **Enable custom font for POS** check box, you can specify a font other than the default system font for the POS.</span></span>
    - <span data-ttu-id="6a587-258">**カスタム テーマ** – 既定では、POS ボタンは視覚プロファイルからアクセント色を使用します。</span><span class="sxs-lookup"><span data-stu-id="6a587-258">**Custom theme** – By default, POS buttons use the accent color from the visual profile.</span></span> <span data-ttu-id="6a587-259">**カスタム テーマの使用**チェック ボックスを選択すると、 追加の色を指定することができます。</span><span class="sxs-lookup"><span data-stu-id="6a587-259">When you select the **Use custom theme** check box, you can specify additional colors.</span></span>

        > [!NOTE]
        > <span data-ttu-id="6a587-260">Retail Modern POS およびクラウド POS は**背景色**および**フォントの色**のみを使用します。</span><span class="sxs-lookup"><span data-stu-id="6a587-260">Retail Modern POS and Cloud POS use only the **Back color** and **Font color** values.</span></span>

    - <span data-ttu-id="6a587-261">**ボタン画像** – ボタンには、画像かアイコンを含めることができます。</span><span class="sxs-lookup"><span data-stu-id="6a587-261">**Button image** – Buttons can include images or icons.</span></span> <span data-ttu-id="6a587-262">**小売\>チャンネル設定\>POS 設定\>POS\>画像**で指定されている利用可能な画像の中から選択します。</span><span class="sxs-lookup"><span data-stu-id="6a587-262">Select among the available images that are specified at **Retail \> Channel setup \> POS setup \> POS \> Images**.</span></span>

![POS でのボタン グリッドの例](../retail/media/Example-Button-Grid-In-POS.png)

## <a name="additional-resources"></a><span data-ttu-id="6a587-264">その他のリソース</span><span class="sxs-lookup"><span data-stu-id="6a587-264">Additional resources</span></span>

[<span data-ttu-id="6a587-265">Retail POS のレイアウト デザイナーのインストール</span><span class="sxs-lookup"><span data-stu-id="6a587-265">Install the Retail POS Layout designer</span></span>](install-pos-layout-designer.md)
