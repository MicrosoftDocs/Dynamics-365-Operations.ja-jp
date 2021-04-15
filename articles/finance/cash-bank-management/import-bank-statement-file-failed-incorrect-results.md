---
title: 口座取引明細書ファイルのインポートのトラブルシューティング
description: 銀行からの口座取引明細書ファイルが、Microsoft Dynamics 365 Finance がサポートするレイアウトと一致することが重要です。 口座取引明細書の基準が厳しいために、ほとんどの統合が正しく動作します。 ただし、明細書ファイルがインポートできない場合または不正確な結果が含まれている場合があります。 通常、これらの問題は口座取引明細書ファイルの小さな差異によって引き起こされます。 この記事は、これらの差異を修正し問題を解決する方法を説明します。
author: panolte
ms.date: 03/29/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: BankStatementFormat
audience: Application User
ms.reviewer: roschlom
ms.custom: 141273
ms.assetid: 3ee2f32b-02aa-420b-8990-e6aa5fc6bda3
ms.search.region: global
ms.author: panolte
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: f0e01881a6b68526479d27014d49a718069cffc9
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/01/2021
ms.locfileid: "5815887"
---
# <a name="bank-statement-file-import-troubleshooting"></a><span data-ttu-id="35e29-107">口座取引明細書ファイルのインポートのトラブルシューティング</span><span class="sxs-lookup"><span data-stu-id="35e29-107">Bank statement file import troubleshooting</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="35e29-108">銀行からの口座取引明細書ファイルが、Microsoft Dynamics 365 Finance がサポートするレイアウトと一致することが重要です。</span><span class="sxs-lookup"><span data-stu-id="35e29-108">It's important that the bank statement file from the bank matches the layout that Microsoft Dynamics 365 Finance supports.</span></span> <span data-ttu-id="35e29-109">口座取引明細書の基準が厳しいために、ほとんどの統合が正しく動作します。</span><span class="sxs-lookup"><span data-stu-id="35e29-109">Because of strict standards for bank statements, most integrations will work correctly.</span></span> <span data-ttu-id="35e29-110">ただし、明細書ファイルがインポートできない場合または不正確な結果が含まれている場合があります。</span><span class="sxs-lookup"><span data-stu-id="35e29-110">However, sometimes the statement file can't be imported or has incorrect results.</span></span> <span data-ttu-id="35e29-111">通常、これらの問題は口座取引明細書ファイルの小さな差異によって引き起こされます。</span><span class="sxs-lookup"><span data-stu-id="35e29-111">Typically, these issues are caused by small differences in the bank statement file.</span></span> <span data-ttu-id="35e29-112">この記事は、これらの差異を修正し問題を解決する方法を説明します。</span><span class="sxs-lookup"><span data-stu-id="35e29-112">This article explains how to fix these differences and resolve the issues.</span></span>

<a name="what-is-the-error"></a><span data-ttu-id="35e29-113">エラーは何ですか?</span><span class="sxs-lookup"><span data-stu-id="35e29-113">What is the error?</span></span>
------------------

<span data-ttu-id="35e29-114">口座取引明細書ファイルのインポートを試行した後に、データ管理ジョブ履歴および実行の詳細に移動し、エラーを検索します。</span><span class="sxs-lookup"><span data-stu-id="35e29-114">After you try to import a bank statement file, go to the Data management job history and its execution details to find the error.</span></span> <span data-ttu-id="35e29-115">エラーは、明細書、残高、または明細行を指し示すのに役立ちます。</span><span class="sxs-lookup"><span data-stu-id="35e29-115">The error can help by pointing to the statement, balance, or statement line.</span></span> <span data-ttu-id="35e29-116">ただし、問題の原因となっているフィールドまたは要素を識別するために十分な情報を提供することは少ないです。</span><span class="sxs-lookup"><span data-stu-id="35e29-116">However, it's unlikely to provide enough information to help you identify the field or element that is causing the issue.</span></span>

> [!NOTE]
> <span data-ttu-id="35e29-117">インポートされた口座取引明細書は、単一時点でのみ重複できます。</span><span class="sxs-lookup"><span data-stu-id="35e29-117">Imported bank statements can overlap only for single a point in time.</span></span>  <span data-ttu-id="35e29-118">たとえば、2021 年 1 月 1 日の午前 12 時に終了する明細書の場合、次の明細書の開始日は、2021 年 1 月 1 日の午前 12 時です。</span><span class="sxs-lookup"><span data-stu-id="35e29-118">For example, if a statement ends at 12:00 AM on January 1, 2021, then beginning date for the next statement can be 12:00 AM on Jarnuary 1, 2021 12:00:00 AM.</span></span>

## <a name="what-are-the-differences"></a><span data-ttu-id="35e29-119">差異は何ですか?</span><span class="sxs-lookup"><span data-stu-id="35e29-119">What are the differences?</span></span>
<span data-ttu-id="35e29-120">銀行ファイル レイアウト定義を Finance のインポート定義と比較し、フィールドおよび要素の差異を確認します。</span><span class="sxs-lookup"><span data-stu-id="35e29-120">Compare the bank file layout definition to the Finance import definition, and note any differences in the fields and elements.</span></span> <span data-ttu-id="35e29-121">口座取引明細書ファイルを関連する Finance ファイルのサンプルと比較します。</span><span class="sxs-lookup"><span data-stu-id="35e29-121">Compare the bank statement file to the related sample Finance file.</span></span> <span data-ttu-id="35e29-122">ISO20022 ファイルでは、差異が一目で分かります。</span><span class="sxs-lookup"><span data-stu-id="35e29-122">In the ISO20022 files, any differences should be easy to see.</span></span>

## <a name="time-zone-differences-on-imported-bank-statements"></a><span data-ttu-id="35e29-123">インポートされた口座取引明細書のタイム ゾーンの違い</span><span class="sxs-lookup"><span data-stu-id="35e29-123">Time zone differences on imported bank statements</span></span>
<span data-ttu-id="35e29-124">インポート ファイルの日付と時刻の値は、Finance and Operations で表示される日付と時刻の値とは異なる場合があります。</span><span class="sxs-lookup"><span data-stu-id="35e29-124">The date-time values in the import file can differ from the date-time values that are shown in Finance and Operations.</span></span> <span data-ttu-id="35e29-125">この不一致を回避するには、**データ ソースの構成** ページでタイム ゾーンの設定を入力します。</span><span class="sxs-lookup"><span data-stu-id="35e29-125">To prevent this discrepancy, enter a time zone preference on the **Configure data sources** page.</span></span> <span data-ttu-id="35e29-126">タイム ゾーン参照の入力方法の詳細については、[詳細な銀行調整のインポート処理の設定](set-up-advanced-bank-reconciliation-import-process.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="35e29-126">For more information about entering a time zone preference, see [Set up the advanced bank reconciliation import process](set-up-advanced-bank-reconciliation-import-process.md).</span></span>

## <a name="transformations"></a><span data-ttu-id="35e29-127">変換</span><span class="sxs-lookup"><span data-stu-id="35e29-127">Transformations</span></span>
<span data-ttu-id="35e29-128">通常、変更は次の 3 つの変換のいずれかで行われます。</span><span class="sxs-lookup"><span data-stu-id="35e29-128">Typically, the change must be made in one of three transformations.</span></span> <span data-ttu-id="35e29-129">各変換は、指定された標準形式で書き込まれます。</span><span class="sxs-lookup"><span data-stu-id="35e29-129">Each transformation is written for a specific standard.</span></span>

| <span data-ttu-id="35e29-130">リソース名</span><span class="sxs-lookup"><span data-stu-id="35e29-130">Resource name</span></span>                                         | <span data-ttu-id="35e29-131">ファイル名</span><span class="sxs-lookup"><span data-stu-id="35e29-131">File name</span></span>                          |
|-------------------------------------------------------|------------------------------------|
| <span data-ttu-id="35e29-132">BankStmtImport\_BAI2CSV\_to\_BAI2XML\_xslt</span><span class="sxs-lookup"><span data-stu-id="35e29-132">BankStmtImport\_BAI2CSV\_to\_BAI2XML\_xslt</span></span>            | <span data-ttu-id="35e29-133">BAI2CSV-to-BAI2XML.xslt</span><span class="sxs-lookup"><span data-stu-id="35e29-133">BAI2CSV-to-BAI2XML.xslt</span></span>            |
| <span data-ttu-id="35e29-134">BankStmtImport\_ISO20022XML\_to\_Reconciliation\_xslt</span><span class="sxs-lookup"><span data-stu-id="35e29-134">BankStmtImport\_ISO20022XML\_to\_Reconciliation\_xslt</span></span> | <span data-ttu-id="35e29-135">ISO20022XML-to-Reconciliation.xslt</span><span class="sxs-lookup"><span data-stu-id="35e29-135">ISO20022XML-to-Reconciliation.xslt</span></span> |
| <span data-ttu-id="35e29-136">BankStmtImport\_MT940TXT\_to\_MT940XML\_xslt</span><span class="sxs-lookup"><span data-stu-id="35e29-136">BankStmtImport\_MT940TXT\_to\_MT940XML\_xslt</span></span>          | <span data-ttu-id="35e29-137">MT940TXT-to-MT940XML.xslt</span><span class="sxs-lookup"><span data-stu-id="35e29-137">MT940TXT-to-MT940XML.xslt</span></span>          |

## <a name="debugging-transformations"></a><span data-ttu-id="35e29-138">デバッグの変換</span><span class="sxs-lookup"><span data-stu-id="35e29-138">Debugging transformations</span></span>
### <a name="adjust-the-bai2-and-mt940-files"></a><span data-ttu-id="35e29-139">BAI2 と MT940 ファイルの調整</span><span class="sxs-lookup"><span data-stu-id="35e29-139">Adjust the BAI2 and MT940 files</span></span>

<span data-ttu-id="35e29-140">BAI2 と MT940 ファイルはテキスト ベースのファイルで、XSLT (Extensible Stylesheet Language Transformations) デバッグを有効にするためには調整が必要です。</span><span class="sxs-lookup"><span data-stu-id="35e29-140">The BAI2 and MT940 files are text-based files and require an adjustment to enable Extensible Stylesheet Language Transformations (XSLT) debugging.</span></span> <span data-ttu-id="35e29-141">プログラムは、ファイルのインポート時にこの調整を行います。</span><span class="sxs-lookup"><span data-stu-id="35e29-141">The program makes this adjustment when a file is imported.</span></span>

1.  <span data-ttu-id="35e29-142">XML ファイルを作成し、次のテキストをコピーします。</span><span class="sxs-lookup"><span data-stu-id="35e29-142">Create an XML file, and copy the following text into it.</span></span>

    ```xml
    <Batch><![CDATA[PASTESTATEMENTFILEHERE
        ]]></Batch>
    ```
    
2.  <span data-ttu-id="35e29-143">口座取引明細書ファイルの内容をコピーし、XML ファイルに貼り **PASTESTATEMENTFILEHERE** を置換します。</span><span class="sxs-lookup"><span data-stu-id="35e29-143">Copy the contents of the bank statement file, and paste them into the XML file so that they replace **PASTESTATEMENTFILEHERE**.</span></span>

### <a name="debug-the-xslt"></a><span data-ttu-id="35e29-144">XSLT のデバッグ</span><span class="sxs-lookup"><span data-stu-id="35e29-144">Debug the XSLT</span></span>

<span data-ttu-id="35e29-145">詳細については、「<https://msdn.microsoft.com/library/ms255605.aspx>」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="35e29-145">For more information, see <https://msdn.microsoft.com/library/ms255605.aspx>.</span></span>

1.  <span data-ttu-id="35e29-146">Microsoft Visual Studio を起動します。</span><span class="sxs-lookup"><span data-stu-id="35e29-146">Start Microsoft Visual Studio.</span></span>
2.  <span data-ttu-id="35e29-147">コンソール アプリケーションを作成します。</span><span class="sxs-lookup"><span data-stu-id="35e29-147">Create a console application.</span></span>
3.  <span data-ttu-id="35e29-148">適切な XSLT を開きます。</span><span class="sxs-lookup"><span data-stu-id="35e29-148">Open the appropriate XSLT.</span></span>
4.  <span data-ttu-id="35e29-149">XLST とプロパティ ページをクリックします。</span><span class="sxs-lookup"><span data-stu-id="35e29-149">Click the XLST and its properties page.</span></span>
5.  <span data-ttu-id="35e29-150">口座取引明細書ファイルの場所の入力を設定します。</span><span class="sxs-lookup"><span data-stu-id="35e29-150">Set the input to the location of the bank statement file.</span></span>
6.  <span data-ttu-id="35e29-151">出力の場所とファイル名を定義します。</span><span class="sxs-lookup"><span data-stu-id="35e29-151">Define a location and file name for the output.</span></span>
7.  <span data-ttu-id="35e29-152">必要な区切り点を設定します。</span><span class="sxs-lookup"><span data-stu-id="35e29-152">Set the required break points.</span></span>
8.  <span data-ttu-id="35e29-153">メニューで、**XML** &gt; **XSLT デバッグの開始** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="35e29-153">On the menu, click **XML** &gt; **Start XSLT Debugging**.</span></span>

### <a name="format-the-xslt-output"></a><span data-ttu-id="35e29-154">XSLT 出力の書式設定</span><span class="sxs-lookup"><span data-stu-id="35e29-154">Format the XSLT output</span></span>

<span data-ttu-id="35e29-155">変換を実行すると、Visual Studio で表示可能な出力ファイルを作成します。</span><span class="sxs-lookup"><span data-stu-id="35e29-155">When the transformation runs, it creates an output file that you can view in Visual Studio.</span></span> <span data-ttu-id="35e29-156">Ctrl+A、Ctrl+K と Ctrl+D を使用して、出力ファイルをすばやく書式設定します。</span><span class="sxs-lookup"><span data-stu-id="35e29-156">Use Ctrl+A, Ctrl+K, and Ctrl+D to quickly format the output file.</span></span>

### <a name="adjust-the-transformation"></a><span data-ttu-id="35e29-157">変換の調整</span><span class="sxs-lookup"><span data-stu-id="35e29-157">Adjust the transformation</span></span>

<span data-ttu-id="35e29-158">口座取引明細書ファイルの適切なフィールドまたは要素を得るために変換を調整します。</span><span class="sxs-lookup"><span data-stu-id="35e29-158">Adjust the transformation to get the appropriate field or element in the bank statement file.</span></span> <span data-ttu-id="35e29-159">次に適切な Finance の要素にそのフィールドまたは要素をマップします。</span><span class="sxs-lookup"><span data-stu-id="35e29-159">Then map that field or element to the appropriate Finance element.</span></span>

### <a name="debitcredit-indicator"></a><span data-ttu-id="35e29-160">借方/貸方インジケーター</span><span class="sxs-lookup"><span data-stu-id="35e29-160">Debit/credit indicator</span></span>

<span data-ttu-id="35e29-161">場合によっては、借方は貸方としてインポートされ、貸方が借方としてインポートされる場合があります。</span><span class="sxs-lookup"><span data-stu-id="35e29-161">Sometimes, debits might be imported as credits, and credits might be imported as debits.</span></span> <span data-ttu-id="35e29-162">この問題を解決するには、適切な XSLT を変更する必要があります。</span><span class="sxs-lookup"><span data-stu-id="35e29-162">To resolve this issue, you must change the appropriate XSLT.</span></span> <span data-ttu-id="35e29-163">口座取引明細書を複数の銀行から取得する場合、すべてが同じ借方/貸方を使用しているか、または別の変換を作成していることを確認してください。</span><span class="sxs-lookup"><span data-stu-id="35e29-163">If bank statements come from multiple banks, make sure that they all use the same debit/credit approach, or create separate transformations.</span></span>

-   <span data-ttu-id="35e29-164">BAI2XML-to-Reconciliation.xlst GetAmountCreditDebitIndicator テンプレート</span><span class="sxs-lookup"><span data-stu-id="35e29-164">BAI2XML-to-Reconciliation.xlst GetAmountCreditDebitIndicator template</span></span>
-   <span data-ttu-id="35e29-165">ISO20022XML-to-Reconcilation.xslt GetCreditDebit テンプレート</span><span class="sxs-lookup"><span data-stu-id="35e29-165">ISO20022XML-to-Reconcilation.xslt GetCreditDebit template</span></span>
-   <span data-ttu-id="35e29-166">MT940XML-to-Reconcilation.xslt GetCreditDebitIndicator テンプレート</span><span class="sxs-lookup"><span data-stu-id="35e29-166">MT940XML-to-Reconcilation.xslt GetCreditDebitIndicator template</span></span>

## <a name="examples-of-bank-statement-formats-and-technical-layouts"></a><span data-ttu-id="35e29-167">口座取引明細書の形式と技術的な配置の例</span><span class="sxs-lookup"><span data-stu-id="35e29-167">Examples of bank statement formats and technical layouts</span></span>
<span data-ttu-id="35e29-168">次の表は、詳細な口座調整のインポート ファイルの技術的な配置の定義、および 3 つの関連する口座取引明細書のサンプル ファイルの一覧を表示します。</span><span class="sxs-lookup"><span data-stu-id="35e29-168">The following table lists examples of the technical layout definitions for advanced bank reconciliation import files and three related bank statement example files.</span></span> <span data-ttu-id="35e29-169">サンプル ファイルと技術的な配置はここでダウンロードできます: [サンプル ファイルのインポート](//download.microsoft.com/download/8/e/c/8ec8d2d0-eb8c-41fb-ad8c-f01a4d670a44/Dynamics365FinanceAdvancedBankStatementLayouts.xlsx)</span><span class="sxs-lookup"><span data-stu-id="35e29-169">You can download the example files and technical layouts here: [Import file examples](//download.microsoft.com/download/8/e/c/8ec8d2d0-eb8c-41fb-ad8c-f01a4d670a44/Dynamics365FinanceAdvancedBankStatementLayouts.xlsx)</span></span>  

| <span data-ttu-id="35e29-170">技術的なレイアウトの定義</span><span class="sxs-lookup"><span data-stu-id="35e29-170">Technical layout definition</span></span>                             | <span data-ttu-id="35e29-171">口座取引明細書のサンプル ファイル</span><span class="sxs-lookup"><span data-stu-id="35e29-171">Bank statement example file</span></span>          |
|---------------------------------------------------------|--------------------------------------|
| <span data-ttu-id="35e29-172">DynamicsAXMT940Layout</span><span class="sxs-lookup"><span data-stu-id="35e29-172">DynamicsAXMT940Layout</span></span>                                   | [<span data-ttu-id="35e29-173">MT940StatementExample</span><span class="sxs-lookup"><span data-stu-id="35e29-173">MT940StatementExample</span></span>](//download.microsoft.com/download/2/d/c/2dcc4e55-ddc8-4a74-b79c-250fae201c3c/mt940StatementExample.txt)                |
| <span data-ttu-id="35e29-174">DynamicsAXISO20022Layout</span><span class="sxs-lookup"><span data-stu-id="35e29-174">DynamicsAXISO20022Layout</span></span>                                | [<span data-ttu-id="35e29-175">ISO20022StatementExample</span><span class="sxs-lookup"><span data-stu-id="35e29-175">ISO20022StatementExample</span></span>](https://nam06.safelinks.protection.outlook.com/?url=https%3A%2F%2Fdownload.microsoft.com%2Fdownload%2F1%2F5%2F5%2F155d84ed-c250-48f3-b0b1-c5a431e7855b%2FISO20022-MultipleStatements.xml&data=04%7C01%7CRobert.Schlomann%40microsoft.com%7C30d0c233cb6546547d0a08d8f4965edc%7C72f988bf86f141af91ab2d7cd011db47%7C1%7C0%7C637528273956712775%7CUnknown%7CTWFpbGZsb3d8eyJWIjoiMC4wLjAwMDAiLCJQIjoiV2luMzIiLCJBTiI6Ik1haWwiLCJXVCI6Mn0%3D%7C1000&sdata=3VzvLZK%2BO8PjuI7XVdC6rD2j3nUJfteo7zFp%2B1s9BwM%3D&reserved=0)             |
| <span data-ttu-id="35e29-176">DynamicsAXBAI2Layout</span><span class="sxs-lookup"><span data-stu-id="35e29-176">DynamicsAXBAI2Layout</span></span>                                    | [<span data-ttu-id="35e29-177">BAI2StatementExample</span><span class="sxs-lookup"><span data-stu-id="35e29-177">BAI2StatementExample</span></span>](//download.microsoft.com/download/1/1/6/11693f57-bfc1-4993-a274-5fb978be70fa/BAI2StatementExample.txt)                 |







[!INCLUDE[footer-include](../../includes/footer-banner.md)]
