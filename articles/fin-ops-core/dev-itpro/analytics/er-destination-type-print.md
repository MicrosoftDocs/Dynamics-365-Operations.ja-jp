---
title: ER プリンター送信先のタイプ
description: このトピックでは、電子申告 (ER) 形式の各フォルダーまたはファイル コンポーネントに対してプリンター出力先を構成する方法について説明します。
author: NickSelin
manager: AnnBe
ms.date: 03/17/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: DocuType, ERSolutionTable, ERFormatDestinationTable
audience: Application User
ms.reviewer: kfend
ms.custom: 97423
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2020-04-01
ms.dyn365.ops.version: AX 10.0.9
ms.openlocfilehash: c6e298f62ec69f349eb713d66313e535c7e01881
ms.sourcegitcommit: 5192cfaedfd861faea63d8954d7bcc500608a225
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/30/2021
ms.locfileid: "5094082"
---
# <a name="printer-destination"></a><a name="PrinterDestinationType"></a><span data-ttu-id="a7903-103">プリンター出力先</span><span class="sxs-lookup"><span data-stu-id="a7903-103">Printer destination</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="a7903-104">直接印刷のために生成されたドキュメントをネットワーク プリンターに直接送信できます。</span><span class="sxs-lookup"><span data-stu-id="a7903-104">You can send a generated document directly to a network printer for direct printing.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="a7903-105">必要条件</span><span class="sxs-lookup"><span data-stu-id="a7903-105">Prerequisites</span></span>

<span data-ttu-id="a7903-106">開始する前に、ドキュメント回覧エージェントのインストールおよびコンフィギュレーションを行い、ネットワーク プリンターを登録する必要があります。</span><span class="sxs-lookup"><span data-stu-id="a7903-106">Before you begin, you must install and configure the Document Routing Agent, and then register the network printers.</span></span> <span data-ttu-id="a7903-107">詳細については、 [ドキュメント ルーティング エージェントをインストールしてネットワーク印刷を有効にする](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/analytics/install-document-routing-agent) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="a7903-107">For more information, see [Install the Document Routing Agent to enable network printing](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/analytics/install-document-routing-agent).</span></span>

## <a name="make-the-printer-destination-available"></a><span data-ttu-id="a7903-108">プリンター送信先を利用可能にする</span><span class="sxs-lookup"><span data-stu-id="a7903-108">Make the Printer destination available</span></span>

<span data-ttu-id="a7903-109">Microsoft Dynamics 365 Finance の現在のインスタンスで **プリンター** 送信先を利用可能にするには、**機能管理** ワークスペースに移動して、順序どおりに次の機能を有効にします。</span><span class="sxs-lookup"><span data-stu-id="a7903-109">To make the **Printer** destination available in the current instance of Microsoft Dynamics 365 Finance, go to the **Feature management** workspace, and turn on the following features, in this order:</span></span>

1. <span data-ttu-id="a7903-110">Microsoft Office 形式から PDF に電子申告送信ドキュメントを変換する</span><span class="sxs-lookup"><span data-stu-id="a7903-110">Convert Electronic Reporting outbound documents from Microsoft Office formats to PDF</span></span>
2. <span data-ttu-id="a7903-111">送信ドキュメントの電子申告の送信先としてのドキュメント回覧エージェント</span><span class="sxs-lookup"><span data-stu-id="a7903-111">Document Routing Agent as Electronic Reporting destination for outbound documents</span></span>

<span data-ttu-id="a7903-112">[![機能管理で ER プリンター送信先機能を有効にする](./media/ER_Destinations-EnablePrinterDestinationFeature.png)](./media/ER_Destinations-EnablePrinterDestinationFeature.png)</span><span class="sxs-lookup"><span data-stu-id="a7903-112">[![Turning on the ER printer destination feature in Feature management](./media/ER_Destinations-EnablePrinterDestinationFeature.png)](./media/ER_Destinations-EnablePrinterDestinationFeature.png)</span></span>

### <a name="applicability"></a><span data-ttu-id="a7903-113">適合性</span><span class="sxs-lookup"><span data-stu-id="a7903-113">Applicability</span></span>

<span data-ttu-id="a7903-114">**プリンター** 送信先は、印刷可能な PDF 形式 (PDF 合併または PDF ファイル形式の要素) または Microsoft Office Excel/Word 形式 (Excel ファイル) のいずれかで出力を生成するために使用されるファイル コンポーネントに対してのみコンフィギュレーションできます。</span><span class="sxs-lookup"><span data-stu-id="a7903-114">The **Printer** destination can be configured only for file components that are used to generate output in either printable PDF format (PDF Merger or PDF file format elements) or Microsoft Office Excel/Word format (Excel file).</span></span> <span data-ttu-id="a7903-115">出力が PDF 形式で生成された場合、プリンターに送信されます。</span><span class="sxs-lookup"><span data-stu-id="a7903-115">When output is generated in PDF format, it's sent to a printer.</span></span> <span data-ttu-id="a7903-116">出力が Microsoft Office 形式で生成された場合、自動的に PDF 形式に変換され、プリンターに送信されます。</span><span class="sxs-lookup"><span data-stu-id="a7903-116">When output is generated in Microsoft Office format, it's automatically converted to PDF format and then sent to a printer.</span></span>

### <a name="limitations"></a><span data-ttu-id="a7903-117">制限</span><span class="sxs-lookup"><span data-stu-id="a7903-117">Limitations</span></span>

<span data-ttu-id="a7903-118">この機能はプレビュー機能で、[Microsoft Dynamics 365 プレビューの追加使用条件](https://go.microsoft.com/fwlink/?linkid=2105274) で説明されている使用条件に従います。</span><span class="sxs-lookup"><span data-stu-id="a7903-118">This feature is a preview feature and is subject to the terms of use that are described in [Supplemental Terms of Use for Microsoft Dynamics 365 Previews](https://go.microsoft.com/fwlink/?linkid=2105274).</span></span>

<span data-ttu-id="a7903-119">**印刷** 送信先は、クラウド配置に対してのみ実装されます。</span><span class="sxs-lookup"><span data-stu-id="a7903-119">The **Printer** destination is implemented only for cloud deployments.</span></span>

### <a name="use-the-printer-destination"></a><span data-ttu-id="a7903-120">印刷送信先の使用</span><span class="sxs-lookup"><span data-stu-id="a7903-120">Use the Printer destination</span></span>

1. <span data-ttu-id="a7903-121">生成されたドキュメントをプリンターに送信するには、**有効** オプションを **Yes** に設定します。</span><span class="sxs-lookup"><span data-stu-id="a7903-121">Set the **Enabled** option to **Yes** to send a generated document to a printer.</span></span>
2. <span data-ttu-id="a7903-122">**プリンター名** フィールドで、必要なネットワーク プリンターを選択します。</span><span class="sxs-lookup"><span data-stu-id="a7903-122">In the **Printer name** field, select the required network printer.</span></span>
3. <span data-ttu-id="a7903-123">**印刷アーカイブに保存しますか?** オプションを **はい** に設定して生成された出力を印刷アーカイブに保存することにより、さらに印刷できるようになります。</span><span class="sxs-lookup"><span data-stu-id="a7903-123">Set the **Save in print archive?** option to **Yes** to store the generated output in the print archive, so that it's available for further printing.</span></span> <span data-ttu-id="a7903-124">後でアーカイブ出力にアクセスするには、**組織管理** \> **照会およびレポート** \> **レポート アーカイブ** に移動します。</span><span class="sxs-lookup"><span data-stu-id="a7903-124">To access archived output later, go to **Organization administration** \> **Inquiries and reports** \> **Report archive**.</span></span>

<span data-ttu-id="a7903-125">[![プリンター送信先の使用](./media/ER_Destinations-PrinterDestination.png)](./media/ER_Destinations-PrinterDestination.png)</span><span class="sxs-lookup"><span data-stu-id="a7903-125">[![Using the Printer destination](./media/ER_Destinations-PrinterDestination.png)](./media/ER_Destinations-PrinterDestination.png)</span></span>

> [!NOTE]
> <span data-ttu-id="a7903-126">**プリンター** 送信先をコンフィギュレーションする場合、**PDF への変換** オプションを有効にする必要はありません。</span><span class="sxs-lookup"><span data-stu-id="a7903-126">The **Convert to PDF** option doesn't have to be turned on when you configure the **Printer** destination.</span></span> <span data-ttu-id="a7903-127">印刷目的のための PDF 変換は、オプションが無効になっていても実行されます。</span><span class="sxs-lookup"><span data-stu-id="a7903-127">The PDF conversion for printing purposes will occur even if the option is turned off.</span></span>

<span data-ttu-id="a7903-128">送信ドキュメントを Excel 形式で印刷する際に特定の [ページの向き](electronic-reporting-destinations.md#SelectPdfPageOrientation) を使用するには、**PDF に変換する** オプションを有効にする必要があります。</span><span class="sxs-lookup"><span data-stu-id="a7903-128">To use a specific [page orientation](electronic-reporting-destinations.md#SelectPdfPageOrientation) when you print an outbound document in Excel format, you must turn on the **Convert to PDF** option.</span></span> <span data-ttu-id="a7903-129">**PDF に変換する** オプションを **はい** に設定すると、**ページの向き** フィールドが使用できるようになります。</span><span class="sxs-lookup"><span data-stu-id="a7903-129">When you set the **Convert to PDF** option to **Yes**, the **Page orientation** field becomes available.</span></span> <span data-ttu-id="a7903-130">**ページの方向** フィールドで、ページの向きを選択することができます。</span><span class="sxs-lookup"><span data-stu-id="a7903-130">In the **Page orientation** field, you can select a page orientation.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="a7903-131">追加リソース</span><span class="sxs-lookup"><span data-stu-id="a7903-131">Additional resources</span></span>

- [<span data-ttu-id="a7903-132">電子申告 (ER) の概要</span><span class="sxs-lookup"><span data-stu-id="a7903-132">Electronic reporting (ER) overview</span></span>](general-electronic-reporting.md)
- [<span data-ttu-id="a7903-133">電子申告 (ER) の送信先</span><span class="sxs-lookup"><span data-stu-id="a7903-133">Electronic reporting (ER) destinations</span></span>](electronic-reporting-destinations.md)
