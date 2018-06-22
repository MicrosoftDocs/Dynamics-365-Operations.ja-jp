---
title: "クラウド配置のシステム要件"
description: "このトピックでは、現在のバージョンの Microsoft Dynamics 365 for Finance and Operations におけるクラウド展開のシステム要件を一覧表示します。"
author: sericks007
manager: AnnBe
ms.date: 03/27/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Developer, IT Pro
ms.reviewer: sericks
ms.search.scope: Operations
ms.custom: 55651
ms.assetid: e564d51d-42d3-47c5-b388-93b8219c692a
ms.search.region: Global
ms.author: sericks
ms.search.validFrom: 2016-08-30
ms.dyn365.ops.version: Platform update 8
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: 994ad641536dc7a2100b9662bc8d76248a8c0a41
ms.contentlocale: ja-jp
ms.lasthandoff: 05/08/2018

---

# <a name="system-requirements-for-cloud-deployments"></a><span data-ttu-id="d3551-103">クラウド配置のシステム要件</span><span class="sxs-lookup"><span data-stu-id="d3551-103">System requirements for cloud deployments</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="d3551-104">このトピックでは、現在のバージョンの Microsoft Dynamics 365 for Finance and Operations におけるクラウド展開のシステム要件を一覧表示します。</span><span class="sxs-lookup"><span data-stu-id="d3551-104">This topic lists the system requirements for the current version of Microsoft Dynamics 365 for Finance and Operations for cloud deployments.</span></span> <span data-ttu-id="d3551-105">Finance and Operations をインストールする前に、このステップが適切な場合、作業しているシステムがネットワーク、ハードウェア、およびソフトウェアの最小要件を満たしているか、または超えているかを検証する必要があります。</span><span class="sxs-lookup"><span data-stu-id="d3551-105">If this step is appropriate, before you install Finance and Operations, you should verify that the system that you're working with meets or exceeds the minimum network, hardware, and software requirements.</span></span>

## <a name="supported-web-browsers"></a><span data-ttu-id="d3551-106">サポートされている Web ブラウザー</span><span class="sxs-lookup"><span data-stu-id="d3551-106">Supported web browsers</span></span>

<span data-ttu-id="d3551-107">Web アプリケーションは、指定されたオペレーティング システムで実行される次のすべての Web ブラウザで実行できます。</span><span class="sxs-lookup"><span data-stu-id="d3551-107">The web application can run in any of the following web browsers that run on the specified operating systems:</span></span>

- <span data-ttu-id="d3551-108">Windows 10 の Microsoft Edge (公開されている最新のバージョン)</span><span class="sxs-lookup"><span data-stu-id="d3551-108">Microsoft Edge (latest publicly available version) on Windows 10</span></span>
- <span data-ttu-id="d3551-109">Windows 10、Windows 8.1、または Windows 7 の Internet Explorer 11</span><span class="sxs-lookup"><span data-stu-id="d3551-109">Internet Explorer 11 on Windows 10, Windows 8.1, or Windows 7</span></span>
- <span data-ttu-id="d3551-110">Windows 10、Windows 8.1、Windows 8、Windows 7、または Google Nexus 10 タブレットの Google Chrome (公開されている最新のバージョン)</span><span class="sxs-lookup"><span data-stu-id="d3551-110">Google Chrome (latest publicly available version) on Windows 10, Windows 8.1, Windows 8, Windows 7, or Google Nexus 10 tablet</span></span>
- <span data-ttu-id="d3551-111">Mac OS X 10.10 (Yosemite)、10.11 (El Capitan)、または 10.12 (Sierra)、または Apple iPad の Apple Safari (公開されている最新のバージョン)</span><span class="sxs-lookup"><span data-stu-id="d3551-111">Apple Safari (latest publicly available version) on Mac OS X 10.10 (Yosemite), 10.11 (El Capitan), or 10.12 (Sierra), or Apple iPad</span></span>

<span data-ttu-id="d3551-112">各 Web ブラウザーの最新版を検索するには、ソフトウェア メーカーの Web サイトに移動します。</span><span class="sxs-lookup"><span data-stu-id="d3551-112">To find the latest release for each web browser, go to the software manufacturer's website.</span></span>

> [!NOTE]
> - <span data-ttu-id="d3551-113">タスク レコーダーがスクリーンショットをキャプチャし、生成された Microsoft Word ドキュメントにそれらを含めるには、プレリリース版の Chrome 拡張機能をインストールする必要があります。</span><span class="sxs-lookup"><span data-stu-id="d3551-113">To enable Task Recorder to capture screenshots and include them in Microsoft Word documents that are generated, you must install a pre-release Chrome extension.</span></span> <!---For instructions about how to install the extension, see [Screenshot Extension setup](../../dev-itpro/user-interface/task-recorder).-->
> - <span data-ttu-id="d3551-114">ワークフロー エディターは ClickOnce アプリケーションとして起動されます。</span><span class="sxs-lookup"><span data-stu-id="d3551-114">The Workflow Editor is started as a ClickOnce application.</span></span> <span data-ttu-id="d3551-115">Microsoft Edge と Internet Explorer (Microsoft Windows のサポートされているバージョン) のみが、ClickOnce アプリケーションをサポートします。</span><span class="sxs-lookup"><span data-stu-id="d3551-115">Only Microsoft Edge and Internet Explorer (on a supported version of Microsoft Windows) support ClickOnce applications.</span></span> <span data-ttu-id="d3551-116">ワークフロー エディター ClickOnce アプリケーションには、64 ビットの互換性のあるオペレーティング システムが必要です。</span><span class="sxs-lookup"><span data-stu-id="d3551-116">The Workflow Editor ClickOnce application requires a 64-bit-compatible operating system.</span></span>
> - <span data-ttu-id="d3551-117">財務報告のレポート デザイナーは、ClickOnce アプリケーションとして起動されます。</span><span class="sxs-lookup"><span data-stu-id="d3551-117">The Report Designer for Financial reporting is started as a ClickOnce application.</span></span> <span data-ttu-id="d3551-118">それには 64 ビットの互換性のあるオペレーティング システムが必要です。</span><span class="sxs-lookup"><span data-stu-id="d3551-118">It requires a 64-bit-compatible operating system.</span></span> <span data-ttu-id="d3551-119">Chrome を使用している場合、レポート デザイナーのクライアントをダウンロードするために ClickOnce 拡張機能をインストールする必要があります。</span><span class="sxs-lookup"><span data-stu-id="d3551-119">If you're using Chrome, you must install a ClickOnce extension to download the Report Designer client.</span></span> <span data-ttu-id="d3551-120">匿名モードで Chrome を使用する場合、ClickOnce の拡張機能が匿名モードに対しても有効化されていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="d3551-120">If you use Chrome in Incognito mode, make sure that the ClickOnce extension is also enabled for Incognito mode.</span></span>
> - <span data-ttu-id="d3551-121">PDF ファイルをプレビューするには、Windows 10 の Microsoft Edge (公開されている最新のバージョン)、もしくは Windows 10、Windows 8.1、Windows 8、Windows 7、または Google Nexus 10 タブレットの Google Chrome (公開されている最新のバージョン) などの最新のブラウザを使用することをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="d3551-121">To preview PDF files, we recommend that you use browsers such as Microsoft Edge (latest publicly available version) on Windows 10, or Google Chrome (latest publicly available version) on Windows 10, Windows 8.1, Windows 8, Windows 7, or Google Nexus 10 tablet.</span></span>

### <a name="supported-web-browsers-for-retail-cloud-pos"></a><span data-ttu-id="d3551-122">Retail Cloud POS でサポートされている Web ブラウザー</span><span class="sxs-lookup"><span data-stu-id="d3551-122">Supported web browsers for Retail Cloud POS</span></span>

<span data-ttu-id="d3551-123">Retail Cloud 販売時点管理 (POS) は、指定されたオペレーティング システムで実行される次のすべての Web ブラウザーで実行できます。</span><span class="sxs-lookup"><span data-stu-id="d3551-123">Retail Cloud point of sale (POS) can run in any of the following web browsers that run on the specified operating systems:</span></span>

- <span data-ttu-id="d3551-124">Windows 10 の Microsoft Edge (公開されている最新のバージョン)</span><span class="sxs-lookup"><span data-stu-id="d3551-124">Microsoft Edge (latest publicly available version) on Windows 10</span></span>
- <span data-ttu-id="d3551-125">Windows 10、Windows 8.1、または Windows 7 の Internet Explorer 11</span><span class="sxs-lookup"><span data-stu-id="d3551-125">Internet Explorer 11 on Windows 10, Windows 8.1, or Windows 7</span></span>
- <span data-ttu-id="d3551-126">Windows 10、Windows 8.1、または Windows 7 の Chrome (公開されている最新のバージョン)</span><span class="sxs-lookup"><span data-stu-id="d3551-126">Chrome (latest publicly available version) on Windows 10, Windows 8.1, or Windows 7</span></span>

## <a name="network-requirements"></a><span data-ttu-id="d3551-127">ネットワーク要件</span><span class="sxs-lookup"><span data-stu-id="d3551-127">Network requirements</span></span>
- <span data-ttu-id="d3551-128">Finance and Operations は、待機時間が 250 ～ 300 ミリ秒 (ms) 以下のネットワーク用に設計されています。</span><span class="sxs-lookup"><span data-stu-id="d3551-128">Finance and Operations is designed for networks that have a latency of 250–300 milliseconds (ms) or less.</span></span> <span data-ttu-id="d3551-129">これは、ブラウザー クライアントから Finance and Operations をホストする Microsoft Azure データセンターまでの待機時間です。</span><span class="sxs-lookup"><span data-stu-id="d3551-129">This latency is the latency from a browser client to the Microsoft Azure datacenter that hosts Finance and Operations.</span></span> <span data-ttu-id="d3551-130">ネットワー待ち時間を <http://www.azurespeed.com> でテストすることをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="d3551-130">We recommend that you test network latency at <http://www.azurespeed.com>.</span></span>
- <span data-ttu-id="d3551-131">Finance and Operations の帯域幅の要件はシナリオによって異なります。</span><span class="sxs-lookup"><span data-stu-id="d3551-131">Bandwidth requirements for Finance and Operations depend on your scenario.</span></span> <span data-ttu-id="d3551-132">最も一般的なシナリオでは、毎秒 50 キロバイト (KBps) を超える帯域幅が必要です。</span><span class="sxs-lookup"><span data-stu-id="d3551-132">Most typical scenarios require a bandwidth that is more than 50 kilobytes per second (KBps).</span></span> <span data-ttu-id="d3551-133">ただし、ワークスペースや大がかりなカスタマイズを含む高度な伝送データ要件があるシナリオには、帯域幅を増やすことを勧めます。</span><span class="sxs-lookup"><span data-stu-id="d3551-133">However, we recommend more bandwidth for scenarios that have high payload requirements, such as scenarios that involve workspaces or extensive customization.</span></span>

<span data-ttu-id="d3551-134">一般に、Finance and Operations は、インターネットに最適化されます。</span><span class="sxs-lookup"><span data-stu-id="d3551-134">In general, Finance and Operations is optimized for the internet.</span></span> <span data-ttu-id="d3551-135">ブラウザー クライアントから Azure データセンターへのラウンド トリップの数は非常に小さく、全伝送データは圧縮されます。</span><span class="sxs-lookup"><span data-stu-id="d3551-135">The number of round trips from a browser client to the Azure datacenter is very small, and the whole payload is compressed.</span></span>

> [!WARNING]
> <span data-ttu-id="d3551-136">ユーザー数に帯域幅要件の最小値を掛けて、クライアントの場所からの帯域幅要件を計算しないでください。</span><span class="sxs-lookup"><span data-stu-id="d3551-136">Don't calculate bandwidth requirements from a client location by multiplying the number of users by the minimum bandwidth requirements.</span></span> <span data-ttu-id="d3551-137">特定の場所の同時使用は非常に計算が困難です。</span><span class="sxs-lookup"><span data-stu-id="d3551-137">The concurrent usage of a given location is very difficult to calculate.</span></span> <span data-ttu-id="d3551-138">帯域幅の要件について懸念する顧客は、Finance and Operations のプレビュー バージョンを使用するべきです。</span><span class="sxs-lookup"><span data-stu-id="d3551-138">Customers who are concerned about bandwidth requirements should use a preview version of Finance and Operations.</span></span>

## <a name="net-framework-requirements"></a><span data-ttu-id="d3551-139">.NET Framework 要件</span><span class="sxs-lookup"><span data-stu-id="d3551-139">.NET Framework requirements</span></span>

<span data-ttu-id="d3551-140">Finance and Operations では、ドキュメント回覧エージェントなどのすべての ClickOnce アプリケーション用として、Microsoft NET Framework バージョン 4.6.2 が必要です。</span><span class="sxs-lookup"><span data-stu-id="d3551-140">Finance and Operations requires the Microsoft .NET Framework version 4.6.2 for all ClickOnce applications, such as the document routing agent.</span></span> <span data-ttu-id="d3551-141">インストール手順については、[開発者の .NET Framework のインストール](https://msdn.microsoft.com/en-us/library/5a4x27ek(v=vs.110).aspx) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="d3551-141">For installation instructions, see [Install the .NET Framework for developers](https://msdn.microsoft.com/en-us/library/5a4x27ek(v=vs.110).aspx).</span></span>

## <a name="supported-microsoft-office-applications"></a><span data-ttu-id="d3551-142">サポートされている Microsoft Office アプリケーション</span><span class="sxs-lookup"><span data-stu-id="d3551-142">Supported Microsoft Office applications</span></span>

<span data-ttu-id="d3551-143">次の Microsoft Office アプリケーションは、Finance and Operations のクラウドおよびオンプレミス配置でサポートされています。</span><span class="sxs-lookup"><span data-stu-id="d3551-143">The following Microsoft Office applications are supported in cloud and on-premises deployments of Finance and Operations:</span></span>


-   <span data-ttu-id="d3551-144">Microsoft Excel と Word のアドインを実行するには、Windows 用の Microsoft Office 2016 をインストールしておく必要があります</span><span class="sxs-lookup"><span data-stu-id="d3551-144">To run the Microsoft Excel and Word add-ins, you must have Microsoft Office 2016 for Windows installed.</span></span> <span data-ttu-id="d3551-145">バージョン要求の詳細については、[Office 統合トラブルシューティング](../../dev-itpro/office-integration/office-integration-troubleshooting.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="d3551-145">For more information about version requirements, see [Office integration troubleshooting](../../dev-itpro/office-integration/office-integration-troubleshooting.md).</span></span>
-   <span data-ttu-id="d3551-146">[Excel にエクスポート] または [Word にエクスポート] 機能によって生成されたドキュメントを表示するには、Microsoft Office 2007 以降をインストールしておく必要があります。</span><span class="sxs-lookup"><span data-stu-id="d3551-146">To view documents that are generated by the Export to Excel or Export to Word functionality, you must have Microsoft Office 2007 or later installed.</span></span>

## <a name="retail-modern-pos-for-windows-requirements"></a><span data-ttu-id="d3551-147">Windows 用 Retail Modern POS の要件</span><span class="sxs-lookup"><span data-stu-id="d3551-147">Retail Modern POS for Windows requirements</span></span>

> [!NOTE]
> <span data-ttu-id="d3551-148">Retai Modern POS でオフライン データベースを使う場合、コンピューターは Microsoft SQL Server のすべてのシステム要件を満たす必要があります。</span><span class="sxs-lookup"><span data-stu-id="d3551-148">If Retail Modern POS will use an offline database, the computer must meet all system requirements for Microsoft SQL Server.</span></span> <span data-ttu-id="d3551-149">Retail Modern POS のオフライン データベースは、Service Pack 3 以降の SQL Server 2012、Service Pack 2 以降の SQL Server 2014 、または SQL Server 2016 が必要です。</span><span class="sxs-lookup"><span data-stu-id="d3551-149">An offline database for Retail Modern POS requires SQL Server 2012 with Service Pack 3 or later, SQL Server 2014 with Service Pack 2 or later, or SQL Server 2016.</span></span>  <span data-ttu-id="d3551-150">使用されている SQL Server のバージョンには、フルテキスト検索機能がインストールされている必要があります。</span><span class="sxs-lookup"><span data-stu-id="d3551-150">The SQL Server version used must have the Full-Text Search feature installed.</span></span> <span data-ttu-id="d3551-151">常に利用可能な最新のバージョンを使用し、すべての最新サービス パックをインストールすることをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="d3551-151">We recommend that you always use the latest version that is available, and that you install all the latest service packs.</span></span> <span data-ttu-id="d3551-152">これらの推奨事項に従うことで、互換性とセキュリティの両方を確保できます。</span><span class="sxs-lookup"><span data-stu-id="d3551-152">By following these recommendations, you can help to ensure both compatibility and security.</span></span>

### <a name="supported-windows-operating-systems"></a><span data-ttu-id="d3551-153">サポートされる Windows オペレーティング システム</span><span class="sxs-lookup"><span data-stu-id="d3551-153">Supported Windows operating systems</span></span>

- <span data-ttu-id="d3551-154">Retail Modern POS は 32 ビット アプリケーションですが、x86 と x64 アーキテクチャの両方で動作します。</span><span class="sxs-lookup"><span data-stu-id="d3551-154">Retail Modern POS is a 32-bit application, but it will run on both x86 and x64 architectures.</span></span>
- <span data-ttu-id="d3551-155">Retail Modern POS は Windows Server 2016、Windows 10 Pro、Windows 10 Enterprise、Windows 10 Enterprise Long Term Servicing Branch (LTSB) エディションでサポートされています。</span><span class="sxs-lookup"><span data-stu-id="d3551-155">Retail Modern POS is supported on Windows Server 2016, Windows 10 Pro, Windows 10 Enterprise, and Windows 10 Enterprise Long Term Servicing Branch (LTSB) editions.</span></span> <span data-ttu-id="d3551-156">少なくとも、Windows 10 Anniversary Update (バージョン 1607)、ビルド 14393 をインストールする必要があります。</span><span class="sxs-lookup"><span data-stu-id="d3551-156">At a minimum, the Windows 10 Anniversary Update (version 1607), build 14393, must be installed.</span></span>
- <span data-ttu-id="d3551-157">Windows 10 Pro がオペレーティング システムに対する更新を高度に管理できるドメイン内でない限り、Windows 10 Pro で Retail Modern POS およびその他の Retail のコンポーネントの使用をお勧めしません。</span><span class="sxs-lookup"><span data-stu-id="d3551-157">It is not recommended to use Retail Modern POS and other Retail components on Windows 10 Pro unless within a domain as Windows 10 Pro doesn't allow for advanced management of updates to the operating system.</span></span>

### <a name="minimum-system-requirements"></a><span data-ttu-id="d3551-158">最少システム要件</span><span class="sxs-lookup"><span data-stu-id="d3551-158">Minimum system requirements</span></span>

- <span data-ttu-id="d3551-159">POS フル レイアウト (PC およびタブレット) のサポートされている最小有効解像度は 1,024 × 768 (1366 x 768以上を推奨) です</span><span class="sxs-lookup"><span data-stu-id="d3551-159">The minimum supported effective resolution for POS Full layout (PCs and tablets) is 1,024 × 768 (recommended 1366 x 768 or greater)</span></span>
- <span data-ttu-id="d3551-160">POS コンパクトレイアウト (電話および小型のタブレット) のサポートされている最小解像度は 320 x 568 (360x640 以上を推奨) です</span><span class="sxs-lookup"><span data-stu-id="d3551-160">The minimum supported effective resolution for POS Compact layout (phones and small tablets) is 320 x 568 (recommended 360x640 or greater)</span></span>
- <span data-ttu-id="d3551-161">Retail Modern POS を実行するコンピュータは以下の要件を満たす必要があります。</span><span class="sxs-lookup"><span data-stu-id="d3551-161">The computer that Retail Modern POS runs on must meet these requirements:</span></span>

    - <span data-ttu-id="d3551-162">最低でも、2 ギガヘルツ (GHz) で動作するデュアルコア プロセッサが必要です。</span><span class="sxs-lookup"><span data-stu-id="d3551-162">It must have, at a minimum, a dual-core processor that runs at no less than 2 gigahertz (GHz).</span></span>
    - <span data-ttu-id="d3551-163">最低でも、3 ギガバイト (GB) の ランダム アクセス メモリー (RAM) が必要です。</span><span class="sxs-lookup"><span data-stu-id="d3551-163">It must have, at a minimum, 3 gigabytes (GB) of random-access memory (RAM).</span></span>  <span data-ttu-id="d3551-164">オフラインの SQL Server と組み合わせるときは、4 GB 以上の RAM が必要です。</span><span class="sxs-lookup"><span data-stu-id="d3551-164">When combining with SQL Server for offline, no less than 4 GB of RAM is required.</span></span>
    - <span data-ttu-id="d3551-165">インターネットにアクセスできる必要があります。</span><span class="sxs-lookup"><span data-stu-id="d3551-165">It must have internet access.</span></span>

## <a name="retail-modern-pos-for-apple-ipad-requirements"></a><span data-ttu-id="d3551-166">Apple iPad 用 Retail Modern POS の要件</span><span class="sxs-lookup"><span data-stu-id="d3551-166">Retail Modern POS for Apple iPad requirements</span></span>

- <span data-ttu-id="d3551-167">iOS 8 またはそれ以降</span><span class="sxs-lookup"><span data-stu-id="d3551-167">iOS 8 or later</span></span>

## <a name="retail-modern-pos-for-android-tablets-requirements"></a><span data-ttu-id="d3551-168">Android タブレット用 Retail Modern POS の要件</span><span class="sxs-lookup"><span data-stu-id="d3551-168">Retail Modern POS for Android tablets requirements</span></span>

- <span data-ttu-id="d3551-169">Android OS 4.0.4 以降</span><span class="sxs-lookup"><span data-stu-id="d3551-169">Android OS 4.0.4 or later</span></span>

## <a name="retail-hardware-station-requirements"></a><span data-ttu-id="d3551-170">Retail hardware station 要件</span><span class="sxs-lookup"><span data-stu-id="d3551-170">Retail hardware station requirements</span></span>
### <a name="supported-operating-systems"></a><span data-ttu-id="d3551-171">サポートされるオペレーティング システム</span><span class="sxs-lookup"><span data-stu-id="d3551-171">Supported operating systems</span></span>

- <span data-ttu-id="d3551-172">Retail hardware station は 32 ビット アプリケーションですが、x86 と x64 アーキテクチャの両方で動作します。</span><span class="sxs-lookup"><span data-stu-id="d3551-172">Retail hardware station is a 32-bit application, but it will run on both x86 and x64 architectures.</span></span>
- <span data-ttu-id="d3551-173">Retail hardware station は、以下のオペレーティング システムでサポートされます。</span><span class="sxs-lookup"><span data-stu-id="d3551-173">Retail hardware station is supported on the following operating systems:</span></span>

    - <span data-ttu-id="d3551-174">Windows 7 Professional、Enterprise、または Ultimate エディション。</span><span class="sxs-lookup"><span data-stu-id="d3551-174">Windows 7 Professional, Enterprise, and Ultimate editions.</span></span>
    
        > [!NOTE]
        > <span data-ttu-id="d3551-175">Windows 7 は、Internet Explorer 11 が手動でシステムにインストールされている場合にのみサポートされます。</span><span class="sxs-lookup"><span data-stu-id="d3551-175">Windows 7 is supported only if Internet Explorer 11 is manually installed on the system.</span></span>

    - <span data-ttu-id="d3551-176">Windows 8.1 Update 1 Professional、Enterprise また Embedded エディション。</span><span class="sxs-lookup"><span data-stu-id="d3551-176">Windows 8.1 Update 1 Professional, Enterprise, and Embedded editions.</span></span>
    - <span data-ttu-id="d3551-177">Windows 10 Pro、Enterprise、または Enterprise LTSB エディション。</span><span class="sxs-lookup"><span data-stu-id="d3551-177">Windows 10 Pro, Enterprise, and Enterprise LTSB editions.</span></span>
    - <span data-ttu-id="d3551-178">Windows Server 2012 R2 および Windows Server 2016。</span><span class="sxs-lookup"><span data-stu-id="d3551-178">Windows Server 2012 R2 and Windows Server 2016.</span></span>
    - <span data-ttu-id="d3551-179">Windows 10 Pro がオペレーティング システムに対する更新を高度に管理できるドメイン内でない限り、Windows 10 Pro で Retail ハードウェア ステーションおよびその他の Retail のコンポーネントの使用をお勧めしません。</span><span class="sxs-lookup"><span data-stu-id="d3551-179">It is not recommended to use Retail hardware station and other Retail components on Windows 10 Pro unless within a domain as Windows 10 Pro doesn't allow for advanced management of updates to the operating system.</span></span>

### <a name="minimum-system-requirements"></a><span data-ttu-id="d3551-180">最少システム要件</span><span class="sxs-lookup"><span data-stu-id="d3551-180">Minimum system requirements</span></span>

<span data-ttu-id="d3551-181">コンピュータは、以下の項目をインストールし使用するためのすべてのシステム要件を満たす必要があります。</span><span class="sxs-lookup"><span data-stu-id="d3551-181">The computer must meet all system requirements for installing and using the following items:</span></span>

- <span data-ttu-id="d3551-182">Microsoft Internet Information Services (IIS)</span><span class="sxs-lookup"><span data-stu-id="d3551-182">Microsoft Internet Information Services (IIS)</span></span>
- <span data-ttu-id="d3551-183">サード パーティのハードウェア</span><span class="sxs-lookup"><span data-stu-id="d3551-183">Third-party hardware</span></span>

## <a name="retail-store-scale-unit-requirements"></a><span data-ttu-id="d3551-184">Retail Store スケール ユニット要件</span><span class="sxs-lookup"><span data-stu-id="d3551-184">Retail Store Scale Unit requirements</span></span>
### <a name="supported-operating-systems"></a><span data-ttu-id="d3551-185">サポートされるオペレーティング システム</span><span class="sxs-lookup"><span data-stu-id="d3551-185">Supported operating systems</span></span>

- <span data-ttu-id="d3551-186">Retail Store スケール ユニットは 32 ビット アプリケーションですが、x86 と x64 アーキテクチャの両方で動作します。</span><span class="sxs-lookup"><span data-stu-id="d3551-186">Retail Store Scale Unit is a 32-bit application, but it will run on both x86 and x64 architectures.</span></span>
- <span data-ttu-id="d3551-187">Retail Store スケール ユニットは、以下のオペレーティング システムでサポートされます。</span><span class="sxs-lookup"><span data-stu-id="d3551-187">Retail Store Scale Unit is supported on the following operating systems:</span></span>

    - <span data-ttu-id="d3551-188">Windows 7 Professional、Enterprise、または Ultimate エディション。</span><span class="sxs-lookup"><span data-stu-id="d3551-188">Windows 7 Professional, Enterprise, and Ultimate editions.</span></span>
    
        > [!NOTE]
        > <span data-ttu-id="d3551-189">Windows 7 は、Internet Explorer 11 が手動でシステムにインストールされている場合にのみサポートされます。</span><span class="sxs-lookup"><span data-stu-id="d3551-189">Windows 7 is supported only if Internet Explorer 11 is manually installed on the system.</span></span>
    
    - <span data-ttu-id="d3551-190">Windows 8.1 Update 1 Professional、Enterprise また Embedded エディション。</span><span class="sxs-lookup"><span data-stu-id="d3551-190">Windows 8.1 Update 1 Professional, Enterprise, and Embedded editions.</span></span>
    - <span data-ttu-id="d3551-191">Windows 10 Pro、Enterprise、または Enterprise LTSB エディション。</span><span class="sxs-lookup"><span data-stu-id="d3551-191">Windows 10 Pro, Enterprise, and Enterprise LTSB editions.</span></span>
    - <span data-ttu-id="d3551-192">Windows Server 2012 R2 および Windows Server 2016。</span><span class="sxs-lookup"><span data-stu-id="d3551-192">Windows Server 2012 R2 and Windows Server 2016.</span></span>
    - <span data-ttu-id="d3551-193">Windows 10 Pro がオペレーティング システムに対する更新を高度に管理できるドメイン内でない限り、Windows 10 Pro で Retail Store Scale Unit およびその他の Retail のコンポーネントの使用をお勧めしません。</span><span class="sxs-lookup"><span data-stu-id="d3551-193">It is not recommended to use Retail Store Scale Unit and other Retail components on Windows 10 Pro unless within a domain as Windows 10 Pro doesn't allow for advanced management of updates to the operating system.</span></span>

### <a name="minimum-system-requirements"></a><span data-ttu-id="d3551-194">最少システム要件</span><span class="sxs-lookup"><span data-stu-id="d3551-194">Minimum system requirements</span></span>

- <span data-ttu-id="d3551-195">4 GB の RAM</span><span class="sxs-lookup"><span data-stu-id="d3551-195">4 GB of RAM</span></span>
- <span data-ttu-id="d3551-196">コアごとの CPU 最大処理スピード 1.6 GHz (最少 2 コア)</span><span class="sxs-lookup"><span data-stu-id="d3551-196">1.6 GHz peak CPU speed per core (Two cores are the minimum.)</span></span>
- <span data-ttu-id="d3551-197">少なくとも 10 GB の空き領域 (チャンネル データベースが大量の領域を必要とする場合があります。）</span><span class="sxs-lookup"><span data-stu-id="d3551-197">At least 10 GB of free space (The channel database can require a large amount of space.)</span></span>

### <a name="recommended-system-requirements"></a><span data-ttu-id="d3551-198">推奨システム要件</span><span class="sxs-lookup"><span data-stu-id="d3551-198">Recommended system requirements</span></span>

- <span data-ttu-id="d3551-199">6 GB の RAM</span><span class="sxs-lookup"><span data-stu-id="d3551-199">6 GB of RAM</span></span>
- <span data-ttu-id="d3551-200">コアごとの最大処理スピード 2.4 GHz i7 (または同等のもの) (推奨 4 コア)</span><span class="sxs-lookup"><span data-stu-id="d3551-200">2.4 GHz i7 (or equivalent) peak CPU speed per core (Four cores are recommended.)</span></span>
- <span data-ttu-id="d3551-201">少なくとも 10 GB の空き領域 (チャンネル データベースが大量の領域を必要とする場合があります。）</span><span class="sxs-lookup"><span data-stu-id="d3551-201">At least 10 GB of free space (The channel database can require a large amount of space.)</span></span>

## <a name="connector-requirements"></a><span data-ttu-id="d3551-202">コネクタの要件</span><span class="sxs-lookup"><span data-stu-id="d3551-202">Connector requirements</span></span>
### <a name="supported-operating-systems"></a><span data-ttu-id="d3551-203">サポートされるオペレーティング システム</span><span class="sxs-lookup"><span data-stu-id="d3551-203">Supported operating systems</span></span>

- <span data-ttu-id="d3551-204">Connector for Microsoft Dynamics AX には、Async Server Connector service と Real-time service for Microsoft Dynamics AX 2012 R3 の 2 つの独立したインストーラーがあります。</span><span class="sxs-lookup"><span data-stu-id="d3551-204">The Connector for Microsoft Dynamics AX has two separate installers, one for Async Server Connector service and one for Real-time service for Microsoft Dynamics AX 2012 R3.</span></span>
- <span data-ttu-id="d3551-205">どちらのコンポーネントも 32 ビット アプリケーションですが、x86 と x64 アーキテクチャの両方で動作します。</span><span class="sxs-lookup"><span data-stu-id="d3551-205">Both components are 32-bit applications, but they will run on both x86 and x64 architectures.</span></span>
- <span data-ttu-id="d3551-206">次のオペレーティング システムでは、両方のコンポーネントがサポートされています。</span><span class="sxs-lookup"><span data-stu-id="d3551-206">Both components are supported on the following operating systems:</span></span>

    - <span data-ttu-id="d3551-207">Windows 7 Professional、Enterprise、または Ultimate エディション。</span><span class="sxs-lookup"><span data-stu-id="d3551-207">Windows 7 Professional, Enterprise, and Ultimate editions.</span></span>
    - <span data-ttu-id="d3551-208">Windows 8.1 Update 1 Professional、Enterprise また Embedded エディション。</span><span class="sxs-lookup"><span data-stu-id="d3551-208">Windows 8.1 Update 1 Professional, Enterprise, and Embedded editions.</span></span>
    - <span data-ttu-id="d3551-209">Windows 10 Pro、Enterprise、または Enterprise LTSB エディション。</span><span class="sxs-lookup"><span data-stu-id="d3551-209">Windows 10 Pro, Enterprise, and Enterprise LTSB editions.</span></span>
    - <span data-ttu-id="d3551-210">Windows Server 2012 R2 および Windows Server 2016。</span><span class="sxs-lookup"><span data-stu-id="d3551-210">Windows Server 2012 R2 and Windows Server 2016.</span></span>
    - <span data-ttu-id="d3551-211">Windows 10 Pro がオペレーティング システムに対する更新を高度に管理できるドメイン内でない限り、Windows 10 Pro で Retail のコンポーネントの使用をお勧めしません。</span><span class="sxs-lookup"><span data-stu-id="d3551-211">It is not recommended to use Retail components on Windows 10 Pro unless within a domain as Windows 10 Pro doesn't allow for advanced management of updates to the operating system.</span></span>

### <a name="minimum-system-requirements"></a><span data-ttu-id="d3551-212">最少システム要件</span><span class="sxs-lookup"><span data-stu-id="d3551-212">Minimum system requirements</span></span>

- <span data-ttu-id="d3551-213">2 GB の RAM (4 GB の RAM を推奨)。</span><span class="sxs-lookup"><span data-stu-id="d3551-213">2 GB of RAM (Four GB of RAM are recommended.)</span></span>
- <span data-ttu-id="d3551-214">コアごとの CPU 最大処理スピード 1.6 GHz (最少 2 コア)</span><span class="sxs-lookup"><span data-stu-id="d3551-214">1.6 GHz peak CPU speed per core (Two cores are the minimum.)</span></span>
- <span data-ttu-id="d3551-215">少なくとも 10 GB の空き領域 (チャンネル データベースが大量の領域を必要とする場合があります。）</span><span class="sxs-lookup"><span data-stu-id="d3551-215">At least 10 GB of free space (The channel database can require a large amount of space.)</span></span>

## <a name="requirements-for-development-on-local-vms"></a><span data-ttu-id="d3551-216">ローカル VM の開発要件</span><span class="sxs-lookup"><span data-stu-id="d3551-216">Requirements for development on local VMs</span></span>

<span data-ttu-id="d3551-217">ローカル仮想マシン (VM) の開発要件については、[オンプレミスで実行されている VM](../../dev-itpro/dev-tools/access-instances.md#vm-that-is-running-on-premises) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="d3551-217">For information about the requirements for development on local virtual machines (VMs), see [VM that is running on-premises](../../dev-itpro/dev-tools/access-instances.md#vm-that-is-running-on-premises).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="d3551-218">その他のリソース</span><span class="sxs-lookup"><span data-stu-id="d3551-218">Additional resources</span></span>

[<span data-ttu-id="d3551-219">ベータ評価版の入手</span><span class="sxs-lookup"><span data-stu-id="d3551-219">Get an evaluation copy</span></span>](../../dev-itpro/dev-tools/get-evaluation-copy.md)

