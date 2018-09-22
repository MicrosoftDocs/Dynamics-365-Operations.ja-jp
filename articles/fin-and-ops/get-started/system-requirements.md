---
title: "クラウド配置のシステム要件"
description: "このトピックでは、現在のバージョンの Microsoft Dynamics 365 for Finance and Operations におけるクラウド展開のシステム要件を一覧表示します。"
author: sericks007
manager: AnnBe
ms.date: 08/24/2018
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
ms.sourcegitcommit: d20bc3519096f1035d26f89d42aa7e8f0fc368cd
ms.openlocfilehash: ab1c2f8b15e593d25e07de83979ff0ad26564c77
ms.contentlocale: ja-jp
ms.lasthandoff: 08/29/2018

---

# <a name="system-requirements-for-cloud-deployments"></a><span data-ttu-id="6f471-103">クラウド配置のシステム要件</span><span class="sxs-lookup"><span data-stu-id="6f471-103">System requirements for cloud deployments</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="6f471-104">このトピックでは、現在のバージョンの Microsoft Dynamics 365 for Finance and Operations におけるクラウド展開のシステム要件を一覧表示します。</span><span class="sxs-lookup"><span data-stu-id="6f471-104">This topic lists the system requirements for the current version of Microsoft Dynamics 365 for Finance and Operations for cloud deployments.</span></span> <span data-ttu-id="6f471-105">Finance and Operations をインストールする前に、このステップが適切な場合、作業しているシステムがネットワーク、ハードウェア、およびソフトウェアの最小要件を満たしているか、または超えているかを検証する必要があります。</span><span class="sxs-lookup"><span data-stu-id="6f471-105">If this step is appropriate, before you install Finance and Operations, you should verify that the system that you're working with meets or exceeds the minimum network, hardware, and software requirements.</span></span>

## <a name="supported-web-browsers"></a><span data-ttu-id="6f471-106">サポートされている Web ブラウザー</span><span class="sxs-lookup"><span data-stu-id="6f471-106">Supported web browsers</span></span>

<span data-ttu-id="6f471-107">Web アプリケーションは、指定されたオペレーティング システムで実行される次のすべての Web ブラウザで実行できます。</span><span class="sxs-lookup"><span data-stu-id="6f471-107">The web application can run in any of the following web browsers that run on the specified operating systems:</span></span>

- <span data-ttu-id="6f471-108">Windows 10 の Microsoft Edge (公開されている最新のバージョン)</span><span class="sxs-lookup"><span data-stu-id="6f471-108">Microsoft Edge (latest publicly available version) on Windows 10</span></span>
- <span data-ttu-id="6f471-109">Windows 10、Windows 8.1、または Windows 7 の Internet Explorer 11</span><span class="sxs-lookup"><span data-stu-id="6f471-109">Internet Explorer 11 on Windows 10, Windows 8.1, or Windows 7</span></span>
- <span data-ttu-id="6f471-110">Windows 10、Windows 8.1、Windows 8、Windows 7、または Google Nexus 10 タブレットの Google Chrome (公開されている最新のバージョン)</span><span class="sxs-lookup"><span data-stu-id="6f471-110">Google Chrome (latest publicly available version) on Windows 10, Windows 8.1, Windows 8, Windows 7, or Google Nexus 10 tablet</span></span>
- <span data-ttu-id="6f471-111">Mac OS X 10.10 (Yosemite)、10.11 (El Capitan)、または 10.12 (Sierra)、または Apple iPad の Apple Safari (公開されている最新のバージョン)</span><span class="sxs-lookup"><span data-stu-id="6f471-111">Apple Safari (latest publicly available version) on Mac OS X 10.10 (Yosemite), 10.11 (El Capitan), or 10.12 (Sierra), or Apple iPad</span></span>

<span data-ttu-id="6f471-112">各 Web ブラウザーの最新版を検索するには、ソフトウェア メーカーの Web サイトに移動します。</span><span class="sxs-lookup"><span data-stu-id="6f471-112">To find the latest release for each web browser, go to the software manufacturer's website.</span></span>

> [!NOTE]
> - <span data-ttu-id="6f471-113">タスク レコーダーがスクリーンショットをキャプチャし、生成された Microsoft Word ドキュメントにそれらを含めるには、プレリリース版の Chrome 拡張機能をインストールする必要があります。</span><span class="sxs-lookup"><span data-stu-id="6f471-113">To enable Task Recorder to capture screenshots and include them in Microsoft Word documents that are generated, you must install a pre-release Chrome extension.</span></span> <!---For instructions about how to install the extension, see [Screenshot Extension setup](../../dev-itpro/user-interface/task-recorder).-->
> - <span data-ttu-id="6f471-114">ワークフロー エディターは ClickOnce アプリケーションとして起動されます。</span><span class="sxs-lookup"><span data-stu-id="6f471-114">The Workflow Editor is started as a ClickOnce application.</span></span> <span data-ttu-id="6f471-115">Microsoft Edge と Internet Explorer (Microsoft Windows のサポートされているバージョン) のみが、ClickOnce アプリケーションをサポートします。</span><span class="sxs-lookup"><span data-stu-id="6f471-115">Only Microsoft Edge and Internet Explorer (on a supported version of Microsoft Windows) support ClickOnce applications.</span></span> <span data-ttu-id="6f471-116">ワークフロー エディター ClickOnce アプリケーションには、64 ビットの互換性のあるオペレーティング システムが必要です。</span><span class="sxs-lookup"><span data-stu-id="6f471-116">The Workflow Editor ClickOnce application requires a 64-bit-compatible operating system.</span></span>
> - <span data-ttu-id="6f471-117">財務報告のレポート デザイナーは、ClickOnce アプリケーションとして起動されます。</span><span class="sxs-lookup"><span data-stu-id="6f471-117">The Report Designer for Financial reporting is started as a ClickOnce application.</span></span> <span data-ttu-id="6f471-118">それには 64 ビットの互換性のあるオペレーティング システムが必要です。</span><span class="sxs-lookup"><span data-stu-id="6f471-118">It requires a 64-bit-compatible operating system.</span></span> <span data-ttu-id="6f471-119">Chrome を使用している場合、レポート デザイナーのクライアントをダウンロードするために ClickOnce 拡張機能をインストールする必要があります。</span><span class="sxs-lookup"><span data-stu-id="6f471-119">If you're using Chrome, you must install a ClickOnce extension to download the Report Designer client.</span></span> <span data-ttu-id="6f471-120">匿名モードで Chrome を使用する場合、ClickOnce の拡張機能が匿名モードに対しても有効化されていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="6f471-120">If you use Chrome in Incognito mode, make sure that the ClickOnce extension is also enabled for Incognito mode.</span></span>
> - <span data-ttu-id="6f471-121">PDF ファイルをプレビューするには、Windows 10 の Microsoft Edge (公開されている最新のバージョン)、もしくは Windows 10、Windows 8.1、Windows 8、Windows 7、または Google Nexus 10 タブレットの Google Chrome (公開されている最新のバージョン) などの最新のブラウザを使用することをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="6f471-121">To preview PDF files, we recommend that you use browsers such as Microsoft Edge (latest publicly available version) on Windows 10, or Google Chrome (latest publicly available version) on Windows 10, Windows 8.1, Windows 8, Windows 7, or Google Nexus 10 tablet.</span></span>

### <a name="supported-web-browsers-for-retail-cloud-pos"></a><span data-ttu-id="6f471-122">Retail Cloud POS でサポートされている Web ブラウザー</span><span class="sxs-lookup"><span data-stu-id="6f471-122">Supported web browsers for Retail Cloud POS</span></span>

<span data-ttu-id="6f471-123">Retail Cloud 販売時点管理 (POS) は、指定されたオペレーティング システムで実行される次のすべての Web ブラウザーで実行できます。</span><span class="sxs-lookup"><span data-stu-id="6f471-123">Retail Cloud point of sale (POS) can run in any of the following web browsers that run on the specified operating systems:</span></span>

- <span data-ttu-id="6f471-124">Windows 10 の Microsoft Edge (公開されている最新のバージョン)</span><span class="sxs-lookup"><span data-stu-id="6f471-124">Microsoft Edge (latest publicly available version) on Windows 10</span></span>
- <span data-ttu-id="6f471-125">Windows 10、Windows 8.1、または Windows 7 の Internet Explorer 11</span><span class="sxs-lookup"><span data-stu-id="6f471-125">Internet Explorer 11 on Windows 10, Windows 8.1, or Windows 7</span></span>
- <span data-ttu-id="6f471-126">Windows 10、Windows 8.1、または Windows 7 の Chrome (公開されている最新のバージョン)</span><span class="sxs-lookup"><span data-stu-id="6f471-126">Chrome (latest publicly available version) on Windows 10, Windows 8.1, or Windows 7</span></span>

## <a name="network-requirements"></a><span data-ttu-id="6f471-127">ネットワーク要件</span><span class="sxs-lookup"><span data-stu-id="6f471-127">Network requirements</span></span>
- <span data-ttu-id="6f471-128">Finance and Operations は、待機時間が 250 ～ 300 ミリ秒 (ms) 以下のネットワーク用に設計されています。</span><span class="sxs-lookup"><span data-stu-id="6f471-128">Finance and Operations is designed for networks that have a latency of 250–300 milliseconds (ms) or less.</span></span> <span data-ttu-id="6f471-129">これは、ブラウザー クライアントから Finance and Operations をホストする Microsoft Azure データセンターまでの待機時間です。</span><span class="sxs-lookup"><span data-stu-id="6f471-129">This latency is the latency from a browser client to the Microsoft Azure datacenter that hosts Finance and Operations.</span></span> <span data-ttu-id="6f471-130">ネットワー待ち時間を <http://www.azurespeed.com> でテストすることをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="6f471-130">We recommend that you test network latency at <http://www.azurespeed.com>.</span></span>
- <span data-ttu-id="6f471-131">Finance and Operations の帯域幅の要件はシナリオによって異なります。</span><span class="sxs-lookup"><span data-stu-id="6f471-131">Bandwidth requirements for Finance and Operations depend on your scenario.</span></span> <span data-ttu-id="6f471-132">最も一般的なシナリオでは、毎秒 50 キロバイト (KBps) を超える帯域幅が必要です。</span><span class="sxs-lookup"><span data-stu-id="6f471-132">Most typical scenarios require a bandwidth that is more than 50 kilobytes per second (KBps).</span></span> <span data-ttu-id="6f471-133">ただし、ワークスペースや大がかりなカスタマイズを含む高度な伝送データ要件があるシナリオには、帯域幅を増やすことを勧めます。</span><span class="sxs-lookup"><span data-stu-id="6f471-133">However, we recommend more bandwidth for scenarios that have high payload requirements, such as scenarios that involve workspaces or extensive customization.</span></span>

<span data-ttu-id="6f471-134">一般に、Finance and Operations は、インターネットに最適化されます。</span><span class="sxs-lookup"><span data-stu-id="6f471-134">In general, Finance and Operations is optimized for the internet.</span></span> <span data-ttu-id="6f471-135">ブラウザー クライアントから Azure データセンターへのラウンド トリップの数は非常に小さく、全伝送データは圧縮されます。</span><span class="sxs-lookup"><span data-stu-id="6f471-135">The number of round trips from a browser client to the Azure datacenter is very small, and the whole payload is compressed.</span></span>

> [!WARNING]
> <span data-ttu-id="6f471-136">ユーザー数に帯域幅要件の最小値を掛けて、クライアントの場所からの帯域幅要件を計算しないでください。</span><span class="sxs-lookup"><span data-stu-id="6f471-136">Don't calculate bandwidth requirements from a client location by multiplying the number of users by the minimum bandwidth requirements.</span></span> <span data-ttu-id="6f471-137">特定の場所の同時使用は非常に計算が困難です。</span><span class="sxs-lookup"><span data-stu-id="6f471-137">The concurrent usage of a given location is very difficult to calculate.</span></span> <span data-ttu-id="6f471-138">帯域幅の要件について懸念する顧客は、Finance and Operations のプレビュー バージョンを使用するべきです。</span><span class="sxs-lookup"><span data-stu-id="6f471-138">Customers who are concerned about bandwidth requirements should use a preview version of Finance and Operations.</span></span>

## <a name="net-framework-requirements"></a><span data-ttu-id="6f471-139">.NET Framework 要件</span><span class="sxs-lookup"><span data-stu-id="6f471-139">.NET Framework requirements</span></span>

<span data-ttu-id="6f471-140">Finance and Operations では、ドキュメント回覧エージェントなどのすべての ClickOnce アプリケーション用として、Microsoft NET Framework バージョン 4.6.2 が必要です。</span><span class="sxs-lookup"><span data-stu-id="6f471-140">Finance and Operations requires the Microsoft .NET Framework version 4.6.2 for all ClickOnce applications, such as the document routing agent.</span></span> <span data-ttu-id="6f471-141">インストール手順については、[開発者の .NET Framework のインストール](https://msdn.microsoft.com/en-us/library/5a4x27ek(v=vs.110).aspx) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="6f471-141">For installation instructions, see [Install the .NET Framework for developers](https://msdn.microsoft.com/en-us/library/5a4x27ek(v=vs.110).aspx).</span></span>

## <a name="supported-microsoft-office-applications"></a><span data-ttu-id="6f471-142">サポートされている Microsoft Office アプリケーション</span><span class="sxs-lookup"><span data-stu-id="6f471-142">Supported Microsoft Office applications</span></span>

<span data-ttu-id="6f471-143">次の Microsoft Office アプリケーションは、Finance and Operations のクラウドおよびオンプレミス配置でサポートされています。</span><span class="sxs-lookup"><span data-stu-id="6f471-143">The following Microsoft Office applications are supported in cloud and on-premises deployments of Finance and Operations:</span></span>


-   <span data-ttu-id="6f471-144">Microsoft Excel と Word のアドインを実行するには、Windows 用の Microsoft Office 2016 をインストールしておく必要があります</span><span class="sxs-lookup"><span data-stu-id="6f471-144">To run the Microsoft Excel and Word add-ins, you must have Microsoft Office 2016 for Windows installed.</span></span> <span data-ttu-id="6f471-145">バージョン要求の詳細については、[Office 統合トラブルシューティング](../../dev-itpro/office-integration/office-integration-troubleshooting.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="6f471-145">For more information about version requirements, see [Office integration troubleshooting](../../dev-itpro/office-integration/office-integration-troubleshooting.md).</span></span>
-   <span data-ttu-id="6f471-146">[Excel にエクスポート] または [Word にエクスポート] 機能によって生成されたドキュメントを表示するには、Microsoft Office 2007 以降をインストールしておく必要があります。</span><span class="sxs-lookup"><span data-stu-id="6f471-146">To view documents that are generated by the Export to Excel or Export to Word functionality, you must have Microsoft Office 2007 or later installed.</span></span>

## <a name="retail-modern-pos-for-windows-requirements"></a><span data-ttu-id="6f471-147">Windows 用 Retail Modern POS の要件</span><span class="sxs-lookup"><span data-stu-id="6f471-147">Retail Modern POS for Windows requirements</span></span>

> [!NOTE]
> <span data-ttu-id="6f471-148">Retai Modern POS でオフライン データベースを使う場合、コンピューターは Microsoft SQL Server のすべてのシステム要件を満たす必要があります。</span><span class="sxs-lookup"><span data-stu-id="6f471-148">If Retail Modern POS will use an offline database, the computer must meet all system requirements for Microsoft SQL Server.</span></span> <span data-ttu-id="6f471-149">Retail Modern POS のオフライン データベースは、Service Pack 3 以降の SQL Server 2012、Service Pack 2 以降の SQL Server 2014 、または SQL Server 2016 が必要です。</span><span class="sxs-lookup"><span data-stu-id="6f471-149">An offline database for Retail Modern POS requires SQL Server 2012 with Service Pack 3 or later, SQL Server 2014 with Service Pack 2 or later, or SQL Server 2016.</span></span>  <span data-ttu-id="6f471-150">使用されている SQL Server のバージョンには、フルテキスト検索機能がインストールされている必要があります。</span><span class="sxs-lookup"><span data-stu-id="6f471-150">The SQL Server version used must have the Full-Text Search feature installed.</span></span> <span data-ttu-id="6f471-151">常に利用可能な最新のバージョンを使用し、すべての最新サービス パックをインストールすることをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="6f471-151">We recommend that you always use the latest version that is available, and that you install all the latest service packs.</span></span> <span data-ttu-id="6f471-152">これらの推奨事項に従うことで、互換性とセキュリティの両方を確保できます。</span><span class="sxs-lookup"><span data-stu-id="6f471-152">By following these recommendations, you can help to ensure both compatibility and security.</span></span>
> <span data-ttu-id="6f471-153">2018 年 10 月 1 日以降、Retail Modern POS や 他のクライアント側コンポーネントを使用するには、Microsoft .NET Framework version 4.6.1 以降をインストールする必要があります。</span><span class="sxs-lookup"><span data-stu-id="6f471-153">Starting October 1, 2018, Retail Modern POS and other client-side components require that the Microsoft .NET Framework version 4.6.1 or later be installed.</span></span> <span data-ttu-id="6f471-154">インストール手順については、[開発者の .NET Framework のインストール](https://msdn.microsoft.com/en-us/library/5a4x27ek(v=vs.110).aspx) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="6f471-154">For installation instructions, see [Install the .NET Framework for developers](https://msdn.microsoft.com/en-us/library/5a4x27ek(v=vs.110).aspx).</span></span>

### <a name="supported-windows-operating-systems"></a><span data-ttu-id="6f471-155">サポートされる Windows オペレーティング システム</span><span class="sxs-lookup"><span data-stu-id="6f471-155">Supported Windows operating systems</span></span>

- <span data-ttu-id="6f471-156">Retail Modern POS は 32 ビット アプリケーションですが、x86 と x64 アーキテクチャの両方で動作します。</span><span class="sxs-lookup"><span data-stu-id="6f471-156">Retail Modern POS is a 32-bit application, but it will run on both x86 and x64 architectures.</span></span>
- <span data-ttu-id="6f471-157">Retail Modern POS は Windows Server 2016、Windows 10 Pro、Windows 10 Enterprise、Windows 10 Enterprise Long Term Servicing Branch (LTSB) エディションでサポートされています。</span><span class="sxs-lookup"><span data-stu-id="6f471-157">Retail Modern POS is supported on Windows Server 2016, Windows 10 Pro, Windows 10 Enterprise, and Windows 10 Enterprise Long Term Servicing Branch (LTSB) editions.</span></span> <span data-ttu-id="6f471-158">少なくとも、Windows 10 Anniversary Update (バージョン 1607)、ビルド 14393 をインストールする必要があります。</span><span class="sxs-lookup"><span data-stu-id="6f471-158">At a minimum, the Windows 10 Anniversary Update (version 1607), build 14393, must be installed.</span></span>
- <span data-ttu-id="6f471-159">Windows 10 Pro がオペレーティング システムに対する更新を高度に管理できるドメイン内でない限り、Windows 10 Pro で Retail Modern POS およびその他の Retail のコンポーネントの使用をお勧めしません。</span><span class="sxs-lookup"><span data-stu-id="6f471-159">It is not recommended to use Retail Modern POS and other Retail components on Windows 10 Pro unless within a domain as Windows 10 Pro doesn't allow for advanced management of updates to the operating system.</span></span>

### <a name="minimum-system-requirements"></a><span data-ttu-id="6f471-160">最少システム要件</span><span class="sxs-lookup"><span data-stu-id="6f471-160">Minimum system requirements</span></span>

- <span data-ttu-id="6f471-161">POS フル レイアウト (PC およびタブレット) のサポートされている最小有効解像度は 1,024 × 768 (1366 x 768以上を推奨) です</span><span class="sxs-lookup"><span data-stu-id="6f471-161">The minimum supported effective resolution for POS Full layout (PCs and tablets) is 1,024 × 768 (recommended 1366 x 768 or greater)</span></span>
- <span data-ttu-id="6f471-162">POS コンパクトレイアウト (電話および小型のタブレット) のサポートされている最小解像度は 320 x 568 (360x640 以上を推奨) です</span><span class="sxs-lookup"><span data-stu-id="6f471-162">The minimum supported effective resolution for POS Compact layout (phones and small tablets) is 320 x 568 (recommended 360x640 or greater)</span></span>
- <span data-ttu-id="6f471-163">Retail Modern POS を実行するコンピュータは以下の要件を満たす必要があります。</span><span class="sxs-lookup"><span data-stu-id="6f471-163">The computer that Retail Modern POS runs on must meet these requirements:</span></span>

    - <span data-ttu-id="6f471-164">最低でも、2 ギガヘルツ (GHz) で動作するデュアルコア プロセッサが必要です。</span><span class="sxs-lookup"><span data-stu-id="6f471-164">It must have, at a minimum, a dual-core processor that runs at no less than 2 gigahertz (GHz).</span></span>
    - <span data-ttu-id="6f471-165">最低でも、3 ギガバイト (GB) の ランダム アクセス メモリー (RAM) が必要です。</span><span class="sxs-lookup"><span data-stu-id="6f471-165">It must have, at a minimum, 3 gigabytes (GB) of random-access memory (RAM).</span></span>  <span data-ttu-id="6f471-166">オフラインの SQL Server と組み合わせるときは、4 GB 以上の RAM が必要です。</span><span class="sxs-lookup"><span data-stu-id="6f471-166">When combining with SQL Server for offline, no less than 4 GB of RAM is required.</span></span>
    - <span data-ttu-id="6f471-167">インターネットにアクセスできる必要があります。</span><span class="sxs-lookup"><span data-stu-id="6f471-167">It must have internet access.</span></span>

## <a name="retail-modern-pos-for-apple-iphone-or-ipad-requirements"></a><span data-ttu-id="6f471-168">Apple iPhone または iPad 用 Retail Modern POS の要件</span><span class="sxs-lookup"><span data-stu-id="6f471-168">Retail Modern POS for Apple iPhone or iPad requirements</span></span>

- <span data-ttu-id="6f471-169">iOS 11 またはそれ以降</span><span class="sxs-lookup"><span data-stu-id="6f471-169">iOS 11 or later</span></span>

## <a name="retail-modern-pos-for-android-phone-or-tablet-requirements"></a><span data-ttu-id="6f471-170">Android 電話またはタブレット用 Retail Modern POS の要件</span><span class="sxs-lookup"><span data-stu-id="6f471-170">Retail Modern POS for Android phone or tablet requirements</span></span>

- <span data-ttu-id="6f471-171">Android OS 6.0 以降</span><span class="sxs-lookup"><span data-stu-id="6f471-171">Android OS 6.0 or later</span></span>

## <a name="retail-hardware-station-requirements"></a><span data-ttu-id="6f471-172">Retail hardware station 要件</span><span class="sxs-lookup"><span data-stu-id="6f471-172">Retail hardware station requirements</span></span>

> [!NOTE]
> <span data-ttu-id="6f471-173">2018 年 10 月 1 日以降、Retail ハードウェア ステーションや 他のクライアント側コンポーネントを使用するには、.NET Framework version 4.6.1 以降をインストールする必要があります。</span><span class="sxs-lookup"><span data-stu-id="6f471-173">Starting October 1, 2018, Retail hardware station and other client-side components require that the .NET Framework version 4.6.1 or later be installed.</span></span> <span data-ttu-id="6f471-174">インストール手順については、[開発者の .NET Framework のインストール](https://msdn.microsoft.com/en-us/library/5a4x27ek(v=vs.110).aspx) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="6f471-174">For installation instructions, see [Install the .NET Framework for developers](https://msdn.microsoft.com/en-us/library/5a4x27ek(v=vs.110).aspx).</span></span>

### <a name="supported-operating-systems"></a><span data-ttu-id="6f471-175">サポートされるオペレーティング システム</span><span class="sxs-lookup"><span data-stu-id="6f471-175">Supported operating systems</span></span>

- <span data-ttu-id="6f471-176">Retail hardware station は 32 ビット アプリケーションですが、x86 と x64 アーキテクチャの両方で動作します。</span><span class="sxs-lookup"><span data-stu-id="6f471-176">Retail hardware station is a 32-bit application, but it will run on both x86 and x64 architectures.</span></span>
- <span data-ttu-id="6f471-177">Retail hardware station は、以下のオペレーティング システムでサポートされます。</span><span class="sxs-lookup"><span data-stu-id="6f471-177">Retail hardware station is supported on the following operating systems:</span></span>

    - <span data-ttu-id="6f471-178">Windows 7 Professional、Enterprise、または Ultimate エディション。</span><span class="sxs-lookup"><span data-stu-id="6f471-178">Windows 7 Professional, Enterprise, and Ultimate editions.</span></span>
    
        > [!NOTE]
        > <span data-ttu-id="6f471-179">Windows 7 は、Internet Explorer 11 が手動でシステムにインストールされている場合にのみサポートされます。</span><span class="sxs-lookup"><span data-stu-id="6f471-179">Windows 7 is supported only if Internet Explorer 11 is manually installed on the system.</span></span>

    - <span data-ttu-id="6f471-180">Windows 8.1 Update 1 Professional、Enterprise また Embedded エディション。</span><span class="sxs-lookup"><span data-stu-id="6f471-180">Windows 8.1 Update 1 Professional, Enterprise, and Embedded editions.</span></span>
    - <span data-ttu-id="6f471-181">Windows 10 Pro、Enterprise、または Enterprise LTSB エディション。</span><span class="sxs-lookup"><span data-stu-id="6f471-181">Windows 10 Pro, Enterprise, and Enterprise LTSB editions.</span></span>
    - <span data-ttu-id="6f471-182">Windows Server 2012 R2 および Windows Server 2016。</span><span class="sxs-lookup"><span data-stu-id="6f471-182">Windows Server 2012 R2 and Windows Server 2016.</span></span>
    - <span data-ttu-id="6f471-183">Windows 10 Pro がオペレーティング システムに対する更新を高度に管理できるドメイン内でない限り、Windows 10 Pro で Retail ハードウェア ステーションおよびその他の Retail のコンポーネントの使用をお勧めしません。</span><span class="sxs-lookup"><span data-stu-id="6f471-183">It is not recommended to use Retail hardware station and other Retail components on Windows 10 Pro unless within a domain as Windows 10 Pro doesn't allow for advanced management of updates to the operating system.</span></span>

### <a name="minimum-system-requirements"></a><span data-ttu-id="6f471-184">最少システム要件</span><span class="sxs-lookup"><span data-stu-id="6f471-184">Minimum system requirements</span></span>

<span data-ttu-id="6f471-185">コンピュータは、以下の項目をインストールし使用するためのすべてのシステム要件を満たす必要があります。</span><span class="sxs-lookup"><span data-stu-id="6f471-185">The computer must meet all system requirements for installing and using the following items:</span></span>

- <span data-ttu-id="6f471-186">Microsoft Internet Information Services (IIS)</span><span class="sxs-lookup"><span data-stu-id="6f471-186">Microsoft Internet Information Services (IIS)</span></span>
- <span data-ttu-id="6f471-187">サード パーティのハードウェア</span><span class="sxs-lookup"><span data-stu-id="6f471-187">Third-party hardware</span></span>

## <a name="retail-store-scale-unit-requirements"></a><span data-ttu-id="6f471-188">Retail Store スケール ユニット要件</span><span class="sxs-lookup"><span data-stu-id="6f471-188">Retail Store Scale Unit requirements</span></span>

> [!NOTE]
> <span data-ttu-id="6f471-189">2018 年 10 月 1 日以降、Retail Store Scale Unit や他のクライアント側コンポーネントを使用するには、.NET Framework version 4.6.1 以降をインストールする必要があります。</span><span class="sxs-lookup"><span data-stu-id="6f471-189">Starting October 1, 2018, Retail Store Scale Unit and other client-side components require that the .NET Framework version 4.6.1 or later be installed.</span></span> <span data-ttu-id="6f471-190">インストール手順については、[開発者の .NET Framework のインストール](https://msdn.microsoft.com/en-us/library/5a4x27ek(v=vs.110).aspx) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="6f471-190">For installation instructions, see [Install the .NET Framework for developers](https://msdn.microsoft.com/en-us/library/5a4x27ek(v=vs.110).aspx).</span></span>

<span data-ttu-id="6f471-191">以下に示す最小システム要件は、テスト シナリオでの機能へ Retail Store スケール ユニットを取得するのに必要最低限であることをご確認下さい。</span><span class="sxs-lookup"><span data-stu-id="6f471-191">Take note that the minimum system requirements listed below are the bare minimum necessary to get a Retail Store Scale Unit to function in a test scenario.</span></span>  <span data-ttu-id="6f471-192">以下は実際的な実稼働環境を表すものではありません。</span><span class="sxs-lookup"><span data-stu-id="6f471-192">The following is not representative of a realistic production environment.</span></span>  <span data-ttu-id="6f471-193">適切なパフォーマンス テストを実行し、使用するハードウェアがユーザーのニーズを満たしているのを検証することが重要です。</span><span class="sxs-lookup"><span data-stu-id="6f471-193">It is critical to perform proper performance testing and validate that the hardware used will meet the needs of the users.</span></span>

### <a name="supported-operating-systems"></a><span data-ttu-id="6f471-194">サポートされるオペレーティング システム</span><span class="sxs-lookup"><span data-stu-id="6f471-194">Supported operating systems</span></span>

- <span data-ttu-id="6f471-195">Retail Store スケール ユニットは 32 ビット アプリケーションですが、x86 と x64 アーキテクチャの両方で動作します。</span><span class="sxs-lookup"><span data-stu-id="6f471-195">Retail Store Scale Unit is a 32-bit application, but it will run on both x86 and x64 architectures.</span></span>
- <span data-ttu-id="6f471-196">Retail Store スケール ユニットは、以下のオペレーティング システムでサポートされます。</span><span class="sxs-lookup"><span data-stu-id="6f471-196">Retail Store Scale Unit is supported on the following operating systems:</span></span>

    - <span data-ttu-id="6f471-197">Windows 7 Professional、Enterprise、または Ultimate エディション。</span><span class="sxs-lookup"><span data-stu-id="6f471-197">Windows 7 Professional, Enterprise, and Ultimate editions.</span></span>
    
        > [!NOTE]
        > <span data-ttu-id="6f471-198">Windows 7 は、Internet Explorer 11 が手動でシステムにインストールされている場合にのみサポートされます。</span><span class="sxs-lookup"><span data-stu-id="6f471-198">Windows 7 is supported only if Internet Explorer 11 is manually installed on the system.</span></span>
    
    - <span data-ttu-id="6f471-199">Windows 8.1 Update 1 Professional、Enterprise また Embedded エディション。</span><span class="sxs-lookup"><span data-stu-id="6f471-199">Windows 8.1 Update 1 Professional, Enterprise, and Embedded editions.</span></span>
    - <span data-ttu-id="6f471-200">Windows 10 Pro、Enterprise、または Enterprise LTSB エディション。</span><span class="sxs-lookup"><span data-stu-id="6f471-200">Windows 10 Pro, Enterprise, and Enterprise LTSB editions.</span></span>
    - <span data-ttu-id="6f471-201">Windows Server 2012 R2 および Windows Server 2016。</span><span class="sxs-lookup"><span data-stu-id="6f471-201">Windows Server 2012 R2 and Windows Server 2016.</span></span>
    - <span data-ttu-id="6f471-202">Windows 10 Pro がオペレーティング システムに対する更新を高度に管理できるドメイン内でない限り、Windows 10 Pro で Retail Store Scale Unit およびその他の Retail のコンポーネントの使用をお勧めしません。</span><span class="sxs-lookup"><span data-stu-id="6f471-202">It is not recommended to use Retail Store Scale Unit and other Retail components on Windows 10 Pro unless within a domain as Windows 10 Pro doesn't allow for advanced management of updates to the operating system.</span></span>

### <a name="minimum-system-requirements"></a><span data-ttu-id="6f471-203">最少システム要件</span><span class="sxs-lookup"><span data-stu-id="6f471-203">Minimum system requirements</span></span>

- <span data-ttu-id="6f471-204">4 GB の RAM</span><span class="sxs-lookup"><span data-stu-id="6f471-204">4 GB of RAM</span></span>
- <span data-ttu-id="6f471-205">コアごとの CPU 最大処理スピード 1.6 GHz (最少 2 コア)</span><span class="sxs-lookup"><span data-stu-id="6f471-205">1.6 GHz peak CPU speed per core (Two cores are the minimum.)</span></span>
- <span data-ttu-id="6f471-206">少なくとも 10 GB の空き領域 (チャンネル データベースが大量の領域を必要とする場合があります。）</span><span class="sxs-lookup"><span data-stu-id="6f471-206">At least 10 GB of free space (The channel database can require a large amount of space.)</span></span>

### <a name="recommended-system-requirements"></a><span data-ttu-id="6f471-207">推奨システム要件</span><span class="sxs-lookup"><span data-stu-id="6f471-207">Recommended system requirements</span></span>

- <span data-ttu-id="6f471-208">6 GB の RAM</span><span class="sxs-lookup"><span data-stu-id="6f471-208">6 GB of RAM</span></span>
- <span data-ttu-id="6f471-209">コアごとの最大処理スピード 2.4 GHz i7 (または同等のもの) (推奨 4 コア)</span><span class="sxs-lookup"><span data-stu-id="6f471-209">2.4 GHz i7 (or equivalent) peak CPU speed per core (Four cores are recommended.)</span></span>
- <span data-ttu-id="6f471-210">少なくとも 10 GB の空き領域 (チャンネル データベースが大量の領域を必要とする場合があります。）</span><span class="sxs-lookup"><span data-stu-id="6f471-210">At least 10 GB of free space (The channel database can require a large amount of space.)</span></span>

<span data-ttu-id="6f471-211">個人のハードウェア ニーズを決定する際に次の品目も考慮することは、組織の最高の利益となります。</span><span class="sxs-lookup"><span data-stu-id="6f471-211">It would be in an organization's best interest to also take the following items into consideration when determining personal hardware needs:</span></span>
- <span data-ttu-id="6f471-212">物理的ネットワーク ポートの数 (ポートが増えると 1 秒あたりのスループットが強化されます。)</span><span class="sxs-lookup"><span data-stu-id="6f471-212">Number of physical network ports (More ports enhances throughput per second.)</span></span>
- <span data-ttu-id="6f471-213">SQL Server のログ フラッシュ サイズ (これは SQL Server パフォーマンスに直接影響します。)</span><span class="sxs-lookup"><span data-stu-id="6f471-213">SQL Server log flush size (This directly impacts SQL Server performance.)</span></span>
- <span data-ttu-id="6f471-214">データの読み取りと書き込み能力 (これは SQL サーバー パフォーマンスに直接影響を与えます。)</span><span class="sxs-lookup"><span data-stu-id="6f471-214">Data read and write capabilities (This directly impacts SQL Server performance.)</span></span>
- <span data-ttu-id="6f471-215">CPU コアの数、コアごとの並行スレッドの数、およびコアあたりの速度 (これはシステムの全体的なスループットに影響します。)</span><span class="sxs-lookup"><span data-stu-id="6f471-215">Number of CPU(s) core, number of simultaneous threads per core, and speed per core (This impacts overall throughput of the system.)</span></span>
- <span data-ttu-id="6f471-216">負荷分散が必要かどうか</span><span class="sxs-lookup"><span data-stu-id="6f471-216">Whether load balancing will be required</span></span> 

## <a name="connector-requirements"></a><span data-ttu-id="6f471-217">コネクタの要件</span><span class="sxs-lookup"><span data-stu-id="6f471-217">Connector requirements</span></span>
### <a name="supported-operating-systems"></a><span data-ttu-id="6f471-218">サポートされるオペレーティング システム</span><span class="sxs-lookup"><span data-stu-id="6f471-218">Supported operating systems</span></span>

- <span data-ttu-id="6f471-219">Connector for Microsoft Dynamics AX には、Async Server Connector service と Real-time service for Microsoft Dynamics AX 2012 R3 の 2 つの独立したインストーラーがあります。</span><span class="sxs-lookup"><span data-stu-id="6f471-219">The Connector for Microsoft Dynamics AX has two separate installers, one for Async Server Connector service and one for Real-time service for Microsoft Dynamics AX 2012 R3.</span></span>
- <span data-ttu-id="6f471-220">どちらのコンポーネントも 32 ビット アプリケーションですが、x86 と x64 アーキテクチャの両方で動作します。</span><span class="sxs-lookup"><span data-stu-id="6f471-220">Both components are 32-bit applications, but they will run on both x86 and x64 architectures.</span></span>
- <span data-ttu-id="6f471-221">次のオペレーティング システムでは、両方のコンポーネントがサポートされています。</span><span class="sxs-lookup"><span data-stu-id="6f471-221">Both components are supported on the following operating systems:</span></span>

    - <span data-ttu-id="6f471-222">Windows 7 Professional、Enterprise、または Ultimate エディション。</span><span class="sxs-lookup"><span data-stu-id="6f471-222">Windows 7 Professional, Enterprise, and Ultimate editions.</span></span>
    - <span data-ttu-id="6f471-223">Windows 8.1 Update 1 Professional、Enterprise また Embedded エディション。</span><span class="sxs-lookup"><span data-stu-id="6f471-223">Windows 8.1 Update 1 Professional, Enterprise, and Embedded editions.</span></span>
    - <span data-ttu-id="6f471-224">Windows 10 Pro、Enterprise、または Enterprise LTSB エディション。</span><span class="sxs-lookup"><span data-stu-id="6f471-224">Windows 10 Pro, Enterprise, and Enterprise LTSB editions.</span></span>
    - <span data-ttu-id="6f471-225">Windows Server 2012 R2 および Windows Server 2016。</span><span class="sxs-lookup"><span data-stu-id="6f471-225">Windows Server 2012 R2 and Windows Server 2016.</span></span>
    - <span data-ttu-id="6f471-226">Windows 10 Pro がオペレーティング システムに対する更新を高度に管理できるドメイン内でない限り、Windows 10 Pro で Retail のコンポーネントの使用をお勧めしません。</span><span class="sxs-lookup"><span data-stu-id="6f471-226">It is not recommended to use Retail components on Windows 10 Pro unless within a domain as Windows 10 Pro doesn't allow for advanced management of updates to the operating system.</span></span>

### <a name="minimum-system-requirements"></a><span data-ttu-id="6f471-227">最少システム要件</span><span class="sxs-lookup"><span data-stu-id="6f471-227">Minimum system requirements</span></span>

- <span data-ttu-id="6f471-228">2 GB の RAM (4 GB の RAM を推奨)。</span><span class="sxs-lookup"><span data-stu-id="6f471-228">2 GB of RAM (Four GB of RAM are recommended.)</span></span>
- <span data-ttu-id="6f471-229">コアごとの CPU 最大処理スピード 1.6 GHz (最少 2 コア)</span><span class="sxs-lookup"><span data-stu-id="6f471-229">1.6 GHz peak CPU speed per core (Two cores are the minimum.)</span></span>
- <span data-ttu-id="6f471-230">少なくとも 10 GB の空き領域 (チャンネル データベースが大量の領域を必要とする場合があります。）</span><span class="sxs-lookup"><span data-stu-id="6f471-230">At least 10 GB of free space (The channel database can require a large amount of space.)</span></span>

## <a name="requirements-for-development-on-local-vms"></a><span data-ttu-id="6f471-231">ローカル VM の開発要件</span><span class="sxs-lookup"><span data-stu-id="6f471-231">Requirements for development on local VMs</span></span>

<span data-ttu-id="6f471-232">ローカル仮想マシン (VM) の開発要件については、[オンプレミスで実行されている VM](../../dev-itpro/dev-tools/access-instances.md#vm-that-is-running-on-premises) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="6f471-232">For information about the requirements for development on local virtual machines (VMs), see [VM that is running on-premises](../../dev-itpro/dev-tools/access-instances.md#vm-that-is-running-on-premises).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="6f471-233">その他のリソース</span><span class="sxs-lookup"><span data-stu-id="6f471-233">Additional resources</span></span>

[<span data-ttu-id="6f471-234">ベータ評価版の入手</span><span class="sxs-lookup"><span data-stu-id="6f471-234">Get an evaluation copy</span></span>](../../dev-itpro/dev-tools/get-evaluation-copy.md)

