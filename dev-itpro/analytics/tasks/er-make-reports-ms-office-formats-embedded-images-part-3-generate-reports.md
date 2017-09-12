--- 
title: "電子申告 (ER) 用に埋め込み画像付きで Microsoft Office 形式のレポートを生成する"
description: "次のステップでは、「システム管理者」または「電子申告開発者」ロールのユーザーが、電子申告 (ER) のコンフィギュレーションを設計し、埋め込み画像を含む MS Office 形式 (Excel および Word) で電子ドキュメントを生成する方法を説明します。"
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
ms.openlocfilehash: de2840ebc6c91e313546859f5c0d8939eb80977b
ms.contentlocale: ja-jp
ms.lasthandoff: 08/29/2017

---
# <a name="generate-reports-in-microsoft-office-formats-with-embedded-images-for-electronic-reporting-er"></a><span data-ttu-id="5085f-103">電子申告 (ER) 用に埋め込み画像付きで Microsoft Office 形式のレポートを生成する</span><span class="sxs-lookup"><span data-stu-id="5085f-103">Generate reports in Microsoft Office formats with embedded images for electronic reporting (ER)</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="5085f-104">次のステップでは、「システム管理者」または「電子申告開発者」ロールのユーザーが、電子申告 (ER) のコンフィギュレーションを設計し、埋め込み画像を含む MS Office 形式 (Excel および Word) で電子ドキュメントを生成する方法を説明します。</span><span class="sxs-lookup"><span data-stu-id="5085f-104">The following steps explain how a user playing either ‘System administrator’ or ‘Electronic reporting developer’ role can design Electronic reporting (ER) configurations to generate electronic documents in MS office formats (Excel and Word) containing embedded images.</span></span>

<span data-ttu-id="5085f-105">この例では、サンプル会社「Litware, Inc.」用に作成した ER コンフィギュレーションを使用します。</span><span class="sxs-lookup"><span data-stu-id="5085f-105">In this example, you will use created ER configurations for sample company, ‘Litware, Inc.’.</span></span>  <span data-ttu-id="5085f-106">これらのステップを完了するには、まず、「ER 埋め込み画像付きで MS Office 形式のレポートを作成する (パート 2: コンフィギュレーションの確認)」タスク ガイドにあるステップを完了する必要があります。</span><span class="sxs-lookup"><span data-stu-id="5085f-106">To complete these steps, you must first complete the steps in the “ER Make reports in MS Office formats with embedded images (Part 2: Review configurations)” task guide.</span></span> <span data-ttu-id="5085f-107">これらのステップは「USMF」会社で実行できます。</span><span class="sxs-lookup"><span data-stu-id="5085f-107">These steps can be performed in ‘USMF’ company.</span></span>


## <a name="run-format-with-initial-model-mapping"></a><span data-ttu-id="5085f-108">初期モデル マッピングを使用して形式を実行する</span><span class="sxs-lookup"><span data-stu-id="5085f-108">Run format with initial model mapping</span></span>
1. <span data-ttu-id="5085f-109">[現金および銀行管理] > [銀行口座] > [銀行口座] の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="5085f-109">Go to Cash and bank management > Bank accounts > Bank accounts.</span></span>
2. <span data-ttu-id="5085f-110">クイック フィルターを使用して、値が「USMF OPER」である [銀行口座] フィールドをフィルター処理します。</span><span class="sxs-lookup"><span data-stu-id="5085f-110">Use the Quick Filter to filter on the Bank account field with a value of 'USMF OPER'.</span></span>
3. <span data-ttu-id="5085f-111">アクション ペインで、[設定] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="5085f-111">On the Action Pane, click Set up.</span></span>
4. <span data-ttu-id="5085f-112">[小切手] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="5085f-112">Click Check.</span></span>
5. <span data-ttu-id="5085f-113">[印刷テスト] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="5085f-113">Click Print test.</span></span>
    * <span data-ttu-id="5085f-114">テスト目的で形式を実行します。</span><span class="sxs-lookup"><span data-stu-id="5085f-114">Run the format for testing purposes.</span></span>  
6. <span data-ttu-id="5085f-115">[譲渡性小切手フォーマット] フィールドで、[はい] を選択します。</span><span class="sxs-lookup"><span data-stu-id="5085f-115">Select Yes in the Negotiable check format field.</span></span>
7. <span data-ttu-id="5085f-116">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="5085f-116">Click OK.</span></span>
    * <span data-ttu-id="5085f-117">作成した出荷を確認します。</span><span class="sxs-lookup"><span data-stu-id="5085f-117">Review the created output.</span></span> <span data-ttu-id="5085f-118">なお、会社のロゴは権限者の署名にもレポートにも表示されます。</span><span class="sxs-lookup"><span data-stu-id="5085f-118">Note that the company logo is presented in the report as well as the authorized person’s signature.</span></span> <span data-ttu-id="5085f-119">署名画像は、選択した銀行口座に関連付けられた小切手のレイアウト レコードの「コンテナー」データ型のフィールドから取得されます。</span><span class="sxs-lookup"><span data-stu-id="5085f-119">The signature image is taken from the field of the ‘Container’ data type of the cheque layout record which is associated with the selected bank account.</span></span>  
8. <span data-ttu-id="5085f-120">[コピー] セクションを展開します。</span><span class="sxs-lookup"><span data-stu-id="5085f-120">Expand the Copies section.</span></span>
9. <span data-ttu-id="5085f-121">[編集] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="5085f-121">Click Edit.</span></span>
10. <span data-ttu-id="5085f-122">[透かし] フィールドで、[無効として透かしを印刷] を入力します。</span><span class="sxs-lookup"><span data-stu-id="5085f-122">In the Watermark field, enter 'Print watermark as Void'.</span></span>
    * <span data-ttu-id="5085f-123">透かしレイアウトの設定を変更して、Excel 図形要素の生成ドキュメントに透かしのテキストを表示します。</span><span class="sxs-lookup"><span data-stu-id="5085f-123">Change the watermark layout setting to show the watermark text in generating document in an Excel shape element.</span></span>  
11. <span data-ttu-id="5085f-124">[印刷テスト] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="5085f-124">Click Print test.</span></span>
12. <span data-ttu-id="5085f-125">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="5085f-125">Click OK.</span></span>
    * <span data-ttu-id="5085f-126">作成した出荷を確認します。</span><span class="sxs-lookup"><span data-stu-id="5085f-126">Review the created output.</span></span> <span data-ttu-id="5085f-127">なお、選択オプションに従って、作成済みのレポートに透かしが表示されます。</span><span class="sxs-lookup"><span data-stu-id="5085f-127">Note that the watermark is shown in the created report in accordance to the selection option.</span></span>  
13. <span data-ttu-id="5085f-128">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="5085f-128">Close the page.</span></span>
14. <span data-ttu-id="5085f-129">[アクション] ウィンドウで [支払の管理] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="5085f-129">On the Action Pane, click Manage payments.</span></span>
15. <span data-ttu-id="5085f-130">[小切手] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="5085f-130">Click Checks.</span></span>
16. <span data-ttu-id="5085f-131">[フィルターの表示] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="5085f-131">Click Show filters.</span></span>
17. <span data-ttu-id="5085f-132">次のフィルターを適用します。"次の値のいずれか" フィルター演算子を使用して、[小切手番号] フィールドで "381","385","389" のフィルター値を入力。</span><span class="sxs-lookup"><span data-stu-id="5085f-132">Apply the following filters: Enter a filter value of "381","385","389" on the "Check number" field using the "is one of" filter operator.</span></span>
18. <span data-ttu-id="5085f-133">リストで、すべての行をマークします。</span><span class="sxs-lookup"><span data-stu-id="5085f-133">In the list, mark all rows.</span></span>
19. <span data-ttu-id="5085f-134">[小切手のコピーの印刷] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="5085f-134">Click Print check copy.</span></span>
    * <span data-ttu-id="5085f-135">形式を実行して、選択した小切手を再印刷します。</span><span class="sxs-lookup"><span data-stu-id="5085f-135">Run the format to re-print the selected cheques.</span></span>  
    * <span data-ttu-id="5085f-136">作成した出荷を確認します。</span><span class="sxs-lookup"><span data-stu-id="5085f-136">Review the created output.</span></span> <span data-ttu-id="5085f-137">選択した小切手が再印刷されていることに注意してください。</span><span class="sxs-lookup"><span data-stu-id="5085f-137">Note that the selected cheques have been re-printed.</span></span> <span data-ttu-id="5085f-138">会社のロゴとラベルは、事前に印刷されたフォームに表示されているので印刷されません。</span><span class="sxs-lookup"><span data-stu-id="5085f-138">The company logo and labels are not printed out since they are presented on the pre-printed form.</span></span>  

## <a name="modify-the-mapping-of-the-imported-data-model"></a><span data-ttu-id="5085f-139">インポート済データ モデルのマッピングを変更する</span><span class="sxs-lookup"><span data-stu-id="5085f-139">Modify the mapping of the imported data model</span></span>
1. <span data-ttu-id="5085f-140">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="5085f-140">Close the page.</span></span>
2. <span data-ttu-id="5085f-141">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="5085f-141">Close the page.</span></span>
3. <span data-ttu-id="5085f-142">[組織管理] > [電子申告] > [コンフィギュレーション] に移動します。</span><span class="sxs-lookup"><span data-stu-id="5085f-142">Go to Organization administration > Electronic reporting > Configurations.</span></span>
4. <span data-ttu-id="5085f-143">ツリーで、「小切手のモデル」を選択します。</span><span class="sxs-lookup"><span data-stu-id="5085f-143">In the tree, select 'Model for cheques'.</span></span>
5. <span data-ttu-id="5085f-144">[デザイナー] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="5085f-144">Click Designer.</span></span>
6. <span data-ttu-id="5085f-145">[モデルからデータ ソースへのマップ] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="5085f-145">Click Map model to datasource.</span></span>
7. <span data-ttu-id="5085f-146">[デザイナー] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="5085f-146">Click Designer.</span></span>
    * <span data-ttu-id="5085f-147">選択した銀行口座に関連付けられている小切手レイアウト レコードに関連付けれたファイルから署名画像を取得するためのデータ モデルの署名品目のバインディングは変更されます。</span><span class="sxs-lookup"><span data-stu-id="5085f-147">We will change the binding of the data model’s signature item to get the signature image from the file that has been attached to the cheque layout record which is associated with the selected bank account.</span></span>  
8. <span data-ttu-id="5085f-148">[詳細の表示] をオフにします。</span><span class="sxs-lookup"><span data-stu-id="5085f-148">Turn Show details off.</span></span>
9. <span data-ttu-id="5085f-149">ツリーで、「レイアウト」を展開します。</span><span class="sxs-lookup"><span data-stu-id="5085f-149">In the tree, expand 'layout'.</span></span>
10. <span data-ttu-id="5085f-150">ツリーで、「レイアウト\署名」を展開します。</span><span class="sxs-lookup"><span data-stu-id="5085f-150">In the tree, expand 'layout\signature'.</span></span>
11. <span data-ttu-id="5085f-151">ツリーで、「レイアウト\署名\image = chequesaccount.'<Relations'.BankChequeLayout.Signature1Bmp」を選択します。</span><span class="sxs-lookup"><span data-stu-id="5085f-151">In the tree, select 'layout\signature\image = chequesaccount.'<Relations'.BankChequeLayout.Signature1Bmp'.</span></span>
12. <span data-ttu-id="5085f-152">ツリーで、「chequesaccount」を展開します。</span><span class="sxs-lookup"><span data-stu-id="5085f-152">In the tree, expand 'chequesaccount'.</span></span>
13. <span data-ttu-id="5085f-153">ツリーで、「chequesaccount\<Relations」を展開します。</span><span class="sxs-lookup"><span data-stu-id="5085f-153">In the tree, expand 'chequesaccount\<Relations'.</span></span>
14. <span data-ttu-id="5085f-154">ツリーで、「chequesaccount\<Relations\BankChequeLayout」を展開します。</span><span class="sxs-lookup"><span data-stu-id="5085f-154">In the tree, expand 'chequesaccount\<Relations\BankChequeLayout'.</span></span>
15. <span data-ttu-id="5085f-155">ツリーで、「chequesaccount\<Relations\BankChequeLayout\<Relations」を展開します。</span><span class="sxs-lookup"><span data-stu-id="5085f-155">In the tree, expand 'chequesaccount\<Relations\BankChequeLayout\<Relations'.</span></span>
16. <span data-ttu-id="5085f-156">ツリーで、「chequesaccount\<Relations\BankChequeLayout\<Relations\<Documents」を展開します。</span><span class="sxs-lookup"><span data-stu-id="5085f-156">In the tree, expand 'chequesaccount\<Relations\BankChequeLayout\<Relations\<Documents'.</span></span>
17. <span data-ttu-id="5085f-157">ツリーで、「chequesaccount\<Relations\BankChequeLayout\<Relations\<Documents\getFileContentAsContainer()」を選択します。</span><span class="sxs-lookup"><span data-stu-id="5085f-157">In the tree, select 'chequesaccount\<Relations\BankChequeLayout\<Relations\<Documents\getFileContentAsContainer()'.</span></span>
18. <span data-ttu-id="5085f-158">[バインド] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="5085f-158">Click Bind.</span></span>
19. <span data-ttu-id="5085f-159">[保存] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="5085f-159">Click Save.</span></span>
20. <span data-ttu-id="5085f-160">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="5085f-160">Close the page.</span></span>
21. <span data-ttu-id="5085f-161">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="5085f-161">Close the page.</span></span>
22. <span data-ttu-id="5085f-162">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="5085f-162">Close the page.</span></span>
23. <span data-ttu-id="5085f-163">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="5085f-163">Close the page.</span></span>

## <a name="run-format-using-the-adjusted-model-mapping"></a><span data-ttu-id="5085f-164">調整済モデル マッピングを使用して形式を実行する</span><span class="sxs-lookup"><span data-stu-id="5085f-164">Run format using the adjusted model mapping</span></span>
1. <span data-ttu-id="5085f-165">[現金および銀行管理] > [銀行口座] > [銀行口座] の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="5085f-165">Go to Cash and bank management > Bank accounts > Bank accounts.</span></span>
2. <span data-ttu-id="5085f-166">クイック フィルターを使用して、レコードを見つけます。</span><span class="sxs-lookup"><span data-stu-id="5085f-166">Use the Quick Filter to find records.</span></span> <span data-ttu-id="5085f-167">たとえば、「USMF OPER」という値を含む [銀行口座] フィールドをフィルターします。</span><span class="sxs-lookup"><span data-stu-id="5085f-167">For example, filter on the Bank account field with a value of 'USMF OPER'.</span></span>
3. <span data-ttu-id="5085f-168">アクション ペインで、[設定] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="5085f-168">On the Action Pane, click Set up.</span></span>
4. <span data-ttu-id="5085f-169">[小切手] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="5085f-169">Click Check.</span></span>
5. <span data-ttu-id="5085f-170">[印刷テスト] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="5085f-170">Click Print test.</span></span>
6. <span data-ttu-id="5085f-171">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="5085f-171">Click OK.</span></span>
    * <span data-ttu-id="5085f-172">作成した出荷を確認します。</span><span class="sxs-lookup"><span data-stu-id="5085f-172">Review the created output.</span></span> <span data-ttu-id="5085f-173">ドキュメント管理添付ファイルからの画像が権限者の署名として表示されることに注意してください。</span><span class="sxs-lookup"><span data-stu-id="5085f-173">Note that the image from the Document Management attachment is presented as the signature of an authorized person.</span></span>  

## <a name="use-ms-word-document-as-a-template-in-the-imported-format"></a><span data-ttu-id="5085f-174">インポートされた形式で MS Word ドキュメントをテンプレートとして使用する</span><span class="sxs-lookup"><span data-stu-id="5085f-174">Use MS Word document as a template in the imported format</span></span>
1. <span data-ttu-id="5085f-175">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="5085f-175">Close the page.</span></span>
2. <span data-ttu-id="5085f-176">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="5085f-176">Close the page.</span></span>
3. <span data-ttu-id="5085f-177">[組織管理] > [電子申告] > [コンフィギュレーション] に移動します。</span><span class="sxs-lookup"><span data-stu-id="5085f-177">Go to Organization administration > Electronic reporting > Configurations.</span></span>
4. <span data-ttu-id="5085f-178">ツリーで、「小切手のモデル」を展開します。</span><span class="sxs-lookup"><span data-stu-id="5085f-178">In the tree, expand 'Model for cheques'.</span></span>
5. <span data-ttu-id="5085f-179">ツリーで、「小切手のモデル\小切手の印刷形式」を選択します。</span><span class="sxs-lookup"><span data-stu-id="5085f-179">In the tree, select 'Model for cheques\Cheques printing format'.</span></span>
6. <span data-ttu-id="5085f-180">[デザイナー] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="5085f-180">Click Designer.</span></span>
7. <span data-ttu-id="5085f-181">[添付ファイル] クリックします。</span><span class="sxs-lookup"><span data-stu-id="5085f-181">Click Attachments.</span></span>
8. <span data-ttu-id="5085f-182">[削除] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="5085f-182">Click Delete.</span></span>
9. <span data-ttu-id="5085f-183">[はい] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="5085f-183">Click Yes.</span></span>
10. <span data-ttu-id="5085f-184">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="5085f-184">Click New.</span></span>
11. <span data-ttu-id="5085f-185">[ファイル] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="5085f-185">Click File.</span></span>
    * <span data-ttu-id="5085f-186">[参照] をクリックし、事前にダウンロードした「小切手テンプレート Word.docx」ファイルを選択します。</span><span class="sxs-lookup"><span data-stu-id="5085f-186">Click Browse and select the downloaded in advance ‘Cheque template Word.docx’ file.</span></span>  
12. <span data-ttu-id="5085f-187">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="5085f-187">Close the page.</span></span>
13. <span data-ttu-id="5085f-188">[テンプレート] フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="5085f-188">In the Template field, enter or select a value.</span></span>
14. <span data-ttu-id="5085f-189">[保存] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="5085f-189">Click Save.</span></span>
15. <span data-ttu-id="5085f-190">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="5085f-190">Close the page.</span></span>
16. <span data-ttu-id="5085f-191">[編集] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="5085f-191">Click Edit.</span></span>
17. <span data-ttu-id="5085f-192">[ドラフトの実行] フィールドで、[はい] を選択します。</span><span class="sxs-lookup"><span data-stu-id="5085f-192">Select Yes in the Run Draft field.</span></span>
18. <span data-ttu-id="5085f-193">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="5085f-193">Close the page.</span></span>
19. <span data-ttu-id="5085f-194">[現金および銀行管理] > [銀行口座] > [銀行口座] の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="5085f-194">Go to Cash and bank management > Bank accounts > Bank accounts.</span></span>
20. <span data-ttu-id="5085f-195">クイック フィルターを使用して、値が「USMF OPER」である [銀行口座] フィールドをフィルター処理します。</span><span class="sxs-lookup"><span data-stu-id="5085f-195">Use the Quick Filter to filter on the Bank account field with a value of 'USMF OPER'.</span></span>
21. <span data-ttu-id="5085f-196">[小切手] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="5085f-196">Click Check.</span></span>
22. <span data-ttu-id="5085f-197">[印刷テスト] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="5085f-197">Click Print test.</span></span>
23. <span data-ttu-id="5085f-198">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="5085f-198">Click OK.</span></span>
    * <span data-ttu-id="5085f-199">作成した出荷を確認します。</span><span class="sxs-lookup"><span data-stu-id="5085f-199">Review the created output.</span></span> <span data-ttu-id="5085f-200">出力は、会社のロゴ、権限者の署名および透かしの選択テキストを表示する埋め込み画像付きの MS Word ドキュメントとして生成されたことに注意してください。</span><span class="sxs-lookup"><span data-stu-id="5085f-200">Note that the output has been generated as a MS Word document with embedded images presenting the company logo, the signature of an authorized person and the selected text of the watermark.</span></span>  


