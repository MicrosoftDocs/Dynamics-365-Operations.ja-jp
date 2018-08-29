--- 
title: "Word 形式でレポートを生成するための ER コンフィギュレーションのデザイン"
description: "次の手順では、システム管理者または電子レポート開発者のロールを持つユーザーが、電子レポート (ER) 形式を構成して、Microsoft Word ファイルとしてレポートを生成する方法を説明します。"
author: NickSelin
manager: AnnBe
ms.date: 12/21/2016
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
ms.sourcegitcommit: e782d33f3748524491dace28008cd9148ae70529
ms.openlocfilehash: 615ab4a4f932478b8b847112d4fed8310187f03b
ms.contentlocale: ja-jp
ms.lasthandoff: 08/09/2018

---
# <a name="design-er-configurations-to-generate-reports-in-word-format"></a><span data-ttu-id="315fa-103">Word 形式でレポートを生成するための ER コンフィギュレーションのデザイン</span><span class="sxs-lookup"><span data-stu-id="315fa-103">Design ER configurations to generate reports in Word format</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="315fa-104">次の手順では、システム管理者または電子レポート開発者のロールを持つユーザーが、電子レポート (ER) 形式を構成して、Microsoft Word ファイルとしてレポートを生成する方法を説明します。</span><span class="sxs-lookup"><span data-stu-id="315fa-104">The following steps explain how a user in either the System administrator or Electronic reporting developer role can configure an Electronic reporting (ER) formats to generate reports as Microsoft Word files.</span></span> <span data-ttu-id="315fa-105">これらのステップは GBSI 会社で実行できます。</span><span class="sxs-lookup"><span data-stu-id="315fa-105">These steps can be performed in the GBSI company.</span></span>

<span data-ttu-id="315fa-106">これらのステップを完了するには、「OPENXML 形式でレポートを生成する ER コンフィギュレーションの作成」タスク ガイドの手順を最初に完了する必要があります。</span><span class="sxs-lookup"><span data-stu-id="315fa-106">To complete these steps, you must first complete the steps in the “Create an ER configuration for generating reports in OPENXML format” task guide.</span></span> <span data-ttu-id="315fa-107">また事前に、サンプル レポート用に次のテンプレートをダウンロードしてローカルに保存する必要があります。</span><span class="sxs-lookup"><span data-stu-id="315fa-107">In advance, you must also download and save the following templates locally for the sample report:</span></span>

[<span data-ttu-id="315fa-108">支払レポートのテンプレート</span><span class="sxs-lookup"><span data-stu-id="315fa-108">Template of Payment Report</span></span>](https://go.microsoft.com/fwlink/?linkid=862266)

[<span data-ttu-id="315fa-109">支払レポートのバインドされたテンプレート</span><span class="sxs-lookup"><span data-stu-id="315fa-109">Bounded Template of Payment Report</span></span>](https://go.microsoft.com/fwlink/?linkid=862266)

<span data-ttu-id="315fa-110">この手順は、Microsoft Dynamics 365 for Operations バージョン 1611 に追加された機能です。</span><span class="sxs-lookup"><span data-stu-id="315fa-110">This procedure is for a feature that was added in Microsoft Dynamics 365 for Operations version 1611.</span></span>


## <a name="select-the-existing-er-report-configuration"></a><span data-ttu-id="315fa-111">既存の ER レポート コンフィギュレーションを選択します</span><span class="sxs-lookup"><span data-stu-id="315fa-111">Select the existing ER report configuration</span></span>
1. <span data-ttu-id="315fa-112">[組織管理] > [ワークスペース] > [電子申告] の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="315fa-112">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
    * <span data-ttu-id="315fa-113">コンフィギュレーション プロバイダー「Litware、Inc.」を確認します。</span><span class="sxs-lookup"><span data-stu-id="315fa-113">Make sure that the configuration provider ‘Litware, Inc.’</span></span> <span data-ttu-id="315fa-114">有効として選択されます。</span><span class="sxs-lookup"><span data-stu-id="315fa-114">is selected as active.</span></span>  
2. <span data-ttu-id="315fa-115">[コンフィギュレーションをレポートする] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="315fa-115">Click Reporting configurations.</span></span>
    * <span data-ttu-id="315fa-116">OPENXML 形式でレポート出力を生成するように最初に設計された既存の ER コンフィギュレーションを再使用します。</span><span class="sxs-lookup"><span data-stu-id="315fa-116">We will re-use the existing ER configuration that has been originally designed to generate the report output in OPENXML format.</span></span>  
3. <span data-ttu-id="315fa-117">ツリーで、「Payment model」を展開します。</span><span class="sxs-lookup"><span data-stu-id="315fa-117">In the tree, expand 'Payment model'.</span></span>
4. <span data-ttu-id="315fa-118">ツリーで、「Payment model\Sample worksheet report」を選択します。</span><span class="sxs-lookup"><span data-stu-id="315fa-118">In the tree, select 'Payment model\Sample worksheet report'.</span></span>
5. <span data-ttu-id="315fa-119">[デザイナー] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="315fa-119">Click Designer.</span></span>

## <a name="replace-the-excel-template-with-the-word-template"></a><span data-ttu-id="315fa-120">Excel テンプレートを Word テンプレートに置き換えます</span><span class="sxs-lookup"><span data-stu-id="315fa-120">Replace the Excel template with the Word template</span></span>
    * <span data-ttu-id="315fa-121">現在は、OPENXML 形式で出力を生成するテンプレートとして Excel ドキュメントが使用されます。</span><span class="sxs-lookup"><span data-stu-id="315fa-121">Currently, the Excel document is used as a template to generate the output in OPENXML format.</span></span> <span data-ttu-id="315fa-122">レポートのテンプレートを Word 形式でインポートします。</span><span class="sxs-lookup"><span data-stu-id="315fa-122">We will import the report’s template in Word format.</span></span>  
1. <span data-ttu-id="315fa-123">[添付ファイル] クリックします。</span><span class="sxs-lookup"><span data-stu-id="315fa-123">Click Attachments.</span></span>
    * <span data-ttu-id="315fa-124">既存の Excel テンプレートを、以前ダウンロードした Word テンプレート 支払いレポートテンプレートに置き換えます。</span><span class="sxs-lookup"><span data-stu-id="315fa-124">Replace the existing Excel template with the Word template that you downloaded earlier, Template of Payment Report.</span></span> <span data-ttu-id="315fa-125">このテンプレートには、ER 出力を生成するドキュメントのレイアウトのみが含まれていることに注意してください。</span><span class="sxs-lookup"><span data-stu-id="315fa-125">Note, this template only contains the layout of the document we want to generate as ER output.</span></span>  
2. <span data-ttu-id="315fa-126">[削除] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="315fa-126">Click Delete.</span></span>
3. <span data-ttu-id="315fa-127">[はい] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="315fa-127">Click Yes.</span></span>
4. <span data-ttu-id="315fa-128">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="315fa-128">Click New.</span></span>
5. <span data-ttu-id="315fa-129">[ファイル] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="315fa-129">Click File.</span></span>
6. <span data-ttu-id="315fa-130">[参照] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="315fa-130">Click Browse.</span></span> <span data-ttu-id="315fa-131">以前ダウンロードした SampleVendPaymDocReport.docx を参照して選択します。</span><span class="sxs-lookup"><span data-stu-id="315fa-131">Navigate to and select SampleVendPaymDocReport.docx that you previously downloaded.</span></span> <span data-ttu-id="315fa-132">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="315fa-132">Click OK.</span></span>
    * <span data-ttu-id="315fa-133">前のステップでダウンロードしたテンプレートを選択します。</span><span class="sxs-lookup"><span data-stu-id="315fa-133">Select the template that you downloaded in the previous step.</span></span>  
7. <span data-ttu-id="315fa-134">[テンプレート] フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="315fa-134">In the Template field, enter or select a value.</span></span>

## <a name="extend-the-word-template-by-adding-a-custom-xml-part"></a><span data-ttu-id="315fa-135">カスタム XML 部分を追加して、Word テンプレートを拡張します。</span><span class="sxs-lookup"><span data-stu-id="315fa-135">Extend the Word template by adding a custom XML part</span></span>
1. <span data-ttu-id="315fa-136">[保存] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="315fa-136">Click Save.</span></span>
    * <span data-ttu-id="315fa-137">保存アクションは、構成の変更を保存するだけでなく、添付されている Word テンプレートも更新します。</span><span class="sxs-lookup"><span data-stu-id="315fa-137">In addition to storing configuration changes, the Save action also updates the attached Word template.</span></span> <span data-ttu-id="315fa-138">設計された形式の構造は、'報告' という名前の新しいカスタム XML 部分として、関連付けられている Word 文書にポートされます。</span><span class="sxs-lookup"><span data-stu-id="315fa-138">The structure of the designed format is ported to the attached Word document as a new custom XML part with the name ‘Report’.</span></span> <span data-ttu-id="315fa-139">関連付けられている Word テンプレートには、ER 出力として生成するドキュメントのレイアウトを含むだけでなく、実行時に ER がこのテンプレートに実装するデータの構造も含まれます。</span><span class="sxs-lookup"><span data-stu-id="315fa-139">Note that the attached Word template contains not only the layout of the document we want to generate as ER output, it also contains the structure of data that ER will populate into this template at runtime.</span></span>  
2. <span data-ttu-id="315fa-140">[添付ファイル] クリックします。</span><span class="sxs-lookup"><span data-stu-id="315fa-140">Click Attachments.</span></span>
    * <span data-ttu-id="315fa-141">ここで、カスタム XML 部分 '報告' の要素を Word ドキュメント パーツにバインドする必要があります。</span><span class="sxs-lookup"><span data-stu-id="315fa-141">Now you need to bind the elements of the custom XML part ‘Report’ to the Word document parts.</span></span>  
    * <span data-ttu-id="315fa-142">カスタム XML パーツの要素でバインドされたコンテンツ コントロールを含む形式としてデザイン可能な Word 文書に慣れている場合は、次のサブタスクのすべてのステップを再生して、そのようなドキュメントを作成します。</span><span class="sxs-lookup"><span data-stu-id="315fa-142">If you're familiar with Word documents that can be designed as forms containing content controls that are bounded with elements of custom XML parts – play all steps of the next sub-task to create such a document.</span></span> <span data-ttu-id="315fa-143">詳細については、こちらのリンク (https://support.office.com/en-us/article/Create-forms-that-users-complete-or-print-in-Word-040c5cc1-e309-445b-94ac-542f732c8c8b?ui=en-US&rs=en-US&ad=US) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="315fa-143">For more details, see this link https://support.office.com/en-us/article/Create-forms-that-users-complete-or-print-in-Word-040c5cc1-e309-445b-94ac-542f732c8c8b?ui=en-US&rs=en-US&ad=US.</span></span> <span data-ttu-id="315fa-144">そうでない場合は、次のサブタスクのすべてのステップをスキップします。</span><span class="sxs-lookup"><span data-stu-id="315fa-144">Otherwise, skip all the steps in the next sub-task.</span></span>  

## <a name="get-word-with-custom-xml-part-to-do-data-bindings"></a><span data-ttu-id="315fa-145">データ バインドを行うカスタム XML 部分と共に Word を取得します。</span><span class="sxs-lookup"><span data-stu-id="315fa-145">Get Word with custom XML part to do data bindings</span></span>
    * <span data-ttu-id="315fa-146">Word でこのドキュメントを開き、以下の操作を行います: - [Word 開発者] タブを開きます (有効になっていない場合は、リボンをカスタマイズします)。</span><span class="sxs-lookup"><span data-stu-id="315fa-146">Open this document in Word and do the following:  - Open the Word Developer tab (customize the ribbon if it is not enabled yet).</span></span>  <span data-ttu-id="315fa-147">- XML マッピング ウィンドウを選択します。</span><span class="sxs-lookup"><span data-stu-id="315fa-147">- Select XML mapping pane.</span></span>  <span data-ttu-id="315fa-148">- ルックアップで、'報告' カスタム XML 部分を選択します。</span><span class="sxs-lookup"><span data-stu-id="315fa-148">- Select the ‘Report’ custom XML part in the lookup.</span></span>  <span data-ttu-id="315fa-149">- 選択したカスタム XML 部分の要素と Word ドキュメントのコンテンツ コントロールとのマッピングを行います。</span><span class="sxs-lookup"><span data-stu-id="315fa-149">- Do mapping of the elements of the selected custom XML part and content controls of the Word document.</span></span>  <span data-ttu-id="315fa-150">- ローカル ドライブに更新された Word ドキュメントを保存します。</span><span class="sxs-lookup"><span data-stu-id="315fa-150">- Save the updated Word document on a local drive.</span></span>  

## <a name="upload-the-word-template-with-custom-xml-part-bounded-to-content-controls"></a><span data-ttu-id="315fa-151">コンテンツ コントロールにバインドされたカスタム XML 部分と共に Word テンプレートをアップロードします。</span><span class="sxs-lookup"><span data-stu-id="315fa-151">Upload the Word template with custom XML part bounded to content controls</span></span>
1. <span data-ttu-id="315fa-152">[削除] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="315fa-152">Click Delete.</span></span>
2. <span data-ttu-id="315fa-153">[はい] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="315fa-153">Click Yes.</span></span>
    * <span data-ttu-id="315fa-154">新しいテンプレートを追加します。</span><span class="sxs-lookup"><span data-stu-id="315fa-154">Add a new template.</span></span> <span data-ttu-id="315fa-155">前のサブタスクのステップを完了した場合、作成してローカルに保存した Word 文書を選択します。</span><span class="sxs-lookup"><span data-stu-id="315fa-155">If you competed the steps in the previous subtask, select the Word document that you prepared and saved locally.</span></span> <span data-ttu-id="315fa-156">そうでない場合、以前ダウンロードした SampleVendPaymDocReportBounded.docx MS Word テンプレートを選択します。</span><span class="sxs-lookup"><span data-stu-id="315fa-156">Otherwise, select the SampleVendPaymDocReportBounded.docx MS Word template that you downloaded earlier.</span></span>  
3. <span data-ttu-id="315fa-157">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="315fa-157">Click New.</span></span>
4. <span data-ttu-id="315fa-158">[ファイル] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="315fa-158">Click File.</span></span>
5. <span data-ttu-id="315fa-159">[参照] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="315fa-159">Click Browse.</span></span> <span data-ttu-id="315fa-160">以前ダウンロードした SampleVendPaymDocReportBounded.docx を参照して選択します。</span><span class="sxs-lookup"><span data-stu-id="315fa-160">Navigate to and select SampleVendPaymDocReportBounded.docx that you previously downloaded.</span></span> <span data-ttu-id="315fa-161">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="315fa-161">Click OK.</span></span>
6. <span data-ttu-id="315fa-162">[テンプレート] フィールドで、前のステップでダウンロードしたドキュメントを選択します。</span><span class="sxs-lookup"><span data-stu-id="315fa-162">In the Template field, select the document that you downloaded in the previous step.</span></span>
7. <span data-ttu-id="315fa-163">[保存] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="315fa-163">Click Save.</span></span>
8. <span data-ttu-id="315fa-164">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="315fa-164">Close the page.</span></span>

## <a name="execute-the-format-to-create-word-output"></a><span data-ttu-id="315fa-165">フォーマットを実行して Word 出力を作成する</span><span class="sxs-lookup"><span data-stu-id="315fa-165">Execute the format to create Word output</span></span>
1. <span data-ttu-id="315fa-166">アクション ウィンドウで、[設定] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="315fa-166">On the Action Pane, click Configurations.</span></span>
2. <span data-ttu-id="315fa-167">[ユーザー パラメーター] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="315fa-167">Click User parameters.</span></span>
3. <span data-ttu-id="315fa-168">[設定の実行] フィールドで、[はい] を選択します。</span><span class="sxs-lookup"><span data-stu-id="315fa-168">Select Yes in the Run settings field.</span></span>
4. <span data-ttu-id="315fa-169">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="315fa-169">Click OK.</span></span>
5. <span data-ttu-id="315fa-170">[編集] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="315fa-170">Click Edit.</span></span>
6. <span data-ttu-id="315fa-171">[ドラフトの実行] フィールドで、[はい] を選択します。</span><span class="sxs-lookup"><span data-stu-id="315fa-171">Select Yes in the Run Draft field.</span></span>
7. <span data-ttu-id="315fa-172">[保存] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="315fa-172">Click Save.</span></span>
8. <span data-ttu-id="315fa-173">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="315fa-173">Close the page.</span></span>
9. <span data-ttu-id="315fa-174">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="315fa-174">Close the page.</span></span>
10. <span data-ttu-id="315fa-175">[買掛金勘定] > [支払] > [支払仕訳帳] の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="315fa-175">Go to Accounts payable > Payments > Payment journal.</span></span>
11. <span data-ttu-id="315fa-176">[明細行] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="315fa-176">Click Lines.</span></span>
12. <span data-ttu-id="315fa-177">一覧で、すべての行のマークを設定または解除します。</span><span class="sxs-lookup"><span data-stu-id="315fa-177">In the list, mark or unmark all rows.</span></span>
13. <span data-ttu-id="315fa-178">[支払ステータス] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="315fa-178">Click Payment status.</span></span>
14. <span data-ttu-id="315fa-179">[なし] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="315fa-179">Click None.</span></span>
15. <span data-ttu-id="315fa-180">[支払の生成] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="315fa-180">Click Generate payments.</span></span>
16. <span data-ttu-id="315fa-181">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="315fa-181">Click OK.</span></span>
17. <span data-ttu-id="315fa-182">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="315fa-182">Click OK.</span></span>
    * <span data-ttu-id="315fa-183">生成された出力を解析します。</span><span class="sxs-lookup"><span data-stu-id="315fa-183">Analyze the generated output.</span></span> <span data-ttu-id="315fa-184">作成された出力が Word 形式で表示され、その出力に処理済みの支払の詳細が含まれます。</span><span class="sxs-lookup"><span data-stu-id="315fa-184">Note that the created output is presented in Word format and contains the details of the processed payments.</span></span>  


