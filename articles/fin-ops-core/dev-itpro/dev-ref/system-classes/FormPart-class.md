---
title: FormPart クラス
description: このトピックでは、FormPart クラスについて説明します。
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
ms.openlocfilehash: da0592a0b720a9e64cf16d609f0d4ce577e398b3
ms.sourcegitcommit: 7b0cec2e898ef8ee33baf72f18cdd9cba0e9399c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/25/2020
ms.locfileid: "3502913"
---
# <a name="class-formpart"></a><span data-ttu-id="eb573-103">クラス FormPart</span><span class="sxs-lookup"><span data-stu-id="eb573-103">Class FormPart</span></span>

[!include [banner](../../includes/banner.md)]

```xpp
class FormPart extends TreeNode
```

## <a name="remarks"></a><span data-ttu-id="eb573-104">備考</span><span class="sxs-lookup"><span data-stu-id="eb573-104">Remarks</span></span>

## <a name="examples"></a><span data-ttu-id="eb573-105">例</span><span class="sxs-lookup"><span data-stu-id="eb573-105">Examples</span></span>

## <a name="methods"></a><span data-ttu-id="eb573-106">メソッド</span><span class="sxs-lookup"><span data-stu-id="eb573-106">Methods</span></span>

| <span data-ttu-id="eb573-107">方法</span><span class="sxs-lookup"><span data-stu-id="eb573-107">Method</span></span>                                       | <span data-ttu-id="eb573-108">説明</span><span class="sxs-lookup"><span data-stu-id="eb573-108">Description</span></span>                                                                                                                               |
|----------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="eb573-109">public str caption(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="eb573-109">public str caption(\[str value\])</span></span>            | <span data-ttu-id="eb573-110">コントロールのキャプションを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="eb573-110">Gets or set the caption of the control.</span></span>                                                                                                   |
| <span data-ttu-id="eb573-111">public str form(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="eb573-111">public str form(\[str value\])</span></span>               |                                                                                                                                           |
| <span data-ttu-id="eb573-112">public str managedContentItem(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="eb573-112">public str managedContentItem(\[str value\])</span></span> |                                                                                                                                           |
| <span data-ttu-id="eb573-113">public str name(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="eb573-113">public str name(\[str value\])</span></span>               | <span data-ttu-id="eb573-114">フォーム、レポート、テーブル、クエリ、または他のアプリケーション オブジェクトを識別するためのコードで使用される名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="eb573-114">Gets or sets the name that is used in code to identify a form, report, table, query, or other application object.</span></span> |
| <span data-ttu-id="eb573-115">public Guid origin(\[Guid value\])</span><span class="sxs-lookup"><span data-stu-id="eb573-115">public Guid origin(\[Guid value\])</span></span>           |                                                                                                                                           |
| <span data-ttu-id="eb573-116">public void new()</span><span class="sxs-lookup"><span data-stu-id="eb573-116">public void new()</span></span>                            | <span data-ttu-id="eb573-117">FormPart クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="eb573-117">Initializes a new instance of the FormPart class.</span></span>                                                                                         |

## <a name="method-caption"></a><span data-ttu-id="eb573-118">メソッド caption</span><span class="sxs-lookup"><span data-stu-id="eb573-118">Method caption</span></span>

<span data-ttu-id="eb573-119">コントロールのキャプションを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="eb573-119">Gets or set the caption of the control.</span></span>

```xpp
public str caption([str value])
```

### <a name="parameters---caption"></a><span data-ttu-id="eb573-120">パラメーター - caption</span><span class="sxs-lookup"><span data-stu-id="eb573-120">Parameters - caption</span></span>

<span data-ttu-id="eb573-121">値</span><span class="sxs-lookup"><span data-stu-id="eb573-121">value</span></span>  

### <a name="return-value---caption"></a><span data-ttu-id="eb573-122">戻り値 - caption</span><span class="sxs-lookup"><span data-stu-id="eb573-122">Return Value - caption</span></span>

<span data-ttu-id="eb573-123">コントロールのキャプションとして使用される文字列。</span><span class="sxs-lookup"><span data-stu-id="eb573-123">The string that is used as the caption of the control.</span></span>

## <a name="method-form"></a><span data-ttu-id="eb573-124">メソッド form</span><span class="sxs-lookup"><span data-stu-id="eb573-124">Method form</span></span>

```xpp
public str form([str value])
```

### <a name="parameters---form"></a><span data-ttu-id="eb573-125">パラメーター - form</span><span class="sxs-lookup"><span data-stu-id="eb573-125">Parameters - form</span></span>

<span data-ttu-id="eb573-126">値</span><span class="sxs-lookup"><span data-stu-id="eb573-126">value</span></span>  

### <a name="return-value---form"></a><span data-ttu-id="eb573-127">戻り値 - form</span><span class="sxs-lookup"><span data-stu-id="eb573-127">Return Value - form</span></span>

## <a name="method-managedcontentitem"></a><span data-ttu-id="eb573-128">メソッド managedContentItem</span><span class="sxs-lookup"><span data-stu-id="eb573-128">Method managedContentItem</span></span>

```xpp
public str managedContentItem([str value])
```

### <a name="parameters---managedcontentitem"></a><span data-ttu-id="eb573-129">パラメーター - managedContentItem</span><span class="sxs-lookup"><span data-stu-id="eb573-129">Parameters - managedContentItem</span></span>

<span data-ttu-id="eb573-130">値</span><span class="sxs-lookup"><span data-stu-id="eb573-130">value</span></span>  

### <a name="return-value---managedcontentitem"></a><span data-ttu-id="eb573-131">戻り値 - managedContentItem</span><span class="sxs-lookup"><span data-stu-id="eb573-131">Return Value - managedContentItem</span></span>

## <a name="method-name"></a><span data-ttu-id="eb573-132">メソッド名</span><span class="sxs-lookup"><span data-stu-id="eb573-132">Method name</span></span>

<span data-ttu-id="eb573-133">フォーム、レポート、テーブル、クエリ、または他のアプリケーション オブジェクトを識別するためのコードで使用される名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="eb573-133">Gets or sets the name that is used in code to identify a form, report, table, query, or other application object.</span></span>

```xpp
public str name([str value])
```

### <a name="parameters---name"></a><span data-ttu-id="eb573-134">パラメーター - name</span><span class="sxs-lookup"><span data-stu-id="eb573-134">Parameters - name</span></span>

<span data-ttu-id="eb573-135">値</span><span class="sxs-lookup"><span data-stu-id="eb573-135">value</span></span>  

### <a name="return-value---name"></a><span data-ttu-id="eb573-136">戻り値 - name</span><span class="sxs-lookup"><span data-stu-id="eb573-136">Return Value - name</span></span>

<span data-ttu-id="eb573-137">アプリケーション オブジェクトを識別するためにコードで使用される名前。</span><span class="sxs-lookup"><span data-stu-id="eb573-137">The name that is used in code to identify an application object.</span></span>

### <a name="remarks---name"></a><span data-ttu-id="eb573-138">備考 - name</span><span class="sxs-lookup"><span data-stu-id="eb573-138">Remarks - name</span></span>

<span data-ttu-id="eb573-139">オブジェクトの名前プロパティ値は、コードの競合を避けるために、次の基準を満たしている必要があります。</span><span class="sxs-lookup"><span data-stu-id="eb573-139">The name property value of an object must meet the following criteria to avoid code conflicts:</span></span>

-   <span data-ttu-id="eb573-140">文字で始めます。</span><span class="sxs-lookup"><span data-stu-id="eb573-140">Begins with a letter.</span></span>
-   <span data-ttu-id="eb573-141">250 文字を超えないでください。</span><span class="sxs-lookup"><span data-stu-id="eb573-141">Doesn't exceed 250 characters.</span></span>
-   <span data-ttu-id="eb573-142">数字とアンダースコア文字を含めることができます。</span><span class="sxs-lookup"><span data-stu-id="eb573-142">Can include numbers and underscore characters.</span></span>
-   <span data-ttu-id="eb573-143">句読点やスペースを含めることはできません。</span><span class="sxs-lookup"><span data-stu-id="eb573-143">Cannot include punctuation or spaces.</span></span>
-   <span data-ttu-id="eb573-144">テーブルは、拡張データ型、基本列挙型、クラスなどの他のパブリック オブジェクトと同じ名前を持つことはできません。</span><span class="sxs-lookup"><span data-stu-id="eb573-144">Tables cannot have the same name as other public objects, such as extended data types, base enums, classes, and so on.</span></span>

## <a name="method-origin"></a><span data-ttu-id="eb573-145">メソッド origin</span><span class="sxs-lookup"><span data-stu-id="eb573-145">Method origin</span></span>

```xpp
public Guid origin([Guid value])
```

### <a name="parameters---origin"></a><span data-ttu-id="eb573-146">パラメーター - origin</span><span class="sxs-lookup"><span data-stu-id="eb573-146">Parameters - origin</span></span>

<span data-ttu-id="eb573-147">値</span><span class="sxs-lookup"><span data-stu-id="eb573-147">value</span></span>  

### <a name="return-value---origin"></a><span data-ttu-id="eb573-148">戻り値 - origin</span><span class="sxs-lookup"><span data-stu-id="eb573-148">Return Value - origin</span></span>

## <a name="method-new"></a><span data-ttu-id="eb573-149">メソッド new</span><span class="sxs-lookup"><span data-stu-id="eb573-149">Method new</span></span>

<span data-ttu-id="eb573-150">FormPart クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="eb573-150">Initializes a new instance of the FormPart class.</span></span>

```xpp
public void new()
```

