---
title: "クラウド配置のシステム要件"
description: "このトピックでは、クラウド配置における 現在のバージョン Microsoft Dynamics 365 for Finance and Operations、Enterprise Edition のシステム要件を一覧表示します。"
author: sericks007
manager: AnnBe
ms.date: 08/02/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Application User, Developer, IT Pro
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.custom: 55651
ms.assetid: e564d51d-42d3-47c5-b388-93b8219c692a
ms.search.region: Global
ms.author: sericks
ms.search.validFrom: 2016-08-30
ms.dyn365.ops.version: Platform update 8
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 83637b4b2ccc01950e68569b3b8bee1a7cd69855
ms.contentlocale: ja-jp
ms.lasthandoff: 11/03/2017

---

# <a name="system-requirements-for-cloud-deployments"></a><span data-ttu-id="d45e0-103">クラウド配置のシステム要件</span><span class="sxs-lookup"><span data-stu-id="d45e0-103">System requirements for cloud deployments</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="d45e0-104">このトピックでは、クラウド配置における 現在のバージョン Microsoft Dynamics 365 for Finance and Operations、Enterprise Edition のシステム要件を一覧表示します。</span><span class="sxs-lookup"><span data-stu-id="d45e0-104">This topic lists the system requirements for the current version of Microsoft Dynamics 365 for Finance and Operations, Enterprise edition, for cloud deployments.</span></span> <span data-ttu-id="d45e0-105">Finance and Operations をインストールする前に、このステップが適切な場合、作業しているシステムがネットワーク、ハードウェア、およびソフトウェアの最小要件を満たしているか、または超えているかを検証します。</span><span class="sxs-lookup"><span data-stu-id="d45e0-105">Before you install Finance and Operations, when this step is appropriate, verify that the system that you're working with meets or exceeds the minimum network, hardware, and software requirements.</span></span>

## <a name="supported-web-browsers"></a><span data-ttu-id="d45e0-106">サポートされている Web ブラウザー</span><span class="sxs-lookup"><span data-stu-id="d45e0-106">Supported web browsers</span></span>
<span data-ttu-id="d45e0-107">Web アプリケーションは、指定されたオペレーティング システムで実行される次のすべての Web ブラウザで実行できます。</span><span class="sxs-lookup"><span data-stu-id="d45e0-107">The web application can run in any of the following web browsers that run on the specified operating systems:</span></span>

-   <span data-ttu-id="d45e0-108">Windows 10 の Microsoft Edge (公開されている最新のバージョン)</span><span class="sxs-lookup"><span data-stu-id="d45e0-108">Microsoft Edge (latest publicly available version) on Windows 10</span></span>
-   <span data-ttu-id="d45e0-109">Windows 10、Windows 8.1、または Windows 7 の Internet Explorer 11</span><span class="sxs-lookup"><span data-stu-id="d45e0-109">Internet Explorer 11 on Windows 10, Windows 8.1, or Windows 7</span></span>
-   <span data-ttu-id="d45e0-110">Windows 10、Windows 8.1、Windows 8、Windows 7、または Google Nexus 10 タブレットの Google Chrome (公開されている最新のバージョン)</span><span class="sxs-lookup"><span data-stu-id="d45e0-110">Google Chrome (latest publicly available version) on Windows 10, Windows 8.1, Windows 8, Windows 7, or Google Nexus 10 tablet</span></span>
-   <span data-ttu-id="d45e0-111">Mac OS X 10.10 (Yosemite)、 10.11 (El Capitan) または 10.12 (Sierra)、または Apple iPad の Apple Safari (公開されている最新のバージョン)</span><span class="sxs-lookup"><span data-stu-id="d45e0-111">Apple Safari (latest publicly available version) on Mac OS X 10.10 (Yosemite), 10.11 (El Capitan) or 10.12 (Sierra), or Apple iPad</span></span>

<span data-ttu-id="d45e0-112">各 Web ブラウザの最新版を検索するには、ソフトウェア メーカーの Web サイトに移動します。</span><span class="sxs-lookup"><span data-stu-id="d45e0-112">To find the latest release for each web browser, go to the software manufacturer’s website.</span></span> 

> [!NOTE]
> -   <span data-ttu-id="d45e0-113">Task Recorder からスクリーンショットのキャプチャを有効にし、生成された Microsoft Word ドキュメントに含めるには、プレリリース版の Chrome 拡張機能をインストールする必要があります。</span><span class="sxs-lookup"><span data-stu-id="d45e0-113">You must install a pre-release Chrome extension to enable Task Recorder to capture screenshots and include them in Microsoft Word documents that are generated.</span></span> <!---For instructions about how to install the extension, see [Screenshot Extension setup](../../dev-itpro/user-interface/task-recorder).-->
> -   <span data-ttu-id="d45e0-114">ワークフロー エディターは ClickOnce アプリケーションとして起動されます。</span><span class="sxs-lookup"><span data-stu-id="d45e0-114">The Workflow Editor is started as a ClickOnce application.</span></span> <span data-ttu-id="d45e0-115">Microsoft Edge と Internet Explorer (Microsoft Windows のサポートされているバージョン) のみが、ClickOnce アプリケーションをサポートします。</span><span class="sxs-lookup"><span data-stu-id="d45e0-115">Only Microsoft Edge and Internet Explorer (on a supported version of Microsoft Windows) support ClickOnce applications.</span></span> <span data-ttu-id="d45e0-116">ワークフロー エディター ClickOnce アプリケーションには、64 ビットの互換性のあるオペレーティング システムが必要です。</span><span class="sxs-lookup"><span data-stu-id="d45e0-116">The Workflow Editor ClickOnce application requires a 64-bit-compatible operating system.</span></span>
> -   <span data-ttu-id="d45e0-117">財務報告のレポート デザイナーは、ClickOnce アプリケーションとして起動されます。</span><span class="sxs-lookup"><span data-stu-id="d45e0-117">The Report Designer for Financial reporting is started as a ClickOnce application.</span></span> <span data-ttu-id="d45e0-118">それには 64 ビットの互換性のあるオペレーティング システムが必要です。</span><span class="sxs-lookup"><span data-stu-id="d45e0-118">It requires a 64-bit-compatible operating system.</span></span> <span data-ttu-id="d45e0-119">Chrome を使用している場合、レポート デザイナーのクライアントをダウンロードするために ClickOnce 拡張機能をインストールする必要があります。</span><span class="sxs-lookup"><span data-stu-id="d45e0-119">If you’re using Chrome, you must install a ClickOnce extension to download the Report Designer client.</span></span> <span data-ttu-id="d45e0-120">匿名モードで Chrome を使用する場合、ClickOnce の拡張機能が匿名モードに対しても有効化されていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="d45e0-120">If you use Chrome in Incognito mode, make sure that the ClickOnce extension is also enabled for Incognito mode.</span></span>
> -   <span data-ttu-id="d45e0-121">PDF ファイルをプレビューするには、Windows 10 の Microsoft Edge (公開されている最新のバージョン)、もしくは Windows 10、Windows 8.1、Windows 8、Windows 7、または Google Nexus 10 タブレットの Google Chrome (公開されている最新のバージョン) などの最新のブラウザを使用することをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="d45e0-121">To preview PDF files, we recommend that you use browsers such as Microsoft Edge (latest publicly available version) on Windows 10, or Google Chrome (latest publicly available version) on Windows 10, Windows 8.1, Windows 8, Windows 7, or Google Nexus 10 tablet.</span></span>

### <a name="supported-web-browsers-for-retail-cloud-pos"></a><span data-ttu-id="d45e0-122">Retail Cloud POS でサポートされている Web ブラウザー</span><span class="sxs-lookup"><span data-stu-id="d45e0-122">Supported web browsers for Retail Cloud POS</span></span>

<span data-ttu-id="d45e0-123">Retail Cloud POS は、指定されたオペレーティング システムで実行される次のすべての Web ブラウザで実行できます。</span><span class="sxs-lookup"><span data-stu-id="d45e0-123">Retail Cloud POS can run in any of the following web browsers that run on the specified operating systems:</span></span>

-   <span data-ttu-id="d45e0-124">Windows 10 の Microsoft Edge (公開されている最新のバージョン)</span><span class="sxs-lookup"><span data-stu-id="d45e0-124">Microsoft Edge (latest publicly available version) on Windows 10</span></span>
-   <span data-ttu-id="d45e0-125">Windows 10、Windows 8.1、または Windows 7 の Internet Explorer 11</span><span class="sxs-lookup"><span data-stu-id="d45e0-125">Internet Explorer 11 on Windows 10, Windows 8.1, or Windows 7</span></span>
-   <span data-ttu-id="d45e0-126">Windows 10、Windows 8.1、または Windows 7 の Chrome (公開されている最新のバージョン)</span><span class="sxs-lookup"><span data-stu-id="d45e0-126">Chrome (latest publicly available version) on Windows 10, Windows 8.1, or Windows 7</span></span>

## <a name="network-requirements"></a><span data-ttu-id="d45e0-127">ネットワーク要件</span><span class="sxs-lookup"><span data-stu-id="d45e0-127">Network requirements</span></span>
-   <span data-ttu-id="d45e0-128">Finance and Operations は、待機時間が 250 ～ 300 ミリ秒 (ms) 以下のネットワーク用に設計されています。</span><span class="sxs-lookup"><span data-stu-id="d45e0-128">Finance and Operations is designed for networks that have a latency of 250–300 milliseconds (ms) or less.</span></span> <span data-ttu-id="d45e0-129">これは、ブラウザー クライアントから Finance and Operations をホストする Microsoft Azure データセンターまでの待機時間です。</span><span class="sxs-lookup"><span data-stu-id="d45e0-129">This latency is the latency from a browser client to the Microsoft Azure datacenter that hosts Finance and Operations.</span></span> <span data-ttu-id="d45e0-130"><http://www.azurespeed.com> でネットワーク待機時間をテストすることをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="d45e0-130">We recommend that you test network latency at <http://www.azurespeed.com>.</span></span>
-   <span data-ttu-id="d45e0-131">Finance and Operations の帯域幅の要件はシナリオによって異なります。</span><span class="sxs-lookup"><span data-stu-id="d45e0-131">Bandwidth requirements for Finance and Operations depend on your scenario.</span></span> <span data-ttu-id="d45e0-132">最も一般的なシナリオでは、毎秒 50 キロバイト (KBps) 以上の帯域幅が必要です。</span><span class="sxs-lookup"><span data-stu-id="d45e0-132">Most typical scenarios require a bandwidth of more than 50 kilobytes per second (KBps).</span></span> <span data-ttu-id="d45e0-133">ただし、ワークスペースや大がかりなカスタマイズを含む高度な伝送データ要件があるシナリオには、帯域幅を増やすことを勧めます。</span><span class="sxs-lookup"><span data-stu-id="d45e0-133">However, we recommend more bandwidth for scenarios that have high payload requirements, such as scenarios that involve workspaces or extensive customization.</span></span>

<span data-ttu-id="d45e0-134">一般に、Finance and Operations は、インターネットに最適化されます。</span><span class="sxs-lookup"><span data-stu-id="d45e0-134">In general, Finance and Operations is optimized for the internet.</span></span> <span data-ttu-id="d45e0-135">ブラウザー クライアントから Azure データセンターへのラウンド トリップの数は非常に小さく、全伝送データは圧縮されます。</span><span class="sxs-lookup"><span data-stu-id="d45e0-135">The number of round trips from a browser client to the Azure datacenter is very small, and the whole payload is compressed.</span></span> 

> [!WARNING]
> <span data-ttu-id="d45e0-136">ユーザー数に帯域幅要件の最小値を掛けて、クライアントの場所からの帯域幅要件を計算しないでください。</span><span class="sxs-lookup"><span data-stu-id="d45e0-136">Don't calculate bandwidth requirements from a client location by multiplying the number of users by the minimum bandwidth requirements.</span></span> <span data-ttu-id="d45e0-137">特定の場所の同時使用は非常に計算が困難です。</span><span class="sxs-lookup"><span data-stu-id="d45e0-137">The concurrent usage of a given location is very difficult to calculate.</span></span> <span data-ttu-id="d45e0-138">帯域幅の要件について懸念する顧客は、Finance and Operations のプレビュー バージョンを使用するべきです。</span><span class="sxs-lookup"><span data-stu-id="d45e0-138">Customers who are concerned about bandwidth requirements should use a preview version of Finance and Operations.</span></span>

## <a name="net-framework-requirements"></a><span data-ttu-id="d45e0-139">.NET Framework 要件</span><span class="sxs-lookup"><span data-stu-id="d45e0-139">.NET Framework requirements</span></span>
<span data-ttu-id="d45e0-140">Finance and Operations では、ドキュメント回覧エージェントなどのすべての ClickOnce アプリケーション用として、Microsoft NET Framework バージョン 4.6.2 が必要です。</span><span class="sxs-lookup"><span data-stu-id="d45e0-140">Finance and Operations requires the Microsoft .NET Framework version 4.6.2 for all ClickOnce applications, such as the document routing agent.</span></span> <span data-ttu-id="d45e0-141">インストール手順については、[.NET Framework のインストール](https://msdn.microsoft.com/en-us/library/5a4x27ek(v=vs.110).aspx) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="d45e0-141">For installation instructions, see [Installing the .NET Framework](https://msdn.microsoft.com/en-us/library/5a4x27ek(v=vs.110).aspx).</span></span>

## <a name="supported-microsoft-office-applications"></a><span data-ttu-id="d45e0-142">サポートされている Microsoft Office アプリケーション</span><span class="sxs-lookup"><span data-stu-id="d45e0-142">Supported Microsoft Office applications</span></span>
<span data-ttu-id="d45e0-143">次の Microsoft Office アプリケーションは、Finance and Operations のクラウドおよびオンプレミス配置でサポートされています。</span><span class="sxs-lookup"><span data-stu-id="d45e0-143">The following Microsoft Office applications are supported in cloud and on-premises deployments of Finance and Operations:</span></span>

-   <span data-ttu-id="d45e0-144">Microsoft Excel と Word のアドインを実行するには、Windows か Mac 用の Microsoft Office 2016 をインストールしておく必要があります。</span><span class="sxs-lookup"><span data-stu-id="d45e0-144">To run the Microsoft Excel and Word add-ins, you must have Microsoft Office 2016 for Windows or Mac installed.</span></span> <span data-ttu-id="d45e0-145">バージョン要求の詳細については、[Office 統合トラブルシューティング](../../dev-itpro/office-integration/office-integration-troubleshooting.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="d45e0-145">For more information about version requirements, see [Office integration troubleshooting](../../dev-itpro/office-integration/office-integration-troubleshooting.md).</span></span>
-   <span data-ttu-id="d45e0-146">[Excel にエクスポート] または [Word にエクスポート] 機能によって生成されたドキュメントを表示するには、Microsoft Office 2007 以降をインストールしておく必要があります。</span><span class="sxs-lookup"><span data-stu-id="d45e0-146">To view documents that are generated by the Export to Excel or Export to Word functionality, you must have Microsoft Office 2007 or later installed.</span></span>

## <a name="retail-modern-pos-requirements"></a><span data-ttu-id="d45e0-147">Retail Modern POS 要件</span><span class="sxs-lookup"><span data-stu-id="d45e0-147">Retail Modern POS requirements</span></span>

> [!NOTE]
> <span data-ttu-id="d45e0-148">Retai Modern POS でオフライン データベースを使う場合、コンピューターは Microsoft SQL Server のすべてのシステム要件を満たす必要があります。</span><span class="sxs-lookup"><span data-stu-id="d45e0-148">If Retail Modern POS will use an offline database, the computer must meet all system requirements for Microsoft SQL Server.</span></span> <span data-ttu-id="d45e0-149">Retail Modern POS オフライン データベースは、Service Pack 3 またはそれ以降と Microsoft SQL Server 2012、Service Pack 2 またはそれ以降と Microsoft SQL Server 2014 、そして Microsoft SQL Server 2016 で動作します。</span><span class="sxs-lookup"><span data-stu-id="d45e0-149">A Retail Modern POS offline database will work on Microsoft SQL Server 2012 with Service Pack 3 or later, Microsoft SQL Server 2014 with Service Pack 2 or later, and Microsoft SQL Server 2016.</span></span> <span data-ttu-id="d45e0-150">常に利用可能な最新のバージョンを使用し、すべての最新サービス パックをインストールすることをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="d45e0-150">We recommend that you always use the latest version that is available, and that you install all the latest service packs.</span></span>

### <a name="supported-operating-systems"></a><span data-ttu-id="d45e0-151">サポートされるオペレーティング システム</span><span class="sxs-lookup"><span data-stu-id="d45e0-151">Supported operating systems</span></span>

-   <span data-ttu-id="d45e0-152">Retail Modern POS は 32 ビット アプリケーションですが、x86 と x64 アーキテクチャの両方で動作します。</span><span class="sxs-lookup"><span data-stu-id="d45e0-152">Retail Modern POS is a 32-bit application, but it will run on both x86 and x64 architectures.</span></span>
-   <span data-ttu-id="d45e0-153">Retail Modern POS は Windows 10 Pro、Enterprise、また Enterprise Long Term Servicing Branch (LTSB) エディションでのみサポートされています。</span><span class="sxs-lookup"><span data-stu-id="d45e0-153">Retail Modern POS is supported only on Windows 10 Pro, Enterprise, and Enterprise Long Term Servicing Branch (LTSB) editions.</span></span>

### <a name="minimum-system-requirements"></a><span data-ttu-id="d45e0-154">最少システム要件</span><span class="sxs-lookup"><span data-stu-id="d45e0-154">Minimum system requirements</span></span>

-   <span data-ttu-id="d45e0-155">最少のサポートされている解像度は 1280 × 1024 です。</span><span class="sxs-lookup"><span data-stu-id="d45e0-155">The minimum supported resolution is 1,280 × 1,024.</span></span>
-   <span data-ttu-id="d45e0-156">Retail Modern POS を実行するコンピュータは以下の要件を満たす必要があります。</span><span class="sxs-lookup"><span data-stu-id="d45e0-156">The computer that Retail Modern POS runs on must meet these requirements:</span></span>

    -   <span data-ttu-id="d45e0-157">最低でも、2 ギガヘルツ (GHz) で動作するデュアルコア プロセッサが必要です。</span><span class="sxs-lookup"><span data-stu-id="d45e0-157">It must have, at a minimum, a dual-core processor that runs at no less than 2 gigahertz (GHz).</span></span>
    -   <span data-ttu-id="d45e0-158">最低でも、3 ギガバイト (GB) の ランダム アクセス メモリー (RAM) が必要です。</span><span class="sxs-lookup"><span data-stu-id="d45e0-158">It must have, at a minimum, 3 gigabytes (GB) of random-access memory (RAM).</span></span>
    -   <span data-ttu-id="d45e0-159">インターネットにアクセスできる必要があります。</span><span class="sxs-lookup"><span data-stu-id="d45e0-159">It must have internet access.</span></span>

## <a name="retail-hardware-station-requirements"></a><span data-ttu-id="d45e0-160">Retail hardware station 要件</span><span class="sxs-lookup"><span data-stu-id="d45e0-160">Retail hardware station requirements</span></span>
### <a name="supported-operating-systems"></a><span data-ttu-id="d45e0-161">サポートされるオペレーティング システム</span><span class="sxs-lookup"><span data-stu-id="d45e0-161">Supported operating systems</span></span>

-   <span data-ttu-id="d45e0-162">Retail hardware station は 32 ビット アプリケーションですが、x86 と x64 アーキテクチャの両方で動作します。</span><span class="sxs-lookup"><span data-stu-id="d45e0-162">Retail hardware station is a 32-bit application, but it will run on both x86 and x64 architectures.</span></span>
-   <span data-ttu-id="d45e0-163">Retail hardware station は、以下のオペレーティング システムでサポートされます。</span><span class="sxs-lookup"><span data-stu-id="d45e0-163">Retail hardware station is supported on the following operating systems:</span></span>

    -   <span data-ttu-id="d45e0-164">Windows 7 Professional、Enterprise、また Ultimate エディション</span><span class="sxs-lookup"><span data-stu-id="d45e0-164">Windows 7 Professional, Enterprise, and Ultimate editions</span></span> 
    
        > [!NOTE]
        > <span data-ttu-id="d45e0-165">Windows 7 は、Internet Explorer 11 が手動でシステムにインストールされている場合にのみサポートされます。</span><span class="sxs-lookup"><span data-stu-id="d45e0-165">Windows 7 is supported only if Internet Explorer 11 is manually installed on the system.</span></span>

    -   <span data-ttu-id="d45e0-166">Windows 8.1 Update 1 Professional、Enterprise また Embedded エディション</span><span class="sxs-lookup"><span data-stu-id="d45e0-166">Windows 8.1 Update 1 Professional, Enterprise, and Embedded editions</span></span>
    -   <span data-ttu-id="d45e0-167">Windows 10 Pro、Enterprise、また Enterprise LTSB エディション</span><span class="sxs-lookup"><span data-stu-id="d45e0-167">Windows 10 Pro, Enterprise, and Enterprise LTSB editions</span></span>

### <a name="minimum-system-requirements"></a><span data-ttu-id="d45e0-168">最少システム要件</span><span class="sxs-lookup"><span data-stu-id="d45e0-168">Minimum system requirements</span></span>

<span data-ttu-id="d45e0-169">コンピュータは、以下の項目をインストールし使用するためのすべてのシステム要件を満たす必要があります。</span><span class="sxs-lookup"><span data-stu-id="d45e0-169">The computer must meet all system requirements for installing and using the following items:</span></span>

-   <span data-ttu-id="d45e0-170">インターネット インフォメーション サービス (IIS)</span><span class="sxs-lookup"><span data-stu-id="d45e0-170">Internet Information Services (IIS)</span></span>
-   <span data-ttu-id="d45e0-171">サード パーティのハードウェア</span><span class="sxs-lookup"><span data-stu-id="d45e0-171">Third-party hardware</span></span>

## <a name="retail-store-scale-unit-requirements"></a><span data-ttu-id="d45e0-172">Retail Store スケール ユニット要件</span><span class="sxs-lookup"><span data-stu-id="d45e0-172">Retail Store Scale Unit requirements</span></span>
### <a name="supported-operating-systems"></a><span data-ttu-id="d45e0-173">サポートされるオペレーティング システム</span><span class="sxs-lookup"><span data-stu-id="d45e0-173">Supported operating systems</span></span>

-   <span data-ttu-id="d45e0-174">Retail Store スケール ユニットは 32 ビット アプリケーションですが、x86 と x64 アーキテクチャの両方で動作します。</span><span class="sxs-lookup"><span data-stu-id="d45e0-174">Retail Store Scale Unit is a 32-bit application, but it will run on both x86 and x64 architectures.</span></span>
-   <span data-ttu-id="d45e0-175">Retail Store スケール ユニットは、以下のオペレーティング システムでサポートされます。</span><span class="sxs-lookup"><span data-stu-id="d45e0-175">Retail Store Scale Unit is supported on the following operating systems:</span></span>

    -   <span data-ttu-id="d45e0-176">Windows 7 Professional、Enterprise、また Ultimate エディション</span><span class="sxs-lookup"><span data-stu-id="d45e0-176">Windows 7 Professional, Enterprise, and Ultimate editions</span></span>
    -   <span data-ttu-id="d45e0-177">Windows 8.1 Update 1 Professional、Enterprise また Embedded エディション</span><span class="sxs-lookup"><span data-stu-id="d45e0-177">Windows 8.1 Update 1 Professional, Enterprise, and Embedded editions</span></span>
    -   <span data-ttu-id="d45e0-178">Windows 10 Pro、Enterprise、また Enterprise LTSB エディション</span><span class="sxs-lookup"><span data-stu-id="d45e0-178">Windows 10 Pro, Enterprise, and Enterprise LTSB editions</span></span>

### <a name="minimum-system-requirements"></a><span data-ttu-id="d45e0-179">最少システム要件</span><span class="sxs-lookup"><span data-stu-id="d45e0-179">Minimum system requirements</span></span>

-   <span data-ttu-id="d45e0-180">4 GB の RAM</span><span class="sxs-lookup"><span data-stu-id="d45e0-180">4 GB of RAM</span></span>
-   <span data-ttu-id="d45e0-181">コアごとの CPU 最大処理スピード 1.6 GHz (最少 2 コア)</span><span class="sxs-lookup"><span data-stu-id="d45e0-181">1.6 GHz peak CPU speed per core (Two cores are the minimum.)</span></span>
-   <span data-ttu-id="d45e0-182">少なくとも 10 GB の空き領域 (チャンネル データベースが大量の領域を必要とする場合があります。）</span><span class="sxs-lookup"><span data-stu-id="d45e0-182">At least 10 GB of free space (The channel database can require a large amount of space.)</span></span>

### <a name="recommended-system-requirements"></a><span data-ttu-id="d45e0-183">推奨システム要件</span><span class="sxs-lookup"><span data-stu-id="d45e0-183">Recommended system requirements</span></span>

-   <span data-ttu-id="d45e0-184">6 GB の RAM</span><span class="sxs-lookup"><span data-stu-id="d45e0-184">6 GB of RAM</span></span>
-   <span data-ttu-id="d45e0-185">コアごとの最大処理スピード 2.4 GHz i7 (または同等のもの) (推奨 4 コア)</span><span class="sxs-lookup"><span data-stu-id="d45e0-185">2.4 GHz i7 (or equivalent) peak CPU speed per core (Four cores are recommended.)</span></span>
-   <span data-ttu-id="d45e0-186">少なくとも 10 GB の空き領域 (チャンネル データベースが大量の領域を必要とする場合があります。）</span><span class="sxs-lookup"><span data-stu-id="d45e0-186">At least 10 GB of free space (The channel database can require a large amount of space.)</span></span>

## <a name="connector-requirements"></a><span data-ttu-id="d45e0-187">コネクタの要件</span><span class="sxs-lookup"><span data-stu-id="d45e0-187">Connector requirements</span></span>
### <a name="supported-operating-systems"></a><span data-ttu-id="d45e0-188">サポートされるオペレーティング システム</span><span class="sxs-lookup"><span data-stu-id="d45e0-188">Supported operating systems</span></span>

-   <span data-ttu-id="d45e0-189">Connector for Microsoft Dynamics AX には、Async Server Connector service と Real-time service for Dynamics AX 2012 R3 の 2 つの独立したインストーラーがあります。</span><span class="sxs-lookup"><span data-stu-id="d45e0-189">The Connector for Microsoft Dynamics AX has two separate installers, one for Async Server Connector service and one for Real-time service for Dynamics AX 2012 R3.</span></span>
-   <span data-ttu-id="d45e0-190">どちらのコンポーネントも 32 ビット アプリケーションですが、x86 と x64 アーキテクチャの両方で動作します。</span><span class="sxs-lookup"><span data-stu-id="d45e0-190">Both components are 32-bit applications, but they will run on both x86 and x64 architectures.</span></span>
-   <span data-ttu-id="d45e0-191">次のオペレーティング システムでは、両方のコンポーネントがサポートされています。</span><span class="sxs-lookup"><span data-stu-id="d45e0-191">Both components are supported on the following operating systems:</span></span>

    -   <span data-ttu-id="d45e0-192">Windows 7 Professional、Enterprise、また Ultimate エディション</span><span class="sxs-lookup"><span data-stu-id="d45e0-192">Windows 7 Professional, Enterprise, and Ultimate editions</span></span>
    -   <span data-ttu-id="d45e0-193">Windows 8.1 Update 1 Professional、Enterprise また Embedded エディション</span><span class="sxs-lookup"><span data-stu-id="d45e0-193">Windows 8.1 Update 1 Professional, Enterprise, and Embedded editions</span></span>
    -   <span data-ttu-id="d45e0-194">Windows 10 Pro、Enterprise、また Enterprise LTSB エディション</span><span class="sxs-lookup"><span data-stu-id="d45e0-194">Windows 10 Pro, Enterprise, and Enterprise LTSB editions</span></span>
    -   <span data-ttu-id="d45e0-195">Microsoft Windows Server 2012 R2 と Microsoft Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="d45e0-195">Microsoft Windows Server 2012 R2 and Microsoft Windows Server 2016</span></span>

### <a name="minimum-system-requirements"></a><span data-ttu-id="d45e0-196">最少システム要件</span><span class="sxs-lookup"><span data-stu-id="d45e0-196">Minimum system requirements</span></span>
-   <span data-ttu-id="d45e0-197">2 GB の RAM (4 GB の RAM を推奨)。</span><span class="sxs-lookup"><span data-stu-id="d45e0-197">2 GB of RAM (4 GB of RAM are recommended.)</span></span>
-   <span data-ttu-id="d45e0-198">コアごとの CPU 最大処理スピード 1.6 GHz (最少 2 コア)</span><span class="sxs-lookup"><span data-stu-id="d45e0-198">1.6 GHz peak CPU speed per core (Two cores are the minimum.)</span></span>
-   <span data-ttu-id="d45e0-199">少なくとも 10 GB の空き領域 (チャンネル データベースが大量の領域を必要とする場合があります。）</span><span class="sxs-lookup"><span data-stu-id="d45e0-199">At least 10 GB of free space (The channel database can require a large amount of space.)</span></span>

## <a name="requirements-for-development-on-local-vms"></a><span data-ttu-id="d45e0-200">ローカル VM の開発要件</span><span class="sxs-lookup"><span data-stu-id="d45e0-200">Requirements for development on local VMs</span></span>
<span data-ttu-id="d45e0-201">ローカル仮想マシン (VM) の開発要件については、[オンプレミス実行の VM](../../dev-itpro/dev-tools/access-instances.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="d45e0-201">For information about the requirements for development on local virtual machines (VMs), see [VM running on-premises](../../dev-itpro/dev-tools/access-instances.md).</span></span>


## <a name="see-also"></a><span data-ttu-id="d45e0-202">参照</span><span class="sxs-lookup"><span data-stu-id="d45e0-202">See also</span></span>

[<span data-ttu-id="d45e0-203">Dynamics 365 for Finance and Operations, Enterprise Edition の評価版を取得</span><span class="sxs-lookup"><span data-stu-id="d45e0-203">Get an evaluation copy of Dynamics 365 for Finance and Operations, Enterprise edition</span></span>](../../dev-itpro/dev-tools/get-evaluation-copy.md)

