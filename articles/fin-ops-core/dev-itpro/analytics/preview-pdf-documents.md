---
title: PDF ビューアを使用して PDF ドキュメントをプレビューする
description: このトピックでは、ビジネスドキュメントを表示するにあたり、埋め込みPDFプレビューオプションを使用する方法について説明します。
author: tjvass
manager: AnnBe
ms.date: 07/22/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: IT Pro
ms.reviewer: kfend
ms.search.region: Global
ms.author: tjvass
ms.search.validFrom: 2019-05-21
ms.dyn365.ops.version: Platform update 28
ms.openlocfilehash: fff8347a235fc9a863fad51967f4ab55e381d682
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 12/05/2020
ms.locfileid: "4680578"
---
# <a name="preview-pdf-documents-using-a-pdf-viewer"></a><span data-ttu-id="6e978-103">PDF ビューアを使用した PDF ドキュメントのプレビュー</span><span class="sxs-lookup"><span data-stu-id="6e978-103">Preview PDF documents using a PDF viewer</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="6e978-104">埋め込み PDF プレビュー オプションを利用することにより、ビジネス ドキュメントの作成にまつわるアプリケーション エクスペリエンスを合理化することができます。</span><span class="sxs-lookup"><span data-stu-id="6e978-104">Streamline application experiences that result in the production of business documents by taking advantage of the embedded PDF Preview option.</span></span> <span data-ttu-id="6e978-105">Finance and Operations アプリケーションは、本サービスによって作成されたビジネスドキュメントをプレビューするにあたって最新のエクスペリエンスをお届けします。</span><span class="sxs-lookup"><span data-stu-id="6e978-105">Finance and Operations applications deliver a modern experience to preview business documents that are produced by the service.</span></span> <span data-ttu-id="6e978-106">組み込みのツールバーを使用することで、ドキュメントの閲覧やダウンロード、またはローカルに接続されている機器での印刷ができます。</span><span class="sxs-lookup"><span data-stu-id="6e978-106">You can use the built-in toolbar to navigate and download the document or to print to locally connected devices.</span></span>

<span data-ttu-id="6e978-107">埋め込みのビューアーを使うと、画面条の表示内容と印刷された内容に整合性を持たせることができます。</span><span class="sxs-lookup"><span data-stu-id="6e978-107">The embedded viewer offers consistency between the screen presentation and the printed output.</span></span> <span data-ttu-id="6e978-108">加えて、従来の操作と比較してレポートの表示時間が大幅に短縮されます。</span><span class="sxs-lookup"><span data-stu-id="6e978-108">In addition, report viewing times are drastically reduced when compared to the legacy experience.</span></span> <span data-ttu-id="6e978-109">Preview オプションは対応するすべての機器での使用が可能であり、サードパーティ製のソフトウェアを追加する必要はありません。</span><span class="sxs-lookup"><span data-stu-id="6e978-109">The Preview option is available on all supported devices and does not require any additional third-party software.</span></span> <span data-ttu-id="6e978-110">組み込みのビューア ツールバー オプションを使用すると、ドキュメントのダウンロードおよび閲覧が簡単になります。</span><span class="sxs-lookup"><span data-stu-id="6e978-110">Documents can be easily downloaded and navigated by using the built-in viewer toolbar options.</span></span>

<span data-ttu-id="6e978-111">次の図は、最新のビジネスドキュメントをプレビューした例です。</span><span class="sxs-lookup"><span data-stu-id="6e978-111">The following illustration shows a preview of the experience with a modern business document.</span></span>
<span data-ttu-id="6e978-112">![PDFプレビュー フォーム](./media/pdf-document-preview.png)</span><span class="sxs-lookup"><span data-stu-id="6e978-112">![PDF preview form](./media/pdf-document-preview.png)</span></span>

<span data-ttu-id="6e978-113">従来のHTMLベースのプレビューは、実物のドキュメントに即したプレビューへと取って代わります。</span><span class="sxs-lookup"><span data-stu-id="6e978-113">The legacy HTML-based preview experience is being replaced by a true document preview experience.</span></span> <span data-ttu-id="6e978-114">最新のPDFプレビュー機能には、いくつかの重要な特徴があります。</span><span class="sxs-lookup"><span data-stu-id="6e978-114">There are several key advantages in the modern PDF preview experience.</span></span> <span data-ttu-id="6e978-115">以下のような特徴を持っています:</span><span class="sxs-lookup"><span data-stu-id="6e978-115">These advantages include:</span></span>

- <span data-ttu-id="6e978-116">画面上に表示された内容を忠実に印刷処理します。</span><span class="sxs-lookup"><span data-stu-id="6e978-116">A fidelity between the screen presentation and the printed output.</span></span>
- <span data-ttu-id="6e978-117">オンプレミス配置を含む、さまざまなデバイスおよびプラットフォーム上であっても、常に整合したドキュメントレポートプレビューを提供します。</span><span class="sxs-lookup"><span data-stu-id="6e978-117">A consistent document report preview experience across devices and platforms, including on-premises deployments.</span></span>
- <span data-ttu-id="6e978-118">サーバーサイド レンダリングにより、ドキュメントを作成する際の効率が向上します。</span><span class="sxs-lookup"><span data-stu-id="6e978-118">The server-side rendering improves the performance when producing the document.</span></span>
- <span data-ttu-id="6e978-119">組み込みツールによって、ビジネスドキュメントの内容をすばやく閲覧することができます。</span><span class="sxs-lookup"><span data-stu-id="6e978-119">A built-in tooling that allows users to quickly navigate the contents of the business document.</span></span>

## <a name="accessing-the-pdf-preview-experience-platform-update-36-or-later"></a><span data-ttu-id="6e978-120">PDF プレビュー機能へのアクセス (プラットフォーム更新プログラム 36 以降)</span><span class="sxs-lookup"><span data-stu-id="6e978-120">Accessing the PDF preview experience (Platform update 36 or later)</span></span>
<span data-ttu-id="6e978-121">PDF プレビュー エクスペリエンスは、既定では [セルフサービス配置](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/infrastructure-stack) およびプラットフォーム更新プログラム 39 またはそれ以降でホストされている環境で有効化されます。</span><span class="sxs-lookup"><span data-stu-id="6e978-121">The PDF preview experience is enabled by default in [Self-Service deployments](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/infrastructure-stack) and in environments hosted on Platform update 39 or later.</span></span> <span data-ttu-id="6e978-122">プラットフォーム更新プログラム 36 から 38 を実行していて、クラウドでホストされている環境および Microsoft が管理する環境で PDF プレビュー エクスペリエンスを使用するには、機能管理を使用して **レポート PDF ビューアー** 機能を有効にします。</span><span class="sxs-lookup"><span data-stu-id="6e978-122">To use the PDF preview experience in cloud-hosted and Microsoft-managed environments running Platform updates 36 thru 38, use Feature Management to enable the **Report PDF viewer** feature.</span></span>

## <a name="additional-feature-information"></a><span data-ttu-id="6e978-123">追加の機能</span><span class="sxs-lookup"><span data-stu-id="6e978-123">Additional feature information</span></span>
- <span data-ttu-id="6e978-124">既定では、展開/折りたたみが可能なセクションが用意されています。</span><span class="sxs-lookup"><span data-stu-id="6e978-124">Expandable/collapsible sections are available by default.</span></span> <span data-ttu-id="6e978-125">これらのインタラクティブな操作は、PDFドキュメントが作成された後には機能しなくなります。</span><span class="sxs-lookup"><span data-stu-id="6e978-125">These interactive operations do not function after the PDF document has been created.</span></span>
- <span data-ttu-id="6e978-126">プリンターのドロップダウンメニューから、ローカル接続されている機器を選択することができます。</span><span class="sxs-lookup"><span data-stu-id="6e978-126">The printer drop-down menu allows users to choose from locally connected devices.</span></span> <span data-ttu-id="6e978-127">ここで表示されるリストには、サービスを通じて接続されるネットワークプリンターは含まれません。</span><span class="sxs-lookup"><span data-stu-id="6e978-127">This list does not include network printers connected through the service.</span></span>
- <span data-ttu-id="6e978-128">ドキュメントは組み込みツールバーのアクションを使用してローカルデバイスにダウンロードされます。</span><span class="sxs-lookup"><span data-stu-id="6e978-128">Documents are downloaded to the local device using the built-in toolbar actions.</span></span>
- <span data-ttu-id="6e978-129">PDF以外の形式のドキュメントを作成するには、 **印刷先** オプションを使用します。</span><span class="sxs-lookup"><span data-stu-id="6e978-129">Use the **Print destination** options to produce documents in formats other than PDF.</span></span>

## <a name="feature-limitations"></a><span data-ttu-id="6e978-130">機能の制限</span><span class="sxs-lookup"><span data-stu-id="6e978-130">Feature limitations</span></span>
<span data-ttu-id="6e978-131">埋め込み PDF ビューアー エクスペリエンスでは、ドキュメントの印刷出力と完全に一致する終了済ドキュメントが提供されます。</span><span class="sxs-lookup"><span data-stu-id="6e978-131">The Embedded PDF viewer experience delivers a closed document that exactly matches the printed output of the document.</span></span>  <span data-ttu-id="6e978-132">受信者はこれらのドキュメントを変更できないため、業務運営に適した形式になります。</span><span class="sxs-lookup"><span data-stu-id="6e978-132">These documents cannot be modified by the recipient making the format ideal for business operations.</span></span>  <span data-ttu-id="6e978-133">ただし、終了済形式のため、HTML プレゼンテーションと比較すると画面上のドキュメントの対話性がはるかに低くなります。</span><span class="sxs-lookup"><span data-stu-id="6e978-133">However, as a closed format, the documents are far less interactive on the screen when compared to HTML presentations.</span></span>  <span data-ttu-id="6e978-134">埋め込み PDF ビューアーを使用してドキュメントをプレビューする場合、次のエンド ユーザー機能はサポートされません。</span><span class="sxs-lookup"><span data-stu-id="6e978-134">The following end-user capabilities are not supported when previewing documents using the embedded PDF viewer.</span></span>

- <span data-ttu-id="6e978-135">既定では、埋め込みドリルスルー ナビゲーションは、PDF ドキュメントのプレビュー時のみ使用可能です。</span><span class="sxs-lookup"><span data-stu-id="6e978-135">By default, embedded drill-thru navigation links are only available while previewing PDF documents.</span></span>
- <span data-ttu-id="6e978-136">PDF ドキュメントでは、展開および折りたたみ可能なセクションはサポートされません。</span><span class="sxs-lookup"><span data-stu-id="6e978-136">PDF documents do not support expandable and collapsible sections.</span></span> 
