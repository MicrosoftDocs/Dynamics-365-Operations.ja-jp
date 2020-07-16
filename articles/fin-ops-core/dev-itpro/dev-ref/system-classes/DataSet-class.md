---
title: DataSet クラス
description: このトピックでは、DataSet クラスについて説明します。
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
ms.openlocfilehash: 8de93053ace905a2e8fa5ba44e5ef84e97c1d429
ms.sourcegitcommit: 7b0cec2e898ef8ee33baf72f18cdd9cba0e9399c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/25/2020
ms.locfileid: "3502736"
---
# <a name="class-dataset"></a><span data-ttu-id="d0cff-103">クラス データセット</span><span class="sxs-lookup"><span data-stu-id="d0cff-103">Class DataSet</span></span>

[!include [banner](../../includes/banner.md)]

```xpp
class DataSet extends TreeNode
```

## <a name="remarks"></a><span data-ttu-id="d0cff-104">備考</span><span class="sxs-lookup"><span data-stu-id="d0cff-104">Remarks</span></span>

## <a name="examples"></a><span data-ttu-id="d0cff-105">例</span><span class="sxs-lookup"><span data-stu-id="d0cff-105">Examples</span></span>

## <a name="methods"></a><span data-ttu-id="d0cff-106">メソッド</span><span class="sxs-lookup"><span data-stu-id="d0cff-106">Methods</span></span>

| <span data-ttu-id="d0cff-107">方法</span><span class="sxs-lookup"><span data-stu-id="d0cff-107">Method</span></span>                                                  | <span data-ttu-id="d0cff-108">説明</span><span class="sxs-lookup"><span data-stu-id="d0cff-108">Description</span></span>                                                                                                                       |
|---------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d0cff-109">public FormBuildDataSource addDataSource(str name)</span><span class="sxs-lookup"><span data-stu-id="d0cff-109">public FormBuildDataSource addDataSource(str name)</span></span>      |                                                                                                                                   |
| <span data-ttu-id="d0cff-110">public str changedBy(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="d0cff-110">public str changedBy(\[str value\])</span></span>                     | <span data-ttu-id="d0cff-111">アプリケーション オブジェクトを最後に変更したユーザーの名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="d0cff-111">Gets or sets the name of the user who last changed the application object.</span></span>                                                        |
| <span data-ttu-id="d0cff-112">public Date changedDate(\[Date value\])</span><span class="sxs-lookup"><span data-stu-id="d0cff-112">public Date changedDate(\[Date value\])</span></span>                 | <span data-ttu-id="d0cff-113">アプリケーション オブジェクトが最後に変更された日付を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="d0cff-113">Gets or sets the date an application object was last changed.</span></span>                                                                     |
| <span data-ttu-id="d0cff-114">public str changedTime(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="d0cff-114">public str changedTime(\[str value\])</span></span>                   | <span data-ttu-id="d0cff-115">アプリケーション オブジェクトが最後に変更された時刻を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="d0cff-115">Gets or sets the time an application object was last changed.</span></span>                                                                     |
| <span data-ttu-id="d0cff-116">public str createdBy(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="d0cff-116">public str createdBy(\[str value\])</span></span>                     | <span data-ttu-id="d0cff-117">アプリケーション オブジェクトを作成したユーザーの名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="d0cff-117">Gets or sets the name of the user who created the application object.</span></span>                                                             |
| <span data-ttu-id="d0cff-118">public Date creationDate(\[Date value\])</span><span class="sxs-lookup"><span data-stu-id="d0cff-118">public Date creationDate(\[Date value\])</span></span>                | <span data-ttu-id="d0cff-119">アプリケーション オブジェクトが作成された日付を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="d0cff-119">Gets or sets the date an application object was created.</span></span>                                                                          |
| <span data-ttu-id="d0cff-120">public str creationTime(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="d0cff-120">public str creationTime(\[str value\])</span></span>                  |                                                                                                                                   |
| <span data-ttu-id="d0cff-121">public FormBuildDataSource dataSource(int dataSourceNo)</span><span class="sxs-lookup"><span data-stu-id="d0cff-121">public FormBuildDataSource dataSource(int dataSourceNo)</span></span> |                                                                                                                                   |
| <span data-ttu-id="d0cff-122">public int dataSourceCount()</span><span class="sxs-lookup"><span data-stu-id="d0cff-122">public int dataSourceCount()</span></span>                            |                                                                                                                                   |
| <span data-ttu-id="d0cff-123">public str name(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="d0cff-123">public str name(\[str value\])</span></span>                          | <span data-ttu-id="d0cff-124">フォーム、レポート、テーブル、クエリ、または他のアプリケーション オブジェクトを識別するためのコードで使用される名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="d0cff-124">Gets or sets the name used in code to identify a form, report, table, query, or other application object.</span></span> |
| <span data-ttu-id="d0cff-125">public Guid origin(\[Guid value\])</span><span class="sxs-lookup"><span data-stu-id="d0cff-125">public Guid origin(\[Guid value\])</span></span>                      |                                                                                                                                   |
| <span data-ttu-id="d0cff-126">public void load(str name, \[boolean buildMode\])</span><span class="sxs-lookup"><span data-stu-id="d0cff-126">public void load(str name, \[boolean buildMode\])</span></span>       |                                                                                                                                   |
| <span data-ttu-id="d0cff-127">public void finalize()</span><span class="sxs-lookup"><span data-stu-id="d0cff-127">public void finalize()</span></span>                                  |                                                                                                                                   |
| <span data-ttu-id="d0cff-128">public void new(\[str name\], \[boolean buildMode\])</span><span class="sxs-lookup"><span data-stu-id="d0cff-128">public void new(\[str name\], \[boolean buildMode\])</span></span>    | <span data-ttu-id="d0cff-129">TreeNode クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="d0cff-129">Initializes a new instance of the TreeNode class.</span></span>                                                                                 |
| <span data-ttu-id="d0cff-130">public void save()</span><span class="sxs-lookup"><span data-stu-id="d0cff-130">public void save()</span></span>                                      |                                                                                                                                   |

## <a name="method-adddatasource"></a><span data-ttu-id="d0cff-131">メソッド addDataSource</span><span class="sxs-lookup"><span data-stu-id="d0cff-131">Method addDataSource</span></span>

```xpp
public FormBuildDataSource addDataSource(str name)
```

### <a name="parameters---adddatasource"></a><span data-ttu-id="d0cff-132">パラメーター - addDataSource</span><span class="sxs-lookup"><span data-stu-id="d0cff-132">Parameters - addDataSource</span></span>

<span data-ttu-id="d0cff-133">名前</span><span class="sxs-lookup"><span data-stu-id="d0cff-133">name</span></span>  

### <a name="return-value---adddatasource"></a><span data-ttu-id="d0cff-134">戻り値 - addDataSource</span><span class="sxs-lookup"><span data-stu-id="d0cff-134">Return Value - addDataSource</span></span>

## <a name="method-changedby"></a><span data-ttu-id="d0cff-135">メソッド changedBy</span><span class="sxs-lookup"><span data-stu-id="d0cff-135">Method changedBy</span></span>

<span data-ttu-id="d0cff-136">アプリケーション オブジェクトを最後に変更したユーザーの名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="d0cff-136">Gets or sets the name of the user who last changed the application object.</span></span>

```xpp
public str changedBy([str value])
```

### <a name="parameters---changedby"></a><span data-ttu-id="d0cff-137">パラメーター - changedBy</span><span class="sxs-lookup"><span data-stu-id="d0cff-137">Parameters - changedBy</span></span>

<span data-ttu-id="d0cff-138">値</span><span class="sxs-lookup"><span data-stu-id="d0cff-138">value</span></span>  

### <a name="return-value---changedby"></a><span data-ttu-id="d0cff-139">戻り値 - changedBy</span><span class="sxs-lookup"><span data-stu-id="d0cff-139">Return Value - changedBy</span></span>

<span data-ttu-id="d0cff-140">ユーザーの名前。</span><span class="sxs-lookup"><span data-stu-id="d0cff-140">The name of the user.</span></span>

## <a name="method-changeddate"></a><span data-ttu-id="d0cff-141">メソッド changedDate</span><span class="sxs-lookup"><span data-stu-id="d0cff-141">Method changedDate</span></span>

<span data-ttu-id="d0cff-142">アプリケーション オブジェクトが最後に変更された日付を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="d0cff-142">Gets or sets the date an application object was last changed.</span></span>

```xpp
public Date changedDate([Date value])
```

### <a name="parameters---changeddate"></a><span data-ttu-id="d0cff-143">パラメーター - changedDate</span><span class="sxs-lookup"><span data-stu-id="d0cff-143">Parameters - changedDate</span></span>

<span data-ttu-id="d0cff-144">値</span><span class="sxs-lookup"><span data-stu-id="d0cff-144">value</span></span>  

### <a name="return-value---changeddate"></a><span data-ttu-id="d0cff-145">戻り値 - changedDate</span><span class="sxs-lookup"><span data-stu-id="d0cff-145">Return Value - changedDate</span></span>

<span data-ttu-id="d0cff-146">アプリケーション オブジェクトが最後に変更された日付。</span><span class="sxs-lookup"><span data-stu-id="d0cff-146">The date an application object was last changed.</span></span>

## <a name="method-changedtime"></a><span data-ttu-id="d0cff-147">メソッド changedTime</span><span class="sxs-lookup"><span data-stu-id="d0cff-147">Method changedTime</span></span>

<span data-ttu-id="d0cff-148">アプリケーション オブジェクトが最後に変更された時刻を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="d0cff-148">Gets or sets the time an application object was last changed.</span></span>

```xpp
public str changedTime([str value])
```

### <a name="parameters---changedtime"></a><span data-ttu-id="d0cff-149">パラメーター - changedTime</span><span class="sxs-lookup"><span data-stu-id="d0cff-149">Parameters - changedTime</span></span>

<span data-ttu-id="d0cff-150">値</span><span class="sxs-lookup"><span data-stu-id="d0cff-150">value</span></span>  

### <a name="return-value---changedtime"></a><span data-ttu-id="d0cff-151">戻り値 - changedTime</span><span class="sxs-lookup"><span data-stu-id="d0cff-151">Return Value - changedTime</span></span>

<span data-ttu-id="d0cff-152">アプリケーション オブジェクトが最後に変更された時間。</span><span class="sxs-lookup"><span data-stu-id="d0cff-152">The time an application object was last changed.</span></span>

## <a name="method-createdby"></a><span data-ttu-id="d0cff-153">メソッド createdBy</span><span class="sxs-lookup"><span data-stu-id="d0cff-153">Method createdBy</span></span>

<span data-ttu-id="d0cff-154">アプリケーション オブジェクトを作成したユーザーの名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="d0cff-154">Gets or sets the name of the user who created the application object.</span></span>

```xpp
public str createdBy([str value])
```

### <a name="parameters---createdby"></a><span data-ttu-id="d0cff-155">パラメーター - createdBy</span><span class="sxs-lookup"><span data-stu-id="d0cff-155">Parameters - createdBy</span></span>

<span data-ttu-id="d0cff-156">値</span><span class="sxs-lookup"><span data-stu-id="d0cff-156">value</span></span>  

### <a name="return-value---createdby"></a><span data-ttu-id="d0cff-157">戻り値 - createdBy</span><span class="sxs-lookup"><span data-stu-id="d0cff-157">Return Value - createdBy</span></span>

<span data-ttu-id="d0cff-158">ユーザーの名前。</span><span class="sxs-lookup"><span data-stu-id="d0cff-158">The name of the user.</span></span>

## <a name="method-creationdate"></a><span data-ttu-id="d0cff-159">メソッド creationDate</span><span class="sxs-lookup"><span data-stu-id="d0cff-159">Method creationDate</span></span>

<span data-ttu-id="d0cff-160">アプリケーション オブジェクトが作成された日付を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="d0cff-160">Gets or sets the date an application object was created.</span></span>

```xpp
public Date creationDate([Date value])
```

### <a name="parameters---creationdate"></a><span data-ttu-id="d0cff-161">パラメーター - creationDate</span><span class="sxs-lookup"><span data-stu-id="d0cff-161">Parameters - creationDate</span></span>

<span data-ttu-id="d0cff-162">値</span><span class="sxs-lookup"><span data-stu-id="d0cff-162">value</span></span>  

### <a name="return-value---creationdate"></a><span data-ttu-id="d0cff-163">戻り値 - creationDate</span><span class="sxs-lookup"><span data-stu-id="d0cff-163">Return Value - creationDate</span></span>

<span data-ttu-id="d0cff-164">アプリケーション オブジェクトが作成された日付。</span><span class="sxs-lookup"><span data-stu-id="d0cff-164">The date an application object was created.</span></span>

## <a name="method-creationtime"></a><span data-ttu-id="d0cff-165">メソッド creationTime</span><span class="sxs-lookup"><span data-stu-id="d0cff-165">Method creationTime</span></span>

```xpp
public str creationTime([str value])
```

### <a name="parameters---creationtime"></a><span data-ttu-id="d0cff-166">パラメーター - creationTime</span><span class="sxs-lookup"><span data-stu-id="d0cff-166">Parameters - creationTime</span></span>

<span data-ttu-id="d0cff-167">値</span><span class="sxs-lookup"><span data-stu-id="d0cff-167">value</span></span>  

### <a name="return-value---creationtime"></a><span data-ttu-id="d0cff-168">戻り値 - creationTime</span><span class="sxs-lookup"><span data-stu-id="d0cff-168">Return Value - creationTime</span></span>

## <a name="method-datasource"></a><span data-ttu-id="d0cff-169">メソッド dataSource</span><span class="sxs-lookup"><span data-stu-id="d0cff-169">Method dataSource</span></span>

```xpp
public FormBuildDataSource dataSource(int dataSourceNo)
```

### <a name="parameters---datasource"></a><span data-ttu-id="d0cff-170">パラメーター - dataSource</span><span class="sxs-lookup"><span data-stu-id="d0cff-170">Parameters - dataSource</span></span>

<span data-ttu-id="d0cff-171">dataSourceNo</span><span class="sxs-lookup"><span data-stu-id="d0cff-171">dataSourceNo</span></span>  

### <a name="return-value---datasource"></a><span data-ttu-id="d0cff-172">戻り値 - dataSource</span><span class="sxs-lookup"><span data-stu-id="d0cff-172">Return Value - dataSource</span></span>

## <a name="method-datasourcecount"></a><span data-ttu-id="d0cff-173">メソッド dataSourceCount</span><span class="sxs-lookup"><span data-stu-id="d0cff-173">Method dataSourceCount</span></span>

```xpp
public int dataSourceCount()
```

### <a name="return-value---datasourcecount"></a><span data-ttu-id="d0cff-174">戻り値 - dataSourceCount</span><span class="sxs-lookup"><span data-stu-id="d0cff-174">Return Value - dataSourceCount</span></span>

## <a name="method-name"></a><span data-ttu-id="d0cff-175">メソッド名</span><span class="sxs-lookup"><span data-stu-id="d0cff-175">Method name</span></span>

<span data-ttu-id="d0cff-176">フォーム、レポート、テーブル、クエリ、または他のアプリケーション オブジェクトを識別するためのコードで使用される名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="d0cff-176">Gets or sets the name used in code to identify a form, report, table, query, or other application object.</span></span>

```xpp
public str name([str value])
```

### <a name="parameters---name"></a><span data-ttu-id="d0cff-177">パラメーター - 名前</span><span class="sxs-lookup"><span data-stu-id="d0cff-177">Parameters - name</span></span>

<span data-ttu-id="d0cff-178">値</span><span class="sxs-lookup"><span data-stu-id="d0cff-178">value</span></span>  

### <a name="return-value---name"></a><span data-ttu-id="d0cff-179">戻り値 - name</span><span class="sxs-lookup"><span data-stu-id="d0cff-179">Return Value - name</span></span>

<span data-ttu-id="d0cff-180">アプリケーション オブジェクトを識別するためにコードで使用される名前。</span><span class="sxs-lookup"><span data-stu-id="d0cff-180">The name used in code to identify an application object.</span></span>

### <a name="remarks---name"></a><span data-ttu-id="d0cff-181">備考 - 名前</span><span class="sxs-lookup"><span data-stu-id="d0cff-181">Remarks - name</span></span>

<span data-ttu-id="d0cff-182">オブジェクトの名前プロパティ値は、コードの競合を避けるために、次の基準を満たしている必要があります。</span><span class="sxs-lookup"><span data-stu-id="d0cff-182">The name property value of an object must meet the following criteria to avoid code conflicts:</span></span>

-   <span data-ttu-id="d0cff-183">文字で始めます。</span><span class="sxs-lookup"><span data-stu-id="d0cff-183">Begins with a letter.</span></span>
-   <span data-ttu-id="d0cff-184">250 文字を超えないでください。</span><span class="sxs-lookup"><span data-stu-id="d0cff-184">Doesn't exceed 250 characters.</span></span>
-   <span data-ttu-id="d0cff-185">数字とアンダースコア文字を含めることができます。</span><span class="sxs-lookup"><span data-stu-id="d0cff-185">Can include numbers and underscore characters.</span></span>
-   <span data-ttu-id="d0cff-186">句読点やスペースを含めることはできません。</span><span class="sxs-lookup"><span data-stu-id="d0cff-186">Cannot include punctuation or spaces.</span></span>
-   <span data-ttu-id="d0cff-187">テーブルは、拡張データ型、基本列挙型、クラスなどの他のパブリック オブジェクトと同じ名前を持つことはできません。</span><span class="sxs-lookup"><span data-stu-id="d0cff-187">Tables cannot have the same name as other public objects, such as extended data types, base enumeration types, classes, and so on.</span></span>

## <a name="method-origin"></a><span data-ttu-id="d0cff-188">メソッド origin</span><span class="sxs-lookup"><span data-stu-id="d0cff-188">Method origin</span></span>

```xpp
public Guid origin([Guid value])
```

### <a name="parameters---origin"></a><span data-ttu-id="d0cff-189">パラメーター - origin</span><span class="sxs-lookup"><span data-stu-id="d0cff-189">Parameters - origin</span></span>

<span data-ttu-id="d0cff-190">値</span><span class="sxs-lookup"><span data-stu-id="d0cff-190">value</span></span>  

### <a name="return-value---origin"></a><span data-ttu-id="d0cff-191">戻り値 - origin</span><span class="sxs-lookup"><span data-stu-id="d0cff-191">Return Value - origin</span></span>

## <a name="method-load"></a><span data-ttu-id="d0cff-192">メソッド load</span><span class="sxs-lookup"><span data-stu-id="d0cff-192">Method load</span></span>

```xpp
public void load(str name, [boolean buildMode])
```

### <a name="parameters---load"></a><span data-ttu-id="d0cff-193">パラメーター - load</span><span class="sxs-lookup"><span data-stu-id="d0cff-193">Parameters - load</span></span>

<span data-ttu-id="d0cff-194">名前</span><span class="sxs-lookup"><span data-stu-id="d0cff-194">name</span></span>  

<!-- -->

<span data-ttu-id="d0cff-195">buildMode</span><span class="sxs-lookup"><span data-stu-id="d0cff-195">buildMode</span></span>  

## <a name="method-finalize"></a><span data-ttu-id="d0cff-196">メソッド finalize</span><span class="sxs-lookup"><span data-stu-id="d0cff-196">Method finalize</span></span>

```xpp
public void finalize()
```

## <a name="method-new"></a><span data-ttu-id="d0cff-197">メソッド new</span><span class="sxs-lookup"><span data-stu-id="d0cff-197">Method new</span></span>

<span data-ttu-id="d0cff-198">TreeNode クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="d0cff-198">Initializes a new instance of the TreeNode class.</span></span>

```xpp
public void new([str name], [boolean buildMode])
```

### <a name="parameters---new"></a><span data-ttu-id="d0cff-199">パラメーター - new</span><span class="sxs-lookup"><span data-stu-id="d0cff-199">Parameters - new</span></span>

<span data-ttu-id="d0cff-200">名前</span><span class="sxs-lookup"><span data-stu-id="d0cff-200">name</span></span>  

<!-- -->

<span data-ttu-id="d0cff-201">buildMode</span><span class="sxs-lookup"><span data-stu-id="d0cff-201">buildMode</span></span>  

## <a name="method-save"></a><span data-ttu-id="d0cff-202">メソッド save</span><span class="sxs-lookup"><span data-stu-id="d0cff-202">Method save</span></span>

```xpp
public void save()
```

