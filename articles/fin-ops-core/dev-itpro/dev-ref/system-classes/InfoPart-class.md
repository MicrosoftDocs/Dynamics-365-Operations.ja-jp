---
title: InfoPart クラス
description: このトピックでは、InfoPart クラスについて説明します。
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
ms.openlocfilehash: 1f762e075c1308c12d35674e1c7763bd67a97686
ms.sourcegitcommit: 7b0cec2e898ef8ee33baf72f18cdd9cba0e9399c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/25/2020
ms.locfileid: "3502900"
---
# <a name="class-infopart"></a><span data-ttu-id="4bbff-103">クラス InfoPart</span><span class="sxs-lookup"><span data-stu-id="4bbff-103">Class InfoPart</span></span>

[!include [banner](../../includes/banner.md)]

```xpp
class InfoPart extends TreeNode
```

## <a name="remarks"></a><span data-ttu-id="4bbff-104">備考</span><span class="sxs-lookup"><span data-stu-id="4bbff-104">Remarks</span></span>

## <a name="examples"></a><span data-ttu-id="4bbff-105">例</span><span class="sxs-lookup"><span data-stu-id="4bbff-105">Examples</span></span>

## <a name="methods"></a><span data-ttu-id="4bbff-106">メソッド</span><span class="sxs-lookup"><span data-stu-id="4bbff-106">Methods</span></span>

| <span data-ttu-id="4bbff-107">方法</span><span class="sxs-lookup"><span data-stu-id="4bbff-107">Method</span></span>                                   | <span data-ttu-id="4bbff-108">説明</span><span class="sxs-lookup"><span data-stu-id="4bbff-108">Description</span></span>                                                                                                                               |
|------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4bbff-109">public str caption(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="4bbff-109">public str caption(\[str value\])</span></span>        | <span data-ttu-id="4bbff-110">コントロールのキャプションを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="4bbff-110">Gets or set the caption of the control.</span></span>                                                                                                   |
| <span data-ttu-id="4bbff-111">public str changedBy(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="4bbff-111">public str changedBy(\[str value\])</span></span>      | <span data-ttu-id="4bbff-112">アプリケーション オブジェクトを最後に変更したユーザーの名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="4bbff-112">Gets or sets the name of the user who last changed the application object.</span></span>                                                                |
| <span data-ttu-id="4bbff-113">public Date changedDate(\[Date value\])</span><span class="sxs-lookup"><span data-stu-id="4bbff-113">public Date changedDate(\[Date value\])</span></span>  | <span data-ttu-id="4bbff-114">アプリケーション オブジェクトが最後に変更された日付を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="4bbff-114">Gets or sets the date an application object was last changed.</span></span>                                                                             |
| <span data-ttu-id="4bbff-115">public str changedTime(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="4bbff-115">public str changedTime(\[str value\])</span></span>    | <span data-ttu-id="4bbff-116">アプリケーション オブジェクトが最後に変更された時刻を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="4bbff-116">Gets or sets the time an application object was last changed.</span></span>                                                                             |
| <span data-ttu-id="4bbff-117">public str createdBy(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="4bbff-117">public str createdBy(\[str value\])</span></span>      | <span data-ttu-id="4bbff-118">アプリケーション オブジェクトを作成したユーザーの名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="4bbff-118">Gets or sets the name of the user who created the application object.</span></span>                                                                     |
| <span data-ttu-id="4bbff-119">public Date creationDate(\[Date value\])</span><span class="sxs-lookup"><span data-stu-id="4bbff-119">public Date creationDate(\[Date value\])</span></span> | <span data-ttu-id="4bbff-120">アプリケーション オブジェクトが作成された日付を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="4bbff-120">Gets or sets the date an application object was created.</span></span>                                                                                  |
| <span data-ttu-id="4bbff-121">public str creationTime(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="4bbff-121">public str creationTime(\[str value\])</span></span>   |                                                                                                                                           |
| <span data-ttu-id="4bbff-122">public str name(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="4bbff-122">public str name(\[str value\])</span></span>           | <span data-ttu-id="4bbff-123">フォーム、レポート、テーブル、クエリ、または他のアプリケーション オブジェクトを識別するためのコードで使用される名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="4bbff-123">Gets or sets the name that is used in code to identify a form, report, table, query, or other application object.</span></span> |
| <span data-ttu-id="4bbff-124">public Guid origin(\[Guid value\])</span><span class="sxs-lookup"><span data-stu-id="4bbff-124">public Guid origin(\[Guid value\])</span></span>       |                                                                                                                                           |
| <span data-ttu-id="4bbff-125">public str query(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="4bbff-125">public str query(\[str value\])</span></span>          |                                                                                                                                           |
| <span data-ttu-id="4bbff-126">public void new()</span><span class="sxs-lookup"><span data-stu-id="4bbff-126">public void new()</span></span>                        | <span data-ttu-id="4bbff-127">InfoPart クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="4bbff-127">Initializes a new instance of the InfoPart class.</span></span>                                                                                         |

## <a name="method-caption"></a><span data-ttu-id="4bbff-128">メソッド caption</span><span class="sxs-lookup"><span data-stu-id="4bbff-128">Method caption</span></span>

<span data-ttu-id="4bbff-129">コントロールのキャプションを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="4bbff-129">Gets or set the caption of the control.</span></span>

```xpp
public str caption([str value])
```

### <a name="parameters---caption"></a><span data-ttu-id="4bbff-130">パラメーター - caption</span><span class="sxs-lookup"><span data-stu-id="4bbff-130">Parameters - caption</span></span>

<span data-ttu-id="4bbff-131">値</span><span class="sxs-lookup"><span data-stu-id="4bbff-131">value</span></span>  

### <a name="return-value---caption"></a><span data-ttu-id="4bbff-132">戻り値 - caption</span><span class="sxs-lookup"><span data-stu-id="4bbff-132">Return Value - caption</span></span>

<span data-ttu-id="4bbff-133">コントロールのキャプションとして使用される文字列。</span><span class="sxs-lookup"><span data-stu-id="4bbff-133">The string that is used as the caption of the control.</span></span>

## <a name="method-changedby"></a><span data-ttu-id="4bbff-134">メソッド changedBy</span><span class="sxs-lookup"><span data-stu-id="4bbff-134">Method changedBy</span></span>

<span data-ttu-id="4bbff-135">アプリケーション オブジェクトを最後に変更したユーザーの名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="4bbff-135">Gets or sets the name of the user who last changed the application object.</span></span>

```xpp
public str changedBy([str value])
```

### <a name="parameters---changedby"></a><span data-ttu-id="4bbff-136">パラメーター - changedBy</span><span class="sxs-lookup"><span data-stu-id="4bbff-136">Parameters - changedBy</span></span>

<span data-ttu-id="4bbff-137">値</span><span class="sxs-lookup"><span data-stu-id="4bbff-137">value</span></span>  

### <a name="return-value---changedby"></a><span data-ttu-id="4bbff-138">戻り値 - changedBy</span><span class="sxs-lookup"><span data-stu-id="4bbff-138">Return Value - changedBy</span></span>

<span data-ttu-id="4bbff-139">ユーザーの名前。</span><span class="sxs-lookup"><span data-stu-id="4bbff-139">The name of the user.</span></span>

## <a name="method-changeddate"></a><span data-ttu-id="4bbff-140">メソッド changedDate</span><span class="sxs-lookup"><span data-stu-id="4bbff-140">Method changedDate</span></span>

<span data-ttu-id="4bbff-141">アプリケーション オブジェクトが最後に変更された日付を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="4bbff-141">Gets or sets the date an application object was last changed.</span></span>

```xpp
public Date changedDate([Date value])
```

### <a name="parameters---changeddate"></a><span data-ttu-id="4bbff-142">パラメーター - changedDate</span><span class="sxs-lookup"><span data-stu-id="4bbff-142">Parameters - changedDate</span></span>

<span data-ttu-id="4bbff-143">値</span><span class="sxs-lookup"><span data-stu-id="4bbff-143">value</span></span>  

### <a name="return-value---changeddate"></a><span data-ttu-id="4bbff-144">戻り値 - changedDate</span><span class="sxs-lookup"><span data-stu-id="4bbff-144">Return Value - changedDate</span></span>

<span data-ttu-id="4bbff-145">アプリケーション オブジェクトが最後に変更された日付。</span><span class="sxs-lookup"><span data-stu-id="4bbff-145">The date an application object was last changed.</span></span>

## <a name="method-changedtime"></a><span data-ttu-id="4bbff-146">メソッド changedTime</span><span class="sxs-lookup"><span data-stu-id="4bbff-146">Method changedTime</span></span>

<span data-ttu-id="4bbff-147">アプリケーション オブジェクトが最後に変更された時刻を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="4bbff-147">Gets or sets the time an application object was last changed.</span></span>

```xpp
public str changedTime([str value])
```

### <a name="parameters---changedtime"></a><span data-ttu-id="4bbff-148">パラメーター - changedTime</span><span class="sxs-lookup"><span data-stu-id="4bbff-148">Parameters - changedTime</span></span>

<span data-ttu-id="4bbff-149">値</span><span class="sxs-lookup"><span data-stu-id="4bbff-149">value</span></span>  

### <a name="return-value---changedtime"></a><span data-ttu-id="4bbff-150">戻り値 - changedTime</span><span class="sxs-lookup"><span data-stu-id="4bbff-150">Return Value - changedTime</span></span>

<span data-ttu-id="4bbff-151">アプリケーション オブジェクトが最後に変更された時間。</span><span class="sxs-lookup"><span data-stu-id="4bbff-151">The time an application object was last changed.</span></span>

## <a name="method-createdby"></a><span data-ttu-id="4bbff-152">メソッド createdBy</span><span class="sxs-lookup"><span data-stu-id="4bbff-152">Method createdBy</span></span>

<span data-ttu-id="4bbff-153">アプリケーション オブジェクトを作成したユーザーの名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="4bbff-153">Gets or sets the name of the user who created the application object.</span></span>

```xpp
public str createdBy([str value])
```

### <a name="parameters---createdby"></a><span data-ttu-id="4bbff-154">パラメーター - createdBy</span><span class="sxs-lookup"><span data-stu-id="4bbff-154">Parameters - createdBy</span></span>

<span data-ttu-id="4bbff-155">値</span><span class="sxs-lookup"><span data-stu-id="4bbff-155">value</span></span>  

### <a name="return-value---createdby"></a><span data-ttu-id="4bbff-156">戻り値 - createdBy</span><span class="sxs-lookup"><span data-stu-id="4bbff-156">Return Value - createdBy</span></span>

<span data-ttu-id="4bbff-157">ユーザーの名前。</span><span class="sxs-lookup"><span data-stu-id="4bbff-157">The name of the user.</span></span>

## <a name="method-creationdate"></a><span data-ttu-id="4bbff-158">メソッド creationDate</span><span class="sxs-lookup"><span data-stu-id="4bbff-158">Method creationDate</span></span>

<span data-ttu-id="4bbff-159">アプリケーション オブジェクトが作成された日付を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="4bbff-159">Gets or sets the date an application object was created.</span></span>

```xpp
public Date creationDate([Date value])
```

### <a name="parameters---creationdate"></a><span data-ttu-id="4bbff-160">パラメーター - creationDate</span><span class="sxs-lookup"><span data-stu-id="4bbff-160">Parameters - creationDate</span></span>

<span data-ttu-id="4bbff-161">値</span><span class="sxs-lookup"><span data-stu-id="4bbff-161">value</span></span>  

### <a name="return-value---creationdate"></a><span data-ttu-id="4bbff-162">戻り値 - creationDate</span><span class="sxs-lookup"><span data-stu-id="4bbff-162">Return Value - creationDate</span></span>

<span data-ttu-id="4bbff-163">アプリケーション オブジェクトが作成された日付。</span><span class="sxs-lookup"><span data-stu-id="4bbff-163">The date an application object was created.</span></span>

## <a name="method-creationtime"></a><span data-ttu-id="4bbff-164">メソッド creationTime</span><span class="sxs-lookup"><span data-stu-id="4bbff-164">Method creationTime</span></span>

```xpp
public str creationTime([str value])
```

### <a name="parameters---creationtime"></a><span data-ttu-id="4bbff-165">パラメーター - creationTime</span><span class="sxs-lookup"><span data-stu-id="4bbff-165">Parameters - creationTime</span></span>

<span data-ttu-id="4bbff-166">値</span><span class="sxs-lookup"><span data-stu-id="4bbff-166">value</span></span>  

### <a name="return-value---creationtime"></a><span data-ttu-id="4bbff-167">戻り値 - creationTime</span><span class="sxs-lookup"><span data-stu-id="4bbff-167">Return Value - creationTime</span></span>

## <a name="method-name"></a><span data-ttu-id="4bbff-168">メソッド名</span><span class="sxs-lookup"><span data-stu-id="4bbff-168">Method name</span></span>

<span data-ttu-id="4bbff-169">フォーム、レポート、テーブル、クエリ、または他のアプリケーション オブジェクトを識別するためのコードで使用される名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="4bbff-169">Gets or sets the name that is used in code to identify a form, report, table, query, or other application object.</span></span>

```xpp
public str name([str value])
```

### <a name="parameters---name"></a><span data-ttu-id="4bbff-170">パラメーター - name</span><span class="sxs-lookup"><span data-stu-id="4bbff-170">Parameters - name</span></span>

<span data-ttu-id="4bbff-171">値</span><span class="sxs-lookup"><span data-stu-id="4bbff-171">value</span></span>  

### <a name="return-value---name"></a><span data-ttu-id="4bbff-172">戻り値 - name</span><span class="sxs-lookup"><span data-stu-id="4bbff-172">Return Value - name</span></span>

<span data-ttu-id="4bbff-173">アプリケーション オブジェクトを識別するためにコードで使用される名前。</span><span class="sxs-lookup"><span data-stu-id="4bbff-173">The name that is used in code to identify an application object.</span></span>

### <a name="remarks---name"></a><span data-ttu-id="4bbff-174">備考 - name</span><span class="sxs-lookup"><span data-stu-id="4bbff-174">Remarks - name</span></span>

<span data-ttu-id="4bbff-175">オブジェクトの名前プロパティ値は、コードの競合を避けるために、次の基準を満たしている必要があります。</span><span class="sxs-lookup"><span data-stu-id="4bbff-175">The name property value of an object must meet the following criteria to avoid code conflicts:</span></span>

-   <span data-ttu-id="4bbff-176">文字で始めます。</span><span class="sxs-lookup"><span data-stu-id="4bbff-176">Begins with a letter.</span></span>
-   <span data-ttu-id="4bbff-177">250 文字を超えないでください。</span><span class="sxs-lookup"><span data-stu-id="4bbff-177">Doesn't exceed 250 characters.</span></span>
-   <span data-ttu-id="4bbff-178">数字とアンダースコア文字を含めることができます。</span><span class="sxs-lookup"><span data-stu-id="4bbff-178">Can include numbers and underscore characters.</span></span>
-   <span data-ttu-id="4bbff-179">句読点やスペースを含めることはできません。</span><span class="sxs-lookup"><span data-stu-id="4bbff-179">Cannot include punctuation or spaces.</span></span>
-   <span data-ttu-id="4bbff-180">テーブルは、拡張データ型、基本列挙型、クラスなどの他のパブリック オブジェクトと同じ名前を持つことはできません。</span><span class="sxs-lookup"><span data-stu-id="4bbff-180">Tables cannot have the same name as other public objects, such as extended data types, base enums, classes, and so on.</span></span>

## <a name="method-origin"></a><span data-ttu-id="4bbff-181">メソッド origin</span><span class="sxs-lookup"><span data-stu-id="4bbff-181">Method origin</span></span>

```xpp
public Guid origin([Guid value])
```

### <a name="parameters---origin"></a><span data-ttu-id="4bbff-182">パラメーター - origin</span><span class="sxs-lookup"><span data-stu-id="4bbff-182">Parameters - origin</span></span>

<span data-ttu-id="4bbff-183">値</span><span class="sxs-lookup"><span data-stu-id="4bbff-183">value</span></span>  

### <a name="return-value---origin"></a><span data-ttu-id="4bbff-184">戻り値 - origin</span><span class="sxs-lookup"><span data-stu-id="4bbff-184">Return Value - origin</span></span>

## <a name="method-query"></a><span data-ttu-id="4bbff-185">メソッド query</span><span class="sxs-lookup"><span data-stu-id="4bbff-185">Method query</span></span>

```xpp
public str query([str value])
```

### <a name="parameters---query"></a><span data-ttu-id="4bbff-186">パラメーター - query</span><span class="sxs-lookup"><span data-stu-id="4bbff-186">Parameters - query</span></span>

<span data-ttu-id="4bbff-187">値</span><span class="sxs-lookup"><span data-stu-id="4bbff-187">value</span></span>  

### <a name="return-value---query"></a><span data-ttu-id="4bbff-188">戻り値 - query</span><span class="sxs-lookup"><span data-stu-id="4bbff-188">Return Value - query</span></span>

## <a name="method-new"></a><span data-ttu-id="4bbff-189">メソッド new</span><span class="sxs-lookup"><span data-stu-id="4bbff-189">Method new</span></span>

<span data-ttu-id="4bbff-190">InfoPart クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="4bbff-190">Initializes a new instance of the InfoPart class.</span></span>

```xpp
public void new()
```

