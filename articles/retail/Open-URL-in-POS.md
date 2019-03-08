---
title: POS で URL を開く
description: このトピックでは、Microsoft Dynamics 365 for Retail の製品および顧客検索機能に加えられた改良の概要を示します。
author: AamirAllaq
manager: AnnBe
ms.date: 01/28/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application user
ms.reviewer: sericks
ms.search.scope: Core, Operations, Retail
ms.custom: 141393
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Retail
ms.author: shajain
ms.search.validFrom: 2018-10-30
ms.dyn365.ops.version: 8.1.1
ms.openlocfilehash: b07406b4e218b45bdde87c4a579814fe0edbc286
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/29/2019
ms.locfileid: "327093"
---
# <a name="open-url-in-pos"></a><span data-ttu-id="67f74-103">POS で URL を開く</span><span class="sxs-lookup"><span data-stu-id="67f74-103">Open URL in POS</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="67f74-104">このトピックでは、小売販売時点管理 (POS) のボタンをコンフィギュレーションして URL を開く方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="67f74-104">This topic describes how you can configure a button in Retail point of sale (POS) to open a URL.</span></span> <span data-ttu-id="67f74-105">この機能はコードのカスタマイズを必要とせず、開発者以外のロールのユーザーがコンフィギュレーションすることもできます。</span><span class="sxs-lookup"><span data-stu-id="67f74-105">This feature does not require a code customization, and can be configured by someone in a non-developer role.</span></span> <span data-ttu-id="67f74-106">この機能は、Dynamics 365 for Finance and Operations バージョン 8.1.3 リリース (ビルド 8.1.227.10014) 以降の一部として使用可能です。</span><span class="sxs-lookup"><span data-stu-id="67f74-106">This feature is available as part of the Dynamics 365 for Finance and Operations version 8.1.3 release (build 8.1.227.10014) and later.</span></span> 

<span data-ttu-id="67f74-107">この機能では、ボタン グリッド デザイナーを使用して URL を開くことで、POS のボタンをコンフィギュレーションすることができます。</span><span class="sxs-lookup"><span data-stu-id="67f74-107">This feature allows configuration of a button in POS, using the button grid designer to open a URL.</span></span> <span data-ttu-id="67f74-108">現時点では、これは次のコンフィギュレーションでサポートされています:</span><span class="sxs-lookup"><span data-stu-id="67f74-108">Currently, this is supported in the following configurations:</span></span>

- <span data-ttu-id="67f74-109">新しいウィンドウで開きます。</span><span class="sxs-lookup"><span data-stu-id="67f74-109">Open in new window.</span></span>
- <span data-ttu-id="67f74-110">POS 内で開きます。</span><span class="sxs-lookup"><span data-stu-id="67f74-110">Open within POS.</span></span>
- <span data-ttu-id="67f74-111">ネイティブ アプリを開きます。</span><span class="sxs-lookup"><span data-stu-id="67f74-111">Open a native app.</span></span>

## <a name="open-in-new-window"></a><span data-ttu-id="67f74-112">新しいウィンドウで開く</span><span class="sxs-lookup"><span data-stu-id="67f74-112">Open in new window</span></span>

<span data-ttu-id="67f74-113">このコンフィギュレーションは、URL を新しいウィンドウで開くか、アプリ内で開くかどうかを定義します。</span><span class="sxs-lookup"><span data-stu-id="67f74-113">This configuration defines whether to open the URL in a new window or within the app.</span></span> <span data-ttu-id="67f74-114">アプリ内で Web URL を開くようにコンフィギュレーションされている場合は、サイド ナビゲーション ウィンドウおよび POS 上部のバーが表示され、ユーザー操作が可能になります。</span><span class="sxs-lookup"><span data-stu-id="67f74-114">When configured to open a web URL within the app, the side navigation panel and top bar of POS are visible and available for user interaction.</span></span> <span data-ttu-id="67f74-115">新しいウィンドウで開くようにコンフィギュレーションされている場合は、URL は Windows 用の Modern POS の新しいアプリ ウィンドウ、およびその他のすべての POS クライアントの新しいブラウザー タブで開きます。</span><span class="sxs-lookup"><span data-stu-id="67f74-115">When configured to open in a new window, the URL will open in a new app window on Modern POS for Windows, and in a new browser tab in all other POS clients.</span></span> <span data-ttu-id="67f74-116">これを有効にするには、**新しいウィンドウで開く**オプションを選択して URL をコンフィギュレーションする必要があります。</span><span class="sxs-lookup"><span data-stu-id="67f74-116">To enable this, you must configure the URL with the **Open in new window** option selected.</span></span>

## <a name="open-within-pos"></a><span data-ttu-id="67f74-117">POS 内で開く</span><span class="sxs-lookup"><span data-stu-id="67f74-117">Open within POS</span></span>

<span data-ttu-id="67f74-118">POS 内で Web URL を開くことは、現在 Windows 用 Modern POS に対してのみサポートされています。</span><span class="sxs-lookup"><span data-stu-id="67f74-118">Opening a web URL within POS is currently only supported for Modern POS on Windows.</span></span> <span data-ttu-id="67f74-119">他のクライアントでは、この機能は現在開発中で、将来の更新でリリースされる予定です。</span><span class="sxs-lookup"><span data-stu-id="67f74-119">On other clients, this capability is under development and planned for release in future updates.</span></span> <span data-ttu-id="67f74-120">これを有効にするには、**新しいウィンドウで開く**オプションを選択せずに URL をコンフィギュレーションする必要があります。</span><span class="sxs-lookup"><span data-stu-id="67f74-120">To enable this, you must configure the URL with the **Open in new window** option not selected.</span></span>

## <a name="open-a-native-app"></a><span data-ttu-id="67f74-121">ネイティブ アプリを開く</span><span class="sxs-lookup"><span data-stu-id="67f74-121">Open a native app</span></span>

<span data-ttu-id="67f74-122">この機能では、ネイティブ アプリを開くための Web 以外の URL を指定することもできます。</span><span class="sxs-lookup"><span data-stu-id="67f74-122">This feature also allows you to specify non-web URLs to open a native app.</span></span> <span data-ttu-id="67f74-123">たとえば、MailTo、SIP、IM、または MSTEAMS などの、ホスト デバイス上のそれぞれのネイティブ アプリで処理できる URL プロトコルを指定できます。</span><span class="sxs-lookup"><span data-stu-id="67f74-123">For example, you can specify URL protocols such as MailTo, SIP, IM, or MSTEAMS, which can then be handled by respective native apps on the host device.</span></span> <span data-ttu-id="67f74-124">これを有効にするには、**新しいウィンドウで開く**オプションを選択して URL をコンフィギュレーションする必要があります。</span><span class="sxs-lookup"><span data-stu-id="67f74-124">To enable this, you must configure the URL with the **Open in new window** option selected.</span></span>

- <span data-ttu-id="67f74-125">Windows のコンピューターで、Deployment Image Servicing and Management (DISM) を使用してコンピューターを設定している場合は、[既定のアプリケーション アソシエーションをエクスポートまたはインポートする](https://docs.microsoft.com/windows-hardware/manufacture/desktop/export-or-import-default-application-associations) を参照して、既定のプロトコル アソシエーションを設定できます。</span><span class="sxs-lookup"><span data-stu-id="67f74-125">For Windows computers, see [Export or Import Default Application Associations](https://docs.microsoft.com/windows-hardware/manufacture/desktop/export-or-import-default-application-associations) to set the default protocol associations if you are setting up your computer using Deployment Image Servicing and Management (DISM).</span></span>
- <span data-ttu-id="67f74-126">Intune のような MDM を使用して Windows コンピューターを管理している場合は、[ポリシー CSP - ApplicationDefaults](https://docs.microsoft.com/windows/client-management/mdm/policy-csp-applicationdefaults) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="67f74-126">If you are using MDM, such as Intune to manage your Windows computers, see [Policy CSP - ApplicationDefaults](https://docs.microsoft.com/windows/client-management/mdm/policy-csp-applicationdefaults).</span></span>
- <span data-ttu-id="67f74-127">カスタム Web サイトを構築する開発者の場合は、[URI の規定のアプリを起動する](https://docs.microsoft.com/windows/uwp/launch-resume/launch-default-app) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="67f74-127">If you are a developer building a custom website, see [Launch the default app for a URI](https://docs.microsoft.com/windows/uwp/launch-resume/launch-default-app).</span></span>

## <a name="open-a-native-app-seamlessly"></a><span data-ttu-id="67f74-128">ネイティブ アプリをシームレスに開く</span><span class="sxs-lookup"><span data-stu-id="67f74-128">Open a native app seamlessly</span></span>

<span data-ttu-id="67f74-129">Windows、iOS、および Android では、アプリ プロトコル アソシエーションに基づいてアプリをよりシームレスに開くことが可能になります。</span><span class="sxs-lookup"><span data-stu-id="67f74-129">Windows, iOS, and Android also allow opening of apps more seamlessly, based on app protocol association.</span></span> <span data-ttu-id="67f74-130">アプリがまだ Web ブラウザから開くことを処理するようにコンフィギュレーションされていない場合、これをコンフィギュレーションするには開発者が必要な場合があります。</span><span class="sxs-lookup"><span data-stu-id="67f74-130">If your app is not already configured to handle opening from a web browser, you may need a developer to configure this.</span></span>

- <span data-ttu-id="67f74-131">Windows の場合は、[アプリ URI ハンドラーを使用して Web サイトのアプリを有効にする](https://docs.microsoft.com/windows/uwp/launch-resume/web-to-app-linking) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="67f74-131">For Windows, see [Enable apps for websites using app URI handlers](https://docs.microsoft.com/windows/uwp/launch-resume/web-to-app-linking).</span></span>
- <span data-ttu-id="67f74-132">iOS の場合は、[開発者向けの汎用リンク](https://developer.apple.com/ios/universal-links/) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="67f74-132">For iOS, see [Universal Links for Developers](https://developer.apple.com/ios/universal-links/).</span></span>
- <span data-ttu-id="67f74-133">Android の場合は、[Android アプリの操作リンク](https://developer.android.com/training/app-links/)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="67f74-133">For Android, see [Handling Android App Links](https://developer.android.com/training/app-links/).</span></span>

| <span data-ttu-id="67f74-134">クライアント</span><span class="sxs-lookup"><span data-stu-id="67f74-134">Client</span></span>                | <span data-ttu-id="67f74-135">新しいウィンドウで開く</span><span class="sxs-lookup"><span data-stu-id="67f74-135">Open in new window</span></span> | <span data-ttu-id="67f74-136">ネイティブ アプリを開く</span><span class="sxs-lookup"><span data-stu-id="67f74-136">Open native app</span></span> | <span data-ttu-id="67f74-137">POS 内で開く</span><span class="sxs-lookup"><span data-stu-id="67f74-137">Open within POS</span></span> | <span data-ttu-id="67f74-138">詳細情報</span><span class="sxs-lookup"><span data-stu-id="67f74-138">Details</span></span>                           |
|-----------------------|--------------------|-----------------|-----------------|-----------------------------------|
| <span data-ttu-id="67f74-139">Windows 上の Modern POS</span><span class="sxs-lookup"><span data-stu-id="67f74-139">Modern POS on Windows</span></span> | <span data-ttu-id="67f74-140">✓\*</span><span class="sxs-lookup"><span data-stu-id="67f74-140">✓\*</span></span>                | <span data-ttu-id="67f74-141">✓</span><span class="sxs-lookup"><span data-stu-id="67f74-141">✓</span></span>               | <span data-ttu-id="67f74-142">✓</span><span class="sxs-lookup"><span data-stu-id="67f74-142">✓</span></span>              | <span data-ttu-id="67f74-143">\*新しい Modern POS ウィンドウで開く</span><span class="sxs-lookup"><span data-stu-id="67f74-143">\* Opens in new Modern POS window</span></span> |
| <span data-ttu-id="67f74-144">クラウド POS</span><span class="sxs-lookup"><span data-stu-id="67f74-144">Cloud POS</span></span>             | <span data-ttu-id="67f74-145">✓\*</span><span class="sxs-lookup"><span data-stu-id="67f74-145">✓\*</span></span>                | <span data-ttu-id="67f74-146">✓</span><span class="sxs-lookup"><span data-stu-id="67f74-146">✓</span></span>               | <span data-ttu-id="67f74-147">x</span><span class="sxs-lookup"><span data-stu-id="67f74-147">X</span></span>              | <span data-ttu-id="67f74-148">\*新しいブラウザー タブで開く</span><span class="sxs-lookup"><span data-stu-id="67f74-148">\* Opens in new browser tab</span></span>        |
| <span data-ttu-id="67f74-149">iOS 上の Modern POS</span><span class="sxs-lookup"><span data-stu-id="67f74-149">Modern POS on iOS</span></span>     | <span data-ttu-id="67f74-150">✓\*</span><span class="sxs-lookup"><span data-stu-id="67f74-150">✓\*</span></span>                | <span data-ttu-id="67f74-151">✓</span><span class="sxs-lookup"><span data-stu-id="67f74-151">✓</span></span>               | <span data-ttu-id="67f74-152">x</span><span class="sxs-lookup"><span data-stu-id="67f74-152">X</span></span>              | <span data-ttu-id="67f74-153">\*新しいブラウザー タブで開く</span><span class="sxs-lookup"><span data-stu-id="67f74-153">\* Opens in new browser tab</span></span>        |
| <span data-ttu-id="67f74-154">Android 上の Modern POS</span><span class="sxs-lookup"><span data-stu-id="67f74-154">Modern POS on Android</span></span> | <span data-ttu-id="67f74-155">✓\*</span><span class="sxs-lookup"><span data-stu-id="67f74-155">✓\*</span></span>                | <span data-ttu-id="67f74-156">✓</span><span class="sxs-lookup"><span data-stu-id="67f74-156">✓</span></span>               | <span data-ttu-id="67f74-157">x</span><span class="sxs-lookup"><span data-stu-id="67f74-157">X</span></span>              | <span data-ttu-id="67f74-158">\*新しいブラウザー タブで開く</span><span class="sxs-lookup"><span data-stu-id="67f74-158">\* Opens in new browser tab</span></span>        |

## <a name="before-you-begin"></a><span data-ttu-id="67f74-159">準備</span><span class="sxs-lookup"><span data-stu-id="67f74-159">Before you begin</span></span>

<span data-ttu-id="67f74-160">開始する前に、[販売時点管理 (POS) の画面レイアウト](pos-screen-layouts.md) をコンフィギュレーションする方法を確認します。</span><span class="sxs-lookup"><span data-stu-id="67f74-160">Before you begin, review how to configure [Screen layouts for the point of sale (POS)](pos-screen-layouts.md).</span></span>

## <a name="open-url-in-pos"></a><span data-ttu-id="67f74-161">POS で URL を開く</span><span class="sxs-lookup"><span data-stu-id="67f74-161">Open URL in POS</span></span>

<span data-ttu-id="67f74-162">POS で開くように URL をコンフィギュレーションするには、次の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="67f74-162">To configure a URL to be opened in POS, perform the following steps.</span></span>

1. <span data-ttu-id="67f74-163">本社で、**小売 \>チャネル設定 \> POS 設定 \> POS \> 画面レイアウト**に移動します。</span><span class="sxs-lookup"><span data-stu-id="67f74-163">In head office, go to **Retail \> Channel Setup \> POS Setup \> POS \> Screen Layouts**.</span></span>
2. <span data-ttu-id="67f74-164">**ボタン グリッド \> デザイナー**を選択します。</span><span class="sxs-lookup"><span data-stu-id="67f74-164">Select **Button Grids \> Designer**.</span></span>
3. <span data-ttu-id="67f74-165">新しいボタンを作成します。</span><span class="sxs-lookup"><span data-stu-id="67f74-165">Create a new button.</span></span>
4. <span data-ttu-id="67f74-166">**ボタン**プロパティを選択します。</span><span class="sxs-lookup"><span data-stu-id="67f74-166">Select **Button** properties.</span></span>
5. <span data-ttu-id="67f74-167">アクションとして **URL を開く**を選択します。</span><span class="sxs-lookup"><span data-stu-id="67f74-167">Select **Open URL** as the action.</span></span>
6. <span data-ttu-id="67f74-168">使用する URL を入力します。</span><span class="sxs-lookup"><span data-stu-id="67f74-168">Enter the URL that you want to use.</span></span>
7. <span data-ttu-id="67f74-169">新しいウィンドウで URL を開くかどうかをコンフィギュレーションします。</span><span class="sxs-lookup"><span data-stu-id="67f74-169">Configure whether to open the URL in a new window.</span></span>
