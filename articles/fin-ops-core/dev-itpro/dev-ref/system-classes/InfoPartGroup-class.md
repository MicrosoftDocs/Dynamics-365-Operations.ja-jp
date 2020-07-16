---
title: InfoPartGroup クラス
description: このトピックでは、InfoPartGroup クラスについて説明します。
author: robinarh
manager: tonyafehr
ms.date: 06/25/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Developer
ms.reviewer: rhaertle
ms.search.scope: Operations
ms.search.region: Global
ms.author: rhaertle
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 740c0e2bf55f89d5e4cb01e471697c1b246f522e
ms.sourcegitcommit: 7b0cec2e898ef8ee33baf72f18cdd9cba0e9399c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/25/2020
ms.locfileid: "3502899"
---
# <a name="class-infopartgroup"></a><span data-ttu-id="6cf6c-103">クラス InfoPartGroup</span><span class="sxs-lookup"><span data-stu-id="6cf6c-103">Class InfoPartGroup</span></span>

[!include [banner](../../includes/banner.md)]

```xpp
class InfoPartGroup extends TreeNode
```

## <a name="remarks"></a><span data-ttu-id="6cf6c-104">備考</span><span class="sxs-lookup"><span data-stu-id="6cf6c-104">Remarks</span></span>

## <a name="examples"></a><span data-ttu-id="6cf6c-105">例</span><span class="sxs-lookup"><span data-stu-id="6cf6c-105">Examples</span></span>

## <a name="methods"></a><span data-ttu-id="6cf6c-106">メソッド</span><span class="sxs-lookup"><span data-stu-id="6cf6c-106">Methods</span></span>

| <span data-ttu-id="6cf6c-107">方法</span><span class="sxs-lookup"><span data-stu-id="6cf6c-107">Method</span></span>                                                         | <span data-ttu-id="6cf6c-108">説明</span><span class="sxs-lookup"><span data-stu-id="6cf6c-108">Description</span></span>                                                                                                                                   |
|----------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6cf6c-109">public str caption(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="6cf6c-109">public str caption(\[str value\])</span></span>                              | <span data-ttu-id="6cf6c-110">コントロールのキャプションを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="6cf6c-110">Gets or sets the caption of the control.</span></span>                                                                                                      |
| <span data-ttu-id="6cf6c-111">public str dataGroup(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="6cf6c-111">public str dataGroup(\[str value\])</span></span>                            |                                                                                                                                               |
| <span data-ttu-id="6cf6c-112">public str dataSource(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="6cf6c-112">public str dataSource(\[str value\])</span></span>                           | <span data-ttu-id="6cf6c-113">コントロールまたはフォームで使用されるデータ ソースを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="6cf6c-113">Gets or sets a data source that will be used by the control or the form.</span></span>                                                                      |
| <span data-ttu-id="6cf6c-114">public int labelPosition(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="6cf6c-114">public int labelPosition(\[int value\])</span></span>                        |                                                                                                                                               |
| <span data-ttu-id="6cf6c-115">public str name(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="6cf6c-115">public str name(\[str value\])</span></span>                                 | <span data-ttu-id="6cf6c-116">フォーム、レポート、テーブル、クエリ、または他のアプリケーション オブジェクトを識別するためのコードで使用される名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="6cf6c-116">Gets or sets the name that is used in the code to identify a form, report, table, query, or other application object.</span></span> |
| <span data-ttu-id="6cf6c-117">public boolean repeating(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="6cf6c-117">public boolean repeating(\[boolean value\])</span></span>                    |                                                                                                                                               |
| <span data-ttu-id="6cf6c-118">public int rowCountWhenSmall(\[int value\], \[AutoMode mode\])</span><span class="sxs-lookup"><span data-stu-id="6cf6c-118">public int rowCountWhenSmall(\[int value\], \[AutoMode mode\])</span></span> |                                                                                                                                               |
| <span data-ttu-id="6cf6c-119">public AutoMode rowCountWhenSmallMode(\[AutoMode mode\])</span><span class="sxs-lookup"><span data-stu-id="6cf6c-119">public AutoMode rowCountWhenSmallMode(\[AutoMode mode\])</span></span>       |                                                                                                                                               |
| <span data-ttu-id="6cf6c-120">public int rowCountWhenSmallValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="6cf6c-120">public int rowCountWhenSmallValue(\[int value\])</span></span>               |                                                                                                                                               |
| <span data-ttu-id="6cf6c-121">public boolean showCaption(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="6cf6c-121">public boolean showCaption(\[boolean value\])</span></span>                  |                                                                                                                                               |
| <span data-ttu-id="6cf6c-122">public boolean showLabels(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="6cf6c-122">public boolean showLabels(\[boolean value\])</span></span>                   |                                                                                                                                               |
| <span data-ttu-id="6cf6c-123">public int showWhenPartSize(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="6cf6c-123">public int showWhenPartSize(\[int value\])</span></span>                     |                                                                                                                                               |
| <span data-ttu-id="6cf6c-124">public boolean verticalSpacing(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="6cf6c-124">public boolean verticalSpacing(\[boolean value\])</span></span>              |                                                                                                                                               |
| <span data-ttu-id="6cf6c-125">public void new()</span><span class="sxs-lookup"><span data-stu-id="6cf6c-125">public void new()</span></span>                                              | <span data-ttu-id="6cf6c-126">InfoPartGroup クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="6cf6c-126">Initializes a new instance of the InfoPartGroup class.</span></span>                                                                                        |

## <a name="method-caption"></a><span data-ttu-id="6cf6c-127">メソッド caption</span><span class="sxs-lookup"><span data-stu-id="6cf6c-127">Method caption</span></span>

<span data-ttu-id="6cf6c-128">コントロールのキャプションを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="6cf6c-128">Gets or sets the caption of the control.</span></span>

```xpp
public str caption([str value])
```

### <a name="parameters---caption"></a><span data-ttu-id="6cf6c-129">パラメーター - caption</span><span class="sxs-lookup"><span data-stu-id="6cf6c-129">Parameters - caption</span></span>

<span data-ttu-id="6cf6c-130">値</span><span class="sxs-lookup"><span data-stu-id="6cf6c-130">value</span></span>  

### <a name="return-value---caption"></a><span data-ttu-id="6cf6c-131">戻り値 - caption</span><span class="sxs-lookup"><span data-stu-id="6cf6c-131">Return Value - caption</span></span>

<span data-ttu-id="6cf6c-132">コントロールのキャプションとして使用される文字列。</span><span class="sxs-lookup"><span data-stu-id="6cf6c-132">The string that is used as the caption of the control.</span></span>

## <a name="method-datagroup"></a><span data-ttu-id="6cf6c-133">メソッド dataGroup</span><span class="sxs-lookup"><span data-stu-id="6cf6c-133">Method dataGroup</span></span>

```xpp
public str dataGroup([str value])
```

### <a name="parameters---datagroup"></a><span data-ttu-id="6cf6c-134">パラメーター - dataGroup</span><span class="sxs-lookup"><span data-stu-id="6cf6c-134">Parameters - dataGroup</span></span>

<span data-ttu-id="6cf6c-135">値</span><span class="sxs-lookup"><span data-stu-id="6cf6c-135">value</span></span>  

### <a name="return-value---datagroup"></a><span data-ttu-id="6cf6c-136">戻り値 - dataGroup</span><span class="sxs-lookup"><span data-stu-id="6cf6c-136">Return Value - dataGroup</span></span>

## <a name="method-datasource"></a><span data-ttu-id="6cf6c-137">メソッド dataSource</span><span class="sxs-lookup"><span data-stu-id="6cf6c-137">Method dataSource</span></span>

<span data-ttu-id="6cf6c-138">コントロールまたはフォームで使用されるデータ ソースを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="6cf6c-138">Gets or sets a data source that will be used by the control or the form.</span></span>

```xpp
public str dataSource([str value])
```

### <a name="parameters---datasource"></a><span data-ttu-id="6cf6c-139">パラメーター - dataSource</span><span class="sxs-lookup"><span data-stu-id="6cf6c-139">Parameters - dataSource</span></span>

<span data-ttu-id="6cf6c-140">値</span><span class="sxs-lookup"><span data-stu-id="6cf6c-140">value</span></span>  

### <a name="return-value---datasource"></a><span data-ttu-id="6cf6c-141">戻り値 - dataSource</span><span class="sxs-lookup"><span data-stu-id="6cf6c-141">Return Value - dataSource</span></span>

<span data-ttu-id="6cf6c-142">使用されるデータ ソースの ID。</span><span class="sxs-lookup"><span data-stu-id="6cf6c-142">The identifier of the data source that will be used.</span></span>

## <a name="method-labelposition"></a><span data-ttu-id="6cf6c-143">メソッド labelPosition</span><span class="sxs-lookup"><span data-stu-id="6cf6c-143">Method labelPosition</span></span>

```xpp
public int labelPosition([int value])
```

### <a name="parameters---labelposition"></a><span data-ttu-id="6cf6c-144">パラメーター - labelPosition</span><span class="sxs-lookup"><span data-stu-id="6cf6c-144">Parameters - labelPosition</span></span>

<span data-ttu-id="6cf6c-145">値</span><span class="sxs-lookup"><span data-stu-id="6cf6c-145">value</span></span>  

### <a name="return-value---labelposition"></a><span data-ttu-id="6cf6c-146">戻り値 - labelPosition</span><span class="sxs-lookup"><span data-stu-id="6cf6c-146">Return Value - labelPosition</span></span>

## <a name="method-name"></a><span data-ttu-id="6cf6c-147">メソッド名</span><span class="sxs-lookup"><span data-stu-id="6cf6c-147">Method name</span></span>

<span data-ttu-id="6cf6c-148">フォーム、レポート、テーブル、クエリ、または他のアプリケーション オブジェクトを識別するためのコードで使用される名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="6cf6c-148">Gets or sets the name that is used in the code to identify a form, report, table, query, or other application object.</span></span>

```xpp
public str name([str value])
```

### <a name="parameters---name"></a><span data-ttu-id="6cf6c-149">パラメーター - name</span><span class="sxs-lookup"><span data-stu-id="6cf6c-149">Parameters - name</span></span>

<span data-ttu-id="6cf6c-150">値</span><span class="sxs-lookup"><span data-stu-id="6cf6c-150">value</span></span>  

### <a name="return-value---name"></a><span data-ttu-id="6cf6c-151">戻り値 - name</span><span class="sxs-lookup"><span data-stu-id="6cf6c-151">Return Value - name</span></span>

<span data-ttu-id="6cf6c-152">アプリケーション オブジェクトを識別するためにコードで使用される名前。</span><span class="sxs-lookup"><span data-stu-id="6cf6c-152">The name that is used in the code to identify an application object.</span></span>

### <a name="remarks---name"></a><span data-ttu-id="6cf6c-153">備考 - name</span><span class="sxs-lookup"><span data-stu-id="6cf6c-153">Remarks - name</span></span>

<span data-ttu-id="6cf6c-154">オブジェクトの名前プロパティ値は、コードの競合を避けるために、次の基準を満たしている必要があります。</span><span class="sxs-lookup"><span data-stu-id="6cf6c-154">The name property value of an object must meet the following criteria to avoid code conflicts:</span></span>

-   <span data-ttu-id="6cf6c-155">文字で始めます。</span><span class="sxs-lookup"><span data-stu-id="6cf6c-155">Begins with a letter.</span></span>
-   <span data-ttu-id="6cf6c-156">250 文字を超えないでください。</span><span class="sxs-lookup"><span data-stu-id="6cf6c-156">Doesn't exceed 250 characters.</span></span>
-   <span data-ttu-id="6cf6c-157">数字とアンダースコア文字を含めることができます。</span><span class="sxs-lookup"><span data-stu-id="6cf6c-157">Can include numbers and underscore characters.</span></span>
-   <span data-ttu-id="6cf6c-158">句読点やスペースを含めることはできません。</span><span class="sxs-lookup"><span data-stu-id="6cf6c-158">Cannot include punctuation or spaces.</span></span>
-   <span data-ttu-id="6cf6c-159">テーブルは、拡張データ型、基本列挙型、クラスなどの他のパブリック オブジェクトと同じ名前を持つことはできません。</span><span class="sxs-lookup"><span data-stu-id="6cf6c-159">Tables cannot have the same name as other public objects, such as extended data types, base enums, classes, and so on.</span></span>

## <a name="method-repeating"></a><span data-ttu-id="6cf6c-160">メソッド repeating</span><span class="sxs-lookup"><span data-stu-id="6cf6c-160">Method repeating</span></span>

```xpp
public boolean repeating([boolean value])
```

### <a name="parameters---repeating"></a><span data-ttu-id="6cf6c-161">パラメーター - repeating</span><span class="sxs-lookup"><span data-stu-id="6cf6c-161">Parameters - repeating</span></span>

<span data-ttu-id="6cf6c-162">値</span><span class="sxs-lookup"><span data-stu-id="6cf6c-162">value</span></span>  

### <a name="return-value---repeating"></a><span data-ttu-id="6cf6c-163">戻り値 - repeating</span><span class="sxs-lookup"><span data-stu-id="6cf6c-163">Return Value - repeating</span></span>

## <a name="method-rowcountwhensmall"></a><span data-ttu-id="6cf6c-164">メソッド rowCountWhenSmall</span><span class="sxs-lookup"><span data-stu-id="6cf6c-164">Method rowCountWhenSmall</span></span>

```xpp
public int rowCountWhenSmall([int value], [AutoMode mode])
```

### <a name="parameters---rowcountwhensmall"></a><span data-ttu-id="6cf6c-165">パラメーター - rowCountWhenSmall</span><span class="sxs-lookup"><span data-stu-id="6cf6c-165">Parameters - rowCountWhenSmall</span></span>

<span data-ttu-id="6cf6c-166">値</span><span class="sxs-lookup"><span data-stu-id="6cf6c-166">value</span></span>  

<!-- -->

<span data-ttu-id="6cf6c-167">モード</span><span class="sxs-lookup"><span data-stu-id="6cf6c-167">mode</span></span>  

### <a name="return-value---rowcountwhensmall"></a><span data-ttu-id="6cf6c-168">戻り値 - rowCountWhenSmall</span><span class="sxs-lookup"><span data-stu-id="6cf6c-168">Return Value - rowCountWhenSmall</span></span>

## <a name="method-rowcountwhensmallmode"></a><span data-ttu-id="6cf6c-169">メソッド rowCountWhenSmallMode</span><span class="sxs-lookup"><span data-stu-id="6cf6c-169">Method rowCountWhenSmallMode</span></span>

```xpp
public AutoMode rowCountWhenSmallMode([AutoMode mode])
```

### <a name="parameters---rowcountwhensmallmode"></a><span data-ttu-id="6cf6c-170">パラメーター - rowCountWhenSmallMode</span><span class="sxs-lookup"><span data-stu-id="6cf6c-170">Parameters - rowCountWhenSmallMode</span></span>

<span data-ttu-id="6cf6c-171">モード</span><span class="sxs-lookup"><span data-stu-id="6cf6c-171">mode</span></span>  

### <a name="return-value---rowcountwhensmallmode"></a><span data-ttu-id="6cf6c-172">戻り値 - rowCountWhenSmallMode</span><span class="sxs-lookup"><span data-stu-id="6cf6c-172">Return Value - rowCountWhenSmallMode</span></span>

## <a name="method-rowcountwhensmallvalue"></a><span data-ttu-id="6cf6c-173">メソッド rowCountWhenSmallValue</span><span class="sxs-lookup"><span data-stu-id="6cf6c-173">Method rowCountWhenSmallValue</span></span>

```xpp
public int rowCountWhenSmallValue([int value])
```

### <a name="parameters---rowcountwhensmallvalue"></a><span data-ttu-id="6cf6c-174">パラメーター - rowCountWhenSmallValue</span><span class="sxs-lookup"><span data-stu-id="6cf6c-174">Parameters - rowCountWhenSmallValue</span></span>

<span data-ttu-id="6cf6c-175">値</span><span class="sxs-lookup"><span data-stu-id="6cf6c-175">value</span></span>  

### <a name="return-value---rowcountwhensmallvalue"></a><span data-ttu-id="6cf6c-176">戻り値 - rowCountWhenSmallValue</span><span class="sxs-lookup"><span data-stu-id="6cf6c-176">Return Value - rowCountWhenSmallValue</span></span>

## <a name="method-showcaption"></a><span data-ttu-id="6cf6c-177">メソッド showCaption</span><span class="sxs-lookup"><span data-stu-id="6cf6c-177">Method showCaption</span></span>

```xpp
public boolean showCaption([boolean value])
```

### <a name="parameters---showcaption"></a><span data-ttu-id="6cf6c-178">パラメーター - showCaption</span><span class="sxs-lookup"><span data-stu-id="6cf6c-178">Parameters - showCaption</span></span>

<span data-ttu-id="6cf6c-179">値</span><span class="sxs-lookup"><span data-stu-id="6cf6c-179">value</span></span>  

### <a name="return-value---showcaption"></a><span data-ttu-id="6cf6c-180">戻り値 - showCaption</span><span class="sxs-lookup"><span data-stu-id="6cf6c-180">Return Value - showCaption</span></span>

## <a name="method-showlabels"></a><span data-ttu-id="6cf6c-181">メソッド showLabels</span><span class="sxs-lookup"><span data-stu-id="6cf6c-181">Method showLabels</span></span>

```xpp
public boolean showLabels([boolean value])
```

### <a name="parameters---showlabels"></a><span data-ttu-id="6cf6c-182">パラメーター - showLabels</span><span class="sxs-lookup"><span data-stu-id="6cf6c-182">Parameters - showLabels</span></span>

<span data-ttu-id="6cf6c-183">値</span><span class="sxs-lookup"><span data-stu-id="6cf6c-183">value</span></span>  

### <a name="return-value---showlabels"></a><span data-ttu-id="6cf6c-184">戻り値 - showLabels</span><span class="sxs-lookup"><span data-stu-id="6cf6c-184">Return Value - showLabels</span></span>

## <a name="method-showwhenpartsize"></a><span data-ttu-id="6cf6c-185">メソッド showWhenPartSize</span><span class="sxs-lookup"><span data-stu-id="6cf6c-185">Method showWhenPartSize</span></span>

```xpp
public int showWhenPartSize([int value])
```

### <a name="parameters---showwhenpartsize"></a><span data-ttu-id="6cf6c-186">パラメーター - showWhenPartSize</span><span class="sxs-lookup"><span data-stu-id="6cf6c-186">Parameters - showWhenPartSize</span></span>

<span data-ttu-id="6cf6c-187">値</span><span class="sxs-lookup"><span data-stu-id="6cf6c-187">value</span></span>  

### <a name="return-value---showwhenpartsize"></a><span data-ttu-id="6cf6c-188">戻り値 - showWhenPartSize</span><span class="sxs-lookup"><span data-stu-id="6cf6c-188">Return Value - showWhenPartSize</span></span>

## <a name="method-verticalspacing"></a><span data-ttu-id="6cf6c-189">メソッド verticalSpacing</span><span class="sxs-lookup"><span data-stu-id="6cf6c-189">Method verticalSpacing</span></span>

```xpp
public boolean verticalSpacing([boolean value])
```

### <a name="parameters---verticalspacing"></a><span data-ttu-id="6cf6c-190">パラメーター - verticalSpacing</span><span class="sxs-lookup"><span data-stu-id="6cf6c-190">Parameters - verticalSpacing</span></span>

<span data-ttu-id="6cf6c-191">値</span><span class="sxs-lookup"><span data-stu-id="6cf6c-191">value</span></span>  

### <a name="return-value---verticalspacing"></a><span data-ttu-id="6cf6c-192">戻り値 - verticalSpacing</span><span class="sxs-lookup"><span data-stu-id="6cf6c-192">Return Value - verticalSpacing</span></span>

## <a name="method-new"></a><span data-ttu-id="6cf6c-193">メソッド new</span><span class="sxs-lookup"><span data-stu-id="6cf6c-193">Method new</span></span>

<span data-ttu-id="6cf6c-194">InfoPartGroup クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="6cf6c-194">Initializes a new instance of the InfoPartGroup class.</span></span>

```xpp
public void new()
```

