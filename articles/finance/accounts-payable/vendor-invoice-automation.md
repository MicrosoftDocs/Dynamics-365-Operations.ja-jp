---
title: スキャン済みドキュメントの請求書の自動化
description: このトピックでは、添付ファイルを含む請求書など、仕入先請求書のエンドツーエンドの自動化で利用可能な機能について説明します。
author: abruer
manager: AnnBe
ms.date: 05/22/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: VendEditInvoiceHeaderStagingListPage
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: f6d19d0e10f477e498e8f0fff1f431bc4bfdd9a1
ms.sourcegitcommit: 6ffbae02de2eee1f3be9bab2da37a3771aae8bec
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/30/2020
ms.locfileid: "3904958"
---
# <a name="invoice-automation-for-scanned-documents"></a><span data-ttu-id="0b336-103">スキャン済みドキュメントの請求書の自動化</span><span class="sxs-lookup"><span data-stu-id="0b336-103">Invoice automation for scanned documents</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="0b336-104">このトピックでは、添付ファイルを含む請求書など、仕入先請求書のエンドツーエンドの自動化で利用可能な機能について説明します。</span><span class="sxs-lookup"><span data-stu-id="0b336-104">This topic explains the features that are available for end-to-end automation of vendor invoices, even invoices that include attachments.</span></span>

<span data-ttu-id="0b336-105">買掛金勘定 (AP) プロセスを合理化したい組織は、多くの場合、請求書処理プロセスが効率化を図る必要があるプロセス領域の最上位にあると考えます。</span><span class="sxs-lookup"><span data-stu-id="0b336-105">Organizations that want to streamline their Accounts payable (AP) processes often identify invoice processing as one of the top process areas that should be more efficient.</span></span> <span data-ttu-id="0b336-106">多くの場合は、このような組織は、紙の請求書の処理からサード パーティ光学式文字認識 (OCR) サービス プロバイダにオフロードします。</span><span class="sxs-lookup"><span data-stu-id="0b336-106">In many cases, these organizations offload the processing of paper invoices to a third-party optical character recognition (OCR) service provider.</span></span> <span data-ttu-id="0b336-107">それにより、各請求書のスキャン イメージと共に機械可読請求書メタデータを受け取ります。</span><span class="sxs-lookup"><span data-stu-id="0b336-107">They then receive machine-readable invoice metadata together with a scanned image of each invoice.</span></span> <span data-ttu-id="0b336-108">オートメーションのためには、請求システムでこれらのコンポーネントの消費を有効にする「最終工程」ソリューションを構築します。</span><span class="sxs-lookup"><span data-stu-id="0b336-108">To help with automation, a “last mile” solution is then built to enable consumption of these artifacts in the invoicing system.</span></span> <span data-ttu-id="0b336-109">請求書自動化ソリューションをそのまま使用することで、この「最終工程」有効になります。</span><span class="sxs-lookup"><span data-stu-id="0b336-109">Now this “last mile” automation is enabled out of the box, through an invoice automation solution.</span></span>

## <a name="solution-context"></a><span data-ttu-id="0b336-110">ソリューション コンテキスト</span><span class="sxs-lookup"><span data-stu-id="0b336-110">Solution context</span></span>

<span data-ttu-id="0b336-111">請求書自動化ソリューションでは、請求書ヘッダーと請求明細行の請求書メタデータおよび請求書に適用される添付ファイルを受け取ることができる標準インターフェイスを実現します。</span><span class="sxs-lookup"><span data-stu-id="0b336-111">The invoice automation solution enables a standard interface that can accept invoice metadata for the invoice header and invoice lines, and also attachments that are applicable to the invoice.</span></span> <span data-ttu-id="0b336-112">このインターフェイスに準拠しているコンポーネントを生成する外部のシステムは、請求書および添付ファイルの自動処理のためのフィードを送信することができます。</span><span class="sxs-lookup"><span data-stu-id="0b336-112">Any external system that can generate artifacts that comply with this interface will be able to send the feed for automatic processing of invoices and attachments.</span></span>

<span data-ttu-id="0b336-113">次の図は、Contoso が仕入先請求書の処理のために OCR サービス プロバイダと統合する場合のシナリオの例を示します。</span><span class="sxs-lookup"><span data-stu-id="0b336-113">The following illustration shows a sample integration scenario where Contoso has partnered with an OCR service provider for vendor invoice processing.</span></span> <span data-ttu-id="0b336-114">Contoso 社の仕入先は、請求書をサービス プロバイダーへ電子メールで送信します。</span><span class="sxs-lookup"><span data-stu-id="0b336-114">Contoso’s vendors send invoices to the service provider by email.</span></span> <span data-ttu-id="0b336-115">OCR 処理によっては、サービス プロバイダーは請求書メタデータ (ヘッダーまたは明細行) および請求書のスキャン イメージを生成します。</span><span class="sxs-lookup"><span data-stu-id="0b336-115">Through OCR processing, the service provider generates invoice metadata (header and/or lines) and a scanned image of the invoice.</span></span> <span data-ttu-id="0b336-116">使用できるよう統合レイヤーでこれらのコンポーネントを変換します。</span><span class="sxs-lookup"><span data-stu-id="0b336-116">An integration layer then transforms these artifacts so that they can be consumed.</span></span>

![統合シナリオ例](media/vendor_invoice_automation_01.png)

<span data-ttu-id="0b336-118">請求書の統合が必要な場合、上記のシナリオのさまざまなバリエーションが可能です。</span><span class="sxs-lookup"><span data-stu-id="0b336-118">Several variations of the preceding scenario are possible if invoice integration is required.</span></span> <span data-ttu-id="0b336-119">別のユースケースはデータ移行で、このインターフェイスを使用して請求書および添付ファイルを作成できます。</span><span class="sxs-lookup"><span data-stu-id="0b336-119">Data migration is another use case where this interface can be used to create invoices and attachments.</span></span>

### <a name="solution-components"></a><span data-ttu-id="0b336-120">ソリューション コンポーネント</span><span class="sxs-lookup"><span data-stu-id="0b336-120">Solution components</span></span>

<span data-ttu-id="0b336-121">ソリューション フットプリントは、次のコンポーネントで構成されます。</span><span class="sxs-lookup"><span data-stu-id="0b336-121">The solution footprint consists of the following components:</span></span>

+ <span data-ttu-id="0b336-122">請求書ヘッダー、請求書の明細行、および請求書の添付ファイルのデータ エンティティ</span><span class="sxs-lookup"><span data-stu-id="0b336-122">Data entities for the invoice header, invoice lines, and invoice attachments</span></span>
+ <span data-ttu-id="0b336-123">請求書の例外処理</span><span class="sxs-lookup"><span data-stu-id="0b336-123">Exception processing for invoices</span></span>
+ <span data-ttu-id="0b336-124">請求書の添付ファイルを並べて表示するビューアー</span><span class="sxs-lookup"><span data-stu-id="0b336-124">A side-by-side attachment viewer in invoices</span></span>

<span data-ttu-id="0b336-125">このトピックの後半では、これらのソリューション コンポーネントの詳細説明を提供します。</span><span class="sxs-lookup"><span data-stu-id="0b336-125">The rest of this topic provides detailed descriptions of these solution components.</span></span>

## <a name="data-entities"></a><span data-ttu-id="0b336-126">データ エンティティ</span><span class="sxs-lookup"><span data-stu-id="0b336-126">Data entities</span></span>

<span data-ttu-id="0b336-127">データ パッケージは、送信する必要がある作業単位で、請求書ヘッダー、請求明細行、および請求書の添付ファイルが作成されます。</span><span class="sxs-lookup"><span data-stu-id="0b336-127">A data package is the unit of work that must be sent so that invoice headers, invoice lines, and invoice attachments can be created.</span></span> <span data-ttu-id="0b336-128">データ パッケージを構成するコンポーネントで使用されるのは次のデータ エンティティです。</span><span class="sxs-lookup"><span data-stu-id="0b336-128">The following data entities are used for the artifacts that make up the data package:</span></span>

+ <span data-ttu-id="0b336-129">仕入先請求書ヘッダー</span><span class="sxs-lookup"><span data-stu-id="0b336-129">Vendor invoice header</span></span>
+ <span data-ttu-id="0b336-130">仕入先請求明細行</span><span class="sxs-lookup"><span data-stu-id="0b336-130">Vendor invoice line</span></span>
+ <span data-ttu-id="0b336-131">仕入先請求書ドキュメントの添付ファイル</span><span class="sxs-lookup"><span data-stu-id="0b336-131">Vendor invoice document attachment</span></span>

<span data-ttu-id="0b336-132">仕入先請求書ドキュメントの添付ファイルは、この機能の一部として導入される新しいデータ エンティティです。</span><span class="sxs-lookup"><span data-stu-id="0b336-132">Vendor invoice document attachment is a new data entity that is introduced as part of this feature.</span></span> <span data-ttu-id="0b336-133">添付ファイルをサポートできるように、仕入先請求書ヘッダーのエンティティが変更されました。</span><span class="sxs-lookup"><span data-stu-id="0b336-133">The Vendor invoice header entity has been modified so that it supports attachments.</span></span> <span data-ttu-id="0b336-134">この機能に関して、仕入先請求書の明細行のエンティティは変更されていません。</span><span class="sxs-lookup"><span data-stu-id="0b336-134">The Vendor invoice line entity hasn’t been modified for this feature.</span></span>

<span data-ttu-id="0b336-135">データパッケージの詳細については、[データ管理の概要](../../fin-ops-core/dev-itpro/data-entities/data-entities-data-packages.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="0b336-135">For detailed information about data packages, see [Data management overview](../../fin-ops-core/dev-itpro/data-entities/data-entities-data-packages.md).</span></span> <span data-ttu-id="0b336-136">データ管理ワークスペースを使用したデータ パッケージの作成方法については、[Dynamics 365 Finance and Operations アプリ ソリューションにおけるデータパッケージの処理と消費](../../fin-ops-core/dev-itpro/lcs-solutions/process-data-packages-lcs-solutions.md)を参照してください 。</span><span class="sxs-lookup"><span data-stu-id="0b336-136">For information about how to create data packages using the data management workspace, see [Process and consume data packages in Dynamics 365 Finance and Operations apps solution](../../fin-ops-core/dev-itpro/lcs-solutions/process-data-packages-lcs-solutions.md).</span></span>

<span data-ttu-id="0b336-137">請求書および添付ファイルを含むテスト データを簡単に生成するには、以下の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="0b336-137">To quickly generate test data that includes invoices and attachments, follow these steps.</span></span>

1. <span data-ttu-id="0b336-138">インスタンスにサインインします。</span><span class="sxs-lookup"><span data-stu-id="0b336-138">Sign in to your instance.</span></span>
1. <span data-ttu-id="0b336-139">**買掛金勘定** > **請求書** > **保留中の仕入先請求書** に移動します。</span><span class="sxs-lookup"><span data-stu-id="0b336-139">Go to **Accounts payables** > **Invoices** > **Pending vendor invoices**.</span></span>
1. <span data-ttu-id="0b336-140">明細行および添付ファイルがある請求書を作成します。</span><span class="sxs-lookup"><span data-stu-id="0b336-140">Create invoices that have lines and attachments.</span></span>

    > [!NOTE]
    > <span data-ttu-id="0b336-141">添付ファイルは、ヘッダー添付ファイルにする必要があります。</span><span class="sxs-lookup"><span data-stu-id="0b336-141">The attachments must be header attachments.</span></span> <span data-ttu-id="0b336-142">現時点では、仕入先請求書ドキュメントの添付ファイルのエンティティは、明細行の添付ファイルをサポートしていません。</span><span class="sxs-lookup"><span data-stu-id="0b336-142">Currently, the Vendor invoice document attachment entity doesn’t support line attachments.</span></span>

1. <span data-ttu-id="0b336-143">**データ管理**ワークスペースを開きます。</span><span class="sxs-lookup"><span data-stu-id="0b336-143">Open the **Data management** workspace.</span></span>
1. <span data-ttu-id="0b336-144">仕入先請求書ヘッダー、仕入先請求書の明細行、および仕入先請求書ドキュメントの添付ファイルのエンティティを含むエクスポート ジョブを作成します。</span><span class="sxs-lookup"><span data-stu-id="0b336-144">Create an export job that includes the Vendor invoice header, Vendor invoice line, and Vendor invoice document attachment entities.</span></span>
1. <span data-ttu-id="0b336-145">データをエクスポートします。</span><span class="sxs-lookup"><span data-stu-id="0b336-145">Export the data.</span></span>
1. <span data-ttu-id="0b336-146">エクスポートしたデータを、パッケージとしてダウンロードします。</span><span class="sxs-lookup"><span data-stu-id="0b336-146">Download the exported data as a package.</span></span> <span data-ttu-id="0b336-147">対象のインスタンスにデータをテスト用にインポートするために、パッケージを使用できます。</span><span class="sxs-lookup"><span data-stu-id="0b336-147">You can now use the package to import data into target instances for testing purposes.</span></span>

### <a name="determining-the-legal-entity-for-an-invoice"></a><span data-ttu-id="0b336-148">請求書の法人を決定します。</span><span class="sxs-lookup"><span data-stu-id="0b336-148">Determining the legal entity for an invoice</span></span>

<span data-ttu-id="0b336-149">データ パッケージからインポートする請求書と、それが属する法人を関連付ける方法は 2 つあります。</span><span class="sxs-lookup"><span data-stu-id="0b336-149">Invoices that are imported via data packages can be associated with the legal entity that they belong to in two ways:</span></span>

+ <span data-ttu-id="0b336-150">請求書を処理するインポート ジョブが、**データ管理**ワークスペースでジョブがスケジュールされた会社にインポートします。</span><span class="sxs-lookup"><span data-stu-id="0b336-150">The import job that processes the invoice imports it into the same company in which the job was scheduled in the **Data management** workspace.</span></span> <span data-ttu-id="0b336-151">つまり、ジョブを実行する会社が、請求書が属する会社となります。</span><span class="sxs-lookup"><span data-stu-id="0b336-151">In other words, the company of the job determines the company that the invoice belongs to.</span></span>
+ <span data-ttu-id="0b336-152">請求書が含まれるデータ パッケージが Finance に送信された時、呼び出し元 (つまり、Finance の外部で実行される統合アプリケーション) は HTTP 要求で明示的に会社の ID に言及します。</span><span class="sxs-lookup"><span data-stu-id="0b336-152">When the data package that contains invoices is sent to Finance, the caller (that is, the integration application that runs outside of Finance) can explicitly mention the company ID in the HTTP request.</span></span> <span data-ttu-id="0b336-153">この場合は、Finance で処理のジョブを実行する会社コンテキストが上書きされ、請求書は HTTP 要求で渡された会社にインポートされます。</span><span class="sxs-lookup"><span data-stu-id="0b336-153">In this case, the company context in which the processing job runs in Finance is overridden, and the invoices are imported into the company that was passed via the HTTP request.</span></span>

> [!NOTE]
> <span data-ttu-id="0b336-154">この動作は、標準的なデータ管理の動作です。</span><span class="sxs-lookup"><span data-stu-id="0b336-154">This behavior is standard data management behavior.</span></span> <span data-ttu-id="0b336-155">間違いが生じないように、請求書のコンテキストで、念のために説明されています。</span><span class="sxs-lookup"><span data-stu-id="0b336-155">It’s explained here, in the context of invoices, just for the sake of completeness.</span></span>

## <a name="exception-processing"></a><span data-ttu-id="0b336-156">例外処理</span><span class="sxs-lookup"><span data-stu-id="0b336-156">Exception processing</span></span>

<span data-ttu-id="0b336-157">仕入先の請求書が統合されて Finance and Operations に渡される場合、買掛金勘定チームのメンバーが例外処理や障害が発生した請求書を簡単に処理したり、障害が発生した請求書から保留中の請求書を作成する方法が必要になります。</span><span class="sxs-lookup"><span data-stu-id="0b336-157">In scenarios where vendor invoices come into Finance and Operations via integration, there must be an easy way for an Accounts payable team member to process exceptions or failed invoices, and to create pending invoices out of failed invoices.</span></span> <span data-ttu-id="0b336-158">この仕入先請求書の例外処理は、現在 Finance and Operations の一部として提供されています。</span><span class="sxs-lookup"><span data-stu-id="0b336-158">This exception processing for vendor invoices is now part of Finance and Operations.</span></span>

### <a name="exceptions-list-page"></a><span data-ttu-id="0b336-159">[例外リスト] ページ</span><span class="sxs-lookup"><span data-stu-id="0b336-159">Exceptions list page</span></span>

<span data-ttu-id="0b336-160">例外請求書の新しいリスト ページは、**買掛金管理** > **請求書** > **インポートの失敗** > **インポートに失敗した仕入先請求書** にあります。</span><span class="sxs-lookup"><span data-stu-id="0b336-160">The new list page for invoice exceptions is available at **Accounts payable** > **Invoices** > **Import failures** > **Vendor invoices that failed to import**.</span></span> <span data-ttu-id="0b336-161">このページは、仕入先請求書ヘッダーのデータ エンティティのステージング テーブルから、すべての仕入先請求書のヘッダー レコードを表示します。</span><span class="sxs-lookup"><span data-stu-id="0b336-161">This page shows all the vendor invoice header records from the staging table of the Vendor invoice header data entity.</span></span> <span data-ttu-id="0b336-162">同じレコードを**データ管理**ワークスペースで表示することもできます。ここでは、例外処理機能で提供されているのと同じアクションを実行することもできます。</span><span class="sxs-lookup"><span data-stu-id="0b336-162">Note that you can view the same records from the **Data management** workspace, where you can also perform the same actions that are provided in the exception handling feature.</span></span> <span data-ttu-id="0b336-163">ただし、例外処理機能が提供する UI は、機能ユーザーに対して最適化されています。</span><span class="sxs-lookup"><span data-stu-id="0b336-163">However, the UI that the exception handling feature provides is optimized for a functional user.</span></span>

![[例外リスト] ページ](media/vendor_invoice_automation_02.png)

<span data-ttu-id="0b336-165">このリスト ページには、フィード経由で受け取る次のフィールドが含まれています。</span><span class="sxs-lookup"><span data-stu-id="0b336-165">This list page includes the following fields that come in via the feed:</span></span>

+ <span data-ttu-id="0b336-166">**会社** – 請求書が属する会社</span><span class="sxs-lookup"><span data-stu-id="0b336-166">**Company** – The company that the invoice belongs to</span></span>
+ <span data-ttu-id="0b336-167">**エラー メッセージ** – 請求書を作成できなかった理由を説明する、データ管理フレームワークが発行するエラー メッセージ</span><span class="sxs-lookup"><span data-stu-id="0b336-167">**Error message** – The error message that the data management framework issues to explain why the invoice could not be created</span></span>
+ <span data-ttu-id="0b336-168">**番号** – 請求書番号</span><span class="sxs-lookup"><span data-stu-id="0b336-168">**Number** – The invoice number</span></span>
+ <span data-ttu-id="0b336-169">**請求元仕入先**</span><span class="sxs-lookup"><span data-stu-id="0b336-169">**Invoice account**</span></span>
+ <span data-ttu-id="0b336-170">**名前** – 仕入先の名前</span><span class="sxs-lookup"><span data-stu-id="0b336-170">**Name** – The vendor’s name</span></span>
+ <span data-ttu-id="0b336-171">**仕入先**</span><span class="sxs-lookup"><span data-stu-id="0b336-171">**Vendor account**</span></span>
+ <span data-ttu-id="0b336-172">**発注書** – 請求書の発注書 (PO) 番号</span><span class="sxs-lookup"><span data-stu-id="0b336-172">**Purchase order** – The purchase order (PO) number for the invoice</span></span>
+ <span data-ttu-id="0b336-173">**転記日付**</span><span class="sxs-lookup"><span data-stu-id="0b336-173">**Posting date**</span></span>
+ <span data-ttu-id="0b336-174">**請求日**</span><span class="sxs-lookup"><span data-stu-id="0b336-174">**Invoice date**</span></span>
+ <span data-ttu-id="0b336-175">**請求明細**</span><span class="sxs-lookup"><span data-stu-id="0b336-175">**Invoice description**</span></span>
+ <span data-ttu-id="0b336-176">**通貨**</span><span class="sxs-lookup"><span data-stu-id="0b336-176">**Currency**</span></span>
+ <span data-ttu-id="0b336-177">**ログ**</span><span class="sxs-lookup"><span data-stu-id="0b336-177">**Log**</span></span>
+ <span data-ttu-id="0b336-178">**明細行参照** – 外部システムから取得する識別子</span><span class="sxs-lookup"><span data-stu-id="0b336-178">**Line reference** – The identifier that comes from the external system</span></span>

    > [!NOTE]
    > <span data-ttu-id="0b336-179">明細行参照は請求書 ID ではありません。</span><span class="sxs-lookup"><span data-stu-id="0b336-179">The line reference isn’t the invoice ID.</span></span>

<span data-ttu-id="0b336-180">このリスト ページには、次のように使用できるプレビュー ウィンドウもあります。</span><span class="sxs-lookup"><span data-stu-id="0b336-180">This list page also has a preview pane that you can used in the following ways:</span></span>

+ <span data-ttu-id="0b336-181">グリッド内の **エラー メッセージ** 列を展開する必要がないように、エラー メッセージ全体を表示します。</span><span class="sxs-lookup"><span data-stu-id="0b336-181">View the whole error message, so that you don’t have to expand the **Error message** column in the grid.</span></span>
+ <span data-ttu-id="0b336-182">請求書に添付ファイルが付属している場合、請求書の添付ファイルのリスト全体を表示します。</span><span class="sxs-lookup"><span data-stu-id="0b336-182">View the whole list of attachments for the invoice, if any attachments came with the invoice.</span></span>

<span data-ttu-id="0b336-183">リスト ページでは、次の操作がサポートされています。</span><span class="sxs-lookup"><span data-stu-id="0b336-183">The list page supports the following actions:</span></span>

+ <span data-ttu-id="0b336-184">**編集** – 編集モードで例外レコードを開くので、問題を修正することができます。</span><span class="sxs-lookup"><span data-stu-id="0b336-184">**Edit** – Open the exception record in edit mode, so that you can fix the issues.</span></span>
+ <span data-ttu-id="0b336-185">**オプション** – リスト ページで利用できる標準オプションにアクセスします。</span><span class="sxs-lookup"><span data-stu-id="0b336-185">**Options** – Access the standard options that are available on list pages.</span></span> <span data-ttu-id="0b336-186">**ワークスペースへの追加** オプションで、例外リスト ページをリストまたはタイルとしてワークスペースに固定することができます。</span><span class="sxs-lookup"><span data-stu-id="0b336-186">You can use the **Add to workspace** option to pin the exceptions list page to your workspace as a list or tile.</span></span>

### <a name="exception-details-page"></a><span data-ttu-id="0b336-187">[例外の詳細] ページ</span><span class="sxs-lookup"><span data-stu-id="0b336-187">Exception details page</span></span>

<span data-ttu-id="0b336-188">編集モードを開始するときに、問題がある請求書の [例外の詳細] ページが表示されます。</span><span class="sxs-lookup"><span data-stu-id="0b336-188">When you start edit mode, the exception details page for the invoice that has issues appears.</span></span> <span data-ttu-id="0b336-189">添付ファイルがある場合、請求書および既定の添付ファイルは [例外の詳細] ページに並べて表示されます。</span><span class="sxs-lookup"><span data-stu-id="0b336-189">If there are any attachments, the invoice and the default attachment appear side by side on the exception details page.</span></span>

![[例外の詳細] ページ](media/vendor_invoice_automation_03.png)

<span data-ttu-id="0b336-191">前の例では、受け取った仕入先請求書ヘッダーには明細行がありませんでした。</span><span class="sxs-lookup"><span data-stu-id="0b336-191">In the preceding illustration, there weren’t any lines for the vendor invoice header that came in.</span></span> <span data-ttu-id="0b336-192">そのため、明細行のセクションは空です。</span><span class="sxs-lookup"><span data-stu-id="0b336-192">Therefore, the lines section is empty.</span></span>

<span data-ttu-id="0b336-193">[例外の詳細] ページでは、次の操作がサポートされています。</span><span class="sxs-lookup"><span data-stu-id="0b336-193">The exception details page supports the following operation:</span></span>

+ <span data-ttu-id="0b336-194">**保留中の請求書の作成** – 例外処理の一部として請求書の問題を解決した後、このボタンをクリックして保留中の請求書を作成できます。</span><span class="sxs-lookup"><span data-stu-id="0b336-194">**Create pending invoice** – After you’ve fixed the issues on the invoice as part of exception processing, you can click this button to create the pending invoice.</span></span> <span data-ttu-id="0b336-195">保留中の請求書の作成は、(非同期操作) としてバック グラウンドで発生します。</span><span class="sxs-lookup"><span data-stu-id="0b336-195">The creation of pending invoices occurs in the background (as an asynchronous operation).</span></span>

### <a name="shared-service-vs-organization-based-exception-processing"></a><span data-ttu-id="0b336-196">共有サービス対組織に基づく例外処理</span><span class="sxs-lookup"><span data-stu-id="0b336-196">Shared service vs. organization-based exception processing</span></span>

<span data-ttu-id="0b336-197">[例外リスト] ページは、**データ管理**ワークスペースがステージング レコードの処理でサポートする標準セキュリティ構造をサポートします。</span><span class="sxs-lookup"><span data-stu-id="0b336-197">The exceptions list page supports the standard security constructs that the **Data management** workspace supports for the processing of staging records.</span></span> <span data-ttu-id="0b336-198">請求書のインポート ジョブは、次の方法でセキュリティ保護できます。</span><span class="sxs-lookup"><span data-stu-id="0b336-198">The invoice import job can be secured in the following ways:</span></span>

+ <span data-ttu-id="0b336-199">ユーザー ロールごと</span><span class="sxs-lookup"><span data-stu-id="0b336-199">By user role</span></span>
+ <span data-ttu-id="0b336-200">ユーザー別</span><span class="sxs-lookup"><span data-stu-id="0b336-200">By user</span></span>
+ <span data-ttu-id="0b336-201">法人ごと</span><span class="sxs-lookup"><span data-stu-id="0b336-201">By legal entity</span></span>

![ユーザー ロールごと、および法人ごとで保護されているインポート ジョブ](media/vendor_invoice_automation_04.png)

<span data-ttu-id="0b336-203">請求書インポート ジョブのセキュリティを構成すると、[例外リスト] ページはその設定に従います。</span><span class="sxs-lookup"><span data-stu-id="0b336-203">If security is configured for the invoice import job, the exceptions list page honors those settings.</span></span> <span data-ttu-id="0b336-204">表示されるように設定された請求書例外レコードのみが表示されます。</span><span class="sxs-lookup"><span data-stu-id="0b336-204">Users will be able to see only the invoice exception records that this setup allows them to see.</span></span>

<span data-ttu-id="0b336-205">たとえば、Contoso は法人ごとに請求書の例外を処理することにしました。</span><span class="sxs-lookup"><span data-stu-id="0b336-205">For example, Contoso has decided to process invoice exceptions by legal entity.</span></span> <span data-ttu-id="0b336-206">この場合、法人 A のユーザーは法人 A の請求書例外のみが表示されるように、法人 B のユーザーは、法人 B の請求書例外だけを見ることができるように、請求書インポート ジョブのセキュリティを構成します。この設定により、請求書の例外管理の職務分掌が実現できます。</span><span class="sxs-lookup"><span data-stu-id="0b336-206">Therefore, security is configured on the invoice import job in such a way that a user in legal entity A can see only invoice exceptions in legal entity A, whereas a user in legal entity B can see only invoice exceptions in legal entity B. This setup enables segregation of duties for the management of invoice exceptions.</span></span>

<span data-ttu-id="0b336-207">Contoso がセキュリティを適用しない場合、同じユーザーがすべての法人の請求書の例外を処理できます。</span><span class="sxs-lookup"><span data-stu-id="0b336-207">Contoso could also decide not to enforce any security, so that the same users can process invoice exceptions for all legal entities.</span></span> <span data-ttu-id="0b336-208">この設定では、請求書の例外管理の共有サービス シナリオを実現できます。</span><span class="sxs-lookup"><span data-stu-id="0b336-208">This setup enables a shared services scenario for the management of invoice exceptions.</span></span>

## <a name="side-by-side-attachment-viewer"></a><span data-ttu-id="0b336-209">添付ファイルを並べて表示するビューアー</span><span class="sxs-lookup"><span data-stu-id="0b336-209">Side-by-side attachment viewer</span></span>

<span data-ttu-id="0b336-210">仕入先請求書の添付ファイルを簡単に表示するため、請求書作成プロセスで現在使用される次のページでは、添付ファイル ビューアーを提供します。</span><span class="sxs-lookup"><span data-stu-id="0b336-210">To help you easily view the attachments for vendor invoices, the following pages that are used in the invoicing process now provide an attachment viewer:</span></span>

+ <span data-ttu-id="0b336-211">**例外処理**</span><span class="sxs-lookup"><span data-stu-id="0b336-211">**Exception handling**</span></span>
+ <span data-ttu-id="0b336-212">**保留中の仕入先請求書** ページ (請求書の確認プロセスでも使用可能)</span><span class="sxs-lookup"><span data-stu-id="0b336-212">**Pending vendor invoices** page (also available in the invoice review process)</span></span>
+ <span data-ttu-id="0b336-213">**請求仕訳帳**照会ページ (転記された請求書)</span><span class="sxs-lookup"><span data-stu-id="0b336-213">**Invoice journal** inquiry page (for posted invoices)</span></span>

<span data-ttu-id="0b336-214">添付ファイル ビューアーが提供する主な機能を以下に示します。</span><span class="sxs-lookup"><span data-stu-id="0b336-214">Here is the main functionality that the attachment viewer provides:</span></span>

+ <span data-ttu-id="0b336-215">ドキュメント管理がサポートするすべての添付ファイル タイプ (ファイル、画像、URL、およびメモ) を表示します。</span><span class="sxs-lookup"><span data-stu-id="0b336-215">View all attachment types that Document management supports (files, images, URLs, and notes).</span></span>
+ <span data-ttu-id="0b336-216">複数ページの TIFF ファイルを表示します。</span><span class="sxs-lookup"><span data-stu-id="0b336-216">View multi-page TIFF files.</span></span>
+ <span data-ttu-id="0b336-217">イメージ ファイルには、次のアクションを実行できます。</span><span class="sxs-lookup"><span data-stu-id="0b336-217">Perform the following actions on image files:</span></span>
  + <span data-ttu-id="0b336-218">画像の一部を強調表示します。</span><span class="sxs-lookup"><span data-stu-id="0b336-218">Highlight parts of the image.</span></span>
  + <span data-ttu-id="0b336-219">画像の一部をブロックします。</span><span class="sxs-lookup"><span data-stu-id="0b336-219">Block parts of the image.</span></span>
  + <span data-ttu-id="0b336-220">イメージに注釈を追加します。</span><span class="sxs-lookup"><span data-stu-id="0b336-220">Add annotations to the image.</span></span>
  + <span data-ttu-id="0b336-221">画像を拡大/縮小します。</span><span class="sxs-lookup"><span data-stu-id="0b336-221">Zoom in and out on the image.</span></span>
  + <span data-ttu-id="0b336-222">画像を移動します。</span><span class="sxs-lookup"><span data-stu-id="0b336-222">Pan the image.</span></span>
  + <span data-ttu-id="0b336-223">操作の取り消し、やり直しができます。</span><span class="sxs-lookup"><span data-stu-id="0b336-223">Undo and redo actions.</span></span>
  + <span data-ttu-id="0b336-224">画像をサイズに合わせます。</span><span class="sxs-lookup"><span data-stu-id="0b336-224">Fit the image to size.</span></span>

> [!NOTE]
> <span data-ttu-id="0b336-225">これらのアクションは、画像ファイル (JPEG、TIFF、PNG など) でのみ使用できます。</span><span class="sxs-lookup"><span data-stu-id="0b336-225">These actions are available only for image files (JPEG, TIFF, PNG, and so on).</span></span> <span data-ttu-id="0b336-226">これらのアクションを使用して画像に対して行う変更は、画像ファイルに保存されます。</span><span class="sxs-lookup"><span data-stu-id="0b336-226">Any changes that you make to an image by using these actions are saved to the image file.</span></span> <span data-ttu-id="0b336-227">現時点では、添付ファイル ビューアーにバージョン管理や監査機能は含まれていません。</span><span class="sxs-lookup"><span data-stu-id="0b336-227">Currently, the attachment viewer doesn’t include versioning or auditing capabilities.</span></span>

### <a name="default-attachment"></a><span data-ttu-id="0b336-228">既定の添付ファイル</span><span class="sxs-lookup"><span data-stu-id="0b336-228">Default attachment</span></span>

<span data-ttu-id="0b336-229">仕入先請求書に複数のファイルが添付されている場合、**添付ファイル** ページで、ドキュメントのいずれかを既定の添付ファイルとして設定できます。</span><span class="sxs-lookup"><span data-stu-id="0b336-229">If a vendor invoice has more than one attachment, you can set one of the documents as the default attachment on the **Attachments** page.</span></span> <span data-ttu-id="0b336-230">**既定の添付ファイルです** オプションは、この機能の一部として追加された新しいオプションです。</span><span class="sxs-lookup"><span data-stu-id="0b336-230">The **Is default attachment** option is a new option that was added as part of this feature.</span></span> <span data-ttu-id="0b336-231">このオプションは、仕入先請求書ドキュメントの添付ファイル データ エンティティでも公開されます。</span><span class="sxs-lookup"><span data-stu-id="0b336-231">This option is also exposed in the Vendor invoice document attachment data entity.</span></span> <span data-ttu-id="0b336-232">したがって、既定の添付ファイルは統合により設定できます。</span><span class="sxs-lookup"><span data-stu-id="0b336-232">Therefore, the default attachment can be set through integrations.</span></span>

<span data-ttu-id="0b336-233">1 つのドキュメントだけを、既定の添付ファイルとして設定できます。</span><span class="sxs-lookup"><span data-stu-id="0b336-233">Only one document can be set as the default attachment.</span></span> <span data-ttu-id="0b336-234">既定の添付ファイルとしてドキュメントを設定した後は、請求書を開いたときに自動的に添付ファイル ビューアーに表示されます。</span><span class="sxs-lookup"><span data-stu-id="0b336-234">After you set a document as the default attachment, it’s automatically shown in the attachment viewer when the invoice is opened.</span></span> <span data-ttu-id="0b336-235">既定の添付ファイルとしてドキュメントを設定しなかった場合、請求書を開いても添付ファイル ビューアーにはどのファイルも自動的に表示されません。</span><span class="sxs-lookup"><span data-stu-id="0b336-235">If you don’t set any document as the default attachment, the viewer doesn’t automatically show any attachment when the invoice is opened.</span></span>

### <a name="showhide-invoice-attachments"></a><span data-ttu-id="0b336-236">請求書添付ファイルの表示/非表示</span><span class="sxs-lookup"><span data-stu-id="0b336-236">Show/hide invoice attachments</span></span>

<span data-ttu-id="0b336-237">**例外処理**、**保留中の請求書**、および **請求仕訳帳**照会ページに新たに表示されるボタンで、添付ファイル ビューアーの表示または非表示を切り替えられます。</span><span class="sxs-lookup"><span data-stu-id="0b336-237">A new button that is available on the **Exception processing**, **Pending invoice**, and **Invoice journal** inquiry pages lets you show or hide the attachment viewer.</span></span>

### <a name="security"></a><span data-ttu-id="0b336-238">セキュリティ</span><span class="sxs-lookup"><span data-stu-id="0b336-238">Security</span></span>

<span data-ttu-id="0b336-239">添付ファイル ビューアーの次のアクションは、ロール ベース セキュリティ経由で制御されます。</span><span class="sxs-lookup"><span data-stu-id="0b336-239">The following actions in the attachment viewer are controlled via role-based security:</span></span>

+ <span data-ttu-id="0b336-240">強調表示</span><span class="sxs-lookup"><span data-stu-id="0b336-240">Highlighting</span></span>
+ <span data-ttu-id="0b336-241">ブロック</span><span class="sxs-lookup"><span data-stu-id="0b336-241">Block</span></span>
+ <span data-ttu-id="0b336-242">注釈</span><span class="sxs-lookup"><span data-stu-id="0b336-242">Annotation</span></span>

### <a name="pending-vendor-invoices-page"></a><span data-ttu-id="0b336-243">[保留中の仕入先請求書] ページ</span><span class="sxs-lookup"><span data-stu-id="0b336-243">Pending vendor invoices page</span></span>

<span data-ttu-id="0b336-244">次の特権は、強調表示、ブロック、および注釈のアクションのための読み取り専用アクセスまたは読み取り/書き込みアクセスを添付ファイル ビューアーに提供します。</span><span class="sxs-lookup"><span data-stu-id="0b336-244">The following privileges provide ready-only access or read/write access to the attachment viewer for the highlighting, block, and annotation actions:</span></span>

+ <span data-ttu-id="0b336-245">**仕入先請求書の画像を管理** – この特権は読み取り/書き込みアクセスを提供します。</span><span class="sxs-lookup"><span data-stu-id="0b336-245">**Maintain vendor invoice image** – This privilege provides read/write access.</span></span>
+ <span data-ttu-id="0b336-246">**仕入先請求書の画像を表示** – この特権は読み取り専用アクセスを提供します。</span><span class="sxs-lookup"><span data-stu-id="0b336-246">**View vendor invoice image** – This privilege provides read-only access.</span></span>

<span data-ttu-id="0b336-247">次の職務は、それらのアクションに関して、添付ファイル ビューアーに読み取り専用アクセスまたは読み取り/書き込みアクセスを提供します。</span><span class="sxs-lookup"><span data-stu-id="0b336-247">The following duties provide read-only access or read/write access to the attachment viewer for those actions:</span></span>

+ <span data-ttu-id="0b336-248">**仕入先請求書の管理** – 仕入先請求書の画像管理権限はこの職務に割り当てられます。</span><span class="sxs-lookup"><span data-stu-id="0b336-248">**Maintain vendor invoices** – The Maintain vendor invoice image privilege is assigned to this duty.</span></span>
+ <span data-ttu-id="0b336-249">**仕入先請求書状態の照会** – 仕入先請求書の画像表示権限はこの職務に割り当てられます。</span><span class="sxs-lookup"><span data-stu-id="0b336-249">**Inquire into vendor invoice status** – The View vendor invoice image privilege is assigned to this duty.</span></span>

<span data-ttu-id="0b336-250">次のロールは、それらのアクションに関して、添付ファイル ビューアーに読み取り専用アクセスまたは読み取り/書き込みアクセスを提供します。</span><span class="sxs-lookup"><span data-stu-id="0b336-250">The following roles provide read-only access or read/write access to the attachment viewer for those actions:</span></span>

+ <span data-ttu-id="0b336-251">**買掛金勘定係**および**買掛金勘定マネージャー** – 仕入先請求書の管理職務がこれらのロールに割り当てられます。</span><span class="sxs-lookup"><span data-stu-id="0b336-251">**Accounts payable clerk** and **Accounts payable manager** – The Maintain vendor invoices duty is assigned to these roles.</span></span>
+ <span data-ttu-id="0b336-252">**買掛金勘定係**、**買掛金勘定マネージャー**、**買掛金勘定集中支払係**、および**買掛金勘定支払係** – 仕入先請求書状態の照会職務がこれらのロールに割り当てられます。</span><span class="sxs-lookup"><span data-stu-id="0b336-252">**Accounts payable clerk**, **Accounts payable manager**, **Accounts payable centralized payments clerk**, and **Accounts payable payments clerk** – The Inquire into vendor invoice status duty is assigned to these roles.</span></span>

### <a name="invoice-exception-details-page"></a><span data-ttu-id="0b336-253">[請求書例外の詳細] ページ</span><span class="sxs-lookup"><span data-stu-id="0b336-253">Invoice exception details page</span></span>

<span data-ttu-id="0b336-254">次の特権は、強調表示、ブロック、および注釈のアクションのための読み取り専用アクセスまたは読み取り/書き込みアクセスを添付ファイル ビューアーに提供します。</span><span class="sxs-lookup"><span data-stu-id="0b336-254">The following privileges provide ready-only access or read/write access to the attachment viewer for the highlighting, block, and annotation actions.</span></span>

> [!NOTE]
> <span data-ttu-id="0b336-255">このセクションに記載されているロールは、最初から添付ファイル ビューアーの請求書の画像の読み取り専用アクセスを提供します。</span><span class="sxs-lookup"><span data-stu-id="0b336-255">Out of the box, the roles that are mentioned in this section provide read-only access to the invoice images in the attachment viewer.</span></span> <span data-ttu-id="0b336-256">ロールに画像への書き込みアクセス権が必要な場合、ここに記載されている特権と職務を使用して、書き込みアクセスをそのロールに割り当てることができます。</span><span class="sxs-lookup"><span data-stu-id="0b336-256">If a role must also have write access to the images, you can grant write access to that role by using the privilege and duty that are described here.</span></span>

+ <span data-ttu-id="0b336-257">**仕入先請求書ヘッダー エンティティ画像の管理** – この特権は、添付ファイル ビューアーで請求書イメージへの読み取り/書き込みアクセスを提供します。</span><span class="sxs-lookup"><span data-stu-id="0b336-257">**Maintain vendor invoice header entity image** – This privilege provides read/write access to the invoice images in the attachment viewer.</span></span>
+ <span data-ttu-id="0b336-258">**仕入先請求書ヘッダー エンティティ画像の表示** – この特権は、添付ファイル ビューアーで請求書イメージへの読み取り専用表示を提供します。</span><span class="sxs-lookup"><span data-stu-id="0b336-258">**View vendor invoice header entity image** – This privilege provides read-only view to the invoice image in the attachment viewer.</span></span>

<span data-ttu-id="0b336-259">次の職務は、それらのアクションに関して、添付ファイル ビューアーに読み取り専用アクセスを提供します。</span><span class="sxs-lookup"><span data-stu-id="0b336-259">The following duties provide read-only access to the attachment viewer for those actions:</span></span>

+ <span data-ttu-id="0b336-260">**仕入先請求書の管理** – 仕入先請求書ヘッダー エンティティ画像管理特権はこの職務に割り当てられます。</span><span class="sxs-lookup"><span data-stu-id="0b336-260">**Maintain vendor invoices** – The Maintain vendor invoice header entity image privilege is assigned to this duty.</span></span>

<span data-ttu-id="0b336-261">次のロールは、それらのアクションに関して、添付ファイル ビューアーに読み取り専用アクセスを提供します。</span><span class="sxs-lookup"><span data-stu-id="0b336-261">The following roles provide read-only access to the attachment viewer for those actions:</span></span>

+ <span data-ttu-id="0b336-262">**買掛金勘定係**および**買掛金勘定マネージャー** – 仕入先請求書の管理職務がこれらのロールに割り当てられます。</span><span class="sxs-lookup"><span data-stu-id="0b336-262">**Accounts payable clerk** and **Accounts payable manager** – The Maintain vendor invoices duty is assigned to these roles.</span></span>

<span data-ttu-id="0b336-263">既定では、ユーザー ロールが任意のページでの編集権限を提供している場合、ユーザーは添付ファイル ビューアーでの強調表示、ブロック、およびコメント アクションの編集権限も有します。</span><span class="sxs-lookup"><span data-stu-id="0b336-263">By default, if the user role provides edit rights on any page, the user will also have edit rights on the attachments viewer for the highlighting, block, and annotation actions.</span></span> <span data-ttu-id="0b336-264">ただし、ページの編集権限があるものの添付ファイル ビューアーの編集権限を持たない特定のロールが必要なシナリオの場合、このユース ケースの必要を満たすためには前のリストから適切な権限を使用することができます。</span><span class="sxs-lookup"><span data-stu-id="0b336-264">However, if there are scenarios where a specific role should have edit rights on the page but not on the attachment viewer, the appropriate privileges from the preceding list can be used to satisfy the use case.</span></span>
