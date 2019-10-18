---
title: Excel テンプレートの再適用による形式の変更
description: この手順にあるステップを完了するには、まず「ER - OPENXML 形式でレポートを生成するコンフィギュレーションの設計」の手順を完了する必要があります。
author: NickSelin
manager: AnnBe
ms.date: 06/19/2017
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 73f2c10d7462c4b52a2b36dd5f221593707d2f4f
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/27/2019
ms.locfileid: "2184672"
---
# <a name="modify-formats-by-reapplying-excel-templates"></a><span data-ttu-id="2e99c-103">Excel テンプレートの再適用による形式の変更</span><span class="sxs-lookup"><span data-stu-id="2e99c-103">Modify formats by reapplying Excel templates</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="2e99c-104">この手順にあるステップを完了するには、まず「ER - OPENXML 形式でレポートを生成するコンフィギュレーションの設計」の手順を完了する必要があります。</span><span class="sxs-lookup"><span data-stu-id="2e99c-104">To complete the steps in this procedure, you must first complete the procedure, ER - Design a configuration for generating reports in OPENXML format.</span></span>

<span data-ttu-id="2e99c-105">この手順では、変更された Microsoft Excel テンプレートの更新を再適用して、電子申告 (ER) 形式コンフィギュレーションを変更する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="2e99c-105">This procedure explains how to modify an Electronic reporting (ER) format configuration by reapplying a Microsoft Excel template that has been modified.</span></span> <span data-ttu-id="2e99c-106">この手順では、サンプル会社 Litware, Inc. 用に作成した ER 形式コンフィギュレーションへ変更した Excel テンプレートをインポートし、電子ドキュメントを生成します。</span><span class="sxs-lookup"><span data-stu-id="2e99c-106">In this procedure, you will import a modified Excel template into ER format configurations that have been created for the sample company, Litware, Inc., and then generate electronic documents.</span></span> <span data-ttu-id="2e99c-107">この手順は、「システム管理者」または「電子レポート開発者」ロールを持つユーザーを対象としています。</span><span class="sxs-lookup"><span data-stu-id="2e99c-107">This procedure is intended for users who have the system administrator or electronic reporting developer role.</span></span> <span data-ttu-id="2e99c-108">これらのステップは、GBSI データ セットを使用して完了することができます。</span><span class="sxs-lookup"><span data-stu-id="2e99c-108">These steps can be completed by using the GBSI dataset.</span></span> <span data-ttu-id="2e99c-109">開始する前に、ヘルプトピック「Excel テンプレートを再適用して電子申告形式を変更」 (modify-electronic-reporting-format-reapply-excel-template/) 内で一覧表示されている SampleVendPaymWsReport2.xlsx ファイルをダウンロードして保存します。</span><span class="sxs-lookup"><span data-stu-id="2e99c-109">Before you begin, download and save the file, SampleVendPaymWsReport2.xlsx, which is listed in the Help topic, Modify Electronic reporting format by reapplying an Excel template (modify-electronic-reporting-format-reapply-excel-template/).</span></span>

1. <span data-ttu-id="2e99c-110">[組織管理] > [ワークスペース] > [電子申告] の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="2e99c-110">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
    * <span data-ttu-id="2e99c-111">サンプル会社 Litware, Inc. のコンフィギュレーション プロバイダーが使用可能であり、アクティブとしてマークされていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="2e99c-111">Make sure that the configuration provider for the sample company, Litware, Inc., is available and marked as Active.</span></span> <span data-ttu-id="2e99c-112">このコンフィギュレーション プロバイダーが表示されない場合は、「コンフィギュレーション プロバイダーの作成および有効なプロバイダーとしてのマーク付け」という手順のステップを完了する必要があります。</span><span class="sxs-lookup"><span data-stu-id="2e99c-112">If you don’t see this configuration provider, complete the steps in the procedure, Create a configuration provider and mark it as active.</span></span>  

## <a name="select-the-er-format"></a><span data-ttu-id="2e99c-113">ER 形式を選択する</span><span class="sxs-lookup"><span data-stu-id="2e99c-113">Select the ER format</span></span>
1. <span data-ttu-id="2e99c-114">[コンフィギュレーションをレポートする] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="2e99c-114">Click Reporting configurations.</span></span>
2. <span data-ttu-id="2e99c-115">ツリーで、「Payment model」を展開します。</span><span class="sxs-lookup"><span data-stu-id="2e99c-115">In the tree, expand 'Payment model'.</span></span>
3. <span data-ttu-id="2e99c-116">ツリーで、「Payment model\Sample worksheet report」を選択します。</span><span class="sxs-lookup"><span data-stu-id="2e99c-116">In the tree, select 'Payment model\Sample worksheet report'.</span></span>
4. <span data-ttu-id="2e99c-117">[添付ファイル] クリックします。</span><span class="sxs-lookup"><span data-stu-id="2e99c-117">Click Attachments.</span></span>
    * <span data-ttu-id="2e99c-118">SampleVendPaymWsReport.xlsx Excel ファイルが、支払仕訳処理のテンプレートとして現在使用されていることに注意してください。</span><span class="sxs-lookup"><span data-stu-id="2e99c-118">Note that the SampleVendPaymWsReport.xlsx Excel file is currently used as a template for payment journal processing.</span></span>   
5. <span data-ttu-id="2e99c-119">[開く] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="2e99c-119">Click Open.</span></span>
    * <span data-ttu-id="2e99c-120">[開く] をクリックして Excel テンプレートのレイアウトを検証します。</span><span class="sxs-lookup"><span data-stu-id="2e99c-120">Click Open to explore the layout of the Excel template.</span></span>  
    * <span data-ttu-id="2e99c-121">テンプレートを確認します。</span><span class="sxs-lookup"><span data-stu-id="2e99c-121">Review the template.</span></span> <span data-ttu-id="2e99c-122">各支払い明細行には、現在以下の詳細が含まれていることに注意してください。仕入先勘定番号、仕入先の名前、銀行、支店コード、口座番号、借方、貸方、および通貨。</span><span class="sxs-lookup"><span data-stu-id="2e99c-122">Note that it currently includes the following details for each payment line: vendor account number, vendor name, bank, routing number, account number, debit, credit, and currency.</span></span> <span data-ttu-id="2e99c-123">この例では、支払日についての詳細を追加することで、この一覧を拡張します。</span><span class="sxs-lookup"><span data-stu-id="2e99c-123">For this example, we want to extend this list by adding details about the payment date.</span></span>   
6. <span data-ttu-id="2e99c-124">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="2e99c-124">Close the page.</span></span>

## <a name="reapply-a-new-excel-template-to-er-format"></a><span data-ttu-id="2e99c-125">ER 形式に新しい Excel テンプレートを再適用する</span><span class="sxs-lookup"><span data-stu-id="2e99c-125">Reapply a new Excel template to ER format</span></span>
1. <span data-ttu-id="2e99c-126">[デザイナー] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="2e99c-126">Click Designer.</span></span>
    * <span data-ttu-id="2e99c-127">編集用に、選択した ER 形式のドラフト バージョンを開きます。</span><span class="sxs-lookup"><span data-stu-id="2e99c-127">Open the draft version of the selected ER format for editing.</span></span>  
2. <span data-ttu-id="2e99c-128">アクション ウィンドウで、[インポート] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="2e99c-128">On the Action Pane, click Import.</span></span>
3. <span data-ttu-id="2e99c-129">[Excel からの更新] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="2e99c-129">Click Update from Excel.</span></span>
    * <span data-ttu-id="2e99c-130">[テンプレートの更新] をクリックし、SampleVendPaymWsReport2.xlsx というファイルを選択します。</span><span class="sxs-lookup"><span data-stu-id="2e99c-130">Click ‘Update template’, and then select the file, SampleVendPaymWsReport2.xlsx.</span></span>  
    * <span data-ttu-id="2e99c-131">[テンプレートの更新] をクリックし、以前にダウンロードした SampleVendPaymWsReport2.xlsx ファイルを参照して取得します。</span><span class="sxs-lookup"><span data-stu-id="2e99c-131">Click Update template and browse to get the downloaded earlier SampleVendPaymWsReport2.xlsx file.</span></span>  
4. <span data-ttu-id="2e99c-132">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="2e99c-132">Click OK.</span></span>
    * <span data-ttu-id="2e99c-133">SampleVendPaymWsReport2.xlsx テンプレートが適用されます。</span><span class="sxs-lookup"><span data-stu-id="2e99c-133">The SampleVendPaymWsReport2.xlsx template is applied.</span></span> <span data-ttu-id="2e99c-134">ER 形式の構造は、要素を ER 形式に追加してあるテンプレートのコンテンツと同期します。</span><span class="sxs-lookup"><span data-stu-id="2e99c-134">The structure of the ER format is synchronized with the content of the template, whose elements are added to the ER format.</span></span> <span data-ttu-id="2e99c-135">テンプレートに含まれていない ER 形式の既存の要素は、形式定義から削除されます。</span><span class="sxs-lookup"><span data-stu-id="2e99c-135">Any existing elements in the ER format that aren’t included in the template are removed from the format definition.</span></span>  
5. <span data-ttu-id="2e99c-136">ツリーで、「Excel」を選択します。</span><span class="sxs-lookup"><span data-stu-id="2e99c-136">In the tree, select 'Excel'.</span></span>
    * <span data-ttu-id="2e99c-137">[テンプレート] フィールドに新しいテンプレートへの参照が含まれたことに注意してください。</span><span class="sxs-lookup"><span data-stu-id="2e99c-137">Note that the Template field now contains a reference to the new template.</span></span>   
6. <span data-ttu-id="2e99c-138">[添付ファイル] クリックします。</span><span class="sxs-lookup"><span data-stu-id="2e99c-138">Click Attachments.</span></span>
7. <span data-ttu-id="2e99c-139">[開く] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="2e99c-139">Click Open.</span></span>
    * <span data-ttu-id="2e99c-140">[開く] をクリックして変更された Excel テンプレートのレイアウトを検証します。</span><span class="sxs-lookup"><span data-stu-id="2e99c-140">Click Open to explore the layout of the modified Excel template.</span></span>  
    * <span data-ttu-id="2e99c-141">テンプレートを確認します。</span><span class="sxs-lookup"><span data-stu-id="2e99c-141">Review the template.</span></span> <span data-ttu-id="2e99c-142">支払日の明細行が含まれたことに注意してください。</span><span class="sxs-lookup"><span data-stu-id="2e99c-142">Note that it now contains a line for the payment date.</span></span>   
8. <span data-ttu-id="2e99c-143">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="2e99c-143">Close the page.</span></span>
9. <span data-ttu-id="2e99c-144">ツリーで、「Excel」を展開します。</span><span class="sxs-lookup"><span data-stu-id="2e99c-144">In the tree, expand 'Excel'.</span></span>
10. <span data-ttu-id="2e99c-145">ツリーで、「Excel\PaymLines」を展開します。</span><span class="sxs-lookup"><span data-stu-id="2e99c-145">In the tree, expand 'Excel\PaymLines'.</span></span>
11. <span data-ttu-id="2e99c-146">ツリーで、「Excel\PaymLines\PaymDate」を選択します。</span><span class="sxs-lookup"><span data-stu-id="2e99c-146">In the tree, select 'Excel\PaymLines\PaymDate'.</span></span>
    * <span data-ttu-id="2e99c-147">ER 形式にもう 1 つの項目が含まれたことに注意してください。</span><span class="sxs-lookup"><span data-stu-id="2e99c-147">Note that the ER format now contains one more item.</span></span> <span data-ttu-id="2e99c-148">PaymDate というセルが Excel テンプレートに追加されています。</span><span class="sxs-lookup"><span data-stu-id="2e99c-148">A cell, PaymDate, has been added to the Excel template.</span></span>  
12. <span data-ttu-id="2e99c-149">[マッピング] タブをクリックします。</span><span class="sxs-lookup"><span data-stu-id="2e99c-149">Click the Mapping tab.</span></span>
13. <span data-ttu-id="2e99c-150">ツリーで、「model」を展開します。</span><span class="sxs-lookup"><span data-stu-id="2e99c-150">In the tree, expand 'model'.</span></span>
14. <span data-ttu-id="2e99c-151">ツリーで、[model\Payments] を展開します。</span><span class="sxs-lookup"><span data-stu-id="2e99c-151">In the tree, expand 'model\Payments'.</span></span>
15. <span data-ttu-id="2e99c-152">ツリーで、[model\Payments\Transaction date(TransactionDate)] を選択します。</span><span class="sxs-lookup"><span data-stu-id="2e99c-152">In the tree, select 'model\Payments\Transaction date(TransactionDate)'.</span></span>
16. <span data-ttu-id="2e99c-153">[バインド] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="2e99c-153">Click Bind.</span></span>
    * <span data-ttu-id="2e99c-154">実行時に新しいセルに追加するデータを指定します。</span><span class="sxs-lookup"><span data-stu-id="2e99c-154">Specify what data is added to the new cell at runtime.</span></span>  
17. <span data-ttu-id="2e99c-155">[保存] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="2e99c-155">Click Save.</span></span>
18. <span data-ttu-id="2e99c-156">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="2e99c-156">Close the page.</span></span>

## <a name="enable-the-modified-draft-version-of-the-er-format-for-use-in-payment-journal-processing"></a><span data-ttu-id="2e99c-157">支払仕訳処理で使用するために ER 形式の変更されたドラフト バージョンを有効にする</span><span class="sxs-lookup"><span data-stu-id="2e99c-157">Enable the modified draft version of the ER format for use in payment journal processing</span></span>
1. <span data-ttu-id="2e99c-158">アクション ウィンドウで、[設定] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="2e99c-158">On the Action Pane, click Configurations.</span></span>
2. <span data-ttu-id="2e99c-159">[ユーザー パラメーター] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="2e99c-159">Click User parameters.</span></span>
3. <span data-ttu-id="2e99c-160">[設定の実行] フィールドで、[はい] を選択します。</span><span class="sxs-lookup"><span data-stu-id="2e99c-160">Select Yes in the Run settings field.</span></span>
4. <span data-ttu-id="2e99c-161">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="2e99c-161">Click OK.</span></span>
5. <span data-ttu-id="2e99c-162">[編集] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="2e99c-162">Click Edit.</span></span>
6. <span data-ttu-id="2e99c-163">[ドラフトの実行] フィールドで、[はい] を選択します。</span><span class="sxs-lookup"><span data-stu-id="2e99c-163">Select Yes in the Run Draft field.</span></span>

## <a name="use-the-modified-draft-version-of-the-er-format-for-payment-journal-processing"></a><span data-ttu-id="2e99c-164">支払仕訳処理に ER 形式の変更されたドラフト バージョンを使用する</span><span class="sxs-lookup"><span data-stu-id="2e99c-164">Use the modified draft version of the ER format for payment journal processing</span></span>
    * <span data-ttu-id="2e99c-165">支払日という支払い明細行の新しい詳細を含む、作成したワークシートを確認します。</span><span class="sxs-lookup"><span data-stu-id="2e99c-165">Review the created worksheet, including new detail of payment lines – payment date.</span></span>  

