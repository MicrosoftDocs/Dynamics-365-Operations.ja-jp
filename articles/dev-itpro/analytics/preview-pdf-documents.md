---
title: 埋め込みビューアを使用してPDFドキュメントのプレビューをする
description: このトピックでは、ビジネスドキュメントを表示するにあたり、埋め込みPDFプレビューオプションを使用する方法について説明します。
author: tjvass
manager: AnnBe
ms.date: 05/21/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: IT Pro
ms.reviewer: kfend
ms.search.scope: Operations
ms.search.region: Global
ms.author: tjvass
ms.search.validFrom: 2019-05-21
ms.dyn365.ops.version: Platform update 28
ms.openlocfilehash: 33c28751eed42ab7a478e02d93385220ecf3568e
ms.sourcegitcommit: 19859d8566a8c7840066b2c10c6b08b67f1b83f4
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/04/2019
ms.locfileid: "1618009"
---
# <a name="preview-pdf-documents-with-an-embedded-viewer"></a><span data-ttu-id="4c16a-103">埋め込みビューアを使用してPDFドキュメントのプレビューをする</span><span class="sxs-lookup"><span data-stu-id="4c16a-103">Preview PDF documents with an embedded viewer</span></span>

[!include[banner](../includes/banner.md)]

[!include[banner](../includes/preview-banner.md)]

<span data-ttu-id="4c16a-104">埋め込みPDFプレビューオプションを利用することにより、ビジネスドキュメントの作成にまつわるアプリケーションエクスペリエンスび効率を上げることができます。</span><span class="sxs-lookup"><span data-stu-id="4c16a-104">You can streamline application experiences that result in the production of business documents by taking advantage of the embedded PDF Preview option.</span></span> <span data-ttu-id="4c16a-105">Microsoft Dynamics 365 for Finance and Operations アプリケーションは、本サービスによって作成されたビジネスドキュメントをプレビューするにあたって最新のエクスペリエンスをお届けします。</span><span class="sxs-lookup"><span data-stu-id="4c16a-105">Microsoft Dynamics 365 for Finance and Operations applications deliver a modern experience to preview business documents that are produced by the service.</span></span> <span data-ttu-id="4c16a-106">組み込みのツールバーを使用することで、ドキュメントの閲覧やダウンロード、またはローカルに接続されている機器での印刷ができます。</span><span class="sxs-lookup"><span data-stu-id="4c16a-106">You can use the built-in toolbar to navigate and download the document or to print to locally connected devices.</span></span>

<span data-ttu-id="4c16a-107">埋め込みのビューアーを使うと、画面条の表示内容と印刷された内容に整合性を持たせることができます。</span><span class="sxs-lookup"><span data-stu-id="4c16a-107">The embedded viewer offers consistency between the screen presentation and the printed output.</span></span> <span data-ttu-id="4c16a-108">加えて、従来の操作と比較してレポートの表示時間が大幅に短縮されます。</span><span class="sxs-lookup"><span data-stu-id="4c16a-108">In addition, report viewing times are drastically reduced when compared to the legacy experience.</span></span> <span data-ttu-id="4c16a-109">Preview オプションは対応するすべての機器での使用が可能であり、サードパーティ製のソフトウェアを追加する必要はありません。</span><span class="sxs-lookup"><span data-stu-id="4c16a-109">The Preview option is available on all supported devices and does not require any additional third-party software.</span></span> <span data-ttu-id="4c16a-110">組み込みのビューア ツールバー オプションを使用すると、ドキュメントのダウンロードおよび閲覧が簡単になります。</span><span class="sxs-lookup"><span data-stu-id="4c16a-110">Documents can be easily downloaded and navigated by using the built-in viewer toolbar options.</span></span>

<span data-ttu-id="4c16a-111">次の図は、最新のビジネスドキュメントをプレビューした例です。</span><span class="sxs-lookup"><span data-stu-id="4c16a-111">The following illustration shows a preview of the experience with a modern business document.</span></span>
<span data-ttu-id="4c16a-112">![PDFプレビュー フォーム](./media/pdf-document-preview.png)</span><span class="sxs-lookup"><span data-stu-id="4c16a-112">![PDF preview form](./media/pdf-document-preview.png)</span></span>

<span data-ttu-id="4c16a-113">従来のHTMLベースのプレビューは、実物のドキュメントに即したプレビューへと取って代わります。</span><span class="sxs-lookup"><span data-stu-id="4c16a-113">The legacy HTML-based preview experience is being replaced by a true document preview experience.</span></span> <span data-ttu-id="4c16a-114">最新のPDFプレビュー機能には、いくつかの重要な特徴があります。</span><span class="sxs-lookup"><span data-stu-id="4c16a-114">There are several key advantages in the modern PDF preview experience.</span></span> <span data-ttu-id="4c16a-115">以下のような特徴を持っています:</span><span class="sxs-lookup"><span data-stu-id="4c16a-115">These advantages include:</span></span>

- <span data-ttu-id="4c16a-116">画面上に表示された内容を忠実に印刷処理します。</span><span class="sxs-lookup"><span data-stu-id="4c16a-116">A fidelity between the screen presentation and the printed output.</span></span>
- <span data-ttu-id="4c16a-117">オンプレミス配置を含む、さまざまなデバイスおよびプラットフォーム上であっても、常に整合したドキュメントレポートプレビューを提供します。</span><span class="sxs-lookup"><span data-stu-id="4c16a-117">A consistent document report preview experience across devices and platforms, including on-premises deployments.</span></span>
- <span data-ttu-id="4c16a-118">サーバーサイド レンダリングにより、ドキュメントを作成する際の効率が向上します。</span><span class="sxs-lookup"><span data-stu-id="4c16a-118">The server-side rendering improves the performance when producing the document.</span></span>
- <span data-ttu-id="4c16a-119">組み込みツールによって、ビジネスドキュメントの内容をすばやく閲覧することができます。</span><span class="sxs-lookup"><span data-stu-id="4c16a-119">A built-in tooling that allows users to quickly navigate the contents of the business document.</span></span>

## <a name="accessing-the-pdf-preview-experience"></a><span data-ttu-id="4c16a-120">PDFプレビュー機能にアクセスする</span><span class="sxs-lookup"><span data-stu-id="4c16a-120">Accessing the PDF preview experience</span></span>
<span data-ttu-id="4c16a-121">利用可能となるPDFドキュメント ビューアー コントロールは、ほとんどの配置タイプで使用できるようになっています。</span><span class="sxs-lookup"><span data-stu-id="4c16a-121">The hosted PDF document viewer control is automatically available in most deployment types.</span></span> <span data-ttu-id="4c16a-122">ただし、ワンボックス配置の場合は、 **レポートオプション**  ページにてPDFプレビュー機能を有効にする必要があります。</span><span class="sxs-lookup"><span data-stu-id="4c16a-122">However, for one-box deployments, the PDF preview experience must be enabled on the **Report options** page.</span></span> <span data-ttu-id="4c16a-123">PDFのプレビューを有効にするには、以下の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="4c16a-123">Complete the following steps to enable the PDF preview experience.</span></span> 

1) <span data-ttu-id="4c16a-124">ブラウザウィンドウのURL末尾に "& Mi = sysreportadministration" を追加して **レポートオプション** に移動します。</span><span class="sxs-lookup"><span data-stu-id="4c16a-124">Go to the **Report options** page by adding "&mi=SysReportAdministration" to the URL in your browser window.</span></span>
2) <span data-ttu-id="4c16a-125">**埋め込みビューアを使用してドキュメントをプレビューする** フィールドを **はい** と設定します。</span><span class="sxs-lookup"><span data-stu-id="4c16a-125">Set the **Preview documents using embedded viewer** field to **Yes**.</span></span>
3) <span data-ttu-id="4c16a-126">**保存**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="4c16a-126">Click **Save**.</span></span>

## <a name="additional-feature-information"></a><span data-ttu-id="4c16a-127">追加の機能</span><span class="sxs-lookup"><span data-stu-id="4c16a-127">Additional feature information</span></span>

- <span data-ttu-id="4c16a-128">既定では、展開/折りたたみが可能なセクションが用意されています。</span><span class="sxs-lookup"><span data-stu-id="4c16a-128">Expandable/collapsible sections are available by default.</span></span> <span data-ttu-id="4c16a-129">これらのインタラクティブな操作は、PDFドキュメントが作成された後には機能しなくなります。</span><span class="sxs-lookup"><span data-stu-id="4c16a-129">These interactive operations do not function after the PDF document has been created.</span></span>
- <span data-ttu-id="4c16a-130">プリンターのドロップダウンメニューから、ローカル接続されている機器を選択することができます。</span><span class="sxs-lookup"><span data-stu-id="4c16a-130">The printer drop-down menu allows users to choose from locally connected devices.</span></span> <span data-ttu-id="4c16a-131">ここで表示されるリストには、Finance and Operations を通じて接続されているネットワークプリンターは含まれません。</span><span class="sxs-lookup"><span data-stu-id="4c16a-131">This list does not include network printers connected through the Finance and Operations service.</span></span>
- <span data-ttu-id="4c16a-132">ドキュメントは組み込みツールバーのアクションを使用してローカルデバイスにダウンロードされます。</span><span class="sxs-lookup"><span data-stu-id="4c16a-132">Documents are downloaded to the local device using the built-in toolbar actions.</span></span>
- <span data-ttu-id="4c16a-133">アプリケーション拡張機能を使用して、PDFドキュメント内の埋め込みドリルスルー リンクを有効にすることができます。</span><span class="sxs-lookup"><span data-stu-id="4c16a-133">Application extensions are available to activate embedded drill-thru links in PDF documents.</span></span>
- <span data-ttu-id="4c16a-134">PDF以外の形式のドキュメントを作成するには、 **印刷先** オプションを使用します。</span><span class="sxs-lookup"><span data-stu-id="4c16a-134">Use the **Print destination** options to produce documents in formats other than PDF.</span></span>

