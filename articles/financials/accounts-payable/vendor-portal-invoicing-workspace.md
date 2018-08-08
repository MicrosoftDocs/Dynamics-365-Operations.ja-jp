---
title: "仕入先コラボレーションの請求ワークスペース"
description: "このトピックでは、仕入先請求書を表示する方法、および仕入先コラボレーションの請求ワークスペースの表示から請求書を送信する方法について説明します。"
author: ShivamPandey-msft
manager: AnnBe
ms.date: 08/22/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: VendInvoiceWorkspace
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 221534
ms.assetid: c4ed62f3-d351-41d7-a2ad-790576cde4ab
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: HT
ms.sourcegitcommit: d9747ba144d56c9410846769e5465372c89ea111
ms.openlocfilehash: 5520012a00e918e8748b974773eeaf2450f0c55e
ms.contentlocale: ja-jp
ms.lasthandoff: 08/07/2018

---

# <a name="vendor-collaboration-invoicing-workspace"></a><span data-ttu-id="751ee-103">仕入先コラボレーションの請求ワークスペース</span><span class="sxs-lookup"><span data-stu-id="751ee-103">Vendor collaboration invoicing workspace</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="751ee-104">このトピックでは、仕入先請求書を表示する方法、および仕入先コラボレーションの請求ワークスペースの表示から請求書を送信する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="751ee-104">This topic explains how you can view vendor invoices and submit invoices from the vendor collaboration invoicing workspace.</span></span>

<span data-ttu-id="751ee-105">[仕入先コラボレーションの請求] ワークスペースが、仕入先請求書の情報を表示するために使用され、ワークフロー機能を使用して Microsoft Dynamics 365 for Finance and Operations に請求書を提出するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="751ee-105">The **Vendor collaboration invoicing** workspace can be used to view vendor invoice information and to submit invoices to Microsoft Dynamics 365 for Finance and Operations using workflow capabilities.</span></span>


<a name="vendor-collaboration-invoicing-workspace"></a><span data-ttu-id="751ee-106">仕入先コラボレーションの請求ワークスペース</span><span class="sxs-lookup"><span data-stu-id="751ee-106">Vendor collaboration invoicing workspace</span></span>
----------------------------------------

### <a name="summary-tiles"></a><span data-ttu-id="751ee-107">概要タイル</span><span class="sxs-lookup"><span data-stu-id="751ee-107">Summary tiles</span></span>

<span data-ttu-id="751ee-108">[**集計**] タイルには、選択された仕入先の請求書の概要が示されます。</span><span class="sxs-lookup"><span data-stu-id="751ee-108">The **Summary** tiles give an overview of the invoices for the selected vendor.</span></span> <span data-ttu-id="751ee-109">これらの状況によって請求書を表示できます。</span><span class="sxs-lookup"><span data-stu-id="751ee-109">You can view invoices by their state.</span></span>
-   <span data-ttu-id="751ee-110">下書きの請求書がワークフローに対して提出されませんでした。</span><span class="sxs-lookup"><span data-stu-id="751ee-110">Draft invoices have not been submitted to workflow.</span></span>
-   <span data-ttu-id="751ee-111">提出済で承認されていない請求書は、仕入先が提出した請求書ですが、これらは Finance and Operations には転記されていません。</span><span class="sxs-lookup"><span data-stu-id="751ee-111">Submitted, not approved invoices are those invoices that the vendor has submitted, but they have not been posted in Finance and Operations.</span></span>
-   <span data-ttu-id="751ee-112">承認され、支払されていない請求書が、Finance and Operations には転記されましたが、完全には支払われていません。</span><span class="sxs-lookup"><span data-stu-id="751ee-112">Approved, not paid invoices are those that have been posted in Finance and Operations, but they have not yet been fully paid.</span></span>
-   <span data-ttu-id="751ee-113">支払済の請求書は、Finance and Operations に全額支払われた請求書です。</span><span class="sxs-lookup"><span data-stu-id="751ee-113">Paid invoices are those that have been fully paid in Finance and Operations.</span></span>

<span data-ttu-id="751ee-114">タイルをクリックすると、フィルター処理された [**請求書の一覧**] ページが開きます。</span><span class="sxs-lookup"><span data-stu-id="751ee-114">Clicking on a tile will open a filtered view of the **Invoices list** page.</span></span>

### <a name="tabular-lists"></a><span data-ttu-id="751ee-115">表形式リスト</span><span class="sxs-lookup"><span data-stu-id="751ee-115">Tabular lists</span></span>

<span data-ttu-id="751ee-116">[**表形式リスト**] セクションでは、請求の状態は概要タイル (下書きと提出済、未承認リスト) と同様の方法で分割されます。</span><span class="sxs-lookup"><span data-stu-id="751ee-116">In the **Tabular lists** section, the status of the invoicing is broken down in similar ways as the summary tiles: Draft and Submitted, not approved lists.</span></span> <span data-ttu-id="751ee-117">下書きの状態では、請求書がワークフローに提出されるかまたは削除されます。</span><span class="sxs-lookup"><span data-stu-id="751ee-117">While in the Draft state, an invoice can be submitted to workflow or deleted.</span></span> <span data-ttu-id="751ee-118">最後の表形式の一覧は、請求書を検索するためのオプションです。</span><span class="sxs-lookup"><span data-stu-id="751ee-118">The last tabular list is an option to find invoices.</span></span> <span data-ttu-id="751ee-119">検索する際、検索をより迅速に行うために、フィルター処理することができます。</span><span class="sxs-lookup"><span data-stu-id="751ee-119">You can filter as you search, to allow for faster searches.</span></span>

### <a name="all-vendor-invoices-list-page"></a><span data-ttu-id="751ee-120">すべての仕入先請求書リスト ページ</span><span class="sxs-lookup"><span data-stu-id="751ee-120">All vendor invoices list page</span></span>

<span data-ttu-id="751ee-121">**仕入先コラボレーション請求書** リストページの全ての転記済みおよび未転記の仕入先請求書を表示できます。</span><span class="sxs-lookup"><span data-stu-id="751ee-121">You can view all posted and unposted vendor invoices on the **Vendor collaboration invoices** list page.</span></span> <span data-ttu-id="751ee-122">このリストページを使用して、請求書の支払状態を表示します。</span><span class="sxs-lookup"><span data-stu-id="751ee-122">You can use this list page to view the payment status of the invoices.</span></span> <span data-ttu-id="751ee-123">支払状態には、未転記、未払、部分的な支払、全額支払が含まれます。</span><span class="sxs-lookup"><span data-stu-id="751ee-123">The payment statuses include Unposted, Unpaid, Partially paid, and Fully paid.</span></span>
<span data-ttu-id="751ee-124">発注書から新しい請求書を作成する</span><span class="sxs-lookup"><span data-stu-id="751ee-124">Creating a new invoice from a purchase order</span></span>

<span data-ttu-id="751ee-125">[**仕入先コラボレーションの請求**] ワークスペースで [**新規**] のアクションを選択して、新しい仕入先請求書を作成します。</span><span class="sxs-lookup"><span data-stu-id="751ee-125">You can create a new vendor invoice by selecting the **New** action on the **Vendor collaboration invoicing** workspace.</span></span> <span data-ttu-id="751ee-126">仕入先から発注書番号および請求書番号が提供されている必要があります。</span><span class="sxs-lookup"><span data-stu-id="751ee-126">The purchase order number and invoice number must be provided by the vendor.</span></span> <span data-ttu-id="751ee-127">既定では、仕入先の発注書の明細行はすべて、新しい請求書に表示されます。</span><span class="sxs-lookup"><span data-stu-id="751ee-127">By default, all of the lines from the vendor's purchase order will appear on the new invoice.</span></span> <span data-ttu-id="751ee-128">数量、および原価情報は、現在の仕入先請求書からワークフローに送信する前に編集できます。</span><span class="sxs-lookup"><span data-stu-id="751ee-128">The quantity and cost information can be edited prior to submitting the vendor invoice to workflow.</span></span> <span data-ttu-id="751ee-129">請求書に情報を送信する前に、ファイル、メモ、画像ファイルおよび URL を添付することができます。</span><span class="sxs-lookup"><span data-stu-id="751ee-129">You can attach files, notes, images, and URLs to an invoice before submitting it.</span></span>

<span data-ttu-id="751ee-130">詳細については次を参照してください。[外部仕入先との仕入先コラボレーション](../../supply-chain/procurement/vendor-collaboration-work-external-vendors.md)</span><span class="sxs-lookup"><span data-stu-id="751ee-130">For more information, see [Vendor collaboration with external vendors](../../supply-chain/procurement/vendor-collaboration-work-external-vendors.md)</span></span>




