---
title: "POS の画面レイアウトのコンフィギュレーション"
description: "このトピックでは、Microsoft Dynamics 365 の Retail POS (販売時点管理) の画面レイアウトに関する情報を提供します。"
author: jblucher
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
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
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: 9082c156fde52aa0c822f8e4753de816f8cc0558
ms.contentlocale: ja-jp
ms.lasthandoff: 05/08/2018

---

# <a name="configure-screen-layouts-for-pos"></a><span data-ttu-id="f7031-103">POS の画面レイアウトのコンフィギュレーション</span><span class="sxs-lookup"><span data-stu-id="f7031-103">Configure screen layouts for POS</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="f7031-104">このトピックでは、Microsoft Dynamics 365 の Retail POS (販売時点管理) の画面レイアウトに関する情報を提供します。</span><span class="sxs-lookup"><span data-stu-id="f7031-104">This topic provides information about screen layouts for the Microsoft Dynamics 365 for Retail point of sale (POS) experiences.</span></span>

<span data-ttu-id="f7031-105">Microsoft Dynamics 365 の Retail POS (販売時点管理) ユーザー インターフェイスは、店舗、レジスター、および / またはユーザーに割り当てられた視覚プロファイルと画面レイアウトの組み合わせを使用して構成できます。</span><span class="sxs-lookup"><span data-stu-id="f7031-105">The Microsoft Dynamics 365 for Retail point of sale (POS) user interface can be configured using a combination of visual profiles and screen layouts, assigned to stores, registers, and/or users.</span></span>

## <a name="visual-profile"></a><span data-ttu-id="f7031-106">ビジュアル プロファイル</span><span class="sxs-lookup"><span data-stu-id="f7031-106">Visual profile</span></span>
<span data-ttu-id="f7031-107">プロファイルはレジスターに割り当てられ、レジスター固有でユーザー間で共有される視覚要素を指定するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="f7031-107">Visual profiles are assigned to registers and are used to specify the visual elements that are register-specific and shared across users.</span></span> <span data-ttu-id="f7031-108">レジスターにログインするユーザーには、同じテーマ、色、および画像があります。</span><span class="sxs-lookup"><span data-stu-id="f7031-108">Any user who logs into the register will have the same theme, colors, and images.</span></span> 

<span data-ttu-id="f7031-109">**プロファイル番号** - プロファイル番号は、Visual プロファイルの一意の識別子です。</span><span class="sxs-lookup"><span data-stu-id="f7031-109">**Profile number** - The profile number is the unique identifier for the Visual profile.</span></span> 

<span data-ttu-id="f7031-110">**説明** - この説明では、状況に合った正しいプロファイルを特定するのに役立つ意味のある名前を指定できます。</span><span class="sxs-lookup"><span data-stu-id="f7031-110">**Description** - The description allows you to specify a meaningful name that will help to identify the correct profile for your situation.</span></span>

<span data-ttu-id="f7031-111">**テーマ** - ユーザーは、Light または Dark アプリケーション テーマを選択できます。</span><span class="sxs-lookup"><span data-stu-id="f7031-111">**Theme** - Users can choose between the Light or Dark application themes.</span></span> <span data-ttu-id="f7031-112">これらの設定は、アプリ全体のフォントと背景色に影響します。</span><span class="sxs-lookup"><span data-stu-id="f7031-112">These settings impact the font and background colors throughout the app.</span></span>

<span data-ttu-id="f7031-113">**アクセント色** - アクセントの色は、タイル、コマンド ボタン、またはハイパーリンクなどの特定の視覚要素を区別またはハイライト表示するために POS 全体で使用されます。</span><span class="sxs-lookup"><span data-stu-id="f7031-113">**Accent color** - The accent color is used throughout the POS to differentiate or highlight certain visual elements such as tiles, command buttons, or hyperlinks.</span></span> <span data-ttu-id="f7031-114">これらの要素は、通常実行可能です。</span><span class="sxs-lookup"><span data-stu-id="f7031-114">These elements are typically actionable.</span></span>

<span data-ttu-id="f7031-115">**ヘッダーの色** - ヘッダー カラーを使用すると、小売業者のブランド ニーズに合わせてページ ヘッダーの色を設定できます。</span><span class="sxs-lookup"><span data-stu-id="f7031-115">**Header color** - The header color allows the user to configure the color of the page header to meet the branding needs of the retailer.</span></span> <span data-ttu-id="f7031-116">この機能は、Dynamics 365 for Retail バージョン 1611 でのみ使用できます。</span><span class="sxs-lookup"><span data-stu-id="f7031-116">This feature is only available in Dynamics 365 for Retail version 1611.</span></span>

<span data-ttu-id="f7031-117">**ログイン バックグラウンド** - ユーザーは、ログイン画面の背景イメージを指定できます。</span><span class="sxs-lookup"><span data-stu-id="f7031-117">**Login backgrounds** - Users can specify a background image for the login screen.</span></span> <span data-ttu-id="f7031-118">大容量のファイルの保存と読み込みは、アプリケーションの動作やパフォーマンスに影響を与える可能性があるため、背景画像のファイル サイズはできるだけ小さくする必要があります。</span><span class="sxs-lookup"><span data-stu-id="f7031-118">The file size of background images should be kept as small as possible, as storing and loading large files can have an impact on the application behavior and performance.</span></span>

<span data-ttu-id="f7031-119">**アプリケーションの背景** - POS は、固体のテーマカラーの代わりに、アプリケーション全体の背景として画像を使用することもできます。</span><span class="sxs-lookup"><span data-stu-id="f7031-119">**Application background** - The POS can also use an image as a background throughout the application in place of the solid theme color.</span></span> <span data-ttu-id="f7031-120">ログイン バックグラウンドと同様に、ファイル サイズはできるだけ小さくすることをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="f7031-120">As with the login backgrounds, it is advised to keep the file size as minimal as possible.</span></span>

## <a name="screen-layouts"></a><span data-ttu-id="f7031-121">画面レイアウト</span><span class="sxs-lookup"><span data-stu-id="f7031-121">Screen layouts</span></span>
<span data-ttu-id="f7031-122">画面レイアウト構成によって、POS Welcome 画面および Transaction 画面で UI コントロールのアクション、コンテンツ、および配置が決定されます。</span><span class="sxs-lookup"><span data-stu-id="f7031-122">Screen layout configuration determines the actions, content, and placement of UI controls in the POS Welcome screen and Transaction screen.</span></span> 

<span data-ttu-id="f7031-123">**ようこそ画面**- ほとんどの場合、ようこそ画面は、ユーザーが初めて POS にログインするときに表示されるページです。</span><span class="sxs-lookup"><span data-stu-id="f7031-123">**Welcome screen**- In most cases, the Welcome screen is the page that users will see when they first log into POS.</span></span> <span data-ttu-id="f7031-124">[ようこそ画面] は、ブランド イメージと、POS 操作へのアクセスを提供するボタン グリッドで構成することができます。</span><span class="sxs-lookup"><span data-stu-id="f7031-124">The Welcome screen can consist of a branding image and button grids that provide access to POS operations.</span></span> <span data-ttu-id="f7031-125">通常、現在のトランザクションに固有でない操作はここに配置されます。</span><span class="sxs-lookup"><span data-stu-id="f7031-125">Typically, operations that are not specific to the current transaction are placed here.</span></span> 

<span data-ttu-id="f7031-126">**トランザクション画面** - トランザクション画面は、販売トランザクションおよび注文処理のための POS のメイン画面です。</span><span class="sxs-lookup"><span data-stu-id="f7031-126">**Transaction screen** - The Transaction screen is the main screen in POS for processing sales transactions and orders.</span></span> <span data-ttu-id="f7031-127">トランザクション画面は、画面レイアウト設計者を使用して設定することができます。</span><span class="sxs-lookup"><span data-stu-id="f7031-127">The Transaction screen can be configured using the Screen layout designer.</span></span> 

<span data-ttu-id="f7031-128">**既定のスタート画面** - 一部の小売業者は、ログイン後にレジ担当者がトランザクション画面に直接ナビゲートすることを好みます。</span><span class="sxs-lookup"><span data-stu-id="f7031-128">**Default start screen** - Some retailers prefer that the cashier navigate directly to the Transaction screen after logging in.</span></span> <span data-ttu-id="f7031-129">既定の開始画面設定では、各画面レイアウトに対してこれを設定できます。</span><span class="sxs-lookup"><span data-stu-id="f7031-129">The default start screen setting allows users to set this for each screen layout.</span></span>

### <a name="assignment"></a><span data-ttu-id="f7031-130">割り当て</span><span class="sxs-lookup"><span data-stu-id="f7031-130">Assignment</span></span>

<span data-ttu-id="f7031-131">画面レイアウトは、店舗、レジスター、またはユーザー レベルで割り当てることができます。</span><span class="sxs-lookup"><span data-stu-id="f7031-131">Screen layouts can be assigned at the store, register, or user level.</span></span> <span data-ttu-id="f7031-132">ユーザーの割り当てはレジスターと店舗の割り当てを上書きし、レジスターの割り当ては店舗の割り当てを上書きします。</span><span class="sxs-lookup"><span data-stu-id="f7031-132">The user assignment overrides the register and store assignment, and the register assignment overrides the store assignment.</span></span> <span data-ttu-id="f7031-133">すべてのユーザーがレジスターまたはロールに関係なく同じレイアウトを使用する単純なシナリオでは、画面レイアウトは店舗でのみ設定できます。</span><span class="sxs-lookup"><span data-stu-id="f7031-133">In a simple scenario where all users use the same layout regardless of register or role, the screen layout can be set only at the store.</span></span> <span data-ttu-id="f7031-134">特定のレジスターまたはユーザが特殊なレイアウトを必要とする場合は、それらを適切に割り当てることができます。</span><span class="sxs-lookup"><span data-stu-id="f7031-134">In cases where certain registers or users require specialized layouts, they can be assigned appropriately.</span></span>

### <a name="layout-sizes"></a><span data-ttu-id="f7031-135">レイアウト サイズ</span><span class="sxs-lookup"><span data-stu-id="f7031-135">Layout sizes</span></span>

<span data-ttu-id="f7031-136">この機能は、Dynamics 365 for Retail バージョン 1611 でのみ適用できます。</span><span class="sxs-lookup"><span data-stu-id="f7031-136">This feature only applies to Dynamics 365 for Retail version 1611.</span></span> <span data-ttu-id="f7031-137">多くの場合、画面レイアウトは複数の画面サイズと解像度で使用できるため、ユーザーはそれぞれのレイアウトとコンテンツを設定できます。</span><span class="sxs-lookup"><span data-stu-id="f7031-137">Because in many cases screen layouts can be used across multiple screen sizes and resolutions, users can configure their layout and content for each.</span></span> <span data-ttu-id="f7031-138">POS アプリケーションは、起動時にデバイスに最も近いレイアウト サイズを自動的に選択します。</span><span class="sxs-lookup"><span data-stu-id="f7031-138">The POS application will automatically choose the closest layout size for the device at the time of startup.</span></span> <span data-ttu-id="f7031-139">画面レイアウトには、フル デバイスとコンパクト デバイスの両方の設定を含めることもできます。</span><span class="sxs-lookup"><span data-stu-id="f7031-139">A screen layout can also contain configurations for both full and compact devices.</span></span> <span data-ttu-id="f7031-140">このコンフィギュレーションにより、ユーザーは、1 つの画面レイアウトに割り当てられ、さまざまなサイズとフォーム係数を店舗内で使用できます。</span><span class="sxs-lookup"><span data-stu-id="f7031-140">This configuration allows a user to be assigned to a single screen layout that will work across various sizes and form factors within the store.</span></span> 

<span data-ttu-id="f7031-141">**Modern POS - Full** - 通常、フル レイアウトは PC モニタまたはタブレットなどの大型ディスプレイに最適です。</span><span class="sxs-lookup"><span data-stu-id="f7031-141">**Modern POS - Full** - Full layouts are typically best used for larger displays such as PC monitors or tablets.</span></span> <span data-ttu-id="f7031-142">ユーザーは、含める UI 要素を選択し、そのサイズと配置を決定し、詳細なプロパティを構成することができます。</span><span class="sxs-lookup"><span data-stu-id="f7031-142">Users can choose which UI elements to include, determine their size and placement, and configure their detailed properties.</span></span> <span data-ttu-id="f7031-143">フル レイアウトは、縦向きおよび横向きの両方のコンフィギュレーションをサポートします。</span><span class="sxs-lookup"><span data-stu-id="f7031-143">Full layouts support both portrait and landscape configurations.</span></span> 

<span data-ttu-id="f7031-144">**Modern POS - Compact** - コンパクトなレイアウトは、通常、携帯電話や小型タブレットに最適です。</span><span class="sxs-lookup"><span data-stu-id="f7031-144">**Modern POS - Compact** - Compact layouts are typically best used for phones or small tablets.</span></span> <span data-ttu-id="f7031-145">コンパクト デバイスでは、設計の可能性が限られています。</span><span class="sxs-lookup"><span data-stu-id="f7031-145">Design possibilities are limited for compact devices.</span></span> <span data-ttu-id="f7031-146">ユーザーは、領収書および合計ペインの列とフィールドを構成できます。</span><span class="sxs-lookup"><span data-stu-id="f7031-146">Users can configure the columns and fields for the receipt and totals panes.</span></span>

### <a name="screen-layout-designer"></a><span data-ttu-id="f7031-147">画面レイアウト デザイナー</span><span class="sxs-lookup"><span data-stu-id="f7031-147">Screen layout designer</span></span>

<span data-ttu-id="f7031-148">画面レイアウト内の各レイアウト サイズは、画面レイアウト デザイナーを使用して設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="f7031-148">Each layout size within a screen layout must be configured using the Screen layout designer.</span></span> <span data-ttu-id="f7031-149">デザイナーは、ユーザーがトランザクション画面の UI 要素を指定および構成できるようにします。</span><span class="sxs-lookup"><span data-stu-id="f7031-149">The designer allows users to specify and configure the UI elements of the Transaction screen.</span></span> <span data-ttu-id="f7031-150">画面レイアウト デザイナーは、ユーザーがアクセスするたびに ClickOnce を使用してアプリケーションの最新バージョンをダウンロード、インストール、および起動します。</span><span class="sxs-lookup"><span data-stu-id="f7031-150">The Screen layout designer uses ClickOnce to download, install, and launch the latest version of the application each time the user accesses it.</span></span> <span data-ttu-id="f7031-151">ClickOnce を使用するためのブラウザ要件を確認してください—Chrome などの一部のブラウザでは、拡張機能が必要です。</span><span class="sxs-lookup"><span data-stu-id="f7031-151">Be sure to check browser requirements for using ClickOnce—some browsers, such as Chrome, require extensions.</span></span> 

<span data-ttu-id="f7031-152">**テンキー** - テンキーは、POS トランザクション画面の主なユーザ入力です。</span><span class="sxs-lookup"><span data-stu-id="f7031-152">**Number pad** - The number pad is the main user input in the POS Transaction screen.</span></span> <span data-ttu-id="f7031-153">タッチスクリーンには理想的なオンスクリーン パッド全体、または物理キーボードで使用できる入力フィールドのみを表示するように設定できます。</span><span class="sxs-lookup"><span data-stu-id="f7031-153">It can be configured to show the entire on-screen pad, which is ideal for touchscreens, or only the input field, which can be used with a physical keyboard.</span></span> <span data-ttu-id="f7031-154">テンキーの設定は、フル レイアウトでのみ使用できます。</span><span class="sxs-lookup"><span data-stu-id="f7031-154">The number pad settings are available in the full layout only.</span></span> <span data-ttu-id="f7031-155">Dynamics 365 for Retail バージョン 1611 では、コンパクト レイアウトには常に、トランザクション画面から利用できるフル テンキーがあります。</span><span class="sxs-lookup"><span data-stu-id="f7031-155">In Dynamics 365 for Retail version 1611, compact layouts always have the full number pad available from the Transaction screen.</span></span>

<span data-ttu-id="f7031-156">**合計パネル** - 合計パネルは、行数、割引額、料金、小計、および税金などのフィールドを表示するように、1 つまたは 2 つの列で構成できます。</span><span class="sxs-lookup"><span data-stu-id="f7031-156">**Totals panel** - The totals panel can be configured in either one or two columns to show fields such as line count, discount amount, charges, subtotal, and tax.</span></span> <span data-ttu-id="f7031-157">Dynamics 365 for Retail バージョン 1611 では、コンパクト レイアウトは単一の合計列のみをサポートします。</span><span class="sxs-lookup"><span data-stu-id="f7031-157">In Dynamics 365 for Retail version 1611, compact layouts only support a single totals column.</span></span> 

<span data-ttu-id="f7031-158">**入庫** - 入庫パネルには、POS で処理された製品およびサービスの販売明細行、支払明細行、および配送情報が含まれています。</span><span class="sxs-lookup"><span data-stu-id="f7031-158">**Receipt** - The receipt panel contains the sales lines, payment lines, and delivery information for the products and services processed in the POS.</span></span> <span data-ttu-id="f7031-159">ユーザーは、列、幅、および配置を指定できます。</span><span class="sxs-lookup"><span data-stu-id="f7031-159">Users can specify columns, widths, and placement.</span></span> <span data-ttu-id="f7031-160">Dynamics 365 for Retail バージョン 1611 のコンパクト レイアウトでは、メイン ラインの下の行に表示される追加情報を設定することもできます。</span><span class="sxs-lookup"><span data-stu-id="f7031-160">In compact layouts in Dynamics 365 for Retail version 1611, you can also configure additional information which will appear in the row under the main line.</span></span> 

<span data-ttu-id="f7031-161">**顧客カード** - 顧客カードには、トランザクションに現在関連付けられている顧客に関する情報が表示されます。</span><span class="sxs-lookup"><span data-stu-id="f7031-161">**Customer card** - The customer card shows information pertaining to the customer currently associated with the transaction.</span></span> <span data-ttu-id="f7031-162">顧客カードは、追加情報を隠すか表示するように設定することができます。</span><span class="sxs-lookup"><span data-stu-id="f7031-162">The customer card can be configured to hide or show additional information.</span></span> 

<span data-ttu-id="f7031-163">**タブ コントロール** - タブ コントロールは画面レイアウト上に置くことができ、テンキー、顧客カード、ボタン グリッドなどの他のコントロールをタブ内に配置することができます。タブ コントロールは、ユーザーが画面により多くのコンテンツを収めるのを助けるコンテナーです。</span><span class="sxs-lookup"><span data-stu-id="f7031-163">**Tab control** - The tab control can be placed onto the screen layout, and other controls such as the number pad, customer card, or button grids can be placed inside the tab. The tab control is a container that helps users fit more content in the screen.</span></span> <span data-ttu-id="f7031-164">タブ コントロールは、フル レイアウトでのみ使用できます。</span><span class="sxs-lookup"><span data-stu-id="f7031-164">The tab control is only available for full layouts.</span></span> 

<span data-ttu-id="f7031-165">**画像** - イメージ コントロールを使用すると、店舗のロゴやその他のブランド イメージをトランザクション画面に表示することができます。</span><span class="sxs-lookup"><span data-stu-id="f7031-165">**Image** - The image control can be used to show the store logo or other branding image on the transaction screen.</span></span> <span data-ttu-id="f7031-166">イメージ コントロールは、フル レイアウトでのみ使用できます。</span><span class="sxs-lookup"><span data-stu-id="f7031-166">The image control is only available for full layouts.</span></span> 

<span data-ttu-id="f7031-167">**お勧めの製品** - 環境用に構成されている場合、お勧めの製品コントロールは、機械学習に基づく製品候補を表示します。</span><span class="sxs-lookup"><span data-stu-id="f7031-167">**Recommended products** - If configured for the environment, the recommended products control will show product suggestions based on machine learning.</span></span> <span data-ttu-id="f7031-168">お勧めの製品コントロールは、Dynamics 365 for Retail バージョン 1611 のフル レイアウトでのみ使用できます。</span><span class="sxs-lookup"><span data-stu-id="f7031-168">The recommended products control is only available for full layouts in Dynamics 365 for Retail version 1611.</span></span> <span data-ttu-id="f7031-169">**カスタム管理**- カスタム管理は、画面レイアウト内のプレース ホルダーとして機能し、ユーザーがカスタム コンテンツ用のスペースを予約できるようにします。</span><span class="sxs-lookup"><span data-stu-id="f7031-169">**Custom control **- The custom control acts as a placeholder within the screen layout to allows users to reserve space for custom content.</span></span> <span data-ttu-id="f7031-170">カスタム コントロールは、フル レイアウトでのみ使用できます。</span><span class="sxs-lookup"><span data-stu-id="f7031-170">The custom control is only available for full layouts.</span></span>

<a name="additional-resources"></a><span data-ttu-id="f7031-171">その他のリソース</span><span class="sxs-lookup"><span data-stu-id="f7031-171">Additional resources</span></span>
--------

[<span data-ttu-id="f7031-172">Retail POS のレイアウト デザイナーのインストール</span><span class="sxs-lookup"><span data-stu-id="f7031-172">Install the Retail POS Layout designer</span></span>](install-pos-layout-designer.md)




