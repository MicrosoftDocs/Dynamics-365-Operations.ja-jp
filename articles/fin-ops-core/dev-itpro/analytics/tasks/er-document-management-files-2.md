---
title: ER ドキュメント管理ファイルを形式出力で使用する (第 2 部 - データ モデルの拡張)
description: 次の手順では、システム管理者または電子レポート開発者のロールに指定されたユーザーが、ER出力のドキュメント管理ファイル（添付）を使用するために電子レポート（ER）フォーマットをどのように環境設定しているのか説明します。
author: NickSelin
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ERWorkspace, ERSolutionTable, ERDataModelDesigner, ERDataModelContentsItemCreationDialog, ERModelMappingTable, ERModelMappingDesigner, ERExpressionDesignerFormula
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 032f9c5707294ee33cc848ecc6990c1ef5bbfdbb
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/27/2019
ms.locfileid: "2185040"
---
# <a name="er-use-document-management-files-in-format-outputs-part-2-extend-data-model"></a><span data-ttu-id="4e477-103">ER 形式の出力 (パート 2: データ モデルの拡張) におけるドキュメント管理ファイルの使用</span><span class="sxs-lookup"><span data-stu-id="4e477-103">ER Use Document Management files in format outputs (Part 2: Extend data model)</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="4e477-104">次の手順では、システム管理者または電子レポート開発者のロールに指定されたユーザーが、ER出力のドキュメント管理ファイル（添付）を使用するために電子レポート（ER）フォーマットをどのように環境設定しているのか説明します。</span><span class="sxs-lookup"><span data-stu-id="4e477-104">The following steps explain how a user assigned to the System Administrator or Electronic Reporting Developer role can configure an Electronic reporting (ER) format to use Document Management files (attachments) in ER output.</span></span> <span data-ttu-id="4e477-105">これらの手順はどのタイプの企業でも実施できます。</span><span class="sxs-lookup"><span data-stu-id="4e477-105">These steps can be performed in any company.</span></span>

<span data-ttu-id="4e477-106">これらの手順を完了するには、まず「フォーマット出力のドキュメント管理ファイルをER使用する (パート1：データモデルを作成）」の作業ガイドの手順を完了する必要があります。</span><span class="sxs-lookup"><span data-stu-id="4e477-106">To complete these steps, you must first complete the steps in the “ER Use Document Management files in format outputs (Part 1: Prepare data model)” task guide.</span></span>

<span data-ttu-id="4e477-107">この手順は Dynamics 365 for Operations バージョン 1611 に追加された機能です。</span><span class="sxs-lookup"><span data-stu-id="4e477-107">This procedure is for a feature that was added in Dynamics 365 for Operations version 1611.</span></span>


## <a name="extend-data-model-to-present-the-document-management-files-in-it"></a><span data-ttu-id="4e477-108">データモデルを拡張して、そのモデルにあるドキュメント管理ファイルを表示します。</span><span class="sxs-lookup"><span data-stu-id="4e477-108">Extend data model to present the Document Management files in it</span></span>
1. <span data-ttu-id="4e477-109">[組織管理] > [ワークスペース] > [電子申告] の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="4e477-109">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
2. <span data-ttu-id="4e477-110">[コンフィギュレーションをレポートする] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="4e477-110">Click Reporting configurations.</span></span>
3. <span data-ttu-id="4e477-111">ツリーで、「Customer invoice model」を選択します。</span><span class="sxs-lookup"><span data-stu-id="4e477-111">In the tree, expand 'Customer invoice model'.</span></span>
4. <span data-ttu-id="4e477-112">ツリーで、「Customer invoice model\Customer invoice model (custom)]を選択します。</span><span class="sxs-lookup"><span data-stu-id="4e477-112">In the tree, select 'Customer invoice model\Customer invoice model (custom)'.</span></span>
5. <span data-ttu-id="4e477-113">[デザイナー] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="4e477-113">Click Designer.</span></span>
6. <span data-ttu-id="4e477-114">ツリーで、「Customer invoice(InvoiceCustomer)」を選択します。</span><span class="sxs-lookup"><span data-stu-id="4e477-114">In the tree, select 'Customer invoice(InvoiceCustomer)'.</span></span>
    * <span data-ttu-id="4e477-115">このデータ モデルを拡張して、販売注文に添付されたファイルに適用させます。この販売注文は電子的処理の請求書に関連付けられています。</span><span class="sxs-lookup"><span data-stu-id="4e477-115">We will extend this data model to expose in it any files that have been attached to a sales order that is related to an electronically processing invoice.</span></span>  
7. <span data-ttu-id="4e477-116">[新規] をクリックすると、ドロップ ダイアログが開きます。</span><span class="sxs-lookup"><span data-stu-id="4e477-116">Click New to open the drop dialog.</span></span>
8. <span data-ttu-id="4e477-117">[名称] フィールドで、「添付請求書」を入力します。</span><span class="sxs-lookup"><span data-stu-id="4e477-117">In the Name field, type 'Invoice attachments'.</span></span>
    * <span data-ttu-id="4e477-118">添付請求書</span><span class="sxs-lookup"><span data-stu-id="4e477-118">Invoice attachments</span></span>  
9. <span data-ttu-id="4e477-119">[品目タイプ] フィールドで、「レコード リスト」を選択します。</span><span class="sxs-lookup"><span data-stu-id="4e477-119">In the Item type field, select 'Record list'.</span></span>
10. <span data-ttu-id="4e477-120">[追加] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="4e477-120">Click Add.</span></span>
11. <span data-ttu-id="4e477-121">[新規] をクリックすると、ドロップ ダイアログが開きます。</span><span class="sxs-lookup"><span data-stu-id="4e477-121">Click New to open the drop dialog.</span></span>
12. <span data-ttu-id="4e477-122">[名称] フィールドで、「ファイルコンテンツ」を入力します。</span><span class="sxs-lookup"><span data-stu-id="4e477-122">In the Name field, type 'File content'.</span></span>
    * <span data-ttu-id="4e477-123">ファイルの内容</span><span class="sxs-lookup"><span data-stu-id="4e477-123">File content</span></span>  
13. <span data-ttu-id="4e477-124">[品目タイプ] フィールドで、「コンテナー」を選択します。</span><span class="sxs-lookup"><span data-stu-id="4e477-124">In the Item type field, select 'Container'.</span></span>
14. <span data-ttu-id="4e477-125">[追加] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="4e477-125">Click Add.</span></span>
15. <span data-ttu-id="4e477-126">[新規] をクリックすると、ドロップ ダイアログが開きます。</span><span class="sxs-lookup"><span data-stu-id="4e477-126">Click New to open the drop dialog.</span></span>
16. <span data-ttu-id="4e477-127">[名称] フィールドで、「ファイル名」を入力します。</span><span class="sxs-lookup"><span data-stu-id="4e477-127">In the Name field, type 'File name'.</span></span>
    * <span data-ttu-id="4e477-128">ファイル名</span><span class="sxs-lookup"><span data-stu-id="4e477-128">File name</span></span>  
17. <span data-ttu-id="4e477-129">[品目タイプ] フィールドで、「String」を選択します。</span><span class="sxs-lookup"><span data-stu-id="4e477-129">In the Item type field, select 'String'.</span></span>
18. <span data-ttu-id="4e477-130">[追加] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="4e477-130">Click Add.</span></span>

## <a name="map-new-data-model-elements-to-data-sources"></a><span data-ttu-id="4e477-131">新規データ モデル・エレメントをデータ ソースにマッピングする</span><span class="sxs-lookup"><span data-stu-id="4e477-131">Map new data model elements to data sources</span></span>
1. <span data-ttu-id="4e477-132">[モデルからデータ ソースへのマップ] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="4e477-132">Click Map model to datasource.</span></span>
2. <span data-ttu-id="4e477-133">クイック フィルターを使用し、 「InvoiceCustomer」の値により「定義」フィールドでフィルターします。</span><span class="sxs-lookup"><span data-stu-id="4e477-133">Use the Quick Filter to filter on the Definition field with a value of 'InvoiceCustomer'.</span></span>
    * <span data-ttu-id="4e477-134">顧客への請求</span><span class="sxs-lookup"><span data-stu-id="4e477-134">InvoiceCustomer</span></span>  
    * <span data-ttu-id="4e477-135">新規モデルエレメントを該当するデータソースにマッピングします。</span><span class="sxs-lookup"><span data-stu-id="4e477-135">We will map new model elements to appropriate data sources.</span></span>  
3. <span data-ttu-id="4e477-136">[デザイナー] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="4e477-136">Click Designer.</span></span>
4. <span data-ttu-id="4e477-137">ツリーで、「Invoice attachments」を選択します。</span><span class="sxs-lookup"><span data-stu-id="4e477-137">In the tree, select 'Invoice attachments'.</span></span>
5. <span data-ttu-id="4e477-138">ツリーで、「Invoice attachments」を展開します。</span><span class="sxs-lookup"><span data-stu-id="4e477-138">In the tree, expand 'Invoice attachments'.</span></span>
6. <span data-ttu-id="4e477-139">ツリーで、「Invoice attachments\File name」を選択します。</span><span class="sxs-lookup"><span data-stu-id="4e477-139">In the tree, select 'Invoice attachments\File name'.</span></span>
7. <span data-ttu-id="4e477-140">[編集] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="4e477-140">Click Edit.</span></span>
8. <span data-ttu-id="4e477-141">「式」フィールドで、「CustInvoiceJour.'>Relations'.SalesTable.'>Relations'.'>Documents'.'originalFileName()」を入力します。</span><span class="sxs-lookup"><span data-stu-id="4e477-141">In the Formula field, enter 'CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents'.'originalFileName()''.</span></span>
    * <span data-ttu-id="4e477-142">CustInvoiceJour.'>Relations'.SalesTable.'>Relations'.'>Documents'.'originalFileName()'</span><span class="sxs-lookup"><span data-stu-id="4e477-142">CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents'.'originalFileName()'</span></span>  
9. <span data-ttu-id="4e477-143">[保存] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="4e477-143">Click Save.</span></span>
10. <span data-ttu-id="4e477-144">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="4e477-144">Close the page.</span></span>
11. <span data-ttu-id="4e477-145">ツリーで、「Invoice attachments\File content」を選択します。</span><span class="sxs-lookup"><span data-stu-id="4e477-145">In the tree, select 'Invoice attachments\File content'.</span></span>
12. <span data-ttu-id="4e477-146">[編集] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="4e477-146">Click Edit.</span></span>
13. <span data-ttu-id="4e477-147">「式」フィールドで、「CustInvoiceJour.'>Relations'.SalesTable.'>Relations'.'>Documents'.'getFileContentAsContainer()」を入力します。</span><span class="sxs-lookup"><span data-stu-id="4e477-147">In the Formula field, enter 'CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents'.'getFileContentAsContainer()''.</span></span>
    * <span data-ttu-id="4e477-148">CustInvoiceJour.'>Relations'.SalesTable.'>Relations'.'>Documents'.'getFileContentAsContainer()'</span><span class="sxs-lookup"><span data-stu-id="4e477-148">CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents'.'getFileContentAsContainer()'</span></span>  
14. <span data-ttu-id="4e477-149">[保存] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="4e477-149">Click Save.</span></span>
15. <span data-ttu-id="4e477-150">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="4e477-150">Close the page.</span></span>
16. <span data-ttu-id="4e477-151">ツリーで、「Invoice attachments」を選択します。</span><span class="sxs-lookup"><span data-stu-id="4e477-151">In the tree, select 'Invoice attachments'.</span></span>
17. <span data-ttu-id="4e477-152">[編集] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="4e477-152">Click Edit.</span></span>
18. <span data-ttu-id="4e477-153">「式」フィールドで、「CustInvoiceJour.'>Relations'.SalesTable.'>Relations'.'>Documents」を入力します。</span><span class="sxs-lookup"><span data-stu-id="4e477-153">In the Formula field, enter 'CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents''.</span></span>
    * <span data-ttu-id="4e477-154">CustInvoiceJour.'>Relations'.SalesTable.'>Relations'.'>Documents'</span><span class="sxs-lookup"><span data-stu-id="4e477-154">CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents'</span></span>  
19. <span data-ttu-id="4e477-155">[保存] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="4e477-155">Click Save.</span></span>
20. <span data-ttu-id="4e477-156">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="4e477-156">Close the page.</span></span>
21. <span data-ttu-id="4e477-157">[保存] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="4e477-157">Click Save.</span></span>
22. <span data-ttu-id="4e477-158">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="4e477-158">Close the page.</span></span>
23. <span data-ttu-id="4e477-159">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="4e477-159">Close the page.</span></span>
24. <span data-ttu-id="4e477-160">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="4e477-160">Close the page.</span></span>
25. <span data-ttu-id="4e477-161">[状態の変更] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="4e477-161">Click Change status.</span></span>
26. <span data-ttu-id="4e477-162">[完了] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="4e477-162">Click Complete.</span></span>
27. <span data-ttu-id="4e477-163">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="4e477-163">Click OK.</span></span>
