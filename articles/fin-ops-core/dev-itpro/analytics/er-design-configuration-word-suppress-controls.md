---
title: 生成されたレポートの Word コンテンツ コントロールを非表示にする
description: このトピックでは、コンテンツ コントロールが非表示の Microsoft Word ファイルとしてレポートを生成する電子申告 (ER) 形式の構成方法について説明します。
author: NickSelin
ms.date: 02/11/2021
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: ERWorkspace, ERSolutionTable, EROperationDesigner,  LedgerJournalTable, LedgerJournalTransVendPaym
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2020-01-01
ms.dyn365.ops.version: Version 10.0.6
ms.openlocfilehash: 8c99203110cfdc7f8123c30488611d55f48e8f67
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/31/2021
ms.locfileid: "5753604"
---
# <a name="suppress-word-content-controls-in-generated-reports"></a><span data-ttu-id="a9dfb-103">生成されたレポートの Word コンテンツ コントロールを非表示にする</span><span class="sxs-lookup"><span data-stu-id="a9dfb-103">Suppress Word content controls in generated reports</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="a9dfb-104">Microsoft Word ドキュメントとしてレポートを生成するには、レポートのテンプレートを Word ドキュメントとしてデザインする必要があります。</span><span class="sxs-lookup"><span data-stu-id="a9dfb-104">To generate reports as Microsoft Word documents, you must design a template for the reports as a Word document.</span></span> <span data-ttu-id="a9dfb-105">このテンプレートには、ランタイムに入力されるデータのプレースホルダーとして Word コンテンツ コントロールを含む必要があります。</span><span class="sxs-lookup"><span data-stu-id="a9dfb-105">This template must contain Word content controls as placeholders for data that will be filled in at runtime.</span></span> <span data-ttu-id="a9dfb-106">レポートのテンプレートとして作成された Word ドキュメントを使用するには、新しい[電子申告 (ER)](general-electronic-reporting.md) [ソリューション](er-quick-start1-new-solution.md) を[構成](er-design-configuration-word.md) できます。</span><span class="sxs-lookup"><span data-stu-id="a9dfb-106">To use the Word document that is created as a template for your reports, you can [configure](er-design-configuration-word.md) a new [Electronic reporting (ER)](general-electronic-reporting.md) [solution](er-quick-start1-new-solution.md).</span></span> <span data-ttu-id="a9dfb-107">ソリューションには、ER [形式](general-electronic-reporting.md#FormatComponentOutbound) コンポーネントを含む ER [構成](general-electronic-reporting.md#Configuration) を含める必要があります。</span><span class="sxs-lookup"><span data-stu-id="a9dfb-107">The solution must include an ER [configuration](general-electronic-reporting.md#Configuration) that contains an ER [format](general-electronic-reporting.md#FormatComponentOutbound) component.</span></span> <span data-ttu-id="a9dfb-108">この ER 形式は、レポート生成用に設計されたテンプレートを使用するように構成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="a9dfb-108">This ER format must be configured to use the designed template for report generation.</span></span>

<span data-ttu-id="a9dfb-109">Dynamics 365 Finance のバージョン 10.0.6 以降のバージョンでは、ER 形式のフォーミュラを構成して生成されるドキュメントで一部の Word コンテンツ コントロールを非表示にできます。</span><span class="sxs-lookup"><span data-stu-id="a9dfb-109">In version 10.0.6 and later of Dynamics 365 Finance, you can configure formulas in your ER format to suppress some Word content controls in generated documents.</span></span>

<span data-ttu-id="a9dfb-110">次の手順では、システム管理者または電子申告機能コンサルタントのロールに割り当てられたユーザーが、レポートを Word ファイルとして生成し、Word テンプレートを使用して構成されている生成されたレポートの一部のコンテンツ コントロールを非表示にする ER 形式を構成する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="a9dfb-110">The following steps explain how a user who is assigned to the System administrator or Electronic reporting functional consultant role can configure an ER format that generates reports as Word files and suppresses some of the content controls in the generated reports that have been configured by using a Word template.</span></span>

<span data-ttu-id="a9dfb-111">これらの手順を GBSI 社を使用して説明します。</span><span class="sxs-lookup"><span data-stu-id="a9dfb-111">These steps can be completed in the GBSI company.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="a9dfb-112">必要条件</span><span class="sxs-lookup"><span data-stu-id="a9dfb-112">Prerequisites</span></span>

<span data-ttu-id="a9dfb-113">これらのステップを完了するには、まず次のタスク ガイドの手順を完了する必要があります。</span><span class="sxs-lookup"><span data-stu-id="a9dfb-113">To complete these steps, you must first complete the steps in the following task guides:</span></span>

- [<span data-ttu-id="a9dfb-114">OPENXML 形式のレポートを生成するコンフィギュレーションを設計する</span><span class="sxs-lookup"><span data-stu-id="a9dfb-114">Design a configuration for generating reports in OPENXML format</span></span>](./tasks/er-design-reports-openxml-2016-11.md)
- [<span data-ttu-id="a9dfb-115">Excel テンプレートで ER の構成を再利用して Word 形式のレポートを生成する</span><span class="sxs-lookup"><span data-stu-id="a9dfb-115">Re-use ER configurations with Excel templates to generate reports in Word format</span></span>](./tasks/er-design-configuration-word-2016-11.md)

<span data-ttu-id="a9dfb-116">これらのタスク ガイドの手順を完了すると、次の項目が準備されます。</span><span class="sxs-lookup"><span data-stu-id="a9dfb-116">When you complete the steps of these task guides, the following items are prepared:</span></span>

- <span data-ttu-id="a9dfb-117">Word 形式でドキュメントを生成するために構成される **ワークシート レポートのサンプル** ER 形式</span><span class="sxs-lookup"><span data-stu-id="a9dfb-117">A **Sample worksheet report** ER format that is configured to generate a document in Word format</span></span>
- <span data-ttu-id="a9dfb-118">**実行可能** としてマークされている **サンプル ワークシート レポート** ER 形式の [ドラフト](general-electronic-reporting.md#component-versioning) バージョン</span><span class="sxs-lookup"><span data-stu-id="a9dfb-118">A [draft](general-electronic-reporting.md#component-versioning) version of the **Sample worksheet report** ER format that is marked as **Runnable**</span></span>
- <span data-ttu-id="a9dfb-119">仕入先支払の処理のために **サンプル ワークシート レポート** ER 形式を使用するために構成される **電子** 支払メソッド</span><span class="sxs-lookup"><span data-stu-id="a9dfb-119">An **Electronic** method of payments that is configured to use the **Sample worksheet report** ER format for vendor payment processing</span></span>

<span data-ttu-id="a9dfb-120">また、サンプル レポート用に次のテンプレートをダウンロードして保存する必要があります。</span><span class="sxs-lookup"><span data-stu-id="a9dfb-120">You must also download and save the following template for the sample report:</span></span>

- [<span data-ttu-id="a9dfb-121">支払レポートのバインドされたテンプレート 2 (SampleVendPaymDocReportBounded2.docx)</span><span class="sxs-lookup"><span data-stu-id="a9dfb-121">Bounded Template 2 of Payment Report (SampleVendPaymDocReportBounded2.docx)</span></span>](https://download.microsoft.com/download/a/1/2/a126cb43-6281-4f7b-bde0-25e03ff9bc1e/SampleVendPaymDocReportBounded2.docx)

## <a name="review-the-downloaded-word-template"></a><a id="tag-control"></a><span data-ttu-id="a9dfb-122">ダウンロードした Word テンプレートの確認</span><span class="sxs-lookup"><span data-stu-id="a9dfb-122">Review the downloaded Word template</span></span>

1. <span data-ttu-id="a9dfb-123">Word デスクトップ アプリケーションで、先にダウンロードした **SampleVendPaymDocReportBounded2.docx** テンプレート ファイルを開きます。</span><span class="sxs-lookup"><span data-stu-id="a9dfb-123">In the Word desktop application, open the **SampleVendPaymDocReportBounded2.docx** template file that you downloaded earlier.</span></span>
2. <span data-ttu-id="a9dfb-124">テンプレート ファイルに、処理された支払に使用される各通貨コードの合計支払金額を示す概要セクションが含まれていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="a9dfb-124">Verify that the template file contains a summary section that shows the total payment amounts for every currency code that has been met in the processed payments.</span></span>

    - <span data-ttu-id="a9dfb-125">概要セクションは、Word ドキュメントの別のテーブルに存在します。</span><span class="sxs-lookup"><span data-stu-id="a9dfb-125">The summary section resides in a separate table of the Word document.</span></span>
    - <span data-ttu-id="a9dfb-126">このテーブルの最初の行は、セクション ヘッダーとしてテーブル列のヘッダーを保持します。</span><span class="sxs-lookup"><span data-stu-id="a9dfb-126">The first row of this table holds the table columns headings as the section header.</span></span>
    - <span data-ttu-id="a9dfb-127">このテーブルの 2 番目の行は、セクションの詳細として繰り返しコンテンツ コントロールを保持します。</span><span class="sxs-lookup"><span data-stu-id="a9dfb-127">The second row of this table holds the repeating content control as the section details.</span></span>
    - <span data-ttu-id="a9dfb-128">このコンテンツ コントロールは、**レポート** カスタム XML パーツの **SummaryLines** フィールドにマップされます。</span><span class="sxs-lookup"><span data-stu-id="a9dfb-128">This content control is mapped to the **SummaryLines** field of the **Report** custom XML part.</span></span>
    - <span data-ttu-id="a9dfb-129">このマッピングに基づいて、コンテンツ コントロールは編集可能な ER 形式の **SummaryLines** 要素に関連付けらされます。</span><span class="sxs-lookup"><span data-stu-id="a9dfb-129">Based on this mapping, the content control is associated with the **SummaryLines** element of the editable ER format.</span></span>

    > [!NOTE]
    > <span data-ttu-id="a9dfb-130">繰り返しコンテンツ コントロールは、マップされているカスタム XML パーツのフィールドに一致する **SummaryLines** キーによってタグ付けされます。</span><span class="sxs-lookup"><span data-stu-id="a9dfb-130">The repeating content control is tagged by the **SummaryLines** key that matches the field of the custom XML part that it has been mapped to.</span></span>

    ![Word テンプレート レイアウト](./media/er-design-configuration-word-suppress-controls-image1.gif)

## <a name="select-the-existing-er-report-configuration"></a><span data-ttu-id="a9dfb-132">既存の ER レポート コンフィギュレーションを選択します</span><span class="sxs-lookup"><span data-stu-id="a9dfb-132">Select the existing ER report configuration</span></span>

<span data-ttu-id="a9dfb-133">以下の手順では、前述のタスク ガイドの手順を完了したときに構成した既存の ER 構成を再利用します。</span><span class="sxs-lookup"><span data-stu-id="a9dfb-133">For the following steps, you will reuse the existing ER configuration that you configured when you completed the steps in the previously mentioned task guides.</span></span>

1. <span data-ttu-id="a9dfb-134">**組織管理** \> **ワークスペース** \> **電子申告** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="a9dfb-134">Go to **Organization administration** \> **Workspaces** \> **Electronic reporting**.</span></span>
2. <span data-ttu-id="a9dfb-135">**コンフィギュレーションをレポートする** を選択します。</span><span class="sxs-lookup"><span data-stu-id="a9dfb-135">Select **Reporting configurations**.</span></span>
3. <span data-ttu-id="a9dfb-136">**構成** ページの構成ツリーで、**支払モデル** を展開し、**サンプル ワークシート レポート** を選択します。</span><span class="sxs-lookup"><span data-stu-id="a9dfb-136">On the **Configurations** page, in the configuration tree, expand **Payment model**, and select **Sample worksheet report**.</span></span>
4. <span data-ttu-id="a9dfb-137">**デザイナー** を選択し、選択した ER 形式のドラフト バージョンを編集します。</span><span class="sxs-lookup"><span data-stu-id="a9dfb-137">Select **Designer** to edit the draft version of the selected ER format.</span></span>

## <a name="replace-the-current-template-with-the-new-template"></a><span data-ttu-id="a9dfb-138">現在のテンプレートを新しいテンプレートに置き換えます</span><span class="sxs-lookup"><span data-stu-id="a9dfb-138">Replace the current template with the new template</span></span>

<span data-ttu-id="a9dfb-139">現在は、Word 形式で出力を生成するテンプレートとして SampleVendPaymDocReportBounded.docx ファイルが使用されます。</span><span class="sxs-lookup"><span data-stu-id="a9dfb-139">Currently, the SampleVendPaymDocReportBounded.docx file is used as a template to generate the output in Word format.</span></span> <span data-ttu-id="a9dfb-140">次の手順では、この Word テンプレートを、以前ダウンロードした新しい Word テンプレートである SampleVendPaymDocReportBounded2.docx に置き換えます。</span><span class="sxs-lookup"><span data-stu-id="a9dfb-140">In the following steps, you will replace this Word template with the new Word template, SampleVendPaymDocReportBounded2.docx, that you downloaded earlier.</span></span>

1. <span data-ttu-id="a9dfb-141">**フォーマット デザイナー** ページで、**添付** を選択します。</span><span class="sxs-lookup"><span data-stu-id="a9dfb-141">On the **Format designer** page, select **Attachments**.</span></span>
2. <span data-ttu-id="a9dfb-142">**添付ファイル** ページで **削除** を選択して、既存のテンプレートを削除します。</span><span class="sxs-lookup"><span data-stu-id="a9dfb-142">On the **Attachments** page, select **Delete** to remove the existing template.</span></span>
3. <span data-ttu-id="a9dfb-143">**はい** を選択して削除を確認します。</span><span class="sxs-lookup"><span data-stu-id="a9dfb-143">Select **Yes** to confirm the deletion.</span></span>
4. <span data-ttu-id="a9dfb-144">**新規** \> **ファイル** を選択します。</span><span class="sxs-lookup"><span data-stu-id="a9dfb-144">Select **New** \> **File**.</span></span>
5. <span data-ttu-id="a9dfb-145">**参照** を選択し、以前にダウンロードした **SampleVendPaymDocReportBounded2** ファイルを参照して選択します。</span><span class="sxs-lookup"><span data-stu-id="a9dfb-145">Select **Browse**, and browse to and select the **SampleVendPaymDocReportBounded2.docx** file that you downloaded earlier.</span></span>
6. <span data-ttu-id="a9dfb-146">**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="a9dfb-146">Select **OK**.</span></span>
7. <span data-ttu-id="a9dfb-147">**添付ファイル** ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="a9dfb-147">Close the **Attachments** page.</span></span>
8. <span data-ttu-id="a9dfb-148">**形式デザイナー** ページの **テンプレート** フィールドで、**SampleVendPaymDocReportBounded2.docx** ファイルを入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="a9dfb-148">On the **Format designer** page, in the **Template** field, enter or select the **SampleVendPaymDocReportBounded2.docx** file.</span></span>

## <a name="run-the-format-to-create-word-output"></a><span data-ttu-id="a9dfb-149">フォーマットを実行して Word 出力を作成する</span><span class="sxs-lookup"><span data-stu-id="a9dfb-149">Run the format to create Word output</span></span>

1. <span data-ttu-id="a9dfb-150">**買掛金勘定** \> **支払** \> **支払仕訳帳** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="a9dfb-150">Go to **Accounts payable** \> **Payments** \> **Payment journal**.</span></span>
2. <span data-ttu-id="a9dfb-151">**仕入先支払** ページの、**リスト** タブで、すべての支払を選択します。</span><span class="sxs-lookup"><span data-stu-id="a9dfb-151">On the **Vendor payments** page, on the **List** tab, select all the payments.</span></span>
3. <span data-ttu-id="a9dfb-152">**支払ステータス** \> **なし** を選択します。</span><span class="sxs-lookup"><span data-stu-id="a9dfb-152">Select **Payment status** \> **None**.</span></span>
4. <span data-ttu-id="a9dfb-153">**支払の生成** を選択します。</span><span class="sxs-lookup"><span data-stu-id="a9dfb-153">Select **Generate payments**.</span></span>
5. <span data-ttu-id="a9dfb-154">**支払方法** フィールドで、**電子** を選択します。</span><span class="sxs-lookup"><span data-stu-id="a9dfb-154">In the **Method of payment** field, select **Electronic**.</span></span>
6. <span data-ttu-id="a9dfb-155">**銀行口座** フィールドで、 **GBSI OPER** を選択します。</span><span class="sxs-lookup"><span data-stu-id="a9dfb-155">In the **Bank account** field, select **GBSI OPER**.</span></span>
7. <span data-ttu-id="a9dfb-156">**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="a9dfb-156">Select **OK**.</span></span>
8. <span data-ttu-id="a9dfb-157">**電子申告パラメーター** ダイアログ ボックスで、**OK** を選択し、生成された出力を分析します。</span><span class="sxs-lookup"><span data-stu-id="a9dfb-157">In the **Electronic report parameters** dialog box, select **OK**, and analyze the generated output.</span></span>

    ![仕入先支払ページでの処理に対する支払](./media/er-design-configuration-word-suppress-controls-image2.gif)

    <span data-ttu-id="a9dfb-159">出力は Word 形式で表示され、概要セクションを含みます。</span><span class="sxs-lookup"><span data-stu-id="a9dfb-159">The output is presented in Word format and contains the summary section.</span></span>

## <a name="configure-the-editable-format-to-suppress-the-summary-section"></a><a id="configure-to-suppress-control"></a><span data-ttu-id="a9dfb-160">編集可能な形式を構成して概要セクションを非表示にする</span><span class="sxs-lookup"><span data-stu-id="a9dfb-160">Configure the editable format to suppress the summary section</span></span>

<span data-ttu-id="a9dfb-161">この ER 形式を実行するユーザーの要求に基づいて、生成されたドキュメントの概要セクションを非表示にする場合は、編集可能な ER 形式を変更する必要があります。</span><span class="sxs-lookup"><span data-stu-id="a9dfb-161">If you want to suppress the summary section in a generated document, based on the request of a user who runs this ER format, you must modify the editable ER format.</span></span>

1. <span data-ttu-id="a9dfb-162">**組織管理** \> **ワークスペース** \> **電子申告** に移動し、編集用の ER 形式のドラフト バージョンを開きます。</span><span class="sxs-lookup"><span data-stu-id="a9dfb-162">Go to **Organization administration** \> **Workspaces** \> **Electronic reporting**, and open the draft version of the ER format for editing.</span></span>
2. <span data-ttu-id="a9dfb-163">**コンフィギュレーションをレポートする** を選択します。</span><span class="sxs-lookup"><span data-stu-id="a9dfb-163">Select **Reporting configurations**.</span></span> 
3. <span data-ttu-id="a9dfb-164">**構成** ページの構成ツリーで、**支払モデル** \> **サンプル ワークシート レポート** を展開します。</span><span class="sxs-lookup"><span data-stu-id="a9dfb-164">On the **Configurations** page, in the configuration tree, expand **Payment model** \> **Sample worksheet report**.</span></span>
4. <span data-ttu-id="a9dfb-165">**デザイナー** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="a9dfb-165">Select **Designer**.</span></span>
5. <span data-ttu-id="a9dfb-166">**形式デザイナー** ページで、**Word** を展開し、**SummaryLines** を選択します。</span><span class="sxs-lookup"><span data-stu-id="a9dfb-166">On the **Format designer** page, expand **Word**, and select **SummaryLines**.</span></span>
6. <span data-ttu-id="a9dfb-167">**マッピング** タブで、新しいデータソースを追加し、ランタイムに、概要セクションを非表示にするかどうかをユーザーに確認します。</span><span class="sxs-lookup"><span data-stu-id="a9dfb-167">On the **Mapping** tab, add a new data source to ask the user, at runtime, whether the summary section should be suppressed:</span></span>

    1. <span data-ttu-id="a9dfb-168">**ルートの追加** を選択します。</span><span class="sxs-lookup"><span data-stu-id="a9dfb-168">Select **Add root**.</span></span>
    2. <span data-ttu-id="a9dfb-169">**データ ソースの追加** ダイアログ ボックスで、**全般\ユーザー入力パラメーター** を選択し、**'ユーザー入力パラメーター' データ ソース プロパティ** のダイアログ ボックスを開きます。</span><span class="sxs-lookup"><span data-stu-id="a9dfb-169">In the **Add data source** dialog box, select **General\User input parameter** to open the **'User input parameter' data source properties** dialog box.</span></span>
    3. <span data-ttu-id="a9dfb-170">**名前** フィールドに、**uipSuppress** と入力します。</span><span class="sxs-lookup"><span data-stu-id="a9dfb-170">In the **Name** field, enter **uipSuppress**.</span></span>
    4. <span data-ttu-id="a9dfb-171">**ラベル** フィールドに、**概要セクションの非表示** を入力します。</span><span class="sxs-lookup"><span data-stu-id="a9dfb-171">In the **Label** field, enter **Suppress summary section**.</span></span>
    5. <span data-ttu-id="a9dfb-172">**操作のデータ型名** フィールドに、**NoYes** を選択または入力します。</span><span class="sxs-lookup"><span data-stu-id="a9dfb-172">In the **Operations data type name** field, select or enter **NoYes**.</span></span>
    6. <span data-ttu-id="a9dfb-173">**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="a9dfb-173">Select **OK**.</span></span>

7. <span data-ttu-id="a9dfb-174">**NoYes** アプリケーション列挙型の新しいデータ ソースを追加します:</span><span class="sxs-lookup"><span data-stu-id="a9dfb-174">Add a new data source of the **NoYes** application enumeration type:</span></span>

    1. <span data-ttu-id="a9dfb-175">**ルートの追加** を選択します。</span><span class="sxs-lookup"><span data-stu-id="a9dfb-175">Select **Add root**.</span></span>
    2. <span data-ttu-id="a9dfb-176">**データ ソースの追加** ダイアログ ボックスで、**Dynamics 365 for Operations\列挙** を選択し、**'列挙型' データ ソースのプロパティ** ダイアログ ボックスを開きます。</span><span class="sxs-lookup"><span data-stu-id="a9dfb-176">In the **Add data source** dialog box, select **Dynamics 365 for Operations\Enumeration** to open the **'Enumeration' data source properties** dialog box.</span></span>
    3. <span data-ttu-id="a9dfb-177">**名前** フィールドに、**enumNoYes** と入力します。</span><span class="sxs-lookup"><span data-stu-id="a9dfb-177">In the **Name** field, enter **enumNoYes**.</span></span>
    4. <span data-ttu-id="a9dfb-178">**ラベル** フィールドに、**オプションの非表示** を入力します。</span><span class="sxs-lookup"><span data-stu-id="a9dfb-178">In the **Label** field, enter **Suppress options**.</span></span>
    5. <span data-ttu-id="a9dfb-179">**操作のデータ型名** フィールドに、**NoYes** を選択または入力します。</span><span class="sxs-lookup"><span data-stu-id="a9dfb-179">In the **Operations data type name** field, select or enter **NoYes**.</span></span>
    6. <span data-ttu-id="a9dfb-180">**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="a9dfb-180">Select **OK**.</span></span>

8. <span data-ttu-id="a9dfb-181">選択した **SummaryLines** 形式要素に対して、選択した形式要素に関連付けられている Word コンテンツ コントロールを非表示にする場合、指定する形式を構成します。</span><span class="sxs-lookup"><span data-stu-id="a9dfb-181">For the selected **SummaryLines** format element, configure the formula to specify when the Word content control that is associated with the selected format element should be suppressed:</span></span>

    1. <span data-ttu-id="a9dfb-182">**マッピング** タブの **削除済** セクションで、**編集** 選択して、**[フォーミュラ デザイナー](general-electronic-reporting-formula-designer.md)** ページを開きます。</span><span class="sxs-lookup"><span data-stu-id="a9dfb-182">On the **Mapping** tab, in the **Removed** section, select **Edit** to open the **[Formula designer](general-electronic-reporting-formula-designer.md)** page.</span></span>
    2. <span data-ttu-id="a9dfb-183">**フォーミュラ** フィールドで、`uipSuppress = enumNoYes.Yes` というフォーミュラを入力します。</span><span class="sxs-lookup"><span data-stu-id="a9dfb-183">In the **Formula** field, enter the formula `uipSuppress = enumNoYes.Yes`.</span></span>
    3. <span data-ttu-id="a9dfb-184">**保存** を選択し、**フォーミュラ デザイナー** ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="a9dfb-184">Select **Save**, and close the **Formula designer** page.</span></span>

        > [!NOTE]
        > <span data-ttu-id="a9dfb-185">この数式は、**その他のすべての形式要素が実行された後** に生成されたドキュメントに適用されます。</span><span class="sxs-lookup"><span data-stu-id="a9dfb-185">This formula will be applied to a generated document **after all other format elements are run**.</span></span> <span data-ttu-id="a9dfb-186">この式を適用するには、式が構成される形式要素としてタグ付けされた Word コンテンツ コントロール (この場合は **SummaryLines**) は生成されたドキュメントにあります。</span><span class="sxs-lookup"><span data-stu-id="a9dfb-186">To apply this formula, a Word content control that is tagged as a format element that the formula is configured for (**SummaryLines** in this case) is found in a generated document.</span></span> <span data-ttu-id="a9dfb-187">そのコンテンツ コントロールは、それを保持する Word テーブルの行と共に完全に削除されます。</span><span class="sxs-lookup"><span data-stu-id="a9dfb-187">That content control is then completely removed, together with the row in the Word table that holds it.</span></span> <span data-ttu-id="a9dfb-188">概要セクションの詳細行は、生成されたドキュメントから削除されます。</span><span class="sxs-lookup"><span data-stu-id="a9dfb-188">The details row of the summary section is removed from the generated document.</span></span>
        >
        > <span data-ttu-id="a9dfb-189">デザイン時に、使用している Word テンプレートのコンテンツ コントロールに **削除済み** プロパティが構成されている形式要素の名前に一致するタグがない場合でも、形式要素に対して **削除済み** の式を構成できます。</span><span class="sxs-lookup"><span data-stu-id="a9dfb-189">At design time, you might configure the **Removed** formula for a format element, even though no content control in the Word template that you're using has a tag that matches the name of a format element that the **Removed** property is configured for.</span></span> <span data-ttu-id="a9dfb-190">デザイン時に形式を検証すると、この不整合に関する[警告](er-components-inspections.md#i14) が表示されます。</span><span class="sxs-lookup"><span data-stu-id="a9dfb-190">When you validate the format at design time, you receive a [warning](er-components-inspections.md#i14) about this inconsistency.</span></span>
        >
        > <span data-ttu-id="a9dfb-191">実行時に、使用している Word テンプレートのコンテンツ コントロールに **削除済み** プロパティが構成されている形式要素の名前に一致するタグがない場合、例外がスローされます。</span><span class="sxs-lookup"><span data-stu-id="a9dfb-191">At runtime, an exception is thrown if no content control in the Word template that you're using has a tag that matches the name of a format element that the **Removed** property is configured for.</span></span>

    4. <span data-ttu-id="a9dfb-192">**マッピング** タブの **削除済み** セクションで、**親を含む** オプションを **はい** に設定します。</span><span class="sxs-lookup"><span data-stu-id="a9dfb-192">On the **Mapping** tab, in the **Removed** section, set the **With parent** option to **Yes**.</span></span>

        > [!NOTE]
        > <span data-ttu-id="a9dfb-193">このオプションを **はい** にして、概要セクションの詳細を保持する行の親オブジェクトとして Word テーブル全体を削除する必要があります。</span><span class="sxs-lookup"><span data-stu-id="a9dfb-193">You must set this option to **Yes** to remove the whole Word table as the parent object of the row that holds the summary section details.</span></span> <span data-ttu-id="a9dfb-194">このオプションを **いいえ** に設定した場合、セクション ヘッダーの行は生成されるドキュメント内に残ります。</span><span class="sxs-lookup"><span data-stu-id="a9dfb-194">If you set this option to **No**, the section header row remains in the generated document.</span></span>

9. <span data-ttu-id="a9dfb-195">**保存** を選択し、編集可能な形式への変更を保存します。</span><span class="sxs-lookup"><span data-stu-id="a9dfb-195">Select **Save** to save your changes to the editable format.</span></span>

    ![Word 形式で生成された出力](./media/er-design-configuration-word-suppress-controls-image3.gif)

## <a name="run-the-modified-format-to-create-word-output"></a><span data-ttu-id="a9dfb-197">修正済みのフォーマットを実行して Word 出力を作成する</span><span class="sxs-lookup"><span data-stu-id="a9dfb-197">Run the modified format to create Word output</span></span>

1. <span data-ttu-id="a9dfb-198">**買掛金勘定** \> **支払** \> **支払仕訳帳** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="a9dfb-198">Go to **Accounts payable** \> **Payments** \> **Payment journal**.</span></span>
2. <span data-ttu-id="a9dfb-199">作成した支払仕訳帳を選択し、**明細行** を選択します。</span><span class="sxs-lookup"><span data-stu-id="a9dfb-199">Select the payment journal that you created, and then select **Lines**.</span></span>
3. <span data-ttu-id="a9dfb-200">**仕入先支払** ページで、すべての行を選択し、**支払ステータス** \> **なし** を選択します。</span><span class="sxs-lookup"><span data-stu-id="a9dfb-200">On the **Vendor payments** page, select all the rows, and then select **Payment status** \> **None**.</span></span>
4. <span data-ttu-id="a9dfb-201">**支払の生成** を選択します。</span><span class="sxs-lookup"><span data-stu-id="a9dfb-201">Select **Generate payments**.</span></span>
5. <span data-ttu-id="a9dfb-202">**支払方法** フィールドで、**電子** を選択します。</span><span class="sxs-lookup"><span data-stu-id="a9dfb-202">In the **Method of payment** field, select **Electronic**.</span></span>
6. <span data-ttu-id="a9dfb-203">**銀行口座** フィールドで、 **GBSI OPER** を選択します。</span><span class="sxs-lookup"><span data-stu-id="a9dfb-203">In the **Bank account** field, select **GBSI OPER**.</span></span>
7. <span data-ttu-id="a9dfb-204">**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="a9dfb-204">Select **OK**.</span></span>
8. <span data-ttu-id="a9dfb-205">**電子申告パラメーター** ダイアログ ボックスの **概要セクションの非表示** フィールドで **はい** を選択します。</span><span class="sxs-lookup"><span data-stu-id="a9dfb-205">In the **Electronic report parameters** dialog box, in the **Suppress summary section** field, select **Yes**.</span></span>
9. <span data-ttu-id="a9dfb-206">**OK** を選択し、生成された出力を分析します。</span><span class="sxs-lookup"><span data-stu-id="a9dfb-206">Select **OK**, and analyze the generated output.</span></span>

    ![Word 形式で生成された出力](./media/er-design-configuration-word-suppress-controls-image4.gif)

    <span data-ttu-id="a9dfb-208">出力が非表示なので、概要セクションが含まれていないことに注意してください。</span><span class="sxs-lookup"><span data-stu-id="a9dfb-208">Notice that the output doesn't contain the summary section, because it has been suppressed.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="a9dfb-209">追加リソース</span><span class="sxs-lookup"><span data-stu-id="a9dfb-209">Additional resources</span></span>

- [<span data-ttu-id="a9dfb-210">OPENXML 形式のレポートを生成するコンフィギュレーションを設計する</span><span class="sxs-lookup"><span data-stu-id="a9dfb-210">Design a configuration for generating reports in OPENXML format</span></span>](./tasks/er-design-reports-openxml-2016-11.md)
- [<span data-ttu-id="a9dfb-211">Word 形式のレポートを生成するための新しい ER コンフィギュレーションを設計する</span><span class="sxs-lookup"><span data-stu-id="a9dfb-211">Design a new ER configuration to generate reports in Word format</span></span>](er-design-configuration-word.md)
- [<span data-ttu-id="a9dfb-212">Excel テンプレートで ER の構成を再利用して Word 形式のレポートを生成する</span><span class="sxs-lookup"><span data-stu-id="a9dfb-212">Re-use ER configurations with Excel templates to generate reports in Word format</span></span>](./tasks/er-design-configuration-word-2016-11.md)
- [<span data-ttu-id="a9dfb-213">構成済み ER コンポーネントを検査して、ランタイムの問題を回避する</span><span class="sxs-lookup"><span data-stu-id="a9dfb-213">Inspect the configured ER component to prevent runtime issues</span></span>](er-components-inspections.md#i14)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]