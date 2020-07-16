---
title: キュー クラス
description: このトピックでは、キュー クラスについて説明します。
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
ms.openlocfilehash: f5b9ff7c933b2c0394ab0cb5fb4e48f09e814566
ms.sourcegitcommit: 7b0cec2e898ef8ee33baf72f18cdd9cba0e9399c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/25/2020
ms.locfileid: "3502701"
---
# <a name="class-cue"></a><span data-ttu-id="c64cc-103">クラス キュー</span><span class="sxs-lookup"><span data-stu-id="c64cc-103">Class Cue</span></span>

[!include [banner](../../includes/banner.md)]

```xpp
class Cue extends TreeNode
```

## <a name="remarks"></a><span data-ttu-id="c64cc-104">備考</span><span class="sxs-lookup"><span data-stu-id="c64cc-104">Remarks</span></span>

## <a name="examples"></a><span data-ttu-id="c64cc-105">例</span><span class="sxs-lookup"><span data-stu-id="c64cc-105">Examples</span></span>

## <a name="methods"></a><span data-ttu-id="c64cc-106">メソッド</span><span class="sxs-lookup"><span data-stu-id="c64cc-106">Methods</span></span>

| <span data-ttu-id="c64cc-107">方法</span><span class="sxs-lookup"><span data-stu-id="c64cc-107">Method</span></span>                                         | <span data-ttu-id="c64cc-108">説明</span><span class="sxs-lookup"><span data-stu-id="c64cc-108">Description</span></span>                                                                                                                               |
|------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c64cc-109">public str changedBy(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="c64cc-109">public str changedBy(\[str value\])</span></span>            | <span data-ttu-id="c64cc-110">アプリケーション オブジェクトを最後に変更したユーザーの名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="c64cc-110">Gets or sets the name of the user who last changed the application object.</span></span>                                                                |
| <span data-ttu-id="c64cc-111">public Date changedDate(\[Date value\])</span><span class="sxs-lookup"><span data-stu-id="c64cc-111">public Date changedDate(\[Date value\])</span></span>        | <span data-ttu-id="c64cc-112">アプリケーション オブジェクトが最後に変更された日付を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="c64cc-112">Gets or sets the date an application object was last changed.</span></span>                                                                             |
| <span data-ttu-id="c64cc-113">public str changedTime(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="c64cc-113">public str changedTime(\[str value\])</span></span>          | <span data-ttu-id="c64cc-114">アプリケーション オブジェクトが最後に変更された時刻を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="c64cc-114">Gets or sets the time an application object was last changed.</span></span>                                                                             |
| <span data-ttu-id="c64cc-115">public str createdBy(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="c64cc-115">public str createdBy(\[str value\])</span></span>            | <span data-ttu-id="c64cc-116">アプリケーション オブジェクトを作成したユーザーの名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="c64cc-116">Gets or sets the name of the user who created the application object.</span></span>                                                                     |
| <span data-ttu-id="c64cc-117">public Date creationDate(\[Date value\])</span><span class="sxs-lookup"><span data-stu-id="c64cc-117">public Date creationDate(\[Date value\])</span></span>       | <span data-ttu-id="c64cc-118">アプリケーション オブジェクトが作成された日付を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="c64cc-118">Gets or sets the date an application object was created.</span></span>                                                                                  |
| <span data-ttu-id="c64cc-119">public str creationTime(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="c64cc-119">public str creationTime(\[str value\])</span></span>         |                                                                                                                                           |
| <span data-ttu-id="c64cc-120">public int cueMax(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="c64cc-120">public int cueMax(\[int value\])</span></span>               |                                                                                                                                           |
| <span data-ttu-id="c64cc-121">public str dataField(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="c64cc-121">public str dataField(\[str value\])</span></span>            |                                                                                                                                           |
| <span data-ttu-id="c64cc-122">public str label(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="c64cc-122">public str label(\[str value\])</span></span>                | <span data-ttu-id="c64cc-123">コントロールのラベルを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="c64cc-123">Gets or sets the label for a control.</span></span>                                                                                                     |
| <span data-ttu-id="c64cc-124">public str LabelId()</span><span class="sxs-lookup"><span data-stu-id="c64cc-124">public str LabelId()</span></span>                           |                                                                                                                                           |
| <span data-ttu-id="c64cc-125">public str menuItemName(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="c64cc-125">public str menuItemName(\[str value\])</span></span>         |                                                                                                                                           |
| <span data-ttu-id="c64cc-126">public str name(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="c64cc-126">public str name(\[str value\])</span></span>                 | <span data-ttu-id="c64cc-127">フォーム、レポート、テーブル、クエリ、または他のアプリケーション オブジェクトを識別するためのコードで使用される名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="c64cc-127">Gets or sets the name that is used in code to identify a form, report, table, query, or other application object.</span></span> |
| <span data-ttu-id="c64cc-128">public Guid origin(\[Guid value\])</span><span class="sxs-lookup"><span data-stu-id="c64cc-128">public Guid origin(\[Guid value\])</span></span>             |                                                                                                                                           |
| <span data-ttu-id="c64cc-129">public str previewPartReference(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="c64cc-129">public str previewPartReference(\[str value\])</span></span> |                                                                                                                                           |
| <span data-ttu-id="c64cc-130">public boolean showAlert(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="c64cc-130">public boolean showAlert(\[boolean value\])</span></span>    |                                                                                                                                           |
| <span data-ttu-id="c64cc-131">public int showAlertValue(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="c64cc-131">public int showAlertValue(\[int value\])</span></span>       |                                                                                                                                           |
| <span data-ttu-id="c64cc-132">public int showAlertWhen(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="c64cc-132">public int showAlertWhen(\[int value\])</span></span>        |                                                                                                                                           |
| <span data-ttu-id="c64cc-133">public boolean showSum(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="c64cc-133">public boolean showSum(\[boolean value\])</span></span>      |                                                                                                                                           |
| <span data-ttu-id="c64cc-134">public str table(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="c64cc-134">public str table(\[str value\])</span></span>                | <span data-ttu-id="c64cc-135">オブジェクトに関連付けられているテーブル ID を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="c64cc-135">Gets or sets the table ID associated with the object.</span></span>                                                                                     |
| <span data-ttu-id="c64cc-136">public void new(str cueName)</span><span class="sxs-lookup"><span data-stu-id="c64cc-136">public void new(str cueName)</span></span>                   | <span data-ttu-id="c64cc-137">TreeNode クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="c64cc-137">Initializes a new instance of the TreeNode class.</span></span>                                                                                         |

## <a name="method-changedby"></a><span data-ttu-id="c64cc-138">メソッド changedBy</span><span class="sxs-lookup"><span data-stu-id="c64cc-138">Method changedBy</span></span>

<span data-ttu-id="c64cc-139">アプリケーション オブジェクトを最後に変更したユーザーの名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="c64cc-139">Gets or sets the name of the user who last changed the application object.</span></span>

```xpp
public str changedBy([str value])
```

### <a name="parameters---changedby"></a><span data-ttu-id="c64cc-140">パラメーター - changedBy</span><span class="sxs-lookup"><span data-stu-id="c64cc-140">Parameters - changedBy</span></span>

<span data-ttu-id="c64cc-141">値</span><span class="sxs-lookup"><span data-stu-id="c64cc-141">value</span></span>  

### <a name="return-value---changedby"></a><span data-ttu-id="c64cc-142">戻り値 - changedBy</span><span class="sxs-lookup"><span data-stu-id="c64cc-142">Return Value - changedBy</span></span>

<span data-ttu-id="c64cc-143">ユーザーの名前。</span><span class="sxs-lookup"><span data-stu-id="c64cc-143">The name of the user.</span></span>

## <a name="method-changeddate"></a><span data-ttu-id="c64cc-144">メソッド changedDate</span><span class="sxs-lookup"><span data-stu-id="c64cc-144">Method changedDate</span></span>

<span data-ttu-id="c64cc-145">アプリケーション オブジェクトが最後に変更された日付を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="c64cc-145">Gets or sets the date an application object was last changed.</span></span>

```xpp
public Date changedDate([Date value])
```

### <a name="parameters---changeddate"></a><span data-ttu-id="c64cc-146">パラメーター - changedDate</span><span class="sxs-lookup"><span data-stu-id="c64cc-146">Parameters - changedDate</span></span>

<span data-ttu-id="c64cc-147">値</span><span class="sxs-lookup"><span data-stu-id="c64cc-147">value</span></span>  

### <a name="return-value---changeddate"></a><span data-ttu-id="c64cc-148">戻り値 - changedDate</span><span class="sxs-lookup"><span data-stu-id="c64cc-148">Return Value - changedDate</span></span>

<span data-ttu-id="c64cc-149">アプリケーション オブジェクトが最後に変更された日付。</span><span class="sxs-lookup"><span data-stu-id="c64cc-149">The date an application object was last changed.</span></span>

## <a name="method-changedtime"></a><span data-ttu-id="c64cc-150">メソッド changedTime</span><span class="sxs-lookup"><span data-stu-id="c64cc-150">Method changedTime</span></span>

<span data-ttu-id="c64cc-151">アプリケーション オブジェクトが最後に変更された時刻を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="c64cc-151">Gets or sets the time an application object was last changed.</span></span>

```xpp
public str changedTime([str value])
```

### <a name="parameters---changedtime"></a><span data-ttu-id="c64cc-152">パラメーター - changedTime</span><span class="sxs-lookup"><span data-stu-id="c64cc-152">Parameters - changedTime</span></span>

<span data-ttu-id="c64cc-153">値</span><span class="sxs-lookup"><span data-stu-id="c64cc-153">value</span></span>  

### <a name="return-value---changedtime"></a><span data-ttu-id="c64cc-154">戻り値 - changedTime</span><span class="sxs-lookup"><span data-stu-id="c64cc-154">Return Value - changedTime</span></span>

<span data-ttu-id="c64cc-155">アプリケーション オブジェクトが最後に変更された時間。</span><span class="sxs-lookup"><span data-stu-id="c64cc-155">The time an application object was last changed.</span></span>

## <a name="method-createdby"></a><span data-ttu-id="c64cc-156">メソッド createdBy</span><span class="sxs-lookup"><span data-stu-id="c64cc-156">Method createdBy</span></span>

<span data-ttu-id="c64cc-157">アプリケーション オブジェクトを作成したユーザーの名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="c64cc-157">Gets or sets the name of the user who created the application object.</span></span>

```xpp
public str createdBy([str value])
```

### <a name="parameters---createdby"></a><span data-ttu-id="c64cc-158">パラメーター - createdBy</span><span class="sxs-lookup"><span data-stu-id="c64cc-158">Parameters - createdBy</span></span>

<span data-ttu-id="c64cc-159">値</span><span class="sxs-lookup"><span data-stu-id="c64cc-159">value</span></span>  

### <a name="return-value---createdby"></a><span data-ttu-id="c64cc-160">戻り値 - createdBy</span><span class="sxs-lookup"><span data-stu-id="c64cc-160">Return Value - createdBy</span></span>

<span data-ttu-id="c64cc-161">ユーザーの名前。</span><span class="sxs-lookup"><span data-stu-id="c64cc-161">The name of the user.</span></span>

## <a name="method-creationdate"></a><span data-ttu-id="c64cc-162">メソッド creationDate</span><span class="sxs-lookup"><span data-stu-id="c64cc-162">Method creationDate</span></span>

<span data-ttu-id="c64cc-163">アプリケーション オブジェクトが作成された日付を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="c64cc-163">Gets or sets the date an application object was created.</span></span>

```xpp
public Date creationDate([Date value])
```

### <a name="parameters---creationdate"></a><span data-ttu-id="c64cc-164">パラメーター - creationDate</span><span class="sxs-lookup"><span data-stu-id="c64cc-164">Parameters - creationDate</span></span>

<span data-ttu-id="c64cc-165">値</span><span class="sxs-lookup"><span data-stu-id="c64cc-165">value</span></span>  

### <a name="return-value---creationdate"></a><span data-ttu-id="c64cc-166">戻り値 - creationDate</span><span class="sxs-lookup"><span data-stu-id="c64cc-166">Return Value - creationDate</span></span>

<span data-ttu-id="c64cc-167">アプリケーション オブジェクトが作成された日付。</span><span class="sxs-lookup"><span data-stu-id="c64cc-167">The date an application object was created.</span></span>

## <a name="method-creationtime"></a><span data-ttu-id="c64cc-168">メソッド creationTime</span><span class="sxs-lookup"><span data-stu-id="c64cc-168">Method creationTime</span></span>

```xpp
public str creationTime([str value])
```

### <a name="parameters---creationtime"></a><span data-ttu-id="c64cc-169">パラメーター - creationTime</span><span class="sxs-lookup"><span data-stu-id="c64cc-169">Parameters - creationTime</span></span>

<span data-ttu-id="c64cc-170">値</span><span class="sxs-lookup"><span data-stu-id="c64cc-170">value</span></span>  

### <a name="return-value---creationtime"></a><span data-ttu-id="c64cc-171">戻り値 - creationTime</span><span class="sxs-lookup"><span data-stu-id="c64cc-171">Return Value - creationTime</span></span>

## <a name="method-cuemax"></a><span data-ttu-id="c64cc-172">メソッド cueMax</span><span class="sxs-lookup"><span data-stu-id="c64cc-172">Method cueMax</span></span>

```xpp
public int cueMax([int value])
```

### <a name="parameters---cuemax"></a><span data-ttu-id="c64cc-173">パラメーター - cueMax</span><span class="sxs-lookup"><span data-stu-id="c64cc-173">Parameters - cueMax</span></span>

<span data-ttu-id="c64cc-174">値</span><span class="sxs-lookup"><span data-stu-id="c64cc-174">value</span></span>  

### <a name="return-value---cuemax"></a><span data-ttu-id="c64cc-175">戻り値 - cueMax</span><span class="sxs-lookup"><span data-stu-id="c64cc-175">Return Value - cueMax</span></span>

## <a name="method-datafield"></a><span data-ttu-id="c64cc-176">メソッド dataField</span><span class="sxs-lookup"><span data-stu-id="c64cc-176">Method dataField</span></span>

```xpp
public str dataField([str value])
```

### <a name="parameters---datafield"></a><span data-ttu-id="c64cc-177">パラメーター - dataField</span><span class="sxs-lookup"><span data-stu-id="c64cc-177">Parameters - dataField</span></span>

<span data-ttu-id="c64cc-178">値</span><span class="sxs-lookup"><span data-stu-id="c64cc-178">value</span></span>  

### <a name="return-value---datafield"></a><span data-ttu-id="c64cc-179">戻り値 - dataField</span><span class="sxs-lookup"><span data-stu-id="c64cc-179">Return Value - dataField</span></span>

## <a name="method-label"></a><span data-ttu-id="c64cc-180">メソッド label</span><span class="sxs-lookup"><span data-stu-id="c64cc-180">Method label</span></span>

<span data-ttu-id="c64cc-181">コントロールのラベルを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="c64cc-181">Gets or sets the label for a control.</span></span>

```xpp
public str label([str value])
```

### <a name="parameters---label"></a><span data-ttu-id="c64cc-182">パラメーター - label</span><span class="sxs-lookup"><span data-stu-id="c64cc-182">Parameters - label</span></span>

<span data-ttu-id="c64cc-183">値</span><span class="sxs-lookup"><span data-stu-id="c64cc-183">value</span></span>  

### <a name="return-value---label"></a><span data-ttu-id="c64cc-184">戻り値 - label</span><span class="sxs-lookup"><span data-stu-id="c64cc-184">Return Value - label</span></span>

<span data-ttu-id="c64cc-185">ラベル文字列の現在の値。</span><span class="sxs-lookup"><span data-stu-id="c64cc-185">The current value of the label string.</span></span>

### <a name="remarks---label"></a><span data-ttu-id="c64cc-186">備考 - label</span><span class="sxs-lookup"><span data-stu-id="c64cc-186">Remarks - label</span></span>

<span data-ttu-id="c64cc-187">ラベルは、コントロール内に表示されているテキストまたはそれに隣接するテキストを指定します。</span><span class="sxs-lookup"><span data-stu-id="c64cc-187">The label determines which text is displayed in the control or adjacent to it.</span></span> <span data-ttu-id="c64cc-188">ラベルのプロパティ値は 250 文字を超えることはできません。</span><span class="sxs-lookup"><span data-stu-id="c64cc-188">The label property value cannot exceed 250 characters.</span></span>

## <a name="method-labelid"></a><span data-ttu-id="c64cc-189">メソッド LabelId</span><span class="sxs-lookup"><span data-stu-id="c64cc-189">Method LabelId</span></span>

```xpp
public str LabelId()
```

### <a name="return-value---labelid"></a><span data-ttu-id="c64cc-190">戻り値 - LabelId</span><span class="sxs-lookup"><span data-stu-id="c64cc-190">Return Value - LabelId</span></span>

## <a name="method-menuitemname"></a><span data-ttu-id="c64cc-191">メソッド menuItemName</span><span class="sxs-lookup"><span data-stu-id="c64cc-191">Method menuItemName</span></span>

```xpp
public str menuItemName([str value])
```

### <a name="parameters---menuitemname"></a><span data-ttu-id="c64cc-192">パラメーター - menuItemName</span><span class="sxs-lookup"><span data-stu-id="c64cc-192">Parameters - menuItemName</span></span>

<span data-ttu-id="c64cc-193">値</span><span class="sxs-lookup"><span data-stu-id="c64cc-193">value</span></span>  

### <a name="return-value---menuitemname"></a><span data-ttu-id="c64cc-194">戻り値 - menuItemName</span><span class="sxs-lookup"><span data-stu-id="c64cc-194">Return Value - menuItemName</span></span>

## <a name="method-name"></a><span data-ttu-id="c64cc-195">メソッド名</span><span class="sxs-lookup"><span data-stu-id="c64cc-195">Method name</span></span>

<span data-ttu-id="c64cc-196">フォーム、レポート、テーブル、クエリ、または他のアプリケーション オブジェクトを識別するためのコードで使用される名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="c64cc-196">Gets or sets the name that is used in code to identify a form, report, table, query, or other application object.</span></span>

```xpp
public str name([str value])
```

### <a name="parameters---name"></a><span data-ttu-id="c64cc-197">パラメーター - 名前</span><span class="sxs-lookup"><span data-stu-id="c64cc-197">Parameters - name</span></span>

<span data-ttu-id="c64cc-198">値</span><span class="sxs-lookup"><span data-stu-id="c64cc-198">value</span></span>  

### <a name="return-value---name"></a><span data-ttu-id="c64cc-199">戻り値 - name</span><span class="sxs-lookup"><span data-stu-id="c64cc-199">Return Value - name</span></span>

<span data-ttu-id="c64cc-200">アプリケーション オブジェクトを識別するためにコードで使用される名前。</span><span class="sxs-lookup"><span data-stu-id="c64cc-200">The name that is used in code to identify an application object.</span></span>

### <a name="remarks---name"></a><span data-ttu-id="c64cc-201">備考 - 名前</span><span class="sxs-lookup"><span data-stu-id="c64cc-201">Remarks - name</span></span>

<span data-ttu-id="c64cc-202">オブジェクトの名前プロパティ値は、コードの競合を避けるために、次の基準を満たしている必要があります。</span><span class="sxs-lookup"><span data-stu-id="c64cc-202">The name property value of an object must meet the following criteria to avoid code conflicts:</span></span>

-   <span data-ttu-id="c64cc-203">文字で始めます。</span><span class="sxs-lookup"><span data-stu-id="c64cc-203">Begins with a letter.</span></span>
-   <span data-ttu-id="c64cc-204">250 文字を超えないでください。</span><span class="sxs-lookup"><span data-stu-id="c64cc-204">Doesn't exceed 250 characters.</span></span>
-   <span data-ttu-id="c64cc-205">数字とアンダースコア文字を含めることができます。</span><span class="sxs-lookup"><span data-stu-id="c64cc-205">Can include numbers and underscore characters.</span></span>
-   <span data-ttu-id="c64cc-206">句読点やスペースを含めることはできません。</span><span class="sxs-lookup"><span data-stu-id="c64cc-206">Cannot include punctuation or spaces.</span></span>
-   <span data-ttu-id="c64cc-207">テーブルは、拡張データ型、基本列挙型、およびクラスなどの他のパブリック オブジェクトと同じ名前を持つことはできません。</span><span class="sxs-lookup"><span data-stu-id="c64cc-207">Tables cannot have the same name as other public objects, such as extended data types, base enumeration types, and classes.</span></span>

## <a name="method-origin"></a><span data-ttu-id="c64cc-208">メソッド origin</span><span class="sxs-lookup"><span data-stu-id="c64cc-208">Method origin</span></span>

```xpp
public Guid origin([Guid value])
```

### <a name="parameters---origin"></a><span data-ttu-id="c64cc-209">パラメーター - origin</span><span class="sxs-lookup"><span data-stu-id="c64cc-209">Parameters - origin</span></span>

<span data-ttu-id="c64cc-210">値</span><span class="sxs-lookup"><span data-stu-id="c64cc-210">value</span></span>  

### <a name="return-value---origin"></a><span data-ttu-id="c64cc-211">戻り値 - origin</span><span class="sxs-lookup"><span data-stu-id="c64cc-211">Return Value - origin</span></span>

## <a name="method-previewpartreference"></a><span data-ttu-id="c64cc-212">メソッド previewPartReference</span><span class="sxs-lookup"><span data-stu-id="c64cc-212">Method previewPartReference</span></span>

```xpp
public str previewPartReference([str value])
```

### <a name="parameters---previewpartreference"></a><span data-ttu-id="c64cc-213">パラメーター - previewPartReference</span><span class="sxs-lookup"><span data-stu-id="c64cc-213">Parameters - previewPartReference</span></span>

<span data-ttu-id="c64cc-214">値</span><span class="sxs-lookup"><span data-stu-id="c64cc-214">value</span></span>  

### <a name="return-value---previewpartreference"></a><span data-ttu-id="c64cc-215">戻り値 - previewPartReference</span><span class="sxs-lookup"><span data-stu-id="c64cc-215">Return Value - previewPartReference</span></span>

## <a name="method-showalert"></a><span data-ttu-id="c64cc-216">メソッド showAlert</span><span class="sxs-lookup"><span data-stu-id="c64cc-216">Method showAlert</span></span>

```xpp
public boolean showAlert([boolean value])
```

### <a name="parameters---showalert"></a><span data-ttu-id="c64cc-217">パラメーター - showAlert</span><span class="sxs-lookup"><span data-stu-id="c64cc-217">Parameters - showAlert</span></span>

<span data-ttu-id="c64cc-218">値</span><span class="sxs-lookup"><span data-stu-id="c64cc-218">value</span></span>  

### <a name="return-value---showalert"></a><span data-ttu-id="c64cc-219">戻り値 - showAlert</span><span class="sxs-lookup"><span data-stu-id="c64cc-219">Return Value - showAlert</span></span>

## <a name="method-showalertvalue"></a><span data-ttu-id="c64cc-220">メソッド showAlertValue</span><span class="sxs-lookup"><span data-stu-id="c64cc-220">Method showAlertValue</span></span>

```xpp
public int showAlertValue([int value])
```

### <a name="parameters---showalertvalue"></a><span data-ttu-id="c64cc-221">パラメーター - showAlertValue</span><span class="sxs-lookup"><span data-stu-id="c64cc-221">Parameters - showAlertValue</span></span>

<span data-ttu-id="c64cc-222">値</span><span class="sxs-lookup"><span data-stu-id="c64cc-222">value</span></span>  

### <a name="return-value---showalertvalue"></a><span data-ttu-id="c64cc-223">戻り値 - showAlertValue</span><span class="sxs-lookup"><span data-stu-id="c64cc-223">Return Value - showAlertValue</span></span>

## <a name="method-showalertwhen"></a><span data-ttu-id="c64cc-224">メソッド showAlertWhen</span><span class="sxs-lookup"><span data-stu-id="c64cc-224">Method showAlertWhen</span></span>

```xpp
public int showAlertWhen([int value])
```

### <a name="parameters---showalertwhen"></a><span data-ttu-id="c64cc-225">パラメーター - showAlertWhen</span><span class="sxs-lookup"><span data-stu-id="c64cc-225">Parameters - showAlertWhen</span></span>

<span data-ttu-id="c64cc-226">値</span><span class="sxs-lookup"><span data-stu-id="c64cc-226">value</span></span>  

### <a name="return-value---showalertwhen"></a><span data-ttu-id="c64cc-227">戻り値 - showAlertWhen</span><span class="sxs-lookup"><span data-stu-id="c64cc-227">Return Value - showAlertWhen</span></span>

## <a name="method-showsum"></a><span data-ttu-id="c64cc-228">メソッド showSum</span><span class="sxs-lookup"><span data-stu-id="c64cc-228">Method showSum</span></span>

```xpp
public boolean showSum([boolean value])
```

### <a name="parameters---showsum"></a><span data-ttu-id="c64cc-229">パラメーター - showSum</span><span class="sxs-lookup"><span data-stu-id="c64cc-229">Parameters - showSum</span></span>

<span data-ttu-id="c64cc-230">値</span><span class="sxs-lookup"><span data-stu-id="c64cc-230">value</span></span>  

### <a name="return-value---showsum"></a><span data-ttu-id="c64cc-231">戻り値 - showSum</span><span class="sxs-lookup"><span data-stu-id="c64cc-231">Return Value - showSum</span></span>

## <a name="method-table"></a><span data-ttu-id="c64cc-232">メソッド table</span><span class="sxs-lookup"><span data-stu-id="c64cc-232">Method table</span></span>

<span data-ttu-id="c64cc-233">オブジェクトに関連付けられているテーブル ID を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="c64cc-233">Gets or sets the table ID associated with the object.</span></span>

```xpp
public str table([str value])
```

### <a name="parameters---table"></a><span data-ttu-id="c64cc-234">パラメーター - table</span><span class="sxs-lookup"><span data-stu-id="c64cc-234">Parameters - table</span></span>

<span data-ttu-id="c64cc-235">値</span><span class="sxs-lookup"><span data-stu-id="c64cc-235">value</span></span>  

### <a name="return-value---table"></a><span data-ttu-id="c64cc-236">戻り値 - toBlob</span><span class="sxs-lookup"><span data-stu-id="c64cc-236">Return Value - table</span></span>

<span data-ttu-id="c64cc-237">オブジェクトに関連付けられたテーブル ID の現在の値。</span><span class="sxs-lookup"><span data-stu-id="c64cc-237">The current value of the table ID associated with the object.</span></span>

## <a name="method-new"></a><span data-ttu-id="c64cc-238">メソッド new</span><span class="sxs-lookup"><span data-stu-id="c64cc-238">Method new</span></span>

<span data-ttu-id="c64cc-239">TreeNode クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="c64cc-239">Initializes a new instance of the TreeNode class.</span></span>

```xpp
public void new(str cueName)
```

### <a name="parameters---new"></a><span data-ttu-id="c64cc-240">パラメーター - new</span><span class="sxs-lookup"><span data-stu-id="c64cc-240">Parameters - new</span></span>

<span data-ttu-id="c64cc-241">cueName</span><span class="sxs-lookup"><span data-stu-id="c64cc-241">cueName</span></span>  

