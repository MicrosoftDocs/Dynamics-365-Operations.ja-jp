---
title: 原産国の USMCA 証明書
description: この機能を使用すると、米国 - メキシコ - カナダ協定 (USMCA) によって要求される原産国ドキュメントを印刷できます。
author: Henrikan
manager: tfehr
ms.date: 10/23/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: henrikan
ms.search.validFrom: 2020-10-23
ms.dyn365.ops.version: Release 10.0.16
ms.openlocfilehash: 2263b3643becedd68911e2325c60ed4d97d6e823
ms.sourcegitcommit: ffb5998e611b83c2e4f98323f39e3e8f6419c652
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/02/2020
ms.locfileid: "4432435"
---
# <a name="usmca-certification-of-origin"></a><span data-ttu-id="ec674-103">原産国の USMCA 証明書</span><span class="sxs-lookup"><span data-stu-id="ec674-103">USMCA certification of origin</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="ec674-104">この機能を使用すると、米国 - メキシコ - カナダ協定 (USMCA) によって要求される原産国ドキュメントを印刷できます。</span><span class="sxs-lookup"><span data-stu-id="ec674-104">This feature lets you print the certification of origin documents required by the United States-Mexico-Canada Agreement (USMCA).</span></span>

<span data-ttu-id="ec674-105">*原産国の USMCA 証明書ドキュメント* には、申告に必要なデータ要素が最低限含まれています。</span><span class="sxs-lookup"><span data-stu-id="ec674-105">The *USMCA certification of origin document* contains the minimum data elements required for declaration.</span></span> <span data-ttu-id="ec674-106">一部のデータ要素は印刷の前に事前に入力できますが、他の要素は印刷後に手動で入力する必要があります。</span><span class="sxs-lookup"><span data-stu-id="ec674-106">Some data elements can be pre-filled before printing while others must be filled in manually after printing.</span></span> <span data-ttu-id="ec674-107">優先順位の処理を行うには、申告時に、ドキュメントに入力されていて輸入者が所有している必要があります。</span><span class="sxs-lookup"><span data-stu-id="ec674-107">To obtain preferential tariff treatment, the document must be completed and in the possession of the importer at the time the declaration is made.</span></span> <span data-ttu-id="ec674-108">このドキュメントは、輸入者、輸出者、または生産者で入力することができます。</span><span class="sxs-lookup"><span data-stu-id="ec674-108">The document may be completed by the importer, exporter, or producer.</span></span>

<span data-ttu-id="ec674-109">**すべての出荷** リスト ページまたは **出荷の詳細** ページから、1 つの出荷のドキュメントを印刷できます。</span><span class="sxs-lookup"><span data-stu-id="ec674-109">You can print the document for a single shipment from the **All shipments** list page or from the **Shipment details** page.</span></span>

<span data-ttu-id="ec674-110">ドキュメントには、法人の基本住所の国が米国である場合にのみアクセスできます。</span><span class="sxs-lookup"><span data-stu-id="ec674-110">The document is only accessible when the country on the primary address for the legal entity is the United States.</span></span>

<span data-ttu-id="ec674-111">ドキュメントの印刷選択に応じて、システムからのデータをドキュメントにあらかじめ入力しておくことができます。</span><span class="sxs-lookup"><span data-stu-id="ec674-111">Depending on the document print selection, the document can be pre-filled with data from your system.</span></span> <span data-ttu-id="ec674-112">印刷されたドキュメントを、Microsoft Word などの編集可能な形式にエクスポートすることによって、印刷ドキュメントに変更または追加することができます。</span><span class="sxs-lookup"><span data-stu-id="ec674-112">It is possible to change or add data to the printed document by exporting the printed document to an editable format, such as Microsoft Word.</span></span> <span data-ttu-id="ec674-113">エクスポート後に、申告を行う前に必要な変更を適用できます。</span><span class="sxs-lookup"><span data-stu-id="ec674-113">After export, you can apply any required changes before a declaration is made.</span></span>

## <a name="turn-on-the-usmca-feature"></a><span data-ttu-id="ec674-114">USMCA 機能をオンにする</span><span class="sxs-lookup"><span data-stu-id="ec674-114">Turn on the USMCA feature</span></span>

<span data-ttu-id="ec674-115">USMCA 機能を使用するには、システム上で有効化する必要があります。</span><span class="sxs-lookup"><span data-stu-id="ec674-115">Before you can use the USMCA feature, it must be turned on in your system.</span></span> <span data-ttu-id="ec674-116">管理者は、[機能管理](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) 設定を使用して、機能の状態を確認し、有効にすることができます。</span><span class="sxs-lookup"><span data-stu-id="ec674-116">Admins can use the [feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) settings to check the status of the feature and turn it on.</span></span> <span data-ttu-id="ec674-117">**機能管理** ワークスペースで、この機能は次のようにリストされています。</span><span class="sxs-lookup"><span data-stu-id="ec674-117">In the **Feature management** workspace, the feature is listed in the following way:</span></span>

- <span data-ttu-id="ec674-118">**モジュール:** *輸送管理*</span><span class="sxs-lookup"><span data-stu-id="ec674-118">**Module:** *Transportation management*</span></span>
- <span data-ttu-id="ec674-119">**機能名:** *原産国の USMCA 証明書ドキュメント*</span><span class="sxs-lookup"><span data-stu-id="ec674-119">**Feature name:** *USMCA certification of origin document*</span></span>

## <a name="document-content"></a><span data-ttu-id="ec674-120">ドキュメントのコンテンツ</span><span class="sxs-lookup"><span data-stu-id="ec674-120">Document content</span></span>

<span data-ttu-id="ec674-121">原産国の USMCA 証明書ドキュメントには、次のデータ要素が含まれています。</span><span class="sxs-lookup"><span data-stu-id="ec674-121">The USMCA certification of origin document contains the following data elements:</span></span>

- <span data-ttu-id="ec674-122">住所要素</span><span class="sxs-lookup"><span data-stu-id="ec674-122">Address elements</span></span>
- <span data-ttu-id="ec674-123">証明関係者の役割</span><span class="sxs-lookup"><span data-stu-id="ec674-123">Role of the certifying party</span></span>
- <span data-ttu-id="ec674-124">1 つの出荷</span><span class="sxs-lookup"><span data-stu-id="ec674-124">Single shipment</span></span>
- <span data-ttu-id="ec674-125">請求書</span><span class="sxs-lookup"><span data-stu-id="ec674-125">Invoices</span></span>
- <span data-ttu-id="ec674-126">空白の期間</span><span class="sxs-lookup"><span data-stu-id="ec674-126">Blanket period</span></span>
- <span data-ttu-id="ec674-127">項目の詳細</span><span class="sxs-lookup"><span data-stu-id="ec674-127">Item details</span></span>
- <span data-ttu-id="ec674-128">証明者の署名</span><span class="sxs-lookup"><span data-stu-id="ec674-128">Certifier signature</span></span>
- <span data-ttu-id="ec674-129">ページ数</span><span class="sxs-lookup"><span data-stu-id="ec674-129">Number of pages</span></span>

<span data-ttu-id="ec674-130">これらの各要素の詳細とその値については、このトピックの残りのセクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="ec674-130">For more information about each of these elements and how their values are found, see the remaining sections in this topic.</span></span>

## <a name="print-a-usmca-certification-of-origin-document"></a><span data-ttu-id="ec674-131">原産国の USMCA 証明書ドキュメントの印刷</span><span class="sxs-lookup"><span data-stu-id="ec674-131">Print a USMCA certification of origin document</span></span>

<span data-ttu-id="ec674-132">出荷のための原産国の USMCA 証明書ドキュメントを印刷するには、次の操作を行います。</span><span class="sxs-lookup"><span data-stu-id="ec674-132">To print a USMCA certification of origin document for a shipment, do the following:</span></span>

1. <span data-ttu-id="ec674-133">次のどちらかを実行します。</span><span class="sxs-lookup"><span data-stu-id="ec674-133">Do one of the following:</span></span>
    - <span data-ttu-id="ec674-134">**輸送管理 > 出荷 > すべての出荷** に移動し、ドキュメントを印刷する出荷を選択します。</span><span class="sxs-lookup"><span data-stu-id="ec674-134">Go to **Transportation management> Shipments > All shipments** and select the shipment you want to print the document for.</span></span>
    - <span data-ttu-id="ec674-135">ドキュメントを印刷する出荷の **出荷の詳細** ページを開きます (**すべての出荷** ページなど、次のいずれかの方法を使用することができます)。</span><span class="sxs-lookup"><span data-stu-id="ec674-135">Open the **Shipment details** page for the shipment you want to print the document for (there are several ways to get here, including from the **All shipments** page).</span></span>
1. <span data-ttu-id="ec674-136">アクション ウィンドウで、**出荷** タブを開き、**印刷** グループから **原産国の USMCA 証明書** を選択します。</span><span class="sxs-lookup"><span data-stu-id="ec674-136">On the Action Pane, open the **Shipments** tab and, from the **Print** group, select **USMCA certificate of origin**.</span></span>
1. <span data-ttu-id="ec674-137">**証明書または原産国** ダイアログ ボックスが開きます。</span><span class="sxs-lookup"><span data-stu-id="ec674-137">The **Certificate or origin** dialog box opens.</span></span> <span data-ttu-id="ec674-138">次のサブセクションで説明されている設定を行い、**OK** を選択してドキュメントを生成します。</span><span class="sxs-lookup"><span data-stu-id="ec674-138">Make the settings described in the following subsections and then select **OK** to generate the document.</span></span>
1. <span data-ttu-id="ec674-139">ドキュメントのプレビューが開きます。</span><span class="sxs-lookup"><span data-stu-id="ec674-139">A preview of the document opens.</span></span> <span data-ttu-id="ec674-140">必要に応じて、アクション ウィンドウに表示されるコマンドを使用して、ドキュメントを印刷またはエクスポートします。</span><span class="sxs-lookup"><span data-stu-id="ec674-140">Use the commands provided on the Action Pane to print or export the document as needed.</span></span>

### <a name="certifying-party"></a><span data-ttu-id="ec674-141">証明関係者</span><span class="sxs-lookup"><span data-stu-id="ec674-141">Certifying party</span></span>

<span data-ttu-id="ec674-142">**証明関係者** ドロップダウン リストを使用して、ドキュメントを印刷する関係者のタイプを識別します。</span><span class="sxs-lookup"><span data-stu-id="ec674-142">Use the **Certifying party** drop-down list to identify the type  of party that is printing the document.</span></span> <span data-ttu-id="ec674-143">証明書関係者が *輸出者*、*輸出者または生産者*、*生産者*、または *輸出者* のいずれであるかを指定します。または、認証当事者がこれらを指定していない場合は、空白のままにしておきます。</span><span class="sxs-lookup"><span data-stu-id="ec674-143">Specify whether the certifying party is the *Exporter*, *Exporter and Producer*, *Producer*, or *Importer*; or leave it blank if the certifying party is none of these.</span></span> <span data-ttu-id="ec674-144">選択したオプションによって、ドキュメントの住所セクションに印刷される内容が決まります。</span><span class="sxs-lookup"><span data-stu-id="ec674-144">The option you select determines what is printed in the address sections of the document.</span></span>

<span data-ttu-id="ec674-145">選択した **証明書当事者** は、印刷されたドキュメントに含められます。</span><span class="sxs-lookup"><span data-stu-id="ec674-145">The **Certifying party** that you choose will be included in the printed document.</span></span>

<span data-ttu-id="ec674-146">ドキュメントは、入庫出荷と出庫出荷の両方に対して印刷できます。</span><span class="sxs-lookup"><span data-stu-id="ec674-146">The document can be printed for both inbound and outbound shipments.</span></span> <span data-ttu-id="ec674-147">入庫出荷の **証明当事者** として *輸入者* を選択します。</span><span class="sxs-lookup"><span data-stu-id="ec674-147">Select *Importer* as **Certifying party** for inbound shipments only.</span></span>

<span data-ttu-id="ec674-148">次の表では、選択した **証明当事者** に基づいてドキュメントに含まれる情報の種類について説明します。</span><span class="sxs-lookup"><span data-stu-id="ec674-148">The following table describes the types of information that are included in the document based on the **Certifying party** that you choose.</span></span>

| <span data-ttu-id="ec674-149">証明関係者&nbsp;</span><span class="sxs-lookup"><span data-stu-id="ec674-149">Certifying&nbsp;party</span></span> | <span data-ttu-id="ec674-150">説明</span><span class="sxs-lookup"><span data-stu-id="ec674-150">Description</span></span> |
|---|---|
| <span data-ttu-id="ec674-151">*\[空白\]*</span><span class="sxs-lookup"><span data-stu-id="ec674-151">*\[Blank\]*</span></span> | <span data-ttu-id="ec674-152">ドキュメントに次の詳細を追加します。</span><span class="sxs-lookup"><span data-stu-id="ec674-152">Adds the following details to the document:</span></span><ul><li><span data-ttu-id="ec674-153">**証明者の詳細**: 配送倉庫の住所の詳細を使用します (存在する場合)。それ以外の場合は、出荷サイトの住所が使用されます。それ以外の場合は、Supply Chain Management で選択した法人 (会社) の住所が使用されます。</span><span class="sxs-lookup"><span data-stu-id="ec674-153">**Certifier details**: Uses the address details for the shipping warehouse, if available; otherwise it uses the shipping site address, if available; otherwise it uses the address of the legal entity (company) selected in Supply Chain Management.</span></span></li><li><span data-ttu-id="ec674-154">**輸出者の詳細**: 空白</span><span class="sxs-lookup"><span data-stu-id="ec674-154">**Exporter details**: Blank</span></span></li><li><span data-ttu-id="ec674-155">**生産者の詳細**: 空白</span><span class="sxs-lookup"><span data-stu-id="ec674-155">**Producer details**: Blank</span></span></li><li><span data-ttu-id="ec674-156">**輸入者の詳細**: 空白</span><span class="sxs-lookup"><span data-stu-id="ec674-156">**Importer details**: Blank</span></span></li><ul>|
| <span data-ttu-id="ec674-157">*輸出者*</span><span class="sxs-lookup"><span data-stu-id="ec674-157">*Exporter*</span></span> | <span data-ttu-id="ec674-158">ドキュメントに次の詳細を追加します。</span><span class="sxs-lookup"><span data-stu-id="ec674-158">Adds the following details to the document:</span></span><ul><li><span data-ttu-id="ec674-159">**証明者の詳細**: 配送倉庫の住所の詳細を使用します (存在する場合)。それ以外の場合は、出荷サイトの住所が使用されます。それ以外の場合は、Supply Chain Management で選択した法人 (会社) の住所が使用されます。</span><span class="sxs-lookup"><span data-stu-id="ec674-159">**Certifier details**: Uses the address details for the shipping warehouse, if available; otherwise it uses the shipping site address, if available; otherwise it uses the address of the legal entity (company) selected in Supply Chain Management.</span></span></li><li><span data-ttu-id="ec674-160">**輸出者の詳細**: 法人の住所の詳細を使用します。</span><span class="sxs-lookup"><span data-stu-id="ec674-160">**Exporter details**: Uses the address details for the legal entity.</span></span></li><li><span data-ttu-id="ec674-161">**生産者の詳細**: 空白</span><span class="sxs-lookup"><span data-stu-id="ec674-161">**Producer details**: Blank</span></span></li><li><span data-ttu-id="ec674-162">**輸入者の詳細**: 関連する販売注文の請求先/元 ID を使用します。</span><span class="sxs-lookup"><span data-stu-id="ec674-162">**Importer details**: Uses the invoice account for the related sales order.</span></span></li><ul>|
| <span data-ttu-id="ec674-163">*輸出者と生産者*</span><span class="sxs-lookup"><span data-stu-id="ec674-163">*Exporter and Producer*</span></span> | <span data-ttu-id="ec674-164">ドキュメントに次の詳細を追加します。</span><span class="sxs-lookup"><span data-stu-id="ec674-164">Adds the following details to the document:</span></span><ul><li><span data-ttu-id="ec674-165">**証明者の詳細**: 配送倉庫の住所の詳細を使用します (存在する場合)。それ以外の場合は、出荷サイトの住所が使用されます。それ以外の場合は、Supply Chain Management で選択した法人 (会社) の住所が使用されます。</span><span class="sxs-lookup"><span data-stu-id="ec674-165">**Certifier details**: Uses the address details for the shipping warehouse, if available; otherwise it uses the shipping site address, if available; otherwise it uses the address of the legal entity (company) selected in Supply Chain Management.</span></span></li><li><span data-ttu-id="ec674-166">**輸出者の詳細**: 法人の住所の詳細を使用します。</span><span class="sxs-lookup"><span data-stu-id="ec674-166">**Exporter details**: Uses the address details for the legal entity.</span></span></li><li><span data-ttu-id="ec674-167">**生産者の詳細**: 法人の住所の詳細を使用します。</span><span class="sxs-lookup"><span data-stu-id="ec674-167">**Producer details**: Uses the address details for the legal entity.</span></span></li><li><span data-ttu-id="ec674-168">**輸入者の詳細**: 関連する販売注文の請求先/元 ID を使用します。</span><span class="sxs-lookup"><span data-stu-id="ec674-168">**Importer details**: Uses the invoice account for the related sales order.</span></span></li><ul>|
| <span data-ttu-id="ec674-169">*輸入者*</span><span class="sxs-lookup"><span data-stu-id="ec674-169">*Importer*</span></span> | <span data-ttu-id="ec674-170">ドキュメントに次の詳細を追加します。</span><span class="sxs-lookup"><span data-stu-id="ec674-170">Adds the following details to the document:</span></span><ul><li><span data-ttu-id="ec674-171">**証明者の詳細**: 配送倉庫の住所の詳細を使用します (存在する場合)。それ以外の場合は、出荷サイトの住所が使用されます。それ以外の場合は、Supply Chain Management で選択した法人 (会社) の住所が使用されます。</span><span class="sxs-lookup"><span data-stu-id="ec674-171">**Certifier details**: Uses the address details for the shipping warehouse, if available; otherwise it uses the shipping site address, if available; otherwise it uses the address of the legal entity (company) selected in Supply Chain Management.</span></span></li><li><span data-ttu-id="ec674-172">**輸出者の詳細**: 空白</span><span class="sxs-lookup"><span data-stu-id="ec674-172">**Exporter details**: Blank</span></span></li><li><span data-ttu-id="ec674-173">**生産者の詳細**: 空白</span><span class="sxs-lookup"><span data-stu-id="ec674-173">**Producer details**: Blank</span></span></li><li><span data-ttu-id="ec674-174">**輸入者の詳細**: 法人の住所の詳細を使用します。</span><span class="sxs-lookup"><span data-stu-id="ec674-174">**Importer details**:  Uses the address details for the legal entity.</span></span></li><ul>|
| <span data-ttu-id="ec674-175">*生産者*</span><span class="sxs-lookup"><span data-stu-id="ec674-175">*Producer*</span></span> | <span data-ttu-id="ec674-176">ドキュメントに次の詳細を追加します。</span><span class="sxs-lookup"><span data-stu-id="ec674-176">Adds the following details to the document:</span></span><ul><li><span data-ttu-id="ec674-177">**証明者の詳細**: 配送倉庫の住所の詳細を使用します (存在する場合)。それ以外の場合は、出荷サイトの住所が使用されます。それ以外の場合は、Supply Chain Management で選択した法人の住所が使用されます。</span><span class="sxs-lookup"><span data-stu-id="ec674-177">**Certifier details**: Uses the address details for the shipping warehouse, if available; otherwise it uses the shipping site address, if available; otherwise it uses the address of the legal entity selected in Supply Chain Management.</span></span></li><li><span data-ttu-id="ec674-178">**輸出者の詳細**: 空白</span><span class="sxs-lookup"><span data-stu-id="ec674-178">**Exporter details**: Blank</span></span></li><li><span data-ttu-id="ec674-179">**生産者の詳細**: 法人の住所の詳細を使用します。</span><span class="sxs-lookup"><span data-stu-id="ec674-179">**Producer details**:  Uses the address details for the legal entity.</span></span></li><li><span data-ttu-id="ec674-180">**輸入者の詳細**: 空白</span><span class="sxs-lookup"><span data-stu-id="ec674-180">**Importer details**: Blank</span></span></li><ul>|

### <a name="has-various-producers"></a><span data-ttu-id="ec674-181">さまざまな生産者を持つ</span><span class="sxs-lookup"><span data-stu-id="ec674-181">Has various producers</span></span>

<span data-ttu-id="ec674-182">**証明関係者** ドロップダウン リストは、ドキュメントの生産者の詳細に使用されるテキストを制御します。</span><span class="sxs-lookup"><span data-stu-id="ec674-182">The **Certifying party** drop-down list controls the text to be used for the producer details in the document.</span></span> <span data-ttu-id="ec674-183">次のいずれかを選択します : </span><span class="sxs-lookup"><span data-stu-id="ec674-183">Choose one of the following:</span></span>

- <span data-ttu-id="ec674-184">*多数の生産者*: 生産者の詳細にテキスト "多数" を印刷します。</span><span class="sxs-lookup"><span data-stu-id="ec674-184">*Various producers* - Prints the text "Various" in the producer details.</span></span>
- <span data-ttu-id="ec674-185">*要求時に使用可能*: 生産者の詳細で、"輸入機関から要求された場合に使用可能" というテキストを印刷します。</span><span class="sxs-lookup"><span data-stu-id="ec674-185">*Available upon request* - Prints the text "Available upon request by the importing authorities" in the producer details.</span></span>

<span data-ttu-id="ec674-186">**証明関係者** が *輸出者または生産者* または *生産者* に設定されている場合、**多数の生産者あり** 設定が上書きされ、生産者の住所の詳細が証明者と同じになります。</span><span class="sxs-lookup"><span data-stu-id="ec674-186">When the **Certifying party** is set to *Exporter and Producer* or *Producer*, then the **Has various producers** setting is overruled, and the producer address details will be the same as the certifier.</span></span>

### <a name="blanket-period"></a><span data-ttu-id="ec674-187">空白の期間</span><span class="sxs-lookup"><span data-stu-id="ec674-187">Blanket period</span></span>

<span data-ttu-id="ec674-188">ドキュメントが 1 つの出荷に対して印刷される場合でも、**一括期間 (開始)** および **一括期間 (終了)** 設定を使用して、ドキュメントが同じ商品の複数の出荷をカバーする一括期間を設定します。</span><span class="sxs-lookup"><span data-stu-id="ec674-188">Use the **Blanket period from** and **Blanket period to** settings to establish a blanket period, during which the document will cover multiple shipments of identical goods, even though the document is printed for only one shipment.</span></span> <span data-ttu-id="ec674-189">一括期間の日付を制約なしで設定し、それをドキュメントに追加することができます。</span><span class="sxs-lookup"><span data-stu-id="ec674-189">You can set the blanket period dates without any constraints, and it will be added to the document.</span></span> <span data-ttu-id="ec674-190">これらの設定は、空白のままにしておくことも、過去に設定することもできます。</span><span class="sxs-lookup"><span data-stu-id="ec674-190">You can also leave these settings blank or set them in the past.</span></span>

### <a name="is-single-shipment"></a><span data-ttu-id="ec674-191">1 つの出荷である</span><span class="sxs-lookup"><span data-stu-id="ec674-191">Is single shipment</span></span>

<span data-ttu-id="ec674-192">**原産国の証明書** ダイアログ ボックスで、**1 つの出荷である** を次のいずれかに設定します。</span><span class="sxs-lookup"><span data-stu-id="ec674-192">In the **Certificate of origin** dialog box, set **Is single shipment** to one of the following:</span></span>

- <span data-ttu-id="ec674-193">*はい*: 請求書番号の横に [1 つの出荷: はい] を追加します。</span><span class="sxs-lookup"><span data-stu-id="ec674-193">*Yes* - Adds "Single Shipment: Yes" next to the invoice number.</span></span>
- <span data-ttu-id="ec674-194">*いいえ*: 何も追加しません。</span><span class="sxs-lookup"><span data-stu-id="ec674-194">*No* - Adds nothing.</span></span>

## <a name="other-information-included-in-the-document"></a><span data-ttu-id="ec674-195">ドキュメントに含まれるその他の情報</span><span class="sxs-lookup"><span data-stu-id="ec674-195">Other information included in the document</span></span>

<span data-ttu-id="ec674-196">**原産国の証明書** ダイアログ ボックスを使用して選択したオプションの要素に加えて、原産国の USMSA 証明書ドキュメントには、次のサブセクションで集計された情報とユーザー設定フィールドが含められます。</span><span class="sxs-lookup"><span data-stu-id="ec674-196">In addition to the optional elements that you select using the **Certificate or origin** dialog box, the USMCA certification of origin document will include the information and custom fields summarized in the following subsections.</span></span> <span data-ttu-id="ec674-197">この情報の一部は、ドキュメントの生成後に手動で入力する必要があります。</span><span class="sxs-lookup"><span data-stu-id="ec674-197">Some of this information must be entered manually after you generate the document.</span></span>

### <a name="invoice-number"></a><span data-ttu-id="ec674-198">請求書番号</span><span class="sxs-lookup"><span data-stu-id="ec674-198">Invoice number</span></span>

<span data-ttu-id="ec674-199">出荷に関連する売上請求書の ID は、一括期間に関係なくドキュメントに印刷されます。</span><span class="sxs-lookup"><span data-stu-id="ec674-199">The IDs of sales invoices related to shipments are printed on the document irrespective of the blanket period.</span></span> <span data-ttu-id="ec674-200">請求書番号は、**1 つの出荷である** の選択に関係なく印刷されます。</span><span class="sxs-lookup"><span data-stu-id="ec674-200">Invoice numbers are printed irrespective of the **Is single shipment** selection.</span></span>

### <a name="item-details"></a><span data-ttu-id="ec674-201">項目の詳細</span><span class="sxs-lookup"><span data-stu-id="ec674-201">Item details</span></span>

<span data-ttu-id="ec674-202">このドキュメントには、特定の品目の詳細を一覧表示するセクションがいくつか用意されています。</span><span class="sxs-lookup"><span data-stu-id="ec674-202">The document provides several sections that list specific item details, which are:</span></span>

- <span data-ttu-id="ec674-203">**SKU 番号**: リリースされた製品の品目番号を印刷します。</span><span class="sxs-lookup"><span data-stu-id="ec674-203">**SKU number**: Prints the item number of the released product.</span></span>

- <span data-ttu-id="ec674-204">**説明**: リリースされた製品の説明または名前を印刷します。</span><span class="sxs-lookup"><span data-stu-id="ec674-204">**Description**: Prints either the description or name for the released product.</span></span> <span data-ttu-id="ec674-205">ユーザーの言語の説明が存在する場合は、その説明が印刷されます。</span><span class="sxs-lookup"><span data-stu-id="ec674-205">If a description in the user's language exists, then this is printed.</span></span> <span data-ttu-id="ec674-206">そのような説明が存在しない場合は、ユーザーの言語で名前が印刷されます。</span><span class="sxs-lookup"><span data-stu-id="ec674-206">If no such description exists, then the name in the user's language is printed.</span></span> <span data-ttu-id="ec674-207">その名前が存在しない場合は、品目名が印刷されます。</span><span class="sxs-lookup"><span data-stu-id="ec674-207">If that name doesn't exist, then the item name is printed.</span></span>

- <span data-ttu-id="ec674-208">**統計品目 (HS) 関税分類**: 製品に関連付けられている統計品目関税表を印刷します。</span><span class="sxs-lookup"><span data-stu-id="ec674-208">**Harmonized System (HS) Tariff Classification**: Prints the Harmonized Tariff Schedule associated to the product.</span></span> <span data-ttu-id="ec674-209">これらの表は、**輸送管理 \> 設定 \>輸送標準 \> 統計品目関税表** に移動することによって設定できます。</span><span class="sxs-lookup"><span data-stu-id="ec674-209">You can set up these schedules by going to **Transportation Management \> Setup \> Transportation standard \> Harmonized Tariff Schedules**.</span></span>

- <span data-ttu-id="ec674-210">**原産国の基準:** このセクションでは、ドキュメントを最初にリリースするときに、データを手動で入力する必要があります。</span><span class="sxs-lookup"><span data-stu-id="ec674-210">**Origin criterion:** You must manually enter data in this section the first time you release the document.</span></span>

- <span data-ttu-id="ec674-211">**原産国:** **製品情報管理 \> セットアップ \>製品コンプライアンス \>原産国** に移動して、原産国を印刷します ([原産国](../pim/country-of-origin.md)を参照)。</span><span class="sxs-lookup"><span data-stu-id="ec674-211">**Country of origin:** Prints the country of origin, which you apply by going to **Product information management \> Setup \> Product compliance \> Country of origin** (see also [Country of origin](../pim/country-of-origin.md)).</span></span> <span data-ttu-id="ec674-212">原産国の ISO コードは、出荷先住所と品目の宛先の国/地域に基づいて印刷されます。</span><span class="sxs-lookup"><span data-stu-id="ec674-212">The ISO code for the country of origin is printed based on the country/region of destination in the shipment delivery address and the item.</span></span> <span data-ttu-id="ec674-213">原産国データが設定されていない場合は、この値によって、**リリースされた製品 \> 対外貿易 \> 原産国** で検出された設定に戻ります。</span><span class="sxs-lookup"><span data-stu-id="ec674-213">If no country of origin data has been set up, then this value reverts back to the setting found at **Released product \> Foreign trade \> Origin**.</span></span> <span data-ttu-id="ec674-214">それでも原産国データが見つからない場合は、ドキュメントを生成した後に原産国を手動で入力する必要があります。</span><span class="sxs-lookup"><span data-stu-id="ec674-214">If still no country of origin data is found, then you must manually enter the country of origin after generating the document.</span></span>

### <a name="certifier-signature-and-date"></a><span data-ttu-id="ec674-215">証明者の署名と日付</span><span class="sxs-lookup"><span data-stu-id="ec674-215">Certifier signature and date</span></span>

<span data-ttu-id="ec674-216">ドキュメントを生成した後に手動で入力する必要があります。</span><span class="sxs-lookup"><span data-stu-id="ec674-216">You must enter this manually after generating the document.</span></span>

### <a name="consists-of-number-of-pages"></a><span data-ttu-id="ec674-217">ページ数で構成されます。</span><span class="sxs-lookup"><span data-stu-id="ec674-217">Consists of number of pages</span></span>

<span data-ttu-id="ec674-218">ドキュメントを生成した後に、証明書に署名するユーザーは、検証のためにページ数を手動で入力する必要があります。</span><span class="sxs-lookup"><span data-stu-id="ec674-218">The user signing the certification must manually enter the number of pages (for verification) after generating the document.</span></span>

### <a name="page-numbers"></a><span data-ttu-id="ec674-219">ページ番号</span><span class="sxs-lookup"><span data-stu-id="ec674-219">Page numbers</span></span>

<span data-ttu-id="ec674-220">ドキュメントの下部に印刷される現在のページとページ数です。</span><span class="sxs-lookup"><span data-stu-id="ec674-220">Current page and number of pages printed at the bottom of the document.</span></span>
