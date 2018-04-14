---
title: "口座取引明細書ファイルのインポートのトラブルシューティング"
description: "銀行からの口座取引明細書ファイルが、Microsoft Dynamics 365 for Finance and Operations がサポートするレイアウトと一致することが重要です。 口座取引明細書の基準が厳しいために、ほとんどの統合が正しく動作します。 ただし、明細書ファイルがインポートできない場合または不正確な結果が含まれている場合があります。 通常、これらの問題は口座取引明細書ファイルの小さな差異によって引き起こされます。 この記事は、これらの差異を修正し問題を解決する方法を説明します。"
author: twheeloc
manager: AnnBe
ms.date: 01/11/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: BankStatementFormat
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 141273
ms.assetid: 3ee2f32b-02aa-420b-8990-e6aa5fc6bda3
ms.search.region: global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: a5f53a76ebd0bd428f791ce8493e9f388eb8e2fa
ms.contentlocale: ja-jp
ms.lasthandoff: 04/13/2018

---

# <a name="bank-statement-file-import-troubleshooting"></a><span data-ttu-id="d967c-107">口座取引明細書ファイルのインポートのトラブルシューティング</span><span class="sxs-lookup"><span data-stu-id="d967c-107">Bank statement file import troubleshooting</span></span>

[!INCLUDE [banner](../includes/banner.md)]

<span data-ttu-id="d967c-108">銀行からの口座取引明細書ファイルが、Microsoft Dynamics 365 for Finance and Operations がサポートするレイアウトと一致することが重要です。</span><span class="sxs-lookup"><span data-stu-id="d967c-108">It's important that the bank statement file from the bank match the layout that Microsoft Dynamics 365 for Finance and Operations supports.</span></span> <span data-ttu-id="d967c-109">口座取引明細書の基準が厳しいために、ほとんどの統合が正しく動作します。</span><span class="sxs-lookup"><span data-stu-id="d967c-109">Because of strict standards for bank statements, most integrations will work correctly.</span></span> <span data-ttu-id="d967c-110">ただし、明細書ファイルがインポートできない場合または不正確な結果が含まれている場合があります。</span><span class="sxs-lookup"><span data-stu-id="d967c-110">However, sometimes the statement file can't be imported or has incorrect results.</span></span> <span data-ttu-id="d967c-111">通常、これらの問題は口座取引明細書ファイルの小さな差異によって引き起こされます。</span><span class="sxs-lookup"><span data-stu-id="d967c-111">Typically, these issues are caused by small differences in the bank statement file.</span></span> <span data-ttu-id="d967c-112">この記事は、これらの差異を修正し問題を解決する方法を説明します。</span><span class="sxs-lookup"><span data-stu-id="d967c-112">This article explains how to fix these differences and resolve the issues.</span></span>

<a name="what-is-the-error"></a><span data-ttu-id="d967c-113">エラーは何ですか?</span><span class="sxs-lookup"><span data-stu-id="d967c-113">What is the error?</span></span>
------------------

<span data-ttu-id="d967c-114">口座取引明細書ファイルのインポートを試行した後に、データ管理ジョブ履歴および実行の詳細に移動し、エラーを検索します。</span><span class="sxs-lookup"><span data-stu-id="d967c-114">After you try to import a bank statement file, go to the Data management job history and its execution details to find the error.</span></span> <span data-ttu-id="d967c-115">エラーは、明細書、残高、または明細行を指し示すのに役立ちます。</span><span class="sxs-lookup"><span data-stu-id="d967c-115">The error can help by pointing to the statement, balance, or statement line.</span></span> <span data-ttu-id="d967c-116">ただし、問題の原因となっているフィールドまたは要素を識別するために十分な情報を提供することは少ないです。</span><span class="sxs-lookup"><span data-stu-id="d967c-116">However, it's unlikely to provide enough information to help you identify the field or element that is causing the issue.</span></span>

## <a name="what-are-the-differences"></a><span data-ttu-id="d967c-117">差異は何ですか?</span><span class="sxs-lookup"><span data-stu-id="d967c-117">What are the differences?</span></span>
<span data-ttu-id="d967c-118">銀行ファイル レイアウト定義を Finance and Operations のインポート定義と比較し、フィールドおよび要素の差異を確認します。</span><span class="sxs-lookup"><span data-stu-id="d967c-118">Compare the bank file layout definition to the Finance and Operations import definition, and note any differences in the fields and elements.</span></span> <span data-ttu-id="d967c-119">口座取引明細書ファイルを関連する Finance and Operations ファイルのサンプルと比較します。</span><span class="sxs-lookup"><span data-stu-id="d967c-119">Compare the bank statement file to the related sample Finance and Operations file.</span></span> <span data-ttu-id="d967c-120">ISO20022 ファイルでは、差異が一目で分かります。</span><span class="sxs-lookup"><span data-stu-id="d967c-120">In the ISO20022 files, any differences should be easy to see.</span></span>

## <a name="transformations"></a><span data-ttu-id="d967c-121">変換</span><span class="sxs-lookup"><span data-stu-id="d967c-121">Transformations</span></span>
<span data-ttu-id="d967c-122">通常、変更は次の 3 つの変換のいずれかで行われます。</span><span class="sxs-lookup"><span data-stu-id="d967c-122">Typically, the change must be made in one of three transformations.</span></span> <span data-ttu-id="d967c-123">各変換は、指定された標準形式で書き込まれます。</span><span class="sxs-lookup"><span data-stu-id="d967c-123">Each transformation is written for a specific standard.</span></span>

| <span data-ttu-id="d967c-124">リソース名</span><span class="sxs-lookup"><span data-stu-id="d967c-124">Resource name</span></span>                                         | <span data-ttu-id="d967c-125">ファイル名</span><span class="sxs-lookup"><span data-stu-id="d967c-125">File name</span></span>                          |
|-------------------------------------------------------|------------------------------------|
| <span data-ttu-id="d967c-126">BankStmtImport\_BAI2CSV\_to\_BAI2XML\_xslt</span><span class="sxs-lookup"><span data-stu-id="d967c-126">BankStmtImport\_BAI2CSV\_to\_BAI2XML\_xslt</span></span>            | <span data-ttu-id="d967c-127">BAI2CSV-to-BAI2XML.xslt</span><span class="sxs-lookup"><span data-stu-id="d967c-127">BAI2CSV-to-BAI2XML.xslt</span></span>            |
| <span data-ttu-id="d967c-128">BankStmtImport\_ISO20022XML\_to\_Reconciliation\_xslt</span><span class="sxs-lookup"><span data-stu-id="d967c-128">BankStmtImport\_ISO20022XML\_to\_Reconciliation\_xslt</span></span> | <span data-ttu-id="d967c-129">ISO20022XML-to-Reconciliation.xslt</span><span class="sxs-lookup"><span data-stu-id="d967c-129">ISO20022XML-to-Reconciliation.xslt</span></span> |
| <span data-ttu-id="d967c-130">BankStmtImport\_MT940TXT\_to\_MT940XML\_xslt</span><span class="sxs-lookup"><span data-stu-id="d967c-130">BankStmtImport\_MT940TXT\_to\_MT940XML\_xslt</span></span>          | <span data-ttu-id="d967c-131">MT940TXT-to-MT940XML.xslt</span><span class="sxs-lookup"><span data-stu-id="d967c-131">MT940TXT-to-MT940XML.xslt</span></span>          |

## <a name="debugging-transformations"></a><span data-ttu-id="d967c-132">デバッグの変換</span><span class="sxs-lookup"><span data-stu-id="d967c-132">Debugging transformations</span></span>
### <a name="adjust-the-bai2-and-mt940-files"></a><span data-ttu-id="d967c-133">BAI2 と MT940 ファイルの調整</span><span class="sxs-lookup"><span data-stu-id="d967c-133">Adjust the BAI2 and MT940 files</span></span>

<span data-ttu-id="d967c-134">BAI2 と MT940 ファイルはテキスト ベースのファイルで、XSLT (Extensible Stylesheet Language Transformations) デバッグを有効にするためには調整が必要です。</span><span class="sxs-lookup"><span data-stu-id="d967c-134">The BAI2 and MT940 files are text-based files and require an adjustment to enable Extensible Stylesheet Language Transformations (XSLT) debugging.</span></span> <span data-ttu-id="d967c-135">プログラムは、ファイルのインポート時にこの調整を行います。</span><span class="sxs-lookup"><span data-stu-id="d967c-135">The program makes this adjustment when a file is imported.</span></span>

1.  <span data-ttu-id="d967c-136">XML ファイルを作成し、次のテキストをコピーします。</span><span class="sxs-lookup"><span data-stu-id="d967c-136">Create an XML file, and copy the following text into it.</span></span>

        <Batch><![CDATA[PASTESTATEMENTFILEHERE
        ]]></Batch>

2.  <span data-ttu-id="d967c-137">口座取引明細書ファイルの内容をコピーし、XML ファイルに貼り **PASTESTATEMENTFILEHERE** を置換します。</span><span class="sxs-lookup"><span data-stu-id="d967c-137">Copy the contents of the bank statement file, and paste them into the XML file so that they replace **PASTESTATEMENTFILEHERE**.</span></span>

### <a name="debug-the-xslt"></a><span data-ttu-id="d967c-138">XSLT のデバッグ</span><span class="sxs-lookup"><span data-stu-id="d967c-138">Debug the XSLT</span></span>

<span data-ttu-id="d967c-139">詳細については、「<https://msdn.microsoft.com/en-us/library/ms255605.aspx>」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="d967c-139">For more information, see <https://msdn.microsoft.com/en-us/library/ms255605.aspx>.</span></span>

1.  <span data-ttu-id="d967c-140">Microsoft Visual Studio を開始します。</span><span class="sxs-lookup"><span data-stu-id="d967c-140">Start Microsoft Visual Studio.</span></span>
2.  <span data-ttu-id="d967c-141">コンソール アプリケーションを作成します。</span><span class="sxs-lookup"><span data-stu-id="d967c-141">Create a console application.</span></span>
3.  <span data-ttu-id="d967c-142">適切な XSLT を開きます。</span><span class="sxs-lookup"><span data-stu-id="d967c-142">Open the appropriate XSLT.</span></span>
4.  <span data-ttu-id="d967c-143">XLST とプロパティ ページをクリックします。</span><span class="sxs-lookup"><span data-stu-id="d967c-143">Click the XLST and its properties page.</span></span>
5.  <span data-ttu-id="d967c-144">口座取引明細書ファイルの場所の入力を設定します。</span><span class="sxs-lookup"><span data-stu-id="d967c-144">Set the input to the location of the bank statement file.</span></span>
6.  <span data-ttu-id="d967c-145">出力の場所とファイル名を定義します。</span><span class="sxs-lookup"><span data-stu-id="d967c-145">Define a location and file name for the output.</span></span>
7.  <span data-ttu-id="d967c-146">必要な区切り点を設定します。</span><span class="sxs-lookup"><span data-stu-id="d967c-146">Set the required break points.</span></span>
8.  <span data-ttu-id="d967c-147">メニューで、[**XML**] &gt; [**XSLT デバッグの開始**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="d967c-147">On the menu, click **XML** &gt; **Start XSLT Debugging**.</span></span>

### <a name="format-the-xslt-output"></a><span data-ttu-id="d967c-148">XSLT 出力の書式設定</span><span class="sxs-lookup"><span data-stu-id="d967c-148">Format the XSLT output</span></span>

<span data-ttu-id="d967c-149">変換を実行すると、Visual Studio で表示可能な出力ファイルを作成します。</span><span class="sxs-lookup"><span data-stu-id="d967c-149">When the transformation runs, it creates an output file that you can view in Visual Studio.</span></span> <span data-ttu-id="d967c-150">Ctrl+A、Ctrl+K と Ctrl+D を使用して、出力ファイルをすばやく書式設定します。</span><span class="sxs-lookup"><span data-stu-id="d967c-150">Use Ctrl+A, Ctrl+K, and Ctrl+D to quickly format the output file.</span></span>

### <a name="adjust-the-transformation"></a><span data-ttu-id="d967c-151">変換の調整</span><span class="sxs-lookup"><span data-stu-id="d967c-151">Adjust the transformation</span></span>

<span data-ttu-id="d967c-152">口座取引明細書ファイルの適切なフィールドまたは要素を得るために変換を調整します。</span><span class="sxs-lookup"><span data-stu-id="d967c-152">Adjust the transformation to get the appropriate field or element in the bank statement file.</span></span> <span data-ttu-id="d967c-153">次に適切な Finance and Operations の要素にそのフィールドまたは要素をマップします。</span><span class="sxs-lookup"><span data-stu-id="d967c-153">Then map that field or element to the appropriate Finance and Operations element.</span></span>

### <a name="debitcredit-indicator"></a><span data-ttu-id="d967c-154">借方/貸方インジケーター</span><span class="sxs-lookup"><span data-stu-id="d967c-154">Debit/credit indicator</span></span>

<span data-ttu-id="d967c-155">場合によっては、借方は貸方としてインポートされ、貸方が借方としてインポートされる場合があります。</span><span class="sxs-lookup"><span data-stu-id="d967c-155">Sometimes, debits might be imported as credits, and credits might be imported as debits.</span></span> <span data-ttu-id="d967c-156">この問題を解決するには、適切な XSLT を変更する必要があります。</span><span class="sxs-lookup"><span data-stu-id="d967c-156">To resolve this issue, you must change the appropriate XSLT.</span></span> <span data-ttu-id="d967c-157">口座取引明細書を複数の銀行から取得する場合、すべてが同じ借方/貸方を使用しているか、または別の変換を作成していることを確認してください。</span><span class="sxs-lookup"><span data-stu-id="d967c-157">If bank statements come from multiple banks, make sure that they all use the same debit/credit approach, or create separate transformations.</span></span>

-   <span data-ttu-id="d967c-158">BAI2XML-to-Reconciliation.xlst GetAmountCreditDebitIndicator テンプレート</span><span class="sxs-lookup"><span data-stu-id="d967c-158">BAI2XML-to-Reconciliation.xlst GetAmountCreditDebitIndicator template</span></span>
-   <span data-ttu-id="d967c-159">ISO20022XML-to-Reconcilation.xslt GetCreditDebit テンプレート</span><span class="sxs-lookup"><span data-stu-id="d967c-159">ISO20022XML-to-Reconcilation.xslt GetCreditDebit template</span></span>
-   <span data-ttu-id="d967c-160">MT940XML-to-Reconcilation.xslt GetCreditDebitIndicator テンプレート</span><span class="sxs-lookup"><span data-stu-id="d967c-160">MT940XML-to-Reconcilation.xslt GetCreditDebitIndicator template</span></span>

## <a name="examples-of-bank-statement-formats-and-technical-layouts"></a><span data-ttu-id="d967c-161">口座取引明細書の形式と技術的な配置の例</span><span class="sxs-lookup"><span data-stu-id="d967c-161">Examples of bank statement formats and technical layouts</span></span>
<span data-ttu-id="d967c-162">次の表は、詳細な口座調整のインポート ファイルの技術的な配置の定義、および 3 つの関連する口座取引明細書のサンプル ファイルの一覧を表示します。</span><span class="sxs-lookup"><span data-stu-id="d967c-162">The following table lists examples of the technical layout definitions for advanced bank reconciliation import files and three related bank statement example files.</span></span> <span data-ttu-id="d967c-163">サンプル ファイルと技術的な配置はここでダウンロードできます。https://mbs.microsoft.com/customersource/northamerica/AX/learning/documentation/how-to-articles/exofbankstfotechlayouts</span><span class="sxs-lookup"><span data-stu-id="d967c-163">You can download the example files and technical layouts here: https://mbs.microsoft.com/customersource/northamerica/AX/learning/documentation/how-to-articles/exofbankstfotechlayouts</span></span>  


| <span data-ttu-id="d967c-164">技術的なレイアウトの定義</span><span class="sxs-lookup"><span data-stu-id="d967c-164">Technical layout definition</span></span>                             | <span data-ttu-id="d967c-165">口座取引明細書のサンプル ファイル</span><span class="sxs-lookup"><span data-stu-id="d967c-165">Bank statement example file</span></span>          |
|---------------------------------------------------------|--------------------------------------|
| <span data-ttu-id="d967c-166">DynamicsAXMT940Layout</span><span class="sxs-lookup"><span data-stu-id="d967c-166">DynamicsAXMT940Layout</span></span>                                   | <span data-ttu-id="d967c-167">MT940StatementExample</span><span class="sxs-lookup"><span data-stu-id="d967c-167">MT940StatementExample</span></span>                |
| <span data-ttu-id="d967c-168">DynamicsAXISO20022Layout</span><span class="sxs-lookup"><span data-stu-id="d967c-168">DynamicsAXISO20022Layout</span></span>                                | <span data-ttu-id="d967c-169">ISO20022StatementExample</span><span class="sxs-lookup"><span data-stu-id="d967c-169">ISO20022StatementExample</span></span>             |
| <span data-ttu-id="d967c-170">DynamicsAXBAI2Layout</span><span class="sxs-lookup"><span data-stu-id="d967c-170">DynamicsAXBAI2Layout</span></span>                                    | <span data-ttu-id="d967c-171">BAI2StatementExample</span><span class="sxs-lookup"><span data-stu-id="d967c-171">BAI2StatementExample</span></span>                 |






