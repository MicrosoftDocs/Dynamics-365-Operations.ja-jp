---
title: Talent のシステム要件
description: このトピックは、Dynamics 365 Talent の要件を一覧表示します。
author: andreabichsel
manager: AnnBe
ms.date: 10/21/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: anbichse
ms.search.scope: Core, Operations, Talent
ms.custom: 63213
ms.assetid: 5dbc62fc-0184-4c0e-9856-e735fc68799e
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: July 2017 update
ms.openlocfilehash: 509827d5736887f56e7754a0760af7dea76277f7
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/13/2020
ms.locfileid: "4461741"
---
# <a name="talent-system-requirements"></a><span data-ttu-id="e7e3a-103">Talent のシステム要件</span><span class="sxs-lookup"><span data-stu-id="e7e3a-103">Talent system requirements</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="e7e3a-104">このトピックでは、Attract および Onboard を含む、Microsoft Dynamics 365 Talent の要件について説明します。</span><span class="sxs-lookup"><span data-stu-id="e7e3a-104">This topic describes requirements for Microsoft Dynamics 365 Talent, including Attract and Onboard.</span></span> <span data-ttu-id="e7e3a-105">また、Talent が利用可能な国および地域、Talent データの言語とローカライズの概要について説明します。</span><span class="sxs-lookup"><span data-stu-id="e7e3a-105">It also outlines the countries and regions where Talent is available, plus information about languages and localization for Talent data.</span></span> <span data-ttu-id="e7e3a-106">さらに、このトピックでは Talent の更新ポリシーについて説明します。</span><span class="sxs-lookup"><span data-stu-id="e7e3a-106">In additions, this topic provides the update policy for Talent.</span></span>

## <a name="supported-web-browsers"></a><span data-ttu-id="e7e3a-107">サポートされている Web ブラウザー</span><span class="sxs-lookup"><span data-stu-id="e7e3a-107">Supported web browsers</span></span>

<span data-ttu-id="e7e3a-108">Microsoft Dynamics 365 Talent は、指定されたオペレーティング システムで実行される次のすべての Web ブラウザで実行できます。</span><span class="sxs-lookup"><span data-stu-id="e7e3a-108">Microsoft Dynamics 365 Talent can run in any of the following web browsers that run on the specified operating systems:</span></span> 

*   <span data-ttu-id="e7e3a-109">Windows 10 の Microsoft Edge (公開されている最新のバージョン)</span><span class="sxs-lookup"><span data-stu-id="e7e3a-109">Microsoft Edge (latest publicly available version) on Windows 10</span></span>
*   <span data-ttu-id="e7e3a-110">Windows 10、Windows 8.1、または Windows 7 の Internet Explorer 11</span><span class="sxs-lookup"><span data-stu-id="e7e3a-110">Internet Explorer 11 on Windows 10, Windows 8.1, or Windows 7</span></span>
*   <span data-ttu-id="e7e3a-111">Google Chrome (公開されている最新バージョン)</span><span class="sxs-lookup"><span data-stu-id="e7e3a-111">Google Chrome (latest publicly available version)</span></span>
*   <span data-ttu-id="e7e3a-112">Apple Safari (公開されている最新バージョン)</span><span class="sxs-lookup"><span data-stu-id="e7e3a-112">Apple Safari (latest publicly available version)</span></span>

<span data-ttu-id="e7e3a-113">各 Web ブラウザの最新版を検索するには、ソフトウェア メーカーの Web サイトに移動します。</span><span class="sxs-lookup"><span data-stu-id="e7e3a-113">To find the latest release for each web browser, go to the software manufacturer’s website.</span></span> 

> [!NOTE]
> * <span data-ttu-id="e7e3a-114">タスク レコーダーから生成される画像をキャプチャして Microsoft Word ドキュメントに含めるには、Chrome 拡張機能をインストールする必要があります。</span><span class="sxs-lookup"><span data-stu-id="e7e3a-114">To capture images that are generated from Task Recorder and include them in Microsoft Word documents, you must have a Chrome extension installed.</span></span> 
> * <span data-ttu-id="e7e3a-115">ワークフロー エディターは ClickOnce アプリケーションとして起動されます。</span><span class="sxs-lookup"><span data-stu-id="e7e3a-115">The Workflow Editor is started as a ClickOnce application.</span></span> <span data-ttu-id="e7e3a-116">Microsoft Edge と Internet Explorer (Microsoft Windows のサポートされているバージョン) のみが、ClickOnce アプリケーションをサポートします。</span><span class="sxs-lookup"><span data-stu-id="e7e3a-116">Only Microsoft Edge and Internet Explorer (on a supported version of Microsoft Windows) support ClickOnce applications.</span></span> <span data-ttu-id="e7e3a-117">ワークフロー エディタ ClickOnce アプリケーションには、64 ビットの互換性のあるオペレーティング システムが必要です。</span><span class="sxs-lookup"><span data-stu-id="e7e3a-117">The Workflow Editor ClickOnce application requires a 64-bit compatible operating system.</span></span>
> * <span data-ttu-id="e7e3a-118">PDF ファイルをプレビューするには、Windows 10 の Microsoft Edge (公開されている最新のバージョン)、もしくは Windows 10、Windows 8.1、Windows 8、Windows 7、または Google Nexus 10 タブレットの Google Chrome (公開されている最新のバージョン) などの最新のブラウザを使用することをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="e7e3a-118">To preview PDF files, we recommend that you use modern browsers like Microsoft Edge (latest publicly available version) on Windows 10, or Google Chrome (latest publicly available version) on Windows 10, Windows 8.1, Windows 8, Windows 7, or Google Nexus 10 tablet.</span></span>
>   <span data-ttu-id="e7e3a-119">ネットワーク要件</span><span class="sxs-lookup"><span data-stu-id="e7e3a-119">Network requirements</span></span>
> * <span data-ttu-id="e7e3a-120">Dynamics 365 Talent は、待機時間が 250 ～ 300 ミリ秒 (ms) 以下のネットワーク用に設計されています。</span><span class="sxs-lookup"><span data-stu-id="e7e3a-120">Dynamics 365 Talent is designed for networks with latency of 250-300 milliseconds (ms) or less.</span></span> <span data-ttu-id="e7e3a-121">これは、ブラウザー クライアントから Talent をホストする Microsoft Azure データ センターまでの待機時間のことです。</span><span class="sxs-lookup"><span data-stu-id="e7e3a-121">This is the latency from a browser client to the Microsoft Azure data center that hosts Talent.</span></span> <span data-ttu-id="e7e3a-122">[www.azurespeed.com](https://www.azurespeed.com "Azure Latency Test") にてネットワークの待機時間をテストすることをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="e7e3a-122">We recommend that you test network latency at [www.azurespeed.com](https://www.azurespeed.com "Azure Latency Test").</span></span>
> * <span data-ttu-id="e7e3a-123">Talent に対する帯域幅の要件は、シナリオによって異なります。</span><span class="sxs-lookup"><span data-stu-id="e7e3a-123">Bandwidth requirements for Talent depend on your scenario.</span></span> <span data-ttu-id="e7e3a-124">最も一般的なシナリオでは、毎秒 50 キロバイト (KBps) 以上の帯域幅が必要です。</span><span class="sxs-lookup"><span data-stu-id="e7e3a-124">Most typical scenarios require a bandwidth of more than 50 kilobytes per second (KBps).</span></span>
> 
> [!WARNING]
> <span data-ttu-id="e7e3a-125">ユーザー数に帯域幅要件の最小値を掛けてクライアントの場所からの帯域幅要件を計算しないでください。</span><span class="sxs-lookup"><span data-stu-id="e7e3a-125">Don't compute bandwidth requirements from a client location by multiplying the number of users by the minimum bandwidth requirements.</span></span> <span data-ttu-id="e7e3a-126">特定の場所の同時使用は非常に計算が困難です。</span><span class="sxs-lookup"><span data-stu-id="e7e3a-126">The concurrent usage of a given location is very difficult to calculate.</span></span> <span data-ttu-id="e7e3a-127">帯域幅の要件について懸念する顧客には、Talent のトライアル バージョンを使用します。</span><span class="sxs-lookup"><span data-stu-id="e7e3a-127">For customers who are concerned about bandwidth requirements, use a trial version of Talent.</span></span>

## <a name="supported-microsoft-office-applications"></a><span data-ttu-id="e7e3a-128">サポートされる Microsoft Office アプリケーション</span><span class="sxs-lookup"><span data-stu-id="e7e3a-128">Supported Microsoft Office applications</span></span>

* <span data-ttu-id="e7e3a-129">Microsoft Excel と Word のアドインを実行するには、Windows または Mac 用の Microsoft Office 2016 をインストールしておく必要があります。</span><span class="sxs-lookup"><span data-stu-id="e7e3a-129">To run the Microsoft Excel and Word add-ins, you must have Microsoft Office 2016 for Windows or Mac installed.</span></span> <span data-ttu-id="e7e3a-130">バージョン要件の詳細については、[Office 統合トラブルシューティング](../dev-itpro/office-integration/office-integration-troubleshooting.md "Office 統合のトラブルシューティング") を参照してください。</span><span class="sxs-lookup"><span data-stu-id="e7e3a-130">For more details about version requirements, see [Office integration troubleshooting](../dev-itpro/office-integration/office-integration-troubleshooting.md "Office integration troubleshooting").</span></span>
* <span data-ttu-id="e7e3a-131">Excel にエクスポートまたはWord にエクスポート機能によって生成されたドキュメントを表示するには、Microsoft Office 2007 以降をインストールしておく必要があります。</span><span class="sxs-lookup"><span data-stu-id="e7e3a-131">To view documents that are generated by the Export to Excel or Export to Word functionality, you must have Microsoft Office 2007 or later installed.</span></span>

## <a name="regional-availability-languages-and-localization"></a><span data-ttu-id="e7e3a-132">地域の使用可用性、言語、およびローカライズ</span><span class="sxs-lookup"><span data-stu-id="e7e3a-132">Regional availability, languages, and localization</span></span>

<span data-ttu-id="e7e3a-133">Talent がサポートする国、地域、および言語に関する PDF ファイルを [Microsoft Dynamics 365 の国際可用性ガイド](https://docs.microsoft.com/dynamics365/get-started/availability) からダウンロードすることができます。</span><span class="sxs-lookup"><span data-stu-id="e7e3a-133">You can download a PDF file of the countries, regions, and languages Talent supports at [International availability of Microsoft Dynamics 365](https://docs.microsoft.com/dynamics365/get-started/availability).</span></span> 

> [!NOTE]
> <span data-ttu-id="e7e3a-134">ユーザー インターフェイスは他の言語にローカライズされますが、ユーザーデータすべては入力された言語で保存されます。</span><span class="sxs-lookup"><span data-stu-id="e7e3a-134">While the user interface is localized into other languages, all user data is stored in the language in which it was entered.</span></span> <span data-ttu-id="e7e3a-135">電子メールおよびテンプレートは他の言語で作成できますが、スケジューリング情報などのデータは、現時点では英語でのみ使用可能です。</span><span class="sxs-lookup"><span data-stu-id="e7e3a-135">You can create emails and templates in other languages, but data such as scheduling information is only available in English at this time.</span></span>

<span data-ttu-id="e7e3a-136">国や地域固有のカスタマイズの作成、または現在 Microsoft にサポートされていない国や地域用のソリューションの作成に関心のある開発者は、[グローバリゼーション](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/lcs-solutions/country-region) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="e7e3a-136">If you're a developer interested in creating country- or region-specific customizations, or in creating a solution for a country or region not currently supported by Microsoft, see [Globalization](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/lcs-solutions/country-region).</span></span>

