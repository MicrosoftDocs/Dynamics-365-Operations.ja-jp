---
title: InfoPartField クラス
description: このトピックでは、InfoPartField クラスについて説明します。
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
ms.openlocfilehash: 1dfa6717154f7d2a49a679617cd1f1bff83e3e70
ms.sourcegitcommit: 7b0cec2e898ef8ee33baf72f18cdd9cba0e9399c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/25/2020
ms.locfileid: "3502595"
---
# <a name="class-infopartfield"></a><span data-ttu-id="31f17-103">クラス InfoPartField</span><span class="sxs-lookup"><span data-stu-id="31f17-103">Class InfoPartField</span></span>

[!include [banner](../../includes/banner.md)]

```xpp
class InfoPartField extends TreeNode
```

## <a name="remarks"></a><span data-ttu-id="31f17-104">備考</span><span class="sxs-lookup"><span data-stu-id="31f17-104">Remarks</span></span>

## <a name="examples"></a><span data-ttu-id="31f17-105">例</span><span class="sxs-lookup"><span data-stu-id="31f17-105">Examples</span></span>

## <a name="methods"></a><span data-ttu-id="31f17-106">メソッド</span><span class="sxs-lookup"><span data-stu-id="31f17-106">Methods</span></span>

| <span data-ttu-id="31f17-107">方法</span><span class="sxs-lookup"><span data-stu-id="31f17-107">Method</span></span>                                            | <span data-ttu-id="31f17-108">説明</span><span class="sxs-lookup"><span data-stu-id="31f17-108">Description</span></span>                                                                                                                               |
|---------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="31f17-109">public str dataField(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="31f17-109">public str dataField(\[str value\])</span></span>               |                                                                                                                                           |
| <span data-ttu-id="31f17-110">public str dataMethod(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="31f17-110">public str dataMethod(\[str value\])</span></span>              |                                                                                                                                           |
| <span data-ttu-id="31f17-111">public str dataSource(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="31f17-111">public str dataSource(\[str value\])</span></span>              | <span data-ttu-id="31f17-112">コントロールまたはフォームで使用されるデータ ソースを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="31f17-112">Gets or sets a data source that will be used by the control or the form.</span></span>                                                                  |
| <span data-ttu-id="31f17-113">public str label(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="31f17-113">public str label(\[str value\])</span></span>                   | <span data-ttu-id="31f17-114">コントロールのラベルを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="31f17-114">Gets or sets the label for a control.</span></span>                                                                                                     |
| <span data-ttu-id="31f17-115">public boolean manualRetrieval(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="31f17-115">public boolean manualRetrieval(\[boolean value\])</span></span> |                                                                                                                                           |
| <span data-ttu-id="31f17-116">public str name(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="31f17-116">public str name(\[str value\])</span></span>                    | <span data-ttu-id="31f17-117">フォーム、レポート、テーブル、クエリ、または他のアプリケーション オブジェクトを識別するためのコードで使用される名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="31f17-117">Gets or sets the name that is used in code to identify a form, report, table, query, or other application object.</span></span> |
| <span data-ttu-id="31f17-118">public int style(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="31f17-118">public int style(\[int value\])</span></span>                   |                                                                                                                                           |
| <span data-ttu-id="31f17-119">public void new()</span><span class="sxs-lookup"><span data-stu-id="31f17-119">public void new()</span></span>                                 | <span data-ttu-id="31f17-120">InfoPartField クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="31f17-120">Initializes a new instance of the InfoPartField class.</span></span>                                                                                    |

## <a name="method-datafield"></a><span data-ttu-id="31f17-121">メソッド dataField</span><span class="sxs-lookup"><span data-stu-id="31f17-121">Method dataField</span></span>

```xpp
public str dataField([str value])
```

### <a name="parameters---datafield"></a><span data-ttu-id="31f17-122">パラメーター - dataField</span><span class="sxs-lookup"><span data-stu-id="31f17-122">Parameters - dataField</span></span>

<span data-ttu-id="31f17-123">値</span><span class="sxs-lookup"><span data-stu-id="31f17-123">value</span></span>  

### <a name="return-value---datafield"></a><span data-ttu-id="31f17-124">戻り値 - dataField</span><span class="sxs-lookup"><span data-stu-id="31f17-124">Return Value - dataField</span></span>

## <a name="method-datamethod"></a><span data-ttu-id="31f17-125">メソッド dataMethod</span><span class="sxs-lookup"><span data-stu-id="31f17-125">Method dataMethod</span></span>

```xpp
public str dataMethod([str value])
```

### <a name="parameters---datamethod"></a><span data-ttu-id="31f17-126">パラメーター - dataMethod</span><span class="sxs-lookup"><span data-stu-id="31f17-126">Parameters - dataMethod</span></span>

<span data-ttu-id="31f17-127">値</span><span class="sxs-lookup"><span data-stu-id="31f17-127">value</span></span>  

### <a name="return-value---datamethod"></a><span data-ttu-id="31f17-128">戻り値 - dataMethod</span><span class="sxs-lookup"><span data-stu-id="31f17-128">Return Value - dataMethod</span></span>

## <a name="method-datasource"></a><span data-ttu-id="31f17-129">メソッド dataSource</span><span class="sxs-lookup"><span data-stu-id="31f17-129">Method dataSource</span></span>

<span data-ttu-id="31f17-130">コントロールまたはフォームで使用されるデータ ソースを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="31f17-130">Gets or sets a data source that will be used by the control or the form.</span></span>

```xpp
public str dataSource([str value])
```

### <a name="parameters---datasource"></a><span data-ttu-id="31f17-131">パラメーター - dataSource</span><span class="sxs-lookup"><span data-stu-id="31f17-131">Parameters - dataSource</span></span>

<span data-ttu-id="31f17-132">値</span><span class="sxs-lookup"><span data-stu-id="31f17-132">value</span></span>  

### <a name="return-value---datasource"></a><span data-ttu-id="31f17-133">戻り値 - dataSource</span><span class="sxs-lookup"><span data-stu-id="31f17-133">Return Value - dataSource</span></span>

<span data-ttu-id="31f17-134">使用されるデータ ソースの ID。</span><span class="sxs-lookup"><span data-stu-id="31f17-134">The identifier of the data source that will be used.</span></span>

## <a name="method-label"></a><span data-ttu-id="31f17-135">メソッド label</span><span class="sxs-lookup"><span data-stu-id="31f17-135">Method label</span></span>

<span data-ttu-id="31f17-136">コントロールのラベルを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="31f17-136">Gets or sets the label for a control.</span></span>

```xpp
public str label([str value])
```

### <a name="parameters---label"></a><span data-ttu-id="31f17-137">パラメーター - label</span><span class="sxs-lookup"><span data-stu-id="31f17-137">Parameters - label</span></span>

<span data-ttu-id="31f17-138">値</span><span class="sxs-lookup"><span data-stu-id="31f17-138">value</span></span>  

### <a name="return-value---label"></a><span data-ttu-id="31f17-139">戻り値 - label</span><span class="sxs-lookup"><span data-stu-id="31f17-139">Return Value - label</span></span>

<span data-ttu-id="31f17-140">ラベル文字列の現在の値。</span><span class="sxs-lookup"><span data-stu-id="31f17-140">The current value of the label string.</span></span>

### <a name="remarks---label"></a><span data-ttu-id="31f17-141">備考 - label</span><span class="sxs-lookup"><span data-stu-id="31f17-141">Remarks - label</span></span>

<span data-ttu-id="31f17-142">ラベルは、コントロール内に表示されているテキストまたはそれに隣接するテキストを指定します。</span><span class="sxs-lookup"><span data-stu-id="31f17-142">The label determines which text is displayed in the control or adjacent to it.</span></span> <span data-ttu-id="31f17-143">ラベルのプロパティ値は 250 文字を超えることはできません。</span><span class="sxs-lookup"><span data-stu-id="31f17-143">The label property value cannot exceed 250 characters.</span></span>

## <a name="method-manualretrieval"></a><span data-ttu-id="31f17-144">メソッド manualRetrieval</span><span class="sxs-lookup"><span data-stu-id="31f17-144">Method manualRetrieval</span></span>

```xpp
public boolean manualRetrieval([boolean value])
```

### <a name="parameters---manualretrieval"></a><span data-ttu-id="31f17-145">パラメーター - manualRetrieval</span><span class="sxs-lookup"><span data-stu-id="31f17-145">Parameters - manualRetrieval</span></span>

<span data-ttu-id="31f17-146">値</span><span class="sxs-lookup"><span data-stu-id="31f17-146">value</span></span>  

### <a name="return-value---manualretrieval"></a><span data-ttu-id="31f17-147">戻り値 - manualRetrieval</span><span class="sxs-lookup"><span data-stu-id="31f17-147">Return Value - manualRetrieval</span></span>

## <a name="method-name"></a><span data-ttu-id="31f17-148">メソッド名</span><span class="sxs-lookup"><span data-stu-id="31f17-148">Method name</span></span>

<span data-ttu-id="31f17-149">フォーム、レポート、テーブル、クエリ、または他のアプリケーション オブジェクトを識別するためのコードで使用される名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="31f17-149">Gets or sets the name that is used in code to identify a form, report, table, query, or other application object.</span></span>

```xpp
public str name([str value])
```

### <a name="parameters---name"></a><span data-ttu-id="31f17-150">パラメーター - name</span><span class="sxs-lookup"><span data-stu-id="31f17-150">Parameters - name</span></span>

<span data-ttu-id="31f17-151">値</span><span class="sxs-lookup"><span data-stu-id="31f17-151">value</span></span>  

### <a name="return-value---name"></a><span data-ttu-id="31f17-152">戻り値 - name</span><span class="sxs-lookup"><span data-stu-id="31f17-152">Return Value - name</span></span>

<span data-ttu-id="31f17-153">アプリケーション オブジェクトを識別するためにコードで使用される名前。</span><span class="sxs-lookup"><span data-stu-id="31f17-153">The name that is used in code to identify an application object.</span></span>

### <a name="remarks---name"></a><span data-ttu-id="31f17-154">備考 - name</span><span class="sxs-lookup"><span data-stu-id="31f17-154">Remarks - name</span></span>

<span data-ttu-id="31f17-155">オブジェクトの名前プロパティ値は、コードの競合を避けるために、次の基準を満たしている必要があります。</span><span class="sxs-lookup"><span data-stu-id="31f17-155">The name property value of an object must meet the following criteria to avoid code conflicts:</span></span>

-   <span data-ttu-id="31f17-156">文字で始めます。</span><span class="sxs-lookup"><span data-stu-id="31f17-156">Begins with a letter.</span></span>
-   <span data-ttu-id="31f17-157">250 文字を超えないでください。</span><span class="sxs-lookup"><span data-stu-id="31f17-157">Doesn't exceed 250 characters.</span></span>
-   <span data-ttu-id="31f17-158">数字とアンダースコア文字を含めることができます。</span><span class="sxs-lookup"><span data-stu-id="31f17-158">Can include numbers and underscore characters.</span></span>
-   <span data-ttu-id="31f17-159">句読点やスペースを含めることはできません。</span><span class="sxs-lookup"><span data-stu-id="31f17-159">Cannot include punctuation or spaces.</span></span>
-   <span data-ttu-id="31f17-160">テーブルは、拡張データ型、基本列挙型、クラスなどの他のパブリック オブジェクトと同じ名前を持つことはできません。</span><span class="sxs-lookup"><span data-stu-id="31f17-160">Tables cannot have the same name as other public objects, such as extended data types, base enums, classes, and so on.</span></span>

## <a name="method-style"></a><span data-ttu-id="31f17-161">メソッド style</span><span class="sxs-lookup"><span data-stu-id="31f17-161">Method style</span></span>

```xpp
public int style([int value])
```

### <a name="parameters---style"></a><span data-ttu-id="31f17-162">パラメーター - style</span><span class="sxs-lookup"><span data-stu-id="31f17-162">Parameters - style</span></span>

<span data-ttu-id="31f17-163">値</span><span class="sxs-lookup"><span data-stu-id="31f17-163">value</span></span>  

### <a name="return-value---style"></a><span data-ttu-id="31f17-164">戻り値 - style</span><span class="sxs-lookup"><span data-stu-id="31f17-164">Return Value - style</span></span>

## <a name="method-new"></a><span data-ttu-id="31f17-165">メソッド new</span><span class="sxs-lookup"><span data-stu-id="31f17-165">Method new</span></span>

<span data-ttu-id="31f17-166">InfoPartField クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="31f17-166">Initializes a new instance of the InfoPartField class.</span></span>

```xpp
public void new()
```

