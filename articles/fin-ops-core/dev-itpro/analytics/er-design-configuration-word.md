---
title: Word 形式でレポートを生成するための新しい ER 構成を設計する
description: このトピックでは、ユーザーが新しい電子申告 (ER) 形式を構成して、レポートを Microsoft Word ドキュメントとして生成する方法について説明します。
author: NickSelin
manager: AnnBe
ms.date: 12/17/2020
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ERWorkspace, ERSolutionTable, EROperationDesigner,  LedgerJournalTable, LedgerJournalTransVendPaym
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2020-01-01
ms.dyn365.ops.version: Version 10.0.6
ms.openlocfilehash: 535e46eb033bf2796ab8e4b0d2e29767ad0a8cdf
ms.sourcegitcommit: 5192cfaedfd861faea63d8954d7bcc500608a225
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/30/2021
ms.locfileid: "5094157"
---
# <a name="design-a-new-er-configuration-to-generate-reports-in-word-format"></a><span data-ttu-id="18b19-103">Word 形式でレポートを生成するための新しい ER 構成を設計する</span><span class="sxs-lookup"><span data-stu-id="18b19-103">Design a new ER configuration to generate reports in Word format</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="18b19-104">レポートを Microsoft Word ドキュメントとして生成するには、Word デスクトップ アプリケーションなどを使用して、レポートのテンプレートをデザインする必要があります。</span><span class="sxs-lookup"><span data-stu-id="18b19-104">To generate reports as Microsoft Word documents, you must design a template for the reports by using, for example, the Word desktop application.</span></span> <span data-ttu-id="18b19-105">次の図は、処理済仕入先支払の詳細を表示するために生成できる管理レポートのサンプル テンプレートを示しています。</span><span class="sxs-lookup"><span data-stu-id="18b19-105">The following illustration shows the sample template for the control report that can be generated to show details of processed vendor payments.</span></span>

![Word デスクトップ アプリケーションの管理レポートのサンプル テンプレート](./media/er-design-configuration-word-image1.png)

<span data-ttu-id="18b19-107">Word ドキュメントを Word 形式のレポートのテンプレートとして使用するには、新しい [電子申告 (ER)](general-electronic-reporting.md) [ソリューション](er-quick-start1-new-solution.md) を構成できます。</span><span class="sxs-lookup"><span data-stu-id="18b19-107">To use a Word document as a template for reports in Word format, you can configure a new [Electronic reporting (ER)](general-electronic-reporting.md) [solution](er-quick-start1-new-solution.md).</span></span> <span data-ttu-id="18b19-108">このソリューションには、ER [形式](general-electronic-reporting.md#FormatComponentOutbound) コンポーネントを含む ER [構成](general-electronic-reporting.md#Configuration) を含める必要があります。</span><span class="sxs-lookup"><span data-stu-id="18b19-108">This solution must include an ER [configuration](general-electronic-reporting.md#Configuration) that contains an ER [format](general-electronic-reporting.md#FormatComponentOutbound) component.</span></span>

> [!NOTE]
> <span data-ttu-id="18b19-109">Word 形式でレポートを生成するために新しい ER 形式の構成を作成する場合は、**構成の作成** ドロップダウン ダイアログ ボックスで形式タイプとして **Word** を選択するか、**形式タイプ** フィールドを空白のままにする必要があります。</span><span class="sxs-lookup"><span data-stu-id="18b19-109">When you create a new ER format configuration to generate reports in Word format, you must either select **Word** as the format type in the **Create configuration** drop-down dialog box or leave the **Format type** field blank.</span></span>

![構成ページで形式構成を作成](./media/er-design-configuration-word-image2.gif)

<span data-ttu-id="18b19-111">ソリューションの ER 形式コンポーネントには **Excel\\File** 形式要素を含む必要があり、その形式要素は、実行時に生成されるレポートのテンプレートとして使用される Word ドキュメントにリンクされている必要があります。</span><span class="sxs-lookup"><span data-stu-id="18b19-111">The ER format component of the solution must contain the **Excel\\File** format element, and that format element must be linked to the Word document that will be used as the template for generated reports at runtime.</span></span> <span data-ttu-id="18b19-112">ER 形式コンポーネントを構成するには、ER 形式デザイナーで作成された ER 構成の [ドラフト](general-electronic-reporting.md#component-versioning) バージョンを開く必要があります。</span><span class="sxs-lookup"><span data-stu-id="18b19-112">To configure the ER format component, you must open the [draft](general-electronic-reporting.md#component-versioning) version of the created ER configuration in the ER format designer.</span></span> <span data-ttu-id="18b19-113">その後、**Excel\\File** 要素を追加し、編集可能な ER 形式に Word テンプレートを添付し、そのテンプレートを追加した **Excel\\File** 要素にリンクします。</span><span class="sxs-lookup"><span data-stu-id="18b19-113">Then add the **Excel\\File** element, attach your Word template to the editable ER format, and link that template to the **Excel\\File** element that you added.</span></span>

> [!NOTE]
> <span data-ttu-id="18b19-114">テンプレートを添付する場合、ER パラメーターで事前に [構成](electronic-reporting-er-configure-parameters.md#parameters-to-manage-documents) されている [ドキュメント タイプ](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/organization-administration/configure-document-management#configure-document-types) を使用して、ER 形式のテンプレートを保存する必要があります。</span><span class="sxs-lookup"><span data-stu-id="18b19-114">When you attach a template, you must use a [document type](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/organization-administration/configure-document-management#configure-document-types) that has previously been [configured](electronic-reporting-er-configure-parameters.md#parameters-to-manage-documents) in the ER parameters to store templates of ER formats.</span></span>

![形式デザイナー ページでテンプレートを添付](./media/er-design-configuration-word-image3.gif)

<span data-ttu-id="18b19-116">**Excel\\File** 要素に **Excel\\Range** と **Excel\\Cell** の入れ子になった要素を追加して、実行時に生成されるレポートに入力されるデータの構造を指定できます。</span><span class="sxs-lookup"><span data-stu-id="18b19-116">You can add **Excel\\Range** and **Excel\\Cell** nested elements for the **Excel\\File** element to specify the structure of data that will be entered in generated reports at runtime.</span></span> <span data-ttu-id="18b19-117">次に、これらの要素を編集可能な ER 形式のデータ ソースにバインドして、実行時に生成されるレポートに入力される実際のデータを指定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="18b19-117">You must then bind those elements to data sources of the editable ER format to specify the actual data that will be entered in generated reports at runtime.</span></span>

![形式デザイナー ページで入れ子になった要素を追加](./media/er-design-configuration-word-image4.gif)

<span data-ttu-id="18b19-119">ER 形式への変更をデザイン時に保存すると、階層形式の構造は、添付された Word テンプレートに、**レポート** という名前の [カスタム XML パーツ](https://docs.microsoft.com/visualstudio/vsto/custom-xml-parts-overview?view=vs-2019) として保存されます。</span><span class="sxs-lookup"><span data-stu-id="18b19-119">When you save your changes to the ER format at design time, the hierarchical format structure is stored in the attached Word template as a [custom XML part](https://docs.microsoft.com/visualstudio/vsto/custom-xml-parts-overview?view=vs-2019) that is named **Report**.</span></span> <span data-ttu-id="18b19-120">変更したテンプレートにアクセスし、Finance からダウンロードして、ローカルに保存して、Word デスクトップ アプリケーションで開く必要があります。</span><span class="sxs-lookup"><span data-stu-id="18b19-120">You must access the modified template, download it from Finance, store it locally, and open it in the Word desktop application.</span></span> <span data-ttu-id="18b19-121">次の図は、**レポート** カスタム XML パーツを含む管理レポートのローカルに保存されているサンプル テンプレートを示します。</span><span class="sxs-lookup"><span data-stu-id="18b19-121">The following illustration shows the locally stored sample template for the control report that contains the **Report** custom XML part.</span></span>

![Word デスクトップ アプリケーションでサンプル レポート テンプレートをプレビュー](./media/er-design-configuration-word-image5.gif)

<span data-ttu-id="18b19-123">**Excel\\Range** と **Excel\\Cell** 形式要素のバインドが実行時に実行される場合、すべてのバインドによって提供されるデータは、**レポート** のカスタム XML パーツの個別のフィールドとして、生成された Word ドキュメントに取り込まれます。</span><span class="sxs-lookup"><span data-stu-id="18b19-123">When bindings of **Excel\\Range** and **Excel\\Cell** format elements are run at runtime, the data that every binding delivers comes into the generated Word document as an individual field of the **Report** custom XML part.</span></span> <span data-ttu-id="18b19-124">生成されるドキュメントでカスタム XML パーツのフィールドから値を入力するには、実行時に入力されるデータのプレースホルダーとして機能させるために、適切な Word [コンテンツ コントロール](https://docs.microsoft.com/office/client-developer/word/content-controls-in-word) を Word テンプレートに追加する必要があります。</span><span class="sxs-lookup"><span data-stu-id="18b19-124">To enter the values from the fields of the custom XML part in a generated document, you must add the appropriate Word [content controls](https://docs.microsoft.com/office/client-developer/word/content-controls-in-word) to your Word template to serve as placeholders for data that will be filled in at runtime.</span></span> <span data-ttu-id="18b19-125">コンテンツ コントロールの入力方法を指定するには、すべてのコンテンツ コントロールを **レポート** カスタム XML パーツの適切なフィールドにマップします。</span><span class="sxs-lookup"><span data-stu-id="18b19-125">To specify how content controls are filled in, map every content control to the appropriate field of the **Report** custom XML part.</span></span>

![Word デスクトップ アプリケーションでコンテンツ コントロールを追加およびマッピング](./media/er-design-configuration-word-image6.gif)

<span data-ttu-id="18b19-127">次に、編集可能な ER 形式の元の Word テンプレートを、**レポート** カスタム XML パーツのフィールドにマップされた Word コンテンツ コントロールを含む変更されたテンプレートに置き換える必要があります。</span><span class="sxs-lookup"><span data-stu-id="18b19-127">You must then replace the original Word template of the editable ER format with the modified template that now contains Word content controls that were mapped to the fields of the **Report** custom XML part.</span></span>

![形式デザイナー ページでテンプレートを置換](./media/er-design-configuration-word-image7.gif)

<span data-ttu-id="18b19-129">構成された ER 形式を実行すると、添付された Word テンプレートを使用して新しいレポートが生成されます。</span><span class="sxs-lookup"><span data-stu-id="18b19-129">When you run the configured ER format, the attached Word template is used to generate a new report.</span></span> <span data-ttu-id="18b19-130">実際のデータは、**レポート** という名前のカスタム XML パーツとして Word レポートに格納されます。</span><span class="sxs-lookup"><span data-stu-id="18b19-130">The actual data is stored in the Word report as a custom XML part that is named **Report**.</span></span> <span data-ttu-id="18b19-131">生成されたレポートを開くと、Word コンテンツ コントロールに **レポート** カスタム XML パーツからデータが入力されます。</span><span class="sxs-lookup"><span data-stu-id="18b19-131">When the generated report is opened, the Word content controls are filled in with data from the **Report** custom XML part.</span></span>

## <a name="frequently-asked-questions"></a><span data-ttu-id="18b19-132">よく寄せられる質問</span><span class="sxs-lookup"><span data-stu-id="18b19-132">Frequently asked questions</span></span>

<span data-ttu-id="18b19-133">**質問:** 会社の住所を含む Word ドキュメントを印刷するように ER 形式を構成しました。</span><span class="sxs-lookup"><span data-stu-id="18b19-133">**Question:** I configured an ER format to print a Word document that contains a company address.</span></span> <span data-ttu-id="18b19-134">この ER 形式の Word テンプレートで、会社の住所を表示するリッチ テキスト コンテンツ コントロールを挿入しました。</span><span class="sxs-lookup"><span data-stu-id="18b19-134">In the Word template for this ER format, I inserted a rich text content control to present a company address.</span></span> <span data-ttu-id="18b19-135">Finance では、会社の住所を複数行テキストとして入力し、入力した各行にキャリッジ・リターンを追加するために **Enter** を選択しました。</span><span class="sxs-lookup"><span data-stu-id="18b19-135">In Finance, I entered the company address as multiline text and selected **Enter** to add a carriage return for every line that I entered.</span></span> <span data-ttu-id="18b19-136">したがって、生成されたドキュメントでは、会社住所が複数行テキストとして表示されることを期待します。</span><span class="sxs-lookup"><span data-stu-id="18b19-136">Therefore, I expect the company address to appear as multiline text in generated documents.</span></span> <span data-ttu-id="18b19-137">しかし、住所は、キャリッジ リターンの代わりに特殊記号を含む 1 行のテキストとして表示されます。</span><span class="sxs-lookup"><span data-stu-id="18b19-137">However, the address appears as a single line of text that contains special symbols instead of carriage returns.</span></span> <span data-ttu-id="18b19-138">設定の何が悪いのですか?</span><span class="sxs-lookup"><span data-stu-id="18b19-138">What is wrong with my settings?</span></span>

<span data-ttu-id="18b19-139">**回答:** リッチ テキスト コンテンツ コントロールを使用する代わりに、プレーン テキスト コンテンツ コントロールを使用し、コントロールのプロパティで **キャリッジ リターンを許可 (複数の段落)** チェック ボックスを選択する必要があります。</span><span class="sxs-lookup"><span data-stu-id="18b19-139">**Answer:** Instead of using a rich text content control, you must use a plain text content control and select the **Allow carriage returns (multiple paragraphs)** check box in the control's properties.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="18b19-140">追加リソース</span><span class="sxs-lookup"><span data-stu-id="18b19-140">Additional resources</span></span>

- [<span data-ttu-id="18b19-141">Excel テンプレートと ER 構成を再利用して Word 形式でレポートを生成</span><span class="sxs-lookup"><span data-stu-id="18b19-141">Reuse ER configurations with Excel templates to generate reports in Word format</span></span>](./tasks/er-design-configuration-word-2016-11.md)
- [<span data-ttu-id="18b19-142">ER を使用して生成されるドキュメントへの画像や図形の埋め込み</span><span class="sxs-lookup"><span data-stu-id="18b19-142">Embed images and shapes in documents that you generate by using ER</span></span>](electronic-reporting-embed-images-shapes.md#embed-an-image-in-a-word-document)
