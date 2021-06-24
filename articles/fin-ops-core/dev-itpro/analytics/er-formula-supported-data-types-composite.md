---
title: 電子レポートの式でサポートされる複合データ型
description: このトピックでは、電子申告 (ER) の式でサポートされる複合データ型について説明します。
author: NickSelin
ms.date: 06/02/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ERDataModelDesigner, ERExpressionDesignerFormula, ERMappedFormatDesigner, ERModelMappingDesigner
audience: Application User, IT Pro
ms.reviewer: kfend
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: c7ed9e62751b6be9fad6de3bf262d37d7977d192
ms.sourcegitcommit: 15aacd0e109b05c7281407b5bba4e6cd99116c28
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/10/2021
ms.locfileid: "6224100"
---
# <a name="supported-composite-data-types-for-electronic-reporting-formulas"></a><span data-ttu-id="7748f-103">電子レポートの式でサポートされる複合データ型</span><span class="sxs-lookup"><span data-stu-id="7748f-103">Supported composite data types for Electronic reporting formulas</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="7748f-104">このトピックでは、[電子申告 (ER)](general-electronic-reporting.md)の式でサポートされる複合データ型について説明します。</span><span class="sxs-lookup"><span data-stu-id="7748f-104">This topic provides information about the composite data types that are supported in [Electronic reporting (ER)](general-electronic-reporting.md) expressions.</span></span> <span data-ttu-id="7748f-105">複合データ型は、[クラス](#class)、[コンテナー](#container)、[レコード](#record)、[レコード リスト](#record-list)、[オブジェクト](#object) です 。</span><span class="sxs-lookup"><span data-stu-id="7748f-105">The composite data types are [class](#class), [container](#container), [record](#record), [record list](#record-list), and [object](#object).</span></span>

## <a name="class"></a><a name="class"></a><span data-ttu-id="7748f-106">クラス</span><span class="sxs-lookup"><span data-stu-id="7748f-106">Class</span></span>

<span data-ttu-id="7748f-107">データ型: *クラス* は、パブリック アプリケーション クラスを参照します。</span><span class="sxs-lookup"><span data-stu-id="7748f-107">The *class* data type refers to a public application class.</span></span> <span data-ttu-id="7748f-108">ERでは、参照されるクラスのすべてのパブリック メソッドに対して個別のフィールドを含む [*レコード*](#record) として表現されます。</span><span class="sxs-lookup"><span data-stu-id="7748f-108">In ER, it's represented as a [*record*](#record) that contains a separate field for every public method of the referenced class.</span></span> <span data-ttu-id="7748f-109">メソッドの呼び出しがパラメータ化されている場合は、メソッドを呼び出す構成がされている ER 式の中で、適切なタイプの必要な引数も指定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="7748f-109">When the call of the method is parameterized, you must also specify the required arguments of the appropriate types in an ER expression that is configured to call the method.</span></span>

<span data-ttu-id="7748f-110">ER [マッピング](general-electronic-reporting.md#data-model-and-model-mapping-components) および [フォーマット](general-electronic-reporting.md#FormatComponentOutbound) のコンポーネントでは、データソースとして提示され、*クラス* タイプの値を返す **クラス** データソースを追加することができます。</span><span class="sxs-lookup"><span data-stu-id="7748f-110">In ER [mapping](general-electronic-reporting.md#data-model-and-model-mapping-components) and [format](general-electronic-reporting.md#FormatComponentOutbound) components, you can add the **Class** data source that is presented as a data source and that returns a value of the *class* type.</span></span> <span data-ttu-id="7748f-111">このデータ ソースは、実行時に呼び出すクラスのパブリック メソッドを公開しています。</span><span class="sxs-lookup"><span data-stu-id="7748f-111">This data source exposes public methods of the class that can be called at runtime.</span></span>

> [!NOTE]
> <span data-ttu-id="7748f-112">値を返すメソッドのみを ER 式から呼び出できます。</span><span class="sxs-lookup"><span data-stu-id="7748f-112">Only methods that return a value can be called from ER expressions.</span></span>
>
> <span data-ttu-id="7748f-113">ER 式から呼び出することができるのは、0 から 8 の範囲の引数を持つメソッドのみです。</span><span class="sxs-lookup"><span data-stu-id="7748f-113">Only methods that have a range of zero to eight arguments can be called from ER expressions.</span></span>

<span data-ttu-id="7748f-114">*クラス* の既定値は **null 値** です。</span><span class="sxs-lookup"><span data-stu-id="7748f-114">The default value of a *class* is **null**.</span></span>

<span data-ttu-id="7748f-115">次の図では、 **クラス** タイプの **System information(xInfo)** データソースを追加して **xInfo** アプリケーション クラスのインスタンスを作成し、その **productName()** メソッドを呼び出して現在のアプリケーションの名前を受け取る方法を表わしています。</span><span class="sxs-lookup"><span data-stu-id="7748f-115">The following illustration shows how the **System information(xInfo)** data source of the **Class** type is added to make the instance of the **xInfo** application class and call its **productName()** method to receive the name of the current application.</span></span> <span data-ttu-id="7748f-116">現在のアプリケーションの名前は、ER データモデルの **ソフトウェア名 (SoftwareName)** フィールドに設定された `xInfo.productName` バインドの実行により、ランタイムに取得されます。</span><span class="sxs-lookup"><span data-stu-id="7748f-116">The name of the current application is fetched at runtime by execution of the `xInfo.productName` binding that was configured for the **Software name(SoftwareName)** field of the ER data model.</span></span> <span data-ttu-id="7748f-117">このバインドは、現在のモデル・マッピングで **システム情報 (xInfo)** データ ソースとして表現されている **xInfo** アプリケーション・クラスの `productName()` メソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="7748f-117">This binding calls the `productName()` method of the **xInfo** application class that is represented in the current model mapping as the **System information(xInfo)** data source.</span></span>

<span data-ttu-id="7748f-118">[![ER モデル マッピング デザイナーでのクラス データ ソースの構成](./media/er-formula-supported-data-types-composite-class1.gif)](./media/er-formula-supported-data-types-composite-class1.gif)</span><span class="sxs-lookup"><span data-stu-id="7748f-118">[![Configuring a Class data source in the ER model mapping designer](./media/er-formula-supported-data-types-composite-class1.gif)](./media/er-formula-supported-data-types-composite-class1.gif)</span></span>

<span data-ttu-id="7748f-119">以下の図は、生成されたドキュメントに提供されたアプリケーション名を入れる ER フォーマットの設定です。</span><span class="sxs-lookup"><span data-stu-id="7748f-119">The following illustration shows how the ER format is configured to put the provided application name in generated documents.</span></span> <span data-ttu-id="7748f-120">使用したデータモデルの **ソフトウェア名 (SoftwareName)** フィールドは、ER フォーマットの **softwareUsed** XML 要素の下に入れ子になっている **String** コンポーネントにバインドされます。</span><span class="sxs-lookup"><span data-stu-id="7748f-120">The **Software name(SoftwareName)** field of the used data model was bound to the **String** component that is nested under the **softwareUsed** XML element of the ER format.</span></span> <span data-ttu-id="7748f-121">そのため、現在のアプリケーションの名前は、XML形式で生成されたドキュメントの **softwareUsed** XML要素にランタイムで配置されます。</span><span class="sxs-lookup"><span data-stu-id="7748f-121">So, the name of the current application is placed at runtime to the **softwareUsed** XML element of a generated document in XML format.</span></span>

<span data-ttu-id="7748f-122">[![ER 形式デザイナでの電子発信ドキュメントの構造の構成](./media/er-formula-supported-data-types-composite-class2.png)](./media/er-formula-supported-data-types-composite-class2.png)</span><span class="sxs-lookup"><span data-stu-id="7748f-122">[![Configuring the structure of an electronic outbound document in the ER format designer](./media/er-formula-supported-data-types-composite-class2.png)](./media/er-formula-supported-data-types-composite-class2.png)</span></span>

## <a name="container"></a><a name="container"></a><span data-ttu-id="7748f-123">コンテナー</span><span class="sxs-lookup"><span data-stu-id="7748f-123">Container</span></span>

<span data-ttu-id="7748f-124">*コンテナ* データ 型はバイナリ コンテンツを保持します。</span><span class="sxs-lookup"><span data-stu-id="7748f-124">The *container* data type holds binary content.</span></span> <span data-ttu-id="7748f-125">*コンテナー* 値は、ストレージから生成されたドキュメントに特定の情報を渡すために使用できます。</span><span class="sxs-lookup"><span data-stu-id="7748f-125">A *container* value can be used to pass specific information from storage to a generated document.</span></span> <span data-ttu-id="7748f-126">このデータタイプは、ER フレームワークでは、生成されたドキュメントに会社のロゴなどのメディア コンテンツを入れるためによく使われます。</span><span class="sxs-lookup"><span data-stu-id="7748f-126">In the ER framework, this data type is frequently used to put media content such as a company logo in generated documents.</span></span>

> [!NOTE]
> <span data-ttu-id="7748f-127">すべてのメディア アイテムは *コンテナー* 値として表現できますが、すべての *コンテナー* 値がメディア アイテムを表すわけではありません。</span><span class="sxs-lookup"><span data-stu-id="7748f-127">Although every media item can be represented as a *container* value, not every *container* value represents a media item.</span></span> <span data-ttu-id="7748f-128">そのため、ER形式を構成して、*コンテナー* を使用して生成されたドキュメントに画像を格納する場合に、参照先の *コンテナー* がメディア コンテンツを返さない場合、次のような例外が発生する可能性があります: 「コードの実行エラー: バイナリ (object) メソッドの method constructFromContainer が無効なパラメーターを呼び出しました」。</span><span class="sxs-lookup"><span data-stu-id="7748f-128">Therefore, if you configure an ER format so that it uses a *container* to put an image in generated documents, but the referenced *container* doesn't return media content, an exception that resembles the following example might be thrown: "Error executing code: Binary (object), method constructFromContainer called with invalid parameters."</span></span>

<span data-ttu-id="7748f-129">*コンテナー* の既定値は **null 値** です。</span><span class="sxs-lookup"><span data-stu-id="7748f-129">The default value of a *container* is **null**.</span></span>

<span data-ttu-id="7748f-130">次の図は、**販売請求書** モデルのマッピングにおいて、*コンテナー* タイプの **ビットマップ (Image)** フィールドが、**コンテナー** タイプのデータモデル **ロゴ** フィールドにバインドされている様子を示しています。</span><span class="sxs-lookup"><span data-stu-id="7748f-130">The following illustration shows how the **Bitmap(Image)** field of the *Container* type is bound to the data model **Logo** field of the **Container** type in the **Sales invoice** model mapping.</span></span> <span data-ttu-id="7748f-131">このバインドにより、**SalesInvoice** ルート定義用に設計され、実行時にこのモデルマッピングを使用する任意の ER フォーマットで会社のロゴを使用できるようになります。</span><span class="sxs-lookup"><span data-stu-id="7748f-131">This binding makes the company logo available to any ER format that is designed for the **SalesInvoice** root definition and that uses this model mapping at runtime.</span></span>

<span data-ttu-id="7748f-132">[![ER モデル マッピング デザイナーでのコンテナー タイプのフィールドのバインド](./media/er-formula-supported-data-types-composite-container.png)](./media/er-formula-supported-data-types-composite-container.png)</span><span class="sxs-lookup"><span data-stu-id="7748f-132">[![Binding a field of the Container type in the ER model mapping designer](./media/er-formula-supported-data-types-composite-container.png)](./media/er-formula-supported-data-types-composite-container.png)</span></span>

## <a name="record"></a><a name="record"></a><span data-ttu-id="7748f-133">レコード</span><span class="sxs-lookup"><span data-stu-id="7748f-133">Record</span></span>

<span data-ttu-id="7748f-134">*レコード* とは、名前の付いたフィールドの集合で、それぞれが、[プリミティブ](er-formula-supported-data-types-primitive.md) データタイプまたはコンポジット データ タイプの値に関連付けられています。</span><span class="sxs-lookup"><span data-stu-id="7748f-134">A *record* is a collection of named fields, each of which is associated with a value of either a [primitive](er-formula-supported-data-types-primitive.md) data type or a composite data type.</span></span> <span data-ttu-id="7748f-135">通常、1 つの *レコード* を使用してレコード リストの 1 つのレコードを表します。</span><span class="sxs-lookup"><span data-stu-id="7748f-135">Usually, a *record* is used to represent a single record of a record list.</span></span> <span data-ttu-id="7748f-136">この場合、すべての品目は個々のフィールド、メソッド、関係を表します。</span><span class="sxs-lookup"><span data-stu-id="7748f-136">In this case, every item represents individual fields, methods, and relations.</span></span>

<span data-ttu-id="7748f-137"> *レコード* の既定値は **空白値** です。</span><span class="sxs-lookup"><span data-stu-id="7748f-137">The default value of a *record* is **empty**.</span></span>

> [!NOTE]
> <span data-ttu-id="7748f-138">空の *レコード* のフィールドの値を取得すると、適切なデータ型の既定の値が返されます。</span><span class="sxs-lookup"><span data-stu-id="7748f-138">When you get the value of a field of an empty *record*, the default value of the appropriate data type is returned.</span></span>

<span data-ttu-id="7748f-139">*レコード* は、次の関数を使用して取得できます。</span><span class="sxs-lookup"><span data-stu-id="7748f-139">A *record* can be obtained by using the following functions:</span></span>

- [<span data-ttu-id="7748f-140">FIRST</span><span class="sxs-lookup"><span data-stu-id="7748f-140">FIRST</span></span>](er-functions-list-first.md)
- [<span data-ttu-id="7748f-141">FIRSTORNULL</span><span class="sxs-lookup"><span data-stu-id="7748f-141">FIRSTORNULL</span></span>](er-functions-list-firstornull.md)
- [<span data-ttu-id="7748f-142">EMPTYRECORD</span><span class="sxs-lookup"><span data-stu-id="7748f-142">EMPTYRECORD</span></span>](er-functions-record-emptyrecord.md)
- [<span data-ttu-id="7748f-143">NULLCONTAINER</span><span class="sxs-lookup"><span data-stu-id="7748f-143">NULLCONTAINER</span></span>](er-functions-record-nullcontainer.md)

<span data-ttu-id="7748f-144">*レコード* 値の変換については、[リストカテゴリーのER関数一覧](er-functions-category-list.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="7748f-144">For more information about the transformation of *record* values, see [List of ER functions in the list category](er-functions-category-list.md).</span></span>

## <a name="record-list"></a><a name="record-list"></a><span data-ttu-id="7748f-145">レコード リスト</span><span class="sxs-lookup"><span data-stu-id="7748f-145">Record list</span></span>

<span data-ttu-id="7748f-146">*レコード* リストは 、その *レコード* タイプの項目の リストです。</span><span class="sxs-lookup"><span data-stu-id="7748f-146">A *record list* is a list of items of the *record* type.</span></span> <span data-ttu-id="7748f-147">通常、 *レコード リスト* は、データベース テーブルから取得されたレコードのリストを表すために使用します。</span><span class="sxs-lookup"><span data-stu-id="7748f-147">Usually, a *record list* is used to represent the list of records that has been fetched from a database table.</span></span>

<span data-ttu-id="7748f-148">既定では、*レコード リスト* の レコードは連続してアクセスされます。</span><span class="sxs-lookup"><span data-stu-id="7748f-148">By default, records of a *record list* are accessed sequentially.</span></span> <span data-ttu-id="7748f-149">特定のレコードにアクセスするために、[INDEX](er-functions-list-index.md) 関数を使用して *整数* インデックスを指定できます。</span><span class="sxs-lookup"><span data-stu-id="7748f-149">To access a specific record, you can use the [INDEX](er-functions-list-index.md) function and specify the *integer* index.</span></span>

<span data-ttu-id="7748f-150"> *レコード リスト* の既定値は **空白値** です。</span><span class="sxs-lookup"><span data-stu-id="7748f-150">The default value of a *record list* is **empty**.</span></span> <span data-ttu-id="7748f-151">[ISEMPTY](/er-functions-list-isempty.md) 関数を使用して、*レコード リスト* が空白かどうかを評価できます。</span><span class="sxs-lookup"><span data-stu-id="7748f-151">You can use the [ISEMPTY](/er-functions-list-isempty.md) function to evaluate whether a *record list* is empty.</span></span>

> [!NOTE]
> <span data-ttu-id="7748f-152">*レコード リスト* が空白の場合、その中の *レコード* のフィールド値を取得しようとすると、実行時の例外エラーが発生します。</span><span class="sxs-lookup"><span data-stu-id="7748f-152">If a *record list* is empty, any attempt to get a field value for a *record* in it causes an exception to be thrown at runtime.</span></span> <span data-ttu-id="7748f-153">このタイプのランタイム例外エラーの回避方法については、[空のリストケースを考慮する](er-components-inspections.md#i9) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="7748f-153">To learn how you can help prevent runtime exceptions of this type, see [Consideration of empty list cases](er-components-inspections.md#i9).</span></span>

<span data-ttu-id="7748f-154">*レコード リスト* は、次の関数を使用して開始できます:</span><span class="sxs-lookup"><span data-stu-id="7748f-154">A *record list* can be initiated by using the following functions:</span></span>

- [<span data-ttu-id="7748f-155">ALLITEMS</span><span class="sxs-lookup"><span data-stu-id="7748f-155">ALLITEMS</span></span>](er-functions-list-allitems.md)
- [<span data-ttu-id="7748f-156">ALLITEMSQUERY</span><span class="sxs-lookup"><span data-stu-id="7748f-156">ALLITEMSQUERY</span></span>](er-functions-list-allitemsquery.md)
- [<span data-ttu-id="7748f-157">EMPTYLIST</span><span class="sxs-lookup"><span data-stu-id="7748f-157">EMPTYLIST</span></span>](er-functions-list-emptylist.md)
- [<span data-ttu-id="7748f-158">LIST</span><span class="sxs-lookup"><span data-stu-id="7748f-158">LIST</span></span>](er-functions-list-list.md)
- [<span data-ttu-id="7748f-159">LISTDISTINCT</span><span class="sxs-lookup"><span data-stu-id="7748f-159">LISTDISTINCT</span></span>](er-functions-list-listdistinct.md)

<span data-ttu-id="7748f-160">*レコード リスト* 値の変換については、[リスト カテゴリーの ER 関数一覧](er-functions-category-list.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="7748f-160">For more information about the transformation of *record list* values, see [List of ER functions in the list category](er-functions-category-list.md).</span></span> <span data-ttu-id="7748f-161">*レコード リスト* の項目アイテムを導入し、そこにアプリケーション データを入力し、そのデータを使ってビジネス ドキュメントを作成する方法については、[カスタム レポートを印刷する新しい ER ソリューションの設計](er-quick-start1-new-solution.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="7748f-161">To learn how to introduce *record list* items, fill them with application data, and then use the data to generate business documents, see [Design a new ER solution to print a custom report](er-quick-start1-new-solution.md).</span></span>

## <a name="object"></a><a name="object"></a><span data-ttu-id="7748f-162">オブジェクト</span><span class="sxs-lookup"><span data-stu-id="7748f-162">Object</span></span>

<span data-ttu-id="7748f-163">*オブジェクト* は、*クラス* のインスタンスを表します。</span><span class="sxs-lookup"><span data-stu-id="7748f-163">An *object* refers to a stateful instance of a *class*.</span></span> <span data-ttu-id="7748f-164">通常、*オブジェクト* は、ソース コードで開始されます。</span><span class="sxs-lookup"><span data-stu-id="7748f-164">Usually, an *object* is initiated in source code.</span></span> <span data-ttu-id="7748f-165">その後、ER モデル マッピングに渡され、実行コンテキストの詳細が提供されます。</span><span class="sxs-lookup"><span data-stu-id="7748f-165">It's then passed to an ER model mapping and provides details of the execution context.</span></span>

<span data-ttu-id="7748f-166">*オブジェクト* の既定値は **null 値** です。</span><span class="sxs-lookup"><span data-stu-id="7748f-166">The default value of an *object* is **null**.</span></span>

<span data-ttu-id="7748f-167">次の図は、*オブジェクト* タイプの **ReportDataContract** データ ソースが、ソース コードから **プロジェクト請求書** モデル マッピングに生成された請求書に関する情報を渡すように追加する方法を示しています。</span><span class="sxs-lookup"><span data-stu-id="7748f-167">The following illustration shows how the **ReportDataContract** data source of the *Object* type is added to pass information about a generated invoice from source code to the **Project invoice** model mapping.</span></span> <span data-ttu-id="7748f-168">たとえば、請求書インスタンスのテキストは、実行コンテキストの一部として渡されます。</span><span class="sxs-lookup"><span data-stu-id="7748f-168">For example, the invoice instance text is passed as part of the execution context.</span></span> <span data-ttu-id="7748f-169">このテキストは、ER データモデルの **注記** フィールド用に設定された `ReportDataContract.parmInvoiceInstanceText` バインドの実行により、ランタイムにソースコードから取得されます。</span><span class="sxs-lookup"><span data-stu-id="7748f-169">This text is taken from source code at runtime by execution of the `ReportDataContract.parmInvoiceInstanceText` binding that was configured for the **Note** field of the ER data model.</span></span> <span data-ttu-id="7748f-170">このバインドは、現在のモデル・マッピングで **ReportDataContract** データ ソースとして表現されている **PSAProjInvoiceContract** アプリケーション・クラスの `parmInvoiceInstanceText()` メソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="7748f-170">This binding calls the `parmInvoiceInstanceText()` method of the **PSAProjInvoiceContract** application class that is represented in the current model mapping as the **ReportDataContract** data source.</span></span>

<span data-ttu-id="7748f-171">[![ER モデル マッピング デザイナーでのオブジェクト データ ソースの構成](./media/er-formula-supported-data-types-composite-object.gif)](./media/er-formula-supported-data-types-composite-object.gif)</span><span class="sxs-lookup"><span data-stu-id="7748f-171">[![Configuring an Object data source in the ER model mapping designer](./media/er-formula-supported-data-types-composite-object.gif)](./media/er-formula-supported-data-types-composite-object.gif)</span></span>

<span data-ttu-id="7748f-172">実行コンテキストの詳細を、ソース コードから実行中の ER ソリューションに渡す方法については、 [設計されたレポートを呼び出すアプリケーション アーティファクトの開発](er-quick-start1-new-solution.md#DevelopCustomCode) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="7748f-172">To learn how to pass details of the execution context from source code to the running ER solution, see [Develop application artefacts to call the designed report](er-quick-start1-new-solution.md#DevelopCustomCode).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="7748f-173">追加リソース</span><span class="sxs-lookup"><span data-stu-id="7748f-173">Additional resources</span></span>

- [<span data-ttu-id="7748f-174">電子申告の概要</span><span class="sxs-lookup"><span data-stu-id="7748f-174">Electronic Reporting overview</span></span>](general-electronic-reporting.md)
- [<span data-ttu-id="7748f-175">電子報告のフォーミュラ言語</span><span class="sxs-lookup"><span data-stu-id="7748f-175">Electronic reporting formula language</span></span>](er-formula-language.md)
- [<span data-ttu-id="7748f-176">対応しているプリミティブ データ型</span><span class="sxs-lookup"><span data-stu-id="7748f-176">Supported primitive data types</span></span>](er-formula-supported-data-types-primitive.md)
