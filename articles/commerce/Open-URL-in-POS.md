---
title: POS で URL を開く
description: このトピックでは、Dynamics 365 Commerce の製品および顧客検索機能に加えられた改良の概要を示します。
author: AamirAllaq
manager: AnnBe
ms.date: 01/28/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application user
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 141393
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Retail
ms.author: shajain
ms.search.validFrom: 2018-10-30
ms.dyn365.ops.version: 8.1.1
ms.openlocfilehash: 137b699d5f60b9b62a5ce9501e3b2a262e60a88f
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/13/2020
ms.locfileid: "4413660"
---
# <a name="open-url-in-pos"></a><span data-ttu-id="b28f9-103">POS で URL を開く</span><span class="sxs-lookup"><span data-stu-id="b28f9-103">Open URL in POS</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="b28f9-104">このトピックでは、小売販売時点管理 (POS) のボタンをコンフィギュレーションして URL を開く方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="b28f9-104">This topic describes how you can configure a button in Retail point of sale (POS) to open a URL.</span></span> <span data-ttu-id="b28f9-105">この機能はコードのカスタマイズを必要とせず、開発者以外のロールのユーザーがコンフィギュレーションすることもできます。</span><span class="sxs-lookup"><span data-stu-id="b28f9-105">This feature does not require a code customization, and can be configured by someone in a non-developer role.</span></span> 

<span data-ttu-id="b28f9-106">この機能では、ボタン グリッド デザイナーを使用して URL を開くことで、POS のボタンをコンフィギュレーションすることができます。</span><span class="sxs-lookup"><span data-stu-id="b28f9-106">This feature allows configuration of a button in POS, using the button grid designer to open a URL.</span></span> <span data-ttu-id="b28f9-107">現時点では、これは次のコンフィギュレーションでサポートされています:</span><span class="sxs-lookup"><span data-stu-id="b28f9-107">Currently, this is supported in the following configurations:</span></span>

- <span data-ttu-id="b28f9-108">新しいウィンドウで開きます。</span><span class="sxs-lookup"><span data-stu-id="b28f9-108">Open in new window.</span></span>
- <span data-ttu-id="b28f9-109">POS 内で開きます。</span><span class="sxs-lookup"><span data-stu-id="b28f9-109">Open within POS.</span></span>
- <span data-ttu-id="b28f9-110">ネイティブ アプリを開きます。</span><span class="sxs-lookup"><span data-stu-id="b28f9-110">Open a native app.</span></span>

## <a name="open-in-new-window"></a><span data-ttu-id="b28f9-111">新しいウィンドウで開く</span><span class="sxs-lookup"><span data-stu-id="b28f9-111">Open in new window</span></span>

<span data-ttu-id="b28f9-112">このコンフィギュレーションは、URL を新しいウィンドウで開くか、アプリ内で開くかどうかを定義します。</span><span class="sxs-lookup"><span data-stu-id="b28f9-112">This configuration defines whether to open the URL in a new window or within the app.</span></span> <span data-ttu-id="b28f9-113">アプリ内で Web URL を開くようにコンフィギュレーションされている場合は、サイド ナビゲーション ウィンドウおよび POS 上部のバーが表示され、ユーザー操作が可能になります。</span><span class="sxs-lookup"><span data-stu-id="b28f9-113">When configured to open a web URL within the app, the side navigation panel and top bar of POS are visible and available for user interaction.</span></span> <span data-ttu-id="b28f9-114">新しいウィンドウで開くようにコンフィギュレーションされている場合は、URL は Windows 用の Modern POS の新しいアプリ ウィンドウ、およびその他のすべての POS クライアントの新しいブラウザー タブで開きます。</span><span class="sxs-lookup"><span data-stu-id="b28f9-114">When configured to open in a new window, the URL will open in a new app window on Modern POS for Windows, and in a new browser tab in all other POS clients.</span></span> <span data-ttu-id="b28f9-115">これを有効にするには、**新しいウィンドウで開く** オプションを選択して URL をコンフィギュレーションする必要があります。</span><span class="sxs-lookup"><span data-stu-id="b28f9-115">To enable this, you must configure the URL with the **Open in new window** option selected.</span></span>

## <a name="open-within-pos"></a><span data-ttu-id="b28f9-116">POS 内で開く</span><span class="sxs-lookup"><span data-stu-id="b28f9-116">Open within POS</span></span>

<span data-ttu-id="b28f9-117">POS 内で Web URL を開くことは、現在 Windows 用 Modern POS に対してのみサポートされています。</span><span class="sxs-lookup"><span data-stu-id="b28f9-117">Opening a web URL within POS is currently only supported for Modern POS on Windows.</span></span> <span data-ttu-id="b28f9-118">他のクライアントでは、この機能は現在開発中で、将来の更新でリリースされる予定です。</span><span class="sxs-lookup"><span data-stu-id="b28f9-118">On other clients, this capability is under development and planned for release in future updates.</span></span> <span data-ttu-id="b28f9-119">これを有効にするには、**新しいウィンドウで開く** オプションを選択せずに URL をコンフィギュレーションする必要があります。</span><span class="sxs-lookup"><span data-stu-id="b28f9-119">To enable this, you must configure the URL with the **Open in new window** option not selected.</span></span>

## <a name="open-a-native-app"></a><span data-ttu-id="b28f9-120">ネイティブ アプリを開く</span><span class="sxs-lookup"><span data-stu-id="b28f9-120">Open a native app</span></span>

<span data-ttu-id="b28f9-121">この機能では、ネイティブ アプリを開くための Web 以外の URL を指定することもできます。</span><span class="sxs-lookup"><span data-stu-id="b28f9-121">This feature also allows you to specify non-web URLs to open a native app.</span></span> <span data-ttu-id="b28f9-122">たとえば、MailTo、SIP、IM、または MSTEAMS などの、ホスト デバイス上のそれぞれのネイティブ アプリで処理できる URL プロトコルを指定できます。</span><span class="sxs-lookup"><span data-stu-id="b28f9-122">For example, you can specify URL protocols such as MailTo, SIP, IM, or MSTEAMS, which can then be handled by respective native apps on the host device.</span></span> <span data-ttu-id="b28f9-123">これを有効にするには、**新しいウィンドウで開く** オプションを選択して URL をコンフィギュレーションする必要があります。</span><span class="sxs-lookup"><span data-stu-id="b28f9-123">To enable this, you must configure the URL with the **Open in new window** option selected.</span></span>

- <span data-ttu-id="b28f9-124">Windows のコンピューターで、Deployment Image Servicing and Management (DISM) を使用してコンピューターを設定している場合は、[既定のアプリケーション アソシエーションをエクスポートまたはインポートする](https://docs.microsoft.com/windows-hardware/manufacture/desktop/export-or-import-default-application-associations) を参照して、既定のプロトコル アソシエーションを設定できます。</span><span class="sxs-lookup"><span data-stu-id="b28f9-124">For Windows computers, see [Export or Import Default Application Associations](https://docs.microsoft.com/windows-hardware/manufacture/desktop/export-or-import-default-application-associations) to set the default protocol associations if you are setting up your computer using Deployment Image Servicing and Management (DISM).</span></span>
- <span data-ttu-id="b28f9-125">Intune のような MDM を使用して Windows コンピューターを管理している場合は、[ポリシー CSP - ApplicationDefaults](https://docs.microsoft.com/windows/client-management/mdm/policy-csp-applicationdefaults) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="b28f9-125">If you are using MDM, such as Intune to manage your Windows computers, see [Policy CSP - ApplicationDefaults](https://docs.microsoft.com/windows/client-management/mdm/policy-csp-applicationdefaults).</span></span>
- <span data-ttu-id="b28f9-126">カスタム Web サイトを構築する開発者の場合は、[URI の規定のアプリを起動する](https://docs.microsoft.com/windows/uwp/launch-resume/launch-default-app) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="b28f9-126">If you are a developer building a custom website, see [Launch the default app for a URI](https://docs.microsoft.com/windows/uwp/launch-resume/launch-default-app).</span></span>

## <a name="open-a-native-app-seamlessly"></a><span data-ttu-id="b28f9-127">ネイティブ アプリをシームレスに開く</span><span class="sxs-lookup"><span data-stu-id="b28f9-127">Open a native app seamlessly</span></span>

<span data-ttu-id="b28f9-128">Windows、iOS、および Android では、アプリ プロトコル アソシエーションに基づいてアプリをよりシームレスに開くことが可能になります。</span><span class="sxs-lookup"><span data-stu-id="b28f9-128">Windows, iOS, and Android also allow opening of apps more seamlessly, based on app protocol association.</span></span> <span data-ttu-id="b28f9-129">アプリがまだ Web ブラウザから開くことを処理するようにコンフィギュレーションされていない場合、これをコンフィギュレーションするには開発者が必要な場合があります。</span><span class="sxs-lookup"><span data-stu-id="b28f9-129">If your app is not already configured to handle opening from a web browser, you may need a developer to configure this.</span></span>

- <span data-ttu-id="b28f9-130">Windows の場合は、[アプリ URI ハンドラーを使用して Web サイトのアプリを有効にする](https://docs.microsoft.com/windows/uwp/launch-resume/web-to-app-linking) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="b28f9-130">For Windows, see [Enable apps for websites using app URI handlers](https://docs.microsoft.com/windows/uwp/launch-resume/web-to-app-linking).</span></span>
- <span data-ttu-id="b28f9-131">iOS の場合は、[開発者向けの汎用リンク](https://developer.apple.com/ios/universal-links/) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="b28f9-131">For iOS, see [Universal Links for Developers](https://developer.apple.com/ios/universal-links/).</span></span>
- <span data-ttu-id="b28f9-132">Android の場合は、[Android アプリの操作リンク](https://developer.android.com/training/app-links/)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="b28f9-132">For Android, see [Handling Android App Links](https://developer.android.com/training/app-links/).</span></span>

| <span data-ttu-id="b28f9-133">クライアント</span><span class="sxs-lookup"><span data-stu-id="b28f9-133">Client</span></span>                | <span data-ttu-id="b28f9-134">新しいウィンドウで開く</span><span class="sxs-lookup"><span data-stu-id="b28f9-134">Open in new window</span></span> | <span data-ttu-id="b28f9-135">ネイティブ アプリを開く</span><span class="sxs-lookup"><span data-stu-id="b28f9-135">Open native app</span></span> | <span data-ttu-id="b28f9-136">POS 内で開く</span><span class="sxs-lookup"><span data-stu-id="b28f9-136">Open within POS</span></span> | <span data-ttu-id="b28f9-137">詳細情報</span><span class="sxs-lookup"><span data-stu-id="b28f9-137">Details</span></span>                           |
|-----------------------|--------------------|-----------------|-----------------|-----------------------------------|
| <span data-ttu-id="b28f9-138">Windows 上の Modern POS</span><span class="sxs-lookup"><span data-stu-id="b28f9-138">Modern POS on Windows</span></span> | <span data-ttu-id="b28f9-139">✓\*</span><span class="sxs-lookup"><span data-stu-id="b28f9-139">✓\*</span></span>                | <span data-ttu-id="b28f9-140">✓</span><span class="sxs-lookup"><span data-stu-id="b28f9-140">✓</span></span>               | <span data-ttu-id="b28f9-141">✓</span><span class="sxs-lookup"><span data-stu-id="b28f9-141">✓</span></span>              | <span data-ttu-id="b28f9-142">\*新しい Modern POS ウィンドウで開く</span><span class="sxs-lookup"><span data-stu-id="b28f9-142">\* Opens in new Modern POS window</span></span> |
| <span data-ttu-id="b28f9-143">クラウド POS</span><span class="sxs-lookup"><span data-stu-id="b28f9-143">Cloud POS</span></span>             | <span data-ttu-id="b28f9-144">✓\*</span><span class="sxs-lookup"><span data-stu-id="b28f9-144">✓\*</span></span>                | <span data-ttu-id="b28f9-145">✓</span><span class="sxs-lookup"><span data-stu-id="b28f9-145">✓</span></span>               | <span data-ttu-id="b28f9-146">x</span><span class="sxs-lookup"><span data-stu-id="b28f9-146">X</span></span>              | <span data-ttu-id="b28f9-147">\*新しいブラウザー タブで開く</span><span class="sxs-lookup"><span data-stu-id="b28f9-147">\* Opens in new browser tab</span></span>        |
| <span data-ttu-id="b28f9-148">iOS 上の Modern POS</span><span class="sxs-lookup"><span data-stu-id="b28f9-148">Modern POS on iOS</span></span>     | <span data-ttu-id="b28f9-149">✓\*</span><span class="sxs-lookup"><span data-stu-id="b28f9-149">✓\*</span></span>                | <span data-ttu-id="b28f9-150">✓</span><span class="sxs-lookup"><span data-stu-id="b28f9-150">✓</span></span>               | <span data-ttu-id="b28f9-151">x</span><span class="sxs-lookup"><span data-stu-id="b28f9-151">X</span></span>              | <span data-ttu-id="b28f9-152">\*新しいブラウザー タブで開く</span><span class="sxs-lookup"><span data-stu-id="b28f9-152">\* Opens in new browser tab</span></span>        |
| <span data-ttu-id="b28f9-153">Android 上の Modern POS</span><span class="sxs-lookup"><span data-stu-id="b28f9-153">Modern POS on Android</span></span> | <span data-ttu-id="b28f9-154">✓\*</span><span class="sxs-lookup"><span data-stu-id="b28f9-154">✓\*</span></span>                | <span data-ttu-id="b28f9-155">✓</span><span class="sxs-lookup"><span data-stu-id="b28f9-155">✓</span></span>               | <span data-ttu-id="b28f9-156">x</span><span class="sxs-lookup"><span data-stu-id="b28f9-156">X</span></span>              | <span data-ttu-id="b28f9-157">\*新しいブラウザー タブで開く</span><span class="sxs-lookup"><span data-stu-id="b28f9-157">\* Opens in new browser tab</span></span>        |

## <a name="before-you-begin"></a><span data-ttu-id="b28f9-158">準備</span><span class="sxs-lookup"><span data-stu-id="b28f9-158">Before you begin</span></span>

<span data-ttu-id="b28f9-159">開始する前に、[販売時点管理 (POS) の画面レイアウト](pos-screen-layouts.md) をコンフィギュレーションする方法を確認します。</span><span class="sxs-lookup"><span data-stu-id="b28f9-159">Before you begin, review how to configure [Screen layouts for the point of sale (POS)](pos-screen-layouts.md).</span></span>

## <a name="open-url-in-pos"></a><span data-ttu-id="b28f9-160">POS で URL を開く</span><span class="sxs-lookup"><span data-stu-id="b28f9-160">Open URL in POS</span></span>

<span data-ttu-id="b28f9-161">POS で開くように URL をコンフィギュレーションするには、次の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="b28f9-161">To configure a URL to be opened in POS, perform the following steps.</span></span>

1. <span data-ttu-id="b28f9-162">本社で、**Retail および Commerce \>チャネル設定 \> POS 設定 \> POS \> 画面レイアウト** に移動します。</span><span class="sxs-lookup"><span data-stu-id="b28f9-162">In head office, go to **Retail and Commerce \> Channel Setup \> POS Setup \> POS \> Screen Layouts**.</span></span>
2. <span data-ttu-id="b28f9-163">**ボタン グリッド \> デザイナー** を選択します。</span><span class="sxs-lookup"><span data-stu-id="b28f9-163">Select **Button Grids \> Designer**.</span></span>
3. <span data-ttu-id="b28f9-164">新しいボタンを作成します。</span><span class="sxs-lookup"><span data-stu-id="b28f9-164">Create a new button.</span></span>
4. <span data-ttu-id="b28f9-165">**ボタン** プロパティを選択します。</span><span class="sxs-lookup"><span data-stu-id="b28f9-165">Select **Button** properties.</span></span>
5. <span data-ttu-id="b28f9-166">アクションとして **URL を開く** を選択します。</span><span class="sxs-lookup"><span data-stu-id="b28f9-166">Select **Open URL** as the action.</span></span>
6. <span data-ttu-id="b28f9-167">使用する URL を入力します。</span><span class="sxs-lookup"><span data-stu-id="b28f9-167">Enter the URL that you want to use.</span></span>
7. <span data-ttu-id="b28f9-168">新しいウィンドウで URL を開くかどうかをコンフィギュレーションします。</span><span class="sxs-lookup"><span data-stu-id="b28f9-168">Configure whether to open the URL in a new window.</span></span>
