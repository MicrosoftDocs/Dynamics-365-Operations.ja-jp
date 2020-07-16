---
title: ListPage クラス
description: このトピックでは、ListPage クラスについて説明します。
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
ms.openlocfilehash: 80b57cf4369574cde992b2c98305f3bd398830ae
ms.sourcegitcommit: 7b0cec2e898ef8ee33baf72f18cdd9cba0e9399c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/25/2020
ms.locfileid: "3502585"
---
# <a name="class-listpage"></a><span data-ttu-id="9a747-103">クラス ListPage</span><span class="sxs-lookup"><span data-stu-id="9a747-103">Class ListPage</span></span>

[!include [banner](../../includes/banner.md)]

```xpp
class ListPage extends Page
```

## <a name="remarks"></a><span data-ttu-id="9a747-104">備考</span><span class="sxs-lookup"><span data-stu-id="9a747-104">Remarks</span></span>

## <a name="examples"></a><span data-ttu-id="9a747-105">例</span><span class="sxs-lookup"><span data-stu-id="9a747-105">Examples</span></span>

## <a name="methods"></a><span data-ttu-id="9a747-106">メソッド</span><span class="sxs-lookup"><span data-stu-id="9a747-106">Methods</span></span>

| <span data-ttu-id="9a747-107">方法</span><span class="sxs-lookup"><span data-stu-id="9a747-107">Method</span></span>                                                                      | <span data-ttu-id="9a747-108">説明</span><span class="sxs-lookup"><span data-stu-id="9a747-108">Description</span></span>                                       |
|-----------------------------------------------------------------------------|---------------------------------------------------|
| <span data-ttu-id="9a747-109">public str actionPaneControlParameters(str controlName, \[str parameters\])</span><span class="sxs-lookup"><span data-stu-id="9a747-109">public str actionPaneControlParameters(str controlName, \[str parameters\])</span></span> |                                                   |
| <span data-ttu-id="9a747-110">public Array activeActionPaneTabNames()</span><span class="sxs-lookup"><span data-stu-id="9a747-110">public Array activeActionPaneTabNames()</span></span>                                     | <span data-ttu-id="9a747-111">指定された有効なタブの名前を取得します。</span><span class="sxs-lookup"><span data-stu-id="9a747-111">Gets the name of the specified active tab.</span></span>        |
| <span data-ttu-id="9a747-112">public str caption(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="9a747-112">public str caption(\[str value\])</span></span>                                           |                                                   |
| <span data-ttu-id="9a747-113">public ListPageArgs listPageArgs()</span><span class="sxs-lookup"><span data-stu-id="9a747-113">public ListPageArgs listPageArgs()</span></span>                                          |                                                   |
| <span data-ttu-id="9a747-114">public int listPageFieldDataField(str fieldName)</span><span class="sxs-lookup"><span data-stu-id="9a747-114">public int listPageFieldDataField(str fieldName)</span></span>                            |                                                   |
| <span data-ttu-id="9a747-115">public Array listPageFieldNames()</span><span class="sxs-lookup"><span data-stu-id="9a747-115">public Array listPageFieldNames()</span></span>                                           |                                                   |
| <span data-ttu-id="9a747-116">public int listPageFieldTableId(str fieldName)</span><span class="sxs-lookup"><span data-stu-id="9a747-116">public int listPageFieldTableId(str fieldName)</span></span>                              |                                                   |
| <span data-ttu-id="9a747-117">public boolean listPageFieldVisible(str fieldName, \[boolean visible\])</span><span class="sxs-lookup"><span data-stu-id="9a747-117">public boolean listPageFieldVisible(str fieldName, \[boolean visible\])</span></span>     |                                                   |
| <span data-ttu-id="9a747-118">public str modeledQueryName(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="9a747-118">public str modeledQueryName(\[str value\])</span></span>                                  |                                                   |
| <span data-ttu-id="9a747-119">public void new()</span><span class="sxs-lookup"><span data-stu-id="9a747-119">public void new()</span></span>                                                           | <span data-ttu-id="9a747-120">ListPage クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="9a747-120">Initializes a new instance of the ListPage class.</span></span> |

## <a name="method-actionpanecontrolparameters"></a><span data-ttu-id="9a747-121">メソッド actionPaneControlParameters</span><span class="sxs-lookup"><span data-stu-id="9a747-121">Method actionPaneControlParameters</span></span>

```xpp
public str actionPaneControlParameters(str controlName, [str parameters])
```

### <a name="parameters---actionpanecontrolparameters"></a><span data-ttu-id="9a747-122">パラメーター - actionPaneControlParameters</span><span class="sxs-lookup"><span data-stu-id="9a747-122">Parameters - actionPaneControlParameters</span></span>

<span data-ttu-id="9a747-123">controlName</span><span class="sxs-lookup"><span data-stu-id="9a747-123">controlName</span></span>  

<!-- -->

<span data-ttu-id="9a747-124">パラメータ</span><span class="sxs-lookup"><span data-stu-id="9a747-124">parameters</span></span>  

### <a name="return-value---actionpanecontrolparameters"></a><span data-ttu-id="9a747-125">戻り値 - actionPaneControlParameters</span><span class="sxs-lookup"><span data-stu-id="9a747-125">Return Value - actionPaneControlParameters</span></span>

## <a name="method-activeactionpanetabnames"></a><span data-ttu-id="9a747-126">メソッド activeActionPaneTabNames</span><span class="sxs-lookup"><span data-stu-id="9a747-126">Method activeActionPaneTabNames</span></span>

<span data-ttu-id="9a747-127">指定された有効なタブの名前を取得します。</span><span class="sxs-lookup"><span data-stu-id="9a747-127">Gets the name of the specified active tab.</span></span>

```xpp
public Array activeActionPaneTabNames()
```

### <a name="return-value---activeactionpanetabnames"></a><span data-ttu-id="9a747-128">戻り値 - activeActionPaneTabNames</span><span class="sxs-lookup"><span data-stu-id="9a747-128">Return Value - activeActionPaneTabNames</span></span>

<span data-ttu-id="9a747-129">アクティブなタブの名前を含む配列です。</span><span class="sxs-lookup"><span data-stu-id="9a747-129">An array that contains the names of the active tabs.</span></span>

## <a name="method-caption"></a><span data-ttu-id="9a747-130">メソッド caption</span><span class="sxs-lookup"><span data-stu-id="9a747-130">Method caption</span></span>

```xpp
public str caption([str value])
```

### <a name="parameters---caption"></a><span data-ttu-id="9a747-131">パラメーター - caption</span><span class="sxs-lookup"><span data-stu-id="9a747-131">Parameters - caption</span></span>

<span data-ttu-id="9a747-132">値</span><span class="sxs-lookup"><span data-stu-id="9a747-132">value</span></span>  

### <a name="return-value---caption"></a><span data-ttu-id="9a747-133">戻り値 - caption</span><span class="sxs-lookup"><span data-stu-id="9a747-133">Return Value - caption</span></span>

## <a name="method-listpageargs"></a><span data-ttu-id="9a747-134">メソッド listPageArgs</span><span class="sxs-lookup"><span data-stu-id="9a747-134">Method listPageArgs</span></span>

```xpp
public ListPageArgs listPageArgs()
```

### <a name="return-value---listpageargs"></a><span data-ttu-id="9a747-135">戻り値 - listPageArgs</span><span class="sxs-lookup"><span data-stu-id="9a747-135">Return Value - listPageArgs</span></span>

## <a name="method-listpagefielddatafield"></a><span data-ttu-id="9a747-136">メソッド listPageFieldDataField</span><span class="sxs-lookup"><span data-stu-id="9a747-136">Method listPageFieldDataField</span></span>

```xpp
public int listPageFieldDataField(str fieldName)
```

### <a name="parameters---listpagefielddatafield"></a><span data-ttu-id="9a747-137">パラメーター - listPageFieldDataField</span><span class="sxs-lookup"><span data-stu-id="9a747-137">Parameters - listPageFieldDataField</span></span>

<span data-ttu-id="9a747-138">fieldName</span><span class="sxs-lookup"><span data-stu-id="9a747-138">fieldName</span></span>  

### <a name="return-value---listpagefielddatafield"></a><span data-ttu-id="9a747-139">戻り値 - listPageFieldDataField</span><span class="sxs-lookup"><span data-stu-id="9a747-139">Return Value - listPageFieldDataField</span></span>

## <a name="method-listpagefieldnames"></a><span data-ttu-id="9a747-140">メソッド listPageFieldNames</span><span class="sxs-lookup"><span data-stu-id="9a747-140">Method listPageFieldNames</span></span>

```xpp
public Array listPageFieldNames()
```

### <a name="return-value---listpagefieldnames"></a><span data-ttu-id="9a747-141">戻り値 - listPageFieldNames</span><span class="sxs-lookup"><span data-stu-id="9a747-141">Return Value - listPageFieldNames</span></span>

## <a name="method-listpagefieldtableid"></a><span data-ttu-id="9a747-142">メソッド listPageFieldTableId</span><span class="sxs-lookup"><span data-stu-id="9a747-142">Method listPageFieldTableId</span></span>

```xpp
public int listPageFieldTableId(str fieldName)
```

### <a name="parameters---listpagefieldtableid"></a><span data-ttu-id="9a747-143">パラメーター - listPageFieldTableId</span><span class="sxs-lookup"><span data-stu-id="9a747-143">Parameters - listPageFieldTableId</span></span>

<span data-ttu-id="9a747-144">fieldName</span><span class="sxs-lookup"><span data-stu-id="9a747-144">fieldName</span></span>  

### <a name="return-value---listpagefieldtableid"></a><span data-ttu-id="9a747-145">戻り値 - listPageFieldTableId</span><span class="sxs-lookup"><span data-stu-id="9a747-145">Return Value - listPageFieldTableId</span></span>

## <a name="method-listpagefieldvisible"></a><span data-ttu-id="9a747-146">メソッド listPageFieldVisible</span><span class="sxs-lookup"><span data-stu-id="9a747-146">Method listPageFieldVisible</span></span>

```xpp
public boolean listPageFieldVisible(str fieldName, [boolean visible])
```

### <a name="parameters---listpagefieldvisible"></a><span data-ttu-id="9a747-147">パラメーター - listPageFieldVisible</span><span class="sxs-lookup"><span data-stu-id="9a747-147">Parameters - listPageFieldVisible</span></span>

<span data-ttu-id="9a747-148">fieldName</span><span class="sxs-lookup"><span data-stu-id="9a747-148">fieldName</span></span>  

<!-- -->

<span data-ttu-id="9a747-149">表示</span><span class="sxs-lookup"><span data-stu-id="9a747-149">visible</span></span>  

### <a name="return-value---listpagefieldvisible"></a><span data-ttu-id="9a747-150">戻り値 - listPageFieldVisible</span><span class="sxs-lookup"><span data-stu-id="9a747-150">Return Value - listPageFieldVisible</span></span>

## <a name="method-modeledqueryname"></a><span data-ttu-id="9a747-151">メソッド modeledQueryName</span><span class="sxs-lookup"><span data-stu-id="9a747-151">Method modeledQueryName</span></span>

```xpp
public str modeledQueryName([str value])
```

### <a name="parameters---modeledqueryname"></a><span data-ttu-id="9a747-152">パラメーター - modeledQueryName</span><span class="sxs-lookup"><span data-stu-id="9a747-152">Parameters - modeledQueryName</span></span>

<span data-ttu-id="9a747-153">値</span><span class="sxs-lookup"><span data-stu-id="9a747-153">value</span></span>  

### <a name="return-value---modeledqueryname"></a><span data-ttu-id="9a747-154">戻り値 - modeledQueryName</span><span class="sxs-lookup"><span data-stu-id="9a747-154">Return Value - modeledQueryName</span></span>

## <a name="method-new"></a><span data-ttu-id="9a747-155">メソッド new</span><span class="sxs-lookup"><span data-stu-id="9a747-155">Method new</span></span>

<span data-ttu-id="9a747-156">ListPage クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="9a747-156">Initializes a new instance of the ListPage class.</span></span>

```xpp
public void new()
```

