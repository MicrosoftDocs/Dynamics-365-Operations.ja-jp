---
title: Modern POS (MPOS) および Cloud POS のデモ データ画面レイアウト
description: このトピックでは、Dynamics 365 Commerce の販売時点管理 (POS) のデモ データ セットに含まれている画面レイアウトに関する情報を提供します。
author: josaw1
manager: AnnBe
ms.date: 10/05/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: RetailTillLayout
audience: Application user
ms.reviewer: josaw
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2017-10-05
ms.dyn365.ops.version: Retail April 2017 update
ms.openlocfilehash: 5e75210e77d1187f482d716f795ec0155553cb3f
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/15/2021
ms.locfileid: "5213629"
---
# <a name="demo-data-screen-layouts-in-modern-pos-mpos-and-cloud-pos"></a><span data-ttu-id="219ab-103">Modern POS (MPOS) および Cloud POS のデモ データ画面レイアウト</span><span class="sxs-lookup"><span data-stu-id="219ab-103">Demo data screen layouts in Modern POS (MPOS) and Cloud POS</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="219ab-104">このトピックでは、Dynamics 365 Commerce の販売時点管理 (POS) のデモ データ セットに含まれている画面レイアウトに関する情報を提供します。</span><span class="sxs-lookup"><span data-stu-id="219ab-104">This topic provides information about the screen layouts that are included with the demo data set for the point of sale (POS) experiences in Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="219ab-105">概要</span><span class="sxs-lookup"><span data-stu-id="219ab-105">Overview</span></span>

<span data-ttu-id="219ab-106">Commerce のデモ データに含まれているサンプル画面レイアウトは、さまざまな小売セグメント、店員の役割、およびデバイスに最適化されたコンテンツを提供します。</span><span class="sxs-lookup"><span data-stu-id="219ab-106">The sample screen layouts that are included with Commerce demo data provide content that is optimized for various retail segments, store worker roles, and devices.</span></span> <span data-ttu-id="219ab-107">1 つのレイアウトに複数のレイアウトサイズとボタングリッドの組み合わせを含めることで、店員によるデバイスとステーション間の移動を確実にカバーできます。</span><span class="sxs-lookup"><span data-stu-id="219ab-107">A single layout can contain several layout sizes and combinations of button grids, to help ensure coverage as store workers move between devices and stations.</span></span> <span data-ttu-id="219ab-108">このトピックでは、これらのレイアウトの違いや、レイアウトが提供する操作や全体的なエクスペリエンスについて説明します。</span><span class="sxs-lookup"><span data-stu-id="219ab-108">This topic highlights the differences between these layouts, the operations that they provide, and the overall experiences that they deliver.</span></span>

![クロス デバイス デモ データのレイアウト](../commerce/media/demo-screen-layouts-fig-1-1.png)

## <a name="anatomy-of-a-screen-layout-id"></a><span data-ttu-id="219ab-110">画面レイアウト ID の構造</span><span class="sxs-lookup"><span data-stu-id="219ab-110">Anatomy of a screen layout ID</span></span>

<span data-ttu-id="219ab-111">画面レイアウトを検索するには、**Retail と Commerce** \> **チャネル設定** \> **POS 設定** \> **POS** \> **画面レイアウト** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="219ab-111">To find screen layouts, go to **Retail and Commerce** \> **Channel setup** \> **POS setup** \> **POS** \> **Screen layouts**.</span></span>

![画面レイアウトのページ](../commerce/media/demo-screen-layouts-fig-2-1.png)

<span data-ttu-id="219ab-113">画面レイアウト ID は、最大 10 文字です。</span><span class="sxs-lookup"><span data-stu-id="219ab-113">Screen layout IDs can have a maximum of 10 characters.</span></span> <span data-ttu-id="219ab-114">ID は、次の 3 つの情報と順序で構成された文字列です。</span><span class="sxs-lookup"><span data-stu-id="219ab-114">The ID is a string that consists of three pieces of information, in this order:</span></span>

1. <span data-ttu-id="219ab-115">法人</span><span class="sxs-lookup"><span data-stu-id="219ab-115">Company</span></span>
2. <span data-ttu-id="219ab-116">レイアウトバージョン</span><span class="sxs-lookup"><span data-stu-id="219ab-116">Layout version</span></span>
3. <span data-ttu-id="219ab-117">個人</span><span class="sxs-lookup"><span data-stu-id="219ab-117">Persona</span></span>

### <a name="company"></a><span data-ttu-id="219ab-118">法人</span><span class="sxs-lookup"><span data-stu-id="219ab-118">Company</span></span>

| <span data-ttu-id="219ab-119">文字</span><span class="sxs-lookup"><span data-stu-id="219ab-119">Letter</span></span> | <span data-ttu-id="219ab-120">法人</span><span class="sxs-lookup"><span data-stu-id="219ab-120">Company</span></span>         |
|--------|-----------------|
| <span data-ttu-id="219ab-121">A</span><span class="sxs-lookup"><span data-stu-id="219ab-121">A</span></span>      | <span data-ttu-id="219ab-122">Adventure Works</span><span class="sxs-lookup"><span data-stu-id="219ab-122">Adventure Works</span></span> |
| <span data-ttu-id="219ab-123">F</span><span class="sxs-lookup"><span data-stu-id="219ab-123">F</span></span>      | <span data-ttu-id="219ab-124">Fabrikam</span><span class="sxs-lookup"><span data-stu-id="219ab-124">Fabrikam</span></span>        |
| <span data-ttu-id="219ab-125">C</span><span class="sxs-lookup"><span data-stu-id="219ab-125">C</span></span>      | <span data-ttu-id="219ab-126">Contoso</span><span class="sxs-lookup"><span data-stu-id="219ab-126">Contoso</span></span>         |

### <a name="layout-version"></a><span data-ttu-id="219ab-127">レイアウトバージョン</span><span class="sxs-lookup"><span data-stu-id="219ab-127">Layout version</span></span>

| <span data-ttu-id="219ab-128">バージョン番号</span><span class="sxs-lookup"><span data-stu-id="219ab-128">Version number</span></span> | <span data-ttu-id="219ab-129">説明</span><span class="sxs-lookup"><span data-stu-id="219ab-129">Description</span></span>                                                                                |
|----------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="219ab-130">3</span><span class="sxs-lookup"><span data-stu-id="219ab-130">3</span></span>              | <span data-ttu-id="219ab-131">さまざまなデバイスや縦横比の複数の画面のサイズをサポートする基本バージョン</span><span class="sxs-lookup"><span data-stu-id="219ab-131">The base version that supports multiple screen sizes for various devices and aspect ratios</span></span> |
| <span data-ttu-id="219ab-132">3.1</span><span class="sxs-lookup"><span data-stu-id="219ab-132">3.1</span></span>            | <span data-ttu-id="219ab-133">**お勧めの製品** パネル用の追加サポートのある基本バージョン</span><span class="sxs-lookup"><span data-stu-id="219ab-133">The base version that has additional support for the **Recommended products** panel</span></span>        |
| <span data-ttu-id="219ab-134">4</span><span class="sxs-lookup"><span data-stu-id="219ab-134">4</span></span>              | <span data-ttu-id="219ab-135">拡張された Fabrikam 更新版レイアウトの拡張バージョン</span><span class="sxs-lookup"><span data-stu-id="219ab-135">The extended version for extended Fabrikam updated layout</span></span>                                  |

### <a name="persona"></a><span data-ttu-id="219ab-136">個人</span><span class="sxs-lookup"><span data-stu-id="219ab-136">Persona</span></span>

| <span data-ttu-id="219ab-137">省略形</span><span class="sxs-lookup"><span data-stu-id="219ab-137">Abbreviation</span></span> | <span data-ttu-id="219ab-138">個人</span><span class="sxs-lookup"><span data-stu-id="219ab-138">Persona</span></span>       | <span data-ttu-id="219ab-139">コンテンツ</span><span class="sxs-lookup"><span data-stu-id="219ab-139">Contents</span></span> |
|--------------|---------------|----------|
| <span data-ttu-id="219ab-140">CSH</span><span class="sxs-lookup"><span data-stu-id="219ab-140">CSH</span></span>          | <span data-ttu-id="219ab-141">出納係</span><span class="sxs-lookup"><span data-stu-id="219ab-141">Cashier</span></span>       | <span data-ttu-id="219ab-142">レジ担当者のレイアウトには、顧客の注文、返品、割引、無効化、およびギフト カードなど、すべてのトランザクションに関連する工程が含まれます。</span><span class="sxs-lookup"><span data-stu-id="219ab-142">Cashier layouts include all transaction-related operations, such as customer orders, returns, discounts, voids, and gift cards.</span></span> <span data-ttu-id="219ab-143">これらのレイアウトには、価格チェック、在庫検索、在庫数などの在庫管理の毎日のタスクも含まれます。</span><span class="sxs-lookup"><span data-stu-id="219ab-143">These layouts also include daily tasks for inventory management, such price checks, inventory lookups, and stock counts.</span></span> <span data-ttu-id="219ab-144">開始時金額、シフトの停止、タイム レコーダーなど基本的なシフト管理も提供されます。</span><span class="sxs-lookup"><span data-stu-id="219ab-144">Basic shift management is also provided for start amounts, suspending shifts, and time clock.</span></span> |
| <span data-ttu-id="219ab-145">マネージャー</span><span class="sxs-lookup"><span data-stu-id="219ab-145">MGR</span></span>          | <span data-ttu-id="219ab-146">店長</span><span class="sxs-lookup"><span data-stu-id="219ab-146">Store Manager</span></span> | <span data-ttu-id="219ab-147">店舗マネージャー レイアウトには、キャッシュレイアウトにあるすべてのトランザクションに関連する操作の他、税の上書きも含まれます。</span><span class="sxs-lookup"><span data-stu-id="219ab-147">Store Manager layouts include all transaction-related operations that are found in the Cashier layouts but also include tax overrides.</span></span> <span data-ttu-id="219ab-148">また、これらのレイアウトには、価格チェック、在庫検索、在庫数などの在庫管理の毎日のタスクも含まれます。</span><span class="sxs-lookup"><span data-stu-id="219ab-148">These layouts also include daily tasks for inventory management, such as price checks, inventory lookups, and stock counts.</span></span> <span data-ttu-id="219ab-149">シフトの開始、停止、終了のためのシフト管理が提供されます。</span><span class="sxs-lookup"><span data-stu-id="219ab-149">Shift management is provided for starting, suspending, and closing shifts.</span></span> <span data-ttu-id="219ab-150">さらに、レイアウトには、入力、削除、支払/入金申告、金庫や銀行預金の引き出し操作が含まれます。</span><span class="sxs-lookup"><span data-stu-id="219ab-150">Additionally, the layouts include drawer operations for entries, removals, tender declarations, and safe and bank drops.</span></span> <span data-ttu-id="219ab-151">最後に、これらのレイアウトにはパフォーマンスレポートへのアクセスが含まれ、XおよびZレポートを印刷できます。</span><span class="sxs-lookup"><span data-stu-id="219ab-151">Finally, these layouts include access to performance reports, and enable X and Z reports to be printed.</span></span> |
| <span data-ttu-id="219ab-152">STK</span><span class="sxs-lookup"><span data-stu-id="219ab-152">STK</span></span>          | <span data-ttu-id="219ab-153">在庫係</span><span class="sxs-lookup"><span data-stu-id="219ab-153">Stock Clerk</span></span>   | <span data-ttu-id="219ab-154">在庫係レイアウトは、在庫管理のために最適化されています。</span><span class="sxs-lookup"><span data-stu-id="219ab-154">Stock Clerk layouts are optimized for inventory management.</span></span> <span data-ttu-id="219ab-155">価格チェック、在庫検索、ピッキングと入荷、在庫数確認、キット分解などの日常業務へのアクセスが含まれています。</span><span class="sxs-lookup"><span data-stu-id="219ab-155">They include access to daily tasks for price checks, inventory lookups, picking and receiving, stock counts, and kit disassembly.</span></span> <span data-ttu-id="219ab-156">これらのレイアウトは、タイム レコーダー、シフトの停止などの基本的なシフト操作も提供します。</span><span class="sxs-lookup"><span data-stu-id="219ab-156">These layouts also provide basic shift operations for time clock and suspending shifts.</span></span> <span data-ttu-id="219ab-157">これらのレイアウトは、主にバックオフィスタスクを対象としていますが、在庫担当者はトランザクションの画面のレジ担当者と同じ操作をしています。</span><span class="sxs-lookup"><span data-stu-id="219ab-157">Although these layouts are intended mainly for back-office tasks, stock clerks have the same operations as cashiers for transaction screens.</span></span> |

### <a name="example-layout"></a><span data-ttu-id="219ab-158">レイアウトの例</span><span class="sxs-lookup"><span data-stu-id="219ab-158">Example layout</span></span>

<span data-ttu-id="219ab-159">これは、Fabrikam 社の、レイアウトバージョン 4、店長個人の画面レイアウト ID の例です。</span><span class="sxs-lookup"><span data-stu-id="219ab-159">Here is an example of a screen layout ID for the Fabrikam company, layout version 4, and the Store Manager persona:</span></span>

<span data-ttu-id="219ab-160">F4MGR</span><span class="sxs-lookup"><span data-stu-id="219ab-160">F4MGR</span></span>

<span data-ttu-id="219ab-161">次の図は、Fabrikam 店長のようこそ画面の例を示しています。</span><span class="sxs-lookup"><span data-stu-id="219ab-161">The following illustration shows an example of the Welcome screen for a Fabrikam store manager.</span></span>

![Fabrikam 店長のようこそ画面](../commerce/media/demo-screen-layouts-fig-2-2.png)

## <a name="layout-sizes"></a><span data-ttu-id="219ab-163">レイアウト サイズ</span><span class="sxs-lookup"><span data-stu-id="219ab-163">Layout sizes</span></span>

### <a name="full-vs-compact-layouts"></a><span data-ttu-id="219ab-164">圧縮レイアウト対完全</span><span class="sxs-lookup"><span data-stu-id="219ab-164">Full vs. compact layouts</span></span>

<span data-ttu-id="219ab-165">画面レイアウトには、フルデバイスとコンパクトデバイスの両方のコンフィギュレーションを持つことができます。</span><span class="sxs-lookup"><span data-stu-id="219ab-165">A screen layout can have configurations for both full devices and compact devices.</span></span> <span data-ttu-id="219ab-166">したがって、ユーザーは、1 つの画面レイアウトに割り当てられ、さまざまなサイズとフォーム係数を店舗内で使用できます。</span><span class="sxs-lookup"><span data-stu-id="219ab-166">Therefore, a user can be assigned to a single screen layout that will work across various sizes and form factors in the store.</span></span>

- <span data-ttu-id="219ab-167">**Modern POS - Full** - 通常、フル レイアウトは PC モニタまたはタブレットなどの大型ディスプレイに最適です。</span><span class="sxs-lookup"><span data-stu-id="219ab-167">**Modern POS - Full** – Typically, full layouts are best used for larger displays, such as desktop computer monitors or tablets.</span></span> <span data-ttu-id="219ab-168">ユーザーは、レイアウトに含まれる UI 要素を選択し、要素のサイズと配置を指定し、詳細なプロパティを設定できます。</span><span class="sxs-lookup"><span data-stu-id="219ab-168">Users can select the UI elements that the layout includes, specify the size and placement of those elements, and configure their detailed properties.</span></span> <span data-ttu-id="219ab-169">フル レイアウトは、縦向きおよび横向きの両方のコンフィギュレーションをサポートします。</span><span class="sxs-lookup"><span data-stu-id="219ab-169">Full layouts support both portrait and landscape configurations.</span></span>
- <span data-ttu-id="219ab-170">**Modern POS - Compact** - コンパクトなレイアウトは、通常、携帯電話や小型タブレットに最適です。</span><span class="sxs-lookup"><span data-stu-id="219ab-170">**Modern POS - Compact** – Typically, compact layouts are best used for phones or small tablets.</span></span> <span data-ttu-id="219ab-171">コンパクト デバイスでは、設計の可能性が限られています。</span><span class="sxs-lookup"><span data-stu-id="219ab-171">Design possibilities are limited for compact devices.</span></span> <span data-ttu-id="219ab-172">ユーザーは、領収書ウインドウおよび合計ウインドウの列とフィールドをコンフィギュレーションできます。</span><span class="sxs-lookup"><span data-stu-id="219ab-172">Users can configure the columns and fields for the receipt pane and the totals pane.</span></span>

### <a name="screen-resolutions-that-are-provided"></a><span data-ttu-id="219ab-173">提供される画面解像度</span><span class="sxs-lookup"><span data-stu-id="219ab-173">Screen resolutions that are provided</span></span>

<span data-ttu-id="219ab-174">次の表は、標準的な画面解像度で提供されているレイアウト サイズを示しています。</span><span class="sxs-lookup"><span data-stu-id="219ab-174">The following table shows the layout sizes that are provided for typical screen resolutions.</span></span>

| <span data-ttu-id="219ab-175">レイアウト タイプ</span><span class="sxs-lookup"><span data-stu-id="219ab-175">Layout type</span></span> | <span data-ttu-id="219ab-176">解像度</span><span class="sxs-lookup"><span data-stu-id="219ab-176">Resolution</span></span> | <span data-ttu-id="219ab-177">縦横比</span><span class="sxs-lookup"><span data-stu-id="219ab-177">Aspect ratio</span></span> | <span data-ttu-id="219ab-178">ターゲット表示</span><span class="sxs-lookup"><span data-stu-id="219ab-178">Target display</span></span>          |
|-------------|------------|--------------|-------------------------|
| <span data-ttu-id="219ab-179">最適化\*</span><span class="sxs-lookup"><span data-stu-id="219ab-179">Compact\*</span></span>   | <span data-ttu-id="219ab-180">480 × 853</span><span class="sxs-lookup"><span data-stu-id="219ab-180">480 × 853</span></span>  | <span data-ttu-id="219ab-181">16:9</span><span class="sxs-lookup"><span data-stu-id="219ab-181">16:9</span></span>         | <span data-ttu-id="219ab-182">電話</span><span class="sxs-lookup"><span data-stu-id="219ab-182">Phones</span></span>                  |
| <span data-ttu-id="219ab-183">完全</span><span class="sxs-lookup"><span data-stu-id="219ab-183">Full</span></span>        | <span data-ttu-id="219ab-184">1024 × 768</span><span class="sxs-lookup"><span data-stu-id="219ab-184">1024 × 768</span></span> | <span data-ttu-id="219ab-185">4:3</span><span class="sxs-lookup"><span data-stu-id="219ab-185">4:3</span></span>          | <span data-ttu-id="219ab-186">タブレット</span><span class="sxs-lookup"><span data-stu-id="219ab-186">Tablets</span></span>                 |
| <span data-ttu-id="219ab-187">完全\*</span><span class="sxs-lookup"><span data-stu-id="219ab-187">Full\*</span></span>      | <span data-ttu-id="219ab-188">1280 × 720</span><span class="sxs-lookup"><span data-stu-id="219ab-188">1280 × 720</span></span> | <span data-ttu-id="219ab-189">16:9</span><span class="sxs-lookup"><span data-stu-id="219ab-189">16:9</span></span>         | <span data-ttu-id="219ab-190">タブレット</span><span class="sxs-lookup"><span data-stu-id="219ab-190">Tablets</span></span>                 |
| <span data-ttu-id="219ab-191">完全</span><span class="sxs-lookup"><span data-stu-id="219ab-191">Full</span></span>        | <span data-ttu-id="219ab-192">1366 × 768</span><span class="sxs-lookup"><span data-stu-id="219ab-192">1366 × 768</span></span> | <span data-ttu-id="219ab-193">16:9</span><span class="sxs-lookup"><span data-stu-id="219ab-193">16:9</span></span>         | <span data-ttu-id="219ab-194">タブレット、大きい画面</span><span class="sxs-lookup"><span data-stu-id="219ab-194">Tablets, larger screens</span></span> |
| <span data-ttu-id="219ab-195">完全</span><span class="sxs-lookup"><span data-stu-id="219ab-195">Full</span></span>        | <span data-ttu-id="219ab-196">1440 × 960</span><span class="sxs-lookup"><span data-stu-id="219ab-196">1440 × 960</span></span> | <span data-ttu-id="219ab-197">3:2</span><span class="sxs-lookup"><span data-stu-id="219ab-197">3:2</span></span>          | <span data-ttu-id="219ab-198">タブレット、大きい画面</span><span class="sxs-lookup"><span data-stu-id="219ab-198">Tablets, larger screens</span></span> |
| <span data-ttu-id="219ab-199">完全\*</span><span class="sxs-lookup"><span data-stu-id="219ab-199">Full\*</span></span>      | <span data-ttu-id="219ab-200">1536 × 864</span><span class="sxs-lookup"><span data-stu-id="219ab-200">1536 × 864</span></span> | <span data-ttu-id="219ab-201">16:9</span><span class="sxs-lookup"><span data-stu-id="219ab-201">16:9</span></span>         | <span data-ttu-id="219ab-202">タブレット、大きい画面</span><span class="sxs-lookup"><span data-stu-id="219ab-202">Tablets, larger screens</span></span> |

<span data-ttu-id="219ab-203">\*これらの追加レイアウト サイズは、Adventure WorksとFabrikamレイアウトでのみ使用できます。</span><span class="sxs-lookup"><span data-stu-id="219ab-203">\* These additional layout sizes are available only in Adventure Works and Fabrikam layouts.</span></span>

> [!TIP]
> <span data-ttu-id="219ab-204">POSでは、現在のアプリケーション ウィンドウの画面解像度に使用される最も近いサイズに基づいて、レイアウトのサイズが自動的に選択されます。</span><span class="sxs-lookup"><span data-stu-id="219ab-204">POS automatically selects layout sizes, based on the closest size that is available for the screen resolution of the current app window.</span></span> <span data-ttu-id="219ab-205">Modern POS (MPOS) または Retail Cloud POS (CPOS) で、現在使用されている画面レイアウト ID とレイアウトの解像度を知るには、**設定** ページを開き、**セッション情報** セクションを見ます。</span><span class="sxs-lookup"><span data-stu-id="219ab-205">To find the screen layout ID and layout resolution that are currently used, in Modern POS (MPOS) or Retail Cloud POS (CPOS), open the **Settings** page, and look in the **Session information** section.</span></span> <span data-ttu-id="219ab-206">現在のアプリケーションまたはブラウザーのフレームの実際のウィンドウの解像度を表示することもできます。</span><span class="sxs-lookup"><span data-stu-id="219ab-206">You can also see the actual window resolution for your current application or browser frame.</span></span> <span data-ttu-id="219ab-207">この情報を得た後に、**チャネル設定** \> **POS 設定** \> **POS** \> **画面レイアウト** で、レイアウト コンテンツのソースを検索することができます。</span><span class="sxs-lookup"><span data-stu-id="219ab-207">After you have this information, you can find the source of the layout content by going to **Channel setup** \> **POS setup** \> **POS** \> **Screen layouts**.</span></span>

![Commerce と POS での画面レイアウトとレイアウトの解像度/サイズ](../commerce/media/demo-screen-layouts-fig-3-1.png)

## <a name="companies-and-brands"></a><span data-ttu-id="219ab-209">会社およびブランド</span><span class="sxs-lookup"><span data-stu-id="219ab-209">Companies and brands</span></span>

<span data-ttu-id="219ab-210">各架空の会社では、さまざまな小売セグメントを対象としており、会社の市場用に調整された製品カタログが含まれています。</span><span class="sxs-lookup"><span data-stu-id="219ab-210">Each fictitious company is targeted to a different retail segment and includes product catalogs that are tuned for the company's market.</span></span> <span data-ttu-id="219ab-211">各企業は、その製品に付属する独自のビジュアルブランドを持っています。</span><span class="sxs-lookup"><span data-stu-id="219ab-211">Each company has a unique visual brand that accompanies its products.</span></span> <span data-ttu-id="219ab-212">ブランド要素には、アクセントの色、濃いまたは薄いテーマ、およびエクスペリエンスを提供する付属の写真が含まれます。</span><span class="sxs-lookup"><span data-stu-id="219ab-212">Branding elements include the accent color, dark or light theme, and accompanying photographs that provide realistic experiences.</span></span>

### <a name="company-segment-and-visual-characteristics"></a><span data-ttu-id="219ab-213">会社のセグメントと視覚的な特性</span><span class="sxs-lookup"><span data-stu-id="219ab-213">Company segment and visual characteristics</span></span>

| <span data-ttu-id="219ab-214">法人</span><span class="sxs-lookup"><span data-stu-id="219ab-214">Company</span></span>         | <span data-ttu-id="219ab-215">保管場所</span><span class="sxs-lookup"><span data-stu-id="219ab-215">Location</span></span> | <span data-ttu-id="219ab-216">区分</span><span class="sxs-lookup"><span data-stu-id="219ab-216">Segment</span></span>        | <span data-ttu-id="219ab-217">アクセント</span><span class="sxs-lookup"><span data-stu-id="219ab-217">Accent</span></span> | <span data-ttu-id="219ab-218">テーマ</span><span class="sxs-lookup"><span data-stu-id="219ab-218">Theme</span></span> |
|-----------------|----------|----------------|--------|-------|
| <span data-ttu-id="219ab-219">Adventure Works</span><span class="sxs-lookup"><span data-stu-id="219ab-219">Adventure Works</span></span> | <span data-ttu-id="219ab-220">シアトル</span><span class="sxs-lookup"><span data-stu-id="219ab-220">Seattle</span></span>  | <span data-ttu-id="219ab-221">スポーツ用品</span><span class="sxs-lookup"><span data-stu-id="219ab-221">Sporting Goods</span></span> | <span data-ttu-id="219ab-222">青</span><span class="sxs-lookup"><span data-stu-id="219ab-222">Blue</span></span>   | <span data-ttu-id="219ab-223">濃い色</span><span class="sxs-lookup"><span data-stu-id="219ab-223">Dark</span></span>  |
| <span data-ttu-id="219ab-224">Fabrikam</span><span class="sxs-lookup"><span data-stu-id="219ab-224">Fabrikam</span></span>        | <span data-ttu-id="219ab-225">サンフランシスコ</span><span class="sxs-lookup"><span data-stu-id="219ab-225">San Francisco</span></span>  | <span data-ttu-id="219ab-226">ファッション</span><span class="sxs-lookup"><span data-stu-id="219ab-226">Fashion</span></span>        | <span data-ttu-id="219ab-227">緑</span><span class="sxs-lookup"><span data-stu-id="219ab-227">Green</span></span>  | <span data-ttu-id="219ab-228">薄い色</span><span class="sxs-lookup"><span data-stu-id="219ab-228">Light</span></span> |
| <span data-ttu-id="219ab-229">Contoso</span><span class="sxs-lookup"><span data-stu-id="219ab-229">Contoso</span></span>         | <span data-ttu-id="219ab-230">ボストン</span><span class="sxs-lookup"><span data-stu-id="219ab-230">Boston</span></span>   | <span data-ttu-id="219ab-231">電子</span><span class="sxs-lookup"><span data-stu-id="219ab-231">Electronics</span></span>    | <span data-ttu-id="219ab-232">赤</span><span class="sxs-lookup"><span data-stu-id="219ab-232">Red</span></span>    | <span data-ttu-id="219ab-233">濃い色</span><span class="sxs-lookup"><span data-stu-id="219ab-233">Dark</span></span>  |

> [!NOTE]
> <span data-ttu-id="219ab-234">Adventure WorksとFabrikamは、2つの主要ブランドです。</span><span class="sxs-lookup"><span data-stu-id="219ab-234">Adventure Works and Fabrikam are the two flagship brands.</span></span> <span data-ttu-id="219ab-235">Contoso は使用可能ですが、すべてのレイアウトが提供されているわけではありません。</span><span class="sxs-lookup"><span data-stu-id="219ab-235">Contoso is available, but not all layouts have been provided.</span></span>

<span data-ttu-id="219ab-236">次の図は、3つの架空企業のようこそページとトランザクション ページの例を示しています。</span><span class="sxs-lookup"><span data-stu-id="219ab-236">The following illustrations show examples of the welcome page and transaction page for the three fictitious companies.</span></span>

### <a name="adventure-works"></a><span data-ttu-id="219ab-237">Adventure Works</span><span class="sxs-lookup"><span data-stu-id="219ab-237">Adventure Works</span></span>

![Adventure Works のデモ データ ウェルカムページ](../commerce/media/demo-screen-layouts-fig-4-1a.png)

![Adventure Works のデモ データ トランザクションページ](../commerce/media/demo-screen-layouts-fig-4-1b.png)

### <a name="fabrikam"></a><span data-ttu-id="219ab-240">Fabrikam</span><span class="sxs-lookup"><span data-stu-id="219ab-240">Fabrikam</span></span>

![Fabrikam のデモ データ ウェルカムページ](../commerce/media/demo-screen-layouts-fig-4-2a.png)

![Fabrikam のデモ データ トランザクション](../commerce/media/demo-screen-layouts-fig-4-2b.png)

### <a name="contoso"></a><span data-ttu-id="219ab-243">Contoso</span><span class="sxs-lookup"><span data-stu-id="219ab-243">Contoso</span></span>

![Contosoのデモ データのレイアウト](../commerce/media/demo-screen-layouts-fig-4-3.png)

## <a name="user-sign-in-matrix"></a><span data-ttu-id="219ab-245">ユーザー ログ イン マトリックス</span><span class="sxs-lookup"><span data-stu-id="219ab-245">User sign in matrix</span></span>

<span data-ttu-id="219ab-246">ユーザーには、さまざまな画面レイアウトが提供されています。</span><span class="sxs-lookup"><span data-stu-id="219ab-246">Users have been provided for the various screen layouts.</span></span> <span data-ttu-id="219ab-247">次の表を使用すると、どの画面にもアクセスできます。</span><span class="sxs-lookup"><span data-stu-id="219ab-247">By using the following table, you should be able to access any of the screens.</span></span> <span data-ttu-id="219ab-248">適切な演算子 ID を使用してログインします。</span><span class="sxs-lookup"><span data-stu-id="219ab-248">Just sign in by using an appropriate operator ID.</span></span>

| <span data-ttu-id="219ab-249">法人</span><span class="sxs-lookup"><span data-stu-id="219ab-249">Company</span></span>         | <span data-ttu-id="219ab-250">画面レイアウト ID</span><span class="sxs-lookup"><span data-stu-id="219ab-250">Screen layout ID</span></span> | <span data-ttu-id="219ab-251">個人</span><span class="sxs-lookup"><span data-stu-id="219ab-251">Persona</span></span>       | <span data-ttu-id="219ab-252">オペレーター ID</span><span class="sxs-lookup"><span data-stu-id="219ab-252">Operator IDs</span></span>           |
|-----------------|------------------|---------------|------------------------|
| <span data-ttu-id="219ab-253">Adventure Works</span><span class="sxs-lookup"><span data-stu-id="219ab-253">Adventure Works</span></span> | <span data-ttu-id="219ab-254">A3MGR</span><span class="sxs-lookup"><span data-stu-id="219ab-254">A3MGR</span></span>            | <span data-ttu-id="219ab-255">店長</span><span class="sxs-lookup"><span data-stu-id="219ab-255">Store Manager</span></span> | <span data-ttu-id="219ab-256">000154, 000137, 000073</span><span class="sxs-lookup"><span data-stu-id="219ab-256">000154, 000137, 000073</span></span> |
| <span data-ttu-id="219ab-257">Adventure Works</span><span class="sxs-lookup"><span data-stu-id="219ab-257">Adventure Works</span></span> | <span data-ttu-id="219ab-258">A3CSH</span><span class="sxs-lookup"><span data-stu-id="219ab-258">A3CSH</span></span>            | <span data-ttu-id="219ab-259">出納係</span><span class="sxs-lookup"><span data-stu-id="219ab-259">Cashier</span></span>       | <span data-ttu-id="219ab-260">000150, 000175, 000165</span><span class="sxs-lookup"><span data-stu-id="219ab-260">000150, 000175, 000165</span></span> |
| <span data-ttu-id="219ab-261">Adventure Works</span><span class="sxs-lookup"><span data-stu-id="219ab-261">Adventure Works</span></span> | <span data-ttu-id="219ab-262">A3STK</span><span class="sxs-lookup"><span data-stu-id="219ab-262">A3STK</span></span>            | <span data-ttu-id="219ab-263">在庫係</span><span class="sxs-lookup"><span data-stu-id="219ab-263">Stock Clerk</span></span>   | <span data-ttu-id="219ab-264">000155, 000181, 000152</span><span class="sxs-lookup"><span data-stu-id="219ab-264">000155, 000181, 000152</span></span> |
| <span data-ttu-id="219ab-265">Fabrikam</span><span class="sxs-lookup"><span data-stu-id="219ab-265">Fabrikam</span></span>        | <span data-ttu-id="219ab-266">F4MGR</span><span class="sxs-lookup"><span data-stu-id="219ab-266">F4MGR</span></span>            | <span data-ttu-id="219ab-267">店長</span><span class="sxs-lookup"><span data-stu-id="219ab-267">Store Manager</span></span> | <span data-ttu-id="219ab-268">000160、000713</span><span class="sxs-lookup"><span data-stu-id="219ab-268">000160, 000713</span></span>         |
| <span data-ttu-id="219ab-269">Fabrikam</span><span class="sxs-lookup"><span data-stu-id="219ab-269">Fabrikam</span></span>        | <span data-ttu-id="219ab-270">F3CSH</span><span class="sxs-lookup"><span data-stu-id="219ab-270">F3CSH</span></span>            | <span data-ttu-id="219ab-271">出納係</span><span class="sxs-lookup"><span data-stu-id="219ab-271">Cashier</span></span>       | <span data-ttu-id="219ab-272">000161, 000113, 000114</span><span class="sxs-lookup"><span data-stu-id="219ab-272">000161, 000113, 000114</span></span> |
| <span data-ttu-id="219ab-273">Fabrikam</span><span class="sxs-lookup"><span data-stu-id="219ab-273">Fabrikam</span></span>        | <span data-ttu-id="219ab-274">F3STK</span><span class="sxs-lookup"><span data-stu-id="219ab-274">F3STK</span></span>            | <span data-ttu-id="219ab-275">在庫係</span><span class="sxs-lookup"><span data-stu-id="219ab-275">Stock Clerk</span></span>   | <span data-ttu-id="219ab-276">000164, 000112, 000123</span><span class="sxs-lookup"><span data-stu-id="219ab-276">000164, 000112, 000123</span></span> |
| <span data-ttu-id="219ab-277">Contoso</span><span class="sxs-lookup"><span data-stu-id="219ab-277">Contoso</span></span>         | <span data-ttu-id="219ab-278">C3MGR</span><span class="sxs-lookup"><span data-stu-id="219ab-278">C3MGR</span></span>            | <span data-ttu-id="219ab-279">店長</span><span class="sxs-lookup"><span data-stu-id="219ab-279">Store Manager</span></span> | <span data-ttu-id="219ab-280">000100, 000111</span><span class="sxs-lookup"><span data-stu-id="219ab-280">000100, 000111</span></span>         |
| <span data-ttu-id="219ab-281">Contoso</span><span class="sxs-lookup"><span data-stu-id="219ab-281">Contoso</span></span>         | <span data-ttu-id="219ab-282">C3CSH</span><span class="sxs-lookup"><span data-stu-id="219ab-282">C3CSH</span></span>            | <span data-ttu-id="219ab-283">出納係</span><span class="sxs-lookup"><span data-stu-id="219ab-283">Cashier</span></span>       | <span data-ttu-id="219ab-284">000110, 000120</span><span class="sxs-lookup"><span data-stu-id="219ab-284">000110, 000120</span></span>         |
| <span data-ttu-id="219ab-285">Contoso</span><span class="sxs-lookup"><span data-stu-id="219ab-285">Contoso</span></span>         | <span data-ttu-id="219ab-286">適用できません</span><span class="sxs-lookup"><span data-stu-id="219ab-286">Not applicable</span></span>   | <span data-ttu-id="219ab-287">在庫係</span><span class="sxs-lookup"><span data-stu-id="219ab-287">Stock Clerk</span></span>   | <span data-ttu-id="219ab-288">適用できません</span><span class="sxs-lookup"><span data-stu-id="219ab-288">Not applicable</span></span>         |

> [!TIP]
> <span data-ttu-id="219ab-289">最適な結果を得るには、対応する店舗在庫場所で登録を有効にし、ログインしたときに使用するペルソナの会社に会社を設定します。</span><span class="sxs-lookup"><span data-stu-id="219ab-289">For best results, activate a register in the corresponding store location, and set the company to the company of the persona that you plan to use when you sign in.</span></span> <span data-ttu-id="219ab-290">これにより、エクスペリエンス全体で、視覚プロファイルやブランド イメージを合わせることができます。</span><span class="sxs-lookup"><span data-stu-id="219ab-290">In this way, you help guarantee that the visual profile and branding images are aligned across the experience.</span></span> <span data-ttu-id="219ab-291">たとえば、レジ担当者用の Fabrikam レイアウトを表示する場合、ヒューストンストアのレジスターを有効にする必要があります。</span><span class="sxs-lookup"><span data-stu-id="219ab-291">For example, if you're interested in seeing a Fabrikam layout for a cashier, you should activate a register in the Houston store.</span></span>

<!-- Hiding until the content page is available on CustomerSource -->

<!-- ## Reference icons and images -->

<!-- The screen layouts, button grids, and visual profiles were created using images and icons that can be found in **Retail and Commerce \> Channel setup \> POS setup \> POS \> Images**. -->

<!-- ![Images in Dynamics 365 Commerce](../commerce/media/demo-screen-layouts-fig-5-1.png) -->

<!-- Use the [POS Icon and Image Mapping](../commerce/media/POS_Icon_and_Image_Mapping.xlsx) reference spreadsheet to locate operation icons, reference photos, swap logos, or provide new images of your own that can be referenced in custom designs. -->

<!-- END HIDDEN CONTENT -->


[!INCLUDE[footer-include](../includes/footer-banner.md)]