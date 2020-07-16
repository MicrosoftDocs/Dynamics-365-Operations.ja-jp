---
title: ReportLibraryNode クラス
description: このトピックでは、ReportLibraryNode クラスについて説明します。
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
ms.openlocfilehash: d16dca1869e4a056da72ecf805949a8683732ea8
ms.sourcegitcommit: 7b0cec2e898ef8ee33baf72f18cdd9cba0e9399c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/25/2020
ms.locfileid: "3502838"
---
# <a name="class-reportlibrarynode"></a><span data-ttu-id="313a6-103">クラス ReportLibraryNode</span><span class="sxs-lookup"><span data-stu-id="313a6-103">Class ReportLibraryNode</span></span>

[!include [banner](../../includes/banner.md)]

```xpp
class ReportLibraryNode extends xresourceNode
```

## <a name="remarks"></a><span data-ttu-id="313a6-104">備考</span><span class="sxs-lookup"><span data-stu-id="313a6-104">Remarks</span></span>

## <a name="examples"></a><span data-ttu-id="313a6-105">例</span><span class="sxs-lookup"><span data-stu-id="313a6-105">Examples</span></span>

## <a name="methods"></a><span data-ttu-id="313a6-106">メソッド</span><span class="sxs-lookup"><span data-stu-id="313a6-106">Methods</span></span>

| <span data-ttu-id="313a6-107">方法</span><span class="sxs-lookup"><span data-stu-id="313a6-107">Method</span></span>                                       | <span data-ttu-id="313a6-108">説明</span><span class="sxs-lookup"><span data-stu-id="313a6-108">Description</span></span>                                                                                                                               |
|----------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="313a6-109">public str changedBy(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="313a6-109">public str changedBy(\[str value\])</span></span>          | <span data-ttu-id="313a6-110">アプリケーション オブジェクトを最後に変更したユーザーの名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="313a6-110">Gets or sets the name of the user who last changed the application object.</span></span>                                                                |
| <span data-ttu-id="313a6-111">public Date changedDate(\[Date value\])</span><span class="sxs-lookup"><span data-stu-id="313a6-111">public Date changedDate(\[Date value\])</span></span>      | <span data-ttu-id="313a6-112">アプリケーション オブジェクトが最後に変更された日付を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="313a6-112">Gets or sets the date an application object was last changed.</span></span>                                                                             |
| <span data-ttu-id="313a6-113">public str changedTime(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="313a6-113">public str changedTime(\[str value\])</span></span>        | <span data-ttu-id="313a6-114">アプリケーション オブジェクトが最後に変更された時刻を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="313a6-114">Gets or sets the time an application object was last changed.</span></span>                                                                             |
| <span data-ttu-id="313a6-115">public str createdBy(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="313a6-115">public str createdBy(\[str value\])</span></span>          | <span data-ttu-id="313a6-116">アプリケーション オブジェクトを作成したユーザーの名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="313a6-116">Gets or sets the name of the user who created the application object.</span></span>                                                                     |
| <span data-ttu-id="313a6-117">public Date creationDate(\[Date value\])</span><span class="sxs-lookup"><span data-stu-id="313a6-117">public Date creationDate(\[Date value\])</span></span>     | <span data-ttu-id="313a6-118">アプリケーション オブジェクトが作成された日付を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="313a6-118">Gets or sets the date an application object was created.</span></span>                                                                                  |
| <span data-ttu-id="313a6-119">public str creationTime(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="313a6-119">public str creationTime(\[str value\])</span></span>       |                                                                                                                                           |
| <span data-ttu-id="313a6-120">public str designs(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="313a6-120">public str designs(\[str value\])</span></span>            |                                                                                                                                           |
| <span data-ttu-id="313a6-121">public str name(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="313a6-121">public str name(\[str value\])</span></span>               | <span data-ttu-id="313a6-122">フォーム、レポート、テーブル、クエリ、または他のアプリケーション オブジェクトを識別するためのコードで使用される名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="313a6-122">Gets or sets the name that is used in code to identify a form, report, table, query, or other application object.</span></span> |
| <span data-ttu-id="313a6-123">public Guid origin(\[Guid value\])</span><span class="sxs-lookup"><span data-stu-id="313a6-123">public Guid origin(\[Guid value\])</span></span>           |                                                                                                                                           |
| <span data-ttu-id="313a6-124">public str projectGuid(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="313a6-124">public str projectGuid(\[str value\])</span></span>        |                                                                                                                                           |
| <span data-ttu-id="313a6-125">public str referencedProjects(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="313a6-125">public str referencedProjects(\[str value\])</span></span> |                                                                                                                                           |

## <a name="method-changedby"></a><span data-ttu-id="313a6-126">メソッド changedBy</span><span class="sxs-lookup"><span data-stu-id="313a6-126">Method changedBy</span></span>

<span data-ttu-id="313a6-127">アプリケーション オブジェクトを最後に変更したユーザーの名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="313a6-127">Gets or sets the name of the user who last changed the application object.</span></span>

```xpp
public str changedBy([str value])
```

### <a name="parameters---changedby"></a><span data-ttu-id="313a6-128">パラメーター - changedBy</span><span class="sxs-lookup"><span data-stu-id="313a6-128">Parameters - changedBy</span></span>

<span data-ttu-id="313a6-129">値</span><span class="sxs-lookup"><span data-stu-id="313a6-129">value</span></span>  

### <a name="return-value---changedby"></a><span data-ttu-id="313a6-130">戻り値 - changedBy</span><span class="sxs-lookup"><span data-stu-id="313a6-130">Return Value - changedBy</span></span>

<span data-ttu-id="313a6-131">ユーザーの名前。</span><span class="sxs-lookup"><span data-stu-id="313a6-131">The name of the user.</span></span>

## <a name="method-changeddate"></a><span data-ttu-id="313a6-132">メソッド changedDate</span><span class="sxs-lookup"><span data-stu-id="313a6-132">Method changedDate</span></span>

<span data-ttu-id="313a6-133">アプリケーション オブジェクトが最後に変更された日付を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="313a6-133">Gets or sets the date an application object was last changed.</span></span>

```xpp
public Date changedDate([Date value])
```

### <a name="parameters---changeddate"></a><span data-ttu-id="313a6-134">パラメーター - changedDate</span><span class="sxs-lookup"><span data-stu-id="313a6-134">Parameters - changedDate</span></span>

<span data-ttu-id="313a6-135">値</span><span class="sxs-lookup"><span data-stu-id="313a6-135">value</span></span>  

### <a name="return-value---changeddate"></a><span data-ttu-id="313a6-136">戻り値 - changedDate</span><span class="sxs-lookup"><span data-stu-id="313a6-136">Return Value - changedDate</span></span>

<span data-ttu-id="313a6-137">アプリケーション オブジェクトが最後に変更された日付。</span><span class="sxs-lookup"><span data-stu-id="313a6-137">The date an application object was last changed.</span></span>

## <a name="method-changedtime"></a><span data-ttu-id="313a6-138">メソッド changedTime</span><span class="sxs-lookup"><span data-stu-id="313a6-138">Method changedTime</span></span>

<span data-ttu-id="313a6-139">アプリケーション オブジェクトが最後に変更された時刻を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="313a6-139">Gets or sets the time an application object was last changed.</span></span>

```xpp
public str changedTime([str value])
```

### <a name="parameters---changedtime"></a><span data-ttu-id="313a6-140">パラメーター - changedTime</span><span class="sxs-lookup"><span data-stu-id="313a6-140">Parameters - changedTime</span></span>

<span data-ttu-id="313a6-141">値</span><span class="sxs-lookup"><span data-stu-id="313a6-141">value</span></span>  

### <a name="return-value---changedtime"></a><span data-ttu-id="313a6-142">戻り値 - changedTime</span><span class="sxs-lookup"><span data-stu-id="313a6-142">Return Value - changedTime</span></span>

<span data-ttu-id="313a6-143">アプリケーション オブジェクトが最後に変更された時間。</span><span class="sxs-lookup"><span data-stu-id="313a6-143">The time an application object was last changed.</span></span>

## <a name="method-createdby"></a><span data-ttu-id="313a6-144">メソッド createdBy</span><span class="sxs-lookup"><span data-stu-id="313a6-144">Method createdBy</span></span>

<span data-ttu-id="313a6-145">アプリケーション オブジェクトを作成したユーザーの名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="313a6-145">Gets or sets the name of the user who created the application object.</span></span>

```xpp
public str createdBy([str value])
```

### <a name="parameters---createdby"></a><span data-ttu-id="313a6-146">パラメーター - createdBy</span><span class="sxs-lookup"><span data-stu-id="313a6-146">Parameters - createdBy</span></span>

<span data-ttu-id="313a6-147">値</span><span class="sxs-lookup"><span data-stu-id="313a6-147">value</span></span>  

### <a name="return-value---createdby"></a><span data-ttu-id="313a6-148">戻り値 - createdBy</span><span class="sxs-lookup"><span data-stu-id="313a6-148">Return Value - createdBy</span></span>

<span data-ttu-id="313a6-149">ユーザーの名前。</span><span class="sxs-lookup"><span data-stu-id="313a6-149">The name of the user.</span></span>

## <a name="method-creationdate"></a><span data-ttu-id="313a6-150">メソッド creationDate</span><span class="sxs-lookup"><span data-stu-id="313a6-150">Method creationDate</span></span>

<span data-ttu-id="313a6-151">アプリケーション オブジェクトが作成された日付を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="313a6-151">Gets or sets the date an application object was created.</span></span>

```xpp
public Date creationDate([Date value])
```

### <a name="parameters---creationdate"></a><span data-ttu-id="313a6-152">パラメーター - creationDate</span><span class="sxs-lookup"><span data-stu-id="313a6-152">Parameters - creationDate</span></span>

<span data-ttu-id="313a6-153">値</span><span class="sxs-lookup"><span data-stu-id="313a6-153">value</span></span>  

### <a name="return-value---creationdate"></a><span data-ttu-id="313a6-154">戻り値 - creationDate</span><span class="sxs-lookup"><span data-stu-id="313a6-154">Return Value - creationDate</span></span>

<span data-ttu-id="313a6-155">アプリケーション オブジェクトが作成された日付。</span><span class="sxs-lookup"><span data-stu-id="313a6-155">The date an application object was created.</span></span>

## <a name="method-creationtime"></a><span data-ttu-id="313a6-156">メソッド creationTime</span><span class="sxs-lookup"><span data-stu-id="313a6-156">Method creationTime</span></span>

```xpp
public str creationTime([str value])
```

### <a name="parameters---creationtime"></a><span data-ttu-id="313a6-157">パラメーター - creationTime</span><span class="sxs-lookup"><span data-stu-id="313a6-157">Parameters - creationTime</span></span>

<span data-ttu-id="313a6-158">値</span><span class="sxs-lookup"><span data-stu-id="313a6-158">value</span></span>  

### <a name="return-value---creationtime"></a><span data-ttu-id="313a6-159">戻り値 - creationTime</span><span class="sxs-lookup"><span data-stu-id="313a6-159">Return Value - creationTime</span></span>

## <a name="method-designs"></a><span data-ttu-id="313a6-160">メソッド designs</span><span class="sxs-lookup"><span data-stu-id="313a6-160">Method designs</span></span>

```xpp
public str designs([str value])
```

### <a name="parameters---designs"></a><span data-ttu-id="313a6-161">パラメーター - designs</span><span class="sxs-lookup"><span data-stu-id="313a6-161">Parameters - designs</span></span>

<span data-ttu-id="313a6-162">値</span><span class="sxs-lookup"><span data-stu-id="313a6-162">value</span></span>  

### <a name="return-value---designs"></a><span data-ttu-id="313a6-163">戻り値 - designs</span><span class="sxs-lookup"><span data-stu-id="313a6-163">Return Value - designs</span></span>

## <a name="method-name"></a><span data-ttu-id="313a6-164">メソッド名</span><span class="sxs-lookup"><span data-stu-id="313a6-164">Method name</span></span>

<span data-ttu-id="313a6-165">フォーム、レポート、テーブル、クエリ、または他のアプリケーション オブジェクトを識別するためのコードで使用される名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="313a6-165">Gets or sets the name that is used in code to identify a form, report, table, query, or other application object.</span></span>

```xpp
public str name([str value])
```

### <a name="parameters---name"></a><span data-ttu-id="313a6-166">パラメーター - name</span><span class="sxs-lookup"><span data-stu-id="313a6-166">Parameters - name</span></span>

<span data-ttu-id="313a6-167">値</span><span class="sxs-lookup"><span data-stu-id="313a6-167">value</span></span>  

### <a name="return-value---name"></a><span data-ttu-id="313a6-168">戻り値 - name</span><span class="sxs-lookup"><span data-stu-id="313a6-168">Return Value - name</span></span>

<span data-ttu-id="313a6-169">アプリケーション オブジェクトを識別するためにコードで使用される名前。</span><span class="sxs-lookup"><span data-stu-id="313a6-169">The name that is used in code to identify an application object.</span></span>

### <a name="remarks---name"></a><span data-ttu-id="313a6-170">備考 - name</span><span class="sxs-lookup"><span data-stu-id="313a6-170">Remarks - name</span></span>

<span data-ttu-id="313a6-171">オブジェクトの名前プロパティ値は、コードの競合を避けるために、次の基準を満たしている必要があります。</span><span class="sxs-lookup"><span data-stu-id="313a6-171">The name property value of an object must meet the following criteria to avoid code conflicts:</span></span>

-   <span data-ttu-id="313a6-172">文字で始めます。</span><span class="sxs-lookup"><span data-stu-id="313a6-172">Begins with a letter.</span></span>
-   <span data-ttu-id="313a6-173">250 文字を超えないでください。</span><span class="sxs-lookup"><span data-stu-id="313a6-173">Doesn't exceed 250 characters.</span></span>
-   <span data-ttu-id="313a6-174">数字とアンダースコア文字を含めることができます。</span><span class="sxs-lookup"><span data-stu-id="313a6-174">Can include numbers and underscore characters.</span></span>
-   <span data-ttu-id="313a6-175">句読点やスペースを含めることはできません。</span><span class="sxs-lookup"><span data-stu-id="313a6-175">Cannot include punctuation or spaces.</span></span>
-   <span data-ttu-id="313a6-176">テーブルは、拡張データ型、基本列挙型、クラスなどの他のパブリック オブジェクトと同じ名前を持つことはできません。</span><span class="sxs-lookup"><span data-stu-id="313a6-176">Tables cannot have the same name as other public objects, such as extended data types, base enums, classes, and so on.</span></span>

## <a name="method-origin"></a><span data-ttu-id="313a6-177">メソッド origin</span><span class="sxs-lookup"><span data-stu-id="313a6-177">Method origin</span></span>

```xpp
public Guid origin([Guid value])
```

### <a name="parameters---origin"></a><span data-ttu-id="313a6-178">パラメーター - origin</span><span class="sxs-lookup"><span data-stu-id="313a6-178">Parameters - origin</span></span>

<span data-ttu-id="313a6-179">値</span><span class="sxs-lookup"><span data-stu-id="313a6-179">value</span></span>  

### <a name="return-value---origin"></a><span data-ttu-id="313a6-180">戻り値 - origin</span><span class="sxs-lookup"><span data-stu-id="313a6-180">Return Value - origin</span></span>

## <a name="method-projectguid"></a><span data-ttu-id="313a6-181">メソッド projectGuid</span><span class="sxs-lookup"><span data-stu-id="313a6-181">Method projectGuid</span></span>

```xpp
public str projectGuid([str value])
```

### <a name="parameters---projectguid"></a><span data-ttu-id="313a6-182">パラメーター - projectGuid</span><span class="sxs-lookup"><span data-stu-id="313a6-182">Parameters - projectGuid</span></span>

<span data-ttu-id="313a6-183">値</span><span class="sxs-lookup"><span data-stu-id="313a6-183">value</span></span>  

### <a name="return-value---projectguid"></a><span data-ttu-id="313a6-184">戻り値 - projectGuid</span><span class="sxs-lookup"><span data-stu-id="313a6-184">Return Value - projectGuid</span></span>

## <a name="method-referencedprojects"></a><span data-ttu-id="313a6-185">メソッド referencedProjects</span><span class="sxs-lookup"><span data-stu-id="313a6-185">Method referencedProjects</span></span>

```xpp
public str referencedProjects([str value])
```

### <a name="parameters---referencedprojects"></a><span data-ttu-id="313a6-186">パラメーター - referencedProjects</span><span class="sxs-lookup"><span data-stu-id="313a6-186">Parameters - referencedProjects</span></span>

<span data-ttu-id="313a6-187">値</span><span class="sxs-lookup"><span data-stu-id="313a6-187">value</span></span>  

### <a name="return-value---referencedprojects"></a><span data-ttu-id="313a6-188">戻り値 - referencedProjects</span><span class="sxs-lookup"><span data-stu-id="313a6-188">Return Value - referencedProjects</span></span>

