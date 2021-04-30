---
title: バーコードのイメージを生成するためにバーコード データソースを使用する
description: このトピックでは、バーコードのイメージを生成するためのバーコード データ ソースの使用方法について説明します。
author: NickSelin
ms.date: 10/21/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ERWorkspace, ERSolutionTable, ERModelMappingDesigner, EROperationDesigner
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.custom: 220314
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2020-05-01
ms.dyn365.ops.version: Version 10.0.13
ms.openlocfilehash: cbc2b5870e855ff4d4a099a51cbb6887dd30bba7
ms.sourcegitcommit: 951393b05bf409333cb3c7ad977bcaa804aa801b
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/13/2021
ms.locfileid: "5893555"
---
# <a name="use-barcode-data-sources-to-generate-bar-code-images"></a><span data-ttu-id="b2c76-103">バーコードのイメージを生成するためにバーコード データソースを使用する</span><span class="sxs-lookup"><span data-stu-id="b2c76-103">Use Barcode data sources to generate bar code images</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="b2c76-104">[電子レポート (ER)](general-electronic-reporting.md) フレームワークを使用すると、必要な電子形式または印刷可能な送信ドキュメントを生成するために実行できる [ER 形式コンポーネント](general-electronic-reporting.md#FormatComponentOutbound) をデザインできます。</span><span class="sxs-lookup"><span data-stu-id="b2c76-104">You can use the [Electronic reporting (ER)](general-electronic-reporting.md) framework to design [ER format components](general-electronic-reporting.md#FormatComponentOutbound) that you can run to generate electronic and printable outbound documents that you require.</span></span> <span data-ttu-id="b2c76-105">Microsoft Office 形式でで送信ドキュメントを生成するには、Microsoft Excel ドキュメントまたはレポート テンプレートとしての Microsoft Word ドキュメントのいずれかを使用することで、レポートのレイアウトを指定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="b2c76-105">To generate an outbound document in Microsoft Office format, you must specify the layout of the report by using either a Microsoft Excel document or a Microsoft Word document as a report template.</span></span> <span data-ttu-id="b2c76-106">[ER 操作デザイナー](general-electronic-reporting.md#building-a-format-that-uses-a-data-model-as-a-base) を使用すると、レポートのテンプレートとして Excel または Word ドキュメントを添付できます。</span><span class="sxs-lookup"><span data-stu-id="b2c76-106">The [ER Operations designer](general-electronic-reporting.md#building-a-format-that-uses-a-data-model-as-a-base) lets you attach an Excel or Word document as a template for an ER format.</span></span> <span data-ttu-id="b2c76-107">以下の添付されたテンプレートの名前付き要素は、次の構成済みの形式コンポーネントの要素に関連付けられます。</span><span class="sxs-lookup"><span data-stu-id="b2c76-107">The following named elements in the attached template are associated with the elements of the configured format component:</span></span>

- <span data-ttu-id="b2c76-108">Word のコンテンツ コントロール</span><span class="sxs-lookup"><span data-stu-id="b2c76-108">Content controls in Word</span></span>
- <span data-ttu-id="b2c76-109">Excel の名前指定シート、範囲、セル、図形、およびイメージ</span><span class="sxs-lookup"><span data-stu-id="b2c76-109">Named sheets, ranges, cells, shapes, and images in Excel</span></span>

<span data-ttu-id="b2c76-110">これらの名前指定要素は、ER 形式を実行したときに生成されるドキュメントに入力されるデータのプレース ホルダーとして使用されます。</span><span class="sxs-lookup"><span data-stu-id="b2c76-110">These named elements are used as placeholders for data that is entered in a generated document when an ER format is run.</span></span> <span data-ttu-id="b2c76-111">ER 形式要素は、データ ソースにバインドされます。</span><span class="sxs-lookup"><span data-stu-id="b2c76-111">ER format elements are bound to data sources.</span></span> <span data-ttu-id="b2c76-112">これらのデータ ソースは、実行時に生成されるドキュメントに入力されるデータを指定します。</span><span class="sxs-lookup"><span data-stu-id="b2c76-112">These data sources specify the data that will be entered in the generated documents at runtime.</span></span> <span data-ttu-id="b2c76-113">詳細については、[ER を使用して生成されるドキュメントへの画像や図形の埋め込み](electronic-reporting-embed-images-shapes.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="b2c76-113">For more information, see [Embed images and shapes in documents that you generate by using ER](electronic-reporting-embed-images-shapes.md).</span></span>

<span data-ttu-id="b2c76-114">ER は **バーコード** データ ソースの種類をサポートするようになりました。</span><span class="sxs-lookup"><span data-stu-id="b2c76-114">ER now supports the **Barcode** data source type.</span></span> <span data-ttu-id="b2c76-115">したがって、指定されたテキストのバーコードを表すイメージを生成できるようになりました。</span><span class="sxs-lookup"><span data-stu-id="b2c76-115">Therefore, you can now generate an image that represents the bar code for specified text.</span></span> <span data-ttu-id="b2c76-116">ER 形式を構成する場合は、**バーコード** の種類のイメージを生成するためのバーコードの種類のデータ ソースを指定できます。</span><span class="sxs-lookup"><span data-stu-id="b2c76-116">When you configure an ER format, you can specify data sources of the **Barcode** type to generate bar code images.</span></span> <span data-ttu-id="b2c76-117">その後、これらのイメージを、注文、請求書、梱包明細、領収書などの生成したビジネス ドキュメントに追加できます。</span><span class="sxs-lookup"><span data-stu-id="b2c76-117">You can then add those images to generated business documents, such as orders, invoices, packing slips, and receipts.</span></span> <span data-ttu-id="b2c76-118">また、製品ラベルや棚ラベル、梱包や出荷ラベルなど、さまざまな種類のラベルに追加することもできます。</span><span class="sxs-lookup"><span data-stu-id="b2c76-118">You can also add them to various kind of labels, such as product and shelf labels, and packaging and shipping labels.</span></span>

<span data-ttu-id="b2c76-119">次のプレースホルダーは、レポート テンプレートでバーコードのイメージを入力するために使用できます。</span><span class="sxs-lookup"><span data-stu-id="b2c76-119">The following placeholders can be used in report templates to enter bar code images:</span></span>

- <span data-ttu-id="b2c76-120">Wordの [画像](/office/client-developer/word/content-controls-in-word) コンテンツ コントロール</span><span class="sxs-lookup"><span data-stu-id="b2c76-120">[Picture](/office/client-developer/word/content-controls-in-word) content control for Word</span></span>
- <span data-ttu-id="b2c76-121">Excel の [画像](https://support.office.com/article/insert-pictures-3c51edf4-22e1-460a-b372-9329a8724344) オブジェクト</span><span class="sxs-lookup"><span data-stu-id="b2c76-121">[Picture](https://support.office.com/article/insert-pictures-3c51edf4-22e1-460a-b372-9329a8724344) object in Excel</span></span>

<span data-ttu-id="b2c76-122">**バーコード** タイプのデータ ソースを使用すると、次の形式でバーコードを生成できます。</span><span class="sxs-lookup"><span data-stu-id="b2c76-122">By using a data source of the **Barcode** type, you can generate bar codes in the following formats:</span></span>

- <span data-ttu-id="b2c76-123">1 次元バーコード。</span><span class="sxs-lookup"><span data-stu-id="b2c76-123">One-dimensional bar codes:</span></span>

    - <span data-ttu-id="b2c76-124">Codabar</span><span class="sxs-lookup"><span data-stu-id="b2c76-124">Codabar</span></span>
    - <span data-ttu-id="b2c76-125">Code 39</span><span class="sxs-lookup"><span data-stu-id="b2c76-125">Code 39</span></span>
    - <span data-ttu-id="b2c76-126">Code 93</span><span class="sxs-lookup"><span data-stu-id="b2c76-126">Code 93</span></span>
    - <span data-ttu-id="b2c76-127">Code 128</span><span class="sxs-lookup"><span data-stu-id="b2c76-127">Code 128</span></span>
    - <span data-ttu-id="b2c76-128">EAN-8</span><span class="sxs-lookup"><span data-stu-id="b2c76-128">EAN-8</span></span>
    - <span data-ttu-id="b2c76-129">EAN-13</span><span class="sxs-lookup"><span data-stu-id="b2c76-129">EAN-13</span></span>
    - <span data-ttu-id="b2c76-130">ITF-14</span><span class="sxs-lookup"><span data-stu-id="b2c76-130">ITF-14</span></span>
    - <span data-ttu-id="b2c76-131">Intelligent Mail</span><span class="sxs-lookup"><span data-stu-id="b2c76-131">Intelligent Mail</span></span>
    - <span data-ttu-id="b2c76-132">MSI</span><span class="sxs-lookup"><span data-stu-id="b2c76-132">MSI</span></span>
    - <span data-ttu-id="b2c76-133">Plessey</span><span class="sxs-lookup"><span data-stu-id="b2c76-133">Plessey</span></span>
    - <span data-ttu-id="b2c76-134">PDF417</span><span class="sxs-lookup"><span data-stu-id="b2c76-134">PDF417</span></span>
    - <span data-ttu-id="b2c76-135">UPC-A</span><span class="sxs-lookup"><span data-stu-id="b2c76-135">UPC-A</span></span>
    - <span data-ttu-id="b2c76-136">UPC-E</span><span class="sxs-lookup"><span data-stu-id="b2c76-136">UPC-E</span></span>

- <span data-ttu-id="b2c76-137">2 次元バーコード。</span><span class="sxs-lookup"><span data-stu-id="b2c76-137">Two-dimensional bar codes:</span></span>

    - <span data-ttu-id="b2c76-138">Aztec</span><span class="sxs-lookup"><span data-stu-id="b2c76-138">Aztec</span></span>
    - <span data-ttu-id="b2c76-139">Data Matrix</span><span class="sxs-lookup"><span data-stu-id="b2c76-139">Data Matrix</span></span>
    - <span data-ttu-id="b2c76-140">QR コード</span><span class="sxs-lookup"><span data-stu-id="b2c76-140">QR Code</span></span>

<span data-ttu-id="b2c76-141">**バーコード** データソースを構成する場合、イメージの生成に使用される特定のレンダリング パラメータを定義できます。</span><span class="sxs-lookup"><span data-stu-id="b2c76-141">When you configure a **Barcode** data source, you can define specific rendering parameters that are used to generate an image:</span></span>

- <span data-ttu-id="b2c76-142">**幅** - バーコードの幅をピクセル単位で指定します。</span><span class="sxs-lookup"><span data-stu-id="b2c76-142">**Width** – Specify the bar code's width in pixels.</span></span> <span data-ttu-id="b2c76-143">**0** (ゼロ) の値は、既定の幅が使用されていることを示します。</span><span class="sxs-lookup"><span data-stu-id="b2c76-143">A value of **0** (zero) indicates that the default width is used.</span></span> <span data-ttu-id="b2c76-144">この意味は、形式によって異なる場合があります。</span><span class="sxs-lookup"><span data-stu-id="b2c76-144">The meaning can vary for different formats.</span></span>
- <span data-ttu-id="b2c76-145">**高さ** - バーコードの高さをピクセル単位で指定します。</span><span class="sxs-lookup"><span data-stu-id="b2c76-145">**Height** – Specify the bar code's height in pixels.</span></span> <span data-ttu-id="b2c76-146">**0** (ゼロ) の値は、既定の高さが使用されていることを示します。</span><span class="sxs-lookup"><span data-stu-id="b2c76-146">A value of **0** (zero) indicates that the default height is used.</span></span> <span data-ttu-id="b2c76-147">この意味は、形式によって異なる場合があります。</span><span class="sxs-lookup"><span data-stu-id="b2c76-147">The meaning can vary for different formats.</span></span>
- <span data-ttu-id="b2c76-148">**余白** - バーコードの余白のサイズをピクセル単位で指定します。</span><span class="sxs-lookup"><span data-stu-id="b2c76-148">**Margin** – Specify the size of the bar code's margin in pixels.</span></span> <span data-ttu-id="b2c76-149">この余白は、バーコードの両側の領域で、明確に保管する必要があります (quiet 領域)。</span><span class="sxs-lookup"><span data-stu-id="b2c76-149">The margin is the area on each side of a bar code that must be kept clear (quiet zone).</span></span> <span data-ttu-id="b2c76-150">**0** (ゼロ) の値は、既定の余白が使用されていることを示します。</span><span class="sxs-lookup"><span data-stu-id="b2c76-150">A value of **0** (zero) indicates that the default margin is used.</span></span> <span data-ttu-id="b2c76-151">この意味は、形式によって異なる場合があります。</span><span class="sxs-lookup"><span data-stu-id="b2c76-151">The meaning can vary for different formats.</span></span>
- <span data-ttu-id="b2c76-152">**出力コンテンツ** - この値を **はい** に設定すると、エンコードされた情報をテキストとして含むバーコードのイメージが生成されます。</span><span class="sxs-lookup"><span data-stu-id="b2c76-152">**Output content** – Set the value to **Yes** to generate a bar code image that contains the encoded information as text.</span></span> <span data-ttu-id="b2c76-153">既定値は **いいえ** です。</span><span class="sxs-lookup"><span data-stu-id="b2c76-153">The default value is **No**.</span></span>
- <span data-ttu-id="b2c76-154">**エンコーディング** - 生成されるバーコードのイメージでエンコードされる文字のタイプを指定します。</span><span class="sxs-lookup"><span data-stu-id="b2c76-154">**Encoding** – Specify the type of characters that are encoded in the generated bar code image.</span></span> <span data-ttu-id="b2c76-155">既定では、**UTF-8** エンコードが使用されます。</span><span class="sxs-lookup"><span data-stu-id="b2c76-155">By default, the **UTF-8** encoding is used.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="b2c76-156">新しい **バーコード** データソースを追加する場合は、入れ子になった要素として別の項目 (コンテナー) の下に配置する必要があります。</span><span class="sxs-lookup"><span data-stu-id="b2c76-156">When you add a new **Barcode** data source, you must place it under another item (container) as a nested element.</span></span>
>
> <span data-ttu-id="b2c76-157">**バーコード** データソースを形式のセル要素にバインドし、セル要素が Word コンテンツ コントロールまたは Excel ピクチャを表す場合、データソースは文字列型の 1 つのパラメーターを持つ **関数** としてバインドされます。</span><span class="sxs-lookup"><span data-stu-id="b2c76-157">When you bind a **Barcode** data source to a cell element in a format, and the cell element represents either a Word content control or an Excel picture, the data source is presented in that binding as a function that has a single parameter of the **String** type.</span></span> <span data-ttu-id="b2c76-158">このパラメータを使用して、バーコードのイメージに変換するテキストを指定し、生成されたバーコードをスキャンしたときに読み取るテキストを指定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="b2c76-158">You must use this parameter to specify the text that should be transformed into a bar code image and read when a generated bar code is scanned.</span></span>

<span data-ttu-id="b2c76-159">この機能の詳細を知るには、このトピックの例を実行します。</span><span class="sxs-lookup"><span data-stu-id="b2c76-159">For more information about this feature, complete the examples in this topic.</span></span>

## <a name="example-generate-a-payment-check-that-contains-a-bar-code-that-encodes-the-payable-amount"></a><span data-ttu-id="b2c76-160">例: 未払金額をエンコードするバーコードを含む支払小切手を生成する</span><span class="sxs-lookup"><span data-stu-id="b2c76-160">Example: Generate a payment check that contains a bar code that encodes the payable amount</span></span>

<span data-ttu-id="b2c76-161">この例では、**システム管理者** または **電子レポート機能コンサルタント** のロールのユーザーが、バーコードが含まれる送信ドキュメントを Excel 形式で生成するために使用されるテンプレートを含む ER 形式を構成する方法を示します。</span><span class="sxs-lookup"><span data-stu-id="b2c76-161">This example shows how a user in the **System administrator** or **Electronic reporting functional consultant** role can configure an ER format that contains a template that is used to generate an outbound document in Excel format that contains a bar code.</span></span> <span data-ttu-id="b2c76-162">ここでは、関連する手順の概要を示します。</span><span class="sxs-lookup"><span data-stu-id="b2c76-162">Here is an overview of the steps that are involved.</span></span>

1. <span data-ttu-id="b2c76-163">[前提条件を満たします](#ExamplePrerequisites)。</span><span class="sxs-lookup"><span data-stu-id="b2c76-163">[Complete the prerequisites](#ExamplePrerequisites).</span></span>
2. <span data-ttu-id="b2c76-164">[構成プロバイダーをアクティブにします](#ExampleProvider)。</span><span class="sxs-lookup"><span data-stu-id="b2c76-164">[Activate a configuration provider](#ExampleProvider).</span></span>
3. <span data-ttu-id="b2c76-165">[指定された ER ソリューションを確認します](#ExampleImportSolution)。</span><span class="sxs-lookup"><span data-stu-id="b2c76-165">[Import the provided ER solution](#ExampleImportSolution).</span></span>
4. <span data-ttu-id="b2c76-166">[支払小切手を生成します](#ExampleGenerateCheque)。</span><span class="sxs-lookup"><span data-stu-id="b2c76-166">[Generate a payment check](#ExampleGenerateCheque).</span></span>
5. <span data-ttu-id="b2c76-167">[生成した支払い小切手をレビューします](#ExampleReviewGeneratedCheque)。</span><span class="sxs-lookup"><span data-stu-id="b2c76-167">[Review the generated payment check](#ExampleReviewGeneratedCheque).</span></span>
6. <span data-ttu-id="b2c76-168">[提供されている ER ソリューションの形式を変更します](#ExampleModifyFormat)。</span><span class="sxs-lookup"><span data-stu-id="b2c76-168">[Modify the format of the provided ER solution](#ExampleModifyFormat).</span></span>

    1. <span data-ttu-id="b2c76-169">[新しい小切手テンプレートを適用します](#ExampleModifyFormatApplyTemplate)。</span><span class="sxs-lookup"><span data-stu-id="b2c76-169">[Apply a new check template](#ExampleModifyFormatApplyTemplate).</span></span>
    2. <span data-ttu-id="b2c76-170">[新しいバーコード データ ソースを追加する](#ExampleModifyFormatAddDataSource)。</span><span class="sxs-lookup"><span data-stu-id="b2c76-170">[Add a new Barcode data source](#ExampleModifyFormatAddDataSource).</span></span>
    3. <span data-ttu-id="b2c76-171">[新しい形式要素をバインドする](#ExampleModifyFormatBindFormatElement)。</span><span class="sxs-lookup"><span data-stu-id="b2c76-171">[Bind a new format element](#ExampleModifyFormatBindFormatElement).</span></span>
    4. <span data-ttu-id="b2c76-172">[変更したバージョンをテストの実行に使用できるようにする](#ExampleModifyFormatMakeVersionAvailable)。</span><span class="sxs-lookup"><span data-stu-id="b2c76-172">[Make the modified version available for test runs](#ExampleModifyFormatMakeVersionAvailable).</span></span>

        1. <span data-ttu-id="b2c76-173">[変更した形式のバージョンを完了します](#CompleteToRun)。</span><span class="sxs-lookup"><span data-stu-id="b2c76-173">[Complete the modified format version](#CompleteToRun).</span></span>
        2. <span data-ttu-id="b2c76-174">[下書きバージョンを使用できるようにする](#MarkToRun)。</span><span class="sxs-lookup"><span data-stu-id="b2c76-174">[Make the draft version available for use](#MarkToRun).</span></span>

7. <span data-ttu-id="b2c76-175">[支払ファイルを生成します](#ExampleGenerateCheque2)。</span><span class="sxs-lookup"><span data-stu-id="b2c76-175">[Generate a payment check](#ExampleGenerateCheque2).</span></span>
8. <span data-ttu-id="b2c76-176">[生成した小切手を PDF に変換します](#ExampleConvertToPDF)。</span><span class="sxs-lookup"><span data-stu-id="b2c76-176">[Convert the generated check to a PDF](#ExampleConvertToPDF).</span></span>

<span data-ttu-id="b2c76-177">この例では、支払チェックを生成するように構成されている、提供される ER ソリューションを使用します。</span><span class="sxs-lookup"><span data-stu-id="b2c76-177">In this example, you will use the provided ER solution that has been configured to generate payment checks.</span></span> <span data-ttu-id="b2c76-178">このソリューションでは、支払額が数字とテキストの両方で書き込まれている支払小切手が生成されます。</span><span class="sxs-lookup"><span data-stu-id="b2c76-178">This solution generates payment checks where the payable amount is written both as a number and as text.</span></span> <span data-ttu-id="b2c76-179">この ER ソリューションを変更して、支払金額がエンコードされ、バーコード スキャナーを使用して読み取ることができる、生成されたバーコードも確認できるようにします。</span><span class="sxs-lookup"><span data-stu-id="b2c76-179">You will modify this ER solution so that the check also includes a generated bar code where the payable amount is encoded and can be read by using a bar code scanner.</span></span>

<span data-ttu-id="b2c76-180">これらのステップは、Microsoft Dynamics 365 Finance の **USMF** 会社で完了できます。</span><span class="sxs-lookup"><span data-stu-id="b2c76-180">The steps can be completed in the **USMF** company in Microsoft Dynamics 365 Finance.</span></span>

### <a name="complete-the-prerequisites"></a><a name="ExamplePrerequisites"></a><span data-ttu-id="b2c76-181">前提条件を満たす</span><span class="sxs-lookup"><span data-stu-id="b2c76-181">Complete the prerequisites</span></span>

<span data-ttu-id="b2c76-182">この例を完了するには、次のいずれかのロール用の Finance の USMF 会社にアクセスできる必要があります。</span><span class="sxs-lookup"><span data-stu-id="b2c76-182">To complete this example, you must have access to the USMF company in Finance for one of the following roles:</span></span>

- <span data-ttu-id="b2c76-183">電子申告機能コンサルタント</span><span class="sxs-lookup"><span data-stu-id="b2c76-183">Electronic reporting functional consultant</span></span>
- <span data-ttu-id="b2c76-184">システム管理者</span><span class="sxs-lookup"><span data-stu-id="b2c76-184">System administrator</span></span>

<span data-ttu-id="b2c76-185">[ER を使用して生成したドキュメントの埋め込まれたイメージと形状](electronic-reporting-embed-images-shapes.md) のトピックにある例をまだ完了していない場合は、次のサンプル ER の構成をダウンロードしてください。</span><span class="sxs-lookup"><span data-stu-id="b2c76-185">If you haven't yet completed the example in the [Embed images and shapes in documents that you generate by using ER](electronic-reporting-embed-images-shapes.md) topic, download the following configurations of the sample ER solution.</span></span>

| <span data-ttu-id="b2c76-186">コンテンツの説明</span><span class="sxs-lookup"><span data-stu-id="b2c76-186">Content description</span></span>         | <span data-ttu-id="b2c76-187">ファイル名</span><span class="sxs-lookup"><span data-stu-id="b2c76-187">File name</span></span>                   |
|-----------------------------|-----------------------------|
| <span data-ttu-id="b2c76-188">ER データ モデル構成</span><span class="sxs-lookup"><span data-stu-id="b2c76-188">ER data model configuration</span></span> | <span data-ttu-id="b2c76-189">cheques.xml 用のモデル</span><span class="sxs-lookup"><span data-stu-id="b2c76-189">Model for cheques.xml</span></span>       |
| <span data-ttu-id="b2c76-190">ER フォーマット構成</span><span class="sxs-lookup"><span data-stu-id="b2c76-190">ER format configuration</span></span>     | <span data-ttu-id="b2c76-191">format.xml を印刷する小切手</span><span class="sxs-lookup"><span data-stu-id="b2c76-191">Cheques printing format.xml</span></span> |

<span data-ttu-id="b2c76-192">さらに、提供されている ER ソリューション用に変更されたテンプレートを含む次の Excel ファイルをダウンロードします。</span><span class="sxs-lookup"><span data-stu-id="b2c76-192">Additionally, download the following Excel file that contains the modified template for the provided ER solution.</span></span>

| <span data-ttu-id="b2c76-193">コンテンツの説明</span><span class="sxs-lookup"><span data-stu-id="b2c76-193">Content description</span></span> | <span data-ttu-id="b2c76-194">ファイル名</span><span class="sxs-lookup"><span data-stu-id="b2c76-194">File name</span></span>                 |
|---------------------|---------------------------|
| <span data-ttu-id="b2c76-195">レポート テンプレート</span><span class="sxs-lookup"><span data-stu-id="b2c76-195">Report template</span></span>     | <span data-ttu-id="b2c76-196">テンプレート Excel .xlsx をチェックする</span><span class="sxs-lookup"><span data-stu-id="b2c76-196">Check template Excel.xlsx</span></span> |

### <a name="activate-a-configuration-provider"></a><a name="ExampleProvider"></a><span data-ttu-id="b2c76-197">コンフィギュレーション プロバイダーの有効化</span><span class="sxs-lookup"><span data-stu-id="b2c76-197">Activate a configuration provider</span></span>

1. <span data-ttu-id="b2c76-198">**組織管理** \> **ワークスペース** \> **電子申告** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="b2c76-198">Go to **Organization administration** \> **Workspaces** \> **Electronic reporting**.</span></span>
2. <span data-ttu-id="b2c76-199">**ローカライズ構成** ページの、**構成プロバイダー** セクションで、**Litware, Inc.** サンプル会社の [構成プロバイダー](general-electronic-reporting.md#Provider) がリストされ、アクティブとしてマークされていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="b2c76-199">On the **Localization configurations** page, in the **Configuration providers** section, make sure that the [configuration provider](general-electronic-reporting.md#Provider) for the **Litware, Inc.** sample company is listed, and that it's marked as active.</span></span> <span data-ttu-id="b2c76-200">この構成プロバイダーがリストに表示されない場合、またはアクティブとしてマークされていない場合、[構成プロバイダーの作成およびアクティブなプロバイダーとしてのマークする](tasks/er-configuration-provider-mark-it-active-2016-11.md) トピックの手順に従ってください。</span><span class="sxs-lookup"><span data-stu-id="b2c76-200">If it isn't listed, or if it isn't marked as active, follow the steps in the [Create a configuration provider and mark it as active](tasks/er-configuration-provider-mark-it-active-2016-11.md) topic.</span></span>

![ローカライズ構成ページで、サンプル会社をアクティブにする設定](./media/er-barcode-data-source-active-provider.png)

### <a name="import-the-provided-er-solution"></a><a name="ExampleImportSolution"></a><span data-ttu-id="b2c76-202">指定された ER ソリューションをインポートする</span><span class="sxs-lookup"><span data-stu-id="b2c76-202">Import the provided ER solution</span></span>

1. <span data-ttu-id="b2c76-203">**組織管理** \> **ワークスペース** \> **電子申告** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="b2c76-203">Go to **Organization administration** \> **Workspaces** \> **Electronic reporting**.</span></span>
2. <span data-ttu-id="b2c76-204">**ローカライズ構成** ページの、**構成** セクションで、**レポート構成** タイルを選択します。</span><span class="sxs-lookup"><span data-stu-id="b2c76-204">On the **Localization configurations** page, in the **Configurations** section, select the **Reporting configurations** tile.</span></span>
3. <span data-ttu-id="b2c76-205">**構成** ページで、**小切手のモデル** 構成が構成ツリーで使用できない場合、ER データ モデル構成をインポートするためにこれらのステップに従います。</span><span class="sxs-lookup"><span data-stu-id="b2c76-205">On the **Configurations** page, if the **Model for cheques** configuration isn't available in the configuration tree, follow these steps to import the ER data model configuration:</span></span>

    1. <span data-ttu-id="b2c76-206">操作ウィンドウで、**交換** \> **XML ファイルからロード** を選択します。</span><span class="sxs-lookup"><span data-stu-id="b2c76-206">On the Action Pane, select **Exchange** \> **Load from XML file**.</span></span>
    2. <span data-ttu-id="b2c76-207">ダイアログ ボックスで、**参照** を選択して、**cheques.xml のモデル** ファイルを見つけて選択し、**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="b2c76-207">In the dialog box, select **Browse**, find and select the **Model for cheques.xml** file, and then select **OK**.</span></span>

4. <span data-ttu-id="b2c76-208">**小切手の印刷形式** 構成は構成ツリーで使用できない場合、これらのステップに従って ER 形式の構成をインポートします。</span><span class="sxs-lookup"><span data-stu-id="b2c76-208">If the **Cheques printing format** configuration isn't available in the configuration tree, follow these steps to import the ER format configuration:</span></span>

    1. <span data-ttu-id="b2c76-209">操作ウィンドウで、**交換** \> **XML ファイルからロード** を選択します。</span><span class="sxs-lookup"><span data-stu-id="b2c76-209">On the Action Pane, select **Exchange** \> **Load from XML file**.</span></span>
    2. <span data-ttu-id="b2c76-210">ダイアログ ボックスで、**参照** を選択して、**小切手印刷のformat.xml** ファイルを見つけて選択して、**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="b2c76-210">In the dialog box, select **Browse**, find and select the **Cheques printing format.xml** file, and then select **OK**.</span></span>

5. <span data-ttu-id="b2c76-211">構成ツリーで、**小切手のモデル** を展開します。</span><span class="sxs-lookup"><span data-stu-id="b2c76-211">In the configuration tree, expand **Model for cheques**.</span></span>
6. <span data-ttu-id="b2c76-212">コンフィギュレーション ツリーでインポートされた ER コンフィギュレーションのリストを確認します。</span><span class="sxs-lookup"><span data-stu-id="b2c76-212">Review the list of imported ER configurations in the configuration tree.</span></span>

### <a name="generate-a-payment-check"></a><a name="ExampleGenerateCheque"></a><span data-ttu-id="b2c76-213">支払小切手を生成する</span><span class="sxs-lookup"><span data-stu-id="b2c76-213">Generate a payment check</span></span>

1. <span data-ttu-id="b2c76-214">**現金および銀行管理** \> **銀行口座** \> **銀行口座** に移動します。</span><span class="sxs-lookup"><span data-stu-id="b2c76-214">Go to **Cash and bank management** \> **Bank accounts** \> **Bank accounts**.</span></span>
2. <span data-ttu-id="b2c76-215">**銀行口座** ページで、**USMF OPER** アカウントを選択します。</span><span class="sxs-lookup"><span data-stu-id="b2c76-215">On the **Bank accounts** page, select the **USMF OPER** account.</span></span>
3. <span data-ttu-id="b2c76-216">[銀行口座の詳細] ページの操作ウィンドウで、**セットアップ** タブの **レイアウト** グループで、**小切手** を選択します。</span><span class="sxs-lookup"><span data-stu-id="b2c76-216">On the bank account details page, on the Action Pane, on the **Set up** tab, in the **Layout** group, select **Check**.</span></span>
4. <span data-ttu-id="b2c76-217">**小切手のレイアウト** ページで、**編集** を選択します。</span><span class="sxs-lookup"><span data-stu-id="b2c76-217">On the **Check layout** page, select **Edit**.</span></span>
5. <span data-ttu-id="b2c76-218">**一般** のクイック タブで、**一般的な電子エクスポート形式** のオプションを **はい** に設定します。</span><span class="sxs-lookup"><span data-stu-id="b2c76-218">On the **General** FastTab, set the **Generic electronic Export format** option to **Yes**.</span></span>
6. <span data-ttu-id="b2c76-219">**エクスポート形式の構成** フィールドで、前にインポートした **小切手印刷形式の** ER形式を選択します。</span><span class="sxs-lookup"><span data-stu-id="b2c76-219">In the **Export format configuration** field, select the **Cheques printing format** ER format that you imported earlier.</span></span>
7. <span data-ttu-id="b2c76-220">操作ウィンドウで、**印刷テスト** を選択します。</span><span class="sxs-lookup"><span data-stu-id="b2c76-220">On the Action Pane, select **Print test**.</span></span>
8. <span data-ttu-id="b2c76-221">ダイアログ ボックスで、**流通小切手形式** オプションを **はい** に設定し、**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="b2c76-221">In the dialog box, set the **Negotiable check format** option to **Yes**, and then select **OK**.</span></span>

    ![レイアウトの確認 - 印刷テストのダイアログ ボックス](./media/er-barcode-data-source-check-layout.png)

### <a name="review-the-generated-payment-check"></a><a name="ExampleReviewGeneratedCheque"></a><span data-ttu-id="b2c76-223">生成された支払い小切手をレビューする</span><span class="sxs-lookup"><span data-stu-id="b2c76-223">Review the generated payment check</span></span>

- <span data-ttu-id="b2c76-224">生成された小切手を Excel で開きます。</span><span class="sxs-lookup"><span data-stu-id="b2c76-224">Open the generated check in Excel.</span></span>
2. <span data-ttu-id="b2c76-225">生成した小切手をレビューします。</span><span class="sxs-lookup"><span data-stu-id="b2c76-225">Review the generated check.</span></span>

    ![生成された支払い小切手を Excel で開く](./media/er-barcode-data-source-cheque1.png)

### <a name="modify-the-format-of-the-provided-er-solution"></a><a name="ExampleModifyFormat"></a><span data-ttu-id="b2c76-227">提供されている ER ソリューションの形式を変更する</span><span class="sxs-lookup"><span data-stu-id="b2c76-227">Modify the format of the provided ER solution</span></span>

#### <a name="apply-a-new-check-template"></a><a name="ExampleModifyFormatApplyTemplate"></a><span data-ttu-id="b2c76-228">新しい小切手テンプレートを適用する</span><span class="sxs-lookup"><span data-stu-id="b2c76-228">Apply a new check template</span></span>

<span data-ttu-id="b2c76-229">Excel デスクトップ アプリケーションを使用して、前にインポートした **小切手テンプレートのExcel .xlsx** ファイルを開きます。</span><span class="sxs-lookup"><span data-stu-id="b2c76-229">You can use the Excel desktop application to open the **Cheque template Excel.xlsx** file that you imported earlier.</span></span> <span data-ttu-id="b2c76-230">このテンプレートは、提供されている ER ソリューションで支払チェックを生成するために使用したテンプレートとは異なることに注意してください。</span><span class="sxs-lookup"><span data-stu-id="b2c76-230">Notice that this template differs from the template that you used to generate a payment check in the provided ER solution.</span></span> <span data-ttu-id="b2c76-231">さらに、バーコード イメージの **AmountBarcode** 要素も含まれます。</span><span class="sxs-lookup"><span data-stu-id="b2c76-231">In addition, it includes an **AmountBarcode** element for the bar code image.</span></span>

![Excel テンプレートの AmountBarcode 要素](./media/er-barcode-data-source-cheque2.png)

<span data-ttu-id="b2c76-233">ER ソリューションを変更してから、変更したテンプレートを[再度適用](modify-electronic-reporting-format-reapply-excel-template.md) する必要があります。</span><span class="sxs-lookup"><span data-stu-id="b2c76-233">You must now modify the ER solution and then [reapply](modify-electronic-reporting-format-reapply-excel-template.md) the modified template.</span></span>

1. <span data-ttu-id="b2c76-234">**組織管理** \> **ワークスペース** \> **電子申告** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="b2c76-234">Go to **Organization administration** \> **Workspaces** \> **Electronic reporting**.</span></span>
2. <span data-ttu-id="b2c76-235">**ローカライズ構成** ページの、**構成** セクションで、**レポートの構成** タイルを選択します。</span><span class="sxs-lookup"><span data-stu-id="b2c76-235">On the **Localization configurations** page, in the **Configurations** section, select **Reporting configurations**.</span></span>
3. <span data-ttu-id="b2c76-236">**構成** ページの構成ツリーで、**小切手のモデル** を展開して、**小切手の印刷形式** を選択します。</span><span class="sxs-lookup"><span data-stu-id="b2c76-236">On the **Configurations** page, in the configuration tree, expand **Model for cheques**, and select **Cheques printing format**.</span></span>
4. <span data-ttu-id="b2c76-237">アクション ウィンドウで、**デザイナー** を選択します。</span><span class="sxs-lookup"><span data-stu-id="b2c76-237">On the Action Pane, select **Designer**.</span></span>
5. <span data-ttu-id="b2c76-238">ER 運営デザイナーで、**マッピング** タブを選択し、左側の形式ツリー ウィンドウで **展開/折りたたみ** を選択します。</span><span class="sxs-lookup"><span data-stu-id="b2c76-238">In the ER Operations designer, select the **Mapping** tab on the right side of the page, and then, in the format tree pane on the left, select **Expand/collapse**.</span></span>
6. <span data-ttu-id="b2c76-239">すべてのセル形式要素が適切なデータソースにバインドされていることに注意してください。</span><span class="sxs-lookup"><span data-stu-id="b2c76-239">Notice that all cell format elements are bound to the appropriate data sources.</span></span>

    ![ER 操作デザイナーにおけるセル形式要素のデータソースへのバインド](./media/er-barcode-data-source-cells-bound.png)

7. <span data-ttu-id="b2c76-241">ページの右側にあるバーで、**フォーマット** を選択します。</span><span class="sxs-lookup"><span data-stu-id="b2c76-241">Select the **Format** tab on the right side of the page.</span></span>
8. <span data-ttu-id="b2c76-242">操作ウィンドウで、省略記号 (**...**) を選択し、**インポート** を選択します。</span><span class="sxs-lookup"><span data-stu-id="b2c76-242">On the Action Pane, select the ellipsis (**...**), and then select **Import**.</span></span>
9. <span data-ttu-id="b2c76-243">**インポート** グループで、**Excelから更新** を選択し、**テンプレートの更新** を選択します。</span><span class="sxs-lookup"><span data-stu-id="b2c76-243">In the **Import** group, select **Update from Excel**, and then select **Update template**.</span></span>
10. <span data-ttu-id="b2c76-244">このダイアログ ボックスで、コンピュータに保存されている **小切手テンプレートの Excel .xlsx** ファイルを参照して選択し、**OK** を選択して、選択したテンプレートが適用されることを確認します。</span><span class="sxs-lookup"><span data-stu-id="b2c76-244">In the dialog box, browse to the **Cheque template Excel.xlsx** file that is saved on your computer, select it, and then select **OK** to confirm that the selected template should be applied.</span></span>
11. <span data-ttu-id="b2c76-245">ページの右側にある **マッピング** タブを選択し、左側の形式ツリー ウィンドウで **展開/折りたたみ** を選択します。</span><span class="sxs-lookup"><span data-stu-id="b2c76-245">Select the **Mapping** tab on the right side of the page, and then, in the format tree pane on the left, select **Expand/collapse**.</span></span>
12. <span data-ttu-id="b2c76-246">**AmountBarcode** セル要素が形式に追加されていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="b2c76-246">Notice that the **AmountBarcode** cell element has been added to the format.</span></span> <span data-ttu-id="b2c76-247">この要素は、変更された Excel テンプレートにバーコードの画像のプレースホルダーとして追加された **AmountBarcode** 要素に関連付けられています。</span><span class="sxs-lookup"><span data-stu-id="b2c76-247">This element is associated with the **AmountBarcode** element that has been added to the modified Excel template as a placeholder for a bar code image.</span></span>

    ![ER 操作デザイナーの形式に追加された AmountBarcode セル要素](./media/er-barcode-data-source-cell-added.png)

#### <a name="add-a-new-barcode-data-source"></a><a name="ExampleModifyFormatAddDataSource"></a><span data-ttu-id="b2c76-249">新しいバーコード データ ソースを追加する</span><span class="sxs-lookup"><span data-stu-id="b2c76-249">Add a new Barcode data source</span></span>

<span data-ttu-id="b2c76-250">次に、**バーコード** タイプの新しいデータソースを追加する必要があります。</span><span class="sxs-lookup"><span data-stu-id="b2c76-250">Next, you must add a new data source of the **Barcode** type.</span></span>

1. <span data-ttu-id="b2c76-251">ER 運営デザイナーで、ページの右側にある **マッピング** タブで、データソースの **印刷** を選択します。</span><span class="sxs-lookup"><span data-stu-id="b2c76-251">In the ER Operations designer, on the **Mapping** tab on the right side of the page, select the **print** data source.</span></span>
2. <span data-ttu-id="b2c76-252">**追加** をクリックし、**機能** グループで、**バーコード** データソース タイプを選択します。</span><span class="sxs-lookup"><span data-stu-id="b2c76-252">Select **Add**, and then, in the **Functions** group, select the **Barcode** data source type.</span></span>

    ![バーコード データソース タイプの選択](./media/er-barcode-data-source-add.png)

3. <span data-ttu-id="b2c76-254">ダイアログボックスで、**名前** フィールドに **バーコード** と入力します。</span><span class="sxs-lookup"><span data-stu-id="b2c76-254">In the dialog box, in the **Name** field, enter **barcode**.</span></span>
4. <span data-ttu-id="b2c76-255">**バーコード形式** で、**Code 128** を選択します。</span><span class="sxs-lookup"><span data-stu-id="b2c76-255">In the **Barcode format**, select **Code 128**.</span></span>
5. <span data-ttu-id="b2c76-256">**幅** フィールドに、**500** と入力します。</span><span class="sxs-lookup"><span data-stu-id="b2c76-256">In the **Width** field, enter **500**.</span></span>
6. <span data-ttu-id="b2c76-257">**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="b2c76-257">Select **OK**.</span></span>

    ![データ ソース プロパティ ダイアログ ボックス](./media/er-barcode-data-source-add2.png)

#### <a name="bind-a-new-format-element"></a><a name="ExampleModifyFormatBindFormatElement"></a><span data-ttu-id="b2c76-259">新規形式要素をバインドする</span><span class="sxs-lookup"><span data-stu-id="b2c76-259">Bind a new format element</span></span>

<span data-ttu-id="b2c76-260">次に、追加したデータ ソースに新しい形式要素をバインドする必要があります。</span><span class="sxs-lookup"><span data-stu-id="b2c76-260">Next, you must bind the new format element to the data source that you just added.</span></span>

1. <span data-ttu-id="b2c76-261">ER 運営デザイナーで、ページの右側にある **マッピング** タブで、**印刷\\バーコード** データ ソースを選択します。</span><span class="sxs-lookup"><span data-stu-id="b2c76-261">In the ER Operations designer, on the **Mapping** tab on the right side of the page, select the **print\\barcode** data source.</span></span>
2. <span data-ttu-id="b2c76-262">左にある書式ツリー ウィンドウで、**AmountBarcode** セル要素を選択して、**バインド** を選択します。</span><span class="sxs-lookup"><span data-stu-id="b2c76-262">In the format tree pane on the left, select the **AmountBarcode** cell element, and then select **Bind**.</span></span>
3. <span data-ttu-id="b2c76-263">操作ウィンドウで、**詳細の表示** を選択します。</span><span class="sxs-lookup"><span data-stu-id="b2c76-263">On the Action Pane, select **Show details**.</span></span>
4. <span data-ttu-id="b2c76-264">**バーコード** データソースは、バインドでは 1 つのパラメータを含む関数として表されているため、バインド形式の要素の名前は、そのパラメータの引数として自動的に取得されます。</span><span class="sxs-lookup"><span data-stu-id="b2c76-264">Notice that, because the **Barcode** data source is represented in the binding as a function that contains a single parameter, the name of the bound format element has been automatically taken as the argument of that parameter.</span></span>

    ![ER オペレーション デザイナーのバーコード データソースの詳細](./media/er-barcode-data-source-bind1.png)

5. <span data-ttu-id="b2c76-266&quot;>**フォーミュラの編集** を選択してバインドを調整します。</span><span class=&quot;sxs-lookup&quot;><span data-stu-id=&quot;b2c76-266&quot;>Select **Edit formula** to adjust the binding.</span></span>

    <span data-ttu-id=&quot;b2c76-267&quot;>セル要素の名前を返さないようにします。</span><span class=&quot;sxs-lookup&quot;><span data-stu-id=&quot;b2c76-267&quot;>You don't want the name of the cell element to be returned.</span></span> <span data-ttu-id=&quot;b2c76-268&quot;>したがって、現在の小切手の未払金額を含むテキストを返す式を構成する必要があります。</span><span class=&quot;sxs-lookup&quot;><span data-stu-id=&quot;b2c76-268&quot;>Therefore, you must configure an expression that returns text that contains the payable amount of the current check.</span></span> <span data-ttu-id=&quot;b2c76-269&quot;>親 **ChequeLines** の範囲は **model.cheques** データソースにバインドされているため 、現在の小切手の未払金額は **実際の** でデータ型の **model.cheques.attributes.amount** フィールドで使用できます。</span><span class=&quot;sxs-lookup&quot;><span data-stu-id=&quot;b2c76-269&quot;>Because the parent **ChequeLines** range is bound to the **model.cheques** data source, the payable amount of the current check is available in the **model.cheques.attributes.amount** field of the **Real** data type.</span></span>

6. <span data-ttu-id=&quot;b2c76-270&quot;>**式** フィールドに、**print.barcode(NUMBERFORMAT(@.attributes.amount, &quot;F2"))** と入力します。</span><span class="sxs-lookup"><span data-stu-id="b2c76-270">In the **Formula** field, enter **print.barcode(NUMBERFORMAT(@.attributes.amount, "F2"))**.</span></span>
7. <span data-ttu-id="b2c76-271">**保存** を選択して、[ER 式デザイナー](general-electronic-reporting-formula-designer.md) を閉じます。</span><span class="sxs-lookup"><span data-stu-id="b2c76-271">Select **Save**, and then close the [ER Formula designer](general-electronic-reporting-formula-designer.md).</span></span>
8. <span data-ttu-id="b2c76-272">バインドが調整されていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="b2c76-272">Notice that the binding has been adjusted.</span></span>

    ![ER 操作デザイナーで調整されたバインド](./media/er-barcode-data-source-bind2.png)

9. <span data-ttu-id="b2c76-274">**保存** を選択して、ER 操作デザイナー を閉じます。</span><span class="sxs-lookup"><span data-stu-id="b2c76-274">Select **Save**, and then close the ER Operations designer.</span></span>

#### <a name="make-the-modified-version-available-for-test-runs"></a><a name="ExampleModifyFormatMakeVersionAvailable"></a><span data-ttu-id="b2c76-275">変更したバージョンをテストの実行に使用できるようにする</span><span class="sxs-lookup"><span data-stu-id="b2c76-275">Make the modified version available for test runs</span></span>

<span data-ttu-id="b2c76-276">既定では、ステータスが **完了済** および **共有** のバージョンのみが、ER 形式を実行したときに使用されます。</span><span class="sxs-lookup"><span data-stu-id="b2c76-276">By default, the only versions that have a status of **Completed** and **Shared** are used when you run an ER format.</span></span>

<span data-ttu-id="b2c76-277">変更が完了している場合は、現在の下書きバージョンを使用して作業を完了し、変更を使用できるようにしておくことができます。</span><span class="sxs-lookup"><span data-stu-id="b2c76-277">If you've finalized your changes, you can complete your work with the current draft version and make your changes available for use.</span></span> <span data-ttu-id="b2c76-278">手順については、この後の [変更された形式のバージョンの詳細](#CompleteToRun) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="b2c76-278">For instructions, see the [Complete the modified format version](#CompleteToRun) section that follows.</span></span>

<span data-ttu-id="b2c76-279">現在のドラフト バージョンで作業を続行するが、小切手を生成するために使用する必要がある場合は、実行するために下書きバージョンの形式を使用するように明示的に指定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="b2c76-279">If you want to continue to work with the current draft version, but you have to use it to generate checks, you must explicitly specify that you want to use the draft version of the format for execution.</span></span> <span data-ttu-id="b2c76-280">手順については、[ドラフト バージョンを使用できるようにする](#MarkToRun) セクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="b2c76-280">For instructions, see the [Make the draft version available for use](#MarkToRun) section.</span></span>

##### <a name="complete-the-modified-format-version"></a><a name="CompleteToRun"></a><span data-ttu-id="b2c76-281">変更した形式のバージョンを完了する</span><span class="sxs-lookup"><span data-stu-id="b2c76-281">Complete the modified format version</span></span>

1. <span data-ttu-id="b2c76-282">**組織管理** \> **ワークスペース** \> **電子申告** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="b2c76-282">Go to **Organization administration** \> **Workspaces** \> **Electronic reporting**.</span></span>
2. <span data-ttu-id="b2c76-283">**ローカライズ構成** ページの、**構成** セクションで、**レポートの構成** タイルを選択します。</span><span class="sxs-lookup"><span data-stu-id="b2c76-283">On the **Localization configurations** page, in the **Configurations** section, select **Reporting configurations**.</span></span>
3. <span data-ttu-id="b2c76-284">**構成** ページの構成ツリーで、**小切手のモデル** を展開して、**小切手の印刷形式** を選択します。</span><span class="sxs-lookup"><span data-stu-id="b2c76-284">On the **Configurations** page, in the configuration tree, expand **Model for cheques**, and select **Cheques printing format**.</span></span>
4. <span data-ttu-id="b2c76-285">**バージョン** クイック タブで、ステータスが **ドラフト** のレコードを選択します。</span><span class="sxs-lookup"><span data-stu-id="b2c76-285">On the **Versions** FastTab, select the record that has a status of **Draft**.</span></span>
5. <span data-ttu-id="b2c76-286">**ステータスの変更** を選択し、**完了** を選択します。</span><span class="sxs-lookup"><span data-stu-id="b2c76-286">Select **Change status**, and then select **Complete**.</span></span>
6. <span data-ttu-id="b2c76-287">ダイアログ ボックスで、**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="b2c76-287">In the dialog box, select **OK**.</span></span>

<span data-ttu-id="b2c76-288">現在のバージョンのステータスが、**下書き** から **完了** に変更され、**ドラフト** のステータスを持つ新しいバージョンが作成されます。</span><span class="sxs-lookup"><span data-stu-id="b2c76-288">The status of the current version is changed from **Draft** to **Completed**, and a new version that has a status of **Draft** is created.</span></span> <span data-ttu-id="b2c76-289">この新しい下書きバージョンを使用して、追加の変更を適用できます。</span><span class="sxs-lookup"><span data-stu-id="b2c76-289">You can use this new draft version to apply additional changes.</span></span>

##### <a name="make-the-draft-version-available-for-use"></a><a name="MarkToRun"></a><span data-ttu-id="b2c76-290">下書きバージョンを使用できるようにする</span><span class="sxs-lookup"><span data-stu-id="b2c76-290">Make the draft version available for use</span></span>

1. <span data-ttu-id="b2c76-291">**組織管理** \> **ワークスペース** \> **電子申告** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="b2c76-291">Go to **Organization administration** \> **Workspaces** \> **Electronic reporting**.</span></span>
2. <span data-ttu-id="b2c76-292">**ローカライズ構成** ページの、**構成** セクションで、**レポートの構成** タイルを選択します。</span><span class="sxs-lookup"><span data-stu-id="b2c76-292">On the **Localization configurations** page, in the **Configurations** section, select **Reporting configurations**.</span></span>
3. <span data-ttu-id="b2c76-293">**構成** ページの、操作ウィンドウ、**構成** タブ、**詳細設定** グループで、**ユーザー パラメーター** を選択します。</span><span class="sxs-lookup"><span data-stu-id="b2c76-293">On the **Configurations** page, on the Action Pane, in the **Configurations** tab, in the **Advance settings** group, select **User parameters**.</span></span>
4. <span data-ttu-id="b2c76-294">ダイアログ ボックスで、**実行設定** オプションを **はい** に設定し、**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="b2c76-294">In the dialog box, set the **Run setting** options to **Yes**, and then select **OK**.</span></span>
5. <span data-ttu-id="b2c76-295">構成ツリーで、**小切手のモデル** を展開して、**小切手の印刷形式** を選択します。</span><span class="sxs-lookup"><span data-stu-id="b2c76-295">In the configuration tree, expand **Model for cheques**, and select **Cheques printing format**.</span></span>
6. <span data-ttu-id="b2c76-296">**実行ドラフト** オプションを **はい** に設定します。</span><span class="sxs-lookup"><span data-stu-id="b2c76-296">Set the **Run draft** option to **Yes**.</span></span>
7. <span data-ttu-id="b2c76-297">**保存** を選択します。</span><span class="sxs-lookup"><span data-stu-id="b2c76-297">Select **Save**.</span></span>

<span data-ttu-id="b2c76-298">選択した形式を実行すると、選択した形式の下書きバージョンが使用可能としてマークされます。</span><span class="sxs-lookup"><span data-stu-id="b2c76-298">The draft version of the selected format is marked as available for use when the selected format is run.</span></span>

### <a name="generate-a-payment-check"></a><a name="ExampleGenerateCheque2"></a><span data-ttu-id="b2c76-299">支払小切手を生成する</span><span class="sxs-lookup"><span data-stu-id="b2c76-299">Generate a payment check</span></span>

1. <span data-ttu-id="b2c76-300">**現金および銀行管理** \> **銀行口座** \> **銀行口座** に移動します。</span><span class="sxs-lookup"><span data-stu-id="b2c76-300">Go to **Cash and bank management** \> **Bank accounts** \> **Bank accounts**.</span></span>
2. <span data-ttu-id="b2c76-301">**銀行口座** ページで、**USMF OPER** アカウントを選択します。</span><span class="sxs-lookup"><span data-stu-id="b2c76-301">On the **Bank accounts** page, select the **USMF OPER** account.</span></span>
3. <span data-ttu-id="b2c76-302">[銀行口座の詳細] ページの操作ウィンドウで、**セットアップ** タブの **レイアウト** グループで、**小切手** を選択します。</span><span class="sxs-lookup"><span data-stu-id="b2c76-302">On the bank account details page, on the Action Pane, on the **Set up** tab, in the **Layout** group, select **Check**.</span></span>
4. <span data-ttu-id="b2c76-303">**小切手のレイアウト** ページの操作ウィンドウで、**テストの印刷** を選択し ます。</span><span class="sxs-lookup"><span data-stu-id="b2c76-303">On the **Check layout** page, on the Action Pane, select **Print test**.</span></span>
5. <span data-ttu-id="b2c76-304">ダイアログ ボックスで、**流通小切手形式** オプションを **はい** に選択します。</span><span class="sxs-lookup"><span data-stu-id="b2c76-304">In the dialog box, set the **Negotiable check format** option to **Yes**.</span></span>
6. <span data-ttu-id="b2c76-305">**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="b2c76-305">Select **OK**.</span></span>
7. <span data-ttu-id="b2c76-306">生成した小切手をレビューします。</span><span class="sxs-lookup"><span data-stu-id="b2c76-306">Review the generated check.</span></span> <span data-ttu-id="b2c76-307">小切手の未払金額をエンコードするためのバーコードが生成されていることに注意してください。</span><span class="sxs-lookup"><span data-stu-id="b2c76-307">Notice that a bar code has been generated to encode the payable amount of the check.</span></span>

    ![Excel のバーコードで生成された支払小切手](./media/er-barcode-data-source-cheque3.png)

> [!IMPORTANT]
> <span data-ttu-id="b2c76-309">**バーコード** データ ソースに固有の適切な要件に、バーコード データ ソースの引数が準拠していない場合は、例外がスローされます。</span><span class="sxs-lookup"><span data-stu-id="b2c76-309">An exception is thrown if the argument of a **Barcode** data source doesn't comply with the appropriate requirements that are specific to the bar code format.</span></span> <span data-ttu-id="b2c76-310">たとえば、**バーコード** データ ソースが、指定されたテキストに [EAN 8](https://wikipedia.org/wiki/EAN-8) バーコードを生成するために呼び出された場合、テキストの長さが 7 文字を超えると例外がスローされます。</span><span class="sxs-lookup"><span data-stu-id="b2c76-310">For example, when the **Barcode** data source is called to generate an [EAN-8](https://wikipedia.org/wiki/EAN-8) bar code for the provided text, an exception is thrown if the length of the text exceeds seven characters.</span></span>

### <a name="convert-the-generated-check-to-a-pdf"></a><a name="ExampleConvertToPDF"></a><span data-ttu-id="b2c76-311">生成された小切手を PDF に変換する</span><span class="sxs-lookup"><span data-stu-id="b2c76-311">Convert the generated check to a PDF</span></span>

<span data-ttu-id="b2c76-312">[印刷可能な FTI 形式の生成](er-generate-printable-fti-forms.md#finland) に関するトピックで説明しているように、特殊フォントを使用して、生成されたドキュメントのバーコードを生成できます。</span><span class="sxs-lookup"><span data-stu-id="b2c76-312">As described in the [Generate printable FTI forms](er-generate-printable-fti-forms.md#finland) topic, you can use a special font to produce bar codes in a generated document.</span></span> <span data-ttu-id="b2c76-313">この場合、生成されたドキュメントの変換を追加すると、変換環境でそのフォントが使用できるかどうかによって異なる場合があります。</span><span class="sxs-lookup"><span data-stu-id="b2c76-313">In this case, additional transformations of the generated document might depend on the availability of that font in the transformation environment.</span></span> <span data-ttu-id="b2c76-314">たとえば、ドキュメントを PDF 形式に変換しようとしたり、フォントが欠落している環境でプレビューしたりすると、バーコードは正しく表示されません。</span><span class="sxs-lookup"><span data-stu-id="b2c76-314">For example, if you try to convert a document to PDF format or preview it in an environment where the font is missing, bar codes won't be rendered correctly.</span></span>

<span data-ttu-id="b2c76-315">ただし、**バーコード** データ ソースを使用してバーコードを作成する場合、これらのバーコードのレンダリングはフォントに依存しません。</span><span class="sxs-lookup"><span data-stu-id="b2c76-315">However, when you use the **Barcode** data source to produce bar codes, the rendering of those bar codes doesn't depend on any font.</span></span> <span data-ttu-id="b2c76-316">したがって、バーコードが含まれているドキュメントを PDF 形式に簡単に変換できます。</span><span class="sxs-lookup"><span data-stu-id="b2c76-316">Therefore, you can easily convert documents that contain the bar codes to PDF format.</span></span> <span data-ttu-id="b2c76-317">次の図は、構成済みの ER [出力先](electronic-reporting-destinations.md) の設定に基づいて、PDFに [変換された](electronic-reporting-destinations.md#OutputConversionToPDF) 、生成された支払小切手のプレビューを示しています。</span><span class="sxs-lookup"><span data-stu-id="b2c76-317">The following illustration shows the preview of a generated payment check that has been [converted](electronic-reporting-destinations.md#OutputConversionToPDF) to a PDF, based on the setting of the configured ER [destination](electronic-reporting-destinations.md).</span></span>

![支払小切手の PDF のプレビュー](./media/er-barcode-data-source-cheque4.png)

## <a name="limitations"></a><span data-ttu-id="b2c76-319">制限</span><span class="sxs-lookup"><span data-stu-id="b2c76-319">Limitations</span></span>

> [!NOTE]
> <span data-ttu-id="b2c76-320">生成されるバーコードのタイプによっては、固定の縦横比が使用されている場合があります。</span><span class="sxs-lookup"><span data-stu-id="b2c76-320">Some types of bar codes that are generated have a fixed aspect ratio.</span></span> <span data-ttu-id="b2c76-321">この動作は、**電子レポート フレームワーク機能で EPPlus ライブラリの使用を有効にする** 機能をオンにして、ER の Excel ドキュメントを操作している場合に理にかなっています。</span><span class="sxs-lookup"><span data-stu-id="b2c76-321">This behavior makes sense if you've turned on the **Enable usage of EPPlus library in Electronic reporting framework** feature to work with Excel documents in ER.</span></span> <span data-ttu-id="b2c76-322">この場合、縦横比がロックされたプレースホルダーにイメージが入力されます。</span><span class="sxs-lookup"><span data-stu-id="b2c76-322">In that case, an image is entered into a placeholder that has a locked aspect ratio.</span></span> <span data-ttu-id="b2c76-323">したがって、テンプレート内のプレースホルダーの寸法が入力された画像の比率に対応する場合、生成されたドキュメントの実際の画像は、必要な縦横比を維持するようにサイズ変更される場合があります。</span><span class="sxs-lookup"><span data-stu-id="b2c76-323">Therefore, when the dimensions of a placeholder in a template correspond to the ratio of an image that is entered, a real picture in a generated document might be resized to maintain the required aspect ratio.</span></span> <span data-ttu-id="b2c76-324">画像がサイズ変更されないようにするには、必要な縦横比のプレースホルダーを使用します。</span><span class="sxs-lookup"><span data-stu-id="b2c76-324">To prevent picture resizing, use a placeholder that has an expected aspect ratio.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="b2c76-325">追加リソース</span><span class="sxs-lookup"><span data-stu-id="b2c76-325">Additional resources</span></span>

- [<span data-ttu-id="b2c76-326">電子申告の概要</span><span class="sxs-lookup"><span data-stu-id="b2c76-326">Electronic Reporting overview</span></span>](general-electronic-reporting.md)
- [<span data-ttu-id="b2c76-327">電子レポートの出力先</span><span class="sxs-lookup"><span data-stu-id="b2c76-327">Electronic Reporting destinations</span></span>](electronic-reporting-destinations.md)
- [<span data-ttu-id="b2c76-328">電子報告のフォーミュラ言語</span><span class="sxs-lookup"><span data-stu-id="b2c76-328">Electronic reporting formula language</span></span>](er-formula-language.md)
- [<span data-ttu-id="b2c76-329">NUMBERFORMAT 機能</span><span class="sxs-lookup"><span data-stu-id="b2c76-329">NUMBERFORMAT function</span></span>](er-functions-text-numberformat.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]