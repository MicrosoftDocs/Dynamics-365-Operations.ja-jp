--- 
title: "電子申告 (ER) 用に埋め込み画像付きで Microsoft Office 形式のレポートを作成するためにコンフィギュレーションを確認する"
description: "これらのステップを完了するには、まず、「ER 埋め込み画像付きで MS Office 形式のレポートを作成する (パート 1 - パラメータの設定)」タスク ガイドにあるステップを完了する必要があります。"
author: NickSelin
manager: AnnBe
ms.date: 06/13/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: kfend
ms.search.scope: Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: 19757b1b8f932113361b6e5d210a66f149a212f6
ms.contentlocale: ja-jp
ms.lasthandoff: 08/29/2017

---
# <a name="review-configurations-to-make-reports-in-microsoft-office-formats-with-embedded-images-for-electronic-reporting-er"></a><span data-ttu-id="0a55a-103">電子申告 (ER) 用に埋め込み画像付きで Microsoft Office 形式のレポートを作成するためにコンフィギュレーションを確認する</span><span class="sxs-lookup"><span data-stu-id="0a55a-103">Review configurations to make reports in Microsoft Office formats with embedded images for electronic reporting (ER)</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="0a55a-104">これらのステップを完了するには、まず、「ER 埋め込み画像付きで MS Office 形式のレポートを作成する (パート 1: パラメータの設定)」タスク ガイドにあるステップを完了する必要があります。</span><span class="sxs-lookup"><span data-stu-id="0a55a-104">To complete these steps, you must first complete the steps in the “ER Make reports in MS Office formats with embedded images (Part 1: Set up parameters)” task guide.</span></span>

<span data-ttu-id="0a55a-105">この手順では、電子レポート (ER) コンフィギュレーションを設計して、Microsoft Excel と Microsoft Word の埋め込み画像を含む電子ドキュメントを生成する方法を示します。</span><span class="sxs-lookup"><span data-stu-id="0a55a-105">This procedure shows how to design Electronic reporting (ER) configurations to generate electronic documents that contain embedded images in Microsoft Excel and Microsoft Word.</span></span> <span data-ttu-id="0a55a-106">この例では、サンプル会社 Litware, Inc. 用に作成した ER コンフィギュレーションを確認します。</span><span class="sxs-lookup"><span data-stu-id="0a55a-106">In this example, you will review ER configurations for the sample company Litware, Inc.</span></span> 

<span data-ttu-id="0a55a-107">この手順は、「システム管理者」または「電子レポート開発者」ロールが割り当てられているユーザーを対象としています。</span><span class="sxs-lookup"><span data-stu-id="0a55a-107">This procedure is intended for users who have the System administrator or Electronic reporting developer role assigned to them.</span></span> <span data-ttu-id="0a55a-108">ステップは、USMF データ セットを使用して完了することができます。</span><span class="sxs-lookup"><span data-stu-id="0a55a-108">The steps can be completed by using the USMF data set.</span></span>


## <a name="review-the-imported-data-model"></a><span data-ttu-id="0a55a-109">インポートされたデータ モデルを確認する</span><span class="sxs-lookup"><span data-stu-id="0a55a-109">Review the imported data model</span></span>
1. <span data-ttu-id="0a55a-110">[組織管理] > [電子申告] > [コンフィギュレーション] に移動します。</span><span class="sxs-lookup"><span data-stu-id="0a55a-110">Go to Organization administration > Electronic reporting > Configurations.</span></span>
2. <span data-ttu-id="0a55a-111">ツリーで、「小切手のモデル」を選択します。</span><span class="sxs-lookup"><span data-stu-id="0a55a-111">In the tree, select 'Model for cheques'.</span></span>
3. <span data-ttu-id="0a55a-112">[デザイナー] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="0a55a-112">Click Designer.</span></span>
    * <span data-ttu-id="0a55a-113">このモデルは、ビジネスの観点とアプリケーションのデータ ソースへのこのモデルのマッピングから支払小切手を表すように設計されています。</span><span class="sxs-lookup"><span data-stu-id="0a55a-113">This model is designed to represent payment cheques from the business standpoint and the mapping of this model to the application’s data sources.</span></span> <span data-ttu-id="0a55a-114">ER Operations によりこのモデルを確認します。</span><span class="sxs-lookup"><span data-stu-id="0a55a-114">Review this model by the ER Operations designer.</span></span> <span data-ttu-id="0a55a-115">表示されるモデル要素の属性に注意してください: 構造、名前、説明、データ型など。</span><span class="sxs-lookup"><span data-stu-id="0a55a-115">Note the attributes of the model elements that are presented: structure, name, description, data type, and so on.</span></span>   
4. <span data-ttu-id="0a55a-116">ツリーで、「ルート」を展開します。</span><span class="sxs-lookup"><span data-stu-id="0a55a-116">In the tree, expand 'root'.</span></span>
5. <span data-ttu-id="0a55a-117">ツリーで、「ルート\小切手」を選択します。</span><span class="sxs-lookup"><span data-stu-id="0a55a-117">In the tree, select 'root\cheques'.</span></span>
6. <span data-ttu-id="0a55a-118">ツリーで、「ルート\小切手」を展開します。</span><span class="sxs-lookup"><span data-stu-id="0a55a-118">In the tree, expand 'root\cheques'.</span></span>
7. <span data-ttu-id="0a55a-119">ツリーで、「ルート\小切手\属性」を展開します。</span><span class="sxs-lookup"><span data-stu-id="0a55a-119">In the tree, expand 'root\cheques\attributes'.</span></span>
8. <span data-ttu-id="0a55a-120">ツリーで、「ルート\支払人」を展開します。</span><span class="sxs-lookup"><span data-stu-id="0a55a-120">In the tree, expand 'root\payer'.</span></span>
9. <span data-ttu-id="0a55a-121">ツリーで、「ルート\istestrun」を選択します。</span><span class="sxs-lookup"><span data-stu-id="0a55a-121">In the tree, select 'root\istestrun'.</span></span>
10. <span data-ttu-id="0a55a-122">ツリーで、「ルート\レイアウト」を選択します。</span><span class="sxs-lookup"><span data-stu-id="0a55a-122">In the tree, select 'root\layout'.</span></span>
    * <span data-ttu-id="0a55a-123">このモデルのレイアウト要素は、選択した銀行口座の小切手フォーム レイアウトの印刷の詳細を表します。</span><span class="sxs-lookup"><span data-stu-id="0a55a-123">The layout element of this model represents the details of the printing cheque form layout for the selected bank account.</span></span> <span data-ttu-id="0a55a-124">画像を保存するコンテナー データ タイプの 2 つのノードも含まれます。</span><span class="sxs-lookup"><span data-stu-id="0a55a-124">It also includes two nodes of the Container data type to store images.</span></span>   
11. <span data-ttu-id="0a55a-125">ツリーで、「ルート\レイアウト」を展開します。</span><span class="sxs-lookup"><span data-stu-id="0a55a-125">In the tree, expand 'root\layout'.</span></span>
12. <span data-ttu-id="0a55a-126">ツリーで、「ルート\レイアウト\会社のロゴ」を選択します。</span><span class="sxs-lookup"><span data-stu-id="0a55a-126">In the tree, select 'root\layout\company logo'.</span></span>
13. <span data-ttu-id="0a55a-127">ツリーで、「ルート\レイアウト\会社のロゴ」を展開します。</span><span class="sxs-lookup"><span data-stu-id="0a55a-127">In the tree, expand 'root\layout\company logo'.</span></span>
14. <span data-ttu-id="0a55a-128">ツリーで、「ルート\レイアウト\会社のロゴ\画像」を選択します。</span><span class="sxs-lookup"><span data-stu-id="0a55a-128">In the tree, select 'root\layout\company logo\image'.</span></span>
15. <span data-ttu-id="0a55a-129">ツリーで、「ルート\レイアウト\会社のロゴ\isprinted」を選択します。</span><span class="sxs-lookup"><span data-stu-id="0a55a-129">In the tree, select 'root\layout\company logo\isprinted'.</span></span>
16. <span data-ttu-id="0a55a-130">ツリーで、「ルート\レイアウト\署名」を選択します。</span><span class="sxs-lookup"><span data-stu-id="0a55a-130">In the tree, select 'root\layout\signature'.</span></span>
17. <span data-ttu-id="0a55a-131">ツリーで、「ルート\レイアウト\署名」を展開します。</span><span class="sxs-lookup"><span data-stu-id="0a55a-131">In the tree, expand 'root\layout\signature'.</span></span>
18. <span data-ttu-id="0a55a-132">ツリーで、「ルート\レイアウト\署名\画像」を選択します。</span><span class="sxs-lookup"><span data-stu-id="0a55a-132">In the tree, select 'root\layout\signature\image'.</span></span>
19. <span data-ttu-id="0a55a-133">ツリーで、「ルート\レイアウト\署名\isprinted」を選択します。</span><span class="sxs-lookup"><span data-stu-id="0a55a-133">In the tree, select 'root\layout\signature\isprinted'.</span></span>
    * <span data-ttu-id="0a55a-134">2 つの画像データ モデル要素が、会社のロゴおよびバイナリ形式の権限者の署名の画像を含んでいるテーブルのフィールドにバインドされていることに注意してください。</span><span class="sxs-lookup"><span data-stu-id="0a55a-134">Note that two image data model elements are bound to the fields of the tables that contain images of the company logo and the authorized person’s signature in binary format.</span></span>  
20. <span data-ttu-id="0a55a-135">ツリーで、「ルート\レイアウト\透かし」を展開します。</span><span class="sxs-lookup"><span data-stu-id="0a55a-135">In the tree, expand 'root\layout\watermark'.</span></span>
21. <span data-ttu-id="0a55a-136">[モデルからデータ ソースへのマップ] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="0a55a-136">Click Map model to datasource.</span></span>
22. <span data-ttu-id="0a55a-137">[デザイナー] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="0a55a-137">Click Designer.</span></span>
23. <span data-ttu-id="0a55a-138">ツリーで、「chequesselected」を展開します。</span><span class="sxs-lookup"><span data-stu-id="0a55a-138">In the tree, expand 'chequesselected'.</span></span>
24. <span data-ttu-id="0a55a-139">ツリーで、「レイアウト」を展開します。</span><span class="sxs-lookup"><span data-stu-id="0a55a-139">In the tree, expand 'layout'.</span></span>
25. <span data-ttu-id="0a55a-140">ツリーで、「レイアウト\会社のロゴ」を展開します。</span><span class="sxs-lookup"><span data-stu-id="0a55a-140">In the tree, expand 'layout\company logo'.</span></span>
26. <span data-ttu-id="0a55a-141">ツリーで、「レイアウト\署名」を展開します。</span><span class="sxs-lookup"><span data-stu-id="0a55a-141">In the tree, expand 'layout\signature'.</span></span>
27. <span data-ttu-id="0a55a-142">ツリーで、「レイアウト\透かし」を展開します。</span><span class="sxs-lookup"><span data-stu-id="0a55a-142">In the tree, expand 'layout\watermark'.</span></span>
28. <span data-ttu-id="0a55a-143">[詳細の表示] をオンに切り替えます。</span><span class="sxs-lookup"><span data-stu-id="0a55a-143">Toggle 'Show details' on.</span></span>
    * <span data-ttu-id="0a55a-144">小切手のデータ モデル要素が、ユーザーが印刷対象に選択した小切手のレコードを実行時に含める TmpChequePrintout テーブルにバインドされていることに注意してください。</span><span class="sxs-lookup"><span data-stu-id="0a55a-144">Note that the cheques data model element is bound to the TmpChequePrintout table that, at runtime, will contain records for cheques that the user has selected for printing.</span></span>   
29. <span data-ttu-id="0a55a-145">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="0a55a-145">Close the page.</span></span>
30. <span data-ttu-id="0a55a-146">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="0a55a-146">Close the page.</span></span>
31. <span data-ttu-id="0a55a-147">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="0a55a-147">Close the page.</span></span>

## <a name="review-the-imported-format"></a><span data-ttu-id="0a55a-148">インポートされた形式を確認する</span><span class="sxs-lookup"><span data-stu-id="0a55a-148">Review the imported format</span></span>
1. <span data-ttu-id="0a55a-149">ツリーで、「小切手のモデル」を展開します。</span><span class="sxs-lookup"><span data-stu-id="0a55a-149">In the tree, expand 'Model for cheques'.</span></span>
2. <span data-ttu-id="0a55a-150">ツリーで、「小切手のモデル\小切手の印刷形式」を選択します。</span><span class="sxs-lookup"><span data-stu-id="0a55a-150">In the tree, select 'Model for cheques\Cheques printing format'.</span></span>
3. <span data-ttu-id="0a55a-151">[デザイナー] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="0a55a-151">Click Designer.</span></span>
4. <span data-ttu-id="0a55a-152">[添付ファイル] クリックします。</span><span class="sxs-lookup"><span data-stu-id="0a55a-152">Click Attachments.</span></span>
5. <span data-ttu-id="0a55a-153">[開く] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="0a55a-153">Click Open.</span></span>
    * <span data-ttu-id="0a55a-154">Excel で添付されたレポートのテンプレートを開きます。</span><span class="sxs-lookup"><span data-stu-id="0a55a-154">Open the attached report’s template in Excel.</span></span>  
    * <span data-ttu-id="0a55a-155">小切手を印刷するのに使用する添付のレポートの Excel テンプレートを確認します。</span><span class="sxs-lookup"><span data-stu-id="0a55a-155">Review the attached report’s Excel template that will be used to print cheques.</span></span> <span data-ttu-id="0a55a-156">そのテンプレートにはページごとに 2 つの小切手が含まれており、プレプリントされたフォームに小切手を印刷するよう設計されています。</span><span class="sxs-lookup"><span data-stu-id="0a55a-156">The template contains two cheques per page and is designed to print cheques to the preprinted form.</span></span> <span data-ttu-id="0a55a-157">2 つの空白の画像が埋め込まれていることに注意してください。</span><span class="sxs-lookup"><span data-stu-id="0a55a-157">Note that two blank images are embedded.</span></span> <span data-ttu-id="0a55a-158">これらの空白の画像は、会社のロゴおよび支払を承認している人の署名用です。</span><span class="sxs-lookup"><span data-stu-id="0a55a-158">These blank images are for the company logo and the signature of the person who is authorizing a payment.</span></span> <span data-ttu-id="0a55a-159">Excel で、画像がそれぞれ CompLogo と SignatureImage という名前であることを確認します。</span><span class="sxs-lookup"><span data-stu-id="0a55a-159">Verify that the images are named CompLogo and SignatureImage, respectively, in Excel.</span></span>   
6. <span data-ttu-id="0a55a-160">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="0a55a-160">Close the page.</span></span>
7. <span data-ttu-id="0a55a-161">ツリーで、「Report」を展開します。</span><span class="sxs-lookup"><span data-stu-id="0a55a-161">In the tree, expand 'Report'.</span></span>
8. <span data-ttu-id="0a55a-162">ツリーで、「Report\ChequeLines」を展開します。</span><span class="sxs-lookup"><span data-stu-id="0a55a-162">In the tree, expand 'Report\ChequeLines'.</span></span>
9. <span data-ttu-id="0a55a-163">ツリーで、「Report\ChequeLines\CompLogo」を選択します。</span><span class="sxs-lookup"><span data-stu-id="0a55a-163">In the tree, select 'Report\ChequeLines\CompLogo'.</span></span>
10. <span data-ttu-id="0a55a-164">[詳細の表示] をオンに切り替えます。</span><span class="sxs-lookup"><span data-stu-id="0a55a-164">Toggle 'Show details' on.</span></span>
    * <span data-ttu-id="0a55a-165">'CompLogo' 形式のセル要素が、レポートに会社のロゴ画像を追加するために使用する Excel 項目を表すことに注意してください。</span><span class="sxs-lookup"><span data-stu-id="0a55a-165">Note that the ‘CompLogo’ format’s cell element represents the Excel item that is used to populate the company logo image in the report.</span></span> <span data-ttu-id="0a55a-166">この形式要素は、実行時にバイナリ形式の会社のロゴ画像が含まれる画像データ モデル要素にバインドされます。</span><span class="sxs-lookup"><span data-stu-id="0a55a-166">This format element is bound to the image data model element that, at runtime, contains a company logo image in binary format.</span></span>   
11. <span data-ttu-id="0a55a-167">[マッピング] タブをクリックします。</span><span class="sxs-lookup"><span data-stu-id="0a55a-167">Click the Mapping tab.</span></span>
12. <span data-ttu-id="0a55a-168">[編集が有効] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="0a55a-168">Click Edit enabled.</span></span>
    * <span data-ttu-id="0a55a-169">なお、「CompLogo」形式のセル要素は有効にならないように作成することができます。</span><span class="sxs-lookup"><span data-stu-id="0a55a-169">Note that you can make the ‘CompLogo’ format’s cell element so that it’s no longer enabled.</span></span> <span data-ttu-id="0a55a-170">この場合、関連付けられている Excel 画像要素は、生成されたレポートで会社のロゴを非表示にします。</span><span class="sxs-lookup"><span data-stu-id="0a55a-170">In this case, the associated Excel image element will hide a company logo in the generated report.</span></span> <span data-ttu-id="0a55a-171">有効な式が TRUE を返し、定義されたバインディングが画像を渡さない場合、関連付けられている Excel 画像要素は、Excel テンプレートに保存されている画像を表示します。</span><span class="sxs-lookup"><span data-stu-id="0a55a-171">If the enabled expression returns TRUE and the defined binding brings no image, the associated Excel image element will show an image that has been saved in the Excel template.</span></span>   
13. <span data-ttu-id="0a55a-172">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="0a55a-172">Close the page.</span></span>
14. <span data-ttu-id="0a55a-173">ツリーで、「labels: Container」を展開します。</span><span class="sxs-lookup"><span data-stu-id="0a55a-173">In the tree, expand 'labels: Container'.</span></span>
    * <span data-ttu-id="0a55a-174">テスト用に作成されている場合、プレプリントされた小切手フォームに表示されるいくつかのラベルがレポートに含まれます。</span><span class="sxs-lookup"><span data-stu-id="0a55a-174">Some labels that are presented in the preprinted cheque form will be included in the report when it’s created for testing purposes.</span></span> <span data-ttu-id="0a55a-175">ただし、それらのラベルは、プレプリントされたフォームにすでに含まれているために実際の印刷中には印刷されません。</span><span class="sxs-lookup"><span data-stu-id="0a55a-175">However, those labels won’t be printed during real printing, because the preprinted form already includes them.</span></span>  
15. <span data-ttu-id="0a55a-176">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="0a55a-176">Close the page.</span></span>


