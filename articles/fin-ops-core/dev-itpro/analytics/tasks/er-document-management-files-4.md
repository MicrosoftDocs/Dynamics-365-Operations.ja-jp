---
title: ER 形式の出力 (パート 4 - 形式の実行) におけるドキュメント管理ファイルの使用
description: このトピックでは、ER 出力でドキュメント管理ファイルを使用するために電子申告形式を構成する方法について説明します。 (パート 4)
author: NickSelin
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: CustOpenInvoicesListPage, CustInvoiceJournal, SalesTable, ERSolutionTable
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: f7a7c9705d8b53ef13cd3faf13290f3f1b1d1c43
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/31/2021
ms.locfileid: "5749120"
---
# <a name="er-use-document-management-files-in-format-outputs-part-4---run-format"></a><span data-ttu-id="ac534-104">ER 形式の出力 (パート 4 - 形式の実行) におけるドキュメント管理ファイルの使用</span><span class="sxs-lookup"><span data-stu-id="ac534-104">ER Use Document Management files in format outputs (Part 4 - Run format)</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="ac534-105">次の手順では、システム管理者または電子レポート開発者のロールに指定されたユーザーが、ER出力のドキュメント管理ファイル（添付）を使用するために電子レポート（ER）フォーマットをどのように環境設定しているのか説明します。</span><span class="sxs-lookup"><span data-stu-id="ac534-105">The following steps explain how a user assigned to the system administrator or electronic reporting developer role can configure an Electronic reporting (ER) format to use Document Management files (attachments) in ER output.</span></span> <span data-ttu-id="ac534-106">これらのステップは DEMF 会社で実行できます。</span><span class="sxs-lookup"><span data-stu-id="ac534-106">These steps can be performed in the DEMF company.</span></span>

<span data-ttu-id="ac534-107">これらの手順を完了するには、まず「フォーマット出力でのドキュメント管理ファイルをER使用（パート3：フォーマットの作成）」に記載の手順を完了する必要があります。</span><span class="sxs-lookup"><span data-stu-id="ac534-107">To complete these steps, you must first complete the steps in the "ER Use Document Management files in format outputs (Part 3: Create format)" procedure.</span></span>

<span data-ttu-id="ac534-108">この手順は Dynamics 365 for Operations バージョン 1611 に追加された機能です。</span><span class="sxs-lookup"><span data-stu-id="ac534-108">This procedure is for a feature that was added in Dynamics 365 for Operations version 1611.</span></span>


## <a name="add-necessary-attachments-for-sales-order-of-a-single-invoice"></a><span data-ttu-id="ac534-109">単一請求書の販売注文に必要な添付ファイルを追加する</span><span class="sxs-lookup"><span data-stu-id="ac534-109">Add necessary attachments for sales order of a single invoice</span></span>
1. <span data-ttu-id="ac534-110">[売掛金勘定] > [請求書] > [未処理の顧客請求書] の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="ac534-110">Go to Accounts receivable > Invoices > Open customer invoices.</span></span>
2. <span data-ttu-id="ac534-111">クイック フィルターを使用して、レコードを見つけます。</span><span class="sxs-lookup"><span data-stu-id="ac534-111">Use the Quick Filter to find records.</span></span> <span data-ttu-id="ac534-112">たとえば、「CIV-000148」の値を含む請求書フィールドでフィルターを実行します。</span><span class="sxs-lookup"><span data-stu-id="ac534-112">For example, filter on the Invoice field with a value of 'CIV-000148'.</span></span>
    * <span data-ttu-id="ac534-113">CIV-000148</span><span class="sxs-lookup"><span data-stu-id="ac534-113">CIV-000148</span></span>  
3. <span data-ttu-id="ac534-114">クリックして選択した請求書のリンク先に移動します。</span><span class="sxs-lookup"><span data-stu-id="ac534-114">Click to follow the selected invoice's link.</span></span>
    * <span data-ttu-id="ac534-115">CIV-000148</span><span class="sxs-lookup"><span data-stu-id="ac534-115">CIV-000148</span></span>  
4. <span data-ttu-id="ac534-116">クリックして、[販売注文] フィールドのリンク先に移動します。</span><span class="sxs-lookup"><span data-stu-id="ac534-116">Click to follow the link in the Sales order field.</span></span>
    * <span data-ttu-id="ac534-117">000148</span><span class="sxs-lookup"><span data-stu-id="ac534-117">000148</span></span>  
5. <span data-ttu-id="ac534-118">明細行またはヘッダーのフィールドで、ヘッダーのオプションを選択します。</span><span class="sxs-lookup"><span data-stu-id="ac534-118">In the Lines or header field, select the option of Header.</span></span>
    * <span data-ttu-id="ac534-119">ヘッダーを選択して、これが添付の追加先であることを示します。</span><span class="sxs-lookup"><span data-stu-id="ac534-119">Select Header to indicate that this will be the target for adding attachments.</span></span>  
6. <span data-ttu-id="ac534-120">[添付] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="ac534-120">Click Attach.</span></span>
    * <span data-ttu-id="ac534-121">この販売注文の添付ファイルとしていくつかのファイルを追加します。</span><span class="sxs-lookup"><span data-stu-id="ac534-121">Add a few files as attachments for this sales order.</span></span> <span data-ttu-id="ac534-122">ドキュメント管理がサポートするドキュメント タイプのファイルを使用します (ファイル拡張子DOCX、DPF、XML、JPGなど)。</span><span class="sxs-lookup"><span data-stu-id="ac534-122">Use the files of the document types that are supported by the Document Management (with file extensions DOCX, DPF, XML, JPG, etc.).</span></span> <span data-ttu-id="ac534-123">ER電子メッセージに関連する請求書に添付され、さらに処理されるファイルを閲覧、選択します。</span><span class="sxs-lookup"><span data-stu-id="ac534-123">Browse and select files to be attached and further processed with the related invoice in the ER electronic message.</span></span>  
7. <span data-ttu-id="ac534-124">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="ac534-124">Click New.</span></span>
8. <span data-ttu-id="ac534-125">[ファイル] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="ac534-125">Click File.</span></span>
9. <span data-ttu-id="ac534-126">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="ac534-126">Click New.</span></span>
10. <span data-ttu-id="ac534-127">[ファイル] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="ac534-127">Click File.</span></span>
11. <span data-ttu-id="ac534-128">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="ac534-128">Close the page.</span></span>
12. <span data-ttu-id="ac534-129">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="ac534-129">Close the page.</span></span>
13. <span data-ttu-id="ac534-130">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="ac534-130">Close the page.</span></span>
14. <span data-ttu-id="ac534-131">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="ac534-131">Close the page.</span></span>

## <a name="run-the-designed-report-for-the-selected-invoice"></a><span data-ttu-id="ac534-132">選択した請求書についてデザインされたレポートを実行する</span><span class="sxs-lookup"><span data-stu-id="ac534-132">Run the designed report for the selected invoice</span></span>
1. <span data-ttu-id="ac534-133">[組織管理] > [電子申告] > [コンフィギュレーション] に移動します。</span><span class="sxs-lookup"><span data-stu-id="ac534-133">Go to Organization administration > Electronic reporting > Configurations.</span></span>
2. <span data-ttu-id="ac534-134">ツリーで、「Customer invoice model」を選択します。</span><span class="sxs-lookup"><span data-stu-id="ac534-134">In the tree, expand 'Customer invoice model'.</span></span>
3. <span data-ttu-id="ac534-135">ツリーで、「Customer invoice model\Customer invoice model (custom)」を展開します。</span><span class="sxs-lookup"><span data-stu-id="ac534-135">In the tree, expand 'Customer invoice model\Customer invoice model (custom)'.</span></span>
4. <span data-ttu-id="ac534-136">ツリーで、「In the tree, select 'Customer invoice model\Customer invoice model (custom)\Electronic invoice sample message」を選択します。</span><span class="sxs-lookup"><span data-stu-id="ac534-136">In the tree, select 'Customer invoice model\Customer invoice model (custom)\Electronic invoice sample message'.</span></span>
5. <span data-ttu-id="ac534-137">[実行] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="ac534-137">Click Run.</span></span>
6. <span data-ttu-id="ac534-138">() セクションを含む記録を展開します。</span><span class="sxs-lookup"><span data-stu-id="ac534-138">Expand the Records to include () section.</span></span>
7. <span data-ttu-id="ac534-139">[フィルター] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="ac534-139">Click Filter.</span></span>
8. <span data-ttu-id="ac534-140">顧客請求書仕訳および販売注文のフィールドの行を選択します。</span><span class="sxs-lookup"><span data-stu-id="ac534-140">Select the row of the Customer invoice journal and the Sales order field.</span></span>
9. <span data-ttu-id="ac534-141">[基準] フィールドで、「000148」と入力します。</span><span class="sxs-lookup"><span data-stu-id="ac534-141">In the Criteria field, type '000148'.</span></span>
    * <span data-ttu-id="ac534-142">条件 「販売注文」 フィールドで、注文番号 000148 を入力します。</span><span class="sxs-lookup"><span data-stu-id="ac534-142">In the criteria "Sales order" field, type the order number 000148.</span></span>  
10. <span data-ttu-id="ac534-143">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="ac534-143">Click OK.</span></span>
11. <span data-ttu-id="ac534-144">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="ac534-144">Click OK.</span></span>
    * <span data-ttu-id="ac534-145">生成された出荷を確認します。</span><span class="sxs-lookup"><span data-stu-id="ac534-145">Review the generated output.</span></span> <span data-ttu-id="ac534-146">各添付ファイルに対して単一のXMLノードが作成されたことに注意してください。</span><span class="sxs-lookup"><span data-stu-id="ac534-146">Note that for each attachment a single XML node has been created.</span></span> <span data-ttu-id="ac534-147">添付ファイルのコンテンツは、MIME (base64) テキスト形式で XML 出力に取り込まれます。</span><span class="sxs-lookup"><span data-stu-id="ac534-147">The attachment's content is populated to the XML output in MIME (base64) text format.</span></span>  



[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]