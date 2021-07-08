---
title: Microsoft Dynamics 365 Commerce での Store Commerce アプリ (プレビュー)
description: このトピックでは、Store Commerce アプリの設定および構成方法について説明します。
author: mugunthanm
ms.date: 04/13/2021
ms.topic: article
audience: Developer
ms.reviewer: rhaertle
ms.search.region: Global
ms.author: mumani
ms.search.validFrom: 04-20-2020
ms.dyn365.ops.version: AX 10.0.19
ms.openlocfilehash: b5a218c885a9e3923f38c54ced466dd5aaf630ac
ms.sourcegitcommit: 60afcd85b3b5b9e5e8981ebbb57c0161cf05e54b
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/09/2021
ms.locfileid: "6216705"
---
# <a name="store-commerce-app-in-microsoft-dynamics-365-commerce-preview"></a><span data-ttu-id="06103-103">Microsoft Dynamics 365 Commerce での Store Commerce アプリ (プレビュー)</span><span class="sxs-lookup"><span data-stu-id="06103-103">Store Commerce app in Microsoft Dynamics 365 Commerce (Preview)</span></span>

[!include [banner](../includes/banner.md)]

[!include [banner](../includes/preview-banner.md)]

<span data-ttu-id="06103-104">このトピックは、Dynamics 365 Commerce バージョン 10.0.20 およびそれ以降に適用されます。</span><span class="sxs-lookup"><span data-stu-id="06103-104">This topic applies to Dynamics 365 Commerce version 10.0.20 and later.</span></span>

<span data-ttu-id="06103-105">Microsoft Dynamics 365 Commerce の Store Commerce アプリは、レジ担当者、販売担当者、販売在庫担当者、在庫担当者、および店舗管理者などの第一線の作業者に豊富なコマース機能を提供します。</span><span class="sxs-lookup"><span data-stu-id="06103-105">The Store Commerce app in Microsoft Dynamics 365 Commerce provides rich commerce functionality for first-line workers such as cashiers, sales associates, inventory associates, stock clerks, and store managers.</span></span> <span data-ttu-id="06103-106">これらの作業者は、現金売りトランザクション、現金/シフト管理、顧客契約、支援販売、クライアンテリング、エンドレス アイル、注文処理/フルフィルメント、在庫管理、レポートなどのコマース操作を実行することができます。</span><span class="sxs-lookup"><span data-stu-id="06103-106">It lets these workers perform commerce operations such cash-and-carry transactions, cash/shift management, customer engagement, assisted selling, clienteling, endless aisle, order processing/fulfillment, inventory management, and reporting.</span></span>

<span data-ttu-id="06103-107">Store Commerce は、Modern 販売時点管理 (MPOS) とクラウド販売時点管理 (CPOS) の両方の利点を提供します。</span><span class="sxs-lookup"><span data-stu-id="06103-107">Store Commerce provides the benefits of both Modern Point of Sale (MPOS) and Cloud Point of Sale (CPOS).</span></span>

> [!NOTE]
> <span data-ttu-id="06103-108">Store Commerceは、プレビュー アプリケーションとしてリリースされます。</span><span class="sxs-lookup"><span data-stu-id="06103-108">Store Commerce is released as a preview app.</span></span> <span data-ttu-id="06103-109">同じくプレビュー中の [Microsoft Edge WebView2](/microsoft-edge/webview2/) コントロールが使用されます。</span><span class="sxs-lookup"><span data-stu-id="06103-109">It uses the [Microsoft Edge WebView2](/microsoft-edge/webview2/) control, which is also in preview.</span></span> <span data-ttu-id="06103-110">したがって、一般に使用可能 (GA) になるまで実稼働環境で Store Commerce を使用 **しません**。</span><span class="sxs-lookup"><span data-stu-id="06103-110">Therefore, do **not** use Store Commerce in production until it's generally available (GA).</span></span>

<span data-ttu-id="06103-111">Store Commerce は、[Microsoft Edge WebView2](/microsoft-edge/webview2/) コントロールを使用してクラウド販売時点管理 (CPOS) アプリを表示する Windows 用のシェル アプリです。</span><span class="sxs-lookup"><span data-stu-id="06103-111">Store Commerce is a shell app for Windows that uses the [Microsoft Edge WebView2](/microsoft-edge/webview2/) control to render the Cloud Point of Sale (CPOS) app.</span></span> <span data-ttu-id="06103-112">CPOS は Web ブラウザーでのみ実行できますが、Store Commerce は [Modern 販売時点管理 (MPOS)](retail-modern-pos-architecture.md) などのネイティブ WIndows アプリとして実行できます。</span><span class="sxs-lookup"><span data-stu-id="06103-112">Although CPOS can run only in a web browser, Store Commerce can run as a native Windows app such as [Modern Point of Sale (MPOS)](retail-modern-pos-architecture.md).</span></span>

<span data-ttu-id="06103-113">Store Commerce はローカル ハードウェア ステーションをサポートし、支払ターミナル、プリンター、キャッシュ ドロワーに直接統合できます。</span><span class="sxs-lookup"><span data-stu-id="06103-113">Store Commerce supports local hardware station, and can be directly integrated with a payment terminal, printer, and cash drawer.</span></span> <span data-ttu-id="06103-114">ハードウェア デバイスを使用するために共有のハードウェア ステーションを設定する必要はありません。</span><span class="sxs-lookup"><span data-stu-id="06103-114">You don't have to set up a shared hardware station to use hardware devices.</span></span>

<span data-ttu-id="06103-115">ユーザー インターフェイス (UI) を表示するために、Store Commerce は、ユニバーサル Windows プラットフォーム (UTC) アプリ表示フレームワークの代わりに Chromium エンジンを使用します。</span><span class="sxs-lookup"><span data-stu-id="06103-115">To render the user interface (UI), Store Commerce uses the Chromium engine instead of the Universal Windows Platform (UWP) app rendering framework.</span></span> <span data-ttu-id="06103-116">Chromium エンジンは、Windows の ネイティブの JavaScript UWP アプリよりも表示パフォーマンスが優れています。</span><span class="sxs-lookup"><span data-stu-id="06103-116">The Chromium engine has better rendering performance than the native JavaScript UWP app in Windows.</span></span> <span data-ttu-id="06103-117">MPOS と Store Commerce の主な違いは、Store Commerce がアプリを表示するのに Chromium エンジンを使用する点です。</span><span class="sxs-lookup"><span data-stu-id="06103-117">The main difference between MPOS and Store Commerce is that Store Commerce uses the Chromium engine to render the app.</span></span>

## <a name="benefits-of-store-commerce"></a><span data-ttu-id="06103-118">Store Commerce の利点</span><span class="sxs-lookup"><span data-stu-id="06103-118">Benefits of Store Commerce</span></span>

+ <span data-ttu-id="06103-119">Microsoft Store を使用した、簡略化したアプリケーション ライフサイクル管理 (ALM)。</span><span class="sxs-lookup"><span data-stu-id="06103-119">Simplified Application lifecycle management (ALM) using Microsoft Store.</span></span>
+ <span data-ttu-id="06103-120">MPOS または CPOS 用に開発された拡張機能または ISV コードは、Store Commerce で再利用できます。</span><span class="sxs-lookup"><span data-stu-id="06103-120">Extension or ISV code developed for MPOS or CPOS can be reused in Store Commerce.</span></span>
+ <span data-ttu-id="06103-121">Store Commerce は、MPOSとCPOSの両方の利点を提供します。</span><span class="sxs-lookup"><span data-stu-id="06103-121">Store Commerce provides the benefits of both MPOS and CPOS.</span></span>
+ <span data-ttu-id="06103-122">パフォーマンス向上。</span><span class="sxs-lookup"><span data-stu-id="06103-122">Better performance.</span></span>
+ <span data-ttu-id="06103-123">POS および拡張機能のアップグレードがより簡単になりました。</span><span class="sxs-lookup"><span data-stu-id="06103-123">Easier POS and extension upgrades.</span></span>
+ <span data-ttu-id="06103-124">専用のハードウェア ステーション (HWS) をサポートしています。</span><span class="sxs-lookup"><span data-stu-id="06103-124">Support for dedicated hardware station (HWS).</span></span>
+ <span data-ttu-id="06103-125">将来オフラインでサポートされます。</span><span class="sxs-lookup"><span data-stu-id="06103-125">Support for offline, in the future.</span></span>

## <a name="application-lifecycle-management"></a><span data-ttu-id="06103-126">アプリケーション ライフサイクル管理</span><span class="sxs-lookup"><span data-stu-id="06103-126">Application lifecycle management</span></span>

<span data-ttu-id="06103-127">Store Commerce は、Windows デバイスで実行するアプリです。</span><span class="sxs-lookup"><span data-stu-id="06103-127">Store Commerce is an app that runs on Windows devices.</span></span> <span data-ttu-id="06103-128">[Windows アプリ- Microsoft Store](https://aka.ms/StoreCommerceApp) から入手できるので、検索、ダウンロード、および配置が容易になります。</span><span class="sxs-lookup"><span data-stu-id="06103-128">It will be available from [Windows Apps - Microsoft Store](https://aka.ms/StoreCommerceApp) so that it's easier to find, download, and deploy.</span></span> <span data-ttu-id="06103-129">したがって、配置とサービスの全体的なライフサイクルは簡素化されます。</span><span class="sxs-lookup"><span data-stu-id="06103-129">Therefore, the overall lifecycle of deployment and servicing will be simplified.</span></span>

<span data-ttu-id="06103-130">Store Commerce には、上位互換性と下位互換性の両方があります。</span><span class="sxs-lookup"><span data-stu-id="06103-130">Store Commerce is both forward compatible and backward compatible.</span></span> <span data-ttu-id="06103-131">このアプリは、Windows ポリシーを設定するか、Intune のような Microsoft Store のアプリでサポートされている更新プログラムや配置ツールを使用して簡単に更新できます。</span><span class="sxs-lookup"><span data-stu-id="06103-131">It can easily be updated, either by setting up the Windows policy or by using any update and deployment tool that Microsoft Store apps support, such as Intune.</span></span> <span data-ttu-id="06103-132">このアプリは、Cloud Scale Unit (CSU) および拡張機能とは別に更新できます。</span><span class="sxs-lookup"><span data-stu-id="06103-132">It can be updated independently of the Cloud Scale Unit (CSU) and extensions.</span></span>

<span data-ttu-id="06103-133">MPOS の場合は、アプリを取得して拡張機能にパッケージ化するために、手動の管理が必要です。</span><span class="sxs-lookup"><span data-stu-id="06103-133">For MPOS, more manual management is required to get the app and package it with extensions.</span></span> <span data-ttu-id="06103-134">ただし、Store Commerce は Microsoft Store を通じて配置されるので、アプリケーション ライフサイクル管理 (ALM) を大幅に簡素化できます。</span><span class="sxs-lookup"><span data-stu-id="06103-134">However, because Store Commerce is deployed through Microsoft Store, application lifecycle management (ALM) is greatly simplified.</span></span>

<span data-ttu-id="06103-135">Store Commerce は、CPOS を表示するシェルです。</span><span class="sxs-lookup"><span data-stu-id="06103-135">Store Commerce is a shell that renders CPOS.</span></span> <span data-ttu-id="06103-136">したがって、更新された CPOS 機能を取得するには、CPOS も更新する必要があります。</span><span class="sxs-lookup"><span data-stu-id="06103-136">Therefore, to get the updated CPOS functionality, you should also update CPOS.</span></span> <span data-ttu-id="06103-137">CPOS は CSU から更新できます。</span><span class="sxs-lookup"><span data-stu-id="06103-137">CPOS can be updated from the CSU.</span></span> <span data-ttu-id="06103-138">CSU の更新方法の詳細については、[Commerce Scale Unit (クラウド) への更新プログラムと拡張機能の適用](../../fin-ops-core/dev-itpro/deployment/update-retail-channel.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="06103-138">For more information about how to update the CSU, see [Apply updates and extensions to Commerce Scale Unit (cloud)](../../fin-ops-core/dev-itpro/deployment/update-retail-channel.md).</span></span>

![Store Commerce](media/StoreCommerce.PNG)


## <a name="store-commerce-and-mpos-parity"></a><span data-ttu-id="06103-140">Store Commerce と MPOS の機能</span><span class="sxs-lookup"><span data-stu-id="06103-140">Store Commerce and MPOS parity</span></span>

<span data-ttu-id="06103-141">Store Commerce は、将来 MPOS と同等の機能を持つようになります。</span><span class="sxs-lookup"><span data-stu-id="06103-141">Store Commerce will have full functional parity with MPOS in the future.</span></span> <span data-ttu-id="06103-142">現時点では、Store Commerce はオフラインでの実行をサポートしません (Headless Commerce への接続がない場合)。</span><span class="sxs-lookup"><span data-stu-id="06103-142">Currently, Store Commerce doesn't support running offline (when there is no connectivity to Headless Commerce).</span></span> <span data-ttu-id="06103-143">さまざまな POS アプリおよびトポロジの詳細については [Modern POS (MPOS) かクラウド POS かの選択](../mpos-or-cpos.md) を参照する</span><span class="sxs-lookup"><span data-stu-id="06103-143">For more information about the different POS apps and topology, see [Choose between Modern POS (MPOS) and Cloud POS](../mpos-or-cpos.md)</span></span>

## <a name="store-commerce-and-cpos-parity"></a><span data-ttu-id="06103-144">Store Commerce と CPOS の機能</span><span class="sxs-lookup"><span data-stu-id="06103-144">Store Commerce and CPOS parity</span></span>

<span data-ttu-id="06103-145">Store Commerce では CPOS が表示され、CPOS と同等の機能を持つほか、Store Commerce は専用のハードウェア ステーションをサポートし、将来はオフラインでサポートすることができます。</span><span class="sxs-lookup"><span data-stu-id="06103-145">Store Commerce renders CPOS and have full functional parity with CPOS, Store Commerce  in addition supports dedicated hardware station and supports offline in the future.</span></span>

## <a name="choosing-between-store-commerce-and-mpos"></a><span data-ttu-id="06103-146">Store Commerce か MPOS かの選択</span><span class="sxs-lookup"><span data-stu-id="06103-146">Choosing between Store Commerce and MPOS</span></span>

<span data-ttu-id="06103-147">Store Commerce では CPOS が表示されますが、MPOS と同等の機能があります。</span><span class="sxs-lookup"><span data-stu-id="06103-147">Store Commerce renders CPOS but has full parity with MPOS.</span></span> <span data-ttu-id="06103-148">Store Commerce と MPOS はユニバーサル Windows プラットフォーム (UTC) アプリで、ローカル ハードウェア ステーションをサポートしています。</span><span class="sxs-lookup"><span data-stu-id="06103-148">Both Store Commerce and MPOS are Universal Windows Platform (UWP) apps and they support local hardware station.</span></span> <span data-ttu-id="06103-149">Store Commerce は現在、オフラインでサポートされていませんが、将来サポートされる予定です。</span><span class="sxs-lookup"><span data-stu-id="06103-149">Store Commerce doesn't currently support offline, but it will in the future.</span></span> 

<span data-ttu-id="06103-150">Store Commerceでは、UI を表示するために Chromium エンジンが使用され、表示パフォーマンスが MPOS よりも向上します。</span><span class="sxs-lookup"><span data-stu-id="06103-150">Because Store Commerce uses the Chromium engine to render the UI, it provides better rendering performance than MPOS.</span></span> <span data-ttu-id="06103-151">さらに、Store Commerce は Microsoft Store を通じて配置されるので、ALM を大幅に簡素化できます。</span><span class="sxs-lookup"><span data-stu-id="06103-151">Additionally, because Store Commerce is deployed through Microsoft Store, ALM is greatly simplified.</span></span> <span data-ttu-id="06103-152">対照的に、MPOS は Microsoft Dynamics Lifecycle Service (LCS) と Commerce 本社を使用してセルフサービスを行います。</span><span class="sxs-lookup"><span data-stu-id="06103-152">By contrast, MPOS is self-serviced by using Microsoft Dynamics Lifecycle Service (LCS) and Commerce headquarters.</span></span>

<span data-ttu-id="06103-153">最終的には、MPOS は非推奨になり、Store Commerce に置き換えられる予定です。</span><span class="sxs-lookup"><span data-stu-id="06103-153">Eventually, MPOS will be deprecated and replaced by Store Commerce.</span></span>

<span data-ttu-id="06103-154">店舗でオフライン サポートを必要としない場合は、MPOS の代わりに Store Commerce を選択する必要があります。</span><span class="sxs-lookup"><span data-stu-id="06103-154">If you don't require offline support in your store, you should choose Store Commerce instead of MPOS.</span></span>

<table>
<thead>
<tr>
<th></th>
<th><span data-ttu-id="06103-155">Store Commerce (プレビュー)</span><span class="sxs-lookup"><span data-stu-id="06103-155">Store Commerce (Preview)</span></span></th>
<th><span data-ttu-id="06103-156">MPOS</span><span class="sxs-lookup"><span data-stu-id="06103-156">MPOS</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<th scope="row"><span data-ttu-id="06103-157">操作環境</span><span class="sxs-lookup"><span data-stu-id="06103-157">Operating environment</span></span></th>
<td><span data-ttu-id="06103-158">Windows</span><span class="sxs-lookup"><span data-stu-id="06103-158">Windows</span></span></td>
<td><span data-ttu-id="06103-159">Windows</span><span class="sxs-lookup"><span data-stu-id="06103-159">Windows</span></span></td>
</tr>
<tr>
<th scope="row"><span data-ttu-id="06103-160">ALM</span><span class="sxs-lookup"><span data-stu-id="06103-160">ALM</span></span></th>
<td><span data-ttu-id="06103-161">Store Commerce は Microsoft Store を通じて配置され、CPOS は CSU を通じて配置します。</span><span class="sxs-lookup"><span data-stu-id="06103-161">Store Commerce is deployed through Microsoft Store, and CPOS is deployed through CSU.</span></span></td>
<td><span data-ttu-id="06103-162">MPOS は、LCS および Commerce 本社を使用してセルフサービスを行います。</span><span class="sxs-lookup"><span data-stu-id="06103-162">MPOS is self-serviced by using LCS and Commerce headquarters.</span></span> <span data-ttu-id="06103-163">MPOS インストーラーを使用してパッケージ化され、インストールされます。</span><span class="sxs-lookup"><span data-stu-id="06103-163">It's packaged and installed by using the MPOS installer.</span></span></td>
</tr>
<tr>
<th scope="row"><span data-ttu-id="06103-164">拡張子</span><span class="sxs-lookup"><span data-stu-id="06103-164">Extensions</span></span></th>
<td><span data-ttu-id="06103-165">拡張機能は CPOS に配置します。</span><span class="sxs-lookup"><span data-stu-id="06103-165">Extensions are deployed to CPOS.</span></span></td>
<td><span data-ttu-id="06103-166">拡張機能が MPOS と共にパッケージ化されるか、あるいは独立した拡張パッケージが使用されます。</span><span class="sxs-lookup"><span data-stu-id="06103-166">Extensions are packaged with MPOS, or an independent extension package is used.</span></span></td>
</tr>
<tr>
<th scope="row"><span data-ttu-id="06103-167">オフライン モードでのサポート</span><span class="sxs-lookup"><span data-stu-id="06103-167">Support for offline mode</span></span></th>
<td><span data-ttu-id="06103-168">いいえ (将来追加する予定)</span><span class="sxs-lookup"><span data-stu-id="06103-168">No (but it will be added in the future)</span></span></td>
<td><span data-ttu-id="06103-169">あり</span><span class="sxs-lookup"><span data-stu-id="06103-169">Yes</span></span></td>
</tr>
<tr>
<th scope="row"><span data-ttu-id="06103-170">ローカル ハードウェア ステーションのサポート</span><span class="sxs-lookup"><span data-stu-id="06103-170">Support for local hardware station</span></span></th>
<td><span data-ttu-id="06103-171">あり</span><span class="sxs-lookup"><span data-stu-id="06103-171">Yes</span></span></td>
<td><span data-ttu-id="06103-172">あり</span><span class="sxs-lookup"><span data-stu-id="06103-172">Yes</span></span></td>
</tr>
<tr>
<th scope="row"><span data-ttu-id="06103-173">UI レンダリング エンジン</span><span class="sxs-lookup"><span data-stu-id="06103-173">UI rendering engine</span></span></th>
<td><span data-ttu-id="06103-174">UI の表示には、Curomium エンジンが使用されます。</span><span class="sxs-lookup"><span data-stu-id="06103-174">The Chromium engine is used to render the UI.</span></span></td>
<td><span data-ttu-id="06103-175">UI の表示には UWP アプリの表示フレームワークが使用されます。</span><span class="sxs-lookup"><span data-stu-id="06103-175">The UWP app rendering framework is used to render the UI.</span></span></td>
</tr>
</tbody>
</table>

## <a name="setup-and-installation"></a><span data-ttu-id="06103-176">設定およびインストール</span><span class="sxs-lookup"><span data-stu-id="06103-176">Setup and installation</span></span>

### <a name="prerequisite"></a><span data-ttu-id="06103-177">前提条件</span><span class="sxs-lookup"><span data-stu-id="06103-177">Prerequisite</span></span>

+ <span data-ttu-id="06103-178">Windows 10 バージョン 17763.0 またはそれ以上、または Windows Server 2019。</span><span class="sxs-lookup"><span data-stu-id="06103-178">Windows 10 version 17763.0 or higher or Windows Server 2019.</span></span>
+ <span data-ttu-id="06103-179">Microsoft Edge、アプリは Microsoft Edge WebView2 コントロールを使用するためです。</span><span class="sxs-lookup"><span data-stu-id="06103-179">Microsoft Edge, because the app uses the Microsoft Edge WebView2 control.</span></span>
+ <span data-ttu-id="06103-180">Dynamics 365 Commerce (バック オフィスおよび CPOS)。</span><span class="sxs-lookup"><span data-stu-id="06103-180">Dynamics 365 Commerce (Back office and CPOS).</span></span>

### <a name="device-setup-in-commerce-headquarters"></a><span data-ttu-id="06103-181">Commerce 本社でのデバイスの設定</span><span class="sxs-lookup"><span data-stu-id="06103-181">Device setup in Commerce headquarters</span></span>

<span data-ttu-id="06103-182">Store Commerce のために、**Store Commerce** という名前の新しいアプリケーション タイプが **デバイス** ページに追加されました (**Retail と Commerce \> チャネル設定 \> POS 設定 \> デバイス**)。</span><span class="sxs-lookup"><span data-stu-id="06103-182">For Store Commerce, a new application type that is named **Store Commerce** has been added on the **Devices** page (**Retail and Commerce \> Channel setup \> POS setup \> Devices**).</span></span> <span data-ttu-id="06103-183">Store Commerce でデバイスを作成する場合、このアプリケーション タイプを選択します。</span><span class="sxs-lookup"><span data-stu-id="06103-183">Select this application type when you create a device for Store Commerce.</span></span>

<span data-ttu-id="06103-184">Store Commerce アプリケーション タイプがドロップ ダウン メニューで表示されない場合は、Retail と Commerce > 本社設定 > パラメーター > コマース パラメーター > 一般 > **初期化子** から **初期化** 実行し、ページを更新します。</span><span class="sxs-lookup"><span data-stu-id="06103-184">If you are not able to see the Store Commerce application type in the drop down menu, try running the **Initialize** from the Retail and Commerce > Headquarters setup > Parameters> Commerce parameters > General  > **Initializer** and refresh the page.</span></span>

<span data-ttu-id="06103-185">Store Commerce のために[登録](../tasks/create-associate-registers.md) と[デバイス](../tasks/create-associate-device.md) を作成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="06103-185">You must create a [register](../tasks/create-associate-registers.md) and a [device](../tasks/create-associate-device.md) for Store Commerce.</span></span> <span data-ttu-id="06103-186">その後、アプリを有効にする前に、Commerce 本社の配送スケジュールからレジスター ジョブを実行します。</span><span class="sxs-lookup"><span data-stu-id="06103-186">Then, before you activate the app, run the register job from the distribution schedule in Commerce headquarters.</span></span> <span data-ttu-id="06103-187">デバイスの作成中に、**アプリケーション タイプ** フィールドを **Store Commerce** に設定します。</span><span class="sxs-lookup"><span data-stu-id="06103-187">During device creation, set the **Application type** field to **Store Commerce**.</span></span>

<span data-ttu-id="06103-188">Store Commerce は Microsoft Store で使用できます。</span><span class="sxs-lookup"><span data-stu-id="06103-188">Store Commerce is available in Microsoft Store.</span></span> <span data-ttu-id="06103-189">アプリをダウンロードおよびインストールするには、これらの手順に従います。</span><span class="sxs-lookup"><span data-stu-id="06103-189">To download and install the app, follow these steps.</span></span>

1. <span data-ttu-id="06103-190">[Windows アプリ- Microsoft Store](https://aka.ms/StoreCommerceApp) を開き、**Store Commerce** を検索します。</span><span class="sxs-lookup"><span data-stu-id="06103-190">Open [Windows Apps - Microsoft Store](https://aka.ms/StoreCommerceApp), and search for **Store Commerce**.</span></span>
2. <span data-ttu-id="06103-191">**入手** を選択し、アプリをインストールします。 </span><span class="sxs-lookup"><span data-stu-id="06103-191">Select **Get** to install the app.</span></span>
3. <span data-ttu-id="06103-192">Windows の **スタート** メニューで **Store Commerce** を検索し、アプリを開きます。</span><span class="sxs-lookup"><span data-stu-id="06103-192">On the Windows **Start** menu, search for **Store Commerce**, and open the app.</span></span>

<span data-ttu-id="06103-193">アプリの起動後、次の手順に従って、アプリを構成および有効化します。</span><span class="sxs-lookup"><span data-stu-id="06103-193">After the app is opened, follow these steps to configure and activate it.</span></span>

1. <span data-ttu-id="06103-194">アプリの開始ページに、CPOS の URL を入力します。</span><span class="sxs-lookup"><span data-stu-id="06103-194">On the app's start page, enter the CPOS URL.</span></span> <span data-ttu-id="06103-195">このURLは、LCSの環境詳細ページ、または Commerce の **チャネル プロファイル** ページで確認できます (**Dynamics 365 Commerce\> チャネル設定 \> チャネル プロファイル**)。</span><span class="sxs-lookup"><span data-stu-id="06103-195">You can find this URL on the environment details page in LCS or on the **Channel profiles** page in Commerce (**Dynamics 365 Commerce \> Channel setup \> Channel profiles**).</span></span>
2. <span data-ttu-id="06103-196">**保存** を選択します。</span><span class="sxs-lookup"><span data-stu-id="06103-196">Select **Save**.</span></span>
3. <span data-ttu-id="06103-197">Store Commerce を有効にするには、POS有効化ガイドの [POS の有効ガイド](retail-device-activation.md#activate-a-modern-pos-or-cloud-pos-device-by-using-guided-activation) の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="06103-197">Activate Store Commerce be following the steps in [POS activation guide](retail-device-activation.md#activate-a-modern-pos-or-cloud-pos-device-by-using-guided-activation).</span></span>
4. <span data-ttu-id="06103-198">従業員アカウントを使用してサイン インします。</span><span class="sxs-lookup"><span data-stu-id="06103-198">Sign in by using an employee account.</span></span>

<span data-ttu-id="06103-199">これで、コマース操作を完了できます。</span><span class="sxs-lookup"><span data-stu-id="06103-199">You can now complete your commerce operations.</span></span>

### <a name="troubleshooting-setup-issues"></a><span data-ttu-id="06103-200"> 設定の問題に関するトラブルシューティング</span><span class="sxs-lookup"><span data-stu-id="06103-200">Troubleshooting setup issues</span></span>

#### <a name="reset-the-app"></a><span data-ttu-id="06103-201">アプリのリセット</span><span class="sxs-lookup"><span data-stu-id="06103-201">Reset the app</span></span>

<span data-ttu-id="06103-202">入力した CPOS URL が無効で、変更したい場合、または、有効化の際にアプリがエラー状態にある場合は、アプリをリセットしてプロセスを再開できます。</span><span class="sxs-lookup"><span data-stu-id="06103-202">If the CPOS URL that you entered isn't valid and you want to change it, or if the app is in an error state during activation, you can restart the process by resetting the app.</span></span>

1. <span data-ttu-id="06103-203">Windowsvの **スタート** メニューで、アプリを選択したまま (あるいは右クリックして) 、それから **詳細 \>アプリの設定** を選択します。</span><span class="sxs-lookup"><span data-stu-id="06103-203">On the Windows **Start** menu, select and hold (or right-click) the app, and then select **More \> App settings**.</span></span>
2. <span data-ttu-id="06103-204">アプリ設定ページを **リセット** ボタンが見つかるまで下にスクロールします。</span><span class="sxs-lookup"><span data-stu-id="06103-204">Scroll down the app settings page until you find the **Reset** button.</span></span>
3. <span data-ttu-id="06103-205">**リセット** を選択し、表示されたらアプリのリセットを確認します。</span><span class="sxs-lookup"><span data-stu-id="06103-205">Select **Reset**, and then, when you're prompted, confirm that you want to reset the app.</span></span>

## <a name="customizing-the-app"></a><span data-ttu-id="06103-206">アプリのカスタマイズ</span><span class="sxs-lookup"><span data-stu-id="06103-206">Customizing the app</span></span>

<span data-ttu-id="06103-207">Retail ソフトウェア開発キット (SDK) が提供する POS 拡張機能サポートを使用して、Store Commerce をカスタマイズできます。</span><span class="sxs-lookup"><span data-stu-id="06103-207">You can customize Store Commerce by using the POS extension support that the Retail software development kit (SDK) provides.</span></span> <span data-ttu-id="06103-208">POS のユーザー エクスペリエンスの変更と作成、標準の機能拡張または変更、検証の追加、カスタム機能の追加を行うことができます。</span><span class="sxs-lookup"><span data-stu-id="06103-208">You can modify and create the POS user experience, enhance or modify out-of-box functionality, add validations, and add custom features.</span></span> <span data-ttu-id="06103-209">- 詳細については、[販売時点管理 (POS) の拡張機能の概要](pos-extension/pos-extension-overview.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="06103-209">For more information, see [Point of Sale (POS) extension overview](pos-extension/pos-extension-overview.md).</span></span>

<span data-ttu-id="06103-210">Retail SDK を使用して開発された拡張機能は、CPOS、MPOS、および Store Commerce で機能します。</span><span class="sxs-lookup"><span data-stu-id="06103-210">Extensions that are developed by using the Retail SDK will work for CPOS, MPOS, and Store Commerce.</span></span> <span data-ttu-id="06103-211">ただし、MPOS と CPOSによって拡張機能をパッケージ化して配置する方法は異なります。</span><span class="sxs-lookup"><span data-stu-id="06103-211">However, the way that the extension is packaged and deployed by MPOS and CPOS differs.</span></span>

<span data-ttu-id="06103-212">Store Commerce では CPOS が表示されるので、CPOS のパッケージと配置のオプションに従って Store Commerce の拡張機能を配置する必要があります。</span><span class="sxs-lookup"><span data-stu-id="06103-212">Because Store Commerce renders CPOS, you must follow the CPOS packaging and deployment options to deploy Store Commerce extensions.</span></span>

### <a name="hardware-station-extension"></a><span data-ttu-id="06103-213">ハードウェア ステーション拡張機能</span><span class="sxs-lookup"><span data-stu-id="06103-213">Hardware station extension</span></span>

<span data-ttu-id="06103-214">Store Commerceは、ハードウェア デバイスと統合できるよう拡張することができます。</span><span class="sxs-lookup"><span data-stu-id="06103-214">Store Commerce can be extended so that it's integrated with hardware devices.</span></span> <span data-ttu-id="06103-215">GitHub で追加された[サンプル拡張機能コード](https://github.com/microsoft/Dynamics365Commerce.InStore/tree/release/9.28/src/PosSample) を使用して、Store Commerce ハードウェア ステーションの拡張機能 (HWS) のパッケージを生成できます。</span><span class="sxs-lookup"><span data-stu-id="06103-215">You can use the [sample extension code](https://github.com/microsoft/Dynamics365Commerce.InStore/tree/release/9.28/src/PosSample) that has been added in GitHub to generate Store Commerce hardware station extension (HWS) packages.</span></span> <span data-ttu-id="06103-216">詳細については [POS と新しいハードウェア デバイスの統合](hardware-device-extension.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="06103-216">For more information, see [Integrate the POS with a new hardware device](hardware-device-extension.md).</span></span>

## <a name="known-issues-with-the-microsoft-edge-webview2-control"></a><span data-ttu-id="06103-217">Microsoft Edge WebView2 コントロールに関する既知の問題</span><span class="sxs-lookup"><span data-stu-id="06103-217">Known issues with the Microsoft Edge WebView2 control</span></span>

+ <span data-ttu-id="06103-218">有効化の際に、複数のオプションを使用して AAD パスワードを入力するように求めるメッセージが表示されたら、パスワードを選択します。</span><span class="sxs-lookup"><span data-stu-id="06103-218">During activation, when prompted for entering the AAD password with multiple options, choose password.</span></span> <span data-ttu-id="06103-219">他のオプションが機能しない場合があります。</span><span class="sxs-lookup"><span data-stu-id="06103-219">The other options might not work.</span></span>
+ <span data-ttu-id="06103-220">Tab キーを押すと、アプリ内のタブが機能しない場合があります。</span><span class="sxs-lookup"><span data-stu-id="06103-220">Tabbing inside the app by pressing the Tab key may not work.</span></span> <span data-ttu-id="06103-221">代わりに、項目をクリックまたは選択します。</span><span class="sxs-lookup"><span data-stu-id="06103-221">Instead, click or select items.</span></span>
+ <span data-ttu-id="06103-222">マウスを使用してドロップダウンを選択できない場合があります。</span><span class="sxs-lookup"><span data-stu-id="06103-222">Using the mouse for drop-down selection might not work.</span></span> <span data-ttu-id="06103-223">代わりに、キーボードを使用して選択します。</span><span class="sxs-lookup"><span data-stu-id="06103-223">Instead, use the keyboard to make a selection.</span></span>

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
