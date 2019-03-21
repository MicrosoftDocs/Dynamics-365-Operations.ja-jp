---
title: Talent システム要件と更新ポリシー
description: このトピックは、Dynamics 365 for Talent の要件を一覧表示します。 同様に、その更新ポリシーについても説明します。
author: rschloma
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: rschloma
ms.search.scope: Core, Operations, Talent
ms.custom: 63213
ms.assetid: 5dbc62fc-0184-4c0e-9856-e735fc68799e
ms.search.region: Global
ms.author: shielas
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: July 2017 update
ms.openlocfilehash: 64362ae9e4ebb63ca6da2cd2f41376d1d9047694
ms.sourcegitcommit: c6af2de37309b574dcb69c9caad436b55136600f
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/26/2019
ms.locfileid: "768488"
---
# <a name="talent-system-requirements-and-update-policy"></a><span data-ttu-id="83323-104">Talent システム要件と更新ポリシー</span><span class="sxs-lookup"><span data-stu-id="83323-104">Talent system requirements and update policy</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="83323-105">このトピックは、Microsoft Dynamics 365 for Talent の要件を一覧表示します。</span><span class="sxs-lookup"><span data-stu-id="83323-105">This topic lists requirements for Microsoft Dynamics 365 for Talent.</span></span> <span data-ttu-id="83323-106">同様に、その更新ポリシーについても説明します。</span><span class="sxs-lookup"><span data-stu-id="83323-106">The update policy is outlined, as well.</span></span>

## <a name="supported-web-browsers"></a><span data-ttu-id="83323-107">サポートされている Web ブラウザー</span><span class="sxs-lookup"><span data-stu-id="83323-107">Supported web browsers</span></span>

<span data-ttu-id="83323-108">Microsoft Dynamics 365 for Talent Web アプリケーションは、指定されたオペレーティング システムで実行される次のすべての Web ブラウザで実行できます。</span><span class="sxs-lookup"><span data-stu-id="83323-108">The Microsoft Dynamics 365 for Talent web application can run in any of the following web browsers that run on the specified operating systems:</span></span> 

*   <span data-ttu-id="83323-109">Windows 10 の Microsoft Edge (公開されている最新のバージョン)</span><span class="sxs-lookup"><span data-stu-id="83323-109">Microsoft Edge (latest publicly available version) on Windows 10</span></span>
*   <span data-ttu-id="83323-110">Windows 10、Windows 8.1、または Windows 7 の Internet Explorer 11</span><span class="sxs-lookup"><span data-stu-id="83323-110">Internet Explorer 11 on Windows 10, Windows 8.1, or Windows 7</span></span>
*   <span data-ttu-id="83323-111">Google Chrome (公開されている最新バージョン)</span><span class="sxs-lookup"><span data-stu-id="83323-111">Google Chrome (latest publicly available version)</span></span>
*   <span data-ttu-id="83323-112">Apple Safari (公開されている最新バージョン)</span><span class="sxs-lookup"><span data-stu-id="83323-112">Apple Safari (latest publicly available version)</span></span>

<span data-ttu-id="83323-113">各 Web ブラウザの最新版を検索するには、ソフトウェア メーカーの Web サイトに移動します。</span><span class="sxs-lookup"><span data-stu-id="83323-113">To find the latest release for each web browser, go to the software manufacturer’s website.</span></span> 

> [!NOTE]
> * <span data-ttu-id="83323-114">タスク レコーダーから生成される画像をキャプチャして Microsoft Word ドキュメントに含めるには、Chrome 拡張機能をインストールする必要があります。</span><span class="sxs-lookup"><span data-stu-id="83323-114">To capture images that are generated from Task Recorder and include them in Microsoft Word documents, you must have a Chrome extension installed.</span></span> 
> * <span data-ttu-id="83323-115">ワークフロー エディターは ClickOnce アプリケーションとして起動されます。</span><span class="sxs-lookup"><span data-stu-id="83323-115">The Workflow Editor is started as a ClickOnce application.</span></span> <span data-ttu-id="83323-116">Microsoft Edge と Internet Explorer (Microsoft Windows のサポートされているバージョン) のみが、ClickOnce アプリケーションをサポートします。</span><span class="sxs-lookup"><span data-stu-id="83323-116">Only Microsoft Edge and Internet Explorer (on a supported version of Microsoft Windows) support ClickOnce applications.</span></span> <span data-ttu-id="83323-117">ワークフロー エディタ ClickOnce アプリケーションには、64 ビットの互換性のあるオペレーティング システムが必要です。</span><span class="sxs-lookup"><span data-stu-id="83323-117">The Workflow Editor ClickOnce application requires a 64-bit compatible operating system.</span></span>
> * <span data-ttu-id="83323-118">PDF ファイルをプレビューするには、Windows 10 の Microsoft Edge (公開されている最新のバージョン)、もしくは Windows 10、Windows 8.1、Windows 8、Windows 7、または Google Nexus 10 タブレットの Google Chrome (公開されている最新のバージョン) などの最新のブラウザを使用することをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="83323-118">To preview PDF files, we recommend that you use modern browsers like Microsoft Edge (latest publicly available version) on Windows 10, or Google Chrome (latest publicly available version) on Windows 10, Windows 8.1, Windows 8, Windows 7, or Google Nexus 10 tablet.</span></span>
>   <span data-ttu-id="83323-119">ネットワーク要件</span><span class="sxs-lookup"><span data-stu-id="83323-119">Network requirements</span></span>
> * <span data-ttu-id="83323-120">Dynamics 365 for Talent は、待機時間が 250 ～ 300 ミリ秒 (ms) 以下のネットワーク用に設計されています。</span><span class="sxs-lookup"><span data-stu-id="83323-120">Dynamics 365 for Talent is designed for networks with latency of 250-300 milliseconds (ms) or less.</span></span> <span data-ttu-id="83323-121">これは、ブラウザー クライアントから Dynamics 365 for Talent をホストする Microsoft Azure データ センターまでの待機時間のことです。</span><span class="sxs-lookup"><span data-stu-id="83323-121">This is the latency from a browser client to the Microsoft Azure data center that hosts Dynamics 365 for Talent.</span></span> <span data-ttu-id="83323-122">[www.azurespeed.com](https://www.azurespeed.com "Azure Latency Test") でネットワーク待機時間をテストすることをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="83323-122">We recommend that you test network latency at [www.azurespeed.com](https://www.azurespeed.com "Azure Latency Test").</span></span>
> * <span data-ttu-id="83323-123">Dynamics 365 for Talent に対する帯域幅の要件は、シナリオによって異なります。</span><span class="sxs-lookup"><span data-stu-id="83323-123">Bandwidth requirements for Dynamics 365 for Talent depend on your scenario.</span></span> <span data-ttu-id="83323-124">最も一般的なシナリオでは、毎秒 50 キロバイト (KBps) 以上の帯域幅が必要です。</span><span class="sxs-lookup"><span data-stu-id="83323-124">Most typical scenarios require a bandwidth of more than 50 kilobytes per second (KBps).</span></span>
> 
> [!WARNING]
> <span data-ttu-id="83323-125">ユーザー数に帯域幅要件の最小値を掛けてクライアントの場所からの帯域幅要件を計算しないでください。</span><span class="sxs-lookup"><span data-stu-id="83323-125">Don't compute bandwidth requirements from a client location by multiplying the number of users by the minimum bandwidth requirements.</span></span> <span data-ttu-id="83323-126">特定の場所の同時使用は非常に計算が困難です。</span><span class="sxs-lookup"><span data-stu-id="83323-126">The concurrent usage of a given location is very difficult to calculate.</span></span> <span data-ttu-id="83323-127">帯域幅の要件について懸念する顧客には、Dynamics 365 for Talent のトライアル バージョンを使用します。</span><span class="sxs-lookup"><span data-stu-id="83323-127">For customers who are concerned about bandwidth requirements, use a trial version of Dynamics 365 for Talent.</span></span>

## <a name="supported-microsoft-office-applications"></a><span data-ttu-id="83323-128">サポートされる Microsoft Office アプリケーション</span><span class="sxs-lookup"><span data-stu-id="83323-128">Supported Microsoft Office applications</span></span>

* <span data-ttu-id="83323-129">Microsoft Excel と Word のアドインを実行するには、Windows または Mac 用の Microsoft Office 2016 をインストールしておく必要があります。</span><span class="sxs-lookup"><span data-stu-id="83323-129">To run the Microsoft Excel and Word add-ins, you must have Microsoft Office 2016 for Windows or Mac installed.</span></span> <span data-ttu-id="83323-130">バージョン要件の詳細については、[Office 統合トラブルシューティング](../dev-itpro/office-integration/office-integration-troubleshooting.md "Office 統合トラブルシューティング") を参照してください。</span><span class="sxs-lookup"><span data-stu-id="83323-130">For more details about version requirements, see [Office integration troubleshooting](../dev-itpro/office-integration/office-integration-troubleshooting.md "Office integration troubleshooting").</span></span>
* <span data-ttu-id="83323-131">Excel にエクスポートまたはWord にエクスポート機能によって生成されたドキュメントを表示するには、Microsoft Office 2007 以降をインストールしておく必要があります。</span><span class="sxs-lookup"><span data-stu-id="83323-131">To view documents that are generated by the Export to Excel or Export to Word functionality, you must have Microsoft Office 2007 or later installed.</span></span>

## <a name="update-policy"></a><span data-ttu-id="83323-132">更新ポリシー</span><span class="sxs-lookup"><span data-stu-id="83323-132">Update policy</span></span>

<span data-ttu-id="83323-133">Microsoft Dynamics 365 for Talent はクラウドの提供としてサービスされます。</span><span class="sxs-lookup"><span data-stu-id="83323-133">Microsoft Dynamics 365 for Talent is serviced as a cloud offering.</span></span> <span data-ttu-id="83323-134">Dynamics 365 for Talent の更新は、Microsoft によって連続的かつ自動的に適用されます。</span><span class="sxs-lookup"><span data-stu-id="83323-134">Updates to Dynamics 365 for Talent are continuous and applied automatically by Microsoft.</span></span>

<span data-ttu-id="83323-135">更新プログラムは一定の調子でリリースされ、すべての環境で行われます。</span><span class="sxs-lookup"><span data-stu-id="83323-135">Updates are released on a regular cadence, updates will be made to all environments.</span></span>  <span data-ttu-id="83323-136">Dynamics 365 for Talent は、[Microsoft Support Lifecycle ポリシー](https://support.microsoft.com/en-us/gp/lifecycle#gp/OSSLpolicy "Microsoft Support Lifecycle") に従ってサポートされています。ここでは、製品サポートの使用可能性における一貫した予測可能なガイドラインを提供します。</span><span class="sxs-lookup"><span data-stu-id="83323-136">Dynamics 365 for Talent is supported according to the [Microsoft Support Lifecycle policy](https://support.microsoft.com/en-us/gp/lifecycle#gp/OSSLpolicy "Microsoft Support Lifecycle"), which provides consistent and predictable guidelines for product support availability.</span></span>
