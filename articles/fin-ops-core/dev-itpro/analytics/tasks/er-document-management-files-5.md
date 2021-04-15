---
title: ER ドキュメント管理ファイルを形式出力で使用する (第 5 部 - 形式の変更および実行)
description: このトピックでは、ER 出力でドキュメント管理ファイル (添付ファイル) を使用するために電子申告 (ER) 形式を構成する方法について説明します。 (第 5 部)
author: NickSelin
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: ERSolutionTable, EROperationDesigner, ERComponentTypeDropDialog, ERExpressionDesignerFormula, SysQueryForm
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: f954b76a09bf7c5edd4c608d400318fbd9386778
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/31/2021
ms.locfileid: "5749096"
---
# <a name="er-use-document-management-files-in-format-outputs-part-5---modify-and-run-format"></a><span data-ttu-id="113de-104">ER ドキュメント管理ファイルを形式出力で使用する (第 5 部 - 形式の変更および実行)</span><span class="sxs-lookup"><span data-stu-id="113de-104">ER Use Document Management files in format outputs (Part 5 - Modify and run format)</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="113de-105">次の手順では、システム管理者または電子レポート開発者のロールに指定されたユーザーが、ER出力のドキュメント管理ファイル（添付）を使用するために電子レポート（ER）フォーマットをどのように環境設定しているのか説明します。</span><span class="sxs-lookup"><span data-stu-id="113de-105">The following steps explain how a user assigned to the system administrator or electronic reporting developer role can configure an Electronic reporting (ER) format to use Document Management files (attachments) in ER output.</span></span> <span data-ttu-id="113de-106">これらのステップは DEMF 会社で実行できます。</span><span class="sxs-lookup"><span data-stu-id="113de-106">These steps can be performed in the DEMF company.</span></span>

<span data-ttu-id="113de-107">これらの手順を完了するには、まず 「ER ドキュメント管理ファイルをフォーマット出力で使用する（パート 4：フォーマットを実行する）」に記載の手順を実行する必要があります。</span><span class="sxs-lookup"><span data-stu-id="113de-107">To complete these steps, you must first complete the steps in the "ER Use Document Management files in format outputs (Part 4: Run format)" procedure.</span></span>

<span data-ttu-id="113de-108">この手順は Dynamics 365 for Operations バージョン 1611 に追加された機能です。</span><span class="sxs-lookup"><span data-stu-id="113de-108">This procedure is for a feature that was added in Dynamics 365 for Operations version 1611.</span></span>


## <a name="modify-the-format-to-populate-attachments-into-generating-messages-in-binary-format"></a><span data-ttu-id="113de-109">バイナリ形式のメッセージの生成に添付ファイルを設定するフォーマットを変更します。</span><span class="sxs-lookup"><span data-stu-id="113de-109">Modify the format to populate attachments into generating messages in binary format</span></span>
1. <span data-ttu-id="113de-110">[組織管理] > [電子申告] > [コンフィギュレーション] に移動します。</span><span class="sxs-lookup"><span data-stu-id="113de-110">Go to Organization administration > Electronic reporting > Configurations.</span></span>
2. <span data-ttu-id="113de-111">ツリーで、「Customer invoice model」を選択します。</span><span class="sxs-lookup"><span data-stu-id="113de-111">In the tree, expand 'Customer invoice model'.</span></span>
3. <span data-ttu-id="113de-112">ツリーで、「Customer invoice model\Customer invoice model (custom)」を展開します。</span><span class="sxs-lookup"><span data-stu-id="113de-112">In the tree, expand 'Customer invoice model\Customer invoice model (custom)'.</span></span>
4. <span data-ttu-id="113de-113">ツリーで、「In the tree, select 'Customer invoice model\Customer invoice model (custom)\Electronic invoice sample message」を選択します。</span><span class="sxs-lookup"><span data-stu-id="113de-113">In the tree, select 'Customer invoice model\Customer invoice model (custom)\Electronic invoice sample message'.</span></span>
5. <span data-ttu-id="113de-114">[デザイナー] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="113de-114">Click Designer.</span></span>
    * <span data-ttu-id="113de-115">UNICODEエンコードを使用し、XMLファイルとして生成される出力の請求書メッセージを設定します。</span><span class="sxs-lookup"><span data-stu-id="113de-115">You will populate the invoice message in the generating output as an XML file using UNICODE encoding.</span></span>  
6. <span data-ttu-id="113de-116">[ルートの追加] をクリックして、ドロップ ダイアログを開きます。</span><span class="sxs-lookup"><span data-stu-id="113de-116">Click Add root to open the drop dialog.</span></span>
7. <span data-ttu-id="113de-117">ツリーで、[Common\File] を選択します。</span><span class="sxs-lookup"><span data-stu-id="113de-117">In the tree, select 'Common\File'.</span></span>
8. <span data-ttu-id="113de-118">[名称] フィールドに、「Xmlメッセージ」と入力します。</span><span class="sxs-lookup"><span data-stu-id="113de-118">In the Name field, type 'Xml message'.</span></span>
    * <span data-ttu-id="113de-119">Xml メッセージ</span><span class="sxs-lookup"><span data-stu-id="113de-119">Xml message</span></span>  
9. <span data-ttu-id="113de-120">[エンコード] フィールドに、「UTF-8」と入力します。</span><span class="sxs-lookup"><span data-stu-id="113de-120">In the Encoding field, type 'UTF-8'.</span></span>
    * <span data-ttu-id="113de-121">UTF-8</span><span class="sxs-lookup"><span data-stu-id="113de-121">UTF-8</span></span>  
10. <span data-ttu-id="113de-122">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="113de-122">Click OK.</span></span>
    * <span data-ttu-id="113de-123">ZIPファイルとして生成される出力を設定します。</span><span class="sxs-lookup"><span data-stu-id="113de-123">Configure the generating output as a zipped file.</span></span>  
11. <span data-ttu-id="113de-124">[ルートの追加] をクリックして、ドロップ ダイアログを開きます。</span><span class="sxs-lookup"><span data-stu-id="113de-124">Click Add root to open the drop dialog.</span></span>
12. <span data-ttu-id="113de-125">ツリーで、「Common\Folder」を選択します。</span><span class="sxs-lookup"><span data-stu-id="113de-125">In the tree, select 'Common\Folder'.</span></span>
13. <span data-ttu-id="113de-126">[名称] フィールドに、「Zip出力」と入力します。</span><span class="sxs-lookup"><span data-stu-id="113de-126">In the Name field, type 'Zip output'.</span></span>
    * <span data-ttu-id="113de-127">Zip 出力</span><span class="sxs-lookup"><span data-stu-id="113de-127">Zip output</span></span>  
14. <span data-ttu-id="113de-128">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="113de-128">Click OK.</span></span>
15. <span data-ttu-id="113de-129">ツリーで、「Zip output」を選択します。</span><span class="sxs-lookup"><span data-stu-id="113de-129">In the tree, select 'Zip output'.</span></span>
    * <span data-ttu-id="113de-130">元名称と拡張子を含むファイルとして生成されるZIPファイルに添付ファイルを追加します。</span><span class="sxs-lookup"><span data-stu-id="113de-130">Add attachments to the generating zipped file as files with original names and extensions.</span></span>  
16. <span data-ttu-id="113de-131">[追加] をクリックしてドロップ ダイアログを開きます。</span><span class="sxs-lookup"><span data-stu-id="113de-131">Click Add to open the drop dialog.</span></span>
17. <span data-ttu-id="113de-132">ツリーで、[Common\File] を選択します。</span><span class="sxs-lookup"><span data-stu-id="113de-132">In the tree, select 'Common\File'.</span></span>
18. <span data-ttu-id="113de-133">[名称] フィールドで、「添付ファイル」を入力します。</span><span class="sxs-lookup"><span data-stu-id="113de-133">In the Name field, type 'Attached file'.</span></span>
    * <span data-ttu-id="113de-134">添付ファイル</span><span class="sxs-lookup"><span data-stu-id="113de-134">Attached file</span></span>  
19. <span data-ttu-id="113de-135">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="113de-135">Click OK.</span></span>
20. <span data-ttu-id="113de-136">ツリーで、「Zip output\Attached file」を選択します。</span><span class="sxs-lookup"><span data-stu-id="113de-136">In the tree, select 'Zip output\Attached file'.</span></span>
21. <span data-ttu-id="113de-137">[追加] をクリックしてドロップ ダイアログを開きます。</span><span class="sxs-lookup"><span data-stu-id="113de-137">Click Add to open the drop dialog.</span></span>
22. <span data-ttu-id="113de-138">ツリーで、「'Text\Base64」を選択します。</span><span class="sxs-lookup"><span data-stu-id="113de-138">In the tree, select 'Text\Base64'.</span></span>
23. <span data-ttu-id="113de-139">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="113de-139">Click OK.</span></span>

## <a name="map-new-format-elements-to-data-model"></a><span data-ttu-id="113de-140">新規フォーマットエレメントをデータ モデルにマッピングする</span><span class="sxs-lookup"><span data-stu-id="113de-140">Map new format elements to data model</span></span>
1. <span data-ttu-id="113de-141">[マッピング] タブをクリックします。</span><span class="sxs-lookup"><span data-stu-id="113de-141">Click the Mapping tab.</span></span>
2. <span data-ttu-id="113de-142">ツリーで、「model」を展開します。</span><span class="sxs-lookup"><span data-stu-id="113de-142">In the tree, expand 'model'.</span></span>
3. <span data-ttu-id="113de-143">ツリーで、「model\Invoice attachments」を展開します。</span><span class="sxs-lookup"><span data-stu-id="113de-143">In the tree, expand 'model\Invoice attachments'.</span></span>
4. <span data-ttu-id="113de-144">ツリーで、「Zip output\Attached file\Base64を選択します。</span><span class="sxs-lookup"><span data-stu-id="113de-144">In the tree, select 'Zip output\Attached file\Base64'.</span></span>
5. <span data-ttu-id="113de-145">ツリーで、「model\Invoice attachments\File content」を選択します。</span><span class="sxs-lookup"><span data-stu-id="113de-145">In the tree, select 'model\Invoice attachments\File content'.</span></span>
6. <span data-ttu-id="113de-146">[バインド] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="113de-146">Click Bind.</span></span>
7. <span data-ttu-id="113de-147">ツリーで、「Zip output\Attached file」を選択します。</span><span class="sxs-lookup"><span data-stu-id="113de-147">In the tree, select 'Zip output\Attached file'.</span></span>
8. <span data-ttu-id="113de-148">[ファイル名の編集] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="113de-148">Click Edit filename.</span></span>
9. <span data-ttu-id="113de-149">ツリーで、[model] を展開します。</span><span class="sxs-lookup"><span data-stu-id="113de-149">In the tree, expand 'model'.</span></span>
10. <span data-ttu-id="113de-150">ツリーで、「model\Invoice attachments」を展開します。</span><span class="sxs-lookup"><span data-stu-id="113de-150">In the tree, expand 'model\Invoice attachments'.</span></span>
11. <span data-ttu-id="113de-151">ツリーで、「model\Invoice attachments\File name」を選択します。</span><span class="sxs-lookup"><span data-stu-id="113de-151">In the tree, select 'model\Invoice attachments\File name'.</span></span>
12. <span data-ttu-id="113de-152">[データ ソースの追加] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="113de-152">Click Add data source.</span></span>
13. <span data-ttu-id="113de-153">[保存] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="113de-153">Click Save.</span></span>
14. <span data-ttu-id="113de-154">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="113de-154">Close the page.</span></span>
15. <span data-ttu-id="113de-155">ツリーで、「model\Invoice attachments」を選択します。</span><span class="sxs-lookup"><span data-stu-id="113de-155">In the tree, select 'model\Invoice attachments'.</span></span>
16. <span data-ttu-id="113de-156">[バインド] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="113de-156">Click Bind.</span></span>
17. <span data-ttu-id="113de-157">[保存] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="113de-157">Click Save.</span></span>
18. <span data-ttu-id="113de-158">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="113de-158">Close the page.</span></span>

## <a name="run-the-designed-report-for-the-selected-invoice"></a><span data-ttu-id="113de-159">選択した請求書についてデザインされたレポートを実行する</span><span class="sxs-lookup"><span data-stu-id="113de-159">Run the designed report for the selected invoice</span></span>
1. <span data-ttu-id="113de-160">[実行] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="113de-160">Click Run.</span></span>
2. <span data-ttu-id="113de-161">() セクションを含む記録を展開します。</span><span class="sxs-lookup"><span data-stu-id="113de-161">Expand the Records to include () section.</span></span>
3. <span data-ttu-id="113de-162">[フィルター] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="113de-162">Click Filter.</span></span>
4. <span data-ttu-id="113de-163">顧客請求書仕訳および販売注文のフィールドの行を選択します。</span><span class="sxs-lookup"><span data-stu-id="113de-163">Select the row of the Customer invoice journal and the Sales order field.</span></span>
5. <span data-ttu-id="113de-164">条件 [販売注文]フィールドでの条件フィールドにて、注文番号 000148 を入力します。</span><span class="sxs-lookup"><span data-stu-id="113de-164">In the Criteria field, In the criteria "Sales order" field, type the order number 000148.</span></span>
    * <span data-ttu-id="113de-165">000148</span><span class="sxs-lookup"><span data-stu-id="113de-165">000148</span></span>  
6. <span data-ttu-id="113de-166">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="113de-166">Click OK.</span></span>
7. <span data-ttu-id="113de-167">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="113de-167">Click OK.</span></span>
    * <span data-ttu-id="113de-168">生成された出荷を確認します。</span><span class="sxs-lookup"><span data-stu-id="113de-168">Review the generated output.</span></span> <span data-ttu-id="113de-169">XML形式の請求書メッセージに加えて、各添付ファイルに対して単一ファイルが作成されたことに注意していください。</span><span class="sxs-lookup"><span data-stu-id="113de-169">Note,that in addition to the invoice message in XML format, a single file has been created for each attachment.</span></span> <span data-ttu-id="113de-170">添付ファイルは、バイナリ形式のZIP出力で設定されます。</span><span class="sxs-lookup"><span data-stu-id="113de-170">The attachment files are populated with the zipped output in binary format.</span></span>  



[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]