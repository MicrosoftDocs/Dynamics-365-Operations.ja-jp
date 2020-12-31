---
title: Excel 形式でドキュメントを生成する構成を設計する
description: このトピックでは、Excel のテンプレートに入力する電子レポート (ER) のフォーマットを設計し、Excel 形式の出力ドキュメントを生成する方法について説明します。
author: NickSelin
manager: AnnBe
ms.date: 11/02/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: EROperationDesigner, ERParameters
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.custom: 220314
ms.assetid: 2685df16-5ec8-4fd7-9495-c0f653e82567
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: d5733e40c67f9c97b04f126f7c3cfea9d4f8f5b5
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 12/05/2020
ms.locfileid: "4686541"
---
# <a name="design-a-configuration-for-generating-documents-in-excel-format"></a><span data-ttu-id="592ac-103">Excel 形式でドキュメントを生成する構成を設計する</span><span class="sxs-lookup"><span data-stu-id="592ac-103">Design a configuration for generating documents in Excel format</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="592ac-104">ER [フォーマットのコンポーネント](general-electronic-reporting.md#FormatComponentOutbound) を持つ[電子レポート (ER) ](general-electronic-reporting.md) フォーマットの構成を設計して、 Microsoft Excel ワークブック形式の出力ドキュメントを生成するように構成することができます。</span><span class="sxs-lookup"><span data-stu-id="592ac-104">You can design an [Electronic reporting (ER)](general-electronic-reporting.md) format configuration that has an ER [format component](general-electronic-reporting.md#FormatComponentOutbound) that you can configure to generate an outbound document in a Microsoft Excel workbook format.</span></span> <span data-ttu-id="592ac-105">これには、特定の ERフォーマットのコンポーネントを使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="592ac-105">Specific ER format components must be used for this purpose.</span></span>

<span data-ttu-id="592ac-106">この機能の詳細については、[OPENXML 形式でレポートを生成する構成を設計する](tasks/er-design-reports-openxml-2016-11.md)に記載の手順に従ってください。</span><span class="sxs-lookup"><span data-stu-id="592ac-106">To learn more about this feature, follow the steps in the topic, [Design a configuration for generating reports in OPENXML format](tasks/er-design-reports-openxml-2016-11.md).</span></span>

## <a name="add-a-new-er-format"></a><span data-ttu-id="592ac-107">新規 ER 形式の追加</span><span class="sxs-lookup"><span data-stu-id="592ac-107">Add a new ER format</span></span>

<span data-ttu-id="592ac-108">新たな ER 形式の構成を追加して、Excel ブック形式で送信ドキュメントを生成する場合は、形式の **形式のタイプ** 属性に **excel** の値を選択するか、**形式のタイプ** 属性を空白のままにしておく必要があります。</span><span class="sxs-lookup"><span data-stu-id="592ac-108">When you add a new ER format configuration to generate an outbound document in an Excel workbook format, you must either select the **Excel** value for the **Format type** attribute of the format or leave the **Format type** attribute blank.</span></span>

- <span data-ttu-id="592ac-109">**Excel** を選択した場合は 、Excel 形式でのみ送信ドキュメントを生成するように形式を構成することができます。</span><span class="sxs-lookup"><span data-stu-id="592ac-109">If you select **Excel**, you can configure the format to generate an outbound document only in Excel format.</span></span>
- <span data-ttu-id="592ac-110">属性を空白のままにすると、ERフ レームワークでサポートされている任意の形式で送信ドキュメントを生成するように形式を構成することができます。</span><span class="sxs-lookup"><span data-stu-id="592ac-110">If you leave the attribute blank, you can configure the format to generate an outbound document in any format that is supported by the ER framework.</span></span>

<span data-ttu-id="592ac-111">ER 形式のコンポーネントを構成するには、アクション ウィンドウで **デザイナー** を選択し、ER オペレーション デザイナーで編集用の ER 形式のコンポーネントを開きます。</span><span class="sxs-lookup"><span data-stu-id="592ac-111">To configure the ER format component of the configuration, select **Designer** on the Action Pane, and open the ER format component for editing in the ER Operation designer.</span></span>

![構成ページ](./media/er-excel-format-add-format.png)

## <a name="excel-file-component"></a><span data-ttu-id="592ac-113">Excel ファイル コンポーネント</span><span class="sxs-lookup"><span data-stu-id="592ac-113">Excel file component</span></span>

### <a name="manual-entry"></a><span data-ttu-id="592ac-114">手動入力</span><span class="sxs-lookup"><span data-stu-id="592ac-114">Manual entry</span></span>

<span data-ttu-id="592ac-115">出力ドキュメントを Excel 形式で生成するには、**Excel\\ファイル** コンポーネントを、構成されたER形式に追加する必要があります。</span><span class="sxs-lookup"><span data-stu-id="592ac-115">You must add an **Excel\\File** component to the configured ER format to generate an outbound document in Excel format.</span></span>

![Excel\ファイル コンポーネント](./media/er-excel-format-add-file-component.png)

<span data-ttu-id="592ac-117">送信ドキュメントのレイアウトを指定するには、 **Excel\\ファイル** コンポーネントに拡張子 .xlsx の Excel ワークブックを 出力ドキュメントのテンプレートとして添付します。</span><span class="sxs-lookup"><span data-stu-id="592ac-117">To specify the layout of the outbound document, attach an Excel workbook that has the .xlsx extension to the **Excel\\File** component as the template for outbound documents.</span></span>

> [!NOTE]
> <span data-ttu-id="592ac-118">テンプレートを手動で関連付ける場合は、[ER パラメータ](electronic-reporting-er-configure-parameters.md#parameters-to-manage-documents) でこの目的に対して構成されている[ドキュメント タイプ](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/organization-administration/configure-document-management#configure-document-types)を使用する必要があり ます。</span><span class="sxs-lookup"><span data-stu-id="592ac-118">When you manually attach a template, you must use a [document type](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/organization-administration/configure-document-management#configure-document-types) that has been configured for that purpose in the [ER parameters](electronic-reporting-er-configure-parameters.md#parameters-to-manage-documents).</span></span>

![Excel\ファイル コンポーネントに添付ファイルを追加する](./media/er-excel-format-add-file-component2.png)

<span data-ttu-id="592ac-120">構成された ER 形式を実行する際に添付のテンプレートがどのように入力されるかを指定するには、**Excel\\ファイル** コンポーネントに入れ子になった **シート**、**範囲**、**セル** コンポーネントを追加する必要があります。</span><span class="sxs-lookup"><span data-stu-id="592ac-120">To specify how the attached template will be filled in when you run the configured ER format, you must add nested **Sheet**, **Range**, and **Cell** components to the **Excel\\File** component.</span></span> <span data-ttu-id="592ac-121">入れ子になった各コンポーネントは、Excel の名前付きアイテムに関連付けられている必要があります。</span><span class="sxs-lookup"><span data-stu-id="592ac-121">Each nested component must be associated with an Excel named item.</span></span>

### <a name="template-import"></a><span data-ttu-id="592ac-122">テンプレートのインポート</span><span class="sxs-lookup"><span data-stu-id="592ac-122">Template import</span></span>

<span data-ttu-id="592ac-123">新しいテンプレートを空の ER 形式にインポートするには、アクションウィンドウの **インポート** タブの **Excel からインポート** を選択します。</span><span class="sxs-lookup"><span data-stu-id="592ac-123">You can select **Import from Excel** on the **Import** tab of the Action Pane to import a new template into a blank ER format.</span></span> <span data-ttu-id="592ac-124">この例では、**Excel \\ファイル** コンポーネントが自動的に作成され、インポートされたテンプレートがそのコンポーネントに関連付けられます。</span><span class="sxs-lookup"><span data-stu-id="592ac-124">In this example, an **Excel\\File** component will be created automatically, and the imported template will be attached to it.</span></span> <span data-ttu-id="592ac-125">検出された Excel の名前付きアイテムの一覧に基づき、必要な ER コンポーネントもすべて自動的に作成されます。</span><span class="sxs-lookup"><span data-stu-id="592ac-125">All required ER components will also be created automatically, based on the list of Excel named items that are discovered.</span></span>

![[Excel からインポート] を選択します](./media/er-excel-format-import-template.png)

> [!NOTE]
> <span data-ttu-id="592ac-127">オプションの **シート** 要素を編集可能な形式で作成する場合は、 **Excel シート形式の要素の作成** オプションを **はい** に設定します。</span><span class="sxs-lookup"><span data-stu-id="592ac-127">If you want to create the optional **Sheet** element in the editable ER format, set the **Create Excel Sheet format element** option to **Yes**.</span></span>

## <a name="sheet-component"></a><span data-ttu-id="592ac-128">シート コンポーネント</span><span class="sxs-lookup"><span data-stu-id="592ac-128">Sheet component</span></span>

<span data-ttu-id="592ac-129">**シート** コンポーネントは、入力する必要がある関連付けられた Excel ブックのワークシートを示します。</span><span class="sxs-lookup"><span data-stu-id="592ac-129">The **Sheet** component indicates a worksheet of the attached Excel workbook that must be filled in.</span></span> <span data-ttu-id="592ac-130">Excel テンプレートのワークシートの名前は、このコンポーネントの **シート** プロパティで定義されます。</span><span class="sxs-lookup"><span data-stu-id="592ac-130">The name of the worksheet in an Excel template is defined in the **Sheet** property of this component.</span></span>

> [!NOTE]
> <span data-ttu-id="592ac-131">Excel ブックに1つのワークシートのみが存在する場合、このコンポーネントは省略可能です。</span><span class="sxs-lookup"><span data-stu-id="592ac-131">This component is optional for Excel workbooks that contain a single worksheet.</span></span>

<span data-ttu-id="592ac-132">ER オペレーション デザイナーの **マッピング** タブで、**シート** コンポーネントの **有効化** プロパティを構成して、生成されるドキュメントにコンポーネントを配置するかどうかを指定することができます。</span><span class="sxs-lookup"><span data-stu-id="592ac-132">On the **Mapping** tab of the ER Operation designer, you can configure the **Enabled** property for a **Sheet** component to specify whether the component must be put in a generated document:</span></span>

- <span data-ttu-id="592ac-133">**有効化** プロパティの式が実行時に **True** を返すように設定されている場合、または式が全く設定されていない場合は、適切なワークシートが生成されたドキュメントに配置されます。</span><span class="sxs-lookup"><span data-stu-id="592ac-133">If an expression of the **Enabled** property is configured to return **True** at runtime, or if no expression is configured at all, the appropriate worksheet will be put in the generated document.</span></span>
- <span data-ttu-id="592ac-134">実行時に **有効化** プロパティの式が **False** を返すように構成されている場合、生成されたドキュメントにはワークシートが含まれません。</span><span class="sxs-lookup"><span data-stu-id="592ac-134">If an expression of the **Enabled** property is configured to return **False** at runtime, the generated document won't contain a worksheet.</span></span>

![シート コンポーネントの例](./media/er-excel-format-sheet-component.png)

## <a name="range-component"></a><span data-ttu-id="592ac-136">範囲コンポーネント</span><span class="sxs-lookup"><span data-stu-id="592ac-136">Range component</span></span>

<span data-ttu-id="592ac-137">**範囲** コンポーネントは、この ER コンポーネントによって制御される必要がある Excel の範囲を示します。</span><span class="sxs-lookup"><span data-stu-id="592ac-137">The **Range** component indicates an Excel range that must be controlled by this ER component.</span></span> <span data-ttu-id="592ac-138">範囲の名前は、このコンポーネントの **Excel の範囲** プロパティで定義されています。</span><span class="sxs-lookup"><span data-stu-id="592ac-138">The name of the range is defined in the **Excel range** property of this component.</span></span>

<span data-ttu-id="592ac-139">**レプリケーションの方向**  プロパティでは、生成されたドキュメントで範囲を繰り返すかどうか、どのように繰り返すかを指定します。</span><span class="sxs-lookup"><span data-stu-id="592ac-139">The **Replication direction** property specifies whether and how the range will be repeated in a generated document:</span></span>

- <span data-ttu-id="592ac-140">**レプリケーションの方向** プロパティが **レプリケーションなし** に設定されている場合、該当する Excel 範囲は、生成されたドキュメント内で繰り返されません。</span><span class="sxs-lookup"><span data-stu-id="592ac-140">If the **Replication direction** property is set to **No replication**, the appropriate Excel range won't be repeated in the generated document.</span></span>
- <span data-ttu-id="592ac-141">**レプリケーションの方向** プロパティが **縦方向** に設定されている場合、該当する Excel 範囲が、生成されたドキュメント内で繰り返されます。</span><span class="sxs-lookup"><span data-stu-id="592ac-141">If the **Replication direction** property is set to **Vertical**, the appropriate Excel range will be repeated in the generated document.</span></span> <span data-ttu-id="592ac-142">レプリケートされたすべての範囲は、Excel テンプレートの元の範囲の下部に配置されます。</span><span class="sxs-lookup"><span data-stu-id="592ac-142">Every replicated range is put below the original range in an Excel template.</span></span> <span data-ttu-id="592ac-143">繰り返される回数は、この ER コンポーネントにバインドされている **レコード リスト** タイプのデータソース内のレコード数で定義されます。</span><span class="sxs-lookup"><span data-stu-id="592ac-143">The number of repetitions is defined by the number of records in a data source of the **Record list** type that is bound to this ER component.</span></span>
- <span data-ttu-id="592ac-144">**レプリケーションの方向** プロパティが **水平方向** に設定されている場合、該当する Excel 範囲が、生成されたドキュメント内で繰り返されます。</span><span class="sxs-lookup"><span data-stu-id="592ac-144">If the **Replication direction** property is set to **Horizontal**, the appropriate Excel range will be repeated in the generated document.</span></span> <span data-ttu-id="592ac-145">レプリケートされたすべての範囲は、Excel テンプレートの元の範囲の右側に配置されます。</span><span class="sxs-lookup"><span data-stu-id="592ac-145">Every replicated range is put to the right of the original range in an Excel template.</span></span> <span data-ttu-id="592ac-146">繰り返される回数は、この ER コンポーネントにバインドされている **レコード リスト** タイプのデータソース内のレコード数で定義されます。</span><span class="sxs-lookup"><span data-stu-id="592ac-146">The number of repetitions is defined by the number of records in a data source of the **Record list** type that is bound to this ER component.</span></span>

<span data-ttu-id="592ac-147">水平方向のレプリケーションの詳細については、[水平方向に拡張可能な範囲を使用して、Excel レポートで列を動的に追加する](tasks/er-horizontal-1.md) に記載の手順に従ってください。</span><span class="sxs-lookup"><span data-stu-id="592ac-147">To learn more about horizontal replication, follow the steps in [Use horizontally expandable ranges to dynamically add columns in Excel reports](tasks/er-horizontal-1.md).</span></span>

<span data-ttu-id="592ac-148">**範囲** コンポーネントは、他のネストされた ER コンポーネントを持つことができ、これは適切な Excel の名前付き範囲に値を入力する目的で使用されます。</span><span class="sxs-lookup"><span data-stu-id="592ac-148">The **Range** component can have other nested ER components that are used to enter values in the appropriate Excel named ranges.</span></span>

- <span data-ttu-id="592ac-149">**テキスト** グループのいずれかのコンポーネントが値の入力に使用されている場合、その値は Excel の範囲のテキスト値として入力されます。</span><span class="sxs-lookup"><span data-stu-id="592ac-149">If any component of the **Text** group is used to enter values, the value is entered in an Excel range as a text value.</span></span>

    > [!NOTE]
    > <span data-ttu-id="592ac-150">このパターンを使用して、アプリケーションで定義されているロケールに基づいて入力された値の書式を設定します。</span><span class="sxs-lookup"><span data-stu-id="592ac-150">Use this pattern to format entered values based on the locale that is defined in the application.</span></span>

- <span data-ttu-id="592ac-151">**Excel** グループの **セル** コンポーネントを使用して値を入力する場合、その値は、その **セル** コンポーネントのバインドが定義するデータ型  ( **文字列**、**実数**、**整数** など ) の値として Excel の範囲に入力されます。</span><span class="sxs-lookup"><span data-stu-id="592ac-151">If the **Cell** component of the **Excel** group is used to enter values, the value is entered in an Excel range as a value of the data type that is defined by the binding of that **Cell** component (for example, **String**, **Real**, or **Integer**).</span></span>

    > [!NOTE]
    > <span data-ttu-id="592ac-152">このパターンを使用すると、Excel アプリケーションが、送信ドキュメントを開くローカル コンピュータのロケールに基づいて入力された値を書式設定できるようになります。</span><span class="sxs-lookup"><span data-stu-id="592ac-152">Use this pattern to enable the Excel application to format entered values based on the locale of the local computer that opens the outbound document.</span></span>

<span data-ttu-id="592ac-153">ER オペレーション デザイナーの **マッピング** タブで、**範囲** コンポーネントの **有効化** プロパティを構成して、生成されるドキュメントにコンポーネントを配置するかどうかを指定することができます。</span><span class="sxs-lookup"><span data-stu-id="592ac-153">On the **Mapping** tab of the ER Operation designer, you can configure the **Enabled** property for a **Range** component to specify whether the component must be put in a generated document:</span></span>

- <span data-ttu-id="592ac-154">**有効化** プロパティの式が実行時に **True** を返すように設定されている場合、または式が全く設定されていない場合は、適切な範囲が生成されたドキュメントに入力されます。</span><span class="sxs-lookup"><span data-stu-id="592ac-154">If an expression of the **Enabled** property is configured to return **True** at runtime, or if no expression is configured at all, the appropriate range will be filled in in the generated document.</span></span>
- <span data-ttu-id="592ac-155">**有効化** プロパティの式が実行時に **True** を返すように設定されている場合、かつこの範囲が行や列全体を表していない場合、生成されたドキュメントでは適切な範囲が入力されません。</span><span class="sxs-lookup"><span data-stu-id="592ac-155">If an expression of the **Enabled** property is configured to return **False** at runtime, and if this range doesn't represent the entire rows or columns, the appropriate range won't be filled in in the generated document.</span></span>
- <span data-ttu-id="592ac-156">**有効化** プロパティの式が実行時に **True** を返すように設定されている場合、かつこの範囲が行または列全体を表す場合、生成されたドキュメントにはそれらの行や列が非表示の行や列として含まれます。</span><span class="sxs-lookup"><span data-stu-id="592ac-156">If an expression of the **Enabled** property is configured to return **False** at runtime, and this range represents the entire rows or columns, the generated document will contain those rows and columns as hidden rows and columns.</span></span>

## <a name="cell-component"></a><span data-ttu-id="592ac-157">セルのコンポーネント</span><span class="sxs-lookup"><span data-stu-id="592ac-157">Cell component</span></span>

<span data-ttu-id="592ac-158">**セル** コンポーネントは、Excel の名前付きセル、図形、画像の入力に使用されます。</span><span class="sxs-lookup"><span data-stu-id="592ac-158">The **Cell** component is used to fill in Excel named cells, shapes, and pictures.</span></span> <span data-ttu-id="592ac-159">**セル** ER コンポーネントで入力する必要がある Excel の名前付きオブジェクトを指定するには、**セル** コンポーネントの **Excel の範囲** プロパティでそのオブジェクトの名前を指定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="592ac-159">To indicate an Excel named object that must be filled in by a **Cell** ER component, you must specify the name of that object in the **Excel range** property of the **Cell** component.</span></span>

<span data-ttu-id="592ac-160">ER オペレーション デザイナーの **マッピング** タブで、**セル** コンポーネントの **有効化** プロパティを構成して、生成されるドキュメントにオブジェクトを配置するかどうかを指定することができます。</span><span class="sxs-lookup"><span data-stu-id="592ac-160">On the **Mapping** tab of the ER Operation designer, you can configure the **Enabled** property for a **Cell** component to specify whether the object must be filled in in a generated document:</span></span>

- <span data-ttu-id="592ac-161">**有効化** プロパティの式が実行時に **True** を返すように設定されている場合、または式が全く設定されていない場合は、適切なオブジェクトが生成されたドキュメントに入力されます。</span><span class="sxs-lookup"><span data-stu-id="592ac-161">If an expression of the **Enabled** property is configured to return **True** at runtime, or if no expression is configured at all, the appropriate object will be filled in in the generated document.</span></span> <span data-ttu-id="592ac-162">この **セル** コンポーネントのバインディングによって、適切なオブジェクトに配置される値が指定されます。</span><span class="sxs-lookup"><span data-stu-id="592ac-162">The binding of this **Cell** component specifies a value that is put in the appropriate object.</span></span>
- <span data-ttu-id="592ac-163">実行時に **有効化** プロパティの式が **False** を返すように構成されている場合、生成されたドキュメントには適切なオブジェクトが含まれません。</span><span class="sxs-lookup"><span data-stu-id="592ac-163">If an expression of the **Enabled** property is configured to return **False** at runtime, the appropriate object won't be filled in in the generated document.</span></span>

<span data-ttu-id="592ac-164">**セル** コンポーネントがセルに値を入力するように構成されている場合は、プリミティブ データ型 ( **文字列**、**実数**、 **整数** など) の値を返すデータソースにバインドでき ます。</span><span class="sxs-lookup"><span data-stu-id="592ac-164">When a **Cell** component is configured to enter a value in a cell, it can be bound with a data source that returns the value of a primitive data type (for example, **String**, **Real**, or **Integer**).</span></span> <span data-ttu-id="592ac-165">この場合、値は同一のデータ型の値としてセルに入力されます。</span><span class="sxs-lookup"><span data-stu-id="592ac-165">In this case, the value is entered in the cell as a value of the same data type.</span></span>

<span data-ttu-id="592ac-166">**セル** コンポーネントが Excel のシェイプで値を入力するように構成されている場合は、プリミティブ データ型 ( **文字列**、**実数**、 **整数** など) の値を返すデータソースにバインドでき ます。</span><span class="sxs-lookup"><span data-stu-id="592ac-166">When a **Cell** component is configured to enter a value in an Excel shape, it can be bound with a data source that returns a value of a primitive data type (for example, **String**, **Real**, or **Integer**).</span></span> <span data-ttu-id="592ac-167">この場合、値はこのシェイプのテキストとして Excel のシェイプに入力されます。</span><span class="sxs-lookup"><span data-stu-id="592ac-167">In this case, the value is entered in the Excel shape as the text of that shape.</span></span> <span data-ttu-id="592ac-168">**文字列** ではないデータ型の値については、自動的にテキストへの変換が行われます。</span><span class="sxs-lookup"><span data-stu-id="592ac-168">For values of data types that aren't **String**, the conversion to text is done automatically.</span></span>

> [!NOTE]
> <span data-ttu-id="592ac-169">[シェイプ テキスト] プロパティがサポートされている場合にのみ、**セル** コンポーネントを構成してシェイプに入力できます。</span><span class="sxs-lookup"><span data-stu-id="592ac-169">You can configure a **Cell** component to fill in a shape only in cases where a shape text property is supported.</span></span>

<span data-ttu-id="592ac-170">**セル** コンポーネントが Excel ピクチャに値を入力するように構成されている場合は、バイナリ形式で画像を表す **コンテナ** データ型の値を返すデータソースにバインドすることができます。</span><span class="sxs-lookup"><span data-stu-id="592ac-170">When a **Cell** component is configured to enter a value in an Excel picture, it can be bound with a data source that returns a value of the **Container** data type that represents an image in binary format.</span></span> <span data-ttu-id="592ac-171">この場合、値が Excel ピクチャに画像として入力されます。</span><span class="sxs-lookup"><span data-stu-id="592ac-171">In this case, the value is entered in the Excel picture as an image.</span></span>

> [!NOTE]
> <span data-ttu-id="592ac-172">すべての Excel のピクチャとシェイプは、その左上隅が特定の Excel セル、または範囲に固定されていると考えられます。</span><span class="sxs-lookup"><span data-stu-id="592ac-172">Every Excel picture and shape is considered to be anchored by its upper-left corner to a specific Excel cell or range.</span></span> <span data-ttu-id="592ac-173">Excel のピクチャまたはシェイプをレプリケートする場合は、固定されているセルまたは範囲をレプリケートされたセル、または範囲として構成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="592ac-173">If you want to replicate an Excel picture or shape, you must configure the cell or range that it's anchored to as a replicated cell or range.</span></span>

<span data-ttu-id="592ac-174">画像とシェイプを埋め込む方法の詳細については、[ER を使用して生成したドキュメントに画像やシェイプを埋め込む](electronic-reporting-embed-images-shapes.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="592ac-174">To learn more about how to embed images and shapes, see [Embed images and shapes in documents that you generate by using ER](electronic-reporting-embed-images-shapes.md).</span></span>

## <a name="page-break-component"></a><span data-ttu-id="592ac-175">改ページ コンポーネント</span><span class="sxs-lookup"><span data-stu-id="592ac-175">Page break component</span></span>

<span data-ttu-id="592ac-176">**改ページ** コンポーネントは、Excel が新たなページを開始するように強制します。</span><span class="sxs-lookup"><span data-stu-id="592ac-176">The **PageBreak** component forces Excel to start a new page.</span></span> <span data-ttu-id="592ac-177">Excel の既定のページ設定を使用する場合、このコンポーネントは必要ありませんが、Excel で ER 形式のページ構造を使用する場合にはこのコンポーネントを推奨します。</span><span class="sxs-lookup"><span data-stu-id="592ac-177">This component isn't required when you want to use Excel's default paging, but you should use it when you want Excel to follow your ER format to structure paging.</span></span>

## <a name="edit-an-added-er-format"></a><span data-ttu-id="592ac-178">追加された ER 形式の編集</span><span class="sxs-lookup"><span data-stu-id="592ac-178">Edit an added ER format</span></span>

### <a name="update-a-template"></a><span data-ttu-id="592ac-179">テンプレートの更新</span><span class="sxs-lookup"><span data-stu-id="592ac-179">Update a template</span></span>

<span data-ttu-id="592ac-180">更新されたテンプレートを編集可能な ER 形式にインポートするには、アクションウィンドウの **インポート** タブの **Excel から更新する** を選択します。</span><span class="sxs-lookup"><span data-stu-id="592ac-180">You can select **Update from Excel** on the **Import** tab of the Action Pane to import an updated template into an editable ER format.</span></span> <span data-ttu-id="592ac-181">このプロセスでは、選択された **Excel \\ファイル** コンポーネントのテンプレートが新たなテンプレートに置き換えられます。</span><span class="sxs-lookup"><span data-stu-id="592ac-181">During this process, a template of the selected **Excel\\File** component will be replaced by a new template.</span></span> <span data-ttu-id="592ac-182">編集可能な ER 形式の内容は、更新されたERテンプレートの内容と同期されます。</span><span class="sxs-lookup"><span data-stu-id="592ac-182">The content of the editable ER format will be synced with the content of the updated ER template.</span></span>

- <span data-ttu-id="592ac-183">ER 形式のコンポーネントが編集可能なフォーマットで見つからなかった場合、新たな ERフォーマットのコンポーネントがすべての Excel 名に対して自動的に作成されます。</span><span class="sxs-lookup"><span data-stu-id="592ac-183">A new ER format component will automatically be created for every Excel name if the ER format component isn't found in the editable format.</span></span>
- <span data-ttu-id="592ac-184">必要な Excel 名が見つからない場合、すべての ER 形式のコンポーネントが編集可能な ER 形式から削除されます。</span><span class="sxs-lookup"><span data-stu-id="592ac-184">Every ER format component will be deleted from the editable ER format if the appropriate Excel name isn't found for it.</span></span>

> [!NOTE]
> <span data-ttu-id="592ac-185">オプションの **シート** 要素を編集可能な ER 形式で作成する場合は、 **Excel シート形式の要素の作成** オプションを **はい** に設定し ます。</span><span class="sxs-lookup"><span data-stu-id="592ac-185">Set the **Create Excel Sheet format element** option to **Yes** if you want to create the optional **Sheet** element in the editable ER format.</span></span>
>
> <span data-ttu-id="592ac-186">編集可能な ER 形式に元の **シート** 要素が含まれている場合は、更新した テンプレートをインポートする際に、**Excel シート形式の要素の作成**  オプションを **はい** に設定することを推奨します。</span><span class="sxs-lookup"><span data-stu-id="592ac-186">If the editable ER format originally contained **Sheet** elements, we recommend that you set the **Create Excel Sheet format element** option to **Yes** when you import an updated template.</span></span> <span data-ttu-id="592ac-187">それ以外の場合、元の **シート** 要素の入れ子になった要素はすべて最初から作成されます。</span><span class="sxs-lookup"><span data-stu-id="592ac-187">Otherwise, all nested elements of the original **Sheet** element will be created from scratch.</span></span> <span data-ttu-id="592ac-188">したがって、再作成された形式要素のすべてのバインドは、更新された ER 形式では失われます。</span><span class="sxs-lookup"><span data-stu-id="592ac-188">Therefore, all bindings of the re-created format elements will be lost in the updated ER format.</span></span>

![[Excelから更新] ダイアログ ボックスの [Excel シート形式の要素] オプションの作成](./media/er-excel-format-update-template.png)

<span data-ttu-id="592ac-190">この機能の詳細については、[Excel のテンプレートを再適用することで、電子レポートの形式を変更する](modify-electronic-reporting-format-reapply-excel-template.md) に記載の手順に従っ てください。</span><span class="sxs-lookup"><span data-stu-id="592ac-190">To learn more about this feature, follow the steps in [Modify Electronic reporting formats by reapplying Excel templates](modify-electronic-reporting-format-reapply-excel-template.md).</span></span>

## <a name="validate-an-er-format"></a><span data-ttu-id="592ac-191">ER 形式の検証</span><span class="sxs-lookup"><span data-stu-id="592ac-191">Validate an ER format</span></span>

<span data-ttu-id="592ac-192">編集可能な ER 形式を検証する場合は、現在使用している Excel のテンプレートに Excel 名が存在することを確認する整合性チェックが行われます。</span><span class="sxs-lookup"><span data-stu-id="592ac-192">When you validate an ER format that can be edited, a consistency check is done to make sure that the Excel name is present in the Excel template that is currently used.</span></span> <span data-ttu-id="592ac-193">不整合性がある場合には通知されます。</span><span class="sxs-lookup"><span data-stu-id="592ac-193">You will be notified about any inconsistencies.</span></span> <span data-ttu-id="592ac-194">不整合がある場合は、自動的に問題を修正するオプションが表示されます。</span><span class="sxs-lookup"><span data-stu-id="592ac-194">For some inconsistencies, the option to automatically fix issues will be offered.</span></span>

![検証エラー メッセージ](./media/er-excel-format-validate.png)

## <a name="control-the-calculation-of-excel-formulas"></a><span data-ttu-id="592ac-196">Excel の数式の計算の制御</span><span class="sxs-lookup"><span data-stu-id="592ac-196">Control the calculation of Excel formulas</span></span>

<span data-ttu-id="592ac-197">Microsoft Excel ブック形式の送信ドキュメントが生成された場合、このドキュメントの一部のセルに Excel の数式が含まれている可能性があります。</span><span class="sxs-lookup"><span data-stu-id="592ac-197">When an outbound document in a Microsoft Excel workbook format is generated, some cells of this document might contain Excel formulas.</span></span> <span data-ttu-id="592ac-198">**電子レポート フレームワーク機能で EPPlus ライブラリの使用を有効にする** 機能が有効になっている場合、使用中の Excel テンプレートの **計算オプション** [パラメーター](https://support.microsoft.com/office/change-formula-recalculation-iteration-or-precision-in-excel-73fc7dac-91cf-4d36-86e8-67124f6bcce4#ID0EAACAAA=Windows) の値を変更することで、数式を計算するタイミングを制御できます。</span><span class="sxs-lookup"><span data-stu-id="592ac-198">When the **Enable usage of EPPlus library in Electronic reporting framework** feature is enabled, you can control when the formulas are calculated by changing the value of the **Calculation Options** [parameter](https://support.microsoft.com/office/change-formula-recalculation-iteration-or-precision-in-excel-73fc7dac-91cf-4d36-86e8-67124f6bcce4#ID0EAACAAA=Windows) in the Excel template that is being used:</span></span>

- <span data-ttu-id="592ac-199">生成されたドキュメントに新しい範囲やセルなどが追加されるたびに、すべての従属数式を再計算するには、**自動** を選択します。</span><span class="sxs-lookup"><span data-stu-id="592ac-199">Select **Automatic** to recalculate all dependent formulas every time a generated document is appended by new ranges, cells, etc.</span></span>
    >[!NOTE]
    > <span data-ttu-id="592ac-200">これにより、複数の関連する数式を含む Excel テンプレートでパフォーマンスの問題が発生する可能性があります。</span><span class="sxs-lookup"><span data-stu-id="592ac-200">This might cause a performance issue for Excel templates that contain multiple related formulas.</span></span>
- <span data-ttu-id="592ac-201">ドキュメントの生成時に数式の再計算を回避するには、**手動** を選択します。</span><span class="sxs-lookup"><span data-stu-id="592ac-201">Select **Manual** to avoid formula recalculation when a document is generated.</span></span>
    >[!NOTE]
    > <span data-ttu-id="592ac-202">生成されたドキュメントを Excel でプレビュー用に開くと、数式の再計算が手動で強制されます。</span><span class="sxs-lookup"><span data-stu-id="592ac-202">Formula recalculation is manually forced when a generated document is opened for preview using Excel.</span></span>
    > <span data-ttu-id="592ac-203">このオプションは、生成されたドキュメントに数式を含むセルの値が含まれていない可能性があるため、Excel でのプレビューなしで生成されたドキュメント (PDF の変換、電子メールなど) の使用を想定する ER 送信先を構成する場合は、使用しないでください。</span><span class="sxs-lookup"><span data-stu-id="592ac-203">Don't use this option if you configure an ER destination that assumes the usage of a generated document without its preview in Excel (PDF conversion, emailing, etc.)because the generated document might not contain values in cells that contain formulas.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="592ac-204">追加リソース</span><span class="sxs-lookup"><span data-stu-id="592ac-204">Additional resources</span></span>

[<span data-ttu-id="592ac-205">電子申告の概要</span><span class="sxs-lookup"><span data-stu-id="592ac-205">Electronic Reporting overview</span></span>](general-electronic-reporting.md)

[<span data-ttu-id="592ac-206">OPENXML 形式のレポートを生成するコンフィギュレーションを設計する</span><span class="sxs-lookup"><span data-stu-id="592ac-206">Design a configuration for generating reports in OPENXML format</span></span>](tasks\er-design-reports-openxml-2016-11.md)

[<span data-ttu-id="592ac-207">Excel テンプレートを再適用して電子申告形式を変更する</span><span class="sxs-lookup"><span data-stu-id="592ac-207">Modify Electronic reporting formats by reapplying Excel templates</span></span>](modify-electronic-reporting-format-reapply-excel-template.md)

[<span data-ttu-id="592ac-208">水平方向に拡張可能な範囲を活用して、Excel のレポートで動的に列を追加する</span><span class="sxs-lookup"><span data-stu-id="592ac-208">Use horizontally expandable ranges to dynamically add columns in Excel reports</span></span>](tasks/er-horizontal-1.md)

[<span data-ttu-id="592ac-209">ER を使用して生成されるドキュメントへの画像や図形の埋め込み</span><span class="sxs-lookup"><span data-stu-id="592ac-209">Embed images and shapes in documents that you generate by using ER</span></span>](electronic-reporting-embed-images-shapes.md)

[<span data-ttu-id="592ac-210">Power BI にデータをプルするよう電子申告 (ER) を構成する</span><span class="sxs-lookup"><span data-stu-id="592ac-210">Configure Electronic reporting (ER) to pull data into Power BI</span></span>](general-electronic-reporting-report-configuration-get-data-powerbi.md)
