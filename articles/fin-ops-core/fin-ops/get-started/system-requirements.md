---
title: クラウド配置のシステム要件
description: このトピックでは、現在のバージョンの Finance and Operations アプリのシステム要件を一覧表示します。
author: sericks007
ms.date: 05/25/2021
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
ms.openlocfilehash: 6c1a54cc3b8f2b669315bdbca06de45e1aa5cffa
ms.sourcegitcommit: 53b797ff1b524f581046b48cdde42f50b37495bc
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/28/2021
ms.locfileid: "6116969"
---
# <a name="system-requirements-for-cloud-deployments"></a><span data-ttu-id="293cc-103">クラウド配置のシステム要件</span><span class="sxs-lookup"><span data-stu-id="293cc-103">System requirements for cloud deployments</span></span>

[!include [banner](../includes/banner.md)]
[!include [banner](../includes/preview-banner.md)]

<span data-ttu-id="293cc-104">このトピックでは、現在のバージョンの Dynamics 365 Finance および Dynamics 365 Supply Chain Management におけるクラウド配置のシステム要件を一覧表示します。</span><span class="sxs-lookup"><span data-stu-id="293cc-104">This topic lists the system requirements for the current version of Dynamics 365 Finance and Dynamics 365 Supply Chain Management for cloud deployments.</span></span> <span data-ttu-id="293cc-105">これらのアプリのいずれかをインストールする前に、このステップが適切な場合、作業しているシステムがネットワーク、ハードウェア、およびソフトウェアの最小要件を満たしているか、または超えているかを検証する必要があります。</span><span class="sxs-lookup"><span data-stu-id="293cc-105">If this step is appropriate, before you install one of these apps, you should verify that the system that you're working with meets or exceeds the minimum network, hardware, and software requirements.</span></span>

## <a name="supported-web-browsers"></a><span data-ttu-id="293cc-106">サポートされている Web ブラウザー</span><span class="sxs-lookup"><span data-stu-id="293cc-106">Supported web browsers</span></span>

<span data-ttu-id="293cc-107">ユーザーは、これらの一般的なブラウザの最新バージョンを使用してアプリにアクセスできます。</span><span class="sxs-lookup"><span data-stu-id="293cc-107">Users can access the apps by using the most recent versions of these popular browsers:</span></span> 

- <span data-ttu-id="293cc-108">Microsoft Edge (推奨: [Chromium ベースの Edge](https://support.microsoft.com/microsoft-edge/download-the-new-microsoft-edge-based-on-chromium-0f4a3dd7-55df-60f5-739f-00010dba52cf))</span><span class="sxs-lookup"><span data-stu-id="293cc-108">Microsoft Edge (recommended: [Chromium-based Edge](https://support.microsoft.com/microsoft-edge/download-the-new-microsoft-edge-based-on-chromium-0f4a3dd7-55df-60f5-739f-00010dba52cf))</span></span>
- <span data-ttu-id="293cc-109">Google Chrome</span><span class="sxs-lookup"><span data-stu-id="293cc-109">Google Chrome</span></span>
- <span data-ttu-id="293cc-110">Apple Safari</span><span class="sxs-lookup"><span data-stu-id="293cc-110">Apple Safari</span></span>
- <span data-ttu-id="293cc-111">Internet Explorer 11 (非推奨)</span><span class="sxs-lookup"><span data-stu-id="293cc-111">Internet Explorer 11 (deprecated, not recommended)</span></span>

<span data-ttu-id="293cc-112">各 Web ブラウザーの最新版を検索するには、ソフトウェア メーカーの Web サイトに移動します。</span><span class="sxs-lookup"><span data-stu-id="293cc-112">To find the latest release for each web browser, go to the software manufacturer's website.</span></span>

> [!NOTE]
> <span data-ttu-id="293cc-113">パフォーマンスを最適化し、最適なエクスペリエンスを提供するために、最新のブラウザ、特に Microsoft Edge の最新バージョンを使用することをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="293cc-113">For optimal performance and an optimal experience, we recommend that you use the latest version of a modern browser, especially Microsoft Edge.</span></span> 

### <a name="internal-explorer-deprecation"></a><span data-ttu-id="293cc-114">Internal Explorer の廃止</span><span class="sxs-lookup"><span data-stu-id="293cc-114">Internal Explorer deprecation</span></span> 
<span data-ttu-id="293cc-115">2020 年 12 月に Internet Explorer 11 のサポートが廃止され、2021 年 8 月にブラウザーのサポートが終了します。</span><span class="sxs-lookup"><span data-stu-id="293cc-115">Support for Internet Explorer 11 was deprecated in December 2020, with end of support for the browser occurring in August 2021.</span></span> <span data-ttu-id="293cc-116">詳細については、[Internet Explorer 非推奨のお知らせ](../../dev-itpro/get-started/removed-deprecated-features-platform-updates.md#platform-updates-for-version-10015-of-finance-and-operations-apps) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="293cc-116">For more information, see [Internet Explorer deprecation announcement](../../dev-itpro/get-started/removed-deprecated-features-platform-updates.md#platform-updates-for-version-10015-of-finance-and-operations-apps).</span></span>

<span data-ttu-id="293cc-117">バージョン 10.0.20/プラットフォーム更新プログラム 44から、Internal Exploler (IE) で Finance and Operations アプリにアクセスするユーザーにそのブラウザーに対するサポートの終了に関する通知が表示されます。</span><span class="sxs-lookup"><span data-stu-id="293cc-117">Starting in version 10.0.20/Platform update 44, users accessing Finance and Operations apps with Internal Explorer (IE) will start seeing notifications about the end of support for that browser.</span></span> <span data-ttu-id="293cc-118">2021 年 8 月 17 日より前に、複数の IE ユーザーに対して、IE サポートが間もなく終了するという情報メッセージが表示されます。</span><span class="sxs-lookup"><span data-stu-id="293cc-118">Before August 17, 2021, IE users will see an informational message that IE support is soon ending.</span></span> <span data-ttu-id="293cc-119">その日以降、サポートが正式に終了したという警告が IE ユーザーに表示されます。</span><span class="sxs-lookup"><span data-stu-id="293cc-119">After that date, IE users will see a warning that support has officially ended.</span></span> <span data-ttu-id="293cc-120">組織は、IE がユーザーにとって必須になっている以外は、これらの通知を継続することが推奨されます。そのケースでは、**Internet Explorer のサポート終了通知** 機能を無効にし、ユーザー ベースを Microsoft Edge または他の最新のブラウザーに移行する内部プロセスに依存することによりこれらの通知の非表示を選択できます。</span><span class="sxs-lookup"><span data-stu-id="293cc-120">Organizations are encouraged to keep these notifications on unless IE is mandated for your users, in which case you can choose to suppress these notifications by disabling the **Internet Explorer end-of-support notifications** feature and relying on internal processes for migrating your user base to Microsoft Edge or another modern browser.</span></span> 

<span data-ttu-id="293cc-121">Finance and Operations アプリ内の IE の使用をブロックするための現在の目標は 2022 年 4 月です。</span><span class="sxs-lookup"><span data-stu-id="293cc-121">The current target for blocking IE usage within Finance and Operations app is April 2022.</span></span> <span data-ttu-id="293cc-122">組織およびユーザーがそのブロックに対応するために、2022 年 1 月以降、IE ユーザーには IE サポートが間もなくブロックされることを示す無視できないエラー メッセージが表示されます。</span><span class="sxs-lookup"><span data-stu-id="293cc-122">To prepare organizations and users for that block, starting in January 2022, IE users will start seeing a non-dismissible error message indicating that IE support will soon be blocked.</span></span> <span data-ttu-id="293cc-123">このエラー メッセージは **Internet Explorer のサポート終了通知** 機能によって制御 **されない** ので、組織がこのメッセージを非表示にする必要がある場合、 顧客は Microsoft サポートに連絡する必要があります。</span><span class="sxs-lookup"><span data-stu-id="293cc-123">This error message is **not** controlled by the **Internet Explorer end-of-support notifications** feature, and customers will need to contact Microsoft Support if this message needs to be suppressed for their organization.</span></span>    

### <a name="special-considerations"></a><span data-ttu-id="293cc-124">特別な注意事項</span><span class="sxs-lookup"><span data-stu-id="293cc-124">Special considerations</span></span>
- <span data-ttu-id="293cc-125">タスク レコーダーがスクリーンショットをキャプチャし、生成された Microsoft Word ドキュメントにそれらを含めるには、プレリリース版の Chrome 拡張機能をインストールする必要があります。</span><span class="sxs-lookup"><span data-stu-id="293cc-125">To enable Task Recorder to capture screenshots and include them in Microsoft Word documents that are generated, you must install a pre-release Chrome extension.</span></span>
- <span data-ttu-id="293cc-126">財務報告のワークフロー エディターおよびレポート デザイナーは、ClickOnce アプリケーションとして起動されます。</span><span class="sxs-lookup"><span data-stu-id="293cc-126">The Workflow Editor and Report Designer for Financial reporting are started as ClickOnce applications.</span></span> <span data-ttu-id="293cc-127">それには 64 ビットの互換性のあるオペレーティング システムが必要です。</span><span class="sxs-lookup"><span data-stu-id="293cc-127">They require a 64-bit-compatible operating system.</span></span> <span data-ttu-id="293cc-128">Microsoft Edge と Internet Explorer (Microsoft Windows のサポートされているバージョン) のみが、ClickOnce アプリケーションをそのままの状態でサポートします。</span><span class="sxs-lookup"><span data-stu-id="293cc-128">Only Microsoft Edge and Internet Explorer (on a supported version of Microsoft Windows) support ClickOnce applications out of the box.</span></span> <span data-ttu-id="293cc-129">Chrom を使用している場合、ClickOnce アプリケーションを使用するには、[Meta4](https://chrome.google.com/webstore/detail/meta4-clickonce-launcher/jkncabbipkgbconhaajbapbhokpbgkdc) などの ClickOnce 拡張をインストールする必要があります。</span><span class="sxs-lookup"><span data-stu-id="293cc-129">If you're using Chrome, you must install a ClickOnce extension, such as [Meta4](https://chrome.google.com/webstore/detail/meta4-clickonce-launcher/jkncabbipkgbconhaajbapbhokpbgkdc) to use ClickOnce applications.</span></span> <span data-ttu-id="293cc-130">匿名モードで Chrome を使用する場合、ClickOnce の拡張機能が匿名モードに対しても有効化されていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="293cc-130">If you use Chrome in incognito mode, make sure that the ClickOnce extension is also enabled for incognito mode.</span></span>
- <span data-ttu-id="293cc-131">PDF ファイルをプレビューするには、Windows 10 の Microsoft Edge (公開されている最新のバージョン)、もしくは Windows 10、Windows 8.1、Windows 8、Windows 7、または Google Nexus 10 タブレットの Google Chrome (公開されている最新のバージョン) などの最新のブラウザを使用することをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="293cc-131">To preview PDF files, we recommend that you use browsers such as Microsoft Edge (latest publicly available version) on Windows 10, or Google Chrome (latest publicly available version) on Windows 10, Windows 8.1, Windows 8, Windows 7, or Google Nexus 10 tablet.</span></span>
## <a name="network-requirements"></a><span data-ttu-id="293cc-132">ネットワーク要件</span><span class="sxs-lookup"><span data-stu-id="293cc-132">Network requirements</span></span>

- <span data-ttu-id="293cc-133">アプリは、待機時間が 250 ～ 300 ミリ秒 (ms) 以下のネットワーク用に設計されています。</span><span class="sxs-lookup"><span data-stu-id="293cc-133">The app is designed for networks that have a latency of 250–300 milliseconds (ms) or less.</span></span> <span data-ttu-id="293cc-134">この待機時間は、ブラウザー クライアントからアプリをホストする Microsoft Azure データ センターまでの待機時間のことです。</span><span class="sxs-lookup"><span data-stu-id="293cc-134">This latency is the latency from a browser client to the Microsoft Azure datacenter that hosts the app.</span></span> <span data-ttu-id="293cc-135">[AzureSpeed.com](https://www.azurespeed.com) にてネットワークの待機時間をテストすることをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="293cc-135">We recommend that you test network latency at [AzureSpeed.com](https://www.azurespeed.com).</span></span>
- <span data-ttu-id="293cc-136">アプリに対する帯域幅の要件は、シナリオによって異なります。</span><span class="sxs-lookup"><span data-stu-id="293cc-136">Bandwidth requirements for the app depend on your scenario.</span></span> <span data-ttu-id="293cc-137">最も一般的なシナリオでは、毎秒 50 キロバイト (KBps) を超える帯域幅が必要です。</span><span class="sxs-lookup"><span data-stu-id="293cc-137">Most typical scenarios require a bandwidth that is more than 50 kilobytes per second (KBps).</span></span> <span data-ttu-id="293cc-138">ただし、ワークスペースや大がかりなカスタマイズを含む高度な伝送データ要件があるシナリオには、帯域幅を増やすことを勧めます。</span><span class="sxs-lookup"><span data-stu-id="293cc-138">However, we recommend more bandwidth for scenarios that have high payload requirements, such as scenarios that involve workspaces or extensive customization.</span></span>

<span data-ttu-id="293cc-139">一般に、アプリはインターネットに最適化されます。</span><span class="sxs-lookup"><span data-stu-id="293cc-139">In general, the app is optimized for the internet.</span></span> <span data-ttu-id="293cc-140">ブラウザー クライアントから Azure データセンターへのラウンド トリップの数は非常に小さく、全伝送データは圧縮されます。</span><span class="sxs-lookup"><span data-stu-id="293cc-140">The number of round trips from a browser client to the Azure datacenter is very small, and the whole payload is compressed.</span></span>

> [!WARNING]
> <span data-ttu-id="293cc-141">ユーザー数に帯域幅要件の最小値を掛けて、クライアントの場所からの帯域幅要件を計算しないでください。</span><span class="sxs-lookup"><span data-stu-id="293cc-141">Don't calculate bandwidth requirements from a client location by multiplying the number of users by the minimum bandwidth requirements.</span></span> <span data-ttu-id="293cc-142">特定の場所の同時使用は非常に計算が困難です。</span><span class="sxs-lookup"><span data-stu-id="293cc-142">The concurrent usage of a given location is very difficult to calculate.</span></span> <span data-ttu-id="293cc-143">帯域幅の要件について懸念する顧客は、アプリのプレビュー バージョンを使用するべきです。</span><span class="sxs-lookup"><span data-stu-id="293cc-143">Customers who are concerned about bandwidth requirements should use a preview version of the app.</span></span>

## <a name="net-framework-requirements"></a><span data-ttu-id="293cc-144">.NET Framework 要件</span><span class="sxs-lookup"><span data-stu-id="293cc-144">.NET Framework requirements</span></span>

<span data-ttu-id="293cc-145">アプリでは、ドキュメント回覧エージェントなどのすべての ClickOnce アプリケーション用として Microsoft .NET Framework バージョン 4.6.2 が必要です。</span><span class="sxs-lookup"><span data-stu-id="293cc-145">The app requires the Microsoft .NET Framework version 4.6.2 for all ClickOnce applications, such as the document routing agent.</span></span> <span data-ttu-id="293cc-146">インストール手順については、[開発者の .NET Framework のインストール](/dotnet/framework/install/guide-for-developers) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="293cc-146">For installation instructions, see [Install the .NET Framework for developers](/dotnet/framework/install/guide-for-developers).</span></span>

## <a name="supported-microsoft-office-applications"></a><span data-ttu-id="293cc-147">サポートされる Microsoft Office アプリケーション</span><span class="sxs-lookup"><span data-stu-id="293cc-147">Supported Microsoft Office applications</span></span>

<span data-ttu-id="293cc-148">次の Microsoft Office アプリケーションがクラウドでサポートされています。</span><span class="sxs-lookup"><span data-stu-id="293cc-148">The following Microsoft Office applications are supported in cloud:</span></span>

- <span data-ttu-id="293cc-149">Microsoft Excel と Word のアドインを実行するには、Windows 用の Microsoft Office 2016 をインストールしておく必要があります。</span><span class="sxs-lookup"><span data-stu-id="293cc-149">To run the Microsoft Excel and Word add-ins, you must have Microsoft Office 2016 for Windows installed.</span></span> <span data-ttu-id="293cc-150">バージョン要求の詳細については、[Office 統合に関するトラブルシューティング](../../dev-itpro/office-integration/office-integration-troubleshooting.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="293cc-150">For more information about version requirements, see [Troubleshoot the Office integration](../../dev-itpro/office-integration/office-integration-troubleshooting.md).</span></span>
- <span data-ttu-id="293cc-151">Excel にエクスポートまたはWord にエクスポート機能によって生成されたドキュメントを表示するには、Microsoft Office 2007 以降をインストールしておく必要があります。</span><span class="sxs-lookup"><span data-stu-id="293cc-151">To view documents that are generated by the Export to Excel or Export to Word functionality, you must have Microsoft Office 2007 or later installed.</span></span>

## <a name="requirements-for-development-on-local-vms"></a><span data-ttu-id="293cc-152">ローカル VM の開発要件</span><span class="sxs-lookup"><span data-stu-id="293cc-152">Requirements for development on local VMs</span></span>

<span data-ttu-id="293cc-153">ローカル仮想マシン (VM) の開発要件については、[ローカルで実行されている VM](../../dev-itpro/dev-tools/access-instances.md#vm-that-is-running-locally) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="293cc-153">For information about the requirements for development on local virtual machines (VMs), see [VM that is running locally](../../dev-itpro/dev-tools/access-instances.md#vm-that-is-running-locally).</span></span>

## <a name="database-collation"></a><span data-ttu-id="293cc-154">データベース照合順序</span><span class="sxs-lookup"><span data-stu-id="293cc-154">Database collation</span></span>

<span data-ttu-id="293cc-155">クラウドで唯一サポートされているアプリケーション データベースの照合順序は、**SQL\_Latin1\_General\_CP1\_CI\_AS** です。</span><span class="sxs-lookup"><span data-stu-id="293cc-155">The only supported collation for application databases in the cloud is **SQL\_Latin1\_General\_CP1\_CI\_AS**.</span></span> <span data-ttu-id="293cc-156">開発環境の SQL Server とデータベース照合順序がこれに設定されていることを確認してください。</span><span class="sxs-lookup"><span data-stu-id="293cc-156">Please ensure that your SQL Server and database collations in development environments are set to this.</span></span> <span data-ttu-id="293cc-157">また、サンドボックスに発行されたすべてのコンフィギュレーション環境にこれと同じ照合順序があることを確認します。</span><span class="sxs-lookup"><span data-stu-id="293cc-157">Also ensure that any configuration environments that are published to Sandbox have this same collation.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="293cc-158">追加リソース</span><span class="sxs-lookup"><span data-stu-id="293cc-158">Additional resources</span></span>

[<span data-ttu-id="293cc-159">評価版コピーの入手</span><span class="sxs-lookup"><span data-stu-id="293cc-159">Get evaluations copies</span></span>](../../dev-itpro/dev-tools/get-evaluation-copy.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
