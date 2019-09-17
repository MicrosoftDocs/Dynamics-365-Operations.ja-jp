---
title: Talent システム要件と更新ポリシー
description: このトピックは、Dynamics 365 for Talent の要件を一覧表示します。 同様に、その更新ポリシーについても説明します。
author: andreabichsel
manager: AnnBe
ms.date: 05/02/2019
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
ms.openlocfilehash: 6c881bf25e7145228ccf7ef73a7ef3637c115a49
ms.sourcegitcommit: 45f8cea6ac75bd2f4187380546a201c056072c59
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 07/12/2019
ms.locfileid: "1741778"
---
# <a name="talent-system-requirements-and-update-policy"></a><span data-ttu-id="2aec3-104">Talent システム要件と更新ポリシー</span><span class="sxs-lookup"><span data-stu-id="2aec3-104">Talent system requirements and update policy</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="2aec3-105">このトピックでは、Attract、Onboard、および Core HR を含め、Microsoft Dynamics 365 for Talent の要件について説明します。</span><span class="sxs-lookup"><span data-stu-id="2aec3-105">This topic describes requirements for Microsoft Dynamics 365 for Talent, including Attract, Onboard, and Core HR.</span></span> <span data-ttu-id="2aec3-106">また、Talent が利用可能な国および地域、Talent データの言語とローカライズの概要について説明します。</span><span class="sxs-lookup"><span data-stu-id="2aec3-106">It also outlines the countries and regions where Talent is available, plus information about languages and localization for Talent data.</span></span> <span data-ttu-id="2aec3-107">さらに、このトピックでは Talent の更新ポリシーについて説明します。</span><span class="sxs-lookup"><span data-stu-id="2aec3-107">In additions, this topic provides the update policy for Talent.</span></span>

## <a name="supported-web-browsers"></a><span data-ttu-id="2aec3-108">サポートされている Web ブラウザー</span><span class="sxs-lookup"><span data-stu-id="2aec3-108">Supported web browsers</span></span>

<span data-ttu-id="2aec3-109">Microsoft Dynamics 365 for Talent Web アプリケーションは、指定されたオペレーティング システムで実行される次のすべての Web ブラウザで実行できます。</span><span class="sxs-lookup"><span data-stu-id="2aec3-109">The Microsoft Dynamics 365 for Talent web application can run in any of the following web browsers that run on the specified operating systems:</span></span> 

*   <span data-ttu-id="2aec3-110">Windows 10 の Microsoft Edge (公開されている最新のバージョン)</span><span class="sxs-lookup"><span data-stu-id="2aec3-110">Microsoft Edge (latest publicly available version) on Windows 10</span></span>
*   <span data-ttu-id="2aec3-111">Windows 10、Windows 8.1、または Windows 7 の Internet Explorer 11</span><span class="sxs-lookup"><span data-stu-id="2aec3-111">Internet Explorer 11 on Windows 10, Windows 8.1, or Windows 7</span></span>
*   <span data-ttu-id="2aec3-112">Google Chrome (公開されている最新バージョン)</span><span class="sxs-lookup"><span data-stu-id="2aec3-112">Google Chrome (latest publicly available version)</span></span>
*   <span data-ttu-id="2aec3-113">Apple Safari (公開されている最新バージョン)</span><span class="sxs-lookup"><span data-stu-id="2aec3-113">Apple Safari (latest publicly available version)</span></span>

<span data-ttu-id="2aec3-114">各 Web ブラウザの最新版を検索するには、ソフトウェア メーカーの Web サイトに移動します。</span><span class="sxs-lookup"><span data-stu-id="2aec3-114">To find the latest release for each web browser, go to the software manufacturer’s website.</span></span> 

> [!NOTE]
> * <span data-ttu-id="2aec3-115">タスク レコーダーから生成される画像をキャプチャして Microsoft Word ドキュメントに含めるには、Chrome 拡張機能をインストールする必要があります。</span><span class="sxs-lookup"><span data-stu-id="2aec3-115">To capture images that are generated from Task Recorder and include them in Microsoft Word documents, you must have a Chrome extension installed.</span></span> 
> * <span data-ttu-id="2aec3-116">ワークフロー エディターは ClickOnce アプリケーションとして起動されます。</span><span class="sxs-lookup"><span data-stu-id="2aec3-116">The Workflow Editor is started as a ClickOnce application.</span></span> <span data-ttu-id="2aec3-117">Microsoft Edge と Internet Explorer (Microsoft Windows のサポートされているバージョン) のみが、ClickOnce アプリケーションをサポートします。</span><span class="sxs-lookup"><span data-stu-id="2aec3-117">Only Microsoft Edge and Internet Explorer (on a supported version of Microsoft Windows) support ClickOnce applications.</span></span> <span data-ttu-id="2aec3-118">ワークフロー エディタ ClickOnce アプリケーションには、64 ビットの互換性のあるオペレーティング システムが必要です。</span><span class="sxs-lookup"><span data-stu-id="2aec3-118">The Workflow Editor ClickOnce application requires a 64-bit compatible operating system.</span></span>
> * <span data-ttu-id="2aec3-119">PDF ファイルをプレビューするには、Windows 10 の Microsoft Edge (公開されている最新のバージョン)、もしくは Windows 10、Windows 8.1、Windows 8、Windows 7、または Google Nexus 10 タブレットの Google Chrome (公開されている最新のバージョン) などの最新のブラウザを使用することをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="2aec3-119">To preview PDF files, we recommend that you use modern browsers like Microsoft Edge (latest publicly available version) on Windows 10, or Google Chrome (latest publicly available version) on Windows 10, Windows 8.1, Windows 8, Windows 7, or Google Nexus 10 tablet.</span></span>
>   <span data-ttu-id="2aec3-120">ネットワーク要件</span><span class="sxs-lookup"><span data-stu-id="2aec3-120">Network requirements</span></span>
> * <span data-ttu-id="2aec3-121">Dynamics 365 for Talent は、待機時間が 250 ～ 300 ミリ秒 (ms) 以下のネットワーク用に設計されています。</span><span class="sxs-lookup"><span data-stu-id="2aec3-121">Dynamics 365 for Talent is designed for networks with latency of 250-300 milliseconds (ms) or less.</span></span> <span data-ttu-id="2aec3-122">これは、ブラウザー クライアントから Dynamics 365 for Talent をホストする Microsoft Azure データ センターまでの待機時間のことです。</span><span class="sxs-lookup"><span data-stu-id="2aec3-122">This is the latency from a browser client to the Microsoft Azure data center that hosts Dynamics 365 for Talent.</span></span> <span data-ttu-id="2aec3-123">[www.azurespeed.com](https://www.azurespeed.com "Azure Latency Test") でネットワーク待機時間をテストすることをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="2aec3-123">We recommend that you test network latency at [www.azurespeed.com](https://www.azurespeed.com "Azure Latency Test").</span></span>
> * <span data-ttu-id="2aec3-124">Dynamics 365 for Talent に対する帯域幅の要件は、シナリオによって異なります。</span><span class="sxs-lookup"><span data-stu-id="2aec3-124">Bandwidth requirements for Dynamics 365 for Talent depend on your scenario.</span></span> <span data-ttu-id="2aec3-125">最も一般的なシナリオでは、毎秒 50 キロバイト (KBps) 以上の帯域幅が必要です。</span><span class="sxs-lookup"><span data-stu-id="2aec3-125">Most typical scenarios require a bandwidth of more than 50 kilobytes per second (KBps).</span></span>
> 
> [!WARNING]
> <span data-ttu-id="2aec3-126">ユーザー数に帯域幅要件の最小値を掛けてクライアントの場所からの帯域幅要件を計算しないでください。</span><span class="sxs-lookup"><span data-stu-id="2aec3-126">Don't compute bandwidth requirements from a client location by multiplying the number of users by the minimum bandwidth requirements.</span></span> <span data-ttu-id="2aec3-127">特定の場所の同時使用は非常に計算が困難です。</span><span class="sxs-lookup"><span data-stu-id="2aec3-127">The concurrent usage of a given location is very difficult to calculate.</span></span> <span data-ttu-id="2aec3-128">帯域幅の要件について懸念する顧客には、Dynamics 365 for Talent のトライアル バージョンを使用します。</span><span class="sxs-lookup"><span data-stu-id="2aec3-128">For customers who are concerned about bandwidth requirements, use a trial version of Dynamics 365 for Talent.</span></span>

## <a name="supported-microsoft-office-applications"></a><span data-ttu-id="2aec3-129">サポートされる Microsoft Office アプリケーション</span><span class="sxs-lookup"><span data-stu-id="2aec3-129">Supported Microsoft Office applications</span></span>

* <span data-ttu-id="2aec3-130">Microsoft Excel と Word のアドインを実行するには、Windows または Mac 用の Microsoft Office 2016 をインストールしておく必要があります。</span><span class="sxs-lookup"><span data-stu-id="2aec3-130">To run the Microsoft Excel and Word add-ins, you must have Microsoft Office 2016 for Windows or Mac installed.</span></span> <span data-ttu-id="2aec3-131">バージョン要件の詳細については、[Office 統合トラブルシューティング](../dev-itpro/office-integration/office-integration-troubleshooting.md "Office 統合トラブルシューティング") を参照してください。</span><span class="sxs-lookup"><span data-stu-id="2aec3-131">For more details about version requirements, see [Office integration troubleshooting](../dev-itpro/office-integration/office-integration-troubleshooting.md "Office integration troubleshooting").</span></span>
* <span data-ttu-id="2aec3-132">Excel にエクスポートまたはWord にエクスポート機能によって生成されたドキュメントを表示するには、Microsoft Office 2007 以降をインストールしておく必要があります。</span><span class="sxs-lookup"><span data-stu-id="2aec3-132">To view documents that are generated by the Export to Excel or Export to Word functionality, you must have Microsoft Office 2007 or later installed.</span></span>

## <a name="regional-availability-languages-and-localization"></a><span data-ttu-id="2aec3-133">地域の使用可用性、言語、およびローカライズ</span><span class="sxs-lookup"><span data-stu-id="2aec3-133">Regional availability, languages, and localization</span></span>

<span data-ttu-id="2aec3-134">Talent がサポートする国、地域、および言語に関する PDF ファイルを [Microsoft Dynamics 365 の国際可用性ガイド](https://docs.microsoft.com/dynamics365/get-started/availability) からダウンロードすることができます。</span><span class="sxs-lookup"><span data-stu-id="2aec3-134">You can download a PDF file of the countries, regions, and languages Talent supports at [International availability of Microsoft Dynamics 365](https://docs.microsoft.com/dynamics365/get-started/availability).</span></span> 

> [!NOTE]
> <span data-ttu-id="2aec3-135">ユーザー インターフェイスは他の言語にローカライズされますが、ユーザーデータすべては入力された言語で保存されます。</span><span class="sxs-lookup"><span data-stu-id="2aec3-135">While the user interface is localized into other languages, all user data is stored in the language in which it was entered.</span></span> <span data-ttu-id="2aec3-136">電子メールおよびテンプレートは他の言語で作成できますが、スケジューリング情報などのデータは、現時点では英語でのみ使用可能です。</span><span class="sxs-lookup"><span data-stu-id="2aec3-136">You can create emails and templates in other languages, but data such as scheduling information is only available in English at this time.</span></span>

<span data-ttu-id="2aec3-137">国や地域固有のカスタマイズの作成、または現在 Microsoft にサポートされていない国や地域用のソリューションの作成に関心のある開発者は、[グローバリゼーション](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/lcs-solutions/country-region) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="2aec3-137">If you're a developer interested in creating country- or region-specific customizations, or in creating a solution for a country or region not currently supported by Microsoft, see [Globalization](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/lcs-solutions/country-region).</span></span>

## <a name="update-policy"></a><span data-ttu-id="2aec3-138">更新ポリシー</span><span class="sxs-lookup"><span data-stu-id="2aec3-138">Update policy</span></span>

<span data-ttu-id="2aec3-139">Microsoft Dynamics 365 for Talent はクラウドの提供としてサービスされます。</span><span class="sxs-lookup"><span data-stu-id="2aec3-139">Microsoft Dynamics 365 for Talent is serviced as a cloud offering.</span></span> <span data-ttu-id="2aec3-140">Dynamics 365 for Talent の更新は、Microsoft によって連続的かつ自動的に適用されます。</span><span class="sxs-lookup"><span data-stu-id="2aec3-140">Updates to Dynamics 365 for Talent are continuous and applied automatically by Microsoft.</span></span>

<span data-ttu-id="2aec3-141">更新プログラムは一定の調子でリリースされ、すべての環境で行われます。</span><span class="sxs-lookup"><span data-stu-id="2aec3-141">Updates are released on a regular cadence and will be made to all environments.</span></span> <span data-ttu-id="2aec3-142">Dynamics 365 for Talent は、[Microsoft Support Lifecycle ポリシー](https://support.microsoft.com/gp/lifecycle#gp/OSSLpolicy "Microsoft Support Lifecycle") に従ってサポートされています。ここでは、製品サポートの使用可能性における一貫した予測可能なガイドラインを提供します。</span><span class="sxs-lookup"><span data-stu-id="2aec3-142">Dynamics 365 for Talent is supported according to the [Microsoft Support Lifecycle policy](https://support.microsoft.com/gp/lifecycle#gp/OSSLpolicy "Microsoft Support Lifecycle"), which provides consistent and predictable guidelines for product support availability.</span></span>
