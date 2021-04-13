---
title: Dynamics 365 Commerce のクラウド配置のシステム要件
description: このトピックでは、現在のバージョンの Dynamics 365 Commerce におけるクラウド配置のシステム要件を一覧表示します。
author: jashanno
ms.date: 02/11/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Developer, IT Pro
ms.reviewer: sericks
ms.custom: 55651
ms.search.region: Global
ms.search.industry: retail
ms.author: jashanno
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 54fe57065fec73f44004a7e9c2e6c8969d3b78d8
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/31/2021
ms.locfileid: "5797168"
---
# <a name="system-requirements-for-cloud-deployments-of-dynamics-365-commerce"></a><span data-ttu-id="e0179-103">Dynamics 365 Commerce のクラウド配置のシステム要件</span><span class="sxs-lookup"><span data-stu-id="e0179-103">System requirements for cloud deployments of Dynamics 365 Commerce</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="e0179-104">このトピックでは、現在のバージョンの Dynamics 365 Commerce のクラウド配置のシステム要件を一覧表示します。</span><span class="sxs-lookup"><span data-stu-id="e0179-104">This topic lists the system requirements for cloud deployments of the current version of Dynamics 365 Commerce.</span></span> <span data-ttu-id="e0179-105">このステップが適切な場合は、コマースをインストールする前に、作業しているシステムがネットワーク、ハードウェア、およびソフトウェアの最小要件を満たしているか、または超えているかを検証する必要があります。</span><span class="sxs-lookup"><span data-stu-id="e0179-105">If this step is appropriate, before you install Commerce, you should verify that the system that you're working with meets or exceeds the minimum network, hardware, and software requirements.</span></span>

## <a name="supported-web-browsers"></a><span data-ttu-id="e0179-106">サポートされている Web ブラウザー</span><span class="sxs-lookup"><span data-stu-id="e0179-106">Supported web browsers</span></span>

<span data-ttu-id="e0179-107">Web アプリケーションは、指定されたオペレーティング システムで実行される次のすべての Web ブラウザで実行できます。</span><span class="sxs-lookup"><span data-stu-id="e0179-107">The web application can run in any of the following web browsers that run on the specified operating systems:</span></span>

- <span data-ttu-id="e0179-108">Windows 10 の Microsoft Edge (公開されている最新のバージョン)</span><span class="sxs-lookup"><span data-stu-id="e0179-108">Microsoft Edge (latest publicly available version) on Windows 10</span></span>
- <span data-ttu-id="e0179-109">Windows 10、Windows 8.1、または Windows 7 の Internet Explorer 11</span><span class="sxs-lookup"><span data-stu-id="e0179-109">Internet Explorer 11 on Windows 10, Windows 8.1, or Windows 7</span></span>
- <span data-ttu-id="e0179-110">Google Chrome (公開されている最新バージョン)</span><span class="sxs-lookup"><span data-stu-id="e0179-110">Google Chrome (latest publicly available version)</span></span> 
- <span data-ttu-id="e0179-111">Apple Safari (公開されている最新バージョン)</span><span class="sxs-lookup"><span data-stu-id="e0179-111">Apple Safari (latest publicly available version)</span></span>

> [!NOTE]
> <span data-ttu-id="e0179-112">Azure Active Directory トークンが取得できないため、クラウド POS デバイスのデバイスのアクティブ化中に Safari ブラウザーでエラーが表示されることがあります。</span><span class="sxs-lookup"><span data-stu-id="e0179-112">It is possible for the Safari browser to show an error during device activation of a Cloud POS device due to an Azure Active Directory token being unattainable.</span></span> <span data-ttu-id="e0179-113">この問題は、[Apple デバイスの Microsoft Enterprise SSO プラグイン](https://docs.microsoft.com/azure/active-directory/develop/apple-sso-plugin) を利用することで解決できます。</span><span class="sxs-lookup"><span data-stu-id="e0179-113">You can resolve this issue by utilizing the [Microsoft Enterprise SSO plug-in for Apple devices](https://docs.microsoft.com/azure/active-directory/develop/apple-sso-plugin).</span></span>

<span data-ttu-id="e0179-114">各 Web ブラウザーの最新版を検索するには、ソフトウェア メーカーの Web サイトに移動します。</span><span class="sxs-lookup"><span data-stu-id="e0179-114">To find the latest release for each web browser, go to the software manufacturer's website.</span></span>

> [!NOTE]
> - <span data-ttu-id="e0179-115">タスク レコーダーがスクリーンショットをキャプチャし、生成された Microsoft Word ドキュメントにそれらを含めるには、プレリリース版の Chrome 拡張機能をインストールする必要があります。</span><span class="sxs-lookup"><span data-stu-id="e0179-115">To enable Task Recorder to capture screenshots and include them in Microsoft Word documents that are generated, you must install a pre-release Chrome extension.</span></span> <!---For instructions about how to install the extension, see [Screenshot Extension setup](../../dev-itpro/user-interface/task-recorder).-->
> - <span data-ttu-id="e0179-116">財務報告のワークフロー エディターおよびレポート デザイナーは、ClickOnce アプリケーションとして起動されます。</span><span class="sxs-lookup"><span data-stu-id="e0179-116">The Workflow Editor and Report Designer for Financial reporting are started as ClickOnce applications.</span></span> <span data-ttu-id="e0179-117">それには 64 ビットの互換性のあるオペレーティング システムが必要です。</span><span class="sxs-lookup"><span data-stu-id="e0179-117">They require a 64-bit-compatible operating system.</span></span> <span data-ttu-id="e0179-118">Microsoft Edge と Internet Explorer (Microsoft Windows のサポートされているバージョン) のみが、ClickOnce アプリケーションをそのままの状態でサポートします。</span><span class="sxs-lookup"><span data-stu-id="e0179-118">Only Microsoft Edge and Internet Explorer (on a supported version of Microsoft Windows) support ClickOnce applications out of the box.</span></span> <span data-ttu-id="e0179-119">Chrom を使用している場合、ClickOnce アプリケーションを使用するには、[Meta4](https://chrome.google.com/webstore/detail/meta4-clickonce-launcher/jkncabbipkgbconhaajbapbhokpbgkdc) などの ClickOnce 拡張をインストールする必要があります。</span><span class="sxs-lookup"><span data-stu-id="e0179-119">If you're using Chrome, you must install a ClickOnce extension, such as [Meta4](https://chrome.google.com/webstore/detail/meta4-clickonce-launcher/jkncabbipkgbconhaajbapbhokpbgkdc) to use ClickOnce applications.</span></span> <span data-ttu-id="e0179-120">匿名モードで Chrome を使用する場合、ClickOnce の拡張機能が匿名モードに対しても有効化されていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="e0179-120">If you use Chrome in incognito mode, make sure that the ClickOnce extension is also enabled for incognito mode.</span></span>
> - <span data-ttu-id="e0179-121">PDF ファイルをプレビューするには、Windows 10 の Microsoft Edge (公開されている最新のバージョン)、もしくは Windows 10、Windows 8.1、Windows 8、Windows 7、または Google Nexus 10 タブレットの Google Chrome (公開されている最新のバージョン) などの最新のブラウザを使用することをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="e0179-121">To preview PDF files, we recommend that you use browsers such as Microsoft Edge (latest publicly available version) on Windows 10, or Google Chrome (latest publicly available version) on Windows 10, Windows 8.1, Windows 8, Windows 7, or Google Nexus 10 tablet.</span></span>

### <a name="supported-web-browsers-for-cloud-pos"></a><span data-ttu-id="e0179-122">クラウド POS でサポートされている Web ブラウザー</span><span class="sxs-lookup"><span data-stu-id="e0179-122">Supported web browsers for Cloud POS</span></span>

<span data-ttu-id="e0179-123">クラウド販売時点管理 (POS) は、指定されたオペレーティング システムで実行される次のすべての Web ブラウザーで実行できます。</span><span class="sxs-lookup"><span data-stu-id="e0179-123">Cloud point of sale (POS) can run in any of the following web browsers that run on the specified operating systems:</span></span>

- <span data-ttu-id="e0179-124">Windows 10 の Microsoft Edge (公開されている最新のバージョン)</span><span class="sxs-lookup"><span data-stu-id="e0179-124">Microsoft Edge (latest publicly available version) on Windows 10</span></span>
- <span data-ttu-id="e0179-125">Windows 10、Windows 8.1、または Windows 7 の Internet Explorer 11</span><span class="sxs-lookup"><span data-stu-id="e0179-125">Internet Explorer 11 on Windows 10, Windows 8.1, or Windows 7</span></span>
  > [!NOTE]
  > <span data-ttu-id="e0179-126">リリース 10.0.17 から、Internet Explorer はサポートされなくなりました。</span><span class="sxs-lookup"><span data-stu-id="e0179-126">Beginning with release 10.0.17, Internet Explorer will no longer be supported.</span></span>
- <span data-ttu-id="e0179-127">Windows 10、Windows 8.1、または Windows 7 の Chrome (公開されている最新のバージョン)</span><span class="sxs-lookup"><span data-stu-id="e0179-127">Chrome (latest publicly available version) on Windows 10, Windows 8.1, or Windows 7</span></span>

## <a name="network-requirements"></a><span data-ttu-id="e0179-128">ネットワーク要件</span><span class="sxs-lookup"><span data-stu-id="e0179-128">Network requirements</span></span>

- <span data-ttu-id="e0179-129">コマースは、待機時間が 250 ～ 300 ミリ秒 (ms) 以下のネットワーク用に設計されています。</span><span class="sxs-lookup"><span data-stu-id="e0179-129">Commerce is designed for networks that have a latency of 250–300 milliseconds (ms) or less.</span></span> <span data-ttu-id="e0179-130">この待機時間は、ブラウザー クライアントからコマースをホストする Microsoft Azure データ センターまでの待機時間のことです。</span><span class="sxs-lookup"><span data-stu-id="e0179-130">This latency is the latency from a browser client to the Microsoft Azure datacenter that hosts Commerce.</span></span> <span data-ttu-id="e0179-131">[AzureSpeed.com](http://www.azurespeed.com) にてネットワークの待機時間をテストすることをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="e0179-131">We recommend that you test network latency at [AzureSpeed.com](http://www.azurespeed.com).</span></span>
- <span data-ttu-id="e0179-132">コマースに対する帯域幅の要件は、シナリオによって異なります。</span><span class="sxs-lookup"><span data-stu-id="e0179-132">Bandwidth requirements for Commerce depend on your scenario.</span></span> <span data-ttu-id="e0179-133">最も一般的なシナリオでは、毎秒 50 キロバイト (KBps) を超える帯域幅が必要です。</span><span class="sxs-lookup"><span data-stu-id="e0179-133">Most typical scenarios require a bandwidth that is more than 50 kilobytes per second (KBps).</span></span> <span data-ttu-id="e0179-134">ただし、ワークスペースや大がかりなカスタマイズを含む高度な伝送データ要件があるシナリオには、帯域幅を増やすことを勧めます。</span><span class="sxs-lookup"><span data-stu-id="e0179-134">However, we recommend more bandwidth for scenarios that have high payload requirements, such as scenarios that involve workspaces or extensive customization.</span></span>

<span data-ttu-id="e0179-135">一般に、コマースはインターネットに最適化されます。</span><span class="sxs-lookup"><span data-stu-id="e0179-135">In general, Commerce is optimized for the internet.</span></span> <span data-ttu-id="e0179-136">ブラウザー クライアントから Azure データセンターへのラウンド トリップの数は非常に小さく、全伝送データは圧縮されます。</span><span class="sxs-lookup"><span data-stu-id="e0179-136">The number of round trips from a browser client to the Azure datacenter is very small, and the whole payload is compressed.</span></span>

> [!WARNING]
> <span data-ttu-id="e0179-137">ユーザー数に帯域幅要件の最小値を掛けて、クライアントの場所からの帯域幅要件を計算しないでください。</span><span class="sxs-lookup"><span data-stu-id="e0179-137">Don't calculate bandwidth requirements from a client location by multiplying the number of users by the minimum bandwidth requirements.</span></span> <span data-ttu-id="e0179-138">特定の場所の同時使用は非常に計算が困難です。</span><span class="sxs-lookup"><span data-stu-id="e0179-138">The concurrent usage of a given location is very difficult to calculate.</span></span> <span data-ttu-id="e0179-139">帯域幅の要件について懸念する顧客は、コマースのプレビュー バージョンを使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="e0179-139">Customers who are concerned about bandwidth requirements should use a preview version of Commerce.</span></span>

## <a name="net-framework-requirements"></a><span data-ttu-id="e0179-140">.NET Framework 要件</span><span class="sxs-lookup"><span data-stu-id="e0179-140">.NET Framework requirements</span></span>

<span data-ttu-id="e0179-141">コマースでは、ドキュメント回覧エージェントなどのすべての ClickOnce アプリケーション用として Microsoft .NET Framework バージョン 4.7.1 以降が必要です。</span><span class="sxs-lookup"><span data-stu-id="e0179-141">Commerce requires Microsoft .NET Framework 4.7.1 or later for all ClickOnce applications, such as the document routing agent.</span></span> <span data-ttu-id="e0179-142">インストール手順については、[開発者の .NET Framework のインストール](https://msdn.microsoft.com/library/5a4x27ek(v=vs.110).aspx) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="e0179-142">For installation instructions, see [Install the .NET Framework for developers](https://msdn.microsoft.com/library/5a4x27ek(v=vs.110).aspx).</span></span> 

## <a name="supported-microsoft-office-applications"></a><span data-ttu-id="e0179-143">サポートされる Microsoft Office アプリケーション</span><span class="sxs-lookup"><span data-stu-id="e0179-143">Supported Microsoft Office applications</span></span>

<span data-ttu-id="e0179-144">次の Microsoft Office アプリケーションがサポートされています。</span><span class="sxs-lookup"><span data-stu-id="e0179-144">The following Microsoft Office applications are supported:</span></span>

- <span data-ttu-id="e0179-145">Microsoft Excel と Word のアドインを実行するには、Windows 用の Microsoft Office 2016 をインストールしておく必要があります。</span><span class="sxs-lookup"><span data-stu-id="e0179-145">To run the Microsoft Excel and Word add-ins, you must have Microsoft Office 2016 for Windows installed.</span></span> <span data-ttu-id="e0179-146">バージョン要求の詳細については、[Office 統合に関するトラブルシューティング](../../fin-ops-core/dev-itpro/office-integration/office-integration-troubleshooting.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="e0179-146">For more information about version requirements, see [Troubleshoot the Office integration](../../fin-ops-core/dev-itpro/office-integration/office-integration-troubleshooting.md).</span></span>
- <span data-ttu-id="e0179-147">Excel にエクスポートまたはWord にエクスポート機能によって生成されたドキュメントを表示するには、Microsoft Office 2007 以降をインストールしておく必要があります。</span><span class="sxs-lookup"><span data-stu-id="e0179-147">To view documents that are generated by the Export to Excel or Export to Word functionality, you must have Microsoft Office 2007 or later installed.</span></span>

## <a name="system-requirements-for-commerce-client-components"></a><span data-ttu-id="e0179-148">コマース クライアント コンポーネントのシステム要件</span><span class="sxs-lookup"><span data-stu-id="e0179-148">System requirements for Commerce client components</span></span>

<span data-ttu-id="e0179-149">実稼働に移行する前に適切なパフォーマンステストを実行することが重要です。</span><span class="sxs-lookup"><span data-stu-id="e0179-149">It is critical to perform proper performance testing prior to going live in production.</span></span> <span data-ttu-id="e0179-150">次に示すのは、アプリケーションが機能するための最小システム要件であると考えられます。</span><span class="sxs-lookup"><span data-stu-id="e0179-150">The following are considered minimum system requirements for applications to function.</span></span> <span data-ttu-id="e0179-151">目的のパフォーマンスを達成するには、データ量、時間あたりのトランザクション負荷、カスタマイズの影響などの概念を考慮します。</span><span class="sxs-lookup"><span data-stu-id="e0179-151">To achieve desired performance, consider concepts like data volumes, transactional load per hour, and customization impact.</span></span> <span data-ttu-id="e0179-152">実装の初期段階と最終テストの前に再度、適切なパフォーマンステストを実施することで、必要なパフォーマンスを向上させることができます。また、基本ソリューションが必要な運用時間を満たしているかどうかを検証できます。</span><span class="sxs-lookup"><span data-stu-id="e0179-152">Proper performance testing both early into implementation and again prior to final testing will allow for any necessary performance improvements to be made and to validate that the base solution meets the expected operation times required.</span></span>

[!WARNING] <span data-ttu-id="e0179-153">Microsoft Windows 7 オペレーティング システムは、セキュリティ関連の修正以外ではサポートされなくなりました。</span><span class="sxs-lookup"><span data-stu-id="e0179-153">The Microsoft Windows 7 operating system is no longer supported for anything other than security-related fixes.</span></span> <span data-ttu-id="e0179-154">そのため、Windows 7 で Dynamics 365 Commerce コンポーネントが機能する場合がありますが、このオペレーティング システムのサポートに関連するバグ修正はありません。</span><span class="sxs-lookup"><span data-stu-id="e0179-154">As a result, while Dynamics 365 Commerce components may function on Windows 7, there will be no bug fixes that specifically relate to supporting this operating system.</span></span> <span data-ttu-id="e0179-155">Windows 7 上でコンポーネントが正常に機能するには回避策が必要な場合があるため、サポートされているオペレーティング システムにアップグレードすることを強くお勧めします。</span><span class="sxs-lookup"><span data-stu-id="e0179-155">Workarounds may be required for components to function properly on Windows 7, so it is highly recommended to upgrade to a supported operating system.</span></span>

## <a name="modern-pos-for-windows-requirements"></a><span data-ttu-id="e0179-156">Windows 用 Modern POS 要件</span><span class="sxs-lookup"><span data-stu-id="e0179-156">Modern POS for Windows requirements</span></span>

> [!NOTE]
> - <span data-ttu-id="e0179-157">Modern POS でオフライン データベースを使用する場合は、Microsoft SQL Server のすべてのシステム要件を満たしていて、システムに 10 GB 以上の空きディスク領域が必要です。</span><span class="sxs-lookup"><span data-stu-id="e0179-157">If Modern POS will use an offline database, the computer must meet all system requirements for Microsoft SQL Server and the system must have no less than 10 GB of disk space available.</span></span> <span data-ttu-id="e0179-158">20 GB 以上の空きディスク領域を用意することをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="e0179-158">It is recommended to have no less than 20 GB of disk space available.</span></span> <span data-ttu-id="e0179-159">Modern POS のオフライン データベースは、Service Pack 3 以降の SQL Server 2014、Service Pack 2 の SQL Server 2016、または SQL Server 2017 以降が必要です。</span><span class="sxs-lookup"><span data-stu-id="e0179-159">An offline database for Modern POS requires SQL Server 2014 with Service Pack 3 or later, SQL Server 2016 with Service Pack 2, SQL Server 2017, or newer.</span></span> <span data-ttu-id="e0179-160">使用されている SQL Server のバージョンには、フルテキスト検索機能がインストールされている必要があります。</span><span class="sxs-lookup"><span data-stu-id="e0179-160">The SQL Server version used must have the Full-Text Search feature installed.</span></span> <span data-ttu-id="e0179-161">常に利用可能な最新のバージョンを使用し、すべての最新サービス パックをインストールすることをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="e0179-161">We recommend that you always use the latest version that is available, and that you install all the latest service packs.</span></span> <span data-ttu-id="e0179-162">これらの推奨事項に従うことで、互換性とセキュリティの両方を確保できます。</span><span class="sxs-lookup"><span data-stu-id="e0179-162">By following these recommendations, you can help to ensure both compatibility and security.</span></span>
> - <span data-ttu-id="e0179-163">2019 年 8 月 1 日以降、 Modern POS や他のクライアント側コンポーネントを使用するには、Microsoft .NET Framework バージョン 4.7.1 以降をインストールする必要があります。</span><span class="sxs-lookup"><span data-stu-id="e0179-163">Starting August 1, 2019, Modern POS and other client-side components require that the Microsoft .NET Framework version 4.7.1 or later be installed.</span></span> <span data-ttu-id="e0179-164">インストール手順については、[開発者の .NET Framework のインストール](https://msdn.microsoft.com/library/5a4x27ek(v=vs.110).aspx) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="e0179-164">For installation instructions, see [Install the .NET Framework for developers](https://msdn.microsoft.com/library/5a4x27ek(v=vs.110).aspx).</span></span>

### <a name="supported-windows-operating-systems"></a><span data-ttu-id="e0179-165">サポートされる Windows オペレーティング システム</span><span class="sxs-lookup"><span data-stu-id="e0179-165">Supported Windows operating systems</span></span>

- <span data-ttu-id="e0179-166">Modern POS は 32 ビット アプリケーションですが、x86 と x64 アーキテクチャの両方で動作します。</span><span class="sxs-lookup"><span data-stu-id="e0179-166">Modern POS is a 32-bit application, but it will run on both x86 and x64 architectures.</span></span>
- <span data-ttu-id="e0179-167">Modern POS は Windows Server 2016、Windows 10 Pro、Windows 10 Enterprise、Windows 10 Enterprise Long Term Service Branch (LTSB)、および Windows 10 IOT Enterprise Edition でサポートされています。</span><span class="sxs-lookup"><span data-stu-id="e0179-167">Modern POS is supported on Windows Server 2016, Windows 10 Pro, Windows 10 Enterprise, Windows 10 Enterprise Long Term Service Branch (LTSB), and Windows 10 IOT Enterprise editions.</span></span> <span data-ttu-id="e0179-168">少なくとも、Windows 10 Anniversary Update (バージョン 1607)、ビルド 14393 をインストールする必要があります。</span><span class="sxs-lookup"><span data-stu-id="e0179-168">At a minimum, the Windows 10 Anniversary Update (version 1607), build 14393, must be installed.</span></span>
- <span data-ttu-id="e0179-169">Windows 10 Pro がオペレーティング システムに対する更新を高度に管理できるドメイン内でない限り、Windows 10 Pro で Modern POS およびその他の Commerce のコンポーネントの使用をお勧めしません。</span><span class="sxs-lookup"><span data-stu-id="e0179-169">It is not recommended to use Modern POS and other Commerce components on Windows 10 Pro unless within a domain as Windows 10 Pro doesn't allow for advanced management of updates to the operating system.</span></span>
- <span data-ttu-id="e0179-170">同じコンピューターで Modern POS と他のコマース コンポーネントを組み合わせて使用することはお勧めできません。</span><span class="sxs-lookup"><span data-stu-id="e0179-170">It is not recommended to use Modern POS and any other Commerce component together on the same computer.</span></span>

### <a name="minimum-system-requirements"></a><span data-ttu-id="e0179-171">最少システム要件</span><span class="sxs-lookup"><span data-stu-id="e0179-171">Minimum system requirements</span></span>

- <span data-ttu-id="e0179-172">POS フル レイアウト (PC およびタブレット) のサポートされている最小有効解像度は 1,024 × 768 (1366 x 768以上を推奨) です</span><span class="sxs-lookup"><span data-stu-id="e0179-172">The minimum supported effective resolution for POS Full layout (PCs and tablets) is 1,024 × 768 (recommended 1366 x 768 or greater)</span></span>
- <span data-ttu-id="e0179-173">POS コンパクトレイアウト (電話および小型のタブレット) のサポートされている最小解像度は 320 x 568 (360x640 以上を推奨) です</span><span class="sxs-lookup"><span data-stu-id="e0179-173">The minimum supported effective resolution for POS Compact layout (phones and small tablets) is 320 x 568 (recommended 360x640 or greater)</span></span>
- <span data-ttu-id="e0179-174">Modern POS を実行するコンピューターは以下の要件を満たす必要があります。</span><span class="sxs-lookup"><span data-stu-id="e0179-174">The computer that Modern POS runs on must meet these requirements:</span></span>

    - <span data-ttu-id="e0179-175">最低でも、2 ギガヘルツ (GHz) で動作するデュアルコア プロセッサが必要です。</span><span class="sxs-lookup"><span data-stu-id="e0179-175">It must have, at a minimum, a dual-core processor that runs at no less than 2 gigahertz (GHz).</span></span>
    - <span data-ttu-id="e0179-176">最低でも、3 ギガバイト (GB) の ランダム アクセス メモリー (RAM) が必要です。</span><span class="sxs-lookup"><span data-stu-id="e0179-176">It must have, at a minimum, 3 gigabytes (GB) of random-access memory (RAM).</span></span> <span data-ttu-id="e0179-177">オフラインの SQL Server と組み合わせるときは、4 GB 以上の RAM が必要です。</span><span class="sxs-lookup"><span data-stu-id="e0179-177">When combining with SQL Server for offline, no less than 4 GB of RAM is required.</span></span>
    - <span data-ttu-id="e0179-178">インターネットにアクセスできる必要があります。</span><span class="sxs-lookup"><span data-stu-id="e0179-178">It must have internet access.</span></span>

## <a name="modern-pos-for-apple-iphone-or-ipad-requirements"></a><span data-ttu-id="e0179-179">Apple iPhone または iPad 用 Modern POS の要件</span><span class="sxs-lookup"><span data-stu-id="e0179-179">Modern POS for Apple iPhone or iPad requirements</span></span>

- <span data-ttu-id="e0179-180">iOS 11 以降</span><span class="sxs-lookup"><span data-stu-id="e0179-180">iOS 11 or later</span></span>

## <a name="modern-pos-for-android-phone-or-tablet-requirements"></a><span data-ttu-id="e0179-181">Android 電話またはタブレット用 Modern POS の要件</span><span class="sxs-lookup"><span data-stu-id="e0179-181">Modern POS for Android phone or tablet requirements</span></span>

- <span data-ttu-id="e0179-182">Android OS 6.0 以降</span><span class="sxs-lookup"><span data-stu-id="e0179-182">Android OS 6.0 or later</span></span>

## <a name="retail-hardware-station-requirements"></a><span data-ttu-id="e0179-183">Retail hardware station 要件</span><span class="sxs-lookup"><span data-stu-id="e0179-183">Retail hardware station requirements</span></span>

> [!NOTE]
> <span data-ttu-id="e0179-184">2019 年 8 月 1 日以降、Retail ハードウェア ステーションや 他のクライアント側コンポーネントを使用するには、.NET Framework version 4.7.1 以降をインストールする必要があります。</span><span class="sxs-lookup"><span data-stu-id="e0179-184">Starting August 1, 2019, Retail hardware station and other client-side components require that the .NET Framework version 4.7.1 or later be installed.</span></span> <span data-ttu-id="e0179-185">インストール手順については、[開発者の .NET Framework のインストール](https://msdn.microsoft.com/library/5a4x27ek(v=vs.110).aspx) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="e0179-185">For installation instructions, see [Install the .NET Framework for developers](https://msdn.microsoft.com/library/5a4x27ek(v=vs.110).aspx).</span></span>
> <span data-ttu-id="e0179-186">このコンポーネントはサーバー証明書を利用することに注意してください。</span><span class="sxs-lookup"><span data-stu-id="e0179-186">It is critical to note that this component utilizes a server certificate.</span></span> <span data-ttu-id="e0179-187">有効期限に対してサーバー証明書を管理する必要があります。</span><span class="sxs-lookup"><span data-stu-id="e0179-187">Server certificates must be managed for expiration.</span></span> <span data-ttu-id="e0179-188">既定では、証明書は 1 つの暦年 (365 日) で期限切れになります。</span><span class="sxs-lookup"><span data-stu-id="e0179-188">By default, a certificate expires in one calendar year (365 days).</span></span>

### <a name="supported-operating-systems"></a><span data-ttu-id="e0179-189">サポートされるオペレーティング システム</span><span class="sxs-lookup"><span data-stu-id="e0179-189">Supported operating systems</span></span>

- <span data-ttu-id="e0179-190">Retail hardware station は 32 ビット アプリケーションですが、x86 と x64 アーキテクチャの両方で動作します。</span><span class="sxs-lookup"><span data-stu-id="e0179-190">Retail hardware station is a 32-bit application, but it will run on both x86 and x64 architectures.</span></span>
- <span data-ttu-id="e0179-191">Retail hardware station は、以下のオペレーティング システムでサポートされます。</span><span class="sxs-lookup"><span data-stu-id="e0179-191">Retail hardware station is supported on the following operating systems:</span></span>

    - <span data-ttu-id="e0179-192">Windows 8.1 Update 1 Professional、Enterprise また Embedded エディション。</span><span class="sxs-lookup"><span data-stu-id="e0179-192">Windows 8.1 Update 1 Professional, Enterprise, and Embedded editions.</span></span>
    - <span data-ttu-id="e0179-193">Windows 10 Pro、Enterprise、Enterprise LTSB、および IOT Enterprise Edition。</span><span class="sxs-lookup"><span data-stu-id="e0179-193">Windows 10 Pro, Enterprise, Enterprise LTSB, and IOT Enterprise editions.</span></span>
    - <span data-ttu-id="e0179-194">Windows Server 2016 および Windows Server 2019。</span><span class="sxs-lookup"><span data-stu-id="e0179-194">Windows Server 2016 and Windows Server 2019.</span></span>
    - <span data-ttu-id="e0179-195">Windows 10 Pro がオペレーティング システムに対する更新を高度に管理できるドメイン内でない限り、Windows 10 Pro で Retail ハードウェア ステーションおよびその他のコマースのコンポーネントの使用をお勧めしません。</span><span class="sxs-lookup"><span data-stu-id="e0179-195">It is not recommended to use Retail hardware station and other Commerce components on Windows 10 Pro unless within a domain as Windows 10 Pro doesn't allow for advanced management of updates to the operating system.</span></span>

### <a name="minimum-system-requirements"></a><span data-ttu-id="e0179-196">最少システム要件</span><span class="sxs-lookup"><span data-stu-id="e0179-196">Minimum system requirements</span></span>

<span data-ttu-id="e0179-197">コンピュータは、以下の項目をインストールし使用するためのすべてのシステム要件を満たす必要があります。</span><span class="sxs-lookup"><span data-stu-id="e0179-197">The computer must meet all system requirements for installing and using the following items:</span></span>

- <span data-ttu-id="e0179-198">Microsoft Internet Information Services (IIS)</span><span class="sxs-lookup"><span data-stu-id="e0179-198">Microsoft Internet Information Services (IIS)</span></span>
- <span data-ttu-id="e0179-199">サード パーティのハードウェア</span><span class="sxs-lookup"><span data-stu-id="e0179-199">Third-party hardware</span></span>

## <a name="commerce-scale-unit-self-hosted-requirements"></a><span data-ttu-id="e0179-200">Commerce Scale Unit (自己ホスト) 要件</span><span class="sxs-lookup"><span data-stu-id="e0179-200">Commerce Scale Unit (self-hosted) requirements</span></span>

> [!NOTE]
> <span data-ttu-id="e0179-201">2019 年 8 月 1 日以降、Commerce Scale Unit や 他のクライアント側コンポーネントを使用するには、.NET Framework バージョン 4.7.1 以降をインストールする必要があります。</span><span class="sxs-lookup"><span data-stu-id="e0179-201">Starting August 1, 2019, Commerce Scale Unit and other client-side components require that the .NET Framework version 4.7.1 or later be installed.</span></span> <span data-ttu-id="e0179-202">インストール手順については、[開発者の .NET Framework のインストール](https://msdn.microsoft.com/library/5a4x27ek(v=vs.110).aspx) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="e0179-202">For installation instructions, see [Install the .NET Framework for developers](https://msdn.microsoft.com/library/5a4x27ek(v=vs.110).aspx).</span></span>
>
> <span data-ttu-id="e0179-203">このコンポーネントは、Azure Service to Service 認証に加えてサーバー証明書を利用することに注意してください。</span><span class="sxs-lookup"><span data-stu-id="e0179-203">It is critical to note that this component utilizes a server certificate in addition to Azure Service to Service authentication.</span></span>  <span data-ttu-id="e0179-204">生成された Azure Web アプリケーション キー (旧 *シークレット*) とサーバー証明書の両方が、有効期限に対して管理されている必要があります。</span><span class="sxs-lookup"><span data-stu-id="e0179-204">Both the generated Azure web application keys (formerly called *secrets*) and the server certificate must be managed for expiration.</span></span>  <span data-ttu-id="e0179-205">既定では、証明書と生成された Azure web アプリケーション キーは 1 つの暦年 (365日) で期限切れになります。</span><span class="sxs-lookup"><span data-stu-id="e0179-205">By default, a certificate and a generated Azure web application key expires in one calendar year (365 days).</span></span>

<span data-ttu-id="e0179-206">以下に示す最小システム要件は、テスト シナリオでの機能へ Commerce Scale Unit を取得するのに必要最低限であることをご確認下さい。</span><span class="sxs-lookup"><span data-stu-id="e0179-206">Take note that the minimum system requirements listed below are the bare minimum necessary to get a Commerce Scale Unit to function in a test scenario.</span></span> <span data-ttu-id="e0179-207">以下は実際的な実稼働環境を表すものではありません。</span><span class="sxs-lookup"><span data-stu-id="e0179-207">The following is not representative of a realistic production environment.</span></span> <span data-ttu-id="e0179-208">適切なパフォーマンス テストを実行し、使用するハードウェアがユーザーのニーズを満たしているのを検証することが重要です。</span><span class="sxs-lookup"><span data-stu-id="e0179-208">It is critical to perform proper performance testing and validate that the hardware used will meet the needs of the users.</span></span>

### <a name="supported-operating-systems"></a><span data-ttu-id="e0179-209">サポートされるオペレーティング システム</span><span class="sxs-lookup"><span data-stu-id="e0179-209">Supported operating systems</span></span>

- <span data-ttu-id="e0179-210">Commerce Scale Unit は 32 ビット アプリケーションですが、x86 と x64 アーキテクチャの両方で動作します。</span><span class="sxs-lookup"><span data-stu-id="e0179-210">Commerce Scale Unit is a 32-bit application, but it will run on both x86 and x64 architectures.</span></span>
- <span data-ttu-id="e0179-211">Commerce Scale Unit は、以下のオペレーティング システムでサポートされます。</span><span class="sxs-lookup"><span data-stu-id="e0179-211">Commerce Scale Unit is supported on the following operating systems:</span></span>

    - <span data-ttu-id="e0179-212">Windows 8.1 Update 1 Professional、Enterprise また Embedded エディション。</span><span class="sxs-lookup"><span data-stu-id="e0179-212">Windows 8.1 Update 1 Professional, Enterprise, and Embedded editions.</span></span>
    - <span data-ttu-id="e0179-213">Windows 10 Pro、Enterprise、Enterprise LTSB、および IOT Enterprise Edition。</span><span class="sxs-lookup"><span data-stu-id="e0179-213">Windows 10 Pro, Enterprise, Enterprise LTSB, and IOT Enterprise editions.</span></span>
    - <span data-ttu-id="e0179-214">Windows Server 2016 および Windows Server 2019。</span><span class="sxs-lookup"><span data-stu-id="e0179-214">Windows Server 2016 and Windows Server 2019.</span></span>
    - <span data-ttu-id="e0179-215">Windows 10 Pro がオペレーティング システムに対する更新を高度に管理できるドメイン内でない限り、Windows 10 Pro で Commerce Scale Unit およびその他のコマース コンポーネントの使用をお勧めしません。</span><span class="sxs-lookup"><span data-stu-id="e0179-215">It is not recommended to use Commerce Scale Unit and other Commerce components on Windows 10 Pro unless within a domain as Windows 10 Pro doesn't allow for advanced management of updates to the operating system.</span></span>

### <a name="minimum-system-requirements"></a><span data-ttu-id="e0179-216">最少システム要件</span><span class="sxs-lookup"><span data-stu-id="e0179-216">Minimum system requirements</span></span>

> [!NOTE]
> <span data-ttu-id="e0179-217">Commerce Scale Unit の最小システム要件を次に示します。</span><span class="sxs-lookup"><span data-stu-id="e0179-217">The following are the minimum system requirements for Commerce Scale Unit.</span></span>  <span data-ttu-id="e0179-218">これらと推奨要件はどちらも、テストおよび基本的な機能のための最小要件です。</span><span class="sxs-lookup"><span data-stu-id="e0179-218">Both these and the recommended requirements are the minimum possible for testing and basic functionality.</span></span>  <span data-ttu-id="e0179-219">パフォーマンス テストを実行し、Commerce Scale Unit で使用するハードウェアが期待を満たしていることを検証することが重要です。</span><span class="sxs-lookup"><span data-stu-id="e0179-219">It is crucial to perform performance testing and validate that the hardware used for Commerce Scale Unit meets expectations.</span></span>

- <span data-ttu-id="e0179-220">4 GB の RAM</span><span class="sxs-lookup"><span data-stu-id="e0179-220">4 GB of RAM</span></span>
- <span data-ttu-id="e0179-221">コアごとの CPU 最小処理スピードが 1.6 GHz の i5 (または同等) (最少 2 コア)。</span><span class="sxs-lookup"><span data-stu-id="e0179-221">1.6 GHz i5 (or equivalent) minimum CPU speed per core (2 cores are the minimum).</span></span>
- <span data-ttu-id="e0179-222">少なくとも 15 GB の空き領域 (チャンネル データベースが大量の領域を必要とする場合があります)。</span><span class="sxs-lookup"><span data-stu-id="e0179-222">At least 15 GB of free space (the channel database can require a large amount of space).</span></span>

### <a name="recommended-system-requirements"></a><span data-ttu-id="e0179-223">推奨システム要件</span><span class="sxs-lookup"><span data-stu-id="e0179-223">Recommended system requirements</span></span>

- <span data-ttu-id="e0179-224">6 GB の RAM</span><span class="sxs-lookup"><span data-stu-id="e0179-224">6 GB of RAM</span></span>
- <span data-ttu-id="e0179-225">コアごとの CPU 最小処理スピードが 2.4 GHz の i7 (または同等) (4 つのコアを推奨)。</span><span class="sxs-lookup"><span data-stu-id="e0179-225">2.4 GHz i7 (or equivalent) minimum CPU speed per core (4 cores are recommended).</span></span>
- <span data-ttu-id="e0179-226">少なくとも 20 GB の空き領域 (チャンネル データベースが大量の領域を必要とする場合があります)。</span><span class="sxs-lookup"><span data-stu-id="e0179-226">At least 20 GB of free space (the channel database can require a large amount of space).</span></span>

<span data-ttu-id="e0179-227">個人のハードウェア ニーズを決定する際に次の品目も考慮することは、組織の最高の利益となります。</span><span class="sxs-lookup"><span data-stu-id="e0179-227">It would be in an organization's best interest to also take the following items into consideration when determining personal hardware needs:</span></span>

- <span data-ttu-id="e0179-228">物理的ネットワーク ポートの数 (ポートが増えると 1 秒あたりのスループットが強化されます)。</span><span class="sxs-lookup"><span data-stu-id="e0179-228">Number of physical network ports (more ports enhances throughput per second).</span></span>
- <span data-ttu-id="e0179-229">SQL Server のログ フラッシュ サイズ (これは SQL Server パフォーマンスに直接影響します)。</span><span class="sxs-lookup"><span data-stu-id="e0179-229">SQL Server log flush size (this directly impacts SQL Server performance).</span></span>
- <span data-ttu-id="e0179-230">データの読み取りと書き込み能力 (これは SQL サーバー パフォーマンスに直接影響を与えます)。</span><span class="sxs-lookup"><span data-stu-id="e0179-230">Data read and write capabilities (this directly impacts SQL Server performance).</span></span>
- <span data-ttu-id="e0179-231">CPU コアの数、コアごとの並行スレッドの数、およびコアあたりの速度 (これはシステムの全体的なスループットに影響します)。</span><span class="sxs-lookup"><span data-stu-id="e0179-231">Number of CPU(s) core, number of simultaneous threads per core, and speed per core (this impacts overall throughput of the system).</span></span>
- <span data-ttu-id="e0179-232">負荷分散が必要かどうか。</span><span class="sxs-lookup"><span data-stu-id="e0179-232">Whether load balancing will be required.</span></span>

## <a name="connector-requirements"></a><span data-ttu-id="e0179-233">コネクタの要件</span><span class="sxs-lookup"><span data-stu-id="e0179-233">Connector requirements</span></span>

### <a name="supported-operating-systems"></a><span data-ttu-id="e0179-234">サポートされるオペレーティング システム</span><span class="sxs-lookup"><span data-stu-id="e0179-234">Supported operating systems</span></span>

- <span data-ttu-id="e0179-235">Connector for Microsoft Dynamics AX には、Async Server Connector service と Real-time service for Microsoft Dynamics AX 2012 R3 の 2 つの独立したインストーラーがあります。</span><span class="sxs-lookup"><span data-stu-id="e0179-235">The Connector for Microsoft Dynamics AX has two separate installers, one for Async Server Connector service and one for Real-time service for Microsoft Dynamics AX 2012 R3.</span></span>
- <span data-ttu-id="e0179-236">どちらのコンポーネントも 32 ビット アプリケーションですが、x86 と x64 アーキテクチャの両方で動作します。</span><span class="sxs-lookup"><span data-stu-id="e0179-236">Both components are 32-bit applications, but they will run on both x86 and x64 architectures.</span></span>
- <span data-ttu-id="e0179-237">次のオペレーティング システムでは、両方のコンポーネントがサポートされています。</span><span class="sxs-lookup"><span data-stu-id="e0179-237">Both components are supported on the following operating systems:</span></span>

    - <span data-ttu-id="e0179-238">Windows 8.1 Update 1 Professional、Enterprise また Embedded エディション。</span><span class="sxs-lookup"><span data-stu-id="e0179-238">Windows 8.1 Update 1 Professional, Enterprise, and Embedded editions.</span></span>
    - <span data-ttu-id="e0179-239">Windows 10 Pro、Enterprise、または Enterprise LTSB エディション。</span><span class="sxs-lookup"><span data-stu-id="e0179-239">Windows 10 Pro, Enterprise, and Enterprise LTSB editions.</span></span>
    - <span data-ttu-id="e0179-240">Windows Server 2016 および Windows Server 2019。</span><span class="sxs-lookup"><span data-stu-id="e0179-240">Windows Server 2016 and Windows Server 2019.</span></span>
    - <span data-ttu-id="e0179-241">Windows 10 Pro がオペレーティング システムに対する更新を高度に管理できるドメイン内でない限り、Windows 10 Pro でコマース コンポーネントの使用をお勧めしません。</span><span class="sxs-lookup"><span data-stu-id="e0179-241">It is not recommended to use Commerce components on Windows 10 Pro unless within a domain as Windows 10 Pro doesn't allow for advanced management of updates to the operating system.</span></span>

### <a name="minimum-system-requirements"></a><span data-ttu-id="e0179-242">最少システム要件</span><span class="sxs-lookup"><span data-stu-id="e0179-242">Minimum system requirements</span></span>

- <span data-ttu-id="e0179-243">2 GB の RAM (4 GB の RAM を推奨)。</span><span class="sxs-lookup"><span data-stu-id="e0179-243">2 GB of RAM (4 GB of RAM are recommended).</span></span>
- <span data-ttu-id="e0179-244">コアごとの CPU 最大処理スピード 1.6 GHz (最少 2 コア)。</span><span class="sxs-lookup"><span data-stu-id="e0179-244">1.6 GHz peak CPU speed per core (2 cores are the minimum).</span></span>
- <span data-ttu-id="e0179-245">少なくとも 10 GB の空き領域 (チャンネル データベースが大量の領域を必要とする場合があります)。</span><span class="sxs-lookup"><span data-stu-id="e0179-245">At least 10 GB of free space (the channel database can require a large amount of space).</span></span>

## <a name="requirements-for-development-on-local-vms"></a><span data-ttu-id="e0179-246">ローカル VM の開発要件</span><span class="sxs-lookup"><span data-stu-id="e0179-246">Requirements for development on local VMs</span></span>

<span data-ttu-id="e0179-247">ローカル仮想マシン (VM) の開発要件については、[オンプレミスで実行されている VM](../../dev-itpro/dev-tools/access-instances.md#vm-that-is-running-on-premises) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="e0179-247">For information about the requirements for development on local virtual machines (VMs), see [VM that is running on-premises](../../dev-itpro/dev-tools/access-instances.md#vm-that-is-running-on-premises).</span></span>

## <a name="database-collation"></a><span data-ttu-id="e0179-248">データベース照合順序</span><span class="sxs-lookup"><span data-stu-id="e0179-248">Database collation</span></span>

<span data-ttu-id="e0179-249">クラウドで唯一サポートされているコマース データベースの照合順序は、**SQL\_Latin1\_General\_CP1\_CI\_AS** です。</span><span class="sxs-lookup"><span data-stu-id="e0179-249">The only supported collation for Commerce databases in the cloud is **SQL\_Latin1\_General\_CP1\_CI\_AS**.</span></span> <span data-ttu-id="e0179-250">開発環境の SQL Server とデータベース照合順序がこれに設定されていることを確認してください。</span><span class="sxs-lookup"><span data-stu-id="e0179-250">Please ensure that your SQL Server and database collations in development environments are set to this.</span></span> <span data-ttu-id="e0179-251">また、サンドボックスに発行されたすべてのコンフィギュレーション環境にこれと同じ照合順序があることを確認します。</span><span class="sxs-lookup"><span data-stu-id="e0179-251">Also ensure that any configuration environments that are published to Sandbox have this same collation.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="e0179-252">その他のリソース</span><span class="sxs-lookup"><span data-stu-id="e0179-252">Additional resources</span></span>

[<span data-ttu-id="e0179-253">ベータ評価版の入手</span><span class="sxs-lookup"><span data-stu-id="e0179-253">Get an evaluation copy</span></span>](../../dev-itpro/dev-tools/get-evaluation-copy.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]