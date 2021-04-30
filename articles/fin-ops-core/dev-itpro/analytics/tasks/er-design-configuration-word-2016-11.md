---
title: Excel テンプレートと ER 構成を再利用して Word 形式でレポートを生成
description: このトピックでは、Excel ブックとしてレポートを生成するように設計されたレポート形式で、Word ドキュメントとしてレポートを生成するように構成する方法について説明します。
author: NickSelin
ms.date: 01/11/2021
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: ERWorkspace, ERSolutionTable, EROperationDesigner, LedgerJournalTable, LedgerJournalTransVendPaym
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: ab4cd4a390782936a74977ac2aef3790aa8ac1af
ms.sourcegitcommit: 951393b05bf409333cb3c7ad977bcaa804aa801b
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/13/2021
ms.locfileid: "5891698"
---
# <a name="reuse-er-configurations-with-excel-templates-to-generate-reports-in-word-format"></a><span data-ttu-id="f53b5-103">Excel テンプレートと ER 構成を再利用して Word 形式でレポートを生成</span><span class="sxs-lookup"><span data-stu-id="f53b5-103">Reuse ER configurations with Excel templates to generate reports in Word format</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="f53b5-104">レポートを Microsoft Word ドキュメントとして生成するように、新しい [電子申告 (ER)](../general-electronic-reporting.md) [形式](../general-electronic-reporting.md#FormatComponentOutbound) を [構成](../er-design-configuration-word.md) することができます。</span><span class="sxs-lookup"><span data-stu-id="f53b5-104">To generate reports as Microsoft Word documents, you can [configure](../er-design-configuration-word.md) a new [Electronic reporting (ER)](../general-electronic-reporting.md) [format](../general-electronic-reporting.md#FormatComponentOutbound).</span></span> <span data-ttu-id="f53b5-105">または、最初に Excel ブックとしてレポートを生成するように設計された ER 形式を再利用できます。</span><span class="sxs-lookup"><span data-stu-id="f53b5-105">Alternatively, you can reuse an ER format that was originally designed to generate reports as Excel workbooks.</span></span> <span data-ttu-id="f53b5-106">この場合、Excel テンプレートを Word テンプレートに置き換える必要があります。</span><span class="sxs-lookup"><span data-stu-id="f53b5-106">In this case, you must replace the Excel template with a Word template.</span></span>

<span data-ttu-id="f53b5-107">次の手順は、システム管理者ロールまたは電子申告開発者ロールでユーザーが、レポートを Excel ファイルとして生成するように設計された ER 形式を再利用することで、Word ファイルとしてレポートを生成する ER 形式を構成する方法を示します。</span><span class="sxs-lookup"><span data-stu-id="f53b5-107">The following procedures show how a user in either the System administrator role or the Electronic reporting developer role can configure an ER format to generate reports as Word files by reusing an ER format that was designed to generate reports as Excel files.</span></span>

<span data-ttu-id="f53b5-108">GBSI 社を例に使用して、これらの手順について解説します。</span><span class="sxs-lookup"><span data-stu-id="f53b5-108">These procedures can be completed in the GBSI company.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="f53b5-109">必要条件</span><span class="sxs-lookup"><span data-stu-id="f53b5-109">Prerequisites</span></span>

<span data-ttu-id="f53b5-110">これらの手順を完了するには、まず [OPENXML 形式でレポートを生成する構成を設計する](er-design-reports-openxml-2016-11.md) タスク ガイドにある手順に従う必要があります。</span><span class="sxs-lookup"><span data-stu-id="f53b5-110">To complete these procedures, you must first follow the steps in the [Design a configuration for generating reports in OPENXML format](er-design-reports-openxml-2016-11.md) task guide.</span></span>

<span data-ttu-id="f53b5-111">また、サンプル レポート用に次のテンプレートをダウンロードしてローカルに保存する必要があります。</span><span class="sxs-lookup"><span data-stu-id="f53b5-111">You must also download and locally save the following templates for the sample report:</span></span>

- [<span data-ttu-id="f53b5-112">支払レポート (SampleVendPaymDocReport.docx) のテンプレート</span><span class="sxs-lookup"><span data-stu-id="f53b5-112">Template of Payment Report (SampleVendPaymDocReport.docx)</span></span>](https://go.microsoft.com/fwlink/?linkid=862266)
- [<span data-ttu-id="f53b5-113">支払レポート (SampleVendPaymDocReportBounded.docx) のバインドされたテンプレート</span><span class="sxs-lookup"><span data-stu-id="f53b5-113">Bounded Template of Payment Report (SampleVendPaymDocReportBounded.docx)</span></span>](https://go.microsoft.com/fwlink/?linkid=862266)

<span data-ttu-id="f53b5-114">これらの手順は、Dynamics 365 for Operations バージョン 1611 (2016年11月) で追加された機能に関するものです。</span><span class="sxs-lookup"><span data-stu-id="f53b5-114">These procedures are for a feature that was added in Dynamics 365 for Operations version 1611 (November 2016).</span></span>

## <a name="select-the-existing-er-report-configuration"></a><span data-ttu-id="f53b5-115">既存の ER レポート コンフィギュレーションを選択します</span><span class="sxs-lookup"><span data-stu-id="f53b5-115">Select the existing ER report configuration</span></span>

1. <span data-ttu-id="f53b5-116">Dynamics 365 Finance で、**組織管理** \> **ワークスペース** \> **電子申告** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="f53b5-116">In Dynamics 365 Finance, go to **Organization administration** \> **Workspaces** \> **Electronic reporting**.</span></span>
2. <span data-ttu-id="f53b5-117">**Litware, Inc.** 構成プロバイダーが **有効** として選択されていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="f53b5-117">Make sure that the **Litware, Inc.** configuration provider is selected as **Active**.</span></span> <span data-ttu-id="f53b5-118">有効になっていない場合は、[構成プロバイダーを作成して、有効としてマークする](er-configuration-provider-mark-it-active-2016-11.md) タスク ガイドにある手順に従います。</span><span class="sxs-lookup"><span data-stu-id="f53b5-118">If it isn't, follow the steps in the [Create configuration providers and mark them as active](er-configuration-provider-mark-it-active-2016-11.md) task guide.</span></span>
3. <span data-ttu-id="f53b5-119">**コンフィギュレーションをレポートする** を選択します。</span><span class="sxs-lookup"><span data-stu-id="f53b5-119">Select **Reporting configurations**.</span></span> <span data-ttu-id="f53b5-120">OPENXML 形式でレポート出力を生成するように設計された既存の ER 構成を再利用します。</span><span class="sxs-lookup"><span data-stu-id="f53b5-120">You will reuse the existing ER configuration that was designed to generate the report output in OPENXML format.</span></span>
4. <span data-ttu-id="f53b5-121">**構成** ページの左側ペインにある構成ツリーで、**支払モデル** を展開し、**サンプル ワークシート レポート** を選択します。</span><span class="sxs-lookup"><span data-stu-id="f53b5-121">On the **Configurations** page, in the configuration tree in the left pane, expand **Payment model**, and select **Sample worksheet report**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="f53b5-122">選択した ER 形式の下書きバージョンは、**バージョン** クイックタブで編集できます。</span><span class="sxs-lookup"><span data-stu-id="f53b5-122">The draft version of the selected ER format can be edited on the **Versions** FastTab.</span></span>

5. <span data-ttu-id="f53b5-123">**デザイナー** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="f53b5-123">Select **Designer**.</span></span>
6. <span data-ttu-id="f53b5-124">**形式デザイナー** ページで、ルート形式要素のタイトルが、Excel テンプレートが現在使用されていることを示していることに注意してください。</span><span class="sxs-lookup"><span data-stu-id="f53b5-124">On the **Format designer** page, notice that the title of the root format element indicates that an Excel template is currently used.</span></span>

![既存の構成の選択](../media/er-design-configuration-word-2016-11-image01.gif)

## <a name="review-the-downloaded-word-template"></a><span data-ttu-id="f53b5-126">ダウンロードした Word テンプレートの確認</span><span class="sxs-lookup"><span data-stu-id="f53b5-126">Review the downloaded Word template</span></span>

1. <span data-ttu-id="f53b5-127">Word デスクトップ アプリケーションで、先にダウンロードした **SampleVendPaymDocReport.docx** テンプレート ファイルを開きます。</span><span class="sxs-lookup"><span data-stu-id="f53b5-127">In the Word desktop application, open the **SampleVendPaymDocReport.docx** template file that you downloaded earlier.</span></span>
2. <span data-ttu-id="f53b5-128">テンプレートに、ER 出力として生成するドキュメントのレイアウトのみが含まれていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="f53b5-128">Verify that the template contains only the layout of the document that you want to generate as ER output.</span></span>

![デスクトップ アプリケーションの Word テンプレート レイアウト](../media/er-design-configuration-word-2016-11-image02.png)

## <a name="replace-the-excel-template-with-the-word-template-and-add-a-custom-xml-part"></a><span data-ttu-id="f53b5-130">Excel テンプレートを Word テンプレートに置き換え、カスタム XML パーツを追加する</span><span class="sxs-lookup"><span data-stu-id="f53b5-130">Replace the Excel template with the Word template and add a custom XML part</span></span>

<span data-ttu-id="f53b5-131">現在は、OPENXML 形式で出力を生成するテンプレートとして Excel ドキュメントが使用されます。</span><span class="sxs-lookup"><span data-stu-id="f53b5-131">Currently, the Excel document is used as a template to generate the output in OPENXML format.</span></span> <span data-ttu-id="f53b5-132">このテンプレートを、以前ダウンロードした SampleVendPaymDocReport.docx Word テンプレート ファイルに置き換えます。</span><span class="sxs-lookup"><span data-stu-id="f53b5-132">You will replace this template with the SampleVendPaymDocReport.docx Word template file that you downloaded earlier.</span></span> <span data-ttu-id="f53b5-133">また、カスタム XML パーツを追加して、Word テンプレートを拡張します。</span><span class="sxs-lookup"><span data-stu-id="f53b5-133">You will also extend the Word template by adding a custom XML part.</span></span>

1. <span data-ttu-id="f53b5-134">Finance の **形式デザイナー** ページにある **形式** タブで、**添付ファイル** を選択します。</span><span class="sxs-lookup"><span data-stu-id="f53b5-134">In Finance, on the **Format designer** page, on the **Format** tab, select **Attachments**.</span></span>
2. <span data-ttu-id="f53b5-135">**添付ファイル** ページで **削除** を選択して、既存の Excel テンプレートを削除します。</span><span class="sxs-lookup"><span data-stu-id="f53b5-135">On the **Attachments** page, select **Delete** to remove the existing Excel template.</span></span> <span data-ttu-id="f53b5-136">**はい** を選択して、変更を確認します。</span><span class="sxs-lookup"><span data-stu-id="f53b5-136">Select **Yes** to confirm the change.</span></span>
3. <span data-ttu-id="f53b5-137">**新規** \> **ファイル** を選択します。</span><span class="sxs-lookup"><span data-stu-id="f53b5-137">Select **New** \> **File**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="f53b5-138">ER パラメーターで [構成](../electronic-reporting-er-configure-parameters.md#parameters-to-manage-documents) されているドキュメント タイプを選択して、ER 形式テンプレートを保存する必要があります。</span><span class="sxs-lookup"><span data-stu-id="f53b5-138">You must select a document type that has been [configured](../electronic-reporting-er-configure-parameters.md#parameters-to-manage-documents) in the ER parameters to store templates of ER formats.</span></span>

4. <span data-ttu-id="f53b5-139">**参照** を選択し、先にダウンロードした **SampleVendPaymDocReport.docx** ファイルを参照して選択します。</span><span class="sxs-lookup"><span data-stu-id="f53b5-139">Select **Browse**, and then browse to and select the **SampleVendPaymDocReport.docx** file that you downloaded earlier.</span></span>
5. <span data-ttu-id="f53b5-140">**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="f53b5-140">Select **OK**.</span></span>
6. <span data-ttu-id="f53b5-141">**添付ファイル** ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="f53b5-141">Close the **Attachments** page.</span></span>
7. <span data-ttu-id="f53b5-142">**形式デザイナー** ページの **テンプレート** フィールドで、以前に使用した Excel テンプレートの代わりに、その Word テンプレートを使用する **SampleVendPaymDocReport.docx** ファイルを入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="f53b5-142">On the **Format designer** page, in the **Template** field, enter or select the **SampleVendPaymDocReport.docx** file to use that Word template instead of the Excel template that was previously used.</span></span>
8. <span data-ttu-id="f53b5-143">**保存** を選択します。</span><span class="sxs-lookup"><span data-stu-id="f53b5-143">Select **Save**.</span></span>

    <span data-ttu-id="f53b5-144">**保存** アクションは、構成の変更を保存することに加えて、添付された Word テンプレートを更新します。</span><span class="sxs-lookup"><span data-stu-id="f53b5-144">In addition to storing configuration changes, the **Save** action updates the attached Word template.</span></span> <span data-ttu-id="f53b5-145">設計されたフォーマットの階層構造は、**レポート** という名前の新しいカスタム XML パーツとして、添付の Word ドキュメントに追加されます。</span><span class="sxs-lookup"><span data-stu-id="f53b5-145">The hierarchical structure of the designed format is added to the attached Word document as a new custom XML part that is named **Report**.</span></span> <span data-ttu-id="f53b5-146">添付された Word テンプレートには、ER 出力として生成されるドキュメントのレイアウトと、実行時に ER がそのテンプレートに入力するデータの構造が含まれます。</span><span class="sxs-lookup"><span data-stu-id="f53b5-146">The attached Word template contains the layout of the document that will be generated as ER output and the structure of data that ER will enter in that template at runtime.</span></span>

9. <span data-ttu-id="f53b5-147">ルート形式要素のタイトルが、Word テンプレートが現在使用されていることを示していることに注意してください。</span><span class="sxs-lookup"><span data-stu-id="f53b5-147">Notice that the title of the root format element indicates that a Word template is currently used.</span></span>

    ![Excel テンプレートを Word テンプレートに置き換え、カスタム XML パーツを追加する](../media/er-design-configuration-word-2016-11-image03.gif)

10. <span data-ttu-id="f53b5-149">**形式** タブで、**添付ファイル** を選択します。</span><span class="sxs-lookup"><span data-stu-id="f53b5-149">On the **Format** tab, select **Attachments**.</span></span>

<span data-ttu-id="f53b5-150">**レポート** カスタム XML パーツの要素を Word ドキュメントのコンテンツ コントロールにマップできるようになりました。</span><span class="sxs-lookup"><span data-stu-id="f53b5-150">You can now map the elements of the **Report** custom XML part to the content controls of the Word document.</span></span>

<span data-ttu-id="f53b5-151">[カスタム XML パーツ](/visualstudio/vsto/custom-xml-parts-overview?view=vs-2019) の要素にマップされた [コンテンツ コントロール](/office/client-developer/word/content-controls-in-word) を含む形式として Word ドキュメントを設計するプロセスに精通している場合は、次の手順にあるすべてのステップを実行して、ドキュメントを作成します。</span><span class="sxs-lookup"><span data-stu-id="f53b5-151">If you're familiar with the process of designing Word documents as forms that contain [content controls](/office/client-developer/word/content-controls-in-word) that are mapped to elements of [custom XML parts](/visualstudio/vsto/custom-xml-parts-overview?view=vs-2019), complete all steps in the next procedure to create the document.</span></span> <span data-ttu-id="f53b5-152">詳細については、[ユーザーが入力または印刷するフォームを Word で作成](https://support.office.com/article/Create-forms-that-users-complete-or-print-in-Word-040c5cc1-e309-445b-94ac-542f732c8c8b) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="f53b5-152">For more information, see [Create forms that users complete or print in Words](https://support.office.com/article/Create-forms-that-users-complete-or-print-in-Word-040c5cc1-e309-445b-94ac-542f732c8c8b).</span></span> <span data-ttu-id="f53b5-153">それ以外の場合、次の手順をスキップします。</span><span class="sxs-lookup"><span data-stu-id="f53b5-153">Otherwise, skip the next procedure.</span></span>

## <a name="get-a-word-document-that-has-a-custom-xml-part-and-do-data-mapping"></a><a id='get-word-doc'></a><span data-ttu-id="f53b5-154">カスタム XML パーツを含む Word ドキュメントの取得とデータ マッピングの実行</span><span class="sxs-lookup"><span data-stu-id="f53b5-154">Get a Word document that has a custom XML part and do data mapping</span></span>

1. <span data-ttu-id="f53b5-155">Finance の **添付ファイル** ページで **開く** を選択し、Finance から選択したテンプレートをダウンロードして、ローカルで Word ドキュメントとして保存します。</span><span class="sxs-lookup"><span data-stu-id="f53b5-155">In Finance, on the **Attachments** page, select **Open** to download the selected template from Finance and store it locally as a Word document.</span></span>
3. <span data-ttu-id="f53b5-156">Word デスクトップ アプリケーションで、ダウンロードしたドキュメントを開きます。</span><span class="sxs-lookup"><span data-stu-id="f53b5-156">In the Word desktop application, open the document that you just downloaded.</span></span>
4. <span data-ttu-id="f53b5-157">**開発者** タブで、**XML マッピング ウィンドウ** を選択します。</span><span class="sxs-lookup"><span data-stu-id="f53b5-157">On the **Developer** tab, select **XML Mapping Pane**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="f53b5-158">**開発者** タブがリボンに表示されない場合は、リボンをカスタマイズして追加します。</span><span class="sxs-lookup"><span data-stu-id="f53b5-158">If the **Developer** tab doesn't appear on the ribbon, customize the ribbon to add it.</span></span>

5. <span data-ttu-id="f53b5-159">**XML マッピング** ウィンドウの **カスタム XML パーツ** フィールドで、**レポート** カスタム XML パーツを選択します。</span><span class="sxs-lookup"><span data-stu-id="f53b5-159">In the **XML Mapping** pane, in the **Custom XML Part** field, select the **Report** custom XML part.</span></span>
6. <span data-ttu-id="f53b5-160">選択した **レポート** カスタム XML パーツの要素と Word ドキュメントのコンテンツ コントロールをマップします。</span><span class="sxs-lookup"><span data-stu-id="f53b5-160">Map the elements of the selected **Report** custom XML part and the content controls of the Word document.</span></span>
7. <span data-ttu-id="f53b5-161">更新された Word ドキュメントを **SampleVendPaymDocReportBounded.docx** としてローカルに保存します。</span><span class="sxs-lookup"><span data-stu-id="f53b5-161">Save the updated Word document locally as **SampleVendPaymDocReportBounded.docx**.</span></span>

## <a name="review-the-word-template-where-the-custom-xml-part-is-mapped-to-content-controls"></a><span data-ttu-id="f53b5-162">カスタム XML パーツがコンテンツ コントロールにマップされている Word テンプレートを確認</span><span class="sxs-lookup"><span data-stu-id="f53b5-162">Review the Word template where the custom XML part is mapped to content controls</span></span>

1. <span data-ttu-id="f53b5-163">Word デスクトップ アプリケーションで、**SampleVendPaymDocReportBounded.docx** テンプレート ファイルを開きます。</span><span class="sxs-lookup"><span data-stu-id="f53b5-163">In the Word desktop application, open the **SampleVendPaymDocReportBounded.docx** template file.</span></span>
2. <span data-ttu-id="f53b5-164">テンプレートに、ER 出力として生成するドキュメントのレイアウトが含まれていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="f53b5-164">Verify that the template contains the layout of the document that you want to generate as ER output.</span></span> <span data-ttu-id="f53b5-165">このテンプレートで実行時に ER が入力するデータのプレースホルダーとして使用されるコンテンツ コントロールは、**レポート** カスタム XML パーツの要素と Word ドキュメントのコンテンツ コントロールの間で構成されるマッピングに基づきます。</span><span class="sxs-lookup"><span data-stu-id="f53b5-165">The content controls that are used as placeholders for data that ER will enter in this template at runtime are based on the mappings that are configured between elements of the **Report** custom XML part and the content controls of the Word document.</span></span>

![デスクトップ アプリケーションの Word テンプレート プレビュー](../media/er-design-configuration-word-2016-11-image04.png)

## <a name="upload-the-word-template-where-the-custom-xml-part-is-mapped-to-content-controls"></a><span data-ttu-id="f53b5-167">カスタム XML パーツがコンテンツ コントロールにマップされている Word テンプレートを更新</span><span class="sxs-lookup"><span data-stu-id="f53b5-167">Upload the Word template where the custom XML part is mapped to content controls</span></span>

1. <span data-ttu-id="f53b5-168">Finance の **添付ファイル** ページで、**削除** を選択して、**レポート** カスタム XML パーツの要素とコンテンツ コントロールの間にマッピングがない Word テンプレート を削除します。</span><span class="sxs-lookup"><span data-stu-id="f53b5-168">In Finance, on the **Attachments** page, select **Delete** to remove the Word template that has no mappings between elements of the **Report** custom XML part and content controls.</span></span> <span data-ttu-id="f53b5-169">**はい** を選択して、変更を確認します。</span><span class="sxs-lookup"><span data-stu-id="f53b5-169">Select **Yes** to confirm the change.</span></span>
2. <span data-ttu-id="f53b5-170">**新規** \> **ファイル** を選択し、**レポート** カスタム XML パーツの要素とコンテンツ コントロールの間のマッピングを含む新しいテンプレート ファイルを追加します。</span><span class="sxs-lookup"><span data-stu-id="f53b5-170">Select **New** \> **File** to add a new template file that contains mappings between elements of the **Report** custom XML part and content controls.</span></span>

    > [!NOTE]
    > <span data-ttu-id="f53b5-171">ER パラメーターで [構成](../electronic-reporting-er-configure-parameters.md#parameters-to-manage-documents) されているドキュメント タイプを選択して、ER 形式テンプレートを保存する必要があります。</span><span class="sxs-lookup"><span data-stu-id="f53b5-171">You must select a document type that has been [configured](../electronic-reporting-er-configure-parameters.md#parameters-to-manage-documents) in the ER parameters to store templates of ER formats.</span></span>

3. <span data-ttu-id="f53b5-172">**参照** を選択し、[カスタム XML パーツを含む Word の取得とデータ マッピングの実行](#get-word-doc) セクションで手順を実行して、ダウンロードまたは準備した **SampleVendPaymDocReportBounded.docx** ファイルを参照して選択します。</span><span class="sxs-lookup"><span data-stu-id="f53b5-172">Select **Browse**, and then browse to and select the **SampleVendPaymDocReportBounded.docx** file that you downloaded or prepared by completing the procedure in the [Get a Word that has a custom XML part to do data mapping](#get-word-doc) section.</span></span>
4. <span data-ttu-id="f53b5-173">**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="f53b5-173">Select **OK**.</span></span>
5. <span data-ttu-id="f53b5-174">**添付ファイル** ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="f53b5-174">Close the **Attachments** page.</span></span>
6. <span data-ttu-id="f53b5-175">**形式デザイナー** ページの **テンプレート** フィールドで、ダウンロードしたドキュメントを選択します。</span><span class="sxs-lookup"><span data-stu-id="f53b5-175">On the **Format designer** page, in the **Template** field, select the document that you just downloaded.</span></span>
7. <span data-ttu-id="f53b5-176">**保存** を選択します。</span><span class="sxs-lookup"><span data-stu-id="f53b5-176">Select **Save**.</span></span>
8. <span data-ttu-id="f53b5-177">**形式デザイナー** ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="f53b5-177">Close the **Format designer** page.</span></span>

## <a name="mark-the-configured-format-as-runnable"></a><span data-ttu-id="f53b5-178">構成された形式を実行可能としてマーク</span><span class="sxs-lookup"><span data-stu-id="f53b5-178">Mark the configured format as runnable</span></span>

<span data-ttu-id="f53b5-179">編集可能な形式の下書きバージョンを実行するには、[実行可能](../er-quick-start2-customize-report.md#MarkFormatRunnable) にする必要があります。</span><span class="sxs-lookup"><span data-stu-id="f53b5-179">To run the draft version of the editable format, you must make it [runnable](../er-quick-start2-customize-report.md#MarkFormatRunnable).</span></span>

1. <span data-ttu-id="f53b5-180">Finance の **構成** ページにあるアクション ペインの **構成** タブの **詳細設定** グループで、**ユーザー パラメーター** を選択します。</span><span class="sxs-lookup"><span data-stu-id="f53b5-180">In Finance, on the **Configurations** page, on the Action Pane, on the **Configurations** tab, in the **Advanced settings** group, select **User parameters**.</span></span>
2. <span data-ttu-id="f53b5-181">**ユーザー パラメーター** ダイアログ ボックスで、**実行設定** オプションを **はい** に設定し、**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="f53b5-181">In the **User parameters** dialog box, set the **Run settings** option to **Yes**, and then select **OK**.</span></span>
3. <span data-ttu-id="f53b5-182">**編集** を選択し、必要に応じて現在のページを編集可能にします。</span><span class="sxs-lookup"><span data-stu-id="f53b5-182">Select **Edit** to make the current page editable, as required.</span></span>
4. <span data-ttu-id="f53b5-183">現在選択されている **サンプル ワークシート レポート** 構成について、**ドラフトの実行** オプションを **はい** に 設定します。</span><span class="sxs-lookup"><span data-stu-id="f53b5-183">For the currently selected **Sample worksheet report** configuration, set the **Run Draft** option to **Yes**.</span></span>
5. <span data-ttu-id="f53b5-184">**保存** を選択します。</span><span class="sxs-lookup"><span data-stu-id="f53b5-184">Select **Save**.</span></span>

## <a name="run-the-format-to-create-output-in-word-format"></a><span data-ttu-id="f53b5-185">Word 形式で出力を作成するための形式の実行</span><span class="sxs-lookup"><span data-stu-id="f53b5-185">Run the format to create output in Word format</span></span>

1. <span data-ttu-id="f53b5-186">Finance で **買掛金勘定** \> **支払** \> **支払仕訳帳** に移動します。</span><span class="sxs-lookup"><span data-stu-id="f53b5-186">In Finance, go to **Accounts payable** \> **Payments** \> **Payment journal**.</span></span>
2. <span data-ttu-id="f53b5-187">先に入力した支払仕訳帳で、**明細行** を選択します。</span><span class="sxs-lookup"><span data-stu-id="f53b5-187">In a payment journal that you entered earlier, select **Lines**.</span></span>
3. <span data-ttu-id="f53b5-188">**仕入先支払** ページ で、グリッド内のすべての行を選択します。</span><span class="sxs-lookup"><span data-stu-id="f53b5-188">On the **Vendor payments** page, select all rows in the grid.</span></span>
4. <span data-ttu-id="f53b5-189">**支払ステータス** \> **なし** を選択します。</span><span class="sxs-lookup"><span data-stu-id="f53b5-189">Select **Payment status** \> **None**.</span></span>

    ![仕入先支払ページでの処理に対する支払](../media/er-design-configuration-word-2016-11-image05.png)

5. <span data-ttu-id="f53b5-191">アクション ペインで **支払の生成** を選択します。</span><span class="sxs-lookup"><span data-stu-id="f53b5-191">On the Action Pane, select **Generate payments**.</span></span>
6. <span data-ttu-id="f53b5-192">表示されるダイアログ ボックスで、次の手順に従います:</span><span class="sxs-lookup"><span data-stu-id="f53b5-192">In the dialog box that appears, follow these steps:</span></span>

    1. <span data-ttu-id="f53b5-193">**支払方法** フィールドで、**電子** を選択します。</span><span class="sxs-lookup"><span data-stu-id="f53b5-193">In the **Method of payment** field, select **Electronic**.</span></span>
    2. <span data-ttu-id="f53b5-194">**銀行口座** フィールドで、 **GBSI OPER** を選択します。</span><span class="sxs-lookup"><span data-stu-id="f53b5-194">In the **Bank account** field, select **GBSI OPER**.</span></span>
    3. <span data-ttu-id="f53b5-195">**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="f53b5-195">Select **OK**.</span></span>

7. <span data-ttu-id="f53b5-196">**電子レポート パラメーター** ダイアログ ボックスで、**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="f53b5-196">In the **Electronic report parameters** dialog box, select **OK**.</span></span>
8. <span data-ttu-id="f53b5-197">作成された出力は、Word 形式で表示され、処理済みの支払の詳細が含まれます。</span><span class="sxs-lookup"><span data-stu-id="f53b5-197">The generated output is presented in Word format and contains the details of the processed payments.</span></span> <span data-ttu-id="f53b5-198">生成された出力を解析します。</span><span class="sxs-lookup"><span data-stu-id="f53b5-198">Analyze the generated output.</span></span>

    ![Word 形式で生成された出力](../media/er-design-configuration-word-2016-11-image06.png)

## <a name="additional-resources"></a><span data-ttu-id="f53b5-200">追加リソース</span><span class="sxs-lookup"><span data-stu-id="f53b5-200">Additional resources</span></span>

- [<span data-ttu-id="f53b5-201">Word 形式でレポートを生成するための新しい ER 構成を設計する</span><span class="sxs-lookup"><span data-stu-id="f53b5-201">Design a new ER configuration to generate reports in Word format</span></span>](../er-design-configuration-word.md)
- [<span data-ttu-id="f53b5-202">ER を使用して生成されるドキュメントへの画像や図形の埋め込み</span><span class="sxs-lookup"><span data-stu-id="f53b5-202">Embed images and shapes in documents that you generate by using ER</span></span>](../electronic-reporting-embed-images-shapes.md#embed-an-image-in-a-word-document)


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]