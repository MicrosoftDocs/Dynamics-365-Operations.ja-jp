---
title: ER プリンター送信先のタイプ
description: このトピックでは、電子申告 (ER) 形式の各フォルダーまたはファイル コンポーネントに対してプリンター出力先を構成する方法について説明します。
author: NickSelin
ms.date: 02/24/2021
ms.topic: article
ms.prod: ''
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
ms.openlocfilehash: 7749a458020de664d00e81ccf0e480ae459da617
ms.sourcegitcommit: 951393b05bf409333cb3c7ad977bcaa804aa801b
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/13/2021
ms.locfileid: "5894007"
---
# <a name="printer-destination"></a><a name="PrinterDestinationType"></a><span data-ttu-id="5d2fb-103">プリンター出力先</span><span class="sxs-lookup"><span data-stu-id="5d2fb-103">Printer destination</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="5d2fb-104">直接印刷のために生成されたドキュメントをネットワーク プリンターに直接送信できます。</span><span class="sxs-lookup"><span data-stu-id="5d2fb-104">You can send a generated document directly to a network printer for direct printing.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="5d2fb-105">必要条件</span><span class="sxs-lookup"><span data-stu-id="5d2fb-105">Prerequisites</span></span>

<span data-ttu-id="5d2fb-106">開始する前に、ドキュメント回覧エージェントのインストールおよびコンフィギュレーションを行い、ネットワーク プリンターを登録する必要があります。</span><span class="sxs-lookup"><span data-stu-id="5d2fb-106">Before you begin, you must install and configure the Document Routing Agent, and then register the network printers.</span></span> <span data-ttu-id="5d2fb-107">詳細については、 [ドキュメント ルーティング エージェントをインストールしてネットワーク印刷を有効にする](./install-document-routing-agent.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="5d2fb-107">For more information, see [Install the Document Routing Agent to enable network printing](./install-document-routing-agent.md).</span></span>

## <a name="make-the-printer-destination-available"></a><span data-ttu-id="5d2fb-108">プリンター送信先を利用可能にする</span><span class="sxs-lookup"><span data-stu-id="5d2fb-108">Make the Printer destination available</span></span>

<span data-ttu-id="5d2fb-109">Microsoft Dynamics 365 Finance の現在のインスタンスで **プリンター** 送信先を利用可能にするには、**機能管理** ワークスペースに移動して、順序どおりに次の機能を有効にします。</span><span class="sxs-lookup"><span data-stu-id="5d2fb-109">To make the **Printer** destination available in the current instance of Microsoft Dynamics 365 Finance, go to the **Feature management** workspace, and turn on the following features, in this order:</span></span>

1. <span data-ttu-id="5d2fb-110">Microsoft Office 形式から PDF に電子申告送信ドキュメントを変換する</span><span class="sxs-lookup"><span data-stu-id="5d2fb-110">Convert Electronic Reporting outbound documents from Microsoft Office formats to PDF</span></span>
2. <span data-ttu-id="5d2fb-111">送信ドキュメントの電子申告の送信先としてのドキュメント回覧エージェント</span><span class="sxs-lookup"><span data-stu-id="5d2fb-111">Document Routing Agent as Electronic Reporting destination for outbound documents</span></span>

<span data-ttu-id="5d2fb-112">[![機能管理で ER プリンター送信先機能を有効にする](./media/ER_Destinations-EnablePrinterDestinationFeature.png)](./media/ER_Destinations-EnablePrinterDestinationFeature.png)</span><span class="sxs-lookup"><span data-stu-id="5d2fb-112">[![Turning on the ER printer destination feature in Feature management](./media/ER_Destinations-EnablePrinterDestinationFeature.png)](./media/ER_Destinations-EnablePrinterDestinationFeature.png)</span></span>

### <a name="applicability"></a><span data-ttu-id="5d2fb-113">適合性</span><span class="sxs-lookup"><span data-stu-id="5d2fb-113">Applicability</span></span>

<span data-ttu-id="5d2fb-114">**プリンター** 送信先は、印刷可能な PDF 形式 (PDF 合併または PDF ファイル形式の要素) または Microsoft Office Excel/Word 形式 (Excel ファイル) のいずれかで出力を生成するために使用されるファイル コンポーネントに対してのみコンフィギュレーションできます。</span><span class="sxs-lookup"><span data-stu-id="5d2fb-114">The **Printer** destination can be configured only for file components that are used to generate output in either printable PDF format (PDF Merger or PDF file format elements) or Microsoft Office Excel/Word format (Excel file).</span></span> <span data-ttu-id="5d2fb-115">出力が PDF 形式で生成された場合、プリンターに送信されます。</span><span class="sxs-lookup"><span data-stu-id="5d2fb-115">When output is generated in PDF format, it's sent to a printer.</span></span> <span data-ttu-id="5d2fb-116">出力が Microsoft Office 形式で生成された場合、自動的に PDF 形式に変換され、プリンターに送信されます。</span><span class="sxs-lookup"><span data-stu-id="5d2fb-116">When output is generated in Microsoft Office format, it's automatically converted to PDF format and then sent to a printer.</span></span>

### <a name="limitations"></a><span data-ttu-id="5d2fb-117">制限</span><span class="sxs-lookup"><span data-stu-id="5d2fb-117">Limitations</span></span>

<span data-ttu-id="5d2fb-118">**印刷** 送信先は、クラウド配置に対してのみ実装されます。</span><span class="sxs-lookup"><span data-stu-id="5d2fb-118">The **Printer** destination is implemented only for cloud deployments.</span></span>

### <a name="use-the-printer-destination"></a><span data-ttu-id="5d2fb-119">印刷送信先の使用</span><span class="sxs-lookup"><span data-stu-id="5d2fb-119">Use the Printer destination</span></span>

1. <span data-ttu-id="5d2fb-120">生成されたドキュメントをプリンターに送信するには、**有効** オプションを **Yes** に設定します。</span><span class="sxs-lookup"><span data-stu-id="5d2fb-120">Set the **Enabled** option to **Yes** to send a generated document to a printer.</span></span>
2. <span data-ttu-id="5d2fb-121">**プリンター名** フィールドで、必要なネットワーク プリンターを選択します。</span><span class="sxs-lookup"><span data-stu-id="5d2fb-121">In the **Printer name** field, select the required network printer.</span></span>
3. <span data-ttu-id="5d2fb-122">**印刷アーカイブに保存しますか?** オプションを **はい** に設定して生成された出力を印刷アーカイブに保存することにより、さらに印刷できるようになります。</span><span class="sxs-lookup"><span data-stu-id="5d2fb-122">Set the **Save in print archive?** option to **Yes** to store the generated output in the print archive, so that it's available for further printing.</span></span> <span data-ttu-id="5d2fb-123">後でアーカイブ出力にアクセスするには、**組織管理** \> **照会およびレポート** \> **レポート アーカイブ** に移動します。</span><span class="sxs-lookup"><span data-stu-id="5d2fb-123">To access archived output later, go to **Organization administration** \> **Inquiries and reports** \> **Report archive**.</span></span>

<span data-ttu-id="5d2fb-124">[![プリンター送信先の使用](./media/ER_Destinations-PrinterDestination.png)](./media/ER_Destinations-PrinterDestination.png)</span><span class="sxs-lookup"><span data-stu-id="5d2fb-124">[![Using the Printer destination](./media/ER_Destinations-PrinterDestination.png)](./media/ER_Destinations-PrinterDestination.png)</span></span>

> [!NOTE]
> <span data-ttu-id="5d2fb-125">**プリンター** 送信先をコンフィギュレーションする場合、**PDF への変換** オプションを有効にする必要はありません。</span><span class="sxs-lookup"><span data-stu-id="5d2fb-125">The **Convert to PDF** option doesn't have to be turned on when you configure the **Printer** destination.</span></span> <span data-ttu-id="5d2fb-126">印刷目的のための PDF 変換は、オプションが無効になっていても実行されます。</span><span class="sxs-lookup"><span data-stu-id="5d2fb-126">The PDF conversion for printing purposes will occur even if the option is turned off.</span></span>

<span data-ttu-id="5d2fb-127">送信ドキュメントを Excel 形式で印刷する際に特定の [ページの向き](electronic-reporting-destinations.md#SelectPdfPageOrientation) を使用するには、**PDF に変換する** オプションを有効にする必要があります。</span><span class="sxs-lookup"><span data-stu-id="5d2fb-127">To use a specific [page orientation](electronic-reporting-destinations.md#SelectPdfPageOrientation) when you print an outbound document in Excel format, you must turn on the **Convert to PDF** option.</span></span> <span data-ttu-id="5d2fb-128">**PDF に変換する** オプションを **はい** に設定すると、**ページの向き** フィールドが使用できるようになります。</span><span class="sxs-lookup"><span data-stu-id="5d2fb-128">When you set the **Convert to PDF** option to **Yes**, the **Page orientation** field becomes available.</span></span> <span data-ttu-id="5d2fb-129">**ページの方向** フィールドで、ページの向きを選択することができます。</span><span class="sxs-lookup"><span data-stu-id="5d2fb-129">In the **Page orientation** field, you can select a page orientation.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="5d2fb-130">追加リソース</span><span class="sxs-lookup"><span data-stu-id="5d2fb-130">Additional resources</span></span>

- [<span data-ttu-id="5d2fb-131">電子申告 (ER) の概要</span><span class="sxs-lookup"><span data-stu-id="5d2fb-131">Electronic reporting (ER) overview</span></span>](general-electronic-reporting.md)
- [<span data-ttu-id="5d2fb-132">電子申告 (ER) の送信先</span><span class="sxs-lookup"><span data-stu-id="5d2fb-132">Electronic reporting (ER) destinations</span></span>](electronic-reporting-destinations.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]