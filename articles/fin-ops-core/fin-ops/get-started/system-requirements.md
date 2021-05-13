---
title: クラウド配置のシステム要件
description: このトピックでは、現在のバージョンの Finance and Operations アプリのシステム要件を一覧表示します。
author: sericks007
ms.date: 01/22/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Developer, IT Pro
ms.reviewer: sericks
ms.custom: 55651
ms.assetid: e564d51d-42d3-47c5-b388-93b8219c692a
ms.search.region: Global
ms.author: sericks
ms.search.validFrom: 2016-08-30
ms.dyn365.ops.version: Platform update 8
ms.openlocfilehash: a20ca1743081b1fc27911432fccc7f668ecef193
ms.sourcegitcommit: 2f766e5bb8574d250f19180ff2e101e895097713
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/21/2021
ms.locfileid: "5923295"
---
# <a name="system-requirements-for-cloud-deployments"></a><span data-ttu-id="0f204-103">クラウド配置のシステム要件</span><span class="sxs-lookup"><span data-stu-id="0f204-103">System requirements for cloud deployments</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="0f204-104">このトピックでは、現在のバージョンの Dynamics 365 Finance および Dynamics 365 Supply Chain Management におけるクラウド配置のシステム要件を一覧表示します。</span><span class="sxs-lookup"><span data-stu-id="0f204-104">This topic lists the system requirements for the current version of Dynamics 365 Finance and Dynamics 365 Supply Chain Management for cloud deployments.</span></span> <span data-ttu-id="0f204-105">これらのアプリのいずれかをインストールする前に、このステップが適切な場合、作業しているシステムがネットワーク、ハードウェア、およびソフトウェアの最小要件を満たしているか、または超えているかを検証する必要があります。</span><span class="sxs-lookup"><span data-stu-id="0f204-105">If this step is appropriate, before you install one of these apps, you should verify that the system that you're working with meets or exceeds the minimum network, hardware, and software requirements.</span></span>

## <a name="supported-web-browsers"></a><span data-ttu-id="0f204-106">サポートされている Web ブラウザー</span><span class="sxs-lookup"><span data-stu-id="0f204-106">Supported web browsers</span></span>

<span data-ttu-id="0f204-107">ユーザーは、これらの一般的なブラウザの最新バージョンを使用してアプリにアクセスできます。</span><span class="sxs-lookup"><span data-stu-id="0f204-107">Users can access the apps by using the most recent versions of these popular browsers:</span></span> 

- <span data-ttu-id="0f204-108">Microsoft Edge (推奨: [Chromium ベースの Edge](https://support.microsoft.com/microsoft-edge/download-the-new-microsoft-edge-based-on-chromium-0f4a3dd7-55df-60f5-739f-00010dba52cf))</span><span class="sxs-lookup"><span data-stu-id="0f204-108">Microsoft Edge (recommended: [Chromium-based Edge](https://support.microsoft.com/microsoft-edge/download-the-new-microsoft-edge-based-on-chromium-0f4a3dd7-55df-60f5-739f-00010dba52cf))</span></span>
- <span data-ttu-id="0f204-109">Google Chrome</span><span class="sxs-lookup"><span data-stu-id="0f204-109">Google Chrome</span></span>
- <span data-ttu-id="0f204-110">Apple Safari</span><span class="sxs-lookup"><span data-stu-id="0f204-110">Apple Safari</span></span>
- <span data-ttu-id="0f204-111">Internet Explorer 11 (非推奨)</span><span class="sxs-lookup"><span data-stu-id="0f204-111">Internet Explorer 11 (deprecated, not recommended)</span></span>

> [!NOTE]
> <span data-ttu-id="0f204-112">パフォーマンスを最適化し、最適なエクスペリエンスを提供するために、最新のブラウザ、特に Microsoft Edge の最新バージョンを使用することをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="0f204-112">For optimal performance and an optimal experience, we recommend that you use the latest version of a modern browser, especially Microsoft Edge.</span></span> <span data-ttu-id="0f204-113">Internet Explorer 11 のサポートは非推奨です。</span><span class="sxs-lookup"><span data-stu-id="0f204-113">Support for Internet Explorer 11 is deprecated.</span></span> <span data-ttu-id="0f204-114">詳細については、[Internet Explorer 非推奨のお知らせ](../../dev-itpro/get-started/removed-deprecated-features-platform-updates.md#platform-updates-for-version-10015-of-finance-and-operations-apps)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="0f204-114">For more information, see the [Internet Explorer deprecation announcement](../../dev-itpro/get-started/removed-deprecated-features-platform-updates.md#platform-updates-for-version-10015-of-finance-and-operations-apps).</span></span>

<span data-ttu-id="0f204-115">各 Web ブラウザーの最新版を検索するには、ソフトウェア メーカーの Web サイトに移動します。</span><span class="sxs-lookup"><span data-stu-id="0f204-115">To find the latest release for each web browser, go to the software manufacturer's website.</span></span>

> [!NOTE]
> - <span data-ttu-id="0f204-116">タスク レコーダーがスクリーンショットをキャプチャし、生成された Microsoft Word ドキュメントにそれらを含めるには、プレリリース版の Chrome 拡張機能をインストールする必要があります。</span><span class="sxs-lookup"><span data-stu-id="0f204-116">To enable Task Recorder to capture screenshots and include them in Microsoft Word documents that are generated, you must install a pre-release Chrome extension.</span></span> <!---For instructions about how to install the extension, see [Screenshot Extension setup](../../dev-itpro/user-interface/task-recorder).-->
> - <span data-ttu-id="0f204-117">財務報告のワークフロー エディターおよびレポート デザイナーは、ClickOnce アプリケーションとして起動されます。</span><span class="sxs-lookup"><span data-stu-id="0f204-117">The Workflow Editor and Report Designer for Financial reporting are started as ClickOnce applications.</span></span> <span data-ttu-id="0f204-118">それには 64 ビットの互換性のあるオペレーティング システムが必要です。</span><span class="sxs-lookup"><span data-stu-id="0f204-118">They require a 64-bit-compatible operating system.</span></span> <span data-ttu-id="0f204-119">Microsoft Edge と Internet Explorer (Microsoft Windows のサポートされているバージョン) のみが、ClickOnce アプリケーションをそのままの状態でサポートします。</span><span class="sxs-lookup"><span data-stu-id="0f204-119">Only Microsoft Edge and Internet Explorer (on a supported version of Microsoft Windows) support ClickOnce applications out of the box.</span></span> <span data-ttu-id="0f204-120">Chrom を使用している場合、ClickOnce アプリケーションを使用するには、[Meta4](https://chrome.google.com/webstore/detail/meta4-clickonce-launcher/jkncabbipkgbconhaajbapbhokpbgkdc) などの ClickOnce 拡張をインストールする必要があります。</span><span class="sxs-lookup"><span data-stu-id="0f204-120">If you're using Chrome, you must install a ClickOnce extension, such as [Meta4](https://chrome.google.com/webstore/detail/meta4-clickonce-launcher/jkncabbipkgbconhaajbapbhokpbgkdc) to use ClickOnce applications.</span></span> <span data-ttu-id="0f204-121">匿名モードで Chrome を使用する場合、ClickOnce の拡張機能が匿名モードに対しても有効化されていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="0f204-121">If you use Chrome in incognito mode, make sure that the ClickOnce extension is also enabled for incognito mode.</span></span>
> - <span data-ttu-id="0f204-122">PDF ファイルをプレビューするには、Windows 10 の Microsoft Edge (公開されている最新のバージョン)、もしくは Windows 10、Windows 8.1、Windows 8、Windows 7、または Google Nexus 10 タブレットの Google Chrome (公開されている最新のバージョン) などの最新のブラウザを使用することをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="0f204-122">To preview PDF files, we recommend that you use browsers such as Microsoft Edge (latest publicly available version) on Windows 10, or Google Chrome (latest publicly available version) on Windows 10, Windows 8.1, Windows 8, Windows 7, or Google Nexus 10 tablet.</span></span>

## <a name="network-requirements"></a><span data-ttu-id="0f204-123">ネットワーク要件</span><span class="sxs-lookup"><span data-stu-id="0f204-123">Network requirements</span></span>

- <span data-ttu-id="0f204-124">アプリは、待機時間が 250 ～ 300 ミリ秒 (ms) 以下のネットワーク用に設計されています。</span><span class="sxs-lookup"><span data-stu-id="0f204-124">The app is designed for networks that have a latency of 250–300 milliseconds (ms) or less.</span></span> <span data-ttu-id="0f204-125">この待機時間は、ブラウザー クライアントからアプリをホストする Microsoft Azure データ センターまでの待機時間のことです。</span><span class="sxs-lookup"><span data-stu-id="0f204-125">This latency is the latency from a browser client to the Microsoft Azure datacenter that hosts the app.</span></span> <span data-ttu-id="0f204-126">[AzureSpeed.com](https://www.azurespeed.com) にてネットワークの待機時間をテストすることをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="0f204-126">We recommend that you test network latency at [AzureSpeed.com](https://www.azurespeed.com).</span></span>
- <span data-ttu-id="0f204-127">アプリに対する帯域幅の要件は、シナリオによって異なります。</span><span class="sxs-lookup"><span data-stu-id="0f204-127">Bandwidth requirements for the app depend on your scenario.</span></span> <span data-ttu-id="0f204-128">最も一般的なシナリオでは、毎秒 50 キロバイト (KBps) を超える帯域幅が必要です。</span><span class="sxs-lookup"><span data-stu-id="0f204-128">Most typical scenarios require a bandwidth that is more than 50 kilobytes per second (KBps).</span></span> <span data-ttu-id="0f204-129">ただし、ワークスペースや大がかりなカスタマイズを含む高度な伝送データ要件があるシナリオには、帯域幅を増やすことを勧めます。</span><span class="sxs-lookup"><span data-stu-id="0f204-129">However, we recommend more bandwidth for scenarios that have high payload requirements, such as scenarios that involve workspaces or extensive customization.</span></span>

<span data-ttu-id="0f204-130">一般に、アプリはインターネットに最適化されます。</span><span class="sxs-lookup"><span data-stu-id="0f204-130">In general, the app is optimized for the internet.</span></span> <span data-ttu-id="0f204-131">ブラウザー クライアントから Azure データセンターへのラウンド トリップの数は非常に小さく、全伝送データは圧縮されます。</span><span class="sxs-lookup"><span data-stu-id="0f204-131">The number of round trips from a browser client to the Azure datacenter is very small, and the whole payload is compressed.</span></span>

> [!WARNING]
> <span data-ttu-id="0f204-132">ユーザー数に帯域幅要件の最小値を掛けて、クライアントの場所からの帯域幅要件を計算しないでください。</span><span class="sxs-lookup"><span data-stu-id="0f204-132">Don't calculate bandwidth requirements from a client location by multiplying the number of users by the minimum bandwidth requirements.</span></span> <span data-ttu-id="0f204-133">特定の場所の同時使用は非常に計算が困難です。</span><span class="sxs-lookup"><span data-stu-id="0f204-133">The concurrent usage of a given location is very difficult to calculate.</span></span> <span data-ttu-id="0f204-134">帯域幅の要件について懸念する顧客は、アプリのプレビュー バージョンを使用するべきです。</span><span class="sxs-lookup"><span data-stu-id="0f204-134">Customers who are concerned about bandwidth requirements should use a preview version of the app.</span></span>

## <a name="net-framework-requirements"></a><span data-ttu-id="0f204-135">.NET Framework 要件</span><span class="sxs-lookup"><span data-stu-id="0f204-135">.NET Framework requirements</span></span>

<span data-ttu-id="0f204-136">アプリでは、ドキュメント回覧エージェントなどのすべての ClickOnce アプリケーション用として Microsoft .NET Framework バージョン 4.6.2 が必要です。</span><span class="sxs-lookup"><span data-stu-id="0f204-136">The app requires the Microsoft .NET Framework version 4.6.2 for all ClickOnce applications, such as the document routing agent.</span></span> <span data-ttu-id="0f204-137">インストール手順については、[開発者の .NET Framework のインストール](/dotnet/framework/install/guide-for-developers) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="0f204-137">For installation instructions, see [Install the .NET Framework for developers](/dotnet/framework/install/guide-for-developers).</span></span>

## <a name="supported-microsoft-office-applications"></a><span data-ttu-id="0f204-138">サポートされる Microsoft Office アプリケーション</span><span class="sxs-lookup"><span data-stu-id="0f204-138">Supported Microsoft Office applications</span></span>

<span data-ttu-id="0f204-139">次の Microsoft Office アプリケーションがクラウドでサポートされています。</span><span class="sxs-lookup"><span data-stu-id="0f204-139">The following Microsoft Office applications are supported in cloud:</span></span>

- <span data-ttu-id="0f204-140">Microsoft Excel と Word のアドインを実行するには、Windows 用の Microsoft Office 2016 をインストールしておく必要があります。</span><span class="sxs-lookup"><span data-stu-id="0f204-140">To run the Microsoft Excel and Word add-ins, you must have Microsoft Office 2016 for Windows installed.</span></span> <span data-ttu-id="0f204-141">バージョン要求の詳細については、[Office 統合に関するトラブルシューティング](../../dev-itpro/office-integration/office-integration-troubleshooting.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="0f204-141">For more information about version requirements, see [Troubleshoot the Office integration](../../dev-itpro/office-integration/office-integration-troubleshooting.md).</span></span>
- <span data-ttu-id="0f204-142">Excel にエクスポートまたはWord にエクスポート機能によって生成されたドキュメントを表示するには、Microsoft Office 2007 以降をインストールしておく必要があります。</span><span class="sxs-lookup"><span data-stu-id="0f204-142">To view documents that are generated by the Export to Excel or Export to Word functionality, you must have Microsoft Office 2007 or later installed.</span></span>

## <a name="requirements-for-development-on-local-vms"></a><span data-ttu-id="0f204-143">ローカル VM の開発要件</span><span class="sxs-lookup"><span data-stu-id="0f204-143">Requirements for development on local VMs</span></span>

<span data-ttu-id="0f204-144">ローカル仮想マシン (VM) の開発要件については、[ローカルで実行されている VM](../../dev-itpro/dev-tools/access-instances.md#vm-that-is-running-locally) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="0f204-144">For information about the requirements for development on local virtual machines (VMs), see [VM that is running locally](../../dev-itpro/dev-tools/access-instances.md#vm-that-is-running-locally).</span></span>

## <a name="database-collation"></a><span data-ttu-id="0f204-145">データベース照合順序</span><span class="sxs-lookup"><span data-stu-id="0f204-145">Database collation</span></span>

<span data-ttu-id="0f204-146">クラウドで唯一サポートされているアプリケーション データベースの照合順序は、**SQL\_Latin1\_General\_CP1\_CI\_AS** です。</span><span class="sxs-lookup"><span data-stu-id="0f204-146">The only supported collation for application databases in the cloud is **SQL\_Latin1\_General\_CP1\_CI\_AS**.</span></span> <span data-ttu-id="0f204-147">開発環境の SQL Server とデータベース照合順序がこれに設定されていることを確認してください。</span><span class="sxs-lookup"><span data-stu-id="0f204-147">Please ensure that your SQL Server and database collations in development environments are set to this.</span></span> <span data-ttu-id="0f204-148">また、サンドボックスに発行されたすべてのコンフィギュレーション環境にこれと同じ照合順序があることを確認します。</span><span class="sxs-lookup"><span data-stu-id="0f204-148">Also ensure that any configuration environments that are published to Sandbox have this same collation.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="0f204-149">追加リソース</span><span class="sxs-lookup"><span data-stu-id="0f204-149">Additional resources</span></span>

[<span data-ttu-id="0f204-150">評価版コピーの入手</span><span class="sxs-lookup"><span data-stu-id="0f204-150">Get evaluations copies</span></span>](../../dev-itpro/dev-tools/get-evaluation-copy.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]