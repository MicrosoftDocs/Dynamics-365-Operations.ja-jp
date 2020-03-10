---
title: 埋め込みビューアを使用してPDFドキュメントのプレビューをする
description: このトピックでは、ビジネスドキュメントを表示するにあたり、埋め込みPDFプレビューオプションを使用する方法について説明します。
author: tjvass
manager: AnnBe
ms.date: 02/13/2020
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
ms.openlocfilehash: 4ea9b930c210699f01c791e3c94c3f04c13dfe23
ms.sourcegitcommit: 3dede95a3b17de920bb0adcb33029f990682752b
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/18/2020
ms.locfileid: "3070406"
---
# <a name="preview-pdf-documents-with-an-embedded-viewer"></a><span data-ttu-id="f9fed-103">埋め込みビューアを使用してPDFドキュメントのプレビューをする</span><span class="sxs-lookup"><span data-stu-id="f9fed-103">Preview PDF documents with an embedded viewer</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="f9fed-104">埋め込みPDFプレビューオプションを利用することにより、ビジネスドキュメントの作成にまつわるアプリケーションエクスペリエンスび効率を上げることができます。</span><span class="sxs-lookup"><span data-stu-id="f9fed-104">You can streamline application experiences that result in the production of business documents by taking advantage of the embedded PDF Preview option.</span></span> <span data-ttu-id="f9fed-105">Finance and Operations アプリケーションは、本サービスによって作成されたビジネスドキュメントをプレビューするにあたって最新のエクスペリエンスをお届けします。</span><span class="sxs-lookup"><span data-stu-id="f9fed-105">Finance and Operations applications deliver a modern experience to preview business documents that are produced by the service.</span></span> <span data-ttu-id="f9fed-106">組み込みのツールバーを使用することで、ドキュメントの閲覧やダウンロード、またはローカルに接続されている機器での印刷ができます。</span><span class="sxs-lookup"><span data-stu-id="f9fed-106">You can use the built-in toolbar to navigate and download the document or to print to locally connected devices.</span></span>

<span data-ttu-id="f9fed-107">埋め込みのビューアーを使うと、画面条の表示内容と印刷された内容に整合性を持たせることができます。</span><span class="sxs-lookup"><span data-stu-id="f9fed-107">The embedded viewer offers consistency between the screen presentation and the printed output.</span></span> <span data-ttu-id="f9fed-108">加えて、従来の操作と比較してレポートの表示時間が大幅に短縮されます。</span><span class="sxs-lookup"><span data-stu-id="f9fed-108">In addition, report viewing times are drastically reduced when compared to the legacy experience.</span></span> <span data-ttu-id="f9fed-109">Preview オプションは対応するすべての機器での使用が可能であり、サードパーティ製のソフトウェアを追加する必要はありません。</span><span class="sxs-lookup"><span data-stu-id="f9fed-109">The Preview option is available on all supported devices and does not require any additional third-party software.</span></span> <span data-ttu-id="f9fed-110">組み込みのビューア ツールバー オプションを使用すると、ドキュメントのダウンロードおよび閲覧が簡単になります。</span><span class="sxs-lookup"><span data-stu-id="f9fed-110">Documents can be easily downloaded and navigated by using the built-in viewer toolbar options.</span></span>

<span data-ttu-id="f9fed-111">次の図は、最新のビジネスドキュメントをプレビューした例です。</span><span class="sxs-lookup"><span data-stu-id="f9fed-111">The following illustration shows a preview of the experience with a modern business document.</span></span>
<span data-ttu-id="f9fed-112">![PDFプレビュー フォーム](./media/pdf-document-preview.png)</span><span class="sxs-lookup"><span data-stu-id="f9fed-112">![PDF preview form](./media/pdf-document-preview.png)</span></span>

<span data-ttu-id="f9fed-113">従来のHTMLベースのプレビューは、実物のドキュメントに即したプレビューへと取って代わります。</span><span class="sxs-lookup"><span data-stu-id="f9fed-113">The legacy HTML-based preview experience is being replaced by a true document preview experience.</span></span> <span data-ttu-id="f9fed-114">最新のPDFプレビュー機能には、いくつかの重要な特徴があります。</span><span class="sxs-lookup"><span data-stu-id="f9fed-114">There are several key advantages in the modern PDF preview experience.</span></span> <span data-ttu-id="f9fed-115">以下のような特徴を持っています:</span><span class="sxs-lookup"><span data-stu-id="f9fed-115">These advantages include:</span></span>

- <span data-ttu-id="f9fed-116">画面上に表示された内容を忠実に印刷処理します。</span><span class="sxs-lookup"><span data-stu-id="f9fed-116">A fidelity between the screen presentation and the printed output.</span></span>
- <span data-ttu-id="f9fed-117">オンプレミス配置を含む、さまざまなデバイスおよびプラットフォーム上であっても、常に整合したドキュメントレポートプレビューを提供します。</span><span class="sxs-lookup"><span data-stu-id="f9fed-117">A consistent document report preview experience across devices and platforms, including on-premises deployments.</span></span>
- <span data-ttu-id="f9fed-118">サーバーサイド レンダリングにより、ドキュメントを作成する際の効率が向上します。</span><span class="sxs-lookup"><span data-stu-id="f9fed-118">The server-side rendering improves the performance when producing the document.</span></span>
- <span data-ttu-id="f9fed-119">組み込みツールによって、ビジネスドキュメントの内容をすばやく閲覧することができます。</span><span class="sxs-lookup"><span data-stu-id="f9fed-119">A built-in tooling that allows users to quickly navigate the contents of the business document.</span></span>

## <a name="accessing-the-pdf-preview-experience"></a><span data-ttu-id="f9fed-120">PDFプレビュー機能にアクセスする</span><span class="sxs-lookup"><span data-stu-id="f9fed-120">Accessing the PDF preview experience</span></span>
<span data-ttu-id="f9fed-121">利用可能となるPDFドキュメント ビューアー コントロールは、ほとんどの配置タイプで使用できるようになっています。</span><span class="sxs-lookup"><span data-stu-id="f9fed-121">The hosted PDF document viewer control is automatically available in most deployment types.</span></span> <span data-ttu-id="f9fed-122">ただし、ワンボックス配置の場合は、 **レポートオプション**  ページにてPDFプレビュー機能を有効にする必要があります。</span><span class="sxs-lookup"><span data-stu-id="f9fed-122">However, for one-box deployments, the PDF preview experience must be enabled on the **Report options** page.</span></span> <span data-ttu-id="f9fed-123">PDFのプレビューを有効にするには、以下の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="f9fed-123">Complete the following steps to enable the PDF preview experience.</span></span> 

1) <span data-ttu-id="f9fed-124">ブラウザウィンドウのURL末尾に "& Mi = sysreportadministration" を追加して **レポートオプション** に移動します。</span><span class="sxs-lookup"><span data-stu-id="f9fed-124">Go to the **Report options** page by adding "&mi=SysReportAdministration" to the URL in your browser window.</span></span>
2) <span data-ttu-id="f9fed-125">**埋め込みビューアを使用してドキュメントをプレビューする** フィールドを **はい** と設定します。</span><span class="sxs-lookup"><span data-stu-id="f9fed-125">Set the **Preview documents using embedded viewer** field to **Yes**.</span></span>
3) <span data-ttu-id="f9fed-126">**保存**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="f9fed-126">Click **Save**.</span></span>

## <a name="additional-feature-information"></a><span data-ttu-id="f9fed-127">追加の機能</span><span class="sxs-lookup"><span data-stu-id="f9fed-127">Additional feature information</span></span>

- <span data-ttu-id="f9fed-128">既定では、展開/折りたたみが可能なセクションが用意されています。</span><span class="sxs-lookup"><span data-stu-id="f9fed-128">Expandable/collapsible sections are available by default.</span></span> <span data-ttu-id="f9fed-129">これらのインタラクティブな操作は、PDFドキュメントが作成された後には機能しなくなります。</span><span class="sxs-lookup"><span data-stu-id="f9fed-129">These interactive operations do not function after the PDF document has been created.</span></span>
- <span data-ttu-id="f9fed-130">プリンターのドロップダウンメニューから、ローカル接続されている機器を選択することができます。</span><span class="sxs-lookup"><span data-stu-id="f9fed-130">The printer drop-down menu allows users to choose from locally connected devices.</span></span> <span data-ttu-id="f9fed-131">ここで表示されるリストには、サービスを通じて接続されるネットワークプリンターは含まれません。</span><span class="sxs-lookup"><span data-stu-id="f9fed-131">This list does not include network printers connected through the service.</span></span>
- <span data-ttu-id="f9fed-132">ドキュメントは組み込みツールバーのアクションを使用してローカルデバイスにダウンロードされます。</span><span class="sxs-lookup"><span data-stu-id="f9fed-132">Documents are downloaded to the local device using the built-in toolbar actions.</span></span>
- <span data-ttu-id="f9fed-133">アプリケーション拡張機能を使用して、PDFドキュメント内の埋め込みドリルスルー リンクを有効にすることができます。</span><span class="sxs-lookup"><span data-stu-id="f9fed-133">Application extensions are available to activate embedded drill-thru links in PDF documents.</span></span>
- <span data-ttu-id="f9fed-134">PDF以外の形式のドキュメントを作成するには、 **印刷先** オプションを使用します。</span><span class="sxs-lookup"><span data-stu-id="f9fed-134">Use the **Print destination** options to produce documents in formats other than PDF.</span></span>

## <a name="feature-limitations"></a><span data-ttu-id="f9fed-135">機能の制限</span><span class="sxs-lookup"><span data-stu-id="f9fed-135">Feature limitations</span></span>
<span data-ttu-id="f9fed-136">埋め込み PDF ビューアー エクスペリエンスでは、ドキュメントの印刷出力と完全に一致する終了済ドキュメントが提供されます。</span><span class="sxs-lookup"><span data-stu-id="f9fed-136">The Embedded PDF viewer experience delivers a closed document that exactly matches the printed output of the document.</span></span>  <span data-ttu-id="f9fed-137">受信者はこれらのドキュメントを変更できないため、業務運営に適した形式になります。</span><span class="sxs-lookup"><span data-stu-id="f9fed-137">These documents cannot be modified by the recipient making the format ideal for business operations.</span></span>  <span data-ttu-id="f9fed-138">ただし、終了済形式のため、HTML プレゼンテーションと比較すると画面上のドキュメントの対話性がはるかに低くなります。</span><span class="sxs-lookup"><span data-stu-id="f9fed-138">However, as a closed format, the documents are far less interactive on the screen when compared to HTML presentations.</span></span>  <span data-ttu-id="f9fed-139">埋め込み PDF ビューアーを使用してドキュメントをプレビューする場合、次のエンド ユーザー機能はサポートされません。</span><span class="sxs-lookup"><span data-stu-id="f9fed-139">The following end-user capabilities are not supported when previewing documents using the embedded PDF viewer.</span></span>

- <span data-ttu-id="f9fed-140">埋め込みドリルスルー ナビゲーションは、PDF ドキュメントのプレビュー時には実行できません。</span><span class="sxs-lookup"><span data-stu-id="f9fed-140">Embedded drill-thru navigations are not actionable while previewing PDF documents.</span></span> 
- <span data-ttu-id="f9fed-141">PDF ドキュメントでは、展開および折りたたみ可能なセクションはサポートされません。</span><span class="sxs-lookup"><span data-stu-id="f9fed-141">PDF documents do not support expandable and collapsible sections.</span></span> 
- <span data-ttu-id="f9fed-142">レポートを PDF ドキュメントとして表示している場合、サブレポートはサポートされません。</span><span class="sxs-lookup"><span data-stu-id="f9fed-142">Sub-reports are not supported when viewing reports as PDF documents.</span></span>
- <span data-ttu-id="f9fed-143">レポートを、ドメインでホストされているプリンター デバイスに直接印刷します。</span><span class="sxs-lookup"><span data-stu-id="f9fed-143">Printing the report directly to domain-hosted printer devices.</span></span>
