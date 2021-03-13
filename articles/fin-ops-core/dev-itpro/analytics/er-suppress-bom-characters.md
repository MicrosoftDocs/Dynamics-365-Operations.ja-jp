---
title: 生成されたファイルの BOM 文字を非表示にする ER 構成の設計
description: このトピックでは、バイト オーダー マーク (BOM) 文字を非表示にするレポートを生成するために電子申告 (ER) 形式を構成する方法について説明します。
author: NickSelin
manager: AnnBe
ms.date: 01/04/2021
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EROperationDesigner
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2018-01-01
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 19fbbdea4bfdf30b1313a47e65056b536ed73dbe
ms.sourcegitcommit: 630a0b3f800f36ced49b79156dd52132904fef75
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/25/2021
ms.locfileid: "5060822"
---
# <a name="design-er-configurations-to-suppress-bom-characters-in-generated-files"></a><span data-ttu-id="bca32-103">生成されたファイルの BOM 文字を非表示にする ER 構成の設計</span><span class="sxs-lookup"><span data-stu-id="bca32-103">Design ER configurations to suppress BOM characters in generated files</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="bca32-104">送信ドキュメントを生成するための [電子申告 (ER)](general-electronic-reporting.md) [ソリューション](er-quick-start1-new-solution.md) をデザインできます。</span><span class="sxs-lookup"><span data-stu-id="bca32-104">You can design an [Electronic reporting (ER)](general-electronic-reporting.md) [solution](er-quick-start1-new-solution.md) to generate outgoing documents.</span></span> <span data-ttu-id="bca32-105">ドキュメントをテキスト ファイルまたは XML ファイルとして生成するには、ER [形式](general-electronic-reporting.md#FormatComponentOutbound) コンポーネントを含む ER [構成](general-electronic-reporting.md#Configuration) をソリューションに含める必要があります。</span><span class="sxs-lookup"><span data-stu-id="bca32-105">To generate the documents as text or XML files, the solution must include an ER [configuration](general-electronic-reporting.md#Configuration) that contains an ER [format](general-electronic-reporting.md#FormatComponentOutbound) component.</span></span> <span data-ttu-id="bca32-106">生成されたファイル内の文字セットを表す [文字エンコード](https://docs.microsoft.com/windows/win32/intl/character-sets) を指定するには、ER 形式に **Common\\File** 形式要素を含む必要があります。</span><span class="sxs-lookup"><span data-stu-id="bca32-106">To specify the [character encoding](https://docs.microsoft.com/windows/win32/intl/character-sets) that represents the set of characters in generated files, the ER format must contain the **Common\\File** format element.</span></span> <span data-ttu-id="bca32-107">ER 形式コンポーネントを構成するには、ER 形式デザイナーで ER 構成の [下書き](general-electronic-reporting.md#component-versioning) バージョンを開き、**Common\\File** 要素を追加します。</span><span class="sxs-lookup"><span data-stu-id="bca32-107">To configure the ER format component, open the [draft](general-electronic-reporting.md#component-versioning) version of the ER configuration in the ER format designer, and add the **Common\\File** element.</span></span> <span data-ttu-id="bca32-108">**エンコード** フィールドで、このコンポーネントを使用して実行時に生成される送信ファイルのエンコードを指定します。</span><span class="sxs-lookup"><span data-stu-id="bca32-108">In the **Encoding** field, specify the encoding of outbound files that are generated at runtime by using this component.</span></span>

> [!NOTE]
> <span data-ttu-id="bca32-109">形式に誤ったエンコード名が含まれている場合、形式の設定に対する変更を保存すると、エラーがスローされます。</span><span class="sxs-lookup"><span data-stu-id="bca32-109">If the format contains an incorrect encoding name, an error is thrown when you save your changes to the format's settings.</span></span>

![形式デザイナー ページでルート要素を追加する](./media/er-suppress-bom-characters-image1.gif)

<span data-ttu-id="bca32-111">エンコードとして **UTF-8**、**UTF-16**、または **UTF-32** を指定すると、**BOM 文字の非表示** オプションが使用可能になります。</span><span class="sxs-lookup"><span data-stu-id="bca32-111">If you specify **UTF-8**, **UTF-16**, or **UTF-32** as the encoding, the **Suppress BOM characters** option becomes available.</span></span> <span data-ttu-id="bca32-112">このオプションを **はい** に設定して、編集可能な ER 形式の実行時に、実行時に生成される発信ファイルで [バイト オーダー マーク (BOM) 文字](https://docs.microsoft.com/globalization/encoding/byte-order-mark) を非表示にします。</span><span class="sxs-lookup"><span data-stu-id="bca32-112">Set this option to **Yes** to suppress [byte order mark (BOM) characters](https://docs.microsoft.com/globalization/encoding/byte-order-mark) in outbound files that are generated at runtime when the editable ER format is run.</span></span>

> [!NOTE]
> <span data-ttu-id="bca32-113">**エンコード** フィールドを空白のままにすると、既定の **UTF-8** エンコードが使用されます。</span><span class="sxs-lookup"><span data-stu-id="bca32-113">If you leave the **Encoding** field blank, the default **UTF-8** encoding is used.</span></span>

![形式デザイナー ページで BOM 文字の非表示オプションを設定する](./media/er-suppress-bom-characters-image2.gif)

<span data-ttu-id="bca32-115">実行時に機能を確認するには、適切な手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="bca32-115">To review the functionality at runtime, complete the appropriate procedure.</span></span> <span data-ttu-id="bca32-116">たとえば、[ER 形式における XML 要素の実行の延期](er-defer-xml-element.md) トピックの手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="bca32-116">For example, complete the steps in the [Defer the execution of XML elements in ER formats](er-defer-xml-element.md) topic.</span></span> <span data-ttu-id="bca32-117">そのトピックにある [計算が生成された出力に基づくように形式を変更する](er-defer-xml-element.md#modify-the-format-so-that-the-calculation-is-based-on-generated-output) セクションの手順を完了したら、次の追加手順に従います。</span><span class="sxs-lookup"><span data-stu-id="bca32-117">After you've completed the steps in the [Modify the format so that the calculation is based on generated output](er-defer-xml-element.md#modify-the-format-so-that-the-calculation-is-based-on-generated-output) section of that topic, follow these additional steps.</span></span>

1. <span data-ttu-id="bca32-118">UTF エンコードを指定します:</span><span class="sxs-lookup"><span data-stu-id="bca32-118">Specify the UTF encoding:</span></span>

    1. <span data-ttu-id="bca32-119">**Common\\File** タイプの **レポート** 要素を選択します。</span><span class="sxs-lookup"><span data-stu-id="bca32-119">Select the **Report** element of the **Common\\File** type.</span></span>
    2. <span data-ttu-id="bca32-120">**エンコード** フィールドで 、**UTF-8** のエンコードを指定します。</span><span class="sxs-lookup"><span data-stu-id="bca32-120">In the **Encoding** field, specify the **UTF-8** encoding.</span></span>

2. <span data-ttu-id="bca32-121">BOM 文字を含む XML ファイルを生成します:</span><span class="sxs-lookup"><span data-stu-id="bca32-121">Generate an XML file that includes a BOM character:</span></span>

    1. <span data-ttu-id="bca32-122">**BOM 文字の非表示** オプションを **いいえ** に設定して、生成された XML ファイルに BOM 文字を含めます。</span><span class="sxs-lookup"><span data-stu-id="bca32-122">Set the **Suppress BOM characters** option to **No** to include BOM characters in generated XML files.</span></span>
    2. <span data-ttu-id="bca32-123">[電子申告形式における XML 要素の実行の延期](er-defer-xml-element.md) トピックの [計算された合計が使用されるように集計 XML 要素の実行を延期](er-defer-xml-element.md#defer-the-execution-of-the-summary-xml-element-so-that-the-calculated-total-is-used) セクションの手順を完了し、生成されたファイルを **SampleXmlReport.xml** として保存します。</span><span class="sxs-lookup"><span data-stu-id="bca32-123">Complete the steps in the [Defer the execution of the summary XML element so that the calculated total is used](er-defer-xml-element.md#defer-the-execution-of-the-summary-xml-element-so-that-the-calculated-total-is-used) section of the [Defer the execution of XML elements in ER formats](er-defer-xml-element.md) topic, and save the generated file as **SampleXmlReport.xml**.</span></span>

3. <span data-ttu-id="bca32-124">BOM 文字を含まない XML ファイルを生成します:</span><span class="sxs-lookup"><span data-stu-id="bca32-124">Generate an XML file that doesn't include a BOM character:</span></span>

    1. <span data-ttu-id="bca32-125">**BOM 文字の非表示** オプションを **はい** に設定して、生成された XML ファイルで BOM 文字を非表示にします。</span><span class="sxs-lookup"><span data-stu-id="bca32-125">Set the **Suppress BOM characters** option to **Yes** to suppress BOM characters in generated XML files.</span></span>
    2. <span data-ttu-id="bca32-126">[電子申告形式における XML 要素の実行の延期](er-defer-xml-element.md) トピックの [計算された合計が使用されるように集計 XML 要素の実行を延期](er-defer-xml-element.md#defer-the-execution-of-the-summary-xml-element-so-that-the-calculated-total-is-used) セクションの手順を完了し、生成されたファイルを **SampleXmlReport (1).xml** として保存します。</span><span class="sxs-lookup"><span data-stu-id="bca32-126">Complete the steps in the [Defer the execution of the summary XML element so that the calculated total is used](er-defer-xml-element.md#defer-the-execution-of-the-summary-xml-element-so-that-the-calculated-total-is-used) section of the [Defer the execution of XML elements in ER formats](er-defer-xml-element.md) topic, and save the generated file as **SampleXmlReport (1).xml**.</span></span>

4. <span data-ttu-id="bca32-127">ファイル比較ユーティリティで、生成されたファイルを比較します。</span><span class="sxs-lookup"><span data-stu-id="bca32-127">In a file comparison utility, compare the generated files.</span></span>

    <span data-ttu-id="bca32-128">最初に気付く違いは、ファイル ヘッダーにあります。</span><span class="sxs-lookup"><span data-stu-id="bca32-128">The first difference that you will notice is in the file header.</span></span> <span data-ttu-id="bca32-129">SampleXmlReport.xml ファイルには BOM 文字が含まれていますが、SampleXmlReport (1).xml ファイルには含まれていません。</span><span class="sxs-lookup"><span data-stu-id="bca32-129">The SampleXmlReport.xml file contains a BOM character, where the SampleXmlReport (1).xml file doesn't.</span></span>

    ![ファイル比較ユーティリティを使用して生成されたファイルを比較する](./media/er-suppress-bom-characters-image3.png)

## <a name="see-also"></a><span data-ttu-id="bca32-131">参照</span><span class="sxs-lookup"><span data-stu-id="bca32-131">See also</span></span>

- [<span data-ttu-id="bca32-132">電子申告形式における XML 要素の実行の延期</span><span class="sxs-lookup"><span data-stu-id="bca32-132">Defer the execution of XML elements in ER formats</span></span>](er-defer-xml-element.md)
