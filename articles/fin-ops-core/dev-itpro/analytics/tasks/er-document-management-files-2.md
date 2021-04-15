---
title: ER ドキュメント管理ファイルを形式出力で使用する (第 2 部 - データ モデルの拡張)
description: このトピックでは、ER 出力でドキュメント管理ファイル (添付ファイル) を使用するために電子申告 (ER) 形式を構成する方法について説明します。 (第 2 部)
author: NickSelin
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: ERWorkspace, ERSolutionTable, ERDataModelDesigner, ERDataModelContentsItemCreationDialog, ERModelMappingTable, ERModelMappingDesigner, ERExpressionDesignerFormula
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 1e79dd0a6c68aa6ba7b857c31c9159c68543d93b
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/31/2021
ms.locfileid: "5754917"
---
# <a name="er-use-document-management-files-in-format-outputs-part-2---extend-data-model"></a><span data-ttu-id="e16b7-104">ER ドキュメント管理ファイルを形式出力で使用する (第 2 部 - データ モデルの拡張)</span><span class="sxs-lookup"><span data-stu-id="e16b7-104">ER Use Document Management files in format outputs (Part 2 - Extend data model)</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="e16b7-105">次の手順では、システム管理者または電子レポート開発者のロールに指定されたユーザーが、ER出力のドキュメント管理ファイル（添付）を使用するために電子レポート（ER）フォーマットをどのように環境設定しているのか説明します。</span><span class="sxs-lookup"><span data-stu-id="e16b7-105">The following steps explain how a user assigned to the System Administrator or Electronic Reporting Developer role can configure an Electronic reporting (ER) format to use Document Management files (attachments) in ER output.</span></span> <span data-ttu-id="e16b7-106">これらの手順はどのタイプの企業でも実施できます。</span><span class="sxs-lookup"><span data-stu-id="e16b7-106">These steps can be performed in any company.</span></span>

<span data-ttu-id="e16b7-107">これらの手順を完了するには、まず 「フォーマット出力のドキュメント管理ファイルを ER 使用する（パート1：データモデルを作成）」 作業ガイドに記載の手順を完了する必要があります。</span><span class="sxs-lookup"><span data-stu-id="e16b7-107">To complete these steps, you must first complete the steps in the "ER Use Document Management files in format outputs (Part 1: Prepare data model)" task guide.</span></span>

<span data-ttu-id="e16b7-108">この手順は Dynamics 365 for Operations バージョン 1611 に追加された機能です。</span><span class="sxs-lookup"><span data-stu-id="e16b7-108">This procedure is for a feature that was added in Dynamics 365 for Operations version 1611.</span></span>


## <a name="extend-data-model-to-present-the-document-management-files-in-it"></a><span data-ttu-id="e16b7-109">データモデルを拡張して、そのモデルにあるドキュメント管理ファイルを表示します。</span><span class="sxs-lookup"><span data-stu-id="e16b7-109">Extend data model to present the Document Management files in it</span></span>
1. <span data-ttu-id="e16b7-110">[組織管理] > [ワークスペース] > [電子申告] の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="e16b7-110">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
2. <span data-ttu-id="e16b7-111">[コンフィギュレーションをレポートする] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="e16b7-111">Click Reporting configurations.</span></span>
3. <span data-ttu-id="e16b7-112">ツリーで、「Customer invoice model」を選択します。</span><span class="sxs-lookup"><span data-stu-id="e16b7-112">In the tree, expand 'Customer invoice model'.</span></span>
4. <span data-ttu-id="e16b7-113">ツリーで、[Customer invoice model\Customer invoice model (custom)]を選択します。</span><span class="sxs-lookup"><span data-stu-id="e16b7-113">In the tree, select 'Customer invoice model\Customer invoice model (custom)'.</span></span>
5. <span data-ttu-id="e16b7-114">[デザイナー] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="e16b7-114">Click Designer.</span></span>
6. <span data-ttu-id="e16b7-115">ツリーで、「Customer invoice(InvoiceCustomer)」を選択します。</span><span class="sxs-lookup"><span data-stu-id="e16b7-115">In the tree, select 'Customer invoice(InvoiceCustomer)'.</span></span>
    * <span data-ttu-id="e16b7-116">このデータ モデルを拡張して、販売注文に添付されたファイルに適用させます。この販売注文は電子的処理の請求書に関連付けられています。</span><span class="sxs-lookup"><span data-stu-id="e16b7-116">We will extend this data model to expose in it any files that have been attached to a sales order that is related to an electronically processing invoice.</span></span>  
7. <span data-ttu-id="e16b7-117">[新規] をクリックすると、ドロップ ダイアログが開きます。</span><span class="sxs-lookup"><span data-stu-id="e16b7-117">Click New to open the drop dialog.</span></span>
8. <span data-ttu-id="e16b7-118">[名称] フィールドで、「添付請求書」を入力します。</span><span class="sxs-lookup"><span data-stu-id="e16b7-118">In the Name field, type 'Invoice attachments'.</span></span>
    * <span data-ttu-id="e16b7-119">添付請求書</span><span class="sxs-lookup"><span data-stu-id="e16b7-119">Invoice attachments</span></span>  
9. <span data-ttu-id="e16b7-120">[品目タイプ] フィールドで、「レコード リスト」を選択します。</span><span class="sxs-lookup"><span data-stu-id="e16b7-120">In the Item type field, select 'Record list'.</span></span>
10. <span data-ttu-id="e16b7-121">[追加] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="e16b7-121">Click Add.</span></span>
11. <span data-ttu-id="e16b7-122">[新規] をクリックすると、ドロップ ダイアログが開きます。</span><span class="sxs-lookup"><span data-stu-id="e16b7-122">Click New to open the drop dialog.</span></span>
12. <span data-ttu-id="e16b7-123">[名称] フィールドで、「ファイルコンテンツ」を入力します。</span><span class="sxs-lookup"><span data-stu-id="e16b7-123">In the Name field, type 'File content'.</span></span>
    * <span data-ttu-id="e16b7-124">ファイルの内容</span><span class="sxs-lookup"><span data-stu-id="e16b7-124">File content</span></span>  
13. <span data-ttu-id="e16b7-125">[品目タイプ] フィールドで、「コンテナー」を選択します。</span><span class="sxs-lookup"><span data-stu-id="e16b7-125">In the Item type field, select 'Container'.</span></span>
14. <span data-ttu-id="e16b7-126">[追加] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="e16b7-126">Click Add.</span></span>
15. <span data-ttu-id="e16b7-127">[新規] をクリックすると、ドロップ ダイアログが開きます。</span><span class="sxs-lookup"><span data-stu-id="e16b7-127">Click New to open the drop dialog.</span></span>
16. <span data-ttu-id="e16b7-128">[名称] フィールドで、「ファイル名」を入力します。</span><span class="sxs-lookup"><span data-stu-id="e16b7-128">In the Name field, type 'File name'.</span></span>
    * <span data-ttu-id="e16b7-129">ファイル名</span><span class="sxs-lookup"><span data-stu-id="e16b7-129">File name</span></span>  
17. <span data-ttu-id="e16b7-130">[品目タイプ] フィールドで、「String」を選択します。</span><span class="sxs-lookup"><span data-stu-id="e16b7-130">In the Item type field, select 'String'.</span></span>
18. <span data-ttu-id="e16b7-131">[追加] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="e16b7-131">Click Add.</span></span>

## <a name="map-new-data-model-elements-to-data-sources"></a><span data-ttu-id="e16b7-132">新規データ モデル・エレメントをデータ ソースにマッピングする</span><span class="sxs-lookup"><span data-stu-id="e16b7-132">Map new data model elements to data sources</span></span>
1. <span data-ttu-id="e16b7-133">[モデルからデータ ソースへのマップ] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="e16b7-133">Click Map model to datasource.</span></span>
2. <span data-ttu-id="e16b7-134">クイック フィルターを使用し、 「InvoiceCustomer」の値により「定義」フィールドでフィルターします。</span><span class="sxs-lookup"><span data-stu-id="e16b7-134">Use the Quick Filter to filter on the Definition field with a value of 'InvoiceCustomer'.</span></span>
    * <span data-ttu-id="e16b7-135">顧客への請求</span><span class="sxs-lookup"><span data-stu-id="e16b7-135">InvoiceCustomer</span></span>  
    * <span data-ttu-id="e16b7-136">新規モデルエレメントを該当するデータソースにマッピングします。</span><span class="sxs-lookup"><span data-stu-id="e16b7-136">We will map new model elements to appropriate data sources.</span></span>  
3. <span data-ttu-id="e16b7-137">[デザイナー] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="e16b7-137">Click Designer.</span></span>
4. <span data-ttu-id="e16b7-138">ツリーで、「Invoice attachments」を選択します。</span><span class="sxs-lookup"><span data-stu-id="e16b7-138">In the tree, select 'Invoice attachments'.</span></span>
5. <span data-ttu-id="e16b7-139">ツリーで、「Invoice attachments」を展開します。</span><span class="sxs-lookup"><span data-stu-id="e16b7-139">In the tree, expand 'Invoice attachments'.</span></span>
6. <span data-ttu-id="e16b7-140">ツリーで、「Invoice attachments\File name」を選択します。</span><span class="sxs-lookup"><span data-stu-id="e16b7-140">In the tree, select 'Invoice attachments\File name'.</span></span>
7. <span data-ttu-id="e16b7-141">[編集] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="e16b7-141">Click Edit.</span></span>
8. <span data-ttu-id="e16b7-142">「式」フィールドで、「CustInvoiceJour.'>Relations'.SalesTable.'>Relations'.'>Documents'.'originalFileName()」を入力します。</span><span class="sxs-lookup"><span data-stu-id="e16b7-142">In the Formula field, enter 'CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents'.'originalFileName()''.</span></span>
    * <span data-ttu-id="e16b7-143">CustInvoiceJour.'>Relations'.SalesTable.'>Relations'.'>Documents'.'originalFileName()'</span><span class="sxs-lookup"><span data-stu-id="e16b7-143">CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents'.'originalFileName()'</span></span>  
9. <span data-ttu-id="e16b7-144">[保存] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="e16b7-144">Click Save.</span></span>
10. <span data-ttu-id="e16b7-145">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="e16b7-145">Close the page.</span></span>
11. <span data-ttu-id="e16b7-146">ツリーで、「Invoice attachments\File content」を選択します。</span><span class="sxs-lookup"><span data-stu-id="e16b7-146">In the tree, select 'Invoice attachments\File content'.</span></span>
12. <span data-ttu-id="e16b7-147">[編集] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="e16b7-147">Click Edit.</span></span>
13. <span data-ttu-id="e16b7-148">「式」フィールドで、「CustInvoiceJour.'>Relations'.SalesTable.'>Relations'.'>Documents'.'getFileContentAsContainer()」を入力します。</span><span class="sxs-lookup"><span data-stu-id="e16b7-148">In the Formula field, enter 'CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents'.'getFileContentAsContainer()''.</span></span>
    * <span data-ttu-id="e16b7-149">CustInvoiceJour.'>Relations'.SalesTable.'>Relations'.'>Documents'.'getFileContentAsContainer()'</span><span class="sxs-lookup"><span data-stu-id="e16b7-149">CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents'.'getFileContentAsContainer()'</span></span>  
14. <span data-ttu-id="e16b7-150">[保存] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="e16b7-150">Click Save.</span></span>
15. <span data-ttu-id="e16b7-151">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="e16b7-151">Close the page.</span></span>
16. <span data-ttu-id="e16b7-152">ツリーで、「Invoice attachments」を選択します。</span><span class="sxs-lookup"><span data-stu-id="e16b7-152">In the tree, select 'Invoice attachments'.</span></span>
17. <span data-ttu-id="e16b7-153">[編集] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="e16b7-153">Click Edit.</span></span>
18. <span data-ttu-id="e16b7-154">「式」フィールドで、「CustInvoiceJour.'>Relations'.SalesTable.'>Relations'.'>Documents」を入力します。</span><span class="sxs-lookup"><span data-stu-id="e16b7-154">In the Formula field, enter 'CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents''.</span></span>
    * <span data-ttu-id="e16b7-155">CustInvoiceJour.'>Relations'.SalesTable.'>Relations'.'>Documents'</span><span class="sxs-lookup"><span data-stu-id="e16b7-155">CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents'</span></span>  
19. <span data-ttu-id="e16b7-156">[保存] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="e16b7-156">Click Save.</span></span>
20. <span data-ttu-id="e16b7-157">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="e16b7-157">Close the page.</span></span>
21. <span data-ttu-id="e16b7-158">[保存] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="e16b7-158">Click Save.</span></span>
22. <span data-ttu-id="e16b7-159">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="e16b7-159">Close the page.</span></span>
23. <span data-ttu-id="e16b7-160">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="e16b7-160">Close the page.</span></span>
24. <span data-ttu-id="e16b7-161">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="e16b7-161">Close the page.</span></span>
25. <span data-ttu-id="e16b7-162">[状態の変更] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="e16b7-162">Click Change status.</span></span>
26. <span data-ttu-id="e16b7-163">[完了] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="e16b7-163">Click Complete.</span></span>
27. <span data-ttu-id="e16b7-164">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="e16b7-164">Click OK.</span></span>



[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]