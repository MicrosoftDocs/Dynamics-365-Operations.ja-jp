---
title: ドキュメント レポートのプレビュー オプション
description: このトピックでは、埋め込みドキュメント レポート プレビューアーで使用できるオプションについて説明します。
author: tjvass
manager: AnnBe
ms.date: 09/11/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: IT Pro
ms.reviewer: kfend
ms.search.scope: Operations
ms.search.region: Global
ms.author: tjvass
ms.search.validFrom: 2020-06-21
ms.dyn365.ops.version: Platform update 34
ms.openlocfilehash: 87e294ba26358d7336bf5b95ba1f8cef184775b4
ms.sourcegitcommit: b6d255a53754ed97e17a5cf5eb23383e46584060
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/12/2020
ms.locfileid: "3796944"
---
# <a name="document-reporting-preview-options"></a><span data-ttu-id="3548e-103">ドキュメント レポートのプレビュー オプション</span><span class="sxs-lookup"><span data-stu-id="3548e-103">Document reporting preview options</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="3548e-104">Finance and Operations アプリは、埋め込み PDF ビューアーでのドキュメントのプレビュー時に使用するオプションをさらに拡張して提供します。</span><span class="sxs-lookup"><span data-stu-id="3548e-104">Finance and Operations apps offer an expanded collection of options to use while previewing documents within the embedded PDF viewer.</span></span> <span data-ttu-id="3548e-105">このトピックでは、**エクスポート**と**ネットワーク プリンター** オプションについて説明します。</span><span class="sxs-lookup"><span data-stu-id="3548e-105">This topic describes the **Export** and **Network Printer** options.</span></span>

## <a name="overview"></a><span data-ttu-id="3548e-106">概要</span><span class="sxs-lookup"><span data-stu-id="3548e-106">Overview</span></span>
<span data-ttu-id="3548e-107">ドキュメントの発行と配分を効率的に行うことは、多くの業務にとって重要なコンポーネントであるだけでなく、日々のビジネス機能にとっても重要です。</span><span class="sxs-lookup"><span data-stu-id="3548e-107">The efficient publication and distribution of documents is not only a key component to many operations, but it’s also critical to daily business functions.</span></span> <span data-ttu-id="3548e-108">ドキュメントは、トランザクションの詳細を把握するために使用されます。また、2 当事者間の合意を表す場合もあります。</span><span class="sxs-lookup"><span data-stu-id="3548e-108">Documents are used to capture transaction details and may represent an agreement between two parties.</span></span> <span data-ttu-id="3548e-109">見積書から最終的な領収書と顧客明細書が発生する梱包明細プロセスで使用された売上請求書に至るまで、ビジネス ドキュメントはさまざまな形式で使用されます。</span><span class="sxs-lookup"><span data-stu-id="3548e-109">From quotations to sales invoices used in the packing slip process, which ultimately produces receipts and customer statements, business documents come in many forms.</span></span> <span data-ttu-id="3548e-110">ドキュメントのレポート プレビュー オプションを使用すると、ドキュメントに対して適切なアクションをすばやく実行することができます。</span><span class="sxs-lookup"><span data-stu-id="3548e-110">The document reporting preview options empower you to quickly take the appropriate action on documents.</span></span>

![ドキュメントのプレビューアー ユーザー オプション](./media/Document-preview-options-toolbar.png)

<span data-ttu-id="3548e-112">ドキュメントすべての相互作用のほぼ半数は、画面プレビューに関連しています。</span><span class="sxs-lookup"><span data-stu-id="3548e-112">Almost half of all document interactions involve the screen preview.</span></span> <span data-ttu-id="3548e-113">使用可能なツールバー オプションは、サポートされているすべてのデバイスに対応しており、Finance and Operations アプリケーションによって表示されるドキュメントをエクスポートおよび印刷するためのシンプルで直観的なソリューションを提供します。</span><span class="sxs-lookup"><span data-stu-id="3548e-113">The toolbar options that are available are for all supported devices and offer a simple and intuitive solution for exporting and printing documents rendered by Finance and Operations apps.</span></span>

## <a name="file-export"></a><span data-ttu-id="3548e-114">ファイルのエクスポート</span><span class="sxs-lookup"><span data-stu-id="3548e-114">File export</span></span>
<span data-ttu-id="3548e-115">追加のユーザー オプションは、HTML ベースの**レポート ビューワー** コントロールで以前提供されていた機能に取って代わります。</span><span class="sxs-lookup"><span data-stu-id="3548e-115">Additional user options replace functions previously supplied by the HTML-based **Report viewer** control.</span></span> <span data-ttu-id="3548e-116">これらのツールバー オプションを使用して、サポートされているさまざまな形式のファイルをエクスポートできます。</span><span class="sxs-lookup"><span data-stu-id="3548e-116">You can use these toolbar options to export files to the various  supported formats.</span></span> <span data-ttu-id="3548e-117">これには、Microsoft Word、Excel、HTML、CSV などが含まれます。</span><span class="sxs-lookup"><span data-stu-id="3548e-117">This includes Microsoft Word, Excel, HTML, CSV, and more.</span></span> <span data-ttu-id="3548e-118">プリンター出力と一貫したレイアウトにするために、新しいモダン エクスペリエンスでは PDF ページネーション ルールを使用したドキュメントが表示されます。</span><span class="sxs-lookup"><span data-stu-id="3548e-118">To ensure a consistent layout with the printer output, the new modern experience displays documents using the PDF pagination rules.</span></span> <span data-ttu-id="3548e-119">詳細については、[レポートでのページネーション](https://docs.microsoft.com/sql/reporting-services/report-design/pagination-in-reporting-services-report-builder-and-ssrs?view=sql-server-ver15)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="3548e-119">For more information, see [Pagination in reports](https://docs.microsoft.com/sql/reporting-services/report-design/pagination-in-reporting-services-report-builder-and-ssrs?view=sql-server-ver15).</span></span>

## <a name="network-printing"></a><span data-ttu-id="3548e-120">ネットワーク印刷</span><span class="sxs-lookup"><span data-stu-id="3548e-120">Network printing</span></span>
<span data-ttu-id="3548e-121">**印刷**ボタンを使用してローカルに接続されたデバイスに印刷するか、またはツールバー オプションを使用してドキュメントをネットワーク プリンターに直接送信するかを選択できます。</span><span class="sxs-lookup"><span data-stu-id="3548e-121">You can choose to print on locally connected devices using the **Print** button or send documents directly to network printers using the toolbar option.</span></span> <span data-ttu-id="3548e-122">ネットワーク印刷 オプションを使用すると、携帯電話などのインターネットに接続されたほとんどのデバイスからリモートでの作業中に、ネットワーク接続されたプリンターに対して印刷手順を開始できます。</span><span class="sxs-lookup"><span data-stu-id="3548e-122">Using the network print option, you can initiate print instructions to network connected printers while working remotely from nearly any internet connected device, including mobile phones.</span></span>

<span data-ttu-id="3548e-123">ツールバー オプションを使用して、ネットワーク プリンターを選択し、印刷設定を確立します。</span><span class="sxs-lookup"><span data-stu-id="3548e-123">Use the toolbar option to choose the network printer and establish print settings.</span></span>

![出力先設定へのアクセス](./media/Document-preview-network-print-options.png)

## <a name="access-preview-options"></a><span data-ttu-id="3548e-125">プレビュー オプションへのアクセス</span><span class="sxs-lookup"><span data-stu-id="3548e-125">Access preview options</span></span>
<span data-ttu-id="3548e-126">機能管理領域を使用して、ドキュメント プレビュー オプションにアクセスします。</span><span class="sxs-lookup"><span data-stu-id="3548e-126">Use the Feature Management area to access the document preview options.</span></span> <span data-ttu-id="3548e-127">次の 2 つの追加機能があります。</span><span class="sxs-lookup"><span data-stu-id="3548e-127">The two additional features are:</span></span>
- <span data-ttu-id="3548e-128">**レポート PDF ビューアーでのエクスポートを有効にする**</span><span class="sxs-lookup"><span data-stu-id="3548e-128">**Enable Export on Report PDF viewer**</span></span>
- <span data-ttu-id="3548e-129">**レポート PDF ビューアーでのネットワーク印刷を有効にする**</span><span class="sxs-lookup"><span data-stu-id="3548e-129">**Enable Network Printing on Report PDF viewer**</span></span>

<span data-ttu-id="3548e-130">これらの機能を選択し、**今すぐ有効にする**を選択して、新しいユーザー オプションを利用します。</span><span class="sxs-lookup"><span data-stu-id="3548e-130">Select these features, and then select **Enable now** to begin taking advantage of the new user options.</span></span> <span data-ttu-id="3548e-131">詳細については [機能管理の概要](../../fin-ops/get-started/feature-management/feature-management-overview.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="3548e-131">For more information, see [Feature management overview](../../fin-ops/get-started/feature-management/feature-management-overview.md).</span></span>
