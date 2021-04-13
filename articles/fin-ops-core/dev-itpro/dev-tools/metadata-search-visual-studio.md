---
title: Visual Studio でのメタデータの検索
description: この記事では、メタデータ検索を使用して、任意のパターンやコンテンツのコードとメタデータを検索する方法について説明します。
author: RobinARH
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Developer
ms.reviewer: rhaertle
ms.custom: 83303
ms.assetid: 4d686948-a78d-48fa-bbf8-28da7880eec7
ms.search.region: Global
ms.author: jorisde
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 286259a1bab5348087a190b79304a10e1a59ead4
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/31/2021
ms.locfileid: "5744537"
---
# <a name="metadata-search-in-visual-studio"></a><span data-ttu-id="b75ec-103">Visual Studio でのメタデータの検索</span><span class="sxs-lookup"><span data-stu-id="b75ec-103">Metadata search in Visual Studio</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="b75ec-104">この記事では、メタデータ検索を使用して、任意のパターンやコンテンツのコードとメタデータを検索する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="b75ec-104">This article describes how to use metadata search to search your code and metadata for arbitrary patterns and content.</span></span>

<span data-ttu-id="b75ec-105">大量のコード ベースおよびメタデータを考えると、多くの場合特定の基準を満たすコード内のものを検索する必要があります。</span><span class="sxs-lookup"><span data-stu-id="b75ec-105">Given the large volume of the code base and metadata, it is often necessary to find things in the code that meet a certain criteria.</span></span> <span data-ttu-id="b75ec-106">たとえば、パターンを含む、または基準を満たしているメタデータ要素の名前が分からない場合があります。</span><span class="sxs-lookup"><span data-stu-id="b75ec-106">For example, you might not know the name of the metadata element that contains the pattern or meets the criteria.</span></span> <span data-ttu-id="b75ec-107">メタデータ検索は、メタデータ検索ツール ウィンドウと移動先ウィンドウの 2 つのユーザー インターフェイスを通じて Visual Studio で公開されます。</span><span class="sxs-lookup"><span data-stu-id="b75ec-107">Metadata search is exposed in Visual Studio through two user interfaces: the Metadata Search tool window and the Navigate To window.</span></span>

## <a name="metadata-search-tool-window"></a><span data-ttu-id="b75ec-108">メタデータ検索ツール ウィンドウ</span><span class="sxs-lookup"><span data-stu-id="b75ec-108">Metadata search tool window</span></span>

<span data-ttu-id="b75ec-109">メタデータ検索ツール ウィンドウには **Dynamics 365 &gt; メタデータ検索** メニュー コマンドからアクセスすることができます。</span><span class="sxs-lookup"><span data-stu-id="b75ec-109">You can access the Metadata search tool window from the **Dynamics 365 &gt; Metadata Search** menu command.</span></span> <span data-ttu-id="b75ec-110">検索クエリを入力して検索を開始します。</span><span class="sxs-lookup"><span data-stu-id="b75ec-110">Enter your search query to start the search.</span></span> <span data-ttu-id="b75ec-111">結果は、入力と同時にウィンドウへの入力が非同期で開始されます。</span><span class="sxs-lookup"><span data-stu-id="b75ec-111">Results will start populating in the window asynchronously as you type.</span></span> <span data-ttu-id="b75ec-112">任意の結果行をダブルクリックして、検索クエリに一致する、対応する X++ コードまたはメタデータに移動することができます。</span><span class="sxs-lookup"><span data-stu-id="b75ec-112">You can double-click any result line to navigate to the corresponding X++ code or metadata that matches your search query.</span></span>

<span data-ttu-id="b75ec-113">[![メタデータ検索ツール ウィンドウ](./media/posted_metasearch.png)](./media/posted_metasearch.png)</span><span class="sxs-lookup"><span data-stu-id="b75ec-113">[![Metadata search tool window](./media/posted_metasearch.png)](./media/posted_metasearch.png)</span></span>

<span data-ttu-id="b75ec-114">また、1 つまたは複数の結果を選択して、右クリックし、これらの要素をプロジェクトに追加することができます。</span><span class="sxs-lookup"><span data-stu-id="b75ec-114">You can also select one or more results, right-click, and then add these elements to a project.</span></span> <span data-ttu-id="b75ec-115">検索結果とやりとりを開始するまで、検索の完了を待機する必要はありません。</span><span class="sxs-lookup"><span data-stu-id="b75ec-115">You don’t need to wait for the search to complete before you start interacting with the search results.</span></span>

<span data-ttu-id="b75ec-116">[![メタデータ検索から新しいプロジェクトへの追加](./media/addnewproject_metasearch.png)](./media/addnewproject_metasearch.png)</span><span class="sxs-lookup"><span data-stu-id="b75ec-116">[![Add to new project from metadata search](./media/addnewproject_metasearch.png)](./media/addnewproject_metasearch.png)</span></span>

## <a name="navigate-to-window"></a><span data-ttu-id="b75ec-117">ウィンドウへの移動</span><span class="sxs-lookup"><span data-stu-id="b75ec-117">Navigate To window</span></span>

<span data-ttu-id="b75ec-118">**移動先** ウィンドウは、**Ctrl + ','** (コンマ区切り記号) ショートカット キーを使用して呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="b75ec-118">The **Navigate To** window is invoked using the **Ctrl+‘,’** (the comma character) shortcut keys.</span></span> <span data-ttu-id="b75ec-119">**Ctrl+‘,’** キーを押すと、Visual Studio の主要なドキュメント ウィンドウの右上隅にクエリ エントリ ボックスが表示されます。</span><span class="sxs-lookup"><span data-stu-id="b75ec-119">Pressing **Ctrl+‘,’** displays the query entry box in top-right corner of the Visual Studio main document window.</span></span> <span data-ttu-id="b75ec-120">また、Visual Studio の **編集** メニューから **移動先** ウィンドウにアクセスすることができます。</span><span class="sxs-lookup"><span data-stu-id="b75ec-120">You can also access the **Navigate To** window from the Visual Studio **Edit** menu.</span></span> <span data-ttu-id="b75ec-121">クエリを検索し、入力時に結果が表示されることを確認します。</span><span class="sxs-lookup"><span data-stu-id="b75ec-121">Enter you search query and see the results appear as you type.</span></span> <span data-ttu-id="b75ec-122">検索が完了したら、進行状況インジケーターが停止します。</span><span class="sxs-lookup"><span data-stu-id="b75ec-122">A progress indicator will stop when the search is complete.</span></span> <span data-ttu-id="b75ec-123">結果とやりとりを開始するために、検索の完了を待機する必要はありません。</span><span class="sxs-lookup"><span data-stu-id="b75ec-123">You don’t need to wait for the search to complete to start interacting with the results.</span></span>

<span data-ttu-id="b75ec-124">[![ウィンドウへの移動](./media/typeform_metasearch.png)](./media/typeform_metasearch.png)</span><span class="sxs-lookup"><span data-stu-id="b75ec-124">[![Navigate To window](./media/typeform_metasearch.png)](./media/typeform_metasearch.png)</span></span>

## <a name="search-query-syntax"></a><span data-ttu-id="b75ec-125">クエリ構文を検索</span><span class="sxs-lookup"><span data-stu-id="b75ec-125">Search query syntax</span></span>

<span data-ttu-id="b75ec-126">ここでは、検索クエリの構文について説明し、クエリの例を示します。</span><span class="sxs-lookup"><span data-stu-id="b75ec-126">This section describes the search query syntax and provides example queries.</span></span>

### <a name="syntax"></a><span data-ttu-id="b75ec-127">構文</span><span class="sxs-lookup"><span data-stu-id="b75ec-127">Syntax</span></span>

<span data-ttu-id="b75ec-128">検索クエリは、この一般的なフォームの一連のフィルターで構成される検索文字列です。</span><span class="sxs-lookup"><span data-stu-id="b75ec-128">The search query is a search string that consists of a set of filters in this general form:</span></span>

```xml
<filter_1>:<filter_1_value> [<filter_2>:<filter_2_value> … [ <filter_N>:<filter_N\_value>]]
```

<span data-ttu-id="b75ec-129">`<filter_i>` は、許容されるフィルター名の 1 つであり、<`filter_i_value>` はコンマで区切られた (場合によっては引用符で括られた) フィルター値です。</span><span class="sxs-lookup"><span data-stu-id="b75ec-129">Where `<filter_i>` is one of the acceptable filter names, and <`filter_i_value>` are comma separated (and possibly quoted) filtering values.</span></span>

### <a name="filter-names"></a><span data-ttu-id="b75ec-130">フィルター名</span><span class="sxs-lookup"><span data-stu-id="b75ec-130">Filter names</span></span>

- <span data-ttu-id="b75ec-131">**名前**: 要素名ごとのフィルター処理。</span><span class="sxs-lookup"><span data-stu-id="b75ec-131">**Name**: Filter by element name.</span></span> <span data-ttu-id="b75ec-132">これは既定のフィルターです。つまり、フィルター値を入力するだけで要素名とみなされます。</span><span class="sxs-lookup"><span data-stu-id="b75ec-132">This is the default filter, meaning if you just type a filter value, it is assumed to be an element name.</span></span> <span data-ttu-id="b75ec-133">各コンマ区切り値は、許容可能な要素名です。</span><span class="sxs-lookup"><span data-stu-id="b75ec-133">Each comma-separated value is an acceptable element name.</span></span>
- <span data-ttu-id="b75ec-134">**タイプ**: 要素タイプでフィルター処理してください。</span><span class="sxs-lookup"><span data-stu-id="b75ec-134">**Type**: Filter by element type.</span></span> <span data-ttu-id="b75ec-135">各コンマ区切り値は、要素またはサブ要素タイプ (ルート タイプまたはサブタイプ) (つまりテーブル、クラス、フィールドなど) の名前にする必要があります。</span><span class="sxs-lookup"><span data-stu-id="b75ec-135">Each comma-separated value should be the name of an element or subelement type (root type or subtype) (that is, table, class, field).</span></span> <span data-ttu-id="b75ec-136">フィルター処理のロジックは次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="b75ec-136">Logic of filtering is:</span></span>

    `(roottype_1 OR roottype_2 OR … OR roottype_N) AND (subtype_1 OR subtype_2 OR … OR subtype_N)`

- <span data-ttu-id="b75ec-137">**モデル**: モデル名ごとのフィルター。</span><span class="sxs-lookup"><span data-stu-id="b75ec-137">**Model**: Filter by model name.</span></span> <span data-ttu-id="b75ec-138">各コンマ区切り値は、アプリケーションのモデル名にする必要があります。</span><span class="sxs-lookup"><span data-stu-id="b75ec-138">Each comma-separated value should be the name of a model in your application.</span></span>
- <span data-ttu-id="b75ec-139">**プロパティ**: プロパティ フィルターを適用します。</span><span class="sxs-lookup"><span data-stu-id="b75ec-139">**Property**: Apply property filters.</span></span> <span data-ttu-id="b75ec-140">各コンマ区切り値は、フォーム `property_name=property_value` に含まれている必要があります。</span><span class="sxs-lookup"><span data-stu-id="b75ec-140">Each comma-separated value should be in the form `property_name=property_value`.</span></span>
- <span data-ttu-id="b75ec-141">**コード**: コード スニペットを使用してフィルタ処理し、コード スニペットを引用符で囲みます。</span><span class="sxs-lookup"><span data-stu-id="b75ec-141">**Code**: Filter using code snippets, use quotes around code snippets.</span></span> <span data-ttu-id="b75ec-142">一致するソース コードは、指定されたコード スニペットを含む要素です。</span><span class="sxs-lookup"><span data-stu-id="b75ec-142">The matching source code is the elements that contain the specified code snippet.</span></span>

<span data-ttu-id="b75ec-143">検索ボックスで使用可能なドロップダウンリスト メニューを開いて、フィルターおよびフィルター構文の使用に関するヘルプを取得することができます。</span><span class="sxs-lookup"><span data-stu-id="b75ec-143">You can get help about using filter and filter syntax by opening the drop-down menu available in the search box.</span></span>

<span data-ttu-id="b75ec-144">[</span><span class="sxs-lookup"><span data-stu-id="b75ec-144">[</span></span>![メタデータ検索フィルター ボタン](./media/metadatasearchfilter.jpg)<span data-ttu-id="b75ec-146">]</span><span class="sxs-lookup"><span data-stu-id="b75ec-146">]</span></span>

## <a name="examples"></a><span data-ttu-id="b75ec-147">例</span><span class="sxs-lookup"><span data-stu-id="b75ec-147">Examples</span></span>

| <span data-ttu-id="b75ec-148">クエリ文字列</span><span class="sxs-lookup"><span data-stu-id="b75ec-148">Query string</span></span>   | <span data-ttu-id="b75ec-149">目的</span><span class="sxs-lookup"><span data-stu-id="b75ec-149">What it does</span></span>       |
|--------------------------------|--------------------------------|
|`TrvExpTable` | <span data-ttu-id="b75ec-150">トークンが単独である場合は、それは名前と見なされます。</span><span class="sxs-lookup"><span data-stu-id="b75ec-150">If the token is by itself, it is assumed to be the name.</span></span> <span data-ttu-id="b75ec-151">したがって、名前に 「TrvExpTable」 を持つアプリケーションのすべてのものが検出されます。</span><span class="sxs-lookup"><span data-stu-id="b75ec-151">So this will find everything in the application that has "TrvExpTable" in the name.</span></span> |
|`type:form ccount`  | <span data-ttu-id="b75ec-152">その名前に 「ccount」 を持つすべてのフォームを検索します。</span><span class="sxs-lookup"><span data-stu-id="b75ec-152">Finds all forms that have "ccount" in their names.</span></span>   |
|`type:form property:formtemplate=listpage` | <span data-ttu-id="b75ec-153">「ListPage」 に等しいプロパティ 「FormTemplate」 を含む、すべてのフォームを検索します。</span><span class="sxs-lookup"><span data-stu-id="b75ec-153">Finds all forms that contain the property "FormTemplate" equal to ‘ListPage’.</span></span>       |
|`type:table,formDesign property:"WorkflowDataSource=TrvExpTable"`              | <span data-ttu-id="b75ec-154">テーブルの下で formDesign ノードを検索しますが、何も見つかりません。</span><span class="sxs-lookup"><span data-stu-id="b75ec-154">Finds formDesign nodes under tables, nothing would be found.</span></span>  |
|`type:form,formmenufunctionbuttoncontrol property:Text=@SYS311998` | <span data-ttu-id="b75ec-155">(ラベル) 「@SYS311998」に等しいテキスト プロパティを含むすべてのメニュー機能ボタン コントロールを検索します。</span><span class="sxs-lookup"><span data-stu-id="b75ec-155">Finds all menu function button controls with the Text property equal to (a label) ‘@SYS311998’.</span></span>                        |
|`type:table,method name:insert` | <span data-ttu-id="b75ec-156">メソッドの名前に 「insert」 を含むメソッドで、テーブルを検索します。</span><span class="sxs-lookup"><span data-stu-id="b75ec-156">Finds tables with a method containing "insert" in the method name.</span></span> |
|`type:table,tableindex name:Export` | <span data-ttu-id="b75ec-157">「Export」 の単語を含むインデックス名で、テーブルを検索します。</span><span class="sxs-lookup"><span data-stu-id="b75ec-157">Finds tables with an index name containing the word "Export".</span></span> |
|`type:table,tableindexfield name:xpNum` | <span data-ttu-id="b75ec-158">インデックス フィールド名の 「xpNum」 で、テーブル インデックスを検索します。</span><span class="sxs-lookup"><span data-stu-id="b75ec-158">Finds table indexes with "xpNum" in the index field name.</span></span> |
|`type:table,tablefieldgroup name:EPNew`  |<span data-ttu-id="b75ec-159">その名前内で「EPNew」を含む FieldGroups (テーブル内) を検索します。</span><span class="sxs-lookup"><span data-stu-id="b75ec-159">Finds FieldGroups (in tables) containing ‘EPNew’ in their names.</span></span> |
|`type:form,formgridcontrol property:allowedit=no,heightmode=column` | <span data-ttu-id="b75ec-160">「いいえ」に等しいプロパティ **allowedit** および「列」に等しい heightmode を持つ、グリッド コントロールのフォームを検索します。</span><span class="sxs-lookup"><span data-stu-id="b75ec-160">Finds form grid controls, with properties **allowedit** equal to "no" and heightmode equal to "column".</span></span> |
|`type:form,formtabcontrol property:arrangeMethod=Vertical,ViewEditMode=view,WidthMode=Auto` |  <span data-ttu-id="b75ec-161">「垂直」に等しい arrangeMethod、「ビュー」に等しい ViewEditMode および「自動」に等しい WidthMode のプロパティを持つ、タブ コントロールのフォームを検索します。</span><span class="sxs-lookup"><span data-stu-id="b75ec-161">Finds form tab controls, with properties arrangeMethod equal to "Vertical" and ViewEditMode equal to "view" and WidthMode equal to "Auto".</span></span>  |
|`type:form,formDesign property:"WorkflowDataSource=TrvExpTable"` |<span data-ttu-id="b75ec-162">「TrvExpTable」の値に設定する FormDesign ノードで、「WorkflowDataSource」 プロパティを持つすべてのフォームを検索します。</span><span class="sxs-lookup"><span data-stu-id="b75ec-162">Finds all forms with the "WorkflowDataSource" property in the FormDesign node set to the value "TrvExpTable".</span></span>                 |
|`model:”Application Suite” type:formdesign property:style=simplelistdetail` | <span data-ttu-id="b75ec-163">FormDesign ノードで simpleListDetail に設定するスタイル プロパティを持つ、アプリケーション スイート モデル内のすべてのフォームを検索します。</span><span class="sxs-lookup"><span data-stu-id="b75ec-163">Find all forms in Application Suite model that has the style property set to simpleListDetail in the FormDesign node.</span></span>             |
|`code:"return null"` | <span data-ttu-id="b75ec-164">「null を返す」を含むソース コード内で、すべての場所を検索します。</span><span class="sxs-lookup"><span data-stu-id="b75ec-164">Finds all places in the source code that contains "return null".</span></span> |
|`code:"element.lock()" type:form`   | <span data-ttu-id="b75ec-165">スニペット 「element.lock()」 を含むソース コードのフォームで、すべての場所を検索します。</span><span class="sxs-lookup"><span data-stu-id="b75ec-165">Finds all places in the forms source code that contain the snippet "element.lock()".</span></span>   |
|`code:"insert" type:table,form`    | <span data-ttu-id="b75ec-166">「挿入」を含むフォームまたはテーブルのいずれかのソース コード内で、すべての場所を検索します。</span><span class="sxs-lookup"><span data-stu-id="b75ec-166">Finds all places in the source code of either forms or tables that contain "insert".</span></span>   |
|`code:"public display" type:form,method`  | <span data-ttu-id="b75ec-167">「公開表示」のコードを含む、すべてのフォーム メソッドを検索します。</span><span class="sxs-lookup"><span data-stu-id="b75ec-167">Finds all form methods that contain the code "public display".</span></span> |
|`type:formbuttoncontrol property:text=` | <span data-ttu-id="b75ec-168">**空** テキスト プロパティを持つ、すべてのフォームのボタン コントロールを検索します。</span><span class="sxs-lookup"><span data-stu-id="b75ec-168">Finds all form Button Controls that have **empty** text properties.</span></span> |


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]