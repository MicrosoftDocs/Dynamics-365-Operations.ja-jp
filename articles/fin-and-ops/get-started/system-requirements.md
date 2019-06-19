---
title: クラウド配置のシステム要件
description: このトピックは、現在のバージョンの Microsoft Dynamics 365 for Finance and Operations におけるクラウド配置のシステム要件を一覧表示します。
author: sericks007
manager: AnnBe
ms.date: 12/17/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Developer, IT Pro
ms.reviewer: sericks
ms.search.scope: Operations
ms.custom: 55651
ms.assetid: e564d51d-42d3-47c5-b388-93b8219c692a
ms.search.region: Global
ms.author: sericks
ms.search.validFrom: 2016-08-30
ms.dyn365.ops.version: Platform update 8
ms.openlocfilehash: f23c558e5482242600ea14a58b083f36a676f28c
ms.sourcegitcommit: 574d4dda83dcab94728a3d35fc53ee7e2b90feb0
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/22/2019
ms.locfileid: "1595480"
---
# <a name="system-requirements-for-cloud-deployments"></a><span data-ttu-id="31acf-103">クラウド配置のシステム要件</span><span class="sxs-lookup"><span data-stu-id="31acf-103">System requirements for cloud deployments</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="31acf-104">このトピックは、現在のバージョンの Microsoft Dynamics 365 for Finance and Operations におけるクラウド配置のシステム要件を一覧表示します。</span><span class="sxs-lookup"><span data-stu-id="31acf-104">This topic lists the system requirements for the current version of Microsoft Dynamics 365 for Finance and Operations for cloud deployments.</span></span> <span data-ttu-id="31acf-105">Finance and Operations をインストールする前に、このステップが適切な場合、作業しているシステムがネットワーク、ハードウェア、およびソフトウェアの最小要件を満たしているか、または超えているかを検証する必要があります。</span><span class="sxs-lookup"><span data-stu-id="31acf-105">If this step is appropriate, before you install Finance and Operations, you should verify that the system that you're working with meets or exceeds the minimum network, hardware, and software requirements.</span></span>

## <a name="supported-web-browsers"></a><span data-ttu-id="31acf-106">サポートされている Web ブラウザー</span><span class="sxs-lookup"><span data-stu-id="31acf-106">Supported web browsers</span></span>

<span data-ttu-id="31acf-107">Web アプリケーションは、指定されたオペレーティング システムで実行される次のすべての Web ブラウザで実行できます。</span><span class="sxs-lookup"><span data-stu-id="31acf-107">The web application can run in any of the following web browsers that run on the specified operating systems:</span></span>

- <span data-ttu-id="31acf-108">Windows 10 の Microsoft Edge (公開されている最新のバージョン)</span><span class="sxs-lookup"><span data-stu-id="31acf-108">Microsoft Edge (latest publicly available version) on Windows 10</span></span>
- <span data-ttu-id="31acf-109">Windows 10、Windows 8.1、または Windows 7 の Internet Explorer 11</span><span class="sxs-lookup"><span data-stu-id="31acf-109">Internet Explorer 11 on Windows 10, Windows 8.1, or Windows 7</span></span>
- <span data-ttu-id="31acf-110">Google Chrome (公開されている最新バージョン)</span><span class="sxs-lookup"><span data-stu-id="31acf-110">Google Chrome (latest publicly available version)</span></span> 
- <span data-ttu-id="31acf-111">Apple Safari (公開されている最新バージョン)</span><span class="sxs-lookup"><span data-stu-id="31acf-111">Apple Safari (latest publicly available version)</span></span>

<span data-ttu-id="31acf-112">各 Web ブラウザーの最新版を検索するには、ソフトウェア メーカーの Web サイトに移動します。</span><span class="sxs-lookup"><span data-stu-id="31acf-112">To find the latest release for each web browser, go to the software manufacturer's website.</span></span>

> [!NOTE]
> - <span data-ttu-id="31acf-113">タスク レコーダーがスクリーンショットをキャプチャし、生成された Microsoft Word ドキュメントにそれらを含めるには、プレリリース版の Chrome 拡張機能をインストールする必要があります。</span><span class="sxs-lookup"><span data-stu-id="31acf-113">To enable Task Recorder to capture screenshots and include them in Microsoft Word documents that are generated, you must install a pre-release Chrome extension.</span></span> <!---For instructions about how to install the extension, see [Screenshot Extension setup](../../dev-itpro/user-interface/task-recorder).-->
> - <span data-ttu-id="31acf-114">財務報告のワークフロー エディターおよびレポート デザイナーは、ClickOnce アプリケーションとして起動されます。</span><span class="sxs-lookup"><span data-stu-id="31acf-114">The Workflow Editor and Report Designer for Financial reporting are started as ClickOnce applications.</span></span> <span data-ttu-id="31acf-115">それには 64 ビットの互換性のあるオペレーティング システムが必要です。</span><span class="sxs-lookup"><span data-stu-id="31acf-115">They require a 64-bit-compatible operating system.</span></span> <span data-ttu-id="31acf-116">Microsoft Edge と Internet Explorer (Microsoft Windows のサポートされているバージョン) のみが、ClickOnce アプリケーションをそのままの状態でサポートします。</span><span class="sxs-lookup"><span data-stu-id="31acf-116">Only Microsoft Edge and Internet Explorer (on a supported version of Microsoft Windows) support ClickOnce applications out of the box.</span></span> <span data-ttu-id="31acf-117">Chrom を使用している場合、ClickOnce アプリケーションを使用するには、[Meta4](https://chrome.google.com/webstore/detail/meta4-clickonce-launcher/jkncabbipkgbconhaajbapbhokpbgkdc) などの ClickOnce 拡張をインストールする必要があります。</span><span class="sxs-lookup"><span data-stu-id="31acf-117">If you're using Chrome, you must install a ClickOnce extension, such as [Meta4](https://chrome.google.com/webstore/detail/meta4-clickonce-launcher/jkncabbipkgbconhaajbapbhokpbgkdc) to use ClickOnce applications.</span></span> <span data-ttu-id="31acf-118">匿名モードで Chrome を使用する場合、ClickOnce の拡張機能が匿名モードに対しても有効化されていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="31acf-118">If you use Chrome in incognito mode, make sure that the ClickOnce extension is also enabled for incognito mode.</span></span>
> - <span data-ttu-id="31acf-119">PDF ファイルをプレビューするには、Windows 10 の Microsoft Edge (公開されている最新のバージョン)、もしくは Windows 10、Windows 8.1、Windows 8、Windows 7、または Google Nexus 10 タブレットの Google Chrome (公開されている最新のバージョン) などの最新のブラウザを使用することをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="31acf-119">To preview PDF files, we recommend that you use browsers such as Microsoft Edge (latest publicly available version) on Windows 10, or Google Chrome (latest publicly available version) on Windows 10, Windows 8.1, Windows 8, Windows 7, or Google Nexus 10 tablet.</span></span>

### <a name="supported-web-browsers-for-retail-cloud-pos"></a><span data-ttu-id="31acf-120">Retail Cloud POS でサポートされている Web ブラウザー</span><span class="sxs-lookup"><span data-stu-id="31acf-120">Supported web browsers for Retail Cloud POS</span></span>

<span data-ttu-id="31acf-121">Retail Cloud 販売時点管理 (POS) は、指定されたオペレーティング システムで実行される次のすべての Web ブラウザーで実行できます。</span><span class="sxs-lookup"><span data-stu-id="31acf-121">Retail Cloud point of sale (POS) can run in any of the following web browsers that run on the specified operating systems:</span></span>

- <span data-ttu-id="31acf-122">Windows 10 の Microsoft Edge (公開されている最新のバージョン)</span><span class="sxs-lookup"><span data-stu-id="31acf-122">Microsoft Edge (latest publicly available version) on Windows 10</span></span>
- <span data-ttu-id="31acf-123">Windows 10、Windows 8.1、または Windows 7 の Internet Explorer 11</span><span class="sxs-lookup"><span data-stu-id="31acf-123">Internet Explorer 11 on Windows 10, Windows 8.1, or Windows 7</span></span>
- <span data-ttu-id="31acf-124">Windows 10、Windows 8.1、または Windows 7 の Chrome (公開されている最新のバージョン)</span><span class="sxs-lookup"><span data-stu-id="31acf-124">Chrome (latest publicly available version) on Windows 10, Windows 8.1, or Windows 7</span></span>

## <a name="network-requirements"></a><span data-ttu-id="31acf-125">ネットワーク要件</span><span class="sxs-lookup"><span data-stu-id="31acf-125">Network requirements</span></span>

- <span data-ttu-id="31acf-126">Finance and Operations は、待機時間が 250 ～ 300 ミリ秒 (ms) 以下のネットワーク用に設計されています。</span><span class="sxs-lookup"><span data-stu-id="31acf-126">Finance and Operations is designed for networks that have a latency of 250–300 milliseconds (ms) or less.</span></span> <span data-ttu-id="31acf-127">この待機時間は、ブラウザー クライアントから Finance and Operations をホストする Microsoft Azure データ センターまでの待機時間のことです。</span><span class="sxs-lookup"><span data-stu-id="31acf-127">This latency is the latency from a browser client to the Microsoft Azure datacenter that hosts Finance and Operations.</span></span> <span data-ttu-id="31acf-128">[AzureSpeed.com](http://www.azurespeed.com) にてネットワークの待機時間をテストすることをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="31acf-128">We recommend that you test network latency at [AzureSpeed.com](http://www.azurespeed.com).</span></span>
- <span data-ttu-id="31acf-129">Finance and Operations の帯域幅の要件はシナリオによって異なります。</span><span class="sxs-lookup"><span data-stu-id="31acf-129">Bandwidth requirements for Finance and Operations depend on your scenario.</span></span> <span data-ttu-id="31acf-130">最も一般的なシナリオでは、毎秒 50 キロバイト (KBps) を超える帯域幅が必要です。</span><span class="sxs-lookup"><span data-stu-id="31acf-130">Most typical scenarios require a bandwidth that is more than 50 kilobytes per second (KBps).</span></span> <span data-ttu-id="31acf-131">ただし、ワークスペースや大がかりなカスタマイズを含む高度な伝送データ要件があるシナリオには、帯域幅を増やすことを勧めます。</span><span class="sxs-lookup"><span data-stu-id="31acf-131">However, we recommend more bandwidth for scenarios that have high payload requirements, such as scenarios that involve workspaces or extensive customization.</span></span>

<span data-ttu-id="31acf-132">一般に、Finance and Operations は、インターネットに最適化されます。</span><span class="sxs-lookup"><span data-stu-id="31acf-132">In general, Finance and Operations is optimized for the internet.</span></span> <span data-ttu-id="31acf-133">ブラウザー クライアントから Azure データセンターへのラウンド トリップの数は非常に小さく、全伝送データは圧縮されます。</span><span class="sxs-lookup"><span data-stu-id="31acf-133">The number of round trips from a browser client to the Azure datacenter is very small, and the whole payload is compressed.</span></span>

> [!WARNING]
> <span data-ttu-id="31acf-134">ユーザー数に帯域幅要件の最小値を掛けて、クライアントの場所からの帯域幅要件を計算しないでください。</span><span class="sxs-lookup"><span data-stu-id="31acf-134">Don't calculate bandwidth requirements from a client location by multiplying the number of users by the minimum bandwidth requirements.</span></span> <span data-ttu-id="31acf-135">特定の場所の同時使用は非常に計算が困難です。</span><span class="sxs-lookup"><span data-stu-id="31acf-135">The concurrent usage of a given location is very difficult to calculate.</span></span> <span data-ttu-id="31acf-136">帯域幅の要件について懸念する顧客は、Finance and Operations のプレビュー バージョンを使用するべきです。</span><span class="sxs-lookup"><span data-stu-id="31acf-136">Customers who are concerned about bandwidth requirements should use a preview version of Finance and Operations.</span></span>

## <a name="net-framework-requirements"></a><span data-ttu-id="31acf-137">.NET Framework 要件</span><span class="sxs-lookup"><span data-stu-id="31acf-137">.NET Framework requirements</span></span>

<span data-ttu-id="31acf-138">Finance and Operations では、ドキュメント回覧エージェントなどのすべての ClickOnce アプリケーション用として Microsoft .NET Framework バージョン 4.6.2 が必要です。</span><span class="sxs-lookup"><span data-stu-id="31acf-138">Finance and Operations requires the Microsoft .NET Framework version 4.6.2 for all ClickOnce applications, such as the document routing agent.</span></span> <span data-ttu-id="31acf-139">インストール手順については、[開発者の .NET Framework のインストール](https://msdn.microsoft.com/library/5a4x27ek(v=vs.110).aspx) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="31acf-139">For installation instructions, see [Install the .NET Framework for developers](https://msdn.microsoft.com/library/5a4x27ek(v=vs.110).aspx).</span></span>

## <a name="supported-microsoft-office-applications"></a><span data-ttu-id="31acf-140">サポートされる Microsoft Office アプリケーション</span><span class="sxs-lookup"><span data-stu-id="31acf-140">Supported Microsoft Office applications</span></span>

<span data-ttu-id="31acf-141">次の Microsoft Office アプリケーションは、Finance and Operations のクラウドおよびオンプレミス配置でサポートされています。</span><span class="sxs-lookup"><span data-stu-id="31acf-141">The following Microsoft Office applications are supported in cloud and on-premises deployments of Finance and Operations:</span></span>

- <span data-ttu-id="31acf-142">Microsoft Excel と Word のアドインを実行するには、Windows 用の Microsoft Office 2016 をインストールしておく必要があります。</span><span class="sxs-lookup"><span data-stu-id="31acf-142">To run the Microsoft Excel and Word add-ins, you must have Microsoft Office 2016 for Windows installed.</span></span> <span data-ttu-id="31acf-143">バージョン要求の詳細については、[Office 統合トラブルシューティング](../../dev-itpro/office-integration/office-integration-troubleshooting.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="31acf-143">For more information about version requirements, see [Office integration troubleshooting](../../dev-itpro/office-integration/office-integration-troubleshooting.md).</span></span>
- <span data-ttu-id="31acf-144">Excel にエクスポートまたはWord にエクスポート機能によって生成されたドキュメントを表示するには、Microsoft Office 2007 以降をインストールしておく必要があります。</span><span class="sxs-lookup"><span data-stu-id="31acf-144">To view documents that are generated by the Export to Excel or Export to Word functionality, you must have Microsoft Office 2007 or later installed.</span></span>

## <a name="retail-modern-pos-for-windows-requirements"></a><span data-ttu-id="31acf-145">Windows 用 Retail Modern POS の要件</span><span class="sxs-lookup"><span data-stu-id="31acf-145">Retail Modern POS for Windows requirements</span></span>

> [!NOTE]
> - <span data-ttu-id="31acf-146">Retail Modern POS でオフライン データベースを使う場合、コンピューターは Microsoft SQL Server のすべてのシステム要件を満たす必要があります。</span><span class="sxs-lookup"><span data-stu-id="31acf-146">If Retail Modern POS will use an offline database, the computer must meet all system requirements for Microsoft SQL Server.</span></span> <span data-ttu-id="31acf-147">Retail Modern POS のオフライン データベースは、Service Pack 3 以降の SQL Server 2012、Service Pack 2 以降の SQL Server 2014 、または SQL Server 2016 が必要です。</span><span class="sxs-lookup"><span data-stu-id="31acf-147">An offline database for Retail Modern POS requires SQL Server 2012 with Service Pack 3 or later, SQL Server 2014 with Service Pack 2 or later, or SQL Server 2016.</span></span> <span data-ttu-id="31acf-148">使用されている SQL Server のバージョンには、フルテキスト検索機能がインストールされている必要があります。</span><span class="sxs-lookup"><span data-stu-id="31acf-148">The SQL Server version used must have the Full-Text Search feature installed.</span></span> <span data-ttu-id="31acf-149">常に利用可能な最新のバージョンを使用し、すべての最新サービス パックをインストールすることをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="31acf-149">We recommend that you always use the latest version that is available, and that you install all the latest service packs.</span></span> <span data-ttu-id="31acf-150">これらの推奨事項に従うことで、互換性とセキュリティの両方を確保できます。</span><span class="sxs-lookup"><span data-stu-id="31acf-150">By following these recommendations, you can help to ensure both compatibility and security.</span></span>
> - <span data-ttu-id="31acf-151">2018 年 10 月 1 日以降、Retail Modern POS や他のクライアント側コンポーネントを使用するには、Microsoft .NET Framework version 4.6.1 以降をインストールする必要があります。</span><span class="sxs-lookup"><span data-stu-id="31acf-151">Starting October 1, 2018, Retail Modern POS and other client-side components require that the Microsoft .NET Framework version 4.6.1 or later be installed.</span></span> <span data-ttu-id="31acf-152">インストール手順については、[開発者の .NET Framework のインストール](https://msdn.microsoft.com/library/5a4x27ek(v=vs.110).aspx) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="31acf-152">For installation instructions, see [Install the .NET Framework for developers](https://msdn.microsoft.com/library/5a4x27ek(v=vs.110).aspx).</span></span>

### <a name="supported-windows-operating-systems"></a><span data-ttu-id="31acf-153">サポートされる Windows オペレーティング システム</span><span class="sxs-lookup"><span data-stu-id="31acf-153">Supported Windows operating systems</span></span>

- <span data-ttu-id="31acf-154">Retail Modern POS は 32 ビット アプリケーションですが、x86 と x64 アーキテクチャの両方で動作します。</span><span class="sxs-lookup"><span data-stu-id="31acf-154">Retail Modern POS is a 32-bit application, but it will run on both x86 and x64 architectures.</span></span>
- <span data-ttu-id="31acf-155">Retail Modern POS は Windows Server 2016、Windows 10 Pro、Windows 10 Enterprise、Windows 10 Enterprise Long Term Service Branch (LTSB) エディションおよび Windows 10 IOT Enterprise Edition でサポートされています。</span><span class="sxs-lookup"><span data-stu-id="31acf-155">Retail Modern POS is supported on Windows Server 2016, Windows 10 Pro, Windows 10 Enterprise, Windows 10 Enterprise Long Term Service Branch (LTSB), and Windows 10 IOT Enterprise editions.</span></span> <span data-ttu-id="31acf-156">少なくとも、Windows 10 Anniversary Update (バージョン 1607)、ビルド 14393 をインストールする必要があります。</span><span class="sxs-lookup"><span data-stu-id="31acf-156">At a minimum, the Windows 10 Anniversary Update (version 1607), build 14393, must be installed.</span></span>
- <span data-ttu-id="31acf-157">Windows 10 Pro がオペレーティング システムに対する更新を高度に管理できるドメイン内でない限り、Windows 10 Pro で Retail Modern POS および他の Retail コンポーネントの使用をお勧めしません。</span><span class="sxs-lookup"><span data-stu-id="31acf-157">It is not recommended to use Retail Modern POS and other Retail components on Windows 10 Pro unless within a domain as Windows 10 Pro doesn't allow for advanced management of updates to the operating system.</span></span>
- <span data-ttu-id="31acf-158">同じコンピューターで Retail Modern POS と他の Retail コンポーネントを組み合わせて使用することはお勧めできません。</span><span class="sxs-lookup"><span data-stu-id="31acf-158">It is not recommended to use Retail Modern POS and any other Retail component together on the same computer.</span></span>

### <a name="minimum-system-requirements"></a><span data-ttu-id="31acf-159">最少システム要件</span><span class="sxs-lookup"><span data-stu-id="31acf-159">Minimum system requirements</span></span>

- <span data-ttu-id="31acf-160">POS フル レイアウト (PC およびタブレット) のサポートされている最小有効解像度は 1,024 × 768 (1366 x 768以上を推奨) です</span><span class="sxs-lookup"><span data-stu-id="31acf-160">The minimum supported effective resolution for POS Full layout (PCs and tablets) is 1,024 × 768 (recommended 1366 x 768 or greater)</span></span>
- <span data-ttu-id="31acf-161">POS コンパクトレイアウト (電話および小型のタブレット) のサポートされている最小解像度は 320 x 568 (360x640 以上を推奨) です</span><span class="sxs-lookup"><span data-stu-id="31acf-161">The minimum supported effective resolution for POS Compact layout (phones and small tablets) is 320 x 568 (recommended 360x640 or greater)</span></span>
- <span data-ttu-id="31acf-162">Retail Modern POS を実行するコンピュータは以下の要件を満たす必要があります。</span><span class="sxs-lookup"><span data-stu-id="31acf-162">The computer that Retail Modern POS runs on must meet these requirements:</span></span>

    - <span data-ttu-id="31acf-163">最低でも、2 ギガヘルツ (GHz) で動作するデュアルコア プロセッサが必要です。</span><span class="sxs-lookup"><span data-stu-id="31acf-163">It must have, at a minimum, a dual-core processor that runs at no less than 2 gigahertz (GHz).</span></span>
    - <span data-ttu-id="31acf-164">最低でも、3 ギガバイト (GB) の ランダム アクセス メモリー (RAM) が必要です。</span><span class="sxs-lookup"><span data-stu-id="31acf-164">It must have, at a minimum, 3 gigabytes (GB) of random-access memory (RAM).</span></span> <span data-ttu-id="31acf-165">オフラインの SQL Server と組み合わせるときは、4 GB 以上の RAM が必要です。</span><span class="sxs-lookup"><span data-stu-id="31acf-165">When combining with SQL Server for offline, no less than 4 GB of RAM is required.</span></span>
    - <span data-ttu-id="31acf-166">インターネットにアクセスできる必要があります。</span><span class="sxs-lookup"><span data-stu-id="31acf-166">It must have internet access.</span></span>

## <a name="retail-modern-pos-for-apple-iphone-or-ipad-requirements"></a><span data-ttu-id="31acf-167">Apple iPhone または iPad 用 Retail Modern POS の要件</span><span class="sxs-lookup"><span data-stu-id="31acf-167">Retail Modern POS for Apple iPhone or iPad requirements</span></span>

- <span data-ttu-id="31acf-168">iOS 11 以降</span><span class="sxs-lookup"><span data-stu-id="31acf-168">iOS 11 or later</span></span>

## <a name="retail-modern-pos-for-android-phone-or-tablet-requirements"></a><span data-ttu-id="31acf-169">Android 電話またはタブレット用 Retail Modern POS の要件</span><span class="sxs-lookup"><span data-stu-id="31acf-169">Retail Modern POS for Android phone or tablet requirements</span></span>

- <span data-ttu-id="31acf-170">Android OS 6.0 以降</span><span class="sxs-lookup"><span data-stu-id="31acf-170">Android OS 6.0 or later</span></span>

## <a name="retail-hardware-station-requirements"></a><span data-ttu-id="31acf-171">Retail hardware station 要件</span><span class="sxs-lookup"><span data-stu-id="31acf-171">Retail hardware station requirements</span></span>

> [!NOTE]
> <span data-ttu-id="31acf-172">2018 年 10 月 1 日以降、Retail ハードウェア ステーションや 他のクライアント側コンポーネントを使用するには、.NET Framework version 4.6.1 以降をインストールする必要があります。</span><span class="sxs-lookup"><span data-stu-id="31acf-172">Starting October 1, 2018, Retail hardware station and other client-side components require that the .NET Framework version 4.6.1 or later be installed.</span></span> <span data-ttu-id="31acf-173">インストール手順については、[開発者の .NET Framework のインストール](https://msdn.microsoft.com/library/5a4x27ek(v=vs.110).aspx) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="31acf-173">For installation instructions, see [Install the .NET Framework for developers](https://msdn.microsoft.com/library/5a4x27ek(v=vs.110).aspx).</span></span>

### <a name="supported-operating-systems"></a><span data-ttu-id="31acf-174">サポートされるオペレーティング システム</span><span class="sxs-lookup"><span data-stu-id="31acf-174">Supported operating systems</span></span>

- <span data-ttu-id="31acf-175">Retail hardware station は 32 ビット アプリケーションですが、x86 と x64 アーキテクチャの両方で動作します。</span><span class="sxs-lookup"><span data-stu-id="31acf-175">Retail hardware station is a 32-bit application, but it will run on both x86 and x64 architectures.</span></span>
- <span data-ttu-id="31acf-176">Retail hardware station は、以下のオペレーティング システムでサポートされます。</span><span class="sxs-lookup"><span data-stu-id="31acf-176">Retail hardware station is supported on the following operating systems:</span></span>

    - <span data-ttu-id="31acf-177">Windows 7 Professional、Enterprise、または Ultimate エディション。</span><span class="sxs-lookup"><span data-stu-id="31acf-177">Windows 7 Professional, Enterprise, and Ultimate editions.</span></span>

        > [!NOTE]
        > <span data-ttu-id="31acf-178">Windows 7 は、Internet Explorer 11 が手動でシステムにインストールされている場合にのみサポートされます。</span><span class="sxs-lookup"><span data-stu-id="31acf-178">Windows 7 is supported only if Internet Explorer 11 is manually installed on the system.</span></span>

    - <span data-ttu-id="31acf-179">Windows 8.1 Update 1 Professional、Enterprise また Embedded エディション。</span><span class="sxs-lookup"><span data-stu-id="31acf-179">Windows 8.1 Update 1 Professional, Enterprise, and Embedded editions.</span></span>
    - <span data-ttu-id="31acf-180">Windows 10 Pro、Enterprise、Enterprise LTSB、および IOT Enterprise Edition。</span><span class="sxs-lookup"><span data-stu-id="31acf-180">Windows 10 Pro, Enterprise, Enterprise LTSB, and IOT Enterprise editions.</span></span>
    - <span data-ttu-id="31acf-181">Windows Server 2012 R2 および Windows Server 2016。</span><span class="sxs-lookup"><span data-stu-id="31acf-181">Windows Server 2012 R2 and Windows Server 2016.</span></span>
    - <span data-ttu-id="31acf-182">Windows 10 Pro がオペレーティング システムに対する更新を高度に管理できるドメイン内でない限り、Windows 10 Pro で Retail ハードウェア ステーションおよびその他の Retail のコンポーネントの使用をお勧めしません。</span><span class="sxs-lookup"><span data-stu-id="31acf-182">It is not recommended to use Retail hardware station and other Retail components on Windows 10 Pro unless within a domain as Windows 10 Pro doesn't allow for advanced management of updates to the operating system.</span></span>

### <a name="minimum-system-requirements"></a><span data-ttu-id="31acf-183">最少システム要件</span><span class="sxs-lookup"><span data-stu-id="31acf-183">Minimum system requirements</span></span>

<span data-ttu-id="31acf-184">コンピュータは、以下の項目をインストールし使用するためのすべてのシステム要件を満たす必要があります。</span><span class="sxs-lookup"><span data-stu-id="31acf-184">The computer must meet all system requirements for installing and using the following items:</span></span>

- <span data-ttu-id="31acf-185">Microsoft Internet Information Services (IIS)</span><span class="sxs-lookup"><span data-stu-id="31acf-185">Microsoft Internet Information Services (IIS)</span></span>
- <span data-ttu-id="31acf-186">サード パーティのハードウェア</span><span class="sxs-lookup"><span data-stu-id="31acf-186">Third-party hardware</span></span>

## <a name="retail-store-scale-unit-requirements"></a><span data-ttu-id="31acf-187">Retail Store Scale Unit の要件</span><span class="sxs-lookup"><span data-stu-id="31acf-187">Retail Store Scale Unit requirements</span></span>

> [!NOTE]
> <span data-ttu-id="31acf-188">2018 年 10 月 1 日以降、Retail Store Scale Unit や他のクライアント側コンポーネントを使用するには、.NET Framework version 4.6.1 以降をインストールする必要があります。</span><span class="sxs-lookup"><span data-stu-id="31acf-188">Starting October 1, 2018, Retail Store Scale Unit and other client-side components require that the .NET Framework version 4.6.1 or later be installed.</span></span> <span data-ttu-id="31acf-189">インストール手順については、[開発者の .NET Framework のインストール](https://msdn.microsoft.com/library/5a4x27ek(v=vs.110).aspx) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="31acf-189">For installation instructions, see [Install the .NET Framework for developers](https://msdn.microsoft.com/library/5a4x27ek(v=vs.110).aspx).</span></span>

<span data-ttu-id="31acf-190">以下に示す最小システム要件は、テスト シナリオでの機能へ Retail Store Scale Unit を取得するのに必要最低限であることをご確認下さい。</span><span class="sxs-lookup"><span data-stu-id="31acf-190">Take note that the minimum system requirements listed below are the bare minimum necessary to get a Retail Store Scale Unit to function in a test scenario.</span></span> <span data-ttu-id="31acf-191">以下は実際的な実稼働環境を表すものではありません。</span><span class="sxs-lookup"><span data-stu-id="31acf-191">The following is not representative of a realistic production environment.</span></span> <span data-ttu-id="31acf-192">適切なパフォーマンス テストを実行し、使用するハードウェアがユーザーのニーズを満たしているのを検証することが重要です。</span><span class="sxs-lookup"><span data-stu-id="31acf-192">It is critical to perform proper performance testing and validate that the hardware used will meet the needs of the users.</span></span>

### <a name="supported-operating-systems"></a><span data-ttu-id="31acf-193">サポートされるオペレーティング システム</span><span class="sxs-lookup"><span data-stu-id="31acf-193">Supported operating systems</span></span>

- <span data-ttu-id="31acf-194">Retail Store Scale Unit は 32 ビット アプリケーションですが、x86 と x64 アーキテクチャの両方で動作します。</span><span class="sxs-lookup"><span data-stu-id="31acf-194">Retail Store Scale Unit is a 32-bit application, but it will run on both x86 and x64 architectures.</span></span>
- <span data-ttu-id="31acf-195">Retail Store Scale Unit は、以下のオペレーティング システムでサポートされます。</span><span class="sxs-lookup"><span data-stu-id="31acf-195">Retail Store Scale Unit is supported on the following operating systems:</span></span>

    - <span data-ttu-id="31acf-196">Windows 7 Professional、Enterprise、または Ultimate エディション。</span><span class="sxs-lookup"><span data-stu-id="31acf-196">Windows 7 Professional, Enterprise, and Ultimate editions.</span></span>

        > [!NOTE]
        > <span data-ttu-id="31acf-197">Windows 7 は、Internet Explorer 11 が手動でシステムにインストールされている場合にのみサポートされます。</span><span class="sxs-lookup"><span data-stu-id="31acf-197">Windows 7 is supported only if Internet Explorer 11 is manually installed on the system.</span></span>

    - <span data-ttu-id="31acf-198">Windows 8.1 Update 1 Professional、Enterprise また Embedded エディション。</span><span class="sxs-lookup"><span data-stu-id="31acf-198">Windows 8.1 Update 1 Professional, Enterprise, and Embedded editions.</span></span>
    - <span data-ttu-id="31acf-199">Windows 10 Pro、Enterprise、Enterprise LTSB、および IOT Enterprise Edition。</span><span class="sxs-lookup"><span data-stu-id="31acf-199">Windows 10 Pro, Enterprise, Enterprise LTSB, and IOT Enterprise editions.</span></span>
    - <span data-ttu-id="31acf-200">Windows Server 2012 R2 および Windows Server 2016。</span><span class="sxs-lookup"><span data-stu-id="31acf-200">Windows Server 2012 R2 and Windows Server 2016.</span></span>
    - <span data-ttu-id="31acf-201">Windows 10 Pro がオペレーティング システムに対する更新を高度に管理できるドメイン内でない限り、Windows 10 Pro で Retail Store Scale Unit および他の Retail コンポーネントの使用をお勧めしません。</span><span class="sxs-lookup"><span data-stu-id="31acf-201">It is not recommended to use Retail Store Scale Unit and other Retail components on Windows 10 Pro unless within a domain as Windows 10 Pro doesn't allow for advanced management of updates to the operating system.</span></span>

### <a name="minimum-system-requirements"></a><span data-ttu-id="31acf-202">最少システム要件</span><span class="sxs-lookup"><span data-stu-id="31acf-202">Minimum system requirements</span></span>

> [!NOTE]
> <span data-ttu-id="31acf-203">Retail Store Scale Unit の最小システム要件を次に示します。</span><span class="sxs-lookup"><span data-stu-id="31acf-203">The following are the minimum system requirements for Retail Store Scale Unit.</span></span>  <span data-ttu-id="31acf-204">これらと推奨要件はどちらも、テストおよび基本的な機能のための最小要件です。</span><span class="sxs-lookup"><span data-stu-id="31acf-204">Both these and the recommended requirements are the minimum possible for testing and basic functionality.</span></span>  <span data-ttu-id="31acf-205">パフォーマンス テストを実行し、Retail Store Scale Unit で使用するハードウェアが期待を満していることを検証することが重要です。</span><span class="sxs-lookup"><span data-stu-id="31acf-205">It is crucial to perform performance testing and validate that the hardware used for Retail Store Scale Unit meets expectations.</span></span>

- <span data-ttu-id="31acf-206">4 GB の RAM</span><span class="sxs-lookup"><span data-stu-id="31acf-206">4 GB of RAM</span></span>
- <span data-ttu-id="31acf-207">コアごとの CPU 最大処理スピード 1.6 GHz (最少 2 コア)</span><span class="sxs-lookup"><span data-stu-id="31acf-207">1.6 GHz peak CPU speed per core (Two cores are the minimum.)</span></span>
- <span data-ttu-id="31acf-208">少なくとも 10 GB の空き領域 (チャンネル データベースが大量の領域を必要とする場合があります。）</span><span class="sxs-lookup"><span data-stu-id="31acf-208">At least 10 GB of free space (The channel database can require a large amount of space.)</span></span>

### <a name="recommended-system-requirements"></a><span data-ttu-id="31acf-209">推奨システム要件</span><span class="sxs-lookup"><span data-stu-id="31acf-209">Recommended system requirements</span></span>

- <span data-ttu-id="31acf-210">6 GB の RAM</span><span class="sxs-lookup"><span data-stu-id="31acf-210">6 GB of RAM</span></span>
- <span data-ttu-id="31acf-211">コアごとの最大処理スピード 2.4 GHz i7 (または同等のもの) (推奨 4 コア)</span><span class="sxs-lookup"><span data-stu-id="31acf-211">2.4 GHz i7 (or equivalent) peak CPU speed per core (Four cores are recommended.)</span></span>
- <span data-ttu-id="31acf-212">少なくとも 10 GB の空き領域 (チャンネル データベースが大量の領域を必要とする場合があります。）</span><span class="sxs-lookup"><span data-stu-id="31acf-212">At least 10 GB of free space (The channel database can require a large amount of space.)</span></span>

<span data-ttu-id="31acf-213">個人のハードウェア ニーズを決定する際に次の品目も考慮することは、組織の最高の利益となります。</span><span class="sxs-lookup"><span data-stu-id="31acf-213">It would be in an organization's best interest to also take the following items into consideration when determining personal hardware needs:</span></span>

- <span data-ttu-id="31acf-214">物理的ネットワーク ポートの数 (ポートが増えると 1 秒あたりのスループットが強化されます。)</span><span class="sxs-lookup"><span data-stu-id="31acf-214">Number of physical network ports (More ports enhances throughput per second.)</span></span>
- <span data-ttu-id="31acf-215">SQL Server のログ フラッシュ サイズ (これは SQL Server パフォーマンスに直接影響します。)</span><span class="sxs-lookup"><span data-stu-id="31acf-215">SQL Server log flush size (This directly impacts SQL Server performance.)</span></span>
- <span data-ttu-id="31acf-216">データの読み取りと書き込み能力 (これは SQL サーバー パフォーマンスに直接影響を与えます。)</span><span class="sxs-lookup"><span data-stu-id="31acf-216">Data read and write capabilities (This directly impacts SQL Server performance.)</span></span>
- <span data-ttu-id="31acf-217">CPU コアの数、コアごとの並行スレッドの数、およびコアあたりの速度 (これはシステムの全体的なスループットに影響します。)</span><span class="sxs-lookup"><span data-stu-id="31acf-217">Number of CPU(s) core, number of simultaneous threads per core, and speed per core (This impacts overall throughput of the system.)</span></span>
- <span data-ttu-id="31acf-218">負荷分散が必要かどうか</span><span class="sxs-lookup"><span data-stu-id="31acf-218">Whether load balancing will be required</span></span>

## <a name="connector-requirements"></a><span data-ttu-id="31acf-219">コネクタの要件</span><span class="sxs-lookup"><span data-stu-id="31acf-219">Connector requirements</span></span>

### <a name="supported-operating-systems"></a><span data-ttu-id="31acf-220">サポートされるオペレーティング システム</span><span class="sxs-lookup"><span data-stu-id="31acf-220">Supported operating systems</span></span>

- <span data-ttu-id="31acf-221">Connector for Microsoft Dynamics AX には、Async Server Connector service と Real-time service for Microsoft Dynamics AX 2012 R3 の 2 つの独立したインストーラーがあります。</span><span class="sxs-lookup"><span data-stu-id="31acf-221">The Connector for Microsoft Dynamics AX has two separate installers, one for Async Server Connector service and one for Real-time service for Microsoft Dynamics AX 2012 R3.</span></span>
- <span data-ttu-id="31acf-222">どちらのコンポーネントも 32 ビット アプリケーションですが、x86 と x64 アーキテクチャの両方で動作します。</span><span class="sxs-lookup"><span data-stu-id="31acf-222">Both components are 32-bit applications, but they will run on both x86 and x64 architectures.</span></span>
- <span data-ttu-id="31acf-223">次のオペレーティング システムでは、両方のコンポーネントがサポートされています。</span><span class="sxs-lookup"><span data-stu-id="31acf-223">Both components are supported on the following operating systems:</span></span>

    - <span data-ttu-id="31acf-224">Windows 7 Professional、Enterprise、または Ultimate エディション。</span><span class="sxs-lookup"><span data-stu-id="31acf-224">Windows 7 Professional, Enterprise, and Ultimate editions.</span></span>
    - <span data-ttu-id="31acf-225">Windows 8.1 Update 1 Professional、Enterprise また Embedded エディション。</span><span class="sxs-lookup"><span data-stu-id="31acf-225">Windows 8.1 Update 1 Professional, Enterprise, and Embedded editions.</span></span>
    - <span data-ttu-id="31acf-226">Windows 10 Pro、Enterprise、または Enterprise LTSB エディション。</span><span class="sxs-lookup"><span data-stu-id="31acf-226">Windows 10 Pro, Enterprise, and Enterprise LTSB editions.</span></span>
    - <span data-ttu-id="31acf-227">Windows Server 2012 R2 および Windows Server 2016。</span><span class="sxs-lookup"><span data-stu-id="31acf-227">Windows Server 2012 R2 and Windows Server 2016.</span></span>
    - <span data-ttu-id="31acf-228">Windows 10 Pro がオペレーティング システムに対する更新を高度に管理できるドメイン内でない限り、Windows 10 Pro で Retail のコンポーネントの使用をお勧めしません。</span><span class="sxs-lookup"><span data-stu-id="31acf-228">It is not recommended to use Retail components on Windows 10 Pro unless within a domain as Windows 10 Pro doesn't allow for advanced management of updates to the operating system.</span></span>

### <a name="minimum-system-requirements"></a><span data-ttu-id="31acf-229">最少システム要件</span><span class="sxs-lookup"><span data-stu-id="31acf-229">Minimum system requirements</span></span>

- <span data-ttu-id="31acf-230">2 GB の RAM (4 GB の RAM を推奨)。</span><span class="sxs-lookup"><span data-stu-id="31acf-230">2 GB of RAM (Four GB of RAM are recommended.)</span></span>
- <span data-ttu-id="31acf-231">コアごとの CPU 最大処理スピード 1.6 GHz (最少 2 コア)</span><span class="sxs-lookup"><span data-stu-id="31acf-231">1.6 GHz peak CPU speed per core (Two cores are the minimum.)</span></span>
- <span data-ttu-id="31acf-232">少なくとも 10 GB の空き領域 (チャンネル データベースが大量の領域を必要とする場合があります。）</span><span class="sxs-lookup"><span data-stu-id="31acf-232">At least 10 GB of free space (The channel database can require a large amount of space.)</span></span>

## <a name="requirements-for-development-on-local-vms"></a><span data-ttu-id="31acf-233">ローカル VM の開発要件</span><span class="sxs-lookup"><span data-stu-id="31acf-233">Requirements for development on local VMs</span></span>

<span data-ttu-id="31acf-234">ローカル仮想マシン (VM) の開発要件については、[オンプレミスで実行されている VM](../../dev-itpro/dev-tools/access-instances.md#vm-that-is-running-on-premises) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="31acf-234">For information about the requirements for development on local virtual machines (VMs), see [VM that is running on-premises](../../dev-itpro/dev-tools/access-instances.md#vm-that-is-running-on-premises).</span></span>

## <a name="database-collation"></a><span data-ttu-id="31acf-235">データベース照合順序</span><span class="sxs-lookup"><span data-stu-id="31acf-235">Database collation</span></span>

<span data-ttu-id="31acf-236">クラウドの Finance and Operations データベースでサポートされている唯一の照合順序は、**SQL\_Latin1\_General\_CP1\_CI\_AS** です。</span><span class="sxs-lookup"><span data-stu-id="31acf-236">The only supported collation for Finance and Operations databases in the cloud is **SQL\_Latin1\_General\_CP1\_CI\_AS**.</span></span> <span data-ttu-id="31acf-237">開発環境の SQL Server とデータベース照合順序がこれに設定されていることを確認してください。</span><span class="sxs-lookup"><span data-stu-id="31acf-237">Please ensure that your SQL Server and database collations in development environments are set to this.</span></span> <span data-ttu-id="31acf-238">また、サンドボックスに発行されたすべてのコンフィギュレーション環境にこれと同じ照合順序があることを確認します。</span><span class="sxs-lookup"><span data-stu-id="31acf-238">Also ensure that any configuration environments that are published to Sandbox have this same collation.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="31acf-239">その他のリソース</span><span class="sxs-lookup"><span data-stu-id="31acf-239">Additional resources</span></span>

[<span data-ttu-id="31acf-240">ベータ評価版の入手</span><span class="sxs-lookup"><span data-stu-id="31acf-240">Get an evaluation copy</span></span>](../../dev-itpro/dev-tools/get-evaluation-copy.md)
